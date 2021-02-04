---
title: ภาพตัวบ่งชี้ประสิทธิภาพหลัก (KPI)
description: สร้างภาพตัวบ่งชี้ประสิทธิภาพหลัก (KPI) ใน Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
featuredvideoid: ''
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 01/30/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 448115ea6cde6c85a7bd3386890f483d71882ad5
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418944"
---
# <a name="create-key-performance-indicator-kpi-visualizations"></a><span data-ttu-id="d57e0-103">สร้างการแสดงภาพตัวบ่งชี้ประสิทธิภาพหลัก (KPI)</span><span class="sxs-lookup"><span data-stu-id="d57e0-103">Create key performance indicator (KPI) visualizations</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="d57e0-104">ดัชนีประสิทธิภาพหลัก (KPI) เป็นภาพสัญลักษณ์ที่แสดงปริมาณความก้าวหน้าของงานที่ทำเพื่อมุ่งไปยังเป้าหมายที่วัดผลได้</span><span class="sxs-lookup"><span data-stu-id="d57e0-104">A Key Performance Indicator (KPI) is a visual cue that communicates the amount of progress made toward a measurable goal.</span></span> <span data-ttu-id="d57e0-105">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ KPI โปรดดู [ตัวบ่งชี้ประสิทธิภาพหลัก (KPI) ใน PowerPivot](https://support.office.com/en-us/article/Key-Performance-Indicators-KPIs-in-Power-Pivot-E653EDEF-8A21-40E4-9ECE-83A6C8C306AA)</span><span class="sxs-lookup"><span data-stu-id="d57e0-105">For more about KPIs, see [Key Performance Indicators (KPIs) in PowerPivot](https://support.office.com/en-us/article/Key-Performance-Indicators-KPIs-in-Power-Pivot-E653EDEF-8A21-40E4-9ECE-83A6C8C306AA).</span></span>


## <a name="when-to-use-a-kpi"></a><span data-ttu-id="d57e0-106">เมื่อต้องการใช้ KPI</span><span class="sxs-lookup"><span data-stu-id="d57e0-106">When to use a KPI</span></span>

<span data-ttu-id="d57e0-107">KPI เป็นตัวเลือกที่ดีที่สุด:</span><span class="sxs-lookup"><span data-stu-id="d57e0-107">KPIs are a great choice:</span></span>

* <span data-ttu-id="d57e0-108">การวัดความคืบหน้า</span><span class="sxs-lookup"><span data-stu-id="d57e0-108">To measure progress.</span></span> <span data-ttu-id="d57e0-109">ตอบคำถาม "ฉันน้ำนำหน้าหรือตามหลังสิ่งใดอยู่"?</span><span class="sxs-lookup"><span data-stu-id="d57e0-109">Answers the question, "What am I ahead or behind on?"</span></span>

* <span data-ttu-id="d57e0-110">การวัดระยะห่างเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="d57e0-110">To measure distance to a goal.</span></span> <span data-ttu-id="d57e0-111">ตอบคำถาม "ฉันน้ำนำหน้าหรือตามหลังอยู่ไกลเท่าใด"?</span><span class="sxs-lookup"><span data-stu-id="d57e0-111">Answers the question, "How far ahead or behind am I?"</span></span>

## <a name="kpi-requirements"></a><span data-ttu-id="d57e0-112">ข้อกำหนดของ KPI</span><span class="sxs-lookup"><span data-stu-id="d57e0-112">KPI requirements</span></span>

<span data-ttu-id="d57e0-113">ตัวออกแบบวัดภาพ KPI ตามหน่วยวัดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="d57e0-113">A designer bases a KPI visual on a specific measure.</span></span> <span data-ttu-id="d57e0-114">เป้าหมายของ KPI คือช่วยให้คุณประเมินค่าและสถานะปัจจุบันเทียบกับเป้าหมายที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="d57e0-114">The intention of the KPI is to help you evaluate the current value and status of a metric against a defined target.</span></span> <span data-ttu-id="d57e0-115">ภาพ KPI จำเป็นต้องมีการวัด *พื้นฐาน* ที่ประเมินเป็นค่าและการวัดหรือค่า *เป้าหมาย* *ค่าเกณฑ์* หรือ *จุดหมาย*</span><span class="sxs-lookup"><span data-stu-id="d57e0-115">A KPI visual requires a *base* measure that evaluates to a value, a *target* measure or value, and a *threshold* or *goal*.</span></span>

