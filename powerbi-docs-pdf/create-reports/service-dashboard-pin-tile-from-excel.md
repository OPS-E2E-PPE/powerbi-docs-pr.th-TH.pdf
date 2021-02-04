---
title: ปักหมุดไทล์ที่แดชบอร์ด Power BI จาก Excel
description: ปักหมุดไทล์ที่แดชบอร์ด Power BI จาก Excel บน OneDrive for Business ปักหมุดช่วง แผนภูมิ ตาราง
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: l8JoB7w0zJA
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 05/02/2018
LocalizationGroup: Dashboards
ms.openlocfilehash: b62a780bc504c0b2fc90aa368d8dc30ac745867e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96417416"
---
# <a name="pin-a-tile-to-a-power-bi-dashboard-from-excel"></a><span data-ttu-id="8578e-104">ปักหมุดไทล์ไปที่แดชบอร์ด Power BI จาก Excel</span><span class="sxs-lookup"><span data-stu-id="8578e-104">Pin a tile to a Power BI dashboard from Excel</span></span>
<span data-ttu-id="8578e-105">ก่อนที่คุณสามารถปักหมุดไทล์จากสมุดงาน Excel ของคุณ คุณจะเชื่อมต่อเวิร์กบุ๊กนั้นกับเซอร์วิซ Power BI (app.powerbi.com)</span><span class="sxs-lookup"><span data-stu-id="8578e-105">Before you can pin a tile from your Excel workbook, you'll connect that workbook to Power BI service (app.powerbi.com).</span></span> <span data-ttu-id="8578e-106">การเชื่อมต่อเวิร์กบุ๊กโดยหลักๆ คือการนำลิงก์เวอร์ชันอ่านอย่างเดียวของเวิร์กบุ๊กนั้นลงในยังเซอร์วิซ Power BI และให้คุณสามารถปักหมุดช่วงในแดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="8578e-106">Connecting a workbook essentially brings a linked read-only version of that workbook into Power BI service and allows you to pin ranges to dashboards.</span></span> <span data-ttu-id="8578e-107">คุณสามารถแม้กระทั้งปักหมุดทั้งแผ่นงานกับยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="8578e-107">You can even pin an entire worksheet to a dashboard.</span></span>  
<span data-ttu-id="8578e-108">ถ้าเวิร์กบุ๊กได้แชร์กับคุณ คุณจะมีความสามารถในการดูไทล์ที่ปักโดยเจ้าของ แต่อย่าสร้างแดชบอร์ดไทล์ด้วยตัวคุณเอง</span><span class="sxs-lookup"><span data-stu-id="8578e-108">If a workbook has been shared with you, you'll have the ability to view the tiles pinned by the owner, but not create any dashboard tiles yourself.</span></span> 

