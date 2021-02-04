---
title: คำแนะนำการรักษาความปลอดภัยระดับแถว (RLS) ใน Power BI Desktop
description: คำแนะนำสำหรับการบังคับใช้การรักษาความปลอดภัยระดับแถว (RLS) ในแบบจำลองข้อมูลของคุณด้วย Power BI Desktop
author: paulinbar
ms.author: painbar
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 06/18/2020
ms.openlocfilehash: 3c8290391d549f4510b4f6ea6ee0fd596500045e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410102"
---
# <a name="row-level-security-rls-guidance-in-power-bi-desktop"></a><span data-ttu-id="e0708-103">คำแนะนำการรักษาความปลอดภัยระดับแถว (RLS) ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e0708-103">Row-level security (RLS) guidance in Power BI Desktop</span></span>

<span data-ttu-id="e0708-104">บทความนี้มุ่งเป้าหมายไปที่เรื่อง ตัวสร้างแบบจำลองข้อมูลนำเข้าที่ทำงานกับ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e0708-104">This article targets you as a data modeler working with Power BI Desktop.</span></span> <span data-ttu-id="e0708-105">สิ่งนั้นได้อธิบายการออกแบบที่ดีสำหรับการบังคับใช้การรักษาความปลอดภัยระดับแถว (RLS) ในแบบจำลองข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="e0708-105">It describes good design practices for enforcing row-levels security (RLS) in your data models.</span></span>

<span data-ttu-id="e0708-106">เป็นสิ่งสำคัญที่ต้องทำความเข้าใจตัวกรอง RLS _แถวของตาราง_</span><span class="sxs-lookup"><span data-stu-id="e0708-106">It's important to understand RLS filters _table rows_.</span></span> <span data-ttu-id="e0708-107">สิ่งนั้นไม่สามารถกำหนดค่าให้จำกัดการเข้าถึงวัตถุของแบบจำลอง รวมถึงตาราง คอลัมน์หรือการวัด</span><span class="sxs-lookup"><span data-stu-id="e0708-107">They can't be configured to restrict access to model objects, including tables, columns, or measures.</span></span>

> [!NOTE]
> <span data-ttu-id="e0708-108">บทความนี้ไม่ได้อธิบาย RLS หรือวิธีการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="e0708-108">This article doesn't describe RLS or how to set it up.</span></span> <span data-ttu-id="e0708-109">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การจำกัดการเข้าถึงข้อมูลด้วยการรักษาความปลอดภัยระดับแถว (RLS) สำหรับ Power BI Desktop](../create-reports/desktop-rls.md)</span><span class="sxs-lookup"><span data-stu-id="e0708-109">For more information, see [Restrict data access with row-level security (RLS) for Power BI Desktop](../create-reports/desktop-rls.md).</span></span>
>
> <span data-ttu-id="e0708-110">นอกจากนี้จะยังไม่ได้ครอบคลุมถึงการบังคับใช้ RLS ในการเชื่อมต่อแบบสดไปยังแบบจำลองที่โฮสต์ภายนอกด้วย Azure Analysis Services หรือ SQL Server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="e0708-110">Also, it doesn't cover enforcing RLS in live connections to external-hosted models with Azure Analysis Services or SQL Server Analysis Services.</span></span> <span data-ttu-id="e0708-111">ในกรณีเหล่านี้ RLS จะถูกบังคับใช้โดย Analysis Services</span><span class="sxs-lookup"><span data-stu-id="e0708-111">In these cases, RLS is enforced by Analysis Services.</span></span> <span data-ttu-id="e0708-112">เมื่อ Power BI เชื่อมต่อโดยใช้การล็อกอินเพียงครั้งเดียว (SSO), Analysis Services จะบังคับใช้ RLS (เว้นแต่บัญชีจะมีสิทธิ์ของผู้ดูแลระบบ)</span><span class="sxs-lookup"><span data-stu-id="e0708-112">When Power BI connects using single-sign on (SSO), Analysis Services will enforce RLS (unless the account has admin privileges).</span></span>

## <a name="create-roles"></a><span data-ttu-id="e0708-113">สร้างบทบาท</span><span class="sxs-lookup"><span data-stu-id="e0708-113">Create roles</span></span>

<span data-ttu-id="e0708-114">สิ่งนั้นเป็นไปได้ที่จะสร้างได้หลายบทบาท</span><span class="sxs-lookup"><span data-stu-id="e0708-114">It's possible to create multiple roles.</span></span> <span data-ttu-id="e0708-115">เมื่อคุณกำลังพิจารณาความต้องการในการอนุญาตสำหรับผู้ใช้รายงานคนเดียว ให้พยายามสร้างบทบาทเดี่ยวที่ให้สิทธิ์เหล่านั้นทั้งหมดแทนที่จะเป็นการออกแบบที่ผู้ใช้รายงานจะเป็นสมาชิกของหลายบทบาทนั้น</span><span class="sxs-lookup"><span data-stu-id="e0708-115">When you're considering the permission needs for a single report user, strive to create a single role that grants all those permissions, instead of a design where a report user will be a member of multiple roles.</span></span> <span data-ttu-id="e0708-116">เป็นเพราะผู้ใช้รายงานสามารถทำแผนที่ไปยังหลายบทบาทได้โดยตรงโดยใช้บัญชีผู้ใช้ของพวกเขาหรือโดยทางอ้อมโดยการเป็นสมาชิกของกลุ่มความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="e0708-116">It's because a report user could map to multiple roles, either directly by using their user account or indirectly by security group membership.</span></span> <span data-ttu-id="e0708-117">การทำแผนที่บทบาทหลายครั้งอาจทำให้เกิดผลลัพธ์ที่ไม่คาดคิด</span><span class="sxs-lookup"><span data-stu-id="e0708-117">Multiple role mappings can result in unexpected outcomes.</span></span>

