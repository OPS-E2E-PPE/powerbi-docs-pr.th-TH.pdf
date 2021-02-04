---
title: ใช้บานหน้าต่างตัวกรองรายงาน
description: วิธีการเพิ่มตัวกรองไปยังรายงานในบริการ Power BI สำหรับผู้ใช้ทางธุรกิจ
author: mihart
ms.reviewer: mihart
ms.custom: ''
ms.service: powerbi
ms.subservice: powerbi-consumer
ms.topic: how-to
ms.date: 09/29/2020
ms.author: mihart
LocalizationGroup: Reports
ms.openlocfilehash: fb283858d9e6fe016e382f4c662de6b66bce0258
ms.sourcegitcommit: 51b965954377884bef7af16ef3031bf10323845f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/30/2020
ms.locfileid: "91600816"
---
# <a name="take-a-tour-of-the-report-filters-pane"></a><span data-ttu-id="8082c-103">สำรวจภาพรวมของบานหน้าต่างตัวกรองรายงาน</span><span class="sxs-lookup"><span data-stu-id="8082c-103">Take a tour of the report Filters pane</span></span>

[!INCLUDE[consumer-appliesto-yyny](../includes/consumer-appliesto-yyny.md)]

[!INCLUDE [power-bi-service-new-look-include](../includes/power-bi-service-new-look-include.md)]

<span data-ttu-id="8082c-104">บทความนี้จะอธิบายบานหน้าต่าง **ตัวกรอง** รายงานในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="8082c-104">This article takes a look at the report **Filters** pane in the Power BI service.</span></span> <span data-ttu-id="8082c-105">ใช้ตัวกรองเพื่อค้นหาข้อมูลเชิงลึกใหม่ในข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="8082c-105">Use the filters to discover new insights in your data.</span></span>

<span data-ttu-id="8082c-106">มีหลายวิธีในการกรองข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8082c-106">There are many different ways to filter data in Power BI.</span></span> <span data-ttu-id="8082c-107">บทความนี้อธิบายวิธีการใช้บานหน้าต่าง **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="8082c-107">This article explains how to use the **Filters** pane.</span></span>  <span data-ttu-id="8082c-108">คุณยังสามารถกรองได้โดยการเลือกจุดข้อมูลบนวิชวลรายงานเพื่อกรองวิชวลอื่น ๆ บนเพจ ซึ่งเรียกว่า**การกรองข้าม**และ**การไฮไลต์ข้าม**</span><span class="sxs-lookup"><span data-stu-id="8082c-108">You can also filter by selecting data points on a report visual to filter the other visuals on the page -- this is referred to as **cross-filtering** and **cross-highlighting**.</span></span> <span data-ttu-id="8082c-109">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการกรองข้ามและการไฮไลต์ข้าม โปรดดู [ตัวกรองและการไฮไลท์ในรายงาน Power BI](../create-reports/power-bi-reports-filters-and-highlighting.md)</span><span class="sxs-lookup"><span data-stu-id="8082c-109">For more information about cross-filtering and cross-highlighting, see [Filters and highlighting in Power BI reports](../create-reports/power-bi-reports-filters-and-highlighting.md).</span></span>

![สกรีนช็อตของรายงานในเบราว์เซอร์ที่มีลูกศรชี้ไปยังตัวเลือกตัวกรอง](media/end-user-report-filter/power-bi-reports.png)

## <a name="working-with-the-report-filters-pane"></a><span data-ttu-id="8082c-111">สำรวจภาพบานหน้าต่างตัวกรองรายงาน</span><span class="sxs-lookup"><span data-stu-id="8082c-111">Working with the report Filters pane</span></span>

<span data-ttu-id="8082c-112">เมื่อเพื่อนร่วมงานแชร์รายงานกับคุณ ให้แน่ใจว่าได้ดูบานหน้าต่าง**ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="8082c-112">When a colleague shares a report with you, be sure to look for the **Filters** pane.</span></span> <span data-ttu-id="8082c-113">ในบางครั้งจะถูกยุบตามขอบด้านขวาของรายงาน</span><span class="sxs-lookup"><span data-stu-id="8082c-113">Sometimes it's collapsed along the right edge of the report.</span></span> <span data-ttu-id="8082c-114">เลือกเพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="8082c-114">Select it to expand it.</span></span>

