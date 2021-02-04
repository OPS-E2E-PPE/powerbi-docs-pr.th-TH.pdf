---
title: ปักหมุดไทล์จากแดชบอร์ดหนึ่งไปยังอีกแดชบอร์ด
description: ปักหมุดไทล์จากแดชบอร์ดหนึ่งไปยังอีกแดชบอร์ด
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 03/01/2018
LocalizationGroup: Dashboards
ms.openlocfilehash: 26da094f7ef7519d29faf4edea1574b6b15dddb1
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96388298"
---
# <a name="pin-a-tile-from-one-dashboard-to-another-dashboard"></a><span data-ttu-id="444f5-103">ปักหมุดไทล์จากแดชบอร์ดหนึ่งไปยังอีกแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="444f5-103">Pin a tile from one dashboard to another dashboard</span></span>
<span data-ttu-id="444f5-104">วิธีหนึ่งในการเพิ่ม[แดชบอร์ดไทล์](../consumer/end-user-tiles.md)ใหม่คือ การคัดลอกจากแดชบอร์ดอื่น</span><span class="sxs-lookup"><span data-stu-id="444f5-104">One way to add a new [dashboard tile](../consumer/end-user-tiles.md) is by copying it from another dashboard.</span></span> <span data-ttu-id="444f5-105">แต่ละไทล์เหล่านี้ เป็นลิงก์กลับไปยังตำแหน่งที่ถูกสร้างขึ้นเมื่อคลิก ใน Q&A หรือรายงาน</span><span class="sxs-lookup"><span data-stu-id="444f5-105">Each of these tiles, when clicked, is a link back to where it was created -- either in Q&A or a report.</span></span> 

> [!NOTE]
> <span data-ttu-id="444f5-106">คุณไม่สามารถปักหมุดไทล์จากแดชบอร์ดทแชร์ได้</span><span class="sxs-lookup"><span data-stu-id="444f5-106">You cannot pin tiles from shared dashboards.</span></span>

## <a name="pin-a-tile-to-another-dashboard"></a><span data-ttu-id="444f5-107">ปักหมุดไทล์ไปยังแดชบอร์ดอื่น</span><span class="sxs-lookup"><span data-stu-id="444f5-107">Pin a tile to another dashboard</span></span>
1. <span data-ttu-id="444f5-108">[รับข้อมูล](../connect-data/service-get-data.md)</span><span class="sxs-lookup"><span data-stu-id="444f5-108">[Get data](../connect-data/service-get-data.md).</span></span> <span data-ttu-id="444f5-109">ตัวอย่างนี้จะใช้[ตัวอย่างการวิเคราะห IT Spend Analysis ](sample-it-spend.md)</span><span class="sxs-lookup"><span data-stu-id="444f5-109">This example uses the [IT Spend Analysis sample](sample-it-spend.md).</span></span>
2. <span data-ttu-id="444f5-110">เปิด[แดชบอร์ด](../consumer/end-user-dashboards.md)</span><span class="sxs-lookup"><span data-stu-id="444f5-110">Open a [dashboard](../consumer/end-user-dashboards.md).</span></span>
3. <span data-ttu-id="444f5-111">วางเมาส์เหนือที่ไทล์คุณต้องการปักหมุด เลือก **ตัวเลือกเพิ่มเติม** (...) และเลือก **ปักหมุดไทล์**</span><span class="sxs-lookup"><span data-stu-id="444f5-111">Hover over the tile you want to pin, select **More options** (...) and choose **Pin tile**.</span></span>  
   
   ![เมนูจุดไข่ปลา](media/service-pin-tile-to-another-dashboard/power-bi-pin-another-dash.png)
4. <span data-ttu-id="444f5-113">ปักหมุดไทล์ลงในแดชบอร์ดที่มีอยู่ หรือแดชบอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="444f5-113">Pin the tile to an existing dashboard or to a new dashboard.</span></span> 
   
   * <span data-ttu-id="444f5-114">**แดชบอร์ดที่มีอยู่** ให้เลือกชื่อของแดชบอร์ดจากรายการแบบดร๊อปดาวน์</span><span class="sxs-lookup"><span data-stu-id="444f5-114">**Existing dashboard**: select the name of the dashboard from the dropdown.</span></span>
   * <span data-ttu-id="444f5-115">**แดชบอร์ดใหม่** พิมพ์ชื่อของแดชบอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="444f5-115">**New dashboard**: type the name of the new dashboard.</span></span>
   
   ![ปักหมุดกล่องข้อความแดชบอร์ด](media/service-pin-tile-to-another-dashboard/pbi_pintoanotherdash.png)
5. <span data-ttu-id="444f5-117">เลือก **หมุด**</span><span class="sxs-lookup"><span data-stu-id="444f5-117">Select **Pin**.</span></span>
   <span data-ttu-id="444f5-118">ข้อความว่าสำเร็จแล้ว(ใกล้กับมุมบนขวา) ช่วยให้คุณทราบว่า การแสดงภาพถูกเพิ่มเป็นไทล์ ลงในแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="444f5-118">A Success message (near the top right corner) lets you know the visualization was added, as a tile, to the selected dashboard.</span></span>
   
   ![ได้ปักหมุดหน้าต่างแดชบอร์ด](media/service-pin-tile-to-another-dashboard/power-bi-pin-success.png)
6. <span data-ttu-id="444f5-120">เลือก **ไปยังแดชบอร์ด** เพื่อดูไทล์ใหม่</span><span class="sxs-lookup"><span data-stu-id="444f5-120">Select **Go to dashboard** to see the pinned tile.</span></span> <span data-ttu-id="444f5-121">ที่นั่น คุณสามารถ[เปลี่ยนชื่อ ปรับขนาด ลิงก์ และย้าย](service-dashboard-edit-tile.md)การแสดงภาพที่ปักหมุดไว้ได้</span><span class="sxs-lookup"><span data-stu-id="444f5-121">There, you can [rename, resize, link, and move](service-dashboard-edit-tile.md) the pinned visualization.</span></span>

## <a name="next-steps"></a><span data-ttu-id="444f5-122">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="444f5-122">Next steps</span></span>
[<span data-ttu-id="444f5-123">เปิด ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="444f5-123">Tiles in Power BI</span></span>](../consumer/end-user-tiles.md)  
[<span data-ttu-id="444f5-124">แดชบอร์ดใน Power BI</span><span class="sxs-lookup"><span data-stu-id="444f5-124">Dashboards in Power BI</span></span>](../consumer/end-user-dashboards.md)  
<span data-ttu-id="444f5-125">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="444f5-125">More questions?</span></span> [<span data-ttu-id="444f5-126">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="444f5-126">Try the Power BI Community</span></span>](https://community.powerbi.com/)
