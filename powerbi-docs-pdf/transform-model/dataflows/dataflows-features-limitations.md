---
title: ขีดจำกัดกระแสข้อมูล ข้อจำกัด และตัวเชื่อมต่อและคุณลักษณะที่รองรับ
description: ภาพรวมของความสามารถทั้งหมดของกระแสข้อมูล
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-dataflows
ms.topic: how-to
ms.date: 10/01/2020
LocalizationGroup: Data from files
ms.openlocfilehash: 762a45dc48bd78ffebcbe68ef2f5ed216ec3cc51
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96416105"
---
# <a name="dataflows-limitations-and-considerations"></a><span data-ttu-id="30f47-103">ข้อจำกัดและข้อควรพิจารณาของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="30f47-103">Dataflows limitations and considerations</span></span>

<span data-ttu-id="30f47-104">มีข้อจำกัดของกระแสข้อมูลบางประการในการเขียน การรีเฟรช และการจัดการความจุที่ผู้ใช้ควรคำนึงถึงดังที่อธิบายไว้ในส่วนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="30f47-104">There are a few dataflow limitations across authoring, refreshes, and capacity management that users should keep in mind, as described in the following sections.</span></span>

## <a name="dataflow-authoring"></a><span data-ttu-id="30f47-105">การเขียนกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="30f47-105">Dataflow Authoring</span></span>

<span data-ttu-id="30f47-106">เมื่อเขียนกระแสข้อมูล ผู้ใช้ควรระวังข้อควรพิจารณาดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="30f47-106">When authoring dataflows, users should be mindful of the following considerations:</span></span>

* <span data-ttu-id="30f47-107">การเขียนในกระแสข้อมูลจะดำเนินการได้ในสภาพแวดล้อม Power Query Online (PQO) ดูข้อจำกัดที่อธิบายไว้ใน [ขีดจำกัด Power Query](/power-query/power-query-online-limits)</span><span class="sxs-lookup"><span data-stu-id="30f47-107">Authoring in Dataflows is done in the Power Query Online (PQO) environment; see the limitations described in [Power Query limits](/power-query/power-query-online-limits).</span></span>
<span data-ttu-id="30f47-108">เนื่องจากดำเนินการเขียนกระแสข้อมูลในสภาพแวดล้อม Power Query Online (PQO) การอัปเดตที่ดำเนินการบนการกำหนดค่าปริมาณงานกระแสข้อมูลจะส่งผลต่อการรีเฟรชเท่านั้นและจะไม่มีผลกระทบต่อประสบการณ์การเขียน</span><span class="sxs-lookup"><span data-stu-id="30f47-108">Because dataflows authoring is done in the  Power Query Online (PQO) environment, updates performed on the Dataflows workload configurations  only impact refreshes, and will not have an impact on the authoring experience</span></span>

* <span data-ttu-id="30f47-109">เฉพาะเจ้าของเท่านั้นที่สามารถแก้ไขกระแสข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="30f47-109">Dataflows can only be modified by their owners</span></span>

* <span data-ttu-id="30f47-110">กระแสข้อมูลไม่พร้อมใช้งานใน *พื้นที่ทำงานของฉัน*</span><span class="sxs-lookup"><span data-stu-id="30f47-110">Dataflows are not available in *My Workspace*</span></span>

* <span data-ttu-id="30f47-111">กระแสข้อมูลโดยใช้แหล่งข้อมูลเกตเวย์ไม่สนับสนุนข้อมูลประจำตัวหลายรายการสำหรับแหล่งข้อมูลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="30f47-111">Dataflows using gateway data sources do not support multiple credentials for the same data source</span></span>

* <span data-ttu-id="30f47-112">การใช้ตัวเชื่อมต่อ Web.Page จำเป็นต้องมีเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="30f47-112">Using the Web.Page connector requires a gateway</span></span>

## <a name="api-considerations"></a><span data-ttu-id="30f47-113">ข้อควรพิจารณาของ API</span><span class="sxs-lookup"><span data-stu-id="30f47-113">API Considerations</span></span>

