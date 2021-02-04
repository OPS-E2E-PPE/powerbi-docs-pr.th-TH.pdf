---
title: ดูรายงานและ KPI ภายในองค์กรในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่
description: แอป Power BI สำหรับอุปกรณ์เคลื่อนที่เสนอการใช้งานระบบสัมผัสที่เชื่อมต่อแบบสดเพื่อเข้าถึงข้อมูลทางธุรกิจภายในองค์กรของคุณใน SQL Server Reporting Services และเซิร์ฟเวอร์รายงาน Power BI
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 12/05/2019
ms.openlocfilehash: 18ad1be61202ddf189da064a833fddf6d793a2ba
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413414"
---
# <a name="view-on-premises-report-server-reports-and-kpis-in-the-power-bi-mobile-apps"></a><span data-ttu-id="f2df6-103">ดูรายงานจากรีพอร์ตเซิร์ฟเวอร์ภายในองค์กรและ KPI ในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="f2df6-103">View on-premises report server reports and KPIs in the Power BI mobile apps</span></span>

<span data-ttu-id="f2df6-104">แอป Power BI สำหรับอุปกรณ์เคลื่อนที่ให้คุณใช้งานในระบบสัมผัสที่เชื่อมต่อแบบสดเพื่อเข้าถึงข้อมูลทางธุรกิจภายในองค์กรของคุณในเซิร์ฟเวอร์รายงาน Power BI และ SQL Server 2016 Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="f2df6-104">The Power BI mobile apps deliver live, touch-enabled mobile access to your on-premises business information in Power BI Report Server and SQL Server 2016 Reporting Services (SSRS).</span></span>

<span data-ttu-id="f2df6-105">นำไปใช้กับ:</span><span class="sxs-lookup"><span data-stu-id="f2df6-105">Applies to:</span></span>

| ![iPhone](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/iphone-logo-50-px.png) | ![iPad](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/ipad-logo-50-px.png) | ![โทรศัพท์ Android](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/android-phone-logo-50-px.png) | ![แท็บเล็ต Android](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/android-tablet-logo-50-px.png) |
|:--- |:--- |:--- |:--- |
| <span data-ttu-id="f2df6-110">iPhone</span><span class="sxs-lookup"><span data-stu-id="f2df6-110">iPhones</span></span> |<span data-ttu-id="f2df6-111">iPad</span><span class="sxs-lookup"><span data-stu-id="f2df6-111">iPads</span></span> |<span data-ttu-id="f2df6-112">โทรศัพท์ Android</span><span class="sxs-lookup"><span data-stu-id="f2df6-112">Android phones</span></span> |<span data-ttu-id="f2df6-113">แท็บเล็ต Android</span><span class="sxs-lookup"><span data-stu-id="f2df6-113">Android tablets</span></span> |


![หน้าแรกของรีพอร์ตเซิร์ฟเวอร์ในแอปสำหรับอุปกรณ์เคลื่อนที่](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-ipad-pbi-report-server-home.png)

## <a name="first-things-first"></a><span data-ttu-id="f2df6-115">ขั้นแรก</span><span class="sxs-lookup"><span data-stu-id="f2df6-115">First things first</span></span>
<span data-ttu-id="f2df6-116">**แอปสำหรับอุปกรณ์เคลื่อนที่เป็นตำแหน่งที่คุณดูเนื้อหา Power BI ไม่ใช่ตำแหน่งที่คุณสร้างเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="f2df6-116">**The mobile apps are where you view Power BI content, not where you create it.**</span></span>

