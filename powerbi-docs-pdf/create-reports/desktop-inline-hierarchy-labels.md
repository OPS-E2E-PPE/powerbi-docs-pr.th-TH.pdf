---
title: ใช้ป้ายลำดับชั้นแบบอินไลน์ใน Power BI Desktop
description: ใช้ป้ายลำดับชั้นแบบอินไลน์ใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 05/08/2019
LocalizationGroup: Create reports
ms.openlocfilehash: 8e9938c1c65e8e5a69f59365b89a10a449c3cf39
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96396808"
---
# <a name="use-inline-hierarchy-labels-in-power-bi-desktop"></a><span data-ttu-id="3b4fa-103">ใช้ป้ายลำดับชั้นแบบอินไลน์ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3b4fa-103">Use inline hierarchy labels in Power BI Desktop</span></span>
<span data-ttu-id="3b4fa-104">**Power BI Desktop** สนับสนุนการใช้ **ป้ายลำดับชั้นแบบอินไลน์** ซึ่งเป็นหนึ่งในสองคุณลักษณะ ที่ปรับปรุงการดูรายละเอียดแบบลำดับชั้นให้ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="3b4fa-104">**Power BI Desktop** supports the use of **inline hierarchy labels**, which is the first of two features intended to enhance hierarchical drilling.</span></span> <span data-ttu-id="3b4fa-105">คุณลักษณะที่สอง ซึ่งอยู่ในขณะนี้อยู่ในระหว่างการพัฒนา คือความสามารถในการใช้ป้ายลำดับชั้นที่ซ้อนกัน (รออีกสักหน่อย - เราอัปเดตอยู่บ่อย ๆ)</span><span class="sxs-lookup"><span data-stu-id="3b4fa-105">The second feature, which is currently in development, is the ability to use nested hierarchy labels (stay tuned for that - our updates happen frequently).</span></span>   

## <a name="how-inline-hierarchy-labels-work"></a><span data-ttu-id="3b4fa-106">ป้ายลำดับชั้นแบบอินไลน์ทำงานอย่างไร</span><span class="sxs-lookup"><span data-stu-id="3b4fa-106">How inline hierarchy labels work</span></span>
<span data-ttu-id="3b4fa-107">ด้วยป้ายลำดับชั้นแบบอินไลน์ คุณสามารถเห็นป้ายลำดับชั้นได้ขณะที่คุณขยายวิชวลโดยใช้คุณลักษณะ **ขยายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="3b4fa-107">With inline hierarchy labels, you can see hierarchy labels as you expand visuals using the **Expand All** feature.</span></span> <span data-ttu-id="3b4fa-108">ประโยชน์ที่สำคัญหนึ่งอย่างก็คือ คุณยังสามารถเลือกที่จะ **เรียงลำดับ** ตามป้ายเหล่านี้ เมื่อคุณขยายข้อมูลของคุณตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="3b4fa-108">One great benefit to seeing these hierarchy labels is that you can also choose to **sort** by these different hierarchy labels as you expand your hierarchical data.</span></span>

### <a name="using-the-built-in-expand-feature-without-sorting-by-hierarchy-labels"></a><span data-ttu-id="3b4fa-109">การใช้คุณลักษณะขยายที่มีอยู่ในตัว (โดยไม่มีการเรียงลำดับตามป้ายลำดับชั้น)</span><span class="sxs-lookup"><span data-stu-id="3b4fa-109">Using the built-in Expand feature (without sorting by hierarchy labels)</span></span>
<span data-ttu-id="3b4fa-110">ก่อนที่เราเห็นการทำงานของป้ายลำดับชั้นแบบอินไลน์ เรามาดูว่าค่าเริ่มต้นคุณลักษณะ **ขยายไปยังระดับถัดไป**</span><span class="sxs-lookup"><span data-stu-id="3b4fa-110">Before we see inline hierarchy labels in action, let's review the default **Expand to next level** feature behavior.</span></span> <span data-ttu-id="3b4fa-111">ซึ่งจะช่วยให้เราเข้าใจ (และชื่นชม) ว่าป้ายลำดับชั้นแบบอินไลน์มีประโยชน์แค่ไหน</span><span class="sxs-lookup"><span data-stu-id="3b4fa-111">Doing so will help us understand (and appreciate) how useful inline hierarchy labels can be.</span></span>

