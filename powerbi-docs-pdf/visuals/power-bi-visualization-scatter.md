---
title: แผนภูมิกระจาย แผนภูมิฟองอากาศ และแผนภูมิลงจุดใน Power BI
description: แผนภูมิกระจาย แผนภูมิลงจุด และแผนภูมิฟองอากาศใน Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
featuredvideoid: ''
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 11/21/2019
LocalizationGroup: Visualizations
ms.openlocfilehash: 4fe8d7c4333c6c540a70c33fdd3e5f4747d347da
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418865"
---
# <a name="scatter-charts-bubble-charts-and-dot-plot-charts-in-power-bi"></a><span data-ttu-id="8b00b-103">แผนภูมิกระจาย แผนภูมิฟองอากาศ และแผนภูมิลงจุดใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8b00b-103">Scatter charts, bubble charts, and dot plot charts in Power BI</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="8b00b-104">แผนภูมิกระจายจะมีแกนค่าสองแกนเสมอเพื่อแสดงข้อมูลตัวเลขหนึ่งชุดตามแกนแนวนอนและอีกชุดของค่าตัวเลขตามแกนแนวตั้ง</span><span class="sxs-lookup"><span data-stu-id="8b00b-104">A scatter chart always has two value axes to show: one set of numerical data along a horizontal axis and another set of numerical values along a vertical axis.</span></span> <span data-ttu-id="8b00b-105">แผนภูมิแสดงจุดที่จุดตัดของค่าตัวเลข x และ y เพื่อรวมค่าเหล่านี้ลงในจุดข้อมูลเดียว</span><span class="sxs-lookup"><span data-stu-id="8b00b-105">The chart displays points at the intersection of an x and y numerical value, combining these values into single data points.</span></span> <span data-ttu-id="8b00b-106">Power BI อาจกระจายจุดข้อมูลสม่ำเสมอกันหรืออาจไม่สม่ำเสมอกันตามแกนแนวนอน</span><span class="sxs-lookup"><span data-stu-id="8b00b-106">Power BI may distribute these data points evenly or unevenly across the horizontal axis.</span></span> <span data-ttu-id="8b00b-107">ขึ้นอยู่กับข้อมูลที่แสดงในแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="8b00b-107">It depends on the data the chart represents.</span></span>

<span data-ttu-id="8b00b-108">คุณสามารถตั้งค่าจำนวนของจุดข้อมูลได้สูงสุดถึง 10,000 จุด</span><span class="sxs-lookup"><span data-stu-id="8b00b-108">You can set the number of data points, up to a maximum of 10,000.</span></span>  

## <a name="when-to-use-a-scatter-chart-bubble-chart-or-a-dot-plot-chart"></a><span data-ttu-id="8b00b-109">เมื่อต้องใช้แผนภูมิกระจายหรือแผนภูมิฟองอากาศหรือแผนภูมิการลงจุด</span><span class="sxs-lookup"><span data-stu-id="8b00b-109">When to use a scatter chart, bubble chart, or a dot plot chart</span></span>

### <a name="scatter-and-bubble-charts"></a><span data-ttu-id="8b00b-110">แผนภูมิกระจายและแผนภูมิฟอง</span><span class="sxs-lookup"><span data-stu-id="8b00b-110">Scatter and bubble charts</span></span>

<span data-ttu-id="8b00b-111">แผนภูมิกระจายแสดงความสัมพันธ์ระหว่างสองค่าตัวเลข</span><span class="sxs-lookup"><span data-stu-id="8b00b-111">A scatter chart shows the relationship between two numerical values.</span></span> <span data-ttu-id="8b00b-112">แผนภูมิฟองอากาศจะแทนที่จุดข้อมูลด้วยฟองอากาศ และ *ขนาด* ของฟองอากาศแสดงข้อมูลสามมิติเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8b00b-112">A bubble chart replaces data points with bubbles, with the bubble *size* representing an additional third data dimension.</span></span>

![สกรีนช็อตของตัวอย่างแผนภูมิฟอง](media/power-bi-visualization-scatter/power-bi-bubble-chart.png)

<span data-ttu-id="8b00b-114">แผนภูมิกระจายเป็นตัวเลือกที่ดีที่สุด:</span><span class="sxs-lookup"><span data-stu-id="8b00b-114">Scatter charts are a great choice:</span></span>

