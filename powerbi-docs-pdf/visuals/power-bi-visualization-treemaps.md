---
title: แผนที่ต้นไม้ใน Power BI
description: แผนที่ต้นไม้ใน Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 05/05/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 11dbfceaf38cef74b4ea2190f805353a7723b0d8
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96387424"
---
# <a name="treemaps-in-power-bi"></a><span data-ttu-id="bf897-103">แผนที่ต้นไม้ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="bf897-103">Treemaps in Power BI</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="bf897-104">ทรีแมปจะแสดงข้อมูลแบบลำดับชั้นเป็นชุดของสี่เหลี่ยมผืนผ้าที่วางเรียงต่อๆ กัน</span><span class="sxs-lookup"><span data-stu-id="bf897-104">Treemaps display hierarchical data as a set of nested rectangles.</span></span> <span data-ttu-id="bf897-105">แต่ละระดับของลำดับชั้นจะแสดงเป็นสี่เหลี่ยมสีต่างๆ (กิ่ง) ซึ่งประกอบด้วยสี่เหลี่ยมเล็กๆ ("ใบ")</span><span class="sxs-lookup"><span data-stu-id="bf897-105">Each level of the hierarchy is represented by a colored rectangle (branch) containing smaller rectangles (leaves).</span></span> <span data-ttu-id="bf897-106">Power BI จะกำหนดขนาดพื้นที่ด้านในรูปสี่เหลี่ยมแต่ละรูปตามค่าที่วัดไว้</span><span class="sxs-lookup"><span data-stu-id="bf897-106">Power BI bases the size of the space inside each rectangle on the measured value.</span></span> <span data-ttu-id="bf897-107">สี่เหลี่ยมเรียงตัวกันตามขนาดจากซ้ายบน (ใหญ่ที่สุด) ไปจนถึงขวาล่าง (เล็กสุด)</span><span class="sxs-lookup"><span data-stu-id="bf897-107">The rectangles are arranged in size from top left (largest) to bottom right (smallest).</span></span>

![สกรีนช็อตของจำนวนผลิตภัณฑ์ตามประเภท และทรีแมปผู้ผลิต](media/power-bi-visualization-treemaps/pbi-nancy-viz-treemap.png)

<span data-ttu-id="bf897-109">เช่น หากคุณกำลังวิเคราะห์ยอดขายของคุณ คุณอาจใช้กิ่งระดับสูงๆ สำหรับประเภทเสื้อผ้า: **เขตเมือง** **ชนบท** **เยาวชน** และ **รวมกัน**</span><span class="sxs-lookup"><span data-stu-id="bf897-109">For example, if you're analyzing your sales, you might have top-level branches for the clothing categories: **Urban**, **Rural**, **Youth**, and **Mix**.</span></span> <span data-ttu-id="bf897-110">Power BI จะแบ่งสี่เหลี่ยมบ่งบอกประเภทของคุณออกเป็นใบไม้หลายๆ ใบ สำหรับผู้ผลิตเสื้อผ้าในประเภทนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="bf897-110">Power BI would split your category rectangles into leaves, for the clothing manufacturers within that category.</span></span> <span data-ttu-id="bf897-111">ใบไม้เหล่านี้จะปรับขนาดและและขนาดตามจำนวนสินค้าที่ขายได้</span><span class="sxs-lookup"><span data-stu-id="bf897-111">These leaves would be sized and shaded based on the number sold.</span></span>

<span data-ttu-id="bf897-112">ในกิ่ง **เขตเมือง** ด้านบน เสื้อผ้า **VanArsdel** ขายได้เป็นจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="bf897-112">In the **Urban** branch above, lots of **VanArsdel** clothing was sold.</span></span> <span data-ttu-id="bf897-113">**Natura** และ **Fama** ขายได้จำนวนน้อยกว่า</span><span class="sxs-lookup"><span data-stu-id="bf897-113">Less **Natura** and **Fama** was sold.</span></span> <span data-ttu-id="bf897-114">**Leo** ขายได้จำนวนเล็กน้อยเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="bf897-114">Only a few **Leo** were sold.</span></span> <span data-ttu-id="bf897-115">ดังนั้น กิ่ง **เขตเมือง** ในทรีแมปของคุณจึงมี:</span><span class="sxs-lookup"><span data-stu-id="bf897-115">So, the **Urban** branch of your Treemap has:</span></span>

