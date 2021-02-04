---
title: ย้ายแอปพลิเคชันการวิเคราะห์แบบฝังตัว Power BI ของคุณไปยังการผลิตสำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: เรียนรู้ขั้นตอนที่จำเป็นในการย้ายแอปพลิเคชัน Power BI ไปยังการผลิต เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: rkarlin
ms.topic: tutorial
ms.service: powerbi
ms.subservice: powerbi-developer
ms.custom: seodec18
ms.date: 06/02/2020
ms.openlocfilehash: 71eff0f09c0e34ffd8789f1b56347d754b6589bc
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97886683"
---
# <a name="move-your-embedded-app-to-production"></a><span data-ttu-id="4c8a9-104">ย้ายแอปแบบฝังตัวของคุณไปยังการผลิต</span><span class="sxs-lookup"><span data-stu-id="4c8a9-104">Move your embedded app to production</span></span>

<span data-ttu-id="4c8a9-105">หลังจากที่คุณพัฒนาแอปพลิเคชันของคุณเสร็จเรียบร้อยแล้ว หากต้องการย้ายไปยังการผลิต คุณจะต้องสำรองพื้นที่ทำงานของคุณด้วยความจุ</span><span class="sxs-lookup"><span data-stu-id="4c8a9-105">After you've completed developing your application, to move to production you'll need to back your workspace with a capacity.</span></span>

> [!Important]
> <span data-ttu-id="4c8a9-106">พื้นที่ทำงานทั้งหมด (ที่มีรายงานหรือแดชบอร์ดและที่มีชุดข้อมูล) จะต้องกำหนดไว้สำหรับความจุ</span><span class="sxs-lookup"><span data-stu-id="4c8a9-106">All workspaces (the ones containing the reports or dashboards, and the ones containing the datasets) must be assigned to a capacity.</span></span>

## <a name="create-a-capacity"></a><span data-ttu-id="4c8a9-107">สร้างความจุ</span><span class="sxs-lookup"><span data-stu-id="4c8a9-107">Create a capacity</span></span>

<span data-ttu-id="4c8a9-108">เมื่อสร้างความจุ คุณสามารถใช้ประโยชน์จากการมีทรัพยากรจัดสรรไว้สำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="4c8a9-108">By creating a capacity, you can take advantage of having a resource for your customers.</span></span> <span data-ttu-id="4c8a9-109">มีความจุสองชนิดที่คุณสามารถเลือกได้:</span><span class="sxs-lookup"><span data-stu-id="4c8a9-109">There are two types of capacities you can choose from:</span></span>

* <span data-ttu-id="4c8a9-110">**Power BI Premium** - การสมัครใช้งาน Microsoft 356 ระดับผู้เช่าที่มีอยู่สองกลุ่ม SKU ได้แก่ *EM* และ *P* เมื่อมีการฝังเนื้อหา Power BI โซลูชันนี้เรียกว่า *การฝัง Power BI*</span><span class="sxs-lookup"><span data-stu-id="4c8a9-110">**Power BI Premium** - A tenant-level Microsoft 356 subscription available in two SKU families, *EM* and *P*. When embedding Power BI content, this solution is referred to as *Power BI embedding*.</span></span> <span data-ttu-id="4c8a9-111">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสมัครสมาชิกนี้ โปรดดู [Power BI Premium คืออะไร](../../admin/service-premium-what-is.md)</span><span class="sxs-lookup"><span data-stu-id="4c8a9-111">For more information regarding this subscription, see [What is Power BI Premium?](../../admin/service-premium-what-is.md)</span></span>

