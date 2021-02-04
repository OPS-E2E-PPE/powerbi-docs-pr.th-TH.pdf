---
title: แสดงข้อมูลที่ถูกใช้เพื่อสร้างการแสดงภาพ Power BI
description: เอกสารนี้อธิบายวิธีการแสดงข้อมูลที่ใช้เพื่อสร้างภาพใน Power BI และวิธีการส่งออกข้อมูลนั้นไปยังไฟล์ .csv
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 12/4/2019
LocalizationGroup: Visualizations
ms.openlocfilehash: 7aa15bae7ab94619a9f652aa20da9222e3d4af41
ms.sourcegitcommit: 0711972326521944fdd8572403c0b15f31b916da
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/22/2020
ms.locfileid: "97721650"
---
# <a name="display-a-visualizations-underlying-data"></a><span data-ttu-id="683cd-103">แสดงข้อมูลเบื้องต้นของการจัดรูปแบบการแสดงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="683cd-103">Display a visualization's underlying data</span></span>

[!INCLUDE[consumer-appliesto-yyyn](../includes/consumer-appliesto-nyyn.md)]    

## <a name="show-data"></a><span data-ttu-id="683cd-104">แสดงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="683cd-104">Show data</span></span>
<span data-ttu-id="683cd-105">การแสดงภาพ Power BI จะถูกสร้างขึ้นโดยใช้ข้อมูลจากชุดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="683cd-105">A Power BI visualization is constructed using data from your datasets.</span></span> <span data-ttu-id="683cd-106">หากคุณสนใจที่เห็นเบื้องหลัง Power BI ให้คุณสามารถ *แสดง* ข้อมูลที่กำลังกำลังมีการใช้เพื่อสร้างภาพดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="683cd-106">If you're interested in seeing behind-the-scenes, Power BI lets you *display* the data that is being used to create the visual.</span></span> <span data-ttu-id="683cd-107">เมื่อคุณเลือก **แสดงข้อมูล** Power BI แสดงข้อมูลด้านล่าง (หรือถัดจาก) การแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="683cd-107">When you select **Show Data**, Power BI displays the data below (or next to) the visualization.</span></span>

<span data-ttu-id="683cd-108">นอกจากนี้ คุณยังสามารถส่งออกข้อมูลที่กำลังมีการใช้งานเพื่อสร้างการแสดงภาพเป็นไฟล์ .xlsx หรือ .csv และดูใน Excel</span><span class="sxs-lookup"><span data-stu-id="683cd-108">You can also export the data that is being used to create the visualization as an .xlsx or .csv file and view it in Excel.</span></span> <span data-ttu-id="683cd-109">สำหรับข้อมูลเพิ่มเติม ดู[ส่งออกข้อมูลจากการแสดงภาพ Power BI](power-bi-visualization-export-data.md)</span><span class="sxs-lookup"><span data-stu-id="683cd-109">For more information, see [Export data from Power BI visualizations](power-bi-visualization-export-data.md).</span></span>

> [!NOTE]
> <span data-ttu-id="683cd-110">ทั้ง *แสดงข้อมูล* และ *ส่งออกข้อมูล* มีใช้งานในบริการ Power BI และ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="683cd-110">*Show Data* and *Export Data* are both available in Power BI service and Power BI Desktop.</span></span> <span data-ttu-id="683cd-111">อย่างไรก็ตาม Power BI Desktop มีรายละเอียดเพิ่มเติมอีกหนึ่งขั้น [*แสดงบันทึก* จะแสดงแถวจริงจากชุดข้อมูล](../create-reports/desktop-see-data-see-records.md)</span><span class="sxs-lookup"><span data-stu-id="683cd-111">However, Power BI Desktop provides one additional layer of detail; [*Show Records* displays the actual rows from the dataset](../create-reports/desktop-see-data-see-records.md).</span></span>
> 
> 

