---
title: สมาชิกเริ่มต้นในแบบจำลองหลายมิติใน Power BI
description: เรียนรู้วิธีการทำงานของ Power BI เมื่อทำงานกับสมาชิกเริ่มต้นในแบบจำลองหลายมิติ
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: conceptual
ms.date: 01/10/2019
LocalizationGroup: Data from files
ms.openlocfilehash: 333651ad89e50a3debe73dfdafc0dced865553a5
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96405456"
---
# <a name="work-with-multidimensional-models-in-power-bi"></a><span data-ttu-id="6913e-103">ทำงานกับแบบจำลองหลายมิติใน Power BI</span><span class="sxs-lookup"><span data-stu-id="6913e-103">Work with multidimensional models in Power BI</span></span>

<span data-ttu-id="6913e-104">คุณสามารถเชื่อมต่อกับแบบจำลองหลายมิติใน Power BI และสร้างรายงานที่แสดงภาพข้อมูลทั้งหมดภายในแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="6913e-104">You can connect to multidimensional models in Power BI, and create reports that visualize all sorts of data within the model.</span></span> <span data-ttu-id="6913e-105">เมื่อทำงานกับแบบจำลองหลายมิติ Power BI จะใช้กฎวิธีการประมวลผลข้อมูล โดยยึดตามคอลัมน์ที่กำหนดเป็นคำ *สมาชิกเริ่มต้น*</span><span class="sxs-lookup"><span data-stu-id="6913e-105">When working with multidimensional models, Power BI applies rules to how it processes data, based on which column is defined as the *default member*.</span></span> 

<span data-ttu-id="6913e-106">เมื่อทำงานกับแบบจำลองหลายมิติ Power BI จัดการข้อมูลจากแบบจำลองตามจุดคอลัมน์ที่มีการใช้ **DefaultMember**</span><span class="sxs-lookup"><span data-stu-id="6913e-106">When working with multidimensional models, Power BI handles data from the model based on where the column that contains the **DefaultMember** is used.</span></span> <span data-ttu-id="6913e-107">แอตทริบิวต์ *DefaultMember* จะถูกตั้งค่าใน CSDL (Conceptual Schema Definition Language) สำหรับคอลัมน์เฉพาะในแบบจำลองหลายมิติ</span><span class="sxs-lookup"><span data-stu-id="6913e-107">The *DefaultMember* attribute is set in CSDL (Conceptual Schema Definition Language) for a particular column in a multidimensional model.</span></span> <span data-ttu-id="6913e-108">คุณสามารถเรียนรู้เพิ่มเติมเกี่ยวกับสมาชิกเริ่มต้นใน[บทความคุณสมบัติแอตทริบิวต์](/sql/analysis-services/multidimensional-models/attribute-properties-define-a-default-member?view=sql-server-2017)ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="6913e-108">You can learn more about the default member in its [attribute properties article](/sql/analysis-services/multidimensional-models/attribute-properties-define-a-default-member?view=sql-server-2017).</span></span> <span data-ttu-id="6913e-109">เมื่อดำเนินการคิวรี DAX สมาชิกเริ่มต้นที่ระบุในแบบจำลองจะถูกนำไปใช้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6913e-109">When a DAX query is executed, the default member specified in the model is applied automatically.</span></span>

<span data-ttu-id="6913e-110">บทความนี้อธิบายวิธีการทำงานของ Power BI ภายใต้สถานการณ์ต่าง ๆ เมื่อทำงานกับแบบจำลองหลายมิติ โดยอิงตามตำแหน่งที่พบ *สมาชิกเริ่มต้น*</span><span class="sxs-lookup"><span data-stu-id="6913e-110">This article described how Power BI behaves under various circumstances when working with multidimensional models, based on where the *default member* is found.</span></span> 

## <a name="working-with-filter-cards"></a><span data-ttu-id="6913e-111">การทำงานกับบัตรตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="6913e-111">Working with filter cards</span></span>

<span data-ttu-id="6913e-112">เมื่อสร้างบัตรตัวกรองบนเขตข้อมูลที่มีสมาชิกเริ่มต้น ค่าเขตข้อมูลของสมาชิกเริ่มต้นจะถูกเลือกโดยอัตโนมัติในบัตรตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="6913e-112">When creating a filter card on a field with a default member, the default member field value is selected automatically in the filter card.</span></span> <span data-ttu-id="6913e-113">ผลลัพธ์คือ วิชวลทั้งหมดที่ได้รับผลกระทบจากบัตรตัวกรองจะรักษาแบบจำลองเริ่มต้นในฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6913e-113">The result is that all visuals that are affected by the filter card retain their default models in the database.</span></span> <span data-ttu-id="6913e-114">ค่าต่าง ๆ ในบัตรตัวกรองดังกล่าวจะแสดงเป็นสมาชิกเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6913e-114">The values in such filter cards reflect that default member.</span></span>

