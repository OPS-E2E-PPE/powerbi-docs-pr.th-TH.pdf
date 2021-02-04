---
title: สร้างวิชวลด้วย Power BI Q&A
description: เรียนรู้การสร้างวิชวลด้วยถามตอบ (Q&A) ในบริการ Power BI โดยใช้การวิเคราะห์ด้านการขายปลีกเป็นตัวอย่าง
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 05/13/2019
LocalizationGroup: Ask questions of your data
ms.openlocfilehash: 7eae93eb2b4594a180836f43a758c6bef7b3e90e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415047"
---
# <a name="create-a-visual-with-power-bi-qa"></a><span data-ttu-id="91b75-103">สร้างวิชวลด้วย Power BI Q&A</span><span class="sxs-lookup"><span data-stu-id="91b75-103">Create a visual with Power BI Q&A</span></span>

<span data-ttu-id="91b75-104">ในบางครั้ง วิธีที่เร็วที่สุดในการให้ได้คำตอบจากข้อมูลของคุณคือ การถามคำถามโดยใช้ภาษาธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="91b75-104">Sometimes the fastest way to get an answer from your data is to ask a question using natural language.</span></span>  <span data-ttu-id="91b75-105">ในบทความนี้ เราจะมาดูวิธีการที่แตกต่างกันสองวิธีในการสร้างการแสดงผลข้อมูลด้วยภาพชนิดเดียวกัน: วิธีแรก ถามคำถามกับถามตอบ (Q&A) และวิธีที่สอง สร้างในรายงาน</span><span class="sxs-lookup"><span data-stu-id="91b75-105">In this article, we look at two different ways of creating the same visualization: first, asking a question with Q&A, and second, building it in a report.</span></span> <span data-ttu-id="91b75-106">เราใช้บริการ Power BI เพื่อสร้างวิชวลในรายงาน แต่กระบวนการเกือบจะเหมือนกันทั้งหมดกับการใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="91b75-106">We use the Power BI service to build the visual in the report, but the process is almost identical using Power BI Desktop.</span></span>

![แผนภูมิแบบเติมของ Power BI](media/power-bi-visualization-introduction-to-q-and-a/power-bi-qna-create-visual.png)

<span data-ttu-id="91b75-108">ในการทำตาม คุณต้องใช้รายงานที่คุณสามารถแก้ไขได้ ดังนั้นเราจะใช้หนึ่งในตัวอย่างที่พร้อมใช้งานกับ Power BI</span><span class="sxs-lookup"><span data-stu-id="91b75-108">To follow along, you must use a report that you can edit, so we'll use one of the samples available with Power BI.</span></span>

## <a name="create-a-visual-with-qa"></a><span data-ttu-id="91b75-109">สร้างการแสดงผลด้วยภาพด้วยการถามตอบ</span><span class="sxs-lookup"><span data-stu-id="91b75-109">Create a visual with Q&A</span></span>

<span data-ttu-id="91b75-110">เราจะทำอย่างไรในการสร้างแผนภูมิเส้นนี้โดยใช้ถามตอบ (Q&A)?</span><span class="sxs-lookup"><span data-stu-id="91b75-110">How would we go about creating this line chart using Q&A?</span></span>

1. <span data-ttu-id="91b75-111">จากพื้นที่ทำงานของ Power BI เลือก **รับข้อมูล** \> **ตัวอย่าง** \> **ตัวอย่างการวิเคราะห์ร้านค้าปลีก**  >  **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="91b75-111">From your Power BI workspace, select **Get Data** \> **Samples** \> **Retail Analysis Sample** > **Connect**.</span></span>

1. <span data-ttu-id="91b75-112">เปิดแดชบอร์ดตัวอย่างการวิเคราะห์ร้านค้าปลีก และวางเคอร์เซอร์ของคุณในกล่องถามตอบ (Q&A) **ถามคำถามเกี่ยวกับข้อมูลของคุณ**</span><span class="sxs-lookup"><span data-stu-id="91b75-112">Open the Retail Analysis Sample dashboard and place your cursor in the Q&A box, **Ask a question about your data**.</span></span>

    ![วางเคอร์เซอร์ของคุณในกล่องถามตอบ (Q&A)](media/power-bi-visualization-introduction-to-q-and-a/power-bi-qna-cursor-in-qna-box.png)