<span data-ttu-id="e0708-118">เมื่อผู้ใช้รายงานถูกกำหนดให้ทำงานหลายบทบาท ตัวกรอง RLS จะกลายเป็นสิ่งที่เพิ่มเข้าไป</span><span class="sxs-lookup"><span data-stu-id="e0708-118">When a report user is assigned to multiple roles, RLS filters become additive.</span></span> <span data-ttu-id="e0708-119">นั่นหมายความว่าผู้ใช้รายงานจะสามารถเห็นแถวของตารางที่แสดงการรวมตัวกันของตัวกรองเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="e0708-119">It means report users can see table rows that represent the union of those filters.</span></span> <span data-ttu-id="e0708-120">มากไปกว่านั้น ในบางเหตุการณ์คุณจะไม่สามารถการันตีได้ว่าผู้ใช้รายงานจะไม่เห็นแถวในตาราง</span><span class="sxs-lookup"><span data-stu-id="e0708-120">What's more, in some scenarios it's not possible to guarantee that a report user doesn't see rows in a table.</span></span> <span data-ttu-id="e0708-121">ดังนั้น ซึ่งแตกต่างจากการอนุญาตที่นำมาใช้กับวัตถุฐานข้อมูลเซิร์ฟเวอร์ SQL (และแบบจำลองการอนุญาตอื่นๆ) หลักการ "เมื่อถูกปฏิเสธแล้วจะถูกปฏิเสธเสมอไป" จะไม่นำไปใช้</span><span class="sxs-lookup"><span data-stu-id="e0708-121">So, unlike permissions applied to SQL Server database objects (and other permission models), the "once denied always denied" principle doesn't apply.</span></span>

<span data-ttu-id="e0708-122">พิจารณาแบบจำลองที่มีสองบทบาท: บทบาทแรก ชื่อ **ผู้ปฏิบัติงาน** จำกัดการเข้าถึงแถวของตาราง **บัญชีเงินเดือน** ทั้งหมดโดยใช้นิพจน์ของกฎต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e0708-122">Consider a model with two roles: The first role, named **Workers**, restricts access to all **Payroll** table rows by using the following rule expression:</span></span>

```dax
FALSE()
```

> [!NOTE]
> <span data-ttu-id="e0708-123">กฎจะไม่ส่งคืนแถวของตารางเมื่อนิพจน์นั้นประเมินเป็น **ผิด**</span><span class="sxs-lookup"><span data-stu-id="e0708-123">A rule will return no table rows when its expression evaluates to **false**.</span></span>

<span data-ttu-id="e0708-124">แต่บทบาทที่สองจะชื่อ **ผู้จัดการ** อนุญาตให้เข้าถึงแถวตาราง **ค่าจ้าง** ทั้งหมดโดยใช้นิพจน์ของกฎต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e0708-124">Yet, a second role, named **Managers**, allows access to all **Payroll** table rows by using the following rule expression:</span></span>

```dax
TRUE()
```

<span data-ttu-id="e0708-125">ดูแล: หากผู้ใช้รายงานแมปกับบทบาททั้งสองพวกเขาจะเห็นแถวตาราง **เงินเดือน** ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e0708-125">Take care: Should a report user map to both roles, they'll see all **Payroll** table rows.</span></span>

## <a name="optimize-rls"></a><span data-ttu-id="e0708-126">ปรับใช้ RLS</span><span class="sxs-lookup"><span data-stu-id="e0708-126">Optimize RLS</span></span>

<span data-ttu-id="e0708-127">RLS ทำงานโดยการนำตัวกรองไปใช้กับคิวรีทั้งหมดของ DAX โดยอัตโนมัติ และตัวกรองเหล่านี้อาจมีผลกระทบเชิงลบบนประสิทธิภาพการทำงานของคิวรี</span><span class="sxs-lookup"><span data-stu-id="e0708-127">RLS works by automatically applying filters to every DAX query, and these filters may have a negative impact on query performance.</span></span> <span data-ttu-id="e0708-128">ดังนั้น RLS ที่มีประสิทธิภาพมาจากการออกแบบแบบจำลองที่ดี</span><span class="sxs-lookup"><span data-stu-id="e0708-128">So, efficient RLS comes down to good model design.</span></span> <span data-ttu-id="e0708-129">สิ่งสำคัญคือต้องทำตามคำแนะนำการออกแบบแบบจำลองตามที่อธิบายไว้ในบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e0708-129">It's important to follow model design guidance, as discussed in the following articles:</span></span>

- [<span data-ttu-id="e0708-130">ทำความเข้าใจแบบจำลองมิติที่มีลักษณะคล้ายดาวและความสำคัญที่มีต่อ Power BI</span><span class="sxs-lookup"><span data-stu-id="e0708-130">Understand star schema and the importance for Power BI</span></span>](star-schema.md)
- <span data-ttu-id="e0708-131">บทความคำแนะนำของความสัมพันธ์ทั้งหมดที่พบใน [เอกสารคำแนะนำของ Power BI](./index.yml)</span><span class="sxs-lookup"><span data-stu-id="e0708-131">All relationship guidance articles found in the [Power BI guidance documentation](./index.yml)</span></span>

<span data-ttu-id="e0708-132">โดยทั่วไป มักจะมีประสิทธิภาพมากกว่าในการบังคับใช้ตัวกรอง RLS ในตารางประเภทมิติและไม่ใช่ตารางประเภทข้อเท็จจริง</span><span class="sxs-lookup"><span data-stu-id="e0708-132">In general, it's often more efficient to enforce RLS filters on dimension-type tables, and not fact-type tables.</span></span> <span data-ttu-id="e0708-133">และพึ่งพาความสัมพันธ์ที่ได้รับการออกแบบมาอย่างดีเพื่อให้แน่ใจว่าตัวกรอง RLS ได้เผยแพร่ไปยังตารางแบบจำลองอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="e0708-133">And, rely on well-designed relationships to ensure RLS filters propagate to other model tables.</span></span> <span data-ttu-id="e0708-134">ดังนั้นให้หลีกเลี่ยงการใช้ฟังก์ชัน DAX ของ [LOOKUPVALUE](/dax/lookupvalue-function-dax)  เมื่อความสัมพันธ์ของแบบจำลองสามารถทำให้เกิดผลลัพธ์เดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="e0708-134">So, avoid using the [LOOKUPVALUE](/dax/lookupvalue-function-dax) DAX function when model relationships could achieve the same result.</span></span>

