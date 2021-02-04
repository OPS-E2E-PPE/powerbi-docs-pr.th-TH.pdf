---
title: ปักหมุดไทล์ไปยังแดชบอร์ด Power BI จากรายงาน
description: ปักหมุดไทล์ไปยังแดชบอร์ด Power BI จากรายงาน
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: lJKgWnvl6bQ
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 12/03/2020
LocalizationGroup: Dashboards
ms.openlocfilehash: ad3a38fa8aef4f5404196213ebd3c7b26d3fc3b8
ms.sourcegitcommit: cb6e0202de27f29dd622e47b305c15f952c5769b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/03/2020
ms.locfileid: "96578417"
---
# <a name="pin-a-tile-to-a-power-bi-dashboard-from-a-report"></a><span data-ttu-id="245ce-103">ปักหมุดไทล์ไปยังแดชบอร์ด Power BI จากรายงาน</span><span class="sxs-lookup"><span data-stu-id="245ce-103">Pin a tile to a Power BI dashboard from a report</span></span>

<span data-ttu-id="245ce-104">วิธีหนึ่งในการเพิ่ม[ไทล์แดชบอร์ด](../consumer/end-user-tiles.md)ใหม นั้นมาจากภายใน [รายงาน Power BI](../consumer/end-user-reports.md)</span><span class="sxs-lookup"><span data-stu-id="245ce-104">One way to add a [dashboard tile](../consumer/end-user-tiles.md) is from within a [Power BI report](../consumer/end-user-reports.md).</span></span> <span data-ttu-id="245ce-105">เมื่อคุณเลือกหนึ่งในไทล์เหล่านี้ ไทล์จะเปิดขึ้นในรายงาน</span><span class="sxs-lookup"><span data-stu-id="245ce-105">When you select one of these tiles, it opens in the report.</span></span>

<span data-ttu-id="245ce-106">หน้ารายงานทั้งหมดสามารถปักหมุดไปยังแดชบอร์ด ซึ่งเรียกว่าการปักหมุดไทล์ *สด*</span><span class="sxs-lookup"><span data-stu-id="245ce-106">An entire report page can be pinned to a dashboard, which is called pinning a *live* tile.</span></span> <span data-ttu-id="245ce-107">ที่เรียกกันว่าไทล์สดเนื่องจากคุณสามารถโต้ตอบกับไทล์บนแดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="245ce-107">It's called a live tile because you can interact with the tile on the dashboard.</span></span> <span data-ttu-id="245ce-108">การเปลี่ยนแปลงที่ทำในรายงานจะซิงค์กับแดชบอร์ดโดยอัตโนมัติ ซึ่งแตกต่างกับไทล์การแสดงข้อมูลด้วยภาพแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="245ce-108">Unlike with individual visualization tiles, changes made in the report are automatically synced with the dashboard.</span></span> <span data-ttu-id="245ce-109">สำหรับข้อมูลเพิ่มเติม ให้ดู[ปักหมุดหน้ารายงานทั้งหน้า](#pin-an-entire-report-page)</span><span class="sxs-lookup"><span data-stu-id="245ce-109">For more information, see [Pin an entire report page](#pin-an-entire-report-page).</span></span>

<span data-ttu-id="245ce-110">คุณไม่สามารถปักหมุดไทล์ จากรายงานที่มีการแชร์กับคุณ หรือจาก Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="245ce-110">You can't pin tiles from reports that have been shared with you or from Power BI Desktop.</span></span> 

> [!TIP]
> <span data-ttu-id="245ce-111">เนื่องจากการแสดงข้อมูลด้วยภาพบางรายการมีการใช้ภาพพื้นหลัง การปักหมุดอาจไม่ทำงานหากภาพพื้นหลังมีขนาดใหญ่เกินไป</span><span class="sxs-lookup"><span data-stu-id="245ce-111">Because some visualizations use background images, pinning might not work if the background image is too large.</span></span> <span data-ttu-id="245ce-112">ลองลดขนาดรูปภาพ หรือโดยใช้การบีบอัดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="245ce-112">Try reducing the image size or using image compression.</span></span>  
> 
> 

