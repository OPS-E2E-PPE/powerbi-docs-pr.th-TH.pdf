---
title: 'ตัวอย่างการวิเคราะห์ด้านการขายปลีก - Power BI: ชมการแนะนำ'
description: 'ตัวอย่างการวิเคราะห์ด้านการขายปลีก - Power BI: ชมการแนะนำ'
author: maggiesMSFT
ms.author: maggies
ms.reviewer: amac
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: conceptual
ms.date: 07/02/2019
LocalizationGroup: Samples
ms.openlocfilehash: 1a3a4bc467299f7baeb12ca68af1d2730d5839f0
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96396003"
---
# <a name="retail-analysis-sample-for-power-bi-take-a-tour"></a><span data-ttu-id="7ec2d-103">ตัวอย่างการวิเคราะห์ด้านการขายปลีก - Power BI: ชมการแนะนำ</span><span class="sxs-lookup"><span data-stu-id="7ec2d-103">Retail Analysis sample for Power BI: Take a tour</span></span>

<span data-ttu-id="7ec2d-104">ชุดเนื้อหาตัวอย่างการวิเคราะห์การขายปลีกประกอบด้วยแดชบอร์ด รายงาน และชุดข้อมูลที่วิเคราะห์ข้อมูลการขายปลีกของสินค้าที่ขายในหลายร้านค้าและเขต</span><span class="sxs-lookup"><span data-stu-id="7ec2d-104">The Retail Analysis sample content pack contains a dashboard, report, and dataset that analyzes retail sales data of items sold across multiple stores and districts.</span></span> <span data-ttu-id="7ec2d-105">The metrics compare this year's performance to last year's for sales, units, gross margin, and variance, as well as new-store analysis.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-105">The metrics compare this year's performance to last year's for sales, units, gross margin, and variance, as well as new-store analysis.</span></span> 

![แดชบอร์ดของตัวอย่างการวิเคราะห์การค้าปลีก](media/sample-retail-analysis/retail1.png)

