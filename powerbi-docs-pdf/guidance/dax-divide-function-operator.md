---
title: 'DAX: ฟังก์ชันการแบ่งเทียบกับตัวดำเนินการหาร (/)'
description: คำแนะนำเมื่อใช้ฟังก์ชันการแบ่ง DAX
author: peter-myers
ms.author: v-pemyer
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 09/09/2019
ms.openlocfilehash: ece1c0d939ef521b20142acb753de7b7554e870a
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96394140"
---
# <a name="dax-divide-function-vs-divide-operator-"></a><span data-ttu-id="7a0f7-103">DAX: ฟังก์ชันการแบ่งเทียบกับตัวดำเนินการหาร (/)</span><span class="sxs-lookup"><span data-stu-id="7a0f7-103">DAX: DIVIDE function vs divide operator (/)</span></span>

<span data-ttu-id="7a0f7-104">ในฐานะผู้สร้างแบบจำลองข้อมูล เมื่อคุณเขียนนิพจน์ DAX เพื่อแบ่งตัวเศษตามตัวหาร คุณสามารถเลือกใช้ฟังก์ชัน [DIVIDE](/dax/divide-function-dax) หรือตัวดำเนินการหาร (/ - เครื่องหมายทับ)</span><span class="sxs-lookup"><span data-stu-id="7a0f7-104">As a data modeler, when you write a DAX expression to divide a numerator by a denominator, you can choose to use the [DIVIDE](/dax/divide-function-dax) function or the divide operator (/ - forward slash).</span></span>

<span data-ttu-id="7a0f7-105">เมื่อใช้ฟังก์ชันการแบ่ง คุณจะต้องส่งผ่านนิพจน์ตัวเลขและตัวหาร</span><span class="sxs-lookup"><span data-stu-id="7a0f7-105">When using the DIVIDE function, you must pass in numerator and denominator expressions.</span></span> <span data-ttu-id="7a0f7-106">อีกทางเลือกหนึ่งคือ คุณสามารถส่งผ่านค่าที่แสดง _ผลลัพธ์สำรอง_ ได้</span><span class="sxs-lookup"><span data-stu-id="7a0f7-106">Optionally, you can pass in a value that represents an _alternate result_.</span></span>

```dax
DIVIDE(<numerator>, <denominator> [,<alternateresult>])
```

<span data-ttu-id="7a0f7-107">ฟังก์ชัน DIVIDE ได้รับการออกแบบขึ้นมาเพื่อจัดการกับการหารโดยอัตโนมัติในกรณีที่มีค่าเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="7a0f7-107">The DIVIDE function was designed to automatically handle division by zero cases.</span></span> <span data-ttu-id="7a0f7-108">หากไม่มีการส่งผ่านผลลัพธ์สำรอง และตัวหารมีค่าเป็นศูนย์หรือว่างเปล่า ฟังก์ชันจะส่งคืนค่าว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="7a0f7-108">If an alternate result is not passed in, and the denominator is zero or BLANK, the function returns BLANK.</span></span> <span data-ttu-id="7a0f7-109">เมื่อมีการส่งผ่านผลลัพธ์สำรอง ผลลัพธ์ดังกล่าวจะถูกส่งกลับแทน BLANK</span><span class="sxs-lookup"><span data-stu-id="7a0f7-109">When an alternate result is passed in, it's returned instead of BLANK.</span></span>

<span data-ttu-id="7a0f7-110">ฟังก์ชันการแบ่งนั้นมีประโยชน์มาก เนื่องจากฟังก์ชันนี้จะบันทึกนิพจน์ของคุณจากการทดสอบค่าตัวหารครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="7a0f7-110">The DIVIDE function is convenient because it saves your expression from having to first test the denominator value.</span></span> <span data-ttu-id="7a0f7-111">นอกจากนี้ ฟังก์ชันนี้ยังได้รับการปรับให้เหมาะสมสำหรับการทดสอบค่าตัวหารมากกว่าฟังก์ชัน [IF](/dax/if-function-dax)</span><span class="sxs-lookup"><span data-stu-id="7a0f7-111">The function is also better optimized for testing the denominator value than the [IF](/dax/if-function-dax) function.</span></span> <span data-ttu-id="7a0f7-112">การเพิ่มประสิทธิภาพการทำงานมีความสำคัญ เนื่องจากการตรวจสอบการหารด้วยศูนย์นั้นมีราคาแพง</span><span class="sxs-lookup"><span data-stu-id="7a0f7-112">The performance gain is significant since checking for division by zero is expensive.</span></span> <span data-ttu-id="7a0f7-113">นอกจากนี้ การใช้ DIVIDE ยังส่งผลให้นิพจน์นั้นกระชับและสละสลวยมากขึ้นด้วย</span><span class="sxs-lookup"><span data-stu-id="7a0f7-113">Further using DIVIDE results in a more concise and elegant expression.</span></span>

## <a name="example"></a><span data-ttu-id="7a0f7-114">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="7a0f7-114">Example</span></span>

<span data-ttu-id="7a0f7-115">นิพจน์การวัดต่อไปนี้สร้างการหารที่ปลอดภัย แต่ยังเกี่ยวข้องกับการใช้ฟังก์ชัน DAX สี่รายการ</span><span class="sxs-lookup"><span data-stu-id="7a0f7-115">The following measure expression produces a safe division, but it involves using four DAX functions.</span></span>

