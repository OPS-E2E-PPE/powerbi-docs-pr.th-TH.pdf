---
title: ดึงข้อมูลเพิ่มเติมจาก Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายถึงวิธีการเปิดใช้งานการดึงชุดข้อมูลขนาดใหญ่เป็นเซกเมนต์สำหรับวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: how-to
ms.date: 12/13/2020
ms.openlocfilehash: 345efe91be1af5ee61d713c576f04657b182ad47
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97886315"
---
# <a name="fetch-more-data-from-power-bi"></a><span data-ttu-id="6938d-104">ดึงข้อมูลเพิ่มเติมจาก Power BI</span><span class="sxs-lookup"><span data-stu-id="6938d-104">Fetch more data from Power BI</span></span>

<span data-ttu-id="6938d-105">`fetchMoreData`API ช่วยให้วิชวล Power BI สามารถข้ามขีดจำกัดที่ยากลำบากในการดูข้อมูลแถว 30K ได้</span><span class="sxs-lookup"><span data-stu-id="6938d-105">The `fetchMoreData` API enables Power BI visuals to bypass the hard limit of a 30K rows data view.</span></span> <span data-ttu-id="6938d-106">ด้วยการเปิดตัว 3.4 API ใหม่ `fetchMoreData`ฟังก์ชันการทำงานของ API จะขยายเพื่อรองรับวิธีการใหม่ ๆ ในการโหลดกลุ่มข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6938d-106">With the new 3.4 API release, the `fetchMoreData` API’s functionality is extended to support a new approach of loading data chunks.</span></span> <span data-ttu-id="6938d-107">นอกเหนือจากวิธีการที่มีอยู่ ซึ่งจะรวมกลุ่มทั้งหมดที่ร้องขอด้วย API จะสนับสนุนการโหลดเฉพาะกลุ่มข้อมูลส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6938d-107">In addition to the existing approach, which aggregates all the chunks requested, the API will support loading only the incremental data chunks.</span></span>

<span data-ttu-id="6938d-108">วิธีการใหม่ช่วยเพิ่มความยืดหยุ่นมากขึ้นในวิธีโหลดกลุ่มข้อมูลเพิ่มเติมไปยังวิชวล</span><span class="sxs-lookup"><span data-stu-id="6938d-108">The new approach allows more flexibility in the way additional data chunks are loaded to the visual.</span></span> <span data-ttu-id="6938d-109">เพื่อปรับปรุงประสิทธิภาพการทำงาน คุณสามารถกำหนดขนาดกลุ่มเพื่อรองรับกรณีการใช้งานของคุณได้</span><span class="sxs-lookup"><span data-stu-id="6938d-109">To improve performance, you can configure the chunk size to accommodate your use case.</span></span>

## <a name="limitations-of-fetchmoredata"></a><span data-ttu-id="6938d-110">ขีดจำกัดของ fetchMoreData</span><span class="sxs-lookup"><span data-stu-id="6938d-110">Limitations of fetchMoreData</span></span>

* <span data-ttu-id="6938d-111">ขนาดระยะห่างจำกัดไว้ที่ช่วง 2 ถึง 30,000</span><span class="sxs-lookup"><span data-stu-id="6938d-111">Window size is limited to a range of 2 to 30,000.</span></span>
* <span data-ttu-id="6938d-112">จำนวนแถวทั้งหมดของดาต้าวิวถูกจำกัดไว้ที่ 1,048,576 แถว</span><span class="sxs-lookup"><span data-stu-id="6938d-112">Dataview total row count is limitd to 1,048,576 rows.</span></span>
* <span data-ttu-id="6938d-113">ในโหมดการรวมเซกเมนต์ ขนาดหน่วยความจำของดาต้าวิวถูกจำกัดไว้ที่ 100 MB</span><span class="sxs-lookup"><span data-stu-id="6938d-113">In segments aggregation mode, dataview memory size is limited to 100 MB.</span></span>

