---
title: เรียงลำดับตามคอลัมน์ใน Power BI Desktop
description: ใน Power BI คุณสามารถเปลี่ยนลักษณะของวิชวล โดยเรียงลำดับตามเขตข้อมูลที่แตกต่างกันได้
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 01/30/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 06cd73aa86fdef58ea77b54305af300b1adb62d7
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412770"
---
# <a name="sort-by-column-in-power-bi-desktop"></a><span data-ttu-id="02951-103">เรียงลำดับตามคอลัมน์ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="02951-103">Sort by column in Power BI Desktop</span></span>
<span data-ttu-id="02951-104">ใน Power BI Desktop และบริการ Power BI คุณสามารถเปลี่ยนลักษณะของวิชวล โดยเรียงลำดับตามเขตข้อมูลที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="02951-104">In Power BI Desktop and the Power BI service, you can change how a visual looks by sorting it by different data fields.</span></span> <span data-ttu-id="02951-105">โดยการเปลี่ยนวิธีการเรียงลำดับวิชวล คุณสามารถเน้นข้อมูลที่คุณต้องการสื่อ และทำให้แน่ใจว่า วิชวลสะท้อนแนวโน้ม (หรือเน้นให้เห็น)</span><span class="sxs-lookup"><span data-stu-id="02951-105">By changing how you sort a visual, you can highlight the information you want to convey, and ensure the visual reflects that trend (or emphasis).</span></span>

<span data-ttu-id="02951-106">ไม่ว่าคุณจะใช้ข้อมูลตัวเลข (เช่น ตัวเลขยอดขาย) หรือข้อมูลข้อความ (เช่น ชื่อรัฐ) คุณสามารถเรียงลำดับการแสดงผลข้อมูลด้วยภาพของคุณ และทำให้แสดงในแบบที่คุณต้องการได้</span><span class="sxs-lookup"><span data-stu-id="02951-106">Whether you're using numeric data (such as sales figures) or text data (such as state names), you can sort your visualizations, and make them look like you want them to.</span></span> <span data-ttu-id="02951-107">Power BI มีความยืดหยุ่นสำหรับการรียงลำดับอย่างมาก และมีเมนูด่วนให้คุณใช้</span><span class="sxs-lookup"><span data-stu-id="02951-107">Power BI provides much flexibility for sorting, and quick menus for you to use.</span></span> <span data-ttu-id="02951-108">เมื่อต้องเรียงลำดับวิชวลใดก็ตาม ให้เลือกเมนู **ตัวเลือกเพิ่มเติม** (... ) เลือก **เรียงลำดับโดย** จากนั้นเลือกเขตข้อมูลที่คุณต้องการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="02951-108">To sort any visual, select its **More options** (...) menu, select **Sort by**, and then select the field by which you want to sort.</span></span>

![เมนูตัวเลือกเพิ่มเติม](media/desktop-sort-by-column/sortbycolumn_2.png)

## <a name="sorting-example"></a><span data-ttu-id="02951-110">ตัวอย่างการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="02951-110">Sorting example</span></span>
<span data-ttu-id="02951-111">ลองใช้ตัวอย่างที่มีความลึกมากกว่าเดิม และดูว่าทำงานอย่างไรใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="02951-111">Let's use an example that has more depth, and see how it works in Power BI Desktop.</span></span>

<span data-ttu-id="02951-112">การแสดงภาพต่อไปนี้แสดงต้นทุน, ปริมาณ และยอดเงินตามชื่อผู้ผลิต</span><span class="sxs-lookup"><span data-stu-id="02951-112">The following visualization shows costs, quantities, and amounts by manufacturer name.</span></span> <span data-ttu-id="02951-113">นี่คือการแสดงผลข้อมูลด้วยภาพ ก่อนที่จะทำการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="02951-113">Here's the visualization as it looks before we do any further sorting:</span></span>

