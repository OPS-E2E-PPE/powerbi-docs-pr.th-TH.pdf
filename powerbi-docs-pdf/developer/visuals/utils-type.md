---
title: บทนำสู่การใช้งานยูทิลิตี้ชนิดของวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการใช้ยูทิลิตี SVG เพื่อขยายชนิดพื้นฐานสำหรับวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
manager: rkarlin
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: reference
ms.date: 06/18/2019
ms.openlocfilehash: 4f81f55f8d5cfc54020b3b4e02e8be55fb65b0d1
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888132"
---
# <a name="type-utils"></a><span data-ttu-id="6e8a9-104">ยูทิลิตี้ชนิด</span><span class="sxs-lookup"><span data-stu-id="6e8a9-104">Type utils</span></span>

<span data-ttu-id="6e8a9-105">TypeUtils คือชุดของฟังก์ชันและคลาสเพื่อขยายชนิดพื้นฐานสำหรับการแสดงผลด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="6e8a9-105">TypeUtils is a set of functions and classes to extend the basic types for Power BI visuals.</span></span>

## <a name="installation"></a><span data-ttu-id="6e8a9-106">การติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="6e8a9-106">Installation</span></span>

<span data-ttu-id="6e8a9-107">หากต้องการติดตั้งแพ็คเกจ คุณควรเรียกใช้คำสั่งต่อไปนี้ในไดเรกทอรีด้วยวิชวลของแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="6e8a9-107">To install the package, you should run the following command in the directory with your current custom visual:</span></span>

<span data-ttu-id="6e8a9-108">npm ติดตั้ง powerbi-visuals-utils-typeutils --บันทึก คำสั่งนี้ติดตั้งแพคเกจและเพิ่มแพคเกจ โดยขึ้นอยู่กับแพคเกจ json ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6e8a9-108">npm install powerbi-visuals-utils-typeutils --save This command installs the package and adds a package as a dependency to your package.json</span></span>

## <a name="double"></a><span data-ttu-id="6e8a9-109">สองครั้ง</span><span class="sxs-lookup"><span data-stu-id="6e8a9-109">Double</span></span>

<span data-ttu-id="6e8a9-110">`Double` มีความสามารถในการจัดการความแม่นยำของตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6e8a9-110">The `Double` provides abilities to manipulate precision of the numbers.</span></span>

<span data-ttu-id="6e8a9-111">โมดูลมอบฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-111">The module provides the following functions:</span></span>

### <a name="pow10"></a><span data-ttu-id="6e8a9-112">pow10</span><span class="sxs-lookup"><span data-stu-id="6e8a9-112">pow10</span></span>

<span data-ttu-id="6e8a9-113">ฟังก์ชันคืนค่ายกกำลัง 10 </span><span class="sxs-lookup"><span data-stu-id="6e8a9-113">This function returns power of 10.</span></span>

```typescript
function pow10(exp: number): number;
```

<span data-ttu-id="6e8a9-114">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-114">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.pow10(25);

// returns: 1e+25
```

### <a name="log10"></a><span data-ttu-id="6e8a9-115">log10</span><span class="sxs-lookup"><span data-stu-id="6e8a9-115">log10</span></span>

<span data-ttu-id="6e8a9-116">ฟังก์ชันนี้คืนค่าลอการิทึมฐาน 10 ของตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6e8a9-116">This function returns a 10 base logarithm of the number.</span></span>

```typescript
function log10(val: number): number;
```

<span data-ttu-id="6e8a9-117">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-117">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.log10(25);

// returns: 1
```

## <a name="getprecision"></a><span data-ttu-id="6e8a9-118">getPrecision</span><span class="sxs-lookup"><span data-stu-id="6e8a9-118">getPrecision</span></span>

<span data-ttu-id="6e8a9-119">ฟังก์ชันนี้คืนค่ายกกำลัง 10 แทนคงามแม่นยำของตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6e8a9-119">This function returns a power of 10 representing precision of the number.</span></span>

```typescript
function getPrecision(x: number, decimalDigits?: number): number;
```

<span data-ttu-id="6e8a9-120">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-120">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.getPrecision(562344, 6);

