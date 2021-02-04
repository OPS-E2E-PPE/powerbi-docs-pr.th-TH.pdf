---
title: สร้างตัวแบ่งส่วนข้อมูล คุณสามารถปรับขนาดใน Power BI ได้
description: เรียนรู้วิธีการสร้างตัวแบ่งส่วนข้อมูลแบบตอบสนองที่คุณสามารถปรับขนาดเพื่อให้เหมาะกับรายงานของคุณ
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 04/06/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 5fde91f2cfabd1f5a7727d3ec8a80d8ecddc7fc6
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96393450"
---
# <a name="create-a-responsive-slicer-you-can-resize-in-power-bi"></a><span data-ttu-id="d50d0-103">สร้างตัวแบ่งส่วนข้อมูล คุณสามารถปรับขนาดใน Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="d50d0-103">Create a responsive slicer you can resize in Power BI</span></span>

<span data-ttu-id="d50d0-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-desktop](../includes/yes-desktop.md)] [!INCLUDE [yes-service](../includes/yes-service.md)]</span><span class="sxs-lookup"><span data-stu-id="d50d0-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-desktop](../includes/yes-desktop.md)] [!INCLUDE [yes-service](../includes/yes-service.md)]</span></span>

<span data-ttu-id="d50d0-105">ตัวแบ่งส่วนข้อมูลแบบตอบสนองปรับขนาดให้พอดีกับพื้นที่บนรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="d50d0-105">Responsive slicers resize to fit any space on your report.</span></span> <span data-ttu-id="d50d0-106">ตัวแบ่งส่วนข้อมูลแบบตอบสนอง คุณสามารถปรับขนาดให้มีหลายรูปร่างและขนาดที่แตกต่างกัน จากแนวนอนเป็นแนวตั้ง และค่าในตัวแบ่งส่วนข้อมูลได้จัดเรียงใหม่ด้วยตนเองเหมือนที่คุณทำอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="d50d0-106">With responsive slicers, you can resize them to different sizes and shapes, from horizontal to square to vertical, and the values in the slicer rearrange themselves as you do.</span></span> <span data-ttu-id="d50d0-107">ใน Power BI Desktop และใน Power BI service คุณสามารถสร้างให้ตัวแบ่งส่วนข้อมูลแนวนอน และตัวแบ่งส่วนข้อมูลแบบตอบสนองตามวัน/ช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="d50d0-107">In Power BI Desktop and in the Power BI service, you can make horizontal slicers and date/range slicers responsive.</span></span> <span data-ttu-id="d50d0-108">ตัวแบ่งส่วนข้อมูลตามวัน/ช่วงเวลา ยังได้ปรับปรุงพื้นที่สัมผัส ซึ่งง่ายต่อการเปลี่ยนแปลงด้วยปลายนิ้ว</span><span class="sxs-lookup"><span data-stu-id="d50d0-108">Date/range slicers also have improved touch areas so it's easier to change them with a fingertip.</span></span> <span data-ttu-id="d50d0-109">คุณสามารถทำให้ตัวแบ่งส่วนข้อมูลแบบตอบสนองเป็นขนาดเล็กหรือใหญ่ตามที่คุณต้อง แล้วพวกมันยังปรับขนาดโดยอัตโนมัติให้พอดีกับรายงาน ใน Power BI service และในแอป mobile Power BI</span><span class="sxs-lookup"><span data-stu-id="d50d0-109">You can make responsive slicers as small or as large as you want; they also resize automatically to fit well on reports in the Power BI service and also in the Power BI mobile apps.</span></span> 

![ตัวแบ่งส่วนข้อมูลแบบตอบสนองสามารถมีหลายรูปร่าง](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-0-slicer.gif)

## <a name="create-a-slicer"></a><span data-ttu-id="d50d0-111">สร้างตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d50d0-111">Create a slicer</span></span>

<span data-ttu-id="d50d0-112">ขั้นตอนแรกในการสร้างตัวแบ่งส่วนข้อมูลแบบไดนามิกคือสร้างตัวแบ่งส่วนข้อมูลพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="d50d0-112">The first step to creating a dynamic slicer is to create a basic slicer.</span></span> 

1. <span data-ttu-id="d50d0-113">เลือกไอคอน **ตัวแบ่งส่วนข้อมูล**![ไอคอนตัวแบ่งส่วนข้อมูล](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-0-slicer-icon.png)ในบานหน้าต่าง **แสดงภาพ**</span><span class="sxs-lookup"><span data-stu-id="d50d0-113">Select the **Slicer** icon ![Slicer icon](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-0-slicer-icon.png) in the **Visualizations** pane.</span></span>
2. <span data-ttu-id="d50d0-114">ลากเขตข้อมูลที่คุณต้องการไปยังตัวกรองบน **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="d50d0-114">Drag the field you want to filter on to **Field**.</span></span>

    ![เพิ่มเขตข้อมูลลงในตัวแบ่งส่วนข้อมูล](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-1-create.png)