![การแสดงภาพเริ่มต้น](media/desktop-sort-by-column/sortbycolumn_1.png)

<span data-ttu-id="02951-115">ในปัจจุบัน วิชวลจะถูกจัดเรียงตามคอลัมน์ **SalesQuantity**</span><span class="sxs-lookup"><span data-stu-id="02951-115">The visual is currently sorted by the **SalesQuantity** column.</span></span> <span data-ttu-id="02951-116">เราสามารถกำหนดคอลัมน์การเรียงลำดับโดยการจับคู่สีของแท่งจากน้อยไปหามากกับคำอธิบายแผนภูมิ แต่มีวิธีที่ดีกว่า: เมนู **ตัวเลือกเพิ่มเติม** ซึ่งคุณเข้าถึงได้โดยการเลือกจุดไข่ปลา (...)</span><span class="sxs-lookup"><span data-stu-id="02951-116">We can determine the sort column by matching the color of the ascending bars to the legend, but there's a better way: the **More options** menu, which you access by selecting the ellipses (...).</span></span>

![เมนูตัวเลือกเพิ่มเติม](media/desktop-sort-by-column/sortbycolumn_2.png)

<span data-ttu-id="02951-118">ตัวเลือกการเรียงลำดับจะเป็นดังนี้:</span><span class="sxs-lookup"><span data-stu-id="02951-118">The sorting selections are as follows:</span></span>

* <span data-ttu-id="02951-119">เขตข้อมูลที่เรียงลำดับในปัจจุบันคือ **SalesQuantity** ระบุโดย **SalesQuantity** เป็นตัวหนานำหน้าด้วยแท่งสีเหลือง</span><span class="sxs-lookup"><span data-stu-id="02951-119">The current sorting field is **SalesQuantity**, indicated by **SalesQuantity** in bold preceded by a yellow bar.</span></span> 

* <span data-ttu-id="02951-120">ทิศทางการเรียงลำดับปัจจุบันเรียงจากน้อยไปมากดังแสดงโดย **เรียงลำดับจากน้อยไปมาก** เป็นตัวหนานำหน้าด้วยแท่งสีเหลือง</span><span class="sxs-lookup"><span data-stu-id="02951-120">The current sorting direction is ascending, as shown by **Sort ascending** in bold preceded by a yellow bar.</span></span>

<span data-ttu-id="02951-121">เราจะดูเขตข้อมูลและทิศทางการเรียงลำดับในส่วนถัดไปอีกสองส่วน</span><span class="sxs-lookup"><span data-stu-id="02951-121">We'll look at the sorting field and sorting direction in the next two sections.</span></span>

## <a name="select-which-column-to-use-for-sorting"></a><span data-ttu-id="02951-122">เลือกคอลัมน์ที่จะใช้สำหรับการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="02951-122">Select which column to use for sorting</span></span>
<span data-ttu-id="02951-123">คุณสังเกตเห็นแท่งสีเหลืองที่อยู่ก่อนหน้า **SalesQuantity** ในเมนู **ตัวเลือกเพิ่มเติม** ซึ่งแสดงว่าวิชวลจะเรียงลำดับตามคอลัมน์ **SalesQuantity**</span><span class="sxs-lookup"><span data-stu-id="02951-123">You noticed the yellow bar preceding **SalesQuantity** in the **More options** menu, which indicates that the visual is sorted by the **SalesQuantity** column.</span></span> <span data-ttu-id="02951-124">การเรียงลำดับตามคอลัมน์อื่นเป็นเรื่องง่าย: เลือกจุดไข่ (...) เพื่อแสดงเมนู **ตัวเลือกเพิ่มเติม** เลือก **เรียงลำดับตาม** จากนั้นเลือกคอลัมน์อื่นที่แตกต่าง</span><span class="sxs-lookup"><span data-stu-id="02951-124">Sorting by another column is easy: select the ellipses (...) to show the **More options** menu, select **Sort by**, and then select a different column.</span></span>