* <span data-ttu-id="f2df6-117">คุณและผู้สร้างรายงานคนอื่นๆ ในองค์กรของคุณ[สร้างรายงาน Power BI ด้วย Power BI Desktop จากนั้นเผยแพร่รายงานนั้นไปยังพอร์ทัลเว็บของเซิร์ฟเวอร์รายงาน Power BI](../../report-server/quickstart-create-powerbi-report.md)</span><span class="sxs-lookup"><span data-stu-id="f2df6-117">You and other report creators in your organization [create Power BI reports with Power BI Desktop, then publish them to the Power BI Report Server](../../report-server/quickstart-create-powerbi-report.md) web portal.</span></span> 
* <span data-ttu-id="f2df6-118">คุณสร้าง [KPI ในพอร์ทัลเว็บ](/sql/reporting-services/working-with-kpis-in-reporting-services)จัดระเบียบในโฟลเดอร์ และทำเครื่องหมายรายการโปรดของคุณเพื่อให้คุณสามารถค้นหาได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="f2df6-118">You create [KPIs right in the web portal](/sql/reporting-services/working-with-kpis-in-reporting-services), organize them in folders, and mark your favorites so you can find them easily.</span></span> 
* <span data-ttu-id="f2df6-119">คุณ[สร้างรายงานสำหรับอุปกรณ์เคลื่อนที่จาก Reporting Services](/sql/reporting-services/mobile-reports/create-mobile-reports-with-sql-server-mobile-report-publisher) ด้วย SQL Server 2016 Enterprise Edition Mobile Report Publisher และเผยแพร่รายงานนนั้นไปยัง[พอร์ทัลเว็บของ Reporting Services](/sql/reporting-services/web-portal-ssrs-native-mode)</span><span class="sxs-lookup"><span data-stu-id="f2df6-119">You [create Reporting Services mobile reports](/sql/reporting-services/mobile-reports/create-mobile-reports-with-sql-server-mobile-report-publisher) with SQL Server 2016 Enterprise Edition Mobile Report Publisher and publish them to the [Reporting Services web portal](/sql/reporting-services/web-portal-ssrs-native-mode).</span></span>  

<span data-ttu-id="f2df6-120">จากนั้น ในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่เชื่อมต่อกับรีพอร์ตเซิร์ฟเวอร์ได้ถึงห้าตัวเมื่อต้องการดูรายงาน Power BI และ KPI ที่ถูกจัดระเบียบในโฟลเดอร์หรือถูกเก็บรวบรวมเป็นรายการโปรด</span><span class="sxs-lookup"><span data-stu-id="f2df6-120">Then in the Power BI mobile apps, connect to up to five report servers to view the Power BI reports and KPIs, organized in folders or collected as favorites.</span></span> 

## <a name="explore-samples-in-the-mobile-apps-without-a-server-connection"></a><span data-ttu-id="f2df6-121">สำรวจตัวอย่างในแอปสำหรับอุปกรณ์เคลื่อนที่โดยไม่มีการเชื่อมต่อเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="f2df6-121">Explore samples in the mobile apps without a server connection</span></span>
<span data-ttu-id="f2df6-122">แม้ว่าคุณไม่สามารถเข้าถึงพอร์ทัลเว็บของ Reporting Services คุณยังสามารถสำรวจฟีเจอร์ของรายงานสำหรับอุปกรณ์เคลื่อนที่ของ Reporting Services และ KPI</span><span class="sxs-lookup"><span data-stu-id="f2df6-122">Even if you don't have access to a Reporting Services web portal, you can still explore the features of Reporting Services mobile reports and KPIs.</span></span> 

1. <span data-ttu-id="f2df6-123">แตะรูปโปรไฟล์ของคุณที่มุมบนซ้ายจากนั้น แตะ **การตั้งค่า** บนแผงบัญชีที่เลื่อนออก</span><span class="sxs-lookup"><span data-stu-id="f2df6-123">Tap your profile picture in the upper-left corner and then tap **Settings** on the accounts panel that slides out.</span></span>

2. <span data-ttu-id="f2df6-124">ในหน้าการตั้งค่าที่เปิด แตะ **ตัวอย่าง Reporting Services** จากนั้น เรียกดูเพื่อโต้ตอบกับตัวอย่าง KPI และรายงานสำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="f2df6-124">On the settings page that opens, tap **Reporting Services samples**, then browse to interact with the sample KPIs and mobile reports.</span></span>
   
   ![ตัวอย่างของบริการการรายงาน](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-iphone-ssrs-samples.png)

