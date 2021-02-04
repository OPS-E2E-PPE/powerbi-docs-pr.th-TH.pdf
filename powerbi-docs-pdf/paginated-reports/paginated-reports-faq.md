---
title: รายงานที่มีการแบ่งหน้าใน Power BI คำถามที่ถามบ่อย
description: บทความนี้จะตอบคำถามที่พบบ่อยเกี่ยวกับรายงานแบบแบ่งหน้า รายงานเหล่านี้คือเอาต์พุตที่มีการจัดรูปแบบสูงและเป็นแบบพิกเซลสมบูรณ์แบบที่เหมาะกับการพิมพ์หรือการสร้าง PDF
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: report-builder
ms.topic: conceptual
ms.date: 10/19/2020
ms.openlocfilehash: 7cba43ff6339ce890ca2f4f1744282648eaf877b
ms.sourcegitcommit: ccf53e87ff7cba1fcd9d2cca761a561e62933f90
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/04/2020
ms.locfileid: "93297890"
---
# <a name="paginated-reports-in-power-bi-faq"></a><span data-ttu-id="1d7b9-104">รายงานที่มีการแบ่งหน้าใน Power BI คำถามที่ถามบ่อย</span><span class="sxs-lookup"><span data-stu-id="1d7b9-104">Paginated reports in Power BI: FAQ</span></span> 

<span data-ttu-id="1d7b9-105">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span><span class="sxs-lookup"><span data-stu-id="1d7b9-105">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span></span> 

<span data-ttu-id="1d7b9-106">บทความนี้จะตอบคำถามที่พบบ่อยเกี่ยวกับรายงานแบบแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="1d7b9-106">This article answers frequently asked questions about paginated reports.</span></span> <span data-ttu-id="1d7b9-107">รายงานเหล่านี้คือเอาต์พุตที่มีการจัดรูปแบบสูงและเป็นแบบพิกเซลสมบูรณ์แบบที่เหมาะกับการพิมพ์หรือการสร้าง PDF</span><span class="sxs-lookup"><span data-stu-id="1d7b9-107">These reports are highly formatted, pixel-perfect output optimized for printing or PDF generation.</span></span> <span data-ttu-id="1d7b9-108">ที่เรียกว่า "แบบแบ่งหน้า" เนื่องจากมีการจัดรูปแบบให้พอดีกับหน้าหลายหน้า</span><span class="sxs-lookup"><span data-stu-id="1d7b9-108">They're called "paginated" because they're formatted to fit well on multiple pages.</span></span> <span data-ttu-id="1d7b9-109">รายงานแบบแบ่งหน้านั้นมาจากเทคโนโลยีรายงาน RDL ใน SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="1d7b9-109">Paginated reports are based on the RDL report technology in SQL Server Reporting Services.</span></span> 

<span data-ttu-id="1d7b9-110">บทความนี้ตอบคำถามทั่วไปที่ผู้คนสงสัยเกี่ยวกับรายงานแบบแบ่งหน้าใน Power BI Premium และเกี่ยวกับตัวสร้างรายงาน อันเป็นเครื่องมือเดี่ยวสำหรับเขียนรายงานแบบแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="1d7b9-110">This article answers many common questions people have about paginated reports in Power BI Premium, and about Report Builder, the standalone tool for authoring paginated reports.</span></span> <span data-ttu-id="1d7b9-111">คุณต้องมีสิทธิ์การใช้งาน Power BI Pro ในการที่จะเผยแพร่รายงานไปยังบริการ</span><span class="sxs-lookup"><span data-stu-id="1d7b9-111">You need a Power BI Pro license to publish a report to the service.</span></span> <span data-ttu-id="1d7b9-112">คุณสามารถเผยแพร่และแบ่งปันรายงานที่มีการแบ่งหน้าได้ในพื้นที่ทำงานของฉัน หรือในพื้นที่ทำงาน ตราบใดที่พื้นที่ทำงานอยู่ในความจุ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="1d7b9-112">You can publish and share paginated reports in your My Workspace or in workspaces, as long as the workspace is in a Power BI Premium capacity.</span></span> 

## <a name="administration"></a><span data-ttu-id="1d7b9-113">การดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="1d7b9-113">Administration</span></span>

### <a name="what-size-premium-capacity-do-i-need-for-paginated-reports"></a><span data-ttu-id="1d7b9-114">ฉันต้องมีความจุพรีเมียมขนาดเท่าใดสำหรับรายงานแบบแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="1d7b9-114">What size Premium capacity do I need for paginated reports?</span></span>

<span data-ttu-id="1d7b9-115">ปริมาณงานของรายงานแบบแบ่งหน้าใช้ได้กับ P1 – P3 SKU</span><span class="sxs-lookup"><span data-stu-id="1d7b9-115">The paginated reports workload is available on P1 – P3 SKUs.</span></span>  <span data-ttu-id="1d7b9-116">คุณยังสามารถใช้กับ A4 - A6 SKUs สำหรับสถานการณ์การฝังหรือทดสอบ/พัฒนา</span><span class="sxs-lookup"><span data-stu-id="1d7b9-116">You may also use it with A4 – A6 SKUs for embed or test/dev scenarios.</span></span>

