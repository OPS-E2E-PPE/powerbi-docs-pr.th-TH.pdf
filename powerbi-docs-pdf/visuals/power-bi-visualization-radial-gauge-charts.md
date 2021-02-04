---
title: แผนภูมิหน้าปัดความเร็วใน Power BI
description: แผนภูมิหน้าปัดความเร็วใน Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
featuredvideoid: ''
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: conceptual
ms.date: 06/17/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 013e9f3143c485fd63a160f8d124e313b7c2edc6
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418842"
---
# <a name="radial-gauge-charts-in-power-bi"></a><span data-ttu-id="72e7d-103">แผนภูมิหน้าปัดความเร็วใน Power BI</span><span class="sxs-lookup"><span data-stu-id="72e7d-103">Radial gauge charts in Power BI</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="72e7d-104">แผนภูมิหน้าปัดความเร็วมีโค้งวงกลมและแสดงเป็นค่าเดียวที่วัดความคืบหน้าตามเพื่อไปสู่เป้าหมาย Key Performance Indicator (KPI)</span><span class="sxs-lookup"><span data-stu-id="72e7d-104">A radial gauge chart has a circular arc and shows a single value that measures progress toward a goal or a Key Performance Indicator (KPI).</span></span> <span data-ttu-id="72e7d-105">เส้น (หรือ *เข็ม*) แทนค่าเป้าหมายหรือปลายทาง</span><span class="sxs-lookup"><span data-stu-id="72e7d-105">The line (or *needle*) represents the goal or target value.</span></span> <span data-ttu-id="72e7d-106">การแรเงาแทนด้วยความคืบหน้าสู่เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="72e7d-106">The shading represents the progress toward that goal.</span></span> <span data-ttu-id="72e7d-107">ค่าภายในส่วนโค้งแทนค่าความคืบหน้า</span><span class="sxs-lookup"><span data-stu-id="72e7d-107">The The value inside the arc represents the progress value.</span></span> <span data-ttu-id="72e7d-108">Power BI แพร่ค่าที่เป็นไปได้ทั้งหมดจะกระจายเท่าๆ กันตามส่วนโค้ง จากค่าต่ำสุด (ค่าซ้ายสุด) ไปสู่ค่าสูงสุด (ค่าขวาสุด)</span><span class="sxs-lookup"><span data-stu-id="72e7d-108">Power BI spreads all possible values evenly along the arc, from the minimum (left-most value) to the maximum (right-most value).</span></span>

![สกรีนช็อตของตัววัดรัศมี](media/power-bi-visualization-radial-gauge-charts/gauge-m.png)

<span data-ttu-id="72e7d-110">ในตัวอย่างนี้ เรามีผู้ค้าปลีกรถยนต์ที่กำลังติดตามการขายเฉลี่ยของทีมขายต่อเดือน</span><span class="sxs-lookup"><span data-stu-id="72e7d-110">In this example, you're a car retailer tracking the sales team's average sales per month.</span></span> <span data-ttu-id="72e7d-111">เข็มแสดงเป้าหมายทางการขายรถยนต์ให้ได้ 140 คัน</span><span class="sxs-lookup"><span data-stu-id="72e7d-111">The needle represents a 140 cars sales goal.</span></span> <span data-ttu-id="72e7d-112">การขายเฉลี่ยที่เป็นไปได้น้อยที่สุดคือ 0 และสูงสุดเป็น 200 คัน</span><span class="sxs-lookup"><span data-stu-id="72e7d-112">The minimum possible average sales is 0 and the maximum is 200.</span></span>  <span data-ttu-id="72e7d-113">การแรเงาสีน้ำเงินแสดงว่า ตอนนี้เราประมาณการว่ามีการขาย 120 คันในเดือนนี้</span><span class="sxs-lookup"><span data-stu-id="72e7d-113">The blue shading shows that the team is averaging approximately 120 sales this month.</span></span> <span data-ttu-id="72e7d-114">โชคดี มีสัปดาห์อื่นยังที่สามารถไปถึงเป้าหมายได้</span><span class="sxs-lookup"><span data-stu-id="72e7d-114">Luckily, there's still another week to reach the goal.</span></span>

> [!NOTE]
> <span data-ttu-id="72e7d-115">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="72e7d-115">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span>

## <a name="when-to-use-a-radial-gauge"></a><span data-ttu-id="72e7d-116">เมื่อต้องการใช้แผนภูมิหน้าปัดความเร็ว</span><span class="sxs-lookup"><span data-stu-id="72e7d-116">When to use a radial gauge</span></span>

