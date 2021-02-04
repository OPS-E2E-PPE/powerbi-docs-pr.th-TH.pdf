---
title: มุมมองข้อมูลใน Power BI Desktop
description: มุมมองข้อมูลใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 05/05/2020
LocalizationGroup: Model your data
ms.openlocfilehash: 500346e9fbdc4302810cce1fe5e49e7fe915a3bb
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411229"
---
# <a name="work-with-data-view-in-power-bi-desktop"></a><span data-ttu-id="cc0b1-103">ทำงานด้วยมุมมองข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="cc0b1-103">Work with Data view in Power BI Desktop</span></span>

<span data-ttu-id="cc0b1-104">*มุมมองข้อมูล* ช่วยให้คุณตรวจสอบ สำรวจ และทำความเข้าใจข้อมูลในรูปแบบ *Power BI Desktop*</span><span class="sxs-lookup"><span data-stu-id="cc0b1-104">*Data view* helps you inspect, explore, and understand data in your *Power BI Desktop* model.</span></span> <span data-ttu-id="cc0b1-105">ซึ่งจะแตกต่างจากวิธีที่คุณดูตาราง คอลัมน์ และข้อมูลใน *ตัวแก้ไข Power Query*</span><span class="sxs-lookup"><span data-stu-id="cc0b1-105">It's different from how you view tables, columns, and data in *Power Query Editor*.</span></span> <span data-ttu-id="cc0b1-106">ด้วยมุมมองข้อมูล คุณจะกำลังดูข้อมูลของคุณ *หลังจาก* ที่โหลดเข้ามาในรูปแบบเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="cc0b1-106">With Data view, you're looking at your data *after* it has been loaded into the model.</span></span>

> [!NOTE]
> <span data-ttu-id="cc0b1-107">เนื่องจากมุมมองข้อมูลแสดงข้อมูลหลังจากที่โหลดลงในแบบจำลองแล้ว ไอคอนมุมมองข้อมูลจะไม่สามารถมองเห็นได้หากแหล่งข้อมูลทั้งหมดขึ้นอยู่กับ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="cc0b1-107">Since Data view shows data after it's loaded into the model, the Data view icon is not visible if all data sources are based on DirectQuery.</span></span> 

<span data-ttu-id="cc0b1-108">เมื่อคุณกำลังจัดรูปแบบข้อมูลของคุณ บางครั้งคุณต้องการดูว่ามีอะไรอยู่ในตารางหรือคอลัมน์จริง ๆ โดยไม่สร้างวิชวลบนพื้นที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="cc0b1-108">When you're modeling your data, sometimes you want to see what's actually in a table or column without creating a visual on the report canvas.</span></span> <span data-ttu-id="cc0b1-109">คุณอาจต้องการดูลึกลงไปถึงระดับแถว</span><span class="sxs-lookup"><span data-stu-id="cc0b1-109">You might want to see right down to the row level.</span></span> <span data-ttu-id="cc0b1-110">ความสามารถนี้จะเป็นประโยชน์มาก โดยเฉพาะอย่างยิ่งเมื่อคุณกำลังจะสร้างการวัดและคอลัมน์จากการคำนวณ หรือคุณจำเป็นต้องระบุชนิดข้อมูลหรือประเภทข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cc0b1-110">This ability is especially useful when you're creating measures and calculated columns, or you need to identify a data type or data category.</span></span>

<span data-ttu-id="cc0b1-111">ลองมาดูรายละเอียดองค์ประกอบที่พบในมุมมองข้อมูลกันบ้าง</span><span class="sxs-lookup"><span data-stu-id="cc0b1-111">Let's take a closer look at some of the elements found in Data view.</span></span>

![มุมมองข้อมูลใน Power BI Desktop](media/desktop-data-view/dataview_fullscreen.png)

1. <span data-ttu-id="cc0b1-113">**ไอคอนมุมมองข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="cc0b1-113">**Data view icon**.</span></span> <span data-ttu-id="cc0b1-114">เลือกไอคอนนี้เพื่อเข้าสู่มุมมองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cc0b1-114">Select this icon to enter Data view.</span></span>

2. <span data-ttu-id="cc0b1-115">**ตารางข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="cc0b1-115">**Data Grid**.</span></span> <span data-ttu-id="cc0b1-116">พื้นที่นี้แสดงตารางที่เลือกและคอลัมน์และแถวทั้งหมดในตารางดด้วย</span><span class="sxs-lookup"><span data-stu-id="cc0b1-116">This area shows the selected table and all columns and rows in it.</span></span> <span data-ttu-id="cc0b1-117">คอลัมน์ที่ซ่อนจากมุมมอง *รายงาน* จะเป็นสีเทา คุณสามารถคลิกขวาบนคอลัมน์สำหรับตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="cc0b1-117">Columns hidden from *Report* view are greyed out. You can right-click on a column for options.</span></span>

