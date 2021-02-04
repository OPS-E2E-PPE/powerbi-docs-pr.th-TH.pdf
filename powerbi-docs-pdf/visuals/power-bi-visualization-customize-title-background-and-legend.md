---
title: เริ่มต้นใช้งานการจัดรูปแบบการแสดงภาพ Power BI
description: กำหนดชื่อเรื่อง การแสดงผลด้วยภาพ พื้นหลัง ป้ายชื่อ และคำอธิบายแผนภูมิ
author: mihart
ms.author: mihart
ms.reviewer: mihart
featuredvideoid: removed
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 12/18/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 2a8c125a37e0d70ea735d9f1962f64deb69061c8
ms.sourcegitcommit: 1691ce556ab5b22e6f9d06086a054d165d482809
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/23/2020
ms.locfileid: "97745150"
---
# <a name="customize-visualization-titles-backgrounds-labels-and-legends"></a><span data-ttu-id="66406-103">กำหนดชื่อเรื่อง การแสดงผลด้วยภาพ พื้นหลัง ป้ายชื่อ และคำอธิบายแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="66406-103">Customize visualization titles, backgrounds, labels, and legends</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]    


<span data-ttu-id="66406-104">ในบทช่วยสอนนี้ คุณจะได้เรียนรู้ถึงวิธีการกำหนดการแสดงภาพของคุณเองสองถึงสามวิธี</span><span class="sxs-lookup"><span data-stu-id="66406-104">In this tutorial, you'll learn a few different ways to customize your visualizations.</span></span> <span data-ttu-id="66406-105">มีตัวเลือกมากมายสำหรับการกำหนดการแสดงภาพของคุณ</span><span class="sxs-lookup"><span data-stu-id="66406-105">There are so many options for customizing your visualizations.</span></span> <span data-ttu-id="66406-106">วิธีดีที่สุดในการเรียนรู้เกี่ยวกับทั้งหมดคือการสำรวจบานหน้าต่าง **รูปแบบ** (เลือกไอคอนลูกกลิ้งทาสี)</span><span class="sxs-lookup"><span data-stu-id="66406-106">The best way to learn about them all is by exploring the **Format** pane (select the paint roller icon).</span></span> <span data-ttu-id="66406-107">เพื่อช่วยให้คุณเริ่มต้นใช้งาน บทความนี้แสดงวิธีการกำหนดชื่อเรื่องการแสดงผลด้วยภาพ คำอธิบายแผนภูมิ พื้นหลัง ป้ายชื่อ และเพิ่มธีม</span><span class="sxs-lookup"><span data-stu-id="66406-107">To get you started, this article shows you how to customize a visualization title, legend, background, label, and add a theme.</span></span>

<span data-ttu-id="66406-108">คุณไม่สามารถกำหนดค่าการแสดงภาพทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="66406-108">You can't customize all visualizations.</span></span> <span data-ttu-id="66406-109">ดู [รายการทั้งหมด](#visualization-types-that-you-can-customize) ของการแสดงภาพสำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="66406-109">See the [complete list](#visualization-types-that-you-can-customize) of visualizations for details.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="66406-110">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="66406-110">Prerequisites</span></span>

- <span data-ttu-id="66406-111">บริการ Power BI หรือ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="66406-111">The Power BI service or Power BI Desktop</span></span>

- <span data-ttu-id="66406-112">รายงานตัวอย่างการวิเคราะห์ร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="66406-112">Retail Analysis Sample report</span></span>

> [!NOTE]
> <span data-ttu-id="66406-113">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="66406-113">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span> <span data-ttu-id="66406-114">ดู [การแชร์รายงาน](../collaborate-share/service-share-reports.md)</span><span class="sxs-lookup"><span data-stu-id="66406-114">See [sharing reports](../collaborate-share/service-share-reports.md).</span></span>

## <a name="customize-visualization-titles-in-reports"></a><span data-ttu-id="66406-115">กำหนดชื่อเรื่องของการแสดงภาพในรายงาน</span><span class="sxs-lookup"><span data-stu-id="66406-115">Customize visualization titles in reports</span></span>

<span data-ttu-id="66406-116">ในการทำตามขั้นตอนนี้ ลงชื่อเข้าใช้ Power BI Desktop และเปิดรายงาน [ตัวอย่างการวิเคราะห์ร้านค้าปลีก](../create-reports/sample-datasets.md)</span><span class="sxs-lookup"><span data-stu-id="66406-116">To follow along, sign into Power BI Desktop and open the [Retail Analysis Sample](../create-reports/sample-datasets.md) report.</span></span>

