---
title: แก้ไขปัญหาการรีเฟรชตามกำหนดเวลาในเซิร์ฟเวอร์รายงาน Power BI
description: บทความนี้อธิบายถึงทรัพยากรมีให้เพื่อใช้แก้ไขปัญหา รีเฟรชตามกำหนดเวลาในเซิร์ฟเวอร์รายงาน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: troubleshooting
ms.date: 11/01/2017
ms.openlocfilehash: 8cb8bf4e6d67f01f7bbdc4370d8a60691dba5a63
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418290"
---
# <a name="troubleshoot-scheduled-refresh-in-power-bi-report-server"></a><span data-ttu-id="f1472-103">แก้ไขปัญหาการรีเฟรชตามกำหนดเวลาในเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="f1472-103">Troubleshoot scheduled refresh in Power BI Report Server</span></span>
<span data-ttu-id="f1472-104">บทความนี้อธิบายถึงทรัพยากรมีให้เพื่อใช้แก้ไขปัญหา รีเฟรชตามกำหนดเวลาในเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="f1472-104">This article discusses resources available to troubleshoot issues with scheduled refresh in Power BI Report Server.</span></span>

<span data-ttu-id="f1472-105">เมื่อมีปัญหาใหม่ ๆ เกิดขึ้น บทความนี้จะถูกปรับปรุงด้วยข้อมูลที่จะช่วยคุณได้</span><span class="sxs-lookup"><span data-stu-id="f1472-105">As issues come up, this article will be updated with information to help you.</span></span>

## <a name="common-issues"></a><span data-ttu-id="f1472-106">ปัญหาที่พบบ่อย</span><span class="sxs-lookup"><span data-stu-id="f1472-106">Common issues</span></span>
<span data-ttu-id="f1472-107">ต่อไปนี้คือ ปัญหาที่พบได้บ่อย ที่คุณอาจจะเจอขณะพยายามกำหนดเวลารีเฟรชสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="f1472-107">The following are the more common issues you will hit when trying to schedule refresh for a report.</span></span> 

### <a name="driver-related-problems"></a><span data-ttu-id="f1472-108">ปัญหาที่เกี่ยวข้องกับโปรแกรมควบคุม</span><span class="sxs-lookup"><span data-stu-id="f1472-108">Driver related problems</span></span>
<span data-ttu-id="f1472-109">การเชื่อมต่อกับแหล่งข้อมูลต่าง ๆ อาจจำเป็นต้องมีการติดตั้งโปรแกรมควบคุมจากบุคคลที่สาม เพื่อให้เชื่อมต่อได้สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="f1472-109">Connecting to different data sources may require 3rd party drivers that need to be installed in order to connect successfully.</span></span> <span data-ttu-id="f1472-110">ไม่เพียงคุณจำเป็นต้องติดตั้งบนเครื่องที่คุณกำลังใช้ Power BI Desktop เท่านั้น แต่คุณยังจำเป็นต้องติดตั้งโปรแกรมควบคุมนั้นอยู่บนเซิร์ฟเวอร์รายงานด้วย</span><span class="sxs-lookup"><span data-stu-id="f1472-110">Not only would you need to install them on the machine you are using Power BI Desktop on, but you will also need to make sure the driver is installed on the report server.</span></span>

<span data-ttu-id="f1472-111">โปรแกรมควบคุมอาจจะมาในรูป 32 บิต และ 64 บิต</span><span class="sxs-lookup"><span data-stu-id="f1472-111">The driver may also come in both 32bit and 64bit.</span></span> <span data-ttu-id="f1472-112">ตรวจสอบให้แน่ใจว่าได้ติดตั้งไดรเวอร์ 64 Power BI บิต เนื่องจากเซิร์ฟเวอร์รายงานเป็นแบบ 64 บิต</span><span class="sxs-lookup"><span data-stu-id="f1472-112">Make sure to install the 64bit driver as Power BI Report Server is 64bit.</span></span>

<span data-ttu-id="f1472-113">โปรดอ้างอิงไปยังผู้ผลิต สำหรับรายละเอียดเกี่ยวกับวิธีการติดตั้ง และกำหนดค่าโปรแกรมควบคุมจากบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="f1472-113">Please refer to the manufacturer for details on how to install and configure 3rd party drivers.</span></span>

### <a name="memory-pressure"></a><span data-ttu-id="f1472-114">หน่วยความจำไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="f1472-114">Memory pressure</span></span>
<span data-ttu-id="f1472-115">หน่วยความจำไม่เพียงพอ สามารถเกิดขึ้นได้เมื่อรายงานต้องใช้หน่วยความจำเพิ่มขึ้น เพื่อประมวลผลและแสดงผล</span><span class="sxs-lookup"><span data-stu-id="f1472-115">Memory pressure can occur when reports require more memory to process and render.</span></span> <span data-ttu-id="f1472-116">การรีเฟรชตามกำหนดเวลาบนรายงาน อาจต้องการหน่วยความจำบนเครื่องเป็นจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="f1472-116">Schedule refresh on reports may demand a significant amount of memory on the machine.</span></span> <span data-ttu-id="f1472-117">โดยเฉพาะอย่างยิ่งสำหรับรายงานที่มีขนาดใหญ่</span><span class="sxs-lookup"><span data-stu-id="f1472-117">Especially for larger reports.</span></span> <span data-ttu-id="f1472-118">ปัญหาหน่วยความจำไม่เพียงพอ อาจก่อให้เกิดความล้มเหลวในการรายงาน และมีโอกาสทำให้เซิร์ฟเวอร์รายงานหยุดทำงาน</span><span class="sxs-lookup"><span data-stu-id="f1472-118">Memory pressure can result in report failures as well as a potential crash of the report server itself.</span></span>

