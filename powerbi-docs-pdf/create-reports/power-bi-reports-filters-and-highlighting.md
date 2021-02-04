---
title: ตัวกรองและการไฮไลท์ในรายงาน Power BI
description: เกี่ยวกับตัวกรองและการไฮไลท์ในรายงาน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: conceptual
ms.date: 10/23/2019
LocalizationGroup: Reports
ms.openlocfilehash: 9a793ff966f7560924f53357ce7518f0ede65c56
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96393588"
---
# <a name="filters-and-highlighting-in-power-bi-reports"></a><span data-ttu-id="1f0bf-103">ตัวกรองและการไฮไลท์ในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="1f0bf-103">Filters and highlighting in Power BI reports</span></span>
 <span data-ttu-id="1f0bf-104">บทความนี้ทำการแนะนำการใช้ตัวกรองและการไฮไลท์ในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="1f0bf-104">This article introduces you to filtering and highlighting in the Power BI service.</span></span> <span data-ttu-id="1f0bf-105">ประสบการณ์การใช้งานนั้นแทบจะเหมือนกับใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="1f0bf-105">The experience is almost exactly the same in Power BI Desktop.</span></span> <span data-ttu-id="1f0bf-106">*ตัวกรอง* ให้ลบออกทั้งหมดยกเว้นข้อมูลที่คุณต้องการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="1f0bf-106">*Filters* remove all but the data you want to focus on.</span></span> <span data-ttu-id="1f0bf-107">*การไฮไลต์* ไม่ใช่การกรอง</span><span class="sxs-lookup"><span data-stu-id="1f0bf-107">*Highlighting* isn't filtering.</span></span> <span data-ttu-id="1f0bf-108">โดยจะไม่ลบข้อมูลออก แต่จะไฮไลต์เซตย่อยของข้อมูลที่สามารถมองเห็นได้แทน ซึ่งข้อมูลที่ไม่ได้ไฮไลต์ยังคงสามารถจะมองเห็นได้แต่จะเป็นสีจาง</span><span class="sxs-lookup"><span data-stu-id="1f0bf-108">It doesn't remove data, but instead highlights a subset of the visible data; the data that isn't highlighted remains visible but dimmed.</span></span>

<span data-ttu-id="1f0bf-109">มีหลายวิธีคุณสามารถกรอง และไฮไลท์รายงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="1f0bf-109">There are many different ways you can filter and highlight reports in Power BI.</span></span> <span data-ttu-id="1f0bf-110">การอัดข้อมูลทั้งหมดในบทความเดียวจะสร้างความสับสน ดังนั้นจึงได้แบ่งส่วนออกมาดังนี้:</span><span class="sxs-lookup"><span data-stu-id="1f0bf-110">Putting all of that information in one article would get confusing, so we've broken it into these sections:</span></span>

