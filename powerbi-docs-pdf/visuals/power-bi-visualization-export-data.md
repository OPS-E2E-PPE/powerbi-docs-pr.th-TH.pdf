---
title: ส่งออกข้อมูลจากการแสดงภาพของ Power BI
description: ส่งออกข้อมูลจากการแสดงภาพของรายงานและการแสดงภาพของแดชบอร์ดและดูใน Excel
author: mihart
ms.author: mihart
manager: kvivek
ms.reviewer: tessa
featuredvideoid: jtlLGRKBvXY
ms.custom: jtlLGRKBvXY
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 12/21/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: bf388f28b83ad67fd246d23ba7113e74f0630a0e
ms.sourcegitcommit: 0711972326521944fdd8572403c0b15f31b916da
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/22/2020
ms.locfileid: "97721489"
---
# <a name="export-the-data-that-was-used-to-create-a-visualization"></a><span data-ttu-id="d714a-103">ส่งออกข้อมูลที่ใช้เพื่อสร้างการแสดงผลข้อมูลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="d714a-103">Export the data that was used to create a visualization</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d714a-104">ผู้ใช้ทั้งหมดไม่สามารถดูหรือส่งออกข้อมูลทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="d714a-104">Not all data can be viewed or exported by all users.</span></span> <span data-ttu-id="d714a-105">มีระบบป้องกันที่ผู้ออกแบบรายงานและผู้ดูแลระบบใช้เมื่อสร้างแดชบอร์ดและรายงาน</span><span class="sxs-lookup"><span data-stu-id="d714a-105">There are safeguards that report designers and administrators use when building dashboards and reports.</span></span> <span data-ttu-id="d714a-106">ข้อมูลบางอย่างถูกจำกัด ซ่อน หรือเป็นความลับ และไม่สามารถมองเห็นหรือส่งออกโดยปราศจากข้ออนุญาตพิเศษ</span><span class="sxs-lookup"><span data-stu-id="d714a-106">Some data is restricted, hidden, or confidential, and cannot be seen or exported without special permissions.</span></span> 

## <a name="who-can-export-data"></a><span data-ttu-id="d714a-107">ผู้ที่สามารถส่งออกข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="d714a-107">Who can export data</span></span>

<span data-ttu-id="d714a-108">ในกรณีที่คุณได้รับสิทธิ์อนุญาตสำหรับข้อมูลหนึ่ง ๆ คุณจะสามารถดูและส่งออกข้อมูลดังกล่าวที่ Power BI ใช้เพื่อสร้างการแสดงผลด้วยภาพได้</span><span class="sxs-lookup"><span data-stu-id="d714a-108">If you have permissions to the data, you can see and export the data that Power BI uses to create a visualization.</span></span> <span data-ttu-id="d714a-109">โดยข้อมูลมักจะเป็นความลับหรือจำกัดต่อผู้ใช้ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="d714a-109">Often, data is confidential or limited to specific users.</span></span> <span data-ttu-id="d714a-110">ในกรณีดังกล่าว คุณจะไม่สามารถดูหรือส่งออกข้อมูลดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="d714a-110">In those cases, you will not be able to see or export that data.</span></span> <span data-ttu-id="d714a-111">สำหรับรายละเอียดต่าง ๆ ดูที่ส่วน **ข้อจำกัดและข้อควรพิจารณา** ที่ส่วนท้ายของเอกสารนี้</span><span class="sxs-lookup"><span data-stu-id="d714a-111">For details, see the **Limitations and considerations** section at the end of this document.</span></span> 


## <a name="viewing-and-exporting-data"></a><span data-ttu-id="d714a-112">การดูและการส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d714a-112">Viewing and exporting data</span></span>

<span data-ttu-id="d714a-113">ถ้าคุณต้องการดูข้อมูลที่ Power BI ใช้ในการสร้างการแสดงภาพ [คุณสามารถแสดงข้อมูลนั้นใน Power BI](service-reports-show-data.md)</span><span class="sxs-lookup"><span data-stu-id="d714a-113">If you'd like to see the data that Power BI uses to create a visualization, [you can display that data in Power BI](service-reports-show-data.md).</span></span> <span data-ttu-id="d714a-114">คุณยังสามารถส่งออกข้อมูลไปยัง Excel ในฐานะไฟล? *.xlsx* หรือ *.csv* ได้</span><span class="sxs-lookup"><span data-stu-id="d714a-114">You can also export that data to Excel as an *.xlsx* or *.csv* file.</span></span> <span data-ttu-id="d714a-115">ตัวเลือกในการส่งออกข้อมูลต้องมีสิทธิ์การใช้งานระดับ Pro หรือ Premium รวมถึงสิทธิในการแก้ไขชุดข้อมูลและรายงาน</span><span class="sxs-lookup"><span data-stu-id="d714a-115">The option to export the data requires a Pro or Premium license as well as edit permissions to the dataset and report.</span></span> <span data-ttu-id="d714a-116">ถ้าคุณมีการเข้าถึงแดชบอร์ดหรือรายงานแต่ข้อมูลมีการจัดประเภทเป็น *ความลับสูง* Power BI จะไม่อนุญาตให้คุณส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d714a-116">If you have access to the dashboard or report but the data is classified as *highly confidential*, Power BI will not allow you to export the data.</span></span>

<span data-ttu-id="d714a-117">ดู Will ส่งออกข้อมูลจากหนึ่งในการแสดงภาพในรายงานของเขา บันทึกเป็นไฟล์  *.xlsx* และเปิดใน Excel</span><span class="sxs-lookup"><span data-stu-id="d714a-117">Watch Will export the data from one of the visualizations in his report, save it as an *.xlsx* file, and open it in Excel.</span></span> <span data-ttu-id="d714a-118">แล้วทำตามคำแนะนำทีละขั้นตอนด้านล่างวิดีโอเพื่อลองทำด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d714a-118">Then follow the step-by-step instructions below the video to try it out yourself.</span></span> <span data-ttu-id="d714a-119">โปรดทราบว่า วิดีโอนี้ใช้ Power BI เวอร์ชันเก่า</span><span class="sxs-lookup"><span data-stu-id="d714a-119">Note that this video uses an older version of Power BI.</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/KjheMTGjDXw" frameborder="0" allowfullscreen></iframe>

## <a name="export-data-from-a-power-bi-dashboard"></a><span data-ttu-id="d714a-120">ส่งออกข้อมูลจากแดชบอร์ด Power BI</span><span class="sxs-lookup"><span data-stu-id="d714a-120">Export data from a Power BI dashboard</span></span>

1. <span data-ttu-id="d714a-121">เลือกการดำเนินการเพิ่มเติม (...) จากมุมขวาบนของการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="d714a-121">Select More actions (...) from the upper-right corner of the visualization.</span></span>

    ![สกรีนช็อตของการแสดงภาพที่มีลูกศรชี้ไปยังปุ่มจุดไข่ปลา](media/power-bi-visualization-export-data/pbi-export-tile3.png)

1. <span data-ttu-id="d714a-123">เลือกตัวเลือก **ส่งออกเป็น .csv**</span><span class="sxs-lookup"><span data-stu-id="d714a-123">Choose the **Export to .csv** option.</span></span>

    ![สกรีนช็อตของการเรียกรายการเมนูดรอปดาวน์ ด้วยตัวเลือกข้อมูลส่งออก](media/power-bi-visualization-export-data/power-bi-export-data.png)

