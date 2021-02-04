---
title: การแสดงภาพตารางในรายงานและแดชบอร์ด Power BI
description: บทช่วยสอนสำหรับการทำงานกับการแสดงภาพตารางในรายงานและแดชบอร์ด Power BI รวมถึงวิธีการปรับขนาดความกว้างของคอลัมน์
author: mihart
ms.author: mihart
ms.reviewer: willt
featuredvideoid: ''
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 02/10/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: aa99cd4efed9239d6685d53f2515d16549a0ae72
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418819"
---
# <a name="tables-in-power-bi-reports-and-dashboards"></a><span data-ttu-id="81bb1-103">การทำงานกับตารางในรายงานและแดชบอร์ด Power BI</span><span class="sxs-lookup"><span data-stu-id="81bb1-103">Tables in Power BI reports and dashboards</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]


[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="81bb1-104">ตารางคือ เส้นตารางที่ประกอบด้วยข้อมูลที่เกี่ยวข้องในชุดที่สมเหตุผลของแถวและคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="81bb1-104">A table is a grid that contains related data in a logical series of rows and columns.</span></span> <span data-ttu-id="81bb1-105">ซึ่งอาจยังประกอบด้วยส่วนหัวและแถวสำหรับผลรวมด้วย</span><span class="sxs-lookup"><span data-stu-id="81bb1-105">It may also contain headers and a row for totals.</span></span> <span data-ttu-id="81bb1-106">ตารางทำงานได้ดีกับข้อเปรียบเทียบเชิงปริมาณซึ่งเป็นการที่คุณดูหลายค่าสำหรับหนึ่งประเภท</span><span class="sxs-lookup"><span data-stu-id="81bb1-106">Tables work well with quantitative comparisons where you're looking at many values for a single category.</span></span> <span data-ttu-id="81bb1-107">ตัวอย่างเช่น ตารางนี้แสดงการวัดที่แตกต่างกันห้าการวัดสำหรับ **ประเภท**</span><span class="sxs-lookup"><span data-stu-id="81bb1-107">For example, this table displays five different measures for **Category**.</span></span>

![สกรีนช็อตของตารางที่แสดงการวัดที่แตกต่างกันห้าการวัดสำหรับประเภท](media/power-bi-visualization-tables/power-bi-table-grid3.png)

<span data-ttu-id="81bb1-109">สร้างตารางในรายงานและองค์ประกอบการไฮไลต์เชื่อมโยงภายในตารางด้วยวิชวลอื่น ในหน้ารายงานหน้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="81bb1-109">Create tables in reports and cross-highlight elements within the table with other visuals on the same report page.</span></span> <span data-ttu-id="81bb1-110">คุณสามารถเลือกแถว คอลัมน์ และแม้แต่ละเซลล์ และทำไฮไลต์เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="81bb1-110">You can select rows, columns, and even individual cells and cross-highlight.</span></span> <span data-ttu-id="81bb1-111">สามารถคัดลอกและวางเซลล์เดียวและหลายเซลล์ลงในแอปพลิเคชันอื่นได้</span><span class="sxs-lookup"><span data-stu-id="81bb1-111">You can also copy and paste individual cells and multiple cell selections into other applications.</span></span>

## <a name="when-to-use-a-table"></a><span data-ttu-id="81bb1-112">เมื่อต้องการใช้ตาราง</span><span class="sxs-lookup"><span data-stu-id="81bb1-112">When to use a table</span></span>

<span data-ttu-id="81bb1-113">ตารางเป็นตัวเลือกที่ดีมาก:</span><span class="sxs-lookup"><span data-stu-id="81bb1-113">Tables are a great choice:</span></span>

* <span data-ttu-id="81bb1-114">เมื่อต้องการดูและเปรียบเทียบข้อมูลโดยละเอียดและค่าที่แน่นอน (แทนการนำเสนอแบบเป็นภาพ)</span><span class="sxs-lookup"><span data-stu-id="81bb1-114">To see and compare detailed data and exact values (instead of visual representations).</span></span>

* <span data-ttu-id="81bb1-115">เพื่อแสดงข้อมูลในรูปแบบตาราง</span><span class="sxs-lookup"><span data-stu-id="81bb1-115">To display data in a tabular format.</span></span>

* <span data-ttu-id="81bb1-116">เพื่อแสดงข้อมูลตัวเลขตามประเภท</span><span class="sxs-lookup"><span data-stu-id="81bb1-116">To display numerical data by categories.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="81bb1-117">เงื่อนไขเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="81bb1-117">Prerequisite</span></span>

<span data-ttu-id="81bb1-118">บทช่วยสอนนี้ใช้[ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix)</span><span class="sxs-lookup"><span data-stu-id="81bb1-118">This tutorial uses the [Retail Analysis sample PBIX file](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix).</span></span>

1. <span data-ttu-id="81bb1-119">จากด้านบนซ้ายของแถบเมนู เลือก **ไฟล์** > **เปิด**</span><span class="sxs-lookup"><span data-stu-id="81bb1-119">From the upper left section of the menubar, select **File** > **Open**</span></span>
   
2. <span data-ttu-id="81bb1-120">ค้นหาสำเนา **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก**</span><span class="sxs-lookup"><span data-stu-id="81bb1-120">Find your copy of the **Retail Analysis sample PBIX file**</span></span>

1. <span data-ttu-id="81bb1-121">เปิด **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก** ในมุมมองรายงาน ![ภาพหน้าจอไอคอนมุมมองรายงาน](media/power-bi-visualization-kpi/power-bi-report-view.png)</span><span class="sxs-lookup"><span data-stu-id="81bb1-121">Open the **Retail Analysis sample PBIX file** in report view ![Screenshot of the report view icon.](media/power-bi-visualization-kpi/power-bi-report-view.png).</span></span>

1. <span data-ttu-id="81bb1-122">เลือก</span><span class="sxs-lookup"><span data-stu-id="81bb1-122">Select</span></span> ![สกรีนช็อตของแท็บสีเหลือง](media/power-bi-visualization-kpi/power-bi-yellow-tab.png) <span data-ttu-id="81bb1-124">หากต้องการเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="81bb1-124">to add a new page.</span></span>

> [!NOTE]
> <span data-ttu-id="81bb1-125">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="81bb1-125">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span>

## <a name="create-a-table"></a><span data-ttu-id="81bb1-126">สร้างตาราง</span><span class="sxs-lookup"><span data-stu-id="81bb1-126">Create a table</span></span>

<span data-ttu-id="81bb1-127">คุณจะสร้างตารางที่มีภาพแสดงอยู่บริเวณส่วนแรกของบทความเพื่อแสดงมูลค่ายอดขายตามประเภทรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="81bb1-127">You'll create the table pictured at the beginning of the article to display sales values by item category.</span></span>


1. <span data-ttu-id="81bb1-128">ในบานหน้าต่างของ **เขตข้อมูล** ให้เลือก **ประเภท** > **รายการสินค้า**</span><span class="sxs-lookup"><span data-stu-id="81bb1-128">From the **Fields** pane, select **Item** > **Category**.</span></span>

    <span data-ttu-id="81bb1-129">Power BI จะสร้างตารางที่แสดงรายการทุกประเภทโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="81bb1-129">Power BI automatically creates a table that lists all the categories.</span></span>

    ![ผลลัพธ์ของการเพิ่มประเภท](media/power-bi-visualization-tables/power-bi-table1.png)

1. <span data-ttu-id="81bb1-131">เลือก **ยอดขาย > ราคาต่อหน่วยเฉลี่ย** และ **ยอดขาย > ยอดขายปีที่ผ่านมา**</span><span class="sxs-lookup"><span data-stu-id="81bb1-131">Select **Sales > Average Unit Price** and **Sales > Last Year Sales**</span></span>

1. <span data-ttu-id="81bb1-132">จากนั้นเลือก **ยอดขาย > ยอดขายของปีนี้** และเลือกตัวเลือกทั้งสาม: **ค่า**, **เป้าหมาย** และ **สถานะ**</span><span class="sxs-lookup"><span data-stu-id="81bb1-132">Then select **Sales > This Year Sales** and select all three options: **Value**, **Goal**, and **Status**.</span></span>

1. <span data-ttu-id="81bb1-133">ในบานหน้าต่าง **การแสดงผลด้วยภาพ** ค้นหาแอ่ง **ค่า** แล้วเลือกค่าจนกว่าลำดับของคอลัมน์แผนภูมิของคุณตรงกับรูปภาพแรกในหน้านี้</span><span class="sxs-lookup"><span data-stu-id="81bb1-133">In the **Visualizations** pane, locate the **Values** well and select the values until the order of your chart columns matches the first image on this page.</span></span> <span data-ttu-id="81bb1-134">ลากค่าดังกล่าวไปยังอ่างดังกล่าวตามความเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="81bb1-134">Drag the values in the well if needed.</span></span> <span data-ttu-id="81bb1-135">**ค่า** ของคุณด้วยจะมีลักษณะดังนี้</span><span class="sxs-lookup"><span data-stu-id="81bb1-135">Your **Values** well will look like this:</span></span>

    ![ค่าที่ดี](media/power-bi-visualization-tables/power-bi-table2.png)


## <a name="format-the-table"></a><span data-ttu-id="81bb1-137">จัดรูปแบบตาราง</span><span class="sxs-lookup"><span data-stu-id="81bb1-137">Format the table</span></span>

<span data-ttu-id="81bb1-138">มีหลายวิธีในการจัดรูปแบบตาราง</span><span class="sxs-lookup"><span data-stu-id="81bb1-138">There are many ways to format a table.</span></span> <span data-ttu-id="81bb1-139">มีเพียงไม่กี่ส่วนที่ครอบคลุมในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="81bb1-139">Only a few are covered here.</span></span> <span data-ttu-id="81bb1-140">วิธีที่ยอดเยี่ยมในการเรียนรู้เกี่ยวกับตัวเลือกอื่น ๆ ในการจัดรูปแบบคือการเปิด **บานหน้าต่าง** การจัดรูปแบบ (ไอคอนลูกกลิ้ง ![paint roller](media/power-bi-visualization-tables/power-bi-format.png)) และสำรวจ</span><span class="sxs-lookup"><span data-stu-id="81bb1-140">A great way to learn about the other formatting options is to open the **Format** pane (paint roller icon ![paint roller](media/power-bi-visualization-tables/power-bi-format.png)) and explore.</span></span>

* <span data-ttu-id="81bb1-141">ลองจัดรูปแบบเส้นตาราง</span><span class="sxs-lookup"><span data-stu-id="81bb1-141">Try formatting the table grid.</span></span> <span data-ttu-id="81bb1-142">ที่นี่เราได้เพิ่มเส้นตารางแนวตั้งสีน้ำเงิน เพิ่มช่องว่างในแถว และเพิ่มเค้าโครง และขนาดข้อความ</span><span class="sxs-lookup"><span data-stu-id="81bb1-142">Here you'll add a blue vertical grid, add space to the rows, and increase the outline and text size.</span></span>

    ![การ์ดเส้นตาราง](media/power-bi-visualization-tables/power-bi-table-gridnew.png)

    ![ตารางแสดงผลลัพธ์](media/power-bi-visualization-tables/power-bi-table-grid3.png)

* <span data-ttu-id="81bb1-145">สำหรับส่วนหัวของคอลัมน์ เปลี่ยนสีพื้นหลัง เพิ่มเค้าโครง และเพิ่มขนาดฟอนต์</span><span class="sxs-lookup"><span data-stu-id="81bb1-145">For the column headers, change the background color, add an outline, and increase the font size.</span></span>

    ![การ์ดหัวข้อคอลัมน์](media/power-bi-visualization-tables/power-bi-table-column-headers.png)

    ![ส่วนหัวในตารางการจัดรูปแบบ](media/power-bi-visualization-tables/power-bi-table-column2.png)

* <span data-ttu-id="81bb1-148">คุณยังสามารถจัดรูปแบบกับ แต่ละคอลัมน์ และส่วนหัวของคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="81bb1-148">You can even apply formatting to individual columns and column headers.</span></span> <span data-ttu-id="81bb1-149">เริ่มต้นด้วยการขยาย **การจัดรูปแบบเขตข้อมูล** และเลือกคอลัมน์เพื่อจัดรูปแบบจากรายการดรอปดาวน์</span><span class="sxs-lookup"><span data-stu-id="81bb1-149">Start by expanding **Field formatting** and selecting the column to format from the drop-down.</span></span> <span data-ttu-id="81bb1-150">ขึ้นอยู่กับค่าของคอลัมน์ **การจัดรูปแบบเขตข้อมูล** ช่วยให้คุณตั้งค่าสิ่งต่างๆ เช่น: หน่วยแสดงผล, สีฟอนต์, จำนวนตำแหน่งทศนิยม, พื้นหลัง, การจัดแนว และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="81bb1-150">Depending on the column values, **Field formatting** lets you set things like: display units, font color, number of decimal places, background, alignment, and more.</span></span> <span data-ttu-id="81bb1-151">เมื่อคุณได้ปรับการตั้งค่าแล้ว ตัดสินใจว่าจะใช้การตั้งค่าเหล่านั้นกับส่วนหัวและแถวผลรวมได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="81bb1-151">Once you've adjusted the settings, decide whether to apply those settings to the header and totals row as well.</span></span>

    ![การจัดรูปแบบเขตข้อมูลสำหรับยอดขายของปีนี้](media/power-bi-visualization-tables/power-bi-field-formatting.png)

    ![การจัดรูปแบบเขตข้อมูลสำหรับยอดขายของปีนี้ในตาราง](media/power-bi-visualization-tables/power-bi-field-formatting-1.png)

* <span data-ttu-id="81bb1-154">หลังการปรับรูปแบบเพิ่มเติมบางส่วน ต่อไปนี้คือตารางขั้นสุดท้ายที่ได้</span><span class="sxs-lookup"><span data-stu-id="81bb1-154">After some additional formatting, here is our final table.</span></span>

    ![ตารางที่มีรูปแบบทั้งหมดไว้](media/power-bi-visualization-tables/power-bi-table-format.png)

### <a name="conditional-formatting"></a><span data-ttu-id="81bb1-156">การจัดรูปแบบแบบมีเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="81bb1-156">Conditional formatting</span></span>

<span data-ttu-id="81bb1-157">*การจัดรูปแบบตามเงื่อนไข* คือการจัดรูปแบบชนิดหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="81bb1-157">*Conditional formatting* is one type of formatting.</span></span> <span data-ttu-id="81bb1-158">Power BI สามารถปรับใช้การจัดรูปแบบตามเงื่อนไขกับเขตข้อมูลใดๆ ที่คุณเพิ่มลงใน **ค่า** ของบานหน้าต่าง **การแสดงผล**</span><span class="sxs-lookup"><span data-stu-id="81bb1-158">Power BI can apply conditional formatting to any of the fields that you added to the **Values** well of the **Visualizations** pane.</span></span>

![หน้าต่างการแสดงผล](media/power-bi-visualization-tables/power-bi-table-values.png)

<span data-ttu-id="81bb1-160">ด้วยการจัดรูปแบบตามเงื่อนไขสำหรับตาราง คุณสามารถระบุไอคอน URL สีพื้นหลังของเซลล์และสีฟอนต์ได้ด้วยตนเองโดยยึดตามค่าของเซลล์ รวมถึงการใช้สีไล่ระดับสี</span><span class="sxs-lookup"><span data-stu-id="81bb1-160">With conditional formatting for tables, you can specify icons, URLs, cell background colors, and font colors based on cell values, including using gradient colors.</span></span>

1. <span data-ttu-id="81bb1-161">ในบานหน้าต่าง **รูปแบบ** เปิดการ์ด **การจัดรูปแบบตามเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="81bb1-161">In the **Format** pane, open the **Conditional formatting** card.</span></span>

    ![การ์ดการจัดรูปแบบตามเงื่อนไข](media/power-bi-visualization-tables/power-bi-conditional.png)

1. <span data-ttu-id="81bb1-163">เลือกเขตข้อมูลที่จะจัดรูปแบบ และเลื่อนแถบเลื่อนสำหรับ **สีพื้นหลัง** เป็น เปิด</span><span class="sxs-lookup"><span data-stu-id="81bb1-163">Select a field to format, and turn the slider for **Background color** to On.</span></span> <span data-ttu-id="81bb1-164">Power BI ปรับใช้การไล่ระดับสีที่ยึดตามค่าในคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="81bb1-164">Power BI applies a gradient based on the values in the column.</span></span> <span data-ttu-id="81bb1-165">เมื่อต้องการเปลี่ยนสีเริ่มต้น ให้เลือก **ตัวควบคุมขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="81bb1-165">To change the default colors, select **Advanced controls**.</span></span>

    <span data-ttu-id="81bb1-166">หากคุณเลือกตัวเลือก **แยกจากกัน** คุณสามารถกำหนดค่า **ศูนย์กลาง** ที่เป็นทางเลือกได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="81bb1-166">If you select the **Diverging** option, you can configure an optional **Center** value as well.</span></span>

    ![หน้าจอระดับสีพื้นหลัง](media/power-bi-visualization-tables/power-bi-conditional-formatting-background2.png)

    <span data-ttu-id="81bb1-168">เราลองใช้การจัดรูปแบบแบบกำหนดเองไปยังค่าของค่าเฉลี่ยราคาต่อหน่วยของเรา</span><span class="sxs-lookup"><span data-stu-id="81bb1-168">Let's apply some custom formatting to our Average Unit Price values.</span></span> <span data-ttu-id="81bb1-169">เลือก **แยกจากกัน** เพิ่มสีเล็กน้อย และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="81bb1-169">Select **Diverging**, add some colors, and select **OK**.</span></span>

    ![ตารางที่แสดงสีที่แยกกัน](media/power-bi-visualization-tables/power-bi-conditional-formatting-data-background.png)
1. <span data-ttu-id="81bb1-171">เพิ่มเขตข้อมูลใหม่ไปยังตารางที่มีทั้งค่าบวกและค่าลบ</span><span class="sxs-lookup"><span data-stu-id="81bb1-171">Add a new field to the table that has both positive and negative values.</span></span> <span data-ttu-id="81bb1-172">เลือก **ยอดขาย > ผลต่างยอดขายรวม**</span><span class="sxs-lookup"><span data-stu-id="81bb1-172">Select **Sales > Total Sales Variance**.</span></span>

    ![แสดงเขตข้อมูลใหม่ที่ด้านขวาสุด](media/power-bi-visualization-tables/power-bi-conditional-formatting2.png)

1. <span data-ttu-id="81bb1-174">เพิ่มการจัดรูปแบบตามเงื่อนไขของแถบข้อมูลโดยการเลื่อนแถบเลื่อน **แถบข้อมูล** เป็น เปิด</span><span class="sxs-lookup"><span data-stu-id="81bb1-174">Add data bar conditional formatting by turning the **Data bars** slider to On.</span></span>  

    ![การ์ดการจัดรูปแบบตามเงื่อนไขกับแถบข้อมูล ตั้งค่าเป็น เปิด](media/power-bi-visualization-tables/power-bi-data-bar-matrix.png)

1. <span data-ttu-id="81bb1-176">หากต้องการปรับแต่งแถบข้อมูล เลือก **ตัวควบคุมขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="81bb1-176">To customize the data bars, select **Advanced controls**.</span></span> <span data-ttu-id="81bb1-177">ในกล่องโต้ตอบที่ปรากฏขึ้น ตั้งค่าสีสำหรับ **แถบค่าบวก** และ **แถบค่าลบ** เลือกตัวเลือก **แสดงแถบเท่านั้น** และทำการเปลี่ยนแปลงอื่นๆ ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="81bb1-177">In the dialog that appears, set colors for **Positive bar** and **Negative bar**, select the **Show bar only** option, and make any other changes you'd like.</span></span>

    ![เครื่องหมายถูกสำหรับการแสดงแถบอย่างเดียว](media/power-bi-visualization-tables/power-bi-data-bar.png)

1. <span data-ttu-id="81bb1-179">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="81bb1-179">Select **OK**.</span></span>

    <span data-ttu-id="81bb1-180">แถบข้อมูลจะแทนค่าตัวเลขในตารางที่ทำให้ง่ายต่อการสแกน</span><span class="sxs-lookup"><span data-stu-id="81bb1-180">Data bars replace the numerical values in the table, making it easier to scan.</span></span>

    ![ตารางเดียวกันแต่มีแถบในคอลัมน์สุดท้าย](media/power-bi-visualization-tables/power-bi-conditional-formatting-data-bars2.png)

1. <span data-ttu-id="81bb1-182">เพิ่มการแสดงภาพลงในตารางของคุณด้วย *ไอคอนแบบมีเงื่อนไข*</span><span class="sxs-lookup"><span data-stu-id="81bb1-182">Add visual cues to your table with *conditional icons*.</span></span>  <span data-ttu-id="81bb1-183">ในการ์ด **การจัดรูปแบบตามเงื่อนไข** เลือก **ยอดขายของปีนี้** จากรายการแบบเลื่อนลง</span><span class="sxs-lookup"><span data-stu-id="81bb1-183">In the **Conditional formatting** card, select **This year sales** from the dropdown.</span></span> <span data-ttu-id="81bb1-184">เลื่อนแถบเลื่อน **ไอคอน** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="81bb1-184">Turn the **Icons** slider to **On**.</span></span>  <span data-ttu-id="81bb1-185">หากต้องการปรับแต่งไอคอนต่างๆ เลือก **ตัวควบคุมขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="81bb1-185">To customize the icons, select **Advanced controls**.</span></span>

    ![เพิ่มตารางที่มีไอคอน](media/power-bi-visualization-tables/power-bi-table-icons.png)


## <a name="copy-values-from-power-bi-tables-for-use-in-other-applications"></a><span data-ttu-id="81bb1-187">คัดลอกค่าจากตาราง Power BI เพื่อนำไปใช้ในแอปพลิเคชันอื่น</span><span class="sxs-lookup"><span data-stu-id="81bb1-187">Copy values from Power BI tables for use in other applications</span></span>

<span data-ttu-id="81bb1-188">ตารางหรือเมทริกซ์ของคุณอาจมีเนื้อหาที่คุณต้องการใช้ในแอปพลิเคชันอื่น เช่น Dynamics CRM, Excel และแม้แต่รายงาน Power BI อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="81bb1-188">Your table or matrix may have content that you'd like to use in other applications, like Dynamics CRM, Excel, and even other Power BI reports.</span></span> <span data-ttu-id="81bb1-189">ใน Power BI เมื่อคุณคลิกขวาในเซล คุณสามารถคัดลอกข้อมูลในเซลเดียวหรือเซลตามที่เลือกไปยังคลิปบอร์ดของคุณ และวางในแอปพลิเคชันอื่น</span><span class="sxs-lookup"><span data-stu-id="81bb1-189">In Power BI, when you right-click inside a cell, you can copy the data in a single cell or a selection of cells onto your clipboard, and paste it into the other applications.</span></span>

<span data-ttu-id="81bb1-190">เมื่อต้องการคัดลอกค่าของเซลล์เดียว:</span><span class="sxs-lookup"><span data-stu-id="81bb1-190">To copy the value of a single cell:</span></span>

1. <span data-ttu-id="81bb1-191">เลือกเซลล์คุณต้องการคัดลอก</span><span class="sxs-lookup"><span data-stu-id="81bb1-191">Select the cell you want to copy.</span></span>

1. <span data-ttu-id="81bb1-192">คลิกขวาภายในเซลล์</span><span class="sxs-lookup"><span data-stu-id="81bb1-192">Right-click inside the cell.</span></span>

1. <span data-ttu-id="81bb1-193">เลือก **คัดลอก** > **คัดลอกค่า**</span><span class="sxs-lookup"><span data-stu-id="81bb1-193">Select **Copy** > **Copy value**.</span></span>

    ![สกรีนช็อตแสดงสำเนาที่เลือกโดยเลือกตัวเลือกค่าคัดลอก](media/power-bi-visualization-tables/power-bi-copy-value.png)

    <span data-ttu-id="81bb1-195">คุณสามารถวางค่าที่คัดลอกลงในแอปพลิเคชันอื่นได้ โดยจะได้ค่าเซลล์ที่ไม่ได้จัดรูปแบบในคลิปบอร์ด</span><span class="sxs-lookup"><span data-stu-id="81bb1-195">With the unformatted cell value on your clipboard, you can paste it into another application.</span></span>

<span data-ttu-id="81bb1-196">เมื่อต้องการคัดลอกมากกว่าเซลล์เดียว:</span><span class="sxs-lookup"><span data-stu-id="81bb1-196">To copy more than a single cell:</span></span>

1. <span data-ttu-id="81bb1-197">เลือกช่วงเซลล์ หรือใช้ปุ่ม **CTRL** เพื่อเลือกเซลล์อย่างน้อยหนึ่งเซลล์</span><span class="sxs-lookup"><span data-stu-id="81bb1-197">Select a range of cells or use **Ctrl** to select one or more cells.</span></span>

1. <span data-ttu-id="81bb1-198">คลิกขวาภายในหนึ่งเซลล์คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="81bb1-198">Right-click inside one of the cells you selected.</span></span>

1. <span data-ttu-id="81bb1-199">เลือก **คัดลอก** > **คัดลอกส่วนที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="81bb1-199">Select **Copy** > **Copy selection**.</span></span>

    ![สกรีนช็อตแสดงสำเนาที่เลือกโดยเลือกตัวเลือกคัดลอก](media/power-bi-visualization-tables/power-bi-copy-selection.png)

## <a name="adjust-the-column-width-of-a-table"></a><span data-ttu-id="81bb1-201">ปรับความกว้างคอลัมน์ของตาราง</span><span class="sxs-lookup"><span data-stu-id="81bb1-201">Adjust the column width of a table</span></span>

<span data-ttu-id="81bb1-202">ในบางครั้ง Power BI จะตัดส่วนหัวของคอลัมน์ในรายงาน และแดชบอร์ดออก</span><span class="sxs-lookup"><span data-stu-id="81bb1-202">Sometimes Power BI will truncate a column heading in a report and on a dashboard.</span></span> <span data-ttu-id="81bb1-203">หากต้องการแสดงชื่อคอลัมน์ทั้งหมด เลื่อนพื้นที่ดังกล่าวไปทางด้านขวาของส่วนหัวเพื่อแสดงลูกศรคู่ เลือกแล้วลาก</span><span class="sxs-lookup"><span data-stu-id="81bb1-203">To show the entire column name, hover over the space to the right of the heading to reveal the double arrows, select, and drag.</span></span>

![วิดีโอระยะใกล้ของการปรับขนาดคอลัมน์](media/power-bi-visualization-tables/resizetable.gif)


## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="81bb1-205">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="81bb1-205">Considerations and troubleshooting</span></span>

* <span data-ttu-id="81bb1-206">เมื่อใช้การจัดรูปแบบคอลัมน์ คุณสามารถเลือกตัวเลือกการจัดแนวเพียงหนึ่งตัวเลือกต่อคอลัมน์: **อัตโนมัติ**, **ซ้าย**, **กึ่งกลาง**, **ขวา**</span><span class="sxs-lookup"><span data-stu-id="81bb1-206">When applying column formatting, you can only choose one alignment option per column: **Auto**, **Left**, **Center**, **Right**.</span></span> <span data-ttu-id="81bb1-207">โดยปกติแล้วจะ คอลัมน์ประกอบด้วยข้อความทั้งหมด หรือตัวเลขทั้งหมด และไม่ผสมกัน</span><span class="sxs-lookup"><span data-stu-id="81bb1-207">Usually, a column contains all text or all numbers, and not a mix.</span></span> <span data-ttu-id="81bb1-208">ในกรณีที่คอลัมน์ที่ประกอบด้วยทั้งตัวเลขและข้อความ **อัตโนมัติ** จะจัดชิดซ้ายสำหรับข้อความ และชิดขวาสำหรับตัวเลข</span><span class="sxs-lookup"><span data-stu-id="81bb1-208">In cases where a column contains both numbers and text, **Auto** will align left for text and right for numbers.</span></span> <span data-ttu-id="81bb1-209">พฤติกรรมนี้สนับสนุนภาษาที่คุณอ่านจากซ้ายไปขวา</span><span class="sxs-lookup"><span data-stu-id="81bb1-209">This behavior supports languages where you read left-to-right.</span></span>

* <span data-ttu-id="81bb1-210">หากข้อมูลข้อความในเซลล์หรือส่วนหัวของตารางของคุณมีอักขระบรรทัดใหม่ อักขระเหล่านั้นจะถูกละเว้นถ้าคุณสลับตัวเลือก 'การตัดคำ' ในการ์ดบานหน้าต่างการจัดรูปแบบที่เกี่ยวข้องขององค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="81bb1-210">If the text data in your table's cells or headers contain new line characters, those characters will be ignored unless you toggle on the 'Word Wrap' option in the element's associated formatting pane card.</span></span> 

* <span data-ttu-id="81bb1-211">Power BI คำนวณขนาดเซลล์สูงสุดตามยี่สิบคอลัมน์แรกและห้าสิบแถวแรก</span><span class="sxs-lookup"><span data-stu-id="81bb1-211">Power BI calculates maximum cell size based on the first twenty columns and the first fifty rows.</span></span> <span data-ttu-id="81bb1-212">เซลล์ที่อยู่นอกเหนือจุดเหล่านั้นอาจมีขนาดไม่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="81bb1-212">Cells beyond those points may not be appropriately sized.</span></span>


## <a name="next-steps"></a><span data-ttu-id="81bb1-213">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="81bb1-213">Next steps</span></span>

* [<span data-ttu-id="81bb1-214">แผนผังต้นไม้ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="81bb1-214">Tree maps in Power BI</span></span>](power-bi-visualization-treemaps.md)

* [<span data-ttu-id="81bb1-215">ชนิดการแสดงภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="81bb1-215">Visualization types in Power BI</span></span>](power-bi-visualization-types-for-reports-and-q-and-a.md)