* <span data-ttu-id="bf897-116">สี่เหลี่ยมอันใหญ่ที่สุดหมายถึง **VanArsdel** ในมุมซ้ายบน</span><span class="sxs-lookup"><span data-stu-id="bf897-116">The largest rectangle for **VanArsdel** in the top-left corner.</span></span>

* <span data-ttu-id="bf897-117">สี่เหลี่ยมอันเล็กกว่าเล็กน้อยหมายถึง  **Natura** และ **Fama**</span><span class="sxs-lookup"><span data-stu-id="bf897-117">Slightly smaller rectangles for **Natura** and **Fama**.</span></span>

* <span data-ttu-id="bf897-118">สี่เหลี่ยมอันอื่นๆ แทนเสื้อผ้าแบรนด์อื่นๆ ที่ขายได้</span><span class="sxs-lookup"><span data-stu-id="bf897-118">Lots of other rectangles for all the other clothing sold.</span></span>

* <span data-ttu-id="bf897-119">สี่เหลี่ยมขนาดเล็กแทน  **Leo**</span><span class="sxs-lookup"><span data-stu-id="bf897-119">A tiny rectangle for **Leo**.</span></span>

<span data-ttu-id="bf897-120">คุณสามารถนำจำนวนสินค้าที่ขายไปเปรียบเทียบกับเสื้อผ้าประเภทอื่นๆ ด้วยการเปรียบเทียบขนาดและเฉดสีของโหนดปลายสุด สี่เหลี่ยมที่ใหญ่กว่าและเข้มกว่าหมายถึงค่าที่สูงกว่า</span><span class="sxs-lookup"><span data-stu-id="bf897-120">You could compare the number of items sold across the other clothing categories by comparing the size and shading of each leaf node; larger and darker rectangles mean higher value.</span></span>


## <a name="when-to-use-a-treemap"></a><span data-ttu-id="bf897-121">เราจะใช้ทรีแมปในกรณีใด</span><span class="sxs-lookup"><span data-stu-id="bf897-121">When to use a treemap</span></span>

<span data-ttu-id="bf897-122">ทรีแมปเป็นทางเลือกที่เหมาะสมอย่างยิ่ง ในกรณีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bf897-122">Treemaps are a great choice:</span></span>

* <span data-ttu-id="bf897-123">เมื่อต้องการแสดงข้อมูลแบบลำดับชั้นเป็นจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="bf897-123">To display large amounts of hierarchical data.</span></span>

* <span data-ttu-id="bf897-124">เมื่อไม่สามารถใช้แผนภูมิแท่งในการนำเสนอข้อมูลจำนวนมากได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="bf897-124">When a bar chart can't effectively handle the large number of values.</span></span>

* <span data-ttu-id="bf897-125">เมื่อต้องการแสดงสัดส่วนระหว่างแต่ละองค์ประกอบกับข้อมูลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="bf897-125">To show the proportions between each part and the whole.</span></span>

* <span data-ttu-id="bf897-126">เมื่อต้องการแสดงรูปแบบของการแจกแจงข้อมูลของข้อมูลตัวเลขในแต่ละระดับของประเภทในลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="bf897-126">To show the pattern of the distribution of the measure across each level of categories in the hierarchy.</span></span>

* <span data-ttu-id="bf897-127">เมื่อต้องการแสดงแอตทริบิวต์ที่ใช้การแสดงรหัสด้วยสีและขนาด</span><span class="sxs-lookup"><span data-stu-id="bf897-127">To show attributes using size and color coding.</span></span>

* <span data-ttu-id="bf897-128">เมื่อต้องการกำหนดรูปแบบ ค่าผิดปกติ ปัจจัยสนับสนุนที่สำคัญอย่างยิ่งและและข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="bf897-128">To spot patterns, outliers, most-important contributors, and exceptions.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="bf897-129">เงื่อนไขเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="bf897-129">Prerequisite</span></span>

