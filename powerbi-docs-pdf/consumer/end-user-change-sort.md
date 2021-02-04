---
title: เปลี่ยนวิธีการเรียงลำดับแผนภูมิในรายงาน
description: เปลี่ยนวิธีการเรียงลำดับแผนภูมิในรายงาน Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-explore
ms.topic: how-to
ms.date: 12/03/2020
LocalizationGroup: Reports
ms.openlocfilehash: e211aded069675c02e59004631ea2264be1e0dcc
ms.sourcegitcommit: cb6e0202de27f29dd622e47b305c15f952c5769b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/03/2020
ms.locfileid: "96578300"
---
# <a name="change-how-a-chart-is-sorted-in-a-power-bi-report"></a><span data-ttu-id="de63b-103">เปลี่ยนวิธีการเรียงลำดับแผนภูมิในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="de63b-103">Change how a chart is sorted in a Power BI report</span></span>

[!INCLUDE[consumer-appliesto-ynnn](../includes/consumer-appliesto-ynnn.md)]


> [!IMPORTANT]
> <span data-ttu-id="de63b-104">**บทความนี้มีไว้สำหรับผู้ใช้ Power BI ที่ไม่มีสิทธิ์ในการแก้ไขรายงานหรือชุดข้อมูล และผู้ที่ทำงานในเวอร์ชันออนไลน์ของ Power BI (บริการของ Power BI) เท่านั้น ถ้าคุณเป็น *ผู้ออกแบบ* รายงาน หรือ *ผู้ดูแลระบบ* หรือ *เจ้าของข้อมูล* บทความนี้อาจไม่มีรายละเอียดทั้งหมดที่คุณต้องการ แต่โปรดอ่าน [เรียงลำดับตามคอลัมน์ใน Power BI Desktop](../create-reports/desktop-sort-by-column.md)**</span><span class="sxs-lookup"><span data-stu-id="de63b-104">**This article is intended for Power BI users who do not have edit permissions to the report or dataset and who only work in the online version of Power BI (the Power BI service). If you are a report *designer* or *administrator* or *owner*, this article may not have all the information you need. Instead, please read [Sort by column in Power BI Desktop](../create-reports/desktop-sort-by-column.md)**.</span></span>

<span data-ttu-id="de63b-105">ในบริการของ Power BI คุณสามารถเปลี่ยนลักษณะของวิชวล โดยเรียงลำดับตามเขตข้อมูลที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="de63b-105">In the Power BI service, you can change how a visual looks by sorting it by different data fields.</span></span> <span data-ttu-id="de63b-106">โดยการเปลี่ยนวิธีการเรียงลำดับวิชวล คุณสามารถไฮไลท์ข้อมูลที่คุณต้องการถ่ายทอดไป</span><span class="sxs-lookup"><span data-stu-id="de63b-106">By changing how you sort a visual, you can highlight the information you want to convey.</span></span> <span data-ttu-id="de63b-107">ไม่ว่าคุณจะใช้ข้อมูลเชิงตัวเลข (เช่น ตัวเลขยอดขาย) หรือข้อมูลแบบข้อความ (เช่น ชื่อรัฐ) คุณสามารถเรียงลำดับการแสดงผลข้อมูลด้วยภาพตามที่คุณต้องการได้</span><span class="sxs-lookup"><span data-stu-id="de63b-107">Whether you're using numeric data (such as sales figures) or text data (such as state names), you can sort your visuals as desired.</span></span> <span data-ttu-id="de63b-108">Power BI มีความยืดหยุ่นมากมายสำหรับการรียงลำดับ และเมนูด่วนให้คุณใช้</span><span class="sxs-lookup"><span data-stu-id="de63b-108">Power BI provides lots of flexibility for sorting, and quick menus for you to use.</span></span> 

