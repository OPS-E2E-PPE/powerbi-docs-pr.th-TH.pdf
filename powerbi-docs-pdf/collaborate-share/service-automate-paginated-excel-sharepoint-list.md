---
title: ส่งออกรายงานที่มีการแบ่งหน้าสำหรับแต่ละแถวในตาราง Excel Online หรือรายการ SharePoint
description: ในบทความนี้คุณใช้ Power Automate เพื่อทำให้การส่งออกรายงานที่มีการแบ่งหน้าสำหรับแต่ละแถวในตาราง Excel Online หรือรายการ SharePoint Online เป็นแบบอัตโนมัติ
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 12/08/2020
LocalizationGroup: Get started
ms.openlocfilehash: 7a48a9a594364de4261aa66de48c1a4262392364
ms.sourcegitcommit: bbf7e9341a4e1cc96c969e24318c8605440282a5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/11/2020
ms.locfileid: "97097857"
---
# <a name="export-a-paginated-report-for-each-row-in-an-excel-online-table-or-sharepoint-list"></a>ส่งออกรายงานที่มีการแบ่งหน้าสำหรับแต่ละแถวในตาราง Excel Online หรือรายการ SharePoint

ด้วย [Power Automate](/power-automate/getting-started) คุณสามารถทำให้การส่งออกและการแจกจ่ายรายงานที่มีการแบ่งหน้า Power BI ไปยังรูปแบบและสถานการณ์ที่ได้รับการสนับสนุนเป็นแบบอัตโนมัติ ในบทความนี้ คุณใช้เทมเพลต Power Automate เพื่อทำให้การตั้งค่าการส่งออกที่เกิดซ้ำของรายงานที่มีการแบ่งหน้าเดียวหรือหลายรายงานเป็นแบบอัตโนมัติ คุณส่งออกรายงานเหล่านั้นในรูปแบบที่ต้องการสำหรับแต่ละแถวในตาราง Excel Online หรือรายการ SharePoint Online คุณสามารถแจกจ่ายรายงานที่มีการแบ่งหน้าที่ส่งออกไปยัง OneDrive for Business หรือไซต์ SharePoint Online หรือส่งอีเมลผ่าน Office 365 Outlook ได้

:::image type="content" source="media/service-automate-paginated-excel-sharepoint-list/excel-template-overview.png" alt-text="ส่งออกรายงานที่มีการแบ่งหน้าโดยใช้ตาราง Excel Online":::

แต่ละแถวในตาราง Excel Online หรือรายการ SharePoint Online สามารถเป็นตัวแทนของผู้ใช้รายเดียวเพื่อรับรายงานที่มีการแบ่งหน้าตามการสมัครใช้งานได้ หรือไม่เช่นนั้นก็แต่ละแถวสามารถเป็นตัวแทนของรายงานที่มีการแบ่งหน้าที่ไม่ซ้ำกันซึ่งคุณต้องการแจกจ่ายได้ ตารางหรือรายการของคุณต้องการคอลัมน์ที่ระบุวิธีการแจกจ่ายรายงาน ไม่ว่าจะเป็น OneDrive, SharePoint Online หรือ Outlook โฟลว์ Power Automate ใช้คอลัมน์นี้ในคำสั่ง Switch

คุณกำลังมองหาเทมเพลต Power Automate อื่น ๆ สำหรับรายงานที่มีการแบ่งหน้า Power BI ใช่หรือไม่ โปรดดู[ส่งออกรายงานที่มีการแบ่งหน้า Power BI ด้วย Power Automate](service-automate-paginated-integration.md)

## <a name="prerequisites"></a>สิ่งที่จำเป็นต้องมี  

เพื่อดำเนินการต่อไป คุณควรตรวจสอบให้แน่ใจว่าคุณมีรายการต่อไปนี้:

