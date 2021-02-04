---
title: ตัวสร้างรายงานใน Power BI
description: ตัวสร้างรายงานใน Power BI เป็นเครื่องมือสำหรับเขียนรายงานแบบแบ่งหน้า
author: maggiesMSFT
ms.author: maggies
ms.date: 07/08/2020
ms.service: powerbi
ms.subservice: report-builder
featuredvideoid: 78TZeiEhveY
ms.topic: conceptual
ms.assetid: 55bf4f9c-d037-412f-ae57-3fc39ce32fa5
ms.openlocfilehash: 32d42ee139ceb03326b99d88e6033475ed2a4cc7
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96416266"
---
# <a name="power-bi-report-builder"></a><span data-ttu-id="3fb08-103">ตัวสร้างรายงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3fb08-103">Power BI Report Builder</span></span>

<span data-ttu-id="3fb08-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span><span class="sxs-lookup"><span data-stu-id="3fb08-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span></span> 

<span data-ttu-id="3fb08-105">เครื่องมือตัวสร้างรายงาน Power BI เป็นเครื่องมือสำหรับการสร้างรายงานที่มีการแบ่งหน้าซึ่งคุณสามารถเผยแพร่ไปยังบริการ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="3fb08-105">Power BI Report Builder is a tool for authoring paginated reports that you can publish to the Power BI service.</span></span>  <span data-ttu-id="3fb08-106">เมื่อคุณออกแบบรายงานที่มีการแบ่งหน้า คุณกำลังสร้างข้อกำหนดของรายงานที่ระบุว่าจะเรียกใช้ข้อมูลใด สถานที่เรียก และวิธีแสดงข้อมูลดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="3fb08-106">When you design a paginated report, you're creating a report definition that specifies what data to retrieve, where to get it, and how to display it.</span></span> <span data-ttu-id="3fb08-107">เมื่อคุณเรียกดูรายงาน ตัวประมวลผลรายงานจะใช้ข้อกำหนดของรายงานที่คุณได้ระบุไว้ ดึงเอาข้อมูลนั้นมา แล้วรวมเข้ากับเค้าโครงรายงานเพื่อสร้างรายงานขึ้น</span><span class="sxs-lookup"><span data-stu-id="3fb08-107">When you run the report, the report processor takes the report definition you have specified, retrieves the data, and combines it with the report layout to generate the report.</span></span> <span data-ttu-id="3fb08-108">คุณดูรายงานของคุณได้ก่อนในตัวสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="3fb08-108">You preview your report in Report Builder.</span></span> <span data-ttu-id="3fb08-109">จากนั้น คุณจะเผยแพร่รายงานไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="3fb08-109">Then publish your report to the Power BI service.</span></span>
 
<span data-ttu-id="3fb08-110">พร้อมที่จะเริ่มการเขียนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3fb08-110">Ready to start authoring?</span></span> <span data-ttu-id="3fb08-111">[ติดตั้งตัวสร้างรายงาน Power BI](https://aka.ms/pbireportbuilder) จากศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="3fb08-111">[Install Power BI Report Builder](https://aka.ms/pbireportbuilder) from the Microsoft Download Center.</span></span>

<span data-ttu-id="3fb08-112">คุณอยากเรียนรู้จากวิดิโอมากกว่าใช่ไหม</span><span class="sxs-lookup"><span data-stu-id="3fb08-112">Prefer learning from videos?</span></span> <span data-ttu-id="3fb08-113">ดู[หลักสูตรที่สอนผ่านวิดีโอ: การเรียนรู้เกี่ยวกับรายงานแบบแบ่งหน้าของ Power BI ในวันเดียว](../learning-catalog/paginated-reports-online-course.md)</span><span class="sxs-lookup"><span data-stu-id="3fb08-113">Check out the [Video-based course: Power BI Paginated Reports in a Day](../learning-catalog/paginated-reports-online-course.md).</span></span>

<span data-ttu-id="3fb08-114">รายงานที่มีเลขต่อไปนี้มีเมทริกซ์ที่มีกลุ่มแถว และคอลัมน์เส้นแบบประกายไฟ ตัวบ่งชี้และแผนภูมิวงกลมแบบสรุปในเซลล์มุมพร้อมแผนที่ที่มีข้อมูลทางภูมิศาสตร์สองชุดที่แสดงด้วยสีและขนาดวงกลม</span><span class="sxs-lookup"><span data-stu-id="3fb08-114">The following paginated report features a matrix with row and column groups, sparklines, indicators, and a summary pie chart in the corner cell, accompanied by a map with two sets of geographic data represented by color and by circle size.</span></span>  

![รายงานแบบแบ่งหน้าในบริการของ Power BI](media/report-builder-power-bi/report-builder-get-started-paginated-report.png)

##  <a name="jump-start-report-creation"></a><a name="JumpStartReptCreation"></a> <span data-ttu-id="3fb08-116">การสร้างรายงานอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="3fb08-116">Jump-start report creation</span></span>  
 
