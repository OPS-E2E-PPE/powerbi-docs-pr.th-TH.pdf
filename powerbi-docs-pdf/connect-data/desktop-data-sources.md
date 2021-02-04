---
title: แหล่งข้อมูลใน Power BI Desktop
description: แหล่งข้อมูลใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 12/10/2020
LocalizationGroup: Connect to data
ms.openlocfilehash: 0d09871f9a47e9c8691ab3f955638c59b016d145
ms.sourcegitcommit: b472236df99b490db30f0168bd7284ae6e6095fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/16/2020
ms.locfileid: "97600564"
---
# <a name="data-sources-in-power-bi-desktop"></a><span data-ttu-id="61c60-103">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="61c60-103">Data sources in Power BI Desktop</span></span>

<span data-ttu-id="61c60-104">คุณสามารถเชื่อมต่อกับข้อมูลจากแหล่งต่าง ๆ มากมายด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="61c60-104">With Power BI Desktop, you can connect to data from many different sources.</span></span> <span data-ttu-id="61c60-105">สำหรับรายการทั้งหมดของแหล่งข้อมูลที่พร้อมใช้งาน ให้ดู[แหล่งข้อมูล Power BI](power-bi-data-sources.md)</span><span class="sxs-lookup"><span data-stu-id="61c60-105">For a full list of available data sources, see [Power BI data sources](power-bi-data-sources.md).</span></span>

<span data-ttu-id="61c60-106">คุณเชื่อมต่อไปยังข้อมูลโดยการใช้ริบบิ้น **หน้าหลัก**</span><span class="sxs-lookup"><span data-stu-id="61c60-106">You connect to data by using the **Home** ribbon.</span></span> <span data-ttu-id="61c60-107">ในการแสดงเมนูประเภทข้อมูล **ทั่วไปส่วนใหญ่** เลือกป้ายปุ่ม **รับข้อมูล** หรือลูกศรชี้ลง</span><span class="sxs-lookup"><span data-stu-id="61c60-107">To show the **Most Common** data types menu, select the **Get Data** button label or the down arrow.</span></span>

![เมนูประเภทข้อมูลทั่วไปส่วนใหญ่ รับข้อมูลใน Power BI Desktop](media/desktop-data-sources/data-sources-01.png)

<span data-ttu-id="61c60-109">ไปยังกล่องบทสนทนา **รับข้อมูล** แสดงเมนูประเภทข้อมูล **ทั่วไปส่วนใหญ่** และเลือก **เพิ่มเติม**</span><span class="sxs-lookup"><span data-stu-id="61c60-109">To go to the **Get Data** dialog box, show the **Most Common** data types menu and select **More**.</span></span> <span data-ttu-id="61c60-110">คุณยังสามารถนำกล่องบทนา **รับข้อมูล** ขึ้นไป (และทางอ้อมไปยังเมนู **ทั่วไปส่วนใหญ่**) โดยการเลือกไอคอน **รับข้อมูล** โดยตรง</span><span class="sxs-lookup"><span data-stu-id="61c60-110">You can also bring up the **Get Data** dialog box (and bypass the **Most Common** menu) by selecting the **Get Data** icon directly.</span></span>

![ปุ่มรับข้อมูล Power BI desktop](media/desktop-data-sources/data-sources-02.png)

> [!NOTE]
> <span data-ttu-id="61c60-112">ทีม Power BI ได้ทำการขยายแหล่งข้อมูลอย่างต่อเนื่องที่ใช้ได้ไปยัง Power BI Desktop และ Power BI service</span><span class="sxs-lookup"><span data-stu-id="61c60-112">The Power BI team is continually expanding the data sources available to Power BI Desktop and the Power BI service.</span></span> <span data-ttu-id="61c60-113">ดังนั้นคุณมักจะเห็นงานระหว่างแหล่งข้อมูลที่กำลังดำเนินการอยู่ในช่วงเริ่มต้นได้รับการทำเครื่องหมายเป็น **เบต้า** หรือ **แสดงตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="61c60-113">As such, you'll often see early versions of work-in-progress data sources marked as **Beta** or **Preview**.</span></span> <span data-ttu-id="61c60-114">ทุกแหล่งข้อมูลทำให้ชัดเจนเป็น **เบต้า** หรือ **การแสดงก่อน** มีการสนับสนุนและการทำงานที่จำกัด และมันอาจจะไม่ถูกใช้ในสภาพแวดล้อมของการผลิต</span><span class="sxs-lookup"><span data-stu-id="61c60-114">Any data source marked as **Beta** or **Preview** has limited support and functionality, and it shouldn't be used in production environments.</span></span> <span data-ttu-id="61c60-115">นอกจากนี้ทุกแหล่งข้อมูลที่ทำให้ชัดเจนเป็น **เบต้า** หรือ **การแสดงก่อน** สำหรับ Power BI Desktop อาจไม่สามารถใช้ได้สำหรับการใช้ในการบริการ Power BI หรือการบริการ Microsoft อื่นๆ จนกว่าแหล่งข้อมูลจะสามารถใช้ได้โดยทั่วไป (GA)</span><span class="sxs-lookup"><span data-stu-id="61c60-115">Additionally, any data source marked as **Beta** or **Preview** for Power BI Desktop may not be available for use in the Power BI service or other Microsoft services until the data source becomes generally available (GA).</span></span>

> [!NOTE]
> <span data-ttu-id="61c60-116">มีตัวเชื่อมต่อข้อมูลจำนวนมากสำหรับ Power BI Desktop ที่จำเป็นต้องใช้ Internet Explorer 10 (หรือใหม่กว่า) สำหรับการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="61c60-116">There are many data connectors for Power BI Desktop that require Internet Explorer 10 (or newer) for authentication.</span></span> 


## <a name="data-sources"></a><span data-ttu-id="61c60-117">แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="61c60-117">Data sources</span></span>

<span data-ttu-id="61c60-118">กล่องบทสนทนา **รับข้อมูล** ทำการจัดระเบียบประเภทข้อมูลในหมวดหมู่ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="61c60-118">The **Get Data** dialog box organizes data types in the following categories:</span></span>

* <span data-ttu-id="61c60-119">ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="61c60-119">All</span></span>
* <span data-ttu-id="61c60-120">ไฟล์</span><span class="sxs-lookup"><span data-stu-id="61c60-120">File</span></span>
* <span data-ttu-id="61c60-121">ฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="61c60-121">Database</span></span>
* <span data-ttu-id="61c60-122">Power Platform</span><span class="sxs-lookup"><span data-stu-id="61c60-122">Power Platform</span></span>
* <span data-ttu-id="61c60-123">Azure</span><span class="sxs-lookup"><span data-stu-id="61c60-123">Azure</span></span>
* <span data-ttu-id="61c60-124">บริการออนไลน์</span><span class="sxs-lookup"><span data-stu-id="61c60-124">Online Services</span></span>
* <span data-ttu-id="61c60-125">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="61c60-125">Other</span></span>

<span data-ttu-id="61c60-126">ประเภท **ทั้งหมด** รวมถึงชนิดการเชื่อมต่อข้อมูลทั้งหมดจากประเภททั้งหมด</span><span class="sxs-lookup"><span data-stu-id="61c60-126">The **All** category includes all data connection types from all categories.</span></span>

### <a name="file-data-sources"></a><span data-ttu-id="61c60-127">แหล่งข้อมูลไฟล์</span><span class="sxs-lookup"><span data-stu-id="61c60-127">File data sources</span></span>

