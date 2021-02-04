---
title: Azure SQL Data Warehouse พร้อม DirectQuery
description: Azure SQL Data Warehouse พร้อม DirectQuery
author: davidiseminger
ms.author: davidi
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.reviewer: ''
ms.custom: ''
ms.date: 06/03/2020
LocalizationGroup: Data from databases
ms.openlocfilehash: d4edc60e844f45c91de11771655e9399cd0e073e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96403708"
---
# <a name="azure-sql-data-warehouse-with-directquery"></a><span data-ttu-id="4b79b-103">Azure SQL Data Warehouse พร้อม DirectQuery</span><span class="sxs-lookup"><span data-stu-id="4b79b-103">Azure SQL Data Warehouse with DirectQuery</span></span>

<span data-ttu-id="4b79b-104">Azure SQL Data Warehouse พร้อม DirectQuery ช่วยให้คุณสามารถสร้างรายงานแบบไดนามิกที่ยึดตามข้อมูลและเมทริกซ์ที่คุณมีอยู่แล้วใน Azure SQL Data Warehouse</span><span class="sxs-lookup"><span data-stu-id="4b79b-104">Azure SQL Data Warehouse with DirectQuery allows you to create dynamic reports based on data and metrics you already have in Azure SQL Data Warehouse.</span></span> <span data-ttu-id="4b79b-105">ด้วย DirectQuery แบบสอบถามจะถูกส่งกลับไปยัง Azure SQL Data Warehouse ของคุณในแบบเรียลไทม์ ตามที่คุณสำรวจข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4b79b-105">With DirectQuery, queries are sent back to your Azure SQL Data Warehouse in real time as you explore the data.</span></span> <span data-ttu-id="4b79b-106">โดยแบบสอบถามแบบเรียลไทม์นั้นมีการรวมเข้ากับ SQL Data Warehouse ส่วนหนึ่ง เพื่อให้ผู้ใช้งานสามารถสร้างรายงานแบบไดนามิกได้ในเวลาเพียงไม่นาน แม้จะมีข้อมูลเยอะระดับเทราไบต์</span><span class="sxs-lookup"><span data-stu-id="4b79b-106">Real-time queries, combined with the scale of SQL Data Warehouse enables users to create dynamic reports in minutes against terabytes of data.</span></span> <span data-ttu-id="4b79b-107">นอกจากนี้ ลิงก์ **สร้างแดชบอร์ด + รายงาน** ช่วยให้ผู้ใช้สามารถสร้างรายงาน Power BI โดยใช้ SQL Data Warehouse ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="4b79b-107">In addition, the **Build dashboards + reports** link allows users to create Power BI reports using their SQL Data Warehouse.</span></span>

<span data-ttu-id="4b79b-108">เมื่อใช้ตัวเชื่อมต่อ SQL Data Warehouse:</span><span class="sxs-lookup"><span data-stu-id="4b79b-108">When using the SQL Data Warehouse connector:</span></span>

