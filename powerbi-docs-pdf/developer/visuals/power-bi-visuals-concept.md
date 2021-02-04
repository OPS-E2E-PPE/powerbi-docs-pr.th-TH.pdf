---
title: แนวคิดวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้ได้อธิบายวิธีการแสดงผลด้วยภาพรวมกับ Power BI และวิธีที่ผู้ใช้สามารถโต้ตอบกับวิชวลใน Power BI ได้ เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
manager: rkarlin
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.date: 06/18/2019
ms.openlocfilehash: 4a6d78e332ae6e6c29b11a4ee79b05718c30f355
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97885004"
---
# <a name="power-bi-visuals-system-integration"></a><span data-ttu-id="21144-104">การรวมระบบวิชวลของ Power BI</span><span class="sxs-lookup"><span data-stu-id="21144-104">Power BI visuals system integration</span></span>

<span data-ttu-id="21144-105">บทความนี้ได้อธิบายวิธีการแสดงผลด้วยภาพรวมกับ Power BI และวิธีที่ผู้ใช้สามารถโต้ตอบกับวิชวลใน Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="21144-105">The article describes how visuals integrate with Power BI and how a user can interact with a visual in Power BI.</span></span> 

<span data-ttu-id="21144-106">รูปภาพต่อไปนี้แสดงการดำเนินการทั่วไปโดยใช้วิชวลที่ผู้ใช้ใช้ เช่น การเลือกที่คั่นหน้าและที่ดำเนินการใน Power BI</span><span class="sxs-lookup"><span data-stu-id="21144-106">The following figure depicts how common visual-based actions that a user takes, like selecting a bookmark, are processed in Power BI.</span></span>

![ไดอะแกรมการดำเนินการวิชวลของ Power BI](media/power-bi-visuals-concept/visual-concept.svg)

## <a name="visuals-get-updates-from-power-bi"></a><span data-ttu-id="21144-108">วิชวลรับการอัปเดตจาก Power BI</span><span class="sxs-lookup"><span data-stu-id="21144-108">Visuals get updates from Power BI</span></span>

<span data-ttu-id="21144-109">วิชวลเรียกใช้วิธีการ `update` เพื่อได้รับการอัปเดตจาก Power BI</span><span class="sxs-lookup"><span data-stu-id="21144-109">A visual calls an `update` method to get updates from Power BI.</span></span> <span data-ttu-id="21144-110">วิธีการ `update` จะประกอบด้วยตรรกะหลักของวิชวลและเป็นความรับผิดชอบในการแสดงแผนภูมิหรือข้อมูลที่เป็นภาพ</span><span class="sxs-lookup"><span data-stu-id="21144-110">The `update` method usually contains the main logic of the visual and is responsible for rendering a chart or visualizing data.</span></span>

<span data-ttu-id="21144-111">การอัปเดตถูกกระตุ้นเมื่อวิชวลเรียกใช้วิธีการ `update`</span><span class="sxs-lookup"><span data-stu-id="21144-111">Updates are triggered when the visual calls the `update` method.</span></span>

## <a name="action-and-update-patterns"></a><span data-ttu-id="21144-112">การดำเนินการและอัปเดตรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="21144-112">Action and update patterns</span></span>

<span data-ttu-id="21144-113">การดำเนินการและการปรับปรุงที่ตามมาในวิชวล Power BI จะเกิดขึ้นในหนึ่งในสามรูปแบบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="21144-113">Actions and subsequent updates in Power BI visuals occur in one of these three patterns:</span></span>

* <span data-ttu-id="21144-114">ผู้ใช้โต้ตอบกับวิชวลผ่าน Power BI</span><span class="sxs-lookup"><span data-stu-id="21144-114">User interacts with a visual through Power BI.</span></span>
* <span data-ttu-id="21144-115">ผู้ใช้โต้ตอบกับวิชวลโดยตรง</span><span class="sxs-lookup"><span data-stu-id="21144-115">User interacts with the visual directly.</span></span>
* <span data-ttu-id="21144-116">วิชวลโต้ตอบกับ Power BI</span><span class="sxs-lookup"><span data-stu-id="21144-116">Visual interacts with Power BI.</span></span>

