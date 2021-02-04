---
title: เพิ่มการรองรับบุ๊กมาร์กสำหรับวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: วิชวล Power BI สามารถจัดการได้ เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI การสลับบุ๊กมาร์ก
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: how-to
ms.date: 06/18/2019
ms.openlocfilehash: a1bd0f694bbc2bc40fc35aef3c6017e7f4a8196a
ms.sourcegitcommit: a5e98bc86915f7bea6a0ab5df282683840e63d2c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/07/2021
ms.locfileid: "97969707"
---
# <a name="add-bookmark-support-for-power-bi-visuals"></a><span data-ttu-id="07258-105">เพิ่มการรองรับบุ๊กมาร์กสำหรับวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="07258-105">Add bookmark support for Power BI visuals</span></span>

<span data-ttu-id="07258-106">ด้วยบุ๊กมาร์กรายงานของ Power BI ช่วยให้คุณสามารถจับภาพมุมมองที่กำหนดค่าไว้ของหน้ารายงาน สถานะตัวเลือก และสถานะการกรองของวิชวลได้</span><span class="sxs-lookup"><span data-stu-id="07258-106">With Power BI report bookmarks, you can capture a configured view of a report page, the selection state, and the filtering state of the visual.</span></span> <span data-ttu-id="07258-107">แต่จำเป็นต้องมีการดำเนินการเพิ่มเติมจากฝั่งวิชวลแบบกำหนดเองเพื่อสนับสนุนบุ๊กมาร์กและตอบสนองต่อการเปลี่ยนแปลงอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="07258-107">But it requires additional action from the Power BI visuals side to support the bookmark and react correctly to changes.</span></span>

<span data-ttu-id="07258-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบุ๊กมาร์ก โปรดดูหัวข้อ [ใช้บุ๊กมาร์กเพื่อแชร์ข้อมูลเชิงลึกและสร้างเรื่องราวใน Power BI](../../create-reports/desktop-bookmarks.md)</span><span class="sxs-lookup"><span data-stu-id="07258-108">For more information about bookmarks, see [Use bookmarks to share insights and build stories in Power BI](../../create-reports/desktop-bookmarks.md).</span></span>

## <a name="report-bookmarks-support-in-your-visual"></a><span data-ttu-id="07258-109">การสนับสนุนของบุ๊กมาร์กรายงานในวิชวลของคุณ</span><span class="sxs-lookup"><span data-stu-id="07258-109">Report bookmarks support in your visual</span></span>

<span data-ttu-id="07258-110">หากวิชวลของคุณโต้ตอบกับวิชวลอื่น เลือกจุดข้อมูล หรือกรองวิชวลอื่น ๆ คุณจะต้องคืนค่าสถานะจากคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="07258-110">If your visual interacts with other visuals, selects data points, or filters other visuals, you need to restore the state from properties.</span></span>

## <a name="add-report-bookmarks-support"></a><span data-ttu-id="07258-111">เพิ่มการสนับสนุนของบุ๊กมาร์กหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="07258-111">Add report bookmarks support</span></span>

