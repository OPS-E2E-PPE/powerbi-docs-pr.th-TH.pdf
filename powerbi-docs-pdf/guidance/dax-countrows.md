---
title: 'DAX: ใช้ COUNTROWS แทน COUNT'
description: คำแนะนำเกี่ยวกับเมื่อใดที่ควรใช้ฟังก์ชัน COUNTROWS
author: peter-myers
ms.author: v-pemyer
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 11/23/2019
ms.openlocfilehash: 1a2b8c6450cfd855a0018fb64dd385a0db6e350f
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96394209"
---
# <a name="dax-use-countrows-instead-of-count"></a><span data-ttu-id="fbb99-103">DAX: ใช้ COUNTROWS แทน COUNT</span><span class="sxs-lookup"><span data-stu-id="fbb99-103">DAX: Use COUNTROWS instead of COUNT</span></span>

<span data-ttu-id="fbb99-104">ในฐานะผู้สร้างแบบจำลองข้อมูล บางครั้งคุณอาจจำเป็นต้องเขียนนิพจน์ DAX ที่นับแถวของตาราง</span><span class="sxs-lookup"><span data-stu-id="fbb99-104">As a data modeler, sometimes you might need to write a DAX expression that counts table rows.</span></span> <span data-ttu-id="fbb99-105">ตารางอาจเป็นตารางของแบบจำลองหรือนิพจน์ที่ส่งกลับตาราง</span><span class="sxs-lookup"><span data-stu-id="fbb99-105">The table could be a model table or an expression that returns a table.</span></span>

<span data-ttu-id="fbb99-106">คุณสามารถบรรลุความต้องการของคุณได้ด้วยสองวิธี</span><span class="sxs-lookup"><span data-stu-id="fbb99-106">Your requirement can be achieved in two ways.</span></span> <span data-ttu-id="fbb99-107">คุณสามารถใช้ฟังก์ชัน [COUNT](/dax/count-function-dax) เพื่อนับค่าคอลัมน์ หรือคุณสามารถใช้ฟังก์ชัน [COUNTROWS](/dax/countrows-function-dax) เพื่อนับแถวของตารางได้</span><span class="sxs-lookup"><span data-stu-id="fbb99-107">You can use the [COUNT](/dax/count-function-dax) function to count column values, or you can use the [COUNTROWS](/dax/countrows-function-dax) function to count table rows.</span></span> <span data-ttu-id="fbb99-108">ทั้งสองฟังก์ชันจะทำให้เกิดผลลัพธ์เดียวกัน ซึ่งคอลัมน์ที่นับไม่มี BLANK</span><span class="sxs-lookup"><span data-stu-id="fbb99-108">Both functions will achieve the same result, providing that the counted column contains no BLANKs.</span></span>

<span data-ttu-id="fbb99-109">ข้อกำหนดหน่วยวัดต่อไปนี้แสดงถึงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="fbb99-109">The following measure definition presents an example.</span></span> <span data-ttu-id="fbb99-110">ซึ่งคำนวณจำนวนค่าคอลัมน์ **OrderDate**</span><span class="sxs-lookup"><span data-stu-id="fbb99-110">It calculates the number of **OrderDate** column values.</span></span>

```dax
Sales Orders =
COUNT(Sales[OrderDate])
```

<span data-ttu-id="fbb99-111">ระบุว่าความละเอียดของตาราง **ยอดขาย (Sales)** คือหนึ่งแถวต่อคำสั่งขาย และคอลัมน์ **OrderDate** ไม่มี BLANK จากนั้นหน่วยวัดจะส่งกลับผลลัพธ์ที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="fbb99-111">Providing that the granularity of the **Sales** table is one row per sales order, and the **OrderDate** column does not contain BLANKs, then the measure will return a correct result.</span></span>

<span data-ttu-id="fbb99-112">อย่างไรก็ตามข้อกำหนดหน่วยวัดต่อไปนี้เป็นโซลูชันที่ดีกว่า</span><span class="sxs-lookup"><span data-stu-id="fbb99-112">However, the following measure definition is a better solution.</span></span>

```dax
Sales Orders =
COUNTROWS(Sales)
```

<span data-ttu-id="fbb99-113">มีสามเหตุผลที่ทำให้ข้อกำหนดหน่วยวัดที่สองดีกว่า:</span><span class="sxs-lookup"><span data-stu-id="fbb99-113">There are three reasons why the second measure definition is better:</span></span>

- <span data-ttu-id="fbb99-114">มีประสิทธิภาพมากกว่า และดังนั้นจึงทำงานได้ดียิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="fbb99-114">It's more efficient, and so it will perform better.</span></span>
- <span data-ttu-id="fbb99-115">ไม่พิจารณา BLANK ที่อยู่ในคอลัมน์ใดก็ตามของตาราง</span><span class="sxs-lookup"><span data-stu-id="fbb99-115">It doesn't consider BLANKs contained in any column of the table.</span></span>
- <span data-ttu-id="fbb99-116">ความตั้งใจของสูตรมีความชัดเจนมากขึ้นจนถึงจุดที่อธิบายตัวเองได้</span><span class="sxs-lookup"><span data-stu-id="fbb99-116">The intention of formula is clearer, to the point of being self-describing.</span></span>

## <a name="recommendation"></a><span data-ttu-id="fbb99-117">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="fbb99-117">Recommendation</span></span>

<span data-ttu-id="fbb99-118">เมื่อคุณต้องการนับแถวของตาราง เราขอแนะนำให้คุณใช้ฟังก์ชัน COUNTROWS เสมอ</span><span class="sxs-lookup"><span data-stu-id="fbb99-118">When it's your intention to count table rows, we recommend that you always use the COUNTROWS function.</span></span>

## <a name="next-steps"></a><span data-ttu-id="fbb99-119">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="fbb99-119">Next steps</span></span>

<span data-ttu-id="fbb99-120">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fbb99-120">For more information about this article, check out the following resources:</span></span>

- [<span data-ttu-id="fbb99-121">ข้อมูลอ้างอิงเกี่ยวกับ Data Analysis Expressions (DAX)</span><span class="sxs-lookup"><span data-stu-id="fbb99-121">Data Analysis Expressions (DAX) Reference</span></span>](/dax/)
- <span data-ttu-id="fbb99-122">เส้นทางการเรียนรู้: [ใช้ DAX ใน Power BI Desktop](/learn/paths/dax-power-bi/)</span><span class="sxs-lookup"><span data-stu-id="fbb99-122">Learning path: [Use DAX in Power BI Desktop](/learn/paths/dax-power-bi/)</span></span>
- <span data-ttu-id="fbb99-123">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="fbb99-123">Questions?</span></span> [<span data-ttu-id="fbb99-124">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="fbb99-124">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="fbb99-125">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="fbb99-125">Suggestions?</span></span> [<span data-ttu-id="fbb99-126">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="fbb99-126">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com)