---
title: การโต้ตอบกับวิชวลของวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายถึงวิธีการตรวจสอบว่าวิชวล Power BI ควรอนุญาตให้มีการโต้ตอบกับวิชวลหรือไม่ เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: how-to
ms.date: 06/18/2019
ms.openlocfilehash: a5b46e901b5e8cabc00d48e4ef307b2ae98de2b6
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888523"
---
# <a name="visual-interactions-in-power-bi-visuals"></a>การโต้ตอบกับวิชวลในวิชวล Power BI

วิชวลสามารถคิวรีค่าของสถานะ `allowInteractions` ได้ซึ่งบ่งชี้ว่าวิชวลควรอนุญาตให้มีการโต้ตอบกับวิชวลหรือไม่ ตัวอย่างเช่น วิชวลมีการโต้ตอบระหว่างการดูหรือแก้ไขรายงาน แต่ไม่สามารถโต้ตอบได้เมื่อดูวิชวลในแดชบอร์ด การโต้ตอบเหล่านี้คือ *การคลิก*, *การแพน*, *การซูม*, *การเลือก* และอื่น ๆ 

> [!NOTE]
> คุณควรเปิดใช้งานคำแนะนำเครื่องมือในทุกสถานการณ์โดยไม่คำนึงว่ามีการระบุเป็นสถานะใด

ค่าสถานะ `allowInteractions` จะถูกส่งผ่านค่าเป็นบูลีนในระหว่างการเตรียมใช้งานของวิชวลในฐานะสมาชิกของอินเทอร์เฟซ IVisualHost

ในสถานการณ์สมมติของ Power BI ใดก็ตามที่ต้องการให้วิชวลไม่สามารถโต้ตอบได้ (ตัวอย่างเช่น ไทล์แดชบอร์ด) `allowInteractions` จะถูกตั้งค่าเป็น `false` มิฉะนั้น (ตัวอย่างเช่น รายงาน) `allowInteractions` จะถูกตั้งค่าเป็น `true`

สำหรับข้อมูลเพิ่มเติม ให้ดู [ที่เก็บวิชวล SampleBarChart](https://github.com/Microsoft/PowerBI-visuals-sampleBarChart/commit/59a47935d8f5272ce145fe804193599ddb7e2001)

```typescript
   ...
   let allowInteractions = options.host.allowInteractions;
   bars.on('click', function(d) {
       if (allowInteractions) {
           selectionManager.select(d.selectionId);
           ...
       }
   });
```
