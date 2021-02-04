---
title: ใช้ตัวแบ่งส่วนข้อมูลหรือตัวกรองวันที่แบบสัมพัทธ์ใน Power BI
description: เรียนรู้วิธีการใช้ตัวแบ่งส่วนข้อมูลหรือตัวกรองเพื่อจำกัดช่วงวันที่ที่สัมพันธ์ใน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: rien
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 09/09/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 8d83a2b655c7a4dd788e34ce5744daaac0f73f63
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96397472"
---
# <a name="creating-a-relative-date-slicer-and-filter-in-power-bi"></a><span data-ttu-id="a333d-103">การสร้างตัวแบ่งส่วนและตัวกรองวันที่แบบสัมพัทธ์ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="a333d-103">Creating a relative date slicer and filter in Power BI</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]

<span data-ttu-id="a333d-104">ด้วย **ตัวแบ่งส่วนข้อมูลวันที่ที่สัมพันธ์** หรือ **ตัวกรองวันที่ี่ที่สัมพันธ์** คุณสามารถใช้ตัวกรองที่ยึดตามเวลากับคอลัมน์วันที่ใดก็ตามในแบบจำลองข้อมูลของคุณได้</span><span class="sxs-lookup"><span data-stu-id="a333d-104">With the **relative date slicer** or **relative date filter**, you can apply time-based filters to any date column in your data model.</span></span> <span data-ttu-id="a333d-105">ตัวอย่างเช่น คุณสามารถใช้ **ตัวแบ่งส่วนข้อมูลวันที่ที่เกี่ยวข้อง** เพื่อแสดงข้อมูลยอดขายเฉพาะที่เกิดขึ้นภายใน 30 วันที่ผ่านมา (หรือ เดือน, เดือนตามปฏิทิน ฯลฯ) ได้</span><span class="sxs-lookup"><span data-stu-id="a333d-105">For example, you can use the **relative date slicer** to show only sales data that's happened within the last 30 days (or month, calendar months, and so on).</span></span> <span data-ttu-id="a333d-106">เมื่อคุณรีเฟรชข้อมูล ช่วงเวลาสัมพัทธ์จะถูกปรับให้ใช้วันที่ที่เหมาะสมโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a333d-106">When you refresh the data, the relative time period automatically applies the appropriate relative date constraint.</span></span>

![ภาพหน้าจอของรายงานที่มีลูกศรชี้ไปยังตัวแบ่งส่วนวันที่แบบสัมพันธ์กัน](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-01.png)

<span data-ttu-id="a333d-108">หากต้องการแชร์รายงานของคุณกับผู้ร่วมงาน Power BI คุณจะต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="a333d-108">To share your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span>

## <a name="create-the-relative-date-range-slicer"></a><span data-ttu-id="a333d-109">ใช้ตัวแบ่งส่วนช่วงวันที่แบบสัมพัทธ์</span><span class="sxs-lookup"><span data-stu-id="a333d-109">Create the relative date range slicer</span></span>

<span data-ttu-id="a333d-110">คุณสามารถใช้ตัวแบ่งส่วนข้อมูลวันที่ที่สัมพันธ์ได้เช่นเดียวกับตัวแบ่งส่วนข้อมูลอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="a333d-110">You can use the relative date slicer just like any other slicer.</span></span> <span data-ttu-id="a333d-111">สร้างวิชวล **ตัวแบ่งส่วนข้อมูล** สำหรับรายงานของคุณ จากนั้นเลือกค่าวันที่สำหรับค่า **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="a333d-111">Create a **slicer** visual for your report and then select a date value for the **Field** value.</span></span> <span data-ttu-id="a333d-112">ในรูปต่อไปนี้ เราได้เลือกเขตข้อมูล *OrderDate*</span><span class="sxs-lookup"><span data-stu-id="a333d-112">In the following image, we selected the *OrderDate* field.</span></span>

![สกรีนช็อตของบานหน้าต่างการแสดงภาพที่มีลูกศรชี้ไปที่ไอคอนวิชวลตัวแบ่งส่วนข้อมูลและเขตข้อมูลด้วย](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-02.png)

