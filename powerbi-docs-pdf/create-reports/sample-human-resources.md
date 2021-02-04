---
title: 'ตัวอย่างทรัพยากรบุคคล: ชมการแนะนำ'
description: 'ตัวอย่างทรัพยากรบุคคลสำหรับ Power BI: ชมการแนะนำ'
author: maggiesMSFT
ms.author: maggies
ms.reviewer: amac
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: conceptual
ms.date: 07/05/2019
LocalizationGroup: Samples
ms.openlocfilehash: 94cb0d7f5ac83220f3b37f878add4f5bfa2caaf6
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96395888"
---
# <a name="human-resources-sample-for-power-bi-take-a-tour"></a><span data-ttu-id="0dbde-103">ตัวอย่างทรัพยากรบุคคลสำหรับ Power BI: ชมการแนะนำ</span><span class="sxs-lookup"><span data-stu-id="0dbde-103">Human Resources sample for Power BI: Take a tour</span></span>

<span data-ttu-id="0dbde-104">ชุดเนื้อหาตัวอย่างทรัพยากรบุคคลประกอบด้วยแดชบอร์ด รายงาน และชุดข้อมูลสำหรับแผนกทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="0dbde-104">The Human Resources sample content pack contains a dashboard, report, and dataset for a human resources department.</span></span> <span data-ttu-id="0dbde-105">ในตัวอย่างนี้ แผนกทรัพยากรบุคคลมีรูปแบบการรายงานเดียวกันในทุกๆ บริษัท แม้ว่าจะอยู่ในอุตสาหกรรมต่างกันหรือมีขนาดต่างกันก็ตาม</span><span class="sxs-lookup"><span data-stu-id="0dbde-105">In this sample, the human resources department has the same reporting model across different companies, even when they differ by industry or size.</span></span> <span data-ttu-id="0dbde-106">ตัวอย่างนี้มีพนักงานใหม่ พนักงานที่ปฏิบัติงานอยู่ และพนักงานที่ลาออกไปแล้ว</span><span class="sxs-lookup"><span data-stu-id="0dbde-106">This sample looks at new hires, active employees, and employees who have left.</span></span> <span data-ttu-id="0dbde-107">ซึ่งมุ่งมั่นเสมอเพื่อเปิดเผยแนวโน้มในกลยุทธ์การจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="0dbde-107">It strives to uncover any trends in the hiring strategy.</span></span> <span data-ttu-id="0dbde-108">วัตถุประสงค์หลักของเราคือ ทำความเข้าใจเกี่ยวกับ:</span><span class="sxs-lookup"><span data-stu-id="0dbde-108">Our main objectives are to understand:</span></span>

* <span data-ttu-id="0dbde-109">เราจ้างใคร</span><span class="sxs-lookup"><span data-stu-id="0dbde-109">Who we hire</span></span>
* <span data-ttu-id="0dbde-110">อคติในกลยุทธ์การจ้างงานของเรา</span><span class="sxs-lookup"><span data-stu-id="0dbde-110">Biases in our hiring strategy</span></span>
* <span data-ttu-id="0dbde-111">แนวโน้มการลาออกตามความสมัครใจ</span><span class="sxs-lookup"><span data-stu-id="0dbde-111">Trends in voluntary separations</span></span>

![แดชบอร์ดของตัวอย่างทรัพยากรบุคคล](media/sample-human-resources/hr1.png)

