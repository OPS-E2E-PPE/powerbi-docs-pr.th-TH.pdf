---
title: บทนำสู่การใช้งานยูทิลิตี้ SVG ของวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการใช้ยูทิลิตี้ SVG เพื่อลดความซับซ้อนของการปรับแต่ง SVG สำหรับวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
manager: rkarlin
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: reference
ms.date: 06/18/2019
ms.openlocfilehash: cf798ae13d874e354f6941d50982bfe26d73424d
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887764"
---
# <a name="svg-utils"></a><span data-ttu-id="f067c-104">ยูทิลิตี้ SVG</span><span class="sxs-lookup"><span data-stu-id="f067c-104">SVG utils</span></span>

<span data-ttu-id="f067c-105">SVGUtils เป็นชุดฟังก์ชันและคลาสเพื่อลดความซับซ้อนของการปรับใช้ SVG สำหรับวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="f067c-105">SVGUtils is a set of functions and classes to simplify SVG manipulations for Power BI visuals</span></span>

## <a name="installation"></a><span data-ttu-id="f067c-106">การติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="f067c-106">Installation</span></span>

<span data-ttu-id="f067c-107">หากต้องการติดตั้งแพ็คเกจ คุณควรเรียกใช้คำสั่งต่อไปนี้ในไดเรกทอรีด้วยวิชวลปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="f067c-107">To install the package, you should run the following command in the directory with your current visual:</span></span>

```bash
npm install powerbi-visuals-utils-svgutils --save
```

## <a name="cssconstants"></a><span data-ttu-id="f067c-108">CssConstants</span><span class="sxs-lookup"><span data-stu-id="f067c-108">CssConstants</span></span>

<span data-ttu-id="f067c-109">โมดูล `CssConstants` มีฟังก์ชันและอินเทอร์เฟสพิเศษในการทำงานกับตัวเลือกคลาส</span><span class="sxs-lookup"><span data-stu-id="f067c-109">The `CssConstants` module provides the special function and interface to work with class selectors.</span></span>

<span data-ttu-id="f067c-110">โมดูล `powerbi.extensibility.utils.svg.CssConstants` มีฟังก์ชันและอินเทอร์เฟสต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f067c-110">The `powerbi.extensibility.utils.svg.CssConstants` module provides the following function and interface:</span></span>

## <a name="classandselector"></a><span data-ttu-id="f067c-111">ClassAndSelector</span><span class="sxs-lookup"><span data-stu-id="f067c-111">ClassAndSelector</span></span>

<span data-ttu-id="f067c-112">อินเทอร์เฟซนี้จะอธิบายคุณสมบัติทั่วไปของตัวเลือกคลาส</span><span class="sxs-lookup"><span data-stu-id="f067c-112">This interface describes common properties of the class selector.</span></span>

```typescript
interface ClassAndSelector {
  class: string;
  selector: string;
}
```

### <a name="createclassandselector"></a><span data-ttu-id="f067c-113">createClassAndSelector</span><span class="sxs-lookup"><span data-stu-id="f067c-113">createClassAndSelector</span></span>

<span data-ttu-id="f067c-114">ฟังก์ชั้นนี้สร้างตัวอย่าง createClassAndSelector พร้อมกับชื่อของคลาสที่ตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="f067c-114">This function creates an instance of ClassAndSelector with the given name of the class.</span></span>

```typescript
function createClassAndSelector(className: string): ClassAndSelector;
```

<span data-ttu-id="f067c-115">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-115">Example:</span></span>

```typescript
import { CssConstants } from "powerbi-visuals-utils-svgutils";
import createClassAndSelector = CssConstants.createClassAndSelector;
import ClassAndSelector = CssConstants.ClassAndSelector;

let divSelector: ClassAndSelector = createClassAndSelector("sample-block");

divSelector.selector === ".sample-block"; // returns: true
divSelector.class === "sample-block"; // returns: true
```

## <a name="manipulation"></a><span data-ttu-id="f067c-116">การจัดการ</span><span class="sxs-lookup"><span data-stu-id="f067c-116">manipulation</span></span>

<span data-ttu-id="f067c-117">`manipulation` มีฟังก์ชันพิเศษบางอย่างที่สร้างสตริงสำหรับใช้กับคุณสมบัติการแปลง SVG</span><span class="sxs-lookup"><span data-stu-id="f067c-117">The `manipulation` provides some special functions to generate strings for using with SVG transform property.</span></span>

