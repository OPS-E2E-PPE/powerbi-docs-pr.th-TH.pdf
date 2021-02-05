---
title: บันทึกรายงานที่มีการแบ่งหน้าไปยังโฟลเดอร์ภายในเครื่องด้วย Power Automate
description: ในบทความนี้ คุณจะใช้เทมเพลตเพื่อตั้งค่าการส่งออกที่เกิดซ้ำของรายงานที่มีการแบ่งหน้าไปยังระบบไฟล์ของคุณในรูปแบบที่ต้องการ
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 12/08/2020
LocalizationGroup: Get started
ms.openlocfilehash: a30f0df972c375af4fb284ce3bba5372870d6efb
ms.sourcegitcommit: bbf7e9341a4e1cc96c969e24318c8605440282a5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/11/2020
ms.locfileid: "97098816"
---
# <a name="save-a-power-bi-paginated-report-to-a-local-folder--with-power-automate"></a>บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยังโฟลเดอร์ภายในเครื่องด้วย Power Automate

ด้วย [Power Automate](/power-automate/getting-started) คุณสามารถทำให้การส่งออกและการแจกจ่ายรายงานที่มีการแบ่งหน้า Power BI ไปยังรูปแบบและสถานการณ์ที่ได้รับการสนับสนุนเป็นแบบอัตโนมัติ ในบทความนี้ คุณจะใช้เทมเพลตเพื่อตั้งค่าการส่งออกที่เกิดซ้ำของรายงานที่มีการแบ่งหน้าไปยังระบบไฟล์ของคุณในรูปแบบที่ต้องการ ดูข้อกำหนดเบื้องต้นหากคุณใช้งานการดำเนินการส่งออกรายงานที่มีการแบ่งหน้าไปยังไฟล์ในโฟลว์ Power Automate เป็นครั้งแรก

:::image type="content" source="media/service-automate-paginated-local-file/paginated-local-file-overview.png" alt-text="ตั้งค่าการส่งออกที่เกิดซ้ำของรายงานที่มีการแบ่งหน้า":::

คุณกำลังมองหาเทมเพลต Power Automate อื่น ๆ สำหรับรายงานที่มีการแบ่งหน้า Power BI ใช่หรือไม่ โปรดดู[ส่งออกรายงานที่มีการแบ่งหน้า Power BI ด้วย Power Automate](service-automate-paginated-integration.md)

## <a name="prerequisites"></a>สิ่งที่จำเป็นต้องมี  

เพื่อดำเนินการต่อไป คุณควรตรวจสอบให้แน่ใจว่าคุณมีรายการต่อไปนี้:

- พื้นที่ทำงานในผู้เช่า Power BI ของคุณที่ได้รับการสนับสนุนจากความจุที่สงวนไว้อย่างน้อยหนึ่งรายการ ความจุนี้สามารถเป็น SKU ใดก็ได้ตั้งแต่ A4/P1 – A6/P3 อ่านข้อมูลเพิ่มเติมเกี่ยวกับ[ความจุสำรองสำหรับรายงานที่มีการแบ่งหน้าใน Power BI Premium](../admin/service-premium-what-is.md#paginated-reports)
- เข้าถึงตัวเชื่อมต่อมาตรฐานใน Power Automate ซึ่งมาพร้อมกับการสมัครใช้งาน Office 365

## <a name="save-a-power-bi-paginated-report-to-a-local-folder"></a>บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยังโฟลเดอร์ภายในเครื่อง

1. เลือก **บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยังเทมเพลตระบบไฟล์ภายในเครื่อง** ตรวจสอบให้แน่ใจว่าคุณได้ลงชื่อเข้าใช้ Power BI และเชื่อมต่อกับระบบไฟล์ภายในเครื่องของคุณ เลือก **ดำเนินต่อ** 

    :::image type="content" source="media/service-automate-paginated-local-file/paginated-local-file-save-report-local-file-1.png" alt-text="บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยังระบบไฟล์ภายในเครื่อง":::

2. คุณอาจจำเป็นต้องเลือก **เพิ่มการเชื่อมต่อใหม่** เพื่อเชื่อมต่อกับระบบไฟล์ของคุณ 
1. ใส่ **ชื่อการเชื่อมต่อ** เส้นทางไปยัง **โฟลเดอร์ราก** ที่คุณต้องการ และรับรองความถูกต้องโดยใส่ **ชื่อผู้ใช้** และ **รหัสผ่าน** ของคุณ เลือก **เกตเวย์** จากรายการดรอปดาวน์หากคุณกำลังใช้เกตเวย์ข้อมูลภายในองค์กร

    :::image type="content" source="media/service-automate-paginated-local-file/paginated-local-file-set-file-system-2.png" alt-text="ใส่ชื่อการเชื่อมต่อและโฟลเดอร์ราก":::
 
3. เมื่อต้องการตั้งค่าความถี่ **การเกิดขึ้นประจำ** สำหรับโฟลว์ของคุณ ให้เลือกตัวเลือกจากรายการดรอปดาวน์ **ความถี่** และใส่ค่า **ช่วง** ที่ต้องการ  

    :::image type="content" source="media/service-automate-paginated-local-file/paginated-local-file-recurrence-frequency-3.png" alt-text="ตั้งค่าความถี่การเกิดขึ้นประจำสำหรับโฟลว์ของคุณ":::

4. หรือเลือก **แสดงตัวเลือกขั้นสูง** ตั้งค่าพารามิเตอร์ **การเกิดขึ้นประจำ** เพิ่มเติม เช่น **โซนเวลา** **เวลาเริ่มต้น** **ในวันนี้** **ในชั่วโมงนี้** และ **ในนาทีนี้** 
 
    :::image type="content" source="media/service-automate-paginated-local-file/paginated-local-file-recurrence-advanced-4.png" alt-text="ตั้งค่าตัวเลือกขั้นสูงสำหรับการเกิดขึ้นประจำ":::

5. ในกล่อง **พื้นที่ทำงาน** ให้เลือกพื้นที่ทำงานในความจุสำรองที่มีรายงานอยู่ ในกล่อง **รายงาน** ให้เลือกรายงานที่มีการแบ่งหน้าที่คุณต้องการส่งออกในพื้นที่ทำงาน ในกล่อง **รูปแบบการส่งออก** ให้เลือกรูปแบบการส่งออกที่ต้องการ อีกทางหนึ่งคือคุณสามารถระบุพารามิเตอร์สำหรับรายงานที่มีการแบ่งหน้าได้ ดูคำอธิบายโดยละเอียดเกี่ยวกับพารามิเตอร์ใน[การอ้างอิงตัวเชื่อมต่อสำหรับ Power BI REST API](/connectors/powerbi/#export-to-file-for-paginated-reports)  
 
    :::image type="content" source="media/service-automate-paginated-local-file/paginated-local-file-select-workspace-report-5.png" alt-text="เลือกพื้นที่ทำงานและรายงาน":::

6. ในกล่องโต้ตอบ **สร้างไฟล์** ใน **เส้นทางโฟลเดอร์** ให้เลือกโฟลเดอร์ที่คุณต้องการส่งออกรายงานที่มีการแบ่งหน้าของคุณ
 
    :::image type="content" source="media/service-automate-paginated-local-file/paginated-local-file-create-file-6.png" alt-text="เลือกโฟลเดอร์ที่คุณต้องการส่งออกรายงานที่มีการแบ่งหน้าของคุณ":::

7. Power Automate จะสร้าง **ชื่อไฟล์** และ **เนื้อหาไฟล์** ให้กับคุณโดยอัตโนมัติ คุณสามารถปรับเปลี่ยน **ชื่อไฟล์** แต่คงค่า **เนื้อหาไฟล์** ที่สร้างขึ้นแบบไดนามิกได้
8. เมื่อเสร็จสิ้นแล้ว ให้เลือก **ขั้นตอนถัดไป** หรือ **บันทึก** Power Automate จะสร้างและประเมินโฟลว์
9. หาก Power Automate พบข้อผิดพลาด ให้เลือก **แก้ไขโฟลว์** เพื่อแก้ไขข้อผิดพลาดดังกล่าว อีกทางหนึ่งคือ เลือกลูกศรย้อนกลับเพื่อดูรายละเอียดโฟลว์ และเรียกใช้โฟลว์ใหม่
10. เมื่อคุณเรียกใช้โฟลว์ Power Automate จะส่งออกรายงานที่มีการแบ่งหน้าในรูปแบบที่ระบุไว้ไปยังโฟลเดอร์ที่เลือกในระบบไฟล์ของคุณ

    :::image type="content" source="media/service-automate-paginated-local-file/paginated-local-file-exported-10.png" alt-text="Power Automate จะส่งออกรายงานที่มีการแบ่งหน้าในรูปแบบที่ระบุไว้":::

## <a name="next-steps"></a>ขั้นตอนถัดไป

- [ส่งออกรายงานที่มีการแบ่งหน้า Power BI ด้วย Power Automate](service-automate-paginated-integration.md)
- [เริ่มต้นใช้งาน Power Automate](/power-automate/getting-started/)
- มีคำถามเพิ่มเติมหรือไม่ [ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)