### <a name="what-is-the-maximum-memory-threshold-i-can-put-for-paginated-reports-in-my-capacity"></a><span data-ttu-id="1d7b9-117">ขีดจำกัดหน่วยความจำสูงสุดเท่าไรที่ฉันสามารถวางให้รายงานแบบแบ่งหน้าในความจุของฉันได้</span><span class="sxs-lookup"><span data-stu-id="1d7b9-117">What is the maximum memory threshold I can put for paginated reports in my capacity?</span></span>

<span data-ttu-id="1d7b9-118">คุณอาจใช้หน่วยความจำเป็น 100% สำหรับปริมาณงานนี้</span><span class="sxs-lookup"><span data-stu-id="1d7b9-118">You may use up to 100% of the memory for this workload.</span></span>

### <a name="how-does-user-access-work-for-paginated-reports"></a><span data-ttu-id="1d7b9-119">ผู้ใช้จะเข้าถึงรายงานแบบแบ่งหน้าได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="1d7b9-119">How does user access work for paginated reports?</span></span>

<span data-ttu-id="1d7b9-120">ผู้ใช้สามารถเข้าถึงรายงานแบบแบ่งหน้าได้ด้วยวิธีเดียวกันกับที่ใช้เข้าถึงเนื้อหาอื่นๆ ทั้งหมดในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="1d7b9-120">User access for paginated reports is the same as user access for all other content in the Power BI service</span></span> 

### <a name="how-do-i-turn-onoff-my-paginated-reports-workload"></a><span data-ttu-id="1d7b9-121">ฉันจะปิด/เปิดปริมาณงานของรายงานแบบแบ่งหน้าได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="1d7b9-121">How do I turn on/off my paginated reports workload?</span></span>

<span data-ttu-id="1d7b9-122">ผู้ดูแลความจุสามารถเปิดหรือปิดปริมาณงานแบบแบ่งหน้าได้ในหน้าพอร์ทัลผู้ดูแลความจุ</span><span class="sxs-lookup"><span data-stu-id="1d7b9-122">The capacity admin can enable or disable the paginated reports workload in the capacity admin portal page.</span></span>  <span data-ttu-id="1d7b9-123">ตามค่าเริ่มต้น ปริมาณงานจะถูกเปิดใช้งานสำหรับความจุใหม่ที่คุณสร้างขึ้นแต่จะไม่มีการใช้ความจำจนกว่าคุณจะอัปโหลดรายงานเลขหน้าแรกของคุณ</span><span class="sxs-lookup"><span data-stu-id="1d7b9-123">By default, the workload will be on for any new capacities you create, but will not consume memory until you upload your first paginated report.</span></span>  

### <a name="how-can-i-monitor-usage-of-paginated-reports-in-my-tenant"></a><span data-ttu-id="1d7b9-124">ฉันจะตรวจสอบผู้ใช้รายงานแบบแบ่งหน้าในผู้เช่าของฉันได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="1d7b9-124">How can I monitor usage of paginated reports in my tenant?</span></span>

<span data-ttu-id="1d7b9-125">บันทึกการตรวจสอบจะบันทึกรายละเอียดการใช้ของรายงานประเภทนี้ไว้เมื่อมีเหตุการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1d7b9-125">The audit logs detail usage of this report type under the following events:</span></span>

- <span data-ttu-id="1d7b9-126">ดูรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="1d7b9-126">View Power BI Report</span></span>
- <span data-ttu-id="1d7b9-127">ลบรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="1d7b9-127">Delete Power BI report</span></span>
- <span data-ttu-id="1d7b9-128">สร้างรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="1d7b9-128">Create Power BI report</span></span>
- <span data-ttu-id="1d7b9-129">รายงาน Power BI ที่ดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="1d7b9-129">Downloaded Power BI report</span></span>

<span data-ttu-id="1d7b9-130">เขตข้อมูล ReportType มีค่า “PaginatedReport” ซึ่งเป็นการระบุว่ารายงานแบบแบ่งหน้านั้นตรงข้ามกับรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="1d7b9-130">The field ReportType has the value "PaginatedReport" to identify paginated as opposed to Power BI reports.</span></span>

<span data-ttu-id="1d7b9-131">นอกจากนี้ บันทึกการตรวจสอบยังให้เหตุการณ์ต่อไปนี้สำหรับรายงานแบบแบ่งหน้า:</span><span class="sxs-lookup"><span data-stu-id="1d7b9-131">Also, the audit logs provide the following events for paginated reports:</span></span>

- <span data-ttu-id="1d7b9-132">ชุดข้อมูล Power BI ที่ผูกกับเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="1d7b9-132">Binded Power BI dataset to gateway</span></span>
- <span data-ttu-id="1d7b9-133">ค้นพบแหล่งข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="1d7b9-133">Discover Power BI Datasource</span></span>
- <span data-ttu-id="1d7b9-134">TakeOverDataset</span><span class="sxs-lookup"><span data-stu-id="1d7b9-134">TakeOverDatasource</span></span>

### <a name="can-i-monitor-this-workload-through-the-premium-capacity-monitoring-app"></a><span data-ttu-id="1d7b9-135">ฉันสามารถตรวจสอบปริมาณงานนี้ผ่านแอปการตรวจสอบความจุพรีเมียมได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="1d7b9-135">Can I monitor this workload through the Premium Capacity Monitoring App?</span></span>

