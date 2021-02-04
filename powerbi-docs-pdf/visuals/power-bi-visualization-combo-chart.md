---
title: แผนภูมิผสมใน Power BI
description: บทช่วยสอนเกี่ยวกับแผนภูมิผสมนี้ อธิบายว่าเมื่อไรที่ควรใช้แผนภูมิผสม และวิธีการสร้างแผนภูมิเหล่านั้นในบริการ Power BI และเดสก์ท็อป
author: mihart
ms.author: mihart
ms.reviewer: mihart
featuredvideoid: lnv66cTZ5ho
ms.custom: lnv66cTZ5ho
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: conceptual
ms.date: 06/18/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 662b385ac88754afaa1e5178d77bfd335f63456b
ms.sourcegitcommit: 5c09d121d3205e65fb33a2eca0e60bc30e777773
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/18/2020
ms.locfileid: "97675361"
---
# <a name="create-and-use-combo-charts-in-power-bi"></a><span data-ttu-id="0d51e-103">สร้างและใช้แผนภูมิผสมใน Power BI</span><span class="sxs-lookup"><span data-stu-id="0d51e-103">Create and use combo charts in Power BI</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="0d51e-104">ใน Power BI แผนภูมิผสม เป็นการแสดงผลภาพที่รวมเอาแผนภูมิเส้นและแผนภูมิคอลัมน์เข้าด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="0d51e-104">In Power BI, a combo chart is a single visualization that combines a line chart and a column chart.</span></span> <span data-ttu-id="0d51e-105">การรวมแผนภูมิทั้ง 2 ให้เป็นหนึ่งเดียว ช่วยให้คุณทำการเปรียบเทียบข้อมูลได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="0d51e-105">Combining the 2 charts into one lets you make a quicker comparison of the data.</span></span>

<span data-ttu-id="0d51e-106">แผนภูมิผสม สามารถมีแกน Y หนึ่งหรือสองแกนก็ได้</span><span class="sxs-lookup"><span data-stu-id="0d51e-106">Combo charts can have one or two Y axes.</span></span>

## <a name="when-to-use-a-combo-chart"></a><span data-ttu-id="0d51e-107">เมื่อใดที่ต้องใช้แผนภูมิผสม</span><span class="sxs-lookup"><span data-stu-id="0d51e-107">When to use a Combo chart</span></span>
<span data-ttu-id="0d51e-108">แผนภูมิผสม เป็นตัวเลือกที่ดี:</span><span class="sxs-lookup"><span data-stu-id="0d51e-108">Combo charts are a great choice:</span></span>

* <span data-ttu-id="0d51e-109">เมื่อคุณมีแผนภูมิเส้นและแผนภูมิคอลัมน์ ที่ใช้แกน X เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="0d51e-109">when you have a line chart and a column chart with the same X axis.</span></span>
* <span data-ttu-id="0d51e-110">เพื่อเปรียบเทียบหลายหน่วยวัด ที่มีช่วงของค่าที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="0d51e-110">to compare multiple measures with different value ranges.</span></span>
* <span data-ttu-id="0d51e-111">เพื่อแสดงความสัมพันธ์ระหว่างสองหน่วยวัดในการแสดงผลหนึ่งภาพ</span><span class="sxs-lookup"><span data-stu-id="0d51e-111">to illustrate the correlation between two measures in one visualization.</span></span>
* <span data-ttu-id="0d51e-112">เพื่อตรวจสอบว่า หน่วยวัดหนึ่งบรรลุตามเป้าหมายที่ถูกกำหนดโดยอีกหน่วยวัดหนึ่งหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0d51e-112">to check whether one measure meet the target which is defined by another measure</span></span>
* <span data-ttu-id="0d51e-113">เพื่อประหยัดพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="0d51e-113">to conserve canvas space.</span></span>

> [!NOTE]
> <span data-ttu-id="0d51e-114">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="0d51e-114">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0d51e-115">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="0d51e-115">Prerequisites</span></span>
<span data-ttu-id="0d51e-116">บทช่วยสอนนี้ใช้[ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix)</span><span class="sxs-lookup"><span data-stu-id="0d51e-116">This tutorial uses the [Retail Analysis sample PBIX file](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix).</span></span>

