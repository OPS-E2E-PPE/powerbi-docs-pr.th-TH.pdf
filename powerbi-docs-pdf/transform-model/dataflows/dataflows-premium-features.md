---
title: ฟีเจอร์พรีเมียมของกระแสข้อมูล
description: ภาพรวมของคุณลักษณะ Premium ที่พร้อมใช้งานกับกระแสข้อมูล Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-dataflows
ms.topic: how-to
ms.date: 11/13/2020
LocalizationGroup: Data from files
ms.openlocfilehash: 2c8a5646f4831c77ac0f8fabed0d74f2a2cfba1f
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414081"
---
# <a name="premium-features-of-dataflows"></a><span data-ttu-id="d4a76-103">ฟีเจอร์พรีเมียมของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4a76-103">Premium features of dataflows</span></span>

<span data-ttu-id="d4a76-104">มีการสนับสนุนกระแสข้อมูลสำหรับผู้ใช้ Power BI Pro และ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="d4a76-104">Dataflows are supported for Power BI Pro and Power BI Premium users.</span></span> <span data-ttu-id="d4a76-105">คุณลักษณะบางอย่างสามารถใช้ได้กับการสมัครใช้งาน Power BI Premium เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d4a76-105">Some features are only available with a Power BI Premium subscription.</span></span> <span data-ttu-id="d4a76-106">บทความนี้อธิบายและแสดงรายละเอียดคุณลักษณะเฉพาะ Premium และการใช้งานของคุณลักษณะดังกล่าวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d4a76-106">This article describes and details the Premium-only features and their uses.</span></span> 

<span data-ttu-id="d4a76-107">คุณลักษณะต่อไปนี้พร้อมใช้งานกับ Power BI Premium เท่านั้น:</span><span class="sxs-lookup"><span data-stu-id="d4a76-107">The following features are available only with Power BI Premium:</span></span>

* <span data-ttu-id="d4a76-108">กลไกการคำนวณขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="d4a76-108">Enhanced compute engine</span></span>
* <span data-ttu-id="d4a76-109">Direct Query</span><span class="sxs-lookup"><span data-stu-id="d4a76-109">Direct Query</span></span>
* <span data-ttu-id="d4a76-110">เอนทิตีที่คำนวณ</span><span class="sxs-lookup"><span data-stu-id="d4a76-110">Computed entities</span></span>
* <span data-ttu-id="d4a76-111">เอนทิตีที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="d4a76-111">Linked Entities</span></span>
* <span data-ttu-id="d4a76-112">การรีเฟรชแบบเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="d4a76-112">Incremental refresh</span></span>

<span data-ttu-id="d4a76-113">ส่วนต่อไปนี้อธิบายคุณลักษณะแต่ละอย่างโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="d4a76-113">The following sections described each of these features in detail.</span></span>

## <a name="the-enhanced-compute-engine"></a><span data-ttu-id="d4a76-114">กลไกการคำนวณขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="d4a76-114">The enhanced compute engine</span></span>

<span data-ttu-id="d4a76-115">กลไกการคำนวณขั้นสูงใน Power BI ช่วยให้ผู้สมัครใช้งาน Power BI Premium สามารถใช้ความจุของพวกเขาเพื่อปรับใช้กระแสข้อมูลในระดับประสิทธิภาพสูงสุด</span><span class="sxs-lookup"><span data-stu-id="d4a76-115">The enhanced compute engine in Power BI enables Power BI Premium subscribers to use their capacity to optimize the use of dataflows.</span></span> <span data-ttu-id="d4a76-116">การใช้กลไกการคำนวณขั้นสูงมีข้อดีดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d4a76-116">Using the enhanced compute engine provides the following advantages:</span></span>

* <span data-ttu-id="d4a76-117">ลดเวลาการรีเฟรชที่จำเป็นสำหรับขั้นตอน ETL ที่ใช้งานเป็นเวลานานผ่านเอนทิตีที่มีการคำนวณลงได้อย่างมาก เช่น การดำเนินการ *รวม* *แยกแยะ* *กรอง* และ *จัดกลุ่มตาม*</span><span class="sxs-lookup"><span data-stu-id="d4a76-117">Drastically reduces the refresh time required for long-running ETL steps over computed entities, such as performing *joins*, *distinct*, *filters,* and *group by*</span></span>
* <span data-ttu-id="d4a76-118">ดำเนินการคิวรี DirectQuery ผ่านเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="d4a76-118">Perform DirectQuery queries over entities</span></span>

