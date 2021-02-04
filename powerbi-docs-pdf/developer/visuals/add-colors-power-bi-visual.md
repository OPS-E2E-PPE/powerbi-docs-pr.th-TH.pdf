---
title: เพิ่มสีไปยังวิชวล Power BI ของคุณในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการเพิ่มสีลงในวิชวล Power BI ของคุณและวิธีการจัดการกับจุดข้อมูลสำหรับวิชวลกับสี เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: how-to
ms.date: 03/27/2020
ms.openlocfilehash: e6b6fb1dbc1397b93ac12692c8610e6f36d0b8bf
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887994"
---
# <a name="add-colors-to-your-power-bi-visuals"></a><span data-ttu-id="b1493-104">เพิ่มสีลงในวิชวล Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="b1493-104">Add colors to your Power BI visuals</span></span>

<span data-ttu-id="b1493-105">บทความนี้อธิบายวิธีการเพิ่มสีลงในวิชวลของคุณและวิธีการจัดการจุดข้อมูลสำหรับวิชวลสี</span><span class="sxs-lookup"><span data-stu-id="b1493-105">This article describes how to add colors to your visuals and how to handle data points for a color visual.</span></span>

<span data-ttu-id="b1493-106">`IVisualHost` แสดงสีเป็นซึ่งหนึ่งในบริการ</span><span class="sxs-lookup"><span data-stu-id="b1493-106">`IVisualHost` exposes color as one of its services.</span></span>
<span data-ttu-id="b1493-107">โค้ดตัวอย่างในบทความนี้จะปรับเปลี่ยน [ วิชวล SampleBarChart](https://github.com/microsoft/PowerBI-visuals-sampleBarChart)</span><span class="sxs-lookup"><span data-stu-id="b1493-107">The example code in this article modifies the [SampleBarChart visual](https://github.com/microsoft/PowerBI-visuals-sampleBarChart).</span></span>
<span data-ttu-id="b1493-108">สำหรับโค้ดแหล่งที่มา โปรดดู [barChart.ts](https://github.com/microsoft/PowerBI-visuals-sampleBarChart/blob/master/src/barChart.ts)</span><span class="sxs-lookup"><span data-stu-id="b1493-108">For source code, see [barChart.ts](https://github.com/microsoft/PowerBI-visuals-sampleBarChart/blob/master/src/barChart.ts).</span></span>

<span data-ttu-id="b1493-109">ในการเริ่มต้นสร้างวิชวลให้ดูที่ [การพัฒนาวิชวลการ์ดวงกลม Power BI](develop-circle-card.md)</span><span class="sxs-lookup"><span data-stu-id="b1493-109">To get started creating visuals, see [Developing a a Power BI circle card visual](develop-circle-card.md).</span></span>

## <a name="add-color-to-data-points"></a><span data-ttu-id="b1493-110">เพิ่มสีไปยังจุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b1493-110">Add color to data points</span></span>

<span data-ttu-id="b1493-111">สีที่แตกต่างกันแสดงแทนแต่ละจุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b1493-111">A different color represents each data point.</span></span>
<span data-ttu-id="b1493-112">เพิ่มสีไปยัง `BarChartDataPoint`อินเทอร์เฟซ  ดังในตัวอย่างต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b1493-112">Add the color to the `BarChartDataPoint` interface, as in the following example:</span></span>

```typescript
/**
 * Interface for BarChart data points.
 *
 * @interface
 * @property {number} value    - Data value for point.
 * @property {string} category - Corresponding category of data value.
 * @property {string} color    - Color corresponding to data point.
 */
interface BarChartDataPoint {
    value: number;
    category: string;
    color: string;
};
```

## <a name="use-the-color-palette-service"></a><span data-ttu-id="b1493-113">ใช้บริการจานสี</span><span class="sxs-lookup"><span data-stu-id="b1493-113">Use the color palette service</span></span>

<span data-ttu-id="b1493-114">บริการ `colorPalette` จะจัดการสีที่ใช้ในวิชวลของคุณ</span><span class="sxs-lookup"><span data-stu-id="b1493-114">The `colorPalette` service manages the colors used in your visual.</span></span>
<span data-ttu-id="b1493-115">อินสแตนซ์ของบริการที่พร้อมใช้งานบน `IVisualHost`</span><span class="sxs-lookup"><span data-stu-id="b1493-115">An instance of the service is available on `IVisualHost`.</span></span>

<span data-ttu-id="b1493-116">กำหนดได้ในวิธีการ `update`</span><span class="sxs-lookup"><span data-stu-id="b1493-116">Define it in the `update` method.</span></span>

```typescript
constructor(options: VisualConstructorOptions) {
        this.host = options.host; // host: IVisualHost
        ...
    }

public update(options: VisualUpdateOptions) {

    let colorPalette: IColorPalette = host.colorPalette;
    ...
}
```

## <a name="assigning-color-to-data-points"></a><span data-ttu-id="b1493-117">กำหนดสีให้กับจุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b1493-117">Assigning color to data points</span></span>

<span data-ttu-id="b1493-118">ถัดไป ให้ระบุ `dataPoints`</span><span class="sxs-lookup"><span data-stu-id="b1493-118">Next, specify `dataPoints`.</span></span>
<span data-ttu-id="b1493-119">ในตัวอย่างนี้ แต่ละ `dataPoints` ได้รวมค่า หมวดหมู่และสีไว้</span><span class="sxs-lookup"><span data-stu-id="b1493-119">In this example, each of the `dataPoints` includes value, category, and color.</span></span>
<span data-ttu-id="b1493-120">นอกจากนี้ `dataPoints` ยังมีคุณสมบัติอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="b1493-120">`dataPoints` can also include other properties.</span></span>

<span data-ttu-id="b1493-121">ใน `SampleBarChart` วิธีการ `visualTransform` จะย่อส่วนการคำนวณ `dataPoints`</span><span class="sxs-lookup"><span data-stu-id="b1493-121">In `SampleBarChart`, the `visualTransform` method encapsulates the `dataPoints` calculation.</span></span>
<span data-ttu-id="b1493-122">วิธีการดังกล่าวเป็นส่วนหนึ่งของแผนภูมิแท่ง viewmodel</span><span class="sxs-lookup"><span data-stu-id="b1493-122">That method is a part of the Bar Chart viewmodel.</span></span>
<span data-ttu-id="b1493-123">เนื่องจากวิธีการนั้นซ้ำผ่าน `dataPoints`การคำนวณใน`visualTransform` จึงเป็นสถานที่ที่เหมาะสมที่จะกำหนดสี ดังเช่นในโค้ดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b1493-123">Because the method iterates through the `dataPoints` calculation in `visualTransform`, it's the ideal place to assign colors, as in the following code:</span></span>

```typescript

public update(options: VisualUpdateOptions) {
    ....
    let viewModel: BarChartViewModel = visualTransform(options, this.host);
    ....
}

function visualTransform(options: VisualUpdateOptions, host: IVisualHost): BarChartViewModel {
    let colorPalette: IColorPalette = host.colorPalette; // host: IVisualHost
    for (let i = 0, len = Math.max(category.values.length, dataValue.values.length); i < len; i++) {
        barChartDataPoints.push({
            category: category.values[i],
            value: dataValue.values[i],
            color: colorPalette.getColor(category.values[i]).value,
        });
    }
}
```

<span data-ttu-id="b1493-124">จากนั้นใช้ข้อมูลจาก `dataPoints` บน [d3](https://d3js.org/)-การเลือก `barSelection` ภายในวิธีการ `update`:</span><span class="sxs-lookup"><span data-stu-id="b1493-124">Then apply data from `dataPoints` on the [d3](https://d3js.org/)-selection `barSelection` inside the `update` method:</span></span>

```typescript
// This code is actual for d3 v5
// in d3 v5 for this case we should use merge() after enter() and apply changes on barSelectionMerged
this.barSelection = this.barContainer
    .selectAll('.bar')
    .data(this.barDataPoints);

const barSelectionMerged = this.barSelection
    .enter()
    .append('rect')
    .merge(<any>this.barSelection);

barSelectionMerged.classed('bar', true);

barSelectionMerged
.attr("width", xScale.bandwidth())
.attr("height", d => height - yScale(<number>d.value))
.attr("y", d => yScale(<number>d.value))
.attr("x", d => xScale(d.category))
.style("fill", (dataPoint: BarChartDataPoint) => dataPoint.color)
.style("stroke", (dataPoint: BarChartDataPoint) => dataPoint.strokeColor)
.style("stroke-width", (dataPoint: BarChartDataPoint) => `${dataPoint.strokeWidth}px`);

this.barSelection
    .exit()
    .remove();
```

## <a name="next-steps"></a><span data-ttu-id="b1493-125">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="b1493-125">Next steps</span></span>

<span data-ttu-id="b1493-126">ในการเรียนรู้เพิ่มเติมเกี่ยวกับ Power BI ดูที่ [ความสามารถและคุณสมบัติของวิชวล Power BI](capabilities.md)</span><span class="sxs-lookup"><span data-stu-id="b1493-126">To learn more about Power BI visuals, see [Capabilities and properties of Power BI visuals](capabilities.md).</span></span>

<span data-ttu-id="b1493-127">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับการพัฒนาวิชวล Power BI โปรดดู [วิธีการแก้จุดบกพร่องของวิชวล Power BI](visuals-how-to-debug.md) และ [การแก้ไขปัญหา Power BI](power-bi-custom-visuals-troubleshoot.md)</span><span class="sxs-lookup"><span data-stu-id="b1493-127">To learn more about developing Power BI visuals, see [How to debug Power BI visuals](visuals-how-to-debug.md) and [Troubleshoot Power BI visuals](power-bi-custom-visuals-troubleshoot.md).</span></span>
