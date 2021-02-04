---
title: เชื่อมต่อหน้าเว็บจาก Power BI Desktop
description: เชื่อมต่อและใช้งานข้อมูลบนหน้าเว็บได้อย่างง่ายดายใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 05/08/2019
LocalizationGroup: Connect to data
ms.openlocfilehash: 0b66c069daedeb714fad3545d61f9cde8f2271da
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411275"
---
# <a name="connect-to-webpages-from-power-bi-desktop"></a><span data-ttu-id="06dc4-103">เชื่อมต่อหน้าเว็บจาก Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="06dc4-103">Connect to webpages from Power BI Desktop</span></span>

<span data-ttu-id="06dc4-104">คุณสามารถเชื่อมต่อกับหน้าเว็บและนำเข้าข้อมูลไปยัง Power BI Desktop สำหรับใช้ในวิชวลและแบบจำลองข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="06dc4-104">You can connect to a webpage and import its data into Power BI Desktop, to use in your visuals and in your data models.</span></span>

<span data-ttu-id="06dc4-105">ใน Power BI Desktop เลือก **รับข้อมูล > เว็บ** จาก **หน้าหลัก** แถบข้อมูล ribbon</span><span class="sxs-lookup"><span data-stu-id="06dc4-105">In Power BI Desktop, select **Get Data > Web** from the **Home** ribbon.</span></span>

![ภาพหน้าจอของ Power BI Desktop ที่แสดงการเลือกเว็บ](media/desktop-connect-to-web/connect-to-web-01.png)

<span data-ttu-id="06dc4-107">ข้อความจะปรากฏขึ้นมาเพื่อถามถึง URL ของหน้าเว็บที่คุณต้องการนำเข้าข้อมูล</span><span class="sxs-lookup"><span data-stu-id="06dc4-107">A dialog appears, asking for the URL of the web page from which you want to import data.</span></span>

![ภาพหน้าจอของกล่องโต้ตอบเว็บ ที่แสดงเขตข้อมูล URL](media/desktop-connect-to-web/connect-to-web-02.png)

<span data-ttu-id="06dc4-109">เมื่อคุณพิมพ์ (หรือวาง) URL ลงไปแล้ว ให้เลือก **OK**</span><span class="sxs-lookup"><span data-stu-id="06dc4-109">Once you’ve typed in (or pasted) the URL, select **OK**.</span></span> <span data-ttu-id="06dc4-110">Power BI Desktop จะพร้อมท์แจ้งให้คุณระบุวิธีที่คุณต้องการเข้าถึงเนื้อหาเว็บ</span><span class="sxs-lookup"><span data-stu-id="06dc4-110">Power BI Desktop prompts you to specify how you want to access the web content.</span></span>

![ข้อมูลประจำตัวที่จะใช้เมื่อเชื่อมต่อกับเว็บ](media/desktop-connect-to-web/connect-to-web-03.png)

<span data-ttu-id="06dc4-112">Power BI Desktop เชื่อมต่อกับเว็บเพจ จากนั้นจะแสดงข้อมูลที่มีอยู่ในหน้านั้นในหน้าต่าง **ตัวนำทาง**</span><span class="sxs-lookup"><span data-stu-id="06dc4-112">Power BI Desktop connects to the web page and then presents the page’s available data in the **Navigator** window.</span></span> <span data-ttu-id="06dc4-113">เมื่อคุณเลือกหนึ่งในองค์ประกอบข้อมูลที่มีอยู่ เช่น ตารางของหน้านั้นทั้งหน้า **หน้าต่าง** นำทาง จะแสดงตัวอย่างของข้อมูลนั้น ๆ อยู่ทางด้านขวาของหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="06dc4-113">When you select one of the available data elements, such as a table of the entire page, the **Navigator** window displays a preview of that data on the right side of the window.</span></span>

