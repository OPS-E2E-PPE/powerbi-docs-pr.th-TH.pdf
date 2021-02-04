---
title: ใช้ตัวแบ่งส่วนหรือตัวกรองเวลา่แบบสัมพัทธ์ใน Power BI
description: เรียนรู้วิธีการใช้ตัวแบ่งส่วนหรือตัวกรองเพื่อจำกัดช่วงเวลาสัมพันธ์ใน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 07/06/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 4b12760584df2471bf02029be0fb428d1ab21e4c
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96387562"
---
# <a name="use-a-relative-time-slicer-and-filter-in-power-bi"></a><span data-ttu-id="d9f50-103">ใช้ตัวแบ่งส่วนและตัวกรองเวลาแบบสัมพัทธ์ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="d9f50-103">Use a relative time slicer and filter in Power BI</span></span>

<span data-ttu-id="d9f50-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-desktop](../includes/yes-desktop.md)] [!INCLUDE [yes-service](../includes/yes-service.md)]</span><span class="sxs-lookup"><span data-stu-id="d9f50-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-desktop](../includes/yes-desktop.md)] [!INCLUDE [yes-service](../includes/yes-service.md)]</span></span>

<span data-ttu-id="d9f50-105">ด้วยสถานการณ์การรีเฟรชอย่างรวดเร็วที่เกิดขึ้นใหม่ ความสามารถในการกรองไปยังหน้าต่างที่มีขนาดเล็กกว่าจะมีประโยชน์</span><span class="sxs-lookup"><span data-stu-id="d9f50-105">With emerging fast refresh scenarios, the ability to filter to a smaller window of time can be useful.</span></span> <span data-ttu-id="d9f50-106">ด้วยตัวแบ่งส่วนเวลาแบบสัมพัทธ์หรือตัวกรองวันที่ี่แบบสัมพัทธ์ คุณสามารถใช้ตัวกรองที่ยึดตามเวลากับคอลัมน์วันที่หรือเวลาใดก็ตามในแบบจำลองข้อมูลของคุณได้</span><span class="sxs-lookup"><span data-stu-id="d9f50-106">Using the relative time slicer or relative time filter, you can apply time-based filters to any date or time column in your data model.</span></span> <span data-ttu-id="d9f50-107">ตัวอย่างเช่น คุณสามารถใช้ตัวแบ่งส่วนเวลาแบบสัมพัทธ์ เพื่อแสดงเฉพาะการดูวิดีโอภายในนาทีหรือชั่วโมงที่ผ่านมาได้</span><span class="sxs-lookup"><span data-stu-id="d9f50-107">For example, you can use the relative time slicer to show only video views within the last minute or hour.</span></span> 

:::image type="content" source="media/slicer-filter-relative-time/power-bi-relative-time.gif" alt-text="สกรีนช็อตของตัวอย่างเวลาสัมพัทธ์":::

<span data-ttu-id="d9f50-109">คุณไม่จำเป็นต้องใช้คุณลักษณะร่วมกับคุณลักษณะ[การรีเฟรชหน้าอัตโนมัติ](../create-reports/desktop-automatic-page-refresh.md)</span><span class="sxs-lookup"><span data-stu-id="d9f50-109">You don't have to use the feature in conjunction with the [automatic page refresh](../create-reports/desktop-automatic-page-refresh.md) feature.</span></span> <span data-ttu-id="d9f50-110">อย่างไรก็ตาม สถานการณ์เวลาที่สัมพันธ์กันหลายรายการจับคู่กับคุณลักษณะการรีเฟรชหน้าอัตโนมัติได้เป็นอย่างดี</span><span class="sxs-lookup"><span data-stu-id="d9f50-110">However, many relative time scenarios pair well with the automatic page refresh feature.</span></span>  

