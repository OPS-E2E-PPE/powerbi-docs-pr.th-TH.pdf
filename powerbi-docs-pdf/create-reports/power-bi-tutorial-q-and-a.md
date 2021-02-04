---
title: ใช้ Power BI Q&A เพื่อสำรวจและสร้างวิชวล
description: วิธีการใช้ Power BI Q&A เพื่อสร้างการแสดงผลข้อมูลด้วยภาพใหม่บนแดชบอร์ดและรายงาน
author: maggiesMSFT
ms.author: maggies
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 05/13/2019
LocalizationGroup: Ask questions of your data
ms.openlocfilehash: 01ab8e63785680ea4fcd30cee170297f1cf1d674
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96396141"
---
# <a name="use-power-bi-qa-to-explore-your-data-and-create-visuals"></a><span data-ttu-id="c671d-103">ใช้ Power BI Q&A เพื่อสำรวจข้อมูลของคุณและสร้างวิชวล</span><span class="sxs-lookup"><span data-stu-id="c671d-103">Use Power BI Q&A to explore your data and create visuals</span></span>

<span data-ttu-id="c671d-104">ในบางครั้ง วิธีที่เร็วที่สุดในการให้ได้คำตอบจากข้อมูลของคุณคือ การถามคำถามโดยใช้ภาษาธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="c671d-104">Sometimes the fastest way to get an answer from your data is to ask a question using natural language.</span></span> <span data-ttu-id="c671d-105">คุณลักษณะถามตอบ (Q&A) ใน Power BI ช่วยให้คุณสามารถสำรวจข้อมูลของคุณด้วยคำพูดของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="c671d-105">The Q&A feature in Power BI lets you explore your data in your own words.</span></span>  <span data-ttu-id="c671d-106">ส่วนแรกของบทความนี้แสดงวิธีการใช้ถามตอบ (Q&A) ในแดชบอร์ดในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="c671d-106">The first part of this article shows how you use Q&A in dashboards in the Power BI service.</span></span> <span data-ttu-id="c671d-107">ส่วนที่สองแสดงสิ่งที่คุณสามารถทำได้ด้วยถามตอบ (Q&A) เมื่อสร้างรายงานในบริการ Power BI หรือไม่ก็ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="c671d-107">The second part shows what you can do with Q&A when creating reports in either the Power BI service or Power BI Desktop.</span></span> <span data-ttu-id="c671d-108">สำหรับพื้นหลังเพิ่มเติม ดูบทความ [ถามตอบ (Q&A) สำหรับผู้บริโภค](../consumer/end-user-q-and-a.md)</span><span class="sxs-lookup"><span data-stu-id="c671d-108">For more background, see the [Q&A for consumers](../consumer/end-user-q-and-a.md) article.</span></span> 

<span data-ttu-id="c671d-109">[Q&A ในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่ ](../consumer/mobile/mobile-apps-ios-qna.md)และ[ Q&A ที่มี Power BI Embedded](../developer/embedded/qanda.md) ครอบคลุมในบทความต่างหาก</span><span class="sxs-lookup"><span data-stu-id="c671d-109">[Q&A in the Power BI mobile apps](../consumer/mobile/mobile-apps-ios-qna.md) and [Q&A with Power BI Embedded](../developer/embedded/qanda.md) are covered in separate articles.</span></span> 

<span data-ttu-id="c671d-110">ระบบถามตอบ (Q&A) เป็นระบบแบบโต้ตอบ แถมยังสนุกด้วย</span><span class="sxs-lookup"><span data-stu-id="c671d-110">Q&A is interactive, even fun.</span></span> <span data-ttu-id="c671d-111">บ่อยครั้งที่คำถามหนึ่งนำไปสู่อีกคำถามหนึ่งเนื่องจากการแสดงผลข้อมูลด้วยภาพแสดงให้เห็นเส้นทางที่น่าสนใจในการติดตาม</span><span class="sxs-lookup"><span data-stu-id="c671d-111">Often, one question leads to others as the visualizations reveal interesting paths to pursue.</span></span> <span data-ttu-id="c671d-112">ดู Amanda สาธิตการใช้ถามตอบ เพื่อสร้างการแสดงภาพ เจาะลึกลงในวิชวลเหล่านั้น และปักหมุดวิชวลไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="c671d-112">Watch Amanda demonstrate using Q&A to create visualizations, dig into those visuals, and pin them to dashboards.</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/qMf7OLJfCz8?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>

