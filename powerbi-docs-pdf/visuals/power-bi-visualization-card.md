---
title: การแสดงภาพการ์ด (ไทล์จำนวนมาก)
description: สร้างการแสดงภาพการ์ดใน Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 05/05/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: f1d4a5b2d69c6d0b2d8cbec8d48e2be00b5a0f78
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96409987"
---
# <a name="create-card-visualizations"></a><span data-ttu-id="72a09-103">สร้างการแสดงภาพการ์ด</span><span class="sxs-lookup"><span data-stu-id="72a09-103">Create card visualizations</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="72a09-104">บางครั้งตัวเลขเพียงตัวเดียวก็เป็นสิ่งสำคัญที่สุดที่คุณต้องการติดตามในแดชบอร์ด Power BI หรือรายงานของคุณ เช่น ยอดขายรวม ส่วนแบ่งตลาดแบบปีต่อปี ตลาดแชร์ปีปี หรือโอกาสทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="72a09-104">Sometimes a single number is the most important thing you want to track in your Power BI dashboard or report, such as total sales, market share year over year, or total opportunities.</span></span> <span data-ttu-id="72a09-105">แสดงภาพชนิดนี้จะเรียกว่า *การ์ด*</span><span class="sxs-lookup"><span data-stu-id="72a09-105">This type of visualization is called a *Card*.</span></span> <span data-ttu-id="72a09-106">เช่นเดียวกับการแสดงภาพดั้งเดิมของ Power BI แทบจะทุกชนิด คุณสามารถสร้างการ์ดขึ้นได้ โดยใช้ตัวแก้ไขรายงาน หรือการถามตอบ</span><span class="sxs-lookup"><span data-stu-id="72a09-106">As with almost all of the native Power BI visualizations, Cards can be created using the report editor or Q&A.</span></span>

![การแสดงภาพการ์ด](media/power-bi-visualization-card/pbi-opptuntiescard.png)

> [!NOTE]
> <span data-ttu-id="72a09-108">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="72a09-108">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="72a09-109">เงื่อนไขเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="72a09-109">Prerequisite</span></span>

<span data-ttu-id="72a09-110">บทช่วยสอนนี้ใช้ [ไฟล์ PBIX ตัวอย่าง การวิเคราะห์การขายปลีก](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix)</span><span class="sxs-lookup"><span data-stu-id="72a09-110">This tutorial uses the [Retail Analysis sample PBIX file](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix)</span></span>

1. <span data-ttu-id="72a09-111">จากส่วนซ้ายบนของแถบเมนู เลือก **ไฟล์** \> **เปิด**</span><span class="sxs-lookup"><span data-stu-id="72a09-111">From the upper left section of the menubar, select **File** \> **Open**</span></span>
   
2. <span data-ttu-id="72a09-112">ค้นหาสำเนา **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก**</span><span class="sxs-lookup"><span data-stu-id="72a09-112">Find your copy of the **Retail Analysis sample PBIX file**</span></span>

1. <span data-ttu-id="72a09-113">เปิด **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก** ในมุมมองรายงาน ![ภาพหน้าจอไอคอนมุมมองรายงาน](media/power-bi-visualization-kpi/power-bi-report-view.png)</span><span class="sxs-lookup"><span data-stu-id="72a09-113">Open the **Retail Analysis sample PBIX file** in report view ![Screenshot of the report view icon.](media/power-bi-visualization-kpi/power-bi-report-view.png).</span></span>

1. <span data-ttu-id="72a09-114">เลือก</span><span class="sxs-lookup"><span data-stu-id="72a09-114">Select</span></span> ![สกรีนช็อตของแท็บสีเหลือง](media/power-bi-visualization-kpi/power-bi-yellow-tab.png) <span data-ttu-id="72a09-116">หากต้องการเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="72a09-116">to add a new page.</span></span>

## <a name="option-1-create-a-card-using-the-report-editor"></a><span data-ttu-id="72a09-117">ตัวเลือกที่ 1: สร้างการ์ดโดยใช้ตัวแก้ไขรายงาน</span><span class="sxs-lookup"><span data-stu-id="72a09-117">Option 1: Create a card using the report editor</span></span>

<span data-ttu-id="72a09-118">วิธีแรกในการจัดทำการ์ดคือใช้ Report Editor จาก Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="72a09-118">The first method to create a card is to use the report editor in Power BI Desktop.</span></span>

1. <span data-ttu-id="72a09-119">เริ่มที่หน้ารายงานว่าง และเลือก **ร้านค้า** \> เขตข้อมูล **เปิดจำนวนร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="72a09-119">Start on a blank report page and select the **Store** \> **Open store count** field.</span></span>

    <span data-ttu-id="72a09-120">Power BI จะสร้างแผนภูมิคอลัมน์ที่มีตัวเลขเพียงตัวเลขเดียว</span><span class="sxs-lookup"><span data-stu-id="72a09-120">Power BI creates a column chart with the one number.</span></span>

   ![ตัวอย่างแผนภูมิไทล์ตัวเลข](media/power-bi-visualization-card/pbi-overview-chart.png)

