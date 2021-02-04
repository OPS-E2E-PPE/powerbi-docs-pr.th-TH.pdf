---
title: ใช้เส้นตารางและจัดชิดกับเส้นตารางในรายงาน Power BI Desktop
description: ใช้เส้นตาราง จัดชิดกับเส้นตาราง ลำดับแบบ Z การจัดแนว และการแจกจ่ายในรายงาน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 05/08/2019
LocalizationGroup: Create reports
ms.openlocfilehash: 745b89efc76c179c0393e4dccd29d5bee6910676
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412954"
---
# <a name="use-gridlines-and-snap-to-grid-in-power-bi-desktop-reports"></a><span data-ttu-id="a9858-103">ใช้เส้นตารางและจัดชิดกับเส้นตารางในรายงาน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a9858-103">Use gridlines and snap-to-grid in Power BI Desktop reports</span></span>
<span data-ttu-id="a9858-104">พื้นที่รายงาน **Power BI Desktop** แสดงเส้นตารางที่ช่วยให้คุณจัดแนววิชวลบนหน้ารายงานได้อย่างสวยงาม และยังมีฟังก์ชันจัดชิดเส้นตาราง ให้วิชวลในรายงานของคุณดูสะอาด, อยู่ในแนวเดียวกัน และระยะห่างเท่ากัน</span><span class="sxs-lookup"><span data-stu-id="a9858-104">The **Power BI Desktop** report canvas provides gridlines that let you neatly align visuals on a report page and use snap-to-grid functionality so the visuals in your report look clean, aligned, and evenly spaced.</span></span>

<span data-ttu-id="a9858-105">ใน **Power BI Desktop** คุณยังสามารถปรับลำดับแบบ Z (นำไปข้างหน้า, ย้ายไปข้างหลัง) ของวัตถุบนรายงาน และจัดแนว หรือกระจายวิชวลที่เลือกห่างให้เท่า ๆ กันบนพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="a9858-105">In **Power BI Desktop**, you can also adjust the z-order (bring forward, send backward) of objects on a report and align or evenly distribute selected visuals on the canvas.</span></span>

![ภาพหน้าจอของผืนผ้าใบรายงาน ที่แสดงวิธีการใช้เส้นกริดและการกระโดดเข้าหาจุดกริดในรายงาน Power BI Desktop](media/desktop-gridlines-snap-to-grid/snap-to-grid_0.png)

## <a name="enabling-gridlines-and-snap-to-grid"></a><span data-ttu-id="a9858-107">การเปิดใช้งานเส้นตารางและจัดชิดกับเส้นตาราง</span><span class="sxs-lookup"><span data-stu-id="a9858-107">Enabling gridlines and snap-to-grid</span></span>
<span data-ttu-id="a9858-108">เมื่อต้องการเปิดใช้งานเส้นตารางและจัดชิดกับเส้นตาราง เลือกแบบ **มุมมอง** Ribbon จากนั้นเปิดใช้กล่องกาเครื่องหมายสำหรับ **แสดงเส้นตาราง** และ **จัดชิดวัตถุกับเส้นตาราง**</span><span class="sxs-lookup"><span data-stu-id="a9858-108">To enable gridlines and snap-to-grid, select the **View** ribbon, then enable the checkboxes for **Show gridlines** and **Snap objects to grid.**</span></span> <span data-ttu-id="a9858-109">คุณสามารถเลือกหนึ่งหรือทั้งสองตัวเลือก ซึ่งทำงานอิสระจากกัน</span><span class="sxs-lookup"><span data-stu-id="a9858-109">You can select one or both options; they operate independently.</span></span>

![ภาพหน้าจอของผืนผ้าใบรายงาน ที่แสดงวิธีการเปิดใช้งานเส้นกริดและการกระโดดเข้าหาจุดกริดในรายงาน Power BI Desktop](media/desktop-gridlines-snap-to-grid/snap-to-grid_1.png)

> [!NOTE]
> <span data-ttu-id="a9858-111">ถ้า **การแสดงเส้นตาราง** และ **จัดชิดวัตถุกับเส้นตาราง** ถูกปิดใช้งาน ให้เชื่อมต่อกับแหล่งข้อมูลใด ๆ และพวกเขาจะถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a9858-111">If **Show gridlines** and **Snap objects to grid** are disabled, connect to any data source and they become enabled.</span></span>