<span data-ttu-id="72e7d-117">แผนภูมิหน้าปัดความเร็วเป็นทางเลือกที่ดีสำหรับ</span><span class="sxs-lookup"><span data-stu-id="72e7d-117">Radial gauges are a great choice to:</span></span>

* <span data-ttu-id="72e7d-118">แสดงความคืบหน้าเพื่อจะบรรลุเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="72e7d-118">Show progress toward a goal.</span></span>

* <span data-ttu-id="72e7d-119">แสดงการวัดร้อยละ เช่น KPI</span><span class="sxs-lookup"><span data-stu-id="72e7d-119">Represent a percentile measure, like a KPI.</span></span>

* <span data-ttu-id="72e7d-120">แสดงความสมบูรณ์ของการวัดเดี่ยว</span><span class="sxs-lookup"><span data-stu-id="72e7d-120">Show the health of a single measure.</span></span>

* <span data-ttu-id="72e7d-121">แสดงข้อมูลเพื่อที่คุณสามารถสแกนและทำความเข้าใจอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="72e7d-121">Display information you can quickly scan and understand.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="72e7d-122">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="72e7d-122">Prerequisites</span></span>

<span data-ttu-id="72e7d-123">บทช่วยสอนนี้ใช้[ไฟล์ Excel ตัวอย่างทางการเงิน](https://go.microsoft.com/fwlink/?LinkID=521962)</span><span class="sxs-lookup"><span data-stu-id="72e7d-123">This tutorial uses the [Financial sample Excel file](https://go.microsoft.com/fwlink/?LinkID=521962).</span></span>

1. <span data-ttu-id="72e7d-124">จากด้านบนซ้ายของแถบเมนู ให้เลือก **รับข้อมูล** > **Excel**</span><span class="sxs-lookup"><span data-stu-id="72e7d-124">From the upper left section of the menubar, select **Get Data** > **Excel**</span></span>
   
2. <span data-ttu-id="72e7d-125">ค้นหาสำเนา **ไฟล์ Excel ตัวอย่างด้านการเงินของคุณ**</span><span class="sxs-lookup"><span data-stu-id="72e7d-125">Find your copy of the **Financial sample Excel file**</span></span>

1. <span data-ttu-id="72e7d-126">เปิด **ไฟล์ Excel ตัวอย่างด้านการเงิน** ในมุมมองรายงาน![ ภาพหน้าจอของไอคอนมุมมองรายงาน](media/power-bi-visualization-kpi/power-bi-report-view.png)</span><span class="sxs-lookup"><span data-stu-id="72e7d-126">Open the **Financial sample Excel file** in report view ![Screenshot of the report view icon.](media/power-bi-visualization-kpi/power-bi-report-view.png).</span></span>

1. <span data-ttu-id="72e7d-127">เลือก **การเงิน** และ **Sheet1**</span><span class="sxs-lookup"><span data-stu-id="72e7d-127">Select **financials** and **Sheet1**</span></span>

1. <span data-ttu-id="72e7d-128">คลิก **โหลด**</span><span class="sxs-lookup"><span data-stu-id="72e7d-128">Click **Load**</span></span>

1. <span data-ttu-id="72e7d-129">เลือก</span><span class="sxs-lookup"><span data-stu-id="72e7d-129">Select</span></span> ![สกรีนช็อตของแท็บสีเหลือง](media/power-bi-visualization-kpi/power-bi-yellow-tab.png) <span data-ttu-id="72e7d-131">หากต้องการเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="72e7d-131">to add a new page.</span></span>



## <a name="create-a-basic-radial-gauge"></a><span data-ttu-id="72e7d-132">สร้างแผนภูมิหน้าปัดความเร็วแบบพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="72e7d-132">Create a basic radial gauge</span></span>

### <a name="step-1-create-a-gauge-to-track-gross-sales"></a><span data-ttu-id="72e7d-133">ขั้นตอนที่ 1: สร้างตัววัดแบบหน้าปัดความเร็วเพื่อติดตามยอดขายรวม</span><span class="sxs-lookup"><span data-stu-id="72e7d-133">Step 1: Create a gauge to track Gross Sales</span></span>

1. <span data-ttu-id="72e7d-134">เริ่มต้นบน หน้ารายงานเปล่า</span><span class="sxs-lookup"><span data-stu-id="72e7d-134">Start on a blank report page</span></span>

1. <span data-ttu-id="72e7d-135">ในบานหน้าต่างของ **เขตข้อมูล** ให้เลือก **ยอดขายรวม**</span><span class="sxs-lookup"><span data-stu-id="72e7d-135">From the **Fields** pane, select **Gross Sales**.</span></span>

   ![ตารางการเงินจะถูกขยายและยอดขายรวมจะถูกเลือก](media/power-bi-visualization-radial-gauge-charts/grosssalesvalue-new.png)

1. <span data-ttu-id="72e7d-137">เปลี่ยนการรวมข้อมูลเป็น **หาค่าเฉลี่ย**</span><span class="sxs-lookup"><span data-stu-id="72e7d-137">Change the aggregation to **Average**.</span></span>

   ![สกรีนช็อตของการเรียกบานหน้าต่างเขตข้อมูลที่มียอดขายรวมและผลรวมค่าเฉลี่ยออกมา](media/power-bi-visualization-radial-gauge-charts/changetoaverage-new.png)

1. <span data-ttu-id="72e7d-139">เลือกไอคอนตัววัด</span><span class="sxs-lookup"><span data-stu-id="72e7d-139">Select the gauge icon</span></span> ![สกรีนช็อตของไอคอนตัววัด](media/power-bi-visualization-radial-gauge-charts/gaugeicon-new.png) <span data-ttu-id="72e7d-141">การแปลงแผนภูมิคอลัมน์ให้เป็นแผนภูมิตัววัด</span><span class="sxs-lookup"><span data-stu-id="72e7d-141">to convert the column chart to a gauge chart.</span></span>

    ![สกรีนช็อตของแผนภูมิตัววัด](media/power-bi-visualization-radial-gauge-charts/gauge-no-target.png)

    <span data-ttu-id="72e7d-143">ขึ้นอยู่กับเมื่อคุณดาวน์โหลดไฟล์ **ตัวอย่างการเงิน** คุณอาจเห็นตัวเลขที่ไม่ตรงกับตัวเลขเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="72e7d-143">Depending on when you download the **Financial Sample** file, you may see numbers that don't match these numbers.</span></span>

    > [!TIP]
    > <span data-ttu-id="72e7d-144">ตามค่าเริ่มต้น Power BI สร้างแผนภูมหน้าปัดความเร็วที่คาดการณ์ตามค่าปัจจุบัน (ในกรณีนี้คือ **ค่าเฉลี่ยของผลรวมขาย**) จะถือว่าเป็นจุดกลิ่งกลางของหน้าปัด</span><span class="sxs-lookup"><span data-stu-id="72e7d-144">By default, Power BI creates a gauge chart where it assumes the current value (in this case, **Average of Gross Sales**) is at the halfway point on the gauge.</span></span> <span data-ttu-id="72e7d-145">เนื่องจากค่า **ยอดขายรวมค่าเฉลี่ย** คือ $182.76K ค่าเริ่มต้น (ต่ำสุด) ถูกตั้งค่าเป็น 0 และค่าสิ้นสุด (สูงสุด) ถูกตั้งค่าเป็นคู่ค่าปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="72e7d-145">Since the **Average of Gross Sales** value is $182.76K, the start value (Minimum) is set to 0 and the end value (Maximum) is set to double the current value.</span></span>

### <a name="step-3-set-a-target-value"></a><span data-ttu-id="72e7d-146">ขั้นตอนที่ 3: ตั้งค่าเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="72e7d-146">Step 3: Set a target value</span></span>

1. <span data-ttu-id="72e7d-147">ลาก **COGS** จากบานหน้าต่าง **เขตข้อมูล** เพื่อตั้ง **ค่าเป้าหมาย** ที่ดี</span><span class="sxs-lookup"><span data-stu-id="72e7d-147">Drag **COGS** from the **Fields** pane to the **Target value** well.</span></span>

1. <span data-ttu-id="72e7d-148">เปลี่ยนการรวมข้อมูลเป็น **หาค่าเฉลี่ย**</span><span class="sxs-lookup"><span data-stu-id="72e7d-148">Change the aggregation to **Average**.</span></span>

   <span data-ttu-id="72e7d-149">Power BI เพิ่มเข็มเพื่อแสดงค่าเป้าหมาย **$145.48K** ของเรา</span><span class="sxs-lookup"><span data-stu-id="72e7d-149">Power BI adds a needle to represent our target value of **$145.48K**.</span></span>

   ![เพิ่มสกรีนช็อตของแผนภูมิตัววัดกับการเฉลี่ยของ COGS](media/power-bi-visualization-radial-gauge-charts/gaugeinprogress-new.png)

    <span data-ttu-id="72e7d-151">โปรดสังเกตว่าเราได้เกินเป้าหมายของเราแล้ว</span><span class="sxs-lookup"><span data-stu-id="72e7d-151">Notice that we've exceeded our target.</span></span>

   > [!NOTE]
   > <span data-ttu-id="72e7d-152">คุณสามารถใส่ค่าเป้าหมายด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="72e7d-152">You can also manually enter a target value.</span></span> <span data-ttu-id="72e7d-153">ดู [ใช้ตัวเลือกของการจัดรูปแบบเพื่อตั้งค่าต่ำสุด สูงสุด และส่วนของค่าเป้าหมาย](#use-manual-format-options-to-set-minimum-maximum-and-target-values)</span><span class="sxs-lookup"><span data-stu-id="72e7d-153">See the [Use manual format options to set Minimum, Maximum, and Target values](#use-manual-format-options-to-set-minimum-maximum-and-target-values) section.</span></span>

### <a name="step-4-set-a-maximum-value"></a><span data-ttu-id="72e7d-154">ขั้นตอนที่ 4: ตั้งค่าสูงสุด</span><span class="sxs-lookup"><span data-stu-id="72e7d-154">Step 4: Set a maximum value</span></span>

<span data-ttu-id="72e7d-155">ในขั้นตอนที่ 2 Power BI ให้ใช้เขตข้อมูลที่ตั้ง **ค่า** ต่ำสุด(เริ่มต้น) และค่าสูงสุด(สิ้นสุด)โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="72e7d-155">In Step 2, Power BI used the **Value** field to automatically set minimum and maximum values.</span></span> <span data-ttu-id="72e7d-156">จะเกิดอะไรขึ้นถ้าคุณต้องการตั้งค่าสูงสุดของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="72e7d-156">What if you want to set your own maximum value?</span></span> <span data-ttu-id="72e7d-157">สมมติว่าแทนที่จะใช้่ค่าปัจจุบันคุณสองเป็นค่าที่เป็นไปได้สูงสุด คุณต้องการตั้งค่าเป็นตัวเลขยอดขายรวมสูงสุดในชุดข้อมูลของคุณหรือไม่</span><span class="sxs-lookup"><span data-stu-id="72e7d-157">Let's say that, instead of using double the current value as the maximum possible value, you want to set it to the highest Gross Sales number in your dataset.</span></span>

1. <span data-ttu-id="72e7d-158">ลาก **ยอดขายรวม** จากหน้าต่าง **เขตข้อมูล** ไปยัง **ค่าสูงสุด**</span><span class="sxs-lookup"><span data-stu-id="72e7d-158">Drag **Gross Sales** from the **Fields** pane to the **Maximum value** well.</span></span>

1. <span data-ttu-id="72e7d-159">เปลี่ยนการรวมข้อมูลเป็น **หาค่าสูงสุด**</span><span class="sxs-lookup"><span data-stu-id="72e7d-159">Change the aggregation to **Maximum**.</span></span>

   ![สกรีนช็อตของการเรียกบานหน้าต่างเขตข้อมูลที่มียอดขายรวมและผลรวมสูงสุดออกมา](media/power-bi-visualization-radial-gauge-charts/setmaximum-new.png)

   <span data-ttu-id="72e7d-161">รูปฟน้าปัดวัดถูกวาดอีกครั้ง ด้วยค่าสุดท้ายใหม่ คือ 1.21 ล้านของยอดขายรวม</span><span class="sxs-lookup"><span data-stu-id="72e7d-161">The gauge is redrawn with a new end value, 1.21 million in gross sales.</span></span>

   ![สกรีนช็อตของแผนภูมิตัววัดที่เสร็จสมบูรณ์แล้ว](media/power-bi-visualization-radial-gauge-charts/power-bi-final-gauge.png)

### <a name="step-5-save-your-report"></a><span data-ttu-id="72e7d-163">ขั้นตอนที่ 5: บันทึกรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="72e7d-163">Step 5: Save your report</span></span>

1. <span data-ttu-id="72e7d-164">[บันทึกรายงาน](../create-reports/service-report-save.md)</span><span class="sxs-lookup"><span data-stu-id="72e7d-164">[Save the report](../create-reports/service-report-save.md).</span></span>

## <a name="use-manual-format-options-to-set-minimum-maximum-and-target-values"></a><span data-ttu-id="72e7d-165">ใช้ตัวเลือกของการจัดรูปแบบเพื่อตั้งค่าต่ำสุด สูงสุด และค่าเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="72e7d-165">Use manual format options to set Minimum, Maximum, and Target values</span></span>

1. <span data-ttu-id="72e7d-166">ลาก **ยอดขายรวมมากที่สุด** จาก **ค่าสูงสุด**</span><span class="sxs-lookup"><span data-stu-id="72e7d-166">Remove **Max of Gross Sales** from the **Maximum value** well.</span></span>

1. <span data-ttu-id="72e7d-167">เลือกไอคอนแปรงลูกกลิ้งเพื่อเปิดแถบ **จัดรูปร่าง**</span><span class="sxs-lookup"><span data-stu-id="72e7d-167">Select the paint roller icon to open the **Format** pane.</span></span>

   ![สกรีนช็อตของการเรียกแผนภูมิตัววัดและบานหน้าต่างจัดรูปแบบที่ มีไอคอนลูกกลิ้งระบายสีออกมา](media/power-bi-visualization-radial-gauge-charts/power-bi-roller.png)

1. <span data-ttu-id="72e7d-169">ขยาย **แกนตัววัด** และใส่ค่า **ต่ำสุด** และ **สูงสุด**</span><span class="sxs-lookup"><span data-stu-id="72e7d-169">Expand **Gauge axis** and enter values for **Min** and **Max**.</span></span>

    ![สกรีนช็อตของตัวเลือกแผนภูมิตัววัด](media/power-bi-visualization-radial-gauge-charts/power-bi-gauge-axis.png)

1. <span data-ttu-id="72e7d-171">ล้างตัวเลือก **COGS** ในบานหน้าต่าง **เขตข้อมูล** เพื่อนำค่าเป้าหมายออก</span><span class="sxs-lookup"><span data-stu-id="72e7d-171">Clear the **COGS** option in the **Fields** pane to remove the target value.</span></span>

    ![สกรีนช็อตของตัวเลือกการล้าง COGS](media/power-bi-visualization-radial-gauge-charts/pbi-remove-target.png)

1. <span data-ttu-id="72e7d-173">เมื่อเขตข้อมูล **เป้าหมาย** ปรากฏภายใต้ **แกนตัววัด** ให้ใส่ค่า</span><span class="sxs-lookup"><span data-stu-id="72e7d-173">When the **Target** field appears under **Gauge axis**, enter a value.</span></span>

     ![สกรีนช็อตของการเรียกตัวเลือกแกนวัดที่มีเป้าหมายออกมา](media/power-bi-visualization-radial-gauge-charts/power-bi-gauge-target.png)

1. <span data-ttu-id="72e7d-175">จัดรูปแบบแผนภูมหน้าปัดต่อไป ก็สามารถทำได้</span><span class="sxs-lookup"><span data-stu-id="72e7d-175">Optionally, continue formatting your gauge chart.</span></span>

<span data-ttu-id="72e7d-176">เมื่อคุณทำเสร็จแล้วทำตามขั้นตอนเหล่านี้ คุณจะมีแผนภูมิตัววัดที่มีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="72e7d-176">Once you're done with these steps, you'll have a gauge chart that looks something like this:</span></span>

![สกรีนช็อตของแผนภูมิตัววัดสุดท้าย](media/power-bi-visualization-radial-gauge-charts/power-bi-final.png)

## <a name="next-step"></a><span data-ttu-id="72e7d-178">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="72e7d-178">Next step</span></span>

* [<span data-ttu-id="72e7d-179">Key Performance Indicator (KPI) วิชวล</span><span class="sxs-lookup"><span data-stu-id="72e7d-179">Key Performance Indicator (KPI) visuals</span></span>](power-bi-visualization-kpi.md)

* [<span data-ttu-id="72e7d-180">ชนิดการแสดงภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="72e7d-180">Visualization types in Power BI</span></span>](power-bi-visualization-types-for-reports-and-q-and-a.md)

<span data-ttu-id="72e7d-181">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="72e7d-181">More questions?</span></span> [<span data-ttu-id="72e7d-182">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="72e7d-182">Try the Power BI Community</span></span>](https://community.powerbi.com/)

