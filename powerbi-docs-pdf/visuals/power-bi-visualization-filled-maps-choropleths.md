---
title: แผนที่แถบสี (Choropleth) ใน Power BI
description: เอกสารประกอบเรื่องการสร้างแผนที่แถบสี (Choropleth) ใน Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
featuredvideoid: ''
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 12/05/2019
LocalizationGroup: Visualizations
ms.openlocfilehash: bfcd684e4899edb5555a784c7148a7abc9b0f29c
ms.sourcegitcommit: 5c09d121d3205e65fb33a2eca0e60bc30e777773
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/18/2020
ms.locfileid: "97675315"
---
# <a name="create-and-use-filled-maps-choropleth-maps-in-power-bi"></a><span data-ttu-id="8fd4c-103">สร้างและใช้แผนที่แถบสี (แผนที่ choropleths) ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8fd4c-103">Create and use filled maps (choropleth maps) in Power BI</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="8fd4c-104">แผนที่แถบสีใช้เฉดสีหรือ หรือการปรับสีอ่อนแก่ หรือรูปแบบต่าง ๆ เพื่อแสดงว่าค่าแตกต่างกันมากเพียงใดในสัดส่วนทั่วทั้งภูมิศาสตร์หรือภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="8fd4c-104">A filled map uses shading or tinting or patterns to display how a value differs in proportion across a geography or region.</span></span>  <span data-ttu-id="8fd4c-105">เพื่อแสดงความแตกต่างเหล่านี้ที่สัมพันธ์กับเฉดสีที่อยู่ในช่วงจากสีอ่อน (ความถี่น้อยกว่า/ต่ำกว่า) ไปถึงเข้ม (ความถี่มากกว่า/สูงกว่า) ได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="8fd4c-105">Quickly display these relative differences with shading that ranges from light (less-frequent/lower) to dark (more-frequent/more).</span></span>    

![แผนที่ของสหรัฐอเมริกา](media/power-bi-visualization-filled-maps-choropleths/large-map.png)

## <a name="what-is-sent-to-bing"></a><span data-ttu-id="8fd4c-107">สิ่งที่จะถูกส่งไปยัง Bing</span><span class="sxs-lookup"><span data-stu-id="8fd4c-107">What is sent to Bing</span></span>
<span data-ttu-id="8fd4c-108">Power BI รวมเข้ากับ Bing เพื่อให้มีพิกัดแมปเริ่มต้น (กระบวนการที่เรียกว่า การกำหนดรหัสทางภูมิศาสตร์)</span><span class="sxs-lookup"><span data-stu-id="8fd4c-108">Power BI integrates with Bing to provide default map coordinates (a process called geo-coding).</span></span> <span data-ttu-id="8fd4c-109">เมื่อคุณสร้างการแสดงภาพของแผนที่ในบริการ Power BI หรือ Power BI Desktop ข้อมูลในบักเก็ต **ตำแหน่งที่ตั้ง** **ละติจูด** และ **ลองติจู** (ที่กำลังถูกใช้เพื่อสร้างการแสดงภาพนั้น) จะถูกส่งไปยัง Bing</span><span class="sxs-lookup"><span data-stu-id="8fd4c-109">When you create a map visualization in Power BI service or Power BI Desktop, the data in the **Location**, **Latitude**, and **Longitude** buckets (that is being used to create that visualization) is sent to Bing.</span></span>

<span data-ttu-id="8fd4c-110">คุณหรือผู้ดูแลระบบของคุณอาจจำเป็นต้องอัปเดตไฟร์วอลล์ของคุณเพื่ออนุญาตให้เข้าถึง URL ที่ Bing ใช้สำหรับการกำหนดพิกัดทางภูมิศาสตร์</span><span class="sxs-lookup"><span data-stu-id="8fd4c-110">You, or your administrator, may need to update your firewall to allow access to the URLs Bing uses for geocoding.</span></span>  <span data-ttu-id="8fd4c-111">URL เหล่านั้นคือ:</span><span class="sxs-lookup"><span data-stu-id="8fd4c-111">Those URLs are:</span></span>
- https://dev.virtualearth.net/REST/V1/Locations    
- https://platform.bing.com/geo/spatial/v1/public/Geodata    
- https://www.bing.com/api/maps/mapcontrol

