---
title: เรียนรู้วิธีการพัฒนาวิชวล Power BI ของคุณเองโดยใช้วิชวลการ์ดวงกลมเป็นตัวอย่างในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทช่วยสอนนี้จะอธิบายวิธีการที่คุณสามารถพัฒนาวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: tutorial
ms.date: 09/02/2020
ms.openlocfilehash: 0bfc36a37dbcc4c595ea467eb3b365c30d4ed781
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97885648"
---
# <a name="tutorial-develop-a-power-bi-circle-card-visual"></a>บทช่วยสอน: พัฒนาวิชวลการ์ดวงกลม Power BI

ในฐานะนักพัฒนาคุณสามารถสร้างวิชวล Power BI ของคุณเองได้ ภาพเหล่านี้สามารถใช้โดยคุณองค์กรของคุณหรือบุคคลที่สามได้

ในบทช่วยสอนนี้คุณจะพัฒนาการแสดงผลด้วยภาพของ Power BI ที่ชื่อว่าการ์ดวงกลมที่แสดงค่าหน่วยวัดที่จัดรูปแบบภายในวงกลม วิชวลการ์ดวงกลมสนับสนุนการกำหนดเองของสีเติมและความหนาของเส้นขอบ

ในบทช่วยสอนนี้ คุณจะเรียนรู้วิธีการ:
> [!div class="checklist"]
> * สร้างโครงการการพัฒนาสำหรับวิชวลของคุณ
> * พัฒนาวิชวลของคุณด้วยองค์ประกอบภาพ D3
> * กำหนดค่าวิชวลของคุณเพื่อประมวลผลข้อมูล

## <a name="prerequisites"></a>สิ่งที่จำเป็นต้องมี

ก่อนที่คุณจะเริ่มพัฒนาวิชวล Power BI ของคุณให้ตรวจสอบว่าคุณมีทุกอย่างที่แสดงอยู่ในส่วนนี้

