---
title: สร้างแดชบอร์ด Power BI จากรายงาน
description: สร้างแดชบอร์ด Power BI จากรายงาน
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 07/17/2019
ms.openlocfilehash: 4482fc3317b1ca10589645f19c22af31c8f8a80a
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96395566"
---
# <a name="create-a-power-bi-dashboard-from-a-report"></a><span data-ttu-id="a52ed-103">สร้างแดชบอร์ด Power BI จากรายงาน</span><span class="sxs-lookup"><span data-stu-id="a52ed-103">Create a Power BI dashboard from a report</span></span>
<span data-ttu-id="a52ed-104">คุณได้อ่าน[บทนำเกี่ยวกับแดชบอร์ดใน Power BI](service-dashboards.md) แล้วและตอนนี้ คุณต้องการสร้างของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="a52ed-104">You've read [Introduction to dashboards in Power BI](service-dashboards.md), and now you want to create your own.</span></span> <span data-ttu-id="a52ed-105">มีหลายวิธีในการสร้างแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="a52ed-105">There are many different ways to create a dashboard.</span></span> <span data-ttu-id="a52ed-106">ตัวอย่างเช่น คุณสามารถสร้างจากรายงาน จาก scratch จากชุดข้อมูล หรือโดยการทำซ้ำแดชบอร์ดที่มีอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="a52ed-106">For example, you can create a dashboard from a report, from scratch, from a dataset, or by duplicating an existing dashboard.</span></span>  

<span data-ttu-id="a52ed-107">เราจะเริ่มต้นโดยการสร้างแดชบอร์ดที่ง่ายและรวดเร็วซึ่งปักหมุดการจัดรูปแบบการแสดงข้อมูลจากรายงานที่มีการทำขึ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="a52ed-107">We start by creating a quick and easy dashboard that pins visualizations from a report that's already been built.</span></span> 

<span data-ttu-id="a52ed-108">หลังจากเสร็จสิ้นบทความนี้ คุณจะเข้าใจเรื่องต่อไปนี้เป็นอย่างดี:</span><span class="sxs-lookup"><span data-stu-id="a52ed-108">After you complete this article, you'll have a good understanding of:</span></span>
- <span data-ttu-id="a52ed-109">ความสัมพันธ์ระหว่างแดชบอร์ดและรายงาน</span><span class="sxs-lookup"><span data-stu-id="a52ed-109">The relationship between dashboards and reports</span></span>
- <span data-ttu-id="a52ed-110">วิธีการเปิดมุมมองการแก้ไขในตัวแก้ไขรายงาน</span><span class="sxs-lookup"><span data-stu-id="a52ed-110">How to open Editing view in the report editor</span></span>
- <span data-ttu-id="a52ed-111">วิธีการปักหมุดไทล์</span><span class="sxs-lookup"><span data-stu-id="a52ed-111">How to pin tiles</span></span> 
- <span data-ttu-id="a52ed-112">วิธีการนำทางระหว่างแดชบอร์ดและรายงาน</span><span class="sxs-lookup"><span data-stu-id="a52ed-112">How to navigate between a dashboard and a report</span></span> 
 
![สกรีนช็อตแสดงแดชบอร์ด Power BI พร้อมการแสดงผลข้อมูลด้วยภาพหลายรายการ](media/service-dashboard-create/power-bi-completed-dashboard-small.png)

> [!NOTE] 
> <span data-ttu-id="a52ed-114">แดชบอร์ดเป็นคุณลักษณะของบริการ Power BI ไม่ใช่ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a52ed-114">Dashboards are a feature of the Power BI service, not Power BI Desktop.</span></span> <span data-ttu-id="a52ed-115">ถึงแม้ว่าคุณไม่สร้างแดชบอร์ดในแอปสำหรับอุปกรณ์เคลื่อนที่ Power BI แต่คุณสามารถ[ดูและแชร์](../consumer/mobile/mobile-apps-view-dashboard.md)ได้</span><span class="sxs-lookup"><span data-stu-id="a52ed-115">Although you don't create dashboards in the Power BI mobile apps, you can [view and share](../consumer/mobile/mobile-apps-view-dashboard.md) there.</span></span>
>
> 

