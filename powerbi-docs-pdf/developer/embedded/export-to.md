---
title: ส่งออก API ของรายงานการวิเคราะห์แบบฝังตัวของ Power BI สำหรับข้อมูลเชิงลึก BI ที่ฝังตัวได้ดีขึ้น
description: เรียนรู้วิธีการส่งออกรายงาน Power BI แบบฝังตัวเพื่อปรับปรุงประสบการณ์ การใช้งาน BI แบบฝังตัวของการวิเคราะห์ Power BI ของคุณ เปิดใช้งานข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.topic: how-to
ms.service: powerbi
ms.subservice: powerbi-developer
ms.date: 02/01/2021
ms.openlocfilehash: 64a9472960195c8d4f91013a778bb61cdf029ab4
ms.sourcegitcommit: 2e81649476d5cb97701f779267be59e393460097
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 02/02/2021
ms.locfileid: "99422363"
---
# <a name="export-power-bi-report-to-file-preview"></a>ส่งออกรายงาน Power BI ไปยังไฟล์ (ตัวอย่าง)

`exportToFile`API เปิดใช้งานการส่งออกรายงาน Power BI โดยใช้การเรียกใช้ REST รูปแบบไฟล์ต่อไปนี้ได้รับการรองรับ:
* **.pptx** (PowerPoint)
* **.pdf**
* **.png**
    * ขณะที่ส่งออกในรูปแบบ .png รายงานที่มีหลายหน้าจะถูกบีบอัดเป็นไฟล์ .zip
    * แต่ละไฟล์ใน .zip จะแสดงหน้ารายงาน
    * ชื่อหน้าจะเหมือนกับค่าที่ส่งกลับของ API [รับหน้า](/rest/api/power-bi/reports/getpages)หรือ[รับหน้าในกลุ่ม](/rest/api/power-bi/reports/getpagesingroup)

## <a name="usage-examples"></a>ตัวอย่างการใช้งาน

คุณสามารถใช้ฟีเจอร์การส่งออกได้หลายวิธี นี่เป็นตัวอย่างสองตัวอย่าง:

* **ส่งไปยังปุ่มพิมพ์** - ในแอปพลิเคชันของคุณ ให้สร้างปุ่มที่เมื่อคลิกที่จะทริกเกอร์งานการส่งออก งานสามารถส่งออกรายงานที่เป็น .pdf หรือ .pptx และเมื่อเสร็จสมบูรณ์ ผู้ใช้จะสามารถรับไฟล์เป็นการดาวน์โหลดได้ คุณสามารถใช้บุ๊กมาร์กส่งออกรายงานในสถานะที่ระบุ รวมถึงตัวกรองที่กำหนดค่า ตัวแบ่งส่วนข้อมูล และการตั้งค่าเพิ่มเติมได้ ในฐานะที่เป็น API แบบอะซิงโครนัส อาจใช้เวลาสักครู่ก่อนที่ไฟล์จะพร้อมใช้งาน

* **ไฟล์แนบอีเมล** - ส่งอีเมลโดยอัตโนมัติในช่วงเวลาที่ตั้งค่า ด้วยรายงาน .pdf ที่แนบมา สถานการณ์นี้อาจเป็นประโยชน์ถ้าคุณต้องการส่งรายงานรายสัปดาห์ไปยังฝ่ายบริหารโดยอัตโนมัติ สำหรับข้อมูลเพิ่มเติมให้ดูที่การ[ส่งออกและส่งอีเมลพร้อมรายงาน Power BI ด้วย Power Automate](../../collaborate-share/service-automate-power-bi-report-export.md)

## <a name="using-the-api"></a>การใช้ API

