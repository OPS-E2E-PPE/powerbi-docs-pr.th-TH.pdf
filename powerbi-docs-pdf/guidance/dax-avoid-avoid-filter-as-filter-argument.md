---
title: 'DAX: หลีกเลี่ยงการใช้ตัวกรองเป็นอาร์กิวเมนต์ตัวกรอง'
description: คำแนะนำเกี่ยวกับการใช้ฟังก์ชัน FILTER เป็นอาร์กิวเมนต์ตัวกรอง
author: peter-myers
ms.author: v-pemyer
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 12/30/2019
ms.openlocfilehash: 651b4f1323738809e19c0ee42f1dbe71f7bc3998
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96394347"
---
# <a name="dax-avoid-using-filter-as-a-filter-argument"></a><span data-ttu-id="c6aff-103">DAX: หลีกเลี่ยงการใช้ตัวกรองเป็นอาร์กิวเมนต์ตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="c6aff-103">DAX: Avoid using FILTER as a filter argument</span></span>

<span data-ttu-id="c6aff-104">ในฐานะที่เป็นผู้สร้างแบบจำลองข้อมูล คุณจะเขียนนิพจน์ DAX ที่จำเป็นต้องได้รับการประเมินในบริบทตัวกรองที่ปรับเปลี่ยนแล้ว</span><span class="sxs-lookup"><span data-stu-id="c6aff-104">As a data modeler, it's common you'll write DAX expressions that need to be evaluated in a modified filter context.</span></span> <span data-ttu-id="c6aff-105">ตัวอย่างเช่น คุณสามารถเขียนข้อกำหนดหน่วยวัดเพื่อคำนวณยอดขายสำหรับ "ผลิตภัณฑ์ที่มีอัตรากำไรสูง"</span><span class="sxs-lookup"><span data-stu-id="c6aff-105">For example, you can write a measure definition to calculate sales for "high margin products".</span></span> <span data-ttu-id="c6aff-106">เราจะอธิบายการคำนวณนี้ในภายหลังในบทความนี้</span><span class="sxs-lookup"><span data-stu-id="c6aff-106">We'll describe this calculation later in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="c6aff-107">บทความนี้จะเกี่ยวข้องโดยเฉพาะอย่างยิ่งสำหรับการคำนวณแบบจำลองที่ใช้ตัวกรองในการนำเข้าตาราง</span><span class="sxs-lookup"><span data-stu-id="c6aff-107">This article is especially relevant for model calculations that apply filters to Import tables.</span></span>

<span data-ttu-id="c6aff-108">ฟังก์ชัน [CALCULATE](/dax/calculate-function-dax) และ [CALCULATETABLE](/dax/calculatetable-function-dax) DAX เป็นฟังก์ชันที่สำคัญและมีประโยชน์</span><span class="sxs-lookup"><span data-stu-id="c6aff-108">The [CALCULATE](/dax/calculate-function-dax) and [CALCULATETABLE](/dax/calculatetable-function-dax) DAX functions are important and useful functions.</span></span> <span data-ttu-id="c6aff-109">ซึ่งช่วยให้คุณสามารถเขียนการคำนวณที่ลบหรือเพิ่มตัวกรอง หรือปรับเปลี่ยนเส้นทางความสัมพันธ์ได้</span><span class="sxs-lookup"><span data-stu-id="c6aff-109">They let you write calculations that remove or add filters, or modify relationship paths.</span></span> <span data-ttu-id="c6aff-110">การดำเนินการโดยการส่งผ่านในอาร์กิวเมนต์ตัวกรอง ซึ่งเป็นนิพจน์บูลีน นิพจน์ตาราง หรือฟังก์ชันตัวกรองพิเศษ</span><span class="sxs-lookup"><span data-stu-id="c6aff-110">It's done by passing in filter arguments, which are either Boolean expressions, table expressions, or special filter functions.</span></span> <span data-ttu-id="c6aff-111">เราจะพูดคุยเกี่ยวกับนิพจน์บูลีนและตารางในบทความนี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c6aff-111">We'll only discuss Boolean and table expressions in this article.</span></span>