<span data-ttu-id="30f47-114">คุณสามารถดูข้อมูลเพิ่มเติมเกี่ยวกับ REST API ของกระแสข้อมูลได้ใน [ข้อมูลอ้างอิง REST API](/rest/api/power-bi/dataflows)</span><span class="sxs-lookup"><span data-stu-id="30f47-114">More about supported Dataflows REST APIs can be found in the [REST API reference](/rest/api/power-bi/dataflows).</span></span> <span data-ttu-id="30f47-115">ต่อไปนี้คือข้อควรพิจารณาบางประการที่ควรทราบ:</span><span class="sxs-lookup"><span data-stu-id="30f47-115">Here are some considerations to keep in mind:</span></span>

* <span data-ttu-id="30f47-116">การส่งออกและนำเข้ากระแสข้อมูลจะทำให้กระแสข้อมูลนั้นมี ID ใหม่</span><span class="sxs-lookup"><span data-stu-id="30f47-116">Exporting and Importing a dataflow gives that dataflow a new ID</span></span>

* <span data-ttu-id="30f47-117">การนำเข้ากระแสข้อมูลที่ประกอบด้วยเอนทิตีที่เชื่อมโยงจะไม่แก้ไขการอ้างอิงที่มีอยู่ภายในกระแสข้อมูล (ควรแก้ไขคิวรีเหล่านี้ด้วยตนเองก่อนที่จะนำเข้ากระแสข้อมูล)</span><span class="sxs-lookup"><span data-stu-id="30f47-117">Importing dataflows that contain linked entities will not fix the existing references within the dataflow (these queries should be fixed manually before importing the dataflow)</span></span>

* <span data-ttu-id="30f47-118">คุณสามารถเขียนทับกระแสข้อมูลด้วยพารามิเตอร์ *CreateOrOverwrite* ได้หากสร้างขึ้นในตอนแรกโดยใช้ API นำเข้า</span><span class="sxs-lookup"><span data-stu-id="30f47-118">Dataflows can be overwritten with the *CreateOrOverwrite* parameter, if they have initially been created using the import API</span></span>

## <a name="dataflows-in-shared"></a><span data-ttu-id="30f47-119">กระแสข้อมูลอยู่ในความจุแบบแชร์</span><span class="sxs-lookup"><span data-stu-id="30f47-119">Dataflows in Shared</span></span>

<span data-ttu-id="30f47-120">มีข้อจำกัดสำหรับกระแสข้อมูลในความจุที่แชร์:</span><span class="sxs-lookup"><span data-stu-id="30f47-120">There are  limitations for Dataflows in shared capacities:</span></span>

* <span data-ttu-id="30f47-121">เมื่อรีเฟรชกระแสข้อมูล ระยะหมดเวลาในการแชร์คือ 2 ชั่วโมงต่อเอนทิตีและ 3 ชั่วโมงต่อกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="30f47-121">When refreshing Dataflows, timeouts in Shared are 2 hours per entity, and 3 hours per Dataflow</span></span>
* <span data-ttu-id="30f47-122">ไม่สามารถสร้างเอนทิตีที่เชื่อมโยงในกระแสข้อมูลที่ใช้ร่วมกันได้ แม้ว่าเอนทิตีดังกล่าวจะสามารถอยู่ในกระแสข้อมูลได้ตราบเท่าที่คุณสมบัติ *เปิดใช้งานการโหลด* บนคิวรีถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="30f47-122">Linked entities cannot be created in shared Dataflows, although they can exist within the Dataflow as long as the *Load Enabled* property on the query is disabled</span></span>
* <span data-ttu-id="30f47-123">ไม่สามารถสร้างเอนทิตีที่คำนวณในกระแสข้อมูลที่แชร์</span><span class="sxs-lookup"><span data-stu-id="30f47-123">Computed entities cannot be created in shared Dataflows</span></span>
* <span data-ttu-id="30f47-124">บริการ AutoML และ Cognitive ไม่พร้อมใช้งานในกระแสข้อมูลที่แชร์</span><span class="sxs-lookup"><span data-stu-id="30f47-124">AutoML and Cognitive services are not available in shared Dataflows</span></span>
* <span data-ttu-id="30f47-125">การรีเฟรชแบบเพิ่มหน่วยไม่ทำงานในกระแสข้อมูลที่แชร์</span><span class="sxs-lookup"><span data-stu-id="30f47-125">Incremental refresh does not work in shared Dataflows</span></span>