- พื้นที่ทำงานในผู้เช่า Power BI ของคุณที่ได้รับการสนับสนุนจากความจุที่สงวนไว้อย่างน้อยหนึ่งรายการ ความจุนี้สามารถเป็น SKU ใดก็ได้ตั้งแต่ A4/P1 – A6/P3 อ่านข้อมูลเพิ่มเติมเกี่ยวกับ[ความจุสำรองสำหรับรายงานที่มีการแบ่งหน้าใน Power BI Premium](../admin/service-premium-what-is.md#paginated-reports)
- เข้าถึงตัวเชื่อมต่อมาตรฐานใน Power Automate ซึ่งมาพร้อมกับการสมัครใช้งาน Office 365
- ถ้าคุณกำลังใช้ตาราง Excel Online คุณจำเป็นต้องจัดรูปแบบให้เป็นตารางใน Excel ดู[สร้างตาราง](https://support.microsoft.com/office/create-a-table-in-excel-bf0ce08b-d012-42ec-8ecf-a2259c9faf3f)เพื่อเรียนรู้วิธีการ

## <a name="export-a-paginated-report-for-each-row-in-a-table-or-list"></a>ส่งออกรายงานที่มีการแบ่งหน้าสำหรับแต่ละแถวในตารางหรือรายการ

> [!NOTE]
> ขั้นตอนและรูปภาพต่อไปนี้แสดงการตั้งค่าโฟลว์โดยใช้เทมเพลต **ส่งออกรายงานที่มีการแบ่งหน้า Power BI สำหรับแต่ละแถวในตาราง Excel Online** คุณสามารถทำตามขั้นตอนเดียวกันนี้เพื่อสร้างโฟลว์โดยใช้เทมเพลต **ส่งออกรายงานที่มีการแบ่งหน้า Power BI สำหรับหน่วยข้อมูลในรายการ SharePoint Online** แทนที่จะเป็นตาราง Excel Online รายการ SharePoint Online จะมีข้อมูลเกี่ยวกับวิธีการส่งออกรายงานที่มีการแบ่งหน้า  

1. ลงชื่อเข้าใช้ Power Automate [flow.microsoft.com](https://flow.microsoft.com/) 
1. เลือก **เทมเพลต** และค้นหา  **รายงานที่มีการแบ่งหน้า** 

    :::image type="content" source="media/service-automate-paginated-integration/power-bi-paginate-automate.png" alt-text="สกรีนช็อตของเทมเพลต Power Automate อื่น ๆ สำหรับรายงานที่มีการแบ่งหน้า Power BI":::

1. เลือกเทมเพลต **ส่งออกรายงานที่มีการแบ่งหน้า Power BI สำหรับแต่ละแถวในตาราง Excel Online** หรือ **ส่งออกรายงานที่มีการแบ่งหน้า Power BI สำหรับหน่วยข้อมูลในรายการ SharePoint Online** ตรวจสอบให้แน่ใจว่าคุณได้ลงชื่อเข้าใช้ Excel Online, Power BI, OneDrive for Business, SharePoint Online และ Office 365 Outlook เรียบร้อยแล้ว เลือก **ดำเนินต่อ**  

   :::image type="content" source="media/service-automate-paginated-excel-sharepoint-list/excel-template-excel-online-1.png" alt-text="ส่งออกรายงานที่มีการแบ่งหน้า Power BI สำหรับแต่ละแถวในตาราง Excel Online":::

1. เมื่อต้องการตั้งค่า **การเกิดซ้ำ** สำหรับโฟลว์ของคุณ ให้เลือกตัวเลือกใน **ความถี่** และป้อนค่า **ช่วงเวลา** ที่ต้องการ

    :::image type="content" source="media/service-automate-paginated-excel-sharepoint-list/excel-template-recurrence-2.png" alt-text="เลือกการเกิดซ้ำสำหรับโฟลว์ของคุณ":::

1. (ไม่บังคับ) เลือก **แสดงตัวเลือกขั้นสูง** เพื่อตั้งค่าพารามิเตอร์ **การเกิดซ้ำ** เพิ่มเติม รวมถึง **เขตเวลา** **เวลาเริ่มต้น** **ในเหล่าวันนี้** **ในชั่วโมงเหล่านี้** และ **ในนาทีเหล่านี้**

    :::image type="content" source="media/service-automate-paginated-excel-sharepoint-list/excel-template-advanced-recurrence-3.png" alt-text="ไม่บังคับ เลือกตัวเลือกการเกิดซ้ำขั้นสูง":::

1. ในกล่อง **ตำแหน่ง** ให้เลือก OneDrive for Business หรือไซต์ SharePoint Online ที่บันทึกตาราง Excel Online หรือรายการ SharePoint Online ของคุณ จากนั้นเลือก **ไลบรารีเอกสาร** จากเมนูแบบดรอปดาวน์

    :::image type="content" source="media/service-automate-paginated-excel-sharepoint-list/excel-template-location-4.png" alt-text="เลือกตำแหน่งของตาราง Excel Online":::

1. เลือกไฟล์ Excel Online หรือรายการ SharePoint Online ในกล่อง **ไฟล์** เลือกชื่อของตารางหรือรายการจากเมนูแบบดรอปดาวน์ในช่อง **ตาราง** 
 
    :::image type="content" source="media/service-automate-paginated-excel-sharepoint-list/excel-template-file-table-5.png" alt-text="เลือกไฟล์ Excel Online และชื่อของตาราง":::

    > [!TIP]
    > ดู[สร้างตาราง](https://support.microsoft.com/office/create-a-table-in-excel-bf0ce08b-d012-42ec-8ecf-a2259c9faf3f)เพื่อเรียนรู้วิธีจัดรูปแบบข้อมูลเป็นตารางใน Excel 

1. เตรียมใช้งานตัวแปรที่จะใช้สำหรับชื่อไฟล์ คุณสามารถเก็บหรือแก้ไขค่าเริ่มต้นสำหรับ **ชื่อ** และ **ค่า** ได้ แต่ปล่อยให้ **ชนิด** เท่ากับ **สตริง**  

    :::image type="content" source="media/service-automate-paginated-excel-sharepoint-list/excel-template-name-type-6.png" alt-text="กรอกชื่อและค่า และให้ชนิดเท่ากับสตริง":::

1. ใน **นำไปใช้กับแต่ละรายการ** กล่อง **เลือกผลลัพธ์จากขั้นตอนก่อนหน้า** ถูกตั้งค่าเป็น **ค่า** ตามค่าเริ่มต้น การตั้งค่านี้จะวนซ้ำผ่านการดำเนินการที่อยู่ใน **นำไปใช้กับแต่ละรายการ** สำหรับแต่ละแถวในตาราง Excel Online หรือรายการ SharePoint Online ของคุณ  

1. ในกล่อง **พื้นที่ทำงาน** ให้เลือกพื้นที่ทำงานในความจุที่สงวนไว้ ในกล่อง **รายงาน** ให้เลือกรายงานที่มีการแบ่งหน้าในพื้นที่ทำงานที่คุณต้องการส่งออก ถ้าคุณตั้งค่า **ป้อนค่าที่กำหนดเอง** จากเมนูแบบดรอปดาวน์ คุณสามารถตั้งค่า **พื้นที่ทำงาน** และ **รายงาน** ให้เท่ากับคอลัมน์ในตาราง Excel Online หรือรายการ SharePoint Online ของคุณ คอลัมน์เหล่านี้ควรมี ID พื้นที่ทำงานและ ID รายงานตามลำดับ  

1. เลือก **รูปแบบการส่งออก** จากเมนูแบบดรอปดาวน์ หรือกำหนดให้เท่ากับคอลัมน์ในตาราง Excel Online ของคุณที่มีรูปแบบการส่งออกที่ต้องการ ตัวอย่างเช่น PDF, DOCX หรือ PPTX อีกทางหนึ่งคือคุณสามารถระบุพารามิเตอร์สำหรับรายงานที่มีการแบ่งหน้าได้ ค้นหาคำอธิบายโดยละเอียดของพารามิเตอร์ใน[การอ้างอิงตัวเชื่อมต่อสำหรับ Power BI REST API](/connectors/powerbi/#export-to-file-for-paginated-reports)

    :::image type="content" source="media/service-automate-paginated-excel-sharepoint-list/excel-template-export-format-9.png" alt-text="กรอกข้อมูลการส่งออกรายงานที่มีการแบ่งหน้าไปยังไฟล์":::

1. ในกล่อง **ค่า** ให้ป้อนชื่อสำหรับรายงานที่มีการแบ่งหน้าเมื่อส่งออก อย่าลืมป้อนนามสกุลไฟล์ คุณสามารถตั้งค่าแบบคงที่ได้ ตัวอย่างเช่น .pdf, .docx หรือ .pptx หรือตั้งค่าแบบไดนามิกโดยการเลือกคอลัมน์ในตาราง Excel ของคุณที่ตรงกับรูปแบบการส่งออกที่คุณต้องการ 

    :::image type="content" source="media/service-automate-paginated-excel-sharepoint-list/excel-template-output-value-10.png" alt-text="เลือกชื่อของรายงานและนามสกุลไฟล์":::

1. ในการดำเนินการ **สลับ** ให้เติมกล่อง **เปิด** ด้วยคอลัมน์ในตาราง Excel Online ของคุณที่ตรงกับวิธีการนำส่งที่ต้องการ: **OneDrive**, **SharePoint** หรือ **อีเมล** 

    :::image type="content" source="media/service-automate-paginated-excel-sharepoint-list/excel-template-switch-11.png" alt-text="ในการดำเนินการสลับ ให้เติมกล่องเปิดด้วยคอลัมน์ในตาราง Excel Online ของคุณ":::

1. ใน **กรณี** **กรณี 2** และ **กรณี 3** ให้ป้อนค่าที่มีอยู่ในคอลัมน์ตาราง Excel Online ที่เลือกในขั้นตอนก่อนหน้า  

    :::image type="content" source="media/service-automate-paginated-excel-sharepoint-list/excel-template-case-1-2-3-12.png" alt-text="ป้อนค่าสำหรับกรณี กรณี 2 และกรณี 3":::

1. ในกรณีที่คุณกำลังบันทึกรายงานที่มีการแบ่งหน้าไปยัง OneDrive ให้เลือก **เส้นทางโฟลเดอร์** ที่ควรบันทึก  

    :::image type="content" source="media/service-automate-paginated-excel-sharepoint-list/excel-template-case-onedrive-13.png" alt-text="ในกรณีที่คุณกำลังบันทึกลงใน OneDrive":::

1. ในกรณีที่คุณกำลังบันทึกรายงานที่มีการแบ่งหน้าไปยัง SharePoint Online ให้ป้อน **ที่อยู่ไซต์** และ **เส้นทางโฟลเดอร์** ที่ควรบันทึก 

    :::image type="content" source="media/service-automate-paginated-excel-sharepoint-list/excel-template-case-sharepoint-14.png" alt-text="ในกรณีที่คุณกำลังบันทึกรายงานที่มีการแบ่งหน้าของคุณไปยัง SharePoint Online":::

1. ในกรณีที่คุณกำลังส่งรายงานที่มีการแบ่งหน้าของคุณเป็นอีเมลผ่าน Outlook ให้ใส่ข้อมูลในกล่อง **ถึง** **เรื่อง** และ **เนื้อหา** กล่องเหล่านี้สามารถมีเนื้อหาคงที่ หรือเนื้อหาแบบไดนามิกจากตาราง Excel Online หรือรายการ SharePoint Online ได้ Power Automate แนบรายงานที่มีการแบ่งหน้าของคุณกับอีเมลนี้โดยอัตโนมัติ  

    :::image type="content" source="media/service-automate-paginated-excel-sharepoint-list/excel-template-case-email-15.png" alt-text="ในกรณีที่คุณกำลังส่งรายงานที่มีการแบ่งหน้าของคุณเป็นอีเมลผ่าน Outlook":::

1. เมื่อคุณดำเนินการเสร็จแล้ว ให้เลือก  **ขั้นตอนถัดไป** หรือ **บันทึก** Power Automate สร้างและประเมินโฟลว์ และแจ้งให้คุณทราบว่าพบข้อผิดพลาดหรือไม่ 

1. ถ้ามีข้อผิดพลาด ให้เลือก **แก้ไขโฟลว์** เพื่อแก้ไขโฟลว์เหล่านั้น มิฉะนั้น ให้เลือกลูกศร **ย้อนกลับ** เพื่อดูรายละเอียดโฟลว์และเรียกใช้โฟลว์ใหม่ 


## <a name="next-steps"></a>ขั้นตอนถัดไป

- [ส่งออกรายงานที่มีการแบ่งหน้า Power BI ด้วย Power Automate](service-automate-paginated-integration.md)
- [เริ่มต้นใช้งาน Power Automate](/power-automate/getting-started/)
- มีคำถามเพิ่มเติมหรือไม่ [ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)

