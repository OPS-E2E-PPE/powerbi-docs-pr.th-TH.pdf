---
title: ส่งออก API ของรายงานการวิเคราะห์แบบฝังตัวของ Power BI สำหรับข้อมูลเชิงลึก BI ที่ฝังตัวได้ดีขึ้น
description: เรียนรู้วิธีการส่งออกรายงาน Power BI แบบฝังตัวเพื่อปรับปรุงประสบการณ์ การใช้งาน BI แบบฝังตัวของการวิเคราะห์ Power BI ของคุณ เปิดใช้งานข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.topic: how-to
ms.service: powerbi
ms.subservice: powerbi-developer
ms.date: 12/28/2020
ms.openlocfilehash: acd9d98b55697e8ca3729cad65a1ead8f01f6e62
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887028"
---
# <a name="export-power-bi-report-to-file-preview"></a><span data-ttu-id="cc1ff-104">ส่งออกรายงาน Power BI ไปยังไฟล์ (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-104">Export Power BI report to file (preview)</span></span>

<span data-ttu-id="cc1ff-105">`exportToFile`API เปิดใช้งานการส่งออกรายงาน Power BI โดยใช้การเรียกใช้ REST</span><span class="sxs-lookup"><span data-stu-id="cc1ff-105">The `exportToFile` API enables exporting a Power BI report by using a REST call.</span></span> <span data-ttu-id="cc1ff-106">รูปแบบไฟล์ต่อไปนี้ได้รับการรองรับ:</span><span class="sxs-lookup"><span data-stu-id="cc1ff-106">The following file formats are supported:</span></span>
* <span data-ttu-id="cc1ff-107">**.pptx** (PowerPoint)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-107">**.pptx** (PowerPoint)</span></span>
* <span data-ttu-id="cc1ff-108">**.pdf**</span><span class="sxs-lookup"><span data-stu-id="cc1ff-108">**.pdf**</span></span>
* <span data-ttu-id="cc1ff-109">**.png**</span><span class="sxs-lookup"><span data-stu-id="cc1ff-109">**.png**</span></span>
    * <span data-ttu-id="cc1ff-110">ขณะที่ส่งออกในรูปแบบ .png รายงานที่มีหลายหน้าจะถูกบีบอัดเป็นไฟล์ .zip</span><span class="sxs-lookup"><span data-stu-id="cc1ff-110">When exporting to a .png, a report with multiple pages is compressed into a .zip file</span></span>
    * <span data-ttu-id="cc1ff-111">แต่ละไฟล์ใน .zip จะแสดงหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="cc1ff-111">Each file in the .zip represents a report page</span></span>
    * <span data-ttu-id="cc1ff-112">ชื่อหน้าจะเหมือนกับค่าที่ส่งกลับของ API [รับหน้า](/rest/api/power-bi/reports/getpages)หรือ[รับหน้าในกลุ่ม](/rest/api/power-bi/reports/getpagesingroup)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-112">The page names are the same as the return values of the [Get Pages](/rest/api/power-bi/reports/getpages) or [Get Pages in Group](/rest/api/power-bi/reports/getpagesingroup) APIs</span></span>

## <a name="usage-examples"></a><span data-ttu-id="cc1ff-113">ตัวอย่างการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cc1ff-113">Usage examples</span></span>

<span data-ttu-id="cc1ff-114">คุณสามารถใช้ฟีเจอร์การส่งออกได้หลายวิธี</span><span class="sxs-lookup"><span data-stu-id="cc1ff-114">You can use the export feature in a variety of ways.</span></span> <span data-ttu-id="cc1ff-115">นี่เป็นตัวอย่างสองตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="cc1ff-115">Here are a couple of examples:</span></span>

* <span data-ttu-id="cc1ff-116">**ส่งไปยังปุ่มพิมพ์** - ในแอปพลิเคชันของคุณ ให้สร้างปุ่มที่เมื่อคลิกที่จะทริกเกอร์งานการส่งออก</span><span class="sxs-lookup"><span data-stu-id="cc1ff-116">**Send to print button** - In your application, create a button that when clicked on triggers an export job.</span></span> <span data-ttu-id="cc1ff-117">งานสามารถส่งออกรายงานที่เป็น .pdf หรือ .pptx และเมื่อเสร็จสมบูรณ์ ผู้ใช้จะสามารถรับไฟล์เป็นการดาวน์โหลดได้</span><span class="sxs-lookup"><span data-stu-id="cc1ff-117">The job can export the viewed report as a .pdf or a .pptx, and when it's complete, the user can receive the file as a download.</span></span> <span data-ttu-id="cc1ff-118">คุณสามารถใช้บุ๊กมาร์กส่งออกรายงานในสถานะที่ระบุ รวมถึงตัวกรองที่กำหนดค่า ตัวแบ่งส่วนข้อมูล และการตั้งค่าเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="cc1ff-118">Using bookmarks you can export the report in a specific state, including configured filters, slicers, and additional settings.</span></span> <span data-ttu-id="cc1ff-119">ในฐานะที่เป็น API แบบอะซิงโครนัส อาจใช้เวลาสักครู่ก่อนที่ไฟล์จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cc1ff-119">As the API is asynchronous, it may take some time for the file to be available.</span></span>

* <span data-ttu-id="cc1ff-120">**ไฟล์แนบอีเมล** - ส่งอีเมลโดยอัตโนมัติในช่วงเวลาที่ตั้งค่า ด้วยรายงาน .pdf ที่แนบมา</span><span class="sxs-lookup"><span data-stu-id="cc1ff-120">**Email attachment** - Send an automated email at set intervals, with an attached .pdf report.</span></span> <span data-ttu-id="cc1ff-121">สถานการณ์นี้อาจเป็นประโยชน์ถ้าคุณต้องการส่งรายงานรายสัปดาห์ไปยังฝ่ายบริหารโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cc1ff-121">This scenario can be useful if you want to automate sending a weekly report to executives.</span></span> <span data-ttu-id="cc1ff-122">สำหรับข้อมูลเพิ่มเติมให้ดูที่การ[ส่งออกและส่งอีเมลพร้อมรายงาน Power BI ด้วย Power Automate](../../collaborate-share/service-automate-power-bi-report-export.md)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-122">For more information see [Export and email a Power BI report with Power Automate](../../collaborate-share/service-automate-power-bi-report-export.md)</span></span>

