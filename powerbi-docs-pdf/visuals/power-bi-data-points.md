---
title: ชุดข้อมูลขนาดใหญ่ ข้อจำกัดของจุดข้อมูล และข้อมูลกลยุทธ์
description: ขีดจำกัดของข้อมูลสำหรับวิชวลและข้อมูลกลยุทธ์ที่ลดลง
author: mihart
ms.author: mihart
ms.reviewer: justyna
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 01/10/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 0feef179fddba93f192559c7ac7bed10c6fa5328
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412540"
---
# <a name="apply-data-point-limits-and-strategies-by-visual-type"></a><span data-ttu-id="527e4-103">ปรับใช้ข้อจำกัดของจุดข้อมูลและกลยุทธ์ตามรูปแบบการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="527e4-103">Apply data-point limits and strategies by visual type</span></span>

[!INCLUDE[consumer-appliesto-yyyn](../includes/consumer-appliesto-yyyn.md)]    

<span data-ttu-id="527e4-104">การแสดงภาพต้องทำได้อย่างรวดเร็ว และแม่นยำเมื่อแสดงภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="527e4-104">When rendering a visual in Power BI, the visualization must be quick and accurate.</span></span> <span data-ttu-id="527e4-105">ที่จำเป็นต้องใช้การตั้งค่าอัลกอริทึมในการกำหนดค่าสำหรับของภาพแต่ละชนิด</span><span class="sxs-lookup"><span data-stu-id="527e4-105">That requires underlying algorithms configured for each visual type.</span></span> <span data-ttu-id="527e4-106">วิชวลใน Power BI ต้องยืดหยุ่นมากพอที่จะจัดการขนาดของชุดข้อมูลที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="527e4-106">Visuals in Power BI must be flexible enough to handle different sizes of datasets.</span></span> <span data-ttu-id="527e4-107">ชุดข้อมูลบางอย่างมีจุดข้อมูลเพียงเล็กน้อย ในขณะที่บางชุดข้อมูลอื่น ๆ มีจุดข้อมูลเป็นระดับเพตะไบต์</span><span class="sxs-lookup"><span data-stu-id="527e4-107">Some datasets have only a handful of data points, while other datasets have petabytes of data points.</span></span> <span data-ttu-id="527e4-108">บทความนี้อธิบายกลยุทธ์ที่ Power BI ใช้ในการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="527e4-108">This article explains the strategies used by Power BI to render visualizations.</span></span>

## <a name="data-reduction-strategies"></a><span data-ttu-id="527e4-109">กลยุทธ์การลดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="527e4-109">Data reduction strategies</span></span>
<span data-ttu-id="527e4-110">ในทุก ๆ ภาพอย่างน้อยจะมี *กลยุทธ์การลดข้อมูล* หนึ่งแบบหรือมากกว่านั้นเพื่อจัดการความเป็นไปได้ที่อาจจะมีข้อมูลขนาดใหญ่ที่กำลังถูกวิเคราะห์ข้อมูลอยู่</span><span class="sxs-lookup"><span data-stu-id="527e4-110">Every visual employs one or more *data reduction strategies* in order to handle the potentially large volumes of data being analyzed.</span></span> <span data-ttu-id="527e4-111">แม้แต่ตารางง่าย ๆ ก็ใช้กลยุทธ์นี้เพื่อหลีกเลี่ยงการโหลดชุดข้อมูลทั้งหมดไปยังไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="527e4-111">Even a simple table employs a strategy to avoid loading the entire dataset to the client.</span></span>  <span data-ttu-id="527e4-112">กลยุทธ์การลดข้อมูลถูกใช้แตกต่างกันตามชนิดของภาพ</span><span class="sxs-lookup"><span data-stu-id="527e4-112">The reduction strategy being used varies by visual type.</span></span> <span data-ttu-id="527e4-113">การเลือกแต่ละภาพนั้นมาจาก *กลยุทธ์การลดข้อมูล* ซึ่งเป็นส่วนหนึ่งของการสร้างคำขอข้อมูลส่งไปยังเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="527e4-113">Each visual selects from the supported *data reduction strategies* as part of generating the data request sent to the server.</span></span> 

<span data-ttu-id="527e4-114">แต่ละภาพจะควบคุมพารามิเตอร์ของแต่ละกลยุทธ์เพื่อให้เกิดมีผลข้อมูลจำนวนโดยรวมเท่า ๆ กัน</span><span class="sxs-lookup"><span data-stu-id="527e4-114">Each visual controls the parameters on those strategies to influence the overall amount of data.</span></span>   

