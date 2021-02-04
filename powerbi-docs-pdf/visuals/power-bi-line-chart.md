---
title: แผนภูมิเส้นใน Power BI
description: แผนภูมิเส้นใน Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: conceptual
ms.date: 05/05/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 6bd2ae3fe4abd3d1db21928edfa217d50f95ca92
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412609"
---
# <a name="line-charts-in-power-bi"></a><span data-ttu-id="94bb7-103">แผนภูมิเส้นใน Power BI</span><span class="sxs-lookup"><span data-stu-id="94bb7-103">Line charts in Power BI</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]

<span data-ttu-id="94bb7-104">แผนภูมิเส้นคือ ชุดของจุดข้อมูลที่จะแสดงด้วยจุดและเชื่อมต่อด้วยเส้นตรง</span><span class="sxs-lookup"><span data-stu-id="94bb7-104">A line chart is a series of data points that are represented by dots and connected by straight lines.</span></span> <span data-ttu-id="94bb7-105">แผนภูมิเส้นอาจมีเส้นเดียวหรือหลายเส้น</span><span class="sxs-lookup"><span data-stu-id="94bb7-105">A line chart may have one or many lines.</span></span> <span data-ttu-id="94bb7-106">แผนภูมิเส้นมีแกน X และแกน Y</span><span class="sxs-lookup"><span data-stu-id="94bb7-106">Line charts have an X and a Y axis.</span></span> 

![แผนภูมิเส้นแบบง่าย](media/power-bi-line-charts/power-bi-line.png)



## <a name="create-a-line-chart"></a><span data-ttu-id="94bb7-108">สร้างแผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="94bb7-108">Create a line chart</span></span>
<span data-ttu-id="94bb7-109">คำแนะนำเหล่านี้ใช้แอปตัวอย่างการขายและการตลาดเพื่อสร้างแผนภูมิเส้นที่แสดงยอดขายของปีนี้ตามประเภท</span><span class="sxs-lookup"><span data-stu-id="94bb7-109">These instructions use the Sales and Marketing Sample app to create a line chart that displays this year's sales by category.</span></span> <span data-ttu-id="94bb7-110">หากต้องการทำตามขั้นตอน รับแอปตัวอย่างจาก appsource.com</span><span class="sxs-lookup"><span data-stu-id="94bb7-110">To follow along, get the sample app from appsource.com.</span></span>

> [!NOTE]
> <span data-ttu-id="94bb7-111">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="94bb7-111">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span>

1. <span data-ttu-id="94bb7-112">เริ่มต้นบน หน้ารายงานเปล่า</span><span class="sxs-lookup"><span data-stu-id="94bb7-112">Start on a blank report page.</span></span> <span data-ttu-id="94bb7-113">หากคุณกำลังใช้บริการของ Power BI ตรวจสอบให้แน่ใจว่า คุณเปิดรายงานใน [มุมมองการแก้ไข](../create-reports/service-interact-with-a-report-in-editing-view.md)</span><span class="sxs-lookup"><span data-stu-id="94bb7-113">If you're using the Power BI service, make sure you open the report in [Editing View](../create-reports/service-interact-with-a-report-in-editing-view.md).</span></span>

2. <span data-ttu-id="94bb7-114">จากบานหน้าต่างเขตข้อมูล ให้เลือก **SalesFact** \> **ผลรวมหน่วย** และเลือก **วัน** > **เดือน**</span><span class="sxs-lookup"><span data-stu-id="94bb7-114">From the Fields pane, select **SalesFact** \> **Total units**, and select **Date** > **Month**.</span></span>  <span data-ttu-id="94bb7-115">Power BI สร้างแผนภูมิคอลัมน์บนพื้นที่รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="94bb7-115">Power BI creates a column chart on your report canvas.</span></span>

    ![เลือกจากบานหน้าต่างเขตข้อมูล](media/power-bi-line-charts/power-bi-step1.png)

4. <span data-ttu-id="94bb7-117">แปลงเป็นแผนภูมิเส้น โดยการเลือกเทมเพลตแผนภูมิเส้นจากบานหน้าต่างการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="94bb7-117">Convert to a line chart by selecting the line chart template from the Visualizations pane.</span></span> 

    ![แปลงเป็นแผนภูมิเส้น](media/power-bi-line-charts/power-bi-convert-to-line.png)
   

