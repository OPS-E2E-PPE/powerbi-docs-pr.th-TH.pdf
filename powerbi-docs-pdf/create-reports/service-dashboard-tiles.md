---
title: แนะนำไทล์แดชบอร์ดสำหรับนักออกแบบ Power BI
description: บทความนี้อธิบายไทล์แดชบอร์ดใน Power BI ซึ่งรวมถึงไทล์ที่สร้างขึ้นจากรายงาน SQL Server Reporting Services (SSRS)
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 04/17/2020
LocalizationGroup: Dashboards
ms.openlocfilehash: 56f00568b22d236b498446065cf97ff565993e7a
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418249"
---
# <a name="intro-to-dashboard-tiles-for-power-bi-designers"></a><span data-ttu-id="76fa3-103">แนะนำไทล์แดชบอร์ดสำหรับนักออกแบบ Power BI</span><span class="sxs-lookup"><span data-stu-id="76fa3-103">Intro to dashboard tiles for Power BI designers</span></span>

<span data-ttu-id="76fa3-104">ไทล์เป็นสแนปช็อตของข้อมูลของคุณที่ปักหมุดไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="76fa3-104">A tile is a snapshot of your data, pinned to the dashboard.</span></span> <span data-ttu-id="76fa3-105">คุณสามารถสร้างไทล์จากรายงาน ชุดข้อมูล แดชบอร์ด กล่องคำถาม Q&A, Excel และรายงาน SQL Server Reporting Services (SSRS) และอื่น ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="76fa3-105">A tile can be created from a report, dataset, dashboard, the Q&A box, Excel, SQL Server Reporting Services (SSRS) reports, and more.</span></span>  <span data-ttu-id="76fa3-106">ภาพถ่ายหน้าจอนี้แสดงไทล์ต่าง ๆ มากมายที่ปักหมุดไปยังแดชบอร์ดหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="76fa3-106">This screenshot shows many different tiles pinned to a dashboard.</span></span>

![แดชบอร์ด Power BI](media/service-dashboard-tiles/power-bi-dashboard.png)

<span data-ttu-id="76fa3-108">แดชบอร์ดและไทล์แดชบอร์ดเป็นคุณลักษณะของบริการ Power BI ไม่ใช่ของ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="76fa3-108">Dashboards and dashboard tiles are a feature of Power BI service, not Power BI Desktop.</span></span> <span data-ttu-id="76fa3-109">คุณไม่สามารถสร้างแดชบอร์ดบนอุปกรณ์มือถือ แต่คุณสามารถ [ดู และแชร์](../consumer/mobile/mobile-apps-view-dashboard.md) ได้</span><span class="sxs-lookup"><span data-stu-id="76fa3-109">You can't create dashboards on mobile devices but you can [view and share](../consumer/mobile/mobile-apps-view-dashboard.md) them there.</span></span>

<span data-ttu-id="76fa3-110">นอกจากการปักหมุดไทล์แล้ว คุณยังสามารถสร้างไทล์แบบเดี่ยวได้โดยตรงบนแดชบอร์ดโดยใช้ตัวควบคุม [เพิ่มไทล์](service-dashboard-add-widget.md)</span><span class="sxs-lookup"><span data-stu-id="76fa3-110">Besides pinning tiles, you can create standalone tiles directly on the dashboard by using the [Add tile](service-dashboard-add-widget.md) control.</span></span> <span data-ttu-id="76fa3-111">ไทล์แบบเดี่ยวรวมถึง: กล่องข้อความ รูปภาพ วิดีโอ ข้อมูลสตรีมมิ่ง และเนื้อหาบนเว็บ</span><span class="sxs-lookup"><span data-stu-id="76fa3-111">Standalone tiles include: text boxes, images, videos, streaming data, and web content.</span></span>

