---
title: การสอนระบบถามตอบเพื่อให้เข้าใจคำถามและคำศัพท์ในระบบถามตอบของ Power BI
description: วิธีการใช้ระบบถามตอบของ Power BI เพื่อสำรวจข้อมูลของคุณ
author: maggiesMSFT
ms.author: maggies
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 04/21/2020
LocalizationGroup: Ask questions of your datadefintion
ms.openlocfilehash: 5f7237102415f5917dab66f9689764c516d2672f
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96393634"
---
# <a name="teach-qa-to-understand-questions-and-terms-in-power-bi-qa"></a><span data-ttu-id="e27c2-103">การสอนระบบถามตอบเพื่อให้เข้าใจคำถามและคำศัพท์ในระบบถามตอบของ Power BI</span><span class="sxs-lookup"><span data-stu-id="e27c2-103">Teach Q&A to understand questions and terms in Power BI Q&A</span></span>

<span data-ttu-id="e27c2-104">ในส่วน **การสอนระบบถามตอบ** ของการตั้งค่าระบบถามตอบ คุณสามารถสอนให้ระบบถามตอบเข้าใจคำถามและคำศัพท์ภาษาธรรมชาติที่ยังไม่รู้จัก</span><span class="sxs-lookup"><span data-stu-id="e27c2-104">In the **Teach Q&A** section of Q&A setup, you train Q&A to understand natural-language questions and terms it hasn't recognized.</span></span> <span data-ttu-id="e27c2-105">หากต้องการเริ่มต้น ให้คุณส่งคำถามที่ประกอบด้วยคำเดี่ยวหรือหลายคำที่ระบบถามตอบยังไม่รู้จัก</span><span class="sxs-lookup"><span data-stu-id="e27c2-105">To begin, you submit a question that contains a word or words that Q&A didn't recognize.</span></span> <span data-ttu-id="e27c2-106">จากนั้นระบบถามตอบจะพร้อมท์ให้คุณกำหนดคำศัพท์นั้น</span><span class="sxs-lookup"><span data-stu-id="e27c2-106">Q&A then prompts you to define that term.</span></span> <span data-ttu-id="e27c2-107">คุณป้อนตัวกรองหรือชื่อเขตข้อมูลที่สอดคล้องกับคำที่แสดง</span><span class="sxs-lookup"><span data-stu-id="e27c2-107">You enter either a filter or a field name that corresponds to what that word represents.</span></span> <span data-ttu-id="e27c2-108">จากนั้นระบบถามตอบจะแปลคำถามเดิมซ้ำอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="e27c2-108">Q&A then reinterprets the original question.</span></span> <span data-ttu-id="e27c2-109">ถ้าคุณพอใจกับผลลัพธ์ ให้คุณบันทึกข้อมูลเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="e27c2-109">If you're happy with the results, you save them.</span></span>

> [!NOTE]
> <span data-ttu-id="e27c2-110">ฟังก์ชันการสอนระบบถามตอบจะรองรับโหมดการนำเข้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e27c2-110">The Teach Q&A functionality only supports import mode.</span></span> <span data-ttu-id="e27c2-111">นอกจากนี้ยังไม่รองรับการเชื่อมต่อไปยังแหล่งข้อมูลภายในองค์กรหรือ Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="e27c2-111">It also doesn't yet support connecting to an on-premises or Azure Analysis Services data source.</span></span> <span data-ttu-id="e27c2-112">ข้อจำกัดนี้ควรถูกลบออกจาก Power BI ในรุ่นที่ออกมาภายหลัง</span><span class="sxs-lookup"><span data-stu-id="e27c2-112">This limitation should be removed in subsequent releases of Power BI.</span></span>

## <a name="start-to-teach-qa"></a><span data-ttu-id="e27c2-113">เริ่มต้นสอนระบบถามตอบ</span><span class="sxs-lookup"><span data-stu-id="e27c2-113">Start to teach Q&A</span></span>

