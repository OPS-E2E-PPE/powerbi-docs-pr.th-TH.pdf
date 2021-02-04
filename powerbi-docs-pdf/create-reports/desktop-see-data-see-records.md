---
title: ตารางวิชวลและระเบียนในวิชวล Power BI Desktop
description: ใช้ตารางวิชวลและคุณลักษณะตารางจุดข้อมูลของ Power BI Desktop เพื่อเข้าถึงรายละเอียด
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 05/21/2020
LocalizationGroup: Learn more
ms.openlocfilehash: 05dcd5f0d7ca1681ee1e82762ea1557c79c5bc24
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412816"
---
# <a name="use-visual-table-and-data-point-table-in-power-bi-desktop"></a><span data-ttu-id="4475c-103">ใช้ตารางวิชวลและตารางจุดข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4475c-103">Use Visual table and Data point table in Power BI Desktop</span></span>
<span data-ttu-id="4475c-104">ใน **Power BI Desktop** คุณสามารถเจาะลึกรายละเอียดของการแสดงผลใด ๆ และดูข้อมูลพื้นฐานหรือระเบียนข้อมูลสำหรับวิชวลที่เลือก ให้อยู่ในรูปข้อความได้</span><span class="sxs-lookup"><span data-stu-id="4475c-104">In **Power BI Desktop** you can drill into the details of a visualization, and see textual representations of the underlying data or the individual data records for the selected visual.</span></span> <span data-ttu-id="4475c-105">คุณลักษณะเหล่านี้ บางครั้งเรียกว่าการ *คลิกผ่าน* หรือ *ดูรายละเอียด* หรือ *เข้าถึงรายละเอียด*</span><span class="sxs-lookup"><span data-stu-id="4475c-105">These features are sometimes referred to as *click-through*, *drill-through*, or *drill-through to details*.</span></span>

<span data-ttu-id="4475c-106">คุณสามารถใช้ **ตารางวิชวล** เพื่อดูข้อมูลในวิชวลในรูปแบบตาราง หรือใช้ **ตารางจุดข้อมูล** เพื่อดูตารางของข้อมูลที่ใช้ในการคำนวณจุดข้อมูลเดียว</span><span class="sxs-lookup"><span data-stu-id="4475c-106">You can use **Visual table** to view the data in a visual as a table, or use **Data point table** to view a table of the data used to calculate a single data point.</span></span> 

![ตารางวิชวลและตารางจุดข้อมูล](media/desktop-see-data-see-records/see-data-record.png)

>[!IMPORTANT]
><span data-ttu-id="4475c-108">**ตารางวิชวล** และ **ตารางจุดข้อมูล** รองรับเฉพาะชนิดการแสดงภาพต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4475c-108">**Visual table** and **Data point table** support only the following visualization types:</span></span>
>  - <span data-ttu-id="4475c-109">แผนภูมิแท่ง</span><span class="sxs-lookup"><span data-stu-id="4475c-109">Bar chart</span></span>
>  - <span data-ttu-id="4475c-110">Column chart</span><span class="sxs-lookup"><span data-stu-id="4475c-110">Column chart</span></span>
>  - <span data-ttu-id="4475c-111">แผนภูมิโดนัท</span><span class="sxs-lookup"><span data-stu-id="4475c-111">Donut chart</span></span>
>  - <span data-ttu-id="4475c-112">แผนที่แถบสี</span><span class="sxs-lookup"><span data-stu-id="4475c-112">Filled map</span></span>
>  - <span data-ttu-id="4475c-113">แผนภูมิกรวย</span><span class="sxs-lookup"><span data-stu-id="4475c-113">Funnel</span></span>
>  - <span data-ttu-id="4475c-114">แผนที่</span><span class="sxs-lookup"><span data-stu-id="4475c-114">Map</span></span>
>  - <span data-ttu-id="4475c-115">Pie chart</span><span class="sxs-lookup"><span data-stu-id="4475c-115">Pie chart</span></span>
>  - <span data-ttu-id="4475c-116">แผนที่ต้นไม้</span><span class="sxs-lookup"><span data-stu-id="4475c-116">Treemap</span></span>

## <a name="use-visual-table-in-power-bi-desktop"></a><span data-ttu-id="4475c-117">ใช้ตารางวิชวลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4475c-117">Use Visual table in Power BI Desktop</span></span>

<span data-ttu-id="4475c-118">**ตารางวิชวล** แสดงข้อมูลเบื้องต้นในการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="4475c-118">**Visual table** shows you the data underlying a visualization.</span></span> <span data-ttu-id="4475c-119">**ตารางวิชวล** ปรากฏในแท็บ **ข้อมูล/เข้าถึงรายละเอียด** ในส่วน **แสดง** ของแถบเครื่องมือ เมื่อวิชวลถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="4475c-119">**Visual table** appears in the **Data/Drill** tab in the **Show** section of the ribbon when a visual is selected.</span></span>

