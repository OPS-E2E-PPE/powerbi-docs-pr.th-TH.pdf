---
title: ทำความเข้าใจวิธีการที่การแสดงผลด้วยภาพโต้ตอบในรายงาน
description: เอกสารสำหรับผู้ใช้ Power BI ที่อธิบายวิธีการที่ภาพโต้ตอบในหน้ารายงาน
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-explore
ms.topic: how-to
ms.date: 09/11/2020
LocalizationGroup: Reports
ms.openlocfilehash: bfb96a6c4d078744bdd285f07ea5cf88a55aab25
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96399890"
---
# <a name="how-visuals-cross-filter-each-other-in-a-power-bi-report"></a><span data-ttu-id="c056b-103">วิธีการใช้วิชวลกรองข้ามกันในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="c056b-103">How visuals cross-filter each other in a Power BI report</span></span>

[!INCLUDE[consumer-appliesto-yyny](../includes/consumer-appliesto-yyny.md)]

<span data-ttu-id="c056b-104">คุณลักษณะยอดเยี่ยมประการหนึ่งของ Power BI คือแนวทางที่ภาพทั้งหมดในหน้ารายงานเชื่อมโยงถึงกัน</span><span class="sxs-lookup"><span data-stu-id="c056b-104">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="c056b-105">หากคุณเลือกจุดข้อมูลในภาพภาพหนึ่ง ภาพอื่นทั้งหมดบนหน้าที่มีข้อมูลที่เปลี่ยนไปนั้นตามการเลือกนั้น</span><span class="sxs-lookup"><span data-stu-id="c056b-105">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> 

![วิดีโอการตอบโต้ด้วยภาพ](media/end-user-interactions/interactions.gif)

## <a name="how-visuals-interact-with-each-other"></a><span data-ttu-id="c056b-107">การแสดงภาพทำงานโต้ตอบกันอย่างไร</span><span class="sxs-lookup"><span data-stu-id="c056b-107">How visuals interact with each other</span></span>

<span data-ttu-id="c056b-108">ตามค่าเริ่มต้นแล้ว การเลือกจุดข้อมูลในการแสดงภาพหนึ่งบนหน้ารายงานจะกรองข้ามหรือไฮไลท์ข้ามการแสดงภาพอื่น ๆ บนหน้า</span><span class="sxs-lookup"><span data-stu-id="c056b-108">By default, selecting a data point in one visual on a report page will cross-filter or cross-highlight the other visuals on the page.</span></span> <span data-ttu-id="c056b-109">*ผู้ออกแบบ* รายงานกำหนดการโต้ตอบของภาพบนหน้าไว้แท้จริงอย่างไร</span><span class="sxs-lookup"><span data-stu-id="c056b-109">Exactly how the visuals on a page interact is set by the report *designer*.</span></span> <span data-ttu-id="c056b-110">*ผู้ออกแบบ* มีทางเลือกในการเปิดและปิดการโต้ตอบด้วยภาพ และเปลี่ยนลักษณะงานในการกรองข้าม การไฮไลท์ข้าม และ [การดูข้อมูลแบบเจาะลึก](end-user-drill.md)ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c056b-110">*Designers* have options to turn visual interactions on and off, and to change the default cross-filtering,  cross-highlighting, and [drilling](end-user-drill.md) behavior.</span></span> 

<span data-ttu-id="c056b-111">หากคุณยังไม่พบลำดับชั้นหรือการดูข้อมูลแบบเจาะลึกใด ๆ คุณสามารถเรียนรู้ทั้งหมดได้โดยการอ่านหัวข้อ [ดูข้อมูลแบบเจาะลึกใน Power BI](end-user-drill.md)</span><span class="sxs-lookup"><span data-stu-id="c056b-111">If you haven't encountered hierarchies or drilling yet, you can learn all about them by reading [drill down in Power BI](end-user-drill.md).</span></span> 

### <a name="cross-filtering-and-cross-highlighting"></a><span data-ttu-id="c056b-112">การกรองข้ามและการไฮไลต์แบบเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="c056b-112">Cross-filtering and cross-highlighting</span></span>

<span data-ttu-id="c056b-113">การกรองข้ามและการไฮไลท์ข้ามมีประโยชน์ในการแสดงให้เห็นว่าค่าหนึ่งในข้อมูลของคุณนั้นมีส่วนเกี่ยวข้องกับค่าอื่นอย่างไร</span><span class="sxs-lookup"><span data-stu-id="c056b-113">Cross-filtering and cross-highlighting can be useful to identify how one value in your data contributes to another.</span></span> <span data-ttu-id="c056b-114">ระบบจะใช้คำว่า *การกรองข้าม* และ *การไฮไลท์ข้าม* เพื่อแยกแยะความแตกต่างระหว่างลักษณะงานที่อธิบายไว้ในส่วนนี้กับสิ่งที่เกิดขึ้นเมื่อคุณใช้บานหน้าต่าง **ตัวกรอง** เพื่อกรองและไฮไลท์ภาพ</span><span class="sxs-lookup"><span data-stu-id="c056b-114">The terms *cross-filter* and *cross-highlight* are used to distinguish the behavior described here from what happens when you use the **Filters** pane to filter and highlight visuals.</span></span>  

<span data-ttu-id="c056b-115">มากำหนดคำเหล่านี้ตามที่เราได้ดูหน้ารายงานด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="c056b-115">Let's define these terms as we look at the report pages below.</span></span> <span data-ttu-id="c056b-116">แผนภูมิโดนัท “ปริมาณประเภทโดยรวมตามเซกเม้น” มีสองค่า: "การควบคุม" และ "ความสะดวกสบาย"</span><span class="sxs-lookup"><span data-stu-id="c056b-116">The "Total category volume by segment" doughnut chart has two values: "Moderation" and "Convenience".</span></span> 

