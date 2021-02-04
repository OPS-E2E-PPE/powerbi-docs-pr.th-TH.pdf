---
title: การวิเคราะห์ผลกระทบของแหล่งข้อมูล
description: ทำความเข้าใจตำแหน่งที่มีการใช้แหล่งข้อมูลของคุณ
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-eim
ms.topic: how-to
ms.date: 07/20/2020
LocalizationGroup: ''
ms.openlocfilehash: 8c8a2a701415d9e937c5b592c915e51a4921840b
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411896"
---
# <a name="data-source-impact-analysis"></a><span data-ttu-id="8a25a-103">การวิเคราะห์ผลกระทบของแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a25a-103">Data source impact analysis</span></span>

<span data-ttu-id="8a25a-104">การวิเคราะห์ผลกระทบของแหล่งข้อมูลช่วยให้คุณเห็นตำแหน่งที่มีการใช้แหล่งข้อมูลของคุณจากทั่วทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="8a25a-104">Data source impact analysis helps you see where your data source is being used throughout your organization.</span></span> <span data-ttu-id="8a25a-105">ซึ่งจะเป็นประโยชน์เมื่อมีการใช้แหล่งข้อมูลแบบออฟไลน์ชั่วคราวหรือถาวร และคุณต้องการทราบเกี่ยวกับบุคคลที่ได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="8a25a-105">This can be useful when the data source is temporarily or permanently taken offline, and you want to get an idea about who is impacted.</span></span> <span data-ttu-id="8a25a-106">การดำเนินการนี้จะแสดงให้เห็นถึงจำนวนพื้นที่ทำงาน กระแสข้อมูล และชุดข้อมูลที่ใช้แหล่งข้อมูล และมอบการนำทางที่ง่ายดายไปยังพื้นที่ทำงานที่มีกระแสข้อมูลและชุดข้อมูลที่ได้รับผลกระทบเพื่อให้คุณสามารถตรวจสอบเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="8a25a-106">It shows you how many workspaces, dataflows, and datasets use the data source, and provides easy navigation to the workspaces where the affected dataflows and datasets are located so that you can investigate further.</span></span>

<span data-ttu-id="8a25a-107">การวิเคราะห์ผลกระทบของแหล่งข้อมูลยังช่วยให้คุณสามารถระบุการสร้างข้อมูลซ้ำในผู้เช่าได้ เช่น เมื่อผู้ใช้หลายรายสร้างแบบจำลองที่คล้ายคลึงกันที่ด้านบนของแหล่งข้อมูลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="8a25a-107">Data source impact analysis can also help you spot data duplication in the tenant, such as when a number of different users build similar models on top of the same data source.</span></span> <span data-ttu-id="8a25a-108">การวิเคราะห์ผลกระทบของแหล่งข้อมูลสนับสนุนเป้าหมายในการมี “แหล่งความจริงหนึ่งเดียว” ด้วยการช่วยให้คุณค้นพบชุดข้อมูลและกระแสข้อมูลที่ซ้ำซ้อนดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="8a25a-108">By helping you discover such redundant datasets and dataflows, data source impact analysis supports the goal of having "a single source of truth".</span></span>

## <a name="perform-data-source-impact-analysis"></a><span data-ttu-id="8a25a-109">ดำเนินการวิเคราะห์ผลกระทบของแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a25a-109">Perform data source impact analysis</span></span>

<span data-ttu-id="8a25a-110">วิธีดำเนินการวิเคราะห์ผลกระทบของแหล่งข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="8a25a-110">To perform data source impact analysis:</span></span>

1. <span data-ttu-id="8a25a-111">ไปยังพื้นที่ทำงานที่มีแหล่งข้อมูลที่คุณสนใจ และเปิด[มุมมองสายข้อมูล](service-data-lineage.md)</span><span class="sxs-lookup"><span data-stu-id="8a25a-111">Go to the workspace that contains the data source you're interested in and open [lineage view](service-data-lineage.md).</span></span>
1. <span data-ttu-id="8a25a-112">ค้นหาการ์ดของแหล่งข้อมูล และคลิกที่ไอคอนการวิเคราะห์ผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="8a25a-112">Find the data source's card and click the impact analysis icon.</span></span>

    ![ภาพหน้าจอของการ์ดแหล่งข้อมูลที่แสดงปุ่มการวิเคราะห์ผลกระทบ](media/service-data-source-impact-analysis/data-source-impact-analysis-button.png)
 
<span data-ttu-id="8a25a-114">บานหน้าต่างข้างการวิเคราะห์ผลกระทบจะเปิดออก</span><span class="sxs-lookup"><span data-stu-id="8a25a-114">The impact analysis side panel opens.</span></span>

