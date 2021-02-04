---
title: เพิ่มตัวกรองไปยังรายงานใน Power BI
description: เพิ่มตัวกรองหน้า การแสดงภาพกรอง หรือตัวกรองรายงานในรายงานใน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 10/20/2019
LocalizationGroup: Reports
ms.openlocfilehash: 113370dd6b3aa19546f1facada6abc07c12b9d1a
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96389126"
---
# <a name="add-a-filter-to-a-report-in-power-bi"></a><span data-ttu-id="90aa1-103">เพิ่มตัวกรองไปยังรายงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="90aa1-103">Add a filter to a report in Power BI</span></span>

[!INCLUDE [power-bi-service-new-look-include](../includes/power-bi-service-new-look-include.md)]

<span data-ttu-id="90aa1-104">บทความนี้จะอธิบายวิธีเพิ่มตัวกรองหน้า, ตัวกรองการแสดงภาพ, ตัวกรองรายงาน หรือตัวกรอง drillthrough ไปยังรายงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="90aa1-104">This article explains how to add a page filter, visualization filter, report filter, or drillthrough filter to a report in Power BI.</span></span> <span data-ttu-id="90aa1-105">ตัวอย่างในบทความนี้จะอยู่ในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="90aa1-105">The examples in this article are in the Power BI service.</span></span> <span data-ttu-id="90aa1-106">ขั้นตอนแทบจะเหมือนกันเกือบทั้งหมดใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="90aa1-106">The steps are almost identical in Power BI Desktop.</span></span>

<span data-ttu-id="90aa1-107">**คุณทราบหรือไม่**</span><span class="sxs-lookup"><span data-stu-id="90aa1-107">**Did you know?**</span></span> <span data-ttu-id="90aa1-108">Power BI มีการใช้งานตัวกรองใหม่</span><span class="sxs-lookup"><span data-stu-id="90aa1-108">Power BI has a new filter experience.</span></span> <span data-ttu-id="90aa1-109">อ่านเพิ่มเติมเกี่ยวกับ[การใช้งานตัวกรองใหม่ในรายงาน Power BI](power-bi-report-filter.md)</span><span class="sxs-lookup"><span data-stu-id="90aa1-109">Read more about [the new filter experience in Power BI reports](power-bi-report-filter.md).</span></span>

![ประสบการณ์ใช้งานตัวกรองใหม่](media/power-bi-report-add-filter/power-bi-filter-reading.png)

<span data-ttu-id="90aa1-111">Power BI มีตัวกรองหลายชนิด ตั้งแต่ชนิดแมนนวลและชนิดอัตโนมัติไปจนถึงชนิดเจาะลึกรายละเอียดและชนิดพาส-ทรู</span><span class="sxs-lookup"><span data-stu-id="90aa1-111">Power BI offers a number of different kinds of filters, from the manual and automatic to the drill-through and pass-through.</span></span> <span data-ttu-id="90aa1-112">อ่านเกี่ยวกับ [ตัวกรองประเภทต่าง ๆ](power-bi-report-filter-types.md)</span><span class="sxs-lookup"><span data-stu-id="90aa1-112">Read about the [different kinds of filters](power-bi-report-filter-types.md).</span></span>

## <a name="filters-in-editing-view-or-reading-view"></a><span data-ttu-id="90aa1-113">ตัวกรองในมุมมองการแก้ไขและมุมมองการอ่าน</span><span class="sxs-lookup"><span data-stu-id="90aa1-113">Filters in Editing view or Reading view</span></span>
<span data-ttu-id="90aa1-114">คุณสามารถโต้ตอบกับรายงานในสองมุมมอง คือ มุมมองการอ่าน และมุมมองการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="90aa1-114">You can interact with reports in two different views: Reading view and Editing view.</span></span> <span data-ttu-id="90aa1-115">ความสามารถในการกรองที่พร้อมใช้งานสำหรับคุณจะขึ้นอยู่กับมุมมองที่เลือก</span><span class="sxs-lookup"><span data-stu-id="90aa1-115">The filtering capabilities available to you depend on which view you're in.</span></span> <span data-ttu-id="90aa1-116">อ่านรายละเอียด [เกี่ยวกับตัวกรองและการไฮไลท์ในรายงาน Power BI](power-bi-reports-filters-and-highlighting.md) ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="90aa1-116">Read all [about filters and highlighting in Power BI reports](power-bi-reports-filters-and-highlighting.md) for details.</span></span>

<span data-ttu-id="90aa1-117">บทความนี้จะอธิบายวิธีการสร้างตัวกรองใน **มุมมองการแก้ไข** ของรายงาน</span><span class="sxs-lookup"><span data-stu-id="90aa1-117">This article describes how to create filters in report **Editing view**.</span></span>  <span data-ttu-id="90aa1-118">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวกรองในมุมมองการอ่าน สามารถดูได้ที่ [โต้ตอบกับตัวกรองในมุมมองการอ่านของรายงาน](../consumer/end-user-report-filter.md)</span><span class="sxs-lookup"><span data-stu-id="90aa1-118">For more information on filters in Reading view, see [interacting with filters in report Reading view](../consumer/end-user-report-filter.md).</span></span>

