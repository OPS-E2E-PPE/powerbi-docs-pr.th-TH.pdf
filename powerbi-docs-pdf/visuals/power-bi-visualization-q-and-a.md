---
title: สร้างวิชวลถามตอบใน Power BI
description: วิธีการสร้างและจัดรูปแบบวิชวลถามตอบ Power BI ใน Power BI Desktop หรือบริการของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: rien
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 01/05/2021
ms.openlocfilehash: 1cf80593458c12a1bee07ed40202e3613fdcb5e9
ms.sourcegitcommit: c700e78dfedc34f5a74b23bbefdaef77e2a87f8a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/07/2021
ms.locfileid: "97961373"
---
# <a name="create-a-qa-visual-in-power-bi"></a><span data-ttu-id="4fd40-103">สร้างวิชวลถามตอบใน Power BI</span><span class="sxs-lookup"><span data-stu-id="4fd40-103">Create a Q&A visual in Power BI</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]    

<span data-ttu-id="4fd40-104">วิชวลถามตอบช่วยให้ผู้ใช้สามารถถามคำถามที่เป็นภาษาธรรมชาติและรับคำตอบในรูปแบบของวิชวลได้</span><span class="sxs-lookup"><span data-stu-id="4fd40-104">The Q&A visual allows users to ask natural language questions and get answers in the form of a visual.</span></span> <span data-ttu-id="4fd40-105">*ผู้บริโภค* สามารถใช้วิชวลถามตอบเพื่อหาคำตอบสำหรับข้อมูลของตนเองได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="4fd40-105">*Consumers* can use it to quickly get answers to their data.</span></span> <span data-ttu-id="4fd40-106">*นักออกแบบ* ยังสามารถใช้วิชวลถามตอบเพื่อสร้างวิชวลได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="4fd40-106">*Designers* can also use it to create visuals quickly.</span></span> <span data-ttu-id="4fd40-107">หากคุณเป็นนักออกแบบรายงาน บทความนี้เหมาะสำหรับคุณ</span><span class="sxs-lookup"><span data-stu-id="4fd40-107">If you're a report designer, this article is for you.</span></span> <span data-ttu-id="4fd40-108">คุณสามารถดับเบิลคลิกที่ใดก็ได้ในรายงาน และใช้ภาษาธรรมชาติเพื่อเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="4fd40-108">You can double-click anywhere on a report and use natural language to get started.</span></span> <span data-ttu-id="4fd40-109">ในบทความนี้ คุณจะได้สร้าง จัดรูปแบบ และปรับแต่งวิชวลถามตอบ</span><span class="sxs-lookup"><span data-stu-id="4fd40-109">In this article, you create, format, and customize a Q&A visual.</span></span> <span data-ttu-id="4fd40-110">วิชวลถามตอบยังสนับสนุนธีมและตัวเลือกการจัดรูปแบบเริ่มต้นอื่น ๆ ที่พร้อมใช้งานภายใน Power BI</span><span class="sxs-lookup"><span data-stu-id="4fd40-110">It supports themes and other default formatting options available inside Power BI.</span></span> <span data-ttu-id="4fd40-111">หลังจากที่คุณสร้างแล้ว วิชวลถามตอบนี้จะทำงานเหมือนกับวิชวลอื่น ๆ โดยการสนับสนุนการกรองข้าม การไฮไลต์ข้าม และบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="4fd40-111">After you create it, it behaves like any other visual, supporting cross-filtering, cross-highlighting, and bookmarks.</span></span> 

<span data-ttu-id="4fd40-112">กำลังมองหาพื้นหลังเพิ่มเติมเกี่ยวกับถามตอบใน Power BI ใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="4fd40-112">Looking for more background about Q&A in Power BI?</span></span> <span data-ttu-id="4fd40-113">ดู[บทนำการถามตอบ](../natural-language/q-and-a-intro.md)</span><span class="sxs-lookup"><span data-stu-id="4fd40-113">Check out [Introduction to Q&A](../natural-language/q-and-a-intro.md).</span></span> 

