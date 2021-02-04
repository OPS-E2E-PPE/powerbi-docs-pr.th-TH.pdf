---
title: API ของวิชวลในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการใช้ IVisual API สำหรับวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: reference
ms.date: 03/19/2020
ms.openlocfilehash: 7b81ecfa1b97b202b6c1ff306cf858f2ea00acde
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888546"
---
# <a name="visual-api"></a><span data-ttu-id="9b888-104">API ของวิชวล</span><span class="sxs-lookup"><span data-stu-id="9b888-104">Visual API</span></span>
<span data-ttu-id="9b888-105">วิชวลทั้งหมดเริ่มต้นด้วย class ที่ใช้อินเทอร์เฟซ `IVisual`</span><span class="sxs-lookup"><span data-stu-id="9b888-105">All visuals start with a class that implements the `IVisual` interface.</span></span> <span data-ttu-id="9b888-106">คุณสามารถตั้งชื่อ class เป็นอะไรก็ได้ตราบใดที่มีหนึ่ง class ที่ใช้อินเทอร์เฟซ `IVisual`</span><span class="sxs-lookup"><span data-stu-id="9b888-106">You can name the class anything as long as there's exactly one class that implements the `IVisual` interface.</span></span>

> [!NOTE]
> <span data-ttu-id="9b888-107">ชื่อ class วิชวลต้องตรงกับที่กำหนดไว้ในไฟล์ *pbiviz.json*</span><span class="sxs-lookup"><span data-stu-id="9b888-107">The visual class name must match what's defined in the *pbiviz.json* file.</span></span>

<span data-ttu-id="9b888-108">ดู class วิชวลตัวอย่างด้วยวิธีการต่อไปนี้ที่ควรนำมาใช้:</span><span class="sxs-lookup"><span data-stu-id="9b888-108">See the sample visual class with the following methods that should be implemented:</span></span>

* <span data-ttu-id="9b888-109">`constructor` คอนสตรักเตอร์มาตรฐานเพื่อเริ่มต้นสถานะของวิชวล</span><span class="sxs-lookup"><span data-stu-id="9b888-109">`constructor`, a standard constructor to initialize the visual's state</span></span>
* <span data-ttu-id="9b888-110">`update` เพื่ออัปเดตข้อมูลของวิชวล</span><span class="sxs-lookup"><span data-stu-id="9b888-110">`update`, to update the visual's data</span></span>
* <span data-ttu-id="9b888-111">`enumerateObjectInstances` เพื่อส่งกลับวัตถุเพื่อเติมบานหน้าต่างคุณสมบัติ (ตัวเลือกการจัดรูปแบบ) ซึ่งคุณสามารถแก้ไขได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="9b888-111">`enumerateObjectInstances`, to return objects to populate the property pane (formatting options) where you can modify them as needed</span></span>
* <span data-ttu-id="9b888-112">`destroy` ดีสตรักเตอร์มาตรฐานสำหรับการล้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9b888-112">`destroy`, a standard destructor for cleanup</span></span>

```typescript
class MyVisual implements IVisual {
    
    constructor(options: VisualConstructorOptions) {
        //one time setup code goes here (called once)
    }
    
    public update(options: VisualUpdateOptions): void {
        //code to update your visual goes here (called on all view or data changes)
    }

    public enumerateObjectInstances(options: EnumerateVisualObjectInstancesOptions): VisualObjectInstanceEnumeration {
        //returns objects to populate the property pane (called for each object defined in capabilities)
    }
    
    public destroy(): void {
        //one time cleanup code goes here (called once)
    }
}
```

## <a name="constructor"></a><span data-ttu-id="9b888-113">คอนสตรักเตอร์</span><span class="sxs-lookup"><span data-stu-id="9b888-113">constructor</span></span>

