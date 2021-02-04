---
title: บทนำสู่การใช้งานยูทิลิตี้การทดสอบของวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการใช้ยูทิลิตี้การทดสอบเพื่อลดความซับซ้อนของการจำลองและการใช้วิธีเฉพาะในการทดสอบหน่วยสำหรับวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.date: 02/14/2020
ms.openlocfilehash: 4b2a846f4905c4cb28fe92043cf3c71750b40f11
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888063"
---
# <a name="power-bi-visuals-test-utils"></a><span data-ttu-id="f72a6-104">Utils การทดสอบวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="f72a6-104">Power BI visuals test utils</span></span>

<span data-ttu-id="f72a6-105">บทความนี้จะช่วยคุณในการติดตั้ง นำเข้า และใช้ Utils การทดสอบวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="f72a6-105">This article helps you install, import, and use the Power BI visuals test utils.</span></span> <span data-ttu-id="f72a6-106">ยูทิลิตี้ทดสอบเหล่านี้สามารถใช้สำหรับการทดสอบหน่วย และรวม การทดสอบและวิธีการสำหรับองค์ประกอบต่าง ๆ เช่น มุมมองข้อมูล การเลือก และแบบแผนสี</span><span class="sxs-lookup"><span data-stu-id="f72a6-106">These test utilities can be used for unit testing and include mocks and methods for elements such as data views, selections and color schemas.</span></span>

## <a name="requirements"></a><span data-ttu-id="f72a6-107">ข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="f72a6-107">Requirements</span></span>

<span data-ttu-id="f72a6-108">หากต้องการใช้แพคเกจนี้ คุณจะต้องทำการติดตั้งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f72a6-108">To use this package, you'll need to install the following:</span></span>

