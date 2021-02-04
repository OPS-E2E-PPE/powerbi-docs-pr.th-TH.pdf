---
title: เพิ่มหลายเขตข้อมูลไปยังตัวแบ่งส่วนลำดับชั้น
description: เรียนรู้วิธีการสร้างตัวแบ่งส่วนลำดับชั้นที่มีหลายเขตข้อมูลในหนึ่งลำดับชั้น
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 07/06/2020
LocalizationGroup: Create reports
ms.openlocfilehash: cadb8d45af40c91e7008e771f2a52ef2ea508341
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96393473"
---
# <a name="add-multiple-fields-to-a-hierarchy-slicer"></a><span data-ttu-id="474ac-103">เพิ่มหลายเขตข้อมูลไปยังตัวแบ่งส่วนลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="474ac-103">Add multiple fields to a hierarchy slicer</span></span>

<span data-ttu-id="474ac-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-desktop](../includes/yes-desktop.md)] [!INCLUDE [yes-service](../includes/yes-service.md)]</span><span class="sxs-lookup"><span data-stu-id="474ac-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-desktop](../includes/yes-desktop.md)] [!INCLUDE [yes-service](../includes/yes-service.md)]</span></span>

<span data-ttu-id="474ac-105">หากคุณต้องการกรองหลายเขตข้อมูลที่เกี่ยวข้องกันภายในหนึ่งตัวแบ่งส่วน คุณสามารถทำได้โดยการสร้างสิ่งที่เรียกว่า ตัวแบ่งส่วน *ลำดับชั้น*</span><span class="sxs-lookup"><span data-stu-id="474ac-105">If you want to filter multiple related fields in a single slicer, you do so by building what's called a *hierarchy* slicer.</span></span> <span data-ttu-id="474ac-106">คุณสามารถสร้างตัวแบ่งส่วนข้อมูลเหล่านี้ได้ทั้งใน Power BI Desktop หรือในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="474ac-106">You can create these slicers in either Power BI Desktop or in the Power BI service.</span></span>

:::image type="content" source="media/power-bi-slicer-hierarchy-multiple-fields/power-bi-slicer-hierarchy.png" alt-text="สกรีนช็อตของตัวแบ่งส่วนลำดับชั้นใน Power B I":::

<span data-ttu-id="474ac-108">เมื่อคุณเพิ่มหลายเขตข้อมูลไปที่ตัวแบ่งส่วนข้อมูล โดยค่าเริ่มต้นแล้ว ระบบจะแสดงลูกศร หรือ *เครื่องหมายบั้ง* ถัดจากรายการที่สามารถขยายเพื่อแสดงรายการในระดับถัดไป</span><span class="sxs-lookup"><span data-stu-id="474ac-108">When you add multiple fields to the slicer, by default it displays an arrow, or *chevron* next to the items that can be expanded to show the items in the next level.</span></span>

:::image type="content" source="media/power-bi-slicer-hierarchy-multiple-fields/power-bi-slicer-hierarchy-arrow.png" alt-text="สกรีนช็อตรายการดรอปดาวน์ของตัวแบ่งส่วนลำดับชั้นใน Power B I":::
 
 
<span data-ttu-id="474ac-110">เมื่อคุณเลือกรายการอย่างน้อยหนึ่งรายการ คุณจะเห็นวงกลมแบบกึ่งเลือกสำหรับรายการระดับสูงสุด</span><span class="sxs-lookup"><span data-stu-id="474ac-110">When you select one or more children for an item, you see a semi-selected circle for the top-level item.</span></span>
 
:::image type="content" source="media/power-bi-slicer-hierarchy-multiple-fields/power-bi-slicer-hierarchy-semi-selected.png" alt-text="สกรีนช็อตของตัวแบ่งส่วนลำดับชั้นการเลือกครั้งเดียวใน Power B I":::

## <a name="format-the-slicer"></a><span data-ttu-id="474ac-112">จัดรูปแบบตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="474ac-112">Format the slicer</span></span>