<span data-ttu-id="76fa3-112">ต้องการความช่วยเหลือในการทำความเข้าใจเกี่ยวกับบล็อกที่ประกอบเป็น Power BI หรือไม่</span><span class="sxs-lookup"><span data-stu-id="76fa3-112">Need help with understanding the building blocks that make up Power BI?</span></span> <span data-ttu-id="76fa3-113">ดู[แนวคิดพื้นฐานสำหรับนักออกแบบในบริการของ Power BI](../fundamentals/service-basic-concepts.md)</span><span class="sxs-lookup"><span data-stu-id="76fa3-113">See [Basic concepts for designers in the Power BI service](../fundamentals/service-basic-concepts.md).</span></span>

> [!NOTE]
> <span data-ttu-id="76fa3-114">ถ้าการแสดงภาพต้นฉบับที่ใช้เพื่อสร้างไทล์เปลี่ยนแปลง ไทล์ดังกล่าวจะไม่เปลี่ยนแปลงไปด้วย</span><span class="sxs-lookup"><span data-stu-id="76fa3-114">If the original visualization used to create the tile changes, the tile doesn't change.</span></span>  <span data-ttu-id="76fa3-115">ตัวอย่างเช่น ถ้าคุณปักหมุดแผนภูมิเส้นจากรายงาน จากนั้นคุณเปลี่ยนแผนภูมิเส้นเป็นแผนภูมิแท่ง ไทล์แดชบอร์ดจะยังคงแสดงแผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="76fa3-115">For example, if you pinned a line chart from a report and then you changed the line chart to a bar chart, the dashboard tile continues to show a line chart.</span></span> <span data-ttu-id="76fa3-116">รีเฟรชข้อมูลแต่การชนิดแสดงภาพไม่เปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="76fa3-116">The data refreshes, but the visualization type does not.</span></span>
> 
> 

## <a name="pin-a-tile"></a><span data-ttu-id="76fa3-117">ปักหมุดไทล์</span><span class="sxs-lookup"><span data-stu-id="76fa3-117">Pin a tile</span></span>
<span data-ttu-id="76fa3-118">มีหลายวิธีในการเพิ่ม (PIN) ไทล์หนึ่ง ๆ ไปยังแดชบอร์ดหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="76fa3-118">There are many different ways to add (pin) a tile to a dashboard.</span></span> <span data-ttu-id="76fa3-119">คุณสามารถปักหมุดไทล์จาก:</span><span class="sxs-lookup"><span data-stu-id="76fa3-119">You can pin tiles from:</span></span>

* [<span data-ttu-id="76fa3-120">การถามตอบสำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="76fa3-120">Power BI Q&A</span></span>](service-dashboard-pin-tile-from-q-and-a.md)
* [<span data-ttu-id="76fa3-121">รายงาน</span><span class="sxs-lookup"><span data-stu-id="76fa3-121">A report</span></span>](service-dashboard-pin-tile-from-report.md)
* [<span data-ttu-id="76fa3-122">แดชบอร์ดอื่น</span><span class="sxs-lookup"><span data-stu-id="76fa3-122">Another dashboard</span></span>](service-pin-tile-to-another-dashboard.md)
* [<span data-ttu-id="76fa3-123">สมุดงาน Excel บน OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="76fa3-123">Excel workbook on OneDrive for Business</span></span>](service-dashboard-pin-tile-from-excel.md)
* [<span data-ttu-id="76fa3-124">Quick Insights (ข้อมูลเชิงลึกด่วน)</span><span class="sxs-lookup"><span data-stu-id="76fa3-124">Quick Insights</span></span>](service-insights.md)
* [<span data-ttu-id="76fa3-125">รายงานที่มีการแบ่งหน้าภายในองค์กรในเซิร์ฟเวอร์รายงาน Power BI หรือ SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="76fa3-125">An on-premises paginated report in Power BI Report Server or SQL Server Reporting Services</span></span>](/sql/reporting-services/pin-reporting-services-items-to-power-bi-dashboards)

<span data-ttu-id="76fa3-126">คุณสามารถสร้างไทล์แบบเดี่ยวสำหรับรูปภาพ กล่องข้อความ วิดีโอ ข้อมูลสตรีมมิ่ง และเนื้อหาบนเว็บได้โดยตรงบนแดชบอร์ดโดยใช้ตัวควบคุม [เพิ่มไทล์](service-dashboard-add-widget.md)</span><span class="sxs-lookup"><span data-stu-id="76fa3-126">You create standalone tiles for images, text boxes, videos, streaming data, and web content directly on the dashboard by using the [Add tile](service-dashboard-add-widget.md) control.</span></span>

  ![เพิ่มไอคอนไทล์](media/service-dashboard-tiles/add_widgetnew.png)

