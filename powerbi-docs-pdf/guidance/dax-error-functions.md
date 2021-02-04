---
title: 'DAX: การใช้ฟังก์ชันข้อผิดพลาดที่เหมาะสม'
description: คำแนะนำเกี่ยวกับเมื่อใดที่ควรใช้ฟังก์ชันข้อผิดพลาด DAX
author: peter-myers
ms.author: v-pemyer
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 09/26/2019
ms.openlocfilehash: fd071fad18580074ce42c990db7f048ce2ad8c2d
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96394048"
---
# <a name="dax-appropriate-use-of-error-functions"></a><span data-ttu-id="107a6-103">DAX: การใช้ฟังก์ชันข้อผิดพลาดที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="107a6-103">DAX: Appropriate use of error functions</span></span>

<span data-ttu-id="107a6-104">ในฐานะผู้สร้างแบบจำลองข้อมูล เมื่อคุณเขียนนิพจน์ DAX ที่อาจทำให้เกิดข้อผิดพลาดในการประเมินระยะเวลา คุณสามารถพิจารณาการใช้ฟังก์ชัน DAX ที่เป็นประโยชน์สองอย่างได้</span><span class="sxs-lookup"><span data-stu-id="107a6-104">As a data modeler, when you write a DAX expression that might raise an evaluation-time error, you can consider using two helpful DAX functions.</span></span>

- <span data-ttu-id="107a6-105">ฟังก์ชัน [ISERROR](/dax/iserror-function-dax) ซึ่งจะใช้นิพจน์เดียวและแสดงค่า TRUE หากนิพจน์ดังกล่าวมีข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="107a6-105">The [ISERROR](/dax/iserror-function-dax) function, which takes a single expression and returns TRUE if that expression results in error.</span></span>
- <span data-ttu-id="107a6-106">ฟังก์ชัน [IFERROR](/dax/iferror-function-dax) ซึ่งจะรับสองนิพจน์</span><span class="sxs-lookup"><span data-stu-id="107a6-106">The [IFERROR](/dax/iferror-function-dax) function, which takes two expressions.</span></span> <span data-ttu-id="107a6-107">หากนิพจน์แรกมีข้อผิดพลาด ค่าสำหรับนิพจน์ที่สองจะถูกส่งกลับ</span><span class="sxs-lookup"><span data-stu-id="107a6-107">Should the first expression result in error, the value for the second expression is returned.</span></span> <span data-ttu-id="107a6-108">ที่จริงแล้วเป็นการปรับการซ้อนฟังก์ชัน ISERROR ภายในฟังก์ชัน [IF](/dax/if-function-dax)</span><span class="sxs-lookup"><span data-stu-id="107a6-108">It is in fact a more optimized implementation of nesting the ISERROR function inside an [IF](/dax/if-function-dax) function.</span></span>

<span data-ttu-id="107a6-109">อย่างไรก็ตาม นอกจากที่ฟังก์ชันเหล่านี้จะเป็นประโยชน์และสามารถสนับสนุนการเขียนนิพจน์ที่เข้าใจได้ง่ายแล้ว ยังสามารถลดประสิทธิภาพการคำนวณได้อย่างมาก</span><span class="sxs-lookup"><span data-stu-id="107a6-109">However, while these functions can be helpful and can contribute to writing easy-to-understand expressions, they can also significantly degrade the performance of calculations.</span></span> <span data-ttu-id="107a6-110">ซึ่งอาจเกิดขึ้นเนื่องจากฟังก์ชันเหล่านี้เพิ่มจำนวนการสแกนกลไกจัดการที่เก็บข้อมูลที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="107a6-110">It can happen because these functions increase the number of storage engine scans required.</span></span>

<span data-ttu-id="107a6-111">ข้อผิดพลาดในการประเมินระยะเวลาส่วนใหญ่จะเกิดขึ้นเนื่องจาก BLANK หรือค่าศูนย์ที่ไม่คาดคิด หรือการแปลงประเภทข้อมูลที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="107a6-111">Most evaluation-time errors are due to unexpected BLANKs or zero values, or invalid data type conversion.</span></span>

## <a name="recommendations"></a><span data-ttu-id="107a6-112">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="107a6-112">Recommendations</span></span>

