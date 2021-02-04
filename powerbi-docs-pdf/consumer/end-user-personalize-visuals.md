---
title: ตั้งค่าวิชวลส่วนบุคคลในรายงาน
description: สร้างมุมมองรายงานของคุณเอง โดยไม่ต้องแก้ไข
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-explore
ms.topic: how-to
ms.date: 10/13/2020
LocalizationGroup: Reports
ms.openlocfilehash: aa94908c8601052c9cb8ac7cd4a6c0e895afeff6
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96390161"
---
# <a name="personalize-visuals-in-a-report"></a><span data-ttu-id="62705-103">ตั้งค่าวิชวลส่วนบุคคลในรายงาน</span><span class="sxs-lookup"><span data-stu-id="62705-103">Personalize visuals in a report</span></span>

[!INCLUDE[consumer-appliesto-ynny](../includes/consumer-appliesto-ynny.md)]

<span data-ttu-id="62705-104">เป็นเรื่องยากที่จะสร้างวิชวลซึ่งสามารถตอบสนองความต้องการของทุกคนได้</span><span class="sxs-lookup"><span data-stu-id="62705-104">It's hard to make one visual that satisfies everyone's requirements.</span></span> <span data-ttu-id="62705-105">แต่เมื่อเพื่อนร่วมงานแชร์รายงานกับคุณคุณอาจต้องการทำการเปลี่ยนแปลงกับวิชวล -- โดยไม่ต้องขอให้เพื่อนร่วมงานของคุณทำการเปลี่ยนแปลงให้คุณ</span><span class="sxs-lookup"><span data-stu-id="62705-105">But, when a colleague shares a report with you, you may want to make changes to the visuals -- without having to ask your colleague to make the changes for you.</span></span> 

<span data-ttu-id="62705-106">บางทีคุณอาจต้องการสลับสิ่งที่อยู่บนแกน เปลี่ยนประเภทวิชวลหรือเพิ่มบางอย่างไปยังคำแนะนำเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="62705-106">Maybe you'd like to swap what's on the axis, change the visual type, or add something to the tooltip.</span></span> <span data-ttu-id="62705-107">ด้วยคุณสมบัติ **ปรับแต่งวิชวลนี้** คุณสามารถทำการเปลี่ยนแปลงด้วยตัวคุณเอง และเมื่อคุณได้วิชวลตามที่คุณต้องการ สามารถบันทึกเป็น [บุ๊กมาร์ก](end-user-bookmarks.md) เพื่อกลับมาดูอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="62705-107">With the **Personalize this visual** feature, make the changes yourself and when you have the visual the way you want it, save it as a [bookmark](end-user-bookmarks.md) to come back to.</span></span> <span data-ttu-id="62705-108">คุณไม่จำเป็นต้องมีสิทธิ์ในการแก้ไขสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="62705-108">You don't even need edit permission for the report.</span></span>

:::image type="content" source="media/end-user-personalize-visuals/power-bi-personalize.png" alt-text="ตั้งค่าวิชวลส่วนบุคคล":::
 
## <a name="what-you-can-change"></a><span data-ttu-id="62705-110">สิ่งที่คุณสามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="62705-110">What you can change</span></span>

<span data-ttu-id="62705-111">คุณลักษณะนี้ช่วยให้คุณสามารถรับข้อมูลเชิงลึกเพิ่มเติมผ่านการสำรวจวิชวลแบบเฉพาะกิจบนรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="62705-111">This feature helps you gain further insights through ad-hoc exploration of visuals on a Power BI report.</span></span> <span data-ttu-id="62705-112">ต่อไปนี้คือการปรับเปลี่ยนบางอย่างที่คุณสามารถทำได้</span><span class="sxs-lookup"><span data-stu-id="62705-112">Here are some of the modifications that you can make.</span></span> <span data-ttu-id="62705-113">ตัวเลือกที่พร้อมใช้งานจะแตกต่างกันไปตามชนิดวิชวล</span><span class="sxs-lookup"><span data-stu-id="62705-113">The available options vary by visual type.</span></span> 