![ภาพรวมของวิชวลถามตอบ](../natural-language/media/qna-visual-walkthrough.gif)

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="4fd40-115">วิชวลถามตอบประกอบด้วยสี่องค์ประกอบหลัก:</span><span class="sxs-lookup"><span data-stu-id="4fd40-115">The Q&A visual consists of four core components:</span></span>

- <span data-ttu-id="4fd40-116">กล่องคำถาม</span><span class="sxs-lookup"><span data-stu-id="4fd40-116">The question box.</span></span> <span data-ttu-id="4fd40-117">กล่องนี้เป็นตำแหน่งที่ผู้ใช้สามารถพิมพ์คำถามของตน และจะแสดงคำแนะนำเพื่อช่วยตอบคำถามของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="4fd40-117">This is where users type in their question and are shown suggestions to help them complete their question.</span></span>
- <span data-ttu-id="4fd40-118">รายการของคำถามที่แนะนำที่มีการเติมข้อมูลไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="4fd40-118">A pre-populated list of suggested questions.</span></span>
- <span data-ttu-id="4fd40-119">ไอคอนเพื่อแปลงวิชวลถามตอบเป็นวิชวลมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="4fd40-119">Icon to convert the Q&A visual into a standard visual.</span></span> 
- <span data-ttu-id="4fd40-120">ไอคอนเพื่อเปิดการใช้เครื่องมือถามตอบ ซึ่งช่วยให้ผู้ออกแบบสามารถกำหนดค่ากลไกจัดการภาษาธรรมชาติเบื้องต้นได้</span><span class="sxs-lookup"><span data-stu-id="4fd40-120">Icon to open Q&A tooling, which allows designers to configure the underlying natural language engine.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4fd40-121">สิ่งที่จำเป็นต้องมี</span><span class="sxs-lookup"><span data-stu-id="4fd40-121">Prerequisites</span></span>