1. <span data-ttu-id="0d51e-117">จากด้านบนซ้ายของแถบเมนู เลือก **ไฟล์** > **เปิด**</span><span class="sxs-lookup"><span data-stu-id="0d51e-117">From the upper left section of the menubar, select **File** > **Open**</span></span>
   
2. <span data-ttu-id="0d51e-118">ค้นหาสำเนา **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก**</span><span class="sxs-lookup"><span data-stu-id="0d51e-118">Find your copy of the **Retail Analysis sample PBIX file**</span></span>

1. <span data-ttu-id="0d51e-119">เปิด **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก** ในมุมมองรายงาน ![ภาพหน้าจอไอคอนมุมมองรายงาน](media/power-bi-visualization-kpi/power-bi-report-view.png)</span><span class="sxs-lookup"><span data-stu-id="0d51e-119">Open the **Retail Analysis sample PBIX file** in report view ![Screenshot of the report view icon.](media/power-bi-visualization-kpi/power-bi-report-view.png).</span></span>

1. <span data-ttu-id="0d51e-120">เลือก</span><span class="sxs-lookup"><span data-stu-id="0d51e-120">Select</span></span> ![สกรีนช็อตของแท็บสีเหลือง](media/power-bi-visualization-kpi/power-bi-yellow-tab.png) <span data-ttu-id="0d51e-122">หากต้องการเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="0d51e-122">to add a new page.</span></span>



## <a name="create-a-basic-single-axis-combo-chart"></a><span data-ttu-id="0d51e-123">สร้างแผนภูมิผสมแบบพื้นฐานที่มีแกนเดียว</span><span class="sxs-lookup"><span data-stu-id="0d51e-123">Create a basic, single-axis, Combo Chart</span></span>
<span data-ttu-id="0d51e-124">ดู Will สร้างแผนภูมิผสมโดยใช้ตัวอย่างการวิเคราะห์ด้านการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="0d51e-124">Watch Will create a combo chart using the Sales and Marketing sample.</span></span>
   > [!NOTE]
   > <span data-ttu-id="0d51e-125">วิดีโอนี้ใช้ Power BI Desktop เวอร์ชันเก่า</span><span class="sxs-lookup"><span data-stu-id="0d51e-125">This video uses an older version of Power BI Desktop.</span></span>
   > 
   > 
<iframe width="560" height="315" src="https://www.youtube.com/embed/lnv66cTZ5ho?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>  

<a name="create"></a>

1. <span data-ttu-id="0d51e-126">เริ่มจากหน้ารายงานเปล่าและจัดทำแผนภูมิแท่งที่แสดงยอดขายต่อปีและกำไรเบื้องต้นต่อเดือน</span><span class="sxs-lookup"><span data-stu-id="0d51e-126">Start on a blank report page and create a column chart that displays this year's sales and gross margin by month.</span></span>

    <span data-ttu-id="0d51e-127">a.</span><span class="sxs-lookup"><span data-stu-id="0d51e-127">a.</span></span>  <span data-ttu-id="0d51e-128">จากบานหน้าต่างเขตข้อมูล เลือก **ยอดขาย**\>**ยอดขายปีนี้** > **ค่า**</span><span class="sxs-lookup"><span data-stu-id="0d51e-128">From the Fields pane, select **Sales** \> **This Year Sales** > **Value**.</span></span>

    <span data-ttu-id="0d51e-129">b.</span><span class="sxs-lookup"><span data-stu-id="0d51e-129">b.</span></span>  <span data-ttu-id="0d51e-130">ลาก **ยอดขาย** \> **กำไรขั้นต้นปีนี้** ไปยัง **ค่า**</span><span class="sxs-lookup"><span data-stu-id="0d51e-130">Drag **Sales** \> **Gross Margin This Year** to the **Value** well.</span></span>

    <span data-ttu-id="0d51e-131">c.</span><span class="sxs-lookup"><span data-stu-id="0d51e-131">c.</span></span> <span data-ttu-id="0d51e-132">เลือก **เวลา** \> **FiscalMonth** เพื่อเพิ่มไปยัง **แกน**</span><span class="sxs-lookup"><span data-stu-id="0d51e-132">Select **Time** \> **FiscalMonth** to add it to the **Axis** well.</span></span>

    ![ตัวอย่างบทช่วยสอนแบบผสมผสาน](media/power-bi-visualization-combo-chart/combotutorial1new.png)