## <a name="using-show-data"></a><span data-ttu-id="683cd-112">ใช้ *แสดงข้อมูล*</span><span class="sxs-lookup"><span data-stu-id="683cd-112">Using *Show Data*</span></span> 
1. <span data-ttu-id="683cd-113">ใน Power BI Desktop ให้เลือกการแสดงผลข้อมูลด้วยภาพเพื่อเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="683cd-113">In Power BI Desktop, select a visualization to make it active.</span></span>

2. <span data-ttu-id="683cd-114">เลือก **การดำเนินการเพิ่มเติม** (...) และเลือก **แสดงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="683cd-114">Select **More actions** (...) and choose **Show data**.</span></span> 
    <span data-ttu-id="683cd-115">![ตัวเลือกการแสดงสำหรับแสดงข้อมูล](media/service-reports-show-data/power-bi-more-action.png)</span><span class="sxs-lookup"><span data-stu-id="683cd-115">![display option for Show Data](media/service-reports-show-data/power-bi-more-action.png)</span></span>


3. <span data-ttu-id="683cd-116">ตามค่าเริ่มต้น ข้อมูลจะแสดงที่ด้านล่างภาพ</span><span class="sxs-lookup"><span data-stu-id="683cd-116">By default, the data displays below the visual.</span></span>
   
   ![ข้อมูลและภาพแสดงในแนวตั้ง](media/service-reports-show-data/power-bi-show-data-below.png)

4. <span data-ttu-id="683cd-118">หากต้องการเปลี่ยนการวางแนว โปรดเลือกเค้าโครงแนวตั้ง</span><span class="sxs-lookup"><span data-stu-id="683cd-118">To change the orientation, select vertical layout</span></span> ![ภาพหน้าจอขนาดเล็กของไอคอนที่ใช้ในการเปลี่ยนเป็นเค้าโครงแนวตั้ง](media/service-reports-show-data/power-bi-vertical-icon-new.png) <span data-ttu-id="683cd-120">บริเวณมุมบนขวาของการแสดงผลภาพ</span><span class="sxs-lookup"><span data-stu-id="683cd-120">from the top-right corner of the visualization.</span></span>
   
   ![ภาพและข้อมูลแสดงในแนวนอน](media/service-reports-show-data/power-bi-show-data-side.png)
5. <span data-ttu-id="683cd-122">เมื่อต้องการส่งออกข้อมูลไปยังไฟล์ .csv เลือกจุดไข่ปลาแล้วเลือก **ส่งออกข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="683cd-122">To export the data to a .csv file, select the ellipses and choose **Export data**.</span></span>
   
    ![เลือกส่งออกข้อมูล](media/service-reports-show-data/power-bi-export-data-new.png)
   
    <span data-ttu-id="683cd-124">สำหรับข้อมูลเพิ่มเติมในการส่งออกข้อมูลไปยัง Exel ดู[ส่งออกข้อมูลจากการแสดงภาพ Power BI](power-bi-visualization-export-data.md)</span><span class="sxs-lookup"><span data-stu-id="683cd-124">For more information on exporting the data to Excel, see [Export data from Power BI visualizations](power-bi-visualization-export-data.md).</span></span>
6. <span data-ttu-id="683cd-125">เมื่อต้องซ่อนข้อมูล ยกเลิกเลือก **สำรวจ** > **แสดงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="683cd-125">To hide the data, de-select **Explore** > **show data**.</span></span>

## <a name="using-show-records"></a><span data-ttu-id="683cd-126">ใช้แสดงเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="683cd-126">Using Show records</span></span>
<span data-ttu-id="683cd-127">คุณยังสามารถมุ่งเน้นไปที่บันทึกข้อมูลเดียวในการแสดงภาพและเจาะลึกรายละเอียดเบื้องหลัง</span><span class="sxs-lookup"><span data-stu-id="683cd-127">You can also focus on one data record in a visualization, and drill into the details behind it.</span></span> 

1. <span data-ttu-id="683cd-128">หากต้องการใช้ **ดูเรกคอร์ด** ให้เลือกการแสดงผลข้อมูลด้วยภาพเพื่อเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="683cd-128">To use **See records**, select a visualization to make it active.</span></span> 

