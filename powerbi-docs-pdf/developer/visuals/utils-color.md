---
title: บทนำสู่การใช้งานยูทิลิตี้สีของวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการใช้ยูทิลิตี้สี ทำให้ง่ายต่อการใช้ชุดรูปแบบและจานสีบนจุดข้อมูลของการแสดงผลด้วยภาพของ Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: reference
ms.date: 02/14/2020
ms.openlocfilehash: cc75188d806d653766860b2fada9028477a75f71
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887856"
---
# <a name="color-utils"></a><span data-ttu-id="45dbe-104">ยูทิลิตี้สี</span><span class="sxs-lookup"><span data-stu-id="45dbe-104">Color utils</span></span>
<span data-ttu-id="45dbe-105">บทความนี้จะช่วยให้คุณสามารถติดตั้ง นำเข้า และใช้คำแนะนำเครื่องมือยูทิลิตี้สี</span><span class="sxs-lookup"><span data-stu-id="45dbe-105">This article will help you to install, import, and use color utils.</span></span> <span data-ttu-id="45dbe-106">บทความนี้อธิบายวิธีการใช้ยูทิลิตี้สี ทำให้ง่ายต่อการใช้ชุดรูปแบบและจานสีบนจุดข้อมูลของการแสดงผลด้วยภาพของ Power BI</span><span class="sxs-lookup"><span data-stu-id="45dbe-106">This article describes how to use color utils simplify applying of themes and palettes on visual's data points on Power BI visuals.</span></span>