## <a name="dataflows-in-premium"></a><span data-ttu-id="30f47-126">กระแสข้อมูลอยู่ในความจุแบบ Premium</span><span class="sxs-lookup"><span data-stu-id="30f47-126">Dataflows in Premium</span></span>

<span data-ttu-id="30f47-127">กระแสข้อมูลที่มีอยู่ใน Premium มีขีดจำกัดและข้อควรพิจารณาต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="30f47-127">Dataflows that exist in Premium have the following limitations and considerations.</span></span>

<span data-ttu-id="30f47-128">**ข้อควรพิจารณาเกี่ยวกับการรีเฟรชและข้อมูล:**</span><span class="sxs-lookup"><span data-stu-id="30f47-128">**Refreshes and data considerations:**</span></span>

* <span data-ttu-id="30f47-129">เมื่อรีเฟรชกระแสข้อมูล ระยะหมดเวลาคือ 24 ชั่วโมง (ไม่มีความแตกต่างสำหรับเอนทิตีและ/หรือกระแสข้อมูล)</span><span class="sxs-lookup"><span data-stu-id="30f47-129">When refreshing Dataflows, timeouts are 24 hours (no distinction for entities and/or dataflows)</span></span>

* <span data-ttu-id="30f47-130">การเปลี่ยนกระแสข้อมูลจากนโยบายการรีเฟรชแบบเพิ่มหน่วยเป็นการรีเฟรชปกติหรือในทางกลับกันจะทำให้ข้อมูลทั้งหมดถูกลบ</span><span class="sxs-lookup"><span data-stu-id="30f47-130">Changing a dataflow from an incremental refresh policy to a normal refresh, or vice versa, will drop all data</span></span>

* <span data-ttu-id="30f47-131">การแก้ไขสคีมาของกระแสข้อมูลจะทำให้ข้อมูลทั้งหมดถูกลบ</span><span class="sxs-lookup"><span data-stu-id="30f47-131">Modifying a dataflow's schema will drop all data</span></span>

<span data-ttu-id="30f47-132">**เอนทิตีที่เชื่อมโยงและคำนวณ:**</span><span class="sxs-lookup"><span data-stu-id="30f47-132">**Linked and Computed Entities:**</span></span>

* <span data-ttu-id="30f47-133">เอนทิตีที่เชื่อมโยงสามารถลงลึกข้อมูลอ้างอิงได้ถึง 32 รายการ</span><span class="sxs-lookup"><span data-stu-id="30f47-133">Linked entities can go down to a depth of 32 references</span></span>

* <span data-ttu-id="30f47-134">วงจรอ้างอิงของเเอนทิตี้ที่เชื่อมโยงไม่ได้รับอนุญาตให้ใช้</span><span class="sxs-lookup"><span data-stu-id="30f47-134">Cyclic dependencies of linked entities are not allowed</span></span>

* <span data-ttu-id="30f47-135">คุณไม่สามารถเชื่อมโยงเอนทิตีที่เชื่อมโยงแล้วกับเอนทิตีปกติที่ได้รับข้อมูลจากแหล่งข้อมูลในองค์กรได้</span><span class="sxs-lookup"><span data-stu-id="30f47-135">A linked entity can't be joined with a regular entity that gets its data from an on-premises data source</span></span>

