---
title: แอปเมตริกความจุ Power BI Premium
description: เรียนรู้วิธีการใช้แอปเมตริกความจุ Power BI Premium เพื่อจัดการและแก้ไขปัญหาความจุพรีเมียมของคุณ
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-premium
ms.topic: how-to
ms.date: 11/11/2020
LocalizationGroup: Premium
ms.openlocfilehash: 6b214aacaeff0cc939af60b97d0c4781e1e4d36b
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413644"
---
# <a name="power-bi-premium-metrics-app"></a><span data-ttu-id="2c382-103">แอปเมตริกความจุ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="2c382-103">Power BI Premium Metrics app</span></span>

<span data-ttu-id="2c382-104">คุณสามารถใช้ **แอปเมตริกความจุ Power BI Premium** เพื่อจัดการประสิทธิภาพและความจุของการสมัครใช้งาน Power BI Premium ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="2c382-104">You can use the **Power BI Premium Metrics app** to manage the health and capacity of your Power BI Premium subscription.</span></span> <span data-ttu-id="2c382-105">ด้วยแอปนี้ ผู้ดูแลระบบใช้ **ศูนย์ประสิทธิภาพความจุ** ของแอปเพื่อดูและโต้ตอบกับตัวบ่งชี้ที่ตรวจสอบประสิทธิภาพของความจุพรีเมียมของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="2c382-105">With the app, administrators use the app's **Capacity health center** to see and interact with indicators that monitor the health of their premium capacity.</span></span> <span data-ttu-id="2c382-106">แอปเมตริกประกอบด้วยหน้าเริ่มต้นที่เรียกว่า **ศูนย์ประสิทธิภาพความจุ** และรายละเอียดเกี่ยวกับเมตริกสำคัญสามรายการ:</span><span class="sxs-lookup"><span data-stu-id="2c382-106">The Metrics app consists of the landing page, called the **Capacity Health Center**, and details about three important metrics:</span></span>

* <span data-ttu-id="2c382-107">หน่วยความจำที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="2c382-107">Active memory</span></span>
* <span data-ttu-id="2c382-108">การรอคิวรี</span><span class="sxs-lookup"><span data-stu-id="2c382-108">Query waits</span></span>
* <span data-ttu-id="2c382-109">การรอรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="2c382-109">Refresh waits</span></span>

![แอปเมตริกความจุ Power BI Premium](media/service-premium-metrics-app/premium-metrics-app-00.png)