<span data-ttu-id="9b888-114">คอนสตรักเตอร์ของ class วิชวลจะถูกเรียกเมื่อมีการสร้างอินสแตนซ์ของวิชวล</span><span class="sxs-lookup"><span data-stu-id="9b888-114">The constructor of the visual class is called when the visual is instantiated.</span></span> <span data-ttu-id="9b888-115">ซึ่งสามารถใช้สำหรับการตั้งค่าการดำเนินการใดๆ ที่จำเป็นต่อวิชวลได้</span><span class="sxs-lookup"><span data-stu-id="9b888-115">It can be used for any set up operations needed by the visual.</span></span>

```typescript
constructor(options: VisualConstructorOptions)
```

<span data-ttu-id="9b888-116">**VisualConstructorOptions**</span><span class="sxs-lookup"><span data-stu-id="9b888-116">**VisualConstructorOptions**</span></span>

* <span data-ttu-id="9b888-117">`element: HTMLElement` การอ้างอิงไปยังองค์ประกอบ DOM ที่จะมีวิชวลของคุณอยู่</span><span class="sxs-lookup"><span data-stu-id="9b888-117">`element: HTMLElement`, a reference to the DOM element that will contain your visual</span></span>
* <span data-ttu-id="9b888-118">`host: IVisualHost` คอลเลกชันของคุณสมบัติและบริการที่สามารถใช้เพื่อโต้ตอบกับโฮสต์วิชวล (Power BI)</span><span class="sxs-lookup"><span data-stu-id="9b888-118">`host: IVisualHost`, a collection of properties and services that can be used to interact with the visual host (Power BI)</span></span>

   <span data-ttu-id="9b888-119">`IVisualHost` ประกอบด้วยบริการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9b888-119">`IVisualHost` contains the following services:</span></span>

   ```typescript
   export interface IVisualHost extends extensibility.IVisualHost {
       createSelectionIdBuilder: () => visuals.ISelectionIdBuilder;
       : () => ISelectionManager;
       colorPalette: ISandboxExtendedColorPalette;
       persistProperties: (changes: VisualObjectInstancesToPersist) => void;
       applyJsonFilter: (filter: IFilter[] | IFilter, objectName: string, propertyName: string, action: FilterAction) => void;
       tooltipService: ITooltipService;
       telemetry: ITelemetryService;
       authenticationService: IAuthenticationService;
       locale: string;
       allowInteractions: boolean;
       launchUrl: (url: string) => void;
       fetchMoreData: () => boolean;
       instanceId: string;
       refreshHostData: () => void;
       createLocalizationManager: () => ILocalizationManager;
       storageService: ILocalVisualStorageService;
       eventService: IVisualEventService;
       switchFocusModeState: (on: boolean) => void;
   }
   ```
   * <span data-ttu-id="9b888-120">`createSelectionIdBuilder`สร้างและจัดเก็บเมตาดาต้าสำหรับรายการที่เลือกไว้ในวิชวลของคุณ</span><span class="sxs-lookup"><span data-stu-id="9b888-120">`createSelectionIdBuilder`, generates and stores metadata for selectable items in your visual</span></span>
   * <span data-ttu-id="9b888-121">`createSelectionManager` สร้างบริดจ์การสื่อสารที่ใช้เพื่อแจ้งโฮสต์วิชวล เกี่ยวกับการเปลี่ยนแปลงในสถานะการเลือก ดู [การเลือก API](./selection-api.md)</span><span class="sxs-lookup"><span data-stu-id="9b888-121">`createSelectionManager`, creates the communication bridge used to notify the visual's host on changes in the selection state, see [Selection API](./selection-api.md).</span></span>
   * <span data-ttu-id="9b888-122">`createLocalizationManager` สร้างผู้จัดการเพื่อช่วยในการ [การแปลเป็นภาษาท้องถิ่น](./localization.md)</span><span class="sxs-lookup"><span data-stu-id="9b888-122">`createLocalizationManager`, generates a manager to help with [Localization](./localization.md)</span></span>
   * <span data-ttu-id="9b888-123">`allowInteractions: boolean` ค่าสถานะบูลีนซึ่งให้คำแนะนำว่าควรมีการโต้ตอบของวิชวลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="9b888-123">`allowInteractions: boolean`, a boolean flag which hints whether or not the visual should be interactive</span></span>
   * <span data-ttu-id="9b888-124">`applyJsonFilter` ใช้ชนิดตัวกรองเฉพาะ ดู [ตัวกรอง API](./filter-api.md)</span><span class="sxs-lookup"><span data-stu-id="9b888-124">`applyJsonFilter`, applies specific filter types, see [Filter API](./filter-api.md)</span></span>
   * <span data-ttu-id="9b888-125">`persistProperties` อนุญาตให้ผู้ใช้สามารถยืนยันคุณสมบัติและบันทึกไปพร้อมกับข้อกำหนดของวิชวลเพื่อให้พร้อมใช้งานบนการโหลดครั้งถัดไป</span><span class="sxs-lookup"><span data-stu-id="9b888-125">`persistProperties`, allows users to persist properties and save them along with the visual definition, so they're available on the next reload</span></span>
   * <span data-ttu-id="9b888-126">`eventService` ส่งกลับ [การบริการเหตุการณ์](./event-service.md) เพื่อรองรับเหตุการณ์ **การแสดงผล**</span><span class="sxs-lookup"><span data-stu-id="9b888-126">`eventService`, returns an [event service](./event-service.md) to support **Render** events</span></span>
   * <span data-ttu-id="9b888-127">`storageService`ส่งกลับบริการเพื่อช่วยในการใช้ [ที่เก็บข้อมูลภายในเครื่อง](./local-storage.md) ในวิชวล</span><span class="sxs-lookup"><span data-stu-id="9b888-127">`storageService`, returns a service to help use [local storage](./local-storage.md) in the visual</span></span>
   * <span data-ttu-id="9b888-128">`authenticationService` สร้างบริการเพื่อช่วยในการรับรองความถูกต้องของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="9b888-128">`authenticationService`, generates a service to help with user authentication</span></span>
   * <span data-ttu-id="9b888-129">`tooltipService` ส่งกลับ [บริการคำแนะนำเครื่องมือ](./add-tooltips.md) เพื่อช่วยในการใช้คำแนะนำเครื่องมือในวิชวล</span><span class="sxs-lookup"><span data-stu-id="9b888-129">`tooltipService`, returns a [tooltip service](./add-tooltips.md) to help use tooltips in the visual</span></span>
   * <span data-ttu-id="9b888-130">`launchUrl` ช่วยในการ [เปิดใช้งาน URL](./launch-url.md) ในแท็บถัดไป</span><span class="sxs-lookup"><span data-stu-id="9b888-130">`launchUrl`, helps to [launch URL](./launch-url.md) in next tab</span></span>
   * <span data-ttu-id="9b888-131">`locale` ส่งกลับสตริงของพื้นที่ ดู [การแปลเป็นภาษาท้องถิ่น](./localization.md)</span><span class="sxs-lookup"><span data-stu-id="9b888-131">`locale`, returns a locale string, see [Localization](./localization.md)</span></span>
   * <span data-ttu-id="9b888-132">`instanceId` ส่งกลับสตริงที่จะระบุอินสแตนซ์วิชวลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="9b888-132">`instanceId`, returns a string to identify the current visual instance</span></span>
   * <span data-ttu-id="9b888-133">`colorPalette` ส่งกลับ colorPalette ที่จำเป็นในการนำสีไปใช้กับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="9b888-133">`colorPalette`, returns the colorPalette required to apply colors to your data</span></span>
   * <span data-ttu-id="9b888-134">`fetchMoreData` สนับสนุนการใช้ข้อมูลมากกว่าขีดจำกัดมาตรฐาน (1K แถว)</span><span class="sxs-lookup"><span data-stu-id="9b888-134">`fetchMoreData`, supports using more data than the standard limit (1K rows)</span></span>
   * <span data-ttu-id="9b888-135">`switchFocusModeState` ช่วยในการเปลี่ยนสถานะโหมดโฟกัส</span><span class="sxs-lookup"><span data-stu-id="9b888-135">`switchFocusModeState`, helps to change the focus mode state</span></span>

