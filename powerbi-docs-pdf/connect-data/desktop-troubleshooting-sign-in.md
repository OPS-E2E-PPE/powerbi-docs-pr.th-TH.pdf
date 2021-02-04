---
title: การแก้ไขปัญหาลงชื่อเข้าใช้ใน Power BI Desktop
description: วิธีแก้ไขปัญหาทั่วไปสำหรับการลงชื่อเข้าใช้ Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: troubleshooting
ms.date: 03/05/2020
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 4a825c2e3bcfdbe637c59fde9c33dc23ad326b0e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96404422"
---
# <a name="troubleshooting-sign-in-for-power-bi-desktop"></a><span data-ttu-id="a635a-103">การแก้ไขปัญหาการลงชื่อเข้าใช้ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a635a-103">Troubleshooting sign-in for Power BI Desktop</span></span>
<span data-ttu-id="a635a-104">อาจมีเวลาเมื่อคุณพยายามลงชื่อเข้าใช้ **Power BI Desktop** แต่ต้องเผชิญกับพบข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="a635a-104">There may be times when you attempt to sign in to **Power BI Desktop** but run into errors.</span></span> <span data-ttu-id="a635a-105">มีสาเหตุหลักสองข้อสำหรับปัญหาในการลงชื่อเข้าใช้: **ข้อผิดพลาดการรับรองความถูกต้องพร็อกซี** และ **ข้อผิดพลาดในการเปลี่ยนเส้นทางไม่ใช่ HTTPS URL**</span><span class="sxs-lookup"><span data-stu-id="a635a-105">There are two primary reasons for sign-in trouble: **Proxy Authentication errors** and **Non-HTTPS URL redirect errors**.</span></span> 

<span data-ttu-id="a635a-106">เมื่อต้องการตรวจสอบปัญหาที่เป็นสาเหตุของปัญหาของคุณลงชื่อเข้าใช้ ขั้นแรกคือ การติดต่อผู้ดูแลระบบของคุณ และส่งข้อมูลการวินิจฉัย เพื่อให้พวกเขาสามารถระบุสาเหตุของปัญหาได้</span><span class="sxs-lookup"><span data-stu-id="a635a-106">To determine which problem is causing your sign-in issue, the first step is to contact your administrator and provide diagnostic information so that they can determine the cause of the issue.</span></span> <span data-ttu-id="a635a-107">จากการติดตามปัญหาที่เกี่ยวข้องกับการลงชื่อเข้าใช้ขอบคุณ ผู้ดูแลระบบสามารถตรวจสอบข้อผิดพลาดที่เกิดขึ้นกับคุณได้</span><span class="sxs-lookup"><span data-stu-id="a635a-107">By tracing issues associated with your sign-in problem, administrators can determine which of the following errors apply to you.</span></span> 

<span data-ttu-id="a635a-108">มาดูที่ปัญหาแต่ละอย่างเหล่านั้นตามลำดับกัน</span><span class="sxs-lookup"><span data-stu-id="a635a-108">Let's take a look at each of those issues in turn.</span></span> <span data-ttu-id="a635a-109">ส่วนท้ายของบทความนี้มีการอภิปรายเกี่ยวกับวิธีการตรวจจับ *การติดตาม* ใน Power BI Desktop ซึ่งจะช่วยคุณติดตามการแก้ไขปัญหาได้</span><span class="sxs-lookup"><span data-stu-id="a635a-109">At the end of this article is a discussion on how to capture a *trace* in Power BI Desktop, which can help track down troubleshooting issues.</span></span>


## <a name="proxy-authentication-required-error"></a><span data-ttu-id="a635a-110">ข้อผิดพลาดที่จำเป็นต้องมีการรับรองความถูกต้องของพร็อกซี</span><span class="sxs-lookup"><span data-stu-id="a635a-110">Proxy Authentication Required error</span></span>

