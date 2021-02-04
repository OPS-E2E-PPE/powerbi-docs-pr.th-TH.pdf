---
title: ความจุและ SKU ในการวิเคราะห์แบบฝังตัวของ Power BI ช่วยให้สามารถใช้งานข้อมูลเชิงลึก BI แบบฝังตัวที่ดีขึ้น
description: เข้าใจเกี่ยวกับความจุและ SKU ในการวิเคราะห์แบบฝังตัวของ Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 01/06/2021
ms.openlocfilehash: c27d95715fe436b59825390b1cc16111e83ffc1d
ms.sourcegitcommit: 1cad78595cca1175b82c04458803764ac36e5e37
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/19/2021
ms.locfileid: "98564989"
---
# <a name="capacity-and-skus-in-power-bi-embedded-analytics"></a><span data-ttu-id="242a9-104">ความจุและ SKU ในการวิเคราะห์แบบฝังตัวของ Power BI</span><span class="sxs-lookup"><span data-stu-id="242a9-104">Capacity and SKUs in Power BI embedded analytics</span></span>

<span data-ttu-id="242a9-105">เมื่อย้ายไปที่การผลิต การวิเคราะห์แบบฝังตัวของ Power BI จำเป็นต้องมีความจุ (*A*, *EM* หรือ *P* SKU) สำหรับการเผยแพร่เนื้อหา Power BI แบบฝังตัว</span><span class="sxs-lookup"><span data-stu-id="242a9-105">When moving to production, Power BI embedded analytics requires a capacity (*A*, *EM*, or *P* SKU) for publishing embedded Power BI content.</span></span>

<span data-ttu-id="242a9-106">ความจุเป็นชุดทรัพยากรเฉพาะที่สงวนไว้สำหรับการใช้งานแบบพิเศษ</span><span class="sxs-lookup"><span data-stu-id="242a9-106">Capacity is a dedicated set of resources reserved for exclusive use.</span></span> <span data-ttu-id="242a9-107">ทำให้คุณสามารถเเผยแพร่แดชบอร์ด รายงาน และชุดข้อมูลไปยังผู้ใช้ โดยไม่จำเป็นต้องซื้อสิทธิ์การใช้งานต่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="242a9-107">It enables you to publish dashboards, reports, and datasets to users, without having to purchase per-user licenses.</span></span> <span data-ttu-id="242a9-108">นอกจากนี้ ยังนำเสนอประสิทธิภาพที่เชื่อถือได้และมีเสถียรภาพสำหรับเนื้อหาของคุณ</span><span class="sxs-lookup"><span data-stu-id="242a9-108">It also offers dependable, consistent performance for your content.</span></span>

>[!NOTE]
><span data-ttu-id="242a9-109">สำหรับการเผยแพร่ คุณต้องมีบัญชี Power BI Pro หนึ่งบัญชี</span><span class="sxs-lookup"><span data-stu-id="242a9-109">For publishing, you'll need one Power BI Pro account.</span></span>

## <a name="what-is-embedded-analytics"></a><span data-ttu-id="242a9-110">การวิเคราะห์แบบฝังตัวคืออะไร</span><span class="sxs-lookup"><span data-stu-id="242a9-110">What is embedded analytics?</span></span>

<span data-ttu-id="242a9-111">การวิเคราะห์แบบฝังตัว Power BI มีโซลูชันสองแบบ:</span><span class="sxs-lookup"><span data-stu-id="242a9-111">Power BI embedded analytics includes two solutions:</span></span>

* <span data-ttu-id="242a9-112">*Power BI Embedded*  - ข้อเสนอของ Azure</span><span class="sxs-lookup"><span data-stu-id="242a9-112">*Power BI Embedded*  - Azure offering</span></span>

* <span data-ttu-id="242a9-113">Power BI แบบฝังตัวเป็นส่วนหนึ่งของ *Power BI Premium*  - ข้อเสนอของ Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="242a9-113">Embedding Power BI as part of *Power BI Premium*  - Microsoft Office offering</span></span>

### <a name="power-bi-embedded"></a><span data-ttu-id="242a9-114">Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="242a9-114">Power BI Embedded</span></span>

