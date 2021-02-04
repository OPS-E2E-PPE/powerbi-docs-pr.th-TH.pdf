---
title: 'DAX: การอ้างอิงคอลัมน์และหน่วยวัด'
description: คำแนะนำเกี่ยวกับการอ้างอิงถึงคอลัมน์ในหน่วยวัดในสมการ DAX ของคุณ
author: peter-myers
ms.author: v-pemyer
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 12/18/2019
ms.openlocfilehash: 861fd2d5c3d511358b508c7a0d6f7e96472e5aaf
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96394255"
---
# <a name="dax-column-and-measure-references"></a><span data-ttu-id="b6e47-103">DAX: การอ้างอิงคอลัมน์และหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="b6e47-103">DAX: Column and measure references</span></span>

<span data-ttu-id="b6e47-104">ในฐานะผู้ออกแบบโมเดลข้อมูล สมการ DAX จะอ้างอิงคอลัมน์และหน่วยวัดโมเดล</span><span class="sxs-lookup"><span data-stu-id="b6e47-104">As a data modeler, your DAX expressions will refer to model columns and measures.</span></span> <span data-ttu-id="b6e47-105">คอลัมน์และหน่วยวัดจะเชื่อมโยงกับตารางแบบจำลองเสมอแต่ความสัมพันธ์เหล่านี้จะแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="b6e47-105">Columns and measures are always associated with model tables, but these associations are different.</span></span> <span data-ttu-id="b6e47-106">ดังนั้นเราจึงมีคำแนะนำที่แตกต่างสำหรับวิธีที่คุณจะอ้างอิงในสูตรของคุณ</span><span class="sxs-lookup"><span data-stu-id="b6e47-106">So, we have different recommendations on how you'll reference them in your expressions.</span></span>

## <a name="columns"></a><span data-ttu-id="b6e47-107">คอลัมน์</span><span class="sxs-lookup"><span data-stu-id="b6e47-107">Columns</span></span>

<span data-ttu-id="b6e47-108">คอลัมน์เป็นวัตถุระดับตาราง และชื่อคอลัมน์ภายในตารางต้องไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="b6e47-108">A column is a table-level object, and column names must be unique within a table.</span></span> <span data-ttu-id="b6e47-109">ดังนั้นจึงเป็นไปได้ว่าชื่อคอลัมน์เดียวกันถูกใช้หลายครั้งในแบบจำลองของคุณ—ให้ชื่อคอลัมน์อยู่ในตารางที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="b6e47-109">So it's possible that the same column name is used multiple times in your model—providing they belong to different tables.</span></span> <span data-ttu-id="b6e47-110">มีกฎอีกหนึ่งข้อ: ชื่อคอลัมน์ไม่สามารถซ้ำกันโดยเป็นชื่อของหน่วยวัดหรือชื่อของลำดับชั้นที่มีอยู่ในตารางเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="b6e47-110">There's one more rule: a column name cannot have the same name as a measure name or hierarchy name that exists in the same table.</span></span>

<span data-ttu-id="b6e47-111">โดยทั่วไป DAX จะไม่บังคับให้ใช้การอ้างอิง _แบบครบถ้วน_ ไปยังคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="b6e47-111">In general, DAX will not force using a _fully qualified_ reference to a column.</span></span> <span data-ttu-id="b6e47-112">การอ้างอิงแบบครบถ้วนหมายความว่าชื่อตารางอยู่ก่อนหน้าชื่อคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="b6e47-112">A fully qualified reference means that the table name precedes the column name.</span></span>

<span data-ttu-id="b6e47-113">นี่คือตัวอย่างขอต่อไปนี้คือตัวอย่างของข้อกำหนดคอลัมน์จากการคำนวณโดยใช้การอ้างอิงชื่อคอลัมน์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b6e47-113">Here's an example of a calculated column definition using only column name references.</span></span> <span data-ttu-id="b6e47-114">คอลัมน์ **ยอดขาย** และ **ต้นทุน** นั้นอยู่ในตารางที่ชื่อว่า **รายการสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="b6e47-114">The **Sales** and **Cost** columns both belong to a table named **Orders**.</span></span>

```dax
Profit = [Sales] - [Cost]
```

<span data-ttu-id="b6e47-115">สามารถเขียนคำจำกัดความใหม่ด้วยการอ้างอิงคอลัมน์แบบครบถ้วน</span><span class="sxs-lookup"><span data-stu-id="b6e47-115">The same definition can be rewritten with fully qualified column references.</span></span>

```dax
Profit = Orders[Sales] - Orders[Cost]
```

