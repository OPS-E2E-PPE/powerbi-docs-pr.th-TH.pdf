---
title: จัดการพื้นที่ทำงานของคุณใน Power BI และ Microsoft 365
description: พื้นที่ทำงานใน Power BI เป็นประสบการณ์การทำงานร่วมกันภายใน Microsoft 365 Group จัดการพื้นที่ทำงานใน Power BI และใน Microsoft 365 ด้วย
author: maggiesMSFT
ms.author: maggies
ms.reviewer: lukasz
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 03/02/2020
LocalizationGroup: Share your work
ms.openlocfilehash: bd1a5b0aaf694f41fdbfe4764e77c1138a57b082
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96407043"
---
# <a name="manage-your-workspace-in-power-bi-and-microsoft-365"></a><span data-ttu-id="24e85-104">จัดการพื้นที่ทำงานของคุณใน Power BI และ Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="24e85-104">Manage your workspace in Power BI and Microsoft 365</span></span>

<span data-ttu-id="24e85-105">ในฐานะผู้สร้างหรือผู้ดูแลระบบของ[พื้นที่ทำงานใน Power BI](service-create-distribute-apps.md)หรือใน Microsoft 365 คุณสามารถจัดการลักษณะบางส่วนของพื้นที่ทำงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="24e85-105">As creator or admin of a [workspace in Power BI](service-create-distribute-apps.md) or in Microsoft 365, you manage some aspects of the workspace in Power BI.</span></span> <span data-ttu-id="24e85-106">ลักษณะอื่น ๆ ที่คุณจัดการใน Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="24e85-106">Other aspects you manage in Microsoft 365.</span></span>

> [!NOTE]
> <span data-ttu-id="24e85-107">ประสบการณ์พื้นที่ทำงานใหม่จะเปลี่ยนความสัมพันธ์ระหว่างพื้นที่ทำงาน Power BI และ Microsoft 365 Group</span><span class="sxs-lookup"><span data-stu-id="24e85-107">The new workspace experience changes the relationship between Power BI workspaces and Microsoft 365 groups.</span></span> <span data-ttu-id="24e85-108">คุณจะไม่สามารถสร้าง Microsoft 365 Group โดยอัตโนมัติทุกครั้งที่คุณสร้างพื้นที่ทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="24e85-108">You aren't automatically creating a Microsoft 365 group every time you create one of the new workspaces.</span></span> <span data-ttu-id="24e85-109">อ่านเกี่ยวกับ [สร้างพื้นที่ทำงานใหม่](service-create-the-new-workspaces.md)</span><span class="sxs-lookup"><span data-stu-id="24e85-109">Read about [creating the new workspaces](service-create-the-new-workspaces.md).</span></span>

<span data-ttu-id="24e85-110">ใน **Power BI** คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="24e85-110">In **Power BI** you can:</span></span>

* <span data-ttu-id="24e85-111">เพิ่มหรือลบสมาชิกพื้นที่ทำงาน รวมถึงการทำให้สมาชิกพื้นที่ทำงานเป็นผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="24e85-111">Add or remove workspace members, including making a workspace member an admin.</span></span>
* <span data-ttu-id="24e85-112">แก้ไขชื่อพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="24e85-112">Edit the workspace name.</span></span>
* <span data-ttu-id="24e85-113">ลบพื้นที่ทำงาน ซึ่งจะลบ Microsoft 365 Group ออกด้วย</span><span class="sxs-lookup"><span data-stu-id="24e85-113">Delete the workspace, which also deletes the Microsoft 365 group.</span></span>

<span data-ttu-id="24e85-114">ใน **Microsoft 365** คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="24e85-114">In **Microsoft 365** you can:</span></span>

* <span data-ttu-id="24e85-115">เพิ่มหรือลบสมาชิกกลุ่มพื้นที่ทำงาน รวมถึงการทำให้สมาชิกเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="24e85-115">Add or remove your workspace's group members, including making a member an owner.</span></span>
* <span data-ttu-id="24e85-116">แก้ไขชื่อกลุ่ม รูปภาพ คำอธิบาย และการตั้งค่าอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="24e85-116">Edit the group name, image, description, and other settings.</span></span>
* <span data-ttu-id="24e85-117">ดูที่อยู่อีเมลของกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="24e85-117">See the group email address.</span></span>
* <span data-ttu-id="24e85-118">ลบกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="24e85-118">Delete the group.</span></span>

