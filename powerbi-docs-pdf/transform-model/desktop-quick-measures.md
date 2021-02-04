---
title: ใช้การวัดผลด่วนสำหรับการคำนวณทั่วไปและมีประสิทธิภาพ
description: การวัดผลด่วนมีสูตร DAX สำเร็จรูปที่ช่วยให้การคำนวณทั่วไปสามารถทำได้อย่างรวดเร็ว
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: how-to
ms.date: 11/22/2019
LocalizationGroup: Create reports
ms.openlocfilehash: 77f15cb0fcb92a895c92bd93d8fa18896dafc7f8
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413897"
---
# <a name="use-quick-measures-for-common-calculations"></a><span data-ttu-id="e2df5-103">ใช้การวัดผลด่วนสำหรับการคำนวณทั่วไป</span><span class="sxs-lookup"><span data-stu-id="e2df5-103">Use quick measures for common calculations</span></span>
<span data-ttu-id="e2df5-104">คุณสามารถใช้ *การวัดผลด่วน* สำหรับการคำนวณทั่วไปและมีประสิทธิภาพได้อย่างรวดเร็วและง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="e2df5-104">You can use *quick measures* to quickly and easily perform common, powerful calculations.</span></span> <span data-ttu-id="e2df5-105">การวัดผลด่วนเรียกใช้ชุดของคำสั่งนิพจน์การวิเคราะห์ข้อมูล (DAX) ที่อยู่เบื้องหลังฉากดังกล่าว จากนั้นแสดงผลลัพธ์ให้แก่คุณในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="e2df5-105">A quick measure runs a set of Data Analysis Expressions (DAX) commands behind the scenes, then presents the results for you to use in your report.</span></span> <span data-ttu-id="e2df5-106">คุณไม่จำเป็นต้องเขียน DAX ซึ่งจะทำให้คุณยึดตามข้อมูลที่คุณใส่ไว้ในกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="e2df5-106">You don't have to write the DAX, it's done for you based on input you provide in a dialog box.</span></span> <span data-ttu-id="e2df5-107">มีการคำนวนอยู่มากมายหลายประเภท และวิธีการปรับเปลี่ยนแต่ละการคำนวณให้ตรงกับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="e2df5-107">There are many available categories of calculations and ways to modify each calculation to fit your needs.</span></span> <span data-ttu-id="e2df5-108">ยิ่งไปกว่านั้น คุณสามารถดู DAX ที่ดำเนินการโดยการวัดผลด่วน และเริ่มต้นหรือขยายความรู้ DAX ของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="e2df5-108">Perhaps best of all, you can see the DAX that's executed by the quick measure and jump-start or expand your own DAX knowledge.</span></span>

## <a name="create-a-quick-measure"></a><span data-ttu-id="e2df5-109">สร้างการวัดผลด่วน</span><span class="sxs-lookup"><span data-stu-id="e2df5-109">Create a quick measure</span></span>

<span data-ttu-id="e2df5-110">หากต้องการสร้างการวัดผลด่วนใน Power BI Desktop ให้คลิกขวาหรือเลือกจุดไข่ปลา **...** ที่อยู่ถัดจากรายการใด ๆ ในบานหน้าต่าง **เขตข้อมูล** และเลือก **การวัดผลวัดด่วนใหม่** จากเมนูที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="e2df5-110">To create a quick measure in Power BI Desktop, right-click or select the ellipsis **...** next to any item in the **Fields** pane, and select **New quick measure** from the menu that appears.</span></span> 

![เลือกการวัดผลด่วนใหม่](media/desktop-quick-measures/quick-measures_01.png)

<span data-ttu-id="e2df5-112">คุณยังสามารถคลิกขวาหรือเลือกลูกศรดรอปดาวน์ที่อยู่ถัดจากค่าใด ๆ ใน **ค่า** ที่เหมาะสำหรับวิชวลที่มีอยู่ และเลือก **การวัดผลด่วนใหม่** จากเมนู</span><span class="sxs-lookup"><span data-stu-id="e2df5-112">You can also right-click or select the drop-down arrow next to any value in the **Values** well for an existing visual, and select **New quick measure** from the menu.</span></span> 

