---
title: การแคชคิวรีใน Power BI Premium
description: การแคชคิวรีใน Power BI Premium
author: KesemSharabi
ms.author: kesharab
ms.reviewer: bhmerc
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 10/04/2019
LocalizationGroup: ''
ms.openlocfilehash: 8495ccd75fec49079e87312bbf5a7693b78b3e6b
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96404145"
---
# <a name="query-caching-in-power-bi-premiumembedded"></a>การแคชคิวรีใน Power BI Premium/แบบฝังตัว

องค์กรที่มี Power BI Premium หรือ Power BI แบบฝังตัว สามารถใช้ประโยชนจาก *การแคชคิวรี* เพื่อให้รายงานที่เกี่ยวข้องกับชุดข้อมูลแสดงผลเร็วขึ้น การแคชคิวรีแนะนำความจุ Premium/แบบฝังตัว เพื่อใช้บริการการแคชในพื้นที่เพื่อรักษาผลลัพธ์คิวรี หลีกเลี่ยงแหล่งข้อมูลแฝงในการคำนวณผลลัพธ์เหล่านั้น

> [!IMPORTANT]
> การแคชคิวรีจะพร้อมใช้งานบน Power BI Premium หรือ Power BI แบบฝังตัว ไม่สามารถใช้กับชุดข้อมูล LiveConnect ที่ใช้ประโยชน์จาก Azure Analysis Services หรือ SQL Server Analysis Services

ผลลัพธ์คิวรีที่แคชไว้จะใช้เฉพาะกับผู้ใช้และบริบทชุดข้อมูล และควรคำนึงถึงกฎความปลอดภัยเสมอ ในปัจจุบัน มีบริการแคชคิวรีสำหรับหน้าเริ่มต้นที่คุณไปถึง กล่าวคือ คิวรีไม่ได้ถูกแคชเมื่อคุณโต้ตอบกับรายงาน แคชของคิวรีมีความสำคัญกับ[บุ๊กมาร์กส่วนบุคคล](../consumer/end-user-bookmarks.md#personal-bookmarks)และ[ตัวกรองแบบถาวร](https://powerbi.microsoft.com/blog/announcing-persistent-filters-in-the-service/) ดังนั้นคิวรีที่สร้างขึ้นโดยรายงานส่วนบุคคลจะถูกแคช [ไทล์แดชบอร์ด](../create-reports/service-dashboard-tiles.md)ที่ขับเคลื่อนโดยคิวรีเดียวกันจะได้ประโยชน์เมื่อมีการแคชคิวรี โดยเฉพาะอย่างยิ่งประสิทธิภาพจะได้รับประโยชน์เมื่อชุดข้อมูลมีการเข้าถึงบ่อยครั้ง และไม่จำเป็นต้องรีเฟรชบ่อยครั้ง การแคชคิวรียังสามารถลดการโหลดความจุแบบ Premium/แบบฝังตัว ของคุณโดยการลดจำนวนคิวรีโดยรวมได้

คุณสามารถควบคุมพฤติกรรมการแคชคิวรี่ได้ที่หน้า **การตั้งค่า** สำหรับชุดข้อมูลในบริการ Power BI การตั้งค่าที่เป็นไปได้มีอยู่สามวิธีด้วยกัน:

- **ค่าเริ่มต้นความจุ**: ปิดการแคชแบบสอบถาม
- **ปิด**: อย่าใช้การแคชคิวรี่สำหรับชุดข้อมูลนี้
- **เปิด**: ใช้การแคชคิวรี่สำหรับชุดข้อมูลนี้

    ![กล่องโต้ตอบการแคชคิวรี](media/power-bi-query-caching/power-bi-query-3-options.png)

## <a name="considerations-and-limitations"></a>ข้อควรพิจารณาและข้อจำกัด

- เมื่อคุณเปลี่ยนการตั้งค่าการแคชจาก **เปิด** เป็น **ปิด** ผลลัพธ์คิวรีที่บันทึกไว้ก่อนหน้านี้ทั้งหมดสำหรับชุดข้อมูลจะถูกลบออกจากแคชความจุ คุณสามารถปิดใช้งานการแคชอย่างชัดแจ้ง หรือโดยการเปลี่ยนกลับไปเป็นการตั้งค่าความจเริ่มต้นุที่ผู้ดูแลระบบตั้งค่าเป็น **ปิด** การปิดอาจก่อให้เกิดความล่าช้าเล็กน้อยในครั้งถัดไปที่ซึ่งรายงานเรียกใช้คิวรีกับชุดข้อมูลนี้ ความล่าช้ามีสาเหตุมาจากคิวรีรายงานที่เรียกใช้ตามคำขอ และไม่ได้ใช้ประโยชน์จากผลลัพธ์ที่บันทึกไว้ นอกจากนี้ ชุดข้อมูลที่กำหนดอาจจำเป็นต้องโหลดลงในหน่วยความจำก่อนที่จะสามารถให้บริการคิวรีได้
- เมื่อแคชของคิวรีถูกรีเฟรช Power BI ต้องเรียกใช้คิวรีกับแบบจำลองข้อมูลเบื้องต้นเพื่อรับผลลัพธ์ล่าสุด หากชุดข้อมูลจำนวนมากเปิดใช้งานการแคชคิวรีและความจุพรีเมียม/แบบฝังตัวต้องทำงานหนัก อาจทำให้ประสิทธิภาพลดลงในระหว่างการรีเฟรชแคช ประสิทธิภาพลดลงเนื่องจากปริมาณการคิวรีที่เพิ่มขึ้น

## <a name="next-steps"></a>ขั้นตอนถัดไป

* [Power BI Premium คืออะไร?](../admin/service-premium-what-is.md)
* [Power BI อะไรที่ถูกฝังอยู่ใน Azure?](../developer/embedded/azure-pbie-what-is-power-bi-embedded.md)
