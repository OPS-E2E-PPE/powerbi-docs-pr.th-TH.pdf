---
title: กำหนดค่าและใช้กระแสข้อมูล
description: ภาพรวมของวิธีการตั้งค่าและใช้กระแสข้อมูลใน Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-dataflows
ms.topic: how-to
ms.date: 10/01/2020
LocalizationGroup: Data from files
ms.openlocfilehash: 5f33f43565187c0276cf6d9c3479bbbb57480ae5
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96416197"
---
# <a name="configure-and-consume-a-dataflow"></a><span data-ttu-id="b9fcf-103">กำหนดค่าและใช้กระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9fcf-103">Configure and consume a dataflow</span></span>

<span data-ttu-id="b9fcf-104">ด้วยกระแสข้อมูล คุณสามารถรวมข้อมูลจากหลายแหล่งและเตรียมข้อมูลที่เป็นหนึ่งเดียวสำหรับการสร้างแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="b9fcf-104">With dataflows, you can unify data from multiple sources and prepare that unified data for modeling.</span></span> <span data-ttu-id="b9fcf-105">เมื่อใดก็ตามที่คุณสร้างกระแสข้อมูล คุณจะได้รับแจ้งให้รีเฟรชข้อมูลสำหรับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9fcf-105">Whenever you create a dataflow, you're prompted to refresh the data for the dataflow.</span></span> <span data-ttu-id="b9fcf-106">จำเป็นต้องมีการรีเฟรชกระแสข้อมูลก่อนจึงจะสามารถใช้งานในชุดข้อมูลภายใน Power BI Desktop หรืออ้างอิงเป็นเอนทิตีที่เชื่อมโยงหรือคำนวณ</span><span class="sxs-lookup"><span data-stu-id="b9fcf-106">Refreshing a dataflow is required before it can be consumed in a dataset inside Power BI Desktop, or referenced as a linked or computed entity.</span></span>

## <a name="configuring-a-dataflow"></a><span data-ttu-id="b9fcf-107">การกำหนดค่ากระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9fcf-107">Configuring a dataflow</span></span>

<span data-ttu-id="b9fcf-108">หากต้องการกำหนดค่าการรีเฟรชกระแสข้อมูล ให้เลือกเมนู **เพิ่มเติม** (จุดไข่ปลา) และเลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="b9fcf-108">To configure the refresh of a dataflow, select the **More** menu (the ellipsis) and select **Settings**.</span></span>

![พอร์ทัลการตั้งค่ากระแสข้อมูล](media/dataflows-configure-consume/dataflow-settings.png)

<span data-ttu-id="b9fcf-110">ตัวเลือก **การตั้งค่า** มีตัวเลือกมากมายสำหรับกระแสข้อมูลของคุณ ดังที่อธิบายในส่วนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b9fcf-110">The **Settings** options provide many options for your dataflow, as the following sections describe.</span></span>

![การตั้งค่ากระแสข้อมูล](media/dataflows-configure-consume/dataflow-settings-detailed.png)

* <span data-ttu-id="b9fcf-112">**มีความเป็นเจ้าของ:** หากคุณไม่ใช่เจ้าของกระแสข้อมูล การตั้งค่าเหล่านี้จำนวนมากจะถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="b9fcf-112">**Take ownership:** If you're not the owner of the dataflow, many of these settings are disabled.</span></span> <span data-ttu-id="b9fcf-113">หากต้องการเป็นเจ้าของกระแสข้อมูล ให้เลือก **เข้าครอง** เพื่อใช้การควบคุม</span><span class="sxs-lookup"><span data-stu-id="b9fcf-113">To take ownership of the dataflow, select **Take over** to take control.</span></span> <span data-ttu-id="b9fcf-114">คุณจะได้รับแจ้งให้ระบุข้อมูลประจำตัวเพื่อให้แน่ใจว่าคุณมีระดับการเข้าถึงที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="b9fcf-114">You are prompted to provide credentials to ensure you have the necessary access level.</span></span>

* <span data-ttu-id="b9fcf-115">**การเชื่อมต่อเกตเวย์:** ในส่วนนี้ คุณสามารถเลือกได้ว่าจะให้กระแสข้อมูลใช้เกตเวย์หรือไม่ และเลือกว่าจะใช้เกตเวย์ใด</span><span class="sxs-lookup"><span data-stu-id="b9fcf-115">**Gateway Connection:** In this section, you can choose whether the dataflow uses a gateway, and select which gateway is used.</span></span> 

