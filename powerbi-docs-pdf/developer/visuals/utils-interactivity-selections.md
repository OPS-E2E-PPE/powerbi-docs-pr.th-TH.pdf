---
title: ยูทิลิตี้การโต้ตอบกับวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการเพิ่มการเลือกลงในวิชวล Power BI โดยใช้ยูทิลิตี้การโต้ตอบ เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: rkarlin
manager: rkarlin
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: reference
ms.date: 02/24/2020
ms.openlocfilehash: 533cf90ed9192a8d9e595cdea6320207b841b559
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887787"
---
# <a name="power-bi-visuals-interactivity-utils"></a><span data-ttu-id="d8ffd-104">utils การโต้ตอบวิชวลของ Power BI</span><span class="sxs-lookup"><span data-stu-id="d8ffd-104">Power BI visuals interactivity utils</span></span>

<span data-ttu-id="d8ffd-105">InteractiveivityUtils (`InteractivityUtils`) เป็นชุดของฟังก์ชันและคลาสเพื่อให้ง่ายต่อการใช้งานการเลือกข้ามและการกรองข้าม</span><span class="sxs-lookup"><span data-stu-id="d8ffd-105">Interactivity utils (`InteractivityUtils`) is a set of functions and classes that can be used to simplify the implementation of cross-selection and cross-filtering.</span></span>

> [!NOTE]
> <span data-ttu-id="d8ffd-106">การอัปเดตยูทิลิตี้การโต้ตอบใหม่จะรองรับเฉพาะเครื่องเวอร์ชันล่าสุดเท่านั้น (3.x.x และใหม่กว่า)</span><span class="sxs-lookup"><span data-stu-id="d8ffd-106">The new updates of interactivity utils support only the latest version of tools (3.x.x and above).</span></span>

## <a name="installation"></a><span data-ttu-id="d8ffd-107">การติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="d8ffd-107">Installation</span></span>

1. <span data-ttu-id="d8ffd-108">หากต้องการติดตั้งแพ็คเกจ คุณควรเรียกใช้คำสั่งต่อไปนี้ในไดเรกทอรีด้วยโครงการการแสดงผลด้วยภาพของ Power BI ปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="d8ffd-108">To install the package, run the following command in the directory with your current Power BI visual project.</span></span>

    ```bash
    npm install powerbi-visuals-utils-interactivityutils --save
    ```

2. <span data-ttu-id="d8ffd-109">ถ้าคุณกำลังใช้รุ่น 3.0 หรือใหม่กว่าหรือเครื่องมือ ให้ติดตั้ง `powerbi-models` เพื่อแก้ไขการขึ้นต่อกัน</span><span class="sxs-lookup"><span data-stu-id="d8ffd-109">If you're using version 3.0 or later or the tool, install `powerbi-models` to resolve dependencies.</span></span>

    ```bash
    npm install powerbi-models --save
    ```

3. <span data-ttu-id="d8ffd-110">หากต้องการใช้ยูทิลิตี้การโต้ตอบ คุณต้องนำเข้าคอมโพเนนต์ที่จำเป็นในโค้ดต้นฉบับของการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="d8ffd-110">To use interactivity utils, import the required component in the source code of the Power BI visual.</span></span>

    ```typescript
    import { interactivitySelectionService } from "powerbi-visuals-utils-interactivityutils";
    ```

### <a name="including-the-css-files"></a><span data-ttu-id="d8ffd-111">รวมถึงไฟล์ CSS</span><span class="sxs-lookup"><span data-stu-id="d8ffd-111">Including the CSS files</span></span>

<span data-ttu-id="d8ffd-112">หากต้องการใช้แพ็คเกจกับการแสดงผลด้วยภาพของ Power BI คุณควรนำเข้าไฟล์ CSS ไปยังไฟล์ `.less`  ดังนี้</span><span class="sxs-lookup"><span data-stu-id="d8ffd-112">To use the package with your Power BI visual, import the following CSS file to your `.less` file.</span></span>