## <a name="part-1-use-qa-on-a-dashboard-in-the-power-bi-service"></a><span data-ttu-id="c671d-113">ส่วนที่ 1: ใช้ Q&A บนแดชบอร์ดในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="c671d-113">Part 1: Use Q&A on a dashboard in the Power BI service</span></span>

<span data-ttu-id="c671d-114">ในบริการของ Power BI (app.powerbi.com) แดชบอร์ดประกอบด้วย ไทล์ที่ปักหมุดจากชุดข้อมูลหนึ่งหรือหลายชุด ดังนั้นคุณสามารถถามคำถามเกี่ยวกับข้อมูลที่มีอยู่ในชุดข้อมูลใดๆ เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="c671d-114">In the Power BI service (app.powerbi.com), a dashboard contains tiles pinned from one or more datasets, so you can ask questions about any of the data contained in any of those datasets.</span></span> <span data-ttu-id="c671d-115">เพื่อดูว่ารายงานและชุดข้อมูลใดถูกใช้ในการสร้างแดชบอร์ด เลือก **ดูรายการที่เกี่ยวข้อง** จากแถบเมนู</span><span class="sxs-lookup"><span data-stu-id="c671d-115">To see what reports and datasets were used to create the dashboard, select **View related** from the menu bar.</span></span>

![ดูรายงานและชุดข้อมูลที่เกี่ยวข้อง](media/power-bi-tutorial-q-and-a/power-bi-view-related.png)

<span data-ttu-id="c671d-117">กล่องคำถามของถามตอบ (Q&A) อยู่ที่มุมบนซ้ายของแดชบอร์ดคุณ และที่คุณพิมพ์คำถามของคุณโดยใช้ภาษาธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="c671d-117">The Q&A question box is located in the upper-left corner of your dashboard, where you type your question using natural language.</span></span> <span data-ttu-id="c671d-118">ไม่เห็นกล่องถามตอบ (Q&A) ใช่หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="c671d-118">Don't see the Q&A box?</span></span> <span data-ttu-id="c671d-119">โปรดดู [ข้อควรพิจารณาและการแก้ไขปัญหา](../consumer/end-user-q-and-a.md#considerations-and-troubleshooting) ในบทความ **ถามตอบ (Q&A) สำหรับผู้บริโภค**</span><span class="sxs-lookup"><span data-stu-id="c671d-119">See [Considerations and troubleshooting](../consumer/end-user-q-and-a.md#considerations-and-troubleshooting) in the **Q&A for consumers** article.</span></span>  <span data-ttu-id="c671d-120">ถามตอบ (Q&A) เข้าใจคำที่คุณพิมพ์เข้าไป และหาว่าที่ไหน (ชุดข้อมูลไหน) เพื่อค้นหาคำตอบ</span><span class="sxs-lookup"><span data-stu-id="c671d-120">Q&A recognizes the words you type and figures out where (in which dataset) to find the answer.</span></span> <span data-ttu-id="c671d-121">ถามตอบยังช่วยคุณสร้างคำถาม ด้วยการทำให้ข้อความสมบูรณ์โดยอัตโนมัติ การเปลี่ยนข้อความในคำถาม และการช่วยเหลืออื่น ๆ ทางข้อความหรือภาพ</span><span class="sxs-lookup"><span data-stu-id="c671d-121">Q&A also helps you form your question with auto-completion, restatement, and other textual and visual aids.</span></span>

![สกรีนช็อตแสดงแดชบอร์ด Power BI พร้อมตัวเลือกในการถามคำถามเกี่ยวกับข้อมูลของคุณ](media/power-bi-tutorial-q-and-a/powerbi-qna.png)

<span data-ttu-id="c671d-123">คำตอบของคำถามคุณ จะแสดงเป็นการแสดงภาพแบบโต้ตอบ และจะปรับปรุงตามเมื่อคุณปรับเปลี่ยนคำถาม</span><span class="sxs-lookup"><span data-stu-id="c671d-123">The answer to your question is displayed as an interactive visualization and updates as you modify the question.</span></span>

