---
title: ติดตั้งและแจกจ่ายแอปแม่แบบในองค์กรของคุณ - Power BI (ตัวอย่าง)
description: เรียนรู้เกี่ยวกับการติดตั้ง กำหนดเอง และการแจกจ่ายแอปแม่แบบในองค์กรของคุณใน Power BI
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: how-to
ms.date: 09/17/2020
ms.openlocfilehash: e6499d9e4547f1bd2b8cf4ac29fbc375af871f8a
ms.sourcegitcommit: 8250187368d3de48663eb516a816ff701119b579
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/10/2020
ms.locfileid: "96998679"
---
# <a name="install-and-distribute-template-apps-in-your-organization"></a><span data-ttu-id="0dca2-103">ติดตั้งและแจกจ่ายแอปเทมเพลตในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="0dca2-103">Install and distribute template apps in your organization</span></span>

<span data-ttu-id="0dca2-104">คุณเป็นนักวิเคราะห์ Power BI หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0dca2-104">Are you a Power BI analyst?</span></span> <span data-ttu-id="0dca2-105">ถ้าใช่ บทความนี้จะอธิบายวิธีการติดตั้ง[แอปเทมเพลต](service-template-apps-overview.md)เพื่อเชื่อมต่อกับบริการมากมายที่คุณใช้เพื่อดำเนินธุรกิจ เช่น Salesforce, Microsoft Dynamics และ Google Analytics</span><span class="sxs-lookup"><span data-stu-id="0dca2-105">If so, this article explains how you can  install [template apps](service-template-apps-overview.md) to connect to many of the services you use to run your business, such as Salesforce, Microsoft Dynamics, and Google Analytics.</span></span> <span data-ttu-id="0dca2-106">จากนั้นคุณสามารถแก้ไขแดชบอร์ดและรายงานที่สร้างไว้ล่วงหน้าของแอปเทมเพลตเพื่อให้เหมาะกับความต้องการขององค์กรของคุณ และแจกจ่ายให้เพื่อนร่วมงานของคุณเป็น[แอป](../consumer/end-user-apps.md)ได้</span><span class="sxs-lookup"><span data-stu-id="0dca2-106">You can then modify the template app's pre-built dashboard and reports to suit the needs of your organization, and distribute them to your colleagues as [apps](../consumer/end-user-apps.md).</span></span> 

![Power BI ได้ติดตั้งแล้ว](media/service-template-apps-install-distribute/power-bi-get-apps.png)

<span data-ttu-id="0dca2-108">ถ้าคุณสนใจที่จะสร้างแอปเทมเพลตเพื่อกระจายด้วยตนเองเพื่อแจกจ่ายนอกองค์กร ให้ดู[สร้างแอปเทมเพลตใน Power BI](service-template-apps-create.md)</span><span class="sxs-lookup"><span data-stu-id="0dca2-108">If you're interested in creating template apps yourself for distribution outside your organization, see [Create a template app in Power BI](service-template-apps-create.md).</span></span> <span data-ttu-id="0dca2-109">คู่ค้า Power BI สามารถสร้างแอป Power BI และทำให้แอปดังกล่าวพร้อมใช้งานสำหรับลูกค้า Power BI ได้ด้วยการเขียนโค้ดเพียงเล็กน้อยหรือไม่ต้องเขียนโค้ดเลย</span><span class="sxs-lookup"><span data-stu-id="0dca2-109">With little or no coding, Power BI partners can build Power BI apps and make them available to Power BI customers.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="0dca2-110">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="0dca2-110">Prerequisites</span></span>  

<span data-ttu-id="0dca2-111">หากต้องการติดตั้ง ปรับแต่ง และเผยแพร่แอปเทมเพลต คุณจำเป็นต้องมี:</span><span class="sxs-lookup"><span data-stu-id="0dca2-111">To install, customize, and distribute a template app, you need:</span></span> 