> [!NOTE]
> <span data-ttu-id="66406-117">เมื่อคุณปักหมุดภาพไปยังแดชบอร์ด การแสดงภาพจะกลายเป็นไทล์ของแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="66406-117">When you pin a visualization to a dashboard, it becomes a dashboard tile.</span></span> <span data-ttu-id="66406-118">นอกจากนี้ คุณสามารถกำหนดไทล์ด้วยตนเองให้มี[ชื่อเรื่องใหม่และคำบรรยาย ไฮเปอร์ลิงก์ และปรับขนาด](../create-reports/service-dashboard-edit-tile.md)ได้</span><span class="sxs-lookup"><span data-stu-id="66406-118">You can also customize the tiles themselves with [new titles and subtitles, hyperlinks, and resizing](../create-reports/service-dashboard-edit-tile.md).</span></span>

1. <span data-ttu-id="66406-119">ไปที่หน้า **ร้านค้าใหม่** ของรายงาน **ตัวอย่างการวิเคราะห์ร้านค้าปลีก**</span><span class="sxs-lookup"><span data-stu-id="66406-119">Go to the **New Stores** page of the **Retail Analysis Sample** report.</span></span>

1. <span data-ttu-id="66406-120">เลือกแผนภูมิคอลัมน์คลัสเตอร์ **จำนวนร้านค้าที่เปิดตามเดือนที่เปิดและเครือร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="66406-120">Select the **Open Store Count by Open Month and Chain** clustered column chart.</span></span>

1. <span data-ttu-id="66406-121">ในพื้นที่ **การแสดงภาพ** นี้ เลือกไอคอนลูกกลิ้งทาสีเพื่อแสดงตัวเลือกการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="66406-121">In the **Visualizations** pane, select the paint roller icon to reveal the format options.</span></span>

1. <span data-ttu-id="66406-122">เลือก **ชื่อเรื่อง** เพื่อขยายส่วนนั้น</span><span class="sxs-lookup"><span data-stu-id="66406-122">Select **Title** to expand that section.</span></span>

   ![สกรีนช็อตของบานหน้าต่างจัดรูปแบบที่มีไอคอนลูกกลิ้งระบายสีแสดงอยู่ และลูกศรที่ชี้ไปยังดรอปดาวน์ของชื่อเรื่อง](media/power-bi-visualization-customize-title-background-and-legend/power-bi-format-menu.png)

1. <span data-ttu-id="66406-124">เลื่อนแถบเลื่อน **ชื่อเรื่อง** ไปยัง **เปิด**</span><span class="sxs-lookup"><span data-stu-id="66406-124">Move the **Title** slider to **On**.</span></span>

1. <span data-ttu-id="66406-125">หากต้องการเปลี่ยนชื่อเรื่อง ให้ใส่ *จำนวนของร้านค้าแยกตามเดือนที่เปิด* ในเขตข้อมูล **ข้อความชื่อเรื่อง**</span><span class="sxs-lookup"><span data-stu-id="66406-125">To change the title, enter *Store count by month opened* in the **Title text** field.</span></span>

    ![ภาพหน้าจอของบานหน้าต่างรูปแบบที่ป้อนข้อความชื่อเรื่อง](media/power-bi-visualization-customize-title-background-and-legend/power-bi-title.png)

1. <span data-ttu-id="66406-127">เปลี่ยน **สีแบบอักษร** เป็นสีขาว และ **สีพื้นหลัง** เป็นสีน้ำเงิน</span><span class="sxs-lookup"><span data-stu-id="66406-127">Change **Font color** to white and **Background color** to blue.</span></span>    

    <span data-ttu-id="66406-128">a.</span><span class="sxs-lookup"><span data-stu-id="66406-128">a.</span></span> <span data-ttu-id="66406-129">เลือกรายการแบบเลื่อนลง แล้วเลือกสีจาก **สีของธีม**, **สีล่าสุด**, หรือ **สีแบบกำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="66406-129">Select the drop-down and choose a color from **Theme colors**, **Recent colors**, or **Custom color**.</span></span>
    
    ![สกรีนช็อตของสีฟอนต์และตัวเลือกสีพื้นหลัง](media/power-bi-visualization-customize-title-background-and-legend/power-bi-color.png)

    <span data-ttu-id="66406-131">b.</span><span class="sxs-lookup"><span data-stu-id="66406-131">b.</span></span> <span data-ttu-id="66406-132">เลือกรายการแบบเลื่อนลงเพื่อปิดหน้าต่างสี</span><span class="sxs-lookup"><span data-stu-id="66406-132">Select the drop-down to close the color window.</span></span>