1. <span data-ttu-id="d714a-125">Power BI ส่งออกข้อมูลเป็นไฟล์ *.csv*</span><span class="sxs-lookup"><span data-stu-id="d714a-125">Power BI exports the data to a *.csv* file.</span></span> <span data-ttu-id="d714a-126">หากคุณกรองการแสดงภาพ การส่งออกไฟล์ .csv จะถูกกรองเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="d714a-126">If you've filtered the visualization, then the .csv export will be filtered as well.</span></span> 

1. <span data-ttu-id="d714a-127">เบราว์เซอร์ของคุณจะปรากฏขึ้นให้คุณบันทึกไฟล์</span><span class="sxs-lookup"><span data-stu-id="d714a-127">Your browser will prompt you to save the file.</span></span>  <span data-ttu-id="d714a-128">เมื่อบันทึกแล้ว เปิดไฟล์ *.csv* ใน Excel</span><span class="sxs-lookup"><span data-stu-id="d714a-128">Once saved, open the *.csv* file in Excel.</span></span>

    ![สกรีนช็อตของไฟล์.csv ที่แสดงข้อมูลส่งออก](media/power-bi-visualization-export-data/pbi-export-to-excel.png)

## <a name="export-data-from-a-report"></a><span data-ttu-id="d714a-130">ส่งข้อมูลออกจากรายงาน</span><span class="sxs-lookup"><span data-stu-id="d714a-130">Export data from a report</span></span>

<span data-ttu-id="d714a-131">เพื่อดำเนินการตามขั้นตอนนี้ เปิด [รายงานตัวอย่างการวิเคราะห์การจัดซื้อ](../create-reports/sample-procurement.md) ในบริการ Power BI ในมุมมองการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="d714a-131">To follow along, open the [Procurement analysis sample report](../create-reports/sample-procurement.md) in the Power BI service in Editing view.</span></span> <span data-ttu-id="d714a-132">เพิ่มหน้ารายงานเปล่าใหม่</span><span class="sxs-lookup"><span data-stu-id="d714a-132">Add a new blank report page.</span></span> <span data-ttu-id="d714a-133">จากนั้น ดำเนินการตามขั้นตอนต่าง ๆ ด้านล่างนี้เพื่อเพิ่มการรวม ลำดับชั้น และตัวกรองระดับการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="d714a-133">Then follow the steps below to add an aggregation, hierarchy, and a visualization-level filter.</span></span>

### <a name="create-a-stacked-column-chart"></a><span data-ttu-id="d714a-134">สร้างแผนภูมิคอลัมน์แบบเรียงซ้อน</span><span class="sxs-lookup"><span data-stu-id="d714a-134">Create a stacked column chart</span></span>

1. <span data-ttu-id="d714a-135">สร้าง **แผนภูมิคอลัมน์แบบเรียงซ้อน** ใหม่</span><span class="sxs-lookup"><span data-stu-id="d714a-135">Create a new **Stacked column chart**.</span></span>

    ![สกรีนช็อตของเทมเพลตของแผนภูมิคอลัมน์แบบกลุ่ม](media/power-bi-visualization-export-data/power-bi-clustered.png)

1. <span data-ttu-id="d714a-137">จากบานหน้าต่าง **เขตข้อมูล** เลือก **ตำแหน่งที่ตั้ง > เมือง**, **ตำแหน่งที่ตั้ง > ประเทศ/ภูมิภาค** และ **ใบแจ้งหนี้ > เปอร์เซ็นต์ส่วนลด**</span><span class="sxs-lookup"><span data-stu-id="d714a-137">From the **Fields** pane, select **Location > City**, **Location > Country/Region**, and **Invoice > Discount Percent**.</span></span>  <span data-ttu-id="d714a-138">คุณอาจจำเป็นต้องย้าย **เปอร์เซ็นต์ส่วนลด** ลงในแอ่ง **ค่า** ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="d714a-138">You may have to move **Discount Percent** into the **Value** well.</span></span>

    ![สกรีนช็อตเรียกการแสดงภาพถูกสร้างขึ้น ด้วยเมืองและจำนวนเปอร์เซ็นต์ส่วนลดออกมา](media/power-bi-visualization-export-data/power-bi-build.png)

1. <span data-ttu-id="d714a-140">เปลี่ยนการรวมสำหรับ **เปอร์เซ็นต์ส่วนลด** จาก **จำนวน** เป็น **ค่าเฉลี่ย**</span><span class="sxs-lookup"><span data-stu-id="d714a-140">Change the aggregation for **Discount Percent** from **Count** to **Average**.</span></span> <span data-ttu-id="d714a-141">ในแอ่ง **ค่า** เลือกลูกศรทางด้านขวาของ **เปอร์เซ็นต์ส่วนลด** (ที่อาจระบุว่า **จำนวนเปอร์เซ็นต์ส่วนลด**) และเลือก **ค่าเฉลี่ย** ได้</span><span class="sxs-lookup"><span data-stu-id="d714a-141">In the **Value** well, select the arrow to the right of **Discount Percent** (it may say **Count of Discount Percent**), and choose **Average**.</span></span>

    ![สกรีนช็อตของการเรียกรายการที่รวมด้วยตัวเลือกโดยเฉลี่ยออกมา](media/power-bi-visualization-export-data/power-bi-export-data6.png)

1. <span data-ttu-id="d714a-143">เพิ่มตัวกรองที่ **เมือง** จากนั้นเลือกเมืองทั้งหมด และจากนั้น นำ **แอตแลนต้า** ออก</span><span class="sxs-lookup"><span data-stu-id="d714a-143">Add a filter to **City**, select all cities, and then remove **Atlanta**.</span></span>

    ![สกรีนช็อตของการเรียกตัวกรองเมืองที่ล้างข้อมูลเกี่ยวกับแอตแลนต้า GA กล่องกาเครื่องหมายออกแล้ว](media/power-bi-visualization-export-data/power-bi-filter.png)

   
1. <span data-ttu-id="d714a-145">เจาะดูข้อมูลลงหนึ่งระดับในลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="d714a-145">Drill down one level in the hierarchy.</span></span> <span data-ttu-id="d714a-146">เปิดการเจาะข้อมูลและเจาะดูข้อมูลลงในระดับ **เมือง**</span><span class="sxs-lookup"><span data-stu-id="d714a-146">Turn on drilling and drill down to the **City** level.</span></span> 

    ![สกรีนช็อตของวิชวลที่เจาะดูข้อมูลลงในระดับเมือง](media/power-bi-visualization-export-data/power-bi-drill.png)

<span data-ttu-id="d714a-148">ในตอนนี้เราก็พร้อมที่จะลองใช้ทั้งสองตัวเลือกสำหรับการส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d714a-148">Now we're ready to try out both options for exporting data.</span></span>

