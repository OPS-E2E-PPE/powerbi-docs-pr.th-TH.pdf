---
title: บทนำสู่การใช้งานยูทิลิตี้สีของวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการใช้ยูทิลิตี้แผนภูมิเพื่อวาดแกนและให้คำอธิบายวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
manager: rkarlin
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: reference
ms.date: 06/18/2019
ms.openlocfilehash: 9094d639225eb82cbcf427346d1ad78943ddc90f
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887879"
---
# <a name="chart-utils"></a><span data-ttu-id="176d9-104">ยูทิลิตี้แผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="176d9-104">Chart utils</span></span>

<span data-ttu-id="176d9-105">ChartUtils คือชุดของอินเทอร์เฟซและวิธีการในการสร้างแกน ป้ายชื่อข้อมูล และคำอธิบายแผนภูมิในการแสดงผลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="176d9-105">ChartUtils is a set of interfaces and methods for creating axis, data labels, and legends in Power BI Visuals.</span></span>

## <a name="installation"></a><span data-ttu-id="176d9-106">การติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="176d9-106">Installation</span></span>

<span data-ttu-id="176d9-107">หากต้องการติดตั้งแพ็คเกจ คุณควรเรียกใช้คำสั่งต่อไปนี้ในไดเรกทอรีด้วยวิชวลปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="176d9-107">To install the package, you should run the following command in the directory with your current visual:</span></span>

```bash
npm install powerbi-visuals-utils-chartutils --save
```

## <a name="axis-helper"></a><span data-ttu-id="176d9-108">ตัวช่วยแกน</span><span class="sxs-lookup"><span data-stu-id="176d9-108">Axis Helper</span></span>

<span data-ttu-id="176d9-109">ตัวช่วยแกน (วัตถุ`axis` ในยูทิลิตี้) มีฟังก์ชันเพื่อลดความซับซ้อนให้กับแกน</span><span class="sxs-lookup"><span data-stu-id="176d9-109">The axis helper (`axis` object in utils) provides functions to simplify manipulations with axis.</span></span>

<span data-ttu-id="176d9-110">โมดูลมอบฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="176d9-110">The module provides the following functions:</span></span>

### <a name="getrecommendednumberofticksforxaxis"></a><span data-ttu-id="176d9-111">getRecommendedNumberOfTicksForXAxis</span><span class="sxs-lookup"><span data-stu-id="176d9-111">getRecommendedNumberOfTicksForXAxis</span></span>

<span data-ttu-id="176d9-112">ฟังก์ชันนี้ส่งกลับจำนวนของเครื่องหมายที่แนะนำตามความกว้างของแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="176d9-112">This function returns recommended number of ticks according to width of chart.</span></span>

```typescript
function getRecommendedNumberOfTicksForXAxis(availableWidth: number): number;
```

<span data-ttu-id="176d9-113">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-113">Example:</span></span>

```typescript
import { axis } from "powerbi-visuals-utils-chartutils";
// ...
axis.getRecommendedNumberOfTicksForXAxis(1024);

// returns: 8
```

### <a name="getrecommendednumberofticksforyaxis"></a><span data-ttu-id="176d9-114">getRecommendedNumberOfTicksForYAxis</span><span class="sxs-lookup"><span data-stu-id="176d9-114">getRecommendedNumberOfTicksForYAxis</span></span>

<span data-ttu-id="176d9-115">ฟังก์ชันนี้ส่งกลับจำนวนของเครื่องหมายที่แนะนำตามความสูงของแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="176d9-115">This function returns recommended number of ticks according to height of chart.</span></span>

```typescript
function getRecommendedNumberOfTicksForYAxis(availableWidth: number);
```

<span data-ttu-id="176d9-116">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-116">Example:</span></span>

```typescript
import { axis } from "powerbi-visuals-utils-chartutils";
// ...
axis.getRecommendedNumberOfTicksForYAxis(100);

// returns: 3
```

### <a name="getbestnumberofticks"></a><span data-ttu-id="176d9-117">getBestNumberOfTicks</span><span class="sxs-lookup"><span data-stu-id="176d9-117">getBestNumberOfTicks</span></span>

<span data-ttu-id="176d9-118">รับจำนวนเครื่องหมายที่เหมาะสมที่สุดโดยยึดตามค่าต่ำสุดและค่าเมตาดาต้าหน่วยวัดและจำนวนเครื่องหมายสูงสุด</span><span class="sxs-lookup"><span data-stu-id="176d9-118">Gets the optimal number of ticks based on minimum value, maximum value, and measure metadata and max tick count;</span></span>