<span data-ttu-id="d4a76-119">โดยค่าเริ่มต้น กลไกการคำนวณขั้นสูงจะ **เปิด**</span><span class="sxs-lookup"><span data-stu-id="d4a76-119">By default, the enhanced compute engine is **On**.</span></span> <span data-ttu-id="d4a76-120">หากกลไกการคำนวณขั้นสูงไม่ได้เปิดอยู่ การเปิดใช้งานกลไกการคำนวณขั้นสูงจะอธิบายไว้ในส่วนถัดไปพร้อมกับคำตอบสำหรับคำถามทั่วไป</span><span class="sxs-lookup"><span data-stu-id="d4a76-120">If the enhanced compute engine is not on, enabling the enhanced compute engine is described in the next section, along with answers to common questions.</span></span>

### <a name="using-the-enhanced-compute-engine"></a><span data-ttu-id="d4a76-121">การใช้กลไกการคำนวณขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="d4a76-121">Using the enhanced compute engine</span></span>

<span data-ttu-id="d4a76-122">กลไกการคำนวณขั้นสูงเปิดใช้งานจากหน้า **การตั้งค่าความจุ** ในบริการของ Power BI ในส่วน **กระแสข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="d4a76-122">The enhanced compute engine is enabled from the **Capacity Settings** page in the Power BI service, in the **dataflows** section.</span></span> <span data-ttu-id="d4a76-123">โดยค่าเริ่มต้น กลไกการคำนวณขั้นสูงจะ **ปิด**</span><span class="sxs-lookup"><span data-stu-id="d4a76-123">By default, the enhanced compute engine is **Off**.</span></span> <span data-ttu-id="d4a76-124">เมื่อต้องการเปิดใช้งานกลไกการคำนวณขั้นสูง ให้สลับเป็น **เปิด** ดังที่แสดงในภาพต่อไปนี้ แล้วบันทึกการตั้งค่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="d4a76-124">To enable the enhanced compute engine, switch the toggle to **On** as shown in the following image, and save your settings.</span></span> 

![เปิดกลไกการคำนวณขั้นสูง](media/dataflows-premium-features/compute-engine-settings.png)

> [!IMPORTANT]
> <span data-ttu-id="d4a76-126">กลไกการคำนวณขั้นสูงทำงานเฉพาะสำหรับความจุ Power BI ของ A3 และใหญ่กว่า</span><span class="sxs-lookup"><span data-stu-id="d4a76-126">The enhanced compute engine works only for Power BI capacities of A3 and larger.</span></span>

<span data-ttu-id="d4a76-127">เมื่อเปิดกลไกการคำนวณขั้นสูงแล้ว ให้กลับไปที่ **กระแสข้อมูล** คุณควรจะมองเห็นการปรับปรุงประสิทธิภาพที่ดีขึ้นในเอนทิตีที่คำนวณใดก็ตามซึ่งทำงานที่ซับซ้อนต่าง ๆ เช่น *รวม* หรือ *จัดกลุ่มตาม* การดำเนินการสำหรับกระแสข้อมูลที่สร้างจากเอนทิตีที่ลิงก์ซึ่งมีอยู่แล้วบนความจุเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="d4a76-127">Once the enhanced compute engine is on, return to **dataflows** and you should see a performance improvement in any computed entity that performs complex operations, such as *joins* or *group by* operations for dataflows created from existing linked entities on the same capacity.</span></span> 

<span data-ttu-id="d4a76-128">เพื่อใช้กลไกการคำนวณให้ได้รับประโยชน์สูงสุด ให้แยกขั้นตอน ETL ออกเป็นกระแสข้อมูลที่แยกจากกันสองรายการด้วยวิธีการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d4a76-128">To make best use of the compute engine, split the ETL stage into two separate dataflows, in the following way:</span></span>

* <span data-ttu-id="d4a76-129">**กระแสข้อมูล 1** - กระแสข้อมูลนี้ควรส่งถ่ายรายการที่จำเป็นทั้งหมดจากแหล่งข้อมูล และวางลงในกระแสข้อมูล 2</span><span class="sxs-lookup"><span data-stu-id="d4a76-129">**Dataflow 1** - this dataflow should only be ingesting all of the required from a data source, and placing it into dataflow 2.</span></span>
* <span data-ttu-id="d4a76-130">**กระแสข้อมูล 2** - ดำเนินการ ETL ทั้งหมดในกระแสข้อมูลที่สองนี้ แต่ตรวจสอบให้แน่ใจว่าคุณกำลังอ้างอิงกระแสข้อมูล 1 ที่ควรมีความจุเดียวกันอยู่</span><span class="sxs-lookup"><span data-stu-id="d4a76-130">**Dataflow 2** - perform all ETL operations in this second dataflow, but ensure you're referencing Dataflow 1, which should be on the same capacity.</span></span> <span data-ttu-id="d4a76-131">นอกจากนี้ ตรวจสอบให้แน่ใจว่าคุณดำเนินงานที่สามารถพับได้ก่อน (กรอง, จัดกลุ่มตาม, แยกแยะ, รวม) ก่อนที่จะดำเนินการอืนใด เพื่อให้แน่ใจว่าสามารถใช้ประโยชน์จากกลไกการคำนวณได้</span><span class="sxs-lookup"><span data-stu-id="d4a76-131">Also ensure you perform operations that can fold (filter, group by, distinct, join) first, before any other operation, to ensure the compute engine is utilized.</span></span>

