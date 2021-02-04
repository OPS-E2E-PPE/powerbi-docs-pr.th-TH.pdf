---
title: การไฮไลต์ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: การเลือกจุดข้อมูลที่ไฮไลต์ในวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: rkarlin
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: how-to
ms.date: 10/31/2019
ms.openlocfilehash: f45b363ce4616a725d19d0b06f4f9fb96110ac8a
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97886545"
---
# <a name="highlight-data-points-in-power-bi-visuals"></a><span data-ttu-id="2a265-104">ไฮไลต์จุดข้อมูลใน Power BI Visuals</span><span class="sxs-lookup"><span data-stu-id="2a265-104">Highlight data points in Power BI Visuals</span></span>

<span data-ttu-id="2a265-105">โดยค่าเริ่มต้นเมื่อใดก็ตามที่มีการเลือกองค์ประกอบ อาร์เรย์ `values` ในวัตถุ `dataView` จะถูกกรองให้เป็นเพียงค่าที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2a265-105">By default whenever an element is selected the `values` array in the `dataView` object will be filtered to just the selected values.</span></span> <span data-ttu-id="2a265-106">ซึ่งจะทำให้วิชวลอื่น ๆ ทั้งหมดในหน้าแสดงเป็นเพียงข้อมูลที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2a265-106">It will cause all other visuals on the page to display just the selected data.</span></span>

![ไฮไลต์ `dataview` ในลักษณะตามค่าเริ่มต้น](media/highlight/highlight-dataview.png)

<span data-ttu-id="2a265-108">หากคุณตั้งค่าคุณสมบัติ `supportsHighlight` ใน `capabilities.json` เป็น `true` คุณจะได้รับอาร์เรย์ `values` แบบไม่มีการกรองเต็มรูปแบบพร้อมกับอาร์เรย์ `highlights`</span><span class="sxs-lookup"><span data-stu-id="2a265-108">If you set the `supportsHighlight` property in your `capabilities.json` to `true`, you'll receive the full unfiltered `values` array along with a `highlights` array.</span></span> <span data-ttu-id="2a265-109">อาร์เรย์ `highlights` จะมีความยาวเท่ากับอาร์เรย์ค่าและค่าที่ไม่ได้เลือกจะถูกตั้งค่าเป็น `null`</span><span class="sxs-lookup"><span data-stu-id="2a265-109">The `highlights` array will be the same length as the values array and any non-selected values will be set to `null`.</span></span> <span data-ttu-id="2a265-110">เมื่อเปิดใช้งานคุณสมบัตินี้แล้ว จึงเป็นความรับผิดชอบของวิชวลในการไฮไลต์ข้อมูลที่เหมาะสมโดยการเปรียบเทียบอาร์เรย์ `values` กับอาร์เรย์ `highlights`</span><span class="sxs-lookup"><span data-stu-id="2a265-110">With this property enabled it's the visual's responsibility to highlight the appropriate data by comparing the `values` array to the `highlights` array.</span></span>

![' dataview ' สนับสนุนการไฮไลต์](media/highlight/highlight-dataview-supports.png)

<span data-ttu-id="2a265-112">ในตัวอย่าง คุณจะสังเกตเห็นว่ามี 1 แถบที่ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="2a265-112">In the example, you'll notice that 1 bar is selected.</span></span> <span data-ttu-id="2a265-113">และเป็นเฉพาะค่าในอาร์เรย์ไฮไลต์</span><span class="sxs-lookup"><span data-stu-id="2a265-113">And it's the only value in the highlights array.</span></span> <span data-ttu-id="2a265-114">นอกจากนี้ สิ่งสำคัญคือต้องทราบว่าอาจมีตัวเลือกหลายรายการและการไฮไลต์บางส่วนด้วย</span><span class="sxs-lookup"><span data-stu-id="2a265-114">It's also important to note that there could be multiple selections and partial highlights.</span></span> <span data-ttu-id="2a265-115">ค่าที่ไฮไลต์ไว้จะแสดงในมุมมองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2a265-115">The highlighted values will be presented in the data view.</span></span>

> [!NOTE]
> <span data-ttu-id="2a265-116">การแมปมุมมองข้อมูลแบบตารางไม่สนับสนุนคุณลักษณะการไฮไลท์</span><span class="sxs-lookup"><span data-stu-id="2a265-116">Table data view mapping doesn't support the highlights feature.</span></span>

## <a name="highlight-data-points-with-categorical-data-view-mapping"></a><span data-ttu-id="2a265-117">ไฮไลต์จุดข้อมูลด้วยการแมปมุมมองข้อมูลตามประเภท</span><span class="sxs-lookup"><span data-stu-id="2a265-117">Highlight data points with categorical data view mapping</span></span>

<span data-ttu-id="2a265-118">วิชวลที่มีการแมปมุมมองข้อมูลตามประเภทมี`capabilities.json`พร้อมด้วย`"supportsHighlight": true`พารามิเตอร์ </span><span class="sxs-lookup"><span data-stu-id="2a265-118">The visuals with categorical data view mapping have `capabilities.json` with `"supportsHighlight": true` parameter.</span></span> <span data-ttu-id="2a265-119">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="2a265-119">For example:</span></span>

```json
{
    "dataRoles": [
        {
            "displayName": "Category",
            "name": "category",
            "kind": "Grouping"
        },
        {
            "displayName": "Value",
            "name": "value",
            "kind": "Measure"
        }
    ],
    "dataViewMappings": [
        {
            "categorical": {
                "categories": {
                    "for": {
                        "in": "category"
                    }
                },
                "values": {
                    "for": {
                        "in": "value"
                    }
                }
            }
        }
    ],
    "supportsHighlight": true
}
```

<span data-ttu-id="2a265-120">รหัสแหล่งข้อมูลของวิชวลเริ่มต้นหลังจากลบรหัสที่ไม่จำเป็นจะมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="2a265-120">The default visual source code after removing unnecessary code will look like this:</span></span>

