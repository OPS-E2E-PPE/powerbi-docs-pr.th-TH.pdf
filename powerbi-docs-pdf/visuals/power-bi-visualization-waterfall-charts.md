---
title: แผนภูมิแบบน้ำตกใน Power BI
description: แผนภูมิแบบน้ำตกใน Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
featuredvideoid: removed
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 12/5/2019
LocalizationGroup: Visualizations
ms.openlocfilehash: 6c358c2e12ee3526445efeab1e45b5f193f8b654
ms.sourcegitcommit: 8250187368d3de48663eb516a816ff701119b579
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/10/2020
ms.locfileid: "96997943"
---
# <a name="waterfall-charts-in-power-bi"></a><span data-ttu-id="64094-103">แผนภูมิแบบน้ำตกใน Power BI</span><span class="sxs-lookup"><span data-stu-id="64094-103">Waterfall charts in Power BI</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="64094-104">แผนภูมิแบบน้ำตกจะแสดงผลรวมสะสมเป็นค่าของ Power BI ที่เพิ่มขึ้นหรือลดลง</span><span class="sxs-lookup"><span data-stu-id="64094-104">Waterfall charts show a running total as Power BI adds and subtracts values.</span></span> <span data-ttu-id="64094-105">แผนภูมิเหล่านี้มีประโยชน์สำหรับการวิเคราะห์ว่าค่าเริ่มต้น (ตัวอย่างเช่น กำไรสุทธิ) ได้รับผลกระทบอย่างไร เมื่อมีการเปลี่ยนแปลงเชิงบวก และเชิงลบที่เกิดขึ้นอย่างต่อเนื่องในช่วงระยะเวลาหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="64094-105">They're useful for understanding how an initial value (like net income) is affected by a series of positive and negative changes.</span></span>

