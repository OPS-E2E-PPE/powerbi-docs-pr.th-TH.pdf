---
title: เปลี่ยนวิธีการที่การแสดงผลด้วยภาพโต้ตอบในรายงาน
description: จัดทำเอกสารประกอบสำหรับวิธีการตั้งค่าการโต้ตอบแบบภาพในรายงานบริการ Microsoft Power BI และรายงาน Power BI Desktop
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: N_xYsCbyHPw
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 02/04/2020
LocalizationGroup: Reports
ms.openlocfilehash: 0070e8e997178a07c93bef4b80403f55aff9ae1d
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96387631"
---
# <a name="change-how-visuals-interact-in-a-power-bi-report"></a><span data-ttu-id="25cad-103">เปลี่ยนวิธีการที่การแสดงผลด้วยภาพโต้ตอบในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="25cad-103">Change how visuals interact in a Power BI report</span></span>
<span data-ttu-id="25cad-104">ถ้าคุณมีสิทธิ์ในการแก้ไขรายงาน คุณสามารถใช้ **โต้ตอบแบบภาพ** เพื่อเปลี่ยนวิธีแสดงภาพบนหน้ารายงานมีผลกระทบต่อกันได้</span><span class="sxs-lookup"><span data-stu-id="25cad-104">If you have edit permissions for a report, you can use **Visual interactions** to change how visualizations on a report page impact each other.</span></span> 

## <a name="introduction-to-visual-interactions"></a><span data-ttu-id="25cad-105">บทนำสู่การโต้ตอบกับภาพ</span><span class="sxs-lookup"><span data-stu-id="25cad-105">Introduction to visual interactions</span></span>
<span data-ttu-id="25cad-106">ตามค่าเริ่มต้น สามารถใช้การแสดงภาพบนหน้ารายงานเพื่อกรองแบบไขว้และไฮไลท์ข้ามไปยังแสดงภาพอื่น ๆ ในหน้าดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="25cad-106">By default, visualizations on a report page can be used to cross-filter and cross-highlight the other visualizations on the page.</span></span>
<span data-ttu-id="25cad-107">ตัวอย่างเช่น เลือกหนึ่งสถานะในการแสดงภาพของแผนที่เน้นแผนภูมิคอลัมน์และตัวกรองแผนภูมิเส้นเพื่อให้แสดงเฉพาะข้อมูลที่นำไปใช้กับหนึ่งสถานะดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="25cad-107">For example, selecting a state on a map visualization highlights the column chart and filters the line chart to display only data that applies to that one state.</span></span>
<span data-ttu-id="25cad-108">ดู[เกี่ยวกับการกรองและการเน้น](power-bi-reports-filters-and-highlighting.md)</span><span class="sxs-lookup"><span data-stu-id="25cad-108">See [About filtering and highlighting](power-bi-reports-filters-and-highlighting.md).</span></span> <span data-ttu-id="25cad-109">และหากคุณมีการแสดงภาพที่สนับสนุน[การเข้าถึงรายละเอียด](../consumer/end-user-drill.md)ตามค่าเริ่มต้น การเข้าถึงรายละเอียดข้อมูลแสดงภาพหนึ่งไม่มีผลกระทบต่อการแสดงภาพอื่น ๆ บนหน้ารายงานดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="25cad-109">And if you have a visualization that supports [drilling](../consumer/end-user-drill.md), by default, drilling one visualization has no impact on the other visualizations on the report page.</span></span> <span data-ttu-id="25cad-110">แต่ลักษณะการทำงานที่เป็นค่าเริ่มต้นทั้งสองนี้สามารถแทนที่ได้ และโต้ตอบมีการตั้งค่าในแบบต่อหนึ่งการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="25cad-110">But both of these default behaviors can be overridden, and interactions set, on a per-visualization basis.</span></span>

