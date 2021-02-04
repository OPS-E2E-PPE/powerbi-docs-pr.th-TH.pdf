---
title: 'ตัวอย่างการวิเคราะห์การจัดซื้อ: ชมการแนะนำ'
description: 'ตัวอย่างการวิเคราะห์การจัดซื้อสำหรับ Power BI: ชมการแนะนำ'
author: maggiesMSFT
ms.author: maggies
ms.reviewer: amac
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: conceptual
ms.date: 07/02/2019
LocalizationGroup: Samples
ms.openlocfilehash: 73384f2f2021d949fcaca26c5b9e55cd7f0407af
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96417554"
---
# <a name="procurement-analysis-sample-for-power-bi-take-a-tour"></a><span data-ttu-id="93ace-103">ตัวอย่างการวิเคราะห์การจัดซื้อสำหรับ Power BI: ชมการแนะนำ</span><span class="sxs-lookup"><span data-stu-id="93ace-103">Procurement Analysis sample for Power BI: Take a tour</span></span>

<span data-ttu-id="93ace-104">ชุดเนื้อหาตัวอย่างการวิเคราะห์การจัดซื้อประกอบด้วยแดชบอร์ด รายงาน และชุดข้อมูลที่วิเคราะห์ค่าใช้จ่ายเกี่ยวกับผู้จัดจำหน่ายของบริษัทผู้ผลิตตามประเภทและตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="93ace-104">The Procurement Analysis sample content pack contains a dashboard, report, and dataset that analyzes a manufacturing company's spending on vendors by category and location.</span></span> <span data-ttu-id="93ace-105">ในตัวอย่าง เราสำรวจด้านต่าง ๆ เหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="93ace-105">In the sample, we explore these areas:</span></span>

* <span data-ttu-id="93ace-106">ใครคือผู้จัดจำหน่ายที่ติดอันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="93ace-106">Who the top vendors are</span></span>
* <span data-ttu-id="93ace-107">ค่าใช้จ่ายประเภทใดที่เราจ่ายมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="93ace-107">What categories we spend the most on</span></span>
* <span data-ttu-id="93ace-108">ผู้จัดจำหน่ายรายใดที่ให้ส่วนลดแก่เราสูงสุด และเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="93ace-108">Which vendors give us the highest discount and when</span></span>

![แดชบอร์ดของตัวอย่างการวิเคราะห์การจัดซื้อ](media/sample-procurement/procurement1.png)