<span data-ttu-id="0dbde-113">ตัวอย่างนี้เป็นส่วนหนึ่งของชุดตัวอย่าง ที่แสดงให้เห็นวิธีการที่คุณสามารถใช้ Power BI กับข้อมูล รายงาน และแดชบอร์ดที่เกี่ยวข้องกับธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="0dbde-113">This sample is part of a series that shows how you can use Power BI with business-oriented data, reports, and dashboards.</span></span> <span data-ttu-id="0dbde-114">ซึ่งสร้างขึ้นโดย [obviEnce](http://www.obvience.com/) ด้วยข้อมูลจริงที่ไม่มีการระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="0dbde-114">It was created by [obviEnce](http://www.obvience.com/) with real data, which has been anonymized.</span></span> <span data-ttu-id="0dbde-115">ข้อมูลมีให้ใช้งานหลายรูปแบบ: ชุดเนื้อหา ไฟล์ Power BI Desktop .pbix หรือเวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="0dbde-115">The data is available in several formats: content pack, .pbix Power BI Desktop file, or Excel workbook.</span></span> <span data-ttu-id="0dbde-116">ดู [ตัวอย่างสำหรับ Power BI](sample-datasets.md)</span><span class="sxs-lookup"><span data-stu-id="0dbde-116">See [Samples for Power BI](sample-datasets.md).</span></span> 

<span data-ttu-id="0dbde-117">บทช่วยสอนนี้จะสำรวจชุดเนื้อหาของตัวอย่างทรัพยากรบุคคลในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="0dbde-117">This tutorial explores the Human Resources sample content pack in the Power BI service.</span></span> <span data-ttu-id="0dbde-118">เนื่องจากประสบการณ์การใช้รายงานจะคล้ายคลึงกันใน Power BI Desktop ดังนั้นคุณสามารถใช้ Power BI Desktop กับไฟล์ .pbix ตัวอย่างใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="0dbde-118">Because the report experience is similar in Power BI Desktop and in the service, you can also follow along by using the sample .pbix file in Power BI Desktop.</span></span> 

<span data-ttu-id="0dbde-119">คุณไม่จำเป็นต้องมีสิทธิการใช้งาน Power BI ในการสำรวจตัวอย่างใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="0dbde-119">You don't need a Power BI license to explore the samples in Power BI Desktop.</span></span> <span data-ttu-id="0dbde-120">ถ้าคุณไม่มีสิทธิการใช้งาน Power BI Pro คุณสามารถบันทึกตัวอย่างไปยังพื้นที่ทำงานของฉันในบริการของ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="0dbde-120">If you don't have a Power BI Pro license, you can save the sample to your My Workspace in the Power BI service.</span></span> 

## <a name="get-the-sample"></a><span data-ttu-id="0dbde-121">รับตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="0dbde-121">Get the sample</span></span>

<span data-ttu-id="0dbde-122">ก่อนที่คุณสามารถใช้ตัวอย่าง คุณต้องดาวน์โหลดในรูปแบบ[ชุดเนื้อหา](#get-the-content-pack-for-this-sample)[ไฟล์ .pbix](#get-the-pbix-file-for-this-sample) หรือ[เวิร์กบุ๊ก Excel](#get-the-excel-workbook-for-this-sample)</span><span class="sxs-lookup"><span data-stu-id="0dbde-122">Before you can use the sample, you must first download it as a [content pack](#get-the-content-pack-for-this-sample), [.pbix file](#get-the-pbix-file-for-this-sample), or [Excel workbook](#get-the-excel-workbook-for-this-sample).</span></span>

### <a name="get-the-content-pack-for-this-sample"></a><span data-ttu-id="0dbde-123">รับชุดเนื้อหาสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="0dbde-123">Get the content pack for this sample</span></span>

1. <span data-ttu-id="0dbde-124">เปิดบริการ Power BI (app.powerbi.com) ลงชื่อเข้าใช้ และเปิดพื้นที่ทำงานที่คุณต้องการบันทึกตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="0dbde-124">Open the Power BI service (app.powerbi.com), sign in, and open the workspace where you want to save the sample.</span></span>

   <span data-ttu-id="0dbde-125">ถ้าคุณไม่มีสิทธิการใช้งาน Power BI Pro คุณสามารถบันทึกตัวอย่างไปยังพื้นที่ทำงานของฉัน</span><span class="sxs-lookup"><span data-stu-id="0dbde-125">If you don't have a Power BI Pro license, you can save the sample to your My Workspace.</span></span>

2. <span data-ttu-id="0dbde-126">ที่มุมด้านล่างซ้าย เลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="0dbde-126">In the bottom-left corner, select **Get Data**.</span></span>
   
   ![เลือกรับข้อมูล](media/sample-datasets/power-bi-get-data.png)
3. <span data-ttu-id="0dbde-128">บนหน้า **รับข้อมูล** ที่ปรากฏขึ้น เลือก **ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="0dbde-128">On the **Get Data** page that appears, select **Samples**.</span></span>
   
4. <span data-ttu-id="0dbde-129">เลือก **ตัวอย่างทรัพยากรบุคคล** แล้วเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="0dbde-129">Select **Human Resources Sample**, then choose **Connect**.</span></span>  
   
   ![เชื่อมต่อกับตัวอย่าง](media/sample-human-resources/pbi_hr_sample_connect.png)

5. <span data-ttu-id="0dbde-131">Power BI นำเข้าชุดเนื้อหา จากนั้นเพิ่มแดชบอร์ด รายงาน และชุดข้อมูลใหม่ไปยังพื้นที่ทำงานปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="0dbde-131">Power BI imports the content pack and then adds a new dashboard, report, and dataset to your current workspace.</span></span>
   
   ![รายการตัวอย่างทรัพยากรบุคคล](media/sample-human-resources/hr-sample-entry.png)
  
### <a name="get-the-pbix-file-for-this-sample"></a><span data-ttu-id="0dbde-133">รับไฟล์ .pbix สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="0dbde-133">Get the .pbix file for this sample</span></span>

<span data-ttu-id="0dbde-134">อีกทางเลือกหนึ่งคือ คุณสามารถดาวน์โหลดตัวอย่างแผนกทรัพยากรบุคคลเป็ น[ไฟล์ .pbix](https://download.microsoft.com/download/6/9/5/69503155-05A5-483E-829A-F7B5F3DD5D27/Human%20Resources%20Sample%20PBIX.pbix) ซึ่งถูกออกแบบมาสำหรับใช้กับ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="0dbde-134">Alternatively, you can download the Human Resources sample as a [.pbix file](https://download.microsoft.com/download/6/9/5/69503155-05A5-483E-829A-F7B5F3DD5D27/Human%20Resources%20Sample%20PBIX.pbix), which is designed for use with Power BI Desktop.</span></span>

### <a name="get-the-excel-workbook-for-this-sample"></a><span data-ttu-id="0dbde-135">รับเวิร์กบุ๊ก Excel สำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="0dbde-135">Get the Excel workbook for this sample</span></span>

<span data-ttu-id="0dbde-136">ถ้าคุณต้องการดูแหล่งข้อมูลสำหรับตัวอย่างนี้ ตัวอย่างนี้ยังมีให้ในรูปแบบ[เวิร์กบุ๊ก Excel](https://go.microsoft.com/fwlink/?LinkId=529780)</span><span class="sxs-lookup"><span data-stu-id="0dbde-136">If you want to view the data source for this sample, it's also available as an [Excel workbook](https://go.microsoft.com/fwlink/?LinkId=529780).</span></span> <span data-ttu-id="0dbde-137">เวิร์กบุ๊กประกอบด้วยแผ่นงาน Power View ที่คุณสามารถดู และปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="0dbde-137">The workbook contains Power View sheets that you can view and modify.</span></span> <span data-ttu-id="0dbde-138">หากต้องการดูข้อมูลดิบ ให้เปิดใช้งาน add-in การวิเคราะห์ข้อมูล แล้วจากนั้นเลือก **Power Pivot > จัดการ**</span><span class="sxs-lookup"><span data-stu-id="0dbde-138">To see the raw data, enable the Data Analysis add-ins, and then select **Power Pivot > Manage**.</span></span> <span data-ttu-id="0dbde-139">หากต้องการเปิดใช้งาน Power View และ Power Pivot add-in โปรดดู [สำรวจตัวอย่าง Excel ใน Excel ](sample-datasets.md#explore-excel-samples-inside-excel)สำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="0dbde-139">To enable the Power View and Power Pivot add-ins, see [Explore the Excel samples in Excel](sample-datasets.md#explore-excel-samples-inside-excel) for details.</span></span>

## <a name="new-hires"></a><span data-ttu-id="0dbde-140">การจ้างใหม่</span><span class="sxs-lookup"><span data-stu-id="0dbde-140">New hires</span></span>
<span data-ttu-id="0dbde-141">เรามาสำรวจพนักงานจ้างใหม่กันก่อน</span><span class="sxs-lookup"><span data-stu-id="0dbde-141">Let's explore new hires first.</span></span>

1. <span data-ttu-id="0dbde-142">ในพื้นที่ทำงานของคุณ เลือกแท็บ **แดชบอร์ด** และเปิดแดชบอร์ด **ตัวอย่างทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="0dbde-142">In your workspace, select the **Dashboards** tab, and open the **Human Resources Sample** dashboard.</span></span>
2. <span data-ttu-id="0dbde-143">บนแดชบอร์ด เลือกไทล์ **จำนวนการจ้างใหม่, การจ้างใหม่ช่วงเวลาเดียวกันปีที่แล้ว, % การเปลี่ยนแปลง YoY พนักงานที่ทำงาน** ตามเดือน</span><span class="sxs-lookup"><span data-stu-id="0dbde-143">On the dashboard, select the **New Hire Count, New Hires Same Period Last Year, Actives YoY % Change By Month** tile.</span></span>  

   ![ไทล์จำนวนพนักงานใหม่](media/sample-human-resources/hr2.png)  

   <span data-ttu-id="0dbde-145">รายงาน ตัวอย่างทรัพยากรบุคคล จะเปิดไปยังหน้า **การจ้างใหม่**</span><span class="sxs-lookup"><span data-stu-id="0dbde-145">The Human Resources Sample report opens to the **New Hires** page.</span></span>  

   ![หน้าพนักงานใหม่](media/sample-human-resources/hr3.png)

3. <span data-ttu-id="0dbde-147">ดูรายการที่สนใจเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="0dbde-147">Look at these items of interest:</span></span>

    * <span data-ttu-id="0dbde-148">แผนภูมิผสม **จำนวนการจ้างใหม่, การจ้างใหม่ช่วงเวลาเดียวกันปีที่แล้ว, % การเปลี่ยนแปลง YoY พนักงานที่ทำงาน ตามเดือน** แสดงให้เห็นว่าเราจ้างคนจำนวนมากกว่าปีที่แล้วทุกเดือน</span><span class="sxs-lookup"><span data-stu-id="0dbde-148">The **New Hire Count, New Hires SPLY and Actives YoY % Change by Month** combo chart shows we hired more people every month this year compared to last year.</span></span> <span data-ttu-id="0dbde-149">บางเดือนจะมีผู้คนจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="0dbde-149">Significantly more people in some months.</span></span>
    * <span data-ttu-id="0dbde-150">ในแผนภูมิผสม **จำนวนการจ้างใหม่ และพนักงานที่ทำงานอยู่ แบ่งตามภูมิภาคและเชื้อชาติ** เราเห็นว่าเรากำลังจ้างพนักงานในภูมิภาค **ตะวันออก** น้อยลง</span><span class="sxs-lookup"><span data-stu-id="0dbde-150">In the combo chart **New Hire Count and Active Employee Count by Region and Ethnicity**, notice we're hiring fewer people in the **East** region.</span></span>
    * <span data-ttu-id="0dbde-151">แผนภูมิแบบน้ำตก **ความแปรปรวนของจ้างใหม่ YoY แบ่งตามกลุ่มอายุ** แสดงให้เห็นว่าเรากำลังจ้างคนที่มีอายุน้อยเป็นหลัก</span><span class="sxs-lookup"><span data-stu-id="0dbde-151">The **New Hires YoY Var by Age Group** waterfall chart shows we're hiring mainly younger people.</span></span> <span data-ttu-id="0dbde-152">แนวโน้มนี้อาจมาจากลักษณะงานที่ไม่เต็มเวลาเสียส่วนใหญ่</span><span class="sxs-lookup"><span data-stu-id="0dbde-152">This trend may be due to the mostly part-time nature of the jobs.</span></span>
    * <span data-ttu-id="0dbde-153">แผนภูมิวงกลม **จำนวนการจ้างใหม่แบ่งตามเพศ** แสดงระดับใกล้เคียงกันแบบผิวเผิน</span><span class="sxs-lookup"><span data-stu-id="0dbde-153">The **New Hire Count by Gender** pie chart shows a roughly even split.</span></span>

    <span data-ttu-id="0dbde-154">คุณสามารถค้นหาข้อมูลเชิงลึกเพิ่มเติมหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="0dbde-154">Can you find more insights?</span></span> <span data-ttu-id="0dbde-155">เช่น ภูมิภาคที่การจ้างงานแต่ละเพศมีความแตกต่างกันมาก</span><span class="sxs-lookup"><span data-stu-id="0dbde-155">For example, a region where the gender split is not even.</span></span> 

4. <span data-ttu-id="0dbde-156">เลือกกลุ่มอายุและเพศที่แตกต่างกันในแผนภูมิ เพื่อสำรวจความสัมพันธ์ระหว่างอายุ เพศ ภูมิภาค และกลุ่มเชื้อชาติ</span><span class="sxs-lookup"><span data-stu-id="0dbde-156">Select different age groups and genders in the charts to explore the relationships between age, gender, region, and ethnicity group.</span></span>

5. <span data-ttu-id="0dbde-157">เลือก **ตัวอย่างทรัพยากรบุคคล** จากบานหน้าต่างนำทางด้านบนเพื่อกลับไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="0dbde-157">Select **Human Resource Sample** from the top nav pane to return to the dashboard.</span></span>

   ![กลับไปยังแดชบอร์ด](media/sample-human-resources/power-bi-breadcrumbs.png)

## <a name="compare-currently-active-and-former-employees"></a><span data-ttu-id="0dbde-159">เปรียบเทียบพนักงานปัจจุบันกับอดีตพนักงาน</span><span class="sxs-lookup"><span data-stu-id="0dbde-159">Compare currently active and former employees</span></span>
<span data-ttu-id="0dbde-160">ลองสำรวจข้อมูลพนักงานปัจจุบันและพนักงานที่ไม่ได้ทำงานในบริษัทแล้ว</span><span class="sxs-lookup"><span data-stu-id="0dbde-160">Let's explore data for currently active employees and employees who no longer work for the company.</span></span>

1. <span data-ttu-id="0dbde-161">บนแดชบอร์ด เลือกไทล์ **จำนวนพนักงานที่ทำงานอยู่ตามกลุ่มอายุ**</span><span class="sxs-lookup"><span data-stu-id="0dbde-161">On the dashboard, select the **Active Employee Count by Age Group** tile.</span></span>

   ![จำนวนพนักงานที่ทำงานอยู่ตามไทล์กลุ่มอายุ](media/sample-human-resources/pbi_hr_sample_activepie.png)

   <span data-ttu-id="0dbde-163">รายงาน ตัวอย่างทรัพยากรบุคคล จะเปิดไปยังหน้า **พนักงานปัจจุบัน เทียบกับ พนักงานที่ออกจากงาน**</span><span class="sxs-lookup"><span data-stu-id="0dbde-163">The Human Resources Sample report opens to the **Active Employees vs. Separations** page.</span></span>  

   ![พนักงานปัจจุบัน เทียบกับ หน้าการแยก](media/sample-human-resources/hr5.png)

 2. <span data-ttu-id="0dbde-165">ดูรายการที่สนใจเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="0dbde-165">Look at these items of interest:</span></span>

    * <span data-ttu-id="0dbde-166">แผนภูมิผสมสองอันทางด้านซ้ายแสดงการเปลี่ยนแปลงปีต่อปี สำหรับการแยกพนักงานที่ทำงานอยู่และที่ลาออกไปแล้ว</span><span class="sxs-lookup"><span data-stu-id="0dbde-166">The two combo charts on the left show the year-over-year change for active employees and employee separations.</span></span> <span data-ttu-id="0dbde-167">เรามีพนักงานที่ทำงานอยู่ในปีนี้มากขึ้น เพราะมีการจ้างเพิ่มขึ้น แต่การออกจากงานก็มีมากกว่าปีที่แล้วด้วย</span><span class="sxs-lookup"><span data-stu-id="0dbde-167">We have more active employees this year due to rapid hiring, but also more separations than last year.</span></span>
    * <span data-ttu-id="0dbde-168">ในเดือนสิงหาคม เรามีพนักงานออกไปมากเทียบกับเดือนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="0dbde-168">In August, we had more separations compared to other months.</span></span> <span data-ttu-id="0dbde-169">ลองเลือกกลุ่มอายุ เพศ หรือภูมิภาค ที่ต่างกันดู เพื่อดูว่าคุณสามารถหาค่าที่ผิดปกติได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0dbde-169">Select the different age groups, genders, or regions to see if you can find any outliers.</span></span>
    * <span data-ttu-id="0dbde-170">ดูที่แผนภูมิวงกลม เราสังเกตการลาออกของพนักงานของเราตามเพศและกลุ่มอายุมีค่าพอ ๆ กัน</span><span class="sxs-lookup"><span data-stu-id="0dbde-170">Looking at the pie charts, we notice we have an even split in our active employees by gender and age groups.</span></span> <span data-ttu-id="0dbde-171">ลองเลือกกลุ่มอายุอื่นดู ดูว่าสัดส่วนของเพศที่กลุ่มอายุต่างๆ เป็นอย่างไร</span><span class="sxs-lookup"><span data-stu-id="0dbde-171">Select different age groups to see how the gender split differs by age.</span></span> <span data-ttu-id="0dbde-172">สัดส่วนของเพศมีค่าใกล้เคียงกันในทุกกลุ่มอายุหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="0dbde-172">Do we have an even split by gender in every age group?</span></span>

## <a name="reasons-for-separation"></a><span data-ttu-id="0dbde-173">เหตุผลของการออกจากงาน</span><span class="sxs-lookup"><span data-stu-id="0dbde-173">Reasons for separation</span></span>
<span data-ttu-id="0dbde-174">มาดูที่รายงาน ในมุมมองการแก้ไขกัน</span><span class="sxs-lookup"><span data-stu-id="0dbde-174">Let's look at the report in Editing View.</span></span> <span data-ttu-id="0dbde-175">คุณสามารถเปลี่ยนแผนภูมิวงกลมเพื่อให้แสดงข้อมูลแบบแยกของพนักงานลาออกแล้วแทนข้อมูลพนักงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="0dbde-175">You can change the pie charts to show employee separations data instead of active employee data.</span></span>

1. <span data-ttu-id="0dbde-176">เลือก **แก้ไขรายงาน** ตรงมุมบนซ้าย</span><span class="sxs-lookup"><span data-stu-id="0dbde-176">Select **Edit report** in the upper-left corner.</span></span>

2. <span data-ttu-id="0dbde-177">เลือกแผนภูมิวงกลม **จำนวนพนักงานที่ทำงานอยู่ตามกลุ่มอายุ**</span><span class="sxs-lookup"><span data-stu-id="0dbde-177">Select the **Active Employee Count by Age Group** pie chart.</span></span>

3. <span data-ttu-id="0dbde-178">ใน **เขตข้อมูล** **พนักงาน** เพื่อขยายตาราง **พนักงาน**</span><span class="sxs-lookup"><span data-stu-id="0dbde-178">In **Fields**, select **Employees** to expand the **Employees** table.</span></span> <span data-ttu-id="0dbde-179">ยกเลิก **จำนวนพนักงานที่ทำงานอยู่** เพื่อเอาเขตข้อมูลนั้นออก</span><span class="sxs-lookup"><span data-stu-id="0dbde-179">Clear **Active Employee Count** to remove that field.</span></span>

4. <span data-ttu-id="0dbde-180">เลือก **จำนวนการลาออก** ในตาราง **พนักงาน** เพื่อเพิ่มไปยังกล่อง **ค่า** ในบริเวณ **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="0dbde-180">Select **Separation Count** in the **Employees** table to add it to the **Values** box in the **Fields** area.</span></span>

5. <span data-ttu-id="0dbde-181">บนพื้นที่รายงาน เลือกแท่ง **ความสมัครใจ** ในแผนภูมิแท่ง **จำนวนการออกจากงานแยกตามเหตุผลการออกจากงาน**</span><span class="sxs-lookup"><span data-stu-id="0dbde-181">On the report canvas, select the **Voluntary** bar in the **Separation Count by Separation Reason** bar chart.</span></span> 

   <span data-ttu-id="0dbde-182">แถบนี้จะไฮไลต์พนักงานที่ออกจากงานโดยสมัครใจในภาพอื่นๆ ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="0dbde-182">This bar highlights those employees who left voluntarily in the other visuals in the report.</span></span>

6. <span data-ttu-id="0dbde-183">เลือกกลุ่มอายุ 50+ ของ แผนภูมิวงกลม **จำนวนการออกจากงานตามกลุ่มอายุ**</span><span class="sxs-lookup"><span data-stu-id="0dbde-183">Select the 50+ slice of the **Separation Count by Age Group** pie chart.</span></span>

7. <span data-ttu-id="0dbde-184">ดูที่แผนภูมิเส้นที่มุมล่างขวา</span><span class="sxs-lookup"><span data-stu-id="0dbde-184">Look at the line chart in the lower-right corner.</span></span> <span data-ttu-id="0dbde-185">แผนภูมินี้จะถูกกรองให้แสดงเฉพาะการออกจากงานตามความสมัครใจ</span><span class="sxs-lookup"><span data-stu-id="0dbde-185">This chart is filtered to show voluntary separations.</span></span>  

   ![พนักงานที่ลาออกเมื่ออายุเกิน 50 ปี](media/sample-human-resources/pbi_hr_sample_sepsover50.png)

   <span data-ttu-id="0dbde-187">สังเกตเห็นแนวโน้มในกลุ่มอายุ 50+ ได้หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="0dbde-187">Notice the trend in the 50+ age group.</span></span> <span data-ttu-id="0dbde-188">ในช่วงหลังของปี มีพนักงานอายุเกิน 50 ออกจากงานโดยสมัครใจมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="0dbde-188">During the latter part of the year, more employees over age 50 left voluntarily.</span></span> <span data-ttu-id="0dbde-189">แนวโน้มนี้เป็นแง่มุมที่ควรนำไปตรวจสอบต่อโดยใช้ข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0dbde-189">This trend is an area to investigate further with more data.</span></span>

8. <span data-ttu-id="0dbde-190">คุณยังสามารถทำตามขั้นตอนเดียวกัน กับแผนภูมิ **จำนวนพนักงานที่ทำงานอยู่แยกตามเพศ** แต่เปลี่ยนเป็นการออกจากงานแทนที่จะเป็นพนักงานที่ยังทำงานอยู่</span><span class="sxs-lookup"><span data-stu-id="0dbde-190">You can also follow the same steps for the **Active Employee Count by Gender** pie chart, changing it to separations instead of active employees.</span></span> <span data-ttu-id="0dbde-191">ดูข้อมูลการออกจากงานโดยสมัครใจ แยกตามเพศว่าคุณเห็นอะไรมากขึ้นบ้าง</span><span class="sxs-lookup"><span data-stu-id="0dbde-191">Look at the voluntary separation data by gender to see if you find any other insights.</span></span>

9. <span data-ttu-id="0dbde-192">เลือก **ตัวอย่างทรัพยากรบุคคล** จากบานหน้าต่างนำทางด้านบนเพื่อกลับไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="0dbde-192">Select **Human Resource Sample** from the top nav pane to return to the dashboard.</span></span> <span data-ttu-id="0dbde-193">คุณสามารถเลือกที่จะบันทึกการเปลี่ยนแปลงคุณที่ทำกับรายงาน</span><span class="sxs-lookup"><span data-stu-id="0dbde-193">You can choose to save the changes you've made to the report.</span></span>

## <a name="bad-hires"></a><span data-ttu-id="0dbde-194">การจ้างที่ไม่ดี</span><span class="sxs-lookup"><span data-stu-id="0dbde-194">Bad hires</span></span>
<span data-ttu-id="0dbde-195">ด้านสุดท้ายที่จะสำรวจคือการจ้างงานที่ไม่ดี</span><span class="sxs-lookup"><span data-stu-id="0dbde-195">The last area to explore is bad hires.</span></span> <span data-ttu-id="0dbde-196">เรานิยามการจ้างงานที่ไม่ดี ว่าเป็นพนักงานที่อยู่กับเราได้ไม่เกิน 60 วันแล้วก็ออกไป</span><span class="sxs-lookup"><span data-stu-id="0dbde-196">Bad hires are defined as employees who didn't last for more than 60 days.</span></span> <span data-ttu-id="0dbde-197">เรากำลังจ้างงานอย่างต่อเนื่อง แต่เรากำลังจ้างคนที่เหมาะสมอยู่หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="0dbde-197">We're hiring rapidly, but are we hiring good candidates?</span></span>

1. <span data-ttu-id="0dbde-198">เลือกไทล์แดชบอร์ด **% การจ้างงานที่ไม่ดีเทียบกับพนักงานที่ทำ แยกตามกลุ่มอายุ**</span><span class="sxs-lookup"><span data-stu-id="0dbde-198">Select the **Bad Hires as % of Actives by Age Group** dashboard tile.</span></span> <span data-ttu-id="0dbde-199">รายงานเปิดแท็บที่สาม **การจ้างที่ไม่ดี**</span><span class="sxs-lookup"><span data-stu-id="0dbde-199">The report opens to tab three, **Bad Hires**.</span></span>

   ![พนักงานที่ไม่ดีเป็น % ของพนักงานที่ทำงานอยู่ตามไทล์กลุ่มอายุ](media/sample-human-resources/hr7.png)  
2. <span data-ttu-id="0dbde-201">เลือก **ตะวันตกเฉียงเหนือ** ในตัวแบ่ง **ภูมิภาค** ที่ด้านซ้ายและเลือก **ผู้ชาย** ในแผนภูมิโดนัทของ **จำนวนการจ้างที่ไม่ดี**</span><span class="sxs-lookup"><span data-stu-id="0dbde-201">Select **Northwest** in the **Region** slicer on the left and select **Male** in the **Bad Hire Count by Gender** donut chart.</span></span> <span data-ttu-id="0dbde-202">ดูที่แผนภูมิอื่นๆ บนหน้า **การจ้างที่ไม่ดี**</span><span class="sxs-lookup"><span data-stu-id="0dbde-202">Look at the other charts on the **Bad Hires** page.</span></span> <span data-ttu-id="0dbde-203">สังเกตได้ว่าการจ้างงานที่ไม่ดีเป็นเพศชายมากกว่าเพศหญิง และมีการจ้างงานที่ไม่ดีในกลุ่ม A จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="0dbde-203">Notice there are more male bad hires than females and many Group A bad hires.</span></span>

   ![การจ้างที่ไม่ดีในตะวันตกเฉียงเหนือ](media/sample-human-resources/pbi_hr_sample_badhirespage.png)  

3. <span data-ttu-id="0dbde-205">หากคุณดูแผนภูมิโดนัท **จำนวนการจ้างที่ไม่ดีที่แบ่งตามเพศ** และเลือกกภูมิภาคที่ต่างกันในตัวแบ่ง **ภูมิภาค** คุณจะสังเกตได้ว่าภูมิภาคตะวันออกเป็นภูมิภาคเดียวที่เกิดการจ้างที่ไม่ดีในส่วนของผู้หญิงมากกว่าผู้ชาย</span><span class="sxs-lookup"><span data-stu-id="0dbde-205">If you look at the **Bad Hire Count by Gender** donut chart and select different regions in the **Region** slicer, you'll notice that the East region is the only region with more female than male bad hires.</span></span>  

4. <span data-ttu-id="0dbde-206">เลือกชื่อของแดชบอร์ดจากบานหน้าต่างนำทางด้านบนเพื่อกลับไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="0dbde-206">Select the name of the dashboard from the top nav pane to return to the dashboard.</span></span>

## <a name="ask-a-question-in-the-dashboard-qa-box"></a><span data-ttu-id="0dbde-207">ถามคำถามในกล่อง Q&A ของแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="0dbde-207">Ask a question in the dashboard Q&A box</span></span>
<span data-ttu-id="0dbde-208">ใน [กล่องคำถาม Q&A](power-bi-tutorial-q-and-a.md) ในแดชบอร์ด คุณสามารถถามคำถามเกี่ยวกับข้อมูลของคุฯโดยใช้ภาษาแบบธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="0dbde-208">In the [Q&A question box](power-bi-tutorial-q-and-a.md) in the dashboard, you can ask a question about your data by using natural language.</span></span> <span data-ttu-id="0dbde-209">Q&A เข้าใจคำที่คุณพิมพ์เข้าไป และหาว่าคำตอบอยู่ตรงไหนในชุดข้อมูลของคุณ เพื่อหาคำตอบนั้น</span><span class="sxs-lookup"><span data-stu-id="0dbde-209">Q&A recognizes the words you type and figures out where in your dataset to find the answer.</span></span>

1. <span data-ttu-id="0dbde-210">เลือกกล่องคำถาม Q&A</span><span class="sxs-lookup"><span data-stu-id="0dbde-210">Select the Q&A question box.</span></span> <span data-ttu-id="0dbde-211">โปรดทราบว่าแม้ว่าคุณยังไม่เริ่มพิมพ์ Q&A จะแสดงคำแนะนำเพื่อช่วยคุณสร้างคำถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="0dbde-211">Notice that even before you start typing, Q&A displays suggestions to help you form your question.</span></span>

   ![คำแนะนำกล่อง Q&A](media/sample-human-resources/pbi_hr_sample_qabox.png)

2. <span data-ttu-id="0dbde-213">คุณสามารถเลือกคำแนะนำหนึ่งในนั้น หรือพิมพ์: *แสดงกลุ่มอายุ เพศ และการจ้างงานที่ไม่ดี ช่วงเวลาเดียวกันปีที่แล้ว (SPLY) โดยที่ภูมิภาคคือตะวันออก*</span><span class="sxs-lookup"><span data-stu-id="0dbde-213">You can pick one of those suggestions, or enter: *show age group, gender, and bad hires SPLY where region is east*.</span></span>  

   ![คำตอบกล่อง Q&A](media/sample-human-resources/pbi_hr_sample_qa_answer.png)

   <span data-ttu-id="0dbde-215">โปรดสังเกตว่า ส่วนใหญ่ของการจ้างงานเพศหญิงที่ไม่ดีอายุต่ำกว่า 30</span><span class="sxs-lookup"><span data-stu-id="0dbde-215">Notice most of the female bad hires are under 30.</span></span>

## <a name="next-steps-connect-to-your-data"></a><span data-ttu-id="0dbde-216">ขั้นตอนถัดไป: เชื่อมต่อไปยังข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="0dbde-216">Next steps: Connect to your data</span></span>
<span data-ttu-id="0dbde-217">สภาพแวดล้อมนี้มีความปลอดภัยให้ดำเนินการต่าง ๆ ได้ เนื่องจากคุณสามารถเลือกที่จะไม่บันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="0dbde-217">This environment is a safe one to play in, because you can choose not to save your changes.</span></span> <span data-ttu-id="0dbde-218">ถ้าคุณบันทึก คุณสามารถเลือก **รับข้อมูล** สำหรับสำเนาชุดใหม่ของตัวอย่างนี้ได้เสมอ</span><span class="sxs-lookup"><span data-stu-id="0dbde-218">But if you do save them, you can always select **Get Data** for a new copy of this sample.</span></span>

<span data-ttu-id="0dbde-219">เราหวังว่าการแนะนำนี้ได้แสดงให้เห็นว่าแดชบอร์ด Q&A และรายงาน Power BI สามารถให้ข้อมูลเชิงลึกในข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="0dbde-219">We hope this tour has shown how Power BI dashboards, Q&A, and reports can provide insights into sample data.</span></span> <span data-ttu-id="0dbde-220">ตอนนี้ถึงตาคุณแล้ว ลองเชื่อมต่อกับข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="0dbde-220">Now it's your turn; connect to your own data.</span></span> <span data-ttu-id="0dbde-221">ด้วย Power BI คุณสามารถเชื่อมต่อกับแหล่งข้อมูลที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="0dbde-221">With Power BI, you can connect to a wide variety of data sources.</span></span> <span data-ttu-id="0dbde-222">เมื่อต้องการเรียนรู้เพิ่มเติม ดู[เริ่มต้นใช้งานบริการ Power BI](../fundamentals/service-get-started.md)</span><span class="sxs-lookup"><span data-stu-id="0dbde-222">To learn more, see [Get started with the Power BI service](../fundamentals/service-get-started.md).</span></span>
