---
title: ส่งออก API รายงานที่มีการแบ่งหน้าของการวิเคราะห์แบบฝังตัวของ Power BI สำหรับข้อมูลเชิงลึก BI ที่ฝังตัวได้ดีขึ้น
description: เรียนรู้วิธีการส่งออกรายงานที่มีการแบ่งหน้า Power BI แบบฝังตัว เปิดใช้งานข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.topic: how-to
ms.service: powerbi
ms.subservice: powerbi-developer
ms.date: 04/05/2020
ms.openlocfilehash: befb64ec85c02f8993d828202df06aafc5901482
ms.sourcegitcommit: 84f0e7f31e62cae3bea2dcf2d62c2f023cc2d404
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 01/26/2021
ms.locfileid: "98781535"
---
# <a name="export-paginated-report-to-file-preview"></a>ส่งออกรายงานที่มีการแบ่งหน้าไปยังไฟล์ (ตัวอย่าง)

`exportToFile` API เปิดใช้งานการส่งออกรายงาน Power BI ที่มีการแบ่งหน้าโดยใช้การเรียกใช้ REST รูปแบบไฟล์ต่อไปนี้ได้รับการรองรับ:
* **.pptx** (PowerPoint)
* **.pdf**
* **.xlsx** (Excel)
* **.dox** (Word)
* **.csv**
* **.xml**
* **.mhtml**
* **รูปภาพ**
    * เมื่อส่งออกไปยังรูปภาพ ให้ตั้งค่ารูปแบบรูปภาพผ่าน `OutputFormat` การตั้งค่ารูปแบบ
    * ค่า OutputFormat ที่ได้รับการสนับสนุนคือ: .bmp, .emf, .gif, .jpeg, .png หรือ .tiff (ค่าเริ่มต้น)

## <a name="usage-examples"></a>ตัวอย่างการใช้งาน

คุณสามารถใช้ฟีเจอร์การส่งออกได้หลายวิธี นี่เป็นตัวอย่างสองตัวอย่าง:

* **ส่งไปยังปุ่มพิมพ์** - ในแอปพลิเคชันของคุณ ให้สร้างปุ่มที่เมื่อคลิกที่จะทริกเกอร์งานการส่งออก งานสามารถส่งออกรายงานที่เป็น .pdf หรือ .pptx และเมื่อเสร็จสมบูรณ์ ผู้ใช้จะสามารถรับไฟล์เป็นการดาวน์โหลดได้ การใช้พารามิเตอร์รายงานและการตั้งค่ารูปแบบจะทำให้คุณสามารถส่งออกรายงานในสถานะที่ระบุ รวมถึงข้อมูลที่กรอง ขนาดหน้าแบบกำหนดเอง และการตั้งค่าเฉพาะรูปแบบอื่นๆ ในฐานะที่เป็น API แบบอะซิงโครนัส อาจใช้เวลาสักครู่ก่อนที่ไฟล์จะพร้อมใช้งาน

* **ไฟล์แนบอีเมล** - ส่งอีเมลโดยอัตโนมัติในช่วงเวลาที่ตั้งค่า ด้วยรายงาน .pdf ที่แนบมา สถานการณ์นี้อาจเป็นประโยชน์ถ้าคุณต้องการส่งรายงานรายสัปดาห์ไปยังฝ่ายบริหารโดยอัตโนมัติ

## <a name="using-the-api"></a>การใช้ API

API เป็นแบบอะซิงโครนัส เมื่อมีการเรียกใช้ API [exportToFile](/rest/api/power-bi/reports/exporttofile) จะทริกเกอร์งานการส่งออก หลังจากทริกเกอร์งานส่งออก ให้ใช้[การโพลล์](/rest/api/power-bi/reports/getexporttofilestatus)เพื่อติดตามงานจนกว่าจะเสร็จสมบูรณ์

เมื่อการส่งออกเสร็จสิ้น การเรียกใช้ API การโพลล์จะส่งคืน [URL ของ Power BI](/rest/api/power-bi/reports/getfileofexporttofile) สำหรับรับไฟล์ URL จะพร้อมใช้งานเป็นเวลา 24 ชั่วโมง

## <a name="supported-features"></a>ฟีเจอร์ที่ได้รับการรองรับ

### <a name="format-settings"></a>การตั้งค่ารูปแบบ