<span data-ttu-id="e2df5-113">เมื่อคุณเลือก **การวัดผลด่วนใหม่** หน้าต่าง **การวัดผลด่วน** จะปรากฏขึ้น ให้คุณเลือกการคำนวณที่คุณต้องการและเขตข้อมูลเพื่อเรียกใช้การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="e2df5-113">When you select **New quick measure**, the **Quick measures** window appears, letting you select the calculation you want and the fields to run the calculation against.</span></span> 

<span data-ttu-id="e2df5-114">เลือกเขตข้อมูล **เลือกการคำนวณ** เพื่อดูรายการของการวัดผลด่วนที่พร้อมใช้งานแบบยาว</span><span class="sxs-lookup"><span data-stu-id="e2df5-114">Select the **Select a calculation** field to see a long list of available quick measures.</span></span> 

![การคำนวณการวัดผลด่วนที่พร้อมใช้งาน](media/desktop-quick-measures/quick-measures_04.png)

<span data-ttu-id="e2df5-116">การวัดผลด่วนห้าชนิดที่มีการคำนวณของตนเองคือ:</span><span class="sxs-lookup"><span data-stu-id="e2df5-116">The five quick measure calculation types, with their calculations, are:</span></span>

* <span data-ttu-id="e2df5-117">**ค่ารวมตามประเภท**</span><span class="sxs-lookup"><span data-stu-id="e2df5-117">**Aggregate per category**</span></span>
  * <span data-ttu-id="e2df5-118">เฉลี่ยตามหมวดหมู่</span><span class="sxs-lookup"><span data-stu-id="e2df5-118">Average per category</span></span>
  * <span data-ttu-id="e2df5-119">ค่าความแปรปรวนตามประเภท</span><span class="sxs-lookup"><span data-stu-id="e2df5-119">Variance per category</span></span>
  * <span data-ttu-id="e2df5-120">สูงสุดตามหมวดหมู่</span><span class="sxs-lookup"><span data-stu-id="e2df5-120">Max per category</span></span>
  * <span data-ttu-id="e2df5-121">ต่ำสุดตามหมวดหมู่</span><span class="sxs-lookup"><span data-stu-id="e2df5-121">Min per category</span></span>
  * <span data-ttu-id="e2df5-122">ค่าเฉลี่ยถ่วงน้ำหนักตามหมวดหมู่</span><span class="sxs-lookup"><span data-stu-id="e2df5-122">Weighted average per category</span></span>
* <span data-ttu-id="e2df5-123">**ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="e2df5-123">**Filters**</span></span>
  * <span data-ttu-id="e2df5-124">ค่าที่กรองแล้ว</span><span class="sxs-lookup"><span data-stu-id="e2df5-124">Filtered value</span></span>
  * <span data-ttu-id="e2df5-125">ส่วนต่างจากค่าที่กรอง</span><span class="sxs-lookup"><span data-stu-id="e2df5-125">Difference from filtered value</span></span>
  * <span data-ttu-id="e2df5-126">เปอร์เซ็นต์ส่วนต่างจากค่าที่กรองแล้ว</span><span class="sxs-lookup"><span data-stu-id="e2df5-126">Percentage difference from filtered value</span></span>
  * <span data-ttu-id="e2df5-127">ยอดขายจากลูกค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="e2df5-127">Sales from new customers</span></span>