5. <span data-ttu-id="0d51e-134">เลือก **ตัวเลือกเพิ่มเติม** (...) ที่มุมบนขวาของการแสดงภาพและเลือก **เรียงลำดับตาม > FiscalMonth**</span><span class="sxs-lookup"><span data-stu-id="0d51e-134">Select **More options** (...) in the upper-right corner of the visualization, and select **Sort by > FiscalMonth**.</span></span> <span data-ttu-id="0d51e-135">เมื่อต้องเปลี่ยนลำดับการจัดเรียง เลือกจุดไข่ปลาอีกครั้ง แล้วคลิก **เรียงลำดับจากน้อยไปมาก** หรือ **เรียงลำดับจากมากไปน้อย**</span><span class="sxs-lookup"><span data-stu-id="0d51e-135">To change the sort order, select the ellipsis again and choose either **Sort ascending** or **Sort descending**.</span></span> <span data-ttu-id="0d51e-136">ในตัวอย่างนี้เราจะใช้ **เรียงลำดับจากน้อยไปมาก**</span><span class="sxs-lookup"><span data-stu-id="0d51e-136">For this example will use **Sort ascending**.</span></span>

6. <span data-ttu-id="0d51e-137">แปลงแผนภูมิคอลัมน์ให้เป็นแผนภูมิผสม</span><span class="sxs-lookup"><span data-stu-id="0d51e-137">Convert the column chart to a combo chart.</span></span> <span data-ttu-id="0d51e-138">มีแผนภูมิผสมสองแผนภูมิที่สามารถใช้งานได้: **เส้นกับคอลัมน์แบบเรียงซ้อน** และ **เส้นกับแผนภูมิคอลัมน์กลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="0d51e-138">There are two combo charts available: **Line and stacked column** and **Line and clustered column**.</span></span> <span data-ttu-id="0d51e-139">เมื่อยังเลือกแผนภูมิคอลัมน์นี้อยู่ ในบานหน้าต่าง **แสดงภาพ** เลือก **แผนภูมิเส้นและแผนภูมิกลุ่มคอลัมน์**</span><span class="sxs-lookup"><span data-stu-id="0d51e-139">With the column chart selected, from the **Visualizations** pane select the **Line and clustered column chart**.</span></span>

    ![ตัวอย่างการแปลงแผนภูมิผสมผสาน](media/power-bi-visualization-combo-chart/converttocombo-new2.png)
7. <span data-ttu-id="0d51e-141">จากบานหน้าต่าง **เขตข้อมูล** ลาก **ยอดขาย** \> **ยอดขายปีล่าสุด** ไปยังบักเก็ต **ค่าเส้นตรง**</span><span class="sxs-lookup"><span data-stu-id="0d51e-141">From the **Fields** pane, drag **Sales** \> **Last Year Sales** to the **Line Values** bucket.</span></span>

   ![พื้นที่ของค่าบรรทัดที่แสดงยอดขายของปีที่แล้ว](media/power-bi-visualization-combo-chart/linevaluebucket.png)

   <span data-ttu-id="0d51e-143">แผนภูมิผสมของคุณควรมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="0d51e-143">Your combo chart should look something like this:</span></span>

   ![ตัวอย่างแผนภูมิแท่งดำเนินการเสร็จสิ้น](media/power-bi-visualization-combo-chart/combochartdone-new.png)