<span data-ttu-id="d57e0-116">ชุดข้อมูล KPI จำเป็นต้องประกอบด้วยค่าเป้าหมายสำหรับ KPI</span><span class="sxs-lookup"><span data-stu-id="d57e0-116">A KPI dataset needs to contain goal values for a KPI.</span></span> <span data-ttu-id="d57e0-117">ถ้าชุดข้อมูลของคุณไม่ประกอบด้วยค่าเป้าหมาย คุณสามารถสร้างค่าเป้าหมายโดยการเพิ่มแผ่นงาน Excel ที่แสดงค่าเป้าหมาย ให้กับรูปแบบข้อมูลหรือไฟล์ PBIX ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d57e0-117">If your dataset doesn't contain goal values, you can create them by adding an Excel sheet with goals to your data model or PBIX file.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d57e0-118">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="d57e0-118">Prerequisites</span></span>

<span data-ttu-id="d57e0-119">บทช่วยสอนนี้ใช้[ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix)</span><span class="sxs-lookup"><span data-stu-id="d57e0-119">This tutorial uses the [Retail Analysis sample PBIX file](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix).</span></span>

1. <span data-ttu-id="d57e0-120">จากด้านบนซ้ายของแถบเมนู เลือก **ไฟล์** > **เปิด**</span><span class="sxs-lookup"><span data-stu-id="d57e0-120">From the upper left section of the menubar, select **File** > **Open**</span></span>

1. <span data-ttu-id="d57e0-121">ค้นหาสำเนา **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก**</span><span class="sxs-lookup"><span data-stu-id="d57e0-121">Find your copy of the **Retail Analysis sample PBIX file**</span></span>

1. <span data-ttu-id="d57e0-122">เปิด **ไฟล์ PBIX ตัวอย่างการวิเคราะห์ด้านการขายปลีก** ในมุมมองรายงาน</span><span class="sxs-lookup"><span data-stu-id="d57e0-122">Open the **Retail Analysis sample PBIX file** in report view.</span></span> <span data-ttu-id="d57e0-123">![สกรีนช็อตของไอคอนมุมมองรายงาน](media/power-bi-visualization-kpi/power-bi-report-view.png)</span><span class="sxs-lookup"><span data-stu-id="d57e0-123">![Screenshot of the report view icon.](media/power-bi-visualization-kpi/power-bi-report-view.png)</span></span>

1. <span data-ttu-id="d57e0-124">เลือ **+** เพื่อเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="d57e0-124">Select **+** to add a new page.</span></span> <span data-ttu-id="d57e0-125">![สกรีนช็อตของแท็บสีเหลือง](media/power-bi-visualization-kpi/power-bi-yellow-tab.png)</span><span class="sxs-lookup"><span data-stu-id="d57e0-125">![Screenshot of the yellow tab.](media/power-bi-visualization-kpi/power-bi-yellow-tab.png)</span></span>

> [!NOTE]
> <span data-ttu-id="d57e0-126">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="d57e0-126">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span>    

## <a name="how-to-create-a-kpi"></a><span data-ttu-id="d57e0-127">วิธีการสร้าง KPI</span><span class="sxs-lookup"><span data-stu-id="d57e0-127">How to create a KPI</span></span>

<span data-ttu-id="d57e0-128">ในตัวอย่างนี้ คุณจะสร้าง KPI เพื่อวัดความคืบหน้าที่คุณได้ทำเพื่อบรรลุเป้าหมายยอดขาย</span><span class="sxs-lookup"><span data-stu-id="d57e0-128">In this example, you'll create a KPI that measures the progress you've made toward a sales goal.</span></span>

1. <span data-ttu-id="d57e0-129">จากบานหน้าต่าง **เขตข้อมูล** ให้เลือก **ยอดขาย > หน่วยรวมปีนี้**</span><span class="sxs-lookup"><span data-stu-id="d57e0-129">From the **Fields** pane, select **Sales > Total Units This Year**.</span></span>  <span data-ttu-id="d57e0-130">ค่านี้จะเป็นตัวดัชนี</span><span class="sxs-lookup"><span data-stu-id="d57e0-130">This value will be the indicator.</span></span>