![หน้ารายงาน](media/end-user-interactions/power-bi-interactions-before.png)

1. <span data-ttu-id="c056b-118">มาดูว่าเกิดอะไรขึ้นเมื่อเราเลือก **การควบคุม**</span><span class="sxs-lookup"><span data-stu-id="c056b-118">Let's see what happens when we select **Moderation**.</span></span>

    ![หน้ารายงานหลังจากส่วนควบคุมของแผนภูมิโดนัทที่เลือก](media/end-user-interactions/power-bi-interactions-after.png)

2. <span data-ttu-id="c056b-120">**การกรองข้าม** นำข้อมูลที่ไม่ได้ใช้ออก</span><span class="sxs-lookup"><span data-stu-id="c056b-120">**Cross-filtering** removes data that doesn't apply.</span></span> <span data-ttu-id="c056b-121">การเลือก **การควบคุม** ในแผนภูมิรูปโดนัทกรองข้ามแผนภูมิแบบเส้น</span><span class="sxs-lookup"><span data-stu-id="c056b-121">Selecting **Moderation** in the doughnut chart cross-filters the line chart.</span></span> <span data-ttu-id="c056b-122">แผนภูมิแบบเส้นเท่านั้นที่แสดงจุดข้อมูลสำหรับส่วนควบคุม</span><span class="sxs-lookup"><span data-stu-id="c056b-122">The line chart now only displays data points for the Moderation segment.</span></span> 

3. <span data-ttu-id="c056b-123">**การไฮไลต์แบบเชื่อมโยง** รักษาจุดข้อมูลดังเดิมแต่ลดส่วนที่ไม่ใช้กับการเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="c056b-123">**Cross-highlighting** retains all the original data points but dims the portion that does not apply to your selection.</span></span> <span data-ttu-id="c056b-124">การเลือก **การควบคุม** ในแผนภูมิรูปโดนัทไฮไลต์แบบเชื่อมโยงแผนภูมิคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="c056b-124">Selecting **Moderation** in the doughnut chart cross-highlights the column chart.</span></span> <span data-ttu-id="c056b-125">แผนภูมิคอลัมน์ลดข้อมูลทั้งหมดที่ใช้กับเซกเมนต์ความสะดวกและไฮไลต์ข้อมูลทั้งหมดที่ช่วยเซกเมนต์การควบคุม</span><span class="sxs-lookup"><span data-stu-id="c056b-125">The column chart dims all the data that applies to the Convenience segment and highlights all the data that applies to the Moderation segment.</span></span> 


## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="c056b-126">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="c056b-126">Considerations and troubleshooting</span></span>
- <span data-ttu-id="c056b-127">หากรายงานของคุณมีภาพที่สนับสนุน[การดูข้อมูลแบบเจาะลึก](end-user-drill.md)ตามค่าเริ่มต้น การเข้าถึงรายละเอียดของภาพหนึ่งจะไม่มีผลกระทบต่อภาพอื่น ๆ บนหน้ารายงานดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="c056b-127">If your report has a visual that supports [drilling](end-user-drill.md), by default, drilling one visual has no impact on the other visuals on the report page.</span></span> <span data-ttu-id="c056b-128">อย่างไรก็ตาม *ผู้ออกแบบ* รายงาน สามารถเปลี่ยนลักษณะการทำงานนี้ได้ ดังนั้นให้ตรวจสอบภาพที่สามารถเจ้าได้ของคุณเพื่อดูว่า **ตัวกรองภาพที่เจาะได้อื่นๆ** ได้รับการเปิดใช้งานโดย *ผู้ออกแบบ* รายงาน</span><span class="sxs-lookup"><span data-stu-id="c056b-128">However, the report *designer* can change this behavior, so check your drillable visuals to see if **drilling filters other visuals** has been enabled by the report *designer*.</span></span>
    
- <span data-ttu-id="c056b-129">ตัวกรองระดับวิชวลจะถูกเก็บรักษาไว้เมื่อกรองแบบข้ามและไฮไลต์แบบเชื่อมโยงในการแสดงผลอื่นในหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="c056b-129">Visual-level filters are retained when cross-filtering and cross-highlighting other visuals on the report page.</span></span> <span data-ttu-id="c056b-130">ดังนั้นหาก VisualA มีฟิลเตอร์ระดับวิชวลที่ใช้โดยนักออกแบบรายงานหรือโดยคุณ และคุณใช้ visualA เพื่อตอบโต้กับ visualB ฟิลเตอร์ระดับวิชวลจาก visualA จะใช้กับ visualB</span><span class="sxs-lookup"><span data-stu-id="c056b-130">So, If VisualA has visual-level filters applied by the report designer or by you, and you use visualA to interact with visualB, visual-level filters from visualA will be applied to visualB.</span></span>

    ![หน้ารายงานแสดงตัวกรองที่ตั้งไว้แล้ว](media/end-user-interactions/power-bi-visual-filters.png)

## <a name="next-steps"></a><span data-ttu-id="c056b-132">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c056b-132">Next steps</span></span>
[<span data-ttu-id="c056b-133">วิธีการใช้ตัวกรองรายงาน</span><span class="sxs-lookup"><span data-stu-id="c056b-133">How to use report filters</span></span>](../consumer/end-user-report-filter.md)


<span data-ttu-id="c056b-134">[เกี่ยวกับการกรองและไฮไลท์](end-user-report-filter.md)</span><span class="sxs-lookup"><span data-stu-id="c056b-134">[About filtering and highlighting](end-user-report-filter.md).</span></span>
