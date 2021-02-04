---
title: แผนภูมิพื้นที่พื้นฐาน
description: แผนภูมิพื้นที่พื้นฐาน
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: conceptual
ms.date: 06/16/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 087aa281890d4b2702e6637bf3f1526ac331ea40
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96409918"
---
# <a name="create-and-use-basic-area-charts"></a><span data-ttu-id="076db-103">สร้างและใช้แผนภูมิพื้นที่แบบพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="076db-103">Create and use basic area charts</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="076db-104">แผนภูมิพื้นที่พื้นฐาน (หรือที่เรียกว่า แผนภูมิพื้นที่แบบชั้น) เป็นไปตามแผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="076db-104">The basic area chart (also known as layered area chart.) is based on the line chart.</span></span> <span data-ttu-id="076db-105">พื้นที่ระหว่างแกนและบรรทัดจะถูกเติมด้วยสีเพื่อระบุปริมาณ</span><span class="sxs-lookup"><span data-stu-id="076db-105">The area between axis and line is filled with colors to indicate volume.</span></span> 

<span data-ttu-id="076db-106">แผนภูมิพื้นที่เน้นให้เห็นปริมาณการเปลี่ยนแปลงตามเวลา และสามารถใช้เพื่อดึงความสนใจไปยังค่าผลรวมในทั่วทั้งแนวโน้ม</span><span class="sxs-lookup"><span data-stu-id="076db-106">Area charts emphasize the magnitude of change over time, and can be used to draw attention to the total value across a trend.</span></span> <span data-ttu-id="076db-107">ตัวอย่างเช่น เราสามารถลงจุดข้อมูลที่แสดงกำไรเมื่อเวลาผ่านไปในแผนภูมิพื้นที่เพื่อเน้นกำไรรวมได้</span><span class="sxs-lookup"><span data-stu-id="076db-107">For example, data that represents profit over time can be plotted in an area chart to emphasize the total profit.</span></span>

![แผนภูมิพื้นที่พื้นฐาน](media/power-bi-visualization-basic-area-chart/power-bi-chart-example.png)

> [!NOTE]
> <span data-ttu-id="076db-109">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="076db-109">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span>

## <a name="when-to-use-a-basic-area-chart"></a><span data-ttu-id="076db-110">เมื่อต้องการใช้แผนภูมิพื้นที่พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="076db-110">When to use a basic area chart</span></span>
<span data-ttu-id="076db-111">แผนภูมิพื้นที่พื้นฐานคือตัวเลือกที่ดีที่สุด:</span><span class="sxs-lookup"><span data-stu-id="076db-111">Basic area charts are a great choice:</span></span>

* <span data-ttu-id="076db-112">ในการดูและเปรียบเทียบแนวโน้มปริมาณข้อมูลทั่วชุดข้อมูลเวลา</span><span class="sxs-lookup"><span data-stu-id="076db-112">to see and compare the volume trend across time series</span></span> 
* <span data-ttu-id="076db-113">สำหรับแต่ละชุดข้อมูลที่แสดงถึงชุดข้อมูลตามจริงในจำนวนที่นับได้</span><span class="sxs-lookup"><span data-stu-id="076db-113">for individual series representing a physically countable set</span></span>

### <a name="prerequisites"></a><span data-ttu-id="076db-114">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="076db-114">Prerequisites</span></span>
<span data-ttu-id="076db-115">บทช่วยสอนนี้ใช้[ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix)</span><span class="sxs-lookup"><span data-stu-id="076db-115">This tutorial uses the [Retail Analysis sample PBIX file](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix).</span></span>

1. <span data-ttu-id="076db-116">จากด้านบนซ้ายของแถบเมนู เลือก **ไฟล์** > **เปิด**</span><span class="sxs-lookup"><span data-stu-id="076db-116">From the upper left section of the menubar, select **File** > **Open**</span></span>
   
2. <span data-ttu-id="076db-117">ค้นหาสำเนา **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก**</span><span class="sxs-lookup"><span data-stu-id="076db-117">Find your copy of the **Retail Analysis sample PBIX file**</span></span>

1. <span data-ttu-id="076db-118">เปิด **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก** ในมุมมองรายงาน ![ภาพหน้าจอไอคอนมุมมองรายงาน](media/power-bi-visualization-kpi/power-bi-report-view.png)</span><span class="sxs-lookup"><span data-stu-id="076db-118">Open the **Retail Analysis sample PBIX file** in report view ![Screenshot of the report view icon.](media/power-bi-visualization-kpi/power-bi-report-view.png).</span></span>

1. <span data-ttu-id="076db-119">เลือก</span><span class="sxs-lookup"><span data-stu-id="076db-119">Select</span></span> ![สกรีนช็อตของแท็บสีเหลือง](media/power-bi-visualization-kpi/power-bi-yellow-tab.png) <span data-ttu-id="076db-121">หากต้องการเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="076db-121">to add a new page.</span></span>


