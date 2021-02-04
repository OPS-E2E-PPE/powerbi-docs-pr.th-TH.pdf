---
title: ใช้การจัดกลุ่มใน Power BI Desktop
description: เรียนรู้วิธีการจัดกลุ่มใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 05/26/2020
LocalizationGroup: Create reports
ms.openlocfilehash: b74e06c076cd25132a6e3bfb8a12775d50b7263f
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412908"
---
# <a name="group-visuals-in-power-bi-desktop-reports"></a><span data-ttu-id="d340a-103">จัดกลุ่มวิชวลในรายงาน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d340a-103">Group visuals in Power BI Desktop reports</span></span>
<span data-ttu-id="d340a-104">ด้วยคุณลักษณะ **การจัดกลุ่ม** ใน **Power BI Desktop** คุณสามารถจัดกลุ่มวิชวลเข้าด้วยกันในรายงานของคุณได้ เช่น ปุ่ม กล่องข้อความ ภาพรูปทรง และวิชวลที่คุณสร้างเช่นเดียวกับที่คุณจัดกลุ่มรายการใน PowerPoint</span><span class="sxs-lookup"><span data-stu-id="d340a-104">With **grouping** in **Power BI Desktop**, you can group visuals together in your report, such as buttons, textboxes, shapes images, and any visual you create, just like you group items in PowerPoint.</span></span> <span data-ttu-id="d340a-105">การจัดกลุ่มวิชวลในรายงานช่วยให้คุณปฏิบัติต่อกลุ่มเช่นเดียวกับวัตถุเดี่ยว ทำให้เคลื่อนไหว ปรับขนาด และทำงานกับเลเยอร์ในรายงานของคุณได้ง่ายขึ้นเร็วขึ้น และทันใจขึ้น</span><span class="sxs-lookup"><span data-stu-id="d340a-105">Grouping visuals in a report lets you treat the group like a single object, making moving, resizing, and working with layers in your report easier, faster, and more intuitive.</span></span>

![ใช้งานการจัดกลุ่ม](media/desktop-grouping-visuals/grouping-visuals-01.png)


## <a name="creating-groups"></a><span data-ttu-id="d340a-107">การสร้างกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="d340a-107">Creating groups</span></span>

<span data-ttu-id="d340a-108">หากต้องการสร้างกลุ่มของวิชวลใน Power BI Desktop ให้เลือกวิชวลแรกจากพื้นที่ทำงาน จากนั้นกดปุ่ม CTRL ค้างไว้ คลิกวิชวลตั้งแต่หนึ่งภาพขึ้นไปซึ่งเป็นวิชวลที่คุณต้องการให้อยู่ในกลุ่ม จากนั้นคลิกขวาที่ชุดของวิชวล และเลือก **กลุ่ม** จากเมนูที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="d340a-108">To create a group of visuals in Power BI Desktop, select the first visual from the canvas, then holding the CTRL button, click one or more additional visuals that you want in the group, then right-click the collection of visuals and select **Group** from the menu that appears.</span></span>

![เลือกอย่างน้อยสองรายการไปยังกลุ่ม](media/desktop-grouping-visuals/grouping-visuals-02.png)

<span data-ttu-id="d340a-110">กลุ่มจะแสดงในบานหน้าต่าง **การเลือก**</span><span class="sxs-lookup"><span data-stu-id="d340a-110">Groups are displayed in the **Selection** pane.</span></span> <span data-ttu-id="d340a-111">คุณสามารถมีกลุ่มของวิชวลจำนวนมากตามที่รายงานของคุณต้องการ และคุณยังสามารถซ้อนกลุ่มของวิชวลได้</span><span class="sxs-lookup"><span data-stu-id="d340a-111">You can have as many groups of visuals as your report needs, and you can also nest groups of visuals.</span></span> <span data-ttu-id="d340a-112">ในรูปภาพต่อไปนี้ กลุ่ม *ออสเตรเลีย* ซ้อนอยู่ในกลุ่ม *การ์ด*</span><span class="sxs-lookup"><span data-stu-id="d340a-112">In the following image, the *Australia* group is nested under the *Cards* group.</span></span> <span data-ttu-id="d340a-113">คุณสามารถขยายกลุ่มโดยเลือกสัญลักษณ์ ^ ข้างชื่อกลุ่มและยุบโดยเลือกสัญลักษณ์ ^ อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="d340a-113">You can expand a group by selecting the caret beside the group name, and collapse it by selecting the caret again.</span></span> 

![การซ้อนกลุ่ม](media/desktop-grouping-visuals/grouping-visuals-03.png)