<span data-ttu-id="c6aff-112">พิจารณาข้อกำหนดหน่วยวัดต่อไปนี้ ซึ่งจะคำนวณยอดขายผลิตภัณฑ์สีแดงโดยใช้นิพจน์ตาราง</span><span class="sxs-lookup"><span data-stu-id="c6aff-112">Consider the following measure definition, which calculates red product sales by using a table expression.</span></span> <span data-ttu-id="c6aff-113">การดำเนินการดังกล่าวจะแทนที่ตัวกรองใด ๆ ที่อาจใช้กับตาราง **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="c6aff-113">It will replace any filters that might be applied to the **Product** table.</span></span>

```dax
Red Sales =
CALCULATE(
    [Sales],
    FILTER('Product', 'Product'[Color] = "Red")
)
```

<span data-ttu-id="c6aff-114">ฟังก์ชันการคำนวณจะยอมรับนิพจน์ตารางที่ส่งกลับโดยฟังก์ชัน [FILTER](/dax/filter-function-dax) DAX ซึ่งประเมินนิพจน์ตัวกรองสำหรับแต่ละแถวของตาราง **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="c6aff-114">The CALCULATE function accepts a table expression returned by the [FILTER](/dax/filter-function-dax) DAX function, which evaluates its filter expression for each row of the **Product** table.</span></span> <span data-ttu-id="c6aff-115">ซึ่งเป็นผลลัพธ์ที่ถูกต้อง–ผลการขายสำหรับผลิตภัณฑ์สีแดง</span><span class="sxs-lookup"><span data-stu-id="c6aff-115">It achieves the correct result—the sales result for red products.</span></span> <span data-ttu-id="c6aff-116">อย่างไรก็ตาม อาจมีประสิทธิภาพมากขึ้นด้วยการใช้นิพจน์บูลีน</span><span class="sxs-lookup"><span data-stu-id="c6aff-116">However, it could be achieved much more efficiently by using a Boolean expression.</span></span>

<span data-ttu-id="c6aff-117">ข้อกำหนดนี้เป็นข้อกำหนดหน่วยวัดที่ได้รับการปรับปรุง ซึ่งใช้นิพจน์บูลีนแทนที่จะเป็นนิพจน์ตาราง</span><span class="sxs-lookup"><span data-stu-id="c6aff-117">Here's an improved measure definition, which uses a Boolean expression instead of the table expression.</span></span> <span data-ttu-id="c6aff-118">ฟังก์ชัน [KEEPFILTERS](/dax/keepfilters-function-dax) DAX ช่วยให้แน่ใจว่าตัวกรองใดๆ ที่มีอยู่ที่ใช้กับคอลัมน์ **สี** ได้รับการรักษาไว้และไม่ได้เขียนทับ</span><span class="sxs-lookup"><span data-stu-id="c6aff-118">The [KEEPFILTERS](/dax/keepfilters-function-dax) DAX function ensures any existing filters applied to the **Color** column are preserved, and not overwritten.</span></span>

```dax
Red Sales =
CALCULATE(
    [Sales],
    KEEPFILTERS('Product'[Color] = "Red")
)
```

<span data-ttu-id="c6aff-119">เราขอแนะนำให้คุณส่งผ่านอาร์กิวเมนต์ตัวกรองเป็นนิพจน์บูลีนเมื่อใดก็ตามที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="c6aff-119">We recommend you pass filter arguments as Boolean expressions, whenever possible.</span></span> <span data-ttu-id="c6aff-120">เนื่องจากมีการนำเข้าตารางแบบจำลองเป็นที่เก็บคอลัมน์ในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="c6aff-120">It's because Import model tables are in-memory column stores.</span></span> <span data-ttu-id="c6aff-121">ซึ่งจะได้รับการปรับให้เหมาะสมเพื่อให้สามารถกรองคอลัมน์ได้อย่างมีประสิทธิภาพด้วยวิธีนี้</span><span class="sxs-lookup"><span data-stu-id="c6aff-121">They are explicitly optimized to efficiently filter columns in this way.</span></span>

