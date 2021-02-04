---
title: ใช้การจัดกลุ่ม และจัดช่องเก็บใน Power BI Desktop
description: เรียนรู้วิธีการจัดกลุ่ม และจัดช่องเก็บใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 12/18/2019
LocalizationGroup: Create reports
ms.openlocfilehash: 5f1b3d226fb7b27ebb31879d2f4a5c3489660b94
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412931"
---
# <a name="use-grouping-and-binning-in-power-bi-desktop"></a><span data-ttu-id="ec9eb-103">ใช้การจัดกลุ่ม และจัดช่องเก็บใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ec9eb-103">Use grouping and binning in Power BI Desktop</span></span>
<span data-ttu-id="ec9eb-104">เมื่อ Power BI Desktop สร้างวิชวล จะรวมข้อมูลของคุณให้เป็นส่วน (หรือกลุ่ม) โดยยึดตามค่าที่พบในข้อมูลเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="ec9eb-104">When Power BI Desktop creates visuals, it aggregates your data into chunks (or groups) based on values found in the underlying data.</span></span> <span data-ttu-id="ec9eb-105">ซึ่งปกติแล้วจะทำงานได้ดี แต่อาจมีบางครั้งเมื่อคุณต้องการปรับวิธีการจัดกลุ่มเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="ec9eb-105">Often that's fine, but there may be times when you want to refine how those chunks are presented.</span></span> <span data-ttu-id="ec9eb-106">ตัวอย่างเช่น คุณอาจต้องการวางผลิตภัณฑ์สามประเภทเข้าในประเภทที่ใหญ่ขึ้น (ในหนึ่ง *กลุ่ม*)</span><span class="sxs-lookup"><span data-stu-id="ec9eb-106">For example, you might want to place three categories of products in one larger category (one *group*).</span></span> <span data-ttu-id="ec9eb-107">หรือคุณอาจต้องการดูยอดขายตัวเลขในแท่งกราฟขนาด 1,000,000 ดอลลาร์แทนที่จะหารเป็นจำนวนเท่าๆ 923,983 ดอลลาร์</span><span class="sxs-lookup"><span data-stu-id="ec9eb-107">Or, you might want to see sales figures put into bin-sizes of 1,000,000 dollars, instead of chunks of 923,983-dollar sizes.</span></span>

<span data-ttu-id="ec9eb-108">ใน Power BI Desktop คุณสามารถ *จัดกลุ่ม* จุดข้อมูล เพื่อช่วยให้คุณเห็น วิเคราะห์ สำรวจข้อมูลและแนวโน้มในวิชวลของคุณได้ชัดเจนขึ้น</span><span class="sxs-lookup"><span data-stu-id="ec9eb-108">In Power BI Desktop, you can *group* data points to help you more clearly view, analyze, and explore data and trends in your visuals.</span></span> <span data-ttu-id="ec9eb-109">คุณยังสามารถกำหนด *แท่งกราฟ* เพื่อใส่ค่าลงในกลุ่มที่มีขนาดเท่ากันที่ช่วยให้คุณไปยังข้อมูลแบบรูปภาพในวิธีที่สื่อความหมายได้ดียิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="ec9eb-109">You can also define the *bin size* to put values into equally sized groups that better enable you to visualized data in ways that are meaningful.</span></span> <span data-ttu-id="ec9eb-110">การดำเนินการนี้มักเรียกว่า *binning*</span><span class="sxs-lookup"><span data-stu-id="ec9eb-110">This action is often called *binning*.</span></span>

## <a name="using-grouping"></a><span data-ttu-id="ec9eb-111">ใช้งานการจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="ec9eb-111">Using grouping</span></span>
<span data-ttu-id="ec9eb-112">เพื่อใช้การจัดกลุ่ม เลือกองค์ประกอบอย่างน้อยสองอย่างบนวิชวล โดยใช้ Ctrl + คลิก เพื่อเลือกหลายองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="ec9eb-112">To use grouping, select two or more elements on a visual by using Ctrl+click to select multiple elements.</span></span> <span data-ttu-id="ec9eb-113">จากนั้นคลิกขวาที่หนึ่งในองค์ประกอบการเลือกหลายส่วนและเลือก **กลุ่ม** จากเมนูบริบท</span><span class="sxs-lookup"><span data-stu-id="ec9eb-113">Then right-click one of the multiple selection elements and choose **Group** from the context menu.</span></span>

![คำสั่งกลุ่ม, กราฟ, การจัดกลุ่ม, Power BI Desktop](media/desktop-grouping-and-binning/grouping-binning_1.png)