1. <span data-ttu-id="c671d-124">เปิดแดชบอร์ด แล้ววางเคอร์เซอร์ของคุณในกล่องคำถาม</span><span class="sxs-lookup"><span data-stu-id="c671d-124">Open a dashboard and place your cursor in the question box.</span></span> <span data-ttu-id="c671d-125">ในมุมขวาบน ให้เลือก **ประสบการณ์การใช้งานถามตอบ (Q&A) แบบใหม่**</span><span class="sxs-lookup"><span data-stu-id="c671d-125">In the upper-right corner, select **New Q&A experience**.</span></span>

    ![ประสบการณ์การใช้งานถามตอบ (Q&A) แบบใหม่ของ Power BI](media/power-bi-tutorial-q-and-a/power-bi-qna-new-experience.png)

1. <span data-ttu-id="c671d-127">ถึงแม้ว่าคุณยังไม่เริ่มพิมพ์ ถามตอบจะแสดงหน้าจอใหม่ ด้วยคำแนะนำเพื่อช่วยคุณสร้างคำถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="c671d-127">Even before you start typing, Q&A displays a new screen with suggestions to help you form your question.</span></span> <span data-ttu-id="c671d-128">คุณเห็นวลีและคำถามทั้งหมดที่มีชื่อของตารางในชุดข้อมูลเบื้องต้น และอาจเห็นรายการคำถามทั้งหมด ถ้าเจ้าของชุดข้อมูลสร้าง[คำถามที่น่าสนใจ](service-q-and-a-create-featured-questions.md)ไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c671d-128">You see phrases and complete questions containing the names of the tables in the underlying datasets and may even see complete questions listed if the dataset owner has created [featured questions](service-q-and-a-create-featured-questions.md),</span></span>

   ![คำถามที่แนะนำจากถามตอบ (Q&A)](media/power-bi-tutorial-q-and-a/power-bi-qna-suggested-questions.png)

   <span data-ttu-id="c671d-130">คุณสามารถเลือกหนึ่งในคำถามเหล่านี้เป็นจุดเริ่มต้น และปรับแต่งคำถามต่อไปเพื่อค้นหาคำตอบเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="c671d-130">You can choose one of these questions as a starting point and continue to refine the question to find a specific answer.</span></span> <span data-ttu-id="c671d-131">หรือใช้ชื่อตารางเพื่อช่วยคุณในการใช้ถ้อยคำสำหรับการตั้งคำถามใหม่</span><span class="sxs-lookup"><span data-stu-id="c671d-131">Or use a table name to help you word a new question.</span></span>

2. <span data-ttu-id="c671d-132">เลือกจากรายการคำถาม หรือเริ่มพิมพ์คำถามของคุณเอง แล้วเลือกจากคำแนะนำในรายการดรอปดาวน์</span><span class="sxs-lookup"><span data-stu-id="c671d-132">Select from the list of questions, or begin typing your own question and select from the dropdown suggestions.</span></span>

   ![เลือกคำถามจากรายการ](media/power-bi-tutorial-q-and-a/power-bi-qna-select-a-question-how-many-stores.png)

3. <span data-ttu-id="c671d-134">ในขณะที่คุณพิมพ์คำถาม ถามตอบ (Q&A) จะเลือกการแสดงผลข้อมูลด้วยภาพที่ดีที่สุดเพื่อแสดงคำถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="c671d-134">As you type a question, Q&A picks the best visualization to display your answer.</span></span>

   ![จำนวนร้านค้าตามรัฐจากถามตอบ (Q&A)](media/power-bi-tutorial-q-and-a/power-bi-qna-how-many-stores-by-state.png)

4. <span data-ttu-id="c671d-136">การแสดงผลข้อมูลด้วยภาพจะเปลี่ยนแปลงแบบไดนามิกเมื่อคุณปรับเปลี่ยนคำถาม</span><span class="sxs-lookup"><span data-stu-id="c671d-136">The visualization changes dynamically as you modify the question.</span></span>

   ![จำนวนร้านค้าตามรัฐเป็นแผนภูมิแท่งจากถามตอบ (Q&A)](media/power-bi-tutorial-q-and-a/power-bi-qna-stores-by-state-bar-chart.png)