* <span data-ttu-id="4b79b-109">ระบุชื่อเซิร์ฟเวอร์ที่มีคุณสมบัติครบถ้วนเมื่อเชื่อมต่อ (ดูด้านล่างสำหรับรายละเอียด)</span><span class="sxs-lookup"><span data-stu-id="4b79b-109">Specify the fully qualified server name when connecting (see below for details)</span></span>
* <span data-ttu-id="4b79b-110">ตรวจสอบให้แน่ใจว่ามีการกำหนดค่ากฎไฟร์วอลล์สำหรับเซิร์ฟเวอร์เพื่อ "อนุญาตการเข้าถึงบริการ Azure"</span><span class="sxs-lookup"><span data-stu-id="4b79b-110">Ensure firewall rules for the server are configured to "Allow access to Azure services"</span></span>
* <span data-ttu-id="4b79b-111">ทุกการดำเนินการ เช่น การเลือกคอลัมน์ หรือเพิ่มตัวกรองจะสอบถามคลังข้อมูลโดยตรง</span><span class="sxs-lookup"><span data-stu-id="4b79b-111">Every action such as selecting a column or adding a filter will directly query the data warehouse</span></span>
* <span data-ttu-id="4b79b-112">ไทล์จะถูกตั้งค่าการรีเฟรชทุก 15 นาทีโดยประมาณ และรีเฟรชไม่จำเป็นต้องมีการทำกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="4b79b-112">Tiles are set to refresh approximately every 15 minutes and refresh does not need to be scheduled.</span></span>  <span data-ttu-id="4b79b-113">ซึ่งคุณอาจปรับการรีเฟรชในส่วนการตั้งค่าขั้นสูงได้เมื่อทำการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="4b79b-113">Refresh can be adjusted in the Advanced settings when you connect.</span></span>
* <span data-ttu-id="4b79b-114">การถามตอบสำหรับชุดข้อมูล DirectQuery ไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4b79b-114">Q&A isn't available for DirectQuery datasets</span></span>
* <span data-ttu-id="4b79b-115">ไม่มีการเลือกการเปลี่ยนแปลง Schema โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="4b79b-115">Schema changes aren't picked up automatically</span></span>

<span data-ttu-id="4b79b-116">ข้อจำกัดและบันทึกย่อเหล่านี้อาจเปลี่ยนแปลงขณะที่เราปรับปรุงประสบการณ์การใช้งานขึ้นเรื่อย ๆ</span><span class="sxs-lookup"><span data-stu-id="4b79b-116">These restrictions and notes may change as we continue to improve the experience.</span></span> <span data-ttu-id="4b79b-117">ขั้นตอนในการเชื่อมต่อจะมีรายละเอียดดังด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="4b79b-117">The steps to connect are detailed below.</span></span>

## <a name="build-dashboards-and-reports-in-power-bi"></a><span data-ttu-id="4b79b-118">สร้างแดชบอร์ดและรายงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="4b79b-118">Build dashboards and reports in Power BI</span></span>

> [!Important]
> <span data-ttu-id="4b79b-119">เรากำลังปรับปรุงการเชื่อมต่อของเรากับคลังข้อมูล SQL ของ Azure</span><span class="sxs-lookup"><span data-stu-id="4b79b-119">We have been improving our connectivity to Azure SQL Data Warehouse.</span></span> <span data-ttu-id="4b79b-120">สำหรับประสบการณ์ดีที่สุดในการเชื่อมต่อกับแหล่งคลังข้อมูล SQL ของ Azure ของคุณ ใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4b79b-120">For the best experience to connect to your Azure SQL Data Warehouse data source, use Power BI Desktop.</span></span> <span data-ttu-id="4b79b-121">เมื่อคุณได้สร้างรูปแบบข้อมูลและรายงานของคุณแล้ว คุณสามารถเผยแพร่สิ่งดังกล่าวไปยังบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="4b79b-121">Once you've built your model and report, you can publish it to the Power BI service.</span></span> <span data-ttu-id="4b79b-122">ตัวเชื่อมต่อโดยตรงที่มีอยู่ก่อนหน้านี้สำหรับ Azure SQL Data Warehouse ในบริการ Power BI ในขณะนี้ไม่สามารถใช้ได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="4b79b-122">The previously available direct connector for Azure SQL Data Warehouse in the Power BI service is no longer available.</span></span>

<span data-ttu-id="4b79b-123">การเคลื่อนย้ายข้อมูลระหว่าง SQL Data Warehouse กับ Power BI คือการสร้างรายงานใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4b79b-123">The easiest way to move between your SQL Data Warehouse and Power BI is to create reports in Power BI Desktop.</span></span> <span data-ttu-id="4b79b-124">คุณสามารถใช้ปุ่ม **สร้างแดชบอร์ด + รายงาน** ภายในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="4b79b-124">You can use the **Build dashboards + reports** button within the Azure portal.</span></span>