![สกรีนช็อตของรายงานที่มีบานหน้าต่างตัวกรองส่วนขยาย](media/end-user-report-filter/power-bi-expand-filters-pane.png)

<span data-ttu-id="8082c-116">บานหน้าต่าง **ตัวกรอง** ประกอบด้วยตัวกรองที่ *ผู้ออกแบบ* ได้เพิ่มในรายงาน</span><span class="sxs-lookup"><span data-stu-id="8082c-116">The **Filters** pane contains filters that the report *designer* added to the report.</span></span> <span data-ttu-id="8082c-117">*ผู้ใช้ทางธุรกิจ*เช่นคุณสามารถโต้ตอบกับตัวกรองที่มีอยู่ และบันทึกการเปลี่ยนแปลงได้ แต่ไม่สามารถเพิ่มตัวกรองใหม่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="8082c-117">*Business users* like you can interact with the existing filters and save your changes, but you can't add new filters to the report.</span></span> <span data-ttu-id="8082c-118">ตัวอย่างเช่น สกรีนช็อตด้านบนตัวออกแบบได้เพิ่มตัวกรองระดับหน้าสามตัวกรอง: **เซกเมนต์คือทั้งหมด**, **ปีคือ 2014** และ**ภูมิภาคเป็นภาคกลาง**</span><span class="sxs-lookup"><span data-stu-id="8082c-118">For example, in the screenshot above the designer added three page level filters: **Segment is All**, **Year is 2014**, and **Region is Central**.</span></span> <span data-ttu-id="8082c-119">คุณสามารถโต้ตอบ และเปลี่ยนตัวกรองเหล่านี้ แต่คุณไม่สามารถเพิ่มตัวกรองระดับหน้าตัวที่สี่ได้</span><span class="sxs-lookup"><span data-stu-id="8082c-119">You can interact and change these filters, but you can't add a fourth page level filter.</span></span>

<span data-ttu-id="8082c-120">มีการแรเงาตัวกรองบางรายการและไม่ได้แรเงาบางรายการ</span><span class="sxs-lookup"><span data-stu-id="8082c-120">Some of the filters are shaded, and some are not.</span></span> <span data-ttu-id="8082c-121">ถ้ามีการแรเงาตัวกรอง นั่นหมายความว่ามีการนำตัวกรองไปใช้และมีการแยกข้อมูลบางอย่างออก</span><span class="sxs-lookup"><span data-stu-id="8082c-121">If a filter is shaded, that means a filter has been applied and some data is being excluded.</span></span> <span data-ttu-id="8082c-122">ตัวอย่างเช่น มีการแรเงาการ์ดตัวกรอง **ภูมิภาค** และเมื่อคุณใช้งานการ์ดคุณเห็นว่ามีเพียง **ภาคกลาง** เท่านั้นที่ถูกเลือกจากรายการดรอปดาวน์</span><span class="sxs-lookup"><span data-stu-id="8082c-122">For example, the **Region** filter card is shaded, and when you expend the card you see that only **Central** is selected from the dropdown.</span></span> <span data-ttu-id="8082c-123">เนื่องจากภูมิภาคอยู่ภายใต้ส่วนหัว **ตัวกรองในหน้านี้** วิชวลทั้งหมดในหน้าเพจนี้จึงไม่แสดงข้อมูล (ไม่รวม) สำหรับภูมิภาค**ตะวันตก**และ**ตะวันออก**</span><span class="sxs-lookup"><span data-stu-id="8082c-123">Since Region is under the **Filters on this page** heading, all visuals on this page are not displaying (excluding) data for the **West** and **East** regions.</span></span>

![สกรีนช็อตของตัวกรองภูมิภาคที่ขยายและแสดงภาคกลางด้วยเครื่องหมายถูก](media/end-user-report-filter/power-bi-filter-region.png)

