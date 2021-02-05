---
title: ดึงข้อมูลเพิ่มเติมจาก Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายถึงวิธีการเปิดใช้งานการดึงชุดข้อมูลขนาดใหญ่เป็นเซกเมนต์สำหรับวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: how-to
ms.date: 12/13/2020
ms.openlocfilehash: 345efe91be1af5ee61d713c576f04657b182ad47
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97886315"
---
# <a name="fetch-more-data-from-power-bi"></a>ดึงข้อมูลเพิ่มเติมจาก Power BI

`fetchMoreData`API ช่วยให้วิชวล Power BI สามารถข้ามขีดจำกัดที่ยากลำบากในการดูข้อมูลแถว 30K ได้ ด้วยการเปิดตัว 3.4 API ใหม่ `fetchMoreData`ฟังก์ชันการทำงานของ API จะขยายเพื่อรองรับวิธีการใหม่ ๆ ในการโหลดกลุ่มข้อมูล นอกเหนือจากวิธีการที่มีอยู่ ซึ่งจะรวมกลุ่มทั้งหมดที่ร้องขอด้วย API จะสนับสนุนการโหลดเฉพาะกลุ่มข้อมูลส่วนเพิ่ม

วิธีการใหม่ช่วยเพิ่มความยืดหยุ่นมากขึ้นในวิธีโหลดกลุ่มข้อมูลเพิ่มเติมไปยังวิชวล เพื่อปรับปรุงประสิทธิภาพการทำงาน คุณสามารถกำหนดขนาดกลุ่มเพื่อรองรับกรณีการใช้งานของคุณได้

## <a name="limitations-of-fetchmoredata"></a>ขีดจำกัดของ fetchMoreData

* ขนาดระยะห่างจำกัดไว้ที่ช่วง 2 ถึง 30,000
* จำนวนแถวทั้งหมดของดาต้าวิวถูกจำกัดไว้ที่ 1,048,576 แถว
* ในโหมดการรวมเซกเมนต์ ขนาดหน่วยความจำของดาต้าวิวถูกจำกัดไว้ที่ 100 MB

## <a name="enable-a-segmented-fetch-of-large-datasets"></a>เปิดใช้งานการดึงชุดข้อมูลขนาดใหญ่เป็นเซกเมนต์

สำหรับโหมดเซกเมนต์ `dataview` คุณกำหนดขนาดหน้าต่างสำหรับ `dataReductionAlgorithm` ในไฟล์ *capabilities.json* ของวิชวลสำหรับ `dataViewMapping` ที่ต้องการ `count` กำหนดขนาดหน้าต่างซึ่งจำกัดจำนวนแถวข้อมูลใหม่ที่สามารถผนวกเข้ากับ `dataview` ในแต่ละการอัปเดต

เพิ่มโค้ดต่อไปนี้ในไฟล์ *capabilities.json*:

```typescript
"dataViewMappings": [
    {
        "table": {
            "rows": {
                "for": {
                    "in": "values"
                },
                "dataReductionAlgorithm": {
                    "window": {
                        "count": 100
                    }
                }
            }
    }
]
```

เซกเมนต์ใหม่จะถูกผนวกเข้า `dataview` ที่มีอยู่และจัดให้กับการแสดงภาพเป็นการโทร `update`

## <a name="usage-in-the-power-bi-visual"></a>การใช้งานในวิชวลของ Power BI

ใน Power BI คุณสามารถใช้ `fetchMoreData` ในโหมดการรวมเซกเมนต์ค่าเริ่มต้นหรือในโหมดการอัปเดตแบบเพิ่มหน่วยได้ 

### <a name="using-segments-aggregation-mode-default"></a>การใช้โหมดการรวมเซกเมนต์ (ค่าเริ่มต้น)

ด้วยโหมดนี้ดาต้าวิวที่จัดเตรียมให้กับวิชวลจะมีข้อมูลสะสมสำหรับ `fetchMoreData requests` ก่อนหน้านี้ทั้งหมด ดังนั้นจึงคาดว่าขนาดดาต้าวิวจะเพิ่มขึ้นในการอัปเดตแต่ละครั้ง ตัวอย่างเช่น หากคาดว่าจะมีทั้งหมด 100,000 แถวและขนาดระยะห่างถูกตั้งค่าไว้ที่ 10,000 ข้อมูลการอัปเดตดาต้าวิวครั้งแรกควรมี 10,000 แถว ข้อมูลการอัปเดตดาต้าวิวครั้งที่สองควรมี 20,000 แถว และเป็นอย่างนี้ต่อไปเรื่อย ๆ

โหมดนี้ถูกเลือกโดยการเรียก `fetchMoreData` ด้วย `aggregateSegments = true`

คุณสามารถตรวจสอบว่ามีข้อมูลอยู่หรือไม่โดยตรวจสอบการมีอยู่ของ `dataView.metadata.segment`:

```typescript
    public update(options: VisualUpdateOptions) {
        const dataView = options.dataViews[0];
        console.log(dataView.metadata.segment);
        // output: __proto__: Object
    }
```

นอกจากนี้คุณยังสามารถตรวจสอบเพื่อดูว่ามันเป็นการอัปเดตครั้งแรกหรือการอัปเดตที่ตามมาภายหลังโดยการตรวจสอบ `options.operationKind` ในโค้ดต่อไปนี้ `VisualDataChangeOperationKind.Create`อ้างถึงเซกเมนต์แรกและ`VisualDataChangeOperationKind.Append` อ้างถึงเซกเมนต์ที่ตามมาภายหลัง

สำหรับตัวอย่างการนำไปใช้งาน โปรดดูข้อมูลโค้ดต่อไปนี้:

```typescript
// CV update implementation
public update(options: VisualUpdateOptions) {
    // indicates this is the first segment of new data.
    if (options.operationKind == VisualDataChangeOperationKind.Create) {

    }

    // on second or subsequent segments:
    if (options.operationKind == VisualDataChangeOperationKind.Append) {

    }

    // complete update implementation
}
```

คุณยังสามารถเรียกใช้เมธอด `fetchMoreData` จากตัวจัดการเหตุการณ์ UI ดังที่แสดงไว้ที่นี่:

```typescript
btn_click(){
{
    // check if more data is expected for the current data view
    if (dataView.metadata.segment) {
        //request for more data if available; as a response, Power BI will call update method
        let request_accepted: bool = this.host.fetchMoreData(true);
        // handle rejection
        if (!request_accepted) {
            // for example, when the 100 MB limit has been reached
        }
    }
}
```

Power BI เรียกเมธอด `update` ของวิชวลด้วยเซกเมนต์ใหม่ของข้อมูลเพื่อตอบสนองต่อการเรียกใช้เมธอด `this.host.fetchMoreData`

> [!NOTE]
> เพื่อหลีกเลี่ยงข้อจำกัดของหน่วยความจำไคลเอนต์ ปัจจุบัน Power BI จำกัดข้อมูลที่ดึงมาทั้งหมดเป็น 100 MB คุณสามารถเห็นว่าถึงขีดจำกัดแล้วเมื่อ `fetchMoreData()` ส่งกลับ `false`

### <a name="using-incremental-updates-mode"></a>การใช้โหมดการอัปเดตแบบเพิ่มหน่วย

ด้วยโหมดนี้ดาต้าวิวที่กำหนดให้กับวิชวลจะมีเพียงข้อมูลที่เพิ่มขึ้น ดังนั้นขนาดดาต้าวิวจะไม่เลยขนาดระยะห่างที่กำหนด ตัวอย่างเช่น หากคาดว่าจะมีทั้งหมด 101,000 แถวและขนาดระยะห่างถูกตั้งค่าไว้ที่ 10,000 วิชวลจะได้รับการอัปเดต 10 รายการโดยมีขนาดข้อมูลเป็น 10,000 รายการ และการอัปเดตหนึ่งรายการที่มีดาต้าวิวขนาด 1,000

โหมดนี้ถูกเลือกโดยการเรียก `fetchMoreData` ด้วย `aggregateSegments = false`

คุณสามารถตรวจสอบว่ามีข้อมูลอยู่หรือไม่โดยตรวจสอบการมีอยู่ของ `dataView.metadata.segment`:

```typescript
    public update(options: VisualUpdateOptions) {
        const dataView = options.dataViews[0];
        console.log(dataView.metadata.segment);
        // output: __proto__: Object
    }
```

นอกจากนี้คุณยังสามารถตรวจสอบเพื่อดูว่ามันเป็นการอัปเดตครั้งแรกหรือการอัปเดตที่ตามมาภายหลังโดยการตรวจสอบ `options.operationKind` ในโค้ดต่อไปนี้ `VisualDataChangeOperationKind.Create`อ้างถึงเซกเมนต์แรกและ`VisualDataChangeOperationKind.Segment` อ้างถึงเซกเมนต์ที่ตามมาภายหลัง

สำหรับตัวอย่างการนำไปใช้งาน โปรดดูข้อมูลโค้ดต่อไปนี้:

```typescript
// CV update implementation
public update(options: VisualUpdateOptions) {
    // indicates this is the first segment of new data.
    if (options.operationKind == VisualDataChangeOperationKind.Create) {

    }

    // on second or subsequent segments:
    if (options.operationKind == VisualDataChangeOperationKind.Segment) {
        
    }

    // skip overlapping rows 
    const rowOffset = (dataView.table['lastMergeIndex'] === undefined) ? 0 : dataView.table['lastMergeIndex'] + 1;

    // Process incoming data
    for (var i = rowOffset; i < dataView.table.rows.length; i++) {
        var val = <number>(dataView.table.rows[i][0]); // Pick first column               
            
     }
     
    // complete update implementation
}
```

คุณยังสามารถเรียกใช้เมธอด `fetchMoreData` จากตัวจัดการเหตุการณ์ UI ดังที่แสดงไว้ที่นี่:

```typescript
btn_click(){
{
    // check if more data is expected for the current data view
    if (dataView.metadata.segment) {
        //request for more data if available; as a response, Power BI will call update method
        let request_accepted: bool = this.host.fetchMoreData(false);
        // handle rejection
        if (!request_accepted) {
            // for example, when the 100 MB limit has been reached
        }
    }
}
```

Power BI เรียกเมธอด `update` ของวิชวลด้วยเซกเมนต์ใหม่ของข้อมูลเพื่อตอบสนองต่อการเรียกใช้เมธอด `this.host.fetchMoreData`

> [!NOTE]
> แม้ว่าข้อมูลดาต้าวิวระหว่างการอัปเดตที่แตกต่างกันส่วนใหญ่จะเป็นข้อมูลเฉพาะ แต่จะมีการทับซ้อนกันระหว่างดาต้าวิวที่ตามมาในภายหลัง
> สำหรับการแมปข้อมูลแบบตารางและจัดกลุ่ม คาดว่าดาต้าวิว N แถวแรกจะมีข้อมูลที่คัดลอกมาจากดาต้าวิวก่อนหน้านี้
> N สามารถกำหนดได้จาก: `(dataView.table['lastMergeIndex'] === undefined) ? 0 : dataView.table['lastMergeIndex'] + 1`