```typescript
"use strict";

// ... default imports list

import DataViewCategorical = powerbi.DataViewCategorical;
import DataViewCategoryColumn = powerbi.DataViewCategoryColumn;
import PrimitiveValue = powerbi.PrimitiveValue;
import DataViewValueColumn = powerbi.DataViewValueColumn;

import { VisualSettings } from "./settings";

export class Visual implements IVisual {
    private target: HTMLElement;
    private settings: VisualSettings;

    constructor(options: VisualConstructorOptions) {
        console.log('Visual constructor', options);
        this.target = options.element;
        this.host = options.host;

    }

    public update(options: VisualUpdateOptions) {
        this.settings = Visual.parseSettings(options && options.dataViews && options.dataViews[0]);
        console.log('Visual update', options);

    }

    private static parseSettings(dataView: DataView): VisualSettings {
        return <VisualSettings>VisualSettings.parse(dataView);
    }

    /**
     * This function gets called for each of the objects defined in the capabilities files and allows you to select which of the
     * objects and properties you want to expose to the users in the property pane.
     *
     */
    public enumerateObjectInstances(options: EnumerateVisualObjectInstancesOptions): VisualObjectInstance[] | VisualObjectInstanceEnumerationObject {
        return VisualSettings.enumerateObjectInstances(this.settings || VisualSettings.getDefault(), options);
    }
}
```

<span data-ttu-id="2a265-121">นำเข้าอินเทอร์เฟสที่จำเป็นเพื่อประมวลผลข้อมูลจาก Power BI:</span><span class="sxs-lookup"><span data-stu-id="2a265-121">Import required interfaces to process data from Power BI:</span></span>

```typescript
import DataViewCategorical = powerbi.DataViewCategorical;
import DataViewCategoryColumn = powerbi.DataViewCategoryColumn;
import PrimitiveValue = powerbi.PrimitiveValue;
import DataViewValueColumn = powerbi.DataViewValueColumn;
```

<span data-ttu-id="2a265-122">สร้างองค์ประกอบ`div`ระดับสูงสำหรับค่าหมวดหมู่:</span><span class="sxs-lookup"><span data-stu-id="2a265-122">Create root `div` element for category values:</span></span>

```typescript
export class Visual implements IVisual {
    private target: HTMLElement;
    private settings: VisualSettings;

    private div: HTMLDivElement; // new property

    constructor(options: VisualConstructorOptions) {
        console.log('Visual constructor', options);
        this.target = options.element;
        this.host = options.host;

        // create div element
        this.div = document.createElement("div");
        this.div.classList.add("vertical");
        this.target.appendChild(this.div);

    }
    // ...
}
```

<span data-ttu-id="2a265-123">ล้างเนื้อหาขององค์ประกอบ div ก่อนที่จะแสดงข้อมูลใหม่:</span><span class="sxs-lookup"><span data-stu-id="2a265-123">Clear content of div elements before rendering new data:</span></span>

```typescript
// ...
public update(options: VisualUpdateOptions) {
    this.settings = Visual.parseSettings(options && options.dataViews && options.dataViews[0]);
    console.log('Visual update', options);

    while (this.div.firstChild) {
        this.div.removeChild(this.div.firstChild);
    }
    // ...
}
```

<span data-ttu-id="2a265-124">รับค่าหมวดหมู่และหน่วยวัดจากวัตถุ `dataView`:</span><span class="sxs-lookup"><span data-stu-id="2a265-124">Get categories and measure values from `dataView` object:</span></span>

```typescript
public update(options: VisualUpdateOptions) {
    this.settings = Visual.parseSettings(options && options.dataViews && options.dataViews[0]);
    console.log('Visual update', options);

    while (this.div.firstChild) {
        this.div.removeChild(this.div.firstChild);
    }

    const dataView: DataView = options.dataViews[0];
    const categoricalDataView: DataViewCategorical = dataView.categorical;
    const categories: DataViewCategoryColumn = categoricalDataView.categories[0];
    const categoryValues = categories.values;

    const measures: DataViewValueColumn = categoricalDataView.values[0];
    const measureValues = measures.values;
    const measureHighlights = measures.highlights;
    // ...
}
```

<span data-ttu-id="2a265-125">โดยที่ `categoryValues` คืออาร์เรย์ของค่าหมวดหมู่ `measureValues` เป็นอาร์เรย์ของหน่วยวัดและ `measureHighlights` คือส่วนที่ไฮไลต์ของค่า</span><span class="sxs-lookup"><span data-stu-id="2a265-125">Where `categoryValues` is an array of category values, `measureValues` is an array of measures, and `measureHighlights` is highlighted parts of values.</span></span>

> [!NOTE]
> <span data-ttu-id="2a265-126">ค่าของคุณสมบัติ `measureHighlights` อาจน้อยกว่าค่าของคุณสมบัติ `categoryValues`</span><span class="sxs-lookup"><span data-stu-id="2a265-126">Values of `measureHighlights` property can be less that values of `categoryValues` property.</span></span>
> <span data-ttu-id="2a265-127">หมายความว่ามีการไฮไลต์ค่าบางส่วน</span><span class="sxs-lookup"><span data-stu-id="2a265-127">In means that value was higlighted partially.</span></span>

<span data-ttu-id="2a265-128">ระบุอาร์เรย์ `categoryValues` และรับค่าและไฮไลต์ที่สอดคล้องกัน:</span><span class="sxs-lookup"><span data-stu-id="2a265-128">Enumerate `categoryValues` array and get corresponding values and highlights:</span></span>

```typescript
// ...
const measureHighlights = measures.highlights;

categoryValues.forEach((category: PrimitiveValue, index: number) => {
    const measureValue = measureValues[index];
    const measureHighlight = measureHighlights && measureHighlights[index] ? measureHighlights[index] : null;
    console.log(category, measureValue, measureHighlight);

});
```

<span data-ttu-id="2a265-129">สร้างองค์ประกอบ `div` และ `p` เพื่อแสดงและดูภาพค่ามุมมองข้อมูลใน DOM ของวิชวล:</span><span class="sxs-lookup"><span data-stu-id="2a265-129">Create `div` and `p` elements to display and visualize data view values in visual DOM:</span></span>