### <a name="user-interacts-with-a-visual-through-power-bi"></a><span data-ttu-id="21144-117">ผู้ใช้โต้ตอบกับวิชวลผ่าน Power BI</span><span class="sxs-lookup"><span data-stu-id="21144-117">User interacts with a visual through Power BI</span></span>

* <span data-ttu-id="21144-118">ผู้ใช้เปิดแผงคุณสมบัติวิชวล</span><span class="sxs-lookup"><span data-stu-id="21144-118">A user opens the visual's properties panel.</span></span>

    <span data-ttu-id="21144-119">เมื่อผู้ใช้เปิดแผงคุณสมบัติของวิชวล Power BI จะได้รับการสนับสนุนวัตถุและคุณสมบัติจาก *ความสามารถไฟล์ .json* ของวิชวล</span><span class="sxs-lookup"><span data-stu-id="21144-119">When a user opens the visual's properties panel, Power BI fetches supported objects and properties from the visual's *capabilities.json* file.</span></span> <span data-ttu-id="21144-120">ในการรับค่าที่แท้จริงของคุณสมบัติ Power BI จะเรียกวิธีการ `enumerateObjectInstances` ของวิชวล</span><span class="sxs-lookup"><span data-stu-id="21144-120">To receive actual values of properties, Power BI calls the `enumerateObjectInstances` method of the visual.</span></span> <span data-ttu-id="21144-121">วิชวลส่งกลับค่าที่แท้จริงของคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="21144-121">The visual returns actual values of properties.</span></span>

    <span data-ttu-id="21144-122">สำหรับข้อมูลเพิ่มเติม ดูที่ [ความสามารถและคุณสมบัติของวิชวล Power BI](capabilities.md)</span><span class="sxs-lookup"><span data-stu-id="21144-122">For more information, see [Capabilities and properties of Power BI visuals](capabilities.md).</span></span>

* <span data-ttu-id="21144-123">ผู้ใช้ [ เปลี่ยนคุณสมบัติของวิชวล](../../visuals/power-bi-visualization-customize-title-background-and-legend.md) ในแผงรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="21144-123">A user [changes a property of the visual](../../visuals/power-bi-visualization-customize-title-background-and-legend.md) in the format panel.</span></span>

    <span data-ttu-id="21144-124">เมื่อผู้ใช้เปลี่ยนค่าของคุณสมบัติในแผงรูปแบบ Power BI จะเรียกใช้วิธีการ `update` ของวิชวล</span><span class="sxs-lookup"><span data-stu-id="21144-124">When a user changes the value of a property in the format panel, Power BI calls the `update` method of the visual.</span></span> <span data-ttu-id="21144-125">Power BI ผ่านในวัตถุ `options` ใหม่ไปยังวิธีการ `update`</span><span class="sxs-lookup"><span data-stu-id="21144-125">Power BI passes in the new `options` object to the `update` method.</span></span> <span data-ttu-id="21144-126">วัตถุประกอบด้วยค่าใหม่</span><span class="sxs-lookup"><span data-stu-id="21144-126">The objects contain the new values.</span></span>

    <span data-ttu-id="21144-127">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ออบเจ็กต์และคุณสมบัติของวิชวล Power BI](objects-properties.md)</span><span class="sxs-lookup"><span data-stu-id="21144-127">For more information, see [Objects and properties of Power BI visuals](objects-properties.md).</span></span>

* <span data-ttu-id="21144-128">ผู้ใช้ปรับขนาดวิชวล</span><span class="sxs-lookup"><span data-stu-id="21144-128">A user resizes the visual.</span></span>

    <span data-ttu-id="21144-129">เมื่อผู้ใช้เปลี่ยนขนาดของวิชวล Power BI เรียกใช้วิธีการ `update` ด้วยวัตถุ `options` ใหม่</span><span class="sxs-lookup"><span data-stu-id="21144-129">When a user changes the size of a visual, Power BI calls the `update` method with the new `options` object.</span></span> <span data-ttu-id="21144-130">วัตถุ `options` มีวัตถุ `viewport` ที่ซ้อนกันที่ประกอบด้วยความกว้างและความสูงใหม่ของวิชวล</span><span class="sxs-lookup"><span data-stu-id="21144-130">The `options` objects have nested `viewport` objects that contain the new width and height of the visual.</span></span>