- <span data-ttu-id="62705-114">การเปลี่ยนชนิดของการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="62705-114">Change the visualization type</span></span>
- <span data-ttu-id="62705-115">สลับหน่วยวัดหรือมิติ</span><span class="sxs-lookup"><span data-stu-id="62705-115">Swap out a measure or dimension</span></span>
- <span data-ttu-id="62705-116">เพิ่มหรือลบคำอธิบายแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="62705-116">Add or remove a legend</span></span>
- <span data-ttu-id="62705-117">เปรียบเทียบหน่วยวัดสองหน่วยขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="62705-117">Compare two or more measures</span></span>
- <span data-ttu-id="62705-118">เปลี่ยนการรวมและอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="62705-118">Change aggregations, etc.</span></span>

<span data-ttu-id="62705-119">ไม่เฉพาะคุณลักษณะนี้เท่านั้นที่อนุญาตให้ใช้งานสำหรับความสามารถในการสำรวจใหม่</span><span class="sxs-lookup"><span data-stu-id="62705-119">Not only does this feature allow for new exploration capabilities.</span></span> <span data-ttu-id="62705-120">แต่ยังมีวิธีการสำหรับคุณในการบันทึกและแชร์การเปลี่ยนแปลงของคุณเอง:</span><span class="sxs-lookup"><span data-stu-id="62705-120">It also includes ways for you to capture and share your changes:</span></span>

- <span data-ttu-id="62705-121">บันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="62705-121">Capture your changes</span></span>
- <span data-ttu-id="62705-122">แชร์การเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="62705-122">Share your changes</span></span>
- <span data-ttu-id="62705-123">รีเซ็ตการเปลี่ยนแปลงทั้งหมดของคุณสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="62705-123">Reset all your changes for a report</span></span>
- <span data-ttu-id="62705-124">รีเซ็ตการเปลี่ยนแปลงทั้งหมดของคุณสำหรับวิชวล</span><span class="sxs-lookup"><span data-stu-id="62705-124">Reset all your changes for a visual</span></span>
- <span data-ttu-id="62705-125">ล้างการเปลี่ยนแปลงล่าสุดของคุณ</span><span class="sxs-lookup"><span data-stu-id="62705-125">Clear out your recent changes</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62705-126">ความสามารถในการปรับแต่งวิชวลในแบบของคุณต้องเปิดใช้งานโดย *ผู้ออกแบบ* รายงาน</span><span class="sxs-lookup"><span data-stu-id="62705-126">The ability to personalize a visual must be enabled by the report *designer*.</span></span> <span data-ttu-id="62705-127">หากคุณไม่เห็นไอคอน **ปรับแต่งวิชวลนี้** ![ปรับแต่งไอคอนวิชวลนี้](media/end-user-personalize-visuals/power-bi-personalize-visual-icon.png) แสดงว่าผู้ออกแบบรายงานไม่ได้เปิดใช้งานคุณสมบัตินี้สำหรับรายงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="62705-127">If you don't see the **Personalize this visual** ![Personalize this visual icon](media/end-user-personalize-visuals/power-bi-personalize-visual-icon.png) icon, then the report designer has not enabled this feature for the current report.</span></span> <span data-ttu-id="62705-128">ตรวจสอบกับเจ้าของรายงานหรือผู้ดูแลระบบ Power BI ของคุณเพื่อเปิดใช้งานคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="62705-128">Check with the report owner or your Power BI administrator to have the feature enabled.</span></span> <span data-ttu-id="62705-129">เมื่อต้องการแสดงข้อมูลที่ติดต่อสำหรับเจ้าของรายงาน ให้เลือกชื่อของรายงานจากแถบเมนู Power BI</span><span class="sxs-lookup"><span data-stu-id="62705-129">To display contact information for the report owner, select the name of the report from the Power BI menu bar.</span></span>

## <a name="personalize-visuals-in-the-power-bi-service"></a><span data-ttu-id="62705-130">ตั้งค่าวิชวลส่วนบุคคลในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="62705-130">Personalize visuals in the Power BI service</span></span>

