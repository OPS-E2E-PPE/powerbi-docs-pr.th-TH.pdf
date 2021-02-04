---
title: เชื่อมต่อกับตัวดึงข้อมูล OData ใน Power BI Desktop
description: เชื่อมต่อและใช้ตัวดึงข้อมูล OData ได้อย่างง่ายดายใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 01/04/2021
LocalizationGroup: Connect to data
ms.openlocfilehash: d1a4e8f7d5a057b51de7284d0db0b2440ccb93df
ms.sourcegitcommit: 932f6856849c39e34229dc9a49fb9379c56a888a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/06/2021
ms.locfileid: "97926433"
---
# <a name="connect-to-odata-feeds-in-power-bi-desktop"></a><span data-ttu-id="38806-103">เชื่อมต่อกับตัวดึงข้อมูล OData ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="38806-103">Connect to OData feeds in Power BI Desktop</span></span>
<span data-ttu-id="38806-104">ใน Power BI Desktop คุณสามารถเชื่อมต่อกับ **ตัวดึงข้อมูล OData** และใช้ข้อมูลเบื้องต้นเช่นเดียวกับแหล่งข้อมูลอื่นใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="38806-104">In Power BI Desktop, you can connect to an **OData feed** and use the underlying data just like any other data source in Power BI Desktop.</span></span>

<span data-ttu-id="38806-105">เมื่อต้องการเชื่อมต่อกับตัวดึงข้อมูล OData เลือก **รับข้อมูล > ตัวดึงข้อมูล OData** จาก Ribbon **หน้าหลัก** ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="38806-105">To connect to an OData feed, select **Get Data > OData Feed** from the **Home** ribbon in Power BI Desktop.</span></span>

![ภาพหน้าจอของริบบอนรับข้อมูลใน Power BI Desktop ที่แสดงการเลือกตัวดึงข้อมูล OData](media/desktop-connect-odata/connect-to-odata_1.png)

<span data-ttu-id="38806-107">ในหน้าต่าง **ตัวดึงข้อมูล OData** ที่ปรากฎขึ้น พิมพ์ หรือวาง URL ของตัวดึงข้อมูล OData ของคุณลงในกล่อง และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="38806-107">In the **OData Feed** window that appears, type or paste your OData feed URL into the box, and select **OK**.</span></span>

![ภาพหน้าจอของกล่องโต้ตอบตัวดึงข้อมูล OData ที่แสดงเขตข้อมูล URL](media/desktop-connect-odata/connect-to-odata_2.png)

<span data-ttu-id="38806-109">Power BI Desktop เชื่อมต่อกับตัวดึงข้อมูล OData และแสดงตารางที่พร้อมใช้งานและองค์ประกอบข้อมูลอื่น ๆ ในหน้าต่าง **ตัวนำทาง**</span><span class="sxs-lookup"><span data-stu-id="38806-109">Power BI Desktop connects to the OData feed, and displays the available tables and other data elements in the **Navigator** window.</span></span> <span data-ttu-id="38806-110">เมื่อคุณเลือกหนึ่งองค์ประกอบ พื้นที่ด้านขวาของหน้าต่าง **ตัวนำทาง** จะแสดงตัวอย่างของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="38806-110">When you select an element, the right pane of the **Navigator** window displays a preview of the data.</span></span> <span data-ttu-id="38806-111">คุณสามารถเลือกตารางต่าง ๆ ได้มากเท่าที่คุณต้องการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="38806-111">You can select as many tables as you want to import.</span></span> <span data-ttu-id="38806-112">หน้าต่าง **ตัวนำทาง** จะแสดงตัวอย่างของตารางที่เลือกในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="38806-112">The **Navigator** window shows a preview of the currently selected table.</span></span>

![ภาพหน้าจอของกล่องโต้ตอบตัวนำทาง ที่แสดงตัวอย่างของข้อมูลของตารางที่เลือก](media/desktop-connect-odata/connect-to-odata_3.png)

