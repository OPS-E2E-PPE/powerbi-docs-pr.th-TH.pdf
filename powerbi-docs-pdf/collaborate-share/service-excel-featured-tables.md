---
title: การเข้าถึงตารางที่แนะนำของ Power BI ใน Excel
description: ใน Excel คุณสามารถค้นหาข้อมูลจากตารางที่แนะนำในชุดข้อมูล Power BI ในแกลเลอรีชนิดข้อมูลขององค์กรได้
author: maggiesMSFT
ms.author: maggies
ms.reviewer: lukaszp
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 12/07/2020
LocalizationGroup: Share your work
ms.openlocfilehash: b5f84f67231393dfed78bd9f90142fbd1b4f6c91
ms.sourcegitcommit: 30d0668434283c633bda9ae03bc2aca75401ab94
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/09/2020
ms.locfileid: "96907052"
---
# <a name="access-power-bi-featured-tables-in-excel-organization-data-types"></a><span data-ttu-id="3b38c-103">เข้าถึงตารางที่แนะนำของ Power BI ในชนิดข้อมูลขององค์กรแบบ Excel</span><span class="sxs-lookup"><span data-stu-id="3b38c-103">Access Power BI featured tables in Excel organization data types</span></span>

<span data-ttu-id="3b38c-104">*ตารางที่แนะนำ* เป็นวิธีการเชื่อมโยงข้อมูลของคุณใน Excel ไปยังข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3b38c-104">*Featured tables* are a way to link your data in Excel to data in Power BI.</span></span> <span data-ttu-id="3b38c-105">สิ่งนี้ช่วยให้การเพิ่มข้อมูลระดับองค์กรไปยังแผ่นงาน Excel ของคุณเป็นไปได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="3b38c-105">They make it easier to add enterprise data to your Excel sheets.</span></span> <span data-ttu-id="3b38c-106">ในแกลเลอรีชนิดข้อมูลใน Excel คุณสามารถค้นหาข้อมูลจากตารางที่แนะนำในชุดข้อมูล Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="3b38c-106">In the Data Types Gallery in Excel, you find data from featured tables in Power BI datasets.</span></span> <span data-ttu-id="3b38c-107">บทความนี้จะอธิบายวิธีการ</span><span class="sxs-lookup"><span data-stu-id="3b38c-107">This article explains how.</span></span>

<span data-ttu-id="3b38c-108">คุณสร้างชุดข้อมูลใน Power BI หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="3b38c-108">Do you create datasets in Power BI?</span></span> <span data-ttu-id="3b38c-109">อ่านเกี่ยวกับ [การตั้งค่าตารางที่แนะนำใน Power BI Desktop](service-create-excel-featured-tables.md)</span><span class="sxs-lookup"><span data-stu-id="3b38c-109">Read about [setting featured tables in Power BI Desktop](service-create-excel-featured-tables.md).</span></span>

> [!NOTE]
> <span data-ttu-id="3b38c-110">ใน Excel คุณยังสามารถวิเคราะห์ข้อมูลจากชุดข้อมูล Power BI ใด ๆ ที่คุณสามารถเข้าถึงได้ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3b38c-110">In Excel, you can also analyze data from any Power BI dataset that you can access in Power BI.</span></span> <span data-ttu-id="3b38c-111">ดูที่ [วิธีอื่น ๆ ในการเข้าถึงชุดข้อมูล Power BI จาก Excel](service-analyze-in-excel.md#other-ways-to-access-power-bi-datasets-from-excel) ในบทความ " วิเคราะห์ใน Excel สำหรับ Power BI" สำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="3b38c-111">See [Other ways to access Power BI datasets from Excel](service-analyze-in-excel.md#other-ways-to-access-power-bi-datasets-from-excel) in the "Analyze in Excel for Power BI" article for details.</span></span>
> 

## <a name="the-excel-data-types-gallery"></a><span data-ttu-id="3b38c-112">แกลเลอรีชนิดข้อมูล Excel</span><span class="sxs-lookup"><span data-stu-id="3b38c-112">The Excel Data Types Gallery</span></span>
<span data-ttu-id="3b38c-113">ตารางที่แนะนำในชุดข้อมูล Power BI จะปรากฏเป็น *ชนิดข้อมูล* บนแถบเครื่องมือริบบอน **ข้อมูล** ในแกลเลอรี **ชนิดข้อมูล** Excel</span><span class="sxs-lookup"><span data-stu-id="3b38c-113">Featured tables in Power BI datasets appear as *data types* on the **Data** ribbon, in the Excel **Data Types** gallery.</span></span>

:::image type="content" source="media/service-excel-featured-tables/excel-data-ribbon.png" alt-text="ภาพหน้าจอของแกลเลอรีชนิดข้อมูลในแถบเครื่องมือริบบอนข้อมูล Excel":::

<span data-ttu-id="3b38c-115">เมื่อขยาย แกลเลอรี่จะแสดงชนิดข้อมูลทั่วไป เช่น **สินค้าในคลัง** และ **ภูมิศาสตร์** เสริมด้วยชนิดข้อมูล 10 อันดับแรกของ **องค์กร** ที่คุณสามารถใช้งานได้ -- ตารางที่แนะนำจากชุดข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="3b38c-115">When expanded, the gallery shows the generic data types such as **Stocks** and **Geography**, plus the top 10 **Organization** data types available to you--featured tables from Power BI datasets.</span></span>