<span data-ttu-id="242a9-115">Power BI Embedded มีไว้สำหรับ ISV และนักพัฒนาที่ต้องการฝังภาพลงในแอปพลิเคชันของตน</span><span class="sxs-lookup"><span data-stu-id="242a9-115">Power BI Embedded is for ISVs and developers who want to embed visuals into their applications.</span></span>

<span data-ttu-id="242a9-116">แอปพลิเคชันที่ใช้ Power BI Embedded ทำให้ผู้ใช้สามารถใช้เนื้อหาที่จัดเก็บไว้ในความจุ Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="242a9-116">Applications using Power BI Embedded allow users to consume content stored on Power BI Embedded capacity.</span></span>

### <a name="power-bi-premium"></a><span data-ttu-id="242a9-117">Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="242a9-117">Power BI Premium</span></span>

<span data-ttu-id="242a9-118">[Power BI Premium](../../admin/service-premium-what-is.md) มีความจุที่ปรับให้เหมาะกับองค์กร ที่ต้องการโซลูชัน BI ที่สมบูรณ์ ที่ให้มุมมองเดียวกันแก่องค์กร คู่ค้า ลูกค้า และผู้จัดหาสินค้าขององค์กร</span><span class="sxs-lookup"><span data-stu-id="242a9-118">[Power BI Premium](../../admin/service-premium-what-is.md) is geared toward enterprises who want a complete BI solution that provides a single view of its organization, partners, customers, and suppliers.</span></span>

<span data-ttu-id="242a9-119">Power BI Premium เป็นผลิตภัณฑ์ SaaS ที่ให้ผู้ใช้สามารถใช้เนื้อหาผ่านทางแอปสำหรับอุปกรณ์เคลื่อนที่ แอปที่พัฒนาขึ้นเองภายใน หรือที่พอร์ทัล Power BI (บริการ Power BI)</span><span class="sxs-lookup"><span data-stu-id="242a9-119">Power BI Premium is a SaaS product that allows users to consume content through mobile apps, internally developed apps, or at the Power BI portal (Power BI service).</span></span> <span data-ttu-id="242a9-120">สิ่งนี้ทำให้ Power BI Premium มีโซลูชันสำหรับแอปพลิเคชันของลูกค้าทั้งภายในและภายนอก</span><span class="sxs-lookup"><span data-stu-id="242a9-120">This enables Power BI Premium to provide a solution for both internal and external customer facing applications.</span></span>

## <a name="capacity-and-skus"></a><span data-ttu-id="242a9-121">ความจุและ SKU</span><span class="sxs-lookup"><span data-stu-id="242a9-121">Capacity and SKUs</span></span>

<span data-ttu-id="242a9-122">ความจุแต่ละแบบจะนำเสนอ SKU เฉพาะแบบ และ SKU แต่ละแบบจะนำเสนอเทียร์ทรัพยากรที่แตกต่างกันสำหรับหน่วยความจำและพลังในการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="242a9-122">Each capacity offers a selection of SKUs, and each SKU provides different resource tiers for memory and computing power.</span></span> <span data-ttu-id="242a9-123">ประเภทของ SKU ที่คุณต้องการ จะขึ้นอยู่กับประเภทโซลูชันที่คุณต้องการปรับใช้</span><span class="sxs-lookup"><span data-stu-id="242a9-123">The type of SKU you require, depends on the type of solution you wish to deploy.</span></span>

<span data-ttu-id="242a9-124">เพื่อทำความเข้าใจปริมาณงานที่รองรับสำหรับแต่ละเทียร์ โปรดดูที่บทความ [กำหนดค่าปริมาณงานในกำลังการผลิตแบบ Premium](../../admin/service-admin-premium-workloads.md)</span><span class="sxs-lookup"><span data-stu-id="242a9-124">To understand which workloads are supported for each tier, refer to the [Configure workloads in a Premium capacity](../../admin/service-admin-premium-workloads.md) article</span></span>

