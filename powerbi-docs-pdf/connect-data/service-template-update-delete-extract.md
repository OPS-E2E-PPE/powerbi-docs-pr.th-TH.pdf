---
title: อัปเดต ลบ และแยกแอปแม่แบบใน Power BI
description: วิธีการอัปเดต ลบ และแยกแอปแม่แบบ
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: how-to
ms.date: 05/04/2020
ms.openlocfilehash: 2eb4df96db51ccbf3308315130fdaa2de85df240
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96392139"
---
# <a name="update-delete-and-extract-template-app"></a><span data-ttu-id="37190-103">อัปเดต ลบ และแยกแอปแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="37190-103">Update, delete, and extract template app</span></span>

<span data-ttu-id="37190-104">หลังจากที่แอปของคุณอยู่ในผลิต คุณสามารถเริ่มต้นในขั้นตอนการทดสอบโดยไม่รบกวนแอปในการผลิต</span><span class="sxs-lookup"><span data-stu-id="37190-104">Now that your app is in production, you can start over in the test phase, without disrupting the app in production.</span></span>
## <a name="update-your-app"></a><span data-ttu-id="37190-105">อัปเดตแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="37190-105">Update your app</span></span>

<span data-ttu-id="37190-106">หากคุณทำการแก้ไขเดสก์ทอป Power BI ให้เริ่มจากขั้นตอนที่ (1)</span><span class="sxs-lookup"><span data-stu-id="37190-106">If you made the changes in Power BI Desktop, start at step (1).</span></span> <span data-ttu-id="37190-107">หากคุณไม่ได้ทำการเปลี่ยนแปลงใด ๆ ในเดสก์ทอป Power BI ให้เริ่มขั้นตอนที่ (4)</span><span class="sxs-lookup"><span data-stu-id="37190-107">If you did not make the changes in Power BI Desktop, start at step (4).</span></span>

