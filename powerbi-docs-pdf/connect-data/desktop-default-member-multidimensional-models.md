---
title: สมาชิกเริ่มต้นในแบบจำลองหลายมิติใน Power BI
description: เรียนรู้วิธีการทำงานของ Power BI เมื่อทำงานกับสมาชิกเริ่มต้นในแบบจำลองหลายมิติ
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: conceptual
ms.date: 01/10/2019
LocalizationGroup: Data from files
ms.openlocfilehash: b339117e8cba73da35759a600d3f303b93415711
ms.sourcegitcommit: fb529c4532fbbdfde7ce28e2b4b35f990e8f21d9
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "99086418"
---
# <a name="work-with-multidimensional-models-in-power-bi"></a>ทำงานกับแบบจำลองหลายมิติใน Power BI

คุณสามารถเชื่อมต่อกับแบบจำลองหลายมิติใน Power BI และสร้างรายงานที่แสดงภาพข้อมูลทั้งหมดภายในแบบจำลอง เมื่อทำงานกับแบบจำลองหลายมิติ Power BI จะใช้กฎวิธีการประมวลผลข้อมูล โดยยึดตามคอลัมน์ที่กำหนดเป็นคำ *สมาชิกเริ่มต้น* 

เมื่อทำงานกับแบบจำลองหลายมิติ Power BI จัดการข้อมูลจากแบบจำลองตามจุดคอลัมน์ที่มีการใช้ **DefaultMember** แอตทริบิวต์ *DefaultMember* จะถูกตั้งค่าใน CSDL (Conceptual Schema Definition Language) สำหรับคอลัมน์เฉพาะในแบบจำลองหลายมิติ คุณสามารถเรียนรู้เพิ่มเติมเกี่ยวกับสมาชิกเริ่มต้นใน[บทความคุณสมบัติแอตทริบิวต์](/sql/analysis-services/multidimensional-models/attribute-properties-define-a-default-member)ดังกล่าว เมื่อดำเนินการคิวรี DAX สมาชิกเริ่มต้นที่ระบุในแบบจำลองจะถูกนำไปใช้โดยอัตโนมัติ

บทความนี้อธิบายวิธีการทำงานของ Power BI ภายใต้สถานการณ์ต่าง ๆ เมื่อทำงานกับแบบจำลองหลายมิติ โดยอิงตามตำแหน่งที่พบ *สมาชิกเริ่มต้น* 

## <a name="working-with-filter-cards"></a>การทำงานกับบัตรตัวกรอง

เมื่อสร้างบัตรตัวกรองบนเขตข้อมูลที่มีสมาชิกเริ่มต้น ค่าเขตข้อมูลของสมาชิกเริ่มต้นจะถูกเลือกโดยอัตโนมัติในบัตรตัวกรอง ผลลัพธ์คือ วิชวลทั้งหมดที่ได้รับผลกระทบจากบัตรตัวกรองจะรักษาแบบจำลองเริ่มต้นในฐานข้อมูล ค่าต่าง ๆ ในบัตรตัวกรองดังกล่าวจะแสดงเป็นสมาชิกเริ่มต้น

หากลบสมาชิกเริ่มต้น การยกเลิกการเลือกค่าจะล้างออกเพื่อวิชวลทั้งหมดสำหรับใช้บัตรตัวกรอง และค่าที่แสดงจะไม่แสดงสมาชิกเริ่มต้น

เช่น สมมติว่าเรามีคอลัมน์ *สกุลเงิน* ที่มีสมาชิกเริ่มต้นซึ่งตั้งค่าเป็น *USD*:

* ในกรณีตัวอย่างนี้ หากเรามีบัตรที่แสดง *ยอดขายรวม* ค่าจะมีสมาชิกเริ่มต้นที่นำไปใช้ และเราจะเห็นยอดขายที่สอดคล้องกับสกุลเงิน "USD"
* หากเราลาก *สกุลเงิน* ไปยังบานหน้าต่างบัตรตัวกรอง เราจะเห็น *USD* เป็นค่าเริ่มต้นที่เลือกไว้ ค่าของ *ยอดขายรวม* จะยังคงเหมือนเดิม เนื่องจากมีการใช้สมาชิกเริ่มต้น
* อย่างไรก็ตาม หากเรายกเลิกการเลือกค่า *USD* จากบัตรตัวกรอง สมาชิกเริ่มต้นสำหรับ *สกุลเงิน* จะถูกล้างออก และตอนนี้ *ยอดขายรวม* จะแสดงสกุลเงินทั้งหมด
* ดังนั้น เมื่อเราเลือกค่าอื่นในบัตรตัวกรอง (สมมติว่าเราเลือก *EURO*) *ยอดขายรวม* จะแสดงตัวกรอง *สกุลเงินเป็น {USD, EURO}* ในสมาชิกเริ่มต้นทั้งหมด