<span data-ttu-id="bf897-130">บทช่วยสอนนี้ใช้[ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix)</span><span class="sxs-lookup"><span data-stu-id="bf897-130">This tutorial uses the [Retail Analysis sample PBIX file](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix).</span></span>

1. <span data-ttu-id="bf897-131">จากด้านบนซ้ายของแถบเมนู เลือก **ไฟล์** > **เปิด**</span><span class="sxs-lookup"><span data-stu-id="bf897-131">From the upper left section of the menubar, select **File** > **Open**</span></span>
   
2. <span data-ttu-id="bf897-132">ค้นหาสำเนา **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก**</span><span class="sxs-lookup"><span data-stu-id="bf897-132">Find your copy of the **Retail Analysis sample PBIX file**</span></span>

1. <span data-ttu-id="bf897-133">เปิด **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก** ในมุมมองรายงาน ![ภาพหน้าจอไอคอนมุมมองรายงาน](media/power-bi-visualization-kpi/power-bi-report-view.png)</span><span class="sxs-lookup"><span data-stu-id="bf897-133">Open the **Retail Analysis sample PBIX file** in report view ![Screenshot of the report view icon.](media/power-bi-visualization-kpi/power-bi-report-view.png).</span></span>

1. <span data-ttu-id="bf897-134">เลือก</span><span class="sxs-lookup"><span data-stu-id="bf897-134">Select</span></span> ![สกรีนช็อตของแท็บสีเหลือง](media/power-bi-visualization-kpi/power-bi-yellow-tab.png) <span data-ttu-id="bf897-136">หากต้องการเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="bf897-136">to add a new page.</span></span>

> [!NOTE]
> <span data-ttu-id="bf897-137">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="bf897-137">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span>    



<span data-ttu-id="bf897-138">หลังจากที่คุณเรียกดูชุดข้อมูล **ตัวอย่างการวิเคราะห์ร้านค้าปลีก** คุณจะสามารถเริ่มใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="bf897-138">After you get the **Retail Analysis Sample** dataset, you can get started.</span></span>

## <a name="create-a-basic-treemap"></a><span data-ttu-id="bf897-139">สร้างทรีแมปแบบพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="bf897-139">Create a basic treemap</span></span>

<span data-ttu-id="bf897-140">คุณจะสร้างรายงาน และเพิ่มทรีแมปแบบพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="bf897-140">You'll create a report and add a basic treemap.</span></span>


1. <span data-ttu-id="bf897-141">ในบานหน้าต่าง **เขตข้อมูล** ให้เลือกมาตรวัด **ยอดขาย** > **ยอดขายของปีที่ผ่านมา**</span><span class="sxs-lookup"><span data-stu-id="bf897-141">From the **Fields** pane, select the **Sales** > **Last Year Sales** measure.</span></span>

   ![สกรีนช็อตของยอดขาย > ยอดขายของปีที่ผ่านมาที่เลือกไว้ และภาพที่แสดง](media/power-bi-visualization-treemaps/treemapfirstvalue-new.png)

1. <span data-ttu-id="bf897-143">เลือกไอคอนทรีแมป</span><span class="sxs-lookup"><span data-stu-id="bf897-143">Select the treemap icon</span></span> ![สกรีนช็อตของไอคอนทรีแมป](media/power-bi-visualization-treemaps/power-bi-treemap-icon.png) <span data-ttu-id="bf897-145">การแปลงแผนภูมิเป็นทรีแมป</span><span class="sxs-lookup"><span data-stu-id="bf897-145">to convert the chart to a treemap.</span></span>

   ![สกรีนช็อตของทรีแมปที่ไม่มีการกำหนดค่า](media/power-bi-visualization-treemaps/treemapconvertto-new.png)