<span data-ttu-id="de63b-109">ไม่สามารถเรียงลำดับการแสดงผลด้วยภาพบนแดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="de63b-109">Visuals on a dashboard cannot be sorted.</span></span> <span data-ttu-id="de63b-110">แต่ในรายงาน Power BI คุณสามารถเรียงลำดับการแสดงภาพส่วนใหญ่ได้หนึ่งและบางครั้งสองเขตข้อมูลในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="de63b-110">But in a Power BI report, you can sort most visuals by one, and sometimes two, fields at a time.</span></span> <span data-ttu-id="de63b-111">สำหรับการแสดงผลด้วยภาพบางชนิดการเรียงลำดับไม่สามารถใช้งานได้เลย: แผนผังต้นไม้, เกจ, แผนที่ ฯลฯ</span><span class="sxs-lookup"><span data-stu-id="de63b-111">For certain types of visuals, sorting is not available at all: tree maps, gauges, maps, etc.</span></span> 

## <a name="get-started"></a><span data-ttu-id="de63b-112">เริ่มใช้งาน</span><span class="sxs-lookup"><span data-stu-id="de63b-112">Get started</span></span>

<span data-ttu-id="de63b-113">เมื่อต้องการเริ่มต้นใช้งาน ให้เปิดรายงานใดก็ตามที่คุณสร้างขึ้นหรือได้แชร์กับคุณ</span><span class="sxs-lookup"><span data-stu-id="de63b-113">To get started, open any report that you have created or that has been shared with you.</span></span> <span data-ttu-id="de63b-114">เลือกวิชวล (ที่สามารถเรียงลำดับได้) และเลือก **การดำเนินการเพิ่มเติม** (...)  มีตัวเลือกสำหรับการเรียงลำดับสามตัวเลือก: **เรียงลำดับจากมากไปหาน้อย** **เรียงลำดับจากน้อยไปหามาก** และ **เรียงลำดับตาม**</span><span class="sxs-lookup"><span data-stu-id="de63b-114">Select a visual (that can be sorted) and choose **More actions** (...).  There are three options for sorting: **Sort descending**, **Sort ascending**, and **Sort by**.</span></span> 
    

![แผนภูมิแท่ง alpha ที่เรียงลำดับตามแกน Y](media/end-user-change-sort/power-bi-actions.png)

### <a name="sort-alphabetically-or-numerically"></a><span data-ttu-id="de63b-116">เรียงลำดับตามตัวอักษรหรือตามตัวเลข</span><span class="sxs-lookup"><span data-stu-id="de63b-116">Sort alphabetically or numerically</span></span>

<span data-ttu-id="de63b-117">คุณสามารถเรียงลำดับวิชวลตามตัวอักษรโดยชื่อของหมวดหมู่ในวิชวล หรือโดยค่าตัวเลขของแต่ละหมวดหมู่ได้</span><span class="sxs-lookup"><span data-stu-id="de63b-117">Visuals can be sorted alphabetically by the names of the categories in the visual, or by the numeric values of each category.</span></span> <span data-ttu-id="de63b-118">ตัวอย่างเช่น แผนภูมินี้จะเรียงตาม **ชื่อ** ร้านค้าของหมวดหมู่บนแกน x โดยเรียงลำดับตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="de63b-118">For example, this chart is sorted alphabetically by the X-axis category store **Name**.</span></span>

![แผนภูมิแท่ง alpha ที่เรียงลำดับตามแกน X](media/end-user-change-sort/powerbi-sort-category.png)

<span data-ttu-id="de63b-120">เมื่อต้องการเปลี่ยนการเรียงลำดับจากประเภท (ชื่อร้านค้า) เป็นค่า (ยอดขายต่อตารางฟุต) เลือก **การดำเนินการเพิ่มเติม** (...) และเลือก **เรียงลำดับตาม**</span><span class="sxs-lookup"><span data-stu-id="de63b-120">To change the sort from a category (store name) to a value (sales per square feet), select **More actions** (...) and choose **Sort by**.</span></span> <span data-ttu-id="de63b-121">เลือกค่าเชิงตัวเลขที่ใช้ในวิชวล</span><span class="sxs-lookup"><span data-stu-id="de63b-121">Select a numeric value used in the visual.</span></span>  <span data-ttu-id="de63b-122">ในตัวอย่างนี้ เราได้เลือก **ยอดขายต่อตารางฟุต (Sales Per Sq Ft)**</span><span class="sxs-lookup"><span data-stu-id="de63b-122">In this example, we've selected **Sales Per Sq Ft**.</span></span>