```dax
Profit Margin =
IF(
    OR(
        ISBLANK([Sales]),
        [Sales] == 0
    ),
    BLANK(),
    [Profit] / [Sales]
)
```

<span data-ttu-id="7a0f7-116">นิพจน์หน่วยวัดนี้ได้ผลลัพธ์เดียวกัน แต่มีประสิทธิภาพและสละสลายมากกว่า</span><span class="sxs-lookup"><span data-stu-id="7a0f7-116">This measure expression achieves the same outcome, yet more efficiently and elegantly.</span></span>

```dax
Profit Margin =
DIVIDE([Profit], [Sales])
```

## <a name="recommendations"></a><span data-ttu-id="7a0f7-117">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="7a0f7-117">Recommendations</span></span>

<span data-ttu-id="7a0f7-118">เราขอแนะนำให้คุณใช้ฟังก์ชันการแบ่งเมื่อใดก็ตามที่ตัวหารเป็นนิพจน์ _ซึ่งสามารถ_ ส่งกลับค่าศูนย์หรือค่าว่างเปล่าได้</span><span class="sxs-lookup"><span data-stu-id="7a0f7-118">We recommend that you use the DIVIDE function whenever the denominator is an expression that _could_ return zero or BLANK.</span></span>

<span data-ttu-id="7a0f7-119">ในกรณีที่ตัวหารเป็นค่าคงที่ เราขอแนะนำให้คุณใช้ตัวดำเนินการหาร</span><span class="sxs-lookup"><span data-stu-id="7a0f7-119">In the case that the denominator is a constant value, we recommend that you use the divide operator.</span></span> <span data-ttu-id="7a0f7-120">ในกรณีนี้ ระบบจะรับประกันความสำเร็จในการแบ่ง และนิพจน์ของคุณจะทำงานได้ดียิ่งขึ้นเนื่องจากฟังก์ชันนี้จะหลีกเลี่ยงการทดสอบที่ไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="7a0f7-120">In this case, the division is guaranteed to succeed, and your expression will perform better because it will avoid unnecessary testing.</span></span>

<span data-ttu-id="7a0f7-121">ให้พิจารณาอย่างรอบคอบว่าฟังก์ชัน DIVIDE ควรแสดงค่าสำรองหรือไม่</span><span class="sxs-lookup"><span data-stu-id="7a0f7-121">Carefully consider whether the DIVIDE function should return an alternate value.</span></span> <span data-ttu-id="7a0f7-122">สำหรับหน่วยวัด โดยปกติแล้วการแสดงค่าว่างถือเป็นการออกแบบที่ดีกว่า</span><span class="sxs-lookup"><span data-stu-id="7a0f7-122">For measures, it's usually a better design that they return BLANK.</span></span> <span data-ttu-id="7a0f7-123">การแสดง BLANK ดีกว่าเนื่องจากวิชวลบรายงานตามค่าเริ่มต้นจะลบการจัดกลุ่มออกไปเมื่อผลสรุปเป็นค่าว่าง</span><span class="sxs-lookup"><span data-stu-id="7a0f7-123">Returning BLANK is better because report visuals—by default—eliminate groupings when summarizations are BLANK.</span></span> <span data-ttu-id="7a0f7-124">ซึ่งช่วยให้วิชวลมุ่งเน้นไปยังกลุ่มที่มีข้อมูลอยู่</span><span class="sxs-lookup"><span data-stu-id="7a0f7-124">It allows the visual to focus attention on groups where data exists.</span></span> <span data-ttu-id="7a0f7-125">เมื่อจำเป็น คุณสามารถกำหนดการแสดงผลด้วยภาพเพื่อแสดงกลุ่มทั้งหมด (ที่ส่งกลับค่าหรือค่าว่างเปล่า) ภายในบริบทของตัวกรองได้โดยการเปิดใช้งานตัวเลือก [แสดงรายการโดยไม่มีข้อมูล](../create-reports/desktop-show-items-no-data.md)</span><span class="sxs-lookup"><span data-stu-id="7a0f7-125">When necessary, you can configure the visual to display all groups (that return values or BLANK) within the filter context by enabling the [Show items with no data](../create-reports/desktop-show-items-no-data.md) option.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7a0f7-126">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="7a0f7-126">Next steps</span></span>

<span data-ttu-id="7a0f7-127">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7a0f7-127">For more information about this article, check out the following resources:</span></span>

- [<span data-ttu-id="7a0f7-128">ข้อมูลอ้างอิงเกี่ยวกับ Data Analysis Expressions (DAX)</span><span class="sxs-lookup"><span data-stu-id="7a0f7-128">Data Analysis Expressions (DAX) Reference</span></span>](/dax/)
- <span data-ttu-id="7a0f7-129">เส้นทางการเรียนรู้: [ใช้ DAX ใน Power BI Desktop](/learn/paths/dax-power-bi/)</span><span class="sxs-lookup"><span data-stu-id="7a0f7-129">Learning path: [Use DAX in Power BI Desktop](/learn/paths/dax-power-bi/)</span></span>
- <span data-ttu-id="7a0f7-130">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="7a0f7-130">Questions?</span></span> [<span data-ttu-id="7a0f7-131">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="7a0f7-131">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="7a0f7-132">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="7a0f7-132">Suggestions?</span></span> [<span data-ttu-id="7a0f7-133">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="7a0f7-133">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com)