* <span data-ttu-id="4c8a9-112">**Azure Power BI Embedded** - คุณสามารถซื้อความจุจาก [พอร์ทัล Microsoft Azure](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="4c8a9-112">**Azure Power BI Embedded** - You can purchase a capacity from the [Microsoft Azure portal](https://portal.azure.com).</span></span> <span data-ttu-id="4c8a9-113">การสมัครใช้งานนี้ใช้ *A* SKU</span><span class="sxs-lookup"><span data-stu-id="4c8a9-113">This subscription uses the *A* SKUs.</span></span> <span data-ttu-id="4c8a9-114">สำหรับรายละเอียดเกี่ยวกับวิธีการสร้างความจุ Power BI Embedded โปรดดู[สร้างความจุ Power BI Embedded ในพอร์ทัล Azure](azure-pbie-create-capacity.md)</span><span class="sxs-lookup"><span data-stu-id="4c8a9-114">For details on how to create a Power BI Embedded capacity, see [Create Power BI Embedded capacity in the Azure portal](azure-pbie-create-capacity.md).</span></span>

    > [!NOTE]
    > <span data-ttu-id="4c8a9-115">ด้วย A SKU คุณไม่สามารถเข้าถึงเนื้อหา Power BI ที่มีสิทธิ์การใช้งาน Power BI ฟรี</span><span class="sxs-lookup"><span data-stu-id="4c8a9-115">With A SKUs, you can't access Power BI content with a FREE Power BI license.</span></span>

### <a name="capacity-specifications"></a><span data-ttu-id="4c8a9-116">ข้อมูลจำเพาะของความจุ</span><span class="sxs-lookup"><span data-stu-id="4c8a9-116">Capacity specifications</span></span>

<span data-ttu-id="4c8a9-117">ตารางด้านล่างอธิบายแหล่งข้อมูลและขีดจำกัดของแต่ละ SKU</span><span class="sxs-lookup"><span data-stu-id="4c8a9-117">The table below describes the resources and limits of each SKU.</span></span> <span data-ttu-id="4c8a9-118">หากต้องการตรวจสอบความจุที่เหมาะสมที่สุดกับความต้องการของคุณ ให้ดูตาราง [SKU ใดที่ฉันควรซื้อสำหรับสถานการณ์ของฉัน](./embedded-faq.md#which-solution-should-i-choose)</span><span class="sxs-lookup"><span data-stu-id="4c8a9-118">To determine which capacity best fits your needs, see the [which SKU should I purchase for my scenario](./embedded-faq.md#which-solution-should-i-choose) table.</span></span>

| <span data-ttu-id="4c8a9-119">โหนดความจุ</span><span class="sxs-lookup"><span data-stu-id="4c8a9-119">Capacity Nodes</span></span> | <span data-ttu-id="4c8a9-120">วี-คอร์รวม</span><span class="sxs-lookup"><span data-stu-id="4c8a9-120">Total v-cores</span></span> | <span data-ttu-id="4c8a9-121">Backend v-cores</span><span class="sxs-lookup"><span data-stu-id="4c8a9-121">Backend v-cores</span></span> | <span data-ttu-id="4c8a9-122">RAM (GB)</span><span class="sxs-lookup"><span data-stu-id="4c8a9-122">RAM (GB)</span></span> | <span data-ttu-id="4c8a9-123">Frontend v-cores</span><span class="sxs-lookup"><span data-stu-id="4c8a9-123">Frontend v-cores</span></span> | <span data-ttu-id="4c8a9-124">DirectQuery/Live Connection (ต่อวินาที)</span><span class="sxs-lookup"><span data-stu-id="4c8a9-124">DirectQuery/Live Connection (per sec)</span></span> | <span data-ttu-id="4c8a9-125">การรีเฟรชแบบจำลองแบบคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="4c8a9-125">Model Refresh Parallelism</span></span> |
| --- | --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="4c8a9-126">EM1/A1</span><span class="sxs-lookup"><span data-stu-id="4c8a9-126">EM1/A1</span></span> | <span data-ttu-id="4c8a9-127">1</span><span class="sxs-lookup"><span data-stu-id="4c8a9-127">1</span></span> | <span data-ttu-id="4c8a9-128">0.5</span><span class="sxs-lookup"><span data-stu-id="4c8a9-128">0.5</span></span> | <span data-ttu-id="4c8a9-129">2.5</span><span class="sxs-lookup"><span data-stu-id="4c8a9-129">2.5</span></span> | <span data-ttu-id="4c8a9-130">0.5</span><span class="sxs-lookup"><span data-stu-id="4c8a9-130">0.5</span></span> | <span data-ttu-id="4c8a9-131">3.75</span><span class="sxs-lookup"><span data-stu-id="4c8a9-131">3.75</span></span> | <span data-ttu-id="4c8a9-132">1</span><span class="sxs-lookup"><span data-stu-id="4c8a9-132">1</span></span> |
| <span data-ttu-id="4c8a9-133">EM2/A2</span><span class="sxs-lookup"><span data-stu-id="4c8a9-133">EM2/A2</span></span> | <span data-ttu-id="4c8a9-134">2</span><span class="sxs-lookup"><span data-stu-id="4c8a9-134">2</span></span> | <span data-ttu-id="4c8a9-135">1</span><span class="sxs-lookup"><span data-stu-id="4c8a9-135">1</span></span> | <span data-ttu-id="4c8a9-136">5</span><span class="sxs-lookup"><span data-stu-id="4c8a9-136">5</span></span> | <span data-ttu-id="4c8a9-137">1</span><span class="sxs-lookup"><span data-stu-id="4c8a9-137">1</span></span> | <span data-ttu-id="4c8a9-138">7.5</span><span class="sxs-lookup"><span data-stu-id="4c8a9-138">7.5</span></span> | <span data-ttu-id="4c8a9-139">2</span><span class="sxs-lookup"><span data-stu-id="4c8a9-139">2</span></span> |
| <span data-ttu-id="4c8a9-140">EM3/A3</span><span class="sxs-lookup"><span data-stu-id="4c8a9-140">EM3/A3</span></span> | <span data-ttu-id="4c8a9-141">4</span><span class="sxs-lookup"><span data-stu-id="4c8a9-141">4</span></span> | <span data-ttu-id="4c8a9-142">2</span><span class="sxs-lookup"><span data-stu-id="4c8a9-142">2</span></span> | <span data-ttu-id="4c8a9-143">10</span><span class="sxs-lookup"><span data-stu-id="4c8a9-143">10</span></span> | <span data-ttu-id="4c8a9-144">2</span><span class="sxs-lookup"><span data-stu-id="4c8a9-144">2</span></span> | <span data-ttu-id="4c8a9-145">15</span><span class="sxs-lookup"><span data-stu-id="4c8a9-145">15</span></span> | <span data-ttu-id="4c8a9-146">3</span><span class="sxs-lookup"><span data-stu-id="4c8a9-146">3</span></span> |
| <span data-ttu-id="4c8a9-147">P1/A4</span><span class="sxs-lookup"><span data-stu-id="4c8a9-147">P1/A4</span></span> | <span data-ttu-id="4c8a9-148">8</span><span class="sxs-lookup"><span data-stu-id="4c8a9-148">8</span></span> | <span data-ttu-id="4c8a9-149">4</span><span class="sxs-lookup"><span data-stu-id="4c8a9-149">4</span></span> | <span data-ttu-id="4c8a9-150">25</span><span class="sxs-lookup"><span data-stu-id="4c8a9-150">25</span></span> | <span data-ttu-id="4c8a9-151">4</span><span class="sxs-lookup"><span data-stu-id="4c8a9-151">4</span></span> | <span data-ttu-id="4c8a9-152">30</span><span class="sxs-lookup"><span data-stu-id="4c8a9-152">30</span></span> | <span data-ttu-id="4c8a9-153">6</span><span class="sxs-lookup"><span data-stu-id="4c8a9-153">6</span></span> |
| <span data-ttu-id="4c8a9-154">P2/A5</span><span class="sxs-lookup"><span data-stu-id="4c8a9-154">P2/A5</span></span> | <span data-ttu-id="4c8a9-155">16</span><span class="sxs-lookup"><span data-stu-id="4c8a9-155">16</span></span> | <span data-ttu-id="4c8a9-156">8</span><span class="sxs-lookup"><span data-stu-id="4c8a9-156">8</span></span> | <span data-ttu-id="4c8a9-157">50</span><span class="sxs-lookup"><span data-stu-id="4c8a9-157">50</span></span> | <span data-ttu-id="4c8a9-158">8</span><span class="sxs-lookup"><span data-stu-id="4c8a9-158">8</span></span> | <span data-ttu-id="4c8a9-159">60</span><span class="sxs-lookup"><span data-stu-id="4c8a9-159">60</span></span> | <span data-ttu-id="4c8a9-160">12</span><span class="sxs-lookup"><span data-stu-id="4c8a9-160">12</span></span> |
| <span data-ttu-id="4c8a9-161">P3/A6</span><span class="sxs-lookup"><span data-stu-id="4c8a9-161">P3/A6</span></span> | <span data-ttu-id="4c8a9-162">32</span><span class="sxs-lookup"><span data-stu-id="4c8a9-162">32</span></span> | <span data-ttu-id="4c8a9-163">16</span><span class="sxs-lookup"><span data-stu-id="4c8a9-163">16</span></span> | <span data-ttu-id="4c8a9-164">100</span><span class="sxs-lookup"><span data-stu-id="4c8a9-164">100</span></span> | <span data-ttu-id="4c8a9-165">16</span><span class="sxs-lookup"><span data-stu-id="4c8a9-165">16</span></span> | <span data-ttu-id="4c8a9-166">120</span><span class="sxs-lookup"><span data-stu-id="4c8a9-166">120</span></span> | <span data-ttu-id="4c8a9-167">24</span><span class="sxs-lookup"><span data-stu-id="4c8a9-167">24</span></span> |
| | | | | | | |

## <a name="development-testing"></a><span data-ttu-id="4c8a9-168">การทดสอบการพัฒนา</span><span class="sxs-lookup"><span data-stu-id="4c8a9-168">Development testing</span></span>

<span data-ttu-id="4c8a9-169">สำหรับการทดสอบการพัฒนา คุณสามารถใช้โทเค็นรุ่นทดลองใช้แบบฝังพร้อมกับสิทธิ์ใช้งานแบบ Pro</span><span class="sxs-lookup"><span data-stu-id="4c8a9-169">For development testing, you can use embed trial tokens with a Pro license.</span></span> <span data-ttu-id="4c8a9-170">หากต้องการฝังในสภาพแวดล้อมการผลิต ให้ใช้ความจุ</span><span class="sxs-lookup"><span data-stu-id="4c8a9-170">To embed in a production environment, use a capacity.</span></span>

<span data-ttu-id="4c8a9-171">จำนวนโทเค็นการทดลองแบบฝังตัวที่ *โครงร่างสำคัญของบริการ* หรือ *ผู้ใช้หลัก* (บัญชีหลัก) ของ Power BI สามารถสร้างได้นั้นมีจำกัด</span><span class="sxs-lookup"><span data-stu-id="4c8a9-171">The number of embed trial tokens a Power BI *service principal* or *master user* (master account) can generate, is limited.</span></span> <span data-ttu-id="4c8a9-172">ใช้ API ของ[คุณลักษณะที่มีอยู่](/rest/api/power-bi/availablefeatures/getavailablefeatures)เพื่อตรวจสอบเปอร์เซ็นต์ของการใช้งานแบบฝังในปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="4c8a9-172">Use the [Available Features](/rest/api/power-bi/availablefeatures/getavailablefeatures) API to check the percentage of your current embedded usage.</span></span> <span data-ttu-id="4c8a9-173">จำนวนการใช้งานจะปรากฏขึ้นต่อบริการหลักหรือบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="4c8a9-173">The usage amount is displayed per service principal or master account.</span></span>

<span data-ttu-id="4c8a9-174">หากคุณใช้งานโทเค็นแบบฝังหมดขณะทดสอบ คุณจำเป็นต้องซื้อ Power BI Embedded หรือ[ความจุ](embedded-capacity.md) Premium</span><span class="sxs-lookup"><span data-stu-id="4c8a9-174">If you run out of embed tokens while testing, you need to purchase a Power BI Embedded or Premium [capacity](embedded-capacity.md).</span></span> <span data-ttu-id="4c8a9-175">ไม่มีการจำกัดจำนวนโทเค็นแบบฝังที่คุณสามารถสร้างได้ด้วยความจุ</span><span class="sxs-lookup"><span data-stu-id="4c8a9-175">There's no limit to the number of embed tokens you can generate with a capacity.</span></span>

## <a name="assign-a-workspace-to-a-capacity"></a><span data-ttu-id="4c8a9-176">กำหนดพื้นที่ทำงานของแอปไปยังความจุ</span><span class="sxs-lookup"><span data-stu-id="4c8a9-176">Assign a workspace to a capacity</span></span>

<span data-ttu-id="4c8a9-177">เมื่อคุณสร้างความจุแล้ว คุณสามารถกำหนดพื้นที่ทำงานไปยังความจุนั้นได้</span><span class="sxs-lookup"><span data-stu-id="4c8a9-177">Once you create a capacity, you can assign your workspace to that capacity.</span></span>

<span data-ttu-id="4c8a9-178">พื้นที่ทำงานทั้งหมดที่ประกอบด้วยแหล่งข้อมูล Power BI ที่เกี่ยวข้องกับเนื้อหาแบบฝังตัว (รวมถึงชุดข้อมูล รายงานและแดชบอร์ด) จะต้องได้รับมอบหมายไปยังความจุ</span><span class="sxs-lookup"><span data-stu-id="4c8a9-178">All the workspaces that contain Power BI resources related to the embedded content (including datasets, reports, and dashboards), must be assigned to capacities.</span></span> <span data-ttu-id="4c8a9-179">ตัวอย่างเช่น หากรายงานแบบฝังและชุดข้อมูลที่ผูกไว้อยู่ในพื้นที่ทำงานที่ต่างกันสองแห่ง ต้องมอบหมายพื้นที่ทำงานทั้งสองแห่งไปยังความจุ</span><span class="sxs-lookup"><span data-stu-id="4c8a9-179">For example, if an embedded report and the dataset bound to it reside in different workspaces, both workspaces must be assigned to capacities.</span></span>

### <a name="assign-a-workspace-to-a-capacity-using-a-service-principal"></a><span data-ttu-id="4c8a9-180">กำหนดพื้นที่ทำงานให้กับความจุโดยใช้โครงร่างสำคัญของบริการ</span><span class="sxs-lookup"><span data-stu-id="4c8a9-180">Assign a workspace to a capacity using a service principal</span></span>

<span data-ttu-id="4c8a9-181">หากต้องกำหนดความจุกับพื้นที่ทำงานโดยใช้[โครงร่างสำคัญของบริการ](embed-service-principal.md) ให้ใช้ [Power BI REST API](/rest/api/power-bi/capacities/groups_assigntocapacity)</span><span class="sxs-lookup"><span data-stu-id="4c8a9-181">To assign a capacity to a workspace using a[service principal](embed-service-principal.md), use the [Power BI REST API](/rest/api/power-bi/capacities/groups_assigntocapacity).</span></span> <span data-ttu-id="4c8a9-182">เมื่อคุณกำลังใช้ Power BI REST API ทำให้แน่ใจว่าใช้[ ID ออบเจ็กต์ของโครงร่างสำคัญของบริการ](embed-service-principal.md)</span><span class="sxs-lookup"><span data-stu-id="4c8a9-182">When you're using the Power BI REST APIs, make sure to use the [service principal object ID](embed-service-principal.md).</span></span>

### <a name="assign-a-workspace-to-a-capacity-using-a-master-user"></a><span data-ttu-id="4c8a9-183">กำหนดพื้นที่ทำงานให้กับความจุโดยใช้ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="4c8a9-183">Assign a workspace to a capacity using a master user</span></span>

<span data-ttu-id="4c8a9-184">ทำตามขั้นตอนด้านล่างเพื่อกำหนดความจุสำหรับพื้นที่ทำงานโดยใช้ **ผู้ใช้หลัก**</span><span class="sxs-lookup"><span data-stu-id="4c8a9-184">Follow the steps below to assign a capacity to a workspace using a **master user**.</span></span>

1. <span data-ttu-id="4c8a9-185">เปิดพื้นที่ทำงานใน **บริการ Power BI** เลือก</span><span class="sxs-lookup"><span data-stu-id="4c8a9-185">Open the workspace in **Power BI service**, select the</span></span> 

1. <span data-ttu-id="4c8a9-186">ภายใน **บริการของ Power BI** ขยายพื้นที่ทำงาน และเลือกที่จุดไข่ปลาสำหรับพื้นที่ทำงานที่คุณกำลังใช้เพื่อฝังเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="4c8a9-186">Within the **Power BI service**, expand workspaces and select the ellipsis for the workspace you're using for embedding your content.</span></span> <span data-ttu-id="4c8a9-187">แล้วเลือก **แก้ไขพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="4c8a9-187">Then select **Edit workspaces**.</span></span>

    >[!div class="mx-imgBorder"]
    >:::image type="content" source="media/move-to-production/workspace-settings.png" alt-text="สกรีนช็อตที่แสดงเมนูการตั้งค่าพื้นที่ทำงานในพอร์ทัลบริการ Power BI":::

2. <span data-ttu-id="4c8a9-189">เลือกแท็บ **Premium** และทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4c8a9-189">Select the **Premium** tab, and do the following:</span></span>

    * <span data-ttu-id="4c8a9-190">เปิดใช้งาน **ความจุ**</span><span class="sxs-lookup"><span data-stu-id="4c8a9-190">Enable **Capacity**.</span></span>

    * <span data-ttu-id="4c8a9-191">เลือกความจุที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="4c8a9-191">Select the capacity you created.</span></span>

    * <span data-ttu-id="4c8a9-192">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="4c8a9-192">Select **Save**.</span></span>

    >[!div class="mx-imgBorder"]
    >:::image type="content" source="media/move-to-production/premium-tab.png" alt-text="สกรีนช็อตที่แสดงแท็บการตั้งค่าพื้นที่ทำงานแบบ premium ในพอร์ทัลบริการ Power BI":::

    <span data-ttu-id="4c8a9-194">หลังจากกำหนดพื้นที่ทำงานของคุณไปยังความจุแล้ว เพชรจะปรากฏขึ้นข้าง ๆ</span><span class="sxs-lookup"><span data-stu-id="4c8a9-194">After assigning your workspace to a capacity, a diamond appears next to it</span></span> 

    >[!div class="mx-imgBorder"]
    >:::image type="content" source="media/move-to-production/premium-workspace.png" alt-text="สกรีนช็อตที่แสดงเพชรถัดจากพื้นที่ทำงานที่มีความจุระดับพรีเมียมในพอร์ทัลบริการ Power BI":::

## <a name="next-steps"></a><span data-ttu-id="4c8a9-196">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4c8a9-196">Next steps</span></span>

>[!div class="nextstepaction"]
>[<span data-ttu-id="4c8a9-197">ความจุและ SKU ในการวิเคราะห์แบบฝังตัวของ Power BI</span><span class="sxs-lookup"><span data-stu-id="4c8a9-197">Capacity and SKUs in Power BI embedded analytics</span></span>](embedded-capacity.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="4c8a9-198">ความจุและ SKU ในการวิเคราะห์แบบฝังของ Power BI</span><span class="sxs-lookup"><span data-stu-id="4c8a9-198">Capacity planning in Power BI embedded analytics</span></span>](embedded-capacity-planning.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="4c8a9-199">ข้อควรพิจารณาเมื่อสร้างโทเค็นแบบฝัง</span><span class="sxs-lookup"><span data-stu-id="4c8a9-199">Considerations when generating an embed token</span></span>](generate-embed-token.md)