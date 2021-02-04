---
title: ไทล์แดชบอร์ดในบริการ Power BI สำหรับผู้ใช้ทางธุรกิจ
description: ทั้งหมดที่เกี่ยวกับไทล์แดชบอร์ดใน Power BI สำหรับผู้ใช้ทางธุรกิจ ซึ่งรวมถึงไทล์ที่สร้างขึ้นจาก SQL Server Reporting Services (SSRS)
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-explore
ms.topic: how-to
ms.date: 12/06/2020
LocalizationGroup: Dashboards
ms.openlocfilehash: 36b1ad58b1ee93f0876de8bf7f7ed7331671abfd
ms.sourcegitcommit: 0bf42b6393cab7a37d21a52b934539cf300a08e2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/07/2020
ms.locfileid: "96781913"
---
# <a name="dashboard-tiles-in-power-bi"></a><span data-ttu-id="acd2a-104">ไทล์แดชบอร์ดใน Power BI</span><span class="sxs-lookup"><span data-stu-id="acd2a-104">Dashboard tiles in Power BI</span></span>

[!INCLUDE[consumer-appliesto-yyny](../includes/consumer-appliesto-ynny.md)]


<span data-ttu-id="acd2a-105">ไทล์เป็นสแนปช็อตของข้อมูลของคุณที่ปักหมุดไปยังแดชบอร์ดโดย *ผู้ออกแบบ*</span><span class="sxs-lookup"><span data-stu-id="acd2a-105">A tile is a snapshot of your data, pinned to a dashboard by a *designer*.</span></span> <span data-ttu-id="acd2a-106">*ผู้ออกแบบ* สามารถสร้างไทล์จากรายงาน ชุดข้อมูล แดชบอร์ด กล่องคำถามของ Q&A, Excel และ SQL Server Reporting Services (SSRS) และอื่น ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="acd2a-106">*Designers* can create tiles from a report, dataset, dashboard, the Q&A question box, Excel, SQL Server Reporting Services (SSRS), and more.</span></span>  <span data-ttu-id="acd2a-107">ภาพถ่ายหน้าจอนี้แสดงไทล์ต่าง ๆ มากมายที่ปักหมุดไปยังแดชบอร์ดหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="acd2a-107">This screenshot shows many different tiles pinned to a dashboard.</span></span>

![แดชบอร์ด Power BI](./media/end-user-tiles/power-bi-dashboard.png)


<span data-ttu-id="acd2a-109">นอกเหนือจากไทล์ที่ปักหมุดจากรายงาน *ผู้ออกแบบ* สามารถเพิ่มไทล์แบบเดี่ยวได้โดยตรงบนแดชบอร์ดผ่านตัวเลือก **เพิ่มไทล์**</span><span class="sxs-lookup"><span data-stu-id="acd2a-109">Besides tiles pinned from reports, *designers* can add standalone tiles directly on the dashboard using **Add tile**.</span></span> <span data-ttu-id="acd2a-110">ไทล์แบบเดี่ยวรวมถึง: กล่องข้อความ รูปภาพ วิดีโอ ข้อมูลสตรีมมิ่ง และเนื้อหาบนเว็บ</span><span class="sxs-lookup"><span data-stu-id="acd2a-110">Standalone tiles include: text boxes, images, videos, streaming data, and web content.</span></span>

<span data-ttu-id="acd2a-111">ต้องการความช่วยเหลือในการทำความเข้าใจเกี่ยวกับบล็อกที่ประกอบเป็น Power BI หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="acd2a-111">Need help understanding the building blocks that make up Power BI?</span></span>  <span data-ttu-id="acd2a-112">ดู[Power BI - แนวคิดพื้นฐาน](end-user-basic-concepts.md)</span><span class="sxs-lookup"><span data-stu-id="acd2a-112">See [Power BI - Basic Concepts](end-user-basic-concepts.md).</span></span>


## <a name="interacting-with-tiles-on-a-dashboard"></a><span data-ttu-id="acd2a-113">โต้ตอบกับไทล์บนแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="acd2a-113">Interacting with tiles on a dashboard</span></span>

1. <span data-ttu-id="acd2a-114">เลื่อนเหนือไทล์เพื่อแสดงจุดไข่ปลา</span><span class="sxs-lookup"><span data-stu-id="acd2a-114">Hover over the tile to display the ellipses.</span></span>
   
    ![จุดไข่ปลาไทล์](./media/end-user-tiles/power-bi-ellipsis.png)