<span data-ttu-id="24e85-119">คุณจำเป็นต้องมี[สิทธิ์การใช้งาน Power BI Pro](../fundamentals/service-features-license-type.md) ในการเป็นผู้ดูแลระบบหรือสมาชิกของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="24e85-119">You need a [Power BI Pro license](../fundamentals/service-features-license-type.md) to be an admin or member of a workspace.</span></span> <span data-ttu-id="24e85-120">ผู้ใช้แอปของคุณต้องมีสิทธิ์ใช้งาน Power BI Pro เช่นกัน ยกเว้นว่าพื้นที่ทำงานของคุณจะอยู่ในความจุ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="24e85-120">Your app users need a Power BI Pro license, too, unless your workspace is in a Power BI Premium capacity.</span></span> <span data-ttu-id="24e85-121">อ่าน[Power BI Premium คืออะไร](../admin/service-premium-what-is.md)สำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="24e85-121">Read [What is Power BI Premium?](../admin/service-premium-what-is.md) for details.</span></span>

## <a name="edit-your-workspace-in-power-bi"></a><span data-ttu-id="24e85-122">แก้ไขพื้นที่ทำงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="24e85-122">Edit your workspace in Power BI</span></span>

1. <span data-ttu-id="24e85-123">ในบริการของ Power BI เลือกลูกศรที่อยู่ถัดจาก **พื้นที่ทำงาน** > เลือก **ตัวเลือกเพิ่มเติม** (...) ถัดจากชื่อพื้นที่ทำงานของคุณ > **แก้ไขพื้นที่ทำงานนี้**</span><span class="sxs-lookup"><span data-stu-id="24e85-123">In the Power BI service, select the arrow next to **Workspaces** > select **More options** (...) next to your workspace name > **Edit this workspace**.</span></span>

   ![สกรีนช็อตแสดงหน้าแรกของ Power BI พร้อมพื้นที่ทำงานที่เลือก และแก้ไขพื้นที่ทำงานที่เลือกจากเมนูตัวเลือกเพิ่มเติม](media/service-manage-app-workspace-in-power-bi-and-office-365/power-bi-app-ellipsis.png)

   > [!NOTE]
   > <span data-ttu-id="24e85-125">คุณเห็นเฉพาะ **แก้ไขพื้นที่ทำงานนี้** ถ้าคุณเป็นผู้ดูแลระบบพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="24e85-125">You only see **Edit this workspace** if you’re a workspace admin.</span></span>

1. <span data-ttu-id="24e85-126">ที่นี่คุณสามารถเปลี่ยนชื่อพื้นที่ทำงาน เพิ่ม หรือลบสมาชิกออก หรือลบพื้นที่ทำงานได้</span><span class="sxs-lookup"><span data-stu-id="24e85-126">Here you can rename the workspace, add or remove members, or delete the workspace.</span></span>

   ![แก้ไขพื้นที่ทำงานของกล่องโต้ตอบ](media/service-manage-app-workspace-in-power-bi-and-office-365/power-bi-app-edit-workspace.png)

1. <span data-ttu-id="24e85-128">เลือก **บันทึก** หรือ **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="24e85-128">Select **Save** or **Cancel**.</span></span>

## <a name="edit-power-bi-workspace-properties-in-microsoft-365"></a><span data-ttu-id="24e85-129">แก้ไขคุณสมบัติพื้นที่ทำงาน Power BI ใน Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="24e85-129">Edit Power BI workspace properties in Microsoft 365</span></span>

<span data-ttu-id="24e85-130">คุณยังสามารถแก้ไขลักษณะของพื้นที่ทำงานได้โดยตรงใน Outlook for Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="24e85-130">You can also edit aspects of a workspace directly in Outlook for Microsoft 365.</span></span>

### <a name="edit-the-members-of-the-workspace-group"></a><span data-ttu-id="24e85-131">แก้ไขสมาชิกของกลุ่มพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="24e85-131">Edit the members of the workspace group</span></span>

1. <span data-ttu-id="24e85-132">ในบริการของ Power BI เลือกลูกศรอยู่ถัดจาก **พื้นที่ทำงาน** > เลือก **ตัวเลือกเพิ่มเติม** (... ) ถัดจากชื่อพื้นที่ทำงานของคุณ > **สมาชิก**</span><span class="sxs-lookup"><span data-stu-id="24e85-132">In the Power BI service, select the arrow next to **Workspaces** > select **More options** (...) next to your workspace name > **Members**.</span></span>

   ![สกรีนช็อตแสดงพื้นที่ทำงาน Power BI ที่เลือก และสมาชิกที่เลือกจากเมนูตัวเลือกเพิ่มเติม](media/service-manage-app-workspace-in-power-bi-and-office-365/power-bi-app-ellipsis-members.png)

   <span data-ttu-id="24e85-134">การดำเนินการนี้จะเปิดมุมมอง Outlook for Microsoft 365 Group ของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="24e85-134">This opens the Outlook for Microsoft 365 group view of your workspace.</span></span> <span data-ttu-id="24e85-135">คุณอาจจำเป็นต้องลงชื่อเข้าใช้บัญชีขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="24e85-135">You may need to sign in to your corporate account.</span></span>

