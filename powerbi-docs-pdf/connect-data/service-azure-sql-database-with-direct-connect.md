---
title: Azure SQL Database พร้อม DirectQuery
description: Azure SQL Database พร้อม DirectQuery
author: davidiseminger
ms.author: davidi
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.reviewer: ''
ms.custom: ''
ms.date: 04/28/2020
LocalizationGroup: Data from databases
ms.openlocfilehash: 3dbd769d11b3122591e0a34df9d74ca8e9c1e3b2
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410677"
---
# <a name="azure-sql-database-with-directquery"></a><span data-ttu-id="cf925-103">Azure SQL Database พร้อม DirectQuery</span><span class="sxs-lookup"><span data-stu-id="cf925-103">Azure SQL Database with DirectQuery</span></span>

<span data-ttu-id="cf925-104">เรียนรู้วิธีการเชื่อมต่อโดยตรงไปยังฐานข้อมูล SQL Azure และสร้างรายงานที่ใช้ข้อมูลสด</span><span class="sxs-lookup"><span data-stu-id="cf925-104">Learn how you can connect directly to Azure SQL Database and create reports that use live data.</span></span> <span data-ttu-id="cf925-105">คุณสามารถเก็บข้อมูลของคุณที่แหล่งข้อมูลได้ แต่ไม่ใช่ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="cf925-105">You can keep your data at the source and not in Power BI.</span></span>

<span data-ttu-id="cf925-106">ด้วย DirectQuery แบบสอบถามจะถูกส่งกลับไปยังฐานข้อมูล SQL Azure ของคุณตามที่คุณสำรวจข้อมูลในมุมมองรายงาน</span><span class="sxs-lookup"><span data-stu-id="cf925-106">With DirectQuery, queries are sent back to your Azure SQL Database as you explore the data in the report view.</span></span> <span data-ttu-id="cf925-107">ประสบการณ์การใช้งานนี้แนะนำสำหรับผู้ใช้ที่คุ้นเคยกับฐานข้อมูลและเอนทิตีที่ผู้ใช้งานดังกล่าวเชื่อมต่อด้วย</span><span class="sxs-lookup"><span data-stu-id="cf925-107">This experience is suggested for users who are familiar with the databases and entities they connect to.</span></span>

> [!Important]
> <span data-ttu-id="cf925-108">คำอธิบายนี้อนุมานว่าฐานข้อมูล Azure SQL ไม่ได้อยู่หลัง VNET หรือเปิดใช้งานจุดเชื่อมโยงส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="cf925-108">This description assumes that Azure SQL database is not behind a VNET or has private link endpoint enabled.</span></span>

<span data-ttu-id="cf925-109">**หมายเหตุ:**</span><span class="sxs-lookup"><span data-stu-id="cf925-109">**Notes:**</span></span>

* <span data-ttu-id="cf925-110">ระบุชื่อเซิร์ฟเวอร์ที่มีคุณสมบัติครบถ้วนเมื่อเชื่อมต่อ (ดูด้านล่างสำหรับรายละเอียดเพิ่มเติม)</span><span class="sxs-lookup"><span data-stu-id="cf925-110">Specify the fully qualified server name when connecting (see below for more details).</span></span>
* <span data-ttu-id="cf925-111">ตรวจสอบให้แน่ใจว่ามีการกำหนดค่ากฎไฟร์วอลล์สำหรับฐานข้อมูลเพื่อ "[อนุญาตการเข้าถึงบริการ Azure](/azure/sql-database/sql-database-networkaccess-overview#allow-azure-services)"</span><span class="sxs-lookup"><span data-stu-id="cf925-111">Ensure firewall rules for the database are configured to "[Allow access to Azure services](/azure/sql-database/sql-database-networkaccess-overview#allow-azure-services)."</span></span>
* <span data-ttu-id="cf925-112">ทุกการดำเนินการ เช่น การเลือกคอลัมน์หรือการเพิ่มตัวกรอง จะส่งการสอบถามย้อนกลับไปยังฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cf925-112">Every action such as selecting a column or adding a filter will send a query back to the database.</span></span>
* <span data-ttu-id="cf925-113">ไทล์จะรีเฟรชทุกชั่วโมง (รีเฟรชไม่จำเป็นต้องมีการจัดกำหนดการ)</span><span class="sxs-lookup"><span data-stu-id="cf925-113">Tiles are refreshed every hour (refresh does not need to be scheduled).</span></span> <span data-ttu-id="cf925-114">คุณสามารถปรับความถี่การรีเฟรชในส่วนการตั้งค่าขั้นสูงเมื่อทำการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="cf925-114">You can adjust how often to refresh in the Advanced settings when you connect.</span></span>
* <span data-ttu-id="cf925-115">การถามตอบไม่พร้อมใช้งานสำหรับชุดข้อมูล DirectQuery</span><span class="sxs-lookup"><span data-stu-id="cf925-115">Q&A is not available for DirectQuery datasets.</span></span>
* <span data-ttu-id="cf925-116">การเปลี่ยนแปลงเค้าร่างจะไม่ถูกเลือกโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cf925-116">Schema changes are not picked up automatically.</span></span>