:::image type="content" source="media/service-excel-featured-tables/excel-data-types-gallery.png" alt-text="ภาพหน้าจอของแกลเลอรีชนิดข้อมูล Excel":::

## <a name="search-for-power-bi-data-in-the-data-types-gallery"></a><span data-ttu-id="3b38c-117">ค้นหาข้อมูล Power BI ในแกลเลอรีชนิดข้อมูล Excel</span><span class="sxs-lookup"><span data-stu-id="3b38c-117">Search for Power BI data in the Data Types Gallery</span></span>

<span data-ttu-id="3b38c-118">หากต้องการค้นหาข้อมูลในตารางที่แนะนำของ Power BI ให้เลือกเซลล์หรือช่วงในแผ่นงาน Excel ที่มีค่าตรงกับค่าในตารางที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="3b38c-118">To search for data in a Power BI featured table, select a cell or a range in your Excel sheet containing a value that matches the value in a featured table.</span></span> <span data-ttu-id="3b38c-119">เลือกลูกศร **เพิ่มเติม** ถัดจากแกลเลอรี่ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3b38c-119">Select the **More** arrow next to the Data Types gallery.</span></span>

:::image type="content" source="media/service-excel-featured-tables/excel-data-types-more.png" alt-text="สกรีนช็อตของไอคอนเพิ่มเติมในแกลเลอรีชนิดข้อมูล Excel":::

<span data-ttu-id="3b38c-121">หากคุณพบตารางที่คุณกำลังมองหา ให้กดเลือก</span><span class="sxs-lookup"><span data-stu-id="3b38c-121">If you see the table you're looking for, select it.</span></span> <span data-ttu-id="3b38c-122">นอกเหนือจากนี้ เลือก **เพิ่มเติมจากองค์กรของคุณ**</span><span class="sxs-lookup"><span data-stu-id="3b38c-122">Otherwise, select **More from your organization**.</span></span> <span data-ttu-id="3b38c-123">Excel จะแสดงตารางที่แนะนำทั้งหมดที่คุณสามารถเข้าถึงได้ในบานหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="3b38c-123">Excel displays all the featured tables you have access to in the pane.</span></span>

:::image type="content" source="media/service-excel-featured-tables/excel-more-your-organization.png" alt-text="สกรีนช็อตของการเลือกจากองค์กรของคุณ (ตัวอย่าง)":::
 
<span data-ttu-id="3b38c-125">Excel จะแสดงตารางที่แนะนำทั้งหมดที่คุณสามารถเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="3b38c-125">Excel displays all featured tables you have access to.</span></span> <span data-ttu-id="3b38c-126">ในบานหน้าต่าง **ตัวเลือกข้อมูล** ให้พิมพ์ในกล่อง **ตัวกรอง** เพื่อจำกัดตัวเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="3b38c-126">In the **Data Selector** pane, type in the **Filter** box to narrow your options.</span></span> <span data-ttu-id="3b38c-127">เลือกตารางที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="3b38c-127">Select the table you want to use.</span></span>

:::image type="content" source="media/service-excel-featured-tables/excel-data-selector-store.png" alt-text="ภาพหน้าจอของข้อมูลองค์กร Excel, ตารางชนิดข้อมูลผู้จัดหา":::
 
<span data-ttu-id="3b38c-129">หาก Excel พบแถวที่ตรงกันซึ่งมีระดับความน่าเชื่อถือสูง เซลล์จะเชื่อมโยงกับแถวเหล่านั้นทันที</span><span class="sxs-lookup"><span data-stu-id="3b38c-129">If Excel finds matching rows with high confidence, the cells are immediately linked to those rows.</span></span> <span data-ttu-id="3b38c-130">ไอคอนหน่วยข้อมูลที่เชื่อมโยงกันจะระบุเซลล์ที่เชื่อมโยงกับแถวใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3b38c-130">The linked item icon indicates the cells are linked to the rows in Power BI.</span></span>

:::image type="content" source="media/service-excel-featured-tables/excel-linked-card-icon.png" alt-text="ภาพหน้าจอของไอคอนหน่วยข้อมูลที่เชื่อมโยง":::

<span data-ttu-id="3b38c-132">หากเซลล์อาจมีแถวที่ตรงกันมากกว่าหนึ่งแถว เซลล์จะแสดงไอคอนเครื่องหมายคำถาม และบานหน้าต่าง **ตัวเลือกข้อมูล** จะเปิด</span><span class="sxs-lookup"><span data-stu-id="3b38c-132">If a cell has more than one potential matching row, the cell shows a question mark icon, and the **Data Selector** pane opens.</span></span> <span data-ttu-id="3b38c-133">ในตัวอย่างต่อไปนี้เราเลือกช่วงจาก B3:B9 จากนั้นเลือกตารางที่แนะนำของ Power BI **จัดเก็บ**</span><span class="sxs-lookup"><span data-stu-id="3b38c-133">In the following example, we selected a range from B3:B9, then selected the Power BI featured table **Store**.</span></span> <span data-ttu-id="3b38c-134">แถวทั้งหมดมีรายการที่ตรงกัน ยกเว้นเซลล์ B9 "508 - พาซาดีนา ลินด์ซี"</span><span class="sxs-lookup"><span data-stu-id="3b38c-134">All the rows had matches except cell B9, "508 - Pasadena Lindseys".</span></span> <span data-ttu-id="3b38c-135">**ตัวเลือกข้อมูล** แสดงการจับคู่ที่เป็นไปได้สองค่าเดียวกันในสองตารางที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="3b38c-135">The **Data Selector** shows two possible matches, the same value in two different tables.</span></span>