```typescript
categoryValues.forEach((category: PrimitiveValue, index: number) => {
    const measureValue = measureValues[index];
    const measureHighlight = measureHighlights && measureHighlights[index] ? measureHighlights[index] : null;
    console.log(category, measureValue, measureHighlight);

    // div element. it contains elements to display values and visualize value as progress bar
    let div = document.createElement("div");
    div.classList.add("horizontal");
    this.div.appendChild(div);

    // div element to vizualize value of measure
    let barValue = document.createElement("div");
    barValue.style.width = +measureValue * 10 + "px";
    barValue.style.display = "flex";
    barValue.classList.add("value");

    // element to display category value
    let bp = document.createElement("p");
    bp.innerText = category.toString();

    // div element to vizualize highlight of measure
    let barHighlight = document.createElement("div");
    barHighlight.classList.add("highlight")
    barHighlight.style.backgroundColor = "blue";
    barHighlight.style.width = +measureHighlight * 10 + "px";

    // element to display highlighted value of measure
    let p = document.createElement("p");
    p.innerText = `${measureHighlight}/${measureValue}`;
    barHighlight.appendChild(bp);

    div.appendChild(barValue);

    barValue.appendChild(barHighlight);
    div.appendChild(p);
});
```

<span data-ttu-id="2a265-130">ใช้ลักษณะที่จำเป็นสำหรับองค์ประกอบเพื่อใช้ `flex box` และกำหนดสีสำหรับองค์ประกอบ div:</span><span class="sxs-lookup"><span data-stu-id="2a265-130">Apply required styles for elements to use `flex box` and define colors for div elements:</span></span>

```css
div.vertical {
    display: flex;
    flex-direction: column;
}

div.horizontal {
    display: flex;
    flex-direction: row;
}

div.highlight {
    background-color: blue
}

div.value {
    background-color: red;
    display: flex;
}
```

<span data-ttu-id="2a265-131">ในผลลัพธ์ คุณควรมีมุมมองของวิชวลดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2a265-131">In the result, you should have the following view of the visual.</span></span>

![วิชวลที่มีการแมปมุมมองข้อมูลตามประเภทและการไฮไลต์](media/highlight/dev-categorical-visual-highlight-demo.gif)

## <a name="highlight-data-points-with-matrix-data-view-mapping"></a><span data-ttu-id="2a265-133">ไฮไลต์จุดข้อมูลด้วยการแมปมุมมองข้อมูลแบบเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="2a265-133">Highlight data points with matrix data view mapping</span></span>

<span data-ttu-id="2a265-134">วิชวลที่มีการแมปมุมมองข้อมูลแบบเมทริกซ์มี`capabilities.json`พร้อมด้วย`"supportsHighlight": true`พารามิเตอร์ </span><span class="sxs-lookup"><span data-stu-id="2a265-134">The visuals with matrix data view mapping have `capabilities.json` with `"supportsHighlight": true` parameter.</span></span> <span data-ttu-id="2a265-135">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="2a265-135">For example:</span></span>

```json
{
    "dataRoles": [
        {
            "displayName": "Columns",
            "name": "columns",
            "kind": "Grouping"
        },
        {
            "displayName": "Rows",
            "name": "rows",
            "kind": "Grouping"
        },
        {
            "displayName": "Value",
            "name": "value",
            "kind": "Measure"
        }
    ],
    "dataViewMappings": [
        {
            "matrix": {
                "columns": {
                    "for": {
                        "in": "columns"
                    }
                },
                "rows": {
                    "for": {
                        "in": "rows"
                    }
                },
                "values": {
                    "for": {
                        "in": "value"
                    }
                }
            }
        }
    ],
    "supportsHighlight": true
}
```

<span data-ttu-id="2a265-136">ข้อมูลตัวอย่างในการสร้างลำดับชั้นสำหรับการแมปมุมมองข้อมูลแบบเมทริกซ์:</span><span class="sxs-lookup"><span data-stu-id="2a265-136">The sample data to create hierarchy for matrix data view mapping:</span></span>