1. <span data-ttu-id="c671d-138">เมื่อคุณพิมพ์คำถาม Power BI จะค้นหาคำตอบที่ดีที่สุด โดยใช้ชุดข้อมูลใด ๆ ที่มีไทล์อยู่บนแดชบอร์ดนั้น</span><span class="sxs-lookup"><span data-stu-id="c671d-138">When you type a question, Power BI looks for the best answer using any dataset that has a tile on that dashboard.</span></span>  <span data-ttu-id="c671d-139">ถ้าไทล์ทั้งหมดมาจาก *ชุดข้อมูล A* คำตอบของคุณจะมาจาก *ชุดข้อมูล A*</span><span class="sxs-lookup"><span data-stu-id="c671d-139">If all the tiles are from *datasetA*, then your answer will come from *datasetA*.</span></span>  <span data-ttu-id="c671d-140">ถ้ามีไทล์จากทั้ง *ชุดข้อมูล A* และ *ชุดข้อมูล B* ถามตอบ (Q&A) จะค้นหาคำตอบที่ดีที่สุดจากชุดข้อมูลทั้ง 2 นั้น</span><span class="sxs-lookup"><span data-stu-id="c671d-140">If there are tiles from *datasetA* and *datasetB*, then Q&A searches for the best answer from those 2 datasets.</span></span>

   > [!TIP]
   > <span data-ttu-id="c671d-141">ดังนั้นโปรดระวัง ถ้าคุณมีไทล์หนึ่งจาก *ชุดข้อมูล A* และคุณเอาออกจากแดชบอร์ดของคุณ ถามตอบจะไม่สามารถเข้าถึง *ชุดข้อมูล A* ได้อีก</span><span class="sxs-lookup"><span data-stu-id="c671d-141">So be careful, if you only have one tile from *datasetA* and you remove it from your dashboard, Q&A will no longer have access to *datasetA*.</span></span>
   >

5. <span data-ttu-id="c671d-142">เมื่อคุณพอใจกับผลลัพธ์ ให้ปักหมุดการแสดงผลข้อมูลด้วยภาพไปยังแดชบอร์ด โดยการเลือกไอคอนรูปเข็มหมุดในมุมบนขวา</span><span class="sxs-lookup"><span data-stu-id="c671d-142">When you're happy with the result, pin the visualization to a dashboard by selecting the pin icon in the top right corner.</span></span> <span data-ttu-id="c671d-143">ถ้าแดชบอร์ดถูกแชร์ให้กับคุณ หรือเป็นส่วนหนึ่งของแอป คุณจะไม่สามารถปักหมุดได้</span><span class="sxs-lookup"><span data-stu-id="c671d-143">If the dashboard has been shared with you, or is part of an app, you won't be able to pin.</span></span>

   ![ถามตอบ (Q&A) ปักหมุดวิชวล](media/power-bi-tutorial-q-and-a/power-bi-qna-pin-visual.png)

## <a name="part-2-use-qa-in-a-report-in-power-bi-service-or-power-bi-desktop"></a><span data-ttu-id="c671d-145">ส่วนที่ 2: ใช้ Q&A ในรายงาน ในบริการของ Power BI หรือ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="c671d-145">Part 2: Use Q&A in a report in Power BI service or Power BI Desktop</span></span>

<span data-ttu-id="c671d-146">ใช้ถามตอบ เพื่อสำรวจชุดข้อมูลของคุณ และเพิ่มการแสดงภาพไปยังรายงาน และแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="c671d-146">Use Q&A to explore your dataset and to add visualizations to the report and to dashboards.</span></span> <span data-ttu-id="c671d-147">รายงานจะมาจากชุดข้อมูลเดียว และอาจเป็นรายงานเปล่า หรือประกอบด้วยหน้าต่าง ๆ ที่เต็มไปด้วยการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="c671d-147">A report is based on a single dataset and may be completely blank or contain pages full of visualizations.</span></span> <span data-ttu-id="c671d-148">แต่เพียงเพราะว่ารายงานว่างเปล่า ไม่ได้หมายความว่าไม่มีข้อมูลใด ๆ ที่คุณสามารถสำรวจได้ - ชุดข้อมูลเชื่อมโยงกับรายงาน และกำลังรอให้คุณสำรวจ และสร้างการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="c671d-148">But just because a report is blank, doesn't mean there isn't any data for you to explore -- the dataset is linked to the report and is waiting for you to explore and create visualizations.</span></span>  <span data-ttu-id="c671d-149">เพื่อดูว่าชุดข้อมูลไหนใช้สร้างรายงาน เปิดรายงานในมุมมองการอ่านในบริการของ Power BI แล้วเลือก **ดูรายการที่เกี่ยวข้อง** จากแถบเมนู</span><span class="sxs-lookup"><span data-stu-id="c671d-149">To see which dataset is being used to create a report, open the report in Power BI service Reading view and select **View related** from the menubar.</span></span>