<span data-ttu-id="a635a-111">หน้าจอต่อไปนี้แสดงตัวอย่างของข้อผิดพลาด  *ที่จำเป็นต้องมีการรับรองความถูกต้องของพร็อกซี*</span><span class="sxs-lookup"><span data-stu-id="a635a-111">The following screen shows an example of the *Proxy Authentication Required* error.</span></span>

![ข้อผิดพลาดในการลงชื่อเข้าใช้ของข้อผิดพลาดการรับรองความถูกต้องของพร็อกซี](media/desktop-troubleshooting-sign-in/desktop-tshoot-sign-in_01.png)

<span data-ttu-id="a635a-113">ข้อยกเว้นในไฟล์การติดตามของ *Power BI Desktop* ต่อไปนี้จะเกี่ยวข้องกับข้อผิดพลาดนี้:</span><span class="sxs-lookup"><span data-stu-id="a635a-113">The following exceptions in *Power BI Desktop* trace files are associated with this error:</span></span>

* <span data-ttu-id="a635a-114">*Microsoft.PowerBI.Client.Windows.Services.PowerBIWebException*</span><span class="sxs-lookup"><span data-stu-id="a635a-114">*Microsoft.PowerBI.Client.Windows.Services.PowerBIWebException*</span></span>
* <span data-ttu-id="a635a-115">*HttpStatusCode: ProxyAuthenticationRequired*</span><span class="sxs-lookup"><span data-stu-id="a635a-115">*HttpStatusCode: ProxyAuthenticationRequired*</span></span>

<span data-ttu-id="a635a-116">เมื่อมีข้อผิดพลาดนี้เกิดขึ้น สาเหตุส่วนใหญ่น่าจะเกิดจากเซิร์ฟเวอร์ที่รับรองความถูกต้องของพร็อกซีบนเครือข่ายของคุณบล็อกการร้องขอจากเว็บที่ออกโดย **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="a635a-116">When this error occurs, the most likely reason is that a proxy authentication server on your network is blocking the web requests issued by **Power BI Desktop**.</span></span> 

<span data-ttu-id="a635a-117">ถ้าเครือข่ายของคุณใช้เซิร์ฟเวอร์ที่รับรองความถูกต้องของพร็อกซี ผู้ดูแลระบบของคุณสามารถแก้ไขปัญหานี้ โดยเพิ่มโดเมนต่อไปนี้ในรายการอนุญาตบนเซิร์ฟเวอร์ที่รับรองความถูกต้องของพร็อกซี:</span><span class="sxs-lookup"><span data-stu-id="a635a-117">If your network uses a proxy authentication server, your administrator can fix this issue by adding the following domains to the allow list on the proxy authentication server:</span></span>

* <span data-ttu-id="a635a-118">app.powerbi.com</span><span class="sxs-lookup"><span data-stu-id="a635a-118">app.powerbi.com</span></span>
* <span data-ttu-id="a635a-119">api.powerbi.com</span><span class="sxs-lookup"><span data-stu-id="a635a-119">api.powerbi.com</span></span>
* <span data-ttu-id="a635a-120">โดเมนใน \*.analysis.windows.net namespace</span><span class="sxs-lookup"><span data-stu-id="a635a-120">domains in the \*.analysis.windows.net namespace</span></span>

<span data-ttu-id="a635a-121">สำหรับลูกค้าที่เป็นส่วนหนึ่งของระบบคลาวด์สำหรับส่วนราชการ การแก้ไขปัญหานี้สามารถทำได้โดยเพิ่มโดเมนต่อไปนี้ไปยังรายการอนุญาตบนเซิร์ฟเวอร์ที่รับรองความถูกต้องของพร็อกซี:</span><span class="sxs-lookup"><span data-stu-id="a635a-121">For customers who are part of a government cloud, fixing this issue can be done by adding the following domains to the allow list on the proxy authentication server:</span></span>