-   <span data-ttu-id="3fb08-117">**เริ่มต้นด้วยตาราง, เมทริกซ์หรือตัวช่วยสร้างแผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="3fb08-117">**Start with the Table, Matrix, or Chart wizard**.</span></span> <span data-ttu-id="3fb08-118">สร้างการเชื่อมต่อแหล่งข้อมูล ลากฟิลด์และวางลงเพื่อสร้างคิวรีชุดข้อมูล เลือกเค้าโครงและสไตล์ แล้วปรับแต่งรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="3fb08-118">Create a data source connection, drag and drop fields to create a dataset query, select a layout and style, and customize your report.</span></span>  
  
-   <span data-ttu-id="3fb08-119">**เริ่มด้วยตัวช่วยสร้างแผนที่** คุณสามารถสร้างรายงานที่แสดงข้อมูลรวมกับพื้นหลังทางภูมิศาสตร์หรือเรขาคณิตได้</span><span class="sxs-lookup"><span data-stu-id="3fb08-119">**Start with the Map wizard** to create reports that display aggregated data against a geographic or geometric background.</span></span> <span data-ttu-id="3fb08-120">ข้อมูลแผนที่อาจเป็นข้อมูลเชิงพื้นที่ที่ได้จากคิวรี Transact-SQL หรือจาก Environmental Systems Research Institute, Inc. แฟ้มเชปไฟล์ (ESRI)</span><span class="sxs-lookup"><span data-stu-id="3fb08-120">Map data can be spatial data from a Transact-SQL query or an Environmental Systems Research Institute, Inc. (ESRI) shapefile.</span></span> <span data-ttu-id="3fb08-121">คุณยังสามารถเพิ่มพื้นหลังไทล์แผนที่ของ Microsoft Bing ได้</span><span class="sxs-lookup"><span data-stu-id="3fb08-121">You can also add a Microsoft Bing map tile background.</span></span>  

##  <a name="design-your-report"></a><a name="DesignRept"></a> <span data-ttu-id="3fb08-122">ออกแบบรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="3fb08-122">Design your report</span></span>  
  
-   <span data-ttu-id="3fb08-123">**สร้างรายงานแบบแบ่งหน้าด้วยตาราง เมทริกซ์ แผนภูมิ และเค้าโครงรายงานแบบอิสระ**</span><span class="sxs-lookup"><span data-stu-id="3fb08-123">**Create paginated reports with table, matrix, chart, and free-form report layouts.**</span></span> <span data-ttu-id="3fb08-124">สร้างรายงานแบบตารางสำหรับข้อมูลจากคอลัมน์ รายงายเมทริกซ์ (เช่น รายงานแบบตารางไขว้หรือ PivotTable) สำหรับข้อมูลสรุป รายงานแผนภูมิสำหรับข้อมูลกราฟิก และรายงานแบบอิสระสำหรับข้อมูลอย่างอื่น</span><span class="sxs-lookup"><span data-stu-id="3fb08-124">Create table reports for column-based data, matrix reports (like cross-tab or PivotTable reports) for summarized data, chart reports for graphical data, and free-form reports for anything else.</span></span> <span data-ttu-id="3fb08-125">รายงานสามารถฝังรายงานและแผนภูมิอื่นๆ พร้อมด้วยรายการ กราฟิก และการควบคุมสำหรับโปรแกรมประยุกต์บนเว็บแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="3fb08-125">Reports can embed other reports and charts, together with lists, graphics, and controls for dynamic Web-based applications.</span></span>  
  
-   <span data-ttu-id="3fb08-126">**รายงานจากแหล่งข้อมูลหลายแหล่ง**</span><span class="sxs-lookup"><span data-stu-id="3fb08-126">**Report from a variety of data sources.**</span></span> <span data-ttu-id="3fb08-127">คุณสามารถสร้างรายงานที่ใช้ข้อมูลเชิงสัมพันธ์และหลายมิติจาก SQL Server และ Analysis Services, Oracle, ชุดข้อมูล Power BI และฐานข้อมูลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="3fb08-127">You can create reports that use relational and multidimensional data from SQL Server and Analysis Services, Oracle, Power BI datasets, and other databases.</span></span>  
  
-   <span data-ttu-id="3fb08-128">**การปรับแต่งรายงานที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="3fb08-128">**Modify existing reports.**</span></span> <span data-ttu-id="3fb08-129">โดยการใช้ตัวสร้างรายงาน คุณสามารถปรับและอัพเดทรายงานต่าง ๆ ที่สร้างบนเครื่องมือ SQL เซริฟเวอร์ได้ (SSDT)</span><span class="sxs-lookup"><span data-stu-id="3fb08-129">By using Report Builder, you can customize and update reports that were created in SQL Server Data Tools (SSDT) Report Designer.</span></span>  
  