* <span data-ttu-id="8b00b-115">ในการแสดงความสัมพันธ์ระหว่างค่าตัวเลขสองค่า</span><span class="sxs-lookup"><span data-stu-id="8b00b-115">To show relationships between two numerical values.</span></span>

* <span data-ttu-id="8b00b-116">ในการทำผังตัวเลขสองกลุ่มให้เป็นหนึ่งชุดข้อมูลของพิกัด X และ Y</span><span class="sxs-lookup"><span data-stu-id="8b00b-116">To plot two groups of numbers as one series of x and y coordinates.</span></span>

* <span data-ttu-id="8b00b-117">แทนที่จะใช้เป็นแผนภูมิเส้นเมื่อคุณต้องการเปลี่ยนมาตราส่วนของแกนแนวนอน</span><span class="sxs-lookup"><span data-stu-id="8b00b-117">To use instead of a line chart when you want to change the scale of the horizontal axis.</span></span>

* <span data-ttu-id="8b00b-118">เมื่อต้องเปลี่ยนแกนแนวนอนเป็นมาตราส่วนลอการิทึม</span><span class="sxs-lookup"><span data-stu-id="8b00b-118">To turn the horizontal axis into a logarithmic scale.</span></span>

* <span data-ttu-id="8b00b-119">เมื่อต้องการแสดงข้อมูลในแผ่นงานซึ่งรวมถึงชุดค่าที่เป็นคู่หรือเป็นกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="8b00b-119">To display worksheet data that includes pairs or grouped sets of values.</span></span>

    > [!TIP]
    > <span data-ttu-id="8b00b-120">ในแผนภูมิกระจาย คุณสามารถปรับระดับอิสระของแกนเพื่อเผยให้เห็นข้อมูลเพิ่มเติมเกี่ยวกับค่าที่จัดกลุ่มได้</span><span class="sxs-lookup"><span data-stu-id="8b00b-120">In a scatter chart, you can adjust the independent scales of the axes to reveal more information about the grouped values.</span></span>

* <span data-ttu-id="8b00b-121">การแสดงรูปแบบสำหรับชุดข้อมูลจำนวนมากตัวอย่างเช่น โดยการแสดงแนวโน้มแบบเส้นตรง หรือที่ไม่ใช่เชิงเส้น แบบกลุ่ม และนอกขอบเขต</span><span class="sxs-lookup"><span data-stu-id="8b00b-121">To show patterns in large sets of data, for example by showing linear or non-linear trends, clusters, and outliers.</span></span>

* <span data-ttu-id="8b00b-122">เพื่อเปรียบเทียบตัวเลขขนาดใหญ่ของจุดข้อมูลโดยไม่คำนึงถึงเวลา</span><span class="sxs-lookup"><span data-stu-id="8b00b-122">To compare large numbers of data points without regard to time.</span></span>  <span data-ttu-id="8b00b-123">ยิ่งคุณใส่ข้อมูลเพิ่มเติมในแผนภูมิกระจายมากเท่าไหร่ คุณยิ่งสามารถทำการเปรียบเทียบได้ดีเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8b00b-123">The more data that you include in a sScatter chart, the better the comparisons that you can make.</span></span>

<span data-ttu-id="8b00b-124">นอกเหนือจากสิ่งที่แผนภูมิกระจายสามารถให้คุณได้ แผนภูมิฟองถือเป็นตัวเลือกที่ดี:</span><span class="sxs-lookup"><span data-stu-id="8b00b-124">In addition to what Scatter charts can do for you, bubble charts are a great choice:</span></span>

* <span data-ttu-id="8b00b-125">ถ้าข้อมูลของคุณมีชุดข้อมูล 3 ชุดที่แต่ละชุดประกอบด้วยชุดของค่า</span><span class="sxs-lookup"><span data-stu-id="8b00b-125">If your data has three data series that each contains a set of values.</span></span>

* <span data-ttu-id="8b00b-126">การนำเสนอข้อมูลทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8b00b-126">To present financial data.</span></span>  <span data-ttu-id="8b00b-127">ฟองอากาศที่มีขนาดแตกต่างกันเป็นประโยชน์สำหรับการเน้นให้เห็นค่าเฉพาะบางค่า</span><span class="sxs-lookup"><span data-stu-id="8b00b-127">Different bubble sizes are useful to visually emphasize specific values.</span></span>

* <span data-ttu-id="8b00b-128">การใช้กับจตุภาค</span><span class="sxs-lookup"><span data-stu-id="8b00b-128">To use with quadrants.</span></span>

