---
title: ส่วนที่ 2 เพิ่มการแสดงภาพไปยังรายงาน Power BI
description: ส่วนที่ 2 เพิ่มการแสดงภาพไปยังรายงาน Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 05/06/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 6ddee012d01c64e0f35ac491d2b20ba362f2da90
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412471"
---
# <a name="add-visuals-to-a-power-bi-report-part-2"></a><span data-ttu-id="3d078-103">เพิ่มวิชวลไปยังรายงาน Power BI (ตอนที่ 2)</span><span class="sxs-lookup"><span data-stu-id="3d078-103">Add visuals to a Power BI report (part 2)</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]    

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="3d078-104">ใน[ส่วนที่ 1](power-bi-report-add-visualizations-i.md) คุณได้สร้างภาพพื้นฐานแล้วโดยการเลือกกล่องข้อความถัดจากชื่อเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3d078-104">In [Part 1](power-bi-report-add-visualizations-i.md), you created a basic visualization by selecting checkboxes next to field names.</span></span>  <span data-ttu-id="3d078-105">ในส่วนที่ 2 คุณจะได้เรียนรู้วิธีใช้การลากและวาง และใช้บานหน้าต่าง **เขตข้อมูล** และ **การแสดงผลข้อมูลด้วยภาพ** เต็มรูปแบบเพื่อสร้างและปรับเปลี่ยนการแสดงผลข้อมูลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="3d078-105">In Part 2, you'll learn how to use drag-and-drop and make full use of the **Fields** and **Visualizations** panes to create and modify visualizations.</span></span>


## <a name="create-a-new-visualization"></a><span data-ttu-id="3d078-106">สร้างการแสดงภาพใหม่</span><span class="sxs-lookup"><span data-stu-id="3d078-106">Create a new visualization</span></span>
<span data-ttu-id="3d078-107">ในบทช่วยสอนนี้ เราจะเจาะลึกลงในชุดข้อมูลการวิเคราะห์ร้านค้าปลีก และสร้างการแสดงผลข้อมูลด้วยภาพที่สำคัญสองถึงสามวิชวล</span><span class="sxs-lookup"><span data-stu-id="3d078-107">In this tutorial, we'll dig into our Retail Analysis dataset and create a few key visualizations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3d078-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="3d078-108">Prerequisites</span></span>

<span data-ttu-id="3d078-109">บทช่วยสอนนี้ใช้ [ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix)</span><span class="sxs-lookup"><span data-stu-id="3d078-109">This tutorial uses the [Retail analysis sample PBIX file](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix).</span></span>

1. <span data-ttu-id="3d078-110">จากด้านบนซ้ายของแถบเมนู Power BI Desktop เลือก **ไฟล์** > **เปิด**</span><span class="sxs-lookup"><span data-stu-id="3d078-110">From the upper left section of the Power BI Desktop menu bar, select **File** > **Open**</span></span>
   
2. <span data-ttu-id="3d078-111">ค้นหาสำเนา **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก**</span><span class="sxs-lookup"><span data-stu-id="3d078-111">Find your copy of the **Retail Analysis sample PBIX file**</span></span>

1. <span data-ttu-id="3d078-112">เปิด **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก** ในมุมมองรายงาน ![ภาพหน้าจอไอคอนมุมมองรายงาน](media/power-bi-visualization-kpi/power-bi-report-view.png)</span><span class="sxs-lookup"><span data-stu-id="3d078-112">Open the **Retail Analysis sample PBIX file** in report view ![Screenshot of the report view icon.](media/power-bi-visualization-kpi/power-bi-report-view.png).</span></span>

1. <span data-ttu-id="3d078-113">เลือก</span><span class="sxs-lookup"><span data-stu-id="3d078-113">Select</span></span> ![สกรีนช็อตของแท็บสีเหลือง](media/power-bi-visualization-kpi/power-bi-yellow-tab.png) <span data-ttu-id="3d078-115">หากต้องการเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="3d078-115">to add a new page.</span></span>

## <a name="add-visualizations-to-the-report"></a><span data-ttu-id="3d078-116">เพิ่มการแสดงภาพลงในรายงาน</span><span class="sxs-lookup"><span data-stu-id="3d078-116">Add visualizations to the report</span></span>

