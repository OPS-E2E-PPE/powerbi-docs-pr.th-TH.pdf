---
title: ใช้ภาษาธรรมชาติเพื่อสำรวจข้อมูลของคุณโดยใช้ระบบถามตอบของ Power BI
description: วิธีใช้ถามตอบ Power BI เพื่อสำรวจข้อมูลของคุณและสร้างการแสดงผลข้อมูลด้วยภาพโดยใช้ภาษาธรรมชาติสำหรับคิวรี
author: mohaali
ms.author: mohaali
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: conceptual
ms.date: 07/01/2020
ms.openlocfilehash: 71a78fe6b1af909079ca0a187ddb14d643c4e576
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96416427"
---
# <a name="intro-to-power-bi-qa"></a><span data-ttu-id="b37ac-103">ข้อมูลเบื้องต้นเกี่ยวกับระบบถามตอบของ Power BI</span><span class="sxs-lookup"><span data-stu-id="b37ac-103">Intro to Power BI Q&A</span></span>

<span data-ttu-id="b37ac-104">บางครั้งวิธีที่เร็วที่สุดในการให้ได้คำตอบจากข้อมูลของคุณคือการค้นหาข้อมูลของคุณโดยใช้ภาษาธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="b37ac-104">Sometimes the fastest way to get an answer from your data is to perform a search over your data using natural language.</span></span> <span data-ttu-id="b37ac-105">คุณลักษณะระบบถามตอบใน Power BI ช่วยให้คุณสามารถสำรวจข้อมูลของคุณด้วยคำพูดของคุณเองโดยใช้ภาษาธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="b37ac-105">The Q&A feature in Power BI lets you explore your data in your own words using natural language.</span></span> <span data-ttu-id="b37ac-106">ระบบถามตอบเป็นระบบแบบโต้ตอบ แถมยังสนุกด้วย</span><span class="sxs-lookup"><span data-stu-id="b37ac-106">Q&A is interactive, even fun.</span></span> <span data-ttu-id="b37ac-107">บ่อยครั้งที่คำถามหนึ่งนำไปสู่อีกคำถามหนึ่งเนื่องจากการแสดงข้อมูลด้วยภาพแสดงให้เห็นเส้นทางที่น่าสนใจในการติดตาม</span><span class="sxs-lookup"><span data-stu-id="b37ac-107">Often, one question leads to others as the visualizations reveal interesting paths to pursue.</span></span> <span data-ttu-id="b37ac-108">การถามคำถามเป็นเพียงการเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b37ac-108">Asking the question is just the beginning.</span></span> <span data-ttu-id="b37ac-109">สำรวจข้อมูลของคุณ เพื่อปรับแต่งหรือขยายคำถามของคุณ ค้นพบข้อมูลใหม่ หรือให้ความสำคัญกับรายละเอียดและซูมออกเพื่อให้ได้มุมมองที่กว้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="b37ac-109">Travel through your data, refining or expanding your question, uncovering new information, zeroing in on details, or zooming out for a broader view.</span></span> <span data-ttu-id="b37ac-110">ประสบการณ์การใช้งานเป็นแบบโต้ตอบและรวดเร็วโดยใช้การจัดเก็บในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="b37ac-110">The experience is interactive and fast, powered by an in-memory storage.</span></span> 

<span data-ttu-id="b37ac-111">ระบบถามตอบของ Power BI เป็นระบบฟรีและพร้อมใช้งานสำหรับผู้ใช้ทุกคน</span><span class="sxs-lookup"><span data-stu-id="b37ac-111">Power BI Q&A is free and available to all users.</span></span> <span data-ttu-id="b37ac-112">ใน Power BI Desktop ผู้ออกแบบรายงานสามารถใช้ระบบถามตอบ เพื่อสำรวจข้อมูลและสร้างการแสดงผลข้อมูลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="b37ac-112">In Power BI Desktop, report designers can use Q&A to explore data and create visualizations.</span></span> <span data-ttu-id="b37ac-113">ในบริการของ Power BI ทุกคนสามารถสำรวจข้อมูลของพวกเขาได้ด้วยระบบถามตอบ</span><span class="sxs-lookup"><span data-stu-id="b37ac-113">In the Power BI service, everyone can explore their data with Q&A.</span></span> <span data-ttu-id="b37ac-114">แอปมือถือของเรารองรับ Q&A ด้วย ซึ่งมาพร้อมกับผู้ช่วย Q&A เสมือนใน iOS และวิชวล Q&A บนอุปกรณ์ Android</span><span class="sxs-lookup"><span data-stu-id="b37ac-114">Our mobile apps support Q&A too, with the Q&A virtual assistant in iOS and the Q&A visual on Android devices.</span></span> <span data-ttu-id="b37ac-115">ถ้าคุณมีสิทธิ์ในการแก้ไขแดชบอร์ดหรือรายงาน คุณยังสามารถปักหมุดผลลัพธ์ของระบบถามตอบได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="b37ac-115">If you have permission to edit a dashboard or report, you can also pin your Q&A results.</span></span>