<span data-ttu-id="a333d-114">เลือกตัวแบ่งส่วนข้อมูลบนพื้นที่ทำงานของคุณ และกะรัตที่มุมบนด้านขวาของวิชวลตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a333d-114">Select the slicer on your canvas and then the carat in the upper-right corner of the slicer visual.</span></span> <span data-ttu-id="a333d-115">หากวิชวลนี้มีข้อมูลวันที่ เมนูจะแสดงตัวเลือกสำหรับ **สัมพัทธ์**</span><span class="sxs-lookup"><span data-stu-id="a333d-115">If the visual has date data, the menu displays the option for **Relative**.</span></span>

![สกรีนช็อตของวิชวลตัวแบ่งส่วนข้อมูลที่มีการเรียกออกไปรอบ ๆ กะรัตและลูกศรชี้ไปที่สัมพัทธ์](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-03.png)

<span data-ttu-id="a333d-117">ตัวแบ่งส่วนข้อมูลวันที่ที่สัมพันธ์ เลือก *สัมพันธ์*</span><span class="sxs-lookup"><span data-stu-id="a333d-117">For the relative date slicer, select *Relative*.</span></span>

<span data-ttu-id="a333d-118">จากนั้นคุณสามารถเลือกการตั้งค่าดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="a333d-118">You can then select the settings.</span></span>

<span data-ttu-id="a333d-119">สำหรับการตั้งค่าครั้งแรกใน *ตัวแบ่งส่วนข้อมูลวันที่ที่สัมพัทธ์* คุณมีตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a333d-119">For the first setting in the *relative date slicer*, you have the following choices:</span></span>

![สกรีนช็อตของตัวเลือกการกำหนดค่าที่สัมพัทธ์กับการตั้งค่าครั้งแรกที่เรียกออก](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-04.png)

* <span data-ttu-id="a333d-121">สุดท้าย</span><span class="sxs-lookup"><span data-stu-id="a333d-121">Last</span></span>
* <span data-ttu-id="a333d-122">ถัดไป</span><span class="sxs-lookup"><span data-stu-id="a333d-122">Next</span></span>
* <span data-ttu-id="a333d-123">นี้</span><span class="sxs-lookup"><span data-stu-id="a333d-123">This</span></span>

<span data-ttu-id="a333d-124">การตั้งค่าครั้งที่สอง (ตรงกลาง) ใน *ตัวแบ่งส่วนข้อมูลวันที่ที่สัมพัทธ์* ให้คุณสามารถระบุตัวเลขเพื่อกำหนดช่วงวันที่สัมพัทธ์ได้</span><span class="sxs-lookup"><span data-stu-id="a333d-124">The second (middle) setting in the *relative date slicer* lets you enter a number to define the relative date range.</span></span>

![สกรีนช็อตของตัวเลือกการกำหนดค่าที่สัมพัทธ์กับการตั้งค่าครั้งที่สองที่เรียกออก](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-04a.png)

<span data-ttu-id="a333d-126">การตั้งค่าที่สาม ให้คุณเลือกหน่วยวัดวันที่</span><span class="sxs-lookup"><span data-stu-id="a333d-126">The third setting lets you pick the date measurement.</span></span> <span data-ttu-id="a333d-127">คุณมีตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a333d-127">You have the following choices:</span></span>

![สกรีนช็อตของตัวเลือกการกำหนดค่าที่สัมพัทธ์กับการตั้งค่าครั้งที่สามที่เรียกออก](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-05.png)

* <span data-ttu-id="a333d-129">วัน</span><span class="sxs-lookup"><span data-stu-id="a333d-129">Days</span></span>
* <span data-ttu-id="a333d-130">สัปดาห์</span><span class="sxs-lookup"><span data-stu-id="a333d-130">Weeks</span></span>
* <span data-ttu-id="a333d-131">สัปดาห์ (ปฏิทิน)</span><span class="sxs-lookup"><span data-stu-id="a333d-131">Weeks (Calendar)</span></span>
* <span data-ttu-id="a333d-132">เดือน</span><span class="sxs-lookup"><span data-stu-id="a333d-132">Months</span></span>
* <span data-ttu-id="a333d-133">เดือน (ปฏิทิน)</span><span class="sxs-lookup"><span data-stu-id="a333d-133">Months (Calendar)</span></span>
* <span data-ttu-id="a333d-134">ปี</span><span class="sxs-lookup"><span data-stu-id="a333d-134">Years</span></span>
* <span data-ttu-id="a333d-135">ปี (ปฏิทิน)</span><span class="sxs-lookup"><span data-stu-id="a333d-135">Years (Calendar)</span></span>