<span data-ttu-id="d340a-115">ภายในบานหน้าต่าง **การเลือก** คุณยังสามารถลากและปล่อยแต่ละวิชวลเพื่อรวมไว้ในกลุ่ม ลบออกจากกลุ่ม ซ้อนกลุ่ม หรือลบกลุ่มหรือแต่ละวิชวลออกจากการซ้อนกันได้</span><span class="sxs-lookup"><span data-stu-id="d340a-115">Within the **Selection** pane, you can also drag and drop individual visuals to include them in a group, remove them from a group, nest a group, or remove a group or individual visual from a nest.</span></span> <span data-ttu-id="d340a-116">เพียงแค่ลากวิชวลที่คุณต้องการปรับและวางลงในตำแหน่งที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="d340a-116">Simply drag the visual you want to adjust, and place it where you want.</span></span> <span data-ttu-id="d340a-117">หากมีการซ้อนทับ การสร้างเลเยอร์ของวิชวลจะถูกกำหนดโดยคำสั่งของพวกเขาในรายการ *ลำดับเลเยอร์*</span><span class="sxs-lookup"><span data-stu-id="d340a-117">Layering of visuals, if there is overlap, is determined by their order in the *Layer order* list.</span></span>

<span data-ttu-id="d340a-118">การเปลี่ยนชื่อกลุ่มเป็นเรื่องง่าย: เพียงแค่ดับเบิลคลิกที่ชื่อกลุ่มในบานหน้าต่าง **การเลือก** จากนั้นจึงพิมพ์ชื่อใหม่ของกลุ่มของคุณ</span><span class="sxs-lookup"><span data-stu-id="d340a-118">Renaming a group is easy: just double-click the group name in the **Selection** pane, and then type in the new name of your group.</span></span>

![ลากแล้วปล่อยกลุ่ม](media/desktop-grouping-visuals/grouping-visuals-04.png)

<span data-ttu-id="d340a-120">เมื่อต้องการยกเลิกการจัดกลุ่ม ให้คลิกขวาแล้วเลือก **ยกเลิกการจัดกลุ่ม** จากเมนูที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="d340a-120">To ungroup just select the group, right-click and select **ungroup** from the menu that appears.</span></span>

## <a name="hide-and-show-visuals-or-groups"></a><span data-ttu-id="d340a-121">ซ่อนและแสดงวิชวลหรือกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="d340a-121">Hide and show visuals or groups</span></span>

<span data-ttu-id="d340a-122">คุณสามารถซ่อนหรือแสดงกลุ่มได้อย่างง่ายดายโดยใช้บานหน้าต่าง **การเลือก**</span><span class="sxs-lookup"><span data-stu-id="d340a-122">You can easily hide or show groups using the **Selection** pane.</span></span> <span data-ttu-id="d340a-123">หากต้องการซ่อนกลุ่ม ให้เลือกปุ่มดวงตาด้านข้างชื่อกลุ่ม (หรือวิชวลแต่ละรายการ) เพื่อสลับว่าจะซ่อนหรือแสดงภาพหรือกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="d340a-123">To hide a group, select the eye button beside the group name (or any individual visual) to toggle whether the visual or group is hidden or displayed.</span></span> <span data-ttu-id="d340a-124">ในรูปภาพต่อไปนี้ กลุ่ม *ออสเตรเลีย* ถูกซ่อนและส่วนที่เหลือของกลุ่มที่ซ้อนกันในกลุ่ม *การ์ด* จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="d340a-124">In the following image, the *Australia* group is hidden, and the rest of the groups nested in the *Cards* group are displayed.</span></span>


![ซ่อนและแสดงกลุ่ม](media/desktop-grouping-visuals/grouping-visuals-05.png)

<span data-ttu-id="d340a-126">เมื่อคุณซ่อนกลุ่ม วิชวลทั้งหมดภายในกลุ่มนั้นจะถูกซ่อนโดยปุ่มดวงตาของพวกเขาจะเป็นสีเทา (ไม่สามารถเปิดหรือปิดการสลับได้เนื่องจากกลุ่มทั้งหมดถูกซ่อนอยู่)</span><span class="sxs-lookup"><span data-stu-id="d340a-126">When you hide a group, all visuals within that group are hidden, indicated by their eye button being grayed out (unavailable to toggle on or off, because the entire group is hidden).</span></span> <span data-ttu-id="d340a-127">หากต้องการซ่อนเฉพาะวิชวลบางอันภายในกลุ่ม เพียงสลับปุ่มดวงตาที่อยู่ข้างวิชวล และเฉพาะวิชวลนั้นในกลุ่มที่จะถูกซ่อน</span><span class="sxs-lookup"><span data-stu-id="d340a-127">To hide only certain visuals within a group, simply toggle the eye button beside that visual, and only that visual in the group is hidden.</span></span>

## <a name="selecting-visuals-within-a-group"></a><span data-ttu-id="d340a-128">การเลือกวิชวลภายในกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="d340a-128">Selecting visuals within a group</span></span>