![ดูชุดข้อมูลที่เกี่ยวข้อง](media/power-bi-tutorial-q-and-a/power-bi-view-related.png)

<span data-ttu-id="c671d-151">หากต้องการใช้ถามตอบ (Q&A) ในรายงาน คุณต้องมีสิทธิ์ในการแก้ไขสำหรับ รายงานและชุดข้อมูลพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="c671d-151">To use Q&A in reports, you must have edit permissions for the report and underlying dataset.</span></span> <span data-ttu-id="c671d-152">ในบทความ [ถามตอบ (Q&A) สำหรับผู้บริโภค](../consumer/end-user-q-and-a.md) เราอ้างถึงสิ่งนี้ว่าเป็นสถานการณ์จำลองของ *ผู้สร้าง*</span><span class="sxs-lookup"><span data-stu-id="c671d-152">In the [Q&A for consumers](../consumer/end-user-q-and-a.md) article, we refer to this as a *creator* scenario.</span></span> <span data-ttu-id="c671d-153">หากคุณ *กำลังใช้งาน* รายงานที่แบ่งปันกับคุณแทน ถามตอบ (Q&A) จะไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="c671d-153">If instead you're *consuming* a report that has been shared with you, Q&A isn't available.</span></span>

1. <span data-ttu-id="c671d-154">เปิดรายงานในมุมมองการแก้ไข (บริการ Power BI) หรือมุมมองรายงาน (Power BI Desktop) และเลือก **ถามคำถาม** จากแถบเมนู</span><span class="sxs-lookup"><span data-stu-id="c671d-154">Open a report in Editing view (Power BI service) or Report view (Power BI Desktop) and select **Ask a question** from the menu bar.</span></span>

    <span data-ttu-id="c671d-155">**Power BI Desktop**  </span><span class="sxs-lookup"><span data-stu-id="c671d-155">**Power BI Desktop**  </span></span>  
    <span data-ttu-id="c671d-156">![เลือกถามคำถามใน Power BI Desktop](media/power-bi-tutorial-q-and-a/power-bi-desktop-question.png)</span><span class="sxs-lookup"><span data-stu-id="c671d-156">![Select Ask A Question in Power BI Desktop](media/power-bi-tutorial-q-and-a/power-bi-desktop-question.png)</span></span>

    <span data-ttu-id="c671d-157">**บริการ**  </span><span class="sxs-lookup"><span data-stu-id="c671d-157">**Service**  </span></span>  
    <span data-ttu-id="c671d-158">![เลือกถามคำถามในบริการ Power BI](media/power-bi-tutorial-q-and-a/power-bi-service.png)</span><span class="sxs-lookup"><span data-stu-id="c671d-158">![Select Ask a question in the Power BI service](media/power-bi-tutorial-q-and-a/power-bi-service.png)</span></span>

2. <span data-ttu-id="c671d-159">กล่องคำถามถามตอบ จะแสดงบนพื้นที่รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="c671d-159">A Q&A question box displays on your report canvas.</span></span> <span data-ttu-id="c671d-160">ในตัวอย่างด้านล่าง กล่องคำถามแสดงอยู่เหนือการแสดงภาพอื่น</span><span class="sxs-lookup"><span data-stu-id="c671d-160">In the example below, the question box displays on top of another visualization.</span></span> <span data-ttu-id="c671d-161">ซึ่งยอมรับได้ แต่จะเป็นการดีกว่าถ้าเพิ่มหน้าเปล่าลงในรายงานก่อนที่ถามคำถาม</span><span class="sxs-lookup"><span data-stu-id="c671d-161">This is fine, but it might be better to add a blank page to the report before asking a question.</span></span>

    ![สกรีนช็อตแสดงพื้นที่ทำงานพร้อมกล่องคำถาม Q&A บนการแสดงผลข้อมูลด้วยภาพ](media/power-bi-tutorial-q-and-a/power-bi-ask-question.png)