<span data-ttu-id="f067c-118">โมดูลมอบฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f067c-118">The module provides the following functions:</span></span>

### <a name="translate"></a><span data-ttu-id="f067c-119">แปล</span><span class="sxs-lookup"><span data-stu-id="f067c-119">translate</span></span>

<span data-ttu-id="f067c-120">ฟังก์ชันนี้สร้างสตริงแปลสำหรับใช้กับคุณสมบัติการแปลง SVG</span><span class="sxs-lookup"><span data-stu-id="f067c-120">This function creates a translate string for using with the SVG transform property.</span></span>

```typescript
function translate(x: number, y: number): string;
```

<span data-ttu-id="f067c-121">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-121">Example:</span></span>

```typescript
import { manipulation } from "powerbi-visuals-utils-svgutils";
// ...

manipulation.translate(100, 100);

// returns: translate(100,100)
```

### <a name="translatexwithpixels"></a><span data-ttu-id="f067c-122">translateXWithPixels</span><span class="sxs-lookup"><span data-stu-id="f067c-122">translateXWithPixels</span></span>

<span data-ttu-id="f067c-123">ฟังก์ชันนี้สร้างสตริงแปลX สำหรับใช้กับคุณสมบัติการแปลง SVG</span><span class="sxs-lookup"><span data-stu-id="f067c-123">This function creates a translateX string for using with the SVG transform property.</span></span>

```typescript
function translateXWithPixels(x: number): string;
```

<span data-ttu-id="f067c-124">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-124">Example:</span></span>

```typescript
import { manipulation } from "powerbi-visuals-utils-svgutils";
// ...

manipulation.translateXWithPixels(100);

// returns: translateX(100px)
```

### <a name="translatewithpixels"></a><span data-ttu-id="f067c-125">translateWithPixels</span><span class="sxs-lookup"><span data-stu-id="f067c-125">translateWithPixels</span></span>

<span data-ttu-id="f067c-126">ฟังก์ชันนี้สร้างสตริงแปลสำหรับใช้กับคุณสมบัติการแปลง SVG</span><span class="sxs-lookup"><span data-stu-id="f067c-126">This function creates a translate string for using with the SVG transform property.</span></span>

```typescript
function translateWithPixels(x: number, y: number): string;
```

<span data-ttu-id="f067c-127">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-127">Example:</span></span>

```typescript
import { manipulation } from "powerbi-visuals-utils-svgutils";
// ...

manipulation.translateWithPixels(100, 100);

// returns: translate(100px,100px)
```

### <a name="translateandrotate"></a><span data-ttu-id="f067c-128">translateAndRotate</span><span class="sxs-lookup"><span data-stu-id="f067c-128">translateAndRotate</span></span>

<span data-ttu-id="f067c-129">ฟังก์ชันนี้สร้างสตริงแปลหมุนสำหรับใช้กับคุณสมบัติการแปลง SVG</span><span class="sxs-lookup"><span data-stu-id="f067c-129">This function creates a translate-rotate string for using with the SVG transform property.</span></span>

```typescript
function translateAndRotate(
  x: number,
  y: number,
  px: number,
  py: number,
  angle: number
): string;
```

<span data-ttu-id="f067c-130">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-130">Example:</span></span>

```typescript
import { manipulation } from "powerbi-visuals-utils-svgutils";
// ...

manipulation.translateAndRotate(100, 100, 50, 50, 35);

// returns: translate(100,100) rotate(35,50,50)
```

### <a name="scale"></a><span data-ttu-id="f067c-131">สเกล</span><span class="sxs-lookup"><span data-stu-id="f067c-131">scale</span></span>

<span data-ttu-id="f067c-132">ฟังก์ชันนี้สร้างสตริงสเกลสำหรับใช้กับคุณสมบัติการแปลง CSS</span><span class="sxs-lookup"><span data-stu-id="f067c-132">This function creates a scale string for using in a CSS transform property.</span></span>

```typescript
function scale(scale: number): string;
```

<span data-ttu-id="f067c-133">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-133">Example:</span></span>

```typescript
import { manipulation } from "powerbi-visuals-utils-svgutils";
// ...

manipulation.scale(50);

// returns: scale(50)
```