### <a name="common-questions-and-answers"></a><span data-ttu-id="d4a76-132">คำถามที่พบทั่วไปและคำตอบ</span><span class="sxs-lookup"><span data-stu-id="d4a76-132">Common questions and answers</span></span>

<span data-ttu-id="d4a76-133">**คำถาม:** ฉันเปิดใช้กลไกการคำนวณขั้นสูง แต่ระบบรีเฟรชช้าลง</span><span class="sxs-lookup"><span data-stu-id="d4a76-133">**Question:** I've enabled the enhanced compute engine, but my refreshes are slower.</span></span> <span data-ttu-id="d4a76-134">ทำไม?</span><span class="sxs-lookup"><span data-stu-id="d4a76-134">Why?</span></span>

<span data-ttu-id="d4a76-135">**คำตอบ:** หากคุณเปิดใช้กลไกการคำนวณขั้นสูง มีคำอธิบายสองแบบที่เป็นไปได้ ที่อาจทำให้เวลารีเฟรชช้าลง:</span><span class="sxs-lookup"><span data-stu-id="d4a76-135">**Answer:** If you enable the enhanced compute engine, there are two possible explanations that could lead to slower refresh times:</span></span>

 * <span data-ttu-id="d4a76-136">เมื่อเปิดใช้กลไกการคำนวณขั้นสูง ระบบต้องการหน่วยความจำบางส่วนเพื่อทำงานได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="d4a76-136">When the enhanced compute engine is enabled, it requires some memory to function properly.</span></span> <span data-ttu-id="d4a76-137">ดังนั้น หน่วยความจำที่พร้อมสำหรับการรีเฟรชจะลดลง และจะเพิ่มความเป็นไปได้เช่นเดียวกันนี้ต่อรายการรีเฟรชที่รอต่อคิวดำเนินการอยู่ ซึ่งจะลดกระแสข้อมูลที่อาจรีเฟรชอยู่ในเวลาเดียวกันเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="d4a76-137">As such, memory available to perform a refresh is reduced and therefore increases the likelihood of refreshes to be queued, which in turn reduces the number of dataflows that can refresh concurrently.</span></span> <span data-ttu-id="d4a76-138">เพื่อแก้ไขปัญหานี้ เมื่อเปิดใช้การคำนวณขั้นสูง ให้เพิ่มหน่วยความจำที่กำหนดมาสำหรับกระแสข้อมูล เพื่อให้แน่ใจว่าหน่วยข้อมูลที่พร้อมใช้งานสำหรับการรีเฟรชกระแสข้อมูลในเวลาเดียวกันจะยังคงเหมือนเดิม</span><span class="sxs-lookup"><span data-stu-id="d4a76-138">To address this, when enabling enhanced compute, increase the memory assigned for dataflows to ensure the memory available for concurrent dataflow refreshes remains the same.</span></span>

 * <span data-ttu-id="d4a76-139">อีกเหตุผลหนึ่งที่คุณอาจพบการรีเฟรชช้าลงคือว่ากลไกการคำนวณจะทำงานที่ด้านบนของเอนทิตีที่มีอยู่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d4a76-139">Another reason you may encounter slower refreshes is that the compute engine only works on top of existing entities.</span></span> <span data-ttu-id="d4a76-140">ถ้ากระแสข้อมูลของคุณอ้างอิงแหล่งข้อมูลที่ไม่ใช่กระแสข้อมูล คุณจะไม่เห็นการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="d4a76-140">If your dataflow references a data source that's not a dataflow, you won't see an improvement.</span></span> <span data-ttu-id="d4a76-141">ประสิทธิภาพการทำงานจะไม่เพี่มขึ้น เนื่องจากในสถานการณ์สมมติครั้งใหญ่บางอย่าง ค่าเริ่มต้นจากแหล่งข้อมูลจะช้าลง เนื่องจากข้อมูลจำเป็นต้องผ่านไปยังกลไกการคำนวณขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="d4a76-141">There will be no performance increase, since in some big data scenarios, the initial read from a data source would be slower because the data needs to be passed to the enhanced compute engine.</span></span>  

