---
title: 'DAX: ใช้ SELECTEDVALUE แทน VALUES'
description: คำแนะนำเกี่ยวกับเมื่อใดที่คุณควรใช้ฟังก์ชัน SELECTEDVALUE
author: peter-myers
ms.author: v-pemyer
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 11/20/2019
ms.openlocfilehash: 1925333b935209484855dff444542a20040a0f6a
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96394232"
---
# <a name="dax-use-selectedvalue-instead-of-values"></a><span data-ttu-id="fd968-103">DAX: ใช้ SELECTEDVALUE แทน VALUES</span><span class="sxs-lookup"><span data-stu-id="fd968-103">DAX: Use SELECTEDVALUE instead of VALUES</span></span>

<span data-ttu-id="fd968-104">ในฐานะผู้สร้างแบบจำลองข้อมูล บางครั้งคุณอาจจำเป็นต้องเขียนนิพจน์ DAX ที่ทดสอบว่ามีการกรองคอลัมน์จากค่าเฉพาะหรือไม่</span><span class="sxs-lookup"><span data-stu-id="fd968-104">As a data modeler, sometimes you might need to write a DAX expression that tests whether a column is filtered by a specific value.</span></span>

<span data-ttu-id="fd968-105">ใน DAX รุ่นก่อนหน้า คุณสามารถบรรลุข้อกำหนดนี้ได้อย่างมั่นคงโดยใช้รูปแบบที่เกี่ยวข้องกับฟังก์ชัน DAX สามฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="fd968-105">In earlier versions of DAX, this requirement was safely achieved by using a pattern involving three DAX functions.</span></span> <span data-ttu-id="fd968-106">ฟังก์ชันดังกล่าวคือ [IF](/dax/if-function-dax), [HASONEVALUE](/dax/hasonevalue-function-dax) และ [VALUES](/dax/values-function-dax)</span><span class="sxs-lookup"><span data-stu-id="fd968-106">The functions are [IF](/dax/if-function-dax), [HASONEVALUE](/dax/hasonevalue-function-dax) and [VALUES](/dax/values-function-dax).</span></span> <span data-ttu-id="fd968-107">ข้อกำหนดหน่วยวัดต่อไปนี้แสดงถึงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="fd968-107">The following measure definition presents an example.</span></span> <span data-ttu-id="fd968-108">ซึ่งคำนวณค่าภาษีขาย แต่เฉพาะสำหรับยอดขายที่เกิดจากลูกค้าชาวออสเตรเลียเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fd968-108">It calculates the sales tax amount, but only for sales made to Australian customers.</span></span>

```dax
Australian Sales Tax =
IF(
    HASONEVALUE(Customer[Country-Region]),
    IF(
        VALUES(Customer[Country-Region]) = "Australia",
        [Sales] * 0.10
    )
)
```

<span data-ttu-id="fd968-109">ในตัวอย่าง ฟังก์ชัน HASONEVALUE ส่งกลับ TRUE เฉพาะเมื่อค่าเดียวกรองคอลัมน์ **Country-Region**</span><span class="sxs-lookup"><span data-stu-id="fd968-109">In the example, the HASONEVALUE function returns TRUE only when a single value filters the **Country-Region** column.</span></span> <span data-ttu-id="fd968-110">เมื่อค่าเป็น TRUE ฟังก์ชัน VALUES จะถูกเปรียบเทียบกับข้อความตัวอักษร "Australia"</span><span class="sxs-lookup"><span data-stu-id="fd968-110">When it's TRUE, the VALUES function is compared to the literal text "Australia".</span></span> <span data-ttu-id="fd968-111">เมื่อฟังก์ชัน VALUES ส่งกลับ TRUE หน่วยวัด **Sales (ยอดขาย)** จะถูกคูณด้วย 0.10 (คิดเป็น 10%)</span><span class="sxs-lookup"><span data-stu-id="fd968-111">When the VALUES function returns TRUE, the **Sales** measure is multiplied by 0.10 (representing 10%).</span></span> <span data-ttu-id="fd968-112">ถ้าฟังก์ชัน HASONEVALUE ส่งกลับค่า FALSE เนื่องจากมีค่ามากกว่าหนึ่งค่ากรองคอลัมน์ ดังนั้นฟังก์ชัน IF แรกจะส่งกลับ BLANK</span><span class="sxs-lookup"><span data-stu-id="fd968-112">If the HASONEVALUE function returns FALSE—because more than one value filters the column—the first IF function returns BLANK.</span></span>