## <a name="create-a-combo-chart-with-two-axes"></a><span data-ttu-id="0d51e-145">สร้างแผนภูมิผสมที่มีสองแกน</span><span class="sxs-lookup"><span data-stu-id="0d51e-145">Create a combo chart with two axes</span></span>
<span data-ttu-id="0d51e-146">ในงานที่จะทำต่อนี้ เราจะเปรียบเทียบอัตรากำไรขั้นต้นกับยอดขาย</span><span class="sxs-lookup"><span data-stu-id="0d51e-146">In this task, we'll compare gross margin and sales.</span></span>

1. <span data-ttu-id="0d51e-147">จัดทำแผนภูมิเส้นใหม่ที่แสดงข้อมูล **ยอดขายเบื้องต้นปีก่อนหน้าเป็น %** ตาม **เดือนในรอบปีบัญชี**</span><span class="sxs-lookup"><span data-stu-id="0d51e-147">Create a new line chart that tracks **Gross Margin last year %** by **FiscalMonth**.</span></span> <span data-ttu-id="0d51e-148">เลือกจุดไข่ปลาการเรียงลำดับตาม **เดือน** และ **จากน้อยไปหามาก**</span><span class="sxs-lookup"><span data-stu-id="0d51e-148">Select the ellipsis to sort it by **Month** and **Ascending**.</span></span>  
<span data-ttu-id="0d51e-149">ในเดือนมกราคม %กำไรขั้นต้น อยู่ที่ 35% ไปจุดสุงสุดที่ 45% ในเดือนเมษายน ตกลงในเดือนกรกฎาคม และกลับไปสูงสุดอีกครั้งในเดือนสิงหาคม</span><span class="sxs-lookup"><span data-stu-id="0d51e-149">In January GM% was 35%, peaked at 45% in April, dropped in July and peaked again in August.</span></span> <span data-ttu-id="0d51e-150">เราจะเห็นรูปแบบที่คล้ายกัน ในยอดขายปีที่แล้วและของปีนี้หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="0d51e-150">Will we see a similar pattern in sales last year and this year?</span></span>

   ![การขายจากตัวอย่างแผนภูมิผสมผสาน](media/power-bi-visualization-combo-chart/combo1-new.png)
2. <span data-ttu-id="0d51e-152">เพิ่ม **ยอดขายปีนี้ > ค่า** และ **ยอดขายปีที่แล้ว** ลงในแผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="0d51e-152">Add **This Year Sales > Value** and **Last Year Sales** to the line chart.</span></span> <span data-ttu-id="0d51e-153">ขนาดของ **%อัตรากำไรขั้นต้นปีที่แล้ว** น้อยกว่าขนาดของ **ยอดขาย** ซึ่งทำให้ยากต่อการเปรียบเทียบ</span><span class="sxs-lookup"><span data-stu-id="0d51e-153">The scale of **Gross Margin Last Year %** is much smaller than the scale of **Sales** which makes it difficult to compare.</span></span>      

   ![ตัวอย่างเส้นระนาบของแผนภูมิผสมผสาน](media/power-bi-visualization-combo-chart/flatline-new.png)
3. <span data-ttu-id="0d51e-155">เพื่อให้ง่ายต่อการอ่านและตีความวิชวล แปลงแผนภูมิเส้นให้เป็น แผนภูมิเส้นและแผนภูมิคอลัมน์แบบเรียงซ้อน</span><span class="sxs-lookup"><span data-stu-id="0d51e-155">To make the visual easier to read and interpret, convert the line chart to a Line and Stacked Column chart.</span></span>

   ![แปลงเป็นตัวอย่างแผนภูมิผสมผสาน](media/power-bi-visualization-combo-chart/converttocombo-new.png)

