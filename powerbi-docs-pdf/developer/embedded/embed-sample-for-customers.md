---
title: ฝังเนื้อหาในแอปพลิเคชันการวิเคราะห์แบบฝังตัว Power BI ของคุณเพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นสําหรับลูกค้าของคุณ
description: เรียนรู้วิธีการฝังรายงาน แดชบอร์ด หรือไทล์ลงในตัวอย่างการวิเคราะห์แบบฝังตัวของ Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: rkarlin
ms.topic: tutorial
ms.service: powerbi
ms.subservice: powerbi-developer
ms.custom: seodec18
ms.date: 12/22/2020
ms.openlocfilehash: a0cfeaece56594c52a8d747350c5f9bfb0886cad
ms.sourcegitcommit: 1cad78595cca1175b82c04458803764ac36e5e37
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/19/2021
ms.locfileid: "98565478"
---
# <a name="tutorial-embed-power-bi-content-using-a-sample-embed-for-your-customers-application"></a><span data-ttu-id="6802a-104">บทช่วยสอน: ฝังเนื้อหา Power BI โดยใช้แอปพลิเคชันตัวอย่าง *การฝังตัวสำหรับลูกค้าของคุณ*</span><span class="sxs-lookup"><span data-stu-id="6802a-104">Tutorial: Embed Power BI content using a sample *embed for your customers* application</span></span>

<span data-ttu-id="6802a-105">**การวิเคราะห์แบบฝังตัว** และ **Power BI Embedded** (ข้อเสนอของ Azure) ช่วยให้คุณสามารถฝังเนื้อหา Power BI เช่น รายงาน แดชบอร์ด และไทล์ลงในแอปพลิเคชันของคุณได้</span><span class="sxs-lookup"><span data-stu-id="6802a-105">**Embedded analytics** and **Power BI Embedded** (the Azure offer) allow you to embed Power BI content such as reports, dashboards and tiles, into your application.</span></span>

<span data-ttu-id="6802a-106">ในบทช่วยสอนนี้ คุณจะเรียนรู้วิธีการ:</span><span class="sxs-lookup"><span data-stu-id="6802a-106">In this tutorial, you'll learn how to:</span></span>
>[!div class="checklist"]
>* <span data-ttu-id="6802a-107">ตั้งค่าสภาพแวดล้อมแบบฝังตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-107">Set up your embedded environment.</span></span>
>* <span data-ttu-id="6802a-108">กำหนดค่าแอปพลิเคชันตัวอย่าง *การฝังตัวสำหรับลูกค้าของคุณ* (หรือที่เรียกว่า *แอปเป็นเจ้าของข้อมูล*)</span><span class="sxs-lookup"><span data-stu-id="6802a-108">Configure an *embed for your customers* (also known as *app owns data*) sample application.</span></span>

<span data-ttu-id="6802a-109">หากต้องการใช้แอปพลิเคชันของคุณ ผู้ใช้ของคุณจะไม่จำเป็นต้องลงชื่อเข้าใช้ Power BI หรือไม่จำเป็นต้องมีสิทธิการใช้งาน Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-109">To use your application, your users will not need to sign in to Power BI or have a Power BI license.</span></span>

<span data-ttu-id="6802a-110">เราขอแนะนำให้ใช้วิธี *การฝังตัวสำหรับลูกค้าของคุณ* เพื่อฝังเนื้อหา Power BI ของคุณ หากคุณเป็นผู้จำหน่ายซอฟต์แวร์อิสระ (ISV) หรือนักพัฒนาที่ต้องการสร้างแอปพลิเคชันสำหรับบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="6802a-110">We recommend using the *embed for your customers* method to embed your Power BI content, if you're an independent software vendor (ISV) or a developer, who wants to create applications for third parties.</span></span>

## <a name="code-sample-specifications"></a><span data-ttu-id="6802a-111">ข้อมูลจำเพาะตัวอย่างของโค้ด</span><span class="sxs-lookup"><span data-stu-id="6802a-111">Code sample specifications</span></span>

<span data-ttu-id="6802a-112">บทช่วยสอนนี้ประกอบด้วยคำแนะนำสำหรับการกำหนดค่าแอปพลิเคชันตัวอย่าง *การฝังตัวสำหรับลูกค้าของคุณ* สำหรับหนึ่งในภาษาต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-112">This tutorial includes instructions for configuring an *embed for your customers* sample application in one of the following languages:</span></span>

* <span data-ttu-id="6802a-113">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="6802a-113">.NET Framework</span></span>
* <span data-ttu-id="6802a-114">.NET Core</span><span class="sxs-lookup"><span data-stu-id="6802a-114">.NET Core</span></span>
* <span data-ttu-id="6802a-115">Java</span><span class="sxs-lookup"><span data-stu-id="6802a-115">Java</span></span>
* <span data-ttu-id="6802a-116">Node JS</span><span class="sxs-lookup"><span data-stu-id="6802a-116">Node JS</span></span>
* <span data-ttu-id="6802a-117">Python</span><span class="sxs-lookup"><span data-stu-id="6802a-117">Python</span></span>

<span data-ttu-id="6802a-118">ตัวอย่างโค้ดรองรับเบราว์เซอร์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-118">The code samples support the following browsers:</span></span>

* <span data-ttu-id="6802a-119">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="6802a-119">Google Chrome</span></span>

* <span data-ttu-id="6802a-120">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6802a-120">Microsoft Edge</span></span>

* <span data-ttu-id="6802a-121">Mozilla Firefox</span><span class="sxs-lookup"><span data-stu-id="6802a-121">Mozilla Firefox</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6802a-122">สิ่งที่จำเป็นต้องมี</span><span class="sxs-lookup"><span data-stu-id="6802a-122">Prerequisites</span></span>

<span data-ttu-id="6802a-123">ก่อนที่คุณจะเริ่มต้นบทช่วยสอนนี้ ให้ตรวจสอบว่าคุณมีการขึ้นต่อกันทั้งของ Power BI และโค้ดที่แสดงรายการด้านล่าง:</span><span class="sxs-lookup"><span data-stu-id="6802a-123">Before you start this tutorial, verify that you have both the Power BI and code dependencies listed below:</span></span>

