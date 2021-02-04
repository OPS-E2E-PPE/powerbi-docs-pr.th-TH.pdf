---
title: วิธีการกำหนดค่าการรีเฟรชตามกำหนดเวลา ของรายงาน Power BI
description: เมื่อต้องการรีเฟรชข้อมูลในรายงาน Power BI ของคุณ แผนการรีเฟรชตามกำหนดเวลาต้องถูกสร้างขึ้น
author: maggiesMSFT
ms.author: maggies
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.date: 06/10/2020
ms.openlocfilehash: 95119cf6ebebbf527245f5b75f0da541c1f87aef
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96386331"
---
# <a name="how-to-configure-power-bi-report-scheduled-refresh"></a><span data-ttu-id="ebb47-103">วิธีการกำหนดค่าการรีเฟรชตามกำหนดเวลา ของรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="ebb47-103">How to configure Power BI report scheduled refresh</span></span>
<span data-ttu-id="ebb47-104">ในการรีเฟรชข้อมูลในรายงาน Power BI ในเซิร์ฟเวอร์รายงาน Power BI คุณต้องสร้างแผนการรีเฟรชตามกำหนดเวลา</span><span class="sxs-lookup"><span data-stu-id="ebb47-104">To refresh data in your Power BI report in Power BI Report Server, you must create a scheduled refresh plan.</span></span> <span data-ttu-id="ebb47-105">คุณสร้างแผนนี้ได้ในพื้นที่ *จัดการ* ของรายงาน Power BI บนเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="ebb47-105">You create this plan in the *Manage* area of a Power BI report on the report server.</span></span>

![รีเฟรชตามกำหนดเวลาที่สำเร็จ ของรายงาน Power BI](media/configure-scheduled-refresh/scheduled-refresh-success.png)

## <a name="configure-data-source-credentials"></a><span data-ttu-id="ebb47-107">กำหนดค่าข้อมูลประจำตัวของแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ebb47-107">Configure data source credentials</span></span>
<span data-ttu-id="ebb47-108">คุณต้องได้รับการอนุญาตที่จำเป็นในการสร้างแผนการรีเฟรชตามกำหนดเวลา</span><span class="sxs-lookup"><span data-stu-id="ebb47-108">You need the necessary permissions to create a scheduled refresh plan.</span></span> <span data-ttu-id="ebb47-109">สิทธิ์ได้รับการกำหนดไว้ในนิยามบทบาทสำหรับเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="ebb47-109">Permissions are defined in the role definitions for the report server.</span></span> <span data-ttu-id="ebb47-110">ดู [นิยามบทบาท - บทบาทที่กำหนดไว้ล่วงหน้า](/sql/reporting-services/security/role-definitions-predefined-roles) ในเอกสารคู่มือ SQL Server Reporting Services สำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="ebb47-110">See [Role definitions - predefined roles](/sql/reporting-services/security/role-definitions-predefined-roles) in the SQL Server Reporting Services documentation for details.</span></span>

<span data-ttu-id="ebb47-111">ก่อนที่จะสร้างแผนการรีเฟรชตามกำหนดเวลา คุณจำเป็นต้องตั้งค่าข้อมูลประจำตัวสำหรับ **แต่ละแหล่งข้อมูล** ที่ใช้ในรายงาน Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ebb47-111">Prior to creating a schedule data refresh plan, you need to set the credentials for **each data source** used in your Power BI report.</span></span>

1. <span data-ttu-id="ebb47-112">ในพอร์ทัลของเว็บ คลิกขวาบนรายงาน Power BI และเลือก **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="ebb47-112">In the web portal, right-click on the Power BI report and select **Manage**.</span></span>
   
    ![เลือกจัดการ จากเมนูบริบทของรายงาน Power BI](media/configure-scheduled-refresh/manage-power-bi-report.png)
2. <span data-ttu-id="ebb47-114">ในเมนูทางด้านซ้าย เลือกแท็บ **แหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="ebb47-114">In the left menu, select the **Data sources** tab.</span></span>
3. <span data-ttu-id="ebb47-115">สำหรับแต่ละแหล่งข้อมูลที่ปรากฏขึ้น เลือกชนิดของการรับรองความถูกต้องที่จะใช้เมื่อเชื่อมต่อกับแหล่งข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="ebb47-115">For each data source that appears, choose the type of authentication to use when connecting to that data source.</span></span> <span data-ttu-id="ebb47-116">ใส่ข้อมูลประจำตัวที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="ebb47-116">Enter the appropriate credentials.</span></span>
   
    ![ข้อมูลประจำตัวของแหล่งข้อมูล ในหน้าจอจัดการรายงาน](media/configure-scheduled-refresh/data-source-credentials.png)