1. <span data-ttu-id="e27c2-114">ใน Power BI Desktop บนแถบริบบอน **การสร้างแบบจำลอง** ให้เลือก **การตั้งค่าระบบถามตอบ** > **การสอนระบบถามตอบ**</span><span class="sxs-lookup"><span data-stu-id="e27c2-114">In Power BI Desktop, on the **Modeling** ribbon, select **Q&A Setup** > **Teach Q&A**.</span></span>

    ![คำพ้องความหมายสำหรับการสอนระบบถามตอบเป็นสีแดง](media/q-and-a-tooling-teach-q-and-a/qna-tooling-teach-synonym-red.png)

2. <span data-ttu-id="e27c2-116">พิมพ์ประโยคด้วยคำที่ระบบถามตอบไม่เข้าใจ และเลือก **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="e27c2-116">Type a sentence with a term Q&A doesn't recognize and select **Submit**.</span></span>

3. <span data-ttu-id="e27c2-117">เลือกคำที่ขีดเส้นใต้สีแดง</span><span class="sxs-lookup"><span data-stu-id="e27c2-117">Select the red-underlined word.</span></span> 

    <span data-ttu-id="e27c2-118">ระบบถามตอบจะนำเสนอข้อเสนอแนะและพร้อมท์ให้คุณป้อนคำจำกัดความที่ถูกต้องของคำศัพท์</span><span class="sxs-lookup"><span data-stu-id="e27c2-118">Q&A offers suggestions and prompts you to provide the correct definition of the term.</span></span> 
    
3. <span data-ttu-id="e27c2-119">ภายใต้ **กำหนดคำศัพท์ที่ระบบถามตอบไม่เข้าใจ** ให้ระบุคำจำกัดความ</span><span class="sxs-lookup"><span data-stu-id="e27c2-119">Under **Define the terms Q&A didn't understand**, provide a definition.</span></span>

    ![ตัวอย่างคำพ้องความหมายสำหรับการสอนระบบถามตอบ](media/q-and-a-tooling-teach-q-and-a/qna-tooling-teach-fixpreview.png)

4. <span data-ttu-id="e27c2-121">เลือก **บันทึก** เพื่อแสดงตัวอย่างวิชวลที่อัปเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="e27c2-121">Select **Save** to preview the updated visual.</span></span>

5. <span data-ttu-id="e27c2-122">ป้อนคำถามถัดไป หรือเลือก **X** เพื่อปิดหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="e27c2-122">Enter the next question, or select the **X** to close.</span></span>

<span data-ttu-id="e27c2-123">ผู้ใช้รายงานของคุณจะไม่เห็นการเปลี่ยนแปลงนี้จนกว่าคุณจะเผยแพร่รายงานกลับไปที่บริการ</span><span class="sxs-lookup"><span data-stu-id="e27c2-123">Your report consumers won't see this change until you publish the report back to the service.</span></span>

## <a name="define-nouns-and-adjectives"></a><span data-ttu-id="e27c2-124">กำหนดคำนามและคำคุณศัพท์</span><span class="sxs-lookup"><span data-stu-id="e27c2-124">Define nouns and adjectives</span></span>

<span data-ttu-id="e27c2-125">คุณสามารถสอนระบบถามตอบได้ด้วยคำศัพท์สองชนิดได้แก่:</span><span class="sxs-lookup"><span data-stu-id="e27c2-125">You can teach Q&A two types of terms:</span></span>

- <span data-ttu-id="e27c2-126">คำนาม</span><span class="sxs-lookup"><span data-stu-id="e27c2-126">Nouns</span></span>
- <span data-ttu-id="e27c2-127">คำคุณศัพท์</span><span class="sxs-lookup"><span data-stu-id="e27c2-127">Adjectives</span></span>

### <a name="define-a-noun-synonym"></a><span data-ttu-id="e27c2-128">กำหนดคำพ้องความหมายที่เป็นคำนาม</span><span class="sxs-lookup"><span data-stu-id="e27c2-128">Define a noun synonym</span></span>