:::image type="content" source="media/service-excel-featured-tables/excel-question-mark-featured-table.png" alt-text="ภาพหน้าจอของบานหน้าต่างตัวเลือกข้อมูล Excel":::
 
<span data-ttu-id="3b38c-137">ตัวเลือกข้อมูลองค์กรสามารถส่งกลับแถวจากหลายตารางที่แนะนำได้</span><span class="sxs-lookup"><span data-stu-id="3b38c-137">The Organization data option can return rows from multiple featured tables.</span></span> <span data-ttu-id="3b38c-138">Excel จะจัดกลุ่มแถวที่อาจตรงกันตามชนิดข้อมูลเดิม</span><span class="sxs-lookup"><span data-stu-id="3b38c-138">Excel groups the potentially matching rows by the data type they came from.</span></span> <span data-ttu-id="3b38c-139">Excel จะเรียงลำดับชนิดข้อมูลโดยยึดตามแถวที่อาจตรงกันที่มีประสิทธิภาพที่สุด</span><span class="sxs-lookup"><span data-stu-id="3b38c-139">Excel sorts the data types based on their strongest potential matching row.</span></span> <span data-ttu-id="3b38c-140">ใช้ลูกศรเชฟรอนเพื่อยุบและขยายชนิดข้อมูลไปยังแถวที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="3b38c-140">Use the chevron arrows to collapse and expand the data types to matching rows.</span></span>

:::image type="content" source="media/service-excel-featured-tables/excel-data-selector-multiple.png" alt-text="ภาพหน้าจอของบานหน้าต่างตัวเลือกข้อมูล Excel ที่มีความเป็นไปได้หลายรายการ":::
 
<span data-ttu-id="3b38c-142">สำหรับคำแนะนำแต่ละรายการ ให้เลือกชื่อแถวในหน้าต่าง **ตัวเลือกข้อมูล** เพื่อดูรายละเอียดเพิ่มเติมภายในแถว เพื่อช่วยให้คุณเลือกแถวที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="3b38c-142">For each suggestion, select the row name in the **Data Selector** pane to see more details within the row to help you pick the right row.</span></span> <span data-ttu-id="3b38c-143">หลังจากที่คุณพบแถวแล้ว ให้กด **เลือก** เพื่อเชื่อมโยงแถวกับเซลล์ใน Excel</span><span class="sxs-lookup"><span data-stu-id="3b38c-143">Once you’ve found it, press **Select** to link the row to the cell in Excel.</span></span> 

:::image type="content" source="media/service-excel-featured-tables/excel-data-selector-details.png" alt-text="ภาพหน้าจอของรายละเอียดตัวเลือกข้อมูล":::

## <a name="explore-related-data"></a><span data-ttu-id="3b38c-145">สำรวจข้อมูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3b38c-145">Explore related data</span></span>

<span data-ttu-id="3b38c-146">ขณะนี้ คุณได้สร้างการเชื่อมต่อระหว่างค่าในแผ่นงาน Excel ของคุณและข้อมูลในตารางที่แนะนำของ Power BI คุณสามารถสำรวจข้อมูลนั้นได้</span><span class="sxs-lookup"><span data-stu-id="3b38c-146">Now that you've created the connection between the values in your Excel sheet and the data in the Power BI featured table, you can explore that data.</span></span> <span data-ttu-id="3b38c-147">ใช้ข้อมูลเพื่อเพิ่มประสิทธิภาพการรายงาน Excel ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3b38c-147">Use the data to enhance your Excel reporting.</span></span>

### <a name="view-related-data-in-a-card"></a><span data-ttu-id="3b38c-148">ดูข้อมูลที่เกี่ยวข้องในการ์ด</span><span class="sxs-lookup"><span data-stu-id="3b38c-148">View related data in a card</span></span> 
 
<span data-ttu-id="3b38c-149">การเลือกไอคอน **การ์ด** ในเซลล์เพื่อแสดงบัตรที่มีข้อมูลจากเขตข้อมูลใด ๆ และเขตข้อมูลจากการคำนวณในตารางที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="3b38c-149">Select the **Card** icon in the cell to show a card with data from any fields and calculated fields in the featured table.</span></span> <span data-ttu-id="3b38c-150">ชื่อของการ์ดแสดงค่าของเขตข้อมูลป้ายชื่อแถวในตารางที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="3b38c-150">The title of the card shows the value of the row label field in the featured table.</span></span>
 
:::image type="content" source="media/service-excel-featured-tables/excel-linked-item-details.png" alt-text="ภาพหน้าจอของรายละเอียดหน่วยข้อมูลที่เชื่อมโยง":::

### <a name="insert-related-data-from-power-bi"></a><span data-ttu-id="3b38c-152">แทรกข้อมูลที่เกี่ยวข้องจาก Power BI</span><span class="sxs-lookup"><span data-stu-id="3b38c-152">Insert related data from Power BI</span></span> 