## <a name="video-create-a-dashboard-by-pinning-visuals-and-images-from-a-report"></a><span data-ttu-id="a52ed-116">วิดีโอ: สร้างแดชบอร์ดโดยการปักหมุดภาพและรูปภาพจากรายงานหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a52ed-116">Video: Create a dashboard by pinning visuals and images from a report</span></span>
<span data-ttu-id="a52ed-117">ดู Amanda สร้างแดชบอร์ดใหม่โดยการปักหมุดไปที่การแสดงภาพจากรายงาน</span><span class="sxs-lookup"><span data-stu-id="a52ed-117">Watch Amanda create a new dashboard by pinning visualizations from a report.</span></span> <span data-ttu-id="a52ed-118">จากนั้นให้ทำตามขั้นตอนในส่วนถัดไป [นำเข้าชุดข้อมูลพร้อมรายงาน](#import-a-dataset-with-a-report)เพื่อลองด้วยตนเองโดยใช้ตัวอย่างการวิเคราะห์การจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="a52ed-118">Then, follow the steps in the next section, [Import a dataset with a report](#import-a-dataset-with-a-report), to try it out yourself using the Procurement Analysis sample.</span></span>
    

<iframe width="560" height="315" src="https://www.youtube.com/embed/lJKgWnvl6bQ" frameborder="0" allowfullscreen></iframe>

## <a name="import-a-dataset-with-a-report"></a><span data-ttu-id="a52ed-119">นำเข้าชุดข้อมูลที่มีรายงาน</span><span class="sxs-lookup"><span data-stu-id="a52ed-119">Import a dataset with a report</span></span>
<span data-ttu-id="a52ed-120">ในคำแนะนำทีละขั้นตอนนี้ เราจะนำเข้าหนึ่งในชุดข้อมูลตัวอย่าง Power BI และใช้ในการสร้างแดชบอร์ดใหม่ของเรา</span><span class="sxs-lookup"><span data-stu-id="a52ed-120">In this step-by-step, we import one of the Power BI sample datasets and use it to create our new dashboard.</span></span> <span data-ttu-id="a52ed-121">ตัวอย่างที่เราใช้คือสมุดงาน Excel ที่มีแผ่นงาน PowerView สองแผ่น</span><span class="sxs-lookup"><span data-stu-id="a52ed-121">The sample we use is an Excel workbook with two PowerView sheets.</span></span> <span data-ttu-id="a52ed-122">เมื่อ Power BI นำเข้าสมุดงาน โปรแกรมจะเพิ่มชุดข้อมูลและรายงานไปยังพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="a52ed-122">When Power BI imports the workbook, it adds a dataset and a report to your workspace.</span></span> <span data-ttu-id="a52ed-123">จากนั้น รายงานจะถูกสร้างขึ้นจากแผ่นงาน PowerView โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a52ed-123">The report is automatically created from the PowerView sheets.</span></span>

1. <span data-ttu-id="a52ed-124">ดาวน์โหลด[ไฟล์ Excel](https://go.microsoft.com/fwlink/?LinkId=529784) ตัวอย่างการวิเคราะห์การจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="a52ed-124">Download the [Procurement Analysis sample](https://go.microsoft.com/fwlink/?LinkId=529784) Excel file.</span></span> <span data-ttu-id="a52ed-125">เราขอแนะนำให้บันทึกไฟล์ใน OneDrive for Business ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a52ed-125">We recommend saving it in your OneDrive for Business.</span></span>
2. <span data-ttu-id="a52ed-126">บริการ Power BI ในเบราว์เซอร์ของคุณ (app.powerbi.com)</span><span class="sxs-lookup"><span data-stu-id="a52ed-126">Open the Power BI service in your browser (app.powerbi.com).</span></span>
3. <span data-ttu-id="a52ed-127">จากบานหน้าต่างนำทาง ให้เลือก **พื้นที่ทำงานของฉัน** จากนั้นเลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="a52ed-127">From the nav pane, select **My Workspace** and then select **Get Data**.</span></span>

    ![บานหน้าต่างนำทาง](media/service-dashboard-create/power-bi-get-data-new-look.png)
5. <span data-ttu-id="a52ed-129">ภายใต้ **ไฟล์** ให้เลือก **รับ**</span><span class="sxs-lookup"><span data-stu-id="a52ed-129">Under **Files**, select **Get**.</span></span>

   ![รับไฟล์](media/service-dashboard-create/power-bi-select-files.png)
6. <span data-ttu-id="a52ed-131">นำทางไปยังตำแหน่งที่คุณบันทึกไฟล์ Excel สำหรับตัวอย่างการวิเคราะห์การจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="a52ed-131">Navigate to the location where you saved the Procurement Analysis sample Excel file.</span></span> <span data-ttu-id="a52ed-132">เลือกไฟล์ดังกล่าว จากนั้นเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="a52ed-132">Select it and choose **Connect**.</span></span>

   ![เชื่อมต่อกับไฟล์](media/service-dashboard-create/power-bi-connectnew.png)
7. <span data-ttu-id="a52ed-134">สำหรับการดำเนินการนี้ เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="a52ed-134">For this exercise, select **Import**.</span></span>

    ![หน้าต่าง OneDrive for Business](media/service-dashboard-create/power-bi-import.png)
8. <span data-ttu-id="a52ed-136">เมื่อข้อความแสดงความสำเร็จปรากฏขึ้น เลือก **x** เพื่อยกเลิก</span><span class="sxs-lookup"><span data-stu-id="a52ed-136">When the success message appears, select the **x** to dismiss it.</span></span>

   ![สกรีนช็อตแสดงข้อความแสดงความสำเร็จพร้อมกับ X ที่ถูกเรียกออกมา](media/service-dashboard-create/power-bi-view-datasetnew.png)

> [!TIP]
> <span data-ttu-id="a52ed-138">คุณทราบหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a52ed-138">Did you know?</span></span> <span data-ttu-id="a52ed-139">คุณสามารถทำให้บานหน้าต่างนำทางแคบลงได้โดยเลือกไอคอนที่มีสามบรรทัดที่ ![ไอคอนแสดงหรือซ่อนบานหน้าต่างนำทาง](media/service-dashboard-create/power-bi-new-look-hide-nav-pane.png)ด้านบน</span><span class="sxs-lookup"><span data-stu-id="a52ed-139">You can narrow the nav pane by selecting the icon with three lines at the top ![nav pane show or hide icon](media/service-dashboard-create/power-bi-new-look-hide-nav-pane.png).</span></span> <span data-ttu-id="a52ed-140">ซึ่งช่วยให้คุณมีพื้นที่มากขึ้นในการรายงาน</span><span class="sxs-lookup"><span data-stu-id="a52ed-140">That gives you more room for the report itself.</span></span>

### <a name="open-the-report-and-pin-tiles-to-your-dashboard"></a><span data-ttu-id="a52ed-141">เปิดรายงานและปักหมุดไทล์ไปยังแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="a52ed-141">Open the report and pin tiles to your dashboard</span></span>
1. <span data-ttu-id="a52ed-142">ในพื้นที่ทำงานเดียวกัน เลือกแท็บ **รายงาน** จากนั้นเลือก **ตัวอย่างการวิเคราะห์การจัดซื้อ** เพื่อเปิดรายงาน</span><span class="sxs-lookup"><span data-stu-id="a52ed-142">In the same workspace, select the **Reports** tab, and then select **Procurement Analysis Sample** to open the report.</span></span>

    <span data-ttu-id="a52ed-143">![แท็บรายงาน](media/service-dashboard-create/power-bi-reports.png) รายงานเปิดขึ้นในมุมมองการอ่าน</span><span class="sxs-lookup"><span data-stu-id="a52ed-143">![Reports tab](media/service-dashboard-create/power-bi-reports.png) The report opens in Reading view.</span></span> <span data-ttu-id="a52ed-144">โปรดสังเกตว่ามีสองแถบที่ด้านซ้าย: **การวิเคราะห์ส่วนลด** และ **ภาพรวมการใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="a52ed-144">Notice it has two tabs on the left: **Discount Analysis** and **Spend Overview**.</span></span> <span data-ttu-id="a52ed-145">แต่ละแถบจะแสดงหน้าของรายงานนั้น ๆ</span><span class="sxs-lookup"><span data-stu-id="a52ed-145">Each tab represents a page of the report.</span></span>

2. <span data-ttu-id="a52ed-146">เลือก **ตัวเลือกอื่นๆ (...)**  > **แก้ไขรายงาน** เพื่อเปิดรายงานในมุมมองการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="a52ed-146">Select **More options (...)** > **Edit report** to open the report in Editing view.</span></span>

    ![รายงานในมุมมองการอ่าน](media/service-dashboard-create/power-bi-reading-view.png)
3. <span data-ttu-id="a52ed-148">เลื่อนไปเหนือการแสดงภาพเพื่อดูตัวเลือกที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a52ed-148">Hover over a visualization to reveal the options available.</span></span> <span data-ttu-id="a52ed-149">เมื่อต้องการเพิ่มการแสดงภาพลงในแดชบอร์ด เลือกไอคอนเข็มหมุด</span><span class="sxs-lookup"><span data-stu-id="a52ed-149">To add a visualization to a dashboard, select the pin icon</span></span> ![ปักหมุดไอคอน](media/service-dashboard-create/power-bi-pin-icon.png)<span data-ttu-id="a52ed-151">.</span><span class="sxs-lookup"><span data-stu-id="a52ed-151">.</span></span>

    ![เลื่อนไปเหนือไทล์](media/service-dashboard-create/power-bi-hover.png)
4. <span data-ttu-id="a52ed-153">เนื่องจากเรากำลังสร้างแดชบอร์ดใหม่ ให้เลือกตัวเลือกสำหรับ **แดชบอร์ดใหม่** และตั้งชื่อ</span><span class="sxs-lookup"><span data-stu-id="a52ed-153">Because we're creating a new dashboard, select the option for **New dashboard** and give it a name.</span></span>

    ![สกรีนช็อตแสดงหน้าต่าง ปักหมุดไปยังแดชบอร์ด](media/service-dashboard-create/power-bi-pin-tile.png)
5. <span data-ttu-id="a52ed-155">เมื่อคุณเลือก **Pin**, Power BI สร้างแดชบอร์ดใหม่ในพื้นที่ทำงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="a52ed-155">When you select **Pin**, Power BI creates the new dashboard in the current workspace.</span></span> <span data-ttu-id="a52ed-156">หลังจากข้อความ **ปักหมุดไปยังแดชบอร์ด** ปรากฏขึ้น ให้เลือก **ไปยังแดชบอร์ด**</span><span class="sxs-lookup"><span data-stu-id="a52ed-156">After the **Pinned to dashboard** message appears, select **Go to dashboard**.</span></span> <span data-ttu-id="a52ed-157">หากมีข้อความปรากฏขึ้นให้บันทึกรายงาน เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a52ed-157">If you're prompted to save the report, choose **Save**.</span></span>

    ![สกรีนช็อตแสดงข้อความแสดงความสำเร็จพร้อมกับตัวเลือก ไปยังแดชบอร์ด ที่ถูกเรียกออกมา](media/service-dashboard-create/power-bi-pin-success.png)

    <span data-ttu-id="a52ed-159">Power BI เปิดแดชบอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="a52ed-159">Power BI opens the new dashboard.</span></span> <span data-ttu-id="a52ed-160">ซึ่งมีหนึ่งไทล์: การแสดงภาพที่คุณเพิ่งปักหมุด</span><span class="sxs-lookup"><span data-stu-id="a52ed-160">It has one tile: the visualization you just pinned.</span></span>

   ![แดชบอร์ดที่มีหนึ่งไทล์](media/service-dashboard-create/power-bi-pinned.png)
7. <span data-ttu-id="a52ed-162">เลือกไทล์ดังกล่าวเพื่อต้องกลับไปยังรายงาน</span><span class="sxs-lookup"><span data-stu-id="a52ed-162">Select the tile to return to the report.</span></span> <span data-ttu-id="a52ed-163">ปักหมุดไทล์เพิ่มเติมไปยังแดชบอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="a52ed-163">Pin a few more tiles to the new dashboard.</span></span> <span data-ttu-id="a52ed-164">เมื่อหน้าต่าง **ปักหมุดลงในแดชบอร์ด** แสดงขึ้นมา ให้เลือก **แดชบอร์ดที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="a52ed-164">When the **Pin to dashboard** window displays, select **Existing dashboard**.</span></span>  

   ![สกรีนช็อตแสดงหน้าต่าง ปักหมุดลงในแดชบอร์ด พร้อมกับตัวเลือก แดชบอร์ดที่มีอยู่ ที่ถูกเรียกออกมา](media/service-dashboard-create/power-bi-existing-dashboard.png)

## <a name="pin-an-entire-report-page-to-the-dashboard"></a><span data-ttu-id="a52ed-166">ปักหมุดทั้งหน้ารายงานไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="a52ed-166">Pin an entire report page to the dashboard</span></span>
<span data-ttu-id="a52ed-167">แทนที่จะเป็นการปักหมุดไปยังทีละภาพ คุณสามารถ [ปักหมุดทั้งหน้ารายงานเป็น *ไทล์สด*](service-dashboard-pin-live-tile-from-report.md)ได้</span><span class="sxs-lookup"><span data-stu-id="a52ed-167">Instead of pinning one visual at a time, you can [pin an entire report page as a *live tile*](service-dashboard-pin-live-tile-from-report.md).</span></span> <span data-ttu-id="a52ed-168">ลองทำดูกัน</span><span class="sxs-lookup"><span data-stu-id="a52ed-168">Let's do it.</span></span>

1. <span data-ttu-id="a52ed-169">ในตัวแก้ไขรายงาน เลือกแถบ **ภาพรวมการใช้จ่าย** เพื่อเปิดหน้าที่สอง ของรายงานขึ้น</span><span class="sxs-lookup"><span data-stu-id="a52ed-169">In the report editor, select the **Spend Overview** tab to open the second page of the report.</span></span>

   ![แถบรายงาน](media/service-dashboard-create/power-bi-page-tab.png)

2. <span data-ttu-id="a52ed-171">เราต้องการการแสดงผลด้วยภาพทั้งหมดในรายงานบนแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="a52ed-171">We want all of the visuals in the report on your dashboard.</span></span> <span data-ttu-id="a52ed-172">ที่มุมขวาบนของแถบเมนู เลือก **ปักหมุดหน้ารายงานสด**</span><span class="sxs-lookup"><span data-stu-id="a52ed-172">In the upper-right corner of the menubar, select **Pin live page**.</span></span> <span data-ttu-id="a52ed-173">ที่แดชบอร์ด ระบบจะอัปเดทไทล์หน้ารายงานสดทุกครั้งที่มีการรีเฟรชหน้าดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="a52ed-173">On a dashboard, live page tiles update each time the page is refreshed.</span></span>

   ![มุมบนขวาของตัวแก้ไขรายงาน](media/service-dashboard-create/power-bi-pin-live.png)

3. <span data-ttu-id="a52ed-175">เมื่อหน้าต่าง **ปักหมุดลงในแดชบอร์ด** ปรากฎขึ้นมา ให้เลือก **แดชบอร์ดที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="a52ed-175">When the **Pin to dashboard** window appears, select **Existing dashboard**.</span></span>

   ![สกรีนช็อตแสดงหน้าต่าง ปักหมุดลงในแดชบอร์ด พร้อมกับตัวเลือก แดชบอร์ดที่มีอยู่ที่คุณเลือกและปุ่ม ปักหมุดหน้านี้](media/service-dashboard-create/power-bi-pin-live2.png)

4. <span data-ttu-id="a52ed-177">หลังจากข้อความแสดงความ สำเร็จ ปรากฏขึ้น เลือก **ไปยังแดชบอร์ด**</span><span class="sxs-lookup"><span data-stu-id="a52ed-177">After the Success message appears, select **Go to dashboard**.</span></span> <span data-ttu-id="a52ed-178">ตรงจุดนี้คุุณจะเห็นไทล์ที่คุณได้ปักหมุดไทล์จากรายงาน</span><span class="sxs-lookup"><span data-stu-id="a52ed-178">There you see the tiles you pinned from the report.</span></span> <span data-ttu-id="a52ed-179">ในตัวอย่างด้านล่าง เราได้ปักหมุดไทล์สองแผ่นจากหน้าหนึ่งของรายงานและหนึ่ง ไทล์รายงานสดที่อยู่บนหน้าสองของรายงาน</span><span class="sxs-lookup"><span data-stu-id="a52ed-179">In the example below, we've pinned two tiles from page one of the report and one live tile, which is page two of the report.</span></span>

   ![สกรีนช็อตแสดงแดชบอร์ด Power BI พร้อมการแสดงผลข้อมูลด้วยภาพจากบทความนี้](media/service-dashboard-create/power-bi-dashboard.png)

## <a name="next-steps"></a><span data-ttu-id="a52ed-181">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a52ed-181">Next steps</span></span>
<span data-ttu-id="a52ed-182">ยินดีด้วย คุณได้สร้างแดชบอร์ดแรกของคุณแล้ว!</span><span class="sxs-lookup"><span data-stu-id="a52ed-182">Congratulations on creating your first dashboard!</span></span> <span data-ttu-id="a52ed-183">ตอนนี้คุณมีแดชบอร์ดหนึ่งอันแล้ว มีสิ่งต่าง ๆ มากมายที่คุณสามารถทำได้บนแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="a52ed-183">Now that you have a dashboard, there's much more you can do with it.</span></span> <span data-ttu-id="a52ed-184">ทำตามหนึ่งในบทความที่แนะนำด้านล่างหรือเริ่มต้นสำรวจด้วยตัวคุณเอง:</span><span class="sxs-lookup"><span data-stu-id="a52ed-184">Follow one of the suggested articles below, or start exploring on your own:</span></span> 

* [<span data-ttu-id="a52ed-185">ปรับขนาดและย้ายไทล์</span><span class="sxs-lookup"><span data-stu-id="a52ed-185">Resize and move tiles</span></span>](service-dashboard-edit-tile.md)
* [<span data-ttu-id="a52ed-186">ทั้งหมดเกี่ยวกับไทล์แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="a52ed-186">All about dashboard tiles</span></span>](service-dashboard-tiles.md)
* [<span data-ttu-id="a52ed-187">แชร์แดชบอร์ดของคุณโดยการสร้างแอปฯ</span><span class="sxs-lookup"><span data-stu-id="a52ed-187">Share your dashboard by creating an app</span></span>](../collaborate-share/service-create-workspaces.md)
* [<span data-ttu-id="a52ed-188">Power BI แนวคิดพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="a52ed-188">Power BI - Basic Concepts</span></span>](../fundamentals/service-basic-concepts.md)
* [<span data-ttu-id="a52ed-189">เคล็ดลับสำหรับการออกแบบแดชบอร์ด ที่ยอดเยี่ยม</span><span class="sxs-lookup"><span data-stu-id="a52ed-189">Tips for designing a great dashboard</span></span>](service-dashboards-design-tips.md)

<span data-ttu-id="a52ed-190">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a52ed-190">More questions?</span></span> <span data-ttu-id="a52ed-191">[ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="a52ed-191">[Try the Power BI Community](https://community.powerbi.com/).</span></span>
