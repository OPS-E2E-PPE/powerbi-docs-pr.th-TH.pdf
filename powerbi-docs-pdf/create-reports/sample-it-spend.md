---
title: 'ตัวอย่างการวิเคราะห์การใช้จ่ายด้าน IT สำหรับ Power BI: ชมการแนะนำ'
description: 'ตัวอย่างการวิเคราะห์การใช้จ่ายด้าน IT สำหรับ Power BI: ชมการแนะนำ'
author: maggiesMSFT
ms.author: maggies
ms.reviewer: amac
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: conceptual
ms.date: 07/05/2019
LocalizationGroup: Samples
ms.openlocfilehash: cdde0e702333feed54637c72fa3193052fde139f
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414978"
---
# <a name="it-spend-analysis-sample-for-power-bi-take-a-tour"></a><span data-ttu-id="532a1-103">ตัวอย่างการวิเคราะห์การใช้จ่ายด้าน IT สำหรับ Power BI: ชมการแนะนำ</span><span class="sxs-lookup"><span data-stu-id="532a1-103">IT Spend Analysis sample for Power BI: Take a tour</span></span>

<span data-ttu-id="532a1-104">การวิเคราะห์การใช้จ่ายด้าน IT ตัวอย่างชุดเนื้อหา ที่มีแดชบอร์ด รายงาน และชุดข้อมูล  วิเคราะห์ค่าใช้จ่ายที่วางแผนเทียบกับที่ใช้จริงของแผนก IT</span><span class="sxs-lookup"><span data-stu-id="532a1-104">The IT Spend Analysis sample content pack contains a dashboard, report, and dataset that analyzes the planned vs. actual costs of an IT department.</span></span> <span data-ttu-id="532a1-105">การเปรียบเทียบนี้ช่วยให้เรา เข้าใจว่าบริษัทวางแผนไว้สำหรับปีได้ดีแค่ไหน และตรวจสอบด้านที่มีความแตกต่างอย่างมากจากแผน</span><span class="sxs-lookup"><span data-stu-id="532a1-105">This comparison helps us understand how well the company planned for the year and investigate areas with huge deviations from the plan.</span></span> <span data-ttu-id="532a1-106">บริษัทในตัวอย่างนี้ ใช้การวางแผนรายปี จากนั้นก็มีการประเมินล่าสุด (Latest Estimation, LE) รายไตรมาส เพื่อช่วยวิเคราะห์การเปลี่ยนแปลงของรายจ่าย IT ตลอดช่วงปีงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="532a1-106">The company in this example goes through a yearly planning cycle, and then quarterly it produces a new latest estimate (LE) to help analyze changes in IT spend over the fiscal year.</span></span>

![แดชบอร์ดตัวอย่างการวิเคราะห์การใช้จ่ายด้าน IT](media/sample-it-spend/it1.png)

