---
title: บทนำสู่การใช้งานยูทิลิตี้การจัดรูปแบบของวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการใช้ยูทิลิตี้การจัดรูปแบบเพื่อจัดรูปแบบค่าและใช้การแปลเป็นภาษาท้องถิ่นกับค่าในวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: rkarlin
manager: rkarlin
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: reference
ms.date: 06/18/2019
ms.openlocfilehash: 564f6587ff361e3b2860bafb4ae43bc19ad8c2ba
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887810"
---
# <a name="formatting-utils"></a><span data-ttu-id="49fe6-104">ยูทิลิตี้การจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="49fe6-104">Formatting utils</span></span>

<span data-ttu-id="49fe6-105">ยูทิลิตี้การจัดรูปแบบประกอบด้วยคลาส อินเทอร์เฟซ และเมธอดการจัดรูปแบบค่า</span><span class="sxs-lookup"><span data-stu-id="49fe6-105">Formatting utils contains the classes, interfaces, and methods to format values.</span></span> <span data-ttu-id="49fe6-106">นอกจากนี้ยังประกอบด้วยเมธอด extender เพื่อประมวลผลสตริงและวัดขนาดข้อความในเอกสาร SVG/HTML</span><span class="sxs-lookup"><span data-stu-id="49fe6-106">It also contains extender methods to process strings, and measure text size in SVG/HTML document.</span></span>

## <a name="text-measurement-service"></a><span data-ttu-id="49fe6-107">บริการการวัดข้อความ</span><span class="sxs-lookup"><span data-stu-id="49fe6-107">Text measurement service</span></span>

<span data-ttu-id="49fe6-108">โมดูลมอบฟังก์ชันและอินเทอร์เฟซต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="49fe6-108">The module provides the following functions and interfaces:</span></span>

### <a name="textproperties-interface"></a><span data-ttu-id="49fe6-109">อินเทอร์เฟซ TextProperties</span><span class="sxs-lookup"><span data-stu-id="49fe6-109">TextProperties interface</span></span>

<span data-ttu-id="49fe6-110">อินเทอร์เฟซนี้จะอธิบายคุณสมบัติทั่วไปของข้อความ</span><span class="sxs-lookup"><span data-stu-id="49fe6-110">This interface describes common properties of the text.</span></span>

```typescript
interface TextProperties {
    text?: string;
    fontFamily: string;
    fontSize: string;
    fontWeight?: string;
    fontStyle?: string;
    fontVariant?: string;
    whiteSpace?: string;
}
```

### <a name="measuresvgtextwidth"></a><span data-ttu-id="49fe6-111">measureSvgTextWidth</span><span class="sxs-lookup"><span data-stu-id="49fe6-111">measureSvgTextWidth</span></span>

<span data-ttu-id="49fe6-112">ฟังก์ชันนี้วัดความกว้างของข้อความด้วยคุณสมบัติข้อความ SVG ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="49fe6-112">This function measures the width of the text with the given SVG text properties.</span></span>

```typescript
function measureSvgTextWidth(textProperties: TextProperties, text?: string): number;
```

<span data-ttu-id="49fe6-113">Example of using `measureSvgTextWidth`:</span><span class="sxs-lookup"><span data-stu-id="49fe6-113">Example of using `measureSvgTextWidth`:</span></span>

```typescript
import { textMeasurementService } from "powerbi-visuals-utils-formattingutils";
import TextProperties = textMeasurementService.TextProperties;
// ...

let textProperties: TextProperties = {
    text: "Microsoft PowerBI",
    fontFamily: "sans-serif",
    fontSize: "24px"
};

textMeasurementService.measureSvgTextWidth(textProperties);

// returns: 194.71875
```

### <a name="measuresvgtextrect"></a><span data-ttu-id="49fe6-114">measureSvgTextRect</span><span class="sxs-lookup"><span data-stu-id="49fe6-114">measureSvgTextRect</span></span>

