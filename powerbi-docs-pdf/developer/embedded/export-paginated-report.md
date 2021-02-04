---
title: ส่งออก API รายงานที่มีการแบ่งหน้าของการวิเคราะห์แบบฝังตัวของ Power BI สำหรับข้อมูลเชิงลึก BI ที่ฝังตัวได้ดีขึ้น
description: เรียนรู้วิธีการส่งออกรายงานที่มีการแบ่งหน้า Power BI แบบฝังตัว เปิดใช้งานข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.topic: how-to
ms.service: powerbi
ms.subservice: powerbi-developer
ms.date: 04/05/2020
ms.openlocfilehash: 42f110356c891235d17810dbb1f220f0a006c066
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887097"
---
# <a name="export-paginated-report-to-file-preview"></a><span data-ttu-id="db174-104">ส่งออกรายงานที่มีการแบ่งหน้าไปยังไฟล์ (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="db174-104">Export paginated report to file (preview)</span></span>

<span data-ttu-id="db174-105">`exportToFile` API เปิดใช้งานการส่งออกรายงาน Power BI ที่มีการแบ่งหน้าโดยใช้การเรียกใช้ REST</span><span class="sxs-lookup"><span data-stu-id="db174-105">The `exportToFile` API enables exporting a Power BI paginated report by using a REST call.</span></span> <span data-ttu-id="db174-106">รูปแบบไฟล์ต่อไปนี้ได้รับการรองรับ:</span><span class="sxs-lookup"><span data-stu-id="db174-106">The following file formats are supported:</span></span>
* <span data-ttu-id="db174-107">**.pptx** (PowerPoint)</span><span class="sxs-lookup"><span data-stu-id="db174-107">**.pptx** (PowerPoint)</span></span>
* <span data-ttu-id="db174-108">**.pdf**</span><span class="sxs-lookup"><span data-stu-id="db174-108">**.pdf**</span></span>
* <span data-ttu-id="db174-109">**.xlsx** (Excel)</span><span class="sxs-lookup"><span data-stu-id="db174-109">**.xlsx** (Excel)</span></span>
* <span data-ttu-id="db174-110">**.dox** (Word)</span><span class="sxs-lookup"><span data-stu-id="db174-110">**.dox** (Word)</span></span>
* <span data-ttu-id="db174-111">**.csv**</span><span class="sxs-lookup"><span data-stu-id="db174-111">**.csv**</span></span>
* <span data-ttu-id="db174-112">**.xml**</span><span class="sxs-lookup"><span data-stu-id="db174-112">**.xml**</span></span>
* <span data-ttu-id="db174-113">**.mhtml**</span><span class="sxs-lookup"><span data-stu-id="db174-113">**.mhtml**</span></span>
* <span data-ttu-id="db174-114">**รูปภาพ**</span><span class="sxs-lookup"><span data-stu-id="db174-114">**Image**</span></span>
    * <span data-ttu-id="db174-115">เมื่อส่งออกไปยังรูปภาพ ให้ตั้งค่ารูปแบบรูปภาพผ่าน `OutputFormat` การตั้งค่ารูปแบบ</span><span class="sxs-lookup"><span data-stu-id="db174-115">When exporting to an image, set the image format via the `OutputFormat` format setting</span></span>
    * <span data-ttu-id="db174-116">ค่า OutputFormat ที่ได้รับการสนับสนุนคือ: .bmp, .emf, .gif, .jpeg, .png หรือ .tiff (ค่าเริ่มต้น)</span><span class="sxs-lookup"><span data-stu-id="db174-116">The supported OutputFormat values are: .bmp, .emf, .gif, .jpeg, .png, or .tiff (default)</span></span>

## <a name="usage-examples"></a><span data-ttu-id="db174-117">ตัวอย่างการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="db174-117">Usage examples</span></span>

<span data-ttu-id="db174-118">คุณสามารถใช้ฟีเจอร์การส่งออกได้หลายวิธี</span><span class="sxs-lookup"><span data-stu-id="db174-118">You can use the export feature in a variety of ways.</span></span> <span data-ttu-id="db174-119">นี่เป็นตัวอย่างสองตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="db174-119">Here are a couple of examples:</span></span>