## <a name="update"></a><span data-ttu-id="9b888-136">อัปเดต</span><span class="sxs-lookup"><span data-stu-id="9b888-136">update</span></span>

<span data-ttu-id="9b888-137">วิชวลทั้งหมดต้องใช้วิธีการอัปเดตสาธารณะที่ถูกเรียกเมื่อใดก็ตามที่มีการเปลี่ยนแปลงในข้อมูลหรือสภาพแวดล้อมของโฮสต์</span><span class="sxs-lookup"><span data-stu-id="9b888-137">All visuals must implement a public update method that's called whenever there's a change in the data or host environment.</span></span>

```typescript
public update(options: VisualUpdateOptions): void
```

<span data-ttu-id="9b888-138">**VisualUpdateOptions**</span><span class="sxs-lookup"><span data-stu-id="9b888-138">**VisualUpdateOptions**</span></span>

* <span data-ttu-id="9b888-139">`viewport: IViewport` ขนาดของวิวพอร์ตที่วิชวลควรแสดงผลอยู่</span><span class="sxs-lookup"><span data-stu-id="9b888-139">`viewport: IViewport`, dimensions of the viewport that the visual should be rendered within</span></span>
* <span data-ttu-id="9b888-140">`dataViews: DataView[]` วัตถุ dataview ที่ประกอบด้วยข้อมูลทั้งหมดที่จำเป็นในการแสดงผลวิชวลของคุณ (โดยทั่วไปแล้ววิชวลของคุณจะใช้คุณสมบัติประเภทภายใต้ DataView)</span><span class="sxs-lookup"><span data-stu-id="9b888-140">`dataViews: DataView[]`, the dataview object which contains all data needed to render your visual (your visual will typically use the categorical property under DataView)</span></span>
* <span data-ttu-id="9b888-141">`type: VisualUpdateType` ค่าสถานะเพื่อระบุประเภทของการอัปเดตนี้ (**ข้อมูล** | **ปรับขนาด** | **ViewMode** | **สไตล์** | **ResizeEnd**)</span><span class="sxs-lookup"><span data-stu-id="9b888-141">`type: VisualUpdateType`, flags to indicate the type(s) of this update (**Data** | **Resize** | **ViewMode** | **Style** | **ResizeEnd**)</span></span>
* <span data-ttu-id="9b888-142">`viewMode: ViewMode` ค่าสถานะเพื่อระบุโหมดมุมมองของวิชวล (**มุมมอง** | **แก้ไข** | **InFocusEdit**)</span><span class="sxs-lookup"><span data-stu-id="9b888-142">`viewMode: ViewMode`, flags to indicate the view mode of the visual (**View** | **Edit** | **InFocusEdit**)</span></span>
* <span data-ttu-id="9b888-143">`editMode: EditMode` ค่าสถานะเพื่อระบุโหมดแก้ไขของวิชวล (**ค่าเริ่มต้น** | **ขั้นสูง**) (ถ้าวิชวลรองรับ **AdvancedEditMode** วิชวลจะแสดงตัวควบคุม UI ขั้นสูงเฉพาะเมื่อ **editMode** ได้รับการตั้งค่าเป็น **ขั้นสูง** เท่านั้น ดู [AdvancedEditMode](./advanced-edit-mode.md))</span><span class="sxs-lookup"><span data-stu-id="9b888-143">`editMode: EditMode`, flag to indicate the edit mode of the visual (**Default** | **Advanced**) (if the visual supports **AdvancedEditMode**, it should render its advanced UI controls only when **editMode** is set to **Advanced**, see [AdvancedEditMode](./advanced-edit-mode.md))</span></span>
* <span data-ttu-id="9b888-144">`operationKind?: VisualDataChangeOperationKind` ค่าสถานะเพื่อระบุชนิดของการเปลี่ยนแปลงข้อมูล (**สร้าง** | **ผนวก**)</span><span class="sxs-lookup"><span data-stu-id="9b888-144">`operationKind?: VisualDataChangeOperationKind`, flag to indicate type of data change (**Create** | **Append**)</span></span>
* <span data-ttu-id="9b888-145">`jsonFilters?: IFilter[]` คอลเลกชันของตัวกรอง json ที่ใช้</span><span class="sxs-lookup"><span data-stu-id="9b888-145">`jsonFilters?: IFilter[]`, collection of applied json filters</span></span>
* <span data-ttu-id="9b888-146">`isInFocus?: boolean` ค่าสถานะเพื่อระบุว่าวิชวลอยู่ในโหมดโฟกัสหรือไม่</span><span class="sxs-lookup"><span data-stu-id="9b888-146">`isInFocus?: boolean`, flag to indicate if the visual is in focus mode or not</span></span>
    
