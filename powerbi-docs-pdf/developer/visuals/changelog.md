---
title: บันทึกการเปลี่ยนแปลง API ของวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายถึงการเปลี่ยนแปลงหลักในเวอร์ชันต่าง ๆ ของ API ของวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: reference
ms.date: 03/13/2019
ms.openlocfilehash: 3917ef64cfecd20e09be9b253ac05953cfe3d37a
ms.sourcegitcommit: a5e98bc86915f7bea6a0ab5df282683840e63d2c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/07/2021
ms.locfileid: "97969684"
---
# <a name="power-bi-visuals-api-changelog"></a><span data-ttu-id="020fc-104">บันทึกการเปลี่ยนแปลง API ของวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="020fc-104">Power BI visuals API changelog</span></span>
<span data-ttu-id="020fc-105">หน้านี้ประกอบด้วยข้อมูลสรุปสั้นๆ ของเวอร์ชัน  API</span><span class="sxs-lookup"><span data-stu-id="020fc-105">This page contains a quick summary of the API versions.</span></span> <span data-ttu-id="020fc-106">เวอร์ชันที่แสดงที่นี่ถือว่าเป็นเวอร์ชันที่เสถียรและจะไม่มีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="020fc-106">Versions listed here are considered stable and will not change.</span></span>


## <a name="api-v340"></a><span data-ttu-id="020fc-107">API v3.4.0</span><span class="sxs-lookup"><span data-stu-id="020fc-107">API v3.4.0</span></span>
  * <span data-ttu-id="020fc-108">`fetchMoreData` :พารามิเตอร์ใหม่ `aggregateSegments` (ค่าเริ่มต้นเป็น true) สำหรับการสนับสนุน fetchMoreData แบบไม่มีผลรวม</span><span class="sxs-lookup"><span data-stu-id="020fc-108">`fetchMoreData` : new `aggregateSegments` parameter (default true), for supporting no-aggregation fetchMoreData</span></span>

## <a name="api-v320"></a><span data-ttu-id="020fc-109">API v3.2.0</span><span class="sxs-lookup"><span data-stu-id="020fc-109">API v3.2.0</span></span>
  * <span data-ttu-id="020fc-110">สนับสนุน **[supportsMultiVisualSelection](./supportsmultivisualselection-feature.md)**</span><span class="sxs-lookup"><span data-stu-id="020fc-110">Supports **[supportsMultiVisualSelection](./supportsmultivisualselection-feature.md)**</span></span>

## <a name="api-v260"></a><span data-ttu-id="020fc-111">API v2.6.0</span><span class="sxs-lookup"><span data-stu-id="020fc-111">API v2.6.0</span></span>
  * <span data-ttu-id="020fc-112">เพิ่ม **isInFocus** เพื่ออัปเดตตัวเลือกและวิธีการ **switchFocusModeState** ไปยังโฮสต์วิชวล</span><span class="sxs-lookup"><span data-stu-id="020fc-112">Adds **isInFocus** to update option and **switchFocusModeState** method to visual host</span></span>
  * <span data-ttu-id="020fc-113">รองรับการปรับแต่ง **ผลรวมย่อย**</span><span class="sxs-lookup"><span data-stu-id="020fc-113">Supports **subtotals** customization</span></span>

## <a name="api-v250"></a><span data-ttu-id="020fc-114">API v2.5.0</span><span class="sxs-lookup"><span data-stu-id="020fc-114">API v2.5.0</span></span>
  * <span data-ttu-id="020fc-115">รองรับ **[บานหน้าต่างการวิเคราะห์](./analytics-pane.md)**</span><span class="sxs-lookup"><span data-stu-id="020fc-115">Supports **[Analytics Pane](./analytics-pane.md)**</span></span>
  * <span data-ttu-id="020fc-116">รองรับวิธีการ `SelectionIdBuilder` **withMatrixNode** และ **withTable**</span><span class="sxs-lookup"><span data-stu-id="020fc-116">Supports `SelectionIdBuilder` **withMatrixNode** and **withTable** methods</span></span>
  * <span data-ttu-id="020fc-117">ไม่รองรับอินเทอร์เฟซ `DataRepetitionSelector` อีกต่อไป โดยแทนที่ด้วยอินเทอร์เฟซ `data.CustomVisualOpaqueIdentity`</span><span class="sxs-lookup"><span data-stu-id="020fc-117">No longer supports `DataRepetitionSelector` interface, replaced with `data.CustomVisualOpaqueIdentity` interface</span></span>