* <span data-ttu-id="b9fcf-116">**ข้อมูลประจำตัวของแหล่งข้อมูล:** ในส่วนนี้คุณสามารถเลือกได้ว่าจะใช้ข้อมูลประจำตัวใด และสามารถเปลี่ยนวิธีการพิสูจน์ตัวตนกับแหล่งข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="b9fcf-116">**Data Source Credentials:** In this section you choose which credentials are being used, and can change how you authenticate to the data source.</span></span>

* <span data-ttu-id="b9fcf-117">**ป้ายชื่อระดับความลับ:** ที่นี่คุณสามารถกำหนดความอ่อนไหวของข้อมูลในกระแสข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="b9fcf-117">**Sensitivity Label:** Here you can define the sensitivity of the data in the dataflow.</span></span> <span data-ttu-id="b9fcf-118">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับป้ายชื่อระดับความลับ โปรดดู [วิธีการใช้ป้ายชื่อระดับความลับใน Power BI](../../admin/service-security-apply-data-sensitivity-labels.md)</span><span class="sxs-lookup"><span data-stu-id="b9fcf-118">To learn more about sensitivity labels, see [how to apply sensitivity labels in Power BI](../../admin/service-security-apply-data-sensitivity-labels.md).</span></span>

* <span data-ttu-id="b9fcf-119">**รีเฟรชตามกำหนดการ:** ที่นี่คุณสามารถกำหนดช่วงเวลาของวันที่การรีเฟรชกระแสข้อมูลที่เลือกได้</span><span class="sxs-lookup"><span data-stu-id="b9fcf-119">**Scheduled Refresh:** Here you can define the times of day the selected dataflow refreshes.</span></span> <span data-ttu-id="b9fcf-120">คุณสามารถรีเฟรชกระแสข้อมูลที่ความถี่เดียวกับชุดข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="b9fcf-120">A dataflow can be refreshed at the same frequency as a dataset.</span></span>

* <span data-ttu-id="b9fcf-121">**การตั้งค่ากลไกการคำนวณขั้นสูง:** ที่นี่คุณสามารถกำหนดได้ว่าจะจัดเก็บกระแสข้อมูลไว้ในกลไกการคำนวณหรือไม่</span><span class="sxs-lookup"><span data-stu-id="b9fcf-121">**Enhanced Compute Engine settings:** Here you can define whether the dataflow is stored inside the compute engine.</span></span> <span data-ttu-id="b9fcf-122">กลไกการคำนวณช่วยให้กระแสข้อมูลที่ตามมา ซึ่งอ้างอิงกระแสข้อมูลนี้ ทำการผสานและรวมและการแปลงอื่น ๆ ได้เร็วกว่าที่คุณเคยทำ</span><span class="sxs-lookup"><span data-stu-id="b9fcf-122">The compute engine allows subsequent dataflows, which reference this dataflow, to perform merges and joins and other transformations much faster than you would otherwise.</span></span> <span data-ttu-id="b9fcf-123">นอกจากนี้ยังอนุญาตให้ DirectQuery ดำเนินการผ่านกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9fcf-123">It also allows DirectQuery to be performed over the dataflow.</span></span> <span data-ttu-id="b9fcf-124">การเลือก **เปิด** ทำให้แน่ใจว่าระบบรองรับกระแสข้อมูลในโหมด DirectQuery เสมอและการอ้างอิงใดก็ตามจะได้รับประโยชน์จากกลไกดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="b9fcf-124">Selecting **On** ensures the dataflow is always supported in DirectQuery mode, and any references benefit from the engine.</span></span> <span data-ttu-id="b9fcf-125">การเลือก **แบบปรับให้เหมาะสม** หมายความว่ากลไกจะถูกใช้ก็ต่อเมื่อมีการอ้างอิงถึงกระแสข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="b9fcf-125">Selecting **Optimized** means the engine is only used if there is a reference to this dataflow.</span></span> <span data-ttu-id="b9fcf-126">การเลือก **ปิด** จะปิดใช้งานกลไกการคำนวณและความสามารถของ DirectQuery สำหรับกระแสข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="b9fcf-126">Selecting **Off** disables the compute engine and DirectQuery capability for this dataflow.</span></span>