<span data-ttu-id="3d078-117">สร้างการแสดงภาพ โดยการเลือกเขตข้อมูลจากบานหน้าต่าง **เขตข้อมูล** บานหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="3d078-117">Create a visualization by selecting a field from the **Fields** pane.</span></span> <span data-ttu-id="3d078-118">ชนิดของการแสดงผลข้อมูลด้วยภาพที่สร้างขึ้นจะขึ้นอยู่กับชนิดของเขตข้อมูลที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3d078-118">The type of visualization created will depend on the type of field selected.</span></span> <span data-ttu-id="3d078-119">Power BI ใช้ชนิดข้อมูลเพื่อระบุว่าการแสดงผลข้อมูลด้วยภาพแบบใดที่จะใช้ในการแสดงผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="3d078-119">Power BI uses the data type to determine which visualization to use to display the results.</span></span> <span data-ttu-id="3d078-120">คุณสามารถเปลี่ยนการแสดงผลข้อมูลด้วยภาพที่ใช้ได้โดยการเลือกไอคอนที่แตกต่างจากบานหน้าต่างการแสดงผลข้อมูลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="3d078-120">You can change the visualization used by selecting a different icon from the Visualizations pane.</span></span> <span data-ttu-id="3d078-121">โปรดทราบว่าไม่ใช่การแสดงผลข้อมูลด้วยภาพทุกชนิดที่สามารถแสดงข้อมูลของคุณได้</span><span class="sxs-lookup"><span data-stu-id="3d078-121">Keep in mind that not all visualizations can display your data.</span></span> <span data-ttu-id="3d078-122">ตัวอย่างเช่น ข้อมูลทางภูมิศาสตร์จะไม่สามารถแสดงผลได้อย่างเหมาะสมหากคุณใช้แผนภูมิกรวยหรือแผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="3d078-122">For example, geographic data will not display well using a funnel chart or line chart.</span></span> 


### <a name="add-an-area-chart-that-looks-at-this-years-sales-compared-to-last-year"></a><span data-ttu-id="3d078-123">เพิ่มแผนภูมิพื้นที่ที่ดูยอดขายของปีนี้เทียบกับปีที่แล้ว</span><span class="sxs-lookup"><span data-stu-id="3d078-123">Add an area chart that looks at this year's sales compared to last year</span></span>

1. <span data-ttu-id="3d078-124">จากตาราง **ยอดขาย** เลือก **ค่ายอดขายของ** > **ปีนี้** และ **ยอดขายของปีที่แล้ว**</span><span class="sxs-lookup"><span data-stu-id="3d078-124">From the **Sales** table, select **This Year Sales** > **Value** and **Last Year Sales**.</span></span> <span data-ttu-id="3d078-125">Power BI สร้างแผนภูมิคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="3d078-125">Power BI creates a column chart.</span></span>  <span data-ttu-id="3d078-126">แผนภูมินี้น่าสนใจ และคุณต้องการเจาะลึกมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="3d078-126">This chart is interesting, and you want to dig deeper.</span></span> <span data-ttu-id="3d078-127">การขายจะมีลักษณะเป็นอย่างไรเมื่อแยกดูเป็นรายเดือน?</span><span class="sxs-lookup"><span data-stu-id="3d078-127">What do the sales look like by month?</span></span>  
   
   ![สกรีนช็อตที่แสดงแผนภูมิคอลัมน์](media/power-bi-report-add-visualizations-ii/power-bi-start.png)

2. <span data-ttu-id="3d078-129">จากตารางเวลา ลาก **เดือนตามรอบบัญชี** ลงในพื้นที่ **แกน**</span><span class="sxs-lookup"><span data-stu-id="3d078-129">From the Time table, drag **FiscalMonth** into the **Axis** area.</span></span>  
   <span data-ttu-id="3d078-130">![สกรีนช็อตที่แสดงแผนภูมิคอลัมน์ที่มี FiscalMonth เป็นแกน](media/power-bi-report-add-visualizations-ii/power-bi-fiscalmonth.png)</span><span class="sxs-lookup"><span data-stu-id="3d078-130">![Screenshot showing column chart with FiscalMonth as axis](media/power-bi-report-add-visualizations-ii/power-bi-fiscalmonth.png)</span></span>

3. <span data-ttu-id="3d078-131">[เปลี่ยนการแสดงผลข้อมูลด้วยภาพ](power-bi-report-change-visualization-type.md)ไปเป็นแผนภูมิพื้นที่</span><span class="sxs-lookup"><span data-stu-id="3d078-131">[Change the visualization](power-bi-report-change-visualization-type.md) to an area chart.</span></span>  <span data-ttu-id="3d078-132">มีการแสดงผลข้อมูลด้วยภาพมากมายหลายชนิดให้คุณเลือก โปรดดู [คำอธิบายของการแสดงผลข้อมูลด้วยภาพแต่ละรายการ คำแนะนำสำหรับแนวทางปฏิบัติที่ดีที่สุด และบทช่วยสอน](power-bi-visualization-types-for-reports-and-q-and-a.md) เพื่อช่วยในการตัดสินใจว่าคุณควรใช้การแสดงผลข้อมูลด้วยภาพชนิดใด</span><span class="sxs-lookup"><span data-stu-id="3d078-132">There are many visualization types to choose from - see [descriptions of each, tips for best practices, and tutorials](power-bi-visualization-types-for-reports-and-q-and-a.md) for help with deciding which type to use.</span></span> <span data-ttu-id="3d078-133">จากบานหน้าต่างการแสดงผลข้อมูลด้วยภาพ ให้เลือกไอคอนแผนภูมิพื้นที่ ![ไอคอนแผนภูมิพื้นที่จากบานหน้าต่างการแสดงผลข้อมูลด้วยภาพ](media/power-bi-report-add-visualizations-ii/power-bi-area-chart.png)</span><span class="sxs-lookup"><span data-stu-id="3d078-133">From the Visualizations pane, select the area chart icon ![Area chart icon from Visualizations pane](media/power-bi-report-add-visualizations-ii/power-bi-area-chart.png).</span></span>