<span data-ttu-id="3b38c-153">เลือกไอคอน **แทรกข้อมูล** จากนั้นเลือกชื่อเขตข้อมูลจากรายการเขตข้อมูลเพื่อเพิ่มค่าลงในเส้นตาราง</span><span class="sxs-lookup"><span data-stu-id="3b38c-153">Select the **Insert Data** icon, then select a field name from the list of fields to add its value to the grid.</span></span>  

:::image type="content" source="media/service-excel-featured-tables/excel-select-field.png" alt-text="ภาพหน้าจอของเลือกชื่อเขตข้อมูล":::

<span data-ttu-id="3b38c-155">ค่าเขตข้อมูลหนึ่งหรือหลายค่าถูกวางลงในเซลล์ที่อยู่ติดกัน</span><span class="sxs-lookup"><span data-stu-id="3b38c-155">The field value or values are placed in the adjacent cells.</span></span> <span data-ttu-id="3b38c-156">สูตรเซลล์หมายถึงเซลล์ที่เชื่อมโยงและชื่อเขตข้อมูล ดังนั้นคุณสามารถใช้ข้อมูลในฟังก์ชัน Excel ได้</span><span class="sxs-lookup"><span data-stu-id="3b38c-156">The cell formula refers to the linked cell and the field name, so you can use the data in Excel functions.</span></span>

:::image type="content" source="media/service-excel-featured-tables/excel-cell-formula.png" alt-text="ภาพหน้าจอของสูตรเซลล์ Excel":::

### <a name="use-cell-formulas"></a><span data-ttu-id="3b38c-158">ใช้สูตรเซลล์</span><span class="sxs-lookup"><span data-stu-id="3b38c-158">Use cell formulas</span></span>

<span data-ttu-id="3b38c-159">ในตาราง Excel คุณสามารถอ้างอิงไปยังคอลัมน์ตารางที่มีการเชื่อมโยง จากนั้นเพิ่มเขตข้อมูลโดยใช้การอ้างอิง `.` (ช่วงเวลา)</span><span class="sxs-lookup"><span data-stu-id="3b38c-159">In an Excel table, you can refer to the linked table column and then add data fields using the `.` (period) reference.</span></span>

:::image type="content" source="media/service-excel-featured-tables/excel-dot-reference.png" alt-text="ภาพหน้าจอของการอ้างอิงช่วงเวลา Excel":::

<span data-ttu-id="3b38c-161">เช่นเดียวกันในเซลล์ คุณสามารถอ้างอิงไปยังเซลล์และใช้การอ้างอิง `.` (ช่วงเวลา) เพื่อเรียกเขตข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="3b38c-161">Likewise in a cell, you can refer to the cell and use the `.` (period) reference to retrieve fields.</span></span>

:::image type="content" source="media/service-excel-featured-tables/excel-cell-dot-reference.png" alt-text="ภาพหน้าจอของการอ้างอิงช่วงเวลาเซลล์":::

### <a name="show-a-card-change-or-convert-to-text"></a><span data-ttu-id="3b38c-163">แสดงการ์ด เปลี่ยนแปลง หรือแปลงเป็นข้อความ</span><span class="sxs-lookup"><span data-stu-id="3b38c-163">Show a card, change, or convert to text</span></span>

<span data-ttu-id="3b38c-164">เซลล์ที่เชื่อมโยงได้เพิ่มตัวเลือกเมนูการคลิกขวาแล้ว</span><span class="sxs-lookup"><span data-stu-id="3b38c-164">Linked cells have added right-click menu options.</span></span> <span data-ttu-id="3b38c-165">คลิกขวาที่เซลล์</span><span class="sxs-lookup"><span data-stu-id="3b38c-165">Right-click a cell.</span></span> <span data-ttu-id="3b38c-166">นอกจากตัวเลือกตามปกแล้ว คุณจะเห็นรายการต่อไปนี้ด้วย:</span><span class="sxs-lookup"><span data-stu-id="3b38c-166">Along with the usual options, you also see:</span></span>

- <span data-ttu-id="3b38c-167">**แสดงการ์ดชนิดข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="3b38c-167">**Show Data Type Card**.</span></span>
- <span data-ttu-id="3b38c-168">**ชนิดของข้อมูล** > **แปลงเป็นข้อความ**</span><span class="sxs-lookup"><span data-stu-id="3b38c-168">**Data Type** > **Convert to Text**.</span></span>
- <span data-ttu-id="3b38c-169">**ชนิดของข้อมูล** > **เปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="3b38c-169">**Data Type** > **Change**.</span></span>
- <span data-ttu-id="3b38c-170">**รีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="3b38c-170">**Refresh**.</span></span>

:::image type="content" source="media/service-excel-featured-tables/excel-right-click-data-type.png" alt-text="ภาพหน้าจอของคลิกขวา แปลงเป็นข้อความ":::
 
