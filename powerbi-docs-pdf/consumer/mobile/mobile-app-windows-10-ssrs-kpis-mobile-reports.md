---
title: ดูรายงานและ KPI ภายในองค์กรในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่
description: แอปสำหรับอุปกรณ์เคลื่อนที่ Power BI สำหรับ Windows 10 มีคุณลักษณะการเข้าถึงผ่านอุปกรณ์เคลื่อนที่แบบสดและรองรับระบบสัมผัส เพื่อเข้าใช้งานข้อมูลทางธุรกิจที่สำคัญภายในองค์กรของคุณ
author: paulinbar
ms.author: painbar
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 05/19/2020
ms.openlocfilehash: eb6b86b2810609c0ad795190afc91c40677f5e70
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413322"
---
# <a name="view-on-premises-reports-and-kpis-in-the-power-bi-windows-app"></a><span data-ttu-id="86943-103">ดูรายงานและ KPI ภายในองค์กรในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="86943-103">View on-premises reports and KPIs in the Power BI Windows app</span></span>
<span data-ttu-id="86943-104">แอป Power BI สำหรับ Windows 10 มีการเข้าถึงแบบไลฟ์, touch ที่เปิดใช้งานการเชื่อมต่อกับข้อมูลทางธุรกิจภายในองค์กรที่สำคัญของคุณในReporting Services SQL Server 2016</span><span class="sxs-lookup"><span data-stu-id="86943-104">The Power BI app for Windows 10 offers live, touch-enabled mobile access to your important on-premises business information in SQL Server 2016 Reporting Services.</span></span> 

![รายงานอุปกรณ์มือถือของ Reporting Services](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/power-bi-ssrs-mobile-report.png)

## <a name="first-things-first"></a><span data-ttu-id="86943-106">สิ่งแรกที่ต้องทำ</span><span class="sxs-lookup"><span data-stu-id="86943-106">First things first</span></span>
<span data-ttu-id="86943-107">[สร้างรายงานอุปกรณ์มือถือของ Reporting Services](/sql/reporting-services/mobile-reports/create-mobile-reports-with-sql-server-mobile-report-publisher) ด้วย SQL Server 2016 Enterprise Edition Mobile Report Publisher แล้วเผยแพร่รายงานอุปกรณ์มือถือนั้นไปยัง [พอร์ทัลของเว็บ Reporting Services](/sql/reporting-services/web-portal-ssrs-native-mode)</span><span class="sxs-lookup"><span data-stu-id="86943-107">[Create Reporting Services mobile reports](/sql/reporting-services/mobile-reports/create-mobile-reports-with-sql-server-mobile-report-publisher) with SQL Server 2016 Enterprise Edition Mobile Report Publisher and publish them to the [Reporting Services web portal](/sql/reporting-services/web-portal-ssrs-native-mode).</span></span> <span data-ttu-id="86943-108">สร้าง KPI อย่างเหมาะสมในพอร์ทัลของเว็บ</span><span class="sxs-lookup"><span data-stu-id="86943-108">Create KPIs right in the web portal.</span></span> <span data-ttu-id="86943-109">จัดระเบียบรายงานอุปกรณ์มือถือในโฟลเดอร์ แล้วทำเครื่องหมายเป็นรายการโปรดของคุณ เพื่อให้คุณสามารถค้นหาได้ง่าย</span><span class="sxs-lookup"><span data-stu-id="86943-109">Organize them in folders and mark your favorites, so you can find them easily.</span></span> 

<span data-ttu-id="86943-110">จากนั้นในแอป Power BI สำหรับ Windows 10 ดู KPS รายงานมือถือและรายงาน Power BI จัดระเบียบในโฟลเดอร์หรือรวบรวมเป็นรายการโปรด</span><span class="sxs-lookup"><span data-stu-id="86943-110">Then in the Power BI app for Windows 10, view the KPS, mobile reports, and Power BI reports, organized in folders or collected as favorites.</span></span> 