* <span data-ttu-id="db174-120">**ส่งไปยังปุ่มพิมพ์** - ในแอปพลิเคชันของคุณ ให้สร้างปุ่มที่เมื่อคลิกที่จะทริกเกอร์งานการส่งออก</span><span class="sxs-lookup"><span data-stu-id="db174-120">**Send to print button** - In your application, create a button that when clicked on triggers an export job.</span></span> <span data-ttu-id="db174-121">งานสามารถส่งออกรายงานที่เป็น .pdf หรือ .pptx และเมื่อเสร็จสมบูรณ์ ผู้ใช้จะสามารถรับไฟล์เป็นการดาวน์โหลดได้</span><span class="sxs-lookup"><span data-stu-id="db174-121">The job can export the viewed report as a .pdf or a .pptx, and when it's complete, the user can receive the file as a download.</span></span> <span data-ttu-id="db174-122">การใช้พารามิเตอร์รายงานและการตั้งค่ารูปแบบจะทำให้คุณสามารถส่งออกรายงานในสถานะที่ระบุ รวมถึงข้อมูลที่กรอง ขนาดหน้าแบบกำหนดเอง และการตั้งค่าเฉพาะรูปแบบอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="db174-122">Using report parameters and format settings you can export the report in a specific state, including filtered data, custom page sizes and other format specific settings.</span></span> <span data-ttu-id="db174-123">ในฐานะที่เป็น API แบบอะซิงโครนัส อาจใช้เวลาสักครู่ก่อนที่ไฟล์จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="db174-123">As the API is asynchronous, it may take some time for the file to be available.</span></span>

* <span data-ttu-id="db174-124">**ไฟล์แนบอีเมล** - ส่งอีเมลโดยอัตโนมัติในช่วงเวลาที่ตั้งค่า ด้วยรายงาน .pdf ที่แนบมา</span><span class="sxs-lookup"><span data-stu-id="db174-124">**Email attachment** - Send an automated email at set intervals, with an attached .pdf report.</span></span> <span data-ttu-id="db174-125">สถานการณ์นี้อาจเป็นประโยชน์ถ้าคุณต้องการส่งรายงานรายสัปดาห์ไปยังฝ่ายบริหารโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="db174-125">This scenario can be useful if you want to automate sending a weekly report to executives.</span></span>

## <a name="using-the-api"></a><span data-ttu-id="db174-126">การใช้ API</span><span class="sxs-lookup"><span data-stu-id="db174-126">Using the API</span></span>

<span data-ttu-id="db174-127">API เป็นแบบอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="db174-127">The API is asynchronous.</span></span> <span data-ttu-id="db174-128">เมื่อมีการเรียกใช้ API [exportToFile](/rest/api/power-bi/reports/exporttofile) จะทริกเกอร์งานการส่งออก</span><span class="sxs-lookup"><span data-stu-id="db174-128">When the [exportToFile](/rest/api/power-bi/reports/exporttofile) API is called, it triggers an export job.</span></span> <span data-ttu-id="db174-129">หลังจากทริกเกอร์งานส่งออก ให้ใช้[การโพลล์](/rest/api/power-bi/reports/getexporttofilestatus)เพื่อติดตามงานจนกว่าจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="db174-129">After triggering an export job, use [polling](/rest/api/power-bi/reports/getexporttofilestatus) to track the job, until it's complete.</span></span>

<span data-ttu-id="db174-130">เมื่อการส่งออกเสร็จสิ้น การเรียกใช้ API การโพลล์จะส่งคืน [URL ของ Power BI](/rest/api/power-bi/reports/getfileofexporttofile) สำหรับรับไฟล์</span><span class="sxs-lookup"><span data-stu-id="db174-130">When the export is complete, the polling API call returns a [Power BI URL](/rest/api/power-bi/reports/getfileofexporttofile) for getting the file.</span></span> <span data-ttu-id="db174-131">URL จะพร้อมใช้งานเป็นเวลา 24 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="db174-131">The URL will be available for 24 hours.</span></span>

## <a name="supported-features"></a><span data-ttu-id="db174-132">ฟีเจอร์ที่ได้รับการรองรับ</span><span class="sxs-lookup"><span data-stu-id="db174-132">Supported features</span></span>

### <a name="format-settings"></a><span data-ttu-id="db174-133">การตั้งค่ารูปแบบ</span><span class="sxs-lookup"><span data-stu-id="db174-133">Format settings</span></span>