<span data-ttu-id="90aa1-119">เนื่องจากตัวกรองยัง *คงอยู่* เมื่อคุณนำทางออกจากรายงาน Power BI ยังคงรักษาการเปลี่ยนแปลงของตัวกรอง, ตัวแบ่งส่วนข้อมูล และการเปลี่ยนแปลงของมุมมองข้อมูลอื่น ๆ ที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="90aa1-119">Because filters *persist*, when you navigate away from the report Power BI retains the filter, slicer, and other data view changes that you've made.</span></span> <span data-ttu-id="90aa1-120">ดังนั้นคุณจะสามารถกลับไปทำงานที่ค้างไว้ได้ เมื่อคุณกลับไปยังรายงาน</span><span class="sxs-lookup"><span data-stu-id="90aa1-120">So you can pick up where you left off when you return to the report.</span></span> <span data-ttu-id="90aa1-121">หากคุณไม่ต้องการเก็บการเปลี่ยนแปลงตัวกรองไว้ ให้เลือก **รีเซ็ตเป็นค่าเริ่มต้น** จากแถบเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="90aa1-121">If you don't want your filter changes to persist, select **Reset to default** from the top menubar.</span></span>

![ปุ่มตัวกรองที่ยังคงอยู่](media/power-bi-report-add-filter/power-bi-reset-to-default.png)

## <a name="levels-of-filters-in-the-filters-pane"></a><span data-ttu-id="90aa1-123">ระดับของตัวกรองในบานหน้าต่างตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="90aa1-123">Levels of filters in the Filters pane</span></span>
<span data-ttu-id="90aa1-124">ไม่ว่าคุณกำลังใช้บริการ Desktop หรือ Power BI บานหน้าต่างตัวกรองจะแสดงตามแนวทางด้านขวาของพื้นที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="90aa1-124">Whether you're using Desktop or Power BI service, the Filters pane displays along the right side of the report canvas.</span></span> <span data-ttu-id="90aa1-125">ถ้าคุณไม่เห็นบานหน้าต่างตัวกรอง เลือกแบบ " > " ไอคอนจากมุมขวาบนเพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="90aa1-125">If you don't see the Filters pane, select the ">" icon from the upper-right corner to expand it.</span></span>

<span data-ttu-id="90aa1-126">คุณสามารถตั้งค่าตัวกรองได้สามระดับสำหรับรายงาน ได้แก่: ตัวกรองระดับการแสดงผลด้วยภาพ ระดับหน้า และระดับรายงาน</span><span class="sxs-lookup"><span data-stu-id="90aa1-126">You can set filters at three different levels for the report: visual-level, page-level, and report-level filters.</span></span> <span data-ttu-id="90aa1-127">คุณยังสามารถตั้งค่าตัวกรองแบบเจาะลึกรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="90aa1-127">You can also set drillthrough filters.</span></span> <span data-ttu-id="90aa1-128">บทความนี้อธิบายถึงระดับต่างๆ</span><span class="sxs-lookup"><span data-stu-id="90aa1-128">This article explains the different levels.</span></span>

![บานหน้าต่างตัวกรองในมุมมองการอ่าน](media/power-bi-report-add-filter/power-bi-add-filter-reading-view.png)

## <a name="add-a-filter-to-a-visual"></a><span data-ttu-id="90aa1-130">เพิ่มตัวกรองลงในวิชวล</span><span class="sxs-lookup"><span data-stu-id="90aa1-130">Add a filter to a visual</span></span>
<span data-ttu-id="90aa1-131">มีสองวิธีที่คุณสามารถเพิ่มตัวกรองระดับการแสดงผลด้วยภาพไปยังการแสดงผลด้วยภาพที่เฉพาะเจาะจง </span><span class="sxs-lookup"><span data-stu-id="90aa1-131">You can add a visual-level filter to a specific visual in two different ways.</span></span> 

* <span data-ttu-id="90aa1-132">โดยการกรองเขตข้อมูลที่กำลังถูกใช้โดยการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="90aa1-132">Filter a field that is already being used by the visualization.</span></span>
* <span data-ttu-id="90aa1-133">โดยการระบุเขตข้อมูลที่ไม่ถูกใช้แล้วโดยการแสดงภาพ และเพิ่มเขตข้อมูลนั้นโดยตรงไปยังบักเก็ต **ตัวกรองระดับภาพ**</span><span class="sxs-lookup"><span data-stu-id="90aa1-133">Identify a field that is not already being used by the visualization, and add that field directly to the **Visual level filters** bucket.</span></span>


