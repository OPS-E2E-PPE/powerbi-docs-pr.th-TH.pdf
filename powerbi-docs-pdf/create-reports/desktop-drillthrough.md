---
title: ตั้งค่าการเข้าถึงรายละเอียดในรายงาน Power BI
description: เรียนรู้วิธีใช้การเข้าถึงรายละเอียดเพื่อเจาะลึกข้อมูลในหน้ารายงานใหม่ในรายงาน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 03/12/2020
LocalizationGroup: Create reports
ms.openlocfilehash: cec22acab7cc44b96f3137df04777671964707a8
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414242"
---
# <a name="set-up-drill-through-in-power-bi-reports"></a><span data-ttu-id="ff418-103">ตั้งค่าการเข้าถึงรายละเอียดในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="ff418-103">Set up drill through in Power BI reports</span></span>
<span data-ttu-id="ff418-104">ด้วย *การเข้าถึงรายละเอียด* ในรายงาน Power BI คุณสามารถสร้างหน้าในรายงานของคุณที่มุ่งเน้นไปยังรายการเฉพาะเช่น ผู้จัดหา ลูกค้า หรือผู้ผลิต</span><span class="sxs-lookup"><span data-stu-id="ff418-104">With *drill through* in Power BI reports, you can create a page in your report that focuses on a specific entity such as a supplier, customer, or manufacturer.</span></span> <span data-ttu-id="ff418-105">เมือผู้อ่านรายงานของคุณใช้การเข้าถึงรายละเอียด พวกเขาจะคลิกขวาที่จุดข้อมูลในหน้ารายงานอื่น ๆ แล้วเข้าถึงรายละเอียดในหน้าที่เน้น เพื่อดูรายละเอียดที่กรองตามบริบทดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="ff418-105">When your report readers use drill through, they right-click a data point in other report pages, and drill through to the focused page to get details that are filtered to that context.</span></span> <span data-ttu-id="ff418-106">นอกจากนี้ คุณยังสามารถ[สร้างปุ่มสำหรับการเข้าถึงรายละเอียด](desktop-drill-through-buttons.md) เมื่อพวกเขาคลิกปุ่ม</span><span class="sxs-lookup"><span data-stu-id="ff418-106">You can also [create a button that drills through](desktop-drill-through-buttons.md) to details when they click it.</span></span>

<span data-ttu-id="ff418-107">คุณสามารถตั้งค่าการเข้าถึงรายละเอียดในรายงานของคุณใน Power BI Desktop หรือบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="ff418-107">You can set up drill through in your reports in Power BI Desktop or the Power BI service.</span></span>

![การใช้การเข้าถึงรายละเอียด](media/desktop-drillthrough/power-bi-drill-through-right-click.png)

## <a name="set-up-the-drill-through-destination-page"></a><span data-ttu-id="ff418-109">ตั้งค่าการเข้าถึงรายละเอียดบนหน้าปลายทาง</span><span class="sxs-lookup"><span data-stu-id="ff418-109">Set up the drill-through destination page</span></span>
1. <span data-ttu-id="ff418-110">หากต้องการตั้งค่าการเข้าถึงรายละเอียด ให้สร้างหน้ารายงานที่มีวิชวลที่คุณต้องการสำหรับชนิดของเอนทิตีที่คุณกำลังจะมีการเข้าถึงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="ff418-110">To set up drill through, create a report page that has the visuals you want for the type of entity that you're going to provide drill through for.</span></span> 

    <span data-ttu-id="ff418-111">ตัวอย่างเช่น สมมติว่าคุณต้องการให้มีการเข้าถึงรายละเอียดสำหรับผู้ผลิต</span><span class="sxs-lookup"><span data-stu-id="ff418-111">For example, suppose you want to provide drill through for manufacturers.</span></span> <span data-ttu-id="ff418-112">ในกรณีนี้ คุณอาจสร้างหน้าการเข้าถึงรายละเอียดด้วยวิชวลที่แสดงยอดขายรวม จำนวนหน่วยรวมที่จัดส่ง ยอดขายตามประเภท ยอดขายตามภูมิภาค และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="ff418-112">For this case, you might create a drill-through page with visuals that show total sales, total units shipped, sales by category, sales by region, and so on.</span></span> <span data-ttu-id="ff418-113">ด้วยวิธีดังกล่าว เมื่อคุณเข้าถึงรายละเอียดในหน้านั้น วิชวลจะแสดงให้เห็นเฉพาะผู้ผลิตที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="ff418-113">That way, when you drill through to that page, the visuals are specific to the manufacturer you selected.</span></span>