![ภาพหน้าจอของกล่องโต้ตอบตัวนำทาง ที่แสดงตัวอย่างของข้อมูลของตารางที่เลือกไว้](media/desktop-connect-to-web/connect-to-web-04.png)

<span data-ttu-id="06dc4-115">คุณสามารถเลือกปุ่ม **แปลงข้อมูล** ซึ่งจะเปิด **Query Editor** ออกมา ซึ่งในหน้าต่างนี้คุณจะสามารถจัดการรูปร่าง และเปลี่ยนแปลงข้อมูลบนหน้าเว็บได้ ก่อนที่จะนำเข้าข้อมูลไปยัง Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="06dc4-115">You can choose the **Transform Data** button, which launches **Query Editor**, where you can shape and transform the data on that Web page before importing it into Power BI Desktop.</span></span> <span data-ttu-id="06dc4-116">หรือคุณสามารถเลือก **ปุ่ม** โหลด และนำเข้าองค์ประกอบข้อมูลทั้งหมดที่คุณเลือกในช่องแสดงข้อมูลด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="06dc4-116">Or you can select the **Load** button, and import all of the data elements you selected in the left pane.</span></span>

<span data-ttu-id="06dc4-117">เมื่อเราเลือก **โหลด** Power BI Desktop จะทำการนำเข้ารายการที่เลือก และทำให้ไฟล์นั้นพร้อมใช้งานใน **ช่อง** เขตข้อมูล ซึ่งอยู่ทางด้านขวาของมุมมองรายงานใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="06dc4-117">When we select **Load**, Power BI Desktop imports the selected items, and makes them available in the **Fields** pane, found on the right side of the Reports view in Power BI Desktop.</span></span>

![ภาพหน้าจอของบานหน้าต่างเขตข้อมูล ที่แสดงรายการของตารางที่เลือกไว้](media/desktop-connect-to-web/connect-to-web-05.png)

<span data-ttu-id="06dc4-119">การเชื่อมต่อเว็บเพจ และนำเข้าข้อมูลลงใน Power BI Desktop มีขั้นตอนเพียงเท่านี้</span><span class="sxs-lookup"><span data-stu-id="06dc4-119">That’s all there is to connecting to a web page and bringing its data into Power BI Desktop.</span></span>

<span data-ttu-id="06dc4-120">จากตรงนี้ คุณสามารถลากเขตข้อมูลเหล่านั้นลงในพื้นที่รายงาน และสร้างการแสดงภาพที่คุณต้องการทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="06dc4-120">From there, you can drag those fields onto the Report canvas and create all the visualizations you want.</span></span> <span data-ttu-id="06dc4-121">คุณยังสามารถใช้ข้อมูลจากหน้าเว็บนั้นได้แบบเดียวที่คุณใช้กับข้อมูลอื่น ๆ กล่าวคือ คุณสามารถสร้างรูปร่าง สร้างความสัมพันธ์ระหว่างข้อมูลเหล่านั้นและแหล่งข้อมูลอื่น ๆ ในโมเดลของคุณ และอีกเรื่องคือคุณสามารถทำทุกอย่างที่คุณต้องการเพื่อสร้างรายงาน Power BI ตามแบบที่ต้องการได้</span><span class="sxs-lookup"><span data-stu-id="06dc4-121">You can also use the data from that Web page just like you would any other data – you can shape it, you can create relationships between it and other data sources in your model, and otherwise do what you’d like to create the Power BI report you want.</span></span>

<span data-ttu-id="06dc4-122">เมื่อต้องการดูการเชื่อมต่อหน้าเว็บในเชิงลึกและดูการเคลื่อนไหวเพิ่มขึ้น ให้ดูที่[คำแนะนำการเริ่มต้นใช้งาน Power BI Desktop](../fundamentals/desktop-getting-started.md)</span><span class="sxs-lookup"><span data-stu-id="06dc4-122">To see connecting to a Web page in more depth and action, take a look at the [Power BI Desktop Getting Started Guide](../fundamentals/desktop-getting-started.md).</span></span>

