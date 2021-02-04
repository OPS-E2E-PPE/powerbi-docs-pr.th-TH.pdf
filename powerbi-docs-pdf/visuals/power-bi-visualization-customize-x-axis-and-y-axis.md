---
title: กำหนดคุณสมบัติแกน X และแกน Y ด้วยตนเอง
description: คุณสมบัติแกน x และแกน y ที่กำหนดด้วยตนเอง
author: mihart
ms.author: mihart
ms.reviewer: mihart
featuredvideoid: 9DeAKM4SNJM
ms.custom: 9DeAKM4SNJM
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 05/06/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 625c2102ca5c8c030dbe2fca10ee030e1ac4c16d
ms.sourcegitcommit: 5c09d121d3205e65fb33a2eca0e60bc30e777773
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/18/2020
ms.locfileid: "97675269"
---
# <a name="customize-x-axis-and-y-axis-properties"></a><span data-ttu-id="bd669-103">ปรับแต่งคุณสมบัติแกน X และแกน Y ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="bd669-103">Customize x-axis and y-axis properties</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]    

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="bd669-104">ในบทช่วยสอนนี้ คุณจะได้เรียนรู้หลายวิธีในการปรับแต่งค่าแกน X และแกน Y ของการแสดงผลด้วยภาพของคุณ</span><span class="sxs-lookup"><span data-stu-id="bd669-104">In this tutorial, you'll learn many different ways to customize the X-axis and Y-axis of your visuals.</span></span> <span data-ttu-id="bd669-105">ไม่ใช่ภาพทั้งหมดที่มีแกน</span><span class="sxs-lookup"><span data-stu-id="bd669-105">Not all visuals have axes.</span></span> <span data-ttu-id="bd669-106">ตัวอย่างเช่น แผนภูมิวงกลมจะไม่มีแกน</span><span class="sxs-lookup"><span data-stu-id="bd669-106">Pie charts, for example, don't have axes.</span></span> <span data-ttu-id="bd669-107">และตัวเลือกการกำหนดเองมีมากมายในระดับภาพต่อภาพ</span><span class="sxs-lookup"><span data-stu-id="bd669-107">And customization options vary from visual to visual.</span></span> <span data-ttu-id="bd669-108">เนื่องจากมีตัวเลือกมากมายเกินกว่าที่จะกล่าวถึงในบทความเดียว ดังนั้นเราจะดูเฉพาะการปรับแต่งที่ใช้บ่อยที่สุดบางตัว เพื่อให้คุณคุ้นเคยกับการใช้บานหน้าต่าง **รูปแบบ** ของวิชวลบนพื้นที่รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="bd669-108">There are too many options to cover in a single article, so we'll take a look at some of the most-used customizations and get comfortable using the visual **Format** pane in the Power BI report canvas.</span></span>  

<span data-ttu-id="bd669-109">ดู Amanda ปรับแต่งแกน X และ Y ของเธอ</span><span class="sxs-lookup"><span data-stu-id="bd669-109">Watch Amanda customize her X- and Y-axes.</span></span> <span data-ttu-id="bd669-110">เธอจะยังสาธิตวิธีการต่างๆ ในการควบคุมการเรียงต่อกันเมื่อใช้การดูรายละเอียดแนวลึกและการดูข้อมูลสรุปอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="bd669-110">She'll also demonstrate the different ways to control concatenation when using drill down and drill up.</span></span>

> [!NOTE]
> <span data-ttu-id="bd669-111">วิดีโอนี้ใช้ Power BI เวอร์ชันเก่า</span><span class="sxs-lookup"><span data-stu-id="bd669-111">This video uses an older version of Power BI.</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/9DeAKM4SNJM" frameborder="0" allowfullscreen></iframe>

## <a name="prerequisites"></a><span data-ttu-id="bd669-112">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="bd669-112">Prerequisites</span></span>

- <span data-ttu-id="bd669-113">Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="bd669-113">Power BI Desktop</span></span>

- [<span data-ttu-id="bd669-114">ตัวอย่างการวิเคราะห์การค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="bd669-114">Retail Analysis Sample </span></span>](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix)


## <a name="add-a-new-visualization"></a><span data-ttu-id="bd669-115">เพิ่มการแสดงผลข้อมูลด้วยภาพใหม่</span><span class="sxs-lookup"><span data-stu-id="bd669-115">Add a new visualization</span></span>

<span data-ttu-id="bd669-116">ก่อนที่คุณจะสามารถกำหนดค่าการแสดงผลด้วยภาพของคุณ คุณต้องสร้างการแสดงผลด้วยภาพก่อน</span><span class="sxs-lookup"><span data-stu-id="bd669-116">Before you can customize your visualization, you have to build it.</span></span>

1. <span data-ttu-id="bd669-117">ใน Power BI Desktop ให้เปิดไฟล์ ตัวอย่างการวิเคราะห์ด้านการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="bd669-117">In Power BI Desktop, open the Retail Analysis sample.</span></span>  