<span data-ttu-id="25cad-111">บทความนี้แสดงให้เห็นว่าคุณจะใช้ **การโต้ตอบกับภาพ** ใน Power BI Desktop ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="25cad-111">This article shows you how to use **visual interactions** in Power BI Desktop.</span></span> <span data-ttu-id="25cad-112">กระบวนการจะเหมือนกันกับในบริการ[มุมมองการแก้ไข](service-interact-with-a-report-in-editing-view.md)ของ Power BI </span><span class="sxs-lookup"><span data-stu-id="25cad-112">The process is the same in the Power BI service [Editing view](service-interact-with-a-report-in-editing-view.md).</span></span> <span data-ttu-id="25cad-113">ถ้ามีการแชร์รายงานกับคุณ คุณจะไม่สามารถเปลี่ยนการตั้งค่าการโต้ตอบแบบภาพได้</span><span class="sxs-lookup"><span data-stu-id="25cad-113">If you only have Reading view access, or the report has been shared with you, you will not be able to change the visual interactions settings.</span></span>

<span data-ttu-id="25cad-114">คำศัพท์ *ตัวกรองไขว้* และ *ไฮไลท์ข้าม* จะนำมาใช้เพื่อแยกความแตกต่างลักษณะการทำงานที่อธิบายไว้ที่นี่สำหรับสิ่งที่เกิดขึ้นเมื่อคุณใช้การพื้นที่ **ตัวกรอง** เพื่อ *กรอง* และ *เน้นการแสดงภาพ*</span><span class="sxs-lookup"><span data-stu-id="25cad-114">The terms *cross-filter* and *cross-highlight* are used to distinguish the behavior described here from what happens when you use the **Filters** pane to *filter* and *highlight* visualizations.</span></span>  

> [!NOTE]
> <span data-ttu-id="25cad-115">วิดีโอนี้ใช้เวอร์ชันเก่าของ Power BI Desktop และบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="25cad-115">This video uses older versions of Power BI Desktop and the Power BI service.</span></span> 
>
>

<iframe width="560" height="315" src="https://www.youtube.com/embed/N_xYsCbyHPw?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>


## <a name="enable-the-visual-interaction-controls"></a><span data-ttu-id="25cad-116">เปิดใช้งานตัวควบคุมการโต้ตอบกับภาพ</span><span class="sxs-lookup"><span data-stu-id="25cad-116">Enable the visual interaction controls</span></span>
<span data-ttu-id="25cad-117">หากคุณมีสิทธิ์แก้ไขรายงาน คุณสามารถเปิดการควบคุมการโต้ตอบกับภาพและกำหนดวิธีการแสดงภาพประกอบเพลงในตัวกรองหน้ารายงานของคุณและไฮไลท์ซึ่งกันและกัน</span><span class="sxs-lookup"><span data-stu-id="25cad-117">If you have edit permissions to a report, you can turn on the visual interaction controls and then customize how the visualizations on your  report page filter and highlight each other.</span></span> 

1. <span data-ttu-id="25cad-118">เลือกการแสดงภาพเพื่อเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="25cad-118">Select a visualization to make it active.</span></span>  
2. <span data-ttu-id="25cad-119">แสดงตัวเลือก **การโต้ตอบแบบภาพ**</span><span class="sxs-lookup"><span data-stu-id="25cad-119">Display the **Visual Interactions** options.</span></span>
    

    - <span data-ttu-id="25cad-120">ที่เดสก์ท็อป เลือก **รูปแบบ > การโต้ตอบ**</span><span class="sxs-lookup"><span data-stu-id="25cad-120">In Desktop, select **Format > Interactions**.</span></span>

        ![จากนั้นเลือก รูปแบบ และเลือก การโต้ตอบ](media/service-reports-visual-interactions/power-bi-interaction.png)

    - <span data-ttu-id="25cad-122">ในบริการ Power BI ให้เปิดรายงานในมุมมองการแก้ไขและเลือกรายการแบบเลื่อนลงจากแถบเมนูรายงาน</span><span class="sxs-lookup"><span data-stu-id="25cad-122">In the Power BI service, open the report in Editing view and select the dropdown from the report menu bar.</span></span>

        ![การโต้ตอบแบบภาพแบบเลื่อนลง](media/service-reports-visual-interactions/power-bi-service.png)