<span data-ttu-id="49fe6-115">ฟังก์ชันนี้คืนค่า rect ด้วยคุณสมบัติข้อความ SVG ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="49fe6-115">This function returns a rect with the given SVG text properties.</span></span>

```typescript
function measureSvgTextRect(textProperties: TextProperties, text?: string): SVGRect;
```

<span data-ttu-id="49fe6-116">Example of using `measureSvgTextRect`:</span><span class="sxs-lookup"><span data-stu-id="49fe6-116">Example of using `measureSvgTextRect`:</span></span>

```typescript
import { textMeasurementService } from "powerbi-visuals-utils-formattingutils";
import TextProperties = textMeasurementService.TextProperties;
// ...

let textProperties: TextProperties = {
    text: "Microsoft PowerBI",
    fontFamily: "sans-serif",
    fontSize: "24px"
};

textMeasurementService.measureSvgTextRect(textProperties);

// returns: { x: 0, y: -22, width: 194.71875, height: 27 }
```

### <a name="measuresvgtextheight"></a><span data-ttu-id="49fe6-117">measureSvgTextHeight</span><span class="sxs-lookup"><span data-stu-id="49fe6-117">measureSvgTextHeight</span></span>

<span data-ttu-id="49fe6-118">ฟังก์ชันนี้วัดความสูงของข้อความด้วยคุณสมบัติข้อความ SVG ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="49fe6-118">This function measures the height of the text with the given SVG text properties.</span></span>

```typescript
function measureSvgTextHeight(textProperties: TextProperties, text?: string): number;
```

<span data-ttu-id="49fe6-119">Example of using `measureSvgTextHeight`:</span><span class="sxs-lookup"><span data-stu-id="49fe6-119">Example of using `measureSvgTextHeight`:</span></span>

```typescript
import { textMeasurementService } from "powerbi-visuals-utils-formattingutils";
import TextProperties = textMeasurementService.TextProperties;
// ...


let textProperties: TextProperties = {
    text: "Microsoft PowerBI",
    fontFamily: "sans-serif",
    fontSize: "24px"
};

textMeasurementService.measureSvgTextHeight(textProperties);

// returns: 27
```

### <a name="estimatesvgtextbaselinedelta"></a><span data-ttu-id="49fe6-120">estimateSvgTextBaselineDelta</span><span class="sxs-lookup"><span data-stu-id="49fe6-120">estimateSvgTextBaselineDelta</span></span>

<span data-ttu-id="49fe6-121">ฟังก์ชันนี้จะส่งกลับเส้นอ้างอิงของคุณสมบัติข้อความ SVG ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="49fe6-121">This function returns a baseline of the given SVG text properties.</span></span>

```typescript
function estimateSvgTextBaselineDelta(textProperties: TextProperties): number;
```

<span data-ttu-id="49fe6-122">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="49fe6-122">Example:</span></span>

```typescript
import { textMeasurementService } from "powerbi-visuals-utils-formattingutils";
import TextProperties = textMeasurementService.TextProperties;
// ...

let textProperties: TextProperties = {
    text: "Microsoft PowerBI",
    fontFamily: "sans-serif",
    fontSize: "24px"
};

textMeasurementService.estimateSvgTextBaselineDelta(textProperties);

// returns: 5
```

### <a name="estimatesvgtextheight"></a><span data-ttu-id="49fe6-123">estimateSvgTextHeight</span><span class="sxs-lookup"><span data-stu-id="49fe6-123">estimateSvgTextHeight</span></span>

<span data-ttu-id="49fe6-124">ฟังก์ชันนี้ประมาณความสูงของข้อความด้วยคุณสมบัติข้อความ SVG ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="49fe6-124">This function estimates the height of the text with the given SVG text properties.</span></span>

```typescript
function estimateSvgTextHeight(textProperties: TextProperties, tightFightForNumeric?: boolean): number;
```