### <a name="export-_summarized__-data"></a><span data-ttu-id="d714a-149">ส่งออกข้อมูล\**_สรุป_* _</span><span class="sxs-lookup"><span data-stu-id="d714a-149">Export \**_summarized_* _ data</span></span>
<span data-ttu-id="d714a-150">เลือกตัวเลือกสำหรับ_ *ข้อมูลสรุป*\* หากคุณต้องการส่งออกข้อมูลที่คุณต้องการมองเห็นในวิชวลดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="d714a-150">Select the option for _ *Summarized data*\* if you want to export data for what you see in that visual.</span></span>  <span data-ttu-id="d714a-151">การส่งออกประเภทนี้จะแสดงเฉพาะข้อมูลดังกล่าว (คอลัมน์และการวัด) ที่ใช้ในการสร้างวิชวลเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d714a-151">This type of export shows you only the data (columns and measures) that are being used to create the visual.</span></span>  <span data-ttu-id="d714a-152">ถ้าภาพมีการรวม คุณจะส่งออกข้อมูลรวม</span><span class="sxs-lookup"><span data-stu-id="d714a-152">If the visual has an aggregate, you'll export aggregated data.</span></span> <span data-ttu-id="d714a-153">ตัวอย่างเช่น หากคุณมีแผนภูมิแท่งที่แสดงกราฟจำนวนสี่แท่ง คุณจะมีข้อมูล Excel จำนวนสี่แถว</span><span class="sxs-lookup"><span data-stu-id="d714a-153">For example, if you have a bar chart showing four bars, you'll get four rows of Excel data.</span></span> <span data-ttu-id="d714a-154">ข้อมูลสรุปจะปรากฏในบริการ Power BI ในรูปแบบ *.xlsx* และ *.csv* และใน Power BI Desktop ในรูปแบบ .csv</span><span class="sxs-lookup"><span data-stu-id="d714a-154">Summarized data is available in the Power BI service as *.xlsx* and *.csv* and in Power BI Desktop as .csv.</span></span>

1. <span data-ttu-id="d714a-155">เลือกจุดไข่ปลาในมุมบนขวาของการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="d714a-155">Select the ellipsis in the upper-right corner of the visualization.</span></span> <span data-ttu-id="d714a-156">เลือก **ส่งออกข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="d714a-156">Select **Export data**.</span></span>

    ![สกรีนช็อตการเรียกเมนูมุมขวาบนที่มีปุ่มจุดไข่ปลาและการเรียกดูตัวเลือกส่งออกข้อมูลออกมา](media/power-bi-visualization-export-data/power-bi-export-data2.png)

    <span data-ttu-id="d714a-158">ในบริการ Power BI เนื่องจากการแสดงภาพของคุณมีผลรวม (คุณเปลี่ยน **จำนวน** เป็น *ค่าเฉลี่ย*) คุณจะมีตัวเลือกจำนวนสองรายการ:</span><span class="sxs-lookup"><span data-stu-id="d714a-158">In the Power BI service, since your visualization has an aggregate (you changed **Count** to *average*),  you'll have two options:</span></span>

    - <span data-ttu-id="d714a-159">**ข้อมูลสรุป**</span><span class="sxs-lookup"><span data-stu-id="d714a-159">**Summarized data**</span></span>

    - <span data-ttu-id="d714a-160">**ข้อมูลเบื้องต้น**</span><span class="sxs-lookup"><span data-stu-id="d714a-160">**Underlying data**</span></span>

    <span data-ttu-id="d714a-161">สำหรับความช่วยเหลือในการทำความเข้าใจค่ารวม ดู[ค่ารวมใน Power BI](../create-reports/service-aggregates.md)</span><span class="sxs-lookup"><span data-stu-id="d714a-161">For help understanding aggregates, see [Aggregates in Power BI](../create-reports/service-aggregates.md).</span></span>


    > [!NOTE]
    > <span data-ttu-id="d714a-162">ใน Power BI Desktop คุณจะมีเพียงตัวเลือกในการส่งออกข้อมูลสรุปในรูปแบบไฟล์ .csv</span><span class="sxs-lookup"><span data-stu-id="d714a-162">In Power BI Desktop, you'll only have the option to export summarized data as a .csv file.</span></span> 
    
    
1. <span data-ttu-id="d714a-163">จากเมนู **ส่งออกข้อมูล** ให้เลือก **ข้อมูลสรุป** แล้วเลือกไฟล์ *.xlsx* หรือ *.csv* จากนั้นเลือก **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="d714a-163">From **Export data**, select **Summarized data**, either choose *.xlsx* or *.csv*, and then select **Export**.</span></span> <span data-ttu-id="d714a-164">Power BI ส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d714a-164">Power BI exports the data.</span></span>

    ![สกรีนช็อตของสกรีนช็อตการเรียกข้อมูลส่งออกไฟล์ข้อมูลนามสกุล xlsx ที่สรุปแล้วและเรียกดูตัวเลือกการส่งออกให้แสดงออกมา](media/power-bi-visualization-export-data/power-bi-export-data5.png)

1. <span data-ttu-id="d714a-166">เมื่อคุณเลือก **ส่งออก** เบราว์เซอร์ของคุณจะปรากฏให้คุณบันทึกไฟล์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="d714a-166">When you select  **Export**, your browser prompts you to save the file.</span></span> <span data-ttu-id="d714a-167">เมื่อบันทึกแล้ว เปิดไฟล์ดังกล่าวใน Excel</span><span class="sxs-lookup"><span data-stu-id="d714a-167">Once saved, open the file in Excel.</span></span> <span data-ttu-id="d714a-168">ถ้าคุณกำลังใช้แอป Power BI ใน Microsoft Teams คุณอาจไม่ได้รับพร้อมท์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="d714a-168">If you're using the Power BI app in Microsoft Teams, you may not receive the same prompts.</span></span> <span data-ttu-id="d714a-169">ไฟล์ที่ส่งออกของคุณจะถูกบันทึกไว้ในโฟลเดอร์ดาวน์โหลดภายในเครื่องของคุณ</span><span class="sxs-lookup"><span data-stu-id="d714a-169">Your exported file is saved in your local Downloads folder.</span></span> 

    ![สกรีนช็อตของการแสดงผล Excel](media/power-bi-visualization-export-data/power-bi-export-data9.png)

    <span data-ttu-id="d714a-171">ในตัวอย่างนี้ การส่งออก Excel ของเราแสดงผลรวมหนึ่งสำหรับแต่ละเมือง</span><span class="sxs-lookup"><span data-stu-id="d714a-171">In this example, our Excel export shows one total for each city.</span></span> <span data-ttu-id="d714a-172">เนื่องจากเราได้กรองรัฐแอตแลนต้าออกไป รัฐดังกล่าวจะไม่รวมอยู่ในผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="d714a-172">Since we filtered out Atlanta, it isn't included in the results.</span></span> <span data-ttu-id="d714a-173">แถวแรกของสเปรดชีตของคุณจะแสดงตัวกรองที่ Power BI ใช้เมื่อดึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d714a-173">The first row of our spreadsheet shows the filters that Power BI used when extracting the data.</span></span>
    
    - <span data-ttu-id="d714a-174">ข้อมูลทั้งหมดที่ใช้โดยลำดับชั้นจะถูกส่งออกไม่เพียงแค่ข้อมูลที่ใช้สำหรับระดับการเจาะปัจจุบันสำหรับการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="d714a-174">All the data used by the hierarchy is exported, not simply the data used for the current drill level for the visual.</span></span> <span data-ttu-id="d714a-175">ตัวอย่างเช่น เราเจาะดูข้อมูลลึกลงในระดับเมือง แต่การส่งออกของเรารวมถึงข้อมูลประเทศเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="d714a-175">For example, we had drilled down to the city level, but our export includes country data as well.</span></span>  

    - <span data-ttu-id="d714a-176">ข้อมูลที่ส่งออกของเราจะรวมไปด้วย</span><span class="sxs-lookup"><span data-stu-id="d714a-176">Our exported data is aggregated.</span></span> <span data-ttu-id="d714a-177">เราจะมีผลรวมทั้งหมด เป็นหนึ่งแถวสำหรับแต่ละเมือง</span><span class="sxs-lookup"><span data-stu-id="d714a-177">We get a total, one row, for each city.</span></span>

    - <span data-ttu-id="d714a-178">เนื่องจากเราได้ปรับใช้ตัวกรองกับการแสดงภาพ ข้อมูลที่ส่งออกจึงจะส่งออกแบบกรองแล้วด้วย</span><span class="sxs-lookup"><span data-stu-id="d714a-178">Since we applied filters to the visualization, the exported data will export as filtered.</span></span> <span data-ttu-id="d714a-179">โปรดทราบว่าแถวแรกจะแสดง **ตัวกรองที่ปรับใช้: เมืองไม่ใช่แอตแลนตา รัฐจอร์เจีย**</span><span class="sxs-lookup"><span data-stu-id="d714a-179">Notice that the first row displays **Applied filters: City is not Atlanta, GA**.</span></span> 