2. <span data-ttu-id="ff418-114">จากนั้น ในหน้าการเข้าถึงรายละเอียดนั้น ในส่วน **เขตข้อมูล** ของบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล** ให้ลากเขตข้อมูลที่คุณต้องการใช้งานการเข้าถึงรายละเอียดลงในช่อง **ตัวกรองการเข้าถึงรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="ff418-114">Then, on that drill-through page, in the **Fields** section of the **Visualizations** pane, drag the field for which you want to enable drill through into the **Drill-through filters** well.</span></span>

    ![ช่องการเข้าถึงรายละเอียดข้อมูล](media/desktop-drillthrough/drillthrough_02.png)

    <span data-ttu-id="ff418-116">เมื่อคุณเพิ่มเขตข้อมูลไปยัง **ตัวกรองการเข้าถึงรายละเอียด** ตามที่เหมาะสม Power BI ก็จะสร้างวิชวลปุ่ม *ย้อนกลับ* โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ff418-116">When you add a field to the **Drill-through filters** well, Power BI automatically creates a *back* button visual.</span></span> <span data-ttu-id="ff418-117">วิชวลนั้นจะกลายเป็นปุ่มในรายงานที่เผยแพร่</span><span class="sxs-lookup"><span data-stu-id="ff418-117">That visual becomes a button in published reports.</span></span> <span data-ttu-id="ff418-118">ผู้ใช้ที่ช้งานรายงานของคุณในบริการของ Power BI จะใช้ปุ่มนี้เพื่อกลับไปยังหน้ารายงานที่ออกมาได้</span><span class="sxs-lookup"><span data-stu-id="ff418-118">Users who consume your report in the Power BI service use this button to get back to the report page from which they came.</span></span>

    ![รูปภาพการเข้าถึงรายละเอียดข้อมูล](media/desktop-drillthrough/drillthrough_03.png)

> [!IMPORTANT]
> <span data-ttu-id="ff418-120">คุณสามารถกำหนดค่าและดำเนินการเข้าถึงรายละเอียดข้อมูลไปยังหน้าในรายงานเดียวกันได้ อย่างไรก็ตามคุณไม่สามารถเข้าถึงหน้าในรายงานอื่นได้</span><span class="sxs-lookup"><span data-stu-id="ff418-120">You can configure and perform drillthrough to a page in the same report, however, you cannot drillthrough to a page in a different report.</span></span>  



## <a name="use-your-own-image-for-a-back-button"></a><span data-ttu-id="ff418-121">ใช้รูปภาพของคุณเองสำหรับปุ่มย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="ff418-121">Use your own image for a back button</span></span>    
 <span data-ttu-id="ff418-122">เนื่องจากปุ่มย้อนกลับเป็นรูปภาพ คุณสามารถแทนรูปภาพของวิชวลด้วยรูปภาพใดก็ได้ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ff418-122">Because the back button is an image, you can replace the image of that visual with any image you want.</span></span> <span data-ttu-id="ff418-123">รูปภาพดังกล่าวจะยังทำงานเป็นปุ่มย้อนกลับเพื่อให้ผู้ใช้รายงานสามารถกลับไปยังหน้าเดิมได้</span><span class="sxs-lookup"><span data-stu-id="ff418-123">It still operates as a back button so that report consumers can go back to their original page.</span></span> 

<span data-ttu-id="ff418-124">หากต้องการใช้รูปภาพของคุณเองสำหรับปุ่มย้อนกลับ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="ff418-124">To use your own image for a back button, follow these steps:</span></span>

1. <span data-ttu-id="ff418-125">บนแท็บ **หน้าแรก** เลือก **รูปภาพ**</span><span class="sxs-lookup"><span data-stu-id="ff418-125">On the **Home** tab, select **Image**.</span></span> <span data-ttu-id="ff418-126">จากนั้นจึงค้นหารูปภาพของคุณและวางบนหน้าการเข้าถึงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="ff418-126">Then, locate your image and place it on the drill-through page.</span></span>

