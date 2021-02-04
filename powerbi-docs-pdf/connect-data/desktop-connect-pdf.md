---
title: เชื่อมต่อกับไฟล์ PDF ใน Power BI Desktop
description: เชื่อมต่อและใช้ข้อมูลจากไฟล์ PDF ได้อย่างง่ายดายใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 01/04/2021
LocalizationGroup: Connect to data
ms.openlocfilehash: 5a6b0d47b524c4f36938878cfe48a64d47470854
ms.sourcegitcommit: 932f6856849c39e34229dc9a49fb9379c56a888a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/06/2021
ms.locfileid: "97926317"
---
# <a name="connect-to-pdf-files-in-power-bi-desktop"></a><span data-ttu-id="61420-103">เชื่อมต่อกับไฟล์ PDF ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="61420-103">Connect to PDF files in Power BI Desktop</span></span>
<span data-ttu-id="61420-104">ใน Power BI Desktop คุณสามารถเชื่อมต่อกับ **ไฟล์ PDF** และใช้ข้อมูลที่รวมจากไฟล์เช่นเดียวกับแหล่งข้อมูลอื่น ๆ ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="61420-104">In Power BI Desktop, you can connect to a **PDF file** and use the included data from the file, just like any other data source in Power BI Desktop.</span></span>

![เชื่อมต่อกับข้อมูลในไฟล์ PDF](media/desktop-connect-pdf/connect-pdf-04.png)

<span data-ttu-id="61420-106">หัวข้อต่อไปนี้อธิบายถึงวิธีเชื่อมต่อกับ **ไฟล์ PDF** เลือกข้อมูล และนำข้อมูลดังกล่าวไปวางไว้ที่ **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="61420-106">The following sections describe how to connect to a **PDF file**, select data, and bring that data into **Power BI Desktop**.</span></span>

<span data-ttu-id="61420-107">เราแนะนำให้อัปเกรดเป็นเวอร์ชันล่าสุด **Power BI Desktop** เสมอ ซึ่งคุณสามารถรับได้จากลิงก์ใน [รับ Power BI Desktop](../fundamentals/desktop-get-the-desktop.md)</span><span class="sxs-lookup"><span data-stu-id="61420-107">We always recommend upgrading to the most recent release of **Power BI Desktop**, which you can get from a link in [get Power BI Desktop](../fundamentals/desktop-get-the-desktop.md).</span></span> 

## <a name="connect-to-a-pdf-file"></a><span data-ttu-id="61420-108">เชื่อมต่อกับไฟล์ PDF</span><span class="sxs-lookup"><span data-stu-id="61420-108">Connect to a PDF file</span></span>
<span data-ttu-id="61420-109">หากต้องการเชื่อมต่อกับไฟล์ **PDF** ให้เลือก **รับข้อมูล** จากริบบิ้น **หน้าแรก** ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="61420-109">To connect to a **PDF** file select **Get Data** from the **Home** ribbon in Power BI Desktop.</span></span> <span data-ttu-id="61420-110">เลือก **ไฟล์** จากหมวดหมู่ด้านซ้าย และคุณจะเห็น **PDF**</span><span class="sxs-lookup"><span data-stu-id="61420-110">Select **File** from the categories on the left, and you see **PDF**.</span></span>

![เลือก PDF จาก Get Data(รับข้อมูล)](media/desktop-connect-pdf/connect-pdf-01.png)

<span data-ttu-id="61420-112">คุณได้รับพร้อมท์ให้ระบุตำแหน่งของไฟล์ PDF ที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="61420-112">You're prompted to provide the location of the PDF file you want to use.</span></span> <span data-ttu-id="61420-113">เมื่อคุณระบุตำแหน่งไฟล์และโหลดไฟล์ PDF หน้าต่าง **เนวิเกเตอร์** จะปรากฏขึ้นและแสดงข้อมูลจากไฟล์ ซึ่งคุณสามารถเลือกองค์ประกอบหนึ่งหรือหลายรายการเพื่อนำเข้าและใช้ใน **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="61420-113">Once you provide the file location and the PDF file loads, a **Navigator** window appears and displays the data available from the file, from which you can select one or multiple elements to import and use in **Power BI Desktop**.</span></span>

