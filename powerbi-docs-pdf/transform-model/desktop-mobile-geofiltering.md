---
title: ตั้งค่าตัวกรองทางภูมิศาสตร์ใน Power BI Desktop สำหรับแอปบนอุปกรณ์เคลื่อนที่
description: เมื่อคุณตั้งค่าการกรองทางภูมิศาสตร์ในรูปแบบข้อมูลของคุณใน Power BI Desktop คุณสามารถกรองข้อมูลตามตำแหน่งของคุณได้โดยอัตโนมัติในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่
author: paulinbar
ms.author: painbar
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: how-to
ms.date: 01/16/2018
LocalizationGroup: Model your data
ms.openlocfilehash: 2368732d5f0f5fe6b0c32ac535068725e8620215
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413997"
---
# <a name="set-geographic-filters-in-power-bi-desktop-for-use-in-the-mobile-app"></a><span data-ttu-id="d712e-103">ตั้งค่าตัวกรองทางภูมิศาสตร์ใน Power BI Desktop สำหรับใช้ในแอปบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="d712e-103">Set geographic filters in Power BI Desktop for use in the mobile app</span></span>
<span data-ttu-id="d712e-104">ใน Power BI Desktop คุณสามารถ[จัดประเภทข้อมูลทางภูมิศาสตร์](desktop-data-categorization.md)สำหรับคอลัมน์ เพื่อให้ Power BI Desktop ทราบว่าควรทำอย่างไรกับค่าในวิชวลในรายงานได้</span><span class="sxs-lookup"><span data-stu-id="d712e-104">In Power BI Desktop, you can [categorize geographical data](desktop-data-categorization.md) for a column, so Power BI Desktop knows how to treat values in visuals in a report.</span></span> <span data-ttu-id="d712e-105">ประโยชน์เพิ่มเติมคือ เมื่อคุณหรือเพื่อนร่วมงานของคุณดูรายงานนั้นในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่ Power BI ใช้ตัวกรองทางภูมิศาสตร์ที่ตรงกับตำแหน่งของคุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d712e-105">As an added benefit, when you or your colleagues view that report in the Power BI mobile apps, Power BI automatically provides geographical filters that match where you are.</span></span> 

