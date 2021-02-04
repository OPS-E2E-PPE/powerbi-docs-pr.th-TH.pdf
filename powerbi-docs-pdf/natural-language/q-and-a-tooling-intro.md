---
title: แนะนำการใช้เครื่องมือระบบถามตอบ เพื่อสอนระบบถามของ Power BI (ตัวอย่าง)
description: บทนำเกี่ยวกับการใช้เครื่องมือถามตอบของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: conceptual
ms.date: 08/31/2020
ms.openlocfilehash: e83a823908a89a300f9bbe97cfaaef19ede77fc8
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96393772"
---
# <a name="intro-to-qa-tooling-to-train-power-bi-qa-preview"></a><span data-ttu-id="e6e9c-103">แนะนำการใช้เครื่องมือระบบถามตอบ เพื่อสอนระบบถามของ Power BI (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="e6e9c-103">Intro to Q&A tooling to train Power BI Q&A (preview)</span></span>

<span data-ttu-id="e6e9c-104">คุณสามารถปรับปรุงประสบการณ์การใช้งานภาษาธรรมชาติสำหรับผู้ใช้ของคุณได้ด้วย *การใช้เครื่องมือ* ถามตอบของ Power BI</span><span class="sxs-lookup"><span data-stu-id="e6e9c-104">With Power BI Q&A *tooling*, you can improve the natural language experience for your users.</span></span> <span data-ttu-id="e6e9c-105">ในฐานะผู้ออกแบบหรือผู้ดูแลระบบ คุณโต้ตอบกับกลไกจัดการภาษาธรรมชาติและทำการปรับปรุงให้ดีขึ้นในสามส่วน:</span><span class="sxs-lookup"><span data-stu-id="e6e9c-105">As a designer or administrator, you interact with the natural language engine and make improvements in three areas:</span></span> 

- <span data-ttu-id="e6e9c-106">ตรวจสอบคำถามที่ผู้ใช้ของคุณถามเข้ามา</span><span class="sxs-lookup"><span data-stu-id="e6e9c-106">Review questions your users have asked.</span></span>
- <span data-ttu-id="e6e9c-107">สอนระบบถามตอบเพื่อให้เข้าใจคำถาม</span><span class="sxs-lookup"><span data-stu-id="e6e9c-107">Teach Q&A to understand questions.</span></span>
- <span data-ttu-id="e6e9c-108">จัดการคำศัพท์ที่คุณได้สอนระบบถามตอบ</span><span class="sxs-lookup"><span data-stu-id="e6e9c-108">Manage terms you've taught Q&A.</span></span>

<span data-ttu-id="e6e9c-109">นอกเหนือจากความสามารถในการใช้เครื่องมือเฉพาะเหล่านี้แล้ว แท็บ **การสร้างแบบจำลอง** ใน Power BI Desktop ยังมีตัวเลือกเพิ่มเติมอีก:</span><span class="sxs-lookup"><span data-stu-id="e6e9c-109">In addition to these dedicated tooling capabilities, the **Modeling** tab in Power BI Desktop offers more options:</span></span>  

- <span data-ttu-id="e6e9c-110">คำเหมือน</span><span class="sxs-lookup"><span data-stu-id="e6e9c-110">Synonyms</span></span>
- <span data-ttu-id="e6e9c-111">ป้ายชื่อแถว</span><span class="sxs-lookup"><span data-stu-id="e6e9c-111">Row labels</span></span>
- <span data-ttu-id="e6e9c-112">ซ่อนจากระบบถามตอบ</span><span class="sxs-lookup"><span data-stu-id="e6e9c-112">Hide from Q&A</span></span>
- <span data-ttu-id="e6e9c-113">การกำหนดค่าของรูปแบบภาษา (ขั้นสูง)</span><span class="sxs-lookup"><span data-stu-id="e6e9c-113">Configuring of the linguistic schema (advanced)</span></span>