## <a name="using-gridlines"></a><span data-ttu-id="a9858-112">การใช้เส้นตาราง</span><span class="sxs-lookup"><span data-stu-id="a9858-112">Using gridlines</span></span>
<span data-ttu-id="a9858-113">เส้นตารางเป็นแนวที่คุณมองเห็นได้ เพื่อช่วยการจัดแนววิชวลของคุณ</span><span class="sxs-lookup"><span data-stu-id="a9858-113">Gridlines are visible guides that help you align your visuals.</span></span> <span data-ttu-id="a9858-114">เมื่อคุณพยายามพิจารณาว่า วิชวลสองวิชวล (หรือมากกว่า) อยู่ในแนวนอนหรือแนวตั้งเดียวกันหรือไม่ ใช้เส้นตารางเพื่อดูว่าเส้นขอบของวิชวลตรงกันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a9858-114">When you're trying to determine whether two (or more) visuals are aligned horizontally or vertically, use the gridlines to determine whether their borders align.</span></span>

<span data-ttu-id="a9858-115">ใช้ Ctrl+คลิก เพื่อเลือกมากกว่าหนึ่งวิชวลในแต่ละครั้ง ซึ่งจะแสดงเส้นขอบของวิชวลที่เลือกทั้งหมด และแสดงให้เห็นว่าวิชวลอยู่ในแนวเดียวกันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a9858-115">Use Ctrl+Click to select more than one visual at a time, which displays all selected visuals' borders and shows whether the visuals are properly aligned.</span></span>

![ภาพหน้าจอของผืนผ้าใบรายงาน ที่แสดงวิธีการใช้เส้นตารางเพื่อจัดแนววิชวลของคุณ](media/desktop-gridlines-snap-to-grid/snap-to-grid_2.png)

### <a name="using-gridlines-inside-visuals"></a><span data-ttu-id="a9858-117">การใช้เส้นตารางภายในภาพ</span><span class="sxs-lookup"><span data-stu-id="a9858-117">Using gridlines inside visuals</span></span>
<span data-ttu-id="a9858-118">ใน Power BI ยังมีเส้นตารางภายในวิชวล ซึ่งแสดงเส้นบอกแนวสำหรับการเปรียบเทียบจุดข้อมูลและค่าต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="a9858-118">In Power BI there are also gridlines inside visuals that provide visible guides for comparing data points and values.</span></span> <span data-ttu-id="a9858-119">เริ่มต้นด้วยการวางจำหน่าย **Power BI Desktop** ในเดือน 2017 กันยายน ตอนนี้คุณสามารถจัดการเส้นตารางภายในภาพที่ใช้บัตร **แกน x** หรือ **แกน y**(ตามความเหมาะสมตามชนิดของภาพ) พบในส่วน **รูปแบบ** ของบานหน้าต่าง **การแสดงภาพ**</span><span class="sxs-lookup"><span data-stu-id="a9858-119">Beginning with the September 2017 release of **Power BI Desktop**, you can now manage the gridlines within visuals using the **X-Axis** or **Y-Axis** card (as appropriate based on visual type), found in the **Format** section of the **Visualizations** pane.</span></span> <span data-ttu-id="a9858-120">คุณสามารถจัดการองค์ประกอบของเส้นตารางภายในภาพต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a9858-120">You can manage the following elements of gridlines within a visual:</span></span>

* <span data-ttu-id="a9858-121">เปิดหรือปิดเส้นตาราง</span><span class="sxs-lookup"><span data-stu-id="a9858-121">Turn gridlines on or off</span></span>
* <span data-ttu-id="a9858-122">เปลี่ยนสีของเส้นตาราง</span><span class="sxs-lookup"><span data-stu-id="a9858-122">Change the color of gridlines</span></span>
* <span data-ttu-id="a9858-123">ปรับเส้นขีด (ความกว้าง) ของเส้นตาราง</span><span class="sxs-lookup"><span data-stu-id="a9858-123">Adjust the stroke (the width) of gridlines</span></span>
* <span data-ttu-id="a9858-124">เลือกสไตล์เส้นของเส้นตารางในภาพ เช่น ทึบ เส้นประ หรือจุด</span><span class="sxs-lookup"><span data-stu-id="a9858-124">Select the line style of the gridlines in the visual, such as solid, dashed, or dotted</span></span>