```typescript
function getBestNumberOfTicks(
  min: number,
  max: number,
  valuesMetadata: DataViewMetadataColumn[],
  maxTickCount: number,
  isDateTime?: boolean
): number;
```

<span data-ttu-id="176d9-119">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-119">Example:</span></span>

```typescript
import { axis } from "powerbi-visuals-utils-chartutils";
// ...
var dataViewMetadataColumnWithIntegersOnly: powerbi.DataViewMetadataColumn[] = [
  {
    displayName: "col1",
    isMeasure: true,
    type: ValueType.fromDescriptor({ integer: true })
  },
  {
    displayName: "col2",
    isMeasure: true,
    type: ValueType.fromDescriptor({ integer: true })
  }
];
var actual = axis.getBestNumberOfTicks(
  0,
  3,
  dataViewMetadataColumnWithIntegersOnly,
  6
);

// returns: 4
```

### <a name="getticklabelmargins"></a><span data-ttu-id="176d9-120">getTickLabelMargins</span><span class="sxs-lookup"><span data-stu-id="176d9-120">getTickLabelMargins</span></span>

<span data-ttu-id="176d9-121">ฟังก์ชันนี้ส่งกลับระยะขอบสำหรับป้ายชื่อเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="176d9-121">This function returns the margins for tick labels.</span></span>

```typescript
function getTickLabelMargins(
  viewport: IViewport,
  yMarginLimit: number,
  textWidthMeasurer: ITextAsSVGMeasurer,
  textHeightMeasurer: ITextAsSVGMeasurer,
  axes: CartesianAxisProperties,
  bottomMarginLimit: number,
  properties: TextProperties,
  scrollbarVisible?: boolean,
  showOnRight?: boolean,
  renderXAxis?: boolean,
  renderY1Axis?: boolean,
  renderY2Axis?: boolean
): TickLabelMargins;
```

<span data-ttu-id="176d9-122">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-122">Example:</span></span>

```typescript
import { axis } from "powerbi-visuals-utils-chartutils";
// ...

axis.getTickLabelMargins(
  plotArea,
  marginLimits.left,
  TextMeasurementService.measureSvgTextWidth,
  TextMeasurementService.estimateSvgTextHeight,
  axes,
  marginLimits.bottom,
  textProperties,
  /*scrolling*/ false,
  showY1OnRight,
  renderXAxis,
  renderY1Axis,
  renderY2Axis
);

// returns:  xMax, yLeft, yRight, stackHeigh;
```

### <a name="isordinal"></a><span data-ttu-id="176d9-123">isOrdinal</span><span class="sxs-lookup"><span data-stu-id="176d9-123">isOrdinal</span></span>

<span data-ttu-id="176d9-124">ตรวจสอบว่าสตริงเป็น null หรือไม่ได้กำหนดหรือว่างเปล่า หรือไม่</span><span class="sxs-lookup"><span data-stu-id="176d9-124">Checks if a string is null or undefined or empty.</span></span>

```typescript
function isOrdinal(type: ValueTypeDescriptor): boolean;
```

<span data-ttu-id="176d9-125">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-125">Example:</span></span>

```typescript
import { axis } from "powerbi-visuals-utils-chartutils";
// ...
let type = ValueType.fromDescriptor({ misc: { barcode: true } });
axis.isOrdinal(type);

// returns: true
```

### <a name="isdatetime"></a><span data-ttu-id="176d9-126">sDateTime</span><span class="sxs-lookup"><span data-stu-id="176d9-126">isDateTime</span></span>

<span data-ttu-id="176d9-127">ตรวจสอบว่าค่าเป็น DateTime หรือไม่</span><span class="sxs-lookup"><span data-stu-id="176d9-127">Checks if value is of DateTime type.</span></span>

```typescript
function isDateTime(type: ValueTypeDescriptor): boolean;
```

<span data-ttu-id="176d9-128">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-128">Example:</span></span>

```typescript
import { axis } from "powerbi-visuals-utils-chartutils";
// ...

axis.isDateTime(ValueType.fromDescriptor({ dateTime: true }));

// returns: true
```