<span data-ttu-id="49fe6-125">Example of using `estimateSvgTextHeight`:</span><span class="sxs-lookup"><span data-stu-id="49fe6-125">Example of using `estimateSvgTextHeight`:</span></span>

```typescript
import { textMeasurementService } from "powerbi-visuals-utils-formattingutils";
import TextProperties = textMeasurementService.TextProperties;
// ...

let textProperties: TextProperties = {
    text: "Microsoft PowerBI",
    fontFamily: "sans-serif",
    fontSize: "24px"
};

textMeasurementService.estimateSvgTextHeight(textProperties);

// returns: 27
```

<span data-ttu-id="49fe6-126">คุณสามารถดูโค้ดตัวอย่างของวิชวลแบบกำหนดเอง [ที่นี่](https://github.com/Microsoft/powerbi-visuals-sankey/blob/4d544ea145b4e15006083a3610dfead3da5f61a4/src/visual.ts#L372)</span><span class="sxs-lookup"><span data-stu-id="49fe6-126">You can take a look at the example code of the custom visual [here](https://github.com/Microsoft/powerbi-visuals-sankey/blob/4d544ea145b4e15006083a3610dfead3da5f61a4/src/visual.ts#L372).</span></span>

### <a name="measuresvgtextelementwidth"></a><span data-ttu-id="49fe6-127">measureSvgTextElementWidth</span><span class="sxs-lookup"><span data-stu-id="49fe6-127">measureSvgTextElementWidth</span></span>

<span data-ttu-id="49fe6-128">ฟังก์ชันนี้วัดความกว้างของ svgElement</span><span class="sxs-lookup"><span data-stu-id="49fe6-128">This function measures the width of the svgElement.</span></span>

```typescript
function measureSvgTextElementWidth(svgElement: SVGTextElement): number;
```

<span data-ttu-id="49fe6-129">ตัวอย่างของการใช้ measureSvgTextElementWidth:</span><span class="sxs-lookup"><span data-stu-id="49fe6-129">Example of using measureSvgTextElementWidth:</span></span>

```typescript
import { textMeasurementService } from "powerbi-visuals-utils-formattingutils";
// ...

let svg: D3.Selection = d3.select("body").append("svg");

svg.append("text")
    .text("Microsoft PowerBI")
    .attr({
        "x": 25,
        "y": 25
    })
    .style({
        "font-family": "sans-serif",
        "font-size": "24px"
    });

let textElement: D3.Selection = svg.select("text");

textMeasurementService.measureSvgTextElementWidth(textElement.node());

// returns: 194.71875
```

### <a name="getmeasurementproperties"></a><span data-ttu-id="49fe6-130">getMeasurementProperties</span><span class="sxs-lookup"><span data-stu-id="49fe6-130">getMeasurementProperties</span></span>

<span data-ttu-id="49fe6-131">ฟังก์ชันนี้ดึงข้อมูลคุณสมบัติการวัดข้อความขององค์ประกอบ DOM ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="49fe6-131">This function fetches the text measurement properties of the given DOM element.</span></span>

```typescript
function getMeasurementProperties(element: Element): TextProperties;
```

<span data-ttu-id="49fe6-132">Example of using `getMeasurementProperties`:</span><span class="sxs-lookup"><span data-stu-id="49fe6-132">Example of using `getMeasurementProperties`:</span></span>

```typescript
import { textMeasurementService } from "powerbi-visuals-utils-formattingutils";
// ...

let element: JQuery = $(document.createElement("div"));

element.text("Microsoft PowerBI");

element.css({
    "width": 500,
    "height": 500,
    "font-family": "sans-serif",
    "font-size": "32em",
    "font-weight": "bold",
    "font-style": "italic",
    "white-space": "nowrap"
});

textMeasurementService.getMeasurementProperties(element.get(0));

/* returns: {
    fontFamily:"sans-serif",
    fontSize: "32em",
    fontStyle: "italic",
    fontVariant: "",
    fontWeight: "bold",
    text: "Microsoft PowerBI",
    whiteSpace: "nowrap"
}*/
```

### <a name="getsvgmeasurementproperties"></a><span data-ttu-id="49fe6-133">getSvgMeasurementProperties</span><span class="sxs-lookup"><span data-stu-id="49fe6-133">getSvgMeasurementProperties</span></span>

<span data-ttu-id="49fe6-134">ฟังก์ชันนี้ดึงข้อมูลคุณสมบัติการวัดข้อความขององค์ประกอบข้อความ SVG ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="49fe6-134">This function fetches the text measurement properties of the given SVG text element.</span></span>

```typescript
function getSvgMeasurementProperties(svgElement: SVGTextElement): TextProperties;
```

<span data-ttu-id="49fe6-135">Example of using `getSvgMeasurementProperties`:</span><span class="sxs-lookup"><span data-stu-id="49fe6-135">Example of using `getSvgMeasurementProperties`:</span></span>

```typescript
import { textMeasurementService } from "powerbi-visuals-utils-formattingutils";
// ...

let svg: D3.Selection = d3.select("body").append("svg");

let textElement: D3.Selection = svg.append("text")
    .text("Microsoft PowerBI")
    .attr({
        "x": 25,
        "y": 25
    })
    .style({
        "font-family": "sans-serif",
        "font-size": "24px"
    });

textMeasurementService.getSvgMeasurementProperties(textElement.node());

/* returns: {
    "text": "Microsoft PowerBI",
    "fontFamily": "sans-serif",
    "fontSize": "24px",
    "fontWeight": "normal",
    "fontStyle": "normal",
    "fontVariant": "normal",
    "whiteSpace": "nowrap"
}*/
```

## <a name="getdivelementwidth"></a><span data-ttu-id="49fe6-136">getDivElementWidth</span><span class="sxs-lookup"><span data-stu-id="49fe6-136">getDivElementWidth</span></span>

<span data-ttu-id="49fe6-137">ฟังก์ชันนี้ส่งกลับความกว้างขององค์ประกอบ div</span><span class="sxs-lookup"><span data-stu-id="49fe6-137">This function returns the width of a div element.</span></span>

```typescript
function getDivElementWidth(element: JQuery): string;
```

<span data-ttu-id="49fe6-138">Example of using `getDivElementWidth`:</span><span class="sxs-lookup"><span data-stu-id="49fe6-138">Example of using `getDivElementWidth`:</span></span>

```typescript
import { textMeasurementService } from "powerbi-visuals-utils-formattingutils";
// ...

let svg: Element = d3.select("body")
    .append("div")
    .style({
        "width": "150px",
        "height": "150px"
    })
    .node();

textMeasurementService.getDivElementWidth(svg)

// returns: 150px
```

### <a name="gettailoredtextordefault"></a><span data-ttu-id="49fe6-139">getTailoredTextOrDefault</span><span class="sxs-lookup"><span data-stu-id="49fe6-139">getTailoredTextOrDefault</span></span>

<span data-ttu-id="49fe6-140">เปรียบเทียบขนาดป้ายข้อความกับขนาดที่มีและแสดงรูปวงรีเมื่อขนาดที่มีอยู่มีขนาดเล็กกว่า</span><span class="sxs-lookup"><span data-stu-id="49fe6-140">Compares labels text size to the available size and renders ellipses when the available size is smaller.</span></span>

```typescript
function getTailoredTextOrDefault(textProperties: TextProperties, maxWidth: number): string;
```

<span data-ttu-id="49fe6-141">Example of using `getTailoredTextOrDefault`:</span><span class="sxs-lookup"><span data-stu-id="49fe6-141">Example of using `getTailoredTextOrDefault`:</span></span>

```typescript
import { textMeasurementService } from "powerbi-visuals-utils-formattingutils";
import TextProperties = textMeasurementService.TextProperties;
// ...

let textProperties: TextProperties = {
    text: "Microsoft PowerBI!",
    fontFamily: "sans-serif",
    fontSize: "24px"
};

textMeasurementService.getTailoredTextOrDefault(textProperties, 100);

// returns: Micros...
```

## <a name="string-extensions"></a><span data-ttu-id="49fe6-142">ส่วนขยายของสตริง</span><span class="sxs-lookup"><span data-stu-id="49fe6-142">String extensions</span></span>

<span data-ttu-id="49fe6-143">โมดูลมอบฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="49fe6-143">The module provides the following functions:</span></span>

## <a name="endswith"></a><span data-ttu-id="49fe6-144">endsWith</span><span class="sxs-lookup"><span data-stu-id="49fe6-144">endsWith</span></span>

<span data-ttu-id="49fe6-145">ฟังก์ชันนี้ตรวจสอบว่าสตริงลงท้ายด้วยซับสตริงหรือไม่</span><span class="sxs-lookup"><span data-stu-id="49fe6-145">This function checks if a string ends with a substring.</span></span>

```typescript
function endsWith(str: string, suffix: string): boolean;
```

<span data-ttu-id="49fe6-146">Example of using `endsWith`:</span><span class="sxs-lookup"><span data-stu-id="49fe6-146">Example of using `endsWith`:</span></span>

```typescript
import { stringExtensions } from "powerbi-visuals-utils-formattingutils";
// ...

stringExtensions.endsWith("Power BI", "BI");

// returns: true
```

### <a name="equalignorecase"></a><span data-ttu-id="49fe6-147">equalIgnoreCase</span><span class="sxs-lookup"><span data-stu-id="49fe6-147">equalIgnoreCase</span></span>

<span data-ttu-id="49fe6-148">ฟังก์ชันนี้เปรียบเทียบสตริงที่ ละเว้นตัวพิมพ์ใหญ่-เล็ก</span><span class="sxs-lookup"><span data-stu-id="49fe6-148">This function compares strings, ignoring case.</span></span>

```typescript
function equalIgnoreCase(a: string, b: string): boolean;
```

<span data-ttu-id="49fe6-149">Example of using `equalIgnoreCase`:</span><span class="sxs-lookup"><span data-stu-id="49fe6-149">Example of using `equalIgnoreCase`:</span></span>

```typescript
import { stringExtensions } from "powerbi-visuals-utils-formattingutils";
// ...

stringExtensions.equalIgnoreCase("Power BI", "power bi");

// returns: true
```

### <a name="startswith"></a><span data-ttu-id="49fe6-150">startsWith</span><span class="sxs-lookup"><span data-stu-id="49fe6-150">startsWith</span></span>

<span data-ttu-id="49fe6-151">ฟังก์ชันนี้ตรวจสอบว่าสตริงเริ่มต้นด้วยซับสตริงหรือไม่</span><span class="sxs-lookup"><span data-stu-id="49fe6-151">This function checks if a string starts with a substring;</span></span>

```typescript
function startsWith(a: string, b: string): boolean;
```

<span data-ttu-id="49fe6-152">Example of using `startsWith`:</span><span class="sxs-lookup"><span data-stu-id="49fe6-152">Example of using `startsWith`:</span></span>

```typescript
import { stringExtensions } from "powerbi-visuals-utils-formattingutils";
// ...

stringExtensions.startsWith("Power BI", "Power");

// returns: true
```

### <a name="contains"></a><span data-ttu-id="49fe6-153">ประกอบด้วย</span><span class="sxs-lookup"><span data-stu-id="49fe6-153">contains</span></span>

<span data-ttu-id="49fe6-154">ฟังก์ชันนี้ตรวจสอบว่าสตริงประกอบด้วยซับสตริงที่ระบุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="49fe6-154">This function checks if a string contains a specified substring.</span></span>

```typescript
function contains(source: string, substring: string): boolean;
```

<span data-ttu-id="49fe6-155">ตัวอย่างของการใช้เมธอด `contains`:</span><span class="sxs-lookup"><span data-stu-id="49fe6-155">Example of using `contains` method:</span></span>

```typescript
import { stringExtensions } from "powerbi-visuals-utils-formattingutils";
// ...

stringExtensions.contains("Microsoft Power BI Visuals", "Power BI");

// returns: true
```

### <a name="isnullorempty"></a><span data-ttu-id="49fe6-156">isNullOrEmpty</span><span class="sxs-lookup"><span data-stu-id="49fe6-156">isNullOrEmpty</span></span>

<span data-ttu-id="49fe6-157">ตรวจสอบว่าสตริงเป็น null หรือไม่ได้กำหนดหรือว่างเปล่า หรือไม่</span><span class="sxs-lookup"><span data-stu-id="49fe6-157">Checks if a string is null or undefined or empty.</span></span>

```typescript
function isNullOrEmpty(value: string): boolean;
```

<span data-ttu-id="49fe6-158">ตัวอย่างของการใช้ `isNullOrEmpty`:</span><span class="sxs-lookup"><span data-stu-id="49fe6-158">Example of `isNullOrEmpty` method:</span></span>

```typescript
import { stringExtensions } from "powerbi-visuals-utils-formattingutils";
// ...

stringExtensions.isNullOrEmpty(null);

// returns: true
```

## <a name="value-formatter"></a><span data-ttu-id="49fe6-159">Value formatter</span><span class="sxs-lookup"><span data-stu-id="49fe6-159">Value formatter</span></span>

<span data-ttu-id="49fe6-160">โมดูลมอบฟังก์ชัน อินเตอร์เฟส และคลาสต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="49fe6-160">The module provides the following functions, interfaces, and classes:</span></span>

## <a name="ivalueformatter"></a><span data-ttu-id="49fe6-161">IValueFormatter</span><span class="sxs-lookup"><span data-stu-id="49fe6-161">IValueFormatter</span></span>

<span data-ttu-id="49fe6-162">อินเทอร์เฟซนี้จะอธิบายเมธอดและคุณสมบัติสาธารณะ (public) ของตัวจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="49fe6-162">This interface describes public methods and properties of the formatter.</span></span>

```typescript
interface IValueFormatter {
    format(value: any): string;
    displayUnit?: DisplayUnit;
    options?: ValueFormatterOptions;
}
```

### <a name="ivalueformatterformat"></a><span data-ttu-id="49fe6-163">IValueFormatter.format</span><span class="sxs-lookup"><span data-stu-id="49fe6-163">IValueFormatter.format</span></span>

<span data-ttu-id="49fe6-164">เมธอดนี้จัดรูปแบบค่าที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="49fe6-164">This method formats the given value.</span></span>

```typescript
function format(value: any, format?: string, allowFormatBeautification?: boolean): string;
```

<span data-ttu-id="49fe6-165">ตัวอย่างสำหรับ `IValueFormatter.format`:</span><span class="sxs-lookup"><span data-stu-id="49fe6-165">Examples for `IValueFormatter.format`:</span></span>

#### <a name="the-thousand-formats"></a><span data-ttu-id="49fe6-166">รูปแบบพัน</span><span class="sxs-lookup"><span data-stu-id="49fe6-166">The thousand formats</span></span>

```typescript
import { valueFormatter } from "powerbi-visuals-utils-formattingutils";

let iValueFormatter = valueFormatter.create({ value: 1001 });

iValueFormatter.format(5678);

// returns: "5.68K"
```

#### <a name="the-million-formats"></a><span data-ttu-id="49fe6-167">รูปแบบล้าน</span><span class="sxs-lookup"><span data-stu-id="49fe6-167">The million formats</span></span>

```typescript
import { valueFormatter } from "powerbi-visuals-utils-formattingutils";

let iValueFormatter = valueFormatter.create({ value: 1e6 });

iValueFormatter.format(1234567890);

// returns: "1234.57M"
```

#### <a name="the-billion-formats"></a><span data-ttu-id="49fe6-168">รูปแบบพันล้าน</span><span class="sxs-lookup"><span data-stu-id="49fe6-168">The billion formats</span></span>

```typescript
import { valueFormatter } from "powerbi-visuals-utils-formattingutils";

let iValueFormatter = valueFormatter.create({ value: 1e9 });

iValueFormatter.format(1234567891236);

// returns: 1234.57bn
```

#### <a name="the-trillion-format"></a><span data-ttu-id="49fe6-169">รูปแบบล้านล้าน</span><span class="sxs-lookup"><span data-stu-id="49fe6-169">The trillion format</span></span>

```typescript
import { valueFormatter } from "powerbi-visuals-utils-formattingutils";

let iValueFormatter = valueFormatter.create({ value: 1e12 });

iValueFormatter.format(1234567891236);

// returns: 1.23T
```

#### <a name="the-exponent-format"></a><span data-ttu-id="49fe6-170">รูปแบบเลขชี้กำลัง</span><span class="sxs-lookup"><span data-stu-id="49fe6-170">The exponent format</span></span>

```typescript
import { valueFormatter } from "powerbi-visuals-utils-formattingutils";

let iValueFormatter = valueFormatter.create({ format: "E" });

iValueFormatter.format(1234567891236);

// returns: 1.234568E+012
```

### <a name="the-culture-selector"></a><span data-ttu-id="49fe6-171">ตัวเลือกวัฒนธรรม</span><span class="sxs-lookup"><span data-stu-id="49fe6-171">The culture selector</span></span>

```typescript
import { valueFormatter } from "powerbi-visuals-utils-formattingutils";

let valueFormatterUK = valueFormatter.create({ cultureSelector: "en-GB" });

valueFormatterUK.format(new Date(2007, 2, 3, 17, 42, 42));

// returns: 03/03/2007 17:42:42

let valueFormatterUSA = valueFormatter.create({ cultureSelector: "en-US" });

valueFormatterUSA.format(new Date(2007, 2, 3, 17, 42, 42));

// returns: 3/3/2007 5:42:42 PM
```

#### <a name="the-percentage-format"></a><span data-ttu-id="49fe6-172">รูปแบบเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="49fe6-172">The percentage format</span></span>

```typescript
import { valueFormatter } from "powerbi-visuals-utils-formattingutils";

let iValueFormatter = valueFormatter.create({ format: "0.00 %;-0.00 %;0.00 %" });

iValueFormatter.format(0.54);

// returns: 54.00 %
```

#### <a name="the-dates-format"></a><span data-ttu-id="49fe6-173">รูปแบบวันที่</span><span class="sxs-lookup"><span data-stu-id="49fe6-173">The dates format</span></span>

```typescript
import { valueFormatter } from "powerbi-visuals-utils-formattingutils";

let date = new Date(2016, 10, 28, 15, 36, 0),
    iValueFormatter = valueFormatter.create({});

iValueFormatter.format(date);

// returns: 11/28/2016 3:36:00 PM
```

#### <a name="the-boolean-format"></a><span data-ttu-id="49fe6-174">รูปแบบบูลีน</span><span class="sxs-lookup"><span data-stu-id="49fe6-174">The boolean format</span></span>

```typescript
import { valueFormatter } from "powerbi-visuals-utils-formattingutils";

let iValueFormatter = valueFormatter.create({});

iValueFormatter.format(true);

// returns: True
```

#### <a name="the-customized-precision"></a><span data-ttu-id="49fe6-175">ความแม่นยำแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="49fe6-175">The customized precision</span></span>

```typescript
import { valueFormatter } from "powerbi-visuals-utils-formattingutils";

let iValueFormatter = valueFormatter.create({ value: 0, precision: 3 });

iValueFormatter.format(3.141592653589793);

// returns: 3.142
```

<span data-ttu-id="49fe6-176">คุณสามารถดูโค้ดตัวอย่างของวิชวลแบบกำหนดเอง [ที่นี่](https://github.com/Microsoft/powerbi-visuals-sankey/blob/4d544ea145b4e15006083a3610dfead3da5f61a4/src/visual.ts#L359)</span><span class="sxs-lookup"><span data-stu-id="49fe6-176">You can take a look at the example code of the custom visual [here](https://github.com/Microsoft/powerbi-visuals-sankey/blob/4d544ea145b4e15006083a3610dfead3da5f61a4/src/visual.ts#L359).</span></span>

## <a name="valueformatteroptions"></a><span data-ttu-id="49fe6-177">ValueFormatterOptions</span><span class="sxs-lookup"><span data-stu-id="49fe6-177">ValueFormatterOptions</span></span>

<span data-ttu-id="49fe6-178">อินเตอร์เฟสนี้อธิบาย `options` ของ IValueFormatter และตัวเลือกของฟังก์ชัน 'สร้าง'</span><span class="sxs-lookup"><span data-stu-id="49fe6-178">This interface describes `options` of the IValueFormatter and options of 'create' function.</span></span>

```typescript
import { valueFormatter } from "powerbi-visuals-utils-formattingutils";
import ValueFormatterOptions = valueFormatter.ValueFormatterOptions;

interface ValueFormatterOptions {
    /** The format string to use. */
    format?: string;
    /** The data value. */
    value?: any;
    /** The data value. */
    value2?: any;
    /** The number of ticks. */
    tickCount?: any;
    /** The display unit system to use */
    displayUnitSystemType?: DisplayUnitSystemType;
    /** True if we are formatting single values in isolation (e.g. card), as opposed to multiple values with a common base (e.g. chart axes) */
    formatSingleValues?: boolean;
    /** True if we want to trim off unnecessary zeroes after the decimal and remove a space before the % symbol */
    allowFormatBeautification?: boolean;
    /** Specifies the maximum number of decimal places to show*/
    precision?: number;
    /** Detect axis precision based on value */
    detectAxisPrecision?: boolean;
    /** Specifies the column type of the data value */
    columnType?: ValueTypeDescriptor;
    /** Specifies the culture */
    cultureSelector?: string;
}
```

## <a name="create"></a><span data-ttu-id="49fe6-179">สร้าง</span><span class="sxs-lookup"><span data-stu-id="49fe6-179">create</span></span>

<span data-ttu-id="49fe6-180">เมธอดนี้สร้างอินสแตนซ์ของ IValueFormatter</span><span class="sxs-lookup"><span data-stu-id="49fe6-180">This method creates an instance of IValueFormatter.</span></span>

```typescript
import { valueFormatter } from "powerbi-visuals-utils-formattingutils";
import create = valueFormatter.create;

function create(options: ValueFormatterOptions): IValueFormatter;
```

### <a name="example-of-using-create"></a><span data-ttu-id="49fe6-181">ตัวอย่างของการใช้ create</span><span class="sxs-lookup"><span data-stu-id="49fe6-181">Example of using create</span></span>

```typescript
import { valueFormatter } from "powerbi-visuals-utils-formattingutils";

valueFormatter.create({});

// returns: an instance of IValueFormatter.
```

## <a name="next-steps"></a><span data-ttu-id="49fe6-182">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="49fe6-182">Next steps</span></span>

[<span data-ttu-id="49fe6-183">เพิ่มการแปลเป็นภาษาท้องถิ่นไปยังวิชวลแบบกำหนดเอง Power BI</span><span class="sxs-lookup"><span data-stu-id="49fe6-183">Add localizations to a Power BI custom visual</span></span>](localization.md)  