3. <span data-ttu-id="c671d-163">วางเคอร์เซอร์ของคุณในกล่องคำถาม</span><span class="sxs-lookup"><span data-stu-id="c671d-163">Place your cursor in the question box.</span></span> <span data-ttu-id="c671d-164">ขณะที่คุณพิมพ์ ถามตอบจะแสดงคำแนะนำ เพื่อช่วยคุณสร้างคำถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="c671d-164">As you type, Q&A displays suggestions to help you form your question.</span></span>

   ![พิมพ์ในกล่องคำถามถามตอบ (Q&A)](media/power-bi-tutorial-q-and-a/power-bi-q-and-a-suggestions.png)

4. <span data-ttu-id="c671d-166">ขณะที่คุณพิมพ์คำถาม ถามตอบจะเลือก[การแสดงภาพ](../visuals/power-bi-visualization-types-for-reports-and-q-and-a.md)ที่ดีที่สุด เพื่อแสดงคำตอบของคุณ และการแสดงภาพจะเปลี่ยนตาม ขณะที่คุณปรับเปลี่ยนคำถาม</span><span class="sxs-lookup"><span data-stu-id="c671d-166">As you type a question, Q&A picks the best [visualization ](../visuals/power-bi-visualization-types-for-reports-and-q-and-a.md)to display your answer; and the visualization changes dynamically as you modify the question.</span></span>

   ![ถามตอบ (Q&A) สร้างการแสดงผลข้อมูลด้วยภาพ](media/power-bi-tutorial-q-and-a/power-bi-q-and-a-visual.png)

5. <span data-ttu-id="c671d-168">เมื่อคุณมีการแสดงภาพที่คุณชอบ เลือก ENTER</span><span class="sxs-lookup"><span data-stu-id="c671d-168">When you have the visualization you like, select ENTER.</span></span> <span data-ttu-id="c671d-169">เพื่อบันทึกการแสดงภาพลงรายงาน เลือก **ไฟล์ > บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c671d-169">To save the visualization with the report, select **File > Save**.</span></span>

6. <span data-ttu-id="c671d-170">โต้ตอบกับการแสดงภาพใหม่</span><span class="sxs-lookup"><span data-stu-id="c671d-170">Interact with the new visualization.</span></span> <span data-ttu-id="c671d-171">ไม่สำคัญว่าคุณได้สร้างการแสดงภาพด้วยวิธีไหน -- ทั้งหมดจะมีการโต้ตอบ จัดรูปแบบ และคุณลักษณะที่เหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="c671d-171">It doesn't matter how you created the visualization -- all the same interactivity, formatting, and features are available.</span></span>

   ![โต้ตอบกับการแสดงผลข้อมูลด้วยภาพ](media/power-bi-tutorial-q-and-a/power-bi-q-and-a-ellipses.png)

   <span data-ttu-id="c671d-173">ถ้าคุณได้สร้างการแสดงภาพในบริการของ Power BI คุณสามารถ[ปักหมุดไปยังแดชบอร์ด](service-dashboard-pin-tile-from-q-and-a.md)ได้</span><span class="sxs-lookup"><span data-stu-id="c671d-173">If you've created the visualization in Power BI service, you can even [pin it to a dashboard](service-dashboard-pin-tile-from-q-and-a.md).</span></span>