### <a name="getcategorythickness"></a><span data-ttu-id="176d9-129">getCategoryThickness</span><span class="sxs-lookup"><span data-stu-id="176d9-129">getCategoryThickness</span></span>

<span data-ttu-id="176d9-130">ใช้สเกล D3 เพื่อรับความหนาของประเภทที่แท้จริง</span><span class="sxs-lookup"><span data-stu-id="176d9-130">Uses the D3 scale to get the actual category thickness.</span></span>

```typescript
function getCategoryThickness(scale: any): number;
```

<span data-ttu-id="176d9-131">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-131">Example:</span></span>

```typescript
import { axis } from "powerbi-visuals-utils-chartutils";
// ...

let range = [0, 100];
let domain = [0, 10];
let scale = d3.scale
  .linear()
  .domain(domain)
  .range(range);
let actualThickness = axis.getCategoryThickness(scale);
```

### <a name="invertordinalscale"></a><span data-ttu-id="176d9-132">invertOrdinalScale</span><span class="sxs-lookup"><span data-stu-id="176d9-132">invertOrdinalScale</span></span>

<span data-ttu-id="176d9-133">ฟังก์ชันนี้สลับสเกลลำดับ</span><span class="sxs-lookup"><span data-stu-id="176d9-133">This function inverts the ordinal scale.</span></span> <span data-ttu-id="176d9-134">ถ้า x < scale.range()[0] จากนั้นจะมีการส่งกลับ scale.domain()[0]</span><span class="sxs-lookup"><span data-stu-id="176d9-134">If x < scale.range()[0], then scale.domain()[0] is returned.</span></span>
<span data-ttu-id="176d9-135">มิฉะนั้นจะส่งกลับรายการที่ยิ่งใหญ่ที่สุดใน scale.domain() ที่ <= x</span><span class="sxs-lookup"><span data-stu-id="176d9-135">Otherwise, it returns the greatest item in scale.domain() that's <= x.</span></span>

```typescript
function invertOrdinalScale(scale: d3.scale.Ordinal<any, any>, x: number);
```

<span data-ttu-id="176d9-136">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-136">Example:</span></span>

```typescript
import { axis } from "powerbi-visuals-utils-chartutils";
// ...

let domain: number[] = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9],
  pixelSpan: number = 100,
  ordinalScale: d3.scale.ordinal = axis.createOrdinalScale(
    pixelSpan,
    domain,
    0.4
  );

axis.invertOrdinalScale(ordinalScale, 49);

// returns: 4
```

### <a name="findclosestxaxisindex"></a><span data-ttu-id="176d9-137">findClosestXAxisIndex</span><span class="sxs-lookup"><span data-stu-id="176d9-137">findClosestXAxisIndex</span></span>

<span data-ttu-id="176d9-138">ฟังก์ชันนี้จะค้นหาและส่งกลับดัชนีแกน x ที่ใกล้ที่สุด</span><span class="sxs-lookup"><span data-stu-id="176d9-138">This function finds and returns the closest x-axis index.</span></span>

```typescript
function findClosestXAxisIndex(
  categoryValue: number,
  categoryAxisValues: AxisHelperCategoryDataPoint[]
): number;
```

<span data-ttu-id="176d9-139">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-139">Example:</span></span>

```typescript
import { axis } from "powerbi-visuals-utils-chartutils";
// ...

/**
 * Finds the index of the category of the given x coordinate given.
 * pointX is in non-scaled screen-space, and offsetX is in render-space.
 * offsetX does not need any scaling adjustment.
 * @param {number} pointX The mouse coordinate in screen-space, without scaling applied
 * @param {number} offsetX Any left offset in d3.scale render-space
 * @return {number}
 */
private findIndex(pointX: number, offsetX?: number): number {
    // we are using mouse coordinates that do not know about any potential CSS transform scale
    let xScale = this.scaleDetector.getScale().x;
    if (!Double.equalWithPrecision(xScale, 1.0, 0.00001)) {
        pointX = pointX / xScale;
    }
    if (offsetX) {
        pointX += offsetX;
    }

    let index = axis.invertScale(this.xAxisProperties.scale, pointX);
    if (this.data.isScalar) {
        // When we have scalar data the inverted scale produces a category value, so we need to search for the closest index.
        index = axis.findClosestXAxisIndex(index, this.data.categoryData);
    }

    return index;
}
```

