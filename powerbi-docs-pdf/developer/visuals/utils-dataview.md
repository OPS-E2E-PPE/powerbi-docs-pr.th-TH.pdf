---
title: บทนำสู่การใช้งานยูทิลิตี้มุมมองข้อมูลของวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการใช้ยูทิลิตี้ SVG เพื่อลดความซับซ้อนของการแยกวิเคราะห์วัตถุ DataView สำหรับวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
manager: rkarlin
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: reference
ms.date: 06/18/2019
ms.openlocfilehash: 3c54333c35809ab272c065973d4d948e1ac37a8b
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887833"
---
# <a name="dataviewutils"></a><span data-ttu-id="2c454-104">DataViewUtils</span><span class="sxs-lookup"><span data-stu-id="2c454-104">DataViewUtils</span></span>

<span data-ttu-id="2c454-105">`DataViewUtils` เป็นชุดฟังก์ชันและคลาสเพื่อลดความซับซ้อนในการวิเคราะห์คำของออบเจ็กต์ DataView สำหรับวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="2c454-105">The `DataViewUtils` is a set of functions and classes to simplify parsing of the DataView object for Power BI visuals</span></span>

## <a name="installation"></a><span data-ttu-id="2c454-106">การติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="2c454-106">Installation</span></span>

<span data-ttu-id="2c454-107">หากต้องการติดตั้งแพ็คเกจ คุณควรเรียกใช้คำสั่งต่อไปนี้ในไดเรกทอรีด้วยวิชวลของแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2c454-107">To install the package, you should run the following command in the directory with your current custom visual:</span></span>

<span data-ttu-id="2c454-108">npm ติดตั้ง powerbi-visuals-utils-dataviewutils --บันทึก คำสั่งนี้ติดตั้งแพคเกจและเพิ่มแพคเกจ โดยขึ้นอยู่กับแพคเกจ json ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2c454-108">npm install powerbi-visuals-utils-dataviewutils --save This command installs the package and adds a package as a dependency to your package.json</span></span>

## <a name="dataviewwildcard"></a><span data-ttu-id="2c454-109">DataViewWildcard</span><span class="sxs-lookup"><span data-stu-id="2c454-109">DataViewWildcard</span></span>