<span data-ttu-id="38806-114">คุณสามารถเลือกปุ่ม **แก้ไข** ซึ่งจะเปิด **ตัวแก้ไขแบบสอบถาม** ขึ้นมา ในหน้าต่างนี้คุณจะสามารถจัดการรูปร่างและเปลี่ยนแปลงข้อมูลจากตัวดึงข้อมูล OData ได้ ก่อนที่จะนำเข้าข้อมูลไปยัง Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="38806-114">You can choose the **Edit** button, which launches **Query Editor**, where you can shape and transform the data from the OData feed before importing it into Power BI Desktop.</span></span> <span data-ttu-id="38806-115">หรือคุณสามารถเลือกปุ่ม **โหลด** และนำเข้าองค์ประกอบข้อมูลทั้งหมดที่คุณได้เลือกในช่องแสดงข้อมูลด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="38806-115">Or you can select the **Load** button, and import all of the data elements you selected in the left pane.</span></span>

<span data-ttu-id="38806-116">เมื่อเราเลือก **การโหลด** Power BI Desktop จะนำเข้ารายการที่เลือกไว้และแสดงหน้าต่าง **การโหลด** ของความคืบหน้าการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="38806-116">When we select **Load**, Power BI Desktop imports the selected items, and displays a **Load** window of the import progress.</span></span>

![ภาพหน้าจอของกล่องโต้ตอบการโหลด ที่แสดงความคืบหน้าการนำเข้า](media/desktop-connect-odata/connect-to-odata_4.png)

<span data-ttu-id="38806-118">เมื่อเสร็จสมบูรณ์ Power BI Desktop จะทำตารางที่เลือกและองค์ประกอบข้อมูลอื่น ๆ ที่พร้อมใช้งานในพื้นที่ **ช่องข้อมูล** ที่พบบนด้านขวาของตัวมุมมอง *รายงาน* ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="38806-118">Once complete, Power BI Desktop makes the selected tables and other data elements available in the **Fields** pane, found on the right side of the *Reports* view in Power BI Desktop.</span></span>

![ภาพหน้าจอของบานหน้าต่างเขตข้อมูล ที่แสดงรายการของตารางที่เลือก](media/desktop-connect-odata/connect-to-odata_5.png)

<span data-ttu-id="38806-120">เท่านี้ก็เรียบร้อย!</span><span class="sxs-lookup"><span data-stu-id="38806-120">And that’s it!</span></span>

<span data-ttu-id="38806-121">ตอนนี้คุณพร้อมที่จะใช้ข้อมูลที่นำเข้าจากตัวดึงข้อมูล OData ใน Power BI Desktop เพื่อสร้างภาพ รายงาน หรือโต้ตอบกับข้อมูลอื่น ๆ ที่คุณอาจต้องการเชื่อมโยงและต้องการนำเข้า เช่น สมุดงาน Excel อื่น ๆ ฐานข้อมูล หรือแหล่งข้อมูลอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="38806-121">You’re now ready to use the imported data from the OData feed in Power BI Desktop to create visuals, reports, or interact with any other data you might want to connect with and import, such as other Excel workbooks, databases, or any other data source.</span></span>

## <a name="next-steps"></a><span data-ttu-id="38806-122">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="38806-122">Next steps</span></span>
<span data-ttu-id="38806-123">มีข้อมูลหลากหลายประเภทที่คุณสามารถเชื่อมต่อโดยใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="38806-123">There are all sorts of data you can connect to using Power BI Desktop.</span></span> <span data-ttu-id="38806-124">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแหล่งข้อมูล โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="38806-124">For more information on data sources, check out the following resources:</span></span>

* [<span data-ttu-id="38806-125">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="38806-125">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="38806-126">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="38806-126">Data Sources in Power BI Desktop</span></span>](desktop-data-sources.md)
* [<span data-ttu-id="38806-127">จัดรูปทรงและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="38806-127">Shape and Combine Data with Power BI Desktop</span></span>](desktop-shape-and-combine-data.md)
* [<span data-ttu-id="38806-128">เชื่อมต่อกับเวิร์กบุ๊ก Excel ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="38806-128">Connect to Excel workbooks in Power BI Desktop</span></span>](desktop-connect-excel.md)   
* [<span data-ttu-id="38806-129">ป้อนข้อมูลลงใน Power BI Desktop โดยตรง</span><span class="sxs-lookup"><span data-stu-id="38806-129">Enter data directly into Power BI Desktop</span></span>](desktop-enter-data-directly-into-desktop.md)   