<span data-ttu-id="6913e-115">หากลบสมาชิกเริ่มต้น การยกเลิกการเลือกค่าจะล้างออกเพื่อวิชวลทั้งหมดสำหรับใช้บัตรตัวกรอง และค่าที่แสดงจะไม่แสดงสมาชิกเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6913e-115">If the default member is removed, de-selecting the value clears it for all visuals to which the filter card applies, and the values displayed do not reflect the default member.</span></span>

<span data-ttu-id="6913e-116">เช่น สมมติว่าเรามีคอลัมน์ *สกุลเงิน* ที่มีสมาชิกเริ่มต้นซึ่งตั้งค่าเป็น *USD*:</span><span class="sxs-lookup"><span data-stu-id="6913e-116">For example, imagine we have a *Currency* column that has a default member set to *USD*:</span></span>

* <span data-ttu-id="6913e-117">ในกรณีตัวอย่างนี้ หากเรามีบัตรที่แสดง *ยอดขายรวม* ค่าจะมีสมาชิกเริ่มต้นที่นำไปใช้ และเราจะเห็นยอดขายที่สอดคล้องกับสกุลเงิน "USD"</span><span class="sxs-lookup"><span data-stu-id="6913e-117">In this example case, if we have a card that shows *Total Sales*, the value will have the default member applied and we see sales that correspond to "USD".</span></span>
* <span data-ttu-id="6913e-118">หากเราลาก *สกุลเงิน* ไปยังบานหน้าต่างบัตรตัวกรอง เราจะเห็น *USD* เป็นค่าเริ่มต้นที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="6913e-118">If we drag *Currency* to the filter card pane, we see *USD* as the default value selected.</span></span> <span data-ttu-id="6913e-119">ค่าของ *ยอดขายรวม* จะยังคงเหมือนเดิม เนื่องจากมีการใช้สมาชิกเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6913e-119">The value of *Total Sales* remains the same, since the default member is applied.</span></span>
* <span data-ttu-id="6913e-120">อย่างไรก็ตาม หากเรายกเลิกการเลือกค่า *USD* จากบัตรตัวกรอง สมาชิกเริ่มต้นสำหรับ *สกุลเงิน* จะถูกล้างออก และตอนนี้ *ยอดขายรวม* จะแสดงสกุลเงินทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6913e-120">However, if we deselect the *USD* value from the filter card, the default member for *Currency* is cleared, and now *Total Sales* reflects all currencies.</span></span>
* <span data-ttu-id="6913e-121">ดังนั้น เมื่อเราเลือกค่าอื่นในบัตรตัวกรอง (สมมติว่าเราเลือก *EURO*) *ยอดขายรวม* จะแสดงตัวกรอง *สกุลเงินเป็น {USD, EURO}* ในสมาชิกเริ่มต้นทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6913e-121">Consequently, when we select another value in the filter card (let's say we select *EURO*), along the default member, the *Total Sales* reflects the filter *Currency IN {USD, EURO}*.</span></span>

## <a name="grouping-behavior"></a><span data-ttu-id="6913e-122">การจัดกลุ่มลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="6913e-122">Grouping behavior</span></span>

<span data-ttu-id="6913e-123">ใน Power BI ทุกครั้งที่คุณจัดกลุ่มวิชวลบนคอลัมน์ที่มี *สมาชิกเริ่มต้น* Power BI จะล้าง *สมาชิกเริ่มต้น* สำหรับคอลัมน์ดังกล่าวและเส้นทางความสัมพันธ์ของแอตทริบิวต์</span><span class="sxs-lookup"><span data-stu-id="6913e-123">In Power BI, whenever you group a visual on a column that has a *default member*, Power BI clears the *default member* for that column and its attribute relationship path.</span></span> <span data-ttu-id="6913e-124">ซึ่งทำให้แน่ใจวิชวลจะแสดงค่าทั้งหมดที่ไม่ใช่แค่เฉพาะค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6913e-124">This ensures the visual displays all values, rather than just the default values.</span></span>