<span data-ttu-id="8082c-125">ในบริการ Power BI รายงานจะเก็บข้อมูลการเปลี่ยนแปลงที่คุณทำในบานหน้าต่าง **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="8082c-125">In the Power BI service, reports keep any changes you make in the **Filters** pane.</span></span> <span data-ttu-id="8082c-126">บริการจะขยายการเปลี่ยนแปลงเหล่านั้นผ่านไปยังอุปกรณ์เคลื่อนที่ของรายงาน</span><span class="sxs-lookup"><span data-stu-id="8082c-126">The service carries those changes through to the mobile version of the report.</span></span> 

<span data-ttu-id="8082c-127">หากต้องการรีเซ็ตบานหน้าต่าง **ตัวกรอง** เป็นค่าเริ่มต้นของตัวออกแบบ เลือก **รีเซ็ตเป็นค่าเริ่มต้น** จากแถบเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="8082c-127">To reset the **Filters** pane to the designer's defaults, select **Reset to default** from the upper menu bar.</span></span>

![สกรีนช็อตของไอคอนรีเซ็ตเป็นค่าเริ่มต้น](media/end-user-report-filter/power-bi-reset-icon.png) 

> [!NOTE]
> <span data-ttu-id="8082c-129">หากคุณไม่เห็นตัวเลือก **รีเซ็ตเป็นค่าเริ่มต้น** ตัวเลือกนี้อาจถูกปิดใช้งานโดย *ผู้ออกแบบ*รายงาน</span><span class="sxs-lookup"><span data-stu-id="8082c-129">If you don't see the **Reset to default** option, it may have been disabled by the report *designer*.</span></span> <span data-ttu-id="8082c-130">*ผู้ออกแบบ* ยังสามารถล็อกตัวกรองที่ระบุเพื่อไม่ให้คุณสามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="8082c-130">The *designer* can also lock specific filters so that you can't change them.</span></span>

## <a name="view-all-the-filters-for-a-report-page"></a><span data-ttu-id="8082c-131">ดูตัวกรองทั้งหมดสำหรับหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="8082c-131">View all the filters for a report page</span></span>

<span data-ttu-id="8082c-132">บานหน้าต่าง **ตัวกรอง** จะแสดงตัวกรองทั้งหมดที่เพิ่มโดยผู้ออกแบบในรายงาน</span><span class="sxs-lookup"><span data-stu-id="8082c-132">The **Filters** pane displays all filters added by the designer to the report.</span></span> <span data-ttu-id="8082c-133">บานหน้าต่าง **ตัวกรอง** เป็นพื้นที่ที่คุณสามารถดูข้อมูลเกี่ยวกับตัวกรอง และโต้ตอบกับตัวกรองเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="8082c-133">The **Filters** pane is also the area where you can view information about the filters and interact with them.</span></span> <span data-ttu-id="8082c-134">บันทึกการเปลี่ยนแปลงที่คุณสร้างหรือใช ้**รีเซ็ตเป็นค่าเริ่มต้น** เพื่อแปลงกลับเป็นการตั้งค่าตัวกรองต้นฉบับได้</span><span class="sxs-lookup"><span data-stu-id="8082c-134">Save changes you make or use **Reset to default** to revert to the original filter settings.</span></span>

<span data-ttu-id="8082c-135">ถ้ามีการเปลี่ยนแปลงที่คุณต้องการบันทึก คุณสามารถสร้างบุ๊กมาร์กส่วนบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="8082c-135">If there are changes you'd like to save, you can also create a personal bookmark.</span></span> <span data-ttu-id="8082c-136">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [บุ๊กมาร์กคืออะไร](end-user-bookmarks.md)</span><span class="sxs-lookup"><span data-stu-id="8082c-136">For more information, see [What are bookmarks?](end-user-bookmarks.md).</span></span>

<span data-ttu-id="8082c-137">บานหน้าต่าง **ตัวกรอง** จะแสดงและจัดการตัวกรองรายงานหลายชนิด: รายงาน หน้ารายงาน และวิชวล</span><span class="sxs-lookup"><span data-stu-id="8082c-137">The **Filters** pane displays and manages several types of report filters: report, report page, and visual.</span></span>