1. <span data-ttu-id="4b79b-125">ในการเริ่มต้น ให้ดาวน์โหลดและติดตั้ง Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4b79b-125">To get started, download and install Power BI Desktop.</span></span> <span data-ttu-id="4b79b-126">ดูบทความ [รับ Power BI Desktop](../fundamentals/desktop-get-the-desktop.md) สำหรับข้อมูลเกี่ยวกับการดาวน์โหลดและติดตั้ง หรือไปยังขั้นตอนถัดไปโดยตรง</span><span class="sxs-lookup"><span data-stu-id="4b79b-126">See the [get Power BI Desktop](../fundamentals/desktop-get-the-desktop.md) article for information about downloading and installing, or go directly to the next step.</span></span>

2. <span data-ttu-id="4b79b-127">คุณยังสามารถคลิกลิงก์ **สร้างแดชบอร์ด + รายงาน** เพื่อดาวน์โหลด Power BI Desktop ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="4b79b-127">You can also click the **Build dashboards + reports** link to download Power BI Desktop.</span></span>

    ![เปิดใน Power BI](media/service-azure-sql-data-warehouse-with-direct-connect/create-reports-01.png)


## <a name="connecting-through-power-bi-desktop"></a><span data-ttu-id="4b79b-129">เชื่อมต่อผ่านทาง Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4b79b-129">Connecting through Power BI Desktop</span></span>

<span data-ttu-id="4b79b-130">คุณสามารถเชื่อมต่อกับ SQL Data Warehouse ได้โดยใช้ปุ่ม **รับข้อมูล** ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4b79b-130">You can connect to a SQL Data Warehouse using the **Get Data** button in Power BI Desktop.</span></span> 

1. <span data-ttu-id="4b79b-131">เลือกปุ่ม **รับข้อมูล** จากเมนู **หน้าหลัก**</span><span class="sxs-lookup"><span data-stu-id="4b79b-131">Select the **Get Data** button from the **Home** menu.</span></span>  

    ![ปุ่มรับข้อมูล](media/service-azure-sql-data-warehouse-with-direct-connect/create-reports-02.png)

2. <span data-ttu-id="4b79b-133">เลือก **เพิ่มเติม ...** เพื่อดูแหล่งข้อมูลทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="4b79b-133">Select **More...** to see all available data sources.</span></span> <span data-ttu-id="4b79b-134">จากหน้าต่างที่ปรากฏขึ้น ให้เลือก **Azure** จากบานหน้าต่างด้านซ้ายจากนั้นเลือก **Azure SQL Data Warehouse** จากรายการของตัวเชื่อมต่อที่พร้อมใช้งานในบานหน้าต่างด้านขวา</span><span class="sxs-lookup"><span data-stu-id="4b79b-134">From the window that appears, select **Azure** from the left pane, then select **Azure SQL Data Warehouse** from the list of available connectors in the right pane.</span></span>

    ![แหล่งข้อมูล Azure](media/service-azure-sql-data-warehouse-with-direct-connect/create-reports-03.png)

3. <span data-ttu-id="4b79b-136">ในหน้าต่างที่ปรากฏขึ้น ให้ใส่เซิร์ฟเวอร์ของคุณและเลือกระบุฐานข้อมูลที่คุณต้องการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="4b79b-136">In the window that appears, input your Server and optionally state the Database to which you want to connect.</span></span> <span data-ttu-id="4b79b-137">คุณยังสามารถเลือกโหมดการเชื่อมต่อข้อมูลของคุณ: Import หรือ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="4b79b-137">You can also select your data connectivity mode: Import or DirectQuery.</span></span> <span data-ttu-id="4b79b-138">สำหรับการเข้าถึงข้อมูลแบบเรียลไทม์ใน Azure SQL Data Warehouse ของคุณ ให้ใช้ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="4b79b-138">For real-time access to information in your Azure SQL Data Warehouse, use DirectQuery.</span></span>

    ![Azure SQL DW ที่มีการเชื่อมต่อโดยตรง](media/service-azure-sql-data-warehouse-with-direct-connect/create-reports-04.png)