2. <span data-ttu-id="acd2a-116">เลือกจุดไข่ปลาเพื่อเปิดเมนูการดำเนินการไทล์</span><span class="sxs-lookup"><span data-stu-id="acd2a-116">Select the ellipses to open the tile action menu.</span></span> <span data-ttu-id="acd2a-117">ตัวเลือกที่พร้อมใช้งานจะแตกต่างกันไปตามสิทธิ์ของคุณ ชนิดของภาพ และวิธีการที่ใช้ในการสร้างไทล์</span><span class="sxs-lookup"><span data-stu-id="acd2a-117">The options available vary by your permissions, the visual type, and the method used to create the tile.</span></span> <span data-ttu-id="acd2a-118">ตัวอย่างเช่น รายการเมนูที่พร้อมใช้งานสำหรับไทล์ที่ปักหมุดจากการถามตอบมีความแตกต่างจากไทล์ที่ปักหมุดจากรายงาน</span><span class="sxs-lookup"><span data-stu-id="acd2a-118">For example, the menu items available for tiles pinned from Q&A are different than the tiles pinned from a report.</span></span> <span data-ttu-id="acd2a-119">นี่คือเมนูการดำเนินการสำหรับไทล์ที่สร้างขึ้นโดยใช้การถามตอบ</span><span class="sxs-lookup"><span data-stu-id="acd2a-119">Here is an action menu for a tile created using Q&A.</span></span>


   
    ![สกรีนช็อตจะแสดงเมนูที่มีเก้าตัวเลือก](./media/end-user-tiles/power-bi-qna-menu.png)

   
    <span data-ttu-id="acd2a-121">บางการดำเนินการที่พร้อมใช้งานจากเมนูเหล่านี้ได้แก่:</span><span class="sxs-lookup"><span data-stu-id="acd2a-121">Some of the actions available from these menus are:</span></span>
   
   * <span data-ttu-id="acd2a-122">[เปิดรายงานที่ถูกใช้เพื่อสร้างไทล์](end-user-reports.md) ![ไอคอนรายงาน](./media/end-user-tiles/chart-icon.jpg)</span><span class="sxs-lookup"><span data-stu-id="acd2a-122">[Open the report that was used to create the tile ](end-user-reports.md) ![report icon](./media/end-user-tiles/chart-icon.jpg)</span></span>  
   
   * <span data-ttu-id="acd2a-123">[เปิดคำถามของ Q&A ที่ถูกใช้เพื่อสร้างไทล์](end-user-reports.md)![ไอคอน Q&A](./media/end-user-tiles/qna-icon.png)</span><span class="sxs-lookup"><span data-stu-id="acd2a-123">[Open the Q&A question that was used to create the tile ](end-user-reports.md) ![Q&A icon](./media/end-user-tiles/qna-icon.png)</span></span>  
   

   * <span data-ttu-id="acd2a-124">[เปิดสมุดงานที่ถูกใช้เพื่อสร้างไทล์](end-user-reports.md) ![ไอคอนแผ่นงาน](./media/end-user-tiles/power-bi-open-worksheet.png)</span><span class="sxs-lookup"><span data-stu-id="acd2a-124">[Open the workbook that was used to create the tile ](end-user-reports.md) ![worksheet icon](./media/end-user-tiles/power-bi-open-worksheet.png)</span></span>  
   * <span data-ttu-id="acd2a-125">[ดูไทล์ในโหมดโฟกัส](end-user-focus.md)![ไอคอนโฟกัส](./media/end-user-tiles/fullscreen-icon.jpg)</span><span class="sxs-lookup"><span data-stu-id="acd2a-125">[View the tile in focus mode ](end-user-focus.md) ![focus icon](./media/end-user-tiles/fullscreen-icon.jpg)</span></span>  
   * <span data-ttu-id="acd2a-126">[ดูข้อมูลเชิงลึก](end-user-insights.md)![ไอคอนข้อมูลเชิงลึก](./media/end-user-tiles/power-bi-insights.png)</span><span class="sxs-lookup"><span data-stu-id="acd2a-126">[View insights ](end-user-insights.md) ![insights icon](./media/end-user-tiles/power-bi-insights.png)</span></span>
   * <span data-ttu-id="acd2a-127">[เพิ่มข้อคิดเห็นและเริ่มการอภิปราย](end-user-comment.md) ![ไอคอนข้อคิดเห็น ](./media/end-user-tiles/comment-icons.png)</span><span class="sxs-lookup"><span data-stu-id="acd2a-127">[Add a comment and start a discussion](end-user-comment.md)  ![comment icon](./media/end-user-tiles/comment-icons.png)</span></span>
   * <span data-ttu-id="acd2a-128">[จัดการการแจ้งเตือนที่ตั้งค่าบนไทล์ของแดชบอร์ด](end-user-alerts.md) ![ไอคอนการแจ้งเตือน](./media/end-user-tiles/power-bi-alert-icon.png)</span><span class="sxs-lookup"><span data-stu-id="acd2a-128">[Manage alerts set on a dashboard tile](end-user-alerts.md)  ![alert icon](./media/end-user-tiles/power-bi-alert-icon.png)</span></span>
   * <span data-ttu-id="acd2a-129">[เปิดข้อมูลใน Excel](end-user-export.md)![ไอคอนการส่งออก](./media/end-user-tiles/power-bi-export-icon.png)</span><span class="sxs-lookup"><span data-stu-id="acd2a-129">[Open the data in Excel](end-user-export.md)  ![export icon](./media/end-user-tiles/power-bi-export-icon.png)</span></span>