> [!NOTE]
> <span data-ttu-id="86943-111">อุปกรณ์ของคุณจะต้องสามารถใช้งาน Windows 10 ได้</span><span class="sxs-lookup"><span data-stu-id="86943-111">Your device needs to be running Windows 10.</span></span> <span data-ttu-id="86943-112">แอปสามารถทำงานได้เต็มประสิทธิภาพในอุปกรณ์ที่มี RAM อย่างน้อย 1 GB และที่เก็บข้อมูลภายใน 8 GB</span><span class="sxs-lookup"><span data-stu-id="86943-112">The app works best on devices with at least 1 GB RAM and 8 GB internal storage.</span></span>

>[!NOTE]
><span data-ttu-id="86943-113">การสนับสนุนแอปอุปกรณ์เคลื่อนที่ Power BI สำหรับ **โทรศัพท์ที่ใช้ Windows 10 Mobile** จะถูกยกเลิกในวันที่ 16 มีนาคม 2021</span><span class="sxs-lookup"><span data-stu-id="86943-113">Power BI mobile app support for **phones using Windows 10 Mobile** will be discontinued on March 16, 2021.</span></span> [<span data-ttu-id="86943-114">ศึกษาเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="86943-114">Learn more</span></span>](/legal/powerbi/powerbi-mobile/power-bi-mobile-app-end-of-support-for-windows-phones)

## <a name="explore-samples-without-a-sql-server-2016-reporting-services-server"></a><span data-ttu-id="86943-115">สำรวจตัวอย่างโดยไม่มีเซิร์ฟเวอร์ SQL Server 2016 Reporting Services</span><span class="sxs-lookup"><span data-stu-id="86943-115">Explore samples without a SQL Server 2016 Reporting Services server</span></span>
<span data-ttu-id="86943-116">แม้ว่าคุณไม่สามารถเข้าถึงพอร์ทัลของเว็บ Reporting Services ได้ แต่ยังสามารถสำรวจดูคุณลักษณะต่างๆ ในรายงานอุปกรณ์มือถือของ Reporting Services ได้</span><span class="sxs-lookup"><span data-stu-id="86943-116">Even if you don't have access to a Reporting Services web portal, you can still explore the features of Reporting Services mobile reports.</span></span>

1. <span data-ttu-id="86943-117">ในอุปกรณ์ที่ใช้งาน Windows 10 ของคุณ ให้เปิดแอป Power BI</span><span class="sxs-lookup"><span data-stu-id="86943-117">In your Windows 10 device, open the Power BI app.</span></span>
2. <span data-ttu-id="86943-118">แตะปุ่มการนำทางส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="86943-118">Tap the global navigation button</span></span> ![ปุ่มการนำทางส่วนกลาง](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/powerbi_windows10_options_icon.png) <span data-ttu-id="86943-120">ในมุมบนซ้าย</span><span class="sxs-lookup"><span data-stu-id="86943-120">in the upper-left corner.</span></span>
3. <span data-ttu-id="86943-121">แตะไอคอน **การตั้งค่า**![ไอคอนการตั้งค่า](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/power-bi-settings-icon.png) คลิกขวา หรือแตะค้าง **เชื่อมต่อกับเซิร์ฟเวอร์** แล้วแตะ **ดูตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="86943-121">Tap **Settings** icon ![Settings icon](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/power-bi-settings-icon.png), right-click or tap and hold **Connect to server**, then tap **View samples**.</span></span>
   
   ![ดูตัวอย่างของ SSRS](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/power-bi-win10-connect-ssrs-samples.png)
4. <span data-ttu-id="86943-123">เปิดโฟลเดอร์รายงานการขายปลีกหรือรายงานการขาย เพื่อสำรวจ KPI และรายงานอุปกรณ์มือถือของโฟลเดอร์เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="86943-123">Open the Retail Reports or Sales Reports folder to explore their KPIs and mobile reports.</span></span>
   
   ![ตัวอย่าง KPIs และรายงานอุปกรณ์มือถือ](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/power-bi-win10-ssrs-sample-kpis.png)

<span data-ttu-id="86943-125">เรียกดูตัวอย่าง เพื่อโต้ตอบกับ KPI และรายงานอุปกรณ์มือถือ</span><span class="sxs-lookup"><span data-stu-id="86943-125">Browse the samples to interact with KPIs and mobile reports.</span></span>

