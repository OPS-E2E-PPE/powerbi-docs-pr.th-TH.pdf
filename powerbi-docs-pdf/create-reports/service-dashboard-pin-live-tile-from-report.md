---
title: 'ปักหมุดหน้ารายงานทั้งหน้ากับแดชบอร์ด Power BI '
description: เอกสารประกอบเกี่ยวกับวิธีการปักหมุดหน้ารายงานทั้งหน้าแบบไลฟ์กับแดชบอร์ด Power BI จากรายงาน
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 03/02/2018
LocalizationGroup: Dashboards
ms.openlocfilehash: 29a0521620b335add8256c87e1e354c58f58584d
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96395198"
---
# <a name="pin-an-entire-report-page-as-a-live-tile-to-a-power-bi-dashboard"></a><span data-ttu-id="38b4f-103">ปักหมุดหน้ารายงานทั้งหน้าแบบไลฟ์ไทล์กับแดชบอร์ด Power BI</span><span class="sxs-lookup"><span data-stu-id="38b4f-103">Pin an entire report page, as a live tile, to a Power BI dashboard</span></span>
<span data-ttu-id="38b4f-104">อีกวิธีในการเพิ่มใหม่[แดชบอร์ดไทล์](../consumer/end-user-tiles.md) คือการปักหมุดหน้ารายงานทั้งหน้า</span><span class="sxs-lookup"><span data-stu-id="38b4f-104">Another way to add a new [dashboard tile](../consumer/end-user-tiles.md) is by pinning an entire report page.</span></span> <span data-ttu-id="38b4f-105">นี่คือวิธีง่ายๆ ในการปักหมุดการแสดงภาพมากกว่าหนึ่งครั้ง</span><span class="sxs-lookup"><span data-stu-id="38b4f-105">This is an easy way to pin more than one visualization at a time.</span></span>  <span data-ttu-id="38b4f-106">นอกจากนี้ เมื่อคุณปักหมุดทั้งหน้า ไทล์จะเป็นแบบ *live* คุณสามารถโต้ตอบกับพวกมันได้จากที่นั่นบนแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="38b4f-106">Also, when you pin an entire page, the tiles are *live*; you can interact with them right there on the dashboard.</span></span> <span data-ttu-id="38b4f-107">และเปลี่ยนแปลงที่คุณทำกับการแสดงภาพก่อนหน้านี้ในตัวแก้ไขรายงาน เช่นการเพิ่มตัวกรองหรือการเปลี่ยนแปลงเขตข้อมูลที่ใช้ในแผนภูมิ จะปรากฏในแดชบอร์ดไทล์เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="38b4f-107">And changes you make to any of the visualizations back in the report editor, like adding a filter or changing the fields used in the chart, are reflected in the dashboard tile as well.</span></span>  

<span data-ttu-id="38b4f-108">ปักหมุดไทล์แบบไลฟ์จากรายงานกับแดชบอร์ด สามารถใช้ได้ใน Power BI service (app.powerbi.com) เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="38b4f-108">Pinning live tiles from reports to dashboards is only available in Power BI service (app.powerbi.com).</span></span>

> [!NOTE]
> <span data-ttu-id="38b4f-109">คุณไม่สามารถปักหมุดไทล์จากรายงานที่ใช้ร่วมกันกับคุณได้</span><span class="sxs-lookup"><span data-stu-id="38b4f-109">You can't pin tiles from reports that are shared with you.</span></span>
> 
> 

## <a name="pin-a-report-page"></a><span data-ttu-id="38b4f-110">ปักหมุดหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="38b4f-110">Pin a report page</span></span>
<span data-ttu-id="38b4f-111">ดู Amanda ปักหมุดหน้ารายงานไว้กับแดชบอร์ด แล้วทำตามคำแนะนำทีละขั้นตอนด้านล่างวิดีโอเพื่อลองทำด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="38b4f-111">Watch Amanda pin a live report page to a dashboard and then follow the step-by-step instructions below the video to try it yourself.</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/EzhfBpPboPA" frameborder="0" allowfullscreen></iframe>


1. <span data-ttu-id="38b4f-112">เปิด[รายงานในมุมมองการแก้ไข](service-interact-with-a-report-in-editing-view.md)</span><span class="sxs-lookup"><span data-stu-id="38b4f-112">Open a report in [Editing view](service-interact-with-a-report-in-editing-view.md).</span></span>
2. <span data-ttu-id="38b4f-113">เนื่องจากการแสดงภาพไม่ได้ถูกเลือกจากแถบเมนู ให้เลือก **ปักหมุดหน้าแบบไลฟ์**</span><span class="sxs-lookup"><span data-stu-id="38b4f-113">With no visualizations selected, from the menubar, select **Pin Live Page**.</span></span>
   
   ![ไอคอนปักหมุดหน้าแบบไลฟ์](media/service-dashboard-pin-live-tile-from-report/pbi-pin-live-page.png) 