<span data-ttu-id="d4a76-142">**คำถาม:** ฉันไม่เห็นการสลับกลไกการคำนวณขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="d4a76-142">**Question:** I cannot see the enhanced compute engine toggle.</span></span> <span data-ttu-id="d4a76-143">ทำไม?</span><span class="sxs-lookup"><span data-stu-id="d4a76-143">Why?</span></span>

<span data-ttu-id="d4a76-144">**คำตอบ:** กลไกการคำนวณขั้นสูงถูกปล่อยออกมาในขั้นตอนต่างๆ ไปยังภูมิภาคต่าง ๆ ทั่วโลก</span><span class="sxs-lookup"><span data-stu-id="d4a76-144">**Answer:** The enhanced compute engine is being released in stages to regions around the world.</span></span> <span data-ttu-id="d4a76-145">เราคาดการณ์ว่า ระบบจะรองรับในทุกภูมิภาคภายในสิ้นปีค.ศ.2020</span><span class="sxs-lookup"><span data-stu-id="d4a76-145">We anticipate all regions will supported by the end of 2020.</span></span>

<span data-ttu-id="d4a76-146">**คำถาม:** ประเภทข้อมูลที่ได้รับการสนับสนุนสำหรับกลไกการคำนวณคืออะไร</span><span class="sxs-lookup"><span data-stu-id="d4a76-146">**Question:** What are the supported data types for the compute engine?</span></span>

<span data-ttu-id="d4a76-147">**คำตอบ:** ปัจจุบัน กลไกการคำนวณขั้นสูงและกระแสข้อมูลสนับสนุนประเภทข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d4a76-147">**Answer:** The enhanced compute engine and dataflows currently support the following data types.</span></span> <span data-ttu-id="d4a76-148">หากกระแสข้อมูลของคุณไม่ได้ใช้หนึ่งในประเภทข้อมูลต่อไปนี้ จะมีข้อผิดพลาดเกิดขึ้นระหว่างการรีเฟรช:</span><span class="sxs-lookup"><span data-stu-id="d4a76-148">If your dataflow doesn't use one of the following data types, an error occurs during refresh:</span></span>

* <span data-ttu-id="d4a76-149">วันที่/เวลา</span><span class="sxs-lookup"><span data-stu-id="d4a76-149">Date/Time</span></span>
* <span data-ttu-id="d4a76-150">เลขทศนิยม</span><span class="sxs-lookup"><span data-stu-id="d4a76-150">Decimal Number</span></span>
* <span data-ttu-id="d4a76-151">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="d4a76-151">Text</span></span>
* <span data-ttu-id="d4a76-152">จำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="d4a76-152">Whole number</span></span>
* <span data-ttu-id="d4a76-153">วันที่/เวลา/โซน</span><span class="sxs-lookup"><span data-stu-id="d4a76-153">Date/Time/Zone</span></span>
* <span data-ttu-id="d4a76-154">จริง/เท็จ</span><span class="sxs-lookup"><span data-stu-id="d4a76-154">True/False</span></span>
* <span data-ttu-id="d4a76-155">วันที่</span><span class="sxs-lookup"><span data-stu-id="d4a76-155">Date</span></span>
* <span data-ttu-id="d4a76-156">เวลา</span><span class="sxs-lookup"><span data-stu-id="d4a76-156">Time</span></span>

## <a name="use-directquery-with-dataflows-in-power-bi-preview"></a><span data-ttu-id="d4a76-157">ใช้ DirectQuery ด้วยกระแสข้อมูลใน Power BI (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="d4a76-157">Use DirectQuery with dataflows in Power BI (preview)</span></span>

<span data-ttu-id="d4a76-158">คุณสามารถใช้ DirectQuery เพื่อเชื่อมต่อโดยตรงไปยังกระแสข้อมูล และเชื่อมต่อโดยตรงกับกระแสข้อมูลของคุณโดยไม่ต้องนำเข้าข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4a76-158">You can use DirectQuery to connect directly to dataflows, and thereby connect directly to your dataflow without having to import its data.</span></span> 

<span data-ttu-id="d4a76-159">การใช้ DirectQuery กับกระแสข้อมูลช่วยให้สามารถปรับปรุงขั้นตอนต่อไปนี้ในกระบวนการ Power BI และกระแสข้อมูลของคุณได้เช่น:</span><span class="sxs-lookup"><span data-stu-id="d4a76-159">Using DirectQuery with dataflows enables the following enhancements to your Power BI and dataflows processes:</span></span>