|   <span data-ttu-id="2a265-137">Row1</span><span class="sxs-lookup"><span data-stu-id="2a265-137">Row1</span></span>   |   <span data-ttu-id="2a265-138">Row2</span><span class="sxs-lookup"><span data-stu-id="2a265-138">Row2</span></span>   |   <span data-ttu-id="2a265-139">Row3</span><span class="sxs-lookup"><span data-stu-id="2a265-139">Row3</span></span>   |   <span data-ttu-id="2a265-140">คอลัมน์ 1</span><span class="sxs-lookup"><span data-stu-id="2a265-140">Column1</span></span>   |   <span data-ttu-id="2a265-141">คอลัมน์2</span><span class="sxs-lookup"><span data-stu-id="2a265-141">Column2</span></span>   |   <span data-ttu-id="2a265-142">คอลัมน์3</span><span class="sxs-lookup"><span data-stu-id="2a265-142">Column3</span></span>   |   <span data-ttu-id="2a265-143">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="2a265-143">Values</span></span>   |
|-----|-----|------|-------|-------|-------|-------|
|   <span data-ttu-id="2a265-144">R1</span><span class="sxs-lookup"><span data-stu-id="2a265-144">R1</span></span>   |   <span data-ttu-id="2a265-145">R11</span><span class="sxs-lookup"><span data-stu-id="2a265-145">R11</span></span>   |   <span data-ttu-id="2a265-146">R111</span><span class="sxs-lookup"><span data-stu-id="2a265-146">R111</span></span>   |   <span data-ttu-id="2a265-147">C1</span><span class="sxs-lookup"><span data-stu-id="2a265-147">C1</span></span>   |   <span data-ttu-id="2a265-148">C11</span><span class="sxs-lookup"><span data-stu-id="2a265-148">C11</span></span>   |   <span data-ttu-id="2a265-149">C111</span><span class="sxs-lookup"><span data-stu-id="2a265-149">C111</span></span>   |   <span data-ttu-id="2a265-150">1</span><span class="sxs-lookup"><span data-stu-id="2a265-150">1</span></span>   |
|   <span data-ttu-id="2a265-151">R1</span><span class="sxs-lookup"><span data-stu-id="2a265-151">R1</span></span>   |   <span data-ttu-id="2a265-152">R11</span><span class="sxs-lookup"><span data-stu-id="2a265-152">R11</span></span>   |   <span data-ttu-id="2a265-153">R112</span><span class="sxs-lookup"><span data-stu-id="2a265-153">R112</span></span>   |   <span data-ttu-id="2a265-154">C1</span><span class="sxs-lookup"><span data-stu-id="2a265-154">C1</span></span>   |   <span data-ttu-id="2a265-155">C11</span><span class="sxs-lookup"><span data-stu-id="2a265-155">C11</span></span>   |   <span data-ttu-id="2a265-156">C112</span><span class="sxs-lookup"><span data-stu-id="2a265-156">C112</span></span>   |   <span data-ttu-id="2a265-157">2</span><span class="sxs-lookup"><span data-stu-id="2a265-157">2</span></span>   |
|   <span data-ttu-id="2a265-158">R1</span><span class="sxs-lookup"><span data-stu-id="2a265-158">R1</span></span>   |   <span data-ttu-id="2a265-159">R11</span><span class="sxs-lookup"><span data-stu-id="2a265-159">R11</span></span>   |   <span data-ttu-id="2a265-160">R113</span><span class="sxs-lookup"><span data-stu-id="2a265-160">R113</span></span>   |   <span data-ttu-id="2a265-161">C1</span><span class="sxs-lookup"><span data-stu-id="2a265-161">C1</span></span>   |   <span data-ttu-id="2a265-162">C11</span><span class="sxs-lookup"><span data-stu-id="2a265-162">C11</span></span>   |   <span data-ttu-id="2a265-163">C113</span><span class="sxs-lookup"><span data-stu-id="2a265-163">C113</span></span>   |   <span data-ttu-id="2a265-164">3</span><span class="sxs-lookup"><span data-stu-id="2a265-164">3</span></span>   |
|   <span data-ttu-id="2a265-165">R1</span><span class="sxs-lookup"><span data-stu-id="2a265-165">R1</span></span>   |   <span data-ttu-id="2a265-166">R12</span><span class="sxs-lookup"><span data-stu-id="2a265-166">R12</span></span>   |   <span data-ttu-id="2a265-167">R121</span><span class="sxs-lookup"><span data-stu-id="2a265-167">R121</span></span>   |   <span data-ttu-id="2a265-168">C1</span><span class="sxs-lookup"><span data-stu-id="2a265-168">C1</span></span>   |   <span data-ttu-id="2a265-169">C12</span><span class="sxs-lookup"><span data-stu-id="2a265-169">C12</span></span>   |   <span data-ttu-id="2a265-170">C121</span><span class="sxs-lookup"><span data-stu-id="2a265-170">C121</span></span>   |   <span data-ttu-id="2a265-171">4</span><span class="sxs-lookup"><span data-stu-id="2a265-171">4</span></span>   |
|   <span data-ttu-id="2a265-172">R1</span><span class="sxs-lookup"><span data-stu-id="2a265-172">R1</span></span>   |   <span data-ttu-id="2a265-173">R12</span><span class="sxs-lookup"><span data-stu-id="2a265-173">R12</span></span>   |   <span data-ttu-id="2a265-174">R122</span><span class="sxs-lookup"><span data-stu-id="2a265-174">R122</span></span>   |   <span data-ttu-id="2a265-175">C1</span><span class="sxs-lookup"><span data-stu-id="2a265-175">C1</span></span>   |   <span data-ttu-id="2a265-176">C12</span><span class="sxs-lookup"><span data-stu-id="2a265-176">C12</span></span>   |   <span data-ttu-id="2a265-177">C122</span><span class="sxs-lookup"><span data-stu-id="2a265-177">C122</span></span>   |   <span data-ttu-id="2a265-178">5</span><span class="sxs-lookup"><span data-stu-id="2a265-178">5</span></span>   |
|   <span data-ttu-id="2a265-179">R1</span><span class="sxs-lookup"><span data-stu-id="2a265-179">R1</span></span>   |   <span data-ttu-id="2a265-180">R12</span><span class="sxs-lookup"><span data-stu-id="2a265-180">R12</span></span>   |   <span data-ttu-id="2a265-181">R123</span><span class="sxs-lookup"><span data-stu-id="2a265-181">R123</span></span>   |   <span data-ttu-id="2a265-182">C1</span><span class="sxs-lookup"><span data-stu-id="2a265-182">C1</span></span>   |   <span data-ttu-id="2a265-183">C12</span><span class="sxs-lookup"><span data-stu-id="2a265-183">C12</span></span>   |   <span data-ttu-id="2a265-184">C123</span><span class="sxs-lookup"><span data-stu-id="2a265-184">C123</span></span>   |   <span data-ttu-id="2a265-185">6</span><span class="sxs-lookup"><span data-stu-id="2a265-185">6</span></span>   |
|   <span data-ttu-id="2a265-186">R1</span><span class="sxs-lookup"><span data-stu-id="2a265-186">R1</span></span>   |   <span data-ttu-id="2a265-187">R13</span><span class="sxs-lookup"><span data-stu-id="2a265-187">R13</span></span>   |   <span data-ttu-id="2a265-188">R131</span><span class="sxs-lookup"><span data-stu-id="2a265-188">R131</span></span>   |   <span data-ttu-id="2a265-189">C1</span><span class="sxs-lookup"><span data-stu-id="2a265-189">C1</span></span>   |   <span data-ttu-id="2a265-190">C13</span><span class="sxs-lookup"><span data-stu-id="2a265-190">C13</span></span>   |   <span data-ttu-id="2a265-191">C131</span><span class="sxs-lookup"><span data-stu-id="2a265-191">C131</span></span>   |   <span data-ttu-id="2a265-192">7</span><span class="sxs-lookup"><span data-stu-id="2a265-192">7</span></span>   |
|   <span data-ttu-id="2a265-193">R1</span><span class="sxs-lookup"><span data-stu-id="2a265-193">R1</span></span>   |   <span data-ttu-id="2a265-194">R13</span><span class="sxs-lookup"><span data-stu-id="2a265-194">R13</span></span>   |   <span data-ttu-id="2a265-195">R132</span><span class="sxs-lookup"><span data-stu-id="2a265-195">R132</span></span>   |   <span data-ttu-id="2a265-196">C1</span><span class="sxs-lookup"><span data-stu-id="2a265-196">C1</span></span>   |   <span data-ttu-id="2a265-197">C13</span><span class="sxs-lookup"><span data-stu-id="2a265-197">C13</span></span>   |   <span data-ttu-id="2a265-198">C132</span><span class="sxs-lookup"><span data-stu-id="2a265-198">C132</span></span>   |   <span data-ttu-id="2a265-199">8</span><span class="sxs-lookup"><span data-stu-id="2a265-199">8</span></span>   |
|   <span data-ttu-id="2a265-200">R1</span><span class="sxs-lookup"><span data-stu-id="2a265-200">R1</span></span>   |   <span data-ttu-id="2a265-201">R13</span><span class="sxs-lookup"><span data-stu-id="2a265-201">R13</span></span>   |   <span data-ttu-id="2a265-202">R133</span><span class="sxs-lookup"><span data-stu-id="2a265-202">R133</span></span>   |   <span data-ttu-id="2a265-203">C1</span><span class="sxs-lookup"><span data-stu-id="2a265-203">C1</span></span>   |   <span data-ttu-id="2a265-204">C13</span><span class="sxs-lookup"><span data-stu-id="2a265-204">C13</span></span>   |   <span data-ttu-id="2a265-205">C133</span><span class="sxs-lookup"><span data-stu-id="2a265-205">C133</span></span>   |   <span data-ttu-id="2a265-206">9</span><span class="sxs-lookup"><span data-stu-id="2a265-206">9</span></span>   |
|   <span data-ttu-id="2a265-207">R2</span><span class="sxs-lookup"><span data-stu-id="2a265-207">R2</span></span>   |   <span data-ttu-id="2a265-208">R21</span><span class="sxs-lookup"><span data-stu-id="2a265-208">R21</span></span>   |   <span data-ttu-id="2a265-209">R211</span><span class="sxs-lookup"><span data-stu-id="2a265-209">R211</span></span>   |   <span data-ttu-id="2a265-210">C2</span><span class="sxs-lookup"><span data-stu-id="2a265-210">C2</span></span>   |   <span data-ttu-id="2a265-211">C21</span><span class="sxs-lookup"><span data-stu-id="2a265-211">C21</span></span>   |   <span data-ttu-id="2a265-212">C211</span><span class="sxs-lookup"><span data-stu-id="2a265-212">C211</span></span>   |   <span data-ttu-id="2a265-213">10</span><span class="sxs-lookup"><span data-stu-id="2a265-213">10</span></span>   |
|   <span data-ttu-id="2a265-214">R2</span><span class="sxs-lookup"><span data-stu-id="2a265-214">R2</span></span>   |   <span data-ttu-id="2a265-215">R21</span><span class="sxs-lookup"><span data-stu-id="2a265-215">R21</span></span>   |   <span data-ttu-id="2a265-216">R212</span><span class="sxs-lookup"><span data-stu-id="2a265-216">R212</span></span>   |   <span data-ttu-id="2a265-217">C2</span><span class="sxs-lookup"><span data-stu-id="2a265-217">C2</span></span>   |   <span data-ttu-id="2a265-218">C21</span><span class="sxs-lookup"><span data-stu-id="2a265-218">C21</span></span>   |   <span data-ttu-id="2a265-219">C212</span><span class="sxs-lookup"><span data-stu-id="2a265-219">C212</span></span>   |   <span data-ttu-id="2a265-220">11</span><span class="sxs-lookup"><span data-stu-id="2a265-220">11</span></span>   |
|   <span data-ttu-id="2a265-221">R2</span><span class="sxs-lookup"><span data-stu-id="2a265-221">R2</span></span>   |   <span data-ttu-id="2a265-222">R21</span><span class="sxs-lookup"><span data-stu-id="2a265-222">R21</span></span>   |   <span data-ttu-id="2a265-223">R213</span><span class="sxs-lookup"><span data-stu-id="2a265-223">R213</span></span>   |   <span data-ttu-id="2a265-224">C2</span><span class="sxs-lookup"><span data-stu-id="2a265-224">C2</span></span>   |   <span data-ttu-id="2a265-225">C21</span><span class="sxs-lookup"><span data-stu-id="2a265-225">C21</span></span>   |   <span data-ttu-id="2a265-226">C213</span><span class="sxs-lookup"><span data-stu-id="2a265-226">C213</span></span>   |   <span data-ttu-id="2a265-227">12</span><span class="sxs-lookup"><span data-stu-id="2a265-227">12</span></span>   |
|   <span data-ttu-id="2a265-228">R2</span><span class="sxs-lookup"><span data-stu-id="2a265-228">R2</span></span>   |   <span data-ttu-id="2a265-229">R22</span><span class="sxs-lookup"><span data-stu-id="2a265-229">R22</span></span>   |   <span data-ttu-id="2a265-230">R221</span><span class="sxs-lookup"><span data-stu-id="2a265-230">R221</span></span>   |   <span data-ttu-id="2a265-231">C2</span><span class="sxs-lookup"><span data-stu-id="2a265-231">C2</span></span>   |   <span data-ttu-id="2a265-232">C22</span><span class="sxs-lookup"><span data-stu-id="2a265-232">C22</span></span>   |   <span data-ttu-id="2a265-233">C221</span><span class="sxs-lookup"><span data-stu-id="2a265-233">C221</span></span>   |   <span data-ttu-id="2a265-234">13</span><span class="sxs-lookup"><span data-stu-id="2a265-234">13</span></span>   |
|   <span data-ttu-id="2a265-235">R2</span><span class="sxs-lookup"><span data-stu-id="2a265-235">R2</span></span>   |   <span data-ttu-id="2a265-236">R22</span><span class="sxs-lookup"><span data-stu-id="2a265-236">R22</span></span>   |   <span data-ttu-id="2a265-237">R222</span><span class="sxs-lookup"><span data-stu-id="2a265-237">R222</span></span>   |   <span data-ttu-id="2a265-238">C2</span><span class="sxs-lookup"><span data-stu-id="2a265-238">C2</span></span>   |   <span data-ttu-id="2a265-239">C22</span><span class="sxs-lookup"><span data-stu-id="2a265-239">C22</span></span>   |   <span data-ttu-id="2a265-240">C222</span><span class="sxs-lookup"><span data-stu-id="2a265-240">C222</span></span>   |   <span data-ttu-id="2a265-241">14</span><span class="sxs-lookup"><span data-stu-id="2a265-241">14</span></span>   |
|   <span data-ttu-id="2a265-242">R2</span><span class="sxs-lookup"><span data-stu-id="2a265-242">R2</span></span>   |   <span data-ttu-id="2a265-243">R22</span><span class="sxs-lookup"><span data-stu-id="2a265-243">R22</span></span>   |   <span data-ttu-id="2a265-244">R223</span><span class="sxs-lookup"><span data-stu-id="2a265-244">R223</span></span>   |   <span data-ttu-id="2a265-245">C2</span><span class="sxs-lookup"><span data-stu-id="2a265-245">C2</span></span>   |   <span data-ttu-id="2a265-246">C22</span><span class="sxs-lookup"><span data-stu-id="2a265-246">C22</span></span>   |   <span data-ttu-id="2a265-247">C223</span><span class="sxs-lookup"><span data-stu-id="2a265-247">C223</span></span>   |   <span data-ttu-id="2a265-248">16</span><span class="sxs-lookup"><span data-stu-id="2a265-248">16</span></span>   |
|   <span data-ttu-id="2a265-249">R2</span><span class="sxs-lookup"><span data-stu-id="2a265-249">R2</span></span>   |   <span data-ttu-id="2a265-250">R23</span><span class="sxs-lookup"><span data-stu-id="2a265-250">R23</span></span>   |   <span data-ttu-id="2a265-251">R231</span><span class="sxs-lookup"><span data-stu-id="2a265-251">R231</span></span>   |   <span data-ttu-id="2a265-252">C2</span><span class="sxs-lookup"><span data-stu-id="2a265-252">C2</span></span>   |   <span data-ttu-id="2a265-253">C23</span><span class="sxs-lookup"><span data-stu-id="2a265-253">C23</span></span>   |   <span data-ttu-id="2a265-254">C231</span><span class="sxs-lookup"><span data-stu-id="2a265-254">C231</span></span>   |   <span data-ttu-id="2a265-255">17</span><span class="sxs-lookup"><span data-stu-id="2a265-255">17</span></span>   |
|   <span data-ttu-id="2a265-256">R2</span><span class="sxs-lookup"><span data-stu-id="2a265-256">R2</span></span>   |   <span data-ttu-id="2a265-257">R23</span><span class="sxs-lookup"><span data-stu-id="2a265-257">R23</span></span>   |   <span data-ttu-id="2a265-258">R232</span><span class="sxs-lookup"><span data-stu-id="2a265-258">R232</span></span>   |   <span data-ttu-id="2a265-259">C2</span><span class="sxs-lookup"><span data-stu-id="2a265-259">C2</span></span>   |   <span data-ttu-id="2a265-260">C23</span><span class="sxs-lookup"><span data-stu-id="2a265-260">C23</span></span>   |   <span data-ttu-id="2a265-261">C232</span><span class="sxs-lookup"><span data-stu-id="2a265-261">C232</span></span>   |   <span data-ttu-id="2a265-262">18</span><span class="sxs-lookup"><span data-stu-id="2a265-262">18</span></span>   |
|   <span data-ttu-id="2a265-263">R2</span><span class="sxs-lookup"><span data-stu-id="2a265-263">R2</span></span>   |   <span data-ttu-id="2a265-264">R23</span><span class="sxs-lookup"><span data-stu-id="2a265-264">R23</span></span>   |   <span data-ttu-id="2a265-265">R233</span><span class="sxs-lookup"><span data-stu-id="2a265-265">R233</span></span>   |   <span data-ttu-id="2a265-266">C2</span><span class="sxs-lookup"><span data-stu-id="2a265-266">C2</span></span>   |   <span data-ttu-id="2a265-267">C23</span><span class="sxs-lookup"><span data-stu-id="2a265-267">C23</span></span>   |   <span data-ttu-id="2a265-268">C233</span><span class="sxs-lookup"><span data-stu-id="2a265-268">C233</span></span>   |   <span data-ttu-id="2a265-269">19</span><span class="sxs-lookup"><span data-stu-id="2a265-269">19</span></span>   |