3. <span data-ttu-id="25cad-124">เมื่อต้องการแสดงตัวควบคุมการแสดงภาพโต้ตอบ เลือก **แก้ไขการโต้ตอบ**</span><span class="sxs-lookup"><span data-stu-id="25cad-124">To display the visualization interaction controls, select **Edit interactions**.</span></span> <span data-ttu-id="25cad-125">Power BI เพิ่มตัวกรองและไฮไลท์ข้ามไปยังการแสดงภาพอื่นๆ ทั้งหมดบนหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="25cad-125">Power BI adds filter and highlight icons to all of the other visualizations on the report page.</span></span> <span data-ttu-id="25cad-126">เราจะเห็นได้ว่าแผนผังต้นไม้เป็นการกรองข้ามแผนภูมิแบบเส้นและแมป และเป็นการเน้นแบบข้ามแผนผังคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="25cad-126">We can see that the tree map is cross-filtering the line chart and the map, and is cross-highlighting the column chart.</span></span> <span data-ttu-id="25cad-127">ตอนนี้คุณสามารถเปลี่ยนวิธีการสร้างภาพข้อมูลที่เลือกโต้ตอบกับการสร้างภาพข้อมูลอื่นๆ ในหน้ารายงานได้</span><span class="sxs-lookup"><span data-stu-id="25cad-127">You can now change how the selected visualization interacts with the other visualizations on the report page.</span></span>
   
    ![รายงานที่มีการโต้ตอบแบบภาพที่เปิดใช้งานอยู่](media/service-reports-visual-interactions/power-bi-turn-on.png)


## <a name="change-the-interaction-behavior"></a><span data-ttu-id="25cad-129">เปลี่ยนลักษณะการทำงานของการโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="25cad-129">Change the interaction behavior</span></span>
<span data-ttu-id="25cad-130">ทำความคุ้นเคยกับการสร้างภาพข้อมูลของคุณโดยการเลือกการสร้างภาพแต่ละภาพในหน้ารายงานของคุณทีละครั้ง</span><span class="sxs-lookup"><span data-stu-id="25cad-130">Get familiar with how your visualizations interact by selecting each visualization on your report page, one at a time.</span></span>  <span data-ttu-id="25cad-131">เลือกจุดข้อมูลหรือแถบหรือรูปร่างและดูผลกระทบต่อการสร้างภาพข้อมูลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="25cad-131">Select a data point or a bar or a shape and watch the impact on the other visualizations.</span></span> <span data-ttu-id="25cad-132">หากลักษณะการทำงานที่คุณเห็นไม่ใช่สิ่งที่คุณต้องการ คุณสามารถเปลี่ยนการโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="25cad-132">If the behavior you see is not what you'd prefer, you can change the interactions.</span></span> <span data-ttu-id="25cad-133">การเปลี่ยนแปลงเหล่านี้จะถูกบันทึกไว้ในรายงาน ดังนั้นคุณและผู้บริโภครายงานของคุณจะได้รับประสบการณ์การโต้ตอบกับภาพเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="25cad-133">These changes are saved with the report, so you and your report consumers will have the same visual interaction experience.</span></span>


<span data-ttu-id="25cad-134">เริ่มต้นด้วยการเลือกการแสดงภาพเพื่อเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="25cad-134">Start by selecting a visualization to make it active.</span></span>  <span data-ttu-id="25cad-135">โปรดสังเกตว่าการแสดงภาพอื่นๆ ทั้งหมดบนหน้าจะแสดงไอคอนโต้ตอบในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="25cad-135">Notice that all the other visualizations on the page now display interaction icons.</span></span> <span data-ttu-id="25cad-136">ไอคอนหนาคือรายการที่จะถูกนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="25cad-136">The bolded icon is the one that is being applied.</span></span> <span data-ttu-id="25cad-137">ถัดไป ให้พิจารณาว่าผลกระทบใดที่คุณต้องการให้ **การแสดงภาพที่เลือกไว้** มีผลต่อรายการอื่น</span><span class="sxs-lookup"><span data-stu-id="25cad-137">Next, determine what impact you'd like the **selected visualization** to have on the others.</span></span>  <span data-ttu-id="25cad-138">และมีอีกหนึ่งทางเลือกคือ ทำซ้ำสำหรับแสดงภาพอื่น ๆ ทั้งหมดบนหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="25cad-138">And, optionally, repeat for all other visualizations on the report page.</span></span>

