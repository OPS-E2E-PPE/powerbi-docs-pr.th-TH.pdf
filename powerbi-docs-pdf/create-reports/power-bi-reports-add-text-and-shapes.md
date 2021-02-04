---
title: กล่องข้อความและรูปร่างในรายงาน Power BI
description: เพิ่มและสร้างกล่องข้อความและรูปร่างในรายงานโดยใช้บริการของ Microsoft Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: _3q6VEBhGew
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 05/29/2019
LocalizationGroup: Visualizations
ms.openlocfilehash: 90c7489ad047be47a2a1f9ac9e814a9da5724f32
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96393565"
---
# <a name="add-text-boxes-and-shapes-to-power-bi-reports"></a><span data-ttu-id="113e8-103">เพิ่มกล่องข้อความและรูปร่างในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="113e8-103">Add text boxes and shapes to Power BI reports</span></span>
<span data-ttu-id="113e8-104">คุณสามารถเพิ่มกล่องข้อความและรูปร่างในรายงานโดยใช้บริการของ Power BI service และ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="113e8-104">You can add text boxes and shapes to reports by using the Power BI service and Power BI Desktop.</span></span> <span data-ttu-id="113e8-105">ในทั้งสองกรณี คุณต้องแก้ไขสิทธิ์สำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="113e8-105">In both cases, you must have editing permissions for the report.</span></span> <span data-ttu-id="113e8-106">ถ้ารายงานมีการแชร์ให้กับคุณในบริการของ Power BI คุณจะไม่ได้สิทธิการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="113e8-106">If a report has been shared with you in the Power BI service, you won't have editing permissions.</span></span> 

<span data-ttu-id="113e8-107">Watch Will ใช้ Power BI Desktop เพื่อ[เพิ่มรูปภาพแบบคงที่ไปยังรายงาน](/learn/modules/visuals-in-power-bi/12-formatting)แล้ว ทำตามขั้นตอนด้านล่างเพื่อลองใช้ Power BI service แทน</span><span class="sxs-lookup"><span data-stu-id="113e8-107">Watch Will use Power BI Desktop to [add static images to a report](/learn/modules/visuals-in-power-bi/12-formatting), and then follow the steps below to try it out yourself by using the Power BI service instead.</span></span>
> 
> <iframe width="560" height="315" src="https://www.youtube.com/embed/_3q6VEBhGew" frameborder="0" allowfullscreen></iframe>
> 

## <a name="add-a-text-box-to-a-report"></a><span data-ttu-id="113e8-108">เพิ่มกล่องข้อความไปยังรายงาน</span><span class="sxs-lookup"><span data-stu-id="113e8-108">Add a text box to a report</span></span>
1. <span data-ttu-id="113e8-109">เปิดรายงานในมุมมองการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="113e8-109">Open a report in Editing view.</span></span>

2. <span data-ttu-id="113e8-110">วางเคอร์เซอร์ของคุณในพื้นที่ว่างบนพื้นที่รายงาน และให้เลือก **กล่องข้อความ** จากเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="113e8-110">Place your cursor in any blank area on the report canvas and select **Text box** from the top menu.</span></span>
   
   ![เลือกกล่องข้อความ](media/power-bi-reports-add-text-and-shapes/pbi_textbox.png)
3. <span data-ttu-id="113e8-112">พิมพ์ข้อความของคุณลงในกล่องข้อความ รวมทั้งตั้งค่ารูปแบบฟอนต์ สี และการจัดแนวข้อความ</span><span class="sxs-lookup"><span data-stu-id="113e8-112">Type your text into the text box and, optionally, set the format font, color, and text alignment.</span></span> 
   
   ![กรอกข้อความ](media/power-bi-reports-add-text-and-shapes/pbi_textbox2new.png)
4. <span data-ttu-id="113e8-114">การจัดตำแหน่งกล่องข้อความ ให้เลือกพื้นที่สีเทาที่ด้านบนแล้วลาก</span><span class="sxs-lookup"><span data-stu-id="113e8-114">To position the text box, select the grey area at the top and drag.</span></span> <span data-ttu-id="113e8-115">เมื่อต้องการปรับขนาดกล่องข้อความ เลือกแล้วลากจุดเค้าร่าง</span><span class="sxs-lookup"><span data-stu-id="113e8-115">To resize the text box, select and drag any of the outline handles.</span></span> 
   
   ![จัดตำแหน่งกล่องข้อความ](media/power-bi-reports-add-text-and-shapes/textboxsmaller.gif)

5. <span data-ttu-id="113e8-117">ด้วยกล่องข้อความที่เลือก เพิ่มการจัดรูปแบบเพิ่มเติมในบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="113e8-117">With the text box still selected, add additional formatting in the **Visualizations** pane.</span></span> <span data-ttu-id="113e8-118">ในตัวอย่างนี้ เราได้จัดรูปแบบพื้นหลังและเส้นขอบ</span><span class="sxs-lookup"><span data-stu-id="113e8-118">In this example, we've formatted the background and border.</span></span> <span data-ttu-id="113e8-119">คุณยังสามารถสร้างเป็นขนาดที่แน่นอนและตำแหน่งของกล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="113e8-119">You can also create an exact size and position for a text box.</span></span>  

   ![การจัดรูปแบบกล่องข้อความ](media/power-bi-reports-add-text-and-shapes/power-bi-borders.png)