2. <span data-ttu-id="bd669-118">ที่ด้านล่าง ให้เลือกไอคอนบวกสีเหลืองเพื่อเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="bd669-118">At the bottom, select the yellow plus icon to add a new page.</span></span> 

    ![เครื่องหมายบวกสีเหลือง](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-new-page-icon.png)

1. <span data-ttu-id="bd669-120">จากบานหน้าต่าง **การแสดงผลด้วยภาพ** เลือกไอคอนแผนภูมิคอลัมน์แบบเรียงซ้อน</span><span class="sxs-lookup"><span data-stu-id="bd669-120">From the **Visualizations** pane, select the stacked column chart icon.</span></span> <span data-ttu-id="bd669-121">สิ่งนี้จะเพิ่มเทมเพลตเปล่าไปยังพื้นที่รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="bd669-121">This adds an empty template to your report canvas.</span></span>

    ![สกรีนช็อตของบานหน้าต่างการแสดงผลด้วยภาพและแผนภูมิคอลัมน์แบบเรียงซ้อนที่ว่างเปล่า](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-column-chart.png)

1. <span data-ttu-id="bd669-123">หากต้องการเพิ่มค่าแกน X ในบานหน้าต่าง **เขตข้อมูล** ให้เลือก **เวลา** > **เดือนทางบัญชี**</span><span class="sxs-lookup"><span data-stu-id="bd669-123">To set the X-axis values, from the **Fields** pane, select **Time** > **FiscalMonth**.</span></span>

1. <span data-ttu-id="bd669-124">หากต้องการตั้งค่าแกน Y จากบานหน้าต่าง **เขตข้อมูล** ให้เลือก **ยอดขาย**  >  **ยอดขายของปีที่ผ่านมา** และ **ยอดขาย** > **ยอดขายของปีนี้** > **ค่า**</span><span class="sxs-lookup"><span data-stu-id="bd669-124">To set the Y-axis values, from the **Fields** pane, select **Sales** > **Last Year Sales** and **Sales** > **This Year Sales** > **Value**.</span></span>

    ![สกรีนช็อตของแผนภูมิคอลัมน์แบบเรียงซ้อนที่เติมข้อมูลแล้ว](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-build-visual.png)

    <span data-ttu-id="bd669-126">ในตอนนี้คุณสามารถกำหนดค่าแกน X ของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="bd669-126">Now you can customize your X-axis.</span></span> <span data-ttu-id="bd669-127">Power BI ช่วยให้คุณมีตัวเลือกแบบไร้ขีดจำกัดสำหรับการจัดรูปแบบการแสดงผลข้อมูลด้วยภาพของคุณ</span><span class="sxs-lookup"><span data-stu-id="bd669-127">Power BI gives you almost limitless options for formatting your visualization.</span></span> 

## <a name="customize-the-x-axis"></a><span data-ttu-id="bd669-128">ปรับแต่งแกน X</span><span class="sxs-lookup"><span data-stu-id="bd669-128">Customize the X-axis</span></span>
<span data-ttu-id="bd669-129">มีคุณลักษณะหลายอย่างที่สามารถกำหนดเองได้สำหรับแกน X</span><span class="sxs-lookup"><span data-stu-id="bd669-129">There are many features that are customizable for the X-axis.</span></span> <span data-ttu-id="bd669-130">คุณสามารถเพิ่มและปรับเปลี่ยนป้ายชื่อข้อมูลและชื่อแกน X</span><span class="sxs-lookup"><span data-stu-id="bd669-130">You can add and modify the data labels and X-axis title.</span></span> <span data-ttu-id="bd669-131">สำหรับหมวดหมู่ คุณสามารถปรับเปลี่ยนความกว้าง ขนาดแ ละระยะห่างของแถบ คอลัมน์ เส้น และพื้นที่</span><span class="sxs-lookup"><span data-stu-id="bd669-131">For categories, you can modify the width, size, and padding of bars, columns, lines, and areas.</span></span> <span data-ttu-id="bd669-132">และสำหรับค่า คุณสามารถปรับเปลี่ยนหน่วยแสดงผล ตำแหน่งทศนิยม และเส้นตาราง</span><span class="sxs-lookup"><span data-stu-id="bd669-132">And for values, you can modify the display units, decimal places, and grid lines.</span></span> <span data-ttu-id="bd669-133">ตัวอย่างต่อไปนี้แสดงการปรับแต่งสำหรับแผนภูมิคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="bd669-133">The following example shows customization for a column chart.</span></span> <span data-ttu-id="bd669-134">เรามาเพิ่มการปรับแต่งบางอย่างเพื่อให้คุณคุ้นเคยกับตัวเลือกและจากนั้นคุณสามารถสำรวจที่เหลือได้ด้วยตัวคุณเอง</span><span class="sxs-lookup"><span data-stu-id="bd669-134">Let's add a few customizations to get you familiar with the options and then you can explore the rest on your own.</span></span>