* <span data-ttu-id="d4a76-160">**หลีกเลี่ยงการกำหนดตารางเวลาการรีเฟรชแยกต่างหาก**-DirectQuery เชื่อมต่อโดยตรงกับกระแสข้อมูลโดยไม่จำเป็นต้องสร้างชุดข้อมูลที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="d4a76-160">**Avoid separate refresh schedules** - DirectQuery connects directly to a dataflow, removing the need to create an imported dataset.</span></span> <span data-ttu-id="d4a76-161">เช่นเดียวกับการใช้ DirectQuery ด้วยกระแสข้อมูลของคุณหมายความว่าคุณไม่จำเป็นต้องกำหนดตารางเวลาการรีเฟรชแยกต่างหากสำหรับกระแสข้อมูลและชุดข้อมูล เพื่อให้แน่ใจว่าข้อมูลของคุณจะถูกซิงโครไนซ์</span><span class="sxs-lookup"><span data-stu-id="d4a76-161">As such, using DirectQuery with your dataflows means you no longer need separate refresh schedules for the dataflow and the dataset to ensure your data is synchronized.</span></span>

* <span data-ttu-id="d4a76-162">**การกรองข้อมูล**- DirectQuery มีประโยชน์สำหรับการทำงานบนมุมมองที่กรองแล้วของข้อมูลภายในกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4a76-162">**Filtering data** - DirectQuery is useful for working on a filtered view of data inside a dataflow.</span></span> <span data-ttu-id="d4a76-163">ถ้าคุณต้องการกรองข้อมูลและทำงานกับชุดย่อยของข้อมูลที่มีขนาดเล็กลงในกระแสข้อมูลของคุณ คุณสามารถใช้ DirectQuery (และโปรแกรมคำนวณ) เพื่อกรองข้อมูลของกระแสข้อมูล และทำงานกับชุดย่อยที่กรองแล้วที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="d4a76-163">If you want to filter data, and thereby work with a smaller subset of the data in your dataflow, you can use DirectQuery (and the compute engine) to filter dataflow data and work with the filtered subset you need.</span></span>


### <a name="using-directquery-for-dataflows"></a><span data-ttu-id="d4a76-164">การใช้ DirectQuery สำหรับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4a76-164">Using DirectQuery for dataflows</span></span>

<span data-ttu-id="d4a76-165">การใช้ DirectQuery ด้วยกระแสข้อมูลคือคุณลักษณะตัวอย่างที่พร้อมใช้งานเริ่มตั้งแต่ Power BI Desktop รุ่นเดือนพฤษภาคม 2020</span><span class="sxs-lookup"><span data-stu-id="d4a76-165">Using DirectQuery with dataflows is a preview feature available beginning with the May 2020 version of Power BI Desktop.</span></span> 

<span data-ttu-id="d4a76-166">นอกจากนี้ ยังมีข้อกำหนดเบื้องต้นสำหรับการใช้ DirectQuery กับกระแสข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="d4a76-166">There are also prerequisites for using DirectQuery with dataflows:</span></span>

* <span data-ttu-id="d4a76-167">กระแสข้อมูลของคุณต้องอยู่ภายในพื้นที่ทำงานที่เปิดใช้ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="d4a76-167">Your dataflow must reside within a Power BI Premium enabled workspace</span></span>
* <span data-ttu-id="d4a76-168">ต้องเปิดใช้งาน **กลไกการคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="d4a76-168">The **compute engine** must be turned on</span></span>

### <a name="enable-directquery-for-dataflows"></a><span data-ttu-id="d4a76-169">เปิดใช้งาน DirectQuery สำหรับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4a76-169">Enable DirectQuery for dataflows</span></span>

<span data-ttu-id="d4a76-170">เพื่อให้แน่ใจว่ากระแสข้อมูลของคุณพร้อมใช้งานสำหรับการเข้าถึง DirectQuery โปรแกรมการคำนวณขั้นสูงจะต้องอยู่ในสถานะที่ปรับให้เหมาะสมแล้ว</span><span class="sxs-lookup"><span data-stu-id="d4a76-170">To ensure your dataflow is available for DirectQuery access, the enhanced compute engine must be in its optimized state.</span></span> <span data-ttu-id="d4a76-171">เมื่อต้องการเปิดใช้งาน DirectQuery สำหรับกระแสข้อมูล ให้ตั้งค่าตัวเลือก **การตั้งค่าโปรแกรมการคำนวณขั้นสูง** ใหม่เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="d4a76-171">To enable DirectQuery for dataflows, set the new **Enhanced compute engine settings** option to **On**.</span></span> <span data-ttu-id="d4a76-172">รูปภาพต่อไปนี้แสดงการตั้งค่าที่เลือกอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="d4a76-172">The following image shows the setting properly selected.</span></span>

![การควบคุมแยกย่อยสำหรับ Direct Query](media/dataflows-premium-features/compute-engine-granular-control.png)

<span data-ttu-id="d4a76-174">เมื่อคุณใช้การตั้งค่าดังกล่าว ให้รีเฟรชกระแสข้อมูลเพื่อทำให้การปรับให้เหมาะสมมีผล</span><span class="sxs-lookup"><span data-stu-id="d4a76-174">Once you've applied that setting, refresh the dataflow for the optimization to take effect.</span></span>