<span data-ttu-id="02951-125">ในรูปต่อไปนี้ เราเลือก **DiscountAmount** เป็นคอลัมน์ที่เราต้องการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="02951-125">In the following image, we select **DiscountAmount** as the column by which we want to sort.</span></span> <span data-ttu-id="02951-126">คอลัมน์นั้นปรากฏเป็นหนึ่งในบรรทัดบนวิชวล แทนที่จะเป็นหนึ่งในแท่ง</span><span class="sxs-lookup"><span data-stu-id="02951-126">That column appears as one of the lines on the visual, rather than one of the bars.</span></span> 

![เรียงลำดับตาม DiscountAmount (มูลค่าส่วนลด)](media/desktop-sort-by-column/sortbycolumn_3.png)

<span data-ttu-id="02951-128">โปรดสังเกตว่าภาพได้เปลี่ยนไป</span><span class="sxs-lookup"><span data-stu-id="02951-128">Notice how the visual has changed.</span></span> <span data-ttu-id="02951-129">ค่าตอนนี้เรียงลำดับจากค่า **DiscountAmount** มากสุด ซึ่งคือ Fabrikam inc. ลงไปถึง Northwind Traders ซึ่งมีค่าต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="02951-129">The values now are ordered from the highest **DiscountAmount** value, Fabrikam Inc., down to the lowest, Northwind Traders.</span></span> 

<span data-ttu-id="02951-130">แต่อะไรจะเกิดขึ้นถ้าเราต้องการเรียงลำดับจากน้อยไปมาก แทนจากมากไปหาน้อยหรือไม่</span><span class="sxs-lookup"><span data-stu-id="02951-130">But what if we want to sort ascending, instead of descending?</span></span> <span data-ttu-id="02951-131">ส่วนถัดไปแสดงว่ามันง่ายอย่างไร</span><span class="sxs-lookup"><span data-stu-id="02951-131">The next section shows how easy that is to do.</span></span>

## <a name="select-the-sort-order"></a><span data-ttu-id="02951-132">เลือกลำดับการจัดเรียง</span><span class="sxs-lookup"><span data-stu-id="02951-132">Select the sort order</span></span>
<span data-ttu-id="02951-133">เมื่อเราดูเมนู **ตัวเลือกเพิ่มเติม** จากรูปภาพก่อนหน้า เราเห็นว่า **เรียงลำดับจากมากไปน้อย** อยู่ในรูปแบบตัวหนานำหน้าด้วยแท่งสีเหลือง</span><span class="sxs-lookup"><span data-stu-id="02951-133">When we take a closer look at the **More options** menu from the previous image, we see that **Sort descending** is in bold preceded by a yellow bar.</span></span>

![เรียงลำดับจากมากสุดไปหาน้อยสุด](media/desktop-sort-by-column/sortbycolumn_4.png)

<span data-ttu-id="02951-135">เมื่อเลือก **เรียงลำดับจากมากไปน้อย** นั่นหมายความว่า ภาพจะถูกเรียงลำดับตามคอลัมน์ที่เลือกตามลำดับของค่าที่มากที่สุดเมื่อต้องการค่าน้อยที่สุด</span><span class="sxs-lookup"><span data-stu-id="02951-135">When **Sort descending** is selected, it means the visual is being sorted by the selected column in order of greatest value to smallest value.</span></span> <span data-ttu-id="02951-136">ต้องการเปลี่ยนสิ่งนั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="02951-136">Want to change that?</span></span> <span data-ttu-id="02951-137">ไม่มีปัญหา เพียงแค่เลือก **เรียงลำดับจากน้อยไปมาก** และลำดับการจัดเรียงของคอลัมน์ที่เลือกจะเปลี่ยนจากค่าน้อยไปหามากที่สุด</span><span class="sxs-lookup"><span data-stu-id="02951-137">No problem, just select **Sort ascending** and the sort order of the selected column changes from smallest to greatest value.</span></span>