* <span data-ttu-id="1f0bf-111">แนะนำตัวกรองและการไฮไลท์ บทความที่คุณกำลังอ่านในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="1f0bf-111">Introduction to filters and highlighting, the article you're reading now.</span></span>
* <span data-ttu-id="1f0bf-112">วิธีการ[สร้างและใช้ตัวกรองในมุมมองการแก้ไข](power-bi-report-add-filter.md)ในรายงานใน Power BI Desktop และบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="1f0bf-112">How to [create and use filters in Editing view](power-bi-report-add-filter.md) in reports in Power BI Desktop and the Power BI service.</span></span> <span data-ttu-id="1f0bf-113">เมื่อคุณมีสิทธิ์การแก้ไขสำหรับรายงาน คุณสามารถสร้าง, แก้ไข และลบตัวกรองในรายงานได้</span><span class="sxs-lookup"><span data-stu-id="1f0bf-113">When you have editing permissions for a report, you can create, modify, and delete filters in reports.</span></span>
* <span data-ttu-id="1f0bf-114">วิธีที่วิชวล[กรองและไฮไลต์ในรายงานที่แชร์ร่วมกับคุณ](../consumer/end-user-interactions.md) ในมุมมองการอ่านรายงานในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="1f0bf-114">How visuals [filter and highlight in a report shared with you](../consumer/end-user-interactions.md), in report Reading view in the Power BI service.</span></span> <span data-ttu-id="1f0bf-115">สิ่งที่คุณสามารถดำเนินการได้มีข้อจำกัดมาก อย่างไรก็ตามคุณยังคงมีตัวเลือกการกรองและการไฮไลต์อีกมากมาย</span><span class="sxs-lookup"><span data-stu-id="1f0bf-115">What you can do is more limited, but you still have a wide range of filtering and highlighting options.</span></span>  
* <span data-ttu-id="1f0bf-116">รายละเอียดของตัวควบคุม[ตัวกรองและการไฮไลต์](power-bi-report-add-filter.md)ที่พร้อมใช้งานในมุมมองการแก้ไขใน Power BI Desktop และบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="1f0bf-116">A detailed tour of the [filter and highlighting controls available in Editing view](power-bi-report-add-filter.md) in Power BI Desktop and the Power BI service.</span></span> <span data-ttu-id="1f0bf-117">บทความนี้จะศึกษาเชิงลึกเกี่ยวกับประเภทของตัวกรองเช่น วันที่และเวลา ตัวเลข และข้อความ</span><span class="sxs-lookup"><span data-stu-id="1f0bf-117">The article takes an in-depth look at types of filters such as date and time, numeric, and text.</span></span> <span data-ttu-id="1f0bf-118">นอกจากนี้ยังครอบคลุมความแตกต่างระหว่างตัวเลือกพื้นฐานและขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="1f0bf-118">It also covers the differences between basic and advanced options.</span></span>
* <span data-ttu-id="1f0bf-119">หลังจากที่ได้เรียนรู้วิธีการทำงานของตัวกรองและไฮไลท์ตามค่าเริ่มต้นแล้ว ลองเรียนรู้การ [เปลี่ยนวิธีที่การจัดรูปแบบการแสดงข้อมูลบนตัวกรองหน้าและไฮไลต์ซึ่งกันและกัน](service-reports-visual-interactions.md)</span><span class="sxs-lookup"><span data-stu-id="1f0bf-119">After you've learned how filters and highlighting work by default, learn how to [change the way visualizations on a page filter and highlight each other](service-reports-visual-interactions.md)</span></span>

<span data-ttu-id="1f0bf-120">**คุณทราบหรือไม่**</span><span class="sxs-lookup"><span data-stu-id="1f0bf-120">**Did you know?**</span></span> <span data-ttu-id="1f0bf-121">Power BI มีการใช้งานตัวกรองใหม่</span><span class="sxs-lookup"><span data-stu-id="1f0bf-121">Power BI has a new filter experience.</span></span> <span data-ttu-id="1f0bf-122">อ่านเพิ่มเติมเกี่ยวกับ[การใช้งานตัวกรองใหม่ในรายงาน Power BI](power-bi-report-filter.md)</span><span class="sxs-lookup"><span data-stu-id="1f0bf-122">Read more about [the new filter experience in Power BI reports](power-bi-report-filter.md).</span></span>

![ประสบการณ์ใช้งานตัวกรองใหม่](media/power-bi-reports-filters-and-highlighting/power-bi-filter-reading.png)


## <a name="intro-to-the-filters-pane"></a><span data-ttu-id="1f0bf-124">บทแนะนำบานหน้าต่างตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="1f0bf-124">Intro to the Filters pane</span></span>