## <a name="get-started-with-qa-tooling"></a><span data-ttu-id="e6e9c-114">เริ่มต้นด้วยการใช้เครื่องมือถามตอบ</span><span class="sxs-lookup"><span data-stu-id="e6e9c-114">Get started with Q&A tooling</span></span>

<span data-ttu-id="e6e9c-115">การใช้เครื่องมือถามตอบมีอยู่ใน Power BI Desktop เท่านั้น และขณะนี้รองรับเฉพาะโหมดการนำเข้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e6e9c-115">Q&A tooling is only available in Power BI Desktop, and currently only supports import mode.</span></span>

1. <span data-ttu-id="e6e9c-116">เปิด Power BI Desktop และใช้ระบบถามตอบเพื่อสร้างวิชวล</span><span class="sxs-lookup"><span data-stu-id="e6e9c-116">Open Power BI Desktop and use Q&A to create a visual.</span></span> 
2. <span data-ttu-id="e6e9c-117">ให้เลือกไอคอนรูปเฟืองจากมุมของวิชวล</span><span class="sxs-lookup"><span data-stu-id="e6e9c-117">From the corner of the visual, select the gear icon.</span></span> 

    ![ไอคอนรูปเฟืองของวิชวลระบบถามตอบ](media/q-and-a-tooling-intro/qna-visual-gear.png)

    <span data-ttu-id="e6e9c-119">หน้าเริ่มต้นใช้งานจะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="e6e9c-119">The Getting started page opens.</span></span>  

    ![เริ่มต้นใช้งานระบบถามตอบ](media/q-and-a-tooling-intro/qna-tooling-dialog.png)

### <a name="field-synonyms"></a><span data-ttu-id="e6e9c-121">คำเหมือนของเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e6e9c-121">Field Synonyms</span></span>

<span data-ttu-id="e6e9c-122">เลือก **คำเหมือนของเขตข้อมูล** เพื่อดูตารางและคอลัมน์ทั้งหมดที่เป็นของโมเดล</span><span class="sxs-lookup"><span data-stu-id="e6e9c-122">Select **Field Synonyms** to see all the tables and columns that belong to the model.</span></span> <span data-ttu-id="e6e9c-123">มุมมองนี้ช่วยให้คุณสามารถเพิ่มชื่อสำรองให้ตรงกับคอลัมน์เพื่อช่วยให้ผู้ใช้ทำงานได้ง่ายยิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="e6e9c-123">This view allows you to add alternative names to match the columns to help users.</span></span> <span data-ttu-id="e6e9c-124">คุณยังสามารถเลือกว่าจะซ่อนคอลัมน์หรือตารางจากคำถามและคำตอบหรือไม่ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="e6e9c-124">You can also choose whether or not a column or table should be hidden from Q&A.</span></span>

![หน้าแรกคำเหมือนของเขตข้อมูลคำถามและคำตอบ](media/q-and-a-tooling-intro/qna-tooling-field-synonyms-home.png)

<span data-ttu-id="e6e9c-126">คลิกที่ตารางใดตารางหนึ่งเพื่อขยายและคุณจะเห็นกล่องโต้ตอบที่คล้ายกับที่แสดงด้านล่างนี้</span><span class="sxs-lookup"><span data-stu-id="e6e9c-126">Click on one of the tables to expand and you will see a dialog similar to the one below.</span></span>

![คำเหมือนของเขตข้อมูลคำถามและคำตอบแบบขยาย](media/q-and-a-tooling-intro/qna-tooling-field-synonyms-expanded.png)

<span data-ttu-id="e6e9c-128">กล่องโต้ตอบจะแสดงคอลัมน์และตารางทั้งหมด รวมถึงคำและคำพ้องที่เกี่ยวข้องซึ่งผู้ใช้สามารถใช้ได้เมื่อถามคำถามต่อชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e6e9c-128">The dialog will show all the columns and tables and their respective terms/synonyms that users can use when asking questions against the dataset.</span></span> <span data-ttu-id="e6e9c-129">คุณสามารถดูคำทั้งหมดในที่เดียวได้อย่างรวดเร็ว และยังเพิ่มหรือลบคำออกจากหลาย ๆ คอลัมน์ได้</span><span class="sxs-lookup"><span data-stu-id="e6e9c-129">You can quickly see all the terms in one place and also add or remove terms for multiple columns.</span></span> 

