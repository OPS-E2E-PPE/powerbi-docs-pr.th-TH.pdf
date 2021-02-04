---
title: ปักหมุดไทล์ที่แดชบอร์ดจาก Q&A
description: เอกสารวิธีการปักหมุดไทล์ตรงแดชบอร์ด Power BI จากกล่องคำถาม Q&A
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 01/05/2021
LocalizationGroup: Dashboards
ms.openlocfilehash: 5ae148feaa294c8779a7140ef450c832bd3376d8
ms.sourcegitcommit: 932f6856849c39e34229dc9a49fb9379c56a888a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/06/2021
ms.locfileid: "97927175"
---
# <a name="pin-a-tile-to-a-dashboard-from-qa"></a><span data-ttu-id="d9fcd-103">ปักหมุดไทล์ที่แดชบอร์ดจาก Q&A</span><span class="sxs-lookup"><span data-stu-id="d9fcd-103">Pin a tile to a dashboard from Q&A</span></span>

<span data-ttu-id="d9fcd-104">Q&A เป็นเครื่องมือของ Power BI สำหรับการสำรวจข้อมูลของคุณโดยใช้ภาษาธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="d9fcd-104">Q&A is a Power BI tool for exploring your data using natural language.</span></span> <span data-ttu-id="d9fcd-105">จำเป็นต้องค้นหาข้อมูลเชิงลึกที่เฉพาะเจาะจงหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d9fcd-105">Need to find a particular insight?</span></span> <span data-ttu-id="d9fcd-106">ถามคำถามเกี่ยวกับข้อมูลของคุณ และรับคำตอบในรูปแบบการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="d9fcd-106">Ask a question about your data, and receive an answer in the form of a visualization.</span></span>

<span data-ttu-id="d9fcd-107">ในบทความวิธีการใช้งานนี้ เราเปิด[แดชบอร์ด](../consumer/end-user-dashboards.md)ในบริการ Power BI (app.powerbi.com) ถามคำถามโดยใช้ภาษาธรรมชาติเพื่อสร้างภาพ และปักหมุดการแสดงภาพนั้นที่แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="d9fcd-107">In this how-to article, we open a [dashboard](../consumer/end-user-dashboards.md) in the Power BI service (app.powerbi.com), ask a question using natural language to create a visualization, and pin that visualization to the dashboard.</span></span> <span data-ttu-id="d9fcd-108">แดชบอร์ดไม่พร้อมใช้งานใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d9fcd-108">Dashboards aren't available in Power BI Desktop.</span></span> <span data-ttu-id="d9fcd-109">สำหรับข้อมูลใน Q&A กับเครื่องมือและเนื้อหา Power BI อื่น ๆ ให้ดู[Q&A ของ Power BI โดยภาพรวม](../consumer/end-user-q-and-a.md)</span><span class="sxs-lookup"><span data-stu-id="d9fcd-109">For information on using Q&A with other Power BI tools and content, see the [Power BI Q&A overview](../consumer/end-user-q-and-a.md).</span></span> 

