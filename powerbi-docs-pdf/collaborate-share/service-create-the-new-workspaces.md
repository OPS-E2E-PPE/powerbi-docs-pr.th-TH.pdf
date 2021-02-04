---
title: สร้างพื้นที่ทำงานใหม่ - Power BI
description: 'เรียนรู้วิธีการสร้างพื้นที่ทำงานใหม่: คอลเลกชันของแดชบอร์ด รายงาน และรายงานที่มีการแบ่งหน้าที่สร้างขึ้นเพื่อนำเสนอเมทริกซ์หลักสำหรับองค์กรของคุณ'
author: maggiesMSFT
ms.author: maggies
ms.reviewer: lukaszp
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 09/04/2020
ms.custom: contperf-fy21q1, contperf-fy20q4
LocalizationGroup: Share your work
ms.openlocfilehash: 2c15c6afbf1a84ab5e8103a8d73792705418d2e6
ms.sourcegitcommit: 7bf09116163afaae312eb2b232eb7967baee2c92
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/17/2020
ms.locfileid: "97621728"
---
# <a name="create-the-new-workspaces-in-power-bi"></a><span data-ttu-id="35228-103">สร้างพื้นที่ทำงานใหม่ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="35228-103">Create the new workspaces in Power BI</span></span>

<span data-ttu-id="35228-104">บทความนี้อธิบายถึงวิธีการสร้าง *พื้นที่ทำงานใหม่* หนึ่งพื้นที่แทนที่จะเป็นพื้นที่ทำงาน *แบบคลาสสิก*</span><span class="sxs-lookup"><span data-stu-id="35228-104">This article explains how to create one of the *new workspaces* instead of a *classic* workspace.</span></span> <span data-ttu-id="35228-105">พื้นที่ทำงานทั้งสองประเภทคือสถานที่ที่จะร่วมงานกับเพื่อนร่วมงาน</span><span class="sxs-lookup"><span data-stu-id="35228-105">Both kinds of workspaces are places to collaborate with colleagues.</span></span> <span data-ttu-id="35228-106">ในพื้นที่เหล่านั้น คุณสามารถสร้างคอลเลกชันของแดชบอร์ด รายงาน และรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="35228-106">In them, you create collections of dashboards, reports, and paginated reports.</span></span> <span data-ttu-id="35228-107">ถ้าคุณต้องการ คุณยังสามารถรวมคอลเลกชันนั้นลงใน *แอป* และแจกจ่ายไปยังผู้ชมที่กว้างขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="35228-107">If you want, you can also bundle that collection into an *app* and distribute it to a broader audience.</span></span> <span data-ttu-id="35228-108">สำหรับพื้นหลังเพิ่มเติม ดูบทความ [พื้นที่ทำงานใหม่](service-new-workspaces.md)</span><span class="sxs-lookup"><span data-stu-id="35228-108">For more background, see the [new workspaces](service-new-workspaces.md) article.</span></span>

<span data-ttu-id="35228-109">พร้อมที่จะโยกย้ายจากพื้นที่ทำงานแบบคลาสสิกของคุณหรือยัง</span><span class="sxs-lookup"><span data-stu-id="35228-109">Ready to migrate your classic workspace?</span></span> <span data-ttu-id="35228-110">ดู [อัปเกรดพื้นที่ทำงานแบบคลาสสิกเป็นพื้นที่งานใหม่ใน Power BI](service-upgrade-workspaces.md) สำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="35228-110">See [Upgrade classic workspaces to the new workspaces in Power BI](service-upgrade-workspaces.md) for details.</span></span>

