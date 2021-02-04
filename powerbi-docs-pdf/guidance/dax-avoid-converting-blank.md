---
title: 'DAX: หลีกเลี่ยงการแปลง BLANK ไปเป็นค่า'
description: คำแนะนำในการแปลง BLANK ไปเป็นค่า
author: peter-myers
ms.author: v-pemyer
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 11/24/2019
ms.openlocfilehash: 20686615c58015040349138ffd49b544c5dac70a
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96394278"
---
# <a name="dax-avoid-converting-blanks-to-values"></a><span data-ttu-id="aea5b-103">DAX: หลีกเลี่ยงการแปลง BLANK ไปเป็นค่า</span><span class="sxs-lookup"><span data-stu-id="aea5b-103">DAX: Avoid converting BLANKs to values</span></span>

<span data-ttu-id="aea5b-104">ในฐานะผู้สร้างแบบจำลองข้อมูล เมื่อเขียนนิพจน์หน่วยวัด คุณอาจเจอกรณีที่ไม่สามารถส่งกลับค่าที่มีนัยสำคัญ</span><span class="sxs-lookup"><span data-stu-id="aea5b-104">As a data modeler, when writing measure expressions you might come across cases where a meaningful value can't be returned.</span></span> <span data-ttu-id="aea5b-105">ในกรณีเหล่านี้ คุณอาจถูกล่อลวงให้คืนค่า เช่น ศูนย์แทน</span><span class="sxs-lookup"><span data-stu-id="aea5b-105">In these instances, you may be tempted to return a value—like zero—instead.</span></span> <span data-ttu-id="aea5b-106">เราแนะนำให้คุณพิจารณาอย่างรอบคอบว่าการออกแบบนี้มีประสิทธิภาพและใช้งานได้จริงหรือไม่</span><span class="sxs-lookup"><span data-stu-id="aea5b-106">We suggest you carefully determine whether this design is efficient and practical.</span></span>

<span data-ttu-id="aea5b-107">พิจารณาข้อกำหนดหน่วยวัดต่อไปนี้ที่แปลงผลลัพธ์ BLANK เป็นศูนย์อย่างชัดเจน</span><span class="sxs-lookup"><span data-stu-id="aea5b-107">Consider the following measure definition that explicitly converts BLANK results to zero.</span></span>

```dax
Sales (No Blank) =
IF(
    ISBLANK([Sales]),
    0,
    [Sales]
)
```

<span data-ttu-id="aea5b-108">พิจารณาข้อกำหนดหน่วยวัดอื่นที่แปลงผลลัพธ์ BLANK เป็นศูนย์ด้วย</span><span class="sxs-lookup"><span data-stu-id="aea5b-108">Consider another measure definition that also converts BLANK results to zero.</span></span>

```dax
Profit Margin =
DIVIDE([Profit], [Sales], 0)
```

<span data-ttu-id="aea5b-109">ฟังก์ชัน [DIVIDE](/dax/divide-function-dax) หารหน่วยวัด **กำไร** ด้วยหน่วยวัด **ยอดขาย**</span><span class="sxs-lookup"><span data-stu-id="aea5b-109">The [DIVIDE](/dax/divide-function-dax) function divides the **Profit** measure by the **Sales** measure.</span></span> <span data-ttu-id="aea5b-110">หากผลลัพธ์เป็นศูนย์หรือ BLANK อาร์กิวเมนต์ที่สาม - ผลลัพธ์อื่น (ซึ่งเป็นทางเลือก) - ถูกส่งกลับ</span><span class="sxs-lookup"><span data-stu-id="aea5b-110">Should the result be zero or BLANK, the third argument—the alternate result (which is optional)—is returned.</span></span> <span data-ttu-id="aea5b-111">ในตัวอย่างนี้ เนื่องจากมีการส่งผ่านศูนย์เป็นผลลัพธ์ทางเลือก ดังนั้นหน่วยวัดนั้นจึงรับประกันว่าจะส่งกลับค่าเสมอ</span><span class="sxs-lookup"><span data-stu-id="aea5b-111">In this example, because zero is passed as the alternate result, the measure is guaranteed to always return a value.</span></span>

<span data-ttu-id="aea5b-112">การออกแบบหน่วยวัดเหล่านี้จะไม่มีประสิทธิภาพและนำไปสู่การออกแบบรายงานที่ไม่ดี</span><span class="sxs-lookup"><span data-stu-id="aea5b-112">These measure designs are inefficient and lead to poor report designs.</span></span>