* <span data-ttu-id="0dca2-112">[สิทธิการใช้งาน Power BI Pro](../fundamentals/service-self-service-signup-for-power-bi.md)</span><span class="sxs-lookup"><span data-stu-id="0dca2-112">A [Power BI pro license](../fundamentals/service-self-service-signup-for-power-bi.md).</span></span>
* <span data-ttu-id="0dca2-113">สิทธิ์ในการติดตั้งแอปเทมเพลตบนผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="0dca2-113">Permissions to install template apps on your tenant.</span></span>
* <span data-ttu-id="0dca2-114">ลิงก์การติดตั้งแอปที่ถูกต้อง ซึ่งคุณจะได้รับจาก AppSource หรือจากผู้สร้างแอป</span><span class="sxs-lookup"><span data-stu-id="0dca2-114">A valid installation link for the app, which you get either from AppSource or from the app creator.</span></span>
* <span data-ttu-id="0dca2-115">ความคุ้นเคยที่ดีกับ[แนวคิดพื้นฐานของ Power BI](../fundamentals/service-basic-concepts.md)</span><span class="sxs-lookup"><span data-stu-id="0dca2-115">A good familiarity with the [basic concepts of Power BI ](../fundamentals/service-basic-concepts.md).</span></span>

## <a name="install-a-template-app"></a><span data-ttu-id="0dca2-116">สร้างแอปแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="0dca2-116">Install a template app</span></span>

1. <span data-ttu-id="0dca2-117">ในบานหน้าต่างนำทางของบริการ Power BI เลือก **แอป** > **รับแอป**</span><span class="sxs-lookup"><span data-stu-id="0dca2-117">In the nav pane in the Power BI service, select **Apps** > **Get apps**.</span></span>

    ![รับแอป](media/service-template-apps-install-distribute/power-bi-get-apps-arrow.png)

1. <span data-ttu-id="0dca2-119">ใน Power BI apps marketplace ที่ปรากฏขึ้น ให้เลือก **แอปแม่แบบ**</span><span class="sxs-lookup"><span data-stu-id="0dca2-119">In the Power BI apps marketplace that appears, select **Template apps**.</span></span> <span data-ttu-id="0dca2-120">แอปแบบแม่แบบทั้งหมดที่พร้อมใช้งานใน AppSource จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="0dca2-120">All the template apps available in AppSource will be shown.</span></span> <span data-ttu-id="0dca2-121">เรียกดูเพื่อค้นหาแอปแบบแม่แบบที่คุณกำลังค้นหา หรือรับการเลือกการกรองโดยใช้กล่องค้นหา</span><span class="sxs-lookup"><span data-stu-id="0dca2-121">Browse to find the template app you're looking for, or get a filtered selection by using the search box.</span></span> <span data-ttu-id="0dca2-122">การพิมพ์ส่วนหนึ่งของชื่อแอปแม่แบบ หรือประเภทเช่น การเงิน การวิเคราะห์ การตลาด และอื่นๆ จะช่วยให้ง่ายต่อการค้นหารายการที่คุณกำลังมองหา</span><span class="sxs-lookup"><span data-stu-id="0dca2-122">Typing part of the name of the template app, or of a category such as finance, analytics, marketing, etc., will make it easier to find the item you're looking for.</span></span>

    ![ค้นหาใน AppSource](media/service-template-apps-install-distribute/power-bi-appsource.png)

1. <span data-ttu-id="0dca2-124">เมื่อคุณพบแอปแม่แบบที่คุณกำลังค้นหา ให้คลิกที่แอปนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="0dca2-124">When you find the template app you're looking for, click it.</span></span> <span data-ttu-id="0dca2-125">ข้อเสนอแอปแม่แบบจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="0dca2-125">The template app offer will display.</span></span> <span data-ttu-id="0dca2-126">คลิก **รับทันที**</span><span class="sxs-lookup"><span data-stu-id="0dca2-126">Click **GET IT NOW**.</span></span>

   ![ข้อเสนอแอปแม่แบบ](media/service-template-apps-install-distribute/power-bi-template-app-offer.png)