## <a name="enable-a-segmented-fetch-of-large-datasets"></a><span data-ttu-id="6938d-114">เปิดใช้งานการดึงชุดข้อมูลขนาดใหญ่เป็นเซกเมนต์</span><span class="sxs-lookup"><span data-stu-id="6938d-114">Enable a segmented fetch of large datasets</span></span>

<span data-ttu-id="6938d-115">สำหรับโหมดเซกเมนต์ `dataview` คุณกำหนดขนาดหน้าต่างสำหรับ `dataReductionAlgorithm` ในไฟล์ *capabilities.json* ของวิชวลสำหรับ `dataViewMapping` ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="6938d-115">For the `dataview` segment mode, you define a window size for `dataReductionAlgorithm` in the visual's *capabilities.json* file for the required `dataViewMapping`.</span></span> <span data-ttu-id="6938d-116">`count` กำหนดขนาดหน้าต่างซึ่งจำกัดจำนวนแถวข้อมูลใหม่ที่สามารถผนวกเข้ากับ `dataview` ในแต่ละการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="6938d-116">The `count` determines the window size, which limits the number of new data rows that can be appended to the `dataview` in each update.</span></span>

<span data-ttu-id="6938d-117">เพิ่มโค้ดต่อไปนี้ในไฟล์ *capabilities.json*:</span><span class="sxs-lookup"><span data-stu-id="6938d-117">Add the following code in the *capabilities.json* file:</span></span>

```typescript
"dataViewMappings": [
    {
        "table": {
            "rows": {
                "for": {
                    "in": "values"
                },
                "dataReductionAlgorithm": {
                    "window": {
                        "count": 100
                    }
                }
            }
    }
]
```

<span data-ttu-id="6938d-118">เซกเมนต์ใหม่จะถูกผนวกเข้า `dataview` ที่มีอยู่และจัดให้กับการแสดงภาพเป็นการโทร `update`</span><span class="sxs-lookup"><span data-stu-id="6938d-118">New segments are appended to the existing `dataview` and provided to the visual as an `update` call.</span></span>

## <a name="usage-in-the-power-bi-visual"></a><span data-ttu-id="6938d-119">การใช้งานในวิชวลของ Power BI</span><span class="sxs-lookup"><span data-stu-id="6938d-119">Usage in the Power BI visual</span></span>

<span data-ttu-id="6938d-120">ใน Power BI คุณสามารถใช้ `fetchMoreData` ในโหมดการรวมเซกเมนต์ค่าเริ่มต้นหรือในโหมดการอัปเดตแบบเพิ่มหน่วยได้</span><span class="sxs-lookup"><span data-stu-id="6938d-120">In Power BI, you can use `fetchMoreData` in the default segments aggregation mode or in incremental updates mode.</span></span> 

### <a name="using-segments-aggregation-mode-default"></a><span data-ttu-id="6938d-121">การใช้โหมดการรวมเซกเมนต์ (ค่าเริ่มต้น)</span><span class="sxs-lookup"><span data-stu-id="6938d-121">Using segments aggregation mode (default)</span></span>

<span data-ttu-id="6938d-122">ด้วยโหมดนี้ดาต้าวิวที่จัดเตรียมให้กับวิชวลจะมีข้อมูลสะสมสำหรับ `fetchMoreData requests` ก่อนหน้านี้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6938d-122">With this mode, the dataview provided to the visual contain the accumulated data for all the previous `fetchMoreData requests`.</span></span> <span data-ttu-id="6938d-123">ดังนั้นจึงคาดว่าขนาดดาต้าวิวจะเพิ่มขึ้นในการอัปเดตแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="6938d-123">Therefore, dataview size is expected to grow with each update.</span></span> <span data-ttu-id="6938d-124">ตัวอย่างเช่น หากคาดว่าจะมีทั้งหมด 100,000 แถวและขนาดระยะห่างถูกตั้งค่าไว้ที่ 10,000 ข้อมูลการอัปเดตดาต้าวิวครั้งแรกควรมี 10,000 แถว ข้อมูลการอัปเดตดาต้าวิวครั้งที่สองควรมี 20,000 แถว และเป็นอย่างนี้ต่อไปเรื่อย ๆ</span><span class="sxs-lookup"><span data-stu-id="6938d-124">For example, if a total of 100,000 rows are expected and the window size is set to 10,000, the first update dataview should include 10,000 rows, the second update dataview should include 20,000 rows, and so on.</span></span>

