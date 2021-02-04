---
title: การสร้างกระแสข้อมูล
description: ภาพรวมของตัวเลือกที่แตกต่างกันในการสร้างกระแสข้อมูล
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-dataflows
ms.topic: how-to
ms.date: 10/01/2020
LocalizationGroup: Data from files
ms.openlocfilehash: c98044303e46af46d36b98f0a1bdc8c7df29d94f
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96416174"
---
# <a name="creating-a-dataflow"></a><span data-ttu-id="97528-103">การสร้างกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="97528-103">Creating a dataflow</span></span>
<span data-ttu-id="97528-104">**กระแสข้อมูล** คือคอลเลกชันของเอนทิตี (เอนทิตีนั้นคล้ายกับตาราง) ซึ่งสร้างและจัดการได้ในพื้นที่ทำงานในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="97528-104">A **dataflow** is a collection of entities (entities are similar to tables) that are created and managed in workspaces in the Power BI service.</span></span> <span data-ttu-id="97528-105">**เอนทิตี/ตาราง** คือชุดเขตข้อมูลที่ใช้เพื่อเก็บข้อมูล ซึ่งคล้ายคลึงกับตารางที่อยู่ภายในฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="97528-105">An **entity/Table** is a set of fields that are used to store data, much like a table within a database.</span></span> <span data-ttu-id="97528-106">คุณสามารถเพิ่มและแก้ไขเอนทิตี/ตารางในกระแสข้อมูลได้ และสามารถจัดการกำหนดการรีเฟรชข้อมูลได้โดยตรงจากพื้นที่ทำงานที่ใช้สร้างกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="97528-106">You can add and edit entities/tables in your dataflow, as well as manage data refresh schedules, directly from the workspace in which your dataflow was created.</span></span>

<span data-ttu-id="97528-107">เมื่อต้องการสร้างกระแสข้อมูล ให้เปิดใช้บริการของ Power BI ในเบราว์เซอร์ จากนั้นเลือก **พื้นที่ทำงาน** (กระแสข้อมูลไม่พร้อมใช้งานใน *พื้นที่ทำงานของฉัน* ในบริการของ Power BI) จากบานหน้าต่างด้านซ้าย ดังที่แสดงในหน้าจอต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="97528-107">To create a dataflow, launch the Power BI service in a browser then select a **workspace** (dataflows are not available in *my-workspace* in the Power BI service) from the nav pane on the left, as shown in the following screen.</span></span> <span data-ttu-id="97528-108">คุณยังสามารถสร้างพื้นที่ทำงานใหม่ได้ ซึ่งใช้เพื่อสร้างกระแสข้อมูลชุดใหม่</span><span class="sxs-lookup"><span data-stu-id="97528-108">You can also create a new workspace in which to create your new dataflow.</span></span>
<span data-ttu-id="97528-109">![เริ่มต้นกระแสข้อมูล](media/dataflows-create/create-options.png)</span><span class="sxs-lookup"><span data-stu-id="97528-109">![start a dataflow](media/dataflows-create/create-options.png)</span></span>

<span data-ttu-id="97528-110">มีหลายแนวทางในการสร้างหรือต่อยอดอยู่ด้านบนของกระแสข้อมูลใหม่:</span><span class="sxs-lookup"><span data-stu-id="97528-110">There are a multiple of ways to create or build on top of a new dataflow:</span></span>