3. <span data-ttu-id="cc0b1-118">**Ribbon การจัดรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="cc0b1-118">**Modeling ribbon**.</span></span> <span data-ttu-id="cc0b1-119">คุณสามารถจัดการความสัมพันธ์ สร้างการคำนวณ เปลี่ยนชนิดข้อมูล รูปแบบ ประเภทข้อมูลสำหรับคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="cc0b1-119">Here you can manage relationships, create calculations, change data type, format, data category for a column.</span></span>

4. <span data-ttu-id="cc0b1-120">**แถบสูตร**</span><span class="sxs-lookup"><span data-stu-id="cc0b1-120">**Formula bar**.</span></span> <span data-ttu-id="cc0b1-121">ป้อนสูตรนิพจน์การวิเคราะห์ข้อมูล (DAX) สำหรับการวัดและคอลัมน์จากการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="cc0b1-121">Enter Data Analysis Expression (DAX) formulas for Measures and Calculated columns.</span></span>

5. <span data-ttu-id="cc0b1-122">**ค้นหา**</span><span class="sxs-lookup"><span data-stu-id="cc0b1-122">**Search**.</span></span> <span data-ttu-id="cc0b1-123">ค้นหาตารางหรือคอลัมน์ในแบบจำลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="cc0b1-123">Search for a table or column in your model.</span></span>

6. <span data-ttu-id="cc0b1-124">**รายการเขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="cc0b1-124">**Fields list**.</span></span> <span data-ttu-id="cc0b1-125">เลือกตารางหรือคอลัมน์เพื่อดูในตารางข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cc0b1-125">Select a table or column to view in the data grid.</span></span>

## <a name="filtering-in-data-view"></a><span data-ttu-id="cc0b1-126">การกรองในมุมมองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cc0b1-126">Filtering in Data view</span></span>

<span data-ttu-id="cc0b1-127">คุณยังสามารถกรองและจัดเรียงข้อมูลในมุมมองข้อมูลได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="cc0b1-127">You can also filter and sort data in Data view.</span></span> <span data-ttu-id="cc0b1-128">แต่ละคอลัมน์จะแสดงไอคอนที่ระบุทิศทางการจัดเรียง ถ้ามีการนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="cc0b1-128">Each column shows an icon that identifies the sort direction, if applied.</span></span>

![เรียงลำดับและกรองในมุมมองข้อมูลใน Power BI Desktop](media/desktop-data-view/dataview_sort-and-filter.png)

<span data-ttu-id="cc0b1-130">คุณสามารถกรองค่าแต่ละค่าได้ หรือใช้การกรองขั้นสูงตามข้อมูลในคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="cc0b1-130">You can filter individual values, or use advanced filtering based on the data in the column.</span></span>

> [!NOTE]
> <span data-ttu-id="cc0b1-131">เมื่อมีการสร้างแบบจำลอง Power BI ในวัฒนธรรมอื่นนอกเหนือจากส่วนติดต่อผู้ใช้ปัจจุบันของคุณ กล่องการค้นหาจะไม่ปรากฏในส่วนติดต่อผู้ใช้ของมุมมองข้อมูล สำหรับสิ่งอื่นใดนอกเหนือจากเขตข้อมูลข้อความ</span><span class="sxs-lookup"><span data-stu-id="cc0b1-131">When a Power BI model is created in a different culture than your current user interface, the search box will not appear in the Data view user interface for anything other than text fields.</span></span> <span data-ttu-id="cc0b1-132">ตัวอย่างเช่น รายการนี้จะปรับใช้สำหรับแบบจำลองที่สร้างขึ้นในภาษาอังกฤษแบบสหรัฐอเมริกาที่คุณดูในภาษาสเปน</span><span class="sxs-lookup"><span data-stu-id="cc0b1-132">For example, this would apply for a model created in US English that you view in Spanish.</span></span>


## <a name="next-steps"></a><span data-ttu-id="cc0b1-133">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="cc0b1-133">Next steps</span></span>

<span data-ttu-id="cc0b1-134">คุณสามารถทำการเรียงลำดับของของต่างๆ ด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="cc0b1-134">You can do all sorts of things with Power BI Desktop.</span></span> <span data-ttu-id="cc0b1-135">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับขีดความสามารถ กรุณาดูแหล่งทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cc0b1-135">For more information on its capabilities, check out the following resources:</span></span>

* [<span data-ttu-id="cc0b1-136">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="cc0b1-136">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="cc0b1-137">ภาพรวมคำถามด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="cc0b1-137">Query overview with Power BI Desktop</span></span>](../transform-model/desktop-query-overview.md)
* [<span data-ttu-id="cc0b1-138">ชนิดข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="cc0b1-138">Data types in Power BI Desktop</span></span>](desktop-data-types.md)
* [<span data-ttu-id="cc0b1-139">จัดรูปร่างและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="cc0b1-139">Shape and combine data with Power BI Desktop</span></span>](desktop-shape-and-combine-data.md)
* [<span data-ttu-id="cc0b1-140">งานแบบสอบถามทั่วไปใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="cc0b1-140">Common query tasks in Power BI Desktop</span></span>](../transform-model/desktop-common-query-tasks.md)
