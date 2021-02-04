---
title: ทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตสำหรับลูกค้าของคุณเป็นแบบอัตโนมัติ
description: เรียนรู้เกี่ยวกับการทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตเป็นแบบอัตโนมัติ
author: paulinbar
ms.author: painbar
ms.topic: conceptual
ms.service: powerbi
ms.subservice: powerbi-developer
ms.date: 11/23/2020
ms.openlocfilehash: 0852fcb2c932680f6c20aeee94a89c68f473e46d
ms.sourcegitcommit: 1cad78595cca1175b82c04458803764ac36e5e37
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/19/2021
ms.locfileid: "98565731"
---
# <a name="automated-configuration-of-a-template-app-installation"></a><span data-ttu-id="13ce2-103">การกำหนดค่าของการติดตั้งแอปเทมเพลตแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="13ce2-103">Automated configuration of a template app installation</span></span>

<span data-ttu-id="13ce2-104">แอปเทมเพลตเป็นวิธีที่ยอดเยี่ยมสำหรับลูกค้าในการเริ่มรับข้อมูลเชิงลึกจากข้อมูลของตน</span><span class="sxs-lookup"><span data-stu-id="13ce2-104">Template apps are a great way for customers to start getting insights from their data.</span></span> <span data-ttu-id="13ce2-105">แอปเทมเพลตช่วยให้แอปเหล่านี้ทำงานได้อย่างรวดเร็วโดยการเชื่อมต่อกับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="13ce2-105">Template apps get them up and running quickly by connecting them to their data.</span></span> <span data-ttu-id="13ce2-106">แอปเทมเพลตจะให้รายงานที่สร้างไว้ล่วงหน้าแก่ลูกค้าซึ่งพวกเขาสามารถปรับแต่งได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="13ce2-106">The template apps provide them with prebuilt reports that they can customize if they so desire.</span></span>

<span data-ttu-id="13ce2-107">ลูกค้ามักไม่คุ้นเคยกับรายละเอียดของวิธีการเชื่อมต่อกับข้อมูลของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="13ce2-107">Customers aren't always familiar with the details of how to connect to their data.</span></span> <span data-ttu-id="13ce2-108">การให้รายละเอียดเหล่านี้ในขณะที่พวกเขาติดตั้งแอปเทมเพลต จะสร้างความยุ่งยากให้</span><span class="sxs-lookup"><span data-stu-id="13ce2-108">Having to provide these details when they install a template app can be a pain point for them.</span></span>

<span data-ttu-id="13ce2-109">หากคุณเป็นผู้ให้บริการข้อมูลและได้สร้างแอปเทมเพลตเพื่อช่วยให้ลูกค้าเริ่มต้นใช้งานข้อมูลในบริการของคุณ คุณสามารถทำให้พวกเขาติดตั้งแอปเทมเพลตของคุณได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="13ce2-109">If you are a data services provider and have created a template app to help your customers get started with their data on your service, you can make it easier for them to install your template app.</span></span> <span data-ttu-id="13ce2-110">คุณสามารถทำให้การกำหนดค่าพารามิเตอร์ของแอปเทมเพลตเป็นแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="13ce2-110">You can automate the configuration of your template app's parameters.</span></span> <span data-ttu-id="13ce2-111">เมื่อลูกค้าลงชื่อเข้าใช้พอร์ทัลของคุณ พวกเขาจะเลือกลิงก์พิเศษที่คุณเตรียมไว้</span><span class="sxs-lookup"><span data-stu-id="13ce2-111">When the customer signs in to your portal, they select a special link you've prepared.</span></span> <span data-ttu-id="13ce2-112">ลิงก์นี้:</span><span class="sxs-lookup"><span data-stu-id="13ce2-112">This link:</span></span>

- <span data-ttu-id="13ce2-113">เปิดการทำงานอัตโนมัติ ซึ่งรวบรวมข้อมูลที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="13ce2-113">Launches the automation, which gathers the information it needs.</span></span>
- <span data-ttu-id="13ce2-114">กำหนดค่าพารามิเตอร์แอปเทมเพลตไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="13ce2-114">Preconfigures the template app parameters.</span></span>
- <span data-ttu-id="13ce2-115">เปลี่ยนเส้นทางลูกค้าไปยังบัญชี Power BI ของพวกเขาซึ่งพวกเขาสามารถติดตั้งแอปได้</span><span class="sxs-lookup"><span data-stu-id="13ce2-115">Redirects the customer to their Power BI account where they can install the app.</span></span>

