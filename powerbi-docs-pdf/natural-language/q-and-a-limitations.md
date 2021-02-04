---
title: ข้อจำกัดของระบบถามตอบของ Power BI
description: ข้อจำกัดปัจจุบันของระบบถามตอบของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: conceptual
ms.date: 09/09/2020
ms.openlocfilehash: 6ad81bc88ee559fa08400b5ed8a74dd1a9b6051f
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410033"
---
# <a name="limitations-of-power-bi-qa"></a><span data-ttu-id="230cd-103">ข้อจำกัดของระบบถามตอบของ Power BI</span><span class="sxs-lookup"><span data-stu-id="230cd-103">Limitations of Power BI Q&A</span></span>

<span data-ttu-id="230cd-104">ระบบถามตอบของ Power BI มีข้อจำกัดบางอย่างอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="230cd-104">Power BI Q&A currently has some limitations.</span></span>

## <a name="data-sources"></a><span data-ttu-id="230cd-105">แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="230cd-105">Data sources</span></span>

### <a name="supported-data-sources"></a><span data-ttu-id="230cd-106">แหล่งข้อมูลที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="230cd-106">Supported data sources</span></span>

<span data-ttu-id="230cd-107">ระบบถามตอบของ Power BI จะรองรับการกำหนดค่าแหล่งข้อมูลต่อไปนี้ในบริการของ Power BI:</span><span class="sxs-lookup"><span data-stu-id="230cd-107">Power BI Q&A supports the following configurations of data sources in the Power BI service:</span></span>

- <span data-ttu-id="230cd-108">โหมดการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="230cd-108">Import mode</span></span>
- <span data-ttu-id="230cd-109">เชื่อมต่อสดกับ Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="230cd-109">Live connect to Azure Analysis Services</span></span>
- <span data-ttu-id="230cd-110">เชื่อมต่อแบบสดกับ SQL Server Analysis Services (ที่มีเกตเวย์)</span><span class="sxs-lookup"><span data-stu-id="230cd-110">Live connect to SQL Server Analysis Services (with a gateway)</span></span>
- <span data-ttu-id="230cd-111">ชุดข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="230cd-111">Power BI datasets.</span></span>

<span data-ttu-id="230cd-112">ในการกำหนดค่าเหล่านี้แต่ละรายการ ยังรองรับการรักษาความปลอดภัยระดับแถวด้วย</span><span class="sxs-lookup"><span data-stu-id="230cd-112">In each of these configurations, row-level security is also supported.</span></span>

