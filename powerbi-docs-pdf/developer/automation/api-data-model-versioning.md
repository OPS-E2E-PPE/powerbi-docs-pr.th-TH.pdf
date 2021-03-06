---
title: การกำหนดรุ่นแบบจำลองข้อมูล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: แบบจำลองข้อมูลที่แสดงโดยบริการ OData เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: 0c645774f7af1a8575ca3c755a74fd65b652031a
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887718"
---
# <a name="data-model-versioning"></a>การกำหนดรุ่นแบบจำลองข้อมูล

แบบจำลองข้อมูลที่แสดงโดยบริการ OData เช่นแบบจำลองข้อมูล Power BI กำหนดสัญญาระหว่างบริการ OData และไคลเอ็นต์ของ OData บริการที่สามารถให้ขยายแบบจำลองของตนให้อยู่ในระดับที่ไม่ทำลายการคงอยู่ของไคลเอ็นต์ การเปลี่ยนแปลงฉับพลันเช่นเอาคุณสมบัติออก หรือเปลี่ยนชนิดของคุณสมบัติที่มีอยู่จำเป็นต้องมีระบบบริการรุ่นใหม่ที่มีการให้บริการด้วย URL ที่ต่างกันสำหรับแบบจำลองใหม่  
  
การเพิ่มรูปแบบข้อมูลดังต่อไปนี้ถือว่าเป็นการกระทำที่ปลอดภัย และไม่จำเป็นต้องมีบริการเพิ่มเติมมาตรวจสอบจุดที่เข้ามาของข้อมูล  
  
* เพิ่มคุณสมบัติที่ไม่มีการตั้งค่าใดๆ หรือเป็นค่าเริ่มต้น ถ้าคุณสมบัติที่เพิ่มเข้ามามีชื่อเดียวกันเป็นคุณสมบัติแบบไดนามิกที่มีอยู่แล้ว คุณสมบัติที่เพิ่มเข้ามาใหม่จะต้องเป็นประเภทเดียวกันกับ (หรือชนิดพื้นฐานเดียวกัน) คุณสมบัติแบบไดนามิกที่มีอยู่  
* เพิ่มคุณสมบัตินำทางที่ไม่มีการตั้งค่าใดๆ ถ้าคุณสมบัติที่เพิ่มเข้ามามีชื่อเดียวกันเป็นคุณสมบัตินำทางแบบไดนามิกที่มีอยู่แล้ว คุณสมบัติที่เพิ่มเข้ามาใหม่จะต้องเป็นประเภทเดียวกันกับ (หรือชนิดพื้นฐานเดียวกัน) คุณสมบัตินำทางแบบไดนามิกที่มีอยู่  
* เพิ่มประเภทเอนทิตีใหม่ลงในรูปแบบ  
* เพิ่มประเภทเอนทิตีซับซ้อนใหม่ลงในรูปแบบ  
* เพิ่มชุดเอนทิตีใหม่  
* เพิ่ม singleton ใหม่  
* เพิ่มการดำเนินการ ฟังก์ชัน การนำเข้าการดำเนินการ หรือนำเข้าฟังก์ชัน
* เพิ่มพารามิเตอร์ดำเนินการที่ไม่มีการตั้งค่า  
* เพิ่มประเภทข้อกำหนดหรือการแจกแจง  
* เพิ่มคำอธิบายประกอบใด ๆ ไปยังแบบจำลององค์ประกอบที่ไคลเอ็นต์ไม่จำเป็นต้องเข้าใจ เพื่อให้มีการโต้ตอบกับการบริการอย่างเหมาะสม  
  
ไคลเอ็นต์ ***ควรจะ** _ เตรียมพร้อมสำหรับบริการเพื่อทำการเปลี่ยนแปลงเพิ่มเติมไปยังแบบจำลองของตน โดยเฉพาะอย่างยิ่ง ไคลเอ็นต์ควรเตรียมพร้อมเพื่อรับมือกับประเภทหรือคุณสมบัติที่ไม่ได้ถูกนิยามไว้ในการบริการ  
  
การบริการ _ *_ไม่ควรจะ_** เปลี่ยนแบบจำลองข้อมูลตามความพอใจของผู้ใช้งานที่ได้รับอนุญาต ถ้าตัวแบบจำลองข้อมูลเป็นผู้ใช้หรือกลุ่มผู้ใช้ที่ขึ้นต่อกัน การเปลี่ยนแปลงทั้งหมดจะต้องเป็นไปอย่างปลอดภัยตามที่ได้กำหนดไว้ในส่วนนี้เมื่อมีการเปรียบเทียบระหว่างการใช้งานแบบจำลองอย่างเต็มประสิทธิภาพกับแบบจำลองที่ถูกจำกัดให้ผู้ใช้งานมองเห็นได้อย่างเดียวเท่านั้น  
  
สำหรับข้อมูลเพิ่มเติมเกี่ยวกับมาตรฐานแบบจำลองข้อมูล OData ให้ดูที่[OData เวอร์ชัน 4.0 ส่วนที่ 1: Protocol Plus Errata 02](https://docs.oasis-open.org/odata/odata/v4.0/odata-v4.0-part1-protocol.html)  
  
## <a name="see-also"></a>นอกจากนี้ โปรดดู
[ภาพรวมของ Power BI REST API](/rest/api/power-bi/)