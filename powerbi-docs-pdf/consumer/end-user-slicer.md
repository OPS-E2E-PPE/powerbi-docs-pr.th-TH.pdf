---
title: การใช้ตัวแบ่งส่วนข้อมูลในบริการ Power BI
description: ตัวแบ่งส่วนข้อมูล Power BI เป็นอีกวิธีหนึ่งของการกรองที่จำกัดส่วนของชุดข้อมูลที่จะแสดงในการแสดงภาพอื่น ๆ ในรายงานให้แคบลง
author: mihart
ms.author: mihart
ms.reviewer: v-thepet
ms.service: powerbi
ms.subservice: pbi-explore
ms.topic: how-to
ms.date: 10/06/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 4ce1105ec646b926e1fabf896ea450029d231131
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96399085"
---
# <a name="slicers-in-the-power-bi-service"></a><span data-ttu-id="40b4a-103">ตัวแบ่งส่วนข้อมูลในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="40b4a-103">Slicers in the Power BI service</span></span>

[!INCLUDE[consumer-appliesto-ynnn](../includes/consumer-appliesto-yynn.md)]

![เปรียบเทียบ 2 รายการเลือกที่แตกต่างกันในตัวแบ่งส่วนข้อมูลแนวนอน](media/end-user-slicer/power-bi-slider.png)

<span data-ttu-id="40b4a-105">ตัวแบ่งส่วนข้อมูลเป็นภาพชนิดหนึ่งที่กรองวิชวลอื่นๆ บนหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="40b4a-105">A slicer is a type of visual that filters the other visuals on a report page.</span></span> <span data-ttu-id="40b4a-106">เมื่อใช้รายงาน Power BI คุณจะพบตัวแบ่งส่วนข้อมูลหลายชนิด</span><span class="sxs-lookup"><span data-stu-id="40b4a-106">When using Power BI reports, you'll discover many types of slicers.</span></span> <span data-ttu-id="40b4a-107">รูปภาพด้านบน แสดงตัวแบ่งส่วนข้อมูลเดียวกัน แต่เป็นรายการเลือกที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="40b4a-107">The image, above, shows the same slicer but with different selections.</span></span> <span data-ttu-id="40b4a-108">ให้สังเกตลักษณะการกรองวิชวลอื่น ๆ บนหน้าของรายการที่เลือกแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="40b4a-108">Notice how each selection filters the other visuals on the page.</span></span>  


## <a name="how-to-use-slicers"></a><span data-ttu-id="40b4a-109">วิธีการใช้ตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="40b4a-109">How to use slicers</span></span>
<span data-ttu-id="40b4a-110">ขณะที่สร้างรายงาน *นักออกแบบ* จะเพิ่มตัวแบ่งส่วนข้อมูลเพื่อช่วยบอกเล่าเรื่องราว และมอบเครื่องมือในการสำรวจข้อมูลของคุณให้แก่คุณ</span><span class="sxs-lookup"><span data-stu-id="40b4a-110">When creating reports, *designers* add slicers to help tell a story and to give you tools to explore your data.</span></span>

### <a name="numeric-range-slicer"></a><span data-ttu-id="40b4a-111">ตัวแบ่งส่วนช่วงตัวเลข</span><span class="sxs-lookup"><span data-stu-id="40b4a-111">Numeric range slicer</span></span>
 <span data-ttu-id="40b4a-112">ตัวแบ่งส่วนข้อมูลช่วงตัวเลขจะช่วยคุณสำรวจข้อมูลเชิงปริมาณ เช่น ยอดขายทั้งหมดตาม: ภูมิศาสตร์, หน่วยในสต็อก และวันที่สั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="40b4a-112">The numeric range slicer helps you explore quantitative data such as total sales by: geography, units in stock, and order date.</span></span> <span data-ttu-id="40b4a-113">ใช้จุดจับเพื่อเลือกช่วง</span><span class="sxs-lookup"><span data-stu-id="40b4a-113">Use the handles to select a range.</span></span> 

![จุดจับสำหรับตัวแบ่งส่วนข้อมูลช่วง](media/end-user-slicer/power-bi-handles.png)

### <a name="basic-vertical-checkbox-slicer"></a><span data-ttu-id="40b4a-115">ตัวแบ่งส่วนข้อมูลของช่องทำเครื่องหมายแนวตั้งพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="40b4a-115">Basic vertical checkbox slicer</span></span>

<span data-ttu-id="40b4a-116">ในตัวแบ่งส่วนข้อมูลของช่องทำเครื่องหมายพื้นฐาน ให้ทำเครื่องหมายที่กล่องช่องทำเครื่องหมายอย่างน้อยหนึ่งกล่อง เพื่อดูผลกระทบเกี่ยวกับวิชวลอื่นๆ บนหน้า</span><span class="sxs-lookup"><span data-stu-id="40b4a-116">In a basic checkbox slicer, select one or more checkboxes to see the impact on the other visuals on the page.</span></span> <span data-ttu-id="40b4a-117">เมื่อต้องการเลือกมากกว่าหนึ่งกล่อง ให้ใช้ CTRL-select</span><span class="sxs-lookup"><span data-stu-id="40b4a-117">To select more than one, use CTRL-select.</span></span> <span data-ttu-id="40b4a-118">ในบางครั้ง *นักออกแบบ* รายงานจะตั้งค่าตัวแบงส่วนข้อมูลเพื่ออนุญาตให้เฉพาะคุณเลือกหนึ่งค่าต่อครั้ง</span><span class="sxs-lookup"><span data-stu-id="40b4a-118">Sometimes, the report *designer* will set the slicer to only allow you to select one value at a time.</span></span> 