### <a name="export-_underlying__-data"></a><span data-ttu-id="d714a-180">ส่งออกข้อมูล\**_เบื้องต้น_* _</span><span class="sxs-lookup"><span data-stu-id="d714a-180">Export \**_underlying_* _ data</span></span>

<span data-ttu-id="d714a-181">เลือกตัวเลือกนี้ หากคุณต้องการดูข้อมูลในวิชวล _\*_และ_\*_ ข้อมูลเพิ่มเติมจากชุดข้อมูล (ดูที่แผนภูมิด้านล่างสำหรับรายละเอียด)</span><span class="sxs-lookup"><span data-stu-id="d714a-181">Select this option if you want to see the data in the visual _*_and_*_ additional data from the dataset (see chart below for details).</span></span> <span data-ttu-id="d714a-182">ถ้าภาพของคุณมีการรวมค่า การเลือก_ \*ข้อมูลต้นแบบ\*\*จะลบการรวมค่า</span><span class="sxs-lookup"><span data-stu-id="d714a-182">If your visualization has an aggregate, selecting _ *Underlying data*\* removes the aggregate.</span></span> <span data-ttu-id="d714a-183">ในตัวอย่างนี้ การส่งออก Excel จะแสดงหนึ่งแถวสำหรับทุกหนึ่งแถวของเมืองในชุดข้อมูลของเรา และเปอร์เซ็นต์ส่วนลดสำหรับรายการเดียวนั้น</span><span class="sxs-lookup"><span data-stu-id="d714a-183">In this example, the Excel export shows one row for every single City row in our dataset and the discount percent for that single entry.</span></span> <span data-ttu-id="d714a-184">Power BI ปรับโครงสร้างข้อมูล แต่ไม่คิดผลรวม</span><span class="sxs-lookup"><span data-stu-id="d714a-184">Power BI flattens the data, it doesn't aggregate it.</span></span>  

<span data-ttu-id="d714a-185">เมื่อคุณเลือก **ส่งออก** Power BI จะส่งออกข้อมูลไปยังไฟล์ *.xlsx* และเบราว์เซอร์ของคุณจะปรากฏข้อความให้คุณบันทึกไฟล์</span><span class="sxs-lookup"><span data-stu-id="d714a-185">When you select **Export**, Power BI exports the data to an *.xlsx* file and your browser prompts you to save the file.</span></span> <span data-ttu-id="d714a-186">เมื่อบันทึกแล้ว เปิดไฟล์ดังกล่าวใน Excel</span><span class="sxs-lookup"><span data-stu-id="d714a-186">Once saved, open the file in Excel.</span></span>

1. <span data-ttu-id="d714a-187">เลือกจุดไข่ปลาจากมุมบนขวาของการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="d714a-187">Select the ellipsis from the upper-right corner of the visualization.</span></span> <span data-ttu-id="d714a-188">เลือก **ส่งออกข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="d714a-188">Select **Export data**.</span></span>

    ![สกรีนช็อตการเรียกเมนูมุมขวาบนที่มีปุ่มจุดไข่ปลาและการเรียกดูตัวเลือกส่งออกข้อมูลออกมา](media/power-bi-visualization-export-data/power-bi-export-data2.png)

    <span data-ttu-id="d714a-190">ในบริการ Power BI เนื่องจากการแสดงภาพของคุณมีผลรวม (คุณเปลี่ยน **จำนวน** เป็น **ค่าเฉลี่ย**) คุณจะมีตัวเลือกจำนวนสองรายการ:</span><span class="sxs-lookup"><span data-stu-id="d714a-190">In the Power BI service, since your visualization has an aggregate (you changed **Count** to **average**),  you'll have two options:</span></span>

    - <span data-ttu-id="d714a-191">**ข้อมูลสรุป**</span><span class="sxs-lookup"><span data-stu-id="d714a-191">**Summarized data**</span></span>

    - <span data-ttu-id="d714a-192">**ข้อมูลเบื้องต้น**</span><span class="sxs-lookup"><span data-stu-id="d714a-192">**Underlying data**</span></span>

    <span data-ttu-id="d714a-193">สำหรับความช่วยเหลือในการทำความเข้าใจค่ารวม ดู[ค่ารวมใน Power BI](../create-reports/service-aggregates.md)</span><span class="sxs-lookup"><span data-stu-id="d714a-193">For help understanding aggregates, see [Aggregates in Power BI](../create-reports/service-aggregates.md).</span></span>


    > [!NOTE]
    > <span data-ttu-id="d714a-194">ใน Power BI Desktop คุณจะมีเพียงตัวเลือกในการส่งออกข้อมูลสรุปเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d714a-194">In Power BI Desktop, you'll only have the option to export summarized data.</span></span> 
    
    
1. <span data-ttu-id="d714a-195">จาก **ส่งออกข้อมูล** เลือก **ข้อมูลเบื้องต้น** แล้วเลือก **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="d714a-195">From **Export data**, select **Underlying data**, and then select **Export**.</span></span> <span data-ttu-id="d714a-196">Power BI ส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d714a-196">Power BI exports the data.</span></span>

    ![สกรีนช็อตของสกรีนช็อตข้อมูลส่งออกพร้อมกับรายการข้อมูลเบื้องต้น](media/power-bi-visualization-export-data/power-bi-underlying.png)

1. <span data-ttu-id="d714a-198">เมื่อคุณเลือก **ส่งออก** เบราว์เซอร์ของคุณจะปรากฏให้คุณบันทึกไฟล์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="d714a-198">When you select  **Export**, your browser prompts you to save the file.</span></span> <span data-ttu-id="d714a-199">เมื่อบันทึกแล้ว เปิดไฟล์ดังกล่าวใน Excel</span><span class="sxs-lookup"><span data-stu-id="d714a-199">Once saved, open the file in Excel.</span></span>  <span data-ttu-id="d714a-200">ถ้าคุณกำลังใช้แอป Power BI ใน Microsoft Teams คุณอาจไม่ได้รับพร้อมท์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="d714a-200">If you're using the Power BI app in Microsoft Teams, you may not receive the same prompts.</span></span> <span data-ttu-id="d714a-201">ไฟล์ที่ส่งออกของคุณจะถูกบันทึกไว้ในโฟลเดอร์ดาวน์โหลดภายในเครื่องของคุณ</span><span class="sxs-lookup"><span data-stu-id="d714a-201">Your exported file is saved in your local Downloads folder.</span></span> 

    ![สกรีนช็อตของไฟล์ .xlsx ที่แสดงข้อมูลส่งออก](media/power-bi-visualization-export-data/power-bi-excel.png)
    
    - <span data-ttu-id="d714a-203">สกรีนช็อตนี้แสดงเฉพาะส่วนน้อยของไฟล Excel โดยมีแถวมากกว่า 100,000 แถว</span><span class="sxs-lookup"><span data-stu-id="d714a-203">This screenshot shows you only a small portion of the Excel file; it has more than 100,000 rows.</span></span>  
    
    - <span data-ttu-id="d714a-204">ข้อมูลทั้งหมดที่ใช้โดยลำดับชั้นจะถูกส่งออกไม่เพียงแค่ข้อมูลที่ใช้สำหรับระดับการเจาะปัจจุบันสำหรับการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="d714a-204">All the data used by the hierarchy is exported, not simply the data used for the current drill level for the visual.</span></span> <span data-ttu-id="d714a-205">ตัวอย่างเช่น เราเจาะดูข้อมูลลึกลงในระดับเมือง แต่การส่งออกของเรารวมถึงข้อมูลประเทศเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="d714a-205">For example, we had drilled down to the city level, but our export includes country data as well.</span></span>  

    - <span data-ttu-id="d714a-206">เนื่องจากเราได้ปรับใช้ตัวกรองกับการแสดงภาพ ข้อมูลที่ส่งออกจึงจะส่งออกแบบกรองแล้วด้วย</span><span class="sxs-lookup"><span data-stu-id="d714a-206">Since we applied filters to the visualization, the exported data will export as filtered.</span></span> <span data-ttu-id="d714a-207">โปรดทราบว่าแถวแรกจะแสดง **ตัวกรองที่ปรับใช้: เมืองไม่ใช่แอตแลนตา รัฐจอร์เจีย**</span><span class="sxs-lookup"><span data-stu-id="d714a-207">Notice that the first row displays **Applied filters: City is not Atlanta, GA**.</span></span> 