<span data-ttu-id="fd968-113">การใช้ HASONEVALUE เป็นเทคนิคเชิงป้องกัน</span><span class="sxs-lookup"><span data-stu-id="fd968-113">The use of the HASONEVALUE is a defensive technique.</span></span> <span data-ttu-id="fd968-114">ซึ่งเทคนิคนี้จำเป็นเนื่องจากเป็นไปได้ว่าค่าหลายค่าจะกรองคอลัมน์ **Country-Region**</span><span class="sxs-lookup"><span data-stu-id="fd968-114">It's required because it's possible that multiple values filter the **Country-Region** column.</span></span> <span data-ttu-id="fd968-115">ในกรณีนี้ ฟังก์ชัน VALUES จะส่งกลับตารางหลายแถว</span><span class="sxs-lookup"><span data-stu-id="fd968-115">In this case, the VALUES function returns a table of multiple rows.</span></span> <span data-ttu-id="fd968-116">การเปรียบเทียบตารางหลายแถวกับค่าสเกลาร์ทำให้เกิดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="fd968-116">Comparing a table of multiple rows to a scalar value results in an error.</span></span>

## <a name="recommendation"></a><span data-ttu-id="fd968-117">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="fd968-117">Recommendation</span></span>

<span data-ttu-id="fd968-118">เราขอแนะนำให้คุณใช้ฟังก์ชัน [SELECTEDVALUE](/dax/selectedvalue-function)</span><span class="sxs-lookup"><span data-stu-id="fd968-118">We recommend that you use the [SELECTEDVALUE](/dax/selectedvalue-function) function.</span></span> <span data-ttu-id="fd968-119">ซึ่งจะทำให้ได้ผลลัพธ์เดียวกันกับรูปแบบที่อธิบายไว้ในบทความนี้ แต่มีประสิทธิภาพและสวยงามยิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="fd968-119">It achieves the same outcome as the pattern described in this article, yet more efficiently and elegantly.</span></span>

<span data-ttu-id="fd968-120">การใช้ฟังก์ชัน SELECTEDVALUE ข้อกำหนดหน่วยวัดตัวอย่างจะถูกเขียนใหม่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="fd968-120">Using the SELECTEDVALUE function, the example measure definition is now rewritten.</span></span>

```dax
Australian Sales Tax =
IF(
    SELECTEDVALUE(Customer[Country-Region]) = "Australia",
    [Sales] * 0.10
)
```

> [!TIP]
> <span data-ttu-id="fd968-121">ซึ่งอาจเป็นไปได้ที่จะส่งผ่านค่า _ผลลัพธ์สำรอง_ ลงในฟังก์ชัน SELECTEDVALUE</span><span class="sxs-lookup"><span data-stu-id="fd968-121">It's possible to pass an _alternate result_ value into the SELECTEDVALUE function.</span></span> <span data-ttu-id="fd968-122">ฟังก์ชันจะส่งกลับค่าผลลัพธ์สำรองเมื่อไม่มีตัวกรองหรือตัวกรองหลายรายการถูกนำไปใช้กับคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="fd968-122">The alternate result value is returned when either no filters—or multiple filters—are applied to the column.</span></span>

## <a name="next-steps"></a><span data-ttu-id="fd968-123">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="fd968-123">Next steps</span></span>

<span data-ttu-id="fd968-124">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fd968-124">For more information about this article, check out the following resources:</span></span>

- [<span data-ttu-id="fd968-125">ข้อมูลอ้างอิงเกี่ยวกับ Data Analysis Expressions (DAX)</span><span class="sxs-lookup"><span data-stu-id="fd968-125">Data Analysis Expressions (DAX) Reference</span></span>](/dax/)
- <span data-ttu-id="fd968-126">เส้นทางการเรียนรู้: [ใช้ DAX ใน Power BI Desktop](/learn/paths/dax-power-bi/)</span><span class="sxs-lookup"><span data-stu-id="fd968-126">Learning path: [Use DAX in Power BI Desktop](/learn/paths/dax-power-bi/)</span></span>
- <span data-ttu-id="fd968-127">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="fd968-127">Questions?</span></span> [<span data-ttu-id="fd968-128">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="fd968-128">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="fd968-129">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="fd968-129">Suggestions?</span></span> [<span data-ttu-id="fd968-130">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="fd968-130">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com)