<span data-ttu-id="107a6-113">เป็นการดีกว่าที่จะหลีกเลี่ยงการใช้ฟังก์ชัน ISERROR และ IFERROR</span><span class="sxs-lookup"><span data-stu-id="107a6-113">It's better to avoid using the ISERROR and IFERROR functions.</span></span> <span data-ttu-id="107a6-114">ให้ใช้กลยุทธ์การป้องกันเมื่อทำการพัฒนาแบบจำลองและการเขียนนิพจน์แทน</span><span class="sxs-lookup"><span data-stu-id="107a6-114">Instead, apply defensive strategies when developing the model and writing expressions.</span></span> <span data-ttu-id="107a6-115">กลยุทธ์สามารถรวมถึง:</span><span class="sxs-lookup"><span data-stu-id="107a6-115">Strategies can include:</span></span>

- <span data-ttu-id="107a6-116">**ตรวจสอบให้แน่ใจว่าโหลดข้อมูลคุณภาพลงในแบบจำลอง:** ใช้การแปลง Power Query เพื่อลบหรือแทนที่ค่าที่ไม่ถูกต้องหรือที่ขาดหายไป และตั้งค่าประเภทข้อมูลที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="107a6-116">**Ensuring quality data is loaded into the model:** Use Power Query transformations to remove or substitute invalid or missing values, and to set correct data types.</span></span> <span data-ttu-id="107a6-117">นอกจากนี้ ยังสามารถใช้การแปลง Power Query เพื่อกรองแถวเมื่อเกิดข้อผิดพลาด เช่น การแปลงข้อมูลที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="107a6-117">A Power Query transformation can also be used to filter rows when errors, like invalid data conversion, occur.</span></span>

    <span data-ttu-id="107a6-118">ยังสามารถควบคุมคุณภาพข้อมูลได้โดยการตั้งค่าคอลัมน์แบบจำลองคุณสมบัติ **เป็นค่าว่างได้** เพื่อปิด ซึ่งจะล้มเหลวในการรีเฟรชข้อมูลหากมีช่องว่าง</span><span class="sxs-lookup"><span data-stu-id="107a6-118">Data quality can also be controlled by setting the model column **Is Nullable** property to Off, which will fail the data refresh should BLANKs be encountered.</span></span> <span data-ttu-id="107a6-119">หากเกิดความล้มเหลวนี้ ข้อมูลที่โหลดเนื่องจากการรีเฟรชที่สำเร็จจะยังคงอยู่ในตาราง</span><span class="sxs-lookup"><span data-stu-id="107a6-119">If this failure occurs, data loaded as a result of a successful refresh will remain in the tables.</span></span>
- <span data-ttu-id="107a6-120">**การใช้ฟังก์ชัน IF:** นิพจน์การทดสอบเชิงตรรกะของฟังก์ชัน IF สามารถกำหนดได้ว่าผลลัพธ์ของข้อผิดพลาดจะเกิดขึ้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="107a6-120">**Using the IF function:** The IF function logical test expression can determine whether an error result would occur.</span></span> <span data-ttu-id="107a6-121">หมายเหตุ ฟังก์ชันนี้อาจส่งผลให้มีการสแกนกลไกจัดการที่เก็บข้อมูลเพิ่มเติม แต่มีแนวโน้มที่จะทำงานได้ดียิ่งขึ้นเนื่องจากไม่มีข้อผิดพลาดที่จำเป็นต้องเกิดขึ้น อย่างฟังก์ชัน ISERROR และ IFERROR</span><span class="sxs-lookup"><span data-stu-id="107a6-121">Note, like the ISERROR and IFERROR functions, this function can result in additional storage engine scans, but will likely perform better than them as no error needs to be raised.</span></span>
- <span data-ttu-id="107a6-122">**การใช้ฟังก์ชันที่ทนต่อข้อผิดพลาด:** ฟังก์ชัน DAX บางฟังก์ชันจะทดสอบและชดเชยเงื่อนไขของข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="107a6-122">**Using error-tolerant functions:** Some DAX functions will test and compensate for error conditions.</span></span> <span data-ttu-id="107a6-123">ฟังก์ชันเหล่านี้ช่วยให้คุณสามารถใส่ผลลัพธ์สำรองที่จะถูกส่งกลับแทน</span><span class="sxs-lookup"><span data-stu-id="107a6-123">These functions allow you to enter an alternate result that would be returned instead.</span></span> <span data-ttu-id="107a6-124">ฟังก์ชัน [DIVIDE](/dax/divide-function-dax) คือตัวอย่างหนึ่งดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="107a6-124">The [DIVIDE](/dax/divide-function-dax) function is one such example.</span></span> <span data-ttu-id="107a6-125">สำหรับคำแนะนำเพิ่มเติมเกี่ยวกับฟังก์ชันนี้ ให้อ่าน [DAX: บทความฟังก์ชัน DIVIDE เทียบกับตัวดำเนินการหาร (/)](dax-divide-function-operator.md)</span><span class="sxs-lookup"><span data-stu-id="107a6-125">For additional guidance about this function, read the [DAX: DIVIDE function vs divide operator (/)](dax-divide-function-operator.md) article.</span></span>