## <a name="creating-a-schedule-refresh-plan"></a><span data-ttu-id="ebb47-118">การสร้างแผนรีเฟรชตามกำหนดเวลา</span><span class="sxs-lookup"><span data-stu-id="ebb47-118">Creating a Schedule Refresh Plan</span></span>
<span data-ttu-id="ebb47-119">ทำตามขั้นตอนเหล่านี้ เพื่อสร้างแผนรีเฟรชตามกำหนดเวลา</span><span class="sxs-lookup"><span data-stu-id="ebb47-119">Follow these steps to create a scheduled refresh plan.</span></span>

1. <span data-ttu-id="ebb47-120">ในพอร์ทัลของเว็บ คลิกขวาบนรายงาน Power BI และเลือก **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="ebb47-120">In the web portal, right-click on the Power BI report and select **Manage**.</span></span>
   
    ![เลือกจัดการ จากเมนูบริบทของรายงาน Power BI](media/configure-scheduled-refresh/manage-power-bi-report.png)
2. <span data-ttu-id="ebb47-122">ในเมนูทางด้านซ้าย เลือกแท็บ **รีเฟรชตามกำหนดเวลา**</span><span class="sxs-lookup"><span data-stu-id="ebb47-122">In the left menu, select the **Scheduled refresh** tab.</span></span>
3. <span data-ttu-id="ebb47-123">บนหน้า **รีเฟรชตามกำหนดเวลา** เลือก **สร้างแผนรีเฟรชตามกำหนดเวลาใหม่**</span><span class="sxs-lookup"><span data-stu-id="ebb47-123">On the **Scheduled refresh** page, select **New scheduled refresh plan**.</span></span>
   
    ![แผนรีเฟรชตามกำหนดเวลาใหม่](media/configure-scheduled-refresh/new-scheduled-refresh-plan.png)
4. <span data-ttu-id="ebb47-125">บนหน้า **สร้างแผนรีเฟรชตามกำหนดเวลาใหม่** ใส่คำอธิบาย และตั้งค่ากำหนดเวลา สำหรับเวลาที่คุณต้องการให้รูปแบบข้อมูลของคุณถูกรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="ebb47-125">On the **New Scheduled Refresh Plan** page, enter a description and set a schedule for when you want your data model to be refreshed.</span></span>
5. <span data-ttu-id="ebb47-126">เลือก **สร้างแผนรีเฟรชตามกำหนดเวลา** เมื่อเสร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="ebb47-126">Select **Create scheduled refresh plan** when done.</span></span>
   
    ![สร้างแผนรีเฟรชตามกำหนดเวลา](media/configure-scheduled-refresh/create-scheduled-refresh-plan.png)

## <a name="modifying-a-schedule-refresh-plan"></a><span data-ttu-id="ebb47-128">การปรับเปลี่ยนแผนรีเฟรชตามกำหนดเวลา</span><span class="sxs-lookup"><span data-stu-id="ebb47-128">Modifying a Schedule Refresh Plan</span></span>
<span data-ttu-id="ebb47-129">การปรับเปลี่ยนแผนรีเฟรชตามกำหนดเวลา จะคล้ายกับเวลาสร้างแผน</span><span class="sxs-lookup"><span data-stu-id="ebb47-129">Modifying a scheduled refresh plan is similar to creating one.</span></span>

1. <span data-ttu-id="ebb47-130">ในพอร์ทัลของเว็บ คลิกขวาบนรายงาน Power BI และเลือก **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="ebb47-130">In the web portal, right-click on the Power BI report and select **Manage**.</span></span>
   
    ![เลือกจัดการ จากเมนูบริบทของรายงาน Power BI](media/configure-scheduled-refresh/manage-power-bi-report.png)
