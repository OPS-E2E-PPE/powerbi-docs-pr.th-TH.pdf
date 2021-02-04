---
title: การแก้ไขปัญหาไปป์ไลน์การปรับใช้
description: แก้ปัญหาไปป์ไลน์การปรับใช้ใน Power BI
author: KesemSharabi
ms.author: kesharab
ms.topic: troubleshooting
ms.service: powerbi
ms.subservice: pbi-deployment
ms.date: 11/11/2020
ms.openlocfilehash: 3787f1cb61262f9f1fa64e04487c7d6395b4e549
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96417646"
---
# <a name="deployment-pipelines-troubleshooting"></a><span data-ttu-id="ce4f0-103">การแก้ไขปัญหาไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-103">Deployment pipelines troubleshooting</span></span>

<span data-ttu-id="ce4f0-104">ใช้บทความนี้เพื่อแก้ไขปัญหาในไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-104">Use this article to troubleshoot issues in deployment pipelines.</span></span>

## <a name="general"></a><span data-ttu-id="ce4f0-105">ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="ce4f0-105">General</span></span>

### <a name="whats-deployment-pipelines-in-power-bi"></a><span data-ttu-id="ce4f0-106">ไปป์ไลน์การปรับใช้ใน Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="ce4f0-106">What's deployment pipelines in Power BI?</span></span>

<span data-ttu-id="ce4f0-107">เมื่อต้องการทำความเข้าใจเกี่ยวกับการปรับใช้ไปป์ไลน์ใน Power BI โปรดดู [ภาพรวมของไปป์ไลน์การปรับใช้](deployment-pipelines-overview.md)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-107">To understand what's deployment pipelines in Power BI, refer to the [deployment pipelines overview](deployment-pipelines-overview.md).</span></span>

### <a name="how-do-i-get-started-with-deployment-pipelines"></a><span data-ttu-id="ce4f0-108">ฉันจะเริ่มต้นอย่างไรกับไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-108">How do I get started with deployment pipelines?</span></span>

<span data-ttu-id="ce4f0-109">เริ่มต้นไปป์ไลน์การปรับใช้โดยใช้ [คำแนะนำเริ่มต้น](deployment-pipelines-get-started.md)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-109">Get started with deployment pipelines using the [get started instructions](deployment-pipelines-get-started.md).</span></span>

### <a name="why-cant-i-see-the-deployment-pipelines-button"></a><span data-ttu-id="ce4f0-110">เหตุใดฉันจึงไม่เห็นปุ่มไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-110">Why can't I see the deployment pipelines button?</span></span>

<span data-ttu-id="ce4f0-111">ถ้าไม่เป็นไปตามเงื่อนไขต่อไปนี้คุณจะไม่สามารถดูปุ่มไปป์ไลน์การปรับใช้ได้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-111">If the following conditions are not met, you'll not be able to see the deployment pipelines button.</span></span>

* <span data-ttu-id="ce4f0-112">คุณมีสิทธิการใช้งาน Premium ต่อไปนี้หนึ่งรายการ:</span><span class="sxs-lookup"><span data-stu-id="ce4f0-112">You have one of the following Premium licenses:</span></span>

    * <span data-ttu-id="ce4f0-113">คุณเป็นผู้ใช้ Power BI แบบ [Pro](../admin/service-admin-purchasing-power-bi-pro.md) และคุณเป็นสมาชิกขององค์กรที่มีความจุแบบ Premium</span><span class="sxs-lookup"><span data-stu-id="ce4f0-113">You're a Power BI [Pro user](../admin/service-admin-purchasing-power-bi-pro.md), and you belong to an organization that has Premium capacity.</span></span>

    * <span data-ttu-id="ce4f0-114">[Premium Per User (PPU)](../admin/service-premium-per-user-faq.md)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-114">[Premium Per User (PPU)](../admin/service-premium-per-user-faq.md).</span></span>

* <span data-ttu-id="ce4f0-115">คุณเป็นผู้ดูแลระบบของ[ประสบการณ์ในพื้นที่ทำงานใหม่](../collaborate-share/service-create-the-new-workspaces.md)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-115">You're an admin of a [new workspace experience](../collaborate-share/service-create-the-new-workspaces.md).</span></span>

### <a name="why-cant-i-see-the-pipeline-stage-tag-in-my-workspace"></a><span data-ttu-id="ce4f0-116">เหตุใดฉันจึงไม่เห็นแท็กขั้นตอนไปป์ไลน์ในพื้นที่ทำงานของฉัน</span><span class="sxs-lookup"><span data-stu-id="ce4f0-116">Why can't I see the pipeline stage tag in my workspace?</span></span>