// returns: 0.1
```

### <a name="equalwithprecision"></a><span data-ttu-id="6e8a9-121">equalWithPrecision</span><span class="sxs-lookup"><span data-stu-id="6e8a9-121">equalWithPrecision</span></span>

<span data-ttu-id="6e8a9-122">ฟังก์ชันนี้ตรวจสอบว่าความแตกต่างของสองตัวเลขน้อยกว่าความแม่นยำที่กำหนดไว้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6e8a9-122">This function checks if a delta between two numbers is less than provided precision.</span></span>

```typescript
function equalWithPrecision(x: number, y: number, precision?: number): boolean;
```

<span data-ttu-id="6e8a9-123">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-123">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.equalWithPrecision(1, 1.005, 0.01);

// returns: true
```

### <a name="lesswithprecision"></a><span data-ttu-id="6e8a9-124">lessWithPrecision</span><span class="sxs-lookup"><span data-stu-id="6e8a9-124">lessWithPrecision</span></span>

<span data-ttu-id="6e8a9-125">ฟังก์ชันนี้ตรวจสอบว่าค่าแรกน้อยกว่าค่าที่สองหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6e8a9-125">This function checks if the first value is less than the second value.</span></span>

```typescript
function lessWithPrecision(x: number, y: number, precision?: number): boolean;
```

<span data-ttu-id="6e8a9-126">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-126">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.lessWithPrecision(0.995, 1, 0.001);

// returns: true
```

### <a name="lessorequalwithprecision"></a><span data-ttu-id="6e8a9-127">lessOrEqualWithPrecision</span><span class="sxs-lookup"><span data-stu-id="6e8a9-127">lessOrEqualWithPrecision</span></span>

<span data-ttu-id="6e8a9-128">ฟังก์ชันนี้ตรวจสอบว่าค่าแรกน้อยกว่าหรือเท่ากับค่าที่สองหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6e8a9-128">This function checks if the first value is less or equal than the second value.</span></span>

```typescript
function lessOrEqualWithPrecision(x: number, y: number, precision?: number): boolean;
```

<span data-ttu-id="6e8a9-129">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-129">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.lessOrEqualWithPrecision(1.005, 1, 0.01);

// returns: true
```

### <a name="greaterwithprecision"></a><span data-ttu-id="6e8a9-130">greaterWithPrecision</span><span class="sxs-lookup"><span data-stu-id="6e8a9-130">greaterWithPrecision</span></span>

<span data-ttu-id="6e8a9-131">ฟังก์ชันนี้ตรวจสอบว่าค่าแรกมากกว่าค่าที่สองหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6e8a9-131">This function checks if the first value it greater than the second value.</span></span>

```typescript
function greaterWithPrecision(x: number, y: number, precision?: number): boolean;
```

<span data-ttu-id="6e8a9-132">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-132">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.greaterWithPrecision(1, 0.995, 0.01);

// returns: false
```

### <a name="greaterorequalwithprecision"></a><span data-ttu-id="6e8a9-133">greaterOrEqualWithPrecision</span><span class="sxs-lookup"><span data-stu-id="6e8a9-133">greaterOrEqualWithPrecision</span></span>

<span data-ttu-id="6e8a9-134">ฟังก์ชันนี้ตรวจสอบว่าค่าแรกมากกว่าหรือเท่ากับค่าที่สองหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6e8a9-134">This function checks if the first value is greater or equal to the second value.</span></span>

```typescript
function greaterOrEqualWithPrecision(x: number, y: number, precision?: number): boolean;
```

<span data-ttu-id="6e8a9-135">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-135">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.greaterOrEqualWithPrecision(1, 1.005, 0.01);

// returns: true
```

### <a name="floorwithprecision"></a><span data-ttu-id="6e8a9-136">floorWithPrecision</span><span class="sxs-lookup"><span data-stu-id="6e8a9-136">floorWithPrecision</span></span>

<span data-ttu-id="6e8a9-137">ฟังก์ชันนี้ปรับตัวเลขลงด้วยความแม่นยำที่ให้มา</span><span class="sxs-lookup"><span data-stu-id="6e8a9-137">This function floors the number with the provided precision.</span></span>

```typescript
function floorWithPrecision(x: number, precision?: number): number;
```