<span data-ttu-id="7ec2d-107">ตัวอย่างนี้เป็นส่วนหนึ่งของชุดตัวอย่าง ที่แสดงให้เห็นวิธีการที่คุณสามารถใช้ Power BI กับข้อมูล รายงาน และแดชบอร์ดที่เกี่ยวข้องกับธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="7ec2d-107">This sample is part of a series that shows how you can use Power BI with business-oriented data, reports, and dashboards.</span></span> <span data-ttu-id="7ec2d-108">ซึ่งสร้างขึ้นโดย [obviEnce](http://www.obvience.com/) ด้วยข้อมูลจริงที่ไม่มีการระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="7ec2d-108">It was created by [obviEnce](http://www.obvience.com/) with real data, which has been anonymized.</span></span> <span data-ttu-id="7ec2d-109">ข้อมูลมีให้ใช้งานหลายรูปแบบ: ชุดเนื้อหา ไฟล์ Power BI Desktop .pbix หรือเวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="7ec2d-109">The data is available in several formats: content pack, .pbix Power BI Desktop file, or Excel workbook.</span></span> <span data-ttu-id="7ec2d-110">ดู [ตัวอย่างสำหรับ Power BI](sample-datasets.md)</span><span class="sxs-lookup"><span data-stu-id="7ec2d-110">See [Samples for Power BI](sample-datasets.md).</span></span> 

<span data-ttu-id="7ec2d-111">บทช่วยสอนนี้จะสำรวจชุดเนื้อหาของตัวอย่างการวิเคราะห์การขายปลีกในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="7ec2d-111">This tutorial explores the Retail Analysis sample content pack in the Power BI service.</span></span> <span data-ttu-id="7ec2d-112">เนื่องจากประสบการณ์การใช้รายงานจะคล้ายคลึงกันใน Power BI Desktop ดังนั้นคุณสามารถใช้ Power BI Desktop กับไฟล์ .pbix ตัวอย่างใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="7ec2d-112">Because the report experience is similar in Power BI Desktop and in the service, you can also follow along by using the sample .pbix file in Power BI Desktop.</span></span> 

<span data-ttu-id="7ec2d-113">คุณไม่จำเป็นต้องมีสิทธิการใช้งาน Power BI ในการสำรวจตัวอย่างใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="7ec2d-113">You don't need a Power BI license to explore the samples in Power BI Desktop.</span></span> <span data-ttu-id="7ec2d-114">ถ้าคุณไม่มีสิทธิการใช้งาน Power BI Pro คุณสามารถบันทึกตัวอย่างไปยังพื้นที่ทำงานของฉันในบริการของ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="7ec2d-114">If you don't have a Power BI Pro license, you can save the sample to your My Workspace in the Power BI service.</span></span> 

## <a name="get-the-sample"></a><span data-ttu-id="7ec2d-115">รับตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="7ec2d-115">Get the sample</span></span>

 <span data-ttu-id="7ec2d-116">ก่อนที่คุณสามารถใช้ตัวอย่าง คุณต้องดาวน์โหลดในรูปแบบ[ชุดเนื้อหา](#get-the-content-pack-for-this-sample)[ไฟล์ .pbix](#get-the-pbix-file-for-this-sample) หรือ[เวิร์กบุ๊ก Excel](#get-the-excel-workbook-for-this-sample)</span><span class="sxs-lookup"><span data-stu-id="7ec2d-116">Before you can use the sample, you must first download it as a [content pack](#get-the-content-pack-for-this-sample), [.pbix file](#get-the-pbix-file-for-this-sample), or [Excel workbook](#get-the-excel-workbook-for-this-sample).</span></span>

### <a name="get-the-content-pack-for-this-sample"></a><span data-ttu-id="7ec2d-117">รับชุดเนื้อหาสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="7ec2d-117">Get the content pack for this sample</span></span>

1. <span data-ttu-id="7ec2d-118">เปิดบริการ Power BI (app.powerbi.com) ลงชื่อเข้าใช้ และเปิดพื้นที่ทำงานที่คุณต้องการบันทึกตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="7ec2d-118">Open the Power BI service (app.powerbi.com), sign in, and open the workspace where you want to save the sample.</span></span> 

    <span data-ttu-id="7ec2d-119">ถ้าคุณไม่มีสิทธิการใช้งาน Power BI Pro คุณสามารถบันทึกตัวอย่างไปยังพื้นที่ทำงานของฉัน</span><span class="sxs-lookup"><span data-stu-id="7ec2d-119">If you don't have a Power BI Pro license, you can save the sample to your My Workspace.</span></span>

2. <span data-ttu-id="7ec2d-120">ที่มุมด้านล่างซ้าย เลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="7ec2d-120">In the bottom-left corner, select **Get Data**.</span></span>

    ![เลือกรับข้อมูล](media/sample-datasets/power-bi-get-data.png)
3. <span data-ttu-id="7ec2d-122">บนหน้า **รับข้อมูล** ที่ปรากฏขึ้น เลือก **ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="7ec2d-122">On the **Get Data** page that appears, select **Samples**.</span></span>
   
4. <span data-ttu-id="7ec2d-123">เลือก **ตัวอย่างการวิเคราะห์ด้านการขายปลีก** และเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="7ec2d-123">Select **Retail Analysis Sample**, and then choose **Connect**.</span></span>  
  
   ![เชื่อมต่อกับตัวอย่าง](media/sample-retail-analysis/retail16.png)
   
5. <span data-ttu-id="7ec2d-125">Power BI นำเข้าชุดเนื้อหา จากนั้นเพิ่มแดชบอร์ด รายงาน และชุดข้อมูลใหม่ไปยังพื้นที่ทำงานปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="7ec2d-125">Power BI imports the content pack, and then adds a new dashboard, report, and dataset to your current workspace.</span></span>
   
   ![รายการตัวอย่างการวิเคราะห์การค้าปลีก](media/sample-retail-analysis/retail-entry.png)
  
### <a name="get-the-pbix-file-for-this-sample"></a><span data-ttu-id="7ec2d-127">รับไฟล์ .pbix สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="7ec2d-127">Get the .pbix file for this sample</span></span>

<span data-ttu-id="7ec2d-128">อีกทางเลือกหนึ่งคือ คุณสามารถดาวน์โหลดตัวอย่างการวิเคราะห์การขายปลีกเป็น[ไฟล์ .pbix](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix) ซึ่งได้รับการออกแบบมาสำหรับใช้กับ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="7ec2d-128">Alternatively, you can download the Retail Analysis sample as a [.pbix file](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix), which is designed for use with Power BI Desktop.</span></span> 

### <a name="get-the-excel-workbook-for-this-sample"></a><span data-ttu-id="7ec2d-129">รับเวิร์กบุ๊ก Excel สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="7ec2d-129">Get the Excel workbook for this sample</span></span>

<span data-ttu-id="7ec2d-130">ถ้าคุณต้องการดูแหล่งข้อมูลสำหรับตัวอย่างนี้ ตัวอย่างนี้ยังมีให้ในรูปแบบ[เวิร์กบุ๊ก Excel](https://go.microsoft.com/fwlink/?LinkId=529778)</span><span class="sxs-lookup"><span data-stu-id="7ec2d-130">If you want to view the data source for this sample, it's also available as an [Excel workbook](https://go.microsoft.com/fwlink/?LinkId=529778).</span></span> <span data-ttu-id="7ec2d-131">เวิร์กบุ๊กประกอบด้วยแผ่นงาน Power View ที่คุณสามารถดู และปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="7ec2d-131">The workbook contains Power View sheets that you can view and modify.</span></span> <span data-ttu-id="7ec2d-132">หากต้องการดูข้อมูลดิบ ให้เปิดใช้งาน add-in การวิเคราะห์ข้อมูล แล้วจากนั้นเลือก **Power Pivot > จัดการ**</span><span class="sxs-lookup"><span data-stu-id="7ec2d-132">To see the raw data, enable the Data Analysis add-ins, and then select **Power Pivot > Manage**.</span></span> <span data-ttu-id="7ec2d-133">หากต้องการเปิดใช้งาน Power View และ Power Pivot add-in โปรดดู [สำรวจตัวอย่าง Excel ใน Excel ](sample-datasets.md#explore-excel-samples-inside-excel)สำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="7ec2d-133">To enable the Power View and Power Pivot add-ins, see [Explore the Excel samples in Excel](sample-datasets.md#explore-excel-samples-inside-excel) for details.</span></span>

## <a name="start-on-the-dashboard-and-open-the-report"></a><span data-ttu-id="7ec2d-134">เริ่มต้นที่แดชบอร์ดและเปิดรายงาน</span><span class="sxs-lookup"><span data-stu-id="7ec2d-134">Start on the dashboard and open the report</span></span>

1. <span data-ttu-id="7ec2d-135">ในพื้นที่ทำงานที่คุณบันทึกตัวอย่าง เปิดแท็บ **แดชบอร์ด** จาก นั้นค้นหาแดชบอร์ด **ตัวอย่างการวิเคราะห์การขายปลีก** และเลือก</span><span class="sxs-lookup"><span data-stu-id="7ec2d-135">In the workspace where you saved the sample, open the **Dashboards** tab, then find the **Retail Analysis Sample** dashboard and select it.</span></span> 
2. <span data-ttu-id="7ec2d-136">บนแดชบอร์ด เลือกไทล์ **รวมร้านค้าใหม่ & ร้านค้าที่มีอยู่** ไทล์ ซึ่งเปิดขึ้นในหน้า **ภาพรวมยอดขายของร้านค้า** ในรายงานตัวอย่างการวิเคราะห์การขายปลีก</span><span class="sxs-lookup"><span data-stu-id="7ec2d-136">On the dashboard, select the **Total Stores New & Existing Stores** tile, which opens to the **Store Sales Overview** page in the Retail Analysis Sample report.</span></span> 

   ![ไทล์ร้านค้าทั้งหมด](media/sample-retail-analysis/retail-analysis-7.png)  

   <span data-ttu-id="7ec2d-138">บนหน้ารายงานนี้ คุณจะเห็นว่าเรามีร้านค้าทั้งหมด 104 แห่ง ซึ่ง 10 ร้านเป็นร้านใหม</span><span class="sxs-lookup"><span data-stu-id="7ec2d-138">On this report page, you see we have a total of 104 stores, 10 of which are new.</span></span> <span data-ttu-id="7ec2d-139">เรามีสองเชนธุรกิจ นั่นคือ Fashions Direct และ Lindseys</span><span class="sxs-lookup"><span data-stu-id="7ec2d-139">We have two chains, Fashions Direct and Lindseys.</span></span> <span data-ttu-id="7ec2d-140">ร้านค้า Fashions Direct มีขนาดใหญ่กว่าเมื่อดูโดยเฉลี่ยแล้ว</span><span class="sxs-lookup"><span data-stu-id="7ec2d-140">Fashions Direct stores are larger, on average.</span></span>
3. <span data-ttu-id="7ec2d-141">ในแผนภูมิวงกลม **ยอดขายของปีนี้ตามห่วงโซ่** เลือก **Fashions Direct**</span><span class="sxs-lookup"><span data-stu-id="7ec2d-141">In the **This Year Sales by Chain** pie chart, select **Fashions Direct**.</span></span>

   ![แผนภูมิยอดขายของปีนี้ตามห่วงโซ่](media/sample-retail-analysis/retail3.png)  

   <span data-ttu-id="7ec2d-143">สังเกตผลลัพธ์ในแผนภูมิฟอง **% ผลต่างของยอดขายรวม**:</span><span class="sxs-lookup"><span data-stu-id="7ec2d-143">Notice the result in the **Total Sales Variance %** bubble chart:</span></span>

   ![แผนภูมิ % ผลต่างของยอดขายรวม](media/sample-retail-analysis/pbi_sample_retanlbubbles.png)  

   <span data-ttu-id="7ec2d-145">เขต **FD-01** มี **ยอดขายเฉลี่ยต่อตารางฟุตสูงสุด** ส่วน FD-02 มี **ค่าความแปรปรวนของยอดขายรวม** ต่ำสุด เมื่อเปรียบเทียบกับปีที่แล้ว</span><span class="sxs-lookup"><span data-stu-id="7ec2d-145">The **FD-01** district has the highest average **Sales per Square Foot** and FD-02 has the lowest **Total Sales Variance** compared to last year.</span></span> <span data-ttu-id="7ec2d-146">FD-03 และ FD-04 มีผลประกอบการโดยรวมแย่ที่สุด</span><span class="sxs-lookup"><span data-stu-id="7ec2d-146">FD-03 and FD-04 are worst performers overall.</span></span>
4. <span data-ttu-id="7ec2d-147">เลือกแต่ละฟองหรือแผนภูมิอื่น ๆ เพื่อดูการไฮไลท์ข้าม ซึ่งเผยให้เห็นผลกระทบของการเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="7ec2d-147">Select individual bubbles or other charts to see cross highlighting, revealing the impact of your selections.</span></span>
5. <span data-ttu-id="7ec2d-148">เลือก **ตัวอย่างการวิเคราะห์การขายปลีก** จากบานหน้าต่างนำทางด้านบนเพื่อกลับไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="7ec2d-148">To return to the dashboard, select  **Retail Analysis Sample** from the top nav pane.</span></span>

   ![แถบนำทาง](media/sample-retail-analysis/power-bi-breadcrumbs.png)
6. <span data-ttu-id="7ec2d-150">บนแดชบอร์ด เลือกไทล์ **ร้านค้าที่มีอยู่และร้านค้าใหม่ของปีนี้** ซึ่งมีค่าเท่ากับการพิมพ์ *ยอดขายของปีนี้* ในกล่องคำถามถามตอบ</span><span class="sxs-lookup"><span data-stu-id="7ec2d-150">On the dashboard, select the **This Year's Sales New & Existing Stores** tile, which is equivalent to typing *This year sales* in the Q&A question box.</span></span>

   ![ไทล์ยอดขายของปีนี้](media/sample-retail-analysis/pbi_sample_retanlthisyrsales.png)

   <span data-ttu-id="7ec2d-152">ผลลัพธ์การถามตอบจะปรากฏขึ้น:</span><span class="sxs-lookup"><span data-stu-id="7ec2d-152">The Q&A results appear:</span></span>

   ![ยอดขายของปีนี้ในถามตอบ](media/sample-retail-analysis/retail7.png)

## <a name="review-a-tile-created-with-power-bi-qa"></a><span data-ttu-id="7ec2d-154">ตรวจทานไทล์ที่สร้างขึ้นด้วย Power BI ถามตอบ</span><span class="sxs-lookup"><span data-stu-id="7ec2d-154">Review a tile created with Power BI Q&A</span></span>
<span data-ttu-id="7ec2d-155">เรามาดูแบบเฉพาะเจาะจงมากขึ้นกัน</span><span class="sxs-lookup"><span data-stu-id="7ec2d-155">Let's get more specific.</span></span>

1. <span data-ttu-id="7ec2d-156">เปลี่ยนคำถามเป็น _ยอดขายของปีนี้ **ตามเขต**_</span><span class="sxs-lookup"><span data-stu-id="7ec2d-156">Change the question to _this year sales **by district**_.</span></span> <span data-ttu-id="7ec2d-157">สังเกตผลลัพธ์: ระบบถามตอบจะใส่คำตอบในแผนภูมิแท่งและแนะนำวลีอื่น ๆ โดยอัตโนมัติ:</span><span class="sxs-lookup"><span data-stu-id="7ec2d-157">Observe the result: Q&A automatically places the answer in a bar chart and suggests other phrases:</span></span>

   ![ยอดขายของปีนี้ตามเขตในถามตอบ](media/sample-retail-analysis/retail8.png)
2. <span data-ttu-id="7ec2d-159">ตอนนี้เปลี่ยนคำถามเป็น _ยอดขายของปีนี้ **แยกตามเขตพื้นที่และเชนธุรกิจ**_</span><span class="sxs-lookup"><span data-stu-id="7ec2d-159">Now change the question to _this year sales **by zip and chain**_.</span></span>

   <span data-ttu-id="7ec2d-160">โปรดสังเกตวิธีการที่ Power BI ตอบคำถามขณะที่คุณพิมพ์และแสดงแผนภูมิที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="7ec2d-160">Notice how Power BI answers the question as you type and displays the appropriate chart.</span></span>
3. <span data-ttu-id="7ec2d-161">ลองใช้คำถามเพิ่มเติมและดูประเภทของผลลัพธ์ที่คุณได้</span><span class="sxs-lookup"><span data-stu-id="7ec2d-161">Experiment with more questions and see what kind of results you get.</span></span>
4. <span data-ttu-id="7ec2d-162">เมื่อคุณพร้อมแล้ว ให้ย้อนกลับไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="7ec2d-162">When you're ready, return to the dashboard.</span></span>

## <a name="dive-deeper-into-the-data"></a><span data-ttu-id="7ec2d-163">เจาะลึกลงในข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="7ec2d-163">Dive deeper into the data</span></span>
<span data-ttu-id="7ec2d-164">ตอนนี้เรามาสำรวจในระดับที่ละเอียดยิ่งขึ้นโดยดูที่การดำเนินการของแต่ละเขต</span><span class="sxs-lookup"><span data-stu-id="7ec2d-164">Now let's explore on a more detailed level, looking at the districts' performances.</span></span>

1. <span data-ttu-id="7ec2d-165">บนแดชบอร์ด เลือกไทล์ **ยอดขายของปีนี้ ยอดขายของปีที่แล้ว** ซึ่งเปิดหน้า **ยอดขายรายเดือนของเขต** ของรายงาน</span><span class="sxs-lookup"><span data-stu-id="7ec2d-165">On the dashboard, select the **This Year's Sales, Last Year's Sales** tile, which opens the **District Monthly Sales** page of the report.</span></span>

   ![ไทล์ยอดขายของปีนี้, ยอดขายของปีที่แล้ว](media/sample-retail-analysis/pbi_sample_retanlareacht.png)

   <span data-ttu-id="7ec2d-167">ในแผนภูมิ **% ผลต่างของยอดขายรวมตามเดือนงบประมาณ** สังเกตว่ามีการแปรผันอย่างมากเกี่ยวกับ % ผลต่างเมื่อเปรียบเทียบกับปีที่แล้ว กับมกราคม เมษายน และกรกฎาคม ซึ่งเป็นเดือนที่มีผลประกอบการไม่ดี</span><span class="sxs-lookup"><span data-stu-id="7ec2d-167">In the **Total Sales Variance % by Fiscal Month** chart, notice the large variability on variance % compared to last year, with January, April, and July being particularly bad months.</span></span>

   ![% ผลต่างของยอดขายรวมตามเดือนงบประมาณ](media/sample-retail-analysis/pbi_sample_retanlsalesvarcol.png)

   <span data-ttu-id="7ec2d-169">มาดูว่าเราสามารถดูรายละเอียดได้หรือไม่ว่าปัญหามาจากที่ใด</span><span class="sxs-lookup"><span data-stu-id="7ec2d-169">Let's see if we can narrow down where the issues might be.</span></span>
2. <span data-ttu-id="7ec2d-170">ในแผนภูมิฟอง เลือกแบบฟอง **020-Mens**</span><span class="sxs-lookup"><span data-stu-id="7ec2d-170">In the bubble chart, select the **020-Mens** bubble.</span></span>

   ![เลือก 020-Mens](media/sample-retail-analysis/retail11.png)  

   <span data-ttu-id="7ec2d-172">สังเกตว่าแม้สินค้าในหมวดสินค้าผู้ชายไม่ได้รับผลกระทบอย่างร้ายแรงในเดือนเมษายนตามผลประกอบการธุรกิจโดยรวม แต่เดือนมกราคมและกรกฎาคมยังคงเป็นเดือนที่มีปัญหา</span><span class="sxs-lookup"><span data-stu-id="7ec2d-172">Observe that although the men's category wasn't as severely affected in April as the overall business, January and July were still problematic months.</span></span>
1. <span data-ttu-id="7ec2d-173">เลือกแบบฟอง **010-Womens**</span><span class="sxs-lookup"><span data-stu-id="7ec2d-173">Select the **010-Womens** bubble.</span></span>

   ![เลือก 010-Womens](media/sample-retail-analysis/retail12.png)

   <span data-ttu-id="7ec2d-175">คุณจะสังเกตเห็นว่าสินค้าในหมวดสินค้าผู้หญิงนั้นมีผลประกอบการแย่กว่าผลประกอบการโดยรวมในทุกเดือน และแย่กว่ามากในเกือบทุกเดือนเมื่อเทียบกับปีก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="7ec2d-175">Notice the women's category performed much worse than the overall business across all months, and in almost every month compared to the previous year.</span></span>
1. <span data-ttu-id="7ec2d-176">เลือกแผนภูมิฟองอีกครั้งเพื่อล้างตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="7ec2d-176">Select the bubble again to clear the filter.</span></span>

## <a name="try-out-the-slicer"></a><span data-ttu-id="7ec2d-177">ลองใช้ตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7ec2d-177">Try out the slicer</span></span>
<span data-ttu-id="7ec2d-178">มาดูว่าในบางเขตมีผลประกอบการเป็นอย่างไรบ้าง</span><span class="sxs-lookup"><span data-stu-id="7ec2d-178">Let's look at how specific districts are doing.</span></span>

1. <span data-ttu-id="7ec2d-179">เลือก **Allan Guinot** ในตัวแบ่งส่วนข้อมูล **ผู้จัดการเขต** ด้านบนซ้าย</span><span class="sxs-lookup"><span data-stu-id="7ec2d-179">Select **Allan Guinot** in the **District Manager** slicer on the top left.</span></span>

   ![เลือก Allan Guinot](media/sample-retail-analysis/retail13.png)

   <span data-ttu-id="7ec2d-181">โปรดทราบว่าเขตของ Allan มีผลประกอบการที่ดีกว่าที่อื่นในเดือนมีนาคมและเดือนมิถุนายน เทียบกับปีที่แล้ว</span><span class="sxs-lookup"><span data-stu-id="7ec2d-181">Note that Allan's district outperformed in March and June, compared to last year.</span></span>
2. <span data-ttu-id="7ec2d-182">เมื่อยังคงเลือก **Allan Guinot** ให้เลือกแบบฟอง **Womens-10** ในแผนภูมิฟอง</span><span class="sxs-lookup"><span data-stu-id="7ec2d-182">With **Allan Guinot** still selected, select the **Womens-10** bubble in the bubble chart.</span></span>

   ![Allan Guinot และ Womens-10 ที่เลือก](media/sample-retail-analysis/power-bi-allan.png)

   <span data-ttu-id="7ec2d-184">Notice that for the Womens-10 category, Allan's district didn't meet last year's volume.</span><span class="sxs-lookup"><span data-stu-id="7ec2d-184">Notice that for the Womens-10 category, Allan's district didn't meet last year's volume.</span></span>
3. <span data-ttu-id="7ec2d-185">สำรวจผู้จัดการเขตอื่นและสินค้าหมวดอื่น ข้อมูลเชิงลึกอื่น ๆ ที่คุณสามารถค้นหาได้ มีอะไรบ้าง?</span><span class="sxs-lookup"><span data-stu-id="7ec2d-185">Explore the other district managers and categories; what other insights can you find?</span></span>
4. <span data-ttu-id="7ec2d-186">เมื่อคุณพร้อมแล้ว ให้ย้อนกลับไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="7ec2d-186">When you are ready, return to the dashboard.</span></span>

## <a name="what-the-data-says-about-sales-growth-this-year"></a><span data-ttu-id="7ec2d-187">ข้อมูลระบุเกี่ยวกับการเพิ่มยอดขายปีนี้</span><span class="sxs-lookup"><span data-stu-id="7ec2d-187">What the data says about sales growth this year</span></span>
<span data-ttu-id="7ec2d-188">ส่วนสุดท้ายที่เราต้องการสำรวจคือการเติบโตของเรา โดยการสำรวจร้านค้าใหม่ ๆ ที่เปิดขึ้นในปีนี้</span><span class="sxs-lookup"><span data-stu-id="7ec2d-188">The last area we want to explore is our growth by examining the new stores opened this year.</span></span>

1. <span data-ttu-id="7ec2d-189">เลือกไทล์ **ร้านค้าที่เปิดในปีนี้ตามเดือนเปิด, เชนธุรกิจ** ซึ่งเปิดหน้า **การวิเคราะห์ร้านค้าใหม่** ของรายงาน</span><span class="sxs-lookup"><span data-stu-id="7ec2d-189">Select the **Stores Opened This Year by Open Month, Chain** tile, which opens the **New Stores Analysis** page of the report.</span></span>

   ![หน้าการวิเคราะห์ร้านค้าใหม่](media/sample-retail-analysis/retail15.png)

   <span data-ttu-id="7ec2d-191">มีร้านค้าของ Fashions Direct เปิดขึ้นในปีนี้มากกว่าร้านค้าของ Lindseys โดยเราจะเห็นได้ชัดเจนจากไทล์</span><span class="sxs-lookup"><span data-stu-id="7ec2d-191">As evident from the tile, more Fashions Direct stores than Lindseys stores opened this year.</span></span>
2. <span data-ttu-id="7ec2d-192">สำรวจแผนภูมิ **ยอดขายต่อตารางฟุตแยกตามชื่อ**:</span><span class="sxs-lookup"><span data-stu-id="7ec2d-192">Observe the **Sales Per Sq Ft by Name** chart:</span></span>

   ![แผนภูมิยอดขายต่อตารางฟุตตามชื่อ](media/sample-retail-analysis/retail14.png)

    <span data-ttu-id="7ec2d-194">โปรดสังเกตความแตกต่างในยอดขาย/ตารางฟุตโดยเฉลี่ยทั่วทั้งร้านค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="7ec2d-194">Notice the difference in average sales/square foot across the new stores.</span></span>
3. <span data-ttu-id="7ec2d-195">เลือกรายการคำอธิบายแผนภูมิ **Fashions Direct** ในแผนภูมิด้านบนขวา **จำนวนร้านค้าที่เปิดตามเดือนที่เปิดและเชนธุรกิจ**</span><span class="sxs-lookup"><span data-stu-id="7ec2d-195">Select the **Fashions Direct** legend item in the **Open Store Count by Open Month and Chain** top-right chart.</span></span> <span data-ttu-id="7ec2d-196">โปรดสังเกตว่าแม้แต่ธุรกิจเชนเดียวกัน ร้านค้าที่ดีที่สุด (Winchester Fashions Direct) มีผลประกอบการดีกว่าร้านค้าที่มีผลประกอบการแย่อย่างมีนัยสำคัญ (Cincinnati 2 Fashions Direct) โดยมีผลประกอบการ $21.22 เทียบกับ $12.86 ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="7ec2d-196">Notice, even for the same chain, the best store (Winchester Fashions Direct) significantly outperforms the worst store (Cincinnati 2 Fashions Direct) by $21.22 vs $12.86, respectively.</span></span>

   ![Fashions Direct ที่เลือก](media/sample-retail-analysis/power-bi-lindseys.png)
4. <span data-ttu-id="7ec2d-198">เลือก **Winchester Fashions Direct** ในตัวแบ่งส่วนข้อมูล **ชื่อ** และสังเกตแผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="7ec2d-198">Select **Winchester Fashions Direct** in the **Name** slicer and observe the line chart.</span></span> <span data-ttu-id="7ec2d-199">มีการรายงานตัวเลขยอดขายแรกในเดือนกุมภาพันธ์</span><span class="sxs-lookup"><span data-stu-id="7ec2d-199">The first sales numbers were reported in February.</span></span>
5. <span data-ttu-id="7ec2d-200">เลือก **Cincinnati 2 Fashions Direct** ในตัวแบ่งส่วนข้อมูล และสังเกตในแผนภูมิเส้นว่าร้านค้านี้เปิดในเดือนมิถุนายน และดูเหมือนว่าเป็นร้านที่มีผลประกอบการแย่ที่สุด</span><span class="sxs-lookup"><span data-stu-id="7ec2d-200">Select **Cincinnati 2 Fashions Direct** in the slicer and observe in the line chart that it was opened in June and appears to be the worst performing store.</span></span>
6. <span data-ttu-id="7ec2d-201">สำรวจโดยการเลือกแถบ เส้นและฟองอื่น ๆ ตลอดทั้งแผนภูมิและดูข้อมูลเชิงลึกที่คุณสามารถค้นหาได้</span><span class="sxs-lookup"><span data-stu-id="7ec2d-201">Explore by selecting other bars, lines, and bubbles throughout the charts and see what insights you can discover.</span></span>

## <a name="next-steps-connect-to-your-data"></a><span data-ttu-id="7ec2d-202">ขั้นตอนถัดไป: เชื่อมต่อไปยังข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="7ec2d-202">Next steps: Connect to your data</span></span>
<span data-ttu-id="7ec2d-203">สภาพแวดล้อมนี้มีความปลอดภัยให้ดำเนินการต่าง ๆ ได้ เนื่องจากคุณสามารถเลือกที่จะไม่บันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="7ec2d-203">This environment is a safe one to play in, because you can choose not to save your changes.</span></span> <span data-ttu-id="7ec2d-204">ถ้าคุณบันทึก คุณสามารถเลือก **รับข้อมูล** สำหรับสำเนาชุดใหม่ของตัวอย่างนี้ได้เสมอ</span><span class="sxs-lookup"><span data-stu-id="7ec2d-204">But if you do save them, you can always select **Get Data** for a new copy of this sample.</span></span>

<span data-ttu-id="7ec2d-205">เราหวังว่าการแนะนำนี้ได้แสดงให้เห็นว่าแดชบอร์ด Q&A และรายงาน Power BI สามารถให้ข้อมูลเชิงลึกในข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="7ec2d-205">We hope this tour has shown how Power BI dashboards, Q&A, and reports can provide insights into sample data.</span></span> <span data-ttu-id="7ec2d-206">ตอนนี้ถึงตาคุณแล้ว ลองเชื่อมต่อกับข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="7ec2d-206">Now it's your turn; connect to your own data.</span></span> <span data-ttu-id="7ec2d-207">ด้วย Power BI คุณสามารถเชื่อมต่อกับแหล่งข้อมูลที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="7ec2d-207">With Power BI, you can connect to a wide variety of data sources.</span></span> <span data-ttu-id="7ec2d-208">เมื่อต้องการเรียนรู้เพิ่มเติม ดู[เริ่มต้นใช้งานบริการ Power BI](../fundamentals/service-get-started.md)</span><span class="sxs-lookup"><span data-stu-id="7ec2d-208">To learn more, see [Get started with the Power BI service](../fundamentals/service-get-started.md).</span></span>