`node_modules/powerbi-visuals-utils-interactivityutils/lib/index.css`

<span data-ttu-id="d8ffd-113">นำเข้าไฟล์ CSS เป็นไฟล์ `.less` เนื่องจากเครื่องมือการแสดงผลด้วยภาพของ Power BI คลุมกฎ CSS ภายนอก</span><span class="sxs-lookup"><span data-stu-id="d8ffd-113">Import the CSS file as a `.less` file because the Power BI visuals tool wraps external CSS rules.</span></span>

```less
@import (less) "node_modules/powerbi-visuals-utils-interactivityutils/lib/index.css";
```

## <a name="selectabledatapoint-properties"></a><span data-ttu-id="d8ffd-114">คุณสมบัติ SelectableDataPoint</span><span class="sxs-lookup"><span data-stu-id="d8ffd-114">SelectableDataPoint properties</span></span>

<span data-ttu-id="d8ffd-115">โดยทั่วไปจุดข้อมูลประกอบด้วยตัวเลือกและค่าต่างๆ</span><span class="sxs-lookup"><span data-stu-id="d8ffd-115">Usually, data points contain selections and values.</span></span> <span data-ttu-id="d8ffd-116">อินเทอร์เฟซจะขยายอินเทอร์เฟซ `SelectableDataPoint`</span><span class="sxs-lookup"><span data-stu-id="d8ffd-116">The interface extends the `SelectableDataPoint` interface.</span></span>

<span data-ttu-id="d8ffd-117">`SelectableDataPoint` มีคุณสมบัติตามที่อธิบายไว้ด้านล่างแล้ว</span><span class="sxs-lookup"><span data-stu-id="d8ffd-117">`SelectableDataPoint` already contains properties as described below.</span></span>

```typescript
  /** Flag for identifying that a data point was selected */
  selected: boolean;

  /** Identity for identifying the selectable data point for selection purposes */
  identity: powerbi.extensibility.ISelectionId;

  /*
   * A specific identity for when data points exist at a finer granularity than
   * selection is performed.  For example, if your data points select based
   * only on series, even if they exist as category/series intersections.
   */

  specificIdentity?: powerbi.extensibility.ISelectionId;
```

## <a name="defining-an-interface-for-data-points"></a><span data-ttu-id="d8ffd-118">กำหนดอินเทอร์เฟซสำหรับจุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d8ffd-118">Defining an interface for data points</span></span>

1. <span data-ttu-id="d8ffd-119">สร้างอินสแตนซ์ของยูทิลิตี้แบบโต้ตอบและบันทึกวัตถุเป็นคุณสมบัติของการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="d8ffd-119">Create an instance of interactivity utils and save the object as a property of the visual</span></span>

    ```typescript
    export class Visual implements IVisual {
      // ...
      private interactivity: interactivityBaseService.IInteractivityService<VisualDataPoint>;
      // ...
      constructor(options: VisualConstructorOptions) {
          // ...
          this.interactivity = interactivitySelectionService.createInteractivitySelectionService(this.host);
          // ...
      }
    }
    ```

    ```typescript
    import { interactivitySelectionService } from "powerbi-visuals-utils-interactivityutils";

    export interface VisualDataPoint extends interactivitySelectionService.SelectableDataPoint {
        value: powerbi.PrimitiveValue;
    }
    ```

2. <span data-ttu-id="d8ffd-120">ขยายคลาสของลักษณะการทำงานพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="d8ffd-120">Extend the base behavior class.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d8ffd-121">`BaseBehavior` ได้รับการแนะนำใน[ยูทิลิตี้แบบโต้ตอบเวอร์ชัน 5.6.x](https://www.npmjs.com/package/powerbi-visuals-utils-interactivityutils/v/5.6.0)</span><span class="sxs-lookup"><span data-stu-id="d8ffd-121">`BaseBehavior` was introduced in the [5.6.x version of interactivity utils](https://www.npmjs.com/package/powerbi-visuals-utils-interactivityutils/v/5.6.0).</span></span> <span data-ttu-id="d8ffd-122">หากคุณใช้เวอร์ชันเก่า ให้สร้างคลาสลักษณะการทำงานจากตัวอย่างด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="d8ffd-122">If you use an older version, create a behavior class from the sample below.</span></span>