<span data-ttu-id="2a265-270">สร้างโครงการวิชวลเริ่มต้นและใช้ตัวอย่างของ `capabilities.json`</span><span class="sxs-lookup"><span data-stu-id="2a265-270">Create the default visual project and apply sample of `capabilities.json`.</span></span>

<span data-ttu-id="2a265-271">รหัสแหล่งข้อมูลของวิชวลเริ่มต้นหลังจากลบรหัสที่ไม่จำเป็นจะมีลักษณะ:</span><span class="sxs-lookup"><span data-stu-id="2a265-271">Default visual source code after removing unessesray code will look:</span></span>

```typescript
"use strict";

// ... default imports

import { VisualSettings } from "./settings";

export class Visual implements IVisual {
    private target: HTMLElement;
    private settings: VisualSettings;


    constructor(options: VisualConstructorOptions) {
        console.log('Visual constructor', options);
        this.target = options.element;
        this.host = options.host;
    }

    public update(options: VisualUpdateOptions) {
        this.settings = Visual.parseSettings(options && options.dataViews && options.dataViews[0]);
        console.log('Visual update', options);

    }

    private static parseSettings(dataView: DataView): VisualSettings {
        return <VisualSettings>VisualSettings.parse(dataView);
    }

    /**
     * This function gets called for each of the objects defined in the capabilities files and allows you to select which of the
     * objects and properties you want to expose to the users in the property pane.
     *
     */
    public enumerateObjectInstances(options: EnumerateVisualObjectInstancesOptions): VisualObjectInstance[] | VisualObjectInstanceEnumerationObject {
        return VisualSettings.enumerateObjectInstances(this.settings || VisualSettings.getDefault(), options);
    }
}
```

