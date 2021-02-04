---
title: เปลี่ยนแปลงชุดอักขระการเชื่อมต่อต้นทางของข้อมูลผ่าน PowerShell
description: เปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูลโดยใช้ API ใน PowerShell - เซิร์ฟเวอร์รายงาน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.date: 10/26/2020
ms.openlocfilehash: 4e1947abe0fa0f17e1db92619f0aa7fba5df5575
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415484"
---
# <a name="change-data-source-connection-strings-in-power-bi-reports-with-powershell---power-bi-report-server"></a><span data-ttu-id="c5602-103">เปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูลในรายงาน Power BI ด้วย PowerShell - เซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="c5602-103">Change data source connection strings in Power BI reports with PowerShell - Power BI Report Server</span></span>


<span data-ttu-id="c5602-104">เริ่มต้นด้วย Power BI Report Server รุ่นการเผยแพร่เดือนตุลาคม 2020 เรากำลังเปิดใช้ความสามารถเพื่ออัปเดตการเชื่อมต่อสำหรับรายงาน Power BI สำหรับ DirectQuery และการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="c5602-104">Starting with the October 2020 release of Power BI Report Server we are enabling the ability to update connections for Power BI reports for DirectQuery and refresh.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5602-105">นอกจากนี้ยังเป็นการเปลี่ยนแปลงอย่างสิ้นเชิงในการตั้งค่านี้ในรุ่นการเผยแพร่ก่อน ๆ อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="c5602-105">This is also a breaking change on how you could set this up in previous releases.</span></span> <span data-ttu-id="c5602-106">ถ้าคุณกำลังใช้ Power BI Report Server เวอร์ชันก่อนเดือนตุลาคม 2020 โปรดดูที่[เปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูลในรายงาน Power BI ด้วย PowerShell - Power BI Report Server ก่อนเดือนตุลาคม 2020](connect-data-source-apis-pre-oct-2020.md)</span><span class="sxs-lookup"><span data-stu-id="c5602-106">If you're using a pre-October 2020 version of Power BI Report Server, see [Change data source connection strings in Power BI reports with PowerShell - Power BI Report Server pre-October 2020](connect-data-source-apis-pre-oct-2020.md)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c5602-107">สิ่งที่จำเป็นต้องมี</span><span class="sxs-lookup"><span data-stu-id="c5602-107">Prerequisites:</span></span>
- <span data-ttu-id="c5602-108">ดาวน์โหลด [Power BI Report Server และ Power BI Desktop ที่ปรับให้เหมาะสมสำหรับ Power BI Report Serve](https://powerbi.microsoft.com/report-server/) รุ่นเผยแพร่เดือนตุลาคม 2020</span><span class="sxs-lookup"><span data-stu-id="c5602-108">Download the October 2020 release of [Power BI Report Server and Power BI Desktop optimized for Power BI Report Server](https://powerbi.microsoft.com/report-server/).</span></span>
- <span data-ttu-id="c5602-109">รายงานที่บันทึกด้วย Power BI Desktop รุ่นเผยแพร่เดือนตุลาคม 2020 ที่ปรับให้เหมาะสมสำหรับ Report Server แล้วโดยมีการเปิดใช้งาน **เมตาดาต้าชุดข้อมูลที่ปรับปรุงประสิทธิภาพแล้ว**</span><span class="sxs-lookup"><span data-stu-id="c5602-109">A report saved with the October 2020 release of Power BI Desktop optimized for Report Server, with **Enhanced DataSet Metadata** enabled.</span></span>
- <span data-ttu-id="c5602-110">รายงานที่ใช้การเชื่อมต่อแบบกำหนดพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="c5602-110">A report that uses parameterized connections.</span></span> <span data-ttu-id="c5602-111">เฉพาะรายงานที่มีการเชื่อมต่อและฐานข้อมูลแบบกำหนดพารามิเตอร์เท่านั้นที่สามารถอัปเดตได้หลังจากเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="c5602-111">Only reports with parameterized connections and databases can be updated after publishing.</span></span>
- <span data-ttu-id="c5602-112">ตัวอย่างนี้ใช้เครื่องมือ Reporting Services PowerShell</span><span class="sxs-lookup"><span data-stu-id="c5602-112">This example uses the Reporting Services PowerShell tools.</span></span> <span data-ttu-id="c5602-113">คุณสามารถทำสิ่งเดียวกันนี้ได้โดยใช้ REST API ใหม่</span><span class="sxs-lookup"><span data-stu-id="c5602-113">You can achieve the same  by using the new REST APIs.</span></span>

## <a name="create-a-report-with-parameterized-connections"></a><span data-ttu-id="c5602-114">สร้างรายงานที่มีการเชื่อมต่อแบบกำหนดพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="c5602-114">Create a report With parameterized connections</span></span>
    
1. <span data-ttu-id="c5602-115">สร้างการเชื่อมต่อ SQL Server ไปยังเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="c5602-115">Create a SQL Server connection to a server.</span></span> <span data-ttu-id="c5602-116">ในตัวอย่างด้านล่าง เรากำลังเชื่อมต่อกับ localhost ในฐานข้อมูลที่เรียกว่า ReportServer และดึงข้อมูลจาก ExecutionLog</span><span class="sxs-lookup"><span data-stu-id="c5602-116">In the example below, we're connecting to the localhost to a database called ReportServer and pulling data from ExecutionLog.</span></span>

    :::image type="content" source="media/connect-data-source-apis/sql-server-connect-database.png" alt-text="เชื่อมต่อไปยังฐานข้อมูล SQL Server":::

    <span data-ttu-id="c5602-118">ต่อไปนี้เป็นลักษณะของคิวรี M:</span><span class="sxs-lookup"><span data-stu-id="c5602-118">Here's what the M query looks like at this point:</span></span>

    ```
    let
        Source = Sql.Database("localhost", "ReportServer"),
        dbo_ExecutionLog3 = Source{[Schema="dbo",Item="ExecutionLog3"]}[Data]
    in
        dbo_ExecutionLog3
    ```

2. <span data-ttu-id="c5602-119">เลือก **จัดการพารามิเตอร์** ในริบบอนตัวแก้ไข Power Query</span><span class="sxs-lookup"><span data-stu-id="c5602-119">Select **Manage Parameters** in the Power Query Editor ribbon.</span></span>

    :::image type="content" source="media/connect-data-source-apis/power-query-manage-parameters.png" alt-text="เลือกจัดการพารามิเตอร์":::

1.  <span data-ttu-id="c5602-121">สร้างพารามิเตอร์สำหรับชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c5602-121">Create parameters for the servername and databasename.</span></span>

    :::image type="content" source="media/connect-data-source-apis/report-server-manage-parameters.png" alt-text="จัดการพารามิเตอร์ ตั้งชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูล":::


3. <span data-ttu-id="c5602-123">แก้ไขคิวรีสำหรับการเชื่อมต่อครั้งแรกและแมปฐานข้อมูลและชื่อเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="c5602-123">Edit the query for the first connection, and map the database and servername.</span></span>

    :::image type="content" source="media/connect-data-source-apis/report-server-map-database-server.png" alt-text="แมปชื่อเซิร์ฟเวอร์และฐานข้อมูล":::

    <span data-ttu-id="c5602-125">ตอนนี้คิวรีมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="c5602-125">Now the query looks like this:</span></span>

    ```
    let
        Source = Sql.Database(ServerName, Databasename),
        dbo_ExecutionLog3 = Source{[Schema="dbo",Item="ExecutionLog3"]}[Data]
    in
        dbo_ExecutionLog3
    ```
    
    4. <span data-ttu-id="c5602-126">เผยแพร่รายงานนั้นไปยังเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="c5602-126">Publish that report to the server.</span></span> <span data-ttu-id="c5602-127">ในตัวอย่างนี้ รายงานมีชื่อว่า executionlogparameter</span><span class="sxs-lookup"><span data-stu-id="c5602-127">In this example, the report is named executionlogparameter.</span></span> <span data-ttu-id="c5602-128">รูปภาพต่อไปนี้เป็นตัวอย่างของหน้าการจัดการแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c5602-128">The following image is an example of a data source management page.</span></span>

    :::image type="content" source="media/connect-data-source-apis/report-server-manage-data-source-credentials.png" alt-text="หน้าการจัดการแหล่งข้อมูล":::

## <a name="update-parameters-using-the-powershell-tools"></a><span data-ttu-id="c5602-130">อัปเดตพารามิเตอร์โดยใช้เครื่องมือ PowerShell</span><span class="sxs-lookup"><span data-stu-id="c5602-130">Update parameters using the PowerShell tools</span></span>

1. <span data-ttu-id="c5602-131">เปิด PowerShell และติดตั้งเครื่องมือ Reporting Services ล่าสุดโดยทำตามคำแนะนำที่ [https://github.com/microsoft/ReportingServicesTools](https://github.com/microsoft/ReportingServicesTools)</span><span class="sxs-lookup"><span data-stu-id="c5602-131">Open PowerShell and install the latest Reporting Services tools, following the instructions at [https://github.com/microsoft/ReportingServicesTools](https://github.com/microsoft/ReportingServicesTools).</span></span>
    
2.  <span data-ttu-id="c5602-132">เมื่อต้องการรับพารามิเตอร์สำหรับรายงาน ให้ใช้ REST DataModelParameters API ใหม่โดยใช้การเรียกของ PowerShell ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c5602-132">To get the parameter for the report, use the new REST DataModelParameters API using the following PowerShell call:</span></span>

    ```powershell
    Get-RsRestItemDataModelParameters '/executionlogparameter'

        Name         Value
        ----         -----
        ServerName   localhost
        Databasename ReportServer
    ```

3. <span data-ttu-id="c5602-133">เราบันทึกผลลัพธ์ของการเรียกนี้ในตัวแปร:</span><span class="sxs-lookup"><span data-stu-id="c5602-133">We save the result of this call in a variable:</span></span>

    ```powershell
    $parameters = Get-RsRestItemDataModelParameters '/executionlogparameter'
    ```

4. <span data-ttu-id="c5602-134">ตัวแปรนี้ได้รับการอัปเดตด้วยค่าที่เราต้องการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="c5602-134">This variable is updated with the values that we need to change.</span></span>
5. <span data-ttu-id="c5602-135">เราบันทึกผลลัพธ์ของการเรียกนี้ในตัวแปร:</span><span class="sxs-lookup"><span data-stu-id="c5602-135">We save the result of this call in a variable:</span></span>

    ```powershell
    $parameters[0].Value = 'myproductionserver'
    $parameters[1].Value = 'myproductiondatabase'
    ```

6. <span data-ttu-id="c5602-136">เราสามารถใช้ commandlet `Set-RsRestItemDataModelParameters` เพื่ออัปเดตค่าในเซิร์ฟเวอร์ด้วยค่าที่อัปเดต:</span><span class="sxs-lookup"><span data-stu-id="c5602-136">With the updated values, we can use the commandlet `Set-RsRestItemDataModelParameters` to update the values in the server:</span></span>

    ```powershell
    Set-RsRestItemDataModelParameters -RsItem '/executionlogparameter' -DataModelParameters $parameters
    ```

7. <span data-ttu-id="c5602-137">เมื่ออัปเดตพารามิเตอร์แล้ว เซิร์ฟเวอร์จะอัปเดตแหล่งข้อมูลใดก็ตามที่ผูกไว้กับพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="c5602-137">Once the parameters are updated, the server updates any data sources that were bound to the parameters.</span></span> <span data-ttu-id="c5602-138">ย้อนกลับไปยังกล่องโต้ตอบ **แก้ไขแหล่งข้อมูล** คุณควรจะสามารถตั้งค่าข้อมูลประจำตัวสำหรับเซิร์ฟเวอร์และฐานข้อมูลที่อัปเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="c5602-138">Going back to the **Edit data source** dialog box, you should be able to set credentials for the updated server and database.</span></span>

    :::image type="content" source="media/connect-data-source-apis/report-server-manage-executionlogparameter-dialog.png" alt-text="ตั้งค่าข้อมูลประจำตัวสำหรับเซิร์ฟเวอร์และฐานข้อมูลที่อัปเดตแล้ว":::

## <a name="next-steps"></a><span data-ttu-id="c5602-140">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c5602-140">Next steps</span></span>

[<span data-ttu-id="c5602-141">แหล่งข้อมูลรายงานที่มีการแบ่งหน้าในเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="c5602-141">Paginated report data sources in Power BI Report Server</span></span>](connect-data-sources.md) 

<span data-ttu-id="c5602-142">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c5602-142">More questions?</span></span> [<span data-ttu-id="c5602-143">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="c5602-143">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