### <a name="transformorigin"></a><span data-ttu-id="f067c-134">transformOrigin</span><span class="sxs-lookup"><span data-stu-id="f067c-134">transformOrigin</span></span>

<span data-ttu-id="f067c-135">ฟังก์ชันนี้สร้างข้อความแปลเดิมสำหรับใช้กับคุณสมบัติการแปลง CSS</span><span class="sxs-lookup"><span data-stu-id="f067c-135">This function creates a transform-origin string for using in a CSS transform-origin property.</span></span>

```typescript
function transformOrigin(xOffset: string, yOffset: string): string;
```

<span data-ttu-id="f067c-136">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-136">Example:</span></span>

```typescript
import { manipulation } from "powerbi-visuals-utils-svgutils";
// ...

manipulation.transformOrigin(5, 5);

// returns: 5 5
```

### <a name="flushalld3transitions"></a><span data-ttu-id="f067c-137">flushAllD3Transitions</span><span class="sxs-lookup"><span data-stu-id="f067c-137">flushAllD3Transitions</span></span>

<span data-ttu-id="f067c-138">ฟังก์ชันนี้ทำให้การเปลี่ยนแปลง D3 ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f067c-138">This function forces every transition of D3 to complete.</span></span>

```typescript
function flushAllD3Transitions(): void;
```

<span data-ttu-id="f067c-139">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-139">Example:</span></span>

```typescript
import { manipulation } from "powerbi-visuals-utils-svgutils";
// ...

manipulation.flushAllD3Transitions();

// forces every transition of D3 to complete
```

### <a name="parsetranslatetransform"></a><span data-ttu-id="f067c-140">parseTranslateTransform</span><span class="sxs-lookup"><span data-stu-id="f067c-140">parseTranslateTransform</span></span>

<span data-ttu-id="f067c-141">ฟังก์ชันนี้แยกวิเคราะห์สตริงด้วยค่า "translate(x,y)"</span><span class="sxs-lookup"><span data-stu-id="f067c-141">This function parses the transform string with value "translate(x,y)".</span></span>

```typescript
function parseTranslateTransform(input: string): { x: string; y: string };
```

<span data-ttu-id="f067c-142">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-142">Example:</span></span>

```typescript
import { manipulation } from "powerbi-visuals-utils-svgutils";
// ...

manipulation.parseTranslateTransform("translate(100px,100px)");

// returns: { "x":"100px", "y":"100px" }
```

### <a name="createarrow"></a><span data-ttu-id="f067c-143">createArrow</span><span class="sxs-lookup"><span data-stu-id="f067c-143">createArrow</span></span>

<span data-ttu-id="f067c-144">ฟังก์ชันนี้สร้างลูกศร</span><span class="sxs-lookup"><span data-stu-id="f067c-144">This function creates an arrow.</span></span>

```typescript
function createArrow(
  width: number,
  height: number,
  rotate: number
): { path: string; transform: string };
```

<span data-ttu-id="f067c-145">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-145">Example:</span></span>

```typescript
import { manipulation } from "powerbi-visuals-utils-svgutils";
// ...

manipulation.createArrow(10, 20, 5);

/* returns: {
    "path": "M0 0L0 20L10 10 Z",
    "transform": "rotate(5 5 10)"
}*/
```

## <a name="rect"></a><span data-ttu-id="f067c-146">Rect</span><span class="sxs-lookup"><span data-stu-id="f067c-146">Rect</span></span>

<span data-ttu-id="f067c-147">โมดูล `Rect` มีฟังก์ชันพิเศษบางอย่างในการจัดการสี่เหลี่ยมผืนผ้า</span><span class="sxs-lookup"><span data-stu-id="f067c-147">The `Rect` module provides some special functions to manipulate rectangles.</span></span>

<span data-ttu-id="f067c-148">โมดูลมอบฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f067c-148">The module provides the following functions:</span></span>

### <a name="getoffset"></a><span data-ttu-id="f067c-149">getOffset</span><span class="sxs-lookup"><span data-stu-id="f067c-149">getOffset</span></span>

<span data-ttu-id="f067c-150">ฟังก์ชันนี้คืนค่าออฟเซตของสี่เหลี่ยมผืนผ้า</span><span class="sxs-lookup"><span data-stu-id="f067c-150">This function returns an offset of the rectangle.</span></span>