## <a name="strategies"></a><span data-ttu-id="527e4-115">กลยุทธ์</span><span class="sxs-lookup"><span data-stu-id="527e4-115">Strategies</span></span>
<span data-ttu-id="527e4-116">สำหรับในแต่ละกลยุทธ์ มีค่าเริ่มต้นที่ยึดตามรูปร่างและชนิดของข้อมูลที่ถูกแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="527e4-116">For each strategy, there are defaults based on the shape and type of data being visualized.</span></span> <span data-ttu-id="527e4-117">แต่ค่าเริ่มต้นสามารถถูกบันทึกแทนที่บน Power BI ได้เพื่อการใช้งานที่เหมาะสมตามรูปแบบการทำงานของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="527e4-117">But the defaults can be overridden, in the Power BI Formatting pane, to provide the right user experience.</span></span> 

* <span data-ttu-id="527e4-118">**ข้อมูล Windowing** (การแบ่งเซกเมนต์): อนุญาตให้ผู้ใช้เลื่อนดูข้อมูลในวิชวล โดยราการโหลดส่วนย่อยของชุดข้อมูลโดยรวม</span><span class="sxs-lookup"><span data-stu-id="527e4-118">**Data Windowing** (Segmentation): Allow users to scroll through the data in a visual by progressively loading fragments of the overall dataset.</span></span>
* <span data-ttu-id="527e4-119">**TopN**: แสดงเฉพาะรายการที่ N แรก</span><span class="sxs-lookup"><span data-stu-id="527e4-119">**TopN**: Show only the first N items</span></span>
* <span data-ttu-id="527e4-120">**ตัวอย่างง่าย ๆ**: แสดงรายการล่าสุด รายการแรก และ N โดยกระจายรายการระหว่างกัน</span><span class="sxs-lookup"><span data-stu-id="527e4-120">**Simple Sample**: Show the first, last, and N evenly distributed items in between.</span></span>
* <span data-ttu-id="527e4-121">**BottomN**: แสดงเฉพาะรายการ N ล่าสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-121">**BottomN**: Show only the last N items.</span></span>  <span data-ttu-id="527e4-122">มีประโยชน์สำหรับการตรวจสอบการอัปเดตข้อมูลอยู่บ่อยครั้ง</span><span class="sxs-lookup"><span data-stu-id="527e4-122">Useful for monitoring frequently updated data.</span></span>
* <span data-ttu-id="527e4-123">**การสุ่มตัวอย่างความหนาแน่นสูง**-การปรับปรุงอัลกอริทึมการสุ่มตัวอย่างให้ดียิ่งขึ้นโดยให้อัลกอริทึมสนใจค่าผิดปกติและ/หรือรูปร่างของเส้นโค้ง</span><span class="sxs-lookup"><span data-stu-id="527e4-123">**High-density sampling** - An improved sampling algorithm that better respects outliers and/or the shape of a curve.</span></span>
    * <span data-ttu-id="527e4-124">**ช่องการสุ่มตัวอย่างเส้น**-จุดข้อมูลตัวอย่างตามที่ผิดปกติในช่องเก็บในแกน</span><span class="sxs-lookup"><span data-stu-id="527e4-124">**Binned line sampling** - Sample data points based on outliers in bins across an axis</span></span>
    * <span data-ttu-id="527e4-125">**ตัวอย่างการซ้อนทับกันของจุด**-ตัวอย่างจุดข้อมูลที่อ้างอิงตามค่าที่ทับซ้อนของค่าผิดปกติ</span><span class="sxs-lookup"><span data-stu-id="527e4-125">**Overlapping points sampling** - Sample data points based on overlapping values to preserve outliers</span></span>

## <a name="statistics"></a><span data-ttu-id="527e4-126">สถิติ</span><span class="sxs-lookup"><span data-stu-id="527e4-126">Statistics</span></span>
<span data-ttu-id="527e4-127">บางแบบจำลองสามารถให้ข้อมูลสถิติเกี่ยวกับจำนวนของค่าสำหรับบางคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="527e4-127">Certain models can provide statistics about the number of values for certain columns.</span></span> <span data-ttu-id="527e4-128">เมื่อทราบข้อมูลดังกล่าว เราสามารถใช้ประโยชน์จากข้อมูลนั้นเพื่อทำให้เกิดสมดุลไปทั่วทั้งลำดับชั้น หากวิชวลคำนวณค่าเข้ามาแทนที่ตามกลยุทธ์ที่มันถูกวางเอาไว้</span><span class="sxs-lookup"><span data-stu-id="527e4-128">When such information is present, we leverage that information to provide better balancing across multiple hierarchies, if a visual does not explicitly override the count of values for a strategy.</span></span>

