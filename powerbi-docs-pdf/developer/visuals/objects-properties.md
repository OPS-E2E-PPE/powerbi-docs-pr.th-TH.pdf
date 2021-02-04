---
title: อ็อบเจกต์และคุณสมบัติของวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายคุณสมบัติแบบปรับแต่งได้ของวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.date: 06/18/2019
ms.openlocfilehash: 4596465fcd9f59768b18282ec3ad39d2531b7768
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97885970"
---
# <a name="objects-and-properties-of-power-bi-visuals"></a><span data-ttu-id="3c54e-104">ออบเจ็กต์และคุณสมบัติของวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="3c54e-104">Objects and properties of Power BI visuals</span></span>

<span data-ttu-id="3c54e-105">ออบเจ็กต์อธิบายคุณสมบัติแบบปรับแต่งได้ที่เกี่ยวข้องกับวิชวล</span><span class="sxs-lookup"><span data-stu-id="3c54e-105">Objects describe customizable properties that are associated with a visual.</span></span> <span data-ttu-id="3c54e-106">ออบเจ็กต์สามารถมีคุณสมบัติได้หลายรายการ และแต่ละคุณสมบัติมีประเภทที่เกี่ยวข้องซึ่งอธิบายถึงคุณสมบัติที่จะเป็น</span><span class="sxs-lookup"><span data-stu-id="3c54e-106">An object can have multiple properties, and each property has an associated type that describes what the property will be.</span></span> <span data-ttu-id="3c54e-107">บทความนี้ให้ข้อมูลเกี่ยวกับออบเจ็กต์และชนิดของคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="3c54e-107">This article provides information about objects and property types.</span></span>

<span data-ttu-id="3c54e-108">`myCustomObject` เป็นชื่อภายในที่ใช้เพื่ออ้างอิงออบเจ็กต์ภายใน `dataView` และ `enumerateObjectInstances`</span><span class="sxs-lookup"><span data-stu-id="3c54e-108">`myCustomObject` is the internal name that's used to reference the object within `dataView` and `enumerateObjectInstances`.</span></span>

```json
"objects": {
    "myCustomObject": {
        "displayName": "My Object Name",
        "properties": { ... }
    }
}
```

## <a name="display-name"></a><span data-ttu-id="3c54e-109">ชื่อที่แสดง</span><span class="sxs-lookup"><span data-stu-id="3c54e-109">Display name</span></span>

<span data-ttu-id="3c54e-110">`displayName` คือชื่อที่จะแสดงในบานหน้าต่างคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="3c54e-110">`displayName` is the name that will be shown in the property pane.</span></span>

## <a name="properties"></a><span data-ttu-id="3c54e-111">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="3c54e-111">Properties</span></span>

<span data-ttu-id="3c54e-112">`properties` เป็นแผนที่ของคุณสมบัติที่กำหนดโดยผู้พัฒนา</span><span class="sxs-lookup"><span data-stu-id="3c54e-112">`properties` is a map of properties that are defined by the developer.</span></span>

```json
"properties": {
    "myFirstProperty": {
        "displayName": "firstPropertyName",
        "type": ValueTypeDescriptor | StructuralTypeDescriptor
    }
}
```

> [!NOTE]
> <span data-ttu-id="3c54e-113">`show` เป็นคุณสมบัติพิเศษที่เปิดใช้งานสวิตช์เพื่อสลับวัตถุ</span><span class="sxs-lookup"><span data-stu-id="3c54e-113">`show` is a special property that enables a switch to toggle the object.</span></span>

<span data-ttu-id="3c54e-114">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="3c54e-114">Example:</span></span>

```json
"properties": {
    "show": {
        "displayName": "My Property Switch",
        "type": {"bool": true}
    }
}
```

### <a name="property-types"></a><span data-ttu-id="3c54e-115">ชนิดของคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="3c54e-115">Property types</span></span>

