---
title: เชื่อมต่อกับไฟล์ CSV ใน Power BI Desktop
description: เชื่อมต่อและใช้ข้อมูลไฟล์ CSV ใน Power BI Desktop ได้อย่างง่ายดาย
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 08/29/2019
LocalizationGroup: Connect to data
ms.openlocfilehash: 3bb37d4ba3b3ca7d5fec3f8577b971432f5a9d0f
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411390"
---
# <a name="connect-to-csv-files-in-power-bi-desktop"></a><span data-ttu-id="a525f-103">เชื่อมต่อกับไฟล์ CSV ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a525f-103">Connect to CSV files in Power BI Desktop</span></span>
<span data-ttu-id="a525f-104">การเชื่อมต่อกับแฟ้มที่ใช้จุลภาคเป็นตัวคั่น (*CSV*) จาก Power BI Desktop เหมือนการเชื่อมต่อกับเวิร์กบุ๊ก Excel มาก</span><span class="sxs-lookup"><span data-stu-id="a525f-104">Connecting to a comma-separated value (*CSV*) file from Power BI Desktop is a lot like connecting to an Excel workbook.</span></span> <span data-ttu-id="a525f-105">ทั้งสองเป็นเรื่องง่าย และบทความนี้จะพาคุณไปตามขั้นตอน วิธีการเชื่อมต่อกับไฟล์ CSV ใด ๆ ที่คุณสามารถเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="a525f-105">Both are easy, and this article steps you through how to connect to any CSV file to which you have access.</span></span>

<span data-ttu-id="a525f-106">เริ่มต้นจากใน Power BI Desktop เลือก **รับข้อมูล > CSV** จาก ribbon **หน้าแรก**</span><span class="sxs-lookup"><span data-stu-id="a525f-106">To start with, from Power BI Desktop select **Get Data > CSV** from the **Home** ribbon.</span></span>

![ภภาพหน้าจอของเมนูรับข้อมูล](media/desktop-connect-csv/connect-to-csv_1.png)

<span data-ttu-id="a525f-108">เลือกไฟล์ CSV ของคุณจากกล่องโต้ตอบ **เปิด** ที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="a525f-108">Select your CSV file from the **Open** dialog that appears.</span></span>

![ภาพหน้าจอของกล่องโต้ตอบเปิด](media/desktop-connect-csv/connect-to-csv_2.png)

<span data-ttu-id="a525f-110">เมื่อคุณเลือก **เปิด** Power BI Desktop จะเข้าถึงไฟล์ และพิจารณาไฟล์แอตทริบิวต์บางตัว เช่นที่มาของไฟล์ ชนิดตัวคั่น และจำนวนแถวที่ควรใช้เพื่อตรวจสอบชนิดข้อมูลในไฟล์</span><span class="sxs-lookup"><span data-stu-id="a525f-110">When you select **Open**, Power BI Desktop accesses the file and determines certain file attributes, such as the file origin, delimiter type, and how many rows should be used to detect the data types in the file.</span></span>

<span data-ttu-id="a525f-111">แอตทริบิวต์และตัวเลือกของไฟล์เหล่านี้ จะแสดงในรายการดรอปดาวน์ด้านบนของหน้าต่างกล่องโต้ตอบ **การนำเข้า CSV** ดังแสดงด้านล่างนี้</span><span class="sxs-lookup"><span data-stu-id="a525f-111">These file attributes and options are shown in the drop-down selections at the top of the **CSV import** dialog window, shown below.</span></span> <span data-ttu-id="a525f-112">คุณสามารถเปลี่ยนการตั้งค่าที่ตรวจพบเหล่านี้ด้วยตนเอง โดยการเลือกตัวเลือกอื่นจากรายการดรอปดาวน์ได้</span><span class="sxs-lookup"><span data-stu-id="a525f-112">You can change any of these detected settings manually, by choosing another option from any of the drop-down selectors.</span></span>

![ภาพหน้าจอของหน้าต่างกล่องโต้ตอบการนำเข้า C S V](media/desktop-connect-csv/connect-to-csv_3.png)

<span data-ttu-id="a525f-114">เมื่อคุณพอใจกับการเลือก คุณสามารถเลือก **โหลด** เพื่อการนำเข้าไฟล์ไปยัง Power BI Desktop หรือคุณสามารถเลือก **แก้ไข** เพื่อเปิด **ตัวแก้ไขคิวรี** และจัดรูปทรงหรือแปลงข้อมูลเพิ่มเติม ก่อนที่จะนำเข้า</span><span class="sxs-lookup"><span data-stu-id="a525f-114">When you’re satisfied with the selections, you can select **Load** to import the file into Power BI Desktop, or you can select **Edit** to open **Query Editor** and further shape or transform the data before importing it.</span></span>

