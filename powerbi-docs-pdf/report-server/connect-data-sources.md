---
title: แหล่งข้อมูลรายงานที่มีการแบ่งหน้าในเซิร์ฟเวอร์รายงาน Power BI
description: เรียนรู้เกี่ยวกับแหล่งข้อมูลที่รายงานที่มีการแบ่งหน้า (.rdl) สามารถเชื่อมต่อกับเซิร์ฟเวอร์รายงาน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: conceptual
ms.date: 06/26/2020
ms.openlocfilehash: 4559995baa7d3e0b5796ca6076687c26c4a0854d
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415392"
---
# <a name="paginated-report-data-sources--in-power-bi-report-server"></a><span data-ttu-id="429c7-103">แหล่งข้อมูลรายงานที่มีการแบ่งหน้าในเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="429c7-103">Paginated report data sources  in Power BI Report Server</span></span>
<span data-ttu-id="429c7-104">รายงานที่มีการแบ่งหน้าของ Reporting Services ในเซิร์ฟเวอร์รายงาน Power BI สนับสนุนแหล่งข้อมูลเดียวกันกับที่ได้รับการสนับสนุนใน SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="429c7-104">Reporting Services paginated reports in Power BI Report Server support the same data sources that are supported in SQL Server Reporting Services.</span></span> <span data-ttu-id="429c7-105">ดูรายการ [แหล่งข้อมูลที่สนับสนุนโดย Reporting Services](/sql/reporting-services/report-data/data-sources-supported-by-reporting-services-ssrs)</span><span class="sxs-lookup"><span data-stu-id="429c7-105">See the list of [Data sources supported by Reporting Services](/sql/reporting-services/report-data/data-sources-supported-by-reporting-services-ssrs).</span></span>

## <a name="connect-to-oracle-data-sources-with-useinstalleduiculture"></a><span data-ttu-id="429c7-106">เชื่อมต่อกับแหล่งข้อมูล Oracle ด้วย UseInstalledUICulture</span><span class="sxs-lookup"><span data-stu-id="429c7-106">Connect to Oracle data sources with UseInstalledUICulture</span></span>

<span data-ttu-id="429c7-107">ในการเชื่อมต่อกับแหล่งข้อมูล Oracle เซิร์ฟเวอร์รายงาน Power BI จะใช้ผู้ให้บริการข้อมูล Oracle สำหรับ .NET (ODP.NET) ซึ่งเป็นการวินิจฉัย NLS</span><span class="sxs-lookup"><span data-stu-id="429c7-107">To connect to Oracle data sources, Power BI Report Server uses the Oracle Data Provider for .NET (ODP.NET) which is NLS agnostic.</span></span>

<span data-ttu-id="429c7-108">ตามค่าเริ่มต้น เซิร์ฟเวอร์รายงานจะใช้วัฒนธรรม UI ของไคลเอ็นต์แรกเพื่อโหลด ODP.NET</span><span class="sxs-lookup"><span data-stu-id="429c7-108">By default, the report server uses the first client's UI culture to load ODP.NET.</span></span>  <span data-ttu-id="429c7-109">ด้วยเหตุนี้ การเชื่อมต่อในภายหลังทั้งหมดไปยัง Oracle จากเซิร์ฟเวอร์รายงานจะอยู่ในวัฒนธรรม UI เริ่มต้นจนกว่าจะเริ่มบริการใหม่</span><span class="sxs-lookup"><span data-stu-id="429c7-109">As a result, all subsequent connections to Oracle from the report server will be in that initial UI culture until restart of the service.</span></span>  <span data-ttu-id="429c7-110">วิธีการนี้อาจทำให้เกิดปัญหาในการแสดงรายงานเนื่องจากไม่ตรงกันในการจัดรูปแบบวัฒนธรรม UI</span><span class="sxs-lookup"><span data-stu-id="429c7-110">This approach can cause issues rendering a report due to mismatches in UI culture formatting.</span></span>

<span data-ttu-id="429c7-111">เพื่อเสนอการใช้งานที่ดีขึ้นในเซิร์ฟเวอร์รายงาน Power BI เราได้แนะนำการตั้งค่าการกำหนดค่าชื่อ UseInstalledUICulture</span><span class="sxs-lookup"><span data-stu-id="429c7-111">To offer a better experience in Power BI Report Server, we have introduced a configuration setting named UseInstalledUICulture.</span></span> <span data-ttu-id="429c7-112">เมื่อ UseInstalledUICulture ถูกตั้งค่าเป็นจริง เซิร์ฟเวอร์รายงานจะโหลด ODP.NET ในวัฒนธรรม UI ของเซิร์ฟเวอร์แทนที่จะเป็นวัฒนธรรมของไคลเอ็นต์แรก</span><span class="sxs-lookup"><span data-stu-id="429c7-112">When UseInstalledUICulture is set to true, the report server always loads ODP.NET in the server’s UI Culture instead of the first client’s culture.</span></span>
<span data-ttu-id="429c7-113">การตั้งค่านี้พร้อมใช้งานในเซิร์ฟเวอร์รายงาน Power BI เริ่มต้นด้วยการเผยแพร่บริการในเดือนมีนาคม 2020</span><span class="sxs-lookup"><span data-stu-id="429c7-113">This setting is available in Power BI Report Server starting with the March 2020 Service Release.</span></span>

<span data-ttu-id="429c7-114">หากต้องการเปิดใช้งานฟีเจอร์ ให้ปรับเปลี่ยนไฟล์ rsreportserver.config ของรายการส่วนขยาย ORACLE เช่นเดียวกันกับด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="429c7-114">To enable the feature, modify ORACLE extension entry rsreportserver.config file like below.</span></span>
```xml
<Extension Name="ORACLE" Type="Microsoft.ReportingServices.DataExtensions.OracleClientConnectionWrapper,Microsoft.ReportingServices.DataExtensions">
    <Configuration>
        <UseInstalledUICulture>true</UseInstalledUICulture>
    </Configuration>
</Extension>
```

## <a name="next-steps"></a><span data-ttu-id="429c7-115">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="429c7-115">Next steps</span></span>
<span data-ttu-id="429c7-116">เมื่อคุณได้เชื่อมต่อกับแหล่งข้อมูลของคุณ [ให้สร้างรายงานที่มีการแบ่งหน้า](quickstart-create-paginated-report.md)</span><span class="sxs-lookup"><span data-stu-id="429c7-116">Now that you've connected to your data source, [create a paginated report](quickstart-create-paginated-report.md).</span></span>  


<span data-ttu-id="429c7-117">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="429c7-117">More questions?</span></span> [<span data-ttu-id="429c7-118">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="429c7-118">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)