4. <span data-ttu-id="4b79b-140">สำหรับตัวเลือกขั้นสูงสำหรับการเชื่อมต่อ Azure SQL Data Warehouse ให้เลือกลูกศรลงที่อยู่ด้านช้าง **ตัวเลือกขั้นสูง** เพื่อแสดงตัวเลือกเพิ่มเติมสำหรับการเชื่อมต่อของคุณ</span><span class="sxs-lookup"><span data-stu-id="4b79b-140">For advanced options for the Azure SQL Data Warehouse connection, select the down arrow beside **Advanced options** to display additional options for your connection.</span></span>

    ![ชื่อเซิร์ฟเวอร์](media/service-azure-sql-data-warehouse-with-direct-connect/create-reports-05.png)

<span data-ttu-id="4b79b-142">ส่วนถัดไปจะอธิบายวิธีการค้นหาค่าพารามิเตอร์สำหรับการเชื่อมต่อของคุณ</span><span class="sxs-lookup"><span data-stu-id="4b79b-142">The next section describes how to find parameter values for your connection.</span></span> 

## <a name="finding-parameter-values"></a><span data-ttu-id="4b79b-143">ค้นหาค่าพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="4b79b-143">Finding Parameter Values</span></span>

<span data-ttu-id="4b79b-144">สามารถค้นหาชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูลแบบเต็มของคุณได้ในพอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="4b79b-144">Your fully qualified server name and database name can be found in the Azure portal.</span></span> <span data-ttu-id="4b79b-145">โปรดสังเกตว่ามีเฉพาะ SQL Data Warehouse เท่านั้นที่ปรากฏในพอร์ทัล Azure ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="4b79b-145">Note that SQL Data Warehouse only has a presence in the Azure portal at this time.</span></span>

![พอร์ทัล Microsoft Azure](media/service-azure-sql-data-warehouse-with-direct-connect/azureportal.png)

> [!NOTE]
> <span data-ttu-id="4b79b-147">ถ้าผู้เช่า Power BI ของคุณอยู่ในภูมิภาคเดียวกันกับ Azure SQL Data Warehouse จะไม่มีค่าธรรมเนียมขาออก</span><span class="sxs-lookup"><span data-stu-id="4b79b-147">If your Power BI tenant is in the same region as the Azure SQL Data Warehouse there will be no egress charges.</span></span> <span data-ttu-id="4b79b-148">คุณสามารถค้นหาตำแหน่งที่ผู้เช่า Power BI ของคุณอยู่โดยใช้[คำแนะนำเหล่านี้](../admin/service-admin-where-is-my-tenant-located.md)ได้</span><span class="sxs-lookup"><span data-stu-id="4b79b-148">You can find where your Power BI tenant is located using [these instructions](../admin/service-admin-where-is-my-tenant-located.md).</span></span>

[!INCLUDE [direct-query-sso](../includes/direct-query-sso.md)]

## <a name="next-steps"></a><span data-ttu-id="4b79b-149">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4b79b-149">Next steps</span></span>

* [<span data-ttu-id="4b79b-150">เกี่ยวกับการใช้ DirectQuery ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="4b79b-150">About using DirectQuery in Power BI</span></span>](desktop-directquery-about.md)
* [<span data-ttu-id="4b79b-151">Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="4b79b-151">What is Power BI?</span></span>](../fundamentals/power-bi-overview.md)  
* [<span data-ttu-id="4b79b-152">รับข้อมูลสำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="4b79b-152">Get Data for Power BI</span></span>](service-get-data.md)  
* [<span data-ttu-id="4b79b-153">คลังข้อมูล Azure SQL</span><span class="sxs-lookup"><span data-stu-id="4b79b-153">Azure SQL Data Warehouse</span></span>](/azure/sql-data-warehouse/sql-data-warehouse-overview-what-is/)

<span data-ttu-id="4b79b-154">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4b79b-154">More questions?</span></span> [<span data-ttu-id="4b79b-155">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="4b79b-155">Try the Power BI Community</span></span>](https://community.powerbi.com/)