> [!NOTE]
> <span data-ttu-id="d9f50-111">เมื่อคุณใช้ตัวกรองและตัวแบ่งส่วนเวลาแบบสัมพัทธ์ในระดับหน้าหรือรายงาน วิชวลทั้งหมดบนหน้าหรือรายงานนั้นจะถูกกรองไปยังช่วงเวลาที่แน่นอนเดียวกัน โดยใช้เวลา *ของจุดยึด* ที่ใช้งานร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="d9f50-111">When you apply a relative time filter or slicer at the page or report level, all visuals on that page or report are filtered to the exact same time range, using a shared *anchor* time.</span></span> <span data-ttu-id="d9f50-112">เนื่องจากวิชวลอาจมีเวลาการดำเนินการที่แตกต่างกันเล็กน้อย เวลาของจุดยึดที่ใช้ร่วมกันนี้จะรับประกันการซิงโครไนซ์วิชวลทั่วทุกหน้าและทั่วทุกรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="d9f50-112">Because visuals might have slightly different execution times, this shared anchor time ensures that visuals are synchronized across your page or across your report.</span></span> <span data-ttu-id="d9f50-113">อ่านข้อมูลเพิ่มเติมเกี่ยวกับ[เวลาของจุดยึด](#understanding-anchor-time)ในบทความนี้</span><span class="sxs-lookup"><span data-stu-id="d9f50-113">Read more about [anchor time](#understanding-anchor-time) in this article.</span></span>

## <a name="create-a-relative-time-slicer-or-filter"></a><span data-ttu-id="d9f50-114">สร้างตัวแบ่งส่วนหรือตัวกรองเวลา่แบบสัมพัทธ์</span><span class="sxs-lookup"><span data-stu-id="d9f50-114">Create a relative time slicer or filter</span></span>

<span data-ttu-id="d9f50-115">หลังจากที่คุณเปิดใช้งานคุณลักษณะแล้ว คุณสามารถลากและวางเขตข้อมูลวันที่หรือเวลาไปยังเขตข้อมูลที่มีตัวแบ่งส่วน หรือไปยังเขตพื้นที่สำหรับการวางในบานหน้าต่างตัวกรองได้</span><span class="sxs-lookup"><span data-stu-id="d9f50-115">After you've enabled the feature, you can drag and drop the date or time field to the field well of a slicer or to the drop zone in the Filters pane.</span></span> 

### <a name="create-a-slicer"></a><span data-ttu-id="d9f50-116">สร้างตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d9f50-116">Create a slicer</span></span>

1. <span data-ttu-id="d9f50-117">ลากเขตข้อมูลวันที่หรือเวลาไปยังพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="d9f50-117">Drag a date or time field to the canvas.</span></span>

2. <span data-ttu-id="d9f50-118">เลือกประเภทการแสดงภาพของ **ตัวแบ่งส่วน**</span><span class="sxs-lookup"><span data-stu-id="d9f50-118">Select the **Slicer** visualization type.</span></span>

    :::image type="content" source="media/slicer-filter-relative-time/power-bi-relative-time-create-slicer.png" alt-text="สกรีนช็อตของการสร้างตัวแบ่งส่วนข้อมูลเวลา":::

### <a name="create-a-filter"></a><span data-ttu-id="d9f50-120">สร้างตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="d9f50-120">Create a filter</span></span>
 
- <span data-ttu-id="d9f50-121">ลากเขตข้อมูลวันที่หรือเวลาไปยังบานหน้าต่างตัวกรอง สำหรับ **วิชวลนี้** **หน้านี้** หรือ **หน้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="d9f50-121">Drag a date or time field to the Filters pane, for **this visual**, **this page**, or **all pages**.</span></span>

### <a name="set-relative-time"></a><span data-ttu-id="d9f50-122">ตั้งเวลาสัมพัทธ์</span><span class="sxs-lookup"><span data-stu-id="d9f50-122">Set relative time</span></span> 

<span data-ttu-id="d9f50-123">ขั้นตอนถัดไป ให้คุณเปลี่ยนประเภทตัวกรองเป็น **เวลาสัมพัทธ์**</span><span class="sxs-lookup"><span data-stu-id="d9f50-123">Next, you change the filter type to **Relative Time**.</span></span>

:::image type="content" source="media/slicer-filter-relative-time/power-bi-relative-time-set.png" alt-text="สกรีนช็อตของการเปลี่ยนแปลงเป็นเวลาที่สัมพันธ์กัน":::
 
<span data-ttu-id="d9f50-125">นี่คือลักษณะที่ปรากฏในตัวแบ่งส่วน:</span><span class="sxs-lookup"><span data-stu-id="d9f50-125">Here’s how it looks in a slicer:</span></span>

:::image type="content" source="media/slicer-filter-relative-time/power-bi-relative-time-slicer.png" alt-text="สกรีนช็อตของเวลาแบบสัมพัทธ์ในตัวแบ่งส่วนข้อมูล":::

<span data-ttu-id="d9f50-127">นี่คือลักษณะที่ปรากฏในการ์ดตัวกรอง:</span><span class="sxs-lookup"><span data-stu-id="d9f50-127">Here’s how it looks in a filter card:</span></span> 

:::image type="content" source="media/slicer-filter-relative-time/power-bi-relative-time-filter.png" alt-text="สกรีนช็อตของเวลาแบบสัมพัทธ์ในตัวกรอง":::
 
<span data-ttu-id="d9f50-129">ด้วยตัวกรองประเภทใหม่นี้ คุณจึงมีตัวเลือกในการกรองตามช่วงเวลา **ล่าสุด** **ถัดไป** หรือ **ช่วงเวลานี้**:</span><span class="sxs-lookup"><span data-stu-id="d9f50-129">With this new filter type, you can filter based on **Last**, **Next**, or **This time period**:</span></span> 

:::image type="content" source="media/slicer-filter-relative-time/power-bi-relative-time-last-next.png" alt-text="สกรีนช็อตของการเลือกล่าสุด ถัดไป หรือช่วงเวลานี้":::
 
<span data-ttu-id="d9f50-131">คุณกำหนดุหน้าต่างเวลาโดยใช้จำนวนเต็มและหน่วยของเวลา: **นาที** หรือ **ชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="d9f50-131">You specify the time window using a whole number and a unit of time: **Minutes** or **Hours**.</span></span>
 
:::image type="content" source="media/slicer-filter-relative-time/power-bi-relative-time-minutes-hours.png" alt-text="สกรีนช็อตของการเลือกนาทีหรือชั่วโมง":::

<span data-ttu-id="d9f50-133">หากคุณต้องการประหยัดพื้นที่บนพื้นที่ทำงาน คุณยังสามารถสร้างตัวกรองเวลาแบบสัมพัทธ์เป็นการ์ดตัวกรองในบานหน้าต่างตัวกรองได้</span><span class="sxs-lookup"><span data-stu-id="d9f50-133">If you need to save space on the canvas, you can also create the relative time filter as a filter card in the Filters pane.</span></span>

:::image type="content" source="media/slicer-filter-relative-time/power-bi-relative-time-set-filter.png" alt-text="สกรีนช็อตของการตั้งค่าเวลาแบบสัมพัทธ์ในตัวกรองแทน":::
 
## <a name="understanding-anchor-time"></a><span data-ttu-id="d9f50-135">การทำความเข้าใจเวลาจุดยึด</span><span class="sxs-lookup"><span data-stu-id="d9f50-135">Understanding anchor time</span></span>

<span data-ttu-id="d9f50-136">เมื่อใช้งานตัวกรองกับระดับหน้าหรือรายงาน วิชวลทั้งหมดบนหน้าหรือรายงานจะซิงโครไนซ์กับช่วงเวลาที่แน่นอนเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="d9f50-136">When a filter is applied to the page or report level, all visuals on that page or report are synchronized to the same exact time range.</span></span> <span data-ttu-id="d9f50-137">การสอบถามเหล่านี้จะจัดทำให้สัมพันธ์กับเวลาที่เรียกว่า *เวลาจุดยึด*</span><span class="sxs-lookup"><span data-stu-id="d9f50-137">These queries are all issued relative to a time called the *anchor time*.</span></span> <span data-ttu-id="d9f50-138">เวลาจุดยึดจะรีเฟรชโดยอัตโนมัติตามเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d9f50-138">The anchor time automatically refreshes in the following conditions:</span></span>

- <span data-ttu-id="d9f50-139">การโหลดหน้าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d9f50-139">Initial page load.</span></span>
- <span data-ttu-id="d9f50-140">การรีเฟรชด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d9f50-140">Manual refresh.</span></span>
- <span data-ttu-id="d9f50-141">การรีเฟรชหน้าการตรวจหาอัตโนมัติหรือการตรวจหาการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="d9f50-141">Automatic or change detection page refresh.</span></span>
- <span data-ttu-id="d9f50-142">การเปลี่ยนแปลงแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="d9f50-142">A change to the model.</span></span>

### <a name="anchor-time-exceptions"></a><span data-ttu-id="d9f50-143">ข้อยกเว้นเวลาของจุดยึด</span><span class="sxs-lookup"><span data-stu-id="d9f50-143">Anchor time exceptions</span></span>

- <span data-ttu-id="d9f50-144">การกรองเวลาแบบสัมพัทธ์โดยใช้วิชวลการถามตอบจะไม่สัมพันธ์กับเวลาจุดยึดนี้ จนกว่าคุณจะแปลงวิชวลการถามตอบเป็นวิชวลมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="d9f50-144">Relative time filtering using the Q&A visual isn't relative to this anchor time, until you convert the Q&A visual to a standard visual.</span></span> <span data-ttu-id="d9f50-145">อย่างไรก็ตาม วิชวล AI อื่น ๆ เช่น ผู้ทรงอิทธิพลหลักและแผนผังการจำแนกข้อมูลแบบต้นไม้ จะถูกซิงโครไนซ์กับเวลาจุดยึด</span><span class="sxs-lookup"><span data-stu-id="d9f50-145">However, the other AI visuals, such as key influencers and the decomposition tree, are synchronized with the anchor time.</span></span> 
- <span data-ttu-id="d9f50-146">นอกจากนี้ ตัวกรองหรือตัวแบ่งส่วนวันที่แบบสัมพัทธ์จะไม่สัมพันธ์กับเวลาจุดยึด ยกเว้นในกรณที่ปรากฏบนตัวกรองเวลาแบบสัมพัทธ์</span><span class="sxs-lookup"><span data-stu-id="d9f50-146">Additionally, relative date filters or slicers aren't relative to the anchor time, unless in the presence of relative time filters.</span></span> <span data-ttu-id="d9f50-147">หากวันที่สัมพัทธ์และตัวกรองเวลาแบบสัมพัทธ์อยู่ในหน้าเดียวกัน ตัวกรองวันที่แบบสัมพัทธ์จะยึดตามเวลาจุดยึด</span><span class="sxs-lookup"><span data-stu-id="d9f50-147">If a relative date and a relative time filter are on the same page, the relative date filter respects the anchor time.</span></span>

## <a name="limitations-and-considerations"></a><span data-ttu-id="d9f50-148">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="d9f50-148">Limitations and considerations</span></span>

<span data-ttu-id="d9f50-149">ในขณะนี้ ข้อจำกัดและข้อควรพิจารณาดังต่อไปนี้มีผลใช้งานกับตัวแบ่งส่วนและตัวกรองวันที่่แบบสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="d9f50-149">The following limitations and considerations currently apply to the relative time slicer and filter.</span></span>

- <span data-ttu-id="d9f50-150">**ข้อควรพิจารณาเกี่ยวกับโซนเวลา**: แบบจำลองข้อมูลใน Power BI จะไม่รวมข้อมูลโซนเวลา</span><span class="sxs-lookup"><span data-stu-id="d9f50-150">**Time zone considerations**: Data models in Power BI don't include time zone info.</span></span> <span data-ttu-id="d9f50-151">แบบจำลองสามารถจัดเก็บเวลาต่าง ๆ ได้ แต่จะไม่มีการระบุโซนเวลาที่แบบจำลองดังกล่าวอยู่</span><span class="sxs-lookup"><span data-stu-id="d9f50-151">The models can store times, but there's no indication of the time zone they're in.</span></span> <span data-ttu-id="d9f50-152">ตัวแบ่งส่วนข้อมูลและตัวกรองจะยึดตามเวลาใน UTC</span><span class="sxs-lookup"><span data-stu-id="d9f50-152">The slicer and filter are always based on the time in UTC.</span></span> <span data-ttu-id="d9f50-153">หากคุณตั้งค่าตัวกรองในรายงาน และส่งไปยังเพื่อนร่วมงานในโซนเวลาอื่น คุณทั้งสองคนจะเห็นข้อมูลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="d9f50-153">If you set up a filter in a report and send it to a colleague in a different time zone, you both see the same data.</span></span> <span data-ttu-id="d9f50-154">หากคุณและเพื่อร่วมงานไม่ได้อยู่ในโซนเวลามาตรฐานสากล คุณทั้งสองคนต้องคำนึงถึงการเผื่อเวลาที่จะเกิดขึ้นกับคุณ</span><span class="sxs-lookup"><span data-stu-id="d9f50-154">Unless you or your colleague are in the UTC time zone, you both must account for the time offset you’ll experience.</span></span> <span data-ttu-id="d9f50-155">ใช้ตัวแก้ไขการสอบถามเพื่อแปลงข้อมูลที่รวบรวมไว้ในโซนเวลาท้องถิ่นเป็นเวลามาตรฐานสากล</span><span class="sxs-lookup"><span data-stu-id="d9f50-155">Use the Query Editor to convert data captured in a local time zone to UTC.</span></span>
- <span data-ttu-id="d9f50-156">ตัวกรองประเภทใหม่นี้ได้รับการสนับสนุนใน Power BI Desktop บริการของ Power BI, Power BI Embedded และแอป Power BI สำหรับอุปกรณมือถือ</span><span class="sxs-lookup"><span data-stu-id="d9f50-156">This new filter type is supported in Power BI Desktop, the Power BI service, Power BI Embedded, and the Power BI mobile apps.</span></span> <span data-ttu-id="d9f50-157">อย่างไรก็ตาม ไม่สนับสนุนการเผยแพร่ไปยังเว็บ</span><span class="sxs-lookup"><span data-stu-id="d9f50-157">However, it isn't supported for Publish to web.</span></span>

- <span data-ttu-id="d9f50-158">**การแคชคิวรี**: เราใช้แคชไคลเอ็นต์</span><span class="sxs-lookup"><span data-stu-id="d9f50-158">**Query caching**: We use the client cache.</span></span> <span data-ttu-id="d9f50-159">สมมติว่าคุณระบุ "1 นาทีที่ผ่านมา" แล้วระบุ "5 นาทีที่ผ่านมา" จากนั้นกลับไปที่ "1 นาทีที่ผ่านมา"</span><span class="sxs-lookup"><span data-stu-id="d9f50-159">Say you specify "last 1 minute," then "last 5 minutes," then back to "last 1 minute."</span></span> <span data-ttu-id="d9f50-160">ที่จุดนั้น คุณจะเห็นผลลัพธ์เดียวกันกับการเรียกใช้ครั้งแรก ยกเว้นในกรณีที่คุณรีเฟรชหน้าหรือหน้านั้นรีเฟรชโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d9f50-160">At that point, you see the same results as when it was first run, unless you refresh the page or the page automatically refreshes.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d9f50-161">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d9f50-161">Next steps</span></span>

- [<span data-ttu-id="d9f50-162">ใช้ตัวแบ่งส่วนและตัวกรองวันที่แบบสัมพัทธ์ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="d9f50-162">Use a relative date slicer and filter in Power BI</span></span>](../visuals/desktop-slicer-filter-date-range.md)
- [<span data-ttu-id="d9f50-163">ตัวแบ่งส่วนข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="d9f50-163">Slicers in Power BI</span></span>](../visuals/power-bi-visualization-slicers.md)