### <a name="diffscaled"></a><span data-ttu-id="176d9-140">diffScaled</span><span class="sxs-lookup"><span data-stu-id="176d9-140">diffScaled</span></span>

<span data-ttu-id="176d9-141">ฟังก์ชันนี้จะคำนวณและส่งกลับค่าที่แตกต่างในสเกล</span><span class="sxs-lookup"><span data-stu-id="176d9-141">This function computes and returns a diff of values in the scale.</span></span>

```typescript
function diffScaled(
  scale: d3.scale.Linear<any, any>,
  value1: any,
  value2: any
): number;
```

<span data-ttu-id="176d9-142">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-142">Example:</span></span>

```typescript
import { axis } from "powerbi-visuals-utils-chartutils";
// ...

var scale: d3.scale.Linear<number, number>,
    range = [0, 999],
    domain = [0, 1, 2, 3, 4, 5, 6, 7, 8, 999];

scale = d3.scale.linear()
    .range(range)
    .domain(domain);

return axis.diffScaled(scale, 0, 0));

// returns: 0
```

### <a name="createdomain"></a><span data-ttu-id="176d9-143">createDomain</span><span class="sxs-lookup"><span data-stu-id="176d9-143">createDomain</span></span>

<span data-ttu-id="176d9-144">ฟังก์ชันนี้จะสร้างโดเมนของค่าสำหรับแกน</span><span class="sxs-lookup"><span data-stu-id="176d9-144">This function creates a domain of values for axis.</span></span>

```typescript
function createDomain(
  data: any[],
  axisType: ValueTypeDescriptor,
  isScalar: boolean,
  forcedScalarDomain: any[],
  ensureDomain?: NumberRange
): number[];
```

<span data-ttu-id="176d9-145">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-145">Example:</span></span>

```typescript
import { axis } from "powerbi-visuals-utils-chartutils";
// ...

var cartesianSeries = [
  {
    data: [
      { categoryValue: 7, value: 11, categoryIndex: 0, seriesIndex: 0 },
      {
        categoryValue: 9,
        value: 9,
        categoryIndex: 1,
        seriesIndex: 0
      },
      {
        categoryValue: 15,
        value: 6,
        categoryIndex: 2,
        seriesIndex: 0
      },
      { categoryValue: 22, value: 7, categoryIndex: 3, seriesIndex: 0 }
    ]
  }
];

var domain = axis.createDomain(
  cartesianSeries,
  ValueType.fromDescriptor({ text: true }),
  false,
  []
);

// returns: [0, 1, 2, 3]
```

### <a name="getcategoryvaluetype"></a><span data-ttu-id="176d9-146">getCategoryValueType</span><span class="sxs-lookup"><span data-stu-id="176d9-146">getCategoryValueType</span></span>

<span data-ttu-id="176d9-147">ฟังก์ชันนี้จะรับ `ValueType` ของคอลัมน์ประเภท</span><span class="sxs-lookup"><span data-stu-id="176d9-147">This function gets the `ValueType` of a category column.</span></span> <span data-ttu-id="176d9-148">ค่าเริ่มต้นคือ `Text` ถ้าไม่มีชนิด</span><span class="sxs-lookup"><span data-stu-id="176d9-148">Default is `Text` if the type isn't present.</span></span>

```typescript
function getCategoryValueType(
  data: any[],
  axisType: ValueTypeDescriptor,
  isScalar: boolean,
  forcedScalarDomain: any[],
  ensureDomain?: NumberRange
): number[];
```

<span data-ttu-id="176d9-149">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-149">Example:</span></span>

```typescript
import { axis } from "powerbi-visuals-utils-chartutils";
// ...

var cartesianSeries = [
  {
    data: [
      { categoryValue: 7, value: 11, categoryIndex: 0, seriesIndex: 0 },
      {
        categoryValue: 9,
        value: 9,
        categoryIndex: 1,
        seriesIndex: 0
      },
      {
        categoryValue: 15,
        value: 6,
        categoryIndex: 2,
        seriesIndex: 0
      },
      { categoryValue: 22, value: 7, categoryIndex: 3, seriesIndex: 0 }
    ]
  }
];

axis.getCategoryValueType(
  cartesianSeries,
  ValueType.fromDescriptor({ text: true }),
  false,
  []
);

// returns: [0, 1, 2, 3]
```

### <a name="createaxis"></a><span data-ttu-id="176d9-150">createAxis</span><span class="sxs-lookup"><span data-stu-id="176d9-150">createAxis</span></span>