### <a name="considerations-and-limitations-for-directquery"></a><span data-ttu-id="d4a76-175">ข้อควรพิจารณาและข้อจำกัดสำหรับ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="d4a76-175">Considerations and limitations for DirectQuery</span></span>

<span data-ttu-id="d4a76-176">มีข้อจำกัดที่เป็นที่รู้กันสองสามประการในเรื่องของ DirectQuery และกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4a76-176">There are a few known limitations with DirectQuery and dataflows:</span></span>

* <span data-ttu-id="d4a76-177">ในระหว่างช่วงเวลาการแสดงตัวอย่างของคุณลักษณะนี้ ลูกค้าบางรายอาจพบปัญหาเกี่ยวกับการหมดเวลา หรือประสิทธิภาพการทำงานเมื่อใช้ DirectQuery กับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4a76-177">During the preview period of this feature, some customers may experience timeouts or performance issues when using DirectQuery with dataflows.</span></span> <span data-ttu-id="d4a76-178">ปัญหาดังกล่าวจะได้รับการแก้ไขในระหว่างช่วงเวลาการแสดงตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="d4a76-178">Such issues are being actively addressed during this preview period.</span></span>

* <span data-ttu-id="d4a76-179">ขณะนี้ยังไม่รองรับแบบจำลองแบบรวม/แบบผสมที่มีการนำเข้าและแหล่งข้อมูล DirectQuery</span><span class="sxs-lookup"><span data-stu-id="d4a76-179">Composite/mixed models that have import and DirectQuery data sources are currently not supported.</span></span>

* <span data-ttu-id="d4a76-180">กระแสข้อมูลขนาดใหญ่อาจมีปัญหาเกี่ยวกับปัญหาการหมดเวลาเมื่อดูการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="d4a76-180">Large dataflows may have trouble with timeout issues when viewing visualizations.</span></span> <span data-ttu-id="d4a76-181">กระแสข้อมูลขนาดใหญ่ที่ประสบกับปัญหาการหมดเวลาควรใช้โหมดการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="d4a76-181">Large dataflows that run into trouble with timeout issues should use Import mode.</span></span>

* <span data-ttu-id="d4a76-182">ภายใต้การตั้งค่าแหล่งข้อมูล ตัวเชื่อมต่อกระแสข้อมูลจะแสดงข้อมูลประจำตัวที่ไม่ถูกต้องหากคุณกำลังใช้ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="d4a76-182">Under data source settings, the dataflow connector will show invalid credentials if you are using DirectQuery.</span></span> <span data-ttu-id="d4a76-183">การดำเนินการนี้จะไม่ส่งผลกระทบต่อลักษณะการทำงาน และชุดข้อมูลจะทำงานได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="d4a76-183">This does not affect the behavior, and the dataset will work properly.</span></span> 

## <a name="computed-entities"></a><span data-ttu-id="d4a76-184">เอนทิตีที่คำนวณ</span><span class="sxs-lookup"><span data-stu-id="d4a76-184">Computed entities</span></span>

<span data-ttu-id="d4a76-185">คุณสามารถดำเนินการ **การประมวลผลในที่จัดเก็บ** ได้เมื่อใช้ **กระแสข้อมูล** ที่มีการสมัครใช้งาน Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="d4a76-185">You can perform **in-storage computations** when using **dataflows** with a Power BI Premium subscription.</span></span> <span data-ttu-id="d4a76-186">ซึ่งจะช่วยให้คุณคำนวณกระแสข้อมูลที่มีอยู่แล้วและส่งผลลัพธ์กลับได้ โดยจะทำให้คุณได้เพ่งความสนใจไปยังการสร้างและการวิเคราะห์รายงาน</span><span class="sxs-lookup"><span data-stu-id="d4a76-186">This lets you perform calculations on your existing dataflows, and return results that enable you to focus on report creation and analytics.</span></span>

![เอนทิตีที่คำนวณ](media/dataflows-premium-features/computed-entity.png)

<span data-ttu-id="d4a76-188">เมื่อต้องการทำเนินการการคำนวณในที่จัดเก็บ คุณต้องสร้างกระแสข้อมูลและนำข้อมูลเข้าที่จัดเก็บกระแสข้อมูลของ Power BI ก่อนเป็นอันดับแรก</span><span class="sxs-lookup"><span data-stu-id="d4a76-188">To perform in-storage computations, you first must create the dataflow and bring data into that Power BI dataflow storage.</span></span> <span data-ttu-id="d4a76-189">เมื่อคุณมีกระแสข้อมูลที่มีข้อมูลแล้ว คุณก็จะสามารถสร้าง เอนทิตีที่คำนวณไว้ ได้ ซึ่งเป็นเอนทิตีที่ใช้ประมวลผลในที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="d4a76-189">Once you have a dataflow that contains data, you can create computed entities, which are entities that perform in-storage computations.</span></span>