- <span data-ttu-id="e6e9c-130">เพิ่มคำ - หากคุณมีเขตข้อมูลที่มีชื่อว่า ยอดขาย คุณสามารถเพิ่มคำว่า รายได้ เพื่อให้ผู้ใช้สามารถใช้คำดังกล่าวแทนที่จะต้องใช้คำว่า ยอดขาย ได้</span><span class="sxs-lookup"><span data-stu-id="e6e9c-130">Add terms - If you have a field called sales, you may decide to add a term called revenue so a user can use this word instead of being required to use the word sales.</span></span> <span data-ttu-id="e6e9c-131">คลิกเครื่องหมายบวกเพื่อเพิ่มคำใหม่อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="e6e9c-131">Click the add sign to quickly add a new term</span></span>

- <span data-ttu-id="e6e9c-132">รวมในคำถามและคำตอบ - ตัวเลือกนี้ใช้เมื่อไม่ต้องการแสดงคอลัมน์หรือตารางไว้ในคำถามและคำตอบ ซึ่งระบบจะไม่แสดงคอลัมน์หรือตารางและผลลัพธ์ของคอลัมน์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e6e9c-132">Include in Q&A - This option allows a column or table to be omitted from Q&A meaning it will not be shown nor a result can be displayed with this column.</span></span> <span data-ttu-id="e6e9c-133">กรณีที่คุณอาจไม่ต้องการรวมคอลัมน์ไว้ในผลการแสดงคือเมื่อต้องจัดการกับวันที่</span><span class="sxs-lookup"><span data-stu-id="e6e9c-133">A circumstance where you may decide to not include a column is when dealing with dates.</span></span> <span data-ttu-id="e6e9c-134">ถ้ามีเขตข้อมูลวันที่ หรือ Foreign keys เป็นจำนวนมาก คุณอาจต้องการลบข้อมูลทั้งหมดยกเว้นเขตข้อมูลวันที่เพื่อเก็บคอลัมน์วันที่ที่ถูกต้องไว้ใช้เมื่อผู้ใช้ถามคำถามที่เกี่ยวข้องกับวันที่</span><span class="sxs-lookup"><span data-stu-id="e6e9c-134">If there are numerous date fields, or foreign keys, you may decide to remove all but one of the date fields so the correct date column is picked when a user asks a date related question.</span></span>

- <span data-ttu-id="e6e9c-135">คำที่แนะนำ - คำถามและคำตอบจะแนะนำคำที่ได้รับจากโปรแกรมการแนะนำของเราเพื่อช่วยคุณเพิ่มคำ/คำเหมือนได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="e6e9c-135">Suggested Terms - Q&A will also recommend suggested terms retrieved from our suggestions engine to help you quickly add terms/synonyms.</span></span> <span data-ttu-id="e6e9c-136">ถ้าไม่มีการเพิ่มคำแนะนำเหล่านั้น ระบบจะยังคงทำงานอยู่แต่จะแสดงเส้นประสีส้มให้ผู้ใช้ทราบเพื่อแสดงว่าระบบคำถามและคำตอบคิดว่ามีคำตอบแต่ไม่แน่ใจ</span><span class="sxs-lookup"><span data-stu-id="e6e9c-136">If the suggestions are not added, They will still function but will give the user an orange dotted line indicating Q&A thinks it has an answer but is not sure.</span></span> <span data-ttu-id="e6e9c-137">ถ้าคำเหมือนที่แนะนำถูกต้อง ให้คลิกที่ไอคอน + เพื่อให้ระบบสามารถใช้คำดังกล่าวเป็นคำเหมือนได้</span><span class="sxs-lookup"><span data-stu-id="e6e9c-137">If the suggested synonym is correct, click the + icon so it can be used as a synonym.</span></span> <span data-ttu-id="e6e9c-138">ถ้าคำแนะนำไม่ถูกต้อง ให้คลิก x เพื่อลบคำดังแล่าวและสั่งให้ระบบไม่ใช้เป็นคำ/เหมือนและจะไม่ทำงานภายในระบบคำถามและคำตอบ</span><span class="sxs-lookup"><span data-stu-id="e6e9c-138">if the suggestion is incorrect, then click the x which will remove the term and ensure it will not be used as a term/synonym and will not function inside Q&A.</span></span> <span data-ttu-id="e6e9c-139">การแนะนำคำนั้นสนับสนุนโดยพจนานุกรม Office และบางส่วนยังมาจากการเปลี่ยนชื่อที่พบภายในรายงานด้วย</span><span class="sxs-lookup"><span data-stu-id="e6e9c-139">The suggestions are powered by Office Dictionary and also come from renames found inside a report</span></span>