<span data-ttu-id="e27c2-129">เมื่อทำงานกับข้อมูล คุณมักจะมีชื่อของเขตข้อมูลที่สามารถอ้างอิงกับชื่อสำรองได้</span><span class="sxs-lookup"><span data-stu-id="e27c2-129">When working with data, you often may have names of fields that could be referred to with alternative names.</span></span> <span data-ttu-id="e27c2-130">ตัวอย่างอาจเป็น 'ยอดขาย'</span><span class="sxs-lookup"><span data-stu-id="e27c2-130">An example could be 'Sales'.</span></span> <span data-ttu-id="e27c2-131">คำหรือวลีจำนวนมากสามารถอ้างอิงไปยังยอดขาย เช่น 'รายได้'</span><span class="sxs-lookup"><span data-stu-id="e27c2-131">Numerous words or phrases could refer to sales, such as 'revenue'.</span></span> <span data-ttu-id="e27c2-132">ถ้าตั้งชื่อคอลัมน์ว่า 'ยอดขาย' และผู้ใช้รายงานพิมพ์คำว่า 'รายได้' ดังนั้นระบบถามตอบอาจไม่สามารถเลือกคอลัมน์ที่ถูกต้องเพื่อตอบคำถามได้อย่างเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="e27c2-132">If a column is named 'Sales', and report consumers type 'revenue', Q&A may fail to pick the correct column to answer the question appropriately.</span></span> <span data-ttu-id="e27c2-133">ในกรณีนี้ คุณต้องการบอกระบบถามตอบว่า 'ยอดขาย' และ 'รายได้' อ้างอิงถึงสิ่งเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="e27c2-133">In that case, you want to tell Q&A that 'Sales' and 'Revenue' refer to the same thing.</span></span>

<span data-ttu-id="e27c2-134">ระบบถามตอบจะตรวจจับโดยอัตโนมัติเมื่อคำที่ไม่รู้จักเป็นคำนามโดยใช้ความรู้จาก Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="e27c2-134">Q&A automatically detects when an unrecognized word is a noun using knowledge from Microsoft Office.</span></span> <span data-ttu-id="e27c2-135">ถ้าระบบถามตอบตรวจพบคำนาม ระบบจะพร้อมท์คุณในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e27c2-135">If Q&A detects a noun, it prompts you in the following way:</span></span>

- <span data-ttu-id="e27c2-136"><your term> **อ้างอิงไปยัง**</span><span class="sxs-lookup"><span data-stu-id="e27c2-136"><your term> **refers to**</span></span> 

<span data-ttu-id="e27c2-137">คุณกรอกคำศัพท์จากข้อมูลของคุณลงในกล่อง</span><span class="sxs-lookup"><span data-stu-id="e27c2-137">You fill in the box with the term from your data.</span></span>

![สกรีนช็อตแสดงบางส่วนของกล่องถามตอบพร้อมคำว่า รายได้ และข้อความที่ปรากฏของรายได้อ้างอิงถึงกล่องข้อความ](media/q-and-a-tooling-teach-q-and-a/qna-tooling-synonym-prompt.png)

<span data-ttu-id="e27c2-139">หากคุณให้สิ่งอื่นที่ไม่ใช่เขตข้อมูลจากแบบจำลองข้อมูล คุณอาจได้รับผลลัพธ์ที่ไม่พึงประสงค์</span><span class="sxs-lookup"><span data-stu-id="e27c2-139">If you provide something other than a field from the data model, you may get undesirable results.</span></span>

### <a name="define-an-adjective-filter-condition"></a><span data-ttu-id="e27c2-140">กำหนดเงื่อนไขของตัวกรองคำคุณศัพท์</span><span class="sxs-lookup"><span data-stu-id="e27c2-140">Define an adjective filter condition</span></span>