* <span data-ttu-id="b9fcf-127">**การรับรอง:** คุณสามารถกำหนดว่าคุณจะรับรองหรือเลื่อนระดับกระแสข้อมูลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="b9fcf-127">**Endorsements:** You can define whether the dataflow is certified or promoted.</span></span> 

## <a name="refreshing-a-dataflow"></a><span data-ttu-id="b9fcf-128">รีเฟรชกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9fcf-128">Refreshing a dataflow</span></span>
<span data-ttu-id="b9fcf-129">กระแสข้อมูลทำหน้าที่เป็นบล็อกการสร้างอยู่ด้านบนของกันและกัน</span><span class="sxs-lookup"><span data-stu-id="b9fcf-129">Dataflows act as building blocks on top of one another.</span></span> <span data-ttu-id="b9fcf-130">สมมติว่าคุณมีกระแสข้อมูลที่เรียกว่า *ข้อมูลดิบ* และเอนทิตีที่เชื่อมโยงชื่อ *ข้อมูลที่แปลงแล้ว* ซึ่งประกอบด้วยเอนทิตีที่เชื่อมโยงกับกระแสข้อมูล *ข้อมูลดิบ*</span><span class="sxs-lookup"><span data-stu-id="b9fcf-130">Suppose you have a dataflow called *Raw Data* and a linked entity called *Transformed Data* which contains a linked entity to the *Raw Data* dataflow.</span></span> <span data-ttu-id="b9fcf-131">เมื่อรีเฟรชตามกำหนดการสำหรับกระแสข้อมูล *ข้อมูลดิบ* ทริกเกอร์ ระบบจะทริกเกอร์กระแสข้อมูลใดก็ตามที่อ้างถึงเมื่อเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="b9fcf-131">When the schedule refresh for the dataflow *Raw Data* triggers, it will trigger any dataflow that references it upon completion.</span></span> <span data-ttu-id="b9fcf-132">ฟังก์ชันการทำงานนี้จะสร้างเอฟเฟกต์ลูกโซ่ของการรีเฟรชซึ่งช่วยให้คุณไม่ต้องกำหนดเวลากระแสข้อมูลด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b9fcf-132">This functionality creates a chain effect of refreshes, allowing you to avoid having to schedule dataflows manually.</span></span> <span data-ttu-id="b9fcf-133">มีความแตกต่างบางประการที่ต้องระวังเมื่อจัดการกับการรีเฟรชเอนทิตีที่มีการเชื่อมโยง:</span><span class="sxs-lookup"><span data-stu-id="b9fcf-133">There are a few nuances to be aware of when dealing with linked entities refreshes:</span></span>

* <span data-ttu-id="b9fcf-134">เอนทิตีที่มีการเชื่อมโยงจะถูกทริกเกอร์โดยการรีเฟรชเฉพาะในกรณีที่มีอยู่ในพื้นที่ทำงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="b9fcf-134">A linked entity will be triggered by a refresh only if it exists in the same workspace</span></span>

* <span data-ttu-id="b9fcf-135">เอนทิตีที่มีการเชื่อมโยงจะถูกล็อกสำหรับการแก้ไขหากมีการรีเฟรชเอนทิตีต้นทาง</span><span class="sxs-lookup"><span data-stu-id="b9fcf-135">A linked entity will be locked for editing if a source entity is being refreshed.</span></span> <span data-ttu-id="b9fcf-136">หากการรีเฟรชกระแสข้อมูลใดก็ตามในห่วงโซ่อ้างอิงล้มเหลว กระแสข้อมูลทั้งหมดจะย้อนกลับไปเป็นข้อมูลเก่า (การรีเฟรชกระแสข้อมูลเป็นการทำธุรกรรมภายในพื้นที่ทำงาน)</span><span class="sxs-lookup"><span data-stu-id="b9fcf-136">If any of the dataflows in a reference chain fail to refresh, all the dataflows will roll back to the old data (dataflow refreshes are transactional within a workspace).</span></span>

