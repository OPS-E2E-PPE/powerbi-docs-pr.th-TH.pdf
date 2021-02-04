---
title: การติดตามการใช้งานข้อมูล
description: ในโครงการระบบธุรกิจอัจฉริยะที่ทันสมัย (BI) การทำความเข้าใจการไหลของข้อมูลจากแหล่งข้อมูลไปยังจุดหมายปลายทางเป็นความท้าทายที่สำคัญสำหรับลูกค้าหลายราย
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-eim
ms.topic: how-to
ms.date: 06/15/2020
LocalizationGroup: ''
ms.openlocfilehash: 8b119f5134fdaf4e251f9a8da560a2a3f7f3a4eb
ms.sourcegitcommit: 46cf62d9bb33ac7b7eae7910fbba6756f626c65f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/15/2020
ms.locfileid: "97492115"
---
# <a name="data-lineage"></a><span data-ttu-id="13e20-103">การติดตามการใช้งานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="13e20-103">Data lineage</span></span>
<span data-ttu-id="13e20-104">ในโครงการระบบธุรกิจอัจฉริยะที่ทันสมัย (BI) การทำความเข้าใจการไหลของข้อมูลจากแหล่งข้อมูลไปยังจุดหมายปลายทางเป็นความท้าทาย</span><span class="sxs-lookup"><span data-stu-id="13e20-104">In modern business intelligence (BI) projects, understanding the flow of data from the data source to its destination can be a challenge.</span></span> <span data-ttu-id="13e20-105">ความท้าทายจะยิ่งเพิ่มมากขึ้นหากคุณสร้างโครงการวิเคราะห์ขั้นสูงซึ่งครอบคุลมแหล่งข้อมูล สิ่งประดิษฐ์ และการอ้างอิงจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="13e20-105">The challenge is even bigger if you have built advanced analytical projects spanning multiple data sources, artifacts, and dependencies.</span></span> <span data-ttu-id="13e20-106">คำถามเช่น "จะเกิดอะไรขึ้นหากฉันเปลี่ยนแปลงข้อมูลนี้"</span><span class="sxs-lookup"><span data-stu-id="13e20-106">Questions like "What happens if I change this data?"</span></span> <span data-ttu-id="13e20-107">หรือ "เพราะเหตุใดรายงานนี้จึงไม่มีข้อมูลล่าสุด"</span><span class="sxs-lookup"><span data-stu-id="13e20-107">or "Why isn't this report up to date?"</span></span> <span data-ttu-id="13e20-108">เป็นคำถามที่ตอบยาก</span><span class="sxs-lookup"><span data-stu-id="13e20-108">can be hard to answer.</span></span> <span data-ttu-id="13e20-109">จึงอาจจำเป็นต้องมีทีมผู้เชี่ยวชาญหรือการตรวจสอบอย่างลึกซึ้งเพื่อทำความเข้าใจ</span><span class="sxs-lookup"><span data-stu-id="13e20-109">They may require a team of experts or deep investigation to understand.</span></span> <span data-ttu-id="13e20-110">เราออกแบบมุมมองสายข้อมูลเพื่อช่วยเหลือคุณในการตอบคำถามเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="13e20-110">We designed a data lineage view to help you answer these questions.</span></span>

![มุมมองสายข้อมูล Power BI](media/service-data-lineage/service-data-lineage-view.png)
 