<span data-ttu-id="2a265-272">นำเข้าอินเทอร์เฟสที่จำเป็นเพื่อประมวลผลข้อมูลจาก Power BI:</span><span class="sxs-lookup"><span data-stu-id="2a265-272">Import required interfaces to process data from Power BI:</span></span>

```typescript
import DataViewMatrix = powerbi.DataViewMatrix;
import DataViewMatrixNode = powerbi.DataViewMatrixNode;
import DataViewHierarchyLevel = powerbi.DataViewHierarchyLevel;
```

<span data-ttu-id="2a265-273">สร้างองค์ประกอบ `div` สองแบบสำหรับเค้าโครงวิชวล:</span><span class="sxs-lookup"><span data-stu-id="2a265-273">Create two `div` elements for visual layout:</span></span>

```typescript
constructor(options: VisualConstructorOptions) {
    // ...
    this.rowsDiv = document.createElement("div");
    this.target.appendChild(this.rowsDiv);

    this.colsDiv = document.createElement("div");
    this.target.appendChild(this.colsDiv);
    this.target.style.overflowY = "auto";
}
```

<span data-ttu-id="2a265-274">ตรวจสอบข้อมูลในวิธีการ `update` เพื่อให้แน่ใจว่าวิชวลได้รับข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="2a265-274">Check the data in `update` method, to ensure that visual gets data:</span></span>