<span data-ttu-id="d712e-106">ตัวอย่างเช่น คุณเป็นผู้จัดการฝ่ายขาย และกำลังเดินทางไปพบลูกค้า และคุณต้องการจะกรองยอดขายและรายได้สำหรับลูกค้าที่คุณกำลังจะไปพบอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="d712e-106">For example, say you're a sales manager traveling to meet customers, and you'd like to quickly filter the total sales and revenue for the specific customer you're planning to visit.</span></span> <span data-ttu-id="d712e-107">คุณต้องการแยกดูเฉพาะข้อมูลสำหรับตำแหน่งปัจจุบันของคุณ ไม่ว่า จะเป็น รัฐ เมือง หรือที่อยู่</span><span class="sxs-lookup"><span data-stu-id="d712e-107">You want to break out the data for your current location, whether by state, city, or an actual address.</span></span> <span data-ttu-id="d712e-108">ต่อไป ถ้าคุณมีเวลาเหลือ คุณอยากจะไปเยี่ยมลูกค้ารายอื่น ๆ อยู่ที่ใกล้</span><span class="sxs-lookup"><span data-stu-id="d712e-108">Later, if you have time left, you'd like to visit other customers located nearby.</span></span> <span data-ttu-id="d712e-109">คุณสามารถ[กรองรายงานตามตำแหน่งของคุณเพื่อค้นหาลูกค้าเหล่านั้น](../consumer/mobile/mobile-apps-geographic-filtering.md)ได้</span><span class="sxs-lookup"><span data-stu-id="d712e-109">You can [filter the report by your location to find those customers](../consumer/mobile/mobile-apps-geographic-filtering.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d712e-110">คุณสามารถกรองข้อมูลตามตำแหน่งที่ตั้งในแอปสำหรับอุปกรณ์เคลื่อนที่ ก็ต่อเมื่อชื่อภูมิศาสตร์ในรายงานเป็นภาษาอังกฤษเท่านั้น &#150; เช่น "New York" หรือ "Germany"</span><span class="sxs-lookup"><span data-stu-id="d712e-110">You can only filter by location in the mobile app if the geographic names in the report are in English &#150; for example, "New York City" or "Germany".</span></span>
> 
> 

## <a name="identify-geographic-data-in-your-report"></a><span data-ttu-id="d712e-111">ระบุข้อมูลทางภูมิศาสตร์ในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="d712e-111">Identify geographic data in your report</span></span>
1. <span data-ttu-id="d712e-112">ใน Power BI Desktop สลับไปยังมุมมองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d712e-112">In Power BI Desktop, switch to Data View</span></span> ![ไอคอนมุมมองข้อมูล](media/desktop-mobile-geofiltering/pbi_desktop_data_icon.png)<span data-ttu-id="d712e-114">.</span><span class="sxs-lookup"><span data-stu-id="d712e-114">.</span></span>
2. <span data-ttu-id="d712e-115">เลือกคอลัมน์ที่เป็นข้อมูลทางภูมิศาสตร์ &#151; ตัวอย่างเช่น คอลัมน์เมือง</span><span class="sxs-lookup"><span data-stu-id="d712e-115">Select a column with geographic data &#151; for example, a City column.</span></span>
   
    ![คอลัมน์เมือง](media/desktop-mobile-geofiltering/power-bi-desktop-geo-column.png)
3. <span data-ttu-id="d712e-117">บนแท็บ **การวางรูปแบบ** เลือก **ประเภทข้อมูล** จากนั้นเลือกประเภทที่ถูกต้อง &#151; ในตัวอย่างนี้คือ **เมือง**</span><span class="sxs-lookup"><span data-stu-id="d712e-117">On the **Modeling** tab, select **Data Category**, then the correct category &#151; in this example, **City**.</span></span>
   
    ![กล่องประเภทข้อมูล](media/desktop-mobile-geofiltering/power-bi-desktop-geo-category.png)
4. <span data-ttu-id="d712e-119">ตั้งค่าประเภทข้อมูลทางภูมิศาสตร์สำหรับเขตข้อมูลอื่น ๆ ในรูปแบบข้อมูลต่อ</span><span class="sxs-lookup"><span data-stu-id="d712e-119">Continue setting geographic data categories for any other fields in the model.</span></span> 
   
   > [!NOTE]
   > <span data-ttu-id="d712e-120">คุณสามารถตั้งค่าหลายคอลัมน์ สำหรับแต่ละประเภทข้อมูลในรูปแบบ แต่ถ้าคุณทำแบบนั้น แอป Power BI สำหรับอุปกรณ์เคลื่อนที่ จะไม่สามารถกรองรูปแบบตามภูมิศาสตร์ได้</span><span class="sxs-lookup"><span data-stu-id="d712e-120">You can set multiple columns for each data category in a model, but if you do the model can't filter for geography in the Power BI mobile app.</span></span> <span data-ttu-id="d712e-121">เพื่อใช้การกรองทางภูมิศาสตร์ในแอปสำหรับอุปกรณ์เคลื่อนที่ ตั้งค่าแค่คอลัมน์เดียวเท่านั้นสำหรับแต่ละประเภทข้อมูล &#151; เช่น มีคอลัมน์ **เมือง** แค่คอลัมน์เดียว คอลัมน์ **รัฐหรือจังหวัด** คอลัมน์เดียว และคอลัมน์ **ประเทศ** คอลัมน์เดียว</span><span class="sxs-lookup"><span data-stu-id="d712e-121">To use geographic filtering in the mobile apps, set only one column for each data category &#151; for example, only one **City** column, one **State or Province** column, and one **Country** column.</span></span> 
   > 
   > 

## <a name="create-visuals-with-your-geographic-data"></a><span data-ttu-id="d712e-122">สร้างวิชวลด้วยข้อมูลทางภูมิศาสตร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d712e-122">Create visuals with your geographic data</span></span>
1. <span data-ttu-id="d712e-123">สลับไปยังมุมมองรายงาน</span><span class="sxs-lookup"><span data-stu-id="d712e-123">Switch to Report view</span></span> ![ไอคอนมุมมองรายงาน](media/desktop-mobile-geofiltering/power-bi-desktop-report-icon.png)<span data-ttu-id="d712e-125">และสร้างวิชวลที่ใช้เขตข้อมูลทางภูมิศาสตร์ในข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="d712e-125">, and create visuals that use the geographic fields in your data.</span></span> 
   
    ![รายงานที่มีแผนที่](media/desktop-mobile-geofiltering/power-bi-desktop-geo-report.png)
   
    <span data-ttu-id="d712e-127">ในตัวอย่างนี้ รูปแบบข้อมูลยังประกอบด้วยคอลัมน์จากการคำนวณ ที่รวมเมืองและรัฐเข้าด้วยกันเป็นหนึ่งคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="d712e-127">In this example, the model also contains a calculated column that brings city and state together in one column.</span></span> <span data-ttu-id="d712e-128">อ่านเกี่ยวกับ[สร้างคอลัมน์จากการคำนวณใน Power BI Desktop](desktop-calculated-columns.md)</span><span class="sxs-lookup"><span data-stu-id="d712e-128">Read about [creating calculated columns in Power BI Desktop](desktop-calculated-columns.md).</span></span>
   
    ![เขตข้อมูล เมือง + รัฐ](media/desktop-mobile-geofiltering/power-bi-desktop-city-state-column.png)
2. <span data-ttu-id="d712e-130">เผยแพร่รายงานไปยังบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="d712e-130">Publish the report to the Power BI service.</span></span>

## <a name="view-the-report-in-power-bi-mobile-app"></a><span data-ttu-id="d712e-131">ดูรายงานในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="d712e-131">View the report in Power BI mobile app</span></span>
1. <span data-ttu-id="d712e-132">เปิดรายงานในใด ๆ ใน[แอป Power BI สำหรับอุปกรณ์เคลื่อนที่](../consumer/mobile/mobile-apps-for-mobile-devices.md)</span><span class="sxs-lookup"><span data-stu-id="d712e-132">Open the report in any of the [Power BI mobile apps](../consumer/mobile/mobile-apps-for-mobile-devices.md).</span></span>
2. <span data-ttu-id="d712e-133">ถ้าคุณอยู่ในตำแหน่งทางภูมิศาสตร์ที่มีข้อมูลในรายงาน คุณสามารถกรองข้อมูลนั้นด้วยตำแหน่งของคุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d712e-133">If you're in a geographic location with data in the report, you can filter it automatically to your location.</span></span>
   
    ![ตัวกรองทางภูมิศาสตร์ในแอปสำหรับอุปกรณ์เคลื่อนที่](media/desktop-mobile-geofiltering/power-bi-mobile-geo-map-set-filter.png)

<span data-ttu-id="d712e-135">อ่านเพิ่มเติมเกี่ยวกับ[การกรองรายงานตามตำแหน่งในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่](../consumer/mobile/mobile-apps-geographic-filtering.md)</span><span class="sxs-lookup"><span data-stu-id="d712e-135">Read more about [filtering a report by location in the Power BI mobile apps](../consumer/mobile/mobile-apps-geographic-filtering.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="d712e-136">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d712e-136">Next steps</span></span>
* [<span data-ttu-id="d712e-137">จัดประเภทข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d712e-137">Data categorization in Power BI Desktop</span></span>](desktop-data-categorization.md)  
* <span data-ttu-id="d712e-138">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d712e-138">Questions?</span></span> [<span data-ttu-id="d712e-139">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="d712e-139">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