<span data-ttu-id="2c454-110">`DataViewWildcard`มี`createDataViewWildcardSelector`ฟังก์ชันเพื่อสนับสนุนการจัดรูปแบบตามเงื่อนไข[ของคุณสมบัติ](conditional-format.md#define-how-conditional-formatting-behaves)</span><span class="sxs-lookup"><span data-stu-id="2c454-110">`DataViewWildcard` provides the `createDataViewWildcardSelector` function to support a property's [conditional formatting](conditional-format.md#define-how-conditional-formatting-behaves).</span></span>

<span data-ttu-id="2c454-111">`createDataViewWildcardSelector`ส่งคืนตัวเลือกที่จำเป็นสำหรับการกำหนดวิธีการใช้รายการการจัดรูปแบบตามเงื่อนไขในบานหน้าต่างรูปแบบ โดยยึดตาม `dataviewWildcardMatchingOption (InstancesAndTotals (default), InstancesOnly, TotalsOnly)`</span><span class="sxs-lookup"><span data-stu-id="2c454-111">`createDataViewWildcardSelector` returns a selector required for defining how the conditional formatting entry in the format pane will be applied, based on `dataviewWildcardMatchingOption (InstancesAndTotals (default), InstancesOnly, TotalsOnly)`.</span></span>

<span data-ttu-id="2c454-112">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-112">Example:</span></span>

 ```typescript
import { dataViewWildcard } from "powerbi-visuals-utils-dataviewutils";

let selector = dataViewWildcard.createDataViewWildcardSelector(dataViewWildcard.DataViewWildcardMatchingOption.InstancesAndTotals);
// returns {data: [{dataViewWildcard:{matchingOption: 0}}]};

```

## <a name="datarolehelper"></a><span data-ttu-id="2c454-113">DataRoleHelper</span><span class="sxs-lookup"><span data-stu-id="2c454-113">DataRoleHelper</span></span>

<span data-ttu-id="2c454-114">`DataRoleHelper` มีฟังก์ชันในการตรวจสอบบทบาทของวัตถุ dataView</span><span class="sxs-lookup"><span data-stu-id="2c454-114">The `DataRoleHelper` provides functions to check roles of the dataView object.</span></span>

<span data-ttu-id="2c454-115">โมดูลมอบฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2c454-115">The module provides the following functions:</span></span>

### <a name="getmeasureindexofrole"></a><span data-ttu-id="2c454-116">getMeasureIndexOfRole</span><span class="sxs-lookup"><span data-stu-id="2c454-116">getMeasureIndexOfRole</span></span>

<span data-ttu-id="2c454-117">ฟังก์ชันนี้จะค้นหาหน่วยวัดตามชื่อบทบาทและส่งกลับดัชนี</span><span class="sxs-lookup"><span data-stu-id="2c454-117">This function finds the measure by role name and returns its index.</span></span>

```typescript
function getMeasureIndexOfRole(grouped: DataViewValueColumnGroup[], roleName: string): number;
```

<span data-ttu-id="2c454-118">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-118">Example:</span></span>

```typescript
import powerbi from "powerbi-visuals-api";
import DataViewValueColumnGroup = powerbi.DataViewValueColumnGroup;
import { dataRoleHelper } from "powerbi-visuals-utils-dataviewutils";
// ...

// This object is actually a part of the dataView object.
let columnGroup: DataViewValueColumnGroup[] = [{
    values: [
        {
            source: {
                displayName: "Microsoft",
                roles: {
                    "company": true
                }
            },
            values: []
        },
        {
            source: {
                displayName: "Power BI",
                roles: {
                    "product": true
                }
            },
            values: []
        }
    ]
}];

dataRoleHelper.getMeasureIndexOfRole(columnGroup, "product");

// returns: 1
```

### <a name="getcategoryindexofrole"></a><span data-ttu-id="2c454-119">getCategoryIndexOfRole</span><span class="sxs-lookup"><span data-stu-id="2c454-119">getCategoryIndexOfRole</span></span>

<span data-ttu-id="2c454-120">ฟังก์ชันนี้จะค้นหาประเภทตามชื่อบทบาทและส่งกลับดัชนี</span><span class="sxs-lookup"><span data-stu-id="2c454-120">This function finds the category by role name and returns its index.</span></span>

```typescript
function getCategoryIndexOfRole(categories: DataViewCategoryColumn[], roleName: string): number;
```

<span data-ttu-id="2c454-121">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-121">Example:</span></span>

```typescript
import powerbi from "powerbi-visuals-api";
import DataViewCategoryColumn = powerbi.DataViewCategoryColumn;
import { dataRoleHelper } from "powerbi-visuals-utils-dataviewutils";
// ...

// This object is actually a part of the dataView object.
let categoryGroup: DataViewCategoryColumn[] = [
    {
        source: {
            displayName: "Microsoft",
            roles: {
                "company": true
            }
        },
        values: []
    },
    {
        source: {
            displayName: "Power BI",
            roles: {
                "product": true
            }
        },
        values: []
    }
];

dataRoleHelper.getCategoryIndexOfRole(categoryGroup, "product");

// returns: 1
```

### <a name="hasrole"></a><span data-ttu-id="2c454-122">hasRole</span><span class="sxs-lookup"><span data-stu-id="2c454-122">hasRole</span></span>

<span data-ttu-id="2c454-123">ฟังก์ชันนี้จะตรวจสอบว่ามีการกำหนดบทบาทที่ให้ไว้ในเมตาดาต้าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2c454-123">This function checks if the provided role is defined in the metadata.</span></span>

```typescript
function hasRole(column: DataViewMetadataColumn, name: string): boolean;
```

<span data-ttu-id="2c454-124">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-124">Example:</span></span>

```typescript
import powerbi from "powerbi-visuals-api";
import DataViewMetadataColumn = powerbi.DataViewMetadataColumn;
import { dataRoleHelper } from "powerbi-visuals-utils-dataviewutils";

// This object is actually a part of the dataView object.
let metadata: DataViewMetadataColumn = {
    displayName: "Microsoft",
    roles: {
        "company": true
    }
};

DataRoleHelper.hasRole(metadata, "company");

// returns: true
```

### <a name="hasroleindataview"></a><span data-ttu-id="2c454-125">hasRoleInDataView</span><span class="sxs-lookup"><span data-stu-id="2c454-125">hasRoleInDataView</span></span>

<span data-ttu-id="2c454-126">ฟังก์ชันนี้จะตรวจสอบว่ามีการกำหนดบทบาทที่ให้ไว้ใน dataView หรือไม่</span><span class="sxs-lookup"><span data-stu-id="2c454-126">This function checks if the provided role is defined in the dataView.</span></span>

```typescript
function hasRoleInDataView(dataView: DataView, name: string): boolean;
```

<span data-ttu-id="2c454-127">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-127">Example:</span></span>

```typescript
import powerbi from "powerbi-visuals-api";
import DataView = powerbi.DataView;
import { dataRoleHelper } from "powerbi-visuals-utils-dataviewutils";

// This object is actually a part of the dataView object.
let dataView: DataView = {
    metadata: {
        columns: [
            {
                displayName: "Microsoft",
                roles: {
                    "company": true
                }
            },
            {
                displayName: "Power BI",
                roles: {
                    "product": true
                }
            }
        ]
    }
};

DataRoleHelper.hasRoleInDataView(dataView, "product");

// returns: true
```

### <a name="hasroleinvaluecolumn"></a><span data-ttu-id="2c454-128">hasRoleInValueColumn</span><span class="sxs-lookup"><span data-stu-id="2c454-128">hasRoleInValueColumn</span></span>

<span data-ttu-id="2c454-129">ฟังก์ชันนี้จะตรวจสอบว่ามีการกำหนดบทบาทที่ให้ไว้ในคอลัมน์ค่าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2c454-129">This function checks if the provided role is defined in the value column.</span></span>

```typescript
function hasRoleInValueColumn(valueColumn: DataViewValueColumn, name: string): boolean;
```

<span data-ttu-id="2c454-130">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-130">Example:</span></span>

```typescript
import powerbi from "powerbi-visuals-api";
import DataViewValueColumn = powerbi.DataViewValueColumn;
import { dataRoleHelper } from "powerbi-visuals-utils-dataviewutils";

// This object is actually a part of the dataView object.
let valueColumn: DataViewValueColumn = {
    source: {
        displayName: "Microsoft",
        roles: {
            "company": true
        }
    },
    values: []
};

dataRoleHelper.hasRoleInValueColumn(valueColumn, "company");

// returns: true
```

## <a name="dataviewobjects"></a><span data-ttu-id="2c454-131">DataViewObjects</span><span class="sxs-lookup"><span data-stu-id="2c454-131">DataViewObjects</span></span>

<span data-ttu-id="2c454-132">`DataViewObjects` มีฟังก์ชันในการแยกค่าของวัตถุ</span><span class="sxs-lookup"><span data-stu-id="2c454-132">The `DataViewObjects` provides functions to extract values of the objects.</span></span>

<span data-ttu-id="2c454-133">โมดูลมอบฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2c454-133">The module provides the following functions:</span></span>

### <a name="getvalue"></a><span data-ttu-id="2c454-134">getValue</span><span class="sxs-lookup"><span data-stu-id="2c454-134">getValue</span></span>

<span data-ttu-id="2c454-135">ฟังก์ชันนี้ส่งกลับค่าของวัตถุที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="2c454-135">This function returns the value of the given object.</span></span>

```typescript
function getValue<T>(objects: DataViewObjects, propertyId: DataViewObjectPropertyIdentifier, defaultValue?: T): T;
```

<span data-ttu-id="2c454-136">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-136">Example:</span></span>

```typescript
import powerbi from "powerbi-visuals-api";
import DataViewObjectPropertyIdentifier = powerbi.DataViewObjectPropertyIdentifier;
import { dataViewObjects } from "powerbi-visuals-utils-dataviewutils";

let property: DataViewObjectPropertyIdentifier = {
    objectName: "microsoft",
    propertyName: "bi"
};

// This object is actually a part of the dataView object.
let objects: powerbi.DataViewObjects = {
    "microsoft": {
        "windows": 5,
        "bi": "Power"
    }
};

dataViewObjects.getValue(objects, property);

// returns: Power
```

### <a name="getobject"></a><span data-ttu-id="2c454-137">getObject</span><span class="sxs-lookup"><span data-stu-id="2c454-137">getObject</span></span>

<span data-ttu-id="2c454-138">ฟังก์ชันนี้ส่งกลับวัตถุของวัตถุที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="2c454-138">This function returns an object of the given object.</span></span>

```typescript
function getObject(objects: DataViewObjects, objectName: string, defaultValue?: IDataViewObject): IDataViewObject;
```

<span data-ttu-id="2c454-139">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-139">Example:</span></span>

```typescript
import { dataViewObjects } from "powerbi-visuals-utils-dataviewutils";

// This object is actually a part of the dataView object.
let objects: powerbi.DataViewObjects = {
    "microsoft": {
        "windows": 5,
        "bi": "Power"
    }
};

dataViewObjects.getObject(objects, "microsoft");

/* returns: {
    "bi": "Power",
    "windows": 5

}*/
```

### <a name="getfillcolor"></a><span data-ttu-id="2c454-140">getFillColor</span><span class="sxs-lookup"><span data-stu-id="2c454-140">getFillColor</span></span>

<span data-ttu-id="2c454-141">ฟังก์ชันนี้ส่งกลับสีทึบของวัตถุ</span><span class="sxs-lookup"><span data-stu-id="2c454-141">This function returns a solid color of the objects.</span></span>

```typescript
function getFillColor(objects: DataViewObjects, propertyId: DataViewObjectPropertyIdentifier, defaultColor?: string): string;
```

<span data-ttu-id="2c454-142">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-142">Example:</span></span>

```typescript
import powerbi from "powerbi-visuals-api";
import DataViewObjectPropertyIdentifier = powerbi.DataViewObjectPropertyIdentifier;
import { dataViewObjects } from "powerbi-visuals-utils-dataviewutils";

let property: DataViewObjectPropertyIdentifier = {
    objectName: "power",
    propertyName: "fillColor"
};

// This object is actually part of the dataView object.
let objects: powerbi.DataViewObjects = {
    "power": {
        "fillColor": {
            "solid": {
                "color": "yellow"
            }
        },
        "bi": "Power"
    }
};

dataViewObjects.getFillColor(objects, property);

// returns: yellow
```

### <a name="getcommonvalue"></a><span data-ttu-id="2c454-143">getCommonValue</span><span class="sxs-lookup"><span data-stu-id="2c454-143">getCommonValue</span></span>

<span data-ttu-id="2c454-144">ฟังก์ชันนี้เป็นฟังก์ชันสากลสำหรับการเรียกใช้สีหรือค่าของวัตถุที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="2c454-144">This function is a universal function for retrieving the color or value of a given object.</span></span>

```typescript
function getCommonValue(objects: DataViewObjects, propertyId: DataViewObjectPropertyIdentifier, defaultValue?: any): any;
```

<span data-ttu-id="2c454-145">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-145">Example:</span></span>

```typescript
import powerbi from "powerbi-visuals-api";
import DataViewObjectPropertyIdentifier = powerbi.DataViewObjectPropertyIdentifier;
import { dataViewObjects } from "powerbi-visuals-utils-dataviewutils";

let colorProperty: DataViewObjectPropertyIdentifier = {
    objectName: "power",
    propertyName: "fillColor"
};

let biProperty: DataViewObjectPropertyIdentifier = {
    objectName: "power",
    propertyName: "bi"
};

// This object is actually part of the dataView object.
let objects: powerbi.DataViewObjects = {
    "power": {
        "fillColor": {
            "solid": {
                "color": "yellow"
            }
        },
        "bi": "Power"
    }
};

dataViewObjects.getCommonValue(objects, colorProperty); // returns: yellow
dataViewObjects.getCommonValue(objects, biProperty); // returns: Power
```

## <a name="dataviewobject"></a><span data-ttu-id="2c454-146">DataViewObject</span><span class="sxs-lookup"><span data-stu-id="2c454-146">DataViewObject</span></span>

<span data-ttu-id="2c454-147">`DataViewObject` มีฟังก์ชันในการแยกค่าของวัตถุ</span><span class="sxs-lookup"><span data-stu-id="2c454-147">The `DataViewObject` provides functions to extract value of the object.</span></span>

<span data-ttu-id="2c454-148">โมดูลมอบฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2c454-148">The module provides the following functions:</span></span>

### <a name="getvalue"></a><span data-ttu-id="2c454-149">getValue</span><span class="sxs-lookup"><span data-stu-id="2c454-149">getValue</span></span>

<span data-ttu-id="2c454-150">ฟังก์ชันนี้ส่งกลับค่าของวัตถุตามชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="2c454-150">This function returns a value of the object by property name.</span></span>

```typescript
function getValue<T>(object: IDataViewObject, propertyName: string, defaultValue?: T): T;
```

<span data-ttu-id="2c454-151">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-151">Example:</span></span>

```typescript
import { dataViewObject } from "powerbi-visuals-utils-dataviewutils";

// This object is actually a part of the dataView object.
let object: powerbi.DataViewObject = {
    "windows": 5,
    "microsoft": "Power BI"
};

dataViewObject.getValue(object, "microsoft");

// returns: Power BI
```

### <a name="getfillcolorbypropertyname"></a><span data-ttu-id="2c454-152">getFillColorByPropertyName</span><span class="sxs-lookup"><span data-stu-id="2c454-152">getFillColorByPropertyName</span></span>

<span data-ttu-id="2c454-153">ฟังก์ชันนี้ส่งกลับสีทึบของวัตถุตามชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="2c454-153">This function returns a solid color of the object by property name.</span></span>

```typescript
function getFillColorByPropertyName(object: IDataViewObject, propertyName: string, defaultColor?: string): string;
```

<span data-ttu-id="2c454-154">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-154">Example:</span></span>

```typescript
import { dataViewObject } from "powerbi-visuals-utils-dataviewutils";

// This object is actually a part of the dataView object.
let object: powerbi.DataViewObject = {
    "windows": 5,
    "fillColor": {
        "solid": {
            "color": "green"
        }
    }
};

dataViewObject.getFillColorByPropertyName(object, "fillColor");

// returns: green
```

### <a name="converterhelper"></a><span data-ttu-id="2c454-155">converterHelper</span><span class="sxs-lookup"><span data-stu-id="2c454-155">converterHelper</span></span>

<span data-ttu-id="2c454-156">`converterHelper` มีฟังก์ชันในการตรวจสอบคุณสมบัติของ dataView</span><span class="sxs-lookup"><span data-stu-id="2c454-156">The `converterHelper` provides functions to check properties of the dataView.</span></span>

<span data-ttu-id="2c454-157">โมดูลมอบฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2c454-157">The module provides the following functions:</span></span>

### <a name="categoryisalsoseriesrole"></a><span data-ttu-id="2c454-158">categoryIsAlsoSeriesRole</span><span class="sxs-lookup"><span data-stu-id="2c454-158">categoryIsAlsoSeriesRole</span></span>

<span data-ttu-id="2c454-159">ฟังก์ชันนี้จะตรวจสอบว่าประเภทคือชุดข้อมูลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2c454-159">This function checks if the category is also series.</span></span>

```typescript
function categoryIsAlsoSeriesRole(dataView: DataViewCategorical, seriesRoleName: string, categoryRoleName: string): boolean;
```

<span data-ttu-id="2c454-160">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-160">Example:</span></span>

```typescript
import powerbi from "powerbi-visuals-api";
import DataViewCategorical = powerbi.DataViewCategorical;
import { converterHelper } from "powerbi-visuals-utils-dataviewutils";
// ...


// This object is actually part of the dataView object.
let categorical: DataViewCategorical = {
    categories: [{
        source: {
            displayName: "Microsoft",
            roles: {
                "power": true,
                "bi": true
            }
        },
        values: []
    }]
};

converterHelper.categoryIsAlsoSeriesRole(categorical, "power", "bi");

// returns: true
```

### <a name="getseriesname"></a><span data-ttu-id="2c454-161">getSeriesName</span><span class="sxs-lookup"><span data-stu-id="2c454-161">getSeriesName</span></span>

<span data-ttu-id="2c454-162">ฟังก์ชันนี้จะส่งกลับชื่อของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2c454-162">This function returns a name of the series.</span></span>

```typescript
function getSeriesName(source: DataViewMetadataColumn): PrimitiveValue;
```

<span data-ttu-id="2c454-163">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-163">Example:</span></span>

```typescript
import powerbi from "powerbi-visuals-api";
import DataViewMetadataColumn = powerbi.DataViewMetadataColumn;
import { converterHelper } from "powerbi-visuals-utils-dataviewutils";

// This object is actually a part of the dataView object.
let metadata: DataViewMetadataColumn = {
    displayName: "Microsoft",
    roles: {
        "power": true,
        "bi": true
    },
    groupName: "Power BI"
};

converterHelper.getSeriesName(metadata);

// returns: Power BI
```

### <a name="isimageurlcolumn"></a><span data-ttu-id="2c454-164">isImageUrlColumn</span><span class="sxs-lookup"><span data-stu-id="2c454-164">isImageUrlColumn</span></span>

<span data-ttu-id="2c454-165">ฟังก์ชันนี้จะตรวจสอบว่าคอลัมน์มี url ของรูปหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2c454-165">This function checks if the column contains an image url.</span></span>

```typescript
function isImageUrlColumn(column: DataViewMetadataColumn): boolean;
```

<span data-ttu-id="2c454-166">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-166">Example:</span></span>

```typescript
import powerbi from "powerbi-visuals-api";
import DataViewMetadataColumn = powerbi.DataViewMetadataColumn;
import { converterHelper } from "powerbi-visuals-utils-dataviewutils";

// This object is actually a part of the dataView object.
let metadata: DataViewMetadataColumn = {
    displayName: "Microsoft",
    type: {
        misc: {
            imageUrl: true
        }
    }
};

converterHelper.isImageUrlColumn(metadata);

// returns: true
```

### <a name="isweburlcolumn"></a><span data-ttu-id="2c454-167">isWebUrlColumn</span><span class="sxs-lookup"><span data-stu-id="2c454-167">isWebUrlColumn</span></span>

<span data-ttu-id="2c454-168">ฟังก์ชันนี้จะตรวจสอบว่าคอลัมน์มี url ของเว็บหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2c454-168">This function checks if the column contains a web url.</span></span>

```typescript
function isWebUrlColumn(column: DataViewMetadataColumn): boolean;
```

<span data-ttu-id="2c454-169">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-169">Example:</span></span>

```typescript
import powerbi from "powerbi-visuals-api";
import DataViewMetadataColumn = powerbi.DataViewMetadataColumn;
import { converterHelper } from "powerbi-visuals-utils-dataviewutils";

// This object is actually a part of the dataView object.
let metadata: DataViewMetadataColumn = {
    displayName: "Microsoft",
    type: {
        misc: {
            webUrl: true
        }
    }
};

converterHelper.isWebUrlColumn(metadata);

// returns: true
```

### <a name="hasimageurlcolumn"></a><span data-ttu-id="2c454-170">hasImageUrlColumn</span><span class="sxs-lookup"><span data-stu-id="2c454-170">hasImageUrlColumn</span></span>

<span data-ttu-id="2c454-171">ฟังก์ชันนี้จะตรวจสอบว่า dataView มีคอลัมน์ที่มี url ของรูป</span><span class="sxs-lookup"><span data-stu-id="2c454-171">This function checks if the dataView has a column with image url.</span></span>

```typescript
function hasImageUrlColumn(dataView: DataView): boolean;
```

<span data-ttu-id="2c454-172">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-172">Example:</span></span>

```typescript
import DataView = powerbi.DataView;
import converterHelper = powerbi.extensibility.utils.dataview.converterHelper;

// This object is actually part of the dataView object.
let dataView: DataView = {
    metadata: {
        columns: [
            {
                displayName: "Microsoft"
            },
            {
                displayName: "Power BI",
                type: {
                    misc: {
                        imageUrl: true
                    }
                }
            }
        ]
    }
};

converterHelper.hasImageUrlColumn(dataView);

// returns: true
```

## <a name="dataviewobjectsparser"></a><span data-ttu-id="2c454-173">DataViewObjectsParser</span><span class="sxs-lookup"><span data-stu-id="2c454-173">DataViewObjectsParser</span></span>

<span data-ttu-id="2c454-174">`DataViewObjectsParser` มีวิธีที่ง่ายที่สุดในการแยกวิเคราะห์คุณสมบัติของแผงการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="2c454-174">The `DataViewObjectsParser` provides the simplest way to parse properties of the formatting panel.</span></span>

<span data-ttu-id="2c454-175">คลาสมีวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2c454-175">The class provides the following methods:</span></span>

### <a name="getdefault"></a><span data-ttu-id="2c454-176">getDefault</span><span class="sxs-lookup"><span data-stu-id="2c454-176">getDefault</span></span>

<span data-ttu-id="2c454-177">วิธีการแบบคงที่นี้ส่งกลับอินสแตนซ์ของ DataViewObjectsParser</span><span class="sxs-lookup"><span data-stu-id="2c454-177">This static method returns an instance of DataViewObjectsParser.</span></span>

```typescript
static getDefault(): DataViewObjectsParser;
```

<span data-ttu-id="2c454-178">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-178">Example:</span></span>

```typescript
import { dataViewObjectsParser } from "powerbi-visuals-utils-dataviewutils";
// ...

dataViewObjectsParser.getDefault();

// returns: an instance of the DataViewObjectsParser
```

### <a name="parse"></a><span data-ttu-id="2c454-179">แยกวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="2c454-179">parse</span></span>

<span data-ttu-id="2c454-180">วิธีนี้แยกวิเคราะห์คุณสมบัติของแผงการจัดรูปแบบและส่งกลับตัวอย่างของ `DataViewObjectsParser`</span><span class="sxs-lookup"><span data-stu-id="2c454-180">This method parses properties of the formatting panel and returns an instance of `DataViewObjectsParser`.</span></span>

```typescript
static parse<T extends DataViewObjectsParser>(dataView: DataView): T;
```

<span data-ttu-id="2c454-181">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-181">Example:</span></span>

```typescript
import powerbi from "powerbi-visuals-api";
import IVisual = powerbi.extensibility.IVisual;
import VisualUpdateOptions = powerbi.extensibility.visual.VisualUpdateOptions;
import { dataViewObjectsParser } from "powerbi-visuals-utils-dataviewutils";

/**
 * This class describes formatting panel properties.
 * Name of the property should match its name described in the capabilities.
 */
class DataPointProperties {
    public fillColor: string = "red"; // This value is a default value of the property.
}

class PropertiesParser extends dataViewObjectsParser.DataViewObjectsParser {
    /**
     * This property describes a group of properties.
     */
    public dataPoint: DataPointProperties = new DataPointProperties();
}

export class YourVisual extends IVisual {
    // implementation of the IVisual.

    private propertiesParser: PropertiesParser;

    public update(options: VisualUpdateOptions): void {
        // Parses properties.
        this.propertiesParser = PropertiesParser.parse<PropertiesParser>(options.dataViews[0]);

        // You can use the properties after parsing
        console.log(this.propertiesParser.dataPoint.fillColor); // returns "red" as default value, it will be updated automatically after any change of the formatting panel.
    }
}
```

## <a name="enumerateobjectinstances"></a><span data-ttu-id="2c454-182">enumerateObjectInstances</span><span class="sxs-lookup"><span data-stu-id="2c454-182">enumerateObjectInstances</span></span>

<span data-ttu-id="2c454-183">วิธีการแบบคงที่นี้จะระบุคุณสมบัติและส่งกลับตัวอย่างของ `VisualObjectInstanceEnumeration`</span><span class="sxs-lookup"><span data-stu-id="2c454-183">This static method enumerates properties and returns an instance of `VisualObjectInstanceEnumeration`.</span></span>

<span data-ttu-id="2c454-184">ดำเนินการในวิธีการ `enumerateObjectInstances` ของการแสดงผล</span><span class="sxs-lookup"><span data-stu-id="2c454-184">Execute it in `enumerateObjectInstances` method of the visual.</span></span>

```typescript
static enumerateObjectInstances(dataViewObjectParser: dataViewObjectsParser.DataViewObjectsParser, options: EnumerateVisualObjectInstancesOptions): VisualObjectInstanceEnumeration;
```

<span data-ttu-id="2c454-185">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2c454-185">Example:</span></span>

```typescript
import powerbi from "powerbi-visuals-api";
import IVisual = powerbi.extensibility.IVisual;
import EnumerateVisualObjectInstancesOptions = powerbi.EnumerateVisualObjectInstancesOptions;
import VisualObjectInstanceEnumeration = powerbi.VisualObjectInstanceEnumeration;
import VisualUpdateOptions = powerbi.extensibility.visual.VisualUpdateOptions;
import { dataViewObjectsParser } from "powerbi-visuals-utils-dataviewutils";

/**
 * This class describes formatting panel properties.
 * Name of the property should match its name described in the capabilities.
 */
class DataPointProperties {
    public fillColor: string = "red";
}

class PropertiesParser extends dataViewObjectsParser.DataViewObjectsParser {
    /**
     * This property describes a group of properties.
     */
    public dataPoint: DataPointProperties = new DataPointProperties();
}

export class YourVisual extends IVisual {
    // implementation of the IVisual.

    private propertiesParser: PropertiesParser;

    public update(options: VisualUpdateOptions): void {
        // Parses properties.
        this.propertiesParser = PropertiesParser.parse<PropertiesParser>(options.dataViews[0]);
    }

    /**
     * This method will be executed only if the formatting panel is open.
     */
    public enumerateObjectInstances(options: EnumerateVisualObjectInstancesOptions): VisualObjectInstanceEnumeration {
        return PropertiesParser.enumerateObjectInstances(this.propertiesParser, options);
    }
}
```