## <a name="connect-to-a-reporting-services-report-server"></a><span data-ttu-id="86943-126">เชื่อมต่อกับรีพอร์ตเซิร์ฟเวอร์ของ Reporting Services</span><span class="sxs-lookup"><span data-stu-id="86943-126">Connect to a Reporting Services report server</span></span>
1. <span data-ttu-id="86943-127">ที่ด้านล่างของบานหน้าต่างนำทาง ให้แตะ **การตั้งค่า** ![ไอคอนการตั้งค่า](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/power-bi-settings-icon.png)</span><span class="sxs-lookup"><span data-stu-id="86943-127">At the bottom of the nav pane, tap **Settings** ![Settings icon](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/power-bi-settings-icon.png)</span></span>
2. <span data-ttu-id="86943-128">แตะ **เชื่อมต่อกับเซิร์ฟเวอร์**</span><span class="sxs-lookup"><span data-stu-id="86943-128">Tap **Connect to server**.</span></span>
3. <span data-ttu-id="86943-129">กรอกที่อยู่เซิร์ฟเวอร์ รวมทั้งชื่อผู้ใช้และรหัสผ่านของคุณ</span><span class="sxs-lookup"><span data-stu-id="86943-129">Fill in the server address and your user name and password.</span></span> <span data-ttu-id="86943-130">ใช้รูปแบบนี้สำหรับที่อยู่เซิร์ฟเวอร์:</span><span class="sxs-lookup"><span data-stu-id="86943-130">Use this format for the server address:</span></span>
   
     <span data-ttu-id="86943-131">`https://<servername>/reports` OR   `https://<servername>/reports`</span><span class="sxs-lookup"><span data-stu-id="86943-131">`https://<servername>/reports` OR   `https://<servername>/reports`</span></span>
   
   > [!NOTE]
   > <span data-ttu-id="86943-132">ใส่ **http** หรือ **https** ที่ด้านหน้าของสตริงการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="86943-132">Include **http** or **https** at the beginning of the connection string.</span></span>
   > 
   > 
   
    <span data-ttu-id="86943-133">แตะ **ตัวเลือกขั้นสูง** เพื่อตั้งชื่อให้เซิร์ฟเวอร์ ถ้าต้องการ</span><span class="sxs-lookup"><span data-stu-id="86943-133">Tap **Advanced option** to give the server a name, if you'd like.</span></span>
4. <span data-ttu-id="86943-134">แตะเครื่องหมายถูก เพื่อเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="86943-134">Tap the check mark to connect.</span></span> 
   
   <span data-ttu-id="86943-135">ในตอนนี้ คุณจะเห็นเซิร์ฟเวอร์อยู่ในบานหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="86943-135">Now you see the server in the nav pane.</span></span>
   
   ![เซิร์ฟเวอร์ในบานหน้าต่างนำทาง](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/power-bi-ssrs-mobile-report-server.png)
   
   >[!TIP]
   ><span data-ttu-id="86943-137">แตะปุ่มการนำทางส่วนกลาง ![ปุ่มการนำทางส่วนกลาง](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/powerbi_windows10_options_icon.png) ได้ตลอดเวลา เพื่อสลับไปมาระหว่างรายงานอุปกรณ์มือถือของ Reporting Services ของคุณกับแดชบอร์ดของคุณในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="86943-137">Tap the global navigation button ![Global navigation button](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/powerbi_windows10_options_icon.png) anytime to go between your Reporting Services mobile reports and your dashboards in the Power BI service.</span></span> 
   > 

   >[!NOTE]
   ><span data-ttu-id="86943-138">เซิร์ฟเวอร์รายงานที่กำหนดค่าด้วยพอร์ตที่กำหนดเองไม่ได้รับการสนับสนุน และไม่สามารถเข้าถึงได้จากแอป Power BI Windows</span><span class="sxs-lookup"><span data-stu-id="86943-138">Report Servers configured with custom ports are not supported and cannot be accessed from the Power BI Windows app.</span></span> 