<span data-ttu-id="474ac-113">ลักษณะการทำงานของตัวแบ่งส่วนไม่มีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="474ac-113">The behavior of the slicer hasn't changed.</span></span> <span data-ttu-id="474ac-114">คุณยังสามารถจัดรูปแบบตัวแบ่งส่วนข้อมูลของคุณได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="474ac-114">You can also style your slicer how you want.</span></span> <span data-ttu-id="474ac-115">ตัวอย่างเช่น คุณสามารถตั้งค่าเป็นโหมดเลือกครั้งเดียวได้</span><span class="sxs-lookup"><span data-stu-id="474ac-115">For example, you can set it to single-select mode.</span></span> <span data-ttu-id="474ac-116">หรือคุณสามารถสลับระหว่างรายการและดรอปดาวน์ได้</span><span class="sxs-lookup"><span data-stu-id="474ac-116">Or you can swap between a list and dropdown.</span></span> 

:::image type="content" source="media/power-bi-slicer-hierarchy-multiple-fields/power-bi-slicer-hierarchy-dropdown.png" alt-text="สกรีนช็อตของตัวแบ่งส่วนลำดับชั้นที่จัดรูปแบบเป็นตัวแบ่งส่วนข้อมูลดรอปดาวน์":::

<span data-ttu-id="474ac-118">คุณยังสามารถทำการเปลี่ยนแปลงรูปแบบต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="474ac-118">You can also make the following formatting changes.</span></span>

### <a name="change-the-title"></a><span data-ttu-id="474ac-119">เปลี่ยนชื่อเรื่อง</span><span class="sxs-lookup"><span data-stu-id="474ac-119">Change the title</span></span>

<span data-ttu-id="474ac-120">คุณสามารถแก้ไขชื่อสำหรับตัวแบ่งส่วนข้อมูลได้ แต่ใช้ได้เฉพาะกับตัวแบ่งส่วนลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="474ac-120">You can edit the title for any slicer, but it's especially useful for hierarchy slicers.</span></span> <span data-ttu-id="474ac-121">ตามค่าเริ่มต้น ชื่อของตัวแบ่งส่วนลำดับชั้นคือรายการของชื่อเขตข้อมูลในลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="474ac-121">By default, the name of a hierarchy slicer is a list of the field names in the hierarchy.</span></span>

<span data-ttu-id="474ac-122">ในตัวอย่างนี้ ชื่อของตัวแบ่งส่วนข้อมูลจะแสดงรายการสามเขตข้อมูลในลำดับชั้น: ประเภท แพลตฟอร์ม และชื่อ</span><span class="sxs-lookup"><span data-stu-id="474ac-122">In this example, the title of the slicer lists the three fields in the hierarchy: Type, Platform, and Name.</span></span>

:::image type="content" source="media/power-bi-slicer-hierarchy-multiple-fields/power-bi-slicer-title.png" alt-text="สกรีนช็อตของตัวแบ่งส่วนลำดับชั้นด้วยประเภท แพลตฟอร์ม และชื่อ":::

<span data-ttu-id="474ac-124">ถ้าต้องการเปลี่ยนชื่อ ให้เลือกตัวแบ่งส่วนข้อมูล จากนั้นเลือกบานหน้าต่าง **รูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="474ac-124">To change the name, select the slicer, then select the **Format** pane.</span></span> <span data-ttu-id="474ac-125">ใน **ส่วนหัวของตัวแบ่งส่วนข้อมูล** คุณจะเห็นชื่อปัจจุบันของตัวแบ่งส่วนข้อมูลในกล่อง **ข้อความชื่อ**</span><span class="sxs-lookup"><span data-stu-id="474ac-125">Under **Slicer header**, you see the current name of the slicer in the **Title text** box.</span></span>

:::image type="content" source="media/power-bi-slicer-hierarchy-multiple-fields/power-bi-slicer-edit-title.png" alt-text="สกรีนช็อตของบานหน้าต่างรูปแบบที่มีชื่อปัจจุบัน":::

<span data-ttu-id="474ac-127">เลือกข้อความและเพิ่มชื่อใหม่</span><span class="sxs-lookup"><span data-stu-id="474ac-127">Select the text and add a new name.</span></span>

:::image type="content" source="media/power-bi-slicer-hierarchy-multiple-fields/power-bi-slicer-new-title.png" alt-text="สกรีนช็อตของชื่อใหม่สำหรับตัวแบ่งส่วนลำดับชั้น":::


### <a name="change-the-expandcollapse-icon"></a><span data-ttu-id="474ac-129">เปลี่ยนไอคอนขยาย/ยุบ</span><span class="sxs-lookup"><span data-stu-id="474ac-129">Change the expand/collapse icon</span></span>

