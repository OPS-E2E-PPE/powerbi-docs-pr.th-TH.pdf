---
title: การสนับสนุนโหมดคอนทราสต์สูงของวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการเพิ่มการรองรับโหมดความคมชัดสูงไปยังวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: how-to
ms.date: 06/18/2019
ms.openlocfilehash: f55427511a76fc65b3ae6b3933dca68ef742039c
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97889213"
---
# <a name="high-contrast-mode-support-in-power-bi-visuals"></a><span data-ttu-id="35757-104">การรองรับโหมดความคมชัดสูงในวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="35757-104">High-contrast mode support in Power BI visuals</span></span>

<span data-ttu-id="35757-105">การตั้งค่า *ความคมชัดสูง* ของ Windows ทำให้ข้อความและแอปสามารถดูได้ง่ายขึ้นโดยการแสดงสีที่แตกต่างกันมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="35757-105">The Windows *high contrast* setting makes text and apps easier to see by displaying more distinct colors.</span></span> <span data-ttu-id="35757-106">บทความนี้อธิบายวิธีการเพิ่มการรองรับโหมดความคมชัดสูงไปยังวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="35757-106">This article discusses how to add high-contrast mode support to Power BI visuals.</span></span> <span data-ttu-id="35757-107">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การรองรับโหมดความคมชัดสูงในวิชวล Power BI](https://powerbi.microsoft.com/blog/power-bi-desktop-june-2018-feature-summary/#highContrast)</span><span class="sxs-lookup"><span data-stu-id="35757-107">For more information, see [high-contrast support in Power BI](https://powerbi.microsoft.com/blog/power-bi-desktop-june-2018-feature-summary/#highContrast).</span></span>

<span data-ttu-id="35757-108">หากต้องการดูการนำการรองรับโหมดความคมชัดสูงไปใช้งาน โปรดไปที่ [พื้นที่เก็บข้อมูลวิชวล PowerBI-visuals-sampleBarChart](https://github.com/Microsoft/PowerBI-visuals-sampleBarChart/commit/61011c82b66ca0d3321868f1d089c65101ca42e6)</span><span class="sxs-lookup"><span data-stu-id="35757-108">To view an implementation of high-contrast support, go to the [PowerBI-visuals-sampleBarChart visual repository](https://github.com/Microsoft/PowerBI-visuals-sampleBarChart/commit/61011c82b66ca0d3321868f1d089c65101ca42e6).</span></span>

## <a name="on-initialization"></a><span data-ttu-id="35757-109">เกี่ยวกับการเตรียมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="35757-109">On initialization</span></span>

<span data-ttu-id="35757-110">สมาชิก colorPalette ของ `options.host` มีคุณสมบัติหลายอย่างสำหรับโหมดความคมชัดสูง</span><span class="sxs-lookup"><span data-stu-id="35757-110">The colorPalette member of `options.host` has several properties for high-contrast mode.</span></span> <span data-ttu-id="35757-111">ใช้คุณสมบัติเหล่านี้เพื่อตรวจสอบว่าโหมดความคมชัดสูงเปิดใช้งานอยู่หรือไม่ และถ้าเปิดอยู่ สีอะไรที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="35757-111">Use these properties to determine whether high-contrast mode is active and, if it is, what colors to use.</span></span>

### <a name="detect-that-power-bi-is-in-high-contrast-mode"></a><span data-ttu-id="35757-112">ตรวจพบว่า Power BI อยู่ในโหมดความคมชัดสูง</span><span class="sxs-lookup"><span data-stu-id="35757-112">Detect that Power BI is in high-contrast mode</span></span>

<span data-ttu-id="35757-113">ถ้า`host.colorPalette.isHighContrast` เป็น`true` โหมดความคมชัดสูงมีการใช้งานอยู่และวิชวลควรวาดตัวเองตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="35757-113">If `host.colorPalette.isHighContrast` is `true`, high-contrast mode is active and the visual should draw itself accordingly.</span></span>

### <a name="get-high-contrast-colors"></a><span data-ttu-id="35757-114">รับสีที่มีความคมชัดสูง</span><span class="sxs-lookup"><span data-stu-id="35757-114">Get high-contrast colors</span></span>

<span data-ttu-id="35757-115">ในโหมดความคมชัดสูง วิชวลของคุณควรจำกัดตัวเองเป็นการตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="35757-115">In high-contrast mode, your visual should limit itself to the following settings:</span></span>

* <span data-ttu-id="35757-116">**สีพื้นหน้า** ใช้ในการวาดเส้น ไอคอน ข้อความ และเค้าร่างหรือการเติมรูปร่าง</span><span class="sxs-lookup"><span data-stu-id="35757-116">**Foreground** color is used to draw any lines, icons, text, and outline or fill of shapes.</span></span>
* <span data-ttu-id="35757-117">**สีพื้นหลัง** ใช้สำหรับพื้นหลังและเป็นสีเติมของรูปร่างที่มีการระบุไว้</span><span class="sxs-lookup"><span data-stu-id="35757-117">**Background** color is used for background, and as the fill color of outlined shapes.</span></span>
* <span data-ttu-id="35757-118">**สีที่เลือกไว้สำหรับเบื้องหน้า** จะใช้เพื่อระบุองค์ประกอบที่เลือกหรือที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="35757-118">**Foreground - selected** color is used to indicate a selected or active element.</span></span>
* <span data-ttu-id="35757-119">**สีของการเชื่อมโยงหลายมิติ** จะใช้เฉพาะกับข้อความที่เชื่อมโยงหลายมิติ</span><span class="sxs-lookup"><span data-stu-id="35757-119">**Hyperlink** color is used only for hyperlink text.</span></span>

> [!NOTE]
> <span data-ttu-id="35757-120">หากจำเป็นต้องใช้สีทุติยภูมิ อาจใช้สีพื้นหน้ากับความทึบแสงบางอย่าง (วิชวลแบบดั้งเดิมของ Power BI ใช้ความทึบ 40%)</span><span class="sxs-lookup"><span data-stu-id="35757-120">If a secondary color is needed, foreground color may be used with some opacity (Power BI native visuals use 40% opacity).</span></span> <span data-ttu-id="35757-121">ใช้การดำเนินการนี้เพื่อให้สามารถดูรายละเอียดของวิชวลได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="35757-121">Use this sparingly to keep the visual details easy to see.</span></span>

<span data-ttu-id="35757-122">ในระหว่างการเตรียมใช้งาน คุณสามารถจัดเก็บค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="35757-122">During initialization, you can store the following values:</span></span>

```typescript
private isHighContrast: boolean;

private foregroundColor: string;
private backgroundColor: string;
private foregroundSelectedColor: string;
private hyperlinkColor: string;
//...

constructor(options: VisualConstructorOptions) {
    this.host = options.host;
    let colorPalette: ISandboxExtendedColorPalette = host.colorPalette;
    //...
    this.isHighContrast = colorPalette.isHighContrast;
    if (this.isHighContrast) {
        this.foregroundColor = colorPalette.foreground.value;
        this.backgroundColor = colorPalette.background.value;
        this.foregroundSelectedColor = colorPalette.foregroundSelected.value;
        this.hyperlinkColor = colorPalette.hyperlink.value;
    }
```

<span data-ttu-id="35757-123">หรือคุณสามารถจัดเก็บออบเจ็กต์ `host` ในระหว่างการเตรียมใช้งานและเข้าถึงคุณสมบัติ `colorPalette` ที่เกี่ยวข้องในระหว่างการอัปเดตได้</span><span class="sxs-lookup"><span data-stu-id="35757-123">Or you can store the `host` object during initialization and access the relevant `colorPalette` properties during update.</span></span>

## <a name="on-update"></a><span data-ttu-id="35757-124">ในการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="35757-124">On update</span></span>

<span data-ttu-id="35757-125">การใช้งานที่เฉพาะเจาะจงของการรองรับความคมชัดสูงจะแตกต่างในแต่ละวิชวล และขึ้นอยู่กับรายละเอียดของการออกแบบกราฟิก</span><span class="sxs-lookup"><span data-stu-id="35757-125">The specific implementations of high-contrast support vary from visual to visual and depend on the details of the graphic design.</span></span> <span data-ttu-id="35757-126">เพื่อให้ง่ายต่อการแยกความแตกต่างของรายละเอียดที่สำคัญด้วยสีที่จำกัด โดยทั่วไป โหมดความคมชัดสูงจะต้องมีการออกแบบที่แตกต่างกันเล็กน้อยกว่าค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="35757-126">To keep important details easy to distinguish with the limited colors, high-contrast mode ordinarily requires a design that's slightly different from the default mode.</span></span>

<span data-ttu-id="35757-127">วิชวลแบบดั้งเดิมของ Power BI เป็นไปตามแนวทางเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="35757-127">Power BI native visuals follow these guidelines:</span></span>

* <span data-ttu-id="35757-128">จุดข้อมูลทั้งหมดใช้สีเดียวกัน (พื้นหน้า)</span><span class="sxs-lookup"><span data-stu-id="35757-128">All data points use the same color (foreground).</span></span>
* <span data-ttu-id="35757-129">ข้อความ แกน ลูกศร เส้น และอื่น ๆ ทั้งหมดใช้สีพื้นหน้า</span><span class="sxs-lookup"><span data-stu-id="35757-129">All text, axes, arrows, lines, and so on use the foreground color.</span></span>
* <span data-ttu-id="35757-130">รูปร่างหนาจะวาดเป็นเค้าร่างด้วยเส้นขีดหนา (อย่างน้อยสองพิกเซล) และการเติมสีพื้นหลัง</span><span class="sxs-lookup"><span data-stu-id="35757-130">Thick shapes are drawn as outlines, with thick strokes (at least two pixels) and background color fill.</span></span>
* <span data-ttu-id="35757-131">เมื่อจุดข้อมูลมีความเกี่ยวข้องกัน จุดข้อมูลจะแตกต่างตามรูปร่างเครื่องหมายที่แตกต่างกัน และเส้นข้อมูลมีความแตกต่างกันตามการลงเส้นประที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="35757-131">When data points are relevant, they're distinguished by different marker shapes, and data lines are distinguished by different dashing.</span></span>
* <span data-ttu-id="35757-132">เมื่อไฮไลท์องค์ประกอบข้อมูล องค์ประกอบอื่น ๆ ทั้งหมดเปลี่ยนความทึบของตนเป็น 40%</span><span class="sxs-lookup"><span data-stu-id="35757-132">When a data element is highlighted, all other elements change their opacity to 40%.</span></span>
* <span data-ttu-id="35757-133">สำหรับตัวแบ่งส่วนข้อมูล องค์ประกอบตัวกรองที่ใช้งานอยู่จะใช้สีที่เลือกไว้สำหรับเบื้องหน้า</span><span class="sxs-lookup"><span data-stu-id="35757-133">For slicers, active filter elements use foreground-selected color.</span></span>

<span data-ttu-id="35757-134">ในแผนภูมิแท่งตัวอย่างต่อไปนี้ ตัวอย่างเช่น แถบทั้งหมดจะถูกวาดด้วยโครงร่างเบื้องหน้าที่หนาขนาดสองพิกเซลและการเติมพื้นหลัง</span><span class="sxs-lookup"><span data-stu-id="35757-134">In the following sample bar chart, for example, all bars are drawn with two pixels of thick foreground outline and background fill.</span></span> <span data-ttu-id="35757-135">เปรียบเทียบลักษณะที่ปรากฏกับสีเริ่มต้นและธีมสองแบบที่มีความคมชัดสูง:</span><span class="sxs-lookup"><span data-stu-id="35757-135">Compare the way it looks with default colors and with a couple of high-contrast themes:</span></span>

<span data-ttu-id="35757-136">![แผนภูมิแท่งตัวอย่างโดยใช้สีมาตรฐาน ](media/high-contrast-support/hc-samplebarchart-standard.png)
![ แผนภูมิแท่งตัวอย่างโดยใช้ธีมสี *Dark #2* ](media/high-contrast-support/hc-samplebarchart-dark2.png)
![แผนภูมิแท่งสีตัวอย่างโดยใช้ธีมสี *White*](media/high-contrast-support/hc-samplebarchart-white.png)</span><span class="sxs-lookup"><span data-stu-id="35757-136">![Sample Bar Chart using standard colors](media/high-contrast-support/hc-samplebarchart-standard.png)
![Sample Bar Chart using *Dark #2* color theme](media/high-contrast-support/hc-samplebarchart-dark2.png)
![Sample Bar Chart using *White* color theme](media/high-contrast-support/hc-samplebarchart-white.png)</span></span>

<span data-ttu-id="35757-137">ส่วนถัดไปแสดงตำแหน่งเดียวในฟังก์ชัน `visualTransform` ที่มีการเปลี่ยนแปลงเพื่อรองรับความคมชัดสูง</span><span class="sxs-lookup"><span data-stu-id="35757-137">The next section shows one place in the `visualTransform` function that was changed to support high contrast.</span></span> <span data-ttu-id="35757-138">ซึ่งเรียกว่าเป็นส่วนหนึ่งของการแสดงผลระหว่างการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="35757-138">It's called as part of rendering during the update.</span></span>

### <a name="before"></a><span data-ttu-id="35757-139">ก่อน</span><span class="sxs-lookup"><span data-stu-id="35757-139">Before</span></span>

```typescript
for (let i = 0, len = Math.max(category.values.length, dataValue.values.length); i < len; i++) {
    let defaultColor: Fill = {
        solid: {
            color: colorPalette.getColor(category.values[i] + '').value
        }
    };

    barChartDataPoints.push({
        category: category.values[i] + '',
        value: dataValue.values[i],
        color: getCategoricalObjectValue<Fill>(category, i, 'colorSelector', 'fill', defaultColor).solid.color,
        selectionId: host.createSelectionIdBuilder()
            .withCategory(category, i)
            .createSelectionId()
    });
}
```

### <a name="after"></a><span data-ttu-id="35757-140">หลังจาก</span><span class="sxs-lookup"><span data-stu-id="35757-140">After</span></span>

```typescript
for (let i = 0, len = Math.max(category.values.length, dataValue.values.length); i < len; i++) {
    const color: string = getColumnColorByIndex(category, i, colorPalette);

    const selectionId: ISelectionId = host.createSelectionIdBuilder()
        .withCategory(category, i)
        .createSelectionId();

    barChartDataPoints.push({
        color,
        strokeColor,
        strokeWidth,
        selectionId,
        value: dataValue.values[i],
        category: `${category.values[i]}`,
    });
}

//...

function getColumnColorByIndex(
    category: DataViewCategoryColumn,
    index: number,
    colorPalette: ISandboxExtendedColorPalette,
): string {
    if (colorPalette.isHighContrast) {
        return colorPalette.background.value;
    }

    const defaultColor: Fill = {
        solid: {
            color: colorPalette.getColor(`${category.values[index]}`).value,
        }
    };

    return getCategoricalObjectValue<Fill>(category, index, 'colorSelector', 'fill', defaultColor).solid.color;
}
```
