---
title: ปรับแดชบอร์ดให้เหมาะสมสำหรับโทรศัพท์มือถือ-Power BI
description: เรียนรู้วิธีการสร้างมุมมองแบบกำหนดเองของแดชบอร์ดใน Power BI service โดยเฉพาะสำหรับการดูบนโทรศัพท์มือถือ
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.custom: contperf-fy21q2
ms.topic: how-to
ms.date: 04/18/2019
LocalizationGroup: Dashboards
ms.openlocfilehash: 3e8733a20a812d74bc09ef1cf91778b5dd37bcfe
ms.sourcegitcommit: a92a3570eb14793a758a32e8fa1a756ec5d83f8c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/21/2020
ms.locfileid: "97708099"
---
# <a name="optimize-a-dashboard-for-mobile-phones---power-bi"></a><span data-ttu-id="38381-103">ปรับแดชบอร์ดให้เหมาะสมสำหรับโทรศัพท์มือถือ-Power BI</span><span class="sxs-lookup"><span data-stu-id="38381-103">Optimize a dashboard for mobile phones - Power BI</span></span> 
<span data-ttu-id="38381-104">เมื่อคุณดูแดชบอร์ดในโหมดแนวตั้งบนโทรศัพท์ของคุณ คุณจะสังเกตเห็นแดชบอร์ดที่เป็นแบบซ้อนถัดๆกัน ที่มีขนาดเดียวกันทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="38381-104">When you view dashboards in portrait mode on a phone, you notice the dashboard tiles are laid out one after another, all the same size.</span></span> <span data-ttu-id="38381-105">ใน Power BI service คุณสามารถสร้างมุมมองของแดชบอร์ดโดยเฉพาะสำหรับโหมดแนวตั้งของคุณ</span><span class="sxs-lookup"><span data-stu-id="38381-105">In the Power BI service, you can create a customized view of a dashboard, specifically for portrait mode on phones.</span></span> <span data-ttu-id="38381-106">เมื่อคุณเปิดใช้งานมุมมองทางโทรศัพท์เมื่อคุณหันโทรศัพท์ไปทางทางด้านข้าง คุณจะเห็นแดชบอร์ดถูกวางไว้ในบริการ</span><span class="sxs-lookup"><span data-stu-id="38381-106">Even if you create a phone view, when you turn the phone sideways, you see the dashboard as it's laid out in the service.</span></span>

<span data-ttu-id="38381-107">คุณกำลังค้นหาข้อมูลเกี่ยวกับการดูแดชบอร์ดบนอุปกรณ์เคลื่อนที่แทนใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="38381-107">Are you looking for information about viewing dashboards on a mobile device?</span></span> <span data-ttu-id="38381-108">ลองใช้การเริ่มต้นใช้งานด่วนแทนที่[ แดชบอร์ดและรายงานในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่](../consumer/mobile/mobile-apps-quickstart-view-dashboard-report.md)</span><span class="sxs-lookup"><span data-stu-id="38381-108">Try this quickstart [Explore dashboards and reports in the Power BI mobile apps](../consumer/mobile/mobile-apps-quickstart-view-dashboard-report.md) instead.</span></span>

> [!NOTE]
> <span data-ttu-id="38381-109">เมื่อคุณแก้ไขมุมมองโทรศัพท์ ทุกคนที่ดูแดชบอร์ดบนโทรศัพท์ของคุณสามารถดูการเปลี่ยนแปลงที่คุณทำในแบบเรียลไทม์</span><span class="sxs-lookup"><span data-stu-id="38381-109">As you edit the phone view, anyone viewing the dashboard on a phone can see the changes you make in real time.</span></span> <span data-ttu-id="38381-110">ตัวอย่างเช่น ถ้าคุณถอนหมุดไทล์ทั้งหมดในมุมมองโทรศัพท์ของแดชบอร์ด แดชบอร์ดบนโทรศัพท์จะไม่มีไทล์ทันที</span><span class="sxs-lookup"><span data-stu-id="38381-110">For example, if you unpin all tiles on the dashboard phone view, the dashboard on the phone will suddenly have no tiles.</span></span> 
> 
> 

## <a name="create-a-phone-view-of-a-dashboard"></a><span data-ttu-id="38381-111">สร้างมุมมองโทรศัพท์ของแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="38381-111">Create a phone view of a dashboard</span></span>
1. <span data-ttu-id="38381-112">ใน Power BI service เปิดแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="38381-112">In the Power BI service, open a dashboard.</span></span>
2. <span data-ttu-id="38381-113">เลือกลูกศรที่อยู่ถัดจาก **มุมมองเว็บ** ที่มุมบนขวา > เลือก **มุมมองโทรศัพท์**</span><span class="sxs-lookup"><span data-stu-id="38381-113">Select the arrow next to **Web view** in the upper-right corner > select **Phone view**.</span></span>

    ![ภาพหน้าจอของเมนูดรอปดาวน์มุมมองเว็บ ที่แสดงตัวชี้ไปยังมุมมองโทรศัพท์](media/service-create-dashboard-mobile-phone-view/power-bi-service-phone-view-dashboard.png)

    <span data-ttu-id="38381-115">ถ้าคุณไม่ได้เป็นเจ้าของแดชบอร์ด คุณจะไม่เห็นตัวเลือกนี้</span><span class="sxs-lookup"><span data-stu-id="38381-115">If you aren't the dashboard owner, you won't see this option.</span></span>

    ![ภาพหน้าจอของแดชบอร์ดของโทรศัพท์ ที่แสดงตัวเลือกแก้ไขมุมมองเพื่อยกเลิกการปักหมุด ปรับขนาด และจัดเรียงไทล์ใหม่เพื่อให้พอดีกับมุมมองโทรศัพท์](media/service-create-dashboard-mobile-phone-view/power-bi-mobile-edit-phone-view-canvas.png)

    <span data-ttu-id="38381-117">มุมมองแก้ไขแดชบอร์ดโทรศัพท์เปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="38381-117">The phone dashboard edit view opens.</span></span> <span data-ttu-id="38381-118">ที่นี่คุณสามารถถอนการปักหมุด ปรับขนาด และจัดเรียงไทล์ให้พอดีกับมุมมองโทรศัพท์ได้</span><span class="sxs-lookup"><span data-stu-id="38381-118">Here you can unpin, resize, and rearrange tiles to fit the phone view.</span></span> <span data-ttu-id="38381-119">แดชบอร์ดเวอร์ชันบนเว็บไม่เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="38381-119">The web version of the dashboard doesn't change.</span></span>