## <a name="interact-with-tiles-on-a-dashboard"></a><span data-ttu-id="76fa3-128">โต้ตอบกับไทล์บนแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="76fa3-128">Interact with tiles on a dashboard</span></span>
<span data-ttu-id="76fa3-129">หลังจากที่คุณได้เพิ่มไทล์ลงในแดชบอร์ดแล้ว คุณสามารถย้ายและปรับขนาดหรือเปลี่ยนลักษณะที่ปรากฏและลักษณะการทำงานได้</span><span class="sxs-lookup"><span data-stu-id="76fa3-129">After you've added a tile to a dashboard, you can move and resize it, or change its appearance and behavior.</span></span>

### <a name="move-and-resize-a-tile"></a><span data-ttu-id="76fa3-130">ย้ายและปรับขนาดไทล์</span><span class="sxs-lookup"><span data-stu-id="76fa3-130">Move and resize a tile</span></span>
<span data-ttu-id="76fa3-131">หยิบไทล์และ[ย้ายไปรอบ ๆ ในแดชบอร์ด](service-dashboard-edit-tile.md)</span><span class="sxs-lookup"><span data-stu-id="76fa3-131">Grab a tile and [move it around on the dashboard](service-dashboard-edit-tile.md).</span></span> <span data-ttu-id="76fa3-132">เลื่อนและเลือกด้ามจับ![ด้ามจับไทล์](media/service-dashboard-tiles/resize-handle.jpg)เพื่อปรับขนาดไทล์</span><span class="sxs-lookup"><span data-stu-id="76fa3-132">Hover and select the handle ![Tile handle](media/service-dashboard-tiles/resize-handle.jpg) to resize the tile.</span></span>

### <a name="hover-over-a-tile-to-change-the-appearance-and-behavior"></a><span data-ttu-id="76fa3-133">เลื่อนเหนือไทล์เพื่อเปลี่ยนลักษณะปรากฏและลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="76fa3-133">Hover over a tile to change the appearance and behavior</span></span>
1. <span data-ttu-id="76fa3-134">เลื่อนเหนือไทล์เพื่อแสดงจุดไข่ปลา</span><span class="sxs-lookup"><span data-stu-id="76fa3-134">Hover over the tile to display the ellipsis.</span></span>
   
    ![จุดไข่ปลาของไทล์](media/service-dashboard-tiles/ellipses_new.png)