<span data-ttu-id="8fd4c-112">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับข้อมูลที่ถูกส่งไปยัง Bing และสำหรับเคล็ดลับในการเพิ่มความสำเร็จการกำหนดรหัสทางภูมิศาสตร์ของคุณ ดู[คำแนะนำและเคล็ดลับสำหรับการแสดงภาพแผนที่](power-bi-map-tips-and-tricks.md)</span><span class="sxs-lookup"><span data-stu-id="8fd4c-112">For more information about the data being sent to Bing, and for tips to increase your geo-coding success, see [Tips and tricks for map visualizations](power-bi-map-tips-and-tricks.md).</span></span>

## <a name="when-to-use-a-filled-map"></a><span data-ttu-id="8fd4c-113">เมื่อใดควรใช้แผนที่แถบสี</span><span class="sxs-lookup"><span data-stu-id="8fd4c-113">When to use a filled map</span></span>
<span data-ttu-id="8fd4c-114">แผนที่แถบสีเป็นทางเลือกที่เหมาะสมอย่างยิ่งในกรณีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8fd4c-114">Filled maps are a great choice:</span></span>

* <span data-ttu-id="8fd4c-115">เมื่อต้องแสดงข้อมูลเชิงปริมาณบนแผนที่</span><span class="sxs-lookup"><span data-stu-id="8fd4c-115">to display quantitative information on a map.</span></span>
* <span data-ttu-id="8fd4c-116">เมื่อต้องแสดงรูปแบบเชิงพื้นที่และความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="8fd4c-116">to show spatial patterns and relationships.</span></span>
* <span data-ttu-id="8fd4c-117">เมื่อข้อมูลของคุณคือข้อมูลมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="8fd4c-117">when your data is standardized.</span></span>
* <span data-ttu-id="8fd4c-118">เมื่อทำงานกับข้อมูลด้านสังคมและเศรษฐกิจ</span><span class="sxs-lookup"><span data-stu-id="8fd4c-118">when working with socioeconomic data.</span></span>
* <span data-ttu-id="8fd4c-119">เมื่อภูมิภาคที่กำหนดไว้มีความสำคัญ</span><span class="sxs-lookup"><span data-stu-id="8fd4c-119">when defined regions are important.</span></span>
* <span data-ttu-id="8fd4c-120">เมื่อต้องดูภาพรวมของการกระจายทั่วทั้งตำแหน่งที่ตั้งทางภูมิศาสตร์</span><span class="sxs-lookup"><span data-stu-id="8fd4c-120">to get an overview of the distribution across the geographic locations.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="8fd4c-121">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="8fd4c-121">Prerequisites</span></span>
<span data-ttu-id="8fd4c-122">บทช่วยสอนนี้ใช้[ไฟล์ PBIX ตัวอย่างการขายและการตลาด](https://download.microsoft.com/download/9/7/6/9767913A-29DB-40CF-8944-9AC2BC940C53/Sales%20and%20Marketing%20Sample%20PBIX.pbix)</span><span class="sxs-lookup"><span data-stu-id="8fd4c-122">This tutorial uses the [Sales and Marketing sample PBIX file](https://download.microsoft.com/download/9/7/6/9767913A-29DB-40CF-8944-9AC2BC940C53/Sales%20and%20Marketing%20Sample%20PBIX.pbix).</span></span>
1. <span data-ttu-id="8fd4c-123">จากด้านบนซ้ายของแถบเมนู เลือก **ไฟล์** > **เปิด**</span><span class="sxs-lookup"><span data-stu-id="8fd4c-123">From the upper left section of the menu bar, select **File** > **Open**</span></span>
   
2. <span data-ttu-id="8fd4c-124">ค้นหาสำเนาของ **ไฟล์ PBIX ตัวอย่างการขายและการตลาด** ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8fd4c-124">Find your copy of the **Sales and Marketing sample PBIX file**</span></span>

1. <span data-ttu-id="8fd4c-125">เปิด **ไฟล์ PBIX ตัวอย่างการขายและการตลาด** ในมุมมองรายงาน ![สกรีนช็อตไอคอนมุมมองรายงาน](media/power-bi-visualization-kpi/power-bi-report-view.png)</span><span class="sxs-lookup"><span data-stu-id="8fd4c-125">Open the **Sales and Marketing sample PBIX file** in report view ![Screenshot of the report view icon.](media/power-bi-visualization-kpi/power-bi-report-view.png).</span></span>

1. <span data-ttu-id="8fd4c-126">เลือก</span><span class="sxs-lookup"><span data-stu-id="8fd4c-126">Select</span></span> ![สกรีนช็อตของแท็บสีเหลือง](media/power-bi-visualization-kpi/power-bi-yellow-tab.png) <span data-ttu-id="8fd4c-128">หากต้องการเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="8fd4c-128">to add a new page.</span></span>

> [!NOTE]
> <span data-ttu-id="8fd4c-129">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="8fd4c-129">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span>    

### <a name="create-a-filled-map"></a><span data-ttu-id="8fd4c-130">สร้างแผนที่แถบสี</span><span class="sxs-lookup"><span data-stu-id="8fd4c-130">Create a filled map</span></span>
1. <span data-ttu-id="8fd4c-131">จากบานหน้าต่างเขตข้อมูล เลือกเขตข้อมูล **ภูมิศาสตร์**\>**รัฐ**</span><span class="sxs-lookup"><span data-stu-id="8fd4c-131">From the Fields pane, select the **Geo** \> **State** field.</span></span>    

   ![เครื่องหมายเลือกสีเหลืองถัดจากรัฐ](media/power-bi-visualization-filled-maps-choropleths/power-bi-state.png)
2. <span data-ttu-id="8fd4c-133">[แปลงแผนภูมิ](power-bi-report-change-visualization-type.md)ให้เป็นแผนภูมิแถบสี</span><span class="sxs-lookup"><span data-stu-id="8fd4c-133">[Convert the chart](power-bi-report-change-visualization-type.md) to a filled map.</span></span> <span data-ttu-id="8fd4c-134">โปรดสังเกตว่าตอนนี้ **รัฐ** อยู่ในแอ่ง **ตำแหน่งที่ตั้ง**</span><span class="sxs-lookup"><span data-stu-id="8fd4c-134">Notice that **State** is now in the **Location** well.</span></span> <span data-ttu-id="8fd4c-135">Bing Maps ใช้เขตข้อมูลในแอ่ง **ตำแหน่งที่ตั้ง** เพื่อสร้างแผนที่</span><span class="sxs-lookup"><span data-stu-id="8fd4c-135">Bing Maps uses the field in the **Location** well to create the map.</span></span>  <span data-ttu-id="8fd4c-136">ตำแหน่งที่ตั้งสามารถเป็นตำแหน่งที่ตั้งที่มีอยู่จริงต่าง ๆ: ประเทศ รัฐ เขต เมือง รหัสไปรษณีย์ หรืออื่น ๆ Bing Maps มีรูปร่างแผนผังแถบสีสำหรับตำแหน่งที่ตั้งต่าง ๆ ทั่วโลก</span><span class="sxs-lookup"><span data-stu-id="8fd4c-136">The location can be a variety of valid locations: countries, states, counties, cities, zip codes, or other postal codes etc. Bing Maps provides filled map shapes for locations around the world.</span></span> <span data-ttu-id="8fd4c-137">หากรายการที่ใส่ในแอ่งตำแหน่งที่ตั้งไม่ถูกต้อง Power BI จะไม่สามารถสร้างแผนผังแถบสีได้</span><span class="sxs-lookup"><span data-stu-id="8fd4c-137">Without a valid entry in the Location well, Power BI cannot create the filled map.</span></span>  

   ![เทมเพลตที่มีไอคอนสำหรับแผนที่แถบสีถูกไฮไลต์แล้ว](media/power-bi-visualization-filled-maps-choropleths/img003.png)
3. <span data-ttu-id="8fd4c-139">กรองแผนที่เพื่อแสดงเฉพาะแผ่นดินใหญ่สหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="8fd4c-139">Filter the map to display only the continental United States.</span></span>

   <span data-ttu-id="8fd4c-140">a.</span><span class="sxs-lookup"><span data-stu-id="8fd4c-140">a.</span></span>  <span data-ttu-id="8fd4c-141">ที่ด้านซ้ายของช่องการแสดงภาพ ค้นหาพื้นที่ **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="8fd4c-141">To the left of the Visualizations pane, look for the **Filters** pane.</span></span> <span data-ttu-id="8fd4c-142">ขยายถ้ามีการย่อเล็กสุด</span><span class="sxs-lookup"><span data-stu-id="8fd4c-142">Expand it if it is minimized</span></span>

   <span data-ttu-id="8fd4c-143">b.</span><span class="sxs-lookup"><span data-stu-id="8fd4c-143">b.</span></span>  <span data-ttu-id="8fd4c-144">เลื่อนไปเหนือ **รัฐ** และเลือกเครื่องหมายรูปตัววี (V) ที่ขยาย</span><span class="sxs-lookup"><span data-stu-id="8fd4c-144">Hover over **State** and select the expand chevron</span></span>  
   <span data-ttu-id="8fd4c-145">![ตัวกรองระดับภาพที่แสดง รัฐ(ทั้งหมด)](media/power-bi-visualization-filled-maps-choropleths/img004.png)</span><span class="sxs-lookup"><span data-stu-id="8fd4c-145">![Visual level filters showing State(All)](media/power-bi-visualization-filled-maps-choropleths/img004.png)</span></span>

   <span data-ttu-id="8fd4c-146">c.</span><span class="sxs-lookup"><span data-stu-id="8fd4c-146">c.</span></span>  <span data-ttu-id="8fd4c-147">ทำเครื่องหมายถูกถัดจาก **ทั้งหมด** และนำเครื่องหมายถูกออกถัดจาก **AK**</span><span class="sxs-lookup"><span data-stu-id="8fd4c-147">Place a check mark next to **All** and remove the check mark next to **AK**.</span></span>

   ![ดรอปดาวน์ รัฐกับทุกรายการและ AK ไม่ได้ถูกเลือก](media/power-bi-visualization-filled-maps-choropleths/img005.png)
4. <span data-ttu-id="8fd4c-149">เลือกไอคอนแปรงลูกกลิ้งเพื่อเปิดบานหน้าต่างจัดรูปแบบ และเลือก **สีข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="8fd4c-149">Select the paint roller icon to open the Formatting pane, and choose **Data colors**.</span></span>

    ![บานหน้าต่างจัดรูปแบบแสดงตัวเลือกสีข้อมูล](media/power-bi-visualization-filled-maps-choropleths/power-bi-colors-data.png)

5. <span data-ttu-id="8fd4c-151">เลือกจุดแนวตั้งสามจุด แล้วเลือก **การจัดรูปแบบตามเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="8fd4c-151">Select the three vertical dots and choose **Conditional formatting**.</span></span>

    ![ปุ่มการจัดรูปแบบตามเงื่อนไขสีข้อมูล](media/power-bi-visualization-filled-maps-choropleths/power-bi-conditional.png)

6. <span data-ttu-id="8fd4c-153">ใช้หน้าจอ **สีตามค่าเริ่มต้น - สีข้อมูล** เพื่อกำหนดวิธีการแรเงาแผนที่แถบสีของคุณ</span><span class="sxs-lookup"><span data-stu-id="8fd4c-153">Use the **Default color - Data colors** screen to determine how your filled map will be shaded.</span></span> <span data-ttu-id="8fd4c-154">ตัวเลือกที่พร้อมใช้งานสำหรับคุณรวมถึงเขตข้อมูลที่ยึดตามฐานการแรเงา และวิธีการปรับใช้การแรเงา</span><span class="sxs-lookup"><span data-stu-id="8fd4c-154">The options available to you include which field to base the shading, and how to apply the shading.</span></span> <span data-ttu-id="8fd4c-155">ในตัวอย่างนี้ เราจะใช้เขตข้อมูล **SalesFact** > **ความคิดเห็น** และการตั้งค่าต่ำสุดสำหรับความคิดเห็นเป็นสีส้มและค่าสูงสุดเป็นสีน้ำเงิน</span><span class="sxs-lookup"><span data-stu-id="8fd4c-155">In this example we're using the field **SalesFact** > **Sentiment**, and setting the lowest value for sentiment as orange and the highest value as blue.</span></span> <span data-ttu-id="8fd4c-156">ค่าที่อยู่ระหว่างค่าสูงสุด และค่าต่ำสุดจะมีแรเงาเป็นสีส้ม และสีน้ำเงิน</span><span class="sxs-lookup"><span data-stu-id="8fd4c-156">Values that fall between the maximum and minimum will be shades of orange and blue.</span></span> <span data-ttu-id="8fd4c-157">ภาพประกอบที่ด้านล่างของหน้าจอจะแสดงช่วงของสีที่จะนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="8fd4c-157">The illustration at the bottom of the screen shows the range of colors that will be used.</span></span> 

    ![เลือกบานหน้าต่างสีตามค่าเริ่มต้นพร้อมความคิดเห็นแล้ว](media/power-bi-visualization-filled-maps-choropleths/power-bi-sentiment-field.png)

7. <span data-ttu-id="8fd4c-159">แผนที่แถบสีจะเป็นสีเขียวและแดง โดยที่สีแดงเป็นตัวแทนตัวเลขความคิดเห็นที่ต่ำกว่า และสีเขียวแสดงตัวเลขความคิดเห็นที่สูงกว่า ซึ่งหมายความว่ามีความเห็นในเชิงบวกมากกว่า</span><span class="sxs-lookup"><span data-stu-id="8fd4c-159">The filled map is shaded in green and red, with red representing the lower sentiment numbers and green representing the higher, more-positive sentiment.</span></span>  <span data-ttu-id="8fd4c-160">เมื่อต้องแสดงรายละเอียดเพิ่มเติม ให้ลากเขตข้อมูลลงในแถบสีเหลืองเขียนคำอธิบายเวลาเอาเมาส์ไปชี้</span><span class="sxs-lookup"><span data-stu-id="8fd4c-160">To display additional detail, drag a field into the Tooltips well.</span></span>  <span data-ttu-id="8fd4c-161">ต่อไปนี้เราได้เพิ่ม **SalesFact** > **ช่องว่างความคิดเห็น**</span><span class="sxs-lookup"><span data-stu-id="8fd4c-161">Here we've added **SalesFact** > **Sentiment gap**.</span></span> <span data-ttu-id="8fd4c-162">การไฮไลท์ถึงสถานะของไอดาโฮ (ID) แสดงให้เราเห็นว่าช่องว่างความคิดเห็นนั้นอยู่ระดับต่ำสุดที่6</span><span class="sxs-lookup"><span data-stu-id="8fd4c-162">Highlighting the state of Idaho (ID) shows us that sentiment gap is low, at 6.</span></span>
   <span data-ttu-id="8fd4c-163">![แผนที่แถบสีแสดงแถบสีเหลืองเขียนคำอธิบายเวลาเอาเมาส์ไปชี้ที่ไอดาโฮ](media/power-bi-visualization-filled-maps-choropleths/power-bi-idaho-filled-map.png)</span><span class="sxs-lookup"><span data-stu-id="8fd4c-163">![filled map showing Idaho tooltips](media/power-bi-visualization-filled-maps-choropleths/power-bi-idaho-filled-map.png)</span></span>

10. <span data-ttu-id="8fd4c-164">[บันทึกรายงาน](../create-reports/service-report-save.md)</span><span class="sxs-lookup"><span data-stu-id="8fd4c-164">[Save the report](../create-reports/service-report-save.md).</span></span>

<span data-ttu-id="8fd4c-165">Power BI ให้คุณควบคุมลักษณะที่ปรากฏของแผนที่ของคุณแถบสีได้มากมาย</span><span class="sxs-lookup"><span data-stu-id="8fd4c-165">Power BI gives you plenty of control over the appearance of your filled map.</span></span> <span data-ttu-id="8fd4c-166">เล่นกับตัวควบคุมสีข้อมูลเหล่านี้จนกว่าคุณได้รับลักษณะที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="8fd4c-166">Play around with these data color controls until you get the look you want.</span></span> 

## <a name="highlighting-and-cross-filtering"></a><span data-ttu-id="8fd4c-167">การทำไฮไลท์และการกรองข้าม</span><span class="sxs-lookup"><span data-stu-id="8fd4c-167">Highlighting and cross-filtering</span></span>
<span data-ttu-id="8fd4c-168">สำหรับข้อมูลเกี่ยวกับการใช้บานหน้าต่างตัวกรอง โปรดดู[เพิ่มตัวกรองไปยังรายงาน](../create-reports/power-bi-report-add-filter.md)</span><span class="sxs-lookup"><span data-stu-id="8fd4c-168">For information about using the Filters pane, see [Add a filter to a report](../create-reports/power-bi-report-add-filter.md).</span></span>

<span data-ttu-id="8fd4c-169">การไฮไลต์ตำแหน่งที่ตั้งหนึ่งในแผนที่แถบสี จะกรองข้ามการแสดงภาพอื่น ๆ บนหน้ารายงานนั้น... และนอกจากนี้จะทำในทางกลับกันด้วย</span><span class="sxs-lookup"><span data-stu-id="8fd4c-169">Highlighting a location in a filled map cross-filters the other visualizations on the report page... and vice versa.</span></span>

1. <span data-ttu-id="8fd4c-170">เมื่อต้องการทำตามขั้นตอน ก่อนบันทึกรายงานนี้ โดยการเลือก **ไฟล์ > บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8fd4c-170">To follow along, first save this report by selecting **File > Save**.</span></span> 

2. <span data-ttu-id="8fd4c-171">คัดลอกแผนที่แถบสีโดยใช้ CTRL C</span><span class="sxs-lookup"><span data-stu-id="8fd4c-171">Copy the filled map using CTRL-C.</span></span>

3. <span data-ttu-id="8fd4c-172">จากด้านล่างของพื้นที่รายงาน เลือกแท็บ **ความคิดเห็น** เพื่อเปิดหน้ารายงานความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="8fd4c-172">From the bottom of the report canvas, select the **Sentiment** tab to open the Sentiment report page.</span></span>

    ![เลือกแท็บความคิดเห็นแล้ว](media/power-bi-visualization-filled-maps-choropleths/power-bi-sentiment-tab.png)

4. <span data-ttu-id="8fd4c-174">ย้ายและปรับขนาดการแสดงภาพบนหน้าเพื่อสร้างพื้นที่ว่าง แล้วกด CTRL V เพื่อวางแผนที่แถบสีจากรายงานก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="8fd4c-174">Move and resize the visualizations on the page to make some room, then CTRL-V paste the filled map from the previous report.</span></span> <span data-ttu-id="8fd4c-175">(ดูรูปภาพดังต่อไปนี้)</span><span class="sxs-lookup"><span data-stu-id="8fd4c-175">(See the following images)</span></span>

   ![แผนที่แถบสีที่เพิ่มไปยังหน้าความคิดเห็น](media/power-bi-visualization-filled-maps-choropleths/power-bi-map.png)

5. <span data-ttu-id="8fd4c-177">บนแผนที่แถบสี เลือกหนึ่งรัฐ</span><span class="sxs-lookup"><span data-stu-id="8fd4c-177">On the filled map, select a state.</span></span>  <span data-ttu-id="8fd4c-178">ซึ่งจะไฮไลต์เชื่อมโยงและตัวกรองเชื่อมโยงไปยังการแสดงภาพอื่น ๆ บนหน้า</span><span class="sxs-lookup"><span data-stu-id="8fd4c-178">This cross-highlights and cross-filters the other visualizations on the page.</span></span> <span data-ttu-id="8fd4c-179">การเลือก **Texas** ตัวอย่างเช่น กรองข้ามการ์ดและไฮไลท์แผนภูมิแท่ง</span><span class="sxs-lookup"><span data-stu-id="8fd4c-179">Selecting **Texas**, for example, cross-filters the cards and cross-highlights the bar chart.</span></span> <span data-ttu-id="8fd4c-180">จากนี้ฉันรู้ว่า ความคิดเห็นเป็น 75 และ Texas อยู่ในเขตกลาง #23</span><span class="sxs-lookup"><span data-stu-id="8fd4c-180">From this, I know that Sentiment is 75 and that Texas is in the Central District #23.</span></span>   
   <span data-ttu-id="8fd4c-181">![เท็กซัสถูกเลือกแล้ว](media/power-bi-visualization-filled-maps-choropleths/power-bi-filter.png)</span><span class="sxs-lookup"><span data-stu-id="8fd4c-181">![Texas selected](media/power-bi-visualization-filled-maps-choropleths/power-bi-filter.png)</span></span>
2. <span data-ttu-id="8fd4c-182">เลือกจุดข้อมูลบน VanArsdel ความคิดเห็นตามเดือนแผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="8fd4c-182">Select a data point on the VanArsdel - Sentiment by Month line chart.</span></span> <span data-ttu-id="8fd4c-183">การทำเช่นนี้จะกรองแผนที่แถบสีเพื่อให้แสดงความคิดเห็นสำหรับ VanArsdel และไม่ใช่สำหรับการแข่งขันของ VanArsdel</span><span class="sxs-lookup"><span data-stu-id="8fd4c-183">This filters the filled map to show Sentiment data for VanArsdel and not their competition.</span></span>  
   ![แรเงาใหม่](media/power-bi-visualization-filled-maps-choropleths/power-bi-vanarsdel.png)

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="8fd4c-185">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="8fd4c-185">Considerations and troubleshooting</span></span>
<span data-ttu-id="8fd4c-186">ข้อมูลในแผนที่อาจไม่ชัดเจน</span><span class="sxs-lookup"><span data-stu-id="8fd4c-186">Map data can be ambiguous.</span></span>  <span data-ttu-id="8fd4c-187">ตัวอย่างเช่น มีปารีส ประเทศฝรั่งเศส และยังมีปารีส ในรัฐเท็กซัสด้วย</span><span class="sxs-lookup"><span data-stu-id="8fd4c-187">For example, there's a Paris, France, but there's also a Paris, Texas.</span></span> <span data-ttu-id="8fd4c-188">ข้อมูลทางภูมิศาสตร์ของคุณถูกเก็บไว้ในคอลัมน์แยกต่างหาก ไม่ว่าจะเป็น คอลัมน์สำหรับชื่อเมือง คอลัมน์สำหรับชื่อรัฐหรือจังหวัด และอื่น ๆ ดังนั้น Bing อาจไม่สามารถบอกได้ว่าเป็นปารีสที่ไหน</span><span class="sxs-lookup"><span data-stu-id="8fd4c-188">Your geographic data is probably stored in separate columns – a column for city names, a column for state or province names, etc. – so Bing may not be able to tell which Paris is which.</span></span> <span data-ttu-id="8fd4c-189">ถ้าชุดข้อมูลของคุณประกอบด้วยข้อมูลละติจูดและลองจิจูดอยู่แล้ว Power BI มีเขตข้อมูลพิเศษเพื่อช่วยทำให้ข้อมูลแผนที่ชัดเจนยิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="8fd4c-189">If your dataset already contains latitude and longitude data, Power BI has special fields to help make the map data unambiguous.</span></span> <span data-ttu-id="8fd4c-190">เพียงแค่ลากเขตข้อมูลที่ประกอบด้วยข้อมูลละติจูดของคุณลงในพื้นที่\>การแสดงภาพ > ละติจูด</span><span class="sxs-lookup"><span data-stu-id="8fd4c-190">Just drag the field that contains your latitude data into the Visualizations \> Latitude area.</span></span>  <span data-ttu-id="8fd4c-191">และทำเช่นเดียวกันสำหรับข้อมูลลองจิจูดของคุณ</span><span class="sxs-lookup"><span data-stu-id="8fd4c-191">And do the same for your longitude data.</span></span>    

![บานหน้าต่างการแสดงภาพและเขตข้อมูล](media/power-bi-visualization-filled-maps-choropleths/pbi-latitude.png)

<span data-ttu-id="8fd4c-193">ถ้าคุณมีสิทธิ์แก้ไขชุดข้อมูลใน Power BI Desktop ดูวิดีโอนี้สำหรับความช่วยเหลือในการแก้ไขแผนที่ที่ไม่ชัดเจน</span><span class="sxs-lookup"><span data-stu-id="8fd4c-193">If you have permissions to edit the dataset in Power BI Desktop, watch this video for help with addressing map ambiguity.</span></span>


<span data-ttu-id="8fd4c-194">ถ้าคุณไม่สามารถเข้าถึงข้อมูลละติจูดและลองจิจูดได้ แต่คุณสามารถเข้าถึงการแก้ไขในชุดข้อมูล [ทำตามคำแนะนำเหล่านี้เพื่ออัปเดตชุดข้อมูลของคุณ](https://support.office.com/article/Maps-in-Power-View-8A9B2AF3-A055-4131-A327-85CC835271F7)</span><span class="sxs-lookup"><span data-stu-id="8fd4c-194">If you do not have access to latitude and longitude data, but you do have edit access to the dataset, [follow these instructions to update your dataset](https://support.office.com/article/Maps-in-Power-View-8A9B2AF3-A055-4131-A327-85CC835271F7).</span></span>

<span data-ttu-id="8fd4c-195">สำหรับความช่วยเหลือเพิ่มเติมเกี่ยวกับการแสดงภาพของแผนที่ ดู[เคล็ดลับและคำแนะนำสำหรับการแสดงภาพของแผนที่](./power-bi-map-tips-and-tricks.md)</span><span class="sxs-lookup"><span data-stu-id="8fd4c-195">For more help with Map visualizations, see [Tips and tricks for map visualizations](./power-bi-map-tips-and-tricks.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="8fd4c-196">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="8fd4c-196">Next steps</span></span>

[<span data-ttu-id="8fd4c-197">แผนที่รูปร่าง</span><span class="sxs-lookup"><span data-stu-id="8fd4c-197">Shape map</span></span>](desktop-shape-map.md)

[<span data-ttu-id="8fd4c-198">ชนิดการแสดงภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8fd4c-198">Visualization types in Power BI</span></span>](power-bi-visualization-types-for-reports-and-q-and-a.md)