### <a name="customize-the-x-axis-labels"></a><span data-ttu-id="bd669-135">ปรับแต่งป้ายชื่อแกน X</span><span class="sxs-lookup"><span data-stu-id="bd669-135">Customize the X-axis labels</span></span>
<span data-ttu-id="bd669-136">ป้ายชื่อแกน X จะแสดงอยู่ด้านล่างของคอลัมน์ในแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="bd669-136">The X-axis labels display below the columns in the chart.</span></span> <span data-ttu-id="bd669-137">ในตอนนี้ ป้ายชื่อเหล่านั้นจะเป็นสีเทาอ่อน ขนาดเล็ก และยากต่อการอ่าน</span><span class="sxs-lookup"><span data-stu-id="bd669-137">Right now, they're light grey, small, and difficult to read.</span></span> <span data-ttu-id="bd669-138">เรามาเปลี่ยนกันเถอะ</span><span class="sxs-lookup"><span data-stu-id="bd669-138">Let's change that.</span></span>

1. <span data-ttu-id="bd669-139">ในบานหน้าต่าง **การแสดงผลข้อมูลด้วยภาพ** ให้เลือก **รูปแบบ** (ไอคอนรูปลูกกลิ้งทาสี ![ภาพหน้าจอของไอคอนรูปลูกกลิ้งทาสี](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-paintroller-icon.png))</span><span class="sxs-lookup"><span data-stu-id="bd669-139">In the **Visualizations** pane, select **Format** (the paint roller icon ![Screenshot of the paint roller icon.](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-paintroller-icon.png)</span></span> <span data-ttu-id="bd669-140">) เพื่อแสดงตัวเลือกการปรับแต่ง</span><span class="sxs-lookup"><span data-stu-id="bd669-140">) to reveal the customization options.</span></span>

2. <span data-ttu-id="bd669-141">ขยายตัวเลือกแกน X</span><span class="sxs-lookup"><span data-stu-id="bd669-141">Expand the X-axis options.</span></span>

   ![สกรีนช็อตของตัวเลือกแกน X](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-axis-x.png)

3. <span data-ttu-id="bd669-143">เลื่อนตัวเลื่อน **แกน X** ไปยัง **เปิด**</span><span class="sxs-lookup"><span data-stu-id="bd669-143">Move the **X-axis** slider to **On**.</span></span>

    ![สกรีนช็อตของแถบเลื่อนเปิดสำหรับแกน X](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-slider-on.png)

    <span data-ttu-id="bd669-145">ด้วยเหตุผลบางอย่างที่คุณอาจต้องการตั้งค่าแกน X เป็น **ปิด** คือถ้าการแสดงผลข้อมูลด้วยภาพนั้นสามารถอธิบายตนเองได้โดยไม่ต้องมีป้ายชื่อ หรือหากคุณมีหน้ารายงานที่แออัดและต้องทำให้มีพื้นที่ในการแสดงข้อมูลเพิ่มเติมมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="bd669-145">Some reasons you may want to set the X axis to **Off**, is if the visualization is self-explanatory without labels or if you have a crowded report page and need to make space to display more data.</span></span>

4. <span data-ttu-id="bd669-146">จัดรูปแบบสีข้อความ ขนาด และแบบตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="bd669-146">Format the text color, size, and font:</span></span>

    - <span data-ttu-id="bd669-147">**สี**: เลือกสีดำ</span><span class="sxs-lookup"><span data-stu-id="bd669-147">**Color**: Select black</span></span>

    - <span data-ttu-id="bd669-148">**ขนาดของข้อความ**: ป้อน *14*</span><span class="sxs-lookup"><span data-stu-id="bd669-148">**Text size**: Enter *14*</span></span>

    - <span data-ttu-id="bd669-149">**ชุดแบบอักษร**: เลือก **Arial Black**</span><span class="sxs-lookup"><span data-stu-id="bd669-149">**Font family**: Select **Arial Black**</span></span>

    - <span data-ttu-id="bd669-150">**ช่องว่างด้านใน**: ป้อน *40%*</span><span class="sxs-lookup"><span data-stu-id="bd669-150">**Inner padding**: Enter *40%*</span></span>

        ![ภาพหน้าจอที่มีป้ายชื่อบนมุม](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-formatting-x.png)
    
