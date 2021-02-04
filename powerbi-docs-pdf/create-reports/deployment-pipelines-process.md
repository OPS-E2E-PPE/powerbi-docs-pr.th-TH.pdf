---
title: กระบวนการไปป์ไลน์การปรับใช้
description: ทำความเข้าใจกระบวนการไปป์ไลน์การปรับใช้ Power BI
author: KesemSharabi
ms.author: kesharab
ms.topic: conceptual
ms.service: powerbi
ms.subservice: pbi-deployment
ms.custom: contperf-fy21q1
ms.date: 12/28/2020
ms.openlocfilehash: 4bb709e41698bc0dc32341f517593717f64f9b6d
ms.sourcegitcommit: a465a0c80ffc0f24ba6b8331f88420a0d21ac0b2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/29/2020
ms.locfileid: "97805222"
---
# <a name="understand-the-deployment-process"></a><span data-ttu-id="f3675-103">ทำความเข้าใจขั้นตอนการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f3675-103">Understand the deployment process</span></span>

<span data-ttu-id="f3675-104">กระบวนการปรับใช้ช่วยให้คุณสามารถโคลนเนื้อหาจากขั้นตอนหนึ่งในไปป์ไลน์ไปยังอีกขั้นหนึ่ง จากการพัฒนาโดยทั่วไปจนถึงการทดสอบและจากการทดสอบไปยังการผลิต</span><span class="sxs-lookup"><span data-stu-id="f3675-104">The deployment process lets you clone content from one stage in the pipeline to another, typically from development to test, and from test to production.</span></span>

<span data-ttu-id="f3675-105">ในระหว่างการปรับใช้ Power BI จะคัดลอกเนื้อหาจากขั้นตอนปัจจุบันไปยังเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="f3675-105">During deployment, Power BI copies the content from the current stage, into the target one.</span></span> <span data-ttu-id="f3675-106">การเชื่อมต่อระหว่างรายการที่คัดลอกจะถูกเก็บไว้ในระหว่างกระบวนการคัดลอก</span><span class="sxs-lookup"><span data-stu-id="f3675-106">The connections between the copied items are kept during the copy process.</span></span> <span data-ttu-id="f3675-107">Power BI ยังใช้กฎชุดข้อมูลที่กำหนดค่าไว้กับเนื้อหาที่อัปเดตแล้วในขั้นตอนเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="f3675-107">Power BI also applies the configured dataset rules to the updated content in the target stage.</span></span> <span data-ttu-id="f3675-108">การจัดวางเนื้อหาอาจใช้เวลาสักครู่โดยขึ้นอยู่กับจำนวนของรายการที่ถูกปรับใช้</span><span class="sxs-lookup"><span data-stu-id="f3675-108">Deploying content may take a while, depending on the number of items being deployed.</span></span> <span data-ttu-id="f3675-109">ในช่วงเวลานี้คุณสามารถนำทางไปยังหน้าอื่นๆ ในพอร์ทัล Power BI แต่คุณไม่สามารถใช้เนื้อหาในขั้นตอนเป้าหมายได้</span><span class="sxs-lookup"><span data-stu-id="f3675-109">During this time, you can navigate to other pages in the Power BI portal, but you cannot use the content in the target stage.</span></span>

## <a name="deploying-content-to-an-empty-stage"></a><span data-ttu-id="f3675-110">ปรับใช้เนื้อหาไปยังขั้นตอนที่ว่าง</span><span class="sxs-lookup"><span data-stu-id="f3675-110">Deploying content to an empty stage</span></span>

<span data-ttu-id="f3675-111">เมื่อคุณปรับใช้เนื้อหาไปยังขั้นตอนที่ว่าง เมตาดาต้าของรายงาน แดชบอร์ด และชุดข้อมูลในพื้นที่ทำงานที่คุณกำลังจัดวางจะถูกคัดลอกไปยังขั้นตอนที่คุณกำลังปรับใช้</span><span class="sxs-lookup"><span data-stu-id="f3675-111">When you deploy content to an empty stage, the metadata of the reports, dashboards, and datasets in the workspace you're deploying from, is copied to the stage you're deploying to.</span></span> <span data-ttu-id="f3675-112">พื้นที่ทำงานใหม่สำหรับขั้นตอนที่คุณปรับใช้จะถูกสร้างขึ้นบนความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="f3675-112">A new workspace for the stage you deployed to, is created on a Premium capacity.</span></span>