![ตารางวิชวลในแถบเครื่องมือ](media/desktop-see-data-see-records/visual-table-01.png)

<span data-ttu-id="4475c-121">คุณยังสามารถดูข้อมูลได้โดยการคลิกขวาบนการแสดงภาพ แล้ว เลือก **แสดงข้อมูล** จากเมนูที่ปรากฏ หรือ โดยการเลือก **ตัวเลือกเพิ่มเติม** (...) ในมุมขวาบนของการแสดงภาพ และจากนั้นเลือก **แสดงในรูปแบบตาราง**</span><span class="sxs-lookup"><span data-stu-id="4475c-121">You can also see the data by right-clicking on a visualization, and then selecting **Show Data** from the menu that appears; or by selecting **More options** (...) in the upper-right corner of a visualization, and then selecting **Show as a table**.</span></span>

![แสดงข้อมูลจากคลิกขวา](media/desktop-see-data-see-records/visual-table-02.png)&nbsp;&nbsp;![แสดงข้อมูลจากตัวเลือกเพิ่มเติม](media/desktop-see-data-see-records/visual-table-03.png)

> [!NOTE]
> <span data-ttu-id="4475c-124">คุณต้องโฮเวอร์เมาส์เหนือจุดข้อมูลในวิชวล เพื่อให้มีเมนูคลิกขวา</span><span class="sxs-lookup"><span data-stu-id="4475c-124">You must be hovering over a data point in the visual for the right-click menu to be available.</span></span>

<span data-ttu-id="4475c-125">เมื่อคุณเลือก **ตารางวิชวล** หรือ **ตารางจุดข้อมูล** พื้นที่ของ Power BI Desktop จะแสดงทั้งวิชวล และข้อมูลพื้นฐานของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4475c-125">When you select **Visual table** or **Data point table**, the Power BI Desktop canvas displays both the visual and the textual representation of the data.</span></span> <span data-ttu-id="4475c-126">ใน *มุมมองแนวนอน* วิชวลจะแสดงอยู่ครึ่งบนของพื้นที่ ส่วนข้อมูลจะแสดงอยู่ครึ่งล่าง ดังรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4475c-126">In the *horizontal view*, the visual is displayed on the top half of the canvas, and the data is shown on the bottom half.</span></span> 

![มุมมองแนวนอน](media/desktop-see-data-see-records/visual-table-04.png)

<span data-ttu-id="4475c-128">คุณยังสามารถสลับระหว่างมุมมองแนวนอน และ *มุมมองแนวตั้ง* โดยการเลือกไอคอนที่มุมบนขวาได้</span><span class="sxs-lookup"><span data-stu-id="4475c-128">You can toggle between the horizontal view and a *vertical view* by selecting the icon in the upper-right corner of the canvas.</span></span>

![สลับไปยังมุมมองแนวตั้ง](media/desktop-see-data-see-records/visual-table-05.png)

<span data-ttu-id="4475c-130">เพื่อกลับไปยังรายงาน เลือก **< กลับไปที่รายงาน** ในมุมบนซ้ายของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="4475c-130">To get back to the report, select **< Back to Report** in the upper-left corner of the canvas.</span></span>

![กลับไปที่รายงาน](media/desktop-see-data-see-records/visual-table-06.png)

## <a name="use-data-point-table-in-power-bi-desktop"></a><span data-ttu-id="4475c-132">ใช้ตารางจุดข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4475c-132">Use Data point table in Power BI Desktop</span></span>

<span data-ttu-id="4475c-133">คุณยังสามารถโฟกัสไปที่ข้อมูลหนึ่งระเบียนในวิชวล และเจาะลึกลงข้อมูลข้างใน</span><span class="sxs-lookup"><span data-stu-id="4475c-133">You can also focus on one data record in a visualization, and drill into the data behind it.</span></span> <span data-ttu-id="4475c-134">เพื่อใช้ **ตารางจุดข้อมูล** ให้เลือกการแสดงภาพ จากนั้นเลือก **ตารางจุดข้อมูล** ในแท็บ **ข้อมูล/เข้าถึงรายละเอียด** ในส่วน **เครื่องมือวิชวล** ของแถบเครื่องมือ แล้วจึงเลือกจุดข้อมูลหรือแถวบนการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="4475c-134">To use **Data point table**, select a visualization, then select **Data point table** in the **Data/Drill** tab in the **Visual Tools** section of the ribbon, and then select a data point or row on the visualization.</span></span> 