<span data-ttu-id="cf925-117">ข้อจำกัดและบันทึกย่อเหล่านี้อาจเปลี่ยนแปลงขณะที่เราปรับปรุงประสบการณ์การใช้งานขึ้นเรื่อย ๆ</span><span class="sxs-lookup"><span data-stu-id="cf925-117">These restrictions and notes may change as we continue to improve the experiences.</span></span> <span data-ttu-id="cf925-118">ขั้นตอนในการเชื่อมต่อจะมีรายละเอียดดังด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="cf925-118">The steps to connect are detailed below.</span></span>

> [!Important]
> <span data-ttu-id="cf925-119">เรากำลังปรับปรุงการเชื่อมต่อของเรากับฐานข้อมูล SQL ของ Azure</span><span class="sxs-lookup"><span data-stu-id="cf925-119">We have been improving our connectivity to Azure SQL Database.</span></span>  <span data-ttu-id="cf925-120">ใช้ Power BI Desktop เชื่อมต่อกับแหล่งฐานข้อมูล SQL ของ Azure</span><span class="sxs-lookup"><span data-stu-id="cf925-120">For the best experience to connect to your Azure SQL Database data source, use Power BI Desktop.</span></span>  <span data-ttu-id="cf925-121">เมื่อคุณได้สร้างรูปแบบข้อมูลและรายงานของคุณแล้ว คุณสามารถเผยแพร่สิ่งดังกล่าวไปยังบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="cf925-121">Once you've built your model and report, you can publish it to the Power BI service.</span></span>  <span data-ttu-id="cf925-122">ตัวเชื่อมต่อโดยตรงกับฐานข้อมูล SQL ของ Azure ในบริการ Power BI ในขณะนี้ไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="cf925-122">The direct connector for Azure SQL Database in the Power BI service is now deprecated.</span></span>

## <a name="power-bi-desktop-and-directquery"></a><span data-ttu-id="cf925-123">ใช้ DirectQuery ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="cf925-123">Power BI Desktop and DirectQuery</span></span>

<span data-ttu-id="cf925-124">เมื่อต้องการเชื่อมต่อกับฐานข้อมูล SQL Azure ที่ใช้ DirectQuery คุณจะต้องใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="cf925-124">To connect to Azure SQL Database using DirectQuery, you must use Power BI Desktop.</span></span> <span data-ttu-id="cf925-125">แนวทางนี้เพิ่มความยืดหยุ่นและขีดความสามารถให้มากขึ้น</span><span class="sxs-lookup"><span data-stu-id="cf925-125">This approach provides additional flexibility and capabilities.</span></span> <span data-ttu-id="cf925-126">รายงานที่สร้างขึ้นโดยใช้ Power BI Desktop จะสามารถเผยแพร่ไปยังบริการ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="cf925-126">Reports created using Power BI Desktop can then be published to the Power BI service.</span></span> <span data-ttu-id="cf925-127">คุณสามารถเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการเชื่อมต่อ[ฐานข้อมูล SQL Azure ที่ใช้ DirectQuery](desktop-use-directquery.md)ภายใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="cf925-127">You can learn more about how to connect to [Azure SQL Database using DirectQuery](desktop-use-directquery.md) within Power BI Desktop.</span></span>

## <a name="find-parameter-values"></a><span data-ttu-id="cf925-128">ค้นหาค่าพารามิเตอร์ต่างๆ</span><span class="sxs-lookup"><span data-stu-id="cf925-128">Find parameter values</span></span>

<span data-ttu-id="cf925-129">คุณสามารถค้นหาชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูลแบบเต็มได้ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="cf925-129">You can find your fully qualified server name and database name in the Azure portal.</span></span>

![การอัปเดตพอร์ทัล Azure ใหม่](media/service-azure-sql-database-with-direct-connect/azureportnew_update.png)

![การอัปเดตพอร์ทัล Azure](media/service-azure-sql-database-with-direct-connect/azureportal_update.png)

[!INCLUDE [direct-query-sso](../includes/direct-query-sso.md)]

## <a name="next-steps"></a><span data-ttu-id="cf925-132">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="cf925-132">Next steps</span></span>

* [<span data-ttu-id="cf925-133">ใช้ DirectQuery ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="cf925-133">Use DirectQuery in Power BI Desktop</span></span>](desktop-use-directquery.md)  
* [<span data-ttu-id="cf925-134">Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="cf925-134">What is Power BI?</span></span>](../fundamentals/power-bi-overview.md)  
* [<span data-ttu-id="cf925-135">รับข้อมูลสำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="cf925-135">Get data for Power BI</span></span>](service-get-data.md)  

<span data-ttu-id="cf925-136">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="cf925-136">More questions?</span></span> [<span data-ttu-id="cf925-137">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="cf925-137">Try the Power BI community</span></span>](https://community.powerbi.com/)