<span data-ttu-id="b6e47-116">อย่างไรก็ตามบางครั้งคุณจะต้องใช้การอ้างอิงคอลัมน์แบบครบถ้วนเมื่อ Power BI พบความคลาดเคลื่อน</span><span class="sxs-lookup"><span data-stu-id="b6e47-116">Sometimes, however, you'll be required to use fully qualified column references when Power BI detects ambiguity.</span></span> <span data-ttu-id="b6e47-117">เมื่อป้อนสูตร เมื่อใส่สูตรจะมีข้อความที่เป็นเส้นหยักและข้อผิดพลาดเป็นสีแดงจะแจ้งเตือนคุณ</span><span class="sxs-lookup"><span data-stu-id="b6e47-117">When entering a formula, a red squiggly and error message will alert you.</span></span> <span data-ttu-id="b6e47-118">นอกจากนั้นบางฟังก์ชัน DAX เช่น ฟังก์ชัน DAX [LOOKUPVALUE](/dax/lookupvalue-function-dax) จะต้องใช้การคอลัมน์แบบครบถ้วน</span><span class="sxs-lookup"><span data-stu-id="b6e47-118">Also, some DAX functions like the [LOOKUPVALUE](/dax/lookupvalue-function-dax) DAX function, require the use of fully qualified columns.</span></span>