### <a name="considerations-and-limitations-of-computed-entities"></a><span data-ttu-id="d4a76-190">ข้อควรพิจารณาและข้อจำกัดของเอนทิตีที่คำนวณ</span><span class="sxs-lookup"><span data-stu-id="d4a76-190">Considerations and limitations of computed entities</span></span>

* <span data-ttu-id="d4a76-191">เมื่อทำงานโดยใช้กระแสข้อมูลที่สร้างขึ้นในบัญชี Azure Data Lake Storage Gen2 ภายในองค์กร เอนทิตีที่มีลิงก์และเอนทิตีที่มีการคำนวณจะทำงานได้อย่างมีประสิทธิภาพต่อเมื่อเอนทิตี้ทั้งสองอยู่ในบัญชีที่เก็บข้อมูลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="d4a76-191">When working with dataflows created in an organization's Azure Data Lake Storage Gen2 account, linked entities and computed entities only work properly when the entities reside in the same storage account.</span></span> 

<span data-ttu-id="d4a76-192">ตามแนวทางปฏิบัติที่ดีที่สุดเมื่อทำการคำนวณข้อมูลที่รวมเข้าด้วยกันโดยข้อมูลภายในองค์กรและข้อมูลบนคลาวด์ ให้สร้างกระแสข้อมูลใหม่สำหรับแหล่งข้อมูลแต่ละแหล่ง (หนึ่งรายการสำหรับภายในองค์กรและอีกแหล่งหนึ่งสำหรับระบบคลาวด์) จากนั้นสร้างกระแสข้อมูลที่สามเพื่อรวม/คำนวณทั้งสองแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4a76-192">As a best practice, when doing computations on data joined by on-premises and cloud data, create a new dataflow for each source (one for on-premises and one for cloud) and then create a third dataflow to merge/compute over these two data sources.</span></span>

## <a name="linked-entities"></a><span data-ttu-id="d4a76-193">เอนทิตีที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="d4a76-193">Linked entities</span></span>

<span data-ttu-id="d4a76-194">คุณสามารถอ้างอิงกระแสข้อมูลที่มีอยู่เมื่อใช้กับการสมัครใช้งาน Power BI Premium ซึ่งช่วยให้คุณทำการคำนวณในเอนทิตีเหล่านี้โดยใช้เอนทิตีที่คำนวณหรืออนุญาตให้คุณสร้างตาราง "งแหล่งที่มาจริงเพียงแหล่งเดียว" ที่คุณสามารถใช้ซ้ำภายในกระแสข้อมูลหลายรายการได้</span><span class="sxs-lookup"><span data-stu-id="d4a76-194">You can reference existing dataflows when using with a Power BI Premium subscription, which lets you either perform calculation on these entities using computed entities or allows you to create a "single source of the truth" table that you can reuse within multiple dataflows.</span></span>

## <a name="incremental-refresh"></a><span data-ttu-id="d4a76-195">การรีเฟรชแบบเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="d4a76-195">Incremental refresh</span></span>

<span data-ttu-id="d4a76-196">คุณสามารถตั้งค่ากระแสข้อมูลให้รีเฟรชทีละน้อยเพื่อหลีกเลี่ยงการดึงข้อมูลทั้งหมดในทุกการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="d4a76-196">Dataflows can be set to refresh incrementally to avoid having to pull all the data on every refresh.</span></span> <span data-ttu-id="d4a76-197">เมื่อต้องการทำเช่นนั้น ให้เลือกกระแสข้อมูล แล้วเลือกไอคอนรีเฟรชแบบเพิ่มหน่วย</span><span class="sxs-lookup"><span data-stu-id="d4a76-197">To do so, select the dataflow then select the incremental refresh icon.</span></span>

![การรีเฟรชแบบเพิ่ม](media/dataflows-premium-features/incremental-refresh.png)

<span data-ttu-id="d4a76-199">การตั้งค่าการรีเฟรชแบบเพิ่มหน่วยจะเพิ่มพารามิเตอร์ให้กับกระแสข้อมูลเพื่อระบุช่วงวันที่</span><span class="sxs-lookup"><span data-stu-id="d4a76-199">Setting incremental refresh adds parameters to the dataflow to specify the date range.</span></span> <span data-ttu-id="d4a76-200">สำหรับข้อมูลโดยละเอียดเกี่ยวกับวิธีตั้งค่าการรีเฟรชแบบเพิ่มหน่วย โปรดดูบทความ [การรีเฟรชแบบเพิ่มหน่วย](/power-query/dataflows/incremental-refresh)</span><span class="sxs-lookup"><span data-stu-id="d4a76-200">For detailed information on how to set up incremental refresh, see the [incremental refresh](/power-query/dataflows/incremental-refresh) article.</span></span>