![ตัวแบ่งส่วนข้อมูลแนวตั้งพื้นฐาน](media/end-user-slicer/power-bi-basic.png)

### <a name="image-and-shape-slicers"></a><span data-ttu-id="40b4a-120">ตัวแบ่งส่วนรูปภาพและรูปทรง</span><span class="sxs-lookup"><span data-stu-id="40b4a-120">Image and shape slicers</span></span>
<span data-ttu-id="40b4a-121">เมื่อตัวเลือกตัวแบ่งส่วนข้อมูลเป็นรูปภาพหรือรูปทรง ทำให้รายการที่คุณเลือกคล้ายคลึงกับการใช้ช่องทำเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="40b4a-121">When the slicer options are images or shapes, making your selections is similar to using checkboxes.</span></span> <span data-ttu-id="40b4a-122">คุณสามารถเลือกรูปภาพหรือรูปทรงอย่างน้อยหนึ่งภาพที่จะปรับใช้ตัวแบ่งส่วนข้อมูลกับวิชวลอื่นๆ ในหน้าดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="40b4a-122">You can choose one or more image or shape to apply the slicer to the other visuals on the page.</span></span> 

![ตัวแบ่งส่วนข้อมูลรูปภาพ](media/end-user-slicer/power-bi-image.png)    

![ตัวแบ่งส่วนข้อมูลแนวนอน](media/end-user-slicer/power-bi-horizontal.png)    

![ตัวแบ่งส่วนข้อมูลรูปทรง](media/end-user-slicer/power-bi-boxes.png)

### <a name="hierarchy-slicer"></a><span data-ttu-id="40b4a-126">ตัวแบ่งส่วนข้อมูลลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="40b4a-126">Hierarchy slicer</span></span>

<span data-ttu-id="40b4a-127">ในตัวแบ่งส่วนข้อมูลที่มีลำดับชั้น ให้ใช้เครื่องหมายบั้งเพื่อขยายและยุบลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="40b4a-127">In a slicer with a hierarchy, use the chevrons to expand and collapse the hierarchy.</span></span> <span data-ttu-id="40b4a-128">ส่วนหัวจะอัปเดตเพื่อแสดงรายการที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="40b4a-128">The header updates to show your selections.</span></span>

![ตัวแบ่งส่วนข้อมูลลำดับชั้น](media/end-user-slicer/power-bi-hierarchy.png)

### <a name="relative-time-slicer"></a><span data-ttu-id="40b4a-130">ตัวแบ่งส่วนเวลาแบบสัมพัทธ์</span><span class="sxs-lookup"><span data-stu-id="40b4a-130">Relative time slicer</span></span>
<span data-ttu-id="40b4a-131">ด้วยสถานการณ์การรีเฟรชอย่างรวดเร็วที่เกิดขึ้นใหม่ ความสามารถในการกรองไปยังหน้าต่างที่มีขนาดเล็กกว่าจะมีประโยชน์มาก</span><span class="sxs-lookup"><span data-stu-id="40b4a-131">With emerging fast refresh scenarios, the ability to filter to a smaller window of time can be very useful.</span></span>
<span data-ttu-id="40b4a-132">การใช้ตัวแบ่งเวลาแบบสัมพัทธ์จะทำให้คุณสามารถใช้ตัวกรองตามเวลากับข้อมูลวันที่หรือเวลาในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="40b4a-132">Using the relative time slicer, you can apply time-based filters to any date or time data in your report.</span></span> <span data-ttu-id="40b4a-133">ตัวอย่างเช่น คุณสามารถใช้ตัวแบ่งส่วนเวลาแบบสัมพัทธ์ เพื่อแสดงเฉพาะการดูวิดีโอภายใน 2 วัน ชั่วโมง หรือนาทีที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="40b4a-133">For example, you can use the relative time slicer to show only video views within the last 2 days, hours, or even minutes.</span></span> 

![ตัวแบ่งส่วนเวลาแบบสัมพัทธ์](media/end-user-slicer/power-bi-relative-time.png)

## <a name="deactivate-a-slicer"></a><span data-ttu-id="40b4a-135">ปิดใช้งานตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="40b4a-135">Deactivate a slicer</span></span>
<span data-ttu-id="40b4a-136">เมื่อต้องการปิดใช้งานตัวแบ่งส่วนข้อมูล ให้เลือกไอคอนยางลบ</span><span class="sxs-lookup"><span data-stu-id="40b4a-136">To deactivate a slicer, select the eraser icon.</span></span>

![ไอคอนยางลบ](media/end-user-slicer/power-bi-eraser.png)

## <a name="next-steps"></a><span data-ttu-id="40b4a-138">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="40b4a-138">Next steps</span></span>
<span data-ttu-id="40b4a-139">สำหรับข้อมูลเพิ่มเติม ให้ดูบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="40b4a-139">For more information, see the following articles:</span></span>

[<span data-ttu-id="40b4a-140">ชนิดการแสดงภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="40b4a-140">Visualization types in Power BI</span></span>](end-user-visualizations.md)

