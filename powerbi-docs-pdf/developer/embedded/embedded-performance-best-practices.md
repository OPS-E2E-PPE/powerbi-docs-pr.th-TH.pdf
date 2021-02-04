---
title: แนวทางปฏิบัติที่ดีที่สุดสำหรับประสิทธิภาพการวิเคราะห์แบบฝังตัวของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้มีคำแนะนำสำหรับแนวทางปฏิบัติที่ดีที่สุดสำหรับการวิเคราะห์แบบฝังตัวของ Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 12/12/2018
ms.openlocfilehash: f8bf41ae9a4b6f2e16aae2c05df8fa4448a0457c
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888799"
---
# <a name="power-bi-embedded-analytics-performance-best-practices"></a><span data-ttu-id="f3b2f-104">แนวทางปฏิบัติที่ดีที่สุดสำหรับประสิทธิภาพการวิเคราะห์แบบฝังตัวของ Power BI</span><span class="sxs-lookup"><span data-stu-id="f3b2f-104">Power BI embedded analytics performance best practices</span></span>

<span data-ttu-id="f3b2f-105">บทความนี้มีคำแนะนำสำหรับการแสดงรายงาน แดชบอร์ด และไทล์ในแอปพลิเคชันของคุณได้เร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="f3b2f-105">This article provides recommendations for faster rendering of reports, dashboards, and tiles in your application.</span></span>

> [!Note]
> <span data-ttu-id="f3b2f-106">โปรดจำไว้ว่าเวลาการโหลดส่วนใหญ่จะขึ้นอยู่กับองค์ประกอบที่เกี่ยวข้องกับรายงานและข้อมูลของตัวเองรวมถึงภาพ ขนาดของข้อมูล และความซับซ้อนของคิวรีและหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="f3b2f-106">Remember that loading time mainly depends on elements relevant to the report and data itself, including visuals, the size of the data, and the complexity of the queries and measures.</span></span> <span data-ttu-id="f3b2f-107">สำหรับข้อมูลเพิ่มเติม โปรดดู[คำแนะนำการปรับให้เหมาะสมสำหรับ Power BI](../../guidance/power-bi-optimization.md)</span><span class="sxs-lookup"><span data-stu-id="f3b2f-107">For more information, see the [Power BI optimization guide](../../guidance/power-bi-optimization.md).</span></span>

## <a name="update-tools-and-sdk-packages"></a><span data-ttu-id="f3b2f-108">เครื่องมืออัปเดตและแพคเกจ SDK</span><span class="sxs-lookup"><span data-stu-id="f3b2f-108">Update tools and SDK packages</span></span>

<span data-ttu-id="f3b2f-109">ปรับปรุงเครื่องมือและแพคเกจ SDK ให้ทันสมัยอยู่เสมอ</span><span class="sxs-lookup"><span data-stu-id="f3b2f-109">Keep tools and SDK packages up-to-date.</span></span>