## <a name="connect-to-an-on-premises-report-server"></a><span data-ttu-id="f2df6-126">เชื่อมต่อกับเซิร์ฟเวอร์ภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="f2df6-126">Connect to an on-premises report server</span></span>
<span data-ttu-id="f2df6-127">คุณสามารถดูรายงาน Power BI สำหรับองค์กร รายงานจาก Reporting Services และ KPI ในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="f2df6-127">You can view on-premises Power BI reports, Reporting Services mobile reports, and KPIs in the Power BI mobile apps.</span></span> 

1. <span data-ttu-id="f2df6-128">บนอุปกรณ์เคลื่อนที่ เปิดแอป Power BI</span><span class="sxs-lookup"><span data-stu-id="f2df6-128">On your mobile device, open the Power BI app.</span></span>
2. <span data-ttu-id="f2df6-129">ถ้าคุณยังไม่ได้ลงชื่อเข้าใช้ Power BI แตะ **รีพอร์ตเซิร์ฟเวอร์**</span><span class="sxs-lookup"><span data-stu-id="f2df6-129">If you haven't signed in to Power BI yet, tap **Report Server**.</span></span>
   
   ![ลงชื่อเข้าใช้รีพอร์ตเซิร์ฟเวอร์](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-connect-to-rs-login.png)
   
   <span data-ttu-id="f2df6-131">หากคุณล็อกอินในแอป Power BI แล้ว ให้แตะรูปโปรไฟล์ของคุณที่มุมบนซ้ายจากนั้น แตะ **การตั้งค่า** บนแผงบัญชีที่เลื่อนออก</span><span class="sxs-lookup"><span data-stu-id="f2df6-131">If you've already signed in to the Power BI app, tap your profile picture in the upper-left corner and then tap **Settings** on the accounts pane that slides out.</span></span>
3. <span data-ttu-id="f2df6-132">บนหน้าการตั้งค่าที่เปิดขึ้น ให้แตะ **เชื่อมต่อกับเซิร์ฟเวอร์**</span><span class="sxs-lookup"><span data-stu-id="f2df6-132">On the settings page that opens, tap **Connect to server**.</span></span>
   
    ![เชื่อมต่อกับเซิร์ฟเวอร์](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-android-server-sign-in.png)

    <span data-ttu-id="f2df6-134">แอปสำหรับอุปกรณ์เคลื่อนที่จำเป็นต้องเข้าถึงเซิร์ฟเวอร์ในลักษณะบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="f2df6-134">The mobile app needs to access the server in some way.</span></span> <span data-ttu-id="f2df6-135">มีสองสามวิธีดำเนินการดังกล่าว:</span><span class="sxs-lookup"><span data-stu-id="f2df6-135">There are a few ways to do that:</span></span>
     * <span data-ttu-id="f2df6-136">การใช้เครือข่ายเดียวกัน/การใช้ VPN เป็นวิธีง่ายที่สุด</span><span class="sxs-lookup"><span data-stu-id="f2df6-136">Being on the same network/using VPN is the easiest way.</span></span>
     * <span data-ttu-id="f2df6-137">จำเป็นต้องใช้พร็อกซีของแอปพลิเคชันบนเว็บเพื่อเชื่อมต่อจากภายนอกองค์กร</span><span class="sxs-lookup"><span data-stu-id="f2df6-137">It's possible to use a Web Application Proxy to connect from outside the organization.</span></span> <span data-ttu-id="f2df6-138">ดู[ใช้ OAuth เพื่อเชื่อมต่อกับ Reporting Services ](mobile-oauth-ssrs.md)สำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="f2df6-138">See [Using OAuth to connect to Reporting Services](mobile-oauth-ssrs.md) for details.</span></span>
     * <span data-ttu-id="f2df6-139">เปิดการเชื่อมต่อ (พอร์ต) ในไฟร์วอลล์</span><span class="sxs-lookup"><span data-stu-id="f2df6-139">Open a connection (port) in the firewall.</span></span>

