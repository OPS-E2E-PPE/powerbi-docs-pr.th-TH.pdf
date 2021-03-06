---
title: เพิ่มเมนูบริบทไปยังวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: เรียนรู้วิธีการเพิ่มเมนูบริบทลงในวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: rkarlin
manager: rkarlin
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: how-to
ms.date: 06/18/2019
ms.openlocfilehash: 1c19ba94588628e002cdb9e65f59bd4182020e1c
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888707"
---
# <a name="add-context-menu-to-power-bi-visual"></a>เพิ่มเมนูบริบทไปยัง Power BI Visual

คุณสามารถใช้ `selectionManager.showContextMenu()`กับพารามิเตอร์ `selectionId`และตำแหน่ง (เป็นวัตถุ `{x:, y:}`) เพื่อให้ Power BI แสดงเมนูบริบทสำหรับการแสดงผลด้วยภาพของคุณได้

> [!IMPORTANT]
> `selectionManager.showContextMenu()`ได้รับการแนะนำใน Visuals API 1.7.0

โดยทั่วไปแล้วจะถูกเพิ่มเป็นการ "คลิกขวา" ที่เหตุการณ์ (หรือ "แตะ" สำหรับอุปกรณ์สัมผัส) ที่มีการเพิ่มเมนูบริบทในตัวอย่าง BarChart สำหรับการอ้างอิง:

```typescript
    public update(options: VisualUpdateOptions) {
        //...
        //handle context menu
        this.svg.on('contextmenu', () => {
            const mouseEvent: MouseEvent = d3.event as MouseEvent;
            const eventTarget: EventTarget = mouseEvent.target;
            let dataPoint = d3.select(eventTarget).datum();
            this.selectionManager.showContextMenu(dataPoint? dataPoint.selectionId : {}, {
                x: mouseEvent.clientX,
                y: mouseEvent.clientY
            });
            mouseEvent.preventDefault();
        });
```
