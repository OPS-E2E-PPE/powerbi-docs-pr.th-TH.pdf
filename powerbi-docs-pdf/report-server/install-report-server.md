---
title: ติดตั้ง Power BI Report Server
description: เรียนรู้วิธีการติดตั้งเซิร์ฟเวอร์รายงาน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.date: 01/16/2020
ms.openlocfilehash: 049f6f563c9ac6e7494b0680b69e0df8909304d4
ms.sourcegitcommit: 9350f994b7f18b0a52a2e9f8f8f8e472c342ea42
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/22/2020
ms.locfileid: "90861900"
---
# <a name="install-power-bi-report-server"></a><span data-ttu-id="86f7b-103">ติดตั้ง Power BI Report Server</span><span class="sxs-lookup"><span data-stu-id="86f7b-103">Install Power BI Report Server</span></span>

<span data-ttu-id="86f7b-104">เรียนรู้วิธีการติดตั้งเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="86f7b-104">Learn how to install Power BI Report Server.</span></span>

## <a name="download-power-bi-report-server"></a><span data-ttu-id="86f7b-105">ดาวน์โหลดเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="86f7b-105">Download Power BI Report Server</span></span>

<span data-ttu-id="86f7b-106">ในหน้า[การรายงานภายในองค์กรกับเซิร์ฟเวอร์รายงาน Power BI](https://powerbi.microsoft.com/report-server/) เลือก**ดาวน์โหลดรุ่นทดลองใช้ฟรี**</span><span class="sxs-lookup"><span data-stu-id="86f7b-106">On the [On-premises reporting with Power BI Report Server](https://powerbi.microsoft.com/report-server/) page, select **Download free trial**.</span></span>

<span data-ttu-id="86f7b-107">เมื่อคุณเรียกใช้ไฟล์ PowerBIReportServer.exe คุณจะเลือกรุ่นทดลองใช้ฟรีหรือป้อนรหัสผลิตภัณฑ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="86f7b-107">When you run the PowerBIReportServer.exe file, you select the free trial or you enter your product key.</span></span> <span data-ttu-id="86f7b-108">อ่านรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="86f7b-108">Read on for details.</span></span>

## <a name="before-you-install"></a><span data-ttu-id="86f7b-109">ก่อนที่คุณจะติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="86f7b-109">Before you install</span></span>

<span data-ttu-id="86f7b-110">ก่อนที่คุณจะติดตั้ง Power BI Report Server เราขอแนะนำให้คุณตรวจสอบ [ข้อกำหนดของฮาร์ดแวร์และซอฟต์แวร์สำหรับการติดตั้ง Power BI Report Server](system-requirements.md)</span><span class="sxs-lookup"><span data-stu-id="86f7b-110">Before you install Power BI Report Server, we recommend you review the [Hardware and Software Requirements for installing Power BI Report Server](system-requirements.md).</span></span>

 > [!IMPORTANT]
 > <span data-ttu-id="86f7b-111">ในขณะที่คุณสามารถติดตั้งเซิร์ฟเวอร์รายงาน Power BI ในสภาพแวดล้อมที่มีตัวควบคุมโดเมนแบบอ่านอย่างเดียว (RODC), Power BI Report Server จำเป็นต้องเข้าถึงตัวควบคุมโดเมนแบบอ่าน-เขียนเพื่อให้ทำงานได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="86f7b-111">While you can install Power BI Report Server in an environment that has a Read-Only Domain Controller (RODC), Power BI Report Server needs access to a Read-Write Domain Controller to function properly.</span></span> <span data-ttu-id="86f7b-112">ถ้า Power BI Report Server สามารถเข้าถึง RODC ได้เท่านั้นคุณอาจพบข้อผิดพลาดเมื่อพยายามจัดการบริการ</span><span class="sxs-lookup"><span data-stu-id="86f7b-112">If Power BI Report Server only has access to a RODC, you may encounter errors when trying to administer the service.</span></span>

### <a name="power-bi-report-server-product-key"></a><span data-ttu-id="86f7b-113">คีย์ผลิตภัณฑ์เซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="86f7b-113">Power BI Report Server product key</span></span>

<span data-ttu-id="86f7b-114">คุณสามารถรับคีย์ผลิตภัณฑ์สำหรับเซิร์ฟเวอร์รายงาน Power BI จากแหล่งข้อมูลอื่นสองแห่ง:</span><span class="sxs-lookup"><span data-stu-id="86f7b-114">You can get the product key for Power BI Report Server from two different sources:</span></span>

- <span data-ttu-id="86f7b-115">Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="86f7b-115">Power BI Premium</span></span>
- <span data-ttu-id="86f7b-116">SQL Server Enterprise Software Assurance (SA)</span><span class="sxs-lookup"><span data-stu-id="86f7b-116">SQL Server Enterprise Software Assurance (SA)</span></span>

<span data-ttu-id="86f7b-117">อ่านรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="86f7b-117">Read on for details.</span></span>

#### <a name="power-bi-premium"></a><span data-ttu-id="86f7b-118">Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="86f7b-118">Power BI Premium</span></span>

<span data-ttu-id="86f7b-119">ถ้าคุณซื้อ Power BI Premium แล้ว ภายในแท็บ **การตั้งค่า Premium** ของพอร์ทัลผู้ดูแลระบบ Power BI คุณสามารถเข้าถึงคีย์ผลิตภัณฑ์ของเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="86f7b-119">If you've purchased Power BI Premium, within the **Premium settings** tab of the Power BI admin portal, you have access to your Power BI Report Server product key.</span></span> <span data-ttu-id="86f7b-120">พอร์ทัลผู้ดูแลระบบพร้อมใช้งานสำหรับผู้ดูแลระบบส่วนกลาง หรือผู้ใช้ที่ได้รับการกำหนดบทบาทเป็นผู้ดูแลระบบบริการของ Power BI เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="86f7b-120">The admin portal is only available to Global Admins or users assigned the Power BI service administrator role.</span></span>

<span data-ttu-id="86f7b-121">![การตั้งค่า Premium](../report-server/media/install-report-server/pbirs-product-key.png "คีย์เซิร์ฟเวอร์รายงาน Power BI ภายในการตั้งค่าขั้นสูง")</span><span class="sxs-lookup"><span data-stu-id="86f7b-121">![Premium settings](../report-server/media/install-report-server/pbirs-product-key.png "Power BI Report Server key within Premium settings")</span></span>

<span data-ttu-id="86f7b-122">การเลือก**คีย์เซิร์ฟเวอร์รายงาน Power BI** จะแสดงบทสนทนาที่มีคีย์ผลิตภัณฑ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="86f7b-122">Selecting **Power BI Report Server key** displays a dialog containing your product key.</span></span> <span data-ttu-id="86f7b-123">คุณสามารถคัดลอกคีย์และนำไปใช้กับการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="86f7b-123">You can copy it and use it with the installation.</span></span>

<span data-ttu-id="86f7b-124">![คีย์ผลิตภัณฑ์](../report-server/media/install-report-server/pbirs-product-key-dialog.png "คีย์ผลิตภัณฑ์เซิร์ฟเวอร์รายงาน Power BI")</span><span class="sxs-lookup"><span data-stu-id="86f7b-124">![Product key](../report-server/media/install-report-server/pbirs-product-key-dialog.png "Power BI Report Server product key")</span></span>

#### <a name="sql-server-enterprise-software-assurance-sa"></a><span data-ttu-id="86f7b-125">SQL Server Enterprise Software Assurance (SA)</span><span class="sxs-lookup"><span data-stu-id="86f7b-125">SQL Server Enterprise Software Assurance (SA)</span></span>

<span data-ttu-id="86f7b-126">ถ้าคุณมีข้อตกลง SQL Server Enterprise SA คุณสามารถรับคีย์ผลิตภัณฑ์ของคุณจาก[ศูนย์บริการการมอบสิทธิ์การใช้งาน Volume](https://www.microsoft.com/Licensing/servicecenter/)ได้</span><span class="sxs-lookup"><span data-stu-id="86f7b-126">If you have a SQL Server Enterprise SA agreement, you can get your product key from the [Volume Licensing Service Center](https://www.microsoft.com/Licensing/servicecenter/).</span></span>

## <a name="install-your-report-server"></a><span data-ttu-id="86f7b-127">ติดตั้งเซิร์ฟเวอร์รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="86f7b-127">Install your report server</span></span>

<span data-ttu-id="86f7b-128">การติดตั้งเซิร์ฟเวอร์รายงาน Power BI จะเป็นไปอย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="86f7b-128">Installing Power BI Report Server is straightforward.</span></span> <span data-ttu-id="86f7b-129">มีเพียงไม่กี่ขั้นตอนในการติดตั้งไฟล์</span><span class="sxs-lookup"><span data-stu-id="86f7b-129">There are only a few steps to install the files.</span></span>

<span data-ttu-id="86f7b-130">คุณไม่จำเป็นต้องใช้เปิดงานเซิร์ฟเวอร์กลไกจัดการฐานข้อมูล SQL Server ในขณะติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="86f7b-130">You don't need a SQL Server Database Engine server available at the time of install.</span></span> <span data-ttu-id="86f7b-131">แต่คุณจะต้องมีเพื่อกำหนดค่า “บริการการรายงาน” หลังจากติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="86f7b-131">You will need one to configure Reporting Services after install.</span></span>

1. <span data-ttu-id="86f7b-132">ค้นหาตำแหน่งที่ตั้งของ PowerBIReportServer.exe และเปิดใช้งานตัวติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="86f7b-132">Find the location of PowerBIReportServer.exe and launch the installer.</span></span>

2. <span data-ttu-id="86f7b-133">เลือก**ติดตั้งเซิร์ฟเวอร์รายงาน Power BI**</span><span class="sxs-lookup"><span data-stu-id="86f7b-133">Select **Install Power BI Report Server**.</span></span>

    ![ติดตั้ง Power BI Report Server](media/install-report-server/pbireportserver-install.png)
3. <span data-ttu-id="86f7b-135">เลือกรุ่นเพื่อติดตั้ง จากนั้นเลือก**ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="86f7b-135">Choose an edition to install and then select **Next**.</span></span>

    ![เลือกรุ่น](media/install-report-server/pbireportserver-choose-edition.png)

    <span data-ttu-id="86f7b-137">เลือก “รุ่นการประเมิน” หรือ “รุ่นนักพัฒนา”</span><span class="sxs-lookup"><span data-stu-id="86f7b-137">Choose either Evaluation or Developer edition.</span></span>

    ![รุ่น 2](media/install-report-server/pbireportserver-choose-edition2.png)

    <span data-ttu-id="86f7b-139">หรือป้อนคีย์ผลิตภัณฑ์ที่คุณได้รับมาจากบริการของ Power BI หรือศูนย์บริการ Volume License</span><span class="sxs-lookup"><span data-stu-id="86f7b-139">Otherwise, enter the product key that you got from either the Power BI service or the Volume License Service Center.</span></span> <span data-ttu-id="86f7b-140">ดูที่ส่วน[ก่อนที่คุณจะติดตั้ง](#before-you-install)ข้างต้น สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการรับคีย์ผลิตภัณฑ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="86f7b-140">For more information about how to get your product key, see the [Before you install](#before-you-install) section above.</span></span>
4. <span data-ttu-id="86f7b-141">อ่านและยอมรับเงื่อนไขและข้อกำหนดสิทธิ์การใช้งาน จากนั้นเลือก**ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="86f7b-141">Read and agree to the license terms and conditions, then select **Next**.</span></span>

    ![ข้อกำหนดสิทธิ์การใช้งาน](media/install-report-server/pbireportserver-eula.png)
5. <span data-ttu-id="86f7b-143">คุณต้องมีกลไลจัดการฐานข้อมูลที่พร้อมใช้งานเพื่อจัดเก็บฐานข้อมูลเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="86f7b-143">You need a Database Engine available to store the report server database.</span></span> <span data-ttu-id="86f7b-144">เลือก**ถัดไป**เพื่อติดตั้งเซิร์ฟเวอร์รายงานเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="86f7b-144">Select **Next** to install the report server only.</span></span>

    ![ติดตั้งไฟล์เท่านั้น](media/install-report-server/pbireportserver-install-files-only.png)
6. <span data-ttu-id="86f7b-146">ระบุตำแหน่งการติดตั้งสำหรับเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="86f7b-146">Specify the install location for the report server.</span></span> <span data-ttu-id="86f7b-147">เลือก**ติดตั้ง**เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="86f7b-147">Select **Install** to continue.</span></span>

    ![ระบุเส้นทางติดตั้ง](media/install-report-server/pbireportserver-install-file-path.png)

    <span data-ttu-id="86f7b-149">เส้นทางเริ่มต้นคือ C:\Program Files\Microsoft Power BI Report Server</span><span class="sxs-lookup"><span data-stu-id="86f7b-149">The default path is C:\Program Files\Microsoft Power BI Report Server.</span></span>

7. <span data-ttu-id="86f7b-150">หลังจากตั้งค่าสำเร็จ เลือก**กำหนดค่าเซิร์ฟเวอร์รายงาน**เพื่อเปิดใช้ตัวจัดการการกำหนดค่าบริการการรายงาน</span><span class="sxs-lookup"><span data-stu-id="86f7b-150">After a successful setup, select **Configure Report Server** to launch the Reporting Services Configuration Manager.</span></span>

    ![กำหนดค่าเซิร์ฟเวอร์รายงาน](media/install-report-server/pbireportserver-configure.png)

## <a name="configure-your-report-server"></a><span data-ttu-id="86f7b-152">กำหนดค่าเซิร์ฟเวอร์รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="86f7b-152">Configure your report server</span></span>

<span data-ttu-id="86f7b-153">หลังจากที่คุณเลือก**กำหนดค่าเซิร์ฟเวอร์รายงาน**ในการตั้งค่า คุณจะพบ Reporting Services Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="86f7b-153">After you select **Configure Report Server** in the setup, you're presented with Reporting Services Configuration Manager.</span></span> <span data-ttu-id="86f7b-154">ดูที่[ตัวจัดการการกำหนดค่าบริการการรายงาน](/sql/reporting-services/install-windows/reporting-services-configuration-manager-native-mode)สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="86f7b-154">For more information, see [Reporting Services Configuration Manager](/sql/reporting-services/install-windows/reporting-services-configuration-manager-native-mode).</span></span>

<span data-ttu-id="86f7b-155">เพื่อดำเนินการกำหนดค่าเริ่มต้นของ “บริการการรายงาน” ให้เสร็จสิ้น คุณต้อง[สร้างฐานข้อมูลเซิร์ฟเวอร์รายงาน](/sql/reporting-services/install-windows/ssrs-report-server-create-a-report-server-database)</span><span class="sxs-lookup"><span data-stu-id="86f7b-155">To complete the initial configuration of Reporting Services, you [create a report server database](/sql/reporting-services/install-windows/ssrs-report-server-create-a-report-server-database).</span></span> <span data-ttu-id="86f7b-156">เซิร์ฟเวอร์ฐานข้อมูล SQL Server จะต้องทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="86f7b-156">A SQL Server Database server is required to complete this step.</span></span>

### <a name="creating-a-database-on-a-different-server"></a><span data-ttu-id="86f7b-157">สร้างฐานข้อมูลในเซิร์ฟเวอร์อื่น</span><span class="sxs-lookup"><span data-stu-id="86f7b-157">Creating a database on a different server</span></span>

<span data-ttu-id="86f7b-158">ถ้าคุณกำลังสร้างฐานข้อมูลเซิร์ฟเวอร์รายงานในเซิร์ฟเวอร์ฐานข้อมูลบนคอมพิวเตอร์เครื่องอื่น ให้เปลี่ยนบัญชีบริการสำหรับเซิร์ฟเวอร์รายงานให้เป็นข้อมูลประจำตัวที่เซิร์ฟเวอร์ฐานข้อมูลจดจำได้</span><span class="sxs-lookup"><span data-stu-id="86f7b-158">If you're creating the report server database on a database server on a different machine, change the service account for the report server to a credential that is recognized on the database server.</span></span> 

<span data-ttu-id="86f7b-159">ตามค่าเริ่มต้น เซิร์ฟเวอร์รายงานใช้บัญชีผู้ใช้บริการเสมือน</span><span class="sxs-lookup"><span data-stu-id="86f7b-159">By default, the report server uses the virtual service account.</span></span> <span data-ttu-id="86f7b-160">ถ้าคุณพยายามที่จะสร้างฐานข้อมูลบนเซิร์ฟเวอร์อื่น คุณอาจได้รับข้อผิดพลาดต่อไปนี้ในขั้นตอนการใช้สิทธิ์การเชื่อมต่อที่นำมาปรับใช้</span><span class="sxs-lookup"><span data-stu-id="86f7b-160">If you try to create a database on a different server, you may receive the following error on the Applying connection rights step.</span></span>

`System.Data.SqlClient.SqlException (0x80131904): Windows NT user or group '(null)' not found. Check the name again.`

<span data-ttu-id="86f7b-161">คุณสามารถเปลี่ยนบัญชีบริการเป็นบริการเครือข่ายหรือบัญชีโดเมน เพื่อหลีกเลี่ยงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="86f7b-161">To work around the error, you can change the service account to either Network Service or a domain account.</span></span> <span data-ttu-id="86f7b-162">การเปลี่ยนบัญชีบริการเป็นบริการเครือข่ายจะใช้สิทธิ์ในบริบทของบัญชีเครื่องสำหรับเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="86f7b-162">Changing the service account to Network Service applies rights in the context of the machine account for the report server.</span></span>

![กำหนดค่าบัญชีผู้ใช้บริการเซิร์ฟเวอร์รายงาน](media/install-report-server/pbireportserver-configure-account.png)

<span data-ttu-id="86f7b-164">ดูที่[การกำหนดค่าบัญชีผู้ใช้บริการเซิร์ฟเวอร์รายงาน](/sql/reporting-services/install-windows/configure-the-report-server-service-account-ssrs-configuration-manager)สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="86f7b-164">For more information, see [Configure the report server service account](/sql/reporting-services/install-windows/configure-the-report-server-service-account-ssrs-configuration-manager).</span></span>

## <a name="windows-service"></a><span data-ttu-id="86f7b-165">บริการ Windows</span><span class="sxs-lookup"><span data-stu-id="86f7b-165">Windows Service</span></span>

<span data-ttu-id="86f7b-166">บริการ windows ได้รับการสร้างให้เป็นส่วนหนึ่งของการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="86f7b-166">A windows service is created as part of the installation.</span></span> <span data-ttu-id="86f7b-167">ซึ่งจะแสดงเป็น**เซิร์ฟเวอร์รายงาน Power BI**</span><span class="sxs-lookup"><span data-stu-id="86f7b-167">It is displayed as **Power BI Report Server**.</span></span> <span data-ttu-id="86f7b-168">ชื่อบริการคือ**PowerBIReportServer**</span><span class="sxs-lookup"><span data-stu-id="86f7b-168">The service name is **PowerBIReportServer**.</span></span>

![บริการ Windows เซิร์ฟเวอร์รายงาน](media/install-report-server/pbireportserver-windows-service.png)

![คุณสมบัติบริการ Windows เซิร์ฟเวอร์รายงาน](media/install-report-server/pbireportserver-windows-service2.png)

## <a name="default-url-reservations"></a><span data-ttu-id="86f7b-171">การจอง URL เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="86f7b-171">Default URL reservations</span></span>

<span data-ttu-id="86f7b-172">การจอง URL ประกอบด้วยคำนำหน้า ชื่อโฮสต์ พอร์ต และไดเรกทอรีเสมือน:</span><span class="sxs-lookup"><span data-stu-id="86f7b-172">URL reservations are composed of a prefix, host name, port, and virtual directory:</span></span>

| <span data-ttu-id="86f7b-173">ส่วน</span><span class="sxs-lookup"><span data-stu-id="86f7b-173">Part</span></span> | <span data-ttu-id="86f7b-174">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="86f7b-174">Description</span></span> |
| --- | --- |
| <span data-ttu-id="86f7b-175">คำนำหน้า</span><span class="sxs-lookup"><span data-stu-id="86f7b-175">Prefix</span></span> |<span data-ttu-id="86f7b-176">คำนำหน้าเริ่มต้นคือ HTTP</span><span class="sxs-lookup"><span data-stu-id="86f7b-176">The default prefix is HTTP.</span></span> <span data-ttu-id="86f7b-177">ถ้าคุณติดตั้งใบรับรอง Secure Sockets Layer (SSL) ไว้แล้วก่อนหน้านี้ “การตั้งค่า” จะพยายามสร้างการจอง URL ที่ใช้คำนำหน้าเป็น HTTPS</span><span class="sxs-lookup"><span data-stu-id="86f7b-177">If you previously installed a Secure Sockets Layer (SSL) certificate, Setup tries to create URL reservations that use the HTTPS prefix.</span></span> |
| <span data-ttu-id="86f7b-178">ชื่อโฮสต์</span><span class="sxs-lookup"><span data-stu-id="86f7b-178">Host name</span></span> |<span data-ttu-id="86f7b-179">ชื่อโฮสต์เริ่มต้นคือ สัญลักษณ์ที่คาดเดายาก (+)</span><span class="sxs-lookup"><span data-stu-id="86f7b-179">The default host name is a strong wildcard (+).</span></span> <span data-ttu-id="86f7b-180">ซึ่งระบุว่าเซิร์ฟเวอร์รายงานยอมรับคำขอ HTTP ใด ๆ บนพอร์ตที่กำหนดไว้สำหรับชื่อโฮสต์ที่แก้ไขไปยังคอมพิวเตอร์ รวมถึง`https://<computername>/reportserver`,`https://localhost/reportserver`หรือ `https://<IPAddress>/reportserver.`</span><span class="sxs-lookup"><span data-stu-id="86f7b-180">It specifies that the report server accepts any HTTP request on the designated port for any host name that resolves to the computer, including `https://<computername>/reportserver`, `https://localhost/reportserver`, or `https://<IPAddress>/reportserver.`</span></span> |
| <span data-ttu-id="86f7b-181">พอร์ต</span><span class="sxs-lookup"><span data-stu-id="86f7b-181">Port</span></span> |<span data-ttu-id="86f7b-182">พอร์ตเริ่มต้นคือ 80</span><span class="sxs-lookup"><span data-stu-id="86f7b-182">The default port is 80.</span></span> <span data-ttu-id="86f7b-183">ถ้าคุณใช้พอร์ตใด ๆ นอกเหนือจากพอร์ต 80 คุณต้องเพิ่มพอร์ตนั้นลงใน URL อย่างชัดเจนเมื่อคุณเปิดเว็บพอร์ทัลในหน้าต่างเบราเซอร์</span><span class="sxs-lookup"><span data-stu-id="86f7b-183">If you use any port other than port 80, you have to explicitly add it to the URL when you open web portal in a browser window.</span></span> |
| <span data-ttu-id="86f7b-184">ไดเรกทอรีเสมือน</span><span class="sxs-lookup"><span data-stu-id="86f7b-184">Virtual directory</span></span> |<span data-ttu-id="86f7b-185">ตามค่าเริ่มต้น ไดเรกทอรีเสมือนได้รับการสร้างขึ้นในรูปแบบของ ReportServer สำหรับ Web Service เซิร์ฟเวอร์รายงาน และรายงานสำหรับพอร์ทัลเว็บ</span><span class="sxs-lookup"><span data-stu-id="86f7b-185">By default, virtual directories are created in the format of ReportServer for the Report Server Web service and Reports for the web portal.</span></span> <span data-ttu-id="86f7b-186">ไดเรกทอรีเสมือนเริ่มต้นคือ**reportserver**สำหรับ Web Service เซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="86f7b-186">For the Report Server Web service, the default virtual directory is **reportserver**.</span></span> <span data-ttu-id="86f7b-187">ไดเรกทอรีเสมือนเริ่มต้นคือ**รายงาน**สำหรับพอร์ทัลเว็บ</span><span class="sxs-lookup"><span data-stu-id="86f7b-187">For the web portal, the default virtual directory is **reports**.</span></span> |

<span data-ttu-id="86f7b-188">ตัวอย่างของสตริงที่ URL สมบูรณ์อาจเป็นดังนี้:</span><span class="sxs-lookup"><span data-stu-id="86f7b-188">An example of the complete URL string might be as follows:</span></span>

* <span data-ttu-id="86f7b-189">`https://+:80/reportserver`มอบการเข้าถึงไปยังเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="86f7b-189">`https://+:80/reportserver`, provides access to the report server.</span></span>
* <span data-ttu-id="86f7b-190">`https://+:80/reports`มอบการเข้าถึงพอร์ทัลเว็บ</span><span class="sxs-lookup"><span data-stu-id="86f7b-190">`https://+:80/reports`, provides access to the web portal.</span></span>

## <a name="firewall"></a><span data-ttu-id="86f7b-191">ไฟร์วอลล์</span><span class="sxs-lookup"><span data-stu-id="86f7b-191">Firewall</span></span>

<span data-ttu-id="86f7b-192">ถ้าคุณกำลังเข้าถึงเซิร์ฟเวอร์รายงานจากเครื่องระยะไกล กรุณาตรวจสอบให้แน่ใจว่าคุณได้กำหนดกฎไฟร์วอลล์แล้วใช่หรือไม่ หากมีไฟร์วอลล์อยู่</span><span class="sxs-lookup"><span data-stu-id="86f7b-192">If you're accessing the report server from a remote machine, make sure you've configured any firewall rules if there is a firewall present.</span></span>

<span data-ttu-id="86f7b-193">เปิดพอร์ต TCP ที่คุณกำหนดค่าสำหรับ Web Service URL และ Web Portal URL ของคุณ</span><span class="sxs-lookup"><span data-stu-id="86f7b-193">Open up the TCP port that you've configured for your Web Service URL and Web Portal URL.</span></span> <span data-ttu-id="86f7b-194">ซึ่งจะกำหนดค่าบนพอร์ต TCP 80 ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="86f7b-194">By default, they're configured on TCP port 80.</span></span>

## <a name="additional-configuration"></a><span data-ttu-id="86f7b-195">การกำหนดค่าเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="86f7b-195">Additional configuration</span></span>

* <span data-ttu-id="86f7b-196">ดูที่[รวมกับบริการ Power BI](/sql/reporting-services/install-windows/power-bi-report-server-integration-configuration-manager)เพื่อกำหนดค่าการรวมกับบริการ Power BI เมื่อต้องการให้คุณสามารถปักหมุดรายการรายงานไปยังแดชบอร์ด Power BI</span><span class="sxs-lookup"><span data-stu-id="86f7b-196">To configure integration with the Power BI service so you can pin report items to a Power BI dashboard, see [Integrate with the Power BI service](/sql/reporting-services/install-windows/power-bi-report-server-integration-configuration-manager).</span></span>
* <span data-ttu-id="86f7b-197">ดูที่[ตั้งค่าอีเมล์](/sql/reporting-services/install-windows/e-mail-settings-reporting-services-native-mode-configuration-manager)และ[อีเมลที่ส่งในเซิร์ฟเวอร์รายงาน](/sql/reporting-services/subscriptions/e-mail-delivery-in-reporting-services)เมื่อต้องการกำหนดค่าอีเมลสำหรับการประมวลผลการสมัครใช้งาน</span><span class="sxs-lookup"><span data-stu-id="86f7b-197">To configure email for subscriptions processing, see [E-Mail settings](/sql/reporting-services/install-windows/e-mail-settings-reporting-services-native-mode-configuration-manager) and [E-Mail delivery in a report server](/sql/reporting-services/subscriptions/e-mail-delivery-in-reporting-services).</span></span>
* <span data-ttu-id="86f7b-198">ดูที่[กำหนดค่าไฟร์วอลล์สำหรับการเข้าถึงเซิร์ฟเวอร์รายงาน](/sql/reporting-services/report-server/configure-a-firewall-for-report-server-access)และ[การกำหนดค่าเซิร์ฟเวอร์รายงานสำหรับการดูแลระบบระยะไกล](/sql/reporting-services/report-server/configure-a-report-server-for-remote-administration) เมื่อต้องการกำหนดค่าพอร์ทัลเว็บเพื่อให้คุณสามารถเข้าถึงได้ผ่านคอมพิวเตอร์รายงานเพื่อดูและจัดการรายงาน</span><span class="sxs-lookup"><span data-stu-id="86f7b-198">To configure the web portal so you can access it on a report computer to view and manage reports, see [Configure a firewall for report server access](/sql/reporting-services/report-server/configure-a-firewall-for-report-server-access) and [Configure a report server for remote administration](/sql/reporting-services/report-server/configure-a-report-server-for-remote-administration).</span></span>
* <span data-ttu-id="86f7b-199">สำหรับรายละเอียดเกี่ยวกับการตั้งค่าคุณสมบัติระบบของเซิร์ฟเวอร์รายงานใน SQL Server Management Studio ดู [หน้าคุณสมบัติของเซิร์ฟเวอร์ขั้นสูง](/sql/reporting-services/tools/server-properties-advanced-page-reporting-services)</span><span class="sxs-lookup"><span data-stu-id="86f7b-199">For details on setting report server system properties in SQL Server Management Studio, see [Server Properties Advanced Page](/sql/reporting-services/tools/server-properties-advanced-page-reporting-services).</span></span> <span data-ttu-id="86f7b-200">ถ้าไม่กำหนด ตัวเลือกจะใช้กับเซิร์ฟเวอร์รายงาน Power BI และ SQL Server Reporting Services ทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="86f7b-200">Unless it specifies otherwise, the options apply to both Power BI Report Server and SQL Server Reporting Services.</span></span>

## <a name="next-steps"></a><span data-ttu-id="86f7b-201">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="86f7b-201">Next steps</span></span>

[<span data-ttu-id="86f7b-202">ภาพรวมของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="86f7b-202">Administrator overview</span></span>](admin-handbook-overview.md)  
[<span data-ttu-id="86f7b-203">วิธีการค้นหาคีย์ผลิตภัณฑ์เซิร์ฟเวอร์รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="86f7b-203">How to find your report server product key</span></span>](find-product-key.md)  
[<span data-ttu-id="86f7b-204">ติดตั้ง Power BI Desktop ที่ปรับให้เหมาะสำหรับ Power BI Report Server</span><span class="sxs-lookup"><span data-stu-id="86f7b-204">Install Power BI Desktop optimized for Power BI Report Server</span></span>](install-powerbi-desktop.md)  
[<span data-ttu-id="86f7b-205">ตรวจสอบการติดตั้งบริการการรายงาน</span><span class="sxs-lookup"><span data-stu-id="86f7b-205">Verify a Reporting Services installation</span></span>](/sql/reporting-services/install-windows/verify-a-reporting-services-installation)  
[<span data-ttu-id="86f7b-206">กำหนดค่าบัญชีผู้ใช้บริการเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="86f7b-206">Configure the report server service account</span></span>](/sql/reporting-services/install-windows/configure-the-report-server-service-account-ssrs-configuration-manager)  
[<span data-ttu-id="86f7b-207">กำหนดค่า URL ของเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="86f7b-207">Configure report server URLs</span></span>](/sql/reporting-services/install-windows/configure-report-server-urls-ssrs-configuration-manager)  
[<span data-ttu-id="86f7b-208">กำหนดค่าการเชื่อมต่อฐานข้อมูลเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="86f7b-208">Configure a report server database connection</span></span>](/sql/reporting-services/install-windows/configure-a-report-server-database-connection-ssrs-configuration-manager)  
[<span data-ttu-id="86f7b-209">เตรียมใช้งานเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="86f7b-209">Initialize a report server</span></span>](/sql/reporting-services/install-windows/ssrs-encryption-keys-initialize-a-report-server)  
[<span data-ttu-id="86f7b-210">กำหนดค่าการเชื่อมต่อ SSL ในเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="86f7b-210">Configure SSL connections on a report server</span></span>](/sql/reporting-services/security/configure-ssl-connections-on-a-native-mode-report-server)  
[<span data-ttu-id="86f7b-211">กำหนดค่าบัญชีบริการ windows และสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="86f7b-211">Configure windows service accounts and permissions</span></span>](/sql/database-engine/configure-windows/configure-windows-service-accounts-and-permissions)  
[<span data-ttu-id="86f7b-212">การสนับสนุนเบราว์เซอร์สำหรับ Power BI Report Server</span><span class="sxs-lookup"><span data-stu-id="86f7b-212">Browser support for Power BI Report Server</span></span>](browser-support.md)

<span data-ttu-id="86f7b-213">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="86f7b-213">More questions?</span></span> [<span data-ttu-id="86f7b-214">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="86f7b-214">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)