<span data-ttu-id="b6e47-119">เราแนะนำให้คุณอ้างอิงคอลัมน์ของคุณแบบครบถ้วน</span><span class="sxs-lookup"><span data-stu-id="b6e47-119">We recommend you always fully qualify your column references.</span></span> <span data-ttu-id="b6e47-120">ซึ่งจะอธิบายเหตุผลในส่วน[คำแนะนำ](#recommendations)</span><span class="sxs-lookup"><span data-stu-id="b6e47-120">The reasons are provided in the [Recommendations](#recommendations) section.</span></span>

## <a name="measures"></a><span data-ttu-id="b6e47-121">หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="b6e47-121">Measures</span></span>

<span data-ttu-id="b6e47-122">หน่วยวัดคือวัตถุระดับโมเดล</span><span class="sxs-lookup"><span data-stu-id="b6e47-122">A measure is a model-level object.</span></span> <span data-ttu-id="b6e47-123">ด้วยเหตุนี้ ชื่อของหน่วยวัดภายในโมเดลจะต้องไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="b6e47-123">For this reason, measure names must be unique within the model.</span></span> <span data-ttu-id="b6e47-124">อย่างในก็ตาม ในหน้าต่าง **เขตข้อมูล** ผู้เขียนรายงานจะเห็นแต่ละหน่วยวัดที่เชื่อมโยงกับตารางโมเดลเดียว</span><span class="sxs-lookup"><span data-stu-id="b6e47-124">However, in the **Fields** pane, report authors will see each measure associated with a single model table.</span></span> <span data-ttu-id="b6e47-125">ความสัมพันธ์นี้เป็นชุดเหตุผลการเติมแต่ง และคุณสามารถกำหนดโดยการตั้งค่าคุณสมบัติ **ตารางหลัก** สำหรับหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="b6e47-125">This association is set for cosmetic reasons, and you can configure it by setting the **Home Table** property for the measure.</span></span> <span data-ttu-id="b6e47-126">สำหรับข้อมูลเพิ่มเติม ศึกษา [หน่ววัดใน Power BI Desktop (การจัดระเบียบหน่วยวัดของคุณ)](../transform-model/desktop-measures.md#organizing-your-measures)</span><span class="sxs-lookup"><span data-stu-id="b6e47-126">For more information, see [Measures in Power BI Desktop (Organizing your measures)](../transform-model/desktop-measures.md#organizing-your-measures).</span></span>

<span data-ttu-id="b6e47-127">คุณสามารถใช้หน่วยวัดแบบครบถ้วนในสมการของคุณ</span><span class="sxs-lookup"><span data-stu-id="b6e47-127">It's possible to use a fully qualified measure in your expressions.</span></span> <span data-ttu-id="b6e47-128">DAX intellisense จะเสนอคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="b6e47-128">DAX intellisense will even offer the suggestion.</span></span> <span data-ttu-id="b6e47-129">อย่างไรก็ตามก็ไม่จำเป็นและไม่ใช้วิธีปฏิบัติที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="b6e47-129">However, it isn't necessary, and it's not a recommended practice.</span></span> <span data-ttu-id="b6e47-130">หากคุณเปลี่ยนตารางหลักสำหรับหน่วยวัด สมการใด ๆ ที่ใช้การอ้างอิงแบบครบถ้วนจะแบ่งออก</span><span class="sxs-lookup"><span data-stu-id="b6e47-130">If you change the home table for a measure, any expression that uses a fully qualified measure reference to it will break.</span></span> <span data-ttu-id="b6e47-131">จากนั้นคุณจะต้องแก้ไขแต่ละสมการที่แยกออกมา เพื่อนำการอ้างอิงการวัดออก (หรืออัพเดต)</span><span class="sxs-lookup"><span data-stu-id="b6e47-131">You'll then need to edit each broken formula to remove (or update) the measure reference.</span></span>

<span data-ttu-id="b6e47-132">เราแนะนำให้คุณไม่รับรองการอ้างอิงหน่วยวัดของคุณ</span><span class="sxs-lookup"><span data-stu-id="b6e47-132">We recommend you never qualify your measure references.</span></span> <span data-ttu-id="b6e47-133">ซึ่งจะอธิบายเหตุผลในส่วน[คำแนะนำ](#recommendations)</span><span class="sxs-lookup"><span data-stu-id="b6e47-133">The reasons are provided in the [Recommendations](#recommendations) section.</span></span>

## <a name="recommendations"></a><span data-ttu-id="b6e47-134">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="b6e47-134">Recommendations</span></span>

<span data-ttu-id="b6e47-135">คำแนะนำของเรานั้นเรียบง่ายต่อการจดจำ</span><span class="sxs-lookup"><span data-stu-id="b6e47-135">Our recommendations are simple and easy to remember:</span></span>

- <span data-ttu-id="b6e47-136">ใช้การอ้างอิงคอลัมน์แบบครบถ้วนเสมอ</span><span class="sxs-lookup"><span data-stu-id="b6e47-136">Always use fully qualified column references</span></span>
- <span data-ttu-id="b6e47-137">ไม่ใช้การอ้างอิงแบบครบถ้วน</span><span class="sxs-lookup"><span data-stu-id="b6e47-137">Never use fully qualified measure references</span></span>

<span data-ttu-id="b6e47-138">นี่คือเหตุผล:</span><span class="sxs-lookup"><span data-stu-id="b6e47-138">Here's why:</span></span>

- <span data-ttu-id="b6e47-139">**การป้องสูตร**: จะยอมรับสมการ เนื่องจากไม่มีการอ้างอิงที่ไม่ชัดเจนที่ต้องแก้ไข</span><span class="sxs-lookup"><span data-stu-id="b6e47-139">**Formula entry**: Expressions will be accepted, as there won't be any ambiguous references to resolve.</span></span> <span data-ttu-id="b6e47-140">นอกจากนั้นคุณจะต้องปฏิบัติตามข้อกำหนดของฟังก์ชัน DAX ที่ต้องอ้างอิงแบบครบถ้วน</span><span class="sxs-lookup"><span data-stu-id="b6e47-140">Also, you'll meet the requirement for those DAX functions that require fully qualified column references.</span></span>
- <span data-ttu-id="b6e47-141">**ความคงทน**: สมการจะต้องทำงาน แม้ว่าคุณจะเปลี่ยนคุณสมบัติตารางหลักหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="b6e47-141">**Robustness**: Expressions will continue to work, even when you change a measure home table property.</span></span>
- <span data-ttu-id="b6e47-142">**การอ่าน**: สมการจะต้องเข้าใจได้โดยง่ายและรวดเร็ว คุณจะกำหนดอย่างรวดเร็วว่าคอลัมน์และหน่วยวัด ซึ่งขึ้นอยู่กับว่ามีคุณสมบัติครบถ้วนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="b6e47-142">**Readability**: Expressions will be quick and easy to understand—you'll quickly determine that it's a column or measure, based on whether it's fully qualified or not.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b6e47-143">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="b6e47-143">Next steps</span></span>

<span data-ttu-id="b6e47-144">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b6e47-144">For more information about this article, check out the following resources:</span></span>

- [<span data-ttu-id="b6e47-145">ข้อมูลอ้างอิงเกี่ยวกับ Data Analysis Expressions (DAX)</span><span class="sxs-lookup"><span data-stu-id="b6e47-145">Data Analysis Expressions (DAX) Reference</span></span>](/dax/)
- <span data-ttu-id="b6e47-146">เส้นทางการเรียนรู้: [ใช้ DAX ใน Power BI Desktop](/learn/paths/dax-power-bi/)</span><span class="sxs-lookup"><span data-stu-id="b6e47-146">Learning path: [Use DAX in Power BI Desktop](/learn/paths/dax-power-bi/)</span></span>
- <span data-ttu-id="b6e47-147">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="b6e47-147">Questions?</span></span> [<span data-ttu-id="b6e47-148">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="b6e47-148">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="b6e47-149">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="b6e47-149">Suggestions?</span></span> [<span data-ttu-id="b6e47-150">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="b6e47-150">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com)