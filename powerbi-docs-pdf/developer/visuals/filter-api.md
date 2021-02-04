---
title: API ตัวกรองวิชวลสำหรับวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายถึงวิธีการที่วิชวล Power BI สามารถกรองวิชวลอื่น ๆ ได้อย่างไร เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: how-to
ms.date: 06/18/2019
ms.openlocfilehash: c03c64c2835ff8bf0b0f1ad3bd555da94aaf3126
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888753"
---
# <a name="the-visual-filters-api-in-power-bi-visuals"></a><span data-ttu-id="ce586-104">API ตัวกรองวิชวลในวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="ce586-104">The Visual Filters API in Power BI visuals</span></span>

<span data-ttu-id="ce586-105">API ตัวกรองวิชวลช่วยให้คุณสามารถกรองข้อมูลในวิชวล Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="ce586-105">The Visual Filters API allows you to filter data in Power BI visuals.</span></span> <span data-ttu-id="ce586-106">ความแตกต่างที่สำคัญจากการเลือกแบบอื่นคือวิชวลอื่น ๆ จะถูกกรองในทุกทางแม้จะมีการไฮไลต์ด้วยการสนับสนุนจากวิชวลอื่น</span><span class="sxs-lookup"><span data-stu-id="ce586-106">The main difference from other selections is that other visuals will be filtered in any way, despite highlight support by other visual.</span></span>

<span data-ttu-id="ce586-107">หากต้องการเปิดใช้งานการกรองสำหรับวิชวล ควรมีวัตถุ `filter` ในส่วน `general` ของ  *โค้ด capabilities.json*</span><span class="sxs-lookup"><span data-stu-id="ce586-107">To enable filtering for the visual, it should contain a `filter` object in the `general` section of *capabilities.json* code.</span></span>

```json
"objects": {
        "general": {
            "displayName": "General",
            "displayNameKey": "formattingGeneral",
            "properties": {
                "filter": {
                    "type": {
                        "filter": true
                    }
                }
            }
        }
    }
```