<span data-ttu-id="6938d-125">โหมดนี้ถูกเลือกโดยการเรียก `fetchMoreData` ด้วย `aggregateSegments = true`</span><span class="sxs-lookup"><span data-stu-id="6938d-125">This mode is selected by calling `fetchMoreData` with `aggregateSegments = true`.</span></span>

<span data-ttu-id="6938d-126">คุณสามารถตรวจสอบว่ามีข้อมูลอยู่หรือไม่โดยตรวจสอบการมีอยู่ของ `dataView.metadata.segment`:</span><span class="sxs-lookup"><span data-stu-id="6938d-126">You can determine whether data exists by checking for the existence of `dataView.metadata.segment`:</span></span>

```typescript
    public update(options: VisualUpdateOptions) {
        const dataView = options.dataViews[0];
        console.log(dataView.metadata.segment);
        // output: __proto__: Object
    }
```

<span data-ttu-id="6938d-127">นอกจากนี้คุณยังสามารถตรวจสอบเพื่อดูว่ามันเป็นการอัปเดตครั้งแรกหรือการอัปเดตที่ตามมาภายหลังโดยการตรวจสอบ `options.operationKind`</span><span class="sxs-lookup"><span data-stu-id="6938d-127">You also can check to see whether it's the first update or a subsequent update by checking `options.operationKind`.</span></span> <span data-ttu-id="6938d-128">ในโค้ดต่อไปนี้ `VisualDataChangeOperationKind.Create`อ้างถึงเซกเมนต์แรกและ`VisualDataChangeOperationKind.Append` อ้างถึงเซกเมนต์ที่ตามมาภายหลัง</span><span class="sxs-lookup"><span data-stu-id="6938d-128">In the following code, `VisualDataChangeOperationKind.Create` refers to the first segment and `VisualDataChangeOperationKind.Append` refers to subsequent segments.</span></span>

<span data-ttu-id="6938d-129">สำหรับตัวอย่างการนำไปใช้งาน โปรดดูข้อมูลโค้ดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6938d-129">For a sample implementation, see the following code snippet:</span></span>

```typescript
// CV update implementation
public update(options: VisualUpdateOptions) {
    // indicates this is the first segment of new data.
    if (options.operationKind == VisualDataChangeOperationKind.Create) {

    }

    // on second or subsequent segments:
    if (options.operationKind == VisualDataChangeOperationKind.Append) {

    }

    // complete update implementation
}
```

<span data-ttu-id="6938d-130">คุณยังสามารถเรียกใช้เมธอด `fetchMoreData` จากตัวจัดการเหตุการณ์ UI ดังที่แสดงไว้ที่นี่:</span><span class="sxs-lookup"><span data-stu-id="6938d-130">You also can invoke the `fetchMoreData` method from a UI event handler, as shown here:</span></span>

```typescript
btn_click(){
{
    // check if more data is expected for the current data view
    if (dataView.metadata.segment) {
        //request for more data if available; as a response, Power BI will call update method
        let request_accepted: bool = this.host.fetchMoreData(true);
        // handle rejection
        if (!request_accepted) {
            // for example, when the 100 MB limit has been reached
        }
    }
}
```