* <span data-ttu-id="f3b2f-110">ใช้ [Power Bi Desktop](https://powerbi.microsoft.com/desktop/) เวอร์ชันล่าสุดเสมอ</span><span class="sxs-lookup"><span data-stu-id="f3b2f-110">Always use the latest version of [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span></span>

* <span data-ttu-id="f3b2f-111">ติดตั้ง [Power BI client SDK](https://github.com/Microsoft/PowerBI-JavaScript) เวอร์ชันล่าสุด</span><span class="sxs-lookup"><span data-stu-id="f3b2f-111">Install the latest version of the [Power BI client SDK](https://github.com/Microsoft/PowerBI-JavaScript).</span></span> <span data-ttu-id="f3b2f-112">เรายังคงมีการปรับปรุงประสิทธิภาพเพิ่มเติมอย่างต่อเนื่อง ดังนั้นอย่าลืมที่จะติดตามการอัปเดตจากเรา</span><span class="sxs-lookup"><span data-stu-id="f3b2f-112">We continuously release additional enhancements, so make sure to follow up from time to time.</span></span>

## <a name="embed-parameters"></a><span data-ttu-id="f3b2f-113">พารามิเตอร์แบบฝัง</span><span class="sxs-lookup"><span data-stu-id="f3b2f-113">Embed parameters</span></span>

<span data-ttu-id="f3b2f-114">วิธี`powerbi.embed(element, config)`การรับองค์ประกอบและการกำหนดค่า ตัวเลขพารามิเตอร์ ประกอบด้วยเขตข้อมูลที่มีผลกระทบต่อประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="f3b2f-114">The `powerbi.embed(element, config)` method receives an element and a config. The config parameter includes fields that have performance implications.</span></span>

### <a name="embed-url"></a><span data-ttu-id="f3b2f-115">URL แบบฝัง</span><span class="sxs-lookup"><span data-stu-id="f3b2f-115">Embed URL</span></span>

<span data-ttu-id="f3b2f-116">หลีกเลี่ยงการสร้าง URL แบบฝังด้วยตัวคุณเอง</span><span class="sxs-lookup"><span data-stu-id="f3b2f-116">Avoid generating the embed URL yourself.</span></span> <span data-ttu-id="f3b2f-117">แต่คุณควรตรวจสอบให้แน่ใจว่าคุณได้รับ URL แบบฝัง โดยการเรียก API [รับรายงาน](/rest/api/power-bi/reports/getreportsingroup), [รับแดชบอร์ด](/rest/api/power-bi/dashboards/getdashboardsingroup) หรือ[รับไทล์](/rest/api/power-bi/dashboards/gettilesingroup)</span><span class="sxs-lookup"><span data-stu-id="f3b2f-117">Instead, make sure you get the Embed URL by calling [Get reports](/rest/api/power-bi/reports/getreportsingroup), [Get dashboards](/rest/api/power-bi/dashboards/getdashboardsingroup), or [Get tiles](/rest/api/power-bi/dashboards/gettilesingroup) API.</span></span> <span data-ttu-id="f3b2f-118">เราได้เพิ่มพารามิเตอร์ใหม่ใน URL ที่เรียกว่า **_config_** ซึ่งใช้สำหรับการปรับปรุงประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="f3b2f-118">We added a new parameter to the URL called **_config_**, which is used for performance improvements.</span></span>

### <a name="permissions"></a><span data-ttu-id="f3b2f-119">การอนุญาต</span><span class="sxs-lookup"><span data-stu-id="f3b2f-119">Permissions</span></span>

<span data-ttu-id="f3b2f-120">ระบุสิทธิ **ดู** หากคุณไม่ต้องการฝังรายงานในโหมดแก้ไข</span><span class="sxs-lookup"><span data-stu-id="f3b2f-120">Provide **View** permissions if you're not intending to embed a report in edit mode.</span></span> <span data-ttu-id="f3b2f-121">โค้ดที่ฝังด้วยวิธีนี้จะไม่เริ่มต้นคอมโพเนนต์ซึ่งใช้สำหรับโหมดแก้ไข</span><span class="sxs-lookup"><span data-stu-id="f3b2f-121">This way, embedded code doesn't initialize components, which are used in edit mode.</span></span>

### <a name="filters-bookmarks-and-slicers"></a><span data-ttu-id="f3b2f-122">ตัวกรอง บุ๊กมาร์ก และตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f3b2f-122">Filters, bookmarks, and slicers</span></span>

<span data-ttu-id="f3b2f-123">โดยปกติ วิชวลในรายงานจะถูกบันทึกด้วยข้อมูลที่แคช</span><span class="sxs-lookup"><span data-stu-id="f3b2f-123">Usually, report visuals are saved with cached data.</span></span> <span data-ttu-id="f3b2f-124">ข้อมูลที่แคชถูกนำมาใช้เพื่อประสิทธิภาพการทำงานที่ดีมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="f3b2f-124">The cached data is used to give perceived performance.</span></span> <span data-ttu-id="f3b2f-125">รายงานจะแสดงข้อมูลที่แคชขณะดำเนินการคิวรี</span><span class="sxs-lookup"><span data-stu-id="f3b2f-125">Reports render cached data while queries are executed.</span></span> <span data-ttu-id="f3b2f-126">ถ้ามีการระบุตัวกรองบุ๊กมาร์กหรือการแบ่งส่วนข้อมูลที่แคชไว้ไม่เกี่ยวข้องกันกับภาพจะแสดงขึ้นหลังจากที่มีการสิ้นสุดแบบสอบถามวิชวลเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f3b2f-126">If filters, bookmarks, or slicers are provided, cached data isn't relevant and the visuals are rendered only after the visual query has ended.</span></span>

<span data-ttu-id="f3b2f-127">ถ้าคุณฝังรายงานที่มีตัวกรองเดียวกันdyบุ๊กมาร์กและตัวแบ่งส่วนข้อมูลเพื่อปรับปรุงประสิทธิภาพการทำงานของคุณ ให้บันทึกรายงานด้วยตัวกรองบุ๊กมาร์กและแบ่งส่วนข้อมูลที่ใช้อยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="f3b2f-127">If you embed reports with the same filters, bookmarks, and slicers, to improve your performance, save the report with the filters, bookmarks, and slicers already applied.</span></span> <span data-ttu-id="f3b2f-128">ซึ่งแสดงรายงานด้วยข้อมูลที่แคชไว้ซึ่งรวมถึงตัวกรองบุ๊กมาร์กและตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f3b2f-128">This renders the report with the cached data which includes the filters, bookmarks, and slicers.</span></span>

## <a name="switching-between-reports"></a><span data-ttu-id="f3b2f-129">การสลับไปมาระหว่างรายงาน</span><span class="sxs-lookup"><span data-stu-id="f3b2f-129">Switching between reports</span></span>

<span data-ttu-id="f3b2f-130">เมื่อฝังรายงานหลายฉบับไปยัง iframe เดียวกันไม่ต้องสร้าง iframe ใหม่สำหรับแต่ละรายงาน</span><span class="sxs-lookup"><span data-stu-id="f3b2f-130">When embedding multiple reports to the same iframe, don't generate a new iframe for each report.</span></span> <span data-ttu-id="f3b2f-131">ให้ใช้`powerbi.embed(element, config)`กับการกำหนดค่าที่แตกต่างกันแทนเพื่อฝังรายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="f3b2f-131">Instead, use `powerbi.embed(element, config)` with a different config to embed the new report.</span></span>

> [!NOTE]
> <span data-ttu-id="f3b2f-132">การสลับระหว่างรายงานเมื่อทำการฝังสำหรับลูกค้าของคุณ (เรียกอีกอย่างว่าสถานการณ์ 'แอปเป็นเจ้าของข้อมูล') ต้องใช้โทเค็นการฝังที่มีสิทธิ์ในการรายงานและชุดข้อมูลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f3b2f-132">Switching between reports when embedding for your customers (also known as an 'app owns data' scenario), requires the use of an embed token with permissions to all reports and datasets.</span></span> <span data-ttu-id="f3b2f-133">สำหรับข้อมูลเพิ่มเติมดู [สร้างโทเค็น API](/rest/api/power-bi/embedtoken/generatetoken)</span><span class="sxs-lookup"><span data-stu-id="f3b2f-133">For more information, see the [generate token API](/rest/api/power-bi/embedtoken/generatetoken).</span></span>

## <a name="query-caching"></a><span data-ttu-id="f3b2f-134">การแคชคิวรี</span><span class="sxs-lookup"><span data-stu-id="f3b2f-134">Query caching</span></span>

<span data-ttu-id="f3b2f-135">องค์กรที่มีความจุของ Power BI Premium หรือความจุใน Power BI แบบฝังตัว สามารถใช้ประโยชน์จากการแคชคิวรีเพื่อให้รายงานที่เกี่ยวข้องกับชุดข้อมูลแสดงผลเร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="f3b2f-135">Organizations with Power BI Premium capacity or Power BI Embedded capacity can take advantage of query caching to speed up reports associated with a dataset.</span></span>

<span data-ttu-id="f3b2f-136">[เรียนรู้เพิ่มเติมเกี่ยวกับการแคชของแบบสอบถามใน Power BI](../../connect-data/power-bi-query-caching.md)</span><span class="sxs-lookup"><span data-stu-id="f3b2f-136">[Learn more about query caching in Power BI](../../connect-data/power-bi-query-caching.md).</span></span>

## <a name="preload"></a><span data-ttu-id="f3b2f-137">พรีโหลด</span><span class="sxs-lookup"><span data-stu-id="f3b2f-137">Preload</span></span>

<span data-ttu-id="f3b2f-138">ใช้ `powerbi.preload()` เพื่อปรับปรุงประสิทธิภาพการทำงานของผู้ใช้ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="f3b2f-138">Use `powerbi.preload()` to improve the end-user performance.</span></span> <span data-ttu-id="f3b2f-139">เมธอด `powerbi.preload()` จะดาวน์โหลด Javascript, ไฟล์ css และวัตถุอื่นๆ ซึ่งจะนำไปใช้ในภายหลังเพื่อฝังในรายงาน</span><span class="sxs-lookup"><span data-stu-id="f3b2f-139">The method `powerbi.preload()` downloads Javascript, css files, and other artifacts, which are used later to embed a report.</span></span>

<span data-ttu-id="f3b2f-140">เรียกใช้ `powerbi.preload()` หากคุณไม่ได้ฝังรายงานไว้ทันที</span><span class="sxs-lookup"><span data-stu-id="f3b2f-140">Call `powerbi.preload()` if you're not embedding the report immediately.</span></span> <span data-ttu-id="f3b2f-141">ตัวอย่างเช่น ถ้าเนื้อหาของ Power BI แบบฝังตัวไม่ปรากฏในโฮมเพจ ให้ใช้ `powerbi.preload()` เพื่อดาวน์โหลดและแคชในวัตถุที่ใช้สำหรับการฝังเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="f3b2f-141">For example, if the embedded Power BI content doesn't appear in the home page, use `powerbi.preload()` to download and cache the artifacts that are used for embedding the content.</span></span>

## <a name="bootstrapping-the-iframe"></a><span data-ttu-id="f3b2f-142">การบูทสเตรป iframe</span><span class="sxs-lookup"><span data-stu-id="f3b2f-142">Bootstrapping the iframe</span></span>

> [!NOTE]
> <span data-ttu-id="f3b2f-143">จำเป็นต้องใช้ [Power BI ไคลเอ็นต์ SDK](https://github.com/Microsoft/PowerBI-JavaScript) เวอร์ชัน 2.9 ในการบูทสเตรป iframe</span><span class="sxs-lookup"><span data-stu-id="f3b2f-143">[Power BI client SDK](https://github.com/Microsoft/PowerBI-JavaScript) version 2.9 is required to bootstrap the iframe.</span></span>

<span data-ttu-id="f3b2f-144">`powerbi.bootstrap(element, config)` ช่วยให้คุณสามารถเริ่มต้นการฝังก่อนพารามิเตอร์ที่จำเป็นทั้งหมดจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f3b2f-144">`powerbi.bootstrap(element, config)` allows you to start embedding before all required parameters are available.</span></span> <span data-ttu-id="f3b2f-145">API บูทสเตรปจะเตรียมและเริ่มต้นใช้งาน iframe</span><span class="sxs-lookup"><span data-stu-id="f3b2f-145">The bootstrap API prepares and initializes the iframe.</span></span>
<span data-ttu-id="f3b2f-146">เมื่อใช้ API บูทสเตรป จะยังคงจำเป็นต้องเรียกใช้ `powerbi.embed(element, config)` บนองค์ประกอบ HTML เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="f3b2f-146">When using the bootstrap API, it's still required to call `powerbi.embed(element, config)` on the same HTML element.</span></span>

<span data-ttu-id="f3b2f-147">ตัวอย่างเช่น หนึ่งในกรณีการใช้งานสำหรับคุณลักษณะนี้คือการเรียกใช้งานการบูทสเตรป iframe และการเรียกใช้ที่ทำงานอยู่ส่วนหลังสำหรับการฝังแบบขนาน</span><span class="sxs-lookup"><span data-stu-id="f3b2f-147">For example, one of the use cases for this feature, is to run the iframe bootstrap and the back-end calls for embedding, in parallel.</span></span>
> [!TIP]
> <span data-ttu-id="f3b2f-148">ใช้ API บูทสเตรปในขณะที่คุณสามารถสร้าง iframe ก่อนที่ผู้ใช้ปลายทางจะมองเห็นได้</span><span class="sxs-lookup"><span data-stu-id="f3b2f-148">Use the bootstrap API when it's possible to generate the iframe before it's visible to the end user.</span></span>

<span data-ttu-id="f3b2f-149">[เรียนรู้เพิ่มเติมเกี่ยวกับ iframe บูทสเตรป](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Bootstrap-For-Better-Performance)</span><span class="sxs-lookup"><span data-stu-id="f3b2f-149">[Learn more about iframe bootstrap](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Bootstrap-For-Better-Performance).</span></span>

## <a name="measure-performance"></a><span data-ttu-id="f3b2f-150">วัดประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="f3b2f-150">Measure performance</span></span>

### <a name="performance-events"></a><span data-ttu-id="f3b2f-151">ประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="f3b2f-151">Performance events</span></span>

<span data-ttu-id="f3b2f-152">ในการวัดประสิทธิภาพการทำงานแบบฝังตัวคุณอาจใช้สองเหตุการณ์:</span><span class="sxs-lookup"><span data-stu-id="f3b2f-152">To measure embedded performance, you may use two events:</span></span>

1. <span data-ttu-id="f3b2f-153">เหตุการณ์ที่โหลด: เวลาจนกว่าจะมีการเตรียมใช้งานรายงาน (โลโก้ Power BI จะหายไปเมื่อโหลดเสร็จสิ้น)</span><span class="sxs-lookup"><span data-stu-id="f3b2f-153">Loaded event: The time until the report is initialized (the Power BI logo will disappear when the load is finished).</span></span>
2. <span data-ttu-id="f3b2f-154">เหตุการณ์การแสดงผล: แสดงผลแล้ว: เวลาจนกว่ารายงานทั้งหมดจะแสดงผลโดยใช้ข้อมูลจริง</span><span class="sxs-lookup"><span data-stu-id="f3b2f-154">Rendered event: The time until the report is fully rendered, using the actual data.</span></span> <span data-ttu-id="f3b2f-155">เหตุการณ์ที่แสดงผลถูกเรียกใช้ในแต่ละครั้งที่มีการแสดงผลรายงานอีกครั้ง (ยกตัวอย่างเช่นหลังจากใช้ตัวกรอง)</span><span class="sxs-lookup"><span data-stu-id="f3b2f-155">The rendered event is fired each time the report is re-rendered (for example, after applying filters).</span></span> <span data-ttu-id="f3b2f-156">ในการวัดรายงาน คุณควรแน่ใจว่าคุณทำการคำนวณในเหตุการณ์ที่เกิดขึ้นครั้งแรกแล้ว</span><span class="sxs-lookup"><span data-stu-id="f3b2f-156">To measure a report, make sure you do the calculations on the first raised event.</span></span>

<span data-ttu-id="f3b2f-157">ข้อมูลที่แคชไว้จะถูกแสดงเมื่อพร้อมใช้งานแต่ไม่มีการสร้างเหตุการณ์เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f3b2f-157">Cached data is rendered when available but no additional event is generated.</span></span>

<span data-ttu-id="f3b2f-158">[เรียนรู้เพิ่มเติมเกี่ยวกับการจัดการเหตุการณ์](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Handling-Events)</span><span class="sxs-lookup"><span data-stu-id="f3b2f-158">[Learn more about event handling](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Handling-Events).</span></span>

### <a name="performance-analyzer"></a><span data-ttu-id="f3b2f-159">ตัววิเคราะห์ประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="f3b2f-159">Performance Analyzer</span></span>

<span data-ttu-id="f3b2f-160">เมื่อต้องการตรวจสอบประสิทธิภาพการทำงานขององค์ประกอบรายงานคุณอาจใช้ตัววิเคราะห์ประสิทธิภาพใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="f3b2f-160">To examine the performance of the report elements, you might use the Performance Analyzer in Power BI Desktop.</span></span>
<span data-ttu-id="f3b2f-161">ตัววิเคราะห์ประสิทธิภาพการทำงานจะช่วยให้คุณสามารถดูและบันทึกบันทึกที่วัดว่าแต่ละองค์ประกอบรายงานของคุณดำเนินการได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="f3b2f-161">The Performance Analyzer will allow you to see and record logs that measure how each of your report elements performs.</span></span>

<span data-ttu-id="f3b2f-162">[เรียนรู้เพิ่มเติมเกี่ยวกับตัววิเคราะห์ประสิทธิภาพ](../../create-reports/desktop-performance-analyzer.md)</span><span class="sxs-lookup"><span data-stu-id="f3b2f-162">[Learn more about Performance Analyzer](../../create-reports/desktop-performance-analyzer.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f3b2f-163">โปรดอย่าลืมเปรียบเทียบประสิทธิภาพรายงานแบบฝังตัวเพื่อประสิทธิภาพการทำงานบน powerbi.com</span><span class="sxs-lookup"><span data-stu-id="f3b2f-163">Always remember to compare the embedded report performance to the performance on powerbi.com.</span></span> <span data-ttu-id="f3b2f-164">ซึ่งอาจช่วยให้คุณเข้าใจจุดเริ่มต้นของปัญหาด้านประสิทธิภาพการทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="f3b2f-164">This might help you understand the origin of your performance issues</span></span>

## <a name="next-steps"></a><span data-ttu-id="f3b2f-165">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="f3b2f-165">Next steps</span></span>

* [<span data-ttu-id="f3b2f-166">คำแนะนำการปรับให้เหมาะสมสำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="f3b2f-166">Power BI optimization guide</span></span>](../../guidance/power-bi-optimization.md)
* [<span data-ttu-id="f3b2f-167">วิธีการแก้ไขปัญหาแบบฝังตัวของ Power BI</span><span class="sxs-lookup"><span data-stu-id="f3b2f-167">How to troubleshoot Power BI embedded analytics issues</span></span>](embedded-troubleshoot.md)
* [<span data-ttu-id="f3b2f-168">คำถามที่พบบ่อยเกี่ยวกับการวิเคราะห์แบบฝังตัวของ Power BI</span><span class="sxs-lookup"><span data-stu-id="f3b2f-168">Power BI embedded analytics FAQ</span></span>](embedded-faq.md)