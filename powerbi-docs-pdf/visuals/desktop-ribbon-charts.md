---
title: ใช้แผนภูมิ ribbon ใน Power BI
description: สร้างและใชแผนภูมิริบบอนในบริการ Power BI Desktop
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 05/05/2019
LocalizationGroup: Visualizations
ms.openlocfilehash: 9fea98f30403d9325ed2c6826418220cdd29ade8
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96397646"
---
# <a name="create-ribbon-charts-in-power-bi"></a><span data-ttu-id="d53ea-103">ใช้แผนภูมิแถบริบบอนใน Power BI</span><span class="sxs-lookup"><span data-stu-id="d53ea-103">Create ribbon charts in Power BI</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]    

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="d53ea-104">คุณสามารถสร้างแผนภูมิแถบริบบอนเพื่อแสดงภาพข้อมูล และค้นหาได้อย่างรวดเร็วว่าข้อมูลประเภทใดมีอันดับสูงสุด (มีค่ามากที่สุด) ได้</span><span class="sxs-lookup"><span data-stu-id="d53ea-104">You can create ribbon charts to visualize data, and quickly discover which data category has the highest rank (largest value).</span></span> <span data-ttu-id="d53ea-105">แผนภูมิ Ribbon เหมาะกับการแสดงการเปลี่ยนแปลงอันดับ โดยที่ค่าอันดับสูงสุดจะแสดงอยู่ด้านบนสุดของแต่ละช่วงเวลาเสมอ</span><span class="sxs-lookup"><span data-stu-id="d53ea-105">Ribbon charts are effective at showing rank change, with the highest range (value) always displayed on top for each time period.</span></span> 

![สกรีนช็อตแสดงแผนภูมิริบบอนพร้อมข้อมูลสำหรับเครื่องเสียงโทรศัพท์มือถือและหมวดหมู่อื่น ๆ ที่แสดงตามปีและไตรมาส](media/desktop-ribbon-charts/ribbon-charts-01.png)