<span data-ttu-id="6e8a9-138">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-138">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.floorWithPrecision(5.96, 0.001);

// returns: 5
```

### <a name="ceilwithprecision"></a><span data-ttu-id="6e8a9-139">ceilWithPrecision</span><span class="sxs-lookup"><span data-stu-id="6e8a9-139">ceilWithPrecision</span></span>

<span data-ttu-id="6e8a9-140">ฟังก์ชันนี้ `ceils` ตัวเลขด้วยความแม่นยำที่ให้มา</span><span class="sxs-lookup"><span data-stu-id="6e8a9-140">This function `ceils` the number with the provided precision.</span></span>

```typescript
function ceilWithPrecision(x: number, precision?: number): number;
```

<span data-ttu-id="6e8a9-141">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-141">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.ceilWithPrecision(5.06, 0.001);

// returns: 6
```

### <a name="floortoprecision"></a><span data-ttu-id="6e8a9-142">floorToPrecision</span><span class="sxs-lookup"><span data-stu-id="6e8a9-142">floorToPrecision</span></span>

<span data-ttu-id="6e8a9-143">ฟังก์ชันนี้ปรับตัวเลขลงไปที่ความแม่นยำที่ให้มา</span><span class="sxs-lookup"><span data-stu-id="6e8a9-143">This function floors the number to the provided precision.</span></span>

```typescript
function floorToPrecision(x: number, precision?: number): number;
```

<span data-ttu-id="6e8a9-144">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-144">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.floorToPrecision(5.96, 0.1);

// returns: 5.9
```

### <a name="ceiltoprecision"></a><span data-ttu-id="6e8a9-145">ceilToPrecision</span><span class="sxs-lookup"><span data-stu-id="6e8a9-145">ceilToPrecision</span></span>

<span data-ttu-id="6e8a9-146">ฟังก์ชันนี้ `ceils` ตัวเลขไปที่ความแม่นยำที่ให้มา</span><span class="sxs-lookup"><span data-stu-id="6e8a9-146">This function `ceils` the number to the provided precision.</span></span>

```typescript
function ceilToPrecision(x: number, precision?: number): number;
```

<span data-ttu-id="6e8a9-147">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-147">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.ceilToPrecision(-506, 10);

// returns: -500
```

### <a name="roundtoprecision"></a><span data-ttu-id="6e8a9-148">roundToPrecision</span><span class="sxs-lookup"><span data-stu-id="6e8a9-148">roundToPrecision</span></span>

<span data-ttu-id="6e8a9-149">ฟังก์ชั้นนี้ปัดเศษตัวเลขให้ตรงกับความแม่นยำที่ให้มา</span><span class="sxs-lookup"><span data-stu-id="6e8a9-149">This function rounds the number to the provided precision.</span></span>

```typescript
function roundToPrecision(x: number, precision?: number): number;
```

<span data-ttu-id="6e8a9-150">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-150">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.roundToPrecision(596, 10);

// returns: 600
```

### <a name="ensureinrange"></a><span data-ttu-id="6e8a9-151">ensureInRange</span><span class="sxs-lookup"><span data-stu-id="6e8a9-151">ensureInRange</span></span>

<span data-ttu-id="6e8a9-152">ฟังก์ชันนี้คืนค่าตัวเลขที่อยู่ระหว่างค่าต่ำสุดและค่าสูงสุด</span><span class="sxs-lookup"><span data-stu-id="6e8a9-152">This function returns a number that is between min and max.</span></span>

```typescript
function ensureInRange(x: number, min: number, max: number): number;
```

<span data-ttu-id="6e8a9-153">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-153">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.ensureInRange(-27.2, -10, -5);

// returns: -10
```

### <a name="round"></a><span data-ttu-id="6e8a9-154">round</span><span class="sxs-lookup"><span data-stu-id="6e8a9-154">round</span></span>

<span data-ttu-id="6e8a9-155">ฟังก์ชันนี้ปัดเศษตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6e8a9-155">This function rounds the number.</span></span>

```typescript
function round(x: number): number;
```

<span data-ttu-id="6e8a9-156">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-156">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.round(27.45);