## <a name="how-to-use-qa"></a><span data-ttu-id="b37ac-116">วิธีการใช้ระบบถามตอบ</span><span class="sxs-lookup"><span data-stu-id="b37ac-116">How to use Q&A</span></span>

![หน้าหลักของระบบถามตอบ](media/qna-visual.png)

<span data-ttu-id="b37ac-118">ถึงแม้ว่าคุณยังไม่เริ่มพิมพ์ ถามตอบจะแสดงหน้าจอใหม่ ด้วยคำแนะนำเพื่อช่วยคุณสร้างคำถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="b37ac-118">Even before you start typing, Q&A displays a new screen with suggestions to help you form your question.</span></span> <span data-ttu-id="b37ac-119">เริ่มจากคำถามที่แนะนำหนึ่งคำถามหรือไม่ก็พิมพ์คำถามของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="b37ac-119">Start either from one of the suggested questions or type your own questions.</span></span> <span data-ttu-id="b37ac-120">ระบบถามตอบรองรับคำถามที่หลากหลาย รวมถึงแต่ไม่จำกัดเพียง:</span><span class="sxs-lookup"><span data-stu-id="b37ac-120">Q&A supports a wide range of questions, including but not limited to:</span></span>

- <span data-ttu-id="b37ac-121">**ถามคำถามที่เป็นธรรมชาติ** ยอดขายใดมีรายได้สูงสุด?</span><span class="sxs-lookup"><span data-stu-id="b37ac-121">**Ask natural questions** Which sales has the highest revenue?</span></span>
- <span data-ttu-id="b37ac-122">**ใช้การกรองวันที่ที่เกี่ยวข้อง** แสดงยอดขายของฉันในปีที่แล้ว</span><span class="sxs-lookup"><span data-stu-id="b37ac-122">**Use relative date filtering** Show me sales in the last year</span></span>
- <span data-ttu-id="b37ac-123">**ส่งกลับเฉพาะผลิตภัณฑ์ยอดนิยม N รายการ** ผลิตภัณฑ์ 10 อันดับแรกตามยอดขาย</span><span class="sxs-lookup"><span data-stu-id="b37ac-123">**Return only the top N** Top 10 products by sales</span></span>
- <span data-ttu-id="b37ac-124">**ระบุตัวกรอง** แสดงยอดขายในสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="b37ac-124">**Provide a filter** Show me sales in the USA</span></span>
- <span data-ttu-id="b37ac-125">**ระบุเงื่อนไขที่ซับซ้อน** แสดงยอดขายที่หมวดหมู่ผลิตภัณฑ์คือหมวดหมู่ 1 หรือหมวดหมู่ 2</span><span class="sxs-lookup"><span data-stu-id="b37ac-125">**Provide complex conditions** Show me sales where product category is Category 1 or Category 2</span></span>
- <span data-ttu-id="b37ac-126">**ส่งกลับวิชวลที่เฉพาะเจาะจง** แสดงยอดขายตามผลิตภัณฑ์เป็นแผนภูมิวงกลม</span><span class="sxs-lookup"><span data-stu-id="b37ac-126">**Return a specific visual** Show me sales by product as pie chart</span></span>
- <span data-ttu-id="b37ac-127">**ใช้การรวมที่ซับซ้อน** แสดงมัธยฐานของยอดขายตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b37ac-127">**Use complex aggregations** Show me median sales by product</span></span>
- <span data-ttu-id="b37ac-128">**เรียงลำดับผลลัพธ์** แสดงรายชื่อประเทศที่มียอดขายสูงสุด 10 ประเทศโดยเรียงตามรหัสประเทศ</span><span class="sxs-lookup"><span data-stu-id="b37ac-128">**Sort results** Show me top 10 countries by sales ordered by country code</span></span>
- <span data-ttu-id="b37ac-129">**เปรียบเทียบข้อมูล** แสดงวันที่ตามยอดขายทั้งหมดเทียบกับต้นทุนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b37ac-129">**Compare data** Show me date by total sales vs total cost</span></span>
- <span data-ttu-id="b37ac-130">**ดูแนวโน้ม** แสดงยอดขายเมื่อเวลาผ่านไป</span><span class="sxs-lookup"><span data-stu-id="b37ac-130">**View trends** Show me sales over time</span></span>

