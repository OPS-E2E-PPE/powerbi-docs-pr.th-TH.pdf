---
title: เชื่อมต่อไปยัง Excel ใน Power BI Desktop
description: เชื่อมต่อและใช้ข้อมูลในเวิร์กบุ๊ก Excel ใน Power BI Desktop ได้อย่างง่ายดาย
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 01/04/2021
LocalizationGroup: Connect to data
ms.openlocfilehash: 7ba25ff8b4462d2cf50f9285b3d9ac92b98373cf
ms.sourcegitcommit: 932f6856849c39e34229dc9a49fb9379c56a888a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/06/2021
ms.locfileid: "97927037"
---
# <a name="connect-to-excel-in-power-bi-desktop"></a><span data-ttu-id="a3a40-103">เชื่อมต่อไปยัง Excel ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a3a40-103">Connect to Excel in Power BI Desktop</span></span>
<span data-ttu-id="a3a40-104">การเชื่อมต่อกับเวิร์กบุ๊ก Excel จาก Power BI Desktop เป็นเรื่องตรงไปตรงมา และบทความนี้จะแนะนำทีละขั้นตอนให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="a3a40-104">Connecting to an Excel workbook from Power BI Desktop is straightforward, and this article walks you through the steps.</span></span>

<span data-ttu-id="a3a40-105">ใน Power BI Desktop เลือก **รับข้อมูล > Excel** จาก ribbon **หน้าแรก**</span><span class="sxs-lookup"><span data-stu-id="a3a40-105">In Power BI Desktop, select **Get Data > Excel** from the **Home** ribbon.</span></span>

![ภาพหน้าจอของตัวเลือก Excel](media/desktop-connect-excel/connect_to_excel_1.png)

<span data-ttu-id="a3a40-107">เลือกเวิร์กบุ๊กของคุณในกล่องโต้ตอบ **เปิด** ที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="a3a40-107">Select your workbook from the **Open** dialog that appears.</span></span>
<span data-ttu-id="a3a40-108">![ภาพหน้าจอของกล่องโต้ตอบเปิด](media/desktop-connect-excel/connect_to_excel_2.png)</span><span class="sxs-lookup"><span data-stu-id="a3a40-108">![Screenshot of the Open dialog.](media/desktop-connect-excel/connect_to_excel_2.png)</span></span>

<span data-ttu-id="a3a40-109">Power BI Desktop แสดงตารางของข้อมูลอื่น ๆ จากเวิร์กบุ๊กในหน้าต่าง **ตัวนำทาง**</span><span class="sxs-lookup"><span data-stu-id="a3a40-109">Power BI Desktop presents the tables on other data elements from the workbook in the **Navigator** window.</span></span> <span data-ttu-id="a3a40-110">เมื่อคุณเลือกตารางในบานหน้าต่างด้านซ้าย ตัวอย่างของข้อมูลจะปรากฏในบานหน้าต่างด้านขวา</span><span class="sxs-lookup"><span data-stu-id="a3a40-110">When you select a table in the left pane, a preview of the data appears in the right pane.</span></span>

![ภาพหน้าจอของหน้าต่างตัวนำทาง](media/desktop-connect-excel/connect_to_excel_3.png)

<span data-ttu-id="a3a40-112">คุณสามารถเลือกปุ่มโหลดเพื่อนำเข้าข้อมูล หรือ ถ้าคุณต้องการแก้ไขข้อมูลโดยใช้ **ตัวแก้ไขคิวรี** ก่อนที่นำเข้าไปใน Power BI Desktop เลือกปุ่ม **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="a3a40-112">You can select the Load button to import the data, or if you want to edit the data using **Query Editor** before bringing it into Power BI Desktop, select the **Edit** button.</span></span>

<span data-ttu-id="a3a40-113">เมื่อคุณโหลดข้อมูล Power BI Desktop แสดงหน้าต่าง **โหลด** และกิจกรรมที่เกี่ยวข้องกับการโหลดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a3a40-113">When you load the data, Power BI Desktop displays the **Load** window and displays the activity associated with loading the data.</span></span>  

![ภาพหน้าจอของหน้าต่างโหลด](media/desktop-connect-excel/connect_to_excel_4.png)

<span data-ttu-id="a3a40-115">เมื่อโหลดเสร็จ Power BI Desktop จะแสดงตารางและเขตข้อมูลที่ได้นำเข้าจากเวิร์กบุ๊ก Excel ของคุณในบานหน้าต่าง **เขตข้อมูล** ทางด้านขวาของเดสก์ท็อป</span><span class="sxs-lookup"><span data-stu-id="a3a40-115">When complete, Power BI Desktop displays the tables and fields it imported from your Excel workbook in the **Fields** pane, on the right side of the Desktop.</span></span>

![ภาพหน้าจอของบานหน้าต่างเขตข้อมูล](media/desktop-connect-excel/connect_to_excel_5.png)

<span data-ttu-id="a3a40-117">เท่านี้ก็เรียบร้อย!</span><span class="sxs-lookup"><span data-stu-id="a3a40-117">And that’s it!</span></span>

<span data-ttu-id="a3a40-118">ตอนนี้คุณพร้อมที่จะใช้ข้อมูลนำเข้าจากเวิร์กบุ๊ก Excel ของคุณใน Power BI Desktop เพื่อสร้างวิชวล รายงาน หรือโต้ตอบกับข้อมูลอื่น ๆ ที่คุณอาจต้องการเชื่อมต่อ และนำเข้า เช่นเวิร์กบุ๊ก Excel อื่นๆ ฐานข้อมูล หรือแหล่งข้อมูลอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="a3a40-118">You’re now ready to use the imported data from your Excel workbook in Power BI Desktop to create visuals, reports, or interact with any other data you might want to connect with and import, such as other Excel workbooks, databases, or any other data source.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a3a40-119">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a3a40-119">Next steps</span></span>
<span data-ttu-id="a3a40-120">มีข้อมูลหลากหลายประเภทที่คุณสามารถเชื่อมต่อโดยใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a3a40-120">There are all sorts of data you can connect to using Power BI Desktop.</span></span> <span data-ttu-id="a3a40-121">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแหล่งข้อมูล โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a3a40-121">For more information on data sources, check out the following resources:</span></span>

* [<span data-ttu-id="a3a40-122">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="a3a40-122">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="a3a40-123">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a3a40-123">Data Sources in Power BI Desktop</span></span>](desktop-data-sources.md)
* [<span data-ttu-id="a3a40-124">จัดรูปร่างและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a3a40-124">Shape and Combine Data with Power BI Desktop</span></span>](desktop-shape-and-combine-data.md)
* [<span data-ttu-id="a3a40-125">เชื่อมต่อกับไฟล์ CSV ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a3a40-125">Connect to CSV files in Power BI Desktop</span></span>](desktop-connect-csv.md)   
* [<span data-ttu-id="a3a40-126">ใส่ข้อมูลลงใน Power BI Desktop โดยตรง</span><span class="sxs-lookup"><span data-stu-id="a3a40-126">Enter data directly into Power BI Desktop</span></span>](desktop-enter-data-directly-into-desktop.md)   
