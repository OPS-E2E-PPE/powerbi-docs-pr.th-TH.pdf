---
title: บทนำสู่การใช้งานยูทิลิตี้คำแนะนำเครื่องมือของวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการใช้ยูทิลิตี้คำแนะนำเครื่องมือ การปรับแต่งคำแนะนำเครื่องมือสำหรับวิชวล Power BI อย่างง่าย เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: reference
ms.date: 02/14/2020
ms.openlocfilehash: b2ddc85d9ba2530dc394b4106d72b4af702bd9b4
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888661"
---
# <a name="tooltip-utils"></a><span data-ttu-id="53e2b-104">คำแนะนำเครื่องมือยูทิลิตี้</span><span class="sxs-lookup"><span data-stu-id="53e2b-104">Tooltip utils</span></span>
<span data-ttu-id="53e2b-105">บทความนี้จะช่วยให้คุณสามารถติดตั้ง นำเข้า และใช้คำแนะนำเครื่องมือยูทิลิตี้</span><span class="sxs-lookup"><span data-stu-id="53e2b-105">This article will help you to install, import, and use tooltip utils.</span></span> <span data-ttu-id="53e2b-106">ยูทิลิตี้นี้มีประโยชน์สำหรับการปรับแต่งคำแนะนำเครื่องมือใดๆ ก็ตามในการแสดงผลด้วยภาพของ Power BI</span><span class="sxs-lookup"><span data-stu-id="53e2b-106">This util useful for any tooltip customization in Power BI visuals.</span></span>