* <span data-ttu-id="f72a6-109">[node.js](https://nodejs.org) ขอแนะนำให้ใช้เวอร์ชัน LTS</span><span class="sxs-lookup"><span data-stu-id="f72a6-109">[node.js](https://nodejs.org), it's recommended to use the LTS version</span></span>
* <span data-ttu-id="f72a6-110">[npm](https://www.npmjs.com/) เวอร์ชัน 3.0.0 หรือสูงกว่า</span><span class="sxs-lookup"><span data-stu-id="f72a6-110">[npm](https://www.npmjs.com/), version 3.0.0 or higher</span></span>
* <span data-ttu-id="f72a6-111">แพคเกจ [PowerBI-visuals-tools](https://github.com/Microsoft/PowerBI-visuals-tools)</span><span class="sxs-lookup"><span data-stu-id="f72a6-111">The [PowerBI-visuals-tools](https://github.com/Microsoft/PowerBI-visuals-tools) package</span></span>

## <a name="installation"></a><span data-ttu-id="f72a6-112">การติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="f72a6-112">Installation</span></span>

<span data-ttu-id="f72a6-113">หากต้องการติดตั้ง Utils การทดสอบและเพิ่มการขึ้นต่อกันของแพคเกจ *package.json* ให้เรียกใช้คำสั่งต่อไปนี้จากไดเรกทอรีวิชวล Power BI ของคุณ:</span><span class="sxs-lookup"><span data-stu-id="f72a6-113">To install test utils and add its dependency to your *package.json*, run the following command from your Power BI visuals directory:</span></span>

```bash
npm install powerbi-visuals-utils-testutils --save
```

<span data-ttu-id="f72a6-114">ต่อไปนี้จะให้คำอธิบายและตัวอย่างเกี่ยวกับ API สาธารณะของ Utils การทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f72a6-114">The following provide descriptions and examples on the test utils public API.</span></span>

## <a name="visualbuilderbase"></a><span data-ttu-id="f72a6-115">VisualBuilderBase</span><span class="sxs-lookup"><span data-stu-id="f72a6-115">VisualBuilderBase</span></span>

<span data-ttu-id="f72a6-116">ใช้โดย **VisualBuilder** ในหน่วยการทดสอบด้วยวิธีการที่ใช้บ่อยที่สุด `build`, `update` และ `updateRenderTimeout`</span><span class="sxs-lookup"><span data-stu-id="f72a6-116">Used by **VisualBuilder** in unit-tests with the most frequently used methods `build`, `update`, and `updateRenderTimeout`.</span></span> 

<span data-ttu-id="f72a6-117">วิธีการ `build` จะแสดงอินสแตนซ์ที่สร้างขึ้นของวิชวล</span><span class="sxs-lookup"><span data-stu-id="f72a6-117">The `build` method returns a created instance of the visual.</span></span>

<span data-ttu-id="f72a6-118">จำเป็นต้องมีวิธีการ `enumerateObjectInstances` และ `updateEnumerateObjectInstancesRenderTimeout` ในการตรวจสอบการเปลี่ยนแปลงบนตัวเลือกการจัดรูปแบบและบักเก็ต</span><span class="sxs-lookup"><span data-stu-id="f72a6-118">The `enumerateObjectInstances` and `updateEnumerateObjectInstancesRenderTimeout` methods are required to check changes on the bucket and formatting options.</span></span>

```typescript
abstract class VisualBuilderBase<T extends IVisual> {
    element: JQuery;
    viewport: IViewport;
    visualHost: IVisualHost;
    protected visual: T;
    constructor(width?: number, height?: number, guid?: string, element?: JQuery);
    protected abstract build(options: VisualConstructorOptions): T;
     nit(): void;
    destroy(): void;
    update(dataView: DataView[] | DataView): void;
    updateRenderTimeout(dataViews: DataView[] | DataView, fn: Function, timeout?: number): number;
    updateEnumerateObjectInstancesRenderTimeout(dataViews: DataView[] | DataView, options: EnumerateVisualObjectInstancesOptions, fn: (enumeration: VisualObjectInstance[]) => void, timeout?: number): number;
    updateFlushAllD3Transitions(dataViews: DataView[] | DataView): void;
    updateflushAllD3TransitionsRenderTimeout(dataViews: DataView[] | DataView, fn: Function, timeout?: number): number;
    enumerateObjectInstances(options: EnumerateVisualObjectInstancesOptions): VisualObjectInstance[];
}
```

> [!NOTE]
> <span data-ttu-id="f72a6-119">สำหรับตัวอย่างเพิ่มเติม ให้ดู [การเขียนการทดสอบหน่วย VisualBuilderBase](./unit-tests-introduction.md#create-a-visual-instance-builder) และ[สถานการณ์สมมติ VisualBuilderBase ในการใช้งานจริง](https://github.com/microsoft/powerbi-visuals-gantt/blob/master/test/visualBuilder.ts)</span><span class="sxs-lookup"><span data-stu-id="f72a6-119">For further examples, see [writing VisualBuilderBase unit tests](./unit-tests-introduction.md#create-a-visual-instance-builder) and a [real usage VisualBuilderBase scenario](https://github.com/microsoft/powerbi-visuals-gantt/blob/master/test/visualBuilder.ts).</span></span>

## <a name="dataviewbuilder"></a><span data-ttu-id="f72a6-120">DataViewBuilder</span><span class="sxs-lookup"><span data-stu-id="f72a6-120">DataViewBuilder</span></span>

<span data-ttu-id="f72a6-121">ใช้โดย **TestDataViewBuilder** โมดูลนี้แสดงคลาส **CategoricalDataViewBuilder** ที่ใช้ในวิธีการ `createCategoricalDataViewBuilder`</span><span class="sxs-lookup"><span data-stu-id="f72a6-121">Used by **TestDataViewBuilder**, this module provides a **CategoricalDataViewBuilder** class used in the `createCategoricalDataViewBuilder` method.</span></span> <span data-ttu-id="f72a6-122">นอกจากนี้ยังระบุอินเทอร์เฟซและวิธีการที่จำเป็นสำหรับการทำงานกับ **DataView** ที่ทดสอบแล้วในหน่วยการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f72a6-122">It also specifies interfaces and methods required for working with mocked **DataView** in unit-tests.</span></span>

* <span data-ttu-id="f72a6-123">`withValues` เพิ่มคอลัมน์ชุดข้อมูลคงที่และ `withGroupedValues` เพิ่มคอลัมน์ชุดข้อมูลแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="f72a6-123">`withValues` adds static series columns and `withGroupedValues` adds dynamic series columns</span></span>

  <span data-ttu-id="f72a6-124">ไม่ต้องใช้ทั้งชุดข้อมูลแบบไดนามิกและชุดข้อมูลแบบคงที่ในวิชวล **DataViewCategorical**</span><span class="sxs-lookup"><span data-stu-id="f72a6-124">Don't apply both dynamic series and static series in a visual **DataViewCategorical**.</span></span> <span data-ttu-id="f72a6-125">คุณสามารถใช้ได้ทั้งสองอย่างในคิวรี **DataViewCategorical** ซึ่ง **DataViewTransform**  ถูกคาดหวังว่าจะแยกออกเป็นวัตถุ **DataViewCategorical** ของวิชวลที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="f72a6-125">You can only use them both in the  **DataViewCategorical** query, where **DataViewTransform** is expected to split them into separate visual **DataViewCategorical** objects.</span></span>

* <span data-ttu-id="f72a6-126">`build` แสดง DataView พร้อมด้วยเมตาดาต้าและ DataViewCategorical</span><span class="sxs-lookup"><span data-stu-id="f72a6-126">`build` returns the DataView with metadata and DataViewCategorical</span></span>

  <span data-ttu-id="f72a6-127">`build` แสดง **ที่ไม่ได้กำหนดไว้** ถ้าการรวมของพารามิเตอร์ไม่ถูกต้องเช่น รวมทั้งชุดข้อมูลแบบไดนามิกและคงที่เมื่อสร้าง **DataView** ของวิชวล</span><span class="sxs-lookup"><span data-stu-id="f72a6-127">`build` returns **Undefined** if the combination of parameters is illegal, such as including both dynamic and static series when building the visual **DataView**.</span></span>

```typescript
class CategoricalDataViewBuilder implements IDataViewBuilderCategorical {
    withCategory(options: DataViewBuilderCategoryColumnOptions): IDataViewBuilderCategorical;
    withCategories(categories: DataViewCategoryColumn[]): IDataViewBuilderCategorical;
    withValues(options: DataViewBuilderValuesOptions): IDataViewBuilderCategorical;
    withGroupedValues(options: DataViewBuilderGroupedValuesOptions): IDataViewBuilderCategorical;
    build(): DataView;
}

function createCategoricalDataViewBuilder(): IDataViewBuilderCategorical;
```

## <a name="testdataviewbuilder"></a><span data-ttu-id="f72a6-128">TestDataViewBuilder</span><span class="sxs-lookup"><span data-stu-id="f72a6-128">TestDataViewBuilder</span></span>

<span data-ttu-id="f72a6-129">ใช้สำหรับการสร้าง **VisualData** ในการทดสอบหน่วย</span><span class="sxs-lookup"><span data-stu-id="f72a6-129">Used for **VisualData** creation in unit tests.</span></span> <span data-ttu-id="f72a6-130">เมื่อข้อมูลถูกใส่เข้าไปในบักเก็ตเขตข้อมูล Power BI จะสร้างวัตถุ **DataView** ตามประเภทที่ยึดตามข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f72a6-130">When data is placed in data-field buckets, Power BI produces a categorical **DataView** object based on the data.</span></span> <span data-ttu-id="f72a6-131">**TestDataViewBuilder** ช่วยจำลองการสร้าง **DataView** ตามประเภท</span><span class="sxs-lookup"><span data-stu-id="f72a6-131">The **TestDataViewBuilder** helps simulate categorical **DataView** creation.</span></span>

```typescript
abstract class TestDataViewBuilder {
    static DataViewName: string;
    private aggregateFunction;
    static setDefaultQueryName(source: DataViewMetadataColumn): DataViewMetadataColumn;
    static getDataViewBuilderColumnIdentitySources(options: TestDataViewBuilderColumnOptions[] | TestDataViewBuilderColumnOptions): DataViewBuilderColumnIdentitySource[];
    static getValuesTable(categories?: DataViewCategoryColumn[], values?: DataViewValueColumn[]): any[][];
    static createDataViewBuilderColumnOptions(categoriesColumns: (TestDataViewBuilderCategoryColumnOptions | TestDataViewBuilderCategoryColumnOptions[])[], valuesColumns: (DataViewBuilderValuesColumnOptions | DataViewBuilderValuesColumnOptions[])[], filter?: (options: TestDataViewBuilderColumnOptions) => boolean, customizeColumns?: CustomizeColumnFn): DataViewBuilderAllColumnOptions;
    static setUpDataViewBuilderColumnOptions(options: DataViewBuilderAllColumnOptions, aggregateFunction: (array: number[]) => number): DataViewBuilderAllColumnOptions;
    static setUpDataView(dataView: DataView, options: DataViewBuilderAllColumnOptions): DataView;
    protected createCategoricalDataViewBuilder(categoriesColumns: (TestDataViewBuilderCategoryColumnOptions | TestDataViewBuilderCategoryColumnOptions[])[], valuesColumns: (DataViewBuilderValuesColumnOptions | DataViewBuilderValuesColumnOptions[])[], columnNames: string[], customizeColumns?: CustomizeColumnFn): IDataViewBuilderCategorical;
    abstract getDataView(columnNames?: string[]): DataView;
}
```

  <span data-ttu-id="f72a6-132">ต่อไปนี้เป็นรายการอินเทอร์เฟซที่ใช้บ่อยที่สุดเมื่อสร้าง `testDataView`:</span><span class="sxs-lookup"><span data-stu-id="f72a6-132">The following lists the most frequently used interfaces when creating a `testDataView`:</span></span>

  ```typescript
  interface TestDataViewBuilderColumnOptions extends DataViewBuilderColumnOptions {
      values: any[];
  }

  interface TestDataViewBuilderCategoryColumnOptions extends TestDataViewBuilderColumnOptions {
      objects?: DataViewObjects[];
      isGroup?: boolean;
  }

  interface DataViewBuilderColumnOptions {
      source: DataViewMetadataColumn;
  }

  interface DataViewBuilderSeriesData {
      values: PrimitiveValue[];
      highlights?: PrimitiveValue[];
      /** Client-computed maximum value for a column. */
      maxLocal?: any;
      /** Client-computed maximum value for a column. */
      minLocal?: any;
  }

  interface DataViewBuilderColumnIdentitySource {
      fields: any[];
      identities?: CustomVisualOpaqueIdentity[];
  }
  ```
   
> [!NOTE]
> <span data-ttu-id="f72a6-133">สำหรับตัวอย่างเพิ่มเติม ให้ดู [การเขียนการทดสอบหน่วย TestDataViewBuilder ](./unit-tests-introduction.md#how-to-add-static-data-for-unit-tests) และ[สถานการณ์สมมติ TestDataViewBuilder ในการใช้งานจริง](https://github.com/microsoft/powerbi-visuals-gantt/blob/master/test/visualData.ts)</span><span class="sxs-lookup"><span data-stu-id="f72a6-133">For further examples, see [writing TestDataViewBuilder unit tests](./unit-tests-introduction.md#how-to-add-static-data-for-unit-tests) and a [real usage TestDataViewBuilder scenario](https://github.com/microsoft/powerbi-visuals-gantt/blob/master/test/visualData.ts).</span></span>

## <a name="mocks"></a><span data-ttu-id="f72a6-134">การทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f72a6-134">Mocks</span></span>

### <a name="mockivisualhost"></a><span data-ttu-id="f72a6-135">MockIVisualHost</span><span class="sxs-lookup"><span data-stu-id="f72a6-135">MockIVisualHost</span></span>

<span data-ttu-id="f72a6-136">ใช้ **IVisualHost** เพื่อทดสอบวิชวล Power BI โดยไม่มีการขึ้นต่อกันภายนอกเช่น เฟรมเวิร์ก Power BI</span><span class="sxs-lookup"><span data-stu-id="f72a6-136">Implements **IVisualHost** to test Power BI visuals without external dependencies, such as the Power BI framework.</span></span>

<span data-ttu-id="f72a6-137">วิธีการที่เป็นประโยชน์ประกอบด้วย `createSelectionIdBuilder`, `createSelectionManager`, `createLocalizationManager` และคุณสมบัติ Getter</span><span class="sxs-lookup"><span data-stu-id="f72a6-137">Useful methods include `createSelectionIdBuilder`, `createSelectionManager`, `createLocalizationManager`, and getter properties.</span></span>

```typescript
import powerbi from "powerbi-visuals-api";

import VisualObjectInstancesToPersist = powerbi.VisualObjectInstancesToPersist;
import ISelectionIdBuilder = powerbi.visuals.ISelectionIdBuilder;
import ISelectionManager = powerbi.extensibility.ISelectionManager;
import IColorPalette = powerbi.extensibility.IColorPalette;
import IVisualEventService = powerbi.extensibility.IVisualEventService;
import ITooltipService = powerbi.extensibility.ITooltipService;
import IVisualHost = powerbi.extensibility.visual.IVisualHost;

class MockIVisualHost implements IVisualHost {
      constructor(
          colorPalette?: IColorPalette,
          selectionManager?: ISelectionManager,
          tooltipServiceInstance?: ITooltipService,
          localeInstance?: MockILocale,
          allowInteractionsInstance?: MockIAllowInteractions,
          localizationManager?: powerbi.extensibility.ILocalizationManager,
          telemetryService?: powerbi.extensibility.ITelemetryService,
          authService?: powerbi.extensibility.IAuthenticationService,
          storageService?: ILocalVisualStorageService,
          eventService?: IVisualEventService);
      createSelectionIdBuilder(): ISelectionIdBuilder;
      createSelectionManager(): ISelectionManager;
      createLocalizationManager(): ILocalizationManager;
      colorPalette: IColorPalette;
      locale: string;
      telemetry: ITelemetryService;
      tooltipService: ITooltipService;
      allowInteractios: boolean;
      storageService: ILocalVisualStorageService;
      eventService: IVisualEventService;
      persistProperties(changes: VisualObjectInstancesToPersist): void;
}
```
   
- <span data-ttu-id="f72a6-138">`createVisualHost` สร้างและแสดงอินสแตนซ์ของ **IVisualHost** จริง ๆ แล้วคือ **MockIVisualHost**</span><span class="sxs-lookup"><span data-stu-id="f72a6-138">`createVisualHost` creates and returns instance of **IVisualHost**, actually **MockIVisualHost**</span></span>
  ```typescript
  function createVisualHost(locale?: Object, allowInteractions?: boolean, colors?: IColorInfo[], isEnabled?: boolean, displayNames?: any, token?: string): IVisualHost;
  ```

    <span data-ttu-id="f72a6-139">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f72a6-139">Example</span></span>
    ```typescript
    import { createVisualHost } from "powerbi-visuals-utils-testutils"

    let host: IVisualHost = createVisualHost();
    ```

> [!IMPORTANT]
> <span data-ttu-id="f72a6-140">**MockIVisualHost** เป็นการดำเนินการหลอกของ **IVisualHost** และควรใช้กับหน่วยการทดสอบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f72a6-140">**MockIVisualHost** is a fake implementation of **IVisualHost** and should only be used with unit-tests.</span></span>

### <a name="mockicolorpalette"></a><span data-ttu-id="f72a6-141">MockIColorPalette</span><span class="sxs-lookup"><span data-stu-id="f72a6-141">MockIColorPalette</span></span>

<span data-ttu-id="f72a6-142">ใช้ **IColorPalette** เพื่อทดสอบวิชวล Power BI โดยไม่มีการขึ้นต่อกันภายนอกเช่น เฟรมเวิร์ก Power BI</span><span class="sxs-lookup"><span data-stu-id="f72a6-142">Implements **IColorPalette** to test Power BI visuals without external dependencies, such as the Power BI Framework.</span></span>

<span data-ttu-id="f72a6-143">**MockIColorPalette** มีคุณสมบัติที่เป็นประโยชน์สำหรับการตรวจสอบแบบแผนสี หรือโหมดความคมชัดสูงในการทดสอบหน่วย</span><span class="sxs-lookup"><span data-stu-id="f72a6-143">**MockIColorPalette** provides useful properties for checking color schema or high-contrast mode in unit-tests.</span></span>

  ```typescript
  import powerbi from "powerbi-visuals-api";
  import IColorPalette = powerbi.extensibility.ISandboxExtendedColorPalette;
  import IColorInfo = powerbi.IColorInfo;

  class MockIColorPalette implements IColorPalette {
      constructor(colors?: IColorInfo[]);
      getColor(key: string): IColorInfo;
      reset(): IColorPalette;
      isHighContrastMode: boolean;
      foreground: {value: string};
      foregroundLight: {value: string};
      ...
      background: {value: string};
      backgroundLight: {value: string};
      ...
      shapeStroke: {value: string};
  }
  ```
  - <span data-ttu-id="f72a6-144">`createColorPalette` สร้างและแสดงอินสแตนซ์ของ **IColorPalette** จริง ๆ แล้วคือ **MockIColorPalette**</span><span class="sxs-lookup"><span data-stu-id="f72a6-144">`createColorPalette` creates and returns an instance of **IColorPalette**, actually **MockIColorPalette**</span></span>
    ```typescript
    function createColorPalette(colors?: IColorInfo[]): IColorPalette;
    ```

    <span data-ttu-id="f72a6-145">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f72a6-145">Example</span></span>
    ```typescript
    import { createColorPalette } from "powerbi-visuals-utils-testutils"

    let colorPalette: IColorPalette = createColorPalette();
    ```
    
> [!IMPORTANT]
> <span data-ttu-id="f72a6-146">**MockIColorPalette** เป็นการดำเนินการหลอกของ  **IColorPalette** และควรใช้กับหน่วยการทดสอบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f72a6-146">**MockIColorPalette** is a fake implementation of **IColorPalette** and should only be used with unit-tests.</span></span>

### <a name="mockiselectionid"></a><span data-ttu-id="f72a6-147">MockISelectionId</span><span class="sxs-lookup"><span data-stu-id="f72a6-147">MockISelectionId</span></span>

<span data-ttu-id="f72a6-148">ใช้ **ISelectionId** เพื่อทดสอบวิชวล Power BI โดยไม่มีการขึ้นต่อกันภายนอกเช่น เฟรมเวิร์ก Power BI</span><span class="sxs-lookup"><span data-stu-id="f72a6-148">Implements **ISelectionId** to test Power BI visuals without external dependencies, such as the Power BI Framework.</span></span>

  ```typescript
  import powerbi from "powerbi-visuals-api";
  import Selector = powerbi.data.Selector;
  import ISelectionId = powerbi.visuals.ISelectionId;

  class MockISelectionId implements ISelectionId {
      constructor(key: string);
      equals(other: ISelectionId): boolean;
      includes(other: ISelectionId, ignoreHighlight?: boolean): boolean;
      getKey(): string;
      getSelector(): Selector;
      getSelectorsByColumn(): Selector;
      hasIdentity(): boolean;
  }
  ```

  - <span data-ttu-id="f72a6-149">`createSelectionId` สร้างและแสดงอินสแตนซ์ของ **ISelectionId** จริง ๆ แล้วคือ **MockISelectionId**</span><span class="sxs-lookup"><span data-stu-id="f72a6-149">`createSelectionId` creates and returns an instance of **ISelectionId**, actually **MockISelectionId**</span></span>
    ```typescript
    function createSelectionId(key?: string): ISelectionId;
    ```

    <span data-ttu-id="f72a6-150">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f72a6-150">Example</span></span>
    ```typescript
    import { createColorPalette } from "powerbi-visuals-utils-testutils"

    let selectionId: ISelectionId = createSelectionId();
    ```
    
> [!NOTE]
> <span data-ttu-id="f72a6-151">**MockISelectionId** เป็นการดำเนินการหลอกของ  **ISelectionId** และควรใช้กับหน่วยการทดสอบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f72a6-151">**MockISelectionId** is a fake implementation of **ISelectionId** and should only be used with unit-tests.</span></span>

### <a name="mockiselectionidbuilder"></a><span data-ttu-id="f72a6-152">MockISelectionIdBuilder</span><span class="sxs-lookup"><span data-stu-id="f72a6-152">MockISelectionIdBuilder</span></span>

<span data-ttu-id="f72a6-153">ใช้ **ISelectionIdBuilder** เพื่อทดสอบวิชวล Power BI โดยไม่มีการขึ้นต่อกันภายนอกเช่น เฟรมเวิร์ก Power BI</span><span class="sxs-lookup"><span data-stu-id="f72a6-153">Implements **ISelectionIdBuilder** to test Power BI visuals without external dependencies, such as the Power BI Framework.</span></span> 

  ```typescript
  import DataViewCategoryColumn = powerbi.DataViewCategoryColumn;
  import DataViewValueColumn = powerbi.DataViewValueColumn;
  import DataViewValueColumnGroup = powerbi.DataViewValueColumnGroup;
  import DataViewValueColumns = powerbi.DataViewValueColumns;
  import ISelectionIdBuilder = powerbi.visuals.ISelectionIdBuilder;
  import ISelectionId = powerbi.visuals.ISelectionId;

  class MockISelectionIdBuilder implements ISelectionIdBuilder {
      withCategory(categoryColumn: DataViewCategoryColumn, index: number): this;
      withSeries(seriesColumn: DataViewValueColumns, valueColumn: DataViewValueColumn | DataViewValueColumnGroup): this;
      withMeasure(measureId: string): this;
      createSelectionId(): ISelectionId;
      withMatrixNode(matrixNode: DataViewMatrixNode, levels: DataViewHierarchyLevel[]): this;
      withTable(table: DataViewTable, rowIndex: number): this;
  }
  ```

  - <span data-ttu-id="f72a6-154">`createSelectionIdBuilder` สร้างและแสดงอินสแตนซ์ของ **ISelectionIdBuilder** จริง ๆ แล้วคือ **MockISelectionIdBuilder**</span><span class="sxs-lookup"><span data-stu-id="f72a6-154">`createSelectionIdBuilder` creates and returns an instance of **ISelectionIdBuilder**, actually **MockISelectionIdBuilder**</span></span>
    ```typescript
    function createSelectionIdBuilder(): ISelectionIdBuilder;
    ```

    <span data-ttu-id="f72a6-155">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f72a6-155">Example</span></span>
    ```typescript
    import { selectionIdBuilder } from "powerbi-visuals-utils-testutils";

    let selectionIdBuilder = createSelectionIdBuilder();
    ```

> [!NOTE]
> <span data-ttu-id="f72a6-156">**MockISelectionIdBuilder** เป็นการดำเนินการหลอกของ  **ISelectionIdBuilder** และควรใช้กับหน่วยการทดสอบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f72a6-156">**MockISelectionIdBuilder** is a fake implementation of **ISelectionIdBuilder** and should only be used with unit-tests.</span></span>

### <a name="mockiselectionmanager"></a><span data-ttu-id="f72a6-157">MockISelectionManager</span><span class="sxs-lookup"><span data-stu-id="f72a6-157">MockISelectionManager</span></span>

<span data-ttu-id="f72a6-158">ใช้ **ISelectionManager** เพื่อทดสอบวิชวล Power BI โดยไม่มีการขึ้นต่อกันภายนอกเช่น เฟรมเวิร์ก Power BI</span><span class="sxs-lookup"><span data-stu-id="f72a6-158">Implements **ISelectionManager** to test Power BI visuals without external dependencies, such as the Power BI Framework.</span></span> 

  ```typescript
  import powerbi from "powerbi-visuals-api";
  import IPromise = powerbi.IPromise;
  import ISelectionId = powerbi.visuals.ISelectionId;
  import ISelectionManager = powerbi.extensibility.ISelectionManager;

  class MockISelectionManager implements ISelectionManager {
      select(selectionId: ISelectionId | ISelectionId[], multiSelect?: boolean): IPromise<ISelectionId[]>;
      hasSelection(): boolean;
      clear(): IPromise<{}>;
      getSelectionIds(): ISelectionId[];
      containsSelection(id: ISelectionId): boolean;
      showContextMenu(selectionId: ISelectionId, position: IPoint): IPromise<{}>;
      registerOnSelectCallback(callback: (ids: ISelectionId[]) => void): void;
      simutateSelection(selections: ISelectionId[]): void;
  }
  ```

  - <span data-ttu-id="f72a6-159">`createSelectionManager` สร้างและแสดงอินสแตนซ์ของ **ISelectionManager** จริง ๆ แล้วคือ **MockISelectionManager**</span><span class="sxs-lookup"><span data-stu-id="f72a6-159">`createSelectionManager` creates and returns an instance of **ISelectionManager**, actually **MockISelectionManager**</span></span>
    ```typescript
    function createSelectionManager(): ISelectionManager
    ```

    <span data-ttu-id="f72a6-160">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f72a6-160">Example</span></span>
    ```typescript
    import { createSelectionManager } from "powerbi-visuals-utils-testutils";

    let selectionManager: ISelectionManager = createSelectionManager();
    ```

> [!NOTE]
> <span data-ttu-id="f72a6-161">**MockISelectionManager** เป็นการดำเนินการหลอกของ  **ISelectionManager** และควรใช้กับหน่วยการทดสอบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f72a6-161">**MockISelectionManager** is a fake implementation of **ISelectionManager** and should only be used with unit-tests.</span></span>

### <a name="mockilocale"></a><span data-ttu-id="f72a6-162">MockILocale</span><span class="sxs-lookup"><span data-stu-id="f72a6-162">MockILocale</span></span>

  <span data-ttu-id="f72a6-163">ตั้งค่าภาษาและเปลี่ยนแปลงภาษาสำหรับความต้องการของคุณในระหว่างกระบวนการทดสอบหน่วย</span><span class="sxs-lookup"><span data-stu-id="f72a6-163">Sets locale and changes it for your needs during unit-testing process.</span></span>
  ```typescript
  class MockILocale {
      constructor(locales?: Object): void; // Default locales are en-US and ru-RU 
      locale(key: string): void;// setter property
      locale(): string; // getter property
  }
  ```
  - <span data-ttu-id="f72a6-164">`createLocale` สร้างและแสดงอินสแตนซ์ของ **MockILocale**</span><span class="sxs-lookup"><span data-stu-id="f72a6-164">`createLocale` creates and returns instance of **MockILocale**</span></span>
    ```typescript
    funciton createLocale(locales?: Object): MockILocale;
    ```

### <a name="mockitooltipservice"></a><a id="mockitooltipservice"></a> <span data-ttu-id="f72a6-165">MockITooltipService</span><span class="sxs-lookup"><span data-stu-id="f72a6-165">MockITooltipService</span></span>
<span data-ttu-id="f72a6-166">จำลอง `TooltipService` และเรียกใช้สำหรับความต้องการของคุณในระหว่างกระบวนการทดสอบหน่วย</span><span class="sxs-lookup"><span data-stu-id="f72a6-166">Simulates `TooltipService` and calls it for your needs during unit-testing process.</span></span>
  ```typescript
  class MockITooltipService implements ITooltipService {
      constructor(isEnabled: boolean = true);
      enabled(): boolean;
      show(options: TooltipShowOptions): void;
      move(options: TooltipMoveOptions): void;
      hide(options: TooltipHideOptions): void;
  }
  ```
  - <span data-ttu-id="f72a6-167">`createTooltipService` สร้างและแสดงอินสแตนซ์ของ **MockITooltipService**</span><span class="sxs-lookup"><span data-stu-id="f72a6-167">`createTooltipService` creates and returns instance of **MockITooltipService**</span></span>
    ```typescript
    function createTooltipService(isEnabled?: boolean): ITooltipService;
    ```

### <a name="mockiallowinteractions"></a><span data-ttu-id="f72a6-168">MockIAllowInteractions</span><span class="sxs-lookup"><span data-stu-id="f72a6-168">MockIAllowInteractions</span></span>

```typescript
export class MockIAllowInteractions {
    constructor(public isEnabled?: boolean); // false by default
}
```
  - <span data-ttu-id="f72a6-169">`createAllowInteractions` สร้างและแสดงอินสแตนซ์ของ **MockIAllowInteractions**</span><span class="sxs-lookup"><span data-stu-id="f72a6-169">`createAllowInteractions` creates and returns instance of **MockIAllowInteractions**</span></span>
    ```typescript
    function createAllowInteractions(isEnabled?: boolean): MockIAllowInteractions;
    ```

### <a name="mockilocalizationmanager"></a><a id="mockilocalizationmanager"></a> <span data-ttu-id="f72a6-170">MockILocalizationManager</span><span class="sxs-lookup"><span data-stu-id="f72a6-170">MockILocalizationManager</span></span>
<span data-ttu-id="f72a6-171">มีความสามารถพื้นฐานของ **LocalizationManager** ซึ่งจำเป็นสำหรับการทดสอบหน่วย</span><span class="sxs-lookup"><span data-stu-id="f72a6-171">Provides basic abilities of **LocalizationManager** which are needed for unit-testing.</span></span>
```typescript
class MockILocalizationManager implements ILocalizationManager {
    constructor(displayNames: {[key: string]: string});
    getDisplayName(key: string): string; // returns default or setted displayNames for localized elements
}
```
  - <span data-ttu-id="f72a6-172">`createLocalizationManager` สร้างและแสดงอินสแตนซ์ของ **ILocalizationManager** จริง ๆ แล้วคือ **MockILocalizationManager**</span><span class="sxs-lookup"><span data-stu-id="f72a6-172">`createLocalizationManager` creates and returns an instance of **ILocalizationManager**, actually **MockILocalizationManager**</span></span>
    ```typescript
    function createLocalizationManager(displayNames?: any): ILocalizationManager;
    ```

    <span data-ttu-id="f72a6-173">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f72a6-173">Example</span></span>
    ```typescript
    import { createLocalizationManager } from "powerbi-visuals-utils-testutils";
    let localizationManagerMock: ILocalizationManager = createLocalizationManager();
    ```

### <a name="mockitelemetryservice"></a><span data-ttu-id="f72a6-174">MockITelemetryService</span><span class="sxs-lookup"><span data-stu-id="f72a6-174">MockITelemetryService</span></span>
<span data-ttu-id="f72a6-175">จำลองการใช้งาน **TelemetryService**</span><span class="sxs-lookup"><span data-stu-id="f72a6-175">Simulates **TelemetryService** usage.</span></span>
```typescript
class MockITelemetryService implements ITelemetryService {
    instanceId: string;
    trace(veType: powerbi.VisualEventType, payload?: string) {
    }
}
```
  <span data-ttu-id="f72a6-176">การสร้าง `MockITelemetryService`</span><span class="sxs-lookup"><span data-stu-id="f72a6-176">Creation of `MockITelemetryService`</span></span>
    ```typescript
    function createTelemetryService(): ITelemetryService;
    ```
### <a name="mockiauthenticationservice"></a><span data-ttu-id="f72a6-177">MockIAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="f72a6-177">MockIAuthenticationService</span></span>
<span data-ttu-id="f72a6-178">จำลองการทำงานของ **AuthenticationService** โดยการกำหนดโทเค็น AAD ที่ทดสอบแล้ว</span><span class="sxs-lookup"><span data-stu-id="f72a6-178">Simulates the work of **AuthenticationService** by providing a mocked AAD token.</span></span>
```typescript
class MockIAuthenticationService implements IAuthenticationService  {
    constructor(token: string);
    getAADToken(visualId?: string): powerbi.IPromise<string>
}
```
  - <span data-ttu-id="f72a6-179">`createAuthenticationService` สร้างและแสดงอินสแตนซ์ของ **IAuthenticationService** จริง ๆ แล้วคือ **MockIAuthenticationService**</span><span class="sxs-lookup"><span data-stu-id="f72a6-179">`createAuthenticationService` creates and returns an instance of **IAuthenticationService**, actually **MockIAuthenticationService**</span></span>
    ```typescript
    function createAuthenticationService(token?: string): IAuthenticationService;
    ```

### <a name="mockistorageservice"></a><span data-ttu-id="f72a6-180">MockIStorageService</span><span class="sxs-lookup"><span data-stu-id="f72a6-180">MockIStorageService</span></span>
<span data-ttu-id="f72a6-181">ช่วยให้คุณสามารถใช้ **ILocalVisualStorageService** กับลักษณะการทำงานเดียวกันกับ **LocalStorage**</span><span class="sxs-lookup"><span data-stu-id="f72a6-181">Allows you to use **ILocalVisualStorageService** with the same behavior as **LocalStorage**.</span></span>
```typescript
class MockIStorageService implements ILocalVisualStorageService {
  get(key: string): IPromise<string>;
  set(key: string, data: string): IPromise<number>;
  remove(key: string): void;
}
```
  - <span data-ttu-id="f72a6-182">`createStorageService` สร้างและแสดงอินสแตนซ์ของ **ILocalVisualStorageService** จริง ๆ แล้วคือ **MockIStorageService**</span><span class="sxs-lookup"><span data-stu-id="f72a6-182">`createStorageService` creates and returns an instance of **ILocalVisualStorageService**, actually **MockIStorageService**</span></span>
    ```typescript
    function createStorageService(): ILocalVisualStorageService;
    ```

### <a name="mockieventservice"></a><span data-ttu-id="f72a6-183">MockIEventService</span><span class="sxs-lookup"><span data-stu-id="f72a6-183">MockIEventService</span></span>
```typescript
import powerbi from "powerbi-visuals-api";
import IVisualEventService = powerbi.extensibility.IVisualEventService;
import VisualUpdateOptions = powerbi.extensibility.VisualUpdateOptions;

class MockIEventService implements IVisualEventService {
      renderingStarted(options: VisualUpdateOptions): void;
      renderingFinished(options: VisualUpdateOptions): void;
      renderingFailed(options: VisualUpdateOptions, reason?: string): void;
}
```
  - <span data-ttu-id="f72a6-184">`createEventService` สร้างและแสดงอินสแตนซ์ของ **IVisualEventService** จริง ๆ แล้วคือ **MockIEventService**</span><span class="sxs-lookup"><span data-stu-id="f72a6-184">`createEventService` creates and returns an instance of **IVisualEventService**, actually **MockIEventService**</span></span>
    ```typescript
    function createEventService(): IVisualEventService;
    ```

## <a name="utils"></a><span data-ttu-id="f72a6-185">Utils</span><span class="sxs-lookup"><span data-stu-id="f72a6-185">Utils</span></span>

<span data-ttu-id="f72a6-186">Utils ประกอบด้วยวิธีการของตัวช่วยเหลือสำหรับการทดสอบหน่วยของ Power BI ที่รวมถึงตัวช่วยเหลือที่เกี่ยวข้องกับสี ตัวเลข และเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="f72a6-186">Utils include helper methods for Power BI visuals' unit testing, including helpers related to colors, numbers, and events.</span></span>

- <span data-ttu-id="f72a6-187">`renderTimeout`แสดงไทม์เอาต์</span><span class="sxs-lookup"><span data-stu-id="f72a6-187">`renderTimeout` returns timeout</span></span>
  ```typescript
  function renderTimeout(fn: Function, timeout: number = DefaultWaitForRender): number
  ```

- <span data-ttu-id="f72a6-188">`testDom` ช่วยตั้งค่าการแข่งขันในการทดสอบหน่วย</span><span class="sxs-lookup"><span data-stu-id="f72a6-188">`testDom` helps set fixture in unit tests</span></span>
  ```typescript
  function testDom(height: number | string, width: number | string): JQuery
  ```
  <span data-ttu-id="f72a6-189">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f72a6-189">Example</span></span>
  ```typescript
  import { testDom }  from "powerbi-visuals-utils-testutils";
  describe("testDom", () => {
      it("should return an element", () => {
          let element: JQuery = testDom(500, 500);
          expect(element.get(0)).toBeDefined();
      });
  });
  ```

### <a name="color-related-helper-methods"></a><span data-ttu-id="f72a6-190">วิธีการของตัวช่วยเหลือที่เกี่ยวข้องกับสี</span><span class="sxs-lookup"><span data-stu-id="f72a6-190">Color-related helper methods</span></span>

- `getSolidColorStructuralObject`
  ```typescript
  function getSolidColorStructuralObject(color: string): any
  ```
  <span data-ttu-id="f72a6-191">แสดงโครงสร้างต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f72a6-191">Returns the following structure:</span></span>

  ```json
  { solid: { color: color } }
  ```

- <span data-ttu-id="f72a6-192">`assertColorsMatch` เปรียบเทียบวัตถุ **RgbColor** ที่แยกวิเคราะห์จากสตริงที่ป้อนเข้า</span><span class="sxs-lookup"><span data-stu-id="f72a6-192">`assertColorsMatch` compares **RgbColor** objects parsed from input strings</span></span>
  ```typescript
  function assertColorsMatch(actual: string, expected: string, invert: boolean = false): boolean
  ```

- <span data-ttu-id="f72a6-193">`parseColorString`แยกวิเคราะห์สีจากสตริงที่ป้อนข้อมูลและแสดงในอินเทอร์เฟซที่ระบุ **RgbColor**</span><span class="sxs-lookup"><span data-stu-id="f72a6-193">`parseColorString` parses color from the input string and returns it in specified interface **RgbColor**</span></span>
  ```typescript
  function parseColorString(color: string): RgbColor
  ```

### <a name="number-related-helper-methods"></a><span data-ttu-id="f72a6-194">วิธีการของตัวช่วยเหลือที่เกี่ยวข้องกับตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f72a6-194">Number-related helper methods</span></span>

- <span data-ttu-id="f72a6-195">`getRandomNumbers` สร้างตัวเลขสุ่มโดยใช้ค่าต่ำสุดและค่าสูงสุด</span><span class="sxs-lookup"><span data-stu-id="f72a6-195">`getRandomNumbers` generates a random number using min and max values.</span></span> <span data-ttu-id="f72a6-196">คุณสามารถระบุ `exceptionList` และให้ฟังก์ชันสำหรับการเปลี่ยนแปลงผลลัพธ์ได้</span><span class="sxs-lookup"><span data-stu-id="f72a6-196">You can specify `exceptionList` and provide a function for result change.</span></span>
  ```typescript
  function getRandomNumber(
      min: number,
      max: number,
      exceptionList?: number[],
      changeResult: (value: any) => number = x => x): number
  ```

- <span data-ttu-id="f72a6-197">`getRandomNumbers` แสดงอาร์เรย์ของตัวเลขสุ่มที่สร้างขึ้นโดยวิธีการ `getRandomNumber` ด้วยค่าต่ำสุดและค่าสูงสุดที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f72a6-197">`getRandomNumbers` provides an array of random numbers generated by the `getRandomNumber` method with specified min and max values</span></span>
  ```typescript
  function getRandomNumbers(count: number, min: number = 0, max: number = 1): number[]
  ```

### <a name="event-related-helper-methods"></a><span data-ttu-id="f72a6-198">วิธีการของตัวช่วยเหลือที่เกี่ยวข้องกับเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="f72a6-198">Event-related helper methods</span></span>
<span data-ttu-id="f72a6-199">วิธีการต่อไปนี้จะถูกเขียนขึ้นสำหรับการจำลองเหตุการณ์ของเว็บเพจในการทดสอบหน่วย</span><span class="sxs-lookup"><span data-stu-id="f72a6-199">The following methods are written for web page event simulation in unit tests.</span></span>

- <span data-ttu-id="f72a6-200">`clickElement` จำลองการคลิกที่องค์ประกอบที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f72a6-200">`clickElement` simulates a click on the specified element</span></span>
  ```typescript
  function clickElement(element: JQuery, ctrlKey: boolean = false): void
  ```

- <span data-ttu-id="f72a6-201">`createTouch` แสดงวัตถุ **การสัมผัส** เพื่อช่วยในการจำลองเหตุการณ์การสัมผัส</span><span class="sxs-lookup"><span data-stu-id="f72a6-201">`createTouch` returns a **Touch** object to help simulate a touch event</span></span>
  ```typescript
  function createTouch(x: number, y: number, element: JQuery, id: number = 0): Touch
  ```

- <span data-ttu-id="f72a6-202">`createTouchesList` แสดงรายการของเหตุการณ์ **การสัมผัส** แบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="f72a6-202">`createTouchesList` returns a list of simulated **Touch** events</span></span>
  ```typescript
  function createTouchesList(touches: Touch[]): TouchList
  ```

- <span data-ttu-id="f72a6-203">`createContextMenuEvent` แสดง **MouseEvent**</span><span class="sxs-lookup"><span data-stu-id="f72a6-203">`createContextMenuEvent` returns **MouseEvent**</span></span>
  ```typescript
  function createContextMenuEvent(x: number, y: number): MouseEvent
  ```

- <span data-ttu-id="f72a6-204">`createMouseEvent` สร้างและแสดง **MouseEvent**</span><span class="sxs-lookup"><span data-stu-id="f72a6-204">`createMouseEvent` creates and returns **MouseEvent**</span></span>
  ```typescript
  function createMouseEvent(
      mouseEventType: MouseEventType,
      eventType: ClickEventType,
      x: number,
      y: number,
      button: number = 0): MouseEvent
  ```

- `createTouchEndEvent`
  ```typescript
  function createTouchEndEvent(touchList?: TouchList): UIEvent
  ```

- `createTouchMoveEvent`
  ```typescript
  function createTouchMoveEvent(touchList?: TouchList): UIEvent
  ```

- `createTouchStartEvent`
  ```typescript
  function createTouchStartEvent(touchList?: TouchList): UIEvent
  ```

### <a name="d3-event-related-helper-methods"></a><span data-ttu-id="f72a6-205">วิธีการของตัวช่วยเหลือที่เกี่ยวข้องกับเหตุการณ์ D3</span><span class="sxs-lookup"><span data-stu-id="f72a6-205">D3 event-related helper methods</span></span>

<span data-ttu-id="f72a6-206">วิธีการต่อไปนี้จะใช้ในการจำลองเหตุการณ์ D3 ในการทดสอบหน่วย</span><span class="sxs-lookup"><span data-stu-id="f72a6-206">The following methods are used to simulate D3 events in unit tests.</span></span>

- <span data-ttu-id="f72a6-207">`flushAllD3Transitions` บังคับการเปลี่ยนแปลง D3 ทั้งหมดให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f72a6-207">`flushAllD3Transitions` forces all D3 transitions to complete</span></span>

  ```typescript
  function flushAllD3Transitions()
  ```
  
  > [!NOTE]
  > <span data-ttu-id="f72a6-208">ตามปกติ การเปลี่ยนช่วงการหน่วงเวลาศูนย์จะดำเนินการหลังจากการหน่วงเวลาแบบทันที (< 10 ms) แต่อาจทำให้เกิดการกะพริบแบบสั้นๆ ถ้าเบราว์เซอร์แสดงหน้าสองครั้ง</span><span class="sxs-lookup"><span data-stu-id="f72a6-208">Normally, zero-delay transitions are executed after an instantaneous delay (<10 ms), but this can cause a brief flicker if the browser renders the page twice.</span></span> <span data-ttu-id="f72a6-209">หนึ่งครั้งที่จุดสิ้นสุดของการวนรอบเหตุการณ์แรก แล้วอีกครั้งในการเรียกกลับตัวจับเวลาครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="f72a6-209">Once at the end of the first event loop, then again immediately on the first timer callback.</span></span>
  >
  > <span data-ttu-id="f72a6-210">กระพริบเหล่านี้จะเห็นได้ชัดขึ้นใน IE และมี Webviews จำนวนมาก และไม่แนะนำสำหรับ iOS</span><span class="sxs-lookup"><span data-stu-id="f72a6-210">These flickers are more noticeable on IE and with a large number of webviews and are not recommended for iOS.</span></span>
  > 
  > <span data-ttu-id="f72a6-211">ด้วยการล้างข้อมูลคิวตัวจับเวลาที่จุดสิ้นสุดของการวนรอบเหตุการณ์แรกคุณ สามารถเรียกใช้การเปลี่ยนการหน่วงเวลาศูนย์ใด ๆ ได้ทันทีและหลีกเลี่ยงการกะพริบ</span><span class="sxs-lookup"><span data-stu-id="f72a6-211">By flushing the timer queue at the end of the first event loop you can run any zero-delay transitions immediately and avoid the flicker.</span></span>

<span data-ttu-id="f72a6-212">นอกจากนี้ยังรวมวิธีการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f72a6-212">The following methods are also included:</span></span>
```typescript
function d3Click(element: JQuery, x: number, y: number, eventType?: ClickEventType, button?: number): void
function d3MouseUp(element: JQuery, x: number, y: number, eventType?: ClickEventType, button?: number): void
function d3MouseDown(element: JQuery, x: number, y: number, eventType?: ClickEventType, button?: number): void
function d3MouseOver(element: JQuery, x: number, y: number, eventType?: ClickEventType, button?: number): void
function d3MouseMove(element: JQuery, x: number, y: number, eventType?: ClickEventType, button?: number): void
function d3MouseOut(element: JQuery, x: number, y: number, eventType?: ClickEventType, button?: number): void
function d3KeyEvent(element: JQuery, typeArg: string, keyArg: string, keyCode: number): void
function d3TouchStart(element: JQuery, touchList?: TouchList): void
function d3TouchMove(element: JQuery, touchList?: TouchList): void
function d3TouchEnd(element: JQuery, touchList?: TouchList): void
function d3ContextMenu(element: JQuery, x: number, y: number): void
```

### <a name="helper-interfaces"></a><span data-ttu-id="f72a6-213">อินเทอร์เฟซตัวช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="f72a6-213">Helper interfaces</span></span>
<span data-ttu-id="f72a6-214">อินเทอร์เฟซและการแจกแจงต่อไปนี้จะใช้ในฟังก์ชันตัวช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="f72a6-214">The following interface and enumerations are used in the helper function.</span></span>

```typescript
interface RgbColor {
    R: number;
    G: number;
    B: number;
    A?: number; 
}

enum ClickEventType {
    Default = 0,
    CtrlKey = 1,
    AltKey = 2,
    ShiftKey = 4,
    MetaKey = 8,
}

enum MouseEventType {
    click,
    mousedown,
    mouseup,
    mouseover,
    mousemove,
    mouseout,
}
```

## <a name="next-steps"></a><span data-ttu-id="f72a6-215">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="f72a6-215">Next steps</span></span>

<span data-ttu-id="f72a6-216">เมื่อต้องการเขียนการทดสอบหน่วยสำหรับวิชวล Power BI ที่ใช้ Webpack และdkiทดสอบหน่วยด้วย `karma` และ `jasmine` โปรดดูตัวอย่าง [บทช่วยสอน: เพิ่มการทดสอบหน่วยสำหรับโครงการวิชวล Power BI ](./unit-tests-introduction.md)</span><span class="sxs-lookup"><span data-stu-id="f72a6-216">To write unit tests for webpack-based Power BI visuals, and unit test with `karma` and `jasmine`, see for example [Tutorial: Add unit tests for Power BI visual projects](./unit-tests-introduction.md).</span></span>
