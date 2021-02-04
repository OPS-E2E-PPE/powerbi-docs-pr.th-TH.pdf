---
title: ใช้มุมมองแบบจำลองใน Power BI Desktop
description: ใช้มุมมองแบบจำลองเพื่อดูชุดข้อมูลที่ซับซ้อนในรูปแบบภาพใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: conceptual
ms.date: 05/08/2019
LocalizationGroup: Transform and shape data
ms.openlocfilehash: a47bcba58a39f76a6e9e64778d2d06a75dc14132
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413966"
---
# <a name="work-with-modeling-view-in-power-bi-desktop"></a><span data-ttu-id="97cf5-103">ทำงานร่วมกับมุมมองแบบจำลองใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="97cf5-103">Work with Modeling view in Power BI Desktop</span></span>

<span data-ttu-id="97cf5-104">ด้วย **มุมมองแบบจำลอง** ใน **Power BI Desktop** คุณสามารถดู และทำงานกับชุดข้อมูลที่ซับซ้อนที่ประกอบด้วยหลายตารางได้</span><span class="sxs-lookup"><span data-stu-id="97cf5-104">With **Modeling view** in **Power BI Desktop**, you can view and work with complex datasets that contain many tables.</span></span>


## <a name="using-modeling-view"></a><span data-ttu-id="97cf5-105">ใช้มุมมองแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="97cf5-105">Using Modeling view</span></span>

<span data-ttu-id="97cf5-106">เมื่อต้องการเข้าถึงมุมมองแบบจำลอง ให้เลือกไอคอนมุมมองแบบจำลองที่ด้านบนซ้ายของ **Power BI Desktop** ดังที่แสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="97cf5-106">To access Modeling view, select the Modeling view icon found on the left side of **Power BI Desktop**, as shown in the following image.</span></span>

![ไอคอนมุมมองแบบจำลองใน Power BI Desktop](media/desktop-modeling-view/modeling-view_02.png)

## <a name="creating-separate-diagrams"></a><span data-ttu-id="97cf5-108">สร้างไดอะแกรมที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="97cf5-108">Creating separate diagrams</span></span>

<span data-ttu-id="97cf5-109">ด้วยมุมมองแบบจำลอง คุณสามารถสร้างไดอะแกรมแบบจำลองของคุณที่ประกอบด้วยชุดย่อยของตารางในแบบจำลองของคุณโดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="97cf5-109">With Modeling view, you can create diagrams of your model that contain only a subset of the tables in your model.</span></span> <span data-ttu-id="97cf5-110">สิ่งนี้จะช่วยให้มุมมองชัดเจนยิ่งขึ้นในตารางที่คุณต้องการใช้งาน และให้การทำงานกับชุดข้อมูลที่ซับซ้อน</span><span class="sxs-lookup"><span data-stu-id="97cf5-110">This can help provide a clearer view into the tables you want to work with, and make working with complex datasets easier.</span></span> <span data-ttu-id="97cf5-111">เมื่อต้องการสร้างไดอะแกรมที่มีเฉพาะชุดย่อยของตาราง ให้คลิก **+** ลงชื่อเข้าใช้ถัดจากแท็บ **ตารางทั้งหมด** ที่ด้านล่างของบานหน้าต่าง Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="97cf5-111">To create a new diagram with only a subset of the tables, click the **+** sign next to the **All tables** tab along the bottom of the Power BI Desktop window.</span></span>

![สร้างไดอะแกรมใหม่ โดยการคลิกที่สัญลักษณ์ + ในส่วนของแท็บ](media/desktop-modeling-view/modeling-view_03.png)

<span data-ttu-id="97cf5-113">คุณยังสามารถลากตารางจากรายการ **เขตข้อมูล** ไปยังพื้นผิวไดอะแกรมได้</span><span class="sxs-lookup"><span data-stu-id="97cf5-113">You can then drag a table from the **Fields** list onto the diagram surface.</span></span> <span data-ttu-id="97cf5-114">คลิกขวาที่ตาราง จากนั้น **เพิ่มตารางที่เกี่ยวข้อง** จากเมนูที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="97cf5-114">Right click the table, and then select **Add related tables** from the menu that appears.</span></span>

![คลิกขวาที่ตาราง และเลือกเพิ่มตารางที่เกี่ยวข้อง](media/desktop-modeling-view/modeling-view_04.png)