![เชื่อมต่อกับข้อมูลในไฟล์ PDF](media/desktop-connect-pdf/connect-pdf-04.png)

<span data-ttu-id="61420-115">การเลือกช่องทำเครื่องหมายถัดจากองค์ประกอบที่ค้นพบในไฟล์ PDF จะแสดงรายการในบานหน้าต่างด้านขวา</span><span class="sxs-lookup"><span data-stu-id="61420-115">Selecting a checkbox next to discovered elements in the PDF file displays them in the right pane.</span></span> <span data-ttu-id="61420-116">เมื่อคุณพร้อมที่จะนำเข้าแล้วให้เลือกปุ่ม **Load (โหลด)** เพื่อนำข้อมูลมาไว้ใน **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="61420-116">When you're ready to import, select the **Load** button to bring the data into **Power BI Desktop**.</span></span>

<span data-ttu-id="61420-117">ตั้งแต่เดือนพฤศจิกายน 2018 ในการเผยแพร่ของ **Power BI Desktop** คุณสามารถระบุ **หน้าเริ่มต้น** และ **หน้าสุดท้าย** เป็นพารามิเตอร์เพิ่มเติมสำหรับการเชื่อมต่อ PDF ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="61420-117">Beginning with the November 2018 release of **Power BI Desktop**, you can specify the **Start page** and **End Page** as optional parameters for your PDF connection.</span></span> <span data-ttu-id="61420-118">คุณยังสามารถระบุพารามิเตอร์เหล่านี้ในภาษาสูตร M โดยใช้รูปแบบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="61420-118">You can also specify these parameters in the M formula language, using the following format:</span></span>

`Pdf.Tables(File.Contents("c:\sample.pdf"), [StartPage=10, EndPage=11])`

## <a name="limitations-and-considerations"></a><span data-ttu-id="61420-119">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="61420-119">Limitations and considerations</span></span>

<span data-ttu-id="61420-120">เมื่อทำงานกับตัวเชื่อมต่อ PDF บนชุดข้อมูลในความจุพรีเมี่ยม ตัวเชื่อมต่อ PDF จะเชื่อมต่ออย่างไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="61420-120">When working with the PDF connector on datasets in a Premium capacity, the PDF connector does not properly make the connection.</span></span> <span data-ttu-id="61420-121">หากต้องการเปิดใช้งานตัวเชื่อมต่อ PDF เพื่อทำงานกับชุดข้อมูลในความจุพรีเมี่ยม ให้กำหนดค่าชุดข้อมูลนั้นเพื่อใช้เกตเวย์และยืนยันการเชื่อมต่อกับชุดข้อมูลนั้นผ่านเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="61420-121">To enable the PDF connector to work on a dataset in a Premium capacity, configure that dataset to use a gateway, and confirm the connection to that dataset goes through the gateway.</span></span>  


## <a name="next-steps"></a><span data-ttu-id="61420-122">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="61420-122">Next steps</span></span>
<span data-ttu-id="61420-123">มีข้อมูลหลากหลายประเภทที่คุณสามารถเชื่อมต่อโดยใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="61420-123">There are all sorts of data you can connect to using Power BI Desktop.</span></span> <span data-ttu-id="61420-124">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแหล่งข้อมูล โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="61420-124">For more information on data sources, check out the following resources:</span></span>

* [<span data-ttu-id="61420-125">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="61420-125">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="61420-126">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="61420-126">Data Sources in Power BI Desktop</span></span>](desktop-data-sources.md)
* [<span data-ttu-id="61420-127">จัดรูปทรงและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="61420-127">Shape and Combine Data with Power BI Desktop</span></span>](desktop-shape-and-combine-data.md)
* [<span data-ttu-id="61420-128">เชื่อมต่อกับเวิร์กบุ๊ก Excel ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="61420-128">Connect to Excel workbooks in Power BI Desktop</span></span>](desktop-connect-excel.md)   
* [<span data-ttu-id="61420-129">ป้อนข้อมูลลงใน Power BI Desktop โดยตรง</span><span class="sxs-lookup"><span data-stu-id="61420-129">Enter data directly into Power BI Desktop</span></span>](desktop-enter-data-directly-into-desktop.md)   