2. <span data-ttu-id="ebb47-132">ในเมนูทางด้านซ้าย เลือกแท็บ **รีเฟรชตามกำหนดเวลา**</span><span class="sxs-lookup"><span data-stu-id="ebb47-132">In the left menu, select the **Scheduled refresh** tab.</span></span>
3. <span data-ttu-id="ebb47-133">บนหน้า **รีเฟรชตามกำหนดเวลา** เลือก **แก้ไข** ข้างแผนการรีเฟรชที่คุณต้องการจัดการ</span><span class="sxs-lookup"><span data-stu-id="ebb47-133">On the **Scheduled refresh** page, select **Edit** beside the refresh plan you want to manage.</span></span>
   
    ![เลือกแก้ไข ที่อยู่ติดกับแผนที่คุณต้องการแก้ไข](media/configure-scheduled-refresh/edit-scheduled-refresh-plan.png)
4. <span data-ttu-id="ebb47-135">บนหน้า **แก้ไขแผนรีเฟรชตามกำหนดเวลา** ใส่คำอธิบาย และตั้งค่ากำหนดเวลา สำหรับเวลาที่คุณต้องการให้รูปแบบข้อมูลของคุณถูกรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="ebb47-135">On the **Edit Scheduled Refresh Plan** page, enter a description and set a schedule for when you want your data model to be refreshed.</span></span>
5. <span data-ttu-id="ebb47-136">เลือก **นำไปใช้** เมื่อทำเสร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="ebb47-136">Select **Apply** when done.</span></span>
   
    ![หน้าแก้ไขแผนรีเฟรชตามกำหนดเวลาจะคล้ายกับหน้าจอสำหรับสร้าง](media/configure-scheduled-refresh/edit-scheduled-refresh-plan-page.png)

## <a name="viewing-the-status-of-schedule-refresh-plan"></a><span data-ttu-id="ebb47-138">ดูสถานะของแผนรีเฟรชตามกำหนดเวลา</span><span class="sxs-lookup"><span data-stu-id="ebb47-138">Viewing the status of Schedule Refresh Plan</span></span>
<span data-ttu-id="ebb47-139">ดูสถานะของแผนรีเฟรชตามกำหนดเวลาในพอร์ทัลของเว็บ</span><span class="sxs-lookup"><span data-stu-id="ebb47-139">View the status of a schedule refresh plan in the web portal.</span></span>

1. <span data-ttu-id="ebb47-140">ในพอร์ทัลของเว็บ คลิกขวาบนรายงาน Power BI และเลือก **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="ebb47-140">In the web portal, right-click on the Power BI report and select **Manage**.</span></span>
   
    ![เลือกจัดการ จากเมนูบริบทของรายงาน Power BI](media/configure-scheduled-refresh/manage-power-bi-report.png)