4. <span data-ttu-id="0d51e-157">ลาก **%อัตรากำไรปีที่แล้ว** จาก **ค่าคอลัมน์** ลงใน **ค่าเส้นตรง**</span><span class="sxs-lookup"><span data-stu-id="0d51e-157">Drag **Gross Margin Last Year %** from **Column Values** into **Line Values**.</span></span> <span data-ttu-id="0d51e-158">Power BI จะสร้างแกนสองแกน ซึ่งช่วยให้ชุดข้อมูลมีการปรับขนาดต่างกัน หน่วยวัดด้านซ้ายเป็นยอดขายในหน่วยดอลลาร์ ส่วนด้านขวาวัดเป็นเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="0d51e-158">Power BI creates two axes, thus allowing the datasets to be scaled differently; the left measures sales dollars and the right measures percentage.</span></span> <span data-ttu-id="0d51e-159">และเราเห็นคำตอบคำถามของเรา ใช่ เราดูแบบที่คล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="0d51e-159">And we see the answer to our question; yes, we do see a similar pattern.</span></span>

   ![ตัวอย่างแผนภูมิผสมผสานแบบคลัสเตอร์](media/power-bi-visualization-combo-chart/power-bi-clustered-combo.png)    

## <a name="add-titles-to-the-axes"></a><span data-ttu-id="0d51e-161">เพิ่มหัวข้อให้กับแกน</span><span class="sxs-lookup"><span data-stu-id="0d51e-161">Add titles to the axes</span></span>
1. <span data-ttu-id="0d51e-162">เลือกไอคอนลูกกลิ้งระบายสี</span><span class="sxs-lookup"><span data-stu-id="0d51e-162">Select the paint roller icon</span></span> ![ไอคอนลูกกลิ้งระบายสี](media/power-bi-visualization-combo-chart/power-bi-paintroller.png) <span data-ttu-id="0d51e-164">ในการเปิดพื้นที่การจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="0d51e-164">to open the Formatting pane.</span></span>
1. <span data-ttu-id="0d51e-165">เลือกลูกศรลงเพื่อขยายตัวเลือกของ **แกน Y**</span><span class="sxs-lookup"><span data-stu-id="0d51e-165">Select the down arrow to expand the **Y-axis** options.</span></span>
1. <span data-ttu-id="0d51e-166">สำหรับ **แกน Y (คอลัมน์)** ตั้งค่า **ตำแหน่ง** ไปเป็น **ซ้าย**, ตั้งค่า **หัวข้อ** เป็น **เปิด**, **สไตล์** เป็น **แสดงเฉพาะหัวข้อ** และ **แสดง** ในหน่วย **ล้าน**</span><span class="sxs-lookup"><span data-stu-id="0d51e-166">For **Y-Axis (Column)**, set **Position** to **Left**, set **Title** to **On**, **Style** to  **Show title only**, and **Display units** as **Millions**.</span></span>

   ![ตัวอย่างการเปิดแผนภูมิผสมผสาน y](media/power-bi-visualization-combo-chart/power-bi-open-y.png)
4. <span data-ttu-id="0d51e-168">จากr **แกน Y (คอลัมน์)** ให้เลื่อนลงจนเห็น **แสดงรายการสำรอง**</span><span class="sxs-lookup"><span data-stu-id="0d51e-168">Under **Y-Axis (Column)**, scroll down until you see **Show secondary**.</span></span> <span data-ttu-id="0d51e-169">เนื่องจากมีตัวเลือกมากมายสำหรับแกน Y คุณอาจต้องใช้แถบเลื่อนทั้งสองชุด</span><span class="sxs-lookup"><span data-stu-id="0d51e-169">Because there are so many options for the Y axes, you may have to use both scrollbars.</span></span> <span data-ttu-id="0d51e-170">หัวข้อ แสดงรายการสำรองจะแสดงตัวเลือกสำหรับการจัดรูปแบบ ส่วนของแผนภูมิเส้นภายในแผนภูมิผสม</span><span class="sxs-lookup"><span data-stu-id="0d51e-170">The Show secondary section displays options for formatting the line chart portion of the combo chart.</span></span>

   ![ตัวอย่างแผนภูมิผสมผสานสำรอง](media/power-bi-visualization-combo-chart/power-bi-secondary.png)