<span data-ttu-id="6938d-131">Power BI เรียกเมธอด `update` ของวิชวลด้วยเซกเมนต์ใหม่ของข้อมูลเพื่อตอบสนองต่อการเรียกใช้เมธอด `this.host.fetchMoreData`</span><span class="sxs-lookup"><span data-stu-id="6938d-131">As a response to calling the `this.host.fetchMoreData` method, Power BI calls the `update` method of the visual with a new segment of data.</span></span>

> [!NOTE]
> <span data-ttu-id="6938d-132">เพื่อหลีกเลี่ยงข้อจำกัดของหน่วยความจำไคลเอนต์ ปัจจุบัน Power BI จำกัดข้อมูลที่ดึงมาทั้งหมดเป็น 100 MB</span><span class="sxs-lookup"><span data-stu-id="6938d-132">To avoid client memory constraints, Power BI currently limits the fetched data total to 100 MB.</span></span> <span data-ttu-id="6938d-133">คุณสามารถเห็นว่าถึงขีดจำกัดแล้วเมื่อ `fetchMoreData()` ส่งกลับ `false`</span><span class="sxs-lookup"><span data-stu-id="6938d-133">You can see that the limit has been reached when `fetchMoreData()` returns `false`.</span></span>

### <a name="using-incremental-updates-mode"></a><span data-ttu-id="6938d-134">การใช้โหมดการอัปเดตแบบเพิ่มหน่วย</span><span class="sxs-lookup"><span data-stu-id="6938d-134">Using incremental updates mode</span></span>

<span data-ttu-id="6938d-135">ด้วยโหมดนี้ดาต้าวิวที่กำหนดให้กับวิชวลจะมีเพียงข้อมูลที่เพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="6938d-135">With this mode, the dataview provided to the visual contains just incremental data.</span></span> <span data-ttu-id="6938d-136">ดังนั้นขนาดดาต้าวิวจะไม่เลยขนาดระยะห่างที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="6938d-136">Therefore, dataview size would not pass the defined window size.</span></span> <span data-ttu-id="6938d-137">ตัวอย่างเช่น หากคาดว่าจะมีทั้งหมด 101,000 แถวและขนาดระยะห่างถูกตั้งค่าไว้ที่ 10,000 วิชวลจะได้รับการอัปเดต 10 รายการโดยมีขนาดข้อมูลเป็น 10,000 รายการ และการอัปเดตหนึ่งรายการที่มีดาต้าวิวขนาด 1,000</span><span class="sxs-lookup"><span data-stu-id="6938d-137">For example, if a total of 101,000 rows are expected and the window size is set to 10,000, the visual would get 10 updates with a dataview size of 10,000 and one update with a dataview of size 1,000.</span></span>

<span data-ttu-id="6938d-138">โหมดนี้ถูกเลือกโดยการเรียก `fetchMoreData` ด้วย `aggregateSegments = false`</span><span class="sxs-lookup"><span data-stu-id="6938d-138">This mode is selected by calling `fetchMoreData` with `aggregateSegments = false`.</span></span>

<span data-ttu-id="6938d-139">คุณสามารถตรวจสอบว่ามีข้อมูลอยู่หรือไม่โดยตรวจสอบการมีอยู่ของ `dataView.metadata.segment`:</span><span class="sxs-lookup"><span data-stu-id="6938d-139">You can determine whether data exists by checking for the existence of `dataView.metadata.segment`:</span></span>

```typescript
    public update(options: VisualUpdateOptions) {
        const dataView = options.dataViews[0];
        console.log(dataView.metadata.segment);
        // output: __proto__: Object
    }
```

<span data-ttu-id="6938d-140">นอกจากนี้คุณยังสามารถตรวจสอบเพื่อดูว่ามันเป็นการอัปเดตครั้งแรกหรือการอัปเดตที่ตามมาภายหลังโดยการตรวจสอบ `options.operationKind`</span><span class="sxs-lookup"><span data-stu-id="6938d-140">You also can check to see whether it's the first update or a subsequent update by checking `options.operationKind`.</span></span> <span data-ttu-id="6938d-141">ในโค้ดต่อไปนี้ `VisualDataChangeOperationKind.Create`อ้างถึงเซกเมนต์แรกและ`VisualDataChangeOperationKind.Segment` อ้างถึงเซกเมนต์ที่ตามมาภายหลัง</span><span class="sxs-lookup"><span data-stu-id="6938d-141">In the following code, `VisualDataChangeOperationKind.Create` refers to the first segment, and `VisualDataChangeOperationKind.Segment` refers to subsequent segments.</span></span>

