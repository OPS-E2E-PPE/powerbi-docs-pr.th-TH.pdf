---
title: 'DAX: ใช้ตัวแปรเพื่อปรับปรุงสูตรของคุณ'
description: คำแนะนำเกี่ยวกับการใช้ตัวแปรในนิพจน์ DAX
author: peter-myers
ms.author: v-pemyer
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 11/23/2019
ms.openlocfilehash: 2448ac8b94465872e4224738162c6a252cafe56c
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96393611"
---
# <a name="dax-use-variables-to-improve-your-formulas"></a><span data-ttu-id="6ac24-103">DAX: ใช้ตัวแปรเพื่อปรับปรุงสูตรของคุณ</span><span class="sxs-lookup"><span data-stu-id="6ac24-103">DAX: Use variables to improve your formulas</span></span>

<span data-ttu-id="6ac24-104">ในฐานะผู้สร้างแบบจำลองข้อมูล การเขียนและการดีบักการคำนวณ DAX บางอย่างอาจเป็นเรื่องที่ท้าทาย</span><span class="sxs-lookup"><span data-stu-id="6ac24-104">As a data modeler, writing and debugging some DAX calculations can be challenging.</span></span> <span data-ttu-id="6ac24-105">ซึ่งเป็นเรื่องปกติที่ข้อกำหนดการคำนวณที่ซับซ้อนมักเกี่ยวข้องกับการเขียนนิพจน์ประสมหรือนิพจน์ซับซ้อน</span><span class="sxs-lookup"><span data-stu-id="6ac24-105">It's common that complex calculation requirements often involve writing compound or complex expressions.</span></span> <span data-ttu-id="6ac24-106">นิพจน์ประสมสามารถเกี่ยวข้องกับการใช้ฟังก์ชันที่ซ้อนกันมากมาย และอาจมีการนำตรรกะของนิพจน์กลับมาใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="6ac24-106">Compound expressions can involve the use of many nested functions, and possibly the reuse of expression logic.</span></span>

<span data-ttu-id="6ac24-107">การใช้ตัวแปรในสูตร DAX ของคุณจะช่วยให้คุณสามารถเขียนการคำนวณที่ซับซ้อนและมีประสิทธิภาพได้</span><span class="sxs-lookup"><span data-stu-id="6ac24-107">Using variables in your DAX formulas helps you write complex and efficient calculations.</span></span> <span data-ttu-id="6ac24-108">ตัวแปรสามารถ:</span><span class="sxs-lookup"><span data-stu-id="6ac24-108">Variables can:</span></span>