* <span data-ttu-id="30f47-136">เมื่อมีการใช้คิวรี (ตัวอย่างเช่น คิวรี *A*) ในการคำนวณของคิวรีอื่น (คิวรี *B*) ในกระแสข้อมูล คิวรี *B* จะกลายเป็นเอนทิตีที่มีการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="30f47-136">When a query (query *A*, for example) is used in the calculation of another query (query *B*) in dataflows, query *B* becomes a calculated entity.</span></span> <span data-ttu-id="30f47-137">คิวรีที่คำนวณไม่สามารถอ้างอิงไปยังแหล่งข้อมูลภายในองค์กรได้</span><span class="sxs-lookup"><span data-stu-id="30f47-137">Calculated entities cannot refer to on-premises sources.</span></span>


<span data-ttu-id="30f47-138">**กลไกการคำนวณ:**</span><span class="sxs-lookup"><span data-stu-id="30f47-138">**Compute Engine:**</span></span>

* <span data-ttu-id="30f47-139">เมื่อคุณใช้กลไกการคำนวณ เวลาในการนำเข้าข้อมูลเพิ่มขึ้นประมาณ 10% ถึง 20% ในช่วงแรก</span><span class="sxs-lookup"><span data-stu-id="30f47-139">While using the Compute engine, there is an approximate 10% to 20% initial increase in time for data ingestion.</span></span>

  1. <span data-ttu-id="30f47-140">ซึ่งเกิดขึ้นกับกระแสข้อมูลแรกที่อยู่ในกลไกการคำนวณและอ่านข้อมูลจากแหล่งข้อมูลเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="30f47-140">This only applied to the first dataflow that is on the compute engine, and reads data from the data source</span></span>
  2. <span data-ttu-id="30f47-141">กระแสข้อมูลที่ตามมา ซึ่งใช้แหล่งที่มาหนึ่งจะไม่ได้รับโทษเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="30f47-141">Subsequent dataflows, that use the source one will not incur the same penalty</span></span>