4. <span data-ttu-id="3d078-134">เรียงลำดับการแสดงผลข้อมูลด้วยภาพโดยการเลือก **ตัวเลือกเพิ่มเติม** (...) แล้วเลือก **เรียงลำดับตาม** >  **FiscalMonth**</span><span class="sxs-lookup"><span data-stu-id="3d078-134">Sort the visualization by selecting **More actions** (...) and choosing **Sort by** >  **FiscalMonth**.</span></span>

5. <span data-ttu-id="3d078-135">[ปรับขนาดการแสดงภาพ](power-bi-visualization-move-and-resize.md)โดยเลือกการแสดงภาพ จับที่เค้าร่างวงกลมหนึ่งวงและลาก</span><span class="sxs-lookup"><span data-stu-id="3d078-135">[Resize the visualization](power-bi-visualization-move-and-resize.md) by selecting the visualization, grabbing one of the outline circles and dragging.</span></span> <span data-ttu-id="3d078-136">ทำให้กว้างพอที่จะกำจัดแถบเลื่อน และเล็กพอที่จะมีพื้นที่ให้เราเพิ่มการแสดงภาพแบบอื่นได้</span><span class="sxs-lookup"><span data-stu-id="3d078-136">Make it wide enough to eliminate the scrollbar and small enough to give us enough room to add another visualization.</span></span>
   
   ![สกรีนช็อตของวิชวลแผนภูมิพื้นที่](media/power-bi-report-add-visualizations-ii/pbi_part2_7b.png)
6. <span data-ttu-id="3d078-138">[บันทึกรายงาน](../create-reports/service-report-save.md)</span><span class="sxs-lookup"><span data-stu-id="3d078-138">[Save the report](../create-reports/service-report-save.md).</span></span>

### <a name="add-a-map-visualization-that-looks-at-sales-by-location"></a><span data-ttu-id="3d078-139">เพิ่มการแสดงภาพของแผนที่ท่ี่ดูยอดขายตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="3d078-139">Add a map visualization that looks at sales by location</span></span>

1. <span data-ttu-id="3d078-140">จากตาราง **ร้านค้า** เลือก **ดินแดน**</span><span class="sxs-lookup"><span data-stu-id="3d078-140">From the **Store** table, select **Territory**.</span></span> <span data-ttu-id="3d078-141">ลาก **ร้านค้ารวม** ลงในพื้นที่ขนาด</span><span class="sxs-lookup"><span data-stu-id="3d078-141">Drag **Total Stores** into the Size area.</span></span> <span data-ttu-id="3d078-142">Power BI จดจำว่าดินแดน (Territory) เป็นตำแหน่งที่ตั้งหนึ่ง และสร้างการแสดงภาพของแผนที่หนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3d078-142">Power BI recognizes that Territory is a location, and creates a map visualization.</span></span>  
   <span data-ttu-id="3d078-143">![แผนภูมิพื้นที่](media/power-bi-report-add-visualizations-ii/power-bi-map1.png)</span><span class="sxs-lookup"><span data-stu-id="3d078-143">![Area chart](media/power-bi-report-add-visualizations-ii/power-bi-map1.png)</span></span>

2. <span data-ttu-id="3d078-144">เพิ่มคำอธิบายแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="3d078-144">Add a legend.</span></span>  <span data-ttu-id="3d078-145">เมื่อต้องการดูข้อมูลตามชื่อร้านค้า ให้ลาก **Store** > **Chain** ไปยังพื้นที่คำอธิบายแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="3d078-145">To see the data by store name, drag **Store** > **Chain** into the Legend area.</span></span>  
   <span data-ttu-id="3d078-146">![พื้นที่รายงานที่มีลูกศรจากเชนในรายการเขตข้อมูลไปยังเชนในกลุ่มคำอธิบายแผนภูมิ](media/power-bi-report-add-visualizations-ii/power-bi-chain.png)</span><span class="sxs-lookup"><span data-stu-id="3d078-146">![report canvas with arrow from Chain in fields list to Chain in Legend bucket](media/power-bi-report-add-visualizations-ii/power-bi-chain.png)</span></span>

> [!NOTE]
> <span data-ttu-id="3d078-147">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="3d078-147">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span> <span data-ttu-id="3d078-148">ดู [การแชร์รายงาน](../collaborate-share/service-share-reports.md)</span><span class="sxs-lookup"><span data-stu-id="3d078-148">See [sharing reports](../collaborate-share/service-share-reports.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="3d078-149">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3d078-149">Next steps</span></span>
* <span data-ttu-id="3d078-150">อ่านเพิ่มเติมเกี่ยวกับ[การแสดงภาพในรายงาน Power BI](power-bi-report-visualizations.md)</span><span class="sxs-lookup"><span data-stu-id="3d078-150">More about [Visualizations in Power BI reports](power-bi-report-visualizations.md).</span></span>  
* <span data-ttu-id="3d078-151">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3d078-151">More questions?</span></span> [<span data-ttu-id="3d078-152">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="3d078-152">Try the Power BI Community</span></span>](https://community.powerbi.com/)