```typescript
public update(options: VisualUpdateOptions) {
    this.settings = Visual.parseSettings(options && options.dataViews && options.dataViews[0]);
    console.log('Visual update', options);

    const dataView: DataView = options.dataViews[0];
    const matrixDataView: DataViewMatrix = dataView.matrix;

    if (!matrixDataView ||
        !matrixDataView.columns ||
        !matrixDataView.rows ) {
        return
    }
    // ...
}
```

<span data-ttu-id="2a265-275">ล้างเนื้อหาขององค์ประกอบ `div` ก่อนที่จะแสดงข้อมูลใหม่:</span><span class="sxs-lookup"><span data-stu-id="2a265-275">Clear content of `div` elements before render new data:</span></span>

```typescript
public update(options: VisualUpdateOptions) {
    // ...

    // remove old elements
    // to better performance use D3js pattern:
    // https://d3js.org/#enter-exit
    while (this.rowsDiv.firstChild) {
        this.rowsDiv.removeChild(this.rowsDiv.firstChild);
    }
    const prow = document.createElement("p");
    prow.innerText = "Rows";
    this.rowsDiv.appendChild(prow);

    while (this.colsDiv.firstChild) {
        this.colsDiv.removeChild(this.colsDiv.firstChild);
    }
    const pcol = document.createElement("p");
    pcol.innerText = "Columns";
    this.colsDiv.appendChild(pcol);
    // ...
}
```

<span data-ttu-id="2a265-276">สร้างฟังก์ชัน `treeWalker` เพื่อสำรวจโครงสร้างข้อมูลแบบเมทริกซ์:</span><span class="sxs-lookup"><span data-stu-id="2a265-276">Create `treeWalker` function to traverse matrix data structure:</span></span>

```typescript
public update(options: VisualUpdateOptions) {
    // ...
    const treeWalker = (matrixNode: DataViewMatrixNode, index: number, levels: DataViewHierarchyLevel[], div: HTMLDivElement)  => {

    }
    // ...
}
```

<span data-ttu-id="2a265-277">โดยที่ `matrixNode` คือโหนดปัจจุบัน `levels` คือคอลัมน์เมตาดาต้าของระดับลำดับชั้นนี้ `div` - องค์ประกอบหลักสำหรับองค์ประกอบ HTML ย่อย</span><span class="sxs-lookup"><span data-stu-id="2a265-277">Where `matrixNode` is the current node, `levels` is metadata columns of this hierarchy level, `div` - parent element for child HTML elements.</span></span>

<span data-ttu-id="2a265-278">`treeWalker` คือฟังก์ชันแบบเรียกใช้ซ้ำ จำเป็นต้องสร้างองค์ประกอบ `div` และ `p` สำหรับข้อความเป็นส่วนหัว และเรียกใช้ฟังก์ชันสำหรับองค์ประกอบย่อยของโหนด:</span><span class="sxs-lookup"><span data-stu-id="2a265-278">The `treeWalker` is recursive function, need to create `div` element and `p` for text as header, and call the function for child elements of node:</span></span>

```typescript
public update(options: VisualUpdateOptions) {
    // ...
    const treeWalker = (matrixNode: DataViewMatrixNode, index: number, levels: DataViewHierarchyLevel[], div: HTMLDivElement)  => {
        // ...

        if (matrixNode.children) {
            const childDiv = document.createElement("div");
            childDiv.classList.add("vertical");
            div.appendChild(childDiv);

            const p = document.createElement("p");
            const level = levels[matrixNode.level]; // get current level column metadata from current node
            p.innerText = level.sources[level.sources.length - 1].displayName; // get column name from metadata

            childDiv.appendChild(p); // add paragraph element to div element
            matrixNode.children.forEach((node, index) => treeWalker(node, levels, childDiv, ++levelIndex));
        }
    }
    // ...
}
```

<span data-ttu-id="2a265-279">เรียกใช้ฟังก์ชันสำหรับองค์ประกอบระดับสูงของคอลัมน์และแถวของโครงสร้างมุมมองข้อมูลแบบเมทริกซ์:</span><span class="sxs-lookup"><span data-stu-id="2a265-279">Call the function for root elements of column and row of matrix data view structure:</span></span>

```typescript
public update(options: VisualUpdateOptions) {
    // ...
    const treeWalker = (matrixNode: DataViewMatrixNode, index: number, levels: DataViewHierarchyLevel[], div: HTMLDivElement)  => {
        // ...
    }
    // ...
    // remove old elements
    // ...

    // ...
    const rowRoot: DataViewMatrixNode = matrixDataView.rows.root;
    rowRoot.children.forEach((node) => treeWalker(node, matrixDataView.rows.levels, this.rowsDiv));

    const colRoot = matrixDataView.columns.root;
    colRoot.children.forEach((node) => treeWalker(node, matrixDataView.columns.levels, this.colsDiv));
}
```

<span data-ttu-id="2a265-280">สร้าง selectionID สำหรับโหนดและสร้างปุ่มเพื่อแสดงโหนด:</span><span class="sxs-lookup"><span data-stu-id="2a265-280">Generate selectionID for nodes and Create buttons to display nodes:</span></span>