3. <span data-ttu-id="acd2a-130">เมื่อต้องปิดเมนูการดำเนินการ เลือกพื้นที่ว่างในพื้นที่ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="acd2a-130">To close the action menu, select a blank area in the canvas.</span></span>

### <a name="select-click-a-tile"></a><span data-ttu-id="acd2a-131">เลือก (คลิกที่) ไทล์</span><span class="sxs-lookup"><span data-stu-id="acd2a-131">Select (click) a tile</span></span>
<span data-ttu-id="acd2a-132">เมื่อคุณเลือกไทล์หนึ่ง สิ่งที่จะเกิดขึ้นถัดไปขึ้นอยู่กับวิธีที่ไทล์ถูกสร้างขึ้น และขึ้นอยู่กับว่าไทล์ดังกล่าวมี[ลิงก์แบบกำหนดเอง](../create-reports/service-dashboard-edit-tile.md)หรือไม่</span><span class="sxs-lookup"><span data-stu-id="acd2a-132">When you select a tile, what happens next depends on how the tile was created and if it has a [custom link](../create-reports/service-dashboard-edit-tile.md).</span></span> <span data-ttu-id="acd2a-133">หากมีีการลิงก์แบบกำหนดเอง การเลือกไทล์จะนำคุณไปที่ลิงก์นั้น</span><span class="sxs-lookup"><span data-stu-id="acd2a-133">If it has a custom link, selecting the tile takes you to that link.</span></span> <span data-ttu-id="acd2a-134">มิฉะนั้น การเลือกไทล์จะนำคุณไปยังรายงาน สมุดงาน Excel Online รายงาน SSRS ที่อยู่ภายในองค์กร หรือการถามตอบที่ถูกใช้เพื่อสร้างไทล์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="acd2a-134">Otherwise, selecting the tile takes you to the report, Excel Online workbook, SSRS report that is on-premises, or Q&A question that was used to create the tile.</span></span>

