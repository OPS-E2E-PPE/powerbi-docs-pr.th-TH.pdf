---
title: โครงข่ายของข้อมูล
description: 'บทช่วยสอน: สร้างการแสดงผลด้วยภาพโครงข่ายของข้อมูลใน Power BI'
author: mihart
ms.author: mihart
ms.reviewer: juluczni
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 01/10/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 47a8ef221caadfabebc5da00793b7fff0b8687f8
ms.sourcegitcommit: 396633fc5f7cff1f7d518f558b20043b2e05a513
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/14/2021
ms.locfileid: "98191877"
---
# <a name="create-and-view-decomposition-tree-visuals-in-power-bi"></a><span data-ttu-id="6f276-103">สร้างและดูวิชวลโครงข่ายของข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="6f276-103">Create and view decomposition tree visuals in Power BI</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="6f276-104">การแสดงผลด้วยภาพโครงข่ายของข้อมูลใน Power BI ช่วยให้คุณสามารถแสดงภาพข้อมูลข้ามหลายมิติได้</span><span class="sxs-lookup"><span data-stu-id="6f276-104">The decomposition tree visual in Power BI lets you visualize data across multiple dimensions.</span></span> <span data-ttu-id="6f276-105">โดยจะรวมข้อมูลและช่วยให้เจาะลึกลงในมิติของคุณในลำดับใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="6f276-105">It automatically aggregates data and enables drilling down into your dimensions in any order.</span></span> <span data-ttu-id="6f276-106">นอกจากนี้ยังเป็นการแสดงภาพข่าวกรอง (AI) แบบเทียมเพื่อให้คุณสามารถขอให้ค้นหามิติถัดไปเพื่อดูรายละเอียดแนวลึกตามเกณฑ์บางอย่าง</span><span class="sxs-lookup"><span data-stu-id="6f276-106">It is also an artificial intelligence (AI) visualization, so you can ask it to find the next dimension to drill down into based on certain criteria.</span></span> <span data-ttu-id="6f276-107">ซึ่งทำให้เป็นเครื่องมือที่มีประโยชน์สำหรับการสำรวจแบบเฉพาะกิจและการดำเนินการวิเคราะห์สาเหตุหลัก</span><span class="sxs-lookup"><span data-stu-id="6f276-107">This makes it a valuable tool for ad hoc exploration and conducting root cause analysis.</span></span>

![โครงข่ายของข้อมูล](media/power-bi-visualization-decomposition-tree/tree-full.png)

<span data-ttu-id="6f276-109">บทช่วยสอนนี้ใช้สองตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6f276-109">This tutorial uses two examples:</span></span>

- <span data-ttu-id="6f276-110">สถานการณ์ของห่วงโซ่อุปทานที่วิเคราะห์เปอร์เซ็นต์ของผลิตภัณฑ์ที่บริษัทมีในรายการค้างส่ง (สินค้าหมด)</span><span class="sxs-lookup"><span data-stu-id="6f276-110">A supply chain scenario that analyzes the percentage of products a company has on backorder (out of stock).</span></span>  
- <span data-ttu-id="6f276-111">สถานการณ์การขายที่แบ่งยอดขายของวิดีโอเกมตามปัจจัยหลายอย่างเช่น ประเภทเกมและผู้เผยแพร่</span><span class="sxs-lookup"><span data-stu-id="6f276-111">A sales scenario that breaks down video game sales by numerous factors like game genre and publisher.</span></span>