* <span data-ttu-id="a635a-122">app.powerbigov.us</span><span class="sxs-lookup"><span data-stu-id="a635a-122">app.powerbigov.us</span></span>
* <span data-ttu-id="a635a-123">api.powerbigov.us</span><span class="sxs-lookup"><span data-stu-id="a635a-123">api.powerbigov.us</span></span>
* <span data-ttu-id="a635a-124">โดเมนใน\*.analysis.usgovcloudapi.net namespace</span><span class="sxs-lookup"><span data-stu-id="a635a-124">domains in the \*.analysis.usgovcloudapi.net namespace</span></span>

## <a name="non-https-url-redirect-not-supported-error"></a><span data-ttu-id="a635a-125">ข้อผิดพลาดการเปลี่ยนเส้นทางที่ไม่ใช่ HTTPS URL ไม่ให้การสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="a635a-125">Non-HTTPS URL redirect not supported error</span></span>

<span data-ttu-id="a635a-126">**Power BI Desktop** เวอร์ชันปัจจุบันใช้ไลบรารีการรับรองความถูกต้องของ Active Directory (ADAL) เวอร์ชั่นปัจจุบัน ซึ่งไม่อนุญาตให้มีการเปลี่ยนเส้นทางไปยัง URL (ที่ไม่ใช่ HTTPS) ที่ไม่มีความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="a635a-126">Current versions of **Power BI Desktop** use the current version of the Active Directory Authentication Library (ADAL), which does not allow a redirect to non-secured (non-HTTPS) URLs.</span></span> 

<span data-ttu-id="a635a-127">ข้อยกเว้นในไฟล์การติดตามของ *Power BI Desktop* ต่อไปนี้จะเกี่ยวข้องกับข้อผิดพลาดนี้:</span><span class="sxs-lookup"><span data-stu-id="a635a-127">The following exceptions in *Power BI Desktop* trace files are associated with this error:</span></span>

* <span data-ttu-id="a635a-128">*Microsoft.IdentityModel.Clients.ActiveDirectory.AdalServiceException: ไม่รองรับข้อผิดพลาดการเปลี่ยนเส้นทางที่ไม่ใช่ HTTPS URL ใน webview*</span><span class="sxs-lookup"><span data-stu-id="a635a-128">*Microsoft.IdentityModel.Clients.ActiveDirectory.AdalServiceException: Non-HTTPS url redirect is not supported in webview*</span></span>
* <span data-ttu-id="a635a-129">*รหัสข้อผิดพลาด: non_https_redirect_failed*</span><span class="sxs-lookup"><span data-stu-id="a635a-129">*ErrorCode: non_https_redirect_failed*</span></span>

<span data-ttu-id="a635a-130">ถ้ามี *รหัสข้อผิดพลาด: non_https_redirect_failed* เกิดขึ้น หมายความว่า หน้าเปลี่ยนเส้นทางหรือผู้ให้บริการในสายการเปลี่ยนเส้นทางอย่างน้อยหนึ่งรายหรือมากกว่าไม่ใช่ปลายทาง HTTPS ที่ได้รับการคุ้มครอง หรือผู้ออกใบรับรองการเปลี่ยนเส้นทางอย่างน้อยหนึ่งเส้นทางหรือมากกว่าไม่ได้อยู่ระหว่างคำ รากที่เชื่อถือได้ของอุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="a635a-130">If the *ErrorCode: non_https_redirect_failed* occurs, it means that one or more redirect pages or providers in the redirect chain is not an HTTPS protected endpoint, or that a certificate issuer of one or more redirects is not among the device's trusted roots.</span></span> <span data-ttu-id="a635a-131">ผู้ให้บริการทั้งหมดในสายการเปลี่ยนเส้นทางใดๆก็ตามต้องมีการเข้าสู่ระบบต้องใช้ HTTPS URL</span><span class="sxs-lookup"><span data-stu-id="a635a-131">All providers in any sign-in redirect chain must use an HTTPS URL.</span></span> <span data-ttu-id="a635a-132">เมื่อต้องการแก้ไขปัญหานี้ ติดต่อผู้ดูแลระบบของคุณและขอให้ใช้ URL ที่มีความปลอดภัยสำหรับไซต์ที่รับรองความถูกต้องของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="a635a-132">To resolve this issue, contact your administrator and request that secured URLs be used for their authentication sites.</span></span> 