<span data-ttu-id="13e20-112">Power BI มีสิ่งประดิษฐ์หลายชนิด เช่น แดชบอร์ด รายงาน ชุดข้อมูล และกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="13e20-112">Power BI has several artifact types, such as dashboards, reports, datasets, and dataflows.</span></span> <span data-ttu-id="13e20-113">ชุดข้อมูลและกระแสข้อมูลจำนวนมากเชื่อมต่อกับแหล่งข้อมูลภายนอก เช่น SQL Server และยังเชื่อมต่อกับชุดข้อมูลภายนอกในพื้นที่ทำงานอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="13e20-113">Many datasets and dataflows connect to external data sources such as SQL Server, and to external datasets in other workspaces.</span></span> <span data-ttu-id="13e20-114">เมื่อชุดข้อมูลอยู่ภายนอกพื้นที่ทำงานที่คุณเป็นเจ้าของ ชุดข้อมูลนั้นอาจอยู่ในพื้นที่ทำงานที่บุคคลในฝ่ายไอทีหรือนักวิเคราะห์รายอื่นเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="13e20-114">When a dataset is external to a workspace you own, it may be in a workspace owned by someone in IT or another analyst.</span></span> <span data-ttu-id="13e20-115">ในท้ายที่สุด แหล่งข้อมูลภายนอกและชุดข้อมูลนั้นทำให้การค้นหาว่าข้อมูลมาจากที่ใดเป็นเรื่องยากขึ้น</span><span class="sxs-lookup"><span data-stu-id="13e20-115">External data sources and datasets make it harder to know where the data is coming from, ultimately.</span></span> <span data-ttu-id="13e20-116">สำหรับโครงการที่มีความซับซ้อนและโครงการที่เรียบง่ายกว่า เราขอแนะนำมุมมองสายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="13e20-116">For complex projects and for simpler ones, we introduce lineage view.</span></span>

<span data-ttu-id="13e20-117">ในมุมมองสายข้อมูล คุณจะเห็นความสัมพันธ์ของสายการเชื่อมโยงระหว่างสิ่งประดิษฐ์ทั้งหมดในพื้นที่ทำงาน และการอ้างอิงภายนอกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="13e20-117">In lineage view, you see the lineage relationships between all the artifacts in a workspace, and all its external dependencies.</span></span> <span data-ttu-id="13e20-118">ซึ่งแสดงการเชื่อมต่อระหว่างสิ่งประดิษฐ์ในพื้นที่ทำงานทั้งหมด รวมถึงการเชื่อมต่อไปยังกระแสข้อมูล ทั้งต้นทางและปลายทาง</span><span class="sxs-lookup"><span data-stu-id="13e20-118">It shows connections between all workspace artifacts, including connections to dataflows, both upstream and downstream.</span></span>    

<iframe width="560" height="315" src="https://www.youtube.com/embed/rUj06dqB98g" frameborder="0" allowfullscreen></iframe>

## <a name="explore-lineage-view"></a><span data-ttu-id="13e20-119">ดูมุมมองสายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="13e20-119">Explore lineage view</span></span>