<span data-ttu-id="61c60-128">ประเภท **ไฟล์** มีการเชื่อมต่อข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="61c60-128">The **File** category provides the following data connections:</span></span>

* <span data-ttu-id="61c60-129">Excel</span><span class="sxs-lookup"><span data-stu-id="61c60-129">Excel</span></span>
* <span data-ttu-id="61c60-130">ข้อความ/CSV</span><span class="sxs-lookup"><span data-stu-id="61c60-130">Text/CSV</span></span>
* <span data-ttu-id="61c60-131">XML</span><span class="sxs-lookup"><span data-stu-id="61c60-131">XML</span></span>
* <span data-ttu-id="61c60-132">JSON</span><span class="sxs-lookup"><span data-stu-id="61c60-132">JSON</span></span>
* <span data-ttu-id="61c60-133">โฟลเดอร์</span><span class="sxs-lookup"><span data-stu-id="61c60-133">Folder</span></span>
* <span data-ttu-id="61c60-134">PDF</span><span class="sxs-lookup"><span data-stu-id="61c60-134">PDF</span></span>
* <span data-ttu-id="61c60-135">โฟลเดอร์ SharePoint</span><span class="sxs-lookup"><span data-stu-id="61c60-135">SharePoint folder</span></span>

<span data-ttu-id="61c60-136">รูปภาพต่อไปนี้แสดงหน้าต่าง **รับข้อมูล** สำหรับ **ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="61c60-136">The following image shows the **Get Data** window for **File**.</span></span>

![แหล่งข้อมูลไฟล์ กล่องบทสนทนารับข้อมูล Power BI Desktop](media/desktop-data-sources/data-sources-03.png)

### <a name="database-data-sources"></a><span data-ttu-id="61c60-138">แหล่งข้อมูลฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="61c60-138">Database data sources</span></span>

<span data-ttu-id="61c60-139">ประเภท **ฐานข้อมูล** มีการเชื่อมต่อข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="61c60-139">The **Database** category provides the following data connections:</span></span>

