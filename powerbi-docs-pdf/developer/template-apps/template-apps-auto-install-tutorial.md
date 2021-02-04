---
title: ทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตเป็นแบบอัตโนมัติโดยใช้ Azure Function
description: ใช้แอปพลิเคชันตัวอย่างเพื่อเรียนรู้วิธีการติดตั้งและกำหนดค่าแอปเทมเพลตสำหรับลูกค้าของคุณ
author: paulinbar
ms.author: painbar
ms.topic: tutorial
ms.service: powerbi
ms.subservice: powerbi-developer
ms.date: 11/23/2020
ms.openlocfilehash: a44bd7837e7605fd23e49a91e3e9eba106d5a933
ms.sourcegitcommit: 1cad78595cca1175b82c04458803764ac36e5e37
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/19/2021
ms.locfileid: "98565777"
---
# <a name="tutorial-automate-configuration-of-template-app-installation-using-an-azure-function"></a><span data-ttu-id="3dabe-103">บทช่วยสอน: ทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตเป็นแบบอัตโนมัติโดยใช้ Azure Function</span><span class="sxs-lookup"><span data-stu-id="3dabe-103">Tutorial: Automate configuration of template app installation using an Azure function</span></span>

<span data-ttu-id="3dabe-104">แอปเทมเพลตเป็นวิธีที่ยอดเยี่ยมสำหรับลูกค้าในการเริ่มรับข้อมูลเชิงลึกจากข้อมูลของตน</span><span class="sxs-lookup"><span data-stu-id="3dabe-104">Template apps are a great way for customers to start getting insights from their data.</span></span> <span data-ttu-id="3dabe-105">แอปเทมเพลตช่วยให้แอปเหล่านี้ทำงานได้อย่างรวดเร็วโดยการเชื่อมต่อกับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3dabe-105">Template apps get them up and running quickly by connecting them to their data.</span></span> <span data-ttu-id="3dabe-106">แอปเทมเพลตจะให้รายงานที่สร้างไว้ล่วงหน้าแก่ลูกค้าซึ่งพวกเขาสามารถปรับแต่งได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="3dabe-106">The template apps provide customers with prebuilt reports that they can customize if they so desire.</span></span>

<span data-ttu-id="3dabe-107">ลูกค้ามักไม่คุ้นเคยกับรายละเอียดของวิธีการเชื่อมต่อกับข้อมูลของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="3dabe-107">Customers aren't always familiar with the details of how to connect to their data.</span></span> <span data-ttu-id="3dabe-108">การให้รายละเอียดเหล่านี้ในขณะที่พวกเขาติดตั้งแอปเทมเพลต จะสร้างความยุ่งยากให้</span><span class="sxs-lookup"><span data-stu-id="3dabe-108">Having to provide these details when they install a template app can be a pain point for them.</span></span>

<span data-ttu-id="3dabe-109">หากคุณเป็นผู้ให้บริการข้อมูลและได้สร้างแอปเทมเพลตเพื่อช่วยให้ลูกค้าเริ่มต้นใช้งานข้อมูลในบริการของคุณ คุณสามารถทำให้พวกเขาติดตั้งแอปเทมเพลตของคุณได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="3dabe-109">If you are a data services provider and have created a template app to help your customers get started with their data on your service, you can make it easier for them to install your template app.</span></span> <span data-ttu-id="3dabe-110">คุณสามารถทำให้การกำหนดค่าพารามิเตอร์ของแอปเทมเพลตเป็นแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3dabe-110">You can automate the configuration of your template app's parameters.</span></span>

<span data-ttu-id="3dabe-111">เมื่อลูกค้าลงชื่อเข้าใช้พอร์ทัลของคุณ พวกเขาจะเลือกลิงก์พิเศษที่คุณเตรียมไว้</span><span class="sxs-lookup"><span data-stu-id="3dabe-111">When the customer signs in to your portal, they select a special link you've prepared.</span></span> <span data-ttu-id="3dabe-112">ลิงก์นี้:</span><span class="sxs-lookup"><span data-stu-id="3dabe-112">This link:</span></span>

- <span data-ttu-id="3dabe-113">เปิดการทำงานอัตโนมัติ ซึ่งรวบรวมข้อมูลที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="3dabe-113">Launches the automation, which gathers the information it needs.</span></span>
- <span data-ttu-id="3dabe-114">กำหนดค่าพารามิเตอร์แอปเทมเพลตไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="3dabe-114">Preconfigures the template app parameters.</span></span>
- <span data-ttu-id="3dabe-115">เปลี่ยนเส้นทางลูกค้าไปยังบัญชี Power BI ของพวกเขาซึ่งพวกเขาสามารถติดตั้งแอปได้</span><span class="sxs-lookup"><span data-stu-id="3dabe-115">Redirects the customer to their Power BI account where they can install the app.</span></span>

<span data-ttu-id="3dabe-116">สิ่งที่พวกเขาต้องทำคือเลือก **ติดตั้ง** และรับรองความถูกต้องเทียบกับแหล่งข้อมูลของพวกเขา เท่านี้ก็เรียบร้อย!</span><span class="sxs-lookup"><span data-stu-id="3dabe-116">All they have to do is select **Install** and authenticate against their data source, and they're good to go!</span></span>

<span data-ttu-id="3dabe-117">ประสบการณ์ของลูกค้านี้แสดงเป็นภาพประกอบไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="3dabe-117">The customer experience is illustrated here.</span></span>

![ภาพประกอบของประสบการณ์ผู้ใช้กับแอปพลิเคชันที่มีการติดตั้งอัตโนมัติ](media/template-apps-auto-install/high-level-flow.png)