3. <span data-ttu-id="d8ffd-123">กำหนดอินเทอร์เฟซสำหรับตัวเลือกของคลาสลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="d8ffd-123">Define the interface for the behavior class options.</span></span>

    ```typescript
    import { SelectableDataPoint } from "./interactivitySelectionService";

    import {
        IBehaviorOptions,
        BaseDataPoint
    } from "./interactivityBaseService";

    export interface BaseBehaviorOptions<SelectableDataPointType extends BaseDataPoint> extends IBehaviorOptions<SelectableDataPointType> {

    /** d3 selection object of the main elements on the chart */
    elementsSelection: Selection<any, SelectableDataPoint, any, any>;

    /** d3 selection object of some elements on backgroup, to hadle click of reset selection */
    clearCatcherSelection: d3.Selection<any, any, any, any>;
    }
    ```

4. <span data-ttu-id="d8ffd-124">กำหนดคลาสสำหรับ `visual behavior`</span><span class="sxs-lookup"><span data-stu-id="d8ffd-124">Define a class for `visual behavior`.</span></span> <span data-ttu-id="d8ffd-125">หรือขยายคลาส `BaseBehavior`</span><span class="sxs-lookup"><span data-stu-id="d8ffd-125">Or, extend the `BaseBehavior` class.</span></span>

    <span data-ttu-id="d8ffd-126">**กำหนดคลาสสำหรับ `visual behavior`**</span><span class="sxs-lookup"><span data-stu-id="d8ffd-126">**Defining a class for `visual behavior`**</span></span>

    <span data-ttu-id="d8ffd-127">คลาสจะรับผิดชอบในการจัดการ `click` `contextmenu` กิจกรรมของเม้าส์</span><span class="sxs-lookup"><span data-stu-id="d8ffd-127">The class is responsible to handle `click` `contextmenu` mouse events.</span></span>

    <span data-ttu-id="d8ffd-128">เมื่อผู้ใช้คลิกองค์ประกอบข้อมูล การแสดงผลด้วยภาพจะใช้ตัวจัดการการเลือกเพื่อเลือกจุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d8ffd-128">When a user clicks on data elements, the visual calls the selection handler to select data points.</span></span> <span data-ttu-id="d8ffd-129">หากผู้ใช้คลิกที่องค์ประกอบพื้นหลังของการแสดงผลด้วยภาพ จะเป็นการเรียกใช้ตัวจัดการล้างการเลือก</span><span class="sxs-lookup"><span data-stu-id="d8ffd-129">if the user clicks on the background element of the visual, it calls the clear selection handler.</span></span>

    <span data-ttu-id="d8ffd-130">และคลาสจะมีวิธีการที่สอดคล้องกันดังนี้:</span><span class="sxs-lookup"><span data-stu-id="d8ffd-130">The class has the following correspond methods:</span></span>
    * `bindClick`
    * `bindClearCatcher`
    * <span data-ttu-id="d8ffd-131">`bindContextMenu`.</span><span class="sxs-lookup"><span data-stu-id="d8ffd-131">`bindContextMenu`.</span></span>

    ```typescript
    export class Behavior<SelectableDataPointType extends BaseDataPoint> implements IInteractiveBehavior {

        /** d3 selection object of main elements in the chart */
        protected options: BaseBehaviorOptions<SelectableDataPointType>;
        protected selectionHandler: ISelectionHandler;
    
        protected bindClick() {
          // ...
        }
    
        protected bindClearCatcher() {
          // ...
        }
    
        protected bindContextMenu() {
          // ...
        }
    
        public bindEvents(
            options: BaseBehaviorOptions<SelectableDataPointType>,
            selectionHandler: ISelectionHandler): void {
          // ...
        }
    
        public renderSelection(hasSelection: boolean): void {
          // ...
        }
    }
    ```

    <span data-ttu-id="d8ffd-132">**การขยาย`BaseBehavior`คลาส**</span><span class="sxs-lookup"><span data-stu-id="d8ffd-132">**Extending the `BaseBehavior` class**</span></span>

    ```typescript
    import powerbi from "powerbi-visuals-api";
    import { interactivitySelectionService, baseBehavior } from "powerbi-visuals-utils-interactivityutils";

    export interface VisualDataPoint extends interactivitySelectionService.SelectableDataPoint {
        value: powerbi.PrimitiveValue;
    }

    export class Behavior extends baseBehavior.BaseBehavior<VisualDataPoint> {
      // ...
    }
    ```

