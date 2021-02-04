---
title: เปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูลด้วย PowerShell - Power BI Report Server ก่อนเดือนตุลาคม 2020
description: เปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูลโดยใช้ API ใน PowerShell - Power BI Report Server ก่อนเดือนตุลาคม 2020
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.date: 10/26/2020
ms.openlocfilehash: 72b81f10b6337530ab05f1fcef0a17a5869af867
ms.sourcegitcommit: ab28cf07b483cb4b01a42fa879b788932bba919d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "98226754"
---
# <a name="change-data-source-connection-strings-in-power-bi-reports-with-powershell---power-bi-report-server-pre-october-2020"></a><span data-ttu-id="e57c7-103">เปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูลในรายงาน Power BI ด้วย PowerShell - Power BI Report Server ก่อนเดือนตุลาคม 2020</span><span class="sxs-lookup"><span data-stu-id="e57c7-103">Change data source connection strings in Power BI reports with PowerShell - Power BI Report Server pre-October 2020</span></span>


<span data-ttu-id="e57c7-104">คุณสามารถเปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูลของรายงาน Power BI ที่โฮสต์ในเซิร์ฟเวอร์รายงาน Power BI โดยใช้ PowerShell เพื่อโต้ตอบกับ Api ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="e57c7-104">You can change data source connection strings of Power BI reports hosted in Power BI Report Server by using PowerShell to interact with the necessary APIs.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="e57c7-105">ถ้าคุณกำลังใช้ Power BI Report Server เวอร์ชันล่าสุด ที่เผยแพร่เดือนตุลาคม 2020 โปรดดูที่[เปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูลในรายงาน Power BI ด้วย PowerShell - Power BI Report Server](connect-data-source-apis.md)</span><span class="sxs-lookup"><span data-stu-id="e57c7-105">If you're using the latest version of Power BI Report Server, October 2020, see [Change data source connection strings in Power BI reports with PowerShell - Power BI Report Server](connect-data-source-apis.md).</span></span>

> [!NOTE]
> <span data-ttu-id="e57c7-106">ตอนนี้ฟังก์ชันนี้ทำงานเพียงกับ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="e57c7-106">Currently this functionality only works for DirectQuery.</span></span> <span data-ttu-id="e57c7-107">การสนับสนุนสำหรับการนำเข้าและการรีเฟรชข้อมูลกำลังจะมา</span><span class="sxs-lookup"><span data-stu-id="e57c7-107">Support for import and data refresh is coming.</span></span>

1. <span data-ttu-id="e57c7-108">ติดตั้งแอปเพล็ตคำสั่ง PowerShell ของเซิร์ฟเวอร์รายงาน Power BI </span><span class="sxs-lookup"><span data-stu-id="e57c7-108">Install the Power BI Report Server PowerShell commandlets.</span></span> <span data-ttu-id="e57c7-109">ค้นหาคำแนะนำเกี่ยวกับแอปเพล็ตคำสั่งและการติดตั้งที่ [https://github.com/Microsoft/ReportingServicesTools](https://github.com/Microsoft/ReportingServicesTools)</span><span class="sxs-lookup"><span data-stu-id="e57c7-109">Find the commandlets and installation instructions at [https://github.com/Microsoft/ReportingServicesTools](https://github.com/Microsoft/ReportingServicesTools).</span></span> 

    <span data-ttu-id="e57c7-110">ติดตั้ง `ReportingServicesTools` มอดูลโดยตรงจาก [แกลเลอรี PowerShell](https://www.powershellgallery.com/packages/ReportingServicesTools/) โดยใช้คำสั่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e57c7-110">Install the `ReportingServicesTools` module directly from the [PowerShell Gallery](https://www.powershellgallery.com/packages/ReportingServicesTools/) using the following command.</span></span>

    ```powershell
    Install-Module ReportingServicesTools
    ```

2. <span data-ttu-id="e57c7-111">ดึงข้อมูลแหล่งข้อมูลที่มีอยู่สำหรับไฟล์ Power BI ผ่านทางแอปเพล็ตคำสั่ง PowerShell</span><span class="sxs-lookup"><span data-stu-id="e57c7-111">Fetch the existing data source information for the Power BI file via the PowerShell commandlets:</span></span>

    ```powershell
    $dataSources = Get-RsRestItemDataSource -RsItem '/MyPbixReport'
    ```

    <span data-ttu-id="e57c7-112">วิธีการดูข้อมูลสำหรับแหล่งข้อมูลแรกที่มีอยู่ในรายงาน Power BI:</span><span class="sxs-lookup"><span data-stu-id="e57c7-112">To view information for the first data source contained in the Power BI report:</span></span> 

    ```powershell
    $dataSources[0]
    ```

3. <span data-ttu-id="e57c7-113">อัปเดตข้อมูลการเชื่อมต่อและข้อมูลประจำตัวตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="e57c7-113">Update connection and credential info as needed.</span></span> <span data-ttu-id="e57c7-114">ถ้าการอัปเดตสตริงการเชื่อมต่อและแหล่งข้อมูลทำให้ใช้ข้อมูลประจำตัวที่เก็บไว้ คุณจำเป็นต้องใส่รหัสผ่านของบัญชี</span><span class="sxs-lookup"><span data-stu-id="e57c7-114">If updating the connection string and the data source makes use of stored credentials, you need to provide the account password.</span></span> 

    <span data-ttu-id="e57c7-115">วิธีการอัปเดตสตริงการเชื่อมต่อแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e57c7-115">To update a data source connection string:</span></span>

    ```powershell
    $dataSources[0].ConnectionString = 'data source=myCatalogServer;initial catalog=ReportServer;persist security info=False' 
    ```

    <span data-ttu-id="e57c7-116">วิธีการเปลี่ยนชนิดข้อมูลประจำตัวของแหล่งข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="e57c7-116">To change the data source credential type:</span></span>

    ```powershell
    $dataSources[0].DataModelDataSource.AuthType = 'Integrated'
    ```

    <span data-ttu-id="e57c7-117">วิธีการเปลี่ยนชื่อผู้ใช้/รหัสผ่านของแหล่งข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="e57c7-117">To change the data source username/password:</span></span>

    ```powershell
    $dataSources[0].DataModelDataSource.Username = 'domain\user'
    ```
    ```powershell
    $dataSources[0].DataModelDataSource.Secret = 'password'
    ```

4. <span data-ttu-id="e57c7-118">บันทึกข้อมูลประจำตัวที่อัปเดตแล้วกลับไปยังเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="e57c7-118">Save the updated credentials back to the server.</span></span>

    ```powershell
    Set-RsRestItemDataSource -RsItem '/MyPbixReport' -RsItemType 'PowerBIReport' -DataSources $dataSources
    ```

## <a name="next-steps"></a><span data-ttu-id="e57c7-119">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="e57c7-119">Next steps</span></span>

[<span data-ttu-id="e57c7-120">แหล่งข้อมูลรายงานที่มีการแบ่งหน้าในเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="e57c7-120">Paginated report data sources in Power BI Report Server</span></span>](connect-data-sources.md) 

<span data-ttu-id="e57c7-121">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="e57c7-121">More questions?</span></span> [<span data-ttu-id="e57c7-122">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="e57c7-122">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