## <a name="attribute-relationship-paths-arps"></a><span data-ttu-id="6913e-125">เส้นทางความสัมพันธ์ของแอตทริบิวต์ (ARP)</span><span class="sxs-lookup"><span data-stu-id="6913e-125">Attribute relationship paths (ARPs)</span></span>

<span data-ttu-id="6913e-126">เส้นทางความสัมพันธ์ของแอตทริบิวต์ (ARP) จะมี *สมาชิกเริ่มต้น* พร้อมความสามารถที่มีประสิทธิภาพ แต่ยังคงมีความซับซ้อนอยู่ส่วนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6913e-126">Attribute relationship paths (ARPs) provide *default members* with powerful capabilities, but also introduce a certain amount of complexity.</span></span> <span data-ttu-id="6913e-127">เมื่อตรวจพบ ARP, Power BI จะติดตามเส้นทางของ ARP เพื่อล้างสมาชิกเริ่มต้นเพิ่มเติมสำหรับคอลัมน์อื่น ๆ เพื่อให้การจัดการข้อมูลสำหรับวิชวลมีความสอดคล้องและแม่นยำ</span><span class="sxs-lookup"><span data-stu-id="6913e-127">When ARPs are encounter, Power BI follows the path of ARPs to clear additional default members for other columns, to provide consistent, and precise handling of data for visuals.</span></span>

<span data-ttu-id="6913e-128">ลองดูตัวอย่างเพื่อทำความเข้าใจลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="6913e-128">Let's look at an example to clarify the behavior.</span></span> <span data-ttu-id="6913e-129">พิจารณาการกำหนดค่าของ ARP ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6913e-129">Consider the following configuration of ARPs:</span></span>

![ARP ในแบบจำลองหลายมิติ](media/desktop-default-member-multidimensional-models/default-members_01.png)

<span data-ttu-id="6913e-131">ตอนนี้ลองจินตนาการ *สมาชิกเริ่มต้น* ต่อไปนี้ที่ตั้งค่าสำหรับคอลัมน์เหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="6913e-131">Now let's imagine the following *default members* are set for these columns:</span></span>

* <span data-ttu-id="6913e-132">เมือง > ซีแอตเทิล</span><span class="sxs-lookup"><span data-stu-id="6913e-132">City > Seattle</span></span>
* <span data-ttu-id="6913e-133">รัฐ > วอชิงตัน</span><span class="sxs-lookup"><span data-stu-id="6913e-133">State > WA</span></span>
* <span data-ttu-id="6913e-134">ประเทศ > สหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="6913e-134">Country > US</span></span>
* <span data-ttu-id="6913e-135">ประชากร > ขนาดใหญ่</span><span class="sxs-lookup"><span data-stu-id="6913e-135">Population > Large</span></span>

<span data-ttu-id="6913e-136">ตอนนี้ลองตรวจสอบสิ่งที่เกิดขึ้นเมื่อแต่ละคอลัมน์ที่ถูกใช้ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="6913e-136">Now let's examine what happens when each of the columns is used in Power BI.</span></span> <span data-ttu-id="6913e-137">เมื่อวิชวลจับกลุ่มบนคอลัมน์ต่อไปนี้ จึงเกิดผลลัพธ์ต่าง ๆ ดังนี้:</span><span class="sxs-lookup"><span data-stu-id="6913e-137">When visuals group on the following columns, here are the results:</span></span>

* <span data-ttu-id="6913e-138">**เมือง** - Power BI แสดงเมืองทั้งหมด โดยล้าง **สมาชิกเริ่มต้น** ทั้งหมดสำหรับ *เมือง* *รัฐ* *ประเทศ* แต่ไม่ล้าง **สมาชิกเริ่มต้น** สำหรับ *ประชากร* เนื่องจาก Power BI ได้ล้าง ARP ทั้งหมดสำหรับ *เมือง* แล้ว</span><span class="sxs-lookup"><span data-stu-id="6913e-138">**City** - Power BI displays all the cities by clearing all the **default members** for *City*, *State*, *Country* but preserves the **default member** for *Population*; Power BI cleared the entire ARP for *City*.</span></span>
    > [!NOTE]
    > <span data-ttu-id="6913e-139">*ประชากร* ไม่อยู่ในเส้นทาง ARP ของ *เมือง* ซึ่งเกี่ยวข้องกับ *รัฐ* เพียงอย่างเดียว ดังนั้น Power BI จึงไม่ได้ล้างค่า</span><span class="sxs-lookup"><span data-stu-id="6913e-139">*Population* is not in the ARP path of *City*, it is solely related to *State* and thus Power BI doesn't clear it.</span></span>