4. <span data-ttu-id="94bb7-119">กรองแผนภูมิเส้นของคุณเพื่อแสดงข้อมูลสำหรับปี 2012-2014</span><span class="sxs-lookup"><span data-stu-id="94bb7-119">Filter your line chart to show data for the years 2012-2014.</span></span> <span data-ttu-id="94bb7-120">หากบานหน้าต่างตัวกรองของคุณยุบตัวอยู่ ให้ขยายในทันที</span><span class="sxs-lookup"><span data-stu-id="94bb7-120">If your Filters pane is collapsed, expand it now.</span></span> <span data-ttu-id="94bb7-121">จากบานหน้าต่างเขตข้อมูล ให้เลือก **วัน** \> **ปี** และลากไปที่บานหน้าต่างตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="94bb7-121">From the Fields pane, select **Date** \> **Year** and drag it onto the Filters pane.</span></span> <span data-ttu-id="94bb7-122">วางลงที่ใต้ **ตัวกรองส่วนหัวบนภาพนี้**</span><span class="sxs-lookup"><span data-stu-id="94bb7-122">Drop it under the heading **Filters on this visual**.</span></span> 
     
    ![เส้นที่อยู่ถัดจากบานหน้าต่างเขตข้อมูล](media/power-bi-line-charts/power-bi-year-filter.png)

    <span data-ttu-id="94bb7-124">เปลี่ยนแปลง **ตัวกรองขั้นสูง** เป็น **ตัวกรองพื้นฐาน** และเลือก **2012**, **2013** และ **2014**</span><span class="sxs-lookup"><span data-stu-id="94bb7-124">Change **Advanced filters** to **Basic filters** and select **2012**, **2013** and **2014**.</span></span>

    ![ตัวกรองสำหรับปี](media/power-bi-line-charts/power-bi-filter-year.png)