<span data-ttu-id="1d7b9-136">ใช่ การตรวจสอบนั้นมีอยู่ในแท็บใหม่ที่มีรายละเอียดที่เกี่ยวข้องเหมือนกับที่คุณมีสำหรับชุดข้อมูล Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="1d7b9-136">Yes, monitoring is available as a new tab with the same relevant details you have for your Power BI datasets.</span></span>

### <a name="do-i-need-a-pro-license-to-create-and-publish-paginated-reports"></a><span data-ttu-id="1d7b9-137">ฉันต้องมีสิทธิ์การใช้งาน Pro ในการที่จะสร้างและเผยแพร่รายงานแบบแบ่งหน้าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="1d7b9-137">Do I need a Pro license to create and publish paginated reports?</span></span>

<span data-ttu-id="1d7b9-138">คุณสามารถอัปโหลดรายงานแบบแบ่งหน้าไปยัง My Workspace ของคุณโดยไม่มีใบอนุญาตให้ใช้งานแบบ Pro ซึ่งมีอยู่ในความจุระดับ Premium</span><span class="sxs-lookup"><span data-stu-id="1d7b9-138">You can upload paginated reports to your My Workspace without a Pro license, provided it's in a Premium Capacity.</span></span>  <span data-ttu-id="1d7b9-139">สำหรับพื้นที่ทำงานอื่น คุณต้องมีสิทธิ์การใช้งาน Pro เพื่อเขียน และเผยแพร่เนื้อหาให้กับพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="1d7b9-139">For other workspaces, you must have a Pro license to author and publish content to them.</span></span> <span data-ttu-id="1d7b9-140">เราขอแนะนำให้คุณสามารถดาวน์โหลดและใช้ตัวสร้างรายงานของ Power BI โดยไม่มีสิทธิ์การใช้งาน Pro แต่คุณไม่สามารถเผยแพร่รายงานแบบแบ่งหน้าที่สร้างโดยไม่มีสิทธิ์การใช้งาน Pro ได้</span><span class="sxs-lookup"><span data-stu-id="1d7b9-140">We encourage you to download and use Power BI Report Builder even without the Pro license, but you can't publish the paginated reports you create without it.</span></span> 

### <a name="what-if-i-have-a-paginated-report-in-a-workspace-and-the-paginated-report-workload-is-turned-off"></a><span data-ttu-id="1d7b9-141">ถ้าฉันมีรายงานแบบแบ่งหน้าในพื้นที่ทำงานและปริมาณงานของรายงานแบบแบ่งหน้าปิดอยู่ จะเป็นอย่างไร</span><span class="sxs-lookup"><span data-stu-id="1d7b9-141">What if I have a paginated report in a workspace and the paginated report workload is turned off?</span></span>

<span data-ttu-id="1d7b9-142">คุณจะได้รับข้อความข้อผิดพลาด และคุณจะไม่สามารถดูรายงานของคุณได้จนกว่าจะเปิดปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="1d7b9-142">You receive an error message, and you can't view your report until the workload is turned back on.</span></span> <span data-ttu-id="1d7b9-143">คุณยังสามารถลบรายงานจากพื้นที่ทำงานได้</span><span class="sxs-lookup"><span data-stu-id="1d7b9-143">You can still delete the report from the workspace.</span></span>

### <a name="what-is-the-default-memory-for-each-of-the-premium-skus-that-support-paginated-reports"></a><span data-ttu-id="1d7b9-144">ความจำเริ่มต้นของ Premium SKU แต่ละตัวที่รองรับสำหรับรายงานแบบแบ่งหน้าคือเท่าไร</span><span class="sxs-lookup"><span data-stu-id="1d7b9-144">What is the default memory for each of the Premium SKUs that support paginated reports?</span></span>

<span data-ttu-id="1d7b9-145">ความจำเริ่มต้นใน Premium SKU แต่ละตัวสำหรับรายงานแบบแบ่งหน้า:</span><span class="sxs-lookup"><span data-stu-id="1d7b9-145">Default memory in each Premium SKU for paginated reports:</span></span>

- <span data-ttu-id="1d7b9-146">**P1/A4** : ค่าเริ่มต้น 20% ค่าต่ำสุด 10%</span><span class="sxs-lookup"><span data-stu-id="1d7b9-146">**P1/A4** : 20% default; 10% minimum</span></span>
- <span data-ttu-id="1d7b9-147">**P2/A5** : ค่าเริ่มต้น 20% ค่าต่ำสุด 5%</span><span class="sxs-lookup"><span data-stu-id="1d7b9-147">**P2/A5** : 20% default; 5% minimum</span></span>
- <span data-ttu-id="1d7b9-148">**P3/A6** : ค่าเริ่มต้น 20% ค่าต่ำสุด 2.5%</span><span class="sxs-lookup"><span data-stu-id="1d7b9-148">**P3/A6** : 20% default; 2.5% minimum</span></span>

