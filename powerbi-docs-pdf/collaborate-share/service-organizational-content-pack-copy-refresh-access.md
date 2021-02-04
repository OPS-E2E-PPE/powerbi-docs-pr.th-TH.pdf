---
title: 'ชุดเนื้อหาระดับองค์กร: เข้าถึงและคัดลอก'
description: อ่านเกี่ยวกับการสร้างสำเนาและการแก้ไขปัญหาการเข้าถึงชุดเนื้อหาระดับองค์กรใน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: lukaszp, kayu
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 08/02/2018
LocalizationGroup: Share your work
ms.openlocfilehash: eccc60c4f26502ea2249c378efbdb910bd7c8a30
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96406744"
---
# <a name="organizational-content-packs-copy-refresh-and-get-access"></a><span data-ttu-id="4f82f-103">ชุดเนื้อหาระดับองค์กร: คัดลอก รีเฟรช และเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="4f82f-103">Organizational content packs: Copy, refresh, and get access</span></span>

<span data-ttu-id="4f82f-104">เมื่อมีชุดเนื้อหาระดับองค์กรการเผยแพร่ ผู้รับทั้งหมดดูแดชบอร์ รายงาน เวิร์กบุ๊ก Excel ชุดข้อมูล และข้อมูล (ยกเว้นแหล่งข้อมูลของ SQL Server Analysis Services (SSAS))เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="4f82f-104">When an organizational content pack is published, all recipients see the same dashboard, reports, Excel workbooks, datasets, and data (unless it's a SQL Server Analysis Services (SSAS) data source).</span></span>  <span data-ttu-id="4f82f-105">[ผู้สร้างชุดเนื้อหาเท่านั้นที่สามารถแก้ไข และประกาศ](service-organizational-content-pack-manage-update-delete.md)ชุดเนื้อหาได้</span><span class="sxs-lookup"><span data-stu-id="4f82f-105">[Only the content pack creator can edit and republish](service-organizational-content-pack-manage-update-delete.md) the content pack.</span></span>  <span data-ttu-id="4f82f-106">อย่างไรก็ตาม ผู้รับทั้งหมดสามารถบันทึกสำเนาของชุดเนื้อหาที่สามารถ live ควบคู่ไปกับต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="4f82f-106">However, all recipients can save a copy of the content pack that can live alongside the original.</span></span>

<span data-ttu-id="4f82f-107">กำลังสร้างชุดเนื้อหาที่จะแตกต่างจากการแชร์แดชบอร์ดหรือการทำงานร่วมกันบนชุดเนื้อหาเหล่านั้นในกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="4f82f-107">Creating content packs is different from sharing dashboards or collaborating on them in a group.</span></span> <span data-ttu-id="4f82f-108">อ่าน[ฉันควรทำงานร่วมกันและแชร์แดชบอร์ดและรายงานอย่างไร](service-how-to-collaborate-distribute-dashboards-reports.md) เพื่อตัดสินใจเลือกตัวเลือกที่ดีที่สุดสำหรับสถานการณ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="4f82f-108">Read [How should I collaborate on and share dashboards and reports?](service-how-to-collaborate-distribute-dashboards-reports.md) to decide on the best option for your situation.</span></span>

> [!NOTE]
> <span data-ttu-id="4f82f-109">คุณไม่สามารถสร้างหรือติดตั้งชุดเนื้อหาขององค์กรในประสบการณ์ในพื้นที่ทำงานใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="4f82f-109">You can't create or install organizational content packs in the new workspace experiences.</span></span> <span data-ttu-id="4f82f-110">ตอนนี้ คือเวลาดีที่จะอัปเกรดชุดเนื้อหาของคุณไปยังแอป ถ้าคุณยังไม่ได้เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="4f82f-110">Now is a good time to upgrade your content packs to apps, if you haven't started yet.</span></span> <span data-ttu-id="4f82f-111">เรียนรู้[เพิ่มเติมเกี่ยวกับการใช้งานพื้นที่ทำงานใหม่](service-create-the-new-workspaces.md)</span><span class="sxs-lookup"><span data-stu-id="4f82f-111">Learn [more about the new workspace experience](service-create-the-new-workspaces.md).</span></span>
>

## <a name="create-a-copy-of-an-organizational-content-pack"></a><span data-ttu-id="4f82f-112">สร้างสำเนาของข้อแพ็คเนื้อหาขององค์กร</span><span class="sxs-lookup"><span data-stu-id="4f82f-112">Create a copy of an organizational content pack</span></span>
<span data-ttu-id="4f82f-113">สร้างสำเนาของคุณเองของชุดเนื้อหา ที่ผู้อื่นไม่สามารถมองเห็น</span><span class="sxs-lookup"><span data-stu-id="4f82f-113">Create your own copy of the content pack, not visible to others.</span></span>

1. <span data-ttu-id="4f82f-114">เลือก **ตัวเลือกเพิ่มเติม** (...) ที่อยู่ถัดจากแดชบอร์ดชุดเนื้อหา > ทำสำเนา</span><span class="sxs-lookup"><span data-stu-id="4f82f-114">Select **More options** (...) next to the content pack dashboard > Make a copy.</span></span>

    ![ภาพหน้าจอของกล่องโต้ตอบสำหรับตัวเลือกเพิ่มเติม](media/service-organizational-content-pack-copy-refresh-access/power-bi-create-copy-organizational-content-pack.png)
2. <span data-ttu-id="4f82f-116">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="4f82f-116">Select **Save**.</span></span>  

<span data-ttu-id="4f82f-117">ในตอนนี้คุณมีสำเนาที่คุณสามารถเปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="4f82f-117">Now you have a copy that you can change.</span></span> <span data-ttu-id="4f82f-118">บุคคลอื่นจะเห็นการเปลี่ยนแปลงที่คุณทำ</span><span class="sxs-lookup"><span data-stu-id="4f82f-118">Nobody else will see changes you make.</span></span>

> [!NOTE]
> <span data-ttu-id="4f82f-119">ก่อนหน้านี้ แต่ละครั้งที่คุณติดตั้งชุดเนื้อหาหรือสร้างสำเนา หนึ่งชุดข้อมูลใหม่จะปรากฏในรายการเนื้อหาพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="4f82f-119">Previously, each time you installed a content pack or created a copy one, a new dataset would appear in the workspace content list.</span></span> <span data-ttu-id="4f82f-120">การอัปเดตล่าสุดประยุกต์ประสบการณ์การใช้งานเพื่อแสดงเพียงหนึ่งรายการโดยใช้ไอคอนอ้างอิงชุดข้อมูลใหม่:</span><span class="sxs-lookup"><span data-stu-id="4f82f-120">A recent update simplified the experience to show just one item using the new referenced dataset icon:</span></span>
>
> ![ฐานข้อมูลที่มีไอคอนลิงก์](media/service-organizational-content-pack-copy-refresh-access/power-bi-dataset-reference-icon.png)
>

## <a name="help--i-can-no-longer-access-the-content-pack"></a><span data-ttu-id="4f82f-122">ความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="4f82f-122">Help!</span></span>  <span data-ttu-id="4f82f-123">ฉันไม่สามารถเข้าถึงชุดเนื้อหาได้</span><span class="sxs-lookup"><span data-stu-id="4f82f-123">I can no longer access the content pack</span></span>
<span data-ttu-id="4f82f-124">ซึ่งสามารถเกิดขึ้นได้จากสาเหตุหลายประการ</span><span class="sxs-lookup"><span data-stu-id="4f82f-124">This can happen for several reasons:</span></span>

* <span data-ttu-id="4f82f-125">**เปลี่ยนแปลงการเป็นสมาชิก**:  ชุดเนื้อหาถูกเผยแพร่ไปยังกลุ่มการกระจายอีเมล กลุ่มความปลอดภัย และ [กลุ่ม Power BI ที่อ้างอิงจาก Microsoft 365](https://support.office.com/article/Create-a-group-in-Office-365-7124dc4c-1de9-40d4-b096-e8add19209e9)</span><span class="sxs-lookup"><span data-stu-id="4f82f-125">**Membership changes**:  Content packs are published to email distribution groups, security groups, and [Power BI groups based on Microsoft 365](https://support.office.com/article/Create-a-group-in-Office-365-7124dc4c-1de9-40d4-b096-e8add19209e9).</span></span>  <span data-ttu-id="4f82f-126">ถ้าคุณจะถูกลบออกจากกลุ่ม คุณจะไม่สามารถเข้าถึงชุดเนื้อหาได้</span><span class="sxs-lookup"><span data-stu-id="4f82f-126">If you are removed from the group, you will no longer have access to the content pack.</span></span>
* <span data-ttu-id="4f82f-127">**เปลี่ยนแปลงการเผยแพร่** ผู้สร้างแพคเนื้อหาเปลี่ยนแปลงการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="4f82f-127">**Distribution changes**: The content pack creator changes the distribution.</span></span> <span data-ttu-id="4f82f-128">ตัวอย่างเช่น ถ้าชุดเนื้อหานี้ถูกเผยแพร่ครั้งแรกทั่วทั้งองค์กร แต่ผู้สร้างเผยแพร่อีกครั้งให้กับผู้ชมที่มีขนาดเล็กกว่า คุณอาจไม่ถูกรวมอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="4f82f-128">For example, if the content pack was originally published to the entire organization but the creator republished it to a smaller audience, you may no longer be included.</span></span>
* <span data-ttu-id="4f82f-129">**เปลี่ยนแปลงการตั้งค่าความปลอดภัย**: ถ้าแดชบอร์ดและรายงานที่เชื่อมต่อกับแหล่งข้อมูล SSAS ภายในองค์กร และการเปลี่ยนแปลงการตั้งค่าความปลอดภัย อาจสามารถเพิกถอนสิทธิ์ของคุณในเซิร์ฟเวอร์ได้</span><span class="sxs-lookup"><span data-stu-id="4f82f-129">**Security settings changes**: If the dashboard and reports connect to on-premises SSAS data sources and changes are made to the security settings, your permissions to that server may be revoked.</span></span>

## <a name="how-are-organizational-content-packs-refreshed"></a><span data-ttu-id="4f82f-130">รีเฟรชชุดเนื้อหาระดับองค์กรทำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="4f82f-130">How are organizational content packs refreshed?</span></span>
<span data-ttu-id="4f82f-131">เมื่อมีการสร้างชุดเนื้อหา การตั้งค่าการรีเฟรชจะถูกสืบทอดกับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4f82f-131">When the content pack is created, the refresh settings are inherited with the dataset.</span></span>  <span data-ttu-id="4f82f-132">เมื่อคุณสร้างสำเนาชุดเนื้อหา เวอร์ชันใหม่ยังมีลิงก์ไปยังชุดข้อมูลต้นฉบับและกำหนดการการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="4f82f-132">When you create a copy of the content pack, the new version retains its link to the original dataset and its refresh schedule.</span></span>

<span data-ttu-id="4f82f-133">ดู[จัดการ ปรับปรุง และลบชุดเนื้อหาระดับองค์กร](service-organizational-content-pack-manage-update-delete.md)</span><span class="sxs-lookup"><span data-stu-id="4f82f-133">See [Manage, update, and delete organizational content packs](service-organizational-content-pack-manage-update-delete.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="4f82f-134">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4f82f-134">Next steps</span></span>
* [<span data-ttu-id="4f82f-135">แนะนำชุดเนื้อหาองค์กร</span><span class="sxs-lookup"><span data-stu-id="4f82f-135">Introduction to organizational content packs</span></span>](service-organizational-content-pack-introduction.md)
* [<span data-ttu-id="4f82f-136">สร้างกลุ่มใน Power BI</span><span class="sxs-lookup"><span data-stu-id="4f82f-136">Create a group in Power BI</span></span>](service-create-distribute-apps.md)
* <span data-ttu-id="4f82f-137">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4f82f-137">More questions?</span></span> [<span data-ttu-id="4f82f-138">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="4f82f-138">Try the Power BI Community</span></span>](https://community.powerbi.com/)