## <a name="grouping-behavior"></a>การจัดกลุ่มลักษณะการทำงาน

ใน Power BI ทุกครั้งที่คุณจัดกลุ่มวิชวลบนคอลัมน์ที่มี *สมาชิกเริ่มต้น* Power BI จะล้าง *สมาชิกเริ่มต้น* สำหรับคอลัมน์ดังกล่าวและเส้นทางความสัมพันธ์ของแอตทริบิวต์ ซึ่งทำให้แน่ใจวิชวลจะแสดงค่าทั้งหมดที่ไม่ใช่แค่เฉพาะค่าเริ่มต้น

## <a name="attribute-relationship-paths-arps"></a>เส้นทางความสัมพันธ์ของแอตทริบิวต์ (ARP)

เส้นทางความสัมพันธ์ของแอตทริบิวต์ (ARP) จะมี *สมาชิกเริ่มต้น* พร้อมความสามารถที่มีประสิทธิภาพ แต่ยังคงมีความซับซ้อนอยู่ส่วนหนึ่ง เมื่อตรวจพบ ARP, Power BI จะติดตามเส้นทางของ ARP เพื่อล้างสมาชิกเริ่มต้นเพิ่มเติมสำหรับคอลัมน์อื่น ๆ เพื่อให้การจัดการข้อมูลสำหรับวิชวลมีความสอดคล้องและแม่นยำ

ลองดูตัวอย่างเพื่อทำความเข้าใจลักษณะการทำงาน พิจารณาการกำหนดค่าของ ARP ต่อไปนี้:

![ARP ในแบบจำลองหลายมิติ](media/desktop-default-member-multidimensional-models/default-members_01.png)

ตอนนี้ลองจินตนาการ *สมาชิกเริ่มต้น* ต่อไปนี้ที่ตั้งค่าสำหรับคอลัมน์เหล่านี้:

* เมือง > ซีแอตเทิล
* รัฐ > วอชิงตัน
* ประเทศ > สหรัฐอเมริกา
* ประชากร > ขนาดใหญ่

ตอนนี้ลองตรวจสอบสิ่งที่เกิดขึ้นเมื่อแต่ละคอลัมน์ที่ถูกใช้ใน Power BI เมื่อวิชวลจับกลุ่มบนคอลัมน์ต่อไปนี้ จึงเกิดผลลัพธ์ต่าง ๆ ดังนี้:

* **เมือง** - Power BI แสดงเมืองทั้งหมด โดยล้าง **สมาชิกเริ่มต้น** ทั้งหมดสำหรับ *เมือง* *รัฐ* *ประเทศ* แต่ไม่ล้าง **สมาชิกเริ่มต้น** สำหรับ *ประชากร* เนื่องจาก Power BI ได้ล้าง ARP ทั้งหมดสำหรับ *เมือง* แล้ว
    > [!NOTE]
    > *ประชากร* ไม่อยู่ในเส้นทาง ARP ของ *เมือง* ซึ่งเกี่ยวข้องกับ *รัฐ* เพียงอย่างเดียว ดังนั้น Power BI จึงไม่ได้ล้างค่า
* **รัฐ** - Power BI แสดง *รัฐ* ทั้งหมดโดยล้าง **สมาชิกเริ่มต้น** ทั้งหมดสำหรับ *เมือง* *รัฐ* *ประเทศ* และ *ประชากร*
* **ประเทศ** - Power BI แสดงประเทศทั้งหมด โดยล้าง **สมาชิกเริ่มต้น** ทั้งหมดสำหรับ *เมือง* *รัฐ* *ประเทศ* แต่ไม่ล้าง **สมาชิกเริ่มต้น** สำหรับ *ประชากร*
* **เมืองและรัฐ** - Power BI จะล้าง **สมาชิกเริ่มต้น** ทั้งหมดสำหรับคอลัมน์ทั้งหมด