<span data-ttu-id="1d7b9-149">ผู้ดูแลระบบของ Power BI สามารถปรับเปลี่ยนเปอร์เซ็นต์หน่วยความจำสูงสุดตามค่าเริ่มต้นในพอร์ทัลผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="1d7b9-149">Power BI admins can modify the default maximum memory percentage in the Admin portal.</span></span> <span data-ttu-id="1d7b9-150">ดูส่วนปริมาณงาน **รายงานที่มีการแบ่งหน้า** ภายใต้ **Power BI Premium** บนแท็บ **การตั้งค่าความจุ**</span><span class="sxs-lookup"><span data-stu-id="1d7b9-150">See the **Paginated Reports** workload section under **Power BI Premium** on the **Capacity settings** tab.</span></span>

:::image type="content" source="media/paginated-reports-faq/paginated-reports-capacity-settings.png" alt-text="แท็บการตั้งค่าความจุรายงานที่มีการแบ่งหน้า":::

## <a name="general"></a><span data-ttu-id="1d7b9-152">ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="1d7b9-152">General</span></span>

### <a name="when-should-i-use-a-paginated-report-vs-a-power-bi-report"></a><span data-ttu-id="1d7b9-153">ฉันควรใช้รายงานแบบแบ่งหน้าหรือรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="1d7b9-153">When should I use a paginated report vs. a Power BI report?</span></span>

<span data-ttu-id="1d7b9-154">รายงานแบบแบ่งหน้าเหมาะที่สุดในสถานการณ์ที่ต้องใช้เอาต์พุตที่มีการจัดรูปแบบสูงและเป็นพิกเซลสมบูรณ์แบบที่เหมาะกับการพิมพ์หรือการสร้าง PDF</span><span class="sxs-lookup"><span data-stu-id="1d7b9-154">Paginated reports are best for scenarios that require a highly formatted, pixel-perfect output optimized for printing or PDF generation.</span></span>  <span data-ttu-id="1d7b9-155">ตัวอย่างที่เห็นได้ชัดคือ เมื่อคุณต้องการสร้างงบกำไรขาดทุน คุณควรสร้างในรูปแบบของรายงานแบบแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="1d7b9-155">A profit and loss statement is a good example of the type of report you would probably want to create as a paginated report.</span></span>  

<span data-ttu-id="1d7b9-156">รายงาน power BI ได้รับการปรับให้เหมาะสำหรับการสำรวจและโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="1d7b9-156">Power BI reports are optimized for exploration and interactivity.</span></span>  <span data-ttu-id="1d7b9-157">เมื่อพนักงานขายต้องการแบ่งส่วนข้อมูลในรายงานยอดขายตัวเดียวกันโดยแยกตามเขตพื้นที่/อุตสาหกรรม/ลูกค้า แล้วดูการเปลี่ยนแปลงของตัวเลข การสร้างรายงาน Power BI จะดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="1d7b9-157">A sales report where different salespeople want to slice the data in the same report for their specific region/industry/customer and see how the numbers change would be best served by a Power BI report.</span></span>

<span data-ttu-id="1d7b9-158">สำหรับข้อมูลเพิ่มเติม ดู [เมื่อใช้รายงานที่มีการแบ่งหน้าใน Power BI](../guidance/report-paginated-or-power-bi.md)</span><span class="sxs-lookup"><span data-stu-id="1d7b9-158">For more information, see [When to use paginated reports in Power BI](../guidance/report-paginated-or-power-bi.md).</span></span>

### <a name="the-documentation-says-power-bi-report-builder-is-the-preferred-authoring-tool-can-i-create-paginated-reports-in-sql-server-data-tools-for-power-bi"></a><span data-ttu-id="1d7b9-159">เอกสารได้บอกว่าตัวสร้างรายงาน Power BI เป็นเครื่องมือการเขียนรายงานที่ผู้คนเลือกใช้</span><span class="sxs-lookup"><span data-stu-id="1d7b9-159">The documentation says Power BI Report Builder is the preferred authoring tool.</span></span> <span data-ttu-id="1d7b9-160">ฉันสามารถสร้างรายงานแบบแบ่งหน้าในเครื่องมือข้อมูลเซิร์ฟเวอร์ SQL ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="1d7b9-160">Can I create paginated reports in SQL Server Data Tools for Power BI?</span></span>

<span data-ttu-id="1d7b9-161">ได้ แต่บริการของ Power BI จะให้คุณอัปโหลดได้ครั้งละหนึ่งชุดเท่านั้น ดังนั้นในหลายๆ กรณีจึงยังไม่รองรับเครื่องมือข้อมูลเซิร์ฟเวอร์ SQL (SSDT) ให้ผู้เขียนได้ใช้</span><span class="sxs-lookup"><span data-stu-id="1d7b9-161">Yes, but the Power BI service only allows you to upload a single item at a time, so many of the scenarios authors use with SQL Server Data Tools (SSDT) aren't yet supported.</span></span> <span data-ttu-id="1d7b9-162">ดู [รายการฟีเจอร์ที่ไม่ได้รับการรับรอง](#what-paginated-report-features-in-ssrs-arent-yet-supported-in-power-bi) ฉบับเต็มได้ในภายหลัง ในส่วนคำถามที่พบบ่อยนี้</span><span class="sxs-lookup"><span data-stu-id="1d7b9-162">See the full [list of unsupported features](#what-paginated-report-features-in-ssrs-arent-yet-supported-in-power-bi) available later in this FAQ.</span></span>  