4. <span data-ttu-id="f2df6-140">กรอกที่อยู่เซิร์ฟเวอร์และตั้งชื่อเซอร์ฟเวอร์ หากคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="f2df6-140">Fill in the server address and give the server a friendly name, if you'd like.</span></span> <span data-ttu-id="f2df6-141">ใช้รูปแบบนี้สำหรับที่อยู่เซิร์ฟเวอร์:</span><span class="sxs-lookup"><span data-stu-id="f2df6-141">Use this format for the server address:</span></span>
   
     `https://<servername>/reports`
   
     <span data-ttu-id="f2df6-142">OR</span><span class="sxs-lookup"><span data-stu-id="f2df6-142">OR</span></span>
   
     `https://<servername>/reports`
   
   <span data-ttu-id="f2df6-143">ใส่ **http** หรือ **https** ด้านหน้าของสตริงการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="f2df6-143">Include **http** or **https** in front of the connection string.</span></span>
   
    ![เชื่อมต่อกับกล่องโต้ตอบของเซิร์ฟเวอร์](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-ios-connect-to-server-dialog.png)
5. <span data-ttu-id="f2df6-145">เมื่อคุณพิมพ์ที่อยู่เซิร์ฟเวอร์และตั้งชื่อเซิร์ฟเวอร์เมื่อต้องการแล้ว แตะ **เชื่อมต่อ** จากนั้นกรอกชื่อผู้ใช้และรหัสผ่านของคุณเมื่อมีข้อความขึ้นเตือน</span><span class="sxs-lookup"><span data-stu-id="f2df6-145">Once you've typed in the server address and optional friendly name, tap **Connect**, and then fill in your username and password when prompted.</span></span>
6. <span data-ttu-id="f2df6-146">ในตอนนี้คุณเห็นเซิร์ฟเวอร์ในหน้าต่างบัญชีในตัวอย่างนี้ เรียกว่า "Work Server"</span><span class="sxs-lookup"><span data-stu-id="f2df6-146">Now you see the server in the Accounts pane - in this example, it is called "Work server".</span></span>
   
   ![เซิร์ฟเวอร์รายงานในบานหน้าต่างนำทาง](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-iphone-left-nav-report-server.png)

## <a name="connect-to-an-on-premises-report-server-in-ios-or-android"></a><span data-ttu-id="f2df6-148">เชื่อมต่อกับเซิร์ฟเวอร์รายงานภายในองค์กรใน iOS หรือแอนดรอยด์</span><span class="sxs-lookup"><span data-stu-id="f2df6-148">Connect to an on-premises report server in iOS or Android</span></span>

<span data-ttu-id="f2df6-149">ถ้าคุณกำลังดู Power BI ในแอปสำหรับอุปกรณ์ iOS หรือแอนดรอยด์ ผู้ดูแลระบบ IT ของคุณอาจมีนโยบายการกำหนดค่าแอป</span><span class="sxs-lookup"><span data-stu-id="f2df6-149">If you're viewing Power BI in the iOS or Android mobile app, your IT admin may have defined an app configuration policy.</span></span> <span data-ttu-id="f2df6-150">ถ้าเป็นเช่นนั้น ประสบการณ์การเชื่อมต่อกับเซิร์ฟเวอร์รายงานของคุณถูกทำให้ง่ายขึ้น และคุณไม่ต้องใส่ข้อมูลมากเท่าเดิมเมื่อคุณเชื่อมต่อกับเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="f2df6-150">If so, your experience connecting to the report server is streamlined, and you won't have to provide as much information when you connect to a report server.</span></span> 

1. <span data-ttu-id="f2df6-151">คุณจะเห็นข้อความว่า แอปสำหรับอุปกรณ์เคลื่อนที่ของคุณได้กำหนดค่าสำหรับเซิร์ฟเวอร์รายงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="f2df6-151">You see a message that your mobile app is configured with a report server.</span></span> <span data-ttu-id="f2df6-152">แตะ **ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="f2df6-152">Tap **Sign in**.</span></span>

    ![ลงชื่อเข้าใช้เซิร์ฟเวอร์รายงาน](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-config-server-sign-in.png)