<span data-ttu-id="474ac-130">ตัวแบ่งส่วนลำดับชั้นมีตัวเลือกการจัดรูปแบบอื่น</span><span class="sxs-lookup"><span data-stu-id="474ac-130">Hierarchy slicers have some other formatting options.</span></span> <span data-ttu-id="474ac-131">คุณสามารถเปลี่ยนไอคอนขยาย/ยุบจากลูกศรตามค่าเริ่มต้นเป็นเครื่องหมายบวก/ลบหรืออักขระ ^ ได้</span><span class="sxs-lookup"><span data-stu-id="474ac-131">You can change the expand/collapse icon from the default arrow to a plus/minus signs, or a caret.</span></span>

1. <span data-ttu-id="474ac-132">เลือกตัวแบ่งส่วนข้อมูล จากนั้นเลือก **รูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="474ac-132">Select the slicer, then select **Format**.</span></span>
1. <span data-ttu-id="474ac-133">ขยาย **รายการ** และเลือก **ไอคอนขยาย/ยุบ**</span><span class="sxs-lookup"><span data-stu-id="474ac-133">Expand **Items** and select **Expand/collapse icon**.</span></span>
1. <span data-ttu-id="474ac-134">เลือกจาก **เครื่องหมายบั้ง** **บวก/ลบ** หรือ **อักขระ ^**</span><span class="sxs-lookup"><span data-stu-id="474ac-134">Choose from **Chevron**, **Plus/minus**, or **Caret**.</span></span>
 
    :::image type="content" source="media/power-bi-slicer-hierarchy-multiple-fields/power-bi-slicer-hierarchy-caret.png" alt-text="สกรีนช็อตของการเลือกไอคอนขยาย/ยุบสำหรับตัวแบ่งส่วนลำดับชั้นของคุณ":::
 
### <a name="change-the-indentation"></a><span data-ttu-id="474ac-136">เปลี่ยนการเยื้อง</span><span class="sxs-lookup"><span data-stu-id="474ac-136">Change the indentation</span></span>

<span data-ttu-id="474ac-137">หากเนื้อที่ในรายงานของคุณอัดแน่น คุณอาจต้องการลดจำนวนการเยื้องรายการย่อย</span><span class="sxs-lookup"><span data-stu-id="474ac-137">If space is tight on your report, you may want to reduce the amount you indent the child items.</span></span> <span data-ttu-id="474ac-138">ตามค่าเริ่มต้น การเยื้องตั้งไว้ที่ 15 พิกเซล แต่คุณสามารถเพิ่มหรือลดค่านั้นได้</span><span class="sxs-lookup"><span data-stu-id="474ac-138">By default, the indentation is 15 pixels, but you can increase or lower that.</span></span> 

1. <span data-ttu-id="474ac-139">เลือกตัวแบ่งส่วนข้อมูล จากนั้นเลือก **รูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="474ac-139">Select the slicer, then select **Format**.</span></span>
1. <span data-ttu-id="474ac-140">ขยาย **รายการ** จากนั้นลาก **การเยื้องรูปแบบขั้น** ให้มีขนาดเล็กลงหรือใหญ่ขึ้น</span><span class="sxs-lookup"><span data-stu-id="474ac-140">Expand **Items**, then drag **Stepped layout indentation** smaller or larger.</span></span> <span data-ttu-id="474ac-141">คุณยังสามารถพิมพ์ตัวเลขลงในกล่องได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="474ac-141">You can also just type a number in the box.</span></span>

    :::image type="content" source="media/power-bi-slicer-hierarchy-multiple-fields/power-bi-slicer-indentation.png" alt-text="สกรีนช็อตของการตั้งค่าตัวแบ่งส่วนลำดับชั้น":::

## <a name="next-steps"></a><span data-ttu-id="474ac-143">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="474ac-143">Next steps</span></span>

- [<span data-ttu-id="474ac-144">ตัวแบ่งส่วนข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="474ac-144">Slicers in Power BI</span></span>](../visuals/power-bi-visualization-slicers.md)
- <span data-ttu-id="474ac-145">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="474ac-145">More questions?</span></span> [<span data-ttu-id="474ac-146">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="474ac-146">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)