<span data-ttu-id="230cd-113">**การสนับสนุน DirectQuery สำหรับคำถามและคำตอบ** (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="230cd-113">**DirectQuery support for Q&A** (preview)</span></span>

<span data-ttu-id="230cd-114">โดยในขณะนี้คำถามและคำตอบจะรองรับแหล่งข้อมูล SQL DirectQuery ซึ่งประกอบด้วย SQL Server 2019, Azure SQL Database และ Azure Synapse Analytics</span><span class="sxs-lookup"><span data-stu-id="230cd-114">Q&A now supports SQL DirectQuery sources, including SQL Server 2019, Azure SQL Database, and Azure Synapse Analytics.</span></span> <span data-ttu-id="230cd-115">คุณสามารถใช้คำถามและคำตอบเพื่อถามคำถามภาษาธรรมชาติกับแหล่งข้อมูลเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="230cd-115">You can use Q&A to ask natural-language questions against these data sources.</span></span> <span data-ttu-id="230cd-116">มีการเปลี่ยนแปลงเล็กน้อยในหนึ่งในการทำงานของคำถามและคำตอบเมื่ออยู่ในโหมด DirectQuery นั่นคือ: หลังจากที่คุณพิมพ์คำถามของคุณแล้ว คุณเลือกปุ่ม **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="230cd-116">There's one small change to the behavior of Q&A when it's in DirectQuery mode: After you type your question, you select the **Submit** button.</span></span> <span data-ttu-id="230cd-117">การเปลี่ยนแปลงนี้จะป้องกันไม่ให้แหล่งข้อมูล DirectQuery มีคิวรีที่ไม่จำเป็นมากจนเกินไปในขณะที่คุณพิมพ์</span><span class="sxs-lookup"><span data-stu-id="230cd-117">This change prevents overloading the DirectQuery source with unnecessary queries as you type.</span></span>

<span data-ttu-id="230cd-118">คำถามและคำตอบไม่รองรับแหล่งข้อมูล DirectQuery อื่น</span><span class="sxs-lookup"><span data-stu-id="230cd-118">Other DirectQuery sources aren't supported for Q&A.</span></span> <span data-ttu-id="230cd-119">เราจะไม่บล็อกคำถามและคำตอบทั้งหมด หากคุณมีแหล่งข้อมูล DirectQuery อื่น ๆ ในชุดข้อมูลของคุณ แต่อาจตอบคำถามบางข้อไม่ถูกต้องหรือตอบกลับมาเป็นข้อผิดพลาดได้</span><span class="sxs-lookup"><span data-stu-id="230cd-119">We don’t block Q&A altogether if you have other DirectQuery sources in your dataset, but some questions may not be answered correctly or return errors.</span></span>

### <a name="data-sources-not-supported"></a><span data-ttu-id="230cd-120">ไม่รองรับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="230cd-120">Data sources not supported</span></span>

<span data-ttu-id="230cd-121">ในปัจจุบัน ระบบถามตอบของ Power BI ยังไม่รองรับการกำหนดค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="230cd-121">Power BI Q&A currently does not support the following configurations:</span></span>

- <span data-ttu-id="230cd-122">การรักษาความปลอดภัยระดับออบเจ็กต์ที่มีแหล่งข้อมูลชนิดใดก็ตาม</span><span class="sxs-lookup"><span data-stu-id="230cd-122">Object level security with any type of data source</span></span>
- <span data-ttu-id="230cd-123">โมเดลแบบรวม</span><span class="sxs-lookup"><span data-stu-id="230cd-123">Composite models</span></span>
- <span data-ttu-id="230cd-124">บริการการรายงาน</span><span class="sxs-lookup"><span data-stu-id="230cd-124">Reporting Services</span></span> 

## <a name="tooling-limitations"></a><span data-ttu-id="230cd-125">ข้อจำกัดของการใช้เครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="230cd-125">Tooling limitations</span></span>

<span data-ttu-id="230cd-126">กล่องโต้ตอบการใช้เครื่องมือใหม่ช่วยให้ผู้ใช้สามารถปรับแต่งและปรับปรุงภาษาธรรมชาติในระบบถามตอบ</span><span class="sxs-lookup"><span data-stu-id="230cd-126">The new tooling dialog allows users to customize and improve the natural language in Q&A.</span></span> <span data-ttu-id="230cd-127">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับการใช้เครื่องมือ ให้อ่าน [คำแนะนำเกี่ยวกับการใช้เครื่องมือถามตอบ](q-and-a-tooling-intro.md)</span><span class="sxs-lookup"><span data-stu-id="230cd-127">To learn more about tooling, read the [intro to Q&A tooling](q-and-a-tooling-intro.md).</span></span>

## <a name="review-question-limitations"></a><span data-ttu-id="230cd-128">ข้อจำกัดของคำถามตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="230cd-128">Review question limitations</span></span>

<span data-ttu-id="230cd-129">คำถามตรวจสอบจะเก็บเฉพาะคำถามที่ถามกับแบบจำลองข้อมูลของคุณไว้นานถึง 28 วัน</span><span class="sxs-lookup"><span data-stu-id="230cd-129">The review questions only store questions asked against your data model for up to 28 days.</span></span> <span data-ttu-id="230cd-130">เมื่อใช้ความสามารถของคำถามตรวจสอบใหม่ คุณอาจสังเกตเห็นว่าคำถามบางข้อไม่ได้รับการบันทึกไว้</span><span class="sxs-lookup"><span data-stu-id="230cd-130">When using the new review questions capability, you may notice some questions aren't recorded.</span></span> <span data-ttu-id="230cd-131">ซึ่งไม่มีการบันทึกโดยการออกแบบ เนื่องจากกลไกจัดการภาษาธรรมชาติดำเนินการตามชุดขั้นตอนการล้างข้อมูลเพื่อให้มั่นใจว่าการเคาะแป้นพิมพ์ที่ผู้ใช้กระทำทุกครั้งจะไม่ถูกบันทึกหรือแสดง</span><span class="sxs-lookup"><span data-stu-id="230cd-131">They aren't recorded by design, as the natural language engine performs a series of data cleansing steps to ensure every key stroke from a user isn't recorded or shown.</span></span>

<span data-ttu-id="230cd-132">ผู้ดูแลระบบของ Power BI สามารถใช้การตั้งค่าผู้เช่าเพื่อจัดการความสามารถในการจัดเก็บคำถาม</span><span class="sxs-lookup"><span data-stu-id="230cd-132">Power BI administrators can use the tenant settings to manage the ability to store questions.</span></span> <span data-ttu-id="230cd-133">สิทธิ์ต่าง ๆ จะขึ้นอยู่กับกลุ่มความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="230cd-133">Permissions are based on security groups.</span></span> 

<span data-ttu-id="230cd-134">ผู้ใช้ยังสามารถป้องกันไม่ให้บันทึกคำถามของพวกเขาโดยเลือก **การตั้งค่า** > **ทั่วไป** และยกเลิกการเลือก **อนุญาตให้ระบบถามตอบบันทึกการออกเสียงของฉัน**</span><span class="sxs-lookup"><span data-stu-id="230cd-134">Users can also keep their questions from being recorded by selecting **Settings** > **General** and deselecting **Allow Q&A to record my utterance**.</span></span> 

## <a name="teach-qa-limitations"></a><span data-ttu-id="230cd-135">ข้อจำกัดของการสอนระบบถามตอบ</span><span class="sxs-lookup"><span data-stu-id="230cd-135">Teach Q&A limitations</span></span>

<span data-ttu-id="230cd-136">การสอนระบบถามตอบช่วยให้คุณสามารถแก้ไขข้อผิดพลาดสองชนิดได้แก่:</span><span class="sxs-lookup"><span data-stu-id="230cd-136">Teach Q&A allows you to fix two types of errors:</span></span>

- <span data-ttu-id="230cd-137">กำหนดคำสำหรับเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="230cd-137">Assign a word to a field.</span></span>
- <span data-ttu-id="230cd-138">กำหนดคำที่เป็นเงื่อนไขตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="230cd-138">Assign a word a filter condition.</span></span>

<span data-ttu-id="230cd-139">ขณะนี้เราไม่รองรับการกำหนดคำศัพท์ที่รู้จักใหม่หรือกำหนดเงื่อนไขหรือวลีประเภทอื่น</span><span class="sxs-lookup"><span data-stu-id="230cd-139">Currently we don't support redefining a recognized term or defining other types of conditions or phrases.</span></span> <span data-ttu-id="230cd-140">นอกจากนี้เมื่อกำหนดเงื่อนไขการกรอง คุณสามารถใช้ภาษาได้เพียงบางส่วนที่จำกัดไว้เท่านั้น ซึ่งรวมถึง:</span><span class="sxs-lookup"><span data-stu-id="230cd-140">Also, when defining filtering conditions, you can only use a limited subset of language, including:</span></span>

- <span data-ttu-id="230cd-141">ประเทศซึ่งก็คือสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="230cd-141">Country which is USA</span></span>
- <span data-ttu-id="230cd-142">ประเทศซึ่งไม่ใช่สหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="230cd-142">Country which is not USA</span></span>
- <span data-ttu-id="230cd-143">ผลิตภัณฑ์ > 100</span><span class="sxs-lookup"><span data-stu-id="230cd-143">Products > 100</span></span>
- <span data-ttu-id="230cd-144">ผลิตภัณฑ์มากกว่า 100</span><span class="sxs-lookup"><span data-stu-id="230cd-144">Products greater than 100</span></span>
- <span data-ttu-id="230cd-145">ผลิตภัณฑ์ = 100</span><span class="sxs-lookup"><span data-stu-id="230cd-145">Products = 100</span></span>
- <span data-ttu-id="230cd-146">ผลิตภัณฑ์เท่ากับ 100</span><span class="sxs-lookup"><span data-stu-id="230cd-146">Products is 100</span></span>
- <span data-ttu-id="230cd-147">ผลิตภัณฑ์ < 100</span><span class="sxs-lookup"><span data-stu-id="230cd-147">Products < 100</span></span>
- <span data-ttu-id="230cd-148">ผลิตภัณฑ์น้อยกว่า 100</span><span class="sxs-lookup"><span data-stu-id="230cd-148">Products smaller than 100</span></span>

> [!NOTE]
> <span data-ttu-id="230cd-149">การใช้เครื่องมือถามตอบจะรองรับเฉพาะโหมดการนำเข้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="230cd-149">Q&A Tooling only supports import mode.</span></span> <span data-ttu-id="230cd-150">ซึ่งไม่รองรับการเชื่อมต่อไปยังแหล่งข้อมูลภายในองค์กรหรือ Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="230cd-150">It doesn't yet support connecting to an on-premises or Azure Analysis Services data source.</span></span> <span data-ttu-id="230cd-151">ข้อจำกัดปัจจุบันนี้จะหายไปจาก Power BI ในรุ่นที่ออกมาภายหลัง</span><span class="sxs-lookup"><span data-stu-id="230cd-151">This current limitation will be removed in subsequent releases of Power BI.</span></span>

### <a name="statements-not-supported"></a><span data-ttu-id="230cd-152">ไม่รองรับคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="230cd-152">Statements not supported</span></span>

- <span data-ttu-id="230cd-153">ไม่ได้สนับสนุนหลายเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="230cd-153">Multiple conditions aren't supported.</span></span> <span data-ttu-id="230cd-154">สำหรับการแก้ปัญหาเฉพาะหน้า ให้สร้างคอลัมน์จากการคำนวณ DAX ที่ประเมินบูลีนของคำสั่งแบบหลายเงื่อนไขและใช้เขตข้อมูลนี้แทน</span><span class="sxs-lookup"><span data-stu-id="230cd-154">As a workaround, create a DAX calculated column that evaluates a multi-condition statement Boolean and use this field instead.</span></span>
- <span data-ttu-id="230cd-155">หากคุณไม่ได้ระบุเงื่อนไขตัวกรองเมื่อระบบถามตอบพร้อมท์สำหรับชุดย่อยของข้อมูล คุณจะไม่สามารถบันทึกคำจำกัดความได้แม้ว่าคำสั่งทั้งหมดจะไม่มีขีดเส้นใต้สีแดงก็ตาม</span><span class="sxs-lookup"><span data-stu-id="230cd-155">If you don't specify a filter condition when Q&A prompts for a subset of data, you can't save the definition, even if the entire statement has no red underlines.</span></span>

## <a name="next-steps"></a><span data-ttu-id="230cd-156">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="230cd-156">Next steps</span></span>

<span data-ttu-id="230cd-157">มีแนวปฏิบัติที่ดีที่สุดหลายประการสำหรับการพัฒนากลไกจัดการภาษาธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="230cd-157">There are a number of best practices for improving the natural language engine.</span></span> <span data-ttu-id="230cd-158">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [แนวทางปฏิบัติที่ดีที่สุดสำหรับการถามตอบ](q-and-a-best-practices.md)</span><span class="sxs-lookup"><span data-stu-id="230cd-158">For more information, [Q&A best practices](q-and-a-best-practices.md).</span></span>