6. <span data-ttu-id="113e8-121">เพื่อปิดกล่องข้อความ เลือกพื้นที่ว่างบนพื้นที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="113e8-121">To close the text box, select any blank space on the report canvas.</span></span> 

7. <span data-ttu-id="113e8-122">เลือกไอคอนหมุด</span><span class="sxs-lookup"><span data-stu-id="113e8-122">Select the pin icon</span></span>  ![ไอคอนรูปเข็มหมุด](media/power-bi-reports-add-text-and-shapes/pbi_pintile.png) <span data-ttu-id="113e8-124">เพื่อปักหมุดกล่องข้อความไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="113e8-124">to pin the text box to a dashboard.</span></span> 

## <a name="add-a-shape-to-a-report"></a><span data-ttu-id="113e8-125">เพิ่มรูปร่างไปยังรายงาน</span><span class="sxs-lookup"><span data-stu-id="113e8-125">Add a shape to a report</span></span>
1. <span data-ttu-id="113e8-126">วางเคอร์เซอร์ของคุณที่ใดก็ได้บนพื้นที่รายงาน แล้วเลือก **รูปร่าง**</span><span class="sxs-lookup"><span data-stu-id="113e8-126">Place your cursor anywhere on the report canvas and select **Shapes**.</span></span>
   
   ![เลือกรูปร่าง](media/power-bi-reports-add-text-and-shapes/power-bi-shapes.png)
2. <span data-ttu-id="113e8-128">จากดร๊อปดาวน์ เลือกรูปร่างเพื่อเพิ่มในพื้นที่รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="113e8-128">From the dropdown, select a shape to add it to your report canvas.</span></span> <span data-ttu-id="113e8-129">สำหรับตัวอย่างนี้ ลองเพิ่มลูกศรเพื่อดึงดูดความสนใจไปที่แผนภูมิฟองที่มีความแปรปรวนของยอดขายสูงสุด</span><span class="sxs-lookup"><span data-stu-id="113e8-129">For this example, add an arrow to direct attention to the bubble with the highest total sales variance.</span></span> 
   
   <span data-ttu-id="113e8-130">ในบานหน้าต่าง **จัดรูปแบบรูปร่าง** ให้ปรับแต่งรูปร่างของคุณ</span><span class="sxs-lookup"><span data-stu-id="113e8-130">In the **Format shape** pane, customize your shape.</span></span> <span data-ttu-id="113e8-131">ในตัวอย่างนี้ เราได้สร้างเป็นลูกศรสีแดงมีขอบสีแดงเข้ม ถูกหมุน 90 องศา</span><span class="sxs-lookup"><span data-stu-id="113e8-131">In this example we've created a red arrow with a dark red border, rotated 90 degrees.</span></span>
   
   ![กำหนดมุมมองเอง](media/power-bi-reports-add-text-and-shapes/power-bi-arrrow.png)
3. <span data-ttu-id="113e8-133">เพื่อจัดตำแหน่งรูปร่าง ให้เลือกพื้นที่สีเทาที่ด้านบนและลาก</span><span class="sxs-lookup"><span data-stu-id="113e8-133">To position the shape, select the grey area at the top and drag.</span></span> <span data-ttu-id="113e8-134">เมื่อต้องการปรับขนาด เลือกและลากจุดเค้าร่างใด ๆ ก็ได้</span><span class="sxs-lookup"><span data-stu-id="113e8-134">To resize the shape, select and drag any of the outline handles.</span></span> <span data-ttu-id="113e8-135">เหมือนในหนังสือ คุณยังสามารถสร้างเป็นขนาดที่แน่นอนและตำแหน่งของกล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="113e8-135">As with the text box, you can also create an exact size and position for a shape.</span></span>

   > [!NOTE]
   > <span data-ttu-id="113e8-136">รูปร่างที่ไม่สามารถปักหมุดที่ยังแดชบอร์ดได้ ยกเว้นเป็นหนึ่งภาพเมื่อคุณ[ปักหมุดหน้าสด](service-dashboard-pin-live-tile-from-report.md)</span><span class="sxs-lookup"><span data-stu-id="113e8-136">Shapes cannot be pinned to a dashboard, except as one of the visuals when you [pin a live page](service-dashboard-pin-live-tile-from-report.md).</span></span> 
   > 
   > 

## <a name="next-steps"></a><span data-ttu-id="113e8-137">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="113e8-137">Next steps</span></span>

<span data-ttu-id="113e8-138">คุณอาจมีความสนใจบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="113e8-138">You might also be interested in the following articles:</span></span>

* [<span data-ttu-id="113e8-139">เพิ่มไฮเปอร์ลิงก์ให้กล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="113e8-139">Add a hyperlink to a text box</span></span>](service-add-hyperlink-to-text-box.md)
* [<span data-ttu-id="113e8-140">แนวคิดพื้นฐานสำหรับนักออกแบบในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="113e8-140">Basic concepts for designers in the Power BI service</span></span>](../fundamentals/service-basic-concepts.md)
* [<span data-ttu-id="113e8-141">เคล็ดลับในการปรับปรุงการวิเคราะห์ด้วยรูปร่าง รูปภาพ และไอคอนในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="113e8-141">Tips to improve analysis with shapes, images, and icons in Power BI reports</span></span>](../guidance/report-tips-shapes-images-icons.md)
* <span data-ttu-id="113e8-142">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="113e8-142">More questions?</span></span> [<span data-ttu-id="113e8-143">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="113e8-143">Try the Power BI Community</span></span>](https://community.powerbi.com/)