1. <span data-ttu-id="07258-112">ติดตั้ง (หรืออัปเดต) ยูทิลิตี้ที่จำเป็น [powerbi-visuals-utils-interactivityutils](https://github.com/Microsoft/PowerBI-visuals-utils-interactivityutils/) เวอร์ชัน 3.0.0 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="07258-112">Install (or update) the required utility, [powerbi-visuals-utils-interactivityutils](https://github.com/Microsoft/PowerBI-visuals-utils-interactivityutils/) version 3.0.0 or later.</span></span> <span data-ttu-id="07258-113">ซึ่งประกอบด้วยคลาสเพิ่มเติมเพื่อจัดการกับตัวเลือกหรือตัวกรองของสถานะ</span><span class="sxs-lookup"><span data-stu-id="07258-113">It contains additional classes to manipulate with the state selection or filter.</span></span> <span data-ttu-id="07258-114">ซึ่งจำเป็นสำหรับวิชวลตัวกรองและวิชวลใดก็ตามที่ใช้ `InteractivityService`</span><span class="sxs-lookup"><span data-stu-id="07258-114">It's required for filter visuals and any visual that uses `InteractivityService`.</span></span>

2. <span data-ttu-id="07258-115">อัปเดต API ของวิชวลไปเป็นเวอร์ชัน 1.11.0 เพื่อใช้ `registerOnSelectCallback` ในอินสแตนซ์ของ `SelectionManager`</span><span class="sxs-lookup"><span data-stu-id="07258-115">Update the visual API to version 1.11.0 to use `registerOnSelectCallback` in an instance of `SelectionManager`.</span></span> <span data-ttu-id="07258-116">ซึ่งจำเป็นสำหรับวิชวลที่ไม่ใช่ตัวกรองที่ใช้ `SelectionManager` แบบธรรมดาแทนที่จะเป็น `InteractivityService`</span><span class="sxs-lookup"><span data-stu-id="07258-116">It's required for non-filter visuals that use the plain `SelectionManager` rather than `InteractivityService`.</span></span>

### <a name="how-power-bi-visuals-interact-with-power-bi-in-report-bookmarks"></a><span data-ttu-id="07258-117">วิธีการที่วิชวลแบบกำหนดเองโต้ตอบกับ Power BI ในบุ๊กมาร์กรายงาน</span><span class="sxs-lookup"><span data-stu-id="07258-117">How Power BI visuals interact with Power BI in report bookmarks</span></span>

<span data-ttu-id="07258-118">ลองพิจารณาสถานการณ์ต่อไปนี้: คุณต้องการสร้างบุ๊กมาร์กหลายรายการในหน้ารายงานโดยมีสถานะตัวเลือกแตกต่างกันในแต่ละบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="07258-118">Let's consider the following scenario: you want to create several bookmarks on the report page, with a different selection state in each bookmark.</span></span>

<span data-ttu-id="07258-119">อันดับแรก คุณเลือกจุดข้อมูลในวิชวลของคุณ</span><span class="sxs-lookup"><span data-stu-id="07258-119">First, you select a data point in your visual.</span></span> <span data-ttu-id="07258-120">วิชวลโต้ตอบกับ Power BI และวิชวลอื่น ๆ โดยการส่งผ่านตัวเลือกไปยังโฮสต์</span><span class="sxs-lookup"><span data-stu-id="07258-120">The visual interacts with Power BI and other visuals by passing selections to the host.</span></span> <span data-ttu-id="07258-121">จากนั้นคุณเลือก **เพิ่ม** ในบานหน้าต่าง **บุ๊กมาร์ก** และ Power BI จะบันทึกตัวเลือกปัจจุบันสำหรับบุ๊กมาร์กใหม่</span><span class="sxs-lookup"><span data-stu-id="07258-121">You then select **Add** in the **Bookmark** pane, and Power BI saves the current selections for the new bookmark.</span></span>

<span data-ttu-id="07258-122">ซึ่งเกิดขึ้นซ้ำ ๆ เมื่อคุณเปลี่ยนแปลงตัวเลือกและเพิ่มบุ๊กมาร์กใหม่</span><span class="sxs-lookup"><span data-stu-id="07258-122">It happens repeatedly as you change the selection and add new bookmarks.</span></span> <span data-ttu-id="07258-123">หลังจากที่คุณสร้างบุ๊กมาร์กแล้ว คุณสามารถสลับไปมาระหว่างไฟล์เหล่านั้นได้</span><span class="sxs-lookup"><span data-stu-id="07258-123">After you create the bookmarks, you can switch between them.</span></span>

<span data-ttu-id="07258-124">เมื่อคุณเลือกบุ๊กมาร์ก Power BI จะคืนค่าตัวกรองหรือสถานะตัวเลือกที่บันทึกไว้และส่งผ่านไปยังวิชวล</span><span class="sxs-lookup"><span data-stu-id="07258-124">When you select a bookmark, Power BI restores the saved filter or selection state and passes it to the visuals.</span></span> <span data-ttu-id="07258-125">วิชวลอื่น ๆ จะถูกไฮไลต์หรือกรองตามสถานะที่จัดเก็บไว้ในบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="07258-125">Other visuals are highlighted or filtered according to the state that's stored in the bookmark.</span></span> <span data-ttu-id="07258-126">โฮสต์ Power BI เป็นผู้รับผิดชอบสำหรับการดำเนินการนี้</span><span class="sxs-lookup"><span data-stu-id="07258-126">The Power BI host is responsible for the actions.</span></span> <span data-ttu-id="07258-127">วิชวลของคุณมีหน้าที่รับผิดชอบในการสะท้อนสถานะตัวเลือกใหม่อย่างถูกต้อง (ตัวอย่างเช่น สำหรับการเปลี่ยนสีของจุดข้อมูลที่แสดง)</span><span class="sxs-lookup"><span data-stu-id="07258-127">Your visual is responsible for correctly reflecting the new selection state (for example, for changing the colors of rendered data points).</span></span>

<span data-ttu-id="07258-128">สถานะตัวเลือกใหม่จะได้รับการสื่อสารไปยังวิชวลผ่านเมธอด `update`</span><span class="sxs-lookup"><span data-stu-id="07258-128">The new selection state is communicated to the visual through the `update` method.</span></span> <span data-ttu-id="07258-129">อาร์กิวเมนต์ `options` ประกอบด้วยคุณสมบัติพิเศษ, `options.jsonFilters`</span><span class="sxs-lookup"><span data-stu-id="07258-129">The `options` argument contains a special property, `options.jsonFilters`.</span></span> <span data-ttu-id="07258-130">คุณสมบัติ JSONFilter สามารถประกอบด้วย `Advanced Filter` และ `Tuple Filter`</span><span class="sxs-lookup"><span data-stu-id="07258-130">Its JSONFilter property can contain `Advanced Filter` and `Tuple Filter`.</span></span>

<span data-ttu-id="07258-131">วิชวลควรคืนค่าตัวกรองเพื่อแสดงสถานะที่สอดคล้องกันของวิชวลสำหรับบุ๊กมาร์กที่เลือก</span><span class="sxs-lookup"><span data-stu-id="07258-131">The visual should restore the filter values to display the corresponding state of the visual for the selected bookmark.</span></span> <span data-ttu-id="07258-132">หรือถ้าวิชวลใช้ตัวเลือกเท่านั้น คุณสามารถใช้ฟังก์ชันการเรียกกลับแบบพิเศษในการเรียกใช้เมธอด `registerOnSelectCallback` ที่ลงทะเบียนไว้ของ ISelectionManager</span><span class="sxs-lookup"><span data-stu-id="07258-132">Or, if the visual uses selections only, you can use the special callback function call that's registered as the `registerOnSelectCallback` method of ISelectionManager.</span></span>

### <a name="visuals-with-selection"></a><span data-ttu-id="07258-133">วิชวลที่มีตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="07258-133">Visuals with Selection</span></span>

<span data-ttu-id="07258-134">ถ้าวิชวลของคุณโต้ตอบกับวิชวลอื่นโดยใช้[ตัวเลือก](https://github.com/PowerBi-Projects/PowerBI-visuals/blob/master/Tutorial/Selection.md) คุณสามารถเพิ่มบุ๊กมาร์กอย่างใดอย่างหนึ่งในสองวิธี:</span><span class="sxs-lookup"><span data-stu-id="07258-134">If your visual interacts with other visuals by using [Selection](https://github.com/PowerBi-Projects/PowerBI-visuals/blob/master/Tutorial/Selection.md), you can add bookmarks in either of two ways:</span></span>

* <span data-ttu-id="07258-135">ถ้าวิชวลไม่ได้ใช้ [InteractivityService](https://github.com/microsoft/powerbi-visuals-utils-interactivityutils/blob/master/src/interactivityService.ts) คุณสามารถใช้เมธอด `FilterManager.restoreSelectionIds`</span><span class="sxs-lookup"><span data-stu-id="07258-135">If the visual hasn't already used [InteractivityService](https://github.com/microsoft/powerbi-visuals-utils-interactivityutils/blob/master/src/interactivityService.ts), you can use the `FilterManager.restoreSelectionIds` method.</span></span>

* <span data-ttu-id="07258-136">ถ้าวิชวลนั้นใช้ [InteractivityService](https://github.com/microsoft/powerbi-visuals-utils-interactivityutils/blob/master/src/interactivityService.ts) เพื่อจัดการตัวเลือกเรียบร้อยแล้ว คุณควรใช้เมธอด `applySelectionFromFilter` ในอินสแตนซ์ของ `InteractivityService`</span><span class="sxs-lookup"><span data-stu-id="07258-136">If the visual already uses [InteractivityService](https://github.com/microsoft/powerbi-visuals-utils-interactivityutils/blob/master/src/interactivityService.ts) to manage selections, you should use the `applySelectionFromFilter` method in the instance of `InteractivityService`.</span></span>

#### <a name="use-iselectionmanagerregisteronselectcallback"></a><span data-ttu-id="07258-137">ใช้ ISelectionManager.registerOnSelectCallback</span><span class="sxs-lookup"><span data-stu-id="07258-137">Use ISelectionManager.registerOnSelectCallback</span></span>

<span data-ttu-id="07258-138">เมื่อคุณเลือกบุ๊กมาร์ก Power BI จะเรียกใช้เมธอด `callback` ของวิชวลที่มีตัวเลือกที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="07258-138">When you select a bookmark, Power BI calls the `callback` method of the visual with the corresponding selections.</span></span> 

```typescript
this.selectionManager.registerOnSelectCallback(
    (ids: ISelectionId[]) => {
        //called when a selection was set by Power BI
    });
);
```

<span data-ttu-id="07258-139">ให้สมมติว่าคุณมีจุดข้อมูลในวิชวลของคุณ ซึ่งถูกสร้างขึ้นในเมธอด [visualTransform](https://github.com/Microsoft/PowerBI-visuals-sampleBarChart/blob/master/src/barChart.ts#L74)</span><span class="sxs-lookup"><span data-stu-id="07258-139">Let's assume that you have a data point in your visual that was created in the [visualTransform](https://github.com/Microsoft/PowerBI-visuals-sampleBarChart/blob/master/src/barChart.ts#L74) method.</span></span>

<span data-ttu-id="07258-140">และ `datapoints` มีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="07258-140">And `datapoints` looks like:</span></span>

```typescript
visualDataPoints.push({
    category: categorical.categories[0].values[i],
    color: getCategoricalObjectValue<Fill>(categorical.categories[0], i, 'colorSelector', 'fill', defaultColor).solid.color,
    selectionId: host.createSelectionIdBuilder()
        .withCategory(categorical.categories[0], i)
        .createSelectionId(),
    selected: false
});
```

<span data-ttu-id="07258-141">ตอนนี้คุณมี `visualDataPoints` เป็นจุดข้อมูลของคุณและอาร์เรย์ `ids` ที่ส่งผ่านไปยังฟังก์ชัน `callback`</span><span class="sxs-lookup"><span data-stu-id="07258-141">You now have `visualDataPoints` as your data points and the `ids` array passed to the `callback` function.</span></span>

<span data-ttu-id="07258-142">ในขั้นตอนนี้ วิชวลควรเปรียบเทียบอาร์เรย์ `ISelectionId[]` ที่มีตัวเลือกในอาร์เรย์ `visualDataPoints` ของคุณและทำเครื่องหมายจุดข้อมูลที่สอดคล้องกันตามที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="07258-142">At this point, the visual should compare the `ISelectionId[]` array with the selections in your `visualDataPoints` array and mark the corresponding data points as selected.</span></span>

```typescript
this.selectionManager.registerOnSelectCallback(
    (ids: ISelectionId[]) => {
        visualDataPoints.forEach(dataPoint => {
            ids.forEach(bookmarkSelection => {
                if (bookmarkSelection.equals(dataPoint.selectionId)) {
                    dataPoint.selected = true;
                }
            });
        });
    });
);
```

<span data-ttu-id="07258-143">หลังจากคุณอัปเดตจุดข้อมูลแล้ว จุดข้อมูลเหล่านี้จะแสดงสถานะตัวเลือกปัจจุบันที่จัดเก็บอยู่ในออบเจ็กต์ `filter`</span><span class="sxs-lookup"><span data-stu-id="07258-143">After you update the data points, they'll reflect the current selection state that's stored in the `filter` object.</span></span> <span data-ttu-id="07258-144">จากนั้นเมื่อมีการแสดงผลจุดข้อมูล สถานะตัวเลือกของวิชวลแบบกำหนดเองจะตรงกับสถานะของบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="07258-144">Then, when the data points are rendered, the custom visual's selection state will match the state of the bookmark.</span></span>

### <a name="use-interactivityservice-for-control-selections-in-the-visual"></a><span data-ttu-id="07258-145">ใช้ InteractivityService สำหรับตัวเลือกการควบคุมในวิชวล</span><span class="sxs-lookup"><span data-stu-id="07258-145">Use InteractivityService for control selections in the visual</span></span>

<span data-ttu-id="07258-146">ถ้าวิชวลของคุณใช้ `InteractivityService` คุณไม่จำเป็นต้องมีการดำเนินการเพิ่มเติมเพื่อสนับสนุนบุ๊กมาร์กในวิชวลของคุณ</span><span class="sxs-lookup"><span data-stu-id="07258-146">If your visual uses `InteractivityService`, you don't need any additional actions to support the bookmarks in your visual.</span></span>

<span data-ttu-id="07258-147">เมื่อคุณเลือกบุ๊กมาร์ก ยูทิลิตี้จะจัดการสถานะตัวเลือกของวิชวล</span><span class="sxs-lookup"><span data-stu-id="07258-147">When you select bookmarks, the utility handles the visual's selection state.</span></span>

### <a name="visuals-with-a-filter"></a><span data-ttu-id="07258-148">วิชวลที่มีตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="07258-148">Visuals with a filter</span></span>

<span data-ttu-id="07258-149">สมมติว่าวิชวลสร้างตัวกรองข้อมูลตามช่วงวันที่</span><span class="sxs-lookup"><span data-stu-id="07258-149">Let's assume that the visual creates a filter of data by date range.</span></span> <span data-ttu-id="07258-150">คุณมี `startDate` และ `endDate` เป็นวันที่เริ่มต้นและสิ้นสุดของช่วง</span><span class="sxs-lookup"><span data-stu-id="07258-150">You have `startDate` and `endDate` as the start and end dates of the range.</span></span>

<span data-ttu-id="07258-151">วิชวลสร้างตัวกรองขั้นสูงและเรียกใช้เมธอด `applyJsonFilter` ของโฮสต์เพื่อกรองข้อมูลตามเงื่อนไขที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="07258-151">The visual creates an advanced filter and calls the host method `applyJsonFilter` to filter data by the relevant conditions.</span></span>

<span data-ttu-id="07258-152">เป้าหมายคือตารางที่ใช้สำหรับการกรอง</span><span class="sxs-lookup"><span data-stu-id="07258-152">The target is the table that's used for filtering.</span></span>

```typescript
import { AdvancedFilter } from "powerbi-models";

const filter: IAdvancedFilter = new AdvancedFilter(
    target,
    "And",
    {
        operator: "GreaterThanOrEqual",
        value: startDate
            ? startDate.toJSON()
            : null
    },
    {
        operator: "LessThanOrEqual",
        value: endDate
            ? endDate.toJSON()
            : null
    });

this.host.applyJsonFilter(
    filter,
    "general",
    "filter",
    (startDate && endDate)
        ? FilterAction.merge
        : FilterAction.remove
);
```

<span data-ttu-id="07258-153">แต่ละครั้งที่คุณเลือกบุ๊กมาร์ก วิชวลแบบกำหนดเองจะมีการเรียกใช้ `update`</span><span class="sxs-lookup"><span data-stu-id="07258-153">Each time you select a bookmark, the custom visual gets an `update` call.</span></span>

<span data-ttu-id="07258-154">วิชวลแบบกำหนดเองควรตรวจสอบตัวกรองในวัตถุ:</span><span class="sxs-lookup"><span data-stu-id="07258-154">The custom visual should check the filter in the object:</span></span>

```typescript
const filter: IAdvancedFilter = FilterManager.restoreFilter(
    && options.jsonFilters
    && options.jsonFilters[0] as any
) as IAdvancedFilter;
```

<span data-ttu-id="07258-155">ถ้าออบเจ็กต์ `filter` ไม่เป็นค่า null วิชวลควรคืนค่าเงื่อนไขตัวกรองจากออบเจ็กต์:</span><span class="sxs-lookup"><span data-stu-id="07258-155">If the `filter` object isn't null, the visual should restore the filter conditions from the object:</span></span>

```typescript
const jsonFilters: AdvancedFilter = this.options.jsonFilters as AdvancedFilter[];

if (jsonFilters
    && jsonFilters[0]
    && jsonFilters[0].conditions
    && jsonFilters[0].conditions[0]
    && jsonFilters[0].conditions[1]
) {
    const startDate: Date = new Date(`${jsonFilters[0].conditions[0].value}`);
    const endDate: Date = new Date(`${jsonFilters[0].conditions[1].value}`);

    // apply restored conditions
} else {
    // apply default settings
}
```

<span data-ttu-id="07258-156">หลังจากนั้น วิชวลควรเปลี่ยนแปลงสถานะภายในเพื่อสะท้อนถึงเงื่อนไขปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="07258-156">After that, the visual should change its internal state to reflect the current conditions.</span></span> <span data-ttu-id="07258-157">สถานะภายในประกอบด้วยออบเจ็กต์จุดข้อมูลและการแสดงผลข้อมูลด้วยภาพ (เส้น สี่เหลี่ยม และอื่นๆ)</span><span class="sxs-lookup"><span data-stu-id="07258-157">The internal state includes the data points and visualization objects (lines, rectangles, and so on).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07258-158">ในสถานการณ์ของบุ๊กมาร์กรายงาน วิชวลไม่ควรเรียกใช้ `applyJsonFilter` เพื่อกรองวิชวลอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="07258-158">In the report bookmarks scenario, the visual shouldn't call `applyJsonFilter` to filter the other visuals.</span></span> <span data-ttu-id="07258-159">วิชวลเหล่านั้นจะถูกกรองโดย Power BI อยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="07258-159">They will already be filtered by Power BI.</span></span>

<span data-ttu-id="07258-160">วิชวลตัวแบ่งข้อมูลเส้นเวลาจะเปลี่ยนตัวเลือกช่วงเพื่อให้สอดคล้องกับช่วงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="07258-160">The Timeline Slicer visual changes the range selector to the corresponding data ranges.</span></span>

<span data-ttu-id="07258-161">สำหรับข้อมูลเพิ่มเติม ให้ดู [ที่เก็บตัวแบ่งข้อมูลเส้นเวลา](https://github.com/Microsoft/powerbi-visuals-timeline/commit/606f1152f59f82b5b5a367ff3b117372d129e597?diff=unified#diff-b6ef9a9ac3a3225f8bd0de84bee0a0df)</span><span class="sxs-lookup"><span data-stu-id="07258-161">For more information, see the [Timeline Slicer repository](https://github.com/Microsoft/powerbi-visuals-timeline/commit/606f1152f59f82b5b5a367ff3b117372d129e597?diff=unified#diff-b6ef9a9ac3a3225f8bd0de84bee0a0df).</span></span>

### <a name="filter-the-state-to-save-visual-properties-in-bookmarks"></a><span data-ttu-id="07258-162">กรองสถานะเพื่อบันทึกคุณสมบัติต่าง ๆ ของวิชวลในบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="07258-162">Filter the state to save visual properties in bookmarks</span></span>

<span data-ttu-id="07258-163">คุณสมบัติ `filterState` นี้ทำให้เป็นคุณสมบัติส่วนหนึ่งของการกรอง</span><span class="sxs-lookup"><span data-stu-id="07258-163">The `filterState` property makes a property of a part of filtering.</span></span> <span data-ttu-id="07258-164">วิชวลสามารถจัดเก็บค่าที่ต่างกันในบุ๊กมาร์กได้หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="07258-164">The visual can store a variety of values in bookmarks.</span></span>

<span data-ttu-id="07258-165">หากต้องการบันทึกค่าคุณสมบัติเป็นสถานะตัวกรอง ให้ทำเครื่องหมายคุณสมบัติออบเจ็กต์เป็น `"filterState": true` ในไฟล์ *capabilities.json*</span><span class="sxs-lookup"><span data-stu-id="07258-165">To save the property value as a filter state, mark the object property as `"filterState": true` in the *capabilities.json* file.</span></span>

<span data-ttu-id="07258-166">ตัวอย่างเช่น ตัวแบ่งข้อมูลเส้นเวลาจะเก็บค่าคุณสมบัติ `Granularity` ในตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="07258-166">For example, the Timeline Slicer stores the `Granularity` property values in a filter.</span></span> <span data-ttu-id="07258-167">ซึ่งช่วยให้หน่วยย่อยที่สุด (Granularity) ในปัจจุบันสามารถเปลี่ยนแปลงได้เมื่อคุณเปลี่ยนบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="07258-167">It allows the current granularity to change as you change the bookmarks.</span></span>

<span data-ttu-id="07258-168">สำหรับข้อมูลเพิ่มเติม ให้ดู [ที่เก็บตัวแบ่งข้อมูลเส้นเวลา](https://github.com/microsoft/powerbi-visuals-timeline/commit/8b7d82dd23cd2bd71817f1bc5d1e1732347a185e#diff-290828b604cfa62f1cb310f2e90c52fdR334)</span><span class="sxs-lookup"><span data-stu-id="07258-168">For more information, see the [Timeline Slicer repository](https://github.com/microsoft/powerbi-visuals-timeline/commit/8b7d82dd23cd2bd71817f1bc5d1e1732347a185e#diff-290828b604cfa62f1cb310f2e90c52fdR334).</span></span>