<span data-ttu-id="3c54e-116">มีชนิดของคุณสมบัติสองชนิด: `ValueTypeDescriptor` และ `StructuralTypeDescriptor`</span><span class="sxs-lookup"><span data-stu-id="3c54e-116">There are two property types: `ValueTypeDescriptor` and `StructuralTypeDescriptor`.</span></span>

#### <a name="value-type-descriptor"></a><span data-ttu-id="3c54e-117">ตัวอธิบายชนิดค่า</span><span class="sxs-lookup"><span data-stu-id="3c54e-117">Value type descriptor</span></span>

<span data-ttu-id="3c54e-118">ส่วนใหญ่ `ValueTypeDescriptor` เป็นชนิดพื้นฐาน และโดยปกติแล้วจะเป็นออบเจ็กต์แบบสแตติก</span><span class="sxs-lookup"><span data-stu-id="3c54e-118">`ValueTypeDescriptor` types are mostly primitive and are ordinarily used as a static object.</span></span>

<span data-ttu-id="3c54e-119">ต่อไปนี้เป็นองค์ประกอบส่วนหนึ่งของ `ValueTypeDescriptor` แบบทั่วไป</span><span class="sxs-lookup"><span data-stu-id="3c54e-119">Here are some of the common `ValueTypeDescriptor` elements:</span></span>

```typescript
export interface ValueTypeDescriptor {
    text?: boolean;
    numeric?: boolean;
    integer?: boolean;
    bool?: boolean;
}
```

#### <a name="structural-type-descriptor"></a><span data-ttu-id="3c54e-120">ตัวอธิบายชนิดโครงสร้าง</span><span class="sxs-lookup"><span data-stu-id="3c54e-120">Structural type descriptor</span></span>

<span data-ttu-id="3c54e-121">ส่วนใหญ่ `StructuralTypeDescriptor` จะใช้สำหรับออบเจ็กต์ที่ผูกกับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3c54e-121">`StructuralTypeDescriptor` types are mostly used for data-bound objects.</span></span>
<span data-ttu-id="3c54e-122">ชนิด `StructuralTypeDescriptor` ที่พบมากที่สุดคือ *การใส่สีพื้นหลัง*</span><span class="sxs-lookup"><span data-stu-id="3c54e-122">The most common `StructuralTypeDescriptor` type is *fill*.</span></span>

```typescript
export interface StructuralTypeDescriptor {
    fill?: FillTypeDescriptor;
}
```

## <a name="gradient-property"></a><span data-ttu-id="3c54e-123">คุณสมบัติการไล่ระดับสี</span><span class="sxs-lookup"><span data-stu-id="3c54e-123">Gradient property</span></span>

<span data-ttu-id="3c54e-124">คุณสมบัติการไล่ระดับสีเป็นคุณสมบัติที่ไม่สามารถกำหนดเป็นคุณสมบัติมาตรฐานได้</span><span class="sxs-lookup"><span data-stu-id="3c54e-124">The gradient property is a property that can't be set as a standard property.</span></span> <span data-ttu-id="3c54e-125">แต่คุณจำเป็นต้องกำหนดกฎสำหรับการแทนที่คุณสมบัติตัวเลือกสี (ชนิด *การใส่สีพื้นหลัง*)</span><span class="sxs-lookup"><span data-stu-id="3c54e-125">Instead, you need to set a rule for the substitution of the color picker property (*fill* type).</span></span>

<span data-ttu-id="3c54e-126">ตัวอย่างจะแสดงในโค้ดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3c54e-126">An example is shown in the following code:</span></span>