### <a name="review-questions"></a><span data-ttu-id="e6e9c-140">ตรวจสอบคำถาม</span><span class="sxs-lookup"><span data-stu-id="e6e9c-140">Review questions</span></span>

<span data-ttu-id="e6e9c-141">เลือก **ตรวจสอบคำถาม** เพื่อดูรายการของชุดข้อมูลที่ใช้ในบริการ Power BI สำหรับผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="e6e9c-141">Select **Review questions** to see a list of datasets being used in the Power BI service for your tenant.</span></span> <span data-ttu-id="e6e9c-142">หน้า **ตรวจสอบคำถาม** ยังแสดงเจ้าของชุดข้อมูล พื้นที่ทำงาน และวันที่รีเฟรชครั้งล่าสุด</span><span class="sxs-lookup"><span data-stu-id="e6e9c-142">The **Review questions** page also displays the dataset owner, workspace, and last refreshed date.</span></span> <span data-ttu-id="e6e9c-143">จากที่นี่คุณสามารถเลือกชุดข้อมูล และดูว่าคำถามใดที่ผู้ใช้ถาม</span><span class="sxs-lookup"><span data-stu-id="e6e9c-143">From here you can select a dataset and see what questions users have been asking.</span></span> <span data-ttu-id="e6e9c-144">ข้อมูลยังแสดงให้เห็นถึงคำที่ไม่รู้จักอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="e6e9c-144">The data also shows words that were not recognized.</span></span> <span data-ttu-id="e6e9c-145">ข้อมูลทั้งหมดที่แสดงที่นี่เป็นช่วง 28 วันที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="e6e9c-145">All data shown here is for the last 28 days.</span></span>

![ตรวจสอบคำถามของระบบถามตอบ](media/q-and-a-tooling-intro/qna-tooling-review-questions.png)

### <a name="teach-qa"></a><span data-ttu-id="e6e9c-147">สอนเกี่ยวกับการ "ถามตอบ"</span><span class="sxs-lookup"><span data-stu-id="e6e9c-147">Teach Q&A</span></span>