1. <span data-ttu-id="bf897-147">เลือก **รายการ** > **หมวดหมู่** ที่จะเพิ่ม **หมวหมู่** ไปยัง **กลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="bf897-147">Select **Item** > **Category** which will add **Category** to the **Group** well.</span></span>

    <span data-ttu-id="bf897-148">Power BI จะสร้างแผนที่ต้นไม้ โดยที่ขนาดของสี่เหลี่ยมผืนผ้าจะแสดงถึงยอดขายรวม และสีจะแสดงถึงประเภท</span><span class="sxs-lookup"><span data-stu-id="bf897-148">Power BI creates a treemap where the size of the rectangles is based on total sales and the color represents the category.</span></span> <span data-ttu-id="bf897-149">แท้จริงแล้ว คุณได้สร้างลำดับชั้นที่อธิบายขนาดสัมพัทธ์ของยอดขายรวมจำแนกตามประเภทได้อย่างชัดเจน</span><span class="sxs-lookup"><span data-stu-id="bf897-149">In essence you've created a hierarchy that visually describes the relative size of total sales by category.</span></span> <span data-ttu-id="bf897-150">ประเภท **ผู้ชาย** มียอดขายสูงสุด และ **ถุงเท้าและชุดชั้นใน** มียอดขายต่ำที่สุด</span><span class="sxs-lookup"><span data-stu-id="bf897-150">The **Men's** category has the highest sales and the **Hosiery** category has the lowest.</span></span>

    ![สกรีนช็อตของทรีแมปที่มีการกำหนดค่า](media/power-bi-visualization-treemaps/power-bi-complete.png)

1. <span data-ttu-id="bf897-152">เลือก **ร้านค้า** > **เครือข่าย** เพื่อเพิ่ม **เครือข่าย** ไปยัง **รายละเอียด** เพื่อเติมแผนผังทรีของคุณ</span><span class="sxs-lookup"><span data-stu-id="bf897-152">Select **Store** > **Chain** which will add **Chain** to the **Details** well to complete your treemap.</span></span> <span data-ttu-id="bf897-153">ตอนนี้คุณก็สามารถเปรียบเทียบยอดขายของปีล่าสุดจำแนกตามประเภทกับร้านค้าเครือข่ายสาขาได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="bf897-153">You can now compare last year's sales by category and chain.</span></span>

   ![สกรีนช็อตของทรีแมปที่มีร้านค้า > เครือร้านค้าที่เพิ่มไปยังรายละเอียด](media/power-bi-visualization-treemaps/power-bi-details.png)

   > [!NOTE]
   > <span data-ttu-id="bf897-155">ไม่สามารถใช้ความเข้มของสีและรายละเอียดในเวลาเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="bf897-155">Color Saturation and Details cannot be used at the same time.</span></span>

1. <span data-ttu-id="bf897-156">โฮเวอร์เหนือพื้นที่ **ร้านเครือข่ายสาขา** เพื่อดูคำแนะนำเครื่องมือสำหรับส่วนนั้นๆ ของ **ประเภท**</span><span class="sxs-lookup"><span data-stu-id="bf897-156">Hover over a **Chain** area to reveal the tooltip for that portion of the **Category**.</span></span>

    <span data-ttu-id="bf897-157">ตัวอย่าง เหนือ **Fashions Direct** ใน **090 Home** สี่เหลี่ยมผืนผ้าแสดงคำแนะนำสำหรับสัดส่วนของ Fashions Direct ของประเภทของบ้าน</span><span class="sxs-lookup"><span data-stu-id="bf897-157">For example, hovering over **Fashions Direct** in the **090-Home** rectangle reveals the tooltip for Fashion Direct's portion of the Home category.</span></span>

   ![สกรีนช็อตของคำแนะนำแรกที่ปรากฏขึ้น](media/power-bi-visualization-treemaps/treemaphoverdetail-new.png)


## <a name="highlighting-and-cross-filtering"></a><span data-ttu-id="bf897-159">การทำไฮไลท์และการกรองข้าม</span><span class="sxs-lookup"><span data-stu-id="bf897-159">Highlighting and cross-filtering</span></span>