5. <span data-ttu-id="bd669-152">บางทีคุณอาจไม่ชอบวิธีการแสดงข้อความบนแกน X ในแนวทแยงมุม</span><span class="sxs-lookup"><span data-stu-id="bd669-152">Maybe you don't like the way the X-axis text is displayed on a diagonal.</span></span> <span data-ttu-id="bd669-153">คุณมีตัวเลือกหลากหลาย</span><span class="sxs-lookup"><span data-stu-id="bd669-153">You have several options.</span></span> 
    - <span data-ttu-id="bd669-154">เปลี่ยนขนาดตัวอักษรเป็นขนาดเล็กกว่า 14</span><span class="sxs-lookup"><span data-stu-id="bd669-154">Change the text size to something smaller than 14.</span></span>
    - <span data-ttu-id="bd669-155">ทำให้การแสดงผลข้อมูลด้วยภาพใหญ่ขึ้น</span><span class="sxs-lookup"><span data-stu-id="bd669-155">Make the visualization larger.</span></span> 
    - <span data-ttu-id="bd669-156">แสดงคอลัมน์น้อยลง และเพิ่มแถบเลื่อนโดยการเพิ่ม **ความกว้างหมวดหมู่ขั้นต่ำ**</span><span class="sxs-lookup"><span data-stu-id="bd669-156">Display fewer columns and add a scrollbar by increasing **Minimum category width**.</span></span> 
    
    <span data-ttu-id="bd669-157">ที่นี่ เราได้เลือกตัวเลือกที่สองและจับแถบปรับขนาดด้านใดด้านหนึ่งเพื่อทำให้การแสดงผลข้อมูลด้วยภาพกว้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="bd669-157">Here, we've selected the second option and grabbed one of the resize bars to make the visualization wider.</span></span> <span data-ttu-id="bd669-158">ในตอนนี้ คุณปรับใช้ข้อความขนาด 14 จุดโดยไม่จำเป็นต้องแสดงข้อความบนมุมหรือด้วยแถบเลื่อน</span><span class="sxs-lookup"><span data-stu-id="bd669-158">It now accommodates the 14-point text without needing to display the text on an angle or with a scrollbar.</span></span> 

   ![บานหน้าต่างแผนภูมิและการจัดรูปแบบที่มีป้ายชื่อในแนวนอน](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-stretch.png)

### <a name="customize-the-x-axis-title"></a><span data-ttu-id="bd669-160">ปรับแต่งชื่อแกน X</span><span class="sxs-lookup"><span data-stu-id="bd669-160">Customize the X-axis title</span></span>
<span data-ttu-id="bd669-161">เมื่อชื่อแกน X **เปิด** อยู่ ชื่อแกน X จะปรากฏใต้ป้ายชื่อแกน X</span><span class="sxs-lookup"><span data-stu-id="bd669-161">When the X-axis title is **On**, the X-axis title displays below the X-axis labels.</span></span> 

1. <span data-ttu-id="bd669-162">เริ่มต้นโดยการเปลี่ยนสถานะของชื่อแกน X เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="bd669-162">Start by turning the X-axis title to **On**.</span></span>  

    ![แถบเลื่อนชื่อ](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-title-on.png)

    <span data-ttu-id="bd669-164">สิ่งแรกที่คุณจะสังเกตเห็นคือการแสดงผลข้อมูลด้วยภาพของคุณในขณะนี้มีชื่อแกน X เป็นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="bd669-164">The first thing you'll notice is that your visualization now has a default X-axis title.</span></span>  <span data-ttu-id="bd669-165">ในกรณีนี้ เป็น **เดือนงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="bd669-165">In this case, it's **FiscalMonth**.</span></span>

   ![แผนภูมิที่มีชื่อแสดงตามแนวด้านล่าง](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-x-title.png)

1. <span data-ttu-id="bd669-167">จัดรูปแบบสี ขนาด และแบบตัวอักษร ของชื่อเรื่อง:</span><span class="sxs-lookup"><span data-stu-id="bd669-167">Format the title text color, size, and font:</span></span>

    - <span data-ttu-id="bd669-168">**สีของชื่อเรื่อง**: เลือกสีส้ม</span><span class="sxs-lookup"><span data-stu-id="bd669-168">**Title color**: Select orange</span></span>

    - <span data-ttu-id="bd669-169">**ชื่อแกน**: พิมพ์ *เดือนทางบัญชี* (มีช่องว่างด้วย)</span><span class="sxs-lookup"><span data-stu-id="bd669-169">**Axis title**: Type *Fiscal Month* (with a space)</span></span>

    - <span data-ttu-id="bd669-170">**ขนาดข้อความของชื่อเรื่อง**: ป้อน *18*</span><span class="sxs-lookup"><span data-stu-id="bd669-170">**Title text size**: Enter *18*</span></span>

    <span data-ttu-id="bd669-171">เมื่อคุณทำการปรับแต่งค่าเองเสร็จสิ้นแล้ว แผนภูมิคอลัมน์แบบเรียงซ้อนของคุณจะมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="bd669-171">After you finish the customizations, your stacked column chart looks something like this:</span></span>

    ![สกรีนช็อตของแผนภูมิคอลัมน์แบบเรียงซ้อนที่ปรับแต่งเอง](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-x-title-formatted.png)

1. <span data-ttu-id="bd669-173">บันทึกการเปลี่ยนแปลงที่คุณทำและย้ายไปยังส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="bd669-173">Save the changes you've made and move to the next section.</span></span> <span data-ttu-id="bd669-174">เมื่อต้องการย้อนกลับการเปลี่ยนแปลงทั้งหมด ให้เลือก **ย้อนกลับไปเป็นค่าเริ่มต้น** ที่ด้านล่างของบานหน้าต่างการกำหนด **แกน X** ด้วยตัวเอง</span><span class="sxs-lookup"><span data-stu-id="bd669-174">If you ever need to revert all of the changes, select **Revert to default** at the bottom of the **X-Axis** customization pane.</span></span> <span data-ttu-id="bd669-175">ถัดไป คุณจะกำหนดค่าแกน Y ของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="bd669-175">Next, you'll customize your Y-Axis.</span></span>