2. <span data-ttu-id="72a09-122">ในบานหน้าต่างการแสดงภาพ ให้เลือกไอคอนการ์ด</span><span class="sxs-lookup"><span data-stu-id="72a09-122">In the Visualizations pane, select the card icon.</span></span>

   ![ตัวอย่างการ์ดชื่อแบบตัวเลข](media/power-bi-visualization-card/power-bi-card-visualization.png)

<span data-ttu-id="72a09-124">คุณจัดทำการ์ดพร้อม Report Editor เสร็จสิ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="72a09-124">You have now successfully created a card with the report editor.</span></span> <span data-ttu-id="72a09-125">ต่อไปนี้เป็นตัวเลือกที่สองในการจัดทำการ์ดโดยใช้ช่องคำถาม ถามตอบ</span><span class="sxs-lookup"><span data-stu-id="72a09-125">Below is the second option for creating a card using the Q&A question box.</span></span>

## <a name="option-2-create-a-card-from-the-qa-question-box"></a><span data-ttu-id="72a09-126">ตัวเลือกที่ 2: สร้างการ์ดจากกล่องคำถามการถามตอบ</span><span class="sxs-lookup"><span data-stu-id="72a09-126">Option 2: Create a card from the Q&A question box</span></span>
<span data-ttu-id="72a09-127">กล่องคำถาม ถามตอบ เป็นอีกทางเลือกสำหรับคุณในการใช้ขณะจัดทำการ์ด</span><span class="sxs-lookup"><span data-stu-id="72a09-127">The Q&A question box is another option for you to use when creating a card.</span></span> <span data-ttu-id="72a09-128">ช่องคำถาม ถามตอบ มีอยู่ในมุมมองรายงานของ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="72a09-128">The Q&A question box is available in Power BI Desktop report view.</span></span>

1. <span data-ttu-id="72a09-129">เริ่มต้นบน หน้ารายงานเปล่า</span><span class="sxs-lookup"><span data-stu-id="72a09-129">Start on a blank report page</span></span>

1. <span data-ttu-id="72a09-130">ด้านบนของหน้าต่าง ให้เลือกไอคอน **ถามคำถาม**</span><span class="sxs-lookup"><span data-stu-id="72a09-130">At the top of your window, select the **Ask a Question** icon.</span></span> 

    <span data-ttu-id="72a09-131">Power BI จะจัดทำการ์ดและช่องสำหรับคำถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="72a09-131">Power BI will create a card and a box for your question.</span></span> 

   ![ตำแหน่งไอคอนถามคำถาม](media/power-bi-visualization-card/power-bi-q-and-a-overview.png)

2. <span data-ttu-id="72a09-133">เช่น พิมพ์ “Total Sales for Tina” ในช่องคำถาม</span><span class="sxs-lookup"><span data-stu-id="72a09-133">For example, type "Total Sales for Tina" in the question box.</span></span>

    <span data-ttu-id="72a09-134">กล่องคำถามจะคอยช่วยเหลือคุณ โดยจะมีคำแนะนำรวมทั้งการกล่าวซ้ำ และสุดท้ายก็จะแสดงจำนวนรวม</span><span class="sxs-lookup"><span data-stu-id="72a09-134">The question box helps you with suggestions and restatements, and finally displays the total number.</span></span>  

   ![ตัวอย่างช่องคำถาม](media/power-bi-visualization-card/power-bi-q-and-a-box.png)

   ![ตัวอย่างการ์ดจากวิธีการถาม](media/power-bi-visualization-card/power-bi-q-and-a-card.png)

<span data-ttu-id="72a09-137">คุณจัดทำการ์ดพร้อมช่องคำถาม ถามตอบ เสร็จสิ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="72a09-137">You have now successfully created a card with the Q&A question box.</span></span> <span data-ttu-id="72a09-138">ต่อไปนี้เป็นขั้นตอนในการกำหนดรูปแบบการ์ดของคุณตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="72a09-138">Below are steps for formatting your card to your specific needs.</span></span>