* <span data-ttu-id="b9fcf-137">มีการรีเฟรชเอนทิตีที่อ้างอิงเฉพาะเมื่อการรีเฟรชต้นทางทริกเกอร์เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="b9fcf-137">Only referenced entities are refreshed when triggered by a source refresh completion.</span></span> <span data-ttu-id="b9fcf-138">หากต้องการกำหนดเวลาเอนทิตีทั้งหมด คุณควรตั้งค่าการรีเฟรชตามกำหนดการในเอนทิตีที่เชื่อมโยงด้วย</span><span class="sxs-lookup"><span data-stu-id="b9fcf-138">To schedule all the entities, you should set a schedule refresh on the linked entity as well.</span></span> <span data-ttu-id="b9fcf-139">หลีกเลี่ยงการตั้งค่ากำหนดการรีเฟรชบนกระแสข้อมูลที่เชื่อมโยงเพื่อหลีกเลี่ยงการรีเฟรชสองครั้ง</span><span class="sxs-lookup"><span data-stu-id="b9fcf-139">Avoid setting a refresh schedule on linked dataflows to avoid double refresh.</span></span>

<span data-ttu-id="b9fcf-140">กระแสข้อมูล **ยกเลิกการรีเฟรช** รองรับความสามารถในการยกเลิกการรีเฟรช ซึ่งแตกต่างจากชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9fcf-140">**Cancel Refresh** Dataflows support the ability to cancel a refresh, unlike datasets.</span></span> <span data-ttu-id="b9fcf-141">หากการรีเฟรชทำงานเป็นเวลานาน คุณสามารถเลือกตัวเลือกกระแสข้อมูล (จุดไข่ปลาที่อยู่ถัดจากกระแสข้อมูล) จากนั้นเลือก **ยกเลิกการรีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="b9fcf-141">If a refresh is running a long time, you can select the dataflow options (the ellipses next to the dataflow) and then select **Cancel refresh**.</span></span>

<span data-ttu-id="b9fcf-142">**การรีเฟรชแบบเพิ่มหน่วย (Premium เท่านั้น)** คุณสามารถตั้งค่าให้รีเฟรชกระแสข้อมูลทีละน้อยได้</span><span class="sxs-lookup"><span data-stu-id="b9fcf-142">**Incremental Refresh (Premium only)** Dataflows can be also set to refresh incrementally.</span></span> <span data-ttu-id="b9fcf-143">เมื่อต้องการทำเช่นนั้น ให้เลือกกระแสข้อมูลที่คุณต้องการตั้งค่าสำหรับการรีเฟรชแบบเพิ่มหน่วย จากนั้นเลือกไอคอนการรีเฟรชแบบเพิ่มหน่วย</span><span class="sxs-lookup"><span data-stu-id="b9fcf-143">To do so, select the dataflow you wish to set up for incremental refresh, and then select the incremental refresh icon.</span></span>

![การรีเฟรชกระแสข้อมูลแบบเพิ่มหน่วย](media/dataflows-configure-consume/dataflow-created-entity.png)

<span data-ttu-id="b9fcf-145">การตั้งค่าการรีเฟรชแบบเพิ่มหน่วยจะเพิ่มพารามิเตอร์ให้กับกระแสข้อมูลเพื่อระบุช่วงวันที่</span><span class="sxs-lookup"><span data-stu-id="b9fcf-145">Setting incremental refresh adds parameters to the dataflow to specify the date range.</span></span> <span data-ttu-id="b9fcf-146">สำหรับข้อมูลโดยละเอียดเกี่ยวกับวิธีตั้งค่าการรีเฟรชแบบเพิ่มหน่วย โปรดดูบทความ [การรีเฟรชแบบเพิ่มหน่วยใน Power Query](/power-query/dataflows/incremental-refresh)</span><span class="sxs-lookup"><span data-stu-id="b9fcf-146">For detailed information on how to set up incremental refresh, see the [incremental refresh in Power Query](/power-query/dataflows/incremental-refresh) article.</span></span>

<span data-ttu-id="b9fcf-147">มีบางสถานการณ์ที่คุณไม่ควรตั้งค่าการรีเฟรชแบบเพิ่มหน่วย:</span><span class="sxs-lookup"><span data-stu-id="b9fcf-147">There are some circumstances under which you should not set incremental refresh:</span></span>

