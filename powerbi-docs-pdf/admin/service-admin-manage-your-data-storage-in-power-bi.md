---
title: จัดการที่เก็บข้อมูลในพื้นที่ทำงานของคุณ
description: เรียนรู้วิธีจัดการที่เก็บข้อมูลของคุณ หรือของพื้นที่ทำงาน เพื่อให้แน่ใจว่าคุณสามารถเผยแพร่รายงานและชุดข้อมูลต่อไปได้
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: how-to
ms.date: 07/27/2020
LocalizationGroup: Administration
ms.openlocfilehash: ccf9cc65cc5dc18d72ced490b18683a6a1af32ff
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96408722"
---
# <a name="manage-data-storage-in-power-bi-workspaces"></a><span data-ttu-id="a0ad7-103">ladakจัดการที่เก็บข้อมูลในพื้นที่ทำงานบน Power BI</span><span class="sxs-lookup"><span data-stu-id="a0ad7-103">Manage data storage in Power BI workspaces</span></span>

<span data-ttu-id="a0ad7-104">เรียนรู้วิธีจัดการที่เก็บข้อมูลของคุณ หรือของพื้นที่ทำงาน เพื่อให้คุณสามารถเผยแพร่รายงานและชุดข้อมูลต่อไปได้</span><span class="sxs-lookup"><span data-stu-id="a0ad7-104">Learn how to manage data storage in your individual or workspace so you can keep publishing reports and datasets.</span></span>

## <a name="capacity-limits"></a><span data-ttu-id="a0ad7-105">ขีดจำกัดความจุ</span><span class="sxs-lookup"><span data-stu-id="a0ad7-105">Capacity limits</span></span>