### <a name="considerations-for-when-not-to-set-incremental-refresh"></a><span data-ttu-id="d4a76-201">ข้อควรพิจารณาเมื่อไม่ควรตั้งค่าการรีเฟรชแบบเพิ่มหน่วย</span><span class="sxs-lookup"><span data-stu-id="d4a76-201">Considerations for when not to set incremental refresh</span></span>

<span data-ttu-id="d4a76-202">อย่าตั้งค่ากระแสข้อมูลเป็นการรีเฟรชแบบเพิ่มหน่วยในสถานการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d4a76-202">Do not set a dataflow to incremental refresh in the following situations:</span></span>

* <span data-ttu-id="d4a76-203">เอนทิตีที่เชื่อมโยงไม่ควรใช้การรีเฟรชแบบเพิ่มหน่วยหากอ้างอิงกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4a76-203">Linked entities should not use incremental refresh if they reference a dataflow.</span></span> <span data-ttu-id="d4a76-204">กระแสข้อมูลไม่สนับสนุนการพับคิวรี (แม้ว่าเอนทิตีจะเปิดใช้งาน Direct Query)</span><span class="sxs-lookup"><span data-stu-id="d4a76-204">Dataflows does not support query folding (even if the entity is DirectQuery enabled).</span></span> 
* <span data-ttu-id="d4a76-205">ชุดข้อมูลที่อ้างอิงกระแสข้อมูลไม่ควรใช้การรีเฟรชแบบเพิ่มหน่วย</span><span class="sxs-lookup"><span data-stu-id="d4a76-205">Datasets referencing dataflows should not use incremental refresh.</span></span> <span data-ttu-id="d4a76-206">โดยทั่วไปการรีเฟรชกระแสข้อมูลควรทำงานได้ดี</span><span class="sxs-lookup"><span data-stu-id="d4a76-206">Refreshes to dataflows should generally perform well.</span></span> <span data-ttu-id="d4a76-207">ถ้าการรีเฟรชใช้เวลานานกว่าที่คาดไว้ ให้พิจารณาใช้กลไกการคำนวณและหรือโหมด DirectQuery</span><span class="sxs-lookup"><span data-stu-id="d4a76-207">If the refreshes take longer than expected, consider using the compute engine and or DirectQuery mode.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d4a76-208">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d4a76-208">Next steps</span></span>
<span data-ttu-id="d4a76-209">บทความต่อไปนี้ให้ข้อมูลเพิ่มเติมเกี่ยวกับกระแสข้อมูลและ Power BI:</span><span class="sxs-lookup"><span data-stu-id="d4a76-209">The following articles provide more information about dataflows and Power BI:</span></span>

* [<span data-ttu-id="d4a76-210">แนวทางปฏิบัติที่ดีที่สุดสำหรับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4a76-210">Dataflows best practices</span></span>](dataflows-best-practices.md)
* [<span data-ttu-id="d4a76-211">กำหนดค่าปริมาณงานกระแสข้อมูลของ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="d4a76-211">Configure Power BI Premium dataflow workloads</span></span>](dataflows-premium-workload-configuration.md)
* [<span data-ttu-id="d4a76-212">ข้อมูลเบื้องต้นเกี่ยวกับกระแสข้อมูลและการเตรียมข้อมูลด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d4a76-212">Introduction to dataflows and self-service data prep</span></span>](dataflows-introduction-self-service.md)
* [<span data-ttu-id="d4a76-213">การสร้างกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4a76-213">Creating a dataflow</span></span>](dataflows-create.md)
* [<span data-ttu-id="d4a76-214">กำหนดค่าและใช้กระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4a76-214">Configure and consume a dataflow</span></span>](dataflows-configure-consume.md)
* [<span data-ttu-id="d4a76-215">การกำหนดค่าที่จัดเก็บกระแสข้อมูลเพื่อใช้ Azure Data Lake Gen 2</span><span class="sxs-lookup"><span data-stu-id="d4a76-215">Configuring Dataflow storage to use Azure Data Lake Gen 2</span></span>](dataflows-azure-data-lake-storage-integration.md)
* [<span data-ttu-id="d4a76-216">AI กับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4a76-216">AI with dataflows</span></span>](dataflows-machine-learning-integration.md)
* [<span data-ttu-id="d4a76-217">ข้อจำกัดและข้อควรพิจารณาของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4a76-217">Dataflows limitations and considerations</span></span>](dataflows-features-limitations.md)