![ภาพหน้าจอที่แสดงการเลือกเรียงลำดับตาม แล้วแสดงค่า](media/end-user-change-sort/power-bi-sort-value.png)

<span data-ttu-id="de63b-124">ถ้าจำเป็น ให้เปลี่ยนลำดับการจัดเรียงระหว่างจากน้อยไปหามากและจากมากไปหาน้อย</span><span class="sxs-lookup"><span data-stu-id="de63b-124">If necessary, change the sort order between ascending and descending.</span></span>  <span data-ttu-id="de63b-125">เลือก **การดำเนินการเพิ่มเติม** (...) อีกครั้ง และเลือก **เรียงลำดับจากมากไปน้อย** หรือ **เรียงลำดับจากน้อยไปมาก**</span><span class="sxs-lookup"><span data-stu-id="de63b-125">Select **More actions** (...) again and choose **Sort descending** or **Sort ascending**.</span></span> <span data-ttu-id="de63b-126">เขตข้อมูลที่ใช้ในการเรียงลำดับจะเป็นตัวหนาและมีแถบสีเหลือง</span><span class="sxs-lookup"><span data-stu-id="de63b-126">The field that is being used to sort is in bold and has a yellow bar.</span></span>

   ![วิดีโอแสดงการเลือกเรียงลำดับตามและจากน้อยไปหามาก มากไปหาน้อย](media/end-user-change-sort/sort.gif)

> [!NOTE]
> <span data-ttu-id="de63b-128">ภาพไม่สามารถเรียงลำดับได้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="de63b-128">Not all visuals can be sorted.</span></span> <span data-ttu-id="de63b-129">ตัวอย่างเช่น ไม่สามารถจัดเรียงวิชวลต่อไปนี้ แผนภาพต้นไม้ แผนที่ แผนที่กรอกข้อมูล แผนภูมิกระจาย หน้าปัด บัตร น้ำตก</span><span class="sxs-lookup"><span data-stu-id="de63b-129">For example, the following visuals cannot be sorted: treemap, map, filled map, scatter, gauge, card, waterfall.</span></span>

## <a name="sorting-by-multiple-columns"></a><span data-ttu-id="de63b-130">การเรียงลำดับตามหลายคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="de63b-130">Sorting by multiple columns</span></span>
<span data-ttu-id="de63b-131">ข้อมูลในตารางนี้จะเรียงลำดับตาม **จำนวนลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="de63b-131">The data in this table is sorted by **Number of customers**.</span></span>  <span data-ttu-id="de63b-132">เรารู้สิ่งนี้เพราะลูกศรเล็กๆ ใต้คำว่า *หมายเลข*</span><span class="sxs-lookup"><span data-stu-id="de63b-132">We know this because of the small arrow beneath the word *Number*.</span></span> <span data-ttu-id="de63b-133">ลูกศรชี้ลงซึ่งหมายความว่าคอลัมน์จะถูกเรียงลำดับ *จากมากไปหาน้อย*</span><span class="sxs-lookup"><span data-stu-id="de63b-133">The arrow is pointing down which means the column is being sorted in *descending* order.</span></span>

![สกรีนช็อตแสดงคอลัมน์แรกที่ใช้สำหรับการเรียงลำดับ](media/end-user-change-sort/power-bi-sort-column.png)


