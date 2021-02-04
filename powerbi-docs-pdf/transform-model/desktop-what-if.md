---
title: ใช้พารามิเตอร์ What if (เกิดอะไรขึ้นถ้า) เพื่อแสดงภาพตัวแปร
description: สร้างตัวแปร What-if ของคุณเองเพื่อจินตนาการและสร้างภาพตัวแปรในรายงาน Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: how-to
ms.date: 01/21/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 2286edc16995e8fecc3b6ff65a53e2c4007ac470
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415438"
---
# <a name="create-and-use-what-if-parameters-to-visualize-variables-in-power-bi-desktop"></a><span data-ttu-id="8966a-103">สร้างและใช้พารามิเตอร์ what-if เพื่อแสดงตัวแปรวิชวลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="8966a-103">Create and use what-if parameters to visualize variables in Power BI Desktop</span></span>

<span data-ttu-id="8966a-104">เริ่มต้นด้วย *Power BI Desktop* รุ่นเผยแพร่เดือนสิงหาคม 2018 คุณสามารถสร้างตัวแปร *เกิดอะไรขึ้นถ้า* สำหรับรายงานของคุณ โต้ตอบกับตัวแปรในฐานะเป็นตัวแบ่งส่วนข้อมูล และแสดงภาพ และกำหนดปริมาณค่าที่สำคัญต่าง ๆ ในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="8966a-104">Starting with the August 2018 release of *Power BI Desktop*, you can create *what-if* variables for your reports, interact with the variable as a slicer, and visualize and quantify different key values in your reports.</span></span>

![ตัวเลือกพารามิเตอร์ใหม่](media/desktop-what-if/what-if_01.png)

<span data-ttu-id="8966a-106">สร้างพารามิเตอร์ *What-if* อยู่บนแท็บ **การวางรูปแบบ** ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="8966a-106">Create a *what-if* parameter on the **Modeling** tab in Power BI Desktop.</span></span> <span data-ttu-id="8966a-107">เมื่อคุณเลือก กล่องโต้ตอบจะปรากฏขึ้น ซึ่งคุณสามารถกำหนดค่าพารามิเตอร์ได้</span><span class="sxs-lookup"><span data-stu-id="8966a-107">When you select it, a dialog box appears where you can configure the parameter.</span></span>

## <a name="creating-a-what-if-parameter"></a><span data-ttu-id="8966a-108">การสร้างพารามิเตอร์ What-if</span><span class="sxs-lookup"><span data-stu-id="8966a-108">Creating a what-if parameter</span></span>

<span data-ttu-id="8966a-109">เมื่อต้องสร้างพารามิเตอร์ What-if (เกิดอะไรขึ้นถ้า) ให้เลือก **พารามิเตอร์ใหม่** จากแท็บ **การสร้างแบบจำลอง** ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="8966a-109">To create a what-if parameter, select **New Parameter** from the **Modeling** tab in Power BI Desktop.</span></span> <span data-ttu-id="8966a-110">ในรูปต่อไปนี้ เราได้สร้างพารามิเตอร์ที่เรียกว่า *เปอร์เซ็นต์ส่วนลด* และตั้งค่าชนิดข้อมูลเป็น **เลขทศนิยม**</span><span class="sxs-lookup"><span data-stu-id="8966a-110">In the following image, we've created a parameter called *Discount percentage* and set its data type to **Decimal number**.</span></span> <span data-ttu-id="8966a-111">ค่า **ต่ำสุด** คือศูนย์</span><span class="sxs-lookup"><span data-stu-id="8966a-111">The **Minimum** value is zero.</span></span> <span data-ttu-id="8966a-112">ค่า **สูงสุด** คือ 0.50 (50 เปอร์เซ็นต์)</span><span class="sxs-lookup"><span data-stu-id="8966a-112">The **Maximum** is 0.50 (50 percent).</span></span> <span data-ttu-id="8966a-113">นอกจากนี้ เรายังได้ตั้งค่า **ส่วนเพิ่ม** เป็น 0.05 หรือห้าเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="8966a-113">We've also set the **Increment** to 0.05, or five percent.</span></span> <span data-ttu-id="8966a-114">นั่นคือจำนวนที่พารามิเตอร์จะปรับเปลี่ยนเมื่อมีการโต้ตอบในรายงาน</span><span class="sxs-lookup"><span data-stu-id="8966a-114">That's how much the parameter will adjust when interacted with in a report.</span></span>

![ค่าพารามิเตอร์ What-if](media/desktop-what-if/what-if_02.png)

