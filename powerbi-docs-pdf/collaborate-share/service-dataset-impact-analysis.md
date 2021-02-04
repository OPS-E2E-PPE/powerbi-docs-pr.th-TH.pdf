---
title: การวิเคราะห์ผลกระทบของชุดข้อมูล
description: แสดงภาพและวิเคราะห์ผลกระทบต่อเนื่องของการทำการเปลี่ยนแปลงกับชุดข้อมูล
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-eim
ms.topic: how-to
ms.date: 06/15/2020
LocalizationGroup: ''
ms.openlocfilehash: cb68ce937218555292bc8f175510c5e14f4b02f6
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96407227"
---
# <a name="dataset-impact-analysis"></a><span data-ttu-id="8bd16-103">การวิเคราะห์ผลกระทบของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8bd16-103">Dataset impact analysis</span></span>

<span data-ttu-id="8bd16-104">เมื่อคุณทำการเปลี่ยนแปลงชุดข้อมูลหรือกำลังพิจารณาทำการเปลี่ยนแปลง สิ่งสำคัญคือต้องสามารถประเมินผลกระทบที่การเปลี่ยนแปลงเหล่านั้นจะมีในรายงานและแดชบอร์ดที่อยู่ในเวลาที่ขึ้นอยู่กับชุดข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="8bd16-104">When you make changes to a dataset, or are considering making changes, it is important to be able to assess the impact those changes will have on downstream reports and dashboards that depend on that dataset.</span></span> <span data-ttu-id="8bd16-105">**การวิเคราะห์ผลกระทบของชุดข้อมูล** ให้ข้อมูลที่ช่วยให้คุณสามารถทำการประเมินนี้ได้</span><span class="sxs-lookup"><span data-stu-id="8bd16-105">**Dataset impact analysis** provides you with information that can help you make this assessment.</span></span>
* <span data-ttu-id="8bd16-106">การดำเนินการนี้จะแสดงให้เห็นถึงจำนวนพื้นที่ทำงาน รายงาน และแดชบอร์ดของคุณที่อาจได้รับผลกระทบ และมอบการนำทางอย่างง่ายไปยังพื้นที่ทำงานที่มีรายงานและแดชบอร์ดที่ได้รับผลกระทบเพื่อให้คุณสามารถตรวจสอบเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="8bd16-106">It shows you how many workspaces, reports, and dashboards might be affected by your change, and provides easy navigation to the workspaces where the affected reports and dashboards are located so that you can investigate further.</span></span>
* <span data-ttu-id="8bd16-107">การดำเนินการนี้จะแสดงให้คุณเห็นถึงจำนวนผู้เยี่ยมชม และจำนวนการเข้าชมที่มีในรายการที่อาจได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="8bd16-107">It shows you how many unique visitors and the number of views there are on the potentially affected items.</span></span> <span data-ttu-id="8bd16-108">การดำเนินการนี้จะช่วยให้คุณพิจารณาผลกระทบโดยรวมของการเปลี่ยนแปลงสำหรับรายการปลายทาง</span><span class="sxs-lookup"><span data-stu-id="8bd16-108">This helps you determine the overall impact of the change for the downstream item.</span></span> <span data-ttu-id="8bd16-109">ตัวอย่างเช่น อาจเป็นเรื่องสำคัญที่ต้องตรวจสอบผลกระทบจากการเปลี่ยนแปลงในรายงานที่มีผู้ชม 20,000 ราย มากกว่าการตรวจสอบผลกระทบจากการเปลี่ยนแปลงในรายงานที่มีผู้ชมสามราย</span><span class="sxs-lookup"><span data-stu-id="8bd16-109">For instance, it is probably more important to investigate the effect of a change on a report that has 20,000 unique viewers than it is to investigate the effect of the change on a report that has three viewers.</span></span>
* <span data-ttu-id="8bd16-110">โดยถือเป็นวิธีการที่ง่ายดายในการแจ้งให้ผู้คนที่เกี่ยวข้องทราบเกี่ยวกับการเปลี่ยนแปลงที่คุณได้ทำ หรือกำลังคิดว่าจะทำ</span><span class="sxs-lookup"><span data-stu-id="8bd16-110">It provides an easy way of notifying the relevant people about a change you made or are thinking about making.</span></span>