<span data-ttu-id="de63b-135">หากต้องการเพิ่มคอลัมน์เพิ่มเติมลงในลำดับการจัดเรียงให้ Shift + คลิกส่วนหัวของคอลัมน์ที่คุณต้องการเพิ่มถัดจากลำดับการจัดเรียง</span><span class="sxs-lookup"><span data-stu-id="de63b-135">To add more columns to the sort order, Shift + click the column header you would like to add next in the sort order.</span></span> <span data-ttu-id="de63b-136">ตัวอย่างเช่นถ้าคุณคลิก **จำนวนลูกค้า** จากนั้น Shift + คลิก **รายได้รวม** ตารางจะถูกเรียงลำดับจากลูกค้าก่อนแล้วตามด้วยรายได้</span><span class="sxs-lookup"><span data-stu-id="de63b-136">For example, if you click **Number of customers** and then Shift + click **Total revenue**, then the table is sorted first by customers, then by revenue.</span></span> <span data-ttu-id="de63b-137">เส้นขอบสีแดงแสดงพื้นที่ที่เปลี่ยนลำดับการจัดเรียง</span><span class="sxs-lookup"><span data-stu-id="de63b-137">The red outline show areas where sort order changed.</span></span>

![สกรีนช็อตแสดงคอลัมน์ที่สองที่ใช้สำหรับการเรียงลำดับ](media/end-user-change-sort/power-bi-sort-second.png)

<span data-ttu-id="de63b-139">ถ้าคุณ Shift + คลิกที่ครั้งที่สองในคอลัมน์เดียวกัน การดำเนินการนี้จะเป็นการเปลี่ยนทิศทางการเรียงลำดับ (จากน้อยไปหามาก) สำหรับคอลัมน์นั้น</span><span class="sxs-lookup"><span data-stu-id="de63b-139">If you Shift + click a second time on the same column, this will change the sort direction (ascending, descending) for that column.</span></span> <span data-ttu-id="de63b-140">นอกจากนี้ ถ้าคุณกด Shift + คลิกที่คอลัมน์ที่คุณได้เพิ่มไปยังลำดับการจัดเรียงก่อนหน้านี้ จะย้ายคอลัมน์นั้นไปยังด้านหลังของลำดับการจัดเรียง</span><span class="sxs-lookup"><span data-stu-id="de63b-140">Furthermore, if you Shift + click a column you have previously added to the sort order, this will move that column to the back of the sort order.</span></span>


## <a name="saving-changes-you-make-to-sort-order"></a><span data-ttu-id="de63b-141">บันทึกการเปลี่ยนแปลงที่คุณทำกับการเรียงลำดับ</span><span class="sxs-lookup"><span data-stu-id="de63b-141">Saving changes you make to sort order</span></span>
<span data-ttu-id="de63b-142">รายงาน Power BI จะคงตัวกรอง ตัวแบ่งส่วนข้อมูล การเรียงลำดับ และการเปลี่ยนแปลงอื่น ๆ ในมุมมองที่คุณทำไว้ -- แม้คุณจะทำงานอยู่ใน [มุมมองการอ่าน](end-user-reading-view.md)</span><span class="sxs-lookup"><span data-stu-id="de63b-142">Power BI reports retain the filters, slicers, sorting, and other data view changes that you make -- even if you're working in [Reading view](end-user-reading-view.md).</span></span> <span data-ttu-id="de63b-143">ดังนั้นถ้าคุณออกจากรายงาน และกลับมาในภายหลัง การเปลี่ยนแปลงการเรียงลำดับของคุณก็ยังถูกบันทึกไว้</span><span class="sxs-lookup"><span data-stu-id="de63b-143">So, if you navigate away from a report, and return later, your sorting changes are saved.</span></span>  <span data-ttu-id="de63b-144">ถ้าคุณต้องการย้อนกลับการเปลี่ยนแปลงของคุณ ให้กลับไปยังการตั้งค่าของ *ผู้ออกแบบ* รายงาน และเลือก **รีเซ็ตเป็นค่าเริ่มต้น** จากแถบเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="de63b-144">If you want to revert your changes back to the report *designer's* settings, select **Reset to default** from the upper menu bar.</span></span> 

![เรียงลำดับแบบคงอยู่](media/end-user-change-sort/power-bi-reset.png)

