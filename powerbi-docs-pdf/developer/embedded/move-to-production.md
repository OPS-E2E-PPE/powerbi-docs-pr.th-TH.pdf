---
title: ย้ายแอปพลิเคชันการวิเคราะห์แบบฝังตัว Power BI ของคุณไปยังการผลิตสำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: เรียนรู้ขั้นตอนที่จำเป็นในการย้ายแอปพลิเคชัน Power BI ไปยังการผลิต เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: rkarlin
ms.topic: tutorial
ms.service: powerbi
ms.subservice: powerbi-developer
ms.custom: seodec18
ms.date: 06/02/2020
ms.openlocfilehash: 71eff0f09c0e34ffd8789f1b56347d754b6589bc
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97886683"
---
# <a name="move-your-embedded-app-to-production"></a>ย้ายแอปแบบฝังตัวของคุณไปยังการผลิต

หลังจากที่คุณพัฒนาแอปพลิเคชันของคุณเสร็จเรียบร้อยแล้ว หากต้องการย้ายไปยังการผลิต คุณจะต้องสำรองพื้นที่ทำงานของคุณด้วยความจุ

> [!Important]
> พื้นที่ทำงานทั้งหมด (ที่มีรายงานหรือแดชบอร์ดและที่มีชุดข้อมูล) จะต้องกำหนดไว้สำหรับความจุ

## <a name="create-a-capacity"></a>สร้างความจุ

เมื่อสร้างความจุ คุณสามารถใช้ประโยชน์จากการมีทรัพยากรจัดสรรไว้สำหรับลูกค้าของคุณ มีความจุสองชนิดที่คุณสามารถเลือกได้:

* **Power BI Premium** - การสมัครใช้งาน Microsoft 356 ระดับผู้เช่าที่มีอยู่สองกลุ่ม SKU ได้แก่ *EM* และ *P* เมื่อมีการฝังเนื้อหา Power BI โซลูชันนี้เรียกว่า *การฝัง Power BI* สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสมัครสมาชิกนี้ โปรดดู [Power BI Premium คืออะไร](../../admin/service-premium-what-is.md)