<span data-ttu-id="d9fcd-110">เพื่อการทำตาม ให้เปิด[แดชบอร์ดตัวอย่างวิเคราะห์ร้านค้าปลีก](sample-retail-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="d9fcd-110">To follow along, open the [Retail Analysis sample dashboard](sample-retail-analysis.md).</span></span>

## <a name="how-to-pin-a-tile-from-qa"></a><span data-ttu-id="d9fcd-111">วิธีการปักหมุดไทล์จาก Q&A</span><span class="sxs-lookup"><span data-stu-id="d9fcd-111">How to pin a tile from Q&A</span></span>

1. <span data-ttu-id="d9fcd-112">เปิดแดชบอร์ดที่มีอย่างน้อยหนึ่งไทล์ที่ปักหมุดจากรายงาน</span><span class="sxs-lookup"><span data-stu-id="d9fcd-112">Open a dashboard that has at least one tile pinned from a report.</span></span> <span data-ttu-id="d9fcd-113">เมื่อคุณถามคำถาม Power BI จะค้นหาคำตอบในชุดข้อมูลใดๆ ที่มีไทล์ถูกปักในแดชบอร์ดนั้น</span><span class="sxs-lookup"><span data-stu-id="d9fcd-113">When you ask a question, Power BI looks for the answer in any dataset that has a tile pinned to that dashboard.</span></span>
2. <span data-ttu-id="d9fcd-114">ที่กล่องคำถามด้านบนในแดชบอร์ดของคุณ ให้เริ่มพิมพ์สิ่งที่คุณต้องการทราบเกี่ยวกับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="d9fcd-114">In the question box at the top of your dashboard, start typing what you want to know about your data.</span></span>  
   ![กล่องคำถาม Q&A](media/service-dashboard-pin-tile-from-q-and-a/power-bi-question-box.png)
3. <span data-ttu-id="d9fcd-116">ตัวอย่างเช่น พิมพ์ “ยอดขายของปีที่แล้วตามเดือนและพื้นที่”</span><span class="sxs-lookup"><span data-stu-id="d9fcd-116">For example, as you type "last year sales by month and territory"...</span></span>  
   ![พิมพ์คำถาม](media/service-dashboard-pin-tile-from-q-and-a/power-bi-type-q-and-a.png)

   <span data-ttu-id="d9fcd-118">กล่องคำถามให้คำแนะนำคุณ</span><span class="sxs-lookup"><span data-stu-id="d9fcd-118">the question box gives you suggestions.</span></span>
4. <span data-ttu-id="d9fcd-119">หากต้องการเพิ่มแผนภูมิไปยังแดชบอร์ดในรูปแบบไทล์ ให้เลือกปักหมุด</span><span class="sxs-lookup"><span data-stu-id="d9fcd-119">To add the chart to your dashboard as a tile, select the pin</span></span> ![ปักหมุดไอคอน](media/service-dashboard-pin-tile-from-q-and-a/pbi_pintile.png) <span data-ttu-id="d9fcd-121">ที่ด้านขวาบนของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="d9fcd-121">on the top-right side of the canvas.</span></span> <span data-ttu-id="d9fcd-122">ถ้ามีการแชร์แดชบอร์ดกับคุณ คุณจะไม่สามารถปักหมุดการสร้างการแสดงภาพใดได้</span><span class="sxs-lookup"><span data-stu-id="d9fcd-122">If the dashboard has been shared with you, you won't be able to pin any visualizations.</span></span>

5. <span data-ttu-id="d9fcd-123">ปักหมุดไทล์ลงในแดชบอร์ดที่มีอยู่ หรือแดชบอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="d9fcd-123">Pin the tile to an existing dashboard or to a new dashboard.</span></span>

   ![ปักหมุดกล่องข้อความแดชบอร์ด](media/service-dashboard-pin-tile-from-q-and-a/power-bi-pin-to-dashboard.png)

   * <span data-ttu-id="d9fcd-125">แดชบอร์ดที่มีอยู่ ให้เลือกชื่อของแดชบอร์ดจากรายการแบบดร๊อปดาวน์</span><span class="sxs-lookup"><span data-stu-id="d9fcd-125">Existing dashboard: select the name of the dashboard from the dropdown.</span></span> <span data-ttu-id="d9fcd-126">ตัวเลือกของคุณจะถูกจำกัดให้ใช้งานเฉพาะกับแดชบอร์ดดังกล่าวภายในพื้นที่ทำงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="d9fcd-126">Your choices will be limited to only those dashboards within the current workspace.</span></span>
   * <span data-ttu-id="d9fcd-127">แดชบอร์ดใหม่ พิมพ์ชื่อของแดชบอร์ดใหม่ แล้วจะได้รับการเพิ่มไปยังพื้นที่ทำงานปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="d9fcd-127">New dashboard: type the name of the new dashboard and it will be added to your current workspace.</span></span>

6. <span data-ttu-id="d9fcd-128">เลือก **หมุด**</span><span class="sxs-lookup"><span data-stu-id="d9fcd-128">Select **Pin**.</span></span>

   <span data-ttu-id="d9fcd-129">ข้อความการดำเนินการสำเร็จ (ใกล้กับมุมบนขวา) ช่วยให้คุณทราบว่าได้เพิ่มการแสดงภาพเป็นไทล์ ลงในแดชบอร์ดของคุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="d9fcd-129">A success message (near the top-right corner) lets you know the visualization was added, as a tile, to your dashboard.</span></span>  

   ![ปักหมุดลงในแดชบอร์ดแล้ว](media/service-dashboard-pin-tile-from-q-and-a/power-bi-pin.png)
7. <span data-ttu-id="d9fcd-131">เลือก **ไปยังแดชบอร์ด** เมื่อต้องการดูไทล์ใหม่</span><span class="sxs-lookup"><span data-stu-id="d9fcd-131">Select **Go to dashboard** to see the new tile.</span></span> <span data-ttu-id="d9fcd-132">ที่นั่น คุณสามารถ[เปลี่ยนชื่อ ปรับขนาด เพิ่มลิงค์ และจัดตำแหน่งไทล์ใหม่ และอื่นๆ](service-dashboard-edit-tile.md) ในแดชบอร์ดของคุณได้</span><span class="sxs-lookup"><span data-stu-id="d9fcd-132">There, you can [rename, resize, add a hyperlink, reposition the tile, and more](service-dashboard-edit-tile.md) on your dashboard.</span></span>

   ![แดชบอร์ดพร้อมไทล์](media/service-dashboard-pin-tile-from-q-and-a/power-bi-pinned.png)

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="d9fcd-134">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="d9fcd-134">Considerations and troubleshooting</span></span>
* <span data-ttu-id="d9fcd-135">เมื่อคุณเริ่มพิมพ์คำถาม Q&Aจะเริ่มค้นหาคำตอบที่ดีที่สุดจากชุดข้อมูลทั้งหมดที่เชื่อมโยงกับแดชบอร์ดปัจจุบันทันที</span><span class="sxs-lookup"><span data-stu-id="d9fcd-135">When you start typing a question, Q&A immediately begins searching for the best answer from all datasets associated with the current dashboard.</span></span>  <span data-ttu-id="d9fcd-136">"แดชบอร์ดปัจจุบัน" เป็นแดชบอร์ดที่แสดงอยู่ในหน้าต่างนำทางด้านบน</span><span class="sxs-lookup"><span data-stu-id="d9fcd-136">The "current dashboard" is the dashboard listed in the top nav pane.</span></span> <span data-ttu-id="d9fcd-137">ตัวอย่างเช่น คำถามนี้จะถูกถามในแดชบอร์ด **ตัวอย่างการวิเคราะห์ร้านค้าปลีก** ที่เป็นส่วนหนึ่งของพื้นที่ทำงาน **mihart**</span><span class="sxs-lookup"><span data-stu-id="d9fcd-137">For example, this question is being asked in the **Retail Analysis Sample** dashboard that is part of the **mihart** workspace.</span></span>

  ![การนำทางแบบแสดงเส้นนำทาง](media/service-dashboard-pin-tile-from-q-and-a/power-bi-navbar.png)
* <span data-ttu-id="d9fcd-139">**Q&A รู้ว่าจะใช้ข้อมูลชุดไหนได้อย่างไร**</span><span class="sxs-lookup"><span data-stu-id="d9fcd-139">**How does Q&A know which datasets to use**?</span></span>  <span data-ttu-id="d9fcd-140">Q&A มีสิทธิ์เข้าถึงชุดข้อมูลทั้งหมดที่มีการแสดงภาพอย่างน้อยหนึ่งที่ ที่ปักหมุดที่แดชบอร์ดนั้น</span><span class="sxs-lookup"><span data-stu-id="d9fcd-140">Q&A has access to all datasets that have at least one visualization pinned to that dashboard.</span></span>

* <span data-ttu-id="d9fcd-141">**ไม่เห็นกล่องคำถาม หรือไม่** ่</span><span class="sxs-lookup"><span data-stu-id="d9fcd-141">**Don't see the question box**?</span></span> <span data-ttu-id="d9fcd-142">ตรวจสอบกับผู้ดูแลระบบ Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d9fcd-142">Check with your Power BI administrator.</span></span> <span data-ttu-id="d9fcd-143">ผู้ดูแลระบบมีความสามารถในการปิดใช้งาน Q&A</span><span class="sxs-lookup"><span data-stu-id="d9fcd-143">The administrator has the ability to disable Q&A.</span></span>


## <a name="next-steps"></a><span data-ttu-id="d9fcd-144">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d9fcd-144">Next steps</span></span>
<span data-ttu-id="d9fcd-145">[เปลี่ยนชื่อ ปรับขนาด เพิ่มไฮเปอร์ลิงก์ เปลี่ยนตำแหน่งไทล์ และอื่น ๆ ](service-dashboard-edit-tile.md)  </span><span class="sxs-lookup"><span data-stu-id="d9fcd-145">[Rename, resize, add a hyperlink, reposition the tile, and more](service-dashboard-edit-tile.md)  </span></span>  
<span data-ttu-id="d9fcd-146">[แสดงแดชบอร์ดไทล์ของคุณในโหมดโฟกัส](../consumer/end-user-focus.md)   </span><span class="sxs-lookup"><span data-stu-id="d9fcd-146">[Display your dashboard tile in Focus mode](../consumer/end-user-focus.md)   </span></span>  
[<span data-ttu-id="d9fcd-147">ภาพรวมของ Q&A ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="d9fcd-147">Overview of Q&A in Power BI</span></span>](../consumer/end-user-q-and-a.md)  
<span data-ttu-id="d9fcd-148">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d9fcd-148">More questions?</span></span> [<span data-ttu-id="d9fcd-149">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="d9fcd-149">Try the Power BI Community</span></span>](https://community.powerbi.com/)
