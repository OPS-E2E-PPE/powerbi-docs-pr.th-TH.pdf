---
title: 'บทช่วยสอน: เปลี่ยนจากสมุดงาน Excel เป็นรายงานที่น่าทึ่งใน Power BI Desktop'
description: บทช่วยสอนนี้จะแสดงให้เห็นว่าคุณสามารถสร้างรายงานที่น่าทึ่งจากสมุดงาน Excel อย่างรวดเร็วได้อย่างไร
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: tutorial
ms.date: 10/13/2020
LocalizationGroup: Data from files
ms.openlocfilehash: b984c0f6ebee6cdcc9982956701f3a112be74ab7
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413207"
---
# <a name="tutorial-from-excel-workbook-to-stunning-report-in-power-bi-desktop"></a><span data-ttu-id="3bbd2-103">บทช่วยสอน: เปลี่ยนจากสมุดงาน Excel เป็นรายงานที่น่าทึ่งใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3bbd2-103">Tutorial: From Excel workbook to stunning report in Power BI Desktop</span></span>

<span data-ttu-id="3bbd2-104">ในบทช่วยสอนนี้ คุณจะต้องสร้างรายงานที่สวยงามตั้งแต่ขั้นตอนแรกจนสำเร็จภายในเวลา 20 นาที!</span><span class="sxs-lookup"><span data-stu-id="3bbd2-104">In this tutorial, you build a beautiful report from start to finish in 20 minutes!</span></span> 

:::image type="content" source="media/desktop-excel-stunning-report/power-bi-excel-formatted-report.png" alt-text="สกรีนช็อตของรายงาน Power BI ที่เสร็จสมบูรณ์"::: 

<span data-ttu-id="3bbd2-106">ผู้จัดการต้องการดูรายงานเกี่ยวกับตัวเลขยอดขายล่าสุดของคุณ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-106">Your manager wants to see a report on your latest sales figures.</span></span> <span data-ttu-id="3bbd2-107">ซึ่งผู้จัดการขอข้อมูลสรุปของฝ่ายบริหารดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3bbd2-107">They've requested an executive summary of:</span></span> 

- <span data-ttu-id="3bbd2-108">เดือนและปีใดที่มีผลกำไรมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="3bbd2-108">Which month and year had the most profit?</span></span> 
- <span data-ttu-id="3bbd2-109">บริษัทเห็นความสำเร็จมากที่สุดจากที่ใด (ตามประเทศ)</span><span class="sxs-lookup"><span data-stu-id="3bbd2-109">Where is the company seeing the most success (by country)?</span></span> 
- <span data-ttu-id="3bbd2-110">ผลิตภัณฑ์และเซกเมนต์ใดที่บริษัทควรลงทุนต่อ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-110">Which product and segment should the company continue to invest in?</span></span> 

<span data-ttu-id="3bbd2-111">เราสามารถสร้างรายงานนี้ได้ในเวลาไม่นานโดยใช้สมุดงานตัวอย่างด้านการเงินของเรา</span><span class="sxs-lookup"><span data-stu-id="3bbd2-111">Using our sample finance workbook, we can build this report in no time.</span></span> <span data-ttu-id="3bbd2-112">ซึ่งรายงานขั้นสุดท้ายจะมีลักษณะเช่นนี้</span><span class="sxs-lookup"><span data-stu-id="3bbd2-112">Here’s what the final report will look like.</span></span> <span data-ttu-id="3bbd2-113">มาเริ่มต้นกันเลย!</span><span class="sxs-lookup"><span data-stu-id="3bbd2-113">Let’s get started!</span></span> 

<span data-ttu-id="3bbd2-114">ในบทช่วยสอนนี้ คุณจะเรียนรู้วิธีการ:</span><span class="sxs-lookup"><span data-stu-id="3bbd2-114">In this tutorial, you'll learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="3bbd2-115">ดาวน์โหลดข้อมูลตัวอย่างสองวิธีที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="3bbd2-115">Download sample data two different ways</span></span>
> * <span data-ttu-id="3bbd2-116">จัดเตรียมข้อมูลของคุณด้วยการแปลงข้อมูลบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="3bbd2-116">Prepare your data with a few transformations</span></span>
> * <span data-ttu-id="3bbd2-117">สร้างรายงานที่มีชื่อเรื่อง วิชวลสามภาพ และตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3bbd2-117">Build a report with a title, three visuals, and a slicer</span></span>
> * <span data-ttu-id="3bbd2-118">เผยแพร่รายงานของคุณในบริการของ Power BI เพื่อให้คุณสามารถแชร์รายงานดังกล่าวกับเพื่อนร่วมงานของคุณได้</span><span class="sxs-lookup"><span data-stu-id="3bbd2-118">Publish your report to the Power BI service so you can share it with your colleagues</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3bbd2-119">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="3bbd2-119">Prerequisites</span></span>