5. <span data-ttu-id="d8ffd-133">หากต้องการจัดการการคลิกที่องค์ประกอบ ให้เรียกใช้วิธีการ *การเลือกวัตถุ* d3`on`</span><span class="sxs-lookup"><span data-stu-id="d8ffd-133">To handle click on elements, call the *d3* selection object `on` method.</span></span> <span data-ttu-id="d8ffd-134">นอกจากนี้ยังใช้สำหรับ `elementsSelection` และ `clearCatcherSelection`</span><span class="sxs-lookup"><span data-stu-id="d8ffd-134">This also applies for `elementsSelection` and `clearCatcherSelection`.</span></span>

    ```typescript
    protected bindClick() {
      const {
          elementsSelection
      } = this.options;
    
      elementsSelection.on("click", (datum) => {
          const mouseEvent: MouseEvent = getEvent() as MouseEvent || window.event as MouseEvent;
          mouseEvent && this.selectionHandler.handleSelection(
              datum,
              mouseEvent.ctrlKey);
      });
    }
    ```

6. <span data-ttu-id="d8ffd-135">เพิ่มตัวจัดการที่คล้ายกันสำหรับเหตุการณ์ `contextmenu` เพื่อเรียกใช้วิธีการ `showContextMenu` ของผู้จัดการการเลือก</span><span class="sxs-lookup"><span data-stu-id="d8ffd-135">Add a similar handler for the `contextmenu` event, to call the selection manager's `showContextMenu` method.</span></span>

    ```typescript
    protected bindContextMenu() {
        const {
            elementsSelection
        } = this.options;
    
        elementsSelection.on("contextmenu", (datum) => {
            const event: MouseEvent = (getEvent() as MouseEvent) || window.event as MouseEvent;
            if (event) {
                this.selectionHandler.handleContextMenu(
                    datum,
                    {
                        x: event.clientX,
                        y: event.clientY
                    });
                event.preventDefault();
            }
        });
    }
    ```

7. <span data-ttu-id="d8ffd-136">เพื่อกำหนดฟังก์ชันให้กับตัวจัดการยูทิลิตี้การโต้ตอบให้เรียกใช้วิธีการ `bindEvents`</span><span class="sxs-lookup"><span data-stu-id="d8ffd-136">To assign functions to handlers, the interactivity utils calls the `bindEvents` method.</span></span> <span data-ttu-id="d8ffd-137">เพิ่มการเรียกไปยังวิธีการ `bindEvents` ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d8ffd-137">Add the following calls to  the `bindEvents` method:</span></span>
    * `bindClick`
    * `bindClearCatcher`
    * `bindContextMenu`

    ```typescript
      public bindEvents(
          options: BaseBehaviorOptions<SelectableDataPointType>,
          selectionHandler: ISelectionHandler): void {

          this.options = options;
          this.selectionHandler = selectionHandler;

          this.bindClick();
          this.bindClearCatcher();
          this.bindContextMenu();
      }
    ```