<span data-ttu-id="6f276-112">คุณสามารถค้นหา pbix ที่ใช้ในสถานการณ์ห่วงโซ่อุปทานได้ที่นี่: [Supply Chain Sample.pbix](
https://github.com/microsoft/powerbi-desktop-samples/blob/main/Sample%20Reports/Supply%20Chain%20Sample.pbix)</span><span class="sxs-lookup"><span data-stu-id="6f276-112">You can find the pbix used in the supply chain scenario here: [Supply Chain Sample.pbix](
https://github.com/microsoft/powerbi-desktop-samples/blob/main/Sample%20Reports/Supply%20Chain%20Sample.pbix).</span></span>

> [!NOTE]
> <span data-ttu-id="6f276-113">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="6f276-113">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span>    

## <a name="get-started"></a><span data-ttu-id="6f276-114">เริ่มใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6f276-114">Get started</span></span>
<span data-ttu-id="6f276-115">เลือกไอคอนแผนภูมิเส้นจากบานหน้าต่างการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="6f276-115">Select the decomposition tree icon from the Visualizations pane.</span></span>
<span data-ttu-id="6f276-116">![ลายน้ำโครงข่ายของข้อมูล](media/power-bi-visualization-decomposition-tree/tree-watermark.png)</span><span class="sxs-lookup"><span data-stu-id="6f276-116">![Decomposition tree watermark](media/power-bi-visualization-decomposition-tree/tree-watermark.png)</span></span>

<span data-ttu-id="6f276-117">การแสดงภาพต้องใช้การป้อนข้อมูลสองชนิด:</span><span class="sxs-lookup"><span data-stu-id="6f276-117">The visualization requires two types of input:</span></span>

 - <span data-ttu-id="6f276-118">**วิเคราะห์** –การวัดที่คุณต้องการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="6f276-118">**Analyze** – the metric you would like to analyze.</span></span> <span data-ttu-id="6f276-119">ซึ่งจะต้องเป็นหน่วยวัดหรือการรวม</span><span class="sxs-lookup"><span data-stu-id="6f276-119">This has to be a measure or an aggregate.</span></span>  
 - <span data-ttu-id="6f276-120">**อธิบายโดย** –หนึ่งหรือหลายมิติตามที่คุณต้องการดูรายละเอียดแนวลึก</span><span class="sxs-lookup"><span data-stu-id="6f276-120">**Explain By** – one or more dimensions you would like to drill down into.</span></span>

<span data-ttu-id="6f276-121">เมื่อคุณลากหน่วยวัดของคุณลงในเขตข้อมูลแล้ว การอัปเดตการแสดงผลด้วยภาพจะแสดงหน่วยวัดรวม</span><span class="sxs-lookup"><span data-stu-id="6f276-121">Once you drag your measure into the field well, the visual updates showcasing the aggregated measure.</span></span> <span data-ttu-id="6f276-122">ในตัวอย่างด้านล่างเราจะแสดง % เฉลี่ยของผลิตภัณฑ์บนรายการค้างส่ง (5.07%)</span><span class="sxs-lookup"><span data-stu-id="6f276-122">In the example below, we are visualizing the average % of products on backorder (5.07%).</span></span>

![โหนดรากของโครงข่ายของข้อมูล](media/power-bi-visualization-decomposition-tree/tree-root.png)

<span data-ttu-id="6f276-124">ขั้นตอนถัดไปคือการนำในหนึ่งหรือหลายมิติที่คุณต้องการดูรายละเอียดแนวลึก</span><span class="sxs-lookup"><span data-stu-id="6f276-124">The next step is to bring in one or more dimensions you would like to drill down into.</span></span> <span data-ttu-id="6f276-125">เพิ่มเขตข้อมูลเหล่านี้ลงในบักเก็ต **อธิบายโดย**</span><span class="sxs-lookup"><span data-stu-id="6f276-125">Add these fields to the **Explain by** bucket.</span></span> <span data-ttu-id="6f276-126">โปรดสังเกตว่าเครื่องหมายบวกจะปรากฏถัดจากโหนดรากของคุณ</span><span class="sxs-lookup"><span data-stu-id="6f276-126">Notice that a plus sign appears next to your root node.</span></span> <span data-ttu-id="6f276-127">การเลือก + ช่วยให้คุณสามารถเลือกเขตข้อมูลที่คุณต้องการดูรายละเอียดแนวลึกได้ (คุณสามารถดูฟิลด์ในลำดับใดก็ได้ที่คุณต้องการ)</span><span class="sxs-lookup"><span data-stu-id="6f276-127">Selecting the + lets you choose which field you would like to drill into (you can drill into fields in any order that you want).</span></span>

![สกรีนช็อตแสดงไอคอนบวกที่เลือกซึ่งแสดงตัวเลือกจากรายการอธิบายตาม](media/power-bi-visualization-decomposition-tree/tree-menu.png)

<span data-ttu-id="6f276-129">การเลือกชุดผลลัพธ์ **การคาดการณ์** ในแผนภูมิขยายและแบ่งหน่วยวัดตามค่าในคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="6f276-129">Selecting **Forecast bias** results in the tree expanding and breaking down the measure by the values in the column.</span></span> <span data-ttu-id="6f276-130">สามารถทำซ้ำกระบวนการนี้ได้โดยการเลือกโหนดอื่นเพื่อดูรายละเอียดแนวลึก</span><span class="sxs-lookup"><span data-stu-id="6f276-130">This process can be repeated by choosing another node to drill into.</span></span>

![การขยายโครงข่ายของข้อมูล](media/power-bi-visualization-decomposition-tree/tree-expansion.png)

<span data-ttu-id="6f276-132">การเลือกโหนดจากตัวกรองข้ามระดับสุดท้ายของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6f276-132">Selecting a node from the last level cross-filters the data.</span></span> <span data-ttu-id="6f276-133">การเลือกโหนดจากระดับก่อนหน้าเปลี่ยนเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="6f276-133">Selecting a node from an earlier level changes the path.</span></span>

![ภาพเคลื่อนไหวแสดงการเลือกโหนดจากระดับก่อนหน้าและวิธีเปลี่ยนการแสดงผลเพื่อแสดงโหนดย่อย](media/power-bi-visualization-decomposition-tree/tree-interaction.gif)

<span data-ttu-id="6f276-135">โต้ตอบด้วยการแสดงผลด้วยภาพอื่นๆ ผ่านตัวกรองโครงข่ายของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6f276-135">Interacting with other visuals cross-filters the decomposition tree.</span></span> <span data-ttu-id="6f276-136">ลำดับของโหนดภายในระดับสามารถเปลี่ยนเป็นผลลัพธ์ได้</span><span class="sxs-lookup"><span data-stu-id="6f276-136">The order of the nodes within levels could change as a result.</span></span>
<span data-ttu-id="6f276-137">ในตัวอย่างด้านล่าง เราได้ทำการกรองแบบผ่านตัวกรองโครงข่ายของข้อมูลด้วย Ubisoft</span><span class="sxs-lookup"><span data-stu-id="6f276-137">In the example below, we've cross-filtered the tree by Ubisoft.</span></span> <span data-ttu-id="6f276-138">เส้นทางจะอัปเดตและการขายของ Xbox จะย้ายจากอันดับหนึ่งไปเป็นอันดับสอง ซึ่งถูกแซงโดย PlayStation</span><span class="sxs-lookup"><span data-stu-id="6f276-138">The path updates and Xbox sales move from first to second place, surpassed by PlayStation.</span></span> 

<span data-ttu-id="6f276-139">หากเรากรองจากโครงข่ายของ Nintendo ยอดขาย Xbox จะว่างเปล่าเนื่องจากไม่มีเกม Nintendo ที่พัฒนาขึ้นสำหรับ Xbox</span><span class="sxs-lookup"><span data-stu-id="6f276-139">If we then cross-filter the tree by Nintendo, Xbox sales are blank as there are no Nintendo games developed for Xbox.</span></span> <span data-ttu-id="6f276-140">Xbox พร้อมกับเส้นทางที่ตามมาได้รับการกรองออกจากมุมมอง</span><span class="sxs-lookup"><span data-stu-id="6f276-140">Xbox, along with its subsequent path, gets filtered out of the view.</span></span>

<span data-ttu-id="6f276-141">แม้ว่าเส้นทางจะหายไป ระดับที่มีอยู่ (ในประเภทเกมกรณีนี้) จะยังคงปักหมุดอยู่บนโครงข่าย</span><span class="sxs-lookup"><span data-stu-id="6f276-141">Despite the path disappearing, the existing levels (in this case Game Genre) remain pinned on the tree.</span></span> <span data-ttu-id="6f276-142">การเลือกโหนด Nintendo จะขยายแผนภูมิไปยังประเภทเกมโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6f276-142">Selecting the Nintendo node therefore automatically expands the tree to Game Genre.</span></span>

![ภาพเคลื่อนไหวแสดงการเลือกตัวกรองข้ามซึ่งส่งผลต่อการแสดงโหนด](media/power-bi-visualization-decomposition-tree/tree-interaction-2.gif)


## <a name="ai-splits"></a><span data-ttu-id="6f276-144">การแยก AI</span><span class="sxs-lookup"><span data-stu-id="6f276-144">AI splits</span></span>

<span data-ttu-id="6f276-145">คุณสามารถใช้“ AI Splits” เพื่อหาว่าคุณควรดูข้อมูลต่อไปที่ใด</span><span class="sxs-lookup"><span data-stu-id="6f276-145">You can use “AI Splits” to figure out where you should look next in the data.</span></span> <span data-ttu-id="6f276-146">การแยกเหล่านี้ปรากฏที่ด้านบนของรายการและมีการทำเครื่องหมายด้วยหลอดไฟ</span><span class="sxs-lookup"><span data-stu-id="6f276-146">These splits appear at the top of the list and are marked with a lightbulb.</span></span> <span data-ttu-id="6f276-147">การแยกจะช่วยให้คุณค้นหาค่าสูงสุดและต่ำสุดในข้อมูลได้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6f276-147">The splits are there to help you find high and low values in the data, automatically.</span></span>

<span data-ttu-id="6f276-148">การวิเคราะห์สามารถทำงานได้สองวิธีโดยขึ้นอยู่กับการกำหนดลักษณะของคุณ</span><span class="sxs-lookup"><span data-stu-id="6f276-148">The analysis can work in two ways depending on your preferences.</span></span> <span data-ttu-id="6f276-149">ลักษณะการทำงานเริ่มต้นจะเป็นดังนี้:</span><span class="sxs-lookup"><span data-stu-id="6f276-149">The default behavior is as follows:</span></span>

 - <span data-ttu-id="6f276-150">**ค่าสูง**: พิจารณาฟิลด์ทั้งหมดที่มีอยู่และกำหนดว่าจะเจาะเข้าไปที่ใดเพื่อรับค่าสูงสุดของการวัดที่กำลังวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="6f276-150">**High Value**: Considers all available fields and determines which one to drill into to get the highest value of the measure being analyzed.</span></span>  
 - <span data-ttu-id="6f276-151">**ค่าต่ำ**: พิจารณาฟิลด์ทั้งหมดที่มีอยู่และกำหนดว่าจะเจาะเข้าไปที่ใดเพื่อรับค่าสูงสุดของการวัดที่กำลังวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="6f276-151">**Low Value**: Considers all available fields and determines which one to drill into to get the lowest value of the measure being analyzed.</span></span>  

<span data-ttu-id="6f276-152">การเลือก **ค่าสูง** ในตัวอย่างสินค้าค้าง ส่งผลลัพธ์ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6f276-152">Selecting **High Value** in the backorders example, results in the following:</span></span>

![โครงข่ายของข้อมูล AI แยก](media/power-bi-visualization-decomposition-tree/tree-ai-split.png)

<span data-ttu-id="6f276-154">หลอดไฟจะปรากฏขึ้นถัดจาก **ประเภทผลิตภัณฑ์** ที่ระบุว่านี่เป็น 'AI แยก'</span><span class="sxs-lookup"><span data-stu-id="6f276-154">A lightbulb appears next to **Product Type** indicating this was an ‘AI split’.</span></span> <span data-ttu-id="6f276-155">แผนผังยังมีเส้นประที่แนะนำโหนด **การตรวจสอบผู้ป่วย** เนื่องจากชุดผลลัพธ์นั้นมีค่าสูงสุดของรายการค้าง (9.2%).</span><span class="sxs-lookup"><span data-stu-id="6f276-155">The tree also provides a dotted line recommending the **Patient Monitoring** node as that results in the highest value of backorders (9.2%).</span></span> 

<span data-ttu-id="6f276-156">วางเมาส์เหนือหลอดไฟเพื่อดูเคล็ดลับเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="6f276-156">Hover over the lightbulb to see a tooltip.</span></span> <span data-ttu-id="6f276-157">ในตัวอย่างนี้คำแนะนำเครื่องมือคือ “% ตามรายการค้างสูงสุดเมื่อประเภทผลิตภัณฑ์คือการตรวจสอบผู้ป่วย”</span><span class="sxs-lookup"><span data-stu-id="6f276-157">In this example, the tooltip is “% on backorder is highest when Product Type is Patient Monitoring”.</span></span>

<span data-ttu-id="6f276-158">คุณสามารถกำหนดค่าการแสดงผลด้วยภาพเพื่อค้นหาการแยก **แบบสัมพัทธ์** เมื่อเทียบกับ **แบบสัมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="6f276-158">You can configure the visual to find **Relative** AI splits as opposed to **Absolute** ones.</span></span> 

<span data-ttu-id="6f276-159">โหมดสัมพัทธ์จะค้นหาค่าสูงที่โดดเด่น (เปรียบเทียบกับส่วนที่เหลือของข้อมูลในคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="6f276-159">Relative mode looks for high values that stand out (compared to the rest of the data in the column).</span></span> <span data-ttu-id="6f276-160">เพื่อแสดงให้เห็นตัวอย่าง มาลองดูตัวอย่างต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6f276-160">To illustrate this, let’s take a look at an example:</span></span>

![โครงข่ายของข้อมูลแยกแบบสัมบูรณ์](media/power-bi-visualization-decomposition-tree/tree-ai-absolute.png)

<span data-ttu-id="6f276-162">ในสกรีนช็อตด้านบน เรากำลังมองหายอดขายของวิดีโอเกมในอเมริกาเหนือ</span><span class="sxs-lookup"><span data-stu-id="6f276-162">In the screenshot above, we are looking at North America sales of video games.</span></span> <span data-ttu-id="6f276-163">ก่อนอื่นเราจะแยกโครงข่ายด้วย **ชื่อผู้เผยแพร่** จากนั้นดูรายละเอียดใน Nintendo</span><span class="sxs-lookup"><span data-stu-id="6f276-163">We first split the tree by **Publisher Name** and then drill into Nintendo.</span></span> <span data-ttu-id="6f276-164">การเลือก **ค่าสูง** ผลลัพธ์ในการขยายของ **แพลตฟอร์มคือ Nintendo**</span><span class="sxs-lookup"><span data-stu-id="6f276-164">Selecting **High Value** results in the expansion of **Platform is Nintendo**.</span></span> <span data-ttu-id="6f276-165">เนื่องจาก Nintendo (ผู้เผยแพร่) เท่านั้นที่พัฒนาสำหรับคอนโซล Nintendo มีค่าเพียงค่าเดียวเท่านั้นดังนั้นค่าสูงสุดจึงไม่น่าแปลกใจ</span><span class="sxs-lookup"><span data-stu-id="6f276-165">Since Nintendo (the publisher) only develops for Nintendo consoles, there is only one value present and so that is unsurprisingly the highest value.</span></span>

<span data-ttu-id="6f276-166">อย่างไรก็ตามการแยกที่น่าสนใจยิ่งขึ้นคือการดูว่าค่าสูงเด่นกว่าค่าอื่นๆ ในคอลัมน์เดียวกันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6f276-166">Nevertheless, a more interesting split would be to look at which high value stands out relative to other values in the same column.</span></span> <span data-ttu-id="6f276-167">ถ้าเราเปลี่ยนชนิดการวิเคราะห์จาก **แบบสัมบูรณ์** เป็น **แบบสัมพัทธ์** เราได้รับผลลัพธ์ดังต่อไปนี้สำหรับ Nintendo: ![โครงข่ายของข้อมูลแบบสัมบูรณ์แยก](media/power-bi-visualization-decomposition-tree/tree-ai-relative.png)</span><span class="sxs-lookup"><span data-stu-id="6f276-167">If we change the Analysis type from **Absolute** to **Relative**, we get the following result for Nintendo: ![Decomposition tree relative split](media/power-bi-visualization-decomposition-tree/tree-ai-relative.png)</span></span>

<span data-ttu-id="6f276-168">เวลานี้ค่าที่แนะนำคือ **แพลตฟอร์มภายในประเภทเกม**</span><span class="sxs-lookup"><span data-stu-id="6f276-168">This time, the recommended value is **Platform within Game Genre**.</span></span>  <span data-ttu-id="6f276-169">แพลตฟอร์มไม่ได้ให้ค่าสัมบูรณ์สูงกว่า Nintendo ($19,950,000 เทียบกับ $46,950,000)</span><span class="sxs-lookup"><span data-stu-id="6f276-169">Platform doesn’t yield a higher absolute value than Nintendo ($19,950,000 vs. $46,950,000).</span></span> <span data-ttu-id="6f276-170">อย่างไรก็ตามมันเป็นคุณค่าที่โดดเด่น</span><span class="sxs-lookup"><span data-stu-id="6f276-170">Nevertheless it’s a value that stands out.</span></span>

<span data-ttu-id="6f276-171">แม่นยำยิ่งขึ้นเนื่องจากมีค่าเกม 10 ประเภทค่าที่คาดหวังสำหรับแพลตฟอร์มจะเท่ากับ $4.6 M หากพวกเขาถูกแบ่งเท่าๆ กัน</span><span class="sxs-lookup"><span data-stu-id="6f276-171">More precisely, since there are 10 Game Genre values, the expected value for Platform would be $4.6M if they were to be split evenly.</span></span> <span data-ttu-id="6f276-172">เนื่องจากแพลตฟอร์มมีมูลค่าเกือบ $20M ซึ่งเป็นผลลัพธ์ที่น่าสนใจเนื่องจากสูงกว่าผลลัพธ์ที่คาดไว้ถึงสี่เท่า</span><span class="sxs-lookup"><span data-stu-id="6f276-172">Since Platform has a value of almost $20M, that is an interesting result as it is four times higher than the expected result.</span></span>

<span data-ttu-id="6f276-173">การคำนวณมีดังนี้:</span><span class="sxs-lookup"><span data-stu-id="6f276-173">The calculation is as follows:</span></span>

<span data-ttu-id="6f276-174">ยอดขายในอเมริกาเหนือสำหรับแพลตฟอร์ม/ Abs (ค่าเฉลี่ย (ยอดขายในอเมริกาเหนือสำหรับประเภทเกม))</span><span class="sxs-lookup"><span data-stu-id="6f276-174">North America Sales for Platform/ Abs(Avg(North America Sales for Game Genre))</span></span>  
<span data-ttu-id="6f276-175">vs</span><span class="sxs-lookup"><span data-stu-id="6f276-175">vs.</span></span>  
<span data-ttu-id="6f276-176">ยอดขายในอเมริกาเหนือสำหรับ Nintendo / Abs (เฉลี่ย (ยอดขายในอเมริกาเหนือสำหรับแพลตฟอร์ม))</span><span class="sxs-lookup"><span data-stu-id="6f276-176">North America Sales for Nintendo / Abs(Avg(North America Sales for Platform))</span></span>  

<span data-ttu-id="6f276-177">ซึ่งตีเป็น:</span><span class="sxs-lookup"><span data-stu-id="6f276-177">Which translates to:</span></span>

<span data-ttu-id="6f276-178">19,550,000 / (19,550,000 + 11,140,000 + ... + 470,000 + 60,000 /10) = 4.25x</span><span class="sxs-lookup"><span data-stu-id="6f276-178">19,550,000 / (19,550,000 + 11,140,000 + ... + 470,000 + 60,000 /10) = 4.25x</span></span>  
<span data-ttu-id="6f276-179">vs</span><span class="sxs-lookup"><span data-stu-id="6f276-179">vs.</span></span>  
<span data-ttu-id="6f276-180">46,950,000/ (46,950,000/1) = 1x</span><span class="sxs-lookup"><span data-stu-id="6f276-180">46,950,000/ (46,950,000/1) = 1x</span></span>  

<span data-ttu-id="6f276-181">หากคุณไม่ต้องการใช้การแบ่ง AI ใด ๆ ในแผนผังคุณยังมีตัวเลือกในการปิดการใช้งานเหล่านี้ภายใต้ตัวเลือก **การจัดรูปแบบการวิเคราะห์** ตัวเลือก:</span><span class="sxs-lookup"><span data-stu-id="6f276-181">If you prefer not to use any AI splits in the tree, you also have the option of turning them off under the **Analysis formatting** options:</span></span>  

![โครงข่ายของข้อมูลปิดใช้งาน  AI แยก](media/power-bi-visualization-decomposition-tree/tree-ai-disable.png)

## <a name="tree-interactions-with-ai-splits"></a><span data-ttu-id="6f276-183">การโต้ตอบกับโครงข่ายของ AI</span><span class="sxs-lookup"><span data-stu-id="6f276-183">Tree interactions with AI splits</span></span>

<span data-ttu-id="6f276-184">คุณสามารถมี AI ได้หลายระดับ</span><span class="sxs-lookup"><span data-stu-id="6f276-184">You can have multiple subsequent AI levels.</span></span> <span data-ttu-id="6f276-185">นอกจากนี้คุณยังสามารถผสม  AI ระดับต่างๆ ได้ (จากค่าสูงไปหาค่าต่ำและกลับไปเป็นมูลค่าสูง):</span><span class="sxs-lookup"><span data-stu-id="6f276-185">You can also mix up different kinds of AI levels (go from High Value to Low Value and back to High Value):</span></span>

![โครงข่ายของข้อมูล AI หลายเส้นทาง](media/power-bi-visualization-decomposition-tree/tree-multi-ai-path.png)

<span data-ttu-id="6f276-187">หากคุณเลือกโหนดอื่นในโครงข่าย AI แยกจะคำนวณใหม่ตั้งแต่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6f276-187">If you select a different node in the tree, the AI Splits recalculate from scratch.</span></span> <span data-ttu-id="6f276-188">ในตัวอย่างด้านล่างเราเปลี่ยนโหนดที่เลือกในระดับ **การคาดการณ์อคติ**</span><span class="sxs-lookup"><span data-stu-id="6f276-188">In the example below, we changed the selected node in the **Forecast Bias** level.</span></span> <span data-ttu-id="6f276-189">ระดับที่ตามมาจะเปลี่ยนเพื่อให้ได้ค่าที่สูงและต่ำที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6f276-189">The subsequent levels change to yield the correct High and Low Values.</span></span>

![โครงข่ายของข้อมูลปฏิสัมพันธ์ AI](media/power-bi-visualization-decomposition-tree/tree-ai-interactions.png)

<span data-ttu-id="6f276-191">ระดับ AI จะคำนวณอีกครั้งเมื่อคุณผ่านการกรองโครงข่ายของข้อมูลด้วยภาพอื่น</span><span class="sxs-lookup"><span data-stu-id="6f276-191">AI levels are also recalculated when you cross-filter the decomposition tree by another visual.</span></span> <span data-ttu-id="6f276-192">ในตัวอย่างด้านล่างเราจะเห็นว่า % รายการค้าง ของเราสูงสุดสำหรับโรงงาน #0477</span><span class="sxs-lookup"><span data-stu-id="6f276-192">In the example below, we can see that our backorder % is highest for Plant #0477.</span></span>

![สกรีนช็อตแสดงการวิเคราะห์สาเหตุที่แท้จริงโดยเดือนที่เลือกทั้งหมด](media/power-bi-visualization-decomposition-tree/tree-ai-crossfilter1.png)

<span data-ttu-id="6f276-194">แต่ถ้าเราเลือก **เดือนเมษายน** ในแผนภูมิแท่ง การเปลี่ยนแปลงสูงสุดของ **ชนิดผลิตภัณฑ์คือราคาประหยัดขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="6f276-194">But if we select **April** in the bar chart, the highest changes to **Product Type is Advanced Surgical**.</span></span> <span data-ttu-id="6f276-195">ในกรณีนี้ไม่ได้เป็นเพียงแค่โหนดที่เรียงลำดับใหม่ แต่เลือกคอลัมน์ที่แตกต่างอย่างสิ้นเชิง</span><span class="sxs-lookup"><span data-stu-id="6f276-195">In this case, it’s not just the nodes that got reordered, but a completely different column was chosen.</span></span> 

![สกรีนช็อตแสดงการวิเคราะห์สาเหตุที่แท้จริงโดยเลือกเฉพาะเดือนเมษายน](media/power-bi-visualization-decomposition-tree/tree-ai-crossfilter2.png)

<span data-ttu-id="6f276-197">หากเราต้องการให้ระดับ  AI ทำงานเหมือนระดับที่ไม่ใช่  AI ให้เลือกหลอดไฟเพื่อเปลี่ยนพฤติกรรมกลับเป็นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6f276-197">If we want AI levels to behave like non-AI levels, select the lightbulb to revert the behavior to default.</span></span> 

<span data-ttu-id="6f276-198">ในขณะที่หลายระดับ  AI สามารถผูกมัดด้วยกัน แต่ระดับที่ไม่ใช่  AI ไม่สามารถติดตามระดับ  AI ได้</span><span class="sxs-lookup"><span data-stu-id="6f276-198">While multiple AI levels can be chained together, a non-AI level cannot follow an AI level.</span></span> <span data-ttu-id="6f276-199">หากเราทำการแยกแบบแมนนวลหลังจากการแยกแบบ  AI หลอดไฟจากระดับ  AI จะหายไปและระดับจะเปลี่ยนเป็นระดับปกติ</span><span class="sxs-lookup"><span data-stu-id="6f276-199">If we do a manual split following an AI split, the lightbulb from the AI level disappears and the level transforms into a normal level.</span></span> 

## <a name="locking"></a><span data-ttu-id="6f276-200">การล็อก</span><span class="sxs-lookup"><span data-stu-id="6f276-200">Locking</span></span>

<span data-ttu-id="6f276-201">ผู้สร้างเนื้อหาสามารถล็อคระดับสำหรับผู้ใช้บริโภค</span><span class="sxs-lookup"><span data-stu-id="6f276-201">A content creator can lock levels for report consumers.</span></span> <span data-ttu-id="6f276-202">เมื่อระดับถูกล็อคจะไม่สามารถลบหรือเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="6f276-202">When a level is locked, it cannot be removed or changed.</span></span> <span data-ttu-id="6f276-203">ผู้บริโภคสามารถสำรวจเส้นทางที่แตกต่างภายในระดับล็อค แต่พวกเขาไม่สามารถเปลี่ยนระดับเองได้</span><span class="sxs-lookup"><span data-stu-id="6f276-203">A consumer can explore different paths within the locked level but they cannot change the level itself.</span></span> <span data-ttu-id="6f276-204">ในฐานะผู้สร้าง คุณสามารถวางเมาส์เหนือระดับที่มีอยู่เพื่อดูไอคอนล็อคได้</span><span class="sxs-lookup"><span data-stu-id="6f276-204">As a creator you can hover over existing levels to see the lock icon.</span></span> <span data-ttu-id="6f276-205">คุณสามารถล็อคได้หลายระดับตามที่คุณต้องการ แต่คุณไม่สามารถปลดล็อคระดับก่อนหน้าระดับล็อคได้</span><span class="sxs-lookup"><span data-stu-id="6f276-205">You can lock as many levels as you want, but you cannot have unlocked levels preceding locked levels.</span></span>

<span data-ttu-id="6f276-206">ในตัวอย่างด้านล่าง มีสองระดับแรกถูกล็อค</span><span class="sxs-lookup"><span data-stu-id="6f276-206">In the example below, the first two levels are locked.</span></span> <span data-ttu-id="6f276-207">ซึ่งหมายความว่าผู้บริโภคดังกล่าวสามารถเปลี่ยนเป็นระดับ 3 และ 4 และเพิ่มระดับใหม่ในภายหลังได้</span><span class="sxs-lookup"><span data-stu-id="6f276-207">This means that report consumers can change level 3 and 4, and even add new levels afterwards.</span></span> <span data-ttu-id="6f276-208">อย่างไรก็ตาม จะไม่สามารถเปลี่ยนแปลงสองระดับแรกได้:</span><span class="sxs-lookup"><span data-stu-id="6f276-208">The first two levels however cannot be changed:</span></span>

![การล็อกโครงข่ายของข้อมูล](media/power-bi-visualization-decomposition-tree/tree-locking.png)

## <a name="known-limitations"></a><span data-ttu-id="6f276-210">ข้อจำกัดที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="6f276-210">Known limitations</span></span>

<span data-ttu-id="6f276-211">จำนวนสูงสุดของระดับสำหรับทรีคือ 50</span><span class="sxs-lookup"><span data-stu-id="6f276-211">The maximum number of levels for the tree is 50.</span></span> <span data-ttu-id="6f276-212">จำนวนสูงสุดของจุดข้อมูลที่สามารถแสดงภาพได้ในหนึ่งครั้งบนทรีคือ 5,000</span><span class="sxs-lookup"><span data-stu-id="6f276-212">Maximum number of data points that can be visualized at one time on the tree is 5000.</span></span> <span data-ttu-id="6f276-213">เราตัดทอนระดับเพื่อแสดง Top n</span><span class="sxs-lookup"><span data-stu-id="6f276-213">We truncate levels to show top n.</span></span> <span data-ttu-id="6f276-214">ในปัจจุบัน Top n ต่อระดับจะถูกตั้งค่าเป็น 10</span><span class="sxs-lookup"><span data-stu-id="6f276-214">Currently the top n per level is set to 10.</span></span> 

<span data-ttu-id="6f276-215">โครงข่ายของข้อมูลไม่สนับสนุนสถานการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6f276-215">The decomposition tree is not supported in the following scenarios:</span></span>  
-   <span data-ttu-id="6f276-216">ไม่สามารถเข้าถึงบริการการวิเคราะห์ภายในองค์กรได้</span><span class="sxs-lookup"><span data-stu-id="6f276-216">On-premises Analysis Services</span></span>

<span data-ttu-id="6f276-217">การแยก AI ไม่ได้รับการสนับสนุนในสถานการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6f276-217">AI splits are not supported in the following scenarios:</span></span>  
-   <span data-ttu-id="6f276-218">Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6f276-218">Azure Analysis Services</span></span>
-   <span data-ttu-id="6f276-219">เซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="6f276-219">Power BI Report Server</span></span>
-   <span data-ttu-id="6f276-220">เผยแพร่บนเว็บ</span><span class="sxs-lookup"><span data-stu-id="6f276-220">Publish to Web</span></span>
-   <span data-ttu-id="6f276-221">หน่วยวัดที่ซับซ้อนและหน่วยวัดจากส่วนขยาย schema ใน ' วิเคราะห์ '</span><span class="sxs-lookup"><span data-stu-id="6f276-221">Complex measures and measures from extensions schemas in 'Analyze'</span></span>

<span data-ttu-id="6f276-222">ข้อจำกัดด้านอื่น:</span><span class="sxs-lookup"><span data-stu-id="6f276-222">Other limitations:</span></span>
- <span data-ttu-id="6f276-223">การสนับสนุนภายในถามตอบ</span><span class="sxs-lookup"><span data-stu-id="6f276-223">Support inside Q&A</span></span>

## <a name="next-steps"></a><span data-ttu-id="6f276-224">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="6f276-224">Next steps</span></span>

[<span data-ttu-id="6f276-225">สร้างแผนภูมิโดนัท Power BI</span><span class="sxs-lookup"><span data-stu-id="6f276-225">Power BI doughnut chart</span></span>](power-bi-visualization-doughnut-charts.md)

[<span data-ttu-id="6f276-226">การแสดงผลข้อมูลด้วยภาพของ Power BI</span><span class="sxs-lookup"><span data-stu-id="6f276-226">Power BI visualizations</span></span>](power-bi-report-visualizations.md)

