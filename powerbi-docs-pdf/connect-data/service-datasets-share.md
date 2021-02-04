---
title: แชร์ชุดข้อมูล
description: ในฐานะเจ้าของชุดข้อมูล คุณสามารถสร้างและแชร์ชุดข้อมูลของคุณเพื่อให้ผู้อื่นสามารถใช้ได้ เรียนรู้วิธีการแชร์
author: paulinbar
ms.author: painbar
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 04/30/2020
LocalizationGroup: Share your work
ms.openlocfilehash: c73c5b1b803b73742f6f13456b07a2060f5757e4
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410424"
---
# <a name="share-a-dataset"></a><span data-ttu-id="0739f-104">แชร์ชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0739f-104">Share a dataset</span></span>

<span data-ttu-id="0739f-105">ในฐานะผู้สร้าง *แบบจำลองข้อมูล* ใน Power BI Desktop คุณกำลังสร้าง *ชุดข้อมูล* ที่คุณสามารถแจกจ่ายได้ในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="0739f-105">As a creator of *data models* in Power BI Desktop, you're creating *datasets* that you can distribute in the Power BI service.</span></span> <span data-ttu-id="0739f-106">จากนั้น ผู้สร้างรายงานอื่น ๆ สามารถใช้ชุดข้อมูลของคุณเป็นพื้นฐานสำหรับรายงานของตนเอง</span><span class="sxs-lookup"><span data-stu-id="0739f-106">Then other report creators can use your datasets as a basis for their own reports.</span></span> <span data-ttu-id="0739f-107">ในบทความนี้ คุณจะได้เรียนรู้วิธีการแชร์ชุดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="0739f-107">In this article, you learn how to share your datasets.</span></span> <span data-ttu-id="0739f-108">หากต้องการเรียนรู้วิธีการให้และลบการเข้าถึงชุดข้อมูลที่คุณแชร์ กรุณาอ่านเกี่ยวกับ[สิทธิ์ในการสร้าง](service-datasets-build-permissions.md)</span><span class="sxs-lookup"><span data-stu-id="0739f-108">To learn how to give and remove access to your shared datasets, read about the [Build permission](service-datasets-build-permissions.md).</span></span>

## <a name="steps-to-sharing-your-dataset"></a><span data-ttu-id="0739f-109">ขั้นตอนการแชร์ชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0739f-109">Steps to sharing your dataset</span></span>

1. <span data-ttu-id="0739f-110">คุณต้องเริ่มต้นโดยการสร้างไฟล์.pbix ด้วยแบบจำลองข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="0739f-110">You start by creating a .pbix file with a data model in Power BI Desktop.</span></span> <span data-ttu-id="0739f-111">หากคุณวางแผนที่จะเสนอชุดข้อมูลนี้ให้ผู้อื่นสร้างรายงาน คุณอาจไม่ได้ออกแบบรายงานในไฟล์. pbix</span><span class="sxs-lookup"><span data-stu-id="0739f-111">If you're planning to offer this dataset for others to build reports, you may not even design a report in the .pbix file.</span></span>

    <span data-ttu-id="0739f-112">แนวทางปฏิบัติที่ดีที่สุดคือการบันทึกไฟล์.pbix ไว้ใน Microsoft 365 Group</span><span class="sxs-lookup"><span data-stu-id="0739f-112">A best practice is to save the .pbix file to a Microsoft 365 group.</span></span>

1. <span data-ttu-id="0739f-113">เผยแพร่ไฟล์.pbix ไปยัง[ประสบการณ์การใช้งานพื้นที่ทำงานใหม่](../collaborate-share/service-create-the-new-workspaces.md)ในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="0739f-113">Publish the .pbix file to a [new workspace experience](../collaborate-share/service-create-the-new-workspaces.md) in the Power BI service.</span></span>
    
    <span data-ttu-id="0739f-114">แล้วสมาชิกอื่น ๆ ในพื้นที่ทำงานนี้จะสามารถสร้างรายงานในพื้นที่ทำงานอื่น ๆ โดยยึดตามชุดข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="0739f-114">Already, other members of this workspace can create reports in other workspaces based on this dataset.</span></span> <span data-ttu-id="0739f-115">ใช้ตัวเลือกจัดการสิทธิ์บนชุดข้อมูลในรายการเนื้อหาพื้นที่ทำงานให้ผู้ใช้เพิ่มเติมในการเข้าถึงชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0739f-115">Use the Manage Permissions option on the dataset in the workspace content list give additional users access to the dataset.</span></span> 

1. <span data-ttu-id="0739f-116">คุณยังสามารถ[เผยแพร่แอป](../collaborate-share/service-create-distribute-apps.md)จากพื้นที่ทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="0739f-116">You can also [publish an app](../collaborate-share/service-create-distribute-apps.md) from this workspace.</span></span> <span data-ttu-id="0739f-117">เมื่อคุณเช่นนั้น บนหน้า **สิทธิ** คุณสามารถระบุได้ว่าใครมีสิทธิและสามารถทำอะไรได้บ้าง</span><span class="sxs-lookup"><span data-stu-id="0739f-117">When you do, on the **Permissions** page, you specify who has permissions and what they can do.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0739f-118">หากคุณเลือก **ทั้งองค์กร** จะไม่มีผู้ใดในองค์กรจะได้รับสิทธิ์ในการสร้าง</span><span class="sxs-lookup"><span data-stu-id="0739f-118">If you select **Entire organization**, then no one in the organization will have Build permission.</span></span> <span data-ttu-id="0739f-119">ปัญหานี้เป็นที่รู้จักกันแล้ว</span><span class="sxs-lookup"><span data-stu-id="0739f-119">This issue is already known.</span></span> <span data-ttu-id="0739f-120">ให้ระบุอยู่อีเมลใน **เฉพาะบุคคลหรือกลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="0739f-120">Instead, specify email addresses in **Specific individuals or groups**.</span></span>  <span data-ttu-id="0739f-121">หากคุณต้องการให้ทั้งองค์กรได้รับสิทธิ์ในการสร้าง กรุณาระบุนามแฝงของอีเมลสำหรับทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="0739f-121">If you want your entire organization to have Build permission, specify an email alias for the entire organization.</span></span>

    ![ตั้งค่าการอนุญาตของแอป](media/service-datasets-build-permissions/power-bi-dataset-app-permission-new-look.png)