* <span data-ttu-id="6913e-140">**รัฐ** - Power BI แสดง *รัฐ* ทั้งหมดโดยล้าง **สมาชิกเริ่มต้น** ทั้งหมดสำหรับ *เมือง* *รัฐ* *ประเทศ* และ *ประชากร*</span><span class="sxs-lookup"><span data-stu-id="6913e-140">**State** - Power BI displays all the *States* by clearing all **default members** for *City*, *State*, *Country* and *Population*.</span></span>
* <span data-ttu-id="6913e-141">**ประเทศ** - Power BI แสดงประเทศทั้งหมด โดยล้าง **สมาชิกเริ่มต้น** ทั้งหมดสำหรับ *เมือง* *รัฐ* *ประเทศ* แต่ไม่ล้าง **สมาชิกเริ่มต้น** สำหรับ *ประชากร*</span><span class="sxs-lookup"><span data-stu-id="6913e-141">**Country** - Power BI displays all the countries by clearing all **default members** for *City*, *State* and *Country*, but preserves the **default member** for *Population*.</span></span>
* <span data-ttu-id="6913e-142">**เมืองและรัฐ** - Power BI จะล้าง **สมาชิกเริ่มต้น** ทั้งหมดสำหรับคอลัมน์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6913e-142">**City and State** - Power BI clears all **default members** for all columns.</span></span>

<span data-ttu-id="6913e-143">กลุ่มที่แสดงในวิชวลมีเส้นทาง ARP ทั้งหมดที่ถูกล้างแล้ว</span><span class="sxs-lookup"><span data-stu-id="6913e-143">Groups displayed in the visual have their entire ARP path cleared.</span></span> 

<span data-ttu-id="6913e-144">หากมีกลุ่มหนึ่งไม่แสดงในวิชวล แต่เป็นส่วนหนึ่งของเส้นทาง ARP บนคอลัมน์ที่จัดกลุ่มอื่น จะมีสิ่งต่อไปนี้เกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="6913e-144">If a group is not displayed in the visual, but is part of the ARP path of another grouped-on column, the following applies:</span></span>

* <span data-ttu-id="6913e-145">เส้นทาง ARP บางสาขาจะถูกล้างออกโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6913e-145">Not all branches of the ARP path are cleared automatically.</span></span>
* <span data-ttu-id="6913e-146">กลุ่มดังกล่าวจะยังคงถูกกรองโดย **สมาชิกเริ่มต้น** ที่ยังไม่ได้ล้าง</span><span class="sxs-lookup"><span data-stu-id="6913e-146">That group is still filtered by that uncleared **default member**.</span></span>

### <a name="slicers-and-filter-cards"></a><span data-ttu-id="6913e-147">ตัวแบ่งส่วนข้อมูลและบัตรตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="6913e-147">Slicers and filter cards</span></span>

<span data-ttu-id="6913e-148">เมื่อทำงานกับตัวแบ่งส่วนข้อมูลหรือบัตรตัวกรอง จะมีลักษณะการทำงานต่อไปนี้เกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="6913e-148">When working with slicers or filter cards, the following behavior occurs:</span></span>

* <span data-ttu-id="6913e-149">เมื่อป้อนข้อมูลลงในตัวแบ่งส่วนข้อมูลหรือบัตรตัวกรอง Power BI จะจัดกลุ่มบนคอลัมน์ในวิชวล เพื่อให้การแสดงลักษณะการทำงานเหมือนกับที่อธิบายไว้ในส่วนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="6913e-149">When a slicer or filter card is loaded with data, Power BI groups on the column in the visual, so the display behavior is the same as described in the previous section.</span></span>

<span data-ttu-id="6913e-150">เนื่องจากตัวแบ่งส่วนข้อมูลและบัตรตัวกรองมักใช้เพื่อโต้ตอบกับวิชวลอื่น ๆ ตรรกะของการล้าง **สมาชิกเริ่มต้น** สำหรับวิชวลที่ได้รับผลกระทบจะเกิดขึ้นตามที่อธิบายไว้ในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6913e-150">Since slicers and filter cards are often used to interact with other visuals, the logic of clearing **default members** for the affected visuals occurs as explained in the following table.</span></span> 

