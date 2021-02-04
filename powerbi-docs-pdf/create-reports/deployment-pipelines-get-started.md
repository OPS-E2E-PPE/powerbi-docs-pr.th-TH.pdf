---
title: เริ่มต้นกับไปป์ไลน์การปรับใช้
description: เรียนรู้วิธีใช้ไปป์ไลน์การปรับใช้ใน Power BI
author: KesemSharabi
ms.author: kesharab
ms.topic: how-to
ms.service: powerbi
ms.subservice: pbi-deployment
ms.custom: contperf-fy21q1
ms.date: 11/11/2020
ms.openlocfilehash: 9d0c10b80aeb1bf4745bb8a646933bcfea9bafc6
ms.sourcegitcommit: 7bf09116163afaae312eb2b232eb7967baee2c92
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/17/2020
ms.locfileid: "97621222"
---
# <a name="get-started-with-deployment-pipelines"></a><span data-ttu-id="49679-103">เริ่มต้นกับไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="49679-103">Get started with deployment pipelines</span></span>

<span data-ttu-id="49679-104">บทความนี้จะแนะนำการตั้งค่าพื้นฐานที่จำเป็นสำหรับการใช้ไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="49679-104">This article walks you through the basic settings required for using deployment pipelines.</span></span>

## <a name="accessing-deployment-pipelines"></a><span data-ttu-id="49679-105">การเข้าถึงไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="49679-105">Accessing deployment pipelines</span></span>

<span data-ttu-id="49679-106">คุณจะสามารถเข้าถึงคุณลักษณะของไปป์ไลน์การปรับใช้ได้ถ้าตรงตามเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="49679-106">You'll be able to access the deployment pipelines feature, if the following conditions are met:</span></span>

* <span data-ttu-id="49679-107">คุณมีสิทธิการใช้งาน Premium ต่อไปนี้หนึ่งรายการ:</span><span class="sxs-lookup"><span data-stu-id="49679-107">You have one of the following Premium licenses:</span></span>

    * <span data-ttu-id="49679-108">คุณเป็นผู้ใช้ Power BI แบบ [Pro](../admin/service-admin-purchasing-power-bi-pro.md) และคุณเป็นสมาชิกขององค์กรที่มีความจุแบบ Premium</span><span class="sxs-lookup"><span data-stu-id="49679-108">You're a Power BI [Pro user](../admin/service-admin-purchasing-power-bi-pro.md), and you belong to an organization that has Premium capacity.</span></span>

    * <span data-ttu-id="49679-109">[Premium Per User (PPU)](../admin/service-premium-per-user-faq.md)</span><span class="sxs-lookup"><span data-stu-id="49679-109">[Premium Per User (PPU)](../admin/service-premium-per-user-faq.md).</span></span>

* <span data-ttu-id="49679-110">คุณเป็นผู้ดูแลระบบของ[ประสบการณ์ในพื้นที่ทำงานใหม่](../collaborate-share/service-create-the-new-workspaces.md)</span><span class="sxs-lookup"><span data-stu-id="49679-110">You're an admin of a [new workspace experience](../collaborate-share/service-create-the-new-workspaces.md).</span></span>

>[!NOTE]
> <span data-ttu-id="49679-111">คุณยังสามารถดูปุ่มไปป์ไลน์การปรับใช้ถ้าคุณได้สร้างไปป์ไลน์ก่อนหน้านี้หรือถ้ามีการแชร์ไปป์ไลน์กับคุณ</span><span class="sxs-lookup"><span data-stu-id="49679-111">You'll also be able to see the deployment pipelines button, if you previously created a pipeline, or if a pipeline was shared with you.</span></span>

![สกรีนช็อตของหน้าเริ่มต้นขั้นตอนการปรับใช้](media/deployment-pipelines-get-started/creating-pipeline.png)

## <a name="step-1---create-a-deployment-pipeline"></a><span data-ttu-id="49679-113">ขั้นตอนที่ 1 - สร้างไปป์ไลน์การปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="49679-113">Step 1 - Create a deployment pipeline</span></span>

<span data-ttu-id="49679-114">คุณสามารถสร้างไปป์ไลน์จากแท็บไปป์ไลน์การปรับใช้หรือจากพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="49679-114">You can create a pipeline from the deployment pipelines tab, or from a workspace.</span></span>