```typescript
function getOffset(rect: IRect): IPoint;
```

<span data-ttu-id="f067c-151">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-151">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.getOffset({ left: 25, top: 25, width: 100, height: 100 });

/* returns: {
    x: 25,
    y: 25
}*/
```

### <a name="getsize"></a><span data-ttu-id="f067c-152">getSize</span><span class="sxs-lookup"><span data-stu-id="f067c-152">getSize</span></span>

<span data-ttu-id="f067c-153">ฟังก์ชันนี้คืนค่าขนาดของสี่เหลี่ยมผืนผ้า</span><span class="sxs-lookup"><span data-stu-id="f067c-153">This function returns size of the rectangle.</span></span>

```typescript
function getSize(rect: IRect): ISize;
```

<span data-ttu-id="f067c-154">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-154">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.getSize({ left: 25, top: 25, width: 100, height: 100 });

/* returns: {
    width: 100,
    height: 100
}*/
```

### <a name="setsize"></a><span data-ttu-id="f067c-155">setSize</span><span class="sxs-lookup"><span data-stu-id="f067c-155">setSize</span></span>

<span data-ttu-id="f067c-156">ฟังก์ชันนี้เปลี่ยนขนาดสี่เหลี่ยมผืนผ้า</span><span class="sxs-lookup"><span data-stu-id="f067c-156">This function modifies size of the rectangle.</span></span>

```typescript
function setSize(rect: IRect, value: ISize): void;
```

<span data-ttu-id="f067c-157">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-157">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

let rectangle = { left: 25, top: 25, width: 100, height: 100 };

Rect.setSize(rectangle, { width: 250, height: 250 });

// rectangle === { left: 25, top: 25, width: 250, height: 250 }
```

### <a name="right"></a><span data-ttu-id="f067c-158">ขวา</span><span class="sxs-lookup"><span data-stu-id="f067c-158">right</span></span>

<span data-ttu-id="f067c-159">ฟังก์ชันนี้คืนค่าตำแหน่งขวาของสี่เหลี่ยมผืนผ้า</span><span class="sxs-lookup"><span data-stu-id="f067c-159">This function returns a right position of the rectangle.</span></span>

```typescript
function right(rect: IRect): number;
```

<span data-ttu-id="f067c-160">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-160">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.right({ left: 25, top: 25, width: 100, height: 100 });

// returns: 125
```

### <a name="bottom"></a><span data-ttu-id="f067c-161">ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="f067c-161">bottom</span></span>

<span data-ttu-id="f067c-162">ฟังก์ชันนี้คืนค่าตำแหน่งล่างของสี่เหลี่ยมผืนผ้า</span><span class="sxs-lookup"><span data-stu-id="f067c-162">This function returns a bottom position of the rectangle.</span></span>

```typescript
function bottom(rect: IRect): number;
```

<span data-ttu-id="f067c-163">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-163">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.bottom({ left: 25, top: 25, width: 100, height: 100 });

// returns: 125
```

### <a name="topleft"></a><span data-ttu-id="f067c-164">topLeft</span><span class="sxs-lookup"><span data-stu-id="f067c-164">topLeft</span></span>

<span data-ttu-id="f067c-165">ฟังก์ชันนี้คืนค่าตำแหน่งมุมบนซ้ายของสี่เหลี่ยมผืนผ้า</span><span class="sxs-lookup"><span data-stu-id="f067c-165">This function returns a top-left position of the rectangle.</span></span>

```typescript
function topLeft(rect: IRect): IPoint;
```

<span data-ttu-id="f067c-166">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-166">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.topLeft({ left: 25, top: 25, width: 100, height: 100 });

// returns: { x: 25, y: 25 }
```

### <a name="topright"></a><span data-ttu-id="f067c-167">topRight</span><span class="sxs-lookup"><span data-stu-id="f067c-167">topRight</span></span>

<span data-ttu-id="f067c-168">ฟังก์ชันนี้คืนค่าตำแหน่งมุมบนขวาของสี่เหลี่ยมผืนผ้า</span><span class="sxs-lookup"><span data-stu-id="f067c-168">This function returns a top-right position of the rectangle.</span></span>

```typescript
function topRight(rect: IRect): IPoint;
```

