---
title: แผนภูมิกรวย
description: แผนภูมิกรวยใน Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
featuredvideoid: qKRZPBnaUXM
ms.custom: video-qKRZPBnaUXM
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 05/05/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 38b33ad06123b64dd049dbae6ee67d6452da806e
ms.sourcegitcommit: 8250187368d3de48663eb516a816ff701119b579
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/10/2020
ms.locfileid: "96998380"
---
# <a name="create-and-use-funnel-charts"></a><span data-ttu-id="d49ad-103">สร้างและใช้แผนภูมิกรวย</span><span class="sxs-lookup"><span data-stu-id="d49ad-103">Create and use funnel charts</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="d49ad-104">แผนภูมิกรวยช่วยให้คุณแสดงกระบวนการเส้นตรง ที่แบ่งเป็นขั้นตอนที่เชื่อมต่อกันตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="d49ad-104">A funnel chart helps you visualize a linear process that has sequential connected stages.</span></span> <span data-ttu-id="d49ad-105">ยกตัวอย่างเช่น ช่วงระยะการขายที่มีการติดตามลูกค้าตามขั้นตอนดังนี้: ลูกค้าที่เป็นเป้าหมาย\>ลูกค้าเป้าหมายที่มีคุณสมบัติ\>ผู้ที่มีแนวโน้มจะเป็นลูกค้า\>ทำสัญญา\>ปิดลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d49ad-105">For example, a sales funnel that tracks customers through stages: Lead \> Qualified Lead \> Prospect \> Contract \> Close.</span></span>  <span data-ttu-id="d49ad-106">มองอย่างรวดเร็ว รูปร่างของกรวยบ่งบอกสุขภาพของกระบวนการที่คุณกำลังติดตาม</span><span class="sxs-lookup"><span data-stu-id="d49ad-106">At a glance, the shape of the funnel conveys the health of the process you're tracking.</span></span>

<span data-ttu-id="d49ad-107">แต่ละขั้นตอนกรวยการแสดงเปอร์เซ็นต์ของผลรวม</span><span class="sxs-lookup"><span data-stu-id="d49ad-107">Each funnel stage represents a percentage of the total.</span></span> <span data-ttu-id="d49ad-108">ดังนั้น ในกรณีส่วนใหญ่ แผนภูมิกรวยจะมีรูปเหมือนกรวย - ด้วยขั้นตอนแรกที่ใหญ่ที่สุด และขั้นตอนถัด ๆ มาเล็กกว่าขั้นตอนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="d49ad-108">So, in most cases, a funnel chart is shaped like a funnel -- with the first stage being the largest, and each subsequent stage smaller than its predecessor.</span></span>  <span data-ttu-id="d49ad-109">แผนภูมิเป็นรูปต้นแพร์จะยังมีประโยชน์ -- สามารถใช้ระบุปัญหาในกระบวนการได้</span><span class="sxs-lookup"><span data-stu-id="d49ad-109">A pear-shaped funnel is also useful -- it can identify a problem in the process.</span></span>  <span data-ttu-id="d49ad-110">แต่โดยทั่วไปแล้ว ขั้นแรกหรือขั้น "ทางเข้า" มีขนาดใหญ่ที่สุด</span><span class="sxs-lookup"><span data-stu-id="d49ad-110">But typically, the first stage, the "intake" stage, is the largest.</span></span>

![ตัวอย่างสีน้ำเงินกรวย](media/power-bi-visualization-funnel-charts/funnelplain.png)

> [!NOTE]
> <span data-ttu-id="d49ad-112">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="d49ad-112">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span>    

## <a name="when-to-use-a-funnel-chart"></a><span data-ttu-id="d49ad-113">เมื่อใดที่ใช้แผนภูมิกรวย</span><span class="sxs-lookup"><span data-stu-id="d49ad-113">When to use a funnel chart</span></span>
<span data-ttu-id="d49ad-114">แผนภูมิกรวยเป็นตัวเลือกที่ดีสำหรับ:</span><span class="sxs-lookup"><span data-stu-id="d49ad-114">Funnel charts are a great choice:</span></span>

