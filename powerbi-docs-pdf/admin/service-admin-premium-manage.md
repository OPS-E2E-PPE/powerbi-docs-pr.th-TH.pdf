---
title: กำหนดค่าและจัดการความจุใน Power BI Premium
description: เรียนรู้วิธีการจัดการ Power BI Premium และเปิดใช้งานการเข้าถึงเนื้อหาให้ทั้งองค์กรของคุณ
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-premium
ms.topic: how-to
ms.date: 11/11/2020
LocalizationGroup: Premium
ms.openlocfilehash: 5cce18c2ec4a24b06f4cf48d5fd2b542109d70c6
ms.sourcegitcommit: cc20b476a45bccb870c9de1d0b384e2c39e25d24
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/11/2020
ms.locfileid: "94512504"
---
# <a name="configure-and-manage-capacities-in-power-bi-premium"></a><span data-ttu-id="f76db-103">กำหนดค่าและจัดการความจุใน Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="f76db-103">Configure and manage capacities in Power BI Premium</span></span>

<span data-ttu-id="f76db-104">การจัดการ Power BI Premium เกี่ยวข้องกับ การสร้าง การจัดการ และการตรวจสอบความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="f76db-104">Managing Power BI Premium involves creating, managing, and monitoring Premium capacities.</span></span> <span data-ttu-id="f76db-105">บทความนี้ให้คำแนะนำทีละขั้นตอน สำหรับภาพรวมของความจุ .ให้ดูที่[การจัดการความ](service-premium-capacity-manage.md)จุพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="f76db-105">This article provides step-by-step instructions; for an overview of capacities; see [Managing Premium capacities](service-premium-capacity-manage.md).</span></span>

<span data-ttu-id="f76db-106">เรียนรู้วิธีการจัดการ Power BI Premium และความจุ Power BI Embedded ซึ่งมีแหล่งข้อมูลเฉพาะสำหรับเนื้อหาของคุณ</span><span class="sxs-lookup"><span data-stu-id="f76db-106">Learn how to manage Power BI Premium and Power BI Embedded capacities, which provide dedicated resources for your content.</span></span>

![หน้าจอการตั้งค่าความจุ BI power](media/service-admin-premium-manage/premium-capacity-management.png)

<span data-ttu-id="f76db-108">*ความจุ* คือหัวใจสำคัญของข้อเสนอ Power BI Premium และ Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="f76db-108">*Capacity* is at the heart of the Power BI Premium and Power BI Embedded offerings.</span></span> <span data-ttu-id="f76db-109">ความจุคือชุดของทรัพยากรที่สงวนไว้สำหรับการใช้เฉพาะองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="f76db-109">It is a set of resources reserved for exclusive use by your organization.</span></span> <span data-ttu-id="f76db-110">โดยการมีค่าความจุนี้ช่วยให้คุณสามารถเผยแพร่แดชบอร์ด รายงาน และชุดข้อมูลไปยังผู้ใช้ทั่วทั้งองค์กรของคุณ โดยไม่ต้องซื้อสิทธิ์การใช้งานต่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f76db-110">Having a capacity enables you to publish dashboards, reports, and datasets to users throughout your organization without having to purchase per-user licenses for them.</span></span> <span data-ttu-id="f76db-111">นอกจากนี้ยังมีความน่าเชื่อถือ ความสอดคล้องของประสิทธิภาพการทำงานสำหรับเนื้อหาที่โฮสต์ในความจุ</span><span class="sxs-lookup"><span data-stu-id="f76db-111">It also offers dependable, consistent performance for the content hosted in capacity.</span></span> <span data-ttu-id="f76db-112">สำหรับข้อมูลเพิ่มเติม ให้ดู [อะไรคือ Power BI Premium](service-premium-what-is.md)</span><span class="sxs-lookup"><span data-stu-id="f76db-112">For more information, see [What is Power BI Premium?](service-premium-what-is.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f76db-113">Power BI Premium เพิ่งเปิดตัว Premium เวอร์ชันใหม่ชื่อ **Premium Gen2** ซึ่งกำลังอยู่ในช่วงการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f76db-113">Power BI Premium recently released a new version of Premium, called **Premium Gen2**, which is currently in preview.</span></span> <span data-ttu-id="f76db-114">Premium Gen2 จะทำให้การจัดการความจุระดับพรีเมียมง่ายขึ้นและลดค่าใช้จ่ายในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="f76db-114">Premium Gen2 will simplify the management of Premium capacities, and reduce management overhead.</span></span> <span data-ttu-id="f76db-115">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Power BI Premium Generation 2 (ตัวอย่าง)](service-premium-what-is.md#power-bi-premium-generation-2-preview)</span><span class="sxs-lookup"><span data-stu-id="f76db-115">For more information, see [Power BI Premium Generation 2 (preview)](service-premium-what-is.md#power-bi-premium-generation-2-preview).</span></span>