<span data-ttu-id="62705-131">ด้วยการปรับแต่งวิชวล คุณสามารถสำรวจข้อมูลของคุณได้หลายวิธี โดยไม่ต้องออกจาก [มุมมองการอ่านรายงาน](end-user-reading-view.md)</span><span class="sxs-lookup"><span data-stu-id="62705-131">By personalizing a visual, you can explore your data in many ways, without leaving [report reading view](end-user-reading-view.md).</span></span> <span data-ttu-id="62705-132">ตัวอย่างต่อไปนี้แสดงวิธีการต่าง ๆ ที่คุณสามารถปรับเปลี่ยนการแสดงภาพเพื่อตอบสนองต่อความต้องการของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="62705-132">The following examples show different ways you can modify a visualization to meet your needs.</span></span> 

1. <span data-ttu-id="62705-133">เปิดรายงานในมุมมองการอ่านในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="62705-133">Open a report in reading view in the Power BI service.</span></span>

2. <span data-ttu-id="62705-134">ที่แถบเมนูสำหรับวิชวล ให้เลือกไอคอน **ตั้งค่าวิชวลนี้ส่วนบุคคล** ![ตั้งค่าไอคอนวิชวลนี้ส่วนบุคคล](media/end-user-personalize-visuals/power-bi-personalize-visual-icon.png)</span><span class="sxs-lookup"><span data-stu-id="62705-134">In the menu bar for the visual, select the **Personalize this visual** ![Personalize this visual icon](media/end-user-personalize-visuals/power-bi-personalize-visual-icon.png) icon.</span></span> 

### <a name="change-the-visualization-type"></a><span data-ttu-id="62705-135">การเปลี่ยนชนิดของการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="62705-135">Change the visualization type</span></span>

<span data-ttu-id="62705-136">คุณคิดว่าข้อมูลจะแสดงผลได้ดีกว่าถ้าเป็นแผนภูมิคอลัมน์แบบสแตกหรือไม่</span><span class="sxs-lookup"><span data-stu-id="62705-136">Do you think the data would display better as a Stacked column chart?</span></span> <span data-ttu-id="62705-137">เปลี่ยน **ประเภทการแสดงภาพ**</span><span class="sxs-lookup"><span data-stu-id="62705-137">Change the **Visualization type**.</span></span>

:::image type="content" source="media/end-user-personalize-visuals/power-bi-personalize-change-visual-type.png" alt-text="เปลี่ยนประเภทการแสดงภาพ":::
 
### <a name="swap-out-a-measure-or-dimension"></a><span data-ttu-id="62705-139">สลับหน่วยวัดหรือมิติ</span><span class="sxs-lookup"><span data-stu-id="62705-139">Swap out a measure or dimension</span></span>
<span data-ttu-id="62705-140">แทนที่เขตข้อมูลที่ใช้สำหรับแกน X โดยการเลือกเขตข้อมูลที่คุณต้องการแทนที่ จากนั้นเลือกเขตข้อมูลอื่น</span><span class="sxs-lookup"><span data-stu-id="62705-140">Replace the field being used for the X axis by selecting the field that you want to replace, then selecting a different field.</span></span>

:::image type="content" source="media/end-user-personalize-visuals/power-bi-personalize-change-axis.png" alt-text="เปลี่ยนแกน":::
 
### <a name="add-or-remove-a-legend"></a><span data-ttu-id="62705-142">เพิ่มหรือลบคำอธิบายแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="62705-142">Add or remove a legend</span></span>
<span data-ttu-id="62705-143">ด้วยการเพิ่มคำอธิบายแผนภูมิ คุณสามารถเข้ารหัสสีวิชวลตามหมวดหมู่ได้</span><span class="sxs-lookup"><span data-stu-id="62705-143">By adding a legend, you can color-code a visual based on a category.</span></span> <span data-ttu-id="62705-144">ในตัวอย่างนี้เราจะเข้ารหัสสีตามชื่อบริษัท</span><span class="sxs-lookup"><span data-stu-id="62705-144">In this example, we're color-coding based on company name.</span></span> 

