---
title: แก้ไขไทล์แดชบอร์ด
description: บทเรียนนี้นำพาคุณจากการสร้างไทล์ และปักหมุดไปยังแดชบอร์ด เพื่อเรียนรู้วิธีการแก้ไขแดชบอร์ดไทล์ปรับขนาด ย้าย เปลี่ยนชื่อ ปักหมุด ลบ เพิ่มไฮเปอร์ลิงก์
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: lJKgWnvl6bQ
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 03/02/2018
LocalizationGroup: Dashboards
ms.openlocfilehash: 4e217b0e75e8d2fadd2eff927ba3ef3c04e40e27
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96417439"
---
# <a name="edit-or-remove-a-dashboard-tile"></a><span data-ttu-id="ebd39-103">แก้ไขหรือลบแดชบอร์ดไทล์</span><span class="sxs-lookup"><span data-stu-id="ebd39-103">Edit or remove a dashboard tile</span></span>

## <a name="dashboard-owners-versus-dashboard-consumers"></a><span data-ttu-id="ebd39-104">*เจ้าของ* แดชบอร์ดเทียบกับ *ผู้บริใช้* แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="ebd39-104">Dashboard *owners* versus dashboard *consumers*</span></span>
<span data-ttu-id="ebd39-105">เมื่อคุณสร้าง หรือเป็นเจ้าของแดชบอร์ด คุณมีตัวเลือกมากมายสำหรับการเปลี่ยนแปลงการลักษณะและพฤติกรรมของไทล์บนแดชบอร์ดนั้น</span><span class="sxs-lookup"><span data-stu-id="ebd39-105">When you create or own a dashboard, you have many options for changing the look and default behavior of the tiles on that dashboard.</span></span> <span data-ttu-id="ebd39-106">ใช้การตั้งค่าและกลยุทธ์ด้านล่างเมื่อต้องการออกแบบแดชบอร์ด *โดยใช้* ประสบการณ์การใช้งานของผู้ร่วมงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="ebd39-106">Use the settings and strategies below to design the dashboard *consuming* experience for your colleagues.</span></span>  <span data-ttu-id="ebd39-107">จะเลือกไทล์เปิดรายงานที่สำคัญ URL ที่กำหนดเอง หรือแดชบอร์ดต่างๆ ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="ebd39-107">Will selecting a tile open the underlying report, a custom URL, or a different dashboard?</span></span> <span data-ttu-id="ebd39-108">อาจคุณจะ[เพิ่มไทล์ที่แสดงวิดีโอ หรือข้อมูลการสตรีม](service-dashboard-add-widget.md)หรือไม่</span><span class="sxs-lookup"><span data-stu-id="ebd39-108">Maybe you'll [add a tile that displays a video or streaming data](service-dashboard-add-widget.md)?</span></span> <span data-ttu-id="ebd39-109">และแม้คุณอาจต้องการ[สร้างไทล์ที่มีตัวแบ่งส่วนข้อมูลแบบโต้ตอบ](service-dashboard-pin-live-tile-from-report.md)</span><span class="sxs-lookup"><span data-stu-id="ebd39-109">And you might even want to [create a tile that has interactive slicers](service-dashboard-pin-live-tile-from-report.md).</span></span> <span data-ttu-id="ebd39-110">ในฐานะ *ผู้สร้าง* คุณมีตัวเลือกมากมาย</span><span class="sxs-lookup"><span data-stu-id="ebd39-110">As a *creator* you have many options.</span></span> 

<iframe width="560" height="315" src="https://www.youtube.com/embed/lJKgWnvl6bQ" frameborder="0" allowfullscreen></iframe>

<span data-ttu-id="ebd39-111">บทความนี้ครอบคลุมเรื่องต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ebd39-111">This article covers the following.</span></span>