### <a name="autocomplete"></a><span data-ttu-id="b37ac-131">เติมข้อความอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b37ac-131">Autocomplete</span></span>

<span data-ttu-id="b37ac-132">ในขณะที่คุณพิมพ์คำถามของคุณ ระบบถามตอบของ Power BI จะแสดงคำแนะนำที่เกี่ยวข้องและตามบริบทเพื่อช่วยให้คุณทำงานได้อย่างรวดเร็วด้วยภาษาธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="b37ac-132">As you type your question, Power BI Q&A shows relevant and contextual suggestions to help you quickly become productive with natural language.</span></span> <span data-ttu-id="b37ac-133">ขณะที่คุณพิมพ์ คุณจะได้รับผลป้อนกลับและผลลัพธ์ทันที</span><span class="sxs-lookup"><span data-stu-id="b37ac-133">As you type, you get immediate feedback and results.</span></span> <span data-ttu-id="b37ac-134">การใช้งานจะคล้ายกับการพิมพ์ในเครื่องมือค้นหา</span><span class="sxs-lookup"><span data-stu-id="b37ac-134">The experience is similar to typing in a search engine.</span></span>

![การกรอกข้อมูลวลีในระบบถามตอบให้สมบูรณ์](media/qna-suggestion-phrase-completion.png)

### <a name="redblueorange-underlines"></a><span data-ttu-id="b37ac-136">ขีดเส้นใต้สีแดง/สีน้ำเงิน/สีส้ม</span><span class="sxs-lookup"><span data-stu-id="b37ac-136">Red/Blue/Orange underlines</span></span>

<span data-ttu-id="b37ac-137">ระบบถามตอบจะแสดงคำพร้อมขีดเส้นใต้เพื่อช่วยให้คุณเห็นว่าคำใดที่ระบบเข้าใจหรือไม่รู้จัก</span><span class="sxs-lookup"><span data-stu-id="b37ac-137">Q&A shows words with underlines to help you see which words the system understood or didn't recognize.</span></span> <span data-ttu-id="b37ac-138">ขีดเส้นใต้สีน้ำเงินทึบแสดงว่าระบบได้จับคู่คำกับเขตข้อมูลหรือค่าในแบบจำลองข้อมูลเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="b37ac-138">A solid blue underline indicates that the system successfully matched the word to a field or value in the data-model.</span></span> <span data-ttu-id="b37ac-139">ตัวอย่างด้านล่างแสดงว่าระบบถามตอบรู้จักคำว่า *ยอดขายใน EU*</span><span class="sxs-lookup"><span data-stu-id="b37ac-139">The example below shows that Q&A recognized the word *EU Sales*.</span></span>

