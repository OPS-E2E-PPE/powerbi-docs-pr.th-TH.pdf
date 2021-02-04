---
title: สร้างรายงานที่ยึดตามชุดข้อมูลจากพื้นที่ทำงานอื่น - Power BI
description: เรียนรู้วิธีที่คุณสามารถแชร์ชุดข้อมูลกับผู้ใช้ทั้งองค์กร จากนั้นพวกเขาสามารถสร้างรายงานที่ยึดตามชุดข้อมูลของคุณในพื้นที่ทำงานของตนเอง
author: paulinbar
ms.author: painbar
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 04/30/2020
LocalizationGroup: Share your work
ms.openlocfilehash: 3f1f689aa272ac98f4a3dd4aef7c2b2728fce41e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96392507"
---
# <a name="create-reports-based-on-datasets-from-different-workspaces"></a><span data-ttu-id="9df16-104">สร้างรายงานที่ยึดตามชุดข้อมูลจากพื้นที่ทำงานอื่น</span><span class="sxs-lookup"><span data-stu-id="9df16-104">Create reports based on datasets from different workspaces</span></span>

<span data-ttu-id="9df16-105">เรียนรู้วิธีการที่คุณสามารถสร้างรายงานในพื้นที่ทำงานของคุณเองโดยยึดตามชุดข้อมูลในพื้นที่ทำงานอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="9df16-105">Learn how you can create reports in your own workspaces based on datasets in other workspaces.</span></span> <span data-ttu-id="9df16-106">หากต้องการสร้างรายงานที่ด้านบนของชุดข้อมูลที่มีอยู่ คุณสามารถเริ่มต้นจาก Power BI Desktop หรือจากบริการของ Power BI ในพื้นที่ทำงานของฉัน หรือใน[ประสบการณ์การใช้งานพื้นที่ทำงานใหม่](../collaborate-share/service-create-the-new-workspaces.md)ได้</span><span class="sxs-lookup"><span data-stu-id="9df16-106">To build a report on top of an existing dataset, you can start from Power BI Desktop or from the Power BI service, in your My Workspace or in a [new workspace experience](../collaborate-share/service-create-the-new-workspaces.md).</span></span>

- <span data-ttu-id="9df16-107">ในบริการของ Power BI: **รับข้อมูล** > **ชุดข้อมูลที่เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="9df16-107">In the Power BI service: **Get data** > **Published datasets**.</span></span>
- <span data-ttu-id="9df16-108">ใน Power BI Desktop: **รับข้อมูล** > **ชุดข้อมูล Power BI**</span><span class="sxs-lookup"><span data-stu-id="9df16-108">In Power BI Desktop: **Get data** > **Power BI datasets**.</span></span>

    ![เชื่อมต่อไปยังชุดข้อมูลที่มีอยู่](media/service-datasets-across-workspaces/power-bi-connect-dataset-pk.png)
   
<span data-ttu-id="9df16-110">ในทั้งสองกรณี ประสบการณ์การค้นพบชุดข้อมูลเริ่มต้นในกล่องโต้ตอบนี้ **เลือกชุดข้อมูลเพื่อสร้างรายงาน**</span><span class="sxs-lookup"><span data-stu-id="9df16-110">In both cases, the dataset discovery experience starts in this dialog box, **Select a dataset to create a report**.</span></span> <span data-ttu-id="9df16-111">คุณจะเห็นชุดข้อมูลทั้งหมดที่คุณสามารถเข้าถึงโดยไม่คำนึงถึงตำแหน่งที่ชุดข้อมูลเหล่านั้นอยู่:</span><span class="sxs-lookup"><span data-stu-id="9df16-111">You see all the datasets you have access to, regardless of where they are:</span></span>

![เลือกชุดข้อมูล](media/service-datasets-across-workspaces/power-bi-select-dataset.png)