1. <span data-ttu-id="4fd40-122">ดาวน์โหลด [ไฟล์ PBIX ตัวอย่างการขายและการตลาด](https://download.microsoft.com/download/9/7/6/9767913A-29DB-40CF-8944-9AC2BC940C53/Sales%20and%20Marketing%20Sample%20PBIX.pbix) เพื่อทำตาม</span><span class="sxs-lookup"><span data-stu-id="4fd40-122">Download [Sales & Marketing sample PBIX file](https://download.microsoft.com/download/9/7/6/9767913A-29DB-40CF-8944-9AC2BC940C53/Sales%20and%20Marketing%20Sample%20PBIX.pbix) to follow along.</span></span>

1. <span data-ttu-id="4fd40-123">ในส่วนซ้ายบนของ Power BI Desktop ให้เลือก **ไฟล์** > **เปิด**</span><span class="sxs-lookup"><span data-stu-id="4fd40-123">In the upper left section of the Power BI Desktop, select **File** > **Open**.</span></span>
   
2. <span data-ttu-id="4fd40-124">ค้นหาสำเนาของ **ไฟล์ PBIX ตัวอย่างการขายและการตลาด**</span><span class="sxs-lookup"><span data-stu-id="4fd40-124">Find your copy of the **Sales & Marketing sample PBIX file**.</span></span>

1. <span data-ttu-id="4fd40-125">เปิดไฟล์ในมุมมองรายงาน</span><span class="sxs-lookup"><span data-stu-id="4fd40-125">Open the file in report view</span></span> ![สกรีนช็อตของไอคอนมุมมองรายงาน](media/power-bi-visualization-kpi/power-bi-report-view.png)<span data-ttu-id="4fd40-127">.</span><span class="sxs-lookup"><span data-stu-id="4fd40-127">.</span></span>

1. <span data-ttu-id="4fd40-128">เลือกเครื่องหมายบวก</span><span class="sxs-lookup"><span data-stu-id="4fd40-128">Select the plus sign</span></span> ![สกรีนช็อตของแท็บสีเหลือง](media/power-bi-visualization-kpi/power-bi-yellow-tab.png) <span data-ttu-id="4fd40-130">หากต้องการเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="4fd40-130">to add a new page.</span></span>

<span data-ttu-id="4fd40-131">หากคุณเห็นข้อผิดพลาดขณะที่สร้างวิชวลถามตอบ คุณต้องตรวจสอบบทความ [ข้อจำกัดการถามตอบ](../natural-language/q-and-a-limitations.md) เพื่อดูว่ามีการรองรับการกำหนดค่าแหล่งข้อมูลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4fd40-131">If you see an error when creating a Q&A visual, be sure to check the [Q&A limitations](../natural-language/q-and-a-limitations.md) article to see if the data source configuration is supported.</span></span>    

> [!NOTE]
> <span data-ttu-id="4fd40-132">คุณจำเป็นต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการหรือคุณต้องบันทึกรายงานในพื้นที่ทำงานที่มีความจุแบบพรีเมียมเพื่อแชร์รายงานของคุณกับผู้ร่วมงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="4fd40-132">Sharing your report with a Power BI colleague requires that either you both have individual Power BI Pro licenses or you save the report in a Premium capacity workspace.</span></span> <span data-ttu-id="4fd40-133">ดู [การแชร์รายงาน](../collaborate-share/service-share-dashboards.md)</span><span class="sxs-lookup"><span data-stu-id="4fd40-133">See [sharing reports](../collaborate-share/service-share-dashboards.md).</span></span>

## <a name="create-a-qa-visual-using-a-suggested-question"></a><span data-ttu-id="4fd40-134">สร้างวิชวลถามตอบโดยใช้คำถามที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="4fd40-134">Create a Q&A visual using a suggested question</span></span>
<span data-ttu-id="4fd40-135">ในแบบฝึกหัดนี้ เราจะเลือกหนึ่งในคำถามที่แนะนำเพื่อสร้างวิชวลถามตอบ</span><span class="sxs-lookup"><span data-stu-id="4fd40-135">In this exercise, we'll select one of the suggested questions to create our Q&A visual.</span></span> 

1. <span data-ttu-id="4fd40-136">เริ่มต้นบนหน้ารายงานที่ว่างเปล่าและเลือกไอคอนวิชวลถามตอบจากบานหน้าต่างการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="4fd40-136">Start on a blank report page and select the Q&A visual icon from the Visualizations pane.</span></span>

    ![บานหน้าต่างการแสดงภาพที่มีไอคอนวิชวลถามตอบที่ระบุ](media/power-bi-visualization-q-and-a/power-bi-icon.png)

2. <span data-ttu-id="4fd40-138">ลากเส้นขอบเพื่อปรับขนาดวิชวล</span><span class="sxs-lookup"><span data-stu-id="4fd40-138">Drag the border to resize the visual.</span></span>

    ![วิชวลถามตอบบนพื้นที่รายงาน](media/power-bi-visualization-q-and-a/power-bi-qna.png)

3. <span data-ttu-id="4fd40-140">หากต้องการสร้างวิชวล เลือกหนึ่งในคำถามที่แนะนำหรือเริ่มพิมพ์ลงในกล่องคำถาม</span><span class="sxs-lookup"><span data-stu-id="4fd40-140">To create the visual, select one of the suggested questions or start typing in the question box.</span></span> <span data-ttu-id="4fd40-141">ในตัวอย่างนี้ เราได้เลือก **รัฐทางภูมิศาสตร์ตามผลรวมของรายได้**.</span><span class="sxs-lookup"><span data-stu-id="4fd40-141">In this example, we've selected **top geo states by sum of revenue**.</span></span> <span data-ttu-id="4fd40-142">Power BI เหมาะที่สุดในการเลือกชนิดของวิชวลที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="4fd40-142">Power BI does its best to select which visual type to use.</span></span> <span data-ttu-id="4fd40-143">ในกรณีนี้ คือแผนที่</span><span class="sxs-lookup"><span data-stu-id="4fd40-143">In this case, it's a map.</span></span>

    ![แผนที่วิชวลถามตอบ](media/power-bi-visualization-q-and-a/power-bi-map.png)

    <span data-ttu-id="4fd40-145">แต่คุณสามารถบอก Power BI ว่าจะใช้วิชวลชนิดใดโดยการเพิ่มลงในคิวรีภาษาธรรมชาติของคุณ</span><span class="sxs-lookup"><span data-stu-id="4fd40-145">But you can tell Power BI which visual type to use by adding it to your natural language query.</span></span> <span data-ttu-id="4fd40-146">โปรดทราบว่าไม่ใช่วิชวลทุกชนิดที่จะทำงานหรือเข้ากับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="4fd40-146">Keep in mind that not all visual types will work or make sense with your data.</span></span> <span data-ttu-id="4fd40-147">ตัวอย่างเช่น ข้อมูลนี้จะไม่สร้างแผนภูมิแบบกระจายที่มีความหมาย</span><span class="sxs-lookup"><span data-stu-id="4fd40-147">For example, this data wouldn't produce a meaningful scatter chart.</span></span> <span data-ttu-id="4fd40-148">แต่จะใช้เป็นแผนที่แบบเติม</span><span class="sxs-lookup"><span data-stu-id="4fd40-148">But it works as a filled map.</span></span>

    ![วิชวลถามตอบที่เป็นแผนที่แบบเติม](media/power-bi-visualization-q-and-a/power-bi-specify-map.png)

## <a name="create-a-qa-visual-using-a-natural-language-query"></a><span data-ttu-id="4fd40-150">สร้างวิชวลถามตอบโดยใช้คิวรีภาษาธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="4fd40-150">Create a Q&A visual using a natural language query</span></span>
<span data-ttu-id="4fd40-151">ในตัวอย่างข้างต้น เราได้เลือกหนึ่งในคำถามที่แนะนำเพื่อสร้างวิชวลถามตอบ</span><span class="sxs-lookup"><span data-stu-id="4fd40-151">In the example above, we selected one of the suggested questions to create our Q&A visual.</span></span>  <span data-ttu-id="4fd40-152">ในแบบฝึกหัดนี้ เราจะพิมพ์คำถามของเราเอง</span><span class="sxs-lookup"><span data-stu-id="4fd40-152">In this exercise, we'll type our own question.</span></span> <span data-ttu-id="4fd40-153">ในขณะที่เราพิมพ์คำถามของเรา Power BI จะช่วยเราด้วยการกรอกข้อมูลอัตโนมัติ การให้คำแนะนำ และคำติชม</span><span class="sxs-lookup"><span data-stu-id="4fd40-153">As we type our question, Power BI helps us with autocomplete, suggestion, and feedback.</span></span>

<span data-ttu-id="4fd40-154">ถ้าคุณไม่แน่ใจว่าคำถามประเภทใดที่ต้องถามหรือคำศัพท์ที่ต้องใช้ ให้ขยาย **แสดงคำแนะนำทั้งหมด** หรือค้นหาในบานหน้าต่างเขตข้อมูลทางด้านขวาของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="4fd40-154">If you're unsure what type of questions to ask or terminology to use, expand **Show all suggestions** or look through the Fields pane along the right side of the canvas.</span></span> <span data-ttu-id="4fd40-155">บานหน้าต่างเขตข้อมูลนี้จะทำให้คุณคุ้นเคยกับศัพท์และเนื้อหาของชุดข้อมูลการขายและการตลาด</span><span class="sxs-lookup"><span data-stu-id="4fd40-155">The Fields pane will get you familiar with the terms and content of the Sales & Marketing dataset.</span></span>

![พื้นที่ทำงานที่มีบานหน้าต่างแสดงคำแนะนำทั้งหมดและเขตข้อมูลที่ระบุ](media/power-bi-visualization-q-and-a/power-bi-terminology.png)


1. <span data-ttu-id="4fd40-157">พิมพ์คำถามในเขตข้อมูลถามตอบ</span><span class="sxs-lookup"><span data-stu-id="4fd40-157">Type a question in the Q&A field.</span></span> <span data-ttu-id="4fd40-158">Power BI เพิ่มขีดเส้นใต้สีแดงเป็นคำที่ไม่รู้จัก</span><span class="sxs-lookup"><span data-stu-id="4fd40-158">Power BI adds a red underline to words it does not recognize.</span></span> <span data-ttu-id="4fd40-159">เมื่อใดก็ตามที่เป็นไปได้ Power BI จะช่วยกำหนดคำที่ไม่รู้จัก</span><span class="sxs-lookup"><span data-stu-id="4fd40-159">Whenever possible, Power BI helps define unrecognized words.</span></span>  <span data-ttu-id="4fd40-160">ในตัวอย่างแรกด้านล่าง ให้เลือกคำแนะนำใดก็ตามที่จะใช้ได้กับเรา</span><span class="sxs-lookup"><span data-stu-id="4fd40-160">In the first example below, selecting either of the suggestions will work for us.</span></span>  

    ![การพิมพ์คำถามในกล่องคำถามสำหรับถามตอบ](media/power-bi-visualization-q-and-a/power-bi-red-suggest.png)

2. <span data-ttu-id="4fd40-162">ในขณะที่เราพิมพ์คำถามเพิ่มเติม Power BI ช่วยให้เราทราบว่าระบบไม่เข้าใจคำถามและพยายามช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="4fd40-162">As we type more of the question, Power BI lets us know that it doesn't understand the question, and tries to help.</span></span> <span data-ttu-id="4fd40-163">ในตัวอย่างด้านล่าง Power BI จะถามเราว่า "คุณหมายถึง ..." และแสดงให้เห็นวิธีการที่แตกต่างกันในการตั้งคำถามของเราโดยใช้ศัพท์จากชุดข้อมูลของเรา</span><span class="sxs-lookup"><span data-stu-id="4fd40-163">In the example below, Power BI asks us "Did you mean..." and suggests a different way to word our question using terminology from our dataset.</span></span> 

    ![วิชวลถามตอบที่แสดงคำแนะนำ](media/power-bi-visualization-q-and-a/power-bi-define.png)

5. <span data-ttu-id="4fd40-165">ด้วยความช่วยเหลือของ Power BI เราสามารถตั้งคำถามด้วยศัพท์ที่เป็นที่รู้จักทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="4fd40-165">With Power BI's help, we were able to ask a question with all recognizable terms.</span></span> <span data-ttu-id="4fd40-166">Power BI จะแสดงผลลัพธ์เป็นแผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="4fd40-166">Power BI displays the results as a line chart.</span></span> 

    ![ผลลัพธ์ของวิชวลถามตอบ](media/power-bi-visualization-q-and-a/power-bi-type.png)


6. <span data-ttu-id="4fd40-168">ลองเปลี่ยนวิชวลเป็นแผนภูมิคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="4fd40-168">Let's change the visual to a column chart.</span></span> 

    ![วิชวลถามตอบที่เพิ่ม "เป็นแผนภูมิคอลัมน์" ลงในคำถาม](media/power-bi-visualization-q-and-a/power-bi-specify-visual.png)

7.  <span data-ttu-id="4fd40-170">เพิ่มวิชวลเพิ่มเติมในหน้ารายงานและดูว่าวิชวลถามตอบ (Q&A) โต้ตอบกับวิชวลอื่น ๆ ในหน้าได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="4fd40-170">Add more visuals to the report page and see how the Q&A visual interacts with the other visuals on the page.</span></span> <span data-ttu-id="4fd40-171">ในตัวอย่างนี้ วิชวลถามตอบ (Q&A) ได้กรองแผนภูมิเส้นแบบกรองข้าม และแมปและไฮไลท์ข้ามแผนภูมิแท่ง</span><span class="sxs-lookup"><span data-stu-id="4fd40-171">In this example, the Q&A visual has cross-filtered the line chart and map and cross-highlighted the bar chart.</span></span>

    ![วิชวลถามตอบ (Q&A) ที่มีหนึ่งแถบถูกเลือก และส่งผลกระทบต่อวิชวลทั้งสามบนหน้ารายงาน](media/power-bi-visualization-q-and-a/power-bi-filters.png)

## <a name="format-and-customize-the-qa-visual"></a><span data-ttu-id="4fd40-173">จัดรูปแบบและปรับแต่งวิชวลถามตอบ</span><span class="sxs-lookup"><span data-stu-id="4fd40-173">Format and customize the Q&A visual</span></span>
<span data-ttu-id="4fd40-174">วิชวลถามตอบสามารถปรับแต่งได้โดยใช้บานหน้าต่างการจัดรูปแบบและโดยการใช้ธีม</span><span class="sxs-lookup"><span data-stu-id="4fd40-174">The Q&A visual can be customized using the formatting pane, and by applying a theme.</span></span> 

### <a name="apply-a-theme"></a><span data-ttu-id="4fd40-175">นำธีมไปใช้</span><span class="sxs-lookup"><span data-stu-id="4fd40-175">Apply a theme</span></span>
<span data-ttu-id="4fd40-176">เมื่อคุณเลือกธีม ธีมดังกล่าวจะถูกนำไปใช้กับหน้ารายงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4fd40-176">When you select a theme, that theme is applied to the entire report page.</span></span> <span data-ttu-id="4fd40-177">มีธีมมากมายให้เลือก ลองใช้จนกว่าคุณจะได้รูปลักษณ์ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="4fd40-177">There are many themes to choose from, so try them out until you get the look you desire.</span></span> 

1. <span data-ttu-id="4fd40-178">ในแถบเมนู ให้เลือกแท็บ **หน้าแรก** และเลือก **สลับธีม**.</span><span class="sxs-lookup"><span data-stu-id="4fd40-178">In the menu bar, select the **Home** tab and choose **Switch theme**.</span></span> 

    ![Desktop พร้อมธีมการสลับที่เลือก](media/power-bi-visualization-q-and-a/power-bi-themes.png)

    
    
2. <span data-ttu-id="4fd40-180">ในตัวอย่างนี้ เราได้เลือก **ธีมเพิ่มเติม** > **ปลอดภัยสำหรับคนตาบอดสี**</span><span class="sxs-lookup"><span data-stu-id="4fd40-180">In this example, we've selected **More themes** > **Color blind safe**.</span></span>

    ![วิชวลถามตอบที่ใช้ธีมตาบอดสี](media/power-bi-visualization-q-and-a/power-bi-color-blind.png)

### <a name="format-the-qa-visual"></a><span data-ttu-id="4fd40-182">จัดรูปแบบวิชวลถามตอบ</span><span class="sxs-lookup"><span data-stu-id="4fd40-182">Format the Q&A visual</span></span>
<span data-ttu-id="4fd40-183">จัดรูปแบบวิชวลถามตอบ เขตข้อมูลคำถาม และวิธีการแสดงคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="4fd40-183">Format the Q&A visual, the question field, and the way suggestions are displayed.</span></span> <span data-ttu-id="4fd40-184">คุณสามารถเปลี่ยนทุกอย่างจากพื้นหลังของชื่อเรื่องให้เป็นสีโฮเวอร์สำหรับคำที่ไม่รู้จัก</span><span class="sxs-lookup"><span data-stu-id="4fd40-184">You can change everything from the background of a title to the hover color for unrecognized words.</span></span> <span data-ttu-id="4fd40-185">ต่อไปนี้เราได้เพิ่มพื้นหลังสีเทาลงในกล่องคำถามและเปลี่ยนเส้นใต้เป็นสีเหลืองและสีเขียว</span><span class="sxs-lookup"><span data-stu-id="4fd40-185">Here we've added a grey background to the question box and changed the underlines to yellow and green.</span></span> <span data-ttu-id="4fd40-186">ชื่อเรื่องอยู่กึ่งกลางและมีพื้นหลังสีเหลือง</span><span class="sxs-lookup"><span data-stu-id="4fd40-186">The title is centered and has a yellow background.</span></span> 

![วิชวลถามตอบที่แสดงผลการจัดรูปแบบของเรา](media/power-bi-visualization-q-and-a/power-bi-q-and-a-format.png)

## <a name="convert-your-qa-visual-into-a-standard-visual"></a><span data-ttu-id="4fd40-188">แปลงวิชวลถามตอบเป็นวิชวลมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="4fd40-188">Convert your Q&A visual into a standard visual</span></span>
<span data-ttu-id="4fd40-189">เราได้จัดรูปแบบวิชวลของแผนภูมิคอลัมน์ที่ปลอดภัยสำหรับคนตาบอดสีแล้วเล็กน้อย: เราเพิ่มชื่อเรื่องและเส้นขอบแล้ว</span><span class="sxs-lookup"><span data-stu-id="4fd40-189">We've formatted our color blind safe column chart visual a bit: We added a title and a border.</span></span> <span data-ttu-id="4fd40-190">ในตอนนี้ เราพร้อมที่จะแปลงเป็นวิชวลมาตรฐานในรายงานของเราและยังมีการปักหมุดไปยังแดชบอร์ดด้วย</span><span class="sxs-lookup"><span data-stu-id="4fd40-190">Now we're ready to convert it to a standard visual in our report and also pin it to a dashboard.</span></span>

<span data-ttu-id="4fd40-191">เลือกไอคอน ![ไอคอนรูปเฟือง](media/power-bi-visualization-q-and-a/power-bi-convert-icon.png)เพื่อ **เปลี่ยนผลการถามตอบนี้เป็นวิชวลมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="4fd40-191">Select the icon ![cog icon](media/power-bi-visualization-q-and-a/power-bi-convert-icon.png) to **Turn this Q&A result into a standard visual**.</span></span>

![วิชวลถามตอบที่มีลูกศรชี้ไปยังไอคอนวิชวลมาตรฐาน](media/power-bi-visualization-q-and-a/power-bi-visual-convert.png)

<span data-ttu-id="4fd40-193">วิชวลนี้ไม่ใช่วิชวลถามตอบอีกต่อไป แต่เป็นแผนภูมิคอลัมน์มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="4fd40-193">This visual is no longer a Q&A visual but is a standard column chart.</span></span> <span data-ttu-id="4fd40-194">ซึ่งสามารถปักหมุดไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="4fd40-194">It can be pinned to a dashboard.</span></span> <span data-ttu-id="4fd40-195">ในรายงาน วิชวลนี้จะทำงานเหมือนกับวิชวลมาตรฐานอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="4fd40-195">In the report, this visual behaves the same as other standard visuals.</span></span> <span data-ttu-id="4fd40-196">โปรดทราบว่าบานหน้าต่างการแสดงภาพจะแสดงไอคอนแผนภูมิคอลัมน์ที่เลือกไว้แทนไอคอนวิชวลถามตอบ</span><span class="sxs-lookup"><span data-stu-id="4fd40-196">Notice that the Visualizations pane shows a Column chart icon selected instead of the Q&A visual icon.</span></span>

<span data-ttu-id="4fd40-197">ถ้าคุณกำลังใช้\**_บริการของ Power BI_* _ คุณสามารถปักหมุดวิชวลไปยังแดชบอร์ดโดยการเลือกไอคอนปักหมุดได้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="4fd40-197">If you're using the \**_Power BI Service_* _, you can now pin the visual to a dashboard by selecting the pin icon.</span></span> 


![บริการของ Power BI ที่มีไอคอนปักหมุดที่ระบุ](media/power-bi-visualization-q-and-a/power-bi-pin.png)


## <a name="advanced-features-of-the-qa-visual"></a><span data-ttu-id="4fd40-199">คุณลักษณะขั้นสูงของวิชวลถามตอบ</span><span class="sxs-lookup"><span data-stu-id="4fd40-199">Advanced features of the Q&A visual</span></span>
<span data-ttu-id="4fd40-200">การเลือกไอคอนรูปเฟืองจะเปิดบานหน้าต่างเครื่องมือวิชวลถามตอบ</span><span class="sxs-lookup"><span data-stu-id="4fd40-200">Selecting the cog icon opens the Q&A visual Tooling pane.</span></span> 

![วิชวลถามตอบที่มีไอคอนเครื่องมือที่เลือก](media/power-bi-visualization-q-and-a/power-bi-q-and-a-tooling.png)

<span data-ttu-id="4fd40-202">ใช้บานหน้าต่างเครื่องมือเพื่อสอนศัพท์ถามตอบที่เครื่องมือไม่รู้จัก จัดการกับศัพท์เหล่านั้น และจัดการคำถามที่แนะนำสำหรับชุดข้อมูลและรายงานนี้</span><span class="sxs-lookup"><span data-stu-id="4fd40-202">Use the Tooling pane to teach Q&A terms it doesn't recognize, to manage those terms, and to manage the suggested questions for this dataset and report.</span></span> <span data-ttu-id="4fd40-203">ในบานหน้าต่างการใช้เครื่องมือ คุณยังสามารถตรวจสอบคำถามที่ผู้ใช้ถามไว้ในวิชวลถามตอบนี้ และดูคำถามต่าง ๆ ที่ผู้ใช้ตั้งค่าสถานะไว้</span><span class="sxs-lookup"><span data-stu-id="4fd40-203">In the Tooling pane, you can also review questions that users have asked in this Q&A visual and see questions that users have flagged.</span></span> <span data-ttu-id="4fd40-204">หากต้องการเรียนรู้เพิ่มเติม ให้ดูข้อมูลที่ [บทนำการใช้เครื่องมือถามตอบเพื่อฝึกฝนการถามตอบ Power BI](../natural-language/q-and-a-tooling-intro.md)</span><span class="sxs-lookup"><span data-stu-id="4fd40-204">To learn more, see [Intro to Q&A tooling to train Power BI Q&A](../natural-language/q-and-a-tooling-intro.md).</span></span>

![บานหน้าต่างเครื่องมือถามตอบ](media/power-bi-visualization-q-and-a/power-bi-q-and-a-tooling-pane.png)

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="4fd40-206">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="4fd40-206">Considerations and troubleshooting</span></span>
<span data-ttu-id="4fd40-207">วิชวลถามตอบจะทำงานร่วมกับ Office และ Bing เพื่อพยายามจับคู่คำทั่วไปที่ไม่รู้จักกับเขตข้อมูลในชุดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="4fd40-207">The Q&A visual integrates with Office and Bing to attempt to match unrecognized common words with fields in your dataset.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="4fd40-208">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4fd40-208">Next steps</span></span>

<span data-ttu-id="4fd40-209">มีหลายวิธีการที่คุณสามารถรวมภาษาธรรมชาติได้</span><span class="sxs-lookup"><span data-stu-id="4fd40-209">There are several ways you can integrate natural language.</span></span> <span data-ttu-id="4fd40-210">สำหรับข้อมูลเพิ่มเติม ให้ดูบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4fd40-210">For more information, see the following articles:</span></span>

<span data-ttu-id="4fd40-211">_ [เครื่องมือถามตอบ](../natural-language/q-and-a-tooling-intro.md)</span><span class="sxs-lookup"><span data-stu-id="4fd40-211">_ [Q&A Tooling](../natural-language/q-and-a-tooling-intro.md)</span></span>
* [<span data-ttu-id="4fd40-212">แนวทางปฏิบัติที่ดีที่สุดของการถามตอบ</span><span class="sxs-lookup"><span data-stu-id="4fd40-212">Q&A Best Practices</span></span>](../natural-language/q-and-a-best-practices.md)