## <a name="customize-the-y-axis"></a><span data-ttu-id="bd669-176">ปรับแต่งแกน Y</span><span class="sxs-lookup"><span data-stu-id="bd669-176">Customize the Y-axis</span></span>
<span data-ttu-id="bd669-177">มีคุณลักษณะมากมายที่คุณสามารถใช้ปรับแต่งแกน Y ได้</span><span class="sxs-lookup"><span data-stu-id="bd669-177">There are many features that can be customized for the Y-axis.</span></span> <span data-ttu-id="bd669-178">คุณสามารถเพิ่มและปรับเปลี่ยนป้ายชื่อข้อมูล ชื่อแกน X และเส้นตารางได้</span><span class="sxs-lookup"><span data-stu-id="bd669-178">You can add and modify the data labels, Y-axis title, and gridlines.</span></span> <span data-ttu-id="bd669-179">สำหรับค่า คุณสามารถปรับเปลี่ยนหน่วยแสดงผล ตำแหน่งทศนิยม จุดเริ่มต้น และจุดสิ้นสุดได้</span><span class="sxs-lookup"><span data-stu-id="bd669-179">For values, you can modify the display units, decimal places, starting point, and end point.</span></span> <span data-ttu-id="bd669-180">และ สำหรับหมวดหมู่ คุณสามารถปรับเปลี่ยนความกว้าง ขนาดแ ละระยะห่างของแถบ คอลัมน์ เส้น และพื้นที่</span><span class="sxs-lookup"><span data-stu-id="bd669-180">And, for categories, you can modify the width, size, and padding of bars, columns, lines, and areas.</span></span> 

<span data-ttu-id="bd669-181">ตัวอย่างต่อไปนี้ยังคงเป็นการปรับแต่งแผนภูมิคอลัมน์ของเรา</span><span class="sxs-lookup"><span data-stu-id="bd669-181">The following example continues our customization of a column chart.</span></span> <span data-ttu-id="bd669-182">ลองทำการปรับแต่งเล็กน้อยเพื่อให้คุณคุ้นเคยกับตัวเลือกและจากนั้นคุณสามารถสำรวจที่เหลือได้ด้วยตัวคุณเอง</span><span class="sxs-lookup"><span data-stu-id="bd669-182">Let's make a few changes to get you familiar with the options, and then you can explore the rest on your own.</span></span>

### <a name="customize-the-y-axis-labels"></a><span data-ttu-id="bd669-183">ปรับแต่งป้ายชื่อแกน Y</span><span class="sxs-lookup"><span data-stu-id="bd669-183">Customize the Y-axis labels</span></span>
<span data-ttu-id="bd669-184">ป้ายชื่อแกน Y จะแสดงทางด้านซ้ายตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="bd669-184">The Y-axis labels are displayed to the left by default.</span></span> <span data-ttu-id="bd669-185">ในตอนนี้ ป้ายชื่อเหล่านั้นจะเป็นสีเทาอ่อน ขนาดเล็ก และยากต่อการอ่าน</span><span class="sxs-lookup"><span data-stu-id="bd669-185">Right now, they're light grey, small, and difficult to read.</span></span> <span data-ttu-id="bd669-186">เรามาเปลี่ยนกันเถอะ</span><span class="sxs-lookup"><span data-stu-id="bd669-186">Let's change that.</span></span>

1. <span data-ttu-id="bd669-187">ขยายตัวเลือกแกน Y</span><span class="sxs-lookup"><span data-stu-id="bd669-187">Expand the Y-Axis options.</span></span>

   ![สกรีนช็อตของตัวเลือกแกน Y](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-axis-y.png)

1. <span data-ttu-id="bd669-189">เลื่อนตัวเลื่อน **แกน Y** ไปยัง **เปิด**</span><span class="sxs-lookup"><span data-stu-id="bd669-189">Move the **Y-Axis** slider to **On**.</span></span>  

    ![สกรีนช็อตของแถบเลื่อนเปิดสำหรับแกน Y](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-y-axis-on.png)

    <span data-ttu-id="bd669-191">เหตุผลหนึ่งที่คุณอาจต้องการปิดแกน Y คือเพื่อประหยัดพื้นที่สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="bd669-191">One reason you might want to turn off the Y-axis, is to save space for more data.</span></span>

