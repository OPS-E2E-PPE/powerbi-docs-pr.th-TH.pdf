---
title: สร้างแอปแม่แบบใน Power BI
description: วิธีการสร้างแอปแม่แบบใน Power BI ที่คุณสามารถแจกจ่ายให้กับลูกค้าทุกคน Power BI
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: how-to
ms.date: 12/14/2020
ms.openlocfilehash: cfd9302c9c64760298eb78be10affad8be510a65
ms.sourcegitcommit: 46cf62d9bb33ac7b7eae7910fbba6756f626c65f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/15/2020
ms.locfileid: "97491770"
---
# <a name="create-a-template-app-in-power-bi"></a><span data-ttu-id="383d2-103">สร้างแอปแม่แบบใน Power BI</span><span class="sxs-lookup"><span data-stu-id="383d2-103">Create a template app in Power BI</span></span>

<span data-ttu-id="383d2-104">*แอปเทมเพลต Power BI* เปิดให้คู่ค้า Power BI สร้างแอป Power BI ด้วยโค้ดเพียงเล็กน้อยหรือไม่มีเลย แล้วนำไปปรับใช้กับลูกค้า Power BI ทุกท่าน</span><span class="sxs-lookup"><span data-stu-id="383d2-104">Power BI *template apps* enable Power BI partners to build Power BI apps with little or no coding, and deploy them to any Power BI customer.</span></span>  <span data-ttu-id="383d2-105">บทความนี้ประกอบด้วยคำแนะนำทีละขั้นตอนเพื่อสร้างแอปเทมเพลต Power BI</span><span class="sxs-lookup"><span data-stu-id="383d2-105">This article contains step-by-step instructions for creating a Power BI template app.</span></span>

<span data-ttu-id="383d2-106">หากคุณสามารถสร้างรายงาน Power BI และแดชบอร์ดได้ คุณย่อมสามารถเป็น *ผู้สร้างแอปเทมเพลต* แล้วทำการสร้างรวมถึงทำแพคเกจเนื้อหาเชิงวิเคราะห์ลงใน *แอป* ได้</span><span class="sxs-lookup"><span data-stu-id="383d2-106">If you can create Power BI reports and dashboards, you can become a *template app builder* and build and package analytical content into an *app*.</span></span> <span data-ttu-id="383d2-107">จากนั้นคุณสามารถปรับใช้แอปของคุณกับผู้เช่า Power BI รายอื่นผ่านแพลตฟอร์มที่พร้อมใช้งาน เช่น AppSource หรือบริการเว็บของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="383d2-107">You can then deploy your app to other Power BI tenants through any available platform, such as AppSource or your own web service.</span></span> <span data-ttu-id="383d2-108">ถ้าหากคุณกําลังกระจายแอปเทมเพลตของคุณผ่านบริการเว็บของคุณเอง คุณสามารถ[ทําให้ส่วนหนึ่งของกระบวนการติดตั้งเป็นไปโดยอัตโนมัติ](../developer/template-apps/template-apps-auto-install.md)เพื่อให้สิ่งต่าง ๆ ง่ายขึ้นสําหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="383d2-108">If you're distributing your template app through your own web service, you can even [automate part of the installation process](../developer/template-apps/template-apps-auto-install.md) to make things easier for your customers.</span></span>

<span data-ttu-id="383d2-109">ผู้ดูแลระบบ Power BI กำกับและควบคุมว่าใครในองค์กรของพวกเขาสามารถสร้างแอปแม่แบบ และใครสามารถติดตั้งแอปดังกล่าวได้บ้าง</span><span class="sxs-lookup"><span data-stu-id="383d2-109">Power BI admins govern and control who in their organization can create template apps, and who can install them.</span></span> <span data-ttu-id="383d2-110">ผู้ใช้เหล่านั้นที่ได้รับอนุญาตสามารถติดตั้งแอปแม่แบบ จาก นั้นปรับเปลี่ยน และแจกจ่ายให้กับผู้ใช้ Power BI ในองค์กรของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="383d2-110">Those users who are authorized can install your template app, then modify it and distribute it to the Power BI consumers in their organization.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="383d2-111">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="383d2-111">Prerequisites</span></span>

<span data-ttu-id="383d2-112">นี่คือข้อกำหนดสำหรับการสร้างแอปแม่แบบ:</span><span class="sxs-lookup"><span data-stu-id="383d2-112">Here are the requirements for building a template app:</span></span>  