<span data-ttu-id="a9858-125">การปรับเปลี่ยนองค์ประกอบบางอย่างของเส้นตารางจะมีประโยชน์ในรายงานที่ใช้พื้นหลังสีเข้มสำหรับภาพ</span><span class="sxs-lookup"><span data-stu-id="a9858-125">Modifying certain elements of gridlines can be especially useful in reports where dark backgrounds are used for visuals.</span></span> <span data-ttu-id="a9858-126">รูปต่อไปนี้แสดงส่วน **เส้นตาราง** ในการ์ด **แกน Y**</span><span class="sxs-lookup"><span data-stu-id="a9858-126">The following image shows the **Gridlines** section in the **Y-Axis** card.</span></span>

![ภาพหน้าจอของวิชวล ที่แสดงส่วนเส้นตารางในการ์ดแกน Y](media/desktop-gridlines-snap-to-grid/snap-to-grid_9.png)

## <a name="using-snap-to-grid"></a><span data-ttu-id="a9858-128">การใช้การจัดชิดกับเส้นตาราง</span><span class="sxs-lookup"><span data-stu-id="a9858-128">Using snap-to-grid</span></span>
<span data-ttu-id="a9858-129">เมื่อคุณเปิดใช้งาน **จัดชิดวัตถุกับเส้นตาราง** ภาพทั้งหมดบนพื้นที่ทำงาน **Power BI Desktop** ที่คุณย้าย (หรือปรับขนาด) จะถูกจัดชิดกับแกนเส้นตารางที่ใกล้ที่สุดโดยอัตโนมัติ ทำให้ง่ายยิ่งขึ้นในการทำให้แน่ใจว่าภาพสองภาพหรือมากกว่าจัดแนวในตำแหน่งหรือขนาดตามแนวนอนหรือแนวตั้งที่เหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="a9858-129">When you enable **Snap objects to grid**, all visuals on the **Power BI Desktop** canvas that you move (or resize) are automatically aligned to the nearest grid axis, making it much easier to ensure two or more visuals align to the same horizontal or vertical location or size.</span></span>

![ภาพหน้าจอของผืนผ้าใบรายงาน ที่แสดงว่าเส้นกริดและการกระโดดเข้าหาจุดกริดสามารถทำให้แน่ใจว่าวิชวลในรายงานของคุณได้รับการจัดตำแหน่งให้เรียบร้อยได้อย่างไร](media/desktop-gridlines-snap-to-grid/snap-to-grid_3.png)

<span data-ttu-id="a9858-131">และนั่นคือทั้งหมดของการใช้ **เส้นตาราง** และ **จัดชิดกับเส้นตาราง** เพื่อให้แน่ใจว่าวิชวลในรายงานของคุณจัดแนวอย่างเรียบร้อย</span><span class="sxs-lookup"><span data-stu-id="a9858-131">And, that's all there is to using **gridlines** and **snap-to-grid** to ensure the visuals in your reports are neatly aligned.</span></span>

## <a name="using-z-order-align-and-distribute"></a><span data-ttu-id="a9858-132">การใช้ลำดับแบบ Z จัดแนว และกระจาย</span><span class="sxs-lookup"><span data-stu-id="a9858-132">Using z-order, align, and distribute</span></span>
<span data-ttu-id="a9858-133">คุณยังสามารถจัดการลำดับจากหน้าไปหลังของวิชวลในรายงาน ซึ่งมักเรียกว่า *ลำดับแบบ Z* ขององค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="a9858-133">You can manage the front-to-back order of visuals in a report, often referred to as the *z-order* of elements.</span></span> <span data-ttu-id="a9858-134">คุณลักษณะนี้ให้คุณสามารถทับซ้อนวิชวลในแบบใดก็ได้ที่คุณต้องการ จากนั้นปรับลำดับจากหน้าไปหลังของแต่ละวิชวล</span><span class="sxs-lookup"><span data-stu-id="a9858-134">This feature lets you overlap visuals in any way you want, then adjust the front-to-back order of each.</span></span> <span data-ttu-id="a9858-135">คุณตั้งค่าลำดับของวิชวลคุณโดยใช้ปุ่ม **นำไปข้างหน้า** และ **ย้ายไปข้างหลัง** ที่พบในส่วน **จัดเรียง** ของ ribbon **รูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="a9858-135">You set the order of your visuals using the **Bring Forward** and **Send Backward** buttons, found in the **Arrange** section of **Format** ribbon.</span></span> <span data-ttu-id="a9858-136">Ribbon **รูปแบบ** จะปรากฏขึ้นทันทีที่คุณเลือกหนึ่งหรือหลายวิชวลบนหน้า</span><span class="sxs-lookup"><span data-stu-id="a9858-136">The **Format** ribbon appears as soon as you select one or more visuals on the page.</span></span>