* <span data-ttu-id="21144-131">ผู้ใช้จะใช้ตัวกรองรายงาน หน้า หรือระดับของวิชวล</span><span class="sxs-lookup"><span data-stu-id="21144-131">A user applies a filter at the report, page, or visual level.</span></span>

    <span data-ttu-id="21144-132">ข้อมูลตัวกรอง Power BI ที่ยึดตามเงื่อนไขตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="21144-132">Power BI filters data based on filter conditions.</span></span> <span data-ttu-id="21144-133">Power BI เรียกใช้วิธีการ `update` ของวิชวลเพื่ออัปเดตวิชวลด้วยข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="21144-133">Power BI calls the `update` method of the visual to update the visual with new data.</span></span>

    <span data-ttu-id="21144-134">วิชวลได้รับการอัปเดตใหม่ของวัตถุ `options` เมื่อมีข้อมูลใหม่ในหนึ่งวัตถุที่มีการซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="21144-134">The visual gets a new update of the `options` objects when there's new data in one of the nested objects.</span></span> <span data-ttu-id="21144-135">การอัปเดตเกิดขึ้นอยู่กับการกำหนดค่าการวางแผนการดูข้อมูลของวิชวล</span><span class="sxs-lookup"><span data-stu-id="21144-135">How the update occurs depends on the data view mapping configuration of the visual.</span></span>

    <span data-ttu-id="21144-136">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ทำความเข้าใจเกี่ยวกับการแมปมุมมองข้อมูลในวิชวล Power BI](dataview-mappings.md)</span><span class="sxs-lookup"><span data-stu-id="21144-136">For more information, see [Understand data view mapping in Power BI visuals](dataview-mappings.md).</span></span>

* <span data-ttu-id="21144-137">ผู้ใช้เลือกจุดข้อมูลในวิชวลอื่นในรายงาน</span><span class="sxs-lookup"><span data-stu-id="21144-137">A user selects a data point in another visual in the report.</span></span>

    <span data-ttu-id="21144-138">เมื่อผู้ใช้เลือกจุดข้อมูลในวิชวลอื่นในรายงาน ตัวกรองหรือ Power BI หรือไฮไลต์จุดข้อมูลที่เลือกและเรียกวิธีการ `update` ของวิชวล</span><span class="sxs-lookup"><span data-stu-id="21144-138">When a user selects a data point in another visual in the report, Power BI filters or highlights the selected data points and calls the visual's `update` method.</span></span> <span data-ttu-id="21144-139">วิชวลได้รับข้อมูลที่ถูกกรองใหม่หรือได้รับข้อมูลเดียวกันกับแถวลำดับของไฮไลต์</span><span class="sxs-lookup"><span data-stu-id="21144-139">The visual gets new filtered data, or it gets the same data with an array of highlights.</span></span>

    <span data-ttu-id="21144-140">สำหรับข้อมูลเพิ่มเติม โปรดดูหัวข้อ [การเน้นจุดข้อมูลในวิชวล Power BI](highlight.md)</span><span class="sxs-lookup"><span data-stu-id="21144-140">For more information, see [Highlight data points in Power BI visuals](highlight.md).</span></span>