<span data-ttu-id="176d9-151">ฟังก์ชันนี้สร้างแกน D3 รวมทั้งสเกล</span><span class="sxs-lookup"><span data-stu-id="176d9-151">This function creates a D3 axis including scale.</span></span> <span data-ttu-id="176d9-152">สามารถอยู่ในแนวตั้งหรือแนวนอนและทั้งวันที่เวลาตัวเลขหรือข้อความ</span><span class="sxs-lookup"><span data-stu-id="176d9-152">Can be vertical or horizontal, and either datetime, numeric, or text.</span></span>

```typescript
function createAxis(options: CreateAxisOptions): IAxisProperties;
```

<span data-ttu-id="176d9-153">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-153">Example:</span></span>

```typescript
import { axis } from "powerbi-visuals-utils-chartutils";
import { valueFormatter } from "powerbi-visuals-utils-formattingutils";
// ...

var dataPercent = [0.0, 0.33, 0.49];

var formatStringProp: powerbi.DataViewObjectPropertyIdentifier = {
  objectName: "general",
  propertyName: "formatString"
};
let metaDataColumnPercent: powerbi.DataViewMetadataColumn = {
  displayName: "Column",
  type: ValueType.fromDescriptor({ numeric: true }),
  objects: {
    general: {
      formatString: "0 %"
    }
  }
};

var os = axis.createAxis({
  pixelSpan: 100,
  dataDomain: [dataPercent[0], dataPercent[2]],
  metaDataColumn: metaDataColumnPercent,
  formatString: valueFormatter.getFormatString(
    metaDataColumnPercent,
    formatStringProp
  ),
  outerPadding: 0.5,
  isScalar: true,
  isVertical: true
});
```

### <a name="applycustomizeddomain"></a><span data-ttu-id="176d9-154">applyCustomizedDomain</span><span class="sxs-lookup"><span data-stu-id="176d9-154">applyCustomizedDomain</span></span>

<span data-ttu-id="176d9-155">ฟังก์ชันนี้จะตั้งค่าโดเมนแบบกำหนดเองแต่ไม่เปลี่ยนแปลงเมื่อไม่มีการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="176d9-155">This function sets customized domain, but don't change when nothing is set.</span></span>

```typescript
function applyCustomizedDomain(customizedDomain, forcedDomain: any[]): any[];
```

<span data-ttu-id="176d9-156">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-156">Example:</span></span>

```typescript
import { axis } from "powerbi-visuals-utils-chartutils";
// ...

let customizedDomain = [undefined, 20],
  existingDomain = [0, 10];

axis.applyCustomizedDomain(customizedDomain, existingDomain);

// returns: {0:0, 1:20}
```

### <a name="combinedomain"></a><span data-ttu-id="176d9-157">combineDomain</span><span class="sxs-lookup"><span data-stu-id="176d9-157">combineDomain</span></span>

<span data-ttu-id="176d9-158">ฟังก์ชันนี้รวมโดเมนที่บังคับกับโดเมนจริงถ้าหนึ่งในค่าถูกตั้งค่าไว้</span><span class="sxs-lookup"><span data-stu-id="176d9-158">This function combines the forced domain with the actual domain if one of the values was set.</span></span>
<span data-ttu-id="176d9-159">ForcedDomain อยู่ในลำดับความสำคัญแรก</span><span class="sxs-lookup"><span data-stu-id="176d9-159">The forcedDomain is in first priority.</span></span> <span data-ttu-id="176d9-160">ขยายโดเมนถ้าจุดอ้างอิงใด ๆ มที่จำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="176d9-160">Extends the domain if any reference point requires it.</span></span>

```typescript
function combineDomain(
  forcedDomain: any[],
  domain: any[],
  ensureDomain?: NumberRange
): any[];
```

<span data-ttu-id="176d9-161">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-161">Example:</span></span>

```typescript
import { axis } from "powerbi-visuals-utils-chartutils";
// ...

let forcedYDomain = this.valueAxisProperties
  ? [this.valueAxisProperties["secStart"], this.valueAxisProperties["secEnd"]]
  : null;

let xDomain = [minX, maxX];

axis.combineDomain(forcedYDomain, xDomain, ensureXDomain);
```

### <a name="poweroften"></a><span data-ttu-id="176d9-162">powerOfTen</span><span class="sxs-lookup"><span data-stu-id="176d9-162">powerOfTen</span></span>