<span data-ttu-id="8bd16-111">การวิเคราะห์ผลกระทบของชุดข้อมูลจะถูกเปิดใช้งานได้อย่างง่ายดายจากภายใน [มุมมองการติดตามการใช้งานข้อมูล](service-data-lineage.md)</span><span class="sxs-lookup"><span data-stu-id="8bd16-111">Dataset impact analysis is easily launched from within [data lineage view](service-data-lineage.md).</span></span>

## <a name="identifying-shared-datasets"></a><span data-ttu-id="8bd16-112">การระบุชุดข้อมูลที่แชร์</span><span class="sxs-lookup"><span data-stu-id="8bd16-112">Identifying shared datasets</span></span>

<span data-ttu-id="8bd16-113">คุณสามารถดำเนินการวิเคราะห์ผลกระทบของชุดข้อมูลได้ทั้งบนชุดข้อมูลที่แชร์และไม่ได้แชร์</span><span class="sxs-lookup"><span data-stu-id="8bd16-113">You can perform dataset impact analysis on both shared and unshared datasets.</span></span> <span data-ttu-id="8bd16-114">อย่างไรก็ตาม จะเป็นประโยชน์อย่างยิ่งสำหรับชุดข้อมูลที่แชร์ในพื้นที่ทำงาน ซึ่งมีความซับซ้อนมากขึ้นเมื่อต้องการรับรูปภาพที่ชัดเจนของการขึ้นต่อกันที่ปลายทาง มากกว่าชุดข้อมูลที่ไม่ได้แชร์ ทั้งนี้ การขึ้นต่อกันทั้งหมดนี้จะตั้งอยู่ในพื้นที่ทำงานเดียวกันกับชุดข้อมูลของตนเอง</span><span class="sxs-lookup"><span data-stu-id="8bd16-114">However, it is particularly useful for datasets which are shared across workspaces, where it is much more complicated to get a clear picture of downstream dependencies than it is with unshared datasets, all of whose dependencies are located in the same workspace as the dataset itself.</span></span>

<span data-ttu-id="8bd16-115">ในมุมมองการติดตามการใช้งาน คุณจะสามารถบอกได้ถึงความแตกต่างระหว่างชุดข้อมูลที่แชร์และไม่ได้แชร์ จากไอคอนที่ปรากฏในมุมบนซ้ายมือของการ์ดของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8bd16-115">In lineage view, you can tell the difference between shared datasets and unshared datasets by the icon that appears in the upper left-hand corner of the dataset's card.</span></span>

![ไอคอนของชุดข้อมูลที่แชร์และไม่ได้แชร์](media/service-dataset-impact-analysis/shared-unshared-icon.png)

## <a name="perform-dataset-impact-analysis"></a><span data-ttu-id="8bd16-117">ดำเนินการวิเคราะห์ผลกระทบของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8bd16-117">Perform dataset impact analysis</span></span>

<span data-ttu-id="8bd16-118">คุณสามารถดำเนินการวิเคราะห์ผลกระทบเกี่ยวกับชุดข้อมูลใด ๆ ในพื้นที่ทำงาน ไม่ว่าจะมีการแชร์หรือไม่ก็ตาม</span><span class="sxs-lookup"><span data-stu-id="8bd16-118">You can perform impact analysis on any dataset in the workspace, whether it is shared or not.</span></span> <span data-ttu-id="8bd16-119">คุณไม่สามารถดำเนินการวิเคราะห์ผลกระทบบนชุดข้อมูลภายนอกที่แสดงในมุมมองการติดตามการใช้งาน แต่ในความเป็นจริง ตั้งอยู่ในพื้นที่ทำงานอื่น</span><span class="sxs-lookup"><span data-stu-id="8bd16-119">You cannot perform impact analysis on external datasets that are displayed in lineage view but are in fact located in another workspace.</span></span> <span data-ttu-id="8bd16-120">เมื่อต้องการทำการวิเคราะห์ผลกระทบบนชุดข้อมูลภายนอก คุณต้องนำทางไปยังพื้นที่ทำงานต้นทาง</span><span class="sxs-lookup"><span data-stu-id="8bd16-120">To perform impact analysis on an external dataset, you need to navigate to the source workspace.</span></span>

<span data-ttu-id="8bd16-121">เมื่อต้องการทำการวิเคราะห์ผลกระทบของชุดข้อมูล ให้คลิกที่ปุ่มการวิเคราะห์ผลกระทบบนการ์ดชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8bd16-121">To perform dataset impact analysis, click the impact analysis button on the dataset card.</span></span>