## <a name="view-reporting-services-kpis-and-mobile-reports-in-the-power-bi-app"></a><span data-ttu-id="86943-139">ดู KPI และรายงานอุปกรณ์มือถือของ Reporting Services ในแอป Power BI</span><span class="sxs-lookup"><span data-stu-id="86943-139">View Reporting Services KPIs and mobile reports in the Power BI app</span></span>
<span data-ttu-id="86943-140">รายงาน Power BI รายงานสำหรับอุปกรณ์เคลื่อนที่ของบริการรายงานและ KPI จะแสดงอยู่ในโฟลเดอร์เดียวกันบนพอร์ทัลเว็บของบริการรายงาน</span><span class="sxs-lookup"><span data-stu-id="86943-140">Reporting Services KPIs, mobile reports, and Power BI reports (preview) are displayed in the same folders they're in on the Reporting Services web portal.</span></span>

![โฟลเดอร์รายงาน](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/power-bi-ssrs-mobile-report-folders.png)

* <span data-ttu-id="86943-142">แตะ KPI เพื่อดูในโหมดโฟกัส</span><span class="sxs-lookup"><span data-stu-id="86943-142">Tap a KPI to see it in focus mode.</span></span>
  
    ![KPI ในโหมดโฟกัส](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/power-bi-ssrs-mobile-report-kpis.png)
* <span data-ttu-id="86943-144">แตะรายงานอุปกรณ์มือถือ เพื่อเปิด และโต้ตอบกับรายงานอุปกรณ์มือถือนั้นในแอป Power BI</span><span class="sxs-lookup"><span data-stu-id="86943-144">Tap a mobile report to open and interact with it in the Power BI app.</span></span>
  
    ![รายงานอุปกรณ์มือถือของ Reporting Services](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/power-bi-ssrs-mobile-report.png)

## <a name="view-your-favorite-kpis-and-reports"></a><span data-ttu-id="86943-146">ดู KPI และรายงานที่เป็นรายการโปรดของคุณ</span><span class="sxs-lookup"><span data-stu-id="86943-146">View your favorite KPIs and reports</span></span>
<span data-ttu-id="86943-147">คุณสามารถทำเครื่องหมายให้ KPI และรายงานอุปกรณ์มือถือต่างๆ ในพอร์ทัลของเว็บบริการรายงานของคุณเป็นรายการโปรด จากนั้นดูรายการโปรดเหล่านี้ในโฟลเดอร์ใดโฟลเดอร์หนึ่งตามที่สะดวกในอุปกรณ์ Windows 10 ของคุณ รวมทั้งรายงานและแดชบอร์ดที่เป็นรายการโปรดใน Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="86943-147">You can mark KPIs, mobile reports, and Power BI reports as favorites on your Reporting Services web portal, and then view them in one convenient folder on your Windows 10 device, along with your Power BI favorite dashboards and reports.</span></span>

* <span data-ttu-id="86943-148">แตะ **รายการโปรด**</span><span class="sxs-lookup"><span data-stu-id="86943-148">Tap **Favorites**.</span></span>
  
   ![ไอคอนรายการโปรด](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/power-bi-ssrs-mobile-report-favorite-menu.png)
  
   <span data-ttu-id="86943-150">รายการโปรดของคุณจากพอร์ทัลของเว็บทั้งหมดล้วนอยู่ในหน้านี้</span><span class="sxs-lookup"><span data-stu-id="86943-150">Your favorites from the web portal are all on this page.</span></span>
  
<span data-ttu-id="86943-151">อ่านข้อมูลเพิ่มเติมเกี่ยวกับ [รายการโปรดในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่](mobile-apps-favorites.md)</span><span class="sxs-lookup"><span data-stu-id="86943-151">Read more about [favorites in the Power BI mobile apps](mobile-apps-favorites.md).</span></span>

## <a name="remove-a-connection-to-a-report-server"></a><span data-ttu-id="86943-152">ยุติการเชื่อมต่อกับรีพอร์ตเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="86943-152">Remove a connection to a report server</span></span>
<span data-ttu-id="86943-153">คุณสามารถเชื่อมต่อกับรีพอร์ตเซิร์ฟเวอร์จากแอป Power BI สำหรับอุปกรณ์เคลื่อนที่ได้เพียงครั้งละหนึ่งเซิร์ฟเวอร์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="86943-153">You can only be connected to one report server at a time from your Power BI mobile app.</span></span> <span data-ttu-id="86943-154">ถ้าคุณต้องการเชื่อมต่อกับเซิร์ฟเวอร์อื่น ก็จะต้องยกเลิกการเชื่อมต่อกับเซิร์ฟเวอร์ที่ใช้งานอยู่ในปัจจุบันก่อน</span><span class="sxs-lookup"><span data-stu-id="86943-154">If you want to connect to a different server, you need to disconnect from the current one.</span></span>