<span data-ttu-id="e27c2-141">บางครั้งคุณอาจต้องการกำหนดคำศัพท์ที่ทำหน้าที่เป็นเงื่อนไขในข้อมูลพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="e27c2-141">Sometimes you may want to define terms that act as a condition on the underlying data.</span></span> <span data-ttu-id="e27c2-142">ตัวอย่างอาจเป็น 'ผู้เผยแพร่ที่ยอดเยี่ยม'</span><span class="sxs-lookup"><span data-stu-id="e27c2-142">An example could be 'Awesome Publishers'.</span></span> <span data-ttu-id="e27c2-143">'ที่ยอดเยี่ยม' อาจเป็นเงื่อนไขที่เลือกเฉพาะผู้เผยแพร่ที่มีการเผยแพร่ผลิตภัณฑ์จำนวน X รายการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e27c2-143">'Awesome' could be a condition that only selects publishers that have published X number of products.</span></span> <span data-ttu-id="e27c2-144">ระบบถามตอบจะพยายามตรวจหาคำคุณศัพท์ ด้วยการแสดงพร้อมท์ที่แตกต่างกัน:</span><span class="sxs-lookup"><span data-stu-id="e27c2-144">Q&A tries to detect adjectives, showing a different prompt:</span></span>

- <span data-ttu-id="e27c2-145"><field name> **ที่มี**</span><span class="sxs-lookup"><span data-stu-id="e27c2-145"><field name> **that have**</span></span>  

<span data-ttu-id="e27c2-146">คุณจะระบุเงื่อนไขลงในกล่อง</span><span class="sxs-lookup"><span data-stu-id="e27c2-146">You fill in the box with the condition.</span></span>

![สกรีนช็อตแสดงส่วนหนึ่งของกล่องถามตอบพร้อมคำว่า ผู้เผยแพร่ยอดเยี่ยมและพร้อมท์ ผู้เผยแพร่ ที่อยู่ถัดจากกล่องข้อความและคำนั้นยอดเยี่ยม](media/q-and-a-tooling-teach-q-and-a/qna-tooling-adjectives.png)

<span data-ttu-id="e27c2-148">ตัวอย่างเงื่อนไขบางอย่างที่คุณสามารถกำหนดได้คือ:</span><span class="sxs-lookup"><span data-stu-id="e27c2-148">Some example conditions that you can define are:</span></span>

- <span data-ttu-id="e27c2-149">ประเทศซึ่งก็คือสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="e27c2-149">Country which is USA</span></span>
- <span data-ttu-id="e27c2-150">ประเทศซึ่งไม่ใช่สหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="e27c2-150">Country which is not USA</span></span>
- <span data-ttu-id="e27c2-151">ผลิตภัณฑ์ > 100</span><span class="sxs-lookup"><span data-stu-id="e27c2-151">Products > 100</span></span>
- <span data-ttu-id="e27c2-152">ผลิตภัณฑ์มากกว่า 100</span><span class="sxs-lookup"><span data-stu-id="e27c2-152">Products greater than 100</span></span>
- <span data-ttu-id="e27c2-153">ผลิตภัณฑ์ = 100</span><span class="sxs-lookup"><span data-stu-id="e27c2-153">Products = 100</span></span>
- <span data-ttu-id="e27c2-154">ผลิตภัณฑ์เท่ากับ 100</span><span class="sxs-lookup"><span data-stu-id="e27c2-154">Products is 100</span></span>
- <span data-ttu-id="e27c2-155">ผลิตภัณฑ์ < 100</span><span class="sxs-lookup"><span data-stu-id="e27c2-155">Products < 100</span></span>
- <span data-ttu-id="e27c2-156">ผลิตภัณฑ์น้อยกว่า 100</span><span class="sxs-lookup"><span data-stu-id="e27c2-156">Products smaller than 100</span></span>

<span data-ttu-id="e27c2-157">ในตัวอย่างเหล่านี้ 'ผลิตภัณฑ์' อาจเป็นชื่อคอลัมน์หรือหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="e27c2-157">In these examples, 'Products' could be either a column name or a measure.</span></span> 