```json
"properties": {
    "showAllDataPoints": {
        "displayName": "Show all",
        "displayNameKey": "Visual_DataPoint_Show_All",
        "type": {
            "bool": true
        }
    },
    "fill": {
        "displayName": "Fill",
        "displayNameKey": "Visual_Fill",
        "type": {
            "fill": {
                "solid": {
                    "color": true
                }
            }
        }
    },
    "fillRule": {
        "displayName": "Color saturation",
        "displayNameKey": "Visual_ColorSaturation",
        "type": {
            "fillRule": {}
        },
        "rule": {
            "inputRole": "Gradient",
            "output": {
                "property": "fill",
                    "selector": [
                        "Category"
                    ]
            }
        }
    }
}
```

<span data-ttu-id="3c54e-127">กรุณาใส่ใจกับคุณสมบัติ *การใส่สีพื้นหลัง* และ *กฎการใส่สีพื้นหลัง*</span><span class="sxs-lookup"><span data-stu-id="3c54e-127">Pay attention to the *fill* and *fillRule* properties.</span></span> <span data-ttu-id="3c54e-128">อันดับแรกคือตัวเลือกสี และอันดับที่สองคือกฎการทดแทนสำหรับการไล่ระดับสีที่จะแทนที่ *คุณสมบัติ การใส่สีพื้นหลัง*, `visually` เมื่อเป็นไปตามเงื่อนไขของกฎ</span><span class="sxs-lookup"><span data-stu-id="3c54e-128">The first is the color picker, and the second is the substitution rule for the gradient that will replace the *fill property*, `visually`, when the rule conditions are met.</span></span>

<span data-ttu-id="3c54e-129">คุณสามารถตั้งค่าการเชื่อมโยงระหว่างคุณสมบัติ *การใส่สีพื้นหลัง* และกฎการแทนที่ได้ในส่วน `"rule"`>`"output"` ของคุณสมบัติ *กฎการใส่สีพื้นหลัง*</span><span class="sxs-lookup"><span data-stu-id="3c54e-129">This link between the *fill* property and the substitution rule is set in the `"rule"`>`"output"` section of the *fillRule* property.</span></span>

<span data-ttu-id="3c54e-130">คุณสมบัติ `"Rule"`>`"InputRole"` กำหนดบทบาทข้อมูลที่ทริกเกอร์กฎ (เงื่อนไข)</span><span class="sxs-lookup"><span data-stu-id="3c54e-130">`"Rule"`>`"InputRole"` property sets which data role triggers the rule (condition).</span></span> <span data-ttu-id="3c54e-131">ในตัวอย่างนี้ ถ้าบทบาทข้อมูล `"Gradient"` ประกอบด้วยข้อมูลแล้ว กฏจะถูกนำไปใช้กับคุณสมบัติ `"fill"`</span><span class="sxs-lookup"><span data-stu-id="3c54e-131">In this example, if data role `"Gradient"` contains data, the rule is applied for the `"fill"` property.</span></span>

<span data-ttu-id="3c54e-132">ตัวอย่างของบทบาทข้อมูลที่ทริกเกอร์กฎ การใส่สีพื้นหลัง (`the last item`) จะแสดงในโค้ดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3c54e-132">An example of the data role that triggers the fill rule (`the last item`) is shown in the following code:</span></span>

```json
{
    "dataRoles": [
            {
                "name": "Category",
                "kind": "Grouping",
                "displayName": "Details",
                "displayNameKey": "Role_DisplayName_Details"
            },
            {
                "name": "Series",
                "kind": "Grouping",
                "displayName": "Legend",
                "displayNameKey": "Role_DisplayName_Legend"
            },
            {
                "name": "Gradient",
                "kind": "Measure",
                "displayName": "Color saturation",
                "displayNameKey": "Role_DisplayName_Gradient"
            }
    ]
}
```

## <a name="the-enumerateobjectinstances-method"></a><span data-ttu-id="3c54e-133">เมธอด enumerateObjectInstances</span><span class="sxs-lookup"><span data-stu-id="3c54e-133">The enumerateObjectInstances method</span></span>

