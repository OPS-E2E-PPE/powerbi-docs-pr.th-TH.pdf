---
title: ลงทะเบียนแอปเพื่อฝังเนื้อหา Power BI ในแอปพลิเคชันการวิเคราะห์แบบฝังตัวของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: เรียนรู้วิธีการลงทะเบียนแอปพลิเคชันภายใน Azure Active Directory สำหรับการใช้งานด้วยการฝังเนื้อหา Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: nishalit
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: how-to
ms.date: 04/02/2019
ms.openlocfilehash: 624e0a2838a08d1cf68ae58223fe979a56312b48
ms.sourcegitcommit: 1cad78595cca1175b82c04458803764ac36e5e37
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/19/2021
ms.locfileid: "98565926"
---
# <a name="register-an-azure-ad-application-to-use-with-power-bi"></a><span data-ttu-id="3eb25-104">ลงทะเบียนแอปพลิเคชัน Azure AD เพื่อใช้กับ Power BI</span><span class="sxs-lookup"><span data-stu-id="3eb25-104">Register an Azure AD application to use with Power BI</span></span>

<span data-ttu-id="3eb25-105">เมื่อต้องการใช้การวิเคราะห์แบบฝังตัวของ Power BI คุณต้องลงทะเบียนแอปพลิเคชัน Azure Active Directory (Azure AD) ใน Azure</span><span class="sxs-lookup"><span data-stu-id="3eb25-105">To use Power BI embedded analytics, you need to register an Azure Active Directory (Azure AD) application in Azure.</span></span> <span data-ttu-id="3eb25-106">แอป Azure AD สร้างสิทธิ์สำหรับทรัพยากร Power BI REST และอนุญาตให้เข้าถึง [Power BI REST APIs](/rest/api/power-bi/)</span><span class="sxs-lookup"><span data-stu-id="3eb25-106">The Azure AD app establishes permissions for Power BI REST resources, and allows access to the [Power BI REST APIs](/rest/api/power-bi/).</span></span>

## <a name="determine-your-embedding-solution"></a><span data-ttu-id="3eb25-107">กำหนดโซลูชันการฝังตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-107">Determine your embedding solution</span></span>

<span data-ttu-id="3eb25-108">ก่อนลงทะเบียนแอปของคุณ ให้ตัดสินใจว่าโซลูชันใดต่อไปนี้เหมาะสมที่สุดสำหรับคุณ:</span><span class="sxs-lookup"><span data-stu-id="3eb25-108">Before registering your app, decide which of the following solutions is best suited for you:</span></span>

* <span data-ttu-id="3eb25-109">ฝังตัวสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-109">Embed for your customers</span></span>
* <span data-ttu-id="3eb25-110">ฝังตัวสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-110">Embed for your organization</span></span>

### <a name="embed-for-your-customers"></a><span data-ttu-id="3eb25-111">ฝังตัวสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-111">Embed for your customers</span></span>

<span data-ttu-id="3eb25-112">ใช้โซลูชัน [ฝังตัวสำหรับลูกค้าของคุณ](embed-sample-for-customers.md) หรือที่เรียกว่า *แอปเป็นเจ้าของข้อมูล* หากคุณกำลังวางแผนที่จะสร้างแอปพลิเคชันที่ออกแบบมาสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-112">Use the [embed for your customers](embed-sample-for-customers.md) solution, also known as *app owns data*, if you're planning to create an application that's designed for your customers.</span></span> <span data-ttu-id="3eb25-113">ผู้ใช้จะไม่จำเป็นต้องลงชื่อเข้าใช้ Power BI หรือไม่จำเป็นต้องมีสิทธิการใช้งาน Power BI เพื่อใช้แอปพลิเคชันของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-113">Users will not need to sign in to Power BI or have a Power BI license, to use your application.</span></span> <span data-ttu-id="3eb25-114">แอปพลิเคชันของคุณจะใช้วิธีใดวิธีหนึ่งต่อไปนี้เพื่อรับรองความถูกต้องกับ Power BI:</span><span class="sxs-lookup"><span data-stu-id="3eb25-114">Your application will use one of the following methods to authenticate against Power BI:</span></span>

* <span data-ttu-id="3eb25-115">บัญชี **ผู้ใช้หลัก** (สิทธิการใช้งาน Power BI Pro ใช้สำหรับการลงชื่อเข้าใช้ Power BI)</span><span class="sxs-lookup"><span data-stu-id="3eb25-115">**Master user** account (a Power BI Pro license used for signing in to Power BI)</span></span>

* [<span data-ttu-id="3eb25-116">โครงร่างสำคัญของบริการ</span><span class="sxs-lookup"><span data-stu-id="3eb25-116">Service principal</span></span>](embed-service-principal.md)

<span data-ttu-id="3eb25-117">โซลูชันฝังตัวสำหรับลูกค้าของคุณมักจะถูกใช้โดยผู้จำหน่ายซอฟต์แวร์อิสระ (ISVs) และนักพัฒนาที่กำลังสร้างแอปพลิเคชันสำหรับบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="3eb25-117">The embed for your customers solution is usually used by independent software vendors (ISVs) and developers who are creating applications for a third party.</span></span>