<span data-ttu-id="93ace-110">ตัวอย่างนี้เป็นส่วนหนึ่งของชุดตัวอย่าง ที่แสดงให้เห็นวิธีการที่คุณสามารถใช้ Power BI กับข้อมูล รายงาน และแดชบอร์ดที่เกี่ยวข้องกับธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="93ace-110">This sample is part of a series that shows how you can use Power BI with business-oriented data, reports, and dashboards.</span></span> <span data-ttu-id="93ace-111">ซึ่งสร้างขึ้นโดย [obviEnce](http://www.obvience.com/) ด้วยข้อมูลจริงที่ไม่มีการระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="93ace-111">It was created by [obviEnce](http://www.obvience.com/) with real data, which has been anonymized.</span></span> <span data-ttu-id="93ace-112">ข้อมูลมีให้ใช้งานหลายรูปแบบ: ชุดเนื้อหา ไฟล์ Power BI Desktop .pbix หรือเวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="93ace-112">The data is available in several formats: content pack, .pbix Power BI Desktop file, or Excel workbook.</span></span> <span data-ttu-id="93ace-113">ดู [ตัวอย่างสำหรับ Power BI](sample-datasets.md)</span><span class="sxs-lookup"><span data-stu-id="93ace-113">See [Samples for Power BI](sample-datasets.md).</span></span> 

<span data-ttu-id="93ace-114">บทช่วยสอนนี้จะสำรวจชุดเนื้อหาของตัวอย่างการวิเคราะห์การจัดซื้อในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="93ace-114">This tutorial explores the Procurement Analysis sample content pack in the Power BI service.</span></span> <span data-ttu-id="93ace-115">เนื่องจากประสบการณ์การใช้รายงานจะคล้ายคลึงกันใน Power BI Desktop ดังนั้นคุณสามารถใช้ Power BI Desktop กับไฟล์ .pbix ตัวอย่างใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="93ace-115">Because the report experience is similar in Power BI Desktop and in the service, you can also follow along by using the sample .pbix file in Power BI Desktop.</span></span> 

<span data-ttu-id="93ace-116">คุณไม่จำเป็นต้องมีสิทธิการใช้งาน Power BI ในการสำรวจตัวอย่างใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="93ace-116">You don't need a Power BI license to explore the samples in Power BI Desktop.</span></span> <span data-ttu-id="93ace-117">ถ้าคุณไม่มีสิทธิการใช้งาน Power BI Pro คุณสามารถบันทึกตัวอย่างไปยังพื้นที่ทำงานของฉันในบริการของ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="93ace-117">If you don't have a Power BI Pro license, you can save the sample to your My Workspace in the Power BI service.</span></span> 

## <a name="get-the-sample"></a><span data-ttu-id="93ace-118">รับตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="93ace-118">Get the sample</span></span>

<span data-ttu-id="93ace-119">ก่อนที่คุณสามารถใช้ตัวอย่าง คุณต้องดาวน์โหลดในรูปแบบ[ชุดเนื้อหา](#get-the-content-pack-for-this-sample)[ไฟล์ .pbix](#get-the-pbix-file-for-this-sample) หรือ[เวิร์กบุ๊ก Excel](#get-the-excel-workbook-for-this-sample)</span><span class="sxs-lookup"><span data-stu-id="93ace-119">Before you can use the sample, you must first download it as a [content pack](#get-the-content-pack-for-this-sample), [.pbix file](#get-the-pbix-file-for-this-sample), or [Excel workbook](#get-the-excel-workbook-for-this-sample).</span></span>

### <a name="get-the-content-pack-for-this-sample"></a><span data-ttu-id="93ace-120">รับชุดเนื้อหาสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="93ace-120">Get the content pack for this sample</span></span>

1. <span data-ttu-id="93ace-121">เปิดบริการ Power BI (app.powerbi.com) ลงชื่อเข้าใช้ และเปิดพื้นที่ทำงานที่คุณต้องการบันทึกตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="93ace-121">Open the Power BI service (app.powerbi.com), sign in, and open the workspace where you want to save the sample.</span></span> 

    <span data-ttu-id="93ace-122">ถ้าคุณไม่มีสิทธิการใช้งาน Power BI Pro คุณสามารถบันทึกตัวอย่างไปยังพื้นที่ทำงานของฉัน</span><span class="sxs-lookup"><span data-stu-id="93ace-122">If you don't have a Power BI Pro license, you can save the sample to your My Workspace.</span></span>

2. <span data-ttu-id="93ace-123">ที่มุมด้านล่างซ้าย เลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="93ace-123">In the bottom-left corner, select **Get Data**.</span></span>

    ![เลือกรับข้อมูล](media/sample-datasets/power-bi-get-data.png)
3. <span data-ttu-id="93ace-125">บนหน้า **รับข้อมูล** ที่ปรากฏขึ้น เลือก **ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="93ace-125">On the **Get Data** page that appears, select **Samples**.</span></span>

4. <span data-ttu-id="93ace-126">เลือก **ตัวอย่างการวิเคราะห์การจัดซื้อ** แล้วเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="93ace-126">Select **Procurement Analysis Sample**, and then choose **Connect**.</span></span>  
  
   ![เชื่อมต่อกับตัวอย่าง](media/sample-procurement/procurement1a.png)
   
5. <span data-ttu-id="93ace-128">Power BI นำเข้าชุดเนื้อหา จากนั้นเพิ่มแดชบอร์ด รายงาน และชุดข้อมูลใหม่ไปยังพื้นที่ทำงานปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="93ace-128">Power BI imports the content pack, and then adds a new dashboard, report, and dataset to your current workspace.</span></span>
   
   ![รายการตัวอย่างการวิเคราะห์การจัดซื้อ](media/sample-procurement/procurement-entry.png)
  
### <a name="get-the-pbix-file-for-this-sample"></a><span data-ttu-id="93ace-130">รับไฟล์ .pbix สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="93ace-130">Get the .pbix file for this sample</span></span>

<span data-ttu-id="93ace-131">อีกทางเลือกหนึ่งคือ คุณสามารถดาวน์โหลดตัวอย่างการวิเคราะห์การจัดซื้อเป็น[ไฟล์ .pbix](https://download.microsoft.com/download/D/5/3/D5390069-F723-413B-8D27-5888500516EB/Procurement%20Analysis%20Sample%20PBIX.pbix) ซึ่งถูกออกแบบมาสำหรับใช้กับ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="93ace-131">Alternatively, you can download the Procurement Analysis sample as a [.pbix file](https://download.microsoft.com/download/D/5/3/D5390069-F723-413B-8D27-5888500516EB/Procurement%20Analysis%20Sample%20PBIX.pbix), which is designed for use with Power BI Desktop.</span></span> 

### <a name="get-the-excel-workbook-for-this-sample"></a><span data-ttu-id="93ace-132">รับเวิร์กบุ๊ก Excel สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="93ace-132">Get the Excel workbook for this sample</span></span>

<span data-ttu-id="93ace-133">ถ้าคุณต้องการดูแหล่งข้อมูลสำหรับตัวอย่างนี้ ตัวอย่างนี้ยังมีให้ในรูปแบบ[เวิร์กบุ๊ก Excel](https://go.microsoft.com/fwlink/?LinkId=529784)</span><span class="sxs-lookup"><span data-stu-id="93ace-133">If you want to view the data source for this sample, it's also available as an [Excel workbook](https://go.microsoft.com/fwlink/?LinkId=529784).</span></span> <span data-ttu-id="93ace-134">เวิร์กบุ๊กประกอบด้วยแผ่นงาน Power View ที่คุณสามารถดู และปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="93ace-134">The workbook contains Power View sheets that you can view and modify.</span></span> <span data-ttu-id="93ace-135">หากต้องการดูข้อมูลดิบ ให้เปิดใช้งาน add-in การวิเคราะห์ข้อมูล แล้วจากนั้นเลือก **Power Pivot > จัดการ**</span><span class="sxs-lookup"><span data-stu-id="93ace-135">To see the raw data, enable the Data Analysis add-ins, and then select **Power Pivot > Manage**.</span></span> <span data-ttu-id="93ace-136">หากต้องการเปิดใช้งาน Power View และ Power Pivot add-in โปรดดู [สำรวจตัวอย่าง Excel ใน Excel ](sample-datasets.md#explore-excel-samples-inside-excel)สำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="93ace-136">To enable the Power View and Power Pivot add-ins, see [Explore the Excel samples in Excel](sample-datasets.md#explore-excel-samples-inside-excel) for details.</span></span>


## <a name="spending-trends"></a><span data-ttu-id="93ace-137">แนวโน้มค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="93ace-137">Spending trends</span></span>
<span data-ttu-id="93ace-138">ก่อนอื่น มาดูแนวโน้มค่าใช้จ่ายตามประเภทและตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="93ace-138">First, let's look for trends in spending by category and location.</span></span>  

1. <span data-ttu-id="93ace-139">ในพื้นที่ทำงานที่คุณบันทึกตัวอย่าง เปิดแท็บ **แดชบอร์ด** จาก นั้นค้นหาแดชบอร์ด **ตัวอย่างการวิเคราะห์การจัดซื้อ** และเลือก</span><span class="sxs-lookup"><span data-stu-id="93ace-139">In the workspace where you saved the sample, open the **Dashboards** tab, then find the **Procurement Analysis Sample** dashboard and select it.</span></span> 
2. <span data-ttu-id="93ace-140">เลือกไทล์แดชบอร์ด **ใบแจ้งหนี้รวมตามประเทศ/ภูมิภาค** ซึ่งเปิดขึ้นในหน้า **ภาพรวมการใช้จ่าย** ของรายงาน **ตัวอย่างการวิเคราะห์การจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="93ace-140">Select the dashboard tile, **Total Invoice by Country/Region**, which opens to the **Spend Overview** page of the **Procurement Analysis Sample** report.</span></span>

    ![หน้าภาพรวมการใช้จ่าย](media/sample-procurement/procurement2.png)

<span data-ttu-id="93ace-142">บันทึกรายละเอียดดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="93ace-142">Note the following details:</span></span>

* <span data-ttu-id="93ace-143">ในแผนภูมิเส้น **ใบแจ้งหนี้รวมตามเดือนและประเภท**: ประเภท **โดยตรง** มีการใช้จ่ายที่ค่อนข้างเสมอต้นเสมอปลาย ประเภท **ลอจิสติกส์** มีค่าสูงสุดในเดือนธันวาคม และประเภท **อื่น ๆ** มีการดีดขึ้นในเดือนกุมภาพันธ์</span><span class="sxs-lookup"><span data-stu-id="93ace-143">In the **Total Invoice by Month and Category** line chart, the **Direct** category has consistent spending, **Logistics** has a peak in December, and **Other** has a spike in February.</span></span>
* <span data-ttu-id="93ace-144">ในแผนที่ **ใบแจ้งหนี้รวมตามประเทศ/ภูมิภาค**: ส่วนใหญ่ของค่าใช้จ่ายของเราอยู่ในสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="93ace-144">In the **Total Invoice by Country/Region** map, most of our spending is in the United States.</span></span>
* <span data-ttu-id="93ace-145">ในแผนภูมิคอลัมน์ **ใบแจ้งหนี้รวมตามประเภทย่อย**: **ฮาร์ดแวร์** และ **สินค้าทางอ้อมและบริการ** เป็นประเภทมีค่าใช้จ่ายสูงที่สุด</span><span class="sxs-lookup"><span data-stu-id="93ace-145">In the **Total Invoice by Sub Category** column chart, **Hardware** and **Indirect Goods & Services** are the biggest spend categories.</span></span>
* <span data-ttu-id="93ace-146">ในแผนภูมิแท่ง **ใบแจ้งหนี้รวมตามระดับ**: ธุรกิจส่วนใหญ่ของเราทำกับผู้จัดจำหน่ายระดับ 1 (10 อันดับแรก)</span><span class="sxs-lookup"><span data-stu-id="93ace-146">In the **Total Invoice by Tier** bar chart, most of our business is done with our tier 1 (top 10) vendors.</span></span> <span data-ttu-id="93ace-147">การดำเนินการดังกล่าวช่วยให้เราสามารถจัดการความสัมพันธ์ผู้จัดจำหน่ายได้ดียิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="93ace-147">Doing so enables us to manage better vendor relationships.</span></span>

## <a name="spending-in-mexico"></a><span data-ttu-id="93ace-148">ค่าใช้จ่ายในเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="93ace-148">Spending in Mexico</span></span>
<span data-ttu-id="93ace-149">เรามาสำรวจค่าใช้จ่ายในเม็กซิโกกัน</span><span class="sxs-lookup"><span data-stu-id="93ace-149">Let's explore the spending areas in Mexico.</span></span>

1. <span data-ttu-id="93ace-150">ในแผนที่ **ใบแจ้งหนี้รวมตามประเทศ/ภูมิภาค** เลือกแผนภูมิแบบฟอง **เม็กซิโก**</span><span class="sxs-lookup"><span data-stu-id="93ace-150">In the **Total Invoice by Country/Region** map, select the **Mexico** bubble.</span></span> <span data-ttu-id="93ace-151">โปรดสังเกตว่า ในแผนภูมิคอลัมน์ **ใบแจ้งหนี้รวมตามประเภทย่อย** ค่าใช้จ่ายส่วนใหญ่จะอยู่ในประเภทย่อย **สินค้าทางอ้อมและบริการ**</span><span class="sxs-lookup"><span data-stu-id="93ace-151">Notice that in the **Total Invoice by Sub Category** column chart, most spending is in the **Indirect Goods & Services** sub category.</span></span>

   ![เลือกเม็กซิโกในหน้าภาพรวมการใช้จ่าย](media/sample-procurement/pbi_procsample_spendmexico.png)
2. <span data-ttu-id="93ace-153">การดูรายละเอียดลึกลงไปในคอลัมน์ **สินค้าทางอ้อมและบริการ**:</span><span class="sxs-lookup"><span data-stu-id="93ace-153">Drill down into the **Indirect Goods & Services** column:</span></span>

   * <span data-ttu-id="93ace-154">ในแผนภูมิ **ใบแจ้งหนี้รวมตามประเภทย่อย** เลือกลูกศรดูรายละเอียดแนวลึก ![ลูกศรดูรายละเอียดแนวลึก](media/sample-procurement/pbi_drilldown_icon.png)ในมุมขวาบนของแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="93ace-154">In the **Total Invoice by Sub Category** chart, select the drill-down arrow ![Drill-down arrow](media/sample-procurement/pbi_drilldown_icon.png) in the upper-right corner of the chart.</span></span>
   * <span data-ttu-id="93ace-155">เลือกคอลัมน์ **สินค้าทางอ้อมและบริการ**</span><span class="sxs-lookup"><span data-stu-id="93ace-155">Select the **Indirect Goods & Services** column.</span></span>

      <span data-ttu-id="93ace-156">ตามที่คุณเห็น ค่าใช้จ่ายสูงสุดโดยมากสำหรับประเภทย่อย **ยอดขายและการตลาด**</span><span class="sxs-lookup"><span data-stu-id="93ace-156">As you can see, the highest spending by far is for the **Sales & Marketing** subcategory.</span></span>
   * <span data-ttu-id="93ace-157">เลือก **เม็กซิโก** ในแผนที่อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="93ace-157">Select **Mexico** in the map again.</span></span>

      <span data-ttu-id="93ace-158">สำหรับเม็กซิโก ค่าใช้จ่ายที่สำคัญที่สุดคือประเภทย่อย **การบำรุงรักษาและการซ่อมแซม**</span><span class="sxs-lookup"><span data-stu-id="93ace-158">For Mexico, the biggest spending is in the **Maintenance & Repair** subcategory.</span></span>

      ![ดูรายละเอียดแนวลึกของสินค้าและบริการทางอ้อมสำหรับเม็กซิโก](media/sample-procurement/pbi_procsample_drill_mexico.png)
3. <span data-ttu-id="93ace-160">เลือกลูกศรขึ้นที่มุมบนซ้ายของแผนภูมิเพื่อกลับขึ้นไปข้างบน</span><span class="sxs-lookup"><span data-stu-id="93ace-160">Select the up arrow on the upper-left corner of the chart to drill back up.</span></span>
4. <span data-ttu-id="93ace-161">เลือกลูกศรดูรายละเอียดแนวลึกอีกครั้งเพื่อปิดการใช้รายละเอียดแนวลึก</span><span class="sxs-lookup"><span data-stu-id="93ace-161">Select the drill-down arrow again to turn drill down off.</span></span>  
5. <span data-ttu-id="93ace-162">ในบานหน้าต่างนำทางด้านบน ให้เลือก **ตัวอย่างการวิเคราะห์การจัดซื้อ** เพื่อกลับไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="93ace-162">In the top nav pane, select **Procurement Analysis Sample** to return to the dashboard.</span></span>

## <a name="evaluate-different-cities"></a><span data-ttu-id="93ace-163">ประเมินเมืองต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="93ace-163">Evaluate different cities</span></span>
<span data-ttu-id="93ace-164">เราสามารถใช้การไฮไลต์ เพื่อประเมินค่าเมืองต่าง ๆ กัน</span><span class="sxs-lookup"><span data-stu-id="93ace-164">We can use highlighting to evaluate different cities.</span></span>

1. <span data-ttu-id="93ace-165">เลือกไทล์แดชบอร์ด **ใบแจ้งหนี้รวม, % ส่วนลดตามเดือน** ซึ่งเปิดขึ้นในหน้า **การวิเคราะห์ส่วนลด** ของรายงาน **ตัวอย่างการวิเคราะห์การจัดซื้อ**</span><span class="sxs-lookup"><span data-stu-id="93ace-165">Select the dashboard tile, **Total Invoice, Discount % By Month**, which opens to the **Discount Analysis** page of the **Procurement Analysis Sample** report.</span></span>
2. <span data-ttu-id="93ace-166">ในแผนที่ต้นไม้ **ใบแจ้งหนี้รวมตามเมือง** เลือกแต่ละเมืองเพื่อเปรียบเทียบกัน</span><span class="sxs-lookup"><span data-stu-id="93ace-166">In the **Total Invoice by City** tree map, select each city in turn to see how they compare.</span></span> <span data-ttu-id="93ace-167">โปรดสังเกตว่าเกือบทั้งหมดของใบแจ้งหนี้ของเมืองไมอามีมาจากผู้จัดจำหน่ายระดับ 1</span><span class="sxs-lookup"><span data-stu-id="93ace-167">Notice that almost all of Miami's invoices are from tier 1 vendors.</span></span>

   ![เมืองเทียบกับ % ส่วนลดตามระดับ](media/sample-procurement/pbi_procsample_miamitreemap2.png)

## <a name="vendor-discounts"></a><span data-ttu-id="93ace-169">ส่วนลดผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="93ace-169">Vendor discounts</span></span>
<span data-ttu-id="93ace-170">เรามาสำรวจส่วนลดจากผู้จัดจำหน่าย และรอบระยะเวลาที่เราได้รับส่วนลดมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="93ace-170">Let's also explore the discounts available from vendors, and the time periods when we get the most discounts:</span></span>
* <span data-ttu-id="93ace-171">มีส่วนลดแตกต่างกันแต่ละเดือน หรือส่วนลดยังคงเหมือนเดิมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="93ace-171">Are the discounts different each month or do they remain the same?</span></span>
* <span data-ttu-id="93ace-172">มีเมืองบางที่ได้รับส่วนลดมากกว่าเมืองอื่น ๆ หรือไม่</span><span class="sxs-lookup"><span data-stu-id="93ace-172">Do some cities get more discounts than others?</span></span>

![หน้าการวิเคราะห์ส่วนลด](media/sample-procurement/procurement4.png)

### <a name="discount-by-month"></a><span data-ttu-id="93ace-174">ส่วนลด ตามเดือน</span><span class="sxs-lookup"><span data-stu-id="93ace-174">Discount by month</span></span>
<span data-ttu-id="93ace-175">หากดูที่แผนภูมิผสม **ใบแจ้งหนี้รวมและ%ส่วนลดตามเดือน** เราเห็นว่าเดือนกุมภาพันธ์คือเดือนที่ยุ่งที่สุด และเดือนกันยายนเป็นเดือนยุ่งน้อยที่สุด</span><span class="sxs-lookup"><span data-stu-id="93ace-175">If you look at the **Total Invoice and Discount % by Month** combo chart, we see that February is the busiest month, and September is the least busy month.</span></span> 

<span data-ttu-id="93ace-176">ดูที่เปอร์เซ็นต์ส่วนลดในช่วงเดือนเหล่านี้: เมื่อปริมาณเพิ่ม ส่วนลดจะลดลง และเมื่อปริมาณอยู่ในระดับต่ำ ส่วนลดจะเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="93ace-176">Look at the discount percent during these months: when volume increases, the discount shrinks, and when volume is low, the discount increases.</span></span> <span data-ttu-id="93ace-177">ยิ่งเราต้องการส่วนลด ข้อเสนอที่เราได้รับกลับยิ่งแย่ลง</span><span class="sxs-lookup"><span data-stu-id="93ace-177">The more we need the discount, the worse of a deal we get.</span></span>

![แผนภูมิใบแจ้งหนี้รวมและ % ส่วนลดตามเดือน](media/sample-procurement/procurement5.png)

### <a name="discount-by-city"></a><span data-ttu-id="93ace-179">ส่วนลด ตามเมือง</span><span class="sxs-lookup"><span data-stu-id="93ace-179">Discount by city</span></span>
<span data-ttu-id="93ace-180">อีกด้านหนึ่งที่จะสำรวจคือส่วนลดตามเมือง</span><span class="sxs-lookup"><span data-stu-id="93ace-180">Another area to explore is the discount by city.</span></span> <span data-ttu-id="93ace-181">เลือกแต่ละเมืองตามลำดับในแผนที่ต้นไม้ และดูว่าแผนภูมิอื่น ๆ มีการเปลี่ยนแปลงอย่างไร</span><span class="sxs-lookup"><span data-stu-id="93ace-181">Select each city in turn in the tree map and see how the other charts change:</span></span>

* <span data-ttu-id="93ace-182">เมืองเซนต์หลุยส์ มีการดีดขึ้นของจำนวนใบแจ้งหนี้ในเดือนกุมภาพันธ์ และการประหยัดจากส่วนลดได้ตกลงอย่างมากเดือนเมษายน</span><span class="sxs-lookup"><span data-stu-id="93ace-182">St. Louis had a large spike in total invoices in February and a large dip in discount savings in April.</span></span>
* <span data-ttu-id="93ace-183">เมืองเม็กซิโกซิตีมี %ส่วนลดสูงสุด (11.05%) และเมืองแอตแลนต้ามีส่วนลดน้อยที่สุด (0.08%)</span><span class="sxs-lookup"><span data-stu-id="93ace-183">Mexico City has the highest discount percentage (11.05%) and Atlanta has the smallest (0.08%).</span></span>

![กราฟส่วนลดสำหรับเมืองเม็กซิโกซิตี](media/sample-procurement/procurement6.png)

### <a name="edit-the-report"></a><span data-ttu-id="93ace-185">แก้ไขรายงาน</span><span class="sxs-lookup"><span data-stu-id="93ace-185">Edit the report</span></span>
<span data-ttu-id="93ace-186">เลือก **แก้ไขรายงาน** ในมุมบนซ้าย และสำรวจในมุมมองการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="93ace-186">Select **Edit report** in the upper-left corner and explore in Editing view:</span></span>

* <span data-ttu-id="93ace-187">ดูว่าหน้าสร้างขึ้นได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="93ace-187">See how the pages are made.</span></span>
* <span data-ttu-id="93ace-188">เพิ่มหน้าและแผนภูมิที่มาจากข้อมูลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="93ace-188">Add pages and charts based on the same data.</span></span>
* <span data-ttu-id="93ace-189">เปลี่ยนชนิดของการแสดงภาพของแผนภูมิ เช่น เปลี่ยนแผนที่ต้นไม้ ไปเป็นแผนภูมิโดนัท</span><span class="sxs-lookup"><span data-stu-id="93ace-189">Change the visualization type for a chart; for example, change the tree map to a donut chart.</span></span>
* <span data-ttu-id="93ace-190">ปักหมุดแผนภูมิเหล่านั้นไปยังแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="93ace-190">Pin charts to your dashboard.</span></span>

## <a name="next-steps-connect-to-your-data"></a><span data-ttu-id="93ace-191">ขั้นตอนถัดไป: เชื่อมต่อกับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="93ace-191">Next steps: Connect to your data</span></span>
<span data-ttu-id="93ace-192">สภาพแวดล้อมนี้มีความปลอดภัยให้ดำเนินการต่างๆ ได้ เนื่องจากคุณสามารถเลือกที่จะไม่บันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="93ace-192">This environment is a safe one to play in, because you can choose not to save your changes.</span></span> <span data-ttu-id="93ace-193">ถ้าคุณบันทึก คุณสามารถเลือก **รับข้อมูล** สำหรับสำเนาชุดใหม่ของตัวอย่างนี้ได้เสมอ</span><span class="sxs-lookup"><span data-stu-id="93ace-193">But if you do save them, you can always select **Get Data** for a new copy of this sample.</span></span>

<span data-ttu-id="93ace-194">เราหวังว่าการแนะนำนี้ได้แสดงให้เห็นว่าแดชบอร์ด Q&A และรายงาน Power BI สามารถให้ข้อมูลเชิงลึกในข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="93ace-194">We hope this tour has shown how Power BI dashboards, Q&A, and reports can provide insights into sample data.</span></span> <span data-ttu-id="93ace-195">ตอนนี้ถึงตาคุณแล้ว ลองเชื่อมต่อกับข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="93ace-195">Now it's your turn; connect to your own data.</span></span> <span data-ttu-id="93ace-196">ด้วย Power BI คุณสามารถเชื่อมต่อกับแหล่งข้อมูลที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="93ace-196">With Power BI, you can connect to a wide variety of data sources.</span></span> <span data-ttu-id="93ace-197">เมื่อต้องการเรียนรู้เพิ่มเติม ดู[เริ่มต้นใช้งานบริการ Power BI](../fundamentals/service-get-started.md)</span><span class="sxs-lookup"><span data-stu-id="93ace-197">To learn more, see [Get started with the Power BI service](../fundamentals/service-get-started.md).</span></span>
