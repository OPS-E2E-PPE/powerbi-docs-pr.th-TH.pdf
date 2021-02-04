---
title: เชื่อมต่อกับ Snowflake Computing Warehouse ใน Power BI Desktop
description: เชื่อมต่อและใช้งาน Snowflake Computing Warehouse ใน Power BI Desktop ได้อย่างง่ายดาย
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 01/04/2021
LocalizationGroup: Connect to data
ms.openlocfilehash: 00f78fef9f1abd11d7c553009db5541822c59c85
ms.sourcegitcommit: 932f6856849c39e34229dc9a49fb9379c56a888a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/06/2021
ms.locfileid: "97926373"
---
# <a name="connect-to-snowflake-in-power-bi-desktop"></a><span data-ttu-id="e88be-103">เชื่อมต่อกับ Snowflake ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e88be-103">Connect to Snowflake in Power BI Desktop</span></span>
<span data-ttu-id="e88be-104">ใน Power BI Desktop คุณสามารถเชื่อมต่อไปยัง **Snowflake** Computing Warehouse และใช้ข้อมูลพื้นฐานได้เช่นเดียวกับแหล่งข้อมูลอื่นๆ ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e88be-104">In Power BI Desktop, you can connect to a **Snowflake** computing warehouse and use the underlying data just like any other data source in Power BI Desktop.</span></span> 

## <a name="connect-to-a-snowflake-computing-warehouse"></a><span data-ttu-id="e88be-105">เชื่อมต่อกับ Snowflake Computing Warehouse</span><span class="sxs-lookup"><span data-stu-id="e88be-105">Connect to a Snowflake computing warehouse</span></span>
<span data-ttu-id="e88be-106">เมื่อต้องการเชื่อมต่อกับ **Snowflake** Computing Warehouse ให้เลือก **เรียกใช้ข้อมูล** จากแถบ **หน้าหลัก** ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e88be-106">To connect to a **Snowflake** computing warehouse, select **Get Data** from the **Home** ribbon in Power BI Desktop.</span></span> <span data-ttu-id="e88be-107">เลือก **ฐานข้อมูล** จากประเภททางด้านซ้าย จากนั้นคุณจะเห็น **Snowflake**</span><span class="sxs-lookup"><span data-stu-id="e88be-107">Select **Database** from the categories on the left, and you see **Snowflake**.</span></span>

![ภาพหน้าจอของกล่องโต้ตอบรับข้อมูล ที่แสดงการเลือกฐานข้อมูล Snowflake](media/desktop-connect-snowflake/connect-snowflake-2b.png)

<span data-ttu-id="e88be-109">ในหน้าต่าง **Snowflake** ที่ปรากฏขึ้น ให้พิมพ์หรือวางชื่อ Snowflake Computing Warehouse ลงในกล่อง แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e88be-109">In the **Snowflake** window that appears, type or paste the name of your Snowflake computing warehouse into the box and select **OK**.</span></span> <span data-ttu-id="e88be-110">โปรดทราบว่าคุณสามารถเลือก **นำเข้า** ข้อมูลได้โดยตรงใน Power BI หรือจะใช้ **DirectQuery** ก็ได้</span><span class="sxs-lookup"><span data-stu-id="e88be-110">Note that you can choose to **Import** data directly into Power BI, or you can use **DirectQuery**.</span></span> <span data-ttu-id="e88be-111">เรียนรู้เพิ่มเติมเกี่ยวกับ[การใช้ DirectQuery](desktop-use-directquery.md)</span><span class="sxs-lookup"><span data-stu-id="e88be-111">You can learn more about [using DirectQuery](desktop-use-directquery.md).</span></span> <span data-ttu-id="e88be-112">โปรดทราบว่า AAD SSO สนับสนุนเฉพาะ DirectQuery เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e88be-112">Please note that AAD SSO only supports DirectQuery.</span></span>

![ภาพหน้าจอของกล่องโต้ตอบ Snowflake ที่แสดงปุ่มนำเข้าวิทยุที่เลือกไว้](media/desktop-connect-snowflake/connect-snowflake-3.png)

<span data-ttu-id="e88be-114">เมื่อได้รับการถาม ให้ใส่ชื่อผู้ใช้และรหัสผ่านของคุณ</span><span class="sxs-lookup"><span data-stu-id="e88be-114">When prompted, put in your username and password.</span></span>

![ภาพหน้าจอของข้อความแจ้งเตือนข้อมูลประจำตัว Snowflake ที่แสดงเขตข้อมูลชื่อผู้ใช้และรหัสผ่าน](media/desktop-connect-snowflake/connect-snowflake-4.png)