2. <span data-ttu-id="ff418-127">เลือกรูปภาพใหม่ของคุณบนหน้าการเข้าถึงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="ff418-127">Select your new image on the drill-through page.</span></span> <span data-ttu-id="ff418-128">ภายใต้บานหน้าต่าง **จัดรูปแบบภาพ** ตั้งค่า **ตัวเลื่อนการดำเนินการ** เป็น **เปิด** จากนั้นตั้งค่า **ชนิด** เป็น **ย้อนกลับ**</span><span class="sxs-lookup"><span data-stu-id="ff418-128">Under the **Format image** pane, set the **Action** slider to **On**, and  then set the **Type** to **Back**.</span></span> <span data-ttu-id="ff418-129">รูปของคุณตอนนี้ทำหน้าที่เป็นปุ่มย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="ff418-129">Your image now functions as a back button.</span></span>

    ![โหลดภาพและตั้งค่าชนิดเป็นย้อนกลับ](media/desktop-drillthrough/drillthrough_05.png)

    
     <span data-ttu-id="ff418-131">ในตอนนี้ ผู้ใช้สามารถคลิกขวาบนจุดข้อมูลในรายงานของคุณ และรับเมนูบริบทที่รองรับการเข้าถึงรายละเอียดไปยังหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="ff418-131">Now users can right-click a data point in your report and get a context menu that supports drill through to that page.</span></span> 

    ![เมนูการเข้าถึงรายละเอียด](media/desktop-drillthrough/drillthrough_04.png)

    <span data-ttu-id="ff418-133">เมื่อผู้ใช้รายงานเลือกที่จะเข้าถึงรายละเอียด หน้าจะถูกกรองให้แสดงข้อมูลเกี่ยวกับจุดข้อมูลที่ผู้ใช้คลิกขวา</span><span class="sxs-lookup"><span data-stu-id="ff418-133">When report consumers choose to drill through, the page is filtered to show information about the data point on which they right-clicked.</span></span> <span data-ttu-id="ff418-134">ตัวอย่างเช่น สมมติว่าผู้ใช้คลิกขวาบนจุดข้อมูลที่เกี่ยวกับ Contoso บริษัทผู้ผลิต และเลือกเพื่อดูรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="ff418-134">For example, suppose they right-clicked on a data point about Contoso, a manufacturer, and selected to drill through.</span></span> <span data-ttu-id="ff418-135">หน้าการเข้าถึงรายละเอียดที่ผู้ใช้จะไปจะถูกกรองเป็น Contoso</span><span class="sxs-lookup"><span data-stu-id="ff418-135">The drill-through page they go to is filtered to Contoso.</span></span>

## <a name="pass-all-filters-in-drill-through"></a><span data-ttu-id="ff418-136">ส่งผ่านตัวกรองทั้งหมดในการเข้าถึงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="ff418-136">Pass all filters in drill through</span></span>

<span data-ttu-id="ff418-137">คุณสามารถส่งผ่านตัวกรองที่นำไปใช้ทั้งหมดไปยังหน้าต่างการเข้าถึงรายละเอียดได้</span><span class="sxs-lookup"><span data-stu-id="ff418-137">You can pass all applied filters to the drill-through window.</span></span> <span data-ttu-id="ff418-138">ตัวอย่างเช่น คุณสามารถเลือกเฉพาะผลิตภัณฑ์บางประเภท และวิชวลจะถูกกรองเป็นประเภทนั้น จากนั้นเลือกเข้าถึงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="ff418-138">For example, you can select only a certain category of products and the visuals filtered to that category, and then select drill through.</span></span> <span data-ttu-id="ff418-139">คุณอาจอยากรู้ว่าหน้าการเข้าถึงรายละเอียดมีลักษณะอย่างไรเมื่อใช้ตัวกรองทั้งหมดเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="ff418-139">You might be interested in what that drill through would look like with all those filters applied.</span></span>

<span data-ttu-id="ff418-140">หากต้องการใช้ตัวกรองที่นำไปใช้ทั้งหมดต่อไป ให้ไปที่ส่วน **การเข้าถึงรายละเอียด** ของบานหน้าต่าง **การแสดงภาพ** และตั้งค่า **เก็บตัวกรองทั้งหมด** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="ff418-140">To keep all applied filters, in the **Drill-through** section of the **Visualizations** pane, set **Keep all filters** to **On**.</span></span> 

![เก็บตัวกรองทั้งหมด](media/desktop-drillthrough/drillthrough_06.png)