<span data-ttu-id="f1472-119">ถ้าคุณกำลังประสบปัญหาเรื่องหน่วยความจำอยู่เสมอ มันอาจถึงเวลาแล้วที่จะมองไปที่การปรับใช้แบบแนวกว้าง เพื่อกระจายการใช้ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="f1472-119">If you are encountering memory pressure consistently, it may be worth looking at a scaled out deployment of the report server in order to spread the load of resources.</span></span> <span data-ttu-id="f1472-120">คุณยังสามารถกำหนดได้ว่า จะใช้เซิร์ฟเวอร์รายงานตัวไหนเพื่อรีเฟรช ด้วยการตั้งค่า `IsDataModelRefreshService` ภายใน rsreportserver.config ได้ ด้วยการตั้งค่านี้ คุณสามารถกำหนดหนึ่งหรือหลายเซิร์ฟเวอร์ ให้เป็นเซิร์ฟเวอร์ front end เพื่อจัดการกับรายงานตามความต้องการ และมีชุดของเซิร์ฟเวอร์อีกชุดที่จะใช้สำหรับรีเฟรชตามกำหนดเวลาเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f1472-120">You can also define that a given report server is used for data refresh with the `IsDataModelRefreshService` setting within rsreportserver.config. With this setting, you could define one or more servers to be the front end server to handle on demand reports, and have another set of servers to only be used for scheduled refresh.</span></span>

<span data-ttu-id="f1472-121">สำหรับข้อมูลเกี่ยวกับวิธีการตรวจสอบอินสแตนซ์ Analysis Services ดู[ตรวจสอบอินสแตนซ์ Analysis Services](/sql/analysis-services/instances/monitor-an-analysis-services-instance)</span><span class="sxs-lookup"><span data-stu-id="f1472-121">For information on how to monitor an Analysis Services instance, see [Monitor an Analysis Services Instance](/sql/analysis-services/instances/monitor-an-analysis-services-instance).</span></span>

<span data-ttu-id="f1472-122">สำหรับข้อมูลเกี่ยวกับการตั้งค่าหน่วยความจำภายใน Analysis Services ดู[คุณสมบัติหน่วยความจำ](/sql/analysis-services/server-properties/memory-properties)</span><span class="sxs-lookup"><span data-stu-id="f1472-122">For information about memory settings within Analysis Services, see [Memory Properties](/sql/analysis-services/server-properties/memory-properties).</span></span>