![ปุ่มการวิเคราะห์ผลกระทบของชุดข้อมูล](media/service-dataset-impact-analysis/open-analysis-pane-button.png)

<span data-ttu-id="8bd16-123">บานหน้าต่างข้างการวิเคราะห์ผลกระทบจะเปิดออก</span><span class="sxs-lookup"><span data-stu-id="8bd16-123">The impact analysis side panel opens.</span></span>

![แผงด้านข้างการวิเคราะห์ผลกระทบของชุดข้อมูล](media/service-dataset-impact-analysis/service-impact-analysis-pane.png)

* <span data-ttu-id="8bd16-125">**สรุปผลกระทบ** แสดงจำนวนพื้นที่ทำงาน รายงาน และแดชบอร์ดที่อาจได้รับผลกระทบ รวมถึงจำนวนมุมมองทั้งหมดสำหรับรายงานปลายทางและแดชบอร์ดทั้งหมดที่เชื่อมต่อกับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8bd16-125">The **impact summary** shows you the number of potentially impacted workspaces, reports, and dashboards, as well as the total number of views for all the downstream reports and dashboards that are connected to the dataset.</span></span>
* <span data-ttu-id="8bd16-126">ลิงก์ **แจ้งบุคคลผู้ติดต่อ** จะเปิดกล่องโต้ตอบที่คุณสามารถสร้างและส่งข้อความเกี่ยวกับการเปลี่ยนแปลงชุดข้อมูลใด ๆ ที่คุณทำต่อรายชื่อติดต่อของพื้นที่ทำงานที่ได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="8bd16-126">The **notify contacts** link opens a dialog where you can create and send a message about any dataset changes you make to the contact lists of the affected workspaces.</span></span> 
* <span data-ttu-id="8bd16-127">**การแจกแจงการใช้งาน** ที่แสดงให้คุณเห็นถึงพื้นที่ทำงานแต่ละรายการ จำนวนมุมมองทั้งหมดสำหรับรายงานและแดชบอร์ดที่อาจได้รับผลกระทบ และสำหรับรายงานและแดชบอร์ดแต่ละรายการ จำนวนผู้ชุมทั้งหมดและมุมมองที่</span><span class="sxs-lookup"><span data-stu-id="8bd16-127">The **usage breakdown** that shows you, for each workspace, the total number of views for the potentially impacted reports and dashboards it contains, and for each report and dashboard, the total number of viewers and views, where</span></span>
   * <span data-ttu-id="8bd16-128">ผู้ชม: จำนวนผู้ใช้ที่ไม่ซ้ำกันที่ดูรายงานหรือมุมมองหนึ่งๆ</span><span class="sxs-lookup"><span data-stu-id="8bd16-128">Viewers: The number of distinct users that viewed a report or dashboard.</span></span>
   * <span data-ttu-id="8bd16-129">มุมมอง: จำนวนมุมมองสำหรับรายงานหรือแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="8bd16-129">Views: The number of views for a report or dashboard</span></span>

<span data-ttu-id="8bd16-130">เมตริกการใช้งานจะสัมพันธ์กับ 30 วันล่าสุด โดยไม่นับรวมวันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="8bd16-130">The usage metrics relate to the last 30 days, excluding the current day.</span></span> <span data-ttu-id="8bd16-131">จำนวนจะหมายรวมถึงการใช้งานผ่านแอปต่าง ๆ ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8bd16-131">The count includes usage coming via related apps.</span></span> <span data-ttu-id="8bd16-132">เมตริกจะช่วยให้คุณเข้าใจการใช้งานชุดข้อมูลในทุกผู้เช่า รวมถึงประเมินผลกระทบที่อาจเกิดจากการเปลี่ยนแปลงของชุดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="8bd16-132">The metrics help you understand dataset use across the tenant, as well as assess the impact any changes to your dataset may have.</span></span>

## <a name="notify-contacts"></a><span data-ttu-id="8bd16-133">แจ้งบุคคลติดต่อ</span><span class="sxs-lookup"><span data-stu-id="8bd16-133">Notify contacts</span></span>