<span data-ttu-id="90aa1-134">อนึ่ง กระบวนงานนี้ใช้ตัวอย่างการวิเคราะห์ร้านค้าปลีก หากคุณต้องการดาวน์โหลดและทำตามไปด้วย</span><span class="sxs-lookup"><span data-stu-id="90aa1-134">By the way, this procedure uses the Retail Analysis sample, if you'd like to download it and follow along.</span></span> <span data-ttu-id="90aa1-135">ดาวน์โหลดชุดเนื้อหา[ตัวอย่างการวิเคราะห์ร้านค้าปลีก](sample-retail-analysis.md#get-the-content-pack-for-this-sample)</span><span class="sxs-lookup"><span data-stu-id="90aa1-135">Download the [Retail Analysis sample](sample-retail-analysis.md#get-the-content-pack-for-this-sample) content pack.</span></span>

### <a name="filter-the-fields-in-the-visual"></a><span data-ttu-id="90aa1-136">กรองเขตข้อมูลในภาพ</span><span class="sxs-lookup"><span data-stu-id="90aa1-136">Filter the fields in the visual</span></span>

1. <span data-ttu-id="90aa1-137">เลือก **ตัวเลือกอื่นๆ (...)**  > **แก้ไขรายงาน** เพื่อเปิดรายงานในมุมมองการแก้ไขของคุณ</span><span class="sxs-lookup"><span data-stu-id="90aa1-137">Select **More options (...)** > **Edit report** to open your report in Editing view.</span></span>
   
   ![แก้ไขปุ่มรายงาน](media/power-bi-report-add-filter/power-bi-edit-view.png)