<span data-ttu-id="3dabe-119">ในบทช่วยสอนนี้ คุณจะใช้ตัวอย่าง Azure Function สำหรับการติดตั้งอัตโนมัติที่เราสร้างขึ้นเพื่อกำหนดค่าล่วงหน้าและติดตั้งแอปเทมเพลตของคุณ</span><span class="sxs-lookup"><span data-stu-id="3dabe-119">In this tutorial, you'll use an automated installation Azure Functions sample that we've created to preconfigure and install your template app.</span></span> <span data-ttu-id="3dabe-120">ตัวอย่างนี้ถูกเก็บไว้อย่างตั้งใจเพื่อวัตถุประสงค์ในการสาธิต</span><span class="sxs-lookup"><span data-stu-id="3dabe-120">This sample has deliberately been kept simple for demonstration purposes.</span></span> <span data-ttu-id="3dabe-121">ซึ่งย่อส่วนการตั้งค่าของ Azure Function เพื่อใช้ Power BI API สำหรับการติดตั้งแอปเทมเพลตและกำหนดค่าให้กับผู้ใช้ของคุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3dabe-121">It encapsulates the setup of an Azure function to use Power BI APIs for installing a template app and configuring it for your users automatically.</span></span>

<span data-ttu-id="3dabe-122">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโฟลว์การทำงานโดยอัตโนมัติแบบทั่วไปและ API ที่แอปใช้ โปรดดู[ทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตเป็นแบบอัตโนมัติ](template-apps-auto-install.md)</span><span class="sxs-lookup"><span data-stu-id="3dabe-122">For more information about the general automation flow and the APIs that the app uses, see [Automate configuration of a template app installation](template-apps-auto-install.md).</span></span>

<span data-ttu-id="3dabe-123">แอปพลิเคชันแบบง่ายของเราใช้ Azure Function</span><span class="sxs-lookup"><span data-stu-id="3dabe-123">Our simple application uses an Azure function.</span></span> <span data-ttu-id="3dabe-124">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Azure Function โปรดดูที่[เอกสารเกี่ยวกับ Azure Function](/azure/azure-functions/)</span><span class="sxs-lookup"><span data-stu-id="3dabe-124">For more information about Azure Functions, see the [Azure Functions documentation](/azure/azure-functions/).</span></span>

## <a name="basic-flow"></a><span data-ttu-id="3dabe-125">โฟลว์พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="3dabe-125">Basic flow</span></span>

<span data-ttu-id="3dabe-126">ขั้นตอนพื้นฐานต่อไปนี้แสดงสิ่งที่แอปพลิเคชันทำเมื่อลูกค้าเปิดใช้งานโดยการเลือกที่ลิงก์บนพอร์ทัลของคุณ</span><span class="sxs-lookup"><span data-stu-id="3dabe-126">The following basic flow lists what the application does when the customer launches it by selecting the link in your portal.</span></span>

1. <span data-ttu-id="3dabe-127">ผู้ใช้ลงชื่อเข้าใช้พอร์ทัลของ ISV และเลือกลิงก์ที่ให้มา</span><span class="sxs-lookup"><span data-stu-id="3dabe-127">The user signs in to the ISV's portal and selects the supplied link.</span></span> <span data-ttu-id="3dabe-128">การดำเนินการนี้จะเริ่มใช้โฟลว์</span><span class="sxs-lookup"><span data-stu-id="3dabe-128">This action initiates the flow.</span></span> <span data-ttu-id="3dabe-129">พอร์ทัลของ ISV เตรียมการกำหนดค่าเฉพาะของผู้ใช้ในลำดับขั้นนี้</span><span class="sxs-lookup"><span data-stu-id="3dabe-129">The ISV's portal prepares the user-specific configuration at this stage.</span></span>

1. <span data-ttu-id="3dabe-130">ISV ได้รับโทเค็น *เฉพาะแอป* ตาม [องค์ประกอบหลักของบริการ (โทเค็นเฉพาะแอป)](../embedded/embed-service-principal.md) ที่ลงทะเบียนในผู้เช่าของ ISV</span><span class="sxs-lookup"><span data-stu-id="3dabe-130">The ISV acquires an *app-only* token based on a [service principal (app-only token)](../embedded/embed-service-principal.md) that's registered in the ISV's tenant.</span></span>

1. <span data-ttu-id="3dabe-131">ด้วยการใช้ [Power BI REST APIs](/rest/api/power-bi/) ISV จะสร้าง *ตั๋วการติดตั้ง* ซึ่งมีการกำหนดค่าพารามิเตอร์เฉพาะของผู้ใช้ตามที่ ISV เตรียมไว้</span><span class="sxs-lookup"><span data-stu-id="3dabe-131">Using [Power BI REST APIs](/rest/api/power-bi/), the ISV creates an *install ticket*, which contains the user-specific parameter configuration as prepared by the ISV.</span></span>

1. <span data-ttu-id="3dabe-132">ISV เปลี่ยนเส้นทางผู้ใช้ไปยัง Power BI โดยใช้วิธีการเปลี่ยนเส้นทาง ```POST``` ที่มีตั๋วการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="3dabe-132">The ISV redirects the user to Power BI by using a ```POST``` redirection method, which contains the install ticket.</span></span>

1. <span data-ttu-id="3dabe-133">ผู้ใช้จะถูกเปลี่ยนเส้นทางไปยังบัญชี Power BI ของพวกเขาด้วยตั๋วการติดตั้งและได้รับพร้อมท์แจ้งให้ติดตั้งแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="3dabe-133">The user is redirected to their Power BI account with the install ticket and is prompted to install the template app.</span></span> <span data-ttu-id="3dabe-134">เมื่อผู้ใช้เลือก **ติดตั้ง** แอปเทมเพลตจะถูกติดตั้งสำหรับพวกเขา</span><span class="sxs-lookup"><span data-stu-id="3dabe-134">When the user selects **Install**, the template app is installed for them.</span></span>

>[!Note]
><span data-ttu-id="3dabe-135">แม้ว่าค่าพารามิเตอร์จะถูกกำหนดโดย ISV ในกระบวนการสร้างตั๋วการติดตั้ง แต่ข้อมูลประจำตัวที่เกี่ยวข้องกับแหล่งข้อมูลจะถูกจัดเตรียมโดยผู้ใช้ในขั้นตอนสุดท้ายของการติดตั้งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3dabe-135">While parameter values are configured by the ISV in the process of creating the install ticket, data source-related credentials are only supplied by the user in the final stages of the installation.</span></span> <span data-ttu-id="3dabe-136">การดำเนินการนี้จะป้องกันไม่ให้มีการเปิดเผยข้อมูลประจำตัวกับบุคคลที่สาม และทำให้มั่นใจได้ว่าการเชื่อมต่อระหว่างผู้ใช้และแหล่งข้อมูลของแอปเทมเพลตมีความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="3dabe-136">This arrangement prevents them from being exposed to a third party and ensures a secure connection between the user and the template app data sources.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3dabe-137">สิ่งที่จำเป็นต้องมี</span><span class="sxs-lookup"><span data-stu-id="3dabe-137">Prerequisites</span></span>