![ภาพหน้าจอของบานหน้าต่างด้านข้างการวิเคราะห์ผลกระทบของแหล่งข้อมูล](media/service-data-source-impact-analysis/data-source-impact-analyis-side-pane.png)
 
* <span data-ttu-id="8a25a-116">**ชนิดแหล่งข้อมูล**: ระบุชนิดแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a25a-116">**Data source type**: Indicates the data source type</span></span>
* <span data-ttu-id="8a25a-117">**เส้นทางไปยังแหล่งข้อมูล**: เส้นทางไปยังแหล่งข้อมูลตามที่กำหนดไว้ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="8a25a-117">**Path to data source**: Path to the data source as defined in Power BI Desktop.</span></span> <span data-ttu-id="8a25a-118">ตัวอย่างเช่น ในรูปภาพด้านบน เส้นทางไปยังแหล่งข้อมูลของฐานข้อมูล SQL server คือสตริงการเชื่อมต่อ "twitterDB-yaronctestingdb1.database.windows.net" ตามที่กำหนดไว้ใน Power BI Desktop (แสดงที่ด้านล่าง)</span><span class="sxs-lookup"><span data-stu-id="8a25a-118">For example, in the image above, the path to the SQL server database data source is the connection string "twitterDB-yaronctestingdb1.database.windows.net", as defined in Power BI Desktop (shown below).</span></span> <span data-ttu-id="8a25a-119">ซึ่งประกอบด้วยชื่อฐานข้อมูล "twitterDB" และชื่อเซิร์ฟเวอร์ "yaronctestingdb1.database.windows.net"</span><span class="sxs-lookup"><span data-stu-id="8a25a-119">It consists of the database name "twitterDB" and the server name "yaronctestingdb1.database.windows.net".</span></span>

    ![ภาพหน้าจอของข้อกำหนดสตริงการเชื่อมต่อใน Power B I Desktop](media/service-data-source-impact-analysis/connection-string-definition-in-desktop.png)
 
* <span data-ttu-id="8a25a-121">**สรุปผลกระทบ**: แสดงจำนวนของพื้นที่ทำงาน กระแสข้อมูล และชุดข้อมูลที่อาจได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="8a25a-121">**Impact summary**: Shows you the number of potentially impacted workspaces, dataflows, and datasets.</span></span> <span data-ttu-id="8a25a-122">การนับจำนวนนี้รวมถึงพื้นที่ทำงานที่คุณไม่มีสิทธิ์เข้าถึงด้วย</span><span class="sxs-lookup"><span data-stu-id="8a25a-122">This count includes workspaces you don't have access to.</span></span>
* <span data-ttu-id="8a25a-123">**การแบ่งการใช้งาน**: แสดงให้คุณเห็นชื่อของกระแสข้อมูลและชุดข้อมูลที่ได้รับผลกระทบสำหรับแต่ละพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="8a25a-123">**Usage breakdown**: Shows you, for each workspace, the names of the impacted dataflows and datasets.</span></span> <span data-ttu-id="8a25a-124">หากต้องการสำรวจผลกระทบเพิ่มเติมในพื้นที่ทำงานเฉพาะ ให้คลิกที่ชื่อพื้นที่ทำงานเพื่อเปิดพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="8a25a-124">To further explore the impact on a particular workspace, click the workspace name to open the workspace.</span></span> <span data-ttu-id="8a25a-125">เมื่ออยู่ในพื้นที่ทำงานที่ได้รับผลกระทบ ให้ใช้[การวิเคราะห์ผลกระทบของชุดข้อมูล](service-dataset-impact-analysis.md) เพื่อดูรายละเอียดการใช้งานเกี่ยวกับรายงานและแดชบอร์ดที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="8a25a-125">Once in the affected workspace, use [dataset impact analysis](service-dataset-impact-analysis.md) to see the usage details about connected reports and dashboards.</span></span>

## <a name="notify-contacts"></a><span data-ttu-id="8a25a-126">แจ้งบุคคลติดต่อ</span><span class="sxs-lookup"><span data-stu-id="8a25a-126">Notify contacts</span></span>