1. <span data-ttu-id="66406-133">เพิ่มขนาดข้อความเป็น **16 pt**</span><span class="sxs-lookup"><span data-stu-id="66406-133">Increase the text size to **16 pt**.</span></span>

1. <span data-ttu-id="66406-134">การกำหนดค่าสุดท้ายที่คุณจะดำเนินการกับชื่อเรื่องแผนภูมิคือการจัดแนวกึ่งกลางของการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="66406-134">The last customization you'll make to the chart title is to align it in the center of the visualization.</span></span>

    ![สกรีนช็อตของตัวควบคุมการจัดแนวโดยมีการเลือกตัวเลือกศูนย์กลาง](media/power-bi-visualization-customize-title-background-and-legend/power-bi-align.png)

    <span data-ttu-id="66406-136">ณ จุดนี้ในบทช่วยสอน ชื่อเรื่อง แผนภูมิคอลัมน์แบบกลุ่มของคุณจะมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="66406-136">At this point in the tutorial, your clustered column chart title will look something like this:</span></span>

    ![สกรีนช็อตของแผนภูมิคอลัมน์แบบกลุ่มที่ผ่านการกำหนดค่าใหม่](media/power-bi-visualization-customize-title-background-and-legend/power-bi-table.png)

<span data-ttu-id="66406-138">บันทึกการเปลี่ยนแปลงที่คุณทำและย้ายไปยังส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="66406-138">Save the changes you've made and move to the next section.</span></span>

<span data-ttu-id="66406-139">เมื่อต้องการย้อนกลับการเปลี่ยนแปลงทั้งหมด ให้เลือก **ย้อนกลับไปเป็นค่าเริ่มต้น** ที่ด้านล่างของบานหน้าต่างการกำหนด **ชื่อเรื่อง** ด้วยตัวเอง</span><span class="sxs-lookup"><span data-stu-id="66406-139">If you ever need to revert all of the changes, select **Revert to default**, at the bottom of the **Title** customization pane.</span></span>

![สกรีนช็อตของการย้อนกลับไปเป็นตัวเลือกเริ่มต้น](media/power-bi-visualization-customize-title-background-and-legend/power-bi-revert.png)

## <a name="customize-visualization-backgrounds"></a><span data-ttu-id="66406-141">กำหนดพื้นหลังการแสดงภาพด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="66406-141">Customize visualization backgrounds</span></span>

<span data-ttu-id="66406-142">ด้วยแผนภูมิคอลัมน์แบ่งคลัสเตอร์เดียวกันที่เลือก ขยายตัวเลือก **พื้นหลัง**</span><span class="sxs-lookup"><span data-stu-id="66406-142">With the same clustered column chart selected, expand the **Background** options.</span></span>

1. <span data-ttu-id="66406-143">เลื่อนตัวเลื่อน **พื้นหลัง** ไปยัง **เปิด**</span><span class="sxs-lookup"><span data-stu-id="66406-143">Move the **Background** slider to **On**.</span></span>

1. <span data-ttu-id="66406-144">เลือกเมนูดรอปดาวน์แล้วเลือกสีเทา</span><span class="sxs-lookup"><span data-stu-id="66406-144">Select the drop-down and choose a grey color.</span></span>

1. <span data-ttu-id="66406-145">เปลี่ยน **ความโปร่งใส** เป็น **74%**</span><span class="sxs-lookup"><span data-stu-id="66406-145">Change **Transparency** to **74%**.</span></span>

<span data-ttu-id="66406-146">ณ จุดนี้ในบทช่วยสอน พื้นหลังแผนภูมิคอลัมน์แบบกลุ่มของคุณจะมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="66406-146">At this point in the tutorial, your clustered column chart background will look something like this:</span></span>

![สกรีนช็อตของแผนภูมิคอลัมน์แบบกลุ่มที่ปรับปรุงสีพื้นหลังแล้ว](media/power-bi-visualization-customize-title-background-and-legend/power-bi-background.png)

<span data-ttu-id="66406-148">บันทึกการเปลี่ยนแปลงที่คุณทำและย้ายไปยังส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="66406-148">Save the changes you've made and move to the next section.</span></span>

<span data-ttu-id="66406-149">เมื่อต้องการย้อนกลับการเปลี่ยนแปลงทั้งหมด ให้เลือก **ย้อนกลับไปเป็นค่าเริ่มต้น** ที่ด้านล่างของบานหน้าต่างการกำหนด **พื้นหลัง** ด้วยตัวเอง</span><span class="sxs-lookup"><span data-stu-id="66406-149">If you ever need to revert all of the changes, select **Revert to default**, at the bottom of the **Background** customization pane.</span></span>