1. <span data-ttu-id="bd669-192">จัดรูปแบบสีข้อความ ขนาด และแบบตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="bd669-192">Format the text color, size, and font:</span></span>

    - <span data-ttu-id="bd669-193">**สี**: เลือกสีดำ</span><span class="sxs-lookup"><span data-stu-id="bd669-193">**Color**: Select black</span></span>

    - <span data-ttu-id="bd669-194">**ขนาดของข้อความ**: ป้อน *10*</span><span class="sxs-lookup"><span data-stu-id="bd669-194">**Text size**: Enter *10*</span></span>

    - <span data-ttu-id="bd669-195">**หน่วยแสดงผล**: เลือก **หน่วยล้าน**</span><span class="sxs-lookup"><span data-stu-id="bd669-195">**Display units**: Select **Millions**</span></span>

    ![แผนภูมิหลังจากการจัดรูปแบบแกน Y](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-formatting-y.png)

### <a name="customize-the-y-axis-title"></a><span data-ttu-id="bd669-197">ปรับแต่งชื่อแกน Y</span><span class="sxs-lookup"><span data-stu-id="bd669-197">Customize the Y-axis title</span></span>
<span data-ttu-id="bd669-198">เมื่อชื่อแกน Y **เปิด** อยู่ ชื่อแกน Y จะปรากฏถัดจากป้ายชื่อแกน Y</span><span class="sxs-lookup"><span data-stu-id="bd669-198">When the Y-axis title is **On**, the Y-axis title displays next to the Y-axis labels.</span></span> <span data-ttu-id="bd669-199">สำหรับการแสดงผลภาพนี้ การมีชื่อแกน Y ไม่ได้ช่วยภาพให้ดีขึ้น ดังนั้นจึงปล่อยให้การแสดง **ชื่อเรื่อง** **ปิด**</span><span class="sxs-lookup"><span data-stu-id="bd669-199">For this visualization, having a Y-Axis title doesn't improve the visual, so leave **Title** turned **Off**.</span></span> <span data-ttu-id="bd669-200">เราจะเพิ่มชื่อแกน Y ไปยังวิชวลแบบสองแกนในภายหลังของบทช่วยสอนนี้</span><span class="sxs-lookup"><span data-stu-id="bd669-200">We'll add Y-axis titles to a dual-axis visual later in this tutorial.</span></span> 

### <a name="customize-the-gridlines"></a><span data-ttu-id="bd669-201">ปรับแต่งเส้นตาราง</span><span class="sxs-lookup"><span data-stu-id="bd669-201">Customize the gridlines</span></span>
<span data-ttu-id="bd669-202">เรามาทำเส้นตารางให้เด่นขึ้นมาโดยการเปลี่ยนสีและเพิ่มสโตรก:</span><span class="sxs-lookup"><span data-stu-id="bd669-202">Let's make the gridlines stand out by changing the color and increasing the stroke:</span></span>

- <span data-ttu-id="bd669-203">**สี**: เลือกสีส้ม</span><span class="sxs-lookup"><span data-stu-id="bd669-203">**Color**: Select orange</span></span>

- <span data-ttu-id="bd669-204">**สโตรก**: ป้อน *2*</span><span class="sxs-lookup"><span data-stu-id="bd669-204">**Stroke**: Enter *2*</span></span>

<span data-ttu-id="bd669-205">หลังจากกำหนดค่าทั้งหมดเหล่านี้ แผนภูมิคอลัมน์ของคุณจะมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="bd669-205">After all these customizations, your column chart should look something like this:</span></span>

![สกรีนช็อตของแผนภูมิที่มีแกน Y ที่กำหนดเอง](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-gridline.png)

## <a name="customizing-visualizations-with-dual-y-axes"></a><span data-ttu-id="bd669-207">กำหนดค่าการแสดงผลข้อมูลด้วยภาพให้มีแกน Y สองแกน</span><span class="sxs-lookup"><span data-stu-id="bd669-207">Customizing visualizations with dual Y axes</span></span>

<span data-ttu-id="bd669-208">การแสดงผลข้อมูลด้วยภาพบางชนิดอาจได้รับประโยชน์จากการมีแกน Y สองแกน</span><span class="sxs-lookup"><span data-stu-id="bd669-208">Some visualizations can benefit from having two Y axes.</span></span> <span data-ttu-id="bd669-209">แผนภูมิผสมเป็นตัวอย่างที่ดี</span><span class="sxs-lookup"><span data-stu-id="bd669-209">Combo charts are a good example.</span></span> <span data-ttu-id="bd669-210">ก่อนที่เราจะสามารถจัดรูปแบบแกน Y คู่ เราจะสร้างแผนภูมิผสมที่เปรียบเทียบแนวโน้มสำหรับยอดขายและกำไรขั้นต้น</span><span class="sxs-lookup"><span data-stu-id="bd669-210">Before we can format dual Y axes, we'll create a combo chart that compares trends for sales and gross margin.</span></span>  

### <a name="create-a-chart-with-two-y-axes"></a><span data-ttu-id="bd669-211">สร้างแผนภูมิที่มีแกน Y สองแกน</span><span class="sxs-lookup"><span data-stu-id="bd669-211">Create a chart with two Y-Axes</span></span>