> [!NOTE]
> <span data-ttu-id="8966a-116">สำหรับตัวเลขทศนิยม ตรวจสอบให้แน่ใจว่าคุณเติมข้างหน้าด้วยศูนย์ เป็น 0.50 แทนที่จะเป็น .50</span><span class="sxs-lookup"><span data-stu-id="8966a-116">For decimal numbers, make sure you precede the value with a zero, as in 0.50 versus just .50.</span></span> <span data-ttu-id="8966a-117">มิฉะนั้น ตัวเลขดังกล่าวจะไม่ผ่านการตรวจสอบ และจะไม่สามารถเลือกปุ่ม **ตกลง** ได้</span><span class="sxs-lookup"><span data-stu-id="8966a-117">Otherwise, the number won't validate and the **OK** button won't be selectable.</span></span>
> 
> 

<span data-ttu-id="8966a-118">เพื่อความสะดวกของคุณ กล่อง **เพิ่มตัวแบ่งส่วนข้อมูลไปยังหน้านี้** จะวางตัวแบ่งส่วนข้อมูลและพารามิเตอร์ What-if (เกิดอะไรขึ้นถ้า) ลงบนหน้ารายงานปัจจุบันโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="8966a-118">For your convenience, the **Add slicer to this page** checkbox automatically puts a slicer with your what-if parameter onto the current report page.</span></span>

![ตัวแบ่งส่วนข้อมูลใหม่บนหน้ารายงานปัจจุบัน](media/desktop-what-if/what-if_03.png)

<span data-ttu-id="8966a-120">นอกจากการสร้างพารามิเตอร์แล้ว การสร้างพารามิเตอร์ What-if (เกิดอะไรขึ้นถ้า) จะสร้างหน่วยวัดด้วย ซึ่งคุณสามารถใช้เพื่อแสดงค่าปัจจุบันของ พารามิเตอร์ What-if ได้</span><span class="sxs-lookup"><span data-stu-id="8966a-120">In addition to creating the parameter, creating a what-if parameter also creates a measure, which you can use to visualize the current value of the what-if parameter.</span></span>

![หน่วยวัดที่สร้างขึ้นสำหรับพารามิเตอร์ What-if](media/desktop-what-if/what-if_04.png)

<span data-ttu-id="8966a-122">การทราบว่าเมื่อคุณสร้างพารามิเตอร์ What-if ขึ้น ทั้งพารามิเตอร์และหน่วยวัดจะกลายเป็นส่วนหนึ่งของแบบจำลองของคุณนั้นเป็นสิ่งสำคัญและเป็นประโยชน์</span><span class="sxs-lookup"><span data-stu-id="8966a-122">It's important and useful to note that once you create a what-if parameter, both the parameter and the measure become part of your model.</span></span> <span data-ttu-id="8966a-123">พารามิเตอร์จะพร้อมใช้งานตลอดทั้งรายงาน และสามารถใช้ได้บนหน้ารายงานอื่น ๆ ด้วย</span><span class="sxs-lookup"><span data-stu-id="8966a-123">So, they're available throughout the report and can be used on other report pages.</span></span> <span data-ttu-id="8966a-124">และเนื่องจากเป็นส่วนหนึ่งของแบบจำลอง คุณสามารถลบตัวแบ่งข้อมูลออกจากหน้ารายงานได้</span><span class="sxs-lookup"><span data-stu-id="8966a-124">And, since they're part of the model, you can delete the slicer from the report page.</span></span> <span data-ttu-id="8966a-125">ถ้าคุณต้องการย้อนกลับ เพียงเลือกพารามิเตอร์ What-if จากรายการ **เขตข้อมูล** แล้วลากไปยังพื้นที่ทำงาน จากนั้น เปลี่ยนวิชวลเป็นตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8966a-125">If you want it back, just grab the what-if parameter from the **Fields** list and drag it onto the canvas, then change the visual to a slicer.</span></span>

## <a name="using-a-what-if-parameter"></a><span data-ttu-id="8966a-126">การใช้พารามิเตอร์ What-If</span><span class="sxs-lookup"><span data-stu-id="8966a-126">Using a what-if parameter</span></span>

