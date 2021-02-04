---
title: ตรวจสอบความจุ Power BI Premium โดยใช้พอร์ทัลผู้ดูแลระบบ
description: ใช้พอร์ทัลผู้ดูแลระบบ Power BI เพื่อตรวจสอบความจุ Premium ของคุณ
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-premium
ms.topic: how-to
ms.date: 11/11/2020
LocalizationGroup: Premium
ms.openlocfilehash: b6f6b819b5c31f655d0c0dc43d8852cb34b5a7a2
ms.sourcegitcommit: cc20b476a45bccb870c9de1d0b384e2c39e25d24
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/11/2020
ms.locfileid: "94512067"
---
# <a name="monitor-capacities-in-the-admin-portal"></a><span data-ttu-id="946c9-103">ตรวจสอบความจุในพอร์ทัลผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="946c9-103">Monitor capacities in the Admin portal</span></span>

<span data-ttu-id="946c9-104">แท็บ **สุขภาพ** ในพื้นที่ **การตั้งค่าความจุ** ในพอร์ทัลผู้ดูแลระบบจะให้ข้อมูลสรุปเมตริกเกี่ยวกับความจุของคุณและปริมาณงานที่เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="946c9-104">The **Health** tab in the **Capacity settings** area in the Admin portal provides a metrics summary about your capacity and enabled workloads.</span></span>  

![แท็บความจุสุขภาพในพอร์ทัล](media/service-admin-premium-monitor-portal/admin-portal-health.png)