## <a name="tell-qa-which-visualization-to-use"></a><span data-ttu-id="c671d-174">บอกการถามตอบว่าต้องใช้การแสดงภาพแบบใด</span><span class="sxs-lookup"><span data-stu-id="c671d-174">Tell Q&A which visualization to use</span></span>
<span data-ttu-id="c671d-175">ด้วยถามตอบ ไม่เพียงแต่คุณสามารถขอให้ข้อมูลคุณพูดออกมาด้วยตัวเอง คุณสามารถบอกวิธีที่ Power BI จะแสดงคำตอบได้</span><span class="sxs-lookup"><span data-stu-id="c671d-175">With Q&A, not only can you ask your data to speak for itself, you can tell Power BI how to display the answer.</span></span> <span data-ttu-id="c671d-176">เพียงแค่เพิ่ม "as a <visualization type>" ตรงท้ายคำถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="c671d-176">Just add "as a <visualization type>" to the end of your question.</span></span>  <span data-ttu-id="c671d-177">ตัวอย่างเช่น "show inventory volume by plant as a map" และ "show total inventory as a card"</span><span class="sxs-lookup"><span data-stu-id="c671d-177">For example, "show inventory volume by plant as a map" and "show total inventory as a card".</span></span>  <span data-ttu-id="c671d-178">ลองทำด้วยตัวเองดู</span><span class="sxs-lookup"><span data-stu-id="c671d-178">Try it for yourself.</span></span>

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="c671d-179">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="c671d-179">Considerations and troubleshooting</span></span>
- <span data-ttu-id="c671d-180">ถ้าคุณได้เชื่อมต่อชุดข้อมูลโดยใช้การเชื่อมต่อสด หรือใช้เกตเวย์ ถามตอบจะต้อง[เปิดใช้งานสำหรับชุดข้อมูลนั้น](service-q-and-a-direct-query.md)</span><span class="sxs-lookup"><span data-stu-id="c671d-180">If you've connected to a dataset using a live connection or gateway, Q&A needs to be [enabled for that dataset](service-q-and-a-direct-query.md).</span></span>

- <span data-ttu-id="c671d-181">คุณได้เปิดรายงาน และไม่เห็นตัวเลือกการถามตอบ</span><span class="sxs-lookup"><span data-stu-id="c671d-181">You've opened a report and don't see the Q&A option.</span></span> <span data-ttu-id="c671d-182">ถ้าคุณกำลังใช้บริการของ Power BI ตรวจสอบทำให้แน่ใจว่า รายงานเปิดในมุมมองการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="c671d-182">If you're using Power BI service, make sure the report is open in Editing view.</span></span> <span data-ttu-id="c671d-183">ถ้าคุณไม่สามารถเปิดรายงานในมุมมองการแก้ไข นั่นหมายความว่า คุณไม่มีสิทธิ์ในการแก้ไขรายงานนั้น และคุณไม่สามารถใช้ถามตอบ (Q&A) กับรายงานเฉพาะนั้นได้</span><span class="sxs-lookup"><span data-stu-id="c671d-183">If you can't open Editing view it means you don't have edit permissions for that report and you can use Q&A with that specific report.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c671d-184">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c671d-184">Next steps</span></span>

- [<span data-ttu-id="c671d-185">การถามตอบสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c671d-185">Q&A for consumers</span></span>](../consumer/end-user-q-and-a.md)   
- [<span data-ttu-id="c671d-186">เคล็ดลับการถามคำถามในถามตอบ (Q&A)</span><span class="sxs-lookup"><span data-stu-id="c671d-186">Tips for asking questions in Q&A</span></span>](../consumer/end-user-q-and-a-tips.md)   
- [<span data-ttu-id="c671d-187">เตรียมเวิร์กบุ๊กสำหรับการถามตอบ</span><span class="sxs-lookup"><span data-stu-id="c671d-187">Prepare a workbook for Q&A</span></span>](service-prepare-data-for-q-and-a.md)  
- [<span data-ttu-id="c671d-188">เตรียมชุดข้อมูลภายในองค์กรสำหรับถามตอบ (Q&A)</span><span class="sxs-lookup"><span data-stu-id="c671d-188">Prepare an on-premises dataset for Q&A</span></span>](service-q-and-a-direct-query.md)   
- [<span data-ttu-id="c671d-189">ปักหมุดไทล์ไปยังแดชบอร์ดจากถามตอบ (Q&A)</span><span class="sxs-lookup"><span data-stu-id="c671d-189">Pin a tile to the dashboard from Q&A</span></span>](service-dashboard-pin-tile-from-q-and-a.md)