- [<span data-ttu-id="6ac24-109">ปรับปรุงประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="6ac24-109">Improve performance</span></span>](#improve-performance)
- [<span data-ttu-id="6ac24-110">ปรับปรุงความสามารถในการอ่าน</span><span class="sxs-lookup"><span data-stu-id="6ac24-110">Improve readability</span></span>](#improve-readability)
- [<span data-ttu-id="6ac24-111">ทำให้การดีบักง่าย</span><span class="sxs-lookup"><span data-stu-id="6ac24-111">Simplify debugging</span></span>](#simplify-debugging)
- [<span data-ttu-id="6ac24-112">ลดความซับซ้อน</span><span class="sxs-lookup"><span data-stu-id="6ac24-112">Reduce complexity</span></span>](#reduce-complexity)

<span data-ttu-id="6ac24-113">ในบทความนี้ เราจะแสดงให้เห็นถึงประโยชน์สามประการแรกโดยใช้ตัวอย่างหน่วยวัดสำหรับการเติบโตของยอดขายแบบรายปี (YoY)</span><span class="sxs-lookup"><span data-stu-id="6ac24-113">In this article, we'll demonstrate the first three benefits by using an example measure for year-over-year (YoY) sales growth.</span></span> <span data-ttu-id="6ac24-114">(สูตรสำหรับการเติบโตของยอดขายแบบรายปีคือ: ยอดขาย sales _fewer ตามช่วงเวลาสำหรับช่วงเวลาเดียวกันของปีที่แล้ว _หารด้วย_ ยอดขายสำหรับช่วงเวลาเดียวกันของปีที่แล้ว)</span><span class="sxs-lookup"><span data-stu-id="6ac24-114">(The formula for YoY sales growth is: period sales _fewer sales for the same period last year, _divided by_ sales for the same period last year.)</span></span>

<span data-ttu-id="6ac24-115">มาเริ่มต้นจากข้อกำหนดหน่วยวัดต่อไปนี้กันดีกว่า</span><span class="sxs-lookup"><span data-stu-id="6ac24-115">Let's start with the following measure definition.</span></span>

```dax
Sales YoY Growth % =
DIVIDE(
    ([Sales] - CALCULATE([Sales], PARALLELPERIOD('Date'[Date], -12, MONTH))),
    CALCULATE([Sales], PARALLELPERIOD('Date'[Date], -12, MONTH))
)
```

<span data-ttu-id="6ac24-116">หน่วยวัดให้ผลลัพธ์ที่ถูกต้อง แต่ตอนนี้มาดูกันว่าเราจะสามารถปรับปรุงอะไรได้อย่างไรบ้าง</span><span class="sxs-lookup"><span data-stu-id="6ac24-116">The measure produces the correct result, yet let's now see how it can be improved.</span></span>

## <a name="improve-performance"></a><span data-ttu-id="6ac24-117">ปรับปรุงประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="6ac24-117">Improve performance</span></span>

<span data-ttu-id="6ac24-118">ขอให้สังเกตว่าสูตรทำซ้ำนิพจน์ที่คำนวณ "ช่วงเวลาเดียวกันของปีที่แล้ว"</span><span class="sxs-lookup"><span data-stu-id="6ac24-118">Notice that the formula repeats the expression that calculates "same period last year".</span></span> <span data-ttu-id="6ac24-119">สูตรนี้ไม่มีประสิทธิภาพ เนื่องจากต้องใช้ Power BI เพื่อประเมินนิพจน์เดียวกันสองครั้ง</span><span class="sxs-lookup"><span data-stu-id="6ac24-119">This formula is inefficient, as it requires Power BI to evaluate the same expression twice.</span></span> <span data-ttu-id="6ac24-120">ข้อกำหนดหน่วยวัดสามารถทำให้มีประสิทธิภาพมากขึ้นโดยใช้ตัวแปร</span><span class="sxs-lookup"><span data-stu-id="6ac24-120">The measure definition can be made more efficient by using a variable.</span></span>

<span data-ttu-id="6ac24-121">ข้อกำหนดหน่วยวัดต่อไปนี้แสดงถึงการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="6ac24-121">The following measure definition represents an improvement.</span></span> <span data-ttu-id="6ac24-122">ซึ่งใช้นิพจน์เพื่อกำหนดผลลัพธ์ "ช่วงเวลาเดียวกันของปีที่แล้ว" ให้กับตัวแปรชื่อ **SalesPriorYear**</span><span class="sxs-lookup"><span data-stu-id="6ac24-122">It uses an expression to assign the "same period last year" result to a variable named **SalesPriorYear**.</span></span> <span data-ttu-id="6ac24-123">จากนั้นตัวแปรจะถูกใช้สองครั้งในนิพจน์ RETURN</span><span class="sxs-lookup"><span data-stu-id="6ac24-123">The variable is then used twice in the RETURN expression.</span></span>

```dax
Sales YoY Growth % =
VAR SalesPriorYear =
    CALCULATE([Sales], PARALLELPERIOD('Date'[Date], -12, MONTH))
RETURN
    DIVIDE(([Sales] - SalesPriorYear), SalesPriorYear)
```

<span data-ttu-id="6ac24-124">หน่วยวัดยังคงสร้างผลลัพธ์ที่ถูกต้องอย่างต่อเนื่องและใช้เวลาประมาณครึ่งหนึ่งของเวลาคิวรี</span><span class="sxs-lookup"><span data-stu-id="6ac24-124">The measure continues to produce the correct result, and does so in about half the query time.</span></span>

## <a name="improve-readability"></a><span data-ttu-id="6ac24-125">ปรับปรุงความสามารถในการอ่าน</span><span class="sxs-lookup"><span data-stu-id="6ac24-125">Improve readability</span></span>

<span data-ttu-id="6ac24-126">ในข้อกำหนดหน่วยวัดก่อนหน้านี้ ให้สังเกตว่าตัวเลือกของชื่อตัวแปรทำให้นิพจน์ RETURN นั้นง่ายต่อการเข้าใจอย่างไร</span><span class="sxs-lookup"><span data-stu-id="6ac24-126">In the previous measure definition, notice how the choice of variable name makes the RETURN expression simpler to understand.</span></span> <span data-ttu-id="6ac24-127">นิพจน์สั้นและสามารถอธิบายตัวเองได้</span><span class="sxs-lookup"><span data-stu-id="6ac24-127">The expression is short and self-describing.</span></span>

## <a name="simplify-debugging"></a><span data-ttu-id="6ac24-128">ทำให้การดีบักง่าย</span><span class="sxs-lookup"><span data-stu-id="6ac24-128">Simplify debugging</span></span>

<span data-ttu-id="6ac24-129">ตัวแปรยังสามารถช่วยคุณในการดีบักสูตรอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="6ac24-129">Variables can also help you debug a formula.</span></span> <span data-ttu-id="6ac24-130">หากต้องการทดสอบนิพจน์ที่กำหนดให้กับตัวแปร คุณจะเขียนนิพจน์ RETURN ชั่วคราวอีกครั้งเพื่อแสดงผลตัวแปร</span><span class="sxs-lookup"><span data-stu-id="6ac24-130">To test an expression assigned to a variable, you temporarily rewrite the RETURN expression to output the variable.</span></span>

<span data-ttu-id="6ac24-131">ข้อกำหนดหน่วยวัดต่อไปนี้ส่งกลับเฉพาะตัวแปร **SalesPriorYear** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6ac24-131">The following measure definition returns only the **SalesPriorYear** variable.</span></span> <span data-ttu-id="6ac24-132">สังเกตว่ามีการคอมเมนต์นิพจน์ RETURN ที่ตั้งใจไว้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="6ac24-132">Notice how it comments-out the intended RETURN expression.</span></span> <span data-ttu-id="6ac24-133">เทคนิคนี้ช่วยให้คุณสามารถย้อนกลับได้ง่ายเมื่อการดีบักเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6ac24-133">This technique allows you to easily revert it back once your debugging is complete.</span></span>

```dax
Sales YoY Growth % =
VAR SalesPriorYear =
    CALCULATE([Sales], PARALLELPERIOD('Date'[Date], -12, MONTH))
RETURN
    --DIVIDE(([Sales] - SalesPriorYear), SalesPriorYear)
    SalesPriorYear
```

## <a name="reduce-complexity"></a><span data-ttu-id="6ac24-134">ลดความซับซ้อน</span><span class="sxs-lookup"><span data-stu-id="6ac24-134">Reduce complexity</span></span>

<span data-ttu-id="6ac24-135">ใน DAX เวอร์ชันก่อนหน้า ยังไม่สนับสนุนตัวแปร</span><span class="sxs-lookup"><span data-stu-id="6ac24-135">In earlier versions of DAX, variables were not yet supported.</span></span> <span data-ttu-id="6ac24-136">ซึ่งต้องใช้นิพจน์ที่ซับซ้อนที่นำบริบทตัวกรองใหม่เข้ามาใช้เพื่อใช้ฟังก์ชัน [EARLIER](/dax/earlier-function-dax) หรือ [ EARLIEST](/dax/earliest-function-dax) DAX ในการอ้างอิงบริบทตัวกรองชั้นนอก</span><span class="sxs-lookup"><span data-stu-id="6ac24-136">Complex expressions that introduced new filter contexts were required to use the [EARLIER](/dax/earlier-function-dax) or [EARLIEST](/dax/earliest-function-dax) DAX functions to reference outer filter contexts.</span></span> <span data-ttu-id="6ac24-137">แต่น่าเสียดายที่ผู้สร้างแบบจำลองข้อมูลพบว่าฟังก์ชันเหล่านี้เข้าใจและใช้งานยาก</span><span class="sxs-lookup"><span data-stu-id="6ac24-137">Unfortunately, data modelers found these functions difficult to understand and use.</span></span>

<span data-ttu-id="6ac24-138">ตัวแปรจะถูกประเมินนอกตัวกรองของคุณโดยใช้นิพจน์ RETURN เสมอ</span><span class="sxs-lookup"><span data-stu-id="6ac24-138">Variables are always evaluated outside the filters your RETURN expression applies.</span></span> <span data-ttu-id="6ac24-139">ด้วยเหตุผลนี้เมื่อคุณใช้ตัวแปรภายในบริบทตัวกรองที่ปรับเปลี่ยนแล้ว จะได้ผลลัพธ์เช่นเดียวกับฟังก์ชัน EARLIEST</span><span class="sxs-lookup"><span data-stu-id="6ac24-139">For this reason, when you use a variable within a modified filter context, it achieves the same result as the EARLIEST function.</span></span> <span data-ttu-id="6ac24-140">ดังนั้นจึงสามารถหลีกเลี่ยงการใช้ฟังก์ชัน EARLIER หรือ EARLIEST ได้</span><span class="sxs-lookup"><span data-stu-id="6ac24-140">The use of the EARLIER or EARLIEST functions can therefore be avoided.</span></span> <span data-ttu-id="6ac24-141">ซึ่งหมายความว่าตอนนี้คุณสามารถเขียนสูตรที่มีความซับซ้อนน้อยลง และทำความเข้าใจได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="6ac24-141">It means you can now write formulas that are less complex, and that are easier to understand.</span></span>

<span data-ttu-id="6ac24-142">พิจารณาคำจำกัดความคอลัมน์จากการคำนวณต่อไปนี้ที่ถูกเพิ่มลงในตาราง **Subcategory**</span><span class="sxs-lookup"><span data-stu-id="6ac24-142">Consider the following calculated column definition added to the **Subcategory** table.</span></span> <span data-ttu-id="6ac24-143">ซึ่งจะประเมินอันดับสำหรับแต่ละหมวดหมู่ย่อยของผลิตภัณฑ์ตามค่าคอลัมน์ **Subcategory Sales**</span><span class="sxs-lookup"><span data-stu-id="6ac24-143">It evaluates a rank for each product subcategory based on the **Subcategory Sales** column values.</span></span>

```dax
Subcategory Sales Rank =
COUNTROWS(
    FILTER(
        Subcategory,
        EARLIER(Subcategory[Subcategory Sales]) < Subcategory[Subcategory Sales]
    )
) + 1
```

<span data-ttu-id="6ac24-144">ฟังก์ชัน EARLIER ถูกใช้เพื่ออ้างถึงค่าคอลัมน์ **Subcategory Sales**_ในบริบทแถวปัจจุบัน_</span><span class="sxs-lookup"><span data-stu-id="6ac24-144">The EARLIER function is used to refer to the **Subcategory Sales** column value _in the current row context_.</span></span>

<span data-ttu-id="6ac24-145">คุณสามารถปรับปรุงคำจำกัดความคอลัมน์จากการคำนวณให้ดีขึ้นได้โดยใช้ตัวแปรแทนฟังก์ชัน EARLIER</span><span class="sxs-lookup"><span data-stu-id="6ac24-145">The calculated column definition can be improved by using a variable instead of the EARLIER function.</span></span> <span data-ttu-id="6ac24-146">ตัวแปร **CurrentSubcategorySales** เก็บค่าคอลัมน์ **Subcategory Sales**_ในบริบทแถวปัจจุบัน_ และนิพจน์ RETURN จะใช้ตัวแปรดังกล่าวภายในบริบทตัวกรองที่ปรับเปลี่ยนแล้ว</span><span class="sxs-lookup"><span data-stu-id="6ac24-146">The **CurrentSubcategorySales** variable stores the **Subcategory Sales** column value _in the current row context_, and the RETURN expression uses it within a modified filter context.</span></span>

```dax
Subcategory Sales Rank =
VAR CurrentSubcategorySales = Subcategory[Subcategory Sales]
RETURN
    COUNTROWS(
        FILTER(
            Subcategory,
            CurrentSubcategorySales < Subcategory[Subcategory Sales]
        )
    ) + 1
```

## <a name="next-steps"></a><span data-ttu-id="6ac24-147">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="6ac24-147">Next steps</span></span>

<span data-ttu-id="6ac24-148">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6ac24-148">For more information about this article, check out the following resources:</span></span>

- [<span data-ttu-id="6ac24-149">ข้อมูลอ้างอิงเกี่ยวกับ Data Analysis Expressions (DAX)</span><span class="sxs-lookup"><span data-stu-id="6ac24-149">Data Analysis Expressions (DAX) Reference</span></span>](/dax/)
- <span data-ttu-id="6ac24-150">บทความ [VAR](/dax/var-dax) DAX</span><span class="sxs-lookup"><span data-stu-id="6ac24-150">[VAR](/dax/var-dax) DAX article</span></span>
- <span data-ttu-id="6ac24-151">เส้นทางการเรียนรู้: [ใช้ DAX ใน Power BI Desktop](/learn/paths/dax-power-bi/)</span><span class="sxs-lookup"><span data-stu-id="6ac24-151">Learning path: [Use DAX in Power BI Desktop](/learn/paths/dax-power-bi/)</span></span>
- <span data-ttu-id="6ac24-152">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6ac24-152">Questions?</span></span> [<span data-ttu-id="6ac24-153">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="6ac24-153">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="6ac24-154">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="6ac24-154">Suggestions?</span></span> [<span data-ttu-id="6ac24-155">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="6ac24-155">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com)