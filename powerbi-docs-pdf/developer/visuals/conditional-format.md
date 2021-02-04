---
title: การจัดรูปแบบตามเงื่อนไขในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: เรียนรู้วิธีใช้การจัดรูปแบบตามเงื่อนไขกับโครงการวิชวล Power BI ของคุณ เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.topic: how-to
ms.subservice: powerbi-custom-visuals
ms.date: 10/27/2020
ms.openlocfilehash: 13f9dae542b8e0a340a880ab50b2f57c660e0ed9
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888776"
---
# <a name="add-conditional-formatting"></a><span data-ttu-id="edd49-104">เพิ่มการจัดรูปแบบตามเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="edd49-104">Add conditional formatting</span></span>

<span data-ttu-id="edd49-105">[การจัดรูปแบบตามเงื่อนไข](../../visuals/service-tips-and-tricks-for-color-formatting.md#conditional-formatting-for-visualizations)จะช่วยให้ผู้สร้างรายงานระบุวิธีการแสดงสีในรายงานตามค่าตัวเลข</span><span class="sxs-lookup"><span data-stu-id="edd49-105">[Conditional formatting](../../visuals/service-tips-and-tricks-for-color-formatting.md#conditional-formatting-for-visualizations) lets a report creator specify how colors are displayed in a report, according to a numerical value.</span></span>

<span data-ttu-id="edd49-106">บทความนี้จะอธิบายวิธีเพิ่มฟังก์ชันการจัดรูปแบบตามเงื่อนไขไปยังการแสดงผลด้วยภาพ Power BI</span><span class="sxs-lookup"><span data-stu-id="edd49-106">This article describes how to add the conditional formatting functionality to your Power BI visual.</span></span>

<span data-ttu-id="edd49-107">การจัดรูปแบบตามเงื่อนไขสามารถนำไปใช้กับชนิดคุณสมบัติต่อไปนี้เท่านั้น:</span><span class="sxs-lookup"><span data-stu-id="edd49-107">Conditional formatting can only be applied to the following property types:</span></span>
* <span data-ttu-id="edd49-108">สี</span><span class="sxs-lookup"><span data-stu-id="edd49-108">Color</span></span>
* <span data-ttu-id="edd49-109">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="edd49-109">Text</span></span>
* <span data-ttu-id="edd49-110">ไอคอน</span><span class="sxs-lookup"><span data-stu-id="edd49-110">Icon</span></span>
* <span data-ttu-id="edd49-111">URL ของเว็บ</span><span class="sxs-lookup"><span data-stu-id="edd49-111">Web URL</span></span>

## <a name="add-conditional-formatting-to-your-project"></a><span data-ttu-id="edd49-112">เพิ่มการจัดรูปแบบตามเงื่อนไขไปยังโครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="edd49-112">Add conditional formatting to your project</span></span>

<span data-ttu-id="edd49-113">ส่วนนี้จะแสดงวิธีเพิ่มการจัดรูปแบบตามเงื่อนไขไปยังการแสดงผลด้วยภาพ Power BI ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="edd49-113">This section shows how to add conditional formatting to an existing Power BI visual.</span></span> <span data-ttu-id="edd49-114">รหัสตัวอย่างในบทความนี้จะเป็นไปตามการแสดงผลด้วยภาพ [SampleBarChart](https://github.com/microsoft/PowerBI-visuals-sampleBarChart)</span><span class="sxs-lookup"><span data-stu-id="edd49-114">The example code in this article is based on the [SampleBarChart](https://github.com/microsoft/PowerBI-visuals-sampleBarChart) visual.</span></span> <span data-ttu-id="edd49-115">คุณสามารถตรวจสอบรหัสแหล่งที่มาได้ใน [barChart.ts](https://github.com/microsoft/PowerBI-visuals-sampleBarChart/blob/master/src/barChart.ts)</span><span class="sxs-lookup"><span data-stu-id="edd49-115">You can examine the source code in [barChart.ts](https://github.com/microsoft/PowerBI-visuals-sampleBarChart/blob/master/src/barChart.ts).</span></span>

### <a name="add-a-conditional-color-formatting-entry-in-the-format-pane"></a><span data-ttu-id="edd49-116">เพิ่มรายการการจัดรูปแบบสีตามเงื่อนไขในบานหน้าต่างการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="edd49-116">Add a conditional color formatting entry in the format pane</span></span>

<span data-ttu-id="edd49-117">ในส่วนนี้ คุณจะได้เรียนรู้วิธีเพิ่มรายการการจัดรูปแบบสีตามเงื่อนไขไปยังจุดข้อมูลในบานหน้าต่างการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="edd49-117">In this section you'll learn how to add a conditional color formatting entry, to a data point in format pane.</span></span>

1. <span data-ttu-id="edd49-118">คุณจะต้องใช้อาร์เรย์ `propertyInstanceKind` ใน `VisualObjectInstance` ซึ่งแสดงโดย `powerbi-visuals-api`</span><span class="sxs-lookup"><span data-stu-id="edd49-118">You'll use the `propertyInstanceKind` array in `VisualObjectInstance`, which is exposed by `powerbi-visuals-api`.</span></span> <span data-ttu-id="edd49-119">ขั้นตอนแรกคือคุณต้องตรวจสอบว่าไฟล์ของคุณมีการนำเข้าสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="edd49-119">Your first step is to verify that your file includes this import:</span></span>

    ```typescript
    import powerbiVisualsApi from "powerbi-visuals-api";
    ```

2. <span data-ttu-id="edd49-120">หากต้องการระบุชนิดของการจัดรูปแบบที่เหมาะสม (*ค่าคงที่* *ค่าคงที่หรือกฎ* หรือ *กฎ*) คุณจะต้องใช้ Enum `VisualEnumerationInstanceKinds`</span><span class="sxs-lookup"><span data-stu-id="edd49-120">To specify the appropriate type of formatting (*Constant*, *ConstantOrRule*, or *Rule*), you'll use  the `VisualEnumerationInstanceKinds` enum.</span></span> <span data-ttu-id="edd49-121">เพิ่มการนำเข้าต่อไปนี้ไปยังไฟล์ของคุณ:</span><span class="sxs-lookup"><span data-stu-id="edd49-121">Add the following import to your file:</span></span>

    ```typescript
    import VisualEnumerationInstanceKinds = powerbiVisualsApi.VisualEnumerationInstanceKinds;
    ```

3. <span data-ttu-id="edd49-122">ระบุคุณสมบัติทั้งหมดที่คุณต้องการสนับสนุนการจัดรูปแบบตามเงื่อนไขภายใต้อาร์เรย์ `propertyInstanceKind`</span><span class="sxs-lookup"><span data-stu-id="edd49-122">List all the properties that you'd like to support conditional formatting, under the `propertyInstanceKind` array.</span></span> <span data-ttu-id="edd49-123">กำหนดคุณสมบัติเหล่านี้ในวิธีการ `enumerateObjectInstances`</span><span class="sxs-lookup"><span data-stu-id="edd49-123">Define these properties in the `enumerateObjectInstances` method.</span></span>

    ```typescript
    public enumerateObjectInstances(options: EnumerateVisualObjectInstancesOptions): VisualObjectInstanceEnumeration {
            …
            case 'colorSelector':
                …
                    objectEnumeration.push({
                        objectName: objectName,
                        displayName: barDataPoint.category,
                        properties: {
                            fill: {
                                solid: {
                                    color: barDataPoint.color
                                }
                            }
                        },
                        selector: dataViewWildcard.createDataViewWildcardSelector(dataViewWildcard.DataViewWildcardMatchingOption.InstancesAndTotals),
                        altConstantValueSelector: barDataPoint.selectionId.getSelector(),

                        // List your conditional formatting properties
                        propertyInstanceKind: {
                            fill: VisualEnumerationInstanceKinds.ConstantOrRule
                        }
                    });
                }
            …
    }

    ```

    <span data-ttu-id="edd49-124">`VisualEnumerationInstanceKinds.ConstantOrRule` จะสร้างรายการ UI การจัดรูปแบบตามเงื่อนไขควบคู่ไปกับองค์ประกอบ UI การจัดรูปแบบตามเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="edd49-124">`VisualEnumerationInstanceKinds.ConstantOrRule` will create the conditional formatting UI entry alongside the constant formatting UI element.</span></span>

    >[!div class="mx-imgBorder"]
    ><span data-ttu-id="edd49-125">![สกรีนช็อตของปุ่มการจัดรูปแบบตามเงื่อนไขตามที่ปรากฏใน Power BI ซึ่งอยู่ถัดจากปุ่มสีปกติ](media/conditional-formatting/conditional-formatting-ui.png)</span><span class="sxs-lookup"><span data-stu-id="edd49-125">![Screenshot of the conditional formatting button, as it appears in Power BI, next to the regular color button.](media/conditional-formatting/conditional-formatting-ui.png)</span></span>

### <a name="define-how-conditional-formatting-behaves"></a><span data-ttu-id="edd49-126">กำหนดลักษณะการทำงานของการจัดรูปแบบตามเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="edd49-126">Define how conditional formatting behaves</span></span>

<span data-ttu-id="edd49-127">กำหนดวิธีการจัดรูปแบบที่จะนำไปใช้กับจุดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="edd49-127">Define how formatting will be applied to your data points.</span></span>

<span data-ttu-id="edd49-128">การใช้ `createDataViewWildcardSelector` ที่ประกาศภายใต้ `powerbi-visuals-utils-dataviewutils` ระบุว่าการจัดรูปแบบตามเงื่อนไขจะนำไปใช้กับอินสแตนซ์ ผลรวม หรือทั้งสองอย่าง</span><span class="sxs-lookup"><span data-stu-id="edd49-128">Using `createDataViewWildcardSelector` declared under `powerbi-visuals-utils-dataviewutils`, specify whether conditional formatting will be applied to instances, totals, or both.</span></span> <span data-ttu-id="edd49-129">โปรดดู [DataViewWildcard](utils-dataview.md#) สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="edd49-129">For more information, see [DataViewWildcard](utils-dataview.md#).</span></span>

<span data-ttu-id="edd49-130">ใน `enumerateObjectInstances` ดำเนินการเปลี่ยนแปลงต่อไปนี้กับออปเจ็กต์ที่คุณต้องการนำไปใช้กับการจัดรูปแบบตามเงื่อนไขเพื่อ:</span><span class="sxs-lookup"><span data-stu-id="edd49-130">In `enumerateObjectInstances`, make the following changes to the objects you want to apply conditional formatting to:</span></span>

 * <span data-ttu-id="edd49-131">แทนที่ค่า `selector` ด้วยการเรียกใช้ `dataViewWildcard.createDataViewWildcardSelector(dataViewWildcardMatchingOption)`</span><span class="sxs-lookup"><span data-stu-id="edd49-131">Replace the `selector` value with the `dataViewWildcard.createDataViewWildcardSelector(dataViewWildcardMatchingOption)` call.</span></span> <span data-ttu-id="edd49-132">`DataViewWildcardMatchingOption` จะกำหนดว่าการจัดรูปแบบตามเงื่อนไขจะนำไปใช้กับอินสแตนซ์ ผลรวม หรือทั้งสองอย่าง</span><span class="sxs-lookup"><span data-stu-id="edd49-132">`DataViewWildcardMatchingOption` defines whether conditional formatting is applied to instances, totals, or both.</span></span>

* <span data-ttu-id="edd49-133">เพิ่มคุณสมบัติ `altConstantValueSelector` ด้วยค่าที่กำหนดไว้ก่อนหน้านี้สำหรับคุณสมบัติ `selector`</span><span class="sxs-lookup"><span data-stu-id="edd49-133">Add the `altConstantValueSelector` property with the value previously defined for the `selector` property.</span></span>

```typescript
case 'colorSelector':
         …
            objectEnumeration.push({
                objectName: objectName,
                displayName: barDataPoint.category,
                properties: {
                    fill: {
                        solid: {
                            color: barDataPoint.color
                        }
                    }
                },

                // Define whether the conditional formatting will apply to instances, totals, or both
                selector: dataViewWildcard.createDataViewWildcardSelector(dataViewWildcard.DataViewWildcardMatchingOption.InstancesAndTotals),

                // Add this property with the value previously defined for the selector property
                altConstantValueSelector: barDataPoint.selectionId.getSelector(),

                propertyInstanceKind: { 
                    fill: VisualEnumerationInstanceKinds.ConstantOrRule
                }
            });
        }

```

## <a name="next-steps"></a><span data-ttu-id="edd49-134">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="edd49-134">Next steps</span></span>

<span data-ttu-id="edd49-135">ตรวจสอบบทความ [DataViewUtils](utils-dataview.md)</span><span class="sxs-lookup"><span data-stu-id="edd49-135">Review the [DataViewUtils](utils-dataview.md) article.</span></span>