<span data-ttu-id="3b4fa-112">รูปต่อไปนี้แสดงแผนภูมิแท่งสำหรับยอดขายรายปี</span><span class="sxs-lookup"><span data-stu-id="3b4fa-112">The following image shows a bar chart visual for annual sales.</span></span> <span data-ttu-id="3b4fa-113">เมื่อคุณคลิกขวาบนแถบ คุณสามารถเลือก **ขยายไปยังระดับถัดไป** ได้</span><span class="sxs-lookup"><span data-stu-id="3b4fa-113">When you right-click on a bar, you can choose **Expand to next level**.</span></span>

![ขยายเมนูบริบท](media/desktop-inline-hierarchy-labels/desktop-inline-hierarchy-labels-menu.png)

> [!NOTE]
> <span data-ttu-id="3b4fa-115">แทนที่จะคลิกขวาบนแถบ คุณสามารถเลือกปุ่ม *ขยาย* ที่ด้านบนซ้ายของการแสดงภาพได้</span><span class="sxs-lookup"><span data-stu-id="3b4fa-115">As an alternative to right-clicking on a bar, you can select the *Expand* button on the top left of the visualization.</span></span>

  ![ปุ่มขยาย](media/desktop-inline-hierarchy-labels/desktop-inline-hierarchy-labels-expand-button-finger.png)


<span data-ttu-id="3b4fa-117">ทันทีที่เลือก **ขยายไปยังระดับถัดไป** วิชวลจะขยายลำดับชั้นวันที่จาก *ปี* ไปเป็น *ไตรมาส* ดังที่แสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3b4fa-117">Once **Expand to next level** is selected, the visual expands the date hierarchy from *Year* to *Quarter*, as shown in the following image.</span></span>

![วิชวลขยายเป็นปีและไตรมาส](media/desktop-inline-hierarchy-labels/desktop-inline-hierarchy-labels-qty-year-quarter.png)

<span data-ttu-id="3b4fa-119">สังเกตว่า ป้าย *ปี* และ *ไตรมาส* จะแสดงแบบอินไลน์เข้าด้วยกัน รูปแบบป้ายนี้ยังดำเนินต่อไปเรื่อยๆ เมื่อคุณ **ขยายทั้งหมด** ลงไปจนถึงลำดับชั้นล่างสุด</span><span class="sxs-lookup"><span data-stu-id="3b4fa-119">Notice that the *Year* and *Quarter* labels are shown inline together - this labeling scheme continues as you **Expand All** down to the bottom of the hierarchy.</span></span>

![วิชวลขยายเป็นปี ไตรมาสและเดือน](media/desktop-inline-hierarchy-labels/desktop-inline-hierarchy-labels-qty-year-quarter-month.png)

<span data-ttu-id="3b4fa-121">นี่คือวิธีการทำงานของลำดับชั้น *วันที่* ที่เชื่อมโยงกับเขตข้อมูลที่มีชนิดข้อมูลเป็น *วันที่/เวลา*</span><span class="sxs-lookup"><span data-stu-id="3b4fa-121">This is how the built-in *Date* hierarchy, associated with fields that have a *date/time* data type, behaves.</span></span> <span data-ttu-id="3b4fa-122">เรามาดูในส่วนถัดไป และดูว่าคุณลักษณะป้ายลำดับชั้นแบบอินไลน์ที่เพิ่มมาใหม่แตกต่างกันอย่างไร</span><span class="sxs-lookup"><span data-stu-id="3b4fa-122">Let's head to the next section, and see how the new inline hierarchy labels feature is different.</span></span>

### <a name="using-inline-hierarchy-labels"></a><span data-ttu-id="3b4fa-123">การใช้ป้ายลำดับชั้นแบบอินไลน์</span><span class="sxs-lookup"><span data-stu-id="3b4fa-123">Using inline hierarchy labels</span></span>
<span data-ttu-id="3b4fa-124">ตอนนี้มาดูที่อีกแผนภูมิหนึ่ง - ที่ใช้ข้อมูลที่มีลำดับชั้นที่ไม่เป็นทางการ</span><span class="sxs-lookup"><span data-stu-id="3b4fa-124">Now let's look at a different chart - using data that has informal hierarchies.</span></span> <span data-ttu-id="3b4fa-125">ในวิชวลต่อไปนี้ เรามีแผนภูมิแท่ง **ปริมาณ** โดยใช้ *ชื่อผลิตภัณฑ์* เป็นแกน</span><span class="sxs-lookup"><span data-stu-id="3b4fa-125">In the following visual, we have a bar chart with **Quantity**, using *ProductName* as the axis.</span></span> <span data-ttu-id="3b4fa-126">ในข้อมูลนี้ *ชื่อผลิตภัณฑ์* และ *ประเทศที่ส่งไป* สร้างลำดับชั้นไม่เป็นทางการ</span><span class="sxs-lookup"><span data-stu-id="3b4fa-126">In this data, *ProductName* and *ShipCountry* form an informal hierarchy.</span></span> <span data-ttu-id="3b4fa-127">จากที่นี่ คุณสามารถเลือก *ขยายไปยังระดับถัดไป* เมื่อต้องการดูข้อมูลแบบละเอียดตามลำดับชั้นลงไป</span><span class="sxs-lookup"><span data-stu-id="3b4fa-127">From here, you can again select *Expand to next level* to drill down into the hierarchy.</span></span>