1. <span data-ttu-id="37190-108">อัปโหลดชุดข้อมูลที่อัปเดตแล้วและเขียนทับชุดข้อมูลที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="37190-108">Upload the updated dataset and overwrite the existing dataset.</span></span> <span data-ttu-id="37190-109">**อย่าลืมใช้ชื่อชุดข้อมูลให้เหมือนกัน**</span><span class="sxs-lookup"><span data-stu-id="37190-109">**Make sure to use the exact same dataset name**.</span></span> <span data-ttu-id="37190-110">การใช้ชื่ออื่นจะทำให้เกิดชุดข้อมูลใหม่สำหรับผู้ใช้ที่กำลังอัปเดตแอพ</span><span class="sxs-lookup"><span data-stu-id="37190-110">Using a different name will create a new dataset for users that are updating the app.</span></span>
<span data-ttu-id="37190-111">![สกรีนช็อตแสดง Power BI ที่มีการอัปเดตแอปแม่แบบด้วยชุดข้อมูลที่เลือก](media/service-template-apps-update-extract-delete/power-bi-template-app-upload-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="37190-111">![Screenshot shows the Power B I Updating a template app with Dataset selected.](media/service-template-apps-update-extract-delete/power-bi-template-app-upload-dataset.png)</span></span>
1. <span data-ttu-id="37190-112">นำเข้าไฟล์ pbix จากคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="37190-112">Import the pbix file from your computer.</span></span>
<span data-ttu-id="37190-113">![สกรีนช็อตแสดงหน้ารับข้อมูลที่มีรับถูกเรียกออกมาภายใต้ไฟล์](media/service-template-apps-update-extract-delete/power-bi-template-app-upload-dataset2.png)</span><span class="sxs-lookup"><span data-stu-id="37190-113">![Screenshot shows the Get Data page with Get called out under Files.](media/service-template-apps-update-extract-delete/power-bi-template-app-upload-dataset2.png)</span></span>
1. <span data-ttu-id="37190-114">ยืนยันการเขียนทับ</span><span class="sxs-lookup"><span data-stu-id="37190-114">Confirm the overwrite.</span></span>
<span data-ttu-id="37190-115">![สกรีนช็อตแสดงข้อความการยืนยันว่าชุดข้อมูล A ที่มีชื่อเดียวกันมีอยู่และมีตัวเลือกให้แทนที่](media/service-template-apps-update-extract-delete/power-bi-template-app-upload-dataset3.png)</span><span class="sxs-lookup"><span data-stu-id="37190-115">![Screenshot shows a confirmation message that A dataset with the same name exists and the option to replace it.](media/service-template-apps-update-extract-delete/power-bi-template-app-upload-dataset3.png)</span></span>

1. <span data-ttu-id="37190-116">ในบานหน้าต่าง **การจัดการวางจำหน่าย** เลือก **สร้างแอป**</span><span class="sxs-lookup"><span data-stu-id="37190-116">In the **Release management** pane, select **Create app**.</span></span>
1. <span data-ttu-id="37190-117">ย้อนกลับผ่านขั้นตอนการสร้างแอป</span><span class="sxs-lookup"><span data-stu-id="37190-117">Go back through the app creation process.</span></span>
1. <span data-ttu-id="37190-118">หลังจากที่คุณได้ตั้งค่า **Branding**, **เนื้อหา**, **ควบคุม** และ **Access** คุณเลือก **สร้างแอป** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="37190-118">After you've set **Branding**, **Content**, **Control**, and **Access**, select **Create app** again.</span></span>
1. <span data-ttu-id="37190-119">เลือก **ปิด** และกลับไปยัง **การจัดการวางจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="37190-119">Select **Close** and go back to **Release management**.</span></span>

   <span data-ttu-id="37190-120">คุณเห็นว่าคุณมีสองเวอร์ชันในขณะนี้: เวอร์ชันในผลิต รวมถึงเวอร์ชันใหม่ในการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="37190-120">You see you have two versions now: The version in production, plus a new version in testing.</span></span>

    ![ทั้งสองเวอร์ชันของแอปแม่แบบ](media/service-template-apps-update-extract-delete/power-bi-template-app-update1.png)

1. <span data-ttu-id="37190-122">เมื่อคุณพร้อมที่จะเลื่อนระดับแอปของคุณไปยังการผลิตล่วงหน้าสำหรับการทดสอบภายนอกผู้เช่าของคุณเพิ่มเติม **ย้อนกลับไปที่บานหน้าต่างการจัดการวางจำหน่าย** **และเลือก เลื่อนแอป ถัดจากการทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="37190-122">When you're ready to promote your app to pre-production for further testing outside your tenant, go back to the Release Management pane and select **Promote app** next to **Testing**.</span></span>

   <span data-ttu-id="37190-123">ขณะนี้คุณมีเวอร์ชันในการผลิตและเวอร์ชันในการผลิตล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="37190-123">You now have a version in production and a version in pre-production.</span></span>

   ![ปุ่มเลื่อนระดับทั้งสองเวอร์ชันของแอปแม่แบบจะเป็นสีเทา](media/service-template-apps-update-extract-delete/power-bi-template-app-update2.png)

   <span data-ttu-id="37190-125">ขณะนี้ลิงก์ของคุณได้ออนไลน์แล้ว</span><span class="sxs-lookup"><span data-stu-id="37190-125">Your link is now live.</span></span> <span data-ttu-id="37190-126">**โปรดทราบว่าปุ่มเลื่อนระดับแอปในระยะก่อนการผลิตจะเป็นสีเทา** นี่คือเพื่อป้องกันการเขียนทับลิงก์การผลิตแบบสดไปยังเวอร์ชันแอปปัจจุบันโดยไม่ตั้งใจก่อนที่ Cloud Partner Portal จะตรวจสอบและอนุมัติเวอร์ชันแอปใหม่</span><span class="sxs-lookup"><span data-stu-id="37190-126">**Note that the Promote app button at the pre-production stage is greyed out**. This is to prevent accidentally overwriting the live production link to the current app version before the Cloud Partner Portal has validated and approved the new app version.</span></span>

1. <span data-ttu-id="37190-127">ส่งลิงก์ของคุณไปยังพอร์ทัล Cloud Partner (CPP) อีกครั้งโดยทำตามขั้นตอนที่ [การอัปเดตข้อเสนอของแอป Power BI](/azure/marketplace/cloud-partner-portal/power-bi/cpp-update-existing-offer)</span><span class="sxs-lookup"><span data-stu-id="37190-127">Submit your link again to the Cloud Partner Portal (CPP) by following the steps at [Power BI App offer update](/azure/marketplace/cloud-partner-portal/power-bi/cpp-update-existing-offer).</span></span> <span data-ttu-id="37190-128">จากพอร์ทัล Cloud Parnter คุณจะต้อง **เผยแพร่** ข้อเสนอของคุณอีกครั้ง และผ่านการตรวจสอบและอนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="37190-128">In the Cloud Partner Portal, you must **publish** your offer again and have it validated and approved.</span></span>

   <span data-ttu-id="37190-129">เมื่อข้อเสนอของคุณได้รับอนุมัติแล้ว ปุ่มเลื่อนระดับแอปจะเปิดใช้งานอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="37190-129">When your offer is approved, the Promote app button will become active again.</span></span> 
1. <span data-ttu-id="37190-130">เลื่อนระดับแอปของคุณไปยังขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="37190-130">Promote your app to the production stage.</span></span>
   
### <a name="update-behavior"></a><span data-ttu-id="37190-131">อัปเดตพฤติกรรม</span><span class="sxs-lookup"><span data-stu-id="37190-131">Update behavior</span></span>

1. <span data-ttu-id="37190-132">การอัปเดตแอปจะช่วยให้ผู้ติดตั้งแอปเทมเพลตสามารถ[อัปเดตแอปเทมเพลต](service-template-apps-install-distribute.md#update-a-template-app)ในพื้นที่ทำงานที่ติดตั้งไว้แล้วโดยที่การกำหนดค่าการเชื่อมต่อไม่หายไป</span><span class="sxs-lookup"><span data-stu-id="37190-132">Updating the app will allow the installer of the template app to [Update a template app](service-template-apps-install-distribute.md#update-a-template-app) in the already installed workspace without losing the connection configuration.</span></span>
1. <span data-ttu-id="37190-133">ดูใน[รูปแบบการเขียนทับ](service-template-apps-install-distribute.md#overwrite-behavior)ของตัวติดตั้งเพื่อเรียนรู้เกี่ยวกับการปรับเปลี่ยนในชุดข้อมูลที่จะมีผลต่อแอปเทมเพลตที่ติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="37190-133">See installer [overwrite behavior](service-template-apps-install-distribute.md#overwrite-behavior) to learn how changes in the dataset affect the installed template app.</span></span>
1. <span data-ttu-id="37190-134">ขณะอัปเดต (เขียนทับ) แอปเทเพลต จะมีการย้อนกลับไปที่ข้อมูลตัวอย่างและทำการเชื่อมต่อใหม่อัตโนมัติกับการกำหนดค่าของผู้ใช้ (พารามิเตอร์และการรับรองความถูกต้อง)</span><span class="sxs-lookup"><span data-stu-id="37190-134">When updating (overwriting) a template app, it first reverts back to sample data and will automatically reconnect with user's configuration (parameters & authentication).</span></span> <span data-ttu-id="37190-135">จนกว่าการรีเฟรชจะเสร็จสิ้น รายงาน แดชบอร์ดและแอปของหน่วยงานจะมีมีอยู่ในแบนเนอร์ข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="37190-135">Until refresh is complete, the reports, dashboards, and org app will present the sample data banner.</span></span>
1. <span data-ttu-id="37190-136">หากคุณเพิ่มพารามิเตอร์การสืบค้นไปยังชุดข้อมูลที่อัพปเดตที่ต้องการข้อมูลจากผู้ใช้ - คุณจะต้องทำเครื่องหมายในช่อง *จำเป็น*</span><span class="sxs-lookup"><span data-stu-id="37190-136">If you added a new query parameter to the updated dataset that requires users input - you must check the *required* check box.</span></span> <span data-ttu-id="37190-137">ซึ่งจะเป็นการแจ้งตัวติดตั้งในสตริงการเชื่อมต่อหลังจากทำการอัปเดตแอพ</span><span class="sxs-lookup"><span data-stu-id="37190-137">This will prompt the installer with the connection string after updating the app.</span></span>
 <span data-ttu-id="37190-138">![พารามิเตอร์ที่จำเป็น](media/service-template-apps-update-extract-delete/power-bi-template-app-upload-dataset4.png)</span><span class="sxs-lookup"><span data-stu-id="37190-138">![required parameters](media/service-template-apps-update-extract-delete/power-bi-template-app-upload-dataset4.png)</span></span>

## <a name="extract-workspace"></a><span data-ttu-id="37190-139">แยกพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="37190-139">Extract workspace</span></span>
<span data-ttu-id="37190-140">ด้วยความสามารถในการแยกการย้อนกลับเป็นเวอร์ชันก่อนหน้าของแอปเทมเพลตสามารถทำได้ง่ายขึ้น </span><span class="sxs-lookup"><span data-stu-id="37190-140">Rolling back to the previous version of a template app is now easier than ever with the extract capability.</span></span> <span data-ttu-id="37190-141">ขั้นตอนต่อไปนี้จะแยกเวอร์ชันแอปเฉพาะจากขั้นตอนต่าง ๆ ที่เผยแพร่ลงในพื้นที่ทำงานใหม่:</span><span class="sxs-lookup"><span data-stu-id="37190-141">The following steps will extract a specific app version from various release stages into a new workspace:</span></span>

1. <span data-ttu-id="37190-142">ในบานหน้าต่างการจัดการแผยแพร่ กด **(...)** เพิ่มจากนั้น **แยก**</span><span class="sxs-lookup"><span data-stu-id="37190-142">In the release management pane, press more **(...)** and then **Extract**.</span></span>

    <span data-ttu-id="37190-143">![สกรีนช็อตแสดงบานหน้าต่างการจัดการการวางจำหน่ายพร้อมการแยกที่เลือกจากเมนู](media/service-template-apps-update-extract-delete/power-bi-template-app-extract.png)</span><span class="sxs-lookup"><span data-stu-id="37190-143">![Screenshot shows the Release Management pane with Extract selected from a menu.](media/service-template-apps-update-extract-delete/power-bi-template-app-extract.png)</span></span>
    <span data-ttu-id="37190-144">![สกรีนช็อตแสดงข้อความยืนยันเพื่อแยกแอปนี้](media/service-template-apps-update-extract-delete/power-bi-template-app-extract-dialog.png)</span><span class="sxs-lookup"><span data-stu-id="37190-144">![Screenshot shows confirmation message to Extract this app.](media/service-template-apps-update-extract-delete/power-bi-template-app-extract-dialog.png)</span></span>
2. <span data-ttu-id="37190-145">ในกล่องโต้ตอบ ใส่ชื่อสำหรับพื้นที่ทำงานที่จะแยกออกมา</span><span class="sxs-lookup"><span data-stu-id="37190-145">In dialog box, enter the name for extracted workspace.</span></span> <span data-ttu-id="37190-146">พื้นที่ทำงานใหม่จะถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="37190-146">a new workspace will be added.</span></span>

<span data-ttu-id="37190-147">รีเซ็ตการกำหนดรุ่นของพื้นที่ทำงานใหม่ของคุณ คุณสามารถพัฒนาและกระจายแอปเทมเพลตจากพื้นที่ทำงานใหม่แยกออกมา</span><span class="sxs-lookup"><span data-stu-id="37190-147">Your new workspace versioning resets and you can continue to develop and distribute the template app from the newly extracted workspace.</span></span>

## <a name="delete-template-app-version"></a><span data-ttu-id="37190-148">ลบเวอรชันแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="37190-148">Delete template app version</span></span>
<span data-ttu-id="37190-149">เทมแพลตพื้นที่ทำงานเป็นแหล่งข้อมูลของแอปเทมเพลตแบบกระจายที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="37190-149">A template workspace is the source of an active distributed template app.</span></span> <span data-ttu-id="37190-150">เพื่อปกป้องผู้ใช้แอปเทมเพลต ผู้ใช้จะไม่สามารถลบพื้นที่ทำงานโดยไม่ต้องลบเวอร์ชันแอปที่สร้างขึ้นทั้งหมดในพื้นที่ทำงานก่อนหน้านี้ได้</span><span class="sxs-lookup"><span data-stu-id="37190-150">To protect the template app users, it's not possible to delete a workspace without first removing all the created app versions in the workspace.</span></span>
<span data-ttu-id="37190-151">การลบเวอร์ชันแอปยังเป็นการลบลบ URL ของแอปที่ไม่ทำงานอีกแล้วไปด้วย</span><span class="sxs-lookup"><span data-stu-id="37190-151">Deleting an app version also deletes the app url that will no longer work.</span></span>

1. <span data-ttu-id="37190-152">ในบานหน้าต่างการจัดการเผยแพร่ กดเลือกจุดไข่ปลา **(...)** จากนั้น **ลบ**</span><span class="sxs-lookup"><span data-stu-id="37190-152">In the release management pane, press select the ellipsis **(...)** and then **Delete**.</span></span>
 <span data-ttu-id="37190-153">![สกรีนช็อตแสดงบานหน้าต่างการจัดการการวางจำหน่ายที่มีการลบที่เลือกจากเมนู](media/service-template-apps-update-extract-delete/power-bi-template-app-delete.png)
  ![สกรีนช็อตแสดงข้อความยืนยันเพื่อลบแอปนี้](media/service-template-apps-update-extract-delete/power-bi-template-app-delete-dialog.png)</span><span class="sxs-lookup"><span data-stu-id="37190-153">![Screenshot shows the Release Management pane with Delete selected from a menu.](media/service-template-apps-update-extract-delete/power-bi-template-app-delete.png)
![Screenshot shows confirmation message to Delete this app.](media/service-template-apps-update-extract-delete/power-bi-template-app-delete-dialog.png)</span></span>

>[!NOTE]
><span data-ttu-id="37190-154">ต้องแน่ใจว่าจะไม่ลบเวอร์ชันแอปหรือ **AppSource** ที่ลูกค้ากำลังใช้งานอยู่หรือแอปเหล่านั้นไม่สามารถใช้งานได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="37190-154">Make sure not to delete app version which are being used by customers or **AppSource** or they will no longer work.</span></span>

## <a name="next-steps"></a><span data-ttu-id="37190-155">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="37190-155">Next steps</span></span>

<span data-ttu-id="37190-156">ดูวิธีการที่ลูกค้าของคุณโต้ตอบกับแอปแม่แบบของคุณใน[ติดตั้ง กำหนดเอง และเผยแพรแอปแม่แบบในองค์กรของคุณ](service-template-apps-install-distribute.md)</span><span class="sxs-lookup"><span data-stu-id="37190-156">See how your customers interact with your template app in [Install, customize, and distribute template apps in your organization](service-template-apps-install-distribute.md).</span></span>

<span data-ttu-id="37190-157">ดู[ข้อเสนอแอปพลิเคชัน BI Power](/azure/marketplace/cloud-partner-portal/power-bi/cpp-power-bi-offer)สำหรับรายละเอียดเกี่ยวกับการแจกจ่ายแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="37190-157">See the [Power BI Application offer](/azure/marketplace/cloud-partner-portal/power-bi/cpp-power-bi-offer) for details on distributing your app.</span></span>