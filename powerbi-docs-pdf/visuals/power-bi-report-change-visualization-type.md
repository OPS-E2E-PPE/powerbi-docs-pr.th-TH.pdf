---
title: เปลี่ยนชนิดของการแสดงภาพในรายงาน
description: เปลี่ยนชนิดของการแสดงภาพในรายงาน ในบริการของ Power BI และ Power BI Desktop
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 12/28/2019
LocalizationGroup: Visualizations
ms.openlocfilehash: 45afac9e1905527ef41a9d8a00a21e29f8b56e61
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412448"
---
# <a name="change-the-type-of-visualization-in-a-power-bi-report"></a><span data-ttu-id="69f27-103">เปลี่ยนชนิดของการแสดงภาพในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="69f27-103">Change the type of visualization in a Power BI report</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]    

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

## <a name="select-a-new-visualization-type"></a><span data-ttu-id="69f27-104">เลือกประเภทการแสดงภาพใหม่</span><span class="sxs-lookup"><span data-stu-id="69f27-104">Select a new visualization type</span></span>

<span data-ttu-id="69f27-105">ลองการแสดงภาพชนิดต่าง ๆ ในบริการของ Power BI และ Power BI Desktop เพื่อดูว่าแบบไหนช่วยให้เห็นข้อมูลของคุณได้ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="69f27-105">Try different types of visualizations in the Power BI service and Power BI Desktop to see which one illustrates your data best.</span></span> 

1. <span data-ttu-id="69f27-106">เปิดรายงานที่มีการแสดงภาพอย่างน้อยหนึ่งภาพ</span><span class="sxs-lookup"><span data-stu-id="69f27-106">Open a report that already has at least one visualization.</span></span>   
2. <span data-ttu-id="69f27-107">เลือกการแสดงภาพเพื่อเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="69f27-107">Select a visualization to make it active.</span></span> <span data-ttu-id="69f27-108">การแสดงภาพที่ใช้งานอยู่มีจุดจับและเส้นขอบ</span><span class="sxs-lookup"><span data-stu-id="69f27-108">An active visualization has handles and a border.</span></span>    
3. <span data-ttu-id="69f27-109">ในบานหน้าต่างการแสดงภาพ เลือกชนิดของการแสดงภาพใหม่</span><span class="sxs-lookup"><span data-stu-id="69f27-109">In the Visualizations pane, select the new visualization type.</span></span> 
   
   ![วิดีโอที่แสดงการเปลี่ยนแผนภูมิคอลัมน์ไปเป็นแผนภูมิเส้น](media/power-bi-report-change-visualization-type/change-viz/change-viz.gif)<span data-ttu-id="69f27-111">.</span><span class="sxs-lookup"><span data-stu-id="69f27-111">.</span></span>
4. <span data-ttu-id="69f27-112">(ตัวเลือก) [ปักหมุดการแสดงภาพของคุณ](../create-reports/service-dashboard-pin-tile-from-report.md)ไปยังแดชบอร์ดให้เป็นไทล์ได้</span><span class="sxs-lookup"><span data-stu-id="69f27-112">(Optional) [Pin your visualization](../create-reports/service-dashboard-pin-tile-from-report.md) to your dashboard as a tile.</span></span> 

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="69f27-113">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="69f27-113">Considerations and troubleshooting</span></span>
<span data-ttu-id="69f27-114">ถ้าคุณเปลี่ยนชนิดการแสดงภาพในรายงานหลังจากที่คุณปักหมุดไปยังแดชบอร์ด ไทล์จะไม่ถูกอัปเดตโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="69f27-114">If you change the visualization type in the report after you pinned it to your dashboard, the dashboard tile does not automatically update.</span></span> <span data-ttu-id="69f27-115">ดังนั้นหากคุณใช้บริการของ Power BI ในการปักหมุดการแสดงผลข้อมูลด้วยภาพเป็นแผนภูมิเส้น จากนั้นในรายงาน คุณเปลี่ยนเป็นแผนภูมิแท่ง แผนภูมิที่ปักหมุดไว้แล้วของข้อมูลนี้จะยังคงเป็นแผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="69f27-115">So, if you used the Power BI service to pin the visualization as a line chart and then, in the report, changed it to a bar chart, the already-pinned version of this data will remain a line chart.</span></span> <span data-ttu-id="69f27-116">ปักหมุดแผนภูมิแท่งเพื่อแสดงบนแดชบอร์ดด้วย</span><span class="sxs-lookup"><span data-stu-id="69f27-116">Pin the bar chart to see it too on the dashboard.</span></span>

<span data-ttu-id="69f27-117">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="69f27-117">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span> <span data-ttu-id="69f27-118">ดู [การแชร์รายงาน](../collaborate-share/service-share-reports.md)</span><span class="sxs-lookup"><span data-stu-id="69f27-118">See [sharing reports](../collaborate-share/service-share-reports.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="69f27-119">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="69f27-119">Next steps</span></span>
<span data-ttu-id="69f27-120">อ่านข้อมูลเพิ่มเติมเกี่ยวกับ[การแสดงภาพในรายงาน Power BI](power-bi-report-visualizations.md)</span><span class="sxs-lookup"><span data-stu-id="69f27-120">More about [Visualizations in Power BI reports](power-bi-report-visualizations.md)</span></span>

[<span data-ttu-id="69f27-121">Power BI แนวคิดพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="69f27-121">Power BI - Basic Concepts</span></span>](../consumer/end-user-basic-concepts.md)

<span data-ttu-id="69f27-122">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="69f27-122">More questions?</span></span> [<span data-ttu-id="69f27-123">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="69f27-123">Try the Power BI Community</span></span>](https://community.powerbi.com/)