## <a name="customize-the-export-data-user-experience"></a><span data-ttu-id="d714a-208">กำหนดค่าประสบการณ์ของผู้ใช้ข้อมูลการส่งออก</span><span class="sxs-lookup"><span data-stu-id="d714a-208">Customize the export data user experience</span></span>

<span data-ttu-id="d714a-209">ผู้ใช้ที่ได้รับสิทธิการเข้าถึงรายงานจะ **ได้รับอนุญาตให้เข้าถึงชุดข้อมูลเบื้องต้นทั้งหมด** เว้นแต่ว่า [การรักษาความปลอดภัยระดับแถว (RLS)](../admin/service-admin-rls.md) จำกัดการเข้าถึงของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="d714a-209">Users who are granted access to a report are **granted access to the entire underlying dataset**, unless [row-level security (RLS)](../admin/service-admin-rls.md) limits their access.</span></span> <span data-ttu-id="d714a-210">ผู้สร้างรายงานและผู้ดูแลระบบ Power BI สามารถใช้ความสามารถที่อธิบายไว้ด้านล่างเพื่อปรับแต่งประสบการณ์ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="d714a-210">Report authors and Power BI administrators can use the capabilities described below to customize the user experience.</span></span>

- <span data-ttu-id="d714a-211">ผู้สร้างรายงาน [ตัดสินใจว่า *ตัวเลือกการส่งออก*](#set-the-export-options)ใดที่พร้อมใช้งานสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="d714a-211">Report authors [decide which *export options*](#set-the-export-options) are available to users.</span></span>  

- <span data-ttu-id="d714a-212">ผู้ดูแลระบบ Power BI สามารถปิดการส่งออกข้อมูลทั้งหมดหรือบางส่วนสำหรับองค์กรของตนเองได้</span><span class="sxs-lookup"><span data-stu-id="d714a-212">Power BI administrators can turn off some or all data export options for their organization.</span></span>  

- <span data-ttu-id="d714a-213">เจ้าของชุดข้อมูลสามารถตั้งค่าการรักษาความปลอดภัยระดับแถว (RLS) ได้</span><span class="sxs-lookup"><span data-stu-id="d714a-213">Dataset owners can set row level security (RLS).</span></span> <span data-ttu-id="d714a-214">RLS จะจำกัดการเข้าถึงผู้ใช้แบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="d714a-214">RLS will restrict access to read-only users.</span></span> <span data-ttu-id="d714a-215">ถ้าคุณกำหนดค่าพื้นที่ทำงานแอปและให้สมาชิกมีสิทธิ์ในการแก้ไข จะไม่สามารถใช้บทบาท RLS กับพื้นที่ทำงานแอปนั้นได้</span><span class="sxs-lookup"><span data-stu-id="d714a-215">But if you have configured an app workspace and given members edit permissions, RLS roles will not be applied to them.</span></span> <span data-ttu-id="d714a-216">สำหรับข้อมูลเพิ่มเติม โปรดดู [การรักษาความปลอดภัยระดับแถว](../admin/service-admin-rls.md)</span><span class="sxs-lookup"><span data-stu-id="d714a-216">For more information, see [Row-level security](../admin/service-admin-rls.md).</span></span>

- <span data-ttu-id="d714a-217">ผู้สร้างรายงานสามารถซ่อนคอลัมน์ เพื่อไม่ให้แสดงในรายการ **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="d714a-217">Report authors can hide columns so that they don't show up in the **Fields** list.</span></span> <span data-ttu-id="d714a-218">สำหรับข้อมูลเพิ่มเติม ดู [คุณสมบัติของชุดข้อมูล](../developer/automation/api-dataset-properties.md)</span><span class="sxs-lookup"><span data-stu-id="d714a-218">For more information, see [Dataset properties](../developer/automation/api-dataset-properties.md)</span></span>


<span data-ttu-id="d714a-219">**ประสบการณ์ผู้ใช้ที่กำหนดเองเหล่านี้ไม่จำกัดสิ่งที่ผู้ใช้สามารถเข้าถึงข้อมูลในชุดข้อมูล ใช้ [การรักษาความปลอดภัยระดับแถว (RLS)](../admin/service-admin-rls.md) ในชุดข้อมูลเพื่อให้ข้อมูลประจำตัวของแต่ละบุคคลกำหนดว่าข้อมูลใดที่พวกเขาสามารถเข้าถึงได้**</span><span class="sxs-lookup"><span data-stu-id="d714a-219">**These customized user experience do not restrict what data users can access in the dataset. Use [row-level security (RLS)](../admin/service-admin-rls.md) in the dataset so that each person's credentials determine which data they can access.**</span></span>

## <a name="protect-data-when-it-is-exported-out-of-power-bi"></a><span data-ttu-id="d714a-220">ปกป้องข้อมูลเมื่อมีการส่งออกจาก Power BI</span><span class="sxs-lookup"><span data-stu-id="d714a-220">Protect data when it is exported out of Power BI</span></span>

- <span data-ttu-id="d714a-221">ผู้เขียนรายงานสามารถจัดประเภทและรายงานป้ายชื่อโดยใช้ [ป้ายชื่อระดับความลับของ Microsoft Information Protection](../admin/service-security-data-protection-overview.md)</span><span class="sxs-lookup"><span data-stu-id="d714a-221">Report authors can classify and label reports using Microsoft Information Protection [sensitivity labels](../admin/service-security-data-protection-overview.md).</span></span> <span data-ttu-id="d714a-222">ถ้าป้ายชื่อระดับความลับมีการตั้งค่าการป้องกัน Power BI จะใช้การตั้งค่าการป้องกันเหล่านี้เมื่อส่งออกข้อมูลรายงานไปยัง Excel, PowerPoint หรือไฟล์ PDF</span><span class="sxs-lookup"><span data-stu-id="d714a-222">If the sensitivity label has protection settings, Power BI will apply these protection settings when export report data to Excel, PowerPoint, or PDF files.</span></span> <span data-ttu-id="d714a-223">เฉพาะผู้ใช้ที่ได้รับอนุญาตเท่านั้นที่สามารถเปิดไฟล์ที่มีการป้องกัน</span><span class="sxs-lookup"><span data-stu-id="d714a-223">Only authorized users can open protected files.</span></span>

- <span data-ttu-id="d714a-224">ผู้ดูแลระบบ Power BI และความปลอดภัยสามารถใช้ [Microsoft Cloud App Security](../admin/service-security-data-protection-overview.md) เพื่อตรวจสอบการเข้าถึงและกิจกรรมของผู้ใช้ ดำเนินการวิเคราะห์ความเสี่ยงแบบเรียลไทม์ และตั้งค่าตัวควบคุมเฉพาะป้ายกำกับได้</span><span class="sxs-lookup"><span data-stu-id="d714a-224">Security and Power BI a administrators can use [Microsoft Cloud App Security](../admin/service-security-data-protection-overview.md) to monitor user access and activity, perform real-time risk analysis, and set label-specific controls.</span></span> <span data-ttu-id="d714a-225">ตัวอย่างเช่น องค์กรสามารถใช้ Microsoft Cloud App Security เพื่อกำหนดค่านโยบายที่ป้องกันไม่ให้ผู้ใช้ดาวน์โหลดข้อมูลที่ละเอียดอ่อนจาก Power BI ไปยังอุปกรณ์ที่ไม่มีการจัดการได้</span><span class="sxs-lookup"><span data-stu-id="d714a-225">For example, organizations can use Microsoft Cloud App Security to configure a policy that prevents users from downloading sensitive data from Power BI to unmanaged devices.</span></span>

## <a name="export-underlying-data-details"></a><span data-ttu-id="d714a-226">ส่งออกรายละเอียดข้อมูลต้นแบบ</span><span class="sxs-lookup"><span data-stu-id="d714a-226">Export underlying data details</span></span>

<span data-ttu-id="d714a-227">สิ่งที่คุณเห็นเมื่อคุณเลือก **ข้อมูลต้นแบบ** อาจแตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="d714a-227">What you see when you select **Underlying data** can vary.</span></span> <span data-ttu-id="d714a-228">การทำความเข้าใจรายละเอียดเหล่านี้อาจต้องการความช่วยเหลือจากผู้ดูแลระบบหรือแผนก IT ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d714a-228">Understanding these details may require the help of your admin or IT department.</span></span> 


>



| <span data-ttu-id="d714a-229">การแสดงภาพประกอบด้วย</span><span class="sxs-lookup"><span data-stu-id="d714a-229">Visual contains</span></span> | <span data-ttu-id="d714a-230">สิ่งที่คุณจะเห็นในการส่งออก</span><span class="sxs-lookup"><span data-stu-id="d714a-230">What you'll see in export</span></span>  |
|---------------- | ---------------------------|
| <span data-ttu-id="d714a-231">การรวมค่า</span><span class="sxs-lookup"><span data-stu-id="d714a-231">Aggregates</span></span> | <span data-ttu-id="d714a-232">ข้อมูลการรวม *ครั้งแรก* และที่เปิดเผยจากตารางทั้งหมดสำหรับการรวมค่านั้น</span><span class="sxs-lookup"><span data-stu-id="d714a-232">the *first* aggregate and non-hidden data from the entire table for that aggregate</span></span> |
| <span data-ttu-id="d714a-233">การรวมค่า</span><span class="sxs-lookup"><span data-stu-id="d714a-233">Aggregates</span></span> | <span data-ttu-id="d714a-234">ข้อมูลที่เกี่ยวข้อง - ถ้าภาพใช้ข้อมูลจากตารางข้อมูลอื่นที่ *เกี่ยวข้อง* กับตารางข้อมูลที่ประกอบด้วยการรวมค่า (ตราบใดที่ความสัมพันธนั้นเป็น \*: 1 หรือ 1:1)</span><span class="sxs-lookup"><span data-stu-id="d714a-234">related data - if the visual uses data from other data tables that are  *related* to the data table that contains the aggregate (as long as that relationship is \*:1 or 1:1)</span></span> |
| <span data-ttu-id="d714a-235">หน่วยวัด\*</span><span class="sxs-lookup"><span data-stu-id="d714a-235">Measures\*</span></span> | <span data-ttu-id="d714a-236">หน่วยวัดทั้งหมดในภาพ *และ* หน่วยวัดทั้งหมดจากตารางข้อมูลใดๆที่ประกอบด้วยหน่วยวัดที่ใช้ในภาพ</span><span class="sxs-lookup"><span data-stu-id="d714a-236">all measures in the visual *and* all measures from any data table containing a measure used in the visual</span></span> |
| <span data-ttu-id="d714a-237">หน่วยวัด\*</span><span class="sxs-lookup"><span data-stu-id="d714a-237">Measures\*</span></span> | <span data-ttu-id="d714a-238">ข้อมูลที่เปิดเผยทั้งหมดจากตารางที่ประกอบด้วยหน่วยวัด (ตราบใดที่ความสัมพันธ์นั้นเป็น\*: 1 หรือ 1:1)</span><span class="sxs-lookup"><span data-stu-id="d714a-238">all non-hidden data from tables that contain that measure (as long as that relationship is \*:1 or 1:1)</span></span> |
| <span data-ttu-id="d714a-239">หน่วยวัด\*</span><span class="sxs-lookup"><span data-stu-id="d714a-239">Measures\*</span></span> | <span data-ttu-id="d714a-240">ข้อมูลทั้งหมดจากตารางทั้งหมดที่เกี่ยวข้องกับตารางที่ประกอบด้วยหน่วยวัดผ่านทางสาย \*: 1 จาก 1:1)</span><span class="sxs-lookup"><span data-stu-id="d714a-240">all data from all tables that are related to table(s) containing the measures via a chain of \*:1 of 1:1)</span></span> |
| <span data-ttu-id="d714a-241">หน่วยวัดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d714a-241">Measures only</span></span> | <span data-ttu-id="d714a-242">คอลัมน์ที่เปิดเผยทั้งหมดจากตารางที่เกี่ยวข้องทั้งหมด (เมื่อต้องขยายหน่วยวัด)</span><span class="sxs-lookup"><span data-stu-id="d714a-242">all non-hidden columns from all related tables (to expand the measure)</span></span> |
| <span data-ttu-id="d714a-243">หน่วยวัดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d714a-243">Measures only</span></span> | <span data-ttu-id="d714a-244">ข้อมูลสรุปของแถวที่ซ้ำกันของหน่วยวัดรูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d714a-244">summarized data for any duplicate rows for model measures</span></span> |