<span data-ttu-id="1f0bf-125">คุณสามารถใช้ตัวกรองในบานหน้าต่าง **ตัวกรอง** หรือโดย [สร้างการเลือกในตัวแบ่งส่วนข้อมูล](../visuals/power-bi-visualization-slicers.md) โดยตรงบนรายงาน</span><span class="sxs-lookup"><span data-stu-id="1f0bf-125">You can apply filters in the **Filters** pane or by [making selections in slicers](../visuals/power-bi-visualization-slicers.md) directly on the report itself.</span></span> <span data-ttu-id="1f0bf-126">บานหน้าต่างตัวกรองแสดงตารางและเขตข้อมูลที่ใช้ในรายงานและตัวกรองที่มีการใช้ ถ้ามี</span><span class="sxs-lookup"><span data-stu-id="1f0bf-126">The Filters pane shows the tables and fields used in the report and the filters that have been applied, if any.</span></span> 

![พื้นที่ตัวกรอง](media/power-bi-reports-filters-and-highlighting/power-bi-add-filter-reading-view.png)

<span data-ttu-id="1f0bf-128">ตัวกรองสี่ประเภท</span><span class="sxs-lookup"><span data-stu-id="1f0bf-128">There are four types of filters.</span></span>

- <span data-ttu-id="1f0bf-129">**ตัวกรองหน้า** ใช้กับภาพทั้งหมดบนหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="1f0bf-129">**page filter** applies to all the visuals on the report page</span></span>     
- <span data-ttu-id="1f0bf-130">**ตัวกรองภาพ** ใช้กับภาพเดียวบนหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="1f0bf-130">**visual filter** applies to a single visual on a report page.</span></span> <span data-ttu-id="1f0bf-131">หากคุณเลือกภาพบนพื้นที่รายงาน คุณจะเห็นตัวกรองระดับภาพเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1f0bf-131">You only see visual level filters if you've selected a visual on the report canvas.</span></span>    
- <span data-ttu-id="1f0bf-132">**ตัวกรองรายงาน** นำไปใช้กับทุกหน้าในรายงาน</span><span class="sxs-lookup"><span data-stu-id="1f0bf-132">**report filter** applies to all pages in the report</span></span>    
- <span data-ttu-id="1f0bf-133">**ตัวกรอง drillthrough** นำไปใช้กับเอนทิตีแบบเดียวในรายงาน</span><span class="sxs-lookup"><span data-stu-id="1f0bf-133">**drillthrough filter** applies to a single entity in a report</span></span>    

<span data-ttu-id="1f0bf-134">คุณสามารถค้นหาในตัวกรองหน้า, ตัวกรองภาพ และตัวกรองรายงานในมุมมองการอ่านหรือมุมมองการแก้ไข เพื่อค้นหาและเลือกค่าที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="1f0bf-134">You can search in page, visual, and report filters, in Reading or Editing view, to find and select the value you want.</span></span> 

![ค้นหาในตัวกรอง](media/power-bi-reports-filters-and-highlighting/power-bi-search-filter.png)

<span data-ttu-id="1f0bf-136">หากตัวกรองมีคำว่า **ทั้งหมด** ด้านข้าง หมายความว่า ค่าทั้งหมดในเขตข้อมูลจะรวมอยู่ในตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="1f0bf-136">If the filter has the word **All** next to it, that means all the values in the field are included in the filter.</span></span>  <span data-ttu-id="1f0bf-137">ตัวอย่างเช่น **สาขา (ทั้งหมด)** ในสกรีนช็อตด้านล่าง หมายถึงหน้ารายงานนี้มีข้อมูลเกี่ยวกับสาขาร้านค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="1f0bf-137">For example, **Chain(All)** in the screenshot below means this report page includes data about all the store chains.</span></span>  <span data-ttu-id="1f0bf-138">ในทางกลับกัน ตัวกรองระดับรายงาน **FiscalYear เป็น 2013 หรือ 2014** แสดงถึงรายงานที่มีข้อมูลสำหรับปีงบประมาณ 2013 และ 2014 เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1f0bf-138">On the other hand, the report-level filter **FiscalYear is 2013 or 2014** tells us that the report only includes data for the fiscal years of 2013 and 2014.</span></span>