:::image type="content" source="media/end-user-personalize-visuals/power-bi-personalize-change-legend.png" alt-text="เพิ่มหรือลบคำอธิบายแผนภูมิ":::

### <a name="change-the-placement-of-fields"></a><span data-ttu-id="62705-146">เปลี่ยนตำแหน่งของเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="62705-146">Change the placement of fields</span></span>

<span data-ttu-id="62705-147">การใช้การลากและวางคุณสามารถเปลี่ยนตำแหน่งของเขตข้อมูลภายในคุณสมบัติวิชวลเดียวกันหรือแม้กระทั่งในคุณสมบัติวิชวลที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="62705-147">Using drag and drop, you can change the placement of fields within the same visual property or even across different visual properties.</span></span> <span data-ttu-id="62705-148">ตัวอย่างเช่น คุณสามารถย้ายเขตข้อมูลในคำอธิบายแผนภูมิไปยังแกนของวิชวลได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="62705-148">For example, you can quickly move a field in the legend to the axis of a visual.</span></span>

:::image type="content" source="media/end-user-personalize-visuals/personalize-drag-and-drop.png" alt-text="สกรีนช็อตของการลากเขตข้อมูลในภาพ":::

<span data-ttu-id="62705-150">คุณยังสามารถจัดลำดับคอลัมน์ของตารางหรือเมทริกซ์ใหม่ได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="62705-150">You can also quickly reorder the columns of a table or matrix.</span></span>

:::image type="content" source="media/end-user-personalize-visuals/personalize-reorder-columns.png" alt-text="สกรีนช็อตของการจัดเรียงคอลัมน์ใหม่ในตาราง":::

### <a name="compare-two-or-more-different-measures"></a><span data-ttu-id="62705-152">เปรียบเทียบหน่วยวัดที่แตกต่างกันสองหน่วยขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="62705-152">Compare two or more different measures</span></span>
<span data-ttu-id="62705-153">เปรียบเทียบค่าสำหรับหน่วยวัดที่แตกต่างกันได้ โดยใช้ไอคอน + เพื่อเพิ่มหน่วยวัดหลายรายการสำหรับวิชวล</span><span class="sxs-lookup"><span data-stu-id="62705-153">Compare and contrast values for different measures by using the + icon to add multiple measures for a visual.</span></span> <span data-ttu-id="62705-154">เมื่อต้องการเอาหน่วยวัดออกให้เลือก **ตัวเลือกเพิ่มเติม (...)** และเลือก **ลบเขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="62705-154">To remove a measure, select **More options (...)** and choose **Remove field**.</span></span>

:::image type="content" source="media/end-user-personalize-visuals/power-bi-personalize-compare-measures.png" alt-text="เปรียบเทียบหน่วยวัด":::

### <a name="change-aggregations"></a><span data-ttu-id="62705-156">เปลี่ยนการรวม</span><span class="sxs-lookup"><span data-stu-id="62705-156">Change aggregations</span></span>
<span data-ttu-id="62705-157">เปลี่ยนวิธีการคำนวณหน่วยวัดได้โดยการเปลี่ยนการรวมในบานหน้าต่าง **ตั้งค่าส่วนบุคคล**</span><span class="sxs-lookup"><span data-stu-id="62705-157">Change how a measure is computed by changing the aggregation in the **Personalize** pane.</span></span> <span data-ttu-id="62705-158">เลือก **ตัวเลือกเพิ่มเติม (...)** และเลือกการรวมที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="62705-158">Select **More options (...)** and choose the aggregation to use.</span></span>

:::image type="content" source="media/end-user-personalize-visuals/power-bi-personalize-change-aggregation.png" alt-text="เปลี่ยนการรวม":::

### <a name="capture-changes"></a><span data-ttu-id="62705-160">บันทึกการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="62705-160">Capture changes</span></span> 
<span data-ttu-id="62705-161">ด้วยการใช้บุ๊กมาร์กส่วนบุคคลในการบันทึกการเปลี่ยนแปลงของคุณช่วยให้คุณสามารถกลับไปยังมุมมองส่วนบุคคลของคุณได้</span><span class="sxs-lookup"><span data-stu-id="62705-161">Using personal bookmarks, capture your changes so you can return to your personalized view.</span></span> <span data-ttu-id="62705-162">เลือก **บุ๊กมาร์ก** > **บุ๊กมาร์กส่วนบุคคล** และให้ชื่อบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="62705-162">Select **Bookmarks** > **Personal bookmarks** and give the bookmark a name.</span></span> 