<span data-ttu-id="8a25a-127">หากคุณได้ทำการเปลี่ยนแปลงแหล่งข้อมูลหรือกำลังคิดที่จะทำการเปลี่ยนแปลงคุณอาจต้องการติดต่อผู้ใช้ที่เกี่ยวข้องเพื่อแจ้งให้ทราบ</span><span class="sxs-lookup"><span data-stu-id="8a25a-127">If you've made a change to a data source or are thinking about making a change, you might want to contact the relevant users to tell them about it.</span></span> <span data-ttu-id="8a25a-128">เมื่อคุณแจ้งผู้ติดต่ออีเมลจะถูกส่งไปยัง [รายชื่อผู้ติดต่อ](service-create-the-new-workspaces.md#create-a-contact-list) ของพื้นที่ทำงานที่ได้รับผลกระทบทั้งหมด (ในกรณีของพื้นที่ทำงานแบบคลาสสิกอีเมลจะถูกส่งไปยังผู้ดูแลระบบพื้นที่ทำงาน)</span><span class="sxs-lookup"><span data-stu-id="8a25a-128">When you notify contacts, an email is sent to the [contact lists](service-create-the-new-workspaces.md#create-a-contact-list) of all the impacted workspaces (in case of classic workspaces, the email is sent to the workspace administrators).</span></span> <span data-ttu-id="8a25a-129">ชื่อของคุณจะปรากฏบนอีเมล ดังนั้น บุคคลติดต่อจะสามารถค้นหาคุณได้และตอบกลับในเธรดอีเมลใหม่</span><span class="sxs-lookup"><span data-stu-id="8a25a-129">Your name appears on the email so the contacts can find you and reply back in a new email thread.</span></span> 

1. <span data-ttu-id="8a25a-130">คลิก **แจ้งบุคคลติดต่อ** ในบานหน้าต่างด้านข่างการวิเคราะห์ผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="8a25a-130">Click **Notify contacts** in the impact analysis side pane.</span></span> <span data-ttu-id="8a25a-131">กล่องโต้ตอบแจ้งบุคคลติดต่อจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="8a25a-131">The notify contacts dialog will appear.</span></span>

   ![สกรีนช็อตของกล่องโต้ตอบการแจ้งเตือนผู้ติดต่อแหล่งข้อมูล](media/service-data-source-impact-analysis/notify-contacts-dialog.png)

1. <span data-ttu-id="8a25a-133">ในกล่องข้อความ ให้ระบุรายละเอียดบางอย่างเกี่ยวกับการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="8a25a-133">In the text box, provide some detail about the change.</span></span>
1. <span data-ttu-id="8a25a-134">เมื่อข้อความพร้อม ให้คลิก **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="8a25a-134">When the message is ready, click **Send**.</span></span>

## <a name="privacy"></a><span data-ttu-id="8a25a-135">ความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="8a25a-135">Privacy</span></span>

<span data-ttu-id="8a25a-136">ในบานหน้าต่างด้านข้างการวิเคราะห์ผลกระทบ คุณจะเห็นเฉพาะชื่อจริงสำหรับพื้นที่ทำงาน ชุดข้อมูล และกระแสข้อมูลที่คุณสามารถเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="8a25a-136">In the impact analysis side pane, you only see real names for workspaces, datasets, and dataflows that you have access to.</span></span> <span data-ttu-id="8a25a-137">หน่วยข้อมูลที่คุณไม่มีสิทธิ์ในการเข้าถึงจะแสดงเป็นการเข้าถึงแบบจำกัด</span><span class="sxs-lookup"><span data-stu-id="8a25a-137">Items that you don't have access to are listed as Limited access.</span></span> <span data-ttu-id="8a25a-138">เนื่องจากชื่อหน่วยข้อมูลบางรายการอาจมีข้อมูลส่วนบุคคลอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="8a25a-138">This is because some item names may contain personal information.</span></span>
<span data-ttu-id="8a25a-139">จำนวนสรุปผลกระทบ รวมถึงกระแสข้อมูลและชุดข้อมูลที่ได้รับผลกระทบทั้งหมด แม้ว่าจะอยู่ในพื้นที่ทำงานที่คุณไม่มีสิทธิ์เข้าถึงก็ตาม</span><span class="sxs-lookup"><span data-stu-id="8a25a-139">The impact summary counts include all impacted dataflows and datasets, even those that reside in workspaces you don't have access to.</span></span>

## <a name="limitations"></a><span data-ttu-id="8a25a-140">ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="8a25a-140">Limitations</span></span>

<span data-ttu-id="8a25a-141">รายงานแบบแบ่งหน้ายังไม่รองรับการวิเคราะห์ผลกระทบของแหล่งข้อมูล ดังนั้นคุณจะไม่เห็นว่าแหล่งข้อมูลมีผลกระทบโดยตรงใด ๆ กับรายงานชนิดนี้ในผู้เช่าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8a25a-141">Data source impact analysis is not yet supported for paginated reports, so you will not see if the data source has any direct impact on these kinds of reports in the tenant.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8a25a-142">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="8a25a-142">Next steps</span></span>

* [<span data-ttu-id="8a25a-143">การวิเคราะห์ผลกระทบของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a25a-143">Dataset impact analysis</span></span>](service-dataset-impact-analysis.md)
* [<span data-ttu-id="8a25a-144">สายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a25a-144">Data lineage</span></span>](service-data-lineage.md)