* [<span data-ttu-id="97528-111">สร้างกระแสข้อมูลโดยใช้กำหนดเอนทิตีใหม่</span><span class="sxs-lookup"><span data-stu-id="97528-111">Create a dataflow using define new entities</span></span>](#create-a-dataflow-using-define-new-entities)
* [<span data-ttu-id="97528-112">สร้างกระแสข้อมูลโดยใช้เอนทิตีที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="97528-112">Create a dataflow using linked entities</span></span>](#create-a-dataflow-using-linked-entities)
* [<span data-ttu-id="97528-113">สร้างกระแสข้อมูลโดยใช้เอนทิตีที่คำนวณ</span><span class="sxs-lookup"><span data-stu-id="97528-113">Create a dataflow using a computed entity</span></span>](#create-a-dataflow-using-a-computed-entity)
* [<span data-ttu-id="97528-114">สร้างกระแสข้อมูลโดยใช้นำเข้า/ส่งออก</span><span class="sxs-lookup"><span data-stu-id="97528-114">Create a dataflow using import/export</span></span>](#create-a-dataflow-using-importexport)

<span data-ttu-id="97528-115">ส่วนต่อไปนี้จะสำรวจแนวทางในการสร้างกระแสข้อมูลโดยละเอียดสำหรับแต่ละแต่ละวิธี</span><span class="sxs-lookup"><span data-stu-id="97528-115">The following sections explore each of these ways to create a dataflow in detail.</span></span>

## <a name="create-a-dataflow-using-define-new-entities"></a><span data-ttu-id="97528-116">สร้างกระแสข้อมูลโดยใช้กำหนดเอนทิตีใหม่</span><span class="sxs-lookup"><span data-stu-id="97528-116">Create a dataflow using define new entities</span></span>

<span data-ttu-id="97528-117">การใช้ตัวเลือกกำหนดเอนทิตีใหม่ช่วยให้คุณสามารถกำหนดเอนทิตี/ตารางใหม่และเชื่อมต่อไปยังแหล่งข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="97528-117">Using the Define new entities option lets you define a new entity/table and connect to a new data source.</span></span>
<span data-ttu-id="97528-118">[ ![เลือกตัวเชื่อมต่อ](media/dataflows-create/create-connectors.png) ](media/dataflows-create/create-connectors.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="97528-118">[ ![choose a connector](media/dataflows-create/create-connectors.png) ](media/dataflows-create/create-connectors.png#lightbox)</span></span>

<span data-ttu-id="97528-119">เมื่อคุณเลือกแหล่งข้อมูล คุณจะได้รับแจ้งเตือนให้ระบุการตั้งค่าการเชื่อมต่อ ที่รวมถึงบัญชีที่ใช้เมื่อทำการเชื่อมต่อกับแหล่งข้อมูล ดังที่แสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="97528-119">When you select a data source, you're prompted to provide the connection settings, including the account to use when connecting to the data source, as shown in the following image.</span></span>
<span data-ttu-id="97528-120">![ตัวเชื่อมต่อ azure sql](media/dataflows-create/azure-sql-connector.png)</span><span class="sxs-lookup"><span data-stu-id="97528-120">![azure sql connector](media/dataflows-create/azure-sql-connector.png)</span></span>

<span data-ttu-id="97528-121">เมื่อเชื่อมต่อแล้ว คุณสามารถเลือกได้ว่าจะใช้ข้อมูลใดกับเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="97528-121">Once connected, you can select which data to use for your entity.</span></span> <span data-ttu-id="97528-122">เมื่อคุณเลือกข้อมูลและแหล่งข้อมูล Power BI จะเชื่อมต่อกับแหล่งข้อมูลอีกครั้งเพื่อเก็บข้อมูลในการรีเฟรชกระแสข้อมูล ตามความถี่ที่คุณจะได้เลือกในขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="97528-122">When you choose data and a source, Power BI reconnects to the data source in order to keep the data in your dataflow refreshed, at the frequency you select later in the setup process.</span></span>
<span data-ttu-id="97528-123">![เลือกตาราง](media/dataflows-create/choose-table.png)</span><span class="sxs-lookup"><span data-stu-id="97528-123">![select table](media/dataflows-create/choose-table.png)</span></span>

<span data-ttu-id="97528-124">เมื่อคุณเลือกข้อมูลเพื่อใช้กับเอนทิตี คุณสามารถใช้ตัวแก้ไขกระแสข้อมูลเพื่อปรับแต่งหรือแปลงข้อมูลนั้นให้อยู่ในรูปแบบที่ต้องใช้งานในกระแสข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="97528-124">Once you select the data for use in the entity, you can use dataflow editor to shape or transform that data into the format necessary for use in your dataflow.</span></span> 

## <a name="create-a-dataflow-using-linked-entities"></a><span data-ttu-id="97528-125">สร้างกระแสข้อมูลโดยใช้เอนทิตีที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="97528-125">Create a dataflow using linked entities</span></span>

<span data-ttu-id="97528-126">การสร้างกระแสข้อมูลโดยใช้เอนทิตีที่เชื่อมโยงช่วยให้คุณสามารถอ้างอิงเอนทิตีที่มีอยู่ ซึ่งกำหนดไว้ในกระแสข้อมูลอื่นในรูปแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="97528-126">Creating a dataflow using linked entities enables you to reference an existing entity, defined in another dataflow, in a read-only fashion.</span></span> <span data-ttu-id="97528-127">รายการต่อไปนี้อธิบายถึงเหตุผลบางประการที่คุณอาจเลือกวิธีการนี้:</span><span class="sxs-lookup"><span data-stu-id="97528-127">The following list describes some of the reasons you may choose this approach:</span></span>

* <span data-ttu-id="97528-128">ถ้าคุณต้องการใช้เอนทิตีซ้ำในหลายกระแสข้อมูล เช่น เอนทิตีวันที่หรือตารางการค้นหาแบบคงที่ คุณควรสร้างเอนทิตีหนึ่งครั้ง และจากนั้นอ้างอิงกับกระแสข้อมูลอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="97528-128">If you want to reuse an entity across multiple dataflows, such as a date entity or a static lookup table, you should create an entity once and then reference it across the other dataflows.</span></span>

* <span data-ttu-id="97528-129">หากคุณต้องการหลีกเลี่ยงการสร้างการรีเฟรชหลายครั้งในแหล่งข้อมูล คุณควรใช้เอนทิตีที่เชื่อมโยงเพื่อจัดเก็บข้อมูลและทำหน้าที่เป็นแคช</span><span class="sxs-lookup"><span data-stu-id="97528-129">If you want to avoid creating multiple refreshes to a data source, it's better to use linked entities to store the data and act as a cache.</span></span> <span data-ttu-id="97528-130">การดำเนินการดังกล่าวจะช่วยให้ผู้บริโภคที่ตามมาทุกคนสามารถใช้ประโยชน์จากเอนทิตีนั้นได้โดยลดภาระให้กับแหล่งข้อมูลเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="97528-130">Doing so allows every subsequent consumer to leverage that entity, reducing the load to the underlying data source.</span></span>

* <span data-ttu-id="97528-131">ถ้าคุณจำเป็นต้องดำเนินการผสานระหว่างสองเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="97528-131">If you need to perform a merge between two entities.</span></span>

> [!NOTE]
> <span data-ttu-id="97528-132">เอนทิตีที่เชื่อมโยงพร้อมใช้งานเฉพาะกับ Power BI Premium เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="97528-132">Linked entities are available only with Power BI Premium.</span></span>

## <a name="create-a-dataflow-using-a-computed-entity"></a><span data-ttu-id="97528-133">สร้างกระแสข้อมูลโดยใช้เอนทิตีที่คำนวณ</span><span class="sxs-lookup"><span data-stu-id="97528-133">Create a dataflow using a computed entity</span></span>

<span data-ttu-id="97528-134">การสร้างกระแสข้อมูลโดยใช้เอนทิตีที่คำนวณช่วยให้คุณสามารถอ้างอิงเอนทิตีที่เชื่อมโยงและดำเนินการกับด้านบนของเอนทิตีในรูปแบบเขียนอย่างเดียวได้</span><span class="sxs-lookup"><span data-stu-id="97528-134">Creating a dataflow using a computed entity allows you to reference a linked entity and perform operations on top of it in a write-only fashion.</span></span> <span data-ttu-id="97528-135">ผลลัพธ์คือเอนทิตีใหม่ ซึ่งเป็นส่วนหนึ่งของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="97528-135">The result is a new entity, which is part of the dataflow.</span></span> <span data-ttu-id="97528-136">เมื่อต้องการแปลงเอนทิตีที่เชื่อมโยงไปเป็นเอนทิตีที่คำนวณ คุณสามารถสร้างคิวรีใหม่จากการดำเนินการผสานหรือถ้าคุณต้องการ คุณสามารถแก้ไขหรือแปลงเอนทิตีได้ ตลอดจนสร้างการอ้างอิงหรือการทำซ้ำของเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="97528-136">To convert a linked entity into a computed entity, you can either create a new query from a merge operation, or if you want to edit or transform the entity, create a reference or duplicate of the entity.</span></span>

### <a name="how-to-create-computed-entities"></a><span data-ttu-id="97528-137">วิธีการสร้างเอนทิตีที่คำนวณไว้</span><span class="sxs-lookup"><span data-stu-id="97528-137">How to create computed entities</span></span>

<span data-ttu-id="97528-138">เมื่อคุณมีกระแสข้อมูลพร้อมรายการเอนทิตี คุณจะสามารถทำการคำนวณเอนทิตีเหล่านั้นได้</span><span class="sxs-lookup"><span data-stu-id="97528-138">Once you have a dataflow with a list of entities, you can perform calculations on those entities.</span></span>
<span data-ttu-id="97528-139">ที่เครื่องมือการเขียนกระแสข้อมูลในบริการของ Power BI ให้คุณเลือก **แก้ไขเอนทิตี** จากนั้นคลิกขวาที่เอนทิตีที่ต้องการใช้เป็นพื้นฐานสำหรับเอนทิตีที่คำนวณและต้องการทำการคำนวณด้วย</span><span class="sxs-lookup"><span data-stu-id="97528-139">In the dataflow authoring tool in the Power BI service, select **Edit entities**, then right-click on the entity you want to use as the basis for your computed entity and on which you want to perform calculations.</span></span> <span data-ttu-id="97528-140">ในเมนูบริบท ให้คุณเลือก **การอ้างอิง**</span><span class="sxs-lookup"><span data-stu-id="97528-140">In the context menu, choose **Reference**.</span></span>
<span data-ttu-id="97528-141">เพื่อให้สิทธิ์เอนทิตีเป็นเอนทิตีที่คำนวณ ต้องเลือกที่ตัวเลือก **เปิดใช้งานโหลด** ดังที่แสดงในภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="97528-141">For the entity to be eligible as a computed entity, the **Enable load** selection must be checked, as shown in the following image.</span></span> <span data-ttu-id="97528-142">คลิกขวาที่เอนทิตีเพื่อให้แสดงเมนูบริบทนี้</span><span class="sxs-lookup"><span data-stu-id="97528-142">Right-click on the entity to display this context menu.</span></span>

![สร้างเอนทิตีที่คำนวณขั้นตอนที่ 1](media/dataflows-create/computed-entity-step-1.png)

<span data-ttu-id="97528-144">เมื่อเลือก **เปิดใช้งานโหลด** แล้ว คุณจะสามารถสร้างเอนทิตีใหม่ได้ ซึ่งต้นทางของมันก็คือเอนทิตีที่อ้างอิงถึง</span><span class="sxs-lookup"><span data-stu-id="97528-144">By selecting **Enable load**, you create a new entity for which its source is the referenced entity.</span></span> <span data-ttu-id="97528-145">ไอคอนจะเปลี่ยนและแสดงไอคอน **ที่คำนวณไว้** ดังที่แสดงในภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="97528-145">The icon changes, and shows the **computed** icon, as shown in the following image.</span></span>

![สร้างเอนทิตีที่คำนวณขั้นตอนที่ 2](media/dataflows-create/computed-entity-step-2.png)

<span data-ttu-id="97528-147">การแปลงข้อมูลใดก็ตามที่คุณดำเนินการในเอนทิตีที่สร้างใหม่นี้ จะถูกเรียกใช้ในข้อมูลที่อยู่ในที่จัดเก็บกระแสข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="97528-147">Any transformation you perform on this newly created entity is run on the data that already resides in Power BI dataflow storage.</span></span> <span data-ttu-id="97528-148">ซึ่งหมายความว่าคิวรีนั้นไม่ได้เรียกใช้กับแหล่งข้อมูลภายนอกที่มีการนำเข้าข้อมูลมา (เช่น ฐานข้อมูล SQL ที่มีการดึงข้อมูลมา) แต่มีการดำเนินการกับข้อมูลที่อยู่ในที่เก็บกระแสข้อมูลอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="97528-148">That means that the query will not run against the external data source from which the data was imported (for example, the SQL database from which the data was pulled), but rather, is performed on the data that resides in the dataflow storage.</span></span>

<span data-ttu-id="97528-149">**ตัวอย่างกรณีการใช้งาน** การแปลงชนิดใดที่สามารถดำเนินการกับเอนทิตีที่คำนวณได้</span><span class="sxs-lookup"><span data-stu-id="97528-149">**Example use cases** What kind of transformations can be performed with computed entities?</span></span> <span data-ttu-id="97528-150">การแปลงใดก็ตามที่คุณมักจะระบุถึงโดยใช้อินเตอร์เฟสผู้ใช้ของการแปลงใน Power BI หรือ M Editor จะได้รับการรองรับเมื่อทำการคำนวณในที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="97528-150">Any transformation that you usually specify using the transformation user interface in Power BI, or the M editor, are all supported when performing in-storage computation.</span></span>

<span data-ttu-id="97528-151">โปรดพิจารณาตัวเลือกต่อไปนี้: คุณมีเอนทิตี *บัญชี* ที่มีข้อมูลดิบสำหรับลูกค้าทั้งหมดจากการสมัครใช้งาน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="97528-151">Consider the following example: you have an *Account* entity that contains the raw data for all the customers from your Dynamics 365 subscription.</span></span> <span data-ttu-id="97528-152">นอกจากนี้คุณยังมีข้อมูลดิบของ *ServiceCalls* จากศูนย์บริการ โดยที่มีข้อมูลจากการโทรศัพท์สนับสนุนที่ทำจากบัญชีอื่นในแต่ละวันของทั้งปี</span><span class="sxs-lookup"><span data-stu-id="97528-152">You also have *ServiceCalls* raw data from the Service Center, with data from the support calls that were performed from the different account in each day of the year.</span></span>

<span data-ttu-id="97528-153">ลองนึกดูว่าคุณต้องการเพิ่มข้อมูลจาก *ServiceCalls* ในเอนทิตี *บัญชี*</span><span class="sxs-lookup"><span data-stu-id="97528-153">Imagine you want to enrich the *Account* entity with data from the *ServiceCalls*.</span></span>
<span data-ttu-id="97528-154">ก่อนอื่นคุณต้องรวบรวมข้อมูลจาก *ServiceCalls* เพื่อคำนวณจำนวนของการโทรศัพท์สนับสนุนในปีก่อนที่ทำให้แต่ละบัญชี</span><span class="sxs-lookup"><span data-stu-id="97528-154">First you would need to aggregate the data from the *ServiceCalls* to calculate the number of support calls that were done for each account in the last year.</span></span>

![สร้างเอนทิตีที่คำนวณขั้นตอนที่ 3](media/dataflows-create/computed-entity-step-3.png)

<span data-ttu-id="97528-156">จากนั้น คุณต้องผสานเอนทิตี *บัญชี* กับเอนทิตี *ServiceCallsAggregated* เพื่อคำนวณตาราง *บัญชี* ที่เพิ่มข้อมูล</span><span class="sxs-lookup"><span data-stu-id="97528-156">Next, you would want to merge the *Account* entity with the *ServiceCallsAggregated* entity to calculate the enriched *Account* table.</span></span>

![สร้างเอนทิตีที่คำนวณขั้นตอนที่ 4](media/dataflows-create/computed-entity-step-4.png)

<span data-ttu-id="97528-158">และจากนั้นคุณจะเห็นผลลัพธ์ ดังที่แสดง *EnrichedAccount* ในภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="97528-158">And then you can see the results, shown as *EnrichedAccount* in the following image.</span></span>

![สร้างเอนทิตีที่คำนวณขั้นตอนที่ 5](media/dataflows-create/computed-entity-step-5.png)

<span data-ttu-id="97528-160">เท่านั้นเอง การแปลงได้ดำเนินการกับข้อมูลในกระแสข้อมูลที่อยู่ในการสมัครใช้งาน Power BI Premium ไม่ใช่กับข้อมูลต้นทาง</span><span class="sxs-lookup"><span data-stu-id="97528-160">And that's it - the transformation is performed on the data in the dataflow that resides in your Power BI Premium subscription, not on the source data.</span></span>

> [!NOTE]
> <span data-ttu-id="97528-161">เอนทิตีที่คำนวณเป็นคุณลักษณะ premium เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="97528-161">Computed entities are a premium only feature</span></span>

## <a name="create-a-dataflow-using-a-cdm-folder"></a><span data-ttu-id="97528-162">สร้างกระแสข้อมูลโดยใช้โฟลเดอร์ CDM</span><span class="sxs-lookup"><span data-stu-id="97528-162">Create a dataflow using a CDM folder</span></span>

<span data-ttu-id="97528-163">การสร้างกระแสข้อมูลจากโฟลเดอร์ CDM ช่วยให้คุณสามารถอ้างอิงเอนทิตีที่เขียนโดยแอปพลิเคชันอื่นในรูปแบบ Common Data Model (CDM)</span><span class="sxs-lookup"><span data-stu-id="97528-163">Creating a dataflow from a CDM folder allows you to reference an entity that has been written by another application in the Common Data Model (CDM) format.</span></span> <span data-ttu-id="97528-164">คุณได้รับพร้อมท์ให้กำหนดเส้นทางที่สมบูรณ์ไปยังไฟล์รูปแบบ CDM ที่จัดเก็บไว้ใน ADLS Gen 2</span><span class="sxs-lookup"><span data-stu-id="97528-164">You are prompted to provide the complete path to the CDM format file stored in ADLS Gen 2.</span></span>

 ![สร้างเอนทิตีที่คำนวณขั้นตอนที่ 6](media/dataflows-create/attach-cdm.jpg)

<span data-ttu-id="97528-166">มีข้อกำหนดสองสามข้อสำหรับการสร้างกระแสข้อมูลจากโฟลเดอร์ CDM ตามรายการที่อธิบายต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="97528-166">There are a few requirements for creating dataflows from CDM folders, as the following list describes:</span></span>

* <span data-ttu-id="97528-167">บัญชี ADLS Gen 2 ต้องมีการตั้งค่าสิทธิ์ที่เหมาะสมเพื่อให้ PBI เข้าถึงไฟล์ได้</span><span class="sxs-lookup"><span data-stu-id="97528-167">The ADLS Gen 2 account must have the appropriate permissions set up in order for PBI to access the file</span></span>

* <span data-ttu-id="97528-168">บัญชี ADLS Gen 2 ต้องสามารถเข้าถึงได้โดยผู้ใช้ที่พยายามสร้างกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="97528-168">The ADLS Gen 2 account must be accessible by the user trying to create the dataflow</span></span>

* <span data-ttu-id="97528-169">การสร้างกระแสข้อมูลจากโฟลเดอร์ CDM สามารถใช้งานได้ในพื้นที่ทำงานใหม่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="97528-169">Creating dataflows from CDM folders is only available in the new workspace experience</span></span>

* <span data-ttu-id="97528-170">URL ต้องเป็นเส้นทางไฟล์ทางตรงไปยังไฟล์ JSON และใช้จุดสิ้นสุด ADLS Gen 2 ซึ่งไม่รองรับ blob.core</span><span class="sxs-lookup"><span data-stu-id="97528-170">The URL must be a direct file path to the JSON file and use the ADLS Gen 2 endpoint; blob.core is not supported</span></span>

## <a name="create-a-dataflow-using-importexport"></a><span data-ttu-id="97528-171">สร้างกระแสข้อมูลโดยใช้นำเข้า/ส่งออก</span><span class="sxs-lookup"><span data-stu-id="97528-171">Create a dataflow using import/export</span></span>

<span data-ttu-id="97528-172">การสร้างกระแสข้อมูลโดยใช้นำเข้า/ส่งออกช่วยให้คุณนำเข้ากระแสข้อมูลจากไฟล์</span><span class="sxs-lookup"><span data-stu-id="97528-172">Creating a dataflow using import/export lets you import a dataflow from a file.</span></span> <span data-ttu-id="97528-173">การดำเนินการนี้จะเป็นประโยชน์ถ้าคุณต้องการบันทึกสำเนากระแสข้อมูลแบบออฟไลน์ หรือย้ายกระแสข้อมูลจากพื้นที่ทำงานหนึ่งไปยังอีกพื้นที่ทำงานหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="97528-173">This is useful if you want to save a dataflow copy offline, or move a dataflow from one workspace to another.</span></span> 

<span data-ttu-id="97528-174">เมื่อต้องการส่งออกกระแสข้อมูล ให้เลือกกระแสข้อมูลที่คุณสร้างขึ้นและเลือกรายการเมนู **เพิ่มเติม** (จุดไข่ปลา) เพื่อขยายตัวเลือกจากนั้นเลือก **ส่งออก .json**</span><span class="sxs-lookup"><span data-stu-id="97528-174">To export a dataflow, select the dataflow you created and select the **More** menu item (the ellipsis) to expand the options, and then select **export .json**.</span></span> <span data-ttu-id="97528-175">คุณได้รับพร้อมท์ให้เริ่มการดาวน์โหลดกระแสข้อมูลที่แสดงในรูปแบบ CDM</span><span class="sxs-lookup"><span data-stu-id="97528-175">You are prompted to begin the download of the dataflow represented in CDM format.</span></span>

![สร้างเอนทิตีที่คำนวณขั้นตอนที่ 7](media/dataflows-create/export-dataflow.png)

<span data-ttu-id="97528-177">หากต้องการนำเข้ากระแสข้อมูล ให้เลือกกล่องนำเข้าและอัปโหลดไฟล์</span><span class="sxs-lookup"><span data-stu-id="97528-177">To import a dataflow, select the import box and upload the file.</span></span> <span data-ttu-id="97528-178">Power BI สร้างกระแสข้อมูลสำหรับคุณและอนุญาตให้คุณบันทึกกระแสข้อมูลตามที่เป็นอยู่หรือเพื่อทำการแปลงเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="97528-178">Power BI creates the dataflow for you, and allows you to save the dataflow as is, or to perform additional transformations.</span></span>

## <a name="next-steps"></a><span data-ttu-id="97528-179">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="97528-179">Next steps</span></span>

<span data-ttu-id="97528-180">เมื่อคุณสร้างกระแสข้อมูล คุณอาจใช้ Power BI Desktop และ บริการของ Power BI เพื่อสร้างชุดข้อมูล รายงาน แดชบอร์ด และแอปที่ใช้ข้อมูลที่คุณป้อนเข้ากระแสข้อมูลของ Power BI ซึ่งจะช่วยให้คุณได้ข้อมูลเชิงลึกในกิจกรรมธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="97528-180">Once you create a dataflow, you can use Power BI Desktop and the Power BI service to create datasets, reports, dashboards, and apps that are based on the data you put into Power BI dataflows, and thereby gain insights into your business activities.</span></span> <span data-ttu-id="97528-181">บทความต่อไปนี้จะลงรายละเอียดที่ลึกขึ้นเกี่ยวกับสถานการณ์การใช้งานทั่วไปสำหรับกระแสข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="97528-181">The following articles go into more detail about common usage scenarios for dataflows:</span></span>

* [<span data-ttu-id="97528-182">ข้อมูลเบื้องต้นเกี่ยวกับกระแสข้อมูลและการเตรียมข้อมูลด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="97528-182">Introduction to dataflows and self-service data prep</span></span>](dataflows-introduction-self-service.md)
* [<span data-ttu-id="97528-183">กำหนดค่าและใช้กระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="97528-183">Configure and consume a dataflow</span></span>](dataflows-configure-consume.md)
* [<span data-ttu-id="97528-184">การกำหนดค่าที่จัดเก็บกระแสข้อมูลเพื่อใช้ Azure Data Lake Gen 2</span><span class="sxs-lookup"><span data-stu-id="97528-184">Configuring Dataflow storage to use Azure Data Lake Gen 2</span></span>](dataflows-azure-data-lake-storage-integration.md)
* [<span data-ttu-id="97528-185">ฟีเจอร์พรีเมียมของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="97528-185">Premium features of dataflows</span></span>](dataflows-premium-features.md)
* [<span data-ttu-id="97528-186">AI กับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="97528-186">AI with dataflows</span></span>](dataflows-machine-learning-integration.md)
* [<span data-ttu-id="97528-187">ข้อจำกัดและข้อควรพิจารณาของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="97528-187">Dataflows limitations and considerations</span></span>](dataflows-features-limitations.md)
* [<span data-ttu-id="97528-188">แนวทางปฏิบัติที่ดีที่สุดสำหรับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="97528-188">Dataflows best practices</span></span>](dataflows-best-practices.md)