* <span data-ttu-id="b9fcf-148">เอนทิตีที่เชื่อมโยงไม่ควรใช้การรีเฟรชแบบเพิ่มหน่วยหากอ้างอิงกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9fcf-148">Linked entities should not use incremental refresh if they reference a dataflow.</span></span> <span data-ttu-id="b9fcf-149">กระแสข้อมูลไม่สนับสนุนการพับคิวรี (แม้ว่าเอนทิตีจะเปิดใช้งาน Direct Query)</span><span class="sxs-lookup"><span data-stu-id="b9fcf-149">Dataflows do not support query folding (even if the entity is Direct Query enabled).</span></span> 

* <span data-ttu-id="b9fcf-150">ชุดข้อมูลที่อ้างอิงกระแสข้อมูลไม่ควรใช้การรีเฟรชแบบเพิ่มหน่วย</span><span class="sxs-lookup"><span data-stu-id="b9fcf-150">Datasets referencing dataflows should not use incremental refresh.</span></span> <span data-ttu-id="b9fcf-151">โดยทั่วไปการรีเฟรชกระแสข้อมูลจะมีประสิทธิภาพ ดังนั้นจึงไม่จำเป็นต้องมีการรีเฟรชแบบเพิ่มหน่วย</span><span class="sxs-lookup"><span data-stu-id="b9fcf-151">Refreshes to dataflows are  generally performant, so incremental refreshes shouldn't be necessary.</span></span> <span data-ttu-id="b9fcf-152">ถ้าการรีเฟรชใช้เวลานานเกินไป ให้พิจารณาการใช้กลไกการคำนวณหรือโหมด DirectQuery</span><span class="sxs-lookup"><span data-stu-id="b9fcf-152">If refreshes take too long, consider using the compute engine, or DirectQuery mode.</span></span>

## <a name="consuming-a-dataflow"></a><span data-ttu-id="b9fcf-153">การใช้กระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9fcf-153">Consuming a dataflow</span></span>

<span data-ttu-id="b9fcf-154">คุณสามารถใช้งานกระแสข้อมูลได้ในสามวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b9fcf-154">A dataflow can be consumed in the following three ways:</span></span>

* <span data-ttu-id="b9fcf-155">สร้างเอนทิตีที่เชื่อมโยงจากกระแสข้อมูลเพื่ออนุญาตให้ผู้เขียนกระแสข้อมูลรายอื่นใช้ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9fcf-155">Create a linked entity from the dataflow to allow another dataflow author to use the data</span></span>

* <span data-ttu-id="b9fcf-156">สร้างชุดข้อมูลจากกระแสข้อมูลเพื่ออนุญาตให้ผู้ใช้สามารถใช้ประโยชน์ข้อมูลเพื่อสร้างรายงานได้</span><span class="sxs-lookup"><span data-stu-id="b9fcf-156">Create a dataset from the dataflow to allow a user to utilize the data to create reports</span></span>

* <span data-ttu-id="b9fcf-157">สร้างการเชื่อมต่อจากเครื่องมือภายนอกที่สามารถอ่านจากรูปแบบ CDM ได้</span><span class="sxs-lookup"><span data-stu-id="b9fcf-157">Create a connection from external tools that can read from the CDM format</span></span>

<span data-ttu-id="b9fcf-158">**การใช้งานจาก Power BI Desktop** เมื่อต้องการใช้กระแสข้อมูล ให้เรียกใช้ Power BI Desktop และเลือก **ตัวเชื่อมต่อกระแสข้อมูล Power BI** ในกล่องโต้ตอบ **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="b9fcf-158">**Consuming from Power BI Desktop** To consume a dataflow, run Power BI Desktop and select the **Power BI dataflows connector** in the **Get Data** dialog.</span></span>

> [!NOTE]
> <span data-ttu-id="b9fcf-159">ตัวเชื่อมต่อกระแสข้อมูล Power BI ใช้ชุดข้อมูลประจำตัวที่แตกต่างจากผู้ใช้ที่เข้าสู่ระบบปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b9fcf-159">The Power BI dataflows connector uses a different set of credentials than the current logged in user.</span></span> <span data-ttu-id="b9fcf-160">นี่คือการออกแบบ เพื่อรองรับผู้ใช้หลายผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="b9fcf-160">This is by design, to support multi-tenant users.</span></span>

![ตัวเชื่อมต่อกระแสข้อมูล](media/dataflows-configure-consume/dataflow-connector.png)

<span data-ttu-id="b9fcf-162">เลือกว่ากระแสข้อมูลใดและเอนทิตีใดที่คุณต้องการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="b9fcf-162">Select which dataflow and which entities to which you want to connect.</span></span> 