## <a name="example"></a><span data-ttu-id="107a6-126">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="107a6-126">Example</span></span>

<span data-ttu-id="107a6-127">นิพจน์หน่วยวัดต่อไปนี้จะทดสอบว่ามีข้อผิดพลาดเกิดขึ้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="107a6-127">The following measure expression tests whether an error would be raised.</span></span> <span data-ttu-id="107a6-128">ซึ่งจะส่งกลับค่าว่างในครั้งนี้ (ซึ่งเป็นกรณีที่คุณไม่ได้ให้ฟังก์ชัน IF ที่มีนิพจน์ค่าหากเป็นเท็จ)</span><span class="sxs-lookup"><span data-stu-id="107a6-128">It returns BLANK in this instance (which is the case when you do not provide the IF function with a value-if-false expression).</span></span>

```dax
Profit Margin
= IF(ISERROR([Profit] / [Sales]))
```

<span data-ttu-id="107a6-129">เวอร์ชันถัดไปนี้ของนิพจน์หน่วยวัดได้รับการปรับปรุงโดยใช้ฟังก์ชัน IFERROR แทนฟังก์ชัน IF และ ISERROR</span><span class="sxs-lookup"><span data-stu-id="107a6-129">This next version of the measure expression has been improved by using the IFERROR function in place of the IF and ISERROR functions.</span></span>

```dax
Profit Margin
= IFERROR([Profit] / [Sales], BLANK())
```

<span data-ttu-id="107a6-130">อย่างไรก็ตาม เวอร์ชันสุดท้ายของนิพจน์หน่วยวัดนี้ได้ผลลัพธ์เดียวกัน แต่มีประสิทธิภาพและสละสลวยมากกว่า</span><span class="sxs-lookup"><span data-stu-id="107a6-130">However, this final version of the measure expression achieves the same outcome, yet more efficiently and elegantly.</span></span>

```dax
Profit Margin
= DIVIDE([Profit], [Sales])
```

## <a name="next-steps"></a><span data-ttu-id="107a6-131">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="107a6-131">Next steps</span></span>

<span data-ttu-id="107a6-132">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="107a6-132">For more information about this article, check out the following resources:</span></span>

- [<span data-ttu-id="107a6-133">ข้อมูลอ้างอิงเกี่ยวกับ Data Analysis Expressions (DAX)</span><span class="sxs-lookup"><span data-stu-id="107a6-133">Data Analysis Expressions (DAX) Reference</span></span>](/dax/)

- <span data-ttu-id="107a6-134">เส้นทางการเรียนรู้: [ใช้ DAX ใน Power BI Desktop](/learn/paths/dax-power-bi/)</span><span class="sxs-lookup"><span data-stu-id="107a6-134">Learning path: [Use DAX in Power BI Desktop](/learn/paths/dax-power-bi/)</span></span>
- <span data-ttu-id="107a6-135">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="107a6-135">Questions?</span></span> [<span data-ttu-id="107a6-136">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="107a6-136">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="107a6-137">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="107a6-137">Suggestions?</span></span> [<span data-ttu-id="107a6-138">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="107a6-138">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com)