![ขีดเส้นใต้สีน้ำเงินในระบบถามตอบ](media/qna-blue-underline.png)

 <span data-ttu-id="b37ac-141">การขีดเส้นใต้สีส้มจะแสดงว่าคำดังกล่าว/เหล่านั้นจะถูกจัดประเภทเป็น *ความมั่นใจต่ำ*</span><span class="sxs-lookup"><span data-stu-id="b37ac-141">An orange underline indicates the word/words is categorized as *low confidence*.</span></span> <span data-ttu-id="b37ac-142">ถ้าคุณพิมพ์คำที่คลุมเครือหรือไม่ชัดเจน เขตข้อมูลจะถูกขีดเส้นใต้เป็นสีส้ม</span><span class="sxs-lookup"><span data-stu-id="b37ac-142">If you type a vague or ambiguous word, the field is underlined in orange.</span></span> <span data-ttu-id="b37ac-143">ตัวอย่างอาจเป็นคำว่า 'ยอดขาย'</span><span class="sxs-lookup"><span data-stu-id="b37ac-143">An example could be the word 'Sales'.</span></span> <span data-ttu-id="b37ac-144">อาจมีหลายเขตข้อมูลที่มีคำว่า 'ยอดขาย' ดังนั้นระบบจะใช้ขีดเส้นใต้สีส้มเพื่อพร้อมท์ให้คุณเลือกเขตข้อมูลที่คุณหมายถึง</span><span class="sxs-lookup"><span data-stu-id="b37ac-144">Multiple fields could contain the word 'Sales', so the system uses a orange underline to prompt you to choose the field you meant.</span></span> <span data-ttu-id="b37ac-145">อีกตัวอย่างหนึ่งของปัญหาประเภทความมั่นใจต่ำ อาจเกิดขึ้นได้ถ้าคุณพิมพ์คำว่า 'พื้นที่' แต่คอลัมน์ที่จับคู่ด้วยคือ 'ภูมิภาค'</span><span class="sxs-lookup"><span data-stu-id="b37ac-145">Another example of low confidence could be if you type the word 'area', but the column it matches is 'region'.</span></span> <span data-ttu-id="b37ac-146">คำถามและคำตอบของ Power BI จะจดจำคำที่มีความหมายเหมือนกัน ด้วยความร่วมมือกับ Bing และ Office และการตีความการเปลี่ยนชื่อจากภายในรายงานเพื่อใช้เป็นคำแนะนำที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="b37ac-146">Power BI Q&A recognizes words that mean the same thing, thanks to the integration with Bing and Office and also interpreting renames from within a report as potential suggestions.</span></span> <span data-ttu-id="b37ac-147">ระบบคำถามและคำตอบจะขีดเส้นใต้คำเป็นสีส้มเพื่อให้คุณรู้ว่าไม่ใช่การจับคู่โดยตรง</span><span class="sxs-lookup"><span data-stu-id="b37ac-147">Q&A underlines the word in orange so you know it's not a direct match.</span></span>

<span data-ttu-id="b37ac-148">เส้นใต้สีแดงหมายถึงระบบคำถามและคำตอบไม่รู้จักคำดังกล่าวเลย</span><span class="sxs-lookup"><span data-stu-id="b37ac-148">A red underline means Q&A didn't recognize the word at all.</span></span> <span data-ttu-id="b37ac-149">คุณอาจพบปัญหานี้ได้จากการใช้คำเฉพาะโดเมนที่ไม่เคยกล่าวถึงในที่ใดเลยบนข้อมูล หรือมีการตั้งชื่อเขตข้อมูลไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="b37ac-149">You could encounter this issue by using a domain-specific term that isn't mentioned anywhere in the data, or the data fields are incorrectly named.</span></span> <span data-ttu-id="b37ac-150">ตัวอย่างเช่น การใช้คำว่า 'ต้นทุน' แต่ทว่าคำนี้ไม่เคยปรากฎอยู่ในที่ใดเลยบนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b37ac-150">An example could be using the word 'Costs' though the word doesn't exist anywhere in the data.</span></span> <span data-ttu-id="b37ac-151">คำดังกล่าวนั้นอยู่ในพจนานุกรมภาษาอังกฤษ แต่รับคำถามและคำตอบจะทำเครื่องหมายคำนี้ด้วยการขีดเส้นใต้สีแดงเพื่อแสดงว่าไม่พบคำนี้ในข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b37ac-151">The word is in the English dictionary, but Q&A will mark this term with a red underline to indicate it didn't find this term with respect to the data.</span></span>

![ระบบถามตอบจะขีดเส้นใต้คำว่ายอดขายเป็นสีแดง](media/qna-red-underline-costs.png)

> [!NOTE]
> <span data-ttu-id="b37ac-153">คุณสามารถปรับแต่งสีของเส้นใต้เป็นสีน้ำเงิน/สีแดง/สีส้มได้ในบานหน้าต่าง **การจัดรูปแบบวิชวล** ของระบบคำถามและคำตอบ</span><span class="sxs-lookup"><span data-stu-id="b37ac-153">You can customize the blue/red/orange underline colors in the Q&A **Visual formatting** pane.</span></span> <span data-ttu-id="b37ac-154">นอกจากนี้ บทความ [การใช้เครื่องมือถามตอบ](q-and-a-tooling-teach-q-and-a.md) ยังอธิบายถึง *การสอนระบบถามตอบ* ซึ่งคุณใช้เพื่อกำหนดคำศัพท์ที่ระบบถามตอบไม่รู้จัก</span><span class="sxs-lookup"><span data-stu-id="b37ac-154">Also, the [Q&A tooling](q-and-a-tooling-teach-q-and-a.md) article explains *Teach Q&A*, which you use to define terms Q&A didn't recognize.</span></span>