* <span data-ttu-id="d49ad-115">เมื่อข้อมูลมีลำดับ และผ่านไปตามลำดับขั้นอย่างน้อย 4 ขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="d49ad-115">when the data is sequential and moves through at least 4 stages.</span></span>
* <span data-ttu-id="d49ad-116">เมื่อจำนวนของ "รายการ" ในขั้นตอนแรกคาดว่า จะมีค่ามากกว่าจำนวนในขั้นตอนสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="d49ad-116">when the number of "items" in the first stage is expected to be greater than the number in the final stage.</span></span>
* <span data-ttu-id="d49ad-117">เพื่อคำนวณโอกาสที่จะเกิดขึ้น (รายได้/ยอดขาย/ข้อตกลง/ฯลฯ) ตามลำดับขั้น</span><span class="sxs-lookup"><span data-stu-id="d49ad-117">to calculate potential (revenue/sales/deals/etc.) by stages.</span></span>
* <span data-ttu-id="d49ad-118">เพื่อคำนวณและติดตาม อัตราการแปลงและการรักษาสถานภาพ</span><span class="sxs-lookup"><span data-stu-id="d49ad-118">to calculate and track conversion and retention rates.</span></span>
* <span data-ttu-id="d49ad-119">เพื่อเปิดเผยปัญหาคอขวดในกระบวนการที่เป็นเส้นตรง</span><span class="sxs-lookup"><span data-stu-id="d49ad-119">to reveal bottlenecks in a linear process.</span></span>
* <span data-ttu-id="d49ad-120">เพื่อติดตามเวิร์กโฟลว์ของตะกร้าสินค้า</span><span class="sxs-lookup"><span data-stu-id="d49ad-120">to track a shopping cart workflow.</span></span>
* <span data-ttu-id="d49ad-121">เพื่อติดตามความคืบหน้าและความสำเร็จของแคมเปญ การคลิกโฆษณา/การตลาด</span><span class="sxs-lookup"><span data-stu-id="d49ad-121">to track the progress and success of click-through advertising/marketing campaigns.</span></span>

## <a name="working-with-funnel-charts"></a><span data-ttu-id="d49ad-122">การทำงานกับแผนภูมิกรวย</span><span class="sxs-lookup"><span data-stu-id="d49ad-122">Working with funnel charts</span></span>
<span data-ttu-id="d49ad-123">แผนภูมิกรวย:</span><span class="sxs-lookup"><span data-stu-id="d49ad-123">Funnel charts:</span></span>

* <span data-ttu-id="d49ad-124">สามารถเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="d49ad-124">Can be sorted.</span></span>
* <span data-ttu-id="d49ad-125">สนับสนุนตัวเลขที่เป็นจำนวนเท่า</span><span class="sxs-lookup"><span data-stu-id="d49ad-125">Support multiples.</span></span>
* <span data-ttu-id="d49ad-126">สามารถไฮไลต์เชื่อมโยง และกรองข้าม จากการแสดงภาพอื่น ๆ บนหน้ารายงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="d49ad-126">Can be highlighted and cross-filtered by other visualizations on the same report page.</span></span>
* <span data-ttu-id="d49ad-127">สามารถไฮไลต์เชื่อมโยง และกรองข้าม ไปยังการแสดงภาพอื่น ๆ บนหน้ารายงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="d49ad-127">Can be used to highlight and cross-filter other visualizations on the same report page.</span></span>
   > [!NOTE]
   > <span data-ttu-id="d49ad-128">รับชมวิดีโอนี้เพื่อดู Will จัดทำแผนภูมิกรวยโดยใช้ตัวอย่างด้านการขายและการตลาด</span><span class="sxs-lookup"><span data-stu-id="d49ad-128">Watch this video to see Will create a funnel chart using the Sales and Marketing sample.</span></span> <span data-ttu-id="d49ad-129">จากนั้นทำตามขั้นตอนด้านล่างวิดีโอเพื่อทดลองด้วยตัวเองโดยใช้ไฟล์ตัวอย่าง Opportunity Analysis PBIX</span><span class="sxs-lookup"><span data-stu-id="d49ad-129">Then follow the steps below the video to try it out yourself using the Opportunity Analysis PBIX sample file</span></span>
   > 
   > 
## <a name="prerequisite"></a><span data-ttu-id="d49ad-130">เงื่อนไขเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="d49ad-130">Prerequisite</span></span>

<span data-ttu-id="d49ad-131">บทช่วยสอนนี้ใช้ไฟล์ PBIX [Opportunity Analysis .PBIX ตัวอย่าง](https://download.microsoft.com/download/9/1/5/915ABCFA-7125-4D85-A7BD-05645BD95BD8/Opportunity%20Analysis%20Sample%20PBIX.pbix
)</span><span class="sxs-lookup"><span data-stu-id="d49ad-131">This tutorial uses the [Opportunity Analysis sample PBIX file](https://download.microsoft.com/download/9/1/5/915ABCFA-7125-4D85-A7BD-05645BD95BD8/Opportunity%20Analysis%20Sample%20PBIX.pbix
).</span></span>