<span data-ttu-id="13ce2-116">สิ่งที่พวกเขาต้องทำคือเลือก **ติดตั้ง** และรับรองความถูกต้องเทียบกับแหล่งข้อมูลของพวกเขา เท่านี้ก็เรียบร้อย!</span><span class="sxs-lookup"><span data-stu-id="13ce2-116">All they have to do is select **Install** and authenticate against their data source, and they're good to go!</span></span>

<span data-ttu-id="13ce2-117">ประสบการณ์ของลูกค้านี้แสดงเป็นภาพประกอบไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="13ce2-117">The customer experience is illustrated here.</span></span>

![ภาพประกอบของประสบการณ์ผู้ใช้กับแอปพลิเคชันที่มีการติดตั้งอัตโนมัติ](media/template-apps-auto-install/high-level-flow.png)

<span data-ttu-id="13ce2-119">บทความนี้อธิบายถึงโฟลว์พื้นฐาน ข้อกำหนดเบื้องต้น และขั้นตอนหลักและ API ที่คุณต้องการเพื่อทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตเป็นแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="13ce2-119">This article describes the basic flow, the prerequisites, and the main steps and APIs you need to automate the configuration of a template app installation.</span></span> <span data-ttu-id="13ce2-120">หากคุณต้องการเพียงแค่เข้าไปและเริ่มต้นใช้งาน คุณสามารถข้ามไปที่[บทช่วยสอน](template-apps-auto-install-tutorial.md) ซึ่งคุณสามารถทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตเป็นแบบอัตโนมัติได้โดยใช้แอปพลิเคชันตัวอย่างง่าย ๆ ที่เราเตรียมไว้ซึ่งใช้ฟังก์ชัน Azure</span><span class="sxs-lookup"><span data-stu-id="13ce2-120">If you want to dive in and get started, you can skip to the [tutorial](template-apps-auto-install-tutorial.md) where you automate the configuration of the template app installation by using a simple sample application we've prepared that uses an Azure function.</span></span>

## <a name="basic-flow"></a><span data-ttu-id="13ce2-121">โฟลว์พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="13ce2-121">Basic flow</span></span>

<span data-ttu-id="13ce2-122">โฟลว์พื้นฐานของการทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตเป็นแบบอัตโนมัติเป็นดังนี้:</span><span class="sxs-lookup"><span data-stu-id="13ce2-122">The basic flow of automating the configuration of a template app installation is as follows:</span></span>

1. <span data-ttu-id="13ce2-123">ผู้ใช้ลงชื่อเข้าใช้พอร์ทัลของ ISV และเลือกลิงก์ที่ให้มา</span><span class="sxs-lookup"><span data-stu-id="13ce2-123">The user signs in to the ISV's portal and selects the supplied link.</span></span> <span data-ttu-id="13ce2-124">การดำเนินการนี้จะเริ่มใช้โฟลว์อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="13ce2-124">This action initiates the automated flow.</span></span> <span data-ttu-id="13ce2-125">พอร์ทัลของ ISV เตรียมการกำหนดค่าเฉพาะของผู้ใช้ในลำดับขั้นนี้</span><span class="sxs-lookup"><span data-stu-id="13ce2-125">The ISV's portal prepares the user-specific configuration at this stage.</span></span>

1. <span data-ttu-id="13ce2-126">ISV ได้รับโทเค็น *เฉพาะแอป* ตาม [องค์ประกอบหลักของบริการ (โทเค็นเฉพาะแอป)](../embedded/embed-service-principal.md) ที่ลงทะเบียนในผู้เช่าของ ISV</span><span class="sxs-lookup"><span data-stu-id="13ce2-126">The ISV acquires an *app-only* token based on a [service principal (app-only token)](../embedded/embed-service-principal.md) that's registered in the ISV's tenant.</span></span>

1. <span data-ttu-id="13ce2-127">ด้วยการใช้ [Power BI REST APIs](/rest/api/power-bi/) ISV จะสร้าง *ตั๋วการติดตั้ง* ซึ่งมีการกำหนดค่าพารามิเตอร์เฉพาะของผู้ใช้ตามที่ ISV เตรียมไว้</span><span class="sxs-lookup"><span data-stu-id="13ce2-127">Using [Power BI REST APIs](/rest/api/power-bi/), the ISV creates an *install ticket*, which contains the user-specific parameter configuration as prepared by the ISV.</span></span>