<span data-ttu-id="aea5b-113">เมื่อมีการเพิ่มการออกแบบเหล่านี้ลงในวิชวลรายงาน Power BI จะพยายามเรียกใช้การจัดกลุ่มทั้งหมดภายในบริบทตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="aea5b-113">When they're added to a report visual, Power BI attempts to retrieve all groupings within the filter context.</span></span> <span data-ttu-id="aea5b-114">การประเมินผลและการดึงผลลัพธ์ของคิวรีที่มีขนาดใหญ่มักจะนำไปสู่การแสดงรายงานที่ล่าช้า</span><span class="sxs-lookup"><span data-stu-id="aea5b-114">The evaluation and retrieval of large query results often leads to slow report rendering.</span></span> <span data-ttu-id="aea5b-115">ตัวอย่างหน่วยวัดแต่ละหน่วยจะเปลี่ยนการคำนวณแบบเบาบางไปเป็นการคำนวณที่หนาแน่น บังคับให้ Power BI ใช้หน่วยความจำมากกว่าที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="aea5b-115">Each example measure effectively turns a sparse calculation into a dense one, forcing Power BI to use more memory than necessary.</span></span>

<span data-ttu-id="aea5b-116">นอกจากนี้ การจัดกลุ่มมากเกินไปมักจะครอบงำผู้ใช้รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="aea5b-116">Also, too many groupings often overwhelm your report users.</span></span>

<span data-ttu-id="aea5b-117">เรามาดูกันว่าจะเกิดอะไรขึ้นเมื่อมีการเพิ่มหน่วยวัด **อัตรากำไร** ในตารางวิชวล การจัดกลุ่มตามลูกค้า</span><span class="sxs-lookup"><span data-stu-id="aea5b-117">Let's see what happens when the **Profit Margin** measure is added to a table visual, grouping by customer.</span></span>

![<span data-ttu-id="aea5b-118">ภาพหน้าจอของ Power BI Desktop ที่แสดงวิชวลตารางของข้อมูลที่มีหนึ่งแถวต่อลูกค้า</span><span class="sxs-lookup"><span data-stu-id="aea5b-118">Screenshot of Power B I Desktop showing table visual of data with one row per customer.</span></span> <span data-ttu-id="aea5b-119">ค่ายอดขายจะว่างเปล่าและค่าอัตราส่วนกำไรเป็นศูนย์เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="aea5b-119">Sales values are BLANK and Profit Margin values are zero per cent.</span></span> ](media/dax-avoid-converting-blank/table-visual-poor.png)

<span data-ttu-id="aea5b-120">วิชวลของตารางแสดงจำนวนแถวมากมาย</span><span class="sxs-lookup"><span data-stu-id="aea5b-120">The table visual displays an overwhelming number of rows.</span></span> <span data-ttu-id="aea5b-121">(ในความเป็นจริงแล้วมีลูกค้า 18,484 รายในแบบจำลอง ดังนั้นตารางจึงพยายามแสดงทั้งหมด) โปรดสังเกตว่าลูกค้าในมุมมองยังไม่ได้ทำให้เกิดยอดขายใดเลย</span><span class="sxs-lookup"><span data-stu-id="aea5b-121">(There are in fact 18,484 customers in the model, and so the table attempts to display all of them.) Notice that the customers in view haven't achieved any sales.</span></span> <span data-ttu-id="aea5b-122">ทว่าเนื่องจากหน่วยวัด **อัตรากำไร** จะส่งกลับค่าเสมอ ดังนั้นจึงมีการแสดงค่า</span><span class="sxs-lookup"><span data-stu-id="aea5b-122">Yet, because the **Profit Margin** measure always returns a value, they are displayed.</span></span>

> [!NOTE]
> <span data-ttu-id="aea5b-123">เมื่อมีจุดข้อมูลที่ต้องการแสดงในวิชวลมากเกินไป Power BI อาจใช้กลยุทธ์ด้านการลดขนาดข้อมูลเพื่อลบหรือสรุปผลลัพธ์คิวรีขนาดใหญ่</span><span class="sxs-lookup"><span data-stu-id="aea5b-123">When there are too many data points to display in a visual, Power BI may use data reduction strategies to remove or summarize large query results.</span></span> <span data-ttu-id="aea5b-124">สำหรับข้อมูลเพิ่มเติม โปรดดู [ข้อจำกัดและกลยุทธ์ของจุดข้อมูลตามรูปแบบของวิชวล](../visuals/power-bi-data-points.md)</span><span class="sxs-lookup"><span data-stu-id="aea5b-124">For more information, see [Data point limits and strategies by visual type](../visuals/power-bi-data-points.md).</span></span>