<span data-ttu-id="a333d-136">หากคุณเลือก **เดือน** จากรายการ และป้อนตัวเลข *2* ในการตั้งค่าตรงกลาง นี่คือสิ่งที่จะเกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="a333d-136">If you select **Months** from that list, and enter *2* in the middle setting, here's what happens:</span></span>

* <span data-ttu-id="a333d-137">ถ้าวันนี้คือวันที่ 20 กรกฎาคม:</span><span class="sxs-lookup"><span data-stu-id="a333d-137">If today is July 20:</span></span>

    - <span data-ttu-id="a333d-138">ข้อมูลที่รวมอยู่ในวิชวลที่จำกัดโดยตัวแบ่งส่วนข้อมูลจะแสดงข้อมูลสองเดือนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="a333d-138">The data included in visuals constrained by the slicer will show data for the previous two months,</span></span>
    - <span data-ttu-id="a333d-139">เริ่มจากวันที่ 21 พฤษภาคมและไปจนถึงวันที่ 20 กรกฎาคม (วันที่ของวันนี้)</span><span class="sxs-lookup"><span data-stu-id="a333d-139">Starting on May 21 and going through July 20 (today's date).</span></span>

<span data-ttu-id="a333d-140">ในการเปรียบเทียบ ถ้าคุณเลือก *เดือน (ปฏิทิน)* วิชวลที่จำกัดจะแสดงข้อมูลจากวันที่ 1 พฤษภาคมถึงวันที่ 30 มิถุนายน (สองเดือนเต็มตามเดือนในปฏิทิน)</span><span class="sxs-lookup"><span data-stu-id="a333d-140">In comparison, if you selected *Months (Calendar)*, the visuals constrained would show data from May 1 through June 30 (the last two complete calendar months).</span></span>

## <a name="create-the-relative-date-range-filter"></a><span data-ttu-id="a333d-141">สร้างตัวกรองข้อมูลช่วงวันที่แบบสัมพัทธ์</span><span class="sxs-lookup"><span data-stu-id="a333d-141">Create the relative date range filter</span></span>

<span data-ttu-id="a333d-142">คุณยังสามารถสร้างตัวกรองช่วงวันที่สัมพัทธ์สำหรับหน้ารายงานของคุณ หรือทั้งรายงานของคุณได้</span><span class="sxs-lookup"><span data-stu-id="a333d-142">You can also create a relative date range filter for your report page or your entire report.</span></span> <span data-ttu-id="a333d-143">ในการทำเช่นนั้น ให้่ลากเขตข้อมูลวันที่ไปยังแหล่งข้อมูล **ตัวกรองระดับหน้า** หรือแหล่งข้อมูล **ตัวกรองระดับรายงาน** ในบานหน้าต่าง **เขตข้อมูล**:</span><span class="sxs-lookup"><span data-stu-id="a333d-143">To do so, drag a date field into the **Page level filters** well or the **Report level filters** well in the **Field** pane:</span></span>

![สกรีนช็อตของเขตข้อมูล OrderDate ที่ถูกลากไปยังแหล่งข้อมูลตัวกรองระดับหน้า](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-06.png)

<span data-ttu-id="a333d-145">เมื่อมี คุณสามารถเปลี่ยนช่วงวันที่ที่สัมพัทธ์</span><span class="sxs-lookup"><span data-stu-id="a333d-145">Once there, you can change the relative date range.</span></span> <span data-ttu-id="a333d-146">ซึ่งคล้ายกับวิธีการที่คุณสามารถกำหนด **ตัวแบ่งส่วนข้อมูลวันที่ที่สัมพันธ์** เอง</span><span class="sxs-lookup"><span data-stu-id="a333d-146">It's similar to how you can customize the **relative date slicer**.</span></span> <span data-ttu-id="a333d-147">เลือก **กรองข้อมูลวันที่ที่สัมพันธ์** จากดรอปดาวน์ **ชนิดตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="a333d-147">Select **Relative date filtering** from the **Filter Type** drop-down.</span></span>

![สกรีนช็อตที่แสดงรายการดรอปดาวน์ของชนิดตัวกรองและตัวชี้เมาส์บนการกรองข้อมูลวันที่ที่สัมพัทธ์](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-07.png)

<span data-ttu-id="a333d-149">เมื่อคุณเลือก **การกรองข้อมูลวันที่ที่สัมพัทธ์** แล้ว คุณจะเห็นสามส่วนที่จะเปลี่ยน ซึ่งรวมถึงกล่องตัวเลขตรงกลาง เช่นเดียวกับตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a333d-149">Once you've selected **Relative date filtering**, you see three sections to change, including a middle numeric box, just like the slicer.</span></span>

![สกรีนช็อตของตัวกรองระดับรายงานมีลูกศรชี้ไปที่แสดงรายการเมื่อมีตัวเลือกค่า](media/desktop-slicer-filter-date-range/relative-date-range-slicer-filter-08.png)

## <a name="limitations-and-considerations"></a><span data-ttu-id="a333d-151">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="a333d-151">Limitations and considerations</span></span>

<span data-ttu-id="a333d-152">ในขณะนี้ ข้อจำกัดและข้อควรพิจารณาดังต่อไปนี้นำไปใช้กับ **ตัวแบ่งส่วนข้อมูลช่วงวันที่ที่สัมพันธ์** และตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="a333d-152">The following limitations and considerations currently apply to the **relative date range slicer** and filter.</span></span>

* <span data-ttu-id="a333d-153">ชนิดข้อมูลสำหรับเขตข้อมูลในตัวแบ่งส่วนข้อมูลจะต้องเป็นค่าวันที่ และไม่ตั้งค่าเริ่มต้นไว้เป็นข้อความ</span><span class="sxs-lookup"><span data-stu-id="a333d-153">The data type for the field in the slicer must be a date, and not the default of text.</span></span> <span data-ttu-id="a333d-154">มิฉะนั้น ตัวเลือกที่เกี่ยวข้องจะไม่แสดงขึ้นมาในตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a333d-154">Otherwise, the relative options don't show up in the slicer.</span></span>
* <span data-ttu-id="a333d-155">แบบจำลองข้อมูลใน **Power BI** จะไม่รวมข้อมูลโซนเวลา</span><span class="sxs-lookup"><span data-stu-id="a333d-155">Data models in **Power BI** don't include time zone info.</span></span> <span data-ttu-id="a333d-156">แบบจำลองสามารถจัดเก็บเวลาต่าง ๆ ได้ แต่จะไม่มีการระบุโซนเวลาที่แบบจำลองดังกล่าวอยู่</span><span class="sxs-lookup"><span data-stu-id="a333d-156">The models can store times, but there's no indication of the time zone they're in.</span></span>
* <span data-ttu-id="a333d-157">ตัวแบ่งส่วนข้อมูลและตัวกรองจะยึดตามเวลาใน UTC</span><span class="sxs-lookup"><span data-stu-id="a333d-157">The slicer and filter are always based on the time in UTC.</span></span> <span data-ttu-id="a333d-158">หากคุณตั้งค่าตัวกรองในรายงาน และส่งไปยังเพื่อนร่วมงานในโซนเวลาอื่น คุณทั้งสองคนจะเห็นข้อมูลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="a333d-158">If you set up a filter in a report and send it to a colleague in a different time zone, you both see the same data.</span></span> <span data-ttu-id="a333d-159">หากคุณไม่ได้อยู่ในโซนเวลามาตรฐานสากล คุณและเพื่อนร่วมงานของคุณต้องคำนึงถึงการเผื่อเวลาทจะเกิดขึ้นกับคุณ</span><span class="sxs-lookup"><span data-stu-id="a333d-159">Unless you are in the UTC time zone, you and your colleague must account for the time offset you experience.</span></span>
* <span data-ttu-id="a333d-160">คุณสามารถแปลงข้อมูลที่รวบรวมไว้ในโซนเวลาท้องถิ่นเป็น UTC ได้โดยใช้ **ตัวแก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="a333d-160">You can convert data captured in a local time zone to UTC using the **Query Editor**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a333d-161">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a333d-161">Next steps</span></span>

- [<span data-ttu-id="a333d-162">ใช้ตัวแบ่งส่วนและตัวกรองเวลาแบบสัมพัทธ์ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="a333d-162">Use a relative time slicer and filter in Power BI</span></span>](../create-reports/slicer-filter-relative-time.md)
- [<span data-ttu-id="a333d-163">ตัวแบ่งส่วนข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="a333d-163">Slicers in Power BI</span></span>](power-bi-visualization-slicers.md)