1. <span data-ttu-id="24e85-136">เลือกบทบาทถัดจากชื่อเพื่อนร่วมทีมเพื่อให้บุคคลนั้นเป็น **สมาชิก** หรือ **เจ้าของ**</span><span class="sxs-lookup"><span data-stu-id="24e85-136">Select the role next to a teammate's name to make the person a **Member** or an **Owner**.</span></span> <span data-ttu-id="24e85-137">เลือก **X** เพื่อลบบุคคลออกจากกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="24e85-137">Select the **X** to remove the person from the group.</span></span>

   ![แก้ไขกลุ่มใน Microsoft 365](media/service-manage-app-workspace-in-power-bi-and-office-365/pbi_managegroupo365.png)

### <a name="add-an-image-and-set-other-workspace-properties"></a><span data-ttu-id="24e85-139">เพิ่มรูปภาพ และตั้งค่าคุณสมบัติพื้นที่ทำงานอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="24e85-139">Add an image and set other workspace properties</span></span>

<span data-ttu-id="24e85-140">เมื่อคุณเผยแพร่แอปของคุณจากพื้นที่ทำงาน รูปภาพที่คุณเพิ่มที่นี่จะเป็นรูปภาพสำหรับแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="24e85-140">When you distribute your app from the workspace, the image you add here is the image for your app.</span></span> <span data-ttu-id="24e85-141">ดูหัวข้อ [เพิ่มรูปภาพในพื้นที่ทำงาน Microsoft 365](service-create-workspaces.md#add-an-image-to-your-microsoft-365-workspace-optional) ในบทความ **สร้างพื้นที่ทำงานใหม่**</span><span class="sxs-lookup"><span data-stu-id="24e85-141">See [Add an image to your Microsoft 365 workspace](service-create-workspaces.md#add-an-image-to-your-microsoft-365-workspace-optional) in the **Create the new workspaces** article.</span></span>

1. <span data-ttu-id="24e85-142">ในมุมมอง Outlook for Microsoft 365 ของพื้นที่ทำงาน ให้ไปที่แท็บ **เกี่ยวกับ** แล้วเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="24e85-142">In the Outlook for Microsoft 365 view of your workspace, go to the **About** tab and select **Edit**.</span></span>

    ![แก้ไขไอคอนกลุ่ม](media/service-manage-app-workspace-in-power-bi-and-office-365/pbi_editgroupo365.png)
1. <span data-ttu-id="24e85-144">คุณสามารถแก้ไขชื่อ คำอธิบาย และภาษาสำหรับการแจ้งเตือนที่เกี่ยวข้องกับกลุ่มได้</span><span class="sxs-lookup"><span data-stu-id="24e85-144">You can edit the name, description, and language for group-related notifications.</span></span> <span data-ttu-id="24e85-145">คุณยังสามารถเพิ่มรูปภาพ และตั้งค่าคุณสมบัติอื่นได้ ที่นี่</span><span class="sxs-lookup"><span data-stu-id="24e85-145">You can also add an image, and set other properties here.</span></span>

   ![แก้ไขกล่องโต้ตอบของกลุ่ม](media/service-manage-app-workspace-in-power-bi-and-office-365/pbi_editgrpo365dialog.png)

1. <span data-ttu-id="24e85-147">เลือก **บันทึก** หรือ **ละทิ้ง**</span><span class="sxs-lookup"><span data-stu-id="24e85-147">Select **Save** or **Discard**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="24e85-148">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="24e85-148">Next steps</span></span>

* [<span data-ttu-id="24e85-149">เผยแพร่แอปใน Power BI</span><span class="sxs-lookup"><span data-stu-id="24e85-149">Publish an app in Power BI</span></span>](service-create-distribute-apps.md)

* <span data-ttu-id="24e85-150">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="24e85-150">More questions?</span></span> [<span data-ttu-id="24e85-151">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="24e85-151">Try the Power BI Community</span></span>](https://community.powerbi.com/)