<span data-ttu-id="ce586-108">อินเทอร์เฟซของ API ตัวกรองวิชวล[พร้อมใช้งานในแพคเกจแบบจำลอง powerbi](https://www.npmjs.com/package/powerbi-models)</span><span class="sxs-lookup"><span data-stu-id="ce586-108">Visual Filters API interfaces are available in the [powerbi-models](https://www.npmjs.com/package/powerbi-models) package.</span></span> <span data-ttu-id="ce586-109">นอกจากนี้ แพคเกจยังประกอบด้วยคลาสที่จะสร้างอินสแตนซ์ตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="ce586-109">The package also contains classes to create filter instances.</span></span>

```cmd
npm install powerbi-models --save
```

<span data-ttu-id="ce586-110">ถ้าคุณใช้เครื่องมือเวอร์ชันเก่ากว่า (เวอร์ชันก่อนหน้า 3.x.x) คุณควรรวม `powerbi-models` ไว้ในแพคเกจวิชวลด้วย</span><span class="sxs-lookup"><span data-stu-id="ce586-110">If you use an older (earlier than 3.x.x) version of the tools, you should include `powerbi-models` in the visuals package.</span></span> <span data-ttu-id="ce586-111">สำหรับข้อมูลเพิ่มเติม โปรดดูคำแนะนำสั้น ๆ ในหัวข้อ [เพิ่ม API ตัวกรองขั้นสูงไปยังวิชวลที่กำหนดเอง](https://github.com/Microsoft/powerbi-visuals-sampleslicer/blob/master/doc/AddingAdvancedFilterAPI.md)</span><span class="sxs-lookup"><span data-stu-id="ce586-111">For more information, see the short guide, [Add the Advanced Filter API to the custom visual](https://github.com/Microsoft/powerbi-visuals-sampleslicer/blob/master/doc/AddingAdvancedFilterAPI.md).</span></span>

<span data-ttu-id="ce586-112">ตัวกรองทั้งหมดเป็นส่วนขยายอินเทอร์เฟซ `IFilter` ดังแสดงในโค้ดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ce586-112">All filters extend the `IFilter` interface, as shown in the following code:</span></span>

```typescript
export interface IFilter {
    $schema: string;
    target: IFilterTarget;
}
```
<span data-ttu-id="ce586-113">ที่ซึ่ง:</span><span class="sxs-lookup"><span data-stu-id="ce586-113">Where:</span></span>
* <span data-ttu-id="ce586-114">`target` เป็นคอลัมน์ตารางในแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ce586-114">`target` is the table column on the data source.</span></span>

## <a name="the-basic-filter-api"></a><span data-ttu-id="ce586-115">API ตัวกรองพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="ce586-115">The Basic Filter API</span></span>

<span data-ttu-id="ce586-116">อินเตอร์เฟซตัวกรองพื้นฐานแสดงในโค้ดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ce586-116">Basic filter interface is shown in the following code:</span></span>

```typescript
export interface IBasicFilter extends IFilter {
    operator: BasicFilterOperators;
    values: (string | number | boolean)[];
}
```

<span data-ttu-id="ce586-117">ที่ซึ่ง:</span><span class="sxs-lookup"><span data-stu-id="ce586-117">Where:</span></span>
* <span data-ttu-id="ce586-118">`operator` เป็นการแจกแจงที่มีค่า *In*, *NotIn* และ *All*</span><span class="sxs-lookup"><span data-stu-id="ce586-118">`operator` is an enumeration with the values *In*, *NotIn*, and *All*.</span></span>
* <span data-ttu-id="ce586-119">`values` เป็นค่าสำหรับเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="ce586-119">`values` are values for the condition.</span></span>

<span data-ttu-id="ce586-120">ตัวอย่างของตัวกรองพื้นฐาน:</span><span class="sxs-lookup"><span data-stu-id="ce586-120">Example of a basic filter:</span></span>

```typescript
let basicFilter = {
    target: {
        column: "Col1"
    },
    operator: "In",
    values: [1,2,3]
}
```

<span data-ttu-id="ce586-121">ตัวกรองหมายถึง "ให้ทุกแถวที่มี `col1` เท่ากับค่า 1, 2 หรือ 3 แก่ฉัน"</span><span class="sxs-lookup"><span data-stu-id="ce586-121">The filter means, "Give me all rows where `col1` equals the value 1, 2, or 3."</span></span>

<span data-ttu-id="ce586-122">SQL ที่เทียบเท่าคือ:</span><span class="sxs-lookup"><span data-stu-id="ce586-122">The SQL equivalent is:</span></span>

```sql
SELECT * FROM table WHERE col1 IN ( 1 , 2 , 3 )
```

<span data-ttu-id="ce586-123">เมื่อต้องการสร้างตัวกรอง คุณสามารถใช้คลาส BasicFilter ใน `powerbi-models`</span><span class="sxs-lookup"><span data-stu-id="ce586-123">To create a filter, you can use the BasicFilter class in `powerbi-models`.</span></span>

<span data-ttu-id="ce586-124">ถ้าคุณใช้เครื่องมือเวอร์ชันเก่ากว่า คุณควรมีอินสแตนซ์ของแบบจำลองในวัตถุหน้าต่างโดยใช้ `window['powerbi-models']` ดังที่แสดงในโค้ดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ce586-124">If you use an older version of the tool, you should get an instance of models in the window object by using `window['powerbi-models']`, as shown in the following code:</span></span>

```javascript
let categories: DataViewCategoricalColumn = this.dataView.categorical.categories[0];

let target: IFilterColumnTarget = {
    table: categories.source.queryName.substr(0, categories.source.queryName.indexOf('.')),
    column: categories.source.displayName
};

let values = [ 1, 2, 3 ];

let filter: IBasicFilter = new window['powerbi-models'].BasicFilter(target, "In", values);
```

<span data-ttu-id="ce586-125">วิชวลจะเรียกใช้ตัวกรองโดยใช้เมธอด applyJsonFilter() บนอินเตอร์เฟสโฮสต์ IVisualHost ซึ่งจัดเตรียมให้กับวิชวลในคอนสตรักเตอร์</span><span class="sxs-lookup"><span data-stu-id="ce586-125">The visual invokes the filter by using the applyJsonFilter() method on the host interface, IVisualHost, which is provided to the visual in the constructor.</span></span>

```typescript
visualHost.applyJsonFilter(filter, "general", "filter", FilterAction.merge);
```

## <a name="the-advanced-filter-api"></a><span data-ttu-id="ce586-126">API ตัวกรองขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="ce586-126">The Advanced Filter API</span></span>

<span data-ttu-id="ce586-127">[API ตัวกรองขั้นสูง](https://github.com/Microsoft/powerbi-models)เปิดใช้งานการเลือกจุดข้อมูลและคิวรีการกรองแบบไขว้วิชวลที่ซับซ้อนโดยยึดตามเกณฑ์หลายอย่าง เช่น *LessThan*, *Contains*, *Is*, *IsBlank* และอื่น ๆ)</span><span class="sxs-lookup"><span data-stu-id="ce586-127">The [Advanced Filter API](https://github.com/Microsoft/powerbi-models) enables complex cross-visual data-point selection and filtering queries that are based on multiple criteria, such as *LessThan*, *Contains*, *Is*, *IsBlank*, and so on).</span></span>

<span data-ttu-id="ce586-128">ตัวกรองได้รับการแนะนำใน Visuals API 1.7.0</span><span class="sxs-lookup"><span data-stu-id="ce586-128">The filter was introduced in Visuals API 1.7.0.</span></span>

<span data-ttu-id="ce586-129">API ตัวกรองขั้นสูงยังจำเป็นต้องมี `target` ที่มีชื่อ `table` และ `column`</span><span class="sxs-lookup"><span data-stu-id="ce586-129">The Advanced Filter API also requires `target` with a `table` and `column` name.</span></span> <span data-ttu-id="ce586-130">แต่ตัวดำเนินการของ API ตัวกรองขั้นสูงคือ *And* และ *Or*</span><span class="sxs-lookup"><span data-stu-id="ce586-130">But the Advanced Filter API operators are *And* and *Or*.</span></span> 

<span data-ttu-id="ce586-131">นอกจากนี้ ตัวกรองใช้เงื่อนไขกับอินเตอร์เฟสแทนที่จะเป็นค่า:</span><span class="sxs-lookup"><span data-stu-id="ce586-131">Additionally, the filter uses conditions instead of values with the interface:</span></span>

```typescript
interface IAdvancedFilterCondition {
    value: (string | number | boolean);
    operator: AdvancedFilterConditionOperators;
}
```

<span data-ttu-id="ce586-132">ตัวดำเนินการเงื่อนไขสำหรับพารามิเตอร์ `operator` คือ *None*, *LessThan*, *LessThanOrEqual*, *GreaterThan*, *GreaterThanOrEqual*, *Contains*, *DoesNotContain*, *StartsWith*, *DoesNotStartWith*, *Is*, *IsNot*, *IsBlank* และ "IsNotBlank"\`</span><span class="sxs-lookup"><span data-stu-id="ce586-132">Condition operators for the `operator` parameter are *None*, *LessThan*, *LessThanOrEqual*, *GreaterThan*, *GreaterThanOrEqual*, *Contains*, *DoesNotContain*, *StartsWith*, *DoesNotStartWith*, *Is*, *IsNot*, *IsBlank*, and "IsNotBlank"\`</span></span>

```javascript
let categories: DataViewCategoricalColumn = this.dataView.categorical.categories[0];

let target: IFilterColumnTarget = {
    table: categories.source.queryName.substr(0, categories.source.queryName.indexOf('.')), // table
    column: categories.source.displayName // col1
};

let conditions: IAdvancedFilterCondition[] = [];

conditions.push({
    operator: "LessThan",
    value: 0
});

let filter: IAdvancedFilter = new window['powerbi-models'].AdvancedFilter(target, "And", conditions);

// invoke the filter
visualHost.applyJsonFilter(filter, "general", "filter", FilterAction.merge);
```

<span data-ttu-id="ce586-133">SQL ที่เทียบเท่าคือ:</span><span class="sxs-lookup"><span data-stu-id="ce586-133">The SQL equivalent is:</span></span>

```sql
SELECT * FROM table WHERE col1 < 0;
```

<span data-ttu-id="ce586-134">สำหรับโค้ดตัวอย่างฉบับสมบูรณ์สำหรับการใช้ API ตัวกรองขั้นสูง โปรดไปที่ [พื้นที่เก็บข้อมูลวิชวล Sampleslicer](https://github.com/Microsoft/powerbi-visuals-sampleslicer)</span><span class="sxs-lookup"><span data-stu-id="ce586-134">For the complete sample code for using the Advanced Filter API, go to the [Sampleslicer visual repository](https://github.com/Microsoft/powerbi-visuals-sampleslicer).</span></span>

## <a name="the-tuple-filter-api-multi-column-filter"></a><span data-ttu-id="ce586-135">API ตัวกรองทูเพิล (ตัวกรองหลายคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="ce586-135">The Tuple Filter API (multi-column filter)</span></span>

<span data-ttu-id="ce586-136">API ตัวกรองทูเพิลถูกนำมาใช้ใน Visuals API 2.3.0</span><span class="sxs-lookup"><span data-stu-id="ce586-136">The Tuple Filter API was introduced in Visuals API 2.3.0.</span></span> <span data-ttu-id="ce586-137">ซึ่งคล้ายกับ API ตัวกรองพื้นฐาน แต่จะอนุญาตให้คุณกำหนดเงื่อนไขสำหรับหลายคอลัมน์และตารางได้</span><span class="sxs-lookup"><span data-stu-id="ce586-137">It is similar to the Basic Filter API, but it allows you to define conditions for several columns and tables.</span></span>

<span data-ttu-id="ce586-138">อินเตอร์เฟซตัวกรองแสดงในโค้ดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ce586-138">The filter interface is shown in the following code:</span></span> 

```typescript
interface ITupleFilter extends IFilter {
    $schema: string;
    filterType: FilterType;
    operator: TupleFilterOperators;
    target: ITupleFilterTarget;
    values: TupleValueType[];
}
```

<span data-ttu-id="ce586-139">ที่ซึ่ง:</span><span class="sxs-lookup"><span data-stu-id="ce586-139">Where:</span></span>
* <span data-ttu-id="ce586-140">`target` เป็นอาร์เรย์ของคอลัมน์ที่มีชื่อตาราง:</span><span class="sxs-lookup"><span data-stu-id="ce586-140">`target` is an array of columns with table names:</span></span>

    ```typescript
    declare type ITupleFilterTarget = IFilterTarget[];
    ```

  <span data-ttu-id="ce586-141">ตัวกรองสามารถระบุที่อยู่ของคอลัมน์จากตารางต่างๆ</span><span class="sxs-lookup"><span data-stu-id="ce586-141">The filter can address columns from various tables.</span></span>

* <span data-ttu-id="ce586-142">`$schema` คือ https://powerbi.com/product/schema#tuple</span><span class="sxs-lookup"><span data-stu-id="ce586-142">`$schema` is https://powerbi.com/product/schema#tuple.</span></span>

* <span data-ttu-id="ce586-143">`filterType` คือ *FilterType.Tuple*</span><span class="sxs-lookup"><span data-stu-id="ce586-143">`filterType` is *FilterType.Tuple*.</span></span>

* <span data-ttu-id="ce586-144">`operator` อนุญาตให้ใช้ได้เฉพาะในตัวดำเนินการ *In* เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ce586-144">`operator` allows use only in the *In* operator.</span></span>

* <span data-ttu-id="ce586-145">`values` เป็นอาร์เรย์ของทูเพิลค่า และแต่ละทูเพิลแสดงชุดข้อมูลที่อนุญาตหนึ่งชุดของค่าคอลัมน์เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="ce586-145">`values` is an array of value tuples, and each tuple represents one permitted combination of the target column values.</span></span> 

```typescript
declare type TupleValueType = ITupleElementValue[];

interface ITupleElementValue {
    value: PrimitiveValueType
}
```

<span data-ttu-id="ce586-146">ตัวอย่างที่สมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="ce586-146">Complete example:</span></span>

```typescript
let target: ITupleFilterTarget = [
    {
        table: "DataTable",
        column: "Team"
    },
    {
        table: "DataTable",
        column: "Value"
    }
];

let values = [
    [
        // the first column combination value (or the column tuple/vector value) that the filter will pass through
        {
            value: "Team1" // the value for the `Team` column of the `DataTable` table
        },
        {
            value: 5 // the value for the `Value` column of the `DataTable` table
        }
    ],
    [
        // the second column combination value (or the column tuple/vector value) that the filter will pass through
        {
            value: "Team2" // the value for `Team` column of `DataTable` table
        },
        {
            value: 6 // the value for `Value` column of `DataTable` table
        }
    ]
];

let filter: ITupleFilter = {
    $schema: "https://powerbi.com/product/schema#tuple",
    filterType: FilterType.Tuple,
    operator: "In",
    target: target,
    values: values
}

// invoke the filter
visualHost.applyJsonFilter(filter, "general", "filter", FilterAction.merge);
```

> [!IMPORTANT]
> <span data-ttu-id="ce586-147">ลำดับของชื่อคอลัมน์และค่าเงื่อนไขมีความละเอียดอ่อน</span><span class="sxs-lookup"><span data-stu-id="ce586-147">The order of the column names and condition values is sensitive.</span></span>

<span data-ttu-id="ce586-148">SQL ที่เทียบเท่าคือ:</span><span class="sxs-lookup"><span data-stu-id="ce586-148">The SQL equivalent is:</span></span>

```sql
SELECT * FROM DataTable WHERE ( Team = "Team1" AND Value = 5 ) OR ( Team = "Team2" AND Value = 6 );
```  

## <a name="restore-the-json-filter-from-the-data-view"></a><span data-ttu-id="ce586-149">คืนค่าตัวกรอง JSON จากมุมมองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ce586-149">Restore the JSON filter from the data view</span></span>

<span data-ttu-id="ce586-150">เริ่มต้นด้วย API เวอร์ชัน 2.2.0 คุณสามารถกู้คืนตัวกรอง JSON จาก *VisualUpdateOptions* ดังที่แสดงในโค้ดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ce586-150">Starting with API version 2.2.0, you can restore the JSON filter from *VisualUpdateOptions*, as shown in the following code:</span></span>

```typescript
export interface VisualUpdateOptions extends extensibility.VisualUpdateOptions {
    viewport: IViewport;
    dataViews: DataView[];
    type: VisualUpdateType;
    viewMode?: ViewMode;
    editMode?: EditMode;
    operationKind?: VisualDataChangeOperationKind;
    jsonFilters?: IFilter[];
}
```

<span data-ttu-id="ce586-151">เมื่อคุณสลับ บุ๊กมาร์ก Power BI เรียกใช้เมธอด `update` ของวิชวล และวิชวลได้รับวัตถุ `filter` ที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ce586-151">When you switch, bookmarks, Power BI calls the `update` method of the visual, and the visual gets a corresponding `filter` object.</span></span> <span data-ttu-id="ce586-152">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [เพิ่มการสนับสนุนบุ๊กมาร์กสำหรับวิชวล Power BI](bookmarks-support.md)</span><span class="sxs-lookup"><span data-stu-id="ce586-152">For more information, see [Add bookmark support for Power BI visuals](bookmarks-support.md).</span></span>

### <a name="sample-json-filter"></a><span data-ttu-id="ce586-153">ตัวกรอง JSON ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="ce586-153">Sample JSON filter</span></span>

<span data-ttu-id="ce586-154">โค้ดตัวกรอง JSON ตัวอย่างบางตัวจะแสดงในรูปต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ce586-154">Some sample JSON filter code is shown in the following image:</span></span>

![โค้ดตัวกรอง JSON](media/filter-api/json-filter.png)

### <a name="clear-the-json-filter"></a><span data-ttu-id="ce586-156">ล้างตัวกรอง JSON</span><span class="sxs-lookup"><span data-stu-id="ce586-156">Clear the JSON filter</span></span>

<span data-ttu-id="ce586-157">API ตัวกรองยอมรับค่า `null` ของตัวกรองเป็น *รีเซ็ต* หรือ *ล้าง*</span><span class="sxs-lookup"><span data-stu-id="ce586-157">The Filter API accepts the `null` value of the filter as *reset* or *clear*.</span></span>

```typescript
// invoke the filter
visualHost.applyJsonFilter(null, "general", "filter", FilterAction.merge);
```