<span data-ttu-id="3c54e-134">ในการใช้ออบเจ็กต์อย่างมีประสิทธิภาพ คุณจะต้องมีฟังก์ชันในวิชวลแบบกำหนดเองของคุณที่เรียกว่า `enumerateObjectInstances`</span><span class="sxs-lookup"><span data-stu-id="3c54e-134">To use objects effectively, you need a function in your custom visual called `enumerateObjectInstances`.</span></span> <span data-ttu-id="3c54e-135">ฟังก์ชันนี้จะเติมข้อมูลในบานหน้าต่างคุณสมบัติที่มีออบเจ็กต์และจะกำหนดตำแหน่งที่ออบเจ็กต์ของคุณควรถูกผูกไว้ภายใน dataView</span><span class="sxs-lookup"><span data-stu-id="3c54e-135">This function populates the property pane with objects and also determines where your objects should be bound within the dataView.</span></span>  

<span data-ttu-id="3c54e-136">นี่คือลักษณะการตั้งค่าทั่วไป:</span><span class="sxs-lookup"><span data-stu-id="3c54e-136">Here is what a typical setup looks like:</span></span>

```typescript
public enumerateObjectInstances(options: EnumerateVisualObjectInstancesOptions): VisualObjectInstanceEnumeration {
    let objectName: string = options.objectName;
    let objectEnumeration: VisualObjectInstance[] = [];

    switch( objectName ) {
        case 'myCustomObject':
            objectEnumeration.push({
                objectName: objectName,
                properties: { ... },
                selector: { ... }
            });
            break;
    };

    return objectEnumeration;
}
```

### <a name="properties"></a><span data-ttu-id="3c54e-137">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="3c54e-137">Properties</span></span>

<span data-ttu-id="3c54e-138">คุณสมบัติใน `enumerateObjectInstances` จะสะท้อนคุณสมบัติที่คุณกำหนดไว้ในความสามารถของคุณ</span><span class="sxs-lookup"><span data-stu-id="3c54e-138">The properties in `enumerateObjectInstances` reflect the properties that you defined in your capabilities.</span></span> <span data-ttu-id="3c54e-139">สำหรับตัวอย่าง ให้ไปที่ส่วนท้ายของบทความนี้</span><span class="sxs-lookup"><span data-stu-id="3c54e-139">For an example, go to the end of this article.</span></span>

### <a name="objects-selector"></a><span data-ttu-id="3c54e-140">ตัวเลือกวัตถุ</span><span class="sxs-lookup"><span data-stu-id="3c54e-140">Objects selector</span></span>

<span data-ttu-id="3c54e-141">ตัวเลือกใน `enumerateObjectInstances` กำหนดตำแหน่งที่แต่ละออบเจ็กต์จะถูกผูกไว้ใน dataView</span><span class="sxs-lookup"><span data-stu-id="3c54e-141">The selector in `enumerateObjectInstances` determines where each object is bound in the dataView.</span></span> <span data-ttu-id="3c54e-142">มีสี่ตัวเลือกที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="3c54e-142">There are four distinct options.</span></span>

#### <a name="static"></a><span data-ttu-id="3c54e-143">คงที่</span><span class="sxs-lookup"><span data-stu-id="3c54e-143">static</span></span>

<span data-ttu-id="3c54e-144">ออบเจ็กต์นี้ถูกผูกกับเมตาดาต้า `dataviews[index].metadata.objects` ดังที่แสดงไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="3c54e-144">This object is bound to metadata `dataviews[index].metadata.objects`, as shown here.</span></span>

```typescript
selector: null
```

#### <a name="columns"></a><span data-ttu-id="3c54e-145">คอลัมน์</span><span class="sxs-lookup"><span data-stu-id="3c54e-145">columns</span></span>

<span data-ttu-id="3c54e-146">ออบเจ็กต์นี้จะผูกกับคอลัมน์ที่มีการจับคู่ `QueryName`</span><span class="sxs-lookup"><span data-stu-id="3c54e-146">This object is bound to columns with the matching `QueryName`.</span></span>