<span data-ttu-id="8966a-127">เรามาสร้างตัวอย่างง่าย ๆ ของการใช้พารามิเตอร์ What-if กัน</span><span class="sxs-lookup"><span data-stu-id="8966a-127">Let's create a simple example of using a what-if parameter.</span></span> <span data-ttu-id="8966a-128">เราได้สร้างพารามิเตอร์ What-if ในส่วนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="8966a-128">We created the what-if parameter in the previous section.</span></span> <span data-ttu-id="8966a-129">ในตอนนี้ เราจะนำไปใช้โดยการสร้างหน่วยวัดใหม่ที่มีการปรับค่าด้วยแถบเลื่อน</span><span class="sxs-lookup"><span data-stu-id="8966a-129">Now we'll put it to use by creating a new measure whose value adjusts with the slider.</span></span>

![เพิ่มหน่วยวัดใหม่เพื่อใช้กับพารามิเตอร์](media/desktop-what-if/what-if_05.png)

<span data-ttu-id="8966a-131">หน่วยวัดใหม่ดังกล่าวจะเป็นยอดขายรวมที่มีการนำอัตราส่วนลดมาใช้</span><span class="sxs-lookup"><span data-stu-id="8966a-131">The new measure is simply going to be the total sales amount, with the discount rate applied.</span></span> <span data-ttu-id="8966a-132">คุณสามารถสร้างหน่วยวัดที่มีความซับซ้อนและน่าสนใจได้ แน่นอนว่านั่นช่วยให้ผู้ใช้รายงานของคุณสร้างภาพตัวแปรของพารามิเตอร์ What-if ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="8966a-132">You can create complex and interesting measures that let the consumers of your reports visualize the variable of your what-if parameter.</span></span> <span data-ttu-id="8966a-133">ตัวอย่างเช่น คุณสามารถสร้างรายงานที่ทำให้ผู้ขายเห็นค่าตอบแทนของตนถ้าสามารถขายได้ตรงตามเป้าหมายหรือเปอร์เซ็นต์ยอดขายที่ตั้งไว้ หรือดูผลกระทบต่อการขายที่เพิ่มขึ้นเมื่อส่วนลดเพิ่มมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="8966a-133">For example, you could create a report that lets sales people see their compensation if they meet certain sales goals or percentages, or see the effect of increased sales to deeper discounts.</span></span>

<span data-ttu-id="8966a-134">ป้อนสูตรหน่วยวัดลงในแถบสูตร และตั้งชื่อเป็น *ยอดขายหลังจากส่วนลด*</span><span class="sxs-lookup"><span data-stu-id="8966a-134">Enter the measure formula into the formula bar, and name the formula *Sales after Discount*.</span></span>

![ข้อกำหนดของยอดขายหลังจากส่วนลด](media/desktop-what-if/what-if_06.png)

<span data-ttu-id="8966a-136">จากนั้น เราสร้างวิชวลคอลัมน์ที่มี **OrderDate** บนแกน และทั้ง **SalesAmount** และหน่วยวัดที่เพิ่งสร้างขึ้นนั่นคือ **ยอดขายหลังจากส่วนลด** เป็นค่า</span><span class="sxs-lookup"><span data-stu-id="8966a-136">Then, we create a column visual with **OrderDate** on the axis, and both **SalesAmount** and the just-created measure, **Sales after Discount** as the values.</span></span>

![การแสดงภาพสำหรับ SalesAmount](media/desktop-what-if/what-if_07.png)

<span data-ttu-id="8966a-138">จากนั้น เมื่อเราเลื่อนแถบเลื่อน เราจะเห็นว่าคอลัมน์ **ยอดขายหลังจากส่วนลด** แสดงปริมาณยอดขายหลังหักส่วนลด</span><span class="sxs-lookup"><span data-stu-id="8966a-138">Then, as we move the slider, we see that the **Sales after Discount** column reflects the discounted sales amount.</span></span>

![แถบเลื่อนโต้ตอบกับการแสดงภาพ](media/desktop-what-if/what-if_08.png)

<span data-ttu-id="8966a-140">และทั้งหมดก็มีแค่นั้นจริง ๆ</span><span class="sxs-lookup"><span data-stu-id="8966a-140">And, that's all there is to it.</span></span> <span data-ttu-id="8966a-141">คุณสามารถใช้พารามิเตอร์ What-if ได้ในสถานการณ์ทุกประเภท</span><span class="sxs-lookup"><span data-stu-id="8966a-141">You can use what-if parameters in all sorts of situations.</span></span> <span data-ttu-id="8966a-142">พารามิเตอร์เหล่านี้จะทำให้ผู้ใช้รายงานสามารถโต้ตอบกับสถานการณ์สมมติต่างๆ ที่คุณได้สร้างไว้ในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="8966a-142">These parameters enable the consumers of reports to interact with different scenarios that you create in your reports.</span></span>