1. <span data-ttu-id="d49ad-132">จากด้านบนซ็ายของแถบเมนู เลือก **ไฟล์** > **เปิด**</span><span class="sxs-lookup"><span data-stu-id="d49ad-132">From the upper left section of the menubar, select **File** > **Open**</span></span>
   
2. <span data-ttu-id="d49ad-133">ค้นหาสำเนา **ไฟล์ PBIX ตัวอย่างการวิเคราะห์โอกาส**</span><span class="sxs-lookup"><span data-stu-id="d49ad-133">Find your copy of the **Opportunity Analysis sample PBIX file**</span></span>

1. <span data-ttu-id="d49ad-134">เปิด **ไฟล์ PBIX ตัวอย่างการวิเคราะห์โอกาส** ในมุมมองรายงาน ![ภาพหน้าจอไอคอนมุมมองรายงาน](media/power-bi-visualization-kpi/power-bi-report-view.png)</span><span class="sxs-lookup"><span data-stu-id="d49ad-134">Open the **Opportunity Analysis sample PBIX file** in report view ![Screenshot of the report view icon.](media/power-bi-visualization-kpi/power-bi-report-view.png).</span></span>

1. <span data-ttu-id="d49ad-135">เลือก</span><span class="sxs-lookup"><span data-stu-id="d49ad-135">Select</span></span> ![สกรีนช็อตของแท็บสีเหลือง](media/power-bi-visualization-kpi/power-bi-yellow-tab.png) <span data-ttu-id="d49ad-137">หากต้องการเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="d49ad-137">to add a new page.</span></span>


## <a name="create-a-basic-funnel-chart"></a><span data-ttu-id="d49ad-138">สร้างแผนภูมิกรวยพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="d49ad-138">Create a basic funnel chart</span></span>
<span data-ttu-id="d49ad-139">รับชมวิดีโอนี้เพื่อดู Will จัดทำแผนภูมิกรวยโดยใช้ตัวอย่างด้านการขายและการตลาด</span><span class="sxs-lookup"><span data-stu-id="d49ad-139">Watch this video to see Will create a funnel chart using the Sales and Marketing sample.</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/qKRZPBnaUXM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>


<span data-ttu-id="d49ad-140">ตอนนี้ ลองสร้างแผนภูมิของคุณเอง ที่แสดงจำนวนโอกาสที่เรามีในแต่ละของขั้นตอนการขายของเรา</span><span class="sxs-lookup"><span data-stu-id="d49ad-140">Now create your own funnel chart that shows the number of opportunities we have in each of our sales stages.</span></span>

1. <span data-ttu-id="d49ad-141">เริ่มต้นที่หน้ารายงานที่ว่างเปล่า แล้วเลือกเขตข้อมูล **SalesStage** \> **ขั้นตอนการขาย**</span><span class="sxs-lookup"><span data-stu-id="d49ad-141">Start on a blank report page and select the **SalesStage** \> **Sales Stage** field.</span></span>
   
    ![เลือกขั้นตอนการขาย](media/power-bi-visualization-funnel-charts/funnelselectfield-new.png)

1. <span data-ttu-id="d49ad-143">เลือกไอคอนกรวย</span><span class="sxs-lookup"><span data-stu-id="d49ad-143">Select the funnel icon</span></span> ![ไอคอนแผนภูมิกรวย](media/power-bi-visualization-funnel-charts/power-bi-funnel-icon.png) <span data-ttu-id="d49ad-145">การแปลงแผนภูมิคอลัมน์ให้เป็นแผนภูมิกรวย</span><span class="sxs-lookup"><span data-stu-id="d49ad-145">to convert the column chart to a funnel chart.</span></span>

2. <span data-ttu-id="d49ad-146">จากบานหน้าต่าง **เขตข้อมูล** เลือก **ข้อเท็จจริง** \> **จำนวนโอกาส**</span><span class="sxs-lookup"><span data-stu-id="d49ad-146">From the **Fields** pane, select **Fact** \> **Opportunity Count**.</span></span>
   
    ![สร้างแผนภูมิกรวย](media/power-bi-visualization-funnel-charts/power-bi-funnel-2.png)
