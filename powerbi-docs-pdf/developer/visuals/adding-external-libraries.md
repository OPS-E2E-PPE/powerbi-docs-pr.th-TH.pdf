---
title: การเพิ่มไลบรารีภายนอกไปยังวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการใช้ไลบรารีภายนอกในการแสดงผลด้วยภาพของ Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.date: 02/24/2020
ms.openlocfilehash: b9a443040384e4d38bd7440eae0a5582cc422836
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97889190"
---
# <a name="adding-external-libraries"></a>การเพิ่มไลบรารีภายนอก

บทความนี้อธิบายวิธีการใช้ไลบรารีภายนอกในการแสดงผลด้วยภาพของ Power BI ซึ่งรวมถึงข้อมูลเกี่ยวกับการติดตั้ง การนำเข้า และเรียกใช้ไลบรารีภายนอกจากรหัสของการแสดงผลด้วยภาพของ Power BI

## <a name="javascript-libraries"></a>ไลบรารี JavaScript

1. ติดตั้งไลบรารี JavaScript ภายนอกโดยใช้ตัวจัดการแพคเกจต่างๆ เช่น *npm* หรือ *yarn*
2. นำเข้าโมดูลที่จำเป็นลงในไฟล์ต้นฉบับโดยใช้ไลบรารีภายนอก

>[!NOTE]
>ถ้าคุณต้องการเพิ่ม typings ไปยังไลบรารี JavaScript ของคุณและรับข้อมูลความปลอดภัยและการคอมไพล์ในขณะนี้ โปรดตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งแพคเกจที่เหมาะสม

### <a name="installing-the-d3-library"></a>การติดตั้งไลบรารี d3

นี่คือตัวอย่างของการติดตั้ง[ไลบรารี d3](https://www.npmjs.com/package/d3) [และแพคเกจ@types/d3](https://www.npmjs.com/package/@types/d3) โดยใช้ [npm](https://www.npmjs.com/)

สำหรับตัวอย่างเต็มรูปแบบ โปรดดูรหัส[การแสดงภาพ Power BI](https://github.com/microsoft/powerbi-visuals-gantt/blob/master/src/gantt.ts#L29)

1. ติดตั้งแพคเกจ *d3* และแพคเกจ *ชนิด d3*

    ```powershell
    npm install d3@5 --save
    npm install @types/d3@5 --save
    ```

2. นำเข้าไลบรารี *d3* ในไฟล์ที่ใช้เช่น `visual.ts`

    ```typescript
    import * as d3 from "d3";
    ```

## <a name="css-framework"></a>CSS framework

1. ติดตั้งไลบรารี JavaScript ภายนอกโดยใช้ตัวจัดการแพคเกจต่างๆ เช่น *npm* หรือ *yarn*
2. ใน`.less`ไฟล์ของการแสดงผลด้วยภาพ รวมถึง`import`คำสั่ง

### <a name="installing-bootstrap"></a>กำลังติดตั้ง bootstrap

นี่คือตัวอย่างของการติดตั้ง [bootstrap](https://www.npmjs.com/package/bootstrap) จากการใช้ [npm](https://www.npmjs.com/)

สำหรับตัวอย่างเต็มรูปแบบ โปรดดูรหัส[การแสดงภาพ Power BI](https://github.com/Microsoft/powerbi-visuals-sankey/blob/c8200da56913cd8b253be949a35fad0f4472b6de/style/visual.less#L32)

1. ติดตั้งแพคเกจ *bootstrap*

    ```powershell
    npm install bootstrap --save
    ```

2. รวม`import`คำสั่งใน`visual.less`

    ```less
    @import (less) "node_modules/bootstrap/dist/css/bootstrap.css";
    ```