<span data-ttu-id="3b38c-172">**แปลงเป็นข้อความ** นำการเชื่อมโยงกับแถวในตารางที่แนะนำ Power BI ออก</span><span class="sxs-lookup"><span data-stu-id="3b38c-172">**Convert to Text** removes the link to the row in the Power BI featured table.</span></span> <span data-ttu-id="3b38c-173">ที่สำคัญคือข้อความในเซลล์จะเป็นค่าป้ายชื่อแถวของเซลล์ที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="3b38c-173">Importantly, the text in the cell will be the row label value of the linked cell.</span></span> <span data-ttu-id="3b38c-174">ถ้าคุณเชื่อมโยงเซลล์ไปยังแถวที่คุณไม่ได้ตั้งใจ ให้เลือก **เลิกทำ** ใน Excel เพื่อคืนค่าเซลล์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3b38c-174">If you linked a cell to a row you didn’t intend to, select **Undo** in Excel to restore the initial cell values.</span></span>
 
## <a name="data-caching-and-refresh"></a><span data-ttu-id="3b38c-175">การแคชข้อมูลและการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="3b38c-175">Data caching and refresh</span></span>

<span data-ttu-id="3b38c-176">เมื่อ Excel เชื่อมโยงเซลล์ไปยังแถวในตารางที่แนะนำของ Power BI ค่าเขตข้อมูลทั้งหมดจะถูกดึงออกมาและบันทึกในไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="3b38c-176">When Excel links a cell to a row in a Power BI featured table, it retrieves and saves all the field values in the Excel file.</span></span> <span data-ttu-id="3b38c-177">ทุกคนที่คุณแชร์ไฟล์ด้วยสามารถอ้างอิงถึงเขตข้อมูลใดๆ ได้โดยไม่ต้องร้องขอข้อมูลจาก Power BI</span><span class="sxs-lookup"><span data-stu-id="3b38c-177">Anyone you share the file with can refer to any of the fields, without requesting data from Power BI.</span></span>  

<span data-ttu-id="3b38c-178">ใช้ปุ่ม **รีเฟรชทั้งหมด** ในแถบเครื่องมือ **ข้อมูล** เพื่อรีเฟรชข้อมูลในเซลล์ที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="3b38c-178">Use the **Refresh All** button in the **Data** ribbon to refresh data in linked cells.</span></span> 

:::image type="content" source="media/service-excel-featured-tables/excel-refresh-all.png" alt-text="ภาพหน้าจอของรีเฟรชทั้งหมด":::
 
<span data-ttu-id="3b38c-180">คุณยังสามารถรีเฟรชเซลล์ทีละรายการได้</span><span class="sxs-lookup"><span data-stu-id="3b38c-180">You can also refresh individual cells.</span></span> <span data-ttu-id="3b38c-181">คลิกขวาที่เซลล์และเลือก **ชนิดข้อมูล** > **รีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="3b38c-181">Right-click the cell and select **Data Types** > **Refresh**.</span></span>

## <a name="licensing"></a><span data-ttu-id="3b38c-182">สิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3b38c-182">Licensing</span></span>

<span data-ttu-id="3b38c-183">แกลเลอรีชนิดข้อมูล Excel และประสบการณ์การเชื่อมต่อกับตารางที่แนะนำของ Power BI จะพร้อมใช้งานสำหรับสมาชิก Excel ที่มีแผนบริการ Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="3b38c-183">The Excel Data Types Gallery and connected experiences to Power BI featured tables is available for Excel subscribers with a Power BI Pro service plan..</span></span> 

## <a name="security"></a><span data-ttu-id="3b38c-184">ความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="3b38c-184">Security</span></span>

<span data-ttu-id="3b38c-185">คุณจะเห็นเฉพาะตารางที่แนะนำจากชุดข้อมูลที่คุณมีสิทธิ์เข้าถึงใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3b38c-185">You see only featured tables from datasets you have permission to in Power BI.</span></span> <span data-ttu-id="3b38c-186">เมื่อรีเฟรชข้อมูล คุณต้องมีสิทธิ์ในการเข้าถึงชุดข้อมูลใน Power BI เพื่อเรียกแถว</span><span class="sxs-lookup"><span data-stu-id="3b38c-186">When refreshing data, you must have permission to access the dataset in Power BI to retrieve the rows.</span></span> <span data-ttu-id="3b38c-187">คุณจำเป็นต้อง [สร้างหรือเขียนสิทธิ์บนชุดข้อมูล](../connect-data/service-datasets-build-permissions.md) ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3b38c-187">You need [Build or Write permission on the dataset](../connect-data/service-datasets-build-permissions.md) in Power BI.</span></span>
 
<span data-ttu-id="3b38c-188">Excel แคชข้อมูลที่ส่งกลับสำหรับทั้งแถว</span><span class="sxs-lookup"><span data-stu-id="3b38c-188">Excel caches the data returned for the entire row.</span></span> <span data-ttu-id="3b38c-189">ทุกคนที่คุณแชร์ไฟล์ Excel ด้วยสามารถดูข้อมูลสำหรับเขตข้อมูลทั้งหมดในเซลล์ที่เชื่อมโยงทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="3b38c-189">Anyone you share the Excel file with can see the data for all the fields in all the linked cells.</span></span>

## <a name="administrative-control"></a><span data-ttu-id="3b38c-190">การควบคุมการดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="3b38c-190">Administrative control</span></span>