* <span data-ttu-id="21144-141">ผู้ใช้เลือกที่คั่นหน้าบนแผงที่คั่นหน้าของรายงาน</span><span class="sxs-lookup"><span data-stu-id="21144-141">A user selects a bookmark in the bookmarks panel of the report.</span></span>

    <span data-ttu-id="21144-142">เมื่อผู้ใช้เลือกที่คั่นหน้าในแผงที่คั่นหน้าของรายงาน หนึ่งในสองการดำเนินการสามารถเกิดขึ้นได้:</span><span class="sxs-lookup"><span data-stu-id="21144-142">When a user selects a bookmark in the report's bookmarks panel, one of two actions can occur:</span></span>

    * <span data-ttu-id="21144-143">Power BI เรียกใช้ฟังก์ชันที่มีการส่งผ่านและลงทะเบียนโดยวิธีการ `registerOnSelectionCallback`</span><span class="sxs-lookup"><span data-stu-id="21144-143">Power BI calls a function that's passed and registered by the `registerOnSelectionCallback` method.</span></span> <span data-ttu-id="21144-144">ฟังก์ชันการเรียกกลับจะรับแถวลำดับของการเลือกสำหรับที่คั่นหน้าที่เหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="21144-144">The callback function gets arrays of selections for the corresponding bookmark.</span></span>

    * <span data-ttu-id="21144-145">Power BI เรียกใช้วิธีการ `update` ด้วยวัตถุ `filter` ที่เหมือนกันกันภายในวัตถุ `options`</span><span class="sxs-lookup"><span data-stu-id="21144-145">Power BI calls the `update` method with a corresponding `filter` object inside the `options` object.</span></span>

    <span data-ttu-id="21144-146">ในกรณีใดที่วิชวลจะต้องเปลี่ยนสถานะตามการเลือกที่ได้รับหรือวัตถุ `filter`</span><span class="sxs-lookup"><span data-stu-id="21144-146">In either case, the visual must change its state according to the received selections or `filter` object.</span></span>

    <span data-ttu-id="21144-147">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับที่คั่นหน้าและตัวกรอง ดู [Visual Filters API ในการแสดงผลด้วยภาพของ Power BI](filter-api.md)</span><span class="sxs-lookup"><span data-stu-id="21144-147">For more information about bookmarks and filters, see [Visual Filters API in Power BI visuals](filter-api.md).</span></span>

### <a name="user-interacts-with-the-visual-directly"></a><span data-ttu-id="21144-148">ผู้ใช้โต้ตอบกับวิชวลโดยตรง</span><span class="sxs-lookup"><span data-stu-id="21144-148">User interacts with the visual directly</span></span>

* <span data-ttu-id="21144-149">ผู้ใช้จะอยู่เหนือการเลื่อนเมาส์บนองค์ประกอบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="21144-149">A user hovers the mouse over a data element.</span></span>

    <span data-ttu-id="21144-150">วิชวลสามารถแสดงข้อมูลเพิ่มเติมเกี่ยวกับจุดข้อมูลผ่าน Power BI Tooltips API</span><span class="sxs-lookup"><span data-stu-id="21144-150">A visual can display more information about a data point through the Power BI Tooltips API.</span></span> <span data-ttu-id="21144-151">เมื่อผู้ใช้อยู่เหนือการเลื่อนเมาส์บนองค์ประกอบวิชวล วิชวลสามารถจัดการเหตุการณ์และแสดงข้อมูลเกี่ยวกับองค์ประกอบคำแนะนำเครื่องมือที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="21144-151">When a user hovers the mouse over a visual element, the visual can handle the event and display data about the associated tooltip element.</span></span> <span data-ttu-id="21144-152">วิชวลสามารถแสดงคำแนะนำเครื่องมือมาตรฐานหรือคำแนะนำเครื่องมือของหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="21144-152">The visual can display either a standard tooltip or a report page tooltip.</span></span>

    <span data-ttu-id="21144-153">สำหรับข้อมูลเพิ่มเติม ดู [คำแนะนำเครื่องมือในวิชวล Power BI](add-tooltips.md)</span><span class="sxs-lookup"><span data-stu-id="21144-153">For more information, see [Tooltips in Power BI visuals](add-tooltips.md).</span></span>