- <span data-ttu-id="3bbd2-120">ก่อนที่คุณจะเริ่มต้น คุณจะต้อง[ดาวน์โหลด Power BI Desktop](https://powerbi.microsoft.com/desktop/)</span><span class="sxs-lookup"><span data-stu-id="3bbd2-120">Before you start, you need to [download Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span></span>
- <span data-ttu-id="3bbd2-121">หากคุณกำลังวางแผนที่จะเผยแพร่รายงานของคุณในบริการของ Power BI แต่คุณยังไม่ได้ลงทะเบียน โปรด[ลงทะเบียนสำหรับรุ่นทดลองใช้ฟรี](https://app.powerbi.com/signupredirect?pbi_source=web)</span><span class="sxs-lookup"><span data-stu-id="3bbd2-121">If you're planning to publish your report to the Power BI service and you aren't signed up yet, [sign up for a free trial](https://app.powerbi.com/signupredirect?pbi_source=web).</span></span>

## <a name="get-data"></a><span data-ttu-id="3bbd2-122">รับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3bbd2-122">Get data</span></span> 

<span data-ttu-id="3bbd2-123">คุณสามารถรับข้อมูลสำหรับบทช่วยสอนนี้ได้โดยใช้หนึ่งในสองวิธี</span><span class="sxs-lookup"><span data-stu-id="3bbd2-123">You can get the data for this tutorial using one of two methods.</span></span>

### <a name="get-data-in-power-bi-desktop"></a><span data-ttu-id="3bbd2-124">รับข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3bbd2-124">Get data in Power BI Desktop</span></span>

<span data-ttu-id="3bbd2-125">เมื่อคุณเปิด Power BI Desktop ให้เลือก **ลองใช้ชุดข้อมูลตัวอย่าง** จากพื้นที่ทำงานว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="3bbd2-125">When you open Power BI Desktop, select **Try a sample dataset** from the blank canvas.</span></span>

:::image type="content" source="media/desktop-excel-stunning-report/power-bi-desktop-canvas-sample-dataset.png" alt-text="สกรีนช็อตของลองใช้ชุดข้อมูลตัวอย่างบนพื้นที่ทำงาน"::: 

<span data-ttu-id="3bbd2-127">ถ้าคุณเคยเข้าชมบทช่วยสอนนี้จาก Power BI Desktop ดำเนินการต่อเลยและเลือก **โหลดข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-127">If you've landed on this tutorial from Power BI Desktop, go ahead and choose **Load data**.</span></span>

:::image type="content" source="media/desktop-excel-stunning-report/power-bi-two-ways-load-data.png" alt-text="สกรีนช็อตของสองวิธีในการใช้ข้อมูลตัวอย่าง > โหลดข้อมูล":::

### <a name="download-the-sample"></a><span data-ttu-id="3bbd2-129">ดาวน์โหลดตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3bbd2-129">Download the sample</span></span>

<span data-ttu-id="3bbd2-130">คุณยังสามารถดาวน์โหลดเวิร์กบุ๊กตัวอย่างได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="3bbd2-130">You can also download the sample workbook directly.</span></span> 

1. <span data-ttu-id="3bbd2-131">ดาวน์โหลด[สมุดงาน Excel สำหรับตัวอย่างด้านการเงิน](https://go.microsoft.com/fwlink/?LinkID=521962)</span><span class="sxs-lookup"><span data-stu-id="3bbd2-131">Download the [Financial sample Excel workbook](https://go.microsoft.com/fwlink/?LinkID=521962).</span></span>
1. <span data-ttu-id="3bbd2-132">เปิด Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3bbd2-132">Open Power BI Desktop.</span></span>
1. <span data-ttu-id="3bbd2-133">ในส่วน **ข้อมูล** ของแถบเครื่องมือริบบอน **หน้าหลัก** ให้เลือก **Excel**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-133">In the **Data** section of the **Home** ribbon, select **Excel**.</span></span>
1. <span data-ttu-id="3bbd2-134">ไปยังตำแหน่งที่คุณบันทึกสมุดงานตัวอย่างไว้ และเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-134">Navigate to where you saved the sample workbook, and select **Open**.</span></span>

## <a name="prepare-your-data"></a><span data-ttu-id="3bbd2-135">จัดเตรียมข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-135">Prepare your data</span></span> 

<span data-ttu-id="3bbd2-136">ใน **ตัวนำทาง** คุณมีตัวเลือกในการ *แปลง* หรือ *โหลด* ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3bbd2-136">In **Navigator**, you have the option to *transform* or *load* the data.</span></span> <span data-ttu-id="3bbd2-137">ตัวนำทางจะแสดงตัวอย่างของข้อมูลของคุณ คุณจึงสามารถตรวจสอบได้ว่าคุณมีช่วงข้อมูลที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="3bbd2-137">The Navigator provides a preview of your data so you can verify that you have the correct range of data.</span></span> <span data-ttu-id="3bbd2-138">ชนิดข้อมูลตัวเลขอยู่ในรูปแบบตัวเอียง</span><span class="sxs-lookup"><span data-stu-id="3bbd2-138">Numeric data types are italicized.</span></span> <span data-ttu-id="3bbd2-139">หากคุณต้องการเปลี่ยน ให้แปลงข้อมูลของคุณก่อนที่จะโหลด</span><span class="sxs-lookup"><span data-stu-id="3bbd2-139">If you need to make changes, transform your data before loading.</span></span> <span data-ttu-id="3bbd2-140">หากต้องการให้การแสดงภาพนั้นอ่านได้ง่ายขึ้นหลังจากนี้ เราจะต้องแปลงข้อมูลก่อน</span><span class="sxs-lookup"><span data-stu-id="3bbd2-140">To make the visualizations easier to read later, we do want to transform the data now.</span></span> <span data-ttu-id="3bbd2-141">ในการแปลงข้อมูลแต่ละครั้ง คุณจะเห็นข้อมูลดังกล่าวถูกเพิ่มในรายการที่ด้านล่าง **การตั้งค่าคิวรี** ใน **ขั้นตอนที่ใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-141">As you do each transformation, you see it added to the list under **Query Settings** in **Applied Steps**</span></span> 

1. <span data-ttu-id="3bbd2-142">เลือกตาราง **การเงิน** และเลือก **แปลงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-142">Select the **Financials** table, and choose **Transform Data**.</span></span> 

    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-financial-navigator.png" alt-text="ภาพหน้าจอของตัวนำทาง Power BI Navigator ที่มีข้อมูลตัวอย่างการเงิน"::: 

1. <span data-ttu-id="3bbd2-144">เลือกคอลัมน์ **หน่วยที่ขายได้**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-144">Select the **Units Sold** column.</span></span> <span data-ttu-id="3bbd2-145">บนแท็บ **หน้าหลัก** ให้เลือก **ชนิดข้อมูล** จากนั้นเลือก **จำนวนเต็ม**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-145">On the **Home** tab, select **Data Type**, then select **Whole Number**.</span></span> <span data-ttu-id="3bbd2-146">เลือก **แทนที่รายการปัจจุบัน** เพื่อเปลี่ยนชนิดคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="3bbd2-146">Choose **Replace current** to change the column type.</span></span> 

    <span data-ttu-id="3bbd2-147">ขั้นตอนการทำความสะอาดข้อมูลยอดนิยมที่ผู้ใช้ทำบ่อยที่สุดคือการเปลี่ยนแปลงชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3bbd2-147">The top data cleaning step users do most often is changing data types.</span></span> <span data-ttu-id="3bbd2-148">ในกรณีนี้ หน่วยที่ขายได้อยู่ในรูปแบบเลขทศนิยม</span><span class="sxs-lookup"><span data-stu-id="3bbd2-148">In this case, the units sold are in decimal form.</span></span> <span data-ttu-id="3bbd2-149">มันไม่สมเหตุสมผลเลย หากหน่วยที่ขายได้มีจำนวน 0.2 หรือ 0.5 ใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="3bbd2-149">It doesn’t make sense to have 0.2 or 0.5 of a unit sold, does it?</span></span> <span data-ttu-id="3bbd2-150">ดังนั้น เรามาเปลี่ยนหน่วยดังกล่าวให้เป็นจำนวนเต็มกันเถอะ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-150">So let’s change that to whole number.</span></span> 

    :::image type="content" source="media/desktop-excel-stunning-report/power-query-whole-number.png" alt-text="ภาพหน้าจอของการเปลี่ยนตัวเลขทศนิยมเป็นจำนวนเต็ม"::: 

1. <span data-ttu-id="3bbd2-152">เลือกคอลัมน์ **เซกเมนต์**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-152">Select the **Segment** column.</span></span> <span data-ttu-id="3bbd2-153">บนแท็บ **แปลง** ให้เลือก **จัดรูปแบบ** จากนั้นเลือก **ตัวพิมพ์ใหญ่**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-153">On the **Transform** tab, select **Format**, then select **UPPERCASE**.</span></span>

    <span data-ttu-id="3bbd2-154">นอกจากนี้เรายังต้องทำให้เซกเมนต์นั้นมองเห็นได้ง่ายขึ้นในแผนภูมิในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="3bbd2-154">We also want to make the segments easier to see in the chart later.</span></span> <span data-ttu-id="3bbd2-155">เราจะจัดรูปแบบคอลัมน์เซกเมนต์กัน</span><span class="sxs-lookup"><span data-stu-id="3bbd2-155">Let’s format the Segment column.</span></span> 

     :::image type="content" source="media/desktop-excel-stunning-report/power-query-upper-case.png" alt-text="ภาพหน้าจอของการเปลี่ยนหัวเรื่องจากตัวพิมพ์เล็กเป็นตัวพิมพ์ใหญ่":::

1. <span data-ttu-id="3bbd2-157">ให้ย่อชื่อคอลัมน์จาก **ชื่อเดือน** เป็น **เดือน** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3bbd2-157">Let's shorten the column name from **Month Name** to just **Month**.</span></span> <span data-ttu-id="3bbd2-158">ดับเบิลคลิกที่คอลัมน์ **ชื่อเดือน** และเปลี่ยนชื่อเป็น **เดือน** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3bbd2-158">Double-click the **Month Name** column, and rename to just **Month**.</span></span>  

     :::image type="content" source="media/desktop-excel-stunning-report/power-query-month-name.png" alt-text="ภาพหน้าจอของชื่อคอลัมน์ที่ตัดให้สั้นลง":::

1. <span data-ttu-id="3bbd2-160">ในคอลัมน์ **ผลิตภัณฑ์** ให้เลือกรายการแบบหล่นลงและยกเลิกการเลือกกล่องซึ่งอยู่ถัดจาก **มอนแทนา**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-160">In the **Product** column, select the dropdown and clear the box next to **Montana**.</span></span> 

     <span data-ttu-id="3bbd2-161">เราทราบว่าผลิตภัณฑ์มอนแทนาถูกยกเลิกเมื่อเดือนที่แล้ว ดังนั้นเราต้องการกรองข้อมูลนี้จากรายงานของเราเพื่อหลีกเลี่ยงความสับสน</span><span class="sxs-lookup"><span data-stu-id="3bbd2-161">We know the Montana product was discontinued last month, so we want to filter this data from our report to avoid confusion.</span></span> 

     :::image type="content" source="media/desktop-excel-stunning-report/power-query-montana.png" alt-text="ภาพหน้าจอของการลบค่ามอนแทนา":::

1. <span data-ttu-id="3bbd2-163">คุณจะเห็นว่าการแปลงข้อมูลแต่ละครั้งถูกเพิ่มในรายการที่ด้านล่าง **การตั้งค่าคิวรี** ใน **ขั้นตอนที่ใช้งาน** แล้ว</span><span class="sxs-lookup"><span data-stu-id="3bbd2-163">You see that each transformation has been added to the list under **Query Settings** in **Applied Steps**.</span></span>

    :::image type="content" source="media/desktop-excel-stunning-report/power-query-applied-steps.png" alt-text="ภาพหน้าจอของรายการขั้นตอนที่ใช้งาน":::

1. <span data-ttu-id="3bbd2-165">กลับไปที่แท็บ **หน้าหลัก** เลือก **ปิดและใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-165">Back on the **Home** tab, select **Close & Apply**.</span></span> <span data-ttu-id="3bbd2-166">ข้อมูลของเราเกือบจะพร้อมสำหรับการสร้างรายงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="3bbd2-166">Our data is almost ready for building a report.</span></span> 

    <span data-ttu-id="3bbd2-167">คุณเห็นสัญลักษณ์ซิกมาในรายการเขตข้อมูลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3bbd2-167">You see the Sigma symbol in the Fields list?</span></span> <span data-ttu-id="3bbd2-168">Power BI ตรวจพบว่าเขตข้อมูลเหล่านั้นเป็นตัวเลข</span><span class="sxs-lookup"><span data-stu-id="3bbd2-168">Power BI has detected that those fields are numeric.</span></span> <span data-ttu-id="3bbd2-169">Power BI ยังแสดงเขตข้อมูลวันที่ด้วยสัญลักษณ์ปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="3bbd2-169">Power BI also indicates the date field with a calendar symbol.</span></span>

     :::image type="content" source="media/desktop-excel-stunning-report/power-bi-fields-list-sigmas-date.png" alt-text="ภาพหน้าจอของรายการเขตข้อมูลที่มีเขตข้อมูลตัวเลขและเขตข้อมูลวันที่":::

### <a name="extra-credit-write-a-measure-in-dax"></a><span data-ttu-id="3bbd2-171">เครดิตเพิ่มเติม: เขียนหน่วยวัดใน DAX</span><span class="sxs-lookup"><span data-stu-id="3bbd2-171">Extra credit: Write a measure in DAX</span></span>

<span data-ttu-id="3bbd2-172">การเขียน *หน่วยวัด* ในภาษาสูตร *DAX* มีประสิทธิภาพสูงสุดสำหรับการสร้างรูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3bbd2-172">Writing *measures* in the *DAX* formula language is super powerful for data modeling.</span></span> <span data-ttu-id="3bbd2-173">มีข้อมูลมากมายที่ต้องเรียนรู้เกี่ยวกับ DAX ในการจัดทำเอกสารของ Power BI</span><span class="sxs-lookup"><span data-stu-id="3bbd2-173">There's lots to learn about DAX in the Power BI documentation.</span></span> <span data-ttu-id="3bbd2-174">ในตอนนี้ เราจะเขียนหน่วยวัดพื้นฐานและรวมสองตารางเข้าด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="3bbd2-174">For now, let's write a basic measure and join two tables.</span></span> 

1. <span data-ttu-id="3bbd2-175">เลือก **มุมมองข้อมูล** ทางด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="3bbd2-175">Select **Data View** on the left.</span></span> 
 
    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-data-view.png" alt-text="ภาพหน้าจอของไอคอนมุมมองข้อมูล":::

1. <span data-ttu-id="3bbd2-177">บนแถบเครื่องมือริบบอน **หน้าหลัก** ให้เลือก **ตารางใหม่**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-177">On the **Home** ribbon, select **New Table**.</span></span> 

    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-new-table.png" alt-text="ภาพหน้าจอของไอคอนตารางใหม่":::

1. <span data-ttu-id="3bbd2-179">พิมพ์หน่วยวัดนี้เพื่อสร้างตารางปฏิทินของวันที่ทั้งหมดระหว่างวันที่ 1 มกราคม 2013 ถึงวันที่ 31 ธันวาคม 2014</span><span class="sxs-lookup"><span data-stu-id="3bbd2-179">Type this measure to generate a Calendar table of all dates between January 1, 2013, and December 31, 2014.</span></span>  

    `Calendar = CALENDAR(DATE(2013,01,01),Date(2014,12,31))` 

2. <span data-ttu-id="3bbd2-180">เลือกเครื่องหมายถูกเพื่อดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-180">Select the check mark to commit.</span></span>

     :::image type="content" source="media/desktop-excel-stunning-report/power-bi-dax-expression.png" alt-text="ภาพหน้าจอของนิพจน์ DAX":::

1. <span data-ttu-id="3bbd2-182">ตอนนี้ ให้เลือก **มุมมองแบบจำลอง** ทางด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="3bbd2-182">Now select **Model View** on the left.</span></span> 

    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-model-view.png" alt-text="ภาพหน้าจอของไอคอนมุมมองแบบจำลอง":::

1. <span data-ttu-id="3bbd2-184">ลากเขตข้อมูล **วันที่** จากตารางการเงินไปที่เขตข้อมูล **วันที่** ในตารางปฏิทิน เพื่อรวมตารางเข้าด้วยกัน และสร้าง *ความสัมพันธ์* ระหว่างตารางต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-184">Drag the **Date** field from the Financials table to the **Date** field in the Calendar table to join the tables, and create a *relationship* between them.</span></span>  

     :::image type="content" source="media/desktop-excel-stunning-report/power-bi-date-relationship.png" alt-text="ภาพหน้าจอของความสัมพันธ์ระหว่างเขตข้อมูลวันที่":::

## <a name="build-your-report"></a><span data-ttu-id="3bbd2-186">บันทึกรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-186">Build your report</span></span> 

<span data-ttu-id="3bbd2-187">คุณได้แปลงและโหลดข้อมูลของคุณแล้ว ในตอนนี้ก็ถึงเวลาที่จะสร้างรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-187">Now that you've transformed and loaded your data, it's time to create your report.</span></span> <span data-ttu-id="3bbd2-188">ในบานหน้าต่างเขตข้อมูลทางด้านขวา คุณจะเห็นเขตข้อมูลในรูปแบบข้อมูลที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="3bbd2-188">In the Fields pane on the right, you see the fields in the data model you created.</span></span> 

<span data-ttu-id="3bbd2-189">เราจะสร้างรายงานขั้นสุดท้ายพร้อมด้วยวิชวลหนึ่งภาพกัน</span><span class="sxs-lookup"><span data-stu-id="3bbd2-189">Let’s build the final report, one visual at a time.</span></span> 

:::image type="content" source="media/desktop-excel-stunning-report/power-bi-report-by-numbers.png" alt-text="ภาพหน้าจอขององค์ประกอบทั้งหมดของรายงาน ตามตัวเลข":::

### <a name="visual-1-add-a-title"></a><span data-ttu-id="3bbd2-191">วิชวล 1: เพิ่มชื่อเรื่อง</span><span class="sxs-lookup"><span data-stu-id="3bbd2-191">Visual 1: Add a title</span></span> 

1. <span data-ttu-id="3bbd2-192">บนแถบเครื่องมือริบบอน **แทรก** ให้เลือก **กล่องข้อความ**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-192">On the **Insert** ribbon, select **Text Box**.</span></span> <span data-ttu-id="3bbd2-193">พิมพ์ "สรุปสำหรับฝ่ายบริหาร - รายงานการเงิน"</span><span class="sxs-lookup"><span data-stu-id="3bbd2-193">Type “Executive Summary – Finance Report”.</span></span> 
1. <span data-ttu-id="3bbd2-194">เลือกข้อความที่คุณพิมพ์ไว้</span><span class="sxs-lookup"><span data-stu-id="3bbd2-194">Select the text you typed.</span></span> <span data-ttu-id="3bbd2-195">ตั้งค่าขนาดแบบอักษรเป็น 20 และตัวหนา</span><span class="sxs-lookup"><span data-stu-id="3bbd2-195">Set the font size to 20 and bold.</span></span> 

    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-title-executive-summary.png" alt-text="ภาพหน้าจอของชื่อการจัดรูปแบบ":::

1. <span data-ttu-id="3bbd2-197">ในบานหน้าต่างการแสดงภาพ ให้ตั้งค่า **พื้นหลัง** เป็น **ปิด**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-197">In the Visualizations pane, toggle the **Background** to **Off**.</span></span> 
1. <span data-ttu-id="3bbd2-198">ปรับขนาดกล่องให้พอดีกับหนึ่งบรรทัด</span><span class="sxs-lookup"><span data-stu-id="3bbd2-198">Resize the box to fit on one line.</span></span> 

### <a name="visual-2-profit-by-date"></a><span data-ttu-id="3bbd2-199">วิชวล 2: กำไรตามวันที่</span><span class="sxs-lookup"><span data-stu-id="3bbd2-199">Visual 2: Profit by Date</span></span> 

<span data-ttu-id="3bbd2-200">ในตอนนี้ คุณจะต้องสร้างแผนภูมิเส้นเพื่อดูว่าเดือนและปีใดที่มีกำไรสูงสุด</span><span class="sxs-lookup"><span data-stu-id="3bbd2-200">Now, you create a line chart to see which month and year had the highest profit.</span></span> 

1. <span data-ttu-id="3bbd2-201">จากบานหน้าต่างเขตข้อมูล ให้ลากเขตข้อมูล **กำไร** ไปยังที่ว่างบนพื้นที่ทำงานในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-201">From the Fields pane, drag the **Profit** field to a blank area on the report canvas.</span></span> <span data-ttu-id="3bbd2-202">ตามค่าเริ่มต้น Power BI จะแสดงแผนภูมิคอลัมน์ที่มีหนึ่งคอลัมน์เป็นการแสดงผลกำไร</span><span class="sxs-lookup"><span data-stu-id="3bbd2-202">By default, Power BI displays a column chart with one column, Profit.</span></span> 
1. <span data-ttu-id="3bbd2-203">ลากเขตข้อมูล **วันที่** ไปยังวิชวลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="3bbd2-203">Drag the **Date** field to the same visual.</span></span> <span data-ttu-id="3bbd2-204">Power BI อัปเดตแผนภูมิคอลัมน์เพื่อแสดงกำไรตามช่วงเวลาสองปี</span><span class="sxs-lookup"><span data-stu-id="3bbd2-204">Power BI updates the column chart to show profit by the two years.</span></span>

    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-column-year.png" alt-text="ภาพหน้าจอของแผนภูมิคอลัมน์กำไร":::

1. <span data-ttu-id="3bbd2-206">ในส่วน **เขตข้อมูล** ของบานหน้าต่างการแสดงภาพ ให้เลือกรายการแบบหล่นลงในค่า **แกน**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-206">In the **Fields** section of the Visualizations pane, select the drop-down in the **Axis** value.</span></span> <span data-ttu-id="3bbd2-207">เปลี่ยน **วันที่** จาก **ลำดับของวันที่** เป็น **วันที่**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-207">Change **Date** from **Date Hierarchy** to **Date**.</span></span>

    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-date-hierarchy.png" alt-text="ภาพหน้าจอของการเปลี่ยนลำดับของวันที่เป็นวันที่":::

    <span data-ttu-id="3bbd2-209">Power BI อัปเดตแผนภูมิคอลัมน์เพื่อแสดงกำไรตามช่วงเวลาแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="3bbd2-209">Power BI updates the column chart to show profit for each month.</span></span>

    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-column-month.png" alt-text="ภาพหน้าจอของแผนภูมิคอลัมน์ตามกำไร":::

1. <span data-ttu-id="3bbd2-211">ในบานหน้าต่างการการแสดงภาพ ให้เปลี่ยนชนิดการแสดงภาพเป็น **แผนภูมิเส้น**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-211">In the Visualizations pane, change the visualization type to **Line chart**.</span></span> 

    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-profit-date-line-chart.png" alt-text="ภาพหน้าจอของการเปลี่ยนคอลัมน์เป็นแผนภูมิแท่ง":::

    <span data-ttu-id="3bbd2-213">ในตอนนี้ คุณสามารถดูได้อย่างง่ายดายว่าเดือนธันวาคม 2014 มีกำไรมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="3bbd2-213">Now you can easily see that December 2014 had the most profit.</span></span>

### <a name="visual-3-profit-by-country"></a><span data-ttu-id="3bbd2-214">วิชวล 3: กำไรตามประเทศ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-214">Visual 3: Profit by Country</span></span> 

<span data-ttu-id="3bbd2-215">สร้างแผนที่เพื่อดูว่าประเทศใดมีผลกำไรสูงสุด</span><span class="sxs-lookup"><span data-stu-id="3bbd2-215">Create a map to see which country had the highest profits.</span></span>

1. <span data-ttu-id="3bbd2-216">จากบานหน้าต่างเขตข้อมูล ให้ลากเขตข้อมูล **ประเทศ** ไปยังที่ว่างบนพื้นที่ทำงานของรายงานเพื่อสร้างแผนที่</span><span class="sxs-lookup"><span data-stu-id="3bbd2-216">From the Fields pane, drag the **Country** field to a blank area on your report canvas to create a map.</span></span>
1. <span data-ttu-id="3bbd2-217">ลากเขตข้อมูล **กำไร** ไปยังแผนที่</span><span class="sxs-lookup"><span data-stu-id="3bbd2-217">Drag the **Profit** field to the map.</span></span>

    <span data-ttu-id="3bbd2-218">Power BI สร้างภาพแผนที่พร้อมฟองอากาศที่เป็นตัวแทนผลกำไรของแต่ละพื้นที่</span><span class="sxs-lookup"><span data-stu-id="3bbd2-218">Power BI creates a map visual with bubbles representing the relative profit of each location.</span></span> 

    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-map-visual.png" alt-text="ภาพหน้าจอของการสร้างแผนภูมิแผนที่":::

    <span data-ttu-id="3bbd2-220">ดูเหมือนว่ายุโรปจะมีประสิทธิภาพกว่าอเมริกาเหนือ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-220">Europe seems to be performing better than North America.</span></span> 

### <a name="visual-4-sales-by-product-and-segment"></a><span data-ttu-id="3bbd2-221">วิชวล 4: ยอดขายตามผลิตภัณฑ์และเซกเมนต์</span><span class="sxs-lookup"><span data-stu-id="3bbd2-221">Visual 4: Sales by Product and Segment</span></span> 

<span data-ttu-id="3bbd2-222">สร้างแผนภูมิแท่งเพื่อกำหนดว่าบริษัทและเซกเมนต์ใดที่ควรลงทุน</span><span class="sxs-lookup"><span data-stu-id="3bbd2-222">Create a bar chart to determine which companies and segments to invest in.</span></span>

1. <span data-ttu-id="3bbd2-223">ลากสองแผนภูมิที่คุณสร้างไปยังพื้นที่ทำงานครึ่งบนโดยวางไว้ข้าง ๆ กัน</span><span class="sxs-lookup"><span data-stu-id="3bbd2-223">Drag the two charts you've created to be side by side in the top half of the canvas.</span></span> <span data-ttu-id="3bbd2-224">เว้นที่ว่างบางส่วนทางด้านซ้ายของพื้นที่ทำงานไว้</span><span class="sxs-lookup"><span data-stu-id="3bbd2-224">Save some room on the left side of the canvas.</span></span> 
1. <span data-ttu-id="3bbd2-225">เลือกพื้นที่ว่างในพื้นที่ทำงานของรายงานครึ่งล่าง</span><span class="sxs-lookup"><span data-stu-id="3bbd2-225">Select a blank area in the lower half of your report canvas.</span></span> 

1. <span data-ttu-id="3bbd2-226">ในบานหน้าต่างเขตข้อมูล ให้เลือกเขตข้อมูล **ยอดขาย** **ผลิตภัณฑ์** และ **เซกเมนต์**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-226">In the Fields pane, select the **Sales**, **Product**, and **Segment** fields.</span></span> 

    <span data-ttu-id="3bbd2-227">Power BI จะสร้างแผนภูมิคอลัมน์แบบคลัสเตอร์โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-227">Power BI automatically creates a clustered column chart.</span></span> 

1. <span data-ttu-id="3bbd2-228">ลากแผนภูมิ เพื่อปรับให้กว้างพอที่จะเติมที่ว่างด้านล่างแผนภูมิสองรายการด้านบน</span><span class="sxs-lookup"><span data-stu-id="3bbd2-228">Drag the chart so it's wide enough to fill the space under the two upper charts.</span></span>

    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-clustered-column-chart.png" alt-text="ภาพหน้าจอของแผนภูมิคอลัมน์แบบคลัสเตอร์":::

    <span data-ttu-id="3bbd2-230">ดูเหมือนว่าบริษัทควรลงทุนต่อในผลิตภัณฑ์พาซิโอและมุ่งเน้นที่ธุรกิจขนาดเล็กและภาครัฐ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-230">Looks like the company should continue to invest in the Paseo product and target the Small Business and Government segments.</span></span>  

### <a name="visual-5-year-slicer"></a><span data-ttu-id="3bbd2-231">วิชวล 5: ตัวแบ่งส่วนข้อมูลปี</span><span class="sxs-lookup"><span data-stu-id="3bbd2-231">Visual 5: Year slicer</span></span> 

<span data-ttu-id="3bbd2-232">ตัวแบ่งส่วนข้อมูลเป็นเครื่องมือที่มีประโยชน์สำหรับการกรองวิชวลบนหน้ารายงานให้เป็นการเลือกที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="3bbd2-232">Slicers are a valuable tool for filtering the visuals on a report page to a specific selection.</span></span> <span data-ttu-id="3bbd2-233">ในกรณีนี้ เราสามารถสร้างตัวแบ่งส่วนข้อมูลเพื่อปรับผลการทำงานสำหรับแต่ละเดือนและปีให้แคบลงได้</span><span class="sxs-lookup"><span data-stu-id="3bbd2-233">In this case, we can create a slicer to narrow in on performance for each month and year.</span></span>  

1. <span data-ttu-id="3bbd2-234">ในบานหน้าต่างเขตข้อมูล ให้เลือกเขตข้อมูล **วันที่** และลากไปยังพื้นที่ว่างทางด้านซ้ายของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="3bbd2-234">In the Fields pane, select the **Date** field and drag it to the blank area on the left of the canvas.</span></span> 
2. <span data-ttu-id="3bbd2-235">ในบานหน้าต่างการแสดงภาพ เลือก **ตัวแบ่งส่วนข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-235">In the Visualizations pane, choose **Slicer**.</span></span> 
3. <span data-ttu-id="3bbd2-236">ในส่วนเขตข้อมูลของบานหน้าต่างการแสดงภาพ ให้เลือกรายการแบบหล่นลงใน **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-236">In the Fields section of the Visualizations pane, select the drop-down in **Fields**.</span></span> <span data-ttu-id="3bbd2-237">ลบไตรมาสและวันออก เพื่อเก็บไว้แต่ปีและเดือน</span><span class="sxs-lookup"><span data-stu-id="3bbd2-237">Remove Quarter and Day so only Year and Month are left.</span></span> 

    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-date-hierarchy-trim.png" alt-text="ภาพหน้าจอของการเปลี่ยนลำดับของวันที่":::

4. <span data-ttu-id="3bbd2-239">ขยายแต่ละปีและปรับขนาดวิชวล เพื่อให้มองเห็นทุกเดือนได้อย่างชัดเจน</span><span class="sxs-lookup"><span data-stu-id="3bbd2-239">Expand each year and resize the visual, so all months are visible.</span></span>

    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-hierarchy-date-slicer.png" alt-text="ภาพหน้าจอของตัวแบ่งส่วนข้อมูลลำดับของวันที่":::

<span data-ttu-id="3bbd2-241">หากตอนนี้ผู้จัดการของคุณขอดูเฉพาะข้อมูลในปี 2013 คุณสามารถใช้ตัวแบ่งส่วนข้อมูลเพื่อสลับระหว่างปีต่าง ๆ หรือเดือนที่เฉพาะเจาะจงของแต่ละปีได้</span><span class="sxs-lookup"><span data-stu-id="3bbd2-241">Now if your manager asks to see just 2013 data, you can use the slicer to switch between years, or specific months of each year.</span></span> 

### <a name="extra-credit-format-the-report"></a><span data-ttu-id="3bbd2-242">เครดิตเพิ่มเติม: จัดรูปแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="3bbd2-242">Extra credit: Format the report</span></span>

<span data-ttu-id="3bbd2-243">หากคุณต้องการจัดรูปแบบแสงบนรายงานนี้เพื่อเพิ่มการปรับแต่งมากขึ้น นี่คือขั้นตอนง่าย ๆ:</span><span class="sxs-lookup"><span data-stu-id="3bbd2-243">If you want to do some light formatting on this report to add more polish, here are a few easy steps.</span></span> 

<span data-ttu-id="3bbd2-244">**ธีม**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-244">**Theme**</span></span>

- <span data-ttu-id="3bbd2-245">บนแถบเครื่องมือริบบอน **มุมมอง** ให้เปลี่ยนธีมเป็น **ฝ่ายบริหาร**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-245">On the **View** ribbon, change the theme to **Executive**.</span></span>  

    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-theme-executive.png" alt-text="ภาพหน้าจอของการเลือกธีมฝ่ายบริหาร"::: 

<span data-ttu-id="3bbd2-247">**จัดการแสดงภาพให้เป็นระเบียบ**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-247">**Spruce up the visuals**</span></span> 

<span data-ttu-id="3bbd2-248">ทำการเปลี่ยนแปลงต่อไปนี้บนแท็บ **จัดรูปแบบ** ในบานหน้าต่างการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-248">Make the following changes on the **Format** tab in the Visualizations pane.</span></span>

:::image type="content" source="media/desktop-excel-stunning-report/power-bi-format-tab-visualizations.png" alt-text="ภาพหน้าจอของแท็บจัดรูปแบบในบานหน้าต่างการแสดงภาพ":::

1. <span data-ttu-id="3bbd2-250">เลือกวิชวล 2</span><span class="sxs-lookup"><span data-stu-id="3bbd2-250">Select Visual 2.</span></span> <span data-ttu-id="3bbd2-251">ในส่วน **ชื่อเรื่อง** ให้เปลี่ยน **ข้อความชื่อเรื่อง** เป็น “กำไรตามเดือนและปี” และเปลี่ยน **ขนาดข้อความ** เป็น **16 pt**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-251">In the **Title** section, change **Title text** to “Profit by Month and Year” and **Text size** to **16 pt**.</span></span> <span data-ttu-id="3bbd2-252">ตั้งค่า **เงา** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-252">Toggle **Shadow** to **On**.</span></span> 

1. <span data-ttu-id="3bbd2-253">เลือกวิชวล 3</span><span class="sxs-lookup"><span data-stu-id="3bbd2-253">Select Visual 3.</span></span> <span data-ttu-id="3bbd2-254">ในส่วน **ลักษณะแผนที่** ให้เปลี่ยน **ธีม** เป็น **โทนสีเทา**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-254">In the **Map styles** section, change **Theme** to **Grayscale**.</span></span> <span data-ttu-id="3bbd2-255">ในส่วน **ชื่อเรื่อง** ให้เปลี่ยน **ขนาดข้อความ** ของชื่อเรื่องเป็น **16 pt**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-255">In the **Title** section, change title **Text size** to **16 pt**.</span></span> <span data-ttu-id="3bbd2-256">ตั้งค่า **เงา** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-256">Toggle **Shadow** to **On**.</span></span>

1. <span data-ttu-id="3bbd2-257">เลือกวิชวล 4</span><span class="sxs-lookup"><span data-stu-id="3bbd2-257">Select Visual 4.</span></span> <span data-ttu-id="3bbd2-258">ในส่วน **ชื่อเรื่อง** ให้เปลี่ยน **ขนาดข้อความ** ของชื่อเรื่องเป็น **16 pt**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-258">In the **Title** section, change title **Text size** to **16 pt**.</span></span> <span data-ttu-id="3bbd2-259">ตั้งค่า **เงา** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-259">Toggle **Shadow** to **On**.</span></span>

1. <span data-ttu-id="3bbd2-260">เลือกวิชวล 5</span><span class="sxs-lookup"><span data-stu-id="3bbd2-260">Select Visual 5.</span></span> <span data-ttu-id="3bbd2-261">ในส่วน **ตัวควบคุมการเลือก** ให้ตั้งค่า **แสดงตัวเลือก “เลือกทั้งหมด”** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-261">In the **Selection controls** section, toggle **Show "Select all" option** to **On**.</span></span> <span data-ttu-id="3bbd2-262">ในส่วน **ส่วนหัวของตัวแบ่งส่วนข้อมูล** เพิ่ม **ขนาดข้อความ** เป็น **16 pt**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-262">In the **Slicer header** section, increase **Text size** to **16 pt**.</span></span> 

<span data-ttu-id="3bbd2-263">**เพิ่มรูปร่างพื้นหลังสำหรับชื่อเรื่อง**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-263">**Add a background shape for the title**</span></span>

1. <span data-ttu-id="3bbd2-264">บนแถบเครื่องมือริบบอน **แทรก** ให้เลือก **รูปร่าง** > **สี่เหลี่ยมผืนผ้า**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-264">On the **Insert** ribbon, select **Shapes** > **Rectangle**.</span></span> <span data-ttu-id="3bbd2-265">วางไว้ที่ด้านบนของหน้า และขยายความกว้างตามหน้าและความสูงตามชื่อเรื่อง</span><span class="sxs-lookup"><span data-stu-id="3bbd2-265">Place it at the top of the page, and stretch it to be the width of the page and height of the title.</span></span> 
1. <span data-ttu-id="3bbd2-266">ในบานหน้าต่าง **จัดรูปแบบรูปร่าง** ในส่วน **เส้น** ให้เปลี่ยน **ความโปร่งใส** เป็น **100%**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-266">In the **Format shape** pane, in the **Line** section, change **Transparency** to **100%**.</span></span> 
1. <span data-ttu-id="3bbd2-267">ในส่วน **เติม** ให้เปลี่ยน **เติมสี** เป็น **ธีมสี 5 #6B91C9** (น้ำเงิน)</span><span class="sxs-lookup"><span data-stu-id="3bbd2-267">In the **Fill** section, change **Fill color** to **Theme color 5 #6B91C9** (blue).</span></span> 

    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-theme-color-5.png" alt-text="ภาพหน้าจอของธีมสี 5":::

1. <span data-ttu-id="3bbd2-269">บนแท็บ **จัดรูปแบบ** ให้เลือก **ส่งไปข้างหลัง** > **ส่งไปด้านหลัง**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-269">On the **Format** tab, select **Send backward** > **Send to back**.</span></span> 
1. <span data-ttu-id="3bbd2-270">เลือกข้อความในวิชวล 1, ชื่อเรื่อง และเปลี่ยนสีแบบอักษรเป็น **สีขาว**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-270">Select the text in Visual 1, the title, and change the font color to **White**.</span></span> 

<span data-ttu-id="3bbd2-271">**เพิ่มรูปร่างพื้นหลังสำหรับวิชวล 2 และ 3**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-271">**Add a background shape for visuals 2 and 3**</span></span>

1. <span data-ttu-id="3bbd2-272">บนแถบเครื่องมือริบบอน **แทรก** ให้เลือก **รูปร่าง** > **สี่เหลี่ยมผืนผ้า** และขยายความกว้างและความสูงของรูปร่างให้พอดีกับวิชวล 2 และ 3</span><span class="sxs-lookup"><span data-stu-id="3bbd2-272">On the **Insert** ribbon, select **Shapes** > **Rectangle**, and stretch it the be the width and height of Visuals 2 and 3.</span></span> 
1. <span data-ttu-id="3bbd2-273">ในบานหน้าต่าง **จัดรูปแบบรูปร่าง** ในส่วน **เส้น** ให้เปลี่ยน **ความโปร่งใส** เป็น **100%**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-273">In the **Format shape** pane, in the **Line** section, change **Transparency** to **100%**.</span></span> 
1. <span data-ttu-id="3bbd2-274">บนแท็บ **จัดรูปแบบ** ให้เลือก **ส่งไปข้างหลัง** > **ส่งไปด้านหลัง**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-274">On the **Format** tab, select **Send backward** > **Send to back**.</span></span> 

### <a name="finished-report"></a><span data-ttu-id="3bbd2-275">รายงานที่เสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="3bbd2-275">Finished report</span></span>

<span data-ttu-id="3bbd2-276">รายงานที่ปรับแต่งขั้นสุดท้ายเสร็จแล้วของคุณมีลักษณะเช่นนี้</span><span class="sxs-lookup"><span data-stu-id="3bbd2-276">Here's how your final polished report will look:</span></span>  

:::image type="content" source="media/desktop-excel-stunning-report/power-bi-excel-formatted-report.png" alt-text="ภาพหน้าจอของรายงานที่จัดรูปแบบขั้นสุดท้ายแล้ว":::

<span data-ttu-id="3bbd2-278">โดยสรุปแล้วรายงานนี้สามารถตอบคำถามที่ผู้จัดการของคุณอยากรู้มากที่สุดได้:</span><span class="sxs-lookup"><span data-stu-id="3bbd2-278">In summary, this report answers your manager’s top questions:</span></span> 

- <span data-ttu-id="3bbd2-279">เดือนและปีใดที่มีผลกำไรมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="3bbd2-279">Which month and year had the most profit?</span></span> 

    <span data-ttu-id="3bbd2-280">ธันวาคม 2014</span><span class="sxs-lookup"><span data-stu-id="3bbd2-280">December 2014</span></span> 

- <span data-ttu-id="3bbd2-281">บริษัทเห็นความสำเร็จมากที่สุดจากประเทศใด</span><span class="sxs-lookup"><span data-stu-id="3bbd2-281">Which country is the company seeing the most success in?</span></span> 

    <span data-ttu-id="3bbd2-282">ในยุโรป โดยเฉพาะฝรั่งเศสและเยอรมนี</span><span class="sxs-lookup"><span data-stu-id="3bbd2-282">In Europe, specifically France and Germany.</span></span> 

- <span data-ttu-id="3bbd2-283">ผลิตภัณฑ์และเซกเมนต์ใดที่บริษัทควรลงทุนต่อ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-283">Which product and segment should the company continue to invest in?</span></span> 

    <span data-ttu-id="3bbd2-284">บริษัทควรลงทุนต่อในผลิตภัณฑ์พาซิโอและมุ่งเน้นที่ธุรกิจขนาดเล็กและภาครัฐ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-284">The company should continue to invest in the Paseo product and target the Small Business and Government segments.</span></span> 

## <a name="save-your-report"></a><span data-ttu-id="3bbd2-285">บันทึกรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-285">Save your report</span></span>

- <span data-ttu-id="3bbd2-286">จากเมนู **ไฟล์** ให้เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-286">On the **File** menu, select **Save**.</span></span>

## <a name="publish-to-the-power-bi-service-to-share"></a><span data-ttu-id="3bbd2-287">เผยแพร่ไปยังบริการของ Power BI เพื่อแชร์</span><span class="sxs-lookup"><span data-stu-id="3bbd2-287">Publish to the Power BI service to share</span></span> 

<span data-ttu-id="3bbd2-288">หากต้องการแชร์รายงานของคุณกับผู้จัดการและเพื่อนร่วมงาน ให้เผยแพร่รายงานดังกล่าวไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="3bbd2-288">To share your report with your manager and colleagues, publish it to the Power BI service.</span></span> <span data-ttu-id="3bbd2-289">เมื่อคุณแชร์กับเพื่อนร่วมงานที่มีบัญชี Power BI พวกเขาสามารถโต้ตอบกับรายงานของคุณแต่ไม่สามารถบันทึกการเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="3bbd2-289">When you share with colleagues that have a Power BI account, they can interact with your report, but can’t save changes.</span></span> 

1. <span data-ttu-id="3bbd2-290">เลือก **เผยแพร่** บนแถบเครื่องมือริบบอน **หน้าหลัก** ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3bbd2-290">In Power BI Desktop, select **Publish** on the **Home** ribbon.</span></span> 

    <span data-ttu-id="3bbd2-291">คุณอาจต้องลงชื่อเข้าใช้บริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="3bbd2-291">You may need to sign in to the Power BI service.</span></span> <span data-ttu-id="3bbd2-292">หากคุณยังไม่มีบัญชีผู้ใช้ คุณสามารถ[ลงทะเบียนสำหรับรุ่นทดลองใช้ฟรี](https://app.powerbi.com/signupredirect?pbi_source=web)ได้</span><span class="sxs-lookup"><span data-stu-id="3bbd2-292">If you don't have an account yet, you can [sign up for a free trial](https://app.powerbi.com/signupredirect?pbi_source=web).</span></span>

1. <span data-ttu-id="3bbd2-293">เลือกปลายทาง เช่น **พื้นที่ทำงานของฉัน** ในบริการของ Power BI > **เลือก**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-293">Select a destination such as **My workspace** in the Power BI service > **Select**.</span></span>
1. <span data-ttu-id="3bbd2-294">เลือก **เปิด 'ชื่อไฟล์ของคุณ' ใน Power BI**</span><span class="sxs-lookup"><span data-stu-id="3bbd2-294">Select **Open 'your-file-name' in Power BI**.</span></span>

    :::image type="content" source="media/desktop-excel-stunning-report/open-power-bi.png" alt-text="ภาพหน้าจอของการเปิดรายงานของคุณในบริการของ Power BI":::

    <span data-ttu-id="3bbd2-296">รายงานที่เสร็จสมบูรณ์ของคุณเปิดขึ้นในเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="3bbd2-296">Your completed report opens in the browser.</span></span>

    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-excel-report-service.png" alt-text="สกรีนช็อตของรายงาน Power BI ที่เสร็จสมบูรณ์ของคุณในบริการ Power BI"::: 

1. <span data-ttu-id="3bbd2-298">เลือก **แชร์** ที่ด้านบนของรายงานเพื่อแชร์รายงานของคุณกับบุคคลอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="3bbd2-298">Select **Share** at the top of the report to share your report with others.</span></span>

    :::image type="content" source="media/desktop-excel-stunning-report/power-bi-share-report.png" alt-text="ภาพหน้าจอของการแชร์รายงานของคุณจากบริการของ Power BI":::

## <a name="next-steps"></a><span data-ttu-id="3bbd2-300">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3bbd2-300">Next steps</span></span>

- [<span data-ttu-id="3bbd2-301">บทช่วยสอน: วิเคราะห์ข้อมูลยอดขายจาก Excel และตัวดึงข้อมูล OData</span><span class="sxs-lookup"><span data-stu-id="3bbd2-301">Tutorial: Analyze sales data from Excel and an OData feed</span></span>](../connect-data/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed.md)

<span data-ttu-id="3bbd2-302">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3bbd2-302">More questions?</span></span> <span data-ttu-id="3bbd2-303">[ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="3bbd2-303">[Try the Power BI Community](https://community.powerbi.com/).</span></span>