<span data-ttu-id="c6aff-122">อย่างไรก็ตาม มีข้อจำกัดที่ใช้กับนิพจน์บูลีนเมื่อใช้เป็นอาร์กิวเมนต์ตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="c6aff-122">There are, however, restrictions that apply to Boolean expressions when they're used as filter arguments.</span></span> <span data-ttu-id="c6aff-123">ข้อจำกัดเหล่านั้นคือ:</span><span class="sxs-lookup"><span data-stu-id="c6aff-123">They:</span></span>

- <span data-ttu-id="c6aff-124">ไม่สามารถเปรียบเทียบคอลัมน์กับคอลัมน์อื่นได้</span><span class="sxs-lookup"><span data-stu-id="c6aff-124">Cannot compare columns to other columns</span></span>
- <span data-ttu-id="c6aff-125">ไม่สามารถอ้างอิงหน่วยวัดได้</span><span class="sxs-lookup"><span data-stu-id="c6aff-125">Cannot reference a measure</span></span>
- <span data-ttu-id="c6aff-126">ไม่สามารถใช้ฟังก์ชันการคำนวณแบบซ้อนกันได้</span><span class="sxs-lookup"><span data-stu-id="c6aff-126">Cannot use nested CALCULATE functions</span></span>
- <span data-ttu-id="c6aff-127">ไม่สามารถใช้ฟังก์ชันที่สแกนหรือแสดงเป็นตารางได้</span><span class="sxs-lookup"><span data-stu-id="c6aff-127">Cannot use functions that scan or return a table</span></span>

<span data-ttu-id="c6aff-128">ซึ่งหมายความว่าคุณจะต้องใช้นิพจน์ตารางสำหรับข้อกำหนดของตัวกรองที่ซับซ้อนมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="c6aff-128">It means that you'll need to use table expressions for more complex filter requirements.</span></span>

<span data-ttu-id="c6aff-129">ตอนนี้ให้พิจารณาข้อกำหนดหน่วยวัดที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="c6aff-129">Consider now a different measure definition.</span></span>

```dax
High Margin Product Sales =
CALCULATE(
    [Sales],
    FILTER(
        'Product',
        'Product'[ListPrice] > 'Product'[StandardCost] * 2
    )
)
```

<span data-ttu-id="c6aff-130">ข้อกำหนดของ _ผลิตภัณฑ์ที่มีอัตรากำไรสูง_ เป็นหนึ่งข้อกำหนดที่มีราคาตามรายการเกินกว่าค่าใช้จ่ายมาตรฐานสองเท่า</span><span class="sxs-lookup"><span data-stu-id="c6aff-130">The definition of a _high margin product_ is one that has a list price exceeding double its standard cost.</span></span> <span data-ttu-id="c6aff-131">ในตัวอย่างนี้ ฟังก์ชัน FILTER ต้องถูกนำมาใช้</span><span class="sxs-lookup"><span data-stu-id="c6aff-131">In this example, the FILTER function must be used.</span></span> <span data-ttu-id="c6aff-132">เนื่องจากนิพจน์ตัวกรองมีความซับซ้อนเกินไปสำหรับนิพจน์บูลีน</span><span class="sxs-lookup"><span data-stu-id="c6aff-132">It's because the filter expression is too complex for a Boolean expression.</span></span>

<span data-ttu-id="c6aff-133">นี่คือหนึ่งในตัวอย่างเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c6aff-133">Here's one more example.</span></span> <span data-ttu-id="c6aff-134">ความต้องการในขณะนี้คือการคำนวณยอดขาย แต่เฉพาะสำหรับเดือนที่มีกำไรเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c6aff-134">The requirement this time is to calculate sales, but only for months that have achieved a profit.</span></span>

```dax
Sales for Profitable Months =
CALCULATE(
    [Sales],
    FILTER(
        VALUES('Date'[Month]),
        [Profit] > 0)
    )
)
```