> [!NOTE]
> <span data-ttu-id="b9fcf-163">คุณสามารถเชื่อมต่อกับกระแสข้อมูลหรือเอนทิตีใดก็ตามไม่ว่าจะอยู่ในพื้นที่ทำงานใดและไม่ว่าจะกำหนดไว้ในพื้นที่ทำงานระดับพรีเมียมหรือไม่ใช่ระดับพรีเมียมก็ตาม</span><span class="sxs-lookup"><span data-stu-id="b9fcf-163">You can connect to any dataflow or entity regardless of which workspace it resides in, and whether or not it was defined in a Premium or non-Premium workspace.</span></span>

![เอนทิตีตัวเชื่อมต่อกระแสข้อมูล](media/dataflows-configure-consume/dataflow-entities-picker.png)

<span data-ttu-id="b9fcf-165">ถ้า DirectQuery พร้อมใช้งาน คุณจะได้รับพร้อมท์แจ้งให้เลือกว่าคุณต้องการเชื่อมต่อกับเอนทิตีผ่าน DirectQuery หรือ Import (นำเข้า)</span><span class="sxs-lookup"><span data-stu-id="b9fcf-165">If DirectQuery is available, you're prompted to choose whether you want to connect to the entities through DirectQuery or Import.</span></span> 

<span data-ttu-id="b9fcf-166">ในโหมด DirectQuery คุณสามารถสอบถามชุดข้อมูลขนาดใหญ่ภายในเครื่องได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="b9fcf-166">In DirectQuery mode, you can quickly interrogate large-scale datasets locally.</span></span> <span data-ttu-id="b9fcf-167">อย่างไรก็ตาม คุณไม่สามารถดำเนินการแปลงเพิ่มเติมใดก็ตามได้</span><span class="sxs-lookup"><span data-stu-id="b9fcf-167">However, you cannot perform any additional transformations.</span></span> 

<span data-ttu-id="b9fcf-168">การใช้โหมด นำเข้า จะนำข้อมูลเข้าไปยัง Power BI และจำเป็นต้องมีชุดข้อมูลเพื่อรีเฟรชอย่างอิสระจากกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9fcf-168">Using Import bring the data into Power BI, and requires the dataset to be refreshed independently of the dataflow.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b9fcf-169">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="b9fcf-169">Next steps</span></span>
<span data-ttu-id="b9fcf-170">บทความต่อไปนี้ให้ข้อมูลเพิ่มเติมเกี่ยวกับกระแสข้อมูลและ Power BI:</span><span class="sxs-lookup"><span data-stu-id="b9fcf-170">The following articles provide more information about dataflows and Power BI:</span></span>

* [<span data-ttu-id="b9fcf-171">ข้อมูลเบื้องต้นเกี่ยวกับกระแสข้อมูลและการเตรียมข้อมูลด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b9fcf-171">Introduction to dataflows and self-service data prep</span></span>](dataflows-introduction-self-service.md)
* [<span data-ttu-id="b9fcf-172">การสร้างกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9fcf-172">Creating a dataflow</span></span>](dataflows-create.md)
* [<span data-ttu-id="b9fcf-173">การกำหนดค่าที่จัดเก็บกระแสข้อมูลเพื่อใช้ Azure Data Lake Gen 2</span><span class="sxs-lookup"><span data-stu-id="b9fcf-173">Configuring Dataflow storage to use Azure Data Lake Gen 2</span></span>](dataflows-azure-data-lake-storage-integration.md)
* [<span data-ttu-id="b9fcf-174">ฟีเจอร์พรีเมียมของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9fcf-174">Premium features of dataflows</span></span>](dataflows-premium-features.md)
* [<span data-ttu-id="b9fcf-175">AI กับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9fcf-175">AI with dataflows</span></span>](dataflows-machine-learning-integration.md)
* [<span data-ttu-id="b9fcf-176">ข้อจำกัดและข้อควรพิจารณาของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9fcf-176">Dataflows limitations and considerations</span></span>](dataflows-features-limitations.md)
* [<span data-ttu-id="b9fcf-177">แนวทางปฏิบัติที่ดีที่สุดสำหรับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9fcf-177">Dataflows best practices</span></span>](dataflows-best-practices.md)