## <a name="how-to-collect-a-trace-in-power-bi-desktop"></a><span data-ttu-id="a635a-133">วิธีการรวบรวมการติดตามใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a635a-133">How to collect a trace in Power BI Desktop</span></span>

<span data-ttu-id="a635a-134">เมื่อต้องการรวบรวมการติดตามใน **Power BI Desktop** ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a635a-134">To collect a trace in **Power BI Desktop**, follow these steps:</span></span>

1. <span data-ttu-id="a635a-135">เปิดใช้งานการติดตามใน **Power BI Desktop** โดยไปที่ **ไฟล์ > ตัวเลือกและการตั้งค่า > ตัวเลือก** แล้วเลือก **การวินิจฉัย** จากตัวเลือกในบานหน้าต่างด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="a635a-135">Enable tracing in **Power BI Desktop** by going to **File > Options and settings > Options** and then select **Diagnostics** from the options in the left pane.</span></span> <span data-ttu-id="a635a-136">ในบานหน้าต่างที่ปรากฏขึ้น เลือกที่กล่องที่อยู่ถัดจาก **เปิดใช้งานการติดตาม** ดังที่แสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a635a-136">In the pane that appears, check the box next to **Enable tracing**, as shown in the following image.</span></span> <span data-ttu-id="a635a-137">คุณอาจจำเป็นต้องรีสตาร์ต **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="a635a-137">You may be required to restart **Power BI Desktop**.</span></span>
   
   ![เปิดใช้งานการติดตามใน Power BI Desktop](media/desktop-troubleshooting-sign-in/desktop-tshoot-sign-in_02.png)

2. <span data-ttu-id="a635a-139">แล้วทำตามขั้นตอนที่ทำให้เกิดข้อผิดพลาดอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="a635a-139">Then follow the steps that reproduce the error.</span></span> <span data-ttu-id="a635a-140">เมื่อเกิดกรณีเช่นนี้ **Power BI Desktop** จะเพิ่มเหตุการณ์ลงในบันทึกการติดตาม ที่ถูกเก็บอยู่บนคอมพิวเตอร์ภายใน</span><span class="sxs-lookup"><span data-stu-id="a635a-140">When that occurs, **Power BI Desktop** adds events to the tracing log, which is kept on the local computer.</span></span>

3. <span data-ttu-id="a635a-141">นำทางไปยังโฟลเดอร์ติดตามบนเครื่องคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a635a-141">Navigate to the Traces folder on your local computer.</span></span> <span data-ttu-id="a635a-142">คุณสามารถค้นหาโฟลเดอร์นั้นได้ โดยเลือกลิงก์ใน **การวินิจฉัย** ที่คุณเปิดใช้งานการติดตาม โดยให้แสดงเป็น *โฟลเดอร์บันทึกข้อมูลความล้มเหลว/การติดตาม*  ในภาพก่อนหน้าได้</span><span class="sxs-lookup"><span data-stu-id="a635a-142">You can find that folder by selecting the link in the **Diagnostics** where you enabled tracing, shown as *Open crash dump/traces folder* in the previous image.</span></span> <span data-ttu-id="a635a-143">บ่อยครั้งที่โฟลเดอร์นี้อาจถูกพบในตำแหน่งที่ตั้งต่อไปนี้ในคอมพิวเตอร์:</span><span class="sxs-lookup"><span data-stu-id="a635a-143">Often this is found on the local computer in the following location:</span></span>

    `C:\Users/<user name>/AppData/Local/Microsoft/Power BI Desktop/Traces`