<span data-ttu-id="c6aff-135">ในตัวอย่างนี้ ฟังก์ชัน FILTER ต้องถูกนำมาใช้</span><span class="sxs-lookup"><span data-stu-id="c6aff-135">In this example, the FILTER function must also be used.</span></span> <span data-ttu-id="c6aff-136">เนื่องจากจำเป็นต้องประเมินผลหน่วยวัด **กำไร** เพื่อลบเดือนที่ไม่ได้กำไรออกไป</span><span class="sxs-lookup"><span data-stu-id="c6aff-136">It's because it requires evaluating the **Profit** measure to eliminate those months that didn't achieve a profit.</span></span> <span data-ttu-id="c6aff-137">ซึ่งไม่สามารถใช้หน่วยวัดในนิพจน์บูลีนเมื่อใช้เป็นอาร์กิวเมนต์ตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="c6aff-137">It's not possible to use a measure in a Boolean expression when it's used as a filter argument.</span></span>

## <a name="recommendations"></a><span data-ttu-id="c6aff-138">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="c6aff-138">Recommendations</span></span>

<span data-ttu-id="c6aff-139">เพื่อประสิทธิภาพที่ดีที่สุด เราขอแนะนำให้คุณใช้นิพจน์บูลีนเป็นอาร์กิวเมนต์ตัวกรองเมื่อใดก็ตามที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="c6aff-139">For best performance, we recommend you use Boolean expressions as filter arguments, whenever possible.</span></span>

<span data-ttu-id="c6aff-140">ดังนั้นควรใช้ฟังก์ชัน FILTER เฉพาะเมื่อจำเป็นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c6aff-140">Therefore, the FILTER function should only be used when necessary.</span></span> <span data-ttu-id="c6aff-141">คุณสามารถใช้เพื่อดำเนินการเปรียบเทียบคอลัมน์ที่ซับซ้อนของตัวกรองได้</span><span class="sxs-lookup"><span data-stu-id="c6aff-141">You can use it to perform filter complex column comparisons.</span></span> <span data-ttu-id="c6aff-142">การเปรียบเทียบคอลัมน์เหล่านี้อาจเกี่ยวข้องกับ:</span><span class="sxs-lookup"><span data-stu-id="c6aff-142">These column comparisons can involve:</span></span>

- <span data-ttu-id="c6aff-143">หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="c6aff-143">Measures</span></span>
- <span data-ttu-id="c6aff-144">คอลัมน์อื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="c6aff-144">Other columns</span></span>
- <span data-ttu-id="c6aff-145">การใช้ฟังก์ชัน [OR](/dax/or-function-dax) DAX หรือตัวดำเนินการ OR เชิงตรรกะ (||)</span><span class="sxs-lookup"><span data-stu-id="c6aff-145">Using the [OR](/dax/or-function-dax) DAX function, or the OR logical operator (||)</span></span>

## <a name="next-steps"></a><span data-ttu-id="c6aff-146">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c6aff-146">Next steps</span></span>

<span data-ttu-id="c6aff-147">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c6aff-147">For more information about this article, check out the following resources:</span></span>

- [<span data-ttu-id="c6aff-148">ข้อมูลอ้างอิงเกี่ยวกับ Data Analysis Expressions (DAX)</span><span class="sxs-lookup"><span data-stu-id="c6aff-148">Data Analysis Expressions (DAX) Reference</span></span>](/dax/)
- [<span data-ttu-id="c6aff-149">ฟังก์ชันตัวกรอง (DAX)</span><span class="sxs-lookup"><span data-stu-id="c6aff-149">Filter functions (DAX)</span></span>](/dax/filter-function-dax)
- <span data-ttu-id="c6aff-150">เส้นทางการเรียนรู้: [ใช้ DAX ใน Power BI Desktop](/learn/paths/dax-power-bi/)</span><span class="sxs-lookup"><span data-stu-id="c6aff-150">Learning path: [Use DAX in Power BI Desktop](/learn/paths/dax-power-bi/)</span></span>
- <span data-ttu-id="c6aff-151">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c6aff-151">Questions?</span></span> [<span data-ttu-id="c6aff-152">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="c6aff-152">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="c6aff-153">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="c6aff-153">Suggestions?</span></span> [<span data-ttu-id="c6aff-154">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="c6aff-154">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com)