6. <span data-ttu-id="94bb7-126">อีกวิธีหนึ่ง คือ [ปรับขนาดและสีของข้อความในแผนภูมิ](power-bi-visualization-customize-title-background-and-legend.md)</span><span class="sxs-lookup"><span data-stu-id="94bb7-126">Optionally, [adjust the size and color of the chart's text](power-bi-visualization-customize-title-background-and-legend.md).</span></span> 

    ![เพิ่มขนาดแบบอักษรและเปลี่ยนแบบอักษรแกน Y](media/power-bi-line-charts/power-bi-line-3years.png)

## <a name="add-additional-lines-to-the-chart"></a><span data-ttu-id="94bb7-128">เพิ่มเส้นเพิ่มเติมลงในแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="94bb7-128">Add additional lines to the chart</span></span>
<span data-ttu-id="94bb7-129">แผนภูมิเส้นสามารถมีเส้นหลายเส้นที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="94bb7-129">Line charts can have many different lines.</span></span> <span data-ttu-id="94bb7-130">และ ในบางกรณี ค่าในเส้นต่างๆ อาจแตกต่างกันมากจนแสดงผลร่วมกันได้ไม่ดี</span><span class="sxs-lookup"><span data-stu-id="94bb7-130">And, in some cases, the values on the lines may be so divergent that they don't display well together.</span></span> <span data-ttu-id="94bb7-131">มาดูที่การเพิ่มแผนภูมิเส้นเพิ่มเติมไปยังแผนภูมิปัจจุบันของเรา และเรียนรู้วิธีการจัดรูปแบบแผนภูมิของเราเมื่อเมื่อค่าที่แสดงด้วยเส้นมีความแตกต่างกันมาก</span><span class="sxs-lookup"><span data-stu-id="94bb7-131">Let's look at adding additional lines to our current chart and then learn how to format our chart when the values represented by the lines are very different.</span></span> 

### <a name="add-additional-lines"></a><span data-ttu-id="94bb7-132">เพิ่มเส้นเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="94bb7-132">Add additional lines</span></span>
<span data-ttu-id="94bb7-133">แทนที่จะดูผลรวมหน่วยสำหรับภูมิภาคทั้งหมดเป็นเส้นเดียวบนแผนภูมิ เราจะแยกหาผลรวมหน่วยตามภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="94bb7-133">Instead of looking at total units for all regions as a single line on the chart, let's split out total units by region.</span></span> <span data-ttu-id="94bb7-134">เพิ่มเส้นเพิ่มเติมโดยการลาก **ภูมิศาสตร์** > **ภูมิภาค** ไปยังส่วนคำอธิบายแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="94bb7-134">Add additional lines by dragging **Geo** > **Region** to the Legend well.</span></span>

   ![เส้นหนึ่งเส้นมีไว้สำหรับแต่ละภูมิภาค](media/power-bi-line-charts/power-bi-line-regions.png)


### <a name="use-two-y-axes"></a><span data-ttu-id="94bb7-136">ใช้แกน Y สองแกน</span><span class="sxs-lookup"><span data-stu-id="94bb7-136">Use two Y axes</span></span>
<span data-ttu-id="94bb7-137">จะเป็นอย่างไรหากคุณต้องการดูยอดขายรวมและผลรวมหน่วยบนแผนภูมิเดียวกัน?</span><span class="sxs-lookup"><span data-stu-id="94bb7-137">What if you want to look at total sales and total units on the same chart?</span></span> <span data-ttu-id="94bb7-138">ตัวเลขยอดขายสูงกว่าจำนวนหน่วย ทำให้แผนภูมิเส้นไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="94bb7-138">Sales numbers are so much higher than unit numbers, making the line chart unusable.</span></span> <span data-ttu-id="94bb7-139">อันที่จริงแล้ว เส้นสีแดงสำหรับผลรวมหน่วยปรากฏเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="94bb7-139">In fact, the red line for total units appears to be zero.</span></span>

   ![สกรีนช็อตแสดงให้เห็นว่าการใช้แกน  y เดี่ยวจะแสดงผลรวมหน่วยเป็นแบบแบนและการเปรียบเทียบที่ไร้ประโยชน์กับตัวเลขยอดขาย](media/power-bi-line-charts/power-bi-diverging.png)

<span data-ttu-id="94bb7-141">หากต้องการแสดงค่าที่แตกต่างกันมากบนแผนภูมิหนึ่งๆ ให้ใช้แผนภูมิผสม</span><span class="sxs-lookup"><span data-stu-id="94bb7-141">To display highly diverging values on one chart, use a combo chart.</span></span> <span data-ttu-id="94bb7-142">คุณสามารถเรียนรู้เกี่ยวกับแผนภูมิผสมทั้งหมด โดยการอ่าน [แผนภูมิผสมใน Power BI](power-bi-visualization-combo-chart.md)</span><span class="sxs-lookup"><span data-stu-id="94bb7-142">You can learn all about combo charts by reading [Combo charts in Power BI](power-bi-visualization-combo-chart.md).</span></span> <span data-ttu-id="94bb7-143">ในตัวอย่างของเราด้านล่าง เราสามารถแสดงยอดขายและหน่วยทั้งหมด ร่วมกันบนแผนภูมิหนึ่งๆ โดยการเพิ่มแกน Y แกนที่สอง</span><span class="sxs-lookup"><span data-stu-id="94bb7-143">In our example below, we can display sales and total units together on one chart by adding a second Y axis.</span></span> 

   ![สกรีนช็อตแสดงมูลค่าการขายเป็นแผนภูมิแท่งโดยมีแกน  y ทางด้านซ้ายและจำนวนหน่วยทั้งหมดเป็นเส้นที่มีแกน  y ทางด้านขวา](media/power-bi-line-charts/power-bi-dual-axes.png)

## <a name="highlighting-and-cross-filtering"></a><span data-ttu-id="94bb7-145">การทำไฮไลท์และการกรองข้าม</span><span class="sxs-lookup"><span data-stu-id="94bb7-145">Highlighting and cross-filtering</span></span>
<span data-ttu-id="94bb7-146">สำหรับข้อมูลเกี่ยวกับการใช้บานหน้าต่างตัวกรอง โปรดดู[เพิ่มตัวกรองไปยังรายงาน](../create-reports/power-bi-report-add-filter.md)</span><span class="sxs-lookup"><span data-stu-id="94bb7-146">For information about using the Filters pane, see [Add a filter to a report](../create-reports/power-bi-report-add-filter.md).</span></span>

<span data-ttu-id="94bb7-147">การเลือกจุดข้อมูลบนแผนภูมิเส้น เป็นการไฮไลต์แบบเชื่อมโยงและกรองข้ามไปยังการแสดงภาพอื่น ๆ บนหน้ารายงาน และในทางกลับกัน การยกเลิกไฮไลต์จะเป็นการยกเลิกการกระทำดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="94bb7-147">Selecting a data point on a line chart cross-highlights and cross-filters the other visualizations on the report page... and vice versa.</span></span> <span data-ttu-id="94bb7-148">หากต้องการปฏิบัติตาม ให้เปิดแท็บ **ตลาด**</span><span class="sxs-lookup"><span data-stu-id="94bb7-148">To follow along, open the **Market Share** tab.</span></span>  

<span data-ttu-id="94bb7-149">บนแผนภูมิเส้น จุดข้อมูลจุดเดียวคือจุดตัดของจุดใดจุดหนึ่งบนแกน Xและแกน Y</span><span class="sxs-lookup"><span data-stu-id="94bb7-149">On a line chart, a single data point is the intersection of a point on the X-axis and Y-axis.</span></span> <span data-ttu-id="94bb7-150">เมื่อคุณเลือกจุดข้อมูล Power BI จะเพิ่มเครื่องหมายเพื่อระบุว่าจุดใดจุดหนึ่ง (สำหรับเส้นเดียว) หรือจุดหลายจุด (ถ้ามีอย่างน้อยสองเส้น) เป็นแหล่งที่มาสำหรับการไฮไลท์ข้ามและกรองข้ามของการแสดงผลด้วยภาพฃอื่นๆ บนหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="94bb7-150">When you select a data point, Power BI adds markers indicating which point(for a single line) or points (if there are two or more lines) are the source for the cross-highlighting and cross-filtering of the other visuals on the report page.</span></span> <span data-ttu-id="94bb7-151">หากการแสดงผลด้วยภาพของคุณแน่นหนามาก Power BI จะเลือกจุดที่ใกล้กับจุดที่คุณคลิกภาพมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="94bb7-151">If your visual is very dense, Power BI will select the closest point to where you click on the visual.</span></span>

<span data-ttu-id="94bb7-152">ในตัวอย่างนี้ เราได้เลือกจุดข้อมูลที่ครอบคลุม: เดือนกรกฎาคม 2014 %ของส่วนแบ่งตลาดของหน่วย R12 เท่ากับ 33.16 และ %ของส่วนแบ่งตลาดของหน่วยเท่ากับ 34.74</span><span class="sxs-lookup"><span data-stu-id="94bb7-152">In this example, we've selected a data point that encompasses: July 2014, %Units Market Share R12 of 33.16 and %Units Market Share of 34.74.</span></span>

![เลือกจุดข้อมูลเดียวบนแผนภูมิเส้น](media/power-bi-line-charts/power-bi-single-select.png)

<span data-ttu-id="94bb7-154">โปรดสังเกตว่า แผนภูมิคอลัมน์จะมีการไฮไลต์ข้าม และเกจวัดมีการกรองแบบข้าม</span><span class="sxs-lookup"><span data-stu-id="94bb7-154">Notice how the column chart is cross-highlighted, and the gauge is cross-filtered.</span></span>

<span data-ttu-id="94bb7-155">เมื่อต้องการจัดการวิธีการที่แผนภูมิเน้นข้ามและกรองข้ามระหว่างกัน โปรดดู[การโต้ตอบแบบการแสดงภาพในรายงาน Power BI](../create-reports/service-reports-visual-interactions.md)</span><span class="sxs-lookup"><span data-stu-id="94bb7-155">To manage how charts cross-highlight and cross-filter each other, see [Visualization interactions in a Power BI report](../create-reports/service-reports-visual-interactions.md)</span></span>

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="94bb7-156">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="94bb7-156">Considerations and troubleshooting</span></span>
* <span data-ttu-id="94bb7-157">แผนภูมิเส้นหนึ่งไม่สามารถมีแกน Y คู่กัน</span><span class="sxs-lookup"><span data-stu-id="94bb7-157">One line chart cannot have dual Y axes.</span></span>  <span data-ttu-id="94bb7-158">คุณจะต้องใช้แผนภูมิผสมแทน</span><span class="sxs-lookup"><span data-stu-id="94bb7-158">You'll need to use a combo chart instead.</span></span>
* <span data-ttu-id="94bb7-159">ในตัวอย่างข้างต้น แผนภูมิถูกจัดรูปแบบเพื่อเพิ่มขนาดฟอนต์ เปลี่ยนสีฟอนต์ เพิ่มชื่อแกน จัดกึ่งกลางชื่อแผนภูมิและคำอธิบายแผนภูมิ เริ่มต้นทั้งสองแกนที่ศูนย์ และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="94bb7-159">In the examples above, the charts were formatted to increase font size, change font color, add axis titles, center the chart title and legend, start both axes at zero, and more.</span></span> <span data-ttu-id="94bb7-160">บานหน้าต่างการจัดรูปแบบ (ไอคอนลูกกลิ้งทาสี) มีชุดตัวเลือกมากมายที่ใช้สำหรับการตกแต่งแผนภูมิของคุณให้เป็นแบบที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="94bb7-160">The Formatting pane (paint roller icon) has a seemingly endless set of options for making your charts look the way you want them to.</span></span> <span data-ttu-id="94bb7-161">วิธีดีที่สุดในการเรียนรู้คือเปิดบานหน้าต่างการจัดรูปแบบและสำรวจ</span><span class="sxs-lookup"><span data-stu-id="94bb7-161">The best way to learn is to open the Formatting pane and explore.</span></span>

## <a name="next-steps"></a><span data-ttu-id="94bb7-162">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="94bb7-162">Next steps</span></span>

[<span data-ttu-id="94bb7-163">ชนิดการแสดงภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="94bb7-163">Visualization types in Power BI</span></span>](power-bi-visualization-types-for-reports-and-q-and-a.md)