- <span data-ttu-id="383d2-113">[ใบอนุญาต Power BI pro ](../fundamentals/service-self-service-signup-for-power-bi.md)</span><span class="sxs-lookup"><span data-stu-id="383d2-113">A [Power BI pro license](../fundamentals/service-self-service-signup-for-power-bi.md)</span></span>
- <span data-ttu-id="383d2-114">แอ[ติดตั้ง Power BI Desktop](../fundamentals/desktop-get-the-desktop.md) (ไม่บังคับ)</span><span class="sxs-lookup"><span data-stu-id="383d2-114">An [installation of Power BI Desktop](../fundamentals/desktop-get-the-desktop.md) (optional)</span></span>
- <span data-ttu-id="383d2-115">ความชำนาญกับ[แนวคิดพื้นฐานของ Power BI](../fundamentals/service-basic-concepts.md)</span><span class="sxs-lookup"><span data-stu-id="383d2-115">Familiarity with the [basic concepts of Power BI](../fundamentals/service-basic-concepts.md)</span></span>
- <span data-ttu-id="383d2-116">สิทธิ์ในการแชร์แอปแม่แบบ (สำหรับข้อมูลเพิ่มเติม ให้ดทีู่พอร์ทัลผู้ดูแลระบบ [Power BI, การตั้งค่าแอปแม่แบบ](../admin/service-admin-portal.md#template-apps-settings)</span><span class="sxs-lookup"><span data-stu-id="383d2-116">Permissions to share a template app publicly (for more information, see Power BI [admin portal, Template app settings](../admin/service-admin-portal.md#template-apps-settings)</span></span>

## <a name="create-the-template-workspace"></a><span data-ttu-id="383d2-117">สร้างพื้นที่ทำงานของแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="383d2-117">Create the template workspace</span></span>

<span data-ttu-id="383d2-118">เมื่อต้องสร้างแอปแม่แบบที่คุณสามารถแจกจ่ายให้กับผู้เช่า Power BI อื่น ๆ คุณต้องสร้างแอปในพื้นที่ใดพื้นที่หนึ่งของพื้นที่ทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="383d2-118">To create a template app you can distribute to other Power BI tenants, you need to create it in one of the new workspaces.</span></span>

1. <span data-ttu-id="383d2-119">ในการบริการของ Power BI ให้เลือก **พื้นที่ทำงาน** > **สร้างพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="383d2-119">In the Power BI service, select **Workspaces** > **Create a workspace**.</span></span>

    ![สร้างพื้นที่ทำงาน](media/service-template-apps-create/power-bi-new-workspace.png)

2. <span data-ttu-id="383d2-121">ใน **สร้างพื้นที่ทำงาน** ให้ป้อนชื่อ คำอธิบาย (ไม่บังคับ), และภาพโลโก้ (ไม่บังคับ) สำหรับพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="383d2-121">In **Create a workspace**, enter a name, description (optional), and logo image (optional) for your workspace.</span></span>

    ![เผยแพร่พื้นที่ทำงานใหม่](media/service-template-apps-create/power-bi-upgrade-new.png)

4. <span data-ttu-id="383d2-123">ขยายหัวข้อ **ขั้นสูง** แล้วเลือก **พัฒนาแอปเทมเพลต**</span><span class="sxs-lookup"><span data-stu-id="383d2-123">Expand the **Advanced** section and select **Develop a template app**.</span></span>

    ![พัฒนาแอปแม่แบบ](media/service-template-apps-create/power-bi-template-app-develop.png)

5. <span data-ttu-id="383d2-125">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="383d2-125">Select **Save**.</span></span>
>[!NOTE]
><span data-ttu-id="383d2-126">คุณต้องมีสิทธิ์จากผู้ดูแลระบบ Power BI เพื่อเลื่อนระดับแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="383d2-126">You need permissions from your Power BI admin to promote template apps.</span></span>

## <a name="add-content-to-the-template-app-workspace"></a><span data-ttu-id="383d2-127">เพิ่มเนื้อหาลงในพื้นที่ทำงานของแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="383d2-127">Add content to the template app workspace</span></span>

<span data-ttu-id="383d2-128">ขั้นตอนต่อไปของคุณคือการเพิ่มเนื้อหาลงในพื้นที่ทำงาน เช่นเดียวกับพื้นที่ทำงานของ Power BI ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="383d2-128">As with a regular Power BI workspace, your next step is add content to the workspace.</span></span>  

- <span data-ttu-id="383d2-129">[สร้างเนื้อหา Power BI ](index.yml)ในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="383d2-129">[Create your Power BI content](index.yml) in your workspace.</span></span>

<span data-ttu-id="383d2-130">ถ้าคุณกำลังใช้พารามิเตอร์ใน Power Query ให้ตรวจสอบให้มั่นใจว่าได้กำหนดชนิดของ้พารามิเตอร์ไว้ดีแล้ว (เช่น ข้อความ)</span><span class="sxs-lookup"><span data-stu-id="383d2-130">If you're using parameters in Power Query, make sure they have well-defined types (for example, Text).</span></span> <span data-ttu-id="383d2-131">ชนิดใด ๆ และไบนารีไม่รองรับ</span><span class="sxs-lookup"><span data-stu-id="383d2-131">The types Any and Binary aren't supported.</span></span>

<span data-ttu-id="383d2-132">[เคล็ดลับสำหรับการเขียนแอปแม่แบบใน Power BI](service-template-apps-tips.md) มีคำแนะนำเพื่อพิจารณาเมื่อสร้างรายงานและแดชบอร์ดสำหรับแอปแม่แบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="383d2-132">[Tips for authoring template apps in Power BI](service-template-apps-tips.md) has suggestions to consider when creating reports and dashboards for your template app.</span></span>

## <a name="define-the-properties-of-the-template-app"></a><span data-ttu-id="383d2-133">กำหนดคุณสมบัติของแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="383d2-133">Define the properties of the template app</span></span>

<span data-ttu-id="383d2-134">หลังจากที่คุณมีเนื้อหาในพื้นที่ทำงานของคุณ คุณก็พร้อมที่จะจัดแพคเกจในแอปแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="383d2-134">Now that you have content in your workspace, you're ready to package it in a template app.</span></span> <span data-ttu-id="383d2-135">ขั้นตอนแรกคือการ สร้างแอแม่แบบทดสอบ เข้าถึงได้เท่านั้นจากภายในองค์กรของคุณในผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="383d2-135">The first step is to create a test template app, accessible only from within your organization on your tenant.</span></span>

1. <span data-ttu-id="383d2-136">ในพื้นที่ทำงานแอปแม่แบบ เลือก **สร้างแอป**</span><span class="sxs-lookup"><span data-stu-id="383d2-136">In the template app workspace, select **Create app**.</span></span>

    ![สร้างแอป](media/service-template-apps-create/power-bi-create-app.png)

    <span data-ttu-id="383d2-138">คุณกรอกตัวเลือกการสร้างเพิ่มเติมสำหรับแอปเทมเพลตในแท็บหกแท็บที่จุดนี้:</span><span class="sxs-lookup"><span data-stu-id="383d2-138">Here, you fill in additional building options for your template app, in six tabs:</span></span>

    <span data-ttu-id="383d2-139">**การกำหนดตราสินค้า**</span><span class="sxs-lookup"><span data-stu-id="383d2-139">**Branding**</span></span>

    ![การกำหนดตราสินค้า](media/service-template-apps-create/power-bi-create-branding.png)
    - <span data-ttu-id="383d2-141">ชื่อแอป</span><span class="sxs-lookup"><span data-stu-id="383d2-141">App name</span></span>
    - <span data-ttu-id="383d2-142">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="383d2-142">Description</span></span>
    - <span data-ttu-id="383d2-143">เว็บไซต์การสนับสนุน (ลิงก์จะแสดงใต้ข้อมูลแอปหลังจากแจกจ่ายแอปเทมเพลตเป็นแอปองค์กรซ้ำ)</span><span class="sxs-lookup"><span data-stu-id="383d2-143">Support site (link is presented under app info after redistributing template app as org app)</span></span>
    - <span data-ttu-id="383d2-144">โลโก้แอป (ขีดจำกัดขนาดไฟล์ 45K อัตราส่วนกว้างยาว 1:1, รูปแบบ .png .jpg .jpeg)</span><span class="sxs-lookup"><span data-stu-id="383d2-144">App logo (45K file size limit, 1:1 aspect ratio, .png .jpg .jpeg formats)</span></span>
    - <span data-ttu-id="383d2-145">สีธีมของแอป</span><span class="sxs-lookup"><span data-stu-id="383d2-145">App theme color</span></span>

    <span data-ttu-id="383d2-146">**การสืบค้นเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="383d2-146">**Navigation**</span></span>

    <span data-ttu-id="383d2-147">เปิดใช้งาน **ระบบจัดทำส่วนการสืบค้นใหม่** โดยคุณสามารถกำหนดรายละเอียดหน้าต่างนำทางของแอป (ดูรายละเอียดในหัวข้อ [ออกแบบรูปแบบการสืบค้น](../collaborate-share/service-create-distribute-apps.md#design-the-navigation-experience) ในบทความนี้)</span><span class="sxs-lookup"><span data-stu-id="383d2-147">Activate the **New navigation builder**, where you can define the nav pane of the app (See [Design the navigation experience](../collaborate-share/service-create-distribute-apps.md#design-the-navigation-experience) in this article for details).</span></span>

   ![ตั้งค่าหน้าเริ่มต้นของแอป](media/service-template-apps-create/power-bi-install-app-content.png)
    
    <span data-ttu-id="383d2-149">**หน้าเริ่มต้นของแอป:** หากคุณตัดสินใจที่จะไม่ใช้ตัวสร้างการนำทาง คุณสามารถเลือกหน้าเชื่อมโยงของแอปดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="383d2-149">**App landing page:** If you decide to opt out of the navigation builder, you have the option to select the app landing page.</span></span> <span data-ttu-id="383d2-150">กำหนดรายงานหรือแดชบอร์ดเป็น เพจเริ่มต้นของแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="383d2-150">Define a report or dashboard to be the landing page of your app.</span></span> <span data-ttu-id="383d2-151">ใช้หน้าเชื่อมโยงเพื่อจะทำให้เกิดความน่าสนใจมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="383d2-151">Use a landing page that gives the right impression.</span></span>

    <span data-ttu-id="383d2-152">**ตัวควบคุม**</span><span class="sxs-lookup"><span data-stu-id="383d2-152">**Control**</span></span>

    <span data-ttu-id="383d2-153">กำหนดขีดจำกัดและข้อจำกัดที่ผู้ใช้แอปของคุณจะต้องใช้กับเนื้อหาของแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="383d2-153">Set limits and restrictions that your app's users will have with the content of your app.</span></span> <span data-ttu-id="383d2-154">คุณสามารถใช้ตัวควบคุมนี้เพื่อปกป้องทรัพย์สินทางปัญญาในแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="383d2-154">You can use this control to protect intellectual property in your app.</span></span>

    ![ตัวควบคุม](media/service-template-apps-create/power-bi-create-control.png)

    >[!NOTE]
    ><span data-ttu-id="383d2-156">การส่งออกเป็นรูปแบบ .pbix จะถูกบล็อกเสมอสำหรับผู้ใช้ที่ติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="383d2-156">Exporting to .pbix format is always blocked for users installing the app.</span></span>

    <span data-ttu-id="383d2-157">**พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="383d2-157">**Parameters**</span></span>

    <span data-ttu-id="383d2-158">พารามิเตอร์จะถูกสร้างขึ้นในไฟล์ .pbix เดิม (เรียนรู้เพิ่มเติมเกี่ยวกับ [การสร้างพารามิเตอร์คำถาม](https://powerbi.microsoft.com/blog/deep-dive-into-query-parameters-and-power-bi-templates/))</span><span class="sxs-lookup"><span data-stu-id="383d2-158">Parameters are created in the original pbix file (learn more about [creating query parameters](https://powerbi.microsoft.com/blog/deep-dive-into-query-parameters-and-power-bi-templates/)).</span></span> <span data-ttu-id="383d2-159">คุณใช้ความสามารถบนแท็บนี้เพื่อช่วยตัวติดตั้งแอปกำหนดค่าต่าง ๆ ของแอปหลังจากการติดตั้ง เมื่อแอปเชื่อมต่อกับข้อมูลของตัวแอปแล้ว</span><span class="sxs-lookup"><span data-stu-id="383d2-159">You use the capabilities on this tab to help the app installer configure the app after installation when they connect to their data.</span></span>

    <span data-ttu-id="383d2-160">ในแท็บนี้ คุณยังสามารถรับลิงก์ไปที่คู่มือของแอปได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="383d2-160">In this tab you also provide a link to the app documentation.</span></span>

    ![พารามิเตอร์](media/service-template-apps-create/power-bi-create-parameters.png)

    <span data-ttu-id="383d2-162">พารามิเตอร์แต่ละพารามิเตอร์จะมีชื่อและคำอธิบาย ซึ่งมาจากการสอบถามและช่องข้อมูลค่า</span><span class="sxs-lookup"><span data-stu-id="383d2-162">Each parameter has a name and a description, which come from the query, and a value field.</span></span> <span data-ttu-id="383d2-163">คุณมีตัวเลือกสามตัวเลือกในการรับค่าสำหรับพารามิเตอร์นั้นในระหว่างการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="383d2-163">You have three options for getting a value for the parameter during installation.</span></span>

    * <span data-ttu-id="383d2-164">คุณสามารถกำหนดให้ตัวติดตั้งต้องป้อนค่าได้</span><span class="sxs-lookup"><span data-stu-id="383d2-164">You can require the installer to enter a value.</span></span> <span data-ttu-id="383d2-165">ในกรณีนี้ คุณต้องให้ตัวอย่างค่าที่จะนำมาป้อนแทน</span><span class="sxs-lookup"><span data-stu-id="383d2-165">In this case, you provide an example that they will replace.</span></span> <span data-ttu-id="383d2-166">ในการกำหนดค่าพารามิเตอร์ด้วยวิธีนี้ ให้ตรวจสอบกล่องทำเครื่องหมายที่ **กำหนดไว้** จากนั้นให้แจ้งตัวอย่างในกล่องข้อความที่แสดงให้ผู้ใช้ทราบว่าควรป้อนค่าชนิดใด</span><span class="sxs-lookup"><span data-stu-id="383d2-166">To configure a parameter in this way, check the **Required** checkbox, and then give an example in the textbox that shows the user what kind of value is expected.</span></span> <span data-ttu-id="383d2-167">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="383d2-167">For example:</span></span>

       ![สกรีนช็อตของค่าพารามิเตอร์ที่ผู้ใช้จำเป็นต้องป้อน](media/service-template-apps-create/power-bi-create-parameters-require-user.png)

    * <span data-ttu-id="383d2-169">คุณสามารถให้ค่าที่กรอกไว้ล่วงหน้า ซึ่งผู้ใช้ที่ติดตั้งแอปจะไม่สามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="383d2-169">You can provide a pre-populated value that the user who installs the app can’t change.</span></span> <span data-ttu-id="383d2-170">ระบบจะซ่อนพารามิเตอร์ที่กำหนดค่าด้วยวิธีนีไว้จากบุคคลที่ติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="383d2-170">A parameter configured in this way is hidden from the person installing the app.</span></span> <span data-ttu-id="383d2-171">คุณควรใช้วิธีนี้เฉพาะเมื่อคุณมั่นใจว่าค่าที่กรอกไว้ล่วงหน้านั้นเหมาะสมสำหรับผู้ใช้ทุกคน มิเช่นนั้น ควรใช้วิธีการแรกที่กล่าวถึงข้างต้นที่กำหนดให้ต้องป้อนข้อมูลของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="383d2-171">You should use this method only if you are sure that the pre-populated value is valid for all users; otherwise use the first method mentioned above that requires user input.</span></span>

       <span data-ttu-id="383d2-172">ในการกำหนดค่าพารามิเตอร์ด้วยวิธีนี้ ให้ป้อนค่าลงในกล่องข้อความ **ค่า** จากนั้นคลิกไอคอนล็อก</span><span class="sxs-lookup"><span data-stu-id="383d2-172">To configure a parameter in this way, enter the value in the **Value** textbox and then click the lock icon.</span></span> <span data-ttu-id="383d2-173">ซึ่งจะทำให้ไม่สามารถเปลี่ยนแปลงค่าดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="383d2-173">This makes it so the value can't be changed.</span></span> <span data-ttu-id="383d2-174">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="383d2-174">For example:</span></span>

       ![สกรีนช็อตของค่าพารามิเตอร์แบบสัมบูรณ์](media/service-template-apps-create/power-bi-create-parameters-absolute.png)

    * <span data-ttu-id="383d2-176">คุณสามารถกำหนดค่าเริ่มต้นที่ผู้ใช้สามารถเปลี่ยนแปลงระหว่างการติดตั้งได้</span><span class="sxs-lookup"><span data-stu-id="383d2-176">You can provide a default value that the user can change during installation.</span></span> <span data-ttu-id="383d2-177">ในการกำหนดค่าพารามิเตอร์ด้วยวิธีนี้ ให้ป้อนค่าเริ่มต้นลงในกล่องข้อความ **ค่า** จากนั้นปล่อยให้ไอคอนล็อกอยู่ในสภาพปลดล็อกเอาไว้</span><span class="sxs-lookup"><span data-stu-id="383d2-177">To configure a parameter in this way, enter the desired default value in the **Value** textbox, and leave the lock icon unlocked.</span></span> <span data-ttu-id="383d2-178">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="383d2-178">For example:</span></span>

      ![ภาพหน้าจอของค่าพารามิเตอร์เริ่มต้นที่สามารถเปลี่ยนแปลงได้](media/service-template-apps-create/power-bi-create-parameters-default.png)

    <span data-ttu-id="383d2-180">**การรับรองความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="383d2-180">**Authentication**</span></span>
    
    <span data-ttu-id="383d2-181">ในแท็บนี้ คุณเลือกวิธีการตรวจสอบสิทธิ์ที่ต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="383d2-181">In this tab you select the authentication method that will be used.</span></span> <span data-ttu-id="383d2-182">ตัวเลือกที่พร้อมใช้งานจะขึ้นอยู่กับชนิดแหล่งข้อมูลที่ใช้</span><span class="sxs-lookup"><span data-stu-id="383d2-182">The options that are available depend on the data source types being used.</span></span>

    ![สกรีนช็อตของตัวเลือกวิธีการตรวจสอบสิทธิ์](media/service-template-apps-create/power-bi-create-authentication.png)

    <span data-ttu-id="383d2-184">โดยระบบจะกำหนดระดับความเป็นส่วนตัวให้โดยอัตโนมัติ:</span><span class="sxs-lookup"><span data-stu-id="383d2-184">Privacy level is configured automatically:</span></span>
   * <span data-ttu-id="383d2-185">แหล่งข้อมูลเดี่ยว: กำหนดค่าให้เป็นส่วนตัวโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="383d2-185">Single datasource: Automatically configured as private.</span></span>
   * <span data-ttu-id="383d2-186">แหล่งข้อมูลแบบไม่ระบุชื่อหลายรายการ: กำหนดค่าให้เป็นสาธารณะโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="383d2-186">Multi anonymous datasource: Automatically configured as public.</span></span>

    <span data-ttu-id="383d2-187">**เข้าถึง**</span><span class="sxs-lookup"><span data-stu-id="383d2-187">**Access**</span></span>
    
    <span data-ttu-id="383d2-188">ในขั้นตอนการทดสอบ ให้ตัดสินใจว่าผู้ใดในองค์กรของคุณที่จะสามารถติดตั้งและทดสอบแอปของคุณได้</span><span class="sxs-lookup"><span data-stu-id="383d2-188">In the test phase, decide who else in your organization can install and test your app.</span></span> <span data-ttu-id="383d2-189">ไม่ต้องกังวล คุณสามารถกลับมา และเปลี่ยนการตั้งค่าเหล่านี้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="383d2-189">Don't worry, you can always come back and change these settings later.</span></span> <span data-ttu-id="383d2-190">การตั้งค่าไม่มีผลต่อการเข้าถึงแอปเทมเพลตที่แจกจ่ายออกไปแล้ว</span><span class="sxs-lookup"><span data-stu-id="383d2-190">The setting doesn't affect access of the distributed template app.</span></span>

    ![สกรีนช็อตของแท็บการเข้าถึง](media/service-template-apps-create/power-bi-create-access.png)

2. <span data-ttu-id="383d2-192">เลือก **สร้างแอป**</span><span class="sxs-lookup"><span data-stu-id="383d2-192">Select **Create app**.</span></span>

    <span data-ttu-id="383d2-193">คุณเห็นข้อความทดสอบแอปพร้อม มีลิงก์เพื่อคัดลอก และแชร์กับแอปทดสอบของคุณ</span><span class="sxs-lookup"><span data-stu-id="383d2-193">You see a message that the test app is ready, with a link to copy and share with your app testers.</span></span>

    ![แอปทดสอบพร้อมใช้งานแล้ว](media/service-template-apps-create/power-bi-template-app-test-ready.png)

    <span data-ttu-id="383d2-195">นอกจากนี้คุณได้ทำขั้นตอนแรกของกระบวนการจัดการวางจำหน่าย ซึ่งตามหลัง</span><span class="sxs-lookup"><span data-stu-id="383d2-195">You've also done the first step of the release management process, which follows.</span></span>

## <a name="manage-the-template-app-release"></a><span data-ttu-id="383d2-196">จัดการการเผยแพร่แอปแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="383d2-196">Manage the template app release</span></span>

<span data-ttu-id="383d2-197">ก่อนที่คุณเผยแพร่แอปนี้แม่แบบสาธารณะ คุณต้องการให้แน่ใจว่า จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="383d2-197">Before you release this template app publicly, you want to make sure it's ready to go.</span></span> <span data-ttu-id="383d2-198">Power BI ได้สร้างบานหน้าต่างการจัดการวางจำหน่าย ที่คุณสามารถติดตาม และตรวจสอบเส้นทางการเผยแพร่แอปเต็มรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="383d2-198">Power BI has created the release management pane, where you can follow and inspect the full app release path.</span></span> <span data-ttu-id="383d2-199">คุณยังสามารถจุดชนวนการเปลี่ยนจากขั้นตอนหนึ่งไปอีกขั้น</span><span class="sxs-lookup"><span data-stu-id="383d2-199">You can also trigger the transition from stage to stage.</span></span> <span data-ttu-id="383d2-200">ขั้นตอนทั่วไปคือ:</span><span class="sxs-lookup"><span data-stu-id="383d2-200">The common stages are:</span></span>

- <span data-ttu-id="383d2-201">สร้างแอปทดสอบ: สำหรับการทดสอบภายในองค์กรของคุณเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="383d2-201">Generate test app: for testing within your organization only.</span></span>
- <span data-ttu-id="383d2-202">เลื่อนระดับแพคเกจทดสอบถึงขั้นตอนก่อนการผลิต: ทดสอบภายนอกองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="383d2-202">Promote the test package to pre-production stage: test outside of your organization.</span></span>
- <span data-ttu-id="383d2-203">เลื่อนระดับแพคเกจก่อนการผลิตไปยังการผลิต: เวอร์ชันการผลิต</span><span class="sxs-lookup"><span data-stu-id="383d2-203">Promote pre-production package to Production: production version.</span></span>
- <span data-ttu-id="383d2-204">ลบแพคเกจใด หรือเริ่มต้นจากขั้นตอนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="383d2-204">Delete any package or start over from previous stage.</span></span>

<span data-ttu-id="383d2-205">URL ไม่เปลี่ยนแปลงเมื่อคุณย้ายระหว่างขั้นตอนการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="383d2-205">The URL doesn't change as you move between release stages.</span></span> <span data-ttu-id="383d2-206">การเพิ่มระดับไม่มีผลต่อ URL เอง</span><span class="sxs-lookup"><span data-stu-id="383d2-206">Promotion doesn't affect the URL itself.</span></span>

<span data-ttu-id="383d2-207">ลองดูขั้นตอนต่าง ๆ:</span><span class="sxs-lookup"><span data-stu-id="383d2-207">Let's go through the stages:</span></span>

1. <span data-ttu-id="383d2-208">ในพื้นที่ทำงานแม่แบบ เลือก **การจัดการวางจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="383d2-208">In the template workspace, select **Release Management**.</span></span>

    ![ไอคอนการจัดการวางจำหน่าย](media/service-template-apps-create/power-bi-release-management-icon.png)

2. <span data-ttu-id="383d2-210">เลือก **รับลิงก์** หากคุณสร้างแอปทดสอบในส่วน **กำหนดคุณสมบัติของแอปแม่แบบ** ด้านบน (ซึ่งจะทำให้ระบบทำการกรอกจุดสีเหลืองที่อยู่ถัดจาก **การทดสอบ** เอาไว้ให้แล้ว)</span><span class="sxs-lookup"><span data-stu-id="383d2-210">Select **Get link** if you created the test app in the **Define the properties of the template app** section above (as a result the yellow dot next to **Testing** is already filled in).</span></span>

    <span data-ttu-id="383d2-211">หากคุณยังไม่ได้สร้างแอป ให้เลือก **สร้างแอป**</span><span class="sxs-lookup"><span data-stu-id="383d2-211">If you didn't yet create the app, select **Create app**.</span></span> <span data-ttu-id="383d2-212">ซึ่งจะนำคุณกลับไปในกระบวนการสร้างแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="383d2-212">This brings you back into the template app creation process.</span></span>

    ![สร้างแอป รับลิงก์](media/service-template-apps-create/power-bi-dev-template-create-app-get-link.png)

4. <span data-ttu-id="383d2-214">เมื่อต้องทดสอบประสบการณ์การใช้งานการติดตั้งแอป ให้คัดลอกลิงก์ในหน้าต่างการแจ้งเตือน แล้ววางลงในหน้าต่างเบราว์เซอร์ใหม่</span><span class="sxs-lookup"><span data-stu-id="383d2-214">To test the app installation experience, copy the link in the notification window and paste it into a new browser window.</span></span>

    <span data-ttu-id="383d2-215">จากที่นี่ คุณกำลังติดตามลูกค้าของคุณจะทำตามขั้นตอนเดียว</span><span class="sxs-lookup"><span data-stu-id="383d2-215">From here, you're following the same procedure your customers will follow.</span></span> <span data-ttu-id="383d2-216">ดู[ติดตั้งและแจกจ่ายแอปเทมเพลตในองค์กรของคุณ](service-template-apps-install-distribute.md)</span><span class="sxs-lookup"><span data-stu-id="383d2-216">See [Install and distribute template apps in your organization](service-template-apps-install-distribute.md).</span></span>

5. <span data-ttu-id="383d2-217">ในกล่องโต้ตอบ ให้เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="383d2-217">In the dialog box, select **Install**.</span></span>

    <span data-ttu-id="383d2-218">เมื่อการติดตั้งสำเร็จ คุณจะเห็นการแจ้งเตือนว่าแอปใหม่ของคุณพร้อมแล้ว</span><span class="sxs-lookup"><span data-stu-id="383d2-218">When installation succeeds, you see a notification that the new app is ready.</span></span>

6. <span data-ttu-id="383d2-219">เลือก **ไปยังแอป**</span><span class="sxs-lookup"><span data-stu-id="383d2-219">Select **Go to app**.</span></span>

    <span data-ttu-id="383d2-220">ตรวจสอบว่าแอปทดสอบมีข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="383d2-220">Verify that the test app has the sample data.</span></span> <span data-ttu-id="383d2-221">เมื่อต้องทำการเปลี่ยนแปลง ย้อนกลับไปยังแอปในพื้นที่ทำงานเดิม</span><span class="sxs-lookup"><span data-stu-id="383d2-221">To make any changes, go back to the app in the original workspace.</span></span> <span data-ttu-id="383d2-222">ปรับปรุงแอปทดสอบจนกว่าคุณจะพอใจ</span><span class="sxs-lookup"><span data-stu-id="383d2-222">Update the test app until you're satisfied.</span></span>

1. <span data-ttu-id="383d2-223">เมื่อคุณพร้อมที่จะเลื่อนระดับแอปของคุณไปยังการผลิตล่วงหน้าสำหรับการทดสอบภายนอกผู้เช่าของคุณเพิ่มเติม ย้อนกลับไป **การจัดการวางจำหน่าย** บานหน้าต่างและเลือก **เลื่อนแอป**</span><span class="sxs-lookup"><span data-stu-id="383d2-223">When you're ready to promote your app to pre-production for further testing outside your tenant, go back to the **Release Management** pane and select **Promote app**.</span></span>

    ![เลื่อนระดับแอปเป็นระดับก่อนใช้งานจริง](media/service-template-apps-create/power-bi-template-app-promote.png)
    >[!NOTE]
    > <span data-ttu-id="383d2-225">เมื่อเลื่อนระดับแอปแล้ว แอปจะอยู่ในรูปแบบสาธารณะที่พร้อมใช้งานภายนอกองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="383d2-225">When the app is promoted it becomes publicly available outside your organization.</span></span>

    <span data-ttu-id="383d2-226">ถ้าคุณไม่เห็นตัวเลือกนั้น ติดต่อผู้ดูแลระบบ Power BI ของคุณเพื่อให้สิทธิ์แก่[สิทธิ์สำหรับการพัฒนาแอปแม่แบบ](../admin/service-admin-portal.md#template-apps-settings)ในพอร์ทัลผู้ดูแล</span><span class="sxs-lookup"><span data-stu-id="383d2-226">If you don't see that option, contact your Power BI admin to grant you [permissions for template app development](../admin/service-admin-portal.md#template-apps-settings) in the admin portal.</span></span>
11. <span data-ttu-id="383d2-227">เลือก **เลื่อน** เพื่อยืนยันตัวเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="383d2-227">Select **Promote** to confirm your choice.</span></span>
12. <span data-ttu-id="383d2-228">คัดลอก URL นี้ใหม่เมื่อต้องแชร์ภายนอกผู้เช่าของคุณสำหรับการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="383d2-228">Copy this new URL to share outside your tenant for testing.</span></span> <span data-ttu-id="383d2-229">ลิงก์นี้ยังเป็นลิงก์ที่คุณส่งเพื่อเริ่มกระบวนการแจกจ่ายแอปของคุณบน AppSource โดยการสร้าง[ข้อเสนอสำหรับ Partner Center ใหม่](/azure/marketplace/partner-center-portal/create-power-bi-app-offer)</span><span class="sxs-lookup"><span data-stu-id="383d2-229">This link is also the one you submit to begin the process of distributing your app on AppSource by creating a [new Partner center offer](/azure/marketplace/partner-center-portal/create-power-bi-app-offer).</span></span> <span data-ttu-id="383d2-230">ส่งลิงก์ก่อนการผลิตไปที่ Partner Center เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="383d2-230">Submit only pre-production links to the Partner center.</span></span> <span data-ttu-id="383d2-231">หลังจากที่แอปผ่านการอนุมัติและคุณได้รับการแจ้งเตือนว่าแอปนั้นเผยแพร่ใน AppSource แล้วเท่านั้น คุณจึงจะสามารถเลื่อนระดับแพ็กเกจนี้ไปเป็นการผลิตใน Power BI</span><span class="sxs-lookup"><span data-stu-id="383d2-231">Only after the app is approved and you get notification that it is published in AppSource, can you promote this package to production in Power BI.</span></span>
13. <span data-ttu-id="383d2-232">เมื่อแอปของคุณพร้อมสำหรับการผลิตหรือการแชร์ผ่าน AppSource ย้อนกลับไป **การจัดการวางจำหน่าย** บานหน้าต่างและเลือก **เลื่อนแอป** ถัดจาก **ก่อนการผลิต**</span><span class="sxs-lookup"><span data-stu-id="383d2-232">When your app is ready for production or sharing via AppSource, go back to the **Release Management** pane and select **Promote app** next to **Pre-production**.</span></span>
14. <span data-ttu-id="383d2-233">เลือก **เลื่อน** เพื่อยืนยันตัวเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="383d2-233">Select **Promote** to confirm your choice.</span></span>

    <span data-ttu-id="383d2-234">ตอนนี้ แอปของคุณอยู่ ในการ ผลิต และพร้อมสำหรับการแจกแจง</span><span class="sxs-lookup"><span data-stu-id="383d2-234">Now your app is in production, and ready for distribution.</span></span>

    ![แอปอยู่ระหว่างการผลิต](media/service-template-apps-create/power-bi-template-app-production.png)

<span data-ttu-id="383d2-236">เพื่อให้แอปของคุณพร้อมใช้งานทั่วไปหลายพันของผู้ใช้ Power BI ในโลก เราขอแนะนำให้คุณส่งไปยัง AppSource</span><span class="sxs-lookup"><span data-stu-id="383d2-236">To make your app widely available to thousands of Power BI users in the world, we encourage you to submit it to AppSource.</span></span> <span data-ttu-id="383d2-237">ดู[ข้อเสนอแอปพลิเคชันPower BI](/azure/marketplace/partner-center-portal/create-power-bi-app-offer)สำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="383d2-237">See the [Power BI Application offer](/azure/marketplace/partner-center-portal/create-power-bi-app-offer) for details.</span></span>

## <a name="automate-parameter-configuration-during-installation"></a><span data-ttu-id="383d2-238">การกําหนดค่าพารามิเตอร์โดยอัตโนมัติระหว่างการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="383d2-238">Automate parameter configuration during installation</span></span>

<span data-ttu-id="383d2-239">หากคุณเป็น ISV และกําลังแจกจ่ายแอปเทมเพลตของคุณผ่านบริการเว็บของคุณ คุณสามารถสร้างการทํางานอัตโนมัติที่กําหนดค่าพารามิเตอร์แอปเทมเพลตโดยอัตโนมัติเมื่อลูกค้าของคุณติดตั้งแอปในบัญชี Power BI ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="383d2-239">If you are an ISV and are distributing your template app via your web service, you can create automation that configures template app parameters automatically when your customers install the app in their Power BI account.</span></span> <span data-ttu-id="383d2-240">ซึ่งจะช่วยให้ลูกค้าของคุณดำเนินการได้ง่ายขึ้นและเพิ่มความเป็นไปได้ในการติดตั้งสำเร็จ เนื่องจากพวกเขาไม่จำเป็นต้องให้รายละเอียดที่พวกเขาอาจไม่ทราบ</span><span class="sxs-lookup"><span data-stu-id="383d2-240">This makes things easier for your customers and increases the likelihood of a successful installation because they don't have to supply details that they might not know.</span></span> <span data-ttu-id="383d2-241">ดูรายละเอียดที่[การกำหนดค่าอัตโนมัติของการติดตั้งแอปเทมเพลต](../developer/template-apps/template-apps-auto-install.md)</span><span class="sxs-lookup"><span data-stu-id="383d2-241">See [Automated configuration of a template app installation](../developer/template-apps/template-apps-auto-install.md) for details.</span></span>

## <a name="next-steps"></a><span data-ttu-id="383d2-242">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="383d2-242">Next steps</span></span>

<span data-ttu-id="383d2-243">ดูวิธีการที่ลูกค้าของคุณโต้ตอบกับแอปแม่แบบของคุณใน[ติดตั้ง กำหนดเอง และเผยแพรแอปแม่แบบในองค์กรของคุณ](service-template-apps-install-distribute.md)</span><span class="sxs-lookup"><span data-stu-id="383d2-243">See how your customers interact with your template app in [Install, customize, and distribute template apps in your organization](service-template-apps-install-distribute.md).</span></span>

<span data-ttu-id="383d2-244">ดู[ข้อเสนอแอปพลิเคชัน BI Power](/azure/marketplace/partner-center-portal/create-power-bi-app-offer)สำหรับรายละเอียดเกี่ยวกับการแจกจ่ายแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="383d2-244">See the [Power BI Application offer](/azure/marketplace/partner-center-portal/create-power-bi-app-offer) for details on distributing your app.</span></span>