* <span data-ttu-id="3dabe-138">ตั้งค่าผู้เช่า Azure Active Directory (Azure AD) ของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="3dabe-138">Your own Azure Active Directory (Azure AD) tenant set up.</span></span> <span data-ttu-id="3dabe-139">สำหรับคำแนะนำเกี่ยวกับวิธีการตั้งค่า โปรดดูที่[สร้างผู้เช่า Azure AD](../embedded/create-an-azure-active-directory-tenant.md)</span><span class="sxs-lookup"><span data-stu-id="3dabe-139">For instructions on how to set one up, see [Create an Azure AD tenant](../embedded/create-an-azure-active-directory-tenant.md).</span></span>
* <span data-ttu-id="3dabe-140">[องค์ประกอบหลักของบริการ (โทเค็นเฉพาะแอป)](../embedded/embed-service-principal.md) ที่ลงทะเบียนในผู้เช่าก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="3dabe-140">A [service principal (app-only token)](../embedded/embed-service-principal.md) registered in the preceding tenant.</span></span>
* <span data-ttu-id="3dabe-141">[แอปเทมเพลต](../../connect-data/service-template-apps-overview.md)แบบกำหนดพารามิเตอร์ที่พร้อมสำหรับการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="3dabe-141">A parameterized [template app](../../connect-data/service-template-apps-overview.md) that's ready for installation.</span></span> <span data-ttu-id="3dabe-142">ต้องสร้างแอปเทมเพลตในผู้เช่าเดียวกันกับที่คุณลงทะเบียนแอปพลิเคชันของคุณใน Azure AD</span><span class="sxs-lookup"><span data-stu-id="3dabe-142">The template app must be created in the same tenant in which you register your application in Azure AD.</span></span> <span data-ttu-id="3dabe-143">สำหรับข้อมูลเพิ่มเติม โปรดดูที่[เคล็ดลับแอปเทมเพลต](../../connect-data/service-template-apps-tips.md)หรือ[สร้างแอปเทมเพลตใน Power BI](../../connect-data/service-template-apps-create.md)</span><span class="sxs-lookup"><span data-stu-id="3dabe-143">For more information, see [Template app tips](../../connect-data/service-template-apps-tips.md) or [Create a template app in Power BI](../../connect-data/service-template-apps-create.md).</span></span>
* <span data-ttu-id="3dabe-144">สิทธิการใช้งาน Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="3dabe-144">A Power BI Pro license.</span></span> <span data-ttu-id="3dabe-145">หากคุณยังไม่ได้สมัคร Power BI Pro ให้ [สมัครทดลองใช้งานฟรี](https://powerbi.microsoft.com/pricing/) ก่อนที่คุณจะเริ่ม</span><span class="sxs-lookup"><span data-stu-id="3dabe-145">If you're not signed up for Power BI Pro, [sign up for a free trial](https://powerbi.microsoft.com/pricing/) before you begin.</span></span>

## <a name="set-up-your-template-apps-automation-development-environment"></a><span data-ttu-id="3dabe-146">ตั้งค่าสภาพแวดล้อมการพัฒนาเพื่อทำให้แอปเทมเพลตของคุณเป็นแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3dabe-146">Set up your template apps automation development environment</span></span>

<span data-ttu-id="3dabe-147">ก่อนที่คุณจะดำเนินการตั้งค่าแอปพลิเคชันของคุณต่อไป ให้ทำตามคำแนะนำใน [เริ่มต้นใช้งานด่วน: สร้างแอป Azure Functions ด้วย Azure App Configuration](/azure/azure-app-configuration/quickstart-azure-functions-csharp) เพื่อพัฒนาฟังก์ชัน Azure พร้อมกับการกำหนดค่าแอป Azure</span><span class="sxs-lookup"><span data-stu-id="3dabe-147">Before you continue setting up your application, follow the instructions in [Quickstart: Create an Azure Functions app with Azure App Configuration](/azure/azure-app-configuration/quickstart-azure-functions-csharp) to develop an Azure function along with an Azure app configuration.</span></span> <span data-ttu-id="3dabe-148">สร้างการกำหนดค่าแอปของคุณตามที่อธิบายไว้ในบทความ</span><span class="sxs-lookup"><span data-stu-id="3dabe-148">Create your app configuration as described in the article.</span></span>

### <a name="register-an-application-in-azure-ad"></a><span data-ttu-id="3dabe-149">ลงทะเบียนแอปพลิเคชันใน Azure AD</span><span class="sxs-lookup"><span data-stu-id="3dabe-149">Register an application in Azure AD</span></span>

<span data-ttu-id="3dabe-150">สร้างองค์ประกอบหลักของบริการตามที่อธิบายไว้ใน[ฝังเนื้อหา Power BI ด้วยองค์ประกอบหลักของบริการและข้อมูลลับของแอปพลิเคชัน](../embedded/embed-service-principal.md)</span><span class="sxs-lookup"><span data-stu-id="3dabe-150">Create a service principal as described in [Embed Power BI content with service principal and an application secret](../embedded/embed-service-principal.md).</span></span>

<span data-ttu-id="3dabe-151">ตรวจสอบให้แน่ใจว่าได้ลงทะเบียนแอปพลิเคชันเป็นแอปแบบ **เว็บแอปพลิเคชันฝั่งเซิร์ฟเวอร์**</span><span class="sxs-lookup"><span data-stu-id="3dabe-151">Make sure to register the application as a **server-side web application** app.</span></span> <span data-ttu-id="3dabe-152">คุณลงทะเบียนแอปพลิเคชันเว็บฝั่งเซิร์ฟเวอร์เพื่อสร้างเป็นความลับของแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="3dabe-152">You register a server-side web application to create an application secret.</span></span>

<span data-ttu-id="3dabe-153">บันทึก *ID แอปพลิเคชัน* (ID ไคลเอ็นต์) และ *ข้อมูลลับของแอปพลิเคชัน* (ข้อมูลลับของไคลเอ็นต์) สำหรับขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="3dabe-153">Save the *application ID* (ClientID) and *application secret* (ClientSecret) for later steps.</span></span>

<span data-ttu-id="3dabe-154">คุณสามารถเข้าถึง[เครื่องมือตั้งค่าการฝังตัว](https://aka.ms/embedsetup/AppOwnsData)เพื่อเริ่มต้นสร้างการลงทะเบียนแอปได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="3dabe-154">You can go through the [Embedding setup tool](https://aka.ms/embedsetup/AppOwnsData) to quickly get started creating an app registration.</span></span> <span data-ttu-id="3dabe-155">หากคุณกำลังใช้ [เครื่องมือการลงทะเบียนแอป Power BI](https://app.powerbi.com/embedsetup) ให้เลือกตัวเลือก **ฝังตัวสำหรับลูกค้าของคุณ**</span><span class="sxs-lookup"><span data-stu-id="3dabe-155">If you're using the [Power BI App Registration Tool](https://app.powerbi.com/embedsetup), select the **Embed for your customers** option.</span></span>

## <a name="template-app-preparation"></a><span data-ttu-id="3dabe-156">การเตรียมแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="3dabe-156">Template app preparation</span></span>

<span data-ttu-id="3dabe-157">หลังจากคุณได้สร้างแอปเทมเพลตของคุณและพร้อมสำหรับการติดตั้งแล้ว ให้บันทึกข้อมูลต่อไปนี้สำหรับขั้นตอนต่อไป:</span><span class="sxs-lookup"><span data-stu-id="3dabe-157">After you've created your template app and it's ready for installation, save the following information for the next steps:</span></span>

* <span data-ttu-id="3dabe-158">*App ID*, *Package Key* และ *Owner ID* ตามที่ปรากฏใน URL การติดตั้งในตอนท้ายของกระบวนการ [กำหนดคุณสมบัติของแอปเทมเพลต](../../connect-data/service-template-apps-create.md#define-the-properties-of-the-template-app)เมื่อสร้างแอปขึ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="3dabe-158">*App ID*, *Package Key*, and *Owner ID* as they appear in the installation URL at the end of the [Define the properties of the template app](../../connect-data/service-template-apps-create.md#define-the-properties-of-the-template-app) process when the app was created.</span></span>

    <span data-ttu-id="3dabe-159">คุณยังสามารถรับลิงก์เดียวกันได้โดยเลือกที่ **รับลิงก์** ใน [บานหน้าต่างการจัดการนำไปใช้งานจริง](../../connect-data/service-template-apps-create.md#manage-the-template-app-release)ของแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="3dabe-159">You can also get the same link by selecting **Get link** in the template app's [Release Management pane](../../connect-data/service-template-apps-create.md#manage-the-template-app-release).</span></span>

* <span data-ttu-id="3dabe-160">*ชื่อพารามิเตอร์* ตามที่กำหนดไว้ในชุดข้อมูลของแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="3dabe-160">*Parameter names* as they're defined in the template app's dataset.</span></span> <span data-ttu-id="3dabe-161">ชื่อพารามิเตอร์เป็นสตริงที่ต้องตรงตามตัวพิมพ์ใหญ่-เล็ก</span><span class="sxs-lookup"><span data-stu-id="3dabe-161">Parameter names are case-sensitive strings.</span></span> <span data-ttu-id="3dabe-162">ซึ่งยังสามารถดึงชื่อดังกล่าวได้จากแท็บ **การตั้งค่าพารามิเตอร์** เมื่อคุณ [กำหนดคุณสมบัติของแอปเทมเพลต](../../connect-data/service-template-apps-create.md#define-the-properties-of-the-template-app) หรือจากการตั้งค่าชุดข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3dabe-162">They can also be retrieved from the **Parameter Settings** tab when you [define the properties of the template app](../../connect-data/service-template-apps-create.md#define-the-properties-of-the-template-app) or from the dataset settings in Power BI.</span></span>

>[!NOTE]
><span data-ttu-id="3dabe-163">คุณสามารถทดสอบแอปพลิเคชันการติดตั้งที่กำหนดค่าไว้ล่วงหน้าบนแอปเทมเพลตของคุณได้หากแอปเทมเพลตพร้อมสำหรับการติดตั้งแม้ว่าจะยังไม่พร้อมใช้งานแบบสาธารณะใน AppSource ก็ตาม</span><span class="sxs-lookup"><span data-stu-id="3dabe-163">You can test your preconfigured installation application on your template app if the template app is ready for installation, even if it isn't publicly available on AppSource yet.</span></span> <span data-ttu-id="3dabe-164">เพื่อให้ผู้ใช้ภายนอกผู้เช่าของคุณสามารถใช้แอปพลิเคชันการติดตั้งอัตโนมัติเพื่อติดตั้งแอปเทมเพลตของคุณได้ แอปเทมเพลตจะต้องพร้อมใช้งานแบบสาธารณะใน [Power BI Apps marketplace](https://app.powerbi.com/getdata/services)</span><span class="sxs-lookup"><span data-stu-id="3dabe-164">For users outside your tenant to be able to use the automated installation application to install your template app, the template app must be publicly available in the [Power BI apps marketplace](https://app.powerbi.com/getdata/services).</span></span> <span data-ttu-id="3dabe-165">ก่อนที่คุณจะแจกจ่ายแอปเทมเพลตของคุณโดยใช้แอปพลิเคชันการติดตั้งอัตโนมัติที่คุณกำลังสร้างขึ้น อย่าลืมเผยแพร่ไปยัง[ศูนย์พันธมิตร](/azure/marketplace/partner-center-portal/create-power-bi-app-offer)ก่อน</span><span class="sxs-lookup"><span data-stu-id="3dabe-165">Before you distribute your template app by using the automated installation application you're creating, be sure to publish it to [Partner Center](/azure/marketplace/partner-center-portal/create-power-bi-app-offer).</span></span>


## <a name="install-and-configure-your-template-app"></a><span data-ttu-id="3dabe-166">ติดตั้งและกำหนดค่าแอปเทมเพลตของคุณ</span><span class="sxs-lookup"><span data-stu-id="3dabe-166">Install and configure your template app</span></span>

<span data-ttu-id="3dabe-167">ในส่วนนี้ คุณจะใช้ตัวอย่าง Azure Function สำหรับการติดตั้งอัตโนมัติที่เราสร้างขึ้นเพื่อกำหนดค่าล่วงหน้าและติดตั้งแอปเทมเพลตของคุณ</span><span class="sxs-lookup"><span data-stu-id="3dabe-167">In this section, you'll use an automated installation Azure Functions sample that we created to preconfigure and install your template app.</span></span> <span data-ttu-id="3dabe-168">ตัวอย่างนี้ถูกเก็บไว้อย่างตั้งใจเพื่อวัตถุประสงค์ในการสาธิต</span><span class="sxs-lookup"><span data-stu-id="3dabe-168">This sample has deliberately been kept simple for demonstration purposes.</span></span> <span data-ttu-id="3dabe-169">ซึ่งช่วยให้คุณสามารถใช้ [ฟังก์ชัน Azure](/azure/azure-functions/functions-overview) และ[การกำหนดค่าแอป Azure](/azure/azure-app-configuration/overview) เพื่อปรับใช้และใช้งาน API การติดตั้งอัตโนมัติสำหรับแอปเทมเพลตของคุณได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="3dabe-169">It allows you to use an [Azure function](/azure/azure-functions/functions-overview) and [Azure App Configuration](/azure/azure-app-configuration/overview) to easily deploy and use the automated installation API for your template apps.</span></span>

### <a name="download-visual-studio-version-2017-or-later"></a><span data-ttu-id="3dabe-170">ดาวน์โหลด [Visual Studio](https://www.visualstudio.com/) (เวอร์ชัน 2017 หรือใหม่กว่า)</span><span class="sxs-lookup"><span data-stu-id="3dabe-170">Download [Visual Studio](https://www.visualstudio.com/) (version 2017 or later)</span></span>

<span data-ttu-id="3dabe-171">ดาวน์โหลด [Visual Studio](https://www.visualstudio.com/) (เวอร์ชัน 2017 หรือใหม่กว่า)</span><span class="sxs-lookup"><span data-stu-id="3dabe-171">Download [Visual Studio](https://www.visualstudio.com/) (version 2017 or later).</span></span> <span data-ttu-id="3dabe-172">ทำให้แน่ใจว่าได้ดาวน์โหลด[แพคเกจ NuGet](https://www.nuget.org/profiles/powerbi)ล่าสุด</span><span class="sxs-lookup"><span data-stu-id="3dabe-172">Make sure to download the latest [NuGet package](https://www.nuget.org/profiles/powerbi).</span></span>

### <a name="download-the-automated-installation-azure-functions-sample"></a><span data-ttu-id="3dabe-173">ดาวน์โหลดตัวอย่างฟังก์ชัน Azure สำหรับการติดตั้งอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3dabe-173">Download the automated installation Azure Functions sample</span></span>

<span data-ttu-id="3dabe-174">ดาวน์โหลด[ตัวอย่างฟังก์ชัน Azure สำหรับการติดตั้งอัตโนมัติ](https://github.com/microsoft/Template-apps-examples/tree/master/Developer%20Samples/Automated%20Install%20Azure%20Function)จาก GitHub เพื่อเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3dabe-174">Download the [automated installation Azure Functions sample](https://github.com/microsoft/Template-apps-examples/tree/master/Developer%20Samples/Automated%20Install%20Azure%20Function) from GitHub to get started.</span></span>

![สกรีนช็อตที่แสดงตัวอย่างฟังก์ชัน Azure สำหรับการติดตั้งอัตโนมัติ](media/template-apps-auto-install/azure-function-sample.png)

### <a name="set-up-your-azure-app-configuration"></a><span data-ttu-id="3dabe-176">ติดตั้งการกำหนดค่าแอป Azure ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3dabe-176">Set up your Azure app configuration</span></span>

<span data-ttu-id="3dabe-177">เมื่อต้องการเรียกใช้ตัวอย่างนี้ คุณต้องตั้งค่าการกำหนดค่าแอป Azure ของคุณด้วยค่าและคีย์ตามที่อธิบายไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="3dabe-177">To run this sample, you need to set up your Azure app configuration with the values and keys as described here.</span></span> <span data-ttu-id="3dabe-178">คีย์คือ **ID แอปพลิเคชัน** **ข้อมูลลับของแอปพลิเคชัน** และ **AppId** **PackageKey** และค่า **OwnerId** ของแอปเทมเพลตของคุณ</span><span class="sxs-lookup"><span data-stu-id="3dabe-178">The keys are the **application ID**, the **application secret**, and your template app's **AppId**, **PackageKey**, and **OwnerId** values.</span></span> <span data-ttu-id="3dabe-179">ดูส่วนต่อไปนี้สำหรับข้อมูลเกี่ยวกับวิธีการรับค่าเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="3dabe-179">See the following sections for information about how to get these values.</span></span>

<span data-ttu-id="3dabe-180">นอกจากนี้ยังมีการกำหนดคีย์ไว้ในไฟล์ **Constants.cs** อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="3dabe-180">The keys are also defined in the **Constants.cs** file.</span></span>

| <span data-ttu-id="3dabe-181">คีย์การกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="3dabe-181">Configuration key</span></span> | <span data-ttu-id="3dabe-182">ความหมาย</span><span class="sxs-lookup"><span data-stu-id="3dabe-182">Meaning</span></span>           |
|---------------    |-------------------|
| <span data-ttu-id="3dabe-183">TemplateAppInstall:Application:AppId</span><span class="sxs-lookup"><span data-stu-id="3dabe-183">TemplateAppInstall:Application:AppId</span></span> | <span data-ttu-id="3dabe-184">**AppId** จาก [URL การติดตั้ง](#get-the-template-app-properties)</span><span class="sxs-lookup"><span data-stu-id="3dabe-184">**AppId** from the  [installation URL](#get-the-template-app-properties)</span></span> |
| <span data-ttu-id="3dabe-185">TemplateAppInstall:Application:PackageKey</span><span class="sxs-lookup"><span data-stu-id="3dabe-185">TemplateAppInstall:Application:PackageKey</span></span> | <span data-ttu-id="3dabe-186">**PackageKey** จาก [URL การติดตั้ง](#get-the-template-app-properties)</span><span class="sxs-lookup"><span data-stu-id="3dabe-186">**PackageKey** from the [installation URL](#get-the-template-app-properties)</span></span> |
| <span data-ttu-id="3dabe-187">TemplateAppInstall:Application:OwnerId</span><span class="sxs-lookup"><span data-stu-id="3dabe-187">TemplateAppInstall:Application:OwnerId</span></span> | <span data-ttu-id="3dabe-188">**OwnerId** จาก [URL การติดตั้ง](#get-the-template-app-properties)</span><span class="sxs-lookup"><span data-stu-id="3dabe-188">**OwnerId** from the [installation URL](#get-the-template-app-properties)</span></span> |
| <span data-ttu-id="3dabe-189">TemplateAppInstall:ServicePrincipal:ClientId</span><span class="sxs-lookup"><span data-stu-id="3dabe-189">TemplateAppInstall:ServicePrincipal:ClientId</span></span> | <span data-ttu-id="3dabe-190">[ID แอปพลิเคชัน](#get-the-application-id)สำหรับองค์ประกอบหลักของบริการ</span><span class="sxs-lookup"><span data-stu-id="3dabe-190">Service principal [application ID](#get-the-application-id)</span></span> |
| <span data-ttu-id="3dabe-191">TemplateAppInstall:ServicePrincipal:ClientSecret</span><span class="sxs-lookup"><span data-stu-id="3dabe-191">TemplateAppInstall:ServicePrincipal:ClientSecret</span></span> | <span data-ttu-id="3dabe-192">[ข้อมูลลับของแอปพลิเคชัน](#get-the-application-secret)สำหรับองค์ประกอบหลักของบริการ</span><span class="sxs-lookup"><span data-stu-id="3dabe-192">Service principal [application secret](#get-the-application-secret)</span></span> |
|||


<span data-ttu-id="3dabe-193">ไฟล์ **Constants.cs** จะแสดงที่นี่</span><span class="sxs-lookup"><span data-stu-id="3dabe-193">The **Constants.cs** file is shown here.</span></span>

![สกรีนช็อตที่แสดงไฟล์ Constant.cs](media/template-apps-auto-install/constants-app-configuration.png)

#### <a name="get-the-template-app-properties"></a><span data-ttu-id="3dabe-195">รับคุณสมบัติแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="3dabe-195">Get the template app properties</span></span>

<span data-ttu-id="3dabe-196">กรอกคุณสมบัติของแอปเทมเพลตที่เกี่ยวข้องทั้งหมดตามที่กำหนดไว้เมื่อสร้างแอป</span><span class="sxs-lookup"><span data-stu-id="3dabe-196">Fill in all relevant template app properties as they're defined when the app is created.</span></span> <span data-ttu-id="3dabe-197">คุณสมบัติเหล่านี้คือ **AppId**, **PackageKey** และ **OwnerId** ของแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="3dabe-197">These properties are the template app's **AppId**, **PackageKey**, and **OwnerId** values.</span></span>

<span data-ttu-id="3dabe-198">เมื่อต้องการรับค่าก่อนหน้า ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="3dabe-198">To get the preceding values, follow these steps:</span></span>

1. <span data-ttu-id="3dabe-199">ลงชื่อเข้าใช้ [Power BI](https://app.powerbi.com)</span><span class="sxs-lookup"><span data-stu-id="3dabe-199">Sign in to [Power BI](https://app.powerbi.com).</span></span>

1. <span data-ttu-id="3dabe-200">ไปยังพื้นที่ทำงานเดิมของแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="3dabe-200">Go to the application's original workspace.</span></span>

1. <span data-ttu-id="3dabe-201">เปิดบานหน้าต่าง **การจัดการนำไปใช้งานจริง**</span><span class="sxs-lookup"><span data-stu-id="3dabe-201">Open the **Release Management** pane.</span></span>

    ![สกรีนช็อตที่แสดงบานหน้าต่างการจัดการนำไปใช้งานจริง](media/template-apps-auto-install/release-management-001.png)

1. <span data-ttu-id="3dabe-203">เลือกเวอร์ชันแอปและรับลิงก์การติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="3dabe-203">Select the app version, and get its installation link.</span></span>

    ![สกรีนช็อตที่แสดงปุ่มการจัดการนำไปใช้งานจริง](media/template-apps-auto-install/release-management-002.png)

1. <span data-ttu-id="3dabe-205">คัดลอกลิงก์ไปยังคลิปบอร์ด</span><span class="sxs-lookup"><span data-stu-id="3dabe-205">Copy the link to the clipboard.</span></span>

    ![สกรีนช็อตที่แสดงปุ่ม “รับลิงก์”](media/template-apps-auto-install/release-management-003.png)

1. <span data-ttu-id="3dabe-207">URL การติดตั้งนี้จะเก็บพารามิเตอร์ URL สามค่าที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="3dabe-207">This installation URL holds the three URL parameters whose values you need.</span></span> <span data-ttu-id="3dabe-208">ใช้ค่า **appId**, **packageKey** และ **ownerId** สำหรับแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="3dabe-208">Use the **appId**, **packageKey**, and **ownerId** values for the application.</span></span> <span data-ttu-id="3dabe-209">URL ตัวอย่างจะคล้ายกับที่แสดงที่นี่</span><span class="sxs-lookup"><span data-stu-id="3dabe-209">A sample URL will be similar to what is shown here.</span></span>

    ```html
    https://app.powerbi.com/Redirect?action=InstallApp&appId=3c386...16bf71c67&packageKey=b2df4b...dLpHIUnum2pr6k&ownerId=72f9...1db47&buildVersion=5
    ```

#### <a name="get-the-application-id"></a><span data-ttu-id="3dabe-210">รับ ID แอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="3dabe-210">Get the application ID</span></span>

<span data-ttu-id="3dabe-211">ป้อนข้อมูลช่อง **applicationId** ด้วย ID แอปพลิเคชันจาก Azure</span><span class="sxs-lookup"><span data-stu-id="3dabe-211">Fill in the **applicationId** information with the application ID from Azure.</span></span> <span data-ttu-id="3dabe-212">แอปพลิเชันจะใช้ค่า **applicationId** เพื่อระบุตัวเองไปยังผู้ใช้จากที่คุณกำลังขอสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="3dabe-212">The **applicationId** value is used by the application to identify itself to the users from which you're requesting permissions.</span></span>

<span data-ttu-id="3dabe-213">สำหรับวิธีรับ ID แอปพลิเคชัน ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3dabe-213">To get the application ID, follow these steps:</span></span>

1. <span data-ttu-id="3dabe-214">ลงชื่อเข้าใช้ไปยัง [พอร์ทัล Azure](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="3dabe-214">Sign in to the [Azure portal](https://portal.azure.com).</span></span>

1. <span data-ttu-id="3dabe-215">ในบานหน้าต่างด้านซ้าย ให้เลือก **บริการทั้งหมด** > **การลงทะเบียนแอป**</span><span class="sxs-lookup"><span data-stu-id="3dabe-215">In the left pane, select **All services** > **App registrations**.</span></span>

    ![สกรีนช็อตที่แสดงการค้นหาการลงทะเบียนแอป](media/template-apps-auto-install/embed-sample-for-customers-003.png)

1. <span data-ttu-id="3dabe-217">เลือกแอปพลิเคชันที่ต้องใช้ **ID แอปพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="3dabe-217">Select the application that needs the **application ID**.</span></span>

    ![สกรีนช็อตที่แสดงการเลือกแอป](media/template-apps-auto-install/embed-sample-for-customers-006.png)

1. <span data-ttu-id="3dabe-219">มี ID แอปพลิเคชันที่แสดงในรูปของ GUID</span><span class="sxs-lookup"><span data-stu-id="3dabe-219">There's an application ID that's listed as a GUID.</span></span> <span data-ttu-id="3dabe-220">ใช้ ID แอปพลิเคชันนี้เป็นค่า **applicationId** สำหรับแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="3dabe-220">Use this application ID as the **applicationId** value for the application.</span></span>

    ![สกรีนช็อตที่แสดงค่า applicationId](media/template-apps-auto-install/embed-sample-for-customers-007.png)

#### <a name="get-the-application-secret"></a><span data-ttu-id="3dabe-222">รับความลับของแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="3dabe-222">Get the application secret</span></span>

<span data-ttu-id="3dabe-223">ป้อนข้อมูล **ApplicationSecret** จากส่วน **คีย์** ของส่วน **การลงทะเบียนแอปพลิเคชัน** ใน Azure</span><span class="sxs-lookup"><span data-stu-id="3dabe-223">Fill in the **ApplicationSecret** information from the **Keys** section of your **App registrations** section in Azure.</span></span> <span data-ttu-id="3dabe-224">แอตทริบิวต์นี้ทำงานเมื่อคุณใช้[องค์ประกอบหลักของบริการ](../embedded/embed-service-principal.md)</span><span class="sxs-lookup"><span data-stu-id="3dabe-224">This attribute works when you use the [service principal](../embedded/embed-service-principal.md).</span></span>

<span data-ttu-id="3dabe-225">สำหรับวิธีรับข้อมูลลับของแอปพลิเคชัน ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3dabe-225">To get the application secret, follow these steps:</span></span>

 1. <span data-ttu-id="3dabe-226">ลงชื่อเข้าใช้ไปยัง [พอร์ทัล Azure](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="3dabe-226">Sign in to the [Azure portal](https://portal.azure.com).</span></span>

 1. <span data-ttu-id="3dabe-227">ในบานหน้าต่างด้านซ้าย ให้เลือก **บริการทั้งหมด** > **การลงทะเบียนแอป**</span><span class="sxs-lookup"><span data-stu-id="3dabe-227">In the left pane, select **All services** > **App registrations**.</span></span>

    ![สกรีนช็อตที่แสดงการค้นหาการลงทะเบียนแอป](media/template-apps-auto-install/embed-sample-for-customers-003.png)

1. <span data-ttu-id="3dabe-229">เลือกแอปพลิเคชันที่ต้องใช้ **ข้อมูลลับของแอปพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="3dabe-229">Select the application that needs to use the **application secret**.</span></span>

    ![สกรีนช็อตแสดงการเลือกแอป](media/template-apps-auto-install/embed-sample-for-customers-0038.png)

1. <span data-ttu-id="3dabe-231">เลือก **ใบรับรองและข้อมูลลับ** ภายใต้ **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="3dabe-231">Select **Certificates and secrets** under **Manage**.</span></span>

1. <span data-ttu-id="3dabe-232">เลือก **ข้อมูลลับไคลเอ็นต์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="3dabe-232">Select **New client secrets**.</span></span>

1. <span data-ttu-id="3dabe-233">ป้อนชื่อในกล่อง **คำอธิบาย** และเลือกระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="3dabe-233">Enter a name in the **Description** box, and select a duration.</span></span> <span data-ttu-id="3dabe-234">จากนั้นเลือก **บันทึก** เพื่อรับค่าสำหรับแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="3dabe-234">Then select **Save** to get the value for your application.</span></span> <span data-ttu-id="3dabe-235">เมื่อคุณเลือกบานหน้าต่าง **คีย์** หลังจากคุณบันทึกค่าคีย์แล้ว ช่อง **ค่า** จะถูกซ่อนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3dabe-235">When you close the **Keys** pane after you save the key value, the **Value** field shows only as hidden.</span></span> <span data-ttu-id="3dabe-236">ในขั้นตอนนี้คุณจะไม่สามารถเรียกดูค่าคีย์ได้</span><span class="sxs-lookup"><span data-stu-id="3dabe-236">At that point, you aren't able to retrieve the key value.</span></span> <span data-ttu-id="3dabe-237">หากคุณทำค่าคีย์หาย ให้สร้างใหม่ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="3dabe-237">If you lose the key value, create a new one in the Azure portal.</span></span>

    ![สกรีนช็อตที่แสดงค่าคีย์](media/template-apps-auto-install/embed-sample-for-customers-042.png)

## <a name="test-your-function-locally"></a><span data-ttu-id="3dabe-239">ทดสอบฟังก์ชันของคุณภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="3dabe-239">Test your function locally</span></span>

<span data-ttu-id="3dabe-240">ทำตามขั้นตอนตามที่อธิบายไว้ใน[เรียกใช้ฟังก์ชันภายในเครื่อง](/azure/azure-functions/functions-create-your-first-function-visual-studio#run-the-function-locally)เพื่อเรียกใช้ฟังก์ชันของคุณ</span><span class="sxs-lookup"><span data-stu-id="3dabe-240">Follow the steps as described in [Run the function locally](/azure/azure-functions/functions-create-your-first-function-visual-studio#run-the-function-locally) to run your function.</span></span>

<span data-ttu-id="3dabe-241">กำหนดค่าพอร์ทัลของคุณเพื่อส่งคำขอ ```POST``` ไปยัง URL ของฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="3dabe-241">Configure your portal to issue a ```POST``` request to the URL of the function.</span></span> <span data-ttu-id="3dabe-242">ตัวอย่างคือ ```POST http://localhost:7071/api/install```</span><span class="sxs-lookup"><span data-stu-id="3dabe-242">An example is ```POST http://localhost:7071/api/install```.</span></span> <span data-ttu-id="3dabe-243">เนื้อความคำขอควรเป็นออบเจ็กต์ JSON ที่อธิบายถึงคู่ค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="3dabe-243">The request body should be a JSON object that describes key-value pairs.</span></span> <span data-ttu-id="3dabe-244">คีย์คือ *ชื่อพารามิเตอร์* ตามที่กำหนดใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3dabe-244">Keys are *parameter names* as defined in Power BI Desktop.</span></span> <span data-ttu-id="3dabe-245">ค่าคือค่าที่ต้องการตั้งสำหรับแต่ละพารามิเตอร์ในแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="3dabe-245">Values are the desired values to be set for each parameter in the template app.</span></span>

>[!Note]
> <span data-ttu-id="3dabe-246">ในการผลิต ค่าพารามิเตอร์จะถูกอนุมานสำหรับผู้ใช้แต่ละรายโดยตรรกะที่เตรียมเอาไว้ของพอร์ทัลของคุณ</span><span class="sxs-lookup"><span data-stu-id="3dabe-246">In production, parameter values are deduced for each user by your portal's intended logic.</span></span>

<span data-ttu-id="3dabe-247">โฟลว์ที่ต้องการควรเป็น:</span><span class="sxs-lookup"><span data-stu-id="3dabe-247">The desired flow should be:</span></span>

1. <span data-ttu-id="3dabe-248">พอร์ทัลจัดเตรียมคำขอ ต่อผู้ใช้หรือเซสชัน</span><span class="sxs-lookup"><span data-stu-id="3dabe-248">The portal prepares the request, per user or session.</span></span>
1. <span data-ttu-id="3dabe-249">มีการส่งคำขอ ```POST /api/install``` ไปยังฟังก์ชัน Azure ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3dabe-249">The ```POST /api/install``` request is issued to your Azure function.</span></span> <span data-ttu-id="3dabe-250">เนื้อความคำขอประกอบด้วยคู่ค่าคีย์</span><span class="sxs-lookup"><span data-stu-id="3dabe-250">The request body consists of key-value pairs.</span></span> <span data-ttu-id="3dabe-251">คีย์คือชื่อพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="3dabe-251">The key is the parameter name.</span></span> <span data-ttu-id="3dabe-252">ค่านี้เป็นค่าที่ต้องการตั้ง</span><span class="sxs-lookup"><span data-stu-id="3dabe-252">The value is the desired value to be set.</span></span>
1. <span data-ttu-id="3dabe-253">หากกำหนดค่าทั้งหมดอย่างถูกต้องแล้ว เบราว์เซอร์ควรเปลี่ยนเส้นทางไปยังบัญชี Power BI ของลูกค้าโดยอัตโนมัติและแสดงโฟลว์การติดตั้งแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3dabe-253">If everything is configured properly, the browser should automatically redirect to the customer's Power BI account and show the automated installation flow.</span></span>
1. <span data-ttu-id="3dabe-254">เมื่อติดตั้งแล้ว ค่าพารามิเตอร์จะถูกตั้งค่าตามที่กำหนดไว้ในขั้นตอนที่ 1 และ 2</span><span class="sxs-lookup"><span data-stu-id="3dabe-254">Upon installation, parameter values are set as configured in steps 1 and 2.</span></span>
 
## <a name="next-steps"></a><span data-ttu-id="3dabe-255">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3dabe-255">Next steps</span></span>

### <a name="publish-your-project-to-azure"></a><span data-ttu-id="3dabe-256">เผยแพร่โครงการของคุณไปยัง Azure</span><span class="sxs-lookup"><span data-stu-id="3dabe-256">Publish your project to Azure</span></span>

<span data-ttu-id="3dabe-257">หากต้องการเผยแพร่โครงการของคุณไปยัง Azure ให้ทำตามคำแนะนำใน[เอกสารของฟังก์ชัน Azure](/azure/azure-functions/functions-create-your-first-function-visual-studio#publish-the-project-to-azure)</span><span class="sxs-lookup"><span data-stu-id="3dabe-257">To publish your project to Azure, follow the instructions in the [Azure Functions documentation](/azure/azure-functions/functions-create-your-first-function-visual-studio#publish-the-project-to-azure).</span></span> <span data-ttu-id="3dabe-258">จากนั้นคุณสามารถรวม API การติดตั้งอัตโนมัติของแอปเทมเพลตเข้ากับผลิตภัณฑ์ของคุณและเริ่มทดสอบในสภาพแวดล้อมการผลิต</span><span class="sxs-lookup"><span data-stu-id="3dabe-258">Then you can integrate template app automated installation APIs into your product and begin testing it in production environments.</span></span>