### <a name="dot-plot-charts"></a><span data-ttu-id="8b00b-129">แผนภูมิการลงจุด</span><span class="sxs-lookup"><span data-stu-id="8b00b-129">Dot plot charts</span></span>

<span data-ttu-id="8b00b-130">แผนภูมิลงจุดนั้นเหมือนกันกับแผนภูมิฟองอากาศและแผนภูมิกระจาย แต่จะใช้เพื่อลงข้อมูลเชิงหมวดหมู่ตามแกน X</span><span class="sxs-lookup"><span data-stu-id="8b00b-130">A dot plot chart is similar to a bubble chart and scatter chart, but is instead used to plot categorical data along the X-Axis.</span></span>

![สกรีนช็อตของแผนภูมิการลงจุด](media/power-bi-visualization-scatter/power-bi-dot-plot.png)

<span data-ttu-id="8b00b-132">แผนภูมิการลงจุดเป็นตัวเลือกที่ดีในกรณีที่คุณต้องการลงข้อมูลเชิงหมวดหมู่ที่แกน X ด้วย</span><span class="sxs-lookup"><span data-stu-id="8b00b-132">They're a great choice if you want to include categorical data along the X-Axis.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8b00b-133">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="8b00b-133">Prerequisites</span></span>

<span data-ttu-id="8b00b-134">บทช่วยสอนนี้ใช้[ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix)</span><span class="sxs-lookup"><span data-stu-id="8b00b-134">This tutorial uses the [Retail Analysis sample PBIX file](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix).</span></span>

1. <span data-ttu-id="8b00b-135">จากด้านบนซ้ายของแถบเมนู เลือก **ไฟล์** > **เปิด**</span><span class="sxs-lookup"><span data-stu-id="8b00b-135">From the upper left section of the menubar, select **File** > **Open**</span></span>
   
2. <span data-ttu-id="8b00b-136">ค้นหาสำเนา **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก**</span><span class="sxs-lookup"><span data-stu-id="8b00b-136">Find your copy of the **Retail Analysis sample PBIX file**</span></span>

1. <span data-ttu-id="8b00b-137">เปิด **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก** ในมุมมองรายงาน ![ภาพหน้าจอไอคอนมุมมองรายงาน](media/power-bi-visualization-kpi/power-bi-report-view.png)</span><span class="sxs-lookup"><span data-stu-id="8b00b-137">Open the **Retail Analysis sample PBIX file** in report view ![Screenshot of the report view icon.](media/power-bi-visualization-kpi/power-bi-report-view.png).</span></span>

1. <span data-ttu-id="8b00b-138">เลือก</span><span class="sxs-lookup"><span data-stu-id="8b00b-138">Select</span></span> ![สกรีนช็อตของแท็บสีเหลือง](media/power-bi-visualization-kpi/power-bi-yellow-tab.png) <span data-ttu-id="8b00b-140">หากต้องการเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="8b00b-140">to add a new page.</span></span>

> [!NOTE]
> <span data-ttu-id="8b00b-141">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="8b00b-141">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span>    

## <a name="create-a-scatter-chart"></a><span data-ttu-id="8b00b-142">สร้างแผนภูมิกระจาย</span><span class="sxs-lookup"><span data-stu-id="8b00b-142">Create a scatter chart</span></span>

1. <span data-ttu-id="8b00b-143">เริ่มจากหน้ารายงานเปล่า และจากแถบคำสั่ง **เขตข้อมูล** เลือกเขตข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8b00b-143">Start on a blank report page and from the **Fields** pane, select these fields:</span></span>

    * <span data-ttu-id="8b00b-144">**ยอดขาย** > **ยอดขายต่อตารางฟุต**</span><span class="sxs-lookup"><span data-stu-id="8b00b-144">**Sales** > **Sales Per Sq Ft**</span></span>

    * <span data-ttu-id="8b00b-145">**ยอดขาย** > **ร้อยละผลต่างยอดขายรวม**</span><span class="sxs-lookup"><span data-stu-id="8b00b-145">**Sales** > **Total Sales Variance %**</span></span>

    * <span data-ttu-id="8b00b-146">**เขต** > **เขต**</span><span class="sxs-lookup"><span data-stu-id="8b00b-146">**District** > **District**</span></span>

    ![สกรีนช็อตของแผนภูมิคอลัมน์คลัสเตอร์ บานหน้าต่างการแสดงภาพ และบานหน้าต่างเขตข้อมูลกับเขตข้อมูลที่คุณเลือกเรียกดู](media/power-bi-visualization-scatter/power-bi-bar-chart.png)