## <a name="requirements"></a><span data-ttu-id="45dbe-107">ข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="45dbe-107">Requirements</span></span>
<span data-ttu-id="45dbe-108">หากต้องการใช้แพคเกจ คุณควรมีสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="45dbe-108">To use the package, you should have the following things:</span></span>
* <span data-ttu-id="45dbe-109">[node.js](https://nodejs.org) (เราขอแนะนำเวอร์ชัน LTS รุ่นล่าสุด)</span><span class="sxs-lookup"><span data-stu-id="45dbe-109">[node.js](https://nodejs.org) (we recommend the latest LTS version)</span></span>
* <span data-ttu-id="45dbe-110">[npm](https://www.npmjs.com/) (เวอร์ชันเก่าที่สุดที่ได้รับการรองรับคือ 3.0.0)</span><span class="sxs-lookup"><span data-stu-id="45dbe-110">[npm](https://www.npmjs.com/) (the minimal supported version is 3.0.0)</span></span>
* <span data-ttu-id="45dbe-111">การแสดงผลด้วยภาพแบบกำหนดเองที่สร้างขึ้นโดย [PowerBI-visuals-tools](https://www.npmjs.com/package/powerbi-visuals-tools)</span><span class="sxs-lookup"><span data-stu-id="45dbe-111">The custom visual created by [PowerBI-visuals-tools](https://www.npmjs.com/package/powerbi-visuals-tools)</span></span>

## <a name="installation"></a><span data-ttu-id="45dbe-112">การติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="45dbe-112">Installation</span></span>

<span data-ttu-id="45dbe-113">หากต้องการติดตั้งแพ็คเกจ คุณควรเรียกใช้คำสั่งต่อไปนี้ในไดเรกทอรีด้วยวิชวลปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="45dbe-113">To install the package, you should run the following command in the directory with your current visual:</span></span>

```bash
npm install powerbi-visuals-utils-colorutils --save
```
<span data-ttu-id="45dbe-114">คำสั่งนี้จะติดตั้งแพคเกจและเพิ่มแพคเกจเป็นการขึ้นต่อกันของคุณ ```package.json```</span><span class="sxs-lookup"><span data-stu-id="45dbe-114">This command installs the package and adds a package as a dependency to your ```package.json```</span></span>

## <a name="usage"></a><span data-ttu-id="45dbe-115">การใช้</span><span class="sxs-lookup"><span data-stu-id="45dbe-115">Usage</span></span>

<span data-ttu-id="45dbe-116">หากต้องการใช้ยูทิลิตี้การโต้ตอบ คุณต้องนำเข้าคอมโพเนนต์ที่จำเป็นในโค้ดต้นฉบับของวิชวล</span><span class="sxs-lookup"><span data-stu-id="45dbe-116">To user interactivity utils, you have to import the required component in the source code of the visual.</span></span>
```typescript
import { ColorHelper } from "powerbi-visuals-utils-colorutils";
```

<span data-ttu-id="45dbe-117">เรียนรู้วิธีการติดตั้งและใช้ ColorUtils ในวิชวล Power BI ของคุณ:</span><span class="sxs-lookup"><span data-stu-id="45dbe-117">Learn how to install and use the ColorUtils in your Power BI visuals:</span></span>

* <span data-ttu-id="45dbe-118">[คำแนะนำการใช้งาน] คำแนะนำการใช้งานนี้จะอธิบาย API สาธารณะของแพคเกจ</span><span class="sxs-lookup"><span data-stu-id="45dbe-118">[Usage Guide] The Usage Guide describes a public API of the package.</span></span> <span data-ttu-id="45dbe-119">คุณจะพบคำอธิบายและตัวอย่างสำหรับแต่ละอินเทอร์เฟซสาธารณะของแพคเกจ</span><span class="sxs-lookup"><span data-stu-id="45dbe-119">You will find a description and a few examples for each public interface of the package.</span></span>

<span data-ttu-id="45dbe-120">แพคเกจนี้ประกอบด้วยคลาสและโมดูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="45dbe-120">This package contains the following classes and modules:</span></span>
* <span data-ttu-id="45dbe-121">[ColorHelper](#colorhelper) - ช่วยในการสร้างสีที่มีความแตกต่างกันสำหรับค่าแผนภูมิของคุณ</span><span class="sxs-lookup"><span data-stu-id="45dbe-121">[ColorHelper](#colorhelper) - helps to generate different colors for your chart values</span></span>
* <span data-ttu-id="45dbe-122">[colorUtils](#colorutils) - ช่วยในการแปลงรูปแบบสีของ</span><span class="sxs-lookup"><span data-stu-id="45dbe-122">[colorUtils](#colorutils) - helps to convert color formats</span></span>

## `ColorHelper`
<span data-ttu-id="45dbe-123">คลาส `ColorHelper` มีฟังก์ชันและวิธีการดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="45dbe-123">The `ColorHelper` class provides the following functions and methods:</span></span>

### `getColorForSeriesValue` 
<span data-ttu-id="45dbe-124">วิธีนี้จะเป็นการได้สีสำหรับค่าชุดข้อมูลที่ระบุไว้</span><span class="sxs-lookup"><span data-stu-id="45dbe-124">This method gets the color for the given series value.</span></span> <span data-ttu-id="45dbe-125">ถ้าไม่มีสีที่ชัดเจนหรือสีเริ่มต้นที่ได้รับการตั้งค่าแล้ว จะมีการจัดสรรสี จากระดับสีสำหรับชุดข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="45dbe-125">If no explicit color or default color has been set, then the color is allocated from the color scale for this series.</span></span>
```typescript
getColorForSeriesValue(objects: IDataViewObjects, value: PrimitiveValue, themeColorName?: ThemeColorName): string;
```
#### <a name="example"></a><span data-ttu-id="45dbe-126">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="45dbe-126">Example</span></span>
```typescript
import powerbi from "powerbi-visuals-api";
import { ColorHelper } from "powerbi-visuals-utils-colorutils";

import DataViewObjects = powerbi.DataViewObjects;

import DataViewValueColumns = powerbi.DataViewValueColumns;
import DataViewValueColumnGroup = powerbi.DataViewValueColumnGroup;
import DataViewObjectPropertyIdentifier = powerbi.DataViewObjectPropertyIdentifier;

import IVisual = powerbi.extensibility.visual.IVisual;
import IColorPalette = powerbi.extensibility.IColorPalette;
import VisualUpdateOptions = powerbi.extensibility.visual.VisualUpdateOptions;
import VisualConstructorOptions = powerbi.extensibility.visual.VisualConstructorOptions;

export class YourVisual implements IVisual {
    // Implementation of IVisual

    private colorPalette: IColorPalette;

    constructor(options: VisualConstructorOptions) {
        this.colorPalette = options.host.colorPalette;
    }

    public update(visualUpdateOptions: VisualUpdateOptions): void {
        const valueColumns: DataViewValueColumns = visualUpdateOptions.dataViews[0].categorical.values,
            grouped: DataViewValueColumnGroup[] = valueColumns.grouped(),
            defaultDataPointColor: string = "green",
            fillProp: DataViewObjectPropertyIdentifier = {
                objectName: "objectName",
                propertyName: "propertyName"
            };

        let colorHelper: ColorHelper = new ColorHelper(
            this.colorPalette,
            fillProp,
            defaultDataPointColor);

        for (let i = 0; i < grouped.length; i++) {
            let grouping: DataViewValueColumnGroup = grouped[i];

            let color = colorHelper.getColorForSeriesValue(grouping.objects, grouping.name); // returns a color of the series
        }
    }
}
```

### `getColorForMeasure`
<span data-ttu-id="45dbe-127">วิธีนี้จะเป็นการรับสีสำหรับหน่วยวัดที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="45dbe-127">This method gets the color for the given measure.</span></span>
```typescript
 getColorForMeasure(objects: IDataViewObjects, measureKey: any, themeColorName?: ThemeColorName): string;
```
#### <a name="example"></a><span data-ttu-id="45dbe-128">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="45dbe-128">Example</span></span>
```typescript
import powerbi from "powerbi-visuals-api";
import { ColorHelper } from "powerbi-visuals-utils-colorutils";

import DataViewObjects = powerbi.DataViewObjects;
import IVisual = powerbi.extensibility.visual.IVisual;
import IColorPalette = powerbi.extensibility.IColorPalette;
import VisualUpdateOptions = powerbi.extensibility.visual.VisualUpdateOptions;
import DataViewObjectPropertyIdentifier = powerbi.DataViewObjectPropertyIdentifier;
import VisualConstructorOptions = powerbi.extensibility.visual.VisualConstructorOptions;

export class YourVisual implements IVisual {
    // Implementation of IVisual

    private colorPalette: IColorPalette;

    constructor(options: VisualConstructorOptions) {
        this.colorPalette = options.host.colorPalette;
    }

    public update(visualUpdateOptions: VisualUpdateOptions): void {
        const objects: DataViewObjects = visualUpdateOptions.dataViews[0].categorical.categories[0].objects[0],
            defaultDataPointColor: string = "green",
            fillProp: DataViewObjectPropertyIdentifier = {
                objectName: "objectName",
                propertyName: "propertyName"
            };

        let colorHelper: ColorHelper = new ColorHelper(
            this.colorPalette,
            fillProp,
            defaultDataPointColor);

        let color = colorHelper.getColorForMeasure(objects, ""); // returns a color
    }
}
```

### <a name="static-normalizeselector"></a><span data-ttu-id="45dbe-129">คงที่ `normalizeSelector`</span><span class="sxs-lookup"><span data-stu-id="45dbe-129">static `normalizeSelector`</span></span>
<span data-ttu-id="45dbe-130">วิธีการนี้จะส่งกลับตัวเลือกปกติ</span><span class="sxs-lookup"><span data-stu-id="45dbe-130">This method returns the normalized selector</span></span>
```typescript
static normalizeSelector(selector: Selector, isSingleSeries?: boolean): Selector;
```
#### <a name="example"></a><span data-ttu-id="45dbe-131">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="45dbe-131">Example</span></span>
```typescript
import ISelectionId = powerbi.visuals.ISelectionId;
import { ColorHelper } from "powerbi-visuals-utils-colorutils";

let selectionId: ISelectionId = ...;
let selector = ColorHelper.normalizeSelector(selectionId.getSelector(), false);
```

<span data-ttu-id="45dbe-132">วิธีการ`getThemeColor`และ`getHighContrastColor` ทั้งหมดที่เกี่ยวข้องกับสีธีมสีต่างๆ</span><span class="sxs-lookup"><span data-stu-id="45dbe-132">Methods `getThemeColor` and `getHighContrastColor` are both related to color theme colors.</span></span>
<span data-ttu-id="45dbe-133">นอกจากนี้`ColorHelper`และ`isHighContrast`ยังมีคุณสมบัติที่อาจมีประโยชน์สำหรับการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="45dbe-133">Also `ColorHelper` has `isHighContrast` property that should be useful for check.</span></span>

### `getThemeColor`
<span data-ttu-id="45dbe-134">วิธีการนี้จะส่งสีของธีมกลับมา</span><span class="sxs-lookup"><span data-stu-id="45dbe-134">This method returns theme color</span></span>
```typescript
 getThemeColor(themeColorName?: ThemeColorName): string;
```
### `getHighContrastColor`
 <span data-ttu-id="45dbe-135">วิธีการนี้จะส่งสีกลับมาสำหรับโหมดความคมชัดสูง</span><span class="sxs-lookup"><span data-stu-id="45dbe-135">This  method return color for high contrast mode</span></span>
```typescript
getHighContrastColor(themeColorName?: ThemeColorName, defaultColor?: string): string;
```
#### <a name="example-related-to-high-contrast-mode-usage"></a><span data-ttu-id="45dbe-136">ตัวอย่างที่เกี่ยวข้องกับการใช้โหมดความคมชัดสูง:</span><span class="sxs-lookup"><span data-stu-id="45dbe-136">Example related to high contrast mode usage:</span></span>
```typescript

import { ColorHelper } from "powerbi-visuals-utils-colorutils";

export class MyVisual implements IVisual {
        private colorHelper: ColorHelper;

        private init(options: VisualConstructorOptions): void {
            this.colors = options.host.colorPalette;
            this.colorHelper = new ColorHelper(this.colors);
        } 

            private createViewport(element: HTMLElement): void {
                const fontColor: string = "#131aea";
                const axisBackgroundColor: string = this.colorHelper.getThemeColor();
                
                // some d3 code before
                d3ElementName.attr("fill", colorHelper.getHighContrastColor("foreground", fontColor);
            }
                
            public static parseSettings(dataView: DataView, colorHelper: ColorHelper): VisualSettings {
                // some code that should be applied on formatting settings
                if (colorHelper.isHighContrast) {
                        this.settings.fontColor = colorHelper.getHighContrastColor("foreground", this.settings.fontColor);
                    }
            }
}
```


## `ColorUtils`
 <span data-ttu-id="45dbe-137">โมดูลมอบฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="45dbe-137">The module provides the following functions:</span></span>

* [<span data-ttu-id="45dbe-138">hexToRGBString</span><span class="sxs-lookup"><span data-stu-id="45dbe-138">hexToRGBString</span></span>](#hextorgbstring)
* [<span data-ttu-id="45dbe-139">หมุน</span><span class="sxs-lookup"><span data-stu-id="45dbe-139">rotate</span></span>](#rotate)
* [<span data-ttu-id="45dbe-140">parseColorString</span><span class="sxs-lookup"><span data-stu-id="45dbe-140">parseColorString</span></span>](#parsecolorstring)
* [<span data-ttu-id="45dbe-141">calculateHighlightColor</span><span class="sxs-lookup"><span data-stu-id="45dbe-141">calculateHighlightColor</span></span>](#calculatehighlightcolor)
* [<span data-ttu-id="45dbe-142">createLinearColorScale</span><span class="sxs-lookup"><span data-stu-id="45dbe-142">createLinearColorScale</span></span>](#createlinearcolorscale)
* [<span data-ttu-id="45dbe-143">shadeColor</span><span class="sxs-lookup"><span data-stu-id="45dbe-143">shadeColor</span></span>](#shadecolor)
* [<span data-ttu-id="45dbe-144">rgbBlend</span><span class="sxs-lookup"><span data-stu-id="45dbe-144">rgbBlend</span></span>](#rgbblend)
* [<span data-ttu-id="45dbe-145">channelBlend</span><span class="sxs-lookup"><span data-stu-id="45dbe-145">channelBlend</span></span>](#channelblend)
* [<span data-ttu-id="45dbe-146">hexBlend</span><span class="sxs-lookup"><span data-stu-id="45dbe-146">hexBlend</span></span>](#hexblend)

### <a name="hextorgbstring"></a><span data-ttu-id="45dbe-147">hexToRGBString</span><span class="sxs-lookup"><span data-stu-id="45dbe-147">hexToRGBString</span></span>
<span data-ttu-id="45dbe-148">แปลงสี hex เป็นสตริง RGB</span><span class="sxs-lookup"><span data-stu-id="45dbe-148">Converts hex color to RGB string.</span></span>

```typescript
function hexToRGBString(hex: string, transparency?: number): string
```

#### <a name="example"></a><span data-ttu-id="45dbe-149">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="45dbe-149">Example</span></span>

```typescript
import  { hexToRGBString } from "powerbi-visuals-utils-colorutils";

hexToRGBString('#112233');

// returns: "rgb(17,34,51)"
```

### <a name="rotate"></a><span data-ttu-id="45dbe-150">หมุน</span><span class="sxs-lookup"><span data-stu-id="45dbe-150">rotate</span></span>
<span data-ttu-id="45dbe-151">การหมุนสี RGB</span><span class="sxs-lookup"><span data-stu-id="45dbe-151">Rotates RGB color.</span></span>

```typescript
function rotate(rgbString: string, rotateFactor: number): string
```

#### <a name="example"></a><span data-ttu-id="45dbe-152">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="45dbe-152">Example</span></span>

```typescript
import { rotate } from "powerbi-visuals-utils-colorutils";

rotate("#CC0000", 0.25); // returns: #66CC00
```

### <a name="parsecolorstring"></a><span data-ttu-id="45dbe-153">parseColorString</span><span class="sxs-lookup"><span data-stu-id="45dbe-153">parseColorString</span></span>
<span data-ttu-id="45dbe-154">แยกวิเคราะห์สตริงของสีไปเป็นรูปแบบ RGB</span><span class="sxs-lookup"><span data-stu-id="45dbe-154">Parses any color string to RGB format.</span></span>

```typescript
function parseColorString(color: string): RgbColor
```

#### <a name="example"></a><span data-ttu-id="45dbe-155">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="45dbe-155">Example</span></span>

```typescript
import { parseColorString } from "powerbi-visuals-utils-colorutils";

parseColorString('#09f');
// returns: {R: 0, G: 153, B: 255 }

parseColorString('rgba(1, 2, 3, 1.0)');
// returns: {R: 1, G: 2, B: 3, A: 1.0 }
```

### <a name="calculatehighlightcolor"></a><span data-ttu-id="45dbe-156">calculateHighlightColor</span><span class="sxs-lookup"><span data-stu-id="45dbe-156">calculateHighlightColor</span></span>
<span data-ttu-id="45dbe-157">คำนวณสีไฮไลต์จาก rgbColor ที่ยึดตาม lumianceThreshold และ delta</span><span class="sxs-lookup"><span data-stu-id="45dbe-157">Calculate the highlight color from the rgbColor based on the lumianceThreshold and delta.</span></span>

```typescript
function calculateHighlightColor(rgbColor: RgbColor, lumianceThreshold: number, delta: number): string
```

#### <a name="example"></a><span data-ttu-id="45dbe-158">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="45dbe-158">Example</span></span>

```typescript
import { calculateHighlightColor } from "powerbi-visuals-utils-colorutils";

let yellow = "#FFFF00",
    yellowRGB = parseColorString(yellow);

calculateHighlightColor(yellowRGB, 0.8, 0.2);

// returns: '#CCCC00'
```

### <a name="createlinearcolorscale"></a><span data-ttu-id="45dbe-159">createLinearColorScale</span><span class="sxs-lookup"><span data-stu-id="45dbe-159">createLinearColorScale</span></span>
<span data-ttu-id="45dbe-160">ส่งสเกลสีแบบเชิงเส้นกลับสำหรับโดเมนของตัวเลขที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="45dbe-160">Returns a linear color scale for given domain of numbers.</span></span>

```typescript
function createLinearColorScale(domain: number[], range: string[], clamp: boolean): LinearColorScale
```

#### <a name="example"></a><span data-ttu-id="45dbe-161">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="45dbe-161">Example</span></span>

```typescript
import { createLinearColorScale } from "powerbi-visuals-utils-colorutils";

let scale = ColorUtility.createLinearColorScale(
    [0, 1, 2, 3, 4],
    ["red", "green", "blue", "black", "yellow"],
    true);

scale(1); // returns: green
scale(10); // returns: yellow
```

### <a name="shadecolor"></a><span data-ttu-id="45dbe-162">shadeColor</span><span class="sxs-lookup"><span data-stu-id="45dbe-162">shadeColor</span></span>
<span data-ttu-id="45dbe-163">แปลงนิพจน์ hex ของสตริงที่เป็นตัวเลข คำนวณเปอร์เซ็นต์และช่อง R, G, B</span><span class="sxs-lookup"><span data-stu-id="45dbe-163">Converts string hex expression to number, calculate percentage and R, G, B channels.</span></span>
<span data-ttu-id="45dbe-164">ใช้เปอร์เซ็นต์สำหรับแต่ละช่องและส่งกลับค่าฐานสิบหกเป็นสตริงที่มีเครื่องหมายปอนด์</span><span class="sxs-lookup"><span data-stu-id="45dbe-164">Applies percentage for each channel and returns back hex value as string with pound sign.</span></span>

```typescript
function shadeColor(color: string, percent: number): string
```

#### <a name="example"></a><span data-ttu-id="45dbe-165">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="45dbe-165">Example</span></span>

```typescript
import { shadeColor } from "powerbi-visuals-utils-colorutils";

shadeColor('#000000', 0.1); // returns '#1a1a1a'
shadeColor('#FFFFFF', -0.5); // returns '#808080'
shadeColor('#00B8AA', -0.25); // returns '#008a80'
shadeColor('#00B8AA', 0); // returns '#00b8aa'
```

### <a name="rgbblend"></a><span data-ttu-id="45dbe-166">rgbBlend</span><span class="sxs-lookup"><span data-stu-id="45dbe-166">rgbBlend</span></span>
<span data-ttu-id="45dbe-167">การซ้อนทับสีด้วยความทึบเหนือสีพื้นหลัง</span><span class="sxs-lookup"><span data-stu-id="45dbe-167">Overlays a color with opacity over a background color.</span></span> <span data-ttu-id="45dbe-168">ให้ละเว้นช่องสัญญาณอัลฟ่า</span><span class="sxs-lookup"><span data-stu-id="45dbe-168">Any alpha-channel is ignored.</span></span>

```typescript
function rgbBlend(foreColor: RgbColor, opacity: number, backColor: RgbColor): RgbColor
```

#### <a name="example"></a><span data-ttu-id="45dbe-169">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="45dbe-169">Example</span></span>

```typescript
import { rgbBlend} from "powerbi-visuals-utils-colorutils";

rgbBlend({R: 100, G: 100, B: 100}, 0.5, {R: 200, G: 200, B: 200});

// returns: {R: 150, G: 150, B: 150}
```

### <a name="channelblend"></a><span data-ttu-id="45dbe-170">channelBlend</span><span class="sxs-lookup"><span data-stu-id="45dbe-170">channelBlend</span></span>
<span data-ttu-id="45dbe-171">ผสมช่องสัญญาณเดียวสำหรับสองสี</span><span class="sxs-lookup"><span data-stu-id="45dbe-171">Blends a single channel for two colors.</span></span>

```typescript
function channelBlend(foreChannel: number, opacity: number, backChannel: number): number
```

#### <a name="example"></a><span data-ttu-id="45dbe-172">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="45dbe-172">Example</span></span>

```typescript
import { channelBlend} from "powerbi-visuals-utils-colorutils";

channelBlend(0, 1, 255); // returns: 0
channelBlend(128, 1, 255); // returns: 128
channelBlend(255, 0, 0); // returns: 0
channelBlend(88, 0, 88); // returns: 88
```

### <a name="hexblend"></a><span data-ttu-id="45dbe-173">hexBlend</span><span class="sxs-lookup"><span data-stu-id="45dbe-173">hexBlend</span></span>
<span data-ttu-id="45dbe-174">การซ้อนทับสีด้วยความทึบเหนือสีพื้นหลัง</span><span class="sxs-lookup"><span data-stu-id="45dbe-174">Overlays a color with opacity over a background color.</span></span>

```typescript
function hexBlend(foreColor: string, opacity: number, backColor: string): string
```

#### <a name="example"></a><span data-ttu-id="45dbe-175">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="45dbe-175">Example</span></span>

```typescript
import { hexBlend} from "powerbi-visuals-utils-colorutils";

let yellow = "#FFFF00",
    black = "#000000",
    white = "#FFFFFF";

hexBlend(yellow, 0.5, white); // returns: "#FFFF80"
hexBlend(white, 0.5, yellow); // returns: "#FFFF80"

hexBlend(yellow, 0.5, black); // returns: "#808000"
hexBlend(black, 0.5, yellow); // returns: "#808000"
```