กลุ่มที่แสดงในวิชวลมีเส้นทาง ARP ทั้งหมดที่ถูกล้างแล้ว 

หากมีกลุ่มหนึ่งไม่แสดงในวิชวล แต่เป็นส่วนหนึ่งของเส้นทาง ARP บนคอลัมน์ที่จัดกลุ่มอื่น จะมีสิ่งต่อไปนี้เกิดขึ้น:

* เส้นทาง ARP บางสาขาจะถูกล้างออกโดยอัตโนมัติ
* กลุ่มดังกล่าวจะยังคงถูกกรองโดย **สมาชิกเริ่มต้น** ที่ยังไม่ได้ล้าง

### <a name="slicers-and-filter-cards"></a>ตัวแบ่งส่วนข้อมูลและบัตรตัวกรอง

เมื่อทำงานกับตัวแบ่งส่วนข้อมูลหรือบัตรตัวกรอง จะมีลักษณะการทำงานต่อไปนี้เกิดขึ้น:

* เมื่อป้อนข้อมูลลงในตัวแบ่งส่วนข้อมูลหรือบัตรตัวกรอง Power BI จะจัดกลุ่มบนคอลัมน์ในวิชวล เพื่อให้การแสดงลักษณะการทำงานเหมือนกับที่อธิบายไว้ในส่วนก่อนหน้า

เนื่องจากตัวแบ่งส่วนข้อมูลและบัตรตัวกรองมักใช้เพื่อโต้ตอบกับวิชวลอื่น ๆ ตรรกะของการล้าง **สมาชิกเริ่มต้น** สำหรับวิชวลที่ได้รับผลกระทบจะเกิดขึ้นตามที่อธิบายไว้ในตารางต่อไปนี้ 

สำหรับตารางนี้ เราใช้ข้อมูลตัวอย่างเดียวกันกับที่ใช้ก่อนหน้าในบทความนี้:

![การล้างลักษณะการทำงานหรือสมาชิกเริ่มต้นของ Power BI ด้วยตัวแบ่งส่วนข้อมูลและบัตรตัวกรอง](media/desktop-default-member-multidimensional-models/default-members_02.png)

กฎต่อไปนี้จะใช้กับวิธีการทำงานของ Power BI ในสถานการณ์เหล่านี้

Power BI จะล้าง **สมาชิกเริ่มต้น** สำหรับคอลัมน์ที่มีให้หาก:

* Power BI จัดกลุ่มบนคอลัมน์ดังกล่าว
* Power BI จัดกลุ่มบนคอลัมน์ที่เกี่ยวข้องกับคอลัมน์ดังกล่าว (ทุกที่ใน ARP ขึ้นหรือลง)
* Power BI กรองคอลัมน์ที่อยู่ใน ARP (ขึ้นหรือลง)
* คอลัมน์มีบัตรตัวกรองที่มีรัฐ *ทั้งหมด*
* คอลัมน์มีบัตรตัวกรองที่มีค่าใด ๆ ที่เลือกไว้ (Power BI ได้รับตัวกรองสำหรับคอลัมน์)

Power BI ไม่ล้าง **สมาชิกเริ่มต้น** สำหรับคอลัมน์ที่มีให้หาก:

* คอลัมน์มีบัตรตัวกรองที่มีสถานะเริ่มต้น และ Power BI กำลังจัดกลุ่มบนคอลัมน์ใน ARP
* คอลัมน์อยู่เหนือคอลัมน์อื่นใน ARP และ Power BI มีบัตรตัวกรองสำหรับคอลัมน์อื่น ๆ ดังกล่าวในสถานะเริ่มต้น


## <a name="next-steps"></a>ขั้นตอนถัดไป

บทความนี้อธิบายลักษณะการทำงานของ Power BI เมื่อทำงานกับสมาชิกเริ่มต้นในแบบจำลองหลายมิติ คุณอาจมีความสนใจบทความต่อไปนี้: 

* [แสดงรายการที่ไม่มีข้อมูลใน Power BI](../create-reports/desktop-show-items-no-data.md)
* [แหล่งข้อมูลใน Power BI Desktop](desktop-data-sources.md)