2. <span data-ttu-id="683cd-129">ในริบบอน Desktop ให้เลือกแท็บสำหรับ **เครื่องมือวิชวล** > **ข้อมูล/เจาะรายละเอียด** > **ดูเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="683cd-129">In the Desktop ribbon, select the tab for **Visual tools** > **Data/Drill** > **See records**.</span></span> 

    ![ภาพหน้าจอที่มีการเลือกดูเรกคอร์ด](media/service-reports-show-data/power-bi-see-record.png)

3. <span data-ttu-id="683cd-131">เลือกจุดข้อมูลหรือแถวบนการแสดงผลข้อมูลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="683cd-131">Select a data point or row on the visualization.</span></span> <span data-ttu-id="683cd-132">ในตัวอย่างนี้ เราได้เลือกคอลัมน์ที่สี่จากด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="683cd-132">In this example, we've selected the fourth column from the left.</span></span> <span data-ttu-id="683cd-133">Power BI แสดงเรกคอร์ดชุดข้อมูลสำหรับจุดข้อมูลนี้ให้เรา</span><span class="sxs-lookup"><span data-stu-id="683cd-133">Power BI shows us the dataset record for this data point.</span></span>

    ![ภาพหน้าจอของเรกคอร์ดเดี่ยวจากชุดข้อมูล](media/service-reports-show-data/power-bi-row.png)

4. <span data-ttu-id="683cd-135">เลือก **กลับไปยังรายงาน** เพื่อกลับไปยังพื้นที่รายงานบน Desktop</span><span class="sxs-lookup"><span data-stu-id="683cd-135">Select **Back to report** to return to the Desktop report canvas.</span></span> 

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="683cd-136">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="683cd-136">Considerations and troubleshooting</span></span>

- <span data-ttu-id="683cd-137">ถ้าปุ่ม **ดูเรกคอร์ด** ในริบบอนถูกปิดใช้งาน และแสดงเป็นสีเทา แสดงว่า การแสดงผลข้อมูลด้วยภาพที่เลือกไม่สนับสนุน ดูเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="683cd-137">If the **See records** button in the ribbon is disabled and grayed-out, it means the selected visualization does not support See Records.</span></span>
- <span data-ttu-id="683cd-138">คุณไม่สามารถเปลี่ยนข้อมูลในมุมมอง ดูเรกคอร์ด และบันทึกกลับไปยังรายงานได้</span><span class="sxs-lookup"><span data-stu-id="683cd-138">You can't change the data in the See Records view and save it back to the report.</span></span>
- <span data-ttu-id="683cd-139">คุณไม่สามารถใช้ ดูระเบียน เมื่อวิชวลของคุณใช้หน่วยวัดจากการคำนวณในแบบจำลองหลายมิติ</span><span class="sxs-lookup"><span data-stu-id="683cd-139">You can't use See Records when your visual uses a calculated measure in a multidimensional model.</span></span>
- <span data-ttu-id="683cd-140">คุณไม่สามารถใช้ ดูเรกคอร์ด เมื่อคุณเชื่อมต่อกับแบบจำลองสดแบบหลายมิติ (MD)</span><span class="sxs-lookup"><span data-stu-id="683cd-140">You can't use See Records when you are connected to a live multidimensional (MD) model.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="683cd-141">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="683cd-141">Next steps</span></span>
[<span data-ttu-id="683cd-142">ส่งออกข้อมูลจากการแสดงผลข้อมูลด้วยภาพของ Power BI</span><span class="sxs-lookup"><span data-stu-id="683cd-142">Export data from Power BI visualizations</span></span>](power-bi-visualization-export-data.md)    

<span data-ttu-id="683cd-143">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="683cd-143">More questions?</span></span> [<span data-ttu-id="683cd-144">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="683cd-144">Try the Power BI Community</span></span>](https://community.powerbi.com/)