## <a name="certificate-revocation-check"></a><span data-ttu-id="06dc4-123">การตรวจสอบการเพิกถอนใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="06dc4-123">Certificate revocation check</span></span>

<span data-ttu-id="06dc4-124">Power BI ใช้การรักษาความปลอดภัยสำหรับการเชื่อมต่อเว็บเพื่อปกป้องข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="06dc4-124">Power BI applies security for web connections to protect your data.</span></span> <span data-ttu-id="06dc4-125">ในบางสถานการณ์เช่นการรวบรวมคำขอเว็บด้วย Fiddler การเชื่อมต่อเว็บอาจทำงานไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="06dc4-125">In some scenarios, such as capturing web requests with Fiddler, web connections may not work properly.</span></span> <span data-ttu-id="06dc4-126">เมื่อต้องการเปิดใช้งานสถานการณ์ดังกล่าว คุณสามารถยกเลิกการเลือกตัวเลือก **เปิดใช้งานการตรวจสอบการเพิกถอนใบรับรอง** ใน Power BI Desktop จากนั้นรีสตาร์ต Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="06dc4-126">To enable such scenarios, you can uncheck the **Enable certificate revocation check** option in Power BI Desktop, then restart Power BI Desktop.</span></span> 

<span data-ttu-id="06dc4-127">ให้เลือก **ไฟล์ > ตัวเลือก** จากนั้นเลือก **การรักษาความปลอดภัย** ในบานหน้าต่างด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="06dc4-127">To change this option, select **File > Options**, then select **Security** in the left pane.</span></span> <span data-ttu-id="06dc4-128">ภาพต่อไปนี้แสดงช่องทำเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="06dc4-128">The following image shows the checkbox.</span></span> <span data-ttu-id="06dc4-129">การยกเลิกการเลือกช่องนี้จะทำให้การเชื่อมต่อเว็บมีความปลอดภัยน้อยลง</span><span class="sxs-lookup"><span data-stu-id="06dc4-129">Unchecking the box will make web connections less secure.</span></span> 

![เปิดหรือปิดใช้งานการตรวจสอบการเพิกถอนใบรับรอง](media/desktop-connect-to-web/connect-to-web-06.png)


## <a name="next-steps"></a><span data-ttu-id="06dc4-131">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="06dc4-131">Next steps</span></span>
<span data-ttu-id="06dc4-132">มีข้อมูลหลากหลายประเภทที่คุณสามารถเชื่อมต่อโดยใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="06dc4-132">There are all sorts of data you can connect to using Power BI Desktop.</span></span> <span data-ttu-id="06dc4-133">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแหล่งข้อมูล กรุณาตรวจดูแหล่งที่มาต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="06dc4-133">For more information on data sources, check out the following resources:</span></span>

* [<span data-ttu-id="06dc4-134">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="06dc4-134">Data Sources in Power BI Desktop</span></span>](desktop-data-sources.md)
* [<span data-ttu-id="06dc4-135">จัดรูปทรงและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="06dc4-135">Shape and Combine Data with Power BI Desktop</span></span>](desktop-shape-and-combine-data.md)
* [<span data-ttu-id="06dc4-136">เชื่อมต่อกับเวิร์กบุ๊ก Excel ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="06dc4-136">Connect to Excel workbooks in Power BI Desktop</span></span>](desktop-connect-excel.md)   
* [<span data-ttu-id="06dc4-137">เชื่อมต่อกับไฟล์ CSV ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="06dc4-137">Connect to CSV files in Power BI Desktop</span></span>](desktop-connect-csv.md)   
* [<span data-ttu-id="06dc4-138">ใส่ข้อมูลลงใน Power BI Desktop โดยตรง</span><span class="sxs-lookup"><span data-stu-id="06dc4-138">Enter data directly into Power BI Desktop</span></span>](desktop-enter-data-directly-into-desktop.md)   