<span data-ttu-id="ff418-142">เมื่อคุณเข้าถึงรายละเอียดบนวิชวล คุณสามารถดูว่าตัวกรองใดถูกนำไปใช้ ซึ่งเป็นผลจากการที่วิชวลต้นทางมีการใช้ตัวกรองชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="ff418-142">When you then drill through on a visual, you can see which filters were applied as a result of the source visual having temporary filters applied.</span></span> <span data-ttu-id="ff418-143">ในส่วน **การเข้าถึงรายละเอียด** ของบานหน้าต่าง **การแสดงภาพ** ตัวกรองชั่วคราวเหล่านั้นจะแสดงในรูปแบบตัวเอียง</span><span class="sxs-lookup"><span data-stu-id="ff418-143">In the **Drill-through** section of the **Visualization** pane, those transient filters are shown in italics.</span></span> 

![ตัวกรองชั่วคราวในรูปแบบตัวเอียง](media/desktop-drillthrough/drillthrough_07.png)

<span data-ttu-id="ff418-145">แม้ว่าคุณจะสามารถดำเนินการนี้ได้กับหน้าคำแนะนำเครื่องมือ แต่จะเป็นประสบการณ์ที่แปลกเนื่องจากคำแนะนำเครื่องมือจะดูเหมือนทำงานไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="ff418-145">Although you could do this with tooltips pages, that would be an odd experience because the tooltip wouldn't appear to be working properly.</span></span> <span data-ttu-id="ff418-146">ด้วยเหตุนี้จึงไม่แนะนำให้ดำเนินการดังกล่าวกับคำแนะนำเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="ff418-146">For this reason, so doing so with tooltips isn't recommended.</span></span>

## <a name="add-a-measure-to-drill-through"></a><span data-ttu-id="ff418-147">เพิ่มหน่วยวัดไปยังการเข้าถึงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="ff418-147">Add a measure to drill through</span></span>

<span data-ttu-id="ff418-148">นอกเหนือจากการส่งผ่านตัวกรองทั้งหมดไปยังหน้าต่างการเข้าถึงรายละเอียด คุณยังสามารถเพิ่มหน่วยวัดหรือคอลัมน์ตัวเลขสรุปไปยังพื้นที่การเข้าถึงรายละเอียดได้</span><span class="sxs-lookup"><span data-stu-id="ff418-148">Besides passing all filters to the drill-through window, you can also add a measure or a summarized numeric column to the drill-through area.</span></span> <span data-ttu-id="ff418-149">ลากเขตข้อมูลการเข้าถึงรายละเอียดไปยังการ์ด **การเข้าถึงรายละเอียด** เพื่อนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="ff418-149">Drag the drill-through field to the **Drill-through** card to apply it.</span></span> 

![เพิ่มหน่วยวัดไปยังการเข้าถึงรายละเอียด](media/desktop-drillthrough/drillthrough_08.png)

<span data-ttu-id="ff418-151">เมื่อคุณเพิ่มหน่วยวัดหรือคอลัมน์ตัวเลขสรุป คุณสามารถเข้าถึงรายละเอียดไปยังหน้าเมื่อเขตข้อมูลถูกใช้ในพื้นที่ *ค่า* ของวิชวลได้</span><span class="sxs-lookup"><span data-stu-id="ff418-151">When you add a measure or summarized numeric column, you can drill through to the page when the field is used in the *Value* area of a visual.</span></span>

<span data-ttu-id="ff418-152">ทั้งหมดนั้นคือวิธีการใช้งานการเข้าถึงรายละเอียดในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="ff418-152">That's all there is to using drill through in your reports.</span></span> <span data-ttu-id="ff418-153">ซึ่งเป็นวิธีการที่ยอดเยี่ยมในการดูข้อมูลเอนทิตี้ในมุมมองขยาย ตามข้อมูลคุณเลือกไว้สำหรับตัวกรองการเข้าถึงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="ff418-153">It's a great way to get an expanded view of the entity information that you selected for your drill-through filter.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ff418-154">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="ff418-154">Next steps</span></span>

<span data-ttu-id="ff418-155">คุณอาจมีความสนใจบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ff418-155">You might also be interested in the following articles:</span></span>

* [<span data-ttu-id="ff418-156">ใช้การเข้าถึงรายละเอียดแบบข้ามรายงานในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="ff418-156">Use cross-report drill through in Power BI reports</span></span>](desktop-cross-report-drill-through.md)
* [<span data-ttu-id="ff418-157">การใช้ตัวแบ่งส่วนข้อมูล Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ff418-157">Using slicers Power BI Desktop</span></span>](../visuals/power-bi-visualization-slicers.md)