<span data-ttu-id="9df16-113">คุณสังเกตเห็นชุดข้อมูลแรกติดป้ายชื่อ **เลื่อนระดับ**</span><span class="sxs-lookup"><span data-stu-id="9df16-113">You notice the first one is labeled **Promoted**.</span></span> <span data-ttu-id="9df16-114">เราจะดำเนินการเช่นนั้นใน[ค้นหาชุดข้อมูลที่รับรองแล้ว](#find-an-endorsed-dataset) ในภายหลังในบทความนี้</span><span class="sxs-lookup"><span data-stu-id="9df16-114">We'll get to that in [Find an endorsed dataset](#find-an-endorsed-dataset), later in this article.</span></span>

<span data-ttu-id="9df16-115">ชุดข้อมูลที่คุณเห็นรายการนี้จะตรงกับเงื่อนไขต่อไปนี้อย่างน้อยหนึ่งข้อ:</span><span class="sxs-lookup"><span data-stu-id="9df16-115">The datasets you see in this list meet at least one of the following conditions:</span></span>

- <span data-ttu-id="9df16-116">ชุดข้อมูลอยู่ในพื้นที่ทำงานที่มีประสบการณ์การใช้งานพื้นที่ทำงานใหม่ที่ใดที่หนึ่ง และคุณเป็นสมาชิกของพื้นที่ทำงานนั้น</span><span class="sxs-lookup"><span data-stu-id="9df16-116">The dataset is in one of the new workspace experience workspaces, and you're a member of that workspace.</span></span> <span data-ttu-id="9df16-117">ดู[ข้อควรพิจารณาและข้อจำกัด](service-datasets-across-workspaces.md#considerations-and-limitations)</span><span class="sxs-lookup"><span data-stu-id="9df16-117">See [Considerations and limitations](service-datasets-across-workspaces.md#considerations-and-limitations).</span></span>
- <span data-ttu-id="9df16-118">คุณมีสิทธิในการสร้างสำหรับชุดข้อมูล ซึ่งอยู่ในพื้นที่ทำงานที่มีประสบการณ์การใช้งานพื้นที่ทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="9df16-118">You have Build permission for the dataset, which is in a new workspace experience workspace.</span></span>
- <span data-ttu-id="9df16-119">ชุดข้อมูลอยู่ในพื้นที่ทำงานของฉัน</span><span class="sxs-lookup"><span data-stu-id="9df16-119">The dataset is in your My Workspace.</span></span>

> [!NOTE]
> <span data-ttu-id="9df16-120">ถ้าคุณเป็นผู้ใช้ฟรี คุณจะเห็นเฉพาะชุดข้อมูลในพื้นที่ทำงานของฉันหรือชุดข้อมูลที่ที่คุณมีสิทธิในการสร้างที่อยู่ในพื้นที่ทำงานของความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="9df16-120">If you're a free user, you only see datasets in your My Workspace, or datasets for which you have Build permission that are in Premium-capacity workspaces.</span></span>

<span data-ttu-id="9df16-121">เมื่อคุณคลิกที่ **สร้าง** คุณสร้างการเชื่อมต่อสดกับชุดข้อมูล และประสบการณ์ในการสร้างรายงานจะเปิดขึ้นพร้อมกับชุดข้อมูลทั้งหมดที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9df16-121">When you click **Create**, you create a live connection to the dataset, and the report creation experience opens with the full dataset available.</span></span> <span data-ttu-id="9df16-122">คุณยังไม่ได้ทำสำเนาของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9df16-122">You haven't made a copy of the dataset.</span></span> <span data-ttu-id="9df16-123">ชุดข้อมูลยังคงอยู่ในตำแหน่งเดิม</span><span class="sxs-lookup"><span data-stu-id="9df16-123">The dataset still resides in its original location.</span></span> <span data-ttu-id="9df16-124">คุณสามารถใช้ตารางและหน่วยวัดทั้งหมดในชุดข้อมูลเพื่อสร้างรายงานของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="9df16-124">You can use all tables and measures in the dataset to build your own reports.</span></span> <span data-ttu-id="9df16-125">ข้อจำกัดด้านความปลอดภัยระดับแถว (RLS) บนชุดข้อมูลจะมีผล เพื่อให้คุณเท่านั้นดูข้อมูลที่คุณมีสิทธิในการดูตามบทบาท RLS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="9df16-125">Row-level security (RLS) restrictions on the dataset are in effect, so you only see data you have permissions to see based on your RLS role.</span></span>

<span data-ttu-id="9df16-126">คุณสามารถบันทึกรายงานไปยังพื้นที่ทำงานปัจจุบันในบริการของ Power BI หรือเผยแพร่รายงานไปยังพื้นที่ทำงานจาก Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="9df16-126">You can save the report to the current workspace in the Power BI service, or publish the report to a workspace from Power BI Desktop.</span></span> <span data-ttu-id="9df16-127">Power BI สร้างรายการในรายชื่อของชุดข้อมูลโดยอัตโนมัติถ้ารายงานที่ยึดตามชุดข้อมูลที่อยู่นอกพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="9df16-127">Power BI automatically creates an entry in the list of datasets if the report is based on a dataset outside of the workspace.</span></span> <span data-ttu-id="9df16-128">ไอคอนสำหรับชุดข้อมูลนี้จะแตกต่างจากไอคอนสำหรับชุดข้อมูลในพื้นที่ทำงาน:</span><span class="sxs-lookup"><span data-stu-id="9df16-128">The icon for this dataset is different from the icon for datasets in the workspace:</span></span> ![ไอคอนชุดข้อมูลที่ใช้ร่วมกัน](media/service-datasets-discover-across-workspaces/power-bi-shared-dataset-icon.png)

<span data-ttu-id="9df16-130">ด้วยวิธี สมาชิกของพื้นที่ทำงานสามารถบอกว่ารายงานและแดชบอร์ดใดใช้ชุดข้อมูลที่อยู่นอกพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="9df16-130">That way, members of the workspace can tell which reports and dashboards use datasets that are outside the workspace.</span></span> <span data-ttu-id="9df16-131">รายการจะแสดงข้อมูลเกี่ยวกับชุดข้อมูลและการดำเนินการเลือกสองสามอย่าง</span><span class="sxs-lookup"><span data-stu-id="9df16-131">The entry shows information about the dataset, and a few select actions.</span></span>

![การดำเนินการของชุดข้อมูล](media/service-datasets-across-workspaces/power-bi-dataset-actions.png)

## <a name="find-an-endorsed-dataset"></a><span data-ttu-id="9df16-133">ค้นหาชุดข้อมูลที่รับรองแล้ว</span><span class="sxs-lookup"><span data-stu-id="9df16-133">Find an endorsed dataset</span></span>

<span data-ttu-id="9df16-134">มีชุดข้อมูลที่รับรองแล้วสองชนิดแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="9df16-134">There are two different kinds of endorsed datasets.</span></span> <span data-ttu-id="9df16-135">เจ้าของชุดข้อมูลสามารถ *เลื่อนระดับ* ชุดข้อมูลที่พวกเขาแนะนำให้คุณได้</span><span class="sxs-lookup"><span data-stu-id="9df16-135">Dataset owners can *promote* a dataset that they recommend to you.</span></span> <span data-ttu-id="9df16-136">นอกจากนี้ ผู้ดูแลระบบ Power BI ยังสามารถกำหนดผู้เชี่ยวชาญในองค์กรของคุณที่สามารถ *รับรอง* ชุดข้อมูลสำหรับทุกคนที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="9df16-136">Also, the Power BI admin can designate experts in your organization who can *certify* datasets for everyone to use.</span></span> <span data-ttu-id="9df16-137">ทั้งชุดข้อมูลที่เลื่อนระดับและได้รับการรับรองจะแสดง *ตัวบอกสถานะ* ที่คุณเห็นทั้งสองอย่างเมื่อค้นหาชุดข้อมูล และในรายชื่อของชุดข้อมูลในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="9df16-137">Promoted and certified datasets both display *badges* that you see both when looking for a dataset, and in the list of datasets in a workspace.</span></span> <span data-ttu-id="9df16-138">ชื่อของบุคคลที่ได้รับการรับรองชุดข้อมูลแล้วจะแสดงในคำแนะนำในระหว่างประสบการณ์การค้นหาชุดข้อมูล โฮเวอร์เหนือป้ายกำกับ **รับรองแล้ว** และคุณเห็น</span><span class="sxs-lookup"><span data-stu-id="9df16-138">The name of the person who certified a dataset is displayed in a tooltip during the dataset discovery experience; hover over the **Certified** label and you see it.</span></span>

- <span data-ttu-id="9df16-139">ในบริการของ Power BI: **รับข้อมูล** > **ชุดข้อมูลที่เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="9df16-139">In the Power BI service: **Get data** > **Published datasets**.</span></span>
- <span data-ttu-id="9df16-140">ใน Power BI Desktop: **รับข้อมูล** > **ชุดข้อมูล Power BI**</span><span class="sxs-lookup"><span data-stu-id="9df16-140">In Power BI Desktop: **Get data** > **Power BI datasets**.</span></span>

    <span data-ttu-id="9df16-141">ในกล่องโต้ตอบ **เลือกชุดข้อมูล** ชุดข้อมูลที่รับรองแล้วจะอยู่ด้านบนรายการตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="9df16-141">In the **Select a dataset** dialog box, endorsed datasets top the list by default.</span></span> 

    ![ชุดข้อมูลที่เลื่อนระดับ](media/service-datasets-discover-across-workspaces/power-bi-dataset-promoted.png)

## <a name="next-steps"></a><span data-ttu-id="9df16-143">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="9df16-143">Next steps</span></span>

- [<span data-ttu-id="9df16-144">ใช้ชุดข้อมูลทั่วทั้งพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="9df16-144">Use datasets across workspaces</span></span>](service-datasets-across-workspaces.md)
- <span data-ttu-id="9df16-145">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="9df16-145">Questions?</span></span> [<span data-ttu-id="9df16-146">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="9df16-146">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