1. <span data-ttu-id="d57e0-131">เพิ่ม **เวลา > เดือนการเงิน**</span><span class="sxs-lookup"><span data-stu-id="d57e0-131">Add **Time > FiscalMonth**.</span></span>  <span data-ttu-id="d57e0-132">ค่านี้จะแสดงแนวโน้ม</span><span class="sxs-lookup"><span data-stu-id="d57e0-132">This value will represent the trend.</span></span>

1. <span data-ttu-id="d57e0-133">ในมุมขวาบนของภาพ เลือกจุดไข่ปลา และตรวจสอบว่า Power BI เรียงลำดับคอลัมน์ตาม **เดือนงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="d57e0-133">In the upper-right corner of the visual, select the ellipsis and check that Power BI sorted the columns in ascending order by **FiscalMonth**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="d57e0-134">เมื่อคุณแปลงการแสดงภาพเป็น KPI จึง **ไม่มี** ตัวเลือกการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="d57e0-134">Once you convert the visualization to a KPI, there's **no** option to sort.</span></span> <span data-ttu-id="d57e0-135">คุณต้องเรียงลำดับอย่างถูกต้องในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="d57e0-135">You must sort it correctly now.</span></span>

    ![สกรีนช็อตของเมนูจุดไข่ปลาขยาย ด้วยการเรียงลำดับจากน้อยไปมากและเดือนงบประมาณที่เลือก](media/power-bi-visualization-kpi/power-bi-ascending-by-fiscal-month.png)

    <span data-ttu-id="d57e0-137">เมื่อเรียงลำดับอย่างถูกต้อง ภาพของคุณจะมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="d57e0-137">Once sorted correctly, your visual will look like this:</span></span>

    ![สกรีนช็อตของภาพเรียงลำดับอย่างถูกต้อง](media/power-bi-visualization-kpi/power-bi-chart.png)

1. <span data-ttu-id="d57e0-139">แปลงภาพเป็น KPI โดยเลือกไอคอน **KPI** จากบานหน้าต่าง **การแสดงภาพ**</span><span class="sxs-lookup"><span data-stu-id="d57e0-139">Convert the visual to a KPI by selecting the **KPI** icon from the **Visualization** pane.</span></span>

    ![สกรีนช็อตของบานหน้าต่างการแสดงภาพที่มีไอคอน KPI แสดงอยู่](media/power-bi-visualization-kpi/power-bi-kpi-template.png)

1. <span data-ttu-id="d57e0-141">หากต้องการเพิ่งเป้าหมาย ลาก **หน่วยรวมปีที่แล้ว** ไปยังเขตข้อมูล **เป้าหมาย**</span><span class="sxs-lookup"><span data-stu-id="d57e0-141">To add a goal, drag **Total Units Last Year** to the **Target goals** field.</span></span>

    ![สกรีนช็อตของภาพ KPI ที่เสร็จแล้วและบานหน้าต่างเขตข้อมูลที่มีค่าแสดงไว้](media/power-bi-visualization-kpi/power-bi-kpi-done.png)