### <a name="visualization-results"></a><span data-ttu-id="b37ac-155">ผลลัพธ์ของการแสดงผลข้อมูลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="b37ac-155">Visualization results</span></span>

<span data-ttu-id="b37ac-156">ในขณะที่คุณพิมพ์คำถามของคุณ ระบบถามตอบจะพยายามตีความและแสดงคำตอบทันที</span><span class="sxs-lookup"><span data-stu-id="b37ac-156">As you type your question, Q&A tries to instantly interpret and visualize the answer.</span></span> <span data-ttu-id="b37ac-157">เนื่องจากเป็นส่วนหนึ่งของการอัปเดตล่าสุด ตอนนี้ระบบถามตอบจะพยายามตีความคำถามและลงจุดเขตข้อมูลไปยังแกนที่ถูกต้องโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b37ac-157">As part of the latest updates, Q&A now tries to interpret the question and plot the fields automatically to the correct axis.</span></span> <span data-ttu-id="b37ac-158">ตัวอย่างเช่น ถ้าคุณพิมพ์ 'ยอดขายตามปี' ระบบถามตอบจะตรวจจับว่าปีนั้นเป็นเขตข้อมูลวันที่ และจะจัดลำดับความสำคัญให้เขตข้อมูลนี้อยู่ในแกน X เสมอ</span><span class="sxs-lookup"><span data-stu-id="b37ac-158">For example, if you type 'Sales by year', Q&A detects that year is a date field and always prioritizes placing this field on the X axis.</span></span> <span data-ttu-id="b37ac-159">ถ้าคุณต้องการเปลี่ยนชนิดการแสดงผลข้อมูลด้วยภาพ ให้พิมพ์ 'เป็น *ชนิดแผนภูมิ*' หลังคำถาม</span><span class="sxs-lookup"><span data-stu-id="b37ac-159">If you want to change the visualization type, type 'as *chart type*' after the question.</span></span> <span data-ttu-id="b37ac-160">ในขณะนี้ ระบบถามตอบรองรับการแสดงผลข้อมูลด้วยภาพชนิดต่าง ๆ ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b37ac-160">Q&A currently supports these types of visualizations:</span></span>

- <span data-ttu-id="b37ac-161">แผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="b37ac-161">Line chart</span></span>
- <span data-ttu-id="b37ac-162">แผนภูมิแท่ง</span><span class="sxs-lookup"><span data-stu-id="b37ac-162">Bar chart</span></span>
- <span data-ttu-id="b37ac-163">เมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="b37ac-163">Matrix</span></span>
- <span data-ttu-id="b37ac-164">ตาราง</span><span class="sxs-lookup"><span data-stu-id="b37ac-164">Table</span></span>
- <span data-ttu-id="b37ac-165">การ์ด</span><span class="sxs-lookup"><span data-stu-id="b37ac-165">Card</span></span>
- <span data-ttu-id="b37ac-166">พื้นที่</span><span class="sxs-lookup"><span data-stu-id="b37ac-166">Area</span></span>
- <span data-ttu-id="b37ac-167">Pie chart</span><span class="sxs-lookup"><span data-stu-id="b37ac-167">Pie chart</span></span>
- <span data-ttu-id="b37ac-168">แผนภูมิกระจาย/ฟอง</span><span class="sxs-lookup"><span data-stu-id="b37ac-168">Scatter/Bubble chart</span></span>
 
![ผลลัพธ์ของวิชวลระบบถามตอบ](media/qna-visual-results-date.png)

## <a name="add-qa-to-a-report"></a><span data-ttu-id="b37ac-170">เพิ่มระบบถามตอบไปยังรายงาน</span><span class="sxs-lookup"><span data-stu-id="b37ac-170">Add Q&A to a report</span></span>

<span data-ttu-id="b37ac-171">คุณสามารถเพิ่มระบบถามตอบไปยังรายงานใน Power BI Desktop หรือบริการของ Power BI ด้วยวิธีที่ต่างกันสองวิธี:</span><span class="sxs-lookup"><span data-stu-id="b37ac-171">You can add Q&A to a report in Power BI Desktop or the Power BI service in two different ways:</span></span>

