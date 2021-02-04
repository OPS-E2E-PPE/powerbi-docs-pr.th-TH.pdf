---
title: 'ตัวอย่างการวิเคราะห์คุณภาพผู้จัดหาสินค้าสำหรับ Power BI: ชมการแนะนำ'
description: 'ตัวอย่างการวิเคราะห์คุณภาพผู้จัดหาสินค้าสำหรับ Power BI: ชมการแนะนำ'
author: maggiesMSFT
ms.author: maggies
ms.reviewer: amac
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: conceptual
ms.date: 07/19/2019
LocalizationGroup: Samples
ms.openlocfilehash: 4b4cfa78a01ec628f5d396ea6a267abe7598998c
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96417623"
---
# <a name="supplier-quality-analysis-sample-for-power-bi-take-a-tour"></a><span data-ttu-id="36b45-103">ตัวอย่างการวิเคราะห์คุณภาพผู้จัดหาสินค้าสำหรับ Power BI: ชมการแนะนำ</span><span class="sxs-lookup"><span data-stu-id="36b45-103">Supplier Quality Analysis sample for Power BI: Take a tour</span></span>

<span data-ttu-id="36b45-104">แดชบอร์ดตัวอย่างสำหรับอุตสาหกรรมนี้และรายงานเบื้องต้นเน้นไปที่หนึ่งในความท้าทายของห่วงโซ่อุปทานทั่วไป: การวิเคราะห์คุณภาพผู้จัดหาสินค้า</span><span class="sxs-lookup"><span data-stu-id="36b45-104">This industry sample dashboard and underlying report focus on one of the typical supply chain challenges: supplier quality analysis.</span></span> <span data-ttu-id="36b45-105">การวิเคราะห์นี้ใช้เมตริกหลักสองอย่าง: ผลรวมจำนวนที่บกพร่องและผลรวมเวลาที่ไม่ได้ทำงานที่เกิดขึ้นจากข้อบกพร่องเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="36b45-105">Two primary metrics are at play in this analysis: total number of defects and the total downtime that these defects caused.</span></span> 

<span data-ttu-id="36b45-106">ตัวอย่างนี้มีสองวัตถุประสงค์หลัก:</span><span class="sxs-lookup"><span data-stu-id="36b45-106">This sample has two main objectives:</span></span>

* <span data-ttu-id="36b45-107">ทำความเข้าใจว่า ใครเป็นผู้จัดหาสินค้าที่มีคุณภาพดีที่สุดและแย่ที่สุด</span><span class="sxs-lookup"><span data-stu-id="36b45-107">Understand who the best and worst suppliers are, with respect to quality.</span></span>
* <span data-ttu-id="36b45-108">ระบุโรงงานไหนสามารถค้นพบและปฏิเสธวัสดุที่มีข้อบกพร่องได้ดีกว่า เพื่อลดเวลาที่ต้องหยุดทำงาน</span><span class="sxs-lookup"><span data-stu-id="36b45-108">Identify which plants do a better job finding and rejecting defects, to minimize downtime.</span></span>

![แดชบอร์ดสำหรับ ตัวอย่างการวิเคราะห์คุคุณภาพผู้จัดหาสินค้า](media/sample-supplier-quality/supplier1.png)