<span data-ttu-id="f067c-169">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-169">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.topRight({ left: 25, top: 25, width: 100, height: 100 });

// returns: { x: 125, y: 25 }
```

### <a name="bottomleft"></a><span data-ttu-id="f067c-170">bottomLeft</span><span class="sxs-lookup"><span data-stu-id="f067c-170">bottomLeft</span></span>

<span data-ttu-id="f067c-171">ฟังก์ชันนี้คืนค่าตำแหน่งล่างของสี่เหลี่ยมผืนผ้า</span><span class="sxs-lookup"><span data-stu-id="f067c-171">This function returns a bottom-left position of the rectangle.</span></span>

```typescript
function bottomLeft(rect: IRect): IPoint;
```

<span data-ttu-id="f067c-172">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-172">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.bottomLeft({ left: 25, top: 25, width: 100, height: 100 });

// returns: { x: 25, y: 125 }
```

### <a name="bottomright"></a><span data-ttu-id="f067c-173">bottomRight</span><span class="sxs-lookup"><span data-stu-id="f067c-173">bottomRight</span></span>

<span data-ttu-id="f067c-174">ฟังก์ชันนี้คืนค่าตำแหน่งล่างขวาของสี่เหลี่ยมผืนผ้า</span><span class="sxs-lookup"><span data-stu-id="f067c-174">This function returns a bottom-right position of the rectangle.</span></span>

```typescript
function bottomRight(rect: IRect): IPoint;
```

### <a name="example"></a><span data-ttu-id="f067c-175">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f067c-175">Example</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.bottomRight({ left: 25, top: 25, width: 100, height: 100 });

// returns: { x: 125, y: 125 }
```

### <a name="clone"></a><span data-ttu-id="f067c-176">โคลน</span><span class="sxs-lookup"><span data-stu-id="f067c-176">clone</span></span>

<span data-ttu-id="f067c-177">ฟังก์ชันนี้สร้างสำเนาของสี่เหลี่ยมผืนผ้า</span><span class="sxs-lookup"><span data-stu-id="f067c-177">This function creates a copy of the rectangle.</span></span>

```typescript
function clone(rect: IRect): IRect;
```

<span data-ttu-id="f067c-178">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-178">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.clone({ left: 25, top: 25, width: 100, height: 100 });

/* returns: {
    left: 25, top: 25, width: 100, height: 100}
*/
```

### <a name="tostring"></a><span data-ttu-id="f067c-179">toString</span><span class="sxs-lookup"><span data-stu-id="f067c-179">toString</span></span>

<span data-ttu-id="f067c-180">ฟังก์ชันนี้แปลงสี่เหลี่ยมผืนผ้าเป็นสตริง</span><span class="sxs-lookup"><span data-stu-id="f067c-180">This function converts rectangle to string.</span></span>

```typescript
function toString(rect: IRect): string;
```

<span data-ttu-id="f067c-181">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-181">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.toString({ left: 25, top: 25, width: 100, height: 100 });

// returns: {left:25, top:25, width:100, height:100}
```

### <a name="offset"></a><span data-ttu-id="f067c-182">ออฟเซต</span><span class="sxs-lookup"><span data-stu-id="f067c-182">offset</span></span>

<span data-ttu-id="f067c-183">ฟังกันนี้ใช้ค่าออฟเซตที่กำหนดกับสี่เหลี่ยมผืนผ้า</span><span class="sxs-lookup"><span data-stu-id="f067c-183">This function applies given offset to the rectangle.</span></span>

```typescript
function offset(rect: IRect, offsetX: number, offsetY: number): IRect;
```

<span data-ttu-id="f067c-184">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-184">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.offset({ left: 25, top: 25, width: 100, height: 100 }, 50, 50);

/* returns: {
    left: 75,
    top: 75,
    width: 100,
    height: 100
}*/
```

### <a name="add"></a><span data-ttu-id="f067c-185">เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="f067c-185">add</span></span>

<span data-ttu-id="f067c-186">ฟังก์ชันนี้เพิ่มสี่เหลี่ยมผืนผ้าแรกลงในสี่เหลี่ยมที่สอง</span><span class="sxs-lookup"><span data-stu-id="f067c-186">This function adds the first rectangle to the second rectangle.</span></span>

```typescript
function add(rect: IRect, rect2: IRect): IRect;
```