<span data-ttu-id="de63b-146">อย่างไรก็ตาม ถ้าปุ่ม **รีเซ็ตเป็นค่าเริ่มต้น** เป็นสีเทา แสดงว่า *ผู้ออกแบบ* รายงานได้ปิดใช้งานความสามารถในการบันทึก (คงอยู่) การเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="de63b-146">If however, the **Reset to default** button is greyed out, that means the report *designer* has disabled the ability to save (persist) your changes.</span></span>

<a name="other"></a>
## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="de63b-147">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="de63b-147">Considerations and troubleshooting</span></span>

### <a name="sorting-using-other-criteria"></a><span data-ttu-id="de63b-148">เรียงลำดับโดยใช้เกณฑ์อื่น</span><span class="sxs-lookup"><span data-stu-id="de63b-148">Sorting using other criteria</span></span>
<span data-ttu-id="de63b-149">บางครั้ง คุณต้องการเรียงลำดับวิชวลของคุณโดยใช้เขตข้อมูลที่แตกต่างกัน (ที่ไม่รวมอยู่ในวิชวล) หรือเกณฑ์อื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="de63b-149">Sometimes, you want to sort your visual using a different field (that isn't included in the visual) or other criteria.</span></span>  <span data-ttu-id="de63b-150">ตัวอย่างเช่น คุณอาจต้องการเรียงลำดับตามเดือนตามลำดับต่อเนื่องกัน
 (และไม่ได้อยู่ในลำดับตัวอักษร) หรือคุณอาจต้องการเรียงลำดับตามตัวเลขทั้งหมด แทนที่เรียงด้วยตัวเลข (ตัวอย่าง 0, 1, 9, 20 และไม่ 0, 1, 20, 9)</span><span class="sxs-lookup"><span data-stu-id="de63b-150">For example, you might want to sort by month in sequential order (and not in alphabetical order) or you might want to sort by entire numbers instead of by digit (example, 0, 1, 9, 20 and not 0, 1, 20, 9).</span></span>  

<span data-ttu-id="de63b-151">เฉพาะผู้ที่ออกแบบรายงานเท่านั้นที่สามารถทำการเปลี่ยนแปลงเหล่านี้ให้คุณได้</span><span class="sxs-lookup"><span data-stu-id="de63b-151">Only the person who designed the report can make these changes for you.</span></span> <span data-ttu-id="de63b-152">คุณสามารถค้นหาข้อมูลการติดต่อสำหรับ *ผู้ออกแบบ* ได้โดยการเลือกชื่อรายงานจากแถบส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="de63b-152">Contact information for the *designer* can be found by selecting the report name from the header bar.</span></span>

![เมนูดรอปดาวน์ที่แสดงข้อมูลการติดต่อ](media/end-user-change-sort/power-bi-heading.png)

<span data-ttu-id="de63b-154">ถ้าคุณเป็น *ผู้ออกแบบ* และมีสิทธิ์ในการแก้ไขเนื้อหา ให้อ่าน [เรียงลำดับตามคอลัมน์ใน Power BI Desktop](../create-reports/desktop-sort-by-column.md) เพื่อเรียนรู้วิธีการอัปเดตชุดข้อมูลและเปิดใช้งานการเรียงลำดับชนิดนี้</span><span class="sxs-lookup"><span data-stu-id="de63b-154">If you are a *designer* and have edit permissions to the content, read [Sort by column in Power BI Desktop](../create-reports/desktop-sort-by-column.md) to learn how to update the dataset and enable this type of sorting.</span></span>

## <a name="next-steps"></a><span data-ttu-id="de63b-155">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="de63b-155">Next steps</span></span>
<span data-ttu-id="de63b-156">อ่านเพิ่มเติมเกี่ยวกับ[การแสดงภาพในรายงาน Power BI](end-user-visualizations.md)</span><span class="sxs-lookup"><span data-stu-id="de63b-156">More about [Visualizations in Power BI reports](end-user-visualizations.md).</span></span>

[<span data-ttu-id="de63b-157">Power BI แนวคิดพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="de63b-157">Power BI - Basic Concepts</span></span>](end-user-basic-concepts.md)