1. <span data-ttu-id="13ce2-128">ISV เปลี่ยนเส้นทางผู้ใช้ไปยัง Power BI โดยใช้วิธีการเปลี่ยนเส้นทาง ```POST``` ที่มีตั๋วการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="13ce2-128">The ISV redirects the user to Power BI by using a ```POST``` redirection method that contains the install ticket.</span></span>

1. <span data-ttu-id="13ce2-129">ผู้ใช้จะถูกเปลี่ยนเส้นทางไปยังบัญชี Power BI ของพวกเขาด้วยตั๋วการติดตั้งและได้รับพร้อมท์แจ้งให้ติดตั้งแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="13ce2-129">The user is redirected to their Power BI account with the install ticket and is prompted to install the template app.</span></span> <span data-ttu-id="13ce2-130">เมื่อผู้ใช้เลือก **ติดตั้ง** แอปเทมเพลตจะถูกติดตั้งสำหรับพวกเขา</span><span class="sxs-lookup"><span data-stu-id="13ce2-130">When the user selects **Install**, the template app is installed for them.</span></span>

>[!Note]
><span data-ttu-id="13ce2-131">แม้ว่าค่าพารามิเตอร์จะถูกกำหนดโดย ISV ในกระบวนการสร้างตั๋วการติดตั้ง แต่ข้อมูลประจำตัวที่เกี่ยวข้องกับแหล่งข้อมูลจะถูกจัดเตรียมโดยผู้ใช้ในขั้นตอนสุดท้ายของการติดตั้งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="13ce2-131">While parameter values are configured by the ISV in the process of creating the install ticket, data source-related credentials are only supplied by the user in the final stages of the installation.</span></span> <span data-ttu-id="13ce2-132">การดำเนินการนี้จะป้องกันไม่ให้มีการเปิดเผยข้อมูลประจำตัวกับบุคคลที่สาม และทำให้มั่นใจได้ว่าการเชื่อมต่อระหว่างผู้ใช้และแหล่งข้อมูลของแอปเทมเพลตมีความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="13ce2-132">This arrangement prevents them from being exposed to a third party and ensures a secure connection between the user and the template app data sources.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="13ce2-133">สิ่งที่จำเป็นต้องมี</span><span class="sxs-lookup"><span data-stu-id="13ce2-133">Prerequisites</span></span>

<span data-ttu-id="13ce2-134">หากต้องการให้ประสบการณ์การติดตั้งที่กำหนดไว้ล่วงหน้าสำหรับแอปแม่แบบ คุณจำเป็นต้องมีข้อกำหนดเบื้องต้นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="13ce2-134">To provide a preconfigured installation experience for your template app, the following prerequisites are required:</span></span>