2. <span data-ttu-id="76fa3-136">เลือกจุดไข่ปลาเพื่อเปิดเมนูการดำเนินการของไทล์</span><span class="sxs-lookup"><span data-stu-id="76fa3-136">Select the ellipsis to open the tile action menu.</span></span>
   
    ![ไอคอนจุดไข่ปลา](media/service-dashboard-tiles/power-bi-tile-menu.png)
   
    <span data-ttu-id="76fa3-138">จากตรงนี้คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="76fa3-138">From here you can:</span></span>
   
     * <span data-ttu-id="76fa3-139">[เพิ่มความคิดเห็นในแดชบอร์ด](../consumer/end-user-comment.md)</span><span class="sxs-lookup"><span data-stu-id="76fa3-139">[Add comments to the dashboard](../consumer/end-user-comment.md).</span></span>
     * <span data-ttu-id="76fa3-140">[เปิดรายงานที่ใช้เพื่อสร้างไทล์นี้](../consumer/end-user-reports.md)</span><span class="sxs-lookup"><span data-stu-id="76fa3-140">[Open the report that was used to create this tile](../consumer/end-user-reports.md).</span></span>  
     * <span data-ttu-id="76fa3-141">[ดูในโหมดโฟกัส](../consumer/end-user-focus.md)</span><span class="sxs-lookup"><span data-stu-id="76fa3-141">[View in focus mode](../consumer/end-user-focus.md).</span></span>   
     * <span data-ttu-id="76fa3-142">[ส่งออกข้อมูลที่ใช้ในไทล์](../visuals/power-bi-visualization-export-data.md)</span><span class="sxs-lookup"><span data-stu-id="76fa3-142">[Export the data used in the tile](../visuals/power-bi-visualization-export-data.md).</span></span>
     * <span data-ttu-id="76fa3-143">[แก้ไขชื่อเรื่องและคำบรรยายและเพิ่มไฮเปอร์ลิงก์](service-dashboard-edit-tile.md)</span><span class="sxs-lookup"><span data-stu-id="76fa3-143">[Edit the title and subtitle and add a hyperlink](service-dashboard-edit-tile.md).</span></span> 
     * <span data-ttu-id="76fa3-144">[เรียกใช้ข้อมูลเชิงลึก](service-insights.md)</span><span class="sxs-lookup"><span data-stu-id="76fa3-144">[Run insights](service-insights.md).</span></span> 
     * <span data-ttu-id="76fa3-145">[ปักหมุดไทล์ไปยังแดชบอร์ดอื่น](service-pin-tile-to-another-dashboard.md)</span><span class="sxs-lookup"><span data-stu-id="76fa3-145">[Pin the tile to another dashboard](service-pin-tile-to-another-dashboard.md).</span></span>
     * <span data-ttu-id="76fa3-146">[ลบไทล์](service-dashboard-edit-tile.md)</span><span class="sxs-lookup"><span data-stu-id="76fa3-146">[Delete the tile](service-dashboard-edit-tile.md).</span></span>

3. <span data-ttu-id="76fa3-147">เมื่อต้องปิดเมนูการดำเนินการ เลือกพื้นที่ว่างในแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="76fa3-147">To close the action menu, select a blank area in the dashboard.</span></span>

### <a name="select-a-tile"></a><span data-ttu-id="76fa3-148">เลือกไทล์</span><span class="sxs-lookup"><span data-stu-id="76fa3-148">Select a tile</span></span>
<span data-ttu-id="76fa3-149">เมื่อคุณเลือกไทล์หนึ่ง สิ่งที่จะเกิดขึ้นถัดไปขึ้นอยู่กับวิธีการที่คุณสร้างไทล์</span><span class="sxs-lookup"><span data-stu-id="76fa3-149">When you select a tile, what happens next depends on how you created the tile.</span></span> <span data-ttu-id="76fa3-150">มิฉะนั้น การเลือกไทล์จะนำคุณไปยังรายงาน เวิร์กบุ๊ก Excel Online รายงาน Reporting Services ที่อยู่ภายในองค์กร หรือคำถาม Q&A ที่ถูกใช้เพื่อสร้างไทล์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="76fa3-150">Otherwise, selecting the tile takes you to the report, Excel Online workbook, on-premises Reporting Services report, or Q&A question that was used to create the tile.</span></span> <span data-ttu-id="76fa3-151">หากมี[ลิงก์แบบกำหนดเอง](service-dashboard-edit-tile.md) การเลือกไทล์จะนำคุณไปที่ลิงก์นั้น</span><span class="sxs-lookup"><span data-stu-id="76fa3-151">Or, if it has a [custom link](service-dashboard-edit-tile.md), selecting the tile takes you to that link.</span></span>

> [!NOTE]
> <span data-ttu-id="76fa3-152">ข้อยกเว้นคือไทล์วิดีโอที่สร้างขึ้นโดยตรงบนแดชบอร์ดโดยใช้ **เพิ่มไทล์**</span><span class="sxs-lookup"><span data-stu-id="76fa3-152">An exception is video tiles created directly on the dashboard by using **Add tile**.</span></span> <span data-ttu-id="76fa3-153">การเลือกไทล์วิดีโอ (ที่สร้างขึ้นด้วยวิธีนี้) ทำให้วิดีโอสามารถเล่นได้บนแดชบอร์ดดังกล่าวโดยตรง</span><span class="sxs-lookup"><span data-stu-id="76fa3-153">Selecting a video tile (that was created this way) causes the video to play directly on the dashboard.</span></span>   
> 
> 

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="76fa3-154">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="76fa3-154">Considerations and troubleshooting</span></span>