<span data-ttu-id="a0ad7-106">ข้อจำกัดที่เก็บข้อมูลพื้นที่ทำงาน ไม่ว่าจะสำหรับพื้นที่ทำงานของฉันหรือพื้นที่ทำงานของแอป ทั้งนี้ขึ้นอยู่กับว่าพื้นที่ทำงานอยู่ใน [ความจุแบบใช้ร่วมกันหรือความจุพรีเมี่ยม](../fundamentals/service-basic-concepts.md#capacities)</span><span class="sxs-lookup"><span data-stu-id="a0ad7-106">Workspace storage limits, whether for My Workspace or an app workspace, depend on whether the workspace is in [shared or Premium capacity](../fundamentals/service-basic-concepts.md#capacities).</span></span>

### <a name="shared-capacity-limits"></a><span data-ttu-id="a0ad7-107">ขีดจำกัดความจุแบบใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="a0ad7-107">Shared capacity limits</span></span>
<span data-ttu-id="a0ad7-108">สำหรับพื้นที่ทำงานในความจุที่ใช้ร่วมกัน:</span><span class="sxs-lookup"><span data-stu-id="a0ad7-108">For workspaces in shared capacity:</span></span> 

- <span data-ttu-id="a0ad7-109">มีขีดจำกัดสำหรับพื้นที่เก็บข้อมูลตามพื้นที่ทำงาน 10 GB</span><span class="sxs-lookup"><span data-stu-id="a0ad7-109">There is a per-workspace storage limit of 10 GB.</span></span>
- <span data-ttu-id="a0ad7-110">สำหรับพื้นที่ทำงานของแอป การใช้งานทั้งหมดจะต้องไม่เกิน 10 GB คูณด้วยจำนวนสิทธิ์ใช้งาน Pro ในผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="a0ad7-110">For app workspaces, the total usage can’t exceed the tenant storage limit of 10 GB multiplied by the number of Pro licenses in the tenant.</span></span>

### <a name="premium-capacity-limits"></a><span data-ttu-id="a0ad7-111">ขีดจำกัดความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="a0ad7-111">Premium capacity limits</span></span>
<span data-ttu-id="a0ad7-112">สำหรับพื้นที่ทำงานในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="a0ad7-112">For workspaces in Premium capacity:</span></span>
- <span data-ttu-id="a0ad7-113">มีขีดจำกัด 100 TB ต่อความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="a0ad7-113">There is a limit of 100 TB per Premium capacity.</span></span>
- <span data-ttu-id="a0ad7-114">ไม่มีขีดจำกัดพื้นที่เก็บข้อมูลต่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="a0ad7-114">There is no per-user storage limit.</span></span>

<span data-ttu-id="a0ad7-115">อ่านเกี่ยวกับคุณลักษณะอื่น ๆ ของ[รูปแบบการกำหนดราคา Power BI](https://powerbi.microsoft.com/pricing)</span><span class="sxs-lookup"><span data-stu-id="a0ad7-115">Read about other features of the [Power BI pricing model](https://powerbi.microsoft.com/pricing).</span></span>

## <a name="whats-included-in-storage"></a><span data-ttu-id="a0ad7-116">มีอะไรรวมอยู่ในพื้นที่เก็บข้อมูลบ้าง</span><span class="sxs-lookup"><span data-stu-id="a0ad7-116">What's included in storage</span></span>

<span data-ttu-id="a0ad7-117">ที่รวมอยู่ในที่เก็บข้อมูลของคุณ ได้แก่ ชุดข้อมูลและรายงาน Excel ของคุณเอง และรายการเหล่านั้นที่มีคนแชร์ให้คุณ</span><span class="sxs-lookup"><span data-stu-id="a0ad7-117">Included in your data storage are your own datasets and Excel reports, and those items that someone has shared with you.</span></span> <span data-ttu-id="a0ad7-118">ชุดข้อมูลเป็นแหล่งข้อมูลใด ๆ ที่คุณอัปโหลดหรือเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="a0ad7-118">Datasets are any of the data sources you’ve uploaded or connected to.</span></span> <span data-ttu-id="a0ad7-119">แหล่งข้อมูลเหล่านี้รวมถึงไฟล์ Power BI Desktop และสมุดงาน Excel ที่คุณกำลังใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a0ad7-119">These data sources include Power BI Desktop files and Excel workbooks you’re using.</span></span> <span data-ttu-id="a0ad7-120">ต่อไปนี้ยังรวมอยู่ในความจุข้อมูลของคุณด้วย</span><span class="sxs-lookup"><span data-stu-id="a0ad7-120">The following are also included in your data capacity.</span></span>

* <span data-ttu-id="a0ad7-121">ช่วงของข้อมูลใน Excel ที่ปักหมุดไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="a0ad7-121">Excel ranges pinned to a dashboard.</span></span>
* <span data-ttu-id="a0ad7-122">การแสดงภาพภายในองค์กรของ Reporting Services ที่ปักหมุดไปยังแดชบอร์ด Power BI</span><span class="sxs-lookup"><span data-stu-id="a0ad7-122">Reporting Services on-premises visualizations pinned to a Power BI dashboard.</span></span>
* <span data-ttu-id="a0ad7-123">รูปภาพที่ถูกอัปโหลด</span><span class="sxs-lookup"><span data-stu-id="a0ad7-123">Uploaded images.</span></span>

<span data-ttu-id="a0ad7-124">ขนาดของแดชบอร์ดที่คุณแชร์จะแตกต่างกัน ทั้งนี้ขึ้นอยู่กับว่ามีอะไรปักหมุดอยู่ข้างในบ้าง</span><span class="sxs-lookup"><span data-stu-id="a0ad7-124">The size of a dashboard that you share varies, depending on what's pinned to it.</span></span> <span data-ttu-id="a0ad7-125">ตัวอย่างเช่น ถ้าคุณปักหมุดรายการจากรายงานสองฉบับที่เป็นส่วนหนึ่งของชุดข้อมูลที่แตกต่างกันสองชุด ขนาดจะรวมชุดข้อมูลทั้งสองชุด</span><span class="sxs-lookup"><span data-stu-id="a0ad7-125">For example, if you pin items from two reports that are part of two different datasets, the size includes both datasets.</span></span>

## <a name="manage-items-you-own"></a><span data-ttu-id="a0ad7-126">จัดการรายการที่คุณเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="a0ad7-126">Manage items you own</span></span>

<span data-ttu-id="a0ad7-127">ดูว่าคุณกำลังใช้พื้นที่จัดเก็บข้อมูลเท่าไรในบัญชีของคุณ Power BI และจัดการบัญชีของคุณ</span><span class="sxs-lookup"><span data-stu-id="a0ad7-127">See how much data storage you’re using in your Power BI account, and manage your account.</span></span>

1. <span data-ttu-id="a0ad7-128">เพื่อจัดการพื้นที่เก็บข้อมูลของคุณเอง ให้ไปที่ **พื้นที่งานของฉัน** ในบานหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="a0ad7-128">To manage your own storage, go to **My Workspace** on the navigation pane.</span></span>
   
    ![ภาพหน้าจอของบานหน้าต่างการนำทางที่มีการเรียกใช้พื้นที่ทำงานของฉัน](media/service-admin-manage-your-data-storage-in-power-bi/pbi_myworkspace.png)

2. <span data-ttu-id="a0ad7-130">เลือก![ไอคอนรูปเฟือง](media/service-admin-manage-your-data-storage-in-power-bi/pbi_gearicon.png)ที่มุมขวาบนของ **จัดการที่เก็บข้อมูลส่วนบุคคล**</span><span class="sxs-lookup"><span data-stu-id="a0ad7-130">Select the gear icon ![Gear icon](media/service-admin-manage-your-data-storage-in-power-bi/pbi_gearicon.png) in the upper-right corner **Manage personal storage**.</span></span>
   
    <span data-ttu-id="a0ad7-131">แถบด้านบนแสดงให้เห็นว่า คุณได้ใช้ที่เก็บข้อมูลมากแค่ไหน</span><span class="sxs-lookup"><span data-stu-id="a0ad7-131">The top bar shows how much of your storage limit you’ve used.</span></span>
   
    ![ภาพหน้าจอของการจัดการขีดจำกัดที่เก็บข้อมูล ที่แสดงว่าที่เก็บข้อมูลถูกใช้งานไปเท่าไหร่แล้ว](media/service-admin-manage-your-data-storage-in-power-bi/pbi_persnlstorage.png)
   
    <span data-ttu-id="a0ad7-133">ชุดข้อมูลและรายงานจะถูกแบ่งออกเป็นสองแท็บ:</span><span class="sxs-lookup"><span data-stu-id="a0ad7-133">The datasets and reports are separated onto two tabs:</span></span>
   
    <span data-ttu-id="a0ad7-134">**ฉันเป็นเจ้าของ:** คุณได้อัปโหลดรายงานและชุดข้อมูลเหล่านี้ไปยังบัญชี Power BI ของคุณ รวมถึงชุดข้อมูลบริการ เช่น Salesforce และ Dynamics CRM</span><span class="sxs-lookup"><span data-stu-id="a0ad7-134">**Owned by me:** You’ve uploaded these reports and datasets to your Power BI account, including service datasets such as Salesforce and Dynamics CRM.</span></span>  

    <span data-ttu-id="a0ad7-135">**ผู้อื่นเป็นเจ้าของ:** ผู้อื่นได้แชร์รายงานและชุดข้อมูลเหล่านี้ให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="a0ad7-135">**Owned by others:** Others have shared these reports and datasets with you.</span></span>
1. <span data-ttu-id="a0ad7-136">เมื่อต้องการลบชุดข้อมูลหรือรายงาน ให้เลือกไอคอนรูปถังขยะ</span><span class="sxs-lookup"><span data-stu-id="a0ad7-136">To delete a dataset or report, select the trash can icon</span></span> ![ไอคอนถังขยะ](media/service-admin-manage-your-data-storage-in-power-bi/pbi_deleteicon.png)<span data-ttu-id="a0ad7-138">.</span><span class="sxs-lookup"><span data-stu-id="a0ad7-138">.</span></span>

<span data-ttu-id="a0ad7-139">โปรดทราบว่า คุณหรือบุคคลอื่นอาจมีรายงานและแดชบอร์ดที่ขึ้นกับชุดข้อมูลหนึ่ง ๆ</span><span class="sxs-lookup"><span data-stu-id="a0ad7-139">Keep in mind that you or someone else may have reports and dashboards based on a dataset.</span></span> <span data-ttu-id="a0ad7-140">ถ้าคุณลบชุดข้อมูล รายงานและแดชบอร์ดเหล่านั้นจะไม่ทำงานอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="a0ad7-140">If you delete the dataset, those reports and dashboards won’t work anymore.</span></span>

## <a name="manage-your-workspace"></a><span data-ttu-id="a0ad7-141">จัดการพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="a0ad7-141">Manage your workspace</span></span>
1. <span data-ttu-id="a0ad7-142">เลือกลูกศรที่อยู่ถัดจาก **พื้นที่ทำงาน** และเลือกชื่อของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="a0ad7-142">Select the arrow next to **Workspaces** select the name of the workspace.</span></span>
   
    ![ภาพหน้าจอของการเลือกพื้นที่ทำงาน ที่แสดงพื้นที่ทำงานของกลุ่มการขาย](media/service-admin-manage-your-data-storage-in-power-bi/pbi_groupworkspaces.png)
2. <span data-ttu-id="a0ad7-144">เลือก![ไอคอนรูปเฟือง](media/service-admin-manage-your-data-storage-in-power-bi/pbi_gearicon.png)ที่มุมบนขวาของ **จัดการที่เก็บข้อมูลกลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="a0ad7-144">Select the gear icon ![Gear icon](media/service-admin-manage-your-data-storage-in-power-bi/pbi_gearicon.png) in the upper-right corner **Manage group storage**.</span></span>
   
    <span data-ttu-id="a0ad7-145">แถบด้านบนแสดงให้เห็นว่า มีการใช้ที่เก็บข้อมูลกลุ่มมากแค่ไหน</span><span class="sxs-lookup"><span data-stu-id="a0ad7-145">The top bar shows how much of the group’s storage limit is used.</span></span>
   
    ![ภาพหน้าจอของการจัดการที่เก็บข้อมูล ที่แสดงว่าขีดจำกัดที่เก็บข้อมูลของกลุ่มการขายถูกใช้งานไปเท่าไหร่แล้ว](media/service-admin-manage-your-data-storage-in-power-bi/pbi_groupstorage.png)
   
    <span data-ttu-id="a0ad7-147">ชุดข้อมูลและรายงานจะถูกแบ่งออกเป็นสองแท็บ:</span><span class="sxs-lookup"><span data-stu-id="a0ad7-147">The datasets and reports are separated onto two tabs:</span></span>
   
    <span data-ttu-id="a0ad7-148">**เราเป็นเจ้าของ:** คุณหรือผู้อื่นได้อัปโหลดรายงานและชุดข้อมูลเหล่านี้ไปยังบัญชี Power BI ของกลุ่ม รวมถึงชุดข้อมูลบริการ เช่น Salesforce และ Dynamics CRM</span><span class="sxs-lookup"><span data-stu-id="a0ad7-148">**Owned by us:** You or someone else has uploaded these reports and datasets to the group’s Power BI account, including service datasets such as Salesforce and Dynamics CRM.</span></span>

    <span data-ttu-id="a0ad7-149">**ผู้อื่นเป็นเจ้าของ:** ผู้อื่นได้แชร์รายงานและชุดข้อมูลเหล่านี้ให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="a0ad7-149">**Owned by others:** Others have shared these reports and datasets with your group.</span></span>

3. <span data-ttu-id="a0ad7-150">เมื่อต้องการลบชุดข้อมูลหรือรายงาน ให้เลือกไอคอนรูปถังขยะ</span><span class="sxs-lookup"><span data-stu-id="a0ad7-150">To delete a dataset or report, select the trash can icon</span></span> ![ไอคอนถังขยะ](media/service-admin-manage-your-data-storage-in-power-bi/pbi_deleteicon.png)<span data-ttu-id="a0ad7-152">.</span><span class="sxs-lookup"><span data-stu-id="a0ad7-152">.</span></span>
   
   > [!NOTE]
   > <span data-ttu-id="a0ad7-153">โปรดทราบว่า คุณหรือบุคคลอื่นในกลุ่มอาจมีรายงานและแดชบอร์ดที่ขึ้นกับชุดข้อมูลหนึ่ง ๆ</span><span class="sxs-lookup"><span data-stu-id="a0ad7-153">Keep in mind that you or someone else in the group may have reports and dashboards based on a dataset.</span></span> <span data-ttu-id="a0ad7-154">ถ้าคุณลบชุดข้อมูล รายงานและแดชบอร์ดเหล่านั้นจะไม่ทำงานอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="a0ad7-154">If you delete the dataset, those reports and dashboards won’t work anymore.</span></span>
   
   <span data-ttu-id="a0ad7-155">สมาชิกใดก็ตามในพื้นที่ทำงานที่มีบทบาทผู้ดูแลระบบ สมาชิก หรือผู้สนับสนุนมีสิทธิ์ในการลบชุดข้อมูลและรายงานออกจากพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="a0ad7-155">Any member in a workspace with the admin, member, or contributor role has permissions to delete datasets and reports from the workspace.</span></span>

## <a name="dataset-limits"></a><span data-ttu-id="a0ad7-156">ขีดจำกัดของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a0ad7-156">Dataset limits</span></span>
<span data-ttu-id="a0ad7-157">มีขีดจำกัด 1 GB ต่อชุดข้อมูลที่นำเข้าไปใน Power BI</span><span class="sxs-lookup"><span data-stu-id="a0ad7-157">There is a 1 GB limit per dataset that is imported into Power BI.</span></span> <span data-ttu-id="a0ad7-158">ถ้าคุณเลือกที่จะเก็บประสบการณ์ Excel แทนที่จะนำเข้าข้อมูล ซึ่งจะถูกจำกัดที่ 250 MB สำหรับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a0ad7-158">If you have chosen to keep the Excel experience, instead of importing the data, the limit is 250 MB for the dataset.</span></span>

## <a name="what-happens-when-you-reach-a-limit"></a><span data-ttu-id="a0ad7-159">เกิดอะไรขึ้นเมื่อคุณถึงขีดจำกัด</span><span class="sxs-lookup"><span data-stu-id="a0ad7-159">What happens when you reach a limit</span></span>
<span data-ttu-id="a0ad7-160">เมื่อคุณถึงขีดจำกัดความจุข้อมูลของคุณ คุณจะเห็นพร้อมท์ภายในบริการ</span><span class="sxs-lookup"><span data-stu-id="a0ad7-160">When you reach the data capacity limit of what you can do, you see prompts within the service.</span></span> 

<span data-ttu-id="a0ad7-161">เมื่อคุณเลือกไอคอนรูปเฟือง</span><span class="sxs-lookup"><span data-stu-id="a0ad7-161">When you select the gear icon</span></span> ![ไอคอนรูปเฟือง](media/service-admin-manage-your-data-storage-in-power-bi/pbi_gearicon.png)<span data-ttu-id="a0ad7-163">, คุณจะเห็นแถบสีแดงซึ่งระบุว่า คุณกำลังใช้งานเกินขีดจำกัดความจุของข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="a0ad7-163">, you see a red bar indicating you are over your data capacity limit.</span></span>

![ภาพหน้าจอของความจุที่เก็บข้อมูล ที่แสดงว่าความจุถึงขีดจำกัดแล้ว](media/service-admin-manage-your-data-storage-in-power-bi/manage-storage-limit.png)

<span data-ttu-id="a0ad7-165">ขีดจำกัดนี้ยังระบุไว้ภายใน **จัดการที่เก็บข้อมูลส่วนบุคคล** อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="a0ad7-165">This limit also is indicated within **Manage personal storage**.</span></span>

 ![ภาพหน้าจอของความจุที่เก็บข้อมูลส่วนบุคคล ที่แสดงว่าความจุของเจนถึงขีดจำกัดแล้ว](media/service-admin-manage-your-data-storage-in-power-bi/manage-storage-limit2.png)

 <span data-ttu-id="a0ad7-167">เมื่อคุณพยายามที่จะดำเนินการใด ๆ ที่ทำให้ถึงขีดจำกัดเหล่านี้ คุณจะเห็นข้อความที่ระบุว่า คุณกำลังใช้เกินขีดจำกัด</span><span class="sxs-lookup"><span data-stu-id="a0ad7-167">When you try to perform an action that will reach one of the limits, you see a message you are over the limit.</span></span> <span data-ttu-id="a0ad7-168">คุณสามารถ[จัดการที่เก็บข้อมูลของคุณ](#manage-items-you-own)เพื่อลดปริมาณข้อมูลในที่เก็บข้อมูลและแก้ไขขีดจำกัดดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="a0ad7-168">You can [manage your storage](#manage-items-you-own) to reduce your storage amount and get past the limit.</span></span>

 ![ภาพหน้าจอของกล่องโต้ตอบการใช้งานเกินขีดจำกัดที่เก็บข้อมูลของคุณ ที่แสดงว่าความจุถึงขีดจำกัดแล้ว](media/service-admin-manage-your-data-storage-in-power-bi/powerbi-pro-over-limit.png)

 ## <a name="next-steps"></a><span data-ttu-id="a0ad7-170">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a0ad7-170">Next steps</span></span>

 <span data-ttu-id="a0ad7-171">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a0ad7-171">More questions?</span></span> [<span data-ttu-id="a0ad7-172">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="a0ad7-172">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