<span data-ttu-id="527e4-129">สำหรับข้อมูลเพิ่มเติม ให้ดูที่[มีอะไรใหม่ในบริการการวิเคราะห์](/sql/analysis-services/what-s-new-in-analysis-services)</span><span class="sxs-lookup"><span data-stu-id="527e4-129">For more information, see [What's new in Analysis Services](/sql/analysis-services/what-s-new-in-analysis-services)</span></span>

## <a name="dynamic-limits"></a><span data-ttu-id="527e4-130">ขีดจำกัดแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="527e4-130">Dynamic limits</span></span>
<span data-ttu-id="527e4-131">นอกเหนือจากกลยุทธ์ด้านบน ภาพ ที่มีลำดับชั้นที่สองของการจัดกลุ่มคอลัมน์ (แกน และคำอธิบายแผน ภูมิ หรือประเภท และชุดข้อมูล) ใช้กลยุทธ์เพิ่มเติมที่ชื่อว่า *ขีดจำกัดแบบไดนามิก*</span><span class="sxs-lookup"><span data-stu-id="527e4-131">In addition to the strategies above, visuals with two hierarchies of grouping columns (axis and legend, or category and series) use one additional strategy called *dynamic limits*.</span></span>  <span data-ttu-id="527e4-132">ขีดจำกัดแบบไดนามิกถูกออกแบบมาเพื่อให้การสมดุลของจุดข้อมูลออกมาดียิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="527e4-132">Dynamic limits are designed to better balance data points.</span></span> 

<span data-ttu-id="527e4-133">ขีดจำกัดแบบไดนามิกให้ตัวเลือกของจุดข้อมูลแบบกระจายได้ดีกว่าการจำกัดเชิงสถิติทำ</span><span class="sxs-lookup"><span data-stu-id="527e4-133">Dynamic limits provide a better selection of points for sparse data than static limits would.</span></span> <span data-ttu-id="527e4-134">ตัวอย่าง วิชวลอาจถูกกำหนดค่าให้เลือกประเภท 100 และ มีผลรวมของจุด 1000 10 ชุด</span><span class="sxs-lookup"><span data-stu-id="527e4-134">For example, a visual could be configured to select 100 categories and 10 series with a total of 1000 points.</span></span> <span data-ttu-id="527e4-135">แต่ข้อมูลจริง ๆ แล้วมี 50 ประเภทและชุดข้อมูล 20 ชุด</span><span class="sxs-lookup"><span data-stu-id="527e4-135">But the actual data has 50 categories and 20 series.</span></span>  <span data-ttu-id="527e4-136">ในขณะที่คิวรีกำลังดำเนินไป ขีดจำกัดแบบไดนามิกจะเลือกมาทั้งหมด 20 ชุดเพื่อให้เพียงพอต่อความต้องการเติมค่า 1000 แต้ม</span><span class="sxs-lookup"><span data-stu-id="527e4-136">At query runtime, dynamic limits selects all 20 series to fill up the 1000 points requested.</span></span>

<span data-ttu-id="527e4-137">ขีดจำกัดแบบไดนามิกจะนำไปใช้โดยอัตโนมัติเมื่อเซิร์ฟเวอร์สามารถดำเนินไปถึงเงื่อนไขตามรายละเอียดด้านล่างนี้:</span><span class="sxs-lookup"><span data-stu-id="527e4-137">Dynamic limits are automatically applied when the server is capable as detailed below:</span></span>

* <span data-ttu-id="527e4-138">เมื่อเวอร์ชันของ Power BI Desktop กับ SSAS ภายในองค์กรเป็นของปี 2016 หรือใหม่กว่า[สามารถใช้ประโยชน์จากความสามารถ SuperDax ของเซิร์ฟเวอร์](/archive/blogs/analysisservices/whats-new-in-microsoft-sql-server-analysis-services-tabular-models-in-sql-server-2016-ctp-2-3)</span><span class="sxs-lookup"><span data-stu-id="527e4-138">In Power BI Desktop with On-premises SSAS version 2016 or higher [leveraging the SuperDax capabilities of the server](/archive/blogs/analysisservices/whats-new-in-microsoft-sql-server-analysis-services-tabular-models-in-sql-server-2016-ctp-2-3)</span></span>

* <span data-ttu-id="527e4-139">ใน Desktop และบริการ Power BI เมื่อใช้ตัวนำเข้าแบบ Direct Query ซึ่งเชื่อมต่อสดไปยังบริการ หรือเชื่อมต่อแบบสดเพื่อ AS PaaS</span><span class="sxs-lookup"><span data-stu-id="527e4-139">In Desktop and Power BI service when using an imported model, Direct Query, live connect to the service, or live connect to AS PaaS.</span></span> 

* <span data-ttu-id="527e4-140">ในบริการ Power BI เมื่อเชื่อมต่อผ่านเกตเวย์ที่มีเพื่อไปยัง SSAS ภายในองค์กร เราไม่สามารถใช้ขีดจำกัดแบบไดนามิกได้</span><span class="sxs-lookup"><span data-stu-id="527e4-140">In Power BI Service, when connecting through an on-premises gateway to on-premises SSAS, we cannot use dynamic limits.</span></span> <span data-ttu-id="527e4-141">เกตเวย์ภายในองค์กรไม่รองรับกลยุทธ์ขีดจำกัดแบบไดนามิกที่ส่งกลับโครงสร้างต่าง ๆ ของชุดผลลัพธ์จาก SSAS ภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="527e4-141">The on-premises gateway does not fully support the dynamic limits strategy that returns a different structure of result sets from the on-premises SSAS.</span></span>  

## <a name="strategies-and-data-point-limits-by-visual-type"></a><span data-ttu-id="527e4-142">กลยุทธ์และจุดข้อมูลจำกัดตามรูปแบบการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="527e4-142">Strategies and data point limits by visual type</span></span>

### <a name="area-chart"></a><span data-ttu-id="527e4-143">แผนภูมิพื้นที่</span><span class="sxs-lookup"><span data-stu-id="527e4-143">Area chart</span></span>
<span data-ttu-id="527e4-144">ดู[วิธีการทำงานของเส้นอย่างง่าย ๆ](../create-reports/desktop-high-density-sampling.md#how-the-new-line-sampling-algorithm-works)</span><span class="sxs-lookup"><span data-stu-id="527e4-144">See [How line sampling works](../create-reports/desktop-high-density-sampling.md#how-the-new-line-sampling-algorithm-works)</span></span>

### <a name="barcolumn-chart"></a><span data-ttu-id="527e4-145">แผนภูมิแท่ง/คอลัมน์</span><span class="sxs-lookup"><span data-stu-id="527e4-145">Bar/column chart</span></span>
- <span data-ttu-id="527e4-146">เมื่ออยู่ในโหมดแบบกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="527e4-146">When in categorical mode</span></span>
    - <span data-ttu-id="527e4-147">หมวดหมู่: การจำลองภาพเสมือน โดยใช้หน้าต่าง 500 แถวในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="527e4-147">Categories: Virtualization by using Window of 500 rows at a time</span></span>
    - <span data-ttu-id="527e4-148">ชุดข้อมูล: 60 อันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-148">Series: Top 60</span></span>
    - <span data-ttu-id="527e4-149">เมื่ออยู่ในโหมดสเกลา (สามารถใช้ขีดจำกัดแบบไดนามิกได้)</span><span class="sxs-lookup"><span data-stu-id="527e4-149">When in scalar mode (could use dynamic limits)</span></span>
        - <span data-ttu-id="527e4-150">แต้มสูงสุด: 10,000</span><span class="sxs-lookup"><span data-stu-id="527e4-150">Max points: 10,000</span></span>
        - <span data-ttu-id="527e4-151">หมวดหมู่: ตัวอย่างของค่า 500 หน่วย</span><span class="sxs-lookup"><span data-stu-id="527e4-151">Categories: Sample of 500 values</span></span>
        - <span data-ttu-id="527e4-152">ชุดข้อมูล: 20 อันดับค่าตัวเลขสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-152">Series: Top 20 values</span></span>

### <a name="card-multirow"></a><span data-ttu-id="527e4-153">การ์ด (หลายแถว)</span><span class="sxs-lookup"><span data-stu-id="527e4-153">Card (multirow)</span></span> 
- <span data-ttu-id="527e4-154">ค่า: การจำลองภาพเสมือน โดยใช้หน้าต่าง 200 แถวในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="527e4-154">Values: Virtualization by using Window of 200 rows at a time</span></span>

### <a name="combo-chart"></a><span data-ttu-id="527e4-155">แผนภูมิผสม</span><span class="sxs-lookup"><span data-stu-id="527e4-155">Combo chart</span></span>
 <span data-ttu-id="527e4-156">ใช้กลยุทธ์เดียวกันเป็นแผนภูมิคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="527e4-156">Uses the same strategies as column chart.</span></span> <span data-ttu-id="527e4-157">โปรดสังเกตว่า เส้นใน **แผนภูมิผสม** ไม่ใช้อัลกอริทึมที่มีความหนาแน่นสูงอย่างที่ **แผนภูมิเส้น** ใช้</span><span class="sxs-lookup"><span data-stu-id="527e4-157">Notice that the line in the **combo chart** does not use the high-density algorithm that the **line chart** uses.</span></span>

### <a name="power-bi-visuals"></a><span data-ttu-id="527e4-158">วิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="527e4-158">Power BI visuals</span></span>
<span data-ttu-id="527e4-159">สามารถเพิ่มขึ้นได้ถึง 30,000 แต่จะขึ้นอยู่กับผู้สร้างวิชวลว่าต้องการให้ใช้กลยุทธ์ใด</span><span class="sxs-lookup"><span data-stu-id="527e4-159">Can get up to 30,000 but it is up to the visual authors to indicate what strategies to use.</span></span> <span data-ttu-id="527e4-160">ขีดจำกัดเริ่มต้นคือ 1,000 แต่ผู้สร้างวิชวลสามารถเปลี่ยนได้ สูงสุด 30,000</span><span class="sxs-lookup"><span data-stu-id="527e4-160">The default limit is 1,000 but the visual creator can change that, up to a maximum of 30,000.</span></span>

### <a name="doughnut"></a><span data-ttu-id="527e4-161">แผนภูมิโดนัท</span><span class="sxs-lookup"><span data-stu-id="527e4-161">Doughnut</span></span>
- <span data-ttu-id="527e4-162">แต้มสูงสุด: 3,500</span><span class="sxs-lookup"><span data-stu-id="527e4-162">Max points: 3,500</span></span>
- <span data-ttu-id="527e4-163">กลุ่ม: 500 อันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-163">Group: Top 500</span></span>
- <span data-ttu-id="527e4-164">รายละเอียด: 20 อันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-164">Details: Top 20</span></span>

### <a name="filled-map-choropleth"></a><span data-ttu-id="527e4-165">แผนที่แถบสี choropleth</span><span class="sxs-lookup"><span data-stu-id="527e4-165">Filled map choropleth</span></span> 
<span data-ttu-id="527e4-166">แผนที่แถบสีสามารถใช้สถิติหรือขีดจำกัดแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="527e4-166">The filled map can use statistics or dynamic limits.</span></span> <span data-ttu-id="527e4-167">Power BI พยายามใช้ลดลำดับตามแผนต่อไปนี้: ขีดจำกัดแบบไดนามิก สถิติ และสุดท้ายการกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="527e4-167">Power BI tries to use reduction in the following order: dynamic limits, statistics, and lastly configuration.</span></span> 
- <span data-ttu-id="527e4-168">แต้มสูงสุด: 10000</span><span class="sxs-lookup"><span data-stu-id="527e4-168">Max points: 10000</span></span>
- <span data-ttu-id="527e4-169">หมวดหมู่: 500 อันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-169">Categories: Top 500</span></span>
- <span data-ttu-id="527e4-170">ชุดข้อมูล (เมื่อทั้ง X และ Y ปรากฏ): 20 อันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-170">Series (when both X and Y are present): Top 20</span></span>

### <a name="funnel"></a><span data-ttu-id="527e4-171">แผนภูมิกรวย</span><span class="sxs-lookup"><span data-stu-id="527e4-171">Funnel</span></span>
- <span data-ttu-id="527e4-172">แต้มสูงสุด: 3,500</span><span class="sxs-lookup"><span data-stu-id="527e4-172">Max points: 3,500</span></span>
- <span data-ttu-id="527e4-173">หมวดหมู่: 3,500 อันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-173">Categories: Top 3,500</span></span>

### <a name="kpi"></a><span data-ttu-id="527e4-174">KPI</span><span class="sxs-lookup"><span data-stu-id="527e4-174">KPI</span></span>
- <span data-ttu-id="527e4-175">แกนแนวโน้ม</span><span class="sxs-lookup"><span data-stu-id="527e4-175">Trend axis</span></span>
- <span data-ttu-id="527e4-176">3,500 อันดับล่างสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-176">Bottom 3,500</span></span>

### <a name="line-chart"></a><span data-ttu-id="527e4-177">แผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="527e4-177">Line chart</span></span>
<span data-ttu-id="527e4-178">ดู[วิธีการทำงานของเส้นอย่างง่าย ๆ](../create-reports/desktop-high-density-sampling.md#how-the-new-line-sampling-algorithm-works)</span><span class="sxs-lookup"><span data-stu-id="527e4-178">See [How line sampling works](../create-reports/desktop-high-density-sampling.md#how-the-new-line-sampling-algorithm-works)</span></span>

### <a name="line-chart-high-density"></a><span data-ttu-id="527e4-179">แผนภูมิเส้น ความหนาแน่นสูง</span><span class="sxs-lookup"><span data-stu-id="527e4-179">Line chart, high density</span></span>
<span data-ttu-id="527e4-180">ดู [การสุ่มตัวอย่างความหนาแน่นสูง](../create-reports/desktop-high-density-sampling.md)</span><span class="sxs-lookup"><span data-stu-id="527e4-180">See [High density sampling](../create-reports/desktop-high-density-sampling.md)</span></span>

### <a name="map"></a><span data-ttu-id="527e4-181">แผนที่</span><span class="sxs-lookup"><span data-stu-id="527e4-181">Map</span></span> 
- <span data-ttu-id="527e4-182">แต้มสูงสุด: 3,500</span><span class="sxs-lookup"><span data-stu-id="527e4-182">Max points: 3,500</span></span>

<span data-ttu-id="527e4-183">ขึ้นอยู่กับการกำหนดค่า แผนที่สามารถมี:</span><span class="sxs-lookup"><span data-stu-id="527e4-183">Depending on the configuration, a map can have:</span></span>
- <span data-ttu-id="527e4-184">ตำแหน่งที่ตั้ง: 3,500 อันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-184">Location: Top 3,500</span></span>
- <span data-ttu-id="527e4-185">ขนาด, ตำแหน่งที่ตั้ง: 3,500 อันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-185">Location, Size: Top 3,500</span></span>
- <span data-ttu-id="527e4-186">ตำแหน่งที่ตั้ง ละติจูด และลองจิจูดรวม (+/- ตามขนาด): 3,500 อันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-186">Location, Latitude, and Longitude aggregates (+/-Size): Top 3,500</span></span>
- <span data-ttu-id="527e4-187">ละติจูด ลองจิจูด: ดูการ[กระจายความหนาแน่นสูง](../create-reports/desktop-high-density-scatter-charts.md)</span><span class="sxs-lookup"><span data-stu-id="527e4-187">Latitude, Longitude: see [High density scatter](../create-reports/desktop-high-density-scatter-charts.md)</span></span>
- <span data-ttu-id="527e4-188">ละติจูด ลองจิจูด ขนาด: 3,500 อันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-188">Latitude, Longitude, Size: Top 3,500</span></span>
- <span data-ttu-id="527e4-189">คำอธิบายแผนภูมิ ละติจูด ลองจิจูด: ดูการ[กระจายความหนาแน่นสูง](../create-reports/desktop-high-density-scatter-charts.md)</span><span class="sxs-lookup"><span data-stu-id="527e4-189">Legend, Latitude, Longitude: see [High density scatter](../create-reports/desktop-high-density-scatter-charts.md)</span></span>
- <span data-ttu-id="527e4-190">คำอธิบายแผนภูมิ ละติจูด ลองจิจูด ขนาด: คำอธิบายแผนภูมิยอดนิยม 233 คำ,  ละติจูดและลองจิจูด 15 ตำแหน่งสูงสุด (สามารถใช้สถิติหรือขีดจำกัดแบบไดนามิกได้)</span><span class="sxs-lookup"><span data-stu-id="527e4-190">Legend, Latitude, Longitude, Size: Top 233 legends, Top 15 latitude and longitude  (could use statistics or dynamic limits)</span></span>
- <span data-ttu-id="527e4-191">ตำแหน่งที่ตั้ง คำอธิบายแผนภูมิ และละติจูดลองจิจูดแบบผลรวม (+/- ตามขนาด): ตำแหน่งที่ตั้งยอดนิยม 233 แห่ง คำอธิบายแผนภูมิยอดนิยม 15 คำ (สามารถใช้สถิติหรือขีดจำกัดแบบไดนามิก)</span><span class="sxs-lookup"><span data-stu-id="527e4-191">Location, Legend, Latitude, and Longitude as aggregates (+/-Size): Top 233 locations, Top 15 legends  (could use statistics or dynamic limits)</span></span>

### <a name="matrix"></a><span data-ttu-id="527e4-192">เมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="527e4-192">Matrix</span></span>
- <span data-ttu-id="527e4-193">แถว: การจำลองภาพเสมือน โดยใช้หน้าต่าง 500 แถวในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="527e4-193">Rows: Virtualization by using Window of 500 rows at a time</span></span>
- <span data-ttu-id="527e4-194">คอลัมน์: คอลัมน์การจัดกลุ่ม 100 อันดับแรก</span><span class="sxs-lookup"><span data-stu-id="527e4-194">Columns: Top 100 grouping columns</span></span> 
- <span data-ttu-id="527e4-195">ค่า: ค่าหลายค่าไม่ถูกนับรวมการลดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="527e4-195">Values: multiple values do not count against the data reduction</span></span>

### <a name="powerapps-visual"></a><span data-ttu-id="527e4-196">วิชวล PowerApps</span><span class="sxs-lookup"><span data-stu-id="527e4-196">PowerApps visual</span></span>
<span data-ttu-id="527e4-197">สามารถเพิ่มขึ้นได้ถึง 30,000 แต่จะขึ้นอยู่กับผู้สร้างวิชวลว่าต้องการให้ใช้กลยุทธ์ใด</span><span class="sxs-lookup"><span data-stu-id="527e4-197">Can get up to 30,000 but it is up to the visual authors to indicate what strategies to use.</span></span> <span data-ttu-id="527e4-198">ขีดจำกัดเริ่มต้นคือ 1,000 แต่ผู้สร้างวิชวลสามารถเปลี่ยนได้ สูงสุด 30,000</span><span class="sxs-lookup"><span data-stu-id="527e4-198">The default limit is 1,000 but the visual creator can change that, up to a maximum of 30,000.</span></span>

### <a name="radial-gauge"></a><span data-ttu-id="527e4-199">ตัววัดรัศมี</span><span class="sxs-lookup"><span data-stu-id="527e4-199">Radial gauge</span></span>
<span data-ttu-id="527e4-200">กลยุทธ์การลดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="527e4-200">No reduction strategy</span></span>

### <a name="slicer"></a><span data-ttu-id="527e4-201">ตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="527e4-201">Slicer</span></span>
- <span data-ttu-id="527e4-202">ค่า: การจำลองภาพเสมือน โดยใช้หน้าต่าง 200 แถวในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="527e4-202">Values: Virtualization by using Window of 200 rows at a time</span></span>

### <a name="scatter-chart-high-density"></a><span data-ttu-id="527e4-203">แผนภูมิกระจาย (แบบความหนาแน่นสูง)</span><span class="sxs-lookup"><span data-stu-id="527e4-203">Scatter chart (high density)</span></span>
<span data-ttu-id="527e4-204">ดู [การกระจายความหนาแน่นสูง](./desktop-high-density-scatter-charts.md)</span><span class="sxs-lookup"><span data-stu-id="527e4-204">See [High density scatter](./desktop-high-density-scatter-charts.md)</span></span>

### <a name="pie"></a><span data-ttu-id="527e4-205">แผนภูมิวงกลม</span><span class="sxs-lookup"><span data-stu-id="527e4-205">Pie</span></span>
- <span data-ttu-id="527e4-206">แต้มสูงสุด: 3,500</span><span class="sxs-lookup"><span data-stu-id="527e4-206">Max points: 3,500</span></span>
- <span data-ttu-id="527e4-207">กลุ่ม: 500 อันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-207">Group: Top 500</span></span>
- <span data-ttu-id="527e4-208">รายละเอียด: 20 อันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-208">Details: Top 20</span></span>

### <a name="r--python-visuals"></a><span data-ttu-id="527e4-209">วิชวล R & Python</span><span class="sxs-lookup"><span data-stu-id="527e4-209">R & Python visuals</span></span>
<span data-ttu-id="527e4-210">จำกัดไว้ที่ 150,000 แถว</span><span class="sxs-lookup"><span data-stu-id="527e4-210">Limited to 150,000 rows.</span></span> <span data-ttu-id="527e4-211">ถ้าเลือกมากกว่า 150,000 แถว ระบบจะใช้ 150,000 แถวบนสุดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="527e4-211">If more than 150,000 rows are selected, only the top 150,000 rows are used</span></span>

### <a name="ribbon-chart"></a><span data-ttu-id="527e4-212">แผนภูมิริบบอน</span><span class="sxs-lookup"><span data-stu-id="527e4-212">Ribbon chart</span></span>
- <span data-ttu-id="527e4-213">เมื่ออยู่ในโหมดแบบกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="527e4-213">When in categorical mode</span></span>
    - <span data-ttu-id="527e4-214">หมวดหมู่: การจำลองภาพเสมือน (หน้าต่างข้อมูล) โดยใช้หน้าต่าง 500 แถวในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="527e4-214">Categories: Virtualization (data windowing) by using Window of 500 rows at a time</span></span>
    - <span data-ttu-id="527e4-215">ชุดข้อมูล: 60 อันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-215">Series: Top 60</span></span>
    - <span data-ttu-id="527e4-216">เมื่ออยู่ในโหมดสเกลา (สามารถใช้ขีดจำกัดแบบไดนามิกได้)</span><span class="sxs-lookup"><span data-stu-id="527e4-216">When in scalar mode (could use dynamic limits)</span></span>
        - <span data-ttu-id="527e4-217">แต้มสูงสุด: 10,000</span><span class="sxs-lookup"><span data-stu-id="527e4-217">Max points: 10,000</span></span>
        - <span data-ttu-id="527e4-218">หมวดหมู่: ตัวอย่างของค่า 500 หน่วย</span><span class="sxs-lookup"><span data-stu-id="527e4-218">Categories: Sample of 500 values</span></span>
        - <span data-ttu-id="527e4-219">ชุดข้อมูล: 20 อันดับค่าตัวเลขสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-219">Series: Top 20 values</span></span>

### <a name="shape-map-preview"></a><span data-ttu-id="527e4-220">แผนที่รูปร่าง (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="527e4-220">Shape map (Preview)</span></span>
<span data-ttu-id="527e4-221">แผนที่รูปร่างสามารถใช้สถิติหรือขีดจำกัดแบบไดนามิกได้</span><span class="sxs-lookup"><span data-stu-id="527e4-221">The shape map can use statistics or dynamic limits.</span></span> 
- <span data-ttu-id="527e4-222">แต้มสูงสุด: 1,500</span><span class="sxs-lookup"><span data-stu-id="527e4-222">Max points: 1,500</span></span>
- <span data-ttu-id="527e4-223">หมวดหมู่: 500 อันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-223">Categories: Top 500</span></span>

### <a name="table"></a><span data-ttu-id="527e4-224">ตาราง</span><span class="sxs-lookup"><span data-stu-id="527e4-224">Table</span></span>
- <span data-ttu-id="527e4-225">ค่า: การจำลองภาพเสมือน (หน้าต่างข้อมูล) โดยใช้หน้าต่าง 500 แถวในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="527e4-225">Values: Virtualization (data windowing) by using Window of 500 rows at a time</span></span>

### <a name="tree-map-could-use-statistics-or-dynamic-limits"></a><span data-ttu-id="527e4-226">แผนที่ต้นไม้ (ซึ่งอาจใช้สถิติหรือขีดจำกัดแบบไดนามิก)</span><span class="sxs-lookup"><span data-stu-id="527e4-226">Tree map (could use statistics or dynamic limits)</span></span>
- <span data-ttu-id="527e4-227">แต้มสูงสุด: 3,500</span><span class="sxs-lookup"><span data-stu-id="527e4-227">Max points: 3,500</span></span>
- <span data-ttu-id="527e4-228">กลุ่ม: 500 อันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-228">Group: Top 500</span></span>
- <span data-ttu-id="527e4-229">รายละเอียด: 20 อันดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="527e4-229">Details: Top 20</span></span>

### <a name="waterfall-chart"></a><span data-ttu-id="527e4-230">แผนภูมิน้ำตก</span><span class="sxs-lookup"><span data-stu-id="527e4-230">Waterfall chart</span></span>
- <span data-ttu-id="527e4-231">เมื่อมีที่เก็บข้อมูลตามหมวดหมู่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="527e4-231">When there is only the category bucket</span></span>
    - <span data-ttu-id="527e4-232">แต้มสูงสุด: 3,500</span><span class="sxs-lookup"><span data-stu-id="527e4-232">Max points: 3,500</span></span>
    - <span data-ttu-id="527e4-233">ตามหมวดหมู่เท่านั้น - 3,500 ยอดนิยม</span><span class="sxs-lookup"><span data-stu-id="527e4-233">Category only - top 3,500</span></span>
- <span data-ttu-id="527e4-234">เมื่อมีการแบ่งประเภทและการแบ่งย่อยเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="527e4-234">When both category and breakdown are present</span></span>
    - <span data-ttu-id="527e4-235">ประเภท: การจำลองภาพเสมือน (หน้าต่างข้อมูล) โดยใช้หน้าต่าง 30 แถวในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="527e4-235">Category: Virtualization (data windowing) by using Window of 30 rows at a time</span></span>
    - <span data-ttu-id="527e4-236">การแบ่งย่อย - ค่าสูงสุด 200 ค่า</span><span class="sxs-lookup"><span data-stu-id="527e4-236">Breakdown - Top 200 values</span></span>


## <a name="next-steps"></a><span data-ttu-id="527e4-237">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="527e4-237">Next steps</span></span>
[<span data-ttu-id="527e4-238">ชนิดการแสดงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="527e4-238">Visualization types</span></span>](power-bi-report-visualizations.md)