* <span data-ttu-id="e2df5-128">**ตัวแสดงเวลา**</span><span class="sxs-lookup"><span data-stu-id="e2df5-128">**Time intelligence**</span></span>
  * <span data-ttu-id="e2df5-129">ผลรวมตั้งแต่ต้นปีจนถึงปัจจุบัน (YTD)</span><span class="sxs-lookup"><span data-stu-id="e2df5-129">Year-to-date total</span></span>
  * <span data-ttu-id="e2df5-130">ผลรวมตั้งแต่ต้นไตรมาสจนถึงปัจจุบัน (QTD)</span><span class="sxs-lookup"><span data-stu-id="e2df5-130">Quarter-to-date total</span></span>
  * <span data-ttu-id="e2df5-131">ผลรวมตั้งแต่ต้นเดือนจนถึงปัจจุบัน (MTD)</span><span class="sxs-lookup"><span data-stu-id="e2df5-131">Month-to-date total</span></span>
  * <span data-ttu-id="e2df5-132">การเปลี่ยนแปลงเมื่อเทียบปีปัจจุบันกับปีที่ผ่านมา (YoY)</span><span class="sxs-lookup"><span data-stu-id="e2df5-132">Year-over-year change</span></span>
  * <span data-ttu-id="e2df5-133">การเปลี่ยนแปลงเมื่อเทียบไตรมาสปัจจุบันกับไตรมาสที่ผ่านมา (QoQ)</span><span class="sxs-lookup"><span data-stu-id="e2df5-133">Quarter-over-quarter change</span></span>
  * <span data-ttu-id="e2df5-134">การเปลี่ยนแปลงเมื่อเทียบเดือนปัจจุบันกับเดือนที่ผ่านมา (MoM)</span><span class="sxs-lookup"><span data-stu-id="e2df5-134">Month-over-month change</span></span>
  * <span data-ttu-id="e2df5-135">ค่าเฉลี่ยเคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="e2df5-135">Rolling average</span></span>
* <span data-ttu-id="e2df5-136">**ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="e2df5-136">**Totals**</span></span>
  * <span data-ttu-id="e2df5-137">การรันทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e2df5-137">Running total</span></span>
  * <span data-ttu-id="e2df5-138">ยอดรวมของประเภท (ใช้ตัวกรอง)</span><span class="sxs-lookup"><span data-stu-id="e2df5-138">Total for category (filters applied)</span></span>
  * <span data-ttu-id="e2df5-139">ยอดรวมของประเภท (ไม่ใช้ตัวกรอง)</span><span class="sxs-lookup"><span data-stu-id="e2df5-139">Total for category (filters not applied)</span></span>
* <span data-ttu-id="e2df5-140">**การดำเนินการทางคณิตศาสตร์**</span><span class="sxs-lookup"><span data-stu-id="e2df5-140">**Mathematical operations**</span></span>
  * <span data-ttu-id="e2df5-141">การบวก</span><span class="sxs-lookup"><span data-stu-id="e2df5-141">Addition</span></span>
  * <span data-ttu-id="e2df5-142">การลบ</span><span class="sxs-lookup"><span data-stu-id="e2df5-142">Subtraction</span></span>
  * <span data-ttu-id="e2df5-143">การคูณ</span><span class="sxs-lookup"><span data-stu-id="e2df5-143">Multiplication</span></span>
  * <span data-ttu-id="e2df5-144">การหาร</span><span class="sxs-lookup"><span data-stu-id="e2df5-144">Division</span></span>
  * <span data-ttu-id="e2df5-145">เปอร์เซ็นต์ผลต่าง</span><span class="sxs-lookup"><span data-stu-id="e2df5-145">Percentage difference</span></span>
  * <span data-ttu-id="e2df5-146">สัมประสิทธิ์สหสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="e2df5-146">Correlation coefficient</span></span>
* <span data-ttu-id="e2df5-147">**ข้อความ**</span><span class="sxs-lookup"><span data-stu-id="e2df5-147">**Text**</span></span>
  * <span data-ttu-id="e2df5-148">การจัดอันดับด้วยดาว</span><span class="sxs-lookup"><span data-stu-id="e2df5-148">Star rating</span></span>
  * <span data-ttu-id="e2df5-149">รายการค่าแบบเชื่อมเข้าด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="e2df5-149">Concatenated list of values</span></span>