* <span data-ttu-id="76fa3-155">ถ้ามีการบันทึกรายงานที่ใช้เพื่อสร้างการแสดงภาพไม่ได้รับการบันทึก การเลือกไทล์จะไม่ก่อให้เกิดการดำเนินการใด ๆ</span><span class="sxs-lookup"><span data-stu-id="76fa3-155">If the report that was used to create the visualization wasn't saved, selecting the tile produces no action.</span></span>
* <span data-ttu-id="76fa3-156">ถ้าไทล์ถูกสร้างขึ้นจากเวิร์กบุ๊กใน Excel Online คุณต้องมีสิทธิ์การอ่านสำหรับเวิร์กบุ๊กนั้นเป็นอย่างน้อย</span><span class="sxs-lookup"><span data-stu-id="76fa3-156">If the tile was created from a workbook in Excel Online, you need at least Read permissions for that workbook.</span></span> <span data-ttu-id="76fa3-157">มิฉะนั้น การเลือกไทล์จะไม่เปิดเวิร์กบุ๊กใน Excel Online</span><span class="sxs-lookup"><span data-stu-id="76fa3-157">Otherwise, selecting the tile won't open the workbook in Excel Online.</span></span>
* <span data-ttu-id="76fa3-158">สมมติว่าคุณสร้างไทล์โดยตรงบนแดชบอร์ดโดยใช้ **เพิ่มไทล์** และตั้งค่าไฮเปอร์ลิงก์แบบกำหนดเองสำหรับไทล์นั้น</span><span class="sxs-lookup"><span data-stu-id="76fa3-158">Say you create a tile directly on the dashboard by using **Add tile** and set a custom hyperlink for it.</span></span> <span data-ttu-id="76fa3-159">ถ้าเป็นเช่นนั้น เมื่อคุณเลือกชื่อเรื่อง คำบรรยาย หรือไทล์ จะเปิด URL นั้น</span><span class="sxs-lookup"><span data-stu-id="76fa3-159">If so, when you select the title, subtitle, or tile, it opens that URL.</span></span> <span data-ttu-id="76fa3-160">มิฉะนั้นตามค่าเริ่มต้น เมื่อคุณเลือกไทล์ที่ถูกสร้างขึ้นโดยตรงบนแดชบอร์ดสำหรับรูปภาพหนึ่ง โค้ดของเว็บ หรือกล่องข้อความ จะไม่ก่อให้เกิดการดำเนินการใด</span><span class="sxs-lookup"><span data-stu-id="76fa3-160">Otherwise, by default, when you select a tile created directly on the dashboard for an image, web code, or text box, nothing happens.</span></span>
* <span data-ttu-id="76fa3-161">ไทล์สามารถสร้างได้จากรายงานที่มีการแบ่งหน้าภายในองค์กรในเซิร์ฟเวอร์รายงาน Power BI หรือ SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="76fa3-161">Tiles can be created from on-premises paginated reports in Power BI Report Server or SQL Server Reporting Services.</span></span> <span data-ttu-id="76fa3-162">ถ้าคุณไม่มีสิทธิ์ในการเข้าถึงรายงานภายในองค์กร การเลือกไทล์จะนำคุณไปยังหน้าที่ระบุว่าคุณไม่มีสิทธิ์เข้าถึง (rsAccessDenied)</span><span class="sxs-lookup"><span data-stu-id="76fa3-162">If you don't have permission to access the on-premises report, selecting the tile takes you to a page indicating you don't have access (rsAccessDenied).</span></span>
* <span data-ttu-id="76fa3-163">สมมติว่าคุณเลือกไทล์ที่สร้างจากรายงานที่มีการแบ่งหน้าภายในองค์กรในเซิร์ฟเวอร์รายงาน Power BI หรือ SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="76fa3-163">Say you select a tile created from an on-premises paginated report in Power BI Report Server or SQL Server Reporting Services.</span></span> <span data-ttu-id="76fa3-164">ถ้าคุณไม่สามารถเข้าถึงเครือข่ายที่มีเซิร์ฟเวอร์รายงานนั้นอยู่ การเลือกไทล์ที่สร้างขึ้นจากรายงานที่มีการแบ่งหน้าจะนำคุณไปยังหน้าที่บ่งชี้ว่าไม่สามารถค้นหาเซิร์ฟเวอร์ (HTTP 404) ได้</span><span class="sxs-lookup"><span data-stu-id="76fa3-164">If you don't have access to the network where the report server is located, selecting a tile created from that paginated report takes you to a page that indicates it can't locate the server (HTTP 404).</span></span> <span data-ttu-id="76fa3-165">อุปกรณ์ของคุณจำเป็นต้องมีสิทธิ์เข้าถึงเครือข่ายไปยังเซิร์ฟเวอร์รายงานเพื่อดูรายงานดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="76fa3-165">Your device needs network access to the report server to view the report.</span></span>
* <span data-ttu-id="76fa3-166">ถ้าการแสดงภาพต้นฉบับที่ใช้เพื่อสร้างไทล์เปลี่ยนแปลง ไทล์ดังกล่าวจะไม่เปลี่ยนแปลงไปด้วย</span><span class="sxs-lookup"><span data-stu-id="76fa3-166">If the original visualization that's used to create the tile changes, the tile doesn't change.</span></span> <span data-ttu-id="76fa3-167">ตัวอย่างเช่น ถ้าคุณปักหมุดแผนภูมิเส้นจากรายงาน จากนั้นคุณเปลี่ยนแผนภูมิเส้นเป็นแผนภูมิแท่ง ไทล์แดชบอร์ดจะยังคงแสดงแผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="76fa3-167">For example, if you pin a line chart from a report and then you change the line chart to a bar chart, the dashboard tile continues to show a line chart.</span></span> <span data-ttu-id="76fa3-168">ข้อมูลจะรีเฟรชแต่ชนิดการแสดงภาพไม่รีเฟรช</span><span class="sxs-lookup"><span data-stu-id="76fa3-168">The data refreshes, but the visualization type doesn't.</span></span>