1. <span data-ttu-id="bd669-212">เลือกแผนภูมิคอลัมน์และเปลี่ยนเป็นแผนภูมิ *เส้นและคอลัมน์แบบเรียงซ้อน*</span><span class="sxs-lookup"><span data-stu-id="bd669-212">Select the column chart, and change it to a *Line and stacked column* chart.</span></span> <span data-ttu-id="bd669-213">วิชวลชนิดนี้รองรับค่าแผนภูมิเส้นเดียว และค่าคอลัมน์แบบเรียงซ้อนหลายอัน</span><span class="sxs-lookup"><span data-stu-id="bd669-213">This type of visual supports a single line chart value and multiple stackable column values.</span></span> 

    ![สกรีนช็อตของการเรียกบานหน้าต่างการแสดงภาพเส้นและไอคอนแผนภูมิคอลัมน์แบบเรียงซ้อนออกมา](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-combo.png)
   

2. <span data-ttu-id="bd669-215">ลาก **ยอดขาย** >  **% อัตรากำไรขั้นต้นเมื่อปีที่แล้ว** จากบานหน้าต่างเขตข้อมูลของคุณไปยังบักเก็ต **ค่าบรรทัด**</span><span class="sxs-lookup"><span data-stu-id="bd669-215">Drag **Sales** > **Gross Margin Last Year %** from your Fields pane into the **Line Values** bucket.</span></span>

    ![สกรีนช็อตของเส้นและแผนภูมิคอลัมน์แบบเรียงซ้อน ที่ค่าทั้งสามค่าทั้งหมดแสดงอย่างชัดเจน](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-add-line.png)

    
3. <span data-ttu-id="bd669-217">จัดรูปแบบการแสดงผลข้อมูลด้วยภาพใหม่เพื่อลบป้ายชื่อแกน X ที่อยู่ตรงมุมออก</span><span class="sxs-lookup"><span data-stu-id="bd669-217">Reformat the visualization to remove the angled X-axis labels.</span></span> 

   ![บานหน้าต่างแผนภูมิผสมและรูปแบบที่มีขนาดแบบอักษรลดลงเป็น 12](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-font-size.png)

   <span data-ttu-id="bd669-219">Power BI สร้างแกน Y สองแกน ช่วยให้แต่ละแกนมีค่ามาตราส่วนที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="bd669-219">Power BI creates two Y axes, allowing the values to be scaled differently.</span></span> <span data-ttu-id="bd669-220">แกนซ้ายวัดยอดขายเป็นดอลลาร์ และแกนขวาวัดเปอร์เซ็นต์อัตรากำไรขั้นต้น</span><span class="sxs-lookup"><span data-stu-id="bd669-220">The left axis measures sales dollars and the right axis measures gross margin percentage.</span></span>

### <a name="format-the-second-y-axis"></a><span data-ttu-id="bd669-221">จัดรูปแบบแกน Y ที่สอง</span><span class="sxs-lookup"><span data-stu-id="bd669-221">Format the second Y-Axis</span></span>
<span data-ttu-id="bd669-222">เนื่องจากเราเริ่มต้นจากการแสดงผลข้อมูลด้วยภาพที่มีการจัดรูปแบบแกน Y หนึ่งแกนแล้ว ดังนั้น Power BI จึงได้สร้างแกน Y ที่สองโดยใช้การตั้งค่าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="bd669-222">Because we started with a visualization with one formatted Y-axis, Power BI created the second Y-axis using the same settings.</span></span> <span data-ttu-id="bd669-223">แต่เราสามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="bd669-223">But we can change that.</span></span> 

1. <span data-ttu-id="bd669-224">ในบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล** เลือกไอคอนลูกกลิ้งทาสี เพื่อแสดงตัวเลือการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="bd669-224">In the **Visualizations** pane, select the paint roller icon to display the format options.</span></span>

1. <span data-ttu-id="bd669-225">ขยายตัวเลือกแกน Y</span><span class="sxs-lookup"><span data-stu-id="bd669-225">Expand the Y-Axis options.</span></span>

1. <span data-ttu-id="bd669-226">เลื่อนลงจนกว่าคุณพบตัวเลือก **แสดงรายการสำรอง**</span><span class="sxs-lookup"><span data-stu-id="bd669-226">Scroll down until you find the **Show secondary** option.</span></span> <span data-ttu-id="bd669-227">ตรวจสอบว่าส่วนนี้ **เปิด**</span><span class="sxs-lookup"><span data-stu-id="bd669-227">Verify that it is **On**.</span></span> <span data-ttu-id="bd669-228">แกน Y ที่สองของเราแสดงแผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="bd669-228">Our secondary Y axis represents the line chart.</span></span>

   ![สกรีนช็อตของตัวเลือกการนำเสนอรอง](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-show-secondary.png)