<span data-ttu-id="8082c-138">ในตัวอย่างนี้ เราได้เลือกวิชวลที่มีตัวกรองสามตัว: **ผู้ผลิต** **เดือน** และ **หน่วยทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="8082c-138">In this example, we've selected a visual that has three filters: **Manufacturer**, **Month**, and **Total units**.</span></span> <span data-ttu-id="8082c-139">หน้ารายงานยังมีตัวกรอง ซึ่งแสดงรายการภายใต้หัวเรื่อง **ตัวกรองในหน้านี้**</span><span class="sxs-lookup"><span data-stu-id="8082c-139">The report page also has filters, listed under the **Filters on this page** heading.</span></span> <span data-ttu-id="8082c-140">และรายงานทั้งหมดมีตัวกรองสำหรับ **วันที่** แสดงอยู่ภายใต้ **ตัวกรองบนหน้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="8082c-140">And, the entire report has a filter for **Date**, listed under **Filters on all pages**.</span></span>

![สกรีนช็อตของรายงานที่มีการแสดงภาพและตัวกรองที่เกี่ยวข้องที่เรียกออก](media/end-user-report-filter/power-bi-filter-pane.png)

<span data-ttu-id="8082c-142">บางตัวกรองมี **(ทั้งหมด)** อยู่ถัดจากตัวกรองเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="8082c-142">Some of the filters have **(All)** next to them.</span></span> <span data-ttu-id="8082c-143">\*\*(ทั้งหมด) \*\* หมายความว่าค่าทั้งหมดจะถูกรวมอยู่ในตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="8082c-143">**(All)** means all values are being included in the filter.</span></span> <span data-ttu-id="8082c-144">ในสกรีนช็อตข้างต้น **Segment(All)** จะบอกให้เราว่าหน้ารายงานนี้มีข้อมูลเกี่ยวกับเซ็กเมนต์ผลิตภัณฑ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8082c-144">In the screenshot above, **Segment(All)** tells us this report page includes data about all the product segments.</span></span> 

<span data-ttu-id="8082c-145">ทุกคนที่มีสิทธิ์ดูรายงานนี้สามารถโต้ตอบกับตัวกรองเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="8082c-145">Anyone with permissions to view this report can interact with these filters.</span></span>

### <a name="view-only-those-filters-applied-to-a-visual"></a><span data-ttu-id="8082c-146">ดูเฉพาะตัวกรองที่นำไปใช้กับวิชวลเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8082c-146">View only those filters applied to a visual</span></span>

<span data-ttu-id="8082c-147">เมื่อต้องการดูรายละเอียดตัวกรองที่ส่งผลกระทบต่อวิชวลเฉพาะ ให้โฮเวอร์เหนือวิชวลเพื่อแสดงไอคอนตัวกรอง ![สกรีนช็อตของไอคอนตัวกรอง](media/end-user-report-filter/power-bi-filter-icon.png)</span><span class="sxs-lookup"><span data-stu-id="8082c-147">To get a closer look at the filters affecting a specific visual, hover over the visual to reveal the filter icon ![Screenshot of the Filter icon.](media/end-user-report-filter/power-bi-filter-icon.png).</span></span> <span data-ttu-id="8082c-148">เลือกไอคอนตัวกรองเพื่อดูเมนูแบบป็อปอัพที่มีตัวกรองทั้งหมด ตัวแบ่งส่วนข้อมูล และอื่นๆ ที่มีผลต่อวิชวลนั้น</span><span class="sxs-lookup"><span data-stu-id="8082c-148">Select that filter icon to see a pop-up with all the filters, slicers, and so on, affecting that visual.</span></span> <span data-ttu-id="8082c-149">ตัวกรองบนป๊อปอัพมีตัวกรองเดียวกันที่แสดงอยู่ในบานหน้าต่าง **ตัวกรอง** รวมถึงการกรองเพิ่มเติมที่ส่งผลกระทบต่อวิชวลที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8082c-149">The filters on the pop-up include the same filters displayed on the **Filters** pane, plus any additional filtering affecting the selected visual.</span></span>

![สกรีนช็อตของรายการตัวกรองที่มีลูกศรชี้ไปที่ตัวกรองเหล่านั้นอยู่ในบานหน้าต่างตัวกรอง](media/end-user-report-filter/power-bi-filters-hover.png)