## <a name="filters-in-reading-or-editing-view"></a><span data-ttu-id="1f0bf-139">ตัวกรองในมุมมองการอ่านหรือมุมมองการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="1f0bf-139">Filters in Reading or Editing view</span></span>
<span data-ttu-id="1f0bf-140">มีการโต้ตอบกับรายงานสองโหมด คือ [มุมมองการอ่าน](../consumer/end-user-reading-view.md) และมุมมองการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="1f0bf-140">There are two modes for interacting with reports: [Reading view](../consumer/end-user-reading-view.md) and Editing view.</span></span> <span data-ttu-id="1f0bf-141">ความสามารถในการกรองที่พร้อมใช้งานสำหรับคุณจะขึ้นอยู่กับโหมดที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1f0bf-141">The filtering capabilities available to you depend on which mode you're in.</span></span>

* <span data-ttu-id="1f0bf-142">ในมุมมองการแก้ไข คุณสามารถเพิ่มตัวกรองรายงาน, ตัวกรองหน้า, ตัวกรอง Drillthrough และตัวกรองภาพ</span><span class="sxs-lookup"><span data-stu-id="1f0bf-142">In Editing view, you can add report, page, drillthrough, and visual filters.</span></span> <span data-ttu-id="1f0bf-143">เมื่อคุณบันทึกรายงาน ตัวกรองจะถูกบันทึกไปกับรายงานด้วย แม้ว่าคุณจะเปิดในแอปสำหรับอุปกรณ์เคลื่อนที่ก็ตาม</span><span class="sxs-lookup"><span data-stu-id="1f0bf-143">When you save the report, the filters are saved with the report, even if you open it in a mobile app.</span></span> <span data-ttu-id="1f0bf-144">บุคคลที่กำลังดูรายงานในมุมมองการอ่านสามารถโต้ตอบกับตัวกรองที่คุณเพิ่มได้ แต่ไม่สามารถเพิ่มตัวกรองใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="1f0bf-144">People looking at the report in Reading view can interact with the filters you added, but can't add new filters.</span></span>
* <span data-ttu-id="1f0bf-145">ในมุมมองการอ่าน คุณสามารถโต้ตอบกับตัวกรองใด ๆ ที่มีอยู่แล้วในรายงาน และบันทึกการเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="1f0bf-145">In Reading view, you can interact with any filters that already exist in the report, and save the selections you make.</span></span> <span data-ttu-id="1f0bf-146">คุณไม่สามารถเพิ่มตัวกรองใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="1f0bf-146">You can't add new filters.</span></span>

### <a name="filters-in-reading-view"></a><span data-ttu-id="1f0bf-147">ตัวกรองในมุมมองการอ่าน</span><span class="sxs-lookup"><span data-stu-id="1f0bf-147">Filters in Reading view</span></span>
<span data-ttu-id="1f0bf-148">หากคุณเข้าถึงรายงานในมุมมองการอ่านเท่านั้น บานหน้าต่างตัวกรองจะมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="1f0bf-148">If you only have access to a report in Reading view, the Filters pane looks similar to this:</span></span>

![ตัวกรองในมุมมองการอ่าน](media/power-bi-reports-filters-and-highlighting/power-bi-filter-reading-view.png)

<span data-ttu-id="1f0bf-150">หน้านี้ของรายงานมีตัวกรองระดับหน้า 6 ตัว และตัวกรองระดับรายงาน 1 ตัว</span><span class="sxs-lookup"><span data-stu-id="1f0bf-150">So this page of the report has six page-level filters and one report-level filter.</span></span>

<span data-ttu-id="1f0bf-151">แต่ละภาพสามารถมีตัวกรองสำหรับทุกเขตข้อมูลในภาพดังกล่าวได้ และผู้เขียนรายงานอาจเพิ่มตัวกรองอื่น ๆ อีก</span><span class="sxs-lookup"><span data-stu-id="1f0bf-151">Each visual can have filters for all the fields in the visual, and a report author may add more.</span></span> <span data-ttu-id="1f0bf-152">ในรูปภาพด้านล่าง แผนภูมิฟองมีตัวกรองหกตัว</span><span class="sxs-lookup"><span data-stu-id="1f0bf-152">In the image below, the bubble chart has six filters.</span></span>