<span data-ttu-id="ec9eb-115">เมื่อสร้างกลุ่มขึ้นแล้ว กลุ่มจะถูกเพิ่มลงในบักเก็ต **คำอธิบายแผนภูมิ** สำหรับวิชวล</span><span class="sxs-lookup"><span data-stu-id="ec9eb-115">Once it's created, the group is added to the **Legend** bucket for the visual.</span></span> <span data-ttu-id="ec9eb-116">กลุ่มจะยังปรากฏในรายการ **เขตข้อมูล** อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="ec9eb-116">The group also appears in the **Fields** list.</span></span>

![รายการคำอธิบายแผนภูมิและเขตข้อมูล, การจัดกลุ่ม, Power BI Desktop](media/desktop-grouping-and-binning/grouping-binning_2.png)

<span data-ttu-id="ec9eb-118">เมื่อมีกลุ่มแล้ว คุณจะสามารถแก้ไขสมาชิกของกลุ่มดังกล่าวได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="ec9eb-118">Once you have a group, you can easily edit the members of that group.</span></span> <span data-ttu-id="ec9eb-119">คลิกขวาที่เขตข้อมูลจากบักเก็ต **คำอธิบายแผนภูมิ** หรือจากรายการ **เขตข้อมูล** จากนั้นเลือก **แก้ไขกลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="ec9eb-119">Right-click the field from the **Legend** bucket or from the **Fields** list, and then choose **Edit Groups**.</span></span>

![แก้ไขคำสั่งกลุ่ม, รายการคำอธิบายแผนภูมิและเขตข้อมูล, Power BI Desktop](media/desktop-grouping-and-binning/grouping-binning_3.png)

<span data-ttu-id="ec9eb-121">ในกล่องโต้ตอบ **กลุ่ม** คุณสามารถสร้างกลุ่มใหม่หรือปรับเปลี่ยนกลุ่มที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="ec9eb-121">In the **Groups** dialog box, you can create new groups or modify existing groups.</span></span> <span data-ttu-id="ec9eb-122">นอกจากนี ้คุณยังสามารถ *เปลี่ยนชื่อ* กลุ่มใด ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="ec9eb-122">You can also *rename* any group.</span></span> <span data-ttu-id="ec9eb-123">เพียงคลิกสองครั้งที่ชื่อกลุ่มในกล่อง **กลุ่มและสมาชิก** จากนั้น ป้อนชื่อใหม่</span><span class="sxs-lookup"><span data-stu-id="ec9eb-123">Just double-click the group title in the **Groups and members** box, and then enter a new name.</span></span>

<span data-ttu-id="ec9eb-124">คุณสามารถทำหลากหลายอย่างได้ด้วยการจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="ec9eb-124">You can do all sorts of things with groups.</span></span> <span data-ttu-id="ec9eb-125">คุณสามารถเพิ่มรายการจากรายการ **ค่าที่ยังไม่ได้จัดกลุ่ม** ลงในกลุ่มใหม่ หรือลงในกลุ่มที่มีอยู่แล้วได้</span><span class="sxs-lookup"><span data-stu-id="ec9eb-125">You can add items from the **Ungrouped values** list into a new group or into one of the existing groups.</span></span> <span data-ttu-id="ec9eb-126">เมื่อต้องการสร้างกลุ่มใหม่ เลือกอย่างน้อยสองหน่วยข้อมูล (ใช้ Ctrl + คลิก) จากกล่อง **ค่าที่ยังไม่ได้จัดกลุ่ม** และจากนั้นเลือกปุ่ม **กลุ่ม** ด้านล่างกล่องนั้น</span><span class="sxs-lookup"><span data-stu-id="ec9eb-126">To create a new group, select two or more items (using Ctrl+click) from the **Ungrouped values** box, and then select the **Group** button below that box.</span></span>

<span data-ttu-id="ec9eb-127">คุณสามารถเพิ่มค่าที่ยังไม่ได้จัดกลุ่มลงในกลุ่มที่มีอยู่: เพียงแค่เลือก **ค่าที่ยังไม่ได้จัดกลุ่ม** จากนั้นเลือกกลุ่มที่มีอยู่ที่คุณต้องการเพิ่มค่า แล้วเลือกปุ่ม **กลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="ec9eb-127">You can add an ungrouped value into an existing group: just select the one of the **Ungrouped values**, then select the existing group to add the value to, and select the **Group** button.</span></span> <span data-ttu-id="ec9eb-128">เมื่อต้องการนำหน่วยข้อมูลออกจากกลุ่ม เลือกจากกล่อง **กลุ่มและสมาชิก** และจากนั้น เลือก **ยกเลิกการจัดกลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="ec9eb-128">To remove an item from a group, select it from the **Groups and members** box, and then select **Ungroup**.</span></span> <span data-ttu-id="ec9eb-129">นอกจากนี้ คุณยังสามารถย้ายหมวดหมู่ที่ยังไม่ได้จัดกลุ่มไปยังกลุ่ม **อื่นๆ** หรือปล่อยไว้โดยไม่จัดกลุ่มเช่นเดิมก็ได้</span><span class="sxs-lookup"><span data-stu-id="ec9eb-129">You can also move ungrouped categories into the **Other** group or leave them ungrouped.</span></span>