<span data-ttu-id="8082c-151">นี่คือชนิดตัวกรองที่มุมมองนี้สามารถแสดงได้:</span><span class="sxs-lookup"><span data-stu-id="8082c-151">Here are the types of filters this view can display:</span></span>

- <span data-ttu-id="8082c-152">ตัวกรองพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="8082c-152">Basic filters</span></span>
- <span data-ttu-id="8082c-153">ตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8082c-153">Slicers</span></span>
- <span data-ttu-id="8082c-154">ไฮไลต์เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="8082c-154">Cross-highlighting</span></span>
- <span data-ttu-id="8082c-155">กรองข้าม</span><span class="sxs-lookup"><span data-stu-id="8082c-155">Cross-filtering</span></span>
- <span data-ttu-id="8082c-156">ตัวกรองขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="8082c-156">Advanced filters</span></span>
- <span data-ttu-id="8082c-157">ตัวกรอง Top N</span><span class="sxs-lookup"><span data-stu-id="8082c-157">Top N filters</span></span>
- <span data-ttu-id="8082c-158">ตัวกรองวันที่ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8082c-158">Relative Date filters</span></span>
- <span data-ttu-id="8082c-159">ตัวแบ่งส่วนข้อมูลซิงค์</span><span class="sxs-lookup"><span data-stu-id="8082c-159">Sync-slicers</span></span>
- <span data-ttu-id="8082c-160">ตัวกรอง รวม/ไม่รวม</span><span class="sxs-lookup"><span data-stu-id="8082c-160">Include/Exclude filters</span></span>
- <span data-ttu-id="8082c-161">ตัวกรองที่ส่งผ่าน URL</span><span class="sxs-lookup"><span data-stu-id="8082c-161">Filters passed through a URL</span></span>

<span data-ttu-id="8082c-162">ในตัวอย่างนี้:</span><span class="sxs-lookup"><span data-stu-id="8082c-162">In this example:</span></span>
1. <span data-ttu-id="8082c-163">**รวม**บอกเราว่าวิชวลได้รับการกรองแบบข้าม</span><span class="sxs-lookup"><span data-stu-id="8082c-163">**Included** tells us that the visual has been cross-filtered.</span></span> <span data-ttu-id="8082c-164">สิ่งนี้หมายความว่ารัฐอลาบามา และเท็กซัสได้ถูกเลือกไว้บนหนึ่งในวิชวลอื่น ๆ บนหน้ารายงานนี้</span><span class="sxs-lookup"><span data-stu-id="8082c-164">What this means is that the states of Alabama and Texas have been selected on one of the other visuals on this report page.</span></span> <span data-ttu-id="8082c-165">ในกรณีนี้ นี่เป็นวิชวลแผนที่</span><span class="sxs-lookup"><span data-stu-id="8082c-165">In this case, it's the map visual.</span></span> <span data-ttu-id="8082c-166">การคัดเลือกทั้งสองรัฐมีการตัดข้อมูลสำหรับรัฐอื่น ๆ ทั้งหมดออกจากการแสดงบนแผนภูมิแท่งที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="8082c-166">The selection of those two states has eliminated data for all other states from displaying on the selected bar chart.</span></span>  

1. <span data-ttu-id="8082c-167">**วันที่**คือตัวกรองที่นำไปใช้กับทุกหน้าในรายงานนี้</span><span class="sxs-lookup"><span data-stu-id="8082c-167">**Date** is a filter applied to all pages in this report.</span></span>

1. <span data-ttu-id="8082c-168">**ภูมิภาคคือภาคกลาง**และ**ปีคือ 2014** เป็นตัวกรองที่นำไปใช้กับหน้ารายงานนี้</span><span class="sxs-lookup"><span data-stu-id="8082c-168">**Region is Central** and **Year is 2014** are filters applied to this report page.</span></span>

4. <span data-ttu-id="8082c-169">**ผู้ผลิตคือ VanArsdel, Natura, Aliqui, หรือ Pirum** เป็นตัวกรองที่นำไปใช้กับวิชวลนี้</span><span class="sxs-lookup"><span data-stu-id="8082c-169">**Manufacturer is VanArsdel, Natura, Aliqui, or Pirum** is a filter applied to this visual.</span></span>