<span data-ttu-id="8bd16-134">หากคุณทำการเปลี่ยนแปลงกับชุดข้อมูล หรือกำลังคิดที่จะทำการเปลี่ยนแปลง คุณอาจต้องการติดต่อผู้ใช้ที่เกี่ยวข้อง เพื่อแจ้งให้พวกเขาทราบ</span><span class="sxs-lookup"><span data-stu-id="8bd16-134">If you've made a change to a dataset or are thinking about making a change, you might want to contact the relevant users to tell them about it.</span></span> <span data-ttu-id="8bd16-135">เมื่อคุณแจ้งบุคคลติดต่อ ระบบจะส่งอีเมลไปยัง [รายชื่อบุคคลติดต่อ](../collaborate-share/service-create-the-new-workspaces.md#create-a-contact-list) ของพื้นที่ทำงานทั้งหมดที่ได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="8bd16-135">When you notify contacts, an email is sent to the [contact lists](../collaborate-share/service-create-the-new-workspaces.md#create-a-contact-list) of all the impacted workspaces.</span></span> <span data-ttu-id="8bd16-136">ชื่อของคุณจะปรากฏบนอีเมล ดังนั้น บุคคลติดต่อจะสามารถค้นหาคุณได้และตอบกลับในเธรดอีเมลใหม่</span><span class="sxs-lookup"><span data-stu-id="8bd16-136">Your name appears on the email so the contacts can find you and reply back in a new email thread.</span></span> 

1. <span data-ttu-id="8bd16-137">คลิก **แจ้งบุคคลติดต่อ** ในบานหน้าต่างด้านข่างการวิเคราะห์ผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="8bd16-137">Click **Notify contacts** in the impact analysis side pane.</span></span> <span data-ttu-id="8bd16-138">กล่องโต้ตอบแจ้งบุคคลติดต่อจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="8bd16-138">The notify contacts dialog will appear.</span></span>

   ![กล่องโต้ตอบแจ้งบุคคลติดต่อ](media/service-dataset-impact-analysis/notify-contacts-dialog.png)

1. <span data-ttu-id="8bd16-140">ในกล่องข้อความ ให้ระบุรายละเอียดบางอย่างเกี่ยวกับการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="8bd16-140">In the text box, provide some detail about the change.</span></span>
1. <span data-ttu-id="8bd16-141">เมื่อข้อความพร้อม ให้คลิก **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="8bd16-141">When the message is ready, click **Send**.</span></span>

> [!NOTE]
> <span data-ttu-id="8bd16-142">แจ้งบุคคลติดต่อจะไม่สามารถใช้งานได้ หากชุดข้อมูลที่คุณกำลังทำการวิเคราะห์ผลกระทบอยู่ในพื้นที่ทำงานแบบคลาสสิก</span><span class="sxs-lookup"><span data-stu-id="8bd16-142">Notify contacts is not available if the dataset you are performing impact analysis on is located in a classic workspace.</span></span>

## <a name="privacy"></a><span data-ttu-id="8bd16-143">ความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="8bd16-143">Privacy</span></span>

<span data-ttu-id="8bd16-144">เพื่อดำเนินการวิเคราะห์ผลกระทบในชุดข้อมูล คุณจำเป็นต้องเขียนสิทธิ์ให้ชุดข้อมูลดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="8bd16-144">In order to perform impact analysis on a dataset, you must have write permissions to it.</span></span> <span data-ttu-id="8bd16-145">ในบานหน้าต่างด้านข้างการวิเคราะห์ผลกระทบ คุณจะเห็นเฉพาะชื่อจริงสำหรับพื้นที่ทำงาน รายงาน และแดชบอร์ดที่คุณสามารถเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="8bd16-145">In the impact analysis side pane, you only see real names for workspaces, reports, and dashboards that you have access to.</span></span> <span data-ttu-id="8bd16-146">หน่วยข้อมูลที่คุณไม่สามารถเข้าถึงได้ จะแสดงแบบ **การเข้าถึงแบบจำกัด**</span><span class="sxs-lookup"><span data-stu-id="8bd16-146">Items that you don't have access to are listed as **Limited access**.</span></span> <span data-ttu-id="8bd16-147">เนื่องจากชื่อหน่วยข้อมูลบางรายการอาจมีข้อมูลส่วนบุคคลอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="8bd16-147">This is because some item names may contain personal information.</span></span>

<span data-ttu-id="8bd16-148">แม้ว่าคุณจะไม่สามารถเข้าถึงพื้นที่ทำงานบางอย่างได้ แต่คุณจะยังคงมองเห็นเมตริกการใช้งานสรุปสำหรับพื้นที่ทำงานดังกล่าว และข้อความแจ้งบุคคลติดต่อของคุณจะเข้าถึงรายชื่อบุคคลติดต่อของพื้นที่ทำงานดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="8bd16-148">Even if you don't have access to some workspaces, you will still see summarized usage metrics for those workspaces, and your notify contacts messages will reach the contact lists of those workspaces.</span></span>