* <span data-ttu-id="30f47-142">เฉพาะการดำเนินการบางอย่างเท่านั้นที่ใช้กลไกการคำนวณและเฉพาะเมื่อใช้ผ่านเอนทิตีที่เชื่อมโยงหรือเป็นเอนทิตีที่คำนวณ</span><span class="sxs-lookup"><span data-stu-id="30f47-142">Only certain operations make use of the compute engine, and only when used through a linked entity or as a computed entity.</span></span> <span data-ttu-id="30f47-143">รายการการดำเนินการทั้งหมดมีอยู่ใน [บล็อกโพสต์นี้](http://petcu40.blogspot.com/2019/06/m-folding-in-enhanced-engine-of-power.html)</span><span class="sxs-lookup"><span data-stu-id="30f47-143">A full list of operations is available in [this blog post](http://petcu40.blogspot.com/2019/06/m-folding-in-enhanced-engine-of-power.html).</span></span>


<span data-ttu-id="30f47-144">**การจัดการความจุ:**</span><span class="sxs-lookup"><span data-stu-id="30f47-144">**Capacity Management:**</span></span>

* <span data-ttu-id="30f47-145">ตามการออกแบบ ความจุ Power BI ระดับพรีเมียมมีตัวจัดการทรัพยากรภายในซึ่งจำกัดปริมาณงานในรูปแบบต่างๆ เมื่อความจุกำลังทำงานบนหน่วยความจำเหลือน้อย</span><span class="sxs-lookup"><span data-stu-id="30f47-145">By design, the Premium Power BI Capacities have an internal resource manager which throttles the workloads in different ways when the capacity is running on low memory.</span></span>

  1. <span data-ttu-id="30f47-146">สำหรับกระแสข้อมูล ความดันการควบคุมนี้จะลดจำนวนคอนเทนเนอร์ M ที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="30f47-146">For Dataflows, this throttling pressure reduces the number of available M Containers</span></span>
  2. <span data-ttu-id="30f47-147">คุ๕สามารถตั้งค่าหน่วยความจำสำหรับกระแสข้อมูลเป็น 100% ด้วยคอนเทนเนอร์ที่มีขนาดเหมาะสมสำหรับขนาดข้อมูลของคุณ และปริมาณงานจะจัดการจำนวนคอนเทนเนอร์อย่างเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="30f47-147">The memory for Dataflows can be set to 100%, with an appropriately sized container for your data sizes, and the workload will manage the number of containers appropriately</span></span>

* <span data-ttu-id="30f47-148">คุณสามารถหาจำนวนคอนเทนเนอร์โดยประมาณได้จากการหารหน่วยความจำทั้งหมดที่จัดสรรให้กับปริมาณงานด้วยจำนวนหน่วยความจำที่จัดสรรให้กับคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="30f47-148">The approximate number of containers can be found out by dividing the total memory allocated to the workload by the amount of memory allocated to a container</span></span>

## <a name="dataflow-usage-in-datasets"></a><span data-ttu-id="30f47-149">การใช้กระแสข้อมูลในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="30f47-149">Dataflow usage in datasets</span></span>

* <span data-ttu-id="30f47-150">เมื่อสร้างชุดข้อมูลใน Power BI Desktop แล้วเผยแพร่ไปยังบริการ Power BI ตรวจสอบให้แน่ใจว่าข้อมูลประจำตัวที่ใช้ใน Power BI Desktop สำหรับแหล่งข้อมูล Dataflows เป็นข้อมูลประจำตัวเดียวกับที่ใช้เมื่อชุดข้อมูลถูกเผยแพร่ไปยังบริการ</span><span class="sxs-lookup"><span data-stu-id="30f47-150">When creating a dataset in Power BI Desktop, and then publishing it to the Power BI service, ensure the credentials used in Power BI Desktop for the Dataflows data source are the same credentials used when the dataset is published to the service.</span></span>
  1. <span data-ttu-id="30f47-151">ความล้มเหลวในการตรวจสอบให้แน่ใจว่าข้อมูลประจำตัวเหล่านั้นเป็นผลลัพธ์เดียวกันในข้อผิดพลาด *ไม่พบคีย์* เมื่อรีเฟรชชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="30f47-151">Failing to ensure those credentials are the same results in a *Key not found* error upon dataset refresh</span></span>

## <a name="next-steps"></a><span data-ttu-id="30f47-152">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="30f47-152">Next steps</span></span>
<span data-ttu-id="30f47-153">บทความต่อไปนี้ให้ข้อมูลเพิ่มเติมเกี่ยวกับกระแสข้อมูลและ Power BI:</span><span class="sxs-lookup"><span data-stu-id="30f47-153">The following articles provide more information about dataflows and Power BI:</span></span>

* [<span data-ttu-id="30f47-154">ข้อมูลเบื้องต้นเกี่ยวกับกระแสข้อมูลและการเตรียมข้อมูลด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="30f47-154">Introduction to dataflows and self-service data prep</span></span>](dataflows-introduction-self-service.md)
* [<span data-ttu-id="30f47-155">การสร้างกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="30f47-155">Creating a dataflow</span></span>](dataflows-create.md)
* [<span data-ttu-id="30f47-156">กำหนดค่าและใช้กระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="30f47-156">Configure and consume a dataflow</span></span>](dataflows-configure-consume.md)
* [<span data-ttu-id="30f47-157">การกำหนดค่าที่จัดเก็บกระแสข้อมูลเพื่อใช้ Azure Data Lake Gen 2</span><span class="sxs-lookup"><span data-stu-id="30f47-157">Configuring Dataflow storage to use Azure Data Lake Gen 2</span></span>](dataflows-azure-data-lake-storage-integration.md)
* [<span data-ttu-id="30f47-158">ฟีเจอร์พรีเมียมของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="30f47-158">Premium features of dataflows</span></span>](dataflows-premium-features.md)
* [<span data-ttu-id="30f47-159">AI กับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="30f47-159">AI with dataflows</span></span>](dataflows-machine-learning-integration.md)
* [<span data-ttu-id="30f47-160">แนวทางปฏิบัติที่ดีที่สุดสำหรับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="30f47-160">Dataflows best practices</span></span>](dataflows-best-practices.md)