<span data-ttu-id="d714a-245">\* ในบริการหรือ Power BI Desktop ในมุมมองการรายงาน *หน่วยวัด* จะแสดงรายการ **เขตข้อมูล** ที่มีไอคอนเครื่องคิดเลข ![ที่แสดงไอคอน](media/power-bi-visualization-export-data/power-bi-calculator-icon.png)</span><span class="sxs-lookup"><span data-stu-id="d714a-245">\* In Power BI Desktop or service, in the reporting view, a *measure* shows in the **Fields** list with a calculator icon ![showing icon](media/power-bi-visualization-export-data/power-bi-calculator-icon.png).</span></span> <span data-ttu-id="d714a-246">หน่วยวัดสามารถสร้างใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="d714a-246">Measures can be created in Power BI Desktop.</span></span>

### <a name="set-the-export-options"></a><span data-ttu-id="d714a-247">ตั้งค่าตัวเลือกการส่งออก</span><span class="sxs-lookup"><span data-stu-id="d714a-247">Set the export options</span></span>

<span data-ttu-id="d714a-248">ตัวออกแบบรายงาน BI power ควบคุมชนิดของตัวเลือกการส่งออกข้อมูลที่ลูกค้าของพวกเขาสามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="d714a-248">Power BI report designers control the types of data export options that are available for their consumers.</span></span> <span data-ttu-id="d714a-249">ตัวเลือกคือ:</span><span class="sxs-lookup"><span data-stu-id="d714a-249">The choices are:</span></span>