1. <span data-ttu-id="0dca2-128">ในกล่องโต้ตอบที่ปรากฏขึ้น ให้เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="0dca2-128">In the dialog box that appears, select **Install**.</span></span>

    ![ติดตั้งแอป](media/service-template-apps-install-distribute/power-install-dialog.png)
    
    <span data-ttu-id="0dca2-130">แอปจะได้รับการติดตั้งพร้อมกับพื้นที่ทำงานชื่อเดียวกันกับที่มีความจำเป็นสำหรับ[การแก้ไข](#customize-and-share-the-app)เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0dca2-130">The app is installed, along with a workspace of the same name that has all the artifacts needed for further [customization](#customize-and-share-the-app).</span></span>

    > [!NOTE]
    > <span data-ttu-id="0dca2-131">หากคุณใช้ลิงก์การติดตั้งสำหรับแอปที่ไม่ระบุอยู่ใน AppSource กล่องโต้ตอบสำหรับการตรวจสอบความถูกต้องจะขอให้คุณยืนยันตัวเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="0dca2-131">If you use an installation link for an app that isn't listed on AppSource, a validation dialog box will ask you to confirm your choice.</span></span>
    >
    ><span data-ttu-id="0dca2-132">เพื่อให้สามารถติดตั้งแอปเทมเพลตที่ไม่ได้อยู่ใน AppSource คุณจำเป็นต้องร้องขอสิทธิ์ที่เกี่ยวข้องจากผู้ดูแลระบบของคุณ ดูรายละเอียดที่ [การตั้งค่าแอปเทมเพลต](../admin/service-admin-portal.md#template-apps-settings) ในพอร์ทัลผู้ดูแลระบบ Power BI</span><span class="sxs-lookup"><span data-stu-id="0dca2-132">To be able to install a template app that is not listed on AppSource, you need to request the relevant permissions from your admin. See the [Template app settings](../admin/service-admin-portal.md#template-apps-settings) in Power BI admin portal for details.</span></span>

    <span data-ttu-id="0dca2-133">เมื่อการติดตั้งสำเร็จแล้ว การแจ้งเตือนจะแจ้งให้คุณทราบว่าแอปใหม่ของคุณพร้อมใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="0dca2-133">When the installation finishes successfully, a notification tells you that your new app is ready.</span></span>

    ![ไปยังแอป](media/service-template-apps-install-distribute/power-bi-go-to-app.png)

## <a name="connect-to-data"></a><span data-ttu-id="0dca2-135">เชื่อมต่อกับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0dca2-135">Connect to data</span></span>

1. <span data-ttu-id="0dca2-136">เลือก **ไปยังแอป**</span><span class="sxs-lookup"><span data-stu-id="0dca2-136">Select **Go to app**.</span></span>

   <span data-ttu-id="0dca2-137">แอปจะเปิดขึ้นและแสดงข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="0dca2-137">The app opens, showing sample data.</span></span>

1. <span data-ttu-id="0dca2-138">เลือกลิงก์ **เชื่อมต่อข้อมูลของคุณ** บนแบนเนอร์ที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="0dca2-138">Select the **Connect your data** link on the banner at the top of the page.</span></span>

   ![แอป GitHub เชื่อมโยงลิงก์ข้อมูลของคุณ](media/service-template-apps-install-distribute/power-bi-template-app-connect-data.png)

    <span data-ttu-id="0dca2-140">ซึ่งจะเปิดกล่องโต้ตอบพารามิเตอร์ ที่คุณสามารถเปลี่ยนแหล่งข้อมูลจากข้อมูลตัวอย่างเป็นแหล่งข้อมูลของคุณเอง (ดู[ข้อจำกัดที่รู้จัก](service-template-apps-overview.md#known-limitations)) ตามด้วยกล่องโต้ตอบวิธีการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="0dca2-140">This opens the parameters dialog, where you change the data source from the sample data to your own data source (see [known limitations](service-template-apps-overview.md#known-limitations)), followed by the authentication method dialog.</span></span> <span data-ttu-id="0dca2-141">คุณอาจต้องกำหนดค่าใหม่ในกล่องโต้ตอบเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="0dca2-141">You may have to redefine the values in these dialogs.</span></span> <span data-ttu-id="0dca2-142">ดูเอกสารประกอบของแอปเทมเพลตที่คุณกำลังติดตั้งอยู่เพื่อดูรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="0dca2-142">See the documentation of the specific template app you're installing for details.</span></span>

   ![สกรีนช็อตของการเชื่อมต่อกับกล่องโต้ตอบข้อมูล](media/service-template-apps-install-distribute/power-bi-template-app-connect-to-data-dialogs.png)

    <span data-ttu-id="0dca2-144">หลังจากที่คุณกรอกข้อความโต้ตอบสำหรับการเชื่อมต่อแล้ว กระบวนการเชื่อมต่อจะเริ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="0dca2-144">Once you've finished filling out the connection dialogs, the connection process starts.</span></span> <span data-ttu-id="0dca2-145">แบนเนอร์จะแจ้งให้คุณทราบว่าข้อมูลกำลังถูกรีเฟรช และในระหว่างนี้คุณกำลังดูข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="0dca2-145">A banner informs you that the data is being refreshed, and that in the meantime you are viewing sample data.</span></span>

    ![กำลังดูข้อมูลตัวอย่าง](media/service-template-apps-install-distribute/power-bi-template-app-viewing-sample-data.png)

   <span data-ttu-id="0dca2-147">ข้อมูลรายงานของคุณจะรีเฟรชโดยอัตโนมัติหนึ่งครั้งต่อวัน เว้นแต่ว่าคุณจะปิดใช้งานการดำเนินการนี้ในระหว่างกระบวนการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="0dca2-147">Your report data will automatically refresh once a day, unless you disabled this during the sign-in process.</span></span> <span data-ttu-id="0dca2-148">นอกจากนี้ คุณยังสามารถ [ตั้งค่าตารางเวลาการรีเฟรชของคุณเอง](./refresh-scheduled-refresh.md) เพื่อรักษาข้อมูลรายงานให้เป็นปัจจุบันหากคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="0dca2-148">You can also [set up your own refresh schedule](./refresh-scheduled-refresh.md) to keep the report data up to date if you so desire.</span></span>

## <a name="customize-and-share-the-app"></a><span data-ttu-id="0dca2-149">ปรับแต่งและแชร์แอป</span><span class="sxs-lookup"><span data-stu-id="0dca2-149">Customize and share the app</span></span>

<span data-ttu-id="0dca2-150">หลังจากที่คุณเชื่อมต่อกับข้อมูลและการรีเฟรชข้อมูลของคุณเสร็จสมบูรณ์แล้ว คุณสามารถปรับแต่งรายงานและแดชบอร์ดของแอปรวมถึงการแชร์แอปให้กับเพื่อนร่วมงานของคุณได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="0dca2-150">After you've connected to your data and data refresh is complete, you can customize any of the reports and dashboards the apps includes, as well as share the app with your colleagues.</span></span> <span data-ttu-id="0dca2-151">อย่างไรก็ตาม โปรดจำไว้ว่าการเปลี่ยนแปลงใดก็ตามที่คุณทำจะถูกเขียนทับเมื่อคุณอัปเดตแอปด้วยเวอร์ชันใหม่ เว้นแต่ว่าคุณจะบันทึกรายการที่คุณเปลี่ยนแปลงภายใต้ชื่อที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="0dca2-151">Remember, however that any changes you make will be overwritten when you update the app with a new version, unless you save the items you changed under different names.</span></span> <span data-ttu-id="0dca2-152">[ดูรายละเอียดเกี่ยวกับการเขียนทับ](#overwrite-behavior)</span><span class="sxs-lookup"><span data-stu-id="0dca2-152">[See details about overwriting](#overwrite-behavior).</span></span>

<span data-ttu-id="0dca2-153">เมื่อต้องการกำหนดค่าและแชร์แอปของคุณ ให้เลือกไอคอนรูปดินสอที่มุมบนขวาของหน้า</span><span class="sxs-lookup"><span data-stu-id="0dca2-153">To customize and share your app, select the pencil icon at the top right corner of the page.</span></span>

![แก้ไขแอป](media/service-template-apps-install-distribute/power-bi-template-app-edit-app.png)


<span data-ttu-id="0dca2-155">สำหรับข้อมูลเกี่ยวกับการแก้ไขอาร์ทิแฟกต์ในพื้นที่ทำงาน โปรดดู</span><span class="sxs-lookup"><span data-stu-id="0dca2-155">For information about editing artifacts in the workspace, see</span></span>
* [<span data-ttu-id="0dca2-156">แนะนำตัวแก้ไขรายงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="0dca2-156">Tour the report editor in Power BI</span></span>](../create-reports/service-the-report-editor-take-a-tour.md)
* [<span data-ttu-id="0dca2-157">แนวคิดพื้นฐานสำหรับนักออกแบบในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="0dca2-157">Basic concepts for designers in the Power BI service</span></span>](../fundamentals/service-basic-concepts.md)

<span data-ttu-id="0dca2-158">หลังจากที่คุณทำการเปลี่ยนแปลงใดก็ตามที่คุณต้องการทำกับอาร์ทิแฟกต์ในพื้นที่ทำงาน คุณก็พร้อมที่จะเผยแพร่และแชร์แอป</span><span class="sxs-lookup"><span data-stu-id="0dca2-158">Once you are done making any changes you wish to the artifacts in the workspace, you are ready to publish and share the app.</span></span> <span data-ttu-id="0dca2-159">ดู [เผยแพร่แอปของคุณ](../collaborate-share/service-create-distribute-apps.md#publish-your-app) เพื่อเรียนรู้วิธีการทำเช่นนี้</span><span class="sxs-lookup"><span data-stu-id="0dca2-159">See [Publish your app](../collaborate-share/service-create-distribute-apps.md#publish-your-app) to learn how to do this.</span></span>

## <a name="update-a-template-app"></a><span data-ttu-id="0dca2-160">อัปเดตแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="0dca2-160">Update a template app</span></span>

<span data-ttu-id="0dca2-161">ในบางครั้ง ผู้สร้างแอปเทมเพลตจะปล่อยแอปเทมเพลตรุ่นใหม่ที่มีการปรับปรุง ผ่าน AppSource ลิงก์โดยตรง หรือทั้งสองทางอย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0dca2-161">From time to time, template app creators release new improved versions of their template apps, via either AppSource, direct link, or both.</span></span>

<span data-ttu-id="0dca2-162">หากคุณดาวน์โหลดแอปจาก AppSource ในครั้งแรก เมื่อเวอร์ชันใหม่ของแอปเทมเพลตพร้อมใช้งาน คุณจะได้รับการแจ้งเตือนสองวิธี:</span><span class="sxs-lookup"><span data-stu-id="0dca2-162">If you originally downloaded the app from AppSource, when a new version of the template app becomes available, you get notified in two ways:</span></span>
* <span data-ttu-id="0dca2-163">แบนเนอร์การอัปเดตที่ปรากฏในบริการของ Power BI แจ้งให้คุณทราบว่ามีแอปเวอร์ชันใหม่ที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0dca2-163">An update banner appears in the Power BI service informing you that a new app version is available.</span></span>
  <span data-ttu-id="0dca2-164">![แบนเนอร์การแจ้งเตือนการอัปเดตแอปเทมเพลต](media/service-template-apps-install-distribute/power-bi-new-app-version-notification-banner.png)</span><span class="sxs-lookup"><span data-stu-id="0dca2-164">![Template app update notification banner](media/service-template-apps-install-distribute/power-bi-new-app-version-notification-banner.png)</span></span>
* <span data-ttu-id="0dca2-165">คุณได้รับการแจ้งเตือนในบานหน้าต่างการแจ้งเตือนของ Power BI</span><span class="sxs-lookup"><span data-stu-id="0dca2-165">You receive a notification in Power BI's notification pane.</span></span>


  ![แผงการแจ้งเตือนการอัปเดตแอปเทมเพลต](media/service-template-apps-install-distribute/power-bi-new-app-version-notification-pane.png)

>[!NOTE]
><span data-ttu-id="0dca2-167">ถ้าแรกเริ่มคุณได้รับแอปผ่านลิงก์โดยตรงแทนที่จะผ่าน AppSource วิธีเดียวที่จะทราบว่าเมื่อไรที่มีเวอร์ชันใหม่พร้อมใช้งานคือการติดต่อผู้สร้างแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="0dca2-167">If you originally got the app via direct link rather than through AppSource, the only way to know when a new version is available is to contact the template app creator.</span></span>

  <span data-ttu-id="0dca2-168">หากต้องการติดตั้งการอัปเดต ให้คลิก **รับ** บนแบนเนอร์การแจ้งเตือนหรือในศูนย์การแจ้งเตือน หรือค้นหาแอปอีกครั้งใน AppSource และเลือก **รับทันที**</span><span class="sxs-lookup"><span data-stu-id="0dca2-168">To install the update, either click **Get it** on the notification banner or in the notification center, or find the app again in AppSource and choose **Get it now**.</span></span> <span data-ttu-id="0dca2-169">ถ้าคุณมีลิงก์โดยตรงสำหรับการอัปเดตจากผู้สร้างแอปเทมเพลต เพียงคลิกที่ลิงก์</span><span class="sxs-lookup"><span data-stu-id="0dca2-169">If you got a direct link for the update from the Template app creator, simply click the link.</span></span>
  
  <span data-ttu-id="0dca2-170">ระบบจะถามว่าคุณต้องการเขียนทับเวอร์ชันปัจจุบัน หรือติดตั้งเวอร์ชันใหม่ในพื้นที่ทำงานใหม่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0dca2-170">You will be asked whether you wish to overwrite the current version, or to install the new version in a new workspace.</span></span> <span data-ttu-id="0dca2-171">ตามค่าเริ่มต้น "เขียนทับ" จะถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="0dca2-171">By default, "overwrite" is selected.</span></span>

  ![อัปเดตแอปเทมเพลต](media/service-template-apps-install-distribute/power-bi-update-app-overwrite.png)

- <span data-ttu-id="0dca2-173">**เขียนทับเวอร์ชั่นปัจจุบัน:** เขียนทับพื้นที่ทำงานเป็นเวอร์ชั่นอัปเดตของแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="0dca2-173">**Overwrite an existing version:** Overwrites the existing workspace with the updated version of the template app.</span></span> <span data-ttu-id="0dca2-174">[ดูรายละเอียดเกี่ยวกับการเขียนทับ](#overwrite-behavior)</span><span class="sxs-lookup"><span data-stu-id="0dca2-174">[See details about overwriting](#overwrite-behavior).</span></span>

- <span data-ttu-id="0dca2-175">**ติดตั้งไปยังพื้นที่ทำงานใหม่:** ติดตั้งพื้นที่ทำงานและแอปเวอร์ชันใหม่ล่าสุดที่คุณต้องการกำหนดค่าอีกครั้ง (นั่นคือ เชื่อมต่อกับข้อมูล กำหนดการนำทางและสิทธิ์อนุญาต)</span><span class="sxs-lookup"><span data-stu-id="0dca2-175">**Install to a new workspace:** Installs a fresh version of the workspace and app that you need to reconfigure (that is, connect to data, define navigation and permissions).</span></span>

### <a name="overwrite-behavior"></a><span data-ttu-id="0dca2-176">รูปแบบการเขียนทับ</span><span class="sxs-lookup"><span data-stu-id="0dca2-176">Overwrite behavior</span></span>

* <span data-ttu-id="0dca2-177">เขียนทับข้อมูลอัปเดตรายงาน แดชบอร์ด และชุดข้อมูบภายในพื้นที่ทำงาน ไม่ใช่แอป</span><span class="sxs-lookup"><span data-stu-id="0dca2-177">Overwriting updates the reports, dashboards, and dataset inside the workspace, not the app.</span></span> <span data-ttu-id="0dca2-178">การเขียนทับไม่ได้เป็นการเปลี่ยนการนำทางของแอป การตั้งค่าและสิทธิ์อนุญาต</span><span class="sxs-lookup"><span data-stu-id="0dca2-178">Overwriting doesn't change app navigation, setup, and permissions.</span></span>
* <span data-ttu-id="0dca2-179">หลังจากอัปเดตพื้นที่ทำงาน **คุณจะต้องอัปเดตแอปเพื่อปรับใช้การเปลี่ยนแปลงจากพื้นที่ทำงานดังกล่าวไปยังแอป**</span><span class="sxs-lookup"><span data-stu-id="0dca2-179">After you update the workspace, **you need to update the app to apply changes from the workspace to the app**.</span></span>
* <span data-ttu-id="0dca2-180">การเขียนทับจะยังคงเก็บค่าพารามิเตอร์และการตรวจรับรองที่กำหนดค่าไว้</span><span class="sxs-lookup"><span data-stu-id="0dca2-180">Overwriting keeps configured parameters and authentication.</span></span> <span data-ttu-id="0dca2-181">หลังการอัปเดต การรีเฟรชชุดข้อมูลอัตโนมัติจะเริ่มต้นขึ้น</span><span class="sxs-lookup"><span data-stu-id="0dca2-181">After update, an automatic dataset refresh starts.</span></span> <span data-ttu-id="0dca2-182">**ในระหว่างการรีเฟรชนี้ แอป รายงาน และแดชบอร์ดแสดงข้อมูลตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="0dca2-182">**During this refresh, the app, reports, and dashboards present sample data**.</span></span>

  ![ข้อมูลตัวอย่าง](media/service-template-apps-install-distribute/power-bi-sample-data.png)

* <span data-ttu-id="0dca2-184">การเขียนทับจะเป็นการนำเสนอข้อมูลตัวอย่างจนกว่าการรีเฟรชจะเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="0dca2-184">Overwriting always presents sample data until the refresh is complete.</span></span> <span data-ttu-id="0dca2-185">หากผู้สร้างแอปเทมเพลตทำการแก้ไขชุดข้อมูลหรือพารามิเตอร์ ผู้ใช้พื้นที่ทำงานและแอปจะมองไม่เห็นข้อมูลใหม่จนกว่าการรีเฟรชจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="0dca2-185">If the template app author made changes to the dataset or parameters, users of the workspace and app will not see the new data until the refresh is complete.</span></span> <span data-ttu-id="0dca2-186">แต่พวกเขาจะยังคงเห็นข้อมูลตัวอย่างในช่วงเวลานี้</span><span class="sxs-lookup"><span data-stu-id="0dca2-186">Rather, they will continue to see sample data during this time.</span></span>
* <span data-ttu-id="0dca2-187">การเขียนทับไม่ได้เป็นการลบรายงานหรือแดชบอร์ดใหม่ที่คุณเพิ่งเพิ่มไปยังพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="0dca2-187">Overwriting never deletes new reports or dashboards you've added to the workspace.</span></span> <span data-ttu-id="0dca2-188">โดยจะเป็นการเขียนทับรายงานและแดชบอร์ดเดิมที่มีการเปลี่ยนแปลงจากผู้สร้างเดิมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0dca2-188">It only overwrites the original reports and dashboards with changes from the original author.</span></span>

>[!IMPORTANT]
><span data-ttu-id="0dca2-189">อย่าลืม[อัปเดตแอป](#customize-and-share-the-app)หลังจากเขียนทับเพื่อปรับใช้การเปลี่ยนแปลงกับรายงานและแดชบอร์ดสำหรับผู้ใช้แอพหน่วยงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="0dca2-189">Remember to [update the app](#customize-and-share-the-app) after overwriting to apply changes to the reports and dashboard for your organizational app users.</span></span>

## <a name="delete-a-template-app"></a><span data-ttu-id="0dca2-190">ลบแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="0dca2-190">Delete a template app</span></span>

<span data-ttu-id="0dca2-191">แอปเทมเพลตที่ติดตั้งแล้วประกอบด้วยแอปและพื้นที่ทํางานที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="0dca2-191">An installed template app consists of the app and its associated workspace.</span></span> <span data-ttu-id="0dca2-192">หากคุณต้องการลบแอปเทมเพลต คุณมีสองตัวเลือก:</span><span class="sxs-lookup"><span data-stu-id="0dca2-192">If you want to remove the template app, you have two options:</span></span>
* <span data-ttu-id="0dca2-193">**ลบแอปและพื้นที่ทํางานที่เกี่ยวข้องออกโดยสมบูรณ์**: หากต้องการลบแอปเทมเพลตและพื้นที่ทำงานที่เกี่ยวข้อง ให้ไปที่ไทล์แอปบนหน้าแอป เลือกไอคอนถังขยะ จากนั้นจึงคลิก **ลบ** ในกล่องโต้ตอบที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="0dca2-193">**Completely remove the app and its associated workspace**: To completely remove template app and its associated workspace, go to the app tile on the Apps page, select the trash icon, and then click **Delete** in the dialog that appears.</span></span>
* <span data-ttu-id="0dca2-194">**ยกเลิกการเผยแพร่แอป**: ตัวเลือกนี้จะลบแอป แต่เก็บพื้นที่ทํางานที่เกี่ยวข้องไว้</span><span class="sxs-lookup"><span data-stu-id="0dca2-194">**Unpublish the app**: This option removes the app but keeps its associated workspace.</span></span> <span data-ttu-id="0dca2-195">ตัวเลือกนี้มีประโยชน์ เช่น หากมีการปรับแต่งที่คุณต้องการเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="0dca2-195">This option is useful if, for instance, there are customizations that you made that you want to keep.</span></span>

    <span data-ttu-id="0dca2-196">วิธียกเลิกการเผยแพร่แอป:</span><span class="sxs-lookup"><span data-stu-id="0dca2-196">To unpublish the app:</span></span>
    1. <span data-ttu-id="0dca2-197">เปิดแอป</span><span class="sxs-lookup"><span data-stu-id="0dca2-197">Open the app.</span></span>
    1. <span data-ttu-id="0dca2-198">คลิกที่ไอคอนดินสอแก้ไขแอป เพื่อเปิดพื้นที่ทํางานของแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="0dca2-198">Click the edit app pencil icon to open the template app's workspace.</span></span>
    1. <span data-ttu-id="0dca2-199">ในพื้นที่ทํางานของแอปเทมเพลต ให้เลือก **ตัวเลือกเพิ่มเติม (...)** จากนั้นเลือก **ยกเลิกการเผยแพร่แอป**</span><span class="sxs-lookup"><span data-stu-id="0dca2-199">In the template app workspace, select **More option (...)**, and then choose **Unpublish App**.</span></span>

        ![ภาพหน้าจอของตัวเลือกการยกเลิกการเผยแพร่แอป](media/service-template-apps-install-distribute/power-bi-template-app-unpublish.png)


## <a name="next-steps"></a><span data-ttu-id="0dca2-201">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="0dca2-201">Next steps</span></span>

[<span data-ttu-id="0dca2-202">สร้างพื้นที่ทำงานกับเพื่อนร่วมงานของคุณใน Power BI</span><span class="sxs-lookup"><span data-stu-id="0dca2-202">Create workspaces with your colleagues in Power BI</span></span>](../collaborate-share/service-create-the-new-workspaces.md)