<span data-ttu-id="13e20-120">พื้นที่ทำงานทั้งหมด ไม่ว่าจะเป็นแบบใหม่หรือแบบดั้งเดิม ก็จะมีมุมมองสายข้อมูลโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="13e20-120">Every workspace, whether new or classic, automatically has a lineage view.</span></span> <span data-ttu-id="13e20-121">อย่างน้อยคุณต้องมีบทบาทผู้สนับสนุนในพื้นที่ทำงานเพื่อดูมุมมองดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="13e20-121">You need at least a Contributor role in the workspace to view it.</span></span> <span data-ttu-id="13e20-122">ดูรายละเอียดที่หัวข้อ [สิทธิ์](#permissions) ในบทความนี้</span><span class="sxs-lookup"><span data-stu-id="13e20-122">See [Permissions](#permissions) in this article for details.</span></span>

* <span data-ttu-id="13e20-123">หากต้องการเข้าถึงมุมมองสายข้อมูล ให้ไปที่มุมมองรายการพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="13e20-123">To access lineage view, go to the workspace list view.</span></span> <span data-ttu-id="13e20-124">แตะลูกศรที่อยู่ถัดจาก **มุมมองรายการ** และเลือก **มุมมองสายข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="13e20-124">Tap the arrow next to **List view** and select **Lineage view**.</span></span>

   ![สลับไปยังมุมมองสายข้อมูล](media/service-data-lineage/service-data-lineage-view-select.png)

<span data-ttu-id="13e20-126">ในมุมมองนี้ คุณจะเห็นสิ่งประดิษฐ์ในพื้นที่ทำงานทั้งหมดและวิธีการที่ข้อมูลส่งจากจุดหนึ่งไปยังอีกจุดหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="13e20-126">In this view, you see all the workspace artifacts and how the data flows from one artifact to another.</span></span>

<span data-ttu-id="13e20-127">**แหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="13e20-127">**Data sources**</span></span>

<span data-ttu-id="13e20-128">คุณจะเห็นแหล่งข้อมูลจากชุดข้อมูลและกระแสข้อมูลที่ได้รับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="13e20-128">You see the data sources from which the datasets and dataflows get their data.</span></span> <span data-ttu-id="13e20-129">บนการ์ดแหล่งข้อมูล คุณจะเห็นข้อมูลเพิ่มเติมที่สามารถช่วยระบุแหล่งที่มาได้</span><span class="sxs-lookup"><span data-stu-id="13e20-129">On the data source cards, you see more information that can help identify the source.</span></span> <span data-ttu-id="13e20-130">ตัวอย่างเช่น สำหรับเซิร์ฟเวอร์ Azure SQL คุณจะเห็นชื่อฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="13e20-130">For example, for Azure SQL server you also see the database name.</span></span>

![แหล่งข้อมูลมุมมองสายข้อมูลที่ไม่มีเกตเวย์](media/service-data-lineage/service-data-lineage-data-source-card.png)
 
<span data-ttu-id="13e20-132">**เกตเวย์**</span><span class="sxs-lookup"><span data-stu-id="13e20-132">**Gateways**</span></span>

<span data-ttu-id="13e20-133">หากมีการเชื่อมต่อแหล่งข้อมูลผ่านเกตเวย์ภายในองค์กร ระบบจะเพิ่มข้อมูลเกตเวย์ไปยังการ์ดแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="13e20-133">If a data source is connected via an on-premises gateway, the gateway information is added to the data source card.</span></span> <span data-ttu-id="13e20-134">หากคุณมีสิทธิ์ในฐานะผู้ดูแลระบบเกตเวย์หรือเป็นผู้ใช้แหล่งข้อมูล คุณจะเห็นข้อมูลเพิ่มเติม เช่น ชื่อเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="13e20-134">If you have permissions, either as a gateway admin or as a data source user, you see more information, such as the gateway name.</span></span>

![แหล่งข้อมูลมุมมองสายข้อมูลที่มีเกตเวย์](media/service-data-lineage/service-data-lineage-data-gateway-card.png)

<span data-ttu-id="13e20-136">**ชุดข้อมูลและกระแสข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="13e20-136">**Datasets and dataflows**</span></span>
 
<span data-ttu-id="13e20-137">บนชุดข้อมูลและกระแสข้อมูล คุณจะเห็นเวลารีเฟรชครั้งล่าสุด เช่นเดียวกับถ้าชุดข้อมูลหรือกระแสข้อมูล ได้รับการรับรองหรือเลื่อนขั้น</span><span class="sxs-lookup"><span data-stu-id="13e20-137">On datasets and dataflows, you see the last refresh time, as well as if the dataset or dataflow is certified or promoted.</span></span>

![ชุดข้อมูลที่ได้รับการโปรโมทและได้รับการรองรับในมุมมองสายข้อมูล](media/service-data-lineage/service-data-lineage-promoted-certified.png)
 
<span data-ttu-id="13e20-139">หากรายงานในพื้นที่ทำงานถูกสร้างขึ้นบนชุดข้อมูลหรือกระแสข้อมูลในพื้นที่ทำงานอื่น คุณจะเห็นชื่อพื้นที่ทำงานต้นทางบนการ์ดของชุดข้อมูลและกระแสข้อมูลนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="13e20-139">If a report in the workspace is built on a dataset or a dataflow that is located in another workspace, you see the source workspace name on the card of that dataset or dataflow.</span></span> <span data-ttu-id="13e20-140">เลือกชื่อพื้นที่ทำงานต้นทางเพื่อไปยังพื้นที่ทำงานนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="13e20-140">Select the name of the source workspace to go to that workspace.</span></span>

* <span data-ttu-id="13e20-141">สำหรับสิ่งประดิษฐ์ใดๆ ก็ตาม ให้เลือก **ตัวเลือกเพิ่มเติม** (... ) เพื่อดูเมนูตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="13e20-141">For any artifact, select **More options (...)** to view the options menu.</span></span> <span data-ttu-id="13e20-142">ซึ่งมีการดำเนินการเหมือนกันทั้งหมดที่สามารถใช้งานได้ในมุมมองรายการ</span><span class="sxs-lookup"><span data-stu-id="13e20-142">It features all the same actions that are available in list view.</span></span>

<span data-ttu-id="13e20-143">หากต้องการดูเมตาดาต้าเพิ่มเติมเกี่ยวกับสิ่งสิ่งประดิษฐ์ใดๆ ให้เลือกการ์ดสิ่งประดิษฐ์</span><span class="sxs-lookup"><span data-stu-id="13e20-143">To see more metadata on any artifact, select the artifact card itself.</span></span> <span data-ttu-id="13e20-144">ข้อมูลเพิ่มเติมเกี่ยวกับชุดข้อมูลจะแสดงในบานหน้าต่างด้านข้าง</span><span class="sxs-lookup"><span data-stu-id="13e20-144">Additional information about the artifact is displayed in a side pane.</span></span> <span data-ttu-id="13e20-145">ในภาพด้านล่าง บานหน้าต่างด้านข้างจะแสดงเมตาดาต้าของชุดข้อมูลที่เลือก</span><span class="sxs-lookup"><span data-stu-id="13e20-145">In the image below, the side pane displays the metadata of a selected dataset.</span></span>

![บานหน้าต่างด้านข้างที่มีข้อมูลเพิ่มเติม](media/service-data-lineage/service-data-lineage-side-pane.png)
 
## <a name="show-lineage-for-any-artifact"></a><span data-ttu-id="13e20-147">แสดงสายข้อมูลสำหรับสิ่งประดิษฐ์ใด ๆ</span><span class="sxs-lookup"><span data-stu-id="13e20-147">Show lineage for any artifact</span></span> 

<span data-ttu-id="13e20-148">สมมติว่าคุณต้องการดูสายข้อมูลสำหรับสิ่งประดิษฐ์เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="13e20-148">Say you want to see the lineage for a specific artifact.</span></span>

* <span data-ttu-id="13e20-149">ให้เลือกลูกศรคู่ซึ่งอยู่ที่ด้านล่างของสิ่งประดิษฐ์</span><span class="sxs-lookup"><span data-stu-id="13e20-149">Select the double arrows under the artifact.</span></span>

   ![ไฮไลท์สายข้อมูลสำหรับสิ่งประดิษฐ์เฉพาะ](media/service-data-lineage/service-data-lineage-specific-artifact.png)

   <span data-ttu-id="13e20-151">Power BI ไฮไลท์สิ่งประดิษฐ์ทั้งหมดที่เกี่ยวข้องกับสิ่งประดิษฐ์นั้น และลดความสว่างของส่วนที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="13e20-151">Power BI highlights all the artifacts related to that artifact, and dims the rest.</span></span> 

## <a name="navigation-and-full-screen"></a><span data-ttu-id="13e20-152">การนำทางและการแสดงผลเต็มหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="13e20-152">Navigation and full screen</span></span> 

<span data-ttu-id="13e20-153">มุมมองสายข้อมูลเป็นพื้นที่ทำงานแบบโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="13e20-153">Lineage view is an interactive canvas.</span></span> <span data-ttu-id="13e20-154">คุณสามารถใช้เมาส์และทัชแพดเพื่อนำทางในพื้นที่ทำงาน และย่อหรือขยาย</span><span class="sxs-lookup"><span data-stu-id="13e20-154">You can use the mouse and touchpad to navigate in the canvas, as well as to zoom in or out.</span></span>

* <span data-ttu-id="13e20-155">เมื่อต้องการย่อและขยาย ให้ใช้เมนูที่มุมขวาล่าง หรือใช้เมาส์หรือทัชแพดของคุณ</span><span class="sxs-lookup"><span data-stu-id="13e20-155">To zoom in and out, use either the menu in the bottom-right corner or your mouse or touchpad.</span></span>
* <span data-ttu-id="13e20-156">หากต้องการเพิ่มพื้นที่ให้มากขึ้นสำหรับกราฟ ให้ใช้ตัวเลือกการแสดงผลเต็มหน้าจอที่มุมขวาล่าง</span><span class="sxs-lookup"><span data-stu-id="13e20-156">To have more room for the graph itself, use the full screen option at the bottom-right corner.</span></span> 

    ![ย่อหรือขยาย หรือเต็มหน้าจอ](media/service-data-lineage/service-data-lineage-zoom.png)

## <a name="permissions"></a><span data-ttu-id="13e20-158">สิทธิ์</span><span class="sxs-lookup"><span data-stu-id="13e20-158">Permissions</span></span>

* <span data-ttu-id="13e20-159">คุณต้องมีสิทธิ์การใช้งาน Power BI Pro เพื่อดูมุมมองสายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="13e20-159">You need a Power BI Pro license to see lineage view.</span></span>
* <span data-ttu-id="13e20-160">มุมมองสายข้อมูลพร้อมใช้งานสำหรับผู้ใช้ที่มีสิทธิ์ในการเข้าถึงพื้นที่ทำงานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="13e20-160">Lineage view is available only to users with access to the workspace.</span></span>
* <span data-ttu-id="13e20-161">ผู้ใช้ต้องมีบทบาทผู้ดูแลระบบ สมาชิก หรือบทบาทผู้สนับสนุนในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="13e20-161">Users must have an Admin, Member, or Contributor role in the workspace.</span></span> <span data-ttu-id="13e20-162">ผู้ใช้ที่มีบทบาทผู้ชมไม่สามารถสลับไปยังมุมมองสายข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="13e20-162">Users with a Viewer role can't switch to lineage view.</span></span>


## <a name="considerations-and-limitations"></a><span data-ttu-id="13e20-163">ข้อควรพิจารณาและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="13e20-163">Considerations and limitations</span></span>

- <span data-ttu-id="13e20-164">มุมมองสายข้อมูลไม่สามารถใช้งานได้บน Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="13e20-164">Lineage view isn't available on Internet Explorer.</span></span> <span data-ttu-id="13e20-165">ดูรายละเอียดที่ [เบราว์เซอร์ที่สนับสนุนสำหรับ Power BI](../fundamentals/power-bi-browsers.md)</span><span class="sxs-lookup"><span data-stu-id="13e20-165">See [Supported browsers for Power BI](../fundamentals/power-bi-browsers.md) for details.</span></span>

## <a name="next-steps"></a><span data-ttu-id="13e20-166">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="13e20-166">Next steps</span></span>

* [<span data-ttu-id="13e20-167">บทนำชุดข้อมูลทั้งพื้นที่ทำงาน (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="13e20-167">Intro to datasets across workspaces (preview)</span></span>](../connect-data/service-datasets-across-workspaces.md)
* [<span data-ttu-id="13e20-168">การวิเคราะห์ผลกระทบของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="13e20-168">Dataset impact analysis</span></span>](service-dataset-impact-analysis.md)