2. <span data-ttu-id="ebb47-142">ในเมนูทางด้านซ้าย เลือกแท็บ **รีเฟรชตามกำหนดเวลา**</span><span class="sxs-lookup"><span data-stu-id="ebb47-142">In the left menu, select the **Scheduled refresh** tab.</span></span>
3. <span data-ttu-id="ebb47-143">บนหน้า **รีเฟรชตามกำหนดเวลา** คอลัมน์ด้านขวาสุดจะแสดงสถานะของแผน</span><span class="sxs-lookup"><span data-stu-id="ebb47-143">On the **Scheduled refresh** page, the right most column displays the status of a plan.</span></span>
   
   | <span data-ttu-id="ebb47-144">**สถานะ**</span><span class="sxs-lookup"><span data-stu-id="ebb47-144">**Status**</span></span> | <span data-ttu-id="ebb47-145">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="ebb47-145">**Description**</span></span> |
   | --- | --- |
   | <span data-ttu-id="ebb47-146">แผนรีเฟรชตามกำหนดเวลาใหม่</span><span class="sxs-lookup"><span data-stu-id="ebb47-146">New Scheduled Refresh Plan</span></span> |<span data-ttu-id="ebb47-147">แผนถูกสร้างขึ้นแล้ว แต่ยังไม่เคยเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ebb47-147">The plan has been created but has not ran.</span></span> |
   | <span data-ttu-id="ebb47-148">กำลังรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="ebb47-148">Refreshing</span></span> |<span data-ttu-id="ebb47-149">กระบวนการรีเฟรชได้เริ่มขึ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="ebb47-149">The refresh process has started.</span></span> |
   | <span data-ttu-id="ebb47-150">กำลังสตรีมรูปแบบไปยังเซิร์ฟเวอร์การวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="ebb47-150">Streaming model to Analysis Server</span></span> |<span data-ttu-id="ebb47-151">กำลังคัดลอกรูปแบบ จากฐานข้อมูลแค็ตตาล็อกเซิร์ฟเวอร์รายงาน ไปยังอินสแตนซ์ของ Analysis Services ที่ถูกโฮสต์</span><span class="sxs-lookup"><span data-stu-id="ebb47-151">Copying the model from the report server catalog database to the hosted Analysis Services instance.</span></span> |
   | <span data-ttu-id="ebb47-152">กำลังรีเฟรชข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ebb47-152">Refreshing data</span></span> |<span data-ttu-id="ebb47-153">กำลังรีเฟรชข้อมูลภายในรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="ebb47-153">Refreshing the data within the model.</span></span> |
   | <span data-ttu-id="ebb47-154">กำลังเอาข้อมูลประจำตัวออกจากรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="ebb47-154">Removing credentials from the model</span></span> |<span data-ttu-id="ebb47-155">เอาข้อมูลประจำตัวที่ใช้ในการเชื่อมต่อกับแหล่งข้อมูลออกจากรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="ebb47-155">Removed the credentials used to connect to the data source from the model.</span></span> |
   | <span data-ttu-id="ebb47-156">กำลังบันทึกรูปแบบไปยังแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="ebb47-156">Saving model to the catalog</span></span> |<span data-ttu-id="ebb47-157">การรีเฟรชข้อมูลเสร็จสมบูรณ์ และรูปแบบปรับปรุงใหม่กำลังถูกบันทึกกลับไปยังฐานข้อมูลแค็ตตาล็อกของเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="ebb47-157">Refreshing of data is complete and the refreshed model is being saved back to the report server catalog database.</span></span> |
   | <span data-ttu-id="ebb47-158">เสร็จสมบูรณ์แล้ว: รีเฟรชข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ebb47-158">Completed: Data Refresh</span></span> |<span data-ttu-id="ebb47-159">รีเฟรชเสร็จสิ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="ebb47-159">Refresh is done.</span></span> |
   | <span data-ttu-id="ebb47-160">ข้อผิดพลาด:</span><span class="sxs-lookup"><span data-stu-id="ebb47-160">Error:</span></span> |<span data-ttu-id="ebb47-161">มีข้อผิดพลาดเกิดขึ้นระหว่างการรีเฟรช และแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="ebb47-161">An error occurred during refresh and is displayed.</span></span> |

<span data-ttu-id="ebb47-162">เว็บเพจนี้ต้องมีการรีเฟรชเพื่อดูสถานะปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="ebb47-162">The web page must be refreshed to see the current status.</span></span> <span data-ttu-id="ebb47-163">สถานะจะไม่เปลี่ยนแปลงโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ebb47-163">The status will not change automatically.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ebb47-164">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="ebb47-164">Next steps</span></span>
<span data-ttu-id="ebb47-165">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับการสร้างและปรับเปลี่ยนกำหนดเวลา ดู[สร้าง แก้ไข และลบกำหนดเวลา](/sql/reporting-services/subscriptions/create-modify-and-delete-schedules)</span><span class="sxs-lookup"><span data-stu-id="ebb47-165">To learn more about creating and modifying schedules, see [Create, modify, and delete schedules](/sql/reporting-services/subscriptions/create-modify-and-delete-schedules).</span></span>

<span data-ttu-id="ebb47-166">สำหรับข้อมูลเกี่ยวกับวิธีการแก้ไขปัญหารีเฟรชตามกำหนดเวลา ดู[แก้ไขปัญหารีเฟรชตามกำหนดเวลาในรีพอร์ตเซิร์ฟเวอร์ Power BI](scheduled-refresh-troubleshoot.md)</span><span class="sxs-lookup"><span data-stu-id="ebb47-166">For information on how to troubleshoot scheduled refresh, see [Troubleshoot scheduled refresh in Power BI Report Server](scheduled-refresh-troubleshoot.md).</span></span>

<span data-ttu-id="ebb47-167">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="ebb47-167">More questions?</span></span> [<span data-ttu-id="ebb47-168">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="ebb47-168">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)