<span data-ttu-id="f3675-113">มีสองวิธีในการปรับใช้เนื้อหาจากหนึ่งขั้นตอนไปยังรายการถัดไป</span><span class="sxs-lookup"><span data-stu-id="f3675-113">There are two ways to deploy content from one stage to the next one.</span></span> <span data-ttu-id="f3675-114">คุณสามารถปรับใช้เนื้อหาทั้งหมดหรือคุณสามารถ [เลือกรายการเนื้อหาที่จะปรับใช้ได้](deployment-pipelines-get-started.md#selective-deployment)</span><span class="sxs-lookup"><span data-stu-id="f3675-114">You can deploy all the content, or you can [select which content items to deploy](deployment-pipelines-get-started.md#selective-deployment).</span></span>

<span data-ttu-id="f3675-115">นอกจากนี้คุณยังสามารถปรับใช้เนื้อหาย้อนหลังจากขั้นตอนถัดไปในไปป์ไลน์การปรับใช้ไปยังรายการก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="f3675-115">You can also deploy content backwards, from a later stage in the deployment pipeline, to an earlier one.</span></span>

<span data-ttu-id="f3675-116">หลังจากที่การปรับใช้เสร็จสมบูรณ์ให้รีเฟรชชุดข้อมูลเพื่อให้คุณสามารถใช้เนื้อหาที่คัดลอกใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="f3675-116">After the deployment is complete, refresh the datasets so that you can use the newly copied content.</span></span> <span data-ttu-id="f3675-117">จำเป็นต้องมีการรีเฟรชชุดข้อมูลเนื่องจากไม่มีการคัดลอกข้อมูลจากขั้นตอนหนึ่งไปยังรายการอื่น</span><span class="sxs-lookup"><span data-stu-id="f3675-117">The dataset refresh is required because data isn't copied from one stage to another.</span></span> <span data-ttu-id="f3675-118">เมื่อต้องการทำความเข้าใจเกี่ยวกับคุณสมบัติของรายการที่จะคัดลอกในระหว่างกระบวนการปรับใช้และคุณสมบัติของรายการที่ไม่ได้คัดลอกให้ตรวจทาน [คุณสมบัติของรายการที่คัดลอกในระหว่างส่วนปรับใช้](#item-properties-copied-during-deployment)</span><span class="sxs-lookup"><span data-stu-id="f3675-118">To understand which item properties are copied during the deployment process, and which item properties are not copied, review the [item properties copied during deployment](#item-properties-copied-during-deployment) section.</span></span>

### <a name="creating-a-premium-capacity-workspace"></a><span data-ttu-id="f3675-119">การสร้างพื้นที่ทำงานความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="f3675-119">Creating a Premium capacity workspace</span></span>

<span data-ttu-id="f3675-120">ในระหว่างการปรับใช้ครั้งแรก ไปป์ไลน์การปรับใช้จะตรวจสอบว่าคุณมีสิทธิ์ความจุแบบพรีเมียมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f3675-120">During first-time deployment, deployment pipelines checks if you have Premium capacity permissions.</span></span>  

<span data-ttu-id="f3675-121">ถ้าคุณมีสิทธิ์ความจุ เนื้อหาของพื้นที่ทำงานจะถูกคัดลอกไปยังขั้นตอนที่คุณกำลังปรับใช้ และพื้นที่ทำงานใหม่สำหรับขั้นตอนดังกล่าวจะถูกสร้างขึ้นบนความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="f3675-121">If you have capacity permissions, the content of the workspace is copied to the stage you're deploying to, and a new  workspace for that stage is created on the Premium capacity.</span></span>

<span data-ttu-id="f3675-122">ถ้าคุณไม่มีสิทธิ์ความจุ พื้นที่ทำงานจะถูกสร้างขึ้นแต่ไม่มีการคัดลอกเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="f3675-122">If you don't have capacity permissions, the workspace is created but the content isn’t copied.</span></span> <span data-ttu-id="f3675-123">คุณสามารถขอให้ผู้ดูแลความจุเพิ่มพื้นที่ทำงานของคุณไปยังความจุ หรือขอสิทธิ์ในการกำหนดสำหรับความจุ</span><span class="sxs-lookup"><span data-stu-id="f3675-123">You can ask a capacity admin to add your workspace to a capacity, or ask for assignment permissions for the capacity.</span></span> <span data-ttu-id="f3675-124">หลังจากที่พื้นที่ทำงานถูกกำหนดให้กับความจุ คุณสามารถปรับใช้เนื้อหาไปยังพื้นที่ทำงานนี้ได้</span><span class="sxs-lookup"><span data-stu-id="f3675-124">Later, when the workspace is assigned to a capacity, you can deploy content to this workspace.</span></span>

<span data-ttu-id="f3675-125">หากคุณกำลังใช้ [Premium Per User (PPU)](../admin/service-premium-per-user-faq.md) พื้นที่ทำงานของคุณจะถูกสร้างขึ้นโดยอัตโนมัติตามความจุที่เชื่อมโยงกับ PPU ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f3675-125">If you're using [Premium Per User (PPU)](../admin/service-premium-per-user-faq.md), your workspace is automatically created in the capacity associated with your PPU.</span></span> <span data-ttu-id="f3675-126">ในกรณีดังกล่าวไม่จำเป็นต้องมีสิทธิ์ความจุ</span><span class="sxs-lookup"><span data-stu-id="f3675-126">In such cases capacity permissions are not required.</span></span> <span data-ttu-id="f3675-127">อย่างไรก็ตาม พื้นที่ทำงานที่สร้างขึ้นจากผู้ใช้ PPU สามารถเข้าถึงได้โดยผู้ใช้ PPU รายอื่นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f3675-127">However, workspaces created by a PPU user, can only be accessed by other PPU users.</span></span> <span data-ttu-id="f3675-128">นอกจากนี้เนื้อหาที่สร้างในพื้นที่ทำงานดังกล่าวสามารถใช้ได้โดยผู้ใช้ PPU เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f3675-128">In addition, content created in such workspaces can only be consumed by PPU users.</span></span>

### <a name="workspace-and-content-ownership"></a><span data-ttu-id="f3675-129">พื้นที่ทำงานและความเป็นเจ้าของเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="f3675-129">Workspace and content ownership</span></span>

<span data-ttu-id="f3675-130">ผู้ใช้จะกลายเป็นเจ้าของชุดข้อมูลแบบโคลนโดยอัตโนมัติและผู้ดูแลระบบเดียวของพื้นที่ทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="f3675-130">The deploying user automatically becomes the dataset owner of the cloned datasets, and the only admin of the new workspace.</span></span>

## <a name="deploy-content-to-an-existing-workspace"></a><span data-ttu-id="f3675-131">ปรับใช้เนื้อหาไปยังพื้นที่ทำงานที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="f3675-131">Deploy content to an existing workspace</span></span>

<span data-ttu-id="f3675-132">การปรับใช้เนื้อหาในไปป์ไลน์การผลิตที่ใช้งานได้ไปยังขั้นตอนที่มีพื้นที่ทำงานที่มีอยู่รวมถึงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f3675-132">Deploying content in a working production pipeline, to a stage that has an existing workspace, includes the following:</span></span>

* <span data-ttu-id="f3675-133">ปรับใช้เนื้อหาใหม่ด้วยการเพิ่มไปยังขั้นตอนที่มีเนื้อหาอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="f3675-133">Deploying new content as an addition, to a stage that already contains content.</span></span>

* <span data-ttu-id="f3675-134">เนื้อหาใหม่ที่ปรับใช้เพื่อแทนที่เนื้อหาเก่าในขั้นตอนการทำงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="f3675-134">New content deployed to replace old content, in a current working  stage.</span></span>

### <a name="deployment-process"></a><span data-ttu-id="f3675-135">กระบวนการปรับใช้</span><span class="sxs-lookup"><span data-stu-id="f3675-135">Deployment process</span></span>

<span data-ttu-id="f3675-136">เนื้อหาจากขั้นตอนปัจจุบันจะถูกคัดลอกไปยังขั้นตอนเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="f3675-136">Content from the current stage is copied over to the target stage.</span></span> <span data-ttu-id="f3675-137">Power BI ระบุเนื้อหาที่มีอยู่ในขั้นตอนเป้าหมายและเขียนทับข้อมูลดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="f3675-137">Power BI identifies existing content in the target stage and overwrites it.</span></span> <span data-ttu-id="f3675-138">ในการระบุว่ารายการเนื้อหาใดที่ต้องถูกเขียนทับไปป์ไลน์การปรับใช้จะใช้การเชื่อมต่อระหว่างรายการหลักกับโคลนของมัน</span><span class="sxs-lookup"><span data-stu-id="f3675-138">To identify which content item needs to be overwritten, deployment pipelines uses the connection between the parent item and its clones.</span></span> <span data-ttu-id="f3675-139">การเชื่อมต่อนี้จะถูกเก็บไว้เมื่อมีการสร้างเนื้อหาใหม่</span><span class="sxs-lookup"><span data-stu-id="f3675-139">This connection is kept when new content is created.</span></span> <span data-ttu-id="f3675-140">การดำเนินการเขียนทับจะเขียนทับเนื้อหาของรายการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f3675-140">The overwrite operation only overwrites the content of the item.</span></span> <span data-ttu-id="f3675-141">ID, URL และสิทธิ์ของรายการยังคงไม่เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="f3675-141">The item's ID, URL, and permissions remain unchanged.</span></span>

<span data-ttu-id="f3675-142">ในขั้นตอนเป้าหมาย [คุณสมบัติของรายการที่ไม่ได้คัดลอก](deployment-pipelines-process.md#item-properties-that-are-not-copied)ยังคงอยู่เหมือนก่อนการปรับใช้</span><span class="sxs-lookup"><span data-stu-id="f3675-142">In the target stage, [item properties that are not copied](deployment-pipelines-process.md#item-properties-that-are-not-copied), remain as they were before deployment.</span></span> <span data-ttu-id="f3675-143">เนื้อหาใหม่และรายการใหม่จะถูกคัดลอกจากขั้นตอนปัจจุบันไปยังขั้นตอนเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="f3675-143">New content and new items are copied from the current stage to the target stage.</span></span>

### <a name="refreshing-the-dataset"></a><span data-ttu-id="f3675-144">รีเฟรชชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f3675-144">Refreshing the dataset</span></span>

<span data-ttu-id="f3675-145">ข้อมูลในชุดข้อมูลเป้าหมายจะถูกเก็บไว้เมื่อเป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="f3675-145">Data in the target dataset is kept when possible.</span></span> <span data-ttu-id="f3675-146">ถ้าไม่มีการเปลี่ยนแปลงไปยังชุดข้อมูล ข้อมูลจะถูกเก็บไว้เหมือนก่อนที่จะมีการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f3675-146">If there are no changes to a dataset, the data is kept as it was before the deployment.</span></span>

<span data-ttu-id="f3675-147">เมื่อมีการเปลี่ยนแปลงเล็กๆ เช่นการเพิ่มตารางหรือหน่วยวัด Power BI จะเก็บข้อมูลเดิมและการรีเฟรชถูกปรับให้เหมาะสมเพื่อรีเฟรชเฉพาะสิ่งที่จำเป็นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f3675-147">With small changes, such as adding a table or measures, Power BI keeps the original data, and the refresh is optimized to refresh only what's needed.</span></span> <span data-ttu-id="f3675-148">สำหรับการทำลาย schema ที่เปลี่ยนแปลงหรือการเปลี่ยนแปลงในการเชื่อมต่อแหล่งข้อมูลจำเป็นต้องรีเฟรชแบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="f3675-148">For breaking schema changes, or changes in the data source connection, a full refresh is required.</span></span>

### <a name="requirements-for-deploying-to-a-stage-with-an-existing-workspace"></a><span data-ttu-id="f3675-149">ข้อกำหนดสำหรับการปรับใช้กับขั้นตอนด้วยพื้นที่ทำงานที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="f3675-149">Requirements for deploying to a stage with an existing workspace</span></span>

<span data-ttu-id="f3675-150">ตราบใดที่เนื้อหาที่มีการปรับใช้อยู่บน [ความจุแบบพรีเมียม](../admin/service-premium-what-is.md) ผู้ใช้ที่เป็นไปตามเงื่อนไขต่อไปนี้สามารถปรับใช้กับขั้นตอนด้วยพื้นที่ทำงานที่มีอยู่:</span><span class="sxs-lookup"><span data-stu-id="f3675-150">As long as the deployed content resides on a [premium capacity](../admin/service-premium-what-is.md), a user that meets the following conditions, can deploy it to a stage with an existing workspace:</span></span>

* <span data-ttu-id="f3675-151">ผู้ใช้ที่มี[สิทธิการใช้งาน Pro](../admin/service-admin-purchasing-power-bi-pro.md) หรือ[ผู้ใช้ PPU](../admin/service-premium-per-user-faq.md) ซึ่งเป็นสมาชิกของพื้นที่ทำงานทั้งสองในขั้นตอนการปรับใช้แหล่งที่มาและเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="f3675-151">A user with a [Pro license](../admin/service-admin-purchasing-power-bi-pro.md) or a [PPU user](../admin/service-premium-per-user-faq.md), who's a member of both workspaces in the source and target deployment stages.</span></span>

* <span data-ttu-id="f3675-152">เจ้าของชุดข้อมูลทั้งหมดในพื้นที่ทำงานเป้าหมายที่จะถูกปรับใช้</span><span class="sxs-lookup"><span data-stu-id="f3675-152">An owner of all the datasets in the target workspace that are about to be deployed.</span></span>

<span data-ttu-id="f3675-153">สำหรับข้อมูลเพิ่มเติมให้ตรวจทานส่วน [สิทธิ์](#permissions)</span><span class="sxs-lookup"><span data-stu-id="f3675-153">For more information, review the [permissions](#permissions) section.</span></span>

## <a name="deployed-items"></a><span data-ttu-id="f3675-154">รายการที่ปรับใช้</span><span class="sxs-lookup"><span data-stu-id="f3675-154">Deployed items</span></span>

<span data-ttu-id="f3675-155">เมื่อคุณปรับใช้เนื้อหาจากขั้นตอนไปป์ไลน์หนึ่งไปยังอีกขั้นตอน เนื้อหาที่คัดลอกจะประกอบด้วยรายการ Power BI ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f3675-155">When you deploy content from one pipeline stage to another, the copied content contains the following Power BI items:</span></span>

* <span data-ttu-id="f3675-156">ชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f3675-156">Datasets</span></span>

* <span data-ttu-id="f3675-157">รายงาน</span><span class="sxs-lookup"><span data-stu-id="f3675-157">Reports</span></span>

* <span data-ttu-id="f3675-158">แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="f3675-158">Dashboards</span></span>

### <a name="unsupported-items"></a><span data-ttu-id="f3675-159">รายการที่ไม่รองรับ</span><span class="sxs-lookup"><span data-stu-id="f3675-159">Unsupported items</span></span>

<span data-ttu-id="f3675-160">ไปป์ไลน์การปรับใช้ไม่รองรับรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f3675-160">Deployment pipelines doesn't support the following items:</span></span>

* <span data-ttu-id="f3675-161">ชุดข้อมูลที่ไม่ได้มาจาก PBIX</span><span class="sxs-lookup"><span data-stu-id="f3675-161">Datasets that do not originate from a PBIX</span></span>

* <span data-ttu-id="f3675-162">รายงานที่ยึดตามชุดข้อมูลที่ไม่ได้รับการรองรับ</span><span class="sxs-lookup"><span data-stu-id="f3675-162">Reports based on unsupported datasets</span></span>

* [<span data-ttu-id="f3675-163">พื้นที่ทำงานของแอปเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="f3675-163">Template app workspaces</span></span>](../connect-data/service-template-apps-create.md#create-the-template-workspace)

* <span data-ttu-id="f3675-164">รายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="f3675-164">Paginated reports</span></span>

* <span data-ttu-id="f3675-165">กระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f3675-165">Dataflows</span></span>

* <span data-ttu-id="f3675-166">ส่งชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f3675-166">PUSH datasets</span></span>

* <span data-ttu-id="f3675-167">เวิร์กบุ๊ก</span><span class="sxs-lookup"><span data-stu-id="f3675-167">Workbooks</span></span>

## <a name="item-properties-copied-during-deployment"></a><span data-ttu-id="f3675-168">คุณสมบัติรายการที่คัดลอกในระหว่างการปรับใช้</span><span class="sxs-lookup"><span data-stu-id="f3675-168">Item properties copied during deployment</span></span>

<span data-ttu-id="f3675-169">ในระหว่างการปรับใช้คุณสมบัติของรายการต่อไปนี้จะถูกคัดลอกและเขียนทับคุณสมบัติของรายการที่ขั้นตอนเป้าหมาย:</span><span class="sxs-lookup"><span data-stu-id="f3675-169">During deployment, the following item properties are copied and overwrite the item properties at the target stage:</span></span>

* <span data-ttu-id="f3675-170">แหล่งข้อมูล ([กฎชุดข้อมูล](deployment-pipelines-get-started.md#step-4---create-dataset-rules) ได้รับการรองรับ)</span><span class="sxs-lookup"><span data-stu-id="f3675-170">Data sources ([dataset rules](deployment-pipelines-get-started.md#step-4---create-dataset-rules) are supported)</span></span>

* <span data-ttu-id="f3675-171">พารามิเตอร์ ([กฎชุดข้อมูล](deployment-pipelines-get-started.md#step-4---create-dataset-rules) ได้รับการรองรับ)</span><span class="sxs-lookup"><span data-stu-id="f3675-171">Parameters ([dataset rules](deployment-pipelines-get-started.md#step-4---create-dataset-rules) are supported)</span></span>

* <span data-ttu-id="f3675-172">ภาพวิชวลรายงาน</span><span class="sxs-lookup"><span data-stu-id="f3675-172">Report visuals</span></span>

* <span data-ttu-id="f3675-173">หน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="f3675-173">Report pages</span></span>

* <span data-ttu-id="f3675-174">ไทล์แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="f3675-174">Dashboard tiles</span></span>

* <span data-ttu-id="f3675-175">เมตาดาต้าแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="f3675-175">Model metadata</span></span>

* <span data-ttu-id="f3675-176">ความสัมพันธ์ของรายการ</span><span class="sxs-lookup"><span data-stu-id="f3675-176">Item relationships</span></span>

### <a name="item-properties-that-are-not-copied"></a><span data-ttu-id="f3675-177">คุณสมบัติรายการที่ไม่ได้คัดลอก</span><span class="sxs-lookup"><span data-stu-id="f3675-177">Item properties that are not copied</span></span>

<span data-ttu-id="f3675-178">ไม่มีการคัดลอกคุณสมบัติของรายการต่อไปนี้ในระหว่างการปรับใช้:</span><span class="sxs-lookup"><span data-stu-id="f3675-178">The following item properties are not copied during deployment:</span></span>

* <span data-ttu-id="f3675-179">ข้อมูล - ข้อมูลไม่ได้รับการคัดลอก เมตาดาต้าเท่านั้นที่จะถูกคัดลอก</span><span class="sxs-lookup"><span data-stu-id="f3675-179">Data - Data isn't being copied, only metadata is copied</span></span>

* <span data-ttu-id="f3675-180">URL</span><span class="sxs-lookup"><span data-stu-id="f3675-180">URL</span></span>

* <span data-ttu-id="f3675-181">ID</span><span class="sxs-lookup"><span data-stu-id="f3675-181">ID</span></span>

* <span data-ttu-id="f3675-182">สิทธิ์ - สำหรับพื้นที่ทำงานหรือรายการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f3675-182">Permissions - For a workspace or a specific item</span></span>

* <span data-ttu-id="f3675-183">การตั้งค่าพื้นที่ทำงาน - แต่ละขั้นตอนจะมีพื้นที่ทำงานของตัวเอง</span><span class="sxs-lookup"><span data-stu-id="f3675-183">Workspace settings - Each stage has its own workspace</span></span>

* <span data-ttu-id="f3675-184">เนื้อหาของแอปและการตั้งค่า - เพื่อปรับใช้งานแอปของคุณดู [ปรับใช้งานแอป Power BI](#deploying-power-bi-apps)</span><span class="sxs-lookup"><span data-stu-id="f3675-184">App content and settings - To deploy your apps, see [deploying Power BI apps](#deploying-power-bi-apps)</span></span>

<span data-ttu-id="f3675-185">ยังไม่มีการคัดลอกคุณสมบัติชุดข้อมูลต่อไปนี้ในระหว่างการปรับใช้:</span><span class="sxs-lookup"><span data-stu-id="f3675-185">The following dataset properties are also not copied during deployment:</span></span>

* <span data-ttu-id="f3675-186">การกำหนดบทบาท</span><span class="sxs-lookup"><span data-stu-id="f3675-186">Role assignment</span></span>

* <span data-ttu-id="f3675-187">กำหนดตารางเวลาการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="f3675-187">Refresh schedule</span></span>

* <span data-ttu-id="f3675-188">ข้อมูลประจำตัวของแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f3675-188">Data source credentials</span></span>

* <span data-ttu-id="f3675-189">การตั้งค่าการแคชของคิวรี (สามารถสืบทอดมาจากความจุ)</span><span class="sxs-lookup"><span data-stu-id="f3675-189">Query caching settings (can be inherited from the capacity)</span></span>

* <span data-ttu-id="f3675-190">การตั้งค่าการรับรอง</span><span class="sxs-lookup"><span data-stu-id="f3675-190">Endorsement settings</span></span>

## <a name="supported-dataset-features"></a><span data-ttu-id="f3675-191">ฟีเจอร์ชุดข้อมูลที่ได้รับการรองรับ</span><span class="sxs-lookup"><span data-stu-id="f3675-191">Supported dataset features</span></span>

<span data-ttu-id="f3675-192">ไปป์ไลน์การปรับใช้รองรับฟีเจอร์ชุดข้อมูล Power BI จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="f3675-192">Deployment pipelines supports many Power BI dataset features.</span></span> <span data-ttu-id="f3675-193">ส่วนนี้แสดงรายการฟีเจอร์ชุดข้อมูล Power BI สองรายการที่สามารถปรับปรุงการใช้งานไปป์ไลน์ของคุณได้ดังนี้:</span><span class="sxs-lookup"><span data-stu-id="f3675-193">This section lists two Power BI dataset features that can enhance your deployment pipelines experience:</span></span>

* [<span data-ttu-id="f3675-194">การรีเฟรชแบบเพิ่มหน่วย</span><span class="sxs-lookup"><span data-stu-id="f3675-194">Incremental refresh</span></span>](#incremental-refresh)

* [<span data-ttu-id="f3675-195">โมเดลแบบรวม</span><span class="sxs-lookup"><span data-stu-id="f3675-195">Composite models</span></span>](#composite-models)

### <a name="incremental-refresh"></a><span data-ttu-id="f3675-196">การรีเฟรชแบบเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f3675-196">Incremental refresh</span></span>

<span data-ttu-id="f3675-197">ไปป์ไลน์การปรับใช้สนับสนุน [การรีเฟรชแบบเพิ่มหน่วย](../admin/service-premium-incremental-refresh.md) ซึ่งเป็นคุณลักษณะที่ช่วยให้ชุดข้อมูลขนาดใหญ่มีการรีเฟรชที่รวดเร็วและน่าเชื่อถือมากขึ้น และใช้ทรัพยากรน้อยลง</span><span class="sxs-lookup"><span data-stu-id="f3675-197">Deployment pipelines supports [incremental refresh](../admin/service-premium-incremental-refresh.md), a feature that allows large datasets faster and more reliable refreshes, with lower consumption.</span></span>

<span data-ttu-id="f3675-198">ด้วยไปป์ไลน์การปรับใช้ คุณสามารถทำการอัปเดตชุดข้อมูลที่มีการรีเฟรชแบบเพิ่มหน่วยโดยที่ยังรักษาทั้งข้อมูลและพาร์ติชันเอาไว้</span><span class="sxs-lookup"><span data-stu-id="f3675-198">With deployment pipelines, you can make updates to a dataset with incremental refresh while retaining both data and partitions.</span></span> <span data-ttu-id="f3675-199">เมื่อคุณปรับใช้ชุดข้อมูล นโยบายจะถูกคัดลอกไปด้วย</span><span class="sxs-lookup"><span data-stu-id="f3675-199">When you deploy the dataset, the policy is copied along.</span></span>

#### <a name="activating-incremental-refresh-in-a-pipeline"></a><span data-ttu-id="f3675-200">การเปิดใช้งานการรีเฟรชแบบเพิ่มหน่วยในไปป์ไลน์</span><span class="sxs-lookup"><span data-stu-id="f3675-200">Activating incremental refresh in a pipeline</span></span>

<span data-ttu-id="f3675-201">หากต้องการเปิดใช้งานการรีเฟรชแบบเพิ่มหน่วย [เปิดใน Power BI Desktop](../admin/service-premium-incremental-refresh.md#configure-incremental-refresh) จากนั้นเผยแพร่ชุดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="f3675-201">To enable incremental refresh, [turn it on in Power BI Desktop](../admin/service-premium-incremental-refresh.md#configure-incremental-refresh), and then publish your dataset.</span></span> <span data-ttu-id="f3675-202">หลังจากที่คุณเผยแพร่ นโยบายการรีเฟรชแบบเพิ่มหน่วยจะคล้ายกันในทั้งไปป์ไลน์ และสามารถสร้างได้เฉพาะใน Power BI Desktop เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f3675-202">After you publish, the incremental refresh policy is similar across the pipeline, and can be authored only in Power BI Desktop.</span></span>

<span data-ttu-id="f3675-203">เมื่อมีการกำหนดค่าไปป์ไลน์ของคุณให้มีการรีเฟรชแบบเพิ่มหน่วย เราขอแนะนำให้คุณใช้โฟลว์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f3675-203">Once your pipeline is configured with incremental refresh, we recommend that you use the following flow:</span></span>

1. <span data-ttu-id="f3675-204">ทำการเปลี่ยนแปลงในไฟล์ PBIX ของคุณใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="f3675-204">Make changes to your PBIX file in Power BI Desktop.</span></span> <span data-ttu-id="f3675-205">เพื่อไม่ให้เสียเวลา คุณสามารถทำการเปลี่ยนแปลงโดยใช้ตัวอย่างของข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="f3675-205">To avoid long waiting times, you can make changes using a sample of your data.</span></span>

2. <span data-ttu-id="f3675-206">อัปโหลดไฟล์ PBIX ของคุณไปยังขั้นตอน *การพัฒนา*</span><span class="sxs-lookup"><span data-stu-id="f3675-206">Upload your PBIX file to the *development* stage.</span></span>

3. <span data-ttu-id="f3675-207">ปรับใช้เนื้อหาของคุณไปยังขั้นตอน *การทดสอบ*</span><span class="sxs-lookup"><span data-stu-id="f3675-207">Deploy your content to the *test* stage.</span></span> <span data-ttu-id="f3675-208">หลังจากการปรับใช้ การเปลี่ยนแปลงที่คุณทำจะมีผลกับชุดข้อมูลทั้งหมดที่คุณกำลังใช้อยู่</span><span class="sxs-lookup"><span data-stu-id="f3675-208">After deployment, the changes you made will apply to the entire dataset you're using.</span></span>

4. <span data-ttu-id="f3675-209">ตรวจทานการเปลี่ยนแปลงที่คุณทำไว้ในขั้นตอน *การทดสอบ* และหลังจากที่คุณตรวจสอบแล้ว ให้ปรับใช้กับขั้นตอน *การผลิต*</span><span class="sxs-lookup"><span data-stu-id="f3675-209">Review the changes you made in the *test* stage, and after you verify them, deploy to the *production* stage.</span></span>

#### <a name="usage-examples"></a><span data-ttu-id="f3675-210">ตัวอย่างการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f3675-210">Usage examples</span></span>

<span data-ttu-id="f3675-211">ด้านล่างนี้คือตัวอย่างบางส่วนของวิธีการที่คุณสามารถนำการรีเฟรชแบบเพิ่มหน่วยไปใช้ร่วมกับไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="f3675-211">Below are a few examples of how you may integrate incremental refresh with deployment pipelines.</span></span>

* <span data-ttu-id="f3675-212">[สร้างไปป์ไลน์ใหม่](deployment-pipelines-get-started.md#step-1---create-a-deployment-pipeline) และเชื่อมต่อกับพื้นที่ทำงานที่มีชุดข้อมูลที่เปิดใช้งานการรีเฟรชแบบเพิ่มหน่วย</span><span class="sxs-lookup"><span data-stu-id="f3675-212">[Create a new pipeline](deployment-pipelines-get-started.md#step-1---create-a-deployment-pipeline) and connect to it a workspace with a dataset that has incremental refresh enabled.</span></span>

* <span data-ttu-id="f3675-213">เปิดใช้งานการรีเฟรชแบบเพิ่มหน่วยในชุดข้อมูลที่อยู่ในพื้นที่ทำงาน *การพัฒนา*</span><span class="sxs-lookup"><span data-stu-id="f3675-213">Enable incremental refresh in a dataset that's already in a *development* workspace.</span></span>  

* <span data-ttu-id="f3675-214">สร้างไปป์ไลน์จากพื้นที่ทำงานการผลิตที่มีชุดข้อมูลที่ใช้การรีเฟรชแบบเพิ่มหน่วย</span><span class="sxs-lookup"><span data-stu-id="f3675-214">Create a pipeline from a production workspace that has a dataset that uses incremental refresh.</span></span> <span data-ttu-id="f3675-215">การดำเนินการนี้ทำได้โดยการกำหนดพื้นที่ทำงานให้กับขั้นตอน *การผลิต* ของไปป์ไลน์ใหม่ และใช้ [การปรับใช้แบบย้อนหลัง](deployment-pipelines-get-started.md#backwards-deployment) เพื่อปรับใช้กับขั้นตอน *การทดสอบ* และจากนั้นขั้นตอน *การพัฒนา*</span><span class="sxs-lookup"><span data-stu-id="f3675-215">This is done by assigning the workspace to a new pipeline's *production* stage, and using [backwards deployment](deployment-pipelines-get-started.md#backwards-deployment) to deploy to the *test* stage, and then to the *development* stage.</span></span>

* <span data-ttu-id="f3675-216">เผยแพร่ชุดข้อมูลที่ใช้การรีเฟรชแบบเพิ่มหน่วยไปยังพื้นที่ทำงานที่เป็นส่วนหนึ่งของไปป์ไลน์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="f3675-216">Publish a dataset that uses incremental refresh to a workspace that's part of an existing pipeline.</span></span>

#### <a name="limitations-and-considerations"></a><span data-ttu-id="f3675-217">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="f3675-217">Limitations and considerations</span></span>

<span data-ttu-id="f3675-218">สำหรับการรีเฟรชแบบเพิ่มหน่วย ไปป์ไลน์การปรับใช้สนับสนุนเฉพาะชุดข้อมูลที่ใช้ [เมตาดาต้าชุดข้อมูลที่ผ่านการเสริมประสิทธิภาพ](../connect-data/desktop-enhanced-dataset-metadata.md)</span><span class="sxs-lookup"><span data-stu-id="f3675-218">For incremental refresh, deployment pipelines only supports datasets that use [enhanced dataset metadata](../connect-data/desktop-enhanced-dataset-metadata.md).</span></span> <span data-ttu-id="f3675-219">ตั้งแต่การเปิดตัวของ Power BI Desktop ในเดือนกันยายน 2020 ชุดข้อมูลทั้งหมดที่สร้างหรือปรับเปลี่ยนด้วย Power BI Desktop จะปรับใช้เมตาดาต้าชุดข้อมูลที่ผ่านการเสริมประสิทธิภาพโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f3675-219">Beginning with the September 2020 release of Power BI Desktop, all datasets created or modified with Power BI Desktop automatically implement enhanced dataset metadata.</span></span>

<span data-ttu-id="f3675-220">เมื่อเผยแพร่ชุดข้อมูลไปยังไปป์ไลน์ที่ทำงานอยู่ที่เปิดใช้งานการรีเฟรชแบบเพิ่มหน่วย การเปลี่ยนแปลงต่อไปนี้จะส่งผลให้การปรับใช้ล้มเหลวเนื่องจากมีโอกาสในการสูญเสียข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="f3675-220">When republishing a dataset to an active pipeline with incremental refresh enabled, the following changes will result in deployment failure due to data loss potential:</span></span>

* <span data-ttu-id="f3675-221">เผยแพร่ชุดข้อมูลที่ไม่ได้ใช้การรีเฟรชแบบเพิ่มหน่วย เพื่อแทนที่ชุดข้อมูลที่มีการเปิดใช้งานการรีเฟรชแบบเพิ่มหน่วย</span><span class="sxs-lookup"><span data-stu-id="f3675-221">Republishing a dataset that doesn't use incremental refresh, to replace a dataset that has incremental refresh enabled.</span></span>

* <span data-ttu-id="f3675-222">การเปลี่ยนชื่อตารางที่มีการเปิดใช้งานการรีเฟรชแบบเพิ่มหน่วย</span><span class="sxs-lookup"><span data-stu-id="f3675-222">Renaming a table that has incremental refresh enabled.</span></span>

* <span data-ttu-id="f3675-223">การเปลี่ยนชื่อคอลัมน์ที่ไม่ผ่านการคำนวณในตารางที่มีการเปิดใช้งานการรีเฟรชแบบเพิ่มหน่วย</span><span class="sxs-lookup"><span data-stu-id="f3675-223">Renaming non-calculated columns in a table with incremental refresh enabled.</span></span>

<span data-ttu-id="f3675-224">การเปลี่ยนแปลงอื่น ๆ เช่นการเพิ่มคอลัมน์ การเอาคอลัมน์ออก และการเปลี่ยนชื่อคอลัมน์ที่ผ่านการคำนวณ อนุญาตให้ดำเนินการได้</span><span class="sxs-lookup"><span data-stu-id="f3675-224">Other changes such as adding a column, removing a column, and renaming a calculated column, are permitted.</span></span> <span data-ttu-id="f3675-225">อย่างไรก็ตาม ถ้าการเปลี่ยนแปลงมีผลต่อการแสดงผล คุณจะต้องรีเฟรชก่อนจึงจะเห็นการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="f3675-225">However, if the changes affect the display, you'll need to refresh before the change is visible.</span></span>

### <a name="composite-models"></a><span data-ttu-id="f3675-226">โมเดลแบบรวม</span><span class="sxs-lookup"><span data-stu-id="f3675-226">Composite models</span></span>

<span data-ttu-id="f3675-227">การใช้[แบบจำลองแบบรวม](../transform-model/desktop-composite-models.md) คุณสามารถตั้งค่ารายงานที่มีการเชื่อมต่อข้อมูลหลายรายการได้</span><span class="sxs-lookup"><span data-stu-id="f3675-227">Using [composite models](../transform-model/desktop-composite-models.md) you can set up a report with multiple data connections.</span></span>

<span data-ttu-id="f3675-228">คุณสามารถใช้ฟังก์ชันแบบจำลองแบบรวมเพื่อเชื่อมต่อชุดข้อมูล Power BI ไปยังชุดข้อมูลภายนอกเช่น บริการวิเคราะห์ Azure ได้</span><span class="sxs-lookup"><span data-stu-id="f3675-228">You can use the composite models functionality to connect a Power BI dataset to an external dataset such as Azure Analysis Services.</span></span> <span data-ttu-id="f3675-229">สำหรับข้อมูลเพิ่มเติม โปรดดู[การใช้ DirectQuery สำหรับชุดข้อมูล Power BI และบริการวิเคราะห์ Azure](../connect-data/desktop-directquery-datasets-azure-analysis-services.md)</span><span class="sxs-lookup"><span data-stu-id="f3675-229">For more information, see [Using DirectQuery for Power BI datasets and Azure Analysis Services](../connect-data/desktop-directquery-datasets-azure-analysis-services.md).</span></span>

<span data-ttu-id="f3675-230">ในไปป์ไลน์การปรับใช้ คุณสามารถใช้แบบจำลองแบบรวมเพื่อเชื่อมต่อชุดข้อมูลไปยังชุดข้อมูล Power BI อื่นภายนอกไปยังไปป์ไลน์ได้</span><span class="sxs-lookup"><span data-stu-id="f3675-230">In a deployment pipeline, you can use composite models to connect a dataset to another Power BI dataset external to the pipeline.</span></span>  

#### <a name="limitations"></a><span data-ttu-id="f3675-231">ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="f3675-231">Limitations</span></span>

<span data-ttu-id="f3675-232">การเชื่อมต่อแบบจำลองแบบรวมต่อไปนี้ไม่ได้รับการรองรับ:</span><span class="sxs-lookup"><span data-stu-id="f3675-232">The following composite models connections are not supported:</span></span>

* <span data-ttu-id="f3675-233">การเชื่อมต่อชุดข้อมูลที่อยู่ในพื้นที่ทำงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="f3675-233">Connecting datasets that reside in the same workspace.</span></span>

* <span data-ttu-id="f3675-234">การเชื่อมต่อชุดข้อมูลที่อยู่ในไปป์ไลน์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="f3675-234">Connecting datasets that reside in distinct pipelines.</span></span>

* <span data-ttu-id="f3675-235">การเชื่อมต่อชุดข้อมูลที่อยู่ในพื้นที่ทำงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="f3675-235">Connecting datasets that reside in the same pipeline.</span></span> 

## <a name="deploying-power-bi-apps"></a><span data-ttu-id="f3675-236">ปรับใช้แอป Power BI</span><span class="sxs-lookup"><span data-stu-id="f3675-236">Deploying Power BI apps</span></span>

<span data-ttu-id="f3675-237">[แอป Power BI](../consumer/end-user-apps.md) เป็นวิธีที่แนะนำสำหรับการกระจายเนื้อหาไปยังผู้บริโภค Power BI ฟรี</span><span class="sxs-lookup"><span data-stu-id="f3675-237">[Power BI apps](../consumer/end-user-apps.md) are the recommended way of distributing content to free Power BI consumers.</span></span> <span data-ttu-id="f3675-238">การใช้ไปป์ไลน์การปรับใช้ คุณสามารถจัดการแอป Power BI ในไปป์ไลน์การปรับใช้เพื่อให้คุณมีการควบคุมและมีความยืดหยุ่นมากขึ้นเมื่อมาถึงวงจรชีวิตแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="f3675-238">Using deployment pipelines you can manage Power BI apps in a deployment pipeline, so that you have more control and flexibility when it comes to your app's lifecycle.</span></span>

<span data-ttu-id="f3675-239">สร้างแอปสำหรับขั้นตอนไปป์ไลน์การปรับใช้แต่ละขั้นตอน เพื่อให้คุณสามารถทดสอบการอัปเดตแอปแต่ละครั้งจากมุมมองของผู้ใช้ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="f3675-239">Create an app for each deployment pipeline stage, so that you can test each app update from an end user's point of view.</span></span> <span data-ttu-id="f3675-240">ไปป์ไลน์การปรับใช้จะช่วยให้คุณสามารถจัดการกระบวนการนี้ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="f3675-240">A deployment pipeline allows you to manage this process easily.</span></span> <span data-ttu-id="f3675-241">ใช้ปุ่มเผยแพร่หรือมุมมองในการ์ดพื้นที่ทำงานเพื่อเผยแพร่หรือดูแอปในขั้นตอนไปป์ไลน์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f3675-241">Use the publish or view button in the workspace card, to publish or view the app in a specific pipeline stage.</span></span>

<span data-ttu-id="f3675-242">[![สกรีนช็อตที่ไฮไลท์ปุ่มเผยแพร่แอปที่ด้านล่างขวาของขั้นตอนการผลิต](media/deployment-pipelines-process/publish.png)](media/deployment-pipelines-process/publish.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="f3675-242">[![A screenshot highlighting the publish app button, at the bottom right of the production stage.](media/deployment-pipelines-process/publish.png)](media/deployment-pipelines-process/publish.png#lightbox)</span></span>

<span data-ttu-id="f3675-243">ในขั้นตอนการผลิต ปุ่มการดำเนินการหลักที่มุมล่างขวาเปิดหน้าการอัปเดตแอปใน Power BI เพื่อให้การอัปเดตข้อมูลเนื้อหาใดๆ พร้อมใช้งานสำหรับผู้ใช้แอป</span><span class="sxs-lookup"><span data-stu-id="f3675-243">In the production stage, the main action button on the bottom-right corner opens the update app page in Power BI, so that any content updates become available to app users.</span></span>

<span data-ttu-id="f3675-244">[![สกรีนช็อตที่ไฮไลท์ปุ่มเผยแพร่แอปที่ด้านล่างขวาของขั้นตอนการผลิต](media/deployment-pipelines-process/update-app.png)](media/deployment-pipelines-process/update-app.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="f3675-244">[![A screenshot highlighting the update app button, at the bottom right of the production stage.](media/deployment-pipelines-process/update-app.png)](media/deployment-pipelines-process/update-app.png#lightbox)</span></span>

>[!IMPORTANT]
><span data-ttu-id="f3675-245">กระบวนการปรับใช้ไม่รวมการอัปเดตเนื้อหาหรือการตั้งค่าของแอป</span><span class="sxs-lookup"><span data-stu-id="f3675-245">The deployment process does not include updating the app content or settings.</span></span> <span data-ttu-id="f3675-246">เมื่อต้องการนำการเปลี่ยนแปลงไปใช้กับเนื้อหาหรือการตั้งค่า คุณจำเป็นต้องอัปเดตแอปในขั้นตอนไปป์ไลน์ที่จำเป็นด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="f3675-246">To apply changes to content or settings, you need to manually update the app in the required pipeline stage.</span></span>

## <a name="permissions"></a><span data-ttu-id="f3675-247">การอนุญาต</span><span class="sxs-lookup"><span data-stu-id="f3675-247">Permissions</span></span>

<span data-ttu-id="f3675-248">สิทธิ์ของไปป์ไลน์และสิทธิ์ในพื้นที่ทำงานได้รับอนุญาตและจัดการแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="f3675-248">Pipeline permissions and workspace permissions are granted and managed separately.</span></span> <span data-ttu-id="f3675-249">ตัวอย่างเช่นผู้ใช้ที่มีการเข้าถึงไปป์ไลน์ที่ไม่มีสิทธิ์ในพื้นที่ทำงานจะสามารถดูไปป์ไลน์และแชร์กับผู้อื่นได้</span><span class="sxs-lookup"><span data-stu-id="f3675-249">For example, a user with pipeline access that doesn't have workspace permissions, will be able to view the pipeline and share it with others.</span></span> <span data-ttu-id="f3675-250">อย่างไรก็ตามผู้ใช้รายนี้จะไม่สามารถดูเนื้อหาของพื้นที่ทำงานในไปป์ไลน์ หรือในหน้าพื้นที่ทำงาน และจะไม่สามารถทำการปรับใช้ได้</span><span class="sxs-lookup"><span data-stu-id="f3675-250">However, this user will not be able to view the content of the workspace in the pipeline, or in the workspace page, and will not be able to perform deployments.</span></span>

### <a name="user-with-pipeline-access"></a><span data-ttu-id="f3675-251">ผู้ใช้ที่มีการเข้าถึงไปป์ไลน์</span><span class="sxs-lookup"><span data-stu-id="f3675-251">User with pipeline access</span></span>

<span data-ttu-id="f3675-252">ผู้ใช้ที่มีการเข้าถึงไปป์ไลน์มีสิทธิ์ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f3675-252">Users with pipeline access have the following permissions:</span></span>

* <span data-ttu-id="f3675-253">ดูไปป์ไลน์</span><span class="sxs-lookup"><span data-stu-id="f3675-253">View the pipeline</span></span>

* <span data-ttu-id="f3675-254">แชร์ไปป์ไลน์กับผู้อื่น</span><span class="sxs-lookup"><span data-stu-id="f3675-254">Share the pipeline with others</span></span>

* <span data-ttu-id="f3675-255">แก้ไขและลบไปป์ไลน์</span><span class="sxs-lookup"><span data-stu-id="f3675-255">Edit and delete the pipeline</span></span>

>[!NOTE]
><span data-ttu-id="f3675-256">การเข้าถึงไปป์ไลน์ไม่ได้ให้สิทธิ์ในการดูหรือดำเนินการกับเนื้อหาพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f3675-256">Pipeline access doesn't grant permissions to view or take actions on the workspace content.</span></span>

### <a name="workspace-viewer"></a><span data-ttu-id="f3675-257">ผู้ชมพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f3675-257">Workspace viewer</span></span>

<span data-ttu-id="f3675-258">ผู้ชมพื้นที่ทำงานที่มี *การเข้าถึงไปป์ไลน์* ยังสามารถทำสิ่งต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="f3675-258">Workspace viewers that have *pipeline access*, can also do the following:</span></span>

* <span data-ttu-id="f3675-259">บริโภคเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="f3675-259">Consume content</span></span>

>[!NOTE]
><span data-ttu-id="f3675-260">ผู้ชมพื้นที่ทำงานไม่สามารถเข้าถึงชุดข้อมูลหรือแก้ไขเนื้อหาพื้นที่ทำงานได้</span><span class="sxs-lookup"><span data-stu-id="f3675-260">Workspace viewers cannot access the dataset or edit workspace content.</span></span>

### <a name="workspace-contributor"></a><span data-ttu-id="f3675-261">ผู้สนับสนุนพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f3675-261">Workspace contributor</span></span>

<span data-ttu-id="f3675-262">ผู้สนับสนุนพื้นที่ทำงานที่มี *การเข้าถึงไปป์ไลน์* ยังสามารถทำสิ่งต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="f3675-262">Workspace contributors that have *pipeline access*, can also do the following:</span></span>

* <span data-ttu-id="f3675-263">บริโภคเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="f3675-263">Consume content</span></span>

* <span data-ttu-id="f3675-264">เปรียบเทียบขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="f3675-264">Compare stages</span></span>

* <span data-ttu-id="f3675-265">ดูชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f3675-265">View datasets</span></span>

### <a name="workspace-member"></a><span data-ttu-id="f3675-266">สมาชิกพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f3675-266">Workspace member</span></span>

<span data-ttu-id="f3675-267">สมาชิกพื้นที่ทำงานที่มี *การเข้าถึงไปป์ไลน์* ยังสามารถทำสิ่งต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="f3675-267">Workspace members that have *pipeline access*, can also do the following:</span></span>

* <span data-ttu-id="f3675-268">ดูเนื้อหาพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f3675-268">View workspace content</span></span>

* <span data-ttu-id="f3675-269">เปรียบเทียบขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="f3675-269">Compare stages</span></span>

* <span data-ttu-id="f3675-270">ปรับใช้รายงานและแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="f3675-270">Deploy reports and dashboards</span></span>

* <span data-ttu-id="f3675-271">เอาพื้นที่ทำงานออก</span><span class="sxs-lookup"><span data-stu-id="f3675-271">Remove workspaces</span></span>

### <a name="workspace-admin"></a><span data-ttu-id="f3675-272">ผู้ดูแลระบบพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f3675-272">Workspace admin</span></span>

<span data-ttu-id="f3675-273">ผู้ดูแลระบบพื้นที่ทำงานที่มี *การเข้าถึงไปป์ไลน์* สามารถดำเนินการแบบ *สมาชิกพื้นที่ทำงาน* และยังทำสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f3675-273">Workspace administrators that have *pipeline access*, can perform *workspace member* actions, and also do the following:</span></span>

* <span data-ttu-id="f3675-274">กำหนดพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f3675-274">Assign workspaces</span></span>

* <span data-ttu-id="f3675-275">เอาพื้นที่ทำงานออก</span><span class="sxs-lookup"><span data-stu-id="f3675-275">Remove workspaces</span></span>

### <a name="dataset-owner"></a><span data-ttu-id="f3675-276">เจ้าของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f3675-276">Dataset owner</span></span>

<span data-ttu-id="f3675-277">เจ้าของชุดข้อมูลที่เป็นสมาชิกพื้นที่ทำงานหรือผู้ดูแลระบบยังสามารถทำสิ่งต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="f3675-277">Dataset owners that are either workspace members or admins, can also do the following:</span></span>

* <span data-ttu-id="f3675-278">อัปเดตชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f3675-278">Update datasets</span></span>

* <span data-ttu-id="f3675-279">กำหนดค่ากฎ</span><span class="sxs-lookup"><span data-stu-id="f3675-279">Configure rules</span></span>

>[!NOTE]
><span data-ttu-id="f3675-280">ในส่วนนี้จะอธิบายสิทธิ์ของผู้ใช้ในไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="f3675-280">This section describes user permissions in deployment pipelines.</span></span> <span data-ttu-id="f3675-281">สิทธิ์ที่แสดงในส่วนนี้อาจมีแอปพลิเคชันที่แตกต่างกันในคุณลักษณะ Power BI อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f3675-281">The permissions listed in this section may have different applications in other Power BI features.</span></span>

## <a name="limitations"></a><span data-ttu-id="f3675-282">ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="f3675-282">Limitations</span></span>

<span data-ttu-id="f3675-283">ส่วนนี้แสดงรายการส่วนใหญ่ของขีดจำกัดในไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="f3675-283">This section lists most of the limitations in deployment pipelines.</span></span>

* <span data-ttu-id="f3675-284">พื้นที่ทำงานต้องอยู่ใน [ความจุแบบพรีเมียม](../admin/service-premium-what-is.md)</span><span class="sxs-lookup"><span data-stu-id="f3675-284">The workspace must reside on a [premium capacity](../admin/service-premium-what-is.md).</span></span>

* <span data-ttu-id="f3675-285">รายการ power BI เช่นรายงานและแดชบอร์ดที่มี [ป้ายชื่อระดับความลับของ Power BI](../admin/service-security-sensitivity-label-overview.md)ไม่สามารถปรับใช้ได้</span><span class="sxs-lookup"><span data-stu-id="f3675-285">Power BI items such as reports and dashboards that have Power BI [sensitivity labels](../admin/service-security-sensitivity-label-overview.md), cannot be deployed.</span></span>

* <span data-ttu-id="f3675-286">จำนวนสูงสุดของรายการ Power BI ที่สามารถปรับใช้ได้ในการจัดวางเดี่ยวคือ 300</span><span class="sxs-lookup"><span data-stu-id="f3675-286">The maximum number of Power BI items that can be deployed in a single deployment is 300.</span></span>

* <span data-ttu-id="f3675-287">ไม่รองรับการดาวน์โหลดไฟล์ PBIX หลังการปรับใช้</span><span class="sxs-lookup"><span data-stu-id="f3675-287">Downloading a PBIX file after deployment isn't supported.</span></span>

* <span data-ttu-id="f3675-288">สำหรับรายการของข้อจำกัดของพื้นที่ทำงาน ดู [ข้อจำกัดของการกำหนดพื้นที่ทำงาน](deployment-pipelines-get-started.md#workspace-assignment-limitations)</span><span class="sxs-lookup"><span data-stu-id="f3675-288">For a list of workspace limitations, see [workspace assignment limitations](deployment-pipelines-get-started.md#workspace-assignment-limitations).</span></span>

* <span data-ttu-id="f3675-289">สำหรับรายการของรายการที่ไม่ได้รับการรองรับ ดู [รายการที่ไม่ได้รับการรองรับ](#unsupported-items)</span><span class="sxs-lookup"><span data-stu-id="f3675-289">For a list of unsupported items, see [unsupported items](#unsupported-items).</span></span>

### <a name="dataset-limitations"></a><span data-ttu-id="f3675-290">ข้อจำกัดของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f3675-290">Dataset limitations</span></span>

* <span data-ttu-id="f3675-291">ชุดข้อมูลที่ใช้การเชื่อมต่อข้อมูลแบบเรียลไทม์ไม่สามารถจัดวางได้</span><span class="sxs-lookup"><span data-stu-id="f3675-291">Datasets that use real-time data connectivity cannot be deployed.</span></span>

* <span data-ttu-id="f3675-292">ในระหว่างการปรับใช้ถ้าชุดข้อมูลเป้าหมายใช้ [การเชื่อมต่อแบบสด](../connect-data/desktop-report-lifecycle-datasets.md) ชุดข้อมูลต้นฉบับต้องใช้โหมดการเชื่อมต่อนี้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="f3675-292">During deployment, if the target dataset is using a [live connection](../connect-data/desktop-report-lifecycle-datasets.md), the source dataset must use this connection mode too.</span></span>

* <span data-ttu-id="f3675-293">หลังจากที่มีการปรับใช้ การดาวน์โหลดชุดข้อมูล (จากขั้นตอนที่ได้รับการจัดวาง) จะไม่ได้รับการรองรับ</span><span class="sxs-lookup"><span data-stu-id="f3675-293">After deployment, downloading a dataset (from the stage it's been deployed to) is not supported.</span></span>

* <span data-ttu-id="f3675-294">สำหรับรายการของข้อจำกัดของกฎชุดข้อมูล ดู [ข้อจำกัดของกฎชุดข้อมูล](deployment-pipelines-get-started.md#dataset-rule-limitations)</span><span class="sxs-lookup"><span data-stu-id="f3675-294">For a list of dataset rule limitations, see [dataset rule limitations](deployment-pipelines-get-started.md#dataset-rule-limitations).</span></span>

## <a name="next-steps"></a><span data-ttu-id="f3675-295">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="f3675-295">Next steps</span></span>

>[!div class="nextstepaction"]
>[<span data-ttu-id="f3675-296">บทนำสู่ไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="f3675-296">Introduction to deployment pipelines</span></span>](deployment-pipelines-overview.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="f3675-297">แนวทางปฏิบัติที่ดีที่สุดสำหรับไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="f3675-297">Deployment pipelines best practices</span></span>](deployment-pipelines-best-practices.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="f3675-298">เริ่มต้นกับไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="f3675-298">Get started with deployment pipelines</span></span>](deployment-pipelines-get-started.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="f3675-299">การแก้ไขปัญหาไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="f3675-299">Deployment pipelines troubleshooting</span></span>](deployment-pipelines-troubleshooting.md)