<span data-ttu-id="d340a-129">มีสองสามวิธีในการนำทางและเลือกรายการภายในกลุ่มของวิชวล</span><span class="sxs-lookup"><span data-stu-id="d340a-129">There are a few ways to navigate and select items within a group of visuals.</span></span> <span data-ttu-id="d340a-130">รายการต่อไปนี้อธิบายลักษณะการทำงาน:</span><span class="sxs-lookup"><span data-stu-id="d340a-130">The following list describes the behavior:</span></span>

* <span data-ttu-id="d340a-131">การคลิกที่พื้นที่ว่างภายในกลุ่ม (เช่น ช่องว่างระหว่างวิชวล) ซึ่งจะเป็นการไม่เลือกอะไรเลย</span><span class="sxs-lookup"><span data-stu-id="d340a-131">Clicking on empty space within a group (such as white space between visuals) does not select anything</span></span>
* <span data-ttu-id="d340a-132">การคลิกที่วิชวลภายในกลุ่มเลือกทั้งกลุ่ม คลิกครั้งที่สอง ซึ่งจะเป็นการเลือกวิชวลแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="d340a-132">Clicking a visual within a group selects the entire group, a second click selects the individual visual</span></span>
* <span data-ttu-id="d340a-133">การเลือกกลุ่ม และจากนั้นวัตถุอื่นบนพื้นที่รายงาน จากนั้นเลือก **กลุ่ม** จากเมนูคลิกขวา ซึ่งจะเป็นการสร้างกลุ่มแบบซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="d340a-133">Selecting a group, and then another object on the report canvas, then selecting **Group** from the right-click menu creates a nested group</span></span>
* <span data-ttu-id="d340a-134">การเลือกสองกลุ่ม จากนั้นคลิกขวา ซึ่งจะเป็นการแสดงตัวเลือกเพื่อผสานกลุ่มที่เลือก แทนที่จะทำการซ้อน</span><span class="sxs-lookup"><span data-stu-id="d340a-134">Selecting two groups, then right-clicking displays an option to merge the selected groups, rather than nesting them</span></span>

## <a name="apply-background-color"></a><span data-ttu-id="d340a-135">ใช้สีพื้นหลัง</span><span class="sxs-lookup"><span data-stu-id="d340a-135">Apply background color</span></span>

<span data-ttu-id="d340a-136">นอกจากนี้คุณยังสามารถใช้สีพื้นหลังกับกลุ่มได้ด้วยการใช้ส่วน **การจัดรูปแบบ** ของบานหน้าต่าง **การแสดงข้อมูลด้วยภาพ** ดังที่ปรากฏในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d340a-136">You can also apply a background color to a group using the **Formatting** section of the **Visualizations** pane, as shown in the following image.</span></span> 

![สีพื้นหลังสำหรับกลุ่ม](media/desktop-grouping-visuals/grouping-visuals-06.png)

<span data-ttu-id="d340a-138">เมื่อคุณใช้สีพื้นหลังแล้ว ให้คลิกที่ช่องว่างระหว่างวิชวลในกลุ่ม ซึ่งจะเป็นการเลือกกลุ่ม (เปรียบเทียบสิ่งนี้กับการคลิกที่ช่องว่างระหว่างภาพในกลุ่ม ซึ่งจะเป็นการไม่เลือกอะไรเลย)</span><span class="sxs-lookup"><span data-stu-id="d340a-138">Once you apply a background color, clicking on the space between visuals in the group selects the group (compare this to clicking on the white space between visuals in a group, which does not select the group).</span></span> 


## <a name="next-steps"></a><span data-ttu-id="d340a-139">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d340a-139">Next steps</span></span>
<span data-ttu-id="d340a-140">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดกลุ่ม โปรดดูที่วิดีโอต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d340a-140">For more information about grouping, take a look at the following video:</span></span>

* [<span data-ttu-id="d340a-141">การจัดกลุ่มใน Power BI Desktop - วิดีโอ</span><span class="sxs-lookup"><span data-stu-id="d340a-141">Grouping in Power BI Desktop - video</span></span>](https://youtu.be/sf4n7VXoQHY?t=10)

<span data-ttu-id="d340a-142">คุณอาจสนใจบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d340a-142">You might also be interested in the following articles:</span></span>

* [<span data-ttu-id="d340a-143">ใช้ตัวเจาะเข้าถึงรายละเอียดข้ามรายงานใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d340a-143">Use cross-report drillthrough in Power BI Desktop</span></span>](desktop-cross-report-drill-through.md)
* [<span data-ttu-id="d340a-144">การใช้ตัวแบ่งส่วนข้อมูล Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d340a-144">Using slicers Power BI Desktop</span></span>](../visuals/power-bi-visualization-slicers.md)