1. <span data-ttu-id="8b00b-148">ในพื้นที่ **การแสดงภาพ** เลือก![ไอคอนสกรีนช็อตแผนภูมิกระจาย](media/power-bi-visualization-scatter/power-bi-scatter-chart-icon.png)</span><span class="sxs-lookup"><span data-stu-id="8b00b-148">In the **Visualization** pane, select  ![Screenshot of the scatter chart icon.](media/power-bi-visualization-scatter/power-bi-scatter-chart-icon.png)</span></span> <span data-ttu-id="8b00b-149">เมื่อต้องแปลงแผนภูมิคอลัมน์คลัสเตอร์เป็นแผนภูมิกระจาย</span><span class="sxs-lookup"><span data-stu-id="8b00b-149">to convert the cluster column chart to a scatter chart.</span></span>

   ![สกรีนชอตของแผนภูมิคอลัมน์คลัสเตอร์กลายเป็นแผนภูมิกระจาย](media/power-bi-visualization-scatter/power-bi-scatter-new.png)

1. <span data-ttu-id="8b00b-151">ลาก **เขต** จาก **รายละเอียด** ไปยัง **คำอธิบายแผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="8b00b-151">Drag **District** from **Details** to **Legend**.</span></span>

    <span data-ttu-id="8b00b-152">Power BI จะแสดงแผนภูมิกระจายที่ทำผัง **ร้อยละผลต่างของยอดขายรวม** ตามแกน Y และทำผัง **ยอดขายต่อตารางฟุต** บนแกน X</span><span class="sxs-lookup"><span data-stu-id="8b00b-152">Power BI displays a scatter chart that plots **Total Sales Variance %** along the Y-Axis, and plots **Sales Per Square Feet** along the X-Axis.</span></span> <span data-ttu-id="8b00b-153">จุดสีข้อมูลแสดงถึงเขตต่าง ๆ:</span><span class="sxs-lookup"><span data-stu-id="8b00b-153">The data point colors represent districts:</span></span>

    ![สกรีนช็อตของแผนภูมิกระจาย](media/power-bi-visualization-scatter/power-bi-scatter2.png)

<span data-ttu-id="8b00b-155">ตอนนี้เรามาเพิ่มมิติที่สามกัน</span><span class="sxs-lookup"><span data-stu-id="8b00b-155">Now let's add a third dimension.</span></span>

## <a name="create-a-bubble-chart"></a><span data-ttu-id="8b00b-156">สร้างแผนภูมิฟองอากาศ</span><span class="sxs-lookup"><span data-stu-id="8b00b-156">Create a bubble chart</span></span>

1. <span data-ttu-id="8b00b-157">จากช่อง **ข้อมูล** ลาก **ยอดขาย** > **ค่ายอดขายของปีนี้** > **ไปยัง** พื้นที่ **ขนาด**</span><span class="sxs-lookup"><span data-stu-id="8b00b-157">From the **Fields** pane, drag **Sales** > **This Year Sales** > **Value** to the **Size** well.</span></span> <span data-ttu-id="8b00b-158">จุดข้อมูลขยายไปยังปริมาณที่เป็นสัดส่วนกันกับมูลค่ายอดขาย</span><span class="sxs-lookup"><span data-stu-id="8b00b-158">The data points expand to volumes proportionate with the sales value.</span></span>

   ![สกรีนช็อตของแผนภูมิกระจายให้กลายเป็นแผนภูมิฟอง โดยการเพิ่ม Sale Vale ให้เป็น Size well](media/power-bi-visualization-scatter/power-bi-scatter-chart-size.png)

1. <span data-ttu-id="8b00b-160">เลื่อนไปเหนือฟองอากาศ</span><span class="sxs-lookup"><span data-stu-id="8b00b-160">Hover over a bubble.</span></span> <span data-ttu-id="8b00b-161">ขนาดของฟองอากาศแสดงค่าของ **ยอดขายของปีนี้**</span><span class="sxs-lookup"><span data-stu-id="8b00b-161">The size of the bubble reflects the value of **This Year Sales**.</span></span>

    ![หน้าแสดงเคล็ดลับเครื่องมือ](media/power-bi-visualization-scatter/pbi-scatter-chart-hover.png)