<span data-ttu-id="946c9-106">ถ้าคุณต้องการเมตริกที่ครอบคลุมมากขึ้น ให้ใช้แอป [Power BI Premium Capacity Metric](service-admin-premium-monitor-capacity.md)</span><span class="sxs-lookup"><span data-stu-id="946c9-106">If you need more comprehensive metrics, use the [Power BI Premium Capacity Metrics](service-admin-premium-monitor-capacity.md) app.</span></span> <span data-ttu-id="946c9-107">แอปนี้มีข้อมูลการเจาะลึกรายละเอียดและการกรอง และเมตริกที่มีรายละเอียดมากที่สุดสำหรับเกือบทุกแง่มุมที่มีผลต่อประสิทธิภาพของความจุ</span><span class="sxs-lookup"><span data-stu-id="946c9-107">The app provides drill-down and filtering, and the most detailed metrics for near every aspect affecting capacity performance.</span></span> <span data-ttu-id="946c9-108">หากต้องการเรียนรู้เพิ่มเติม โปรดดู [ตรวจสอบความจุ Premium ด้วยแอป](service-admin-premium-monitor-capacity.md)</span><span class="sxs-lookup"><span data-stu-id="946c9-108">To learn more, see [Monitor Premium capacities with the app](service-admin-premium-monitor-capacity.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="946c9-109">ถ้าความจุ Power BI Premium ของคุณกำลังประสบปัญหาการใช้ทรัพยากรสูงจนส่งผลให้เกิดปัญหาด้านประสิทธิภาพการทำงานหรือความมั่นคง คุณสามารถรับอีเมลแจ้งเตือนเพื่อทราบปัญหาและแก้ไขปัญหาได้</span><span class="sxs-lookup"><span data-stu-id="946c9-109">If your Power BI Premium capacity is experiencing high resource usage, resulting in performance or reliability issues, you can receive notification emails to identify and resolve the issue.</span></span> <span data-ttu-id="946c9-110">ซึ่งอาจเป็นวิธีที่มีประสิทธิภาพในการแก้ไขปัญหาความจุโอเวอร์โหลด</span><span class="sxs-lookup"><span data-stu-id="946c9-110">This can be a streamlined way to troubleshoot overloaded capacities.</span></span> <span data-ttu-id="946c9-111">คุณสามารถศึกษาข้อมูลเพิ่มเติมได้ที่[ความจุและการแจ้งเตือนความมั่นคง](service-interruption-notifications.md#capacity-and-reliability-notifications)</span><span class="sxs-lookup"><span data-stu-id="946c9-111">See [capacity and reliability notifications](service-interruption-notifications.md#capacity-and-reliability-notifications) for more information.</span></span>

> [!NOTE]
> <span data-ttu-id="946c9-112">Power BI Premium เพิ่งเปิดตัว Premium เวอร์ชันใหม่ชื่อ **Premium Gen2** ซึ่งกำลังอยู่ในช่วงการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="946c9-112">Power BI Premium recently released a new version of Premium, called **Premium Gen2**, which is currently in preview.</span></span> <span data-ttu-id="946c9-113">Premium Gen2 จะทำให้การจัดการความจุระดับพรีเมียมง่ายขึ้นและลดค่าใช้จ่ายในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="946c9-113">Premium Gen2 will simplify the management of Premium capacities, and reduce management overhead.</span></span> <span data-ttu-id="946c9-114">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Power BI Premium Generation 2 (ตัวอย่าง)](service-premium-what-is.md#power-bi-premium-generation-2-preview)</span><span class="sxs-lookup"><span data-stu-id="946c9-114">For more information, see [Power BI Premium Generation 2 (preview)](service-premium-what-is.md#power-bi-premium-generation-2-preview).</span></span>

## <a name="system-metrics"></a><span data-ttu-id="946c9-115">เมตริกระบบ</span><span class="sxs-lookup"><span data-stu-id="946c9-115">System Metrics</span></span>

<span data-ttu-id="946c9-116">บนแท็บ **สุขภาพ** ที่ระดับสูงสุด การใช้งาน CPU และการใช้หน่วยความจำให้มุมมองที่รวดเร็วของเมตริกที่สำคัญที่สุดสำหรับความจุ</span><span class="sxs-lookup"><span data-stu-id="946c9-116">On the **Health** tab, at the highest level, CPU utilization and memory usage provide a quick view of the most important metrics for the capacity.</span></span> <span data-ttu-id="946c9-117">เมตริกเหล่านี้เป็นแบบสะสม รวมถึงปริมาณงานที่เปิดใช้งานทั้งหมดสำหรับความจุด้วย</span><span class="sxs-lookup"><span data-stu-id="946c9-117">These metrics are cumulative, including all enabled workloads for the capacity.</span></span>

| <span data-ttu-id="946c9-118">**การวัด**</span><span class="sxs-lookup"><span data-stu-id="946c9-118">**Metric**</span></span> | <span data-ttu-id="946c9-119">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="946c9-119">**Description**</span></span> |
| --- | --- |
| <span data-ttu-id="946c9-120">การใช้ CPU อย่างเต็มประโยชน์</span><span class="sxs-lookup"><span data-stu-id="946c9-120">CPU UTILIZATION</span></span> | <span data-ttu-id="946c9-121">การใช้งาน CPU โดยเฉลี่ย เป็นเปอร์เซ็นต์ของ CPU ที่ว่างพร้อมใช้งานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="946c9-121">Average CPU utilization, as a percentage of total available CPU.</span></span> |
| <span data-ttu-id="946c9-122">การใช้หน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="946c9-122">MEMORY USAGE</span></span> | <span data-ttu-id="946c9-123">การใช้หน่วยความจำโดยเฉลี่ย เป็นกิกะไบต์ (GB)</span><span class="sxs-lookup"><span data-stu-id="946c9-123">Average memory usage in gigabytes (GB).</span></span>|

## <a name="workload-metrics"></a><span data-ttu-id="946c9-124">เมตริกปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="946c9-124">Workload metrics</span></span>

<span data-ttu-id="946c9-125">สำหรับปริมาณงานแต่ละรายการที่เปิดใช้สำหรับความจุ</span><span class="sxs-lookup"><span data-stu-id="946c9-125">For each workload enabled for the capacity.</span></span> <span data-ttu-id="946c9-126">มีการแสดงข้อมูลการใช้งาน CPU และการใช้หน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="946c9-126">CPU utilization and memory usage are shown.</span></span>

| <span data-ttu-id="946c9-127">**การวัด**</span><span class="sxs-lookup"><span data-stu-id="946c9-127">**Metric**</span></span> | <span data-ttu-id="946c9-128">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="946c9-128">**Description**</span></span> |
| --- | --- |
| <span data-ttu-id="946c9-129">การใช้ CPU อย่างเต็มประโยชน์</span><span class="sxs-lookup"><span data-stu-id="946c9-129">CPU UTILIZATION</span></span> | <span data-ttu-id="946c9-130">การใช้งาน CPU โดยเฉลี่ย เป็นเปอร์เซ็นต์ของ CPU ที่ว่างพร้อมใช้งานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="946c9-130">Average CPU utilization, as a percentage of total available CPU.</span></span> |
| <span data-ttu-id="946c9-131">การใช้หน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="946c9-131">MEMORY USAGE</span></span> | <span data-ttu-id="946c9-132">การใช้หน่วยความจำโดยเฉลี่ย เป็นกิกะไบต์ (GB)</span><span class="sxs-lookup"><span data-stu-id="946c9-132">Average memory usage in gigabytes (GB).</span></span>|

### <a name="detailed-workload-metrics"></a><span data-ttu-id="946c9-133">เมตริกปริมาณงานโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="946c9-133">Detailed workload metrics</span></span>

<span data-ttu-id="946c9-134">ปริมาณงานแต่ละรายการมีเมตริกเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="946c9-134">Each workload has additional metrics.</span></span> <span data-ttu-id="946c9-135">ชนิดของเมตริกที่แสดงขึ้นอยู่กับปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="946c9-135">The type of metrics shown depend on the workload.</span></span> <span data-ttu-id="946c9-136">หากต้องการดูเมตริกโดยละเอียดสำหรับปริมาณงาน ให้คลิกลูกศร (ลง) ขยาย</span><span class="sxs-lookup"><span data-stu-id="946c9-136">To see detailed metrics for a workload, click the expand (down) arrow.</span></span>

![สุขภาพของปริมาณงานที่ขยาย](media/service-admin-premium-monitor-portal/admin-portal-health-expand.png)

#### <a name="dataflows"></a><span data-ttu-id="946c9-138">กระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="946c9-138">Dataflows</span></span>

##### <a name="dataflow-operations"></a><span data-ttu-id="946c9-139">การดำเนินการของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="946c9-139">Dataflow Operations</span></span>

| <span data-ttu-id="946c9-140">**การวัด**</span><span class="sxs-lookup"><span data-stu-id="946c9-140">**Metric**</span></span> | <span data-ttu-id="946c9-141">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="946c9-141">**Description**</span></span> |
| --- | --- |
| <span data-ttu-id="946c9-142">จำนวนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="946c9-142">Total Count</span></span> | <span data-ttu-id="946c9-143">การรีเฟรชทั้งหมดสำหรับแต่ละกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="946c9-143">Total refreshes for each dataflow.</span></span> |
| <span data-ttu-id="946c9-144">จำนวนความสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="946c9-144">Success Count</span></span> | <span data-ttu-id="946c9-145">การรีเฟรชที่สำเร็จทั้งหมดสำหรับแต่ละกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="946c9-145">Total successful refreshes for each dataflow.</span></span>|
| <span data-ttu-id="946c9-146">ระยะเวลาเฉลี่ย (นาที)</span><span class="sxs-lookup"><span data-stu-id="946c9-146">Average Duration (min)</span></span> | <span data-ttu-id="946c9-147">ระยะเวลาเฉลี่ยของการรีเฟรชสำหรับกระแสข้อมูล หน่วยเป็นนาที</span><span class="sxs-lookup"><span data-stu-id="946c9-147">The average duration of refresh for the dataflow, in minutes</span></span> |
| <span data-ttu-id="946c9-148">ระยะเวลาสูงสุด (นาที)</span><span class="sxs-lookup"><span data-stu-id="946c9-148">Max Duration (min)</span></span> | <span data-ttu-id="946c9-149">ระยะเวลาของการรีเฟรชที่ทำงานนานที่สุดสำหรับกระแสข้อมูล เป็นนาที</span><span class="sxs-lookup"><span data-stu-id="946c9-149">The duration of the longest-running refresh for the dataflow, in minutes.</span></span> |
| <span data-ttu-id="946c9-150">เวลารอเฉลี่ย (นาที)</span><span class="sxs-lookup"><span data-stu-id="946c9-150">Average Wait Time (min)</span></span> | <span data-ttu-id="946c9-151">การหน่วงเวลาเฉลี่ยระหว่างเวลาที่กำหนดไว้และเวลาเริ่มต้นของการรีเฟรชกระแสข้อมูล หน่วยเป็นนาที</span><span class="sxs-lookup"><span data-stu-id="946c9-151">The average lag between the scheduled time and start of a refresh for the dataflow, in minutes.</span></span> |
| <span data-ttu-id="946c9-152">เวลารอสูงสุด (นาที)</span><span class="sxs-lookup"><span data-stu-id="946c9-152">Max Wait Time (min)</span></span> | <span data-ttu-id="946c9-153">เวลารอสูงสุดสำหรับกระแสข้อมูล หน่วยเป็นนาที</span><span class="sxs-lookup"><span data-stu-id="946c9-153">The maximum wait time for the dataflow, in minutes.</span></span>  |

#### <a name="datasets"></a><span data-ttu-id="946c9-154">ชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="946c9-154">Datasets</span></span>

##### <a name="refresh"></a><span data-ttu-id="946c9-155">รีเฟรช</span><span class="sxs-lookup"><span data-stu-id="946c9-155">Refresh</span></span>

| <span data-ttu-id="946c9-156">**การวัด**</span><span class="sxs-lookup"><span data-stu-id="946c9-156">**Metric**</span></span> | <span data-ttu-id="946c9-157">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="946c9-157">**Description**</span></span> |
| --- | --- |
| <span data-ttu-id="946c9-158">จำนวนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="946c9-158">Total Count</span></span> | <span data-ttu-id="946c9-159">การรีเฟรชทั้งหมดสำหรับแต่ละชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="946c9-159">Total refreshes for each dataset.</span></span> |
| <span data-ttu-id="946c9-160">จำนวนความสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="946c9-160">Success Count</span></span> | <span data-ttu-id="946c9-161">การรีเฟรชที่สำเร็จทั้งหมดสำหรับแต่ละชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="946c9-161">Total successful refreshes for each dataset.</span></span> |
| <span data-ttu-id="946c9-162">จำนวนความล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="946c9-162">Failure Count</span></span> | <span data-ttu-id="946c9-163">การรีเฟรชที่ล้มเหลวทั้งหมดสำหรับแต่ละชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="946c9-163">Total failed refreshes for each dataset.</span></span> |
| <span data-ttu-id="946c9-164">อัตราความสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="946c9-164">Success Rate</span></span>  | <span data-ttu-id="946c9-165">จำนวนการรีเฟรชที่สำเร็จหารด้วยจำนวนการรีเฟรชทั้งหมดที่ทำการวัด</span><span class="sxs-lookup"><span data-stu-id="946c9-165">Number of successful refreshes divided by the total refreshes to measure.</span></span> <span data-ttu-id="946c9-166">ความน่าเชื่อถือ</span><span class="sxs-lookup"><span data-stu-id="946c9-166">reliability.</span></span> |
| <span data-ttu-id="946c9-167">ระยะเวลาเฉลี่ย (นาที)</span><span class="sxs-lookup"><span data-stu-id="946c9-167">Average Duration (min)</span></span> | <span data-ttu-id="946c9-168">ระยะเวลาเฉลี่ยของการรีเฟรชสำหรับชุดข้อมูล เป็นนาที</span><span class="sxs-lookup"><span data-stu-id="946c9-168">The average duration of refresh for the dataset, in minutes.</span></span>  |
| <span data-ttu-id="946c9-169">ระยะเวลาสูงสุด (นาที)</span><span class="sxs-lookup"><span data-stu-id="946c9-169">Max Duration (min)</span></span> | <span data-ttu-id="946c9-170">ระยะเวลาของการรีเฟรชที่ทำงานนานที่สุดสำหรับชุดข้อมูล หน่วยเป็นนาที</span><span class="sxs-lookup"><span data-stu-id="946c9-170">The duration of the longest-running refresh for the dataset, in minutes.</span></span> |
| <span data-ttu-id="946c9-171">เวลารอเฉลี่ย (นาที)</span><span class="sxs-lookup"><span data-stu-id="946c9-171">Average Wait Time (min)</span></span> | <span data-ttu-id="946c9-172">การหน่วงเวลาเฉลี่ยระหว่างเวลาที่กำหนดไว้และเวลาเริ่มต้นของการดำเนินการ หน่วยเป็นนาที</span><span class="sxs-lookup"><span data-stu-id="946c9-172">The average lag between the scheduled time and start of a refresh for the dataset, in minutes.</span></span> |
| <span data-ttu-id="946c9-173">เวลารอสูงสุด (นาที)</span><span class="sxs-lookup"><span data-stu-id="946c9-173">Max Wait Time (min)</span></span> | <span data-ttu-id="946c9-174">เวลารอสูงสุดสำหรับชุดข้อมูล หน่วยเป็นนาที</span><span class="sxs-lookup"><span data-stu-id="946c9-174">The maximum wait time for the dataset, in minutes.</span></span> |

##### <a name="query"></a><span data-ttu-id="946c9-175">คิวรี</span><span class="sxs-lookup"><span data-stu-id="946c9-175">Query</span></span>

| <span data-ttu-id="946c9-176">**การวัด**</span><span class="sxs-lookup"><span data-stu-id="946c9-176">**Metric**</span></span> | <span data-ttu-id="946c9-177">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="946c9-177">**Description**</span></span> |
| --- | --- |
| <span data-ttu-id="946c9-178">จำนวนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="946c9-178">Total Count</span></span> | <span data-ttu-id="946c9-179">จำนวนรวมของคิวรีที่เรียกใช้สำหรับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="946c9-179">The total number of queries run for the dataset.</span></span> |
| <span data-ttu-id="946c9-180">ระยะเวลาเฉลี่ย (ms)</span><span class="sxs-lookup"><span data-stu-id="946c9-180">Average Duration (ms)</span></span> |<span data-ttu-id="946c9-181">ระยะเวลาคิวรีเฉลี่ยสำหรับชุดข้อมูล หน่วยเป็นมิลลิวินาที</span><span class="sxs-lookup"><span data-stu-id="946c9-181">The average query duration for the dataset, in milliseconds</span></span>|
| <span data-ttu-id="946c9-182">ระยะเวลาสูงสุด (ms)</span><span class="sxs-lookup"><span data-stu-id="946c9-182">Max Duration (ms)</span></span> |<span data-ttu-id="946c9-183">ระยะเวลาคิวรีที่ทำงานนานที่สุดในชุดข้อมูล หน่วยเป็นมิลลิวินาที</span><span class="sxs-lookup"><span data-stu-id="946c9-183">The duration of the longest-running query in the dataset, in milliseconds.</span></span> |
| <span data-ttu-id="946c9-184">เวลารอเฉลี่ย (ms)</span><span class="sxs-lookup"><span data-stu-id="946c9-184">Average Wait Time (ms)</span></span> |<span data-ttu-id="946c9-185">ระยะเวลารอคิวรีเฉลี่ยสำหรับชุดข้อมูล หน่วยเป็นมิลลิวินาที</span><span class="sxs-lookup"><span data-stu-id="946c9-185">The average query wait time for the dataset, in milliseconds.</span></span> |
| <span data-ttu-id="946c9-186">เวลารอสูงสุด (ms)</span><span class="sxs-lookup"><span data-stu-id="946c9-186">Max Wait Time (ms)</span></span> |<span data-ttu-id="946c9-187">ระยะเวลาคิวรีที่รอนานที่สุดในชุดข้อมูล หน่วยเป็นมิลลิวินาที</span><span class="sxs-lookup"><span data-stu-id="946c9-187">The duration of the longest-waiting query in the dataset, in milliseconds.</span></span> |

##### <a name="eviction"></a><span data-ttu-id="946c9-188">การลดสัดส่วน</span><span class="sxs-lookup"><span data-stu-id="946c9-188">Eviction</span></span>

| <span data-ttu-id="946c9-189">**การวัด**</span><span class="sxs-lookup"><span data-stu-id="946c9-189">**Metric**</span></span> | <span data-ttu-id="946c9-190">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="946c9-190">**Description**</span></span> |
| --- | --- |
| <span data-ttu-id="946c9-191">จำนวนแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="946c9-191">Model Count</span></span> | <span data-ttu-id="946c9-192">จำนวนรวมของการลดสัดส่วนชุดข้อมูลสำหรับความจุนี้</span><span class="sxs-lookup"><span data-stu-id="946c9-192">The total number of dataset evictions for this capacity.</span></span> <span data-ttu-id="946c9-193">เมื่อความจุเผชิญกับความกดดันที่มีต่อหน่วยความจำ โหนดจะลดชุดข้อมูลอย่างน้อยหนึ่งชุดออกจากหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="946c9-193">When a capacity faces memory pressure, the node evicts one or more datasets from memory.</span></span> <span data-ttu-id="946c9-194">ชุดข้อมูลที่ไม่ได้ใช้งาน (ที่ไม่มีการสคิวรี่/ รีเฟรชกำลังดำเนินการอยู่) จะถูกขับออกก่อน</span><span class="sxs-lookup"><span data-stu-id="946c9-194">Datasets that are inactive (with no query/refresh operation currently executing) are evicted first.</span></span> <span data-ttu-id="946c9-195">จากนั้นคำสั่งการขับไล่จะขึ้นอยู่กับการวัด 'การใช้น้อยที่สุด' (LRU)</span><span class="sxs-lookup"><span data-stu-id="946c9-195">Then the eviction order is based on a measure of 'least recently used' (LRU).</span></span> |

#### <a name="paginated-reports"></a><span data-ttu-id="946c9-196">รายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="946c9-196">Paginated Reports</span></span>

##### <a name="report-execution"></a><span data-ttu-id="946c9-197">การดำเนินการรายงาน</span><span class="sxs-lookup"><span data-stu-id="946c9-197">Report Execution</span></span>

| <span data-ttu-id="946c9-198">**การวัด**</span><span class="sxs-lookup"><span data-stu-id="946c9-198">**Metric**</span></span> | <span data-ttu-id="946c9-199">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="946c9-199">**Description**</span></span> |
| --- | --- |
| <span data-ttu-id="946c9-200">จำนวนการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="946c9-200">Execution Count</span></span>  | <span data-ttu-id="946c9-201">จำนวนครั้งที่ผู้ใช้ดำเนินการและดูรายงาน</span><span class="sxs-lookup"><span data-stu-id="946c9-201">The number of times the report was been executed and viewed by users.</span></span>|

##### <a name="report-usage"></a><span data-ttu-id="946c9-202">การใช้รายงาน</span><span class="sxs-lookup"><span data-stu-id="946c9-202">Report Usage</span></span>

| <span data-ttu-id="946c9-203">**การวัด**</span><span class="sxs-lookup"><span data-stu-id="946c9-203">**Metric**</span></span> | <span data-ttu-id="946c9-204">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="946c9-204">**Description**</span></span> |
| --- | --- |
| <span data-ttu-id="946c9-205">จำนวนความสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="946c9-205">Success Count</span></span> | <span data-ttu-id="946c9-206">จำนวนครั้งที่ผู้ใช้ดูรายงาน</span><span class="sxs-lookup"><span data-stu-id="946c9-206">The number of times the report has been viewed by a user.</span></span> |
| <span data-ttu-id="946c9-207">จำนวนความล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="946c9-207">Failure Count</span></span> |<span data-ttu-id="946c9-208">จำนวนครั้งที่ผู้ใช้ดูรายงาน</span><span class="sxs-lookup"><span data-stu-id="946c9-208">The number of times the report has been viewed by a user.</span></span>|
| <span data-ttu-id="946c9-209">จำนวนแถว</span><span class="sxs-lookup"><span data-stu-id="946c9-209">Row Count</span></span> |<span data-ttu-id="946c9-210">จำนวนแถวของข้อมูลในรายงาน</span><span class="sxs-lookup"><span data-stu-id="946c9-210">The number of rows of data in the report.</span></span> |
| <span data-ttu-id="946c9-211">ระยะเวลาการเรียกข้อมูล (ms)</span><span class="sxs-lookup"><span data-stu-id="946c9-211">Data Retrieval Duration (ms)</span></span> |<span data-ttu-id="946c9-212">ปริมาณเวลาเฉลี่ยที่ใช้ในการดึงข้อมูลสำหรับรายงาน หน่วยเป็นมิลลิวินาที</span><span class="sxs-lookup"><span data-stu-id="946c9-212">The average amount of time it takes to retrieve data for the report, in milliseconds.</span></span> <span data-ttu-id="946c9-213">ระยะเวลาที่ยาวนานอาจเป็นการบ่งชี้ถึงคิวรีที่ช้าหรือปัญหาแหล่งข้อมูลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="946c9-213">Long durations can indicate slow queries or other data source issues.</span></span>  |
| <span data-ttu-id="946c9-214">ระยะเวลาการประมวลผล (ms)</span><span class="sxs-lookup"><span data-stu-id="946c9-214">Processing Duration (ms)</span></span> |<span data-ttu-id="946c9-215">ปริมาณเวลาเฉลี่ยที่ใช้ในการประมวลผลข้อมูลสำหรับรายงาน หน่วยเป็นมิลลิวินาที</span><span class="sxs-lookup"><span data-stu-id="946c9-215">The average amount of time it takes to process the data for a report, in milliseconds.</span></span> |
| <span data-ttu-id="946c9-216">ระยะเวลาการแสดงผล (ms)</span><span class="sxs-lookup"><span data-stu-id="946c9-216">Rendering Duration (ms)</span></span> |<span data-ttu-id="946c9-217">ปริมาณเวลาเฉลี่ยที่ใช้ในการแสดงรายงานในเบราเซอร์ หน่วยเป็นมิลลิวินาที</span><span class="sxs-lookup"><span data-stu-id="946c9-217">The average amount of time it takes to render a report in the browser, in milliseconds.</span></span> |

> [!NOTE]
> <span data-ttu-id="946c9-218">เมตริกโดยละเอียดสำหรับปริมาณงานของ **AI** ยังไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="946c9-218">Detailed metrics for the **AI** workload are not yet available.</span></span>

## <a name="next-steps"></a><span data-ttu-id="946c9-219">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="946c9-219">Next steps</span></span>

<span data-ttu-id="946c9-220">หลังจากที่คุณทำความเข้าใจวิธีการตรวจสอบความจุของ Power BI Premium ลองเรียนรู้เพิ่มเติมเกี่ยวกับการปรับความจุให้เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="946c9-220">Now that you understand how to monitor Power BI Premium capacities, learn more about optimizing capacities.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="946c9-221">การปรับ Power BI Premium ให้เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="946c9-221">Optimizing Power BI Premium capacities</span></span>](service-premium-capacity-optimize.md)


<span data-ttu-id="946c9-222">Power BI ได้แนะนำ Power BI Premium Gen2 เข้ามาใช้งานเป็นข้อเสนอการแสดงตัวอย่าง ซึ่งปรับปรุงประสบการณ์การใช้งาน Power BI Premium ด้วยการปรับปรุงในสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="946c9-222">Power BI has introduced Power BI Premium Gen2 as a preview offering, which improves the Power BI Premium experience with improvements in the following:</span></span>
* <span data-ttu-id="946c9-223">ประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="946c9-223">Performance</span></span>
* <span data-ttu-id="946c9-224">สิทธิการใช้งานต่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="946c9-224">Per-user licensing</span></span>
* <span data-ttu-id="946c9-225">ขนาดใหญ่ขึ้น</span><span class="sxs-lookup"><span data-stu-id="946c9-225">Greater scale</span></span>
* <span data-ttu-id="946c9-226">เมตริกที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="946c9-226">Improved metrics</span></span>
* <span data-ttu-id="946c9-227">การปรับขนาดอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="946c9-227">Autoscaling</span></span>
* <span data-ttu-id="946c9-228">ลดค่าใช้จ่ายในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="946c9-228">Reduced management overhead</span></span>

<span data-ttu-id="946c9-229">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI Premium Gen2 โปรดดูที่ [Power BI Premium Generation 2 (ตัวอย่าง)](service-premium-what-is.md#power-bi-premium-generation-2-preview)</span><span class="sxs-lookup"><span data-stu-id="946c9-229">For more information about Power BI Premium Gen2, see [Power BI Premium Generation 2 (preview)](service-premium-what-is.md#power-bi-premium-generation-2-preview).</span></span>