## <a name="pin-a-tile-from-a-report"></a><span data-ttu-id="245ce-113">ปักหมุดไทล์จากรายงาน</span><span class="sxs-lookup"><span data-stu-id="245ce-113">Pin a tile from a report</span></span>
<span data-ttu-id="245ce-114">ดู Amanda สร้างแดชบอร์ดโดยการปักหมุดภาพและรูปภาพจากรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="245ce-114">Watch Amanda create a dashboard by pinning visuals and images from a Power BI report.</span></span>
    

<iframe width="560" height="315" src="https://www.youtube.com/embed/lJKgWnvl6bQ" frameborder="0" allowfullscreen></iframe>

<span data-ttu-id="245ce-115">ในตอนนี้ ให้สร้างแดชบอร์ดของคุณเองโดยใช้หนึ่งในตัวอย่างรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="245ce-115">Now create your own dashboard by using one of the Power BI sample reports.</span></span>

1. <span data-ttu-id="245ce-116">ในรายงาน ให้วางเคอร์เซอร์เหนือการแสดงข้อมูลด้วยภาพที่คุณต้องการปักหมุด แล้วเลือกไอคอนเข็มหมุด</span><span class="sxs-lookup"><span data-stu-id="245ce-116">In the report, hover over the visualization you want to pin, and select the pin icon.</span></span> <span data-ttu-id="245ce-117">![ไอคอนเข็มหมุด](media/service-dashboard-pin-tile-from-report/pbi_pintile_small.png)</span><span class="sxs-lookup"><span data-stu-id="245ce-117">![Pin icon](media/service-dashboard-pin-tile-from-report/pbi_pintile_small.png).</span></span> <span data-ttu-id="245ce-118">Power BI เปิดขึ้นในหน้าจอ **ปักหมุดลงในแดชบอร์ด**</span><span class="sxs-lookup"><span data-stu-id="245ce-118">Power BI opens the **Pin to dashboard** screen.</span></span>
   
     ![ได้ปักหมุดหน้าต่างแดชบอร์ด](media/service-dashboard-pin-tile-from-report/pbi_themes2.png)
2. <span data-ttu-id="245ce-120">เลือกว่า คุณต้องการปักหมุดไปยังแดชบอร์ดที่มีอยู่ หรือสร้างแดชบอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="245ce-120">Select whether to pin to an existing dashboard or new dashboard.</span></span>
   
   * <span data-ttu-id="245ce-121">**แดชบอร์ดที่มีอยู่**: ให้เลือกชื่อของแดชบอร์ดจากรายการแบบดึงลง</span><span class="sxs-lookup"><span data-stu-id="245ce-121">**Existing dashboard**: Select the name of the dashboard from the dropdown.</span></span> <span data-ttu-id="245ce-122">แดชบอร์ดที่แชร์กับคุณจะไม่ปรากฏขึ้นที่นี่</span><span class="sxs-lookup"><span data-stu-id="245ce-122">Dashboards that have been shared with you won't appear in the dropdown.</span></span>
   * <span data-ttu-id="245ce-123">**แดชบอร์ดใหม่**: ป้อนชื่อของแดชบอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="245ce-123">**New dashboard**: Enter the name of the new dashboard.</span></span>
