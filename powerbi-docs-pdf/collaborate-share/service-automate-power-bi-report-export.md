---
title: ส่งออกและส่งรายงานทางอีเมลด้วย Power Automate
description: ในบทความนี้ คุณจะใช้ Power Automate เพื่อปรับให้การส่งออกและการแจกจ่ายรายงาน Power BI เป็นไปโดยอัตโนมัติในรูปแบบและสถานการณ์ต่างๆ ที่รองรับ
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 12/10/2020
LocalizationGroup: Get started
ms.openlocfilehash: 45bccbefc6e499375d33aa049ead8a6c6e47bc8c
ms.sourcegitcommit: bbf7e9341a4e1cc96c969e24318c8605440282a5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/11/2020
ms.locfileid: "97098837"
---
# <a name="export-and-email-a-power-bi-report-with-power-automate"></a>ส่งออกและส่งรายงาน Power BI ทางอีเมลด้วย Power Automate

ด้วย [Power Automate](/power-automate/getting-started) คุณสามารถปรับให้การส่งออกและการกระจายรายงาน Power BI เป็นไปโดยอัตโนมัติตามรูปแบบและสถานการณ์ต่างๆ ในบทความนี้ คุณจะสร้างโฟลว์ของคุณเองตั้งแต่ต้น คุณจะใช้การดำเนินการส่งออกไปยังไฟล์สำหรับรายงาน Power BI เพื่อแจกจ่ายรายงาน Power BI ทางอีเมลโดยอัตโนมัติ

:::image type="content" source="media/service-automate-power-bi-report-export/automate-power-bi-report-overview.png" alt-text="ขั้นตอนการส่งออกและการส่งรายงานทางอีเมลของ Power Automate":::

## <a name="prerequisites"></a>สิ่งที่จำเป็นต้องมี  

เพื่อดำเนินการต่อไป คุณควรตรวจสอบให้แน่ใจว่าคุณมีรายการต่อไปนี้:

- พื้นที่ทำงานในผู้เช่า Power BI ของคุณที่ได้รับการสนับสนุนจากความจุที่สงวนไว้อย่างน้อยหนึ่งรายการ ความจุนี้อาจเป็น A1/EM1 - A6/P3 SKUs อ่านเพิ่มเติมเกี่ยวกับ[ความจุที่สงวนไว้ใน Power BI Premium](../admin/service-premium-what-is.md)
- เข้าถึงตัวเชื่อมต่อมาตรฐานใน Power Automate ซึ่งมาพร้อมกับการสมัครใช้งาน Office 365

## <a name="create-a-flow-from-scratch"></a>สร้างโฟลว์ตั้งแต่เริ่มต้น 

ในงานนี้ คุณจะสร้างโฟลว์ง่ายๆ ตั้งแต่ต้น โฟลว์จะส่งออกรายงาน Power BI เป็น PDF และจะแนบไปกับอีเมลที่จะส่งเป็นรายสัปดาห์  

1. ลงชื่อเข้าใช้ Power Automate (flow.microsoft.com)
2. เลือก **สร้าง** > **โฟลว์ที่จัดกำหนดการ** 

    :::image type="content" source="media/service-automate-power-bi-report-export/automate-report-scheduled-flow-2.png" alt-text="สร้างโฟลว์ที่จัดกำหนดการใน Power Automate":::

3. ใน **สร้างโฟลว์ที่จัดกำหนดการ** ให้ตั้งชื่อโฟลว์ของคุณ 
4. ใน **เรียกใช้โฟลว์นี้** ให้เลือกวันที่และเวลาเริ่มต้นสำหรับโฟลว์ของคุณ รวมถึงความถี่การเกิดขึ้นประจำ
5. ใน **ในวันนี้** ให้เลือกวันที่ที่คุณต้องการให้โฟลว์ของคุณถูกเรียกใช้ แล้วเลือก **สร้าง**

    :::image type="content" source="media/service-automate-power-bi-report-export/automate-report-build-flow-5.png" alt-text="Power Automate จัดกำหนดการโฟลว์":::

6. ใน **การเกิดขึ้นประจำ** ให้เลือก **แสดงตัวเลือกขั้นสูง** และใส่ค่าใน **ในชั่วโมงนี้** และ **ในนาทีนี้** เพื่อกำหนดเวลาที่เฉพาะเจาะจงสำหรับโฟลว์ของคุณที่จะถูกเรียกใช้
 
    :::image type="content" source="media/service-automate-power-bi-report-export/automate-report-recurrence-6.png" alt-text="ตั้งค่าการเกิดขึ้นประจำใน Power Automate":::