<span data-ttu-id="25cad-139">ถ้าการแสดงภาพที่เลือกไว้:</span><span class="sxs-lookup"><span data-stu-id="25cad-139">If the selected visualization should:</span></span>
   
   * <span data-ttu-id="25cad-140">กรองข้ามการแสดงภาพอื่นๆ บนหน้า ให้เลือกไอคอน **ตัวกรอง** ในมุมบนขวาของ ![ไอคอนตัวกรอง](media/service-reports-visual-interactions/power-bi-filter-icon.png) ของการแสดงภาพนั้น</span><span class="sxs-lookup"><span data-stu-id="25cad-140">cross-filter one of the other visualizations on the page, select the **filter** icon in the upper right corner of that visualization ![filter icon](media/service-reports-visual-interactions/power-bi-filter-icon.png).</span></span>
   * <span data-ttu-id="25cad-141">ไฮไลต์ข้ามหนึ่งในการแสดงภาพอื่นๆ บนหน้า ให้เลือกไอคอน **ไฮไลต์** ![ไอคอนไฮไลต์](media/service-reports-visual-interactions/power-bi-highlight-icon.png)</span><span class="sxs-lookup"><span data-stu-id="25cad-141">cross-highlight one of the other visualizations on the page, select the **highlight** icon ![highlight icon](media/service-reports-visual-interactions/power-bi-highlight-icon.png).</span></span>
   * <span data-ttu-id="25cad-142">ไม่มีผลกระทบต่อการแสดงภาพอื่นๆ ภาพใดภาพหนึ่งบนหน้า ให้เลือกไอคอน **ไม่มีผลกระทบ** ![ไอคอนไม่มีผลกระทบ](media/service-reports-visual-interactions/power-bi-no-impact.png)</span><span class="sxs-lookup"><span data-stu-id="25cad-142">have no impact on one of the other visualizations on the page, select the **no impact** icon ![no impact icon](media/service-reports-visual-interactions/power-bi-no-impact.png).</span></span>

## <a name="change-the-interactions-of-drillable-visualizations"></a><span data-ttu-id="25cad-143">เปลี่ยนการโต้ตอบของการแสดงภาพที่สามารถเจาะได้</span><span class="sxs-lookup"><span data-stu-id="25cad-143">Change the interactions of drillable visualizations</span></span>
<span data-ttu-id="25cad-144">[การแสดงภาพ Power BI บางอย่างสามารถเจาะได้](../consumer/end-user-drill.md)</span><span class="sxs-lookup"><span data-stu-id="25cad-144">[Certain Power BI visualizations can be drilled](../consumer/end-user-drill.md).</span></span> <span data-ttu-id="25cad-145">ตามค่าเริ่มต้นเมื่อคุณเจาะการสร้างภาพข้อมูลนั้นจะไม่มีผลกระทบต่อการสร้างภาพข้อมูลอื่นๆ ในหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="25cad-145">By default, when you drill a visualization, it has no impact on the other visualizations on the report page.</span></span> <span data-ttu-id="25cad-146">แต่ลักษณะการทำงานนั้นสามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="25cad-146">But, that behavior can be changed.</span></span> 