## <a name="convert-to-a-horizontal-slicer"></a><span data-ttu-id="d50d0-116">แปลงเป็นตัวแบ่งส่วนข้อมูลแนวนอน</span><span class="sxs-lookup"><span data-stu-id="d50d0-116">Convert to a horizontal slicer</span></span>

1. <span data-ttu-id="d50d0-117">ด้วยตัวแบ่งส่วนข้อมูลที่เลือกไว้ ในบานหน้าต่าง **แสดงภาพ** ให้เลือกแท็บ **รูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="d50d0-117">With the slicer selected, in the **Visualizations** pane select the **Format** tab.</span></span>
2. <span data-ttu-id="d50d0-118">ขยายส่วน **ทั่วไป** แล้วสำหรับ **วางแนว** ให้เลือก **แนวนอน**</span><span class="sxs-lookup"><span data-stu-id="d50d0-118">Expand the **General** section, then for **Orientation**, select **Horizontal**.</span></span>

    ![ตั้งค่าตัวแบ่งส่วนข้อมูลเป็นแนวนอน](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-2-horizontal.png) 

1.  <span data-ttu-id="d50d0-120">คุณอาจจะต้องการทำให้กว้างขึ้น เพื่อแสดงค่าเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d50d0-120">You'll probably want to make it wider, to show more values.</span></span>

     ![ทำให้ตัวแบ่งส่วนข้อมูลที่กว้างขึ้น](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-3-wider.png)

## <a name="make-it-responsive-and-experiment-with-it"></a><span data-ttu-id="d50d0-122">ทำให้เป็นแบบตอบสนอง และทดลองใช้มัน</span><span class="sxs-lookup"><span data-stu-id="d50d0-122">Make it responsive and experiment with it</span></span>

<span data-ttu-id="d50d0-123">ขั้นตอนนี้เป็นเรื่องง่าย</span><span class="sxs-lookup"><span data-stu-id="d50d0-123">This step is easy.</span></span> 

1. <span data-ttu-id="d50d0-124">ที่ใต้ **การจัดแนว** ในส่วน **ทั่วไป** ของแท็บ **รูปแบบ** สไลด์ค่า **ตอบสนอง** ไปยัง **เปิด**</span><span class="sxs-lookup"><span data-stu-id="d50d0-124">Right under **Orientation** in the **General** section of the **Format** tab, slide **Responsive** to **On**.</span></span>  

    ![ตอนนี้ตัวแบ่งส่วนข้อมูลเป็นแบบตอบสนอง](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-4-responsive-on.png)

1. <span data-ttu-id="d50d0-126">ในตอนนี้ คุณสามารถเล่นกับมัน</span><span class="sxs-lookup"><span data-stu-id="d50d0-126">Now you can play with it.</span></span> <span data-ttu-id="d50d0-127">ลากตรงมุมเพื่อทำให้สั้น สูง ความกว้างและแคบ</span><span class="sxs-lookup"><span data-stu-id="d50d0-127">Drag the corners to make it short, tall, wide, and narrow.</span></span> <span data-ttu-id="d50d0-128">ถ้าคุณปรับให้มีขนาดเล็กพอ จะกลายเป็นเพียงไอคอนตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="d50d0-128">If you make it small enough, it becomes just a filter icon.</span></span>

    ![ตัวแบ่งส่วนข้อมูลแบบตอบสนองที่เล็กมาก เป็นไอคอนตัวกรอง](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-5-mini-icon.png)

## <a name="add-it-to-a-phone-report-layout"></a><span data-ttu-id="d50d0-130">เพิ่มลงในเค้าโครงรายงานโทรศัพท์</span><span class="sxs-lookup"><span data-stu-id="d50d0-130">Add it to a phone report layout</span></span>

<span data-ttu-id="d50d0-131">ใน Power BI Desktop คุณสามารถสร้างเค้าโครงโทรศัพท์สำหรับแต่ละหน้าของรายงาน</span><span class="sxs-lookup"><span data-stu-id="d50d0-131">In Power BI Desktop, you can create a phone layout for each page of a report.</span></span> <span data-ttu-id="d50d0-132">ถ้าหน้ามีเค้าโครงโทรศัพท์ จะแสดงบนโทรศัพท์มือถือในมุมมองแนวตั้ง</span><span class="sxs-lookup"><span data-stu-id="d50d0-132">If a page has a phone layout, it displays on a mobile phone in portrait view.</span></span> <span data-ttu-id="d50d0-133">ไม่เช่นนั้น คุณจำเป็นต้องดูในมุมมองแนวนอน</span><span class="sxs-lookup"><span data-stu-id="d50d0-133">Otherwise, you need to view it in landscape view.</span></span> 

1. <span data-ttu-id="d50d0-134">ที่เมนู **มุมมอง** ให้เลือก **เค้าโครงโทรศัพท์**</span><span class="sxs-lookup"><span data-stu-id="d50d0-134">On the **View** menu, select **Phone Layout**.</span></span>

     ![ไอคอนเค้าโครงโทรศัพท์ เมนูมุมมอง](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-6-phone-layout-button.png)
    