### <a name="embed-for-your-organization"></a><span data-ttu-id="3eb25-118">ฝังตัวสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-118">Embed for your organization</span></span>

<span data-ttu-id="3eb25-119">ใช้โซลูชัน [ฝังตัวสำหรับองค์กรของคุณ](embed-sample-for-your-organization.md) หรือที่เรียกว่า *ผู้ใช้เป็นเจ้าของข้อมูล* ถ้าคุณกำลังวางแผนที่จะสร้างแอปพลิเคชันที่ต้องการให้ผู้ใช้ใช้ข้อมูลประจำตัวของพวกเขาเพื่อรับรองความถูกต้องกับ Power BI</span><span class="sxs-lookup"><span data-stu-id="3eb25-119">Use the [embed for your organization](embed-sample-for-your-organization.md) solution, also known as *user owns data*, if you're planning to create an application  that requires users to use their credentials to authenticate against Power BI.</span></span>

<span data-ttu-id="3eb25-120">โซลูชันฝังตัวสำหรับองค์กรของคุณมักจะใช้โดยวิสาหกิจและองค์กรขนาดใหญ่ และมีไว้สำหรับผู้ใช้ภายใน</span><span class="sxs-lookup"><span data-stu-id="3eb25-120">The embed for your organization solution is usually used by enterprises and big organizations, and is intended for internal users.</span></span>

## <a name="register-an-azure-ad-app"></a><span data-ttu-id="3eb25-121">ลงทะเบียนแอป Azure AD</span><span class="sxs-lookup"><span data-stu-id="3eb25-121">Register an Azure AD app</span></span>