> [!TIP]
> <span data-ttu-id="25cad-147">ลองด้วยตัวคุณเองโดยใช้[ไฟล์ PBIX ตัวอย่างทรัพยากรบุคคล](https://download.microsoft.com/download/6/9/5/69503155-05A5-483E-829A-F7B5F3DD5D27/Human%20Resources%20Sample%20PBIX.pbix)</span><span class="sxs-lookup"><span data-stu-id="25cad-147">Try it yourself using the [Human Resources sample PBIX file](https://download.microsoft.com/download/6/9/5/69503155-05A5-483E-829A-F7B5F3DD5D27/Human%20Resources%20Sample%20PBIX.pbix).</span></span> <span data-ttu-id="25cad-148">มีแผนภูมิคอลัมน์พร้อมดริลล์ดาวน์บนแท็บ **จ้างใหม่**</span><span class="sxs-lookup"><span data-stu-id="25cad-148">There's a column chart with drill down on the **New hires** tab.</span></span>
>

1. <span data-ttu-id="25cad-149">บรรยายภาพที่เจาะได้เพื่อให้ใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="25cad-149">Select the drillable visual to make it active.</span></span> 

2. <span data-ttu-id="25cad-150">เปิดใช้งานการดูข้อมูลแบบเจาะลึกโดยการเลือกไอคอนการดูรายละเอียดแนวลึก</span><span class="sxs-lookup"><span data-stu-id="25cad-150">Turn on drill down by selecting the drill down icon.</span></span>

    ![เปิดใช้งานการเจาะ](media/service-reports-visual-interactions/power-bi-drill-down.png)

2. <span data-ttu-id="25cad-152">จากแถบเมนู ให้เลือก **รูปแบบ** > **การเจาะตัวกรองภาพอื่น ๆ**</span><span class="sxs-lookup"><span data-stu-id="25cad-152">From the menu bar, select **Format** > **Drilling filters other visuals**.</span></span>  <span data-ttu-id="25cad-153">ในตอนนี้เมื่อคุณเจาะลึกลงรายละเอียด (และเจาะขึ้นมา) ในการแสดงภาพ การแสดงภาพอื่น ๆ บนหน้ารายงานจะเปลี่ยนเพื่อแสดงเลือกการเจาะลงรายละเอียดปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="25cad-153">Now when you drill down (and up) in a visualization, the other visualizations on the report page change to reflect your current drilling selection.</span></span> 

    ![เปิดการเจาะการกรองภาพอื่นๆ](media/service-reports-visual-interactions/power-bi-drill.png)

3. <span data-ttu-id="25cad-155">หากลักษณะการทำงานที่คุณเห็นไม่ใช่สิ่งที่คุณต้องการ คุณสามารถเปลี่ยนการโต้ตอบได้ [ตามที่อธิบายไว้ข้างต้น](#change-the-interaction-behavior)</span><span class="sxs-lookup"><span data-stu-id="25cad-155">If the behavior you see is not what you'd prefer, you can change the interactions [as described above](#change-the-interaction-behavior).</span></span>

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="25cad-156">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="25cad-156">Considerations and troubleshooting</span></span>
<span data-ttu-id="25cad-157">ถ้าคุณสร้างเมทริกซ์ด้วยเขตข้อมูลจากตารางที่แตกต่างกัน จากนั้นลองเน้นแบบข้ามโดยการเลือกหลายรายการในระดับที่แตกต่างกันของลำดับชั้น คุณจะได้รับข้อผิดพลาดในการแสดงผลด้วยภาพอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="25cad-157">If you build a matrix with fields from different tables, then try to cross-highlight by selecting multiple items at different levels of the hierarchy, you get errors on the other visuals.</span></span> 

![วิดีโอแสดงบักเมื่อพยายามกรองในระดับที่แตกต่างกันของลำดับชั้น](media/service-reports-visual-interactions/cross-highlight.gif)
    
## <a name="next-steps"></a><span data-ttu-id="25cad-159">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="25cad-159">Next steps</span></span>
[<span data-ttu-id="25cad-160">ตัวกรองและการไฮไลท์ในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="25cad-160">Filtering and highlighting in Power BI reports</span></span>](power-bi-reports-filters-and-highlighting.md)