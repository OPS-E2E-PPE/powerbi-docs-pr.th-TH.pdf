---
title: 'สร้างรายงานจากไฟล์ Excel ในบริการของ Power BI '
description: สร้างรายงาน Power BI จากไฟล์ Excel ในบริการของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 10/14/2020
LocalizationGroup: Reports
ms.openlocfilehash: a971e0d0b35b0a3988a1c10ea2b7b801830229d6
ms.sourcegitcommit: 0711972326521944fdd8572403c0b15f31b916da
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/22/2020
ms.locfileid: "97721558"
---
# <a name="create-a-report-from-an-excel-file-in-the-power-bi-service"></a><span data-ttu-id="6c403-103">สร้างรายงานจากไฟล์ Excel ในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="6c403-103">Create a report from an Excel file in the Power BI service</span></span>
<span data-ttu-id="6c403-104">คุณได้อ่าน[รายงานใน Power BI](../consumer/end-user-reports.md)และตอนนี้ คุณต้องการสร้างรายงานของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="6c403-104">You've read [Reports in Power BI](../consumer/end-user-reports.md) and now you want to create your own.</span></span> <span data-ttu-id="6c403-105">มีหลายวิธีในการสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="6c403-105">There are different ways to create a report.</span></span> <span data-ttu-id="6c403-106">ในบทความนี้ เราจะเริ่มต้นด้วยการสร้างรายงานพื้นฐานในบริการของ Power BI จากไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="6c403-106">In this article, we start by creating a basic report in the Power BI service from an Excel file.</span></span> <span data-ttu-id="6c403-107">เมื่อคุณทำความเข้าใจพื้นฐานของการสร้างรายงาน ตรวจดู[ขั้นตอนถัดไป](#next-steps)ที่ด้านล่างสำหรับหัวข้อการรายงานขั้นสูงเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6c403-107">Once you understand the basics of creating a report, check out the [Next steps](#next-steps) at the end for more advanced report topics.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="6c403-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="6c403-108">Prerequisites</span></span>
- <span data-ttu-id="6c403-109">[ลงทะเบียนสำหรับบริการของ Power BI](../fundamentals/service-self-service-signup-for-power-bi.md)</span><span class="sxs-lookup"><span data-stu-id="6c403-109">[Sign up for the Power BI service](../fundamentals/service-self-service-signup-for-power-bi.md).</span></span> 
- <span data-ttu-id="6c403-110">[ดาวน์โหลดไฟล์ Excel ตัวอย่างการวิเคราะห์การค้าปลีก](https://go.microsoft.com/fwlink/?LinkId=529778) และบันทึกลงในคอมพิวเตอร์ของคุณหรือไปยัง OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="6c403-110">[Download the Retail Analysis sample Excel file](https://go.microsoft.com/fwlink/?LinkId=529778) and save it to your computer or to OneDrive for Business.</span></span>

## <a name="import-the-excel-file"></a><span data-ttu-id="6c403-111">นำเข้าไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="6c403-111">Import the Excel file</span></span>
<span data-ttu-id="6c403-112">วิธีการสร้างรายงานนี้เริ่มต้น ด้วยไฟล์และพื้นทีรายงานที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="6c403-112">This method of creating a report starts with a file and a blank report canvas.</span></span> <span data-ttu-id="6c403-113">คุณสามารถทำตามในไฟล์ Excel ตัวอย่างของการวิเคราะห์ร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="6c403-113">You can follow along in the Retail Analysis sample Excel file.</span></span>

1. <span data-ttu-id="6c403-114">ในบานหน้าต่างการนำทาง ให้เลือก **พื้นที่ทำงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="6c403-114">In the navigation pane, select **My Workspace**.</span></span>
   
   :::image type="content" source="media/service-report-create-new/power-bi-select-my-workspace.png" alt-text="สกรีนช็อตของการเลือก พื้นที่ทำงานของฉัน":::
2. <span data-ttu-id="6c403-116">จากด้านล่างของบานหน้าต่างนำทาง เลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="6c403-116">From the bottom of the nav pane, select **Get data**.</span></span>
   
   ![รับข้อมูล](media/service-report-create-new/power-bi-get-data3.png)
3. <span data-ttu-id="6c403-118">เลือก **แฟ้ม** และนำทางไปยังตำแหน่งที่คุณบันทึกตัวอย่างการวิเคราะห์ร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="6c403-118">Select **Files** and navigate to the location where you saved the Retail Analysis sample.</span></span>
   
    ![เลือกไฟล์](media/service-report-create-new/power-bi-select-files.png)
4. <span data-ttu-id="6c403-120">สำหรับการดำเนินการนี้ เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="6c403-120">For this exercise, select **Import**.</span></span>
   
   ![เลือกนำเข้า](media/service-report-create-new/power-bi-import.png)
5. <span data-ttu-id="6c403-122">เลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="6c403-122">Select **Open**.</span></span>

   <span data-ttu-id="6c403-123">เมื่อนำเข้าไฟล์ Excel แล้ว ระบบจะแสดงเป็น *ชุดข้อมูล* ในรายการพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="6c403-123">Once the Excel file is imported, it's listed as a *dataset* in the workspace list.</span></span>

1. <span data-ttu-id="6c403-124">เลือก **ตัวเลือกเพิ่มเติม (...)** ที่อยู่ถัดจากชุดข้อมูล แล้วเลือก **สร้างรายงาน**</span><span class="sxs-lookup"><span data-stu-id="6c403-124">Select **More options (...)** next to the dataset, and select **Create report**.</span></span>
   
   :::image type="content" source="media/service-report-create-new/power-bi-dataset-create-report.png" alt-text="สกรีนช็อตของการเลือก สร้างรายงาน":::
6. <span data-ttu-id="6c403-126">ตัวแก้ไขรายงานจะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="6c403-126">The report editor opens.</span></span> 
   
   ![สกรีนช็อตของตัวแก้ไขรายงาน](media/service-report-create-new/power-bi-blank-report.png)

> [!TIP]
> <span data-ttu-id="6c403-128">เลือกไอคอนเมนูเพื่อซ่อนบานหน้าต่างนำทาง เพื่อให้คุณมีพื้นที่มากขึ้น</span><span class="sxs-lookup"><span data-stu-id="6c403-128">Select the menu icon to hide the navigation pane, to give you more room.</span></span>
> 
> :::image type="content" source="../media/power-bi-hide-navigation-pane.png" alt-text="สกรีนช็อตของเลือกไอคอนเมนู เพื่อซ่อนบานหน้าต่างนำทาง":::


## <a name="add-a-radial-gauge-to-the-report"></a><span data-ttu-id="6c403-130">เพิ่มการวัดรัศมีลงในรายงาน</span><span class="sxs-lookup"><span data-stu-id="6c403-130">Add a Radial Gauge to the report</span></span>
<span data-ttu-id="6c403-131">หลังจากที่ชุดข้อมูลของเราจะถูกนำเข้า มาเริ่มต้นการตอบคำถามบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="6c403-131">Now that our dataset is imported, let's start answering some questions.</span></span>  <span data-ttu-id="6c403-132">เราหัวหน้าฝ่ายตลาดเจ้าหน้าที่ (CMO) ต้องการทราบเกี่ยวกับวิธีปิดเราที่การประชุมเป้าหมายการขายของปีนี้</span><span class="sxs-lookup"><span data-stu-id="6c403-132">Our Chief Marketing Officer (CMO) wants to know how close we are to meeting this year's sales goals.</span></span> <span data-ttu-id="6c403-133">การวัดจะเป็น[ตัวเลือกการแสดงภาพที่ดี](../visuals/power-bi-report-visualizations.md)สำหรับการแสดงข้อมูลชนิดนี้</span><span class="sxs-lookup"><span data-stu-id="6c403-133">A Gauge is a [good visualization choice](../visuals/power-bi-report-visualizations.md) for displaying this type of information.</span></span>

1. <span data-ttu-id="6c403-134">ในบานหน้าต่างเขตข้อมูล เลือก **ยอดขาย** > **ค่ายอดขายของปี** > **นี้**</span><span class="sxs-lookup"><span data-stu-id="6c403-134">In the Fields pane, select **Sales** > **This Year Sales** > **Value**.</span></span>
   
    ![แผนภูมิคอลัมน์ในตัวแก้ไขรายงาน](media/service-report-create-new/power-bi-report-step1.png)
2. <span data-ttu-id="6c403-136">แปลงภาพเป็นการวัด โดยการเลือกเทมเพลวัด![ไอคอนตัววัด](media/service-report-create-new/powerbi-gauge-icon.png)จาก **หน้าต่าง** แสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="6c403-136">Convert the visual to a Gauge by selecting the Gauge template ![Gauge icon](media/service-report-create-new/powerbi-gauge-icon.png) from the **Visualizations** pane.</span></span>
   
    ![ภาพแผนที่ในตัวแก้ไขรายงาน](media/service-report-create-new/power-bi-report-step2.png)
3. <span data-ttu-id="6c403-138">ลาก **ยอดขาย** > **เป้าหมายยอดขาย** > **ของปีนี้** เพื่อ **ค่าเป้าหมาย** กัน</span><span class="sxs-lookup"><span data-stu-id="6c403-138">Drag **Sales** > **This Year Sales** > **Goal** to the **Target value** well.</span></span> <span data-ttu-id="6c403-139">ดูเหมือนว่าเรากำลังใกล้เคียงกับเป้าหมายของเรามาก</span><span class="sxs-lookup"><span data-stu-id="6c403-139">Looks like we're very close to our goal.</span></span>
   
    ![ตัววัดแบบภาพ ด้วยเป้าหมายเป็นค่าเป้าหมาย](media/service-report-create-new/power-bi-report-step3.png)
4. <span data-ttu-id="6c403-141">ในตอนนี้เป็นเวลาที่เหมาะสมที่จะบันทึกรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="6c403-141">Now would be a good time to save your report.</span></span>
   
   ![เมนูไฟล์](media/service-report-create-new/powerbi-save.png)

## <a name="add-an-area-chart-and-slicer-to-the-report"></a><span data-ttu-id="6c403-143">เพิ่มชาร์ตพื้นที่และ slicer ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="6c403-143">Add an area chart and slicer to the report</span></span>
<span data-ttu-id="6c403-144">CMO ของเรามีคำถามบางอย่างเพิ่มเติมให้แก่เรา</span><span class="sxs-lookup"><span data-stu-id="6c403-144">Our CMO has some additional questions for us to answer.</span></span> <span data-ttu-id="6c403-145">พวกเขาต้องการทราบวิธีการเปรียบเทียบยอดขายของปีนี้กับปีที่แล้ว</span><span class="sxs-lookup"><span data-stu-id="6c403-145">They'd like to know how sales this year compare to last year.</span></span> <span data-ttu-id="6c403-146">และพวกเขาต้องการดูผลลัพธ์ตามเขต</span><span class="sxs-lookup"><span data-stu-id="6c403-146">And, they'd like to see the findings by district.</span></span>

1. <span data-ttu-id="6c403-147">ก่อนอื่น มาสร้างพื้นที่ว่างในพื้นที่รายงานก่อน</span><span class="sxs-lookup"><span data-stu-id="6c403-147">First, let's make some room on our canvas.</span></span> <span data-ttu-id="6c403-148">เลือกตัววัด และย้ายไปมุมบนขวา</span><span class="sxs-lookup"><span data-stu-id="6c403-148">Select the Gauge and move it into the top-right corner.</span></span> <span data-ttu-id="6c403-149">จากนั้น จับ และลากมุมหนึ่ง และทำให้เล็กลง</span><span class="sxs-lookup"><span data-stu-id="6c403-149">Then grab and drag one of the corners and make it smaller.</span></span>
2. <span data-ttu-id="6c403-150">ยกเลิกเลือกตัววัด</span><span class="sxs-lookup"><span data-stu-id="6c403-150">Deselect the gauge.</span></span> <span data-ttu-id="6c403-151">ในบานหน้าต่างเขตข้อมูล เลือก **ยอดขาย** > **ค่ายอดขายของปีนี้** > **นี้** เลือก **ขาย** > **ยอดขายของปีที่แล้ว**</span><span class="sxs-lookup"><span data-stu-id="6c403-151">In the Fields pane, select **Sales** > **This Year Sales** > **Value** and select **Sales** > **Last Year Sales**.</span></span>
   
    ![ตัวแก้ไขรายงาน ด้วยตัววัดและแผนภูมิแท่ง](media/service-report-create-new/power-bi-report-step4.png)
3. <span data-ttu-id="6c403-153">แปลงภาพเป็นแผนภูมิพื้นที่โดยเลือกเทมเพลตแผนภูมิพื้นที่![
ไอคอนแผนภูมิ](media/service-report-create-new/power-bi-areachart-icon.png)จาก **หน้าต่าง** แสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="6c403-153">Convert the visual to an Area chart by selecting the Area chart template ![chart icon](media/service-report-create-new/power-bi-areachart-icon.png) from the **Visualizations** pane.</span></span>
4. <span data-ttu-id="6c403-154">เลือก **เวลา** > **รอบระยะเวลา** เพื่อเพิ่มไปยัง **แกน** กัน</span><span class="sxs-lookup"><span data-stu-id="6c403-154">Select **Time** > **Period** to add it to the **Axis** well.</span></span>
   
    ![ตัวแก้ไขรายงาน ด้วยแผนภูมิพื้นที่ที่ใช้งานอยู่](media/service-report-create-new/power-bi-report-step5.png)
5. <span data-ttu-id="6c403-156">เมื่อต้องการเรียงลำดับการแสดงภาพ โดยรอบระยะเวลา เลือกจุดไข่ปลา แล้วเลือก **เรียงลำดับตามระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="6c403-156">To sort the visualization by time period, select the ellipses and choose **Sort by Period**.</span></span>
6. <span data-ttu-id="6c403-157">ตอนนี้มาเพิ่มตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6c403-157">Now let's add the slicer.</span></span> <span data-ttu-id="6c403-158">เลือกพื้นที่ว่างบนพื้นที่รายงาน และเลือกตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6c403-158">Select an empty area on the canvas and choose the Slicer</span></span> ![ไอคอนตัวแบ่งส่วนข้อมูล](media/service-report-create-new/power-bi-slicer-icon.png) <span data-ttu-id="6c403-160">แม่แบบ</span><span class="sxs-lookup"><span data-stu-id="6c403-160">template.</span></span> <span data-ttu-id="6c403-161">ตอนนี้เรามีตัวแบ่งส่วนข้อมูลที่ว่างเปล่าบนพื้นที่ทำงานของเรา</span><span class="sxs-lookup"><span data-stu-id="6c403-161">We now have an empty slicer on our canvas.</span></span>
   
    ![พื้นที่รายงาน](media/service-report-create-new/power-bi-report-step6.png)    
7. <span data-ttu-id="6c403-163">จากบานหน้าต่างเขตข้อมูล เลือก **เขต** > **เขต**</span><span class="sxs-lookup"><span data-stu-id="6c403-163">From the Fields pane, select **District** > **District**.</span></span> <span data-ttu-id="6c403-164">ย้าย และปรับขนาดตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6c403-164">Move and resize the slicer.</span></span>
   
    ![ตัวแก้ไขรายงาน เพิ่มเขต](media/service-report-create-new/power-bi-report-step7.png)  
8. <span data-ttu-id="6c403-166">ใช้ตัวแบ่งส่วนข้อมูลเพื่อค้นหารูปแบบและข้อมูลเชิงลึก โดยเขต</span><span class="sxs-lookup"><span data-stu-id="6c403-166">Use the slicer to look for patterns and insights by District.</span></span>
   
   ![วิดีโอของการใช้ตัวแบ่งส่วนข้อมูล](media/service-report-create-new/power-bi-slicer-video2.gif)  

<span data-ttu-id="6c403-168">สำรวจข้อมูลของคุณ และเพิ่มการแสดงภาพต่อไป</span><span class="sxs-lookup"><span data-stu-id="6c403-168">Continue exploring your data and adding visualizations.</span></span> <span data-ttu-id="6c403-169">เมื่อคุณค้นหาข้อมูลเชิงลึกที่น่าสนใจโดยเฉพาะอย่างยิ่ง[ปักหมุดเหล่านั้นไปยังแดชบอร์ด](service-dashboard-pin-tile-from-report.md)</span><span class="sxs-lookup"><span data-stu-id="6c403-169">When you find especially interesting insights, [pin them to a dashboard](service-dashboard-pin-tile-from-report.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="6c403-170">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="6c403-170">Next steps</span></span>

* [<span data-ttu-id="6c403-171">ปักหมุดภาพไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="6c403-171">Pin visualizations to a dashboard</span></span>](service-dashboard-pin-tile-from-report.md)
* [<span data-ttu-id="6c403-172">เปลี่ยนการตั้งค่ารายงานในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="6c403-172">Change report settings in the Power BI service</span></span>](power-bi-report-settings.md)
* <span data-ttu-id="6c403-173">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6c403-173">More questions?</span></span> [<span data-ttu-id="6c403-174">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="6c403-174">Try the Power BI Community</span></span>](https://community.powerbi.com/)