* <span data-ttu-id="61c60-140">ฐานข้อมูล SQL Server</span><span class="sxs-lookup"><span data-stu-id="61c60-140">SQL Server database</span></span>
* <span data-ttu-id="61c60-141">ฐานข้อมูล Access</span><span class="sxs-lookup"><span data-stu-id="61c60-141">Access database</span></span>
* <span data-ttu-id="61c60-142">ฐานข้อมูล SQL Server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="61c60-142">SQL Server Analysis Services database</span></span>
* <span data-ttu-id="61c60-143">ฐานข้อมูล Oracle</span><span class="sxs-lookup"><span data-stu-id="61c60-143">Oracle database</span></span>
* <span data-ttu-id="61c60-144">ฐานข้อมูล IBM Db2</span><span class="sxs-lookup"><span data-stu-id="61c60-144">IBM Db2 database</span></span>
* <span data-ttu-id="61c60-145">ฐานข้อมูล IBM Informix</span><span class="sxs-lookup"><span data-stu-id="61c60-145">IBM Informix database (Beta)</span></span>
* <span data-ttu-id="61c60-146">IBM Netezza</span><span class="sxs-lookup"><span data-stu-id="61c60-146">IBM Netezza</span></span>
* <span data-ttu-id="61c60-147">ฐานข้อมูล MySQL</span><span class="sxs-lookup"><span data-stu-id="61c60-147">MySQL database</span></span>
* <span data-ttu-id="61c60-148">ฐานข้อมูล PostgreSQL</span><span class="sxs-lookup"><span data-stu-id="61c60-148">PostgreSQL database</span></span>
* <span data-ttu-id="61c60-149">ฐานข้อมูล Sybase</span><span class="sxs-lookup"><span data-stu-id="61c60-149">Sybase database</span></span>
* <span data-ttu-id="61c60-150">ฐานข้อมูล Teradata</span><span class="sxs-lookup"><span data-stu-id="61c60-150">Teradata database</span></span>
* <span data-ttu-id="61c60-151">ฐานข้อมูล SAP HANA</span><span class="sxs-lookup"><span data-stu-id="61c60-151">SAP HANA database</span></span>
* <span data-ttu-id="61c60-152">เซิร์ฟเวอร์แอปพลิเคชัน SAP Business Warehouse</span><span class="sxs-lookup"><span data-stu-id="61c60-152">SAP Business Warehouse Application Server</span></span>
* <span data-ttu-id="61c60-153">เซิร์ฟเวอร์ข้อความ SAP Business Warehouse</span><span class="sxs-lookup"><span data-stu-id="61c60-153">SAP Business Warehouse Message Server</span></span>
* <span data-ttu-id="61c60-154">Amazon Redshift</span><span class="sxs-lookup"><span data-stu-id="61c60-154">Amazon Redshift</span></span>
* <span data-ttu-id="61c60-155">Impala</span><span class="sxs-lookup"><span data-stu-id="61c60-155">Impala</span></span>
* <span data-ttu-id="61c60-156">Google BigQuery</span><span class="sxs-lookup"><span data-stu-id="61c60-156">Google BigQuery</span></span>
* <span data-ttu-id="61c60-157">Vertica</span><span class="sxs-lookup"><span data-stu-id="61c60-157">Vertica</span></span>
* <span data-ttu-id="61c60-158">Snowflake</span><span class="sxs-lookup"><span data-stu-id="61c60-158">Snowflake</span></span>
* <span data-ttu-id="61c60-159">Essbase</span><span class="sxs-lookup"><span data-stu-id="61c60-159">Essbase</span></span>
* <span data-ttu-id="61c60-160">คิวบ์ AtScale</span><span class="sxs-lookup"><span data-stu-id="61c60-160">AtScale cubes</span></span>
* <span data-ttu-id="61c60-161">Data Virtuality LDW (Beta)</span><span class="sxs-lookup"><span data-stu-id="61c60-161">Data Virtuality LDW (Beta)</span></span>
* <span data-ttu-id="61c60-162">Denodo</span><span class="sxs-lookup"><span data-stu-id="61c60-162">Denodo</span></span>
* <span data-ttu-id="61c60-163">Dremio</span><span class="sxs-lookup"><span data-stu-id="61c60-163">Dremio</span></span>
* <span data-ttu-id="61c60-164">Exasol</span><span class="sxs-lookup"><span data-stu-id="61c60-164">Exasol</span></span>
* <span data-ttu-id="61c60-165">Indexima</span><span class="sxs-lookup"><span data-stu-id="61c60-165">Indexima</span></span>
* <span data-ttu-id="61c60-166">InterSystems IRIS (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-166">InterSystems IRIS (Beta)</span></span>
* <span data-ttu-id="61c60-167">Jethro (รุ่นเบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-167">Jethro (Beta)</span></span>
* <span data-ttu-id="61c60-168">Kyligence</span><span class="sxs-lookup"><span data-stu-id="61c60-168">Kyligence</span></span>
* <span data-ttu-id="61c60-169">Linkar PICK Style / MultiValue Databases (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-169">Linkar PICK Style / MultiValue Databases (Beta)</span></span>
* <span data-ttu-id="61c60-170">MariaDB (Beta)</span><span class="sxs-lookup"><span data-stu-id="61c60-170">MariaDB (Beta)</span></span>
* <span data-ttu-id="61c60-171">MarkLogic</span><span class="sxs-lookup"><span data-stu-id="61c60-171">MarkLogic</span></span>
* <span data-ttu-id="61c60-172">BI Connector</span><span class="sxs-lookup"><span data-stu-id="61c60-172">BI Connector</span></span>
* <span data-ttu-id="61c60-173">Actian (รุ่นเบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-173">Actian (Beta)</span></span>

> [!NOTE]
> <span data-ttu-id="61c60-174">ตัวเชื่อมต่อฐานข้อมูลบางอย่างจำเป็นต้องให้คุณเปิดใช้งานโดยการเลือก **ไฟล์ > ตัวเลือกและการตั้งค่า > ตัวเลือก** จากนั้นเลือก **คุณลักษณะการแสดงตัวอย่าง** และเปิดใช้งานตัวเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="61c60-174">Some database connectors require that you enable them by selecting **File > Options and settings > Options** then selecting **Preview Features** and enabling the connector.</span></span> <span data-ttu-id="61c60-175">ถ้าคุณไม่เห็นตัวเชื่อมต่อที่กล่าวถึงด้านบน และต้องการใช้งานตัวเชื่อมต่อเหล่านั้น โปรดตรวจสอบการตั้งค่าของ **คุณลักษณะการแสดงตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="61c60-175">If you don't see some of the connectors mentioned above and want to use them, check your **Preview Features** settings.</span></span> <span data-ttu-id="61c60-176">และโปรดทราบว่าแหล่งข้อมูลใด ๆ ที่ได้รับการทำเครื่องหมายเป็น *เบต้า* หรือ *แสดงตัวอย่าง* มีการจำกัดการสนับสนุนและฟังก์ชันการทำงาน และไม่ควรใช้ในสภาพแวดล้อมการผลิต</span><span class="sxs-lookup"><span data-stu-id="61c60-176">Also note that any data source marked as *Beta* or *Preview* has limited support and functionality, and should not be used in production environments.</span></span>

<span data-ttu-id="61c60-177">รูปภาพต่อไปนี้แสดงหน้าต่าง **รับข้อมูล** สำหรับ **ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="61c60-177">The following image shows the **Get Data** window for **Database**.</span></span>

![แหล่งข้อมูลฐานข้อมูล กล่องบทสนทนารับข้อมูล Power BI Desktop](media/desktop-data-sources/data-sources-04.png)

### <a name="power-platform-data-sources"></a><span data-ttu-id="61c60-179">แหล่งข้อมูล Power Platform</span><span class="sxs-lookup"><span data-stu-id="61c60-179">Power Platform data sources</span></span>

<span data-ttu-id="61c60-180">ประเภท **Power Platform** มีการเชื่อมต่อข้อมูลดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="61c60-180">The **Power Platform** category provides the following data connections:</span></span>

* <span data-ttu-id="61c60-181">ชุดข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="61c60-181">Power BI datasets</span></span>
* <span data-ttu-id="61c60-182">กระแสข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="61c60-182">Power BI dataflows</span></span>
* <span data-ttu-id="61c60-183">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="61c60-183">Microsoft Dataverse</span></span>
* <span data-ttu-id="61c60-184">กระแสข้อมูล Power Platform (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-184">Power Platform dataflows (Beta)</span></span>

<span data-ttu-id="61c60-185">รูปภาพต่อไปนี้แสดงหน้าต่าง **รับข้อมูล** สำหรับ **Power Platform**</span><span class="sxs-lookup"><span data-stu-id="61c60-185">The following image shows the **Get Data** window for **Power Platform**.</span></span>

![แหล่งข้อมูล Power Platform กล่องบทสนทนารับข้อมูล Power BI Desktop](media/desktop-data-sources/data-sources-05.png)

### <a name="azure-data-sources"></a><span data-ttu-id="61c60-187">แหล่งข้อมูล Azure</span><span class="sxs-lookup"><span data-stu-id="61c60-187">Azure data sources</span></span>

<span data-ttu-id="61c60-188">ประเภท **Azure** มีการเชื่อมต่อข้อมูลดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="61c60-188">The **Azure** category provides the following data connections:</span></span>

* <span data-ttu-id="61c60-189">ฐานข้อมูล Azure SQL</span><span class="sxs-lookup"><span data-stu-id="61c60-189">Azure SQL Database</span></span>
* <span data-ttu-id="61c60-190">Azure Synapse Analytics (SQL DW)</span><span class="sxs-lookup"><span data-stu-id="61c60-190">Azure Synapse Analytics (SQL DW)</span></span>
* <span data-ttu-id="61c60-191">ฐานข้อมูล Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="61c60-191">Azure Analysis Services database</span></span>
* <span data-ttu-id="61c60-192">ฐานข้อมูล Azure สำหรับ PostgreSQL</span><span class="sxs-lookup"><span data-stu-id="61c60-192">Azure Database for PostgreSQL</span></span>
* <span data-ttu-id="61c60-193">พื้นที่เก็บข้อมูล Azure Blob</span><span class="sxs-lookup"><span data-stu-id="61c60-193">Azure Blob Storage</span></span>
* <span data-ttu-id="61c60-194">พื้นที่เก็บข้อมูล Azure Table</span><span class="sxs-lookup"><span data-stu-id="61c60-194">Azure Table Storage</span></span>
* <span data-ttu-id="61c60-195">Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="61c60-195">Azure Cosmos DB</span></span>
* <span data-ttu-id="61c60-196">Azure Data Explorer (Kusto)</span><span class="sxs-lookup"><span data-stu-id="61c60-196">Azure Data Explorer (Kusto)</span></span>
* <span data-ttu-id="61c60-197">Azure Data Lake Storage Gen2</span><span class="sxs-lookup"><span data-stu-id="61c60-197">Azure Data Lake Storage Gen2</span></span>
* <span data-ttu-id="61c60-198">Azure Data Lake Storage Gen1</span><span class="sxs-lookup"><span data-stu-id="61c60-198">Azure Data Lake Storage Gen1</span></span>
* <span data-ttu-id="61c60-199">Azure HDInsight (HDFS)</span><span class="sxs-lookup"><span data-stu-id="61c60-199">Azure HDInsight (HDFS)</span></span>
* <span data-ttu-id="61c60-200">Azure HDInsight Spark</span><span class="sxs-lookup"><span data-stu-id="61c60-200">Azure HDInsight Spark</span></span>
* <span data-ttu-id="61c60-201">HDInsight Interactive Query</span><span class="sxs-lookup"><span data-stu-id="61c60-201">HDInsight Interactive Query</span></span>
* <span data-ttu-id="61c60-202">Azure Cost Management</span><span class="sxs-lookup"><span data-stu-id="61c60-202">Azure Cost Management</span></span>
* <span data-ttu-id="61c60-203">Azure Databricks</span><span class="sxs-lookup"><span data-stu-id="61c60-203">Azure Databricks</span></span>
* <span data-ttu-id="61c60-204">Azure Time Series Insights (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-204">Azure Time Series Insights (Beta)</span></span>


<span data-ttu-id="61c60-205">แสดงรูปภาพต่อไปนี้ **รับข้อมูล** สำหรับ **Azure**</span><span class="sxs-lookup"><span data-stu-id="61c60-205">The following image shows the **Get Data** window for **Azure**.</span></span>

![แหล่งข้อมูล Azure กล่องบทสนทนารับข้อมูล Power BI Desktop](media/desktop-data-sources/data-sources-06.png)

### <a name="online-services-data-sources"></a><span data-ttu-id="61c60-207">แหล่งข้อมูลการบริการออนไลน์</span><span class="sxs-lookup"><span data-stu-id="61c60-207">Online Services data sources</span></span>

<span data-ttu-id="61c60-208">ประเภท **บริการออนไลน์** มีการเชื่อมต่อข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="61c60-208">The **Online Services** category provides the following data connections:</span></span>

* <span data-ttu-id="61c60-209">รายการ SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="61c60-209">SharePoint Online List</span></span>
* <span data-ttu-id="61c60-210">Microsoft Exchange Online</span><span class="sxs-lookup"><span data-stu-id="61c60-210">Microsoft Exchange Online</span></span>
* <span data-ttu-id="61c60-211">Dynamics 365 (ออนไลน์)</span><span class="sxs-lookup"><span data-stu-id="61c60-211">Dynamics 365 (online)</span></span>
* <span data-ttu-id="61c60-212">Dynamics NAV</span><span class="sxs-lookup"><span data-stu-id="61c60-212">Dynamics NAV</span></span>
* <span data-ttu-id="61c60-213">Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="61c60-213">Dynamics 365 Business Central</span></span>
* <span data-ttu-id="61c60-214">Dynamics 365 Business Central (ภายในองค์กร)</span><span class="sxs-lookup"><span data-stu-id="61c60-214">Dynamics 365 Business Central (on-premises)</span></span>
* <span data-ttu-id="61c60-215">Microsoft Azure Consumption Insights (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-215">Microsoft Azure Consumption Insights (Beta)</span></span>
* <span data-ttu-id="61c60-216">Azure DevOps (เฉพาะบอร์ดเท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="61c60-216">Azure DevOps (Boards only)</span></span>
* <span data-ttu-id="61c60-217">Azure DevOps Server (เฉพาะบอร์ดเท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="61c60-217">Azure DevOps Server (Boards only)</span></span>
* <span data-ttu-id="61c60-218">ออบเจ็กต์ Salesforce</span><span class="sxs-lookup"><span data-stu-id="61c60-218">Salesforce Objects</span></span>
* <span data-ttu-id="61c60-219">รายงาน Salesforce</span><span class="sxs-lookup"><span data-stu-id="61c60-219">Salesforce Reports</span></span>
* <span data-ttu-id="61c60-220">Google Analytics</span><span class="sxs-lookup"><span data-stu-id="61c60-220">Google Analytics</span></span>
* <span data-ttu-id="61c60-221">Adobe Analytics</span><span class="sxs-lookup"><span data-stu-id="61c60-221">Adobe Analytics</span></span>
* <span data-ttu-id="61c60-222">appFigures (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-222">appFigures (Beta)</span></span>
* <span data-ttu-id="61c60-223">Data.World - รับชุดข้อมูล (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-223">Data.World - Get Dataset (Beta)</span></span>
* <span data-ttu-id="61c60-224">GitHub (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-224">GitHub (Beta)</span></span>
* <span data-ttu-id="61c60-225">ผู้นำทางการขาย LinkedIn (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-225">LinkedIn Sales Navigator (Beta)</span></span>
* <span data-ttu-id="61c60-226">Marketo (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-226">Marketo (Beta)</span></span>
* <span data-ttu-id="61c60-227">Mixpanel (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-227">Mixpanel (Beta)</span></span>
* <span data-ttu-id="61c60-228">Planview Enterprise One - PRM (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-228">Planview Enterprise One - PRM (Beta)</span></span>
* <span data-ttu-id="61c60-229">QuickBooks Online (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-229">QuickBooks Online (Beta)</span></span>
* <span data-ttu-id="61c60-230">Smartsheet</span><span class="sxs-lookup"><span data-stu-id="61c60-230">Smartsheet</span></span>
* <span data-ttu-id="61c60-231">SparkPost (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-231">SparkPost (Beta)</span></span>
* <span data-ttu-id="61c60-232">SweetIQ (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-232">SweetIQ (Beta)</span></span>
* <span data-ttu-id="61c60-233">Planview Enterprise One - CTM (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-233">Planview Enterprise One - CTM (Beta)</span></span>
* <span data-ttu-id="61c60-234">Twilio (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-234">Twilio (Beta)</span></span>
* <span data-ttu-id="61c60-235">Zendesk (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-235">Zendesk (Beta)</span></span>
* <span data-ttu-id="61c60-236">Asana (Beta)</span><span class="sxs-lookup"><span data-stu-id="61c60-236">Asana (Beta)</span></span>
* <span data-ttu-id="61c60-237">Dynamics 365 Customer Insights (Beta)</span><span class="sxs-lookup"><span data-stu-id="61c60-237">Dynamics 365 Customer Insights (Beta)</span></span>
* <span data-ttu-id="61c60-238">แหล่งข้อมูล Emigo</span><span class="sxs-lookup"><span data-stu-id="61c60-238">Emigo Data Source</span></span>
* <span data-ttu-id="61c60-239">Entersoft Business Suite (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-239">Entersoft Business Suite (Beta)</span></span>
* <span data-ttu-id="61c60-240">การวิเคราะห์ FactSet</span><span class="sxs-lookup"><span data-stu-id="61c60-240">FactSet Analytics</span></span>
* <span data-ttu-id="61c60-241">กระบวนการหลอม Palantir</span><span class="sxs-lookup"><span data-stu-id="61c60-241">Palantir Foundry</span></span>
* <span data-ttu-id="61c60-242">Industrial App Store</span><span class="sxs-lookup"><span data-stu-id="61c60-242">Industrial App Store</span></span>
* <span data-ttu-id="61c60-243">คลังข้อมูล Intune (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-243">Intune Data Warehouse (Beta)</span></span>
* <span data-ttu-id="61c60-244">การรักษาความปลอดภัยของ Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="61c60-244">Microsoft Graph Security (Beta)</span></span>
* <span data-ttu-id="61c60-245">Projectplace สำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="61c60-245">Projectplace for Power BI</span></span>
* <span data-ttu-id="61c60-246">ความเข้าใจผลิตภัณฑ์ (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-246">Product Insights (beta)</span></span>
* <span data-ttu-id="61c60-247">Quick Base</span><span class="sxs-lookup"><span data-stu-id="61c60-247">Quick Base</span></span>
* <span data-ttu-id="61c60-248">Spigit (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-248">Spigit (Beta)</span></span>
* <span data-ttu-id="61c60-249">TeamDesk (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-249">TeamDesk (Beta)</span></span>
* <span data-ttu-id="61c60-250">การวิเคราะห์ Webtrends (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-250">Webtrends Analytics (Beta)</span></span>
* <span data-ttu-id="61c60-251">Witivio (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-251">Witivio (Beta)</span></span>
* <span data-ttu-id="61c60-252">การวิเคราะห์สถานที่ทำงาน (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-252">Workplace Analytics (Beta)</span></span>
* <span data-ttu-id="61c60-253">Zoho Creator (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-253">Zoho Creator (Beta)</span></span>
* <span data-ttu-id="61c60-254">eWay-CRM (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-254">eWay-CRM (Beta)</span></span>
* <span data-ttu-id="61c60-255">Hexagon PPM Smart API</span><span class="sxs-lookup"><span data-stu-id="61c60-255">Hexagon PPM Smart API</span></span>


<span data-ttu-id="61c60-256">รูปภาพต่อไปนี้แสดงหน้าต่าง **รับข้อมูล** สำหรับ **บริการออนไลน์**</span><span class="sxs-lookup"><span data-stu-id="61c60-256">The following image shows the **Get Data** window for **Online Services**.</span></span>

![แหล่งข้อมูลการบริการออนไลน์ กล่องบทสนทนารับข้อมูล  Power BI Desktop](media/desktop-data-sources/data-sources-07.png)

### <a name="other-data-sources"></a><span data-ttu-id="61c60-258">แหล่งข้อมูลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="61c60-258">Other data sources</span></span>

<span data-ttu-id="61c60-259">ประเภท **อื่น ๆ** มีการเชื่อมต่อข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="61c60-259">The **Other** category provides the following data connections:</span></span>

* <span data-ttu-id="61c60-260">เว็บ</span><span class="sxs-lookup"><span data-stu-id="61c60-260">Web</span></span>
* <span data-ttu-id="61c60-261">รายการ SharePoint</span><span class="sxs-lookup"><span data-stu-id="61c60-261">SharePoint list</span></span>
* <span data-ttu-id="61c60-262">ตัวดึงข้อมูล OData</span><span class="sxs-lookup"><span data-stu-id="61c60-262">OData Feed</span></span>
* <span data-ttu-id="61c60-263">Active Directory</span><span class="sxs-lookup"><span data-stu-id="61c60-263">Active Directory</span></span>
* <span data-ttu-id="61c60-264">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="61c60-264">Microsoft Exchange</span></span>
* <span data-ttu-id="61c60-265">ไฟล์ Hadoop (HDFS)</span><span class="sxs-lookup"><span data-stu-id="61c60-265">Hadoop File (HDFS)</span></span>
* <span data-ttu-id="61c60-266">Spark</span><span class="sxs-lookup"><span data-stu-id="61c60-266">Spark</span></span>
* <span data-ttu-id="61c60-267">Hive LLAP</span><span class="sxs-lookup"><span data-stu-id="61c60-267">Hive LLAP</span></span>
* <span data-ttu-id="61c60-268">สคริปต์ R</span><span class="sxs-lookup"><span data-stu-id="61c60-268">R script</span></span>
* <span data-ttu-id="61c60-269">สคริปต์ Python</span><span class="sxs-lookup"><span data-stu-id="61c60-269">Python script</span></span>
* <span data-ttu-id="61c60-270">ODBC</span><span class="sxs-lookup"><span data-stu-id="61c60-270">ODBC</span></span>
* <span data-ttu-id="61c60-271">OLE DB</span><span class="sxs-lookup"><span data-stu-id="61c60-271">OLE DB</span></span>
* <span data-ttu-id="61c60-272">Acterys : การวางแผน & แบบจำลองอัตโนมัติ (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-272">Acterys : Model Automation & Planning (Beta)</span></span>
* <span data-ttu-id="61c60-273">ระบบอัตโนมัติที่ใดก็ได้ (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-273">Automation Anywhere (Beta)</span></span>
* <span data-ttu-id="61c60-274">Solver</span><span class="sxs-lookup"><span data-stu-id="61c60-274">Solver</span></span>
* <span data-ttu-id="61c60-275">Cherwell (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-275">Cherwell (Beta)</span></span>
* <span data-ttu-id="61c60-276">การรวมข้อมูล Cognite</span><span class="sxs-lookup"><span data-stu-id="61c60-276">Cognite Data Fusion</span></span>
* <span data-ttu-id="61c60-277">FHIR</span><span class="sxs-lookup"><span data-stu-id="61c60-277">FHIR</span></span>
* <span data-ttu-id="61c60-278">เส้นตารางข้อมูล (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-278">Information Grid (Beta)</span></span>
* <span data-ttu-id="61c60-279">Jamf Pro (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-279">Jamf Pro (Beta)</span></span>
* <span data-ttu-id="61c60-280">MicroStrategy สำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="61c60-280">MicroStrategy for Power BI</span></span>
* <span data-ttu-id="61c60-281">Paxata</span><span class="sxs-lookup"><span data-stu-id="61c60-281">Paxata</span></span>
* <span data-ttu-id="61c60-282">QubolePresto (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-282">QubolePresto (Beta)</span></span>
* <span data-ttu-id="61c60-283">Roamler (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-283">Roamler (Beta)</span></span>
* <span data-ttu-id="61c60-284">ทางลัดข้อมูลเชิงลึกทางธุรกิจ (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-284">Shortcuts Business Insights (Beta)</span></span>
* <span data-ttu-id="61c60-285">Siteimprove</span><span class="sxs-lookup"><span data-stu-id="61c60-285">Siteimprove</span></span>
* <span data-ttu-id="61c60-286">SurveyMonkey(เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-286">SurveyMonkey (Beta)</span></span>
* <span data-ttu-id="61c60-287">รายการ Tenforce (สมาร์ท)</span><span class="sxs-lookup"><span data-stu-id="61c60-287">Tenforce (Smart)List</span></span>
* <span data-ttu-id="61c60-288">TIBCO(R) Data Virtualization (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-288">TIBCO(R) Data Virtualization (Beta)</span></span>
* <span data-ttu-id="61c60-289">Vena (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-289">Vena (Beta)</span></span>
* <span data-ttu-id="61c60-290">ข้อมูลเชิงลึก Vessel (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-290">Vessel Insight (Beta)</span></span>
* <span data-ttu-id="61c60-291">Zucchetti HR Infinity (เบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-291">Zucchetti HR Infinity (Beta)</span></span>
* <span data-ttu-id="61c60-292">Anaplan Connector v1.0 (รุ่นเบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-292">Anaplan Connector v1.0 (Beta)</span></span>
* <span data-ttu-id="61c60-293">Starburst Enterprise Presto (รุ่นเบต้า)</span><span class="sxs-lookup"><span data-stu-id="61c60-293">Starburst Enterprise Presto (Beta)</span></span>
* <span data-ttu-id="61c60-294">คิวรีที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="61c60-294">Blank Query</span></span>



<span data-ttu-id="61c60-295">รูปภาพต่อไปนี้แสดงหน้าต่าง **รับข้อมูล** สำหรับ **อื่น ๆ**</span><span class="sxs-lookup"><span data-stu-id="61c60-295">The following image shows the **Get Data** window for **Other**.</span></span>

![แหล่งข้อมูลอื่นใน Power BI Desktop](media/desktop-data-sources/data-sources-08.png)

> [!NOTE]
> <span data-ttu-id="61c60-297">ในขณะนี้คุณไม่สามารถเชื่อมต่อกับแหล่งข้อมูลแบบกำหนดเองที่รักษาความปลอดภัยโดยใช้ Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="61c60-297">At this time, it's not possible to connect to custom data sources secured using Azure Active Directory.</span></span>

### <a name="template-apps"></a><span data-ttu-id="61c60-298">แอปแม่แบบ</span><span class="sxs-lookup"><span data-stu-id="61c60-298">Template apps</span></span>

<span data-ttu-id="61c60-299">คุณสามารถค้นหาแอปเทมเพลตสำหรับองค์กรของคุณได้โดยเลือกลิงก์ **เแอปเทมเพลต** ใกล้ด้านล่างของหน้าต่าง **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="61c60-299">You can find template apps for your organization by selecting the **Template Apps** link near the bottom of the **Get Data** window.</span></span> 

![กล่องโต้ตอบรับข้อมูลสำหรับแหล่งข้อมูลอื่นใน Power BI Desktop](media/desktop-data-sources/data-sources-12.png)

<span data-ttu-id="61c60-301">แอปเทมเพลตที่มีให้ใช้งานอาจแตกต่างกันไปตามองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="61c60-301">Available Template Apps may vary based on your organization.</span></span>

## <a name="connecting-to-a-data-source"></a><span data-ttu-id="61c60-302">เชื่อมต่อกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="61c60-302">Connecting to a data source</span></span>

<span data-ttu-id="61c60-303">เลือกแหล่งข้อมูลจากหน้าต่าง **รับข้อมูล** และเลือก **เชื่อมต่อ** เพื่อเชื่อมต่อกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="61c60-303">To connect to a data source, select the data source from the **Get Data** window and select **Connect**.</span></span> <span data-ttu-id="61c60-304">ในรูปต่อไปนี้ **เว็บ** ได้รับการเลือกจากประเภทการเชื่อมต่อข้อมูล **อื่น ๆ**</span><span class="sxs-lookup"><span data-stu-id="61c60-304">In the following image, **Web** is selected from the **Other** data connection category.</span></span>

![เชื่อมต่อไปยังเว็ป กล่องบทสนทนารับข้อมูล Power BI Desktop](media/desktop-data-sources/data-sources-08.png)

<span data-ttu-id="61c60-306">หน้าต่างการเชื่อมต่อจะแสดงขึ้นตามชนิดของการเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="61c60-306">A connection window is displayed, specific to the type of data connection.</span></span> <span data-ttu-id="61c60-307">คุณจะได้รับพร้อมท์เพื่อแจ้งให้ป้อนข้อมูลประจำตัว หากจำเป็นต้องใช้</span><span class="sxs-lookup"><span data-stu-id="61c60-307">If credentials are required, you’ll be prompted to provide them.</span></span> <span data-ttu-id="61c60-308">รูปต่อไปนี้แสดง URL ที่ป้อนเพื่อเชื่อมต่อกับแหล่งข้อมูลเว็บ</span><span class="sxs-lookup"><span data-stu-id="61c60-308">The following image shows a URL being entered to connect to a Web data source.</span></span>

![ป้อน URL จากกล่องบทสนทนาเว็ป Power BI Desktop](media/desktop-data-sources/datasources-fromwebbox.png)

<span data-ttu-id="61c60-310">ป้อน URL หรือข้อมูลการเชื่อมต่อแหล่ง จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="61c60-310">Enter the URL or resource connection information, and then select **OK**.</span></span> <span data-ttu-id="61c60-311">Power BI Desktop ทำการเชื่อมต่อไปยังแหล่งข้อมูล และแสดงแหล่งข้อมูลที่ใช้ได้ใน **ผู้นำทาง**.</span><span class="sxs-lookup"><span data-stu-id="61c60-311">Power BI Desktop makes the connection to the data source, and it presents the available data sources in the **Navigator**.</span></span>

![กล่องบทสนทนาผู้นำทาง Power BI Desktop](media/desktop-data-sources/datasources-fromnavigatordialog.png)

<span data-ttu-id="61c60-313">ในการโหลดข้อมูล เลือกปุ่ม **โหลด** ที่ปุ่มของแผง **ผู้นำทาง**</span><span class="sxs-lookup"><span data-stu-id="61c60-313">To load the data, select the **Load** button at the bottom of the **Navigator** pane.</span></span> <span data-ttu-id="61c60-314">ในการแปลงหรือแก้ไขคำถามใน Power Query Editor ก่อนการโหลดข้อมูล เลือกปุ่ม **แปลงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="61c60-314">To transform or edit the query in Power Query Editor before loading the data, select the **Transform Data** button.</span></span>

<span data-ttu-id="61c60-315">นั่นคือทั้งหมดของการเชื่อมต่อกับแหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="61c60-315">That’s all there is to connecting to data sources in Power BI Desktop!</span></span> <span data-ttu-id="61c60-316">ลองเชื่อมต่อกับข้อมูลจากรายการของแหล่งข้อมูลที่เรากำลังพัฒนา และกลับมาตรวจสอบบ่อยๆ - เราจะดำเนินการเพื่อเพิ่มลงในรายการนี้อยู่ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="61c60-316">Try connecting to data from our growing list of data sources, and check back often - we continue to add to this list all the time.</span></span>

## <a name="using-pbids-files-to-get-data"></a><span data-ttu-id="61c60-317">การใช้ไฟล์ PBIDS เพื่อรับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="61c60-317">Using PBIDS files to get data</span></span>

<span data-ttu-id="61c60-318">ไฟล์ PBIDS คือไฟล์ Power BI Desktop ที่จะมีโครงสร้างเฉพาะและยังมีส่วนขยาย .PBIDS ที่ระบุว่าตือไฟล์แหล่งข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="61c60-318">PBIDS files are Power BI Desktop files that have a specific structure, and they have a .PBIDS extension to identify it is a Power BI data source file.</span></span>

<span data-ttu-id="61c60-319">คุณสามารถสร้างไฟล์ PBIDS เพื่อปรับปรุงประสบการณ์ในการ **รับข้อมูล** สำหรับผู้สร้างรายงานมือใหม่หรือผู้เริ่มต้นในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="61c60-319">You can create a PBIDS file to streamline the **Get Data** experience for new or beginner report creators in your organization.</span></span> <span data-ttu-id="61c60-320">หากคุณสร้างไฟล์ PBIDS จากรายงานที่มีอยู่การเริ่มต้นผู้เขียนรายงานจะสร้างรายงานใหม่จากข้อมูลเดียวกันได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="61c60-320">If you create the PBIDS file from existing reports, it's easier for beginning report authors to build new reports from the same data.</span></span>

<span data-ttu-id="61c60-321">เมื่อผู้เขียนเปิดไฟล์ PBIDS Power BI Desktop เปิดและพร้อมใช้สำหรับผู้ใช้สำหรับการอ้างอิงไปยังการรับรองและเชื่อมต่อไปยังแหล่งข้อมูลที่ถูกระบุในไฟล์</span><span class="sxs-lookup"><span data-stu-id="61c60-321">When an author opens a PBIDS file, Power BI Desktop opens and prompts the user for credentials to authenticate and connect to the data source that's specified in the file.</span></span> <span data-ttu-id="61c60-322">กล่องบทสนทนา **ผู้นำทาง** ปรากฏและผู้ใช้ต้องเลือกตารางจากแหล่งข้อมูลนั้นเพื่อโหลดไปในโมเดล</span><span class="sxs-lookup"><span data-stu-id="61c60-322">The **Navigation** dialog box appears, and the user must select the tables from that data source to load into the model.</span></span> <span data-ttu-id="61c60-323">ผู้ใช้อาจต้องเลือกฐานข้อมูลและโหมดการเชื่อมต่อหากไม่มีการระบุไว้ในไฟล์ PBIDS</span><span class="sxs-lookup"><span data-stu-id="61c60-323">Users may also need to select the database(s) and connection mode if none was specified in the PBIDS file.</span></span>

<span data-ttu-id="61c60-324">จากจุดข้างหน้า ผู้ใช้สามารถเริ่มการสร้างการแสดงผลด้วยภาพหรือเลือก **แหล่งปัจจุบัน** เพื่อโหลดเซตใหม่ของตารางไปในโมเดล</span><span class="sxs-lookup"><span data-stu-id="61c60-324">From that point forward, the user can begin building visualizations or select **Recent Sources** to load a new set of tables into the model.</span></span>

<span data-ttu-id="61c60-325">ปัจจุบัน ไฟล์ PBIDS สนับสนุนเพียงแหล่งข้อมูลเดี่ยวในไฟล์เดียว</span><span class="sxs-lookup"><span data-stu-id="61c60-325">Currently, PBIDS files only support a single data source in one file.</span></span> <span data-ttu-id="61c60-326">การระบุแหล่งข้อมูลมากกว่าหนึ่งผลลัพธ์ในข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="61c60-326">Specifying more than one data source results in an error.</span></span>


### <a name="how-to-create-a-pbids-connection-file"></a><span data-ttu-id="61c60-327">วิธีสร้างไฟล์การเชื่อมต่อ PBIDS</span><span class="sxs-lookup"><span data-stu-id="61c60-327">How to create a PBIDS connection file</span></span>

<span data-ttu-id="61c60-328">ถ้าคุณมีไฟล์ Power BI Desktop (.PBIX) ที่เชื่อมต่อกับข้อมูลที่คุณสนใจอยู่แล้ว คุณสามารถส่งออกไฟล์การเชื่อมต่อเหล่านี้จากภายใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="61c60-328">If you have an existing Power BI Desktop (.PBIX) file that's already connected to the data you’re interested in, you can simply export these connection files from within Power BI Desktop.</span></span> <span data-ttu-id="61c60-329">นี่เป็นวิธีที่แนะนำเนื่องจากไฟล์ PBIDS สามารถสร้างขึ้นโดยอัตโนมัติจากเดสก์ท็อป</span><span class="sxs-lookup"><span data-stu-id="61c60-329">This is the recommended method, since the PBIDS file can be auto-generated from Desktop.</span></span> <span data-ttu-id="61c60-330">นอกจากนี้คุณยังสามารถแก้ไขหรือสร้างไฟล์ด้วยตนเองในโปรแกรมแก้ไขข้อความ</span><span class="sxs-lookup"><span data-stu-id="61c60-330">In addition, you can still edit or manually create the file in a text editor.</span></span> 

<span data-ttu-id="61c60-331">ในการสร้างไฟล์ PBIDS ให้เลือก **ไฟล์> ตัวเลือกและการตั้งค่า> การตั้งค่าแหล่งข้อมูล**:</span><span class="sxs-lookup"><span data-stu-id="61c60-331">To create the PBIDS file, select **File > Options and settings > Data source settings**:</span></span>

![ตัวเลือกเมนูการตั้งค่าแหล่งข้อมูล](media/desktop-data-sources/data-sources-09.png)

<span data-ttu-id="61c60-333">ในกล่องโต้ตอบที่ปรากฏขึ้นให้เลือกแหล่งข้อมูลที่คุณต้องการส่งออกเป็น PBIDS จากนั้นเลือก **ส่งออก PBIDS**</span><span class="sxs-lookup"><span data-stu-id="61c60-333">In the dialog that appears, select the data source you want to export as a PBIDS, and then select **Export PBIDS**.</span></span>

![กล่องโต้ตอบการตั้งค่าแหล่งข้อมูล](media/desktop-data-sources/data-sources-10.png)

<span data-ttu-id="61c60-335">เมื่อคุณเลือกปุ่ม **ส่งออก PBIDS** Power BI Desktop จะสร้างไฟล์ PBIDS ซึ่งคุณสามารถเปลี่ยนชื่อและบันทึกในไดเรกทอรีของคุณและแชร์กับผู้อื่นได้</span><span class="sxs-lookup"><span data-stu-id="61c60-335">When you select the **Export PBIDS** button, Power BI Desktop generates the PBIDS file, which you can rename and save in your directory, and share with others.</span></span> <span data-ttu-id="61c60-336">คุณยังสามารถเปิดไฟล์ในโปรแกรมแก้ไขข้อความและแก้ไขไฟล์เพิ่มเติมรวมถึงการระบุโหมดการเชื่อมต่อในไฟล์ดังที่แสดงในภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="61c60-336">You can also open the file in a text editor, and modify the file further, including specifying the mode of connection in the file itself, as shown in the following image.</span></span> 

![ใช้เครื่องมือแก้ไขข้อความเพื่อแก้ไขไฟล์ PBIDS](media/desktop-data-sources/data-sources-11.png)

<span data-ttu-id="61c60-338">หากคุณต้องการสร้างไฟล์ PBIDS ด้วยตนเองในโปรแกรมแก้ไขข้อความคุณต้องระบุอินพุตที่จำเป็นสำหรับการเชื่อมต่อเดียวและบันทึกไฟล์ด้วยส่วนขยาย PBIDS</span><span class="sxs-lookup"><span data-stu-id="61c60-338">If you prefer to manually create your PBIDS files in a text editor, you must specify the required inputs for a single connection and save the file with the PBIDS extension.</span></span> <span data-ttu-id="61c60-339">คุณยังสามารถระบุโหมดการเชื่อมต่อเป็น DirectQuery หรือ นำเข้า</span><span class="sxs-lookup"><span data-stu-id="61c60-339">Optionally, you can also specify the connection mode as either DirectQuery or Import.</span></span> <span data-ttu-id="61c60-340">หาก **โหมด** ไม่พบ/ว่างในไฟล์ ผู้ใช้ที่เปิดไฟล์ใน Power BI Desktop ที่พร้อมใช้ให้เลือก **DirectQuery** หรือ **การนำเข้า**</span><span class="sxs-lookup"><span data-stu-id="61c60-340">If **mode** is missing/null in the file, the user who opens the file in Power BI Desktop is prompted to select **DirectQuery** or **Import**.</span></span>


### <a name="pbids-file-examples"></a><span data-ttu-id="61c60-341">ตัวอย่างไฟล์ PBIDS</span><span class="sxs-lookup"><span data-stu-id="61c60-341">PBIDS file examples</span></span>

<span data-ttu-id="61c60-342">ส่วนนี้แสดงตัวอย่างจากแหล่งข้อมูลที่ใช้กันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="61c60-342">This section provides some examples from commonly used data sources.</span></span> <span data-ttu-id="61c60-343">ประเภทไฟล์ PBIDS รองรับเฉพาะการเชื่อมต่อข้อมูลที่ได้รับการสนับสนุนใน Power BI Desktop โดยมีข้อยกเว้นต่อไปนี้: Wiki URLS, Live Connect และ Blank Query</span><span class="sxs-lookup"><span data-stu-id="61c60-343">The PBIDS file type only supports data connections that are also supported in Power BI Desktop, with the following exceptions: Wiki URLS, Live Connect and Blank Query.</span></span>

<span data-ttu-id="61c60-344">ไฟล์ PBIDS *ไม่ได้* รวมกับข้อมูลที่พิสูจน์จริงและตารางและข้อมูลเค้าร่าง</span><span class="sxs-lookup"><span data-stu-id="61c60-344">The PBIDS file *doesn't* include authentication information and table and schema information.</span></span>  

<span data-ttu-id="61c60-345">โค้ดต่างๆ ต่อไปนี้แสดงตัวอย่างทั่วไปที่หลากหลายสำหรับไฟล์ PBIDS แต่ไม่สามารถทำให้สำเร็จหรือครอบคลุมได้</span><span class="sxs-lookup"><span data-stu-id="61c60-345">The following code snippets show several common examples for PBIDS files, but they aren't complete or comprehensive.</span></span> <span data-ttu-id="61c60-346">สำหรับแหล่งข้อมูลอื่นๆ คุณสามารถอ้างอิงไปยังรูปแบบ [Data การอ้างอิงแหล่งข้อมูล (DSR) สำหรับโพรโทคอลและข้อมูลที่อยู่ ](/azure/data-catalog/data-catalog-dsr#data-source-reference-specification)</span><span class="sxs-lookup"><span data-stu-id="61c60-346">For other data sources, you can refer to the [Data Source Reference (DSR) format for protocol and address information](/azure/data-catalog/data-catalog-dsr#data-source-reference-specification).</span></span>

<span data-ttu-id="61c60-347">หากคุณกำลังแก้ไขหรือสร้างไฟล์การเชื่อมต่อด้วยตนเอง ตัวอย่างเหล่านี้มีไว้เพื่อความสะดวกเท่านั้นไม่ได้มีไว้เพื่อให้ครอบคลุมและไม่รวมตัวเชื่อมต่อที่รองรับทั้งหมดในรูปแบบ DSR</span><span class="sxs-lookup"><span data-stu-id="61c60-347">If you're editing or manually creating the connection files, these examples are for convenience only, aren't meant to be comprehensive, and don't include all supported connectors in DSR format.</span></span>

#### <a name="azure-as"></a><span data-ttu-id="61c60-348">Azure AS</span><span class="sxs-lookup"><span data-stu-id="61c60-348">Azure AS</span></span>

```json
{ 
    "version": "0.1", 
    "connections": [ 
    { 
        "details": { 
        "protocol": "analysis-services", 
        "address": { 
            "server": "server-here" 
        }, 
        } 
    } 
    ] 
}
```

#### <a name="folder"></a><span data-ttu-id="61c60-349">โฟลเดอร์</span><span class="sxs-lookup"><span data-stu-id="61c60-349">Folder</span></span>

```json
{ 
  "version": "0.1", 
  "connections": [ 
    { 
      "details": { 
        "protocol": "folder", 
        "address": { 
            "path": "folder-path-here" 
        } 
      } 
    } 
  ] 
} 
```

#### <a name="odata"></a><span data-ttu-id="61c60-350">OData</span><span class="sxs-lookup"><span data-stu-id="61c60-350">OData</span></span>

```json
{ 
  "version": "0.1", 
  "connections": [ 
    { 
      "details": { 
        "protocol": "odata", 
        "address": { 
            "url": "URL-here" 
        } 
      } 
    } 
  ] 
} 
```

#### <a name="sap-bw"></a><span data-ttu-id="61c60-351">SAP BW</span><span class="sxs-lookup"><span data-stu-id="61c60-351">SAP BW</span></span>

```json
{ 
  "version": "0.1", 
  "connections": [ 
    { 
      "details": { 
        "protocol": "sap-bw-olap", 
        "address": { 
          "server": "server-name-here", 
          "systemNumber": "system-number-here", 
          "clientId": "client-id-here" 
        }, 
      } 
    } 
  ] 
} 
```

#### <a name="sap-hana"></a><span data-ttu-id="61c60-352">SAP Hana</span><span class="sxs-lookup"><span data-stu-id="61c60-352">SAP Hana</span></span>

```json
{ 
  "version": "0.1", 
  "connections": [ 
    { 
      "details": { 
        "protocol": "sap-hana-sql", 
        "address": { 
          "server": "server-name-here:port-here" 
        }, 
      } 
    } 
  ] 
} 
```

#### <a name="sharepoint-list"></a><span data-ttu-id="61c60-353">รายการ SharePoint</span><span class="sxs-lookup"><span data-stu-id="61c60-353">SharePoint list</span></span>

<span data-ttu-id="61c60-354">URL ต้องไปยังตำแหน่ง SharePoint ด้วยตัวเอง ไม่ใช่ไปยังรายการกับตำแหน่งอื่น</span><span class="sxs-lookup"><span data-stu-id="61c60-354">The URL must point to the SharePoint site itself, not to a list within the site.</span></span> <span data-ttu-id="61c60-355">ผู้ใช้จะได้รับตัวนำทางที่ช่วยให้พวกเขาสามารถเลือกอย่างน้อยหนึ่งรายการจากไซต์นั้นแต่ละอันจะกลายเป็นตารางในแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="61c60-355">Users get a navigator that allows them to select one or more lists from that site, each of which becomes a table in the model.</span></span>

```json
{ 
  "version": "0.1", 
  "connections": [ 
    { 
      "details": { 
        "protocol": "sharepoint-list", 
        "address": { 
          "url": "URL-here" 
        }, 
       } 
    } 
  ] 
} 
```

#### <a name="sql-server"></a><span data-ttu-id="61c60-356">SQL Server</span><span class="sxs-lookup"><span data-stu-id="61c60-356">SQL Server</span></span>

```json
{ 
  "version": "0.1", 
  "connections": [ 
    { 
      "details": { 
        "protocol": "tds", 
        "address": { 
          "server": "server-name-here", 
          "database": "db-name-here (optional) "
        } 
      }, 
      "options": {}, 
      "mode": "DirectQuery" 
    } 
  ] 
} 
```

#### <a name="text-file"></a><span data-ttu-id="61c60-357">ไฟล์ข้อความ</span><span class="sxs-lookup"><span data-stu-id="61c60-357">Text file</span></span>

```json
{ 
  "version": "0.1", 
  "connections": [ 
    { 
      "details": { 
        "protocol": "file", 
        "address": { 
            "path": "path-here" 
        } 
      } 
    } 
  ] 
} 
```

#### <a name="web"></a><span data-ttu-id="61c60-358">เว็บ</span><span class="sxs-lookup"><span data-stu-id="61c60-358">Web</span></span>

```json
{ 
  "version": "0.1", 
  "connections": [ 
    { 
      "details": { 
        "protocol": "http", 
        "address": { 
            "url": "URL-here" 
        } 
      } 
    } 
  ] 
} 
```

#### <a name="dataflow"></a><span data-ttu-id="61c60-359">กระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="61c60-359">Dataflow</span></span>

```json
{
  "version": "0.1",
  "connections": [
    {
      "details": {
        "protocol": "powerbi-dataflows",
        "address": {
          "workspace":"workspace id (Guid)",
          "dataflow":"optional dataflow id (Guid)",
          "entity":"optional entity name"
        }
       }
    }
  ]
}
```

## <a name="next-steps"></a><span data-ttu-id="61c60-360">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="61c60-360">Next steps</span></span>

<span data-ttu-id="61c60-361">คุณสามารถทำการเรียงลำดับของของต่างๆ ด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="61c60-361">You can do all sorts of things with Power BI Desktop.</span></span> <span data-ttu-id="61c60-362">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับขีดความสามารถ กรุณาดูแหล่งทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="61c60-362">For more information on its capabilities, check out the following resources:</span></span>

* [<span data-ttu-id="61c60-363">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="61c60-363">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="61c60-364">ภาพรวมคำถามด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="61c60-364">Query overview with Power BI Desktop</span></span>](../transform-model/desktop-query-overview.md)
* [<span data-ttu-id="61c60-365">ชนิดข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="61c60-365">Data types in Power BI Desktop</span></span>](desktop-data-types.md)
* [<span data-ttu-id="61c60-366">จัดรูปร่างและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="61c60-366">Shape and combine data with Power BI Desktop</span></span>](desktop-shape-and-combine-data.md)
* [<span data-ttu-id="61c60-367">งานแบบสอบถามทั่วไปใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="61c60-367">Common query tasks in Power BI Desktop</span></span>](../transform-model/desktop-common-query-tasks.md)