```typescript
public update(options: VisualUpdateOptions) {
    // ...
    const treeWalker = (matrixNode: DataViewMatrixNode, index: number, levels: DataViewHierarchyLevel[], div: HTMLDivElement)  => {
        const selectionID: ISelectionID = this.host.createSelectionIdBuilder()
            .withMatrixNode(matrixNode, levels)
            .createSelectionId();

        let nodeBlock = document.createElement("button");
        nodeBlock.innerText = matrixNode.value.toString();

        nodeBlock.addEventListener("click", (event) => {
            // call select method in the selection manager
            this.selectionManager.select(selectionID);
        });

        nodeBlock.addEventListener("contextmenu", (event) => {
            // call showContextMenu method to display context menu on the visual
            this.selectionManager.showContextMenu(selectionID, {
                x: event.clientX,
                y: event.clientY
            });
            event.preventDefault();
        });
        // ...
    }
    // ...
}
```

<span data-ttu-id="2a265-281">ขั้นตอนหลักของการใช้การไฮไลต์คือการประมวลผลอาร์เรย์เพิ่มเติมของค่า</span><span class="sxs-lookup"><span data-stu-id="2a265-281">The main step of using highlighting is to process additional array of values.</span></span>

<span data-ttu-id="2a265-282">หากคุณตรวจสอบวัตถุของโหนดเทอร์มินัล คุณจะเห็นว่าอาร์เรย์ค่ามีคุณสมบัติสองอย่างคือ ค่าและไฮไลต์:</span><span class="sxs-lookup"><span data-stu-id="2a265-282">If you inspect the object of terminal node, you can see that the values array has two properties - value and highlight:</span></span>

```javascript
JSON.stringify(options.dataViews[0].matrix.rows.root.children[0].children[0].children[0], null, " ");
```

```json
{
 "level": 2,
 "levelValues": [
  {
   "value": "R233",
   "levelSourceIndex": 0
  }
 ],
 "value": "R233",
 "identity": {
  "identityIndex": 2
 },
 "values": {
  "0": {
   "value": null,
   "highlight": null
  },
  "1": {
   "value": 19,
   "highlight": 19
  }
 }
}
```

<span data-ttu-id="2a265-283">โดยที่คุณสมบัติ `value` แสดงค่าของโหนดโดยไม่ต้องใช้ตัวเลือกจากวิชวลอื่น ๆ และคุณสมบัติการไฮไลต์แสดงให้เห็นว่าเป็นส่วนหนึ่งของข้อมูลที่ถูกไฮไลต์</span><span class="sxs-lookup"><span data-stu-id="2a265-283">Where `value` property represents value of node without applying a selection from other visual, and highlight property indicates which part of data was highlighted.</span></span>

> [!NOTE]
> <span data-ttu-id="2a265-284">ค่าของคุณสมบัติ `highlight` อาจน้อยกว่าค่าของคุณสมบัติ `value`</span><span class="sxs-lookup"><span data-stu-id="2a265-284">Value of `highlight` property can be less that value of `value` property.</span></span>
> <span data-ttu-id="2a265-285">หมายความว่ามีการไฮไลต์ค่าบางส่วน</span><span class="sxs-lookup"><span data-stu-id="2a265-285">In means that value was higlighted partially.</span></span>

<span data-ttu-id="2a265-286">เพิ่มรหัสเพื่อประมวลผลอาร์เรย์ `values` ของโหนดถ้าแสดง:</span><span class="sxs-lookup"><span data-stu-id="2a265-286">Add the code to process the `values` array of node if it is presented:</span></span>

```typescript
public update(options: VisualUpdateOptions) {
    // ...
    const treeWalker = (matrixNode: DataViewMatrixNode, index: number, levels: DataViewHierarchyLevel[], div: HTMLDivElement)  => {
        // ...

        if (matrixNode.values) {
            const sumOfValues = Object.keys(matrixNode.values) // get key property of object (value are 0 to N)
                .map(key => +matrixNode.values[key].value) // convert key property to number
                .reduce((prev, curr) => prev + curr) // sum of values

            let sumOfHighlights = sumOfValues;
            sumOfHighlights = Object.keys(matrixNode.values) // get key property of object (value are 0 to N)
                .map(key => matrixNode.values[key].highlight ? +matrixNode.values[key].highlight : null ) // convert key property to number if it exists
                .reduce((prev, curr) => curr ? prev + curr : null) // convert key property to number

            // create div container for value and highlighted value
            const vals = document.createElement("div");
            vals.classList.add("vertical")
            vals.classList.replace("vertical", "horizontal");
            // create paragraph element for label
            const highlighted = document.createElement("p");
            // Display complete value and highlighted value
            highlighted.innerText = `${sumOfHighlights}/${sumOfValues}`;

            // create div container for value
            const valueDiv = document.createElement("div");
            valueDiv.style.width = sumOfValues * 10 + "px";
            valueDiv.classList.add("value");

            // create div container for highlighted values
            const highlightsDiv = document.createElement("div");
            highlightsDiv.style.width = sumOfHighlights * 10 + "px";
            highlightsDiv.classList.add("highlight");
            valueDiv.appendChild(highlightsDiv);

            // append button and paragraph to div containers to parent div
            vals.appendChild(nodeBlock);
            vals.appendChild(valueDiv);
            vals.appendChild(highlighted);
            div.appendChild(vals);
        } else {
            div.appendChild(nodeBlock);
        }

        if (matrixNode.children) {
            // ...
        }
    }
    // ...
}
```

<span data-ttu-id="2a265-287">ด้วยเหตุนี้ คุณจะได้รับวิชวลที่มีปุ่มและค่า `highlighted value/default value`</span><span class="sxs-lookup"><span data-stu-id="2a265-287">As the result you'll get the visual with buttons and values `highlighted value/default value`</span></span>

![วิชวลที่มีการแมปและการไฮไลต์มุมมองข้อมูลแบบเมทริกซ์](media/highlight/dev-matrix-visual-highlight-demo.gif)

## <a name="next-steps"></a><span data-ttu-id="2a265-289">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="2a265-289">Next steps</span></span>

* [<span data-ttu-id="2a265-290">อ่านเกี่ยวกับการแมปมุมมองข้อมูลแบบเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="2a265-290">Read about matrix data view mappings</span></span>](dataview-mappings.md#matrix-data-mapping)

* [<span data-ttu-id="2a265-291">อ่านเกี่ยวกับความสามารถของวิชวล</span><span class="sxs-lookup"><span data-stu-id="2a265-291">Read about capabilities of the visual</span></span>](capabilities.md)