<span data-ttu-id="64094-106">คอลัมน์เป็นสีที่แสดงรหัส เพื่อให้คุณสามารถสังเกตการเพิ่มขึ้นและการลดลงได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="64094-106">The columns are color coded so you can quickly notice increases and decreases.</span></span> <span data-ttu-id="64094-107">คอลัมน์ค่าเริ่มต้นและคอลัมน์ค่าสุดท้ายมัก[เริ่มต้นบนแกนนอน](https://support.office.com/article/Create-a-waterfall-chart-in-Office-2016-for-Windows-8de1ece4-ff21-4d37-acd7-546f5527f185#BKMK_Float "เริ่มต้นบนแกนนอน")ขณะที่ค่ากลางจะเป็นคอลัมน์แบบลอยตัว</span><span class="sxs-lookup"><span data-stu-id="64094-107">The initial and the final value columns often [start on the horizontal axis](https://support.office.com/article/Create-a-waterfall-chart-in-Office-2016-for-Windows-8de1ece4-ff21-4d37-acd7-546f5527f185#BKMK_Float "start on the horizontal axis"), while the intermediate values are floating columns.</span></span> <span data-ttu-id="64094-108">เนื่องจากมี "สไตล์" แบบนี้ จึงยังเรียกแผนภูมิแบบน้ำตกอีกชื่อหนึ่งว่าแผนภูมิแบบสะพาน</span><span class="sxs-lookup"><span data-stu-id="64094-108">Because of this style, waterfall charts are also called bridge charts.</span></span>

## <a name="when-to-use-a-waterfall-chart"></a><span data-ttu-id="64094-109">เมื่อต้องการใช้แผนภูมิแบบน้ำตก</span><span class="sxs-lookup"><span data-stu-id="64094-109">When to use a waterfall chart</span></span>

<span data-ttu-id="64094-110">แผนภูมิแบบน้ำตกเป็นตัวเลือกที่เหมาะสมอย่างยิ่ง ในกรณีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="64094-110">Waterfall charts are a great choice:</span></span>

* <span data-ttu-id="64094-111">เมื่อคุณมีการเปลี่ยนแปลงข้อมูลตัวเลขตลอดช่วงระยะเวลาหนึ่งหรือตามประเภทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="64094-111">When you have changes for the measure across time, a series, or different categories.</span></span>

* <span data-ttu-id="64094-112">เมื่อต้องการตรวจสอบการเปลี่ยนแปลงหลักที่ส่งผลให้เกิดค่าผลรวม</span><span class="sxs-lookup"><span data-stu-id="64094-112">To audit the major changes contributing to the total value.</span></span>

* <span data-ttu-id="64094-113">เมื่อต้องการลงจุดกำไรรายปีของบริษัทคุณ โดยแสดงแหล่งข้อมูลต่างๆ ของรายได้ และจนถึงกำไร (หรือขาดทุน) รวม</span><span class="sxs-lookup"><span data-stu-id="64094-113">To plot your company's annual profit by showing various sources of revenue and arrive at the total profit (or loss).</span></span>

* <span data-ttu-id="64094-114">เมื่อต้องการแสดงจำนวนพนักงานตอนต้นปีและปลายปีในบริษัทของคุณในหนึ่งปี</span><span class="sxs-lookup"><span data-stu-id="64094-114">To illustrate the beginning and the ending headcount for your company in a year.</span></span>

* <span data-ttu-id="64094-115">เมื่อต้องการแสดงภาพจำนวนเงินที่หาได้และใช้จ่ายในแต่ละเดือน และยอดคงเหลือสะสมสำหรับบัญชีของคุณ</span><span class="sxs-lookup"><span data-stu-id="64094-115">To visualize how much money you make and spend each month, and the running balance for your account.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="64094-116">เงื่อนไขเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="64094-116">Prerequisite</span></span>

<span data-ttu-id="64094-117">บทช่วยสอนนี้ใช้[ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix)</span><span class="sxs-lookup"><span data-stu-id="64094-117">This tutorial uses the [Retail Analysis sample PBIX file](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix).</span></span>

1. <span data-ttu-id="64094-118">จากด้านบนซ้ายของแถบเมนู เลือก **ไฟล์** > **เปิด**</span><span class="sxs-lookup"><span data-stu-id="64094-118">From the upper left section of the menubar, select **File** > **Open**</span></span>
   
2. <span data-ttu-id="64094-119">ค้นหาสำเนา **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก**</span><span class="sxs-lookup"><span data-stu-id="64094-119">Find your copy of the **Retail Analysis sample PBIX file**</span></span>

1. <span data-ttu-id="64094-120">เปิด **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก** ในมุมมองรายงาน ![ภาพหน้าจอไอคอนมุมมองรายงาน](media/power-bi-visualization-kpi/power-bi-report-view.png)</span><span class="sxs-lookup"><span data-stu-id="64094-120">Open the **Retail Analysis sample PBIX file** in report view ![Screenshot of the report view icon.](media/power-bi-visualization-kpi/power-bi-report-view.png).</span></span>

1. <span data-ttu-id="64094-121">เลือก</span><span class="sxs-lookup"><span data-stu-id="64094-121">Select</span></span> ![สกรีนช็อตของแท็บสีเหลือง](media/power-bi-visualization-kpi/power-bi-yellow-tab.png) <span data-ttu-id="64094-123">หากต้องการเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="64094-123">to add a new page.</span></span>

> [!NOTE]
> <span data-ttu-id="64094-124">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="64094-124">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span>    

## <a name="create-a-waterfall-chart"></a><span data-ttu-id="64094-125">สร้างแผนภูมิแบบน้ำตก</span><span class="sxs-lookup"><span data-stu-id="64094-125">Create a waterfall chart</span></span>

<span data-ttu-id="64094-126">คุณจะสร้างแผนภูมิแบบน้ำตกที่แสดงผลต่างของยอดขาย (ประมาณการยอดขายเทียบกับยอดขายจริง) เป็นรายเดือน</span><span class="sxs-lookup"><span data-stu-id="64094-126">You'll create a waterfall chart that displays sales variance (estimated sales versus actual sales) by month.</span></span>

### <a name="build-the-waterfall-chart"></a><span data-ttu-id="64094-127">สร้างแผนภูมิน้ำตก</span><span class="sxs-lookup"><span data-stu-id="64094-127">Build the waterfall chart</span></span>

1. <span data-ttu-id="64094-128">ในส่วนบานหน้าต่าง **เขตข้อมูล** ให้เลือก **ยอดขาย** >  **ผลต่างของยอดขายรวม**</span><span class="sxs-lookup"><span data-stu-id="64094-128">From the **Fields** pane, select **Sales** > **Total Sales Variance**.</span></span>

   ![สกรีนช็อตของยอดขาย >ผลต่างของยอดขายรวมที่เลือกและภาพที่เป็นผลลัพธ์](media/power-bi-visualization-waterfall-charts/power-bi-bar.png)

1. <span data-ttu-id="64094-130">เลือกไอคอนน้ำตก</span><span class="sxs-lookup"><span data-stu-id="64094-130">Select the waterfall icon</span></span> ![สกรีนช็อตของไอคอนน้ำตก](media/power-bi-visualization-waterfall-charts/power-bi-waterfall-icon.png)

    ![แม่แบบการแสดงภาพ](media/power-bi-visualization-waterfall-charts/convert-waterfall.png)

1. <span data-ttu-id="64094-133">เลือก **เวลา** > **เดือนตามรอบบัญชี** เพื่อเพิ่มไปยังแอ่ง **ประเภท**</span><span class="sxs-lookup"><span data-stu-id="64094-133">Select **Time** > **FiscalMonth** to add it to the **Category** well.</span></span>

    ![แผนภูมิน้ำตก](media/power-bi-visualization-waterfall-charts/power-bi-waterfall-month.png)

### <a name="sort-the-waterfall-chart"></a><span data-ttu-id="64094-135">เรียงลำดับแผนภูมิน้ำตก</span><span class="sxs-lookup"><span data-stu-id="64094-135">Sort the waterfall chart</span></span>

1. <span data-ttu-id="64094-136">ตรวจสอบให้แน่ใจว่า Power BI เรียงลำดับแผนภูมิแบบน้ำตกตามลำดับเดือน</span><span class="sxs-lookup"><span data-stu-id="64094-136">Make sure Power BI sorts the waterfall chart chronologically by month.</span></span> <span data-ttu-id="64094-137">จากมุมบนขวาของแผนภูมิ ให้เลือก **ตัวเลือกเพิ่มเติม** (...)</span><span class="sxs-lookup"><span data-stu-id="64094-137">From the top-right corner of the chart, select **More options** (...).</span></span>

    <span data-ttu-id="64094-138">สำหรับตัวอย่างนี้ ให้เลือก **เรียงลำดับตาม** และเลือก **FiscalMonth (เดือนงบประมาณ)**</span><span class="sxs-lookup"><span data-stu-id="64094-138">For this example, select **Sort by** and choose **FiscalMonth**.</span></span> <span data-ttu-id="64094-139">ตัวบ่งชี้สีเหลืองที่อยู่ถัดจากสิ่งที่คุณเลือกจะแสดงขึ้นเมื่อมีการใช้ตัวเลือกการเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="64094-139">A yellow indicator next to your selection indicates when your selection option is being applied.</span></span>

    ![เลือกการเรียงลำดับตาม > เดือนงบประมาณ](media/power-bi-visualization-waterfall-charts/power-bi-sort-by-fiscalmonth.png)
    
    <span data-ttu-id="64094-141">เพื่อแสดงเดือนตามลำดับเวลา ให้เลือก **เรียงลำดับจากน้อยไปหามาก**</span><span class="sxs-lookup"><span data-stu-id="64094-141">To display the months in chronological order, select **Sort ascending**.</span></span> <span data-ttu-id="64094-142">เช่นเดียวกับขั้นตอนก่อนหน้า ให้ตรวจสอบว่ามีตัวบ่งชี้สีเหลืองอยู่ถัดจากด้านซ้ายของตัวเลือก **การเรียงลำดับจากน้อยไปมาก** หรือไม่</span><span class="sxs-lookup"><span data-stu-id="64094-142">As with the previous step, check that there is a yellow indicator next to the left of **Sort ascending.**</span></span> <span data-ttu-id="64094-143">ซึ่งเป็นการระบุว่าตัวเลือกที่คุณเลือกกำลังถูกปรับใช้</span><span class="sxs-lookup"><span data-stu-id="64094-143">This indicates that your selected option is being applied.</span></span>

    ![เลือกเรียงจาก > ลำดับจากน้อยไปมาก](media/power-bi-visualization-waterfall-charts/power-bi-waterfall-ascending.png)

    

    <span data-ttu-id="64094-145">โปรดสังเกตว่าแผนภูมิของคุณถูกจัดเรียงตั้งแต่เดือนมกราคมถึงเดือนสิงหาคมสำหรับ FiscalMonth (เดือนงบประมาณ)</span><span class="sxs-lookup"><span data-stu-id="64094-145">Notice that your chart is sorted from January to August for FiscalMonth.</span></span>  

### <a name="explore-the-waterfall-chart"></a><span data-ttu-id="64094-146">สำรวจแผนภูมิน้ำตก</span><span class="sxs-lookup"><span data-stu-id="64094-146">Explore the waterfall chart</span></span>

<span data-ttu-id="64094-147">ดูรายละเอียดเพิ่มเติมอีกเล็กน้อย เพื่อดูว่าอะไรคือปัจจัยที่สนับสนุนให้เกิดการเปลี่ยนแปลงมากที่สุดในแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="64094-147">Dig in a little more to see what's contributing most to the changes month to month.</span></span>

1.  <span data-ttu-id="64094-148">เลือก **ร้านค้า** > **พื้นที่** ซึ่งจะเป็นการเพิ่ม **พื้นที่** ไปยังบักเก็ต **แยกย่อย**</span><span class="sxs-lookup"><span data-stu-id="64094-148">Select **Store** > **Territory**, which will add **Territory** to the **Breakdown** bucket.</span></span>

    ![สกรีนช็อตแสดงการเพิ่มเขตแดนลงในพื้นที่การแบ่งย่อย](media/power-bi-visualization-waterfall-charts/power-bi-waterfall-breakdown.png)

    <span data-ttu-id="64094-150">Power BI ใช้ค่าใน **แยกย่อย** เพื่อเพิ่มข้อมูลเพิ่มเติมไปยังการแสดงผลข้อมูลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="64094-150">Power BI uses the value in **Breakdown** to add additional data to the visualization.</span></span> <span data-ttu-id="64094-151">ซึ่งจะเพิ่มปัจจัยสนับสนุนห้าอันดับแรกที่จะเพิ่ม หรือลดสำหรับแต่ละเดือนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="64094-151">It adds the top five contributors to increases or decreases for each fiscal month.</span></span> <span data-ttu-id="64094-152">ตัวอย่างเช่นในเดือนกุมภาพันธ์ มีจุดข้อมูลหกจุดแทนที่จะเป็นเพียงจุดเดียว</span><span class="sxs-lookup"><span data-stu-id="64094-152">This means that February, for example, now has six data points instead of just one.</span></span>  

    ![แสดงร้านค้าในบักเก็ต](media/power-bi-visualization-waterfall-charts/power-bi-waterfall-breakdown-default.png)

    <span data-ttu-id="64094-154">สมมติว่าคุณสนใจเฉพาะปัจจัยสนับสนุน 2 อันดับแรก</span><span class="sxs-lookup"><span data-stu-id="64094-154">Let's say that you're only interested in the top two contributors.</span></span>

1. <span data-ttu-id="64094-155">ในบานหน้าต่าง **การจัดรูปแบบ** ให้เลือก **การแบ่งย่อย** แล้วตั้ง **การแบ่งย่อยสูงสุดเป็น** **2**</span><span class="sxs-lookup"><span data-stu-id="64094-155">In the **Format** pane, select **Breakdown** and set **Max breakdowns** to **2**.</span></span>

    ![รูปแบบ > แบ่งย่อย](media/power-bi-visualization-waterfall-charts/power-bi-waterfall-breakdown-two.png)

    <span data-ttu-id="64094-157">การตรวจสอบอย่างรวดเร็วแสดงให้เห็นว่าเขตโอไฮโอ และเพนซิลเวเนียเป็นปัจจัยสนับสนุนที่มีอิทธิพลมากที่สุดที่ทำให้เกิดการเปลี่ยนแปลงทั้งในเชิงบวกและเชิงลบในแผนภูมิแบบน้ำตกของเรา</span><span class="sxs-lookup"><span data-stu-id="64094-157">A quick review reveals that the territories of Ohio and Pennsylvania are the biggest contributors to movement, both negative and positive, in your waterfall chart.</span></span>

    ![แผนภูมิน้ำตก](media/power-bi-visualization-waterfall-charts/power-bi-axis-waterfall.png)

## <a name="next-steps"></a><span data-ttu-id="64094-159">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="64094-159">Next steps</span></span>

* [<span data-ttu-id="64094-160">เปลี่ยนวิธีการที่การแสดงผลด้วยภาพโต้ตอบในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="64094-160">Change how visuals interact in a Power BI report</span></span>](../create-reports/service-reports-visual-interactions.md)

* [<span data-ttu-id="64094-161">ชนิดการแสดงภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="64094-161">Visualization types in Power BI</span></span>](power-bi-visualization-types-for-reports-and-q-and-a.md)