<span data-ttu-id="36b45-110">ตัวอย่างนี้เป็นส่วนหนึ่งของชุดตัวอย่าง ที่แสดงให้เห็นวิธีการที่คุณสามารถใช้ Power BI กับข้อมูล รายงาน และแดชบอร์ดที่เกี่ยวข้องกับธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="36b45-110">This sample is part of a series that shows how you can use Power BI with business-oriented data, reports, and dashboards.</span></span> <span data-ttu-id="36b45-111">ซึ่งสร้างขึ้นโดย [obviEnce](http://www.obvience.com/) ด้วยข้อมูลจริงที่ไม่มีการระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="36b45-111">It was created by [obviEnce](http://www.obvience.com/) with real data, which has been anonymized.</span></span> <span data-ttu-id="36b45-112">ข้อมูลมีให้ใช้งานหลายรูปแบบ: ชุดเนื้อหา ไฟล์ Power BI Desktop .pbix หรือเวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="36b45-112">The data is available in several formats: content pack, .pbix Power BI Desktop file, or Excel workbook.</span></span> <span data-ttu-id="36b45-113">ดู [ตัวอย่างสำหรับ Power BI](sample-datasets.md)</span><span class="sxs-lookup"><span data-stu-id="36b45-113">See [Samples for Power BI](sample-datasets.md).</span></span> 

<span data-ttu-id="36b45-114">บทช่วยสอนนี้จะสำรวจชุดเนื้อหาของตัวอย่างการวิเคราะห์คุณภาพผู้จัดหาสินค้าในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="36b45-114">This tutorial explores the Supplier Quality Analysis sample content pack in the Power BI service.</span></span> <span data-ttu-id="36b45-115">เนื่องจากประสบการณ์การใช้รายงานจะคล้ายคลึงกันใน Power BI Desktop ดังนั้นคุณสามารถใช้ Power BI Desktop กับไฟล์ .pbix ตัวอย่างใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="36b45-115">Because the report experience is similar in Power BI Desktop and in the service, you can also follow along by using the sample .pbix file in Power BI Desktop.</span></span> 

<span data-ttu-id="36b45-116">คุณไม่จำเป็นต้องมีสิทธิการใช้งาน Power BI ในการสำรวจตัวอย่างใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="36b45-116">You don't need a Power BI license to explore the samples in Power BI Desktop.</span></span> <span data-ttu-id="36b45-117">ถ้าคุณไม่มีสิทธิการใช้งาน Power BI Pro คุณสามารถบันทึกตัวอย่างไปยังพื้นที่ทำงานของฉันในบริการของ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="36b45-117">If you don't have a Power BI Pro license, you can save the sample to your My Workspace in the Power BI service.</span></span> 

## <a name="get-the-sample"></a><span data-ttu-id="36b45-118">รับตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="36b45-118">Get the sample</span></span>

<span data-ttu-id="36b45-119">ก่อนที่คุณสามารถใช้ตัวอย่าง คุณต้องดาวน์โหลดในรูปแบบ[ชุดเนื้อหา](#get-the-content-pack-for-this-sample)[ไฟล์ .pbix](#get-the-pbix-file-for-this-sample) หรือ[เวิร์กบุ๊ก Excel](#get-the-excel-workbook-for-this-sample)</span><span class="sxs-lookup"><span data-stu-id="36b45-119">Before you can use the sample, you must first download it as a [content pack](#get-the-content-pack-for-this-sample), [.pbix file](#get-the-pbix-file-for-this-sample), or [Excel workbook](#get-the-excel-workbook-for-this-sample).</span></span>

### <a name="get-the-content-pack-for-this-sample"></a><span data-ttu-id="36b45-120">รับชุดเนื้อหาสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="36b45-120">Get the content pack for this sample</span></span>

1. <span data-ttu-id="36b45-121">เปิดบริการ Power BI (app.powerbi.com) ลงชื่อเข้าใช้ และเปิดพื้นที่ทำงานที่คุณต้องการบันทึกตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="36b45-121">Open the Power BI service (app.powerbi.com), sign in, and open the workspace where you want to save the sample.</span></span>

   <span data-ttu-id="36b45-122">ถ้าคุณไม่มีสิทธิการใช้งาน Power BI Pro คุณสามารถบันทึกตัวอย่างไปยังพื้นที่ทำงานของฉัน</span><span class="sxs-lookup"><span data-stu-id="36b45-122">If you don't have a Power BI Pro license, you can save the sample to your My Workspace.</span></span>

2. <span data-ttu-id="36b45-123">ที่มุมด้านล่างซ้าย เลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="36b45-123">In the bottom-left corner, select **Get Data**.</span></span>
   
   ![เลือกรับข้อมูล](media/sample-datasets/power-bi-get-data.png)
3. <span data-ttu-id="36b45-125">บนหน้า **รับข้อมูล** ที่ปรากฏขึ้น เลือก **ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="36b45-125">On the **Get Data** page that appears, select **Samples**.</span></span>
   
4. <span data-ttu-id="36b45-126">เลือก **ตัวอย่างการวิเคราะห์คุณภาพผู้จัดหาสินค้า** แล้วเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="36b45-126">Select **Supplier Quality Analysis Sample**, then choose **Connect**.</span></span>  
   
   ![เชื่อมต่อกับตัวอย่าง](media/sample-supplier-quality/supplier16.png)

5. <span data-ttu-id="36b45-128">Power BI นำเข้าชุดเนื้อหา จากนั้นเพิ่มแดชบอร์ด รายงาน และชุดข้อมูลใหม่ไปยังพื้นที่ทำงานปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="36b45-128">Power BI imports the content pack and then adds a new dashboard, report, and dataset to your current workspace.</span></span>
   
   ![รายการตัวอย่างการวิเคราะห์คุณภาพผู้จัดหา](media/sample-supplier-quality/supplier17.png)
  
### <a name="get-the-pbix-file-for-this-sample"></a><span data-ttu-id="36b45-130">รับไฟล์ .pbix สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="36b45-130">Get the .pbix file for this sample</span></span>

<span data-ttu-id="36b45-131">อีกทางเลือกหนึ่งคือ คุณสามารถดาวน์โหลดตัวอย่างการวิเคราะห์คุณภาพผู้จัดหาสินค้าเป็น [ไฟล์ .pbix](https://download.microsoft.com/download/8/C/6/8C661638-C102-4C04-992E-9EA56A5D319B/Supplier-Quality-Analysis-Sample-PBIX.pbix) ซึ่งถูกออกแบบมาสำหรับใช้กับ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="36b45-131">Alternatively, you can download the Supplier Quality Analysis sample as a [.pbix file](https://download.microsoft.com/download/8/C/6/8C661638-C102-4C04-992E-9EA56A5D319B/Supplier-Quality-Analysis-Sample-PBIX.pbix), which is designed for use with Power BI Desktop.</span></span>

### <a name="get-the-excel-workbook-for-this-sample"></a><span data-ttu-id="36b45-132">รับเวิร์กบุ๊ก Excel สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="36b45-132">Get the Excel workbook for this sample</span></span>

<span data-ttu-id="36b45-133">ถ้าคุณต้องการดูแหล่งข้อมูลสำหรับตัวอย่างนี้ ตัวอย่างนี้ยังมีให้ในรูปแบบ[เวิร์กบุ๊ก Excel](https://go.microsoft.com/fwlink/?LinkId=529779)</span><span class="sxs-lookup"><span data-stu-id="36b45-133">If you want to view the data source for this sample, it's also available as an [Excel workbook](https://go.microsoft.com/fwlink/?LinkId=529779).</span></span> <span data-ttu-id="36b45-134">เวิร์กบุ๊กประกอบด้วยแผ่นงาน Power View ที่คุณสามารถดู และปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="36b45-134">The workbook contains Power View sheets that you can view and modify.</span></span> <span data-ttu-id="36b45-135">หากต้องการดูข้อมูลดิบ ให้เปิดใช้งาน add-in การวิเคราะห์ข้อมูล แล้วจากนั้นเลือก **Power Pivot > จัดการ**</span><span class="sxs-lookup"><span data-stu-id="36b45-135">To see the raw data, enable the Data Analysis add-ins, and then select **Power Pivot > Manage**.</span></span> <span data-ttu-id="36b45-136">หากต้องการเปิดใช้งาน Power View และ Power Pivot add-in โปรดดู [สำรวจตัวอย่าง Excel ใน Excel ](sample-datasets.md#explore-excel-samples-inside-excel)สำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="36b45-136">To enable the Power View and Power Pivot add-ins, see [Explore the Excel samples in Excel](sample-datasets.md#explore-excel-samples-inside-excel) for details.</span></span>

## <a name="downtime-caused-by-defective-materials"></a><span data-ttu-id="36b45-137">เวลาหยุดทำงานที่เกิดจากวัสดุที่มีข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="36b45-137">Downtime caused by defective materials</span></span>
<span data-ttu-id="36b45-138">เรามาวิเคราะห์เวลาหยุดทำงานที่เกิดจากวัสดุที่มีข้อบกพร่อง และดูว่าผู้จัดหาสินค้ารายไหนที่เป็นผู้รับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="36b45-138">Let's analyze the downtime caused by defective materials and see which vendors are responsible.</span></span>  

1. <span data-ttu-id="36b45-139">บนแดชบอร์ด เลือก **จำนวนข้อบกพร่องรวม** หรือไทล์ **เวลาหยุดทำงานรวม เป็นนาที**</span><span class="sxs-lookup"><span data-stu-id="36b45-139">On the dashboard, select the **Total Defect Quantity** or the **Total Downtime Minutes** tile.</span></span>

   ![เลือกไทล์เพื่อเปิดรายงาน](media/sample-supplier-quality/supplier2.png)  

   <span data-ttu-id="36b45-141">รายงานตัวอย่างการวิเคราะห์คุณภาพผู้จัดหาสินค้าจะเปิดไปยังหน้า **วิเคราะห์เวลาหยุดทำงาน**</span><span class="sxs-lookup"><span data-stu-id="36b45-141">The Supplier Quality Analysis Sample report opens to the **Downtime Analysis** page.</span></span>

   <span data-ttu-id="36b45-142">โปรดสังเกตว่าเรามีชิ้นส่วนที่บกพร่อง 33 ล้านชิ้น ทำให้เวลาในการหยุดทำงานทั้งหมดเท่ากับ 77,000 นาที</span><span class="sxs-lookup"><span data-stu-id="36b45-142">Notice we have 33 million defective pieces, causing a total downtime of 77,000 minutes.</span></span> <span data-ttu-id="36b45-143">แม้ว่าวัสดุบางชนิดจะมีชิ้นส่วนที่บกพร่องน้อยลง แต่ก็อาจทำให้เกิดความล่าช้า ซึ่งส่งผลให้มีปัญหาในการหยุดทำงานมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="36b45-143">Although some materials have fewer defective pieces, they can cause delays, which result in more downtime.</span></span> <span data-ttu-id="36b45-144">เรามาสำรวจวัสดุเหล่านี้บนหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="36b45-144">Let's explore them on the report page.</span></span>  
2. <span data-ttu-id="36b45-145">หากเราดูที่เส้น **เวลาหยุดทำงานรวม เป็นนาที** ในแผนภูมิผสม **ข้อบกพร่องและเวลาหยุดทำงาน (นาที) ตามชนิดของวัสดุ** เราจะเห็นว่าวัสดุที่เป็นลอนก่อให้เกิดการหยุดทำงานสูงที่สุด</span><span class="sxs-lookup"><span data-stu-id="36b45-145">If we look at the **Total Downtime Minutes** line in the **Defects and Downtime (min) by Material Type** combo chart, we can see that corrugate materials cause the most downtime.</span></span>  
3. <span data-ttu-id="36b45-146">เลือกคอลัมน์ **เป็นลอน** เพื่อดูว่าโรงงานไหนได้รับผลกระทบมากที่สุดจากข้อบกพร่องนี้ และผู้จัดหาสินค้ารายไหนที่เป็นผู้ที่รับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="36b45-146">Select the **Corrugate** column to see which plants are affected most by this defect and which vendor is responsible.</span></span>  

   ![เลือกคอลัมน์เป็นลอน](media/sample-supplier-quality/supplier3.png)  
4. <span data-ttu-id="36b45-148">ในแผนที่ **การหยุดทำงาน (นาที) ตามโรงงาน** ให้เลือกโรงงานแต่ละแห่งเพื่อดูว่าผู้จัดหาสินค้าหรือวัสดุไหนที่รับผิดชอบต่อการหยุดทำงานในโรงงานนั้น</span><span class="sxs-lookup"><span data-stu-id="36b45-148">In the **Downtime (min) by Plant** map, select individual plants in turn to see which vendor or material is responsible for the downtime at that plant.</span></span>

### <a name="which-are-the-worst-suppliers"></a><span data-ttu-id="36b45-149">ผู้จัดหาสินค้ารายไหนเป็นผู้จัดหาที่แย่ที่สุด</span><span class="sxs-lookup"><span data-stu-id="36b45-149">Which are the worst suppliers?</span></span>
 <span data-ttu-id="36b45-150">เราต้องการค้นหาผู้จัดหาสินค้าแปดรายที่แย่ที่สุด และหาว่า มีกี่เปอร์เซ็นต์ของเวลาหยุดทำงานทั้งหมดที่ของพวกเขาเป็นผู้รับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="36b45-150">We want to find the worst eight suppliers and determine what percentage of the downtime they're responsible for creating.</span></span> <span data-ttu-id="36b45-151">เราสามารถทำได้โดยการเปลี่ยนแผนภูมิพื้นที่ **เวลาหยุดทำงาน (นาที) ตามผู้จัดหาสินค้า** ให้เป็นแผนที่ต้นไม้</span><span class="sxs-lookup"><span data-stu-id="36b45-151">We can do so by changing the **Downtime (min) by Vendor** area chart to a treemap.</span></span>  

1. <span data-ttu-id="36b45-152">ในหน้า **การวิเคราะห์การหยุดทำงาน** ของรายงาน ให้เลือก **แก้ไขรายงาน** ในมุมบนซ้าย</span><span class="sxs-lookup"><span data-stu-id="36b45-152">On the **Downtime Analysis** page of the report, select **Edit report** in the upper-left corner.</span></span>  
2. <span data-ttu-id="36b45-153">เลือกแผนภูมิพื้นที่ **เวลาหยุดทำงาน (นาที) ตามผู้จัดหาสินค้า** และในบานหน้าต่างการ **แสดงภาพข้อมูล** เลือกไอคอน **แผนที่ต้นไม้**</span><span class="sxs-lookup"><span data-stu-id="36b45-153">Select the **Downtime (min) by Vendor** area chart, and in the **Visualizations** pane, select the **Treemap** icon.</span></span>  

   ![เลือกไอคอนแผนที่ต้นไม้](media/sample-supplier-quality/supplier4.png)  

    <span data-ttu-id="36b45-155">แผนที่ต้นไม้จะกำหนดเขตข้อมูล **ผู้จัดหาสินค้า** สำหรับ **จัดกลุ่ม** ให้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="36b45-155">The treemap automatically sets the **Vendor** field as the **Group**.</span></span>  

    ![เวลาที่ไม่ได้ทำงาน (ต่ำสุด) ตามแผนที่ต้นไม้ของผู้จำหน่าย](media/sample-supplier-quality/supplier5.png)  

   <span data-ttu-id="36b45-157">จากแผนที่ต้นไม้นี้ เราสามารถเห็นผู้จัดหาที่แย่ที่สุดแปดราย เป็นรูปสี่เหลี่ยมแปดรูป บนด้านซ้ายของแผนที่ต้นไม้</span><span class="sxs-lookup"><span data-stu-id="36b45-157">From this treemap, we can see the top eight vendors are the eight blocks on the left of the treemap.</span></span> <span data-ttu-id="36b45-158">นอกจากนี้เรายังสามารถเห็นว่า พวกเขาทำให้เกิดการหยุดทำงานประมาณ 50% ของจำนวนนาทีทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="36b45-158">We can also see they account for about 50% of all downtime minutes.</span></span>  
3. <span data-ttu-id="36b45-159">เลือก **ตัวอย่างการวิเคราะห์คุณภาพผู้จัดหาสินค้า** ในบานหน้าต่างนำทางด้านบนเพื่อย้อนกลับไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="36b45-159">Select **Supplier Quality Analysis Sample** in the top nav pane to return to the dashboard.</span></span>

### <a name="comparing-plants"></a><span data-ttu-id="36b45-160">เปรียบเทียบโรงงานต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="36b45-160">Comparing plants</span></span>
<span data-ttu-id="36b45-161">ในตอนนี้เรามาสำรวจกันว่า โรงงานไหนสามารถจัดการกับวัสดุที่มีข้อบกพร่องได้ดีกว่า และส่งผลให้เกิดการหยุดทำงานน้อยกว่า</span><span class="sxs-lookup"><span data-stu-id="36b45-161">Now let's explore which plant does a better job managing defective material, resulting in less downtime.</span></span>  

1. <span data-ttu-id="36b45-162">บนแดชบอร์ด เลือกไทล์แผนที่ **รายงานข้อบกพร่องรวมโดยแยกตามโรงงาน, ชนิดข้อบกพร่อง**</span><span class="sxs-lookup"><span data-stu-id="36b45-162">On the dashboard, select the **Total Defect Reports by Plant, Defect Type** map tile.</span></span>      

   ![ผลรวมรายงานสินค้าบกพร่องตามโรงงานและไทล์ชนิดข้อบกพร่อง](media/sample-supplier-quality/supplier6.png)  

   <span data-ttu-id="36b45-164">รายงานจะเปิดขึ้นไปยังหน้า **การวิเคราะห์คุณภาพผู้จัดหาสินค้า**</span><span class="sxs-lookup"><span data-stu-id="36b45-164">The report opens to the **Supplier Quality Analysis** page.</span></span>  

2. <span data-ttu-id="36b45-165">ในคำอธิบายของ **รายงานข้อบกพร่องรวมโดยแยกตามโรงงานและชนิดข้อบกพร่อง** ให้เลือกวงกลม **ผลกระทบ**</span><span class="sxs-lookup"><span data-stu-id="36b45-165">In the legend of the **Total Defect Reports by Plant and Defect Type**, select the **Impact** circle.</span></span>  

    ![เลือกผลกระทบ](media/sample-supplier-quality/supplier7.png)  

    <span data-ttu-id="36b45-167">โปรดสังเกตว่าในแผนภูมิแบบฟองที่ซึ่ง **โลจิสติกส์** เป็นประเภทที่ยุ่งยากที่สุด</span><span class="sxs-lookup"><span data-stu-id="36b45-167">Notice in the bubble chart that **Logistics** is the most troublesome category.</span></span> <span data-ttu-id="36b45-168">โดยมีจำนวนมากที่สุดในแง่ของปริมาณข้อบกพร่องทั้งหมด รายงานข้อบกพร่อง และนาทีการหยุดทำงาน
</span><span class="sxs-lookup"><span data-stu-id="36b45-168">It's the largest in terms of total defect quantity, defect reports, and downtime minutes.</span></span> <span data-ttu-id="36b45-169">เรามาสำรวจประเภทนี้เพิ่มเติมกัน</span><span class="sxs-lookup"><span data-stu-id="36b45-169">Let's explore this category more.</span></span>  
3. <span data-ttu-id="36b45-170">เลือกฟอง **ลอจิสติกส์** ในแผนภูมิฟอง และสังเกตโรงงานในเมืองสปริงฟิลด์ รัฐอิลลินอยส์ และเนเปอร์วิลล์ รัฐอิลลินอยส์</span><span class="sxs-lookup"><span data-stu-id="36b45-170">Select the **Logistics** bubble in the bubble chart and observe the plants in Springfield and Naperville, IL.</span></span> <span data-ttu-id="36b45-171">ดูเหมือนว่าเนเปอร์วิลล์จะจัดการกับข้อบกพร่องได้ดีกว่า เนื่องจากมีจำนวนที่ถูกปฏิเสธมากและผลกระทบน้อย เมื่อเทียบกับผลกระทบจำนวนมากของสปริงฟิลด์</span><span class="sxs-lookup"><span data-stu-id="36b45-171">Naperville seems to be doing a much better job of managing defective supplies as it has a high number of rejects and few impacts, compared to Springfield's large number for impacts.</span></span>  

   ![เลือกโลจิสติกส์](media/sample-supplier-quality/supplier8.png)  
4. <span data-ttu-id="36b45-173">เลือก **ตัวอย่างการวิเคราะห์คุณภาพผู้จัดหาสินค้า** ในบานหน้าต่างนำทางด้านบนเพื่อย้อนกลับไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="36b45-173">Select **Supplier Quality Analysis Sample** in the top nav pane to return to the dashboard.</span></span>

## <a name="which-material-type-is-best-managed"></a><span data-ttu-id="36b45-174">วัสดุชนิดไหนที่จัดการได้ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="36b45-174">Which material type is best managed?</span></span>
<span data-ttu-id="36b45-175">วัสดุที่ได้รับการจัดการดีที่สุด คือวัสดุที่มีเวลาหยุดทำงานต่ำที่สุดหรือไม่มีเลย โดยไม่ขึ้นกับปริมาณวัสดุที่มีข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="36b45-175">The best managed material type is the one with lowest downtime or no impact, regardless of defect quantity.</span></span>

1. <span data-ttu-id="36b45-176">ในแดชบอร์ด ลองดูที่ไทล์ **จำนวนข้อบกพร่องรวม ตามชนิดของวัสดุ, ชนิดของข้อบกพร่อง**</span><span class="sxs-lookup"><span data-stu-id="36b45-176">In the dashboard, look at the **Total Defect Quantity by Material Type, Defect Type** tile.</span></span>

   ![จำนวนข้อบกพร่องรวม ตามชนิดของวัสดุ, ชนิดของข้อบกพร่อง](media/sample-supplier-quality/supplier9.png)

   <span data-ttu-id="36b45-178">โปรดสังเกตว่าแม้ว่า **วัตถุดิบ** ประเภทวัสดุมีข้อบกพร่องทั้งหมดจำนวนมาก แต่ข้อบกพร่องเหล่านั้นส่วนใหญ่จะถูกปฏิเสธหรือไม่มีผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="36b45-178">Notice that although **Raw Materials** material type has many total defects, most of those defects are either rejected or have no impact.</span></span>

   <span data-ttu-id="36b45-179">เรามาตรวจสอบเพื่อยืนยันว่า ชนิดของวัสดุนี้ไม่ก่อให้เกิดการหยุดทำงานมากนัก แม้ว่าจะมีจำนวนข้อบกพร่องที่สูง</span><span class="sxs-lookup"><span data-stu-id="36b45-179">Let's verify that this material type doesn't cause much downtime, despite high defect quantity.</span></span>

2. <span data-ttu-id="36b45-180">ในแดชบอร์ด ดูที่ไทล์ **จำนวนข้อพร่องรวม เวลาหยุดทำงานรวมเป็นนาที ตามชนิดของวัสดุ**</span><span class="sxs-lookup"><span data-stu-id="36b45-180">In the dashboard, look at the **Total Defect Qty, Total Downtime Minutes by Material Type** tile.</span></span>

   ![ไทล์จำนวนข้อพร่องรวม เวลาหยุดทำงานรวมเป็นนาที ตามชนิดของวัสดุ](media/sample-supplier-quality/supplier10.png)

   <span data-ttu-id="36b45-182">เห็นได้ว่าการจัดการวัตถุดิบทำได้ดี: ถึงแม้ว่ามีจำนวนข้อบกพร่องมากกว่า แต่จำนวนนาทีรวมที่หยุดทำงานต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="36b45-182">Raw materials appear to be well managed; although they have more defects, they have lower total downtime minutes.</span></span>

### <a name="compare-defects-to-downtime-by-year"></a><span data-ttu-id="36b45-183">เปรียบเทียบข้อบกพร่องกับเวลาหยุดทำงาน ตามปี</span><span class="sxs-lookup"><span data-stu-id="36b45-183">Compare defects to downtime by year</span></span>
1. <span data-ttu-id="36b45-184">เลือกไทล์แผนที่ **รายงานความบกพร่องรวม ตามโรงงาน, ชนิดข้อบกพร่อง** เพื่อเปิดรายงานไปยังหน้า **การวิเคราะห์คุณภาพผู้จัดหาสินค้า**</span><span class="sxs-lookup"><span data-stu-id="36b45-184">Select the **Total Defect Reports by Plant, Defect Type** map tile to open the report to the **Supplier Quality Analysis** page.</span></span>
2. <span data-ttu-id="36b45-185">ในแผนภูมิ **จำนวนข้อบกพร่องรวมแบ่งตามเดือนและปี**  ให้สังเกตว่าปริมาณข้อบกพร่องในปี 2014 สูงกว่ากว่าในปี 2013</span><span class="sxs-lookup"><span data-stu-id="36b45-185">In the **Total Defect Qty by Month and Year** chart, notice that defect quantity is higher in 2014 than in 2013.</span></span>  

    ![จำนวนข้อบกพร่องรวมแบ่งตามเดือนและปี](media/sample-supplier-quality/supplier11.png)  
3. <span data-ttu-id="36b45-187">ข้อบกพร่องที่มากกว่า ลงผลให้เกิดเวลาหยุดทำงานที่มากขึ้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="36b45-187">Do more defects translate into more downtime?</span></span> <span data-ttu-id="36b45-188">ถามคำถามในกล่อง Q&A เพื่อค้นหาคำตอบ</span><span class="sxs-lookup"><span data-stu-id="36b45-188">Ask questions in the Q&A box to find out.</span></span>  
4. <span data-ttu-id="36b45-189">เลือก **ตัวอย่างการวิเคราะห์คุณภาพผู้จัดหาสินค้า** ในบานหน้าต่างนำทางด้านบนเพื่อย้อนกลับไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="36b45-189">Select **Supplier Quality Analysis Sample** in the top nav pane to return to the dashboard.</span></span>  
5. <span data-ttu-id="36b45-190">เนื่องจากเราทราบว่าวัตถุดิบมีจำนวนข้อบกพร่องสูงสุด ให้พิมพ์ในกล่องคำถาม: *แสดงประเภทวัสดุ ปี และจำนวนข้อบกพร่องรวม*</span><span class="sxs-lookup"><span data-stu-id="36b45-190">Because we know that raw materials have the highest number of defects, type in the question box: *show material types, year, and total defect qty*.</span></span>  

    <span data-ttu-id="36b45-191">มีข้อบกพร่องที่เกิดจากวัตถุดิบในปี 2014 มากกว่าของปี 2013</span><span class="sxs-lookup"><span data-stu-id="36b45-191">There were many more raw materials defects in 2014 than in 2013.</span></span>  

    ![คำถาม Q&A: แสดงชนิดวัสดุ ปี และจำนวนข้อบกพร่องรวม](media/sample-supplier-quality/supplier12.png)  
6. <span data-ttu-id="36b45-193">ถัดไป เปลี่ยนคำถามเป็น: _แสดงชนิดของวัสดุ ปี และ **เวลาหยุดทำงานทั้งหมดเป็นนาที**_</span><span class="sxs-lookup"><span data-stu-id="36b45-193">Next, change the question to: _show material types, year, and total **downtime minutes**_.</span></span>  

   ![คำถาม Q&A: แสดงชนิดวัสดุ ปี และเวลาหยุดทำงานรวมเป็นนาที](media/sample-supplier-quality/supplier13.png)

   <span data-ttu-id="36b45-195">ขอให้สังเกตว่าเวลาหยุดทำงานเนื่องจากวัตถุดิบของปี 2013 และปี 2014 มีค่าใกล้เคียงกัน ถึงแม้ว่าจะมีข้อบกพร่องจากวัตถุดิบในปี 2014 มากกว่ามาก</span><span class="sxs-lookup"><span data-stu-id="36b45-195">Notice that downtime for raw materials was about the same in 2013 and 2014, even though there were many more raw materials defects in 2014.</span></span> <span data-ttu-id="36b45-196">ซึ่งปรากฏว่าข้อบกพร่องของวัตถุดิบในปี 2014 ไม่ได้ทำให้เกิดการหยุดทำงานเนื่องจากวัตถุดิบในปี 2014 มากขึ้น</span><span class="sxs-lookup"><span data-stu-id="36b45-196">It appears that more defects for raw materials in 2014 didn't lead to much more downtime for raw materials in 2014.</span></span>

### <a name="compare-defects-to-downtime-month-to-month"></a><span data-ttu-id="36b45-197">เปรียบเทียบข้อบกพร่องกับเวลาหยุดทำงาน เทียบเดือนต่อเดือน</span><span class="sxs-lookup"><span data-stu-id="36b45-197">Compare defects to downtime month to month</span></span>
<span data-ttu-id="36b45-198">มาดูอีกหนึ่งไทล์แดชบอร์ด ซึ่งเกี่ยวข้องกับจำนวนข้อบกพร่องรวม</span><span class="sxs-lookup"><span data-stu-id="36b45-198">Let's look at another dashboard tile related to total defective quantity.</span></span>  

1. <span data-ttu-id="36b45-199">เลือก **ออกจาก Q&A** ในมุมบนซ้ายเพื่อกลับไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="36b45-199">Select **Exit Q&A** in the upper-left corner to return to the dashboard.</span></span>  

    <span data-ttu-id="36b45-200">ดูรายละเอียดเพิ่มเติมในไทล์ **ปริมาณข้อบกพร่องรวม ตามเดือน ปี**</span><span class="sxs-lookup"><span data-stu-id="36b45-200">Look more closely at the **Total Defect Quantity by Month, Year** tile.</span></span> <span data-ttu-id="36b45-201">พบว่า ครึ่งปีแรกของปี 2014 มีจำนวนข้อบกพร่องที่คล้ายกับของปี 2013 แต่ในครึ่งปีหลังของปี 2014 จำนวนข้อบกพร่องเพิ่มขึ้นอย่างมาก</span><span class="sxs-lookup"><span data-stu-id="36b45-201">It shows that the first half of 2014 had a similar number of defects as 2013, but in the second half of 2014, the number of defects increased significantly.</span></span>  

    ![ไทล์ปริมาณข้อบกพร่องรวม ตามเดือน ปี](media/sample-supplier-quality/supplier14.png)  

    <span data-ttu-id="36b45-203">เรามาดูกันว่า การเพิ่มจำนวนของข้อบกพร่องนี้ ส่งผลให้เกิดเวลาหยุดทำงานเป็นนาทีในระดับที่เท่ากันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="36b45-203">Let's see if this increase in defect quantity led to an equal increase in downtime minutes.</span></span>  
2. <span data-ttu-id="36b45-204">ในกล่องคำถาม พิมพ์ *เวลาหยุดทำงานรวมเป็นนาที ตามเดือนและปี เป็นแผนภูมิเส้น*</span><span class="sxs-lookup"><span data-stu-id="36b45-204">In the question box, type *total downtime minutes by month and year as a line chart*.</span></span>  

   ![คำถาม Q&A: ผลรวมนาทีที่ไม่ได้ทำงานตามเดือนและปีเป็นแผนภูมิเส้น](media/sample-supplier-quality/supplier15.png)

   <span data-ttu-id="36b45-206">นอกเหนือจากการเพิ่มขึ้นของเวลาหยุดทำงานอย่างก้าวกระโดดในเดือนมิถุนายนและตุลาคม จำนวนข้อบกพร่องไม่ได้ส่งผลให้เกิดเวลาหยุดทำงานเพิ่มขึ้นอย่างมีนัยสำคัญ</span><span class="sxs-lookup"><span data-stu-id="36b45-206">Other than a jump in downtime minutes during June and October, the number of defects didn't result in significantly more downtime.</span></span> <span data-ttu-id="36b45-207">ผลลัพธ์นี้แสดงให้เห็นว่าเราจัดการกับข้อบกพร่องนี้ได้ดีทีเดียว</span><span class="sxs-lookup"><span data-stu-id="36b45-207">This result shows we're managing defects well.</span></span>  
3. <span data-ttu-id="36b45-208">เมื่อต้องการปักหมุดแผนภูมินี้ไปยังแดชบอร์ด เลือกไอคอนปักหมุด</span><span class="sxs-lookup"><span data-stu-id="36b45-208">To pin this chart to your dashboard, select the pin icon</span></span> ![ปักหมุดไอคอน](media/sample-supplier-quality/pin.png) <span data-ttu-id="36b45-210">เหนือกล่องคำถาม</span><span class="sxs-lookup"><span data-stu-id="36b45-210">above the question box.</span></span>  
4. <span data-ttu-id="36b45-211">เพื่อจะสำรวจเดือนที่มีค่าแตกต่างจากเดือนอื่นมาก ลองดูจำนวนนาทีในเดือนตุลาคม ตามชนิดของวัสดุ ตำแหน่งโรงงาน ประเภท และอื่นๆ โดยการถามคำถามเช่น *เวลาหยุดทำงานรวมเป็นนาที ในเดือนตุลาคม ตามโรงงาน*</span><span class="sxs-lookup"><span data-stu-id="36b45-211">To explore the outlier months, check out the downtime minutes during October by material type, plant location, category, and so on, by asking questions such as *total downtime minutes in October by plant*.</span></span> 
5. <span data-ttu-id="36b45-212">เลือก **ออกจาก Q&A** ในมุมบนซ้ายเพื่อกลับไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="36b45-212">Select **Exit Q&A** in the upper-left corner to return to the dashboard.</span></span>

## <a name="next-steps-connect-to-your-data"></a><span data-ttu-id="36b45-213">ขั้นตอนถัดไป: เชื่อมต่อไปยังข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="36b45-213">Next steps: Connect to your data</span></span>
<span data-ttu-id="36b45-214">สภาพแวดล้อมนี้มีความปลอดภัยให้ดำเนินการต่าง ๆ ได้ เนื่องจากคุณสามารถเลือกที่จะไม่บันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="36b45-214">This environment is a safe one to play in, because you can choose not to save your changes.</span></span> <span data-ttu-id="36b45-215">ถ้าคุณบันทึก คุณสามารถเลือก **รับข้อมูล** สำหรับสำเนาชุดใหม่ของตัวอย่างนี้ได้เสมอ</span><span class="sxs-lookup"><span data-stu-id="36b45-215">But if you do save them, you can always select **Get Data** for a new copy of this sample.</span></span>

<span data-ttu-id="36b45-216">เราหวังว่าการแนะนำนี้ได้แสดงให้เห็นว่าแดชบอร์ด Q&A และรายงาน Power BI สามารถให้ข้อมูลเชิงลึกในข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="36b45-216">We hope this tour has shown how Power BI dashboards, Q&A, and reports can provide insights into sample data.</span></span> <span data-ttu-id="36b45-217">ตอนนี้ถึงตาคุณแล้ว ลองเชื่อมต่อกับข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="36b45-217">Now it's your turn; connect to your own data.</span></span> <span data-ttu-id="36b45-218">ด้วย Power BI คุณสามารถเชื่อมต่อกับแหล่งข้อมูลที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="36b45-218">With Power BI, you can connect to a wide variety of data sources.</span></span> <span data-ttu-id="36b45-219">เมื่อต้องการเรียนรู้เพิ่มเติม ดู[เริ่มต้นใช้งานบริการ Power BI](../fundamentals/service-get-started.md)</span><span class="sxs-lookup"><span data-stu-id="36b45-219">To learn more, see [Get started with the Power BI service](../fundamentals/service-get-started.md).</span></span>