2. <span data-ttu-id="91b75-114">ในกล่องถามตอบ (Q&A) ให้พิมพ์บางสิ่งบางอย่างเช่นคำถามนี้:</span><span class="sxs-lookup"><span data-stu-id="91b75-114">In the Q&A box, type something like this question:</span></span>
   
    <span data-ttu-id="91b75-115">**ยอดขายในปีนี้และยอดขายในปีที่แล้วตามเดือนโดยแสดงเป็นแผนภูมิพื้นที่**</span><span class="sxs-lookup"><span data-stu-id="91b75-115">**this year sales and last year sales by month as area chart**</span></span>
   
    <span data-ttu-id="91b75-116">ขณะที่คุณพิมพ์คำถามของคุณ การถามตอบจะเลือกการแสดงภาพที่ดีที่สุดเพื่อแสดงคำตอบของคุณ และการแสดงภาพจะเปลี่ยนแปลงอย่างต่อเนื่องขณะที่คุณเปลี่ยนคำถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="91b75-116">As you type your question, Q&A picks the best visualization to display your answer; and the visualization changes dynamically as you modify the question.</span></span> <span data-ttu-id="91b75-117">นอกจากนี้ การถามตอบยังช่วยให้คุณสามารถจัดรูปแบบคำถามของคุณตามคำแนะนำ การกรอกข้อมูลอัตโนมัติ และการแก้ไขการสะกด</span><span class="sxs-lookup"><span data-stu-id="91b75-117">Also, Q&A helps you format your question with suggestions, autocomplete, and spelling corrections.</span></span> <span data-ttu-id="91b75-118">ถามตอบ (Q&A) แนะนำให้ใช้การเปลี่ยนแปลงถ้อยคำเล็กน้อย: "ยอดขายในปีนี้และยอดขายในปีที่แล้วตาม *เดือนเวลา* โดยแสดงเป็นแผนภูมิพื้นที่"</span><span class="sxs-lookup"><span data-stu-id="91b75-118">Q&A recommends a small wording change: "this year sales and last year sales by *time month* as area chart".</span></span>  

    ![การใช้ถ้อยคำที่ถูกต้องในถามตอบ (Q&A)](media/power-bi-visualization-introduction-to-q-and-a/power-bi-qna-corrected-create-filled-chart.png)

4. <span data-ttu-id="91b75-120">เลือกประโยคเพื่อยอมรับคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="91b75-120">Select the sentence to accept the suggestion.</span></span> 
   
   <span data-ttu-id="91b75-121">เมื่อคุณพิมพ์คำถามของคุณเสร็จแล้ว ผลลัพธ์จะแสดงเป็นแผนภูมิเดียวกับที่คุณเห็นในแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="91b75-121">When you finish typing your question, the result is the same chart that you see in the dashboard.</span></span>
   
   ![แผนภูมิพื้นที่แบบเติมของถามตอบ (Q&A)](media/power-bi-visualization-introduction-to-q-and-a/power-bi-qna-create-filled-chart.png)

4. <span data-ttu-id="91b75-123">เมื่อต้องการปักหมุดแผนภูมิไปยังแดชบอร์ด เลือกไอคอนปักหมุด</span><span class="sxs-lookup"><span data-stu-id="91b75-123">To pin the chart to your dashboard, select the pin icon</span></span> ![ไอคอนรูปเข็มหมุด](media/power-bi-visualization-introduction-to-q-and-a/pinnooutline.png) <span data-ttu-id="91b75-125">ที่มุมขวาบน</span><span class="sxs-lookup"><span data-stu-id="91b75-125">in the upper-right corner.</span></span>

## <a name="create-a-visual-in-the-report-editor"></a><span data-ttu-id="91b75-126">สร้างวิชวลในตัวแก้ไขรายงาน</span><span class="sxs-lookup"><span data-stu-id="91b75-126">Create a visual in the report editor</span></span>

1. <span data-ttu-id="91b75-127">นำทางกลับไปยังแดชบอร์ดตัวอย่างการวิเคราะห์ร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="91b75-127">Navigate back to the Retail Analysis Sample dashboard.</span></span>
   