<span data-ttu-id="e2df5-150">หากต้องการส่งแนวคิดของคุณเกี่ยวกับการวัดผลด่วนใหม่ที่คุณต้องการดู สูตร DAX ต้นแบบหรือแนวคิดการวัดผลด่วนอื่น ๆ เพื่อพิจารณา โปรดดูที่ตอนท้ายของบทความนี้</span><span class="sxs-lookup"><span data-stu-id="e2df5-150">To submit your ideas about new quick measures you'd like to see, underlying DAX formulas, or other quick measures ideas for consideration, see the end of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="e2df5-151">เมื่อใช้การเชื่อมต่อสดของ SQL Server Analysis Services (SSAS) มีการวัดผลด่วนให้ใช้งานบางตัว</span><span class="sxs-lookup"><span data-stu-id="e2df5-151">When using SQL Server Analysis Services (SSAS) live connections, some quick measures are available.</span></span> <span data-ttu-id="e2df5-152">Power BI Desktop จะแสดงเฉพาะชุดของการวัดผลด่วนที่ได้รับการสนับสนุนสำหรับรุ่นของ SSAS ที่คุณกำลังเชื่อมต่อไปยัง</span><span class="sxs-lookup"><span data-stu-id="e2df5-152">Power BI Desktop displays only the quick measures that are supported for the version of SSAS you're connecting to.</span></span> <span data-ttu-id="e2df5-153">ถ้าคุณเชื่อมต่อกับแหล่งข้อมูลสด SSAS และคุณไม่เห็นการวัดผลด่วนบางตัวในรายการ อาจเป็นเพราะเวอร์ชัน SSAS ที่คุณเชื่อมต่อไม่สนับสนุนคำสั่ง DAX ที่ใช้โดยการวัดผลด่วนเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="e2df5-153">If you're connected to a SSAS live data source and don't see certain quick measures in the list, it's because the SSAS version you're connected to doesn't support the DAX commands used to implement those quick measures.</span></span>

<span data-ttu-id="e2df5-154">หลังจากเลือกการคำนวณและเขตข้อมูลที่คุณต้องการสำหรับการวัดผลด่วน เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e2df5-154">After you select the calculations and fields you want for your quick measure, select **OK**.</span></span> <span data-ttu-id="e2df5-155">การวัดผลด่วนใหม่จะปรากฎในบานหน้าต่าง **เขตข้อมูล** และสูตร DAX ต้นแบบจะปรากฎในแถบสูตร</span><span class="sxs-lookup"><span data-stu-id="e2df5-155">The new quick measure appears in the **Fields** pane, and the underlying DAX formula appears in the formula bar.</span></span> 

## <a name="quick-measure-example"></a><span data-ttu-id="e2df5-156">ตัวอย่างการวัดผลด่วน</span><span class="sxs-lookup"><span data-stu-id="e2df5-156">Quick measure example</span></span>
<span data-ttu-id="e2df5-157">ลองมาดูที่การวัดผลด่วนในการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="e2df5-157">Let's take a look at a quick measure in action.</span></span>

<span data-ttu-id="e2df5-158">วิชวลเมทริกซ์ต่อไปนี้แสดงตารางยอดขายสำหรับผลิตภัณฑ์ต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="e2df5-158">The following matrix visual shows a sales table for various products.</span></span> <span data-ttu-id="e2df5-159">ตารางนี้เป็นตารางพื้นฐานที่มีผลรวมยอดขายสำหรับผลิตภัณฑ์แต่ละประเภท</span><span class="sxs-lookup"><span data-stu-id="e2df5-159">It's a basic table that includes the sales totals for each category.</span></span>

![วิชวลเมทริกซ์ที่แสดงตารางยอดขาย](media/desktop-quick-measures/quick-measures_05.png)

<span data-ttu-id="e2df5-161">ด้วยวิชวลเมทริกซ์ที่เลือกไว้ เลือกลูกศรดรอปดาวน์ที่อยู่ถัดจาก **TotalSales** ใน **ค่า** และเลือก **การวัดผลด่วนใหม่**</span><span class="sxs-lookup"><span data-stu-id="e2df5-161">With the matrix visual selected, select the drop-down arrow next to **TotalSales** in the **Values** well, and select **New quick measure**.</span></span> 