<span data-ttu-id="6913e-151">สำหรับตารางนี้ เราใช้ข้อมูลตัวอย่างเดียวกันกับที่ใช้ก่อนหน้าในบทความนี้:</span><span class="sxs-lookup"><span data-stu-id="6913e-151">For this table, we use the same example data used earlier in this article:</span></span>

![การล้างลักษณะการทำงานหรือสมาชิกเริ่มต้นของ Power BI ด้วยตัวแบ่งส่วนข้อมูลและบัตรตัวกรอง](media/desktop-default-member-multidimensional-models/default-members_02.png)

<span data-ttu-id="6913e-153">กฎต่อไปนี้จะใช้กับวิธีการทำงานของ Power BI ในสถานการณ์เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="6913e-153">The following rules apply for how Power BI behaves in these circumstances.</span></span>

<span data-ttu-id="6913e-154">Power BI จะล้าง **สมาชิกเริ่มต้น** สำหรับคอลัมน์ที่มีให้หาก:</span><span class="sxs-lookup"><span data-stu-id="6913e-154">Power BI clears a **default member** for a given column if:</span></span>

* <span data-ttu-id="6913e-155">Power BI จัดกลุ่มบนคอลัมน์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="6913e-155">Power BI groups on that column</span></span>
* <span data-ttu-id="6913e-156">Power BI จัดกลุ่มบนคอลัมน์ที่เกี่ยวข้องกับคอลัมน์ดังกล่าว (ทุกที่ใน ARP ขึ้นหรือลง)</span><span class="sxs-lookup"><span data-stu-id="6913e-156">Power BI groups on a column related to that column (anywhere in the ARP, up or down)</span></span>
* <span data-ttu-id="6913e-157">Power BI กรองคอลัมน์ที่อยู่ใน ARP (ขึ้นหรือลง)</span><span class="sxs-lookup"><span data-stu-id="6913e-157">Power BI filters on a column that is in the ARP (up or down)</span></span>
* <span data-ttu-id="6913e-158">คอลัมน์มีบัตรตัวกรองที่มีรัฐ *ทั้งหมด*</span><span class="sxs-lookup"><span data-stu-id="6913e-158">The column has a filter card with *ALL* state</span></span>
* <span data-ttu-id="6913e-159">คอลัมน์มีบัตรตัวกรองที่มีค่าใด ๆ ที่เลือกไว้ (Power BI ได้รับตัวกรองสำหรับคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="6913e-159">The column has a filter card with any value selected (Power BI receives a filter for the column)</span></span>

<span data-ttu-id="6913e-160">Power BI ไม่ล้าง **สมาชิกเริ่มต้น** สำหรับคอลัมน์ที่มีให้หาก:</span><span class="sxs-lookup"><span data-stu-id="6913e-160">Power BI does not clear a **default member** for a given column if:</span></span>

* <span data-ttu-id="6913e-161">คอลัมน์มีบัตรตัวกรองที่มีสถานะเริ่มต้น และ Power BI กำลังจัดกลุ่มบนคอลัมน์ใน ARP</span><span class="sxs-lookup"><span data-stu-id="6913e-161">The column has a filter card with default state, and Power BI is groupings on a column in its ARP.</span></span>
* <span data-ttu-id="6913e-162">คอลัมน์อยู่เหนือคอลัมน์อื่นใน ARP และ Power BI มีบัตรตัวกรองสำหรับคอลัมน์อื่น ๆ ดังกล่าวในสถานะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6913e-162">The column is above another column in the ARP, and Power BI has a filter card for that other column in default state.</span></span>


## <a name="next-steps"></a><span data-ttu-id="6913e-163">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="6913e-163">Next steps</span></span>

<span data-ttu-id="6913e-164">บทความนี้อธิบายลักษณะการทำงานของ Power BI เมื่อทำงานกับสมาชิกเริ่มต้นในแบบจำลองหลายมิติ</span><span class="sxs-lookup"><span data-stu-id="6913e-164">This article described the behavior of Power BI when working with default members in multidimensional models.</span></span> <span data-ttu-id="6913e-165">คุณอาจมีความสนใจบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6913e-165">You might also be interested in the following articles:</span></span> 

* [<span data-ttu-id="6913e-166">แสดงรายการที่ไม่มีข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="6913e-166">Show items with no data in Power BI</span></span>](../create-reports/desktop-show-items-no-data.md)
* [<span data-ttu-id="6913e-167">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="6913e-167">Data sources in Power BI Desktop</span></span>](desktop-data-sources.md)