<span data-ttu-id="f067c-187">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-187">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.add(
  { left: 25, top: 25, width: 100, height: 100 },
  { left: 50, top: 50, width: 75, height: 75 }
);

/* returns: {
    left: 75,
    top: 75,
    height: 175,
    width: 175
}*/
```

### <a name="getclosestpoint"></a><span data-ttu-id="f067c-188">getClosestPoint</span><span class="sxs-lookup"><span data-stu-id="f067c-188">getClosestPoint</span></span>

<span data-ttu-id="f067c-189">ฟังก์ชันนี้คืนค่าจุดใกล้สุดบนสามเหลี่ยมกับจุดที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="f067c-189">This function returns the closest point on the rect to the given point.</span></span>

```typescript
function getClosestPoint(rect: IRect, x: number, y: number): IPoint;
```

<span data-ttu-id="f067c-190">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-190">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.getClosestPoint({ left: 0, top: 0, width: 100, height: 100 }, 50, 50);

/* returns: {
    x: 50,
    y: 50
}*/
```

### <a name="equal"></a><span data-ttu-id="f067c-191">เท่ากับ</span><span class="sxs-lookup"><span data-stu-id="f067c-191">equal</span></span>

<span data-ttu-id="f067c-192">ฟังก์ชันนี้เปรียบเทียบสี่เหลี่ยมและคืนค่า True หากสี่เหลี่ยมนั้นเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="f067c-192">This function compares rectangles and returns true if they're the same.</span></span>

```typescript
function equal(rect1: IRect, rect2: IRect): boolean;
```

<span data-ttu-id="f067c-193">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-193">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.equal(
  { left: 0, top: 0, width: 100, height: 100 },
  { left: 50, top: 50, width: 100, height: 100 }
);

// returns: false
```

### <a name="equalwithprecision"></a><span data-ttu-id="f067c-194">equalWithPrecision</span><span class="sxs-lookup"><span data-stu-id="f067c-194">equalWithPrecision</span></span>

<span data-ttu-id="f067c-195">ฟังก์ชันนี้เปรียบเทียบโดยพิจารณาความแม่นยำของค่า</span><span class="sxs-lookup"><span data-stu-id="f067c-195">This function compares rectangles by considering precision of the values.</span></span>

```typescript
function equalWithPrecision(rect1: IRect, rect2: IRect): boolean;
```

<span data-ttu-id="f067c-196">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-196">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.equalWithPrecision(
  { left: 0, top: 0, width: 100, height: 100 },
  { left: 50, top: 50, width: 100, height: 100 }
);

// returns: false
```

### <a name="isempty"></a><span data-ttu-id="f067c-197">isEmpty</span><span class="sxs-lookup"><span data-stu-id="f067c-197">isEmpty</span></span>

<span data-ttu-id="f067c-198">ฟังก์ชันนี้ตรวจสอบว่าสี่เหลี่ยมนั้นว่างเปล่าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f067c-198">This function checks if rectangle is empty.</span></span>

```typescript
function isEmpty(rect: IRect): boolean;
```

<span data-ttu-id="f067c-199">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-199">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.isEmpty({ left: 0, top: 0, width: 0, height: 0 });

// returns: true
```

### <a name="containspoint"></a><span data-ttu-id="f067c-200">containsPoint</span><span class="sxs-lookup"><span data-stu-id="f067c-200">containsPoint</span></span>

<span data-ttu-id="f067c-201">ฟังก์ชั้นนี้ตรวจสอบว่าภายในสี่เหลี่ยมมีจุดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f067c-201">This function checks if rectangle contains the point.</span></span>

```typescript
function containsPoint(rect: IRect, point: IPoint): boolean;
```

<span data-ttu-id="f067c-202">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-202">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.containsPoint(
  { left: 0, top: 0, width: 100, height: 100 },
  { x: 50, y: 50 }
);

// returns: true
```

### <a name="isintersecting"></a><span data-ttu-id="f067c-203">isIntersecting</span><span class="sxs-lookup"><span data-stu-id="f067c-203">isIntersecting</span></span>

<span data-ttu-id="f067c-204">ฟังก์ชันนี้ตรวจสอบสี่เหลี่ยมซ้อนทับกันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f067c-204">This function checks if rectangles are intersecting.</span></span>