7. เลือก **ขั้นตอนใหม่**
8. ใน **เลือกการดำเนินการ** ให้ค้นหา **Power BI** แล้วเลือก **ส่งออกไปยังไฟล์สำหรับรายงาน Power BI**
 
    :::image type="content" source="media/service-automate-power-bi-report-export/automate-report-choose-action-8.png" alt-text="เลือกการดำเนินการใน Power Automate":::

9. ใน **ส่งออกไปยังไฟล์สำหรับรายงาน Power BI** ให้เลือก **พื้นที่ทำงาน** และ **รายงาน** จากรายการดรอปดาวน์
10. เลือก **รูปแบบการส่งออก** ที่ต้องการสำหรับรายงาน Power BI ของคุณ
 
    :::image type="content" source="media/service-automate-power-bi-report-export/automate-report-export-file-10.png" alt-text="เลือกรูปแบบการส่งออกใน Power Automate":::

11. หรือระบุหน้าเฉพาะที่จะส่งออกในเขตข้อมูล **Pages pageName -1** โปรดทราบว่าพารามิเตอร์ชื่อหน้าจะแตกต่างจากชื่อหน้าที่แสดง ค้นหาชื่อหน้าโดยการนำทางไปยังหน้าในบริการ Power BI และคัดลอกส่วนสุดท้ายของ URL
 
     :::image type="content" source="media/service-automate-power-bi-report-export/automate-report-copy-url-11.png" alt-text="เลือกชื่อบานหน้าต่างใน U R L":::

12. หรือระบุบุ๊กมาร์กเฉพาะที่จะแสดงในเขตข้อมูล **Pages Bookmark Name** เช่นเดียวกับพารามิเตอร์ชื่อหน้า คุณจะพบพารามิเตอร์ชื่อบุ๊กมาร์กใน URL รายงาน คุณสามารถระบุพารามิเตอร์เพิ่มเติมสำหรับรายงาน Power BI ได้ ค้นหาคำอธิบายโดยละเอียดเกี่ยวกับพารามิเตอร์เหล่านี้ใน[การอ้างอิงตัวเชื่อมต่อสำหรับ Power BI REST API](/connectors/powerbi/#export-to-file-for-power-bi-reports)

    :::image type="content" source="media/service-automate-power-bi-report-export/automate-report-bookmark-url-12.png" alt-text="เลือกชื่อบุ๊กมาร์กใน U R L":::

13. เลือก **ขั้นตอนใหม่**
14. ใน **เลือกการดำเนินการ** ให้ค้นหา **Outlook** แล้วเลือก **ส่งอีเมล (V2)**
15. ใน **ส่งอีเมล (V2)** ให้กรอกเขตข้อมูล **ถึง** **ชื่อเรื่อง** และ **เนื้อหา** สำหรับอีเมลของคุณ
16. เลือก **แสดงตัวเลือกขั้นสูง** ใน **ชื่อสิ่งที่แนบมา – 1** ใส่ชื่อสิ่งที่แนบมาของคุณ เพิ่มนามสกุลไฟล์ลงในชื่อไฟล์ (เช่น .PDF) ที่ตรงกับ **รูปแบบการส่งออก** ที่คุณต้องการ
17. ใน **เนื้อหาสิ่งที่แนบมา** ให้เลือก **เนื้อหาไฟล์** เพื่อแนบรายงาน Power BI ที่ส่งออก  
 
    :::image type="content" source="media/service-automate-power-bi-report-export/automate-report-send-email-17.png" alt-text="เลือกรายงานที่ส่งออกของคุณไปยังอีเมล":::

18. เมื่อเสร็จสิ้นแล้ว ให้เลือก **ขั้นตอนถัดไป** หรือ **บันทึก** Power Automate สร้างและประเมินโฟลว์ และแจ้งให้คุณทราบว่าพบข้อผิดพลาดหรือไม่
1. ถ้ามีข้อผิดพลาด ให้เลือก **แก้ไขโฟลว์** เพื่อแก้ไขโฟลว์เหล่านั้น อีกทางหนึ่งคือ เลือกลูกศร **ย้อนกลับ** เพื่อดูรายละเอียดโฟลว์ และเรียกใช้โฟลว์ใหม่
    เมื่อคุณเรียกใช้โฟลว์ Power Automate จะส่งออกรายงาน Power BI ในรูปแบบที่ระบุไว้ และส่งเป็นสิ่งที่แนบมากับอีเมลตามที่กำหนดเวลาไว้  

## <a name="next-steps"></a>ขั้นตอนถัดไป

- [รวมการแจ้งเตือนข้อมูล Power BI ด้วย Power Automate](service-flow-integration.md)
- [เริ่มต้นใช้งาน Power Automate](/power-automate/getting-started/)
- มีคำถามเพิ่มเติมหรือไม่ [ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)