<span data-ttu-id="176d9-163">ฟังก์ชันนี้จะระบุว่าตัวเลขคือยกกำลัง 10 หรือไม่</span><span class="sxs-lookup"><span data-stu-id="176d9-163">This function indicates whether the number is power of 10.</span></span>

```typescript
function powerOfTen(d: any): boolean;
```

<span data-ttu-id="176d9-164">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-164">Example:</span></span>

```typescript
import { axis } from "powerbi-visuals-utils-chartutils";
// ...

axis.powerOfTen(10);

// returns: true
```

## <a name="datalabelmanager"></a><span data-ttu-id="176d9-165">DataLabelManager</span><span class="sxs-lookup"><span data-stu-id="176d9-165">DataLabelManager</span></span>

<span data-ttu-id="176d9-166">`DataLabelManager` ช่วยในการสร้างและรักษาป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="176d9-166">The `DataLabelManager` helps to create and maintain labels.</span></span> <span data-ttu-id="176d9-167">ซึ่งจัดเรียงองค์ประกอบป้ายชื่อโดยใช้จุดยึดหรือสี่เหลี่ยมผืนผ้า</span><span class="sxs-lookup"><span data-stu-id="176d9-167">It arranges label elements using the anchor point or rectangle.</span></span> <span data-ttu-id="176d9-168">สามารถตรวจพบการตัดกัน เพื่อจัดตำแหน่งหรือซ่อนองค์ประกอบได้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="176d9-168">Collisions can be automatically detected to reposition or hide elements.</span></span>

<span data-ttu-id="176d9-169">คลาส `DataLabelManager` มีวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="176d9-169">The `DataLabelManager` class provides the following methods:</span></span>

## <a name="hidecollidedlabels"></a><span data-ttu-id="176d9-170">hideCollidedLabels</span><span class="sxs-lookup"><span data-stu-id="176d9-170">hideCollidedLabels</span></span>

<span data-ttu-id="176d9-171">วิธีนี้จะจัดเรียงตำแหน่งป้ายชื่อและการมองเห็นบนพื้นที่ทำงานตามขนาดป้ายชื่อและการซ้อนทับกัน</span><span class="sxs-lookup"><span data-stu-id="176d9-171">This method arranges the labels position and visibility on the canvas according to labels sizes and overlapping.</span></span>

```typescript
function hideCollidedLabels(
  viewport: IViewport,
  data: any[],
  layout: any,
  addTransform: boolean = false
): LabelEnabledDataPoint[];
```

<span data-ttu-id="176d9-172">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-172">Example:</span></span>

```typescript
let dataLabelManager = new DataLabelManager();
let filteredData = dataLabelManager.hideCollidedLabels(
  this.viewport,
  values,
  labelLayout,
  true
);
```

## <a name="isvalid"></a><span data-ttu-id="176d9-173">IsValid</span><span class="sxs-lookup"><span data-stu-id="176d9-173">IsValid</span></span>

<span data-ttu-id="176d9-174">วิธีการแบบคงที่นี้จะตรวจสอบว่าสี่เหลี่ยมที่ให้ไว้ถูกต้องหรือไม่ (มีความกว้างและความสูงเป็นบวก)</span><span class="sxs-lookup"><span data-stu-id="176d9-174">This static method checks if provided rectangle is valid(has positive width and height).</span></span>

```typescript
function isValid(rect: IRect): boolean;
```

<span data-ttu-id="176d9-175">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-175">Example:</span></span>

```typescript
let rectangle = {
  left: 150,
  top: 130,
  width: 120,
  height: 110
};

DataLabelManager.isValid(rectangle);

// returns: true
```

## <a name="datalabelutils"></a><span data-ttu-id="176d9-176">DataLabelUtils</span><span class="sxs-lookup"><span data-stu-id="176d9-176">DataLabelUtils</span></span>

<span data-ttu-id="176d9-177">`DataLabelUtils` ให้ยูทิลิตี้จัดการป้ายชื่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="176d9-177">The `DataLabelUtils` provides utils to manipulate data labels.</span></span>

<span data-ttu-id="176d9-178">โมดูลมอบฟังก์ชัน อินเตอร์เฟส และคลาสต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="176d9-178">The module provides the following functions, interfaces, and classes:</span></span>