4. <span data-ttu-id="d49ad-148">โฮเวอร์เหนือแท่ง จะแสดงข้อมูลจำนวนมากออกมา</span><span class="sxs-lookup"><span data-stu-id="d49ad-148">Hovering over a bar displays a wealth of information.</span></span>
   
   * <span data-ttu-id="d49ad-149">ชื่อของขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="d49ad-149">The name of the stage</span></span>
   * <span data-ttu-id="d49ad-150">จำนวนโอกาสทางการขายในขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="d49ad-150">Number of opportunities currently in this stage</span></span>
   * <span data-ttu-id="d49ad-151">อัตราการแปลงโดยรวม (% ของลูกค้าเป้าหมาย)</span><span class="sxs-lookup"><span data-stu-id="d49ad-151">Overall conversion rate (% of Lead)</span></span> 
   * <span data-ttu-id="d49ad-152">ขั้นตอน-ถึง-ขั้นตอน (หรืออัตราการดรอป) ซึ่งก็เป็น % ของขั้นตอนก่อนหน้า (ในกรณีนี้ ขั้นตอนข้อเสนอ/ขั้นตอนโซลูชัน)</span><span class="sxs-lookup"><span data-stu-id="d49ad-152">Stage-to-stage (also known as Drop Rate) which is the % of the previous stage (in this case, Proposal Stage/Solution Stage)</span></span>
     
     ![รายละเอียดสำหรับแถบข้อเสนอ](media/power-bi-visualization-funnel-charts/funnelhover-new.png)

6. <span data-ttu-id="d49ad-154">[บันทึกรายงาน](../create-reports/service-report-save.md)</span><span class="sxs-lookup"><span data-stu-id="d49ad-154">[Save the report](../create-reports/service-report-save.md).</span></span>

## <a name="highlighting-and-cross-filtering"></a><span data-ttu-id="d49ad-155">การทำไฮไลท์และการกรองข้าม</span><span class="sxs-lookup"><span data-stu-id="d49ad-155">Highlighting and cross-filtering</span></span>
<span data-ttu-id="d49ad-156">สำหรับข้อมูลเกี่ยวกับการใช้บานหน้าต่างตัวกรอง ดู[เพิ่มตัวกรองไปยังรายงาน](../create-reports/power-bi-report-add-filter.md)</span><span class="sxs-lookup"><span data-stu-id="d49ad-156">For information about using the Filters pane, see [Add a filter to a report](../create-reports/power-bi-report-add-filter.md).</span></span>

<span data-ttu-id="d49ad-157">ไฮไลต์แท่งในแผนภูมิกรวย จะกรองข้ามการแสดงภาพอื่น ๆ บนหน้ารายงาน... และในทางกลับกัน</span><span class="sxs-lookup"><span data-stu-id="d49ad-157">Highlighting a bar in a funnel cross-filters the other visualizations on the report page... and vice versa.</span></span> <span data-ttu-id="d49ad-158">เพื่อทำตาม เพิ่มวิชวลอีกสองสามวิชวล บนหน้ารายงานที่มีแผนภูมิกรวย</span><span class="sxs-lookup"><span data-stu-id="d49ad-158">To follow along, add a few more visuals to the report page that contains the funnel chart.</span></span>

1. <span data-ttu-id="d49ad-159">บนกรวย เลือกแท่ง **ข้อเสนอ**</span><span class="sxs-lookup"><span data-stu-id="d49ad-159">On the funnel, select the **Proposal** bar.</span></span> <span data-ttu-id="d49ad-160">ซึ่งจะไฮไลต์เชื่อมโยงไปยังการแสดงภาพอื่น ๆ บนหน้า</span><span class="sxs-lookup"><span data-stu-id="d49ad-160">This cross-highlights the other visualizations on the page.</span></span> <span data-ttu-id="d49ad-161">ใช้ CTRL เพื่อเลือกหลายค่า</span><span class="sxs-lookup"><span data-stu-id="d49ad-161">Use CTRL to multi-select.</span></span>
   
   ![โต้ตอบกับภาพแสดงวิดีโอสั้น ๆ](media/power-bi-visualization-funnel-charts/funnelchartnoowl.gif)
2. <span data-ttu-id="d49ad-163">เพื่อกำหนดลักษณะ การไฮไลต์เชื่อมโยง และการกรองข้าม ระหว่างวิชวล ดู[การโต้ตอบระหว่างวิชวลใน Power BI](../create-reports/service-reports-visual-interactions.md)</span><span class="sxs-lookup"><span data-stu-id="d49ad-163">To set preferences for how visuals cross-highlight and cross-filter each other, see [Visual interactions in Power BI](../create-reports/service-reports-visual-interactions.md)</span></span>

## <a name="next-steps"></a><span data-ttu-id="d49ad-164">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d49ad-164">Next steps</span></span>

[<span data-ttu-id="d49ad-165">ตัววัดใน Power BI</span><span class="sxs-lookup"><span data-stu-id="d49ad-165">Gauges in Power BI</span></span>](power-bi-visualization-radial-gauge-charts.md)

[<span data-ttu-id="d49ad-166">ชนิดการแสดงภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="d49ad-166">Visualization types in Power BI</span></span>](power-bi-visualization-types-for-reports-and-q-and-a.md)