* คุณจำเป็นต้องมีบัญชี **Power BI Pro** ถ้าคุณยังไม่มี [ลงทะเบียนสำหรับ](https://powerbi.microsoft.com/pricing/)รุ่นทดลองใช้ฟรี

* [ รหัส Visual Studio (VS Code)](https://www.visualstudio.com/) VS Code คือสภาพแวดล้อมการพัฒนาแบบบูรณาการที่เหมาะสม (IDE) สำหรับการพัฒนาแอปพลิเคชัน JavaScript และ TypeScript

* [Windows PowerShell](/powershell/scripting/install/installing-windows-powershell) เวอร์ชัน4หรือใหม่กว่า (สำหรับ Windows) [Terminal](https://macpaw.com/how-to/use-terminal-on-mac) (สำหรับ OSX)

* สภาพแวดล้อมที่พร้อมสำหรับการพัฒนาวิชวล Power BI [ตั้งค่าสภาพแวดล้อมของคุณสำหรับการพัฒนา](environment-setup.md)วิชวล Power BI

* บทช่วยสอนนี้ใช้รายงาน **การวิเคราะห์การขายของสหรัฐอเมริกา** คุณสามารถ [ดาวน์โหลด](https://microsoft.github.io/PowerBI-visuals/docs/step-by-step-lab/images/US_Sales_Analysis.pbix) รายงานนี้และอัปโหลดไปยังบริการของ Power BI หรือใช้รายงานของคุณเองได้ หากคุณต้องการข้อมูลเพิ่มเติมเกี่ยวกับการบริการของ Power BI และการอัปโหลดไฟล์โปรดดูที่ [เริ่มต้นสร้างในบทช่วยสอน](../../fundamentals/service-get-started.md) บริการของ Power BI

## <a name="create-a-development-project"></a>สร้างโครงการการพัฒนา

ในส่วนนี้คุณจะสร้างโครงการสำหรับการแสดงผลด้วยภาพของการ์ดวงกลม

1. เปิด PowerShell และนำทางไปยังโฟลเดอร์ที่คุณต้องการสร้างโครงการของคุณ

2. ป้อนคำสั่งต่อไปนี้:

    ```PowerShell
    pbiviz new CircleCard
    ```

3. นำทางไปยังโฟลเดอร์ของโครงการ

    ```powershell
    cd CircleCard
    ```

4. เริ่มการแสดงผลด้วยภาพของการ์ดวงกลม ขณะนี้วิชวลของคุณกำลังทำงานอยู่ในขณะที่โฮสต์บนคอมพิวเตอร์ของคุณ

    ```powershell
    pbiviz start
    ```
    >[!IMPORTANT]
    >อย่าปิดหน้าต่าง PowerSell จนกว่าจะถึงตอนท้ายของบทช่วยสอน เมื่อต้องการหยุดการแสดงผลด้วยภาพให้ใส่ Ctrl + C และถ้าได้รับพร้อมท์ให้สิ้นสุดชุดงานให้ป้อน Y และกด *ใส่*

## <a name="view-the-circle-card-in-power-bi-service"></a>ดูการ์ดวงกลมในบริการของ Power BI

ในการทดสอบการแสดงผลด้วยภาพของการ์ดวงกลมในบริการของ Power BI เราจะใช้รายงานการวิเคราะห์การขายของ **สหรัฐ** คุณสามารถ [ดาวน์โหลด](https://microsoft.github.io/PowerBI-visuals/docs/step-by-step-lab/images/US_Sales_Analysis.pbix) รายงานนี้และอัปโหลดไปยังบริการของ Power BI ได้

คุณยังสามารถใช้รายงานของคุณเองเพื่อทดสอบการแสดงผลด้วยภาพของการ์ดวงกลม

>[!NOTE]
>ก่อนที่คุณจะดำเนินการต่อให้ตรวจสอบว่าคุณ [เปิดใช้งานการตั้งค่านักพัฒนาวิชวล](environment-setup.md#set-up-power-bi-service-for-developing-a-visual)

1. ลงชื่อเข้าใช้ [PowerBI.com](https://powerbi.microsoft.com/) และเปิดรายงาน **การวิเคราะห์การขาย** สหรัฐ

2. เลือก **ตัวเลือกเพิ่มเติม** > **แก้ไข**

    >[!div class="mx-imgBorder"]
    >![สกรีนช็อตของตัวเลือกการแก้ไขในบริการ Power B I](media/develop-circle-card/edit-report.png)

3. สร้างหน้าใหม่สำหรับการทดสอบโดยการคลิกที่ปุ่ม **หน้าใหม่** ที่ด้านล่างของส่วนติดต่อบริการของ Power BI

    >[!div class="mx-imgBorder"]
    >![สกรีนช็อตของปุ่มหน้าใหม่ในบริการ Power B I](media/develop-circle-card/new-page.png)

4. จากบานหน้าต่าง **การแสดงภาพ** ให้เลือก **วิชวลของนักพัฒนา**

    >[!div class="mx-imgBorder"]
    >![สกรีนช็อตของวิชวลของนักพัฒนาในบานหน้าต่างการแสดงภาพ](media/develop-circle-card/developer-visual.png)

    ภาพนี้แสดงการแสดงผลด้วยภาพแบบกำหนดเองที่คุณกำลังใช้งานบนคอมพิวเตอร์ของคุณ พร้อมใช้งานเฉพาะเมื่อเปิดใช้งานการตั้งค่าการ [การตรวจแก้จุดบกพร่องของวิชวลแบบกำหนดเอง](environment-setup.md#set-up-power-bi-service-for-developing-a-visual)

5. ตรวจสอบว่ามีการเพิ่มวิชวลลงในพื้นที่รายงาน

    >[!div class="mx-imgBorder"]
    >![สกรีนช็อตของวิชวลใหม่ที่เพิ่มลงในรายงาน](media/develop-circle-card/new-visual.png)

    นี่เป็นวิชวลแบบง่าย ๆ ที่แสดงจำนวนครั้งที่มีการเรียกใช้วิธีการอัปเดต ในขั้นตอนนี้ วิชวลยังไม่ได้เรียกข้อมูลใด

    >[!NOTE]
    >หากภาพแสดงข้อความแสดงข้อผิดพลาดในการเชื่อมต่อให้เปิดแท็บใหม่ในเบราว์เซอร์ของคุณไปที่ `https://localhost:8080/assets/status` และอนุญาตให้เบราว์เซอร์ของคุณใช้ที่อยู่นี้
    >
    >![สกรีนช็อตของวิชวลใหม่ที่แสดงข้อผิดพลาดในการเชื่อมต่อ](media/develop-circle-card/connection-error.png)

6. ในขณะที่เลือกภาพใหม่ให้ไปที่บานหน้าต่าง **เขตข้อมูล** ขยาย **ยอดขาย** และเลือก **ปริมาณ**

    >[!div class="mx-imgBorder"]
    >![สกรีนช็อตของเขตข้อมูลปริมาณบริการ Power B I ในตารางการขายในรายงานการวิเคราะห์การขายของสหรัฐอเมริกา](media/develop-circle-card/fields-sales-quantity.png)

7. หากต้องการทดสอบการตอบสนองของภาพให้ปรับขนาดและสังเกตว่าค่า *อัปเดตจำนวน* จะเพิ่มขึ้นทุกครั้งที่คุณปรับขนาดวิชวล

    >[!div class="mx-imgBorder"]
    >![สกรีนช็อตของวิชวลใหม่ที่แสดงจำนวนการอัปเดตที่แตกต่างกันหลังจากปรับขนาดแล้ว](media/develop-circle-card/resized-visual.png)

## <a name="add-visual-elements-and-text"></a>เพิ่มองค์ประกอบวิชวลและข้อความ

ในส่วนนี้ คุณจะได้เรียนรู้วิธีเปลี่ยนวิชวลของคุณให้เป็นวงกลมและทำให้แสดงข้อความ

>[!NOTE]
>ในบทช่วยสอนนี้ [รหัส Visual Studio](https://code.visualstudio.com/) (VS Code) ใช้สำหรับการพัฒนาวิชวลของ Power BI

### <a name="modify-the-visuals-file"></a>ปรับเปลี่ยนไฟล์วิชวล

ตั้งค่าไฟล์ **visual.ts** โดยการลบและเพิ่มรหัสสองสามบรรทัด

1. เปิดโปรเจกต์ของคุณใน VS Code (**ไฟล์**  >  **เปิดโฟลเดอร์**)

2. ใน **บานหน้าต่าง Explorer** ขยายโฟลเดอร์ **src** และเลือกไฟล์ **visual.ts**

    >[!div class="mx-imgBorder"]
    >![สกรีนช็อตของการเข้าถึงไฟล์ visual.ts ในรหัส V S](media/develop-circle-card/visual-file.png)

    > [!IMPORTANT]
    > สังเกตดูข้อคิดเห็นที่ด้านบนของไฟล์ **visual.ts** การอนุญาตให้ใช้แพคเกจวิชวล Power BI จะได้รับโดยไม่เสียค่าใช้จ่ายภายใต้เงื่อนไขของสิทธิ์การใช้งานของสถาบันเทคโนโลยีแมสซาชูเซตส์ (MIT) คุณต้องออกจากข้อคิดเห็นที่ด้านบนของไฟล์ ตามส่วนหนึ่งของข้อตกลง

3. ลบบรรทัดโค้ดต่อไปนี้ออกจากไฟล์ *visual.ts*

    * การนำเข้า *VisualSettings*:
        ```typescript
        import { VisualSettings } from "./settings";
        ```

    * การยืนยันตัวแปรส่วนตัวระดับคลาสทั้งสี่ครั้ง

    * ทุกบรรทัดของรหัสภายใน *คอนสตรักเตอร์*

    * ทุกบรรทัดของรหัสภายในวิธี *การอัปเดต*

    * บรรทัดโค้ดที่เหลือทั้งหมดใต้วิธี *อัปเดต* รวมถึงวิธี *parseSettings* และ *enumerateObjectInstances*

4. เพิ่มบรรทัดรหัสต่อไปนี้ที่ส่วนท้ายของส่วนการนำเข้า:

    * *IVisualHost* - คอลเลกชันของคุณสมบัติและบริการที่ใช้ในการโต้ตอบกับโฮสต์ภาพ (Power BI)

         ```typescript
        import IVisualHost = powerbi.extensibility.IVisualHost;
        ```

    * *ไลบรารี D3*

        ```typescript
        import * as d3 from "d3";
        type Selection<T extends d3.BaseType> = d3.Selection<T, any,any, any>;
        ```
    
        >[!NOTE]
        >หากคุณไม่ได้ติดตั้งไลบรารีนี้เป็นส่วนหนึ่งของการตั้งค่าของคุณให้ [ติดตั้งไลบรารี D3 JavaScript](environment-setup.md#d3-javascript-library)

5. ภายใต้การประกาศคลาส *วิชวล* ให้แทรกคุณสมบัติระดับคลาสต่อไปนี้ คุณต้องเพิ่มบรรทัดรหัสที่ขึ้นต้นด้วย `private`

    ```typescript
    export class Visual implements IVisual {
        // ...
        private host: IVisualHost;
        private svg: Selection<SVGElement>;
        private container: Selection<SVGElement>;
        private circle: Selection<SVGElement>;
        private textValue: Selection<SVGElement>;
        private textLabel: Selection<SVGElement>;
        // ...
    }
    ```

6. บันทึกไฟล์ **visual.ts**

### <a name="add-a-circle-and-text-elements"></a>เพิ่มองค์ประกอบวงกลมและข้อความ

เพิ่มกราฟิกเวกเตอร์ D3 ที่ปรับขนาดได้ (SVG) ซึ่งเปิดใช้งานการสร้างรูปร่างสามแบบ: วงกลมและสององค์ประกอบข้อความ

1. เปิด **visual.ts** ในรหัส VS

2. เพิ่มรหัสต่อไปนี้ไปยัง *คอนสตรักเตอร์*

    ```typescript
    this.svg = d3.select(options.element)
        .append('svg')
        .classed('circleCard', true);
    this.container = this.svg.append("g")
        .classed('container', true);
    this.circle = this.container.append("circle")
        .classed('circle', true);
    this.textValue = this.container.append("text")
        .classed("textValue", true);
    this.textLabel = this.container.append("text")
        .classed("textLabel", true);
    ```

    >[!TIP]
    >เพื่อปรับปรุงความสามารถในการอ่าน ขอแนะนำให้คุณจัดรูปแบบเอกสารทุกครั้งที่คุณคัดลอกข้อมูลโค้ดลงในโปรเจกต์ของคุณ คลิกขวาที่ใดก็ได้ในรหัส VS แล้วเลือก *จัดรูปแบบเอกสาร* (Alt+Shift+F)

3. บันทึกไฟล์ **visual.ts**

### <a name="set-the-width-and-height"></a>ตั้งค่าความกว้างและความสูง

ตั้งค่าความกว้างและความสูงของวิชวลและเริ่มต้นแอตทริบิวต์และสไตล์ขององค์ประกอบของวิชวล

1. เปิด **visual.ts** ในรหัส VS

2. เพิ่มรหัสต่อไปนี้ไปยังวิธี *อัปเดต*

    ```typescript
    let width: number = options.viewport.width;
    let height: number = options.viewport.height;
    this.svg.attr("width", width);
    this.svg.attr("height", height);
    let radius: number = Math.min(width, height) / 2.2;
    this.circle
        .style("fill", "white")
        .style("fill-opacity", 0.5)
        .style("stroke", "black")
        .style("stroke-width", 2)
        .attr("r", radius)
        .attr("cx", width / 2)
        .attr("cy", height / 2);
    let fontSizeValue: number = Math.min(width, height) / 5;
    this.textValue
        .text("Value")
        .attr("x", "50%")
        .attr("y", "50%")
        .attr("dy", "0.35em")
        .attr("text-anchor", "middle")
        .style("font-size", fontSizeValue + "px");
    let fontSizeLabel: number = fontSizeValue / 4;
    this.textLabel
        .text("Label")
        .attr("x", "50%")
        .attr("y", height / 2)
        .attr("dy", fontSizeValue / 1.2)
        .attr("text-anchor", "middle")
        .style("font-size", fontSizeLabel + "px");
    ```

3. บันทึกไฟล์ **visual.ts**

### <a name="optional-review-the-code-in-the-visuals-file"></a>(ไม่จำเป็น) รีวิวรหัสในไฟล์วิชวล

ตรวจสอบว่าโค้ดในไฟล์ *visuals.ts* มีลักษณะดังนี้:

```typescript
/*
*  Power BI Visual CLI
*
*  Copyright (c) Microsoft Corporation
*  All rights reserved.
*  MIT License
*
*  Permission is hereby granted, free of charge, to any person obtaining a copy
*  of this software and associated documentation files (the ""Software""), to deal
*  in the Software without restriction, including without limitation the rights
*  to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
*  copies of the Software, and to permit persons to whom the Software is
*  furnished to do so, subject to the following conditions:
*
*  The above copyright notice and this permission notice shall be included in
*  all copies or substantial portions of the Software.
*
*  THE SOFTWARE IS PROVIDED *AS IS*, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
*  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
*  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
*  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
*  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
*  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
*  THE SOFTWARE.
*/
"use strict";

import "core-js/stable";
import "./../style/visual.less";
import powerbi from "powerbi-visuals-api";
import VisualConstructorOptions = powerbi.extensibility.visual.VisualConstructorOptions;
import VisualUpdateOptions = powerbi.extensibility.visual.VisualUpdateOptions;
import IVisual = powerbi.extensibility.visual.IVisual;
import EnumerateVisualObjectInstancesOptions = powerbi.EnumerateVisualObjectInstancesOptions;
import VisualObjectInstance = powerbi.VisualObjectInstance;
import DataView = powerbi.DataView;
import VisualObjectInstanceEnumerationObject = powerbi.VisualObjectInstanceEnumerationObject;
import IVisualHost = powerbi.extensibility.IVisualHost;
import * as d3 from "d3";
type Selection<T extends d3.BaseType> = d3.Selection<T, any, any, any>;

export class Visual implements IVisual {
    private host: IVisualHost;
    private svg: Selection<SVGElement>;
    private container: Selection<SVGElement>;
    private circle: Selection<SVGElement>;
    private textValue: Selection<SVGElement>;
    private textLabel: Selection<SVGElement>;

    constructor(options: VisualConstructorOptions) {
        this.svg = d3.select(options.element)
            .append('svg')
            .classed('circleCard', true);
        this.container = this.svg.append("g")
            .classed('container', true);
        this.circle = this.container.append("circle")
            .classed('circle', true);
        this.textValue = this.container.append("text")
            .classed("textValue", true);
        this.textLabel = this.container.append("text")
            .classed("textLabel", true);
    }

    public update(options: VisualUpdateOptions) {
        let width: number = options.viewport.width;
        let height: number = options.viewport.height;
        this.svg.attr("width", width);
        this.svg.attr("height", height);
        let radius: number = Math.min(width, height) / 2.2;
        this.circle
            .style("fill", "white")
            .style("fill-opacity", 0.5)
            .style("stroke", "black")
            .style("stroke-width", 2)
            .attr("r", radius)
            .attr("cx", width / 2)
            .attr("cy", height / 2);
        let fontSizeValue: number = Math.min(width, height) / 5;
        this.textValue
            .text("Value")
            .attr("x", "50%")
            .attr("y", "50%")
            .attr("dy", "0.35em")
            .attr("text-anchor", "middle")
            .style("font-size", fontSizeValue + "px");
        let fontSizeLabel: number = fontSizeValue / 4;
        this.textLabel
            .text("Label")
            .attr("x", "50%")
            .attr("y", height / 2)
            .attr("dy", fontSizeValue / 1.2)
            .attr("text-anchor", "middle")
            .style("font-size", fontSizeLabel + "px");
    }
}
```

### <a name="modify-the-capabilities-file"></a>ปรับเปลี่ยนไฟล์ความสามารถ

ลบบรรทัดรหัสที่ไม่จำเป็นออกจากไฟล์ความสามารถ

1. เปิดโปรเจกต์ของคุณใน VS Code (**ไฟล์**  >  **เปิดโฟลเดอร์**)

2. บันทึกไฟล์ **capabilities.json**

    >[!div class="mx-imgBorder"]
    >![สกรีนช็อตของการเข้าถึงไฟล์ capabilities.json ในรหัส V S ](media/develop-circle-card/capabilities-file.png)

3. ลบองค์ประกอบวัตถุทั้งหมด (บรรทัดที่ 14-60)

4. บันทึกไฟล์ **capabilities.json**

### <a name="restart-the-circle-card-visual"></a>รีสตาร์ตวิชวลการ์ดวงกลม

หยุดวิชวลจากการเรียกใช้และรีสตาร์ต

1. ในหน้าต่าง PowerShell ที่เรียกใช้วิชวลให้ป้อน Ctrl + C และหากได้รับแจ้งให้ยุติงานแบตช์ให้ป้อน Y แล้วกด *Enter*

2. เริ่มวิชวล ใน PowerShell

    ```powershell
    pbiviz start
    ```

### <a name="test-the-visual-with-the-added-elements"></a>ทดสอบวิชวลด้วยองค์ประกอบที่เพิ่มเข้ามา

ตรวจสอบว่าวิชวลแสดงองค์ประกอบที่เพิ่มใหม่

1. ในบริการ Power BI เปิดรายงาน *การวิเคราะห์การขาย Power BI ของสหรัฐอเมริกา* หากคุณใช้รายงานอื่นเพื่อพัฒนาวิชวลการ์ดวงกลมให้ไปที่รายงานนั้น

2. ตรวจสอบให้แน่ใจว่าวิชวลเป็นรูปวงกลม

    >[!div class="mx-imgBorder"]
    >![สกรีนช็อตของวิชวลการ์ดวงกลมรูปภาพเป็นวงกลม](media/develop-circle-card/circle.png)

    >[!NOTE]
    >หากวิชวลไม่แสดงอะไรเลยจากบานหน้าต่าง **เขตข้อมูล** ลากเขตข้อมูล **ปริมาณ** ลงในวิชวลของนักพัฒนา

3. ปรับขนาดวิชวล

    สังเกตว่าวงกลมและขนาดข้อความจะพอดีกับขนาดของวิชวล วิธีการอัปเดตจะถูกเรียกเมื่อคุณปรับขนาดวิชวลและด้วยเหตุนี้องค์ประกอบวิชวลจึงถูกปรับขนาด

### <a name="enable-auto-reload"></a>เปิดใช้งานการโหลดซ้ำอัตโนมัติ

ใช้การตั้งค่านี้เพื่อให้แน่ใจว่าวิชวลถูกโหลดซ้ำโดยอัตโนมัติทุกครั้งที่คุณบันทึกการเปลี่ยนแปลงโปรเจกต์

1. ไปที่รายงาน *การวิเคราะห์การขาย Power BI ของสหรัฐอเมริกา* (หรือไปยังโครงการที่มีวิชวลการ์ดวงกลมของคุณ)

2. เลือกวิชวลการ์ดวงกลม

3. ในแถบเครื่องมือแบบลอยให้เลือก **สลับการโหลดอัตโนมัติ**

    >[!div class="mx-imgBorder"]
    >![สกรีนช็อตของการคลิกตัวเลือกสลับการโหลดอัตโนมัติในแถบเครื่องมือการแสดงวิชวลการ์ดวงกลม](media/develop-circle-card/toggle-auto-reload.png)

## <a name="get-the-visual-to-process-data"></a>รับวิชวลเพื่อประมวลผลข้อมูล

ในส่วนนี้ คุณจะกำหนดบทบาทข้อมูลและการแมปมุมมองข้อมูล นอกจากนี้คุณยังจะปรับเปลี่ยนวิชวลเพื่อแสดงชื่อของค่าที่แสดง

### <a name="configure-the-capabilities-file"></a>กำหนดค่าไฟล์ความสามารถ

ปรับเปลี่ยนไฟล์ **capabilities.json** เพื่อกำหนดบทบาทข้อมูลและการแมปมุมมองข้อมูล

* **การกำหนดบทบาทข้อมูล**

    กำหนดอาร์เรย์ *dataRoles* ที่มีบทบาทข้อมูลเดียวของชนิด *หน่วยวัด* บทบาทข้อมูลนี้เรียกว่า *หน่วยวัด* และแสดงเป็น *หน่วยวัด* อนุญาตให้ส่งผ่านเขตข้อมูลการวัดหรือเขตข้อมูลที่สรุปได้

    1. เปิดไฟล์ **capabilities.json** ใน VS Code

    2. ลบเนื้อหาทั้งหมดภายในอาร์เรย์ **dataRoles** (บรรทัด 3-12)

    3. แทรกรหัสต่อไปนี้ในอาร์เรย์ **dataRoles**

        ```json
        {
            "displayName": "Measure",
            "name": "measure",
            "kind": "Measure"
        }
        ```

    4. บันทึกไฟล์ **capabilities.json**

* **การกำหนดการแมปมุมมองข้อมูล**

    กำหนดไฟล์ที่เรียกว่า *หน่วยวัด* ในอาร์เรย์ *dataViewMappings* เขตข้อมูลนี้สามารถส่งผ่านไปยังบทบาทข้อมูล

    1. เปิดไฟล์ **capabilities.json** ใน VS Code

    2. ลบเนื้อหาทั้งหมดภายในอาร์เรย์ **dataViewMappings** (บรรทัดที่ 10-30)

    3. แทรกรหัสต่อไปนี้ในอาร์เรย์ **dataViewMappings**

        ```json
        {
            "conditions": [
                { "measure": { "max": 1 } }
            ],
            "single": {
                "role": "measure"
            }
        }
        ```

    4. บันทึกไฟล์ **capabilities.json**

### <a name="optional-review-the-capabilities-file-code-changes"></a>(ไม่จำเป็น) ตรวจสอบการเปลี่ยนแปลงรหัสไฟล์ความสามารถ

ตรวจสอบว่าวิชวลของการ์ดวงกลมแสดงเขตข้อมูล *หน่วยวัด* และตรวจสอบการเปลี่ยนแปลงที่คุณทำโดยใช้ตัวเลือก *แสดง Dataview* 

1. ในบริการ Power BI เปิดรายงาน *การวิเคราะห์การขาย Power BI ของสหรัฐอเมริกา* หากคุณใช้รายงานอื่นเพื่อพัฒนาวิชวลการ์ดวงกลมให้ไปที่รายงานนั้น

2. สังเกตว่าขณะนี้ภาพการ์ดวงกลมสามารถกำหนดค่าด้วยเขตข้อมูลที่ชื่อ *หน่วยวัด* คุณสามารถลากและวางองค์ประกอบจากบานหน้าต่าง **เขตข้อมูล** ลงในเขตข้อมูล *หน่วยวัด*

    >[!div class="mx-imgBorder"]
    >![สกรีนช็อตของการวัดการ์ดวงกลมที่ยื่นในบานหน้าต่างการแสดงภาพบริการของ Power BI](media/develop-circle-card/measure.png)

    > [!Note]
    > โครงการวิชวลยังไม่ได้รวมตรรกะการผูกข้อมูลเอาไว้

3. ในแถบเครื่องมือลอยให้เลือก **แสดงมุมมองข้อมูล** 

    >[!div class="mx-imgBorder"]
    >![สกรีนช็อตของปุ่มแสดงข้อมูลที่อยู่ในแถบเครื่องมือแบบลอยของการ์ดวงกลม](media/develop-circle-card/show-dataview.png)

4. เลือกจุดสามจุดเพื่อขยายการแสดงผลและเลือก **แบบเดี่ยว** เพื่อดูค่า

    >[!div class="mx-imgBorder"]
    >![สกรีนช็อตของรูปค่าตามที่แสดงในการ์ดวงกลมแสดงตัวเลือกมุมมองข้อมูล](media/develop-circle-card/value.png)

5. ขยาย **เมตาดาต้า** ตามด้วยอาร์เรย์ **คอลัมน์** และตรวจสอบค่า **รูปแบบ** และ **displayName**

    >[!div class="mx-imgBorder"]
    >![สกรีนช็อตของรูปแบบและค่าชื่อที่แสดงในการ์ดวงกลมแสดงตัวเลือกมุมมองข้อมูล](media/develop-circle-card/colunms.png)

6. เมื่อต้องการสลับกลับไปที่วิชวล ในแถบเครื่องมือที่ลอยอยู่เหนือวิชวล ให้เลือก **แสดงมุมมองข้อมูล**

### <a name="configure-the-visual-to-consume-data"></a>กำหนดค่าวิชวลเพื่อใช้ข้อมูล

ทำการเปลี่ยนแปลงไฟล์ **visual.ts** เพื่อให้วิชวลการ์ดวงกลมสามารถใช้ข้อมูลได้

1. เปิดไฟล์ **visual.ts** ใน VS Code

2. เพิ่มบรรทัดต่อไปนี้เพื่อนำเข้า `DataView`อินเทอร์เฟซจาก`powerbi` โมดูล

    ```typescript
    import DataView = powerbi.DataView;
    ```

3. ในวิธีการ *อัปเดต* ให้ดำเนินการดังต่อไปนี้:

    * เพิ่มคำสั่งต่อไปนี้เป็นคำสั่งแรก คำสั่งกำหนด *มุมมองข้อมูล* ให้กับตัวแปรเพื่อให้เข้าถึงได้ง่ายและประกาศให้ตัวแปรอ้างอิงออบเจ็กต์ *มุมมองข้อมูล*

        ```typescript
        let dataView: DataView = options.dataViews[0];
        ```

    * แทนที่ **.text ("Value")** ด้วยโค้ดบรรทัดนี้:

        ```typescript
        .text(<string>dataView.single.value)
        ```

    * แทนที่ **.text("Label")** ด้วยโค้ดบรรทัดนี้:

        ```typescript
        .text(dataView.metadata.columns[0].displayName)
        ```

4. บันทึกไฟล์ **visual.ts**

5. ตรวจสอบวิชวลในบริการ Power BI ขณะนี้วิชวลแสดงค่าและชื่อที่แสดง

## <a name="next-steps"></a>ขั้นตอนถัดไป

> [!div class="nextstepaction"]
> [เพิ่มตัวเลือกการจัดรูปแบบไปยังวิชวลการ์ดวงกลม](custom-visual-develop-tutorial-format-options.md)

> [!div class="nextstepaction"]
> [สร้างวิชวลแผนภูมิแท่ง Power BI](create-bar-chart.md)

> [!div class="nextstepaction"]
> [เรียนรู้วิธีการดีบักภาพ Power BI ที่คุณสร้างขึ้น](visuals-how-to-debug.md)

> [!div class="nextstepaction"]
> [โครงสร้างของโครงการวิชวล Power BI](visual-project-structure.md)