<span data-ttu-id="e27c2-158">คุณยังสามารถระบุการรวมในนิพจน์การถามตอบได้</span><span class="sxs-lookup"><span data-stu-id="e27c2-158">You can also specify an aggregation in the Q&A expression itself.</span></span> <span data-ttu-id="e27c2-159">ตัวอย่างเช่น หาก 'ผลิตภัณฑ์ยอดนิยม' เป็นผลิตภัณฑ์ที่มียอดขาย 100 หน่วย คุณสามารถกำหนดผลิตภัณฑ์ที่มี 'ผลรวมของหน่วยที่ขายได้ > 100' เป็นผลิตภัณฑ์ยอดนิยม</span><span class="sxs-lookup"><span data-stu-id="e27c2-159">For example, if ‘popular products’ are products with at least 100 units sold, you can define products with ‘sum of units sold > 100’ as popular.</span></span>  

:::image type="content" source="media/q-and-a-tooling-teach-q-and-a/power-bi-qna-popular-products.png" alt-text="กำหนด 'ผลิตภัณฑ์ยอดนิยม '":::

<span data-ttu-id="e27c2-161">คุณสามารถกำหนดได้เพียงเงื่อนไขเดียวเฉพาะในการใช้เครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="e27c2-161">You can only define a single condition in tooling.</span></span> <span data-ttu-id="e27c2-162">หากต้องการกำหนดเงื่อนไขที่ซับซ้อนมากขึ้น ให้ใช้ DAX เพื่อสร้างคอลัมน์หรือการวัดจากการคำนวณ จากนั้นใช้ส่วนการใช้เครื่องมือเพื่อสร้างเงื่อนไขเดียวสำหรับคอลัมน์หรือการวัดนั้น</span><span class="sxs-lookup"><span data-stu-id="e27c2-162">To define more complex conditions, use DAX to create a calculated column or measure, and then use the tooling section to create a single condition for that column or measure.</span></span>

## <a name="manage-terms"></a><span data-ttu-id="e27c2-163">จัดการคำศัพท์</span><span class="sxs-lookup"><span data-stu-id="e27c2-163">Manage terms</span></span>

<span data-ttu-id="e27c2-164">หลังจากที่คุณให้คำจำกัดความแล้ว คุณสามารถกลับไปดูการแก้ไขทั้งหมดที่คุณทำและแก้ไขหรือลบได้</span><span class="sxs-lookup"><span data-stu-id="e27c2-164">After you've provided definitions, you can go back to see all the fixes you made and edit or delete them.</span></span> 

1. <span data-ttu-id="e27c2-165">ใน **การตั้งค่าระบบถามตอบ** ให้ไปที่ส่วน **จัดการคำศัพท์**</span><span class="sxs-lookup"><span data-stu-id="e27c2-165">In **Q&A setup**, go to the **Manage terms** section.</span></span>

2. <span data-ttu-id="e27c2-166">ลบคำศัพท์ใดก็ตามที่คุณไม่ต้องการอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="e27c2-166">Delete any terms you no longer want.</span></span> <span data-ttu-id="e27c2-167">ในขณะนี้ คุณไม่สามารถแก้ไขคำศัพท์ได้</span><span class="sxs-lookup"><span data-stu-id="e27c2-167">Currently you can't edit terms.</span></span> <span data-ttu-id="e27c2-168">หากต้องการกำหนดคำศัพท์ใหม่ ให้ลบคำศัพท์และกำหนดใหม่</span><span class="sxs-lookup"><span data-stu-id="e27c2-168">To redefine a term, delete the term and define it.</span></span>

    ![จัดการคำศัพท์ของระบบถามตอบ](media/q-and-a-tooling-teach-q-and-a/qna-manage-terms.png)

## <a name="next-steps"></a><span data-ttu-id="e27c2-170">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="e27c2-170">Next steps</span></span>

<span data-ttu-id="e27c2-171">มีแนวปฏิบัติที่ดีที่สุดหลายประการสำหรับการพัฒนากลไกจัดการภาษาธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="e27c2-171">There are a number of best practices for improving the natural language engine.</span></span> <span data-ttu-id="e27c2-172">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [แนวทางปฏิบัติที่ดีที่สุดสำหรับการถามตอบ](q-and-a-best-practices.md)</span><span class="sxs-lookup"><span data-stu-id="e27c2-172">For more information, [Q&A best practices](q-and-a-best-practices.md).</span></span>