- <span data-ttu-id="d714a-250">อนุญาตให้ผู้ใช้ปลายทางส่งออกข้อมูลสรุปจากบริการ Power BI หรือรายงานเซิฟเวอร์ Power BI</span><span class="sxs-lookup"><span data-stu-id="d714a-250">Allow end users to export summarized data from the Power BI service or Power BI Report Server</span></span>

- <span data-ttu-id="d714a-251">อนุญาตให้ผู้ใช้ปลายทางส่งออกข้อมูลสรุปและข้อมูลพื้นฐานจากบริการหรือรายงานเซิฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="d714a-251">Allow end users to export both summarized and underlying data from the service or Report Server</span></span>

- <span data-ttu-id="d714a-252">ไม่อนุญาตให้ผู้ใช้ปลายทางส่งออกข้อมูลใดๆ จากบริการหรือรายงานเซิฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="d714a-252">Don't allow end users to export any data from the service or Report Server</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="d714a-253">เราขอแนะนำให้ผู้ออกแบบรายงานทบทวนรายงานเก่าและตั้งค่าตัวเลือกการส่งออกด้วยตนเองตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="d714a-253">We recommend that report designers revisit old reports and manually reset the export option as needed.</span></span>

<span data-ttu-id="d714a-254">การตั้งค่าตัวเลือกเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="d714a-254">To set these options:</span></span>

1. <span data-ttu-id="d714a-255">เริ่มต้นใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d714a-255">Start in Power BI Desktop.</span></span>

1. <span data-ttu-id="d714a-256">จากมุมบนซ้าย เลือก **แฟ้ม** > **ตัวเลือกและการตั้งค่า** > **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="d714a-256">From the upper left corner, select **File** > **Options and Settings** > **Options**.</span></span>

1. <span data-ttu-id="d714a-257">ภายใต้ **แฟ้มปัจจุบัน** เลือก **ตั้งค่ารายงาน**</span><span class="sxs-lookup"><span data-stu-id="d714a-257">Under **CURRENT FILE**, select **Report settings**.</span></span>

    ![ตั้งค่ารายงานบนเดสก์ท็อป](media/power-bi-visualization-export-data/desktop-report-settings.png)

1. <span data-ttu-id="d714a-259">เลือกรายการจากเมนูส่วนของการ **ส่งออกข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="d714a-259">Make your selection from the **Export data** section.</span></span>

<span data-ttu-id="d714a-260">นอกจากนี้ คุณยังสามารถอัปเดตการตั้งค่านี้ในบริการ Power BI ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="d714a-260">You can also update this setting in the Power BI service.</span></span>

<span data-ttu-id="d714a-261">จำเป็นจะต้องทราบว่าหากการตั้งค่าพอร์ทัลของผู้ดูแลระบบ Power BI ขัดแย้งกับการตั้งค่ารายงานสำหรับส่งออกข้อมูล การตั้งค่าของผู้ดูแลระบบจะแทนที่การตั้งค่าการส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d714a-261">It's important to note that if the Power BI admin portal settings conflict with the report settings for export data, the admin settings will override the export data settings.</span></span>

## <a name="limitations-and-considerations"></a><span data-ttu-id="d714a-262">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="d714a-262">Limitations and considerations</span></span>
<span data-ttu-id="d714a-263">ข้อจำกัดและข้อควรพิจารณาเหล่านี้สามารถนำไปใช้กับ Power BI Desktop และบริการของ Power BI รวมถึง Power BI Pro และ Premium</span><span class="sxs-lookup"><span data-stu-id="d714a-263">These limitations and considerations apply to Power BI Desktop and the Power BI service, including Power BI Pro and Premium.</span></span>

- <span data-ttu-id="d714a-264">หากต้องการส่งออกข้อมูลจากวิชวล คุณจำเป็นต้อง[สร้างสิทธิ์สำหรับชุดข้อมูลพื้นฐาน](../connect-data/service-datasets-build-permissions.md)</span><span class="sxs-lookup"><span data-stu-id="d714a-264">To export the data from a visual, you need to have [Build permission for the underlying dataset](../connect-data/service-datasets-build-permissions.md).</span></span>

-  <span data-ttu-id="d714a-265">จำนวนแถวสูงสุดที่สามารถส่งออกจาก **Power BI Desktop** และ **บริการ Power BI** สามารถส่งออกจาก **รายงานโหมดนำเข้า** ไปยังไฟล์ *.csv* คือ 30,000</span><span class="sxs-lookup"><span data-stu-id="d714a-265">The maximum number of rows that **Power BI Desktop** and **Power BI service** can export from an **import mode report** to a *.csv* file is 30,000.</span></span>

- <span data-ttu-id="d714a-266">จำนวนสูงสุดของแถวที่แอปพลิเคชันสามารถส่งออกจาก **รายงานโหมดนำเข้า** ไปยังไฟล์ *.xlsx* คือ 150,000</span><span class="sxs-lookup"><span data-stu-id="d714a-266">The maximum number of rows that the applications can export from an **import mode report** to an *.xlsx* file is 150,000.</span></span>

- <span data-ttu-id="d714a-267">ส่งออกโดยใช้ *ข้อมูลเบื้องต้น* จะไม่สามารถทำงานถ้าหาก:</span><span class="sxs-lookup"><span data-stu-id="d714a-267">Export using *Underlying data* won't work if:</span></span>

  - <span data-ttu-id="d714a-268">เวอร์ชันเก่ากว่าปี 2016</span><span class="sxs-lookup"><span data-stu-id="d714a-268">the version is older than 2016.</span></span>

  - <span data-ttu-id="d714a-269">ตารางในแบบจำลองไม่มีคีย์เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="d714a-269">the tables in the model don't have a unique key.</span></span>
    
  -  <span data-ttu-id="d714a-270">ผู้ดูแลระบบหรือผู้ออกแบบรายงานได้ปิดใช้งานคุณลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="d714a-270">an administrator or report designer has disabled this feature.</span></span>

- <span data-ttu-id="d714a-271">การส่งออกโดยใช้ *ข้อมูลเบื้องต้น* จะไม่สามารถทำได้ถ้าคุณเปิดตัวเลือก *แสดงรายการที่ไม่มีข้อมูล* สำหรับการแสดงภาพ Power BI ที่ถูกกำลังส่งออก</span><span class="sxs-lookup"><span data-stu-id="d714a-271">Export using *Underlying data* won't work if you enable the *Show items with no data* option for the visualization Power BI is exporting.</span></span>