### <a name="search-in-a-filter"></a><span data-ttu-id="8082c-170">ค้นหาในตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="8082c-170">Search in a filter</span></span>

<span data-ttu-id="8082c-171">ในบางครั้งตัวกรองอาจมีรายการค่าที่ยาว</span><span class="sxs-lookup"><span data-stu-id="8082c-171">Sometimes a filter can have a long list of values.</span></span> <span data-ttu-id="8082c-172">ใช้กล่องค้นหาเพื่อค้นหา และเลือกค่าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="8082c-172">Use the search box to find and select the value you want.</span></span>

![สกรีนช็อตวิธีการค้นหาในตัวกรอง](media/end-user-report-filter/power-bi-search-filter.png)

### <a name="display-filter-details"></a><span data-ttu-id="8082c-174">แสดงรายละเอียดตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="8082c-174">Display filter details</span></span>

<span data-ttu-id="8082c-175">หากต้องการทำความเข้าใจตัวกรอง ให้ขยายและดูค่าและจำนวนที่ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="8082c-175">To understand a filter, expand it and take a look at the available values and counts.</span></span>  <span data-ttu-id="8082c-176">หากต้องการขยายตัวกรอง ให้เลือกลูกศรที่อยู่ถัดจากชื่อตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="8082c-176">To expand the filter, select the arrow next to the filter name.</span></span>
  
![สกรีนช็อตของตัวกรองที่แสดงข้อมูลภูมิภาคตะวันตกตามที่เลือกไว้](media/end-user-report-filter/power-bi-filters-expand.png)

### <a name="change-filter-selections"></a><span data-ttu-id="8082c-178">เปลี่ยนแปลงการเลือกตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="8082c-178">Change filter selections</span></span>

<span data-ttu-id="8082c-179">วิธีหนึ่งในการค้นหาข้อมูลเชิงลึกคือการโต้ตอบกับตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="8082c-179">One way to search for data insights is to interact with the filters.</span></span> <span data-ttu-id="8082c-180">คุณสามารถเปลี่ยนการเลือกตัวกรองโดยใช้ลูกศรดรอปดาวน์ถัดจากชื่อเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8082c-180">You can change filter selections using the drop-down arrow next to the field name.</span></span>  <span data-ttu-id="8082c-181">ตัวเลือกของคุณจะมีตั้งแต่ตัวเลือกแบบง่ายจากรายการไปจนถึงการระบุช่วงของวันที่หรือตัวเลข ทั้งนี้ขึ้นอยู่กับตัวกรองและชนิดของข้อมูลที่ Power BI กำลังกรอง</span><span class="sxs-lookup"><span data-stu-id="8082c-181">Depending on the filter and type of data that Power BI is filtering, your options will range from simple selections from a list, to identifying ranges of dates or numbers.</span></span> <span data-ttu-id="8082c-182">ในตัวกรองขั้นสูงด้านล่าง เราได้เปลี่ยนแปลงตัวกรอง **YTD ของหน่วยรวม** บนแผนที่ต้นไม้เพื่อให้อยู่ระหว่าง 2,000 และ 3,000</span><span class="sxs-lookup"><span data-stu-id="8082c-182">In the advanced filter below, we've changed the **Total Units YTD** filter on the treemap to be between 2,000 and 3,000.</span></span> <span data-ttu-id="8082c-183">โปรดสังเกตว่าการเปลี่ยนแปลงนี้จะลบ Pirum ออกจากแผนที่ต้นไม้</span><span class="sxs-lookup"><span data-stu-id="8082c-183">Notice that this change removes Pirum from the treemap.</span></span>
  
![สกรีนช็อตของรายงานและตัวกรองที่แสดงวิชวลแผนที่ต้นไม้ที่เลือกไว้](media/end-user-report-filter/power-bi-treemap-filter.png)

> [!TIP]
> <span data-ttu-id="8082c-185">เมื่อต้องเลือกค่าตัวกรองมากกว่าหนึ่งรายการในแต่ละครั้ง ให้กดแป้น CTRL ค้างไว้</span><span class="sxs-lookup"><span data-stu-id="8082c-185">To select more than one filter value at a time, hold down the CTRL key.</span></span> <span data-ttu-id="8082c-186">ตัวกรองส่วนใหญ่รองรับการเลือกหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="8082c-186">Most filters support multi-select.</span></span>