## <a name="impact-analysis-from-power-bi-desktop"></a><span data-ttu-id="8bd16-149">การวิเคราะห์ผลกระทบจาก Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="8bd16-149">Impact analysis from Power BI Desktop</span></span>

<span data-ttu-id="8bd16-150">เมื่อคุณทำการเปลี่ยนแปลงกับชุดข้อมูลใน Power BI Desktop แล้วเผยแพร่อีกครั้งไปยังบริการ Power BI ข้อความจะแสดงจำนวนพื้นที่ทำงาน รายงาน และแดชบอร์ดที่อาจได้รับผลกระทบจากการเปลี่ยนแปลงนั้น และขอให้คุณยืนยันว่า คุณต้องการแทนที่ชุดข้อมูลที่เผยแพร่ในปัจจุบันด้วยรายการที่คุณปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="8bd16-150">When you make a change to a dataset in Power BI Desktop and then republish it to the Power BI service, a message shows you how many workspaces, reports, and dashboards are potentially impacted by the change, and asks you to confirm that you want to replace the currently published dataset with the one you modified.</span></span> <span data-ttu-id="8bd16-151">นอกจากนี้ ข้อความยังประกอบด้วยลิงก์ไปยังการวิเคราะห์ผลกระทบของชุดข้อมูลแบบเต็มรูปแบบในบริการ Power BI ที่คุณจะสามารถมองเห็นข้อมูลเพิ่มเติม และดำเนินการเพื่อบรรเทาความเสี่ยงจากการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="8bd16-151">The message also provides a link to the full dataset impact analysis in the Power BI service, where you can see more information and take action to mitigate the risks of your change.</span></span>

![ข้อความเกี่ยวกับการวิเคราะห์ผลกระทบของชุดข้อมูลใน Power BI Desktop](media/service-dataset-impact-analysis/service-dataset-impact-analysis-desktop-warning.png)

> [!NOTE]
> <span data-ttu-id="8bd16-153">ข้อมูลที่แสดงในข้อความจะระบุถึงผลกระทบที่อาจเกิดขึ้น โดยไม่จำเป็นต้องระบุว่ามีสิ่งใดเสียหายบ้าง</span><span class="sxs-lookup"><span data-stu-id="8bd16-153">The information shown in the message only indicates potential impact - it does not necessarily indicate that anything has broken.</span></span> <span data-ttu-id="8bd16-154">ในบางครั้ง การเปลี่ยนแปลงของชุดข้อมูลจะไม่ส่งผลเสียต่อแดชบอร์ดและรายงานปลายทาง แต่คุณจะได้รับข้อความนี้ทีมอบความชัดเจนให้แก่คุณเกี่ยวกับผลกระทบที่อาจเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="8bd16-154">Oftentimes dataset changes have no adverse effect on their downstream reports and dashboards - still, you'll get this message that gives you clarity concerning potential impact.</span></span>
>
><span data-ttu-id="8bd16-155">ในข้อความดังกล่าว จำนวนพื้นที่ทำงานจะปรากฏก็ต่อเมื่อมีพื้นที่ทำงานมากกว่าหนึ่งรายการที่มีแดชบอร์ดและรายงานที่ได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="8bd16-155">In the message, the number of workspaces is only shown if more than one workspace contains impacted reports and dashboards.</span></span>

## <a name="limitations"></a><span data-ttu-id="8bd16-156">ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="8bd16-156">Limitations</span></span>

* <span data-ttu-id="8bd16-157">ขณะนี้ เมตริกการใช้งานจะไม่ได้รับการสนับสนุนสำหรับพื้นที่ทำงานส่วนบุคคลและแบบคลาสสิก</span><span class="sxs-lookup"><span data-stu-id="8bd16-157">Usage metrics are currently not supported for classic and personal workspaces.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8bd16-158">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="8bd16-158">Next steps</span></span>

* [<span data-ttu-id="8bd16-159">บทนำชุดข้อมูลทั้งพื้นที่ทำงาน (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="8bd16-159">Intro to datasets across workspaces (preview)</span></span>](../connect-data/service-datasets-across-workspaces.md)
* [<span data-ttu-id="8bd16-160">สายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8bd16-160">Data lineage</span></span>](service-data-lineage.md)