<span data-ttu-id="a635a-144">อาจมีไฟล์การติดตามจำนวนมากในโฟลเดอร์นั้น</span><span class="sxs-lookup"><span data-stu-id="a635a-144">There may be many trace files in that folder.</span></span> <span data-ttu-id="a635a-145">ตรวจสอบให้แน่ใจว่าคุณส่งเฉพาะไฟล์ล่าสุดให้แก่ผู้ดูแลของคุณ เพื่อให้ง่ายต่อการระบุข้อผิดพลาดได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="a635a-145">Make sure you only send the recent files to your administrator to facilitate quickly identifying the error.</span></span> 


## <a name="using-default-system-credentials-for-web-proxy"></a><span data-ttu-id="a635a-146">การใช้ข้อมูลประจำตัวของระบบเริ่มต้นสำหรับเว็บพร็อกซี</span><span class="sxs-lookup"><span data-stu-id="a635a-146">Using default system credentials for web proxy</span></span>

<span data-ttu-id="a635a-147">คำขอทางเว็บที่ออกโดย Power BI Desktop ไม่ได้ใช้ข้อมูลประจำตัวของเว็บพร็อกซี</span><span class="sxs-lookup"><span data-stu-id="a635a-147">Web requests issued by Power BI Desktop do not use web proxy credentials.</span></span> <span data-ttu-id="a635a-148">ในเครือข่ายที่ใช้พร็อกซีเซิร์ฟเวอร์ Power BI Desktop อาจไม่สามารถทำการร้องขอทางเว็บได้สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="a635a-148">In networks that use a proxy server, Power BI Desktop may not be able to successfully make web requests.</span></span> 

<span data-ttu-id="a635a-149">เริ่มต้นด้วยการเผยแพร่ Power BI Desktop เดือนมีนาคม 2020 ผู้ดูแลระบบหรือผู้ดูแลเครือข่ายสามารถอนุญาตให้ใช้ข้อมูลประจำตัวของระบบค่าเริ่มต้นสำหรับการรับรองความถูกต้องของเว็บพร็อกซี</span><span class="sxs-lookup"><span data-stu-id="a635a-149">Starting with the March 2020 Power BI Desktop release, system or network administrators can allow the use of default system credentials for web proxy authentication.</span></span> <span data-ttu-id="a635a-150">ผู้ดูแลระบบสามารถสร้างรายการการลงทะเบียนที่เรียกว่า **UseDefaultCredentialsForProxy** และตั้งค่าเป็นหนึ่ง (1) เพื่อเปิดใช้งานการใช้ข้อมูลประจำตัวของระบบตามค่าเริ่มต้นสำหรับการรับรองความถูกต้องของเว็บพร็อกซี</span><span class="sxs-lookup"><span data-stu-id="a635a-150">Administrators can create a registry entry called **UseDefaultCredentialsForProxy**, and set the value to one (1) to enable the use of default system credentials for web proxy authentication.</span></span>

<span data-ttu-id="a635a-151">รายการการลงทะเบียนสามารถวางไว้ในตำแหน่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a635a-151">The registry entry can be placed in either of the following locations:</span></span>

`[HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Microsoft Power BI Desktop]`
`[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Microsoft Power BI Desktop]`

<span data-ttu-id="a635a-152">ไม่จำเป็นต้องมีรายการการลงทะเบียนในทั้งสองตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="a635a-152">It is not necessary to have the registry entry in both locations.</span></span>

![รหัสการลงทะเบียนสำหรับการใช้ข้อมูลประจำตัวของระบบตามค่าเริ่มต้น](media/desktop-troubleshooting-sign-in/desktop-tshoot-sign-in-03.png)

<span data-ttu-id="a635a-154">เมื่อมีการสร้างรายการการลงทะเบียน (อาจจำเป็นต้องรีบูต) ระบบจะใช้การตั้งค่าพร็อกซีที่ระบุไว้ใน Internet Explorer เมื่อ Power BI Desktop สร้างการร้องขอเว็บ</span><span class="sxs-lookup"><span data-stu-id="a635a-154">Once the registry entry is created (a reboot may be necessary) the proxy settings defined in Internet Explorer are used when Power BI Desktop makes web requests.</span></span> 