1. <span data-ttu-id="d57e0-143">อีกทางหนึ่งคือ จัดรูปแบบ KPI โดยเลือกไอคอน ลูกกลิ้งทาสี เพื่อเปิดบานหน้าต่างการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="d57e0-143">Optionally, format the KPI by selecting the paint roller icon to open the Formatting pane.</span></span>

    * <span data-ttu-id="d57e0-144">**ตัวดัชนี** - ควบคุมหน่วยแสดงผลของตัวดัชนีและตำแหน่งทศนิยม</span><span class="sxs-lookup"><span data-stu-id="d57e0-144">**Indicator** - controls the indicator’s display units and decimal places.</span></span>

    * <span data-ttu-id="d57e0-145">**แกนแนวโน้ม** - เมื่อตั้งค่าเป็น **เปิด** ภาพจะแสดงแกนแนวโน้มเป็นพื้นหลังของภาพ KPI</span><span class="sxs-lookup"><span data-stu-id="d57e0-145">**Trend axis** - when set to **On**, the visual shows the trend axis as the background of the KPI visual.</span></span>  

    * <span data-ttu-id="d57e0-146">**เป้าหมาย** - เมื่อตั้งค่าเป็น **เปิด** ภาพจะแสดงเป้าหมายและระยะห่างจากเป้าหมายเป็นเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="d57e0-146">**Goals** - when set to **On**, the visual shows the goal and the distance from the goal as a percentage.</span></span>

    * <span data-ttu-id="d57e0-147">**รหัสสี > ทิศทาง** - ผู้คนจะพิจารณา KPI บางส่วนว่า ดีกว่า เมื่อมีค่า *สูงกว่า* และพิจารณา KPI บางส่วนว่า *ดีกว่า* เมื่อมีค่าต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="d57e0-147">**Color coding > Direction** - people consider some KPIs better for *higher* values and consider some better for *lower* values.</span></span> <span data-ttu-id="d57e0-148">ตัวอย่างเช่น กำไรเทียบกับเวลารอ</span><span class="sxs-lookup"><span data-stu-id="d57e0-148">For example, earnings versus wait time.</span></span> <span data-ttu-id="d57e0-149">โดยทั่วไปแล้ว กำไรที่สูงขึ้นจะดีกว่าเมื่อเทียบกับค่าสูงขึ้นของเวลารอ</span><span class="sxs-lookup"><span data-stu-id="d57e0-149">Typically a higher value of earnings is better versus a higher value of wait time.</span></span> <span data-ttu-id="d57e0-150">เลือก **สูงขึ้นดีกว่า** และเลือกเปลี่ยนการตั้งค่าสีได้</span><span class="sxs-lookup"><span data-stu-id="d57e0-150">Select **high is good** and, optionally, change the color settings.</span></span>

<span data-ttu-id="d57e0-151">KPI ยังมีให้บริการในบริการของ Power BI และจากอุปกรณ์มือถือของคุณและติดตั้งได้ง่ายๆ</span><span class="sxs-lookup"><span data-stu-id="d57e0-151">KPIs are also available in the Power BI service and on your mobile devices.</span></span> <span data-ttu-id="d57e0-152">ช่วยให้คุณสามารถเลือกที่จะเชื่อมต่อกับความคืบหน้าของธุรกิจของคุณได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="d57e0-152">It gives you the option to be always connected to your business's heartbeat.</span></span>

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="d57e0-153">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="d57e0-153">Considerations and troubleshooting</span></span>

<span data-ttu-id="d57e0-154">ถ้า KPI ของคุณไม่มีลักษณะคล้ายกับด้านบน อาจเป็นเพราะคุณไม่ได้จัดเรียงตาม **เดือนงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="d57e0-154">If your KPI doesn't look like the one above, it may be because you didn't sort by **FiscalMonth**.</span></span> <span data-ttu-id="d57e0-155">KPI ไม่มีตัวเลือกการจัดเรียง</span><span class="sxs-lookup"><span data-stu-id="d57e0-155">KPIs don't have a sort option.</span></span> <span data-ttu-id="d57e0-156">คุณจะต้องเริ่มต้นใหม่อีกครั้งและจัดเรียงตาม **FiscalMonth** *ก่อน* ที่คุณจะแปลงการแสดงภาพของคุณเป็น KPI</span><span class="sxs-lookup"><span data-stu-id="d57e0-156">You'll need to start again and sort by **FiscalMonth** *before* you convert your visualization to a KPI.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d57e0-157">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d57e0-157">Next steps</span></span>

* [<span data-ttu-id="d57e0-158">เคล็ดลับและลูกเล่นในการแสดงข้อมูลแผนที่ Power BI</span><span class="sxs-lookup"><span data-stu-id="d57e0-158">Tips and Tricks for Power BI Map visualizations</span></span>](power-bi-map-tips-and-tricks.md)

* [<span data-ttu-id="d57e0-159">ชนิดการแสดงภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="d57e0-159">Visualization types in Power BI</span></span>](power-bi-visualization-types-for-reports-and-q-and-a.md)

<span data-ttu-id="d57e0-160">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d57e0-160">More questions?</span></span> [<span data-ttu-id="d57e0-161">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="d57e0-161">Try the Power BI Community</span></span>](https://community.powerbi.com/)