* **Azure Power BI Embedded** - คุณสามารถซื้อความจุจาก [พอร์ทัล Microsoft Azure](https://portal.azure.com) การสมัครใช้งานนี้ใช้ *A* SKU สำหรับรายละเอียดเกี่ยวกับวิธีการสร้างความจุ Power BI Embedded โปรดดู[สร้างความจุ Power BI Embedded ในพอร์ทัล Azure](azure-pbie-create-capacity.md)

    > [!NOTE]
    > ด้วย A SKU คุณไม่สามารถเข้าถึงเนื้อหา Power BI ที่มีสิทธิ์การใช้งาน Power BI ฟรี

### <a name="capacity-specifications"></a>ข้อมูลจำเพาะของความจุ

ตารางด้านล่างอธิบายแหล่งข้อมูลและขีดจำกัดของแต่ละ SKU หากต้องการตรวจสอบความจุที่เหมาะสมที่สุดกับความต้องการของคุณ ให้ดูตาราง [SKU ใดที่ฉันควรซื้อสำหรับสถานการณ์ของฉัน](./embedded-faq.md#which-solution-should-i-choose)

| โหนดความจุ | วี-คอร์รวม | Backend v-cores | RAM (GB) | Frontend v-cores | DirectQuery/Live Connection (ต่อวินาที) | การรีเฟรชแบบจำลองแบบคู่ขนาน |
| --- | --- | --- | --- | --- | --- | --- |
| EM1/A1 | 1 | 0.5 | 2.5 | 0.5 | 3.75 | 1 |
| EM2/A2 | 2 | 1 | 5 | 1 | 7.5 | 2 |
| EM3/A3 | 4 | 2 | 10 | 2 | 15 | 3 |
| P1/A4 | 8 | 4 | 25 | 4 | 30 | 6 |
| P2/A5 | 16 | 8 | 50 | 8 | 60 | 12 |
| P3/A6 | 32 | 16 | 100 | 16 | 120 | 24 |
| | | | | | | |

## <a name="development-testing"></a>การทดสอบการพัฒนา

สำหรับการทดสอบการพัฒนา คุณสามารถใช้โทเค็นรุ่นทดลองใช้แบบฝังพร้อมกับสิทธิ์ใช้งานแบบ Pro หากต้องการฝังในสภาพแวดล้อมการผลิต ให้ใช้ความจุ

จำนวนโทเค็นการทดลองแบบฝังตัวที่ *โครงร่างสำคัญของบริการ* หรือ *ผู้ใช้หลัก* (บัญชีหลัก) ของ Power BI สามารถสร้างได้นั้นมีจำกัด ใช้ API ของ[คุณลักษณะที่มีอยู่](/rest/api/power-bi/availablefeatures/getavailablefeatures)เพื่อตรวจสอบเปอร์เซ็นต์ของการใช้งานแบบฝังในปัจจุบันของคุณ จำนวนการใช้งานจะปรากฏขึ้นต่อบริการหลักหรือบัญชีหลัก

หากคุณใช้งานโทเค็นแบบฝังหมดขณะทดสอบ คุณจำเป็นต้องซื้อ Power BI Embedded หรือ[ความจุ](embedded-capacity.md) Premium ไม่มีการจำกัดจำนวนโทเค็นแบบฝังที่คุณสามารถสร้างได้ด้วยความจุ

## <a name="assign-a-workspace-to-a-capacity"></a>กำหนดพื้นที่ทำงานของแอปไปยังความจุ

เมื่อคุณสร้างความจุแล้ว คุณสามารถกำหนดพื้นที่ทำงานไปยังความจุนั้นได้

พื้นที่ทำงานทั้งหมดที่ประกอบด้วยแหล่งข้อมูล Power BI ที่เกี่ยวข้องกับเนื้อหาแบบฝังตัว (รวมถึงชุดข้อมูล รายงานและแดชบอร์ด) จะต้องได้รับมอบหมายไปยังความจุ ตัวอย่างเช่น หากรายงานแบบฝังและชุดข้อมูลที่ผูกไว้อยู่ในพื้นที่ทำงานที่ต่างกันสองแห่ง ต้องมอบหมายพื้นที่ทำงานทั้งสองแห่งไปยังความจุ

### <a name="assign-a-workspace-to-a-capacity-using-a-service-principal"></a>กำหนดพื้นที่ทำงานให้กับความจุโดยใช้โครงร่างสำคัญของบริการ

หากต้องกำหนดความจุกับพื้นที่ทำงานโดยใช้[โครงร่างสำคัญของบริการ](embed-service-principal.md) ให้ใช้ [Power BI REST API](/rest/api/power-bi/capacities/groups_assigntocapacity) เมื่อคุณกำลังใช้ Power BI REST API ทำให้แน่ใจว่าใช้[ ID ออบเจ็กต์ของโครงร่างสำคัญของบริการ](embed-service-principal.md)

### <a name="assign-a-workspace-to-a-capacity-using-a-master-user"></a>กำหนดพื้นที่ทำงานให้กับความจุโดยใช้ผู้ใช้หลัก

ทำตามขั้นตอนด้านล่างเพื่อกำหนดความจุสำหรับพื้นที่ทำงานโดยใช้ **ผู้ใช้หลัก**

1. เปิดพื้นที่ทำงานใน **บริการ Power BI** เลือก 

1. ภายใน **บริการของ Power BI** ขยายพื้นที่ทำงาน และเลือกที่จุดไข่ปลาสำหรับพื้นที่ทำงานที่คุณกำลังใช้เพื่อฝังเนื้อหา แล้วเลือก **แก้ไขพื้นที่ทำงาน**

    >[!div class="mx-imgBorder"]
    >:::image type="content" source="media/move-to-production/workspace-settings.png" alt-text="สกรีนช็อตที่แสดงเมนูการตั้งค่าพื้นที่ทำงานในพอร์ทัลบริการ Power BI":::

2. เลือกแท็บ **Premium** และทำตามขั้นตอนต่อไปนี้:

    * เปิดใช้งาน **ความจุ**

    * เลือกความจุที่คุณสร้าง

    * เลือก **บันทึก**

    >[!div class="mx-imgBorder"]
    >:::image type="content" source="media/move-to-production/premium-tab.png" alt-text="สกรีนช็อตที่แสดงแท็บการตั้งค่าพื้นที่ทำงานแบบ premium ในพอร์ทัลบริการ Power BI":::

    หลังจากกำหนดพื้นที่ทำงานของคุณไปยังความจุแล้ว เพชรจะปรากฏขึ้นข้าง ๆ 

    >[!div class="mx-imgBorder"]
    >:::image type="content" source="media/move-to-production/premium-workspace.png" alt-text="สกรีนช็อตที่แสดงเพชรถัดจากพื้นที่ทำงานที่มีความจุระดับพรีเมียมในพอร์ทัลบริการ Power BI":::

## <a name="next-steps"></a>ขั้นตอนถัดไป

>[!div class="nextstepaction"]
>[ความจุและ SKU ในการวิเคราะห์แบบฝังตัวของ Power BI](embedded-capacity.md)

>[!div class="nextstepaction"]
>[ความจุและ SKU ในการวิเคราะห์แบบฝังของ Power BI](embedded-capacity-planning.md)

>[!div class="nextstepaction"]
>[ข้อควรพิจารณาเมื่อสร้างโทเค็นแบบฝัง](generate-embed-token.md)