> [!NOTE]
> <span data-ttu-id="d53ea-107">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="d53ea-107">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span> <span data-ttu-id="d53ea-108">ดู [การแชร์รายงาน](../collaborate-share/service-share-reports.md)</span><span class="sxs-lookup"><span data-stu-id="d53ea-108">See [sharing reports](../collaborate-share/service-share-reports.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d53ea-109">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="d53ea-109">Prerequisites</span></span>

<span data-ttu-id="d53ea-110">บทช่วยสอนนี้ใช้[ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix)</span><span class="sxs-lookup"><span data-stu-id="d53ea-110">This tutorial uses the [Retail Analysis sample PBIX file](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix).</span></span>

1. <span data-ttu-id="d53ea-111">จากด้านบนซ้ายของแถบเมนู เลือก **ไฟล์** > **เปิด**</span><span class="sxs-lookup"><span data-stu-id="d53ea-111">From the upper left section of the menubar, select **File** > **Open**</span></span>
   
2. <span data-ttu-id="d53ea-112">ค้นหาสำเนา **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก**</span><span class="sxs-lookup"><span data-stu-id="d53ea-112">Find your copy of the **Retail Analysis sample PBIX file**</span></span>

1. <span data-ttu-id="d53ea-113">เปิด **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก** ในมุมมองรายงาน ![ภาพหน้าจอไอคอนมุมมองรายงาน](media/power-bi-visualization-kpi/power-bi-report-view.png)</span><span class="sxs-lookup"><span data-stu-id="d53ea-113">Open the **Retail Analysis sample PBIX file** in report view ![Screenshot of the report view icon.](media/power-bi-visualization-kpi/power-bi-report-view.png).</span></span>

1. <span data-ttu-id="d53ea-114">เลือก</span><span class="sxs-lookup"><span data-stu-id="d53ea-114">Select</span></span> ![สกรีนช็อตของแท็บสีเหลือง](media/power-bi-visualization-kpi/power-bi-yellow-tab.png) <span data-ttu-id="d53ea-116">หากต้องการเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="d53ea-116">to add a new page.</span></span>

## <a name="create-a-ribbon-chart"></a><span data-ttu-id="d53ea-117">สร้างแผนภูมิ ribbon</span><span class="sxs-lookup"><span data-stu-id="d53ea-117">Create a ribbon chart</span></span>

1. <span data-ttu-id="d53ea-118">เพื่อสร้างแผนภูมิ Ribbon เลือก **แผนภูมิ Ribbon** จากแผง **การแสดงภาพ**</span><span class="sxs-lookup"><span data-stu-id="d53ea-118">To create a ribbon chart, select **Ribbon chart** from the **Visualizations** panel.</span></span>

    ![แม่แบบการแสดงผลด้วยภาพ](media/desktop-ribbon-charts/power-bi-template.png)

    <span data-ttu-id="d53ea-120">แผนภูมิ Ribbon เชื่อมต่อประเภทของข้อมูลผ่านช่วงเวลาที่แสดงภาพอย่างต่อเนื่องโดยใช้ Ribbon ให้คุณมองเห็นว่าแต่ละประเภทถูกจัดอันดับอย่างไรตลอดช่วงของแกน X ของแผนภูมิ (ซึ่งมักจะเป็นแกนเวลา)</span><span class="sxs-lookup"><span data-stu-id="d53ea-120">Ribbon charts connect a category of data over the visualized time continuum using ribbons, enabling you to see how a given category ranks throughout the span of the chart's x-axis (usually the timeline).</span></span>

2. <span data-ttu-id="d53ea-121">เลือกเขตข้อมูลสำหรับ **แกน**, **คำอธิบายแผนภูมิ** และ **ค่า**</span><span class="sxs-lookup"><span data-stu-id="d53ea-121">Select fields for **Axis**, **Legend**, and **Value**.</span></span>  <span data-ttu-id="d53ea-122">ในตัวอย่างนี้ เราได้เลือก: **จัดเก็บ** > **OpenDate**, **หมวดหมู่** > **รายการ** และ **ยอดขาย** > **ยอดขายปีนี้** > **มูลค่า**</span><span class="sxs-lookup"><span data-stu-id="d53ea-122">In this example, we've selected: **Store** > **OpenDate**, **Item** > **Category**, and **Sales** > **This year sales** > **Value**.</span></span>  

    ![เขตข้อมูลที่เลือก](media/desktop-ribbon-charts/power-bi-ribbon-values.png)

    <span data-ttu-id="d53ea-124">เนื่องจากชุดข้อมูลประกอบด้วยข้อมูลเพียงหนึ่งปีเท่านั้น เราจึงลบเขตข้อมูล **ปี** และ **ไตรมาส** ออกจาก **แกน**</span><span class="sxs-lookup"><span data-stu-id="d53ea-124">Since the dataset contains data for only one year, we removed the **Year** and **Quarter** field from the **Axis** well.</span></span>

3. <span data-ttu-id="d53ea-125">แผนภูมิริบบอนแสดงอันดับสำหรับทุกเดือน</span><span class="sxs-lookup"><span data-stu-id="d53ea-125">The ribbon chart shows rank for every month.</span></span> <span data-ttu-id="d53ea-126">สังเกตว่าอันดับมีการเปลี่ยนแปลงอย่างไรตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="d53ea-126">Notice how rank changes across time.</span></span> <span data-ttu-id="d53ea-127">ตัวอย่างเช่น ประเภทหน้าแรกย้ายจากลำดับที่สองไปยังที่ห้า จากเดือนกุมภาพันธ์ไปยังมีนาคม</span><span class="sxs-lookup"><span data-stu-id="d53ea-127">For example, the Home category moves from second to fifth from February to March.</span></span>

    ![สกรีนช็อตแสดงแผนภูมิริบบอนที่คุณสร้างขึ้นโดยมีการเรียกข้อมูลบางอย่างออกมา](media/desktop-ribbon-charts/power-bi-ribbon.png)

## <a name="format-a-ribbon-chart"></a><span data-ttu-id="d53ea-129">จัดรูปแบบแผนภูมิ ribbon</span><span class="sxs-lookup"><span data-stu-id="d53ea-129">Format a ribbon chart</span></span>
<span data-ttu-id="d53ea-130">เมื่อคุณสร้างแผนภูมิ ribbon คุณมีตัวเลือกจัดรูปแบบในส่วน **รูปแบบ** ของบานหน้าต่าง **แสดงภาพ**</span><span class="sxs-lookup"><span data-stu-id="d53ea-130">When you create a ribbon chart, you have formatting options available in the **Format** section of the **Visualizations** pane.</span></span> <span data-ttu-id="d53ea-131">ตัวเลือกจัดรูปแบบสำหรับแผนภูมิ ribbon จะคล้ายกับตัวเลือกสำหรับแผนภูมิคอลัมน์แบบเรียงซ้อน และมีตัวเลือกจัดรูปแบบเพิ่มเติมที่ใช้กับเฉพาะ ribbon</span><span class="sxs-lookup"><span data-stu-id="d53ea-131">The formatting options for ribbon charts are similar to those for a stacked column chart, with additional formatting options that are specific to the ribbons.</span></span>

![สกรีนช็อตจะแสดงไอคอนรูปแบบที่เลือกและพื้นที่ริบบอนที่ขยาย](media/desktop-ribbon-charts/power-bi-format-ribbon.png)

<span data-ttu-id="d53ea-133">ตัวเลือกการจัดรูปแบบสำหรับแผนภูมิ Ribbon เหล่านี้ ให้คุณปรับรูปแบบเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="d53ea-133">These formatting options for ribbon charts let you make adjustments.</span></span>

* <span data-ttu-id="d53ea-134">**ระยะห่าง** ช่วยให้คุณปรับช่องว่างที่จะแสดงระหว่าง ribbon</span><span class="sxs-lookup"><span data-stu-id="d53ea-134">**Spacing** lets you adjust how much space appears between ribbons.</span></span> <span data-ttu-id="d53ea-135">ตัวเลขเป็นเปอร์เซ็นต์ของความสูงมากสุดของคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="d53ea-135">The number is the percentage of the column's maximum height.</span></span>
* <span data-ttu-id="d53ea-136">**ตรงกับสีชุดข้อมูล** ช่วยให้คุณสามารถจับคู่สีของ ribbon ให้มีสีเดียวกับของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d53ea-136">**Match series color** allows you to match the color of the ribbons with the series color.</span></span> <span data-ttu-id="d53ea-137">เมื่อตั้งค่าเป็น **ปิด** Ribbon จะกลายเป็นสีเทา</span><span class="sxs-lookup"><span data-stu-id="d53ea-137">When set to **off**, ribbons are gray.</span></span>
* <span data-ttu-id="d53ea-138">**โปร่งใส** กำหนดว่า ribbon ต่าง ๆ จะมีความโปร่งใสแค่ไหน ค่าเริ่มต้นคือ 30</span><span class="sxs-lookup"><span data-stu-id="d53ea-138">**Transparency** specifies how transparent the ribbons are, with the default set to 30.</span></span>
* <span data-ttu-id="d53ea-139">**ขอบ** ให้คุณวางขอบสีเข้มบนด้านบนและด้านล่างของ ribbon ต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="d53ea-139">**Border** lets you place a dark border on the top and bottom of the ribbons.</span></span> <span data-ttu-id="d53ea-140">ตามค่าเริ่มต้น จะไม่แสดงขอบ</span><span class="sxs-lookup"><span data-stu-id="d53ea-140">By default, borders are off.</span></span>

<span data-ttu-id="d53ea-141">เนื่องจากแผนภูมิริบบอนไม่มีป้ายกำกับแกน y คุณอาจต้องการเพิ่มป้ายชื่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d53ea-141">Since the ribbon chart does not have y-axis labels, you may want to add data labels.</span></span> <span data-ttu-id="d53ea-142">จากบานหน้าต่างจัดรูปแบบ เลือก **ป้ายชื่อข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="d53ea-142">From the Formatting pane, select **Data labels**.</span></span> 

![ตัวเลือกการจัดรูปแบบสำหรับป้ายชื่อข้อมูล](media/desktop-ribbon-charts/power-bi-labels.png)

<span data-ttu-id="d53ea-144">ตั้งค่าตัวเลือกการจัดรูปแบบสำหรับป้ายชื่อข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="d53ea-144">Set formatting options for your data labels.</span></span> <span data-ttu-id="d53ea-145">ในตัวอย่างนี้ เราได้ตั้งค่าสีของตัวอักษรเป็นสีขาวและแสดงหน่วยเป็นพัน</span><span class="sxs-lookup"><span data-stu-id="d53ea-145">In this example, we've set the text color to white and display units to thousands.</span></span>

![สกรีนช็อตแสดงแผนภูมิริบบอนที่จัดรูปแบบขั้นสุดท้ายของคุณ](media/desktop-ribbon-charts/power-bi-data-labels.png)

## <a name="next-steps"></a><span data-ttu-id="d53ea-147">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d53ea-147">Next steps</span></span>

[<span data-ttu-id="d53ea-148">แผนภูมิกระจายและแผนภูมิฟองใน Power BI</span><span class="sxs-lookup"><span data-stu-id="d53ea-148">Scatter charts and bubble charts in Power BI</span></span>](power-bi-visualization-scatter.md)

[<span data-ttu-id="d53ea-149">ชนิดการแสดงภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="d53ea-149">Visualization types in Power BI</span></span>](power-bi-visualization-types-for-reports-and-q-and-a.md)