-   <span data-ttu-id="3fb08-130">**การแก้ไขข้อมูลของคุณ**</span><span class="sxs-lookup"><span data-stu-id="3fb08-130">**Modify your data**.</span></span> <span data-ttu-id="3fb08-131">ตัวกรอง กลุ่ม และเรียงลำดับข้อมูล หรือเพิ่มสูตรหรือนิพจน์</span><span class="sxs-lookup"><span data-stu-id="3fb08-131">Filter, group, and sort data, or add formulas or expressions.</span></span>  

-   <span data-ttu-id="3fb08-132">**เพิ่มแผนภูมิ ตัววัด เส้นแบบประกายไฟ และตัวบ่งชี้**</span><span class="sxs-lookup"><span data-stu-id="3fb08-132">**Add charts, gauges, sparklines, and indicators**.</span></span> <span data-ttu-id="3fb08-133">สรุปข้อมูลในรูปแบบภาพ และนำเสนอข้อมูลที่ถูกรวมเป็นปริมาณมากอย่างย่อ</span><span class="sxs-lookup"><span data-stu-id="3fb08-133">Summarize data in a visual format, and present large volumes of aggregated information at a glance.</span></span>  
  
-   <span data-ttu-id="3fb08-134">**เพิ่มคุณลักษณะแบบโต้ตอบ** เช่น แผนที่เอกสาร แสดง/ซ่อนปุ่ม และลิงก์ลงรายละเอียดไปยังรายงานย่อยและรายงานลงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="3fb08-134">**Add interactive features** such as document maps, show/hide buttons, and drillthrough links to subreports and drillthrough reports.</span></span> <span data-ttu-id="3fb08-135">ใช้พารามิเตอร์และตัวกรองเพื่อกรองข้อมูลสำหรับมุมมองแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="3fb08-135">Use parameters and filters to filter data for customized views.</span></span>  
  
-   <span data-ttu-id="3fb08-136">**รูปภาพฝังหรือรูปภาพอ้างอิง** และทรัพยากรอื่นๆ รวมทั้งเนื้อหาจากภายนอก</span><span class="sxs-lookup"><span data-stu-id="3fb08-136">**Embed or reference images** and other resources, including external content.</span></span>  
  
##  <a name="manage-your-report"></a><a name="ManageRpt"></a> <span data-ttu-id="3fb08-137">จัดการรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="3fb08-137">Manage your report</span></span>  
  
-   <span data-ttu-id="3fb08-138">**บันทึกคำอธิบายของรายงาน** ลงบนคอมพิวเตอร์ของคุณ หรือเซิร์ฟเวอร์รายงาน ที่คุณสามารถจัดการได้และแบ่งปันกับผู้อื่น</span><span class="sxs-lookup"><span data-stu-id="3fb08-138">**Save the definition of the report** to your computer or to the report server, where you can manage it and share it with others.</span></span>  
  
-   <span data-ttu-id="3fb08-139">**เลือกรูปแบบการนำเสนอ** เมื่อคุณเปิดรายงาน หรือหลังจากที่คุณเปิดรายงาน</span><span class="sxs-lookup"><span data-stu-id="3fb08-139">**Choose a presentation format** when you open the report, or after you open the report.</span></span> <span data-ttu-id="3fb08-140">คุณสามารถเลือกสำหรับเว็บ สำหรับหน้า และรูปแบบแอปพลิเคชันเดสก์ท็อป</span><span class="sxs-lookup"><span data-stu-id="3fb08-140">You can select Web-oriented, page-oriented, and desktop application formats.</span></span> <span data-ttu-id="3fb08-141">รูปแบบรวมถึง MHTML, PDF, XML, CSV, Word และ Excel</span><span class="sxs-lookup"><span data-stu-id="3fb08-141">Formats include MHTML, PDF, XML, CSV, Word, and Excel.</span></span>  
  
-   <span data-ttu-id="3fb08-142">**การสมัครใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="3fb08-142">**Set up subscriptions.**</span></span> <span data-ttu-id="3fb08-143">หลังจากเผยแพร่รายงานไปยังบริการ Power BI แล้ว คุณจะสามารถกำหนดค่าให้รายงานของคุณเรียกใช้ ณ เวลาใดเวลาหนึ่ง และส่งเป็นอีเมลการสมัครใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3fb08-143">After you publish the report to the Power BI service, you can configure your report to run at a specific time and send as an e-mail subscription.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="3fb08-144">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3fb08-144">Next steps</span></span>

- [<span data-ttu-id="3fb08-145">รายงานแบบแบ่งหน้าใน Power BI Premium คืออะไร</span><span class="sxs-lookup"><span data-stu-id="3fb08-145">What are paginated reports in Power BI Premium?</span></span>](paginated-reports-report-builder-power-bi.md)
- [<span data-ttu-id="3fb08-146">หลักสูตรที่สอนผ่านวิดีโอ: รายงานที่มีการแบ่งหน้าของ Power BI ในวันเดียว</span><span class="sxs-lookup"><span data-stu-id="3fb08-146">Video-based course: Power BI Paginated Reports in a Day</span></span>](../learning-catalog/paginated-reports-online-course.md)