## <a name="format-a-card"></a><span data-ttu-id="72a09-139">จัดรูปแบบการ์ด</span><span class="sxs-lookup"><span data-stu-id="72a09-139">Format a card</span></span>
<span data-ttu-id="72a09-140">คุณมีตัวเลือกมากมายสำหรับการเปลี่ยนป้ายชื่อ, ข้อความ, สี และอีกมาก</span><span class="sxs-lookup"><span data-stu-id="72a09-140">You have many options for changing labels, text, color and more.</span></span> <span data-ttu-id="72a09-141">วิธีดีที่สุดในการเรียนรู้คือ สร้างการ์ด จากนั้นสำรวจบานหน้าต่างการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="72a09-141">The best way to learn is to create a card and then explore the Formatting pane.</span></span> <span data-ttu-id="72a09-142">ต่อไปนี้เป็นเพียงบางตัวเลือกของการจัดรูปแบบที่มี</span><span class="sxs-lookup"><span data-stu-id="72a09-142">Here are just a few of the formatting options available.</span></span> 

<span data-ttu-id="72a09-143">บานหน้าต่างการจัดรูปแบบจะพร้อมใช้งานขณะโต้ตอบกับการ์ดในรายงาน</span><span class="sxs-lookup"><span data-stu-id="72a09-143">The Formatting pane is available when interacting with the card in a report.</span></span> 

1. <span data-ttu-id="72a09-144">เริ่มต้นด้วยการเลือกไอคอนรูปลูกกลิ้งทาสีเพื่อเปิดบานหน้าต่างการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="72a09-144">Start by selecting the paint roller icon to open the Formatting pane.</span></span> 

    ![การ์ดที่มีเค้าโครงลูกกลิ้งทาสี](media/power-bi-visualization-card/power-bi-format-card-2.png)

2. <span data-ttu-id="72a09-146">ด้วยการ์ดที่เลือก ขยาย **ป้ายชื่อข้อมูล** และเปลี่ยนสี ขนาด และตระกูลแบบอักษร</span><span class="sxs-lookup"><span data-stu-id="72a09-146">With the card selected, expand **Data label** and change the color, size, and font family.</span></span> <span data-ttu-id="72a09-147">ถ้าคุณมีหลายพันร้านค้า คุณสามารถใช้ **แสดงหน่วย** เพื่อแสดงจำนวนของร้านค้าเป็นหลักพัน และควบคุมตำแหน่งทศนิยมได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="72a09-147">If you had thousands of stores, you could use **Display units** to show the number of stores by thousands and control the decimal places as well.</span></span> <span data-ttu-id="72a09-148">ตัวอย่างเช่น แสดง 125.8K แทนที่จะเป็น 125,832.00</span><span class="sxs-lookup"><span data-stu-id="72a09-148">For example, 125.8K instead of 125,832.00.</span></span>

    ![ตัวอย่างการ์ดพร้อมรูปแบบข้อมูล](media/power-bi-visualization-card/power-bi-card-format-2.png)

3.  <span data-ttu-id="72a09-150">ขยาย **ป้ายชื่อประเภท** และเปลี่ยนสีและขนาด</span><span class="sxs-lookup"><span data-stu-id="72a09-150">Expand **Category label** and change the color and size.</span></span>

    ![ตัวอย่างการ์ดพร้อมหมวดหมู่](media/power-bi-visualization-card/power-bi-card-format-category.png)

4. <span data-ttu-id="72a09-152">ขยาย **พื้นหลัง** และเลื่อนแถบเลื่อนเป็นเปิด</span><span class="sxs-lookup"><span data-stu-id="72a09-152">Expand **Background** and move the slider to On.</span></span>  <span data-ttu-id="72a09-153">ตอนนี้คุณสามารถเปลี่ยนสีพื้นหลังและความโปร่งใส</span><span class="sxs-lookup"><span data-stu-id="72a09-153">Now you can change the background color and transparency.</span></span>

    ![ตั้งค่าเป็นเปิดแถบเลื่อน](media/power-bi-visualization-card/power-bi-format-color-2.png)

5. <span data-ttu-id="72a09-155">ลองสำรวจตัวเลือกการจัดรูปแบบต่อไป จนกว่าการ์ดของคุณเป็นแบบที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="72a09-155">Continue to explore the formatting options until your card is exactly how you'd like it.</span></span> 

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="72a09-156">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="72a09-156">Considerations and troubleshooting</span></span>

<span data-ttu-id="72a09-157">ถ้าคุณไม่เห็นกล่องคำถามทั้งหมด โปรดติดต่อผู้ดูแลระบบ Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="72a09-157">If you do not see a question box at all, contact your Power BI admin.</span></span>

## <a name="next-steps"></a><span data-ttu-id="72a09-158">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="72a09-158">Next steps</span></span>
[<span data-ttu-id="72a09-159">แผนภูมิผสมใน Power BI</span><span class="sxs-lookup"><span data-stu-id="72a09-159">Combo charts in Power BI</span></span>](power-bi-visualization-combo-chart.md)

[<span data-ttu-id="72a09-160">ชนิดการแสดงภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="72a09-160">Visualization types in Power BI</span></span>](power-bi-visualization-types-for-reports-and-q-and-a.md)