<span data-ttu-id="a525f-115">เมื่อคุณโหลดข้อมูลลงใน Power BI Desktop แล้ว คุณจะเห็นตารางและคอลัมน์ (ซึ่งจะแสดงเป็นเขตข้อมูลใน Power BI Desktop) ในบานหน้าต่าง **เขตข้อมูล** ทางด้านขวาของมุมมองรายงานใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a525f-115">Once you load the data into Power BI Desktop, you see the table and its columns (which are presented as Fields in Power BI Desktop) in the **Fields** pane, along the right of the Report view in Power BI Desktop.</span></span>

![ภาพหน้าจอของหน้าต่าง Power B I Desktop ที่แสดงบานหน้าต่างเขตข้อมูล](media/desktop-connect-csv/connect-to-csv_4.png)

<span data-ttu-id="a525f-117">นั่นคือทั้งหมดที่คุณต้องทำ – ข้อมูลจากไฟล์ CSV ของคุณในขณะนี้ อยู่ใน Power BI Desktop เรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="a525f-117">That’s all you have to do – the data from your CSV file is now in Power BI Desktop.</span></span>

<span data-ttu-id="a525f-118">คุณสามารถใช้ข้อมูลดังกล่าวใน Power BI Desktop เพื่อสร้างวิชวล รายงาน หรือโต้ตอบกับข้อมูลอื่น ๆ ที่คุณอาจต้องการเชื่อมต่อและนำเข้า เช่น เวิร์กบุ๊ก Excel, ฐานข้อมูล หรือแหล่งข้อมูลอื่น</span><span class="sxs-lookup"><span data-stu-id="a525f-118">You can use that data in Power BI Desktop to create visuals, reports, or interact with any other data you might want to connect with and import, such as Excel workbooks, databases, or any other data source.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a525f-119">เมื่อคุณนำเข้าไฟล์ CSV, Power BI Desktop จะสร้าง *คอลัมน์ = x* (โดยที่ *x* คือจำนวนคอลัมน์ในไฟล์ CSV ในระหว่างการนำเข้าเริ่มต้น) เป็นขั้นตอนในตัวแก้ไข Power Query</span><span class="sxs-lookup"><span data-stu-id="a525f-119">When you import a CSV file, Power BI Desktop generates a *columns=x* (where *x* is the number of columns in the CSV file during initial import) as a step in Power Query Editor.</span></span> <span data-ttu-id="a525f-120">หากคุณเพิ่มคอลัมน์เพิ่มเติมในภายหลังและแหล่งข้อมูลถูกตั้งค่าให้รีเฟรช คอลัมน์ใด ๆ ที่เกินจำนวนคอลัมน์ *x* เริ่มต้น จะไม่รีเฟรช</span><span class="sxs-lookup"><span data-stu-id="a525f-120">If you subsequently add more columns and the data source is set to refresh, any columns beyond the initial *x* count of columns are not refreshed.</span></span> 


## <a name="next-steps"></a><span data-ttu-id="a525f-121">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a525f-121">Next steps</span></span>
<span data-ttu-id="a525f-122">มีข้อมูลหลากหลายประเภทที่คุณสามารถเชื่อมต่อโดยใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a525f-122">There are all sorts of data you can connect to using Power BI Desktop.</span></span> <span data-ttu-id="a525f-123">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแหล่งข้อมูล โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a525f-123">For more information on data sources, check out the following resources:</span></span>

* [<span data-ttu-id="a525f-124">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="a525f-124">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="a525f-125">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a525f-125">Data Sources in Power BI Desktop</span></span>](desktop-data-sources.md)
* [<span data-ttu-id="a525f-126">จัดรูปทรงและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a525f-126">Shape and Combine Data with Power BI Desktop</span></span>](desktop-shape-and-combine-data.md)
* [<span data-ttu-id="a525f-127">เชื่อมต่อกับเวิร์กบุ๊ก Excel ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a525f-127">Connect to Excel workbooks in Power BI Desktop</span></span>](desktop-connect-excel.md)   
* [<span data-ttu-id="a525f-128">ป้อนข้อมูลลงใน Power BI Desktop โดยตรง</span><span class="sxs-lookup"><span data-stu-id="a525f-128">Enter data directly into Power BI Desktop</span></span>](desktop-enter-data-directly-into-desktop.md)   