<span data-ttu-id="49679-115">หลังจากสร้างไปป์ไลน์แล้วคุณสามารถแชร์กับผู้ใช้อื่นหรือลบออกได้</span><span class="sxs-lookup"><span data-stu-id="49679-115">After the pipeline is created, you can share it with other users or delete it.</span></span> <span data-ttu-id="49679-116">เมื่อคุณแชร์ไปป์ไลน์กับผู้อื่น ผู้ใช้ที่คุณแชร์ไปป์ไลน์จะได้รับการ [การเข้าถึงไปป์ไลน์](deployment-pipelines-process.md#user-with-pipeline-access)</span><span class="sxs-lookup"><span data-stu-id="49679-116">When you share a pipeline with others, the users you share the pipeline with will be given [access to the pipeline](deployment-pipelines-process.md#user-with-pipeline-access).</span></span> <span data-ttu-id="49679-117">การเข้าถึงไปป์ไลน์ช่วยให้ผู้ใช้สามารถดู แชร์ แก้ไข และลบไปป์ไลน์ได้</span><span class="sxs-lookup"><span data-stu-id="49679-117">Pipeline access enables users to view, share, edit, and delete the pipeline.</span></span>

### <a name="create-a-pipeline-from-the-deployment-pipelines-tab"></a><span data-ttu-id="49679-118">สร้างไปป์ไลน์จากแท็บไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="49679-118">Create a pipeline from the deployment pipelines tab</span></span>

<span data-ttu-id="49679-119">หากต้องการสร้างไปป์ไลน์จากแท็บไปป์ไลน์การปรับใช้ ให้เดินเนินการดังนี้:</span><span class="sxs-lookup"><span data-stu-id="49679-119">To create a pipeline from the deployment pipelines tab, do the following:</span></span>

1. <span data-ttu-id="49679-120">ใน Power BI service จากบานหน้าต่างนำทาง ให้เลือก **ไปป์ไลน์การปรับใช้** และจากนั้นเลือก **สร้างไปป์ไลน์**</span><span class="sxs-lookup"><span data-stu-id="49679-120">In Power BI service, from the navigation pane, select **Deployment pipelines** and then select **Create pipeline**.</span></span>

2. <span data-ttu-id="49679-121">ในกล่องโต้ตอบ *สร้างการปรับใช้ไปป์ไลน์* ใส่ชื่อและคำอธิบายสำหรับไปป์ไลน์และเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="49679-121">In the *Create a deployment pipeline* dialog box, enter a name and description for the pipeline, and select **Create**.</span></span>

### <a name="create-a-pipeline-from-a-workspace"></a><span data-ttu-id="49679-122">สร้างไปป์ไลน์จากพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="49679-122">Create a pipeline from a workspace</span></span>

<span data-ttu-id="49679-123">คุณสามารถสร้างไปป์ไลน์จากพื้นที่ทำงานที่มีอยู่แล้ว โดยถือว่าคุณคือผู้ดูแลระบบของ [ประสบการณ์พื้นที่ทำงานใหม่](../collaborate-share/service-create-the-new-workspaces.md)</span><span class="sxs-lookup"><span data-stu-id="49679-123">You can create a pipeline from an existing workspace, providing you're the admin of a [new workspace experience](../collaborate-share/service-create-the-new-workspaces.md).</span></span>

1. <span data-ttu-id="49679-124">จากพื้นที่ทำงาน ให้เลือก **สร้างไปป์ไลน์**</span><span class="sxs-lookup"><span data-stu-id="49679-124">From the workspace, select **Create a pipeline**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="49679-125">![สกรีนช็อตของปุ่มสร้างไปป์ไลน์ในพื้นที่ทำงาน](media/deployment-pipelines-get-started/workspace-deploy.png)</span><span class="sxs-lookup"><span data-stu-id="49679-125">![A screenshot of the create a pipeline button in a workspace.](media/deployment-pipelines-get-started/workspace-deploy.png)</span></span>

2. <span data-ttu-id="49679-126">ในกล่องโต้ตอบ *สร้างการปรับใช้ไปป์ไลน์* ใส่ชื่อและคำอธิบายสำหรับไปป์ไลน์และเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="49679-126">In the *Create a deployment pipeline* dialog box, enter a name and description for the pipeline, and select **Create**.</span></span>

>[!NOTE]
><span data-ttu-id="49679-127">ถ้าพื้นที่ทำงานไม่ได้อยู่ในความจุ Premium ขององค์กร หรือความจุ PPU ของคุณ คุณจะได้รับการแจ้งเตือนเพื่อ [กำหนดพื้นที่ทำงานให้กับความจุ](../admin/service-admin-premium-manage.md#assign-a-workspace-to-a-capacity)</span><span class="sxs-lookup"><span data-stu-id="49679-127">If the workspace isn't assigned to your organization's Premium capacity, or to your PPU capacity, you'll get a notification to [assign it to a capacity](../admin/service-admin-premium-manage.md#assign-a-workspace-to-a-capacity).</span></span>  

## <a name="step-2---assign-a-workspace-to-a-deployment-pipeline"></a><span data-ttu-id="49679-128">ขั้นตอนที่ 2 - กำหนดพื้นที่ทำงานให้กับไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="49679-128">Step 2 - Assign a workspace to a deployment pipeline</span></span>

<span data-ttu-id="49679-129">หลังจากสร้างไปป์ไลน์แล้ว คุณจำเป็นต้องเพิ่มเนื้อหาที่คุณต้องการจัดการไปยังไปป์ไลน์</span><span class="sxs-lookup"><span data-stu-id="49679-129">After creating a pipeline, you need to add the content you want to manage to the pipeline.</span></span> <span data-ttu-id="49679-130">การเพิ่มเนื้อหาลงในไปป์ไลน์จะทำได้โดยการกำหนดพื้นที่ทำงานให้กับขั้นตอนไปป์ไลน์</span><span class="sxs-lookup"><span data-stu-id="49679-130">Adding content to the pipeline is done by assigning a workspace to the pipeline stage.</span></span> <span data-ttu-id="49679-131">คุณสามารถกำหนดพื้นที่ทำงานให้กับขั้นตอนใดๆได้</span><span class="sxs-lookup"><span data-stu-id="49679-131">You can assign a workspace to any stage.</span></span> 

<span data-ttu-id="49679-132">คุณสามารถกำหนดหนึ่งพื้นที่ทำงานให้กับไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="49679-132">You can assign one workspace to a deployment pipeline.</span></span> <span data-ttu-id="49679-133">ไปป์ไลน์การปรับใช้จะสร้างการลอกแบบ ของเนื้อหาพื้นที่ทำงานเพื่อใช้ในขั้นตอนที่แตกต่างกันของไปป์ไลน์</span><span class="sxs-lookup"><span data-stu-id="49679-133">Deployment pipelines will create clones of the workspace content, to be used in different stages of the pipeline.</span></span>

<span data-ttu-id="49679-134">ทำตามขั้นตอนเหล่านี้เพื่อกำหนดพื้นที่ทำงานในไปป์ไลน์การปรับใช้:</span><span class="sxs-lookup"><span data-stu-id="49679-134">Follow these steps to assign a workspace in a deployment pipeline:</span></span>

1. <span data-ttu-id="49679-135">ในไปป์ไลน์การปรับใช้ที่สร้างขึ้นใหม่ ให้เลือก **กำหนดพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="49679-135">In the newly created deployment pipeline, select **Assign a workspace**.</span></span>

2. <span data-ttu-id="49679-136">ในเมนูดรอปดาวน์ *เลือกพื้นที่ทำงาน* เลือกพื้นที่ทำงานที่คุณต้องการกำหนดให้กับไปป์ไลน์</span><span class="sxs-lookup"><span data-stu-id="49679-136">In the *Choose the workspace* drop-down menu, select the workspace you want to assign to the pipeline.</span></span>

    >[!NOTE]
    ><span data-ttu-id="49679-137">ถ้าคุณกำลังสร้างไปป์ไลน์จากพื้นที่ทำงาน คุณสามารถข้ามขั้นตอนนี้เนื่องจากมีการเลือกพื้นที่ทำงานอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="49679-137">If you're creating a pipeline from a workspace, you can skip this stage as the workspace is already selected.</span></span>

3. <span data-ttu-id="49679-138">เลือกขั้นตอนที่คุณต้องการกำหนดพื้นที่ทำงานให้</span><span class="sxs-lookup"><span data-stu-id="49679-138">Select the stage you want to assign the workspace to.</span></span>

### <a name="workspace-assignment-limitations"></a><span data-ttu-id="49679-139">ข้อจำกัดการกำหนดพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="49679-139">Workspace assignment limitations</span></span>

* <span data-ttu-id="49679-140">พื้นที่ทำงานต้องเป็น [ประสบการณ์ของพื้นที่ทำงานใหม่](../collaborate-share/service-create-the-new-workspaces.md)</span><span class="sxs-lookup"><span data-stu-id="49679-140">The workspace must be a [new workspace experience](../collaborate-share/service-create-the-new-workspaces.md).</span></span>

* <span data-ttu-id="49679-141">คุณต้องเป็นผู้ดูแลระบบของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="49679-141">You must be an admin of the workspace.</span></span>

* <span data-ttu-id="49679-142">พื้นที่ทำงานไม่ได้ถูกกำหนดให้กับไปป์ไลน์อื่น</span><span class="sxs-lookup"><span data-stu-id="49679-142">The workspace is not assigned to any other pipeline.</span></span>

* <span data-ttu-id="49679-143">พื้นที่ทำงานต้องอยู่ใน [ความจุแบบ Premium](../admin/service-premium-what-is.md)</span><span class="sxs-lookup"><span data-stu-id="49679-143">The workspace must reside on a [Premium capacity](../admin/service-premium-what-is.md).</span></span>

* <span data-ttu-id="49679-144">คุณไม่สามารถกำหนดพื้นที่ทำงานด้วย [ตัวอย่าง Power BI](../create-reports/sample-datasets.md) ไปยังขั้นตอนของไปป์ไลน์</span><span class="sxs-lookup"><span data-stu-id="49679-144">You cannot assign a workspace with [Power BI samples](../create-reports/sample-datasets.md) to a pipeline stage.</span></span>

>[!NOTE]
><span data-ttu-id="49679-145">เฉพาะพื้นที่ทำงานที่สามารถใช้กับไปป์ไลน์การปรับใช้เท่านั้นที่จะแสดงในรายการของพื้นที่ทำงานที่คุณสามารถเลือกได้</span><span class="sxs-lookup"><span data-stu-id="49679-145">Only workspaces that can be used with deployment pipelines, will show in the list of workspaces you can select from.</span></span>

## <a name="step-3---deploy-to-an-empty-stage"></a><span data-ttu-id="49679-146">ขั้นตอนที่ 3 - ปรับใช้กับขั้นตอนที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="49679-146">Step 3 - Deploy to an empty stage</span></span>

<span data-ttu-id="49679-147">[ผู้ใช้ Pro ใดๆ](../admin/service-admin-purchasing-power-bi-pro.md) ที่เป็นสมาชิกหรือผู้ดูแลระบบในพื้นที่ทำงานต้นทางสามารถปรับใช้เนื้อหาไปยังขั้นตอนที่ว่างเปล่า (ขั้นตอนที่ไม่มีเนื้อหา)</span><span class="sxs-lookup"><span data-stu-id="49679-147">Any [Pro user](../admin/service-admin-purchasing-power-bi-pro.md) that's a member or admin in the source workspace, can deploy content to an empty stage (a stage that doesn't contain content).</span></span> <span data-ttu-id="49679-148">พื้นที่ทำงานต้องอยู่ในความจุสำหรับการปรับใช้เพื่อให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="49679-148">The workspace must reside on a capacity for the deployment to be completed.</span></span>

<span data-ttu-id="49679-149">เมื่อปรับใช้เนื้อหาไปยังขั้นตอนที่ว่างเปล่า ความสัมพันธ์ระหว่างรายการจะถูกเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="49679-149">When deploying content to an empty stage, the relationships between the items are kept.</span></span> <span data-ttu-id="49679-150">ตัวอย่างเช่นรายงานที่ถูกผูกกับชุดข้อมูลในขั้นตอนแหล่งข้อมูลจะมีการลอกแบบควบคู่ไปกับชุดข้อมูลและโคลนจะถูกผูกไว้ในพื้นที่ทำงานเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="49679-150">For example, a report that is bound to a dataset in the source stage, will be cloned alongside its dataset, and the clones will be similarly bound in the target workspace.</span></span>

<span data-ttu-id="49679-151">เมื่อการปรับใช้เสร็จสมบูรณ์ ให้รีเฟรชชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49679-151">Once the deployment is complete, refresh the dataset.</span></span> <span data-ttu-id="49679-152">สำหรับข้อมูลเพิ่มเติม ดู [ปรับใช้เนื้อหาไปยังขั้นตอนที่ว่างเปล่า](deployment-pipelines-process.md#deploying-content-to-an-empty-stage)</span><span class="sxs-lookup"><span data-stu-id="49679-152">For more information, see [deploying content to an empty stage](deployment-pipelines-process.md#deploying-content-to-an-empty-stage).</span></span>

### <a name="deploying-all-content"></a><span data-ttu-id="49679-153">ปรับใช้เนื้อหาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="49679-153">Deploying all content</span></span>

<span data-ttu-id="49679-154">เลือกขั้นตอนที่จะปรับใช้และจากนั้นเลือกปุ่มปรับใช้</span><span class="sxs-lookup"><span data-stu-id="49679-154">Select the stage to deploy from and then select the deployment button.</span></span> <span data-ttu-id="49679-155">กระบวนการปรับใช้สร้างพื้นที่ทำงานซ้ำในขั้นตอนเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="49679-155">The deployment process creates a duplicate workspace in the target stage.</span></span> <span data-ttu-id="49679-156">พื้นที่ทำงานนี้ประกอบด้วยเนื้อหาทั้งหมดที่มีอยู่ในขั้นตอนปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="49679-156">This workspace includes all the content existing in the current stage.</span></span>

<span data-ttu-id="49679-157">[![สกรีนช็อตที่แสดงปุ่มปรับใช้สำหรับขั้นตอนการพัฒนาและทดสอบในไปป์ไลน์การปรับใช้งาน](media/deployment-pipelines-get-started/deploy.png)](media/deployment-pipelines-get-started/deploy.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="49679-157">[![A screenshot showing the deploy button for the development and test stages in a deployment pipeline.](media/deployment-pipelines-get-started/deploy.png)](media/deployment-pipelines-get-started/deploy.png#lightbox)</span></span>

### <a name="selective-deployment"></a><span data-ttu-id="49679-158">การปรับใช้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="49679-158">Selective deployment</span></span>

<span data-ttu-id="49679-159">เมื่อต้องการปรับใช้เฉพาะรายการที่ระบุ ให้เลือก **แสดงลิงก์เพิ่มเติม** แล้วจากนั้นเลือกรายการที่คุณต้องการปรับใช้</span><span class="sxs-lookup"><span data-stu-id="49679-159">To deploy only specific items, select the **Show more** link, and then select the items you wish to deploy.</span></span> <span data-ttu-id="49679-160">เมื่อคลิกปุ่มปรับใช้ เฉพาะรายการที่เลือกเท่านั้นที่จะถูกปรับใช้ในขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="49679-160">When clicking the deploy button, only the selected items are deployed to the next stage.</span></span>

<span data-ttu-id="49679-161">เนื่องจากแดชบอร์ด รายงาน และชุดข้อมูลที่เกี่ยวข้องและมีการขึ้นต่อกัน คุณสามารถใช้ปุ่มเลือกที่เกี่ยวข้องเพื่อตรวจสอบรายการทั้งหมดที่รายการเหล่านั้นจะขึ้นอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="49679-161">Since dashboards, reports and datasets are related and have dependencies, you can use the select related button to check all items that those items are dependent on.</span></span> <span data-ttu-id="49679-162">ตัวอย่างเช่นหากคุณต้องการปรับใช้รายงานไปยังขั้นตอนถัดไปการคลิกปุ่มเลือกที่เกี่ยวข้องจะทำเครื่องหมายชุดข้อมูลที่รายงานเชื่อมต่อด้วยเพื่อให้ทั้งคู่ใช้งานได้ทันทีและรายงานจะไม่แตก</span><span class="sxs-lookup"><span data-stu-id="49679-162">For example, if you want to deploy a report to the next stage, clicking the select related button will mark the dataset that the report is connected to, so that both will be deployed at once and the report will not break.</span></span>

<span data-ttu-id="49679-163">[![สกรีนช็อตที่แสดงตัวเลือกการปรับใช้งานในไปป์ไลน์การปรับใช้งานที่มีอยู่หลังจากเลือกตัวเลือกแสดงเพิ่มเติม](media/deployment-pipelines-get-started/selective-deploy.png)](media/deployment-pipelines-get-started/selective-deploy.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="49679-163">[![A screenshot showing the selective deploy option in deployment pipelines, available after selecting the show more option.](media/deployment-pipelines-get-started/selective-deploy.png)](media/deployment-pipelines-get-started/selective-deploy.png#lightbox)</span></span>

>[!NOTE]
> * <span data-ttu-id="49679-164">คุณไม่สามารถปรับใช้รายงานหรือแดชบอร์ดไปยังขั้นตอนถัดไปได้ถ้าไม่มีรายการที่ขึ้นอยู่ด้วยอยู่ในขั้นตอนที่คุณกำลังปรับใช้อยู่</span><span class="sxs-lookup"><span data-stu-id="49679-164">You can't deploy a report or dashboard to next stage if the items it's dependent on do not exist in the stage you are deploying to.</span></span>
> * <span data-ttu-id="49679-165">คุณอาจได้รับผลลัพธ์ที่ไม่คาดคิดถ้าคุณเลือกที่จะปรับใช้รายงานหรือแดชบอร์ดโดยไม่มีชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49679-165">You might get unexpected results if you choose to deploy a report or dashboard without its dataset.</span></span> <span data-ttu-id="49679-166">สิ่งนี้สามารถเกิดขึ้นได้เมื่อชุดข้อมูลในขั้นตอนเป้าหมายมีการเปลี่ยนแปลงและไม่เหมือนกับชุดข้อมูลในขั้นตอนที่คุณกำลังปรับใช้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="49679-166">This can happen when the dataset in the target stage, has changed and is no longer identical to the one in the stage you're deploying from.</span></span>

### <a name="backwards-deployment"></a><span data-ttu-id="49679-167">การปรับใช้ย้อนหลัง</span><span class="sxs-lookup"><span data-stu-id="49679-167">Backwards deployment</span></span>

<span data-ttu-id="49679-168">คุณสามารถเลือกที่จะปรับใช้เป็นขั้นตอนก่อนหน้า ตัวอย่างเช่นในสถานการณ์ที่คุณกำหนดพื้นที่ทำงานที่มีอยู่ให้กับขั้นตอนการผลิตและจากนั้นปรับใช้ย้อนกลับก่อนขั้นตอนทดสอบและจากนั้นไปที่การพัฒนา</span><span class="sxs-lookup"><span data-stu-id="49679-168">You can choose to deploy to a previous stage, for example in a scenario where you assign an existing workspace to a production stage and then deploy it backwards, first to the test stage, and then to the development one.</span></span>

<span data-ttu-id="49679-169">การปรับใช้ไปยังขั้นตอนก่อนหน้านี้จะทำงานเฉพาะเมื่อขั้นตอนก่อนหน้าว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="49679-169">Deploying to a previous stage works only if the previous stage is empty.</span></span> <span data-ttu-id="49679-170">เมื่อปรับใช้กับขั้นตอนก่อนหน้า คุณไม่สามารถเลือกรายการที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="49679-170">When deploying to a previous stage, you can't select specific items.</span></span> <span data-ttu-id="49679-171">เนื้อหาทั้งหมดในขั้นตอนจะถูกปรับใช้</span><span class="sxs-lookup"><span data-stu-id="49679-171">All content in the stage will be deployed.</span></span>

<span data-ttu-id="49679-172">[![สกรีนช็อตที่แสดงปุ่มปรับใช้กับขั้นตอนก่อนหน้าพร้อมใช้งานจากเมนูทดสอบหรือขั้นตอนการผลิต](media/deployment-pipelines-get-started/deploy-back.png)](media/deployment-pipelines-get-started/deploy-back.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="49679-172">[![A screenshot showing the deploy to previous stage button, available from the test or production stage menus.](media/deployment-pipelines-get-started/deploy-back.png)](media/deployment-pipelines-get-started/deploy-back.png#lightbox)</span></span>

## <a name="step-4---create-dataset-rules"></a><span data-ttu-id="49679-173">ขั้นตอนที่ 4 - สร้างกฎชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49679-173">Step 4 - Create dataset rules</span></span>

<span data-ttu-id="49679-174">เมื่อทำงานในไปป์ไลน์การปรับใช้ ขั้นตอนที่แตกต่างกันอาจมีการกำหนดค่าที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="49679-174">When working in a deployment pipeline, different stages may have different configurations.</span></span> <span data-ttu-id="49679-175">ตัวอย่างเช่น แต่ละขั้นตอนสามารถมีฐานข้อมูลที่แตกต่างกัน หรือพารามิเตอร์คิวรีที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="49679-175">For example, each stage can have different databases or different query parameters.</span></span> <span data-ttu-id="49679-176">ขั้นตอนการพัฒนาอาจคิวรีตัวอย่างข้อมูลจากฐานข้อมูลในขณะที่การทดสอบและขั้นตอนการผลิตคิวรีฐานข้อมูลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="49679-176">The development stage might query sample data from the database, while the test and production stages query the entire database.</span></span>

<span data-ttu-id="49679-177">เมื่อคุณปรับใช้เนื้อหาระหว่างขั้นตอนไปป์ไลน์ การกำหนดค่ากฎชุดข้อมูลช่วยให้คุณสามารถอนุญาตให้มีการเปลี่ยนแปลงกับเนื้อหาในขณะที่ยังคงมีการตั้งค่าบางอย่างได้</span><span class="sxs-lookup"><span data-stu-id="49679-177">When you deploy content between pipeline stages, configuring dataset rules enables you to allow changes to content, while keeping some settings intact.</span></span>

<span data-ttu-id="49679-178">กฎชุดข้อมูลถูกกำหนดบนแหล่งข้อมูลและพารามิเตอร์ในแต่ละชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49679-178">Dataset rules are defined on data sources and parameters, in each dataset.</span></span> <span data-ttu-id="49679-179">กฎชุดข้อมูลจะกำหนดค่าของแหล่งข้อมูลหรือพารามิเตอร์สำหรับชุดข้อมูลที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="49679-179">They determine the values of the data sources or parameters for a specific dataset.</span></span> <span data-ttu-id="49679-180">ตัวอย่างเช่น ถ้าคุณต้องการให้ชุดข้อมูลในขั้นตอนการผลิตชี้ไปยังฐานข้อมูลการผลิต คุณสามารถกำหนดกฎสำหรับการดำเนินการนี้ได้</span><span class="sxs-lookup"><span data-stu-id="49679-180">For example, if you want a dataset in a production stage to point to a production database, you can define a rule for this.</span></span> <span data-ttu-id="49679-181">มีการกำหนดกฎในขั้นตอนการผลิตภายใต้ชุดข้อมูลที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="49679-181">The rule is defined in the production stage, under the appropriate dataset.</span></span> <span data-ttu-id="49679-182">เมื่อกำหนดกฎแล้วเนื้อหาที่ปรับใช้จากการทดสอบไปยังการผลิตจะได้รับค่าตามที่กำหนดในกฎชุดข้อมูลและจะมีผลตลอดเวลาตราบเท่าที่กฎไม่เปลี่ยนแปลงและถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="49679-182">Once the rule is defined, content deployed from test to production, will inherit the value as defined in the dataset rule, and will always apply as long as the rule is unchanged and valid.</span></span>

>[!NOTE]
> <span data-ttu-id="49679-183">กฎชุดข้อมูลจะทำงานเฉพาะเมื่อแหล่งข้อมูลต้นทางและเป้าหมายเป็นชนิดเดียวกันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="49679-183">Dataset rules work only when the source and target data source are of the same type.</span></span>

### <a name="create-a-dataset-rule"></a><span data-ttu-id="49679-184">สร้างกฎชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49679-184">Create a dataset rule</span></span>

1. <span data-ttu-id="49679-185">ในขั้นตอนไปป์ไลน์ที่คุณต้องการสร้างกฎชุดข้อมูล ให้เลือก **การตั้งค่าการปรับใช้**</span><span class="sxs-lookup"><span data-stu-id="49679-185">In the pipeline stage you want to create a dataset rule for, select **Deployment settings**.</span></span>

    ![สกรีนช็อตของปุ่มการตั้งค่าการปรับใช้ตั้งอยู่ที่ด้านขวาบนของแต่ละขั้นตอนไปป์ไลน์การปรับใช้งาน](media/deployment-pipelines-get-started/deployment-settings.png)

2. <span data-ttu-id="49679-187">จากบานหน้าต่างการตั้งค่าการปรับใช้ เลือกชุดข้อมูลที่คุณต้องการสร้างกฎ</span><span class="sxs-lookup"><span data-stu-id="49679-187">From the Deployment settings pane, select the dataset you want to create a rule for.</span></span>

    <span data-ttu-id="49679-188">[![สกรีนช็อตที่แสดงการเลือกชุดข้อมูลสำหรับการสร้างกฎชุดข้อมูล](media/deployment-pipelines-get-started/dataset-rules.png)](media/deployment-pipelines-get-started/dataset-rules.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="49679-188">[![A screenshot showing selecting a dataset for creating a dataset rule.](media/deployment-pipelines-get-started/dataset-rules.png)](media/deployment-pipelines-get-started/dataset-rules.png#lightbox)</span></span>

3. <span data-ttu-id="49679-189">เลือกชนิดของกฎที่คุณต้องการสร้าง ขยายรายการและจากนั้นเลือก **เพิ่มกฎ**</span><span class="sxs-lookup"><span data-stu-id="49679-189">Select the type of rule you want to create, expand the list, and then select **Add rule**.</span></span>

     <span data-ttu-id="49679-190">[![สกรีนช็อตที่แสดงการเลือกกฎแหล่งข้อมูลและคลิกเพิ่มตัวเลือกกฎ](media/deployment-pipelines-get-started/add-rule.png)](media/deployment-pipelines-get-started/add-rule.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="49679-190">[![A screenshot showing selecting a data source rule, and clicking the add rule option.](media/deployment-pipelines-get-started/add-rule.png)](media/deployment-pipelines-get-started/add-rule.png#lightbox)</span></span>

### <a name="dataset-rule-types"></a><span data-ttu-id="49679-191">ชนิดกฎชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49679-191">Dataset rule types</span></span>

<span data-ttu-id="49679-192">มีกฎสองชนิดที่คุณสามารถสร้างได้:</span><span class="sxs-lookup"><span data-stu-id="49679-192">There are two types of rules you can create:</span></span>

* <span data-ttu-id="49679-193">**กฎแหล่งข้อมูล** รายการแหล่งข้อมูลจะถูกนำมาจากชุดข้อมูลของขั้นตอนไปป์ไลน์ต้นทาง</span><span class="sxs-lookup"><span data-stu-id="49679-193">**Data source rules** The data source list is taken from the dataset of the source pipeline stage.</span></span> <span data-ttu-id="49679-194">จากรายการแหล่งข้อมูล เลือกแหล่งข้อมูลที่จะแทนที่</span><span class="sxs-lookup"><span data-stu-id="49679-194">From the data source list, select a data source to be replaced.</span></span> <span data-ttu-id="49679-195">ใช้หนึ่งในวิธีต่อไปนี้เพื่อเลือกค่าที่จะแทนที่อีกค่าจากขั้นตอนต้นทาง:</span><span class="sxs-lookup"><span data-stu-id="49679-195">Use one of the following methods to select a value to replace the one from the source stage:</span></span>

    1. <span data-ttu-id="49679-196">เลือกจากรายการ</span><span class="sxs-lookup"><span data-stu-id="49679-196">Select from a list.</span></span>

    2. <span data-ttu-id="49679-197">เลือก **อื่น ๆ** และเพิ่มแหล่งข้อมูลใหม่ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="49679-197">Select **Other** and manually add the new data source.</span></span> <span data-ttu-id="49679-198">คุณสามารถเปลี่ยนไปยังแหล่งข้อมูลจากชนิดเดียวกันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="49679-198">You can only change to a data source from the same type.</span></span>

* <span data-ttu-id="49679-199">**กฎพารามิเตอร์** เลือกพารามิเตอร์จากรายการพารามิเตอร์ ค่าปัจจุบันจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="49679-199">**Parameter rules** Select a parameter from the list of parameters; the current value is shown.</span></span> <span data-ttu-id="49679-200">แก้ไขค่าเป็นค่าที่คุณต้องการให้มีผลหลังจากการปรับใช้แต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="49679-200">Edit the value to the value you want to take effect after each deployment.</span></span>

### <a name="dataset-rule-limitations"></a><span data-ttu-id="49679-201">ข้อจำกัดของกฎชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49679-201">Dataset rule limitations</span></span>

* <span data-ttu-id="49679-202">คุณต้องเป็นเจ้าของชุดข้อมูลเพื่อสร้างกฎชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49679-202">You must be the dataset owner to create a dataset rule.</span></span>

* <span data-ttu-id="49679-203">ไม่สามารถสร้างกฎชุดข้อมูลในขั้นตอนการพัฒนาได้</span><span class="sxs-lookup"><span data-stu-id="49679-203">Dataset rules cannot be created in the development stage.</span></span>

* <span data-ttu-id="49679-204">เมื่อรายการถูกเอาออกหรือลบกฎจะถูกลบด้วย</span><span class="sxs-lookup"><span data-stu-id="49679-204">When an item is removed or deleted, its rules are deleted too.</span></span> <span data-ttu-id="49679-205">ไม่สามารถคืนค่ากฎเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="49679-205">These rules cannot be restored.</span></span>

* <span data-ttu-id="49679-206">หากแหล่งข้อมูลหรือพารามิเตอร์ที่กำหนดไว้ในกฎมีการเปลี่ยนแปลงหรือลบออกจากชุดข้อมูลต้นทาง กฎจะไม่ถูกต้องและการปรับใช้จะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="49679-206">If the data source or parameters defined in a rule are changed or removed from the source dataset, the rule will not be valid and the deployment will fail.</span></span>

* <span data-ttu-id="49679-207">ไม่สามารถกำหนดกฎพารามิเตอร์สำหรับพารามิเตอร์ที่มีชนิดเป็น *ทุกชนิด* หรือ *ไบนารี*</span><span class="sxs-lookup"><span data-stu-id="49679-207">Parameter rules cannot be defined for parameters that are of type *Any* or *Binary*.</span></span> <span data-ttu-id="49679-208">สำหรับข้อมูลเพิ่มเติม โปรดดู [ข้อจำกัดของพารามิเตอร์การปรับปรุงชุดข้อมูล](/rest/api/power-bi/datasets/updateparameters)</span><span class="sxs-lookup"><span data-stu-id="49679-208">For more information, see [datasets update parameters restrictions](/rest/api/power-bi/datasets/updateparameters).</span></span>

* <span data-ttu-id="49679-209">กฎแหล่งข้อมูลสามารถกำหนดได้สำหรับแหล่งข้อมูลต่อไปนี้เท่านั้น:</span><span class="sxs-lookup"><span data-stu-id="49679-209">Data source rules can only be defined for the following data sources:</span></span>
    * <span data-ttu-id="49679-210">Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="49679-210">Azure Analysis Services</span></span>
    * <span data-ttu-id="49679-211">Azure Synapse</span><span class="sxs-lookup"><span data-stu-id="49679-211">Azure Synapse</span></span>
    * <span data-ttu-id="49679-212">SQL Server Analysis Services (SSAS)</span><span class="sxs-lookup"><span data-stu-id="49679-212">SQL Server Analysis Services (SSAS)</span></span>
    * <span data-ttu-id="49679-213">Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="49679-213">Azure SQL Server</span></span>
    * <span data-ttu-id="49679-214">SQL server</span><span class="sxs-lookup"><span data-stu-id="49679-214">SQL server</span></span>
    * <span data-ttu-id="49679-215">Odata Feed</span><span class="sxs-lookup"><span data-stu-id="49679-215">Odata Feed</span></span>
    * <span data-ttu-id="49679-216">Oracle</span><span class="sxs-lookup"><span data-stu-id="49679-216">Oracle</span></span>
    * <span data-ttu-id="49679-217">SapHana (รองรับเฉพาะโหมดการนำเข้า ไม่ใช่โหมดคิวรีโดยตรง)</span><span class="sxs-lookup"><span data-stu-id="49679-217">SapHana (only supported for import mode; not direct query mode)</span></span>
    * <span data-ttu-id="49679-218">SharePoint</span><span class="sxs-lookup"><span data-stu-id="49679-218">SharePoint</span></span>
    * <span data-ttu-id="49679-219">Teradata</span><span class="sxs-lookup"><span data-stu-id="49679-219">Teradata</span></span>

    <span data-ttu-id="49679-220">สำหรับแหล่งข้อมูลอื่นเราขอแนะนำให้ [ ใช้พารามิเตอร์เพื่อกำหนดค่าแหล่งข้อมูลของคุณ](deployment-pipelines-best-practices.md#use-parameters-in-your-model)</span><span class="sxs-lookup"><span data-stu-id="49679-220">For other data sources, we recommend [using parameters to configure your data source](deployment-pipelines-best-practices.md#use-parameters-in-your-model).</span></span>

## <a name="step-5---deploy-content-from-one-stage-to-another"></a><span data-ttu-id="49679-221">ขั้นตอนที่ 5 - ปรับใช้เนื้อหาจากขั้นตอนหนึ่งไปยังอีกขั้น</span><span class="sxs-lookup"><span data-stu-id="49679-221">Step 5 - Deploy content from one stage to another</span></span>

<span data-ttu-id="49679-222">เมื่อคุณมีเนื้อหาในขั้นตอนไปป์ไลน์แล้วคุณสามารถปรับใช้กับขั้นตอนถัดไปได้</span><span class="sxs-lookup"><span data-stu-id="49679-222">Once you have content in a pipeline stage, you can deploy it to the next stage.</span></span> <span data-ttu-id="49679-223">การปรับใช้เนื้อหาไปยังขั้นตอนอื่นมักจะทำหลังจากคุณได้ดำเนินการบางอย่างในไปป์ไลน์</span><span class="sxs-lookup"><span data-stu-id="49679-223">Deploying content to another stage is usually done after you've performed some actions in the pipeline.</span></span> <span data-ttu-id="49679-224">ตัวอย่างเช่น ทำการเปลี่ยนแปลงการพัฒนาเนื้อหาของคุณในขั้นตอนการพัฒนา หรือทดสอบเนื้อหาของคุณในขั้นตอนการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="49679-224">For example, made development changes to your content in the development stage, or tested your content in the test stage.</span></span> <span data-ttu-id="49679-225">เวิร์กโฟลว์ทั่วไปสำหรับการย้ายเนื้อหาจากขั้นตอนหนึ่งไปอีกขั้นคือการพัฒนาเพื่อทดสอบแล้วทดสอบกับการผลิต</span><span class="sxs-lookup"><span data-stu-id="49679-225">A typical workflow for moving content from stage to stage, is development to test, and then test to production.</span></span> <span data-ttu-id="49679-226">คุณสามารถเรียนรู้เพิ่มเติมเกี่ยวกับกระบวนการนี้ได้ในส่วน [ ปรับใช้เนื้อหาไปยังพื้นที่ทำงานที่มีอยู่](deployment-pipelines-process.md#deploy-content-to-an-existing-workspace)</span><span class="sxs-lookup"><span data-stu-id="49679-226">You can learn more about this process, in the [deploy content to an existing workspace](deployment-pipelines-process.md#deploy-content-to-an-existing-workspace) section.</span></span>

<span data-ttu-id="49679-227">ในการปรับใช้เนื้อหาไปยังขั้นตอนถัดไปในไปป์ไลน์การปรับใช้ ให้เลือกปุ่มปรับใช้ที่ด้านล่างของขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="49679-227">To deploy content to the next stage in the deployment pipeline, select the deploy button at the bottom of the stage.</span></span>

<span data-ttu-id="49679-228">เมื่อตรวจสอบการ์ดขั้นตอนทดสอบและการผลิต คุณสามารถดูเวลาการปรับใช้ล่าสุด</span><span class="sxs-lookup"><span data-stu-id="49679-228">When reviewing the test and production stage cards, you can see the last deployment time.</span></span> <span data-ttu-id="49679-229">ซึ่งแสดงเนื้อหาครั้งล่าสุดที่ถูกปรับใช้กับขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="49679-229">This indicates the last time content was deployed to the stage.</span></span>

<span data-ttu-id="49679-230">เวลาการปรับใช้จะเป็นประโยชน์สำหรับการสร้างเมื่อขั้นตอนได้รับการอัปเดตครั้งล่าสุด</span><span class="sxs-lookup"><span data-stu-id="49679-230">Deployment time is useful for establishing when a stage was last updated.</span></span> <span data-ttu-id="49679-231">นอกจากนี้ยังสามารถเป็นประโยชน์ถ้าคุณต้องการติดตามเวลาระหว่างการทดสอบและการปรับใช้การผลิต</span><span class="sxs-lookup"><span data-stu-id="49679-231">It can also be helpful if you want to track time between test and production deployments.</span></span>

## <a name="comparing-stages"></a><span data-ttu-id="49679-232">การเปรียบเทียบขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="49679-232">Comparing stages</span></span>

<span data-ttu-id="49679-233">เมื่อสองลำดับขั้นตอนมีเนื้อหา เนื้อหาจะถูกเปรียบเทียบโดยยึดตามเมตาดาต้าของรายการเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="49679-233">When two sequential stages have content, the content is compared based on the content items metadata.</span></span> <span data-ttu-id="49679-234">การเปรียบเทียบนี้ไม่รวมการเปรียบเทียบข้อมูลหรือเวลาการรีเฟรชระหว่างขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="49679-234">This comparison doesn't include comparing data or refresh time between stages.</span></span>

 <span data-ttu-id="49679-235">[![สกรีนช็อตที่แสดงไปป์ไลน์การปรับใช้งานที่มีตัวบ่งชี้การเปรียบเทียบ](media/deployment-pipelines-get-started/deployment-flow.png)](media/deployment-pipelines-get-started/deployment-flow.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="49679-235">[![A screenshot showing a deployment pipeline with its comparison indicators.](media/deployment-pipelines-get-started/deployment-flow.png)](media/deployment-pipelines-get-started/deployment-flow.png#lightbox)</span></span>

<span data-ttu-id="49679-236">เพื่อให้สามารถแสดงข้อมูลเชิงลึกของวิชวลได้อย่างรวดเร็วในความแตกต่างระหว่างสองลำดับขั้นตอน ตัวบ่งชี้ไอคอนเปรียบเทียบจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="49679-236">To allow a quick visual insight into the differences between two sequential stages, a comparison icon indicator appears between them.</span></span> <span data-ttu-id="49679-237">ตัวบ่งชี้การเปรียบเทียบมีสองสถานะ:</span><span class="sxs-lookup"><span data-stu-id="49679-237">The comparison indicator has two states:</span></span>

* <span data-ttu-id="49679-238">**ตัวบ่งชี้สีเขียว** – เมตาดาต้าสำหรับแต่ละรายการเนื้อหาในทั้งสองขั้นตอนจะเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="49679-238">**Green indicator** – The metadata for each content item in both stages, is the same.</span></span>

* <span data-ttu-id="49679-239">**ตัวบ่งชี้สีส้ม** - ปรากฏขึ้นหากเป็นไปตามเงื่อนไขหนึ่งในเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="49679-239">**Orange indicator** - Appears if one of these conditions is met:</span></span>
    * <span data-ttu-id="49679-240">บางรายการเนื้อหาในแต่ละขั้นตอนมีการเปลี่ยนแปลงหรืออัปเดต (มีเมตาดาต้าที่แตกต่างกัน)</span><span class="sxs-lookup"><span data-stu-id="49679-240">Some of the content items in each stage, were changed or updated (have different metadata).</span></span>
    * <span data-ttu-id="49679-241">มีความแตกต่างในจำนวนของรายการระหว่างขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="49679-241">There is a difference in the number of items between the stages.</span></span>

<span data-ttu-id="49679-242">เมื่อสองลำดับขั้นตอนไม่เหมือนกัน ลิงก์ **เปรียบเทียบ** จะปรากฏขึ้นใต้ไอคอนการเปรียบเทียบสีส้ม</span><span class="sxs-lookup"><span data-stu-id="49679-242">When two sequential stages aren't the same, a **compare** link appears underneath the orange comparison icon.</span></span> <span data-ttu-id="49679-243">การคลิกที่ลิงก์จะเปิดรายการเนื้อหาในทั้งสองขั้นตอนในมุมมองการเปรียบเทียบ</span><span class="sxs-lookup"><span data-stu-id="49679-243">Clicking the link opens the content item list in both stages in Compare view.</span></span> <span data-ttu-id="49679-244">มุมมองการเปรียบเทียบช่วยให้คุณติดตามการเปลี่ยนแปลงหรือความแตกต่างระหว่างรายการในแต่ละขั้นตอนไปป์ไลน์</span><span class="sxs-lookup"><span data-stu-id="49679-244">Compare view helps you track changes or differences between items, in each pipeline stage.</span></span> <span data-ttu-id="49679-245">รายการที่เปลี่ยนแปลงจะได้รับหนึ่งในป้ายกำกับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="49679-245">Changed items get one of the following labels:</span></span>

* <span data-ttu-id="49679-246">**ใหม่** - รายการใหม่ในขั้นตอนต้นทาง</span><span class="sxs-lookup"><span data-stu-id="49679-246">**New** – A new item in the source stage.</span></span> <span data-ttu-id="49679-247">นี่คือรายการที่ไม่มีในขั้นตอนเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="49679-247">This is an item that doesn't exist in the target stage.</span></span> <span data-ttu-id="49679-248">หลังจากการปรับใช้ รายการนี้จะถูกลอกแบบไปยังขั้นตอนเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="49679-248">After deployment, this item will be cloned to the target stage.</span></span>

* <span data-ttu-id="49679-249">**ที่แตกต่างกัน** – รายการที่มีอยู่ทั้งในแหล่งที่มาและขั้นตอนเป้าหมาย เป็นหนึ่งในเวอร์ชันที่มีการเปลี่ยนแปลงหลังจากการปรับใช้ครั้งล่าสุด</span><span class="sxs-lookup"><span data-stu-id="49679-249">**Different** – An item that exists both in the source and the target stage, were one of the versions was changed after the last deployment.</span></span> <span data-ttu-id="49679-250">หลังจากการปรับใช้ รายการในขั้นตอนต้นทางจะเขียนทับรายการในขั้นตอนเป้าหมายโดยไม่คำนึงถึงตำแหน่งที่ทำการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="49679-250">After deployment, the item in the source stage will overwrite the item in the target stage, regardless of where the change was made.</span></span>

* <span data-ttu-id="49679-251">**หายไปจาก** – ป้ายชื่อนี้แสดงว่ารายการปรากฏในขั้นตอนเป้าหมายแต่ไม่อยู่ในขั้นตอนต้นทาง</span><span class="sxs-lookup"><span data-stu-id="49679-251">**Missing from** – This label indicates that an item appears in the target stage, but not in the source stage.</span></span>

    >[!NOTE]
    ><span data-ttu-id="49679-252">การใช้งานจะไม่ส่งผลกระทบรายการ *หายไปจาก*</span><span class="sxs-lookup"><span data-stu-id="49679-252">Deployment will not impact *missing from* items.</span></span>

 <span data-ttu-id="49679-253">[![สกรีนช็อตที่แสดงตัวเลือกการเปรียบเทียบซึ่งขยายมุมมองการเปรียบเทียบและอนุญาตให้มีการเปรียบเทียบรายการระหว่างขั้นตอนไปป์ไลน์การปรับใช้งาน](media/deployment-pipelines-get-started/compare.png)](media/deployment-pipelines-get-started/compare.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="49679-253">[![A screenshot showing the compare option which expands the compare view and allows comparing items between deployment pipeline stages.](media/deployment-pipelines-get-started/compare.png)](media/deployment-pipelines-get-started/compare.png#lightbox)</span></span>

## <a name="overriding-content"></a><span data-ttu-id="49679-254">การแทนที่เนื้อหา</span><span class="sxs-lookup"><span data-stu-id="49679-254">Overriding content</span></span>

<span data-ttu-id="49679-255">เมื่อคุณปรับใช้หลังจากทำการเปลี่ยนแปลงเนื้อหาในขั้นตอนต้นทาง เนื้อหาที่คุณเปลี่ยนในขั้นตอนเป้าหมายจะถูกเขียนทับ</span><span class="sxs-lookup"><span data-stu-id="49679-255">When you deploy after making changes to content in the source stage, the content you changed in the target stage is overwritten.</span></span> <span data-ttu-id="49679-256">หลังจากที่คลิก *ปรับใช้* แล้วคุณจะได้รับคำเตือนเป็นรายการจำนวนของรายการที่จะถูกเขียนทับ</span><span class="sxs-lookup"><span data-stu-id="49679-256">After clicking *deploy*, you'll get a warning listing the number of items that will be overwritten.</span></span>

![สกรีนช็อตของคำเตือนเนื้อหาที่ถูกแทนที่ซึ่งจะแสดงขึ้นเมื่อการปรับใช้เป็นสาเหตุทำให้เกิดการเปลี่ยนแปลงไปยังรายการในขั้นตอนที่คุณใช้งานอยู่](media/deployment-pipelines-get-started/replaced-content.png)

<span data-ttu-id="49679-258">คุณสามารถเรียนรู้เพิ่มเติมเกี่ยวกับ [รายการที่จะถูกคัดลอกไปยังขั้นตอนถัดไป](deployment-pipelines-process.md#deployed-items)และ [รายการที่ไม่ถูกคัดลอก](deployment-pipelines-process.md#unsupported-items)ใน [ทำความเข้าใจกระบวนการปรับใช้](deployment-pipelines-process.md)</span><span class="sxs-lookup"><span data-stu-id="49679-258">You can learn more about [which items are copied to the next stage](deployment-pipelines-process.md#deployed-items), and [which items are not copied](deployment-pipelines-process.md#unsupported-items), in [Understand the deployment process](deployment-pipelines-process.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="49679-259">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="49679-259">Next steps</span></span>

>[!div class="nextstepaction"]
>[<span data-ttu-id="49679-260">บทนำสู่ไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="49679-260">Introduction to deployment pipelines</span></span>](deployment-pipelines-overview.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="49679-261">ทำความเข้าใจกระบวนการไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="49679-261">Understand the deployment pipelines process</span></span>](deployment-pipelines-process.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="49679-262">การแก้ไขปัญหาไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="49679-262">Deployment pipelines troubleshooting</span></span>](deployment-pipelines-troubleshooting.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="49679-263">แนวทางปฏิบัติที่ดีที่สุดสำหรับไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="49679-263">Deployment pipelines best practices</span></span>](deployment-pipelines-best-practices.md)