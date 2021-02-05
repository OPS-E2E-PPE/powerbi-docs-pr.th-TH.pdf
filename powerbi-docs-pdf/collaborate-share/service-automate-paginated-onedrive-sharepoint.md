---
title: บันทึกรายงานที่มีการแบบแบ่งหน้าไปยัง OneDrive for Business หรือ SharePoint Online
description: ในบทความนี้คุณสามารถใช้ Power Automate เพื่อทำให้การบันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยัง OneDrive for Business หรือโฟลเดอร์ SharePoint Online เป็นแบบอัตโนมัติ
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 11/17/2020
LocalizationGroup: Get started
ms.openlocfilehash: 6aaad48fb3e97aa6c1b4fc51834ee593a49a8192
ms.sourcegitcommit: bbf7e9341a4e1cc96c969e24318c8605440282a5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/11/2020
ms.locfileid: "97097742"
---
# <a name="save-a-paginated-report-to-onedrive-for-business-or-sharepoint-online"></a>บันทึกรายงานที่มีการแบบแบ่งหน้าไปยัง OneDrive for Business หรือ SharePoint Online

ด้วย [Power Automate](/power-automate/getting-started) คุณสามารถทำให้การส่งออกและการแจกจ่ายรายงานที่มีการแบ่งหน้า Power BI ไปยังรูปแบบและสถานการณ์ที่ได้รับการสนับสนุนเป็นแบบอัตโนมัติ ในบทความนี้คุณสามารถใช้ Power Automate เพื่อทำให้การบันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยัง OneDrive for Business หรือโฟลเดอร์ SharePoint Online เป็นแบบอัตโนมัติ


:::image type="content" source="media/service-automate-paginated-onedrive-sharepoint/paginated-onedrive-flow.png" alt-text="สกรีนช็อตของโฟลว์ Power Automate สำหรับการบันทึกรายงานที่มีการแบ่งหน้าไปยัง OneDrive หรือ SharePoint Online":::

คุณกำลังมองหาเทมเพลต Power Automate อื่น ๆ สำหรับรายงานที่มีการแบ่งหน้า Power BI ใช่หรือไม่ โปรดดู[ส่งออกรายงานที่มีการแบ่งหน้า Power BI ด้วย Power Automate](service-automate-paginated-integration.md) 

## <a name="prerequisites"></a>สิ่งที่จำเป็นต้องมี  

เพื่อดำเนินการต่อไป คุณควรตรวจสอบให้แน่ใจว่าคุณมีรายการต่อไปนี้:

- พื้นที่ทำงานในผู้เช่า Power BI ของคุณที่ได้รับการสนับสนุนจากความจุที่สงวนไว้อย่างน้อยหนึ่งรายการ ความจุนี้สามารถเป็น SKU ใดก็ได้ตั้งแต่ A4/P1 – A6/P3 อ่านข้อมูลเพิ่มเติมเกี่ยวกับ[ความจุสำรองสำหรับรายงานที่มีการแบ่งหน้าใน Power BI Premium](../admin/service-premium-what-is.md#paginated-reports)
- เข้าถึงตัวเชื่อมต่อมาตรฐานใน Power Automate ซึ่งมาพร้อมกับการสมัครใช้งาน Office 365

## <a name="save-a-paginated-report-to-onedrive-for-business-or-a-sharepoint-online-folder"></a>บันทึกรายงานที่มีการแบบแบ่งหน้าไปยัง OneDrive for Business หรือโฟลเดอร์ SharePoint Online 

คุณสามารถตั้งค่าการส่งออกรายงานที่มีการแบ่งหน้าที่เกิดขึ้นประจำในรูปแบบที่ต้องการไปยัง OneDrive for Business หรือโฟลเดอร์ SharePoint Online ได้ด้วยหนึ่งในเทมเพลตเหล่านี้ ดูข้อกำหนดเบื้องต้นถ้าคุณใช้งานการดำเนินการส่งออกรายงานที่มีการแบ่งหน้าไปยังไฟล์ในโฟลว์ Power Automate เป็นครั้งแรก 

> [!NOTE]
> ขั้นตอนและรูปภาพต่อไปนี้แสดงการตั้งค่าโฟลว์โดยใช้เทมเพลต **บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยัง OneDrive for Business** ทำตามขั้นตอนเดียวกันนี้เพื่อสร้างโฟลว์โดยใช้เทมเพลต **บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยังโฟลเดอร์ SharePoint Online** เมื่อเลือกตำแหน่งที่คุณต้องการส่งออกรายงานที่มีการแบ่งหน้าของคุณ ให้เลือกโฟลเดอร์ SharePoint Online แทนที่จะเป็นโฟลเดอร์ OneDrive for Business 

1. ลงชื่อเข้าใช้ Power Automate [flow.microsoft.com](https://flow.microsoft.com/) 
1. เลือก **เทมเพลต** และค้นหา  **รายงานที่มีการแบ่งหน้า** 

    :::image type="content" source="media/service-automate-paginated-integration/power-bi-paginate-automate.png" alt-text="สกรีนช็อตของเทมเพลต Power Automate อื่น ๆ สำหรับรายงานที่มีการแบ่งหน้า Power BI":::

1. เลือก **บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยัง OneDrive for Business** หรือ **บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยังโฟลเดอร์ SharePoint Online** ตรวจสอบให้แน่ใจว่าคุณได้ลงชื่อเข้าใช้ Power BI และ OneDrive for Business หรือ SharePoint Online แล้ว

    :::image type="content" source="media/service-automate-paginated-onedrive-sharepoint/onedrive-template-step1.png" alt-text="สกรีนช็อตของการเลือกเทมเพลต Power BI และ OneDrive for Business":::
1. เลือก **ดำเนินต่อ**  


1. เมื่อต้องการตั้งค่า **การเกิดซ้ำ** สำหรับโฟลว์ของคุณ ให้เลือกตัวเลือกใน **ความถี่** และป้อนค่า **ช่วงเวลา** ที่ต้องการ

    :::image type="content" source="media/service-automate-paginated-onedrive-sharepoint/onedrive-template-2-recurrence.png" alt-text="การเลือกการเกิดซ้ำสำหรับโฟลว์":::

1. (ไม่บังคับ) เลือก **แสดงตัวเลือกขั้นสูง** เพื่อตั้งค่าพารามิเตอร์ **การเกิดซ้ำ** เพิ่มเติม รวมถึง **เขตเวลา** **เวลาเริ่มต้น** **ในเหล่าวันนี้** **ในชั่วโมงเหล่านี้** และ **ในนาทีเหล่านี้**  

    :::image type="content" source="media/service-automate-paginated-onedrive-sharepoint/onedrive-template-3-advanced-recurrence.png" alt-text="แสดงตัวเลือกขั้นสูงสำหรับการเกิดซ้ำ":::

1. ในกล่อง **พื้นที่ทำงาน** ให้เลือกพื้นที่ทำงานในความจุที่สงวนไว้ ในกล่อง **รายงาน** ให้เลือกรายงานที่มีการแบ่งหน้าในพื้นที่ทำงานที่คุณต้องการส่งออก ในกล่อง **รูปแบบการส่งออก** ให้เลือกรูปแบบการส่งออกที่ต้องการ อีกทางหนึ่งคือคุณสามารถระบุพารามิเตอร์สำหรับรายงานที่มีการแบ่งหน้าได้ ค้นหาคำอธิบายโดยละเอียดของพารามิเตอร์ใน[การอ้างอิงตัวเชื่อมต่อสำหรับ Power BI REST API](/connectors/powerbi/#export-to-file-for-paginated-reports)  

    :::image type="content" source="media/service-automate-paginated-onedrive-sharepoint/onedrive-template-4-export-format.png" alt-text="เลือกรายงานที่มีการแบ่งหน้า พื้นที่ทำงาน และรูปแบบการส่งออก":::

1. ใน **เส้นทางโฟลเดอร์** ให้เลือกโฟลเดอร์ OneDrive for Business หรือ SharePoint Online ที่คุณต้องการส่งออกรายงานที่มีการแบ่งหน้าของคุณ

    :::image type="content" source="media/service-automate-paginated-onedrive-sharepoint/onedrive-template-5-create-file.png" alt-text="เลือกปลายทางและสร้างไฟล์":::

1. Power Automate จะสร้าง **ชื่อไฟล์** และ **เนื้อหาไฟล์** ให้คุณโดยอัตโนมัติ คุณสามารถเปลี่ยนชื่อไฟล์ได้ แต่คงค่า **เนื้อหาไฟล์** ที่สร้างขึ้นแบบไดนามิก 

1. เมื่อคุณดำเนินการเสร็จแล้ว ให้เลือก  **ขั้นตอนถัดไป** หรือ **บันทึก** Power Automate สร้างและประเมินโฟลว์ และแจ้งให้คุณทราบว่าพบข้อผิดพลาดหรือไม่ 

1. ถ้ามีข้อผิดพลาด ให้เลือก **แก้ไขโฟลว์** เพื่อแก้ไขโฟลว์เหล่านั้น มิฉะนั้น ให้เลือกลูกศร **ย้อนกลับ** เพื่อดูรายละเอียดโฟลว์และเรียกใช้โฟลว์ใหม่ 

    เมื่อคุณเรียกใช้โฟลว์ Power Automate จะส่งออกรายงานที่มีการแบ่งหน้าในรูปแบบที่ระบุไปยัง OneDrive for Business หรือ SharePoint Online  

## <a name="next-steps"></a>ขั้นตอนถัดไป

- [ส่งออกรายงานที่มีการแบ่งหน้า Power BI ด้วย Power Automate](service-automate-paginated-integration.md)
- [เริ่มต้นใช้งาน Power Automate](/power-automate/getting-started/)
- มีคำถามเพิ่มเติมหรือไม่ [ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)
