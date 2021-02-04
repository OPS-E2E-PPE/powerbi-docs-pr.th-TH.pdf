---
title: เชื่อมต่อกับฐานข้อมูล Amazon Redshift ใน Power BI Desktop
description: ง่ายที่จะเชื่อมต่อและใช้ฐานข้อมูล Amazon Redshift ใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 05/08/2019
LocalizationGroup: Connect to data
ms.openlocfilehash: 60bf73e4500785c766a485fffc92a25bd8f2c852
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411367"
---
# <a name="connect-to-an-amazon-redshift-database-in-power-bi-desktop"></a><span data-ttu-id="633d0-103">เชื่อมต่อกับฐานข้อมูล Amazon Redshift ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="633d0-103">Connect to an Amazon Redshift database in Power BI Desktop</span></span>
<span data-ttu-id="633d0-104">ใน **Power BI Desktop** คุณสามารถเชื่อมต่อกับฐานข้อมูล **Amazon Redshift** และใช้ข้อมูลเบื้องต้นเช่นเดียวกับแหล่งข้อมูลอื่นใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="633d0-104">In **Power BI Desktop**, you can connect to an **Amazon Redshift** database and use the underlying data just like any other data source in Power BI Desktop.</span></span>

## <a name="connect-to-an-amazon-redshift-database"></a><span data-ttu-id="633d0-105">เชื่อมต่อกับฐานข้อมูล Amazon Redshift</span><span class="sxs-lookup"><span data-stu-id="633d0-105">Connect to an Amazon Redshift database</span></span>
<span data-ttu-id="633d0-106">เพื่อเชื่อมต่อกับฐานข้อมูล **Impala** ให้เลือก **รับข้อมูล** จาก ริบบอน **หน้าแรก** ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="633d0-106">To connect to an **Amazon Redshift** database, select **Get Data** from the **Home** ribbon in Power BI Desktop.</span></span> <span data-ttu-id="633d0-107">เลือก **ฐานข้อมูล** จากประเภททางด้านซ้าย จากนั้นคุณจะเห็น **Amazon Redshift**</span><span class="sxs-lookup"><span data-stu-id="633d0-107">Select **Database** from the categories on the left, and you see **Amazon Redshift**.</span></span>

![ภาพหน้าจอของกล่องโต้ตอบรับข้อมูล ที่แสดงการเลือกฐานข้อมูล Amazon Redshift](media/desktop-connect-redshift/connect_redshift_3.png)

<span data-ttu-id="633d0-109">ในหน้าต่าง **Amazon Redshift** ที่ปรากฎขึ้น พิมพ์หรือวางชื่อเซิร์ฟเวอร์ **Amazon Redshift** และฐานข้อมูลของคุณลงในกล่อง</span><span class="sxs-lookup"><span data-stu-id="633d0-109">In the **Amazon Redshift** window that appears, type or paste the name of your **Amazon Redshift** server and database into the box.</span></span> <span data-ttu-id="633d0-110">ในฐานะเป็นส่วนหนึ่งของเขตข้อมูล *เซิร์ฟเวอร์* ผู้ใช้สามารถระบุพอร์ตในรูปแบบต่อไปนี้: *ServerURL:Port*</span><span class="sxs-lookup"><span data-stu-id="633d0-110">As part of the *Server* field, users can specify a port in the following format: *ServerURL:Port*</span></span>

![ภาพหน้าจอของกล่องโต้ตอบ Amazon Redshift ที่แสดงเขตข้อมูลเซิร์ฟเวอร์และฐานข้อมูล](media/desktop-connect-redshift/connect_redshift_4.png)

<span data-ttu-id="633d0-112">เมื่อได้รับการถาม ให้ใส่ชื่อผู้ใช้และรหัสผ่านของคุณ</span><span class="sxs-lookup"><span data-stu-id="633d0-112">When prompted, put in your username and password.</span></span> <span data-ttu-id="633d0-113">คุณควรใช้ชื่อเซิร์ฟเวอร์ที่ได้ตรงกับใบรับรอง SSL เพื่อหลีกเลี่ยงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="633d0-113">You should use the server name that precisely matches the SSL certificate to avoid errors.</span></span> 

![ภาพหน้าจอของพรอมต์ข้อมูลประจำตัว Amazon Redshift ที่แสดงเขตข้อมูลชื่อผู้ใช้และรหัสผ่าน](media/desktop-connect-redshift/connect_redshift_5.png)