![ตารางจุดข้อมูลในแถบเครื่องมือ](media/desktop-see-data-see-records/visual-table-07.png)

> [!NOTE]
> <span data-ttu-id="4475c-136">ถ้าปุ่ม **ตารางจุดข้อมูล** ในแถบเครื่องมือถูกปิดใช้งาน และแสดงเป็นสีเทา แสดงว่า การแสดงผลภาพที่เลือกไม่รองรับ **ตารางจุดข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="4475c-136">If the **Data point table** button in the ribbon is disabled and grayed-out, it means the selected visualization does not support **Data point table**.</span></span>

<span data-ttu-id="4475c-137">คุณยังสามารถคลิกขวาที่องค์ประกอบข้อมูล และเลือก **ตารางจุดข้อมูล** จากเมนูที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="4475c-137">You can also right-click a data element and select **Data point table** from the menu that appears.</span></span>

![ตารางจุดข้อมูลโดยการคลิกขวา](media/desktop-see-data-see-records/visual-table-08.png)

<span data-ttu-id="4475c-139">เมื่อคุณได้เลือก **ตารางจุดข้อมูล** สำหรับองค์ประกอบข้อมูล พื้นที่ทำงานของ Power BI Desktop จะแสดงข้อมูลทั้งหมดที่เกี่ยวข้องกับองค์ประกอบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4475c-139">When you select **Data point table** for a data element, the Power BI Desktop canvas displays all the data associated with the selected element.</span></span> 

![ภาพหน้าจอของผืนผ้าใบ ที่แสดงข้อมูลทั้งหมดที่เกี่ยวข้องกับองค์ประกอบที่เลือกเมื่อคุณเลือกตารางจุดข้อมูล](media/desktop-see-data-see-records/visual-table-09.png)

<span data-ttu-id="4475c-141">เพื่อกลับไปยังรายงาน เลือก **< กลับไปที่รายงาน** ในมุมบนซ้ายของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="4475c-141">To get back to the report, select **< Back to Report** in the upper-left corner of the canvas.</span></span>


> [!NOTE]
><span data-ttu-id="4475c-142">**ตารางจุดข้อมูล** มีข้อจำกัดดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4475c-142">**Data point table** has the following limitations:</span></span>
> - <span data-ttu-id="4475c-143">คุณไม่สามารถเปลี่ยนข้อมูลในมุมมอง **ตารางจุดข้อมูล** และบันทึกกลับไปยังรายงานได้</span><span class="sxs-lookup"><span data-stu-id="4475c-143">You can't change the data in the **Data point table** view and save it back to the report.</span></span>
> - <span data-ttu-id="4475c-144">คุณไม่สามารถใช้ **ตารางจุดข้อมูล** เมื่อวิชวลของคุณใช้หน่วยวัดจากการคำนวณในกลุ่มหน่วยวัด (หลายมิติ)</span><span class="sxs-lookup"><span data-stu-id="4475c-144">You can't use **Data point table** when your visual uses a calculated measure in a (multidimensional) measure group.</span></span>
> - <span data-ttu-id="4475c-145">คุณไม่สามารถใช้ **ตารางจุดข้อมูล** เมื่อคุณเชื่อมต่อกับแบบจำลองสดแบบหลายมิติ (MD)</span><span class="sxs-lookup"><span data-stu-id="4475c-145">You can't use **Data point table** when you are connected to a live multidimensional (MD) model.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4475c-146">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4475c-146">Next steps</span></span>
<span data-ttu-id="4475c-147">มีการจัดรูปแบบและการจัดการข้อมูลที่หลากหลายใน **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="4475c-147">There are all sorts of report formatting and data management features in **Power BI Desktop**.</span></span> <span data-ttu-id="4475c-148">ลองดูทรัพยากรต่อไปนี้สำหรับตัวอย่างบางส่วน:</span><span class="sxs-lookup"><span data-stu-id="4475c-148">Check out the following resources for a few examples:</span></span>

* [<span data-ttu-id="4475c-149">ใช้การจัดกลุ่ม และจัดช่องเก็บใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4475c-149">Use grouping and binning in Power BI Desktop</span></span>](desktop-grouping-and-binning.md)
* [<span data-ttu-id="4475c-150">ใช้เส้นตาราง, จัดชิดกับเส้นตาราง, ลําดับบนแกน Z, การจัดแนว และการแจกจ่ายในรายงาน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4475c-150">Use gridlines, snap-to-grid, z-order, alignment and distribution in Power BI Desktop reports</span></span>](desktop-gridlines-snap-to-grid.md)