<span data-ttu-id="aea5b-125">เรามาดูว่าจะเกิดอะไรขึ้นเมื่อมีการปรับปรุงข้อกำหนดหน่วยวัด **อัตรากำไร**</span><span class="sxs-lookup"><span data-stu-id="aea5b-125">Let's see what happens when the **Profit Margin** measure definition is improved.</span></span> <span data-ttu-id="aea5b-126">ในตอนนี้จะส่งกลับค่าเฉพาะเมื่อหน่วยวัด **ยอดขาย** ไม่เป็น BLANK (หรือศูนย์)</span><span class="sxs-lookup"><span data-stu-id="aea5b-126">It now returns a value only when the **Sales** measure isn't BLANK (or zero).</span></span>

```dax
Profit Margin =
DIVIDE([Profit], [Sales])
```

<span data-ttu-id="aea5b-127">ขณะนี้วิชวลตารางจะแสดงเฉพาะลูกค้าที่สร้างยอดขายภายในบริบทตัวกรองปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="aea5b-127">The table visual now displays only customers who have made sales within the current filter context.</span></span> <span data-ttu-id="aea5b-128">หน่วยวัดที่ปรับปรุงใหม่ส่งผลให้ผู้ใช้รายงานของคุณมีประสบการณ์ที่มีประสิทธิภาพมากขึ้นและใช้งานได้จริง</span><span class="sxs-lookup"><span data-stu-id="aea5b-128">The improved measure results in a more efficient and practical experience for your report users.</span></span>

![ภาพหน้าจอของ Power BI Desktop ที่แสดงวิชวลตารางของข้อมูลที่มีเนื้อหาที่ถูกกรอง](media/dax-avoid-converting-blank/table-visual-good.png)

> [!TIP]
> <span data-ttu-id="aea5b-130">เมื่อจำเป็น คุณสามารถกำหนดค่าวิชวลเพื่อแสดงการจัดกลุ่มทั้งหมด (ที่ส่งกลับค่าหรือค่า BLANK) ภายในบริบทของตัวกรองได้โดยการเปิดใช้งานตัวเลือก [แสดงรายการโดยไม่มีข้อมูล](../create-reports/desktop-show-items-no-data.md)</span><span class="sxs-lookup"><span data-stu-id="aea5b-130">When necessary, you can configure a visual to display all groupings (that return values or BLANK) within the filter context by enabling the [Show Items With No Data](../create-reports/desktop-show-items-no-data.md) option.</span></span>

## <a name="recommendation"></a><span data-ttu-id="aea5b-131">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="aea5b-131">Recommendation</span></span>

<span data-ttu-id="aea5b-132">เราขอแนะนำให้หน่วยวัดของคุณส่งกลับค่า BLANK เมื่อไม่สามารถส่งกลับค่าที่มีนัยสำคัญ</span><span class="sxs-lookup"><span data-stu-id="aea5b-132">We recommend that your measures return BLANK when a meaningful value cannot be returned.</span></span>

<span data-ttu-id="aea5b-133">วิธีการออกแบบนี้มีประสิทธิภาพ ช่วยให้ Power BI สามารถแสดงรายงานได้เร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="aea5b-133">This design approach is efficient, allowing Power BI to render reports faster.</span></span> <span data-ttu-id="aea5b-134">นอกจากนี้การส่งกลับค่า BLANK จะดีกว่าเนื่องจากวิชวลบรายงานตามค่าเริ่มต้นจะลบการจัดกลุ่มออกไปเมื่อผลสรุปเป็น BLANK</span><span class="sxs-lookup"><span data-stu-id="aea5b-134">Also, returning BLANK is better because report visuals—by default—eliminate groupings when summarizations are BLANK.</span></span>

## <a name="next-steps"></a><span data-ttu-id="aea5b-135">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="aea5b-135">Next steps</span></span>

<span data-ttu-id="aea5b-136">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="aea5b-136">For more information about this article, check out the following resources:</span></span>

- [<span data-ttu-id="aea5b-137">ข้อมูลอ้างอิงเกี่ยวกับ Data Analysis Expressions (DAX)</span><span class="sxs-lookup"><span data-stu-id="aea5b-137">Data Analysis Expressions (DAX) Reference</span></span>](/dax/)
- <span data-ttu-id="aea5b-138">เส้นทางการเรียนรู้: [ใช้ DAX ใน Power BI Desktop](/learn/paths/dax-power-bi/)</span><span class="sxs-lookup"><span data-stu-id="aea5b-138">Learning path: [Use DAX in Power BI Desktop](/learn/paths/dax-power-bi/)</span></span>
- <span data-ttu-id="aea5b-139">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="aea5b-139">Questions?</span></span> [<span data-ttu-id="aea5b-140">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="aea5b-140">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="aea5b-141">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="aea5b-141">Suggestions?</span></span> [<span data-ttu-id="aea5b-142">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="aea5b-142">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com)