> [!NOTE]
> <span data-ttu-id="e88be-116">เมื่อคุณป้อนชื่อผู้ใช้และรหัสผ่านสำหรับเซิร์ฟเวอร์ **Snowflake** ที่เฉพาะเจาะจงแล้ว Power BI Desktop จะใช้ข้อมูลประจำตัวเดียวกันนั้นเพื่อพยายามเชื่อมต่ออีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="e88be-116">Once you enter your username and password for a particular **Snowflake** server, Power BI Desktop uses those same credentials in subsequent connection attempts.</span></span> <span data-ttu-id="e88be-117">คุณสามารถปรับเปลี่ยนข้อมูลประจำตัวเหล่านั้นได้โดยไปที่ **ไฟล์ > ตัวเลือกและการตั้งค่า > การตั้งค่าแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="e88be-117">You can modify those credentials by going to **File > Options and settings > Data source settings**.</span></span>
> 
> 

<span data-ttu-id="e88be-118">ถ้าคุณต้องการใช้ตัวเลือกบัญชี Microsoft จะต้องมีการกำหนดค่าการรวม Snowflake AAD ในฝั่ง Snowflake</span><span class="sxs-lookup"><span data-stu-id="e88be-118">If you want to use the Microsoft account option, the Snowflake AAD integration must be configured on the Snowflake side.</span></span> <span data-ttu-id="e88be-119">เมื่อต้องการทำเช่นนี้ ให้อ่านส่วนเริ่มต้นใช้งานของ [เอกสารประกอบ Snowflake บนหัวข้อนั้น](https://docs.snowflake.net/manuals/user-guide/oauth-powerbi.html#power-bi-sso-to-snowflake)</span><span class="sxs-lookup"><span data-stu-id="e88be-119">To do this, read the Getting Started section of the [Snowflake documentation on the topic](https://docs.snowflake.net/manuals/user-guide/oauth-powerbi.html#power-bi-sso-to-snowflake).</span></span>

![ชนิดการรับรองความถูกต้องของบัญชี Microsoft ในตัวเชื่อมต่อ Snowflake](media/desktop-connect-snowflake/connect-snowflake-6.png)


<span data-ttu-id="e88be-121">เมื่อเชื่อมต่อเสร็จเรียบร้อยแล้ว หน้าต่าง **ตัวนำทาง** จะปรากฏขึ้น และแสดงข้อมูลที่พร้อมใช้งานบนเซิร์ฟเวอร์ ซึ่งคุณสามารถเลือกองค์ประกอบหนึ่งรายการหรือหลายรายการเพื่อนำเข้าและใช้ใน **Power BI Desktop** ได้</span><span class="sxs-lookup"><span data-stu-id="e88be-121">Once you successfully connect, a **Navigator** window appears and displays the data available on the server, from which you can select one or multiple elements to import and use in **Power BI Desktop**.</span></span>

![ODBC Error 28000 ทำให้เกิดความผิดพลาดในการเชื่อมต่อ](media/desktop-connect-snowflake/connect-snowflake-5.png)

<span data-ttu-id="e88be-123">คุณสามารถ **โหลด** ตารางที่เลือก ซึ่งจะนำทั้งตารางลงใน **Power BI Desktop** หรือคุณสามารถ **แก้ไข** คิวรี ซึ่งจะเปิด **ตัวแก้ไขคิวรี** เพื่อให้คุณสามารถกรองและปรับปรุงชุดข้อมูลที่ต้องการใช้ จากนั้นจึงโหลดชุดข้อมูลที่ปรับปรุงแล้วลงใน **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="e88be-123">You can **Load** the selected table, which brings the entire table into **Power BI Desktop**, or you can **Edit** the query, which opens **Query Editor** so you can filter and refine the set of data you want to use, and then load that refined set of data into **Power BI Desktop**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e88be-124">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="e88be-124">Next steps</span></span>
<span data-ttu-id="e88be-125">มีข้อมูลหลากหลายประเภทที่คุณสามารถเชื่อมต่อโดยใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e88be-125">There are all sorts of data you can connect to using Power BI Desktop.</span></span> <span data-ttu-id="e88be-126">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแหล่งข้อมูล โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e88be-126">For more information on data sources, check out the following resources:</span></span>

* [<span data-ttu-id="e88be-127">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="e88be-127">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="e88be-128">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e88be-128">Data Sources in Power BI Desktop</span></span>](desktop-data-sources.md)
* [<span data-ttu-id="e88be-129">จัดรูปทรงและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e88be-129">Shape and Combine Data with Power BI Desktop</span></span>](desktop-shape-and-combine-data.md)
* [<span data-ttu-id="e88be-130">เชื่อมต่อกับเวิร์กบุ๊ก Excel ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e88be-130">Connect to Excel workbooks in Power BI Desktop</span></span>](desktop-connect-excel.md)   
* [<span data-ttu-id="e88be-131">ป้อนข้อมูลลงใน Power BI Desktop โดยตรง</span><span class="sxs-lookup"><span data-stu-id="e88be-131">Enter data directly into Power BI Desktop</span></span>](desktop-enter-data-directly-into-desktop.md)   