### <a name="getlabelprecision"></a><span data-ttu-id="176d9-179">getLabelPrecision</span><span class="sxs-lookup"><span data-stu-id="176d9-179">getLabelPrecision</span></span>

<span data-ttu-id="176d9-180">ฟังก์ชันนี้จะคำนวณความแม่นยำจากรูปแบบที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="176d9-180">This function calculates precision from given format.</span></span>

```typescript
function getLabelPrecision(precision: number, format: string): number;
```

### <a name="getlabelformattedtext"></a><span data-ttu-id="176d9-181">getLabelFormattedText</span><span class="sxs-lookup"><span data-stu-id="176d9-181">getLabelFormattedText</span></span>

<span data-ttu-id="176d9-182">ฟังก์ชันนี้ส่งกลับความแม่นยำของรูปแบบจากรูปแบบที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="176d9-182">This function returns format precision from given format.</span></span>

```typescript
function getLabelFormattedText(options: LabelFormattedTextOptions): string;
```

<span data-ttu-id="176d9-183">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-183">Example:</span></span>

```typescript
import { dataLabelUtils } from "powerbi-visuals-utils-chartutils";
// ...

let options: LabelFormattedTextOptions = {
  text: "some text",
  fontFamily: "sans",
  fontSize: "15",
  fontWeight: "normal"
};

dataLabelUtils.getLabelFormattedText(options);
```

### <a name="enumeratedatalabels"></a><span data-ttu-id="176d9-184">enumerateDataLabels</span><span class="sxs-lookup"><span data-stu-id="176d9-184">enumerateDataLabels</span></span>

<span data-ttu-id="176d9-185">ฟังก์ชันนี้จะส่งกลับ VisualObjectInstance สำหรับป้ายชื่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="176d9-185">This function returns VisualObjectInstance for data labels.</span></span>

```typescript
function enumerateDataLabels(
  options: VisualDataLabelsSettingsOptions
): VisualObjectInstance;
```

### <a name="enumeratecategorylabels"></a><span data-ttu-id="176d9-186">enumerateCategoryLabels</span><span class="sxs-lookup"><span data-stu-id="176d9-186">enumerateCategoryLabels</span></span>

<span data-ttu-id="176d9-187">ฟังก์ชันนี้เพิ่ม VisualObjectInstance สำหรับป้ายชื่อข้อมูลประเภทไปยังวัตถุการแจงนับ</span><span class="sxs-lookup"><span data-stu-id="176d9-187">This function adds VisualObjectInstance for Category data labels to enumeration object.</span></span>

```typescript
function enumerateCategoryLabels(
  enumeration: VisualObjectInstanceEnumerationObject,
  dataLabelsSettings: VisualDataLabelsSettings,
  withFill: boolean,
  isShowCategory: boolean = false,
  fontSize?: number
): void;
```

### <a name="createcolumnformattercachemanager"></a><span data-ttu-id="176d9-188">createColumnFormatterCacheManager</span><span class="sxs-lookup"><span data-stu-id="176d9-188">createColumnFormatterCacheManager</span></span>

<span data-ttu-id="176d9-189">ฟังก์ชันนี้ส่งกลับตัวจัดการแคชที่ช่วยให้สามารถเข้าถึงป้ายชื่อที่จัดรูปแบบได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="176d9-189">This function returns Cache Manager that provides quick access to formatted labels</span></span>

```typescript
function createColumnFormatterCacheManager(): IColumnFormatterCacheManager;
```

<span data-ttu-id="176d9-190">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-190">Example:</span></span>

```typescript
import { dataLabelUtils } from "powerbi-visuals-utils-chartutils";
// ...

let value: number = 200000;

labelSettings.displayUnits = 1000000;
labelSettings.precision = 1;

let formattersCache = DataLabelUtils.createColumnFormatterCacheManager();
let formatter = formattersCache.getOrCreate(null, labelSettings);
let formattedValue = formatter.format(value);

// formattedValue == "0.2M"
```

## <a name="legend-service"></a><span data-ttu-id="176d9-191">บริการคำอธิบายแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="176d9-191">Legend service</span></span>

<span data-ttu-id="176d9-192">บริการ `Legend` มีอินเทอร์เฟสตัวช่วยเหลือสำหรับการสร้างและการจัดการคำอธิบายแผนภูมิ PBI สำหรับวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="176d9-192">The `Legend` service provides helper interfaces for creating and managing PBI legends for Power BI visuals</span></span>