1. <span data-ttu-id="8b00b-163">ในการตั้งค่าจำนวนของจุดข้อมูลที่จะแสดงในแผนภูมิฟองอากาศ ในหัวข้อ **รูปแบบ** ของพื้นที่การ **แสดงภาพ** ขยาย **ทั่วไป** และปรับ **ปริมาณข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="8b00b-163">To set the number of data points to show in your bubble chart, in the **Format** section of the **Visualizations** pane, expand **General**, and adjust the **Data Volume**.</span></span>

    ![สกรีนช็อตของการเรียกใช้งานบานหน้าต่างการแสดงภาพด้วยไอคอนรูปแบบ เมนูดรอปดาวน์ทั่วไป และตัวเลือกไดรฟ์ข้อมูล](media/power-bi-visualization-scatter/pbi-scatter-data-volume.png)

    <span data-ttu-id="8b00b-165">คุณสามารถตั้งค่าปริมาณข้อมูลสูงสุดเป็นตัวเลขใด ๆ จนถึง 10,000</span><span class="sxs-lookup"><span data-stu-id="8b00b-165">You can set the max data volume to any number up to 10,000.</span></span> <span data-ttu-id="8b00b-166">เมื่อคุณใช้ตัวเลขที่สูงขึ้น เราแนะนำให้ทดสอบก่อนเพื่อให้แน่ใจว่ายังมีประสิทธิภาพที่ดี</span><span class="sxs-lookup"><span data-stu-id="8b00b-166">As you get into the higher numbers, we suggest testing first to ensure good performance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8b00b-167">จุดข้อมูลเพิ่มอาจหมายถึงเวลาการโหลดที่นานขึ้น</span><span class="sxs-lookup"><span data-stu-id="8b00b-167">More data points can mean a longer loading time.</span></span> <span data-ttu-id="8b00b-168">ถ้าคุณเลือกที่จะเผยแพร่รายงาน ด้วยขีดจำกัดที่สูงกว่าจุดสิ้นสุดของสเกล คุณต้องแน่ใจว่าได้ทดสอบลางรายงานผลของคุณไปทั่วทั้งเว็บ และอุปกรณ์เคลื่อนที่แล้ว</span><span class="sxs-lookup"><span data-stu-id="8b00b-168">If you do choose to publish reports with limits at the higher end of the scale, make sure to test out your reports across the web and mobile as well.</span></span> <span data-ttu-id="8b00b-169">คุณต้องการยืนยันว่า ประสิทธิภาพการทำงานของแผนภูมิตรงกับความคาดหวังของผู้ใช้งานของคุณ</span><span class="sxs-lookup"><span data-stu-id="8b00b-169">You want to confirm that the performance of the chart matches your users' expectations.</span></span>

1. <span data-ttu-id="8b00b-170">จัดรูปแบบสี ป้ายชื่อ ชื่อเรื่อง พื้นหลัง และอื่น ๆ ของการแสดงภาพต่อไป</span><span class="sxs-lookup"><span data-stu-id="8b00b-170">Continue formatting the visualization colors, labels, titles, background, and more.</span></span> <span data-ttu-id="8b00b-171">การ[ปรับปรุงการเข้าถึง](../create-reports/desktop-accessibility-overview.md) ให้พิจารณาเพิ่มรูปร่างเครื่องหมายไปยังแต่ละบรรทัด</span><span class="sxs-lookup"><span data-stu-id="8b00b-171">To [improve accessibility](../create-reports/desktop-accessibility-overview.md), consider adding marker shapes to each line.</span></span> <span data-ttu-id="8b00b-172">การเลือกรูปร่างเครื่องหมาย ขยาย **รูปร่าง** เลือก **รูปร่างตัวทำเครื่องหมาย** แล้วจึงเลือกรูปร่าง</span><span class="sxs-lookup"><span data-stu-id="8b00b-172">To select the marker shape, expand **Shapes**, select **Marker shape**, and select a shape.</span></span>

    ![สกรีนช็อตของการเรียกรูปร่างรายการดรอปดาวน์พร้อมกับตัวเลือกรูปร่างตัวทำเครื่องหมายออกมา](media/power-bi-visualization-scatter/pbi-scatter-marker.png)

    <span data-ttu-id="8b00b-174">เปลี่ยนรูปร่างเครื่องหมายเป็นข้าวหลามตัด สามเหลี่ยม หรือสี่เหลี่ยมจัตุรัส</span><span class="sxs-lookup"><span data-stu-id="8b00b-174">Change the marker shape to a diamond, triangle, or square.</span></span> <span data-ttu-id="8b00b-175">ใช้รูปร่างเครื่องหมายที่แตกต่างกันสำหรับแต่ละเส้น ทำให้ง่ายสำหรับผู้บริโภครายงาน เพื่อแยกแยะเส้น (หรือพื้นที่) ออกจากกัน</span><span class="sxs-lookup"><span data-stu-id="8b00b-175">Using a different marker shape for each line makes it easier for report consumers to differentiate lines (or areas) from each other.</span></span>