// returns: 27
```

### <a name="removedecimalnoise"></a><span data-ttu-id="6e8a9-157">removeDecimalNoise</span><span class="sxs-lookup"><span data-stu-id="6e8a9-157">removeDecimalNoise</span></span>

<span data-ttu-id="6e8a9-158">ฟังก์ชันนี้นำค่าทศนิยมออก</span><span class="sxs-lookup"><span data-stu-id="6e8a9-158">This function removes the decimal noise.</span></span>

```typescript
function removeDecimalNoise(value: number): number;
```

<span data-ttu-id="6e8a9-159">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-159">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.removeDecimalNoise(21.493000000000002);

// returns: 21.493
```

### <a name="isinteger"></a><span data-ttu-id="6e8a9-160">isInteger</span><span class="sxs-lookup"><span data-stu-id="6e8a9-160">isInteger</span></span>

<span data-ttu-id="6e8a9-161">ฟังก์ชันนี้ตรวจสอบว่าตัวเลขเป็นจำนวนจริงหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6e8a9-161">This function checks if the number is integer.</span></span>

```typescript
function isInteger(value: number): boolean;
```

<span data-ttu-id="6e8a9-162">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-162">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.isInteger(21.493000000000002);

// returns: false
```

### <a name="toincrement"></a><span data-ttu-id="6e8a9-163">toIncrement</span><span class="sxs-lookup"><span data-stu-id="6e8a9-163">toIncrement</span></span>

<span data-ttu-id="6e8a9-164">ฟังก์ชันนี้เพิ่มตัวเลขตามจำนวนที่กำหนดและคืนค่าตัวเลขที่ปัดเศษแล้ว</span><span class="sxs-lookup"><span data-stu-id="6e8a9-164">This function increments the number by the provided number and returns the rounded number.</span></span>

```typescript
function toIncrement(value: number, increment: number): number;
```

<span data-ttu-id="6e8a9-165">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-165">Example:</span></span>

```typescript
import { double } from "powerbi-visuals-utils-typeutils";
// ...

double.toIncrement(0.6383723, 0.05);

// returns: 0.65
```

## <a name="prototype"></a><span data-ttu-id="6e8a9-166">Prototype</span><span class="sxs-lookup"><span data-stu-id="6e8a9-166">Prototype</span></span>

<span data-ttu-id="6e8a9-167">`Prototype` มีความสามารถในการโอนถ่ายวัตถุ</span><span class="sxs-lookup"><span data-stu-id="6e8a9-167">The `Prototype` provides abilities to inherit objects.</span></span>

<span data-ttu-id="6e8a9-168">โมดูลมอบฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-168">The module provides the following functions:</span></span>

## <a name="inherit"></a><span data-ttu-id="6e8a9-169">inherit</span><span class="sxs-lookup"><span data-stu-id="6e8a9-169">inherit</span></span>

<span data-ttu-id="6e8a9-170">ฟังก์ชันนี้คืนค่าวัตถุพร้อมกับวัตถุที่กำหนดให้เป็นโปโตคอล</span><span class="sxs-lookup"><span data-stu-id="6e8a9-170">This function returns a new object with the provided object as its prototype.</span></span>

```typescript
function inherit<T>(obj: T, extension?: (inherited: T) => void): T;
```

<span data-ttu-id="6e8a9-171">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-171">Example:</span></span>

```typescript
import { prototype } from "powerbi-visuals-utils-typeutils";
// ...

let base = { Microsoft: "Power BI" };

prototype.inherit(base);

/* returns: {
    __proto__: {
        Microsoft: "Power BI"
    }
}*/
```

## <a name="inheritsingle"></a><span data-ttu-id="6e8a9-172">inheritSingle</span><span class="sxs-lookup"><span data-stu-id="6e8a9-172">inheritSingle</span></span>

<span data-ttu-id="6e8a9-173">ฟังก์ชันนี้คืนค่าวัตถุใหม่พร้อมกับวัตถุที่กำหนดให้เป็นโปรโตคอล หากไม่ได้กำหนดโปรโตคอลเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6e8a9-173">This function returns a new object with the provided object as its prototype if, and only if, the prototype hasn't been set.</span></span>

```typescript
function inheritSingle<T>(obj: T): T;
```

<span data-ttu-id="6e8a9-174">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-174">Example:</span></span>

```typescript
import { prototype } from "powerbi-visuals-utils-typeutils";
// ...