:::image type="content" source="media/end-user-personalize-visuals/power-bi-personalize-bookmark.png" alt-text="สร้างบุ๊กมาร์ก":::
 
<span data-ttu-id="62705-164">นอกจากนี้ คุณยังสามารถสร้างบุ๊กมาร์กเป็นมุมมองเริ่มต้นของคุณได้</span><span class="sxs-lookup"><span data-stu-id="62705-164">You can also make the bookmark your default view.</span></span>

### <a name="share-changes"></a><span data-ttu-id="62705-165">แชร์การเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="62705-165">Share changes</span></span> 
<span data-ttu-id="62705-166">หากคุณมีสิทธิ์ในการอ่านและแชร์ต่อ คุณสามารถเลือกเพื่อรวมการเปลี่ยนแปลงของคุณได้เมื่อคุณแชร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="62705-166">If you have read and reshare permissions, when you share the report you can choose to include your changes.</span></span>

:::image type="content" source="media/end-user-personalize-visuals/power-bi-personalize-share-changes.png" alt-text="แชร์การเปลี่ยนแปลง":::
 
### <a name="reset-all-your-changes-to-a-report"></a><span data-ttu-id="62705-168">รีเซ็ตการเปลี่ยนแปลงทั้งหมดของคุณในรายงาน</span><span class="sxs-lookup"><span data-stu-id="62705-168">Reset all your changes to a report</span></span>

<span data-ttu-id="62705-169">จากมุมบนขวาของพื้นที่รายงานของคุณให้เลือก **รีเซ็ตเป็นค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="62705-169">From the upper-right corner of your report canvas, select **Reset to default**.</span></span> <span data-ttu-id="62705-170">ซึ่งจะลบการเปลี่ยนแปลงทั้งหมดของคุณในรายงานออก และตั้งค่ากลับไปเป็นมุมมองที่บันทึกไว้ล่าสุดของผู้เขียนของรายงาน</span><span class="sxs-lookup"><span data-stu-id="62705-170">This removes all your changes in the report and sets it back to the author's last saved view of the report.</span></span>

:::image type="content" source="media/end-user-personalize-visuals/power-bi-personalize-reset-all.png" alt-text="รีเซ็ตการเปลี่ยนแปลงทั้งหมด":::
 
### <a name="reset-all-your-changes-to-a-visual"></a><span data-ttu-id="62705-172">รีเซ็ตการเปลี่ยนแปลงทั้งหมดของคุณในวิชวล</span><span class="sxs-lookup"><span data-stu-id="62705-172">Reset all your changes to a visual</span></span>

<span data-ttu-id="62705-173">จากแถบเมนูสำหรับวิชวล เลือก **รีเซ็ตวิชวลนี้** เพื่อลบการเปลี่ยนแปลงทั้งหมดของคุณในวิชวลที่เฉพาะเจาะจงออก และตั้งค่ากลับไปเป็นมุมมองวิชวลที่บันทึกไว้ล่าสุดของผู้เขียนของรายงาน</span><span class="sxs-lookup"><span data-stu-id="62705-173">From the menu bar for the visual, select **Reset this visual** to remove all your changes to a particular visual and set it back to the author's last saved view of that visual.</span></span>

:::image type="content" source="media/end-user-personalize-visuals/power-bi-personalize-reset-visual.png" alt-text="รีเซ็ตการเปลี่ยนแปลงวิชวลทั้งหมด":::
 
### <a name="clear-recent-changes"></a><span data-ttu-id="62705-175">ล้างการเปลี่ยนแปลงล่าสุด</span><span class="sxs-lookup"><span data-stu-id="62705-175">Clear recent changes</span></span>