![ตัวกรองระดับวิชวล](media/power-bi-reports-filters-and-highlighting/power-bi-filter-visual-level.png)

<span data-ttu-id="1f0bf-154">ในมุมมองการอ่าน สำรวจข้อมูลโดยการปรับเปลี่ยนตัวกรองที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="1f0bf-154">In Reading view, explore the data by modifying the existing filters.</span></span> <span data-ttu-id="1f0bf-155">เปลี่ยนแปลงที่คุณเซฟในรายงาน แม้ว่าคุณดูรายงานในแอปสำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="1f0bf-155">The changes you make are saved with the report, even if you open the report in a mobile app.</span></span> <span data-ttu-id="1f0bf-156">เรียนรู้วิธีเมื่อคุณ [สำรวจบานหน้าต่างตัวกรองรายงาน](../consumer/end-user-report-filter.md)</span><span class="sxs-lookup"><span data-stu-id="1f0bf-156">Learn how when you [take a tour of the report Filters pane](../consumer/end-user-report-filter.md)</span></span>

<span data-ttu-id="1f0bf-157">เมื่อคุณออกจากรายงาน ตัวกรองของคุณจะถูกบันทึก</span><span class="sxs-lookup"><span data-stu-id="1f0bf-157">When you exit the report, your filters are saved.</span></span> <span data-ttu-id="1f0bf-158">หากต้องการยกเลิกการกรองของคุณและกลับไปยังการกรอง, การแบ่งส่วนข้อมูล, การดูรายละเอียด และชุดการเรียงลำดับ ตามค่าเริ่มต้นของผู้เขียนรายงาน ให้เลือก **รีเซ็ตเป็นค่าเริ่มต้น** จากแถบเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="1f0bf-158">To undo your filtering and return to the default filtering, slicing, drill, and sorting set by the report author, select **Reset to default** from the top menubar.</span></span>

![รีเซ็ตเป็นไอคอนเริ่มต้น](media/power-bi-reports-filters-and-highlighting/power-bi-reset-to-default.png)

### <a name="filters-in-editing-view"></a><span data-ttu-id="1f0bf-160">ตัวกรองในมุมมองการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="1f0bf-160">Filters in Editing view</span></span>
<span data-ttu-id="1f0bf-161">เมื่อคุณมีสิทธิ์ระดับเจ้าของสำหรับรายงาน และเปิดในมุมมองการแก้ไข คุณจะเห็นว่า **ตัวกรอง** เป็นเพียงหนึ่งในบานหน้าต่างตัวแก้ไข</span><span class="sxs-lookup"><span data-stu-id="1f0bf-161">When you have owner permissions for a report and open it in Editing view, you see that **Filters** is just one of several editing panes available.</span></span>

![บานหน้าต่างตัวกรองในมุมมองการแก้ไข](media/power-bi-reports-filters-and-highlighting/power-bi-add-filter-editing-view.png)

<span data-ttu-id="1f0bf-163">ในมุมมองการอ่าน จะเห็นหน้านี้ของรายงานมีตัวกรองระดับหน้า 6 ตัว และตัวกรองระดับรายงาน 1 ตัว</span><span class="sxs-lookup"><span data-stu-id="1f0bf-163">As in Reading view, we see this page of the report has six page-level filters and one report-level filter.</span></span> <span data-ttu-id="1f0bf-164">และโดยการเลือกแผนภูมิฟอง เราจะเห็นว่ามีตัวกรองระดับภาพ 6 ตัวถูกใช้อยู่</span><span class="sxs-lookup"><span data-stu-id="1f0bf-164">And by selecting the bubble chart, we'd see it has six visual level filters applied.</span></span>