## <a name="create-a-basic-area-chart"></a><span data-ttu-id="076db-122">สร้างแผนภูมิพื้นที่พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="076db-122">Create a basic area chart</span></span>
 

1. <span data-ttu-id="076db-123">ขั้นตอนเหล่านี้จะช่วยสร้างแผนภูมิพื้นที่ที่แสดงยอดขายของปีนี้และยอดขายของปีที่แล้วแยกตามเดือน</span><span class="sxs-lookup"><span data-stu-id="076db-123">These steps will help you create an area chart that displays this year's sales and last year's sales by month.</span></span>
   
   <span data-ttu-id="076db-124">a.</span><span class="sxs-lookup"><span data-stu-id="076db-124">a.</span></span> <span data-ttu-id="076db-125">จากพื้นที่เขตข้อมูล เลือก **ยอดขาย\>ยอดขายของปีที่แล้ว** และ **ยอดขายของปีนี้ > ค่า**</span><span class="sxs-lookup"><span data-stu-id="076db-125">From the Fields pane, select **Sales \> Last Year Sales**, and **This Year Sales > Value**.</span></span>

   ![ค่าข้อมูลแผนภูมิพื้นที่](media/power-bi-visualization-basic-area-chart/power-bi-bar-chart.png)

   <span data-ttu-id="076db-127">b.</span><span class="sxs-lookup"><span data-stu-id="076db-127">b.</span></span>  <span data-ttu-id="076db-128">แปลงแผนภูมิเป็นแผนภูมิพื้นที่พื้นฐานโดยการเลือกไอคอนพื้นที่แผนภูมิจากพื้นที่การแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="076db-128">Convert the chart to a basic area chart by selecting the Area chart icon from the Visualizations pane.</span></span>

   ![ไอคอนแผนภูมิพื้นที่](media/power-bi-visualization-basic-area-chart/convertchart.png)
   
   <span data-ttu-id="076db-130">c.</span><span class="sxs-lookup"><span data-stu-id="076db-130">c.</span></span>  <span data-ttu-id="076db-131">เลือก **เวลา\>เดือนทางบัญชี** เพื่อเพิ่มไปยัง **แกน**</span><span class="sxs-lookup"><span data-stu-id="076db-131">Select **Time \> FiscalMonth** to add it to the **Axis** well.</span></span>   
   <span data-ttu-id="076db-132">![ค่าแกนแผนภูมิพื้นที่](media/power-bi-visualization-basic-area-chart/powerbi-area-chartnew.png)</span><span class="sxs-lookup"><span data-stu-id="076db-132">![area chart axis values](media/power-bi-visualization-basic-area-chart/powerbi-area-chartnew.png)</span></span>
   
   <span data-ttu-id="076db-133">d.</span><span class="sxs-lookup"><span data-stu-id="076db-133">d.</span></span>  <span data-ttu-id="076db-134">ในการแสดงแผนภูมิตามเดือน เลือกจุดไข่ปลา (มุมบนขวาของภาพ) แล้วเลือก **เรียงลำดับตามเดือน**</span><span class="sxs-lookup"><span data-stu-id="076db-134">To display the chart by month, select the ellipses (top right corner of the visual) and choose **Sort by month**.</span></span> <span data-ttu-id="076db-135">เมื่อต้องเปลี่ยนลำดับการจัดเรียง เลือกจุดไข่ปลาอีกครั้ง แล้วคลิก **เรียงลำดับจากน้อยไปมาก** หรือ **เรียงลำดับจากมากไปน้อย**</span><span class="sxs-lookup"><span data-stu-id="076db-135">To change the sort order, select the ellipses again and select either **Sort ascending** or **Sort descending**.</span></span>

## <a name="highlighting-and-cross-filtering"></a><span data-ttu-id="076db-136">การทำไฮไลท์และการกรองข้าม</span><span class="sxs-lookup"><span data-stu-id="076db-136">Highlighting and cross-filtering</span></span>
<span data-ttu-id="076db-137">สำหรับข้อมูลเกี่ยวกับการใช้บานหน้าต่างตัวกรอง โปรดดู[เพิ่มตัวกรองไปยังรายงาน](../create-reports/power-bi-report-add-filter.md)</span><span class="sxs-lookup"><span data-stu-id="076db-137">For information about using the Filters pane, see [Add a filter to a report](../create-reports/power-bi-report-add-filter.md).</span></span>