## <a name="api-v230"></a><span data-ttu-id="020fc-118">API v2.3.0</span><span class="sxs-lookup"><span data-stu-id="020fc-118">API v2.3.0</span></span>
  * <span data-ttu-id="020fc-119">**[API หน้าเริ่มต้น](./landing-page.md)**</span><span class="sxs-lookup"><span data-stu-id="020fc-119">**[Landing Page API](./landing-page.md)**</span></span>
  * <span data-ttu-id="020fc-120">**[API ที่เก็บข้อมูลภายใน](./local-storage.md)**</span><span class="sxs-lookup"><span data-stu-id="020fc-120">**[Local Storage API](./local-storage.md)**</span></span>
  * <span data-ttu-id="020fc-121">**[API ตัวกรองทูเพิล (ตัวกรองหลายคอลัมน์)](./filter-api.md#the-tuple-filter-api-multi-column-filter)**</span><span class="sxs-lookup"><span data-stu-id="020fc-121">**[Tuple filter API (multi-column filter)](./filter-api.md#the-tuple-filter-api-multi-column-filter)**</span></span>
  * <span data-ttu-id="020fc-122">**[API เหตุการณ์การแสดงผล](./event-service.md#render-events-in-power-bi-visuals)**</span><span class="sxs-lookup"><span data-stu-id="020fc-122">**[Rendering Events API](./event-service.md#render-events-in-power-bi-visuals)**</span></span>

## <a name="api-v220"></a><span data-ttu-id="020fc-123">API v2.2.0</span><span class="sxs-lookup"><span data-stu-id="020fc-123">API v2.2.0</span></span>
  * <span data-ttu-id="020fc-124">รองรับ **[การกู้คืนตัวกรอง JSON จาก DataView](./filter-api.md#restore-the-json-filter-from-the-data-view)**</span><span class="sxs-lookup"><span data-stu-id="020fc-124">Supports **[restoring JSON Filter from DataView](./filter-api.md#restore-the-json-filter-from-the-data-view)**</span></span>
  * <span data-ttu-id="020fc-125">**[API ContextMenu](./context-menu.md)**</span><span class="sxs-lookup"><span data-stu-id="020fc-125">**[ContextMenu API](./context-menu.md)**</span></span>
  * <span data-ttu-id="020fc-126">สนับสนุนคุณลักษณะ **[ดูข้อมูลรายละเอียด](../../create-reports/desktop-drillthrough.md)**</span><span class="sxs-lookup"><span data-stu-id="020fc-126">Supports **[Drill through](../../create-reports/desktop-drillthrough.md)** feature</span></span>

## <a name="api-v210"></a><span data-ttu-id="020fc-127">API v2.1.0</span><span class="sxs-lookup"><span data-stu-id="020fc-127">API v2.1.0</span></span>
  * <span data-ttu-id="020fc-128">การปรับปรุงประสิทธิภาพการทำงาน:</span><span class="sxs-lookup"><span data-stu-id="020fc-128">Performance enhancements:</span></span>
    * <span data-ttu-id="020fc-129">เวลาโหลดเร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="020fc-129">Faster load times</span></span>
    * <span data-ttu-id="020fc-130">ฟุตพริ้นท์หน่วยความจำที่มีขนาดเล็กลง</span><span class="sxs-lookup"><span data-stu-id="020fc-130">Smaller memory footprint</span></span>
    * <span data-ttu-id="020fc-131">ข้อมูลและทรานแซคชันเหตุการณ์ที่ปรับอย่างเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="020fc-131">Optimized data and event transactions</span></span>  

<span data-ttu-id="020fc-132">**บันทึกย่อประจำรุ่น**</span><span class="sxs-lookup"><span data-stu-id="020fc-132">**Release notes**</span></span>
* <span data-ttu-id="020fc-133">การกรอง API ที่สร้างขึ้นใหม่จะพร้อมใช้งานใน  API 2.2 และไม่ได้รับการรองรับใน  API 2.1</span><span class="sxs-lookup"><span data-stu-id="020fc-133">Refactored filtering APIs will be available in API 2.2 and are not supported in API 2.1.</span></span>
* <span data-ttu-id="020fc-134">วิชวลจะรับเฉพาะชนิด dataView ที่ได้รับการระบุในความสามารถเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="020fc-134">Visuals will only receive the dataView type that was declared in their capabilities.</span></span> <span data-ttu-id="020fc-135">วิชวลที่ใช้ชนิด dataView หลายชนิดจะเสียหาย ซึ่งเป็นผลจากการอัปเดตนี้</span><span class="sxs-lookup"><span data-stu-id="020fc-135">Visuals that used multiple dataView types will break as a result of this update.</span></span>
* <span data-ttu-id="020fc-136">ไม่รองรับอินเทอร์เฟซ `DataViewScopeIdentity` อีกต่อไป โดยแทนที่ด้วยอินเทอร์เฟซ `data.DataRepetitionSelector`</span><span class="sxs-lookup"><span data-stu-id="020fc-136">No longer supports `DataViewScopeIdentity` interface, replaced with `data.DataRepetitionSelector` interface.</span></span> <span data-ttu-id="020fc-137">ถ้าคุณใช้คุณสมบัติหลักของอินเทอร์เฟซ `DataViewScopeIdentity` คุณสามารถแทนที่ด้วย `JSON.stringify(identity)`</span><span class="sxs-lookup"><span data-stu-id="020fc-137">If you used key property of the `DataViewScopeIdentity` interface, you can replace it with `JSON.stringify(identity)`</span></span>
* <span data-ttu-id="020fc-138">`undefined` ถูกแทนที่ด้วย `null` ภายใน dataView</span><span class="sxs-lookup"><span data-stu-id="020fc-138">`undefined` is replaced with `null` inside the dataView.</span></span> <span data-ttu-id="020fc-139">เมื่อมีการวนซ้ำในอาร์เรย์โดยใช้ `var item in myArray` จะเกิดการข้าม `undefined` แต่จะไม่ข้าม `null`</span><span class="sxs-lookup"><span data-stu-id="020fc-139">When iterating over an array using `var item in myArray` it skips on `undefined`, but doesn’t skip on `null`.</span></span> <span data-ttu-id="020fc-140">วิชวลที่ใช้รูปแบบนี้อาจเสียหายจากการอัปเดตนี้</span><span class="sxs-lookup"><span data-stu-id="020fc-140">Visuals that use this pattern may be broken by this update.</span></span> <span data-ttu-id="020fc-141">ตรวจดูให้แน่ใจว่าได้ตรวจสอบ `null` ในอาร์เรย์:</span><span class="sxs-lookup"><span data-stu-id="020fc-141">Make sure to check for `null` in arrays:</span></span>
   ```typescript
   for (var item in myArray) {
     if (!item) {
       continue;
     }
     console.log(item);
   }
   ```
* <span data-ttu-id="020fc-142">คุณสมบัติ `proto` ไม่จัดเก็บ metadata\data ที่ซ่อนไว้ภายใน dataView อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="020fc-142">The `proto` property no longer stores hidden metadata\data inside the dataView.</span></span> <span data-ttu-id="020fc-143">วิชวลที่สามารถเข้าถึงคุณสมบัติผ่าน `proto` อาจเสียหายจากการอัปเดตนี้</span><span class="sxs-lookup"><span data-stu-id="020fc-143">Visuals that access properties via `proto` may be broken by this update.</span></span>

## <a name="api-v1130"></a><span data-ttu-id="020fc-144">API v1.13.0</span><span class="sxs-lookup"><span data-stu-id="020fc-144">API v1.13.0</span></span>
* <span data-ttu-id="020fc-145">รองรับ **[ตัวแบ่งส่วนข้อมูลการซิงค์](./enable-sync-slicers.md)** โปรดทราบว่าจะใช้ได้เฉพาะตัวแบ่งส่วนเขตข้อมูลเดี่ยว เนื่องจาก PBI สถานะของโค้ดปัจจุบัน [อ่านเพิ่มเติม](../../visuals/power-bi-visualization-slicers.md)</span><span class="sxs-lookup"><span data-stu-id="020fc-145">Supports **[Sync Slicers](./enable-sync-slicers.md)**, note this only works for single field slicers due to PBI current code state, [read more](../../visuals/power-bi-visualization-slicers.md).</span></span>
* <span data-ttu-id="020fc-146">การเข้าถึง: [รองรับความคมชัดสูง](./high-contrast-support.md)</span><span class="sxs-lookup"><span data-stu-id="020fc-146">Accessibility: [High-contrast support](./high-contrast-support.md)</span></span> 
* <span data-ttu-id="020fc-147">การเข้าถึง: อนุญาตให้มีการตั้งค่าสถานะโฟกัสของแป้นพิมพ์</span><span class="sxs-lookup"><span data-stu-id="020fc-147">Accessibility: Allow Keyboard Focus flag</span></span>

## <a name="api-v1120"></a><span data-ttu-id="020fc-148">API v1.12.0</span><span class="sxs-lookup"><span data-stu-id="020fc-148">API v1.12.0</span></span>
* <span data-ttu-id="020fc-149">รองรับธีม</span><span class="sxs-lookup"><span data-stu-id="020fc-149">Supports Themes</span></span>
* <span data-ttu-id="020fc-150">รองรับ **[fetchMoreData](./fetch-more-data.md)** โปรดทราบว่า **Fetch More Data API** เอาชนะขีดจำกัดสูงสุดของจุดข้อมูลที่ 30K</span><span class="sxs-lookup"><span data-stu-id="020fc-150">Supports **[fetchMoreData](./fetch-more-data.md)**, note the **Fetch More Data API** overcomes the hard limit of 30K data points</span></span>
* <span data-ttu-id="020fc-151">**[API คำแนะนำเครื่องมือของ Canvas](./add-tooltips.md#add-report-page-tooltips)**</span><span class="sxs-lookup"><span data-stu-id="020fc-151">**[Canvas Tooltips API](./add-tooltips.md#add-report-page-tooltips)**</span></span>

## <a name="api-v1110"></a><span data-ttu-id="020fc-152">API v1.11.0</span><span class="sxs-lookup"><span data-stu-id="020fc-152">API v1.11.0</span></span>
* <span data-ttu-id="020fc-153">**[ API FilterManager](./filter-api.md)**</span><span class="sxs-lookup"><span data-stu-id="020fc-153">**[FilterManager API](./filter-api.md)**</span></span>
* <span data-ttu-id="020fc-154">รองรับ **[บุ๊กมาร์ก](./bookmarks-support.md)**</span><span class="sxs-lookup"><span data-stu-id="020fc-154">Supports **[Bookmarks](./bookmarks-support.md)**</span></span> 

## <a name="api-v1100"></a><span data-ttu-id="020fc-155">API v1.10.0</span><span class="sxs-lookup"><span data-stu-id="020fc-155">API v1.10.0</span></span>
* <span data-ttu-id="020fc-156">เพิ่ม `ILocalizationManager`</span><span class="sxs-lookup"><span data-stu-id="020fc-156">Adds `ILocalizationManager`</span></span>
* <span data-ttu-id="020fc-157">**API การรับรองความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="020fc-157">**Authentication API**</span></span>

## <a name="api-v190"></a><span data-ttu-id="020fc-158">API v1.9.0</span><span class="sxs-lookup"><span data-stu-id="020fc-158">API v1.9.0</span></span>
* <span data-ttu-id="020fc-159">**[API launchUrl](./launch-url.md)**</span><span class="sxs-lookup"><span data-stu-id="020fc-159">**[launchUrl API](./launch-url.md)**</span></span>

## <a name="api-v180"></a><span data-ttu-id="020fc-160">API v1.8.0</span><span class="sxs-lookup"><span data-stu-id="020fc-160">API v1.8.0</span></span>
* <span data-ttu-id="020fc-161">รองรับ **fillRule** ชนิดใหม่ (การไล่ระดับสี) ใน schema ความสามารถ</span><span class="sxs-lookup"><span data-stu-id="020fc-161">Supports new type **fillRule** (gradient) in capabilities schema</span></span>
* <span data-ttu-id="020fc-162">รองรับคุณสมบัติ **กฎ** ใน schema ความสามารถสำหรับคุณสมบัติวัตถุ</span><span class="sxs-lookup"><span data-stu-id="020fc-162">Supports **rule** property in capabilities schema for object properties</span></span>

## <a name="api-v170"></a><span data-ttu-id="020fc-163">API v1.7.0</span><span class="sxs-lookup"><span data-stu-id="020fc-163">API v1.7.0</span></span>
* <span data-ttu-id="020fc-164">รองรับ **[RESJSON](./localization.md#resource-file)**</span><span class="sxs-lookup"><span data-stu-id="020fc-164">Supports **[RESJSON](./localization.md#resource-file)**</span></span>

## <a name="api-v162"></a><span data-ttu-id="020fc-165">API  v1.6.2</span><span class="sxs-lookup"><span data-stu-id="020fc-165">API v1.6.2</span></span>
* <span data-ttu-id="020fc-166">รองรับ **[โหมดแก้ไข](./advanced-edit-mode.md)** สำหรับวิชวลเพื่อเข้าสู่โหมดแก้ไขในวิชวล</span><span class="sxs-lookup"><span data-stu-id="020fc-166">Supports **[Edit mode](./advanced-edit-mode.md)** for visual to enter in-visual edit mode</span></span>
* <span data-ttu-id="020fc-167">รองรับ **[วิชวล R Power BI แบบโต้ตอบ (html)](https://github.com/PowerBi-Projects/PowerBI-visuals/blob/master/RVisualTutorial/CreateRHTML.md)** โดยอ้างอิงตาม html</span><span class="sxs-lookup"><span data-stu-id="020fc-167">Supports **[Interactive (html) R Power BI visuals](https://github.com/PowerBi-Projects/PowerBI-visuals/blob/master/RVisualTutorial/CreateRHTML.md)**, based on html</span></span>

## <a name="api-v150"></a><span data-ttu-id="020fc-168">API v1.5.0</span><span class="sxs-lookup"><span data-stu-id="020fc-168">API v1.5.0</span></span>
* <span data-ttu-id="020fc-169">รองรับ **[อนุญาตให้มีการโต้ตอบ](./visuals-interactions.md)** สำหรับความสามารถในการโต้ตอบของวิชวล</span><span class="sxs-lookup"><span data-stu-id="020fc-169">Supports **[Allow interactions](./visuals-interactions.md)** for visual interactivity</span></span>

## <a name="api-v140"></a><span data-ttu-id="020fc-170">API v1.4.0</span><span class="sxs-lookup"><span data-stu-id="020fc-170">API v1.4.0</span></span>
* <span data-ttu-id="020fc-171">รองรับ **[การแปลเป็นภาษาท้องถิ่น](./localization.md)**</span><span class="sxs-lookup"><span data-stu-id="020fc-171">Supports **[Localization](./localization.md)**</span></span>

## <a name="api-v130"></a><span data-ttu-id="020fc-172">API v1.3.0</span><span class="sxs-lookup"><span data-stu-id="020fc-172">API v1.3.0</span></span>
* <span data-ttu-id="020fc-173">รองรับ **[คำแนะนำเครื่องมือ](./add-tooltips.md)**</span><span class="sxs-lookup"><span data-stu-id="020fc-173">Supports **[Tooltips](./add-tooltips.md)**</span></span>

## <a name="api-v120"></a><span data-ttu-id="020fc-174">API v1.2.0</span><span class="sxs-lookup"><span data-stu-id="020fc-174">API v1.2.0</span></span>
* <span data-ttu-id="020fc-175">เพิ่ม **colorPalette** เพื่อจัดการสีที่ใช้ในวิชวลของคุณ</span><span class="sxs-lookup"><span data-stu-id="020fc-175">Adds **colorPalette** to manage the colors used on your visual.</span></span>
* <span data-ttu-id="020fc-176">รองรับ **การเลือกหลายรายการ** - selectionManager สามารถยอมรับอาร์เรย์ของ `SelectionId`</span><span class="sxs-lookup"><span data-stu-id="020fc-176">Supports **Multiple selection** - selectionManager can accept an array of `SelectionId`.</span></span>
* <span data-ttu-id="020fc-177">รองรับ **[วิชวล R](https://github.com/PowerBi-Projects/PowerBI-visuals/blob/master/RVisualTutorial/CreateRHTML.md)** โดยใช้สคริปต์ R</span><span class="sxs-lookup"><span data-stu-id="020fc-177">Supports **[R visuals](https://github.com/PowerBi-Projects/PowerBI-visuals/blob/master/RVisualTutorial/CreateRHTML.md)** using R scripts</span></span>

## <a name="api-v110"></a><span data-ttu-id="020fc-178">API v1.1.0</span><span class="sxs-lookup"><span data-stu-id="020fc-178">API v1.1.0</span></span>
* <span data-ttu-id="020fc-179">รองรับการแก้จุดบกพร่องของวิชวลใน iFrame</span><span class="sxs-lookup"><span data-stu-id="020fc-179">Supports debug visual in iFrame</span></span>
* <span data-ttu-id="020fc-180">เพิ่ม Sandbox น้ำหนักเบาด้วยการเตรียมใช้งาน iFrame ที่รวดเร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="020fc-180">Adds light weight sandbox with faster initialization of the iFrame</span></span>
* <span data-ttu-id="020fc-181">แก้ไขปัญหา [Capabilities.objects ไม่รองรับชนิด "ข้อความ"](https://github.com/Microsoft/PowerBI-visuals-tools/issues/12)</span><span class="sxs-lookup"><span data-stu-id="020fc-181">Fixes [Capabilities.objects does not support "text" type](https://github.com/Microsoft/PowerBI-visuals-tools/issues/12) issue</span></span>
* <span data-ttu-id="020fc-182">รองรับ `pbiviz update` เพื่ออัปเดตข้อกำหนดชนิด API ของวิชวลและ schema</span><span class="sxs-lookup"><span data-stu-id="020fc-182">Supports `pbiviz update` to update visual API type definitions and schema</span></span>
* <span data-ttu-id="020fc-183">รองรับค่าสถานะ `--api-version` ใน `pbiviz new` เพื่อสร้างวิชวลด้วยเวอร์ชัน api เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="020fc-183">Supports `--api-version` flag in `pbiviz new` to create visuals with a specific api version</span></span>
* <span data-ttu-id="020fc-184">รองรับ Alpha Release ของ API v1.2.0</span><span class="sxs-lookup"><span data-stu-id="020fc-184">Supports alpha release of API v1.2.0</span></span>

<span data-ttu-id="020fc-185">**โฮสต์วิชวล**</span><span class="sxs-lookup"><span data-stu-id="020fc-185">**Visual Host**</span></span>
* <span data-ttu-id="020fc-186">เพิ่ม **createSelectionIdBuilder** เพื่อสร้างรหัสเฉพาะที่ใช้สำหรับการเลือกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="020fc-186">Adds **createSelectionIdBuilder** to create unique identifiers used for data selection</span></span>
* <span data-ttu-id="020fc-187">เพิ่ม **createSelectionManager** เพื่อจัดการสถานะการเลือกของวิชวลและการสื่อสารเกี่ยวกับการเปลี่ยนแปลงกับโฮสต์วิชวล</span><span class="sxs-lookup"><span data-stu-id="020fc-187">Adds **createSelectionManager** to manage the selection state of the visual and communicates changes to the visual host</span></span>
* <span data-ttu-id="020fc-188">เพิ่มอาร์เรย์ของค่าเริ่มต้น **สี** เพื่อใช้ในวิชวล</span><span class="sxs-lookup"><span data-stu-id="020fc-188">Adds an array of default **colors** to use in visuals</span></span>

## <a name="api-v100"></a><span data-ttu-id="020fc-189">API v1.0.0</span><span class="sxs-lookup"><span data-stu-id="020fc-189">API v1.0.0</span></span>
* <span data-ttu-id="020fc-190">การเผยแพร่ API เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="020fc-190">Initial API release</span></span>