### <a name="what-versions-of-report-builder-do-you-support"></a><span data-ttu-id="1d7b9-163">คุณรองรับตัวสร้างรายงานเวอร์ชันใด</span><span class="sxs-lookup"><span data-stu-id="1d7b9-163">What version(s) of Report Builder do you support?</span></span>

<span data-ttu-id="1d7b9-164">เราเพิ่งเผยแพร่ตัวสร้างรายงาน Power BI ในฐานะเครื่องมือการเขียนหลักสำหรับรายงานแบบแบ่งหน้าในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="1d7b9-164">We released Power BI Report Builder as the primary authoring tool for paginated reports in the Power BI Service.</span></span> <span data-ttu-id="1d7b9-165">ติดตั้ง[ตัวสร้างรายงาน Power BI จากศูนย์ดาวน์โหลด Microsoft](https://aka.ms/pbireportbuilder)</span><span class="sxs-lookup"><span data-stu-id="1d7b9-165">Install [Power BI Report Builder from the Microsoft Download Center](https://aka.ms/pbireportbuilder).</span></span>

### <a name="how-do-i-move-existing-reports-i-have-saved-in-sql-server-reporting-services-to-power-bi"></a><span data-ttu-id="1d7b9-166">ฉันจะย้ายรายงานที่มีอยู่แล้วและบันทึกไว้ใน SQL Server Reporting Services ไปยัง Power BI ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="1d7b9-166">How do I move existing reports I have saved in SQL Server Reporting Services to Power BI?</span></span>

<span data-ttu-id="1d7b9-167">ขณะนี้โครงการบน GitHub สนับสนุนการย้ายเนื้อหาจาก SQL Server Reporting Services ไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="1d7b9-167">A project on GitHub now supports migrating content from SQL Server Reporting Services to Power BI.</span></span>  <span data-ttu-id="1d7b9-168">ดูรายละเอียดและดาวน์โหลดเครื่องมือที่นี่: [https://github.com/microsoft/RdlMigration](https://github.com/microsoft/RdlMigration)</span><span class="sxs-lookup"><span data-stu-id="1d7b9-168">View details and download the tool here: [https://github.com/microsoft/RdlMigration](https://github.com/microsoft/RdlMigration)</span></span>

### <a name="can-i-open-reports-and-publish-directly-to-the-service"></a><span data-ttu-id="1d7b9-169">ฉันสามารถเปิดรายงานและเผยแพร่ไปยังบริการโดยตรงได้เลยหรือไม่</span><span class="sxs-lookup"><span data-stu-id="1d7b9-169">Can I open reports and publish directly to the service?</span></span>

<span data-ttu-id="1d7b9-170">ใช่</span><span class="sxs-lookup"><span data-stu-id="1d7b9-170">Yes.</span></span> <span data-ttu-id="1d7b9-171">เราพึ่งจะเพิ่มส่วนสนับสนุนในการเปิดรายงานและเผยแพร่จากตัวสร้างรายงานไปยังบริการโดยตรงจากตัวสร้างรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="1d7b9-171">We've added support for opening reports and publishing them directly to the service from Power BI Report Builder.</span></span>

### <a name="what-paginated-report-features-in-ssrs-arent-yet-supported-in-power-bi"></a><span data-ttu-id="1d7b9-172">ฟีเจอร์ของรายงานแบบแบ่งหน้าตัวใดใน SSRS ที่ยังไม่ได้รับการรองรับใน Power BI</span><span class="sxs-lookup"><span data-stu-id="1d7b9-172">What paginated report features in SSRS aren't yet supported in Power BI?</span></span>

<span data-ttu-id="1d7b9-173">ในขณะนี้ รายงานแบบแบ่งหน้าไม่รองรับรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1d7b9-173">Currently, paginated reports don't support the following items:</span></span>

- <span data-ttu-id="1d7b9-174">แหล่งข้อมูลที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="1d7b9-174">Shared data sources</span></span>
- <span data-ttu-id="1d7b9-175">ชุดข้อมูลที่แชร์</span><span class="sxs-lookup"><span data-stu-id="1d7b9-175">Shared datasets</span></span>
- <span data-ttu-id="1d7b9-176">เข้าถึงรายละเอียดและคลิกผ่านรายงานอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="1d7b9-176">Drillthrough and click-through to other reports</span></span>
- <span data-ttu-id="1d7b9-177">รายงานที่เชื่อมโยงไว้</span><span class="sxs-lookup"><span data-stu-id="1d7b9-177">Linked reports</span></span>
- <span data-ttu-id="1d7b9-178">ฟอนต์แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="1d7b9-178">Custom fonts</span></span>

<span data-ttu-id="1d7b9-179">คุณจะได้รับข้อความข้อผิดพลาดหากคุณพยายามอัปโหลดไฟล์ที่มีฟีเจอร์ที่ไม่ได้รับการรองรับในบริการของ Power BI นอกเหนือจากการสลับ/โต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="1d7b9-179">You get an error message if you try to upload a file that has an unsupported feature in the Power BI service, other than toggle/sort.</span></span>

### <a name="what-data-sources-do-you-support-currently-for-paginated-reports"></a><span data-ttu-id="1d7b9-180">แหล่งข้อมูลใดบ้างที่คุณรับรองสำหรับรายงานแบบแบ่งหน้าในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="1d7b9-180">What data sources do you support currently for paginated reports?</span></span>

<span data-ttu-id="1d7b9-181">ดูบทความ [แหล่งข้อมูลที่ได้รับการสนับสนุนสำหรับรายงานที่มีการแบ่งหน้าใน Power BI](paginated-reports-data-sources.md) สำหรับรายการของแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1d7b9-181">See the article [Supported data sources for Power BI paginated reports](paginated-reports-data-sources.md) for a list of data sources.</span></span> 

### <a name="what-authentication-methods-do-you-support"></a><span data-ttu-id="1d7b9-182">คุณรองรับวิธีการรับรองความถูกต้องแบบใด</span><span class="sxs-lookup"><span data-stu-id="1d7b9-182">What authentication methods do you support?</span></span>

<span data-ttu-id="1d7b9-183">เรารับรอง SSO สำหรับ Azure Analysis Services, Azure SQL Database และแหล่งข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="1d7b9-183">We support SSO for Azure Analysis Services, Azure SQL Database, and Power BI data sources.</span></span>  <span data-ttu-id="1d7b9-184">นอกจากนี้ เรายังรองรับ OAuth สำหรับ Azure SQL Database และ Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="1d7b9-184">We also support OAuth for Azure SQL Database and Azure Analysis Services.</span></span>  <span data-ttu-id="1d7b9-185">สำหรับแหล่งข้อมูลอื่น ในตอนนี้ คุณต้องเก็บชื่อผู้ใช้และรหัสผ่านพร้อมแหล่งข้อมูลไว้ในพอร์ทัลหรือเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="1d7b9-185">For other data sources, you currently need to store a user name and password with the data source in the portal or gateway.</span></span>  

### <a name="can-i-use-a-power-bi-dataset-as-a-data-source-for-my-paginated-report"></a><span data-ttu-id="1d7b9-186">ฉันสามารถใช้ชุดข้อมูล Power BI เป็นแหล่งข้อมูลสำหรับรายงานแบบแบ่งหน้าได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="1d7b9-186">Can I use a Power BI dataset as a data source for my paginated report?</span></span>

<span data-ttu-id="1d7b9-187">ใช่ เรารองรับชุดข้อมูล Power BI เป็นแหล่งข้อมูลสำหรับรายงานของคุณที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="1d7b9-187">Yes, we support Power BI datasets as data sources for your paginated reports.</span></span>

### <a name="can-i-use-stored-procedures-through-the-gateway"></a><span data-ttu-id="1d7b9-188">ฉันสามารถใช้ขั้นตอนที่เก็บไว้ผ่านทางเกตเวย์ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="1d7b9-188">Can I use stored procedures through the Gateway?</span></span>

<span data-ttu-id="1d7b9-189">ใช่ กระบวนงานที่เก็บไว้ผ่านเกตเวย์ได้รับการรองรับสำหรับแหล่งข้อมูลเซิร์ฟเวอร์ SQL รวมทั้งที่ใช้พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="1d7b9-189">Yes, stored procedures through the Gateway are supported for SQL Server data sources, including those that use parameters.</span></span>

### <a name="what-export-formats-are-available-for-my-report-in-the-power-bi-service"></a><span data-ttu-id="1d7b9-190">ในบริการของ Power BI มีรูปแบบการส่งออกแบบใดบ้างที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="1d7b9-190">What export formats are available for my report in the Power BI service?</span></span>

<span data-ttu-id="1d7b9-191">คุณสามารถส่งออกไปยัง Microsoft Excel, Microsoft Word, Microsoft PowerPoint, PDF, .CSV, XML, และ MHTML ได้</span><span class="sxs-lookup"><span data-stu-id="1d7b9-191">You can export to Microsoft Excel, Microsoft Word, Microsoft PowerPoint, PDF, .CSV, XML, and MHTML.</span></span>

### <a name="can-i-print-paginated-reports"></a><span data-ttu-id="1d7b9-192">ฉันสามารถพิมพ์รายงานแบบแบ่งหน้าได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="1d7b9-192">Can I print paginated reports?</span></span>

<span data-ttu-id="1d7b9-193">ใช่ การพิมพ์นั้นพร้อมใช้งานสำหรับรายงานที่มีการแบ่งหน้าแล้ว รวมถึงการแสดงตัวอย่างก่อนพิมพ์ที่ปรับปรุงใหม่</span><span class="sxs-lookup"><span data-stu-id="1d7b9-193">Yes, printing is available for paginated reports, including a new and improved print preview experience.</span></span> 

### <a name="are-e-mail-subscriptions-available-for-paginated-reports"></a><span data-ttu-id="1d7b9-194">การสมัครใช้งานอีเมลสำหรับรายงานแบบแบ่งหน้าสามารถใช้ได้หรือยัง?</span><span class="sxs-lookup"><span data-stu-id="1d7b9-194">Are e-mail subscriptions available for paginated reports?</span></span>

<span data-ttu-id="1d7b9-195">ใช่ การสมัครใช้งานอีเมลที่จะรองรับการทำงานในรายงานแบบแบ่งหน้าอย่างเต็มรูปแบบ และรวมการรองรับรูปแบบไฟล์ที่แตกต่างหกรูปแบบและค่าพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="1d7b9-195">Yes, e-mail subscriptions are fully supported for paginated reports and include support for six different file formats and parameter values.</span></span>

### <a name="can-i-run-custom-code-in-my-report"></a><span data-ttu-id="1d7b9-196">ฉันสามารถเรียกใช้รหัสแบบกำหนดเองในรายงานของฉันได้ไหม</span><span class="sxs-lookup"><span data-stu-id="1d7b9-196">Can I run custom code in my report?</span></span>

<span data-ttu-id="1d7b9-197">ได้ เรารองรับการเรียกใช้รหัสในรายงานของคุณเช่นเดียวกับที่คุณสามารถทำได้ใน SSRS</span><span class="sxs-lookup"><span data-stu-id="1d7b9-197">Yes, we support the ability to run code in your reports as you can in SSRS.</span></span>

### <a name="can-i-use-power-bi-embedded-to-embed-my-paginated-reports-into-an-app-im-hosting"></a><span data-ttu-id="1d7b9-198">ฉันสามารถใช้ Power BI Embedded เพื่อฝังรายงานแบบแบ่งหน้าในแอปที่ฉันโฮสต์อยู่ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="1d7b9-198">Can I use Power BI embedded to embed my paginated reports into an app I'm hosting?</span></span>

<span data-ttu-id="1d7b9-199">การฝัง SaaS ซึ่งรวมถึงการสนับสนุนแบบฝังตัวที่ปลอดภัยพร้อมใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="1d7b9-199">SaaS embedding, including Secure Embed support, is already available.</span></span> <span data-ttu-id="1d7b9-200">สำหรับการฝัง PaaS โปรดดูที่บทช่วยสอน [ฝังรายงานที่มีการแบ่งหน้าของ Power BI ในแอปพลิเคชันสำหรับลูกค้าของคุณ](../developer/embedded/embed-paginated-reports-customers.md)</span><span class="sxs-lookup"><span data-stu-id="1d7b9-200">For PaaS embedding, refer to the [Embed Power BI paginated reports into an application for your customers](../developer/embedded/embed-paginated-reports-customers.md) tutorial.</span></span>

### <a name="can-i-drill-through-from-a-power-bi-report-to-a-paginated-report"></a><span data-ttu-id="1d7b9-201">ฉันสามารถลงรายละเอียดจากรายงาน Power BI ในรายงานแบบแบ่งหน้าได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="1d7b9-201">Can I drill through from a Power BI report to a paginated report?</span></span>

<span data-ttu-id="1d7b9-202">ใช่ สามารถทำได้โดยใช้พารามิเตอร์ URL ที่มีรายงานแบบแบ่งหน้าของบคุณ</span><span class="sxs-lookup"><span data-stu-id="1d7b9-202">Yes, this can be accomplished using URL parameters with your paginated reports.</span></span>

### <a name="can-i-share-my-paginated-report-content-through-a-power-bi-app"></a><span data-ttu-id="1d7b9-203">ฉันจะแชร์เนื้อหาของรายงานแบบแบ่งหน้าผ่านแอป Power BI ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="1d7b9-203">Can I share my paginated report content through a Power BI app?</span></span>

<span data-ttu-id="1d7b9-204">ใช่ รายงานแบบแบ่งหน้าจะรองรับการปรับใช้กับแอปจากพื้นที่ทำงานทั้ง v1 และ v2</span><span class="sxs-lookup"><span data-stu-id="1d7b9-204">Yes, paginated reports are supported to be deployed with apps from both v1 and v2 workspaces.</span></span> 

### <a name="will-other-report-specific-features-in-power-bi-like-pinning-report-tiles-to-dashboards-work-with-paginated-reports"></a><span data-ttu-id="1d7b9-205">ฟีเจอร์เฉพาะอื่นๆ ของรายงานใน Power BI เช่น การปักหมุดไทล์รายงานไปยังแดชบอร์ด จะใช้งานกับรายงานแบบแบ่งหน้าได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="1d7b9-205">Will other report-specific features in Power BI, like pinning report tiles to dashboards, work with paginated reports?</span></span>

<span data-ttu-id="1d7b9-206">เรามีแผนที่จะทำให้รายงานรองรับสถานการณ์ส่วนใหญ่ในบริการให้ได้มากที่สุด</span><span class="sxs-lookup"><span data-stu-id="1d7b9-206">We plan to have the reports support the same major scenarios in the service as much as possible.</span></span>  <span data-ttu-id="1d7b9-207">ตามหลักการแล้ว แม้ว่าเครื่องมือที่ใช้เขียนรายงานจะต่างกัน แต่เมื่อดูจากมุมของผู้บริโภค จะเห็นว่ามันเป็นเพียงแค่รายงานอีกตัวหนึ่งที่อยู่ในรายการในพอร์ทัล</span><span class="sxs-lookup"><span data-stu-id="1d7b9-207">Ideally, though the tool to author them is different, from a consumer perspective it's just another report in their list in the portal.</span></span> <span data-ttu-id="1d7b9-208">พวกเขาไม่สนใจว่าสร้างอย่างไร พวกเขาสามารถทำสิ่งที่ต้องการได้เลย</span><span class="sxs-lookup"><span data-stu-id="1d7b9-208">They don't care how it was created, they can accomplish what they need to.</span></span>  <span data-ttu-id="1d7b9-209">ตัวอย่างของแพริตีฟีเจอร์นี้ที่เห็นได้ชัดคือส่วนรองรับข้อคิดเห็นที่ได้วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="1d7b9-209">A good example of this feature parity is the planned comment support.</span></span> <span data-ttu-id="1d7b9-210">แม้ว่าตัวฟีเจอร์จะทำงานต่างกันเล็กน้อยเมื่อใช้กับรายงานแต่ละประเภท แต่คุณจะใช้ส่วนข้อคิดเห็นได้กับทั้งคู่</span><span class="sxs-lookup"><span data-stu-id="1d7b9-210">Though the feature itself may work slightly differently for each report type, you'll be able to use comments for both.</span></span>

### <a name="is-there-a-report-viewer-control-for-paginated-reports-in-the-power-bi-service"></a><span data-ttu-id="1d7b9-211">มีส่วนควบคุมตัวแสดงรายงานสำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI หรือไม่</span><span class="sxs-lookup"><span data-stu-id="1d7b9-211">Is there a report viewer control for paginated reports in the Power BI service?</span></span>

<span data-ttu-id="1d7b9-212">ไม่มี ตอนนี้ยังไม่มีส่วนควบคุมตัวแสดงรายงาน</span><span class="sxs-lookup"><span data-stu-id="1d7b9-212">No, a report viewer control isn't available currently.</span></span>

### <a name="can-you-search-for-paginated-reports-from-the-new-home-experience-in-the-power-bi-service"></a><span data-ttu-id="1d7b9-213">คุณสามารถค้นหารายงานแบบแบ่งหน้าจากส่วนใช้งานหน้าหลักตัวใหม่ในบริการของ Power BI ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="1d7b9-213">Can you search for paginated reports from the new Home experience in the Power BI service?</span></span>

<span data-ttu-id="1d7b9-214">ใช่ คุณสามารถค้นหารายงานแบบแบ่งหน้าของคุณจากหน้าหลักได้</span><span class="sxs-lookup"><span data-stu-id="1d7b9-214">Yes, you can now search for your paginated reports from Home.</span></span>  <span data-ttu-id="1d7b9-215">และคุณจะเห็นตัวรายงานอยู่ในส่วนใช้งานหน้าหลักใหม่ส่วนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="1d7b9-215">You also see them in other parts of the new Home experience.</span></span>

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="1d7b9-216">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="1d7b9-216">Considerations and troubleshooting</span></span>
<span data-ttu-id="1d7b9-217">นี่คือสิ่งที่ควรทราบเมื่อทำงานกับเขตข้อมูล DateTime ในรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="1d7b9-217">Here's something to keep in mind when working with DateTime fields in paginated reports.</span></span>

- <span data-ttu-id="1d7b9-218">ขณะนี้มีข้อจำกัดทั่วโลกบางอย่างที่เกี่ยวข้องกับพารามิเตอร์ DateTime</span><span class="sxs-lookup"><span data-stu-id="1d7b9-218">Currently there are some globalization limitations related to DateTime parameters.</span></span> <span data-ttu-id="1d7b9-219">พารามิเตอร์ DateTime ทั้งหมดในบริการของ Power BI จะถูกนำมาใช้ในรูปแบบสหรัฐอเมริกา (ดด/วว/ปปปป) โดยไม่คำนึงถึงวิธีที่คุณออกแบบ DataTime ในตัวสร้างรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="1d7b9-219">All DateTime parameters in the Power BI service are fetched in US format (MM/DD/YYYY) regardless of how you design the DataTime in Power BI Report Builder.</span></span>

<span data-ttu-id="1d7b9-220">เมื่อดูรายงานที่มีการแบ่งหน้าในบริการ Power BI เซสชันอาจหมดเวลาให้นำเสนอผู้ใช้ที่มีการแจ้งเตือนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1d7b9-220">When viewing paginated reports in the Power BI service, sessions may time out, presenting the user with the following notification:</span></span>

:::image type="content" source="media/paginated-reports-faq/expired-session-notification.png" alt-text="การแจ้งเตือนที่หมดอายุของเซสชันรายงานที่มีการแบ่งหน้า":::

- <span data-ttu-id="1d7b9-222">เซสชันจะหมดเวลาหลังจาก 60 นาทีของการไม่ได้ใช้งาน หรือก่อนหน้านี้เมื่ออุปกรณ์ถูกล็อกหรือไม่ได้ใช้งาน หรือเมื่อไม่มีการแสดงรายงานในแท็บ active ของเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="1d7b9-222">The session will time out after 60 minutes of inactivity, or earlier when the device is locked or inactive, or when the report isn't displayed in the active tab of the browser.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1d7b9-223">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="1d7b9-223">Next steps</span></span>

- [<span data-ttu-id="1d7b9-224">ติดตั้งตัวสร้างรายงาน Power BI จากศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="1d7b9-224">Install Power BI Report Builder from the Microsoft Download Center</span></span>](https://aka.ms/pbireportbuilder)
- [<span data-ttu-id="1d7b9-225">บทช่วยสอน: สร้างรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="1d7b9-225">Tutorial: Create a paginated report</span></span>](paginated-reports-quickstart-aw.md)