* <span data-ttu-id="21144-154">ผู้ใช้เปลี่ยนคุณสมบัติของวิชวล</span><span class="sxs-lookup"><span data-stu-id="21144-154">A user changes visual properties.</span></span> <span data-ttu-id="21144-155">(ตัวอย่างเช่น ผู้ใช้ขยายแผนผังต้นไม้และวิชวลที่บันทึกในคุณสมบัติวิชวล)</span><span class="sxs-lookup"><span data-stu-id="21144-155">(For example, a user expands a tree and the visual saves state in the visual properties.)</span></span>

    <span data-ttu-id="21144-156">วิชวลสามารถบันทึกค่าคุณสมบัติผ่าน Power BI API</span><span class="sxs-lookup"><span data-stu-id="21144-156">A visual can save properties values through the Power BI API.</span></span> <span data-ttu-id="21144-157">ตัวอย่าง เมื่อผู้ใช้โต้ตอบกับวิชวลและวิชวลต้องการบันทึกหรืออัปเดตค่าคุณสมบัติ วิชวลสามารถเรียกใช้วิธีการ `presistProperties`</span><span class="sxs-lookup"><span data-stu-id="21144-157">For example, when a user interacts with the visual and the visual needs to save or update properties values, the visual can call the `presistProperties` method.</span></span>

* <span data-ttu-id="21144-158">ผู้ใช้เลือก URL</span><span class="sxs-lookup"><span data-stu-id="21144-158">A user selects a URL.</span></span>

    <span data-ttu-id="21144-159">ตามค่าเริ่มต้น วิชวลไม่สามารถเปิด URL ได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="21144-159">By default, a visual can't open a URL directly.</span></span> <span data-ttu-id="21144-160">แทนที่จะเปิด URL ในแท็บใหม่ วิชวลสามารถเรียกใช้วิธีการ `launchUrl` และส่งผ่าน URL เป็นพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="21144-160">Instead, to open a URL in a new tab, the visual can call the `launchUrl` method and pass the URL as a parameter.</span></span>

    <span data-ttu-id="21144-161">สำหรับข้อมูลเพิ่มเติม ดู [สร้างการเปิดใช้ URL](launch-url.md)</span><span class="sxs-lookup"><span data-stu-id="21144-161">For more information, see [Create a launch URL](launch-url.md).</span></span>

* <span data-ttu-id="21144-162">ผู้ใช้ใช้ตัวกรองผ่านวิชวล</span><span class="sxs-lookup"><span data-stu-id="21144-162">A user applies a filter through the visual.</span></span>

    <span data-ttu-id="21144-163">วิชวลสามารถเรียกใช้วิธีการ `applyJsonFilter` และส่งผ่านเงื่อนไขเพื่อกรองข้อมูลในวิชวลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="21144-163">A visual can call the `applyJsonFilter` method and pass conditions to filter for data in other visuals.</span></span> <span data-ttu-id="21144-164">ชนิดตัวกรองที่หลากหลายสามารถใช้งานได้ รวมถึงตัวกรองพื้นฐาน ขั้นสูงและ Tuple</span><span class="sxs-lookup"><span data-stu-id="21144-164">Several types of filters are available, including Basic, Advanced, and Tuple filters.</span></span>

    <span data-ttu-id="21144-165">สำหรับข้อมูลเพิ่มเติม ดู [API ตัวกรองวิชวลในวิชวล Power BI](filter-api.md)</span><span class="sxs-lookup"><span data-stu-id="21144-165">For more information, see [Visual Filters API in Power BI visuals](filter-api.md).</span></span>

* <span data-ttu-id="21144-166">ผู้ใช้เลือกองค์ประกอบในวิชวล</span><span class="sxs-lookup"><span data-stu-id="21144-166">A user selects elements in the visual.</span></span>

    <span data-ttu-id="21144-167">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเลือกในวิชวล Power BI ดู [เพิ่มการโต้ตอบได้โดยใช้การเลือกวิชวลของ Power BI](selection-api.md)</span><span class="sxs-lookup"><span data-stu-id="21144-167">For more information about selections in a Power BI visual, see [Add interactivity by using Power BI visual selections](selection-api.md).</span></span>