<span data-ttu-id="e6e9c-148">ส่วน **การสอนระบบถามตอบ** ช่วยให้คุณสามารถสอนระบบถามตอบให้รู้จำคำศัพท์ได้</span><span class="sxs-lookup"><span data-stu-id="e6e9c-148">The **Teach Q&A** section allows you to train Q&A to recognize words.</span></span> <span data-ttu-id="e6e9c-149">ให้พิมพ์คำถามที่ประกอบด้วยคำศัพท์หนึ่งคำหรือหลายคำที่ระบบถามตอบยังไม่รู้จัก</span><span class="sxs-lookup"><span data-stu-id="e6e9c-149">To begin, type a question that contains a word or words that Q&A doesn't recognize.</span></span> <span data-ttu-id="e6e9c-150">ระบบถามตอบจะพร้อมท์ให้คุณทราบสำหรับคำจำกัดความของคำศัพท์นั้น</span><span class="sxs-lookup"><span data-stu-id="e6e9c-150">Q&A prompts you for the definition of that term.</span></span> <span data-ttu-id="e6e9c-151">ให้ป้อนตัวกรองหรือชื่อเขตข้อมูลที่สอดคล้องกับคำที่แสดง</span><span class="sxs-lookup"><span data-stu-id="e6e9c-151">Enter either a filter or a field name that corresponds to what that word represents.</span></span> <span data-ttu-id="e6e9c-152">จากนั้นระบบถามตอบจะแปลคำถามเดิมซ้ำอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="e6e9c-152">Q&A then reinterprets the original question.</span></span> <span data-ttu-id="e6e9c-153">ถ้าคุณพอใจกับผลลัพธ์ คุณสามารถบันทึกการป้อนข้อมูลของคุณได้</span><span class="sxs-lookup"><span data-stu-id="e6e9c-153">If you're happy with the results, you can save your input.</span></span> <span data-ttu-id="e6e9c-154">หากต้องการเรียนรู้เพิ่มเติม โปรดดู [การสอนระบบถามตอบ](q-and-a-tooling-teach-q-and-a.md)</span><span class="sxs-lookup"><span data-stu-id="e6e9c-154">To learn more, see [Teach Q&A](q-and-a-tooling-teach-q-and-a.md)</span></span>

![ตัวอย่างคำพ้องความหมายสำหรับการสอนระบบถามตอบ](media/q-and-a-tooling-intro/qna-tooling-teach-fixpreview.png)

### <a name="manage-terms"></a><span data-ttu-id="e6e9c-156">จัดการคำศัพท์</span><span class="sxs-lookup"><span data-stu-id="e6e9c-156">Manage terms</span></span>

<span data-ttu-id="e6e9c-157">สิ่งใดก็ตามที่คุณบันทึกจากส่วนการสอนระบบถามตอบจะปรากฏที่นี่ ดังนั้นคุณสามารถตรวจสอบหรือลบคำศัพท์ที่คุณกำหนดไว้ได้</span><span class="sxs-lookup"><span data-stu-id="e6e9c-157">Anything you've saved from the Teach Q&A section shows up here, so you can review or delete terms you've defined.</span></span> <span data-ttu-id="e6e9c-158">ในปัจจุบันคุณยังไม่สามารถแก้ไขคำจำกัดความที่มีอยู่ได้ ดังนั้นหากต้องการกำหนดคำศัพท์ใหม่ คุณต้องลบและสร้างคำศัพท์นั้นขึ้นใหม่อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="e6e9c-158">Currently you can't edit an existing definition, so to redefine a term you must delete and recreate that term.</span></span>

![จัดการคำศัพท์ของระบบถามตอบ](media/q-and-a-tooling-intro/qna-manage-terms.png)

### <a name="suggest-questions"></a><span data-ttu-id="e6e9c-160">แนะนำคำถาม</span><span class="sxs-lookup"><span data-stu-id="e6e9c-160">Suggest questions</span></span>

> [!NOTE]
> <span data-ttu-id="e6e9c-161">ระบบจะแสดงคำถามที่แนะนำสำหรับอินสแตนซ์ทั้งหมดของวิชวลระบบคำถามและคำตอบ</span><span class="sxs-lookup"><span data-stu-id="e6e9c-161">The suggested questions will show up for all instances of the Q&A visual.</span></span> <span data-ttu-id="e6e9c-162">ไม่สามารถสร้างชุดการแนะนำแบบแยกสำหรับวิชวลระบบคำถามและคำตอบแต่ละรายการได้</span><span class="sxs-lookup"><span data-stu-id="e6e9c-162">It isn't possible to create a separate set of suggestions for each Q&A visual.</span></span>
> 
> 