<span data-ttu-id="a635a-155">เช่นเดียวกับการเปลี่ยนแปลงใด ๆ กับพร็อกซีหรือการตั้งค่าข้อมูลประจำตัว มีผลกระทบด้านความปลอดภัยในการสร้างรายการการลงทะเบียนนี้ ดังนั้นผู้ดูแลระบบต้องตรวจสอบให้แน่ใจว่าตนเองได้กำหนดค่าพร็อกซี Internet Explorer อย่างถูกต้องแล้วก่อนที่จะเปิดใช้งานคุณลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="a635a-155">As with any change to proxy or credential settings, there are security implications to creating this registry entry, so administrators must make sure they have configured the Internet Explorer proxies correctly before enabling this feature.</span></span>         

### <a name="limitations-and-considerations-for-using-default-system-credentials"></a><span data-ttu-id="a635a-156">ขีดจำกัดและข้อควรพิจารณาสำหรับการใช้ข้อมูลประจำตัวของระบบตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a635a-156">Limitations and considerations for using default system credentials</span></span>

<span data-ttu-id="a635a-157">มีชุดของผลกระทบด้านความปลอดภัยที่ผู้ดูแลระบบควรพิจารณาก่อนเปิดใช้งานความสามารถนี้</span><span class="sxs-lookup"><span data-stu-id="a635a-157">There are a collection of security implications that administrators should consider before enabling this capability.</span></span> 

<span data-ttu-id="a635a-158">ควรทำตามคำแนะนำต่อไปนี้เมื่อใดก็ตามที่เปิดใช้งานคุณลักษณะนี้สำหรับไคลเอ็นต์:</span><span class="sxs-lookup"><span data-stu-id="a635a-158">The following recommendations should be followed whenever enabling this feature for clients:</span></span>

* <span data-ttu-id="a635a-159">ใช้ **การเจรจาต่อรอง** เป็นแบบแผนในการตรวจสอบความถูกต้องบนพร็อกซีเซิร์ฟเวอร์เท่านั้น เพื่อให้แน่ใจว่าไคลเอ็นต์ใช้งานเฉพาะพร็อกซีเซิร์ฟเวอร์ที่เข้าร่วมกับเครือข่าย Active Directory</span><span class="sxs-lookup"><span data-stu-id="a635a-159">Only use **Negotiation** as the authentication scheme on the for the proxy server, to ensure only proxy servers that are joined to the Active Directory network are used by the client.</span></span> 
* <span data-ttu-id="a635a-160">อย่าใช้ **การแสดงแทน NTLM** บนไคลเอ็นต์ที่ใช้คุณลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="a635a-160">Do not use **NTLM fallback** on clients that use this feature.</span></span>
* <span data-ttu-id="a635a-161">หากผู้ใช้ไม่ได้อยู่ในเครือข่ายที่มีพร็อกซีเมื่อเปิดใช้งานและกำหนดค่าคุณลักษณะนี้ตามที่แนะนำในส่วนนี้ จะไม่มีการใช้งานกระบวนการติดต่อพร็อกซีเซิร์ฟเวอร์และการใช้ข้อมูลประจำตัวของระบบตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a635a-161">If users are not on a network with a proxy when this feature is enabled and configured as recommended in this section, the process of attempting to contact the proxy server and using default system credentials is not used.</span></span>


[<span data-ttu-id="a635a-162">การใช้ข้อมูลประจำตัวของระบบตามค่าเริ่มต้นสำหรับเว็บพร็อกซี</span><span class="sxs-lookup"><span data-stu-id="a635a-162">Using default system credentials for web proxy</span></span>](#using-default-system-credentials-for-web-proxy)