<span data-ttu-id="02951-138">ต่อไปนี้เป็นวิชวลเดียวกันของเรา หลังจากการเปลี่ยนแปลงการเรียงลำดับของ **DiscountAmount**</span><span class="sxs-lookup"><span data-stu-id="02951-138">Here's our same visual, after changing the ordering of **DiscountAmount**.</span></span> <span data-ttu-id="02951-139">สังเกตเห็นว่า ตอนนี้ Northwind Traders เป็นผู้ผลิตแรกที่แสดงในรายการ และ Fabrikam Inc. อยู่ลำดับสุดท้าย ซึ่งตรงกันข้ามกับการเรียงลำดับก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="02951-139">Notice that Northwind Traders is now the first manufacturer listed, and Fabrikam Inc. is the last; the opposite sorting from before.</span></span>

![เรียงลำดับจากน้อยสุดไปหามากสุด](media/desktop-sort-by-column/sortbycolumn_5.png)

<span data-ttu-id="02951-141">คุณสามารถเรียงลำดับตามคอลัมน์ใดก็ตามที่มีในวิชวล เราสามารถเลือก **SalesQuantity** ให้เป็นคอลัมน์ที่เราต้องการเรียงลำดับได้อย่างง่ายดาย เพื่อแสดงผู้ผลิตที่มียอดขายสูงที่สุดก่อน และยังคงรักษาคอลัมน์อื่น ๆ ไว้ในวิชวลตามที่ใช้กับผู้ผลิตรายนั้น</span><span class="sxs-lookup"><span data-stu-id="02951-141">You can sort by any column included in the visual; we could have easily selected **SalesQuantity** as the column by which we want to sort, to show the manufacturers with the most sales first, and still retain the other columns in the visual as they apply to that manufacturer.</span></span> <span data-ttu-id="02951-142">นี่คือวิชวลที่มองเห็นด้วยการตั้งค่าเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="02951-142">Here's a look at the visual with those settings:</span></span>

![เรียงลำดับตาม SalesQuantity](media/desktop-sort-by-column/sortbycolumn_6.png)

## <a name="sort-using-the-sort-by-column-button"></a><span data-ttu-id="02951-144">เรียงลำดับโดยใช้การเรียงลำดับตามปุ่มคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="02951-144">Sort using the Sort by Column button</span></span>
<span data-ttu-id="02951-145">มีวิธีอื่นในการเรียงลำดับข้อมูลของคุณ โดยใช้ปุ่ม **เรียงลำดับตามคอลัมน์** ในริบบิ้น **การสร้างแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="02951-145">There's another way to sort your data, by using the **Sort by Column** button in the **Modeling** ribbon.</span></span>

![ปุ่มจัดเรียงตามคอลัมน์](media/desktop-sort-by-column/sortbycolumn_8.png)

<span data-ttu-id="02951-147">วิธีการเรียงลำดับนี้ต้องการให้คุณเลือกคอลัมน์ (เขตข้อมูล) ก่อนเพื่อเรียงลำดับจากบานหน้าต่าง **เขตข้อมูล** จากนั้นเลือก **การสร้างแบบจำลอง** > **เรียงตามคอลัมน์** เพื่อเรียงลำดับวิชวลของคุณ</span><span class="sxs-lookup"><span data-stu-id="02951-147">This approach to sorting requires that you first select the column (field) to sort from the **Fields** pane, and then select **Modeling** > **Sort by Column** to sort your visual.</span></span> <span data-ttu-id="02951-148">ถ้าคุณไม่ได้เลือกคอลัมน์ ปุ่ม **เรียงตามคอลัมน์** จะไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="02951-148">If you don't select a column, the **Sort by Column** button is inactive.</span></span>