<span data-ttu-id="e2df5-162">ในหน้าต่าง **การวัดผลด่วน** ภายใต้ **การคำนวณ** ให้เลือก **ค่าเฉลี่ยต่อประเภท**</span><span class="sxs-lookup"><span data-stu-id="e2df5-162">In the **Quick measures** window, under **Calculation**, select **Average per category**.</span></span> 

<span data-ttu-id="e2df5-163">ลาก **ราคาต่อหน่วยโดยเฉลี่ย** จากบานหน้าต่าง **เขตข้อมูล** ไปยังเขตข้อมูล **ค่าฐาน**</span><span class="sxs-lookup"><span data-stu-id="e2df5-163">Drag **Average Unit Price** from the **Fields** pane into the **Base value** field.</span></span> <span data-ttu-id="e2df5-164">เว้น **ประเภท** ในเขตข้อมูล **ประเภท** และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e2df5-164">Leave **Category** in the **Category** field, and select **OK**.</span></span> 

![ภาพหน้าจอของ Power B I Desktop ที่แสดงตัวเลือกตัวกรองในบานหน้าต่างเขตข้อมูล](media/desktop-quick-measures/quick-measures_06.png)

<span data-ttu-id="e2df5-166">เมื่อคุณเลือก **ตกลง** มีสิ่งที่น่าสนใจหลายอย่างเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="e2df5-166">When you select **OK**, several interesting things happen.</span></span>

![การวัดผลด่วนใหม่ในรายการวิชวล แถบสูตร และเขตข้อมูล](media/desktop-quick-measures/quick-measures_07.png)

1. <span data-ttu-id="e2df5-168">วิชวลเมทริกซ์มีคอลัมน์ใหม่ที่แสดง **ค่าเฉลี่ยของราคาต่อหน่วยเฉลี่ยตามประเภท** จากการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="e2df5-168">The matrix visual has a new column that shows the calculated **Average Unit Price average per Category**.</span></span>
   