<span data-ttu-id="bf897-160">แรเงาเลือก **หมวดหมู่** หรือ **รายละเอียด** จากแผนผังทรี แรเงาและกรองโยงสว่นการแสดงผลอื่น ๆ ในหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="bf897-160">Highlighting a **Category** or **Detail** in a treemap cross-highlights and cross-filters the other visualizations on the report page.</span></span> <span data-ttu-id="bf897-161">เมื่อต้องการทำตามขั้นตอน เพิ่มภาพบางภาพไปยังหน้ารายงานนี้ หรือคัดลอกทรีแมปไปยังหน้าอื่นๆ ในรายงานนี้</span><span class="sxs-lookup"><span data-stu-id="bf897-161">To follow along, either add some visuals to this report page or copy the treemap to one of the other pages in this report.</span></span> <span data-ttu-id="bf897-162">ภาพแผนผังทรีด้านล่างถูกคัดลอกไปที่หน้า **ภาพรวม**</span><span class="sxs-lookup"><span data-stu-id="bf897-162">The below image the treemap was copied over to the **Overview** page.</span></span> 

1. <span data-ttu-id="bf897-163">ในทรีแมป ให้เลือก **ประเภท** หรือ **ร้านในเครือ** ภายใน **ประเภท**</span><span class="sxs-lookup"><span data-stu-id="bf897-163">On the treemap, select either a **Category** or a **Chain** within a **Category**.</span></span> <span data-ttu-id="bf897-164">ซึ่งจะไฮไลต์ข้ามการแสดงภาพอื่นๆ บนหน้า</span><span class="sxs-lookup"><span data-stu-id="bf897-164">That will cross-highlight the other visualizations on the page.</span></span> <span data-ttu-id="bf897-165">ตัวอย่างเช่น การเลือก **050-Shoes** จะแสดงให้เห็นว่ายอดขายของรองเท้าของปีที่แล้วมีมูลค่า **16,352,432 ดอลลาร์** โดยที่ **การขายตรงสินค้าแฟชั่น** คิดเป็นมูลค่า **2,174,185 ดอลลาร์** ของยอดขายเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="bf897-165">Selecting **050-Shoes**, for example, shows you that last year's sales for shoes was **$16,352,432** with **Fashions Direct** accounting for **$2,174,185** of those sales.</span></span>

   ![สกรีนช็อตของรายงานภาพรวมยอดขายร้านค้ากำลังแสดงการไฮไลต์ข้าม](media/power-bi-visualization-treemaps/treemaphiliting.png)

1. <span data-ttu-id="bf897-167">ในแผนภูมิวงกลม **ยอดขายปีล่าสุดในร้านค้าเครือข่ายสาขา** เมื่อเลือกชิ้นวงกลม **การขายตรงสินค้าแฟชั่น** จะกรองข้ามทรีแมป</span><span class="sxs-lookup"><span data-stu-id="bf897-167">In the **Last Year Sales by Chain** pie chart, selecting the **Fashions Direct** slice, cross-filters the treemap.</span></span>
   <span data-ttu-id="bf897-168">![การสาธิต GIF ของคุณลักษณะการกรองข้าม](media/power-bi-visualization-treemaps/treemapnoowl.gif)</span><span class="sxs-lookup"><span data-stu-id="bf897-168">![GIF demonstration of the cross-filtering feature.](media/power-bi-visualization-treemaps/treemapnoowl.gif)</span></span>

1. <span data-ttu-id="bf897-169">เมื่อต้องการจัดการวิธีการที่แผนภูมิไฮไลต์ข้ามและกรองข้ามระหว่างกัน โปรดดู [การเปลี่ยนแปลงวิธีการโต้ตอบของการแสดงภาพในรายงาน Power BI](../create-reports/service-reports-visual-interactions.md)</span><span class="sxs-lookup"><span data-stu-id="bf897-169">To manage how charts cross-highlight and cross-filter each other, see [Change how visuals interact in a Power BI report](../create-reports/service-reports-visual-interactions.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="bf897-170">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="bf897-170">Next steps</span></span>

* [<span data-ttu-id="bf897-171">แผนภูมิแบบน้ำตกใน Power BI</span><span class="sxs-lookup"><span data-stu-id="bf897-171">Waterfall charts in Power BI</span></span>](power-bi-visualization-waterfall-charts.md)

* [<span data-ttu-id="bf897-172">ชนิดการแสดงภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="bf897-172">Visualization types in Power BI</span></span>](power-bi-visualization-types-for-reports-and-q-and-a.md)