<span data-ttu-id="2c382-111">ส่วนต่อไปนี้จะอธิบายในรายละเอียดของหน้าเริ่มต้นและหน้ารายงานเมตริกสามรายการ</span><span class="sxs-lookup"><span data-stu-id="2c382-111">The following sections describe the landing page, and the three metrics report pages, in detail.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="2c382-112">ถ้าความจุ Power BI Premium ของคุณกำลังประสบปัญหาการใช้ทรัพยากรสูงจนส่งผลให้เกิดปัญหาด้านประสิทธิภาพการทำงานหรือความมั่นคง คุณสามารถรับอีเมลแจ้งเตือนเพื่อทราบปัญหาและแก้ไขปัญหาได้</span><span class="sxs-lookup"><span data-stu-id="2c382-112">If your Power BI Premium capacity is experiencing high resource usage, resulting in performance or reliability issues, you can receive notification emails to identify and resolve the issue.</span></span> <span data-ttu-id="2c382-113">ซึ่งอาจเป็นวิธีที่มีประสิทธิภาพในการแก้ไขปัญหาความจุโอเวอร์โหลด</span><span class="sxs-lookup"><span data-stu-id="2c382-113">This can be a streamlined way to troubleshoot overloaded capacities.</span></span> <span data-ttu-id="2c382-114">คุณสามารถศึกษาข้อมูลเพิ่มเติมได้ที่[ความจุและการแจ้งเตือนความมั่นคง](service-interruption-notifications.md#capacity-and-reliability-notifications)</span><span class="sxs-lookup"><span data-stu-id="2c382-114">See [capacity and reliability notifications](service-interruption-notifications.md#capacity-and-reliability-notifications) for more information.</span></span>

> [!NOTE]
> <span data-ttu-id="2c382-115">Power BI Premium เพิ่งเปิดตัว Premium เวอร์ชันใหม่ชื่อ **Premium Gen2** ซึ่งกำลังอยู่ในช่วงการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="2c382-115">Power BI Premium recently released a new version of Premium, called **Premium Gen2**, which is currently in preview.</span></span> <span data-ttu-id="2c382-116">Premium Gen2 จะทำให้การจัดการความจุระดับพรีเมียมง่ายขึ้นและลดค่าใช้จ่ายในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="2c382-116">Premium Gen2 will simplify the management of Premium capacities, and reduce management overhead.</span></span> <span data-ttu-id="2c382-117">โดยเฉพาะอย่างยิ่งจะช่วยลดความจำเป็นในการเฝ้าติดตามระบบของผู้ดูแลเมตริก (CPU เท่านั้น) เพื่อให้มั่นใจถึงประสิทธิภาพและประสบการณ์ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2c382-117">In particular, it greatly reduces the metrics administrators must monitor (CPU only) to ensure performance and users’ experience.</span></span> <span data-ttu-id="2c382-118">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Power BI Premium Generation 2 (ตัวอย่าง)](service-premium-what-is.md#power-bi-premium-generation-2-preview)</span><span class="sxs-lookup"><span data-stu-id="2c382-118">For more information, see [Power BI Premium Generation 2 (preview)](service-premium-what-is.md#power-bi-premium-generation-2-preview).</span></span>


## <a name="premium-capacity-health-center"></a><span data-ttu-id="2c382-119">ศูนย์ประสิทธิภาพความจุพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="2c382-119">Premium capacity health center</span></span>

<span data-ttu-id="2c382-120">เมื่อคุณเปิด **แอปเมตริก Power BI Premium** คุณจะได้รับการแสดงผลด้วย **ศูนย์ประสิทธิภาพความจุ** ซึ่งแสดงภาพรวมของประสิทธิภาพของความจุ Power BI Premium ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2c382-120">When you open the **Power BI Premium metrics app** you're presented with the **Capacity health center**, which provides an overview of the health of your Power BI Premium capacity.</span></span>

![ศูนย์ประสิทธิภาพความจุในแอปเมตริกพรีเมียม](media/service-premium-metrics-app/premium-metrics-app-01.png)

<span data-ttu-id="2c382-122">จากหน้าเริ่มต้น คุณสามารถเลือกความจุ Power BI Premium ที่คุณต้องการดู ในกรณีที่องค์กรของคุณมีการสมัครใช้งาน Premium หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="2c382-122">From the landing page, you can select the Power BI Premium capacity you want to view, in case your organization has multiple Premium subscriptions.</span></span> <span data-ttu-id="2c382-123">หากต้องการดูความจุพรีเมียม ให้เลือกรายการดรอปดาวน์ที่อยู่ใกล้กับด้านบนของหน้า ซึ่งเรียกว่า **เลือกความจุเพื่อดูเมตริก**</span><span class="sxs-lookup"><span data-stu-id="2c382-123">To view a Premium capacity, select the dropdown near the top of the page called **Select a capacity to see its metrics**.</span></span>

<span data-ttu-id="2c382-124">KPI ทั้งสามรายการแสดงประสิทธิภาพปัจจุบันของความจุพรีเมียมที่เลือก โดยยึดตามการตั้งค่าที่ใช้กับแต่ละ KPI แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="2c382-124">The three KPIs show the current health of the selected Premium capacity, based on the settings applied to each of the three KPIs.</span></span> 

<span data-ttu-id="2c382-125">เมื่อต้องการดูรายละเอียดเกี่ยวกับ KPI แต่ละรายการ ให้เลือกปุ่ม **สำรวจ** ที่ด้านล่างของวิชวลของ KPI แต่ละรายการ และหน้ารายละเอียดจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="2c382-125">To view specifics about each KPI, select the **Explore** button at the bottom of each KPI's visual, and its detail page is displayed.</span></span> <span data-ttu-id="2c382-126">ส่วนต่อไปนี้อธิบาย KPI แต่ละรายการและรายละเอียดของเพจ</span><span class="sxs-lookup"><span data-stu-id="2c382-126">The following sections describe each KPI and the details its page provides.</span></span>

## <a name="the-active-memory-metric"></a><span data-ttu-id="2c382-127">เมตริกหน่วยความจำที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="2c382-127">The active memory metric</span></span>

<span data-ttu-id="2c382-128">เมตริก **หน่วยความจำที่ใช้งานอยู่** เป็นส่วนหนึ่งของประเภท *การวางแผนความจุ* ซึ่งเป็นตัวบ่งชี้ประสิทธิภาพที่ดีในการประเมินปริมาณการใช้ทรัพยากรของความจุของคุณสำหรับการใช้งาน เพื่อให้คุณสามารถปรับความจุตามที่จำเป็นในการวางแผนขนาดความจุ</span><span class="sxs-lookup"><span data-stu-id="2c382-128">The **active memory** metric is part of the *capacity planning* category, which is a good health indicator to evaluate your capacity's resource consumption for usage, so you can adjust the capacity as necessary to plan capacity scale.</span></span> 

![KPI หน่วยความจำที่ใช้งานอยู่](media/service-premium-metrics-app/premium-metrics-app-02.png)

<span data-ttu-id="2c382-130">**หน่วยความจำที่ใช้งานอยู่** คือหน่วยความจำที่ใช้ในการประมวลผลชุดข้อมูลที่กำลังใช้งานอยู่ในขณะนั้น และดังนั้นจึงไม่สามารถนำออกได้เมื่อต้องการหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="2c382-130">**Active memory** is the memory used to process datasets that are currently in use, and which therefore will not be evicted when memory is needed.</span></span> <span data-ttu-id="2c382-131">เมตริกหน่วยความจำที่ใช้งานอยู่จะระบุว่าความจุของคุณสามารถรองรับการโหลดเพิ่มเติม หรือมีความจุเข้าใกล้หรือเกินความจุการโหลดที่รับได้ในปัจจุบันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2c382-131">The active memory metric indicates whether your capacity can handle additional load, or of already nearing or over capacity, the capacity's current load.</span></span> <span data-ttu-id="2c382-132">หน่วยความจำที่ใช้งานอยู่ในขณะนี้ หมายความว่า มีหน่วยความจำที่พร้อมใช้งานน้อยลงเพื่อสนับสนุนการรีเฟรชและคิวรีเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2c382-132">The active memory currently being consumed means less memory is available to support additional refreshes and queries.</span></span> 

<span data-ttu-id="2c382-133">KPI ของ **หน่วยความจำที่ใช้งานอยู่** จะวัดจำนวนครั้งที่หน่วยความจำที่ใช้งานอยู่ของความจุข้ามเกณฑ์ 70% จำนวน 50 ครั้ง (ตัวกำหนดถูกตั้งค่าเป็น 30% ของเจ็ดวันที่ผ่านมา) ซึ่งแสดงให้เห็นว่าความจุกำลังจะใกล้จุดที่เมื่อผู้ใช้จะเริ่มพบปัญหาด้านประสิทธิภาพการทำงานของคิวรี</span><span class="sxs-lookup"><span data-stu-id="2c382-133">The **active memory** KPI measures how many times the capacity's active memory has crossed the 70% threshold 50 times (the marker is set to 30% of the last seven days), which indicates that the capacity is approaching a point when users may begin seeing performance issues with queries.</span></span>

<span data-ttu-id="2c382-134">วิชวลตัววัดที่แสดงในหัวข้อนี้แสดงให้เห็นว่าในเจ็ดวันที่ผ่านมาจากเวลาที่มีการรีเฟรชรายงานครั้งล่าสุด ความจุได้ข้ามเกณฑ์ 70% สี่ครั้ง แยกตามกลุ่มรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="2c382-134">The gauge visual shown in this section reveals that, in the last seven days from the time the report was last refreshed, the capacity has crossed the 70% threshold four times, split by hourly buckets.</span></span> <span data-ttu-id="2c382-135">ค่าสูงสุดของตัววัด 168 แสดงถึงเจ็ดวันที่ผ่านมาในหน่วยชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="2c382-135">The maximum value of the gauge, 168, represents the last seven days, in hours.</span></span>

<span data-ttu-id="2c382-136">หากต้องการเรียนรู้รายละเอียดของ KPI ของหน่วยความจำที่ใช้งานอยู่ คลิกที่ปุ่ม **สำรวจ** เพื่อดูหน้ารายงานที่มีการแสดงภาพเฉพาะของเมตริกรายละเอียด พร้อมด้วยคำแนะนำการแก้ไขปัญหาที่แสดงอยู่บนคอลัมน์ด้านขวาของหน้า</span><span class="sxs-lookup"><span data-stu-id="2c382-136">To learn the details of the active memory KPI, click the **Explore** button to see a report page that provides specific visualizations of its detailed metrics, along with a troubleshooting guide shown on the right column of the page.</span></span> 

<span data-ttu-id="2c382-137">มีสองสถานการณ์ที่มีการอธิบายประกอบ ซึ่งคุณสามารถแสดงบนหน้ารายงานได้โดยการเลือก **สถานการณ์ 1** หรือ **สถานการณ์ 2** บนหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="2c382-137">There are two scenarios explained, which you can show on the report page by selecting **Scenario 1** or **Scenario 2** on the page.</span></span> 

![สกรีนช็อตแสดงหน้ารายละเอียดหน่วยความจำที่ใช้งานอยู่](media/service-premium-metrics-app/premium-metrics-app-03.png)

<span data-ttu-id="2c382-139">คำแนะนำการแก้ไขปัญหาที่เกี่ยวข้องกับแต่ละสถานการณ์จะให้คำอธิบายโดยละเอียดเกี่ยวกับความหมายของเมตริก เพื่อที่คุณจะเข้าใจสถานะของความจุได้ดียิ่งขึ้นและทราบถึงสิ่งที่สามารถทำได้เพื่อลดปัญหาใดก็ตาม</span><span class="sxs-lookup"><span data-stu-id="2c382-139">The troubleshooting guides, associated with each scenario, provide detailed explanations about what the metrics mean, so you can better understand the state of the capacity, and what can be done to mitigate any issues.</span></span> 

<span data-ttu-id="2c382-140">สองสถานการณ์นั้นจะอธิบายไว้ในส่วนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2c382-140">Those two scenarios are described in the following sections.</span></span>

### <a name="scenario-one---current-load-is-too-high"></a><span data-ttu-id="2c382-141">สถานการณ์ที่หนึ่ง - การโหลดปัจจุบันสูงเกินไป</span><span class="sxs-lookup"><span data-stu-id="2c382-141">Scenario one - current load is too high</span></span> 

<span data-ttu-id="2c382-142">หากต้องการตรวจสอบว่ามีหน่วยความจำเพียงพอสำหรับความจุในการดำเนินการปริมาณงานที่มีหรือไม่ ให้ดูที่วิชวลแรกบนหน้า: **A: เปอร์เซ็นต์หน่วยความจำที่ใช้** ซึ่งแสดงหน่วยความจำที่ใช้โดยชุดข้อมูลที่กำลังประมวลผลอยู่ และดังนั้นจึงไม่นำออกได้</span><span class="sxs-lookup"><span data-stu-id="2c382-142">To determine whether there's enough memory for the capacity to complete its workloads, consult the first visual on the page: **A: Consumed Memory Percentages**, which displays the memory consumed by datasets that are being actively processed, and thus, cannot be evicted.</span></span>

<span data-ttu-id="2c382-143">ค่าเกณฑ์การแจ้งเตือน ซึ่งเป็นเส้นประสีแดง เป็นการบอกเหตุการณ์ของการใช้หน่วยความจำ 90%</span><span class="sxs-lookup"><span data-stu-id="2c382-143">The alarm threshold, which is the red dotted line, marks incidents of 90% memory consumption.</span></span>

<span data-ttu-id="2c382-144">ค่าเกณฑ์คำเตือน ซึ่งเป็นเส้นประสีเหลือง เป็นการบอกเหตุการณ์ของการใช้หน่วยความจำ 70%</span><span class="sxs-lookup"><span data-stu-id="2c382-144">The warning threshold, which is the yellow dotted line, marks incidents of 70% memory consumption.</span></span> 

<span data-ttu-id="2c382-145">เส้นประสีดำจะแสดงแนวโน้มการใช้หน่วยความจำโดยยึดตามการใช้งานหน่วยความจำของความจุปัจจุบันผ่านช่วงของเส้นเวลาของกราฟ</span><span class="sxs-lookup"><span data-stu-id="2c382-145">The black dotted line indicates the memory usage trendline, based on the current capacity's memory usage over the course of the graph timeline.</span></span>

<span data-ttu-id="2c382-146">การเกิดขึ้นบ่อยครั้งของหน่วยความจำที่ใช้งานอยู่เหนือค่าเกณฑ์การแจ้งเตือน (เส้นประสีแดง) และเส้นแนวโน้มหน่วยความจำ (เส้นประสีดำ) แสดงถึงความดันความจุหน่วยความจำซึ่งอาจป้องกันไม่ให้มีการโหลดชุดข้อมูลเพิ่มเติมลงในหน่วยความจำระหว่างเวลานั้น</span><span class="sxs-lookup"><span data-stu-id="2c382-146">High occurrences of active memory above the alarm threshold (red dotted line) and memory trendline (black dotted line) indicates memory capacity pressure, possibly preventing additional datasets from being loaded into memory during that time.</span></span> 

<span data-ttu-id="2c382-147">เมื่อคุณเห็นเหตุการณ์ดังกล่าว คุณควรดูที่แผนภูมิอื่นๆ บนหน้าอย่างละเอียดเพื่อพิจารณาให้มากขึ้นว่าเหตุการณ์เกิดขึ้นกับหน่วยความจำใดและสาเหตุใดที่ทำให้มีการใช้หน่วยความจำจำนวนมาก และหาวิธีการโหลดสมดุลหรือปรับให้เหมาะสม หรือต้องมีการเพิ่มขนาดความจุหากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="2c382-147">When you see such cases, you should look carefully at the other charts on the page to better determine what and why so much memory is so frequently being consumed, and how to load balance or optimize, or if necessary, scale up the capacity.</span></span> 

<span data-ttu-id="2c382-148">วิชวลที่สองบนหน้า **B: ชุดข้อมูลที่ใช้งานอยู่เป็นรายชั่วโมง** แสดงจำนวนสูงสุดของชุดข้อมูลที่โหลดในหน่วยความจำในกลุ่มรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="2c382-148">The second visual on the page, **B: Hourly loaded active datasets** displays the counts of the maximum number of datasets that were loaded in memory, in hourly buckets.</span></span> 

<span data-ttu-id="2c382-149">วิชวลที่สาม **C: สาเหตุที่ชุดข้อมูลในหน่วยความจำ** คือตารางที่แสดงรายการชุดข้อมูลตามชื่อพื้นที่ทำงาน ชื่อชุดข้อมูล ขนาดที่ไม่มีการบีบอัดในหน่วยความจำอธิบายเหตุผลที่จะโหลดในหน่วยความจำ (เช่นการรีเฟรชหรือการคิวรีหรือทั้งสองอย่าง)</span><span class="sxs-lookup"><span data-stu-id="2c382-149">The third visual, **C: Why datasets are in memory** is a table that lists the dataset by workspace name, dataset name, datasets uncompressed size in memory, explains the reason it's loaded in memory (such as, being refreshed or queried against, or both).</span></span>

#### <a name="diagnosing-scenario-one"></a><span data-ttu-id="2c382-150">วินิจฉัยสถานการณ์ที่หนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2c382-150">Diagnosing scenario one</span></span>

<span data-ttu-id="2c382-151">การใช้หน่วยความจำที่ใช้งานสูงที่สอดคล้องกันอาจส่งผลให้ชุดข้อมูลที่กำลังใช้งานถูกนำออก หรือป้องกันไม่ให้ชุดข้อมูลใหม่สามารถโหลดได้</span><span class="sxs-lookup"><span data-stu-id="2c382-151">Consistent high active memory utilization may result in forcing datasets that are actively being used to be evicted, or can prevent new datasets from able to load.</span></span> <span data-ttu-id="2c382-152">ขั้นตอนต่อไปนี้สามารถช่วยให้คุณวิเคราะห์ปัญหาได้</span><span class="sxs-lookup"><span data-stu-id="2c382-152">The following steps can help you diagnose problems</span></span>

1. <span data-ttu-id="2c382-153">ลองดูที่แผนภูมิ *A: เปอร์เซ็นต์ความจำที่ใช้*</span><span class="sxs-lookup"><span data-stu-id="2c382-153">Have a look at chart *A: Consumed memory percentages*</span></span>

    <span data-ttu-id="2c382-154">**a.**</span><span class="sxs-lookup"><span data-stu-id="2c382-154">**a.**</span></span> <span data-ttu-id="2c382-155">ถ้าแผนภูมิ A แสดงการข้ามเกณฑ์การแจ้งเตือน (90%) หลายครั้งและ/หรือหลายชั่วโมงติดต่อกันแล้ว ความจุของคุณกำลังทำงานในหน่วยความจำต่ำบ่อยครั้งเกินไป</span><span class="sxs-lookup"><span data-stu-id="2c382-155">If Chart A shows the alarm threshold (90%) is crossed many times and/or for consecutive hours, then your capacity is running low on memory too frequently.</span></span> <span data-ttu-id="2c382-156">ในแผนภูมิด้านล่าง เราจะเห็นว่ามีการข้ามค่าเกณฑ์คำเตือน (70%) สี่ครั้ง</span><span class="sxs-lookup"><span data-stu-id="2c382-156">In the chart below, we can see the warning threshold (70%) was crossed four times.</span></span>

    ![แผนภูมิ a เปอร์เซ็นต์ความจำที่ใช้](media/service-premium-metrics-app/premium-metrics-app-04.png)

    <span data-ttu-id="2c382-158">**b.**</span><span class="sxs-lookup"><span data-stu-id="2c382-158">**b.**</span></span> <span data-ttu-id="2c382-159">ชื่อแผนภูมิ *B: ชุดข้อมูลที่ใช้งานอยู่ซึ่งโหลดเป็นรายชั่วโมง* แสดงจำนวนสูงสุดของชุดข้อมูลที่ไม่ซ้ำกันที่โหลดในหน่วยความจำตามกลุ่มรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="2c382-159">The chart titled *B: Hourly loaded active datasets* shows the maximum number of unique datasets loaded in memory by hourly buckets.</span></span> <span data-ttu-id="2c382-160">การเลือกแถบในวิชวลจะข้ามตัวกรอง เหตุผลที่ชุดข้อมูลอยู่ในวิชวลหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="2c382-160">Selecting a bar in the visual will cross filter the reasons datasets are in memory visual.</span></span>  

    ![แผนภูมิ b ความจำที่ใช้เป็นชั่วโมง](media/service-premium-metrics-app/premium-metrics-app-05.png)     

    <span data-ttu-id="2c382-162">**c.**</span><span class="sxs-lookup"><span data-stu-id="2c382-162">**c.**</span></span> <span data-ttu-id="2c382-163">ดูตาราง **สาเหตุที่ชุดข้อมูลอยู่หน่วยความจำ** เพื่อดูรายการของชุดข้อมูลที่โหลดในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="2c382-163">Consult the **Why datasets are in memory** table to see a list of the datasets that were loaded in memory.</span></span> <span data-ttu-id="2c382-164">เรียงลำดับตาม *ขนาดชุดข้อมูล (MB)* เพื่อให้เห็นชุดข้อมูลที่มีการใช้หน่วยความจำมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="2c382-164">Sort by *Dataset Size (MB)* to highlight the datasets taking up the most memory.</span></span> <span data-ttu-id="2c382-165">การทำงานของความจุจะถูกจัดประเภทเป็นการทำงาน *แบบโต้ตอบ* หรือ *การทำงานแบบเบื้องหลัง*</span><span class="sxs-lookup"><span data-stu-id="2c382-165">Capacity operations are classified as either *interactive* or *background*.</span></span> <span data-ttu-id="2c382-166">การทำงานแบบโต้ตอบประกอบด้วยการแสดงคำขอ และการตอบสนองโต้ตอบกับผู้ใช้ (การกรอง การคิวรีถามตอบ และอีกมากมาย)</span><span class="sxs-lookup"><span data-stu-id="2c382-166">Interactive operations include rendering requests and responding to user interactions (filtering, Q&A querying, and so on).</span></span> <span data-ttu-id="2c382-167">คิวรีทั้งหมดและการรีเฟรชทั้งหมดให้ข้อมูลว่ามีการทำงานแบบโต้ตอบ (คิวรี) หนัก หรือการทำงานแบบเบื้องหลัง (รีเฟรช) ที่กระทำบนชุดข้อมูลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2c382-167">Total queries and total refreshes provide an idea of whether there are interactive (queries) heavy or background (refreshes) operations done on the dataset.</span></span> <span data-ttu-id="2c382-168">คุณจะต้องเข้าใจว่าการทำงานแบบโต้ตอบจะมีความสำคัญมากกว่าการทำงานแบบเบื้องหลัง เพื่อให้แน่ใจว่าผู้ใช้จะได้รับประสบการณ์การใช้งานที่ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="2c382-168">It's important to understand that interactive operations are always prioritized over background operations to ensure the best possible user experience.</span></span> <span data-ttu-id="2c382-169">ถ้ามีทรัพยากรไม่เพียงพอ การทำงานแบบเบื้องหลังจะถูกเพิ่มไปยังคิว และได้รับการประมวลผลเมื่อเพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2c382-169">If there are insufficient resources, background operations are added to a queue, and are processed once resources free up.</span></span> <span data-ttu-id="2c382-170">การทำงานแบบเบื้องหลัง เช่น การรีเฟรชชุดข้อมูลและฟังก์ชัน AI สามารถหยุดกลางกระบวนการได้โดยบริการของ Power BI และเพิ่มลงในคิว</span><span class="sxs-lookup"><span data-stu-id="2c382-170">Background operations, such as dataset refreshes and AI functions, can be stopped mid-process by the Power BI service and added to a queue.</span></span>
    
    ![ตาราง c รายการของชุดข้อมูล](media/service-premium-metrics-app/premium-metrics-app-06.png)  

#### <a name="remedies-for-scenario-one"></a><span data-ttu-id="2c382-172">การแก้ไขสำหรับสถานการณ์ที่หนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2c382-172">Remedies for scenario one</span></span>

<span data-ttu-id="2c382-173">คุณสามารถทำตามขั้นตอนต่อไปนี้เพื่อแก้ไขปัญหาที่เกี่ยวข้องกับสถานการณ์ที่หนึ่ง:</span><span class="sxs-lookup"><span data-stu-id="2c382-173">You can take the following steps to remedy the problems associated with scenario one:</span></span>

1. <span data-ttu-id="2c382-174">**เพิ่มขนาดความจุ** - เพิ่มขนาดความจุไปยัง SKU ถัดไปจะทำให้มีจำนวนหน่วยความจำที่มากกว่า SKU ปัจจุบันสองเท่า ทำให้บรรเทาความดันหน่วยความจำใดๆ ที่กำลังประสบอยู่</span><span class="sxs-lookup"><span data-stu-id="2c382-174">**Scale up the capacity** - scaling up the capacity to the next SKU will make available twice the amount of memory than the current SKU, thus alleviating any memory pressure the capacity is currently experiencing.</span></span>

2. <span data-ttu-id="2c382-175">**ย้ายชุดข้อมูลไปยังความจุอื่น** - ถ้าคุณมีความจุอื่นที่มีหน่วยความจำมากกว่า คุณสามารถย้ายพื้นที่ทำงานที่ประกอบด้วยชุดข้อมูลขนาดใหญ่ไปยังความจุนั้นได้</span><span class="sxs-lookup"><span data-stu-id="2c382-175">**Move datasets to another capacity** - if you have another capacity that has more memory available, you can move the workspaces that contain the larger datasets to that capacity.</span></span>


### <a name="scenario-two---future-load-will-exceed-limits"></a><span data-ttu-id="2c382-176">สถานการณ์ที่สอง - โหลดในอนาคตจะเกินขีดจำกัด</span><span class="sxs-lookup"><span data-stu-id="2c382-176">Scenario two - future load will exceed limits</span></span>

<span data-ttu-id="2c382-177">หากต้องการตรวจสอบว่ามีหน่วยความจำเพียงพอสำหรับความจุในการดำเนินการปริมาณงานที่มีหรือไม่ คุณสามารถอ้างอิงถึง **A: เปอร์เซ็นต์หน่วยความจำที่ใช้** วิชวลที่ด้านบนสุดของหน้า ซึ่งแสดงหน่วยความจำที่ใช้โดยชุดข้อมูลที่กำลังประมวลผลอยู่ และดังนั้นจึงนำออกไม่ได้</span><span class="sxs-lookup"><span data-stu-id="2c382-177">To determine whether there's enough memory for the capacity to complete its workloads, you can refer to the **A: Consumed Memory Percentages** visual on the top of the page, representing the memory consumed by datasets that are being actively processed so cannot be evicted.</span></span> <span data-ttu-id="2c382-178">เส้นประสีดำแสดงถึงแนวโน้ม</span><span class="sxs-lookup"><span data-stu-id="2c382-178">The black dotted line highlights the trends.</span></span> <span data-ttu-id="2c382-179">ในความจุที่มีความดันหน่วยความจำ วิชวลเดียวกันจะแสดงเส้นแนวโน้มหน่วยความจำ (เส้นประสีดำ) ที่เพิ่มขึ้นอย่างชัดเจน หมายความว่าอาจมีการป้องกันไม่ให้มีการโหลดชุดข้อมูลเพิ่มเติมลงในหน่วยความจำระหว่างเวลานั้น</span><span class="sxs-lookup"><span data-stu-id="2c382-179">In a capacity experiencing memory pressure, the same visual will clearly show the memory trendline (black dotted line) upwards, meaning that it is possibly preventing additional datasets from being loaded into memory at that point in time.</span></span> <span data-ttu-id="2c382-180">เส้นแนวโน้ม หรือเส้นประสีดำนั้น จะแสดงแนวโน้มของการเติบโตโดยยึดตามข้อมูลเจ็ดวัน</span><span class="sxs-lookup"><span data-stu-id="2c382-180">The trend line, the black dashed line, shows the trend of growth based on the seven days of data.</span></span> 

![สกรีนช็อตแสดงหน้ารายละเอียดหน่วยความจำที่ใช้งานอยู่สำหรับสถานการณ์ที่สอง](media/service-premium-metrics-app/premium-metrics-app-07.png)

#### <a name="diagnosing-scenario-two"></a><span data-ttu-id="2c382-182">วินิจฉัยสถานการณ์ที่สอง</span><span class="sxs-lookup"><span data-stu-id="2c382-182">Diagnosing scenario two</span></span>

<span data-ttu-id="2c382-183">ในการวินิจฉัยสถานการณ์ที่สอง ให้พิจารณาดูว่าเส้นแนวโน้มแสดงแนวโน้มขึ้นไปยังค่าเกณฑ์คำเตือนหรือการแจ้งเตือนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2c382-183">To diagnose scenario two, determine if the trend line is showing an upward trend towards warning or alarm thresholds.</span></span> 

1. <span data-ttu-id="2c382-184">พิจารณา **แผนภูมิ A:**</span><span class="sxs-lookup"><span data-stu-id="2c382-184">Consider **Chart A:**</span></span>

    ![กราฟความจำที่ใช้](media/service-premium-metrics-app/premium-metrics-app-08.png)

    <span data-ttu-id="2c382-186">**a.**</span><span class="sxs-lookup"><span data-stu-id="2c382-186">**a.**</span></span> <span data-ttu-id="2c382-187">ถ้าแผนภูมิแสดงความชันที่มีแนวโน้มเพิ่มขึ้น แสดงให้เห็นว่าปริมาณการใช้หน่วยความจำนั้นเพิ่มขึ้นในช่วงเจ็ดวันที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="2c382-187">If the chart shows an upward slope, that indicates that memory consumption has increased over the past seven days.</span></span>

    <span data-ttu-id="2c382-188">**b.**</span><span class="sxs-lookup"><span data-stu-id="2c382-188">**b.**</span></span> <span data-ttu-id="2c382-189">สมมติว่ามีการเติบโตในปัจจุบันและทำนายเมื่อเส้นแนวโน้มข้ามค่าเกณฑ์การเตือน (เส้นประสีเหลือง)</span><span class="sxs-lookup"><span data-stu-id="2c382-189">Assume the current growth, and predict when the trend line will cross the warning threshold (the yellow dashed line).</span></span>

    <span data-ttu-id="2c382-190">**c.**</span><span class="sxs-lookup"><span data-stu-id="2c382-190">**c.**</span></span> <span data-ttu-id="2c382-191">ให้ตรวจสอบเส้นแนวโน้มอย่างน้อยทุกสองวันเพื่อดูว่ายังคงมีแนวโน้มต่อเนื่องหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2c382-191">Keep checking the trend line at least every two days, to see if the trend continuing.</span></span>

#### <a name="remedies-for-scenario-two"></a><span data-ttu-id="2c382-192">การแก้ไขสำหรับสถานการณ์ที่สอง</span><span class="sxs-lookup"><span data-stu-id="2c382-192">Remedies for scenario two</span></span>

<span data-ttu-id="2c382-193">คุณสามารถทำตามขั้นตอนต่อไปนี้เพื่อแก้ไขปัญหาที่เกี่ยวข้องกับสถานการณ์ที่สอง:</span><span class="sxs-lookup"><span data-stu-id="2c382-193">You can take the following steps to remedy the problems associated with scenario two:</span></span>

1. <span data-ttu-id="2c382-194">**เพิ่มขนาดความจุ** - เพิ่มขนาดความจุไปยัง SKU ถัดไปจะทำให้มีจำนวนหน่วยความจำที่มากกว่า SKU ปัจจุบันสองเท่า ทำให้บรรเทาความดันหน่วยความจำใดๆ ที่กำลังประสบอยู่</span><span class="sxs-lookup"><span data-stu-id="2c382-194">**Scale up the capacity** - scaling up the capacity to the next SKU will make available twice the amount of memory than the current SKU, thus alleviating any memory pressure the capacity is currently experiencing.</span></span>

2. <span data-ttu-id="2c382-195">**ย้ายชุดข้อมูลไปยังความจุอื่น** - ถ้าคุณมีความจุอื่นที่มีหน่วยความจำมากกว่า คุณสามารถย้ายพื้นที่ทำงานที่ประกอบด้วยชุดข้อมูลขนาดใหญ่ไปยังความจุนั้นได้</span><span class="sxs-lookup"><span data-stu-id="2c382-195">**Move datasets to another capacity** - if you have another capacity that has more memory available, you can move the workspaces that contain the larger datasets to that capacity.</span></span>


## <a name="the-query-waits-metric"></a><span data-ttu-id="2c382-196">เมตริกการรอคิวรี</span><span class="sxs-lookup"><span data-stu-id="2c382-196">The query waits metric</span></span>

<span data-ttu-id="2c382-197">ประเภท **คิวรี** ระบุว่าผู้ใช้สามารถพบวิชวลรายงานที่ตอบสนองช้าหรือไม่มีการตอบสนองหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2c382-197">The **Queries** category indicates whether users could experience report visuals that are slow to respond, or could become unresponsive.</span></span> <span data-ttu-id="2c382-198">**การรอคิวรี** คือเวลาที่คิวรีใช้เพื่อเริ่มต้นการดำเนินการจากเวลาที่ทริกเกอร์</span><span class="sxs-lookup"><span data-stu-id="2c382-198">**Query waits** is the time the query takes to start execution from the time it was triggered.</span></span> <span data-ttu-id="2c382-199">KPI นี้จะวัดว่าคิวรีของความจุที่เลือกไว้จำนวน 25% หรือมากกว่ากำลังรอเป็นเวลา 100 มิลลิวินาทีหรือนานกว่านั้นในการปฏิบัติการ</span><span class="sxs-lookup"><span data-stu-id="2c382-199">This KPI measures whether 25% or more of the selected capacity's queries are waiting 100 milliseconds or longer to execute.</span></span> <span data-ttu-id="2c382-200">การรอคิวรีเกิดขึ้นเมื่อมี CPU ที่พร้อมใช้งานไม่เพียงพอที่จะดำเนินการคิวรีที่รอดำเนินการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2c382-200">Query waits occur when there's not enough available CPU to execute all pending queries.</span></span> 

![ตัววัดการรอคิวรี](media/service-premium-metrics-app/premium-metrics-app-09.png)

<span data-ttu-id="2c382-202">ตัววัดในวิชวลนี้แสดงให้เห็นว่าในเจ็ดวันล่าสุดจากเวลาที่มีการรีเฟรชรายงานครั้งสุดท้าย 17.32% ของคิวรีมีการรอมากกว่า 100 มิลลิวินาที</span><span class="sxs-lookup"><span data-stu-id="2c382-202">The gauge in this visual shows that in the last seven days from the time the report was last refreshed, 17.32% of the queries waited more than 100 milliseconds.</span></span> 

<span data-ttu-id="2c382-203">เมื่อต้องการเรียนรู้รายละเอียดของ KPI การรอคิวรี ให้คลิกปุ่ม **สำรวจ** เพื่อแสดงหน้ารายงานที่มีการแสดงภาพของเมตริกที่เกี่ยวข้องและคำแนะนำการแก้ไขปัญหาในคอลัมน์ด้านขวาของหน้า</span><span class="sxs-lookup"><span data-stu-id="2c382-203">To learn details of Query waits KPI, click the **Explore** button to display a report page with visualization of relevant metrics, and a troubleshooting guide in the right column of the page.</span></span> <span data-ttu-id="2c382-204">คำแนะนำการแก้ไขปัญหามีสองสถานการณ์ แต่ละรายการจะให้คำอธิบายโดยละเอียดของเมตริก สถานะของความจุ และสิ่งที่คุณสามารถทำเพื่อลดปัญหา</span><span class="sxs-lookup"><span data-stu-id="2c382-204">The troubleshooting guide has two scenarios, each providing detailed explanations of the metric, the state of the capacity, and what you can do to mitigate the issue.</span></span>

<span data-ttu-id="2c382-205">ในลำดับต่อไป เราพูดคุยถึงสถานการณ์การรอคิวรีแต่ละสถานการณ์ในส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="2c382-205">We discuss each query waits scenario, in turn, in the following sections.</span></span>

### <a name="scenario-one---long-running-queries-consume-cpu"></a><span data-ttu-id="2c382-206">สถานการณ์ที่หนึ่ง - คิวรีการเรียกใช้ที่นานใช้พื้นที่ CPU</span><span class="sxs-lookup"><span data-stu-id="2c382-206">Scenario one - long running queries consume CPU</span></span>

<span data-ttu-id="2c382-207">ในสถานการณ์ที่หนึ่ง คิวรีการเรียกใช้ที่นานนั้นใช้พื้นที่ CPU มากเกินไป</span><span class="sxs-lookup"><span data-stu-id="2c382-207">In scenario one, long running queries are taking up too much CPU.</span></span> 

<span data-ttu-id="2c382-208">คุณสามารถตรวจสอบว่าประสิทธิภาพการทำงานของรายงานที่ต่ำนั้นเกิดจากความจุที่โอเวอร์โหลดหรือเนื่องจากชุดข้อมูลหรือรายงานที่ได้รับการออกแบบไม่ดี</span><span class="sxs-lookup"><span data-stu-id="2c382-208">You can investigate whether poor report performance is caused by an overloaded capacity, or due to a poorly designed dataset or report.</span></span> <span data-ttu-id="2c382-209">มีหลายสาเหตุที่ทำให้คิวรีสามารถเรียกใช้ได้เป็นระยะเวลายาวนาน ซึ่งหมายความว่าใช้เวลามากกว่า 10 วินาทีในการดำเนินการจนเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="2c382-209">There are several reasons why a query can run for an extended period, which is defined as taking more than 10 seconds to finish executing.</span></span> <span data-ttu-id="2c382-210">ขนาดชุดข้อมูลและความซับซ้อน เช่นเดียวกับความซับซ้อนของคิวรี เป็นเพียงตัวอย่างบางส่วนของสิ่งที่สามารถทำให้เกิดการเรียกใช้คิวรีเป็นเวลานานได้</span><span class="sxs-lookup"><span data-stu-id="2c382-210">Dataset size and complexity, as well as query complexity are just a few examples of what can cause a long running query.</span></span> 

<span data-ttu-id="2c382-211">บนหน้ารายงาน วิชวลดังต่อไปนี้จะปรากฏขึ้น:</span><span class="sxs-lookup"><span data-stu-id="2c382-211">On the report page, the following visuals appear:</span></span> 

* <span data-ttu-id="2c382-212">ชื่อตารางบนสุด **A: เวลาการรอสูง** แสดงรายการชุดข้อมูลที่มีคิวรีที่กำลังรออยู่</span><span class="sxs-lookup"><span data-stu-id="2c382-212">The top table titled **A: High wait times** lists the datasets with queries that are waiting.</span></span> 
* <span data-ttu-id="2c382-213">**B: การกระจายเวลาการรอสูงรายชั่วโมง** แสดงการกระจายของเวลาการรอสูง</span><span class="sxs-lookup"><span data-stu-id="2c382-213">**B: Hourly high wait time distributions** shows the distribution of high wait times.</span></span> 
* <span data-ttu-id="2c382-214">ชื่อแผนภูมิ **C: จำนวนคิวแบบยาวรายชั่วโมง** แสดงจำนวนคิวรีการเรียกใช้ที่นานที่ได้รับการดำเนินการ แยกตามกลุ่มรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="2c382-214">The chart titled **C: Hourly long query counts** displays the count of long running queries that were executed split by hourly buckets.</span></span>
* <span data-ttu-id="2c382-215">วิชวลสุดท้าย ตาราง **D: คิวรีการเรียกใช้ที่นาน** แสดงรายการคิวรีการเรียกใช้ที่นานและสถิติ</span><span class="sxs-lookup"><span data-stu-id="2c382-215">The last visual, table **D: Long running queries**, lists the long running queries and their stats.</span></span>

![หน้ารายละเอียดการรอคิวรี](media/service-premium-metrics-app/premium-metrics-app-10.png)

<span data-ttu-id="2c382-217">มีขั้นตอนที่คุณสามารถใช้เพื่อวินิจฉัยและแก้ไขปัญหาของเวลาการรอคิวรี โดยอธิบายไว้ในตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="2c382-217">There are steps you can take to diagnose and remedy issues with query wait times, described next.</span></span>

#### <a name="diagnosing-scenario-one"></a><span data-ttu-id="2c382-218">วินิจฉัยสถานการณ์ที่หนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2c382-218">Diagnosing scenario one</span></span>

<span data-ttu-id="2c382-219">อันดับแรก คุณสามารถพิจารณาดูได้ว่าคิวรีการเรียกใช้ที่นานเกิดขึ้นขณะที่คิวรีของคุณอยู่ในระหว่างการรออยู่</span><span class="sxs-lookup"><span data-stu-id="2c382-219">First, you can determine if long running queries are occurring when your queries are waiting.</span></span> 

![ตารางเวลาการรอสูง](media/service-premium-metrics-app/premium-metrics-app-11.png)

<span data-ttu-id="2c382-221">ดู **แผนภูมิ B** ซึ่งแสดงจำนวนคิวรีที่มีการรอมากกว่า 100 มิลลิวินาที</span><span class="sxs-lookup"><span data-stu-id="2c382-221">Look at **Chart B**, which shows the count of queries that are waiting more than 100 ms.</span></span> <span data-ttu-id="2c382-222">เลือกหนึ่งคอลัมน์ที่แสดงการรอในระดับสูง</span><span class="sxs-lookup"><span data-stu-id="2c382-222">Select one of the columns that shows a high number of waits.</span></span>

![การกระจายเวลาการรอสูง](media/service-premium-metrics-app/premium-metrics-app-12.png)

<span data-ttu-id="2c382-224">เมื่อคุณคลิกที่คอลัมน์ที่มีเวลาการรอสูง **แผนภูมิ C** มีการกรองเพื่อแสดงจำนวนคิวรีที่มีการเรียกใช้ที่นานที่ดำเนินการในช่วงเวลานั้น ซึ่งแสดงในรูปต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2c382-224">When you click on a column with high wait times, **Chart C** is filtered to show the count of long-running queries that executed during that time, shown in the following image:</span></span>

![จำนวนคิวรีแบบยาวรายชั่วโมง](media/service-premium-metrics-app/premium-metrics-app-13.png)

<span data-ttu-id="2c382-226">และนอกจากนี้ยังมีการกรอง **แผนภูมิ D** เพื่อแสดงคิวรีที่ทำงานอยู่ในระหว่างช่วงเวลาที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="2c382-226">And in addition, **Chart D** is also filtered to show the queries that were long running during that selected time period.</span></span>

![คิวรีการเรียกใช้ที่นาน](media/service-premium-metrics-app/premium-metrics-app-14.png)

#### <a name="remedies-for-scenario-one"></a><span data-ttu-id="2c382-228">การแก้ไขสำหรับสถานการณ์ที่หนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2c382-228">Remedies for scenario one</span></span>

<span data-ttu-id="2c382-229">นี่คือขั้นตอนที่คุณสามารถใช้เพื่อแก้ไขปัญหาจากสถานการณ์ที่หนึ่ง:</span><span class="sxs-lookup"><span data-stu-id="2c382-229">Here are steps you can take to remedy issues from scenario one:</span></span>

1. <span data-ttu-id="2c382-230">**เรียกใช้ PerfAnalyzer เพื่อปรับรายงานและชุดข้อมูลให้เหมาะสม** - ตัววิเคราะห์ประสิทธิภาพสำหรับรายงานจะแสดงผลของการโต้ตอบทั้งหมดบนหน้า รวมถึงระยะเวลาที่แต่ละวิชวลใช้ในการรีเฟรชและตำแหน่งที่ใช้เวลานั้น</span><span class="sxs-lookup"><span data-stu-id="2c382-230">**Run PerfAnalyzer to optimize reports and datasets** - the performance analyzer for reports will show the effect of every interaction on a page, including how long each visual takes to refresh and where the time is spent.</span></span>

2. <span data-ttu-id="2c382-231">**เพิ่มขนาดความจุ** - เพิ่มขนาดความจุไปยัง SKU ถัดไปจะทำให้มีจำนวน CPU พร้อมใช้งานเพิ่มเป็นสองเท่า ทำให้บรรเทาความดัน CPU ใดๆ ที่อาจทำให้คิวรีเรียกใช้งานนานได้</span><span class="sxs-lookup"><span data-stu-id="2c382-231">**Scale up the capacity** - scaling up the capacity to the next SKU will make available twice the amount of CPU thus alleviating any CPU pressure that may be causing the queries to run longer.</span></span>

3. <span data-ttu-id="2c382-232">**ย้ายชุดข้อมูลไปยังความจุอื่น** - ถ้าคุณมีความจุอื่นที่มี CPU มากกว่า คุณสามารถย้ายพื้นที่ทำงานที่ประกอบด้วยชุดข้อมูลที่มีคิวรีที่กำลังรออยู่ไปยังความจุอื่นได้</span><span class="sxs-lookup"><span data-stu-id="2c382-232">**Move datasets to another capacity** - if you have another capacity that has more CPU available, you can move the workspaces that contain the datasets that contain the queries that are waiting to the other capacity.</span></span>

### <a name="scenario-two---too-many-queries"></a><span data-ttu-id="2c382-233">สถานการณ์ที่สอง - จำนวนคิวรีมากเกินไป</span><span class="sxs-lookup"><span data-stu-id="2c382-233">Scenario two - too many queries</span></span>

<span data-ttu-id="2c382-234">ในสถานการณ์ที่สอง มีคิวรีที่ใช้งานอยู่มากเกินไป</span><span class="sxs-lookup"><span data-stu-id="2c382-234">In scenario two, too many queries are executing.</span></span>

<span data-ttu-id="2c382-235">เมื่อจำนวนคิวรีที่จะดำเนินการเกินขีดจำกัดของความจุ คิวรีจะถูกวางอยู่ในคิวจนกว่าแหล่งข้อมูลจะพร้อมใช้งานในการดำเนินการดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="2c382-235">When the number of queries to execute exceeds the limits of the capacity, queries are placed in a queue until resources are available to execute them.</span></span> <span data-ttu-id="2c382-236">ถ้าขนาดของคิวขยายใหญ่เกินไป คิวรีในคิวนั้นสามารถรออยู่ได้มากกว่า 100 มิลลิวินาที</span><span class="sxs-lookup"><span data-stu-id="2c382-236">If the size of the queue grows too large, queries in that queue can end up waiting more than 100 milliseconds.</span></span>

![สถานการณ์ที่สอง](media/service-premium-metrics-app/premium-metrics-app-15.png)


#### <a name="diagnosing-scenario-two"></a><span data-ttu-id="2c382-238">วินิจฉัยสถานการณ์ที่สอง</span><span class="sxs-lookup"><span data-stu-id="2c382-238">Diagnosing scenario two</span></span>

<span data-ttu-id="2c382-239">จาก **ตาราง  A** เลือกชุดข้อมูลที่มีเปอร์เซ็นต์ของเวลาการรอสูง</span><span class="sxs-lookup"><span data-stu-id="2c382-239">From **Table A** select a dataset that has a high percentage of wait time.</span></span>

![ตารางเวลาการรอสูง](media/service-premium-metrics-app/premium-metrics-app-16.png)

<span data-ttu-id="2c382-241">เมื่อคุณได้เลือกชุดข้อมูลที่มีเวลาการรอสูงแล้ว **แผนภูมิ B** มีการกรองเพื่อแสดงการกระจายเวลารอสำหรับคิวรีบนชุดข้อมูลนั้นในช่วงเจ็ดวันที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="2c382-241">Once you've selected a dataset with a high wait time, **Chart B** is filtered to show the wait time distributions for queries on that dataset, over the past seven days.</span></span> <span data-ttu-id="2c382-242">ถัดไป เลือกหนึ่งคอลัมน์จาก **แผนภูมิ B**</span><span class="sxs-lookup"><span data-stu-id="2c382-242">Next, select one of the columns from **Chart B**.</span></span>

![แผนภูมิการกระจายเวลาการรอสูงรายชั่วโมง](media/service-premium-metrics-app/premium-metrics-app-17.png)

<span data-ttu-id="2c382-244">**แผนภูมิ C** จะถูกกรองเพื่อแสดงความยาวของคิวในเวลาที่เลือกจากแผนภูมิ B</span><span class="sxs-lookup"><span data-stu-id="2c382-244">**Chart C** is then filtered to show the queue length at the time selected from Chart B.</span></span>

![ความยาวคิวของคิวรีรายชั่วโมง](media/service-premium-metrics-app/premium-metrics-app-18.png)

<span data-ttu-id="2c382-246">ถ้าความยาวของคิวได้ข้ามขีดจำกัดของ 20 แล้ว อาจเป็นไปได้ว่าคิวรีในชุดข้อมูลที่เลือกจะเกิดความล่าช้า เนื่องจากมีคิวรีมากเกินไปที่พยายามดำเนินการในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="2c382-246">If the length of the queue has crossed the threshold of 20, then it's likely that the queries in the selected dataset are delayed, due to too many queries trying to execute at the same time.</span></span>

![ตารางคิวรีกำลังดำเนินการ](media/service-premium-metrics-app/premium-metrics-app-19.png)

#### <a name="remedies-for-scenario-two"></a><span data-ttu-id="2c382-248">การแก้ไขสำหรับสถานการณ์ที่สอง</span><span class="sxs-lookup"><span data-stu-id="2c382-248">Remedies for scenario two</span></span>

<span data-ttu-id="2c382-249">คุณสามารถทำตามขั้นตอนต่อไปนี้เพื่อแก้ไขปัญหาที่เกี่ยวข้องกับสถานการณ์ที่สอง:</span><span class="sxs-lookup"><span data-stu-id="2c382-249">You can take the following steps to remedy the problems associated with scenario two:</span></span>

1. <span data-ttu-id="2c382-250">**เพิ่มขนาดความจุ** - เพิ่มขนาดความจุไปยัง SKU ถัดไปจะทำให้มีจำนวนหน่วยความจำที่มากกว่า SKU ปัจจุบันสองเท่า ทำให้บรรเทาความดันหน่วยความจำใดๆ ที่กำลังประสบอยู่</span><span class="sxs-lookup"><span data-stu-id="2c382-250">**Scale up the capacity** - scaling up the capacity to the next SKU will make available twice the amount of memory than the current SKU, thus alleviating any memory pressure the capacity is currently experiencing.</span></span>

2. <span data-ttu-id="2c382-251">**ย้ายชุดข้อมูลไปยังความจุอื่น** - ถ้าคุณมีความจุอื่นที่มีหน่วยความจำมากกว่า คุณสามารถย้ายพื้นที่ทำงานที่ประกอบด้วยชุดข้อมูลขนาดใหญ่ไปยังความจุนั้นได้</span><span class="sxs-lookup"><span data-stu-id="2c382-251">**Move datasets to another capacity** - if you have another capacity that has more memory available, you can move the workspaces that contain the larger datasets to that capacity.</span></span>


## <a name="the-refresh-waits-metric"></a><span data-ttu-id="2c382-252">เมตริกการรอรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="2c382-252">The refresh waits metric</span></span>

<span data-ttu-id="2c382-253">เมตริก **การรอรีเฟรช** จะให้ข้อมูลเชิงลึกในเวลาที่ผู้ใช้อาจประสบข้อมูลรายงานที่เก่าหรือค้างอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="2c382-253">The **Refresh waits** metric provides insights to when users could be experiencing report data that's old or stale.</span></span> <span data-ttu-id="2c382-254">**การรอรีเฟรช** คือเวลาที่การรีเฟรชข้อมูลรอเพื่อเริ่มต้นการดำเนิน การจากเวลาที่ถูกทริกเกอร์ตามความต้องการหรือกำหนดเวลาให้เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="2c382-254">**Refresh waits** is the time a given data refresh waited to start execution, from the time it was triggered on demand, or scheduled to run.</span></span> <span data-ttu-id="2c382-255">KPI นี้จะวัดค่าว่ามีการรอการรีเฟรชที่ค้างอยู่ 10% หรือมากกว่าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2c382-255">This KPI measures whether 10% or more of pending refresh requests are waiting 10 minutes or longer.</span></span> <span data-ttu-id="2c382-256">โดยทั่วไปแล้วจะเกิดการรอขึ้นเมื่อมีหน่วยความจำหรือ CPU ที่พร้อมใช้งานไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="2c382-256">Waiting generally occurs when there's insufficient available memory or CPU.</span></span>

![ตัววัดการรอรีเฟรช](media/service-premium-metrics-app/premium-metrics-app-20.png)

<span data-ttu-id="2c382-258">ตัววัดนี้แสดงให้เห็นว่าในเจ็ดวันที่ผ่านมาจากการรีเฟรชรายงานครั้งล่าสุด 3.18% ของรีเฟรชมีการรอมากกว่า 10 นาที</span><span class="sxs-lookup"><span data-stu-id="2c382-258">This gauge shows that in the last seven days from the last refresh report refresh, 3.18% of the refreshes waited more than 10 minutes.</span></span> 

<span data-ttu-id="2c382-259">เมื่อต้องการเรียนรู้รายละเอียดของ KPI **การรอรีเฟรช**  ให้คลิกปุ่ม **สำรวจ** ซึ่งแสดงหน้าที่มีเมตริกและคำแนะนำการแก้ไขปัญหาบนคอลัมน์ด้านขวาของหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="2c382-259">To learn the details of the **Refresh waits** KPI, click the **Explore** button, which presents a page with metrics and a troubleshooting guide on the right column of the report page.</span></span> <span data-ttu-id="2c382-260">คำแนะนำให้คำอธิบายอย่างละเอียดเกี่ยวกับเมตริกบนหน้า และช่วยให้คุณเข้าใจสถานะของความจุ และสิ่งที่คุณสามารถทำเพื่อลดปัญหาใดก็ตาม</span><span class="sxs-lookup"><span data-stu-id="2c382-260">The guide provides detailed explanations about the metrics on the page, and helps you  understand the state of the capacity, and what you can do to mitigate any issues.</span></span>

![เมตริกการสำรวจการรอรีเฟรช](media/service-premium-metrics-app/premium-metrics-app-21.png)

<span data-ttu-id="2c382-262">มีสองสถานการณ์ที่มีการอธิบายประกอบ ซึ่งคุณสามารถแสดงบนหน้ารายงานได้โดยการเลือก สถานการณ์ 1 หรือ สถานการณ์ 2 บนหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="2c382-262">There are two scenarios explained, which you can show on the report page by selecting Scenario 1 or Scenario 2 on the page.</span></span> <span data-ttu-id="2c382-263">ในลำดับต่อไป เราพูดคุยถึงสถานการณ์แต่ละสถานการณ์ในส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="2c382-263">We discuss each scenario in turn, in the following sections.</span></span>

### <a name="scenario-one---not-enough-memory"></a><span data-ttu-id="2c382-264">สถานการณ์ที่หนึ่ง - หน่วยความจำไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="2c382-264">Scenario one - not enough memory</span></span>

<span data-ttu-id="2c382-265">ในสถานการณ์ที่หนึ่ง มีหน่วยความจำไม่เพียงพอที่จะโหลดชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2c382-265">In scenario one, there isn't enough available memory to load the dataset.</span></span> <span data-ttu-id="2c382-266">มีสองสถานการณ์ที่ทำให้เกิดการรีเฟรชการจำกัดผลลัพธ์ระหว่างสภาวะที่หน่วยความจำเหลือน้อย:</span><span class="sxs-lookup"><span data-stu-id="2c382-266">There are two situations that result in a refresh being throttled during low memory conditions:</span></span>

1. <span data-ttu-id="2c382-267">ความจำไม่เพียงพอในการโหลดชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2c382-267">Not enough memory to load the dataset.</span></span>
2. <span data-ttu-id="2c382-268">การรีเฟรชถูกยกเลิกเนื่องจากการดำเนินการที่มีลำดับความสำคัญสูงกว่า</span><span class="sxs-lookup"><span data-stu-id="2c382-268">The refresh was canceled due to a higher priority operation.</span></span> 

<span data-ttu-id="2c382-269">ลำดับความสำคัญสำหรับการโหลดชุดข้อมูลมีดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2c382-269">The priority for loading datasets is the following:</span></span>

1. <span data-ttu-id="2c382-270">คิวรีแบบโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="2c382-270">Interactive query</span></span>
2. <span data-ttu-id="2c382-271">รีเฟรชตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="2c382-271">On-demand refresh</span></span>
3. <span data-ttu-id="2c382-272">รีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="2c382-272">Scheduled refresh</span></span>

<span data-ttu-id="2c382-273">ถ้ามีหน่วยความจำไม่เพียงพอในการโหลดชุดข้อมูลสำหรับคิวรีแบบโต้ตอบ การรีเฟรชตามกำหนดการจะหยุดและชุดข้อมูลจะถูกยกเลิกการโหลดจนกว่าจะมีหน่วยความจำพร้อมใช้งานที่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="2c382-273">If there isn't enough memory to load a dataset for an interactive query, scheduled refreshes are stopped and their datasets unloaded until sufficient memory become available.</span></span> <span data-ttu-id="2c382-274">ถ้าไม่ได้เพิ่มหน่วยความจำเพียงพอแล้ว การรีเฟรชตามความต้องการจะหยุดลงและชุดข้อมูลจะถูกยกเลิกการโหลด</span><span class="sxs-lookup"><span data-stu-id="2c382-274">If that doesn't free up enough memory, then on-demand refreshes are stopped and their datasets are unloaded.</span></span>

#### <a name="diagnosing-scenario-one"></a><span data-ttu-id="2c382-275">วินิจฉัยสถานการณ์ที่หนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2c382-275">Diagnosing scenario one</span></span>

<span data-ttu-id="2c382-276">ในการวิเคราะห์สถานการณ์ที่หนึ่ง อันดับแรกคือให้พิจารณาว่าการจำกัดผลลัพธ์เกิดจากหน่วยความจำที่ไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="2c382-276">To diagnose scenario one, first determine whether throttling is due to insufficient memory.</span></span> <span data-ttu-id="2c382-277">ขั้นตอนในการทำมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2c382-277">The steps to do so are the following.</span></span>

1. <span data-ttu-id="2c382-278">เลือกชุดข้อมูลที่คุณสนใจจาก **ตาราง  A** ด้วยการคลิกที่ตาราง:</span><span class="sxs-lookup"><span data-stu-id="2c382-278">Select the dataset you're interested in from **Table A** by clicking on it:</span></span> 

    ![ตาราง  A](media/service-premium-metrics-app/premium-metrics-app-22.png)

    <span data-ttu-id="2c382-280">a.</span><span class="sxs-lookup"><span data-stu-id="2c382-280">a.</span></span> <span data-ttu-id="2c382-281">เมื่อมีการเลือกชุดข้อมูลใน **ตาราง A** **แผนภูมิ B** จะถูกกรองเพื่อแสดงเวลาเมื่อมีการรอเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="2c382-281">When a dataset is selected in **Table A**, **Chart B** is filtered to show when waiting occurred.</span></span>

    ![แผนภูมิ B](media/service-premium-metrics-app/premium-metrics-app-23.png)

    <span data-ttu-id="2c382-283">b.</span><span class="sxs-lookup"><span data-stu-id="2c382-283">b.</span></span> <span data-ttu-id="2c382-284">**แผนภูมิ C** จะถูกกรองเพื่อแสดงการจำกัดผลลัพธ์ ที่จะอธิบายไว้ในขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="2c382-284">**Chart C** is then filtered to show any throttling, explained in the next step.</span></span> 

2. <span data-ttu-id="2c382-285">ดูผลลัพธ์ใน **แผนภูมิ C** ที่กรองแล้วในขณะนี้ ถ้าแผนภูมิแสดงการจำกัดผลลัพธ์จากหน่วยความจำไม่เพียงพอที่เกิดขึ้นในช่วงเวลาที่ชุดข้อมูลกำลังรอนั้น ชุดข้อมูลกำลังรอเนื่องจากสภาวะหน่วยความจำเหลือน้อย</span><span class="sxs-lookup"><span data-stu-id="2c382-285">Look at the results in the now-filtered **Chart C**. If the chart shows out of memory throttling occurred at the times the dataset was waiting, then the dataset was waiting due to low memory conditions.</span></span>

    ![แผนภูมิ C](media/service-premium-metrics-app/premium-metrics-app-24.png)

3. <span data-ttu-id="2c382-287">สุดท้าย ให้ตรวจสอบ **แผนภูมิ D** ซึ่งแสดงชนิดการรีเฟรชที่เกิดขึ้น โดยมีรีเฟรชตามกำหนดเวลาเทียบกับรีเฟรชตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="2c382-287">Finally, check **Chart D**, which shows the types of refreshes that were occurring, scheduled versus on-demand.</span></span> <span data-ttu-id="2c382-288">การรีเฟรชตามความต้องการใดๆ ที่เกิดขึ้นในเวลาเดียวกันอาจเป็นสาเหตุของการจำกัดผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="2c382-288">Any on-demand refreshes occurring at the same time could be the cause of the throttling.</span></span>

    ![แผนภูมิ D](media/service-premium-metrics-app/premium-metrics-app-25.png)


#### <a name="remedies-for-scenario-one"></a><span data-ttu-id="2c382-290">การแก้ไขสำหรับสถานการณ์ที่หนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2c382-290">Remedies for scenario one</span></span>

<span data-ttu-id="2c382-291">คุณสามารถทำตามขั้นตอนต่อไปนี้เพื่อแก้ไขปัญหาที่เกี่ยวข้องกับสถานการณ์ที่หนึ่ง:</span><span class="sxs-lookup"><span data-stu-id="2c382-291">You can take the following steps to remedy the problems associated with scenario one:</span></span>

1. <span data-ttu-id="2c382-292">**เพิ่มขนาดความจุ** - เพิ่มขนาดความจุไปยัง SKU ถัดไปจะทำให้มีจำนวนหน่วยความจำที่มากกว่า SKU ปัจจุบันสองเท่า ทำให้บรรเทาความดันหน่วยความจำ และ CPU ใดๆ ที่กำลังประสบอยู่</span><span class="sxs-lookup"><span data-stu-id="2c382-292">**Scale up the capacity** - scaling up the capacity to the next SKU will make available twice the amount of memory than the current SKU, thus alleviating any memory and CPU pressure the capacity is currently experiencing.</span></span>

2. <span data-ttu-id="2c382-293">**ย้ายชุดข้อมูลไปยังความจุอื่น** - ถ้าเวลาการรอของคุณเกิดจากความดันหน่วยความจำและคุณมีความจุอื่นที่มีหน่วยความจำมากกว่า คุณสามารถย้ายพื้นที่ทำงานที่ประกอบด้วยชุดข้อมูลที่กำลังรออยู่ไปยังความจุอื่นได้</span><span class="sxs-lookup"><span data-stu-id="2c382-293">**Move datasets to another capacity** - if your wait times are being caused by memory pressure and you have another capacity that has more memory available, you can move the workspaces that contain the datasets that are waiting to the other capacity.</span></span>

3. <span data-ttu-id="2c382-294">**กระจายการรีเฟรชตามกำหนดเวลา** - การกระจายการรีเฟรชจะช่วยให้คุณสามารถหลีกเลี่ยงการรีเฟรชจำนวนมากเกินไปที่พยายามดำเนินการพร้อมๆ กัน</span><span class="sxs-lookup"><span data-stu-id="2c382-294">**Spread out scheduled refreshes** - spreading out the refreshes will help to avoid too many refreshes attempting to execute concurrently.</span></span>



### <a name="scenario-two---not-enough-cpu-for-refresh"></a><span data-ttu-id="2c382-295">สถานการณ์ที่สอง - มี CPU ไม่เพียงพอในการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="2c382-295">Scenario two - not enough CPU for refresh</span></span>

<span data-ttu-id="2c382-296">ในสถานการณ์ที่สอง มี CPU ที่พร้อมใช้งานไม่เพียงพอที่จะดำเนินการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="2c382-296">In scenario two, there isn't enough available CPU to carry out the refresh.</span></span> 

<span data-ttu-id="2c382-297">สำหรับความจุ Power BI จำกัดจำนวนการรีเฟรชที่สามารถเกิดขึ้นได้พร้อม ๆ กัน</span><span class="sxs-lookup"><span data-stu-id="2c382-297">For capacities, Power BI limits the number of refreshes that can happen concurrently.</span></span> <span data-ttu-id="2c382-298">ตัวเลขนี้เท่ากับจำนวนของแกนประมวลผล back-end x 1.5</span><span class="sxs-lookup"><span data-stu-id="2c382-298">This number is equal to the number of back-end cores x 1.5.</span></span> <span data-ttu-id="2c382-299">ตัวอย่างเช่น ความจุ P1 ซึ่งมีแกนประมวลผล back-end สี่แกน จะสามารถเรียกใช้งานรีเฟรชได้ 6 รายการพร้อม ๆ กัน</span><span class="sxs-lookup"><span data-stu-id="2c382-299">For example, a P1 capacity, which has four back-end cores, can run 6 refreshes concurrently.</span></span> <span data-ttu-id="2c382-300">เมื่อถึงจำนวนสูงสุดของการรีเฟรชพร้อมกันแล้ว การรีเฟรชอื่นๆ จะรอจนกว่าการดำเนินการเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="2c382-300">Once the maximum number of concurrent refreshes has been reached, other refreshes will wait until an executing refresh finishes.</span></span>

![สถานการณ์ที่สองสำหรับรีเฟรช](media/service-premium-metrics-app/premium-metrics-app-26.png)

#### <a name="diagnosing-scenario-two"></a><span data-ttu-id="2c382-302">วินิจฉัยสถานการณ์ที่สอง</span><span class="sxs-lookup"><span data-stu-id="2c382-302">Diagnosing scenario two</span></span>

<span data-ttu-id="2c382-303">ในการวินิจฉัยสถานการณ์ที่สอง ก่อนอื่นให้พิจารณาว่าการจำกัดผลลัพธ์เกิดจากการทำงานถึงภาวะพร้อมกันระดับสูงสุดสำหรับการรีเฟรชหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2c382-303">To diagnose scenario two, first determine whether throttling is due to running into the maximum concurrency for refreshes.</span></span> <span data-ttu-id="2c382-304">ขั้นตอนในการทำมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2c382-304">The steps to do so are the following.</span></span>

1. <span data-ttu-id="2c382-305">เลือกชุดข้อมูลที่คุณสนใจจาก **ตาราง  A** ด้วยการคลิกที่ตาราง:</span><span class="sxs-lookup"><span data-stu-id="2c382-305">Select the dataset you're interested in from **Table A** by clicking on it:</span></span> 

    ![ตาราง  A](media/service-premium-metrics-app/premium-metrics-app-22.png)

    <span data-ttu-id="2c382-307">a.</span><span class="sxs-lookup"><span data-stu-id="2c382-307">a.</span></span> <span data-ttu-id="2c382-308">เมื่อมีการเลือกชุดข้อมูลใน **ตาราง A** **แผนภูมิ B** จะถูกกรองเพื่อแสดงเวลาเมื่อมีการรอเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="2c382-308">When a dataset is selected in **Table A**, **Chart B** is filtered to show when waiting occurred.</span></span>

    ![แผนภูมิ B](media/service-premium-metrics-app/premium-metrics-app-23.png)

    <span data-ttu-id="2c382-310">b.</span><span class="sxs-lookup"><span data-stu-id="2c382-310">b.</span></span> <span data-ttu-id="2c382-311">**แผนภูมิ C** จะถูกกรองเพื่อแสดงการจำกัดผลลัพธ์ ที่จะอธิบายไว้ในขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="2c382-311">**Chart C** is then filtered to show any throttling, explained in the next step.</span></span> 

2. <span data-ttu-id="2c382-312">ดูผลลัพธ์ใน **แผนภูมิ C** ที่กรองแล้วในขณะนี้ ถ้าแผนภูมิแสดง *ภาวะพร้อมกันระดับสูงสุด* เกิดขึ้นในช่วงเวลาที่ชุดข้อมูลกำลังรอนั้น ชุดข้อมูลกำลังรอเนื่องจากมี CPU ไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="2c382-312">Look at the results in the now-filtered **Chart C**. If the chart shows *max concurrency* occurred at the times the dataset was waiting, then the dataset was waiting due to not enough available CPU.</span></span>

    ![แผนภูมิ C](media/service-premium-metrics-app/premium-metrics-app-24.png)

3. <span data-ttu-id="2c382-314">สุดท้าย ให้ตรวจสอบ **แผนภูมิ D** ซึ่งแสดงชนิดการรีเฟรชที่เกิดขึ้น โดยมีรีเฟรชตามกำหนดเวลาเทียบกับรีเฟรชตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="2c382-314">Finally, check **Chart D**, which shows the types of refreshes that were occurring, scheduled versus on-demand.</span></span> <span data-ttu-id="2c382-315">การรีเฟรชตามความต้องการใดๆ ที่เกิดขึ้นในเวลาเดียวกันอาจเป็นสาเหตุของการจำกัดผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="2c382-315">Any on-demand refreshes occurring at the same time could be the cause of the throttling.</span></span>

    ![แผนภูมิ D](media/service-premium-metrics-app/premium-metrics-app-25.png)


#### <a name="remedies-for-scenario-two"></a><span data-ttu-id="2c382-317">การแก้ไขสำหรับสถานการณ์ที่สอง</span><span class="sxs-lookup"><span data-stu-id="2c382-317">Remedies for scenario two</span></span>

1. <span data-ttu-id="2c382-318">**เพิ่มขนาดความจุ** - เพิ่มขนาดความจุไปยัง SKU ถัดไปจะทำให้มีจำนวนหน่วยความจำและมีจำนวนครั้งที่มีการรีเฟรชพร้อมกันที่มากกว่า SKU ปัจจุบันสองเท่า ทำให้บรรเทาความดันหน่วยความจำ และ CPU ใดๆ ที่กำลังประสบอยู่</span><span class="sxs-lookup"><span data-stu-id="2c382-318">**Scale up the capacity** - scaling up the capacity to the next SKU will make available twice the amount of memory than the current SKU, and twice the number of concurrent refreshes than the current SKU, thus alleviating any memory and CPU pressure the capacity is currently experiencing.</span></span>

2. <span data-ttu-id="2c382-319">**ย้ายชุดข้อมูลไปยังความจุอื่น** - ถ้าเวลาการรอของคุณเกิดจากการทำงานถึงภาวะพร้อมกันระดับสูงสุดและคุณมีความจุอื่นที่มีภาวะพร้อมกันมากกว่า คุณสามารถย้ายพื้นที่ทำงานที่ประกอบด้วยชุดข้อมูลที่ที่กำลังรออยู่ไปยังความจุอื่นได้</span><span class="sxs-lookup"><span data-stu-id="2c382-319">**Move datasets to another capacity** - if your wait times are being caused by maximum concurrency being reached and you have another capacity that has available concurrency, you can move the workspaces that contain the datasets that are waiting to the other capacity.</span></span>

3. <span data-ttu-id="2c382-320">**กระจายการรีเฟรชตามกำหนดเวลา** - การกระจายการรีเฟรชจะช่วยให้คุณสามารถหลีกเลี่ยงการรีเฟรชจำนวนมากเกินไปที่พยายามดำเนินการพร้อมๆ กัน</span><span class="sxs-lookup"><span data-stu-id="2c382-320">**Spread out scheduled refreshes** - spreading out the refreshes will help to avoid too many refreshes attempting to execute concurrently.</span></span>



## <a name="next-steps"></a><span data-ttu-id="2c382-321">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="2c382-321">Next steps</span></span>

* [<span data-ttu-id="2c382-322">Power BI Premium คืออะไร?</span><span class="sxs-lookup"><span data-stu-id="2c382-322">What is Power BI Premium?</span></span>](service-premium-what-is.md)
* [<span data-ttu-id="2c382-323">เอกสารทางเทคนิคเรื่อง Microsoft Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="2c382-323">Microsoft Power BI Premium whitepaper</span></span>](https://aka.ms/pbipremiumwhitepaper)
* [<span data-ttu-id="2c382-324">เอกสารทางเทคนิคเรื่องการวางแผนการใช้ Power BI สำหรับองค์กร</span><span class="sxs-lookup"><span data-stu-id="2c382-324">Planning a Power BI Enterprise Deployment whitepaper</span></span>](https://aka.ms/pbienterprisedeploy)
* [<span data-ttu-id="2c382-325">เปิดใช้งานเวอร์ชันทดลองใช้ Extended Pro </span><span class="sxs-lookup"><span data-stu-id="2c382-325">Extended Pro Trial activation</span></span>](../fundamentals/service-self-service-signup-for-power-bi.md)
* [<span data-ttu-id="2c382-326">คำถามที่พบบ่อยสำหรับ Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="2c382-326">Power BI Embedded FAQ</span></span>](../developer/embedded/embedded-faq.md)

<span data-ttu-id="2c382-327">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2c382-327">More questions?</span></span> [<span data-ttu-id="2c382-328">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="2c382-328">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)

<span data-ttu-id="2c382-329">Power BI ได้แนะนำ Power BI Premium Gen2 เข้ามาใช้งานเป็นข้อเสนอการแสดงตัวอย่าง ซึ่งปรับปรุงประสบการณ์การใช้งาน Power BI Premium ด้วยการปรับปรุงในสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2c382-329">Power BI has introduced Power BI Premium Gen2 as a preview offering, which improves the Power BI Premium experience with improvements in the following:</span></span>
* <span data-ttu-id="2c382-330">ประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="2c382-330">Performance</span></span>
* <span data-ttu-id="2c382-331">สิทธิการใช้งานต่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2c382-331">Per-user licensing</span></span>
* <span data-ttu-id="2c382-332">ขนาดใหญ่ขึ้น</span><span class="sxs-lookup"><span data-stu-id="2c382-332">Greater scale</span></span>
* <span data-ttu-id="2c382-333">เมตริกที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="2c382-333">Improved metrics</span></span>
* <span data-ttu-id="2c382-334">การปรับขนาดอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2c382-334">Autoscaling</span></span>
* <span data-ttu-id="2c382-335">ลดค่าใช้จ่ายในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="2c382-335">Reduced management overhead</span></span>

<span data-ttu-id="2c382-336">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI Premium Gen2 โปรดดูที่ [Power BI Premium Generation 2 (ตัวอย่าง)](service-premium-what-is.md#power-bi-premium-generation-2-preview)</span><span class="sxs-lookup"><span data-stu-id="2c382-336">For more information about Power BI Premium Gen2, see [Power BI Premium Generation 2 (preview)](service-premium-what-is.md#power-bi-premium-generation-2-preview).</span></span>