## <a name="manage-capacity"></a><span data-ttu-id="f76db-116">จัดการความจุ</span><span class="sxs-lookup"><span data-stu-id="f76db-116">Manage capacity</span></span>

<span data-ttu-id="f76db-117">หลังจากที่คุณได้ซื้อโหนดความจุใน Microsoft 365 แล้ว ให้คุณตั้งค่าความจุในพอร์ทัลผู้ดูแลระบบของ Power BI</span><span class="sxs-lookup"><span data-stu-id="f76db-117">After you have purchased capacity nodes in Microsoft 365, you set up the capacity in the Power BI admin portal.</span></span> <span data-ttu-id="f76db-118">คุณจัดการความจุ Power BI Premium ในส่วน **การตั้งค่าความจุ** ของพอร์ทัล</span><span class="sxs-lookup"><span data-stu-id="f76db-118">You manage Power BI Premium capacities in the **Capacity settings** section of the portal.</span></span>

![ตั้งค่าความจุในพอร์ทัลผู้ดูแล](media/service-admin-premium-manage/admin-portal-premium.png)

<span data-ttu-id="f76db-120">คุณจัดการความจุ โดยการเลือกชื่อของความจุ</span><span class="sxs-lookup"><span data-stu-id="f76db-120">You manage a capacity by selecting the name of the capacity.</span></span> <span data-ttu-id="f76db-121">ซึ่งนำคุณไปยังหน้าจอการจัดการความจุ</span><span class="sxs-lookup"><span data-stu-id="f76db-121">This takes you to the capacity management screen.</span></span>

![เลือกชื่อกำลังความจุเพื่อการเข้าถึงหน้าจอที่มอบความจุ](media/service-admin-premium-manage/capacity-assignment.png)