![ภาพหน้าจอของผืนผ้าใบรายงาน ที่แสดงวิธีการจัดการลำดับของวิชวลจากด้านหน้าไปด้านหลังในรายงาน](media/desktop-gridlines-snap-to-grid/snap-to-grid_4.png)

<span data-ttu-id="a9858-138">Ribbon **รูปแบบ** ให้คุณสามารถจัดแนวภาพของคุณในวิธีต่าง ๆ ให้คุณแน่ใจว่าวิชวลของคุณปรากฏบนหน้า ที่จัดแนวได้สวยงามและทำงานได้ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="a9858-138">The **Format** ribbon lets you align your visuals in many different ways, which ensures your visuals appear on the page in the alignment that looks and works best.</span></span>

![ภาพหน้าจอของผืนผ้าใบรายงาน ที่แสดงวิธีจัดแนววิชวลของคุณในหลากหลายวิธี](media/desktop-gridlines-snap-to-grid/snap-to-grid_5.png)

<span data-ttu-id="a9858-140">ปุ่ม **จัดแนว** จัดแนววิชวลตามขอบ (หรือกึ่งกลาง) ของพื้นที่รายงาน ดังที่แสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a9858-140">The **Align** button aligns a selected visual to the edge (or center) of the report canvas, as shown in the following image.</span></span>

![ภาพหน้าจอของผืนผ้าใบรายงาน ที่แสดงวิธีการใช้ปุ่มจัดแนวเพื่อจัดแนววิชวลที่เลือกไปที่ขอบ (หรือกึ่งกลาง) ของผืนผ้าใบ](media/desktop-gridlines-snap-to-grid/snap-to-grid_6.png)

<span data-ttu-id="a9858-142">เมื่อเลือกวิชวลอย่างน้อยสองวิชวล วิชวลเหล่านั้นจะถูกจัดแนวพร้อมกัน และใช้ขอบเขตที่ถูกจัดแนวแล้วของวิชวลสำหรับการจัดแนว</span><span class="sxs-lookup"><span data-stu-id="a9858-142">When two or more visuals are selected, they are aligned together and use the existing aligned boundary of the visuals for their alignment.</span></span> <span data-ttu-id="a9858-143">ตัวอย่างเช่น ถ้าคุณเลือกสองวิชวล และเลือกตัวเลือก **จัดชิดซ้าย** วิชวลจะจัดชิดขอบซ้ายสุดของวิชวลที่เลือกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a9858-143">For example, if you select two visuals and choose the **Align Left** option, the visuals then align to the left-most boundary of all selected visuals.</span></span>

![ภาพหน้าจอของผืนผ้าใบรายงาน ที่แสดงวิธีการจัดแนววิชวลสองภาพโดยใช้ตัวเลือกจัดชิดซ้าย](media/desktop-gridlines-snap-to-grid/snap-to-grid_7.png)

<span data-ttu-id="a9858-145">คุณยังสามารถกระจายภาพของคุณอย่างสม่ำเสมอทั่วพื้นที่รายงาน ไม่ว่าจะเป็นในแนวตั้งหรือแนวนอน</span><span class="sxs-lookup"><span data-stu-id="a9858-145">You can also distribute your visuals evenly across the report canvas, either vertically or horizontally.</span></span> <span data-ttu-id="a9858-146">เพียงแค่ใช้ปุ่ม **กระจาย** จาก Ribbon **รูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="a9858-146">Just use the **Distribute** button from the **Format** ribbon.</span></span>

![ภาพหน้าจอของผืนผ้าใบรายงาน ที่แสดงวิธีการกระจายวิชวลของคุณอย่างสม่ำเสมอทั่วทั้งผืนผ้าใบโดยใช้ตัวเลือกการแจกจ่าย](media/desktop-gridlines-snap-to-grid/snap-to-grid_8.png)

<span data-ttu-id="a9858-148">ด้วยการเลือกสองสามรายการจากเส้นตาราง, การจัดแนว และเครื่องมือการกระจาย รายงานของคุณจะมีลักษณะตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="a9858-148">With a few selections from these gridlines, alignment, and distribution tools, your reports will look just how you want them to.</span></span>