## <a name="requirements"></a><span data-ttu-id="53e2b-107">ข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="53e2b-107">Requirements</span></span>
<span data-ttu-id="53e2b-108">หากต้องการใช้แพคเกจ คุณควรมีสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="53e2b-108">To use the package, you should have the following things:</span></span>
* <span data-ttu-id="53e2b-109">[node.js](https://nodejs.org) (เราขอแนะนำเวอร์ชัน LTS รุ่นล่าสุด)</span><span class="sxs-lookup"><span data-stu-id="53e2b-109">[node.js](https://nodejs.org) (we recommend the latest LTS version)</span></span>
* <span data-ttu-id="53e2b-110">[npm](https://www.npmjs.com/) (เวอร์ชันเก่าที่สุดที่ได้รับการรองรับคือ 3.0.0)</span><span class="sxs-lookup"><span data-stu-id="53e2b-110">[npm](https://www.npmjs.com/) (the minimal supported version is 3.0.0)</span></span>
* <span data-ttu-id="53e2b-111">การแสดงผลด้วยภาพแบบกำหนดเองที่สร้างขึ้นโดย [PowerBI-visuals-tools](https://www.npmjs.com/package/powerbi-visuals-tools)</span><span class="sxs-lookup"><span data-stu-id="53e2b-111">The custom visual created by [PowerBI-visuals-tools](https://www.npmjs.com/package/powerbi-visuals-tools)</span></span>

## <a name="installation"></a><span data-ttu-id="53e2b-112">การติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="53e2b-112">Installation</span></span>

<span data-ttu-id="53e2b-113">หากต้องการติดตั้งแพ็คเกจ คุณควรเรียกใช้คำสั่งต่อไปนี้ในไดเรกทอรีด้วยวิชวลปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="53e2b-113">To install the package, you should run the following command in the directory with your current visual:</span></span>

```bash
npm install powerbi-visuals-utils-tooltiputils --save
```
<span data-ttu-id="53e2b-114">คำสั่งนี้จะติดตั้งแพคเกจและเพิ่มแพคเกจเป็นการขึ้นต่อกันของคุณ ```package.json```</span><span class="sxs-lookup"><span data-stu-id="53e2b-114">This command installs the package and adds a package as a dependency to your ```package.json```</span></span>

## <a name="usage"></a><span data-ttu-id="53e2b-115">การใช้</span><span class="sxs-lookup"><span data-stu-id="53e2b-115">Usage</span></span>

> <span data-ttu-id="53e2b-116">คำแนะนำการใช้งานจะอธิบาย API สาธารณะของแพคเกจ</span><span class="sxs-lookup"><span data-stu-id="53e2b-116">The Usage Guide describes a public API of the package.</span></span> <span data-ttu-id="53e2b-117">คุณจะพบคำอธิบายและตัวอย่างสำหรับแต่ละอินเทอร์เฟซสาธารณะของแพคเกจ</span><span class="sxs-lookup"><span data-stu-id="53e2b-117">You will find a description and a few examples for each public interface of the package.</span></span>

<span data-ttu-id="53e2b-118">แพคเกจนี้ประกอบด้วยวิธีการสร้าง `TooltipServiceWrapper` และวิธีการเพื่อช่วยจัดการการดำเนินการคำแนะนำเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="53e2b-118">This package contains provide you the way to create `TooltipServiceWrapper` and methods to help handle tooltip actions.</span></span> <span data-ttu-id="53e2b-119">ซึ่งใช้อินเทอร์เฟซคำแนะนำเครื่องมือ- `ITooltipServiceWrapper` `TooltipEventArgs` `TooltipEnabledDataPoint`</span><span class="sxs-lookup"><span data-stu-id="53e2b-119">It uses tooltip interfaces - `ITooltipServiceWrapper`, `TooltipEventArgs`, `TooltipEnabledDataPoint`.</span></span> 

<span data-ttu-id="53e2b-120">นอกจากนี้ยังมีวิธีการเฉพาะ (ตัวจัดการเหตุการณ์การ touch) ที่เกี่ยวข้องกับการพัฒนาอุปกรณ์เคลื่อนที่: `touchEndEventName` `touchStartEventName` `usePointerEvents`</span><span class="sxs-lookup"><span data-stu-id="53e2b-120">Also it has specific methods (touch events handlers) related to mobile development: `touchEndEventName`, `touchStartEventName`, `usePointerEvents`.</span></span>

<span data-ttu-id="53e2b-121">`TooltipServiceWrapper` ให้วิธีที่ง่ายที่สุดในการจัดการคำแนะนำเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="53e2b-121">`TooltipServiceWrapper` provides the simplest way in order to manipulate tooltips.</span></span>

<span data-ttu-id="53e2b-122">โมดูลนี้มีฟังก์ชันและอินเทอร์เฟสต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="53e2b-122">This module provides the following interface and function:</span></span>
* [<span data-ttu-id="53e2b-123">ITooltipServiceWrapper</span><span class="sxs-lookup"><span data-stu-id="53e2b-123">ITooltipServiceWrapper</span></span>](#itooltipservicewrapper)
  * [<span data-ttu-id="53e2b-124">addTooltip</span><span class="sxs-lookup"><span data-stu-id="53e2b-124">addTooltip</span></span>](#itooltipservicewrapperaddtooltip)
  * [<span data-ttu-id="53e2b-125">ซ่อน</span><span class="sxs-lookup"><span data-stu-id="53e2b-125">hide</span></span>](#itooltipservicewrapperhide)

* [<span data-ttu-id="53e2b-126">อินเทอร์เฟซ</span><span class="sxs-lookup"><span data-stu-id="53e2b-126">Interfaces</span></span>](#interfaces)
  * [<span data-ttu-id="53e2b-127">TooltipEventArgs</span><span class="sxs-lookup"><span data-stu-id="53e2b-127">TooltipEventArgs</span></span>](#tooltipeventargs)
  * [<span data-ttu-id="53e2b-128">TooltipEnabledDataPoint</span><span class="sxs-lookup"><span data-stu-id="53e2b-128">TooltipEnabledDataPoint</span></span>](#tooltipenableddatapoint)
  * [<span data-ttu-id="53e2b-129">TooltipServiceWrapperOptions</span><span class="sxs-lookup"><span data-stu-id="53e2b-129">TooltipServiceWrapperOptions</span></span>](#tooltipservicewrapperoptions)
* [<span data-ttu-id="53e2b-130">เหตุการณ์ Touch</span><span class="sxs-lookup"><span data-stu-id="53e2b-130">Touch events</span></span>](#touch-events)

### `createTooltipServiceWrapper`
<span data-ttu-id="53e2b-131">ฟังก์ชันนี้สร้างตัวอย่างของ ITooltipServiceWrapper</span><span class="sxs-lookup"><span data-stu-id="53e2b-131">This function creates an instance of ITooltipServiceWrapper.</span></span>

```typescript
function createTooltipServiceWrapper(tooltipService: ITooltipService, rootElement: Element, handleTouchDelay?: number,  getEventMethod?: () => MouseEvent): ITooltipServiceWrapper;
```

<span data-ttu-id="53e2b-132">```ITooltipService``` พร้อมใช้งานใน [IVisualHost](https://github.com/microsoft/PowerBI-visuals-tools/blob/master/templates/visuals/.api/v2.6.0/PowerBI-visuals.d.ts#L1335)</span><span class="sxs-lookup"><span data-stu-id="53e2b-132">The ```ITooltipService``` is available in [IVisualHost](https://github.com/microsoft/PowerBI-visuals-tools/blob/master/templates/visuals/.api/v2.6.0/PowerBI-visuals.d.ts#L1335).</span></span>

<span data-ttu-id="53e2b-133">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="53e2b-133">**Example**</span></span>

```typescript
import { createTooltipServiceWrapper } from "powerbi-visuals-utils-tooltiputils";

export class YourVisual implements IVisual {
    // implementation of IVisual.

    constructor(options: VisualConstructorOptions) {
        createTooltipServiceWrapper(
            options.host.tooltipService,
            options.element);

        // returns: an instance of ITooltipServiceWrapper.
    }
}
```

<span data-ttu-id="53e2b-134">คุณสามารถดูโค้ดตัวอย่างของวิชวลแบบกำหนดเอง [ที่นี่](https://github.com/microsoft/powerbi-visuals-gantt/blob/master/src/gantt.ts#L391)</span><span class="sxs-lookup"><span data-stu-id="53e2b-134">You can take a look at the example code of the custom visual [here](https://github.com/microsoft/powerbi-visuals-gantt/blob/master/src/gantt.ts#L391).</span></span>

### `ITooltipServiceWrapper`
<span data-ttu-id="53e2b-135">อินเทอร์เฟซนี้จะอธิบายวิธีการสาธารณะของ TooltipService</span><span class="sxs-lookup"><span data-stu-id="53e2b-135">This interface describes public methods of the TooltipService.</span></span>

```typescript
interface ITooltipServiceWrapper {
    addTooltip<T>(selection: d3.Selection<any, any, any, any>, getTooltipInfoDelegate: (args: TooltipEventArgs<T>) => powerbi.extensibility.VisualTooltipDataItem[], getDataPointIdentity?: (args: TooltipEventArgs<T>) => powerbi.visuals.ISelectionId, reloadTooltipDataOnMouseMove?: boolean): void;
    hide(): void;
}
```

#### `ITooltipServiceWrapper.addTooltip`

<span data-ttu-id="53e2b-136">วิธีนี้จะเพิ่มคำแนะนำเครื่องมือในการเลือกปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="53e2b-136">This method adds tooltips to the current selection.</span></span>

```typescript
addTooltip<T>(selection: d3.Selection<any>, getTooltipInfoDelegate: (args: TooltipEventArgs<T>) => VisualTooltipDataItem[], getDataPointIdentity?: (args: TooltipEventArgs<T>) => ISelectionId, reloadTooltipDataOnMouseMove?: boolean): void;
```

<span data-ttu-id="53e2b-137">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="53e2b-137">**Example**</span></span>

```typescript
import { createTooltipServiceWrapper, TooltipEventArgs, ITooltipServiceWrapper, TooltipEnabledDataPoint } from "powerbi-visuals-utils-tooltiputils";

let bodyElement = d3.select("body");

let element = bodyElement
    .append("div")
    .style({
        "background-color": "green",
        "width": "150px",
        "height": "150px"
    })
    .classed("visual", true)
    .data([{
        tooltipInfo: [{
            displayName: "Power BI",
            value: 2016
        }]
    }]);

let tooltipServiceWrapper: ITooltipServiceWrapper = createTooltipServiceWrapper(tooltipService, bodyElement.get(0)); // tooltipService is from the IVisualHost.

tooltipServiceWrapper.addTooltip<TooltipEnabledDataPoint>(element, (eventArgs: TooltipEventArgs<TooltipEnabledDataPoint>) => {
    return eventArgs.data.tooltipInfo;
});

// You will see a tooltip if you mouseover the element.
```

<span data-ttu-id="53e2b-138">คุณสามารถดูโค้ดตัวอย่างของวิชวลแบบกำหนดเอง [ที่นี่](https://github.com/microsoft/powerbi-visuals-gantt/blob/master/src/gantt.ts#L2931)</span><span class="sxs-lookup"><span data-stu-id="53e2b-138">You can take a look at the example code of the custom visual [here](https://github.com/microsoft/powerbi-visuals-gantt/blob/master/src/gantt.ts#L2931).</span></span>

<span data-ttu-id="53e2b-139">โปรดตั้งใจดูตัวอย่างของการปรับแต่งคำแนะนำเครื่องมือในการแสดงผลด้วยภาพของ Gantt ที่กำหนดเอง[ที่นี่](https://github.com/microsoft/powerbi-visuals-gantt/blob/master/src/gantt.ts#L573-L648)</span><span class="sxs-lookup"><span data-stu-id="53e2b-139">Also pay attention at following example of tooltip customization in Gantt custom visual [here](https://github.com/microsoft/powerbi-visuals-gantt/blob/master/src/gantt.ts#L573-L648)</span></span>

### `ITooltipServiceWrapper.hide`

<span data-ttu-id="53e2b-140">วิธีนี้จะซ่อนคำแนะนำเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="53e2b-140">This method hides the tooltip.</span></span>

```typescript
hide(): void;
```

<span data-ttu-id="53e2b-141">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="53e2b-141">**Example**</span></span>

```typescript
import {createTooltipServiceWrapper} from "powerbi-visuals-utils-tooltiputils";

let tooltipServiceWrapper = createTooltipServiceWrapper(options.host.tooltipService, options.element); // options are from the VisualConstructorOptions.

tooltipServiceWrapper.hide();
```
### `Interfaces`
<span data-ttu-id="53e2b-142">อินเทอร์เฟซนี้ถูกใช้ในระหว่างการสร้าง TooltipServiceWrapper และการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="53e2b-142">This interfaces are used during TooltipServiceWrapper creation and it's usage.</span></span> <span data-ttu-id="53e2b-143">นอกจากนี้ยังมีการกล่าวถึงในตัวอย่างจากหัวข้อก่อนหน้า[ที่นี่](#itooltipservicewrapperaddtooltip)</span><span class="sxs-lookup"><span data-stu-id="53e2b-143">Also they were mentioned in examples from previous topic [here](#itooltipservicewrapperaddtooltip).</span></span>

#### `TooltipEventArgs`
```typescript
interface TooltipEventArgs<TData> {
    data: TData;
    coordinates: number[];
    elementCoordinates: number[];
    context: HTMLElement;
    isTouchEvent: boolean;
}
```

#### `TooltipEnabledDataPoint`
```typescript
interface TooltipEnabledDataPoint {
    tooltipInfo?: powerbi.extensibility.VisualTooltipDataItem[];
}
```

#### `TooltipServiceWrapperOptions`
```typescript
interface TooltipServiceWrapperOptions {
    tooltipService: ITooltipService;
    rootElement: Element;
    handleTouchDelay: number;
    getEventMethod?: () => MouseEvent;
```

### `Touch events`

<span data-ttu-id="53e2b-144">ตอนนี้คำแนะนำเครื่องมือ utils มีความสามารถในการจัดการเหตุการณ์การสัมผัสหลายอย่างที่เป็นประโยชน์สำหรับการพัฒนาอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="53e2b-144">Now tooltip utils has ability to handle several touch events useful for mobile development.</span></span>

#### `touchStartEventName`
```typescript
function touchStartEventName(): string
```
<span data-ttu-id="53e2b-145">วิธีนี้จะส่งกลับชื่อเหตุการณ์ touch</span><span class="sxs-lookup"><span data-stu-id="53e2b-145">This method returns touch start event name.</span></span>

#### `touchEndEventName`
```typescript
function touchEndEventName(): string
```
<span data-ttu-id="53e2b-146">วิธีนี้จะส่งกลับชื่อเหตุการณ์ touch</span><span class="sxs-lookup"><span data-stu-id="53e2b-146">This method returns touch start event name.</span></span>

#### `usePointerEvents`
```typescript
function usePointerEvents(): boolean
```
<span data-ttu-id="53e2b-147">วิธีการนี้จะส่งกลับเป็นเหตุการณ์ touchStart ปัจจุบันที่เกี่ยวข้องกับตัวชี้หรือไม่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="53e2b-147">This method returns is current touchStart event related to pointer or not.</span></span>