### <a name="kerberos-configuration"></a><span data-ttu-id="f1472-123">การกำหนดค่า Kerberos</span><span class="sxs-lookup"><span data-stu-id="f1472-123">Kerberos configuration</span></span>
<span data-ttu-id="f1472-124">การเชื่อมต่อกับแหล่งข้อมูลด้วยข้อมูลประจำตัว Windows อาจจำเป็นต้องกำหนดการมอบหมายที่มีข้อจำกัดของ Kerberos เพื่อให้การเชื่อมต่อสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="f1472-124">Connecting to a data source with windows credentials may require configuring Kerberos constrained delegation to make a successful connection.</span></span> <span data-ttu-id="f1472-125">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการกำหนดค่าการมอบหมายที่มีข้อจำกัดของ Kerberos ดู[การกำหนดค่า Kerberos เพื่อใช้กับ Power BI](configure-kerberos-powerbi-reports.md)</span><span class="sxs-lookup"><span data-stu-id="f1472-125">For more information about how to configure Kerberos constrained delegation, see [Configure Kerberos to use Power BI reports](configure-kerberos-powerbi-reports.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="f1472-126">รับทราบปัญหาแล้ว</span><span class="sxs-lookup"><span data-stu-id="f1472-126">Known issues</span></span>
<span data-ttu-id="f1472-127">ข้อมูลเกี่ยวกับปัญหาที่ทราบแล้ว จะแสดงอยู่ที่นี่เมื่อมีข้อมูลพร้อมให้บริการ</span><span class="sxs-lookup"><span data-stu-id="f1472-127">Information about known issues will be listed here when they become available.</span></span>

## <a name="configuration-settings"></a><span data-ttu-id="f1472-128">การกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="f1472-128">Configuration settings</span></span>
<span data-ttu-id="f1472-129">การตั้งค่าต่อไปนี้อาจมีผลต่อการรีเฟรชตามกำหนดเวลา</span><span class="sxs-lookup"><span data-stu-id="f1472-129">The following settings can be used to affect scheduled refresh.</span></span> <span data-ttu-id="f1472-130">การตั้งค่าที่ตั้งจากภายใน SQL Server Management Studio (SSMS) จะมีผลกับทุก ๆ เซิร์ฟเวอร์รายงาน ภายในการปรับใช้แบบแนวกว้าง</span><span class="sxs-lookup"><span data-stu-id="f1472-130">Settings set within SQL Server Management Studio (SSMS) apply to all report servers within a scale-out deployment.</span></span> <span data-ttu-id="f1472-131">การตั้งค่าที่กำหนดใน rsreportserver.config จะมีผลเฉพาะเซิร์ฟเวอร์ที่ตั้งค่านั้น</span><span class="sxs-lookup"><span data-stu-id="f1472-131">Settings configured within rsreportserver.config are for the specific server they are set on.</span></span>

<span data-ttu-id="f1472-132">**การตั้งค่าภายใน SSMS:**</span><span class="sxs-lookup"><span data-stu-id="f1472-132">**Settings within SSMS:**</span></span>

| <span data-ttu-id="f1472-133">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="f1472-133">Setting</span></span> | <span data-ttu-id="f1472-134">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f1472-134">Description</span></span> |
| --- | --- |
| <span data-ttu-id="f1472-135">MaxFileSizeMb</span><span class="sxs-lookup"><span data-stu-id="f1472-135">MaxFileSizeMb</span></span> |<span data-ttu-id="f1472-136">ขนาดไฟล์สูงสุดสำหรับรายงานที่อัปโหลด</span><span class="sxs-lookup"><span data-stu-id="f1472-136">Maximum file size for uploaded reports.</span></span> <span data-ttu-id="f1472-137">ค่าเริ่มต้นคือ 1000 MB (1 GB)</span><span class="sxs-lookup"><span data-stu-id="f1472-137">Default is 1000 MB (1 GB).</span></span> <span data-ttu-id="f1472-138">ค่าสูงสุดคือ 2000 MB (2 GB)</span><span class="sxs-lookup"><span data-stu-id="f1472-138">Maximum value is 2000 MB (2 GB).</span></span> |
| <span data-ttu-id="f1472-139">ModelCleanupCycleMinutes</span><span class="sxs-lookup"><span data-stu-id="f1472-139">ModelCleanupCycleMinutes</span></span> |<span data-ttu-id="f1472-140">กำหนดว่ารูปแบบมีการตรวจสอบบ่อยแค่ไหน เพื่อลบออกจากหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="f1472-140">Defines how often the model is checked to evict it from memory.</span></span> <span data-ttu-id="f1472-141">ค่าเริ่มต้นคือ 15 นาที</span><span class="sxs-lookup"><span data-stu-id="f1472-141">Default is 15 minutes.</span></span> |
| <span data-ttu-id="f1472-142">ModelExpirationMinutes</span><span class="sxs-lookup"><span data-stu-id="f1472-142">ModelExpirationMinutes</span></span> |<span data-ttu-id="f1472-143">กำหนดว่าเวลานานเท่าไรนับจากการใช้งานล่าสุด ที่รูปแบบจะหมดอายุและลบออกจากหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="f1472-143">Defines how long until the model expires based on the last time used and is evicted.</span></span> <span data-ttu-id="f1472-144">ค่าเริ่มต้นคือ 60 นาที</span><span class="sxs-lookup"><span data-stu-id="f1472-144">Default is 60 minutes.</span></span> |
| <span data-ttu-id="f1472-145">ScheduleRefreshTimeoutMinutes</span><span class="sxs-lookup"><span data-stu-id="f1472-145">ScheduleRefreshTimeoutMinutes</span></span> |<span data-ttu-id="f1472-146">กำหนดว่าการรีเฟรชข้อมูลสามารถใช้เวลานานแค่ไหน สำหรับแต่ละโหมด</span><span class="sxs-lookup"><span data-stu-id="f1472-146">Defines how long the data refresh can take for a mode.</span></span> <span data-ttu-id="f1472-147">ค่าเริ่มต้นคือ 120 นาที</span><span class="sxs-lookup"><span data-stu-id="f1472-147">Default is 120 minutes.</span></span> <span data-ttu-id="f1472-148">ไม่มีขีดจำกัดสูงสุด</span><span class="sxs-lookup"><span data-stu-id="f1472-148">There is no upper limit.</span></span> |

<span data-ttu-id="f1472-149">**การตั้งค่าภายใน rsreportserver.config:**</span><span class="sxs-lookup"><span data-stu-id="f1472-149">**Settings within rsreportserver.config:**</span></span>

```xml
<Configuration>
    <Service>
        <PollingInterval>10</PollingInterval>
        <IsDataModelRefreshService>false</IsDataModelRefreshService>
        <MaxQueueThreads>0</MaxQueueThreads>
    </Service>
</Configuration>
```

## <a name="tools-for-troubleshooting"></a><span data-ttu-id="f1472-150">เครื่องมือสำหรับการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="f1472-150">Tools for troubleshooting</span></span>
### <a name="logs-relevant-for-scheduled-refresh-of-power-bi-reports"></a><span data-ttu-id="f1472-151">บันทึกที่เกี่ยวข้องกับการรีเฟรชตามกำหนดเวลาของรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="f1472-151">Logs relevant for scheduled refresh of Power BI reports</span></span>
<span data-ttu-id="f1472-152">แฟ้มบันทึกที่เก็บข้อมูลเกี่ยวกับการรีเฟรชตามกำหนดเวลาได้แก่ ล็อกของ RSPowerBI_</span><span class="sxs-lookup"><span data-stu-id="f1472-152">The log files which hold information about scheduled refresh are the RSPowerBI_ logs.</span></span> <span data-ttu-id="f1472-153">บันทึกดังกล่าวอยู่ในโฟลเดอร์ LogFiles ของตำแหน่งการติดตั้งเซิร์ฟเวอร์รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="f1472-153">They are located in the LogFiles folder of your report server installation location.</span></span> 

```
C:\Program Files\Microsoft Power BI Report Server\PBIRS\LogFiles\RSPowerBI_*.log
```

<span data-ttu-id="f1472-154">**เงื่อนไขข้อผิดพลาด**</span><span class="sxs-lookup"><span data-stu-id="f1472-154">**Error condition**</span></span>

```
2017-10-20 02:00:09.5188|ERROR|744|Error Processing Data Model Refresh: SessionId: e960c25e-ddd4-4763-aa78-0e5dceb53472, Status: Error Model can not be refreshed because not all the data sources are embedded, Exception Microsoft.PowerBI.ReportServer.AsServer.InvalidDataSourceException: Model can not be refreshed because not all the data sources are embedde
   at Microsoft.PowerBI.ReportServer.WebHost.EventHandler.AnalysisServicesDataRefresh.CanModelRefresh(IEnumerable`1 dataSources)
   at Microsoft.PowerBI.ReportServer.WebHost.EventHandler.DataRefreshScope.<>c__DisplayClass7.<ExecuteActionWithLogging>b__5()
   at Microsoft.PowerBI.ReportServer.WebHost.EventHandler.DataRefreshScope.<ExecuteFuncWithLogging>d__1`1.MoveNext()
```