<span data-ttu-id="6938d-142">สำหรับตัวอย่างการนำไปใช้งาน โปรดดูข้อมูลโค้ดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6938d-142">For a sample implementation, see the following code snippet:</span></span>

```typescript
// CV update implementation
public update(options: VisualUpdateOptions) {
    // indicates this is the first segment of new data.
    if (options.operationKind == VisualDataChangeOperationKind.Create) {

    }

    // on second or subsequent segments:
    if (options.operationKind == VisualDataChangeOperationKind.Segment) {
        
    }

    // skip overlapping rows 
    const rowOffset = (dataView.table['lastMergeIndex'] === undefined) ? 0 : dataView.table['lastMergeIndex'] + 1;

    // Process incoming data
    for (var i = rowOffset; i < dataView.table.rows.length; i++) {
        var val = <number>(dataView.table.rows[i][0]); // Pick first column               
            
     }
     
    // complete update implementation
}
```

<span data-ttu-id="6938d-143">คุณยังสามารถเรียกใช้เมธอด `fetchMoreData` จากตัวจัดการเหตุการณ์ UI ดังที่แสดงไว้ที่นี่:</span><span class="sxs-lookup"><span data-stu-id="6938d-143">You also can invoke the `fetchMoreData` method from a UI event handler, as shown here:</span></span>

```typescript
btn_click(){
{
    // check if more data is expected for the current data view
    if (dataView.metadata.segment) {
        //request for more data if available; as a response, Power BI will call update method
        let request_accepted: bool = this.host.fetchMoreData(false);
        // handle rejection
        if (!request_accepted) {
            // for example, when the 100 MB limit has been reached
        }
    }
}
```

<span data-ttu-id="6938d-144">Power BI เรียกเมธอด `update` ของวิชวลด้วยเซกเมนต์ใหม่ของข้อมูลเพื่อตอบสนองต่อการเรียกใช้เมธอด `this.host.fetchMoreData`</span><span class="sxs-lookup"><span data-stu-id="6938d-144">As a response to calling the `this.host.fetchMoreData` method, Power BI calls the `update` method of the visual with a new segment of data.</span></span>

> [!NOTE]
> <span data-ttu-id="6938d-145">แม้ว่าข้อมูลดาต้าวิวระหว่างการอัปเดตที่แตกต่างกันส่วนใหญ่จะเป็นข้อมูลเฉพาะ แต่จะมีการทับซ้อนกันระหว่างดาต้าวิวที่ตามมาในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="6938d-145">Although the dataviews data between the different updates is mostly exclusive, there will be some overlap between subsequent dataviews.</span></span>
> <span data-ttu-id="6938d-146">สำหรับการแมปข้อมูลแบบตารางและจัดกลุ่ม คาดว่าดาต้าวิว N แถวแรกจะมีข้อมูลที่คัดลอกมาจากดาต้าวิวก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6938d-146">For table and categorical data mapping, it is expected the the first N dataview rows will contain data copied from the previous dataview.</span></span>
> <span data-ttu-id="6938d-147">N สามารถกำหนดได้จาก: `(dataView.table['lastMergeIndex'] === undefined) ? 0 : dataView.table['lastMergeIndex'] + 1`</span><span class="sxs-lookup"><span data-stu-id="6938d-147">N can be determined by: `(dataView.table['lastMergeIndex'] === undefined) ? 0 : dataView.table['lastMergeIndex'] + 1`</span></span>