<span data-ttu-id="3eb25-122">วิธีที่ง่ายที่สุดในการลงทะเบียนแอป Azure AD คือการใช้[เครื่องมือตั้งค่าการฝัง Power BI](https://app.powerbi.com/embedsetup)</span><span class="sxs-lookup"><span data-stu-id="3eb25-122">The easiest way to register an Azure AD app, is by using the  [Power BI embedding setup tool](https://app.powerbi.com/embedsetup).</span></span> <span data-ttu-id="3eb25-123">เครื่องมือนี้มีกระบวนการลงทะเบียนที่รวดเร็วสำหรับโซลูชันการฝังทั้งสองโดยใช้อินเทอร์เฟซแบบกราฟิกที่เรียบง่าย</span><span class="sxs-lookup"><span data-stu-id="3eb25-123">The tool offers a quick registration process for both embedding solutions, using a simple graphical interface.</span></span>

<span data-ttu-id="3eb25-124">ถ้าคุณกำลังสร้างแอปพลิเคชันแบบ *ฝังตัวสำหรับองค์กรของคุณ* และต้องการควบคุมแอป Azure AD ของคุณมากขึ้น คุณสามารถลงทะเบียนได้ด้วยตนเองในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="3eb25-124">If you're creating an *embed for your organization* application, and want more control over your Azure AD app, you can register it manually in the Azure portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3eb25-125">ก่อนที่คุณลงทะเบียนแอป Power BI คุณต้องการ[ผู้เช่า Azure Active Directory และผู้ใช้ขององค์กร](create-an-azure-active-directory-tenant.md)</span><span class="sxs-lookup"><span data-stu-id="3eb25-125">Before you register a Power BI app you need an [Azure Active Directory tenant and an organizational user](create-an-azure-active-directory-tenant.md).</span></span>

# <a name="embed-for-your-customers"></a>[<span data-ttu-id="3eb25-126">ฝังสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-126">Embed for your customers</span></span>](#tab/customers)

<span data-ttu-id="3eb25-127">ขั้นตอนเหล่านี้จะอธิบายวิธีการลงทะเบียนแอปพลิเคชัน Azure AD สำหรับโซลูชัน[ฝังตัวสำหรับลูกค้าของคุณ](embed-sample-for-customers.md)ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3eb25-127">These steps describe how to register an Azure AD application for the Power BI [embed for your customers](embed-sample-for-customers.md) solution.</span></span>

[!INCLUDE[registration tool step 1](../../includes/register-tool-step-1.md)]

2. <span data-ttu-id="3eb25-128">ในส่วน *เลือกโซลูชันการฝังตัว* ให้เลือก **ฝังตัวสำหรับลูกค้าของคุณ**</span><span class="sxs-lookup"><span data-stu-id="3eb25-128">In the *Choose an embedding solution* section, select **Embed for your customers**.</span></span>

[!INCLUDE[registration tool step 3](../../includes/register-tool-step-3.md)]

4. <span data-ttu-id="3eb25-129">ใน *ขั้นตอนที่ 2 - ลงทะเบียนแอปพลิเคชันของคุณ* ให้กรอกเขตข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3eb25-129">In *Step 2 - Register your application*, fill in the following fields:</span></span>

    * <span data-ttu-id="3eb25-130">**ชื่อแอปพลิเคชัน** - ตั้งชื่อให้แอปพลิเคชันของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-130">**Application Name** - Give your application a name.</span></span>

    * <span data-ttu-id="3eb25-131">**การเข้าถึง API** - เลือก Power BI APIs (หรือที่เรียกว่าขอบเขต) ที่แอปพลิเคชันของคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="3eb25-131">**API access** - Select the Power BI APIs (also known as scopes) that your application needs.</span></span> <span data-ttu-id="3eb25-132">คุณสามารถใช้ *เลือกทั้งหมด* เพื่อเลือก APIs ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3eb25-132">You can use *Select all* to select all the APIs.</span></span> <span data-ttu-id="3eb25-133">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสิทธิ์การเข้าถึง Power BI ให้ดู [สิทธิ์และการยินยอมในจุดสิ้นสุดของแพลตฟอร์มข้อมูลประจำตัวของ Microsoft](/azure/active-directory/develop/v2-permissions-and-consent)</span><span class="sxs-lookup"><span data-stu-id="3eb25-133">For more information about Power BI access permissions, see [Permissions and consent in the Microsoft identity platform endpoint](/azure/active-directory/develop/v2-permissions-and-consent).</span></span>

5. <span data-ttu-id="3eb25-134">เลือก **ลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="3eb25-134">Select **Register**.</span></span>

    <span data-ttu-id="3eb25-135">**ID แอปพลิเคชัน** สำหรับแอป Azure AD ของคุณจะแสดงอยู่ในกล่อง *สรุป*</span><span class="sxs-lookup"><span data-stu-id="3eb25-135">Your Azure AD app **Application ID** is displayed in the *Summary* box.</span></span> <span data-ttu-id="3eb25-136">คัดลอกค่านี้เพื่อใช้งานในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="3eb25-136">Copy this value for later use.</span></span>

[!INCLUDE[registration tool steps 6-7](../../includes/register-tool-steps-6-7.md)]

8. <span data-ttu-id="3eb25-137">ใน *ขั้นตอนที่ 5 - ให้สิทธิ์* ให้เลือก **ให้สิทธิ์** และเลือก **ยอมรับ** ในหน้าต่างป็อปอัพ</span><span class="sxs-lookup"><span data-stu-id="3eb25-137">In *Step 5 - Grant permissions*, select **Grant permissions** and in the pop-up window select **accept**.</span></span> <span data-ttu-id="3eb25-138">ซึ่งจะช่วยให้แอป Azure AD ของคุณสามารถเข้าถึง APIs ที่คุณเลือก (หรือที่เรียกว่าขอบเขต) ด้วยผู้ใช้ที่ลงชื่อเข้าใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-138">This allows your Azure AD app to access the APIs you selected (also known as scopes) with your signed in user.</span></span> <span data-ttu-id="3eb25-139">ผู้ใช้รายนี้ถุกเรียกอีกอย่างว่า **ผู้ใช้หลัก**</span><span class="sxs-lookup"><span data-stu-id="3eb25-139">This user is also known as the **master user**.</span></span>

9. <span data-ttu-id="3eb25-140">(ไม่บังคับ) ถ้าคุณสร้างพื้นที่ทำงาน Power BI และอัปโหลดเนื้อหาโดยใช้เครื่องมือ ตอนนี้คุณสามารถเลือก **ดาวน์โหลดแอปพลิเคชันตัวอย่าง** ได้</span><span class="sxs-lookup"><span data-stu-id="3eb25-140">(Optional) If you created a Power BI workspace and uploaded content to it using the tool, you can now select **Download sample application**.</span></span> <span data-ttu-id="3eb25-141">อย่าลืมคัดลอกข้อมูลทั้งหมดในช่อง *สรุป*</span><span class="sxs-lookup"><span data-stu-id="3eb25-141">Make sure you copy all the information in the *Summary* Box.</span></span>

[!INCLUDE[registration tool note](../../includes/register-tool-note.md)]

# <a name="embed-for-your-organization"></a>[<span data-ttu-id="3eb25-142">ฝังตัวสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-142">Embed for your organization</span></span>](#tab/organization)

<span data-ttu-id="3eb25-143">ขั้นตอนเหล่านี้จะอธิบายวิธีการลงทะเบียนแอปพลิเคชัน Azure AD สำหรับโซลูชัน[ฝังตัวสำหรับองค์กรของคุณ](embed-sample-for-your-organization.md)ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3eb25-143">These steps describe how to register an Azure AD application for the Power BI [embed for your organization](embed-sample-for-your-organization.md) solution.</span></span>

[!INCLUDE[registration tool step 1](../../includes/register-tool-step-1.md)]

2. <span data-ttu-id="3eb25-144">ในส่วน *เลือกโซลูชันการฝังตัว* ให้เลือก **ฝังตัวสำหรับองค์กรของคุณ**</span><span class="sxs-lookup"><span data-stu-id="3eb25-144">In the *Choose an embedding solution* section, select **Embed for your organization**.</span></span>

[!INCLUDE[registration tool step 3](../../includes/register-tool-step-3.md)]

4. <span data-ttu-id="3eb25-145">ใน *ขั้นตอนที่ 2 - ลงทะเบียนแอปพลิเคชันของคุณ* ให้กรอกเขตข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3eb25-145">In *Step 2 - Register your application*, fill in the following fields:</span></span>

    * <span data-ttu-id="3eb25-146">**ชื่อแอปพลิเคชัน** - ตั้งชื่อให้แอปพลิเคชันของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-146">**Application Name** - Give your application a name.</span></span>

    * <span data-ttu-id="3eb25-147">**URL ของโฮมเพจ** - ป้อน URL สำหรับโฮมเพจของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-147">**Home Page URL** - Enter a URL for your home page.</span></span>

    * <span data-ttu-id="3eb25-148">**URL เปลี่ยนเส้นทาง** - เมื่อลงชื่อเข้าใช้ ผู้ใช้แอปพลิเคชันของคุณจะถูกเปลี่ยนเส้นทางไปยังที่อยู่นี้ในขณะที่แอปพลิเคชันของคุณได้รับรหัสรับรองความถูกต้องจาก Azure</span><span class="sxs-lookup"><span data-stu-id="3eb25-148">**Redirect URL** - Upon singing in, your application users will be redirected to this address while your application receives an authentication code from Azure.</span></span> <span data-ttu-id="3eb25-149">เลือกหนึ่งในตัวเลือกเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="3eb25-149">Select one of these options:</span></span>

        * <span data-ttu-id="3eb25-150">**ใช้ URL ค่าเริ่มต้น** - ตัวเลือกนี้จะสร้างและดาวน์โหลดตัวอย่างแอปพลิเคชันการวิเคราะห์แบบฝังตัวโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3eb25-150">**Use a default URL** - This option will automatically create and download a sample embedded analytics application.</span></span> <span data-ttu-id="3eb25-151">URL ค่าเริ่มต้นคือ http://localhost:13526/</span><span class="sxs-lookup"><span data-stu-id="3eb25-151">The default URL is http://localhost:13526/.</span></span>

        * <span data-ttu-id="3eb25-152">**ใช้ URL ที่กำหนดเอง** - เลือกตัวเลือกนี้หากคุณมีแอปพลิเคชันการวิเคราะห์แบบฝังตัวอยู่แล้ว และทราบว่าคุณต้องการใช้อะไรเป็น URL เปลี่ยนเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="3eb25-152">**Use a custom URL** - Select this option if you already have an embedded analytics application, and know what you want to use as a redirect URL.</span></span>

    * <span data-ttu-id="3eb25-153">**การเข้าถึง API** - เลือก Power BI APIs (หรือที่เรียกว่าขอบเขต) ที่แอปพลิเคชันของคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="3eb25-153">**API access** - Select the Power BI APIs (also known as scopes) that your application needs.</span></span> <span data-ttu-id="3eb25-154">คุณสามารถใช้ *เลือกทั้งหมด* เพื่อเลือก APIs ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3eb25-154">You can use *Select all* to select all the APIs.</span></span> <span data-ttu-id="3eb25-155">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสิทธิ์การเข้าถึง Power BI ให้ดู [สิทธิ์และการยินยอมในจุดสิ้นสุดของแพลตฟอร์มข้อมูลประจำตัวของ Microsoft](/azure/active-directory/develop/v2-permissions-and-consent)</span><span class="sxs-lookup"><span data-stu-id="3eb25-155">For more information about Power BI access permissions, see [Permissions and consent in the Microsoft identity platform endpoint](/azure/active-directory/develop/v2-permissions-and-consent).</span></span>

5. <span data-ttu-id="3eb25-156">เลือก **ลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="3eb25-156">Select **Register**.</span></span>

    <span data-ttu-id="3eb25-157">**ID แอปพลิเคชัน** และค่า **รหัสลับแอปพลิเคชัน** ของแอป Azure AD ของคุณจะแสดงในกล่อง *สรุป*</span><span class="sxs-lookup"><span data-stu-id="3eb25-157">Your Azure AD app **Application ID** and **Application secret** values are displayed in the *Summary* box.</span></span> <span data-ttu-id="3eb25-158">คัดลอกค่าเหล่านี้เพื่อใช้งานในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="3eb25-158">Copy these values for later use.</span></span>

[!INCLUDE[registration tool steps 6-7](../../includes/register-tool-steps-6-7.md)]

8. <span data-ttu-id="3eb25-159">(ไม่บังคับ) ถ้าคุณสร้างพื้นที่ทำงาน Power BI และอัปโหลดเนื้อหาโดยใช้เครื่องมือ ตอนนี้คุณสามารถเลือก **ดาวน์โหลดแอปพลิเคชันตัวอย่าง** ได้</span><span class="sxs-lookup"><span data-stu-id="3eb25-159">(Optional) If you created a Power BI workspace and uploaded content to it using the tool, you can now select **Download sample application**.</span></span> <span data-ttu-id="3eb25-160">อย่าลืมคัดลอกข้อมูลทั้งหมดในช่อง *สรุป*</span><span class="sxs-lookup"><span data-stu-id="3eb25-160">Make sure you copy all the information in the *Summary* Box.</span></span>

[!INCLUDE[registration tool note](../../includes/register-tool-note.md)]

# <a name="manual-registration"></a>[<span data-ttu-id="3eb25-161">การลงทะเบียนด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="3eb25-161">Manual registration</span></span>](#tab/manual)

<span data-ttu-id="3eb25-162">ใช้การลงทะเบียนแอป Azure AD ด้วยตนเองเฉพาะในกรณีที่คุณกำลังสร้างหนึ่งในโซลูชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3eb25-162">Use the Azure AD manual app registration only if you're creating one of the following solutions:</span></span>

* <span data-ttu-id="3eb25-163">แอปพลิเคชัน *การฝังตัวสำหรับองค์กรของคุณ*</span><span class="sxs-lookup"><span data-stu-id="3eb25-163">An *embed for your organization* application.</span></span>

* <span data-ttu-id="3eb25-164">แอปพลิเคชัน *การฝังตัวสำหรับลูกค้าของคุณ* ด้วย *โครงร่างสำคัญของบริการ*</span><span class="sxs-lookup"><span data-stu-id="3eb25-164">An *embed for your customers* application with a *service principal*.</span></span>

    >[!NOTE]
    ><span data-ttu-id="3eb25-165">ถ้าคุณเลือกตัวเลือกนี้ หลังจากที่คุณลงทะเบียนแอป Azure AD ของคุณ คุณจะต้อง[เพิ่มสิทธิ์ Power BI](#change-your-azure-ad-apps-permissions)</span><span class="sxs-lookup"><span data-stu-id="3eb25-165">If you choose this option, after you register your Azure AD app you'll have to [add Power BI permissions](#change-your-azure-ad-apps-permissions) to it.</span></span>

<span data-ttu-id="3eb25-166">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการลงทะเบียนแอปพลิเคชันใน Azure Active Directory ดู[กาลงทะเบียนใช้แอปพลิเคชันด้วย Azure Active Directory](/azure/active-directory/develop/quickstart-v2-register-an-app)</span><span class="sxs-lookup"><span data-stu-id="3eb25-166">For more information about how to register applications in Azure Active Directory, see [Register an app with the Azure Active Directory](/azure/active-directory/develop/quickstart-v2-register-an-app).</span></span>

1. <span data-ttu-id="3eb25-167">ลงชื่อเข้าใช้[พอร์ทัล Azure](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="3eb25-167">Sign into the [Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="3eb25-168">เลือกผู้เช่า Azure AD ของคุณ โดยการเลือกบัญชีของคุณในมุมบนขวาของหน้า</span><span class="sxs-lookup"><span data-stu-id="3eb25-168">Select your Azure AD tenant by selecting your account in the upper right corner of the page.</span></span>

3. <span data-ttu-id="3eb25-169">เลือก **การลงทะเบียนแอป**</span><span class="sxs-lookup"><span data-stu-id="3eb25-169">Select **App registrations**.</span></span> <span data-ttu-id="3eb25-170">หากคุณไม่เห็นตัวเลือกนี้ ให้ค้นหา</span><span class="sxs-lookup"><span data-stu-id="3eb25-170">If you can't see this option, search for it.</span></span>
 
4. <span data-ttu-id="3eb25-171">ใน *การลงทะเบียนแอป* ให้เลือก **การลงทะเบียนใหม่**</span><span class="sxs-lookup"><span data-stu-id="3eb25-171">In *App registrations*, select **New registration**.</span></span>

5. <span data-ttu-id="3eb25-172">กรอกข้อมูลในเขตข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3eb25-172">Fill in the following fields:</span></span>

    * <span data-ttu-id="3eb25-173">**ชื่อ** - ตั้งชื่อให้แอปพลิเคชันของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-173">**Name** - Give your application a name.</span></span>

    * <span data-ttu-id="3eb25-174">**ชนิดบัญชีที่รองรับ** - เลือกผู้ที่สามารถใช้แอปพลิเคชันได้</span><span class="sxs-lookup"><span data-stu-id="3eb25-174">**Supported account type** - Select who can use the application.</span></span>

6. <span data-ttu-id="3eb25-175">(ไม่บังคับ) ใน **URI เปลี่ยนเส้นทาง** ให้เพิ่ม URL เปลี่ยนเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="3eb25-175">(Optional) In the **Redirect URI**, add a redirect URL.</span></span>

7. <span data-ttu-id="3eb25-176">เลือก **ลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="3eb25-176">Select **Register**.</span></span> <span data-ttu-id="3eb25-177">หลังจากลงทะเบียนแอปแล้ว คุณจะเข้าสู่หน้าภาพรวมของแอปซึ่งคุณสามารถรับ *ID แอปพลิเคชัน*</span><span class="sxs-lookup"><span data-stu-id="3eb25-177">After your app is registered you're directed to your app's overview page, where you can obtain the *Application ID*.</span></span>

---

## <a name="change-your-azure-ad-apps-permissions"></a><span data-ttu-id="3eb25-178">เปลี่ยนสิทธิ์ของแอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-178">Change your Azure AD app's permissions</span></span>

<span data-ttu-id="3eb25-179">หลังจากที่คุณลงทะเบียนแอปพลิเคชันของคุณแล้ว คุณสามารถทำการเปลี่ยนแปลงสิทธิ์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="3eb25-179">After you register your application, you can make changes to its permissions.</span></span> <span data-ttu-id="3eb25-180">การเปลี่ยนแปลงสิทธิ์สามารถทำได้ผ่านการกำหนดด้วยโปรแกรมหรือในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="3eb25-180">Permission changes can be made programmatically, or in the Azure portal.</span></span>

>[!NOTE]
><span data-ttu-id="3eb25-181">สิทธิ์ของแอป Azure AD ใช้ได้กับโซลูชัน *การฝังตัวสำหรับลูกค้าของคุณ* ด้วยวิธีการรับรองความถูกต้อง *ผู้ใช้หลัก* เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3eb25-181">Azure AD app permissions are only applicable for the *embed for your customers* solution with the *master user* authentication method.</span></span>

# <a name="azure"></a>[<span data-ttu-id="3eb25-182">Azure</span><span class="sxs-lookup"><span data-stu-id="3eb25-182">Azure</span></span>](#tab/Azure)

<span data-ttu-id="3eb25-183">ในพอร์ทัล Azure คุณสามารถดูแอปของคุณและทำการเปลี่ยนแปลงสิทธิ์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="3eb25-183">In the Azure portal, you can view your app and make changes to its permissions.</span></span>

1. <span data-ttu-id="3eb25-184">ลงชื่อเข้าใช้[พอร์ทัล Azure](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="3eb25-184">Sign into the [Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="3eb25-185">เลือกผู้เช่า Azure AD ของคุณ โดยการเลือกบัญชีของคุณในมุมบนขวาของหน้า</span><span class="sxs-lookup"><span data-stu-id="3eb25-185">Select your Azure AD tenant by selecting your account in the upper right corner of the page.</span></span>

3. <span data-ttu-id="3eb25-186">เลือก **การลงทะเบียนแอป**</span><span class="sxs-lookup"><span data-stu-id="3eb25-186">Select **App registrations**.</span></span> <span data-ttu-id="3eb25-187">หากคุณไม่เห็นตัวเลือกนี้ ให้ค้นหา</span><span class="sxs-lookup"><span data-stu-id="3eb25-187">If you can't see this option, search for it.</span></span>

4. <span data-ttu-id="3eb25-188">จากแท็บ **แอปพลิเคชันที่เป็นเจ้า** ให้เลือกแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-188">From the **Owned applications** tab, select your app.</span></span> <span data-ttu-id="3eb25-189">แอปพลิเคชันจะเปิดขึ้นในแท็บ *ภาพรวม* ซึ่งคุณสามารถตรวจสอบ *ID แอปพลิเคชัน* ได้</span><span class="sxs-lookup"><span data-stu-id="3eb25-189">The application opens in the *Overview* tab, where you can review the *Application ID*.</span></span>

5. <span data-ttu-id="3eb25-190">เลือกแท็บ **สิทธิ์ API**</span><span class="sxs-lookup"><span data-stu-id="3eb25-190">Select the **API permissions** tab.</span></span>

6. <span data-ttu-id="3eb25-191">เมื่อต้องเพิ่มสิทธิ์ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="3eb25-191">To add permissions, follow these steps:</span></span>

    1. <span data-ttu-id="3eb25-192">เลือก **เพิ่มสิทธิ์** จากนั้นเลือก **บริการ Power BI**</span><span class="sxs-lookup"><span data-stu-id="3eb25-192">Select **Add a permission** and then select **Power BI service**.</span></span>

    2. <span data-ttu-id="3eb25-193">เลือก **สิทธิ์ที่ได้รับมอบหมาย** และเพิ่มหรือลบสิทธิ์เฉพาะที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="3eb25-193">Select **Delegated Permissions** and add or remove the specific permissions you need.</span></span>

    3. <span data-ttu-id="3eb25-194">เมื่อคุณทำเสร็จแล้ว ให้เลือก **เพิ่มสิทธิ์** เพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-194">When you're done, select **Add permissions** to save your changes.</span></span>

7. <span data-ttu-id="3eb25-195">เมื่อต้องการเอาสิทธิ์ออก ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="3eb25-195">To remove a permission, follow these steps:</span></span>

    1. <span data-ttu-id="3eb25-196">เลือกจุดไข่ปลา (...) ทางด้านขวาของสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="3eb25-196">Select the ellipsis (...) to the right of the permission.</span></span>
    
    2. <span data-ttu-id="3eb25-197">เลือก **เอาสิทธิ์ออก**</span><span class="sxs-lookup"><span data-stu-id="3eb25-197">Select **Remove permission**.</span></span>
    
    3. <span data-ttu-id="3eb25-198">ในหน้าต่างป็อปอัพ *เอาสิทธิ์ออก* ให้เลือก **ใช่ เอาออก**</span><span class="sxs-lookup"><span data-stu-id="3eb25-198">In the *Remove permission* pop-up window, select **Yes, remove**.</span></span>

# <a name="http"></a>[<span data-ttu-id="3eb25-199">HTTP</span><span class="sxs-lookup"><span data-stu-id="3eb25-199">HTTP</span></span>](#tab/HTTP)

<span data-ttu-id="3eb25-200">เมื่อต้องการเปลี่ยนสิทธิ์แอป Azure AD ของคุณผ่านการกำหนดด้วยโปรแกรม คุณจะต้องได้รับชื่อบัญชีผู้ใช้บริการ (ผู้ใช้) ที่มีอยู่ภายในผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-200">To change your Azure AD app permissions programmatically, you'll need to get the existing service principals (users) within your tenant.</span></span> <span data-ttu-id="3eb25-201">สำหรับข้อมูลเกี่ยวกับวิธีการดังกล่าว ดู[servicePrincipal](/graph/api/resources/serviceprincipal)</span><span class="sxs-lookup"><span data-stu-id="3eb25-201">For information on how to do that, see [servicePrincipal](/graph/api/resources/serviceprincipal).</span></span>

1. <span data-ttu-id="3eb25-202">หากต้องการรับชื่อบัญชีผู้ใช้บริการทั้งหมดภายในผู้เช่าของคุณ ให้เรียกใช้ API `Get servicePrincipal` โดยไม่ต้องใช้ `{ID}`</span><span class="sxs-lookup"><span data-stu-id="3eb25-202">To get all the service principals within your tenant, call the `Get servicePrincipal` API without `{ID}`.</span></span>

2. <span data-ttu-id="3eb25-203">ตรวจสอบชื่อบัญชีผู้ใช้บริการโดยใช้ *ID แอปพลิเคชัน* ของแอปของคุณเป็นคุณสมบัติ `appId`</span><span class="sxs-lookup"><span data-stu-id="3eb25-203">Check for a service principal with your app's *application ID* as the `appId` property.</span></span>

    ```json
    Post https://graph.microsoft.com/v1.0/servicePrincipals HTTP/1.1
    Authorization: Bearer ey..qw
    Content-Type: application/json
    {
    "accountEnabled" : true,
    "appId" : "{App_Client_ID}",
    "displayName" : "{App_DisplayName}"
    }
    ```

    >[!NOTE]
    ><span data-ttu-id="3eb25-204">`displayName` เป็นแบบทางเลือก</span><span class="sxs-lookup"><span data-stu-id="3eb25-204">`displayName` is optional.</span></span>

3. <span data-ttu-id="3eb25-205">ให้สิทธิ์ Power BI แก่แอปของคุณโดยกำหนดค่าใดค่าหนึ่งเป็น `consentType`:</span><span class="sxs-lookup"><span data-stu-id="3eb25-205">Grant Power BI permissions to your app, by assigning one of these values to `consentType`:</span></span>

    * <span data-ttu-id="3eb25-206">`AllPrincipals` - สามารถใช้ได้โดยผู้ดูแลระบบ Power BI เท่านั้นเพื่อให้สิทธิ์ในนามของผู้ใช้ทั้งหมดในผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="3eb25-206">`AllPrincipals` - Can only be used by a Power BI admin to grant permissions on behalf of all the users in the tenant.</span></span>

    * <span data-ttu-id="3eb25-207">`Principal` - ใช้เพื่อให้สิทธิ์ในนามของผู้ใช้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3eb25-207">`Principal` - Use to grant permissions on behalf of a specific user.</span></span> <span data-ttu-id="3eb25-208">ถ้าคุณกำลังใช้ตัวเลือกนี้ ให้เพิ่มคุณสมบัติ `principalId={User_ObjectId}` ลงในเนื้อหาคำขอ</span><span class="sxs-lookup"><span data-stu-id="3eb25-208">If you're using this option, add the `principalId={User_ObjectId}` property to the request body.</span></span>

     ```json
     Post https://graph.microsoft.com/v1.0/OAuth2PermissionGrants HTTP/1.1
     Authorization: Bearer ey..qw
     Content-Type: application/json
     {
     "clientId":"{Service_Plan_ID}",
     "consentType":"AllPrincipals",
     "resourceId":"c78a3685-1ce7-52cd-95f7-dc5aea8ec98e",
     "scope":"Dataset.ReadWrite.All Dashboard.Read.All Report.Read.All Group.Read Group.Read.All Content.Create Metadata.View_Any Dataset.Read.All Data.Alter_Any",
     "expiryTime":"2018-03-29T14:35:32.4943409+03:00",
     "startTime":"2017-03-29T14:35:32.4933413+03:00"
     }
     ```

    >[!NOTE]
    >* <span data-ttu-id="3eb25-209">หากคุณใช้ **ผู้ใช้หลัก** เพื่อหลีกเลี่ยงไม่ให้ Azure AD พร้อมต์แจ้งขอรับคำยินยอม คุณจะต้องให้สิทธิ์แก่บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="3eb25-209">If you're using a **master user**, to avoid being prompted for consent by Azure AD, you need to grant permissions to the master account.</span></span>
    >* <span data-ttu-id="3eb25-210">`resourceId` *c78a3685-1ce7-52cd-95f7-dc5aea8ec98e* ขึ้นอยู่กับผู้เช่าและไม่เป็นสากล</span><span class="sxs-lookup"><span data-stu-id="3eb25-210">The `resourceId` *c78a3685-1ce7-52cd-95f7-dc5aea8ec98e* is tenant dependent and not universal.</span></span> <span data-ttu-id="3eb25-211">ค่านี้เป็น *objectId* ของแอปพลิเคชัน *Power BI Service* ใน Azure AD</span><span class="sxs-lookup"><span data-stu-id="3eb25-211">This value is the *objectId* of the *Power BI Service* application in Azure AD.</span></span> <span data-ttu-id="3eb25-212">หากต้องการรับค่านี้จากพอร์ทัล Azure ให้ไปที่ [Enterprise applications> All applications](https://portal.azure.com/#blade/Microsoft_AAD_IAM/StartboardApplicationsMenuBlade/AllApps) และค้นหา *Power BI Service*</span><span class="sxs-lookup"><span data-stu-id="3eb25-212">To get this value from the Azure portal, navigate to [Enterprise applications > All applications](https://portal.azure.com/#blade/Microsoft_AAD_IAM/StartboardApplicationsMenuBlade/AllApps), and search for *Power BI Service*.</span></span>

4. <span data-ttu-id="3eb25-213">ให้สิทธิ์แอปแก่ Azure AD โดยกำหนดค่าเป็น `consentType`</span><span class="sxs-lookup"><span data-stu-id="3eb25-213">Grant app permissions to Azure AD, by assigning a value to `consentType`.</span></span>

    ```json
    Post https://graph.microsoft.com/v1.0/OAuth2PermissionGrants HTTP/1.1
    Authorization: Bearer ey..qw
    Content-Type: application/json
    {
    "clientId":"{Service_Plan_ID}",
    "consentType":"AllPrincipals",
    "resourceId":"61e57743-d5cf-41ba-bd1a-2b381390a3f1",
    "scope":"User.Read Directory.AccessAsUser.All",
    "expiryTime":"2018-03-29T14:35:32.4943409+03:00",
    "startTime":"2017-03-29T14:35:32.4933413+03:00"
    }
    ```

# <a name="c"></a>[<span data-ttu-id="3eb25-214">C#</span><span class="sxs-lookup"><span data-stu-id="3eb25-214">C#</span></span>](#tab/CSharp)

<span data-ttu-id="3eb25-215">คุณยังสามารถเปลี่ยนสิทธิ์แอป Azure AD ของคุณโดยใช้ C#</span><span class="sxs-lookup"><span data-stu-id="3eb25-215">You can also change your Azure AD app permissions using C#.</span></span> <span data-ttu-id="3eb25-216">สำหรับข้อมูลเพิ่มเติม โปรดดู API สำหรับ [oAuth2PermissionGrant](/graph/api/oauth2permissiongrant-get)</span><span class="sxs-lookup"><span data-stu-id="3eb25-216">For more information see the [oAuth2PermissionGrant](/graph/api/oauth2permissiongrant-get) API.</span></span> <span data-ttu-id="3eb25-217">วิธีนี้มีประโยชน์หากคุณกำลังพิจารณาที่จะทำให้กระบวนการบางอย่างเป็นไปโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3eb25-217">This method can be useful if you're considering to automate some of your processes.</span></span>

<span data-ttu-id="3eb25-218">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำขอ HTTP โปรดดูที่[แท็บ HTTP](register-app.md?tabs=customers%2CHTTP#change-your-azure-ad-apps-permissions)</span><span class="sxs-lookup"><span data-stu-id="3eb25-218">For more information regarding the HTTP requests, refer to the [HTTP tab](register-app.md?tabs=customers%2CHTTP#change-your-azure-ad-apps-permissions).</span></span>

```csharp
var graphClient = GetGraphClient();

currentState.createdApp = await graphClient.Applications
    .Request()
    .AddAsync(application);

System.Threading.Thread.Sleep(2000);

var passwordCredential = new PasswordCredential
{
    DisplayName = "Client Secret Created in C#"
};

currentState.createdSecret = await graphClient.Applications[currentState.createdApp.Id]
    .AddPassword(passwordCredential)
    .Request()
    .PostAsync();

var servicePrincipal = new ServicePrincipal
{
    AppId = currentState.createdApp.AppId
};

currentState.createdServicePrincipal = await graphClient.ServicePrincipals
    .Request()
    .AddAsync(servicePrincipal);

GraphServiceClient graphClient = new GraphServiceClient(authProvider);

// Use oAuth2PermissionGrant to change permissions
var oAuth2PermissionGrant = await graphClient.Oauth2PermissionGrants["{id}"]
               .Request()
               .GetAsync();
```

---

## <a name="next-steps"></a><span data-ttu-id="3eb25-219">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3eb25-219">Next steps</span></span>

>[!div class="nextstepaction"]
>[<span data-ttu-id="3eb25-220">รับโทเค็นการเข้าถึง Azure AD สำหรับแอปพลิเคชัน Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3eb25-220">Get an Azure AD access token for your Power BI application</span></span>](get-azuread-access-token.md)

<span data-ttu-id="3eb25-221">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3eb25-221">More questions?</span></span> [<span data-ttu-id="3eb25-222">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="3eb25-222">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)