2. <span data-ttu-id="e2df5-169">สูตร DAX สำหรับการวัดผลด่วนใหม่จะปรากฏขึ้นในแถบสูตร</span><span class="sxs-lookup"><span data-stu-id="e2df5-169">The DAX formula for the new quick measure appears in the formula bar.</span></span> <span data-ttu-id="e2df5-170">ดู[ส่วนถัดไป](#learn-dax-by-using-quick-measures)สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสูตร DAX</span><span class="sxs-lookup"><span data-stu-id="e2df5-170">See the [next section](#learn-dax-by-using-quick-measures) for more about the DAX formula.</span></span>
   
3. <span data-ttu-id="e2df5-171">การวัดผลด่วนใหม่จะปรากฏขึ้นตามที่เลือกและเน้นในบานหน้าต่าง **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="e2df5-171">The new quick measure appears selected and highlighted in the **Fields** pane.</span></span> 

<span data-ttu-id="e2df5-172">การวัดผลด่วนใหม่จะพร้อมใช้งานสำหรับวิชวลใด ๆ ในรายงาน ไม่ใช่เฉพาะวิชวลที่คุณสร้างขึ้นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e2df5-172">The new quick measure is available to any visual in the report, not just the visual you created it for.</span></span> <span data-ttu-id="e2df5-173">รูปภาพต่อไปนี้แสดงวิชวลแผนภูมิคอลัมน์ด่วนที่สร้างขึ้นโดยใช้เขตข้อมูลการวัดผลด่วนใหม่</span><span class="sxs-lookup"><span data-stu-id="e2df5-173">The following image shows a quick column chart visual created by using the new quick measure field.</span></span>

![วิชวลแผนภูมิแท่งใหม่ที่ยึดตามเขตข้อมูลการวัดผลด่วน](media/desktop-quick-measures/quick-measures_09.png)

## <a name="learn-dax-by-using-quick-measures"></a><span data-ttu-id="e2df5-175">เรียนรู้ DAX โดยใช้การวัดผลด่วน</span><span class="sxs-lookup"><span data-stu-id="e2df5-175">Learn DAX by using quick measures</span></span>
<span data-ttu-id="e2df5-176">ข้อได้เปรียบอย่างมากของการวัดผลด่วนคือการแสดงสูตร DAX ที่ใช้หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="e2df5-176">A great advantage of quick measures is that they show you the DAX formula that implements the measure.</span></span> <span data-ttu-id="e2df5-177">เมื่อคุณเลือกการวัดผลด่วนในบานหน้าต่าง **เขตข้อมูล** **แถบสูตร** จะปรากฏขึ้น โดยแสดงสูตร DAX ที่ Power BI สร้างขึ้นเพื่อใช้หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="e2df5-177">When you select a quick measure in the **Fields** pane, the **Formula bar** appears, showing the DAX formula that Power BI created to implement the measure.</span></span>

![สูตรการวัดผลด่วนในแถบสูตร](media/desktop-quick-measures/quick-measures_10.png)

<span data-ttu-id="e2df5-179">แถบสูตรไม่ได้แสดงเฉพาะสูตรที่อยู่เบื้องหลังหน่วยวัดเท่านั้น แต่อาจมีความสำคัญมากขึ้น โดยช่วยให้คุณเห็นวิธีการสร้างการวัดผลด่วนต้นแบบของสูตร DAX</span><span class="sxs-lookup"><span data-stu-id="e2df5-179">The formula bar not only shows you the formula behind the measure, but perhaps more importantly, lets you see how to create the DAX formulas underlying quick measures.</span></span>

<span data-ttu-id="e2df5-180">สมมติว่าคุณต้องคำนวณการเปลี่ยนแปลงปีต่อปี แต่คุณไม่แน่ใจว่าจะจัดโครงสร้างสูตร DAX อย่างไร หรือคุณยังไม่รู้ว่าจะเริ่มต้นอย่างไร</span><span class="sxs-lookup"><span data-stu-id="e2df5-180">Imagine you need to do a year-over-year calculation, but you're not sure how to structure the DAX formula, or you have no idea where to start.</span></span> <span data-ttu-id="e2df5-181">คุณสามารถสร้างการวัดผลด่วนโดยใช้การคำนวณ **การเปลี่ยนแปลงเมื่อเทียบปีปัจจุบันกับปีที่ผ่านมา** และดูว่าวิธีการที่จะปรากฏในวิชวลของคุณ และวิธีการทำงานของสูตร DAX</span><span class="sxs-lookup"><span data-stu-id="e2df5-181">Instead of banging your head on the desk, you can create a quick measure using the **Year-over-year change** calculation, and see how it appears in your visual and how the DAX formula works.</span></span> <span data-ttu-id="e2df5-182">จากนั้นคุณสามารถทำการเปลี่ยนแปลงในสูตร DAX โดยตรง หรือสร้างหน่วยวัดที่คล้ายกันที่ตรงตามความต้องการและการคาดหวังของคุณ</span><span class="sxs-lookup"><span data-stu-id="e2df5-182">Then you can either make changes directly to the DAX formula, or create a similar measure that meets your needs and expectations.</span></span> <span data-ttu-id="e2df5-183">เหมือนกับมีครูผู้สอนที่ตอบคำถามคุณแบบ what-if ในทันที โดยการคลิกไม่กี่ครั้ง</span><span class="sxs-lookup"><span data-stu-id="e2df5-183">It's like having a teacher that immediately responds to what-if questions you ask with a few clicks.</span></span> 

<span data-ttu-id="e2df5-184">คุณสามารถลบการวัดผลด่วนออกจากแบบจำลองของคุณได้เสมอหากคุณไม่ชอบ</span><span class="sxs-lookup"><span data-stu-id="e2df5-184">You can always delete quick measures from your model if you don't like them.</span></span> <span data-ttu-id="e2df5-185">ด้วยการคลิกขวาหรือเลือก **...** ถัดจากหน่วยวัดและการเลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="e2df5-185">That's as easy as right-clicking or selecting the **...** next to the measure and selecting **Delete**.</span></span> <span data-ttu-id="e2df5-186">นอกจากนี้ คุณยังสามารถเปลี่ยนชื่อการวัดผลด่วนสิ่งที่คุณต้องการโดยการเลือก **เปลี่ยนชื่อ** จากเมนู</span><span class="sxs-lookup"><span data-stu-id="e2df5-186">You can also rename a quick measure whatever you like by selecting **Rename** from the menu.</span></span> 

![ลบหรือเปลี่ยนชื่อการวัดผลด่วน](media/desktop-quick-measures/quick-measures_11.png)

## <a name="limitations-and-considerations"></a><span data-ttu-id="e2df5-188">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="e2df5-188">Limitations and considerations</span></span>
<span data-ttu-id="e2df5-189">มีข้อจำกัดและข้อควรพิจารณาบางข้อที่คุณควรทราบ</span><span class="sxs-lookup"><span data-stu-id="e2df5-189">There are a few limitations and considerations to keep in mind.</span></span>

- <span data-ttu-id="e2df5-190">คุณสามารถใช้การวัดผลด่วนที่เพิ่มลงในบานหน้าต่าง **เขตข้อมูล** ด้วยวิชวลต่าง ๆ ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="e2df5-190">You can use quick measures added to the **Fields** pane with any visual in the report.</span></span>
- <span data-ttu-id="e2df5-191">คุณสามารถดู DAX ที่เชื่อมโยงกับการวัดผลด่วนได้ตลอดเวลาโดยการเลือกหน่วยวัดในรายการ **เขตข้อมูล** จากนั้นดูสูตรในแถบสูตร</span><span class="sxs-lookup"><span data-stu-id="e2df5-191">You can always see the DAX associated with a quick measure by selecting the measure in the **Fields** list and looking at the formula in the formula bar.</span></span>
- <span data-ttu-id="e2df5-192">การวัดผลด่วนจะพร้อมใช้งานเฉพาะเมื่อคุณสามารถปรับเปลี่ยนแบบจำลองได้</span><span class="sxs-lookup"><span data-stu-id="e2df5-192">Quick measures are only available if you can modify the model.</span></span> <span data-ttu-id="e2df5-193">ซึ่งไม่ใช่กรณีเมื่อคุณกำลังทำงานกับการเชื่อมต่อสดบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="e2df5-193">That isn't the case when you're working with some Live connections.</span></span> <span data-ttu-id="e2df5-194">การเชื่อมต่อสดของตาราง SSAS ได้รับการสนับสนุนตามที่ได้อธิบายไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="e2df5-194">SSAS tabular live connections are supported, as previously described.</span></span>
- <span data-ttu-id="e2df5-195">คุณไม่สามารถสร้างการวัดผลด่วนตัวแสดงเวลา เมื่อทำงานในโหมด DirectQuery</span><span class="sxs-lookup"><span data-stu-id="e2df5-195">You can't create time intelligence quick measures when working in DirectQuery mode.</span></span> <span data-ttu-id="e2df5-196">ฟังก์ชัน DAX ที่ใช้ในการวัดผลด่วนเหล่านี้มีผลต่อประสิทธิภาพการทำงาน เมื่อแปลเป็นคำสั่ง T-SQL ที่ส่งไปยังแหล่งข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="e2df5-196">The DAX functions used in these quick measures have performance implications when translated into the T-SQL statements that are sent to your data source.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2df5-197">คำสั่ง DAX สำหรับการวัดผลด่วนใช้เครื่องหมายจุลภาคสำหรับตัวคั่นอาร์กิวเมนต์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e2df5-197">DAX statements for quick measures use only commas for argument separators.</span></span> <span data-ttu-id="e2df5-198">ถ้าเวอร์ชัน Power BI Desktop อยู่ในภาษาที่ใช้เครื่องหมายจุลภาคเป็นตัวคั่นทศนิยม การวัดผลด่วนจะทำงานไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e2df5-198">If your version of Power BI Desktop is in a language that uses commas as decimal separators, quick measures will not work properly.</span></span>

### <a name="time-intelligence-and-quick-measures"></a><span data-ttu-id="e2df5-199">ตัวแสดงเวลาและการวัดผลด่วน</span><span class="sxs-lookup"><span data-stu-id="e2df5-199">Time intelligence and quick measures</span></span>
<span data-ttu-id="e2df5-200">คุณสามารถใช้ตารางวันที่แบบกำหนดเองของคุณเองด้วยหน่วยวัดด่วนของตัวแสดงเวลา</span><span class="sxs-lookup"><span data-stu-id="e2df5-200">You can use your own custom date tables with time intelligence quick measures.</span></span> <span data-ttu-id="e2df5-201">ถ้าคุณกำลังใช้รูปแบบตารางจากภายนอก คุณต้องแน่ใจว่าเมื่อสร้างแบบจำลองขึ้นมา คอลัมน์วันที่หลักในตารางต้องถูกทำเครื่องหมายว่าเป็นตารางวันที่ ตามที่อธิบายไว้ใน[ระบุเครื่องหมายเป็นตารางวันที่สำหรับใช้กับตัวแสดงเวลา](/sql/analysis-services/tabular-models/specify-mark-as-date-table-for-use-with-time-intelligence-ssas-tabular)</span><span class="sxs-lookup"><span data-stu-id="e2df5-201">If you're using an external tabular model, make sure that when the model was built, the primary date column in the table was marked as a date table, as described in [Specify Mark as Date Table for use with time-intelligence](/sql/analysis-services/tabular-models/specify-mark-as-date-table-for-use-with-time-intelligence-ssas-tabular).</span></span> <span data-ttu-id="e2df5-202">ถ้าคุณกำลังนำเข้าตารางวันที่ของคุณเอง ตรวจสอบให้แน่ใจว่าได้ทำเครื่องหมายเป็นตารางวันที่ ตามที่อธิบายไว้ใน[ ตั้งค่าและใช้ตารางวันที่ใน Power BI Desktop](desktop-date-tables.md)</span><span class="sxs-lookup"><span data-stu-id="e2df5-202">If you're importing your own date table, make sure to mark it as a date table, as described in [Set and use date tables in Power BI Desktop](desktop-date-tables.md).</span></span>

### <a name="additional-information-and-examples"></a><span data-ttu-id="e2df5-203">ข้อมูลเพิ่มเติมและตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="e2df5-203">Additional information and examples</span></span>
<span data-ttu-id="e2df5-204">มีแนวคิดสำหรับการวัดผลด่วนที่ยังไม่มีหรือไม่</span><span class="sxs-lookup"><span data-stu-id="e2df5-204">Have an idea for a quick measure that isn't already provided?</span></span> <span data-ttu-id="e2df5-205">ดีเยี่ยม!</span><span class="sxs-lookup"><span data-stu-id="e2df5-205">Great!</span></span> <span data-ttu-id="e2df5-206">ลองดูหน้า[ Power BI Ideas](https://go.microsoft.com/fwlink/?linkid=842906) และส่งแนวคิดและสูตร DAX ของคุณสำหรับการวัดผลด่วนที่คุณต้องการดูใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e2df5-206">Check out the [Power BI Ideas](https://go.microsoft.com/fwlink/?linkid=842906) page, and submit your ideas and DAX formulas for quick measures you'd like to see in Power BI Desktop.</span></span> <span data-ttu-id="e2df5-207">เราจะพิจารณาการเพิ่มแนวคิดเหล่านี้ลงในรายการการวัดผลด่วนที่จะเผยแพร่ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="e2df5-207">We'll consider adding them to the quick measures list in a future release.</span></span>