<span data-ttu-id="62705-176">เลือกไอคอนยางลบเพื่อล้างการเปลี่ยนแปลงล่าสุดทั้งหมดที่คุณทำไว้ตั้งแต่คุณเปิดบานหน้าต่าง **ตั้งค่าส่วนบุคคล**</span><span class="sxs-lookup"><span data-stu-id="62705-176">Select the eraser icon to clear all recent changes you've made since you opened the **Personalize** pane.</span></span>  

:::image type="content" source="media/end-user-personalize-visuals/power-bi-personalize-revert-changes.png" alt-text="เปลี่ยนการเปลี่ยนแปลงล่าสุดกลับเป็นค่าเดิม":::

## <a name="limitations"></a><span data-ttu-id="62705-178">ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="62705-178">Limitations</span></span>

<span data-ttu-id="62705-179">คุณลักษณะมีข้อจำกัดบางอย่างที่ต้องระวังในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="62705-179">Currently the feature has a few limitations to be aware of.</span></span>

- <span data-ttu-id="62705-180">**ปรับแต่งวิชวลนี้** สามารถปิดใช้งานสำหรับรายงานทั้งหมดหรือสำหรับวิชวลที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="62705-180">**Personalize this visual** can be turned off for an entire report or for a particular visual.</span></span> <span data-ttu-id="62705-181">ถ้าคุณไม่มีตัวเลือกในการปรับแต่งวิชวล ให้ตรวจสอบกับผู้ดูแลระบบ Power BI ของคุณหรือเจ้าของรายงาน</span><span class="sxs-lookup"><span data-stu-id="62705-181">If you don't have an option to personalize a visual, check with your Power BI admin or the report owner.</span></span> <span data-ttu-id="62705-182">เมื่อต้องการแสดงข้อมูลที่ติดต่อสำหรับเจ้าของรายงาน ให้เลือกชื่อของรายงานจากแถบเมนู Power BI</span><span class="sxs-lookup"><span data-stu-id="62705-182">To display contact information for the report owner, select the name of the report from the Power BI menu bar.</span></span>
- <span data-ttu-id="62705-183">การสำรวจของผู้ใช้ไม่ดำเนินการต่อโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="62705-183">User explorations don't automatically persist.</span></span> <span data-ttu-id="62705-184">คุณต้องบันทึกมุมมองของคุณเป็นบุ๊กมาร์กส่วนบุคคล เพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="62705-184">You need to save your view as a personal bookmark to capture your changes.</span></span>
- <span data-ttu-id="62705-185">คุณลักษณะนี้ได้รับการรองรับในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่สำหรับแท็บเล็ต iOS และ Android และในแอป Power BI Windows แต่ไม่ได้รับการรองรับในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่สำหรับโทรศัพท์</span><span class="sxs-lookup"><span data-stu-id="62705-185">This feature is supported in the Power BI mobile apps for iOS and Android tablets and in the Power BI Windows app; it is not supported in the Power BI mobile apps for phones.</span></span> <span data-ttu-id="62705-186">อย่างไรก็ตาม การเปลี่ยนแปลงใด ๆ ที่ทำกับวิชวล ซึ่งคุณได้บันทึกในบุ๊กมาร์กส่วนบุคคลขณะที่ใช้บริการของ Power BI นั้นจะสามารถดำเนินการในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่ทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="62705-186">However, any change to a visual you save in a personal bookmark while in the Power BI service is respected in all the Power BI mobile apps.</span></span>

## <a name="next-steps"></a><span data-ttu-id="62705-187">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="62705-187">Next steps</span></span>
<span data-ttu-id="62705-188">[คัดลอกวิชวลรายงานเป็นรูปแบบคงที่](../visuals/power-bi-visualization-copy-paste.md)  </span><span class="sxs-lookup"><span data-stu-id="62705-188">[Copy a report visual as a static image](../visuals/power-bi-visualization-copy-paste.md)  </span></span>  
<span data-ttu-id="62705-189">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="62705-189">More questions?</span></span> [<span data-ttu-id="62705-190">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="62705-190">Try the Power BI Community</span></span>](https://community.powerbi.com/)