2.  <span data-ttu-id="f2df6-154">บนหน้า **เชื่อมต่อกับเซิร์ฟเวอร์** รายละเอียดของเซิร์ฟเวอร์รายงานได้ถูกกรอกให้แล้ว</span><span class="sxs-lookup"><span data-stu-id="f2df6-154">On the **Connect to server** page, the report server details already filled in.</span></span> <span data-ttu-id="f2df6-155">แตะ **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="f2df6-155">Tap **Connect**.</span></span>

    ![รายละเอียดของเซิร์ฟเวอร์รายงานที่กรอกให้แล้ว](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-ios-remote-configure-connect-server.png)

3. <span data-ttu-id="f2df6-157">พิมพ์รหัสผ่านเพื่อรับรองความถูกต้อง จากนั้นแตะ **ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="f2df6-157">Type a password to authenticate, then tap **Sign in**.</span></span> 

    ![สกรีนช็อตแสดงรายการรหัสผ่านพร้อมปุ่มลงชื่อเข้าใช้](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-config-server-address.png)

<span data-ttu-id="f2df6-159">ตอนนี้ คุณสามารถดูและโต้ตอบกับ KPI และรายงาน Power BI ที่จัดเก็บบนเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="f2df6-159">Now you can view and interact with KPIs and Power BI reports stored on the report server.</span></span>

## <a name="view-power-bi-reports-and-kpis-in-the-power-bi-app"></a><span data-ttu-id="f2df6-160">ดูรายงาน Power BI และ KPI ในแอป Power BI</span><span class="sxs-lookup"><span data-stu-id="f2df6-160">View Power BI reports and KPIs in the Power BI app</span></span>
<span data-ttu-id="f2df6-161">รายงาน Power BI รายงานสำหรับอุปกรณ์เคลื่อนที่ของ Reporting Services และ KPI จะแสดงอยู่ในโฟลเดอร์เดียวกันบนพอร์ทัลเว็บของ Reporting Services</span><span class="sxs-lookup"><span data-stu-id="f2df6-161">Power BI reports, Reporting Services mobile reports, and KPIs are displayed in the same folders they're in on the Reporting Services web portal.</span></span> 

* <span data-ttu-id="f2df6-162">แตะรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="f2df6-162">Tap a Power BI report</span></span> ![ไอคอนรายงานของ power BI](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-rs-mobile-report-icon.png)<span data-ttu-id="f2df6-164">.</span><span class="sxs-lookup"><span data-stu-id="f2df6-164">.</span></span> <span data-ttu-id="f2df6-165">การแตะจะเปิดโหมดแนวนอน และคุณสามารถโต้ตอบกับไฟล์ในแอป Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="f2df6-165">It opens in landscape mode, and you can interact with it in the Power BI app.</span></span>

    > [!NOTE]
  > <span data-ttu-id="f2df6-166">ดูรายละเอียดลงและขึ้นในขณะนี้ไม่ได้เปิดใช้งานในรายงานของ Power BI บนเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="f2df6-166">Drill down and up is currently not enabled in Power BI reports on a Power BI Report Server.</span></span>
  
    ![รายงาน power BI](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-iphone-report-server-report.png)
* <span data-ttu-id="f2df6-168">ใน Power BI Desktop เจ้าของรายงานสามารถ[ปรับรายงาน](../../create-reports/desktop-create-phone-report.md)ให้เหมาะสมสำหรับแอป Power BI สำหรับอุปกรณ์เคลื่อนที่ได้</span><span class="sxs-lookup"><span data-stu-id="f2df6-168">In Power BI Desktop, report owners can [optimize a report](../../create-reports/desktop-create-phone-report.md) for the Power BI mobile apps.</span></span> <span data-ttu-id="f2df6-169">บนโทรศัพท์มือถือ รายงานที่ปรับให้เหมาะสมจะมีไอคอนพิเศษ![ไอคอนรายงาน Power BI ที่ปรับให้เหมาะสม](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-rs-mobile-optimized-icon.png)และแบบการจัดหน้า</span><span class="sxs-lookup"><span data-stu-id="f2df6-169">On your mobile phone, optimized reports have a special icon, ![Optimized Power BI report icon](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-rs-mobile-optimized-icon.png), and layout.</span></span>
  
    ![รายงาน power BI ที่ปรับให้เหมาะสมสำหรับอุปกรณ์เคลื่อนที่](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-rs-mobile-optimized-report.png)
