---
title: เพิ่มการเชื่อมโยงหลายมิติไปยังกล่องข้อความในรายงาน
description: เพิ่มการเชื่อมโยงหลายมิติไปยังกล่องข้อความใน Power BI Desktop และบริการของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 07/25/2019
LocalizationGroup: Visualizations
ms.openlocfilehash: 235a1c0523eff09b0d43be3220b0165eba4dbed6
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96417508"
---
# <a name="add-a-hyperlink-to-a-text-box-in-a-report"></a><span data-ttu-id="bd608-103">เพิ่มการเชื่อมโยงหลายมิติไปยังกล่องข้อความในรายงาน</span><span class="sxs-lookup"><span data-stu-id="bd608-103">Add a hyperlink to a text box in a report</span></span>
<span data-ttu-id="bd608-104">คุณสามารถเพิ่มกล่องข้อความไปยังรายงานใน Power BI Desktop หรือบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="bd608-104">You can add a text box to a report in Power BI Desktop or the Power BI service.</span></span> <span data-ttu-id="bd608-105">คุณสามารถปักหมุดกล่องข้อความจากรายงานไปยังแดชบอร์ด หรือเพิ่มลงในแดชบอร์ดได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="bd608-105">You can pin a text box from a report to a dashboard, or add one directly to a dashboard.</span></span> <span data-ttu-id="bd608-106">ไม่ว่ากล่องข้อความจะอยู่ที่ไหนคุณสามารถเพิ่มการเชื่อมโยงหลายมิติไปยังกล่องข้อความได้เสมอ</span><span class="sxs-lookup"><span data-stu-id="bd608-106">Wherever the text box is, you can always add a hyperlink to it.</span></span> <span data-ttu-id="bd608-107">บทความนี้แสดงวิธีการเพิ่มการเชื่อมโยงหลายมิติไปยังกล่องข้อความในรายงาน</span><span class="sxs-lookup"><span data-stu-id="bd608-107">This article shows how to add a hyperlink to a text box in a report.</span></span> 


<span data-ttu-id="bd608-108">ดู วิล ทอมป์สัน สร้างกล่องข้อความและเพิ่มการเชื่อมโยงหลายมิติไปยังกล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="bd608-108">Watch Will Thompson create a text box and add a hyperlink to it.</span></span> 

<iframe width="560" height="315" src="https://www.youtube.com/embed/_3q6VEBhGew#t=0m55s" frameborder="0" allowfullscreen></iframe>

<span data-ttu-id="bd608-109">สำหรับข้อมูลเกี่ยวกับการเชื่อมโยงหลายมิติในตารางและเมทริกซ์ของ Power BI โปรดดู [เพิ่มการเชื่อมโยงหลายมิติไปยังตาราง](power-bi-hyperlinks-in-tables.md)</span><span class="sxs-lookup"><span data-stu-id="bd608-109">For information on hyperlinks in Power BI tables and matrixes, see [Add hyperlinks to a table](power-bi-hyperlinks-in-tables.md).</span></span> <span data-ttu-id="bd608-110">สำหรับข้อมูลเกี่ยวกับการเพิ่มกล่องข้อความลงในแดชบอร์ดของคุณ โปรดดู [เพิ่มรูปภาพ วิดีโอ และอื่นๆ ไปยังแดชบอร์ดของคุณ](service-dashboard-add-widget.md)</span><span class="sxs-lookup"><span data-stu-id="bd608-110">For information on adding text boxes to your dashboard, see [Add images, videos, and more to your dashboard](service-dashboard-add-widget.md).</span></span> 

## <a name="to-add-a-hyperlink-to-a-text-box"></a><span data-ttu-id="bd608-111">เมื่อต้องเพิ่มการเชื่อมโยงหลายมิติไปยังกล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="bd608-111">To add a hyperlink to a text box</span></span>
1. <span data-ttu-id="bd608-112">เปิดรายงาน [สร้างกล่องข้อความ](power-bi-reports-add-text-and-shapes.md) แล้วเพิ่มข้อความบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="bd608-112">Open a report, [create a text box](power-bi-reports-add-text-and-shapes.md), and add some text.</span></span> 
2. <span data-ttu-id="bd608-113">เลือกข้อความที่มีอยู่ หรือเพิ่มข้อความใหม่ เพื่อใช้เป็นการเชื่อมโยงหลายมิติ</span><span class="sxs-lookup"><span data-stu-id="bd608-113">Select existing text, or add new text to use as a hyperlink.</span></span> 

   <span data-ttu-id="bd608-114">เมนูกล่องข้อความจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="bd608-114">The text box menu appears.</span></span>
   
   ![เลือกข้อความในกล่องข้อความ](media/service-add-hyperlink-to-text-box/power-bi-hyperlink-new.png)