## <a name="customize-visualization-legends"></a><span data-ttu-id="66406-150">คำอธิบายแผนภูมิแสดงภาพที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="66406-150">Customize visualization legends</span></span>

1. <span data-ttu-id="66406-151">เปิดหน้ารายงาน **ภาพรวม** และเลือกแผนภูมิ **ผลต่างยอดขายรวมแยกตาม FiscalMonth และผู้จัดการเขต**</span><span class="sxs-lookup"><span data-stu-id="66406-151">Open the **Overview** report page and select the **Total Sales Variance by FiscalMonth and District Manager** chart.</span></span>

1. <span data-ttu-id="66406-152">ในแท็บ **การแสดงผลด้วยภาพ** เลือกไอคอนลูกกลิ้งทาสีเพื่อเปิดบานหน้าต่างรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="66406-152">In the **Visualization** tab, select the paint roller icon to open the Format pane.</span></span>

1. <span data-ttu-id="66406-153">ขยายตัวเลือก **คำอธิบายแผนภูมิ**:</span><span class="sxs-lookup"><span data-stu-id="66406-153">Expand the **Legend** options:</span></span>

    ![ภาพหน้าจอของการ์ดคำอธิบายแผนภูมิ](media/power-bi-visualization-customize-title-background-and-legend/power-bi-legends.png)

1. <span data-ttu-id="66406-155">เลื่อนแถบเลื่อน **คำอธิบายแผนภูมิ** ไปยัง **เปิด**</span><span class="sxs-lookup"><span data-stu-id="66406-155">Move the **Legend** slider to **On**.</span></span>

1. <span data-ttu-id="66406-156">ย้ายคำอธิบายแผนภูมิไปด้านซ้ายของการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="66406-156">Move the legend to the left side of the visualization.</span></span>

1. <span data-ttu-id="66406-157">เพิ่มชื่อคำอธิบายแผนภูมิโดยการสลับ **ชื่อ** ให้เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="66406-157">Add a legend title by toggling **Title** to **On**.</span></span>

1. <span data-ttu-id="66406-158">ป้อน *ผู้จัดการ* ในเขตข้อมูล **ชื่อคำอธิบายแผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="66406-158">Enter *Manager* in the **Legend name** field.</span></span>

1. <span data-ttu-id="66406-159">เปลี่ยน **สี** เป็นสีดำ</span><span class="sxs-lookup"><span data-stu-id="66406-159">Change **Color** to black.</span></span>

<span data-ttu-id="66406-160">บันทึกการเปลี่ยนแปลงที่คุณทำและย้ายไปยังส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="66406-160">Save the changes you've made and move to the next section.</span></span>

<span data-ttu-id="66406-161">เมื่อต้องการย้อนกลับการเปลี่ยนแปลงทั้งหมด ให้เลือก **ย้อนกลับไปเป็นค่าเริ่มต้น** ที่ด้านล่างของบานหน้าต่างการกำหนด **คำอธิบายแผนภูมิ** ด้วยตัวเอง</span><span class="sxs-lookup"><span data-stu-id="66406-161">If you ever need to revert all of the changes, select **Revert to default**, at the bottom of the **Legend** customization pane.</span></span>

## <a name="customize-total-labels-for-stacked-visuals"></a><span data-ttu-id="66406-162">กำหนดป้ายชื่อทั้งหมดสำหรับภาพแบบเรียงซ้อน</span><span class="sxs-lookup"><span data-stu-id="66406-162">Customize total labels for stacked visuals</span></span>
<span data-ttu-id="66406-163">ภาพแบบเรียงซ้อนสามารถแสดงป้ายชื่อข้อมูลและป้ายชื่อทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="66406-163">Stacked visuals can display data labels and total labels.</span></span> <span data-ttu-id="66406-164">ในแผนภูมิคอลัมน์แบบเรียงซ้อน ป้ายชื่อข้อมูลระบุค่าสำหรับแต่ละส่วนของคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="66406-164">On a stacked column chart, data labels identify the value for each portion of a column.</span></span> <span data-ttu-id="66406-165">ป้ายชื่อทั้งหมดจะแสดงค่าผลรวมสำหรับทั้งคอลัมน์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="66406-165">Total labels display the total value for the entire aggregated column.</span></span> 