<span data-ttu-id="97cf5-116">เมื่อคุณทำตาม ตารางที่เกี่ยวข้องกับตารางต้นฉบับจะแสดงในไดอะแกรมใหม่</span><span class="sxs-lookup"><span data-stu-id="97cf5-116">When you do, tables that are related to the original table are displayed in the new diagram.</span></span> <span data-ttu-id="97cf5-117">รูปต่อไปนี้แสดงตารางที่เกี่ยวข้องวิธีแสดงหลังจากเลือกตัว **เพิ่มตารางที่เกี่ยวข้อง** ตัวเลือกเมนู</span><span class="sxs-lookup"><span data-stu-id="97cf5-117">The following image shows how related tables are displayed after selecting the **Add related tables** menu option.</span></span>

![แสดงตารางที่เกี่ยวข้อง](media/desktop-modeling-view/modeling-view_05.png)

## <a name="setting-common-properties"></a><span data-ttu-id="97cf5-119">ตั้งค่าคุณสมบัติทั่วไป</span><span class="sxs-lookup"><span data-stu-id="97cf5-119">Setting common properties</span></span>

<span data-ttu-id="97cf5-120">คุณสามารถเลือกวัตถุหลายวัตถุพร้อมกันในมุมมองแบบจำลองได้โดยกดปุ่ม **CTRL** ค้างไว้และคลิกที่ตารางหลายๆ ตารางพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="97cf5-120">You can select multiple objects at once in Modeling view by holding down the **CTRL** key and clicking multiple tables.</span></span> <span data-ttu-id="97cf5-121">เมื่อคุณเลือกตารางหลายตาราง ตารางจะถูกเน้นไว้ในมุมมองแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="97cf5-121">When you select multiple tables they become highlighted in Modeling view.</span></span> <span data-ttu-id="97cf5-122">เมื่อตารางหลายตารางถูกเน้น การเปลี่ยนแปลงได้ถูกนำไปใช้ในบานหน้าต่าง **คุณสมบัติ** กับตารางที่เลือกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="97cf5-122">When multiple tables are highlighted, changes applied in the **Properties** pane apply to all selected tables.</span></span>

<span data-ttu-id="97cf5-123">ตัวอย่าง คุณสามารถเปลี่ยน [โหมดที่เก็บ](desktop-storage-mode.md)สำหรับตารางหลายตารางในมุมมองไดอะแกรมของคุณได้โดยกดปุ่ม **CTRL** ค้าง เลือกตาราง จาก นั้นเปลี่ยนการตั้งค่าโหมดที่เก็บข้อมูลในบานหน้าต่าง **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="97cf5-123">For example, you could change the [storage mode](desktop-storage-mode.md) for multiple tables in your diagram view by holding down the **CTRL** key, selecting tables, then changing the storage mode setting in the **Properties** pane.</span></span>

![เลือกตารางหลายตาราง โดยกด CTRL แล้วตั้งค่าคุณสมบัติทั่วไปในตารางที่เลือกทั้งหมด](media/desktop-modeling-view/modeling-view_06.png)


## <a name="next-steps"></a><span data-ttu-id="97cf5-125">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="97cf5-125">Next steps</span></span>

<span data-ttu-id="97cf5-126">บทความต่อไปนี้อธิบายเพิ่มเติมเกี่ยวกับแบบจำลองข้อมูล และยังอธิบายเกี่ยวกับ DirectQuery อย่างละเอียด</span><span class="sxs-lookup"><span data-stu-id="97cf5-126">The following articles describe more about data models, and also describe DirectQuery in detail.</span></span>

* [<span data-ttu-id="97cf5-127">รวมข้อมูลใน Power BI Desktop (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="97cf5-127">Aggregations in Power BI Desktop (Preview)</span></span>](desktop-aggregations.md)
* [<span data-ttu-id="97cf5-128">โมเดลแบบรวมใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="97cf5-128">Composite models in Power BI Desktop</span></span>](desktop-composite-models.md)
* [<span data-ttu-id="97cf5-129">โหมดที่เก็บข้อมูล ใน Power BI Desktop (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="97cf5-129">Storage Mode in Power BI Desktop (Preview)</span></span>](desktop-storage-mode.md)
* [<span data-ttu-id="97cf5-130">ความสัมพันธ์แบบกลุ่มต่อกลุ่มใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="97cf5-130">Many-to-many relationships in Power BI Desktop</span></span>](desktop-many-to-many-relationships.md)


<span data-ttu-id="97cf5-131">บทความ DirectQuery:</span><span class="sxs-lookup"><span data-stu-id="97cf5-131">DirectQuery articles:</span></span>

* [<span data-ttu-id="97cf5-132">การใช้ DirectQuery ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="97cf5-132">Using DirectQuery in Power BI</span></span>](../connect-data/desktop-directquery-about.md)
* [<span data-ttu-id="97cf5-133">แหล่งข้อมูลที่ได้รับการรองรับโดย DirectQuery ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="97cf5-133">Data sources supported by DirectQuery in Power BI</span></span>](../connect-data/power-bi-data-sources.md)