1. <span data-ttu-id="38381-120">เลือกไทล์เพื่อลาก ปรับขนาดหรือถอนหมุด</span><span class="sxs-lookup"><span data-stu-id="38381-120">Select a tile to drag, resize, or unpin it.</span></span> <span data-ttu-id="38381-121">คุณสังเกตเห็นว่า ไทล์อื่นจะย้ายออกในขณะที่คุณลากไทล์</span><span class="sxs-lookup"><span data-stu-id="38381-121">You notice the other tiles move out of the way as you drag a tile.</span></span>
   
    ![ภาพหน้าจอของไทล์โทรศัพท์ ที่แสดงการเลือกไทล์เพื่อลาก ปรับขนาด หรือยกเลิกการปักหมุด](media/service-create-dashboard-mobile-phone-view/power-bi-unpin-tile-phone-dashboard.png)
   
    <span data-ttu-id="38381-123">หมุดไทล์ที่ถูกถอนจะไปอยู่ในบานหน้าต่างไทล์ที่ถูกถอน ซึ่งเป็นที่ที่พวกมันอยูเว้นแต่ว่าคุณเพิ่มมันกลับมา</span><span class="sxs-lookup"><span data-stu-id="38381-123">The unpinned tiles go in the Unpinned tiles pane, where they stay unless you add them back.</span></span>
   
    ![ภาพหน้าจอของแดชบอร์ดโทรศัพท์ ที่แสดงไทล์ในบานหน้าต่างไทล์ที่ไม่ได้ปักหมุด](media/service-create-dashboard-mobile-phone-view/power-bi-mobile-edit-phone-view-post-edit.png)
2. <span data-ttu-id="38381-125">ถ้าคุณเปลี่ยนใจ ให้เลือก **รีเซ็ตไทล์** เพื่อเปลี่ยนเป็นขนาดและลำดับเดิมของพวกมัน</span><span class="sxs-lookup"><span data-stu-id="38381-125">If you change your mind, select **Reset tiles**  to put them back in the size and order they were before.</span></span>
   
    ![ภาพหน้าจอของบานหน้าต่างไทล์ที่ไม่ได้ปักหมุด ที่แสดงตัวชี้เพื่อรีเซ็ตไทล์](media/service-create-dashboard-mobile-phone-view/power-bi-service-phone-view-reset-tiles.png)
   
    <span data-ttu-id="38381-127">เพียงแค่เปิดมุมมองแก้ไขของโทรศัพท์ใน Power BI service เปลี่ยนแปลงขนาดและรูปร่างของไทล์บนโทรศัพท์ของคุณเล็กน้อย</span><span class="sxs-lookup"><span data-stu-id="38381-127">Just opening Phone Edit view in the Power BI service slightly changes the size and shape of the tiles on a phone.</span></span> <span data-ttu-id="38381-128">ดังนั้นเพื่อเปลี่ยนแดชบอร์ดให้อยู่ในสถานะเช่นเดียวกับก่อนที่คุณได้เปิดแก้ไขมุมมองโทรศัพท์ ให้เลือก **รีเซ็ตไทล์**</span><span class="sxs-lookup"><span data-stu-id="38381-128">So to return the dashboard to its exact state before you opened it in Phone Edit view, select **Reset tiles**.</span></span>
3. <span data-ttu-id="38381-129">เมื่อคุณพอใจกับเค้าโครงแดชบอร์ดโทรศัพท์ ให้เลือกลูกศรที่อยู่ถัดจาก **มุมมองโทรศัพท** ที่มุมบนขวา > เลือก **มุมมองเว็บ**</span><span class="sxs-lookup"><span data-stu-id="38381-129">When you're satisfied with the phone dashboard layout, select the arrow next to **Phone view** in the upper-right corner > select **Web view**.</span></span>
   
    <span data-ttu-id="38381-130">Power BI จะบันทึกเค้าโครงโทรศัพท์โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="38381-130">Power BI saves the phone layout automatically.</span></span>

## <a name="next-steps"></a><span data-ttu-id="38381-131">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="38381-131">Next steps</span></span>
* [<span data-ttu-id="38381-132">สร้างรายงานที่ปรับให้เหมาะสมสำหรับแอปมือถือ Power BI</span><span class="sxs-lookup"><span data-stu-id="38381-132">Create reports optimized for the Power BI phone apps</span></span>](desktop-create-phone-report.md)
* [<span data-ttu-id="38381-133">สร้างภาพแบบตอบสนองที่ปรับให้เหมาะสมกับทุกขนาด</span><span class="sxs-lookup"><span data-stu-id="38381-133">Create responsive visuals optimized for any size</span></span>](../visuals/power-bi-report-visualizations.md)
* <span data-ttu-id="38381-134">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="38381-134">More questions?</span></span> [<span data-ttu-id="38381-135">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="38381-135">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
