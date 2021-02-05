---
title: API ของวิชวลในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการใช้ IVisual API สำหรับวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: reference
ms.date: 03/19/2020
ms.openlocfilehash: 7b81ecfa1b97b202b6c1ff306cf858f2ea00acde
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888546"
---
# <a name="visual-api"></a>API ของวิชวล
วิชวลทั้งหมดเริ่มต้นด้วย class ที่ใช้อินเทอร์เฟซ `IVisual` คุณสามารถตั้งชื่อ class เป็นอะไรก็ได้ตราบใดที่มีหนึ่ง class ที่ใช้อินเทอร์เฟซ `IVisual`

> [!NOTE]
> ชื่อ class วิชวลต้องตรงกับที่กำหนดไว้ในไฟล์ *pbiviz.json*

ดู class วิชวลตัวอย่างด้วยวิธีการต่อไปนี้ที่ควรนำมาใช้:

* `constructor` คอนสตรักเตอร์มาตรฐานเพื่อเริ่มต้นสถานะของวิชวล
* `update` เพื่ออัปเดตข้อมูลของวิชวล
* `enumerateObjectInstances` เพื่อส่งกลับวัตถุเพื่อเติมบานหน้าต่างคุณสมบัติ (ตัวเลือกการจัดรูปแบบ) ซึ่งคุณสามารถแก้ไขได้ตามต้องการ
* `destroy` ดีสตรักเตอร์มาตรฐานสำหรับการล้างข้อมูล

```typescript
class MyVisual implements IVisual {
    
    constructor(options: VisualConstructorOptions) {
        //one time setup code goes here (called once)
    }
    
    public update(options: VisualUpdateOptions): void {
        //code to update your visual goes here (called on all view or data changes)
    }

    public enumerateObjectInstances(options: EnumerateVisualObjectInstancesOptions): VisualObjectInstanceEnumeration {
        //returns objects to populate the property pane (called for each object defined in capabilities)
    }
    
    public destroy(): void {
        //one time cleanup code goes here (called once)
    }
}
```

## <a name="constructor"></a>คอนสตรักเตอร์

คอนสตรักเตอร์ของ class วิชวลจะถูกเรียกเมื่อมีการสร้างอินสแตนซ์ของวิชวล ซึ่งสามารถใช้สำหรับการตั้งค่าการดำเนินการใดๆ ที่จำเป็นต่อวิชวลได้

```typescript
constructor(options: VisualConstructorOptions)
```

**VisualConstructorOptions**

* `element: HTMLElement` การอ้างอิงไปยังองค์ประกอบ DOM ที่จะมีวิชวลของคุณอยู่
* `host: IVisualHost` คอลเลกชันของคุณสมบัติและบริการที่สามารถใช้เพื่อโต้ตอบกับโฮสต์วิชวล (Power BI)

   `IVisualHost` ประกอบด้วยบริการต่อไปนี้:

   ```typescript
   export interface IVisualHost extends extensibility.IVisualHost {
       createSelectionIdBuilder: () => visuals.ISelectionIdBuilder;
       : () => ISelectionManager;
       colorPalette: ISandboxExtendedColorPalette;
       persistProperties: (changes: VisualObjectInstancesToPersist) => void;
       applyJsonFilter: (filter: IFilter[] | IFilter, objectName: string, propertyName: string, action: FilterAction) => void;
       tooltipService: ITooltipService;
       telemetry: ITelemetryService;
       authenticationService: IAuthenticationService;
       locale: string;
       allowInteractions: boolean;
       launchUrl: (url: string) => void;
       fetchMoreData: () => boolean;
       instanceId: string;
       refreshHostData: () => void;
       createLocalizationManager: () => ILocalizationManager;
       storageService: ILocalVisualStorageService;
       eventService: IVisualEventService;
       switchFocusModeState: (on: boolean) => void;
   }
   ```
   * `createSelectionIdBuilder`สร้างและจัดเก็บเมตาดาต้าสำหรับรายการที่เลือกไว้ในวิชวลของคุณ
   * `createSelectionManager` สร้างบริดจ์การสื่อสารที่ใช้เพื่อแจ้งโฮสต์วิชวล เกี่ยวกับการเปลี่ยนแปลงในสถานะการเลือก ดู [การเลือก API](./selection-api.md)
   * `createLocalizationManager` สร้างผู้จัดการเพื่อช่วยในการ [การแปลเป็นภาษาท้องถิ่น](./localization.md)
   * `allowInteractions: boolean` ค่าสถานะบูลีนซึ่งให้คำแนะนำว่าควรมีการโต้ตอบของวิชวลหรือไม่
   * `applyJsonFilter` ใช้ชนิดตัวกรองเฉพาะ ดู [ตัวกรอง API](./filter-api.md)
   * `persistProperties` อนุญาตให้ผู้ใช้สามารถยืนยันคุณสมบัติและบันทึกไปพร้อมกับข้อกำหนดของวิชวลเพื่อให้พร้อมใช้งานบนการโหลดครั้งถัดไป
   * `eventService` ส่งกลับ [การบริการเหตุการณ์](./event-service.md) เพื่อรองรับเหตุการณ์ **การแสดงผล**
   * `storageService`ส่งกลับบริการเพื่อช่วยในการใช้ [ที่เก็บข้อมูลภายในเครื่อง](./local-storage.md) ในวิชวล
   * `authenticationService` สร้างบริการเพื่อช่วยในการรับรองความถูกต้องของผู้ใช้
   * `tooltipService` ส่งกลับ [บริการคำแนะนำเครื่องมือ](./add-tooltips.md) เพื่อช่วยในการใช้คำแนะนำเครื่องมือในวิชวล
   * `launchUrl` ช่วยในการ [เปิดใช้งาน URL](./launch-url.md) ในแท็บถัดไป
   * `locale` ส่งกลับสตริงของพื้นที่ ดู [การแปลเป็นภาษาท้องถิ่น](./localization.md)
   * `instanceId` ส่งกลับสตริงที่จะระบุอินสแตนซ์วิชวลปัจจุบัน
   * `colorPalette` ส่งกลับ colorPalette ที่จำเป็นในการนำสีไปใช้กับข้อมูลของคุณ
   * `fetchMoreData` สนับสนุนการใช้ข้อมูลมากกว่าขีดจำกัดมาตรฐาน (1K แถว)
   * `switchFocusModeState` ช่วยในการเปลี่ยนสถานะโหมดโฟกัส

