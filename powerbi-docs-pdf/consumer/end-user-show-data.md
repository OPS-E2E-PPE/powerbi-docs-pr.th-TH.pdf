---
title: แสดงข้อมูลที่ใช้ในการสร้างส่วนการแสดงผลรายงาน
description: เอกสารนี้อธิบายว่าผู้ใช้ธุรกิจ Power BI สามารถ "ดู" ข้อมูลที่ใช้ในการสร้างส่วนการแสดงผลรายงานได้อย่างไร
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-explore
ms.topic: how-to
ms.date: 12/06/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: a4b9f7d25b9199e924d1b91a3b870730fc068fa3
ms.sourcegitcommit: 0bf42b6393cab7a37d21a52b934539cf300a08e2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/07/2020
ms.locfileid: "96781761"
---
# <a name="show-data-with-power-bi-reports"></a><span data-ttu-id="8efa5-103">แสดงข้อมูลพร้อมรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="8efa5-103">Show data with Power BI reports</span></span>

[!INCLUDE[consumer-appliesto-yyny](../includes/consumer-appliesto-yyny.md)]



<span data-ttu-id="8efa5-104">ระบบจะสร้างการแสดงผลด้วยภาพของ Power BI ขึ้นโดยใช้ข้อมูลจากชุดข้อมูลเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="8efa5-104">A Power BI visual is constructed using data from underlying datasets.</span></span> <span data-ttu-id="8efa5-105">หากคุณสนใจที่เห็นเบื้องหลัง Power BI ให้คุณสามารถ *แสดง* ข้อมูลที่กำลังกำลังมีการใช้เพื่อสร้างภาพดังกล่าวในรายงาน</span><span class="sxs-lookup"><span data-stu-id="8efa5-105">If you're interested in seeing behind-the-scenes, the Power BI service lets you *display* the data that is being used to create a visual in a report.</span></span> <span data-ttu-id="8efa5-106">เมื่อคุณเลือก **แสดงเป็นตาราง** Power BI จะแสดงข้อมูลด้านล่าง (หรือถัดจาก) วิชวล</span><span class="sxs-lookup"><span data-stu-id="8efa5-106">When you select **Show as a table**, Power BI displays the data below (or next to) the visual.</span></span>

<span data-ttu-id="8efa5-107">จากแดชบอร์ด สามารถดูข้อมูลที่เกี่ยวข้องได้โดยใช้ [ส่งออกเป็น Excel](end-user-export.md)</span><span class="sxs-lookup"><span data-stu-id="8efa5-107">On a dashboard, to see the underlying data, use [Export to Excel](end-user-export.md)</span></span>

## <a name="show-the-data-being-used-to-create-a-report-visual"></a><span data-ttu-id="8efa5-108">แสดงข้อมูลที่กำลังใช้เพื่อจัดทำส่วนการแสดงผลรายงาน</span><span class="sxs-lookup"><span data-stu-id="8efa5-108">Show the data being used to create a report visual</span></span>
1. <span data-ttu-id="8efa5-109">ในบริการของ Power BI ให้[เปิดรายงาน](end-user-report-open.md)แล้วเลือกการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="8efa5-109">In the Power BI service, [open a report](end-user-report-open.md) and select a visual.</span></span>  
2. <span data-ttu-id="8efa5-110">เมื่อต้องการแสดงข้อมูลเบื้องหลังวิชวล เลือก **ตัวเลือกเพิ่มเติม** (...) และเลือก **แสดงเป็นวิชวล**</span><span class="sxs-lookup"><span data-stu-id="8efa5-110">To display the data behind the visual, select **More options** (...) and choose **Show as a table**.</span></span>
   
   ![เลือกแสดงเป็นตารางจากรายการแบบหล่นลง](./media/end-user-show-data/power-bi-show-data-vertical.png)
3. <span data-ttu-id="8efa5-112">ตามค่าเริ่มต้น ข้อมูลจะแสดงที่ด้านล่างภาพ</span><span class="sxs-lookup"><span data-stu-id="8efa5-112">By default, the data displays below the visual.</span></span>
   
   ![ข้อมูลและภาพแสดงในแนวตั้ง](./media/end-user-show-data/power-bi-show-data-table.png)

4. <span data-ttu-id="8efa5-114">หากต้องการเปลี่ยนการวางแนว โปรดเลือกเค้าโครงแนวตั้ง</span><span class="sxs-lookup"><span data-stu-id="8efa5-114">To change the orientation, select vertical layout</span></span> ![ไอคอนเค้าโครง](media/end-user-show-data/power-bi-vertical-icon-new.png) <span data-ttu-id="8efa5-116">บริเวณมุมบนขวาของการแสดงผลภาพ</span><span class="sxs-lookup"><span data-stu-id="8efa5-116">from the top-right corner of the visualization.</span></span>
   
   ![ภาพและข้อมูลแสดงในแนวนอน](./media/end-user-show-data/power-bi-show-horizontal.png)

<span data-ttu-id="8efa5-118">หากต้องการกลับไปที่รายงาน ให้เลือก **กลับไปที่รายงาน** จากมุมบนซ้าย</span><span class="sxs-lookup"><span data-stu-id="8efa5-118">To return to the report, select **Back to report** from the upper left corner.</span></span> 

   ![สกรีนช็อตที่แสดงลิงก์สำหรับกลับไปยังรายงาน](./media/end-user-show-data/power-bi-back.png)

## <a name="next-steps"></a><span data-ttu-id="8efa5-120">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="8efa5-120">Next steps</span></span>
<span data-ttu-id="8efa5-121">[การแสดงผลด้วยภาพในรายงาน Power BI](../visuals/power-bi-report-visualizations.md)  </span><span class="sxs-lookup"><span data-stu-id="8efa5-121">[Visuals in Power BI reports](../visuals/power-bi-report-visualizations.md)  </span></span>  
[<span data-ttu-id="8efa5-122">รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="8efa5-122">Power BI reports</span></span>](end-user-reports.md)    