ก่อนที่จะใช้ API ให้ยืนยันว่ามีการเปิดใช้งาน[การตั้งค่าผู้เช่าผู้ดูแลระบบ](../../admin/service-admin-portal.md#tenant-settings)ดังต่อไปนี้:
* **ส่งออกรายงานในรูปแบบงานนำเสนอ PowerPoint หรือเอกสาร PDF** - เปิดใช้งานโดยค่าเริ่มต้น
* **ส่งออกรายงานเป็นไฟล์รูปภาพ** - จำเป็นสำหรับ *.png* เท่านั้นและปิดใช้งานตามค่าเริ่มต้น

API เป็นแบบอะซิงโครนัส เมื่อมีการเรียกใช้ API [exportToFile](/rest/api/power-bi/reports/exporttofile) จะทริกเกอร์งานการส่งออก หลังจากทริกเกอร์งานส่งออก ให้ใช้[การโพลล์](/rest/api/power-bi/reports/getexporttofilestatus)เพื่อติดตามงานจนกว่าจะเสร็จสมบูรณ์

ในระหว่างการโพลล์ API จะส่งกลับตัวเลขที่แสดงถึงจำนวนการทำงานที่เสร็จสมบูรณ์ งานในแต่ละงานการส่งออกจะถูกคำนวณโดยยึดตามผลรวมของการส่งออกในงาน การส่งออกมีการส่งออกวิชวลเดียวหรือหน้าที่มีหรือไม่มีบุ๊กมาร์ก การส่งออกทั้งหมดมีน้ำหนักเดียวกัน ถ้าตัวอย่างเช่นงานการส่งออกของคุณมีการส่งออกรายงานด้วย10หน้าและการ polling ส่งกลับ๗๐หมายความว่า API ได้รับการประมวลผลเจ็ดจาก10หน้าในงานส่งออก

เมื่อการส่งออกเสร็จสิ้น การเรียกใช้ API การโพลล์จะส่งคืน [URL ของ Power BI](/rest/api/power-bi/reports/getfileofexporttofile) สำหรับรับไฟล์ URL จะพร้อมใช้งานเป็นเวลา 24 ชั่วโมง

## <a name="supported-features"></a>ฟีเจอร์ที่ได้รับการรองรับ

ส่วนนี้อธิบายการดำเนินการของคุณลักษณะที่ได้รับการสนับสนุนต่อไปนี้:

* [การเลือกหน้าเพื่อพิมพ์](#selecting-which-pages-to-print)
* [การส่งออกหน้าหรือการแสดงผลด้วยภาพเดียว](#exporting-a-page-or-a-single-visual)
* [บุ๊กมาร์ก](#bookmarks)
* [ตัวกรอง](#filters)
* [การรับรองความถูกต้อง](#authentication)
* [การรักษาความปลอดภัยระดับแถว (RLS)](#row-level-security-rls)
* [การป้องกันข้อมูล](#data-protection)
* [การแปลเป็นภาษาท้องถิ่น](#localization)

### <a name="selecting-which-pages-to-print"></a>การเลือกหน้าเพื่อพิมพ์

ระบุหน้าที่คุณต้องการพิมพ์ตามค่าส่งคืนการ[รับหน้า](/rest/api/power-bi/reports/getpages)หรือ[รับหน้าในกลุ่ม](/rest/api/power-bi/reports/getpagesingroup) คุณยังสามารถระบุลำดับของหน้าที่คุณกำลังส่งออกได้

### <a name="exporting-a-page-or-a-single-visual"></a>การส่งออกหน้าหรือการแสดงผลด้วยภาพเดียว

คุณสามารถระบุหน้าหรือการแสดงผลด้วยภาพเดียวเพื่อส่งออก สามารถส่งออกหน้าเว็บที่มีหรือไม่มีบุ๊กมาร์กได้

ขึ้นอยู่กับชนิดของการส่งออกคุณต้องผ่านแอตทริบิวต์ที่แตกต่างกันไปยังวัตถุ[ExportReportPage](/rest/api/power-bi/reports/exporttofile#exportreportpage) ตารางด้านล่างระบุแอตทริบิวต์ที่จำเป็นสำหรับแต่ละงานการส่งออก  

>[!NOTE]
>การส่งออกวิชวลเดียวมีน้ำหนักเดียวกับการส่งออกหน้า (มีหรือไม่มีที่คั่นหน้า) ซึ่งหมายความว่าในแง่ของการคำนวณระบบการดำเนินการทั้งสองจะดำเนินการค่าเดียวกัน

|แอตทริบิวต์   |หน้า     |ภาพเดียว  |ข้อคิดเห็น|
|------------|---------|---------|---|
|`bookmark`  |ไม่จำเป็น |![ไม่นำไปใช้](../../media/no.png)|ใช้เพื่อส่งออกหน้าในสถานะที่ระบุ|
|`pageName`  |![นำไปใช้กับ](../../media/yes.png)|![นำไปใช้กับ](../../media/yes.png)|ใช้ REST API [GetPages](/rest/api/power-bi/reports/getpage) หรือ API ของ `getPages` ไคลเอ็นต์ สำหรับข้อมูลเพิ่มเติมดู [รับหน้าและ](/javascript/api/overview/powerbi/get-visuals)วิชวล   |
|`visualName`|![ไม่นำไปใช้](../../media/no.png)|![นำไปใช้กับ](../../media/yes.png)|มีสองวิธีในการรับชื่อของวิชวล:<li>ใช้ `getVisuals` API ของไคลเอ็นต์ สำหรับข้อมูลเพิ่มเติมดู [รับหน้าและ](/javascript/api/overview/powerbi/get-visuals)วิชวล</li><li>ฟังและบันทึกเหตุการณ์ *visualClicked* ซึ่งจะถูกทริกเกอร์เมื่อมีการเลือกวิชวล สำหรับข้อมูลเพิ่มเติมดู [วิธีการจัดการเหตุการณ์](/javascript/api/overview/powerbi/handle-events)</li>. |

### <a name="bookmarks"></a>บุ๊กมาร์ก

[คุณสามารถใช้บุ๊กมาร์ก](../../consumer/end-user-bookmarks.md) เพื่อบันทึกรายงานในการกำหนดค่าเฉพาะรวมถึงตัวกรองที่นำไปใช้และสถานะของการแสดงผลด้วยภาพของรายงาน คุณสามารถใช้ API [exportToFile](/rest/api/power-bi/reports/exporttofile) เพื่อส่งออกบุ๊กมาร์กของรายงานโดยทางโปรแกรมได้สองวิธี:

* **ส่งออกบุ๊กมาร์กที่มีอยู่**

    หากต้องการส่งออกที่คั่นหน้ารายงาน [ที่มีอยู่](../../consumer/end-user-bookmarks.md#report-bookmarks)ให้ใช้คุณสมบัติ `name` ซึ่งเป็นตัวระบุที่ไม่ซ้ำกัน (ตรงตามตัวพิมพ์ใหญ่-เล็ก) ที่คุณสามารถรับได้โดยใช้ [ที่คั่นหน้าของ JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Bookmarks)

* **ส่งออกสถานะของรายงาน**

    เมื่อต้องการส่งออกสถานะปัจจุบันของรายงานให้ใช้คุณสมบัติ `state` ตัวอย่างเช่นคุณสามารถใช้วิธีการ `bookmarksManager.capture` ของบุ๊กมาร์กเพื่อจับภาพการเปลี่ยนแปลงของผู้ใช้ที่ระบุที่ทำกับรายงานจากนั้นส่งออกในสถานะปัจจุบันโดยใช้ `capturedBookmark.state`

>[!NOTE]
>ไม่รองรับ[บุ๊กมาร์กส่วนบุคคล](../../consumer/end-user-bookmarks.md#personal-bookmarks)และ[ตัวกรองแบบถาวร](https://powerbi.microsoft.com/blog/announcing-persistent-filters-in-the-service/)

### <a name="filters"></a>ตัวกรอง

การใช้ `reportLevelFilters` ใน [PowerBIReportExportConfiguration](/rest/api/power-bi/reports/exporttofile#powerbireportexportconfiguration) คุณสามารถส่งออกรายงานในเงื่อนไขที่ถูกกรองได้

เมื่อต้องการส่งออกรายงานที่ถูกกรอง ให้แทรก[พารามิเตอร์สตริงแบบสอบถาม URL](../../collaborate-share/service-url-filters.md) ที่คุณต้องการใช้เป็นตัวกรองของคุณ เพื่อ [ExportFilter](/rest/api/power-bi/reports/exporttofile#exportfilter) เมื่อคุณใส่สตริงที่ คุณต้องนำส่วน `?filter=` ของพารามิเตอร์แบบสอบถาม URL ออก

ตารางด้านล่างนี้ประกอบด้วยตัวอย่างของสตริงข้อความที่คุณสามารถส่งผ่านไปยัง  `ExportFilter` ได้

|ตัวกรอง    |ไวยากรณ์    |ตัวอย่าง    |
|---|----|----|----|
|ค่าในเขตข้อมูล    |ของตาราง/ฟิลด์ eq 'ค่า'    |ร้านค้า/อาณาเขต eq 'NC'    |
|หลายค่าในเขตข้อมูล    |ตาราง/เขตข้อมูลใน ('value1', 'value2')     |ร้านค้า/อาณาเขตใน ('NC', 'TN')    |
|ค่าที่แตกต่างกันในเขตข้อมูลหนึ่งและค่าที่แตกต่างในเขตข้อมูลอื่น    |ตาราง/Field1 eq 'value1' และตาราง/Field2 eq 'value2'    |ร้านค้า/อาณาเขต eq 'NC' และร้านค้า/เครือข่าย eq 'Fashions Direct'    |

>[!NOTE]
>`ReportLevelFilters` สามารถมีได้เฉพาะ [ExportFilter](/rest/api/power-bi/reports/exporttofile#exportfilter) เดียวเท่านั้น

### <a name="authentication"></a>การรับรองความถูกต้อง

คุณสามารถรับรองความถูกต้องได้โดยใช้ผู้ใช้ (หรือผู้ใช้หลัก) หรือ [หลักบริการ](embed-service-principal.md)

### <a name="row-level-security-rls"></a>การรักษาความปลอดภัยระดับแถว (RLS)

ด้วย[การรักษาความปลอดภัยระดับแถว (RLS)](embedded-row-level-security.md) คุณสามารถส่งออกรายงานที่แสดงข้อมูลที่สามารถมองเห็นได้เฉพาะผู้ใช้บางรายเท่านั้น ตัวอย่างเช่น ถ้าคุณกำลังส่งออกรายงานยอดขายที่กำหนดไว้กับบทบาทภูมิภาค คุณสามารถกรองรายงานเพื่อให้แสดงเฉพาะภูมิภาคที่ระบุเท่านั้นได้

หากต้องการส่งออกโดยใช้ RLS คุณต้องมีสิทธิ์ต่อไปนี้:
* สิทธิ์การเขียนและแชร์ต่อสำหรับชุดข้อมูลที่มีการเชื่อมต่อกับรายงาน
* ถ้ารายงานอยู่ในพื้นที่ทำงาน v1 คุณจะต้องเป็นผู้ดูแลระบบพื้นที่ทำงาน
* ถ้ารายงานอยู่ในพื้นที่ทำงาน v2 คุณจะต้องเป็นผู้ดูแลระบบพื้นที่ทำงาน

### <a name="data-protection"></a>การป้องกันข้อมูล

รูปแบบ .pdf และ .pptx รองรับ[ป้ายชื่อระดับความลับ](../../admin/service-security-sensitivity-label-overview.md) หากคุณส่งออกรายงานที่มีป้ายชื่อระดับความลับในรูปแบบ .pdf หรือ .pptx ไฟล์ที่ส่งออกจะแสดงรายงานที่มีป้ายชื่อระดับความลับ

รายงานที่มีป้ายชื่อระดับความลับ จะไม่สามารถส่งออกในรูปแบบ .pdf หรือ .pptx โดยใช้ [หลักบริการ](embed-service-principal.md) ได้

### <a name="localization"></a>การแปลเป็นภาษาท้องถิ่น

เมื่อใช้ `exportToFile` API คุณสามารถผ่านท้องถิ่นที่คุณต้องการได้ การตั้งค่าการแปลมีผลต่อวิธีการแสดงรายงาน ตัวอย่างเช่น โดยการเปลี่ยนการจัดรูปแบบโดยอ้างอิงจากเครื่องที่เลือก

## <a name="concurrent-requests"></a>คำขอที่เกิดขึ้นพร้อมกัน

`exportToFile` รองรับคำของานการส่งออกที่เกิดขึ้นพร้อมกัน ตารางด้านล่างแสดงจำนวนของงานที่คุณสามารถเรียกใช้ในเวลาเดียวกันได้โดยขึ้นอยู่กับ SKU รายงานของคุณ คำขอที่เกิดขึ้นพร้อมกันจะอ้างอิงไปยังหน้ารายงาน ตัวอย่างเช่น 20 หน้าในคำขอการส่งออกในหนึ่ง A6 SKU จะได้รับการประมวลผลพร้อมๆ กัน การดำเนินการนี้จะใช้เวลาพอๆ กันกับการส่งคำขอการส่งออก 20 ครั้งต่อหนึ่งหน้า

งานที่เกินจำนวนคำขอที่เกิดขึ้นพร้อมกันจะไม่ยุติลง ตัวอย่างเช่น ถ้าคุณส่งออกสามหน้าใน A1 SKU งานแรกจะเรียกใช้ และสองงานหลังจะต้องสองรอบการดำเนินการถัดไป

>[!NOTE]
>การส่งออกรายงาน Power BI ไปยังไฟล์โดยใช้ API `exporToFile` ไม่รองรับสำหรับ [Premium Per User (PPU)](../../admin/service-premium-per-user-faq.md) 

|Azure SKU  |Office SKU  |หน้ารายงานที่เกิดขึ้นพร้อมกันสูงสุด  |
|-----------|------------|-----------|
|A1         |EM1         |1          |
|A2         |EM2         |2          |
|A3         |EM3         |3          |
|A4         |P1          |6          |
|A5         |P2          |12         |
|A6         |P3          |24         |

## <a name="limitations"></a>ข้อจำกัด

* รายงานที่คุณกำลังส่งออกต้องอยู่บนความจุพรีเมียมหรือแบบฝัง
* ชุดข้อมูลที่คุณกำลังส่งออกต้องอยู่บนความจุ
* สำหรับการแสดงตัวอย่างสาธารณะจำนวนการส่งออก Power BI ต่อชั่วโมงถูกจำกัดไว้ที่๕๐ต่อความจุ การส่งออกอ้างอิงถึงการส่งออกภาพเดียวหรือหน้ารายงานที่มีหรือไม่มีบุ๊กมาร์กและไม่มีการส่งออกรายงานจน
* รายงานที่ส่งออกต้องมีขนาดไฟล์ไม่เกิน 250 MB
* เมื่อส่งออกในรูปแบบ .png ป้ายชื่อความระดับความลับจะไม่ได้รับการสนับสนุน
* จำนวนการส่งออก (วิชวลเดี่ยวหรือหน้ารายงาน) ที่สามารถรวมอยู่ในรายงานที่ส่งออกคือ๕๐ (ซึ่งไม่รวมถึงการส่งออกรายงานจน) ถ้าการร้องขอมีการส่งออกเพิ่มเติม API ส่งกลับข้อผิดพลาดและงานการส่งออกถูกยกเลิก
* ไม่รองรับ[บุ๊กมาร์กส่วนบุคคล](../../consumer/end-user-bookmarks.md#personal-bookmarks)และ[ตัวกรองแบบถาวร](https://powerbi.microsoft.com/blog/announcing-persistent-filters-in-the-service/)
* การแสดงผลด้วยภาพของ Power BI ที่แสดงในรายการด้านล่างไม่ได้รับการรองรับ เมื่อรายงานที่มีการแสดงผลด้วยภาพเหล่านี้ถูกส่งออก ส่วนของรายงานที่ประกอบด้วยการแสดงผลด้วยภาพดังกล่าวจะไม่แสดง และจะแสดงสัญลักษณ์ข้อผิดพลาด
    * การแสดงผลด้วยภาพของ Power BI ที่ไม่ผ่านการจัดการ
    * วิชวล R
    * PowerApps
    * การแสดงผลด้วยภาพของ Python
    * Visio

## <a name="code-examples"></a>ตัวอย่างรหัส

เมื่อคุณสร้างงานส่งออก มีสามขั้นตอนเพื่อการปฏิบัติตามดังนี้:

1. [การส่งคำขอการส่งออก](#step-1---sending-an-export-request)
2. [การโพลล์](#step-2---polling)
3. [การรับไฟล์](#step-3---getting-the-file)
4. [การใช้สตรีมไฟล์](#step-4---using-the-file-stream)

หัวข้อนี้มีตัวอย่างสำหรับแต่ละขั้นตอน

### <a name="step-1---sending-an-export-request"></a>ขั้นตอนที่ 1 - ส่งคำขอส่งออก

ขั้นตอนแรกคือการส่งคำขอส่งออก ในตัวอย่างนี้ คำขอส่งออกจะถูกส่งไปยังหน้าที่ระบุ

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

### <a name="step-2---polling"></a>ขั้นตอนที่ 2 - การโพลล์

หลังจากที่คุณส่งคำขอส่งออก ให้ใช้การโพลล์เพื่อระบุว่าไฟล์ส่งออกที่คุณรออยู่พร้อมหรือไม่

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

### <a name="step-3---getting-the-file"></a>ขั้นตอนที่ 3 - การรับไฟล์

เมื่อการโพลล์ส่งคืน URL ให้ใช้ตัวอย่างนี้เพื่อรับไฟล์ที่ได้รับ

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

### <a name="step-4---using-the-file-stream"></a>ขั้นตอนที่ 4 - การใช้สตรีมไฟล์

เมื่อคุณมีสตรีมไฟล์ คุณสามารถจัดการได้ในแบบที่เหมาะกับความต้องการของคุณมากที่สุด ตัวอย่างเช่น คุณสามารถส่งอีเมลหรือใช้เพื่อดาวน์โหลดรายงานที่ส่งออก

### <a name="end-to-end-example"></a>ตัวอย่างแบบต้นจนจบ

นี่คือตัวอย่างแบบต้นจนจบสำหรับการส่งออกรายงาน ตัวอย่างนี้รวมไปถึงขั้นตอนต่อไปนี้:
1. [ส่งคำขอการส่งออก](#step-1---sending-an-export-request)
2. [การโพลล์](#step-2---polling)
3. [การรับไฟล์](#step-3---getting-the-file)

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

## <a name="next-steps"></a>ขั้นตอนถัดไป

ตรวจทานวิธีการฝังเนื้อหาสำหรับลูกค้าและองค์กรของคุณ:

> [!div class="nextstepaction"]
>[ส่งออกรายงานที่มีการแบ่งหน้าไปยังไฟล์](export-paginated-report.md)

> [!div class="nextstepaction"]
>[ฝังสำหรับลูกค้าของคุณ](embed-sample-for-customers.md)

> [!div class="nextstepaction"]
>[ฝังตัวสำหรับองค์กรของคุณ](embed-sample-for-your-organization.md)

> [!div class="nextstepaction"]
>[ส่งออกและส่งอีเมลรายงาน Power BI ด้วย Power Automate](../../collaborate-share/service-automate-power-bi-report-export.md)