2. <span data-ttu-id="90aa1-139">เปิดบานหน้าต่างการจัดรูปแบบข้อมูลและตัวกรองและบานหน้าต่างเขตข้อมูล (ถ้าพวกเขายังไม่ได้อยู่เปิด)</span><span class="sxs-lookup"><span data-stu-id="90aa1-139">Open the Visualizations and Filters pane and the Fields pane (if they're not already open).</span></span>
   
   ![บานหน้าต่างการแสดงภาพ ตัวกรอง และเขตข้อมูล](media/power-bi-report-add-filter/power-bi-display-panes.png)
3. <span data-ttu-id="90aa1-141">เลือกการแสดงภาพเพื่อเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="90aa1-141">Select a visual to make it active.</span></span> <span data-ttu-id="90aa1-142">เขตข้อมูลทั้งหมดที่ถูกใช้ โดยภาพจะอยู่บานหน้าต่าง **เขตข้อมูล** และยังแสดงอยู่ในบานหน้าต่าง **ตัวกรอง** ใต้หัวเรื่อง **ตัวกรองระดับภาพ**</span><span class="sxs-lookup"><span data-stu-id="90aa1-142">All the fields being used by the visual are in the **Fields** pane and also listed in the **Filters** pane, under the **Visual level filters** heading.</span></span>
   
   ![เลือกตัวกรองระดับการแสดงผลด้วยภาพ](media/power-bi-report-add-filter/power-bi-default-visual-filter.png)
4. <span data-ttu-id="90aa1-144">ในตอนนี้ เราจะเพิ่มตัวกรองลงในเขตข้อมูลที่ถูกใช้แล้ว โดยการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="90aa1-144">At this point, we'll add a filter to a field already being used by the visualization.</span></span> 
   
    <span data-ttu-id="90aa1-145">เลื่อนลงไป **ตัวกรองระดับการมองเห็น** พื้นที่แล้วเลือกลูกศรเพื่อขยายเขตข้อมูลคุณต้องการกรอง</span><span class="sxs-lookup"><span data-stu-id="90aa1-145">Scroll down to the **Visual level filters** area and select the arrow to expand the field you'd like to filter.</span></span> <span data-ttu-id="90aa1-146">ในตัวอย่างนี้ เราจะกรอง **StoreNumberName**</span><span class="sxs-lookup"><span data-stu-id="90aa1-146">In this example, we'll filter **StoreNumberName**.</span></span>
     
    ![ลูกศรขยายตัวกรอง](media/power-bi-report-add-filter/power-bi-visual-level-filter.png) 
    
    <span data-ttu-id="90aa1-148">ตั้งค่าการควบคุมการกรองแบบ **พื้นฐาน**, **ขั้นสูง** หรือ **Top N** อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="90aa1-148">Set either **Basic**, **Advanced**, or **Top N** filtering controls.</span></span> <span data-ttu-id="90aa1-149">ในตัวอย่างนี้ เราจะค้นหาในการกรองพื้นฐานสำหรับ **cha** และเลือกร้านค้าทั้งห้าเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="90aa1-149">In this example, we'll search in Basic filtering for **cha** and select those five stores.</span></span>
     
    ![ค้นหาในการกรองพื้นฐาน](media/power-bi-report-add-filter/power-bi-search-filter.png) 
   
    <span data-ttu-id="90aa1-151">เปลี่ยนแปลงภาพเพื่อแสดงตัวกรองใหม่</span><span class="sxs-lookup"><span data-stu-id="90aa1-151">The visual changes to reflect the new filter.</span></span> <span data-ttu-id="90aa1-152">หากคุณบันทึกรายงานของคุณกับตัวกรอง ผู้อ่านรายงานจะสามารถเห็นภาพที่กรองเป็นอย่างแรก และสามารถโต้ตอบกับตัวกรองในมุมมองการอ่านที่เลือก หรือยกเลิกค่า</span><span class="sxs-lookup"><span data-stu-id="90aa1-152">If you save your report with the filter, report readers will see the visual filtered to begin with, and can interact with the filter in Reading view, selecting or clearing values.</span></span>
     
    ![สกรีนช็อตแสดงแผนภูมิแท่งที่สะท้อนค่าที่กรองแล้ว](media/power-bi-report-add-filter/power-bi-search-visual-filter-results.png)
    
    <span data-ttu-id="90aa1-154">เมื่อคุณใช้ตัวกรองบนเขตข้อมูลที่ใช้ในวิชวลที่รวมเขตข้อมูล (ตัวอย่างเช่น sum, value, หรือ count) คุณกำลังกรองค่า *รวม* ในแต่ละจุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="90aa1-154">When you use the filter on a field used in the visual where the field is aggregated (for example a sum, average, or count), you're filtering on the *aggregated* value in each data point.</span></span> <span data-ttu-id="90aa1-155">ดังนั้นขอให้กรองวิชวลข้างต้นที่ **ยอดขายในปีนี้ > 500,000**  หมายความว่าคุณจะเห็นเฉพาะจุดข้อมูล **13 - Charleston Fashion Direct** เท่านั้นในผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="90aa1-155">So, asking to filter the visual above where **This Year Sales > 500000** means you would see only the **13 - Charleston Fashion Direct** data point in the result.</span></span> <span data-ttu-id="90aa1-156">ตัวกรองบน [หน่วยวัดแบบจำลอง](../transform-model/desktop-measures.md) จะนำไปใช้กับค่ารวมของจุดข้อมูลเสมอ</span><span class="sxs-lookup"><span data-stu-id="90aa1-156">Filters on [model measures](../transform-model/desktop-measures.md) always apply to the aggregated value of the data point.</span></span>

### <a name="filter-with-a-field-thats-not-in-the-visual"></a><span data-ttu-id="90aa1-157">กรองด้วยเขตข้อมูลที่ไม่ได้อยู่ในภาพ</span><span class="sxs-lookup"><span data-stu-id="90aa1-157">Filter with a field that's not in the visual</span></span>

<span data-ttu-id="90aa1-158">ตอนนี้มาเพิ่มเขตข้อมูลใหม่ไปยังการแสดงภาพเป็นตัวกรองระดับภาพกัน</span><span class="sxs-lookup"><span data-stu-id="90aa1-158">Now let's add a new field to our visualization as a visual-level filter.</span></span>
   
1. <span data-ttu-id="90aa1-159">จากบานหน้าต่างเขตข้อมูล เลือกเขตข้อมูลที่ต้องการเพิ่มเป็นตัวกรองระดับภาพใหม่ และลากลงในการ **พื้นที่ตัวกรองระดับภาพ**</span><span class="sxs-lookup"><span data-stu-id="90aa1-159">From the Fields pane, select the field you want to add as a new visual-level filter, and drag it into the **Visual level filters area**.</span></span>  <span data-ttu-id="90aa1-160">ในตัวอย่างนี้ เราจะลาก **ผู้จัดการเขต** ลงในบักเก็ต **ตัวกรองระดับภาพ** ค้นหา **an** และเลือกผู้จัดการทั้งสามเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="90aa1-160">In this example, we'll drag **District Manager** into the **Visual level filters** bucket, search for **an**, and select those three managers.</span></span>
     
    ![เพิ่มเขตข้อมูลไปยังบานหน้าต่างตัวกรอง](media/power-bi-report-add-filter/power-bi-search-add-visual-filter.png)

    <span data-ttu-id="90aa1-162">โปรดสังเกตว่า \**ผู้จัดการเขต\*\*\*ไม่* ได้ถูกเพิ่มลงในการแสดงภาพของตัวเอง</span><span class="sxs-lookup"><span data-stu-id="90aa1-162">Notice **District Manager** is *not* added to the visualization itself.</span></span> <span data-ttu-id="90aa1-163">การแสดงภาพจะยังประกอบด้วย **StoreNumberName** เป็นแกน และ **ยอดขายของปีนี้** เป็นค่า</span><span class="sxs-lookup"><span data-stu-id="90aa1-163">The visualization is still composed of **StoreNumberName** as the Axis and **This Year Sales** as the Value.</span></span>  
     
    ![เขตข้อมูลไม่ได้อยู่ในการแสดงผลด้วยภาพ](media/power-bi-report-add-filter/power-bi-visualization.png)

    <span data-ttu-id="90aa1-165">และ ตอนนี้มีการกรองข้อมูลการแสดงภาพของตัวเองเพื่อแสดงยอดขายปีนี้ของผู้จัดการสำหรับร้านค้าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="90aa1-165">And the visualization itself is now filtered to show only those managers' sales this year for the specified stores.</span></span>
     
    ![สกรีนช็อตแสดงแผนภูมิแท่งที่สะท้อนค่าที่กรองโดยยึดตามเขตข้อมูลใหม่](media/power-bi-report-add-filter/power-bi-search-visual-filter-results-2.png)

    <span data-ttu-id="90aa1-167">หากคุณบันทึกรายงานของคุณกับตัวกรองนี้ ผู้อ่านรายงานจะสามารถโต้ตอบกับตัวกรอง **ผู้จัดการเขต** ในมุมมองการอ่านที่เลือกหรือยกเลิกค่า</span><span class="sxs-lookup"><span data-stu-id="90aa1-167">If you save your report with this filter, report readers can interact with the **District Manager** filter in Reading view, selecting or clearing values.</span></span>
    
    <span data-ttu-id="90aa1-168">ถ้าคุณลาก *คอลัมน์ตัวเลข* ไปยังบานหน้าต่างตัวกรอง เพื่อสร้างตัวกรองระดับ วิชวลตัวกรองจะถูกนำไปใช้กับ *แถวข้อมูลพื้นฐาน*</span><span class="sxs-lookup"><span data-stu-id="90aa1-168">If you drag a *numeric column* to the filter pane to create a visual-level filter, the filter is applied to the *underlying rows of data*.</span></span> <span data-ttu-id="90aa1-169">ตัวอย่างเช่น การเพิ่มตัวกรองบนเขตข้อมูล **UnitCost** และการตั้งค่าที่ **UnitCost** > 20 จะแสดงเฉพาะข้อมูลสำหรับแถวผลิตภัณฑ์ที่ต้นทุนต่อหน่วยมีค่ามากกว่า 20 โดยไม่คำนึงถึงต้นทุนต่อหน่วยทั้งหมดสำหรับจุดข้อมูลที่แสดงในวิชวล</span><span class="sxs-lookup"><span data-stu-id="90aa1-169">For example, adding a filter on the **UnitCost** field and setting it where **UnitCost** > 20 would only show data for the Product rows where the Unit Cost was greater than 20, regardless of the total Unit Cost for the data points shown in the visual.</span></span>

## <a name="add-a-filter-to-an-entire-page"></a><span data-ttu-id="90aa1-170">เพิ่มตัวกรองไปยังหน้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="90aa1-170">Add a filter to an entire page</span></span>

<span data-ttu-id="90aa1-171">นอกจากนี้ คุณยังสามารถเพิ่มตัวกรองระดับหน้าเพื่อกรองหน้าทั้งหน้า</span><span class="sxs-lookup"><span data-stu-id="90aa1-171">You can also add a page-level filter to filter an entire page.</span></span>

1. <span data-ttu-id="90aa1-172">ในบริการของ Power BI ให้เปิดรายงานการวิเคราะห์ด้านการขายปลีกแล้วไปที่หน้า **ยอดขายรายเดือนในแต่ละเขต**</span><span class="sxs-lookup"><span data-stu-id="90aa1-172">In the Power BI service, open the Retail Analysis report, then go to the **District Monthly Sales** page.</span></span> 

2. <span data-ttu-id="90aa1-173">เลือก **...**  > **แก้ไขรายงาน** เพื่อเปิดรายงานของคุณในมุมมองการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="90aa1-173">Select **...** > **Edit report** to open your report in Editing view.</span></span>
   
   ![แก้ไขปุ่มรายงาน](media/power-bi-report-add-filter/power-bi-edit-view.png)
2. <span data-ttu-id="90aa1-175">เปิดบานหน้าต่างการจัดรูปแบบข้อมูลและตัวกรองและบานหน้าต่างเขตข้อมูล (ถ้าพวกเขายังไม่ได้อยู่เปิด)</span><span class="sxs-lookup"><span data-stu-id="90aa1-175">Open the Visualizations and Filters pane and the Fields pane (if they're not already open).</span></span>
3. <span data-ttu-id="90aa1-176">จากบานหน้าต่างเขตข้อมูล เลือกเขตข้อมูลที่ต้องการเพิ่มเป็นตัวกรองระดับภาพใหม่ และลากลงในพื้นที่ **ตัวกรองระดับหน้า**</span><span class="sxs-lookup"><span data-stu-id="90aa1-176">From the Fields pane, select the field you want to add as a new page-level filter, and drag it into the **Page level filters** area.</span></span>  
4. <span data-ttu-id="90aa1-177">เลือกค่าที่ต้องการกรอง และตั้งค่ากรองตัวการควบคุมการกรองแบบ **พื้นฐาน** หรือ **ขั้นสูง** อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="90aa1-177">Select the values you want to filter and set either  **Basic** or **Advanced** filtering controls.</span></span>
   
   <span data-ttu-id="90aa1-178">การแสดงภาพทั้งหมดบนหน้ามีการวาดอีกครั้งเพื่อแสดงการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="90aa1-178">All the visualizations on the page are redrawn to reflect the change.</span></span>
   
   ![เพิ่มตัวกรองและเลือกค่า](media/power-bi-report-add-filter/filterpage.gif)

    <span data-ttu-id="90aa1-180">หากคุณบันทึกรายงานของคุณกับตัวกรอง ผู้อ่านรายงานจะสามารถโต้ตอบกับตัวกรองในมุมมองการอ่านที่เลือกหรือยกเลิกค่า</span><span class="sxs-lookup"><span data-stu-id="90aa1-180">If you save your report with the filter, report readers can interact with the filter in Reading view, selecting or clearing values.</span></span>

## <a name="add-a-drillthrough-filter"></a><span data-ttu-id="90aa1-181">ตัวกรอง Drillthrough</span><span class="sxs-lookup"><span data-stu-id="90aa1-181">Add a drillthrough filter</span></span>
<span data-ttu-id="90aa1-182">ด้วยหากต้องการเข้าถึงรายละเอียดในบริการ Power BI และ Power BI Desktop คุณสามารถสร้างการ *ปลายทาง* หน้ารายงานที่มุ่งเน้นเฉพาะเจาะจงเอนทิตี - เช่นผู้ ขาย หรือลูกค้า หรือผู้ผลิต ได้</span><span class="sxs-lookup"><span data-stu-id="90aa1-182">With drillthrough in Power BI service and Power BI Desktop, you can create a *destination* report page that focuses on a specific entity - such as a supplier, or customer, or manufacturer.</span></span> <span data-ttu-id="90aa1-183">ตอนนี้ จากรายงานหน้าอื่น ๆ ผู้ใช้สามารถคลิกขวาบนจุดข้อมูลสำหรับเอนทิตีและเข้าถึงรายละเอียดไปยังหน้าโฟกัสนั้น</span><span class="sxs-lookup"><span data-stu-id="90aa1-183">Now, from the other report pages, users can right-click on a data point for that entity and drillthrough to the focused page.</span></span>

### <a name="create-a-drillthrough-filter"></a><span data-ttu-id="90aa1-184">การสร้างตัวกรอง Drillthrough</span><span class="sxs-lookup"><span data-stu-id="90aa1-184">Create a drillthrough filter</span></span>
<span data-ttu-id="90aa1-185">หากต้องการทำตาม ให้ดาวน์โหลด [ตัวอย่างการทำกำไรลูกค้า](sample-customer-profitability.md#get-the-content-pack-for-this-sample)</span><span class="sxs-lookup"><span data-stu-id="90aa1-185">To follow along, download the [Customer Profitability sample](sample-customer-profitability.md#get-the-content-pack-for-this-sample).</span></span> <span data-ttu-id="90aa1-186">สมมติว่าคุณต้องการสร้างให้หน้าหนึ่งหน้ามีความมุ่งเน้นพื้นที่ธุรกิจผู้บริหาร</span><span class="sxs-lookup"><span data-stu-id="90aa1-186">Let's say that you want a page that focuses on Executive business areas.</span></span>

1. <span data-ttu-id="90aa1-187">ในบริการของ Power BI ให้เปิดรายงานการวิเคราะห์ด้านการขายปลีกแล้วไปที่หน้า **ยอดขายรายเดือนในแต่ละเขต**</span><span class="sxs-lookup"><span data-stu-id="90aa1-187">In the Power BI service, open the Retail Analysis report, then go to the **District Monthly Sales** page.</span></span>

2. <span data-ttu-id="90aa1-188">เลือก **ตัวเลือกอื่นๆ (...)**  > **แก้ไขรายงาน** เพื่อเปิดรายงานในมุมมองการแก้ไขของคุณ</span><span class="sxs-lookup"><span data-stu-id="90aa1-188">Select **More options (...)** > **Edit report** to open your report in Editing view.</span></span>
   
   ![แก้ไขปุ่มรายงาน](media/power-bi-report-add-filter/power-bi-edit-view.png)

1. <span data-ttu-id="90aa1-190">เพิ่มหน้าใหม่ลงในรายงาน และตั้งชื่อเป็น **ทีมผู้บริหาร**</span><span class="sxs-lookup"><span data-stu-id="90aa1-190">Add a new page to the report and name it **Team Executive**.</span></span> <span data-ttu-id="90aa1-191">นี่จะเป็นการเข้าถึงรายละเอียด *ปลายทาง* หน้า</span><span class="sxs-lookup"><span data-stu-id="90aa1-191">This page will be the drillthrough *destination*.</span></span>
2. <span data-ttu-id="90aa1-192">เพิ่มการแสดงภาพที่ติดตามเมตริกหลักสำหรับพื้นที่ทางธุรกิจของผู้บริหารทีม</span><span class="sxs-lookup"><span data-stu-id="90aa1-192">Add visualizations that track key metrics for the team executives' business areas.</span></span>    
3. <span data-ttu-id="90aa1-193">จากตาราง **ผู้บริหาร** ลากคำว่า **ผู้บริหาร** เมื่อต้องการเข้าถึงรายละเอียดตัวกรองได้ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="90aa1-193">From the **Executives** table, drag **Executive** to the Drillthrough filters well.</span></span>    
   
    ![เพิ่มค่าลงในตัวกรองแบบเจาะลึกรายละเอียด](media/power-bi-report-add-filter/power-bi-drillthrough-filter.png)
   
    <span data-ttu-id="90aa1-195">โปรดสังเกตว่า Power BI เพิ่มเป็นลูกศรย้อนกลับไปยังหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="90aa1-195">Notice that Power BI adds a back arrow to the report page.</span></span>  <span data-ttu-id="90aa1-196">เลือกลูกศรย้อนกลับคืนค่าผู้ใช้รายงาน *ต้นฉบับ* หน้าที่พวกเขาทำงานอยู่เมื่อพวกเขาร่วมการเข้าถึงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="90aa1-196">Selecting the back arrow returns users to the *originating* report page -- the page they were on when they opted to drillthrough.</span></span> <span data-ttu-id="90aa1-197">ในมุมมองการแก้ไขให้กดแป้น Ctrl ค้างไว้เพื่อเลือกลูกศรย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="90aa1-197">In Editing view, hold down the Ctrl key to select the back arrow</span></span>
   
     ![ลูกศรย้อนกลับ](media/power-bi-report-add-filter/power-bi-back-arrow.png)

### <a name="use-the-drillthrough-filter"></a><span data-ttu-id="90aa1-199">ตัวกรอง Drillthrough</span><span class="sxs-lookup"><span data-stu-id="90aa1-199">Use the drillthrough filter</span></span>
<span data-ttu-id="90aa1-200">มาดูวิธีการทำงานของตัวกรองการเข้าถึงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="90aa1-200">Let's see how the drillthrough filter works.</span></span>

1. <span data-ttu-id="90aa1-201">เริ่มต้นบนการ **ดัชนีชี้วัดทีม** หน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="90aa1-201">Start on the **Team Scorecard** report page.</span></span>    
2. <span data-ttu-id="90aa1-202">สมมติว่าคุณคือ Andrew Ma และคุณต้องการดูหน้ารายงานทีมผู้บริหารที่ถูกกรองเพียงข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="90aa1-202">Let's say you're Andrew Ma and you want to see the Team Executive report page filtered to just your data.</span></span>  <span data-ttu-id="90aa1-203">จากแผนภูมิพื้นที่ด้านบนซ้าย ให้คลิกขวาที่จุดข้อมูลสีเขียวใด ๆ เพื่อเปิดตัวเลือกเมนูการเจาะลึกรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="90aa1-203">From the top-left area chart, right-click any green data point to open the Drillthrough menu option.</span></span>
   
    ![เริ่มการดำเนินการเจาะลึก](media/power-bi-report-add-filter/power-bi-drillthrough.png)
3. <span data-ttu-id="90aa1-205">เลือก **Drillthrough > ทีมผู้บริหาร** เมื่อต้องการเข้าถึงรายละเอียดไปยังหน้ารายงานมีชื่อว่า **ทีมผู้บริหาร**</span><span class="sxs-lookup"><span data-stu-id="90aa1-205">Select **Drillthrough > Team Executive** to drillthrough to the report page named **Team Executive**.</span></span> <span data-ttu-id="90aa1-206">หน้าจะถูกกรองให้แสดงข้อมูลเกี่ยวกับจุดข้อมูลที่คุณคลิกขวา ใน Andrew Ma นี้กรณีและปัญหา</span><span class="sxs-lookup"><span data-stu-id="90aa1-206">The page is filtered to show information about the data point from which you right-clicked; in this case Andrew Ma.</span></span> <span data-ttu-id="90aa1-207">ตัวกรองใดๆ บนหน้าเริ่มต้นจะถูกนำไปใช้กับหน้ารายงาน drillthrough</span><span class="sxs-lookup"><span data-stu-id="90aa1-207">Any filters on the originating page are applied to the drillthrough report page.</span></span>  
   
    ![เริ่มการดำเนินการเจาะลึก](media/power-bi-report-add-filter/power-bi-drillthrough-executive.png)

## <a name="add-a-report-level-filter-to-filter-an-entire-report"></a><span data-ttu-id="90aa1-209">เพิ่มตัวกรองระดับรายงานเพื่อกรองรายงานทั้งฉบับ</span><span class="sxs-lookup"><span data-stu-id="90aa1-209">Add a report-level filter to filter an entire report</span></span>

1. <span data-ttu-id="90aa1-210">เลือก **แก้ไขรายงาน** เพื่อเปิดรายงานในมุมมองการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="90aa1-210">Select **Edit report** to open the report in Editing view.</span></span>
   
   ![แก้ไขปุ่มรายงาน](media/power-bi-report-add-filter/power-bi-edit-view.png)

2. <span data-ttu-id="90aa1-212">เปิดบานหน้าต่างการจัดรูปแบบข้อมูลและตัวกรองและบานหน้าต่างเขตข้อมูล หากยังไม่ได้เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="90aa1-212">Open the Visualizations and Filters pane and the Fields pane, if they're not already open.</span></span>
3. <span data-ttu-id="90aa1-213">จากบานหน้าต่างเขตข้อมูล เลือกเขตข้อมูลที่คุณต้องการเพิ่มเป็นตัวกรองระดับภาพใหม่ และลากลงในพื้นที่ **ตัวกรองระดับภาพ**</span><span class="sxs-lookup"><span data-stu-id="90aa1-213">From the Fields pane, select the field you want to add as a new report-level filter, and drag it into the **Report level filters** area.</span></span>  
4. <span data-ttu-id="90aa1-214">เลือกค่าที่คุณต้องการกรอง</span><span class="sxs-lookup"><span data-stu-id="90aa1-214">Select the values you want to filter.</span></span>

    <span data-ttu-id="90aa1-215">ภาพบนหน้าที่ทำงาน และหน้าทั้งหมดในรายงาน เปลี่ยนแปลงเพื่อแสดงตัวกรองใหม่</span><span class="sxs-lookup"><span data-stu-id="90aa1-215">The visuals on the active page, and on all pages in the report, change to reflect the new filter.</span></span> <span data-ttu-id="90aa1-216">หากคุณบันทึกรายงานของคุณกับตัวกรอง ผู้อ่านรายงานจะสามารถโต้ตอบกับตัวกรองในมุมมองการอ่านที่เลือกหรือยกเลิกค่า</span><span class="sxs-lookup"><span data-stu-id="90aa1-216">If you save your report with the filter, report readers can interact with the filter in Reading view, selecting or clearing values.</span></span>

1. <span data-ttu-id="90aa1-217">เลือกลูกศรย้อนกลับเพื่อย้อนกลับไปยังเพจก่อนหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="90aa1-217">Select the back arrow to return to the previous report page.</span></span>

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="90aa1-218">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="90aa1-218">Considerations and troubleshooting</span></span>

- <span data-ttu-id="90aa1-219">ถ้าคุณไม่เห็นบานหน้าต่างเขตข้อมูล ตรวจสอบให้แน่ใจว่า คุณอยู่ในรายงาน[มุมมองการแก้ไข](service-interact-with-a-report-in-editing-view.md)</span><span class="sxs-lookup"><span data-stu-id="90aa1-219">If you do not see the Fields pane, make sure you're in report [Editing view](service-interact-with-a-report-in-editing-view.md)</span></span>    
- <span data-ttu-id="90aa1-220">ถ้าคุณได้ทำการเปลี่ยนแปลงมากมายกับตัวกรอง และต้องการกลับไปยังค่าเริ่มต้นของผู้เขียนรายงาน เลือก **รีเซ็ตเป็นค่าเริ่มต้น** จากแถบเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="90aa1-220">If you've made lots of changes to the filters and want to return to the report author default settings, select **Reset to default** from the top menubar.</span></span>

## <a name="next-steps"></a><span data-ttu-id="90aa1-221">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="90aa1-221">Next steps</span></span>
[<span data-ttu-id="90aa1-222">สำรวจภาพรวมของบานหน้าต่างตัวกรองของรายงาน</span><span class="sxs-lookup"><span data-stu-id="90aa1-222">Take a tour of the report Filters pane</span></span>](../consumer/end-user-report-filter.md)

[<span data-ttu-id="90aa1-223">ตัวกรองและการทำไฮไลท์ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="90aa1-223">Filters and highlighting in reports</span></span>](power-bi-reports-filters-and-highlighting.md)

[<span data-ttu-id="90aa1-224">ตัวกรองประเภทต่างๆ ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="90aa1-224">Different kinds of filters in Power BI</span></span>](power-bi-report-filter-types.md)

<span data-ttu-id="90aa1-225">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="90aa1-225">More questions?</span></span> [<span data-ttu-id="90aa1-226">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="90aa1-226">Try the Power BI Community</span></span>](https://community.powerbi.com/)