1. <span data-ttu-id="d50d0-136">ลากภาพทั้งหมดที่คุณต้องการในรายงานโทรศัพท์ลงในตาราง</span><span class="sxs-lookup"><span data-stu-id="d50d0-136">Drag all the visuals you want in the phone report to the grid.</span></span> <span data-ttu-id="d50d0-137">เมื่อคุณลากตัวแบ่งส่วนข้อมูลแบบตอบสนอง มันทำให้ได้ขนาดที่คุณต้องการ ในกรณีนี้ เป็นเพียงไอคอนตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="d50d0-137">When you drag the responsive slicer, make it the size you want -- in this case, just a filter icon.</span></span>

    ![เพิ่มตัวแบ่งส่วนข้อมูลไปยังเค้าโครงรายงานโทรศัพท์](media/power-bi-slicer-filter-responsive/power-bi-slicer-filter-responsive-7-phone-slicer-icon.png)

<span data-ttu-id="d50d0-139">อ่านเพิ่มเติมเกี่ยวกับการสร้าง[รายงานที่ปรับให้เหมาะสมสำหรับแอปอุปกรณ์เคลื่อนที่ Power BI](desktop-create-phone-report.md)</span><span class="sxs-lookup"><span data-stu-id="d50d0-139">Read more about creating [reports optimized for the Power BI mobile apps](desktop-create-phone-report.md).</span></span>

## <a name="make-a-time-or-range-slicer-responsive"></a><span data-ttu-id="d50d0-140">สร้างตัวแบ่งส่วนข้อมูลแบบตอบสนองต่แเวลาหรือช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="d50d0-140">Make a time or range slicer responsive</span></span>

<span data-ttu-id="d50d0-141">คุณสามารถทำตามขั้นตอนเดียวกันเพื่อสร้างตัวแบ่งส่วนข้อมูลแบบตอบสนองต่อเวลาหรือช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="d50d0-141">You can follow the same steps to make a time or range slicer responsive.</span></span> <span data-ttu-id="d50d0-142">หลังจากที่คุณตั้งค่า **การตอบสนอง** เป็น **เปิด** คุณจะสังเกตเห็นบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="d50d0-142">After you set **Responsive** to **On**, you notice a few things:</span></span>

- <span data-ttu-id="d50d0-143">ภาพได้ปรับลำดับของกล่องป้อนข้อมูลให้เหมาะสมโดยขึ้นอยู่กับขนาดที่อนุญาตให้ใช้บนพื้นที่</span><span class="sxs-lookup"><span data-stu-id="d50d0-143">Visuals optimize the order of input boxes depending on the size allowed on the canvas.</span></span> 
- <span data-ttu-id="d50d0-144">แสดงองค์ประกอบข้อมูลที่ถูกปรับให้เหมาะสม เพื่อทำให้ตัวแบ่งส่วนข้อมูลใช้งานได้มากที่สุด ขึ้นอยู่กับขนาดที่อนุญาตบนพื้นที่</span><span class="sxs-lookup"><span data-stu-id="d50d0-144">Data-element display is optimized to make the slicer as usable as possible, based on the size it's allowed on the canvas.</span></span> 
- <span data-ttu-id="d50d0-145">แถบที่จับทรงกลมใหม่บนแถบเลื่อนที่ปรับการโต้ตอบแบบสัมผัสให้เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="d50d0-145">New round handlebars on the sliders optimize touch interactions.</span></span> 
- <span data-ttu-id="d50d0-146">เมื่อรูปภาพเปลี่ยนขนาดจนเล็กเกินไปที่จะเป็นประโยชน์ จะกลายเป็นไอคอนที่แสดงชนิดภาพแทน</span><span class="sxs-lookup"><span data-stu-id="d50d0-146">When a visual becomes too small to be useful, it becomes an icon representing the visual type in its place.</span></span> <span data-ttu-id="d50d0-147">เพื่อใช้งาน ก็แค่แตะครั้งสองครั้งเพื่อเปิดในโหมดโฟกัส</span><span class="sxs-lookup"><span data-stu-id="d50d0-147">To interact with it, just double-tap to open it in focus mode.</span></span> <span data-ttu-id="d50d0-148">ซึ่งช่วยประหยัดเนื้อที่อันมีค่าบนหน้ารายงานโดยไม่สูญเสียความสามารถการทำงาน</span><span class="sxs-lookup"><span data-stu-id="d50d0-148">This saves valuable space on the report page without losing the functionality.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d50d0-149">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d50d0-149">Next steps</span></span>

- [<span data-ttu-id="d50d0-150">ตัวแบ่งส่วนข้อมูลในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="d50d0-150">Slicers in the Power BI service</span></span>](../visuals/power-bi-visualization-slicers.md)
- <span data-ttu-id="d50d0-151">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d50d0-151">More questions?</span></span> [<span data-ttu-id="d50d0-152">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="d50d0-152">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)