![แผนภูมิที่มีลำดับชั้นที่ไม่เป็นทางการ](media/desktop-inline-hierarchy-labels/desktop-inline-hierarchy-labels-informal-top-expand.png)

<span data-ttu-id="3b4fa-129">การเลือก **ขยายไปยังระดับถัดไป** จะแสดงระดับถัดไป ด้วยการแสดงผลป้ายลำดับชั้นแบบอินไลน์</span><span class="sxs-lookup"><span data-stu-id="3b4fa-129">Selecting **Expand to next level** shows the next level with the inline display of hierarchy labels.</span></span> <span data-ttu-id="3b4fa-130">ตามค่าเริ่มต้น ลำดับชั้นแบบอินไลน์ จะเรียงลำดับตามค่าหน่วยวัด – ในกรณีนี้คือ **ปริมาณ**</span><span class="sxs-lookup"><span data-stu-id="3b4fa-130">By default, inline hierarchies are sorted by the measure value – in this case, **Quantity**.</span></span> <span data-ttu-id="3b4fa-131">เมื่อเปิดใช้งานป้ายลำดับชั้นแบบอินไลน์ คุณสามารถเลือกที่จะเรียงลำดับข้อมูลนี้ตามลำดับชั้นด้วย โดยการเลือกจุดไข่ปลาในมุมบนขวา ( **...** ), แล้วเลือก **เรียงลำดับตามชื่อผลิตภัณฑ์ ประเทศที่ส่งไป** ดังที่แสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3b4fa-131">With inline hierarchy labels enabled, you can choose to sort this data by the hierarchy too, by selecting the ellipsis in the upper right corner (the **...**), then selecting **Sort by ProductName ShipCountry** as shown in the following image.</span></span>

![แผนภูมิที่มีลำดับชั้นไม่เป็นทางการเรียงลำดับตามค่าเริ่มต้น](media/desktop-inline-hierarchy-labels/desktop-inline-hierarchy-labels-informal-sort-quantity.png)

<span data-ttu-id="3b4fa-133">ทันทีที่เลือก **ประเทศที่ส่งไป** ข้อมูลมีการเรียงลำดับตามลำดับชั้นที่ไม่เป็นทางการ ดังแสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3b4fa-133">Once **ShipCountry** is selected, the data is sorted based on the informal hierarchy selection, as shown in the following image.</span></span>

![แผนภูมิที่มีลำดับชั้นไม่เป็นทางการเรียงลำดับตามลำดับชั้นไม่เป็นทางการ](media/desktop-inline-hierarchy-labels/desktop-inline-hierarchy-labels-informal-sorted.png)

> [!NOTE]
> <span data-ttu-id="3b4fa-135">ป้ายลำดับชั้นแบบอินไลน์ ยังไม่เรียงลำดับชั้นเวลาที่มีอยู่แล้วตามค่าได้ ทำได้เพียงจัดเรียงตามลำดับชั้นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3b4fa-135">The inline hierarchy label feature doesn't yet allow for the built-in time hierarchy to be sorted by value; it's only sorted by hierarchy order.</span></span>
> 
> 