5. <span data-ttu-id="0d51e-172">สำหรับ **แกน Y (เส้น)** ปล่อยให้ **ตำแหน่ง** ยังคงเป็น **ขวา** เลื่อน **หัวข้อ** ให้เป็น **เปิด** และตั้งค่า **สไตล์** เป็น **แสดงเฉพาะหัวข้อ**</span><span class="sxs-lookup"><span data-stu-id="0d51e-172">For **Y-Axis (Line)**, leave **Position** as **Right**, turn **Title** to **On**, and set **Style** to **Show title only**.</span></span>

   <span data-ttu-id="0d51e-173">แผนภูมิผสมของคุณขณะนี้ แสดงแกนทั้งสองแกน และทั้งคู่ต่างก็มีหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="0d51e-173">Your combo chart now displays dual axes, both with titles.</span></span>

   ![ตัวอย่างชื่อแผนภูมิผสมสผสาน](media/power-bi-visualization-combo-chart/power-bi-2-titles.png)

6. <span data-ttu-id="0d51e-175">(ไม่บังคับ) ปรับเปลี่ยนแบบอักษรข้อความ ขนาด และสี และตั้งค่าตัวเลือกการจัดรูปแบบอื่น ๆ เพื่อปรับปรุงการแสดงผลและทำให้แผนภูมิอ่านง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="0d51e-175">Optionally, modify the text font, size, and color and set other formatting options to improve the display and readability of the chart.</span></span>

<span data-ttu-id="0d51e-176">จากตรงนี้ คุณอาจต้องการ:</span><span class="sxs-lookup"><span data-stu-id="0d51e-176">From here you might want to:</span></span>

* <span data-ttu-id="0d51e-177">[เพิ่มแผนภูมิผสมเป็นไทล์แดชบอร์ด](../create-reports/service-dashboard-tiles.md)</span><span class="sxs-lookup"><span data-stu-id="0d51e-177">[Add the combo chart as a dashboard tile](../create-reports/service-dashboard-tiles.md).</span></span>
* <span data-ttu-id="0d51e-178">[บันทึกรายงาน](../create-reports/service-report-save.md)</span><span class="sxs-lookup"><span data-stu-id="0d51e-178">[Save the report](../create-reports/service-report-save.md).</span></span>
* <span data-ttu-id="0d51e-179">[ทำให้รายงานสามารถเข้าถึงได้มากขึ้นสำหรับผู้ทุพพลภาพ](../create-reports/desktop-accessibility-overview.md)</span><span class="sxs-lookup"><span data-stu-id="0d51e-179">[Make the report more accessible for people with disabilities](../create-reports/desktop-accessibility-overview.md).</span></span>

## <a name="cross-highlighting-and-cross-filtering"></a><span data-ttu-id="0d51e-180">การไฮไลต์แบบเชื่อมโยง และการกรองข้าม</span><span class="sxs-lookup"><span data-stu-id="0d51e-180">Cross-highlighting and cross-filtering</span></span>

<span data-ttu-id="0d51e-181">การไฮไลต์คอลัมน์หรือเส้นในแผนภูมิผสม เป็นการไฮไลต์แบบเชื่อมโยงและกรองข้ามไปยังการแสดงภาพอื่น ๆ บนหน้ารายงาน และในทางกลับกัน การยกเลิกไฮไลต์จะเป็นการยกเลิกการกระทำดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="0d51e-181">Highlighting a column or line in a combo chart cross-highlights and cross-filters the other visualizations on the report page... and vice versa.</span></span> <span data-ttu-id="0d51e-182">ใช้[การปฏิสัมพันธ์กับภาพ](../create-reports/service-reports-visual-interactions.md) เพื่อเปลี่ยนคุณลักษณะเริ่มต้นนี้</span><span class="sxs-lookup"><span data-stu-id="0d51e-182">Use [visual interactions](../create-reports/service-reports-visual-interactions.md) to change this default behavior.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0d51e-183">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="0d51e-183">Next steps</span></span>

[<span data-ttu-id="0d51e-184">แผนภูมิโดนัทใน Power BI</span><span class="sxs-lookup"><span data-stu-id="0d51e-184">Doughnut charts in Power BI</span></span>](power-bi-visualization-doughnut-charts.md)

[<span data-ttu-id="0d51e-185">ชนิดการแสดงภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="0d51e-185">Visualization types in Power BI</span></span>](power-bi-visualization-types-for-reports-and-q-and-a.md)