1. <span data-ttu-id="8b00b-176">เปิดบานหน้าต่างการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="8b00b-176">Open the Analytics pane</span></span> ![สกรีนช็อตของไอคอนสำหรับบานหน้าต่างการวิเคราะห์](media/power-bi-visualization-scatter/power-bi-analytics.png) <span data-ttu-id="8b00b-178">เพื่อเพิ่มข้อมูลเพิ่มเติมลงในการแสดงภาพของคุณ</span><span class="sxs-lookup"><span data-stu-id="8b00b-178">to add additional information to your visualization.</span></span>  
    - <span data-ttu-id="8b00b-179">เพิ่มเส้นมัธยฐาน</span><span class="sxs-lookup"><span data-stu-id="8b00b-179">Add a Median line.</span></span> <span data-ttu-id="8b00b-180">เลือก **เส้นมัธยฐาน** > **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="8b00b-180">Select **Median line** > **Add**.</span></span> <span data-ttu-id="8b00b-181">ตามค่าเริ่มต้น Power BI จะเพิ่มเส้นมัธยฐานสำหรับ *ยอดขายต่อตารางฟุต* การดำเนินการนี้ไม่ค่อยมีประโยชน์เนื่องจากเราเห็นว่ามีจุดข้อมูล 10 จุด และรู้ว่าค่ามัธยฐานจะถูกสร้างขึ้นด้วยจุดข้อมูลห้าจุดในแต่ละด้าน</span><span class="sxs-lookup"><span data-stu-id="8b00b-181">By default, Power BI adds a median line for *Sales per sq ft*. This isn't very helpful since we can see that there are 10 data points and know that the median will be created with five data points on each side.</span></span> <span data-ttu-id="8b00b-182">ให้เปลี่ยน **หน่วยวัด** เป็น *% ผลต่างของยอดขายทั้งหมด* แทน</span><span class="sxs-lookup"><span data-stu-id="8b00b-182">Instead, switch the **Measure** to *Total sales variance %*.</span></span>  

        ![สกรีนช็อตของแผนภูมิฟองที่มีการเพิ่มเส้นมัธยฐาน](media/power-bi-visualization-scatter/power-bi-analytics-median.png)

    - <span data-ttu-id="8b00b-184">เพิ่มแรเงาสมมาตรเพื่อแสดงจุดที่มีค่าสูงกว่าของหน่วยวัดแกน x เมื่อเทียบกับหน่วยวัดแกน y ในทางกลับกัน</span><span class="sxs-lookup"><span data-stu-id="8b00b-184">Add symmetry shading to show which points have a higher value of the x-axis measure compared to the y-axis measure, and vice-versa.</span></span> <span data-ttu-id="8b00b-185">เมื่อคุณเปิดการแรเงาสมมาตรในบานหน้าต่างการวิเคราะห์ Power BI จะแสดงพื้นหลังของแผนภูมิกระจายของคุณแบบสมมาตรตามขอบเขตด้านบนและด้านล่างของแกนปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="8b00b-185">When you turn symmetry shading on in the Analytics pane, Power BI shows you the background of your scatter chart symmetrically based on your current axis upper and lower boundaries.</span></span> <span data-ttu-id="8b00b-186">วิธีการนี้เป็นวิธีที่รวดเร็วมากในการระบุแกนใดที่วัดจุดข้อมูลที่เน้น โดยเฉพาะอย่างยิ่งเมื่อคุณมีช่วงแกนที่แตกต่างกันสำหรับแกน x และ y ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8b00b-186">This is a very quick way to identify which axis measure a data point favors, especially when you have a different axis range for your x- and y-axis.</span></span>

        <span data-ttu-id="8b00b-187">a.</span><span class="sxs-lookup"><span data-stu-id="8b00b-187">a.</span></span> <span data-ttu-id="8b00b-188">เปลี่ยน **% ผลต่างของยอดขายรวม** เป็น **% กำไรขั้นต้นของปีที่แล้ว**</span><span class="sxs-lookup"><span data-stu-id="8b00b-188">Change the **Total sales variance %** field to **Gross margin last year %**</span></span>

        ![สกรีนช็อตของรายละเอียดที่มีการเลือกเปอร์เซ็นต์อัตรากำไรขั้นต้นของปีที่แล้ว](media/power-bi-visualization-scatter/power-bi-format-symmetry.png)

        <span data-ttu-id="8b00b-190">b.</span><span class="sxs-lookup"><span data-stu-id="8b00b-190">b.</span></span> <span data-ttu-id="8b00b-191">จากบานหน้าต่างการวิเคราะห์ เพิ่ม **แรเงาสมมาตร**</span><span class="sxs-lookup"><span data-stu-id="8b00b-191">From the Analytics pane, add **Symmetry shading**.</span></span> <span data-ttu-id="8b00b-192">เราสามารถดูจากการแรเงาที่ร้านขายเครื่องถุงเท้า (ฟองสีเขียวในพื้นที่แรเงาสีชมพู) เป็นประเภทเดียวที่เน้นกำไรขั้นต้นแทนที่ยอดขายต่อตารางฟุตของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="8b00b-192">We can see from the shading that Hosiery (the green bubble in the pink shaded area) is the only category that favors  gross margin rather than its sales per store square footage.</span></span> 

        ![สกรีนช็อตของแผนภูมิฟองที่มีการเพิ่มแรเงาสมมาตร](media/power-bi-visualization-scatter/power-bi-symmetry.png)

    - <span data-ttu-id="8b00b-194">สำรวจบานหน้าต่างการวิเคราะห์เพื่อค้นหาข้อมูลเชิงลึกที่น่าสนใจในข้อมูลของคุณต่อไป</span><span class="sxs-lookup"><span data-stu-id="8b00b-194">Continue exploring the Analytics pane to discover interesting insights in your data.</span></span> 

        ![สกรีนช็อตของบานหน้าต่างการวิเคราะห์](media/power-bi-visualization-scatter/power-bi-analytics-example.png)