## <a name="troubleshooting"></a><span data-ttu-id="3b4fa-136">แนวทางการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="3b4fa-136">Troubleshooting</span></span>
<span data-ttu-id="3b4fa-137">เป็นไปได้ที่วิชวลของคุณ ค้างอยู่ที่ระดับลำดับชั้นแบบอินไลน์ที่ขยายแล้ว</span><span class="sxs-lookup"><span data-stu-id="3b4fa-137">It's possible for your visuals to get stuck in an expanded inline hierarchy level state.</span></span> <span data-ttu-id="3b4fa-138">ในบางกรณีคุณอาจพบว่า บางวิชวลของคุณค้างอยู่ในโหมดที่ขยายแล้ว และไม่สามารถเลื่อนขึ้นไปยังลำดับชั้นสูงกว่าได้</span><span class="sxs-lookup"><span data-stu-id="3b4fa-138">In some cases, you might find that some of your visuals are stuck in the mode where they were expanded, in which case drilling up doesn't work.</span></span> <span data-ttu-id="3b4fa-139">ซึ่งสามารถเกิดขึ้นได้ถ้าคุณทำขั้นตอนต่อไปนี้ (วิธีการแก้ไขปัญหานี้อยู่ *ด้านล่าง* ขั้นตอนที่ก่อให้เกิดปัญหา):</span><span class="sxs-lookup"><span data-stu-id="3b4fa-139">This can happen if you happened to take the following steps (the fix for this is *below* these steps):</span></span>

<span data-ttu-id="3b4fa-140">ขั้นตอนที่อาจทำให้วิชวลของคุณค้างอยู่ในสถานะที่ถูกขยาย:</span><span class="sxs-lookup"><span data-stu-id="3b4fa-140">Steps that might get your visuals stuck in an expanded state:</span></span>

1. <span data-ttu-id="3b4fa-141">คุณเปิดใช้งานคุณลักษณะ **ป้ายลำดับชั้นแบบอินไลน์**</span><span class="sxs-lookup"><span data-stu-id="3b4fa-141">You enable the **inline hierarchy label** feature</span></span>
2. <span data-ttu-id="3b4fa-142">คุณสร้างวิชวลบางอย่างที่มีลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="3b4fa-142">You create some visuals with hierarchies</span></span>
3. <span data-ttu-id="3b4fa-143">แล้วคุณ **ขยายทั้งหมด** และบันทึกไฟล์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3b4fa-143">Then you **Expand All** and save your file</span></span>
4. <span data-ttu-id="3b4fa-144">จากนั้นก็ *ปิดใช้งาน* คุณลักษณะ **ป้ายลำดับชั้นแบบอินไลน์** และรีสตาร์ท Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3b4fa-144">You then *disable* the **inline hierarchy label** feature, and restart Power BI Desktop</span></span>
5. <span data-ttu-id="3b4fa-145">แล้วคุณเปิดไฟล์ของคุณอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="3b4fa-145">Then you re-open your file</span></span>

<span data-ttu-id="3b4fa-146">ถ้าคุณบังเอิญทำขั้นตอนเหล่านั้น และวิชวลของคุณจะค้างอยู่ในโหมดขยาย คุณสามารถทำตามขั้นตอนต่อไปนี้เพื่อแก้ไขปัญหา:</span><span class="sxs-lookup"><span data-stu-id="3b4fa-146">If you happen to take those steps, and your visuals are stuck in expanded mode, you can do the following to troubleshoot them:</span></span>

1. <span data-ttu-id="3b4fa-147">เปิดใช้งานคุณลักษณะ **ป้ายลำดับชั้นแบบอินไลน์** ใหม่ จากนั้นรีสตาร์ท Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3b4fa-147">Re-enable the **inline hierarchy label** feature, then restart Power BI Desktop</span></span>
2. <span data-ttu-id="3b4fa-148">เปิดไฟล์ของคุณอีกครั้ง และเลื่อนขึ้นจนถึงระดับชั้นบนสุดของวิชวลที่ได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="3b4fa-148">Re-open your file, and drill back up to top of your affected visual(s)</span></span>
3. <span data-ttu-id="3b4fa-149">บันทึกไฟล์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3b4fa-149">Save your file</span></span>
4. <span data-ttu-id="3b4fa-150">ปิดใช้งานคุณลักษณะ **ป้ายลำดับชั้นแบบอินไลน์** จากนั้นรีสตาร์ท Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3b4fa-150">Disable the **inline hierarchy label** feature, then restart Power BI Desktop</span></span>
5. <span data-ttu-id="3b4fa-151">เปิดไฟล์ของคุณอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="3b4fa-151">Re-open your file</span></span>

<span data-ttu-id="3b4fa-152">อีกวิธีหนึ่งคือ คุณสามารถเพียงแค่ลบวิชวลของคุณ แล้วสร้างขึ้นใหม่</span><span class="sxs-lookup"><span data-stu-id="3b4fa-152">Alternatively, you can just delete your visual and recreate it.</span></span>