<span data-ttu-id="e6e9c-163">โดยไม่ต้องทำการตั้งค่าใด ๆ วิชวลการถามตอบจะแนะนำคำถามหลายคำถามเพื่อเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e6e9c-163">Without doing any setup, the Q&A visual will suggest several questions to get started with.</span></span> <span data-ttu-id="e6e9c-164">คำถามเหล่านี้จะถูกสร้างขึ้นโดยอัตโนมัติตามรูปแบบข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="e6e9c-164">These questions are automatically generated based on your data model.</span></span> <span data-ttu-id="e6e9c-165">ใน **แนะนำคำถาม** คุณสามารถเขียนทับคำถามที่สร้างขึ้นโดยอัตโนมัติด้วยคำถามของคุณเองได้</span><span class="sxs-lookup"><span data-stu-id="e6e9c-165">In **Suggest questions**, you can overwrite the auto-generated questions with your own questions.</span></span>

<span data-ttu-id="e6e9c-166">หากต้องการเริ่มต้น ให้พิมพ์คำถามที่คุณต้องการเพิ่มลงในกล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="e6e9c-166">To start, type the question you want to add in the text box.</span></span> <span data-ttu-id="e6e9c-167">ในส่วนการแสดงตัวอย่าง คุณจะเห็นว่าผลลัพธ์มีลักษณะอย่างไรในวิชวลการถามตอบ</span><span class="sxs-lookup"><span data-stu-id="e6e9c-167">In the preview section, you see what the result will look like in the Q&A visual.</span></span> 

:::image type="content" source="media/q-and-a-tooling-intro/power-bi-qna-suggest-questions.png" alt-text="แนะนำคำถามสำหรับการถามตอบ":::
 
<span data-ttu-id="e6e9c-169">เลือกปุ่ม **เพิ่ม** เพื่อเพิ่มคำถามนี้ไปยัง **คำถามที่แนะนำของคุณ**</span><span class="sxs-lookup"><span data-stu-id="e6e9c-169">Select the **Add** button to add this question to **Your suggested questions**.</span></span> <span data-ttu-id="e6e9c-170">คำถามเพิ่มเติมทุกข้อจะเพิ่มไปยังส่วนท้ายของรายการนี้</span><span class="sxs-lookup"><span data-stu-id="e6e9c-170">Every additional question is added to the end of this list.</span></span> <span data-ttu-id="e6e9c-171">คำถามจะปรากฏในวิชวลการถามตอบเหมือนกับลำดับที่ปรากฏในรายการนี้</span><span class="sxs-lookup"><span data-stu-id="e6e9c-171">The questions will show up in the Q&A visual in the same order as they do in this list.</span></span> 

:::image type="content" source="media/q-and-a-tooling-intro/power-bi-qna-save-suggest-questions.png" alt-text="บันทึกคำถามที่แนะนำ":::
 
<span data-ttu-id="e6e9c-173">ตรวจสอบให้แน่ใจว่าคุณได้เลือก **บันทึก** เพื่อแสดงรายการคำถามที่แนะนำของคุณในวิชวลการถามตอบ</span><span class="sxs-lookup"><span data-stu-id="e6e9c-173">Make sure to select **Save** to show your list of suggested questions in the Q&A visual.</span></span> 

## <a name="other-qa-settings"></a><span data-ttu-id="e6e9c-174">การตั้งค่าอื่น ๆ ของระบบถามตอบ</span><span class="sxs-lookup"><span data-stu-id="e6e9c-174">Other Q&A settings</span></span>

### <a name="set-a-row-label"></a><span data-ttu-id="e6e9c-175">ตั้งค่าป้ายชื่อแถว</span><span class="sxs-lookup"><span data-stu-id="e6e9c-175">Set a row label</span></span>

