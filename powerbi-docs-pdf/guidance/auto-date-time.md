---
title: คำแนะนำวันที่/เวลาอัตโนมัติใน Power BI Desktop
description: คำแนะนำสำหรับการใช้เกี่ยวกับฟังก์ชันการทำงานของวันที่/เวลาอัตโนมัติใน Power BI Desktop
author: peter-myers
ms.author: kfollis
manager: asaxton
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 10/23/2019
ms.openlocfilehash: e7fcab58dc61735639689c4574a9ce89757882ca
ms.sourcegitcommit: fb529c4532fbbdfde7ce28e2b4b35f990e8f21d9
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "99088683"
---
# <a name="auto-datetime-guidance-in-power-bi-desktop"></a>คำแนะนำวันที่/เวลาอัตโนมัติใน Power BI Desktop

บทความนี้มุ่งเป้าหมายไปที่เรื่อง ตัวสร้างแบบจำลองข้อมูลที่พัฒนามาจากแบบจำลองนำเข้าหรือแบบจำลองผสมใน Power BI Desktop ซึ่งมีคำแนะนำคำแนะนำและข้อควรพิจารณาเมื่อใช้ Power BI Desktop _วันที่/เวลาอัตโนมัติ_ ในสถานการณ์ที่เฉพาะเจาะจง สำหรับภาพรวมและบทนำทั่วไปเกี่ยวกับ _วันที่/เวลาอัตโนมัติ_ ให้ดูที่ [วันที่/เวลาอัตโนมัติใน Power BI Desktop](../transform-model/desktop-auto-date-time.md)

ตัวเลือก _วันที่/เวลาแบบอัตโนมัต_ ให้ความสะดวกรวดเร็วและสามารถปรับแต่งตัวแสดงเวลาได้ง่าย ผู้เขียนรายงานสามารถใช้งานตัวปรับแต่งการแสดงเวลาได้ง่ายเมื่อมีการกรอง การจัดกลุ่มและการเจาะลึกลงไปตามช่วงเวลาของปฏิทิน

## <a name="considerations"></a>ข้อควรพิจารณา

รายการหัวข้อย่อยต่อไปนี้อธิบายถึงข้อควรพิจารณาและขีดจำกัดที่สามารถทำได้ซึ่งเกี่ยวข้องกับตัวเลือก _วันที่/เวลาอัตโนมัติ_

- **สามารถนำไปใช้ทั้งหมดได้หรือไม่:** เมื่อเปิดใช้งานตัวเลือก _วันที่/เวลาอัตโนมัติ_ ระบบจะนำไปใช้กับคอลัมน์วันที่ทั้งหมดในการนำเข้าตารางที่ไม่ใช่ &quot;ด้าน&quot; จำนวนมากของความสัมพันธ์ ไม่สามารถเลือกเปิดหรือปิดใช้งานคอลัมน์ตามคอลัมน์พื้นฐานได้
- **รอบระยะเวลาตามปฏิทินเท่านั้น:** คอลัมน์ปีและไตรมาสเกี่ยวข้องกับรอบระยะเวลาปฏิทิน ซึ่งหมายความว่าการนับปีจะเริ่มต้นวันที่ 1 มกราคมและสิ้นสุดในวันที่ 31 ธันวาคม ไม่สามารถกำหนดค่าวันที่เริ่มต้นปี (หรือเสร็จสมบูรณ์) ได้ด้วยตัวเอง
- **การเลือกกำหนด:** ไม่สามารถกำหนดค่าที่ใช้เพื่ออธิบายช่วงเวลาได้ นอกจากนี้คุณยังไม่สามารถเพิ่มคอลัมน์เพิ่มเติมเพื่ออธิบายช่วงเวลาอื่นๆตัวอย่างเช่นสัปดาห์
- **ตัวกรองรายปี:** ค่าคอลัมน์ของ **ไตรมาส**, **เดือน** และ **วัน** จะไม่รวมปี ตัวอย่างเช่นคอลัมน์ **เดือน** ประกอบด้วยชื่อเดือนเท่านั้น (เช่นเดือนมกราคม เดือนกุมภาพันธ์ ฯลฯ) ค่าตัวเลขไม่ได้อธิบายค่าของตัวเองทั้งหมดและในบางการออกแบบรายงานอาจไม่เชื่อมต่อกับตัวกรองของปี

    ด้วยเหตุนี้จึงเป็นสิ่งสำคัญที่ตัวกรองหรือการจัดกลุ่มจะต้องมีอยู่ในคอลัมน์ **ปี** เมื่อดูรายละเอียดแนวลึกโดยใช้ปีที่มีลำดับชั้นซึ่งจะถูกกรองเว้นแต่ว่าจะมีการลบระดับ **ป** ี ออกโดยเจตนา ยกตัวอย่างเช่นถ้าไม่มีตัวกรองหรือการจัดกลุ่มตามปี การจัดกลุ่มตามเดือนจะสรุปค่าในทุกปีสำหรับเดือนนั้น