## <a name="create-a-dot-plot-chart"></a><span data-ttu-id="8b00b-196">สร้างแผนภูมิการลงจุด</span><span class="sxs-lookup"><span data-stu-id="8b00b-196">Create a dot plot chart</span></span>

<span data-ttu-id="8b00b-197">เมื่อต้องการสร้างแผนภูมิการลงจุดให้แทนที่เขตข้อมูล **แกน X** เชิงตัวเลขด้วยเขตข้อมูลเชิงหมวดหมู่</span><span class="sxs-lookup"><span data-stu-id="8b00b-197">To create a dot plot chart, replace the numerical **X-Axis** field with a categorical field.</span></span>

<span data-ttu-id="8b00b-198">จากแผง **แกน X** ให้ลบ **ยอดขายต่อตารางฟุต** และแทนที่ด้วย **เขต**  > **ตัวจัดการเขต**</span><span class="sxs-lookup"><span data-stu-id="8b00b-198">From the **X-Axis** pane, remove **Sales per sq ft** and replace it with **District** > **District Manager**.</span></span>

![สกรีนช็อตของแผนภูมิการลงจุดใหม่](media/power-bi-visualization-scatter/power-bi-dot-plot-squares.png)

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="8b00b-200">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="8b00b-200">Considerations and troubleshooting</span></span>

### <a name="your-scatter-chart-has-only-one-data-point"></a><span data-ttu-id="8b00b-201">แผนภูมิกระจายของคุณมีจุดข้อมูลเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8b00b-201">Your scatter chart has only one data point</span></span>

<span data-ttu-id="8b00b-202">แผนภูมิกระจายของคุณที่มีจุดข้อมูลเดียวเท่านั้น เป็นแผนภูมิที่รวมค่าทั้งหมดบนแกน X และ Y หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="8b00b-202">Does your scatter chart have only one data point that aggregates all the values on the X- and Y-axes?</span></span>  <span data-ttu-id="8b00b-203">หรืออาจเป็นแผนภูมิที่รวมค่าทั้งหมดตามเส้นแนวนอนหรือแนวตั้งเดียว?</span><span class="sxs-lookup"><span data-stu-id="8b00b-203">Or maybe it aggregates all the values along a single horizontal or vertical line?</span></span>