![กล่องโต้ตอบกลุ่ม, Power BI Desktop](media/desktop-grouping-and-binning/grouping-binning_4.png)

> [!NOTE]
> <span data-ttu-id="ec9eb-131">คุณสามารถสร้างกลุ่มสำหรับเขตข้อมูลใด ๆ ใน **เขตข้อมูล** โดยไม่จำเป็นต้องเลือกหน่วยข้อมูลหลายรายการจากวิชวลที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="ec9eb-131">You can create groups for any field in the **Fields** well, without having to select multiple items from an existing visual.</span></span> <span data-ttu-id="ec9eb-132">เพียงคลิกขวาที่เขตข้อมูล และเลือก **กลุ่มใหม่** จากเมนูที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="ec9eb-132">Just right-click the field, and select **New Group** from the menu that appears.</span></span>

## <a name="using-binning"></a><span data-ttu-id="ec9eb-133">ใช้งานการจัดช่องเก็บ</span><span class="sxs-lookup"><span data-stu-id="ec9eb-133">Using binning</span></span>
<span data-ttu-id="ec9eb-134">คุณสามารถตั้งค่าขนาดช่องเก็บสำหรับเขตข้อมูลตัวเลข และเวลาใน **Power BI Desktop** ได้</span><span class="sxs-lookup"><span data-stu-id="ec9eb-134">You can set the bin size for numerical and time fields in **Power BI Desktop.**</span></span> <span data-ttu-id="ec9eb-135">คุณสามารถใช้การจัดช่องเก็บ (Binning) เพื่อให้ Power BI Desktop แสดงข้อมูลด้วยขนาดที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="ec9eb-135">You can use binning to right-size the data that Power BI Desktop displays.</span></span>

<span data-ttu-id="ec9eb-136">เมื่อต้องการปรับใช้ขนาดช่องเก็บ คลิกขวาที่ **เขตข้อมูล** และเลือก **กลุ่มใหม่**</span><span class="sxs-lookup"><span data-stu-id="ec9eb-136">To apply a bin size, right-click a **Field** and choose **New Group**.</span></span>

![คำสั่งกลุ่มใหม่, รายการเขตข้อมูล, Power BI Desktop](media/desktop-grouping-and-binning/grouping-binning_5.png)

<span data-ttu-id="ec9eb-138">จากกล่องโต้ตอบ **กลุ่ม** แสดง **ขนาดช่องเก็บ** เป็นขนาดที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="ec9eb-138">From the **Groups** dialog box, set the **Bin size** to the size you want.</span></span>

![ขนาดช่องเก็บ, กล่องโต้ตอบกลุ่ม, Power BI Desktop](media/desktop-grouping-and-binning/grouping-binning_6.png)

<span data-ttu-id="ec9eb-140">เมื่อคุณเลือก **ตกลง** คุณจะสังเกตเห็นว่า เขตข้อมูลใหม่ปรากฏในบานหน้าต่าง **เขตข้อมูล** ที่มี **(ช่องเก็บ)** ต่อท้าย</span><span class="sxs-lookup"><span data-stu-id="ec9eb-140">When you select **OK**, you'll notice that a new field appears in the **Fields** pane with **(bins)** appended.</span></span> <span data-ttu-id="ec9eb-141">คุณยังสามารถลากเขตข้อมูลนั้นลงบนพื้นที่ทำงานเพื่อใช้ขนาดช่องเก็บนั้นในวิชวล</span><span class="sxs-lookup"><span data-stu-id="ec9eb-141">You can then drag that field onto the canvas to use the bin size in a visual.</span></span>

![ลากเขตข้อมูลช่องเก็บลงบนพื้นที่ทำงาน, Power BI Desktop](media/desktop-grouping-and-binning/grouping-binning_7.png)

<span data-ttu-id="ec9eb-143">ถ้าต้องการดูสาธิต *การจัดช่องเก็บ* โปรดดูที [วิดีโอ](https://www.youtube.com/watch?v=BRvdZSfO0DY)นี้</span><span class="sxs-lookup"><span data-stu-id="ec9eb-143">To see *binning* in action, take a look at this [video](https://www.youtube.com/watch?v=BRvdZSfO0DY).</span></span>

<span data-ttu-id="ec9eb-144">และนั่นคือทั้งหมดเกี่ยวกับ *การจัดกลุ่ม* และ *การจัดช่องเก็บ* เพื่อให้แน่ใจว่า วิชวลในรายงานของคุณแสดงข้อมูลในแบบที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="ec9eb-144">And that's all there is to using *grouping* and *binning* to ensure the visuals in your reports show your data just the way you want them to.</span></span>
