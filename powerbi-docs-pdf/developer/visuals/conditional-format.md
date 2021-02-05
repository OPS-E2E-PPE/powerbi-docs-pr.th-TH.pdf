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
# <a name="add-conditional-formatting"></a>เพิ่มการจัดรูปแบบตามเงื่อนไข

[การจัดรูปแบบตามเงื่อนไข](../../visuals/service-tips-and-tricks-for-color-formatting.md#conditional-formatting-for-visualizations)จะช่วยให้ผู้สร้างรายงานระบุวิธีการแสดงสีในรายงานตามค่าตัวเลข

บทความนี้จะอธิบายวิธีเพิ่มฟังก์ชันการจัดรูปแบบตามเงื่อนไขไปยังการแสดงผลด้วยภาพ Power BI

การจัดรูปแบบตามเงื่อนไขสามารถนำไปใช้กับชนิดคุณสมบัติต่อไปนี้เท่านั้น:
* สี
* ข้อความ
* ไอคอน
* URL ของเว็บ

## <a name="add-conditional-formatting-to-your-project"></a>เพิ่มการจัดรูปแบบตามเงื่อนไขไปยังโครงการของคุณ

ส่วนนี้จะแสดงวิธีเพิ่มการจัดรูปแบบตามเงื่อนไขไปยังการแสดงผลด้วยภาพ Power BI ที่มีอยู่ รหัสตัวอย่างในบทความนี้จะเป็นไปตามการแสดงผลด้วยภาพ [SampleBarChart](https://github.com/microsoft/PowerBI-visuals-sampleBarChart) คุณสามารถตรวจสอบรหัสแหล่งที่มาได้ใน [barChart.ts](https://github.com/microsoft/PowerBI-visuals-sampleBarChart/blob/master/src/barChart.ts)

### <a name="add-a-conditional-color-formatting-entry-in-the-format-pane"></a>เพิ่มรายการการจัดรูปแบบสีตามเงื่อนไขในบานหน้าต่างการจัดรูปแบบ

ในส่วนนี้ คุณจะได้เรียนรู้วิธีเพิ่มรายการการจัดรูปแบบสีตามเงื่อนไขไปยังจุดข้อมูลในบานหน้าต่างการจัดรูปแบบ

1. คุณจะต้องใช้อาร์เรย์ `propertyInstanceKind` ใน `VisualObjectInstance` ซึ่งแสดงโดย `powerbi-visuals-api` ขั้นตอนแรกคือคุณต้องตรวจสอบว่าไฟล์ของคุณมีการนำเข้าสิ่งต่อไปนี้:

    ```typescript
    import powerbiVisualsApi from "powerbi-visuals-api";
    ```

2. หากต้องการระบุชนิดของการจัดรูปแบบที่เหมาะสม (*ค่าคงที่* *ค่าคงที่หรือกฎ* หรือ *กฎ*) คุณจะต้องใช้ Enum `VisualEnumerationInstanceKinds` เพิ่มการนำเข้าต่อไปนี้ไปยังไฟล์ของคุณ:

    ```typescript
    import VisualEnumerationInstanceKinds = powerbiVisualsApi.VisualEnumerationInstanceKinds;
    ```

3. ระบุคุณสมบัติทั้งหมดที่คุณต้องการสนับสนุนการจัดรูปแบบตามเงื่อนไขภายใต้อาร์เรย์ `propertyInstanceKind` กำหนดคุณสมบัติเหล่านี้ในวิธีการ `enumerateObjectInstances`

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

    `VisualEnumerationInstanceKinds.ConstantOrRule` จะสร้างรายการ UI การจัดรูปแบบตามเงื่อนไขควบคู่ไปกับองค์ประกอบ UI การจัดรูปแบบตามเงื่อนไข

    >[!div class="mx-imgBorder"]
    >![สกรีนช็อตของปุ่มการจัดรูปแบบตามเงื่อนไขตามที่ปรากฏใน Power BI ซึ่งอยู่ถัดจากปุ่มสีปกติ](media/conditional-formatting/conditional-formatting-ui.png)

### <a name="define-how-conditional-formatting-behaves"></a>กำหนดลักษณะการทำงานของการจัดรูปแบบตามเงื่อนไข

กำหนดวิธีการจัดรูปแบบที่จะนำไปใช้กับจุดข้อมูลของคุณ

การใช้ `createDataViewWildcardSelector` ที่ประกาศภายใต้ `powerbi-visuals-utils-dataviewutils` ระบุว่าการจัดรูปแบบตามเงื่อนไขจะนำไปใช้กับอินสแตนซ์ ผลรวม หรือทั้งสองอย่าง โปรดดู [DataViewWildcard](utils-dataview.md#) สำหรับข้อมูลเพิ่มเติม

ใน `enumerateObjectInstances` ดำเนินการเปลี่ยนแปลงต่อไปนี้กับออปเจ็กต์ที่คุณต้องการนำไปใช้กับการจัดรูปแบบตามเงื่อนไขเพื่อ:

 * แทนที่ค่า `selector` ด้วยการเรียกใช้ `dataViewWildcard.createDataViewWildcardSelector(dataViewWildcardMatchingOption)` `DataViewWildcardMatchingOption` จะกำหนดว่าการจัดรูปแบบตามเงื่อนไขจะนำไปใช้กับอินสแตนซ์ ผลรวม หรือทั้งสองอย่าง

* เพิ่มคุณสมบัติ `altConstantValueSelector` ด้วยค่าที่กำหนดไว้ก่อนหน้านี้สำหรับคุณสมบัติ `selector`

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

## <a name="next-steps"></a>ขั้นตอนถัดไป

ตรวจสอบบทความ [DataViewUtils](utils-dataview.md)