## <a name="enumerateobjectinstances-optional"></a><span data-ttu-id="9b888-147">enumerateObjectInstances `optional`</span><span class="sxs-lookup"><span data-stu-id="9b888-147">enumerateObjectInstances `optional`</span></span>

<span data-ttu-id="9b888-148">มีการเรียกใช้วิธีนี้สำหรับทุกวัตถุที่แสดงอยู่ในรายการความสามารถ</span><span class="sxs-lookup"><span data-stu-id="9b888-148">This method is called for every object listed in the capabilities.</span></span> <span data-ttu-id="9b888-149">การใช้ตัวเลือก (เฉพาะชื่อในขณะนี้) คุณได้ส่งกลับ `VisualObjectInstanceEnumeration` พร้อมข้อมูลเกี่ยวกับวิธีการแสดงคุณสมบัตินี้</span><span class="sxs-lookup"><span data-stu-id="9b888-149">Using the options (currently just the name) you return a `VisualObjectInstanceEnumeration` with information about how to display this property.</span></span>

```typescript
enumerateObjectInstances(options:EnumerateVisualObjectInstancesOptions):VisualObjectInstanceEnumeration
```

<span data-ttu-id="9b888-150">**EnumerateVisualObjectInstancesOptions**</span><span class="sxs-lookup"><span data-stu-id="9b888-150">**EnumerateVisualObjectInstancesOptions**</span></span>