1. <span data-ttu-id="bd669-230">(ไม่บังคับ) ปรับแต่งสีฟอนต์ ขนาด และหน่วยแสดงผลสำหรับสองแกน</span><span class="sxs-lookup"><span data-stu-id="bd669-230">(Optional) Customize the font color, size, and display units for the two axes.</span></span> <span data-ttu-id="bd669-231">ถ้าคุณสลับ **ตำแหน่ง** สำหรับแกนคอลัมน์หรือแกนเส้นแล้ว ทั้งสองแกนจะสลับด้านกัน</span><span class="sxs-lookup"><span data-stu-id="bd669-231">If you switch **Position** for either the column axis or the line axis, then the two axes switch sides.</span></span>

### <a name="add-titles-to-both-axes"></a><span data-ttu-id="bd669-232">เพิ่มชื่อแกนให้กับทั้งสองแกน</span><span class="sxs-lookup"><span data-stu-id="bd669-232">Add titles to both axes</span></span>

<span data-ttu-id="bd669-233">เนื่องจากการแสดงผลข้อมูลด้วยภาพที่ซับซ้อน สิ่งนี้จะช่วยในการเพิ่มชื่อแกน</span><span class="sxs-lookup"><span data-stu-id="bd669-233">With a visualization that's complex, it helps to add axes titles.</span></span>  <span data-ttu-id="bd669-234">ชื่อแกนช่วยให้เพื่อนร่วมงานของคุณ เข้าใจเรื่องราวที่การแสดงภาพของคุณกำลังบอก</span><span class="sxs-lookup"><span data-stu-id="bd669-234">Titles help your colleagues understand the story your visualization is telling.</span></span>

1. <span data-ttu-id="bd669-235">สลับ **ชื่อแกน** ไปเป็น **เปิด** สำหรับ **แกน Y (คอลัมน์)** และ **แกน Y (เส้น)**</span><span class="sxs-lookup"><span data-stu-id="bd669-235">Toggle **Title** to **On** for **Y-Axis (Column)** and the **Y-Axis (Line)**.</span></span>

1. <span data-ttu-id="bd669-236">ตั้งค่า **สไตล์** เป็น **แสดงเฉพาะหัวข้อ** สำหรับทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="bd669-236">Set **Style** to **Show title only** for both.</span></span>

   ![สกรีนช็อตของตัวเลือกชื่อเรื่องและสไตล์](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-show-title.png)

1. <span data-ttu-id="bd669-238">แผนภูมิผสมของคุณตอนนี้แสดงแกนทั้งสองแกนด้วยชื่อ</span><span class="sxs-lookup"><span data-stu-id="bd669-238">Your combo chart now shows dual axes, both with titles.</span></span>

   ![สกรีนช็อตของแผนภูมิแกน Y คู่แบบกำหนดเอง](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-titles-on.png)

1. <span data-ttu-id="bd669-240">จัดรูปแบบชื่อแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="bd669-240">Format the titles.</span></span> <span data-ttu-id="bd669-241">ในตัวอย่างนี้ เราได้ย่อชื่อแกนหนึ่งแกน และลดขนาดตัวอักษรสำหรับชื่อเรื่องทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="bd669-241">In this example, we've shorted one of the titles and reduced the font size for both.</span></span> 
    - <span data-ttu-id="bd669-242">ขนาดฟอนต์: **9**</span><span class="sxs-lookup"><span data-stu-id="bd669-242">Font size: **9**</span></span>
    - <span data-ttu-id="bd669-243">ย่อ **ชื่อแกน** สำหรับแกน Y แรก (แผนภูมิคอลัมน์): ยอดขายปีที่แล้วและปีนี้</span><span class="sxs-lookup"><span data-stu-id="bd669-243">Shortened the **Axis title** for the first Y axis (the column chart): Sales last year & this year.</span></span> 
    
     ![ภาพหน้าจอของแผนภูมิผสมที่มีการแสดงชื่อแบบเต็ม](media/power-bi-visualization-customize-x-axis-and-y-axis/power-bi-dual.png)

    <span data-ttu-id="bd669-245">สำหรับข้อมูลเพิ่มเติม โปรดดู [คำแนะนำและเคล็ดลับในการจัดรูปแบบสีใน Power BI](service-tips-and-tricks-for-color-formatting.md) และ [กำหนดชื่อเรื่องการแสดงผลข้อมูลด้วยภาพ คำอธิบายแผนภูมิ และพื้นหลัง](power-bi-visualization-customize-title-background-and-legend.md)</span><span class="sxs-lookup"><span data-stu-id="bd669-245">For more information, see [Tips and tricks for color formatting in Power BI](service-tips-and-tricks-for-color-formatting.md) and [Customize visualization titles, legends, and backgrounds](power-bi-visualization-customize-title-background-and-legend.md).</span></span> 
    

## <a name="next-steps"></a><span data-ttu-id="bd669-246">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="bd669-246">Next steps</span></span>

- [<span data-ttu-id="bd669-247">การแสดงภาพในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="bd669-247">Visualizations in Power BI reports</span></span>](power-bi-report-visualizations.md)

<span data-ttu-id="bd669-248">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="bd669-248">More questions?</span></span> [<span data-ttu-id="bd669-249">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="bd669-249">Try the Power BI Community</span></span>](https://community.powerbi.com/)