```typescript
function isIntersecting(rect1: IRect, rect2: IRect): boolean;
```

<span data-ttu-id="f067c-205">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-205">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.isIntersecting(
  { left: 0, top: 0, width: 100, height: 100 },
  { left: 0, top: 0, width: 50, height: 50 }
);

// returns: true
```

### <a name="intersect"></a><span data-ttu-id="f067c-206">intersect</span><span class="sxs-lookup"><span data-stu-id="f067c-206">intersect</span></span>

<span data-ttu-id="f067c-207">ฟังก์ชั้นนี้คืนค่าทับซ้อนของสี่เหลี่ยมผืนผ้า</span><span class="sxs-lookup"><span data-stu-id="f067c-207">This function returns an intersection of rectangles.</span></span>

```typescript
function intersect(rect1: IRect, rect2: IRect): IRect;
```

<span data-ttu-id="f067c-208">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-208">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.intersect(
  { left: 0, top: 0, width: 100, height: 100 },
  { left: 0, top: 0, width: 50, height: 50 }
);

/* returns: {
    left: 0,
    top: 0,
    width: 50,
    height: 50
}*/
```

### <a name="combine"></a><span data-ttu-id="f067c-209">รวม</span><span class="sxs-lookup"><span data-stu-id="f067c-209">combine</span></span>

<span data-ttu-id="f067c-210">ฟังก์ชันนี้รวมสี่เหลี่ยม</span><span class="sxs-lookup"><span data-stu-id="f067c-210">This function combines rectangles.</span></span>

```typescript
function combine(rect1: IRect, rect2: IRect): IRect;
```

<span data-ttu-id="f067c-211">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-211">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.combine(
  { left: 0, top: 0, width: 100, height: 100 },
  { left: 0, top: 0, width: 50, height: 120 }
);

/* returns: {
    left: 0,
    top: 0,
    width: 100,
    height: 120
}*/
```

### <a name="getcentroid"></a><span data-ttu-id="f067c-212">getCentroid</span><span class="sxs-lookup"><span data-stu-id="f067c-212">getCentroid</span></span>

<span data-ttu-id="f067c-213">ฟังก์ชันนี้คืนค่าออฟเซตของสี่เหลี่ยมผืนผ้า</span><span class="sxs-lookup"><span data-stu-id="f067c-213">This function returns a center point of the rectangle.</span></span>

```typescript
function getCentroid(rect: IRect): IPoint;
```

<span data-ttu-id="f067c-214">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-214">Example:</span></span>

```typescript
import { shapes } from "powerbi-visuals-utils-svgutils";
import Rect = shapes.Rect;
// ...

Rect.getCentroid({ left: 0, top: 0, width: 100, height: 100 });

/* returns: {
    x: 50,
    y: 50
}*/
```

## <a name="pointer"></a><span data-ttu-id="f067c-215">ตัวชี้</span><span class="sxs-lookup"><span data-stu-id="f067c-215">pointer</span></span>

<span data-ttu-id="f067c-216">โมดูล `pointer` มีฟังก์ชันเพื่อให้ได้ตำแหน่งของตัวชี้</span><span class="sxs-lookup"><span data-stu-id="f067c-216">The `pointer` module provides a special function to get position of the pointer.</span></span>

<span data-ttu-id="f067c-217">โมดูลมีฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f067c-217">The module provides the following function:</span></span>

### <a name="getcoordinates"></a><span data-ttu-id="f067c-218">getCoordinates</span><span class="sxs-lookup"><span data-stu-id="f067c-218">getCoordinates</span></span>

<span data-ttu-id="f067c-219">ฟังก์ชันนี้คืนค่าตำแหน่งของตัวชี้</span><span class="sxs-lookup"><span data-stu-id="f067c-219">This function returns position of the pointer.</span></span>

```typescript
function getCoordinates(rootNode: Element, isPointerEvent: boolean): number[];
```

<span data-ttu-id="f067c-220">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="f067c-220">Example:</span></span>

```typescript
import { pointer } from "powerbi-visuals-utils-svgutils";

let bodySelection = d3.select("body");

bodySelection
  .append("div")
  .style({
    width: "100px",
    height: "100px",
    "background-color": "green"
  })
  .on("click", () => {
    pointer.getCoordinates(bodySelection.node(), true);
  });

// click element, after that you will get position of the pointer
```