<span data-ttu-id="176d9-193">โมดูลมอบฟังก์ชันและอินเทอร์เฟซต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="176d9-193">The module provides the following functions and interfaces:</span></span>

### <a name="createlegend"></a><span data-ttu-id="176d9-194">createLegend</span><span class="sxs-lookup"><span data-stu-id="176d9-194">createLegend</span></span>

<span data-ttu-id="176d9-195">ฟังก์ชันผู้ช่วยเหลือนี้ลดความซับซ้อนของการสร้างคำอธิบายแผนภูมิแบบกำหนดเองของ Power BI</span><span class="sxs-lookup"><span data-stu-id="176d9-195">This helper function simplifies Power BI Custom Visual legends creation.</span></span>

```typescript
function createLegend(
  legendParentElement: HTMLElement, // top visual element, container in which legend will be created
  interactive: boolean, // indicates that legend should be interactive
  interactivityService: IInteractivityService, // reference to IInteractivityService interface which need to create legend click events
  isScrollable: boolean = false, // indicates that legend could be scrollable or not
  legendPosition: LegendPosition = LegendPosition.Top // Position of the legend inside of legendParentElement container
): ILegend;
```

<span data-ttu-id="176d9-196">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-196">Example:</span></span>

```typescript
public constructor(options: VisualConstructorOptions) {
    this.visualInitOptions = options;
    this.layers = [];

    var element = this.element = options.element;
    var viewport = this.currentViewport = options.viewport;
    var hostServices = options.host;

    //... some other init calls

    if (this.behavior) {
        this.interactivityService = createInteractivityService(hostServices);
    }
    this.legend = createLegend(
        element,
        options.interactivity && options.interactivity.isInteractiveLegend,
        this.interactivityService,
        true);
}
```

### <a name="ilegend"></a><span data-ttu-id="176d9-197">ILegend</span><span class="sxs-lookup"><span data-stu-id="176d9-197">ILegend</span></span>

<span data-ttu-id="176d9-198">อินเทอร์เฟซนี้ใช้วิธีการทั้งหมดที่จำเป็นสำหรับการสร้างคำอธิบายแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="176d9-198">This Interface implements all methods necessary for legend creation</span></span>

```typescript
export interface ILegend {
  getMargins(): IViewport;
  isVisible(): boolean;
  changeOrientation(orientation: LegendPosition): void; // processing legend orientation
  getOrientation(): LegendPosition; // get information about current legend orientation
  drawLegend(data: LegendData, viewport: IViewport); // all legend rendering code is placing here
  /**
   * Reset the legend by clearing it
   */
  reset(): void;
}
```

### <a name="drawlegend"></a><span data-ttu-id="176d9-199">drawLegend</span><span class="sxs-lookup"><span data-stu-id="176d9-199">drawLegend</span></span>

<span data-ttu-id="176d9-200">ฟังก์ชันนี้วัดความสูงของข้อความด้วยคุณสมบัติข้อความ SVG ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="176d9-200">This function measures the height of the text with the given SVG text properties.</span></span>

```typescript
function drawLegend(data: LegendData, viewport: IViewport): void;
```

<span data-ttu-id="176d9-201">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="176d9-201">Example:</span></span>

```typescript
private renderLegend(): void {
    if (!this.isInteractive) {
        let legendObjectProperties = this.data.legendObjectProperties;
        if (legendObjectProperties) {
            let legendData = this.data.legendData;
            LegendData.update(legendData, legendObjectProperties);
            let position = <string>legendObjectProperties[legendProps.position];
            if (position)
                this.legend.changeOrientation(LegendPosition[position]);

            this.legend.drawLegend(legendData, this.parentViewport);
        } else {
            this.legend.changeOrientation(LegendPosition.Top);
            this.legend.drawLegend({ dataPoints: [] }, this.parentViewport);
        }
    }
}
```

## <a name="next-steps"></a><span data-ttu-id="176d9-202">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="176d9-202">Next steps</span></span>

- [<span data-ttu-id="176d9-203">อ่านวิธีการใช้ InteractivityUtils เพื่อเพิ่มการเลือกลงในภาพ Power BI</span><span class="sxs-lookup"><span data-stu-id="176d9-203">Read how to use InteractivityUtils to add selections into Power BI Visuals</span></span>](utils-interactivity-selections.md)