<span data-ttu-id="66406-166">ดู Rien เพิ่มป้ายชื่อทั้งหมดลงในแผนภูมิแบบเรียงซ้อนแล้วทำตามขั้นตอนด้านล่างเพื่อลองใช้งานด้วยตัวคุณเอง</span><span class="sxs-lookup"><span data-stu-id="66406-166">Watch Rien add total labels to a stacked chart, and then follow the steps below to try it out yourself.</span></span>

> [!VIDEO https://www.youtube.com/embed/OgjX-pFGgfM]

1. <span data-ttu-id="66406-167">เปิดหน้ารายงาน **ภาพรวม** และเลือก แผนภูมิแท่ง **ขนาดพื้นที่การขายโดยเฉลี่ยตามการเกียวโยงและชนิดของร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="66406-167">Open the **Overview** report page and select the **Average selling area size by chain and store type** bar chart.</span></span>

1. <span data-ttu-id="66406-168">ในแท็บ **การแสดงผลด้วยภาพ** เลือก![ไอคอนสำหรับแผนภูมิแท่งแบบเรียงซ้อน](media/power-bi-visualization-customize-title-background-and-legend/power-bi-stacked-bar.png) เพื่อแปลงแผนภูมิแท่งนี้เป็นแผนภูมิแท่งแบบเรียงซ้อน</span><span class="sxs-lookup"><span data-stu-id="66406-168">In the **Visualization** tab, select ![icon for the stacked bar chart](media/power-bi-visualization-customize-title-background-and-legend/power-bi-stacked-bar.png) to convert this bar chart to a stacked bar chart.</span></span> <span data-ttu-id="66406-169">โปรดสังเกตว่าภาพยังคงมีป้ายชื่อข้อมูลอยู่</span><span class="sxs-lookup"><span data-stu-id="66406-169">Notice that the visual retains its data labels.</span></span> 

    ![สกรีนช็อตของแผนภูมิแท่งแบบเรียงซ้อนใหม่](media/power-bi-visualization-customize-title-background-and-legend/power-bi-stacked-chart.png)

1. <span data-ttu-id="66406-171">ในแท็บ **การแสดงผลด้วยภาพ** เลือกไอคอนลูกกลิ้งทาสีเพื่อเปิดบานหน้าต่างรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="66406-171">In the **Visualization** tab, select the paint roller icon to open the Format pane.</span></span>

1. <span data-ttu-id="66406-172">ย้ายแถบเลื่อน **ป้ายชื่อทั้งหมด** ไปเป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="66406-172">Move the **Total labels** slider to **On**.</span></span> 

    ![สกรีนช็อตที่แสดงแถบเลื่อนป้ายชื่อทั้งหมดที่ตั้งเป็นเปิด](media/power-bi-visualization-customize-title-background-and-legend/power-bi-totals.png)

1. <span data-ttu-id="66406-174">อีกทางหนึ่งคือจัดรูปแบบป้ายชื่อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="66406-174">Optionally, format the total labels.</span></span> <span data-ttu-id="66406-175">ในตัวอย่างนี้ เราได้เปลี่ยนสีเป็นสีดำ เพิ่มขนาดฟอนต์ และเลือกที่จะแสดงค่าเป็น **หลักพัน**</span><span class="sxs-lookup"><span data-stu-id="66406-175">In this example, we've changed color to black, increased font size, and opted to display the values as **Thousands**.</span></span>

    ![สกรีนช็อตของแผนภูมิแท่งแบบเรียงซ้อนทั้งหมดใหม่](media/power-bi-visualization-customize-title-background-and-legend/power-bi-bar-totals.png)

## <a name="customize-colors-using-a-theme"></a><span data-ttu-id="66406-177">ปรับแต่งสีเองโดยใช้ธีม</span><span class="sxs-lookup"><span data-stu-id="66406-177">Customize colors using a theme</span></span>

<span data-ttu-id="66406-178">ด้วยธีมรายงาน คุณสามารถใช้การเปลี่ยนแปลงการออกแบบกับรายงานทั้งหมดของคุณได้ เช่น การใช้สีสำหรับองค์กร การเปลี่ยนชุดไอคอน หรือการใช้การจัดรูปแบบภาพตามค่าเริ่มต้นใหม่</span><span class="sxs-lookup"><span data-stu-id="66406-178">With report themes you can apply design changes to your entire report, such as using corporate colors, changing icon sets, or applying new default visual formatting.</span></span> <span data-ttu-id="66406-179">เมื่อคุณใช้ธีมรายงาน การแสดงผลด้วยภาพทั้งหมดในรายงานของคุณจะใช้สีและการจัดรูปแบบจากธีมที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="66406-179">When you apply a report theme, all visuals in your report use the colors and formatting from your selected theme.</span></span>

<span data-ttu-id="66406-180">เมื่อต้องการนำธีมไปใช้กับรายงานของคุณ ให้เลือก **สลับธีม** จากแถบเมนู</span><span class="sxs-lookup"><span data-stu-id="66406-180">To apply a theme to your report, select **Switch theme** from the menu bar.</span></span> <span data-ttu-id="66406-181">เลือกธีม</span><span class="sxs-lookup"><span data-stu-id="66406-181">Choose a theme.</span></span>  <span data-ttu-id="66406-182">รายงานด้านล่างใช้ธีม **Solar**</span><span class="sxs-lookup"><span data-stu-id="66406-182">The report below uses the **Solar** theme.</span></span>

 
![รายงานที่ใช้ธีม Solar ซึ่งประกอบด้วยสีเหลือง ส้ม และแดง](media/power-bi-visualization-customize-title-background-and-legend/power-bi-theme.png)

## <a name="visualization-types-that-you-can-customize"></a><span data-ttu-id="66406-184">ชนิดการแสดงผลด้วยภาพที่สามารถกำหนดเองได้</span><span class="sxs-lookup"><span data-stu-id="66406-184">Visualization types that you can customize</span></span>

<span data-ttu-id="66406-185">นี่คือรายการของการแสดงผลด้วยภาพและตัวเลือกที่กำหนดเองที่พร้อมใช้งานสำหรับแต่ละส่วน:</span><span class="sxs-lookup"><span data-stu-id="66406-185">Here is a list of the visualizations and the customization options that are available for each:</span></span>

| <span data-ttu-id="66406-186">การแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="66406-186">Visualization</span></span> | <span data-ttu-id="66406-187">ชื่อเรื่อง</span><span class="sxs-lookup"><span data-stu-id="66406-187">Title</span></span> | <span data-ttu-id="66406-188">พื้นหลัง</span><span class="sxs-lookup"><span data-stu-id="66406-188">Background</span></span> | <span data-ttu-id="66406-189">คำอธิบายแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="66406-189">Legend</span></span> | <span data-ttu-id="66406-190">ป้ายชื่อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="66406-190">Total labels</span></span>
|:--- |:--- |:--- |:--- |:--- |
| <span data-ttu-id="66406-191">พื้นที่</span><span class="sxs-lookup"><span data-stu-id="66406-191">Area</span></span> | <span data-ttu-id="66406-192">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-192">yes</span></span> | <span data-ttu-id="66406-193">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-193">yes</span></span> |<span data-ttu-id="66406-194">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-194">yes</span></span> | <span data-ttu-id="66406-195">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-195">yes</span></span>  |
| <span data-ttu-id="66406-196">แผนภูมิแท่ง</span><span class="sxs-lookup"><span data-stu-id="66406-196">Bar</span></span> | <span data-ttu-id="66406-197">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-197">yes</span></span> | <span data-ttu-id="66406-198">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-198">yes</span></span> |<span data-ttu-id="66406-199">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-199">yes</span></span> | <span data-ttu-id="66406-200">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-200">yes</span></span> |
| <span data-ttu-id="66406-201">การ์ด</span><span class="sxs-lookup"><span data-stu-id="66406-201">Card</span></span> | <span data-ttu-id="66406-202">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-202">yes</span></span> | <span data-ttu-id="66406-203">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-203">yes</span></span> |<span data-ttu-id="66406-204">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-204">n/a</span></span> | <span data-ttu-id="66406-205">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-205">n/a</span></span> |
| <span data-ttu-id="66406-206">การ์ดแบบหลายแถว</span><span class="sxs-lookup"><span data-stu-id="66406-206">Multi-row Card</span></span> | <span data-ttu-id="66406-207">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-207">yes</span></span> | <span data-ttu-id="66406-208">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-208">yes</span></span> | <span data-ttu-id="66406-209">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-209">n/a</span></span> | <span data-ttu-id="66406-210">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-210">n/a</span></span> |
| <span data-ttu-id="66406-211">คอลัมน์แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="66406-211">Column</span></span> | <span data-ttu-id="66406-212">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-212">yes</span></span> | <span data-ttu-id="66406-213">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-213">yes</span></span> | <span data-ttu-id="66406-214">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-214">yes</span></span> |  <span data-ttu-id="66406-215">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-215">yes</span></span> |
| <span data-ttu-id="66406-216">ผสม</span><span class="sxs-lookup"><span data-stu-id="66406-216">Combo</span></span> | <span data-ttu-id="66406-217">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-217">yes</span></span> | <span data-ttu-id="66406-218">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-218">yes</span></span> | <span data-ttu-id="66406-219">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-219">yes</span></span> | <span data-ttu-id="66406-220">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-220">yes</span></span> |
| <span data-ttu-id="66406-221">แผนภูมิโดนัท</span><span class="sxs-lookup"><span data-stu-id="66406-221">Donut</span></span> | <span data-ttu-id="66406-222">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-222">yes</span></span> | <span data-ttu-id="66406-223">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-223">yes</span></span> | <span data-ttu-id="66406-224">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-224">yes</span></span> | <span data-ttu-id="66406-225">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-225">n/a</span></span> |
| <span data-ttu-id="66406-226">แผนที่แถบสี</span><span class="sxs-lookup"><span data-stu-id="66406-226">Filled map</span></span> | <span data-ttu-id="66406-227">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-227">yes</span></span> | <span data-ttu-id="66406-228">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-228">yes</span></span> | <span data-ttu-id="66406-229">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-229">yes</span></span> |<span data-ttu-id="66406-230">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-230">n/a</span></span> |
| <span data-ttu-id="66406-231">แผนภูมิกรวย</span><span class="sxs-lookup"><span data-stu-id="66406-231">Funnel</span></span> | <span data-ttu-id="66406-232">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-232">yes</span></span> | <span data-ttu-id="66406-233">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-233">yes</span></span> | <span data-ttu-id="66406-234">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-234">n/a</span></span> |<span data-ttu-id="66406-235">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-235">n/a</span></span> |
| <span data-ttu-id="66406-236">ตัววัด</span><span class="sxs-lookup"><span data-stu-id="66406-236">Gauge</span></span> | <span data-ttu-id="66406-237">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-237">yes</span></span> | <span data-ttu-id="66406-238">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-238">yes</span></span> | <span data-ttu-id="66406-239">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-239">n/a</span></span> |<span data-ttu-id="66406-240">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-240">n/a</span></span> |
| <span data-ttu-id="66406-241">ผู้มีอิทธิพลหลัก</span><span class="sxs-lookup"><span data-stu-id="66406-241">Key Influencer</span></span> | <span data-ttu-id="66406-242">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-242">yes</span></span> | <span data-ttu-id="66406-243">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-243">yes</span></span> | <span data-ttu-id="66406-244">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-244">n/a</span></span> |<span data-ttu-id="66406-245">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-245">n/a</span></span> |
| <span data-ttu-id="66406-246">KPI</span><span class="sxs-lookup"><span data-stu-id="66406-246">KPI</span></span> | <span data-ttu-id="66406-247">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-247">yes</span></span> | <span data-ttu-id="66406-248">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-248">yes</span></span> | <span data-ttu-id="66406-249">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-249">n/a</span></span> |<span data-ttu-id="66406-250">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-250">n/a</span></span> |
| <span data-ttu-id="66406-251">เส้น</span><span class="sxs-lookup"><span data-stu-id="66406-251">Line</span></span> | <span data-ttu-id="66406-252">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-252">yes</span></span> | <span data-ttu-id="66406-253">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-253">yes</span></span> | <span data-ttu-id="66406-254">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-254">yes</span></span> |<span data-ttu-id="66406-255">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-255">n/a</span></span> |
| <span data-ttu-id="66406-256">แผนที่</span><span class="sxs-lookup"><span data-stu-id="66406-256">Map</span></span> | <span data-ttu-id="66406-257">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-257">yes</span></span> | <span data-ttu-id="66406-258">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-258">yes</span></span> | <span data-ttu-id="66406-259">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-259">yes</span></span> |<span data-ttu-id="66406-260">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-260">n/a</span></span> |
| <span data-ttu-id="66406-261">เมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="66406-261">Matrix</span></span> | <span data-ttu-id="66406-262">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-262">yes</span></span> | <span data-ttu-id="66406-263">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-263">yes</span></span> | <span data-ttu-id="66406-264">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-264">n/a</span></span> |<span data-ttu-id="66406-265">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-265">yes</span></span> |
| <span data-ttu-id="66406-266">แผนภูมิวงกลม</span><span class="sxs-lookup"><span data-stu-id="66406-266">Pie</span></span> | <span data-ttu-id="66406-267">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-267">yes</span></span> | <span data-ttu-id="66406-268">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-268">yes</span></span> | <span data-ttu-id="66406-269">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-269">yes</span></span> |<span data-ttu-id="66406-270">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-270">n/a</span></span> |
| <span data-ttu-id="66406-271">ถามตอบ</span><span class="sxs-lookup"><span data-stu-id="66406-271">Q&A</span></span> | <span data-ttu-id="66406-272">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-272">yes</span></span> | <span data-ttu-id="66406-273">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-273">yes</span></span> | <span data-ttu-id="66406-274">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-274">n/a</span></span> |<span data-ttu-id="66406-275">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-275">n/a</span></span> |
| <span data-ttu-id="66406-276">แผนภูมิกระจาย</span><span class="sxs-lookup"><span data-stu-id="66406-276">Scatter</span></span> | <span data-ttu-id="66406-277">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-277">yes</span></span> | <span data-ttu-id="66406-278">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-278">yes</span></span> | <span data-ttu-id="66406-279">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-279">yes</span></span> |<span data-ttu-id="66406-280">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-280">n/a</span></span> |
| <span data-ttu-id="66406-281">รูปร่าง</span><span class="sxs-lookup"><span data-stu-id="66406-281">Shape</span></span> | <span data-ttu-id="66406-282">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-282">yes</span></span> | <span data-ttu-id="66406-283">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-283">yes</span></span> | <span data-ttu-id="66406-284">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-284">yes</span></span> |<span data-ttu-id="66406-285">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-285">n/a</span></span> |
| <span data-ttu-id="66406-286">ตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="66406-286">Slicer</span></span> | <span data-ttu-id="66406-287">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-287">yes</span></span> | <span data-ttu-id="66406-288">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-288">yes</span></span> | <span data-ttu-id="66406-289">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-289">n/a</span></span> |<span data-ttu-id="66406-290">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-290">n/a</span></span> |
| <span data-ttu-id="66406-291">ตาราง</span><span class="sxs-lookup"><span data-stu-id="66406-291">Table</span></span> | <span data-ttu-id="66406-292">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-292">yes</span></span> | <span data-ttu-id="66406-293">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-293">yes</span></span> | <span data-ttu-id="66406-294">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-294">n/a</span></span> |<span data-ttu-id="66406-295">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-295">yes</span></span> |
| <span data-ttu-id="66406-296">กล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="66406-296">Textbox</span></span> | <span data-ttu-id="66406-297">ไม่</span><span class="sxs-lookup"><span data-stu-id="66406-297">no</span></span> | <span data-ttu-id="66406-298">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-298">yes</span></span> | <span data-ttu-id="66406-299">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-299">n/a</span></span> |<span data-ttu-id="66406-300">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-300">n/a</span></span> |
| <span data-ttu-id="66406-301">แผนที่ต้นไม้</span><span class="sxs-lookup"><span data-stu-id="66406-301">Treemap</span></span> | <span data-ttu-id="66406-302">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-302">yes</span></span> | <span data-ttu-id="66406-303">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-303">yes</span></span> | <span data-ttu-id="66406-304">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-304">yes</span></span> |<span data-ttu-id="66406-305">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-305">n/a</span></span> |
| <span data-ttu-id="66406-306">น้ำตก</span><span class="sxs-lookup"><span data-stu-id="66406-306">Waterfall</span></span> | <span data-ttu-id="66406-307">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-307">yes</span></span> | <span data-ttu-id="66406-308">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-308">yes</span></span> | <span data-ttu-id="66406-309">ใช่</span><span class="sxs-lookup"><span data-stu-id="66406-309">yes</span></span> |<span data-ttu-id="66406-310">n/a</span><span class="sxs-lookup"><span data-stu-id="66406-310">n/a</span></span> |

## <a name="next-steps"></a><span data-ttu-id="66406-311">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="66406-311">Next steps</span></span>

- [<span data-ttu-id="66406-312">คุณสมบัติแกน X และแกน Y ที่กำหนดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="66406-312">Customize X-Axis and Y-Axis properties</span></span>](power-bi-visualization-customize-x-axis-and-y-axis.md)

- [<span data-ttu-id="66406-313">เริ่มใช้งานด้วยคุณสมบัติแกนและการจัดรูปแบบสี</span><span class="sxs-lookup"><span data-stu-id="66406-313">Getting started with color formatting and axis properties</span></span>](service-getting-started-with-color-formatting-and-axis-properties.md)

<span data-ttu-id="66406-314">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="66406-314">More questions?</span></span> [<span data-ttu-id="66406-315">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="66406-315">Try the Power BI Community</span></span>](https://community.powerbi.com/)