* <span data-ttu-id="6802a-124">**การขึ้นต่อกันของ Power BI**</span><span class="sxs-lookup"><span data-stu-id="6802a-124">**Power BI dependencies**</span></span>

    * <span data-ttu-id="6802a-125">[ผู้เช่า Azure Active Directory](create-an-azure-active-directory-tenant.md) ของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="6802a-125">Your own [Azure Active Directory tenant](create-an-azure-active-directory-tenant.md).</span></span>

    * <span data-ttu-id="6802a-126">หากต้องการรับรองความถูกต้องของแอปกับ Power BI คุณจะต้องมีหนึ่งในรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-126">To authenticate your app against Power BI, you'll need one of the following:</span></span>

        * <span data-ttu-id="6802a-127">[โครงร่างสำคัญของบริการ](embed-service-principal.md) - Azure Active Directory (Azure AD) [ออบเจ็กต์โครงร่างสำคัญของบริการ](/azure/active-directory/develop/app-objects-and-service-principals#service-principal-object)ที่อนุญาตให้ Azure AD รับรองความถูกต้องของแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-127">[Service principal](embed-service-principal.md) - An Azure Active Directory (Azure AD) [service principal object](/azure/active-directory/develop/app-objects-and-service-principals#service-principal-object) that allows Azure AD to authenticate your app.</span></span>

        * <span data-ttu-id="6802a-128">สิทธิ์การใช้งาน [Power BI Pro](../../admin/service-admin-purchasing-power-bi-pro.md) - ซึ่งจะเป็น **ผู้ใช้หลัก** ของคุณและแอปของคุณจะใช้เพื่อรับรองความถูกต้องกับ Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-128">[Power BI Pro](../../admin/service-admin-purchasing-power-bi-pro.md) license - This will be your **master user** and your app will use it to authenticate to Power BI.</span></span>

        * <span data-ttu-id="6802a-129">สิทธิ์การใช้งาน Power BI [Premium Per User (PPU)](../../admin/service-premium-per-user-faq.md) - ซึ่งจะเป็น **ผู้ใช้หลัก** ของคุณและแอปของคุณจะใช้เพื่อรับรองความถูกต้องกับ Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-129">A Power BI [Premium Per User (PPU)](../../admin/service-premium-per-user-faq.md) license - This will be your **master user** and your app will use it to authenticate to Power BI.</span></span>

    >[!NOTE]
    ><span data-ttu-id="6802a-130">หากต้องการ[ย้ายไปยังการผลิต](move-to-production.md) คุณจะต้องมี[ความจุ](embedded-capacity.md)</span><span class="sxs-lookup"><span data-stu-id="6802a-130">To [move to production](move-to-production.md) you'll need a [capacity](embedded-capacity.md).</span></span>

* <span data-ttu-id="6802a-131">**การขึ้นต่อกันของโค้ด**</span><span class="sxs-lookup"><span data-stu-id="6802a-131">**Code dependencies**</span></span>

    # <a name="net-framework"></a>[<span data-ttu-id="6802a-132">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="6802a-132">.NET Framework</span></span>](#tab/net-framework)
    
    * [<span data-ttu-id="6802a-133">.NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="6802a-133">.NET Framework 4.8</span></span>](https://dotnet.microsoft.com/download/dotnet-framework/)
    
    * [<span data-ttu-id="6802a-134">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6802a-134">Visual Studio</span></span>](https://visualstudio.microsoft.com/)
    
    
    # <a name="net-core"></a>[<span data-ttu-id="6802a-135">.NET Core</span><span class="sxs-lookup"><span data-stu-id="6802a-135">.NET Core</span></span>](#tab/net-core)
    
    * <span data-ttu-id="6802a-136">[.NET Core 3.1 SDK](https://dotnet.microsoft.com/download/dotnet-core) (หรือสูงกว่า)</span><span class="sxs-lookup"><span data-stu-id="6802a-136">[.NET Core 3.1 SDK](https://dotnet.microsoft.com/download/dotnet-core) (or higher)</span></span>
    
    * <span data-ttu-id="6802a-137">เครื่องมือพัฒนาโปรแกรม (integrated development environment : IDE)</span><span class="sxs-lookup"><span data-stu-id="6802a-137">An integrated development environment (IDE).</span></span> <span data-ttu-id="6802a-138">เราขอแนะนำให้ใช้หนึ่งในรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-138">We recommend using one of the following:</span></span>
    
        * [<span data-ttu-id="6802a-139">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6802a-139">Visual Studio</span></span>](https://visualstudio.microsoft.com/)
    
        * [<span data-ttu-id="6802a-140">รหัส Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6802a-140">Visual Studio Code</span></span>](https://code.visualstudio.com/)

    # <a name="java"></a>[<span data-ttu-id="6802a-141">Java</span><span class="sxs-lookup"><span data-stu-id="6802a-141">Java</span></span>](#tab/java)
    
    * [<span data-ttu-id="6802a-142">JDK (หรือ JRE)</span><span class="sxs-lookup"><span data-stu-id="6802a-142">JDK (or JRE)</span></span>](https://www.oracle.com/java/technologies/)
    
    * <span data-ttu-id="6802a-143">[Eclipse IDE](https://www.eclipse.org/downloads/packages/) - ตรวจสอบว่าคุณมี *Eclipse for Java EE Developers* (รุ่นสำหรับองค์กร)</span><span class="sxs-lookup"><span data-stu-id="6802a-143">[Eclipse IDE](https://www.eclipse.org/downloads/packages/) - Verify that you have the *Eclipse for Java EE Developers* (enterprise edition)</span></span>
    
    * [<span data-ttu-id="6802a-144">Apache Tomcat Binary Distributions</span><span class="sxs-lookup"><span data-stu-id="6802a-144">Apache Tomcat Binary Distributions</span></span>](https://tomcat.apache.org/)
    
    # <a name="node-js"></a>[<span data-ttu-id="6802a-145">Node JS</span><span class="sxs-lookup"><span data-stu-id="6802a-145">Node JS</span></span>](#tab/node-js)
    
    * [<span data-ttu-id="6802a-146">.NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="6802a-146">.NET Framework 4.8</span></span>](https://dotnet.microsoft.com/download/dotnet-framework/)
    
    * <span data-ttu-id="6802a-147">เครื่องมือพัฒนาโปรแกรม (integrated development environment : IDE)</span><span class="sxs-lookup"><span data-stu-id="6802a-147">An integrated development environment (IDE).</span></span> <span data-ttu-id="6802a-148">เราขอแนะนำให้ใช้หนึ่งในรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-148">We recommend using one of the following:</span></span>
    
        * [<span data-ttu-id="6802a-149">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6802a-149">Visual Studio</span></span>](https://visualstudio.microsoft.com/)
    
        * [<span data-ttu-id="6802a-150">รหัส Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6802a-150">Visual Studio Code</span></span>](https://code.visualstudio.com/)
    
    # <a name="python"></a>[<span data-ttu-id="6802a-151">Python</span><span class="sxs-lookup"><span data-stu-id="6802a-151">Python</span></span>](#tab/python)
    
    * <span data-ttu-id="6802a-152">[Python 3](https://www.python.org/downloads/) (หรือสูงกว่า)</span><span class="sxs-lookup"><span data-stu-id="6802a-152">[Python 3](https://www.python.org/downloads/) (or higher)</span></span>
    
        >[!NOTE]
        >* <span data-ttu-id="6802a-153">หากคุณติดตั้ง *Python* เป็นครั้งแรก ให้เลือกตัวเลือก **เพิ่ม Python ไปยัง PATH** เพื่อเพิ่มการติดตั้งลงในตัวแปร `PATH`</span><span class="sxs-lookup"><span data-stu-id="6802a-153">If you're installing *Python* for the first time, select the **Add Python to PATH** option, to add the installation to the `PATH` variable.</span></span>
        >* <span data-ttu-id="6802a-154">หากคุณติดตั้ง *Python* ไว้แล้วให้ตรวจสอบว่าตัวแปร `PATH` มีเส้นทางการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="6802a-154">If you already have *Python* installed, verify that the `PATH` variable includes its installation path.</span></span> <span data-ttu-id="6802a-155">สำหรับข้อมูลเพิ่มเติม โปรดดู [Excursus: การตั้งค่าตัวแปรของสภาพแวดล้อม](https://docs.python.org/3/using/windows.html#excursus-setting-environment-variables) เอกสารประกอบ Python (ลิงก์นี้อ้างอิงถึง Python 3)</span><span class="sxs-lookup"><span data-stu-id="6802a-155">For more information, see the [Excursus: Setting environment variables](https://docs.python.org/3/using/windows.html#excursus-setting-environment-variables) Python documentation (this link refers to Python 3).</span></span>
    
    * <span data-ttu-id="6802a-156">เครื่องมือพัฒนาโปรแกรม (integrated development environment : IDE)</span><span class="sxs-lookup"><span data-stu-id="6802a-156">An integrated development environment (IDE).</span></span> <span data-ttu-id="6802a-157">เราขอแนะนำให้ใช้หนึ่งในรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-157">We recommend using one of the following:</span></span>
    
        * [<span data-ttu-id="6802a-158">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6802a-158">Visual Studio</span></span>](https://visualstudio.microsoft.com/)
    
        * [<span data-ttu-id="6802a-159">รหัส Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6802a-159">Visual Studio Code</span></span>](https://code.visualstudio.com/)
    
    ---

## <a name="method"></a><span data-ttu-id="6802a-160">วิธีการ</span><span class="sxs-lookup"><span data-stu-id="6802a-160">Method</span></span>

<span data-ttu-id="6802a-161">หากต้องการสร้างแอปตัวอย่าง *การฝังตัวสำหรับลูกค้าของคุณ* ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-161">To create an *embed for your customers* sample app, follow these steps:</span></span>

1. <span data-ttu-id="6802a-162">[เลือกวิธีการรับรองความถูกต้องของคุณ](#step-1---select-your-authentication-method)</span><span class="sxs-lookup"><span data-stu-id="6802a-162">[Select your authentication method](#step-1---select-your-authentication-method).</span></span>

2. <span data-ttu-id="6802a-163">[ลงทะเบียนแอปพลิเคชัน Azure AD](#step-2---register-an-azure-ad-application)</span><span class="sxs-lookup"><span data-stu-id="6802a-163">[Register an Azure AD application](#step-2---register-an-azure-ad-application).</span></span>

3. <span data-ttu-id="6802a-164">[สร้างพื้นที่ทำงาน Power BI](#step-3---create-a-power-bi-workspace)</span><span class="sxs-lookup"><span data-stu-id="6802a-164">[Create a Power BI workspace](#step-3---create-a-power-bi-workspace).</span></span>

4. <span data-ttu-id="6802a-165">[สร้าง และเผยแพร่รายงาน Power BI](#step-4---create-and-publish-a-power-bi-report)</span><span class="sxs-lookup"><span data-stu-id="6802a-165">[Create and publish a Power BI report](#step-4---create-and-publish-a-power-bi-report).</span></span>

5. <span data-ttu-id="6802a-166">[รับค่าพารามิเตอร์การฝัง](#step-5---get-the-embedding-parameter-values)</span><span class="sxs-lookup"><span data-stu-id="6802a-166">[Get the embedding parameter values](#step-5---get-the-embedding-parameter-values).</span></span>

6. [<span data-ttu-id="6802a-167">สิทธิ์การเข้าถึง API ของโครงร่างสำคัญของบริการ</span><span class="sxs-lookup"><span data-stu-id="6802a-167">Service principal API access</span></span>](#step-6---service-principal-api-access)
 
7. <span data-ttu-id="6802a-168">[เปิดใช้งานการเข้าถึงพื้นที่ทำงาน](#step-7---enable-workspace-access)</span><span class="sxs-lookup"><span data-stu-id="6802a-168">[Enable workspace access](#step-7---enable-workspace-access).</span></span>

8. <span data-ttu-id="6802a-169">[ฝังตัวเนื้อหาของคุณ](#step-8---embed-your-content)</span><span class="sxs-lookup"><span data-stu-id="6802a-169">[Embed your content](#step-8---embed-your-content).</span></span>

## <a name="step-1---select-your-authentication-method"></a><span data-ttu-id="6802a-170">ขั้นตอนที่ 1 - เลือกวิธีการรับรองความถูกต้องของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-170">Step 1 - Select your authentication method</span></span>

<span data-ttu-id="6802a-171">โซลูชันแบบฝังตัวของคุณจะแตกต่างกันโดยขึ้นอยู่กับวิธีการรับรองความถูกต้องที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="6802a-171">Your embedded solution will vary depending on the authentication method you select.</span></span> <span data-ttu-id="6802a-172">ดังนั้นสิ่งสำคัญคือต้องเข้าใจความแตกต่างระหว่างวิธีการรับรองความถูกต้องและตัดสินใจว่าวิธีใดเหมาะสมกับโซลูชันของคุณมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="6802a-172">Therefore, it's important to understand the differences between the authentication methods, and decide which one best suits your solution.</span></span>

<span data-ttu-id="6802a-173">ตารางด้านล่างนี้อธิบายความแตกต่างที่สำคัญบางประการระหว่างวิธีการรับรองความถูกต้องแบบ [โครงร่างสำคัญของบริการ](embed-service-principal.md) และ **ผู้ใช้หลัก**</span><span class="sxs-lookup"><span data-stu-id="6802a-173">The table below describes a few key differences between the [service principal](embed-service-principal.md) and **master user** authentication methods.</span></span>

|<span data-ttu-id="6802a-174">ข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="6802a-174">Consideration</span></span>  |<span data-ttu-id="6802a-175">โครงร่างสำคัญของบริการ</span><span class="sxs-lookup"><span data-stu-id="6802a-175">Service principal</span></span>  |<span data-ttu-id="6802a-176">ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="6802a-176">Master user</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="6802a-177">กลไก</span><span class="sxs-lookup"><span data-stu-id="6802a-177">Mechanism</span></span>     |<span data-ttu-id="6802a-178">[ออบเจ็กต์โครงร่างสำคัญของบริการ](/azure/active-directory/develop/app-objects-and-service-principals#service-principal-object)ของแอป Azure AD ของคุณช่วยให้ Azure AD สามารถรับรองความถูกต้องของแอปโซลูชันแบบฝังตัวของคุณกับ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="6802a-178">Your Azure AD app's [service principal object](/azure/active-directory/develop/app-objects-and-service-principals#service-principal-object) allows Azure AD to authenticate your embedded solution app against Power BI.</span></span>        |<span data-ttu-id="6802a-179">แอป Azure AD ของคุณใช้ข้อมูลประจำตัว (ชื่อผู้ใช้และรหัสผ่าน) ของผู้ใช้ Power BI เพื่อรับรองความถูกต้องกับ Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-179">Your Azure AD app uses the credentials (username and password) of a Power BI user, to authenticate against Power BI.</span></span>         |
|<span data-ttu-id="6802a-180">ความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="6802a-180">Security</span></span>     |<span data-ttu-id="6802a-181">*โครงร่างสำคัญของบริการ* เป็นวิธีการรับรองความถูกต้องที่แนะนำของ Azure AD</span><span class="sxs-lookup"><span data-stu-id="6802a-181">*Service principal* is the Azure AD recommended authorization method.</span></span> <span data-ttu-id="6802a-182">ถ้าคุณกำลังใช้โครงร่างสำคัญของบริการ \*คุณสามารถรับรองความถูกต้องโดยใช้ *ข้อมูลลับของแอปพลิเคชัน* หรือ *ใบรับรอง*</span><span class="sxs-lookup"><span data-stu-id="6802a-182">If you're using a service principal,\* you can authenticate using either an *application secret* or a *certificate*.</span></span></br></br><span data-ttu-id="6802a-183">บทช่วยสอนนี้อธิบายเฉพาะการใช้ *โครงร่างสำคัญของบริการ* ด้วย *ข้อมูลลับของแอปพลิเคชัน*</span><span class="sxs-lookup"><span data-stu-id="6802a-183">This tutorial only describes using *service principal* with an *application secret*.</span></span> <span data-ttu-id="6802a-184">หากต้องการฝังโดยใช้ *โครงร่างสำคัญของบริการ* และ *ใบรับรอง* โปรดดูบทความ [โครงร่างสำคัญของบริการด้วยใบรับรอง](embed-service-principal-certificate.md)</span><span class="sxs-lookup"><span data-stu-id="6802a-184">To embed using a *service principal* and a *certificate*, refer to the [service principal with a certificate](embed-service-principal-certificate.md) article.</span></span>         |<span data-ttu-id="6802a-185">วิธีการรับรองความถูกต้องนี้ไม่ได้รับการพิจารณาว่าปลอดภัยเท่ากับการใช้ *โครงร่างสำคัญของบริการ*</span><span class="sxs-lookup"><span data-stu-id="6802a-185">This authentication method is not considered as secure as using a *service principal*.</span></span> <span data-ttu-id="6802a-186">เนื่องจากคุณต้องระมัดระวังข้อมูลประจำตัว *ผู้ใช้หลัก* (ชื่อผู้ใช้และรหัสผ่าน)</span><span class="sxs-lookup"><span data-stu-id="6802a-186">This is because you have to be vigilant with the *master user* credentials (username and password).</span></span> <span data-ttu-id="6802a-187">ตัวอย่างเช่น คุณต้องไม่เปิดเผยในแอปพลิเคชันการฝังของคุณ และคุณควรเปลี่ยนรหัสผ่านบ่อย ๆ</span><span class="sxs-lookup"><span data-stu-id="6802a-187">For example, you must not expose them in your embedding application, and you should change the password frequently.</span></span>         |
|<span data-ttu-id="6802a-188">สิทธิ์ที่ได้รับมอบหมายของ Azure AD</span><span class="sxs-lookup"><span data-stu-id="6802a-188">Azure AD delegated permissions</span></span> |<span data-ttu-id="6802a-189">ไม่จำเป็นต้องมี</span><span class="sxs-lookup"><span data-stu-id="6802a-189">Not required.</span></span> |<span data-ttu-id="6802a-190">*ผู้ใช้หลัก* ของคุณหรือผู้ดูแลระบบต้องให้ความยินยอมเพื่อให้แอปของคุณเข้าถึง [สิทธิ์](/azure/active-directory/develop/v2-permissions-and-consent) Power BI REST API (หรือที่เรียกว่าขอบเขต)</span><span class="sxs-lookup"><span data-stu-id="6802a-190">Your *master user* or an administrator has to grant consent for your app to access Power BI REST API [permissions](/azure/active-directory/develop/v2-permissions-and-consent) (also known as scopes).</span></span> <span data-ttu-id="6802a-191">ตัวอย่างเช่น *Report.ReadWrite All*</span><span class="sxs-lookup"><span data-stu-id="6802a-191">For example, *Report.ReadWrite.All*.</span></span> |
|<span data-ttu-id="6802a-192">สิทธิ์การเข้าถึงบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-192">Power BI service access</span></span> |<span data-ttu-id="6802a-193">คุณไม่สามารถเข้าถึงบริการ Power BI ด้วย *โครงร่างสำคัญของบริการ*</span><span class="sxs-lookup"><span data-stu-id="6802a-193">You can't access Power BI service with a *service principal*.</span></span>|<span data-ttu-id="6802a-194">คุณสามารถเข้าถึงบริการ Power BI ด้วยข้อมูลประจำตัวของ *ผู้ใช้หลัก* ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-194">You can access Power BI service with your *master user* credentials.</span></span>|
|<span data-ttu-id="6802a-195">สิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6802a-195">License</span></span>     |<span data-ttu-id="6802a-196">ไม่จำเป็นต้องมีสิทธิ์การใช้งาน Pro</span><span class="sxs-lookup"><span data-stu-id="6802a-196">Doesn't require a Pro license.</span></span> <span data-ttu-id="6802a-197">คุณสามารถใช้เนื้อหาจากพื้นที่ทำงานใดก็ได้ที่คุณเป็นสมาชิกหรือผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="6802a-197">You can use content from any workspace that you're a member or an admin of.</span></span>         |<span data-ttu-id="6802a-198">ต้องมีสิทธิ์การใช้งาน [Power BI Pro](../../admin/service-admin-purchasing-power-bi-pro.md)</span><span class="sxs-lookup"><span data-stu-id="6802a-198">Requires a [Power BI Pro](../../admin/service-admin-purchasing-power-bi-pro.md) license.</span></span>         |

## <a name="step-2---register-an-azure-ad-application"></a><span data-ttu-id="6802a-199">ขั้นตอนที่ 2 - ลงทะเบียนแอปพลิเคชัน Azure AD</span><span class="sxs-lookup"><span data-stu-id="6802a-199">Step 2 - Register an Azure AD application</span></span>

<span data-ttu-id="6802a-200">การลงทะเบียนแอปพลิเคชันของคุณด้วย Azure AD ช่วยให้คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="6802a-200">Registering your application with Azure AD allows you to:</span></span>
> [!div class="checklist"]
>* <span data-ttu-id="6802a-201">สร้างข้อมูลประจำตัวสำหรับแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-201">Establish an identity for your app</span></span>
>* <span data-ttu-id="6802a-202">อนุญาตให้แอปของคุณเข้าถึง [Power BI REST APIs](/rest/api/power-bi/)</span><span class="sxs-lookup"><span data-stu-id="6802a-202">Let your app access the [Power BI REST APIs](/rest/api/power-bi/)</span></span>
>* <span data-ttu-id="6802a-203">ถ้าคุณกำลังใช้ *ผู้ใช้หลัก* - ให้ระบุ [สิทธิ์ Power BI REST](/azure/active-directory/develop/v2-permissions-and-consent) ของแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-203">If you're using a *master user* - Specify your app's [Power BI REST permissions](/azure/active-directory/develop/v2-permissions-and-consent)</span></span>

<span data-ttu-id="6802a-204">หากต้องการลงทะเบียนแอปพลิเคชันของคุณด้วย Azure AD ให้ทำตามคำแนะนำใน[ลงทะเบียนแอปพลิเคชันของคุณ](register-app.md)</span><span class="sxs-lookup"><span data-stu-id="6802a-204">To register your application with Azure AD, follow the instructions in [Register your application](register-app.md).</span></span>

>[!NOTE]
><span data-ttu-id="6802a-205">ก่อนที่จะลงทะเบียนแอปพลิเคชันของคุณ คุณจะต้องตัดสินใจว่าจะใช้วิธีการรับรองความถูกต้องใด *โครงร่างสำคัญของบริการ* หรือ *ผู้ใช้หลัก*</span><span class="sxs-lookup"><span data-stu-id="6802a-205">Before registering your application, you'll need to decide which authentication method to use, *service principal* or *master user*.</span></span>

## <a name="step-3---create-a-power-bi-workspace"></a><span data-ttu-id="6802a-206">ขั้นตอนที่ 3 - สร้างพื้นที่ทำงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-206">Step 3 - Create a Power BI workspace</span></span>

<span data-ttu-id="6802a-207">Power BI เก็บรายงาน แดชบอร์ด และไทล์ของคุณไว้ในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="6802a-207">Power BI keeps your reports, dashboards, and tiles in a workspace.</span></span> <span data-ttu-id="6802a-208">หากต้องการฝังรายการเหล่านี้ คุณจะต้องสร้างและอัปโหลดรายการเหล่านั้นลงในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="6802a-208">To embed these items, you'll need to create them and upload them into a workspace.</span></span>

>[!TIP]
><span data-ttu-id="6802a-209">ถ้าคุณมีพื้นที่ทำงานอยู่แล้ว คุณสามารถข้ามขั้นตอนนี้ได้เลย</span><span class="sxs-lookup"><span data-stu-id="6802a-209">If you already have a workspace, you can skip this step.</span></span>

<span data-ttu-id="6802a-210">หากต้องการสร้างพื้นที่ทำงาน ให้ทำดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-210">To create a workspace, do the following:</span></span>

1. <span data-ttu-id="6802a-211">ลงชื่อเข้าใช้ไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-211">Sign in to Power BI.</span></span>

2. <span data-ttu-id="6802a-212">เลือก **พื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="6802a-212">Select **Workspaces**.</span></span>

3. <span data-ttu-id="6802a-213">เลือก **สร้างพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="6802a-213">Select **Create a workspace**.</span></span>

4. <span data-ttu-id="6802a-214">ตั้งชื่อพื้นที่ทำงานของคุณและเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6802a-214">Name your workspace and select **Save**.</span></span>

## <a name="step-4---create-and-publish-a-power-bi-report"></a><span data-ttu-id="6802a-215">ขั้นตอนที่ 4 - สร้าง และเผยแพร่รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-215">Step 4 - Create and publish a Power BI report</span></span>

<span data-ttu-id="6802a-216">ขั้นตอนถัดไปของคุณคือการสร้างรายงานและอัปโหลดไปยังพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-216">Your next step is to create a report and upload it to your workspace.</span></span> <span data-ttu-id="6802a-217">คุณสามารถ[สร้างรายงานของคุณเอง](../../fundamentals/desktop-getting-started.md#build-reports)โดยใช้ Power BI Desktop และจากนั้น[เผยแพร่](/powerbi-docs/fundamentals/desktop-getting-started#share-your-work)รายงานดังกล่าวไปยังพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-217">You can [create your own report](../../fundamentals/desktop-getting-started.md#build-reports) using Power BI Desktop, and then [publish](/powerbi-docs/fundamentals/desktop-getting-started#share-your-work) it to your workspace.</span></span> <span data-ttu-id="6802a-218">หรือคุณสามารถอัปโหลดรายงานตัวอย่างไปยังพื้นที่ทำงานของคุณได้</span><span class="sxs-lookup"><span data-stu-id="6802a-218">Or, you can upload a sample report to your workspace.</span></span>

>[!Tip]
><span data-ttu-id="6802a-219">ถ้าคุณมีพื้นที่ทำงานที่มีรายงานอยู่แล้ว คุณสามารถข้ามขั้นตอนนี้ได้เลย</span><span class="sxs-lookup"><span data-stu-id="6802a-219">If you already have a workspace with a report, you can skip this step.</span></span>

<span data-ttu-id="6802a-220">หากต้องการดาวน์โหลดรายงานตัวอย่างและเผยแพร่ไปยังพื้นที่ทำงานของคุณ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-220">To download a sample report and publish it to your workspace, follow these steps:</span></span>

1. <span data-ttu-id="6802a-221">เปิดโฟลเดอร์[ตัวอย่าง Power BI Desktop](https://github.com/Microsoft/PowerBI-Desktop-Samples) ใน GitHub</span><span class="sxs-lookup"><span data-stu-id="6802a-221">Open the GitHub [Power BI Desktop samples](https://github.com/Microsoft/PowerBI-Desktop-Samples) folder.</span></span>

2. <span data-ttu-id="6802a-222">เลือก **โค้ด** จากนั้นเลือก **ดาวน์โหลด zip**</span><span class="sxs-lookup"><span data-stu-id="6802a-222">Select **Code** and then select **Download zip**.</span></span>

    :::image type="content" source="media/embed-sample-for-customers/download-sample-report.png" alt-text="สกรีนช็อตที่แสดงตัวเลือกการดาวน์โหลด ZIP ใน GitHub ตัวอย่าง Power BI desktop":::

3. <span data-ttu-id="6802a-224">แยก ZIP ที่ดาวน์โหลดและนำทางไปยังโฟลเดอร์ **รายงานตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="6802a-224">Extract the downloaded ZIP and navigate to the **Samples Reports** folder.</span></span>

4. <span data-ttu-id="6802a-225">เลือกรายงานที่จะฝัง และ[เผยแพร่](/powerbi-docs/fundamentals/desktop-getting-started#share-your-work)รายงานนั้นไปยังพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-225">Select a report to embed, and [publish](/powerbi-docs/fundamentals/desktop-getting-started#share-your-work) it to your workspace.</span></span>

## <a name="step-5---get-the-embedding-parameter-values"></a><span data-ttu-id="6802a-226">ขั้นตอนที่ 5 -รับค่าพารามิเตอร์การฝัง</span><span class="sxs-lookup"><span data-stu-id="6802a-226">Step 5 - Get the embedding parameter values</span></span>

<span data-ttu-id="6802a-227">หากต้องการฝังเนื้อหาของคุณ คุณจะต้องขอรับค่าพารามิเตอร์บางอย่าง</span><span class="sxs-lookup"><span data-stu-id="6802a-227">To embed your content, you'll need to obtain certain parameter values.</span></span> <span data-ttu-id="6802a-228">ตารางแสดงค่าที่ต้องการและระบุว่าสามารถใช้ได้กับวิธีการรับรองความถูกต้องแบบ *โครงร่างสำคัญของบริการ* วิธีการรับรองความถูกต้องแบบ *ผู้ใช้หลัก* หรือทั้งสองอย่าง</span><span class="sxs-lookup"><span data-stu-id="6802a-228">The table blow shows the required values, and indicates if they're applicable to the *service principal* authentication method, the *master user* authentication method, or both.</span></span>

<span data-ttu-id="6802a-229">ก่อนที่คุณจะฝังเนื้อหาของคุณ ควรตรวจสอบให้แน่ใจว่าคุณมีค่าทั้งหมดที่แสดงอยู่ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="6802a-229">Before you embed your content, make sure you have all the values listed below.</span></span> <span data-ttu-id="6802a-230">ค่าบางอย่างจะแตกต่างกันขึ้นอยู่กับวิธีการรับรองความถูกต้องที่คุณกำลังใช้</span><span class="sxs-lookup"><span data-stu-id="6802a-230">Some of the values will differ, depending on the authentication method you're using.</span></span>

|<span data-ttu-id="6802a-231">พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="6802a-231">Parameter</span></span>   |<span data-ttu-id="6802a-232">โครงร่างสำคัญของบริการ</span><span class="sxs-lookup"><span data-stu-id="6802a-232">Service principal</span></span>   |<span data-ttu-id="6802a-233">ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="6802a-233">Master user</span></span>  |
|-------------------|---|---|
|[<span data-ttu-id="6802a-234">ID ของไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="6802a-234">Client ID</span></span>](#client-id) |![นำไปใช้กับ](../../media/yes.png) |![นำไปใช้กับ](../../media/yes.png) |
|[<span data-ttu-id="6802a-237">รหัสพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="6802a-237">Workspace ID</span></span>](#workspace-id)     |![นำไปใช้กับ](../../media/yes.png) |![นำไปใช้กับ](../../media/yes.png) |
|[<span data-ttu-id="6802a-240">รหัสรายงาน</span><span class="sxs-lookup"><span data-stu-id="6802a-240">Report ID</span></span>](#report-id)           |![นำไปใช้กับ](../../media/yes.png) |![นำไปใช้กับ](../../media/yes.png) |
|[<span data-ttu-id="6802a-243">ข้อมูลลับไคลเอ็นต์</span><span class="sxs-lookup"><span data-stu-id="6802a-243">Client secret</span></span>](#client-secret) |![นำไปใช้กับ](../../media/yes.png) |![ไม่นำไปใช้](../../media/no.png) |
|[<span data-ttu-id="6802a-246">ID ผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="6802a-246">Tenant ID</span></span>](#tenant-id)                 |![นำไปใช้กับ](../../media/yes.png) |![ไม่นำไปใช้](../../media/no.png) |
|[<span data-ttu-id="6802a-249">ชื่อผู้ใช้ Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-249">Power BI username</span></span>](#power-bi-username-and-password)   |![ไม่นำไปใช้](../../media/no.png) |![นำไปใช้กับ](../../media/yes.png) |
|[<span data-ttu-id="6802a-252">รหัสผ่าน Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-252">Power BI password</span></span>](#power-bi-username-and-password)   |![ไม่นำไปใช้](../../media/no.png) |![นำไปใช้กับ](../../media/yes.png) |

### <a name="client-id"></a><span data-ttu-id="6802a-255">ID ของไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="6802a-255">Client ID</span></span>

>[!TIP]
><span data-ttu-id="6802a-256">**นำไปใช้กับ:** ![นำไปใช้กับ](../../media/yes.png)โครงร่างสำคัญของบริการ![ นำไปใช้กับ](../../media/yes.png)ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="6802a-256">**Applies to:** ![Applies to.](../../media/yes.png)Service principal ![Applies to.](../../media/yes.png)Master user</span></span>

<span data-ttu-id="6802a-257">หากต้องการรับ GUID สำหรับ ID ของไคลเอ็นต์ (หรือที่เรียกว่า *ID แอปพลิเคชัน*) ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-257">To get the client ID GUID (also know as *application ID*), follow these steps:</span></span>

1. <span data-ttu-id="6802a-258">ลงชื่อเข้าใช้ใน [Microsoft Azure](https://ms.portal.azure.com/#allservices)</span><span class="sxs-lookup"><span data-stu-id="6802a-258">Log into [Microsoft Azure](https://ms.portal.azure.com/#allservices).</span></span>

2. <span data-ttu-id="6802a-259">ค้นหา **การลงทะเบียนแอป** และเลือกลิงก์ **การลงทะเบียนแอป**</span><span class="sxs-lookup"><span data-stu-id="6802a-259">Search for **App registrations** and select the **App registrations** link.</span></span>

3. <span data-ttu-id="6802a-260">เลือกแอป Azure AD ที่คุณใช้สำหรับการฝังเนื้อหา Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-260">Select the Azure AD app your using for embedding your Power BI content.</span></span>

4. <span data-ttu-id="6802a-261">จากส่วน **ภาพรวม** ให้คัดลอก GUID สำหรับ **ID แอปพลิเคชัน (ไคลเอนต์)**</span><span class="sxs-lookup"><span data-stu-id="6802a-261">From the **Overview** section, copy the **Application (client) ID** GUID.</span></span>

### <a name="workspace-id"></a><span data-ttu-id="6802a-262">ID พื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="6802a-262">Workspace ID</span></span>

>[!TIP]
><span data-ttu-id="6802a-263">**นำไปใช้กับ:** ![นำไปใช้กับ](../../media/yes.png)โครงร่างสำคัญของบริการ![ นำไปใช้กับ](../../media/yes.png)ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="6802a-263">**Applies to:** ![Applies to.](../../media/yes.png)Service principal ![Applies to.](../../media/yes.png)Master user</span></span>

<span data-ttu-id="6802a-264">หากต้องการรับ GUID สำหรับ ID พื้นที่ทำงาน ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-264">To get the workspace ID GUID, follow these steps:</span></span>

1. <span data-ttu-id="6802a-265">ลงชื่อเข้าใช้บริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-265">Sign in to Power BI service.</span></span>

2. <span data-ttu-id="6802a-266">เปิดรายงานที่คุณต้องการฝัง</span><span class="sxs-lookup"><span data-stu-id="6802a-266">Open the report you want to embed.</span></span>

3. <span data-ttu-id="6802a-267">คัดลอก GUID จาก URL</span><span class="sxs-lookup"><span data-stu-id="6802a-267">Copy the GUID from the URL.</span></span> <span data-ttu-id="6802a-268">GUID คือตัวเลขระหว่าง **/groups/** และ **/reports/**</span><span class="sxs-lookup"><span data-stu-id="6802a-268">The GUID is the number between **/groups/** and **/reports/**.</span></span>

    :::image type="content" source="media/embed-sample-for-customers/workspace-id.png" alt-text="สกรีนช็อตที่แสดง GUID สำหรับ ID พื้นที่ทำงานใน URL ของบริการ Power BI":::

### <a name="report-id"></a><span data-ttu-id="6802a-270">รหัสรายงาน</span><span class="sxs-lookup"><span data-stu-id="6802a-270">Report ID</span></span>

>[!TIP]
><span data-ttu-id="6802a-271">**นำไปใช้กับ:** ![นำไปใช้กับ](../../media/yes.png)โครงร่างสำคัญของบริการ![ นำไปใช้กับ](../../media/yes.png)ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="6802a-271">**Applies to:** ![Applies to.](../../media/yes.png)Service principal ![Applies to.](../../media/yes.png)Master user</span></span>

1. <span data-ttu-id="6802a-272">ลงชื่อเข้าใช้บริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-272">Sign in to Power BI service.</span></span>

2. <span data-ttu-id="6802a-273">เปิดรายงานที่คุณต้องการฝัง</span><span class="sxs-lookup"><span data-stu-id="6802a-273">Open the report you want to embed.</span></span>

3. <span data-ttu-id="6802a-274">คัดลอก GUID จาก URL</span><span class="sxs-lookup"><span data-stu-id="6802a-274">Copy the GUID from the URL.</span></span> <span data-ttu-id="6802a-275">GUID คือตัวเลขระหว่าง **/reports/** และ **/ReportSection**</span><span class="sxs-lookup"><span data-stu-id="6802a-275">The GUID is the number between **/reports/** and **/ReportSection**.</span></span>

    :::image type="content" source="media/embed-sample-for-customers/report-id.png" alt-text="สกรีนช็อตที่แสดง GUID สำหรับ ID รายงานใน URL ของบริการ Power BI":::

### <a name="client-secret"></a><span data-ttu-id="6802a-277">ข้อมูลลับไคลเอ็นต์</span><span class="sxs-lookup"><span data-stu-id="6802a-277">Client secret</span></span>

>[!TIP]
><span data-ttu-id="6802a-278">**นำไปใช้กับ:** ![นำไปใช้กับ](../../media/yes.png)โครงร่างสำคัญของบริการ![ ไม่นำไปใช้กับ](../../media/no.png)ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="6802a-278">**Applies to:** ![Applies to.](../../media/yes.png)Service principal ![Does not apply to.](../../media/no.png)Master user</span></span>

<span data-ttu-id="6802a-279">หากต้องการรับข้อมูลลับไคลเอ็นต์ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-279">To get the client secret, follow these steps:</span></span>

1. <span data-ttu-id="6802a-280">ลงชื่อเข้าใช้ใน [Microsoft Azure](https://ms.portal.azure.com/#allservices)</span><span class="sxs-lookup"><span data-stu-id="6802a-280">Log into [Microsoft Azure](https://ms.portal.azure.com/#allservices).</span></span>

2. <span data-ttu-id="6802a-281">ค้นหา **การลงทะเบียนแอป** และเลือกลิงก์ **การลงทะเบียนแอป**</span><span class="sxs-lookup"><span data-stu-id="6802a-281">Search for **App registrations** and select the **App registrations** link.</span></span>

3. <span data-ttu-id="6802a-282">เลือกแอป Azure AD ที่คุณใช้สำหรับการฝังเนื้อหา Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-282">Select the Azure AD app your using for embedding your Power BI content.</span></span>

4. <span data-ttu-id="6802a-283">เลือก **ใบรับรองและข้อมูลลับ** ภายใต้ **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="6802a-283">Under **Manage**, select **Certificates & secrets**.</span></span>

5. <span data-ttu-id="6802a-284">เลือก **ข้อมูลลับไคลเอ็นต์ใหม่** ภายใต้ **ข้อมูลลับไคลเอ็นต์**</span><span class="sxs-lookup"><span data-stu-id="6802a-284">Under **Client secrets**, select **New client secret**.</span></span>

6. <span data-ttu-id="6802a-285">ในหน้าต่างป๊อปอัป **เพิ่มข้อมูลลับไคลเอ็นต์** ให้คำอธิบายสำหรับข้อมูลลับของแอปพลิเคชันของคุณ เลือกเวลาที่ข้อมูลลับของแอปพลิเคชันจะหมดอายุและเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="6802a-285">In the **Add a client secret** pop-up window, provide a description for your application secret, select when the application secret expires, and select **Add**.</span></span>

7. <span data-ttu-id="6802a-286">คัดลอกสตริงในคอลัมน์ **ค่า** ของข้อมูลลับของแอปพลิเคชันที่สร้างขึ้นใหม่จากส่วน **ข้อมูลลับไคลเอ็นต์**</span><span class="sxs-lookup"><span data-stu-id="6802a-286">From the **Client secrets** section, copy the string in the **Value** column of the newly created application secret.</span></span> <span data-ttu-id="6802a-287">ค่าข้อมูลลับไคลเอ็นต์คือ *ID ไคลเอ็นต์* ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-287">The client secret value is your *client ID*.</span></span>

### <a name="tenant-id"></a><span data-ttu-id="6802a-288">ID ผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="6802a-288">Tenant ID</span></span>

>[!TIP]
><span data-ttu-id="6802a-289">**นำไปใช้กับ:** ![นำไปใช้กับ](../../media/yes.png)โครงร่างสำคัญของบริการ![ ไม่นำไปใช้กับ](../../media/no.png)ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="6802a-289">**Applies to:** ![Applies to.](../../media/yes.png)Service principal ![Does not apply to.](../../media/no.png)Master user</span></span>

<span data-ttu-id="6802a-290">หากต้องการรับ GUID สำหรับ ID ผู้เช่า ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-290">To get the tenant ID GUID, follow these steps:</span></span>

1. <span data-ttu-id="6802a-291">ลงชื่อเข้าใช้ใน [Microsoft Azure](https://ms.portal.azure.com/#allservices)</span><span class="sxs-lookup"><span data-stu-id="6802a-291">Log into [Microsoft Azure](https://ms.portal.azure.com/#allservices).</span></span>

2. <span data-ttu-id="6802a-292">ค้นหา **การลงทะเบียนแอป** และเลือกลิงก์ **การลงทะเบียนแอป**</span><span class="sxs-lookup"><span data-stu-id="6802a-292">Search for **App registrations** and select the **App registrations** link.</span></span>

3. <span data-ttu-id="6802a-293">เลือกแอป Azure AD ที่คุณใช้สำหรับการฝังเนื้อหา Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-293">Select the Azure AD app your using for embedding your Power BI content.</span></span>

4. <span data-ttu-id="6802a-294">จากส่วน **ภาพรวม** ให้คัดลอก GUID สำหรับ **ID ของ Directory (ผู้เช่า)**</span><span class="sxs-lookup"><span data-stu-id="6802a-294">From the **Overview** section, copy the **Directory (tenant) ID** GUID.</span></span>

### <a name="power-bi-username-and-password"></a><span data-ttu-id="6802a-295">ชื่อผู้ใช้และรหัสผ่าน Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-295">Power BI username and password</span></span>

>[!TIP]
><span data-ttu-id="6802a-296">**นำไปใช้กับ:** ![ไม่นำไปใช้กับ](../../media/no.png)โครงร่างสำคัญของบริการ![ นำไปใช้กับ](../../media/yes.png)ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="6802a-296">**Applies to:** ![Does not apply to.](../../media/no.png)Service principal ![Applies to.](../../media/yes.png)Master user</span></span>

<span data-ttu-id="6802a-297">รับ *ชื่อผู้ใช้* และ *รหัสผ่าน* ของผู้ใช้ Power BI ที่คุณใช้เป็น **ผู้ใช้หลัก** ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-297">Obtain the *username* and *password* of the Power BI user you're using as your **master user**.</span></span> <span data-ttu-id="6802a-298">ซึ่งเป็นผู้ใช้เดียวกับที่คุณใช้ในการสร้างพื้นที่ทำงานและอัปโหลดรายงานในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-298">This is the same user you used to create a workspace and upload a report to, in Power BI service.</span></span>

## <a name="step-6---service-principal-api-access"></a><span data-ttu-id="6802a-299">ขั้นตอนที่ 6 - สิทธิ์การเข้าถึง API ของโครงร่างสำคัญของบริการ</span><span class="sxs-lookup"><span data-stu-id="6802a-299">Step 6 - Service principal API access</span></span>

>[!TIP]
><span data-ttu-id="6802a-300">**นำไปใช้กับ:** ![นำไปใช้กับ](../../media/yes.png)โครงร่างสำคัญของบริการ![ ไม่นำไปใช้กับ](../../media/no.png)ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="6802a-300">**Applies to:** ![Applies to.](../../media/yes.png)Service principal ![Does not apply to.](../../media/no.png)Master user</span></span>
>
><span data-ttu-id="6802a-301">ขั้นตอนนี้จะเกี่ยวข้องก็ต่อเมื่อคุณใช้วิธีการรับรองความถูกต้องแบบ *โครงร่างสำคัญของบริการ*</span><span class="sxs-lookup"><span data-stu-id="6802a-301">This step is only relevant if you're using the *service principal* authentication method.</span></span> <span data-ttu-id="6802a-302">หากคุณกำลังใช้ *ผู้ใช้หลัก* ให้ข้ามขั้นตอนนี้และดำเนินการต่อด้วย [ขั้นตอนที่ 7 - เปิดใช้งานการเข้าถึงพื้นที่ทำงาน](#step-7---enable-workspace-access)</span><span class="sxs-lookup"><span data-stu-id="6802a-302">If you're using a *master user*, skip this step and continue with [Step 7 - Enable workspace access](#step-7---enable-workspace-access).</span></span>

<span data-ttu-id="6802a-303">เพื่อให้แอป Azure AD สามารถเข้าถึงเนื้อหา Power BI และ API ได้ ผู้ดูแลระบบ Power BI จำเป็นต้องเปิดใช้งานการเข้าถึงบริการหลักในพอร์ทัลผู้ดูแลระบบของ Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-303">For an Azure AD app to be able to access the Power BI content and APIs, a Power BI admin needs to enable service principal access in the Power BI admin portal.</span></span> <span data-ttu-id="6802a-304">หากคุณไม่ใช่ผู้ดูแลระบบของผู้เช่าของคุณ ให้แจ้งผู้ดูแลระบบของผู้เช่าเพื่อเปิดใช้งาน *การตั้งค่าผู้เช่า* ให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-304">If you're not the admin of your tenant, get the tenant's admin to enable the *Tenant settings* for you.</span></span>
        
1. <span data-ttu-id="6802a-305">ใน *บริการ Power BI* ให้เลือก **การตั้งค่า** > **การตั้งค่า** > **พอร์ทัลผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="6802a-305">In *Power BI service*, select **Settings** > **Settings** > **Admin portal**.</span></span>
        
    :::image type="content" source="media/embed-sample-for-customers/admin-settings.png" alt-text="สกรีนช็อตที่แสดงตัวเลือกเมนูการตั้งค่าผู้ดูแลระบบในเมนูการตั้งค่าบริการ Power BI":::
        
2. <span data-ttu-id="6802a-307">เลือก **การตั้งค่าผู้เช่า** จากนั้นเลื่อนลงไปที่ส่วน **การตั้งค่าสำหรับนักพัฒนาซอฟต์แวร์**</span><span class="sxs-lookup"><span data-stu-id="6802a-307">Select **Tenant settings** and then scroll down to the **Developer settings** section.</span></span>
        
3. <span data-ttu-id="6802a-308">ขยาย **อนุญาตให้โครงร่างสำคัญของบริการใช้ Power BI APIs** และเปิดใช้งานตัวเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="6802a-308">Expand **Allow service principals to use Power BI APIs**, and enable this option.</span></span>
        
    :::image type="content" source="media/embed-sample-for-customers/developer-settings.png" alt-text="สกรีนช็อตที่แสดงวิธีเปิดใช้งานตัวเลือกการตั้งค่าของนักพัฒนาในตัวเลือกเมนูการตั้งค่าผู้เช่าในบริการ Power BI":::
        
>[!NOTE]
><span data-ttu-id="6802a-310">เมื่อใช้ *โครงร่างสำคัญของบริการ* ขอแนะนำให้จำกัดการเข้าถึงการตั้งค่าผู้เช่าโดยใช้ *กลุ่มความปลอดภัย*</span><span class="sxs-lookup"><span data-stu-id="6802a-310">When using a *service principal*, it's recommended to limit its access to the tenant settings using a *security group*.</span></span> <span data-ttu-id="6802a-311">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะนี้ ให้ดูส่วนเหล่านี้ในบทความ[โครงร่างสำคัญของบริการ](embed-service-principal.md):</span><span class="sxs-lookup"><span data-stu-id="6802a-311">To learn more about this feature, see these sections in the [service principal](embed-service-principal.md) article:</span></span>
> * [<span data-ttu-id="6802a-312">สร้างกลุ่มความปลอดภัย Azure AD</span><span class="sxs-lookup"><span data-stu-id="6802a-312">Create an Azure AD security group</span></span>](embed-service-principal.md#step-2---create-an-azure-ad-security-group)
>* [<span data-ttu-id="6802a-313">เปิดใช้งานการตั้งค่าการจัดการบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-313">Enable the Power BI service admin settings</span></span>](embed-service-principal.md#step-3---enable-the-power-bi-service-admin-settings)

## <a name="step-7---enable-workspace-access"></a><span data-ttu-id="6802a-314">ขั้นตอนที่ 7 - เปิดใช้งานการเข้าถึงพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="6802a-314">Step 7 - Enable workspace access</span></span>

<span data-ttu-id="6802a-315">หากต้องการเปิดใช้งานการเข้าถึงแอป Azure AD ของคุณ เช่น รายงาน แดชบอร์ด และชุดข้อมูลในบริการ Power BI ให้เพิ่ม *โครงร่างสำคัญของบริการ* หรือ *ผู้ใช้หลัก* ในฐานะที่เป็น *สมาชิก* หรือ *ผู้ดูแลระบบ* ในพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-315">To enable your Azure AD app access artifacts such as reports, dashboards and datasets in the Power BI service, add the *service principal* or *master user*, as a *member* or *admin* to your workspace.</span></span>

1. <span data-ttu-id="6802a-316">ลงชื่อเข้าใช้บริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-316">Sign in to Power BI service.</span></span>

2. <span data-ttu-id="6802a-317">เลื่อนไปยังพื้นที่ทำงานที่คุณต้องการเปิดใช้งานการเข้าถึง และจากเมนู **เพิ่มเติม** เลือก **การเข้าถึงพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="6802a-317">Scroll to the workspace you want to enable access for, and from the **More** menu, select **Workspace access**.</span></span>

    :::image type="content" source="media/embed-service-principal/workspace-access.png" alt-text="สกรีนช็อตแสดงปุ่มการเข้าถึงพื้นที่ทำงานในเมนูเพิ่มเติมของพื้นที่ทำงาน Power BI":::

3. <span data-ttu-id="6802a-319">ในบานหน้าต่าง **การเข้าถึง** ซึ่งขึ้นอยู่กับวิธีการรับรองความถูกต้องที่คุณใช้ ให้คัดลอก *โครงร่างสำคัญของบริการ* หรือ *ผู้ใช้หลัก* ไปยังกล่องข้อความ **ป้อนที่อยู่อีเมล**</span><span class="sxs-lookup"><span data-stu-id="6802a-319">In the **Access** pane, depending on which authentication method you're using, copy the *service principal* or *master user* to the **Enter email address** text box.</span></span>

    >[!NOTE]
    ><span data-ttu-id="6802a-320">ถ้าคุณกำลังใช้ *โครงร่างสำคัญของบริการ* ชื่อนี้เป็นชื่อที่คุณตั้งให้แอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-320">If you're using a *service principal*, its name is the name you gave your Azure AD app.</span></span>

5. <span data-ttu-id="6802a-321">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="6802a-321">Select **Add**.</span></span>

## <a name="step-8---embed-your-content"></a><span data-ttu-id="6802a-322">ขั้นตอนที่ 8 - ฝังเนื้อหาของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-322">Step 8 - Embed your content</span></span>

<span data-ttu-id="6802a-323">แอปพลิเคชันตัวอย่าง Power BI embedded ช่วยให้คุณสามารถสร้างแอป Power BI *การฝังตัวสำหรับลูกค้าของคุณ*</span><span class="sxs-lookup"><span data-stu-id="6802a-323">The Power BI embedded sample application allows you to create an *embed for your customers* Power BI app.</span></span>

<span data-ttu-id="6802a-324">ทำตามขั้นตอนเหล่านี้เพื่อปรับเปลี่ยนแอปพลิเคชันตัวอย่าง *การฝังตัวสำหรับลูกค้าของคุณ* เพื่อฝังรายงาน Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-324">Follow these steps to modify the *embed for your customers* sample application, to embed your Power BI report.</span></span>  

1. <span data-ttu-id="6802a-325">เปิดโฟลเดอร์[ตัวอย่างสำหรับนักพัฒนา Power BI](https://github.com/microsoft/PowerBI-Developer-Samples)</span><span class="sxs-lookup"><span data-stu-id="6802a-325">Open the [Power BI developer samples](https://github.com/microsoft/PowerBI-Developer-Samples) folder.</span></span>

2. <span data-ttu-id="6802a-326">เลือก **โค้ด** จากนั้นเลือก **ดาวน์โหลด zip**</span><span class="sxs-lookup"><span data-stu-id="6802a-326">Select **Code** and then select **Download zip**.</span></span>

    :::image type="content" source="media/embed-sample-for-customers/developer-samples.png" alt-text="สกรีนช็อตที่แสดงตัวเลือกการดาวน์โหลด ZIP ใน GitHub ตัวอย่างสำหรับนักพัฒนา Power BI":::

3. <span data-ttu-id="6802a-328">แตกไฟล์ ZIP ที่ดาวน์โหลดมาและไปที่โฟลเดอร์ **PowerBI-Developer-Samples-master**</span><span class="sxs-lookup"><span data-stu-id="6802a-328">Extract the downloaded ZIP and navigate to the **PowerBI-Developer-Samples-master** folder.</span></span>

4. <span data-ttu-id="6802a-329">เปิดหนึ่งในโฟลเดอร์เหล่านี้ ทั้งนี้ขึ้นอยู่กับภาษาที่คุณต้องการให้แอปพลิเคชันของคุณใช้:</span><span class="sxs-lookup"><span data-stu-id="6802a-329">Depending on the language you want your application to use, open one of these folders:</span></span>

* <span data-ttu-id="6802a-330">.NET Core</span><span class="sxs-lookup"><span data-stu-id="6802a-330">.NET Core</span></span>
* <span data-ttu-id="6802a-331">เฟรมเวอร์ค .NET</span><span class="sxs-lookup"><span data-stu-id="6802a-331">.NET Framework</span></span>
* <span data-ttu-id="6802a-332">Java</span><span class="sxs-lookup"><span data-stu-id="6802a-332">Java</span></span>
* <span data-ttu-id="6802a-333">Node JS</span><span class="sxs-lookup"><span data-stu-id="6802a-333">Node JS</span></span>
* <span data-ttu-id="6802a-334">Python</span><span class="sxs-lookup"><span data-stu-id="6802a-334">Python</span></span>
    >[!NOTE]
    ><span data-ttu-id="6802a-335">แอปพลิเคชันตัวอย่าง *การฝังตัวสำหรับลูกค้าของคุณ* สนับสนุนเฉพาะภาษาที่ระบุไว้ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="6802a-335">The *embed for your customers* sample applications only support the languages listed above.</span></span> <span data-ttu-id="6802a-336">แอปพลิเคชันตัวอย่าง *React TS* รองรับเฉพาะโซลูชัน *[การฝังสำหรับองค์กรของคุณ](embed-sample-for-your-organization.md)* เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6802a-336">The *React TS* sample application only supports the *[embed for your organization](embed-sample-for-your-organization.md)* solution.</span></span>

5. <span data-ttu-id="6802a-337">เปิดโฟลเดอร์ **การฝังตัวสำหรับลูกค้าของคุณ**</span><span class="sxs-lookup"><span data-stu-id="6802a-337">Open the **Embed for your customers** folder.</span></span>

# <a name="net-core"></a>[<span data-ttu-id="6802a-338">.NET Core</span><span class="sxs-lookup"><span data-stu-id="6802a-338">.NET Core</span></span>](#tab/net-core)

6. <span data-ttu-id="6802a-339">เปิด *แอปตัวอย่างการฝังตัวสำหรับลูกค้าของคุณ* โดยใช้วิธีใดวิธีหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-339">Open the *embed for your customers sample app* using one of these methods:</span></span>

    * <span data-ttu-id="6802a-340">หากคุณกำลังใช้ [Visual Studio](https://visualstudio.microsoft.com/) ให้เปิดไฟล์ **AppOwnsData.sln**</span><span class="sxs-lookup"><span data-stu-id="6802a-340">If you're using [Visual Studio](https://visualstudio.microsoft.com/), open the **AppOwnsData.sln** file.</span></span>

    * <span data-ttu-id="6802a-341">หากคุณกำลังใช้ [Visual Studio Code](https://code.visualstudio.com/) ให้เปิดโฟลเดอร์ **App Owns Data**</span><span class="sxs-lookup"><span data-stu-id="6802a-341">If you're using [Visual Studio Code](https://code.visualstudio.com/), open the **App Owns Data** folder.</span></span>

7. <span data-ttu-id="6802a-342">เปิด **appsettings.json**</span><span class="sxs-lookup"><span data-stu-id="6802a-342">Open **appsettings.json**.</span></span>

8. <span data-ttu-id="6802a-343">ให้กรอกค่าพารามิเตอร์ต่อไปนี้ ทั้งนี้ขึ้นอยู่กับวิธีการรับรองความถูกต้องของคุณ:</span><span class="sxs-lookup"><span data-stu-id="6802a-343">Depending on your authentication method, fill in the following parameter values:</span></span>

    |<span data-ttu-id="6802a-344">พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="6802a-344">Parameter</span></span>            |<span data-ttu-id="6802a-345">โครงร่างสำคัญของบริการ</span><span class="sxs-lookup"><span data-stu-id="6802a-345">Service principal</span></span>  |<span data-ttu-id="6802a-346">ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="6802a-346">Master user</span></span>  |
    |---------------------|---------|---------|
    |`AuthenticationMode` |<span data-ttu-id="6802a-347">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6802a-347">ServicePrincipal</span></span>         |<span data-ttu-id="6802a-348">MasterUser</span><span class="sxs-lookup"><span data-stu-id="6802a-348">MasterUser</span></span>         |
    |`ClientId`           |<span data-ttu-id="6802a-349">[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-349">Your Azure AD app [client ID](#client-id)</span></span>         |<span data-ttu-id="6802a-350">[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-350">Your Azure AD app [client ID](#client-id)</span></span>         |
    |`TenantId`           |<span data-ttu-id="6802a-351">[ID ผู้เช่า](#tenant-id)ของแอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-351">Your Azure AD [tenant ID](#tenant-id)</span></span>         |<span data-ttu-id="6802a-352">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-352">N/A</span></span>         |
    |`PbiUsername`        |<span data-ttu-id="6802a-353">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-353">N/A</span></span>         |<span data-ttu-id="6802a-354">ชื่อผู้ใช้ของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)</span><span class="sxs-lookup"><span data-stu-id="6802a-354">Your *master user* username, see [Power BI username and password](#power-bi-username-and-password)</span></span>         |
    |`PbiPassword`        |<span data-ttu-id="6802a-355">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-355">N/A</span></span>         |<span data-ttu-id="6802a-356">รหัสผ่านของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)</span><span class="sxs-lookup"><span data-stu-id="6802a-356">Your *master user* password, see [Power BI username and password](#power-bi-username-and-password)</span></span>         |
    |`ClientSecret`       |<span data-ttu-id="6802a-357">[ข้อมูลลับไคลเอ็นต์](#client-secret)ของ Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-357">Your Azure AD [client secret](#client-secret)</span></span>         |<span data-ttu-id="6802a-358">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-358">N/A</span></span>         |
    |`WorkspaceId`        |<span data-ttu-id="6802a-359">ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-359">The ID of the workspace with your embedded report, see [Workspace ID](#workspace-id)</span></span>          |<span data-ttu-id="6802a-360">ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-360">The ID of the workspace with your embedded report, see [Workspace ID](#workspace-id)</span></span>         |
    |`ReportId`           |<span data-ttu-id="6802a-361">ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-361">The ID of the report you're embedding, see [Report ID](#report-id)</span></span>            |<span data-ttu-id="6802a-362">ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-362">The ID of the report you're embedding, see [Report ID](#report-id)</span></span>         |

9. <span data-ttu-id="6802a-363">เรียกใช้โครงการโดยการเลือกตัวเลือกที่เหมาะสม:</span><span class="sxs-lookup"><span data-stu-id="6802a-363">Run the project by selecting the appropriate option:</span></span>

    * <span data-ttu-id="6802a-364">หากคุณกำลังใช้ **Visual Studio** ให้เลือก **IIS Express** (เล่น)</span><span class="sxs-lookup"><span data-stu-id="6802a-364">If you're using **Visual Studio**, select **IIS Express** (play).</span></span>

    * <span data-ttu-id="6802a-365">หากคุณกำลังใช้ **Visual Studio Code** ให้เลือก **เรียกใช้> เริ่มต้นการดีบัก**</span><span class="sxs-lookup"><span data-stu-id="6802a-365">If you're using **Visual Studio Code**, select **Run > Start Debugging**.</span></span>

# <a name="net-framework"></a>[<span data-ttu-id="6802a-366">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="6802a-366">.NET Framework</span></span>](#tab/net-framework)

6. <span data-ttu-id="6802a-367">กำลังใช้ [Visual Studio](https://visualstudio.microsoft.com/) ให้เปิดไฟล์ **AppOwnsData.sln**</span><span class="sxs-lookup"><span data-stu-id="6802a-367">Using [Visual Studio](https://visualstudio.microsoft.com/), open the **AppOwnsData.sln** file.</span></span>

7. <span data-ttu-id="6802a-368">เปิด **Web.config**</span><span class="sxs-lookup"><span data-stu-id="6802a-368">Open **Web.config**.</span></span>

8. <span data-ttu-id="6802a-369">ให้กรอกค่าพารามิเตอร์ต่อไปนี้ ทั้งนี้ขึ้นอยู่กับวิธีการรับรองความถูกต้องของคุณ:</span><span class="sxs-lookup"><span data-stu-id="6802a-369">Depending on your authentication method, fill in the following parameter values:</span></span>

    |<span data-ttu-id="6802a-370">พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="6802a-370">Parameter</span></span>            |<span data-ttu-id="6802a-371">โครงร่างสำคัญของบริการ</span><span class="sxs-lookup"><span data-stu-id="6802a-371">Service principal</span></span>  |<span data-ttu-id="6802a-372">ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="6802a-372">Master user</span></span>  |
    |---------------------|---------|---------|
    |`authenticationType` |<span data-ttu-id="6802a-373">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6802a-373">ServicePrincipal</span></span>         |<span data-ttu-id="6802a-374">MasterUser</span><span class="sxs-lookup"><span data-stu-id="6802a-374">MasterUser</span></span>         |
    |`applicationId`           |<span data-ttu-id="6802a-375">[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-375">Your Azure AD app [client ID](#client-id)</span></span>         |<span data-ttu-id="6802a-376">[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-376">Your Azure AD app [client ID](#client-id)</span></span>         |
    |`workspaceId`        |<span data-ttu-id="6802a-377">ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-377">The ID of the workspace with your embedded report, see [Workspace ID](#workspace-id)</span></span>          |<span data-ttu-id="6802a-378">ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-378">The ID of the workspace with your embedded report, see [Workspace ID](#workspace-id)</span></span>         |
    |`reportId`           |<span data-ttu-id="6802a-379">ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-379">The ID of the report you're embedding, see [Report ID](#report-id)</span></span>            |<span data-ttu-id="6802a-380">ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-380">The ID of the report you're embedding, see [Report ID](#report-id)</span></span>         |
    |`pbiUsername`        |<span data-ttu-id="6802a-381">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-381">N/A</span></span>         |<span data-ttu-id="6802a-382">ชื่อผู้ใช้ของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)</span><span class="sxs-lookup"><span data-stu-id="6802a-382">Your *master user* username, see [Power BI username and password](#power-bi-username-and-password)</span></span>         |
    |`pbiPassword`        |<span data-ttu-id="6802a-383">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-383">N/A</span></span>         |<span data-ttu-id="6802a-384">รหัสผ่านของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)</span><span class="sxs-lookup"><span data-stu-id="6802a-384">Your *master user* password, see [Power BI username and password](#power-bi-username-and-password)</span></span>         |
    |`applicationSecret`       |<span data-ttu-id="6802a-385">[ข้อมูลลับไคลเอ็นต์](#client-secret)ของ Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-385">Your Azure AD [client secret](#client-secret)</span></span>         |<span data-ttu-id="6802a-386">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-386">N/A</span></span>         |
    |`tenant`           |<span data-ttu-id="6802a-387">[ID ผู้เช่า](#tenant-id)ของแอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-387">Your Azure AD [tenant ID](#tenant-id)</span></span>         |<span data-ttu-id="6802a-388">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-388">N/A</span></span>         |

9. <span data-ttu-id="6802a-389">เรียกใช้โครงการโดยการเลือก **IIS Express** (เล่น)</span><span class="sxs-lookup"><span data-stu-id="6802a-389">Run the project by selecting **IIS Express** (play).</span></span>

>[!NOTE]
><span data-ttu-id="6802a-390">ถ้าคุณไม่เห็นรายงานที่ฝังตัวเมื่อเรียกใช้แอปตัวอย่าง ให้รีเฟรชแพคเกจ Power BI โดยทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-390">If you're not seeing the embedded report when running the sample app, refresh the Power BI packages by following these steps:</span></span>
>1. <span data-ttu-id="6802a-391">คลิกขวาบนชื่อโครงการ (AppOwnesData) และเลือก **จัดการแพคเกจ NuGet**</span><span class="sxs-lookup"><span data-stu-id="6802a-391">Right-click on the project name (AppOwnesData), and select **Manage NuGet packages**.</span></span>
>2. <span data-ttu-id="6802a-392">ค้นหา **Power BI JavaScript** และจากนั้นติดตั้งแพคเกจใหม่</span><span class="sxs-lookup"><span data-stu-id="6802a-392">Search for **Power BI JavaScript** and then reinstall the package.</span></span>
>
><span data-ttu-id="6802a-393">สำหรับข้อมูลเพิ่มเติม โปรดดู[วิธีการติดตั้งและปรับปรุงแพคเกจ](/nuget/consume-packages/reinstalling-and-updating-packages)</span><span class="sxs-lookup"><span data-stu-id="6802a-393">For more information, see [How to reinstall and update packages](/nuget/consume-packages/reinstalling-and-updating-packages).</span></span>

# <a name="java"></a>[<span data-ttu-id="6802a-394">Java</span><span class="sxs-lookup"><span data-stu-id="6802a-394">Java</span></span>](#tab/java)

6. <span data-ttu-id="6802a-395">เปิด **Eclipse** และทำตามคำแนะนำที่อธิบายไว้ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="6802a-395">Open **Eclipse** and follow the instructions described below.</span></span>

    >[!NOTE]
    ><span data-ttu-id="6802a-396">คำแนะนำสำหรับ *แอปตัวอย่างการฝังตัวสำหรับลูกค้าของคุณ* ด้วยภาษา Java โปรดดูที่ [Eclipse IDE สำหรับ Java EE Developers](https://www.eclipse.org/downloads/packages/) (รุ่นสำหรับองค์กร)</span><span class="sxs-lookup"><span data-stu-id="6802a-396">The instructions for the Java *embed for your customers sample app*, refer to [Eclipse IDE for Java EE Developers](https://www.eclipse.org/downloads/packages/) (enterprise edition).</span></span> <span data-ttu-id="6802a-397">หากคุณกำลังใช้แอปพลิเคชันอื่น คุณจะต้องตั้งค่าด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="6802a-397">If you're using a different application, you'll have to set it up yourself.</span></span>

7. <span data-ttu-id="6802a-398">เพิ่มเซิร์ฟเวอร์ Tomcat ไปยัง Eclipse:</span><span class="sxs-lookup"><span data-stu-id="6802a-398">Add the Tomcat server to Eclipse:</span></span>

    <span data-ttu-id="6802a-399">a.</span><span class="sxs-lookup"><span data-stu-id="6802a-399">a.</span></span> <span data-ttu-id="6802a-400">เลือก **หน้าต่าง** > **แสดงมุมมอง** > **เซิร์ฟเวอร์**</span><span class="sxs-lookup"><span data-stu-id="6802a-400">Select **Window** > **Show View** > **Servers**.</span></span>

    <span data-ttu-id="6802a-401">b.</span><span class="sxs-lookup"><span data-stu-id="6802a-401">b.</span></span> <span data-ttu-id="6802a-402">ในแท็บเซิร์ฟเวอร์ ให้เลือก **ไม่มีเซิร์ฟเวอร์ที่พร้อมใช้งาน คลิกที่ลิงก์นี้เพื่อสร้างเซิร์ฟเวอร์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="6802a-402">In the servers tab, select **No servers are available. Click this link to create new server**.</span></span>

    <span data-ttu-id="6802a-403">c.</span><span class="sxs-lookup"><span data-stu-id="6802a-403">c.</span></span> <span data-ttu-id="6802a-404">ในหน้าต่าง **กำหนดเซิร์ฟเวอร์ใหม่** ขยาย **Apache** และเลือกเซิร์ฟเวอร์ Tomcat ที่คุณใช้งานบนเครื่องของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-404">In the **Define a New Server** window, expand **Apache** and select the Tomcat server you're running on your machine.</span></span> <span data-ttu-id="6802a-405">ตัวอย่างเช่น *เซิร์ฟเวอร์ Tomcat v9.0*</span><span class="sxs-lookup"><span data-stu-id="6802a-405">For example, *Tomcat v9.0 Server*.</span></span>

    <span data-ttu-id="6802a-406">d.</span><span class="sxs-lookup"><span data-stu-id="6802a-406">d.</span></span> <span data-ttu-id="6802a-407">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="6802a-407">Select **Next**.</span></span>

    <span data-ttu-id="6802a-408">e.</span><span class="sxs-lookup"><span data-stu-id="6802a-408">e.</span></span> <span data-ttu-id="6802a-409">ในหน้าต่าง **เซิร์ฟเวอร์ Tomcat** เลือก **เรียกดู** และไปที่โฟลเดอร์ที่มีเซิร์ฟเวอร์ Tomcat</span><span class="sxs-lookup"><span data-stu-id="6802a-409">In the **Tomcat Server** window, select **Browse** and navigate to the folder that contains the Tomcat server.</span></span>

    <span data-ttu-id="6802a-410">f.</span><span class="sxs-lookup"><span data-stu-id="6802a-410">f.</span></span> <span data-ttu-id="6802a-411">ในหน้าต่าง **เซิร์ฟเวอร์ Tomcat** ให้เลือก **JREs ที่ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="6802a-411">In the **Tomcat Server** window, select **Installed JREs**.</span></span>

    <span data-ttu-id="6802a-412">เช่น</span><span class="sxs-lookup"><span data-stu-id="6802a-412">g.</span></span> <span data-ttu-id="6802a-413">ในหน้าต่าง **JREs ที่ติดตั้ง** ให้เลือก *jre* ที่มีอยู่ แล้วเลือก **นำไปใช้และปิด**</span><span class="sxs-lookup"><span data-stu-id="6802a-413">In the **Installed JREs** window, select the available *jre*, and select **Apply and Close**.</span></span>

    <span data-ttu-id="6802a-414">h.</span><span class="sxs-lookup"><span data-stu-id="6802a-414">h.</span></span> <span data-ttu-id="6802a-415">ในหน้าต่าง **เซิร์ฟเวอร์ Tomcat** ให้เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="6802a-415">In the **Tomcat Server** window, select **Finish**.</span></span> <span data-ttu-id="6802a-416">คุณจะเห็นเซิร์ฟเวอร์ Tomcat ในแท็บ *เซิร์ฟเวอร์*</span><span class="sxs-lookup"><span data-stu-id="6802a-416">You'll be able to see the Tomcat server in the *Servers* tab.</span></span>

8. <span data-ttu-id="6802a-417">เปิดโครงการใน Eclipse:</span><span class="sxs-lookup"><span data-stu-id="6802a-417">Open the project in Eclipse:</span></span>

    >[!IMPORTANT]
    ><span data-ttu-id="6802a-418">Eclipse อาจประสบปัญหาหากชื่อพาธของคุณยาวเกินไป</span><span class="sxs-lookup"><span data-stu-id="6802a-418">Eclipse may run into trouble if your path name is too long.</span></span> <span data-ttu-id="6802a-419">เพื่อหลีกเลี่ยงปัญหานี้ ให้ตรวจสอบว่าโฟลเดอร์ของแอปตัวอย่างของคุณไม่ได้ซ้อนกันมากเกินไปในโครงสร้างโฟลเดอร์ของเครื่องของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-419">To avoid this issue, verify that your sample app's folder is not nested too deeply in your machine's folder structure.</span></span>

    <span data-ttu-id="6802a-420">a.</span><span class="sxs-lookup"><span data-stu-id="6802a-420">a.</span></span> <span data-ttu-id="6802a-421">เลือก **ไฟล์** จากนั้นเลือก **เปิดโครงการจากระบบไฟล์**</span><span class="sxs-lookup"><span data-stu-id="6802a-421">Select **File** and then select **Open Projects from File System**.</span></span>

    <span data-ttu-id="6802a-422">b.</span><span class="sxs-lookup"><span data-stu-id="6802a-422">b.</span></span> <span data-ttu-id="6802a-423">ในหน้าต่าง **นำเข้าโครงการจากระบบไฟล์หรือที่เก็บถาวร** เลือก **Directory** และเปิดโฟลเดอร์ **AppOwnsData**</span><span class="sxs-lookup"><span data-stu-id="6802a-423">In the **Import Projects form File System or Archive** window, select **Directory** and open the **AppOwnsData** folder.</span></span>

    <span data-ttu-id="6802a-424">c.</span><span class="sxs-lookup"><span data-stu-id="6802a-424">c.</span></span> <span data-ttu-id="6802a-425">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="6802a-425">Select **Finish**.</span></span>

9. <span data-ttu-id="6802a-426">เพิ่มเซิร์ฟเวอร์ Tomcat ไปยังโครงการ:</span><span class="sxs-lookup"><span data-stu-id="6802a-426">Add the Tomcat server to the project:</span></span>

    <span data-ttu-id="6802a-427">a.</span><span class="sxs-lookup"><span data-stu-id="6802a-427">a.</span></span> <span data-ttu-id="6802a-428">ในบานหน้าต่าง **ตัวต้นหาแพคเกจ** คลิกขวาที่ **AppOwnsData** และเลือก **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="6802a-428">In the **Package Explorer** pane, right-click **AppOwnsData**, and select **Properties**.</span></span>

    <span data-ttu-id="6802a-429">b.</span><span class="sxs-lookup"><span data-stu-id="6802a-429">b.</span></span> <span data-ttu-id="6802a-430">ในหน้าต่าง **คุณสมบัติสำหรับ AppOwnesData** ให้เลือก **รันไทม์ที่กำหนดเป้าหมาย** จากนั้นเลือก **Apache Tomcat**</span><span class="sxs-lookup"><span data-stu-id="6802a-430">In the **Properties for AppOwnesData** window, select **Targeted Runtimes** and then select **Apache Tomcat**.</span></span> <span data-ttu-id="6802a-431">การเลือกนี้จะรวมถึงเวอร์ชันของ *Apache Tomcat* ที่คุณใช้อยู่ ตัวอย่างเช่น *Apache Tomact v9.0*</span><span class="sxs-lookup"><span data-stu-id="6802a-431">This selection will include the version of *Apache Tomcat* you're using, for example *Apache Tomact v9.0*.</span></span>

    <span data-ttu-id="6802a-432">c.</span><span class="sxs-lookup"><span data-stu-id="6802a-432">c.</span></span> <span data-ttu-id="6802a-433">เลือก **นำไปใช้และปิด**</span><span class="sxs-lookup"><span data-stu-id="6802a-433">Select  **Apply and Close**.</span></span>

10. <span data-ttu-id="6802a-434">ระบุพารามิเตอร์ที่จำเป็น:</span><span class="sxs-lookup"><span data-stu-id="6802a-434">Fill in the required parameters</span></span>

    <span data-ttu-id="6802a-435">a.</span><span class="sxs-lookup"><span data-stu-id="6802a-435">a.</span></span> <span data-ttu-id="6802a-436">ใน **ตัวต้นหาแพคเกจ** ขยายโครงการ **AppOwnsData**</span><span class="sxs-lookup"><span data-stu-id="6802a-436">In the **Package explorer**, expand the **AppOwnsData** project.</span></span>

    <span data-ttu-id="6802a-437">b.</span><span class="sxs-lookup"><span data-stu-id="6802a-437">b.</span></span> <span data-ttu-id="6802a-438">ขยาย **Java Resources**</span><span class="sxs-lookup"><span data-stu-id="6802a-438">Expand **Java Resources**.</span></span>

    <span data-ttu-id="6802a-439">c.</span><span class="sxs-lookup"><span data-stu-id="6802a-439">c.</span></span> <span data-ttu-id="6802a-440">ขยาย **src**</span><span class="sxs-lookup"><span data-stu-id="6802a-440">Expand **src**.</span></span>

    <span data-ttu-id="6802a-441">d.</span><span class="sxs-lookup"><span data-stu-id="6802a-441">d.</span></span> <span data-ttu-id="6802a-442">ขยาย **com.embedsample.appoensdata.config**</span><span class="sxs-lookup"><span data-stu-id="6802a-442">Expand **com.embedsample.appoensdata.config**.</span></span>

    <span data-ttu-id="6802a-443">e.</span><span class="sxs-lookup"><span data-stu-id="6802a-443">e.</span></span> <span data-ttu-id="6802a-444">เปิด **Config.java**</span><span class="sxs-lookup"><span data-stu-id="6802a-444">Open **Config.java**.</span></span>

    <span data-ttu-id="6802a-445">f.</span><span class="sxs-lookup"><span data-stu-id="6802a-445">f.</span></span> <span data-ttu-id="6802a-446">ให้กรอกค่าพารามิเตอร์ต่อไปนี้ ทั้งนี้ขึ้นอยู่กับวิธีการรับรองความถูกต้องของคุณ:</span><span class="sxs-lookup"><span data-stu-id="6802a-446">Depending on your authentication method, fill in the following parameter values:</span></span>

    |<span data-ttu-id="6802a-447">พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="6802a-447">Parameter</span></span>            |<span data-ttu-id="6802a-448">โครงร่างสำคัญของบริการ</span><span class="sxs-lookup"><span data-stu-id="6802a-448">Service principal</span></span>  |<span data-ttu-id="6802a-449">ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="6802a-449">Master user</span></span>  |
    |---------------------|---------|---------|
    |`authenticationType` |<span data-ttu-id="6802a-450">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6802a-450">ServicePrincipal</span></span>         |<span data-ttu-id="6802a-451">MasterUser</span><span class="sxs-lookup"><span data-stu-id="6802a-451">MasterUser</span></span>         |
    |`workspaceId`        |<span data-ttu-id="6802a-452">ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-452">The ID of the workspace with your embedded report, see [Workspace ID](#workspace-id)</span></span>          |<span data-ttu-id="6802a-453">ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-453">The ID of the workspace with your embedded report, see [Workspace ID](#workspace-id)</span></span>         |
    |`reportId`           |<span data-ttu-id="6802a-454">ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-454">The ID of the report you're embedding, see [Report ID](#report-id)</span></span>            |<span data-ttu-id="6802a-455">ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-455">The ID of the report you're embedding, see [Report ID](#report-id)</span></span>         | 
    |`clientId`           |<span data-ttu-id="6802a-456">[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-456">Your Azure AD app [client ID](#client-id)</span></span>         |<span data-ttu-id="6802a-457">[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-457">Your Azure AD app [client ID](#client-id)</span></span>         |
    |`pbiUsername`        |<span data-ttu-id="6802a-458">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-458">N/A</span></span>         |<span data-ttu-id="6802a-459">ชื่อผู้ใช้ของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)</span><span class="sxs-lookup"><span data-stu-id="6802a-459">Your *master user* username, see [Power BI username and password](#power-bi-username-and-password)</span></span>         |
    |`pbiPassword`        |<span data-ttu-id="6802a-460">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-460">N/A</span></span>         |<span data-ttu-id="6802a-461">รหัสผ่านของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)</span><span class="sxs-lookup"><span data-stu-id="6802a-461">Your *master user* password, see [Power BI username and password](#power-bi-username-and-password)</span></span>         |
    |`tenantId`           |<span data-ttu-id="6802a-462">[ID ผู้เช่า](#tenant-id)ของแอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-462">Your Azure AD [tenant ID](#tenant-id)</span></span>         |<span data-ttu-id="6802a-463">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-463">N/A</span></span>         |
    |`appSecret`       |<span data-ttu-id="6802a-464">[ข้อมูลลับไคลเอ็นต์](#client-secret)ของ Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-464">Your Azure AD [client secret](#client-secret)</span></span>         |<span data-ttu-id="6802a-465">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-465">N/A</span></span>         |

11. <span data-ttu-id="6802a-466">เรียกใช้โครงการ</span><span class="sxs-lookup"><span data-stu-id="6802a-466">Run the project</span></span>

    <span data-ttu-id="6802a-467">a.</span><span class="sxs-lookup"><span data-stu-id="6802a-467">a.</span></span> <span data-ttu-id="6802a-468">ใน **ตัวต้นหาแพคเกจ** คลิกขวา **AppOwnesData**</span><span class="sxs-lookup"><span data-stu-id="6802a-468">In the **Package Explorer**, right-click **AppOwnesData**.</span></span>

    <span data-ttu-id="6802a-469">b.</span><span class="sxs-lookup"><span data-stu-id="6802a-469">b.</span></span> <span data-ttu-id="6802a-470">เลือก **เรียกใช้เป็น**  > **เรียกใช้บนเซิร์ฟเวอร์**</span><span class="sxs-lookup"><span data-stu-id="6802a-470">Select **Run As**  > **Run on Server**.</span></span>

    <span data-ttu-id="6802a-471">c.</span><span class="sxs-lookup"><span data-stu-id="6802a-471">c.</span></span> <span data-ttu-id="6802a-472">ในหน้าต่าง **เรียกใช้บนเซิร์ฟเวอร์** ให้เลือก **เลือกเซิร์ฟเวอร์ที่มีอยู่** และเลือกเซิร์ฟเวอร์ *Tomcat*</span><span class="sxs-lookup"><span data-stu-id="6802a-472">In the **Run on Server** window, select **Choose an existing server** and select the *Tomcat* server.</span></span>

    <span data-ttu-id="6802a-473">d.</span><span class="sxs-lookup"><span data-stu-id="6802a-473">d.</span></span> <span data-ttu-id="6802a-474">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="6802a-474">Select **Finish**.</span></span>

# <a name="node-js"></a>[<span data-ttu-id="6802a-475">Node JS</span><span class="sxs-lookup"><span data-stu-id="6802a-475">Node JS</span></span>](#tab/node-js)

6. <span data-ttu-id="6802a-476">เปิดโฟลเดอร์ **แอปเป็นเจ้าของข้อมูล** โดยใช้ IDE ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="6802a-476">Open the **App Owns Data** folder using your preferred IDE.</span></span> <span data-ttu-id="6802a-477">เราขอแนะนำให้ใช้หนึ่งในรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-477">We recommend using one of the following:</span></span>

    * [<span data-ttu-id="6802a-478">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6802a-478">Visual Studio</span></span>](https://visualstudio.microsoft.com/)

    * [<span data-ttu-id="6802a-479">รหัส Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6802a-479">Visual Studio Code</span></span>](https://code.visualstudio.com/)

7. <span data-ttu-id="6802a-480">เปิดเทอร์มินัลและติดตั้งการขึ้นต่อกันที่จำเป็นโดยดำเนินการ: `npm install`</span><span class="sxs-lookup"><span data-stu-id="6802a-480">Open a terminal and install the required dependencies by executing: `npm install`.</span></span>

8. <span data-ttu-id="6802a-481">ขยายโฟลเดอร์ **กำหนดค่า** และเปิด **config.json**</span><span class="sxs-lookup"><span data-stu-id="6802a-481">Expand the **Config** folder and open **config.json**.</span></span>

9. <span data-ttu-id="6802a-482">ให้กรอกค่าพารามิเตอร์ต่อไปนี้ ทั้งนี้ขึ้นอยู่กับวิธีการรับรองความถูกต้องของคุณ:</span><span class="sxs-lookup"><span data-stu-id="6802a-482">Depending on your authentication method, fill in the following parameter values:</span></span>

    |<span data-ttu-id="6802a-483">พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="6802a-483">Parameter</span></span>            |<span data-ttu-id="6802a-484">โครงร่างสำคัญของบริการ</span><span class="sxs-lookup"><span data-stu-id="6802a-484">Service principal</span></span>  |<span data-ttu-id="6802a-485">ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="6802a-485">Master user</span></span>  |
    |---------------------|---------|---------|
    |`authenticationMode` |<span data-ttu-id="6802a-486">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6802a-486">ServicePrincipal</span></span>         |<span data-ttu-id="6802a-487">MasterUser</span><span class="sxs-lookup"><span data-stu-id="6802a-487">MasterUser</span></span>         |
    |`clientId`           |<span data-ttu-id="6802a-488">[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-488">Your Azure AD app [client ID](#client-id)</span></span>         |<span data-ttu-id="6802a-489">[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-489">Your Azure AD app [client ID](#client-id)</span></span>         |
    |`workspaceId`        |<span data-ttu-id="6802a-490">ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-490">The ID of the workspace with your embedded report, see [Workspace ID](#workspace-id)</span></span>          |<span data-ttu-id="6802a-491">ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-491">The ID of the workspace with your embedded report, see [Workspace ID](#workspace-id)</span></span>         |
    |`reportId`           |<span data-ttu-id="6802a-492">ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-492">The ID of the report you're embedding, see [Report ID](#report-id)</span></span>            |<span data-ttu-id="6802a-493">ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-493">The ID of the report you're embedding, see [Report ID](#report-id)</span></span>         |
    |`pbiUsername`        |<span data-ttu-id="6802a-494">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-494">N/A</span></span>         |<span data-ttu-id="6802a-495">ชื่อผู้ใช้ของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)</span><span class="sxs-lookup"><span data-stu-id="6802a-495">Your *master user* username, see [Power BI username and password](#power-bi-username-and-password)</span></span>         |
    |`pbiPassword`        |<span data-ttu-id="6802a-496">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-496">N/A</span></span>         |<span data-ttu-id="6802a-497">รหัสผ่านของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)</span><span class="sxs-lookup"><span data-stu-id="6802a-497">Your *master user* password, see [Power BI username and password](#power-bi-username-and-password)</span></span>         |
    |`clientSecret`       |<span data-ttu-id="6802a-498">[ข้อมูลลับไคลเอ็นต์](#client-secret)ของ Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-498">Your Azure AD [client secret](#client-secret)</span></span>         |<span data-ttu-id="6802a-499">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-499">N/A</span></span>         |
    |`tenantId`           |<span data-ttu-id="6802a-500">[ID ผู้เช่า](#tenant-id)ของแอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-500">Your Azure AD [tenant ID](#tenant-id)</span></span>         |<span data-ttu-id="6802a-501">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-501">N/A</span></span>         |

10. <span data-ttu-id="6802a-502">เรียกใช้โครงการโดยทำดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-502">Run the project by doing the following:</span></span>

    <span data-ttu-id="6802a-503">a.</span><span class="sxs-lookup"><span data-stu-id="6802a-503">a.</span></span> <span data-ttu-id="6802a-504">ในเทอร์มินัล IDE ให้ดำเนินการ `npm start`</span><span class="sxs-lookup"><span data-stu-id="6802a-504">In the IDE terminal, execute `npm start`.</span></span>

    <span data-ttu-id="6802a-505">b.</span><span class="sxs-lookup"><span data-stu-id="6802a-505">b.</span></span> <span data-ttu-id="6802a-506">เปิดแท็บใหม่ในเบราว์เซอร์ของคุณและนำทางไปยัง `http://localhost:5300`</span><span class="sxs-lookup"><span data-stu-id="6802a-506">Open a new tab in your browser and navigate to `http://localhost:5300`.</span></span>

# <a name="python"></a>[<span data-ttu-id="6802a-507">Python</span><span class="sxs-lookup"><span data-stu-id="6802a-507">Python</span></span>](#tab/python)

6. <span data-ttu-id="6802a-508">เปิด **PowerShell** หรือ **Command Prompt**</span><span class="sxs-lookup"><span data-stu-id="6802a-508">Open **PowerShell** or **Command Prompt**.</span></span>

7. <span data-ttu-id="6802a-509">ตรวจสอบว่าคุณอยู่ในโฟลเดอร์ **Python** > **การฝังสำหรับลูกค้าของคุณ** และไฟล์ **requirements.txt** อยู่ในโฟลเดอร์และเรียกใช้ `pip3 install -r requirements.txt`</span><span class="sxs-lookup"><span data-stu-id="6802a-509">Verify that you're in the **Python** > **Embed for your customers** folder, and that the file **requirements.txt** is in the folder, and run `pip3 install -r requirements.txt`.</span></span>

8. <span data-ttu-id="6802a-510">เปิดโฟลเดอร์ **แอปเป็นเจ้าของข้อมูล** โดยใช้ IDE ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="6802a-510">Open the **App Owns Data** folder using your preferred IDE.</span></span> <span data-ttu-id="6802a-511">เราขอแนะนำให้ใช้หนึ่งในรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-511">We recommend using one of the following:</span></span>

    * [<span data-ttu-id="6802a-512">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6802a-512">Visual Studio</span></span>](https://visualstudio.microsoft.com/)

    * [<span data-ttu-id="6802a-513">รหัส Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6802a-513">Visual Studio Code</span></span>](https://code.visualstudio.com/)

9. <span data-ttu-id="6802a-514">เปิด **config.py**</span><span class="sxs-lookup"><span data-stu-id="6802a-514">Open **config.py**.</span></span>

10. <span data-ttu-id="6802a-515">ให้กรอกค่าพารามิเตอร์ต่อไปนี้ ทั้งนี้ขึ้นอยู่กับวิธีการรับรองความถูกต้องของคุณ:</span><span class="sxs-lookup"><span data-stu-id="6802a-515">Depending on your authentication method, fill in the following parameter values:</span></span>

    |<span data-ttu-id="6802a-516">พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="6802a-516">Parameter</span></span>            |<span data-ttu-id="6802a-517">โครงร่างสำคัญของบริการ</span><span class="sxs-lookup"><span data-stu-id="6802a-517">Service principal</span></span>  |<span data-ttu-id="6802a-518">ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="6802a-518">Master user</span></span>  |
    |---------------------|---------|---------|
    |`AUTHENTICATION_MODE` |<span data-ttu-id="6802a-519">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6802a-519">ServicePrincipal</span></span>         |<span data-ttu-id="6802a-520">MasterUser</span><span class="sxs-lookup"><span data-stu-id="6802a-520">MasterUser</span></span>         |
    |`WORKSPACE_ID`        |<span data-ttu-id="6802a-521">ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-521">The ID of the workspace with your embedded report, see [Workspace ID](#workspace-id)</span></span>          |<span data-ttu-id="6802a-522">ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-522">The ID of the workspace with your embedded report, see [Workspace ID](#workspace-id)</span></span>         |
    |`REPORT_ID`           |<span data-ttu-id="6802a-523">ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-523">The ID of the report you're embedding, see [Report ID](#report-id)</span></span>            |<span data-ttu-id="6802a-524">ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)</span><span class="sxs-lookup"><span data-stu-id="6802a-524">The ID of the report you're embedding, see [Report ID](#report-id)</span></span>         |
    |`TENANT_ID`           |<span data-ttu-id="6802a-525">[ID ผู้เช่า](#tenant-id)ของแอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-525">Your Azure AD [tenant ID](#tenant-id)</span></span>         |<span data-ttu-id="6802a-526">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-526">N/A</span></span>         |
    |`CLIENT_ID`           |<span data-ttu-id="6802a-527">[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-527">Your Azure AD app [client ID](#client-id)</span></span>         |<span data-ttu-id="6802a-528">[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-528">Your Azure AD app [client ID](#client-id)</span></span>         |
    |`CLIENT_SECRET`       |<span data-ttu-id="6802a-529">[ข้อมูลลับไคลเอ็นต์](#client-secret)ของ Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-529">Your Azure AD [client secret](#client-secret)</span></span>         |<span data-ttu-id="6802a-530">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-530">N/A</span></span>         |
    |`POWER_BI_USER`        |<span data-ttu-id="6802a-531">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-531">N/A</span></span>         |<span data-ttu-id="6802a-532">ชื่อผู้ใช้ของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)</span><span class="sxs-lookup"><span data-stu-id="6802a-532">Your *master user* username, see [Power BI username and password](#power-bi-username-and-password)</span></span>         |
    |`POWER_BI_PASS`        |<span data-ttu-id="6802a-533">N/A</span><span class="sxs-lookup"><span data-stu-id="6802a-533">N/A</span></span>         |<span data-ttu-id="6802a-534">รหัสผ่านของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)</span><span class="sxs-lookup"><span data-stu-id="6802a-534">Your *master user* password, see [Power BI username and password](#power-bi-username-and-password)</span></span>         |

11. <span data-ttu-id="6802a-535">บันทึกไฟล์</span><span class="sxs-lookup"><span data-stu-id="6802a-535">Save the file.</span></span>

12. <span data-ttu-id="6802a-536">เรียกใช้โครงการโดยทำดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6802a-536">Run the project by doing the following:</span></span>

    <span data-ttu-id="6802a-537">a.</span><span class="sxs-lookup"><span data-stu-id="6802a-537">a.</span></span> <span data-ttu-id="6802a-538">ใน **PowerShell** หรือ **Command Prompt** ให้ไปที่โฟลเดอร์ **Python**  > **การฝังสำหรับลูกค้าของคุณ** > **AppOwnesData** และดำเนินการ `flask run`</span><span class="sxs-lookup"><span data-stu-id="6802a-538">In **PowerShell** or **Command Prompt**, navigate to the **Python** > **Embed for your customers** > **AppOwnesData** folder, and execute `flask run`.</span></span>

    <span data-ttu-id="6802a-539">b.</span><span class="sxs-lookup"><span data-stu-id="6802a-539">b.</span></span> <span data-ttu-id="6802a-540">เปิดแท็บใหม่ในเบราว์เซอร์ของคุณและนำทางไปยัง `http://localhost:5300`</span><span class="sxs-lookup"><span data-stu-id="6802a-540">Open a new tab in your browser and navigate to `http://localhost:5300`.</span></span>

---

## <a name="developing-your-application"></a><span data-ttu-id="6802a-541">การพัฒนาแอปพลิเคชันของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-541">Developing your application</span></span>

<span data-ttu-id="6802a-542">หลังจากกำหนดค่าและเรียกใช้แอปพลิเคชันตัวอย่าง *การฝังตัวสำหรับลูกค้าของคุณ* คุณสามารถเริ่มต้นการพัฒนาแอปพลิเคชันของคุณเองได้</span><span class="sxs-lookup"><span data-stu-id="6802a-542">After configuring and running the *embed for your customers* sample application, you can start developing your own application.</span></span>

<span data-ttu-id="6802a-543">เมื่อคุณพร้อมแล้ว ให้ตรวจสอบข้อกำหนด[การย้ายไปยังการผลิต](move-to-production.md)</span><span class="sxs-lookup"><span data-stu-id="6802a-543">When you're ready, review the [move to production](move-to-production.md) requirements.</span></span> <span data-ttu-id="6802a-544">นอกจากนี้ คุณจะต้องมี[ความจุ](embedded-capacity.md) และควรอ่านบทความ[การวางแผนความจุ](embedded-capacity-planning.md)เพื่อกำหนดว่า SKU ใดที่เหมาะสมกับความต้องการของคุณมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="6802a-544">You'll also need a [capacity](embedded-capacity.md), and should review the [capacity planning](embedded-capacity-planning.md) article to establish which SKU best suits your needs.</span></span>


## <a name="next-steps"></a><span data-ttu-id="6802a-545">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="6802a-545">Next steps</span></span>

> [!div class="nextstepaction"]
>[<span data-ttu-id="6802a-546">ย้ายไปยังการผลิต</span><span class="sxs-lookup"><span data-stu-id="6802a-546">Move to production</span></span>](move-to-production.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="6802a-547">ฝังตัวสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-547">Embed for your organization</span></span>](embed-sample-for-your-organization.md)

> [!div class="nextstepaction"]
>[<span data-ttu-id="6802a-548">รายงานที่มีการแบ่งหน้าแบบฝังตัวสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-548">Embed paginated reports for your customers</span></span>](embed-paginated-reports-customers.md)

> [!div class="nextstepaction"]
>[<span data-ttu-id="6802a-549">รายงานกิจกรรมแบบฝังสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="6802a-549">Embed paginated reports for your organization</span></span>](embed-paginated-reports-organization.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="6802a-550">ถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="6802a-550">Ask the Power BI Community</span></span>](https://community.powerbi.com/)