<span data-ttu-id="db174-134">ระบุการตั้งค่ารูปแบบที่หลากหลายสำหรับแต่ละรูปแบบไฟล์</span><span class="sxs-lookup"><span data-stu-id="db174-134">Specify a variety of format settings for each file format.</span></span> <span data-ttu-id="db174-135">คุณสมบัติและค่าที่ได้รับการสนับสนุนจะเทียบเท่ากับ [พารามิเตอร์ข้อมูลอุปกรณ์](../../paginated-reports/report-builder-url-parameters.md#report-commands-rdl) สำหรับพารามิเตอร์ URL ของรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="db174-135">The supported properties and values are equivalent to [Device Info parameters](../../paginated-reports/report-builder-url-parameters.md#report-commands-rdl) for paginated report URL parameters.</span></span>

<span data-ttu-id="db174-136">ต่อไปนี้ป็นตัวอย่างสองรายการ รายการแรกคือการส่งออกสี่หน้าแรกของรายงานโดยใช้ขนาดหน้ารายงาน ในรูปแบบไฟล์ .pptx และอีกรายการหนึ่งคือ การส่งออกหน้าที่สามของรายงาน ในรูปแบบไฟล์ .jpeg</span><span class="sxs-lookup"><span data-stu-id="db174-136">Here are two examples, one for exporting the first four pages of a report using the report page size to a .pptx file, and another for exporting the third page of a report to a .jpeg file.</span></span>

<span data-ttu-id="db174-137">**การส่งออกสี่หน้าแรกในรูปแบบ .pptx**</span><span class="sxs-lookup"><span data-stu-id="db174-137">**Exporting the first four pages to a .pptx**</span></span>

```json
{
      "format": "PPTX",
      "paginatedReportConfiguration":{
            "formatSettings":{
                  "UseReportPageSize": "true",
                  "StartPage": "1",
                  "EndPage": "4"
            }
      }
}
```

<span data-ttu-id="db174-138">**การส่งออกหน้าที่สามในรูปแบบ .jpeg**</span><span class="sxs-lookup"><span data-stu-id="db174-138">**Exporting the third page to a .jpeg**</span></span>

```json
{
      "format": "IMAGE",
      "paginatedReportConfiguration":{
            "formatSettings":{
                  "OutputFormat": "JPEG",
                  "StartPage": "3",
                  "EndPage": "3"
            }
      }
}
```

### <a name="report-parameters"></a><span data-ttu-id="db174-139">รายงานพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="db174-139">Report parameters</span></span>

<span data-ttu-id="db174-140">คุณสามารถใช้ `exportToFile` API เพื่อส่งออกรายงานด้วยชุดพารามิเตอร์ของรายงานโดยทางโปรแกรม</span><span class="sxs-lookup"><span data-stu-id="db174-140">You can use the `exportToFile` API to programmatically export a report with a set of report parameters.</span></span> <span data-ttu-id="db174-141">การดำเนินการนี้จะทำได้โดยใช้ความสามารถของ [พารามิเตอร์รายงาน](../../paginated-reports/paginated-reports-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="db174-141">This is done using [report parameter](../../paginated-reports/paginated-reports-parameters.md) capabilities.</span></span>

<span data-ttu-id="db174-142">ต่อไปนี้คือตัวอย่างสำหรับการตั้งค่าของพารามิเตอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="db174-142">Here is an example for setting report parameter values.</span></span>

```json
{
      "format": "PDF",
      "paginatedReportConfiguration":{
            "parameterValues":[
                  {"name": "State", "value": "WA"},
                  {"name": "City", "value": "Seattle"},
                  {"name": "City", "value": "Bellevue"},
                  {"name": "City", "value": "Redmond"}
            ]
      }
}
```

### <a name="authentication"></a><span data-ttu-id="db174-143">การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="db174-143">Authentication</span></span>

<span data-ttu-id="db174-144">คุณสามารถรับรองความถูกต้องได้โดยใช้ผู้ใช้ (หรือผู้ใช้หลัก) หรือ [หลักบริการ](embed-service-principal.md)</span><span class="sxs-lookup"><span data-stu-id="db174-144">You can authenticate using a user (or master user) or a [service principal](embed-service-principal.md).</span></span>

### <a name="row-level-security-rls"></a><span data-ttu-id="db174-145">การรักษาความปลอดภัยระดับแถว (RLS)</span><span class="sxs-lookup"><span data-stu-id="db174-145">Row Level Security (RLS)</span></span>

<span data-ttu-id="db174-146">ขณะที่ใช้ชุดข้อมูล Power BI ที่มีความปลอดภัยระดับแถว (RLS) ซึ่งกำหนดให้เป็นแหล่งข้อมูล คุณจะสามารถส่งออกรายงานที่แสดงข้อมูลที่จะมีผู้ใช้บางรายเท่านั้นที่เห็น</span><span class="sxs-lookup"><span data-stu-id="db174-146">When using a Power BI dataset that has Row Level Security (RLS) defined as a data source, you can export a report showing data that's only visible to certain users.</span></span> <span data-ttu-id="db174-147">ตัวอย่างเช่น ถ้าคุณกำลังส่งออกรายงานยอดขายที่กำหนดไว้กับบทบาทภูมิภาค คุณสามารถกรองรายงานเพื่อให้แสดงเฉพาะภูมิภาคที่ระบุเท่านั้นได้</span><span class="sxs-lookup"><span data-stu-id="db174-147">For example, if you're exporting a sales report that's defined with regional roles, you can programmatically filter the report so that only a certain region is displayed.</span></span>

<span data-ttu-id="db174-148">เมื่อต้องการส่งออกโดยใช้ RLS คุณจำเป็นต้องมีสิทธิ์การอ่านสำหรับชุดข้อมูล Power BI ที่รายงานกำลังใช้เป็นแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="db174-148">To export using RLS, you must have read permission for the Power BI dataset the report is using as a data source.</span></span>

<span data-ttu-id="db174-149">ต่อไปนี้คือตัวอย่างสำหรับการใช้ชื่อผู้ใช้ที่มีประสิทธิภาพสำหรับ RLS</span><span class="sxs-lookup"><span data-stu-id="db174-149">Here is an example for supplying an effective user name for RLS.</span></span>

```json
{
      "format": "PDF",
      "paginatedReportConfiguration":{
            "identities": [
                  {"username": "john@contoso.com"}
            ]
      }
}
```
## <a name="ppu-concurrent-requests"></a><span data-ttu-id="db174-150">คำขอที่เกิดขึ้นพร้อมกันสำหรับ PPU</span><span class="sxs-lookup"><span data-stu-id="db174-150">PPU concurrent requests</span></span>
<span data-ttu-id="db174-151">API `exportToFile` อนุญาตให้มีหนึ่งคำขอในช่วงเวลาห้านาทีเมื่อใช้ [Premium Per User (PPU)](../../admin/service-premium-per-user-faq.md)</span><span class="sxs-lookup"><span data-stu-id="db174-151">The `exportToFile` API allows one request in a five minute window when using [Premium Per User (PPU)](../../admin/service-premium-per-user-faq.md).</span></span> <span data-ttu-id="db174-152">คำขอหลายรายการ (มากกว่าหนึ่งรายการ) ภายในช่วงเวลาห้านาทีจะทำให้เกิดข้อผิดพลาด (429) *คำขอมากเกินไป*</span><span class="sxs-lookup"><span data-stu-id="db174-152">Multiple (greater than one) requests within a five minute window will result in a *Too Many Requests* (429) error.</span></span>

## <a name="code-examples"></a><span data-ttu-id="db174-153">ตัวอย่างรหัส</span><span class="sxs-lookup"><span data-stu-id="db174-153">Code examples</span></span>

<span data-ttu-id="db174-154">Power BI API SDK ที่ใช้ในตัวอย่างโค้ด สามารถดาวน์โหลดได้ [ที่นี่](https://www.nuget.org/packages/Microsoft.PowerBI.Api)</span><span class="sxs-lookup"><span data-stu-id="db174-154">The Power BI API SDK used in the code examples can be download [here](https://www.nuget.org/packages/Microsoft.PowerBI.Api).</span></span>

<span data-ttu-id="db174-155">เมื่อคุณสร้างงานส่งออก มีสามขั้นตอนเพื่อการปฏิบัติตามดังนี้:</span><span class="sxs-lookup"><span data-stu-id="db174-155">When you create an export job, there are three steps to follow:</span></span>

1. <span data-ttu-id="db174-156">ส่งคำขอการส่งออก</span><span class="sxs-lookup"><span data-stu-id="db174-156">Sending an export request.</span></span>
2. <span data-ttu-id="db174-157">การโพลล์</span><span class="sxs-lookup"><span data-stu-id="db174-157">Polling.</span></span>
3. <span data-ttu-id="db174-158">การรับไฟล์</span><span class="sxs-lookup"><span data-stu-id="db174-158">Getting the file.</span></span>

<span data-ttu-id="db174-159">หัวข้อนี้มีตัวอย่างสำหรับแต่ละขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="db174-159">This section provides examples for each step.</span></span>

### <a name="step-1---sending-an-export-request"></a><span data-ttu-id="db174-160">ขั้นตอนที่ 1 - ส่งคำขอส่งออก</span><span class="sxs-lookup"><span data-stu-id="db174-160">Step 1 - sending an export request</span></span>

<span data-ttu-id="db174-161">ขั้นตอนแรกคือการส่งคำขอส่งออก</span><span class="sxs-lookup"><span data-stu-id="db174-161">The first step is sending an export request.</span></span> <span data-ttu-id="db174-162">ในตัวอย่างนี้ ระบบได้ส่งคำขอส่งออกสำหรับช่วงหน้าที่ระบุ ขนาด และค่าพารามิเตอร์ของรายงาน</span><span class="sxs-lookup"><span data-stu-id="db174-162">In this example, an export request is sent for a specific page range, size, and report parameter values.</span></span>

```csharp
private async Task<string> PostExportRequest(
    Guid reportId,
    Guid groupId)
{
    // For documentation purposes the export configuration is created in this method
    // Ordinarily, it would be created outside and passed in
    var paginatedReportExportConfiguration = new PaginatedReportExportConfiguration()
    {
        FormatSettings = new Dictionary<string, string>()
        {
            {"PageHeight", "14in"},
            {"PageWidth", "8.5in" },
            {"StartPage", "1"},
            {"EndPage", "4"},
        },
        ParameterValues = new List<ParameterValue>()
        {
            { new ParameterValue() {Name = "State", Value = "WA"} },
            { new ParameterValue() {Name = "City", Value = "Redmond"} },
        },
    };

    var exportRequest = new ExportReportRequest
    {
        Format = FileFormat.PDF,
        PaginatedReportExportConfiguration = paginatedReportExportConfiguration,
    };

    var export = await Client.Reports.ExportToFileInGroupAsync(groupId, reportId, exportRequest);

    // Save the export ID, you'll need it for polling and getting the exported file
    return export.Id;
}
```

### <a name="step-2---polling"></a><span data-ttu-id="db174-163">ขั้นตอนที่ 2 - การโพลล์</span><span class="sxs-lookup"><span data-stu-id="db174-163">Step 2 - polling</span></span>

<span data-ttu-id="db174-164">หลังจากที่คุณส่งคำขอส่งออก ให้ใช้การโพลล์เพื่อระบุว่าไฟล์ส่งออกที่คุณรออยู่พร้อมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="db174-164">After you've sent an export request, use polling to identify when the export file you're waiting for is ready.</span></span>

```csharp
private async Task<Export> PollExportRequest(
    Guid reportId,
    Guid groupId,
    string exportId /* Get from the ExportToAsync response */,
    int timeOutInMinutes,
    CancellationToken token)
{
    Export exportStatus = null;
    DateTime startTime = DateTime.UtcNow;
    const int secToMillisec = 1000;
    do
    {
        if (DateTime.UtcNow.Subtract(startTime).TotalMinutes > timeOutInMinutes || token.IsCancellationRequested)
        {
            // Error handling for timeout and cancellations
            return null;
        }

        var httpMessage = 
            await Client.Reports.GetExportToFileStatusInGroupWithHttpMessagesAsync(groupId, reportId, exportId);
            
        exportStatus = httpMessage.Body;
        if (exportStatus.Status == ExportState.Running || exportStatus.Status == ExportState.NotStarted)
        {
            // The recommended waiting time between polling requests can be found in the RetryAfter header
            // Note that this header is only populated when the status is either Running or NotStarted
            var retryAfter = httpMessage.Response.Headers.RetryAfter;
            var retryAfterInSec = retryAfter.Delta.Value.Seconds;

            await Task.Delay(retryAfterInSec * secToMillisec);
        }
    }
    // While not in a terminal state, keep polling
    while (exportStatus.Status != ExportState.Succeeded && exportStatus.Status != ExportState.Failed);

    return exportStatus;
}
```

### <a name="step-3---getting-the-file"></a><span data-ttu-id="db174-165">ขั้นตอนที่ 3 - การรับไฟล์</span><span class="sxs-lookup"><span data-stu-id="db174-165">Step 3 - getting the file</span></span>

<span data-ttu-id="db174-166">เมื่อการโพลล์ส่งคืน URL ให้ใช้ตัวอย่างนี้เพื่อรับไฟล์ที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="db174-166">Once polling returns a URL, use this example to get the received file.</span></span>

```csharp
private async Task<ExportedFile> GetExportedFile(
    Guid reportId,
    Guid groupId,
    Export export /* Get from the GetExportStatusAsync response */)
{
    if (export.Status == ExportState.Succeeded)
    {
        var httpMessage = 
            await Client.Reports.GetFileOfExportToFileInGroupWithHttpMessagesAsync(groupId, reportId, export.Id);

        return new ExportedFile
        {
            FileStream = httpMessage.Body,
            ReportName = export.ReportName,
            FileExtension = export.ResourceFileExtension,
        };
    }

    return null;
}

public class ExportedFile
{
    public Stream FileStream;
    public string ReportName;
    public string FileExtension;
}
```

### <a name="end-to-end-example"></a><span data-ttu-id="db174-167">ตัวอย่างแบบต้นจนจบ</span><span class="sxs-lookup"><span data-stu-id="db174-167">End-to-end example</span></span>

<span data-ttu-id="db174-168">นี่คือตัวอย่างแบบต้นจนจบสำหรับการส่งออกรายงาน</span><span class="sxs-lookup"><span data-stu-id="db174-168">This is an end-to-end example for exporting a report.</span></span> <span data-ttu-id="db174-169">ตัวอย่างนี้รวมไปถึงขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="db174-169">This example includes the following stages:</span></span>
1. <span data-ttu-id="db174-170">[ส่งคำขอการส่งออก](#step-1---sending-an-export-request)</span><span class="sxs-lookup"><span data-stu-id="db174-170">[Sending the export request](#step-1---sending-an-export-request).</span></span>
2. <span data-ttu-id="db174-171">[การโพลล์](#step-2---polling)</span><span class="sxs-lookup"><span data-stu-id="db174-171">[Polling](#step-2---polling).</span></span>
3. <span data-ttu-id="db174-172">[การรับไฟล์](#step-3---getting-the-file)</span><span class="sxs-lookup"><span data-stu-id="db174-172">[Getting the file](#step-3---getting-the-file).</span></span>

```csharp
private async Task<ExportedFile> ExportPaginatedReport(
    Guid reportId,
    Guid groupId,
    int pollingtimeOutInMinutes,
    CancellationToken token)
{
    try
    {
        var exportId = await PostExportRequest(reportId, groupId);

        var export = await PollExportRequest(reportId, groupId, exportId, pollingtimeOutInMinutes, token);
        if (export == null || export.Status != ExportState.Succeeded)
        {
           // Error, failure in exporting the report
            return null;
        }

        return await GetExportedFile(reportId, groupId, export);
    }
    catch
    {
        // Error handling
        throw;
    }
}
```

## <a name="limitations"></a><span data-ttu-id="db174-173">ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="db174-173">Limitations</span></span>

<span data-ttu-id="db174-174">การส่งออกรายงานที่มีการแบ่งหน้าที่มีชุดข้อมูล Power BI เป็นแหล่งข้อมูลไม่ได้รับการสนับสนุนสำหรับหลักการบริการ</span><span class="sxs-lookup"><span data-stu-id="db174-174">Exporting a paginated report that has a Power BI dataset as its data source, is not supported for service principals.</span></span>

## <a name="next-steps"></a><span data-ttu-id="db174-175">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="db174-175">Next steps</span></span>

<span data-ttu-id="db174-176">ตรวจทานวิธีการฝังเนื้อหาสำหรับลูกค้าและองค์กรของคุณ:</span><span class="sxs-lookup"><span data-stu-id="db174-176">Review how to embed content for your customers and your organization:</span></span>

> [!div class="nextstepaction"]
>[<span data-ttu-id="db174-177">ส่งออกรายงานไปยังไฟล์</span><span class="sxs-lookup"><span data-stu-id="db174-177">Export report to file</span></span>](export-to.md)

> [!div class="nextstepaction"]
>[<span data-ttu-id="db174-178">ฝังสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="db174-178">Embed for your customers</span></span>](embed-sample-for-customers.md)

> [!div class="nextstepaction"]
>[<span data-ttu-id="db174-179">ฝังตัวสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="db174-179">Embed for your organization</span></span>](embed-sample-for-your-organization.md)