> [!NOTE]
> <span data-ttu-id="35228-111">เมื่อต้องการบังคับใช้การรักษาความปลอดภัยระดับแถว (RLS) สำหรับผู้ใช้ Power BI Pro ที่เรียกดูเนื้อหาในพื้นที่ทำงาน ให้มอบหมายบทบาทผู้ชมให้แก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="35228-111">To enforce row-level security (RLS) for Power BI Pro users browsing content in a workspace, assign the users the Viewer Role.</span></span> <span data-ttu-id="35228-112">ดู[บทบาทในพื้นที่ทำงานใหม่](service-new-workspaces.md#roles-in-the-new-workspaces)สำหรับคำอธิบายเรื่องบทบาทที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="35228-112">See [Roles in the new workspaces](service-new-workspaces.md#roles-in-the-new-workspaces) for an explanation of the different roles.</span></span>

## <a name="create-one-of-the-new-workspaces"></a><span data-ttu-id="35228-113">สร้างพื้นที่ทำงานใหม่หนึ่งพื้นที่</span><span class="sxs-lookup"><span data-stu-id="35228-113">Create one of the new workspaces</span></span>

1. <span data-ttu-id="35228-114">เริ่มต้นโดยการสร้างพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="35228-114">Start by creating the workspace.</span></span> <span data-ttu-id="35228-115">เลือก **พื้นที่ทำงาน** > **สร้างพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="35228-115">Select **Workspaces** > **Create workspace**.</span></span>
   
     ![ภาพหน้าจอของการสร้างพื้นที่ทำงาน](media/service-create-the-new-workspaces/power-bi-workspace-create.png)

2. <span data-ttu-id="35228-117">คุณกำลังสร้างพื้นที่ทำงานที่อัปเกรดโดยอัตโนมัติ เว้นแต่ว่าคุณจะเลือกที่จะ **แปลงกลับเป็นแบบดั้งเดิม**</span><span class="sxs-lookup"><span data-stu-id="35228-117">You're automatically creating an upgraded workspace, unless you opt to **Revert to classic**.</span></span>
   
     ![ภาพหน้าจอของประสบการณ์การใช้งานพื้นที่ทำงานใหม่](media/service-create-the-new-workspaces/power-bi-new-workspace.png)
     
     <span data-ttu-id="35228-119">ถ้าคุณเลือก **แปลงกลับเป็นแบบคลาสสิก** คุณจะสร้าง [พื้นที่ทำงานโดยยึดตาม Microsoft 365 Group](service-create-workspaces.md)</span><span class="sxs-lookup"><span data-stu-id="35228-119">If you select **Revert to classic**, you [create a classic workspace](service-create-workspaces.md) based on a Microsoft 365 group.</span></span>

2. <span data-ttu-id="35228-120">ตั้งชื่อพื้นที่ทำงานที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="35228-120">Give the workspace a unique name.</span></span> <span data-ttu-id="35228-121">ถ้าไม่มีชื่อ แก้ไขโดยให้ชื่อที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="35228-121">If the name isn't available, edit it to come up with a unique name.</span></span>
   
     <span data-ttu-id="35228-122">แอปที่คุณสร้างจากพื้นที่ทำงานจะมีชื่อและไอคอนเดียวกันกับพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="35228-122">The app you create from the workspace will have the same name and icon as the workspace.</span></span>
   
1. <span data-ttu-id="35228-123">ต่อไปนี้คือรายการที่เป็นตัวเลือกบางอย่างที่คุณสามารถตั้งค่าสำหรับพื้นที่ทำงานของคุณ:</span><span class="sxs-lookup"><span data-stu-id="35228-123">Here are some optional items you can set for your workspace:</span></span>

    - <span data-ttu-id="35228-124">อัปโหลด **รูปพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="35228-124">Upload a **Workspace image**.</span></span> <span data-ttu-id="35228-125">ไฟล์สามารถเป็นรูปแบบ .png หรือ .jpg ได้</span><span class="sxs-lookup"><span data-stu-id="35228-125">Files can be .png or .jpg format.</span></span> <span data-ttu-id="35228-126">ขนาดไฟล์จะต้องน้อยกว่า 45 KB</span><span class="sxs-lookup"><span data-stu-id="35228-126">File size has to be less than 45 KB.</span></span> 
    - <span data-ttu-id="35228-127">[ระบุ OneDrive ของพื้นที่ทำงาน](#set-a-workspace-onedrive) เพื่อใช้ตำแหน่งพื้นที่จัดเก็บไฟล์ Microsoft 365 Group</span><span class="sxs-lookup"><span data-stu-id="35228-127">[Specify a Workspace OneDrive](#set-a-workspace-onedrive) to use a Microsoft 365 group file storage location.</span></span>    
    - <span data-ttu-id="35228-128">[เพิ่มรายชื่อผู้ติดต่อ](#create-a-contact-list)</span><span class="sxs-lookup"><span data-stu-id="35228-128">[Add a Contact list](#create-a-contact-list).</span></span> <span data-ttu-id="35228-129">ตามค่าเริ่มต้น ผู้ดูแลระบบพื้นที่ทำงานเป็นผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="35228-129">By default, the workspace admins are the contacts.</span></span> 
    - <span data-ttu-id="35228-130">[อนุญาตให้ผู้สนับสนุนอัปเดตแอป](#allow-contributors-to-update-the-app)สำหรับพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="35228-130">[Allow contributors to update the app](#allow-contributors-to-update-the-app) for the workspace</span></span>
    - <span data-ttu-id="35228-131">หากต้องการกำหนดพื้นที่ทำงานสำหรับ **ความจุเฉพาะ** บนแท็บ **พรีเมียม** เลือก **ความจุเฉพาะ**</span><span class="sxs-lookup"><span data-stu-id="35228-131">To assign the workspace to a **Dedicated capacity**, on the **Premium** tab select **Dedicated capacity**.</span></span>

        ![ภาพหน้าจอของความจุเฉพาะ](media/service-create-the-new-workspaces/power-bi-workspace-premium.png)

1. <span data-ttu-id="35228-133">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="35228-133">Select **Save**.</span></span>

    <span data-ttu-id="35228-134">Power BI จะสร้างพื้นที่ทำงาน และเปิดพื้นที่ทำงานนั้น</span><span class="sxs-lookup"><span data-stu-id="35228-134">Power BI creates the workspace and opens it.</span></span> <span data-ttu-id="35228-135">ซึ่งคุณจะเห็นในรายการของพื้นที่ทำงานที่คุณเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="35228-135">You see it in the list of workspaces you’re a member of.</span></span> 

## <a name="give-access-to-your-workspace"></a><span data-ttu-id="35228-136">ให้สิทธิ์การเข้าถึงพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="35228-136">Give access to your workspace</span></span>

<span data-ttu-id="35228-137">ทุกคนที่มีบทบาทเป็นผู้ดูแลระบบในพื้นที่ทำงานสามารถให้สิทธิ์ผู้อื่นในการเข้าถึงพื้นที่ทำงานได้โดยการเพิ่มบุคคลดังกล่าวไปยังบทบาทอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="35228-137">Anyone who has an admin role in a workspace can give others access to the workspace by adding them to the different roles.</span></span> <span data-ttu-id="35228-138">ผู้สร้างพื้นที่ทำงานจะเป็นผู้ดูแลระบบโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="35228-138">Workspace creators are automatically admins.</span></span> <span data-ttu-id="35228-139">ดูคำอธิบายเรื่องบทบาทต่าง ๆ ได้ที่[บทบาทในพื้นที่ทำงานใหม่](service-new-workspaces.md#roles-in-the-new-workspaces)</span><span class="sxs-lookup"><span data-stu-id="35228-139">See [Roles in the new workspaces](service-new-workspaces.md#roles-in-the-new-workspaces) for an explanation of the roles.</span></span>

1. <span data-ttu-id="35228-140">เนื่องจากคุณเป็นผู้ดูแลระบบในรายการเนื้อหาของพื้นที่ทำงาน คุณจะเห็น **การเข้าถึง**</span><span class="sxs-lookup"><span data-stu-id="35228-140">Because you're an admin, on the workspace content list page, you see **Access**.</span></span>

    ![ภาพหน้าจอของรายการเนื้อหาของพื้นที่ทำงาน](media/service-create-the-new-workspaces/power-bi-workspace-access-icon.png)

1. <span data-ttu-id="35228-142">เพิ่มกลุ่มความปลอดภัย รายการการแจกจ่าย Microsoft 365 Group หรือบุคคลลงในพื้นที่ทำงานเหล่านี้เป็นผู้ชม สมาชิก ผู้สนับสนุน หรือผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="35228-142">Add security groups, distribution lists, Microsoft 365 groups, or individuals to these workspaces as admins, members, contributors, or viewers.</span></span> 

    ![ภาพหน้าจอของพื้นที่ทำงานเพิ่มสมาชิก ผู้ดูแลระบบ ผู้สนับสนุน](media/service-create-the-new-workspaces/power-bi-workspace-add-members.png)

9. <span data-ttu-id="35228-144">เลือก **เพิ่ม** > **ปิด**</span><span class="sxs-lookup"><span data-stu-id="35228-144">Select **Add** > **Close**.</span></span>

## <a name="set-a-workspace-onedrive"></a><span data-ttu-id="35228-145">ตั้งค่า OneDrive ของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="35228-145">Set a workspace OneDrive</span></span>

<span data-ttu-id="35228-146">คุณลักษณะ OneDrive ของพื้นที่ทำงานช่วยให้คุณสามารถกำหนดค่า Microsoft 365 Group ที่มีที่จัดเก็บไฟล์ SharePoint Document Library พร้อมใช้งานสำหรับผู้ใช้พื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="35228-146">The Workspace OneDrive feature allows you to configure a Microsoft 365 group whose SharePoint Document Library file storage is available to workspace users.</span></span> <span data-ttu-id="35228-147">คุณสร้างกลุ่มภายนอก Power BI ก่อน</span><span class="sxs-lookup"><span data-stu-id="35228-147">You create the group outside of Power BI first.</span></span> 

<span data-ttu-id="35228-148">Power BI ไม่ซิงค์สิทธิ์ของผู้ใช้หรือกลุ่มที่มีการกำหนดค่าให้มีสิทธิ์การเข้าถึงพื้นที่ทำงานด้วยการเป็นสมาชิกของ Microsoft 365 Group</span><span class="sxs-lookup"><span data-stu-id="35228-148">Power BI doesn't synchronize permissions of users or groups who are configured to have workspace access with the Microsoft 365 group membership.</span></span> <span data-ttu-id="35228-149">แนวทางปฏิบัติที่ดีที่สุดคือการให้ [สิทธิ์การเข้าถึงพื้นที่ทำงาน ](#give-access-to-your-workspace)กับ Microsoft 365 Group เดียวกันซึ่งมีที่เก็บข้อมูลไฟล์ที่คุณกำหนดค่าในการตั้งค่า Microsoft 365 Group นี้</span><span class="sxs-lookup"><span data-stu-id="35228-149">The best practice is to give [access to the workspace](#give-access-to-your-workspace) to the same Microsoft 365 group whose file storage you configure in this setting Microsoft 365 group.</span></span> <span data-ttu-id="35228-150">จากนั้นจัดการการเข้าถึงพื้นที่ทำงานโดยการจัดการสมาชิกของ Microsoft 365 Group</span><span class="sxs-lookup"><span data-stu-id="35228-150">Then manage workspace access by managing membership of the Microsoft 365 group.</span></span> 

1. <span data-ttu-id="35228-151">เข้าถึงการตั้งค่า **พื้นที่ทำงาน OneDrive** ใหม่ในหนึ่งในสองวิธี:</span><span class="sxs-lookup"><span data-stu-id="35228-151">Access the new **Workspace OneDrive** setting in one of two ways:</span></span>

    <span data-ttu-id="35228-152">ในบานหน้าต่าง **สร้างพื้นที่ทำงาน** เมื่อคุณสร้างในครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="35228-152">In the **Create a workspace** pane when you first create it.</span></span>

    <span data-ttu-id="35228-153">ในบานหน้าต่างการนำทาง เลือกลูกศรถัดจาก **พื้นที่ทำงาน** เลือก **ตัวเลือกเพิ่มเติม** (...) ถัดจากชื่อพื้นที่ทำงานของคุณ > **การตั้งค่าพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="35228-153">In the nav pane, select the arrow next to **Workspaces**, select **More options** (...) next to the workspace name > **Workspace settings**.</span></span> <span data-ttu-id="35228-154">บานหน้าต่าง **การตั้งค่า** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="35228-154">The **Settings** pane opens.</span></span>

    ![ภาพหน้าจอของการตั้งค่าพื้นที่ทำงาน](media/service-create-the-new-workspaces/power-bi-workspace-new-settings.png)

2. <span data-ttu-id="35228-156">ภายใต้ **ขั้นสูง** > **พื้นที่ทำงาน OneDrive** พิมพ์ชื่อของ Microsoft 365 Group ที่คุณสร้างก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="35228-156">Under **Advanced** > **Workspace OneDrive**, type the name of the Microsoft 365 group that you created earlier.</span></span> <span data-ttu-id="35228-157">พิมพ์เพียงชื่อไม่ใช่ URL</span><span class="sxs-lookup"><span data-stu-id="35228-157">Type just the name, not the URL.</span></span> <span data-ttu-id="35228-158">Power BI จะเลือก OneDrive สำหรับกลุ่มโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="35228-158">Power BI automatically picks up the OneDrive for the group.</span></span>

    ![ภาพหน้าจอของการระบุตำแหน่งที่ตั้ง OneDrive](media/service-create-the-new-workspaces/power-bi-new-workspace-onedrive.png)

3. <span data-ttu-id="35228-160">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="35228-160">Select **Save**.</span></span>

### <a name="access-the-workspace-onedrive-location"></a><span data-ttu-id="35228-161">เข้าถึงตำแหน่งที่ตั้งพื้นที่ทำงาน OneDrive</span><span class="sxs-lookup"><span data-stu-id="35228-161">Access the workspace OneDrive location</span></span>

<span data-ttu-id="35228-162">หลังจากที่คุณกำหนดค่าตำแหน่งที่ตั้ง OneDrive แล้ว คุณจะได้รับในลักษณะเดียวกับที่คุณได้รับแหล่งข้อมูลอื่น ๆ ในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="35228-162">After you've configured the OneDrive location, you get to it in the same way you get to other data sources in the Power BI service.</span></span>

1. <span data-ttu-id="35228-163">ในบานหน้าต่างนำทาง ให้เลือก **รับข้อมูล** จากนั้นไปที่กล่อง **ไฟล์** แล้วเลือก **รับ**</span><span class="sxs-lookup"><span data-stu-id="35228-163">In the nav pane, select **Get Data**, then in the **Files** box select **Get**.</span></span>

    ![ภาพหน้าจอของรับข้อมูล รับไฟล์](media/service-create-the-new-workspaces/power-bi-get-data-files.png)

1.  <span data-ttu-id="35228-165">รายการ **OneDrive – Business** คือ OneDrive สำหรับธุรกิจส่วนตัวของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="35228-165">The **OneDrive – Business** entry is your own personal OneDrive for Business.</span></span> <span data-ttu-id="35228-166">OneDrive ที่สองคือรายการที่คุณเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="35228-166">The second OneDrive is the one you added.</span></span>

    ![ภาพหน้าจอของตำแหน่งที่ตั้งไฟล์พื้นที่ทำงาน - รับข้อมูล](media/service-create-the-new-workspaces/power-bi-new-workspace-get-data-onedrive.png)

## <a name="create-a-contact-list"></a><span data-ttu-id="35228-168">สร้างรายชื่อผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="35228-168">Create a contact list</span></span>

<span data-ttu-id="35228-169">คุณสามารถระบุได้ว่าจะให้ผู้ใช้รายใดได้รับการแจ้งเตือนเกี่ยวกับปัญหาที่เกิดขึ้นในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="35228-169">You can specify which users receive notification about issues occurring in the workspace.</span></span> <span data-ttu-id="35228-170">ตามค่าเริ่มต้นผู้ใช้หรือกลุ่มใด ๆ ที่ระบุเป็นผู้ดูแลระบบพื้นที่ทำงานได้รับการแจ้งเตือน แต่คุณสามารถเพิ่มบุคคลอื่นลงใน *รายชื่อผู้ติดต่อ* ได้</span><span class="sxs-lookup"><span data-stu-id="35228-170">By default, any user or group specified as a workspace admin is notified, but you can add others to the *contact list*.</span></span> <span data-ttu-id="35228-171">ผู้ใช้หรือกลุ่มต่าง ๆ ในรายการที่ติดต่อจะระบุอยู่ในอินเทอร์เฟซผู้ใช้ (UI) เพื่อให้ความช่วยเหลือเกี่ยวกับพื้นที่ทำงานแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="35228-171">Users or groups in the contact list are listed in the user interface (UI) to help users get help related to the workspace.</span></span>

1. <span data-ttu-id="35228-172">เข้าถึงการตั้งค่า **รายชื่อผู้ติดต่อ** ใหม่ด้วยหนึ่งในสองวิธี:</span><span class="sxs-lookup"><span data-stu-id="35228-172">Access the new **Contact list** setting in one of two ways:</span></span>

    <span data-ttu-id="35228-173">ในบานหน้าต่าง **สร้างพื้นที่ทำงาน** เมื่อคุณสร้างในครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="35228-173">In the **Create a workspace** pane when you first create it.</span></span>

    <span data-ttu-id="35228-174">ในบานหน้าต่างการนำทาง เลือกลูกศรถัดจาก **พื้นที่ทำงาน** เลือก **ตัวเลือกเพิ่มเติม** (...) ถัดจากชื่อพื้นที่ทำงานของคุณ > **การตั้งค่าพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="35228-174">In the nav pane, select the arrow next to **Workspaces**, select **More options** (...) next to the workspace name > **Workspace settings**.</span></span> <span data-ttu-id="35228-175">บานหน้าต่าง **การตั้งค่า** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="35228-175">The **Settings** pane opens.</span></span>

    ![ภาพหน้าจอของการตั้งค่าพื้นที่ทำงาน](media/service-create-the-new-workspaces/power-bi-workspace-new-settings.png)

2. <span data-ttu-id="35228-177">ภายในเมนู **ขั้นสูง**, **รายชื่อผู้ติดต่อ**, ยอมรับค่าเริ่มต้น, **ผู้ดูแลระบบพื้นที่ทำงาน** หรือเพิ่มรายชื่อ **กลุ่มหรือผู้ใช้ที่เฉพาะเจาะจง** ของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="35228-177">Under **Advanced**, **Contact list**, accept the default, **Workspace admins**, or add your own list of **Specific users or groups**.</span></span> 

    ![ภาพหน้าจอของผู้ติดต่อในพื้นที่ทำงาน](media/service-create-the-new-workspaces/power-bi-workspace-contacts.png)

3. <span data-ttu-id="35228-179">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="35228-179">Select **Save**.</span></span>

## <a name="allow-contributors-to-update-the-app"></a><span data-ttu-id="35228-180">อนุญาตให้ผู้สนับสนุนอัปเดตแอปได้</span><span class="sxs-lookup"><span data-stu-id="35228-180">Allow contributors to update the app</span></span>

<span data-ttu-id="35228-181">**อนุญาตให้ผู้สนับสนุนในการอัปเดตแอปสำหรับพื้นที่ทำงานนี้** การตั้งค่าอนุญาตให้ผู้ดูแลระบบพื้นที่ทำงานเพื่อมอบสิทธิ์ให้กับผู้ใช้ในบทบาทการสนับสนุนสามารถอัปเดตแอปสำหรับพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="35228-181">The **Allow contributors to update the app for this workspace** setting allows workspace Admins to delegate to users in the Contributor role the ability to update the app for the workspace.</span></span> <span data-ttu-id="35228-182">ตามค่าเริ่มต้น เฉพาะผู้ดูแลระบบพื้นที่ทำงานและสมาชิกเท่านั้นที่สามารถเผยแพร่และอัปเดตแอปสำหรับพื้นที่ทำงานได้</span><span class="sxs-lookup"><span data-stu-id="35228-182">By default, only workspace Admins and Members can publish and update the app for the workspace.</span></span> 

1. <span data-ttu-id="35228-183">หากต้องการเข้าถึงการตั้งค่านี้ ในบานหน้าต่างการนำทาง ให้เลือกลูกศรถัดจาก **พื้นที่ทำงาน** เลือก **ตัวเลือกเพิ่มเติม** (...) ถัดจากชื่อพื้นที่ทำงานของคุณ > **การตั้งค่าพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="35228-183">To access this setting, in the nav pane, select the arrow next to **Workspaces**, select **More options** (...) next to the workspace name > **Workspace settings**.</span></span> <span data-ttu-id="35228-184">บานหน้าต่าง **การตั้งค่า** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="35228-184">The **Settings** pane opens.</span></span>

    ![ภาพหน้าจอของการตั้งค่าพื้นที่ทำงาน](media/service-create-the-new-workspaces/power-bi-workspace-new-settings.png)

2. <span data-ttu-id="35228-186">ภายในเมนู **ขั้นสูง** ให้ขยาย **การตั้งค่าการรักษาความปลอดภัย**</span><span class="sxs-lookup"><span data-stu-id="35228-186">Under **Advanced**, expand **Security settings**.</span></span> <span data-ttu-id="35228-187">เลือก **อนุญาตให้ผู้สนับสนุนอัปเดตแอปสำหรับพื้นที่ทำงานนี้**</span><span class="sxs-lookup"><span data-stu-id="35228-187">Select **Allow contributors to update the app for this workspace**.</span></span> 

<span data-ttu-id="35228-188">เมื่อเปิดใช้งาน ผู้สนับสนุนสามารถ:</span><span class="sxs-lookup"><span data-stu-id="35228-188">When enabled, contributors can:</span></span>
* <span data-ttu-id="35228-189">อัปเดตข้อมูลเมตาดาต้าของแอปเช่น ชื่อ ไอคอน คำอธิบาย ไซต์ที่รองรับ และสี</span><span class="sxs-lookup"><span data-stu-id="35228-189">Update app metadata like name, icon, description, support site, and color</span></span>
* <span data-ttu-id="35228-190">เพิ่มหรือลบรายการที่รวมอยู่ในแอป เช่น การเพิ่มรายงานหรือชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="35228-190">Add or remove items included in the app, like adding reports or datasets</span></span>
* <span data-ttu-id="35228-191">เปลี่ยนการนำทางแอปหรือรายการเริ่มต้นที่แอปจะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="35228-191">Change the app navigation or default item the app opens on</span></span>

<span data-ttu-id="35228-192">แต่ผู้สนับสนุนไม่สามารถ:</span><span class="sxs-lookup"><span data-stu-id="35228-192">However, contributors can't:</span></span>
* <span data-ttu-id="35228-193">เผยแพร่แอปในครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="35228-193">Publish the app for the first time</span></span>
* <span data-ttu-id="35228-194">เปลี่ยนผู้ที่มีสิทธิ์ไปยังแอป</span><span class="sxs-lookup"><span data-stu-id="35228-194">Change who has permission to the app</span></span>

## <a name="apps-in-the-new-workspaces"></a><span data-ttu-id="35228-195">แอปในพื้นที่ทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="35228-195">Apps in the new workspaces</span></span>

<span data-ttu-id="35228-196">คุณสามารถสร้างและใช้ *แอป* เพื่อเป็นประสบการณ์การใช้งานพื้นที่ทำงานใหม่ แทนที่จะเป็นชุดเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="35228-196">You can create and consume *apps* the new workspace experiences, instead of content packs.</span></span> <span data-ttu-id="35228-197">แอปคือคอลเลกชันของแดชบอร์ด รายงาน และชุดข้อมูลที่เชื่อมต่อกับบริการของบุคคลที่สามและข้อมูลองค์กร</span><span class="sxs-lookup"><span data-stu-id="35228-197">Apps are collections of dashboards, reports, and datasets that connect to third-party services and organizational data.</span></span> <span data-ttu-id="35228-198">แอปจะทำให้ง่ายต่อการรับข้อมูลจากบริการต่าง ๆ เช่น Microsoft Dynamics CRM, Salesforce และ Google Analytics</span><span class="sxs-lookup"><span data-stu-id="35228-198">Apps make it easy to get data from the services such as Microsoft Dynamics CRM, Salesforce, and Google Analytics.</span></span>

<span data-ttu-id="35228-199">ในการใช้งานของพื้นที่ทำงานใหม่ คุณไม่สามารถสร้าง หรือใช้ชุดเนื้อหาระดับองค์กร</span><span class="sxs-lookup"><span data-stu-id="35228-199">In the new workspace experience, you can't create or consume organizational content packs.</span></span> <span data-ttu-id="35228-200">ถามทีมภายในของคุณเพื่อจัดหาแอปสำหรับชุดเนื้อหาใด ๆ ที่คุณกำลังใช้อยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="35228-200">Ask your internal teams to provide apps for any content packs you’re currently using.</span></span> 

### <a name="distribute-an-app"></a><span data-ttu-id="35228-201">แจกจ่ายแอป</span><span class="sxs-lookup"><span data-stu-id="35228-201">Distribute an app</span></span>

<span data-ttu-id="35228-202">ถ้าคุณต้องการแจกจ่ายเนื้อหาอย่างเป็นทางการไปยังผู้ชมจำนวนมากในองค์กรของคุณ คุณสามารถเผยแพร่ *แอป* จากพื้นที่ทำงานของคุณได้</span><span class="sxs-lookup"><span data-stu-id="35228-202">If you want to distribute official content to a large audience in your organization, you can publish an *app* from your workspace.</span></span>  <span data-ttu-id="35228-203">เมื่อเนื้อหาของคุณพร้อมแล้ว คุณสามารถเลือกแดชบอร์ดและรายงานที่คุณต้องการเผยแพร่ และเผยแพร่เป็นแอปได้</span><span class="sxs-lookup"><span data-stu-id="35228-203">When your content is ready, you choose which dashboards and reports you want to publish, and publish them as an app.</span></span> <span data-ttu-id="35228-204">คุณสามารถสร้างแอปหนึ่งจากแต่ละพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="35228-204">You can create one app from each workspace.</span></span>

<span data-ttu-id="35228-205">อ่านเกี่ยวกับ[วิธีการเผยแพร่แอปจากพื้นที่ทำงานใหม่](service-create-distribute-apps.md)</span><span class="sxs-lookup"><span data-stu-id="35228-205">Read about how to [publish an app from the new workspaces](service-create-distribute-apps.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="35228-206">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="35228-206">Next steps</span></span>
* <span data-ttu-id="35228-207">อ่านเกี่ยวกับ[การจัดระเบียบงานในการใช้งานพื้นที่ทำงานใหม่ใน Power BI](service-new-workspaces.md)</span><span class="sxs-lookup"><span data-stu-id="35228-207">Read about [organizing work in the new workspaces experience in Power BI](service-new-workspaces.md)</span></span>
* [<span data-ttu-id="35228-208">สร้างพื้นที่ทำงานแบบดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="35228-208">Create classic workspaces</span></span>](service-create-workspaces.md)
* [<span data-ttu-id="35228-209">เผยแพร่แอปจากพื้นที่ทำงานใหม่ใน Power BI </span><span class="sxs-lookup"><span data-stu-id="35228-209">Publish an app from the new workspaces in Power BI</span></span>](service-create-distribute-apps.md)
* <span data-ttu-id="35228-210">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="35228-210">Questions?</span></span> [<span data-ttu-id="35228-211">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="35228-211">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