* [<span data-ttu-id="ebd39-112">สร้างภาพและปักหมุดกับแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="ebd39-112">Create a visualization and pin it to a dashboard</span></span>](#create)
* [<span data-ttu-id="ebd39-113">ย้ายไทล์</span><span class="sxs-lookup"><span data-stu-id="ebd39-113">Move a tile</span></span>](#move)
* [<span data-ttu-id="ebd39-114">ปรับขนาดไทล์</span><span class="sxs-lookup"><span data-stu-id="ebd39-114">Resize a tile</span></span>](#resize)
* [<span data-ttu-id="ebd39-115">เปลี่ยนชื่อไทล์</span><span class="sxs-lookup"><span data-stu-id="ebd39-115">Rename a tile</span></span>](#rename)
* [<span data-ttu-id="ebd39-116">เพิ่มไฮเปอร์ลิงก์ให้ไทล์</span><span class="sxs-lookup"><span data-stu-id="ebd39-116">Add a hyperlink to a tile</span></span>](#hyperlink)
* [<span data-ttu-id="ebd39-117">ปักหมุดไทล์ให้แดชบอร์ดต่างๆ</span><span class="sxs-lookup"><span data-stu-id="ebd39-117">Pin a tile to a different dashboard</span></span>](#different)
* [<span data-ttu-id="ebd39-118">ลบไทล์</span><span class="sxs-lookup"><span data-stu-id="ebd39-118">Delete a tile</span></span>](#delete)
  
  > [!TIP]
  > <span data-ttu-id="ebd39-119">เมื่อต้องเปลี่ยนการแสดงภาพที่แสดงบนไทล์เอง ลบไทล์ และเพิ่ม[แดชบอร์ดไทล์](../consumer/end-user-tiles.md)ใหม่</span><span class="sxs-lookup"><span data-stu-id="ebd39-119">To change the visualization shown on the tile itself, delete the tile and add a new [dashboard tile](../consumer/end-user-tiles.md).</span></span>

  
## <a name="prerequisites"></a><span data-ttu-id="ebd39-120">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="ebd39-120">Prerequisites</span></span>
<span data-ttu-id="ebd39-121">เพื่อติดตาม ให้เปิด Power BI service(ไม่ใช่ Power BI Desktop) และ[ดาวน์โหลดตัวอย่างการวิเคราะห์การใช้จ่ายด้าน IT](sample-it-spend.md)</span><span class="sxs-lookup"><span data-stu-id="ebd39-121">To follow along, open Power BI service (not Power BI Desktop) and [download the IT Spend Analysis sample](sample-it-spend.md).</span></span> <span data-ttu-id="ebd39-122">เมื่อข้อความแสดงความสำเร็จปรากฏขึ้น เลือก **ไปยังแดชบอร์ด**</span><span class="sxs-lookup"><span data-stu-id="ebd39-122">When the "Success" message appears, select **Go to dashboard**</span></span>

- - -
<a name="create"></a>

## <a name="create-a-new-visualization-and-pin-it-to-the-dashboard"></a><span data-ttu-id="ebd39-123">สร้างภาพใหญ่และปักมันไว้กับแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="ebd39-123">Create a new visualization and pin it to the dashboard</span></span>
1. <span data-ttu-id="ebd39-124">จากแดชบอร์ดการวิเคราะห์การใช้จ่ายด้าน IT ให้เลือกไทล์ "Amount" เพื่อเปิดรายงาน</span><span class="sxs-lookup"><span data-stu-id="ebd39-124">From the IT Spend Analysis dashboard, select the "Amount" tile to open the report.</span></span>

    ![ไทล์ Amount](media/service-dashboard-edit-tile/power-bi-amount-tile.png)

2. <span data-ttu-id="ebd39-126">เปิดรายงานในมุมมองการแก้ไข โดยการเลือก **แก้ไขรายงาน** จากแถบเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="ebd39-126">Open the report in Editing view by selecting **Edit report** from the top menubar.</span></span>

3. <span data-ttu-id="ebd39-127">เพิ่มหน้ารายงานใหม่โดยเลือกไอคอนเครื่องหมายบวก (+) ที่ด้านล่างของรายงาน</span><span class="sxs-lookup"><span data-stu-id="ebd39-127">Add a new report page by selecting the plus sign (+) at the bottom of the report.</span></span>

    ![ไอคอนบวก](media/service-dashboard-edit-tile/power-bi-add-page.png)

4. <span data-ttu-id="ebd39-129">จากบานหน้าต่างเขตข้อมูล ให้เลือก **ข้อเท็จจริง > ยอด** และ **พื้นที่ธุรกิจ > พื้นที่ธุรกิจ**</span><span class="sxs-lookup"><span data-stu-id="ebd39-129">From the FIELDS pane, select **Fact > Amount** and **Business Area > Business Area**.</span></span>
 
5. <span data-ttu-id="ebd39-130">จากบานหน้าต่างการแสดงภาพ ให้เลือกไอคอนแผนภูมิโดนัทเพื่อแปลงการสดงภาพลงเป็นแผนภูมิโดนัท</span><span class="sxs-lookup"><span data-stu-id="ebd39-130">From the VISUALIZATIONS pane, select the Donut chart icon to convert the visualization to a Donut chart.</span></span>

    ![บานหน้าต่างการแสดงรูปภาพ](media/service-dashboard-edit-tile/power-bi-donut-chart.png)

5. <span data-ttu-id="ebd39-132">เลือกไอคอนหมุดและปักหมุดแผนภูมิโดนัทกับแดชบอร์ดตัวอย่างการวิเคราะห์การใช้จ่ายด้าน IT</span><span class="sxs-lookup"><span data-stu-id="ebd39-132">Select the pin icon and pin the Donut chart to the IT Spend Analysis sample dashboard.</span></span>

   ![เลื่อนไปเหนือไทล์](media/service-dashboard-edit-tile/power-bi-pin.png)

6. <span data-ttu-id="ebd39-134">เมื่อข้อความแสดงความ “สำเร็จ” ปรากฏขึ้น เลือก **ไปยังแดชบอร์ด**</span><span class="sxs-lookup"><span data-stu-id="ebd39-134">When the "Success"message appears, select **Go to dashboard**.</span></span> <span data-ttu-id="ebd39-135">คุณจะถูกถามให้บันทึกการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="ebd39-135">You will be prompted to save your changes.</span></span> <span data-ttu-id="ebd39-136">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ebd39-136">Select **Save**.</span></span>

- - -
<a name="move"></a>

## <a name="move-the-tile"></a><span data-ttu-id="ebd39-137">ย้ายไทล์</span><span class="sxs-lookup"><span data-stu-id="ebd39-137">Move the tile</span></span>
<span data-ttu-id="ebd39-138">บนแดชบอร์ด ค้นหาไทล์ใหม่</span><span class="sxs-lookup"><span data-stu-id="ebd39-138">On the dashboard, locate the new tile.</span></span> <span data-ttu-id="ebd39-139">เลือกและกดไทล์เพื่อลากไปยังตำแหน่งใหม่บนผืนผ้าใบแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="ebd39-139">Select and hold the tile to drag it to a new location on the dashboard canvas.</span></span>

- - -
<a name="resize"></a>

## <a name="resize-the-tile"></a><span data-ttu-id="ebd39-140">ปรับขนาดไทล์</span><span class="sxs-lookup"><span data-stu-id="ebd39-140">Resize the tile</span></span>
<span data-ttu-id="ebd39-141">คุณสามารถสร้างไทล์ได้หลายขนาด จาก 1 x 1 หน่วยไทล์จนถึง 5 x 5</span><span class="sxs-lookup"><span data-stu-id="ebd39-141">You can make tiles many different sizes -- from 1x1 tile units up to 5x5.</span></span> <span data-ttu-id="ebd39-142">เลือกและลากหูหิ้ว(ที่มุมล่างขวา) เพื่อปรับขนาดไทล์</span><span class="sxs-lookup"><span data-stu-id="ebd39-142">Select and drag the handle (in the bottom right corner) to resize the tile.</span></span>

![video](media/service-dashboard-edit-tile/pbigif_resizetile4.gif)

- - -
## <a name="more-options--menu"></a><span data-ttu-id="ebd39-144">เมนู **ตัวเลือกเพิ่มเติม** (...)</span><span class="sxs-lookup"><span data-stu-id="ebd39-144">**More options** (...) menu</span></span>

1. <span data-ttu-id="ebd39-145">เลือก **ตัวเลือกเพิ่มเติม** (...) ในมุมขวาบนของไทล์</span><span class="sxs-lookup"><span data-stu-id="ebd39-145">Select **More options** (...) in the upper-right corner of the tile.</span></span> 
   
   ![จุดไข่ปลาไทล์](media/service-dashboard-edit-tile/power-bi-tile.png)

2. <span data-ttu-id="ebd39-147">วางเคอร์เซอร์เหนือไทล์ "บัญชี" และเลือกจุดไข่ปลาเมื่อต้องแสดงตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="ebd39-147">Hover over the "Account" tile and select the ellipses to display the options.</span></span> <span data-ttu-id="ebd39-148">ตัวเลือกที่พร้อมใช้งานจะแตกต่างกันตามชนิดไทล์</span><span class="sxs-lookup"><span data-stu-id="ebd39-148">The options available will vary by tile type.</span></span>  <span data-ttu-id="ebd39-149">ตัวอย่าง ตัวเลือกที่พร้อมใช้งานสำหรับไทล์รายงานแบบไลฟ์ต่างจากตัวเลือกที่พร้อมใช้งานสำหรับไทล์การแสดงภาพแบบมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="ebd39-149">For example, the options available for a live tile are different from options available for a standard visualization tile.</span></span> <span data-ttu-id="ebd39-150">นอกจากนี้ ถ้ามีการแชร์แดชบอร์ดกับคุณ(คุณไม่ใช่เจ้าของ) คุณจะมีตัวเลือกน้อยลง</span><span class="sxs-lookup"><span data-stu-id="ebd39-150">Also, if a dashboard has been shared with you (you are not the owner), you will have fewer options.</span></span>

   ![เมนูตัวเลือกจุดไข่ปลา](media/service-dashboard-edit-tile/power-bi-tile-menu-new.png)

3. <span data-ttu-id="ebd39-152">ให้เลือก **แก้ไขรายละเอียด** เพื่อเปิดหน้าต่าง "ไทล์รายละเอียด"</span><span class="sxs-lookup"><span data-stu-id="ebd39-152">Select **Edit details** to open the "Tile details" window.</span></span> 

    <span data-ttu-id="ebd39-153">เปลี่ยนชื่อและค่าเริ่มต้นลักษณะการทำงานของไทล์</span><span class="sxs-lookup"><span data-stu-id="ebd39-153">Change the title and default behavior of the tile.</span></span>  <span data-ttu-id="ebd39-154">ตัวอย่างเช่น คุณอาจตัดสินใจว่าเมื่อเลือก *ผู้บริโภค* ในฐานะไทล์ แทนที่จะเปิดรายงานที่ถูกใช้เพื่อสร้างไทล์ แดชบอร์ดใหม่ได้แสดงแทน</span><span class="sxs-lookup"><span data-stu-id="ebd39-154">For example, you may decide that when a *consumer* selects a tile, instead of opening the report that was used to create that tile, a new dashboard displays instead.</span></span>  
   


<a name="rename"></a>

### <a name="rename-the-tile"></a><span data-ttu-id="ebd39-155">เปลี่ยนชื่อไทล์</span><span class="sxs-lookup"><span data-stu-id="ebd39-155">Rename the tile</span></span>
<span data-ttu-id="ebd39-156">ที่ด้านบนของหน้าต่าง "ไทล์รายละเอียด" ให้เปลี่ยน **ชื่อเรื่อง** เป็น **ยอดเงินที่ใช้**</span><span class="sxs-lookup"><span data-stu-id="ebd39-156">At the top of the "Tile details" window, change **Title** to **Amount spent**.</span></span>

![หน้าต่างรายละเอียดไทล์](media/service-dashboard-edit-tile/power-bi-tile-title.png)


<a name="hyperlink"></a>

### <a name="change-the-default-hyperlink"></a><span data-ttu-id="ebd39-158">เปลี่ยนไฮเปอร์ลิงก์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ebd39-158">Change the default hyperlink</span></span>
<span data-ttu-id="ebd39-159">ตามค่าเริ่มต้น การเลือกไทล์โดยปกติแล้วจะนำคุณไปยังรายงานทีไทล์ หรือ Q&A(ถ้าไทล์ถูกสร้างขึ้นใน Q&A)</span><span class="sxs-lookup"><span data-stu-id="ebd39-159">By default, selecting a tile usually takes you to the report where the tile was created or to Q&A (if the tile was created in Q&A).</span></span> <span data-ttu-id="ebd39-160">เมื่อต้องการเชื่อมโยงไปยังเว็บเพจ แดชบอร์ดอื่นหรือรายงาน (ในพื้นที่ทำงานเดียวกัน) รายงาน SSRS หรือเนื้อหาอื่นๆ แบบออนไลน์ ให้เพิ่มลิงก์แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ebd39-160">To link to a webpage, another dashboard or report (in the same workspace), an SSRS report, or other online content - add a custom link.</span></span>

1. <span data-ttu-id="ebd39-161">ภายใต้หัวเรื่องฟังก์ชันการทำงาน ให้เลือก **ตั้งค่าลิงก์แบบกำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="ebd39-161">Under the Functionality heading, select **Set custom link**.</span></span>

2. <span data-ttu-id="ebd39-162">เลือก **ลิงก์ไปยังแดชบอร์ดหรือรายงานในพื้นที่ทำงานปัจจุบัน** แล้ว เลือกจากรายการแบบดร๊อปดาวน์</span><span class="sxs-lookup"><span data-stu-id="ebd39-162">Select **Link to a dashboard or report in the current workspace** and then select from the dropdown.</span></span>  <span data-ttu-id="ebd39-163">ในตัวอย่างนี้ เราได้เลือกแดชบอร์ดตัวอย่างทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="ebd39-163">In this example I've selected the Human Resources sample dashboard.</span></span> <span data-ttu-id="ebd39-164">ถ้าคุณไม่มีตัวอย่างนี้อยู่ในพื้นที่ทำงานของคุณ คุณสามารถเพิ่มและกลับไปยังขั้นตอนนี้ หรือคุณสามารถเลือกแดชบอร์ดที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="ebd39-164">If you don't have this sample already in your workspace, you can add it and come back to this step, or you can select a different dashboard.</span></span> 

    ![กล่องโต้ตอบการทำงาน](media/service-dashboard-edit-tile/power-bi-custom-link.png)

3. <span data-ttu-id="ebd39-166">เลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="ebd39-166">Select **Apply**.</span></span>

4. <span data-ttu-id="ebd39-167">ชื่อเรื่องใหม่แสดงบนไทล์</span><span class="sxs-lookup"><span data-stu-id="ebd39-167">The new title displays on the tile.</span></span>  <span data-ttu-id="ebd39-168">และ เมื่อคุณเลือกไทล์ Power BI เปิดแดชบอร์ดทรัพยากรบุคคลขึ้น</span><span class="sxs-lookup"><span data-stu-id="ebd39-168">And, when you select the tile, Power BI opens the Human Resources dashboard.</span></span> 

    ![ชื่อไทล์](media/service-dashboard-edit-tile/power-bi-title.png)

<a name="different"></a>

### <a name="pin-the-tile-to-a-different-dashboard"></a><span data-ttu-id="ebd39-170">ปักหมุดแดชบอร์ดไทล์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="ebd39-170">Pin the tile to a different dashboard</span></span>
1. <span data-ttu-id="ebd39-171">จากเมนูจุดไข่ปลาแบบหล่นลง ให้เลือก **ปักหมุดไทล์** ![ไอคอนหมุด](media/service-dashboard-edit-tile/pinnooutline.png)</span><span class="sxs-lookup"><span data-stu-id="ebd39-171">From the ellipses dropdown menu, select **Pin tile** ![pin icon](media/service-dashboard-edit-tile/pinnooutline.png) .</span></span>
2. <span data-ttu-id="ebd39-172">ให้ตัดสินใจว่าจะปักหมุดรายการซ้ำของไทล์นี้กับแดชบอร์ดที่มีอยแล้วหรือแดชบอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="ebd39-172">Decide whether to pin a duplicate of this tile to an existing dashboard or to a new dashboard.</span></span> 
   
   ![ปักหมุดไปยังแดชบอร์ด](media/service-dashboard-edit-tile/pbi_pintoanotherdash.png)
3. <span data-ttu-id="ebd39-174">เลือก **หมุด**</span><span class="sxs-lookup"><span data-stu-id="ebd39-174">Select **Pin**.</span></span>

<a name="delete"></a>

### <a name="delete-the-tile"></a><span data-ttu-id="ebd39-175">ลบไทล์</span><span class="sxs-lookup"><span data-stu-id="ebd39-175">Delete the tile</span></span>
1. <span data-ttu-id="ebd39-176">หากต้องการลบไทล์ออกอย่างถาวรจากแดชบอร์ด ให้เลือก **ลบไทล์** ![ไอคอนลบ](media/service-dashboard-edit-tile/power-bi-delete-tile-icon.png) จากเมนูจุดไข่ปลาแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="ebd39-176">To permanently remove a tile from a dashboard, select  **Delete tile** ![delete icon](media/service-dashboard-edit-tile/power-bi-delete-tile-icon.png) from the ellipses dropdown menu.</span></span> 

2. <span data-ttu-id="ebd39-177">การลบไทล์ไม่ลบการแสดงภาพแบบพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="ebd39-177">Deleting a tile does not delete the underlying visualization.</span></span> <span data-ttu-id="ebd39-178">เปิดรายงานพื้นฐาน โดยเลือกไทล์ "Amount"</span><span class="sxs-lookup"><span data-stu-id="ebd39-178">Open the underlying report by selecting the "Amount" tile.</span></span> <span data-ttu-id="ebd39-179">เปิดหน้าสุดท้ายในรายงานของคุณ เพื่อดูว่าการแสดงภาพต้นฉบับไม่ถูกลบจากรายงานหรือไม่</span><span class="sxs-lookup"><span data-stu-id="ebd39-179">Open the last page in your report to see that the original visualization has not been deleted from the report.</span></span> 

- - -
## <a name="next-steps"></a><span data-ttu-id="ebd39-180">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="ebd39-180">Next steps</span></span>
[<span data-ttu-id="ebd39-181">ไทล์แดชบอร์ดใน Power BI</span><span class="sxs-lookup"><span data-stu-id="ebd39-181">Dashboard tiles in Power BI</span></span>](../consumer/end-user-tiles.md)

[<span data-ttu-id="ebd39-182">แดชบอร์ดใน Power BI</span><span class="sxs-lookup"><span data-stu-id="ebd39-182">Dashboards in Power BI</span></span>](../consumer/end-user-dashboards.md)

[<span data-ttu-id="ebd39-183">แนวคิดพื้นฐานสำหรับนักออกแบบในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="ebd39-183">Basic concepts for designers in the Power BI service</span></span>](../fundamentals/service-basic-concepts.md)

<span data-ttu-id="ebd39-184">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="ebd39-184">More questions?</span></span> [<span data-ttu-id="ebd39-185">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="ebd39-185">Try the Power BI Community</span></span>](https://community.powerbi.com/)