<span data-ttu-id="e0708-135">เมื่อใดก็ตามที่มีการบังคับใช้ตัวกรอง RLS ในตาราง DirectQuery และมีความสัมพันธ์กับตาราง DirectQuery อื่นๆ ให้ตรวจสอบให้แน่ใจว่าได้ปรับใช้ฐานข้อมูลต้นฉบับให้เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="e0708-135">Whenever RLS filters are enforced on DirectQuery tables and there are relationships to other DirectQuery tables, be sure to optimize the source database.</span></span> <span data-ttu-id="e0708-136">ซึ่งอาจเกี่ยวข้องกับการออกแบบดัชนีที่เหมาะสมหรือใช้คอลัมน์ที่มีการคำนวณอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="e0708-136">It can involve designing appropriate indexes or using persisted computed columns.</span></span> <span data-ttu-id="e0708-137">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [คำแนะนำแบบจำลอง DirectQuery ใน Power BI Desktop](directquery-model-guidance.md)</span><span class="sxs-lookup"><span data-stu-id="e0708-137">For more information, see [DirectQuery model guidance in Power BI Desktop](directquery-model-guidance.md).</span></span>

### <a name="measure-rls-impact"></a><span data-ttu-id="e0708-138">วัดผลกระทบ RLS</span><span class="sxs-lookup"><span data-stu-id="e0708-138">Measure RLS impact</span></span>

<span data-ttu-id="e0708-139">เป็นไปได้ที่จะวัดผลกระทบของประสิทธิภาพการทำงานของตัวกรอง RLS ใน Power BI Desktop โดยใช้ [ตัววิเคราะห์ประสิทธิภาพ](../create-reports/desktop-performance-analyzer.md)</span><span class="sxs-lookup"><span data-stu-id="e0708-139">It's possible to measure the performance impact of RLS filters in Power BI Desktop by using [Performance Analyzer](../create-reports/desktop-performance-analyzer.md).</span></span> <span data-ttu-id="e0708-140">ก่อนอื่นให้กำหนดระยะเวลาของคิวรีวิชวลรายงานเมื่อ RLS ไม่ได้บังคับใช้</span><span class="sxs-lookup"><span data-stu-id="e0708-140">First, determine report visual query durations when RLS isn't enforced.</span></span> <span data-ttu-id="e0708-141">จากนั้นให้ใช้คำสั่ง **ดูเป็น** บนแท็บริบบอน **การสร้างรูปแบบ** เพื่อบังคับใช้ RLS และกำหนดและเปรียบเทียบระยะเวลาคิวรี</span><span class="sxs-lookup"><span data-stu-id="e0708-141">Then, use the **View As** command on the **Modeling** ribbon tab to enforce RLS and determine and compare query durations.</span></span>

## <a name="configure-role-mappings"></a><span data-ttu-id="e0708-142">กำหนดค่าการแมปบทบาท</span><span class="sxs-lookup"><span data-stu-id="e0708-142">Configure role mappings</span></span>

<span data-ttu-id="e0708-143">เมื่อเผยแพร่ไปยัง Power BI แล้ว คุณต้องแมปสมาชิกไปยังบทบาทชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e0708-143">Once published to Power BI, you must map members to dataset roles.</span></span> <span data-ttu-id="e0708-144">เฉพาะเจ้าของชุดข้อมูลหรือผู้ดูแลระบบพื้นที่ทำงานเท่านั้นที่สามารถเพิ่มสมาชิกลงในบทบาทได้</span><span class="sxs-lookup"><span data-stu-id="e0708-144">Only dataset owners or workspace admins can add members to roles.</span></span> <span data-ttu-id="e0708-145">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การรักษาความปลอดภัยระดับแถว (RLS) ด้วย Power BI (จัดการความปลอดภัยบนแบบจำลองของคุณ)](../admin/service-admin-rls.md#manage-security-on-your-model)</span><span class="sxs-lookup"><span data-stu-id="e0708-145">For more information, see [Row-level security (RLS) with Power BI (Manage security on your model)](../admin/service-admin-rls.md#manage-security-on-your-model).</span></span>

<span data-ttu-id="e0708-146">สมาชิกสามารถเป็นบัญชีผู้ใช้หรือกลุ่มความปลอดภัยได้</span><span class="sxs-lookup"><span data-stu-id="e0708-146">Members can be user accounts or security groups.</span></span> <span data-ttu-id="e0708-147">เมื่อใดก็ตามที่เป็นไปได้ เราขอแนะนำให้คุณแมปกลุ่มความปลอดภัยไปยังบทบาทชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e0708-147">Whenever possible, we recommend you map security groups to dataset roles.</span></span> <span data-ttu-id="e0708-148">ซึ่งเกี่ยวข้องกับการจัดการการเป็นสมาชิกของกลุ่มความปลอดภัยใน Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="e0708-148">It involves managing security group memberships in Azure Active Directory.</span></span> <span data-ttu-id="e0708-149">อาจเป็นไปได้ว่าได้มอบหมายงานให้กับผู้ดูแลระบบเครือข่ายของคุณ</span><span class="sxs-lookup"><span data-stu-id="e0708-149">Possibly, it delegates the task to your network administrators.</span></span>

## <a name="validate-roles"></a><span data-ttu-id="e0708-150">ตรวจสอบบทบาท</span><span class="sxs-lookup"><span data-stu-id="e0708-150">Validate roles</span></span>

<span data-ttu-id="e0708-151">ทดสอบแต่ละบทบาทเพื่อให้แน่ใจว่ามีการกรองแบบจำลองได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e0708-151">Test each role to ensure it filters the model correctly.</span></span> <span data-ttu-id="e0708-152">ทำได้อย่างง่ายดายโดยใช้คำสั่ง **ดูเป็น** บนแท็บริบบอน **การสร้างรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="e0708-152">It's easily done by using the **View As** command on the **Modeling** ribbon tab.</span></span>