<span data-ttu-id="02951-149">มาลองดูตัวอย่างที่พบบ่อยกัน</span><span class="sxs-lookup"><span data-stu-id="02951-149">Let's look at a common example.</span></span> <span data-ttu-id="02951-150">คุณมีข้อมูลจากแต่ละเดือนของปี และคุณต้องการเรียงตามลำดับเวลา</span><span class="sxs-lookup"><span data-stu-id="02951-150">You have data from each month of the year, and you want to sort it based on chronological order.</span></span> <span data-ttu-id="02951-151">ขั้นตอนต่อไปนี้แสดงวิธีการดังกล่าว:</span><span class="sxs-lookup"><span data-stu-id="02951-151">The following steps show you how:</span></span>

1. <span data-ttu-id="02951-152">ให้สังเกตว่า เมื่อเลือกวิชวลแต่ไม่มีคอลัมน์ถูกเลือกไว้ในบานหน้าต่าง **เขตข้อมูล** ปุ่ม **เรียงลำดับตามคอลัมน์** จะไม่ทำงาน (เป็นสีเทา)</span><span class="sxs-lookup"><span data-stu-id="02951-152">Notice that when the visual is selected but no column is selected in the **Fields** pane, the **Sort by Column** button is inactive (grayed out).</span></span>
   
   ![ปุ่มจัดเรียงตามคอลัมน์ที่ไม่ใช้งาน](media/desktop-sort-by-column/sortbycolumn_9.png)

2. <span data-ttu-id="02951-154">เมื่อเราเลือกคอลัมน์ที่เราต้องการเรียงลำดับ ในบานหน้าต่าง **เขตข้อมูล** ปุ่ม **เรียงลำดับตามคอลัมน์** จะถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="02951-154">When we select the column by which we want to sort, in the **Fields** pane, the **Sort by Column** button becomes active.</span></span>
   
   ![ปุ่มจัดเรียงตามคอลัมน์ที่ใช้งาน](media/desktop-sort-by-column/sortbycolumn_10.png)
3. <span data-ttu-id="02951-156">ตอนนี้ เลือกวิชวลแล้ว เราสามารถเลือก **MonthOfYear** แทนที่จะเป็นค่าเริ่มต้น **MonthName** และตอนนี้วิชวลเรียงลำดับตามลำดับที่เราต้องการ คือเรียงตามเดือนในปี</span><span class="sxs-lookup"><span data-stu-id="02951-156">Now, with the visual selected, we can select **MonthOfYear**, instead of the default **MonthName**, and the visual sorts in the order we want: by the month of the year.</span></span>
   
   ![เมนูจัดเรียงตามคอลัมน์](media/desktop-sort-by-column/sortbycolumn_11.png)


<!---
This functionality is no longer active. Jan 2020

## Getting back to default column for sorting
You can sort by any column you'd like, but there may be times when you want the visual to return to its default sorting column. No problem. For a visual that has a sort column selected, open the **More options** menu and select that column again, and the visualization returns to its default sort column.

For example, here's our previous chart:

![Initial visualization](media/desktop-sort-by-column/sortbycolumn_6.png)

When we go back to the menu and select **SalesQuantity** again, the visual defaults to being ordered alphabetically by **Manufacturer**, as shown in the following image.

![Default sort order](media/desktop-sort-by-column/sortbycolumn_7.png)

With so many options for sorting your visuals, creating just the chart or image you want is easy.
--->

## <a name="next-steps"></a><span data-ttu-id="02951-158">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="02951-158">Next steps</span></span>

<span data-ttu-id="02951-159">คุณอาจมีความสนใจบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="02951-159">You might also be interested in the following articles:</span></span>

* [<span data-ttu-id="02951-160">ใช้ตัวเจาะเข้าถึงรายละเอียดข้ามรายงานใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="02951-160">Use cross-report drillthrough in Power BI Desktop</span></span>](desktop-cross-report-drill-through.md)
* [<span data-ttu-id="02951-161">ตัวแบ่งส่วนข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="02951-161">Slicers in Power BI</span></span>](../visuals/power-bi-visualization-slicers.md)