## <a name="update"></a>อัปเดต

วิชวลทั้งหมดต้องใช้วิธีการอัปเดตสาธารณะที่ถูกเรียกเมื่อใดก็ตามที่มีการเปลี่ยนแปลงในข้อมูลหรือสภาพแวดล้อมของโฮสต์

```typescript
public update(options: VisualUpdateOptions): void
```

**VisualUpdateOptions**

* `viewport: IViewport` ขนาดของวิวพอร์ตที่วิชวลควรแสดงผลอยู่
* `dataViews: DataView[]` วัตถุ dataview ที่ประกอบด้วยข้อมูลทั้งหมดที่จำเป็นในการแสดงผลวิชวลของคุณ (โดยทั่วไปแล้ววิชวลของคุณจะใช้คุณสมบัติประเภทภายใต้ DataView)
* `type: VisualUpdateType` ค่าสถานะเพื่อระบุประเภทของการอัปเดตนี้ (**ข้อมูล** | **ปรับขนาด** | **ViewMode** | **สไตล์** | **ResizeEnd**)
* `viewMode: ViewMode` ค่าสถานะเพื่อระบุโหมดมุมมองของวิชวล (**มุมมอง** | **แก้ไข** | **InFocusEdit**)
* `editMode: EditMode` ค่าสถานะเพื่อระบุโหมดแก้ไขของวิชวล (**ค่าเริ่มต้น** | **ขั้นสูง**) (ถ้าวิชวลรองรับ **AdvancedEditMode** วิชวลจะแสดงตัวควบคุม UI ขั้นสูงเฉพาะเมื่อ **editMode** ได้รับการตั้งค่าเป็น **ขั้นสูง** เท่านั้น ดู [AdvancedEditMode](./advanced-edit-mode.md))
* `operationKind?: VisualDataChangeOperationKind` ค่าสถานะเพื่อระบุชนิดของการเปลี่ยนแปลงข้อมูล (**สร้าง** | **ผนวก**)
* `jsonFilters?: IFilter[]` คอลเลกชันของตัวกรอง json ที่ใช้
* `isInFocus?: boolean` ค่าสถานะเพื่อระบุว่าวิชวลอยู่ในโหมดโฟกัสหรือไม่
    
## <a name="enumerateobjectinstances-optional"></a>enumerateObjectInstances `optional`

มีการเรียกใช้วิธีนี้สำหรับทุกวัตถุที่แสดงอยู่ในรายการความสามารถ การใช้ตัวเลือก (เฉพาะชื่อในขณะนี้) คุณได้ส่งกลับ `VisualObjectInstanceEnumeration` พร้อมข้อมูลเกี่ยวกับวิธีการแสดงคุณสมบัตินี้

```typescript
enumerateObjectInstances(options:EnumerateVisualObjectInstancesOptions):VisualObjectInstanceEnumeration
```

**EnumerateVisualObjectInstancesOptions**

* `objectName: string` ชื่อของวัตถุ

## <a name="destroy-optional"></a>ทำลาย `optional`

ฟังก์ชันการทำลายจะถูกเรียกเมื่อวิชวลของคุณถูกยกเลิกการโหลด และสามารถใช้สำหรับงานล้างข้อมูล เช่น การลบผู้ฟังเหตุการณ์

``` typescript
public destroy(): void
```

> [!Note]
> โดยทั่วไป Power BI ไม่ได้เรียกใช้ `destroy` เนื่องจากการลบ IFrame ทั้งหมดที่มีวิชวลสามารถทำได้รวดเร็วกว่า