<span data-ttu-id="e0708-153">เมื่อแบบจำลองมีกฎแบบไดนามิกที่ใช้ฟังก์ชัน DAX ของ [USERNAME](/dax/username-function-dax) โปรดตรวจสอบให้แน่ใจว่าได้ทดสอบค่าที่คาดไว้ _และที่ไม่คาดคิด_</span><span class="sxs-lookup"><span data-stu-id="e0708-153">When the model has dynamic rules using the [USERNAME](/dax/username-function-dax) DAX function, be sure to test for expected _and unexpected_ values.</span></span> <span data-ttu-id="e0708-154">เมื่อทำการฝังเนื้อหา Power BI — โดยเฉพาะโดยการใช้สถานการณ์จำลองของ [แอปที่เป็นเจ้าของข้อมูล](../developer/embedded/embedding.md#embedding-for-your-customers) — เช่นตรรกะของแอปสามารถส่งผ่านค่าใดก็ได้ในฐานะชื่อผู้ใช้ข้อมูลประจำตัวที่มีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="e0708-154">When embedding Power BI content—specifically using the [App owns data](../developer/embedded/embedding.md#embedding-for-your-customers) scenario—app logic can pass any value as an effective identity user name.</span></span> <span data-ttu-id="e0708-155">เมื่อใดก็ตามที่เป็นไปได้ ให้ตรวจสอบให้แน่ใจว่าค่าที่ไม่ได้ตั้งใจหรือเป็นอันตรายในตัวกรองที่ส่งแถวกลับมา</span><span class="sxs-lookup"><span data-stu-id="e0708-155">Whenever possible, ensure accidental or malicious values result in filters that return no rows.</span></span>

<span data-ttu-id="e0708-156">พิจารณาตัวอย่างโดยใช้ Power BI ที่ฝังอยู่ ซึ่งแอปจะส่งผ่านบทบาทงานของผู้ใช้เป็นชื่อผู้ใช้ที่มีประสิทธิภาพ: ซึ่งเป็น "ผู้จัดการ" หรือ "ผู้ปฏิบัติงาน"</span><span class="sxs-lookup"><span data-stu-id="e0708-156">Consider an example using Power BI embedded, where the app passes the user's job role as the effective user name: It's either "Manager" or "Worker".</span></span> <span data-ttu-id="e0708-157">ผู้จัดการสามารถดูแถวได้ทั้งหมด แต่ผู้ปฏิบัติงานจะสามารถดูได้เฉพาะแถวที่ค่าคอลัมน์ของ **ประเภท** เท่านั้นคือ "ภายใน"</span><span class="sxs-lookup"><span data-stu-id="e0708-157">Managers can see all rows, but workers can only see rows where the **Type** column value is "Internal".</span></span>

<span data-ttu-id="e0708-158">มีการกำหนดนิพจน์กฎต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e0708-158">The following rule expression is defined:</span></span>

```dax
IF(
    USERNAME() = "Worker",
    [Type] = "Internal",
    TRUE()
)
```

<span data-ttu-id="e0708-159">ปัญหาของนิพจน์กฎนี้คือค่าทั้งหมดยกเว้น "ผู้ปฏิบัติงาน" ที่ส่งกลับ _แถวตารางทั้งหมด_</span><span class="sxs-lookup"><span data-stu-id="e0708-159">The problem with this rule expression is that all values, except "Worker", return _all table rows_.</span></span> <span data-ttu-id="e0708-160">ดังนั้นค่าที่ไม่ได้ตั้งใจ เช่น "Wrker" โดยไม่ได้ตั้งใจจะส่งกลับแถวตารางทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e0708-160">So, an accidental value, like "Wrker",  unintentionally returns all table rows.</span></span> <span data-ttu-id="e0708-161">ดังนั้น จึงเป็นการปลอดภัยในการเขียนนิพจน์ที่ทดสอบสำหรับแต่ละค่าที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="e0708-161">Therefore, it's safer to write an expression that tests for each expected value.</span></span> <span data-ttu-id="e0708-162">ในนิพจน์กฎที่ได้รับการปรับปรุงต่อไปนี้ ค่าที่ไม่คาดคิดจะส่งผลให้ไม่มีการส่งคืนแถว</span><span class="sxs-lookup"><span data-stu-id="e0708-162">In the following improved rule expression, an unexpected value will result in the table returning no rows.</span></span>

```dax
IF(
    USERNAME() = "Worker",
    [Type] = "Internal",
    IF(
        USERNAME() = "Manager",
        TRUE(),
        FALSE()
    )
)
```

## <a name="design-partial-rls"></a><span data-ttu-id="e0708-163">ออกแบบ RLS บางส่วน</span><span class="sxs-lookup"><span data-stu-id="e0708-163">Design partial RLS</span></span>

<span data-ttu-id="e0708-164">บางครั้งการคำนวณต้องมีค่าที่ไม่ถูกจำกัดโดยตัวกรอง RLS</span><span class="sxs-lookup"><span data-stu-id="e0708-164">Sometimes, calculations need values that aren't constrained by RLS filters.</span></span> <span data-ttu-id="e0708-165">ตัวอย่างเช่น รายงานอาจจำเป็นต้องแสดงอัตราส่วนของรายได้ที่ได้รับสำหรับภูมิภาคการขายของผู้ใช้รายงานใน _รายได้ทั้งหมดที่ได้รับ_</span><span class="sxs-lookup"><span data-stu-id="e0708-165">For example, a report may need to display a ratio of revenue earned for the report user's sales region over _all revenue earned_.</span></span>

<span data-ttu-id="e0708-166">แม้ว่านิพจน์ DAX จะไม่สามารถแทนที่ RLS ได้ — แต่ในความเป็นจริงจะไม่สามารถระบุได้ว่า RLS นั้นถูกบังคับใช้หรือไม่ — คุณสามารถใช้ตารางแบบจำลองสรุปได้</span><span class="sxs-lookup"><span data-stu-id="e0708-166">While it's not possible for a DAX expression to override RLS—in fact, it can't even determine that RLS is enforced—you can use a summary model table.</span></span> <span data-ttu-id="e0708-167">ตารางแบบจำลองสรุปจะได้รับการสอบถามเพื่อดึงรายได้สำหรับ "ภูมิภาคทั้งหมด" และไม่ได้ถูกจำกัดโดยตัวกรอง RLS ใดๆ</span><span class="sxs-lookup"><span data-stu-id="e0708-167">The summary model table is queried to retrieve revenue for "all regions" and it's not constrained by any RLS filters.</span></span>

<span data-ttu-id="e0708-168">มาดูกันว่าคุณสามารถใช้ข้อกำหนดการออกแบบนี้ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="e0708-168">Let's see how you could implement this design requirement.</span></span> <span data-ttu-id="e0708-169">ก่อนอื่นให้พิจารณาการออกแบบแบบจำลองต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e0708-169">First, consider the following model design:</span></span>

:::image type="content" source="media/rls-guidance/mixed-rls-model.png" alt-text="รูปภาพของไดอะแกรมแบบจำลองจะแสดงขึ้นมา โดยจะได้รับการอธิบายในย่อหน้าถัดไป":::

<span data-ttu-id="e0708-171">แบบจำลองที่ประกอบด้วยสี่ตาราง:</span><span class="sxs-lookup"><span data-stu-id="e0708-171">The model comprises four tables:</span></span>

- <span data-ttu-id="e0708-172">ตาราง **พนักงานขาย** เก็บข้อมูลหนึ่งแถวต่อพนักงานขาย</span><span class="sxs-lookup"><span data-stu-id="e0708-172">The **Salesperson** table stores one row per salesperson.</span></span> <span data-ttu-id="e0708-173">ซึ่งรวมถึงคอลัมน์ **EmailAddress** ซึ่งจัดเก็บที่อยู่อีเมลสำหรับพนักงานขายแต่ละราย</span><span class="sxs-lookup"><span data-stu-id="e0708-173">It includes the **EmailAddress** column, which stores the email address for each salesperson.</span></span> <span data-ttu-id="e0708-174">ตารางนี้ถูกซ่อนไว้</span><span class="sxs-lookup"><span data-stu-id="e0708-174">This table is hidden.</span></span>
- <span data-ttu-id="e0708-175">ตาราง **ยอดขาย** จัดเก็บหนึ่งแถวต่อคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e0708-175">The **Sales** table stores one row per order.</span></span> <span data-ttu-id="e0708-176">ซึ่งรวมถึงหน่วยวัด **รายได้% ของภูมิภาคทั้งหมด** ซึ่งได้รับการออกแบบมาเพื่อส่งกลับอัตราส่วนของรายได้ที่ได้จากภูมิภาคของผู้ใช้รายงานที่มีรายได้ที่ได้รับจากภูมิภาคทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e0708-176">It includes the **Revenue % All Region** measure, which is designed to return a ratio of revenue earned by the report user's region over revenue earned by all regions.</span></span>
- <span data-ttu-id="e0708-177">ตาราง **วันที่** จัดเก็บหนึ่งแถวต่อวันที่ และอนุญาตให้มีการกรองและการจัดกลุ่มปีและเดือน</span><span class="sxs-lookup"><span data-stu-id="e0708-177">The **Date** table stores one row per date and allows filtering and grouping year and month.</span></span>
- <span data-ttu-id="e0708-178">**SalesRevenueSummary** เป็นตารางที่มีการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="e0708-178">The **SalesRevenueSummary** is a calculated table.</span></span> <span data-ttu-id="e0708-179">ซึ่งจัดเก็บรายได้รวมสำหรับแต่ละวันที่การสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="e0708-179">It stores total revenue for each order date.</span></span> <span data-ttu-id="e0708-180">ตารางนี้ถูกซ่อนไว้</span><span class="sxs-lookup"><span data-stu-id="e0708-180">This table is hidden.</span></span>

<span data-ttu-id="e0708-181">นิพจน์ต่อไปนี้กำหนดตารางที่มีการคำนวณของ **SalesRevenueSummary** :</span><span class="sxs-lookup"><span data-stu-id="e0708-181">The following expression defines the **SalesRevenueSummary** calculated table:</span></span>

```dax
SalesRevenueSummary =
SUMMARIZECOLUMNS(
    Sales[OrderDate],
    "RevenueAllRegion", SUM(Sales[Revenue])
)
```

> [!NOTE]
> <span data-ttu-id="e0708-182">[ตารางการรวม](../transform-model/desktop-aggregations.md) อาจทำให้เกิดความต้องการในการออกแบบเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="e0708-182">An [aggregation table](../transform-model/desktop-aggregations.md) could achieve the same design requirement.</span></span>

<span data-ttu-id="e0708-183">กฎการ RLS ต่อไปนี้ถูกนำไปใช้กับตาราง **พนักงานขาย** :</span><span class="sxs-lookup"><span data-stu-id="e0708-183">The following RLS rule is applied to the **Salesperson** table:</span></span>

```dax
[EmailAddress] = USERNAME()
```

<span data-ttu-id="e0708-184">แต่ละความสัมพันธ์ของแบบจำลองสามอย่างจะอธิบายไว้ในตารางต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e0708-184">Each of the three model relationships is described in the following table:</span></span>

|<span data-ttu-id="e0708-185">ความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="e0708-185">Relationship</span></span>|<span data-ttu-id="e0708-186">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e0708-186">Description</span></span>|
|---------|---------|
|![แผนผังลำดับงานของตัวกำจัด 1](media/common/icon-01-red-30x30.png)|<span data-ttu-id="e0708-188">มีความสัมพันธ์แบบกลุ่มต่อกลุ่มระหว่าง **พนักงานขาย** และตาราง **ยอดขาย**</span><span class="sxs-lookup"><span data-stu-id="e0708-188">There's a many-to-many relationship between the **Salesperson** and **Sales** tables.</span></span> <span data-ttu-id="e0708-189">กฎการ RLS กรองคอลัมน์ **EmailAddress** ของตาราง **พนักงานขาย** ที่ซ่อนไว้โดยใช้ฟังก์ชัน DAX ของ [USERNAME](/dax/username-function-dax)</span><span class="sxs-lookup"><span data-stu-id="e0708-189">The RLS rule filters the **EmailAddress** column of the hidden **Salesperson** table by using the [USERNAME](/dax/username-function-dax) DAX function.</span></span> <span data-ttu-id="e0708-190">ค่าคอลัมน์ **ภูมิภาค** (สำหรับผู้ใช้รายงาน) ได้กระจายไปยังตาราง **ยอดขาย**</span><span class="sxs-lookup"><span data-stu-id="e0708-190">The **Region** column value (for the report user) propagates to the **Sales** table.</span></span>|
|![แผนผังลำดับงานของตัวกำจัด 2](media/common/icon-02-red-30x30.png)|<span data-ttu-id="e0708-192">มีความสัมพันธ์แบบหนึ่งต่อกลุ่มระหว่าง **วันที่** และตาราง  **ยอดขาย**</span><span class="sxs-lookup"><span data-stu-id="e0708-192">There's a one-to-many relationships between the **Date** and **Sales** tables.</span></span>|
|![แผนผังลำดับงานของตัวกำจัด 3](media/common/icon-03-red-30x30.png)|<span data-ttu-id="e0708-194">มีความสัมพันธ์แบบหนึ่งต่อกลุ่มระหว่าง **วันที่** และตารางของ **SalesRevenueSummary**</span><span class="sxs-lookup"><span data-stu-id="e0708-194">There's a one-to-many relationships between the **Date** and **SalesRevenueSummary** tables.</span></span>|

<span data-ttu-id="e0708-195">นิพจน์ต่อไปนี้จะกำหนดหน่วยวัด **รายได้ % ของภูมิภาคทั้งหมด**:</span><span class="sxs-lookup"><span data-stu-id="e0708-195">The following expression defines the **Revenue % All Region** measure:</span></span>

```dax
Revenue % All Region =
DIVIDE(
    SUM(Sales[Revenue]),
    SUM(SalesRevenueSummary[RevenueAllRegion])
)
```

> [!NOTE]
> <span data-ttu-id="e0708-196">ดูแลเพื่อหลีกเลี่ยงการเปิดเผยข้อเท็จจริงที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="e0708-196">Take care to avoid disclosing sensitive facts.</span></span> <span data-ttu-id="e0708-197">หากมีเพียงสองภูมิภาคเท่านั้นในตัวอย่างนี้ จะเป็นไปได้สำหรับผู้ใช้รายงานในการคำนวณรายได้สำหรับภูมิภาคอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="e0708-197">If there are only two regions in this example, then it would be possible for a report user to calculate revenue for the other region.</span></span>

## <a name="avoid-using-rls"></a><span data-ttu-id="e0708-198">หลีกเลี่ยงการใช้ RLS</span><span class="sxs-lookup"><span data-stu-id="e0708-198">Avoid using RLS</span></span>

<span data-ttu-id="e0708-199">หลีกเลี่ยงการใช้ RLS เมื่อใดก็ตามที่คิดว่าเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="e0708-199">Avoid using RLS, whenever it makes sense to do so.</span></span> <span data-ttu-id="e0708-200">หากคุณมีกฎ RLS แบบง่ายๆจำนวนน้อยที่ใช้ตัวกรองแบบสแตติกให้พิจารณาการเผยแพร่หลายชุดข้อมูลแทน</span><span class="sxs-lookup"><span data-stu-id="e0708-200">If you have only a small number of simplistic RLS rules that apply static filters, consider publishing multiple datasets instead.</span></span> <span data-ttu-id="e0708-201">ไม่มีชุดข้อมูลที่มีการกำหนดบทบาทเนื่องจากแต่ละชุดข้อมูลที่ประกอบด้วยข้อมูลสำหรับผู้ชมผู้ใช้รายงานที่ระบุซึ่งมีสิทธิ์ในข้อมูลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="e0708-201">None of the datasets define roles because each dataset contains data for a specific report user audience, which has the same data permissions.</span></span> <span data-ttu-id="e0708-202">จากนั้นให้สร้างพื้นที่ทำงานหนึ่งรายการต่อผู้ชมและกำหนดสิทธิ์การเข้าถึงไปยังพื้นที่ทำงานหรือแอป</span><span class="sxs-lookup"><span data-stu-id="e0708-202">Then, create one workspace per audience and assign access permissions to the workspace or app.</span></span>

<span data-ttu-id="e0708-203">ตัวอย่างเช่น ที่มีเพียงสองภูมิภาคการขายที่ตัดสินใจที่จะเผยแพร่ชุดข้อมูล _สำหรับแต่ละภูมิภาคการขาย_ ไปยังพื้นที่ทำงานที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="e0708-203">For example, a company that has just two sales regions decides to publish a dataset _for each sales region_ to different workspaces.</span></span> <span data-ttu-id="e0708-204">ชุดข้อมูลไม่บังคับใช้ RLS</span><span class="sxs-lookup"><span data-stu-id="e0708-204">The datasets don't enforce RLS.</span></span> <span data-ttu-id="e0708-205">อย่างไรก็ตาม การใช้ [พารามิเตอร์คิวรี](/power-query/power-query-query-parameters) เพื่อกรองข้อมูลแหล่งที่มา</span><span class="sxs-lookup"><span data-stu-id="e0708-205">They do, however, use [query parameters](/power-query/power-query-query-parameters) to filter source data.</span></span> <span data-ttu-id="e0708-206">ด้วยวิธีนี้ แบบจำลองเดียวกันนี้จะถูกเผยแพร่ไปยังแต่ละพื้นทำงาน — ซึ่งมีค่าพารามิเตอร์ชุดข้อมูลที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="e0708-206">This way, the same model is published to each workspace—they just have different dataset parameter values.</span></span> <span data-ttu-id="e0708-207">พนักงานขายได้รับการกำหนดให้เข้าถึงหนึ่งในพื้นที่ทำงาน (หรือแอปที่เผยแพร่)</span><span class="sxs-lookup"><span data-stu-id="e0708-207">Salespeople are assigned access to just one of the workspaces (or published apps).</span></span>

<span data-ttu-id="e0708-208">มีข้อดีหลายประการที่เกี่ยวข้องกับการหลีกเลี่ยงการใช้ RLS:</span><span class="sxs-lookup"><span data-stu-id="e0708-208">There are several advantages associated with avoiding RLS:</span></span>

- <span data-ttu-id="e0708-209">**ปรับปรุงประสิทธิภาพคิวรี:** ซึ่งสามารถส่งผลให้ประสิทธิภาพดีขึ้นเนื่องจากตัวกรองน้อยลง</span><span class="sxs-lookup"><span data-stu-id="e0708-209">**Improved query performance:** It can result in improved performance due to fewer filters.</span></span>
- <span data-ttu-id="e0708-210">**แบบจำลองที่เล็กลง:** ในขณะที่ให้ผลในแบบจำลองที่มากขึ้น แต่มีขนาดเล็กลง</span><span class="sxs-lookup"><span data-stu-id="e0708-210">**Smaller models:** While it results in more models, they are smaller in size.</span></span> <span data-ttu-id="e0708-211">แบบจำลองที่เล็กลงสามารถปรับรุงการตอบสนองการรีเฟรชของคิวรีและข้อมูล โดยเฉพาะอย่างยิ่งถ้าความสามารถในการโฮสต์นั้นมีแรงกดดันต่อทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="e0708-211">Smaller models can improve query and data refresh responsiveness, especially if the hosting capacity experiences pressure on resources.</span></span> <span data-ttu-id="e0708-212">นอกจากนี้ยังง่ายต่อการรักษาขนาดของรุ่นให้ต่ำกว่าขนาดที่กำหนดโดยความจุข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="e0708-212">Also, it's easier to keep model sizes beneath size limits imposed by your capacity.</span></span> <span data-ttu-id="e0708-213">สุดท้ายแล้วมันง่ายกว่าที่จะสร้างสมดุลภาระงานในความสามารถที่แตกต่างกัน เนื่องจากคุณสามารถสร้างพื้นที่ทำงาน—หรือย้ายพื้นที่ทำงานไปยัง— ความสามารถที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="e0708-213">Lastly, it's easier to balance workloads across different capacities, because you can create workspaces on—or move workspaces to—different capacities.</span></span>
- <span data-ttu-id="e0708-214">**ฟีเจอร์เพิ่มเติม:** ฟีเจอร์ของ Power BI จะไม่ทำงานร่วมกับ RLS เช่น [เผยแพร่ไปยังเว็บ](../collaborate-share/service-publish-to-web.md) สามารถใช้ได้</span><span class="sxs-lookup"><span data-stu-id="e0708-214">**Additional features:** Power BI features that don't work with RLS, like [Publish to web](../collaborate-share/service-publish-to-web.md), can be used.</span></span>

<span data-ttu-id="e0708-215">อย่างไรก็ตามก็มีข้อเสียที่เกี่ยวข้องกับการหลีกเลี่ยงการใช้ RLS:</span><span class="sxs-lookup"><span data-stu-id="e0708-215">However, there are disadvantages associated with avoiding RLS:</span></span>

- <span data-ttu-id="e0708-216">**พื้นที่ทำงานหลายแห่ง:** จำเป็นต้องใช้พื้นที่ทำงานหนึ่งรายการสำหรับผู้ชมผู้ใช้รายงานแต่ละราย</span><span class="sxs-lookup"><span data-stu-id="e0708-216">**Multiple workspaces:** One workspace is required for each report user audience.</span></span> <span data-ttu-id="e0708-217">หาแอปได้รับการเผยแพร่แล้ว นั่นหมายความว่ามีหนึ่งแอปต่อผู้ชมผู้ใช้รายงาน</span><span class="sxs-lookup"><span data-stu-id="e0708-217">If apps are published, it also means there's one app per report user audience.</span></span>
- <span data-ttu-id="e0708-218">**การทำซ้ำของเนื้อหา:** ต้องสร้างรายงานและแดชบอร์ดในแต่ละพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="e0708-218">**Duplication of content:** Reports and dashboards must be created in each workspace.</span></span> <span data-ttu-id="e0708-219">ต้องใช้ความพยายามและเวลาเพิ่มเติมในการตั้งค่าและบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="e0708-219">It requires additional effort and time to set up and maintain.</span></span>
- <span data-ttu-id="e0708-220">**ผู้ใช้ที่มีสิทธิ์สูง:** ผู้ใช้ที่มีสิทธิ์สูงที่อยู่ในกลุ่มผู้ใช้รายงานหลายคนจะไม่สามารถดูมุมมองรวมของข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="e0708-220">**High privilege users:** High privilege users, who belong to multiple report user audiences, can't see a consolidated view of the data.</span></span> <span data-ttu-id="e0708-221">พวกเขาจะต้องเปิดรายงานหลายฉบับ (จากพื้นที่ทำงานหรือแอปที่แตกต่างกัน)</span><span class="sxs-lookup"><span data-stu-id="e0708-221">They'll need to open multiple reports (from different workspaces or apps).</span></span>

## <a name="troubleshoot-rls"></a><span data-ttu-id="e0708-222">แก้ไขปัญหา RLS</span><span class="sxs-lookup"><span data-stu-id="e0708-222">Troubleshoot RLS</span></span>

<span data-ttu-id="e0708-223">หาก RLS ให้ผลลัพธ์ที่ไม่คาดคิดให้ตรวจสอบปัญหาต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e0708-223">If RLS produces unexpected results, check for the following issues:</span></span>

- <span data-ttu-id="e0708-224">มีความสัมพันธ์ที่ไม่ถูกต้องระหว่างตารางแบบจำลองในเงื่อนไขของการแมปคอลัมน์และทิศทางของตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="e0708-224">Incorrect relationships exist between model tables, in terms of column mappings and filter directions.</span></span>
- <span data-ttu-id="e0708-225">คุณสมบัติความสัมพันธ์ **ใช้ตัวกรองความปลอดภัยทั้งสองทิศทาง** ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e0708-225">The **Apply security filter in both directions** relationship property isn't correctly set.</span></span> <span data-ttu-id="e0708-226">สำหรับข้อมูลเพิ่มเติม โปรดดู[คำแนะนำความแตกต่างระหว่างความสัมพันธ์ที่ใช้และไม่ได้ใช้งาน](relationships-bidirectional-filtering.md)</span><span class="sxs-lookup"><span data-stu-id="e0708-226">For more information, see [Bi-directional relationship guidance](relationships-bidirectional-filtering.md).</span></span>
- <span data-ttu-id="e0708-227">ตารางไม่มีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e0708-227">Tables contain no data.</span></span>
- <span data-ttu-id="e0708-228">มีการโหลดค่าที่ไม่ถูกต้องลงในตาราง</span><span class="sxs-lookup"><span data-stu-id="e0708-228">Incorrect values are loaded into tables.</span></span>
- <span data-ttu-id="e0708-229">ผู้ใช้ถูกแมปกับหลายบทบาท</span><span class="sxs-lookup"><span data-stu-id="e0708-229">The user is mapped to multiple roles.</span></span>
- <span data-ttu-id="e0708-230">แบบจำลองมีตารางสรุปรวมและกฎ RLS ไม่กรองการรวมและรายละเอียดอย่างสม่ำเสมอ</span><span class="sxs-lookup"><span data-stu-id="e0708-230">The model includes aggregation tables, and RLS rules don't consistently filter aggregations and details.</span></span> <span data-ttu-id="e0708-231">สำหรับข้อมูลเพิ่มเติม ให้ดู [ใช้การรวมใน Power BI Desktop (RLS สำหรับการรวม)](../transform-model/desktop-aggregations.md#rls-for-aggregations)</span><span class="sxs-lookup"><span data-stu-id="e0708-231">For more information, see [Use aggregations in Power BI Desktop (RLS for aggregations)](../transform-model/desktop-aggregations.md#rls-for-aggregations).</span></span>

<span data-ttu-id="e0708-232">เมื่อผู้ใช้ที่ระบุเฉพาะไม่เห็นข้อมูลใดๆ อาจเป็นเพราะ UPN ของพวกเขาไม่ได้ถูกจัดเก็บไว้หรือถูกป้อนเข้าไปไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e0708-232">When a specific user can't see any data, it could be because their UPN isn't stored or it's entered incorrectly.</span></span> <span data-ttu-id="e0708-233">ซึ่งสามารถเกิดขึ้นได้ทันทีเนื่องจากบัญชีผู้ใช้ของพวกเขาเปลี่ยนไปเนื่องจากผลของการเปลี่ยนชื่อ</span><span class="sxs-lookup"><span data-stu-id="e0708-233">It can happen abruptly because their user account has changed as the result of a name change.</span></span>

> [!TIP]
> <span data-ttu-id="e0708-234">สำหรับการทดสอบให้เพิ่มการวัดที่ส่งกลับฟังก์ชัน DAX ของ [USERNAME](/dax/username-function-dax)</span><span class="sxs-lookup"><span data-stu-id="e0708-234">For testing purposes, add a measure that returns the [USERNAME](/dax/username-function-dax) DAX function.</span></span> <span data-ttu-id="e0708-235">คุณอาจตั้งชื่อว่า "ฉันเป็นใคร"</span><span class="sxs-lookup"><span data-stu-id="e0708-235">You might name it something like "Who Am I".</span></span> <span data-ttu-id="e0708-236">จากนั้นให้เพิ่มการวัดลงในการ์ดที่มองเห็นในรายงานและเผยแพร่ลงใน Power BI</span><span class="sxs-lookup"><span data-stu-id="e0708-236">Then, add the measure to a card visual in a report and publish it to Power BI.</span></span>

<span data-ttu-id="e0708-237">เมื่อผู้ใช้ที่เฉพาะเจาะจงสามารถดูข้อมูลทั้งหมดได้ นั่นเป็นไปได้ว่าพวกเขากำลังเข้าถึงรายงานโดยตรงในพื้นที่ทำงานและพวกเขาเป็นเจ้าของชุดข้อมูลด้วย</span><span class="sxs-lookup"><span data-stu-id="e0708-237">When a specific user can see all data, it's possible they're accessing reports directly in the workspace and they're the dataset owner.</span></span> <span data-ttu-id="e0708-238">RLS ถูกบังคับใช้เฉพาะเมื่อ:</span><span class="sxs-lookup"><span data-stu-id="e0708-238">RLS is only enforced when:</span></span>

- <span data-ttu-id="e0708-239">รายงานถูกเปิดในแอป</span><span class="sxs-lookup"><span data-stu-id="e0708-239">The report is opened in an app.</span></span>
- <span data-ttu-id="e0708-240">รายงานถูกเปิดในพื้นที่ทำงานและผู้ใช้งานถูกแมปไปยัง [บทบาทของผู้ชม](../collaborate-share/service-new-workspaces.md#roles-in-the-new-workspaces)</span><span class="sxs-lookup"><span data-stu-id="e0708-240">The report is opened in a workspace, and the user is mapped to the [Viewer role](../collaborate-share/service-new-workspaces.md#roles-in-the-new-workspaces).</span></span>

## <a name="next-steps"></a><span data-ttu-id="e0708-241">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="e0708-241">Next steps</span></span>

<span data-ttu-id="e0708-242">สำหรับข้อมูลเพิ่มเติมที่เกี่ยวข้องกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e0708-242">For more information related to this article, check out the following resources:</span></span>

- [<span data-ttu-id="e0708-243">การรักษาความปลอดภัยระดับแถว (RLS) ด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="e0708-243">Row-level security (RLS) with Power BI</span></span>](../admin/service-admin-rls.md)
- [<span data-ttu-id="e0708-244">จำกัดการเข้าถึงข้อมูลด้วยการรักษาความปลอดภัยระดับแถว (RLS) สำหรับ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e0708-244">Restrict data access with row-level security (RLS) for Power BI Desktop</span></span>](../create-reports/desktop-rls.md)
- [<span data-ttu-id="e0708-245">ความสัมพันธ์ของแบบจำลองใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e0708-245">Model relationships in Power BI Desktop</span></span>](../transform-model/desktop-relationships-understand.md)
- <span data-ttu-id="e0708-246">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="e0708-246">Questions?</span></span> [<span data-ttu-id="e0708-247">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="e0708-247">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="e0708-248">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="e0708-248">Suggestions?</span></span> [<span data-ttu-id="e0708-249">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="e0708-249">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com/)