let base = { Microsoft: "Power BI" };

prototype.inheritSingle(base);

/* returns: {
    __proto__: {
        Microsoft: "Power BI"
    }
}*/
```

## <a name="pixelconverter"></a><span data-ttu-id="6e8a9-175">PixelConverter</span><span class="sxs-lookup"><span data-stu-id="6e8a9-175">PixelConverter</span></span>

<span data-ttu-id="6e8a9-176">`PixelConverter` มีความสามารถในการเปลี่ยนพิกเซลเป็นจุด และจุดเป็นพิกเซล</span><span class="sxs-lookup"><span data-stu-id="6e8a9-176">The `PixelConverter` provides an ability to convert pixels to points, and points to pixels.</span></span>

<span data-ttu-id="6e8a9-177">โมดูลมอบฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-177">The module provides the following functions:</span></span>

## <a name="tostring"></a><span data-ttu-id="6e8a9-178">toString</span><span class="sxs-lookup"><span data-stu-id="6e8a9-178">toString</span></span>

<span data-ttu-id="6e8a9-179">ฟังก์ชันนี้แปลงค่าพิกเซลเป็นสตริง</span><span class="sxs-lookup"><span data-stu-id="6e8a9-179">This function converts the pixel value to a string.</span></span>

```typescript
function toString(px: number): string;
```

<span data-ttu-id="6e8a9-180">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-180">Example:</span></span>

```typescript
import { pixelConverter } from "powerbi-visuals-utils-typeutils";
// ...

pixelConverter.toString(25);

// returns: 25px
```

## <a name="frompoint"></a><span data-ttu-id="6e8a9-181">fromPoint</span><span class="sxs-lookup"><span data-stu-id="6e8a9-181">fromPoint</span></span>

<span data-ttu-id="6e8a9-182">ฟังก์ชันนี้แปลงค่าจุดที่กำหนดให้เป็นค่าพิกเซลและคืนค่าการแปลเป็นสตริง</span><span class="sxs-lookup"><span data-stu-id="6e8a9-182">This function converts the provided point value to the pixel value and returns the string interpretation.</span></span>

```typescript
function fromPoint(pt: number): string;
```

<span data-ttu-id="6e8a9-183">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-183">Example:</span></span>

```typescript
import { pixelConverter } from "powerbi-visuals-utils-typeutils";
// ...

pixelConverter.fromPoint(8);

// returns: 33.33333333333333px
```

## <a name="frompointtopixel"></a><span data-ttu-id="6e8a9-184">fromPointToPixel</span><span class="sxs-lookup"><span data-stu-id="6e8a9-184">fromPointToPixel</span></span>

<span data-ttu-id="6e8a9-185">ฟังก์ชันนี้แปลงค่าจุดเป็นค่าพิกเซล</span><span class="sxs-lookup"><span data-stu-id="6e8a9-185">This function converts the provided point value to the pixel value.</span></span>

```typescript
function fromPointToPixel(pt: number): number;
```

<span data-ttu-id="6e8a9-186">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-186">Example:</span></span>

```typescript
import { pixelConverter } from "powerbi-visuals-utils-typeutils";
// ...

pixelConverter.fromPointToPixel(8);

// returns: 10.666666666666666
```

## <a name="topoint"></a><span data-ttu-id="6e8a9-187">toPoint</span><span class="sxs-lookup"><span data-stu-id="6e8a9-187">toPoint</span></span>

<span data-ttu-id="6e8a9-188">ฟังก์ชันนี้แปลงค่าพิกเซลเป็นค่าจุด</span><span class="sxs-lookup"><span data-stu-id="6e8a9-188">This function converts the pixel value to the point value.</span></span>

```typescript
function toPoint(px: number): number;
```

<span data-ttu-id="6e8a9-189">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="6e8a9-189">Example:</span></span>

```typescript
import { pixelConverter } from "powerbi-visuals-utils-typeutils";
// ...

pixelConverter.toPoint(8);

// returns: 6
```
