---
title: ประมาณการตั้งค่า referential integrity ใน Power BI Desktop
description: ด้วย DirectQuery เรียนรู้วิธีการใช้ Power BI Desktop ประมาณ referential integrity
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 05/07/2019
LocalizationGroup: Connect to data
ms.openlocfilehash: 1b078f837efe0637a4ac7769ceb868af23c7a298
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96405939"
---
# <a name="apply-the-assume-referential-integrity-setting-in-power-bi-desktop"></a><span data-ttu-id="dc412-103">ใช้ประมาณการตั้งค่า Referential Integrity ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="dc412-103">Apply the Assume Referential Integrity setting in Power BI Desktop</span></span>
<span data-ttu-id="dc412-104">เมื่อเชื่อมต่อกับแหล่งข้อมูลโดยใช้ **DirectQuery** คุณสามารถใช้การเลือก **ประมาณ Referential Integrity** เพื่อเปิดใช้งานการเรียกใช้แบบสอบถามที่มีปะสิทธิภาพมากยิ่งขึ้นกับแหล่งข้อมูลของคุณได้</span><span class="sxs-lookup"><span data-stu-id="dc412-104">When connecting to a data source using **DirectQuery**, you can use the **Assume Referential Integrity** selection to enable running more efficient queries against your data source.</span></span> <span data-ttu-id="dc412-105">คุณลักษณะนี้มีข้อกำหนดบางอย่างเกี่ยวกับข้อมูลต้นแบบ และจะพร้อมใช้งานเมื่อใช้ **DirectQuery**</span><span class="sxs-lookup"><span data-stu-id="dc412-105">This feature has a few requirements of the underlying data, and it is only available when using **DirectQuery**.</span></span>

<span data-ttu-id="dc412-106">การตั้งค่า **ประมาณ referential integrity** จะเปิดใช้งานแบบสอบถามบนแหล่งข้อมูลเพื่อใช้คำสั่ง **INNER JOIN** ่ แทน **OUTER JOIN** ซึ่งช่วยปรับปรุงประสิทธิภาพแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="dc412-106">Setting **Assume referential integrity** enables queries on the data source to use **INNER JOIN** statements rather than **OUTER JOIN**, which improves query efficiency.</span></span>

![ภาพหน้าจอของกล่องโต้ตอบแก้ไขความสัมพันธ์เพื่อเลือก ตั้งสมมุติฐานว่ามีกฎการอ้างอิง](media/desktop-assume-referential-integrity/assume-referential-integrity_1.png)

## <a name="requirements-for-using-assume-referential-integrity"></a><span data-ttu-id="dc412-108">ข้อกำหนดสำหรับการใช้การประมาณ referential integrity</span><span class="sxs-lookup"><span data-stu-id="dc412-108">Requirements for using Assume referential integrity</span></span>
<span data-ttu-id="dc412-109">เป็นการตั้งค่าขั้นสูงและจะเปิดใช้งานเมื่อเชื่อมต่อกับข้อมูลโดยใช้ **DirectQuery** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="dc412-109">This is an advanced setting, and is only enabled when connecting to data using **DirectQuery**.</span></span> <span data-ttu-id="dc412-110">ข้อกำหนดดังต่อไปนี้เป็นสิ่งจำเป็นสำหรับ **ประมาณ referential integrity** เพื่อให้ทำงานอย่างถูกต้อง:</span><span class="sxs-lookup"><span data-stu-id="dc412-110">The following requirements are necessary for **Assume referential integrity** to work properly:</span></span>

* <span data-ttu-id="dc412-111">ข้อมูลในคอลัมน์ **From** ในความสัมพันธ์ไม่เป็น *Null* หรือ *ว่างเปล่า*</span><span class="sxs-lookup"><span data-stu-id="dc412-111">Data in the **From** column in the relationship is never *Null* or *blank*</span></span>
* <span data-ttu-id="dc412-112">สำหรับแต่ละค่าในคอลัมน์ **From** ไม่มีค่าที่สอดคล้องกันในคอลัมน์ **To**</span><span class="sxs-lookup"><span data-stu-id="dc412-112">For each value in the **From** column, there is a corresponding value in the **To** column</span></span>

<span data-ttu-id="dc412-113">ในบริบทนี้ คอลัมน์ **From** จะเป็นแบบ *กลุ่ม* ในความสัมพันธ์แบบ *หนึ่งต่อกลุ่ม* หรือเป็นคอลัมน์ในตารางแรกในความสัมพันธ์แบบ *หนึ่งต่อหนึ่ง*</span><span class="sxs-lookup"><span data-stu-id="dc412-113">In this context, the **From** column is the *Many* in a *One-to-Many* relationship, or it is the column in the first table in a *One-to-One* relationship.</span></span>