3. <span data-ttu-id="245ce-124">ในบางกรณี รายการที่คุณปักหมุดอาจจะมี *ธีม* ที่ถูกนำไปใช้อยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="245ce-124">In some cases, the item you're pinning might have a *theme* already applied.</span></span> <span data-ttu-id="245ce-125">ตัวอย่างเช่น ภาพปักหมุดจากสมุดงาน Excel</span><span class="sxs-lookup"><span data-stu-id="245ce-125">For example, visuals pinned from an Excel workbook.</span></span> <span data-ttu-id="245ce-126">ถ้าเป็นเช่นนั้น เลือกชุดรูปแบบที่จะใช้กับไทล์</span><span class="sxs-lookup"><span data-stu-id="245ce-126">If so, select which theme to apply to the tile.</span></span>
4. <span data-ttu-id="245ce-127">เลือก **หมุด**</span><span class="sxs-lookup"><span data-stu-id="245ce-127">Select **Pin**.</span></span>
   
   <span data-ttu-id="245ce-128">ข้อความว่าสำเร็จแล้ว (ใกล้กับมุมบนขวา) ช่วยให้คุณทราบว่าได้เพิ่มการแสดงข้อมูลด้วยภาพเป็นไทล์ลงในแดชบอร์ดของคุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="245ce-128">A success message (near the top-right corner) informs you the visualization was added, as a tile, to your dashboard.</span></span>
   
   ![ข้อความแสดงความสำเร็จ](media/service-dashboard-pin-tile-from-report/pinsuccess.png)
5. <span data-ttu-id="245ce-130">จากบานหน้าต่างนำทาง ให้เลือกแดชบอร์ดที่มีไทล์ใหม่</span><span class="sxs-lookup"><span data-stu-id="245ce-130">From the nav pane, select the dashboard with the new tile.</span></span> <span data-ttu-id="245ce-131">[แก้ไขการแสดงไทล์และลักษณะการทำงาน](service-dashboard-edit-tile.md)หรือเลือกไทล์เพื่อกลับไปยังรายงาน</span><span class="sxs-lookup"><span data-stu-id="245ce-131">[Edit the tile display and behavior](service-dashboard-edit-tile.md) or select the tile to return to the report.</span></span>

## <a name="pin-an-entire-report-page"></a><span data-ttu-id="245ce-132">ปักหมุดทั้งหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="245ce-132">Pin an entire report page</span></span>
<span data-ttu-id="245ce-133">อีกหนึ่งตัวเลือกก็คือ การปักหมุดหน้ารายงานทั้งหมดไปยังแดชบอร์ด ซึ่งเป็นวิธีง่าย ๆ ในการปักหมุดการแสดงข้อมูลด้วยภาพมากกว่าหนึ่งรายการในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="245ce-133">Another option is to pin an entire report page to a dashboard, which is an easy way to pin more than one visualization at a time.</span></span> <span data-ttu-id="245ce-134">เมื่อคุณปักหมุดหน้ารายงานทั้งหน้า ไทล์จะเป็นแบบ *สด*</span><span class="sxs-lookup"><span data-stu-id="245ce-134">When you pin an entire page, the tiles are *live*.</span></span> <span data-ttu-id="245ce-135">นั่นก็คือ คุณสามารถโต้ตอบกับไทล์บนแดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="245ce-135">That is, you can interact with them there on the dashboard.</span></span> <span data-ttu-id="245ce-136">การเปลี่ยนแปลงที่คุณทำกับการแสดงข้อมูลลด้วยภาพในตัวแก้ไขรายงาน เช่นการเพิ่มตัวกรองหรือการเปลี่ยนแปลงเขตข้อมูลที่ใช้ในแผนภูมิ จะปรากฏในไทล์แดชบอร์ดด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="245ce-136">Changes you make to any of the visualizations in the report editor, like adding a filter or changing the fields used in the chart, are reflected in the dashboard tile as well.</span></span>  

<span data-ttu-id="245ce-137">สำหรับข้อมูลเพิ่มเติม ให้ดู[ปักหมุดหน้ารายงานทั้งหน้า](service-dashboard-pin-live-tile-from-report.md)</span><span class="sxs-lookup"><span data-stu-id="245ce-137">For more information, see [Pin an entire report page](service-dashboard-pin-live-tile-from-report.md).</span></span>