## <a name="next-steps"></a><span data-ttu-id="76fa3-169">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="76fa3-169">Next steps</span></span>
- [<span data-ttu-id="76fa3-170">สร้างการ์ด (ไทล์ตัวเลขขนาดใหญ่) สำหรับแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="76fa3-170">Create a card (large number tile) for your dashboard</span></span>](../visuals/power-bi-visualization-card.md)
- [<span data-ttu-id="76fa3-171">บทนำแดชบอร์ดสำหรับนักออกแบบ Power BI</span><span class="sxs-lookup"><span data-stu-id="76fa3-171">Introduction to dashboards for Power BI designers</span></span>](service-dashboards.md)  
- [<span data-ttu-id="76fa3-172">การรีเฟรชข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="76fa3-172">Data refresh in Power BI</span></span>](../connect-data/refresh-data.md)
- [<span data-ttu-id="76fa3-173">แนวคิดพื้นฐานสำหรับนักออกแบบในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="76fa3-173">Basic concepts for designers in the Power BI service</span></span>](../fundamentals/service-basic-concepts.md)
- [<span data-ttu-id="76fa3-174">การรวมไทล์ Power BI ลงในเอกสาร Office</span><span class="sxs-lookup"><span data-stu-id="76fa3-174">Integrating Power BI tiles into Office documents</span></span>](https://powerbi.microsoft.com/blog/integrating-power-bi-tiles-into-office-documents/)
- [<span data-ttu-id="76fa3-175">ปักหมุดรายการ Reporting Services ไปยังแดชบอร์ด Power BI</span><span class="sxs-lookup"><span data-stu-id="76fa3-175">Pin Reporting Services items to Power BI dashboards</span></span>](/sql/reporting-services/pin-reporting-services-items-to-power-bi-dashboards)

<span data-ttu-id="76fa3-176">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="76fa3-176">More questions?</span></span> <span data-ttu-id="76fa3-177">[ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="76fa3-177">[Try the Power BI Community](https://community.powerbi.com/).</span></span>