<span data-ttu-id="1f0bf-165">เราสามารถจัดการตัวกรองและการไฮไลต์ในมุมมองการแก้ไขได้มากขึ้น</span><span class="sxs-lookup"><span data-stu-id="1f0bf-165">We can do more with filters and highlighting in Editing view.</span></span> <span data-ttu-id="1f0bf-166">โดยส่วนใหญ่เราสามารถเพิ่มตัวกรองใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="1f0bf-166">Mainly, we can add new filters.</span></span> <span data-ttu-id="1f0bf-167">เรียนรู้วิธีการ [เพิ่มตัวกรองไปยังรายงาน](power-bi-report-add-filter.md) และอีกมากมาย</span><span class="sxs-lookup"><span data-stu-id="1f0bf-167">Learn how to [Add a filter to a report](power-bi-report-add-filter.md) and much more.</span></span>

## <a name="ad-hoc-highlighting"></a><span data-ttu-id="1f0bf-168">การไฮไลต์เฉพาะกิจ</span><span class="sxs-lookup"><span data-stu-id="1f0bf-168">Ad hoc highlighting</span></span>
<span data-ttu-id="1f0bf-169">เลือกป้ายชื่อค่าหรือแกนในวิชวลเพื่อไฮไลต์วิชวลอื่น ๆ บนหน้า</span><span class="sxs-lookup"><span data-stu-id="1f0bf-169">Select a value or axis label in a visual to highlight the other visuals on the page.</span></span> <span data-ttu-id="1f0bf-170">หากต้องการลบไฮไลต์ออก ให้เลือกค่าอีกครั้งหรือเลือกพื้นที่ว่างในวิชวลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="1f0bf-170">To remove the highlighting, select the value again, or select any empty space in the same visual.</span></span> <span data-ttu-id="1f0bf-171">การไฮไลต์คือวิธีการที่สนุกในการสำรวจผลกระทบของข้อมูลอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="1f0bf-171">Highlighting is a fun way to quickly explore data impacts.</span></span> <span data-ttu-id="1f0bf-172">หากต้องการปรับแต่งวิธีการทำงานของการไฮไลต์เชื่อมโยง สามารถดูได้ที่ [การโต้ตอบของภาพ](service-reports-visual-interactions.md)</span><span class="sxs-lookup"><span data-stu-id="1f0bf-172">To fine-tune how this type of cross-highlighting works, see [Visual interactions](service-reports-visual-interactions.md).</span></span>

![ไฮไลต์เชื่อมโยง](media/power-bi-reports-filters-and-highlighting/power-bi-adhoc-filter.gif)


## <a name="next-steps"></a><span data-ttu-id="1f0bf-174">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="1f0bf-174">Next steps</span></span>

[<span data-ttu-id="1f0bf-175">การใช้งานตัวกรองใหม่ในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="1f0bf-175">The new filter experience in Power BI reports</span></span>](power-bi-report-filter.md)

[<span data-ttu-id="1f0bf-176">เพิ่มตัวกรองไปยังรายงาน (ในมุมมองการแก้ไข)</span><span class="sxs-lookup"><span data-stu-id="1f0bf-176">Add a filter to a report (in Editing view)</span></span>](power-bi-report-add-filter.md)

[<span data-ttu-id="1f0bf-177">ชมการแนะนำของตัวกรองรายงาน</span><span class="sxs-lookup"><span data-stu-id="1f0bf-177">Take a tour of report filters</span></span>](../consumer/end-user-report-filter.md)

[<span data-ttu-id="1f0bf-178">เปลี่ยนวิธีที่่ภาพรายงานกรองแบบไขว้ และข้ามไฮไลท์ของแต่ละตัว</span><span class="sxs-lookup"><span data-stu-id="1f0bf-178">Change how report visuals cross-filter and cross-highlight each other</span></span>](../consumer/end-user-interactions.md)

<span data-ttu-id="1f0bf-179">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="1f0bf-179">More questions?</span></span> [<span data-ttu-id="1f0bf-180">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="1f0bf-180">Try the Power BI Community</span></span>](https://community.powerbi.com/)