## <a name="using-the-api"></a><span data-ttu-id="cc1ff-123">การใช้ API</span><span class="sxs-lookup"><span data-stu-id="cc1ff-123">Using the API</span></span>

<span data-ttu-id="cc1ff-124">ก่อนที่จะใช้ API ให้ยืนยันว่ามีการเปิดใช้งาน[การตั้งค่าผู้เช่าผู้ดูแลระบบ](../../admin/service-admin-portal.md#tenant-settings)ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cc1ff-124">Before using the API, verify that the following [admin tenant settings](../../admin/service-admin-portal.md#tenant-settings) are enabled:</span></span>
* <span data-ttu-id="cc1ff-125">**ส่งออกรายงานในรูปแบบงานนำเสนอ PowerPoint หรือเอกสาร PDF** - เปิดใช้งานโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="cc1ff-125">**Export reports as PowerPoint presentations or PDF documents** - Enabled by default.</span></span>
* <span data-ttu-id="cc1ff-126">**ส่งออกรายงานเป็นไฟล์รูปภาพ** - จำเป็นสำหรับ *.png* เท่านั้นและปิดใช้งานตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="cc1ff-126">**Export reports as image files** - Required only for *.png* and disabled by default.</span></span>

<span data-ttu-id="cc1ff-127">API เป็นแบบอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="cc1ff-127">The API is asynchronous.</span></span> <span data-ttu-id="cc1ff-128">เมื่อมีการเรียกใช้ API [exportToFile](/rest/api/power-bi/reports/exporttofile) จะทริกเกอร์งานการส่งออก</span><span class="sxs-lookup"><span data-stu-id="cc1ff-128">When the [exportToFile](/rest/api/power-bi/reports/exporttofile) API is called, it triggers an export job.</span></span> <span data-ttu-id="cc1ff-129">หลังจากทริกเกอร์งานส่งออก ให้ใช้[การโพลล์](/rest/api/power-bi/reports/getexporttofilestatus)เพื่อติดตามงานจนกว่าจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="cc1ff-129">After triggering an export job, use [polling](/rest/api/power-bi/reports/getexporttofilestatus) to track the job, until it's complete.</span></span>

<span data-ttu-id="cc1ff-130">ในระหว่างการโพลล์ API จะส่งกลับตัวเลขที่แสดงถึงจำนวนการทำงานที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="cc1ff-130">During polling, the API returns a number that represents the amount of work completed.</span></span> <span data-ttu-id="cc1ff-131">งานในแต่ละงานส่งออกจะถูกคำนวณตามจำนวนหน้าของรายงาน</span><span class="sxs-lookup"><span data-stu-id="cc1ff-131">The work in each export job is calculated based on the number of pages the report has.</span></span> <span data-ttu-id="cc1ff-132">จะมีหน้าทั้งหมดเท่าๆ กัน</span><span class="sxs-lookup"><span data-stu-id="cc1ff-132">All pages have the same weight.</span></span> <span data-ttu-id="cc1ff-133">ตัวอย่างเช่น ถ้าคุณกำลังส่งออกรายงานที่มี 10 หน้าและการโพลล์ส่งกลับ 70 หน้า นั่นหมายความว่า API ได้รับการประมวลผล 7 จาก 10 หน้าในงานส่งออก</span><span class="sxs-lookup"><span data-stu-id="cc1ff-133">If for example you're exporting a report with 10 pages, and the polling returns 70, it means that the API has processed seven out of the 10 pages in the export job.</span></span>

<span data-ttu-id="cc1ff-134">เมื่อการส่งออกเสร็จสิ้น การเรียกใช้ API การโพลล์จะส่งคืน [URL ของ Power BI](/rest/api/power-bi/reports/getfileofexporttofile) สำหรับรับไฟล์</span><span class="sxs-lookup"><span data-stu-id="cc1ff-134">When the export is complete, the polling API call returns a [Power BI URL](/rest/api/power-bi/reports/getfileofexporttofile) for getting the file.</span></span> <span data-ttu-id="cc1ff-135">URL จะพร้อมใช้งานเป็นเวลา 24 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="cc1ff-135">The URL will be available for 24 hours.</span></span>

## <a name="supported-features"></a><span data-ttu-id="cc1ff-136">ฟีเจอร์ที่ได้รับการรองรับ</span><span class="sxs-lookup"><span data-stu-id="cc1ff-136">Supported features</span></span>

### <a name="selecting-which-pages-to-print"></a><span data-ttu-id="cc1ff-137">การเลือกหน้าเพื่อพิมพ์</span><span class="sxs-lookup"><span data-stu-id="cc1ff-137">Selecting which pages to print</span></span>

<span data-ttu-id="cc1ff-138">ระบุหน้าที่คุณต้องการพิมพ์ตามค่าส่งคืนการ[รับหน้า](/rest/api/power-bi/reports/getpages)หรือ[รับหน้าในกลุ่ม](/rest/api/power-bi/reports/getpagesingroup)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-138">Specify the pages you want to print according to the [Get Pages](/rest/api/power-bi/reports/getpages) or [Get Pages in Group](/rest/api/power-bi/reports/getpagesingroup) return value.</span></span> <span data-ttu-id="cc1ff-139">คุณยังสามารถระบุลำดับของหน้าที่คุณกำลังส่งออกได้</span><span class="sxs-lookup"><span data-stu-id="cc1ff-139">You can also specify the order of the pages you're exporting.</span></span>

### <a name="bookmarks"></a><span data-ttu-id="cc1ff-140">บุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="cc1ff-140">Bookmarks</span></span>

<span data-ttu-id="cc1ff-141">[คุณสามารถใช้บุ๊กมาร์ก](../../consumer/end-user-bookmarks.md) เพื่อบันทึกรายงานในการกำหนดค่าเฉพาะรวมถึงตัวกรองที่นำไปใช้และสถานะของการแสดงผลด้วยภาพของรายงาน</span><span class="sxs-lookup"><span data-stu-id="cc1ff-141">[Bookmarks](../../consumer/end-user-bookmarks.md) can be used to save a report in a specific configuration, including applied filters and the state of the report's visuals.</span></span> <span data-ttu-id="cc1ff-142">คุณสามารถใช้ API [exportToFile](/rest/api/power-bi/reports/exporttofile) เพื่อส่งออกบุ๊กมาร์กของรายงานโดยทางโปรแกรมได้สองวิธี:</span><span class="sxs-lookup"><span data-stu-id="cc1ff-142">You can use the [exportToFile](/rest/api/power-bi/reports/exporttofile) API to programmatically export a report's bookmark, in two ways:</span></span>

* <span data-ttu-id="cc1ff-143">**ส่งออกบุ๊กมาร์กที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="cc1ff-143">**Export an existing bookmark**</span></span>

    <span data-ttu-id="cc1ff-144">หากต้องการส่งออกที่คั่นหน้ารายงาน [ที่มีอยู่](../../consumer/end-user-bookmarks.md#report-bookmarks)ให้ใช้คุณสมบัติ `name` ซึ่งเป็นตัวระบุที่ไม่ซ้ำกัน (ตรงตามตัวพิมพ์ใหญ่-เล็ก) ที่คุณสามารถรับได้โดยใช้ [ที่คั่นหน้าของ JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Bookmarks)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-144">To export an existing [report bookmark](../../consumer/end-user-bookmarks.md#report-bookmarks), use the `name` property, a unique (case sensitive) identifier which you can get using the [bookmarks JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Bookmarks).</span></span>

* <span data-ttu-id="cc1ff-145">**ส่งออกสถานะของรายงาน**</span><span class="sxs-lookup"><span data-stu-id="cc1ff-145">**Export the report's state**</span></span>

    <span data-ttu-id="cc1ff-146">เมื่อต้องการส่งออกสถานะปัจจุบันของรายงานให้ใช้คุณสมบัติ `state`</span><span class="sxs-lookup"><span data-stu-id="cc1ff-146">To export the current state of the report, use the `state` property.</span></span> <span data-ttu-id="cc1ff-147">ตัวอย่างเช่นคุณสามารถใช้วิธีการ `bookmarksManager.capture` ของบุ๊กมาร์กเพื่อจับภาพการเปลี่ยนแปลงของผู้ใช้ที่ระบุที่ทำกับรายงานจากนั้นส่งออกในสถานะปัจจุบันโดยใช้ `capturedBookmark.state`</span><span class="sxs-lookup"><span data-stu-id="cc1ff-147">For example, you can use the bookmark's `bookmarksManager.capture` method to capture the changes a specific user made to a report, and then export it in its current state using `capturedBookmark.state`.</span></span>

>[!NOTE]
><span data-ttu-id="cc1ff-148">ไม่รองรับ[บุ๊กมาร์กส่วนบุคคล](../../consumer/end-user-bookmarks.md#personal-bookmarks)และ[ตัวกรองแบบถาวร](https://powerbi.microsoft.com/blog/announcing-persistent-filters-in-the-service/)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-148">[Personal bookmarks](../../consumer/end-user-bookmarks.md#personal-bookmarks) and [persistent filters](https://powerbi.microsoft.com/blog/announcing-persistent-filters-in-the-service/) are not supported.</span></span>

### <a name="filters"></a><span data-ttu-id="cc1ff-149">ตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="cc1ff-149">Filters</span></span>

<span data-ttu-id="cc1ff-150">การใช้ `reportLevelFilters` ใน [PowerBIReportExportConfiguration](/rest/api/power-bi/reports/exporttofile#powerbireportexportconfiguration) คุณสามารถส่งออกรายงานในเงื่อนไขที่ถูกกรองได้</span><span class="sxs-lookup"><span data-stu-id="cc1ff-150">Using `reportLevelFilters` in [PowerBIReportExportConfiguration](/rest/api/power-bi/reports/exporttofile#powerbireportexportconfiguration), you can export a report in a filtered condition.</span></span>

<span data-ttu-id="cc1ff-151">เมื่อต้องการส่งออกรายงานที่ถูกกรอง ให้แทรก[พารามิเตอร์สตริงแบบสอบถาม URL](../../collaborate-share/service-url-filters.md) ที่คุณต้องการใช้เป็นตัวกรองของคุณ เพื่อ [ExportFilter](/rest/api/power-bi/reports/exporttofile#exportfilter)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-151">To export a filtered report, insert the [URL query string parameters](../../collaborate-share/service-url-filters.md) you want to use as your filter, to [ExportFilter](/rest/api/power-bi/reports/exporttofile#exportfilter).</span></span> <span data-ttu-id="cc1ff-152">เมื่อคุณใส่สตริงที่ คุณต้องนำส่วน `?filter=` ของพารามิเตอร์แบบสอบถาม URL ออก</span><span class="sxs-lookup"><span data-stu-id="cc1ff-152">When you enter the string, you must remove the `?filter=` part of the URL query parameter.</span></span>

<span data-ttu-id="cc1ff-153">ตารางด้านล่างนี้ประกอบด้วยตัวอย่างของสตริงข้อความที่คุณสามารถส่งผ่านไปยัง  `ExportFilter` ได้</span><span class="sxs-lookup"><span data-stu-id="cc1ff-153">The table below includes a few syntax examples of strings you can pass to  `ExportFilter`.</span></span>

|<span data-ttu-id="cc1ff-154">ตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="cc1ff-154">Filter</span></span>    |<span data-ttu-id="cc1ff-155">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="cc1ff-155">Syntax</span></span>    |<span data-ttu-id="cc1ff-156">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="cc1ff-156">Example</span></span>    |
|---|----|----|----|
|<span data-ttu-id="cc1ff-157">ค่าในเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cc1ff-157">A value in a field</span></span>    |<span data-ttu-id="cc1ff-158">ของตาราง/ฟิลด์ eq 'ค่า'</span><span class="sxs-lookup"><span data-stu-id="cc1ff-158">Table/Field eq 'value'</span></span>    |<span data-ttu-id="cc1ff-159">ร้านค้า/อาณาเขต eq 'NC'</span><span class="sxs-lookup"><span data-stu-id="cc1ff-159">Store/Territory eq 'NC'</span></span>    |
|<span data-ttu-id="cc1ff-160">หลายค่าในเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cc1ff-160">Multiple values in a field</span></span>    |<span data-ttu-id="cc1ff-161">ตาราง/เขตข้อมูลใน ('value1', 'value2')</span><span class="sxs-lookup"><span data-stu-id="cc1ff-161">Table/Field in ('value1', 'value2')</span></span>     |<span data-ttu-id="cc1ff-162">ร้านค้า/อาณาเขตใน ('NC', 'TN')</span><span class="sxs-lookup"><span data-stu-id="cc1ff-162">Store/Territory in ('NC', 'TN')</span></span>    |
|<span data-ttu-id="cc1ff-163">ค่าที่แตกต่างกันในเขตข้อมูลหนึ่งและค่าที่แตกต่างในเขตข้อมูลอื่น</span><span class="sxs-lookup"><span data-stu-id="cc1ff-163">A distinct value in one field, and a different distinct value in another field</span></span>    |<span data-ttu-id="cc1ff-164">ตาราง/Field1 eq 'value1' และตาราง/Field2 eq 'value2'</span><span class="sxs-lookup"><span data-stu-id="cc1ff-164">Table/Field1 eq 'value1' and Table/Field2 eq 'value2'</span></span>    |<span data-ttu-id="cc1ff-165">ร้านค้า/อาณาเขต eq 'NC' และร้านค้า/เครือข่าย eq 'Fashions Direct'</span><span class="sxs-lookup"><span data-stu-id="cc1ff-165">Store/Territory eq 'NC' and Store/Chain eq 'Fashions Direct'</span></span>    |

>[!NOTE]
><span data-ttu-id="cc1ff-166">`ReportLevelFilters` สามารถมีได้เฉพาะ [ExportFilter](/rest/api/power-bi/reports/exporttofile#exportfilter) เดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="cc1ff-166">`ReportLevelFilters` can only contain a single [ExportFilter](/rest/api/power-bi/reports/exporttofile#exportfilter).</span></span>

### <a name="authentication"></a><span data-ttu-id="cc1ff-167">การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="cc1ff-167">Authentication</span></span>

<span data-ttu-id="cc1ff-168">คุณสามารถรับรองความถูกต้องได้โดยใช้ผู้ใช้ (หรือผู้ใช้หลัก) หรือ [หลักบริการ](embed-service-principal.md)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-168">You can authenticate using a user (or master user) or a [service principal](embed-service-principal.md).</span></span>

### <a name="row-level-security-rls"></a><span data-ttu-id="cc1ff-169">การรักษาความปลอดภัยระดับแถว (RLS)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-169">Row Level Security (RLS)</span></span>

<span data-ttu-id="cc1ff-170">ด้วย[การรักษาความปลอดภัยระดับแถว (RLS)](embedded-row-level-security.md) คุณสามารถส่งออกรายงานที่แสดงข้อมูลที่สามารถมองเห็นได้เฉพาะผู้ใช้บางรายเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="cc1ff-170">With [Row Level Security (RLS)](embedded-row-level-security.md), you can export a report showing data that's only visible to certain users.</span></span> <span data-ttu-id="cc1ff-171">ตัวอย่างเช่น ถ้าคุณกำลังส่งออกรายงานยอดขายที่กำหนดไว้กับบทบาทภูมิภาค คุณสามารถกรองรายงานเพื่อให้แสดงเฉพาะภูมิภาคที่ระบุเท่านั้นได้</span><span class="sxs-lookup"><span data-stu-id="cc1ff-171">For example, if you're exporting a sales report that's defined with regional roles, you can programmatically filter the report so that only a certain region is displayed.</span></span>

<span data-ttu-id="cc1ff-172">หากต้องการส่งออกโดยใช้ RLS คุณต้องมีสิทธิ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cc1ff-172">To export using RLS, you must have the following permissions:</span></span>
* <span data-ttu-id="cc1ff-173">สิทธิ์การเขียนและแชร์ต่อสำหรับชุดข้อมูลที่มีการเชื่อมต่อกับรายงาน</span><span class="sxs-lookup"><span data-stu-id="cc1ff-173">Write and reshare permissions for the dataset the report is connected to</span></span>
* <span data-ttu-id="cc1ff-174">ถ้ารายงานอยู่ในพื้นที่ทำงาน v1 คุณจะต้องเป็นผู้ดูแลระบบพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="cc1ff-174">If the report resides on a v1 workspace, you need to be the workspace admin</span></span>
* <span data-ttu-id="cc1ff-175">ถ้ารายงานอยู่ในพื้นที่ทำงาน v2 คุณจะต้องเป็นผู้ดูแลระบบพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="cc1ff-175">If the report resides on a v2 workspace, you need to be a workspace member or admin</span></span>

### <a name="data-protection"></a><span data-ttu-id="cc1ff-176">การป้องกันข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cc1ff-176">Data protection</span></span>

<span data-ttu-id="cc1ff-177">รูปแบบ .pdf และ .pptx รองรับ[ป้ายชื่อระดับความลับ](../../admin/service-security-sensitivity-label-overview.md)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-177">The .pdf and .pptx formats support [sensitivity labels](../../admin/service-security-sensitivity-label-overview.md).</span></span> <span data-ttu-id="cc1ff-178">หากคุณส่งออกรายงานที่มีป้ายชื่อระดับความลับในรูปแบบ .pdf หรือ .pptx ไฟล์ที่ส่งออกจะแสดงรายงานที่มีป้ายชื่อระดับความลับ</span><span class="sxs-lookup"><span data-stu-id="cc1ff-178">If you export a report with a sensitivity label to a .pdf or a .pptx, the exported file will display the report with its sensitivity label.</span></span>

<span data-ttu-id="cc1ff-179">รายงานที่มีป้ายชื่อระดับความลับ จะไม่สามารถส่งออกในรูปแบบ .pdf หรือ .pptx โดยใช้ [หลักบริการ](embed-service-principal.md) ได้</span><span class="sxs-lookup"><span data-stu-id="cc1ff-179">A report with a sensitivity label cannot be exported to a .pdf or a .pptx using a [service principal](embed-service-principal.md).</span></span>

### <a name="localization"></a><span data-ttu-id="cc1ff-180">การแปลเป็นภาษาท้องถิ่น</span><span class="sxs-lookup"><span data-stu-id="cc1ff-180">Localization</span></span>

<span data-ttu-id="cc1ff-181">เมื่อใช้ `exportToFile` API คุณสามารถผ่านท้องถิ่นที่คุณต้องการได้</span><span class="sxs-lookup"><span data-stu-id="cc1ff-181">When using the `exportToFile` API, you can pass your desired local.</span></span> <span data-ttu-id="cc1ff-182">การตั้งค่าการแปลมีผลต่อวิธีการแสดงรายงาน ตัวอย่างเช่น โดยการเปลี่ยนการจัดรูปแบบโดยอ้างอิงจากเครื่องที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cc1ff-182">The localization settings affect the way the report is displayed, for example by changing formatting according to the selected local.</span></span>

## <a name="concurrent-requests"></a><span data-ttu-id="cc1ff-183">คำขอที่เกิดขึ้นพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="cc1ff-183">Concurrent requests</span></span>

<span data-ttu-id="cc1ff-184">`exportToFile` รองรับคำของานการส่งออกที่เกิดขึ้นพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="cc1ff-184">`exportToFile` supports concurrent export job requests.</span></span> <span data-ttu-id="cc1ff-185">ตารางด้านล่างแสดงจำนวนของงานที่คุณสามารถเรียกใช้ในเวลาเดียวกันได้โดยขึ้นอยู่กับ SKU รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="cc1ff-185">The table below shows the number of jobs you can run at the same time, depending on the SKU your report resides on.</span></span> <span data-ttu-id="cc1ff-186">คำขอที่เกิดขึ้นพร้อมกันจะอ้างอิงไปยังหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="cc1ff-186">Concurrent requests refer to report pages.</span></span> <span data-ttu-id="cc1ff-187">ตัวอย่างเช่น 20 หน้าในคำขอการส่งออกในหนึ่ง A6 SKU จะได้รับการประมวลผลพร้อมๆ กัน</span><span class="sxs-lookup"><span data-stu-id="cc1ff-187">For example, 20 pages in one export request on an A6 SKU, will be processed concurrently.</span></span> <span data-ttu-id="cc1ff-188">การดำเนินการนี้จะใช้เวลาพอๆ กันกับการส่งคำขอการส่งออก 20 ครั้งต่อหนึ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="cc1ff-188">This will take roughly the same time as sending 20 export requests with one page each.</span></span>

<span data-ttu-id="cc1ff-189">งานที่เกินจำนวนคำขอที่เกิดขึ้นพร้อมกันจะไม่ยุติลง</span><span class="sxs-lookup"><span data-stu-id="cc1ff-189">A job that exceeds its number of concurrent requests doesn't terminate.</span></span> <span data-ttu-id="cc1ff-190">ตัวอย่างเช่น ถ้าคุณส่งออกสามหน้าใน A1 SKU งานแรกจะเรียกใช้ และสองงานหลังจะต้องสองรอบการดำเนินการถัดไป</span><span class="sxs-lookup"><span data-stu-id="cc1ff-190">For example, if you export three pages in an A1 SKU, the first job will run, and the latter two will wait for the next two execution cycles.</span></span>

>[!NOTE]
><span data-ttu-id="cc1ff-191">การส่งออกรายงาน Power BI ไปยังไฟล์โดยใช้ API `exporToFile` ไม่รองรับสำหรับ [Premium Per User (PPU)](../../admin/service-premium-per-user-faq.md)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-191">Exporting a Power BI report to file using the `exporToFile` API, is not supported for [Premium Per User (PPU)](../../admin/service-premium-per-user-faq.md).</span></span> 

|<span data-ttu-id="cc1ff-192">Azure SKU</span><span class="sxs-lookup"><span data-stu-id="cc1ff-192">Azure SKU</span></span>  |<span data-ttu-id="cc1ff-193">Office SKU</span><span class="sxs-lookup"><span data-stu-id="cc1ff-193">Office SKU</span></span>  |<span data-ttu-id="cc1ff-194">หน้ารายงานที่เกิดขึ้นพร้อมกันสูงสุด</span><span class="sxs-lookup"><span data-stu-id="cc1ff-194">Maximum concurrent report pages</span></span>  |
|-----------|------------|-----------|
|<span data-ttu-id="cc1ff-195">A1</span><span class="sxs-lookup"><span data-stu-id="cc1ff-195">A1</span></span>         |<span data-ttu-id="cc1ff-196">EM1</span><span class="sxs-lookup"><span data-stu-id="cc1ff-196">EM1</span></span>         |<span data-ttu-id="cc1ff-197">1</span><span class="sxs-lookup"><span data-stu-id="cc1ff-197">1</span></span>          |
|<span data-ttu-id="cc1ff-198">A2</span><span class="sxs-lookup"><span data-stu-id="cc1ff-198">A2</span></span>         |<span data-ttu-id="cc1ff-199">EM2</span><span class="sxs-lookup"><span data-stu-id="cc1ff-199">EM2</span></span>         |<span data-ttu-id="cc1ff-200">2</span><span class="sxs-lookup"><span data-stu-id="cc1ff-200">2</span></span>          |
|<span data-ttu-id="cc1ff-201">A3</span><span class="sxs-lookup"><span data-stu-id="cc1ff-201">A3</span></span>         |<span data-ttu-id="cc1ff-202">EM3</span><span class="sxs-lookup"><span data-stu-id="cc1ff-202">EM3</span></span>         |<span data-ttu-id="cc1ff-203">3</span><span class="sxs-lookup"><span data-stu-id="cc1ff-203">3</span></span>          |
|<span data-ttu-id="cc1ff-204">A4</span><span class="sxs-lookup"><span data-stu-id="cc1ff-204">A4</span></span>         |<span data-ttu-id="cc1ff-205">P1</span><span class="sxs-lookup"><span data-stu-id="cc1ff-205">P1</span></span>          |<span data-ttu-id="cc1ff-206">6</span><span class="sxs-lookup"><span data-stu-id="cc1ff-206">6</span></span>          |
|<span data-ttu-id="cc1ff-207">A5</span><span class="sxs-lookup"><span data-stu-id="cc1ff-207">A5</span></span>         |<span data-ttu-id="cc1ff-208">P2</span><span class="sxs-lookup"><span data-stu-id="cc1ff-208">P2</span></span>          |<span data-ttu-id="cc1ff-209">12</span><span class="sxs-lookup"><span data-stu-id="cc1ff-209">12</span></span>         |
|<span data-ttu-id="cc1ff-210">A6</span><span class="sxs-lookup"><span data-stu-id="cc1ff-210">A6</span></span>         |<span data-ttu-id="cc1ff-211">P3</span><span class="sxs-lookup"><span data-stu-id="cc1ff-211">P3</span></span>          |<span data-ttu-id="cc1ff-212">24</span><span class="sxs-lookup"><span data-stu-id="cc1ff-212">24</span></span>         |

## <a name="limitations"></a><span data-ttu-id="cc1ff-213">ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="cc1ff-213">Limitations</span></span>

* <span data-ttu-id="cc1ff-214">รายงานที่คุณกำลังส่งออกต้องอยู่บนความจุพรีเมียมหรือแบบฝัง</span><span class="sxs-lookup"><span data-stu-id="cc1ff-214">The report you're exporting must reside on a Premium or Embedded capacity.</span></span>
* <span data-ttu-id="cc1ff-215">ชุดข้อมูลที่คุณกำลังส่งออกต้องอยู่บนความจุ</span><span class="sxs-lookup"><span data-stu-id="cc1ff-215">The dataset of the report you're exporting must reside on a Premium or Embedded capacity.</span></span>
* <span data-ttu-id="cc1ff-216">สำหรับการแสดงตัวอย่างสาธารณะ จำนวนหน้ารายงาน Power BI ที่ส่งออกต่อชั่วโมงจะถูกจำกัดไว้ที่ 50 หน้าต่อความจุ</span><span class="sxs-lookup"><span data-stu-id="cc1ff-216">For public preview, the number of Power BI report pages exported per hour is limited to 50 per capacity.</span></span>
* <span data-ttu-id="cc1ff-217">รายงานที่ส่งออกต้องมีขนาดไฟล์ไม่เกิน 250 MB</span><span class="sxs-lookup"><span data-stu-id="cc1ff-217">Exported reports cannot exceed a file size of 250 MB.</span></span>
* <span data-ttu-id="cc1ff-218">เมื่อส่งออกในรูปแบบ .png ป้ายชื่อความระดับความลับจะไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="cc1ff-218">When exporting to .png, sensitivity labels are not supported.</span></span>
* <span data-ttu-id="cc1ff-219">จำนวนหน้าซึ่งสามารถรวมอยู่ในรายงานที่ส่งออกได้คือ 50</span><span class="sxs-lookup"><span data-stu-id="cc1ff-219">The number of pages that can be included in an exported report is 50.</span></span> <span data-ttu-id="cc1ff-220">หากรายงานมีหลายหน้า API จะส่งคืนข้อผิดพลาดและงานส่งออกจะถูกยกเลิก</span><span class="sxs-lookup"><span data-stu-id="cc1ff-220">If the report includes more pages, the API returns an error and the export job is canceled.</span></span>
* <span data-ttu-id="cc1ff-221">ไม่รองรับ[บุ๊กมาร์กส่วนบุคคล](../../consumer/end-user-bookmarks.md#personal-bookmarks)และ[ตัวกรองแบบถาวร](https://powerbi.microsoft.com/blog/announcing-persistent-filters-in-the-service/)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-221">[Personal bookmarks](../../consumer/end-user-bookmarks.md#personal-bookmarks) and [persistent filters](https://powerbi.microsoft.com/blog/announcing-persistent-filters-in-the-service/) are not supported.</span></span>
* <span data-ttu-id="cc1ff-222">การแสดงผลด้วยภาพของ Power BI ที่แสดงในรายการด้านล่างไม่ได้รับการรองรับ</span><span class="sxs-lookup"><span data-stu-id="cc1ff-222">The Power BI visuals listed below are not supported.</span></span> <span data-ttu-id="cc1ff-223">เมื่อรายงานที่มีการแสดงผลด้วยภาพเหล่านี้ถูกส่งออก ส่วนของรายงานที่ประกอบด้วยการแสดงผลด้วยภาพดังกล่าวจะไม่แสดง และจะแสดงสัญลักษณ์ข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="cc1ff-223">When a report containing these visuals is exported, the parts of the report that contain these visuals will not render, and will display an error symbol.</span></span>
    * <span data-ttu-id="cc1ff-224">การแสดงผลด้วยภาพของ Power BI ที่ไม่ผ่านการจัดการ</span><span class="sxs-lookup"><span data-stu-id="cc1ff-224">Uncertified Power BI visuals</span></span>
    * <span data-ttu-id="cc1ff-225">วิชวล R</span><span class="sxs-lookup"><span data-stu-id="cc1ff-225">R visuals</span></span>
    * <span data-ttu-id="cc1ff-226">PowerApps</span><span class="sxs-lookup"><span data-stu-id="cc1ff-226">PowerApps</span></span>
    * <span data-ttu-id="cc1ff-227">การแสดงผลด้วยภาพของ Python</span><span class="sxs-lookup"><span data-stu-id="cc1ff-227">Python visuals</span></span>
    * <span data-ttu-id="cc1ff-228">Visio</span><span class="sxs-lookup"><span data-stu-id="cc1ff-228">Visio</span></span>

## <a name="code-examples"></a><span data-ttu-id="cc1ff-229">ตัวอย่างรหัส</span><span class="sxs-lookup"><span data-stu-id="cc1ff-229">Code examples</span></span>

<span data-ttu-id="cc1ff-230">เมื่อคุณสร้างงานส่งออก มีสามขั้นตอนเพื่อการปฏิบัติตามดังนี้:</span><span class="sxs-lookup"><span data-stu-id="cc1ff-230">When you create an export job, there are three steps to follow:</span></span>

1. <span data-ttu-id="cc1ff-231">[การส่งคำขอการส่งออก](#step-1---sending-an-export-request)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-231">[Sending an export request](#step-1---sending-an-export-request).</span></span>
2. <span data-ttu-id="cc1ff-232">[การโพลล์](#step-2---polling)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-232">[Polling](#step-2---polling).</span></span>
3. <span data-ttu-id="cc1ff-233">[การรับไฟล์](#step-3---getting-the-file)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-233">[Getting the file](#step-3---getting-the-file).</span></span>
4. <span data-ttu-id="cc1ff-234">[การใช้สตรีมไฟล์](#step-4---using-the-file-stream)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-234">[Using the file stream](#step-4---using-the-file-stream).</span></span>

<span data-ttu-id="cc1ff-235">หัวข้อนี้มีตัวอย่างสำหรับแต่ละขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="cc1ff-235">This section provides examples for each step.</span></span>

### <a name="step-1---sending-an-export-request"></a><span data-ttu-id="cc1ff-236">ขั้นตอนที่ 1 - ส่งคำขอส่งออก</span><span class="sxs-lookup"><span data-stu-id="cc1ff-236">Step 1 - sending an export request</span></span>

<span data-ttu-id="cc1ff-237">ขั้นตอนแรกคือการส่งคำขอส่งออก</span><span class="sxs-lookup"><span data-stu-id="cc1ff-237">The first step is sending an export request.</span></span> <span data-ttu-id="cc1ff-238">ในตัวอย่างนี้ คำขอส่งออกจะถูกส่งไปยังหน้าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="cc1ff-238">In this example, an export request is sent for a specific page.</span></span>

```csharp
private async Task<string> PostExportRequest(
    Guid reportId,
    Guid groupId,
    FileFormat format,
    IList<string> pageNames = null, /* Get the page names from the GetPages REST API */
    string urlFilter = null)
{
    var powerBIReportExportConfiguration = new PowerBIReportExportConfiguration
    {
        Settings = new ExportReportSettings
        {
            Locale = "en-us",
        },
        // Note that page names differ from the page display names
        // To get the page names use the GetPages REST API
        Pages = pageNames?.Select(pn => new ExportReportPage(Name = pn)).ToList(),
        // ReportLevelFilters collection needs to be instantiated explicitly
        ReportLevelFilters = !string.IsNullOrEmpty(urlFilter) ? new List<ExportFilter>() { new ExportFilter(urlFilter) } : null,

    };

    var exportRequest = new ExportReportRequest
    {
        Format = format,
        PowerBIReportConfiguration = powerBIReportExportConfiguration,
    };

    // The 'Client' object is an instance of the Power BI .NET SDK
    var export = await Client.Reports.ExportToFileInGroupAsync(groupId, reportId, exportRequest);

    // Save the export ID, you'll need it for polling and getting the exported file
    return export.Id;
}
```

### <a name="step-2---polling"></a><span data-ttu-id="cc1ff-239">ขั้นตอนที่ 2 - การโพลล์</span><span class="sxs-lookup"><span data-stu-id="cc1ff-239">Step 2 - polling</span></span>

<span data-ttu-id="cc1ff-240">หลังจากที่คุณส่งคำขอส่งออก ให้ใช้การโพลล์เพื่อระบุว่าไฟล์ส่งออกที่คุณรออยู่พร้อมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="cc1ff-240">After you've sent an export request, use polling to identify when the export file you're waiting for is ready.</span></span>

```csharp
private async Task<HttpOperationResponse<Export>> PollExportRequest(
    Guid reportId,
    Guid groupId,
    string exportId /* Get from the PostExportRequest response */,
    int timeOutInMinutes,
    CancellationToken token)
{
    HttpOperationResponse<Export> httpMessage = null;
    Export exportStatus = null;
    DateTime startTime = DateTime.UtcNow;
    const int c_secToMillisec = 1000;
    do
    {
        if (DateTime.UtcNow.Subtract(startTime).TotalMinutes > timeOutInMinutes || token.IsCancellationRequested)
        {
            // Error handling for timeout and cancellations 
            return null;
        }

        // The 'Client' object is an instance of the Power BI .NET SDK
        httpMessage = await Client.Reports.GetExportToFileStatusInGroupWithHttpMessagesAsync(groupId, reportId, exportId);
        exportStatus = httpMessage.Body;

        // You can track the export progress using the PercentComplete that's part of the response
        SomeTextBox.Text = string.Format("{0} (Percent Complete : {1}%)", exportStatus.Status.ToString(), exportStatus.PercentComplete);
        if (exportStatus.Status == ExportState.Running || exportStatus.Status == ExportState.NotStarted)
        {
            // The recommended waiting time between polling requests can be found in the RetryAfter header
            // Note that this header is not always populated
            var retryAfter = httpMessage.Response.Headers.RetryAfter;
            var retryAfterInSec = retryAfter.Delta.Value.Seconds;
            await Task.Delay(retryAfterInSec * c_secToMillisec);
        }
    }
    // While not in a terminal state, keep polling
    while (exportStatus.Status != ExportState.Succeeded && exportStatus.Status != ExportState.Failed);

    return httpMessage;
}
```

### <a name="step-3---getting-the-file"></a><span data-ttu-id="cc1ff-241">ขั้นตอนที่ 3 - การรับไฟล์</span><span class="sxs-lookup"><span data-stu-id="cc1ff-241">Step 3 - getting the file</span></span>

<span data-ttu-id="cc1ff-242">เมื่อการโพลล์ส่งคืน URL ให้ใช้ตัวอย่างนี้เพื่อรับไฟล์ที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="cc1ff-242">Once polling returns a URL, use this example to get the received file.</span></span>

```csharp
private async Task<ExportedFile> GetExportedFile(
    Guid reportId,
    Guid groupId,
    Export export /* Get from the PollExportRequest response */)
{
    if (export.Status == ExportState.Succeeded)
    {
        // The 'Client' object is an instance of the Power BI .NET SDK
        var fileStream = await Client.Reports.GetFileOfExportToFileAsync(groupId, reportId, export.Id);
        return new ExportedFile
        {
            FileStream = fileStream,
            FileSuffix = export.ResourceFileExtension,
        };
    }
    return null;
}

public class ExportedFile
{
    public Stream FileStream;
    public string FileSuffix;
}
```

### <a name="step-4---using-the-file-stream"></a><span data-ttu-id="cc1ff-243">ขั้นตอนที่ 4 - การใช้สตรีมไฟล์</span><span class="sxs-lookup"><span data-stu-id="cc1ff-243">Step 4 - Using the file stream</span></span>

<span data-ttu-id="cc1ff-244">เมื่อคุณมีสตรีมไฟล์ คุณสามารถจัดการได้ในแบบที่เหมาะกับความต้องการของคุณมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="cc1ff-244">When you have the file stream, you can handle it in the way that best fits your needs.</span></span> <span data-ttu-id="cc1ff-245">ตัวอย่างเช่น คุณสามารถส่งอีเมลหรือใช้เพื่อดาวน์โหลดรายงานที่ส่งออก</span><span class="sxs-lookup"><span data-stu-id="cc1ff-245">For example, you can email it or use it to download the exported reports.</span></span>

### <a name="end-to-end-example"></a><span data-ttu-id="cc1ff-246">ตัวอย่างแบบต้นจนจบ</span><span class="sxs-lookup"><span data-stu-id="cc1ff-246">End-to-end example</span></span>

<span data-ttu-id="cc1ff-247">นี่คือตัวอย่างแบบต้นจนจบสำหรับการส่งออกรายงาน</span><span class="sxs-lookup"><span data-stu-id="cc1ff-247">This is an end-to-end example for exporting a report.</span></span> <span data-ttu-id="cc1ff-248">ตัวอย่างนี้รวมไปถึงขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cc1ff-248">This example includes the following stages:</span></span>
1. <span data-ttu-id="cc1ff-249">[ส่งคำขอการส่งออก](#step-1---sending-an-export-request)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-249">[Sending the export request](#step-1---sending-an-export-request).</span></span>
2. <span data-ttu-id="cc1ff-250">[การโพลล์](#step-2---polling)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-250">[Polling](#step-2---polling).</span></span>
3. <span data-ttu-id="cc1ff-251">[การรับไฟล์](#step-3---getting-the-file)</span><span class="sxs-lookup"><span data-stu-id="cc1ff-251">[Getting the file](#step-3---getting-the-file).</span></span>

```csharp
private async Task<ExportedFile> ExportPowerBIReport(
    Guid reportId,
    Guid groupId,
    FileFormat format,
    int pollingtimeOutInMinutes,
    CancellationToken token,
    IList<string> pageNames = null,  /* Get the page names from the GetPages REST API */
    string urlFilter = null)
{
    const int c_maxNumberOfRetries = 3; /* Can be set to any desired number */
    const int c_secToMillisec = 1000;
    try
    {
        Export export = null;
        int retryAttempt = 1;
        do
        {
            var exportId = await PostExportRequest(reportId, groupId, format, pageNames, urlFilter);
            var httpMessage = await PollExportRequest(reportId, groupId, exportId, pollingtimeOutInMinutes, token);
            export = httpMessage.Body;
            if (export == null)
            {
                // Error, failure in exporting the report
                return null;
            }
            if (export.Status == ExportState.Failed)
            {
                // Some failure cases indicate that the system is currently busy. The entire export operation can be retried after a certain delay
                // In such cases the recommended waiting time before retrying the entire export operation can be found in the RetryAfter header
                var retryAfter = httpMessage.Response.Headers.RetryAfter;
                if(retryAfter == null)
                {
                    // Failed state with no RetryAfter header indicates that the export failed permanently
                    return null;
                }

                var retryAfterInSec = retryAfter.Delta.Value.Seconds;
                await Task.Delay(retryAfterInSec * c_secToMillisec);
            }
        }
        while (export.Status != ExportState.Succeeded && retryAttempt++ < c_maxNumberOfRetries);

        if (export.Status != ExportState.Succeeded)
        {
            // Error, failure in exporting the report
            return null;
        }

        var exportedFile = await GetExportedFile(reportId, groupId, export);

        // Now you have the exported file stream ready to be used according to your specific needs
        // For example, saving the file can be done as follows:
        /*
            var pathOnDisk = @"C:\temp\" + export.ReportName + exportedFile.FileSuffix;

            using (var fileStream = File.Create(pathOnDisk))
            {
                exportedFile.FileStream.CopyTo(fileStream);
            }
        */

        return exportedFile;
    }
    catch
    {
        // Error handling
        throw;
    }
}
```

## <a name="next-steps"></a><span data-ttu-id="cc1ff-252">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="cc1ff-252">Next steps</span></span>

<span data-ttu-id="cc1ff-253">ตรวจทานวิธีการฝังเนื้อหาสำหรับลูกค้าและองค์กรของคุณ:</span><span class="sxs-lookup"><span data-stu-id="cc1ff-253">Review how to embed content for your customers and your organization:</span></span>

> [!div class="nextstepaction"]
>[<span data-ttu-id="cc1ff-254">ส่งออกรายงานที่มีการแบ่งหน้าไปยังไฟล์</span><span class="sxs-lookup"><span data-stu-id="cc1ff-254">Export paginated report to file</span></span>](export-paginated-report.md)

> [!div class="nextstepaction"]
>[<span data-ttu-id="cc1ff-255">ฝังสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="cc1ff-255">Embed for your customers</span></span>](embed-sample-for-customers.md)

> [!div class="nextstepaction"]
>[<span data-ttu-id="cc1ff-256">ฝังตัวสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="cc1ff-256">Embed for your organization</span></span>](embed-sample-for-your-organization.md)

> [!div class="nextstepaction"]
>[<span data-ttu-id="cc1ff-257">ส่งออกและส่งอีเมลรายงาน Power BI ด้วย Power Automate</span><span class="sxs-lookup"><span data-stu-id="cc1ff-257">Export and email a Power BI report with Power Automate</span></span>](../../collaborate-share/service-automate-power-bi-report-export.md)