1. <span data-ttu-id="0739f-123">เลือก **เผยแพร่แอป** หรือ **อัปเดตแอป** ถ้ามีการเผยแพร่อยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="0739f-123">Select **Publish app**, or **Update app** if it's already published.</span></span>

## <a name="track-your-dataset-usage"></a><span data-ttu-id="0739f-124">ติดตามการใช้งานชุดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="0739f-124">Track your dataset usage</span></span>

<span data-ttu-id="0739f-125">เมื่อคุณมีชุดข้อมูลที่ใช้ร่วมกันในพื้นที่ทำงานของคุณ คุณอาจจำเป็นต้องทราบว่ารายงานใดในพื้นที่ทำงานอื่น ๆ ที่ใช้ชุดข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="0739f-125">When you have a shared dataset in your workspace, you may need to know what reports in other workspaces are based on it.</span></span>

1. <span data-ttu-id="0739f-126">ในมุมมองรายการชุดข้อมูล เลือก **มุมมองที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="0739f-126">In the Datasets list view, select **View related**.</span></span>

    ![ดูไอคอนที่เกี่ยวข้อง](media/service-datasets-build-permissions/power-bi-dataset-view-related-to-dataset.png)

1. <span data-ttu-id="0739f-128">กล่องโต้ตอบ **เนื้อหาที่เกี่ยวข้อง** จะแสดงรายการที่เกี่ยวข้องทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0739f-128">The **Related content** dialog box shows all related items.</span></span> <span data-ttu-id="0739f-129">ในรายการนี้ คุณจะเห็นรายการที่เกี่ยวข้องในพื้นที่ทำงานนี้ และใน **พื้นที่ทำงานอื่น ๆ**</span><span class="sxs-lookup"><span data-stu-id="0739f-129">In this list, you see the related items in this workspace and in **Other workspaces**.</span></span>
 
    ![กล่องโต้ตอบเนื้อหาที่เกี่ยวข้อง](media/service-datasets-build-permissions/power-bi-dataset-related-workspaces.png)

## <a name="limitations-and-considerations"></a><span data-ttu-id="0739f-131">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="0739f-131">Limitations and considerations</span></span>
<span data-ttu-id="0739f-132">สิ่งที่ควรทราบเกี่ยวกับการแชร์ชุดข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="0739f-132">Things to keep in mind about sharing datasets:</span></span>

* <span data-ttu-id="0739f-133">เมื่อคุณแชร์ชุดข้อมูลโดยการจัดการสิทธิ์ โดยการแชร์รายงานหรือแดชบอร์ด หรือโดยการเผยแพร่แอป แสดงว่าคุณอนุญาตให้เข้าถึงชุดข้อมูลทั้งหมด เว้นแต่[การรักษาความปลอดภัยระดับแถว (RLS)](../admin/service-admin-rls.md) จะจำกัดการเข้าถึงของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="0739f-133">When you share a dataset by managing permissions, by sharing reports or dashboards, or by publishing an app, you're granting access to the entire dataset unless [row-level security (RLS)](../admin/service-admin-rls.md) limits their access.</span></span> <span data-ttu-id="0739f-134">ผู้เขียนรายงานอาจใช้ความสามารถที่กำหนดประสบการณ์ผู้ใช้เมื่อดูหรือโต้ตอบกับรายงาน เช่น การซ่อนคอลัมน์ การจำกัดการดำเนินงานในวิชวล และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="0739f-134">Report authors may use capabilities that customize user experiences when viewing or interacting with reports, for example hiding columns, limiting the actions on visuals, and others.</span></span> <span data-ttu-id="0739f-135">ประสบการณ์ผู้ใช้ที่กำหนดเองเหล่านี้ไม่จำกัดสิ่งที่ผู้ใช้สามารถเข้าถึงข้อมูลในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0739f-135">These customized user experience do not restrict what data users can access in the dataset.</span></span> <span data-ttu-id="0739f-136">ใช้ [การรักษาความปลอดภัยระดับแถว (RLS)](../admin/service-admin-rls.md) ในชุดข้อมูลเพื่อให้ข้อมูลประจำตัวของแต่ละบุคคลกำหนดว่าข้อมูลใดที่พวกเขาสามารถเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="0739f-136">Use [row-level security (RLS)](../admin/service-admin-rls.md) in the dataset so that each person's credentials determine which data they can access.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0739f-137">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="0739f-137">Next steps</span></span>

- [<span data-ttu-id="0739f-138">ใช้ชุดข้อมูลทั่วทั้งพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="0739f-138">Use datasets across workspaces</span></span>](service-datasets-across-workspaces.md)
- <span data-ttu-id="0739f-139">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0739f-139">Questions?</span></span> [<span data-ttu-id="0739f-140">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="0739f-140">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