> [!NOTE]
> <span data-ttu-id="acd2a-135">ข้อยกเว้นนี้คือไทล์วิดีโอที่เพิ่มไปยังแดชบอร์ดโดย *นักออกแบบ*</span><span class="sxs-lookup"><span data-stu-id="acd2a-135">The exception to this is video tiles added to dashboards by *designers*.</span></span> <span data-ttu-id="acd2a-136">การเลือกไทล์วิดีโอ (ที่ถูกสร้างขึ้นด้วยวิธีนี้) ทำให้วิดีโอเล่นบนแดชบอร์ดดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="acd2a-136">Selecting a video tile (that was created this way) causes the video to play right there on the dashboard.</span></span>   
> 
> 

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="acd2a-137">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="acd2a-137">Considerations and troubleshooting</span></span>
* <span data-ttu-id="acd2a-138">ถ้าไม่มีอะไรเกิดขึ้นเมื่อคุณเลือก (คลิก) ไทล์ หรือคุณได้รับข้อผิดพลาด ต่อไปนี้เป็นสาเหตุที่เป็นไปได้บางประการ:</span><span class="sxs-lookup"><span data-stu-id="acd2a-138">If nothing happens when you select (click) a tile, or you receive an error message, here are some possible reasons:</span></span>
  - <span data-ttu-id="acd2a-139">รายงานที่ถูกใช้เพื่อสร้างการแสดงภาพไม่ได้รับการบันทึก หรือถูกลบไปแล้ว</span><span class="sxs-lookup"><span data-stu-id="acd2a-139">The report that was used to create the visualization was not saved, or has been deleted.</span></span>
  - <span data-ttu-id="acd2a-140">ถ้าไทล์ถูกสร้างขึ้นจากเวิร์กบุ๊กใน Excel Online และคุณไม่มีสิทธิ์ในการอ่านสำหรับเวิร์กบุ๊กนั้นเป็นอย่างน้อย</span><span class="sxs-lookup"><span data-stu-id="acd2a-140">The tile was created from a workbook in Excel Online, and you do not have at least Read permissions for that workbook.</span></span>
  - <span data-ttu-id="acd2a-141">ถ้าไทล์ถูกสร้างขึ้นจาก SSRS และคุณไม่มีสิทธิ์ในรายงาน SSRS หรือคุณไม่สามารถเข้าถึงเครือข่ายที่เซิร์ฟเวอร์ SSRS อยู่ได้</span><span class="sxs-lookup"><span data-stu-id="acd2a-141">If the tile was created from SSRS, and you don't have permission to the SSRS report or you don't have access to the network where the SSRS server is located.</span></span>
* <span data-ttu-id="acd2a-142">สำหรับไทล์ที่สร้างขึ้นโดยตรงบนแดชบอร์ดโดยใช้ **เพิ่มไทล์** ถ้ามีการตั้งค่าไฮเปอร์ลิงก์แบบกำหนดเอง การเลือกชื่อเรื่อง ชื่อเรื่องรอง และหรือไทล์จะเปิด URL นั้น</span><span class="sxs-lookup"><span data-stu-id="acd2a-142">For tiles created directly on the dashboard using **Add tile**, if a custom hyperlink has been set, selecting the title, subtitle, and or tile will open that URL.</span></span>  <span data-ttu-id="acd2a-143">มิฉะนั้น ตามค่าเริ่มต้น การเลือกหนึ่งไทล์จากไทล์เหล่านี้ที่ถูกสร้างขึ้นโดยตรงบนแดชบอร์ดสำหรับรูปภาพหนึ่ง โค้ดของเว็บ หรือกล่องข้อความ จะไม่ก่อให้เกิดการดำเนินการใด</span><span class="sxs-lookup"><span data-stu-id="acd2a-143">Otherwise, by default, selecting one of these tiles created directly on the dashboard for an image, web code, or text box produces no action.</span></span>
* <span data-ttu-id="acd2a-144">ถ้าการแสดงภาพต้นฉบับที่ใช้เพื่อสร้างไทล์เปลี่ยนแปลง ไทล์ดังกล่าวจะไม่เปลี่ยนแปลงไปด้วย</span><span class="sxs-lookup"><span data-stu-id="acd2a-144">If the original visualization used to create the tile changes, the tile doesn't change.</span></span>  <span data-ttu-id="acd2a-145">ตัวอย่างเช่น ถ้า *ผู้ออกแบบ* ปักหมุดแผนภูมิเส้นจากรายงาน จากนั้นคุณเปลี่ยนแผนภูมิเส้นเป็นแผนภูมิแท่ง ไทล์แดชบอร์ดจะยังคงแสดงแผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="acd2a-145">For example, if the *designer* pinned a line chart from a report and then changed the line chart to a bar chart, the dashboard tile continues to show a line chart.</span></span> <span data-ttu-id="acd2a-146">รีเฟรชข้อมูลแต่การชนิดแสดงภาพไม่เปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="acd2a-146">The data refreshes, but the visualization type does not.</span></span>

## <a name="next-steps"></a><span data-ttu-id="acd2a-147">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="acd2a-147">Next steps</span></span>
[<span data-ttu-id="acd2a-148">รีเฟรชข้อมูล</span><span class="sxs-lookup"><span data-stu-id="acd2a-148">Data refresh</span></span>](../connect-data/refresh-data.md)

[<span data-ttu-id="acd2a-149">Power BI แนวคิดพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="acd2a-149">Power BI - Basic Concepts</span></span>](end-user-basic-concepts.md)