## <a name="example-of-using-assume-referential-integrity"></a><span data-ttu-id="dc412-114">ข้อกำหนดสำหรับการใช้การประมาณ referential integrity</span><span class="sxs-lookup"><span data-stu-id="dc412-114">Example of using Assume referential integrity</span></span>
<span data-ttu-id="dc412-115">ตัวอย่างต่อไปนี้จะสาธิตลักษณะการทำงาน **ประมาณ referential integrity** เมื่อใช้ในการเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dc412-115">The following example demonstrates how **Assume referential integrity** behaves when used in data connections.</span></span> <span data-ttu-id="dc412-116">ตัวอย่างการเชื่อมต่อกับแหล่งข้อมูลรวมถึงตาราง **Orders** ตาราง **Products** และตาราง **Depots**</span><span class="sxs-lookup"><span data-stu-id="dc412-116">The example connects to a data source that includes an **Orders** table, a **Products** table, and a **Depots** table.</span></span>

1. <span data-ttu-id="dc412-117">ในรูปต่อไปนี้ที่แสดงในตาราง **Orders** และตาราง **Products** โปรดสังเกตว่า referential integrity จะเกิดขึ้นระหว่าง **Orders[ProductID]** กับ **Products[ProductID]**</span><span class="sxs-lookup"><span data-stu-id="dc412-117">In the following image that shows the **Orders** table and the **Products** table, note that referential integrity exists between **Orders[ProductID]** and **Products[ProductID]**.</span></span> <span data-ttu-id="dc412-118">คอลัมน์ **[ProductID]** ในตาราง **Orders** จะไม่เป็น *Null* และทุกค่ายังปรากฏในตาราง **Products** ด้วย</span><span class="sxs-lookup"><span data-stu-id="dc412-118">The **[ProductID]** column in the **Orders** table is never *Null*, and every value also appears in the **Products** table.</span></span> <span data-ttu-id="dc412-119">ดังนั้น **ประมาณ Referential Integrity** จึงควรถูกตั้งค่าเพื่อรับแบบสอบถามมีประสิทธิภาพมากขึ้น (การใช้การตั้งค่านี้จะไม่เปลี่ยนแปลงค่าที่แสดงในการแสดงผลด้วยภาพ)</span><span class="sxs-lookup"><span data-stu-id="dc412-119">As such, **Assume Referential Integrity** should be set to get more efficient queries (using this setting does not change the values shown in visuals).</span></span>
   
   ![ภาพหน้าจอของตารางคำสั่งซื้อและตารางผลิตภัณฑ์](media/desktop-assume-referential-integrity/assume-referential-integrity_2.png)
2. <span data-ttu-id="dc412-121">ในภาพถัดไป จะสังเกตเห็นได้ว่า ไม่มี referential integrity เกิดขึ้นระหว่าง **Orders[DepotID]** กับ **Depots[DepotID]** เพราะ **DepotID** เป็น *Null* สำหรับบาง *Orders*</span><span class="sxs-lookup"><span data-stu-id="dc412-121">In the next image, notice that no referential integrity exists between **Orders[DepotID]** and **Depots[DepotID]**, because the **DepotID** is *Null* for some *Orders*.</span></span> <span data-ttu-id="dc412-122">ดังนั้น **ประมาณ Referential Integrity** จึงไม่ควร *ถูก* ตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="dc412-122">As such, **Assume Referential Integrity** should *not* be set.</span></span>
   
   ![สกรีนช็อตของตารางคำสั่งซื้อและตารางคลังสินค้า](media/desktop-assume-referential-integrity/assume-referential-integrity_3.png)
3. <span data-ttu-id="dc412-124">ในตอนท้าย ไม่มีของ referential integrity เกิดขึ้นระหว่าง **Orders[CustomerID]** กับ **Customers[CustID]** ในตารางดังต่อไปนี้ กล่าวคือ **CustomerID** จะมีบางค่า (ในกรณีนี้ ได้แก่ *CustX*) ซึ่งไม่เกิดขึ้นในตาราง *Customers*</span><span class="sxs-lookup"><span data-stu-id="dc412-124">Finally, no referential integrity exists between **Orders[CustomerID]** and **Customers[CustID]** in the following tables; the **CustomerID** contains some values (in this case, *CustX*) that do not exist in the *Customers* table.</span></span> <span data-ttu-id="dc412-125">ดังนั้น **ประมาณ Referential Integrity** จึงไม่ควร *ถูก* ตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="dc412-125">As such, **Assume Referential Integrity** should *not* be set.</span></span>
   
   ![ภาพหน้าจอของตารางคำสั่งซื้อและตารางลูกค้า](media/desktop-assume-referential-integrity/assume-referential-integrity_4.png)

## <a name="setting-assume-referential-integrity"></a><span data-ttu-id="dc412-127">การตั้งค่าการประมาณ Referential Integrity</span><span class="sxs-lookup"><span data-stu-id="dc412-127">Setting Assume referential integrity</span></span>
<span data-ttu-id="dc412-128">เมื่อต้องการเปิดใช้งานคุณลักษณะนี้ เลือกกล่องกาเครื่องหมายถัดจาก **ประมาณ Referential Integrity** ดังที่แสดงในภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="dc412-128">To enable this feature, select the checkbox next to **Assume Referential Integrity** as shown in the following image.</span></span>