3. <span data-ttu-id="bd608-116">เลือกไอคอนการเชื่อมโยงหลายมิติ</span><span class="sxs-lookup"><span data-stu-id="bd608-116">Select the hyperlink icon</span></span> ![ไฮเปอร์ลิงก์ไอคอน](media/service-add-hyperlink-to-text-box/power-bi-hyperlink-icon.png) <span data-ttu-id="bd608-118">บนเมนูกล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="bd608-118">on the text box menu.</span></span>

   <span data-ttu-id="bd608-119">เขตข้อมูลการเชื่อมโยงหลายมิติจะปรากฏบนเมนูกล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="bd608-119">The hyperlink field appears on the text box menu.</span></span>

4. <span data-ttu-id="bd608-120">พิมพ์หรือวาง URL ลงในเขตข้อมูลการเชื่อมโยงหลายมิติ แล้วเลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="bd608-120">Type or paste the URL in the hyperlink field, and then select **Done**.</span></span>
   
   ![พิมพ์ หรือวาง URL ลงในเขตข้อมูลการเชื่อมโยงหลายมิติ](media/service-add-hyperlink-to-text-box/power-bi-add-link.png)
5. <span data-ttu-id="bd608-122">ทดสอบลิงก์:</span><span class="sxs-lookup"><span data-stu-id="bd608-122">Test the link:</span></span>  

   <span data-ttu-id="bd608-123">ก.</span><span class="sxs-lookup"><span data-stu-id="bd608-123">a.</span></span> <span data-ttu-id="bd608-124">วางเคอร์เซอร์ของคุณที่ใดก็ได้ในการเชื่อมโยงหลายมิติอันใหม่ในกล่องข้อความเพื่อแสดง URL ในเขตข้อมูลการเชื่อมโยงหลายมิติ</span><span class="sxs-lookup"><span data-stu-id="bd608-124">Place your cursor anywhere in the new hyperlink in the text box to display the URL in the hyperlink field.</span></span>  
     
      ![การเชื่อมโยงหลายมิติในกล่องข้อความ](media/service-add-hyperlink-to-text-box/power-bi-test-link.png)
   
      ![URL ในเขตข้อมูลการเชื่อมโยงหลายมิติ](media/service-add-hyperlink-to-text-box/power-bi-hyperlink-edit.png)

   <span data-ttu-id="bd608-127">b.</span><span class="sxs-lookup"><span data-stu-id="bd608-127">b.</span></span> <span data-ttu-id="bd608-128">เลือก URL ในเขตข้อมูลการเชื่อมโยงหลายมิติที่จะเปิดหน้าเพจในหน้าต่างเบราว์เซอร์ใหม่</span><span class="sxs-lookup"><span data-stu-id="bd608-128">Select the URL in the hyperlink field to open the page in a new browser window.</span></span>

## <a name="to-remove-the-hyperlink"></a><span data-ttu-id="bd608-129">หากต้องการนำการเชื่อมโยงหลายมิติออก</span><span class="sxs-lookup"><span data-stu-id="bd608-129">To remove the hyperlink</span></span>
1. <span data-ttu-id="bd608-130">ในกล่องข้อความ ให้เลือกการเชื่อมโยงหลายมิติเพื่อไฮไลต์การเชื่อมโยงดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="bd608-130">In the text box, select the hyperlink to highlight it.</span></span>
   
     ![นำการเชื่อมโยงหลายมิติออก](media/service-add-hyperlink-to-text-box/power-bi-hyperlink-remove.png)
2. <span data-ttu-id="bd608-132">เลือก **นำออก** จากเมนูกล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="bd608-132">Select **Remove** from the text box menu.</span></span> 

   <span data-ttu-id="bd608-133">Power BI Desktop จะนำการเชื่อมโยงหลายมิติออก แต่ปล่อยข้อความทิ้งไว้</span><span class="sxs-lookup"><span data-stu-id="bd608-133">Power BI Desktop removes the hyperlink, but leaves the text.</span></span>

## <a name="next-steps"></a><span data-ttu-id="bd608-134">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="bd608-134">Next steps</span></span>
[<span data-ttu-id="bd608-135">กล่องข้อความและรูปร่างในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="bd608-135">Text boxes and shapes in Power BI reports</span></span>](power-bi-reports-add-text-and-shapes.md)

<span data-ttu-id="bd608-136">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="bd608-136">More questions?</span></span> <span data-ttu-id="bd608-137">[ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="bd608-137">[Try the Power BI Community](https://community.powerbi.com/).</span></span>