<span data-ttu-id="f1472-155">\**_การรีเฟรชที่สำเร็จ_* _</span><span class="sxs-lookup"><span data-stu-id="f1472-155">\**_Successful refresh_* _</span></span>

```
2017-10-25 15:23:41.9370|INFO|6|Handling event with data: TimeEntered: 10/25/2017 8:23:41 PM, Type: Event, SessionId: 46d398db-0b1f-49d8-b7bd-c5461c07ec7a, EventType: DataModelRefresh
2017-10-25 15:23:41.9370|INFO|6|Processing Data Model Refresh: SessionId: 46d398db-0b1f-49d8-b7bd-c5461c07ec7a, Status: Starting Data Refresh.
2017-10-25 15:23:41.9370|INFO|6|Processing Data Model Refresh: SessionId: 46d398db-0b1f-49d8-b7bd-c5461c07ec7a, Status: Starting Retrieving PBIX AsDatabaseInfo.
2017-10-25 15:23:42.7134|INFO|6|Processing Data Model Refresh: SessionId: 46d398db-0b1f-49d8-b7bd-c5461c07ec7a, Status: Starting Verifying all the data sources are embedded.
2017-10-25 15:23:42.7134|INFO|6|Processing Data Model Refresh: SessionId: 46d398db-0b1f-49d8-b7bd-c5461c07ec7a, Status: Starting Verifying connection strings are valid.
2017-10-25 15:23:42.7134|INFO|6|Processing Data Model Refresh: SessionId: 46d398db-0b1f-49d8-b7bd-c5461c07ec7a, Status: Starting Streaming model to Analysis Server.
2017-10-25 15:23:42.7603|INFO|6|Processing Data Model Refresh: SessionId: 46d398db-0b1f-49d8-b7bd-c5461c07ec7a, Status: Starting Refreshing the model.
2017-10-25 15:23:51.5258|INFO|6|Processing Data Model Refresh: SessionId: 46d398db-0b1f-49d8-b7bd-c5461c07ec7a, Status: Starting Removing credentials from the model.
2017-10-25 15:23:51.6508|INFO|6|Processing Data Model Refresh: SessionId: 46d398db-0b1f-49d8-b7bd-c5461c07ec7a, Status: Starting Saving model to the catalog.
```

<span data-ttu-id="f1472-156">_ *ข้อมูลประจำตัวไม่ถูกต้อง*\*</span><span class="sxs-lookup"><span data-stu-id="f1472-156">_ *Incorrect Credentials*\*</span></span>