![ภาพหน้าจอของกล่องโต้ตอบแก้ไขความสัมพันธ์ที่ช่วยให้คุณสามารถเลือก ตั้งสมมุติฐานว่ามีกฎการอ้างอิง](media/desktop-assume-referential-integrity/assume-referential-integrity_1.png)

<span data-ttu-id="dc412-130">เมื่อเลือกแล้ว การตั้งค่าก็จะถูกตรวจสอบกับข้อมูลเพื่อให้แน่ใจว่า ไม่มี *Null* หรือแถวที่ไม่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="dc412-130">When selected, the setting is validated against the data to ensure there are no *Null* or mismatched rows.</span></span> <span data-ttu-id="dc412-131">*อย่างไรก็ตาม* สำหรับกรณีที่มีจำนวนค่ามาก การตรวจสอบจะไม่สามารถรับประกันได้ว่า ไม่มีปัญหาใด ๆ เกี่ยวกับ referential integrity</span><span class="sxs-lookup"><span data-stu-id="dc412-131">*However*, for cases with a very large number of values, the validation is not a guarantee that there are no referential integrity issues.</span></span>

<span data-ttu-id="dc412-132">นอกจากนี้ การตรวจสอบจะเกิดขึ้นในเวลาที่มีการแก้ไขความสัมพันธ์ และจะ *ไม่* แสดงการเปลี่ยนแปลงใด ๆ กับข้อมูลในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="dc412-132">In addition, the validation occurs at the time of editing the relationship, and does *not* reflect any subsequent changes to the data.</span></span>

## <a name="what-happens-if-you-incorrectly-set-assume-referential-integrity"></a><span data-ttu-id="dc412-133">จะเกิดอะไรขึ้นถ้าคุณตั้งค่าการประมาณ referential integrity ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="dc412-133">What happens if you incorrectly set Assume referential integrity?</span></span>
<span data-ttu-id="dc412-134">ถ้าคุณตั้งค่า **ประมาณ Referential Integrity** เมื่อไม่มีปัญหา referential integrity ในข้อมูล สิ่งนี้จะไม่ส่งผลให้เกิดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="dc412-134">If you set **Assume Referential Integrity** when there are referential integrity issues in the data, this will not result in errors.</span></span> <span data-ttu-id="dc412-135">อย่างไรก็ตาม จะส่งผลให้เกิดความไม่สอดคล้องกันของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dc412-135">However, it will result in apparent inconsistencies in the data.</span></span> <span data-ttu-id="dc412-136">ตัวอย่างเช่น ในกรณีของความสัมพันธ์กับตาราง **Depots** ที่อธิบายไว้ข้างต้น อาจส่งผลดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="dc412-136">For example, in the case of the relationship to the **Depots** table described above, it would result in the following:</span></span>

* <span data-ttu-id="dc412-137">การแสดงผลด้วยภาพซึ่งแสดง *Order Qty* รวมจะแสดงค่า 40</span><span class="sxs-lookup"><span data-stu-id="dc412-137">A visual showing the total *Order Qty* would show a value of 40</span></span>
* <span data-ttu-id="dc412-138">การแสดงผลด้วยภาพซึ่งแสดง *Order Qty by Depot City* รวมจะแสดงค่าผลรวมเฉพาะ *30* เนื่องจากนั้นไม่รวม Order ID 1 ซึ่ง **DepotID** เป็น *Null*</span><span class="sxs-lookup"><span data-stu-id="dc412-138">A visual showing the total *Order Qty by Depot City* would show a total value of only *30*, because it would not include Order ID 1, where **DepotID** is *Null*.</span></span>

## <a name="next-steps"></a><span data-ttu-id="dc412-139">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="dc412-139">Next steps</span></span>
<span data-ttu-id="dc412-140">เรียนรู้เพิ่มเติมเกี่ยวกับ [DirectQuery](desktop-use-directquery.md)</span><span class="sxs-lookup"><span data-stu-id="dc412-140">Learn more about [DirectQuery](desktop-use-directquery.md)</span></span>

<span data-ttu-id="dc412-141">รับข้อมูลเพิ่มเติมเกี่ยวกับ [ความสัมพันธ์ใน Power BI](../transform-model/desktop-create-and-manage-relationships.md)</span><span class="sxs-lookup"><span data-stu-id="dc412-141">Get more information about [Relationships in Power BI](../transform-model/desktop-create-and-manage-relationships.md)</span></span>

<span data-ttu-id="dc412-142">เมื่อต้องการเรียนรู้เพิ่มเติม ดู [มุมมองความสัมพันธ์ใน Power BI Desktop](../transform-model/desktop-relationship-view.md)</span><span class="sxs-lookup"><span data-stu-id="dc412-142">Learn more about [Relationship View in Power BI Desktop](../transform-model/desktop-relationship-view.md).</span></span>