- **การกรองวันที่ด้วยตารางเดียว:** เนื่องจากแต่ละคอลัมน์มีวันที่สร้างตารางวันที่/เวลาอัตโนมัติของตนเอง (ถูกซ่อนไว้) ระบบจึงไม่สามารถใช้ตัวกรองเวลากับตารางหนึ่งและมีการเผยแพร่ไปยังตารางหลายแบบจำลอง การกรองด้วยวิธีนี้คือข้อกำหนดในการวางรูปแบบทั่วไปเมื่อรายงานในหลายวิชา (ตารางชนิดจริง) เช่นยอดขายและงบประมาณยอดขาย ผู้เขียนรายงานจะต้องนำตัวกรองไปใช้กับคอลัมน์วันที่ที่แตกต่างกันเมื่อใช้วันที่/เวลาอัตโนมัติ
- **ขนาดแบบจำลอง:** สำหรับแต่ละคอลัมน์วันที่ที่สร้างตารางวันที่/เวลาอัตโนมัติซึ่งซ่อนไว้จะส่งผลให้ขนาดของแบบจำลองที่เพิ่มขึ้นและยังขยายเวลาการรีเฟรชข้อมูล
- **เครื่องมือรายงานอื่นๆ:** ไม่สามารถทำงานกับตารางวันที่/เวลาอัตโนมัติเมื่อ:
  - การใช้ [การวิเคราะห์ใน Excel](../collaborate-share/service-analyze-in-excel.md)
  - การใช้ตัวออกแบบคิวรีของบริการการวิเคราะห์รายงานที่มีการแบ่งหน้าของ Power BI
  - การเชื่อมต่อไปยังแบบจำลองโดยใช้ตัวออกแบบรายงานที่ไม่ใช่ Power BI

## <a name="recommendations"></a>คำแนะนำ

เราขอแนะนำให้คุณเก็บตัวเลือก _วันที่/ เวลาอัตโนมัติ_ ที่เปิดใช้งานเฉพาะเมื่อคุณใช้งานช่วงเวลาของปฏิทินและเมื่อคุณมีข้อกำหนดแบบจำลองที่เรียบง่ายในความสัมพันธ์กับเวลา การใช้ตัวเลือกนี้ยังสามารถทำได้อย่างสะดวกสบายเมื่อสร้างแบบจำลองเฉพาะกิจ การดำเนินการสำรวจข้อมูลหรือการสร้างโพรไฟล์

ตารางนี้ควรใช้ในการกำหนดเวลาอย่างต่อเนื่องภายในองค์กรของคุณเมื่อแหล่งข้อมูลของคุณกำหนดตารางมิติวันที่แล้ว จะเป็นเคสขึ้นมาอย่างแน่นอนถ้าแหล่งข้อมูลของคุณเป็นคลังข้อมูล มิฉะนั้นคุณสามารถสร้างตารางวันที่ในแบบจำลองของคุณโดยใช้ฟังก์ชัน[ปฏิทิน DAX](/dax/calendar-function-dax)  หรือ [CALENDARAUTO](/dax/calendarauto-function-dax) จากนั้นคุณสามารถเพิ่มคอลัมน์จากการคำนวณเพื่อสนับสนุนความต้องการกรองและการจัดกลุ่มเวลาที่รู้จัก วิธีการออกแบบนี้อาจช่วยให้คุณสามารถสร้างตารางวันที่แบบเดี่ยวที่แพร่กระจายไปยังตารางชนิดข้อเท็จจริงทั้งหมดและอาจส่งผลให้ตารางเดียวสามารถใช้ตัวกรองเวลาได้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสร้างตารางวันที่ให้อ่านบทความ [ตั้งค่าและใช้ตารางวันที่ใน Power BI Desktop](../transform-model/desktop-date-tables.md)

ถ้าตัวเลือก _วันที่/เวลาอัตโนมัติ_ ไม่เกี่ยวข้องกับโครงการของคุณ เราขอแนะนำให้คุณปิดใช้งานตัวเลือก _วันที่/เวลาอัตโนมัติ_ จากส่วนกลาง เพื่อเป็นการทำให้มั่นใจว่าไฟล์ Power BI Desktop ใหม่ที่คุณสร้างจะไม่เปิดใช้งานตัวเลือก _วันที่/เวลาอัตโนมัติ_

## <a name="next-steps"></a>ขั้นตอนถัดไป

สำหรับข้อมูลเพิ่มเติมที่เกี่ยวข้องกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:

- [สร้างตารางวันที่ใน Power BI Desktop](model-date-tables.md)
- [วันที่/เวลาอัตโนมัติใน Power BI Desktop](../transform-model/desktop-auto-date-time.md)
- [ตั้งค่า และใช้งานตารางวันที่ใน Power BI Desktop](../transform-model/desktop-date-tables.md)
- มีคำถามหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)
- มีข้อเสนอแนะไหม [สนับสนุนแนวคิดในการปรับปรุง Power BI](https://ideas.powerbi.com/)