```
2017-10-20 08:22:01.5595|INFO|302|Processing Data Model Refresh: SessionId: 22cd9ec3-b21a-4eb1-81ae-15fac8d379ea, Status: Starting Refreshing the model.
2017-10-20 08:22:02.3758|ERROR|302|Error Processing Data Model Refresh: SessionId: 22cd9ec3-b21a-4eb1-81ae-15fac8d379ea, Status: Error Failed to refresh the model, Exception Microsoft.AnalysisServices.OperationException: Failed to save modifications to the server. Error returned: 'The credentials provided for the SQL source are invalid. (Source at rosecatalog;reportserver.). The exception was raised by the IDbCommand interface.
'.
   at Microsoft.AnalysisServices.Tabular.Model.SaveChanges(SaveOptions saveOptions)
   at Microsoft.PowerBI.ReportServer.AsServer.TOMWrapper.RefreshModel(Database database)
   at Microsoft.PowerBI.ReportServer.AsServer.AnalysisServicesServer.RefreshDatabase(String databaseName, IEnumerable`1 dataSources)
   at Microsoft.PowerBI.ReportServer.WebHost.EventHandler.AnalysisServicesDataRefresh.RefreshDatabase(AsDatabaseInfo asDatabaseInfo)
   at Microsoft.PowerBI.ReportServer.WebHost.EventHandler.DataRefreshScope.<>c__DisplayClass7.<ExecuteActionWithLogging>b__5()
   at Microsoft.PowerBI.ReportServer.WebHost.EventHandler.DataRefreshScope.<ExecuteFuncWithLogging>d__1`1.MoveNext()
2017-10-20 08:22:02.4588|ERROR|302|Error Processing Data Model Refresh: SessionId: 22cd9ec3-b21a-4eb1-81ae-15fac8d379ea, Status: Error Failed Data Refresh, Exception Microsoft.AnalysisServices.OperationException: Failed to save modifications to the server. Error returned: 'The credentials provided for the SQL source are invalid. (Source at rosecatalog;reportserver.). The exception was raised by the IDbCommand interface.
'.
   at Microsoft.PowerBI.ReportServer.WebHost.EventHandler.DataRefreshScope.ExecuteActionWithLogging(Action methodToExecute, String description, String localizedDescription, String messageInFailure, RefreshInfo refreshInfo, DataAccessors dataAccessors, ReportEventType operation, Int64 size, Boolean isDataRetrieval, Boolean showInExecutionLog)
   at Microsoft.PowerBI.ReportServer.WebHost.EventHandler.AnalysisServicesDataRefresh.RefreshData(RefreshInfo refreshInfo)
   at Microsoft.PowerBI.ReportServer.WebHost.EventHandler.DataRefreshScope.<>c__DisplayClass7.<ExecuteActionWithLogging>b__5()
   at Microsoft.PowerBI.ReportServer.WebHost.EventHandler.DataRefreshScope.<ExecuteFuncWithLogging>d__1`1.MoveNext()
