---
title: เรียกใช้และดูข้อมูลเชิงลึกบนไทล์แดชบอร์ด
description: ในฐานะผู้ใช้งานปลายทางของ Power BI เรียนรู้วิธีการรับข้อมูลเชิงลึกเกี่ยวกับไทล์ของชุดข้อมูลและแดชบอร์ดของคุณ
author: mihart
ms.reviewer: mihart
featuredvideoid: et_MLSL2sA8
ms.service: powerbi
ms.subservice: powerbi-consumer
ms.topic: conceptual
ms.date: 09/09/2020
ms.author: mihart
LocalizationGroup: Dashboards
ms.openlocfilehash: 21bccbd11f8d2060b648e22c8ed8aa9471c820f0
ms.sourcegitcommit: 002c140d0eae3137a137e9a855486af6c55ad957
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/10/2020
ms.locfileid: "89642555"
---
# <a name="view-data-insights-on-dashboard-tiles-with-power-bi"></a><span data-ttu-id="53c34-103">ดูข้อมูลเชิงลึกบนไทล์แดชบอร์ดด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="53c34-103">View data insights on dashboard tiles with Power BI</span></span>

[!INCLUDE[consumer-appliesto-yyny](../includes/consumer-appliesto-yyny.md)]

<span data-ttu-id="53c34-104">[ไทล์](end-user-tiles.md)การแสดงผลแต่ละส่วนที่แดชบอร์ดของคุณจะเป็นช่องทางไปสู่การสืบค้นข้อมูล</span><span class="sxs-lookup"><span data-stu-id="53c34-104">Each visual [tile](end-user-tiles.md) on your dashboard is a doorway into data exploration.</span></span> <span data-ttu-id="53c34-105">เมื่อคุณเลือกไทล์ รายงานจะถูกเปิดขึ้นมา หรือเป็นการ[เปิดส่วนถามตอบ](end-user-q-and-a.md)เพื่อให้คุณสามารถกรอกและจัดเรียงและเจาะรายละเอียดชุดข้อมูลในรายงานดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="53c34-105">When you select a tile, it opens a report or [opens Q&A](end-user-q-and-a.md) where you can filter and sort and dig into the dataset behind the report.</span></span> <span data-ttu-id="53c34-106">และเมื่อคุณเรียกใช้ข้อมูลเชิงลึก Power BI จะสำรวจข้อมูลให้คุณ</span><span class="sxs-lookup"><span data-stu-id="53c34-106">And when you run insights, Power BI does the data exploration for you.</span></span>

![โหมดเมนูจุดไข่ปลาที่แสดงข้อมูลเชิงลึกของมุมมองในฐานะตัวเลือก](./media/end-user-insights/power-bi-insight.png)

<span data-ttu-id="53c34-108">เรียกใช้ข้อมูลเชิงลึกเพื่อจัดทำส่วนการแสดงผลอินเทอร์แอคทีฟที่น่าสนใจที่ยึดตามข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="53c34-108">Run insights to generate interesting interactive visuals based on your data.</span></span> <span data-ttu-id="53c34-109">สามารถเรียกใช้ข้อมูลเชิงลึกบนไทล์ของแดชบอร์ดเฉพาะและคุณยังสามารถเรียกใช้ข้อมูลเชิงลึกในข้อมูลเชิงลึกได้!</span><span class="sxs-lookup"><span data-stu-id="53c34-109">Insights can be run on a specific dashboard tile and you can even run insights on an insight!</span></span>