- <span data-ttu-id="b37ac-172">เพิ่มวิชวลระบบถามตอบ</span><span class="sxs-lookup"><span data-stu-id="b37ac-172">Add a Q&A visual.</span></span>
- <span data-ttu-id="b37ac-173">เพิ่มปุ่มถามตอบ</span><span class="sxs-lookup"><span data-stu-id="b37ac-173">Add a Q&A button.</span></span>

<span data-ttu-id="b37ac-174">เมื่อต้องการเพิ่มวิชวลระบบถามตอบไปยังรายงาน ให้เลือกไอคอน **ถามตอบ** ใหม่ จากนั้นเลือกวิชวลระบบถามตอบใหม่ในบานหน้าต่างการแสดงผลข้อมูลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="b37ac-174">To add the Q&A visual to a report, select the new **Q&A** icon the select the new Q&A visual in the Visualization pane.</span></span> <span data-ttu-id="b37ac-175">อีกวิธีหนึ่งคือดับเบิลคลิกที่ใดก็ได้บนพื้นที่รายงานเพื่อแทรกวิชวลระบบถามตอบ</span><span class="sxs-lookup"><span data-stu-id="b37ac-175">Alternatively, double-click anywhere on the report canvas to insert the Q&A visual.</span></span>

![ไอคอนวิชวลระบบถามตอบ](media/qna-visual-icon.png)

<span data-ttu-id="b37ac-177">หากต้องการเพิ่มปุ่ม ให้เลือก **ปุ่ม** > **ถามตอบ** บนริบบอน **หน้าหลัก** ซึ่งคุณสามารถปรับแต่งรูปภาพปุ่มถามตอบได้อย่างสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b37ac-177">To add a button, on the **Home** ribbon, select **Buttons** > **Q&A** You can completely customize the Q&A button image.</span></span>

> [!NOTE]
> <span data-ttu-id="b37ac-178">เมื่อคุณเริ่มต้นระบบถามตอบจากปุ่ม ระบบจะยังคงใช้ระบบถามตอบ แบบเก่าอยู่</span><span class="sxs-lookup"><span data-stu-id="b37ac-178">When you start Q&A from the button, it still uses the old Q&A.</span></span> <span data-ttu-id="b37ac-179">Power BI ในเวอร์ชันที่เผยแพร่ออกมาทีหลังจะเปลี่ยนแปลงไปแล้ว</span><span class="sxs-lookup"><span data-stu-id="b37ac-179">Subsequent releases of Power BI will change that.</span></span>

## <a name="use-qa-for-dashboards"></a><span data-ttu-id="b37ac-180">ใช้ระบบถามตอบสำหรับแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="b37ac-180">Use Q&A for dashboards</span></span>

<span data-ttu-id="b37ac-181">ตามค่าเริ่มต้น คุณสามารถใช้งานระบบถามตอบได้จากด้านบนของแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="b37ac-181">By default, Q&A is available at the top of dashboards.</span></span> <span data-ttu-id="b37ac-182">หากต้องการใช้ระบบถามตอบ ให้พิมพ์ในกล่อง **ถามคำถามกับข้อมูลของคุณ**</span><span class="sxs-lookup"><span data-stu-id="b37ac-182">To use Q&A, type in the **Ask a question on your data** box.</span></span>

![แดชบอร์ดระบบถามตอบ](media/qna-dashboard.png)

## <a name="next-steps"></a><span data-ttu-id="b37ac-184">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="b37ac-184">Next steps</span></span>

<span data-ttu-id="b37ac-185">คุณสามารถผสานรวมภาษาธรรมชาติในรายงานของคุณได้หลายวิธี</span><span class="sxs-lookup"><span data-stu-id="b37ac-185">You can integrate natural language in your reports in a variety of ways.</span></span> <span data-ttu-id="b37ac-186">สำหรับข้อมูลเพิ่มเติม โปรดดูบทความเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="b37ac-186">For more information, see these articles:</span></span>

* [<span data-ttu-id="b37ac-187">วิชวลระบบถามตอบ</span><span class="sxs-lookup"><span data-stu-id="b37ac-187">Q&A visual</span></span>](../visuals/power-bi-visualization-q-and-a.md)
* [<span data-ttu-id="b37ac-188">แนวทางปฏิบัติที่ดีที่สุดของระบบถามตอบ</span><span class="sxs-lookup"><span data-stu-id="b37ac-188">Q&A best practices</span></span>](q-and-a-best-practices.md)