<span data-ttu-id="633d0-115">เมื่อเชื่อมต่อเสร็จเรียบร้อยแล้ว หน้าต่าง **ตัวนำทาง** จะปรากฏขึ้น และแสดงข้อมูลที่พร้อมใช้งานบนเซิร์ฟเวอร์ ซึ่งคุณสามารถเลือกองค์ประกอบหนึ่งรายการหรือหลายรายการเพื่อนำเข้าและใช้ใน **Power BI Desktop** ได้</span><span class="sxs-lookup"><span data-stu-id="633d0-115">Once you successfully connect, a **Navigator** window appears and displays the data available on the server, from which you can select one or multiple elements to import and use in **Power BI Desktop**.</span></span>

![ภาพหน้าจอของกล่องโต้ตอบตัวนำทาง ที่แสดงข้อมูลที่พร้อมใช้งานบนเซิร์ฟเวอร์](media/desktop-connect-redshift/connect_redshift_6.png)

<span data-ttu-id="633d0-117">เมื่อคุณทำการเลือกจากหน้าต่าง **ตัวนำทาง** คุณสามารถเลือกที่จะ **การโหลด** หรือ **แก้ไข** ข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="633d0-117">Once you make selections from the **Navigator** window, you can either **Load** or **Edit** the data.</span></span>

* <span data-ttu-id="633d0-118">ถ้าคุณเลือกที่จะ **โหลด** ข้อมูล คุณจะถูกถามให้ใช้ฟังก์ชัน *นำเข้า* หรือโหมด *DirectQuery* เพื่อโหลดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="633d0-118">If you choose to **Load** data, you'll be prompted to use either *Import* or *DirectQuery* mode to load the data.</span></span> <span data-ttu-id="633d0-119">สำหรับข้อมูลเพิ่มเติม ให้ตรวจสอบ[บทความที่อธิบาย DirectQuery](desktop-use-directquery.md)</span><span class="sxs-lookup"><span data-stu-id="633d0-119">For more information, check out this [article that explains DirectQuery](desktop-use-directquery.md).</span></span>
* <span data-ttu-id="633d0-120">ถ้าคุณเลือกที่จะ **แก้ไข** ข้อมูล **ตัวแก้ไขคิวรี** จะปรากฏขึ้นซึ่งคุณสามารถทำการเรียงลำดับของการเปลี่ยนแปลงและตัวกรองข้อมูลทั้งหมด มีหลายตัวที่จะนำไปใช้กับต้นแบบฐานข้อมูล **Amazon Redshift**  (ถ้าได้รับการสนับสนุน)</span><span class="sxs-lookup"><span data-stu-id="633d0-120">If you select to **Edit** the data, **Query Editor** appears where you can apply all sorts of transformations and filters to the data, many of which are applied to the underlying **Amazon Redshift** database itself (if supported).</span></span>

## <a name="next-steps"></a><span data-ttu-id="633d0-121">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="633d0-121">Next steps</span></span>
<span data-ttu-id="633d0-122">มีข้อมูลหลากหลายประเภทที่คุณสามารถเชื่อมต่อโดยใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="633d0-122">There are all sorts of data you can connect to using Power BI Desktop.</span></span> <span data-ttu-id="633d0-123">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแหล่งข้อมูล โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="633d0-123">For more information on data sources, check out the following resources:</span></span>

* [<span data-ttu-id="633d0-124">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="633d0-124">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="633d0-125">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="633d0-125">Data Sources in Power BI Desktop</span></span>](desktop-data-sources.md)
* [<span data-ttu-id="633d0-126">จัดรูปทรงและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="633d0-126">Shape and Combine Data with Power BI Desktop</span></span>](desktop-shape-and-combine-data.md)
* [<span data-ttu-id="633d0-127">เชื่อมต่อกับเวิร์กบุ๊ก Excel ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="633d0-127">Connect to Excel workbooks in Power BI Desktop</span></span>](desktop-connect-excel.md)   
* [<span data-ttu-id="633d0-128">ป้อนข้อมูลลงใน Power BI Desktop โดยตรง</span><span class="sxs-lookup"><span data-stu-id="633d0-128">Enter data directly into Power BI Desktop</span></span>](desktop-enter-data-directly-into-desktop.md)   