- <span data-ttu-id="d714a-272">เมื่อใช้ DirectQuery จำนวนข้อมูลที่ Power BI สามารถส่งออกได้สูงสุดคือ ข้อมูลที่ไม่บีบอัด 16 MB</span><span class="sxs-lookup"><span data-stu-id="d714a-272">When using DirectQuery, the maximum amount of data that Power BI can export is 16-MB uncompressed data.</span></span> <span data-ttu-id="d714a-273">ผลลัพธ์ไม่เป็นไปตามที่คาดหวังอาจเป็นเพราะคุณส่งออกข้อมูลน้อยกว่าจำนวนแถวสูงสุด 150,000 แถว</span><span class="sxs-lookup"><span data-stu-id="d714a-273">An unintended result may be that you export less than the maximum number of rows of 150,000.</span></span> <span data-ttu-id="d714a-274">ซึ่งเป็นไปได้ที่จะเป็นเช่นนั้นหาก:</span><span class="sxs-lookup"><span data-stu-id="d714a-274">This is likely if:</span></span>

    - <span data-ttu-id="d714a-275">มีจำนวนคอลัมน์มากเกินไป</span><span class="sxs-lookup"><span data-stu-id="d714a-275">There are too many columns.</span></span> <span data-ttu-id="d714a-276">ลองลดจำนวนคอลัมน์ลงและส่งออกอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="d714a-276">Try reducing the number of columns and exporting again.</span></span>

    - <span data-ttu-id="d714a-277">มีข้อมูลที่ยากต่อการบีบอัด</span><span class="sxs-lookup"><span data-stu-id="d714a-277">There's data that is difficult to compress.</span></span>

    - <span data-ttu-id="d714a-278">ปัจจัยอื่น ๆ ก็มีส่วนในการเพิ่มขนาดไฟล์และลดจำนวนแถวที่ Power BI สามารถส่งออก ได้</span><span class="sxs-lookup"><span data-stu-id="d714a-278">Other factors are at play that increase file size and decrease the number of rows Power BI can export.</span></span>

- <span data-ttu-id="d714a-279">ถ้าการแสดงภาพใช้ข้อมูลจากตารางข้อมูลมากกว่าหนึ่งตาราง และไม่มีความสัมพันธ์ระหว่างตารางเหล่านั้นในรูปแบบข้อมูล Power BI จะทำได้เพียงส่งออกข้อมูลสำหรับตารางแรก</span><span class="sxs-lookup"><span data-stu-id="d714a-279">If the visualization uses data from more than one data table, and no relationship exists for those tables in the data model, Power BI only exports data for the first table.</span></span>

- <span data-ttu-id="d714a-280">ยังไม่สนับสนุนวิชวล Power BI และวิชวล R ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="d714a-280">Power BI visuals and R visuals aren't currently supported.</span></span>

- <span data-ttu-id="d714a-281">ใน Power BI คุณสามารถตั้งชื่อใหม่ให้กับเขตข้อมูล (คอลัมน์) โดยการดับเบิลคลิกที่เขตข้อมูล แล้วพิมพ์ชื่อใหม่</span><span class="sxs-lookup"><span data-stu-id="d714a-281">In Power BI, you can rename a field (column) by double-clicking the field and typing a new name.</span></span> <span data-ttu-id="d714a-282">Power BI จะอ้างอิงข้อมูลชื่อใหม่เป็นในฐานะ *นามแฝง*</span><span class="sxs-lookup"><span data-stu-id="d714a-282">Power BI refers to the new name as an *alias*.</span></span> <span data-ttu-id="d714a-283">อาจเป็นไปได้ว่า รายงาน Power BI สุดท้ายแล้วมีชื่อเขตข้อมูลที่ซ้ำกัน แต่ Excel ไม่อนุญาตให้มีชื่อที่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="d714a-283">It's possible that a Power BI report can end up with duplicate field names, but Excel doesn't allow duplicates.</span></span> <span data-ttu-id="d714a-284">ดังนั้น เมื่อPower BI ส่งออกข้อมูลไปยัง Excel นามแฝงของเขตข้อมูลถูกแปลงกลับไปเป็นชื่อเขตข้อมูล (คอลัมน์) เดิม</span><span class="sxs-lookup"><span data-stu-id="d714a-284">So when Power BI exports the data to Excel, the field aliases revert to their original field (column) names.</span></span>  

- <span data-ttu-id="d714a-285">ถ้ามีอักขระ Unicode ในไฟล์ *.csv* ข้อความใน Excel อาจไม่แสดงอย่างเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="d714a-285">If there are Unicode characters in the *.csv* file, the text in Excel may not display properly.</span></span> <span data-ttu-id="d714a-286">ตัวอย่างของอักขระ Unicode คือสัญลักษณ์สกุลเงินและคำในภาษาต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="d714a-286">Examples of Unicode characters are currency symbols and foreign words.</span></span> <span data-ttu-id="d714a-287">คุณสามารถเปิดไฟล์ใน Notepad และ Unicode ซึ่งจะแสดงผลอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="d714a-287">You can open the file in Notepad and the Unicode will display correctly.</span></span> <span data-ttu-id="d714a-288">การแก้ไขปัญหาชั่วคราวคือการ นำเข้าไฟล์ *.csv* ถ้าคุณต้องการเปิดไฟล์ใน Excel</span><span class="sxs-lookup"><span data-stu-id="d714a-288">If you want to open the file in Excel, the workaround is to import the *.csv*.</span></span> <span data-ttu-id="d714a-289">การนำเข้าไฟล์ลงใน Excel:</span><span class="sxs-lookup"><span data-stu-id="d714a-289">To import the file into Excel:</span></span>

  1. <span data-ttu-id="d714a-290">เปิด Excel</span><span class="sxs-lookup"><span data-stu-id="d714a-290">Open Excel.</span></span>

  1. <span data-ttu-id="d714a-291">ไปที่แท็บ **ข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="d714a-291">Go to the **Data** tab.</span></span>
  
  1. <span data-ttu-id="d714a-292">เลือก **รับข้อมูลภายนอก** > **จากข้อความ**</span><span class="sxs-lookup"><span data-stu-id="d714a-292">Select **Get external data** > **From text**.</span></span>
  
  1. <span data-ttu-id="d714a-293">ไปยังโฟลเดอร์เฉพาะที่จัดเก็บไฟล์และเลือกไฟล์ *.csv*</span><span class="sxs-lookup"><span data-stu-id="d714a-293">Go to the local folder where the file is stored and select the *.csv*.</span></span>

- <span data-ttu-id="d714a-294">เมื่อทำการส่งออกไปเป็นไฟล์ *csv* แล้ว อักขระบางตัวจะเลื่อนออกไปโดยมีเครื่องหมาย **'** นำหน้า เพื่อใช้ป้องกันการทำงานของสคริปต์เมื่อเปิดไฟล์ใน Excel</span><span class="sxs-lookup"><span data-stu-id="d714a-294">When exporting to *.csv*, certain characters will be escaped with a leading **'** to prevent script execution when opened in Excel.</span></span> <span data-ttu-id="d714a-295">ซึ่งจะเกิดขึ้นเมื่อ:</span><span class="sxs-lookup"><span data-stu-id="d714a-295">This happens when:</span></span>
  - <span data-ttu-id="d714a-296">คุณกำหนดคอลัมน์ไว้เป็นชนิด "Text" (ข้อความ) ในแบบจำลองข้อมูล **_และ_**</span><span class="sxs-lookup"><span data-stu-id="d714a-296">The column is defined as type "text" in the data model, **_and_**</span></span>
  - <span data-ttu-id="d714a-297">อักขระตัวแรกของข้อความมีอักขระต่อไปนี้: **=, @, +,-**</span><span class="sxs-lookup"><span data-stu-id="d714a-297">The first character of the text is one of the following: **=, @, +, -**</span></span>

- <span data-ttu-id="d714a-298">ผู้ดูแลระบบ Power BI สามารถปิดการส่งออกข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="d714a-298">Power BI admins can disable the export of data.</span></span>

<span data-ttu-id="d714a-299">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d714a-299">More questions?</span></span> [<span data-ttu-id="d714a-300">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="d714a-300">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)