<span data-ttu-id="8578e-109">สำหรับข้อมูลเชิงลึกเกี่ยวกับว่า Excel และ Power BI ทำงานร่วมกันอย่างไร ให้ดู[รับข้อมูลจากแฟ้มสมุดงาน Excel](https://go.microsoft.com/fwlink/?LinkID=521962)</span><span class="sxs-lookup"><span data-stu-id="8578e-109">For in-depth information about how Excel and Power BI work together, see [Get data from Excel workbook files](https://go.microsoft.com/fwlink/?LinkID=521962).</span></span>

<span data-ttu-id="8578e-110">Watch Will แสดงให้เห็นวิธีการนำเข้าข้อมูลหลายวิธีจาก และเชื่อมต่อไปยัง เวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="8578e-110">Watch Will demonstrate several ways to import data from, and connect to, Excel workbooks.</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/l8JoB7w0zJA" frameborder="0" allowfullscreen></iframe>

## <a name="connect-your-excel-workbook-from-onedrive-for-business-to-power-bi"></a><span data-ttu-id="8578e-111">เชื่อมต่อเวิร์กบุ๊ก Excel ของคุณจาก OneDrive for Business กับ Power BI</span><span class="sxs-lookup"><span data-stu-id="8578e-111">Connect your Excel workbook from OneDrive for Business to Power BI</span></span>
<span data-ttu-id="8578e-112">เมื่อคุณเลือกตัวเลือกนี้ **สมุดงานข** องคุณจะปรากฏใน Power BI เช่นเดียวกับที่ปรากฏใน Excel Online</span><span class="sxs-lookup"><span data-stu-id="8578e-112">When you choose **Connect**, your workbook will appear in Power BI just like it would in Excel Online.</span></span> <span data-ttu-id="8578e-113">แต่ไม่เหมือนกับ Excel Online เนื่องจากคุณจะมีคุณลักษณะบางอย่างที่ช่วยให้คุณสามารถปักหมุดองค์ประกอบต่าง ๆ จากแผ่นงานของคุณไปยังแดชบอร์ดได้ทันที</span><span class="sxs-lookup"><span data-stu-id="8578e-113">But, unlike Excel Online, you’ll have some great features to help you pin elements from your worksheets right to your dashboards.</span></span>

<span data-ttu-id="8578e-114">คุณไม่สามารถแก้ไขเวิร์กบุ๊กของคุณใน Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="8578e-114">You can’t edit your workbook in Power BI.</span></span> <span data-ttu-id="8578e-115">แต่ถ้าคุณจำเป็นต้องทำการเปลี่ยนแปลงบางอย่าง คุณสามารถเลือกไอคอนดินสอจากแถบ **เวิ๊กบุ๊ก** ของพื้นที่การทำงานของคุณใน Excel Online หรือเปิดใน Excel บนคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8578e-115">But if you need to make some changes, you can select the pencil icon from the **Workbooks** tab of your workspace, and then choose to edit your workbook in Excel Online or open it in Excel on your computer.</span></span> <span data-ttu-id="8578e-116">การเปลี่ยนแปลงใด ๆ ที่คุณดำเนินการจะถูกบันทึกไปยังสมุดงานบน OneDrive</span><span class="sxs-lookup"><span data-stu-id="8578e-116">Any changes you make are saved to the workbook on OneDrive.</span></span>

1. <span data-ttu-id="8578e-117">อัปโหลดเวิร์กบุ๊กของคุณไปยัง OneDrive for Business ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8578e-117">Upload your workbook to your OneDrive for Business.</span></span>

2. <span data-ttu-id="8578e-118">จาก Power BI, [เชื่อมต่อกับสมุดงานนั้น](../connect-data/service-excel-workbook-files.md)โดยการเลือก **รับข้อมูล > ไฟล์ > OneDrive - ธุรกิจ** และไปยังตำแหน่งที่ตั้งคุณบันทึกไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="8578e-118">From Power BI, [connect to that workbook](../connect-data/service-excel-workbook-files.md) by selecting **Get Data > Files > OneDrive - Business** and nagivating to the location where you saved the Excel file.</span></span> <span data-ttu-id="8578e-119">เลือกไฟล์ แล้วเลือก **เชื่อมต่อ > เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="8578e-119">Select the file and choose **Connect > Connect**.</span></span>

    ![หน้าต่างโต้ตอบ OneDrive for Business](media/service-dashboard-pin-tile-from-excel/power-bi-connect.png)

3. <span data-ttu-id="8578e-121">ใน Power BI เวิร์กบุ๊กจะถูกเพิ่มไปยังแท็บ **เวิร์กบุ๊ก** ของพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="8578e-121">In Power BI, the workbook is added to the **Workbooks** tab of your workspace.</span></span>  <span data-ttu-id="8578e-122">ไอคอน![ไอคอนเวิร์กบุ๊ก](media/service-dashboard-pin-tile-from-excel/pbi_workbookicon.png)ระบุว่านี่คือเวิร์กบุ๊ก Excel และเครื่องหมายดอกจันสีเหลืองบ่งชี้ว่าใหม่</span><span class="sxs-lookup"><span data-stu-id="8578e-122">The ![workbook icon](media/service-dashboard-pin-tile-from-excel/pbi_workbookicon.png) icon indicates this is an Excel workbook and a yellow asterisk indicates it's new.</span></span>
    
    ![แถบเวิร์กบุ๊ก](media/service-dashboard-pin-tile-from-excel/power-bi-workbooks.png)
4. <span data-ttu-id="8578e-124">เปิดเวิร์กบุ๊กใน Power BI โดยเลือกชื่อเวิร์กบุ๊ก</span><span class="sxs-lookup"><span data-stu-id="8578e-124">Open the workbook in Power BI by selecting the workbook name.</span></span>

    <span data-ttu-id="8578e-125">เปลี่ยนแปลงที่คุณทำกับเวิร์กบุ๊กใน Power BI จะไม่ถูกบันทึก และไม่มีผลต่อเวิร์กบุ๊กดั้งเดิมบน OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="8578e-125">Changes you make to the workbook in Power BI are not saved and do not affect the original workbook on OneDrive for Business.</span></span> <span data-ttu-id="8578e-126">ถ้าคุณเรียงลำดับ กรอง หรือเปลี่ยนค่าใน Power BI การเปลี่ยนแปลงเหล่านั้นไม่สามารถบันทึกหรือปักหมุดได้</span><span class="sxs-lookup"><span data-stu-id="8578e-126">If you sort, filter, or change values in Power BI, those changes cannot be saved or pinned.</span></span> <span data-ttu-id="8578e-127">ถ้าคุณจำเป็นต้องทำการเปลี่ยนแปลงที่จะถูกบันทึก เลือก **แก้ไข** จากมุมขวาบนเพื่อเปิดสำหรับการแก้ไขใน Excel Online หรือ Excel</span><span class="sxs-lookup"><span data-stu-id="8578e-127">If you need to make changes that will be saved, select **Edit** from the upper-right corner to open it for editing in Excel Online or Excel.</span></span> <span data-ttu-id="8578e-128">การเปลี่ยนแปลงด้วยวิธีนี้อาจใช้เวลาสักครู่เพื่อปรับปรุงไทล์บนแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="8578e-128">Changes made this way may take a few minutes to update the tiles on the dashboards.</span></span>
   
    ![Excel Online ใน Power BI](media/service-dashboard-pin-tile-from-excel/power-bi-opened.png)

## <a name="pin-a-range-of-cells-to-a-dashboard"></a><span data-ttu-id="8578e-130">ปักหมุดช่วงของเซลกับแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="8578e-130">Pin a range of cells to a dashboard</span></span>
<span data-ttu-id="8578e-131">วิธีหนึ่งในการเพิ่ม[ไทล์แดชบอร์ด](../consumer/end-user-tiles.md)ใหม่ นั้นมาจากภายในเวิร์กบุ๊ก Excel ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8578e-131">One way to add a new [dashboard tile](../consumer/end-user-tiles.md) is from within an Excel workbook in Power BI.</span></span> <span data-ttu-id="8578e-132">ช่วงที่ถูกปักหมุดจากเวิร์กบุ๊ก Excel ที่ได้รับการบันทึกใน OneDrive for Business หรือไลบรารีเอกสารที่แชร์กลุ่มอื่น</span><span class="sxs-lookup"><span data-stu-id="8578e-132">Ranges can be pinned from Excel workbooks that have been saved in your OneDrive for Business or another group-shared document library.</span></span> <span data-ttu-id="8578e-133">ช่วงต่าง ๆ สามารถมีข้อมูล แผนภูมิ ตาราง Pivottable PivotCharts และส่วนอื่น ๆ Excel</span><span class="sxs-lookup"><span data-stu-id="8578e-133">The ranges can contain data, charts, tables, PivotTables, PivotCharts, and other Excel parts.</span></span>

1. <span data-ttu-id="8578e-134">การไฮไลท์เซลล์ที่คุณต้องการปักหมุดกับแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="8578e-134">Highlight the cells that you'd like to pin to a dashboard.</span></span>
   
    ![เลือกเซลล์ในเวิร์กบุ๊ก Excel](media/service-dashboard-pin-tile-from-excel/pbi_selectrange.png)
2. <span data-ttu-id="8578e-136">เลือกหมุด</span><span class="sxs-lookup"><span data-stu-id="8578e-136">Select the pin</span></span> ![ปักหมุดไอคอน](media/service-dashboard-pin-tile-from-excel/pbi_pintile_small.png) <span data-ttu-id="8578e-138">icon.</span><span class="sxs-lookup"><span data-stu-id="8578e-138">icon.</span></span> 
3. <span data-ttu-id="8578e-139">ปักหมุดไทล์ลงในแดชบอร์ดที่มีอยู่ หรือแดชบอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="8578e-139">Pin the tile to an existing dashboard or to a new dashboard.</span></span> 
   
   * <span data-ttu-id="8578e-140">แดชบอร์ดที่มีอยู่: เลือกชื่อของแดชบอร์ดจากรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="8578e-140">Existing dashboard: select the name of the dashboard from the dropdown.</span></span>
   * <span data-ttu-id="8578e-141">แดชบอร์ดใหม่ พิมพ์ชื่อของแดชบอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="8578e-141">New dashboard: type the name of the new dashboard.</span></span>
   
     ![ปักหมุดไปยังแดชบอร์ด](media/service-dashboard-pin-tile-from-excel/pbi_dashdialog1.png)
4. <span data-ttu-id="8578e-143">เลือก **หมุด**</span><span class="sxs-lookup"><span data-stu-id="8578e-143">Select **Pin**.</span></span> <span data-ttu-id="8578e-144">ข้อความว่าสำเร็จแล้ว (ใกล้กับมุมบนขวา) ช่วยให้คุณทราบว่า การช่วงถูกเพิ่ม เป็นไทล์ ลงในแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="8578e-144">A Success message (near the top right corner) lets you know the range was added, as a tile, to your dashboard.</span></span> 
   
    ![ได้ปักหมุดกล่องโต้ตอบแดชบอร์ด](media/service-dashboard-pin-tile-from-excel/power-bi-go-to-dashboard.png)
5. <span data-ttu-id="8578e-146">เลือก **ไปยังแดชบอร์ด**</span><span class="sxs-lookup"><span data-stu-id="8578e-146">Select **Go to dashboard**.</span></span> <span data-ttu-id="8578e-147">จากที่นี่ คุณสามารถ[เปลี่ยนชื่อ ปรับขนาด ลิงก์ และย้าย](service-dashboard-edit-tile.md)การแสดงภาพที่ปักหมุดไว้ได้</span><span class="sxs-lookup"><span data-stu-id="8578e-147">From here you can [rename, resize, link, and move](service-dashboard-edit-tile.md) the pinned visualization.</span></span> <span data-ttu-id="8578e-148">ตามค่าเริ่มต้น การเลือกไทล์ที่ปักหมุดไว้นั้นเปิดสมุดงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8578e-148">By default, selecting the pinned tile opens the workbook in Power BI.</span></span>

## <a name="pin-an-entire-table-or-pivottable-to-a-dashboard"></a><span data-ttu-id="8578e-149">ปักหมุดทั้งตารางหรือ PivotTable ไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="8578e-149">Pin an entire table or PivotTable to a dashboard</span></span>
<span data-ttu-id="8578e-150">ทำตามขั้นตอนข้างบน ยกเว้นแทนที่จะเลือกช่วงของเซลล์ เลือกทั้งตารางหรือ PivotTable</span><span class="sxs-lookup"><span data-stu-id="8578e-150">Follow the steps above except instead of selecting a range of cells, select an entire table or PivotTable.</span></span>

<span data-ttu-id="8578e-151">เพื่อปักหมุดตาราง ให้เลือกช่วงทั้งหมดของตารางและอย่าลืมรวมส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="8578e-151">To pin a table, select the entire range of the table and be sure to include the headers.</span></span>  <span data-ttu-id="8578e-152">เพื่อปักหมุด PivotTable ตรวจสอบให้แน่ใจว่าได้รวมทุกส่วนที่มองเห็นได้ของ PivotTable รวมถึงตัวกรอง ถ้าใช้</span><span class="sxs-lookup"><span data-stu-id="8578e-152">To pin a PivotTable, be sure to include every visible part of the PivotTable, including filters if used.</span></span>

 ![เลือกเซลล์](media/service-dashboard-pin-tile-from-excel/pbi_selecttable.png)

<span data-ttu-id="8578e-154">ไทล์ที่สร้างขึ้นจากตารางหรือ PivotTable จะแสดงทั้งตาราง</span><span class="sxs-lookup"><span data-stu-id="8578e-154">A tile created from a table or PivotTable will show the entire table.</span></span>  <span data-ttu-id="8578e-155">ถ้าคุณเพิ่ม/ลบ/ตัวกรองแถวหรือคอลัมน์ในเวิร์กบุ๊กเดิม พวกมันจะเพิ่ม/ลบ/ถูกกรองในไทล์</span><span class="sxs-lookup"><span data-stu-id="8578e-155">If you add/remove/filter rows or columns in the original workbook, they will also be added/removed/filtered in the tile.</span></span>

## <a name="view-the-workbook-linked-to-the-tile"></a><span data-ttu-id="8578e-156">ดูสมุดงานที่เชื่อมโยงกับไทล์</span><span class="sxs-lookup"><span data-stu-id="8578e-156">View the workbook linked to the tile</span></span>
<span data-ttu-id="8578e-157">การเลือกไทล์เวิร์กบุ๊กได้เปิดเวิร์กบุ๊กที่ลิงก์ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8578e-157">Selecting a workbook tile opens the linked workbook in Power BI.</span></span> <span data-ttu-id="8578e-158">เนื่องจากไฟล์เวิร์กบุ๊กอยู่บน OneDrive ของเจ้าของ OneDrive for Business การดูเวิร์กบุ๊กจำเป็นต้องมีสิทธิ์การอ่านเวิร์กบุ๊ก</span><span class="sxs-lookup"><span data-stu-id="8578e-158">Since the workbook file is located on the owner’s OneDrive for Business, viewing the workbook requires you have Read permissions for the workbook.</span></span> <span data-ttu-id="8578e-159">ถ้าคุณไม่มีสิทธิ์ คุณจะได้รับข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="8578e-159">If you do not have permission, you will receive an error message.</span></span>  

 ![video](media/service-dashboard-pin-tile-from-excel/pin-from-excel.gif)

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="8578e-161">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="8578e-161">Considerations and troubleshooting</span></span>
<span data-ttu-id="8578e-162">ฟีเจอร์ที่ไม่รองรับ Power BI ใช้ Excel Services เพื่อรับไทล์ของเวิร์กบุ๊ก</span><span class="sxs-lookup"><span data-stu-id="8578e-162">Unsupported features: Power BI uses Excel Services to retrieve the workbook tiles.</span></span> <span data-ttu-id="8578e-163">ดังนั้น เนื่องจากฟีเจอร์บางอย่างจาก Excel ไม่รองรับ Excel Services REST API มันจะมองไม่เห็นบนไทล์ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8578e-163">Therefore, since some features from Excel are not supported in Excel Services REST API, they will not be seen on tiles in Power BI.</span></span> <span data-ttu-id="8578e-164">ตัวอย่างเช่น เส้นแบบประกายไฟ ไอคอนการตั้งค่าการจัดรูปแบบตามเงื่อนไข และตัวแบ่งส่วนข้อมูลเวลา</span><span class="sxs-lookup"><span data-stu-id="8578e-164">For example: Sparklines, icon set conditional formatting, and time slicers.</span></span> <span data-ttu-id="8578e-165">สำหรับรายการทั้งหมดของฟีเจอร์ไม่รองรับ ให้ดู[ฟีเจอร์ที่ไม่รองรับใน Excel Services REST API](/sharepoint/dev/general-development/unsupported-features-in-excel-services-rest-api)</span><span class="sxs-lookup"><span data-stu-id="8578e-165">For a full list of unsupported features see [Unsupported Features in Excel Services REST API](/sharepoint/dev/general-development/unsupported-features-in-excel-services-rest-api)</span></span>

## <a name="next-steps"></a><span data-ttu-id="8578e-166">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="8578e-166">Next steps</span></span>
[<span data-ttu-id="8578e-167">แชร์แดชบอร์ดที่เชื่อมโยงไปยังเวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="8578e-167">Share a dashboard that has links to an Excel workbook</span></span>](../collaborate-share/service-share-dashboard-that-links-to-excel-onedrive.md)

[<span data-ttu-id="8578e-168">รับข้อมูลจากเวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="8578e-168">Get data from Excel workbooks</span></span>](../connect-data/service-excel-workbook-files.md)

<span data-ttu-id="8578e-169">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8578e-169">More questions?</span></span> [<span data-ttu-id="8578e-170">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="8578e-170">Try the Power BI Community</span></span>](https://community.powerbi.com/)