<span data-ttu-id="e6e9c-176">ป้ายชื่อแถวช่วยให้คุณสามารถกำหนดว่าคอลัมน์ (หรือ *เขตข้อมูล*) ใดระบุตัวตนแถวเดียวในตารางได้ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="e6e9c-176">A row label allows you to define which column (or *field*) best identifies a single row in a table.</span></span> <span data-ttu-id="e6e9c-177">ตัวอย่างเช่น สำหรับตารางที่เรียกว่า 'ลูกค้า' ป้ายชื่อแถวมักจะเป็น ' ชื่อที่แสดง'</span><span class="sxs-lookup"><span data-stu-id="e6e9c-177">For example, for a table called 'Customer', the row label is usually 'Display Name'.</span></span> <span data-ttu-id="e6e9c-178">การจัดให้มีเมตาดาต้าเพิ่มเติมนี้ช่วยให้ระบบถามตอบสามารถลงจุดข้อมูลวิชวลที่เป็นประโยชน์มากขึ้นเมื่อผู้ใช้พิมพ์ใน 'แสดงยอดขายตามลูกค้า'</span><span class="sxs-lookup"><span data-stu-id="e6e9c-178">Providing this extra metadata allows Q&A to plot a more helpful visual when users type in 'Show me sales by customer'.</span></span> <span data-ttu-id="e6e9c-179">แทนที่จะใช้ข้อมูล 'ลูกค้า' แสดงในตาราง ก็สามารถใช้ 'ชื่อที่แสดง' แทน และแสดงเป็นแผนภูมิแท่งที่แสดงยอดขายของลูกค้าแต่ละราย</span><span class="sxs-lookup"><span data-stu-id="e6e9c-179">Instead of treating 'customer' as a table, it can instead use 'Display Name' and display a bar chart showing each customer's sales.</span></span> <span data-ttu-id="e6e9c-180">คุณสามารถตั้งค่ามุมมองการสร้างแบบจำลองของป้ายชื่อแถวได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e6e9c-180">You can only set the row label Modeling view.</span></span> 

1. <span data-ttu-id="e6e9c-181">ให้เลือกมุมมองการสร้างแบบจำลองใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e6e9c-181">In Power BI Desktop, select Modeling view.</span></span>

2. <span data-ttu-id="e6e9c-182">เลือกตารางเพื่อแสดงบานหน้าต่าง **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="e6e9c-182">Select a table to display the **Properties** pane.</span></span>

3. <span data-ttu-id="e6e9c-183">ในกล่อง **ป้ายชื่อแถว** ให้เลือกเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e6e9c-183">In the **Row label** box, select a field.</span></span>

## <a name="configure-the-linguistic-schema-advanced"></a><span data-ttu-id="e6e9c-184">กำหนดค่าของรูปแบบภาษา (ขั้นสูง)</span><span class="sxs-lookup"><span data-stu-id="e6e9c-184">Configure the linguistic schema (advanced)</span></span>

<span data-ttu-id="e6e9c-185">ใน Power BI คุณสามารถสอนและปรับปรุงประสิทธิภาพกลไกจัดการภาษาธรรมชาติภายในระบบถามตอบ รวมถึงการเปลี่ยนแปลง การให้คะแนน และการถ่วงน้ำหนักของผลลัพธ์ภาษาธรรมชาติพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="e6e9c-185">In Power BI, you can completely train and enhance the natural language engine inside Q&A, including changing the scoring and weighting of the underlying natural language results.</span></span> <span data-ttu-id="e6e9c-186">หากต้องการเรียนรู้วิธีการ โปรดดู [แก้ไขรูปแบบภาษาและเพิ่มการใช้ถ้อยคำของระบบถามตอบ](q-and-a-tooling-advanced.md)</span><span class="sxs-lookup"><span data-stu-id="e6e9c-186">To learn how, see [Edit Q&A linguistic schema and add phrasings](q-and-a-tooling-advanced.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="e6e9c-187">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="e6e9c-187">Next steps</span></span>

<span data-ttu-id="e6e9c-188">มีแนวปฏิบัติที่ดีที่สุดหลายประการสำหรับการพัฒนากลไกจัดการภาษาธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="e6e9c-188">There are a number of best practices for improving the natural language engine.</span></span> <span data-ttu-id="e6e9c-189">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [แนวทางปฏิบัติที่ดีที่สุดสำหรับการถามตอบ](q-and-a-best-practices.md)</span><span class="sxs-lookup"><span data-stu-id="e6e9c-189">For more information, [Q&A best practices](q-and-a-best-practices.md).</span></span>