8. <span data-ttu-id="d8ffd-138">เมธอด `renderSelection` จะรับผิดชอบในการปรับปรุงสถานะวิชวลขององค์ประกอบในแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="d8ffd-138">The `renderSelection` method is responsible for updating the visual state of elements in the chart.</span></span> <span data-ttu-id="d8ffd-139">ตัวอย่างของวิธีการ `renderSelection` การดำเนินการ:</span><span class="sxs-lookup"><span data-stu-id="d8ffd-139">Here's a sample implementation of `renderSelection`.</span></span>

    ```typescript
    public renderSelection(hasSelection: boolean): void {
        this.options.elementsSelection.style("opacity", (category: any) => {
            if (category.selected) {
                return 0.5;
            } else {
                return 1;
            }
        });
    }
    ```

9. <span data-ttu-id="d8ffd-140">ขั้นตอนสุดท้ายคือการสร้างอินสแตนซ์ของ `visual behavior` และเรียกใช้วิธีการ `bind` ของอินสแตนซ์ยูทิลิตี้การโต้ตอบดังนี้:</span><span class="sxs-lookup"><span data-stu-id="d8ffd-140">The last step is creating an instance of `visual behavior`, and calling the `bind` method of the interactivity utils instance.</span></span>

    ```typescript
    this.interactivity.bind(<BaseBehaviorOptions<VisualDataPoint>>{
        behavior: this.behavior,
        dataPoints: this.categories,
        clearCatcherSelection: select(this.target),
        elementsSelection: selectionMerge
    });
    ```

    * <span data-ttu-id="d8ffd-141">`selectionMerge` เป็นออบเจ็กต์การเลือก *d3* ซึ่งจะแสดงองค์ประกอบที่สามารถเลือกได้ทั้งหมดในการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="d8ffd-141">`selectionMerge` is the *d3* selection object, which represents all the visuals's selectable elements.</span></span>
    * <span data-ttu-id="d8ffd-142">`select(this.target)` เป็นออบเจ็กต์การเลือก *d3* ซึ่งจะแสดงองค์ประกอบ DOM หลักของการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="d8ffd-142">`select(this.target)` is the *d3* selection object, which represents the visual's main DOM elements.</span></span>
    * <span data-ttu-id="d8ffd-143">`this.categories` เป็นจุดข้อมูลที่มีองค์ประกอบ ที่ซึ่งอินเทอร์เฟซคือ `VisualDataPoint` (หรือ `categories: VisualDataPoint[];`)</span><span class="sxs-lookup"><span data-stu-id="d8ffd-143">`this.categories` are data points with elements, where the interface is `VisualDataPoint` or `categories: VisualDataPoint[];`.</span></span>
    * <span data-ttu-id="d8ffd-144">`this.behavior` เป็นอินสแตนซ์ใหม่ของ `visual behavior` ที่สร้างขึ้นในตัวจัดการของการแสดงผลด้วยภาพดังที่แสดงด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="d8ffd-144">`this.behavior` is a new instance of `visual behavior` created in the constructor of the visual, as shown below.</span></span>

      ```typescript
      export class Visual implements IVisual {
        // ...
        constructor(options: VisualConstructorOptions) {
            // ...
            this.behavior = new Behavior();
        }
        // ...
      }
      ```
## <a name="next-steps"></a><span data-ttu-id="d8ffd-145">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d8ffd-145">Next steps</span></span>

* [<span data-ttu-id="d8ffd-146">อ่านวิธีการจัดการกับการเลือกในการสลับบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="d8ffd-146">Read how to handle selections on bookmarks switching</span></span>](bookmarks-support.md#visuals-with-selection)

* [<span data-ttu-id="d8ffd-147">อ่านวิธีการเพิ่มเมนูบริบทสำหรับจุดข้อมูลภาพ</span><span class="sxs-lookup"><span data-stu-id="d8ffd-147">Read how to add context menu for visuals data points</span></span>](context-menu.md)

* [<span data-ttu-id="d8ffd-148">อ่านวิธีการใช้ตัวจัดการการเลือกเพื่อเพิ่มการเลือกลงในการแสดงด้วยภาพของ Power BI</span><span class="sxs-lookup"><span data-stu-id="d8ffd-148">Read how to use selection manager to add selections into Power BI Visuals</span></span>](selection-api.md)