* <span data-ttu-id="13ce2-135">สิทธิการใช้งาน Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="13ce2-135">A Power BI Pro license.</span></span> <span data-ttu-id="13ce2-136">หากคุณยังไม่ได้สมัคร Power BI Pro ให้ [สมัครทดลองใช้งานฟรี](https://powerbi.microsoft.com/pricing/) ก่อนที่คุณจะเริ่ม</span><span class="sxs-lookup"><span data-stu-id="13ce2-136">If you're not signed up for Power BI Pro, [sign up for a free trial](https://powerbi.microsoft.com/pricing/) before you begin.</span></span>
* <span data-ttu-id="13ce2-137">ตั้งค่าผู้เช่า Azure Active Directory (Azure AD) ของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="13ce2-137">Your own Azure Active Directory (Azure AD) tenant set up.</span></span> <span data-ttu-id="13ce2-138">สำหรับคำแนะนำเกี่ยวกับวิธีการตั้งค่า โปรดดูที่[สร้างผู้เช่า Azure AD](../embedded/create-an-azure-active-directory-tenant.md)</span><span class="sxs-lookup"><span data-stu-id="13ce2-138">For instructions on how to set one up, see [Create an Azure AD tenant](../embedded/create-an-azure-active-directory-tenant.md).</span></span>
* <span data-ttu-id="13ce2-139">**องค์ประกอบหลักของบริการ (โทเค็นเฉพาะแอป)** ที่ลงทะเบียนในผู้เช่าก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="13ce2-139">A **service principal (app-only token)** registered in the preceding tenant.</span></span> <span data-ttu-id="13ce2-140">สำหรับข้อมูลเพิ่มเติม โปรดดู[ฝังเนื้อหา Power BI ด้วยองค์ประกอบหลักของบริการและข้อมูลลับของแอปพลิเคชัน](../embedded/embed-service-principal.md)</span><span class="sxs-lookup"><span data-stu-id="13ce2-140">For more information, see [Embed Power BI content with service principal and an application secret](../embedded/embed-service-principal.md).</span></span> <span data-ttu-id="13ce2-141">ตรวจสอบให้แน่ใจว่าได้ลงทะเบียนแอปพลิเคชันเป็นแอปแบบ **เว็บแอปพลิเคชันฝั่งเซิร์ฟเวอร์**</span><span class="sxs-lookup"><span data-stu-id="13ce2-141">Make sure to register the application as a **server-side web application** app.</span></span> <span data-ttu-id="13ce2-142">คุณลงทะเบียนแอปพลิเคชันเว็บฝั่งเซิร์ฟเวอร์เพื่อสร้างเป็นความลับของแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="13ce2-142">You register a server-side web application to create an application secret.</span></span> <span data-ttu-id="13ce2-143">จากขั้นตอนนี้คุณต้องบันทึก *ID แอปพลิเคชัน* (ID ไคลเอ็นต์) และ *ข้อมูลลับของแอปพลิเคชัน* (ข้อมูลลับของไคลเอ็นต์) สำหรับขั้นตอนในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="13ce2-143">From this process, you need to save the *application ID* (ClientID) and *application secret* (ClientSecret) for later steps.</span></span>
* <span data-ttu-id="13ce2-144">**แอปเทมเพลต** แบบกำหนดพารามิเตอร์ที่พร้อมสำหรับการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="13ce2-144">A **parameterized template app** that's ready for installation.</span></span> <span data-ttu-id="13ce2-145">ต้องสร้างแอปเทมเพลตในผู้เช่าเดียวกันกับที่คุณลงทะเบียนแอปพลิเคชันของคุณใน Azure AD</span><span class="sxs-lookup"><span data-stu-id="13ce2-145">The template app must be created in the same tenant in which you register your application in Azure AD.</span></span> <span data-ttu-id="13ce2-146">สำหรับข้อมูลเพิ่มเติม โปรดดูที่[เคล็ดลับแอปเทมเพลต](../../connect-data/service-template-apps-tips.md)หรือ[สร้างแอปเทมเพลตใน Power BI](../../connect-data/service-template-apps-create.md)</span><span class="sxs-lookup"><span data-stu-id="13ce2-146">For more information, see [Template app tips](../../connect-data/service-template-apps-tips.md) or [Create a template app in Power BI](../../connect-data/service-template-apps-create.md).</span></span> <span data-ttu-id="13ce2-147">จากแอปเทมเพลต คุณต้องจดข้อมูลต่อไปนี้สำหรับขั้นตอนต่อไป:</span><span class="sxs-lookup"><span data-stu-id="13ce2-147">From the template app, you need to note the following information for the next steps:</span></span>
     * <span data-ttu-id="13ce2-148">*App ID*, *Package Key* และ *Owner ID* ตามที่ปรากฏใน URL การติดตั้งในตอนท้ายของกระบวนการ [กำหนดคุณสมบัติของแอปเทมเพลต](../../connect-data/service-template-apps-create.md#define-the-properties-of-the-template-app)เมื่อสร้างแอปขึ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="13ce2-148">*App ID*, *Package Key*, and *Owner ID* as they appear in the installation URL at the end of the process of [defining the properties of the template app](../../connect-data/service-template-apps-create.md#define-the-properties-of-the-template-app) when the app was created.</span></span> <span data-ttu-id="13ce2-149">คุณยังสามารถรับลิงก์เดียวกันได้โดยเลือกที่ **รับลิงก์** ในบานหน้าต่าง [การจัดการนำไปใช้งานจริง](../../connect-data/service-template-apps-create.md#manage-the-template-app-release)ของแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="13ce2-149">You can also get the same link by selecting **Get link** in the template app's [Release Management](../../connect-data/service-template-apps-create.md#manage-the-template-app-release) pane.</span></span>
    * <span data-ttu-id="13ce2-150">*ชื่อพารามิเตอร์* ตามที่กำหนดไว้ในชุดข้อมูลของแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="13ce2-150">*Parameter names* as they're defined in the template app's dataset.</span></span> <span data-ttu-id="13ce2-151">ชื่อพารามิเตอร์เป็นสตริงที่คำนึงถึงตัวพิมพ์เล็กและใหญ่ และยังสามารถดึงชื่อดังกล่าวได้จากแท็บ **การตั้งค่าพารามิเตอร์** เมื่อคุณ [กำหนดคุณสมบัติของแอปเทมเพลต](../../connect-data/service-template-apps-create.md#define-the-properties-of-the-template-app) หรือจากการตั้งค่าชุดข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="13ce2-151">Parameter names are case-sensitive strings and can also be retrieved from the **Parameter Settings** tab when you [define the properties of the template app](../../connect-data/service-template-apps-create.md#define-the-properties-of-the-template-app) or from the dataset settings in Power BI.</span></span>

    >[!NOTE]
    ><span data-ttu-id="13ce2-152">คุณสามารถทดสอบแอปพลิเคชันการติดตั้งที่กำหนดค่าไว้ล่วงหน้าบนแอปเทมเพลตของคุณได้หากแอปเทมเพลตพร้อมสำหรับการติดตั้งแม้ว่าจะยังไม่พร้อมใช้งานแบบสาธารณะใน AppSource ก็ตาม</span><span class="sxs-lookup"><span data-stu-id="13ce2-152">You can test your preconfigured installation application on your template app if the template app is ready for installation, even if it isn't publicly available on AppSource yet.</span></span> <span data-ttu-id="13ce2-153">เพื่อให้ผู้ใช้ภายนอกผู้เช่าของคุณสามารถใช้แอปพลิเคชันการติดตั้งอัตโนมัติเพื่อติดตั้งแอปเทมเพลตของคุณได้ แอปเทมเพลตจะต้องพร้อมใช้งานแบบสาธารณะใน [Power BI Apps marketplace](https://app.powerbi.com/getdata/services)</span><span class="sxs-lookup"><span data-stu-id="13ce2-153">For users outside your tenant to be able to use the automated installation application to install your template app, the template app must be publicly available in the [Power BI apps marketplace](https://app.powerbi.com/getdata/services).</span></span> <span data-ttu-id="13ce2-154">ก่อนที่คุณจะแจกจ่ายแอปเทมเพลตของคุณโดยใช้แอปพลิเคชันการติดตั้งอัตโนมัติที่คุณกำลังสร้างขึ้น อย่าลืมเผยแพร่ไปยัง[ศูนย์พันธมิตร](/azure/marketplace/partner-center-portal/create-power-bi-app-offer)ก่อน</span><span class="sxs-lookup"><span data-stu-id="13ce2-154">Before you distribute your template app by using the automated installation application you're creating, be sure to publish it to [Partner Center](/azure/marketplace/partner-center-portal/create-power-bi-app-offer).</span></span>

## <a name="main-steps-and-apis"></a><span data-ttu-id="13ce2-155">ขั้นตอนหลักและ Api</span><span class="sxs-lookup"><span data-stu-id="13ce2-155">Main steps and APIs</span></span>

<span data-ttu-id="13ce2-156">ขั้นตอนหลักสำหรับการทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตและ API ที่คุณต้องการเป็นแบบอัตโนมัติมีอธิบายไว้ในส่วนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="13ce2-156">The main steps for automating the configuration of a template app installation, and the APIs you'll need, are described in the following sections.</span></span> <span data-ttu-id="13ce2-157">แม้ว่าขั้นตอนส่วนใหญ่จะดำเนินการด้วย [Power BI REST APIs](/rest/api/power-bi/) แต่ตัวอย่างโค้ดที่อธิบายที่นี้ใช้ .NET SDK</span><span class="sxs-lookup"><span data-stu-id="13ce2-157">While most of the steps are done with [Power BI REST APIs](/rest/api/power-bi/), the code examples described here are made with the .NET SDK.</span></span>

## <a name="step-1-create-a-power-bi-client-object"></a><span data-ttu-id="13ce2-158">ขั้นตอนที่ 1: สร้างออบเจ็กต์ไคลเอนต์ Power BI</span><span class="sxs-lookup"><span data-stu-id="13ce2-158">Step 1: Create a Power BI client object</span></span>

<span data-ttu-id="13ce2-159">เมื่อคุณใช้งาน Power BI REST API คุณจำเป็นต้องได้รับ *โทเค็นการเข้าถึง* สำหรับ [องค์ประกอบหลักของบริการ](../embedded/embed-service-principal.md)ของคุณจาก Azure AD</span><span class="sxs-lookup"><span data-stu-id="13ce2-159">Using Power BI REST APIs requires you to get an *access token* for your [service principal](../embedded/embed-service-principal.md) from Azure AD.</span></span> <span data-ttu-id="13ce2-160">คุณต้องได้รับ[โทเค็นการเข้าถึง Azure AD](../embedded/get-azuread-access-token.md#access-token-for-non-power-bi-users-app-owns-data) สำหรับแอปพลิเคชัน Power BI ของคุณก่อนที่คุณจะเรียกใช้ [Power BI REST API](/rest/api/power-bi/)</span><span class="sxs-lookup"><span data-stu-id="13ce2-160">You're required to get an [Azure AD access token](../embedded/get-azuread-access-token.md#access-token-for-non-power-bi-users-app-owns-data) for your Power BI application before you make calls to the [Power BI REST APIs](/rest/api/power-bi/).</span></span>
<span data-ttu-id="13ce2-161">เมื่อต้องการสร้าง Power BI Client ด้วยโทเค็นการเข้าถึง คุณจำเป็นต้องสร้างออบเจ็กต์ไคลเอ็นต์ Power BI ซึ่งช่วยให้คุณสามารถโต้ตอบกับ [Power BI REST APIs](/rest/api/power-bi/) ได้</span><span class="sxs-lookup"><span data-stu-id="13ce2-161">To create the Power BI client with your access token, you need to create your Power BI client object, which allows you to interact with the [Power BI REST APIs](/rest/api/power-bi/).</span></span> <span data-ttu-id="13ce2-162">คุณสร้างวัตถุไคลเอ็นต์ Power BI ได้โดยการคลุม **AccessToken** ด้วยวัตถุ **Microsoft.Rest.TokenCredentials**</span><span class="sxs-lookup"><span data-stu-id="13ce2-162">You create the Power BI client object by wrapping the **AccessToken** with a **Microsoft.Rest.TokenCredentials** object.</span></span>

```csharp
using Microsoft.IdentityModel.Clients.ActiveDirectory;
using Microsoft.Rest;
using Microsoft.PowerBI.Api.V2;

var tokenCredentials = new TokenCredentials(authenticationResult.AccessToken, "Bearer");

// Create a Power BI client object. It's used to call Power BI APIs.
using (var client = new PowerBIClient(new Uri(ApiUrl), tokenCredentials))
{
    // Your code goes here.
}
```

## <a name="step-2-create-an-install-ticket"></a><span data-ttu-id="13ce2-163">ขั้นตอนที่ 2: สร้างตั๋วการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="13ce2-163">Step 2: Create an install ticket</span></span>

<span data-ttu-id="13ce2-164">สร้างตั๋วการติดตั้งซึ่งใช้เมื่อคุณเปลี่ยนเส้นทางผู้ใช้ของคุณไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="13ce2-164">Create an install ticket, which is used when you redirect your users to Power BI.</span></span> <span data-ttu-id="13ce2-165">API ที่ใช้สำหรับการดำเนินการนี้คือ **CreateInstallTicket** API</span><span class="sxs-lookup"><span data-stu-id="13ce2-165">The API used for this operation is the **CreateInstallTicket** API.</span></span>
* [<span data-ttu-id="13ce2-166">แอปเทมเพลต CreateInstallTicket</span><span class="sxs-lookup"><span data-stu-id="13ce2-166">Template Apps CreateInstallTicket</span></span>](/rest/api/power-bi/templateapps/createinstallticket)

<span data-ttu-id="13ce2-167">ตัวอย่างวิธีการสร้างตั๋วการติดตั้งสำหรับการติดตั้งและการกำหนดค่าแอปเทมเพลตสามารถดูได้จากไฟล์ [InstallTemplateApp / InstallAppFunction.cs](https://github.com/microsoft/Template-apps-examples/blob/master/Developer%20Samples/Automated%20Install%20Azure%20Function/InstallTemplateAppSample/InstallTemplateApp/InstallAppFunction.cs) ใน [แอปพลิเคชันตัวอย่าง](https://github.com/microsoft/Template-apps-examples/tree/master/Developer%20Samples/Automated%20Install%20Azure%20Function/InstallTemplateAppSample)</span><span class="sxs-lookup"><span data-stu-id="13ce2-167">A sample of how to create an install ticket for template app installation and configuration is available from the [InstallTemplateApp/InstallAppFunction.cs](https://github.com/microsoft/Template-apps-examples/blob/master/Developer%20Samples/Automated%20Install%20Azure%20Function/InstallTemplateAppSample/InstallTemplateApp/InstallAppFunction.cs) file in the [sample application](https://github.com/microsoft/Template-apps-examples/tree/master/Developer%20Samples/Automated%20Install%20Azure%20Function/InstallTemplateAppSample).</span></span>


<span data-ttu-id="13ce2-168">ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการใช้ **CreateInstallTicket** REST API ของแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="13ce2-168">The following code example shows how to use the template app **CreateInstallTicket** REST API.</span></span>
```csharp
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

// Create Install Ticket Request.
InstallTicket ticketResponse = null;
var request = new CreateInstallTicketRequest()
{
    InstallDetails = new List<TemplateAppInstallDetails>()
    {
        new TemplateAppInstallDetails()
        {
            AppId = Guid.Parse(AppId),
            PackageKey = PackageKey,
            OwnerTenantId = Guid.Parse(OwnerId),
            Config = new TemplateAppConfigurationRequest()
            {
                Configuration = Parameters
                                    .GroupBy(p => p.Name)
                                    .ToDictionary(k => k.Key, k => k.Select(p => p.Value).Single())
            }
        }
    }
};

// Issue the request to the REST API using .NET SDK.
InstallTicket ticketResponse = await client.TemplateApps.CreateInstallTicketAsync(request);
```

## <a name="step-3-redirect-users-to-power-bi-with-the-ticket"></a><span data-ttu-id="13ce2-169">ขั้นตอนที่ 3: เปลี่ยนเส้นทางผู้ใช้ไปยัง Power BI ด้วยตั๋ว</span><span class="sxs-lookup"><span data-stu-id="13ce2-169">Step 3: Redirect users to Power BI with the ticket</span></span>

<span data-ttu-id="13ce2-170">หลังจากคุณสร้างตั๋วการติดตั้งแล้ว คุณจะใช้ตั๋วดังกล่าวเพื่อเปลี่ยนเส้นทางผู้ใช้ของคุณไปยัง Power BI เพื่อดำเนินการติดตั้งและการกำหนดค่าแอปเทมเพลตต่อไป</span><span class="sxs-lookup"><span data-stu-id="13ce2-170">After you've created an install ticket, you use it to redirect your users to Power BI to continue with the template app installation and configuration.</span></span> <span data-ttu-id="13ce2-171">คุณใช้วิธีการเปลี่ยนเส้นทาง ```POST``` ไปยัง URL การติดตั้งของแอปเทมเพลต ด้วยตั๋วการติดตั้งในเนื้อความของคำขอ</span><span class="sxs-lookup"><span data-stu-id="13ce2-171">You use a ```POST``` method redirection to the template app's installation URL, with the install ticket in its request body.</span></span>

<span data-ttu-id="13ce2-172">มีวิธีการเปลี่ยนเส้นทางโดยใช้คำขอ ```POST``` ที่จัดทำเป็นเอกสารมากมาย</span><span class="sxs-lookup"><span data-stu-id="13ce2-172">There are various documented methods of how to issue a redirection by using ```POST``` requests.</span></span> <span data-ttu-id="13ce2-173">การเลือกอย่างใดอย่างหนึ่งขึ้นอยู่กับสถานการณ์และวิธีการที่ผู้ใช้ของคุณโต้ตอบกับพอร์ทัลหรือบริการของคุณ</span><span class="sxs-lookup"><span data-stu-id="13ce2-173">Choosing one or another depends on the scenario and how your users interact with your portal or service.</span></span>

<span data-ttu-id="13ce2-174">ตัวอย่างแบบง่ายนี้ ที่ส่วนใหญ่ใช้เพื่อวัตถุประสงค์ในการทดสอบ ใช้ฟอร์มที่มีเขตข้อมูลที่ซ่อนอยู่ซึ่งจะส่งตัวเองโดยอัตโนมัติเมื่อโหลด</span><span class="sxs-lookup"><span data-stu-id="13ce2-174">A simple example, mostly used for testing purposes, uses a form with a hidden field, which automatically submits itself upon loading.</span></span>

```javascript
<html>
    <body onload='document.forms["form"].submit()'>
        <!-- form method is POST and action is the app install URL -->
        <form name='form' action='https://app.powerbi.com/....' method='post' enctype='application/json'>
            <!-- value should be the new install ticket -->
            <input type='hidden' name='ticket' value='H4sI....AAA='>
        </form>
    </body>
</html>
```

<span data-ttu-id="13ce2-175">ตัวอย่างต่อไปนี้ของการตอบสนองของ[แอปพลิเคชันตัวอย่าง](https://github.com/microsoft/Template-apps-examples/tree/master/Developer%20Samples/Automated%20Install%20Azure%20Function/InstallTemplateAppSample)เก็บตั๋วการติดตั้งและเปลี่ยนเส้นทางผู้ใช้ไปยัง Power BI โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="13ce2-175">The following example of the [sample application](https://github.com/microsoft/Template-apps-examples/tree/master/Developer%20Samples/Automated%20Install%20Azure%20Function/InstallTemplateAppSample)'s response holds the install ticket and automatically redirects users to Power BI.</span></span> <span data-ttu-id="13ce2-176">การตอบสนองสำหรับฟังก์ชัน Azure นี้เป็นแบบฟอร์มการส่งด้วยตนเองโดยอัตโนมัติแบบเดียวกับที่เราเห็นในตัวอย่าง HTML ก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="13ce2-176">The response for this Azure function is the same automatically self-submitting form that we see in the preceding HTML example.</span></span>

```csharp
...
    return new ContentResult() { Content = RedirectWithData(redirectUrl, ticket.Ticket), ContentType = "text/html" };
}

...

public static string RedirectWithData(string url, string ticket)
{
    StringBuilder s = new StringBuilder();
    s.Append("<html>");
    s.AppendFormat("<body onload='document.forms[\"form\"].submit()'>");
    s.AppendFormat("<form name='form' action='{0}' method='post' enctype='application/json'>", url);
    s.AppendFormat("<input type='hidden' name='ticket' value='{0}' />", ticket);
    s.Append("</form></body></html>");
    return s.ToString();
}
```

>[!Note]
><span data-ttu-id="13ce2-177">แม้ว่าจะมีวิธีการหลากหลายในการใช้เบราว์เซอร์ ```POST``` เปลี่ยนเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="13ce2-177">There are various methods of using ```POST``` browser redirects.</span></span> <span data-ttu-id="13ce2-178">แต่คุณควรใช้วิธีที่ปลอดภัยที่สุดเสมอซึ่งขึ้นอยู่กับความต้องการและข้อจำกัดของบริการของคุณ</span><span class="sxs-lookup"><span data-stu-id="13ce2-178">You should always use the most secure method, which depends on your service needs and restrictions.</span></span> <span data-ttu-id="13ce2-179">โปรดจำไว้ว่ารูปแบบการเปลี่ยนเส้นทางที่ไม่ปลอดภัยบางรูปแบบอาจส่งผลให้ผู้ใช้หรือบริการของคุณพบปัญหาด้านความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="13ce2-179">Remember that some forms of insecure redirection can result in exposing your users or service to security issues.</span></span>

## <a name="step-4-move-your-automation-to-production"></a><span data-ttu-id="13ce2-180">ขั้นตอนที่ 4: ย้ายการทำงานโดยอัตโนมัติของคุณไปยังการผลิต</span><span class="sxs-lookup"><span data-stu-id="13ce2-180">Step 4: Move your automation to production</span></span>

<span data-ttu-id="13ce2-181">เมื่อการทำงานโดยอัตโนมัติที่คุณออกแบบไว้พร้อมแล้ว อย่าลืมย้ายไปยังการผลิต</span><span class="sxs-lookup"><span data-stu-id="13ce2-181">When the automation you've designed is ready, be sure to move it to production.</span></span>

## <a name="next-steps"></a><span data-ttu-id="13ce2-182">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="13ce2-182">Next steps</span></span>

* <span data-ttu-id="13ce2-183">ลองดู[บทช่วยสอน](template-apps-auto-install-tutorial.md)ของเราซึ่งใช้ฟังก์ชัน Azure อย่างง่ายเพื่อทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตเป็นแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="13ce2-183">Try our [tutorial](template-apps-auto-install-tutorial.md), which uses a simple Azure function to automate the configuration of a template app installation.</span></span>
* <span data-ttu-id="13ce2-184">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="13ce2-184">More questions?</span></span> <span data-ttu-id="13ce2-185">[ลองถามชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="13ce2-185">[Try asking the Power BI Community](https://community.powerbi.com/).</span></span>