![สกรีนช็อตของแผนภูมิกระจายที่มีข้อมูลจุดเพียงจุดเดียว](media/power-bi-visualization-scatter/pbi-scatter-tshoot1.png)

<span data-ttu-id="8b00b-205">เพิ่มเขตข้อมูลไปยัง **รายละเอียด** ได้ดีเพื่อที่จะบอกวิธีการจัดกลุ่มค่า Power BI</span><span class="sxs-lookup"><span data-stu-id="8b00b-205">Add a field to the **Details** well to tell Power BI how to group the values.</span></span> <span data-ttu-id="8b00b-206">ช่องข้อมูลต้องไม่ซ้ำกันสำหรับแต่ละจุดที่คุณต้องการลรทำผัง</span><span class="sxs-lookup"><span data-stu-id="8b00b-206">The field must be unique for each point you want to plot.</span></span> <span data-ttu-id="8b00b-207">เตัวเลขแถวอย่างง่ายหรือช่องข้อมูล ID ที่จะสามารถทำได้</span><span class="sxs-lookup"><span data-stu-id="8b00b-207">A simple row number or ID field will do.</span></span>

![สกรีนช็อตของแผนภูมิกระจาย มี RowNum ถูกเพิ่มไปยังรายละเอียดได้ดี](media/power-bi-visualization-scatter/pbi-scatter-tshoot.png)

<span data-ttu-id="8b00b-209">ถ้าคุณไม่มีในข้อมูลของคุณ ให้สร้างช่องข้อมูลที่รวมค่า X และ Y เข้าด้วยกันลงในสิ่งที่ไม่ซ้ำกันสำหรับแต่ละจุด:</span><span class="sxs-lookup"><span data-stu-id="8b00b-209">If you don't have that in your data, create a field that concatenates your X and Y values together into something unique per point:</span></span>

![สกรีนช็อตของแผนภูมิกระจาย มี TempTime ถูกเพิ่มไปยังรายละเอียดได้ดี](media/power-bi-visualization-scatter/pbi-scatter-tshoot2.png)

<span data-ttu-id="8b00b-211">การสร้างเขตข้อมูลใหม่[ใช้ตัวแก้ไขแบบสอบถามของ Power BI Desktop เพืื่อเพิ่มคอลัมน์ดัชนี](../create-reports/desktop-add-custom-column.md)ไปยังชุดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="8b00b-211">To create a new field, [use the Power BI Desktop Query Editor to add an Index Column](../create-reports/desktop-add-custom-column.md) to your dataset.</span></span> <span data-ttu-id="8b00b-212">จากนั้นเพิ่มคอลัมน์นี้ไปยังพื้นที่การแสดงภาพ **รายละเอียด** ของคุณได้ดี</span><span class="sxs-lookup"><span data-stu-id="8b00b-212">Then add this column to your visualization's **Details** well.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8b00b-213">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="8b00b-213">Next steps</span></span>

<span data-ttu-id="8b00b-214">คุณอาจสนใจบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8b00b-214">You might also be interested in the following articles:</span></span>

* [<span data-ttu-id="8b00b-215">การสุ่มตัวอย่างความหนาแน่นสูงในแผนภูมิกระจาย Power BI</span><span class="sxs-lookup"><span data-stu-id="8b00b-215">High-density sampling in Power BI scatter charts</span></span>](../create-reports/desktop-high-density-scatter-charts.md)
* [<span data-ttu-id="8b00b-216">ชนิดการแสดงภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8b00b-216">Visualization types in Power BI</span></span>](power-bi-visualization-types-for-reports-and-q-and-a.md)
* [<span data-ttu-id="8b00b-217">เคล็ดลับในการเรียงลำดับและเผยแพร่แผนพลอตข้อมูลในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="8b00b-217">Tips to sort and distribute data plots in Power BI reports</span></span>](../guidance/report-tips-sort-distribute-data-plots.md)

<span data-ttu-id="8b00b-218">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8b00b-218">More questions?</span></span> [<span data-ttu-id="8b00b-219">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="8b00b-219">Try the Power BI Community</span></span>](https://community.powerbi.com/)