<span data-ttu-id="53c34-110">ฟีเจอร์ข้อมูลเชิงลึกมีอยู่แล้วภายในการเติบโต[ชุดของอัลกอริทึมวิเคราะห์ขั้นสูง](end-user-insight-types.md)พัฒนาขึ้นร่วมกับ Microsoft ค้นคว้าที่เราจะยังคงใช้การอนุญาตให้บุคคลเพิ่มเติมเมื่อต้องการค้นหาข้อมูลเชิงลึกในข้อมูลของพวกเขาในด้วยวิธีใหม่ ๆ</span><span class="sxs-lookup"><span data-stu-id="53c34-110">The insights feature is built on a growing [set of advanced analytical algorithms](end-user-insight-types.md) developed in conjunction with Microsoft Research that we'll continue to use to allow more people to find insights in their data in new and intuitive ways.</span></span>

## <a name="run-insights-on-a-dashboard-tile"></a><span data-ttu-id="53c34-111">เรียกใช้ข้อมูลเชิงลึกบนไทล์แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="53c34-111">Run insights on a dashboard tile</span></span>
<span data-ttu-id="53c34-112">เมื่อคุณเรียกใช้ข้อมูลเชิงลึกบนไทล์ของแดชบอร์ด Power BI จะค้นหาเฉพาะข้อมูลที่ใช้ในการสร้างไทล์ของแดชบอร์ดเดียว</span><span class="sxs-lookup"><span data-stu-id="53c34-112">When you run insights on a dashboard tile, Power BI searches just the data used to create that single dashboard tile.</span></span> 

1. <span data-ttu-id="53c34-113">[เปิดแดชบอร์ด](end-user-dashboards.md)</span><span class="sxs-lookup"><span data-stu-id="53c34-113">[Open a dashboard](end-user-dashboards.md).</span></span>
2. <span data-ttu-id="53c34-114">เลื่อนไปเหนือไทล์</span><span class="sxs-lookup"><span data-stu-id="53c34-114">Hover over a tile.</span></span> <span data-ttu-id="53c34-115">เลือก**ตัวเลือกเพิ่มเติม** (...) และเลือก**ดูข้อมูลเชิงลึก**</span><span class="sxs-lookup"><span data-stu-id="53c34-115">select **More options** (...), and choose **View insights**.</span></span> 

    ![สกรีนช็อตที่แสดงการเลือกแสดงรายการแบบหล่นลงรูปจุดไข่ปลา](./media/end-user-insights/power-bi-hover.png)


3. <span data-ttu-id="53c34-117">ไทล์เปิดขึ้นใน[โหมดโฟกัส](end-user-focus.md)ด้วยข้อมูลเชิงลึกการ์ดที่แสดงตามแนวทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="53c34-117">The tile opens in [Focus mode](end-user-focus.md) with the insights cards displayed along the right.</span></span>    
   
    ![โหมดโฟกัส](./media/end-user-insights/power-bi-insights-tiles.png)    
4. <span data-ttu-id="53c34-119">ข้อมูลเชิงลึกกระตุ้นความสนใจของคุณหรือไม่</span><span class="sxs-lookup"><span data-stu-id="53c34-119">Does one insight pique your interest?</span></span> <span data-ttu-id="53c34-120">เลือกบัตรข้อมูลเชิงลึกเพื่อเจาะลึกเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="53c34-120">Select that insight card to dig further.</span></span> <span data-ttu-id="53c34-121">ข้อมูลเชิงลึกแสดงทางด้านซ้าย และการ์ดใหม่ เท่านั้นตามข้อมูลในข้อมูลเชิงลึกที่เดียว แสดงตามแนวทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="53c34-121">The selected insight appears on the left and new insight cards, based solely on the data in that single insight, display along the right.</span></span>    

 ## <a name="interact-with-the-insight-cards"></a><span data-ttu-id="53c34-122">โต้ตอบกับบัตรข้อมูลเชิงลึก</span><span class="sxs-lookup"><span data-stu-id="53c34-122">Interact with the insight cards</span></span>