<span data-ttu-id="242a9-125">ใช้ลิงก์นี้เพื่อวางแผนและทดสอบความจุของคุณ</span><span class="sxs-lookup"><span data-stu-id="242a9-125">To plan and test your capacity, use these links:</span></span>
* [<span data-ttu-id="242a9-126">การวางแผนความจุ</span><span class="sxs-lookup"><span data-stu-id="242a9-126">Capacity planning</span></span>](embedded-capacity-planning.md)
* [<span data-ttu-id="242a9-127">การทดสอบวิธีการ</span><span class="sxs-lookup"><span data-stu-id="242a9-127">Testing approaches</span></span>](../../admin/service-premium-capacity-optimize.md#testing-approaches)

### <a name="power-bi-embedded-skus"></a><span data-ttu-id="242a9-128">SKU สำหรับ Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="242a9-128">Power BI Embedded SKUs</span></span>

<span data-ttu-id="242a9-129">Power BI Embedded จะถูกจัดส่งด้วย [*a* SKU](../../admin/service-admin-premium-purchase.md#purchase-a-skus-for-testing-and-other-scenarios)</span><span class="sxs-lookup"><span data-stu-id="242a9-129">Power BI Embedded is shipped with an [*a* SKU](../../admin/service-admin-premium-purchase.md#purchase-a-skus-for-testing-and-other-scenarios).</span></span>

### <a name="power-bi-premium-skus"></a><span data-ttu-id="242a9-130">Power BI Premium SKU</span><span class="sxs-lookup"><span data-stu-id="242a9-130">Power BI Premium SKUs</span></span>

<span data-ttu-id="242a9-131">Power BI premium นำเสนอ SKU สองแบบคือ *P* และ *EM*</span><span class="sxs-lookup"><span data-stu-id="242a9-131">Power BI premium offers two SKUs, *P* and *EM*.</span></span>
* [<span data-ttu-id="242a9-132">เข้าใจความแตกต่างระหว่าง *P* กับ *EM* SKU</span><span class="sxs-lookup"><span data-stu-id="242a9-132">Understand the differences between the *P* and *EM* SKUs</span></span>](../../admin/service-premium-what-is.md#subscriptions-and-licensing)
* [<span data-ttu-id="242a9-133">ซื้อ Premium SKU</span><span class="sxs-lookup"><span data-stu-id="242a9-133">Buy a Premium SKU</span></span>](../../admin/service-admin-premium-purchase.md)

### <a name="which-sku-should-i-use"></a><span data-ttu-id="242a9-134">SKU ใดที่คุณควรใช้</span><span class="sxs-lookup"><span data-stu-id="242a9-134">Which SKU should I use?</span></span>

<span data-ttu-id="242a9-135">ตารางด้านล่างระบุข้อมูลสรุปของคุณลักษณะ กำลังการผลิตที่จำเป็น และ SKU เฉพาะที่จำเป็นสำหรับแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="242a9-135">The table below provides a summary of features, the capacity they require, and the specific SKU that is needed for each one.</span></span>

<span data-ttu-id="242a9-136">ในตารางนี้ แอปแบบกำหนดเอง หมายถึง เว็บแอปที่สร้างขึ้นโดยใช้การวิเคราะห์แบบฝังตัว</span><span class="sxs-lookup"><span data-stu-id="242a9-136">In this table, a custom app refers to a web app created using embedded analytics.</span></span> <span data-ttu-id="242a9-137">เมื่อคุณทำการฝังตัวไปยังเว็บแอป แบบกำหนดเองในฐานะนักพัฒนา (โดยใช้ JavaScript หรือ .NET SDK หรือ REST API) คุณมีความสามารถในการควบคุมและกำหนดค่า UX</span><span class="sxs-lookup"><span data-stu-id="242a9-137">When you embed to a custom web app as a developer (using the JavaScript or .NET SDKs, or the REST APIs), you have the ability to control and customize the UX.</span></span> <span data-ttu-id="242a9-138">ความสามารถนี้จะไม่พร้อมใช้งานเมื่อคุณใช้ตัวเลือกการฝังแบบอื่นๆ เช่นบริการของ Power BI และ Power BI สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="242a9-138">This ability is not available when you use other embedding options, such as Power BI service and Power BI Mobile.</span></span>

| <span data-ttu-id="242a9-139">สถานการณ์สมมติ</span><span class="sxs-lookup"><span data-stu-id="242a9-139">Scenario</span></span> | <span data-ttu-id="242a9-140">Azure</span><span class="sxs-lookup"><span data-stu-id="242a9-140">Azure</span></span>   | <span data-ttu-id="242a9-141">Office</span><span class="sxs-lookup"><span data-stu-id="242a9-141">Office</span></span>          |
|----------|---------|-----------------|
|          | <span data-ttu-id="242a9-142">(A SKU)</span><span class="sxs-lookup"><span data-stu-id="242a9-142">(A SKU)</span></span> | <span data-ttu-id="242a9-143">(P และ EM SKU)</span><span class="sxs-lookup"><span data-stu-id="242a9-143">(P and EM SKUs)</span></span> |
|[<span data-ttu-id="242a9-144">ฝังสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="242a9-144">Embed for your customers</span></span>](embed-sample-for-customers.md)</br><span data-ttu-id="242a9-145">(ข้อมูลชองแอป)</span><span class="sxs-lookup"><span data-stu-id="242a9-145">(app owns data)</span></span>     |<span data-ttu-id="242a9-146">✔</span><span class="sxs-lookup"><span data-stu-id="242a9-146">✔</span></span>        |<span data-ttu-id="242a9-147">✔</span><span class="sxs-lookup"><span data-stu-id="242a9-147">✔</span></span>        |
|[<span data-ttu-id="242a9-148">ฝังตัวสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="242a9-148">Embed for your organization</span></span>](embed-sample-for-your-organization.md)</br><span data-ttu-id="242a9-149">(ข้อมูลของผู้ใช้เอง)</span><span class="sxs-lookup"><span data-stu-id="242a9-149">(user owns data)</span></span>     |<span data-ttu-id="242a9-150">✖</span><span class="sxs-lookup"><span data-stu-id="242a9-150">✖</span></span>        |<span data-ttu-id="242a9-151">✔</span><span class="sxs-lookup"><span data-stu-id="242a9-151">✔</span></span>         |
|<span data-ttu-id="242a9-152">แอป Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="242a9-152">Microsoft 365 apps</span></span></br><span data-ttu-id="242a9-153">(เดิมเรียกว่าแอป Office 365)</span><span class="sxs-lookup"><span data-stu-id="242a9-153">(formerly known as Office 365 apps)</span></span><ul><li>[<span data-ttu-id="242a9-154">ฝังใน Teams</span><span class="sxs-lookup"><span data-stu-id="242a9-154">Embed in Teams</span></span>](../../collaborate-share/service-embed-report-microsoft-teams.md)</li><li>[<span data-ttu-id="242a9-155">ฝังใน SharePoint</span><span class="sxs-lookup"><span data-stu-id="242a9-155">Embed in SharePoint</span></span>](../../collaborate-share/service-embed-report-spo.md)</li></ul>     |<span data-ttu-id="242a9-156">✖</span><span class="sxs-lookup"><span data-stu-id="242a9-156">✖</span></span>        |<span data-ttu-id="242a9-157">✔</span><span class="sxs-lookup"><span data-stu-id="242a9-157">✔</span></span>        |
|[<span data-ttu-id="242a9-158">การฝัง URL ที่ปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="242a9-158">Secure URL embedding</span></span>](../../collaborate-share/service-embed-secure.md)</br><span data-ttu-id="242a9-159">(ฝังจากบริการของ Power BI)</span><span class="sxs-lookup"><span data-stu-id="242a9-159">(embed from Power BI service)</span></span>     |<span data-ttu-id="242a9-160">✖</span><span class="sxs-lookup"><span data-stu-id="242a9-160">✖</span></span>        |<span data-ttu-id="242a9-161">✔</span><span class="sxs-lookup"><span data-stu-id="242a9-161">✔</span></span>        |

>[!NOTE]
>* <span data-ttu-id="242a9-162">[สิทธิ์การใช้งาน Power BI Pro](../../admin/service-admin-purchasing-power-bi-pro.md) จำเป็นสำหรับการเผยแพร่เนื้อหาไปยังพื้นที่ทำงานของแอป Power BI</span><span class="sxs-lookup"><span data-stu-id="242a9-162">A [Power BI Pro license](../../admin/service-admin-purchasing-power-bi-pro.md) is needed for publishing content to a Power BI app workspace.</span></span>
>* <span data-ttu-id="242a9-163">เฉพาะ **P SKU** เท่านั้นที่อนุญาตให้ผู้ใช้ฟรีของ Power BI สามารถใช้งานแอป Power BI และเนื้อหาที่ใช้ร่วมกันได้ ในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="242a9-163">Only the **P SKU** allows free Power BI users to consume Power BI apps and shared content, in Power BI service.</span></span>

### <a name="capacity-considerations"></a><span data-ttu-id="242a9-164">ข้อควรพิจารณาเกี่ยวกับกำลังการผลิต</span><span class="sxs-lookup"><span data-stu-id="242a9-164">Capacity considerations</span></span>

<span data-ttu-id="242a9-165">ตารางด้านล่างแสดงรายการข้อควรพิจารณาเกี่ยวกับการชำระเงินและการใช้งานต่อความจุ</span><span class="sxs-lookup"><span data-stu-id="242a9-165">The table below lists payment and usage considerations per capacity.</span></span>

</br>
<table>
<tbody>
<tr>
<td></td>
<td style="text-align: center;"><p><span data-ttu-id="242a9-166"><strong>Power BI Embedded</strong></span><span class="sxs-lookup"><span data-stu-id="242a9-166"><strong>Power BI Embedded</strong></span></span></p></td>
<td style="text-align: center;" colspan="2"><p><span data-ttu-id="242a9-167"><strong>Power BI Premium</strong></span><span class="sxs-lookup"><span data-stu-id="242a9-167"><strong>Power BI Premium</strong></span></span></p></td>
</tr>
<tr>
<td><p><span data-ttu-id="242a9-168"><strong>ข้อเสนอ</strong></span><span class="sxs-lookup"><span data-stu-id="242a9-168"><strong>Offer</strong></span></span></p></td>
<td style="text-align: center"><p><span data-ttu-id="242a9-169">Azure</span><span class="sxs-lookup"><span data-stu-id="242a9-169">Azure</span></span></p></td>
<td style="text-align: center" colspan="2"><p><span data-ttu-id="242a9-170">Office</span><span class="sxs-lookup"><span data-stu-id="242a9-170">Office</span></span></p></td>
</tr>
<tr>
<td><p><span data-ttu-id="242a9-171"><strong>SKU</strong></span><span class="sxs-lookup"><span data-stu-id="242a9-171"><strong>SKU</strong></span></span></p></td>
<td style="text-align: center"><p><span data-ttu-id="242a9-172">A</span><span class="sxs-lookup"><span data-stu-id="242a9-172">A</span></span></p></td>
<td style="text-align: center"><p><span data-ttu-id="242a9-173">EM</span><span class="sxs-lookup"><span data-stu-id="242a9-173">EM</span></span></p></td>
<td style="text-align: center"><p><span data-ttu-id="242a9-174">P</span><span class="sxs-lookup"><span data-stu-id="242a9-174">P</span></span></p></td>
</tr>
<tr>
<td><p><span data-ttu-id="242a9-175"><strong>การเรียกเก็บเงิน</strong></span><span class="sxs-lookup"><span data-stu-id="242a9-175"><strong>Billing</strong></span></span></td>
<td style="text-align: center"><span data-ttu-id="242a9-176">รายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="242a9-176">Hourly</span></span></td>
<td style="text-align: center"><span data-ttu-id="242a9-177">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="242a9-177">Monthly</span></span></td>
<td style="text-align: center"><span data-ttu-id="242a9-178">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="242a9-178">Monthly</span></span></td>
</tr>
<tr>
<td><p><span data-ttu-id="242a9-179"><strong>ข้อผูกมัด</strong></span><span class="sxs-lookup"><span data-stu-id="242a9-179"><strong>Commitment</strong></span></span></td>
<td style="text-align: center"><span data-ttu-id="242a9-180">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="242a9-180">None</span></span></td>
<td style="text-align: center"><span data-ttu-id="242a9-181">รายปี</span><span class="sxs-lookup"><span data-stu-id="242a9-181">Yearly</span></span></td>
<td style="text-align: center"><span data-ttu-id="242a9-182">รายเดือนหรือรายปี</span><span class="sxs-lookup"><span data-stu-id="242a9-182">Monthly or yearly</span></span></td>
</tr>
<tr>
<td valign="top"><p><span data-ttu-id="242a9-183"><strong>การใช้งาน</strong></span><span class="sxs-lookup"><span data-stu-id="242a9-183"><strong>Usage</strong></span></span></td>
<td style="text-align: center"><span data-ttu-id="242a9-184">ทรัพยากร Azure อาจเป็น:</span><span class="sxs-lookup"><span data-stu-id="242a9-184">Azure resources can be:</span></span><li><span data-ttu-id="242a9-185"><a href="azure-pbie-scale-capacity.md">ปรับค่าสูงหรือลดลง</a></span><span class="sxs-lookup"><span data-stu-id="242a9-185"><a href="azure-pbie-scale-capacity.md">Scaled up or down</a></span></span></li><li><span data-ttu-id="242a9-186"><a href="azure-pbie-pause-start.md">หยุดชั่วคราวและทำต่อ</a>
</span><span class="sxs-lookup"><span data-stu-id="242a9-186"><a href="azure-pbie-pause-start.md">Paused and resumed</a>
</span></span></td></li>
<td style="text-align: center"><span data-ttu-id="242a9-187">ฝังในแอปและใน</span><span class="sxs-lookup"><span data-stu-id="242a9-187">Embed in apps, and in</span></span></br> <span data-ttu-id="242a9-188">แอปพลิเคชัน Microsoft</span><span class="sxs-lookup"><span data-stu-id="242a9-188">Microsoft applications</span></span></td>
<td style="text-align: center"><span data-ttu-id="242a9-189">ฝังในแอปและ</span><span class="sxs-lookup"><span data-stu-id="242a9-189">Embed in apps, and</span></span></br> <span data-ttu-id="242a9-190">ในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="242a9-190">in Power BI service</span></span></td>
</tr>
</tbody>
</table>

### <a name="sku-memory-and-computing-power"></a><span data-ttu-id="242a9-191">หน่วยความจำ SKU และกำลังสำหรับการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="242a9-191">SKU memory and computing power</span></span>

<span data-ttu-id="242a9-192">ตารางด้านล่างอธิบายแหล่งข้อมูลและขีดจำกัดของแต่ละ SKU</span><span class="sxs-lookup"><span data-stu-id="242a9-192">The table below describes the resources and limits of each SKU.</span></span>

| <span data-ttu-id="242a9-193">โหนดความจุ</span><span class="sxs-lookup"><span data-stu-id="242a9-193">Capacity Nodes</span></span> | <span data-ttu-id="242a9-194">วี-คอร์รวม</span><span class="sxs-lookup"><span data-stu-id="242a9-194">Total v-cores</span></span> | <span data-ttu-id="242a9-195">Backend v-cores</span><span class="sxs-lookup"><span data-stu-id="242a9-195">Backend v-cores</span></span> | <span data-ttu-id="242a9-196">RAM (GB)</span><span class="sxs-lookup"><span data-stu-id="242a9-196">RAM (GB)</span></span> | <span data-ttu-id="242a9-197">Frontend v-cores</span><span class="sxs-lookup"><span data-stu-id="242a9-197">Frontend v-cores</span></span> | <span data-ttu-id="242a9-198">DirectQuery/Live Connection (ต่อวินาที)</span><span class="sxs-lookup"><span data-stu-id="242a9-198">DirectQuery/Live Connection (per sec)</span></span> | <span data-ttu-id="242a9-199">การรีเฟรชแบบจำลองแบบคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="242a9-199">Model Refresh Parallelism</span></span> |
| --- | --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="242a9-200">EM1/A1</span><span class="sxs-lookup"><span data-stu-id="242a9-200">EM1/A1</span></span> | <span data-ttu-id="242a9-201">1</span><span class="sxs-lookup"><span data-stu-id="242a9-201">1</span></span> | <span data-ttu-id="242a9-202">0.5</span><span class="sxs-lookup"><span data-stu-id="242a9-202">0.5</span></span> | <span data-ttu-id="242a9-203">2.5</span><span class="sxs-lookup"><span data-stu-id="242a9-203">2.5</span></span> | <span data-ttu-id="242a9-204">0.5</span><span class="sxs-lookup"><span data-stu-id="242a9-204">0.5</span></span> | <span data-ttu-id="242a9-205">3.75</span><span class="sxs-lookup"><span data-stu-id="242a9-205">3.75</span></span> | <span data-ttu-id="242a9-206">1</span><span class="sxs-lookup"><span data-stu-id="242a9-206">1</span></span> |
| <span data-ttu-id="242a9-207">EM2/A2</span><span class="sxs-lookup"><span data-stu-id="242a9-207">EM2/A2</span></span> | <span data-ttu-id="242a9-208">2</span><span class="sxs-lookup"><span data-stu-id="242a9-208">2</span></span> | <span data-ttu-id="242a9-209">1</span><span class="sxs-lookup"><span data-stu-id="242a9-209">1</span></span> | <span data-ttu-id="242a9-210">5</span><span class="sxs-lookup"><span data-stu-id="242a9-210">5</span></span> | <span data-ttu-id="242a9-211">1</span><span class="sxs-lookup"><span data-stu-id="242a9-211">1</span></span> | <span data-ttu-id="242a9-212">7.5</span><span class="sxs-lookup"><span data-stu-id="242a9-212">7.5</span></span> | <span data-ttu-id="242a9-213">2</span><span class="sxs-lookup"><span data-stu-id="242a9-213">2</span></span> |
| <span data-ttu-id="242a9-214">EM3/A3</span><span class="sxs-lookup"><span data-stu-id="242a9-214">EM3/A3</span></span> | <span data-ttu-id="242a9-215">4</span><span class="sxs-lookup"><span data-stu-id="242a9-215">4</span></span> | <span data-ttu-id="242a9-216">2</span><span class="sxs-lookup"><span data-stu-id="242a9-216">2</span></span> | <span data-ttu-id="242a9-217">10</span><span class="sxs-lookup"><span data-stu-id="242a9-217">10</span></span> | <span data-ttu-id="242a9-218">2</span><span class="sxs-lookup"><span data-stu-id="242a9-218">2</span></span> | <span data-ttu-id="242a9-219">15</span><span class="sxs-lookup"><span data-stu-id="242a9-219">15</span></span> | <span data-ttu-id="242a9-220">3</span><span class="sxs-lookup"><span data-stu-id="242a9-220">3</span></span> |
| <span data-ttu-id="242a9-221">P1/A4</span><span class="sxs-lookup"><span data-stu-id="242a9-221">P1/A4</span></span> | <span data-ttu-id="242a9-222">8</span><span class="sxs-lookup"><span data-stu-id="242a9-222">8</span></span> | <span data-ttu-id="242a9-223">4</span><span class="sxs-lookup"><span data-stu-id="242a9-223">4</span></span> | <span data-ttu-id="242a9-224">25</span><span class="sxs-lookup"><span data-stu-id="242a9-224">25</span></span> | <span data-ttu-id="242a9-225">4</span><span class="sxs-lookup"><span data-stu-id="242a9-225">4</span></span> | <span data-ttu-id="242a9-226">30</span><span class="sxs-lookup"><span data-stu-id="242a9-226">30</span></span> | <span data-ttu-id="242a9-227">6</span><span class="sxs-lookup"><span data-stu-id="242a9-227">6</span></span> |
| <span data-ttu-id="242a9-228">P2/A5</span><span class="sxs-lookup"><span data-stu-id="242a9-228">P2/A5</span></span> | <span data-ttu-id="242a9-229">16</span><span class="sxs-lookup"><span data-stu-id="242a9-229">16</span></span> | <span data-ttu-id="242a9-230">8</span><span class="sxs-lookup"><span data-stu-id="242a9-230">8</span></span> | <span data-ttu-id="242a9-231">50</span><span class="sxs-lookup"><span data-stu-id="242a9-231">50</span></span> | <span data-ttu-id="242a9-232">8</span><span class="sxs-lookup"><span data-stu-id="242a9-232">8</span></span> | <span data-ttu-id="242a9-233">60</span><span class="sxs-lookup"><span data-stu-id="242a9-233">60</span></span> | <span data-ttu-id="242a9-234">12</span><span class="sxs-lookup"><span data-stu-id="242a9-234">12</span></span> |
| <span data-ttu-id="242a9-235">P3/A6</span><span class="sxs-lookup"><span data-stu-id="242a9-235">P3/A6</span></span> | <span data-ttu-id="242a9-236">32</span><span class="sxs-lookup"><span data-stu-id="242a9-236">32</span></span> | <span data-ttu-id="242a9-237">16</span><span class="sxs-lookup"><span data-stu-id="242a9-237">16</span></span> | <span data-ttu-id="242a9-238">100</span><span class="sxs-lookup"><span data-stu-id="242a9-238">100</span></span> | <span data-ttu-id="242a9-239">16</span><span class="sxs-lookup"><span data-stu-id="242a9-239">16</span></span> | <span data-ttu-id="242a9-240">120</span><span class="sxs-lookup"><span data-stu-id="242a9-240">120</span></span> | <span data-ttu-id="242a9-241">24</span><span class="sxs-lookup"><span data-stu-id="242a9-241">24</span></span> |
| <span data-ttu-id="242a9-242">P4</span><span class="sxs-lookup"><span data-stu-id="242a9-242">P4</span></span> | <span data-ttu-id="242a9-243">64</span><span class="sxs-lookup"><span data-stu-id="242a9-243">64</span></span> | <span data-ttu-id="242a9-244">32</span><span class="sxs-lookup"><span data-stu-id="242a9-244">32</span></span> | <span data-ttu-id="242a9-245">200</span><span class="sxs-lookup"><span data-stu-id="242a9-245">200</span></span> | <span data-ttu-id="242a9-246">32</span><span class="sxs-lookup"><span data-stu-id="242a9-246">32</span></span> | <span data-ttu-id="242a9-247">240</span><span class="sxs-lookup"><span data-stu-id="242a9-247">240</span></span> | <span data-ttu-id="242a9-248">48</span><span class="sxs-lookup"><span data-stu-id="242a9-248">48</span></span> |
| <span data-ttu-id="242a9-249">P5</span><span class="sxs-lookup"><span data-stu-id="242a9-249">P5</span></span> | <span data-ttu-id="242a9-250">128</span><span class="sxs-lookup"><span data-stu-id="242a9-250">128</span></span> | <span data-ttu-id="242a9-251">64</span><span class="sxs-lookup"><span data-stu-id="242a9-251">64</span></span> | <span data-ttu-id="242a9-252">400</span><span class="sxs-lookup"><span data-stu-id="242a9-252">400</span></span> | <span data-ttu-id="242a9-253">64</span><span class="sxs-lookup"><span data-stu-id="242a9-253">64</span></span> | <span data-ttu-id="242a9-254">480</span><span class="sxs-lookup"><span data-stu-id="242a9-254">480</span></span> | <span data-ttu-id="242a9-255">96</span><span class="sxs-lookup"><span data-stu-id="242a9-255">96</span></span> |
| | | | | | | |

## <a name="next-steps"></a><span data-ttu-id="242a9-256">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="242a9-256">Next steps</span></span>

> [!div class="nextstepaction"]
>[<span data-ttu-id="242a9-257">ฝังสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="242a9-257">Embed for your customers</span></span>](embed-sample-for-customers.md)

> [!div class="nextstepaction"]
>[<span data-ttu-id="242a9-258">ฝังตัวสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="242a9-258">Embed for your organization</span></span>](embed-sample-for-your-organization.md)

> [!div class="nextstepaction"]
> [<span data-ttu-id="242a9-259">ฝังตัวจากแอป</span><span class="sxs-lookup"><span data-stu-id="242a9-259">Embed from apps</span></span>](./index.yml)