### <a name="reset-filter-to-default"></a><span data-ttu-id="8082c-187">รีเซ็ตตัวกรองเป็นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8082c-187">Reset filter to default</span></span>

<span data-ttu-id="8082c-188">ถ้าคุณต้องการย้อนกลับการเปลี่ยนแปลงทั้งหมดที่คุณได้ทำกับตัวกรอง ให้เลือก**รีเซ็ตเป็นค่าเริ่มต้น**จากแถบเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="8082c-188">If you want to back out of all changes you've made to the filters, select **Reset to default** from the top menu bar.</span></span>  <span data-ttu-id="8082c-189">การเลือกนี้เปลี่ยนกลับตัวกรองเป็นแบบเดิมตามที่ผู้ออกแบบรายงานตั้งค่าไว้</span><span class="sxs-lookup"><span data-stu-id="8082c-189">This selection reverts the filters to their original state, as set by the report designer.</span></span>

![สกรีนช็อตของตัวเลือกรีเซ็ตเป็นค่าเริ่มต้น](media/end-user-report-filter/power-bi-reset-icon.png)

### <a name="clear-a-filter"></a><span data-ttu-id="8082c-191">ล้างตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="8082c-191">Clear a filter</span></span>

<span data-ttu-id="8082c-192">เมื่อต้องการรีเซ็ตตัวกรองเป็น (ทั้งหมด) ให้ล้างข้อมูลด้วยการเลือกไอคอนยางลบที่อยู่ถัดจากชื่อตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="8082c-192">To reset a filter to (All), clear it by selecting the eraser icon next to the filter name.</span></span>

![สกรีนช็อตของไอคอนยางลบ](media/end-user-report-filter/power-bi-erase.png)
  
<!--  too much detail for consumers

## Types of filters: text field filters
### List mode
Ticking a checkbox either selects or deselects the value. The **All** checkbox can be used to toggle the state of all checkboxes on or off. The checkboxes represent all the available values for that field.  As you adjust the filter, the restatement updates to reflect your choices. 

![list mode filter](media/end-user-report-filter/power-bi-restatement-new.png)

Note how the restatement now says "is Mar, Apr or May".

### Advanced mode
Select **Advanced Filtering** to switch to advanced mode. Use the dropdown controls and text boxes to identify which fields to include. By choosing between **And** and **Or**, you can build complex filter expressions. Select the **Apply Filter** button when you've set the values you want.  

![advanced mode](media/end-user-report-filter/power-bi-advanced.png)

## Types of filters: numeric field filters
### List mode
If the values are finite, selecting the field name displays a list.  See **Text field filters** &gt; **List mode** above for help using checkboxes.   

### Advanced mode
If the values are infinite or represent a range, selecting the field name opens the advanced filter mode. Use the dropdown and text boxes to specify a range of values that you want to see. 

![advanced filter](media/end-user-report-filter/power-bi-dropdown-and-text.png)

By choosing between **And** and **Or**, you can build complex filter expressions. Select the **Apply Filter** button when you've set the values you want.

## Types of filters: date and time
### List mode
If the values are finite, selecting the field name displays a list.  See **Text field filters** &gt; **List mode** above for help using checkboxes.   

### Advanced mode
If the field values represent date or time, you can specify a start/end time when using Date/Time filters.  

![datetime filter](media/end-user-report-filter/pbi_date-time-filters.png)

-->

## <a name="next-steps"></a><span data-ttu-id="8082c-194">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="8082c-194">Next steps</span></span>

<span data-ttu-id="8082c-195">เรียนรู้วิธีที่ [วิชวลกรองแบบไขว้และข้ามไฮไลท์ของแต่ละตัวบนหน้ารายงาน](end-user-interactions.md)</span><span class="sxs-lookup"><span data-stu-id="8082c-195">Learn how and why [visuals cross-filter and cross-highlight each other on a report page](end-user-interactions.md)</span></span>