* <span data-ttu-id="f2df6-171">แตะ KPI เพื่อดูในโหมดโฟกัส</span><span class="sxs-lookup"><span data-stu-id="f2df6-171">Tap a KPI to see it in focus mode.</span></span>
  
    ![KPI ในโหมดโฟกัส](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/pbi_ipad_ssmrp_tile.png)

## <a name="view-your-favorite-kpis-and-reports"></a><span data-ttu-id="f2df6-173">ดู KPI และรายงานที่เป็นรายการโปรดของคุณ</span><span class="sxs-lookup"><span data-stu-id="f2df6-173">View your favorite KPIs and reports</span></span>
<span data-ttu-id="f2df6-174">คุณสามารถเพิ่ม KPIs และรายงานให้เป็นรายการโปรดบนพอร์ทัลเว็บ จากนั้น ดูข้อมูลดังกล่าวได้ในโฟลเดอร์หนึ่งที่สะดวกบนอุปกรณ์เคลื่อนที่ พร้อมกับแดชบอร์ดโปรด Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f2df6-174">You can mark KPIs and reports as favorites on the web portal, and then view them in one convenient folder on your mobile device, along with your Power BI favorite dashboards.</span></span>

* <span data-ttu-id="f2df6-175">แตะ **รายการโปรด** บนแถบนำทาง</span><span class="sxs-lookup"><span data-stu-id="f2df6-175">Tap **Favorites** on the navigation bar.</span></span>
  
   ![รายการโปรดในบานหน้าต่างนำทาง](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-ipad-faves-pbi-report-server-update.png)
  
   <span data-ttu-id="f2df6-177">KPI และรายงานโปรดจากพอร์ทัลเว็บของคุณจะอยู่บนหน้านี้ทั้งหมด พร้อมกับแดชบอร์ด Power BI ในบริการของ Power BI:</span><span class="sxs-lookup"><span data-stu-id="f2df6-177">Your favorite KPIs and reports from the web portal are all on this page, along with Power BI dashboards in the Power BI service:</span></span>
  
   ![รายงาน Power BI และแดชบอร์ดในหน้ารายการโปรด](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-ipad-favorites.png)

## <a name="remove-a-connection-to-a-report-server"></a><span data-ttu-id="f2df6-179">ยุติการเชื่อมต่อกับรีพอร์ตเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="f2df6-179">Remove a connection to a report server</span></span>
1. <span data-ttu-id="f2df6-180">เปิดหน้าต่างบัญชี แตะ **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="f2df6-180">Open the accounts pane, tap **Settings**.</span></span>
2. <span data-ttu-id="f2df6-181">แตะชื่อเซิร์ฟเวอร์ที่คุณไม่ต้องการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="f2df6-181">Tap the name of the server you don't want to be connected to.</span></span>
3. <span data-ttu-id="f2df6-182">แตะ **ถอดเซิร์ฟเวอร์**</span><span class="sxs-lookup"><span data-stu-id="f2df6-182">Tap **Remove Server**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f2df6-183">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="f2df6-183">Next steps</span></span>
* [<span data-ttu-id="f2df6-184">Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="f2df6-184">What is Power BI?</span></span>](../../fundamentals/power-bi-overview.md)  
* <span data-ttu-id="f2df6-185">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f2df6-185">Questions?</span></span> [<span data-ttu-id="f2df6-186">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="f2df6-186">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)