3. <span data-ttu-id="38b4f-115">ปักหมุดไทล์ลงในแดชบอร์ดที่มีอยู่ หรือแดชบอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="38b4f-115">Pin the tile to an existing dashboard or to a new dashboard.</span></span> <span data-ttu-id="38b4f-116">โปรดสังเกตว่า ข้อความที่ไฮไลท์ *การปักหมุดหน้าแบบไลฟ์สามารถทำให้รายงานปรากฏในแดชบอร์ดไทล์เปลี่ยนเมื่อมีการรีเฟรชหน้าได้*</span><span class="sxs-lookup"><span data-stu-id="38b4f-116">Notice the highlighted text: *Pin live page enables changes to reports to appear in the dashboard tile when the page is refreshed.*</span></span>
   
   * <span data-ttu-id="38b4f-117">แดชบอร์ดที่มีอยู่: เลือกชื่อของแดชบอร์ดจากรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="38b4f-117">Existing dashboard: select the name of the dashboard from the dropdown.</span></span> <span data-ttu-id="38b4f-118">แดชบอร์ดที่แชร์กับคุณจะไม่ปรากฏขึ้นที่นี่</span><span class="sxs-lookup"><span data-stu-id="38b4f-118">Dashboards that have been shared with you will not appear in the dropdown.</span></span>
   * <span data-ttu-id="38b4f-119">แดชบอร์ดใหม่ พิมพ์ชื่อของแดชบอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="38b4f-119">New dashboard: type the name of the new dashboard.</span></span>
     
     ![ปักหมุดไปยังแดชบอร์ด](media/service-dashboard-pin-live-tile-from-report/pbi-pin-live-page-dialog.png)
4. <span data-ttu-id="38b4f-121">เลือก **Pin live**</span><span class="sxs-lookup"><span data-stu-id="38b4f-121">Select **Pin live**.</span></span> <span data-ttu-id="38b4f-122">ข้อความว่าสำเร็จแล้ว (ใกล้กับมุมบนขวา) ช่วยให้คุณทราบว่า การหน้าถูกเพิ่มเป็นไทล์ ลงในแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="38b4f-122">A Success message (near the top right corner) lets you know the page was added, as a tile, to your dashboard.</span></span>

## <a name="open-the-dashboard-to-see-the-pinned-live-tile"></a><span data-ttu-id="38b4f-123">เปิดแดชบอร์ดเพื่อดูไทล์ที่ถูกปักหมุดแบบไลฟ์</span><span class="sxs-lookup"><span data-stu-id="38b4f-123">Open the dashboard to see the pinned live tile</span></span>
1. <span data-ttu-id="38b4f-124">จากบานหน้าต่างนำทาง ให้เลือกแดชบอร์ดที่มีไทล์แบบสดอันใหม่</span><span class="sxs-lookup"><span data-stu-id="38b4f-124">From the nav pane, select the dashboard with the new live tile.</span></span> <span data-ttu-id="38b4f-125">ที่นั่น คุณสามารถทำสิ่งต่างๆ เช่น[เปลี่ยนชื่อ ปรับขนาด ลิงก์ และย้าย](service-dashboard-edit-tile.md)หน้ารายงานที่ปักหมุดไว้ได้</span><span class="sxs-lookup"><span data-stu-id="38b4f-125">There, you can do things like [rename, resize, link, and move](service-dashboard-edit-tile.md) the pinned report page.</span></span>  
2. <span data-ttu-id="38b4f-126">โต้ตอบกับไทล์รายงานแบบไลฟ์</span><span class="sxs-lookup"><span data-stu-id="38b4f-126">Interact with the live tile.</span></span>  <span data-ttu-id="38b4f-127">ในสกรีนช็อตด้านล่าง ให้เลือกแถบบนคอลัมน์ แผนภูมิมีตัวกรองแบบสลับ และแสดงภาพอื่นๆ บนไทล์แบบไฮไลท์สลับ</span><span class="sxs-lookup"><span data-stu-id="38b4f-127">In the screenshot below, selecting a bar on the column chart has cross-filtered and cross-highlighted the other visualizations on the tile.</span></span>
   
    ![แดชบอร์ดที่มีไทลแบบไลฟ์](media/service-dashboard-pin-live-tile-from-report/pbi-live-tile.png)

## <a name="next-steps"></a><span data-ttu-id="38b4f-129">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="38b4f-129">Next steps</span></span>
[<span data-ttu-id="38b4f-130">แดชบอร์ดใน Power BI</span><span class="sxs-lookup"><span data-stu-id="38b4f-130">Dashboards in Power BI</span></span>](../consumer/end-user-dashboards.md)

<span data-ttu-id="38b4f-131">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="38b4f-131">More questions?</span></span> [<span data-ttu-id="38b4f-132">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="38b4f-132">Try the Power BI Community</span></span>](https://community.powerbi.com/)