```

#### <a name="enabling-verbose-logging"></a><span data-ttu-id="f1472-157">เปิดใช้งานการบันทึกแบบละเอียด</span><span class="sxs-lookup"><span data-stu-id="f1472-157">Enabling Verbose Logging</span></span>
<span data-ttu-id="f1472-158">เปิดใช้งานการบันทึกแบบละเอียด ในเซิร์ฟเวอร์รายงาน Power BI จะเหมือนกับใน SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="f1472-158">Enabling verbose logging, in Power BI Report Server, is the same as it is for SQL Server Reporting Services.</span></span>

1. <span data-ttu-id="f1472-159">เปิด `<install directory>\PBIRS\ReportServer\bin\ReportingServicesService.exe.config`</span><span class="sxs-lookup"><span data-stu-id="f1472-159">Open `<install directory>\PBIRS\ReportServer\bin\ReportingServicesService.exe.config`.</span></span>
2. <span data-ttu-id="f1472-160">ภายใต้ `<system.diagnostics>` เปลี่ยน **DefaultTraceSwitch** เป็น **4**</span><span class="sxs-lookup"><span data-stu-id="f1472-160">Under `<system.diagnostics>`, change **DefaultTraceSwitch** to **4**.</span></span>
3. <span data-ttu-id="f1472-161">ภายใต้ `<RStrace>` เปลี่ยน **Components** เป็น **all:4**</span><span class="sxs-lookup"><span data-stu-id="f1472-161">Under `<RStrace>`, change **Components** to **all:4**.</span></span> 

### <a name="executionlog"></a><span data-ttu-id="f1472-162">บันทึกการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="f1472-162">ExecutionLog</span></span>
<span data-ttu-id="f1472-163">เมื่อใดก็ตามที่มีการแสดงผลรายงาน Power BI หรือดำเนินการกับแผนการรีเฟรชตามกำหนดเวลา รายการใหม่จะถูกเพิ่มลงในบันทึกการดำเนินการในฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f1472-163">Whenever a Power BI report is rendered, or a schedule refresh plan is executed, new entries are added to the Execution Log in the database.</span></span> <span data-ttu-id="f1472-164">รายการดังกล่าวจะปรากฏอยู่ในมุมมอง **ExecutionLog3** ภายในฐานข้อมูลแค็ตตาล็อกของเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="f1472-164">These entries are available in the **ExecutionLog3** view within the report server catalog database.</span></span>

<span data-ttu-id="f1472-165">รายการบันทึกการดำเนินการสำหรับรายงาน Power BI แตกต่างจากรายการสำหรับรายงานชนิดอื่น</span><span class="sxs-lookup"><span data-stu-id="f1472-165">Execution log entries for Power BI reports differ from entries for other report types.</span></span>

* <span data-ttu-id="f1472-166">คอลัมน์ TimeRendering จะมีค่าเป็น 0 เสมอ</span><span class="sxs-lookup"><span data-stu-id="f1472-166">TimeRendering columns is always 0.</span></span> <span data-ttu-id="f1472-167">การแสดงผลของรายงาน Power BI เกิดขึ้นในเบราว์เซอร์ ไม่ได้อยู่ในเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="f1472-167">Rendering of Power BI reports happens in the browser, not in the server.</span></span>
* <span data-ttu-id="f1472-168">มีค่า Request Types ได้ 2 แบบและการดำเนินการที่เกิดขึ้นต่อมา:</span><span class="sxs-lookup"><span data-stu-id="f1472-168">There are 2 Request Types and subsequent item actions:</span></span>
  * <span data-ttu-id="f1472-169">**แบบโต้ตอบ**: เมื่อใดก็ตามที่มีการดูรายงาน</span><span class="sxs-lookup"><span data-stu-id="f1472-169">**Interactive**: whenever a report is being viewed.</span></span>
    * <span data-ttu-id="f1472-170">**ASModelStream**: เมื่อรูปแบบข้อมูลถูกสตรีมไปยัง Analysis Services จากแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="f1472-170">**ASModelStream**: when the data model is streamed to Analysis Services from the catalog.</span></span>
    * <span data-ttu-id="f1472-171">**ConceptualSchema**: เมื่อผู้ใช้คลิกดูรายงาน</span><span class="sxs-lookup"><span data-stu-id="f1472-171">**ConceptualSchema**: when user clicks on viewing the report.</span></span>
    * <span data-ttu-id="f1472-172">**QueryData**: เมื่อใดก็ตามที่ข้อมูลมีการร้องขอจากไคลเอ็นต์</span><span class="sxs-lookup"><span data-stu-id="f1472-172">**QueryData**: whenever data is being requested from client.</span></span>
  * <span data-ttu-id="f1472-173">**รีเฟรชแค**: เมื่อใดก็ตามที่มีการดำเนินการตามแผนการรีเฟรชตามกำหนดเวลา</span><span class="sxs-lookup"><span data-stu-id="f1472-173">**Refresh Cache**: whenever a schedule refresh plan has been executed.</span></span>
    * <span data-ttu-id="f1472-174">**ASModelStream**: เมื่อใดก็ตามที่รูปแบบข้อมูลถูกสตรีมไปยัง Analysis Services จากแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="f1472-174">**ASModelStream**: whenever the data model is streamed to Analysis Services from the catalog.</span></span>
    * <span data-ttu-id="f1472-175">**DataRefresh**: เมื่อใดก็ตามที่มีการรีเฟรชข้อมูลจากแหล่งข้อมูลหนึ่งหรือหลายแหล่ง</span><span class="sxs-lookup"><span data-stu-id="f1472-175">**DataRefresh**: whenever data is being refreshed from one or more data sources.</span></span>
    * <span data-ttu-id="f1472-176">**SaveToCatalog**: เมื่อใดก็ตามตัวที่รูปแบบข้อมูลถูกบันทึกกลับไปยังแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="f1472-176">**SaveToCatalog**: whenever the data model is being saved back to the catalog.</span></span>

## <a name="analysis-services"></a><span data-ttu-id="f1472-177">บริการด้านการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="f1472-177">Analysis Services</span></span>
<span data-ttu-id="f1472-178">อาจมีบางครั้งที่คุณต้องการปรับแก้ Analysis Services เพื่อวินิจฉัยปัญหา หรือปรับค่าขีดจำกัดหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="f1472-178">There may be times you want to modify Analysis Services for diagnosing issues, or adjust memory limits.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1472-179">ค่าเหล่านี้จะถูกตั้งค่าใหม่ทุกครั้งที่คุณอัปเกรดเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="f1472-179">These settings will be reset any time you upgrade the report server.</span></span> <span data-ttu-id="f1472-180">ตรวจสอบให้แน่ใจว่ามีการเก็บสำเนาของการเปลี่ยนแปลงของคุณ และนำกลับมาใช้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="f1472-180">Be sure to keep a copy of your changes and reapply them if needed.</span></span>
> 
> 

### <a name="install-location"></a><span data-ttu-id="f1472-181">ตำแหน่งที่ติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="f1472-181">Install location</span></span>
<span data-ttu-id="f1472-182">ค่าเริ่มต้นของตำแหน่งที่ติดตั้งเซิร์ฟเวอร์รายงาน Power BI และ Analysis Services มีดังนี้</span><span class="sxs-lookup"><span data-stu-id="f1472-182">The default location for Power BI Report Server, and Analysis Services is the following.</span></span>

`C:\Program Files\Microsoft Power BI Report Server\PBIRS\ASEngine`

### <a name="configuring-analysis-services-settings-msmdsrvini"></a><span data-ttu-id="f1472-183">การกำหนดค่า Analysis Services (msmdsrv.ini)</span><span class="sxs-lookup"><span data-stu-id="f1472-183">Configuring Analysis Services settings (msmdsrv.ini)</span></span>
<span data-ttu-id="f1472-184">ในไดเรกทอรี `<install directory>\PBIRS\ASEngine` คุณจะพบแฟ้ม *msmdsrv.ini* ซึ่งคุณสามารถใช้ควบคุมการตั้งค่าต่าง ฯ ของ Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f1472-184">In the `<install directory>\PBIRS\ASEngine` directory, you will find the *msmdsrv.ini* file, which you can use to control different settings of Analysis Services.</span></span> <span data-ttu-id="f1472-185">เมื่อคุณเปิดไฟล์นี้ คุณจะเห็นได้ทันทีว่า แฟ้มนี้ไม่มีการตั้งค่าทุกค่าที่คุณคาดว่าจะมีในแฟ้ม msmdsrv.ini</span><span class="sxs-lookup"><span data-stu-id="f1472-185">When you open this file, you will immediately realize that this file doesn't have all the settings you would expect in the msmdsrv.ini file.</span></span> 

<span data-ttu-id="f1472-186">เนื่องจากว่า กระบวนการ Analysis Services จริงที่เรียกใช้โดยเซิร์ฟเวอร์รายงาน Power BI จะเรียกใช้ภายใน `<install directory>\PBIRS\ASEngine\workspaces`</span><span class="sxs-lookup"><span data-stu-id="f1472-186">This is because the actual Analysis Services process that is run by Power BI Report Server is launched in `<install directory>\PBIRS\ASEngine\workspaces`.</span></span> <span data-ttu-id="f1472-187">ในโฟลเดอร์นั้น คุณจะเห็นแฟ้ม *msmdsrv.ini* แบบเต็มที่คุณคุ้นเคย</span><span class="sxs-lookup"><span data-stu-id="f1472-187">In that folder, you will see the full *msmdsrv.ini* file you are used to.</span></span> <span data-ttu-id="f1472-188">สิ่งสำคัญคือ ต้องไม่ปรับเปลี่ยนแฟ้มภายในโฟลเดอร์พื้นที่ทำงาน เพราะมันจะถูกเขียนทับทุกครั้งที่เปิดใช้ Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f1472-188">It is important not to modify the file within the workspaces folder as it is rewritten whenever the Analysis Services process launches.</span></span> <span data-ttu-id="f1472-189">ถ้าคุณต้องการควบคุมการตั้งค่า โปรดปรับเปลี่ยน msmdsrv.ini ในไดเรกทอรี `<install directory>\PBIRS\ASEngine`</span><span class="sxs-lookup"><span data-stu-id="f1472-189">If you want to control a setting, please do this by modifying msmdsrv.ini in the `<install directory>\PBIRS\ASEngine` directory.</span></span>

<span data-ttu-id="f1472-190">การตั้งค่าต่อไปนี้จะถูกตั้งค่าใหม่ ทุกครั้งที่เปิดใช้ Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f1472-190">The following settings are reset when ever the Analysis Services process is launched.</span></span> <span data-ttu-id="f1472-191">การเปลี่ยนแปลงใด ๆ ที่คุณทำกับค่าเหล่านี้จะไม่มีผล</span><span class="sxs-lookup"><span data-stu-id="f1472-191">Any changes you make to these will be ignored.</span></span>

* <span data-ttu-id="f1472-192">ConfigurationSettings\PrivateProcess</span><span class="sxs-lookup"><span data-stu-id="f1472-192">ConfigurationSettings\PrivateProcess</span></span>
* <span data-ttu-id="f1472-193">ConfigurationSettings\DataDir</span><span class="sxs-lookup"><span data-stu-id="f1472-193">ConfigurationSettings\DataDir</span></span>
* <span data-ttu-id="f1472-194">ConfigurationSettings\LogDir</span><span class="sxs-lookup"><span data-stu-id="f1472-194">ConfigurationSettings\LogDir</span></span>
* <span data-ttu-id="f1472-195">ConfigurationSettings\TempDir</span><span class="sxs-lookup"><span data-stu-id="f1472-195">ConfigurationSettings\TempDir</span></span>
* <span data-ttu-id="f1472-196">ConfigurationSettings\BackupDir</span><span class="sxs-lookup"><span data-stu-id="f1472-196">ConfigurationSettings\BackupDir</span></span>
* <span data-ttu-id="f1472-197">ConfigurationSettings\AllowedBrowsingFolders</span><span class="sxs-lookup"><span data-stu-id="f1472-197">ConfigurationSettings\AllowedBrowsingFolders</span></span>
* <span data-ttu-id="f1472-198">ConfigurationSettings\CrashReportsFolder</span><span class="sxs-lookup"><span data-stu-id="f1472-198">ConfigurationSettings\CrashReportsFolder</span></span>
* <span data-ttu-id="f1472-199">ConfigurationSettings\ExtensionDir</span><span class="sxs-lookup"><span data-stu-id="f1472-199">ConfigurationSettings\ExtensionDir</span></span>
* <span data-ttu-id="f1472-200">ConfigurationSettings\Port</span><span class="sxs-lookup"><span data-stu-id="f1472-200">ConfigurationSettings\Port</span></span>
* <span data-ttu-id="f1472-201">ConfigurationSettings\DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="f1472-201">ConfigurationSettings\DeploymentMode</span></span>
* <span data-ttu-id="f1472-202">ConfigurationSettings\ServerLocation</span><span class="sxs-lookup"><span data-stu-id="f1472-202">ConfigurationSettings\ServerLocation</span></span>
* <span data-ttu-id="f1472-203">ConfigurationSettings\TMCompatabilitySKU</span><span class="sxs-lookup"><span data-stu-id="f1472-203">ConfigurationSettings\TMCompatabilitySKU</span></span>
* <span data-ttu-id="f1472-204">ConfigurationSettings\FlightRecorder\TraceDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="f1472-204">ConfigurationSettings\FlightRecorder\TraceDefinitionFile</span></span>

### <a name="profiling-the-local-analysis-services-process"></a><span data-ttu-id="f1472-205">การทำโพรไฟล์กระบวนการ Analysis Services ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="f1472-205">Profiling the local Analysis Services process</span></span>
<span data-ttu-id="f1472-206">การติดตาม SQL Profiler สามารถเรียกใช้ได้ในเครื่องของ Analysis Services สำหรับการวินิจฉัยปัญหา</span><span class="sxs-lookup"><span data-stu-id="f1472-206">A SQL Profiler trace can be run on the local Analysis Services process for diagnostic purposes.</span></span> <span data-ttu-id="f1472-207">เมื่อต้องการเชื่อมต่อกับอินสแตนซ์ Analysis Services ภายในเครื่อง ให้ทำสิ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f1472-207">To connect to the local Analysis Services instance, do the following.</span></span>

<span data-ttu-id="f1472-208">การติดตาม SQL Server Profiler จะรวมอยู่ในการ[ดาวน์โหลด SQL Server Management Studio (SSMS)](/sql/ssms/download-sql-server-management-studio-ssms) เรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="f1472-208">SQL Server Profiler Trace is included with the [SQL Server Management Studio (SSMS) download](/sql/ssms/download-sql-server-management-studio-ssms).</span></span>

1. <span data-ttu-id="f1472-209">เริ่มต้น **SQL Server Profiler** ด้วยสิทธิ์ผู้ดูแล</span><span class="sxs-lookup"><span data-stu-id="f1472-209">Start **SQL Server Profiler** as an administrator.</span></span>
2. <span data-ttu-id="f1472-210">เลือกปุ่ม **การติดตามใหม่**</span><span class="sxs-lookup"><span data-stu-id="f1472-210">Select the **New Trace** button.</span></span>
3. <span data-ttu-id="f1472-211">ในกล่องโต้ตอบ **เชื่อมต่อกับเซิร์ฟเวอร์** เลือก **Analysis Services** และใส่ **localhost:5132** สำหรับชื่อเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="f1472-211">In the **Connect to server** dialog, select **Analysis Services** and enter **localhost:5132** for the server name.</span></span>
4. <span data-ttu-id="f1472-212">ในกล่องโต้ตอบ **คุณสมบัติการติดตาม** เลือกเหตุการณ์คุณต้องการบันทึก และเลือก **เรียกใช้**</span><span class="sxs-lookup"><span data-stu-id="f1472-212">In the **Trace properties** dialog, select the events you want to capture and select **Run**.</span></span>

## <a name="lock-pages-in-memory-windows-privilege"></a><span data-ttu-id="f1472-213">สิทธิ์ Windows ในการล็อกหน้าในหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="f1472-213">Lock Pages In Memory Windows privilege</span></span>
<span data-ttu-id="f1472-214">ถ้าคุณพบว่า คุณจะไม่สามารถแสดงรายงาน Power BI การกำหนดสิทธิ์ **ล็อกหน้าในหน่วยความจำ** ให้กับบัญชีบริการที่เรียกใช้งาน เซิร์ฟเวอร์รายงาน Power BI อาจช่วยได้</span><span class="sxs-lookup"><span data-stu-id="f1472-214">If you find that you are unable to render a Power BI report, assigning the **Lock pages in memory** privilege to the services account running Power BI Report server may help.</span></span> <span data-ttu-id="f1472-215">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการกำหนดค่า **ล็อกหน้าในหน่วยความจำ** ดู [สิทธิ์การใช้งาน Windows ที่กำหนดให้กับบัญชีบริการ Analysis Services](/sql/analysis-services/instances/configure-service-accounts-analysis-services#bkmk_winpriv)</span><span class="sxs-lookup"><span data-stu-id="f1472-215">For more information about how to configure **Lock pages in memory**, see [Windows privileges assigned to the Analysis Services service account](/sql/analysis-services/instances/configure-service-accounts-analysis-services#bkmk_winpriv).</span></span>

<span data-ttu-id="f1472-216">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f1472-216">More questions?</span></span> [<span data-ttu-id="f1472-217">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="f1472-217">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)