* <span data-ttu-id="9b888-151">`objectName: string` ชื่อของวัตถุ</span><span class="sxs-lookup"><span data-stu-id="9b888-151">`objectName: string`, name of the object</span></span>

## <a name="destroy-optional"></a><span data-ttu-id="9b888-152">ทำลาย `optional`</span><span class="sxs-lookup"><span data-stu-id="9b888-152">destroy `optional`</span></span>

<span data-ttu-id="9b888-153">ฟังก์ชันการทำลายจะถูกเรียกเมื่อวิชวลของคุณถูกยกเลิกการโหลด และสามารถใช้สำหรับงานล้างข้อมูล เช่น การลบผู้ฟังเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="9b888-153">The destroy function is called when your visual is unloaded and can be used for clean up tasks such as removing event listeners.</span></span>

``` typescript
public destroy(): void
```

> [!Note]
> <span data-ttu-id="9b888-154">โดยทั่วไป Power BI ไม่ได้เรียกใช้ `destroy` เนื่องจากการลบ IFrame ทั้งหมดที่มีวิชวลสามารถทำได้รวดเร็วกว่า</span><span class="sxs-lookup"><span data-stu-id="9b888-154">Power BI generally doesn't call `destroy` since it's faster to remove the entire IFrame that contains the visual.</span></span>