ระบุการตั้งค่ารูปแบบที่หลากหลายสำหรับแต่ละรูปแบบไฟล์ คุณสมบัติและค่าที่ได้รับการสนับสนุนจะเทียบเท่ากับ [พารามิเตอร์ข้อมูลอุปกรณ์](../../paginated-reports/report-builder-url-parameters.md#report-commands-rdl) สำหรับพารามิเตอร์ URL ของรายงานที่มีการแบ่งหน้า

ต่อไปนี้ป็นตัวอย่างสองรายการ รายการแรกคือการส่งออกสี่หน้าแรกของรายงานโดยใช้ขนาดหน้ารายงาน ในรูปแบบไฟล์ .pptx และอีกรายการหนึ่งคือ การส่งออกหน้าที่สามของรายงาน ในรูปแบบไฟล์ .jpeg

**การส่งออกสี่หน้าแรกในรูปแบบ .pptx**

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

**การส่งออกหน้าที่สามในรูปแบบ .jpeg**

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

### <a name="report-parameters"></a>รายงานพารามิเตอร์

คุณสามารถใช้ `exportToFile` API เพื่อส่งออกรายงานด้วยชุดพารามิเตอร์ของรายงานโดยทางโปรแกรม การดำเนินการนี้จะทำได้โดยใช้ความสามารถของ [พารามิเตอร์รายงาน](../../paginated-reports/paginated-reports-parameters.md)

ต่อไปนี้คือตัวอย่างสำหรับการตั้งค่าของพารามิเตอร์รายงาน

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

### <a name="authentication"></a>การรับรองความถูกต้อง

คุณสามารถรับรองความถูกต้องได้โดยใช้ผู้ใช้ (หรือผู้ใช้หลัก) หรือ [หลักบริการ](embed-service-principal.md)

### <a name="row-level-security-rls"></a>การรักษาความปลอดภัยระดับแถว (RLS)

ขณะที่ใช้ชุดข้อมูล Power BI ที่มีความปลอดภัยระดับแถว (RLS) ซึ่งกำหนดให้เป็นแหล่งข้อมูล คุณจะสามารถส่งออกรายงานที่แสดงข้อมูลที่จะมีผู้ใช้บางรายเท่านั้นที่เห็น ตัวอย่างเช่น ถ้าคุณกำลังส่งออกรายงานยอดขายที่กำหนดไว้กับบทบาทภูมิภาค คุณสามารถกรองรายงานเพื่อให้แสดงเฉพาะภูมิภาคที่ระบุเท่านั้นได้

เมื่อต้องการส่งออกโดยใช้ RLS คุณจำเป็นต้องมีสิทธิ์การอ่านสำหรับชุดข้อมูล Power BI ที่รายงานกำลังใช้เป็นแหล่งข้อมูล

ต่อไปนี้คือตัวอย่างสำหรับการใช้ชื่อผู้ใช้ที่มีประสิทธิภาพสำหรับ RLS

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

### <a name="single-sign-on-sql-and-dataverse-sso"></a>การลงชื่อเข้าระบบครั้งเดียวใน SQL และ Dataverse (SSO)

ใน Power BI คุณมีตัวเลือกในการตั้งค่า OAuth ด้วย SSO เมื่อคุณทำเช่นนั้นข้อมูลประจำตัวสำหรับผู้ใช้ที่ดูรายงานจะถูกใช้เพื่อดึงข้อมูล โทเค็นการเข้าถึงในส่วนหัว requrest ไม่ได้ถูกใช้ในการเข้าถึงข้อมูลโทเค็นจะต้องได้รับการส่งผ่านไปด้วยข้อมูลประจำตัวที่มีผลบังคับใช้ในเนื้อความของโพสต์

สิ่งที่สามารถทำให้โทเค็นการเข้าถึงสับสนได้รับโทเค็นการเข้าถึงที่ถูกต้องสำหรับทรัพยากรที่คุณต้องการเข้าถึง

- สำหรับ Azure SQL `https://database.windows.net` ทรัพยากรคือ
- สำหรับ Dataverse ทรัพยากรคือ `https://` ที่อยู่สำหรับสภาพแวดล้อมของคุณ `https://contoso.crm.dynamics.com`ตัวอย่างเช่น

เข้าถึงโทเค็น API โดยใช้เมธอด[AuthenticationContext AcquireTokenAsync](https://docs.microsoft.com/dotnet/api/microsoft.identitymodel.clients.activedirectory.authenticationcontext.acquiretokenasync)

ต่อไปนี้เป็นตัวอย่างสำหรับการจัดหาชื่อผู้ใช้ที่มีประสิทธิภาพด้วยโทเค็นการเข้าถึง

```json
{
       "format":"PDF",
       "paginatedReportConfiguration":{
          "formatSettings":{
             "AccessiblePDF":"true",
             "PageHeight":"11in",
             "PageWidth":"8.5in",
             "MarginBottom":"2in"
          },
          "identities":[
             {
                "username":"john@contoso.com",
                "identityBlob": {
                "value": "eyJ0eX....full access token"
         }
        }
     ]
   }
}
```

## <a name="ppu-concurrent-requests"></a>คำขอที่เกิดขึ้นพร้อมกันสำหรับ PPU
API `exportToFile` อนุญาตให้มีหนึ่งคำขอในช่วงเวลาห้านาทีเมื่อใช้ [Premium Per User (PPU)](../../admin/service-premium-per-user-faq.md) คำขอหลายรายการ (มากกว่าหนึ่งรายการ) ภายในช่วงเวลาห้านาทีจะทำให้เกิดข้อผิดพลาด (429) *คำขอมากเกินไป*

## <a name="code-examples"></a>ตัวอย่างรหัส

Power BI API SDK ที่ใช้ในตัวอย่างโค้ด สามารถดาวน์โหลดได้ [ที่นี่](https://www.nuget.org/packages/Microsoft.PowerBI.Api)

เมื่อคุณสร้างงานส่งออก มีสามขั้นตอนเพื่อการปฏิบัติตามดังนี้:

1. ส่งคำขอการส่งออก
2. การโพลล์
3. การรับไฟล์

หัวข้อนี้มีตัวอย่างสำหรับแต่ละขั้นตอน

### <a name="step-1---sending-an-export-request"></a>ขั้นตอนที่ 1 - ส่งคำขอส่งออก

ขั้นตอนแรกคือการส่งคำขอส่งออก ในตัวอย่างนี้ ระบบได้ส่งคำขอส่งออกสำหรับช่วงหน้าที่ระบุ ขนาด และค่าพารามิเตอร์ของรายงาน

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

### <a name="step-2---polling"></a>ขั้นตอนที่ 2 - การโพลล์

หลังจากที่คุณส่งคำขอส่งออก ให้ใช้การโพลล์เพื่อระบุว่าไฟล์ส่งออกที่คุณรออยู่พร้อมหรือไม่

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

### <a name="step-3---getting-the-file"></a>ขั้นตอนที่ 3 - การรับไฟล์

เมื่อการโพลล์ส่งคืน URL ให้ใช้ตัวอย่างนี้เพื่อรับไฟล์ที่ได้รับ

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

### <a name="end-to-end-example"></a>ตัวอย่างแบบต้นจนจบ

นี่คือตัวอย่างแบบต้นจนจบสำหรับการส่งออกรายงาน ตัวอย่างนี้รวมไปถึงขั้นตอนต่อไปนี้:
1. [ส่งคำขอการส่งออก](#step-1---sending-an-export-request)
2. [การโพลล์](#step-2---polling)
3. [การรับไฟล์](#step-3---getting-the-file)

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

## <a name="limitations"></a>ข้อจำกัด

การส่งออกรายงานที่มีการแบ่งหน้าที่มีชุดข้อมูล Power BI เป็นแหล่งข้อมูลไม่ได้รับการสนับสนุนสำหรับหลักการบริการ

## <a name="next-steps"></a>ขั้นตอนถัดไป

ตรวจทานวิธีการฝังเนื้อหาสำหรับลูกค้าและองค์กรของคุณ:

> [!div class="nextstepaction"]
>[ส่งออกรายงานไปยังไฟล์](export-to.md)

> [!div class="nextstepaction"]
>[ฝังสำหรับลูกค้าของคุณ](embed-sample-for-customers.md)

> [!div class="nextstepaction"]
>[ฝังตัวสำหรับองค์กรของคุณ](embed-sample-for-your-organization.md)