<span data-ttu-id="f76db-123">หากไม่ได้กำหนดพื้นที่ทำงานไว้ในความจุ คุณจะเห็นข้อความเกี่ยวกับ [การกำหนดพื้นที่ทำงานให้กับความจุ](#assign-a-workspace-to-a-capacity)</span><span class="sxs-lookup"><span data-stu-id="f76db-123">If no workspaces have been assigned to the capacity, you will see a message about [assigning a workspace to the capacity](#assign-a-workspace-to-a-capacity).</span></span>

### <a name="setting-up-a-new-capacity-power-bi-premium"></a><span data-ttu-id="f76db-124">การตั้งค่าความจุใหม่ (Power BI Premium)</span><span class="sxs-lookup"><span data-stu-id="f76db-124">Setting up a new capacity (Power BI Premium)</span></span>

<span data-ttu-id="f76db-125">พอร์ทัลของผู้ดูแลระบบแสดงจำนวน *แกนเสมือน* (v-cores) ที่คุณใช้และคุณยังมีอยู่</span><span class="sxs-lookup"><span data-stu-id="f76db-125">The admin portal shows the number of *virtual cores* (v-cores) that you have used and that you still have available.</span></span> <span data-ttu-id="f76db-126">จำนวน v-cores ทั้งหมดขึ้นอยู่กับ SKU ระดับ Premium ที่คุณซื้อ</span><span class="sxs-lookup"><span data-stu-id="f76db-126">The total number of v-cores is based on the Premium SKUs that you have purchased.</span></span> <span data-ttu-id="f76db-127">ตัวอย่างเช่น ซื้อแบบ P3 และ P2 ส่งผลให้มี 48 core ที่ใช้ได้ 32 cores จาก P3 และ 16 cores จาก P2</span><span class="sxs-lookup"><span data-stu-id="f76db-127">For example, purchasing a P3 and a P2 results in 48 available cores – 32 from the P3 and 16 from the P2.</span></span>

![v-cores ที่ใช้งานอล้วและที่มีสำหรับ Power BI Premium](media/service-admin-premium-manage/admin-portal-v-cores.png)

<span data-ttu-id="f76db-129">ถ้าคุณมี v-cores ให้ตั้งความจุใหม่ของคุณโดยทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f76db-129">If you have available v-cores, set up your new capacity by following these steps.</span></span>

1. <span data-ttu-id="f76db-130">เลือก **ตั้งค่าความจุใหม่**</span><span class="sxs-lookup"><span data-stu-id="f76db-130">Select **Set up new capacity**.</span></span>

1. <span data-ttu-id="f76db-131">ตั้งชื่อความจุของคุณ</span><span class="sxs-lookup"><span data-stu-id="f76db-131">Give your capacity a name.</span></span>

1. <span data-ttu-id="f76db-132">กำหนดว่าใครจะเป็นผู้ดูแลสำหรับความจุนี้</span><span class="sxs-lookup"><span data-stu-id="f76db-132">Define who the admin is for this capacity.</span></span>

1. <span data-ttu-id="f76db-133">เลือกขนาดของความจุ</span><span class="sxs-lookup"><span data-stu-id="f76db-133">Select your capacity size.</span></span> <span data-ttu-id="f76db-134">ตัวเลือกที่พร้อมใช้งานจะขึ้นอยู่กับจำนวน v-cores ที่คุณมี</span><span class="sxs-lookup"><span data-stu-id="f76db-134">Available options are dependent on how many available v-cores you have.</span></span> <span data-ttu-id="f76db-135">คุณไม่สามารถเลือกตัวเลือกที่มีขนาดใหญ่กว่าสิ่งที่คุณมีพร้อมใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="f76db-135">You can't select an option that is larger than what you have available.</span></span>

    ![ขนาดความจุพรีเมียมต่างๆที่พร้อมใช้งาน](media/service-admin-premium-manage/premium-capacity-size.png)

1. <span data-ttu-id="f76db-137">เลือก **ตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="f76db-137">Select **Set up**.</span></span>

    ![ตั้งค่าความจุใหม่](media/service-admin-premium-manage/set-up-capacity.png)

<span data-ttu-id="f76db-139">ผู้ดูแลความจุ รวมถึงผู้ดูแลระบบ Power BI และผู้ดูแลระบบส่วนกลาง จากนั้นดูความจุที่ระบุในพอร์ทัลผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="f76db-139">Capacity admins, as well as Power BI admins and global administrators, then see the capacity listed in the admin portal.</span></span>

### <a name="capacity-settings"></a><span data-ttu-id="f76db-140">การตั้งค่าความจุ</span><span class="sxs-lookup"><span data-stu-id="f76db-140">Capacity settings</span></span>

1. <span data-ttu-id="f76db-141">ในหน้าจอการจัดการความจุระดับพรีเมี่ยม ภายใต้ **การดำเนินการ** ให้เลือก **ไอคอนฟันเฟือง** เพื่อทบทวนและอัปเดตการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="f76db-141">In the Premium capacity management screen, under **Actions**, select the **gear icon** to review and update settings.</span></span> 

    ![การดำเนินการความจุในพื้นที่การจัดการความจุ](media/service-admin-premium-manage/capacity-actions.png)

1. <span data-ttu-id="f76db-143">คุณสามารถดูว่าใครคือผู้ดูแลระบบบริการ SKU/ขนาด ความจุของใคร ความจุของภูมิภาคใดที่อยู่ในนั้น</span><span class="sxs-lookup"><span data-stu-id="f76db-143">You can see who the service admins are, the SKU/size of the capacity, and what region the capacity is in.</span></span>

    ![การตั้งค่าความจุ](media/service-admin-premium-manage/capacity-settings.png)

1. <span data-ttu-id="f76db-145">นอกจากนี้คุณยังสามารถเปลี่ยนชื่อหรือลบความจุได้</span><span class="sxs-lookup"><span data-stu-id="f76db-145">You can also rename or delete a capacity.</span></span>

    ![ลบ และใช้ปุ่มสำหรับการตั้งค่าความจุใน Power BI Premium](media/service-admin-premium-manage/capacity-settings-delete.png)

> [!NOTE]
> <span data-ttu-id="f76db-147">คุณสามารถจัดการการตั้งค่าความจุ Power BI Embedded ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="f76db-147">Power BI Embedded capacity settings are managed in the Microsoft Azure portal.</span></span>

### <a name="change-capacity-size"></a><span data-ttu-id="f76db-148">เปลี่ยนขนาดความจุ</span><span class="sxs-lookup"><span data-stu-id="f76db-148">Change capacity size</span></span>

<span data-ttu-id="f76db-149">ผู้ดูแลระบบ Power BI และผู้ดูแลระบบส่วนกลางสามารถเปลี่ยนแปลงความจุ Power BI Premium ได้</span><span class="sxs-lookup"><span data-stu-id="f76db-149">Power BI admins and global administrators can change Power BI Premium capacity.</span></span> <span data-ttu-id="f76db-150">ผู้ดูแลความจุที่ไม่ใช่ผู้ดูแลระบบ Power BI หรือผู้ดูแลระบบส่วนกลางจะไม่มีตัวเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="f76db-150">Capacity admins who are not a Power BI admin or global administrator don't have this option.</span></span>

1. <span data-ttu-id="f76db-151">เลือก **เปลี่ยนขนาดความจุ**.</span><span class="sxs-lookup"><span data-stu-id="f76db-151">Select **Change capacity size**.</span></span>

    ![เปลี่ยนขนาดความจุ Power BI Premium](media/service-admin-premium-manage/change-capacity-size.png)

1. <span data-ttu-id="f76db-153">ในหน้าจอ **เปลี่ยนขนาดความจุ** ปรับเพิ่มหรือปรับลดความจุของคุณตามความเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="f76db-153">On the **Change capacity size** screen upgrade or downgrade your capacity as appropriate.</span></span>

    ![ดร๊อปดาวน์เปลี่ยนขนาดความจุ Power BI Premium](media/service-admin-premium-manage/change-capacity-size2.png)

    <span data-ttu-id="f76db-155">ผู้ดูแลมีอิสระที่จะสร้าง การปรับขนาด และลบโหนด ดังนั้นตราบใดที่พวกเขามีจำนวน v-cores</span><span class="sxs-lookup"><span data-stu-id="f76db-155">Administrators are free to create, resize and delete nodes, so long as they have the requisite number of v-cores.</span></span>

    <span data-ttu-id="f76db-156">คุณไม่สามารถปรับลด P SKU ให้เป็น EM SKUs ได้</span><span class="sxs-lookup"><span data-stu-id="f76db-156">P SKUs cannot be downgraded to EM SKUs.</span></span> <span data-ttu-id="f76db-157">คุณสามารถเลื่อนเมาส์ไปวางเหนือตัวเลือกที่ถูกปิดใช้งานเพื่อดูคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f76db-157">You can hover over any disabled options to see an explanation.</span></span>



> [!IMPORTANT]
> <span data-ttu-id="f76db-158">ถ้าความจุ Power BI Premium ของคุณกำลังประสบปัญหาการใช้ทรัพยากรสูงจนส่งผลให้เกิดปัญหาด้านประสิทธิภาพการทำงานหรือความมั่นคง คุณสามารถรับอีเมลแจ้งเตือนเพื่อทราบปัญหาและแก้ไขปัญหาได้</span><span class="sxs-lookup"><span data-stu-id="f76db-158">If your Power BI Premium capacity is experiencing high resource usage, resulting in performance or reliability issues, you can receive notification emails to identify and resolve the issue.</span></span> <span data-ttu-id="f76db-159">คุณสามารถศึกษาข้อมูลเพิ่มเติมได้ที่[ความจุและการแจ้งเตือนความมั่นคง](service-interruption-notifications.md#capacity-and-reliability-notifications)</span><span class="sxs-lookup"><span data-stu-id="f76db-159">See [capacity and reliability notifications](service-interruption-notifications.md#capacity-and-reliability-notifications) for more information.</span></span>


### <a name="manage-user-permissions"></a><span data-ttu-id="f76db-160">จัดการสิทธิ์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f76db-160">Manage user permissions</span></span>

<span data-ttu-id="f76db-161">คุณสามารถมอบหมายผู้ดูแลความจุเพิ่มเติม และกำหนดผู้ใช้ที่มีสิทธิ์ *การกำหนดความจุ* ได้</span><span class="sxs-lookup"><span data-stu-id="f76db-161">You can assign additional capacity admins, and assign users that have *capacity assignment* permissions.</span></span> <span data-ttu-id="f76db-162">ผู้ใช้ที่มีสิทธิ์ในการกำหนดอาจกำหนดพื้นที่ทำงานไปยังความจุใดความจุหนึ่ง ถ้าพวกเขาเป็นผู้ดูแลระบบของพื้นที่ทำงานนั้น</span><span class="sxs-lookup"><span data-stu-id="f76db-162">Users that have assignment permissions can assign a workspace to a capacity if they are an admin of that workspace.</span></span> <span data-ttu-id="f76db-163">พวกเขายังสามารถกำหนด *My Workspace* ส่วนบุคคลของพวกเขาให้ความจุได้</span><span class="sxs-lookup"><span data-stu-id="f76db-163">They can also assign their personal *My Workspace* to the capacity.</span></span> <span data-ttu-id="f76db-164">ผู้ใช้ที่มีสิทธิ์ในการกำหนดจะไม่เข้าถึงพอร์ทัลผู้ดูแล</span><span class="sxs-lookup"><span data-stu-id="f76db-164">Users with assignment permissions do not have access to the admin portal.</span></span>

> [!NOTE]
> <span data-ttu-id="f76db-165">สำหรับ Power BI Embedded ผู้ดูแลความจุจะถูกกำหนดในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="f76db-165">For Power BI Embedded, capacity admins are defined in the Microsoft Azure portal.</span></span>

<span data-ttu-id="f76db-166">ภายใต้หน้าจอ **สิทธิ์ผู้ใช้** ขยายตัวเลือก **ผู้ใช้ที่ มีสิทธิ์ในการกำหนด** จากนั้นเพิ่มผู้ใช้หรือกลุ่มตามความเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="f76db-166">Under **User permissions**, expand **Users with assignment permissions**, then add users or groups as appropriate.</span></span>

![สิทธิ์ผู้ใช้ของความจุ](media/service-admin-premium-manage/capacity-user-permissions2.png)

## <a name="assign-a-workspace-to-a-capacity"></a><span data-ttu-id="f76db-168">กำหนดพื้นที่ทำงานของแอปไปยังความจุ</span><span class="sxs-lookup"><span data-stu-id="f76db-168">Assign a workspace to a capacity</span></span>

<span data-ttu-id="f76db-169">มีสองวิธีในการกำหนดพื้นที่ทำงานไปยังความจุ: ในพอร์ทัลผู้ดูแลระบบ และจากพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f76db-169">There are two ways to assign a workspace to a capacity: in the admin portal; and from a workspace.</span></span>

### <a name="assign-from-the-admin-portal"></a><span data-ttu-id="f76db-170">กำหนดจากพอร์ทัลผู้ดูแล</span><span class="sxs-lookup"><span data-stu-id="f76db-170">Assign from the admin portal</span></span>

<span data-ttu-id="f76db-171">ผู้ดูแลความจุ พร้อมกับผู้ดูแลระบบ Power BI และผู้ดูแลระบบส่วนกลาง สามารถกำหนดพื้นที่ทำงานที่ละหลาย ๆ ตัว ในส่วนการจัดการความจุพรีเมียมของพอร์ทัลผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="f76db-171">Capacity admins, along with Power BI admins and global administrators, can bulk assign workspaces in the premium capacity management section of the admin portal.</span></span> <span data-ttu-id="f76db-172">เมื่อคุณจัดการความจุ คุณจะเห็นส่วน **พื้นที่ทำงาน** ที่ช่วยให้คุณสามารถกำหนดพื้นที่ทำงานได้</span><span class="sxs-lookup"><span data-stu-id="f76db-172">When you manage a capacity, you see a **Workspaces** section that allows you to assign workspaces.</span></span>

![พื้นที่ทำงานกำหนดพื้นที่ของการจัดการความจุ](media/service-admin-premium-manage/capacity-manage-workspaces.png)

1. <span data-ttu-id="f76db-174">เลือก **กำหนดพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="f76db-174">Select **Assign workspaces**.</span></span> <span data-ttu-id="f76db-175">ตัวเลือกนี้จะพร้อมใช้งานในหลายตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="f76db-175">This option is available in multiple places.</span></span>

1. <span data-ttu-id="f76db-176">เลือกตัวเลือกสำหรับ **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="f76db-176">Select an option for **Apply to**.</span></span>

    ![กำหนดพื้นที่ทำงาน](media/service-admin-premium-manage/assign-workspaces.png)

   | <span data-ttu-id="f76db-178">การเลือก</span><span class="sxs-lookup"><span data-stu-id="f76db-178">Selection</span></span> | <span data-ttu-id="f76db-179">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f76db-179">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f76db-180">**พื้นที่ทำงานโดยผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="f76db-180">**Workspaces by users**</span></span> | <span data-ttu-id="f76db-181">เมื่อคุณกำหนดพื้นที่ทำงาน ตามผู้ใช้หรือตามกลุ่ม พื้นที่ทำงานทั้งหมดที่ผู้ใช้เหล่านั้นเป็นเจ้าของ จะถูกกำหนดให้กับความจุพรีเมียม รวมถึงพื้นที่ทำงานส่วนบุคคลของผู้ใช้ด้วย</span><span class="sxs-lookup"><span data-stu-id="f76db-181">When you assign workspaces by user, or group, all the workspaces owned by those users are assigned to Premium capacity, including the user's personal workspace.</span></span> <span data-ttu-id="f76db-182">ลูกค้าที่ถูกบอกจะถูกำหนดการอนุญาตของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f76db-182">Said users automatically get workspace assignment permissions.</span></span><br><span data-ttu-id="f76db-183">ซึ่งรวมถึงพื้นที่ทำงานที่ถูกกำหนดให้กับความจุอื่น</span><span class="sxs-lookup"><span data-stu-id="f76db-183">This includes workspaces already assigned to a different capacity.</span></span> |
   | <span data-ttu-id="f76db-184">**พื้นที่ทำงานเฉพาะ**</span><span class="sxs-lookup"><span data-stu-id="f76db-184">**Specific workspaces**</span></span> | <span data-ttu-id="f76db-185">ป้อนชื่อของพื้นที่ทำงานเฉพาะเมื่อต้องกำหนดความจุที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f76db-185">Enter the name of a specific workspace to assign to the selected capacity.</span></span> |
   | <span data-ttu-id="f76db-186">**พื้นที่ทำงานของทั้งองค์กร**</span><span class="sxs-lookup"><span data-stu-id="f76db-186">**The entire organization's workspaces**</span></span> | <span data-ttu-id="f76db-187">การกำหนดพื้นที่ทำงานของทั้งองค์กรไปยังความจุระดับพรีเมี่ยม จะกำหนดพื้นที่ทำงานและพื้นที่ทำงานของฉันทั้งหมดในองค์กรของคุณ ไปยังความจุระดับพรีเมี่ยมนี้</span><span class="sxs-lookup"><span data-stu-id="f76db-187">Assigning the entire organization's workspaces to Premium capacity assigns all workspaces and My Workspaces, in your organization, to this Premium capacity.</span></span> <span data-ttu-id="f76db-188">นอกจากนี้ ผู้ใช้ปัจจุบันและในอนาคตทั้งหมดจะมีสิทธิ์ในการกำหนดพื้นที่ทำงานของแต่ละคนให้ความจุนี้</span><span class="sxs-lookup"><span data-stu-id="f76db-188">In addition, all current and future users will have the permission to reassign individual workspaces to this capacity.</span></span> |
   | | |

1. <span data-ttu-id="f76db-189">เลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="f76db-189">Select **Apply**.</span></span>

### <a name="assign-from-workspace-settings"></a><span data-ttu-id="f76db-190">กำหนดจากการตั้งค่าพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f76db-190">Assign from workspace settings</span></span>

<span data-ttu-id="f76db-191">คุณยังสามารถกำหนดพื้นที่ทำงานเป็นความจุพรีเมียมจากการตั้งค่าของพื้นที่การทำงานนั้น</span><span class="sxs-lookup"><span data-stu-id="f76db-191">You can also assign a workspace to a Premium capacity from the settings of that workspace.</span></span> <span data-ttu-id="f76db-192">เมื่อต้องการย้ายพื้นที่ทำงานไปสู่ความจุ คุณต้องมีสิทธิ์ของผู้ดูแลระบบในพื้นที่ทำงานนั้นและยังต้องมีสิทธิ์ในการกำหนดความจุไปยังความจุดังกล่าวด้วย</span><span class="sxs-lookup"><span data-stu-id="f76db-192">To move a workspace into a capacity, you must have admin permissions to that workspace, and also capacity assignment permissions to that capacity.</span></span> <span data-ttu-id="f76db-193">โปรดทราบว่าผู้ดูแลระบบผู้ดูแลระบบพื้นที่ทำงานสามารถลบพื้นที่ทำงานออกจากความจุระดับพรีเมี่ยมได้</span><span class="sxs-lookup"><span data-stu-id="f76db-193">Note that workspace admins can always remove a workspace from Premium capacity.</span></span>

1. <span data-ttu-id="f76db-194">แก้ไขพื้นที่ทำงานโดยเลือกจุดไข่ปลา **(...)** แล้วเลือก **แก้ไขพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="f76db-194">Edit a workspace by selecting the ellipsis **(. . .)** then selecting **Edit workspace**.</span></span>

    ![แก้ไขพื้นที่ทำงานจากเมนจุดไข่ปลา](media/service-admin-premium-manage/edit-app-workspace.png)

1. <span data-ttu-id="f76db-196">ภายใต้ **แก้ไขพื้นที่ทำงาน** ขยาย **ขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="f76db-196">Under **Edit workspace**, expand **Advanced**.</span></span>

1. <span data-ttu-id="f76db-197">เลือกความจุที่คุณต้องการกำหนดพื้นที่ทำงานนี้ไปยัง</span><span class="sxs-lookup"><span data-stu-id="f76db-197">Select the capacity that you want to assign this workspace to.</span></span>

    ![ส่วนที่เลือกกำลังการผลิตแบบดร๊อปดาวน์](media/service-admin-premium-manage/app-workspace-advanced.png)

1. <span data-ttu-id="f76db-199">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f76db-199">Select **Save**.</span></span>

<span data-ttu-id="f76db-200">เมื่อคุณบันทึก พื้นที่ทำงานและเนื้อหาทั้งหมด จะถูกย้ายไปยังความจุระดับพรีเมียมโดยไม่ทำให้เกิดปัญหากับผู้ใช้ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="f76db-200">Once saved, the workspace and all its contents are moved into Premium capacity without any experience interruption for end users.</span></span>

## <a name="power-bi-report-server-product-key"></a><span data-ttu-id="f76db-201">คีย์ผลิตภัณฑ์เซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="f76db-201">Power BI Report Server product key</span></span>

<span data-ttu-id="f76db-202">ในแท็บ **การตั้งค่าความจุ** ของพอร์ทัลผู้ดูแลระบบ Power BI คุณจะสามารถเข้าถึงคีย์ผลิตภัณฑ์เซิร์ฟเวอร์รายงาน Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f76db-202">On the **Capacity settings** tab of the Power BI admin portal, you will have access to your Power BI Report Server product key.</span></span> <span data-ttu-id="f76db-203">ซึ่งจะพร้อมใช้งานสำหรับผู้ดูแลระบบสากล หรือผู้ใช้ที่ได้รับการกำหนดบทบาทเป็นผู้ดูแลระบบ Power BI Premium SKU</span><span class="sxs-lookup"><span data-stu-id="f76db-203">This will only be available for Global Admins or users assigned the Power BI service administrator role and if you have purchase a Power BI Premium SKU.</span></span>

![Power BI Report Server คีย์ภายในการตั้งค่าความจุ](media/service-admin-premium-manage/pbirs-product-key.png)

<span data-ttu-id="f76db-205">โดยเลือก **คีย์เซิร์ฟเวอร์รายงาน Power BI** จะแสดงกล่องโต้ตอบที่มีคีย์ผลิตภัณฑ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f76db-205">Selecting **Power BI Report Server key** will display a dialog contain your product key.</span></span> <span data-ttu-id="f76db-206">คุณสามารถคัดลอกและใช้กับการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="f76db-206">You can copy it and use it with the installation.</span></span>

![คีย์ผลิตภัณฑ์เซิร์ฟเวอร์รายงาน Power BI](media/service-admin-premium-manage/pbirs-product-key-dialog.png)

<span data-ttu-id="f76db-208">สำหรับข้อมูลเพิ่มเติม ให้ดู[ติดตั้งเซิร์ฟเวอร์รายงาน Power BI](../report-server/install-report-server.md)</span><span class="sxs-lookup"><span data-stu-id="f76db-208">For more information, see [Install Power BI Report Server](../report-server/install-report-server.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="f76db-209">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="f76db-209">Next steps</span></span>

[<span data-ttu-id="f76db-210">การจัดการความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="f76db-210">Managing Premium capacities</span></span>](service-premium-capacity-manage.md)

<span data-ttu-id="f76db-211">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f76db-211">More questions?</span></span> [<span data-ttu-id="f76db-212">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="f76db-212">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)

<span data-ttu-id="f76db-213">Power BI ได้แนะนำ Power BI Premium Gen2 เข้ามาใช้งานเป็นข้อเสนอการแสดงตัวอย่าง ซึ่งปรับปรุงประสบการณ์การใช้งาน Power BI Premium ด้วยการปรับปรุงในสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f76db-213">Power BI has introduced Power BI Premium Gen2 as a preview offering, which improves the Power BI Premium experience with improvements in the following:</span></span>
* <span data-ttu-id="f76db-214">ประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="f76db-214">Performance</span></span>
* <span data-ttu-id="f76db-215">สิทธิการใช้งานต่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f76db-215">Per-user licensing</span></span>
* <span data-ttu-id="f76db-216">ขนาดใหญ่ขึ้น</span><span class="sxs-lookup"><span data-stu-id="f76db-216">Greater scale</span></span>
* <span data-ttu-id="f76db-217">เมตริกที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="f76db-217">Improved metrics</span></span>
* <span data-ttu-id="f76db-218">การปรับขนาดอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f76db-218">Autoscaling</span></span>
* <span data-ttu-id="f76db-219">ลดค่าใช้จ่ายในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="f76db-219">Reduced management overhead</span></span>

<span data-ttu-id="f76db-220">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI Premium Gen2 โปรดดูที่ [Power BI Premium Generation 2 (ตัวอย่าง)](service-premium-what-is.md#power-bi-premium-generation-2-preview)</span><span class="sxs-lookup"><span data-stu-id="f76db-220">For more information about Power BI Premium Gen2, see [Power BI Premium Generation 2 (preview)](service-premium-what-is.md#power-bi-premium-generation-2-preview).</span></span>