<span data-ttu-id="076db-138">เมื่อต้องการทำไฮไลท์เฉพาะพื้นที่หนึ่งในแผนภูมิของคุณ เลือกพื้นที่นั้นหรือเส้นขอบด้านบนของพื้นที่ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="076db-138">To highlight one particular area in your chart, select that area or its top border.</span></span>  <span data-ttu-id="076db-139">ถ้ามีการแสดงภาพอื่น ๆ บนหน้าเดียวกัน การทำไฮไลท์บนแผนภูมิพื้นที่พื้นฐานจะไม่กรองข้ามการแสดงภาพอื่น ๆ บนหน้ารายงาน ซึ่งต่างจากชนิดการแสดงภาพอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="076db-139">Unlike other visualization types, if there are other visualizations on the same page, highlighting a basic area charts does not cross-filter the other visualizations on the report page.</span></span> <span data-ttu-id="076db-140">อย่างไรก็ตาม แผนภูมิพื้นที่เป็นเป้าหมายสำหรับการกรองข้ามที่เปิดใช้งานโดยการแสดงภาพอื่น ๆ บนหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="076db-140">However, area charts are a target for cross-filtering triggered by other visualizations on the report page.</span></span> 

1. <span data-ttu-id="076db-141">ลองใช้โดยการเลือกแผนภูมิพื้นที่ของคุณ และคัดลอกไปยัง **ตัววิเคราะห์ร้านใหม่** หน้ารายงาน (CTRL C และ CTRL V)</span><span class="sxs-lookup"><span data-stu-id="076db-141">Try it out by selecting your area chart and copying it to the **New Store Analysis** report page (CTRL-C and CTRL-V).</span></span>
2. <span data-ttu-id="076db-142">เลือกหนึ่งพื้นที่แรเงาของแผนภูมิพื้นที่และเลือกแรเงาพื้นที่อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="076db-142">Select one of the shaded areas of the area chart and then select the other shaded area.</span></span> <span data-ttu-id="076db-143">คุณจะสังเกตผลที่มีต่อการแสดงภาพอื่น ๆ บนหน้า</span><span class="sxs-lookup"><span data-stu-id="076db-143">You'll notice no impact on the other visualizations on the page.</span></span>
1. <span data-ttu-id="076db-144">และตอนนี้ให้เลือกองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="076db-144">Now select an element.</span></span> <span data-ttu-id="076db-145">สังเกตผลกระทบบนแผนภูมิพื้นที่ที่ข้ามการกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="076db-145">Notice the impact on the area chart -- it gets cross-filtered.</span></span>

    ![ตัวอย่างการกรอง](media/power-bi-visualization-basic-area-chart/power-bi-area-chart-filters.gif) 

<span data-ttu-id="076db-147">เมื่อต้องการเรียนรู้เพิ่มเติม ดู[การโต้ตอบแบบภาพในรายงาน](../create-reports/service-reports-visual-interactions.md)</span><span class="sxs-lookup"><span data-stu-id="076db-147">To learn more, see [Visual interactions in reports](../create-reports/service-reports-visual-interactions.md)</span></span>


## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="076db-148">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="076db-148">Considerations and troubleshooting</span></span>   
* [<span data-ttu-id="076db-149">ทำให้รายงานสามารถเข้าถึงได้มากขึ้นสำหรับผู้ทุพพลภาพ</span><span class="sxs-lookup"><span data-stu-id="076db-149">Make the report more accessible for people with disabilities</span></span>](../create-reports/desktop-accessibility-overview.md)
* <span data-ttu-id="076db-150">แผนภูมิพื้นที่พื้นฐานจะไม่มีผลบังคับใช้สำหรับการเปรียบเทียบค่าดังกล่าวเนื่องจากมีสิ่งบดบังบนพื้นที่แบบชั้น</span><span class="sxs-lookup"><span data-stu-id="076db-150">Basic area charts are not effective for comparing the values due to the occlusion on the layered areas.</span></span> <span data-ttu-id="076db-151">Power BI ใช้ความโปร่งใสเพื่อระบุการเหลื่อมกันของพื้นที่</span><span class="sxs-lookup"><span data-stu-id="076db-151">Power BI uses transparency to indicate the overlap of areas.</span></span> <span data-ttu-id="076db-152">อย่างไรก็ตาม คุณลักษณะนี้จะทำงานได้ดีกับพื้นที่ที่แตกต่างกันสองหรือสามส่วนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="076db-152">However, it only works well with two or three different areas.</span></span> <span data-ttu-id="076db-153">เมื่อคุณต้องการเปรียบเทียบแนวโน้มกับค่าการวัดที่มากกว่าสามค่า ให้ลองใช้แผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="076db-153">When you need to compare trend to more than three measures, try using line charts.</span></span> <span data-ttu-id="076db-154">เมื่อคุณต้องการเปรียบเทียบปริมาณเทียบกับค่าการวัดที่มากกว่าสามค่า ลองใช้แผนภูมิต้นไม้</span><span class="sxs-lookup"><span data-stu-id="076db-154">When you need to compare volume to more than three measures, try using treemap.</span></span>

## <a name="next-step"></a><span data-ttu-id="076db-155">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="076db-155">Next step</span></span>
[<span data-ttu-id="076db-156">รายงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="076db-156">Reports in Power BI</span></span>](power-bi-visualization-card.md)  