<span data-ttu-id="532a1-108">ตัวอย่างนี้เป็นส่วนหนึ่งของชุดตัวอย่าง ที่แสดงให้เห็นวิธีการที่คุณสามารถใช้ Power BI กับข้อมูล รายงาน และแดชบอร์ดที่เกี่ยวข้องกับธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="532a1-108">This sample is part of a series that shows how you can use Power BI with business-oriented data, reports, and dashboards.</span></span> <span data-ttu-id="532a1-109">ซึ่งสร้างขึ้นโดย [obviEnce](http://www.obvience.com/) ด้วยข้อมูลจริงที่ไม่มีการระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="532a1-109">It was created by [obviEnce](http://www.obvience.com/) with real data, which has been anonymized.</span></span> <span data-ttu-id="532a1-110">ข้อมูลมีให้ใช้งานหลายรูปแบบ: ชุดเนื้อหา ไฟล์ Power BI Desktop .pbix หรือเวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="532a1-110">The data is available in several formats: content pack, .pbix Power BI Desktop file, or Excel workbook.</span></span> <span data-ttu-id="532a1-111">ดู [ตัวอย่างสำหรับ Power BI](sample-datasets.md)</span><span class="sxs-lookup"><span data-stu-id="532a1-111">See [Samples for Power BI](sample-datasets.md).</span></span> 

<span data-ttu-id="532a1-112">บทช่วยสอนนี้จะสำรวจชุดเนื้อหาของตัวอย่างการวิเคราะห์การใช้จ่ายด้าน IT ในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="532a1-112">This tutorial explores the IT Spend Analysis sample content pack in the Power BI service.</span></span> <span data-ttu-id="532a1-113">เนื่องจากประสบการณ์การใช้รายงานจะคล้ายคลึงกันใน Power BI Desktop ดังนั้นคุณสามารถใช้ Power BI Desktop กับไฟล์ .pbix ตัวอย่างใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="532a1-113">Because the report experience is similar in Power BI Desktop and in the service, you can also follow along by using the sample .pbix file in Power BI Desktop.</span></span> 

<span data-ttu-id="532a1-114">คุณไม่จำเป็นต้องมีสิทธิการใช้งาน Power BI ในการสำรวจตัวอย่างใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="532a1-114">You don't need a Power BI license to explore the samples in Power BI Desktop.</span></span> <span data-ttu-id="532a1-115">ถ้าคุณไม่มีสิทธิการใช้งาน Power BI Pro คุณสามารถบันทึกตัวอย่างไปยังพื้นที่ทำงานของฉันในบริการของ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="532a1-115">If you don't have a Power BI Pro license, you can save the sample to your My Workspace in the Power BI service.</span></span> 

## <a name="get-the-sample"></a><span data-ttu-id="532a1-116">รับตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="532a1-116">Get the sample</span></span>

 <span data-ttu-id="532a1-117">ก่อนที่คุณสามารถใช้ตัวอย่าง คุณต้องดาวน์โหลดในรูปแบบ[ชุดเนื้อหา](#get-the-content-pack-for-this-sample)[ไฟล์ .pbix](#get-the-pbix-file-for-this-sample) หรือ[เวิร์กบุ๊ก Excel](#get-the-excel-workbook-for-this-sample)</span><span class="sxs-lookup"><span data-stu-id="532a1-117">Before you can use the sample, you must first download it as a [content pack](#get-the-content-pack-for-this-sample), [.pbix file](#get-the-pbix-file-for-this-sample), or [Excel workbook](#get-the-excel-workbook-for-this-sample).</span></span>

### <a name="get-the-content-pack-for-this-sample"></a><span data-ttu-id="532a1-118">รับชุดเนื้อหาสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="532a1-118">Get the content pack for this sample</span></span>

1. <span data-ttu-id="532a1-119">เปิดบริการ Power BI (app.powerbi.com) ลงชื่อเข้าใช้ และเปิดพื้นที่ทำงานที่คุณต้องการบันทึกตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="532a1-119">Open the Power BI service (app.powerbi.com), sign in, and open the workspace where you want to save the sample.</span></span>

   <span data-ttu-id="532a1-120">ถ้าคุณไม่มีสิทธิการใช้งาน Power BI Pro คุณสามารถบันทึกตัวอย่างไปยังพื้นที่ทำงานของฉัน</span><span class="sxs-lookup"><span data-stu-id="532a1-120">If you don't have a Power BI Pro license, you can save the sample to your My Workspace.</span></span>

2. <span data-ttu-id="532a1-121">ที่มุมด้านล่างซ้าย เลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="532a1-121">In the bottom-left corner, select **Get Data**.</span></span>
   
   ![เลือกรับข้อมูล](media/sample-datasets/power-bi-get-data.png)
3. <span data-ttu-id="532a1-123">บนหน้า **รับข้อมูล** ที่ปรากฏขึ้น เลือก **ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="532a1-123">On the **Get Data** page that appears, select **Samples**.</span></span>
   
4. <span data-ttu-id="532a1-124">เลือก **ตัวอย่างการวิเคราะห์การใช้จ่ายด้าน IT** แล้วเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="532a1-124">Select **IT Spend Analysis Sample**, then choose **Connect**.</span></span>  
  
   ![เชื่อมต่อกับตัวอย่าง](media/sample-it-spend/it-connect.png)
   
5. <span data-ttu-id="532a1-126">Power BI นำเข้าชุดเนื้อหา จากนั้นเพิ่มแดชบอร์ด รายงาน และชุดข้อมูลใหม่ไปยังพื้นที่ทำงานปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="532a1-126">Power BI imports the content pack and then adds a new dashboard, report, and dataset to your current workspace.</span></span>
   
   ![รายการตัวอย่างการวิเคราะห์การใช้จ่ายด้าน IT](media/sample-it-spend/it-spend-analysis-sample-entry.png)
  
### <a name="get-the-pbix-file-for-this-sample"></a><span data-ttu-id="532a1-128">รับไฟล์ .pbix สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="532a1-128">Get the .pbix file for this sample</span></span>

<span data-ttu-id="532a1-129">อีกทางเลือกหนึ่งคือ คุณสามารถดาวน์โหลดตัวอย่างการวิเคราะห์การใช้จ่ายด้าน IT เป็น[ไฟล์ .pbix](https://download.microsoft.com/download/E/9/8/E98CEB6D-CEBB-41CF-BA2B-1A1D61B27D87/IT%20Spend%20Analysis%20Sample%20PBIX.pbix) ซึ่งถูกออกแบบมาสำหรับใช้กับ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="532a1-129">Alternatively, you can download the IT Spend Analysis sample as a [.pbix file](https://download.microsoft.com/download/E/9/8/E98CEB6D-CEBB-41CF-BA2B-1A1D61B27D87/IT%20Spend%20Analysis%20Sample%20PBIX.pbix), which is designed for use with Power BI Desktop.</span></span>

### <a name="get-the-excel-workbook-for-this-sample"></a><span data-ttu-id="532a1-130">รับเวิร์กบุ๊ก Excel สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="532a1-130">Get the Excel workbook for this sample</span></span>

<span data-ttu-id="532a1-131">ถ้าคุณต้องการดูแหล่งข้อมูลสำหรับตัวอย่างนี้ ตัวอย่างนี้ยังมีให้ในรูปแบบ[เวิร์กบุ๊ก Excel](https://go.microsoft.com/fwlink/?LinkId=529783)</span><span class="sxs-lookup"><span data-stu-id="532a1-131">If you want to view the data source for this sample, it's also available as an [Excel workbook](https://go.microsoft.com/fwlink/?LinkId=529783).</span></span> <span data-ttu-id="532a1-132">เวิร์กบุ๊กประกอบด้วยแผ่นงาน Power View ที่คุณสามารถดู และปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="532a1-132">The workbook contains Power View sheets that you can view and modify.</span></span> <span data-ttu-id="532a1-133">หากต้องการดูข้อมูลดิบ ให้เปิดใช้งาน add-in การวิเคราะห์ข้อมูล แล้วจากนั้นเลือก **Power Pivot > จัดการ**</span><span class="sxs-lookup"><span data-stu-id="532a1-133">To see the raw data, enable the Data Analysis add-ins, and then select **Power Pivot > Manage**.</span></span> <span data-ttu-id="532a1-134">หากต้องการเปิดใช้งาน Power View และ Power Pivot add-in โปรดดู [สำรวจตัวอย่าง Excel ใน Excel ](sample-datasets.md#explore-excel-samples-inside-excel)สำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="532a1-134">To enable the Power View and Power Pivot add-ins, see [Explore the Excel samples in Excel](sample-datasets.md#explore-excel-samples-inside-excel) for details.</span></span>

## <a name="it-spend-analysis-sample-dashboard"></a><span data-ttu-id="532a1-135">แดชบอร์ดตัวอย่างการวิเคราะห์การใช้จ่ายด้าน IT</span><span class="sxs-lookup"><span data-stu-id="532a1-135">IT Spend Analysis Sample dashboard</span></span>
<span data-ttu-id="532a1-136">ไทล์ตัวเลขสองไทล์ที่อยู่บนด้านซ้ายของแดชบอร์ด **%แปรปรวน แผน** และ **%แปรปรวน ประเมินล่าสุด ไตรมาสที่ 3** บอกภาพรวมว่าเราดำเนินไปอย่างไร เทียบกับแผน และเทียบกับการประเมินในไตรมาสล่าสุด (LE3 =ประเมินล่าสุดไตรมาส 3)</span><span class="sxs-lookup"><span data-stu-id="532a1-136">The two numbers tiles on the left of the dashboard, **Var Plan %** and **Variance Latest Estimate % Quarter 3**, give us an overview of how well we're doing against the plan and against the latest quarterly estimate (LE3 = latest estimate quarter 3).</span></span> <span data-ttu-id="532a1-137">โดยรวมแล้ว เราผิดไปจากแผนประมาณ 6%</span><span class="sxs-lookup"><span data-stu-id="532a1-137">Overall, we're about 6% off the plan.</span></span> <span data-ttu-id="532a1-138">เราลองมาสำรวจสาเหตุของความแปรปรวนนี้: เมื่อใด ที่ไหน และในประเภทใด</span><span class="sxs-lookup"><span data-stu-id="532a1-138">Let's explore the cause of this variance: when, where, and in which category.</span></span>

## <a name="ytd-it-spend-trend-analysis-page"></a><span data-ttu-id="532a1-139">หน้าการวิเคราะห์แนวโน้มการใช้จ่ายด้าน IT YTD</span><span class="sxs-lookup"><span data-stu-id="532a1-139">YTD IT Spend Trend Analysis page</span></span>
<span data-ttu-id="532a1-140">เมื่อคุณเลือกเลือกที่ไทล์แดชบอร์ด **%ความแปรปรวน แผน ตามภูมิภาค** ระบบจะแสดง **การวิเคราะห์แนวโน้มการใช้จ่ายด้าน IT** ของรายงานตัวอย่างการวิเคราะห์การใช้จ่ายด้าน IT</span><span class="sxs-lookup"><span data-stu-id="532a1-140">When you select the **Var Plan % by Sales Region** dashboard tile, it displays the **YTD IT Spend Trend Analysis** page of the IT Spend Analysis Sample report.</span></span> <span data-ttu-id="532a1-141">เห็นได้อย่างรวดเร็วว่าเรามีค่าความแปรปรวนด้านบวกในสหรัฐอเมริกา และยุโรป และด้านลบในแคนาดา ละตินอเมริกา และออสเตรเลีย</span><span class="sxs-lookup"><span data-stu-id="532a1-141">At a glance, we see that we have positive variance in the United States and Europe and negative variance in Canada, Latin America, and Australia.</span></span> <span data-ttu-id="532a1-142">สหรัฐอเมริกามีค่าความแปรปรวน +LE ประมาณ 6% และออสเตรเลียมีค่าความแปรปรวน -LE ประมาณ 7%</span><span class="sxs-lookup"><span data-stu-id="532a1-142">The United States has about 6% +LE variance and Australia has about 7% -LE variance.</span></span>

![% การวางแผนการใช้ประโยชน์ที่ดินตามภูมิภาคการขาย](media/sample-it-spend/it2.png)

<span data-ttu-id="532a1-144">อย่างไรก็ตามแค่ดูแผนภูมินี้และสรุป สามารถทำให้เข้าใจผิดได้</span><span class="sxs-lookup"><span data-stu-id="532a1-144">However, just looking at this chart and drawing conclusions can be misleading.</span></span> <span data-ttu-id="532a1-145">เราจำเป็นต้องดูที่จำนวนเงินจริง ๆ เพื่อให้เห็นภาพที่ถูกต้องยิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="532a1-145">We need to look at actual dollar amounts to put things in perspective.</span></span>

1. <span data-ttu-id="532a1-146">เลือก **ออสเตรเลียและนิวซีแลนด์** ในแผนภูมิ **%ความแปรปรวน แผน ตามภูมิภาค** และดู **แผนภูมิ ความแปรปรวน แผน ตามด้านของ IT**</span><span class="sxs-lookup"><span data-stu-id="532a1-146">Select **Aus and NZ** in the **Var Plan % by Sales Region** chart, and then observe the **Var Plan by IT Area** chart.</span></span>

   ![หน้าการวิเคราะห์แนวโน้มการใช้จ่ายด้าน IT YTD](media/sample-it-spend/it3.png)
2. <span data-ttu-id="532a1-148">ตอนนี้ เลือก **สหรัฐอเมริกา**</span><span class="sxs-lookup"><span data-stu-id="532a1-148">Now select **USA**.</span></span> <span data-ttu-id="532a1-149">โปรดสังเกตว่า ออสเตรเลียและนิวซีแลนด์เป็นส่วนหนึ่งของค่าใช้จ่ายของเราโดยรวมมาเทียบกับสหรัฐอเมริกาซึ่งมีขนาดเล็กมาก</span><span class="sxs-lookup"><span data-stu-id="532a1-149">Notice that Australia and New Zealand are a very small part of our overall spending as compared to the United States.</span></span>

    <span data-ttu-id="532a1-150">ต่อไป เรามาสำรวจว่าประเภทใดในสหรัฐอเมริกาที่ทำให้เกิดความแปรปรวน</span><span class="sxs-lookup"><span data-stu-id="532a1-150">Next, let's explore which category in the USA is causing the variance.</span></span>

## <a name="ask-questions-of-the-data"></a><span data-ttu-id="532a1-151">ถามคำถามจากข้อมูล</span><span class="sxs-lookup"><span data-stu-id="532a1-151">Ask questions of the data</span></span>
1. <span data-ttu-id="532a1-152">เลือก **ตัวอย่างการวิเคราะห์การใช้จ่ายด้าน IT** ในบานหน้าต่างนำทางด้านบนเพื่อกลับไปยังตัวอย่างแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="532a1-152">Select **IT Spend Analysis Sample** in the top nav pane to return to the sample dashboard.</span></span>
2. <span data-ttu-id="532a1-153">เลือก **ถามคำถามเกี่ยวกับข้อมูลของคุณ**</span><span class="sxs-lookup"><span data-stu-id="532a1-153">Select **Ask a question about your data**.</span></span>
3. <span data-ttu-id="532a1-154">จากรายการ **คำถามเพื่อเริ่มต้นใช้** ทางด้านซ้าย เลือก **อะไรคือแผนตามพื้นที่ไอที**</span><span class="sxs-lookup"><span data-stu-id="532a1-154">From the **Questions to get you started** list on the left side, select **what is the plan by IT area**.</span></span>

   ![กราฟการวางแผนการใช้ประโยชน์ที่ดินตามพื้นที่ไอที](media/sample-it-spend/it-area-chart.png)

4. <span data-ttu-id="532a1-156">ในกล่องถามตอบ ล้างรายการก่อนหน้า และใส่ *แสดงพื้นที่ IT, %ความแปรปรวนแผน% และใช้ประโยชน์ที่ดิน le3 แผนภูมิแท่ง*</span><span class="sxs-lookup"><span data-stu-id="532a1-156">In the Q&A box, clear the previous entry and enter *show IT areas, var plan % and var le3 % bar chart*.</span></span>

   ![% การวางแผนการใช้ประโยชน์ที่ดินและ % การใช้ประโยชน์ที่ดิน LE3 ตามพื้นที่ไอที](media/sample-it-spend/it4.png)

   <span data-ttu-id="532a1-158">ในด้านแรกของ IT ซึ่งก็คือ **โครงสร้างพื้นฐาน** สังเกตว่าเปอร์เซ็นต์มีการเปลี่ยนแปลงอย่างรวดเร็ว ระหว่างค่าความแปรปรวนของแผนเริ่มต้น และค่าความแปรปรวนของแผนจากการประเมินล่าสุด</span><span class="sxs-lookup"><span data-stu-id="532a1-158">In the first IT area, **Infrastructure**, notice that the percentage has changed drastically between the initial variance plan and the variance plan latest estimate.</span></span>

## <a name="ytd-spend-by-cost-elements-page"></a><span data-ttu-id="532a1-159">หน้าการใช้จ่าย ตามประเภทค่าใช้จ่าย YTD</span><span class="sxs-lookup"><span data-stu-id="532a1-159">YTD Spend by Cost Elements page</span></span>

1. <span data-ttu-id="532a1-160">กลับไปยังแดชบอร์ดและดูไทล์แดชบอร์ด **%ความแปรปรวนแผน %การประเมินค่าความแปรปรวนล่าสุด - ไตรมาสที่ 3**</span><span class="sxs-lookup"><span data-stu-id="532a1-160">Return to the dashboard and look at the **Variance Plan %, Variance Latest Estimate % - Quarter 3** dashboard tile.</span></span>

   ![ไทล์ %ความแปรปรวนแผน, %ความแปรปรวน LE3](media/sample-it-spend/it5.png)

   <span data-ttu-id="532a1-162">โปรดสังเกตว่า พื้นที่โครงสร้างพื้นฐานที่โดดเด่นมากกับเป็นค่าความแปรปรวนบวกขนาดใหญ่เมื่อเทียบกับแผน</span><span class="sxs-lookup"><span data-stu-id="532a1-162">Notice that the Infrastructure area stands out with a large positive variance to the plan.</span></span>

1. <span data-ttu-id="532a1-163">เลือกไทล์นี้เพื่อเปิดหน้ารายงานและมุมมอง **YTD ใช้จ่ายตามประเภทค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="532a1-163">Select this tile to open the report and view the **YTD Spend by Cost Elements** page.</span></span>
2. <span data-ttu-id="532a1-164">เลือกที่แท่ง **โครงสร้างพื้นฐาน** ในแผนภูมิ **%ความแปรปรวน แผน %ความแปรปรวน LE3 ตามด้านของ IT** ในด้านล่างซ้าย และสังเกตค่าความแปรปรวนเทียบกับแผนใน **%ความแปรปรวน แผน ตามภูมิภาคการขาย** ทางด้านซ้ายด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="532a1-164">Select the **Infrastructure** bar in the **Var Plan % and Var LE3 % by IT Area** chart on the lower right, and observe the variance-to-plan values in the **Var Plan % by Sales Region** chart on the lower left.</span></span>

    ![หน้าการใช้จ่าย ตามประเภทค่าใช้จ่าย YTD](media/sample-it-spend/it6.png)
3. <span data-ttu-id="532a1-166">เลือกตัวแบ่งส่วนข้อมูลแต่ละชื่อในลำดับ **ค่าใช้จ่าย** เพื่อค้นหาองค์ประกอบค่าใช้จ่ายที่ มีค่าความแปรปรวนมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="532a1-166">Select each name in turn in the **Cost Element Group** slicer to find the cost element with the largest variance.</span></span>
4. <span data-ttu-id="532a1-167">เมื่อมีการเลือก **อื่น ๆ** แล้ว ให้เลือก **โครงสร้างพื้นฐาน** ในตัวแบ่งส่วนข้อมูล **ตามด้านของ IT** และเลือกด้านย่อยใน **ตัวแบ่งส่วนข้อมูล ด้านย่อยของ IT** เพื่อค้นหาด้านย่อย ที่มีความแปรปรวนมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="532a1-167">With **Other** selected, select **Infrastructure** in the **IT Area** slicer and select subareas in the **IT Sub Area** slicer to find the subarea with the largest variance.</span></span>  

   <span data-ttu-id="532a1-168">โปรดสังเกตค่าความแปรปรวนขนาดใหญ่สำหรับ **เครือข่าย**</span><span class="sxs-lookup"><span data-stu-id="532a1-168">Notice the large variance for **Networking**.</span></span> <span data-ttu-id="532a1-169">บริษัทตัดสินใจให้บริการโทรศัพท์แก่พนักงานเป็นสวัสดิการ แม้ว่าเรื่องนี้ไม่ได้วางแผนเอาไว้ก่อน</span><span class="sxs-lookup"><span data-stu-id="532a1-169">Apparently the company decided to give its employees phone services as a benefit, even though this move was not planned for.</span></span>

## <a name="plan-variance-analysis-page"></a><span data-ttu-id="532a1-170">หน้า "การวิเคราะห์ความแปรปรวนของแผน"</span><span class="sxs-lookup"><span data-stu-id="532a1-170">Plan Variance Analysis page</span></span>

1. <span data-ttu-id="532a1-171">เลือกแท็บ **วิเคราะห์ความแปรปรวนแผน** ที่ด้านล่างของหน้า</span><span class="sxs-lookup"><span data-stu-id="532a1-171">Select the **Plan Variance Analysis** tab on the bottom of the page.</span></span>

2. <span data-ttu-id="532a1-172">ในแผนภูมิ **ความแปรปรวนแผน, %ความแปรปรวนแผน ตามด้านของธุรกิจ** ทางด้านซ้าย เลือกที่คอลัมน์ **โครงสร้างพื้นฐาน** เพื่อไฮไลต์ค่าโครงสร้างพื้นฐานทางธุรกิจในส่วนเหลือของหน้า</span><span class="sxs-lookup"><span data-stu-id="532a1-172">In the **Var Plan and Var Plan % by Business Area** chart on the left, select the **Infrastructure** column to highlight infrastructure business area values in the rest of the page.</span></span>

    ![หน้า "การวิเคราะห์ความแปรปรวนของแผน"](media/sample-it-spend/it7.png)

   <span data-ttu-id="532a1-174">โปรดสังเกตว่า ในแผนภูมิ **%แผน%ความแปรปรวนตามเดือนและพื้นที่ธุรกิจ** โครงสร้างพื้นฐานเริ่มต้นค่าความแปรปรวนเป็นบวกในเดือนกุมภาพันธ์</span><span class="sxs-lookup"><span data-stu-id="532a1-174">Notice in the **Var plan % by Month and Business Area** chart that the infrastructure business area started a positive variance in February.</span></span> <span data-ttu-id="532a1-175">นอกจากนี้ยังสังเกตว่าค่าความแปรปรวนของแผน สำหรับพื้นที่ธุรกิจแตกต่างกันตามประเทศเมื่อเทียบกับค่าของทุก ๆ ด้านของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="532a1-175">Also, notice how the variance-to-plan value for that business area varies by country, as compared to all other business areas.</span></span> 

3. <span data-ttu-id="532a1-176">ใช้ตัวแบ่งส่วนข้อมูล **ด้านของ IT** และ **ด้านย่อยของ IT** ทางด้านขวาเพื่อกรองค่าในส่วนเหลือของหน้าเพื่อค้นหาข้อมูล</span><span class="sxs-lookup"><span data-stu-id="532a1-176">Use the **IT Area** and **IT Sub Area** slicers on the right to filter the values in the rest of the page and to explore the data.</span></span> 

## <a name="edit-the-report"></a><span data-ttu-id="532a1-177">แก้ไขรายงาน</span><span class="sxs-lookup"><span data-stu-id="532a1-177">Edit the report</span></span>
<span data-ttu-id="532a1-178">เลือก **แก้ไขรายงาน** ในมุมบนซ้ายเพื่อสำรวจในมุมมองการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="532a1-178">Select **Edit Report** in the upper-left corner to explore in Editing view:</span></span>

* <span data-ttu-id="532a1-179">ดูว่าหน้าถูกสร้างขึ้นอย่างไร – เขตข้อมูลในแต่ละแผนภูมิและตัวกรองบนหน้า</span><span class="sxs-lookup"><span data-stu-id="532a1-179">See how the pages are made, the fields in each chart, and the filters on the pages.</span></span>
* <span data-ttu-id="532a1-180">เพิ่มหน้าและแผนภูมิที่มาจากข้อมูลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="532a1-180">Add pages and charts, based on the same data.</span></span>
* <span data-ttu-id="532a1-181">เปลี่ยนชนิดของการแสดงภาพสำหรับแต่ละแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="532a1-181">Change the visualization type for each chart.</span></span>
* <span data-ttu-id="532a1-182">แผนภูมิปักหมุดที่สนใจแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="532a1-182">Pin charts of interest to your dashboard.</span></span>

## <a name="next-steps-connect-to-your-data"></a><span data-ttu-id="532a1-183">ขั้นตอนถัดไป: เชื่อมต่อกับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="532a1-183">Next steps: Connect to your data</span></span>
<span data-ttu-id="532a1-184">สภาพแวดล้อมนี้มีความปลอดภัยให้ดำเนินการต่างๆ ได้ เนื่องจากคุณสามารถเลือกที่จะไม่บันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="532a1-184">This environment is a safe one to play in, because you can choose not to save your changes.</span></span> <span data-ttu-id="532a1-185">ถ้าคุณบันทึก คุณสามารถเลือก **รับข้อมูล** สำหรับสำเนาชุดใหม่ของตัวอย่างนี้ได้เสมอ</span><span class="sxs-lookup"><span data-stu-id="532a1-185">But if you do save them, you can always select **Get Data** for a new copy of this sample.</span></span>

<span data-ttu-id="532a1-186">เราหวังว่าการแนะนำนี้ได้แสดงให้เห็นว่าแดชบอร์ด Q&A และรายงาน Power BI สามารถให้ข้อมูลเชิงลึกในข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="532a1-186">We hope this tour has shown how Power BI dashboards, Q&A, and reports can provide insights into sample data.</span></span> <span data-ttu-id="532a1-187">ตอนนี้ถึงตาคุณแล้ว ลองเชื่อมต่อกับข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="532a1-187">Now it's your turn; connect to your own data.</span></span> <span data-ttu-id="532a1-188">ด้วย Power BI คุณสามารถเชื่อมต่อกับแหล่งข้อมูลที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="532a1-188">With Power BI, you can connect to a wide variety of data sources.</span></span> <span data-ttu-id="532a1-189">เมื่อต้องการเรียนรู้เพิ่มเติม ดู[เริ่มต้นใช้งานบริการ Power BI](../fundamentals/service-get-started.md)</span><span class="sxs-lookup"><span data-stu-id="532a1-189">To learn more, see [Get started with the Power BI service](../fundamentals/service-get-started.md).</span></span>