## <a name="limitations"></a><span data-ttu-id="245ce-138">ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="245ce-138">Limitations</span></span>
<span data-ttu-id="245ce-139">ตัวเลือกการจัดรูปแบบรายงานหรือธีมบางอย่างจะไม่นำไปใช้กับวิชวลเมื่อคุณปักหมุดไว้ที่แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="245ce-139">Some report formatting options or themes aren't applied to visuals when you pin them to a dashboard.</span></span>
- <span data-ttu-id="245ce-140">การตั้งค่าเส้นขอบ เงา และพื้นหลังจะถูกละเว้นในไทล์ที่ปักหมุดไว้</span><span class="sxs-lookup"><span data-stu-id="245ce-140">Border, shadow, and background settings are ignored in the pinned tile.</span></span>
- <span data-ttu-id="245ce-141">สำหรับวิชวลการ์ดจะมีการแสดงข้อความที่ใช้สำหรับค่าในแดชบอร์ดโดยใช้ตระกูลฟอนต์ 'DIN' พร้อมข้อความสีดำ</span><span class="sxs-lookup"><span data-stu-id="245ce-141">For card visuals, the text used for the value is shown in dashboards using the 'DIN' font family, with black text.</span></span> <span data-ttu-id="245ce-142">คุณสามารถเปลี่ยนสีข้อความสำหรับไทล์ทั้งหมดบนแดชบอร์ดได้โดย[การสร้างธีมแดชบอร์ดที่กำหนดเอง](service-dashboard-themes.md)</span><span class="sxs-lookup"><span data-stu-id="245ce-142">You can change the text color for all the tiles on a dashboard by [creating a custom dashboard theme](service-dashboard-themes.md).</span></span>
- <span data-ttu-id="245ce-143">การจัดรูปแบบตามเงื่อนไขในตารางไม่ถูกนำมาใช้</span><span class="sxs-lookup"><span data-stu-id="245ce-143">Conditional formatting isn't applied.</span></span>
- <span data-ttu-id="245ce-144">วิชวลจะปรับขนาดของตัวเองให้พอดีกับขนาดของไทล์</span><span class="sxs-lookup"><span data-stu-id="245ce-144">Visuals will adjust their size to fit the size of the tile.</span></span> <span data-ttu-id="245ce-145">ซึ่งอาจส่งผลให้เกิดความแตกต่างในเค้าโครง ราวกับว่ามีการปรับขนาดวิชวลใหม่อีกครั้งบนรายงาน</span><span class="sxs-lookup"><span data-stu-id="245ce-145">This can result in differences in layout as if the visual had been resized on the report.</span></span>

## <a name="next-steps"></a><span data-ttu-id="245ce-146">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="245ce-146">Next steps</span></span>
- [<span data-ttu-id="245ce-147">แดชบอร์ดสำหรับผู้บริโภคบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="245ce-147">Dashboards for Power BI service consumers</span></span>](../consumer/end-user-dashboards.md)
- [<span data-ttu-id="245ce-148">ไทล์แดชบอร์ดใน Power BI</span><span class="sxs-lookup"><span data-stu-id="245ce-148">Dashboard tiles in Power BI</span></span>](../consumer/end-user-tiles.md)
- [<span data-ttu-id="245ce-149">รายงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="245ce-149">Reports in Power BI</span></span>](../consumer/end-user-reports.md)
- [<span data-ttu-id="245ce-150">การรีเฟรชข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="245ce-150">Data refresh in Power BI</span></span>](../connect-data/refresh-data.md)
- [<span data-ttu-id="245ce-151">แนวคิดพื้นฐานสำหรับนักออกแบบในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="245ce-151">Basic concepts for designers in the Power BI service</span></span>](../fundamentals/service-basic-concepts.md)

<span data-ttu-id="245ce-152">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="245ce-152">More questions?</span></span> [<span data-ttu-id="245ce-153">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="245ce-153">Try the Power BI Community</span></span>](https://community.powerbi.com/)