<span data-ttu-id="ce4f0-117">ไปป์ไลน์การปรับใช้จะแสดงแท็กขั้นตอนไปป์ไลน์ในพื้นที่ทำงานที่กำหนดให้กับไปป์ไลน์</span><span class="sxs-lookup"><span data-stu-id="ce4f0-117">Deployment pipelines displays a pipeline stage tag in workspaces that are assigned to a pipeline.</span></span> <span data-ttu-id="ce4f0-118">แท็กสำหรับขั้นตอน *การพัฒนา* และ *การทดสอบ* จะมองเห็นได้เสมอ</span><span class="sxs-lookup"><span data-stu-id="ce4f0-118">Tags for the *Development* and *Test* stages are always visible.</span></span> <span data-ttu-id="ce4f0-119">อย่างไรก็ตาม คุณจะเห็นแท็ก *การผลิต* เท่านั้นถ้าคุณมี [สิทธิ์ในการเข้าถึงไปป์ไลน์](deployment-pipelines-process.md#user-with-pipeline-access) หรือถ้าคุณเป็น [ผู้ดูแลระบบพื้นที่ทำงาน](deployment-pipelines-process.md#workspace-admin)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-119">However, you'll only see the *Production* tag if you have [access to the pipeline](deployment-pipelines-process.md#user-with-pipeline-access) or if you're a [workspace admin](deployment-pipelines-process.md#workspace-admin).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="ce4f0-120">![สกรีนช็อตของแท็กการผลิตในพื้นที่ทำงานของไปป์ไลน์การผลิต](media/deployment-pipelines-troubleshooting/production-tag.png)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-120">![A screenshot of the production tag in a production pipeline workspace.](media/deployment-pipelines-troubleshooting/production-tag.png)</span></span>

## <a name="licensing"></a><span data-ttu-id="ce4f0-121">สิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ce4f0-121">Licensing</span></span>

### <a name="what-licenses-are-needed-to-work-with-deployment-pipelines"></a><span data-ttu-id="ce4f0-122">สิทธิ์การใช้งานใดที่จำเป็นในการดำเนินการไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-122">What licenses are needed to work with deployment pipelines?</span></span>

<span data-ttu-id="ce4f0-123">หากต้องการใช้ไปป์ไลน์การปรับใช้ คุณจำเป็นต้องมีสิทธิการใช้งานใดสิทธิการใช้งานหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ce4f0-123">To use deployment pipelines, you need to have one of the following licenses:</span></span>

* <span data-ttu-id="ce4f0-124">สิทธิการใช้งานของ[ผู้ใช้ Pro](../admin/service-admin-purchasing-power-bi-pro.md) ที่มีพื้นที่ทำงานที่อยู่บน[ความจุรแบบ Premium](../admin/service-premium-what-is.md)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-124">A [Pro user](../admin/service-admin-purchasing-power-bi-pro.md) license, with a workspace that resides on a [Premium capacity](../admin/service-premium-what-is.md).</span></span>

* <span data-ttu-id="ce4f0-125">[Premium Per User (PPU)](../admin/service-premium-per-user-faq.md)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-125">[Premium Per User (PPU)](../admin/service-premium-per-user-faq.md).</span></span>

<span data-ttu-id="ce4f0-126">สำหรับข้อมูลเพิ่มเติม ดู [การเข้าถึงไปป์ไลน์การปรับใช้](deployment-pipelines-get-started.md#accessing-deployment-pipelines)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-126">For more information, see [accessing deployment pipelines](deployment-pipelines-get-started.md#accessing-deployment-pipelines).</span></span>

### <a name="what-type-of-capacity-can-i-assign-to-a-workspace-in-a-pipeline"></a><span data-ttu-id="ce4f0-127">ฉันสามารถกำหนดความจุชนิดใดให้กับพื้นที่ทำงานในไปป์ไลน์ได้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-127">What type of capacity can I assign to a workspace in a pipeline?</span></span>

<span data-ttu-id="ce4f0-128">พื้นที่ทำงานทั้งหมดในขั้นตอนการปรับใช้จะต้องอยู่ภายในความจุสำหรับไปป์ไลน์เพื่อให้สามารถใช้ได้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-128">All workspaces in a deployment pipeline must reside within a capacity for the pipeline to be functional.</span></span> <span data-ttu-id="ce4f0-129">อย่างไรก็ตามคุณสามารถใช้ความจุที่แตกต่างกันสำหรับพื้นที่ทำงานที่แตกต่างกันในไปป์ไลน์</span><span class="sxs-lookup"><span data-stu-id="ce4f0-129">However, you can use different capacities for different workspaces in a pipeline.</span></span> <span data-ttu-id="ce4f0-130">คุณยังสามารถใช้ชนิดความจุที่แตกต่างกันสำหรับพื้นที่ทำงานที่แตกต่างกันในไปป์ไลน์เดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-130">You can also use different capacity types for different workspaces in the same pipeline.</span></span>

<span data-ttu-id="ce4f0-131">สำหรับการพัฒนาและการทดสอบ คุณสามารถใช้ความจุ A หรือ EM ควบคู่ไปกับบัญชี Pro Power BI สำหรับผู้ใช้แต่ละราย</span><span class="sxs-lookup"><span data-stu-id="ce4f0-131">For development and testing, you can use A or EM capacity alongside a Pro Power BI account for each user.</span></span> <span data-ttu-id="ce4f0-132">คุณยังสามารถใช้ PPU สำหรับผู้ใช้แต่ละรายในขั้นตอนการพัฒนาและการทดสอบได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="ce4f0-132">You can also use a PPU for each user in the development and test stages.</span></span>

<span data-ttu-id="ce4f0-133">สำหรับพื้นที่ทำงานการผลิต คุณต้องมีความจุ P</span><span class="sxs-lookup"><span data-stu-id="ce4f0-133">For production workspaces, you need a P capacity.</span></span> <span data-ttu-id="ce4f0-134">ถ้าคุณเป็น ISV แจกจ่ายเนื้อหาผ่านแอปพลิเคชันแบบฝังตัวคุณยังสามารถใช้ความจุ A หรือ EM สำหรับการผลิตได้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-134">If you're an ISV distributing content through embedded applications, you can also use A or EM capacities for production.</span></span> <span data-ttu-id="ce4f0-135">นอกจากนี้ PPUs ยังสามารถใช้สำหรับพื้นที่ทำงานการผลิต</span><span class="sxs-lookup"><span data-stu-id="ce4f0-135">PPUs can also be used for production workspaces.</span></span>

>[!NOTE]
><span data-ttu-id="ce4f0-136">เมื่อคุณสร้างพื้นที่ทำงานด้วย PPU เฉพาะผู้ใช้ PPU รายอื่นเท่านั้นที่จะสามารถเข้าถึงพื้นที่ทำงานและใช้เนื้อหาได้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-136">When you create a workspace with a PPU, only other PPU users will be able to access the workspace and consume its content.</span></span>

## <a name="technical"></a><span data-ttu-id="ce4f0-137">ทางเทคนิค</span><span class="sxs-lookup"><span data-stu-id="ce4f0-137">Technical</span></span>

### <a name="why-cant-i-see-all-my-workspaces-when-i-try-to-assign-a-workspace-to-a-pipeline"></a><span data-ttu-id="ce4f0-138">เหตุใดฉันจึงไม่สามารถดูพื้นที่ทำงานของฉันทั้งหมดได้เมื่อฉันพยายามกำหนดพื้นที่ทำงานให้กับไปป์ไลน์</span><span class="sxs-lookup"><span data-stu-id="ce4f0-138">Why can't I see all my workspaces when I try to assign a workspace to a pipeline?</span></span>

<span data-ttu-id="ce4f0-139">เมื่อต้องการกำหนดพื้นที่ทำงานให้กับไปป์ไลน์ต้องเป็นไปตามเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ce4f0-139">To assign a workspace to a pipeline, the following conditions must be met:</span></span>

* <span data-ttu-id="ce4f0-140">พื้นที่ทำงานเป็น [ประสบการณ์พื้นที่ทำงานใหม่](../collaborate-share/service-create-the-new-workspaces.md)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-140">The workspace is a [new workspace experience](../collaborate-share/service-create-the-new-workspaces.md)</span></span>

* <span data-ttu-id="ce4f0-141">คุณเป็นผู้ดูแลระบบของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="ce4f0-141">You're an admin of the workspace</span></span>

* <span data-ttu-id="ce4f0-142">พื้นที่ทำงานไม่ได้ถูกกำหนดให้กับไปป์ไลน์อื่น</span><span class="sxs-lookup"><span data-stu-id="ce4f0-142">The workspace is not assigned to any other pipeline</span></span>

* <span data-ttu-id="ce4f0-143">พื้นที่ทำงานอยู่บน [ความจุแบบพรีเมียม](../admin/service-premium-what-is.md)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-143">The workspace resides on a [premium capacity](../admin/service-premium-what-is.md)</span></span>

<span data-ttu-id="ce4f0-144">พื้นที่ทำงานที่ไม่เป็นไปตามเงื่อนไขเหล่านี้จะไม่แสดงในรายการของพื้นที่ทำงานที่คุณสามารถเลือกได้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-144">Workspaces that don't meet these conditions, are not displayed in the list of workspaces you can select from.</span></span>

### <a name="how-can-i-assign-workspaces-to-all-the-stages-in-a-pipeline"></a><span data-ttu-id="ce4f0-145">ฉันสามารถกำหนดพื้นที่ทำงานให้กับขั้นตอนทั้งหมดในไปป์ไลน์ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="ce4f0-145">How can I assign workspaces to all the stages in a pipeline?</span></span>

<span data-ttu-id="ce4f0-146">คุณสามารถกำหนดพื้นที่ทำงานได้หนึ่งรายการต่อไปป์ไลน์</span><span class="sxs-lookup"><span data-stu-id="ce4f0-146">You can assign one workspace per pipeline.</span></span> <span data-ttu-id="ce4f0-147">เมื่อพื้นที่ทำงานถูกกำหนดให้กับไปป์ไลน์คุณสามารถปรับใช้กับขั้นตอนไปป์ไลน์ถัดไปได้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-147">Once a workspace is assigned to a pipeline, you can deploy it to the next pipeline stages.</span></span> <span data-ttu-id="ce4f0-148">ในระหว่างการปรับใช้ครั้งแรก พื้นที่ทำงานใหม่จะถูกสร้างขึ้นด้วยสำเนาของรายการในขั้นตอนต้นทาง</span><span class="sxs-lookup"><span data-stu-id="ce4f0-148">During first-time deployment, a new workspace is created with copies of the items in the source stage.</span></span> <span data-ttu-id="ce4f0-149">ความสัมพันธ์ของรายการที่คัดลอกจะถูกเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-149">The relationships of the copied items are kept.</span></span> <span data-ttu-id="ce4f0-150">สำหรับข้อมูลเพิ่มเติม ดูวิธีการ [กำหนดพื้นที่ทำงานให้กับไปป์ไลน์การปรับใช้](deployment-pipelines-get-started.md#step-2---assign-a-workspace-to-a-deployment-pipeline)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-150">For more information, see how to [assign a workspace to a deployment pipeline](deployment-pipelines-get-started.md#step-2---assign-a-workspace-to-a-deployment-pipeline).</span></span>

### <a name="why-did-my-first-deployment-fail"></a><span data-ttu-id="ce4f0-151">เหตุใดการปรับใช้ครั้งแรกของฉันจึงล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="ce4f0-151">Why did my first deployment fail?</span></span>

<span data-ttu-id="ce4f0-152">การปรับใช้ครั้งแรกของคุณอาจล้มเหลวเนื่องจากมีเหตุผลหลายประการ</span><span class="sxs-lookup"><span data-stu-id="ce4f0-152">Your first deployment may have failed due to a number of reasons.</span></span> <span data-ttu-id="ce4f0-153">บางสาเหตุเหล่านี้จะแสดงอยู่ในตารางด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="ce4f0-153">Some of these reasons are listed in the table below.</span></span>

|<span data-ttu-id="ce4f0-154">ข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="ce4f0-154">Error</span></span>  |<span data-ttu-id="ce4f0-155">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="ce4f0-155">Action</span></span>  |
|---------|---------|
|<span data-ttu-id="ce4f0-156">คุณไม่มี [สิทธิ์ความจุแบบพรีเมียม](deployment-pipelines-process.md#creating-a-premium-capacity-workspace)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-156">You don't have [premium capacity permissions](deployment-pipelines-process.md#creating-a-premium-capacity-workspace).</span></span>     |<span data-ttu-id="ce4f0-157">หากคุณทำงานในองค์กรที่มีความจุแบบ Premium คุณสามารถขอให้ผู้ดูแลความจุเพิ่มพื้นที่ทำงานของคุณไปยังความจุ หรือขอสิทธิ์ในการกำหนดสำหรับความจุ</span><span class="sxs-lookup"><span data-stu-id="ce4f0-157">If you work in an organization that has a Premium capacity, ask a capacity admin to add your workspace to a capacity, or ask for assignment permissions for the capacity.</span></span> <span data-ttu-id="ce4f0-158">หลังจากที่พื้นที่ทำงานอยู่ในความจุให้ปรับใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="ce4f0-158">After the workspace is in a capacity, redeploy.</span></span></br></br><span data-ttu-id="ce4f0-159">ถ้าคุณไม่ได้ทำงานในองค์กรที่มีความจุแบบ Premium ให้พิจารณาซื้อ [Premium Per User (PPU)](../admin/service-premium-per-user-faq.md)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-159">If you don't work in an organization with Premium capacity, consider purchasing [Premium Per User (PPU)](../admin/service-premium-per-user-faq.md).</span></span>        |
|<span data-ttu-id="ce4f0-160">คุณไม่มีสิทธิ์ในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="ce4f0-160">You don't have workspace permissions.</span></span>     |<span data-ttu-id="ce4f0-161">หากต้องการปรับใช้ คุณจะต้องเป็นสมาชิกพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="ce4f0-161">To deploy, you need to be a workspace member.</span></span> <span data-ttu-id="ce4f0-162">ขอให้ผู้ดูแลระบบพื้นที่ทำงานของคุณมอบสิทธิ์ที่เหมาะสมให้แก่คุณ</span><span class="sxs-lookup"><span data-stu-id="ce4f0-162">Ask your workspace admin to grant you the appropriate permissions.</span></span>         |
|<span data-ttu-id="ce4f0-163">ผู้ดูแลระบบ Power BI ของคุณได้ปิดใช้งานการสร้างพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="ce4f0-163">Your Power BI admin disabled the creation of workspaces.</span></span>     |<span data-ttu-id="ce4f0-164">ติดต่อผู้ดูแลระบบ Power BI ของคุณเพื่อขอรับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="ce4f0-164">Contact your Power BI admin for support.</span></span>         |
|<span data-ttu-id="ce4f0-165">พื้นที่ทำงานของคุณไม่เป็น [ประสบการณ์พื้นที่ทำงานใหม่](../collaborate-share/service-create-the-new-workspaces.md)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-165">Your workspace isn't a [new workspace experience](../collaborate-share/service-create-the-new-workspaces.md).</span></span>     |<span data-ttu-id="ce4f0-166">สร้างเนื้อหาของคุณในประสบการณ์พื้นที่ทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="ce4f0-166">Create your content in the new workspace experience.</span></span> <span data-ttu-id="ce4f0-167">ถ้าคุณมีเนื้อหาในพื้นที่ทำงานคลาสสิกคุณสามารถ [อัปเกรด](../collaborate-share/service-upgrade-workspaces.md) ไปยังประสบการณ์พื้นที่ทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="ce4f0-167">If you have content in a classic workspace, you can [upgrade](../collaborate-share/service-upgrade-workspaces.md) it to a new workspace experience.</span></span>         |
|<span data-ttu-id="ce4f0-168">คุณกำลังใช้ [การปรับใช้แบบเลือก](deployment-pipelines-get-started.md#selective-deployment) และไม่ได้เลือกชุดข้อมูลของเนื้อหาของคุณ</span><span class="sxs-lookup"><span data-stu-id="ce4f0-168">You're using [selective deployment](deployment-pipelines-get-started.md#selective-deployment) and are not selecting your content's dataset.</span></span>     |<span data-ttu-id="ce4f0-169">ทำรายการใดรายการหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ce4f0-169">Do one of the following:</span></span> </br></br><span data-ttu-id="ce4f0-170">ยกเลิกการเลือกเนื้อหาที่เชื่อมโยงกับชุดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="ce4f0-170">Unselect the content that is linked to your dataset.</span></span> <span data-ttu-id="ce4f0-171">เนื้อหาที่ไม่ได้เลือกของคุณ (เช่นรายงานหรือแดชบอร์ด) จะไม่ถูกคัดลอกไปยังขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="ce4f0-171">Your unselected content (such as reports or dashboards) will not be copied to the next stage.</span></span> </br></br><span data-ttu-id="ce4f0-172">เลือกชุดข้อมูลที่เชื่อมโยงกับเนื้อหาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ce4f0-172">Select the dataset that's linked to the selected content.</span></span> <span data-ttu-id="ce4f0-173">ชุดข้อมูลของคุณจะถูกคัดลอกไปยังขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="ce4f0-173">Your dataset will be copied to the next stage.</span></span>         |

### <a name="im-getting-a-warning-that-i-have-unsupported-artifacts-in-my-workspace-when-im-trying-to-deploy-how-can-i-know-which-artifacts-are-not-supported"></a><span data-ttu-id="ce4f0-174">ฉันได้รับคำเตือนว่าฉันมี 'วัตถุที่ไม่ได้รับการรองรับ' ในพื้นที่ทำงานของฉันเมื่อฉันพยายามปรับใช้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-174">I'm getting a warning that I have 'unsupported artifacts' in my workspace when I'm trying to deploy.</span></span> <span data-ttu-id="ce4f0-175">ฉันจะทราบได้อย่างไรว่าวัตถุใดที่ไม่ได้รับการรองรับ</span><span class="sxs-lookup"><span data-stu-id="ce4f0-175">How can I know which artifacts are not supported?</span></span>

<span data-ttu-id="ce4f0-176">สำหรับรายการที่ครอบคลุมของรายการและวัตถุที่ไม่ได้รับการรองรับในไปป์ไลน์การปรับใช้ดูส่วนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ce4f0-176">For a comprehensive list of items and artifacts that are not supported in deployment pipelines, see the following sections:</span></span>

* [<span data-ttu-id="ce4f0-177">รายการที่ไม่รองรับ</span><span class="sxs-lookup"><span data-stu-id="ce4f0-177">Unsupported items</span></span>](deployment-pipelines-process.md#unsupported-items)

* [<span data-ttu-id="ce4f0-178">คุณสมบัติรายการที่ไม่ได้คัดลอก</span><span class="sxs-lookup"><span data-stu-id="ce4f0-178">Item properties that are not copied</span></span>](deployment-pipelines-process.md#item-properties-that-are-not-copied)

### <a name="why-did-my-deployment-fail-due-to-broken-rules"></a><span data-ttu-id="ce4f0-179">ทำไมการปรับใช้ของฉันล้มเหลวเนื่องจากกฎที่เสียหาย</span><span class="sxs-lookup"><span data-stu-id="ce4f0-179">Why did my deployment fail due to broken rules?</span></span>

<span data-ttu-id="ce4f0-180">ถ้าคุณมีปัญหาในการกำหนดค่ากฎของชุดข้อมูลให้เยี่ยมชม [กฎชุดข้อมูล](deployment-pipelines-get-started.md#step-4---create-dataset-rules)และตรวจสอบให้แน่ใจว่าคุณได้ทำตาม [ข้อจำกัดของกฎชุดข้อมูล](deployment-pipelines-get-started.md#dataset-rule-limitations)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-180">If you have problems configuring dataset rules, visit [dataset rules](deployment-pipelines-get-started.md#step-4---create-dataset-rules), and make sure you follow the [dataset rule limitations](deployment-pipelines-get-started.md#dataset-rule-limitations).</span></span>

<span data-ttu-id="ce4f0-181">ถ้าการปรับใช้ของคุณได้รับการดำเนินการสำเร็จก่อนหน้านี้และไม่สามารถทำงานกับกฎที่เสียหายแบบฉับพลันได้ อาจเกิดจากชุดข้อมูลถูกเผยแพร่ใหม่</span><span class="sxs-lookup"><span data-stu-id="ce4f0-181">If your deployment was previously successful, and is suddenly failing with broken rules, it may be due to a dataset being republished.</span></span> <span data-ttu-id="ce4f0-182">การเปลี่ยนแปลงต่อไปนี้ไปยังชุดข้อมูลต้นทางให้ผลลัพธ์ในการปรับใช้ล้มเหลว:</span><span class="sxs-lookup"><span data-stu-id="ce4f0-182">The following changes to the source dataset, result in a failed deployment:</span></span>

<span data-ttu-id="ce4f0-183">**กฎพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="ce4f0-183">**Parameter rules**</span></span>

* <span data-ttu-id="ce4f0-184">พารามิเตอร์ที่ถูกเอาออก</span><span class="sxs-lookup"><span data-stu-id="ce4f0-184">A removed parameter</span></span>

* <span data-ttu-id="ce4f0-185">ชื่อพารามิเตอร์ที่มีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="ce4f0-185">A changed parameter name</span></span>

<span data-ttu-id="ce4f0-186">**กฎของแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="ce4f0-186">**Data source rules**</span></span>

<span data-ttu-id="ce4f0-187">กฎชุดข้อมูลของคุณมีค่าที่ขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="ce4f0-187">Your dataset rules are missing values.</span></span> <span data-ttu-id="ce4f0-188">ซึ่งอาจเกิดขึ้นหากมีการเปลี่ยนแปลงชุดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="ce4f0-188">This may have happened if your dataset changed.</span></span>

![สกรีนช็อตของข้อผิดพลาดของกฎที่ไม่ถูกต้องแสดงขึ้นเมื่อการปรับใช้ล้มเหลวเนื่องจากลิงก์เสียหาย](media/deployment-pipelines-troubleshooting/broken-rule.png)

<span data-ttu-id="ce4f0-190">เมื่อการปรับใช้ที่สำเร็จก่อนหน้านี้ล้มเหลวเนื่องจากลิงก์ที่เสียหาย คำเตือนจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="ce4f0-190">When a previously successful deployment fails due to broken links, a warning is displayed.</span></span> <span data-ttu-id="ce4f0-191">คุณสามารถเลือก **กำหนดค่ากฎ** เพื่อนำทางไปยังแผงการตั้งค่าการปรับใช้ที่มีการทำเครื่องหมายชุดข้อมูลที่ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="ce4f0-191">You can select **Configure rules** to navigate to the deployment settings pane, where the failed dataset is marked.</span></span> <span data-ttu-id="ce4f0-192">เมื่อคุณเลือกชุดข้อมูล กฎที่ถูกฝ่าฝืนจะถูกทำเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="ce4f0-192">When you select the dataset, the broken rules are marked.</span></span>

<span data-ttu-id="ce4f0-193">เมื่อต้องการปรับใช้สำเร็จ ให้แก้ไขหรือลบกฎที่เสียหายและปรับใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="ce4f0-193">To deploy successfully, fix or remove the broken rules, and redeploy.</span></span>

### <a name="how-can-i-change-the-data-source-in-the-pipeline-stages"></a><span data-ttu-id="ce4f0-194">ฉันจะเปลี่ยนแหล่งข้อมูลในขั้นตอนไปป์ไลน์ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="ce4f0-194">How can I change the data source in the pipeline stages?</span></span>

<span data-ttu-id="ce4f0-195">คุณไม่สามารถเปลี่ยนการเชื่อมต่อแหล่งข้อมูลในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="ce4f0-195">You can’t change the data source connection in Power BI service.</span></span>

<span data-ttu-id="ce4f0-196">ถ้าคุณต้องการเปลี่ยนแหล่งข้อมูลในขั้นตอนการทดสอบหรือการผลิตคุณสามารถใช้ [กฎชุดข้อมูล](deployment-pipelines-get-started.md#step-4---create-dataset-rules) หรือ [Api](/rest/api/power-bi/datasets/updateparametersingroup)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-196">If you want to change the data source in the test or production stages, you can use [dataset rules](deployment-pipelines-get-started.md#step-4---create-dataset-rules) or [APIs](/rest/api/power-bi/datasets/updateparametersingroup).</span></span> <span data-ttu-id="ce4f0-197">กฎชุดข้อมูลจะมีผลหลังจากการปรับใช้ครั้งถัดไปเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ce4f0-197">Dataset rules will only come into effect after the next deployment.</span></span>

### <a name="i-fixed-a-bug-in-production-but-now-i-cant-select-the-deploy-to-previous-stage-button-why-is-it-greyed-out"></a><span data-ttu-id="ce4f0-198">ฉันแก้ไขบักในการผลิตแล้ว แต่ตอนนี้ฉันไม่สามารถเลือกปุ่ม "ปรับใช้กับขั้นตอนก่อนหน้า"</span><span class="sxs-lookup"><span data-stu-id="ce4f0-198">I fixed a bug in production, but now I can't select the 'deploy to previous stage' button.</span></span> <span data-ttu-id="ce4f0-199">เหตุใดจึงเป็นสีเทา</span><span class="sxs-lookup"><span data-stu-id="ce4f0-199">Why is it greyed out?</span></span>

<span data-ttu-id="ce4f0-200">คุณสามารถปรับใช้งานย้อนกลับไปยังขั้นตอนที่ว่างเปล่าได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ce4f0-200">You can only deploy backwards to an empty stage.</span></span> <span data-ttu-id="ce4f0-201">ถ้าคุณมีเนื้อหาในขั้นตอนการทดสอบคุณจะไม่สามารถปรับใช้งานย้อนหลังจากการผลิตได้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-201">If you have content in the test stage, you will not be able to deploy backwards from production.</span></span>

<span data-ttu-id="ce4f0-202">หลังจากสร้างไปป์ไลน์ให้ใช้ขั้นตอนการพัฒนาเพื่อพัฒนาเนื้อหาของคุณและขั้นตอนการทดสอบเพื่อตรวจทานและทดสอบ</span><span class="sxs-lookup"><span data-stu-id="ce4f0-202">After creating the pipeline, use the development stage to develop your content, and the test stages to review and test it.</span></span> <span data-ttu-id="ce4f0-203">คุณสามารถแก้ไขบักในขั้นตอนเหล่านี้และจากนั้นปรับใช้สภาพแวดล้อมแบบคงที่ไปยังขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="ce4f0-203">You can fix bugs in these stages, and then deploy the fixed environment to the production stage.</span></span>

>[!NOTE]
><span data-ttu-id="ce4f0-204">การปรับใช้ย้อนหลังรองรับเฉพาะ [การปรับใช้เต็มรูปแบบ](deployment-pipelines-get-started.md#deploying-all-content) เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ce4f0-204">Backwards deployment only supports [full deployment](deployment-pipelines-get-started.md#deploying-all-content).</span></span> <span data-ttu-id="ce4f0-205">ไม่รองรับ [การปรับใช้ที่เลือก](deployment-pipelines-get-started.md#selective-deployment)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-205">It doesn't support [selective deployment](deployment-pipelines-get-started.md#selective-deployment)</span></span>

### <a name="does-deployment-pipelines-support-multi-geo"></a><span data-ttu-id="ce4f0-206">ไปป์ไลน์การปรับใช้รองรับหลายพรมแดนหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="ce4f0-206">Does deployment pipelines support multi-geo?</span></span>

<span data-ttu-id="ce4f0-207">รองรับหลายพรมแดน</span><span class="sxs-lookup"><span data-stu-id="ce4f0-207">Multi-geo is supported.</span></span> <span data-ttu-id="ce4f0-208">ซึ่งอาจใช้เวลานานในการปรับใช้เนื้อหาระหว่างขั้นตอนในพรมแดนแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="ce4f0-208">It may take longer to deploy content between stages in different geos.</span></span>

## <a name="permissions"></a><span data-ttu-id="ce4f0-209">การอนุญาต</span><span class="sxs-lookup"><span data-stu-id="ce4f0-209">Permissions</span></span>

### <a name="what-is-the-deployment-pipelines-permissions-model"></a><span data-ttu-id="ce4f0-210">แบบจำลองสิทธิ์ของไปป์ไลน์การปรับใช้คืออะไร</span><span class="sxs-lookup"><span data-stu-id="ce4f0-210">What is the deployment pipelines permissions model?</span></span>

<span data-ttu-id="ce4f0-211">แบบจำลองสิทธิ์ของไปป์ไลน์การปรับใช้ได้รับการอธิบายไว้ในส่วน [สิทธิ์](deployment-pipelines-process.md#permissions)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-211">The deployment pipelines permissions model is described the [permissions](deployment-pipelines-process.md#permissions) section.</span></span>

### <a name="who-can-deploy-content-between-stages"></a><span data-ttu-id="ce4f0-212">ใครสามารถปรับใช้เนื้อหาระหว่างขั้นตอนได้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-212">Who can deploy content between stages?</span></span>

<span data-ttu-id="ce4f0-213">สามารถปรับใช้เนื้อหาไปยังขั้นตอนที่ว่างเปล่าหรือไปยังขั้นตอนที่มีเนื้อหาได้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-213">Content can be deployed to an empty stage or to a stage that contains content.</span></span> <span data-ttu-id="ce4f0-214">เนื้อหาต้องอยู่ใน [ความจุแบบพรีเมียม](../admin/service-premium-what-is.md)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-214">The content must reside on a [premium capacity](../admin/service-premium-what-is.md).</span></span>

* <span data-ttu-id="ce4f0-215">**การปรับใช้งานไปยังขั้นตอนที่ว่างเปล่า** - [ผู้ใช้ Pro](../admin/service-admin-purchasing-power-bi-pro.md) หรือ [PPU](../admin/service-premium-per-user-faq.md) ใดก็ตามที่เป็นสมาชิกหรือผู้ดูแลระบบในพื้นที่ทำงานต้นทาง</span><span class="sxs-lookup"><span data-stu-id="ce4f0-215">**Deploying to an empty stage** - Any [Pro](../admin/service-admin-purchasing-power-bi-pro.md) or [PPU](../admin/service-premium-per-user-faq.md) user, that's a member or admin in the source workspace.</span></span>

* <span data-ttu-id="ce4f0-216">**ปรับใช้กับขั้นตอนที่มีเนื้อหา** - [ผู้ใช้ Pro](../admin/service-admin-purchasing-power-bi-pro.md) หรือ [PPU](../admin/service-premium-per-user-faq.md) ใดก็ตามที่เป็นสมาชิกหรือผู้ดูแลระบบของทั้งสองพื้นที่ทำงานในขั้นตอนปรับใช้แหล่งที่มาและเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="ce4f0-216">**Deploying to a stage with content** - Any [Pro](../admin/service-admin-purchasing-power-bi-pro.md) or [PPU](../admin/service-premium-per-user-faq.md) user, who's a member or admin of both workspaces in the source and target deployment stages.</span></span>

* <span data-ttu-id="ce4f0-217">**การแทนที่ชุดข้อมูล** - การปรับใช้แทนที่แต่ละชุดข้อมูลที่รวมอยู่ในขั้นตอนเป้าหมายแม้ว่าจะไม่มีการเปลี่ยนแปลงชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ce4f0-217">**Overriding a dataset** - Deployment overrides each dataset that is included in the target stage, even if the dataset wasn't changed.</span></span> <span data-ttu-id="ce4f0-218">ผู้ใช้ต้องเป็นเจ้าของชุดข้อมูลในขั้นตอนเป้าหมายทั้งหมดที่ระบุในการปรับใช้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-218">The user must be the owner of all the target stage datasets specified in the deployment.</span></span>

### <a name="which-permissions-do-i-need-to-configure-dataset-rules"></a><span data-ttu-id="ce4f0-219">ฉันจำเป็นต้องใช้สิทธิ์ใดในการกำหนดค่ากฎชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ce4f0-219">Which permissions do I need to configure dataset rules?</span></span>

<span data-ttu-id="ce4f0-220">ในการกำหนดค่ากฎชุดข้อมูลในไปป์ไลน์การปรับใช้คุณต้องเป็นเจ้าของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ce4f0-220">To configure dataset rules in deployment pipelines, you must be the dataset owner.</span></span>

### <a name="why-cant-i-see-workspaces-in-the-pipeline"></a><span data-ttu-id="ce4f0-221">เหตุใดฉันจึงไม่เห็นพื้นที่ทำงานในไปป์ไลน์</span><span class="sxs-lookup"><span data-stu-id="ce4f0-221">Why can't I see workspaces in the pipeline?</span></span>

<span data-ttu-id="ce4f0-222">สิทธิ์ของไปป์ไลน์และพื้นที่ทำงานได้รับการจัดการแยกกัน</span><span class="sxs-lookup"><span data-stu-id="ce4f0-222">Pipeline and workspace permissions are managed separately.</span></span> <span data-ttu-id="ce4f0-223">คุณอาจมีสิทธิ์ในการใช้งานไปป์ไลน์ แต่ไม่สามารถใช้สิทธิ์ในพื้นที่ทำงานได้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-223">You may have pipeline permissions, but not workspace permissions.</span></span> <span data-ttu-id="ce4f0-224">สำหรับข้อมูลเพิ่มเติมให้ตรวจทานส่วน [สิทธิ์](deployment-pipelines-process.md#permissions)</span><span class="sxs-lookup"><span data-stu-id="ce4f0-224">For more information, review the [permissions](deployment-pipelines-process.md#permissions) section.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ce4f0-225">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="ce4f0-225">Next steps</span></span>

>[!div class="nextstepaction"]
>[<span data-ttu-id="ce4f0-226">บทนำไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-226">Introduction to deployment pipelines</span></span>](deployment-pipelines-overview.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="ce4f0-227">เริ่มต้นกับไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-227">Get started with deployment pipelines</span></span>](deployment-pipelines-get-started.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="ce4f0-228">ทำความเข้าใจกระบวนการไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-228">Understand the deployment pipelines process</span></span>](deployment-pipelines-process.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="ce4f0-229">แนวทางปฏิบัติที่ดีที่สุดสำหรับไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="ce4f0-229">Deployment pipelines best practices</span></span>](deployment-pipelines-best-practices.md)