1. <span data-ttu-id="86943-155">ที่ด้านล่างของบานหน้าต่างนำทาง ให้แตะ **การตั้งค่า** ![ไอคอนการตั้งค่า](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/power-bi-settings-icon.png)</span><span class="sxs-lookup"><span data-stu-id="86943-155">At the bottom of the nav pane, tap **Settings** ![Settings icon](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/power-bi-settings-icon.png).</span></span>
2. <span data-ttu-id="86943-156">แตะค้างที่ชื่อเซิร์ฟเวอร์ที่คุณไม่ต้องการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="86943-156">Tap and hold the server name you don't want to be connected to.</span></span>
3. <span data-ttu-id="86943-157">แตะ **ลบเซิร์ฟเวอร์**</span><span class="sxs-lookup"><span data-stu-id="86943-157">Tap **Remove server**.</span></span>
   
    ![ลบเซิร์ฟเวอร์](media/mobile-app-windows-10-ssrs-kpis-mobile-reports/power-bi-windows-10-ssrs-remove-server-menu.png)

## <a name="create-reporting-services-mobile-reports-and-kpis"></a><span data-ttu-id="86943-159">สร้างรายงานอุปกรณ์มือถือและ KPI ของ Reporting Services</span><span class="sxs-lookup"><span data-stu-id="86943-159">Create Reporting Services mobile reports and KPIs</span></span>
<span data-ttu-id="86943-160">คุณไม่สามารถสร้าง KPI และรายงานอุปกรณ์มือถือของ Reporting Services ในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่ได้</span><span class="sxs-lookup"><span data-stu-id="86943-160">You don't create Reporting Services KPIs and mobile reports in the Power BI mobile app.</span></span> <span data-ttu-id="86943-161">คุณสามารถสร้างส่วนเหล่านั้นได้ใน SQL Server Mobile Report Publisher และพอร์ทัลของเว็บ SQL Server 2016 Reporting Services</span><span class="sxs-lookup"><span data-stu-id="86943-161">You create them in SQL Server Mobile Report Publisher and a SQL Server 2016 Reporting Services web portal.</span></span>

* <span data-ttu-id="86943-162">[สร้างรายงานอุปกรณ์มือถือของ Reporting Services ของคุณเอง](/sql/reporting-services/mobile-reports/create-mobile-reports-with-sql-server-mobile-report-publisher) แล้วเผยแพร่ไปยังพอร์ทัลของเว็บ Reporting Services</span><span class="sxs-lookup"><span data-stu-id="86943-162">[Create your own Reporting Services mobile reports](/sql/reporting-services/mobile-reports/create-mobile-reports-with-sql-server-mobile-report-publisher), and publish them to a Reporting Services web portal.</span></span>
* <span data-ttu-id="86943-163">สร้าง [KPI ในพอร์ทัลของเว็บ Reporting Services](/sql/reporting-services/working-with-kpis-in-reporting-services)</span><span class="sxs-lookup"><span data-stu-id="86943-163">Create [KPIs on a Reporting Services web portal](/sql/reporting-services/working-with-kpis-in-reporting-services)</span></span>

## <a name="next-steps"></a><span data-ttu-id="86943-164">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="86943-164">Next steps</span></span>
* [<span data-ttu-id="86943-165">เริ่มต้นใช้งานแอป Power BI สำหรับอุปกรณ์เคลื่อนที่สำหรับ Windows 10</span><span class="sxs-lookup"><span data-stu-id="86943-165">Get started with the Power BI mobile app for Windows 10</span></span>](mobile-windows-10-phone-app-get-started.md)  
* [<span data-ttu-id="86943-166">Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="86943-166">What is Power BI?</span></span>](../../fundamentals/power-bi-overview.md)  
* <span data-ttu-id="86943-167">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="86943-167">Questions?</span></span> [<span data-ttu-id="86943-168">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="86943-168">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)