2. <span data-ttu-id="91b75-128">แดชบอร์ดประกอบด้วยไทล์แผนภูมิพื้นที่เดียวกันสำหรับ "ยอดขายของปีที่แล้วและยอดขายของปีนี้"</span><span class="sxs-lookup"><span data-stu-id="91b75-128">The dashboard contains the same area chart tile for "Last Year Sales and This Year Sales."</span></span>  <span data-ttu-id="91b75-129">เลือกไทล์นี้</span><span class="sxs-lookup"><span data-stu-id="91b75-129">Select this tile.</span></span> <span data-ttu-id="91b75-130">อย่าเลือกไทล์ที่คุณสร้างขึ้นด้วยถามตอบ (Q&A)</span><span class="sxs-lookup"><span data-stu-id="91b75-130">Don't select the tile you created with Q&A.</span></span> <span data-ttu-id="91b75-131">การเลือกจะเปิดถามตอบ (Q&A)</span><span class="sxs-lookup"><span data-stu-id="91b75-131">Selecting it opens Q&A.</span></span> <span data-ttu-id="91b75-132">ไทล์แผนภูมิพื้นที่ดั้งเดิมถูกสร้างขึ้นในรายงาน ดังนั้นรายงานจะเปิดไปยังหน้าที่ประกอบด้วยการแสดงภาพนี้</span><span class="sxs-lookup"><span data-stu-id="91b75-132">The original area chart tile was created in a report, so the report opens to the page that contains this visualization.</span></span>

    ![แดชบอร์ดตัวอย่างการวิเคราะห์การค้าปลีก](media/power-bi-visualization-introduction-to-q-and-a/power-bi-dashboard.png)

1. <span data-ttu-id="91b75-134">เปิดรายงานในมุมมองการแก้ไขโดยการเลือก **แก้ไขรายงาน**</span><span class="sxs-lookup"><span data-stu-id="91b75-134">Open the report in Editing View by selecting **Edit Report**.</span></span>  <span data-ttu-id="91b75-135">ถ้าคุณไม่ได้เป็นเจ้าของรายงาน คุณจะไม่มีตัวเลือกในการเปิดรายงานในมุมมองแก้ไข</span><span class="sxs-lookup"><span data-stu-id="91b75-135">If you aren't the owner of a report, you don't have the option to open the report in Editing view.</span></span>
   
    ![แก้ไขปุ่มรายงาน](media/power-bi-visualization-introduction-to-q-and-a/power-bi-edit-report.png)
4. <span data-ttu-id="91b75-137">เลือกแผนภูมิพื้นที่และตรวจทานการตั้งค่าในพื้นที่ **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="91b75-137">Select the area chart and review the settings in the **Fields** pane.</span></span>  <span data-ttu-id="91b75-138">ผู้สร้างรายงานสร้างแผนภูมินี้โดยการเลือกทั้งสามค่านี้ (**ยอดขายปีที่แล้ว** และ **ยอดขายในปีนี้ > ค่า** จากตาราง **ยอดขาย** และ **เดือนทางบัญชี** จากตาราง **เวลา**) และจัดระเบียบพวกเขาในพื้นที่ **แกน** และ **ค่า**</span><span class="sxs-lookup"><span data-stu-id="91b75-138">The report creator built this chart by selecting these three values (**Last Year Sales** and **This Year Sales > Value** from the **Sales** table, and **FiscalMonth** from the **Time** table) and organizing them in the **Axis** and **Values** wells.</span></span>
   
    ![บานหน้าต่างการแสดงรูปภาพ](media/power-bi-visualization-introduction-to-q-and-a/gnatutorial_3-new.png)

    <span data-ttu-id="91b75-140">คุณเห็นพวกเขาจบลงด้วยวิชวลที่เหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="91b75-140">You see they ended up with the same visual.</span></span> <span data-ttu-id="91b75-141">การสร้างแบบนี้ไม่ซับซ้อนเกินไป</span><span class="sxs-lookup"><span data-stu-id="91b75-141">Creating it this way wasn't too complicated.</span></span> <span data-ttu-id="91b75-142">แต่การสร้างด้วยถามตอบ (Q&A) นั้นง่ายกว่า!</span><span class="sxs-lookup"><span data-stu-id="91b75-142">But creating it with Q&A was easier!</span></span>

## <a name="next-steps"></a><span data-ttu-id="91b75-143">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="91b75-143">Next steps</span></span>

- [<span data-ttu-id="91b75-144">ใช้การถามตอบในแดชบอร์ดและรายงาน</span><span class="sxs-lookup"><span data-stu-id="91b75-144">Use Q&A in dashboards and reports</span></span>](power-bi-tutorial-q-and-a.md)  
- [<span data-ttu-id="91b75-145">การถามตอบสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="91b75-145">Q&A for consumers</span></span>](../consumer/end-user-q-and-a.md)
- [<span data-ttu-id="91b75-146">ทำให้ข้อมูลของคุณทำงานได้ดีกับการถามตอบใน Power BI</span><span class="sxs-lookup"><span data-stu-id="91b75-146">Make your data work well with Q&A in Power BI</span></span>](service-prepare-data-for-q-and-a.md)

<span data-ttu-id="91b75-147">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="91b75-147">More questions?</span></span> [<span data-ttu-id="91b75-148">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="91b75-148">Try the Power BI Community</span></span>](https://community.powerbi.com/)
