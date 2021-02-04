---
title: อัปเกรด Power BI Report Server
description: เรียนรู้วิธีการอัปเกรด Power BI Report Server
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.custom: ''
ms.date: 09/22/2020
ms.openlocfilehash: 890b3c8124cc1711e08415cdcfda1f51b548fa63
ms.sourcegitcommit: 02484b2d7a352e96213353702d60c21e8c07c6c0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "91983079"
---
# <a name="upgrade-power-bi-report-server"></a><span data-ttu-id="87e6a-103">อัปเกรด Power BI Report Server</span><span class="sxs-lookup"><span data-stu-id="87e6a-103">Upgrade Power BI Report Server</span></span>

<span data-ttu-id="87e6a-104">เรียนรู้วิธีการอัปเกรด Power BI Report Server</span><span class="sxs-lookup"><span data-stu-id="87e6a-104">Learn how to upgrade Power BI Report Server.</span></span>

 <span data-ttu-id="87e6a-105">**ดาวน์โหลด** ![ไอคอนดาวน์โหลด](media/upgrade/download.png "ไอคอนดาวน์โหลด")</span><span class="sxs-lookup"><span data-stu-id="87e6a-105">**Download** ![download icon](media/upgrade/download.png "download icon")</span></span>

<span data-ttu-id="87e6a-106">เมื่อต้องการดาวน์โหลด Power BI Report Server และ Power BI Desktop ซึ่งปรับให้เหมาะสมที่สุดกับ Power BI Report Server ไปที่ [การรายงานภายในองค์กรกับ Power BI Report Server](https://powerbi.microsoft.com/report-server/)</span><span class="sxs-lookup"><span data-stu-id="87e6a-106">To download Power BI Report Server, and Power BI Desktop optimized for Power BI Report Server, go to [On-premises reporting with Power BI Report Server](https://powerbi.microsoft.com/report-server/).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="87e6a-107">ก่อนเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="87e6a-107">Before you begin</span></span>

<span data-ttu-id="87e6a-108">ก่อนที่คุณจะอัปเกรดเซิร์ฟเวอร์รายงานเราขอแนะนำให้ทำตามขั้นตอนต่อไปนี้เพื่อสำรองข้อมูลเซิร์ฟเวอร์รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="87e6a-108">Before you upgrade a report server, we recommend the following steps to back up your report server.</span></span>

### <a name="backing-up-the-encryption-keys"></a><span data-ttu-id="87e6a-109">การสำรองข้อมูลคีย์การเข้ารหัสลับ</span><span class="sxs-lookup"><span data-stu-id="87e6a-109">Backing up the encryption keys</span></span>

<span data-ttu-id="87e6a-110">คุณควรสำรองข้อมูลคีย์การเข้ารหัสลับเมื่อคุณกำหนดค่าการติดตั้งเซิร์ฟเวอร์รายงานเป็นครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="87e6a-110">Back up the encryption keys when you configure a report server installation for the first time.</span></span> <span data-ttu-id="87e6a-111">คุณควรสำรองข้อมูลคีย์ทุกครั้งที่คุณเปลี่ยนข้อมูลประจำตัวของบัญชีบริการหรือเปลี่ยนชื่อคอมพิวเตอร์</span><span class="sxs-lookup"><span data-stu-id="87e6a-111">Also back up the keys anytime you change the identity of the service accounts or rename the computer.</span></span> <span data-ttu-id="87e6a-112">สำหรับข้อมูลเพิ่มเติม ดู [สำรองข้อมูลและคืนค่าคีย์การเข้ารหัสลับบริการรายงาน](/sql/reporting-services/install-windows/ssrs-encryption-keys-back-up-and-restore-encryption-keys)</span><span class="sxs-lookup"><span data-stu-id="87e6a-112">For more information, see [Back Up and Restore Reporting Services Encryption Keys](/sql/reporting-services/install-windows/ssrs-encryption-keys-back-up-and-restore-encryption-keys).</span></span>

### <a name="backing-up-the-report-server-databases"></a><span data-ttu-id="87e6a-113">สำรองฐานข้อมูลเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="87e6a-113">Backing up the report server databases</span></span>

<span data-ttu-id="87e6a-114">เนื่องจากเซิร์ฟเวอร์รายงานเป็นเซิร์ฟเวอร์ไม่มีสถานะ ข้อมูลแอปพลิเคชันทั้งหมดจึงถูกเก็บไว้ในฐานข้อมูล **reportserver** และ **reportservertempdb**ที่ทำงานบนอินสแตนซ์ SQL Server Database Engine</span><span class="sxs-lookup"><span data-stu-id="87e6a-114">Because a report server is a stateless server, all application data is stored in the **reportserver** and **reportservertempdb** databases that run on a SQL Server Database Engine instance.</span></span> <span data-ttu-id="87e6a-115">คุณสามารถสำรองฐานข้อมูล **reportserver** และ **reportservertempdb** ได้โดยใช้หนึ่งในวิธีที่ได้รับการสนับสนุนสำหรับการสำรองฐานข้อมูล SQL Server</span><span class="sxs-lookup"><span data-stu-id="87e6a-115">You can back up the **reportserver** and **reportservertempdb** databases using one of the supported methods for backing up SQL Server databases.</span></span> <span data-ttu-id="87e6a-116">คำแนะนำเหล่านี้จะระบุไว้ในฐานข้อมูลเซิร์ฟเวอร์รายงาน:</span><span class="sxs-lookup"><span data-stu-id="87e6a-116">These recommendations are specific to report server databases:</span></span>

* <span data-ttu-id="87e6a-117">ใช้แบบจำลองการกู้คืนแบบเต็มอัตราเพื่อสำรองฐานข้อมูล **reportserver**</span><span class="sxs-lookup"><span data-stu-id="87e6a-117">Use the full recovery model to back up the **reportserver** database.</span></span>
* <span data-ttu-id="87e6a-118">ใช้แบบจำลองการกู้คืนอย่างง่ายเพื่อสำรองฐานข้อมูล **reportservertempdb**</span><span class="sxs-lookup"><span data-stu-id="87e6a-118">Use the simple recovery model to back up the **reportservertempdb** database.</span></span>
* <span data-ttu-id="87e6a-119">คุณสามารถใช้กำหนดการสำรองข้อมูลที่แตกต่างกันสำหรับแต่ละฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="87e6a-119">You can use different backup schedules for each database.</span></span> <span data-ttu-id="87e6a-120">เหตุผลเดียวที่ต้องสำรองข้อมูล **reportservertempdb** ก็คือเพื่อหลีกเลี่ยงการสร้างขึ้นใหม่หากฮาร์ดแวร์ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="87e6a-120">The only reason to back up the **reportservertempdb** is to avoid having to recreate it if there is a hardware failure.</span></span> <span data-ttu-id="87e6a-121">ในกรณีที่ฮาร์ดแวร์ล้มเหลว คุณไม่จำเป็นต้องกู้คืนข้อมูลใน **reportservertempdb** แต่คุณจำเป็นต้องมีโครงสร้างตาราง</span><span class="sxs-lookup"><span data-stu-id="87e6a-121">In case of hardware failure, you don't need to recover the data in **reportservertempdb**, but you do need the table structure.</span></span> <span data-ttu-id="87e6a-122">ถ้าคุณทำ **reportservertempdb**หายไป วิธีเดียวที่จะได้คืนมาก็คือ การสร้างฐานข้อมูลเซิร์ฟเวอร์รายงานขึ้นมาไป</span><span class="sxs-lookup"><span data-stu-id="87e6a-122">If you lose **reportservertempdb**, the only way to get it back is to recreate the report server database.</span></span> <span data-ttu-id="87e6a-123">หากคุณสร้าง **reportservertempdb** ขึ้นใหม่ สิ่งสำคัญคือต้องมีชื่อเดียวกับฐานข้อมูลเซิร์ฟเวอร์รายงานหลัก</span><span class="sxs-lookup"><span data-stu-id="87e6a-123">If you recreate the **reportservertempdb**, it's important that it have the same name as the primary report server database.</span></span>

<span data-ttu-id="87e6a-124">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสำรองและกู้คืนฐานข้อมูลเชิงสัมพันธ์ SQL Server ดู [สำรองข้อมูลและคืนค่าฐานข้อมูล SQL Server](/sql/relational-databases/backup-restore/back-up-and-restore-of-sql-server-databases)</span><span class="sxs-lookup"><span data-stu-id="87e6a-124">For more information about backup and recovery of SQL Server relational databases, see [Back Up and Restore of SQL Server Databases](/sql/relational-databases/backup-restore/back-up-and-restore-of-sql-server-databases).</span></span>

### <a name="backing-up-the-configuration-files"></a><span data-ttu-id="87e6a-125">การสำรองข้อมูลไฟล์กำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="87e6a-125">Backing up the configuration files</span></span>

<span data-ttu-id="87e6a-126">Power BI Report Server จะใช้ไฟลกำหนดค่าเพื่อจัดเก็บการตั้งค่าแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="87e6a-126">Power BI Report Server uses configuration files to store application settings.</span></span> <span data-ttu-id="87e6a-127">สำรองไฟล์เมื่อคุณกำหนดค่าเซิร์ฟเวอร์เป็นครั้งแรก และหลังจากที่คุณปรับใช้ส่วนขยายที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="87e6a-127">Back up the files when you first configure the server, and after you deploy any custom extensions.</span></span> <span data-ttu-id="87e6a-128">ไฟล์ที่จะสำรองข้อมูลประกอบด้วย:</span><span class="sxs-lookup"><span data-stu-id="87e6a-128">Files to back up include:</span></span>

* <span data-ttu-id="87e6a-129">config.json</span><span class="sxs-lookup"><span data-stu-id="87e6a-129">config.json</span></span>
* <span data-ttu-id="87e6a-130">RSHostingService.exe.config</span><span class="sxs-lookup"><span data-stu-id="87e6a-130">RSHostingService.exe.config</span></span>
* <span data-ttu-id="87e6a-131">Rsreportserver.config</span><span class="sxs-lookup"><span data-stu-id="87e6a-131">Rsreportserver.config</span></span>
* <span data-ttu-id="87e6a-132">Rssvrpolicy.config</span><span class="sxs-lookup"><span data-stu-id="87e6a-132">Rssvrpolicy.config</span></span>
* <span data-ttu-id="87e6a-133">Reportingservicesservice.exe.config</span><span class="sxs-lookup"><span data-stu-id="87e6a-133">Reportingservicesservice.exe.config</span></span>
* <span data-ttu-id="87e6a-134">Web.config สำหรับแอปพลิเคชัน Report Server ASP.NET</span><span class="sxs-lookup"><span data-stu-id="87e6a-134">Web.config for the Report Server ASP.NET applications</span></span>
* <span data-ttu-id="87e6a-135">Machine.config สำหรับ ASP.NET</span><span class="sxs-lookup"><span data-stu-id="87e6a-135">Machine.config for ASP.NET</span></span>

## <a name="upgrade-the-report-server"></a><span data-ttu-id="87e6a-136">การอัปเกรดเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="87e6a-136">Upgrade the report server</span></span>

<span data-ttu-id="87e6a-137">การอัปเกรดเซิร์ฟเวอร์รายงาน Power BI นั้นตรงไปตรงมา</span><span class="sxs-lookup"><span data-stu-id="87e6a-137">Upgrading Power BI Report Server is straightforward.</span></span> <span data-ttu-id="87e6a-138">มีเพียงไม่กี่ขั้นตอนในการติดตั้งไฟล์</span><span class="sxs-lookup"><span data-stu-id="87e6a-138">There are only a few steps to install the files.</span></span>

1. <span data-ttu-id="87e6a-139">ค้นหาตำแหน่งที่ตั้งของ PowerBIReportServer.exe และเปิดใช้งานตัวติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="87e6a-139">Find the location of PowerBIReportServer.exe and launch the installer.</span></span>

2. <span data-ttu-id="87e6a-140">เลือก **อัปเกรด Power BI Report Server**</span><span class="sxs-lookup"><span data-stu-id="87e6a-140">Select **Upgrade Power BI Report Server**.</span></span>

    <span data-ttu-id="87e6a-141">![อัปเกรด Power BI Report Server](media/upgrade/reportserver-upgrade1.png "อัปเกรด Power BI Report Server")</span><span class="sxs-lookup"><span data-stu-id="87e6a-141">![Upgrade Power BI Report Server](media/upgrade/reportserver-upgrade1.png "Upgrade Power BI Report Server")</span></span>

3. <span data-ttu-id="87e6a-142">อ่านและยอมรับเงื่อนไขและข้อกำหนดสิทธิ์การใช้งาน และจากนั้นเลือก **อัปเกรด**</span><span class="sxs-lookup"><span data-stu-id="87e6a-142">Read and agree to the license terms and conditions and then select **Upgrade**.</span></span>

    <span data-ttu-id="87e6a-143">![ข้อตกลงอนุญาตใช้สิทธิ์](media/upgrade/reportserver-upgrade-eula.png "ข้อตกลงอนุญาตใช้สิทธิ์")</span><span class="sxs-lookup"><span data-stu-id="87e6a-143">![License agreement](media/upgrade/reportserver-upgrade-eula.png "License agreement")</span></span>

4. <span data-ttu-id="87e6a-144">หลังจากอัปเกรดสำเร็จ คุณสามารถเลือก **กำหนดค่าเซิร์ฟเวอร์รายงาน**เพื่อเปิดใช้ตัวจัดการการกำหนดค่าบริการการรายงาน หรือเลือก **ปิด** เพื่ออกจากตัวติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="87e6a-144">After a successful upgrade, you can select **Configure Report Server** to launch the Reporting Services Configuration Manager, or select **Close** to exit the installer.</span></span>

    ![กำหนดค่าการอัปเกรด](media/upgrade/reportserver-upgrade-configure.png)

## <a name="enable-microsoft-update-security-fixes-for-power-bi-report-server"></a><span data-ttu-id="87e6a-146">เปิดใช้งานการแก้ไขความปลอดภัยของการอัปเดต Microsoft สำหรับเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="87e6a-146">Enable Microsoft Update security fixes for Power BI Report Server</span></span>

<span data-ttu-id="87e6a-147">เซิร์ฟเวอร์รายงาน Power BI ได้รับการแก้ไขด้านความปลอดภัยผ่านการอัปเดต Microsoft</span><span class="sxs-lookup"><span data-stu-id="87e6a-147">Power BI Report Server receives security fixes via Microsoft Update.</span></span> <span data-ttu-id="87e6a-148">หากต้องการเปิดใช้งานการรับให้เลือกใช้การอัปเดต Microsoft ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="87e6a-148">To enable getting them, manually opt in to Microsoft Update.</span></span>

1.  <span data-ttu-id="87e6a-149">เปิดการอัปเดต Windows ใน **การตั้งค่าการอัปเดตและความปลอดภัย** บนคอมพิวเตอร์ที่คุณต้องการเลือกใช้</span><span class="sxs-lookup"><span data-stu-id="87e6a-149">Open Windows Update in **Update & security settings** on the computer you want to opt in.</span></span>
2.  <span data-ttu-id="87e6a-150">เลือก **ตัวเลือกขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="87e6a-150">Select **Advanced options**.</span></span>
3.  <span data-ttu-id="87e6a-151">เลือกกล่องกาเครื่องหมายสำหรับ **แจ้งการอัปเดตสำหรับผลิตภัณฑ์อื่น ๆ ของ Microsoft เมื่อฉันอัปเดต Windows**</span><span class="sxs-lookup"><span data-stu-id="87e6a-151">Select the checkbox for **Give me updates for other Microsoft products when I update Windows**.</span></span>

## <a name="upgrade-power-bi-desktop"></a><span data-ttu-id="87e6a-152">อัปเกรด Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="87e6a-152">Upgrade Power BI Desktop</span></span>

<span data-ttu-id="87e6a-153">หลังจากที่คุณอัปเกรดเซิร์ฟเวอร์รายงาน ให้ตรวจสอบให้แน่ใจว่าผู้เขียนรายงาน Power BI ทุกคนได้อัปเกรดเป็นเวอร์ชันของ Power BI Desktop ที่ปรับให้เหมาะสมสำหรับเซิร์ฟเวอร์รายงาน Power BI ที่ตรงกับเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="87e6a-153">After you upgrade the report server, make sure that any Power BI report authors upgrade to the version of Power BI Desktop optimized for Power BI Report Server that matches the server.</span></span>

## <a name="next-steps"></a><span data-ttu-id="87e6a-154">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="87e6a-154">Next steps</span></span>

* [<span data-ttu-id="87e6a-155">ภาพรวมของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="87e6a-155">Administrator overview</span></span>](admin-handbook-overview.md)  
* [<span data-ttu-id="87e6a-156">ติดตั้ง Power BI Desktop ที่ปรับให้เหมาะสำหรับ Power BI Report Server</span><span class="sxs-lookup"><span data-stu-id="87e6a-156">Install Power BI Desktop optimized for Power BI Report Server</span></span>](install-powerbi-desktop.md)  
* [<span data-ttu-id="87e6a-157">ตรวจสอบการติดตั้งบริการการรายงาน</span><span class="sxs-lookup"><span data-stu-id="87e6a-157">Verify a Reporting Services installation</span></span>](/sql/reporting-services/install-windows/verify-a-reporting-services-installation)  
* [<span data-ttu-id="87e6a-158">กำหนดค่าบัญชีผู้ใช้บริการเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="87e6a-158">Configure the report server service account</span></span>](/sql/reporting-services/install-windows/configure-the-report-server-service-account-ssrs-configuration-manager)  
* [<span data-ttu-id="87e6a-159">กำหนดค่า URL ของเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="87e6a-159">Configure report server URLs</span></span>](/sql/reporting-services/install-windows/configure-report-server-urls-ssrs-configuration-manager)  
* [<span data-ttu-id="87e6a-160">กำหนดค่าการเชื่อมต่อฐานข้อมูลเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="87e6a-160">Configure a report server database connection</span></span>](/sql/reporting-services/install-windows/configure-a-report-server-database-connection-ssrs-configuration-manager)  
* [<span data-ttu-id="87e6a-161">เตรียมใช้งานเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="87e6a-161">Initialize a report server</span></span>](/sql/reporting-services/install-windows/ssrs-encryption-keys-initialize-a-report-server)  
* [<span data-ttu-id="87e6a-162">กำหนดค่าการเชื่อมต่อ SSL ในเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="87e6a-162">Configure SSL connections on a report server</span></span>](/sql/reporting-services/security/configure-ssl-connections-on-a-native-mode-report-server)  
* [<span data-ttu-id="87e6a-163">กำหนดค่าบัญชีบริการ windows และสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="87e6a-163">Configure windows service accounts and permissions</span></span>](/sql/database-engine/configure-windows/configure-windows-service-accounts-and-permissions)  
* [<span data-ttu-id="87e6a-164">การสนับสนุนเบราว์เซอร์สำหรับเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="87e6a-164">Browser support for Power BI Report Server</span></span>](browser-support.md)

<span data-ttu-id="87e6a-165">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="87e6a-165">More questions?</span></span> [<span data-ttu-id="87e6a-166">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="87e6a-166">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)