<span data-ttu-id="3b38c-191">ผู้ดูแลระบบ Power BI สามารถควบคุมกำหนดบุคคลในองค์กรที่สามารถใช้ตารางที่แนะนำในแกลเลอรีประเภทข้อมูล Excel ได้</span><span class="sxs-lookup"><span data-stu-id="3b38c-191">Power BI admins can control who in the organization can use featured tables in the Excel Data Types Gallery.</span></span> <span data-ttu-id="3b38c-192">ดู[อนุญาตให้เชื่อมต่อกับตารางที่แนะนำ](../admin/service-admin-portal.md#allow-connections-to-featured-tables)ในบทความพอร์ทัลผู้ดูแลระบบสำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="3b38c-192">See [Allow connections to featured tables](../admin/service-admin-portal.md#allow-connections-to-featured-tables) in the Admin portal article for details.</span></span> 
 
### <a name="auditing"></a><span data-ttu-id="3b38c-193">การตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="3b38c-193">Auditing</span></span>

<span data-ttu-id="3b38c-194">บันทึกการตรวจสอบการจัดการแสดงเหตุการณ์เหล่านี้สำหรับตารางที่แนะนำ:</span><span class="sxs-lookup"><span data-stu-id="3b38c-194">Administration audit logs show these events for featured tables:</span></span>

- <span data-ttu-id="3b38c-195">**AnalyzedByExternalApplication**: ให้ผู้ดูแลระบบสามารถมองเห็นว่าผู้ใช้ใดกำลังเข้าถึงตารางที่แนะนำชนิดใด</span><span class="sxs-lookup"><span data-stu-id="3b38c-195">**AnalyzedByExternalApplication**: Gives admins visibility into which users are accessing which featured tables.</span></span>
- <span data-ttu-id="3b38c-196">**UpdateFeaturedTables**: ให้ผู้ดูแลระบบสามารถมองเห็นว่าผู้ใช้ใดกำลังเผยแพร่และอัปเดตตารางที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="3b38c-196">**UpdateFeaturedTables**: Gives admins visibility into which users are publishing and updating featured tables.</span></span>

<span data-ttu-id="3b38c-197">สำหรับรายการทั้งหมดของเหตุการณ์บันทึกการตรวจสอบ ดู [ติดตามกิจกรรมของผู้ใช้ใน Power BI](../admin/service-admin-auditing.md)</span><span class="sxs-lookup"><span data-stu-id="3b38c-197">For a complete list of audit log events, see [Track user activities in Power BI](../admin/service-admin-auditing.md).</span></span>

## <a name="considerations-and-limitations"></a><span data-ttu-id="3b38c-198">ข้อควรพิจารณาและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="3b38c-198">Considerations and limitations</span></span>

<span data-ttu-id="3b38c-199">ข้อจำกัดในปัจจุบันมีดังนี้:</span><span class="sxs-lookup"><span data-stu-id="3b38c-199">Here are the current limitations:</span></span>

- <span data-ttu-id="3b38c-200">การรวมพร้อมให้ใช้งานใน Excel สำหรับช่องทางปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="3b38c-200">The integration is available in Excel in the current channel.</span></span>
- <span data-ttu-id="3b38c-201">ตารางที่แนะนำในชุดข้อมูล Power BI ที่ใช้ความสามารถดังต่อไปนี้ไม่ได้แสดงใน Excel:</span><span class="sxs-lookup"><span data-stu-id="3b38c-201">Featured tables in Power BI datasets that use the following capabilities aren't shown in Excel:</span></span> 

    - <span data-ttu-id="3b38c-202">ชุดข้อมูล DirectQuery</span><span class="sxs-lookup"><span data-stu-id="3b38c-202">DirectQuery datasets.</span></span>
    - <span data-ttu-id="3b38c-203">ชุดข้อมูลที่มีการเชื่อมต่อสด</span><span class="sxs-lookup"><span data-stu-id="3b38c-203">Datasets with a live connection.</span></span>

- <span data-ttu-id="3b38c-204">Excel แสดงเฉพาะข้อมูลในคอลัมน์ คอลัมน์จากการคำนวณ และหน่วยวัดที่กำหนดไว้ในตารางที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="3b38c-204">Excel shows only data in columns, calculated columns, and measures defined in the featured table.</span></span> <span data-ttu-id="3b38c-205">ไม่มีรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3b38c-205">The following aren't provided:</span></span>
   
    - <span data-ttu-id="3b38c-206">หน่วยวัดที่กำหนดในตารางที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3b38c-206">Measures defined on related tables.</span></span>
    - <span data-ttu-id="3b38c-207">หน่วยวัดโดยนัยที่คำนวณจากความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="3b38c-207">Implicit measures calculated from relationships.</span></span>

- <span data-ttu-id="3b38c-208">Excel จะแสดงเฉพาะตารางที่แนะนำ (*ชนิดข้อมูล*) ที่จัดเก็บในพื้นที่ทำงาน Power BI ใหม่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3b38c-208">Excel only displays featured tables (*data types*) that are stored in the new Power BI workspaces.</span></span> <span data-ttu-id="3b38c-209">ตารางที่แนะนำที่จัดเก็บไว้ในพื้นที่ทำงานแบบคลาสสิกไม่ได้แสดงเป็นรูปแบบชนิดข้อมูลใน Excel</span><span class="sxs-lookup"><span data-stu-id="3b38c-209">Featured tables stored in the classic workspaces  aren't shown as data types in Excel.</span></span> <span data-ttu-id="3b38c-210">คุณสามารถ [ อัปเกรดพื้นที่ทำงานแบบคลาสสิกเป็นพื้นที่งานใหม่ใน](service-upgrade-workspaces.md) Power BI</span><span class="sxs-lookup"><span data-stu-id="3b38c-210">You can [upgrade classic workspaces to the new workspaces](service-upgrade-workspaces.md) in Power BI.</span></span>

<span data-ttu-id="3b38c-211">ประสบการณ์ชนิดข้อมูลใน Excel จะคล้ายกับฟังก์ชันการค้นหา</span><span class="sxs-lookup"><span data-stu-id="3b38c-211">The Data Types experience in Excel is similar to a lookup function.</span></span> <span data-ttu-id="3b38c-212">โดยจะใช้ค่าเซลล์ที่ให้มาจากแผ่นงาน Excel และค้นหาแถวที่ตรงกันในตารางที่แนะนำของ Power BI</span><span class="sxs-lookup"><span data-stu-id="3b38c-212">It takes a cell value provided by the Excel sheet, and searches for matching rows in Power BI featured tables.</span></span> <span data-ttu-id="3b38c-213">ประสบการณ์การค้นหามีลักษณะการทำงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3b38c-213">The search experience has the following behaviors:</span></span>

- <span data-ttu-id="3b38c-214">การจับคู่แถวจะขึ้นอยู่กับคอลัมน์ข้อความในตารางที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="3b38c-214">Row matching is based on text columns in the featured table.</span></span> <span data-ttu-id="3b38c-215">ซึ่งใช้การจัดทำดัชนีแบบเดียวกันกับความสามารถ Power BI Q&A ซึ่งได้รับการปรับให้เหมาะสมสำหรับการค้นหาภาษาอังกฤษ</span><span class="sxs-lookup"><span data-stu-id="3b38c-215">It uses the same indexing as Power BI Q&A capability, which is optimized for English-language search.</span></span> <span data-ttu-id="3b38c-216">การค้นหาในภาษาอื่นอาจได้ผลการจับคู่ที่แม่นยำ</span><span class="sxs-lookup"><span data-stu-id="3b38c-216">Searching in other languages may not result in accurate matches.</span></span> 
- <span data-ttu-id="3b38c-217">คอลัมน์ตัวเลขส่วนใหญ่จะไม่ถูกนำมาพิจารณาสำหรับการจับคู่</span><span class="sxs-lookup"><span data-stu-id="3b38c-217">Most numerical columns aren't considered for matching.</span></span> <span data-ttu-id="3b38c-218">หากป้ายชื่อแถวหรือคอลัมน์คีย์เป็นตัวเลข จะรวมไว้สำหรับการจับคู่</span><span class="sxs-lookup"><span data-stu-id="3b38c-218">If the Row Label or Key Column are numeric, they are included for matching.</span></span>
- <span data-ttu-id="3b38c-219">การจับคู่จะขึ้นอยู่กับการจับคู่ที่แน่นอนและการจับคู่คำนำหน้าสำหรับคำค้นหาแต่ละคำ</span><span class="sxs-lookup"><span data-stu-id="3b38c-219">Matching is based on Exact and Prefix matches for individual search terms.</span></span> <span data-ttu-id="3b38c-220">ค่าของเซลล์ถูกแยกตามช่องว่างหรือตัวอักขระช่องว่างอื่นๆ เช่น แท็บ</span><span class="sxs-lookup"><span data-stu-id="3b38c-220">A cell’s value is split based on spaces or other whitespace characters like tabs.</span></span> <span data-ttu-id="3b38c-221">จากนั้นจะถือว่าแต่ละคำเป็นคำที่ใช้ค้นหา</span><span class="sxs-lookup"><span data-stu-id="3b38c-221">Then each word is considered a search term.</span></span> <span data-ttu-id="3b38c-222">ค่าเขตข้อมูลข้อความของแถวจะถูกเปรียบเทียบกับคำที่ใช้ค้นหาแต่ละรายการสำหรับการจับคู่ที่แน่นอนและการจับคำนำหน้า</span><span class="sxs-lookup"><span data-stu-id="3b38c-222">A row’s text field values are compared to each search term for Exact and Prefix matches.</span></span> <span data-ttu-id="3b38c-223">การจับคู่คำนำหน้าจะถูกส่งกลับถ้าเขตข้อมูลข้อความของแถวเริ่มต้นด้วยคำที่ใช้ค้นหา</span><span class="sxs-lookup"><span data-stu-id="3b38c-223">A Prefix match is returned if the row’s text field starts with the search term.</span></span> <span data-ttu-id="3b38c-224">ตัวอย่างเช่น ถ้าเซลล์มี "Orange County" ดังนั้น "Orange" และ "County" เป็นคำที่ใช้ค้นหาที่แยกจากกัน</span><span class="sxs-lookup"><span data-stu-id="3b38c-224">For example, if a cell contains “Orange County”, then “Orange” and “County” are distinct search terms.</span></span> 

    - <span data-ttu-id="3b38c-225">แถวที่มีคอลัมน์ข้อความซึ่งมีค่าที่ตรงกับ "Orange" หรือ "County" จะถูกส่งกลับมา</span><span class="sxs-lookup"><span data-stu-id="3b38c-225">Rows with text columns whose values exactly match “Orange” or “County” are returned.</span></span> 
    - <span data-ttu-id="3b38c-226">แถวที่มีคอลัมน์ข้อความซึ่งมีค่าเริ่มต้นด้วย "Orange" หรือ "County" จะถูกส่งกลับมา</span><span class="sxs-lookup"><span data-stu-id="3b38c-226">Rows with text columns whose values start with “Orange” or “County” are returned.</span></span> 
    - <span data-ttu-id="3b38c-227">ที่สำคัญคือ แถวที่ประกอบด้วย "Orange" หรือ "County" แต่ไม่ได้เริ่มต้นด้วยสองคำนี้จะไม่ถูกส่งกลับมา</span><span class="sxs-lookup"><span data-stu-id="3b38c-227">Importantly, rows that contain “Orange” or “County” but don’t start with them aren't returned.</span></span>

- <span data-ttu-id="3b38c-228">Power BI จะส่งกลับผลลัพธ์ที่แนะนำอย่างมากที่สุด 100 แถวสำหรับแต่ละเซลล์</span><span class="sxs-lookup"><span data-stu-id="3b38c-228">Power BI returns at most 100 row suggestions for each cell.</span></span>
- <span data-ttu-id="3b38c-229">ไม่รองรับสัญลักษณ์บางอย่าง</span><span class="sxs-lookup"><span data-stu-id="3b38c-229">Some symbols aren't supported.</span></span>
- <span data-ttu-id="3b38c-230">ไม่รองรับการตั้งค่าหรือการอัปเดตตารางที่แนะนำในตำแหน่งข้อมูล XMLA</span><span class="sxs-lookup"><span data-stu-id="3b38c-230">Setting or updating the featured table isn't supported in the XMLA endpoint</span></span>
- <span data-ttu-id="3b38c-231">ไฟล์ Excel ที่มีรูปแบบข้อมูลสามารถใช้ในการเผยแพร่ตารางที่แนะนำได้</span><span class="sxs-lookup"><span data-stu-id="3b38c-231">Excel files with a data model can be used to publish featured tables.</span></span> <span data-ttu-id="3b38c-232">โหลดข้อมูลลงใน Power BI desktop แล้วจึงเผยแพร่ตารางที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="3b38c-232">Load the data into Power BI desktop and then publish the featured table.</span></span>
- <span data-ttu-id="3b38c-233">การเปลี่ยนชื่อตาราง ป้ายชื่อแถว หรือคอลัมน์คีย์ของตารางที่แนะนำอาจส่งผลกระทบต่อผู้ใช้ Excel ที่มีเซลล์ที่เชื่อมโยงไปยังแถวในตาราง</span><span class="sxs-lookup"><span data-stu-id="3b38c-233">Changing the Table name, Row Label, or Key Column the featured table may impact Excel users with linked cells to rows in the table.</span></span> 
- <span data-ttu-id="3b38c-234">Excel แสดงเวลาที่มีการดึงข้อมูลจากชุดข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="3b38c-234">Excel shows when the data was retrieved from the Power BI dataset.</span></span> <span data-ttu-id="3b38c-235">เวลานี้ไม่จำเป็นต้องเป็นเวลาที่รีเฟรชข้อมูลใน Power BI หรือเวลาของจุดข้อมูลล่าสุดในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3b38c-235">This time isn't necessarily the time that the data was refreshed in Power BI, or the time of the most recent data point in a dataset.</span></span> <span data-ttu-id="3b38c-236">ตัวอย่างเช่น สมมติว่าชุดข้อมูลใน Power BI ได้รับการรีเฟรชสัปดาห์ที่ผ่านมา แต่แหล่งข้อมูลพื้นฐานมีอายุหนึ่งสัปดาห์ในตอนที่มีการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="3b38c-236">For example, say a dataset in Power BI was refreshed a week ago, but the underlying source data was a week old when the refresh happened.</span></span> <span data-ttu-id="3b38c-237">ข้อมูลจริงอาจจะมีอายุสองสัปดาห์ แต่ Excel จะแสดงข้อมูลที่มีการเรียกในวันที่/เวลาที่มีการดึงข้อมูลลงใน Excel</span><span class="sxs-lookup"><span data-stu-id="3b38c-237">The actual data would be two weeks old, but Excel would show data retrieved as the date/time at which the data was pulled into Excel.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="3b38c-238">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3b38c-238">Next steps</span></span>

- [<span data-ttu-id="3b38c-239">ตั้งค่าตารางที่แนะนำใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3b38c-239">Set featured tables in Power BI Desktop</span></span>](service-create-excel-featured-tables.md)
- <span data-ttu-id="3b38c-240">อ่านข้อมูลเกี่ยวกับ[การใช้ชนิดข้อมูล Excel จาก Power BI](https://support.office.com/article/use-excel-data-types-from-power-bi-preview-cd8938ce-f963-444d-b82a-7140848241e9) ในเอกสารประกอบของ Excel</span><span class="sxs-lookup"><span data-stu-id="3b38c-240">Read about [using Excel data types from Power BI](https://support.office.com/article/use-excel-data-types-from-power-bi-preview-cd8938ce-f963-444d-b82a-7140848241e9) in the Excel documentation.</span></span>
- <span data-ttu-id="3b38c-241">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3b38c-241">Questions?</span></span> [<span data-ttu-id="3b38c-242">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="3b38c-242">Try the Power BI Community</span></span>](https://community.powerbi.com/)