### <a name="visual-interacts-with-power-bi"></a><span data-ttu-id="21144-168">วิชวลโต้ตอบกับ Power BI</span><span class="sxs-lookup"><span data-stu-id="21144-168">Visual interacts with Power BI</span></span>

* <span data-ttu-id="21144-169">วิชวลร้องขอข้อมูลเพิ่มเติมจาก Power BI</span><span class="sxs-lookup"><span data-stu-id="21144-169">A visual requests more data from Power BI.</span></span>

    <span data-ttu-id="21144-170">วิชวลสามารถประมวลผลส่วนข้อมูลตามส่วน</span><span class="sxs-lookup"><span data-stu-id="21144-170">A visual processes data part by part.</span></span> <span data-ttu-id="21144-171">วิธีการ API `fetchMoreData` ร้องขอส่วนของข้อมูลต่อไปในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="21144-171">The `fetchMoreData` API method requests the next fragment of data in the dataset.</span></span>

    <span data-ttu-id="21144-172">สำหรับข้อมูลเพิ่มเติม ดู [รับข้อมูลเพิ่มขึ้นจาก Power BI](fetch-more-data.md)</span><span class="sxs-lookup"><span data-stu-id="21144-172">For more information, see [Fetch more data from Power BI](fetch-more-data.md).</span></span>

* <span data-ttu-id="21144-173">ตัวกระตุ้นบริการของเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="21144-173">The event service triggers.</span></span>

    <span data-ttu-id="21144-174">Power BI สามารถส่งออกรายงานไปยัง PDF หรือส่งรายงานโดยอีเมล (ใช้กับเพียงวิชวลที่ได้รับการรับรองแล้ว)</span><span class="sxs-lookup"><span data-stu-id="21144-174">Power BI can export a report to PDF or send a report by e-mail (applies only to certified visuals).</span></span> <span data-ttu-id="21144-175">ในการแจ้งเตือน Power BI ที่แสดงได้สิ้นสุดและวิชวลที่พร้อมสำหรับจับภาพเป็น PDF หรืออีเมล์ วิชวลสามารถเรียกใช้การแสดงเหตุการณ์ API</span><span class="sxs-lookup"><span data-stu-id="21144-175">To notify Power BI that rendering is finished and that the visual is ready to be captured as PDF or e-mail, the visual should call the Rendering Events API.</span></span>

    <span data-ttu-id="21144-176">สำหรับข้อมูลเพิ่มเติม ดู [ส่งออกรายงานจาก Power BI ไปยัง PDF](../../consumer/end-user-pdf.md)</span><span class="sxs-lookup"><span data-stu-id="21144-176">For more information, see [Export reports from Power BI to PDF](../../consumer/end-user-pdf.md).</span></span>

    <span data-ttu-id="21144-177">ในการเรียนรู้เกี่ยวกับการบริการเหตุการณ์ ดู [แสดงเหตุการณ์ในวิชวล](event-service.md)</span><span class="sxs-lookup"><span data-stu-id="21144-177">To learn about the event service, see [Render events in Power BI visuals](event-service.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="21144-178">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="21144-178">Next steps</span></span>

<span data-ttu-id="21144-179">สนใจในการสร้างการแสดงด้วยภาพและเพิ่มสิ่งเหล่านั้นไปยัง Microsoft AppSource หรือไม่</span><span class="sxs-lookup"><span data-stu-id="21144-179">Interested in creating visualizations and adding them to Microsoft AppSource?</span></span> <span data-ttu-id="21144-180">ดูบทความเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="21144-180">See these articles:</span></span>

* [<span data-ttu-id="21144-181">การพัฒนาวิชวลการ์ดวงกลมใน Power BI</span><span class="sxs-lookup"><span data-stu-id="21144-181">Developing a Power BI circle card visual</span></span>](./develop-circle-card.md)
* [<span data-ttu-id="21144-182">เผยแพร่วิชวล Power BI ให้กับ Partner Center</span><span class="sxs-lookup"><span data-stu-id="21144-182">Publish Power BI visuals to Partner Center</span></span>](office-store.md)