```typescript
selector: {
    metadata: 'QueryName'
}
```

#### <a name="selector"></a><span data-ttu-id="3c54e-147">ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="3c54e-147">selector</span></span>

<span data-ttu-id="3c54e-148">ออบเจ็กต์นี้จะผูกกับองค์ประกอบที่คุณได้สร้าง `selectionID` ขึ้น</span><span class="sxs-lookup"><span data-stu-id="3c54e-148">This object is bound to the element that you created a `selectionID` for.</span></span> <span data-ttu-id="3c54e-149">ในตัวอย่างนี้ ให้สมมติว่าเราได้สร้าง `selectionID` ขึ้นสำหรับบางจุดข้อมูล และเราจะวนลูปผ่านจุดข้อมูลดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="3c54e-149">In this example, let's assume that we've created `selectionID`s for some data points, and that we're looping through them.</span></span>

```typescript
for (let dataPoint in dataPoints) {
    ...
    selector: dataPoint.selectionID.getSelector()
}
```

#### <a name="scope-identity"></a><span data-ttu-id="3c54e-150">ข้อมูลเฉพาะตัวของขอบเขต</span><span class="sxs-lookup"><span data-stu-id="3c54e-150">Scope identity</span></span>

<span data-ttu-id="3c54e-151">ออบเจ็กต์นี้จะผูกกับค่าเฉพาะที่จุดตัดของกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="3c54e-151">This object is bound to particular values at the intersection of groups.</span></span> <span data-ttu-id="3c54e-152">ตัวอย่างเช่น ถ้าคุณมีข้อมูลจัดกลุ่ม `["Jan", "Feb", "March", ...]` และชุดข้อมูล `["Small", "Medium", "Large"]` คุณอาจต้องการให้มีออบเจ็กต์บนจุดตัดของค่าที่ตรงกับ `Feb` และ `Large`</span><span class="sxs-lookup"><span data-stu-id="3c54e-152">For example, if you have categories `["Jan", "Feb", "March", ...]` and series `["Small", "Medium", "Large"]`, you might want to have an object at the intersection of values that match `Feb` and `Large`.</span></span> <span data-ttu-id="3c54e-153">เมื่อต้องการทำเช่นนี้ คุณจะได้รับค่า `DataViewScopeIdentity` ทั้งสองคอลัมน์ ให้ส่งค่าเหล่านั้นไปยังตัวแปร `identities` และใช้ไวยากรณ์นี้กับตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="3c54e-153">To accomplish this, you could get the `DataViewScopeIdentity` of both columns, push them to variable `identities`, and use this syntax with the selector.</span></span>

```typescript
selector: {
    data: <DataViewScopeIdentity[]>identities
}
```

##### <a name="example"></a><span data-ttu-id="3c54e-154">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3c54e-154">Example</span></span>

<span data-ttu-id="3c54e-155">ตัวอย่างต่อไปนี้แสดงให้เห็นว่า objectEnumeration หนึ่งออบเจ็กต์จะมองหาออบเจ็กต์ customColor ที่มีหนึ่งคุณสมบัติ *การใส่สีพื้นหลัง* หนึ่งค่า</span><span class="sxs-lookup"><span data-stu-id="3c54e-155">The following example shows what one objectEnumeration would look like for a customColor object with one property, *fill*.</span></span> <span data-ttu-id="3c54e-156">เราต้องการให้ออบเจ็กต์นี้ผูกไว้กับ `dataViews[index].metadata.objects` แบบสแตติก ตามที่แสดง:</span><span class="sxs-lookup"><span data-stu-id="3c54e-156">We want this object bound statically to `dataViews[index].metadata.objects`, as shown:</span></span>

```typescript
objectEnumeration.push({
    objectName: "customColor",
    displayName: "Custom Color",
    properties: {
        fill: {
            solid: {
                color: dataPoint.color
            }
        }
    },
    selector: null
});
```