<span data-ttu-id="53c34-123">เมื่อคุณเปิดข้อมูลเชิงลึกแล้ว ให้สำรวจต่อไป</span><span class="sxs-lookup"><span data-stu-id="53c34-123">Once you have an insight open, continue exploring.</span></span>

   * <span data-ttu-id="53c34-124">กรองวิชวลบนพื้นที่</span><span class="sxs-lookup"><span data-stu-id="53c34-124">Filter the visual on the canvas.</span></span>  <span data-ttu-id="53c34-125">แสดงตัวกรอง โดยเลือกลูกศรเพื่อขยายบานหน้าต่างตัวกรองในมุมบนขวา</span><span class="sxs-lookup"><span data-stu-id="53c34-125">To display the filters, in the upper right corner, select the arrow to expand the Filters pane.</span></span>

      ![ขยายเมนูที่มีตัวกรองข้อมูลเชิงลึกแล้ว](./media/end-user-insights/power-bi-filter.png)
   
   * <span data-ttu-id="53c34-127">เรียกใช้ข้อมูลเชิงลึกบนบัตรข้อมูลเชิงลึก</span><span class="sxs-lookup"><span data-stu-id="53c34-127">Run insights on the insight card itself.</span></span> <span data-ttu-id="53c34-128">ซึ่งมักจะเรียกว่า**ข้อมูลเชิงลึกที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="53c34-128">This is often referred to as **related insights**.</span></span> <span data-ttu-id="53c34-129">เลือกการ์ดข้อมูลเชิงลึกเพื่อใช้งาน</span><span class="sxs-lookup"><span data-stu-id="53c34-129">Select an insight card to make it active.</span></span> <span data-ttu-id="53c34-130">การ์ดจะเลื่อนไปที่ด้านซ้าย และการ์ดใหม่ตามข้อมูลเฉพาะในข้อมูลเชิงลึกนั้นเท่านั้นที่จะแสดงตามแนวทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="53c34-130">It will move to the left side of the report canvas, and new cards, based solely on the data in that single insight,will  display along the right.</span></span>
   
      ![ข้อมูลเชิงลึกที่เกี่ยวข้องและเมนูตัวกรองที่ขยายแล้ว](./media/end-user-insights/power-bi-insights-card.png)
   
     
<span data-ttu-id="53c34-132">กลับไปที่รายงานของคุณ โดยเลือก **ออกจากโหมดโฟกัส**จากมุมด้านซ้ายบน</span><span class="sxs-lookup"><span data-stu-id="53c34-132">To return to your report, from the upper left corner, select **Exit Focus mode**.</span></span>

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="53c34-133">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="53c34-133">Considerations and troubleshooting</span></span>
- <span data-ttu-id="53c34-134">**ดูข้อมูลเชิงลึก**ใช้ไม่ได้กับชนิดไทล์ของแดชบอร์ดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="53c34-134">**View insights** doesn't work with all dashboard tile types.</span></span> <span data-ttu-id="53c34-135">เช่น ไม่พร้อมใช้งานสำหรับวิชวลแบบกำหนดเองของ Power BI</span><span class="sxs-lookup"><span data-stu-id="53c34-135">For example, it is not available for Power BI custom visuals.</span></span><!--[Power BI visuals](end-user-custom-visuals.md)-->


## <a name="next-steps"></a><span data-ttu-id="53c34-136">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="53c34-136">Next steps</span></span>

<span data-ttu-id="53c34-137">เรียกใช้ข้อมูลเชิงลึกบนวิชวลรายงาน [โดยใช้คุณลักษณะการวิเคราะห์](end-user-analyze-visuals.md)  </span><span class="sxs-lookup"><span data-stu-id="53c34-137">Run insights on report visuals [using the Analyze feature](end-user-analyze-visuals.md)  </span></span>  
<span data-ttu-id="53c34-138">เรียนรู้เกี่ยวกับ[ชนิดของข้อมูลเชิงลึกที่พร้อมใช้งาน](end-user-insight-types.md)</span><span class="sxs-lookup"><span data-stu-id="53c34-138">Learn about the [types of Insights available](end-user-insight-types.md)</span></span>

