---
title: ใช้ Web Application Proxy และ Active Directory Federated Services - เซิร์ฟเวอร์รายงาน Power BI
description: เรียนรู้วิธีการใช้ Web Application Proxy (WAP) และ  Active Directory Federated Services (AD FS) เพื่อเชื่อมต่อกับเซิร์ฟเวอร์รายงาน Power BI และ SQL Server Reporting Services (SSRS) 2016 และใหม่กว่า
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.date: 10/12/2020
ms.openlocfilehash: 17e153528e45a52de7addf3563c58c2586600660
ms.sourcegitcommit: 383d87841d2509131fac7cc02c5c37c6a868144f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/14/2020
ms.locfileid: "92026034"
---
# <a name="use-web-application-proxy-and-active-directory-federated-services---power-bi-report-server"></a><span data-ttu-id="956ca-103">ใช้ Web Application Proxy และ Active Directory Federated Services - เซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="956ca-103">Use Web Application Proxy and Active Directory Federated Services - Power BI Report Server</span></span>

<span data-ttu-id="956ca-104">บทความนี้อธิบายวิธีการใช้ Web Application Proxy (WAP) และ  Active Directory Federated Services (AD FS) เพื่อเชื่อมต่อกับเซิร์ฟเวอร์รายงาน Power BI และ SQL Server Reporting Services (SSRS) 2016 และใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="956ca-104">This article discusses how to use Web Application Proxy (WAP) and Active Directory Federated Services (AD FS) to connect to Power BI Report Server, and SQL Server Reporting Services (SSRS) 2016 and later.</span></span> <span data-ttu-id="956ca-105">ด้วยการรวมนี้ ผู้ใช้ที่อยู่ห่างจากเครือข่ายขององค์กรสามารถเข้าถึงเซิร์ฟเวอร์รายงาน Power BI และรายงาน Reporting Services จากเบราว์เซอร์ลูกค้าของพวกเขา และได้รับการป้องกันโดยการรับรองความถูกต้องล่วงหน้าของ  AD FS</span><span class="sxs-lookup"><span data-stu-id="956ca-105">Through this integration, users who are away from the corporate network can access their Power BI Report Server and Reporting Services reports from their client browsers and be protected by AD FS preauthentication.</span></span> <span data-ttu-id="956ca-106">สำหรับแอปสำหรับอุปกรณ์เคลื่อนที่ Power BI คุณยังจำเป็นต้อง [กำหนดค่า OAuth เพื่อเชื่อมต่อกับเซิร์ฟเวอร์รายงาน Power BI และ SSRS](../consumer/mobile/mobile-oauth-ssrs.md)</span><span class="sxs-lookup"><span data-stu-id="956ca-106">For the Power BI mobile apps, you also need to [configure OAuth to connect to Power BI Report Server and SSRS](../consumer/mobile/mobile-oauth-ssrs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="956ca-107">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="956ca-107">Prerequisites</span></span>

### <a name="domain-name-services-dns-configuration"></a><span data-ttu-id="956ca-108">การกำหนดค่าบริการชื่อโดเมน (DNS)</span><span class="sxs-lookup"><span data-stu-id="956ca-108">Domain Name Services (DNS) configuration</span></span>

- <span data-ttu-id="956ca-109">กำหนด URL สาธารณะที่ผู้ใช้จะเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="956ca-109">Determine the public URL that the user will connect to.</span></span> <span data-ttu-id="956ca-110">ควรมีลักษณะคล้ายกับตัวอย่างนี้: `https://reports.contosolab.com`</span><span class="sxs-lookup"><span data-stu-id="956ca-110">It may look similar to this example: `https://reports.contosolab.com`.</span></span>
- <span data-ttu-id="956ca-111">กำหนดค่าระเบียน DNS สำหรับชื่อโฮสต์ของคุณ `reports.contosolab.com` ตัวอย่างเช่น เพื่อชี้ไปยังที่อยู่ IP สาธารณะของเซิร์ฟเวอร์ Web Application Proxy (WAP) </span><span class="sxs-lookup"><span data-stu-id="956ca-111">Configure your DNS record for the host name, `reports.contosolab.com`, for example, to point to the public IP address of the Web Application Proxy (WAP) server.</span></span>
- <span data-ttu-id="956ca-112">กำหนดค่า DNS สาธารณะสำหรับเซิร์ฟเวอร์ AD FS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="956ca-112">Configure a public DNS record for your AD FS server.</span></span> <span data-ttu-id="956ca-113">ตัวอย่างเช่น คุณอาจกำหนดค่าเซิร์ฟเวอร์ AD FS ด้วย URL ต่อไปนี้: `https://adfs.contosolab.com`</span><span class="sxs-lookup"><span data-stu-id="956ca-113">For example, you may have configured the AD FS server with the following URL: `https://adfs.contosolab.com`.</span></span>
- <span data-ttu-id="956ca-114">กำหนดค่าระเบียน DNS ของคุณเพื่อชี้ไปยังที่อยู่ IP สาธารณะของเซิร์ฟเวอร์ Web Application Proxy (WAP) ตัวอย่างเช่น `adfs.contosolab.com`</span><span class="sxs-lookup"><span data-stu-id="956ca-114">Configure your DNS record to point to the public IP address of the Web Application Proxy (WAP) server, for example `adfs.contosolab.com`.</span></span> <span data-ttu-id="956ca-115">ซึ่งมีการเผยแพร่เป็นส่วนหนึ่งของแอปพลิเคชัน WAP</span><span class="sxs-lookup"><span data-stu-id="956ca-115">It's published as part of the WAP application.</span></span>

### <a name="certificates"></a><span data-ttu-id="956ca-116">ใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="956ca-116">Certificates</span></span>

<span data-ttu-id="956ca-117">คุณต้องกำหนดค่าใบรับรองสำหรับทั้งแอปพลิเคชัน WAP และเซิร์ฟเวอร์ AD FS</span><span class="sxs-lookup"><span data-stu-id="956ca-117">You need to configure certificates for both the WAP application and the AD FS server.</span></span> <span data-ttu-id="956ca-118">ใบรับรองทั้งสองต้องเป็นส่วนหนึ่งของผู้มีสิทธิ์ออกใบรับรองที่ถูกต้องที่เครื่องของคุณรู้จัก</span><span class="sxs-lookup"><span data-stu-id="956ca-118">Both of these certificates must be part of a valid certificate authority that your machines recognize.</span></span>

## <a name="1-configure-the-report-server"></a><span data-ttu-id="956ca-119">1. กำหนดค่าเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="956ca-119">1. Configure the report server</span></span>

<span data-ttu-id="956ca-120">เราจำเป็นต้องตรวจสอบให้แน่ใจว่าเรามีชื่อบริการหลัก (SPN) ที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="956ca-120">We need to make sure that we have a valid Service Principal Name (SPN).</span></span> <span data-ttu-id="956ca-121">SPN ที่ถูกต้องจะเปิดใช้งานการรับรองความถูกต้อง Kerberos ที่เหมาะสมและเปิดใช้งานเซิร์ฟเวอร์รายงานสำหรับการรับรองความถูกต้องในการเจรจา</span><span class="sxs-lookup"><span data-stu-id="956ca-121">The valid SPN enables the proper Kerberos authentication to occur and enables the report server for negotiate authentication.</span></span>

### <a name="service-principal-name-spn"></a><span data-ttu-id="956ca-122">ชื่อบริการหลัก (SPN)</span><span class="sxs-lookup"><span data-stu-id="956ca-122">Service Principal Name (SPN)</span></span>

<span data-ttu-id="956ca-123">SPN เป็นตัวระบุเฉพาะสำหรับบริการที่ใช้การรับรองความถูกต้อง Kerberos</span><span class="sxs-lookup"><span data-stu-id="956ca-123">The SPN is a unique identifier for a service that uses Kerberos authentication.</span></span> <span data-ttu-id="956ca-124">ตรวจสอบให้แน่ใจว่า คุณมี SPN HTTP ที่เหมาะสมสำหรับเซิร์ฟเวอร์รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="956ca-124">Make sure you have a proper HTTP SPN present for your report server.</span></span>

<span data-ttu-id="956ca-125">สำหรับข้อมูลเกี่ยวกับวิธีการกำหนดค่าชื่อบริการหลัก (SPN) ที่เหมาะสมสำหรับเซิร์ฟเวอร์รายงานของคุณ ดู[ลงทะเบียน ชื่อบริการหลัก (SPN) สำหรับเซิร์ฟเวอร์รายงาน](/sql/reporting-services/report-server/register-a-service-principal-name-spn-for-a-report-server)</span><span class="sxs-lookup"><span data-stu-id="956ca-125">For information on how to configure the proper Service Principal Name (SPN) for your report server, see [Register a Service Principal Name (SPN) for a Report Server](/sql/reporting-services/report-server/register-a-service-principal-name-spn-for-a-report-server).</span></span>

### <a name="enabling-negotiate-authentication"></a><span data-ttu-id="956ca-126">การเปิดใช้งานการรับรองความถูกต้องในการเจรจา</span><span class="sxs-lookup"><span data-stu-id="956ca-126">Enabling negotiate authentication</span></span>

<span data-ttu-id="956ca-127">ในการเปิดใช้งานเซิร์ฟเวอร์รายงานเพื่อใช้การรับรองความถูกต้อง Kerberos คุณต้องกำหนดค่าชนิดของการรับรองความถูกต้องของเซิร์ฟเวอร์รายงานให้เป็น RSWindowsNegotiate</span><span class="sxs-lookup"><span data-stu-id="956ca-127">To enable a report server to use Kerberos authentication, you need to configure the Authentication Type of the report server to be RSWindowsNegotiate.</span></span> <span data-ttu-id="956ca-128">คุณสามารถกำหนดค่าได้ภายในไฟล์ rsreportserver.config</span><span class="sxs-lookup"><span data-stu-id="956ca-128">You configure it in the rsreportserver.config file.</span></span>

```
<AuthenticationTypes>

    <RSWindowsNegotiate />

    <RSWindowsNTLM />

</AuthenticationTypes>
```

<span data-ttu-id="956ca-129">สำหรับข้อมูลเพิ่มเติม ดู[ปรับเปลี่ยนแฟ้มการกำหนดค่า Reporting Services](/sql/reporting-services/report-server/modify-a-reporting-services-configuration-file-rsreportserver-config) และ[กำหนดค่าการรับรองความถูกต้องของ Windows บนเซิร์ฟเวอร์รายงาน](/sql/reporting-services/security/configure-windows-authentication-on-the-report-server)</span><span class="sxs-lookup"><span data-stu-id="956ca-129">For more information, see [Modify a Reporting Services Configuration File](/sql/reporting-services/report-server/modify-a-reporting-services-configuration-file-rsreportserver-config) and [Configure Windows Authentication on a Report Server](/sql/reporting-services/security/configure-windows-authentication-on-the-report-server).</span></span>

## <a name="2-configure-active-directory-federation-services-ad-fs"></a><span data-ttu-id="956ca-130">2. กำหนดค่า Active Directory Federation Services (AD FS) </span><span class="sxs-lookup"><span data-stu-id="956ca-130">2. Configure Active Directory Federation Services (AD FS)</span></span>

<span data-ttu-id="956ca-131">คุณต้องกำหนดค่า AD FS บนเซิร์ฟเวอร์ Windows 2016 ภายในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="956ca-131">You need to configure AD FS on a Windows 2016 server within your environment.</span></span> <span data-ttu-id="956ca-132">การกำหนดค่าสามารถทำได้ผ่านตัวจัดการเซิร์ฟเวอร์ และการเลือกเพิ่มบทบาทและคุณลักษณะซึ่งอยู่ด้านล่างจัดการ</span><span class="sxs-lookup"><span data-stu-id="956ca-132">The configuration can be done through the Server Manager and selecting Add Roles and Features under Manage.</span></span> <span data-ttu-id="956ca-133">สำหรับข้อมูลเพิ่มเติม ดู[Active Directory Federation Services](/windows-server/identity/active-directory-federation-services)</span><span class="sxs-lookup"><span data-stu-id="956ca-133">For more information, see [Active Directory Federation Services](/windows-server/identity/active-directory-federation-services).</span></span>

<span data-ttu-id="956ca-134">บนเซิร์ฟเวอร์ AD FS ให้ใช้แอปการจัดการ AD FS ในการทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="956ca-134">On the AD FS server, using AD FS Management App, complete these steps.</span></span>

1. <span data-ttu-id="956ca-135">คลิกขวา **ความน่าเชื่อถือของฝ่ายที่เกี่ยวช้อง** > **เพิ่มความน่าเชื่อถือของฝ่ายที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="956ca-135">Right-click **Relying Party Trusts** > **Add Relying Party Trust**.</span></span>

    ![ความน่าเชื่อถือของฝ่ายที่เกี่ยวข้อง](media/connect-adfs-wap-report-server/report-server-adfs-add-relying-party-trust.png)

2. <span data-ttu-id="956ca-137">ทำตามขั้นตอนในตัวช่วยสร้าง **เพิ่มความน่าเชื่อถือของฝ่ายที่เกี่ยวข้อง** </span><span class="sxs-lookup"><span data-stu-id="956ca-137">Follow the steps in **Add Relying Party Trust** wizard.</span></span>

    <span data-ttu-id="956ca-138">เลือกตัวเลือก **ที่ไม่ได้รับการอ้างสิทธิ์** เพื่อใช้การรักษาความปลอดภัยรวมของ Windows ในฐานะกลไกการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="956ca-138">Choose the **Non claims aware** option to use Windows Integrated security as the authentication mechanism.</span></span>

    ![ยินดีต้อนรับตัวช่วยสร้างการเพิ่มความน่าเชื่อถือของฝ่ายที่เกี่ยวข้อง](media/connect-adfs-wap-report-server/report-server-adfs-add-relying-party-trust-welcome.png)

    <span data-ttu-id="956ca-140">กรอกชื่อที่คุณต้องการใน **ระบุชื่อที่แสดง** และเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="956ca-140">Enter a name you prefer in the **Specify Display Name** and select **Next**.</span></span>
    <span data-ttu-id="956ca-141">เพิ่มตัวระบุความน่าเชื่อถือของฝ่ายที่เกี่ยวข้อง: `<ADFS\_URL>/adfs/services/trust`</span><span class="sxs-lookup"><span data-stu-id="956ca-141">Add the Relying party trust identifier: `<ADFS\_URL>/adfs/services/trust`</span></span>

    <span data-ttu-id="956ca-142">ตัวอย่างเช่น: `https://adfs.contosolab.com/adfs/services/trust`</span><span class="sxs-lookup"><span data-stu-id="956ca-142">For example: `https://adfs.contosolab.com/adfs/services/trust`</span></span>

    ![เซิร์ฟเวอร์รายงาน Power BI](media/connect-adfs-wap-report-server/report-server-adfs-configure-identifiers.png)

    <span data-ttu-id="956ca-144">เลือก **นโยบายการควบคุมการเข้าถึง** ที่เหมาะกับความต้องการขององค์กรของคุณ แล้วเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="956ca-144">Choose the **Access Control Policy** that fits your organization's needs, and select **Next**.</span></span>

    ![เลือกการควบคุมการเข้าถึง](media/connect-adfs-wap-report-server/report-server-adfs-choose-access-control.png)
    
    <span data-ttu-id="956ca-146">เลือก **ถัดไป**จากนั้นเลือก **เสร็จสิ้น** เพื่อดำเนินการตัวช่วยสร้าง **เพิ่มความน่าเชื่อถือของฝ่ายที่เกี่ยวข้อง** ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="956ca-146">Select **Next**, then select **Finish** to complete the **Add Relying Party Trust** wizard.</span></span>

    <span data-ttu-id="956ca-147">เมื่อเสร็จสมบูรณ์แล้ว คุณสมบัติของความเชื่อถือของฝ่ายที่เกี่ยวข้อง ควรมีลักษณะดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="956ca-147">When completed, the properties of the Relying Party Trusts should look like the following.</span></span>

    ![ความน่าเชื่อถือของฝ่ายที่เกี่ยวข้อง](media/connect-adfs-wap-report-server/report-server-adfs-relying-party-trusts.png)

## <a name="3-configure-web-application-proxy-wap"></a><span data-ttu-id="956ca-149">3. กำหนดค่า Web  Application Proxy (WAP)</span><span class="sxs-lookup"><span data-stu-id="956ca-149">3. Configure Web Application Proxy (WAP)</span></span>

<span data-ttu-id="956ca-150">คุณต้องเปิดใช้งานบทบาท Windows ของ Web Application Proxy (ROLE) บนเซิร์ฟเวอร์ในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="956ca-150">You want to enable the Web Application Proxy (Role) Windows role on a server in your environment.</span></span> <span data-ttu-id="956ca-151">ซึ่งต้องอยู่บนเซิร์ฟเวอร์ Windows 2016</span><span class="sxs-lookup"><span data-stu-id="956ca-151">It must be on a Windows 2016 server.</span></span> <span data-ttu-id="956ca-152">สำหรับข้อมูลเพิ่มเติม ดู [Web Application Proxy ใน Windows Server 2016 ](/windows-server/remote/remote-access/web-application-proxy/web-application-proxy-windows-server)และ[เผยแพร่แอปพลิเคชันโดยใช้การรับรองความถูกต้องล่วงหน้า AD FS](/windows-server/remote/remote-access/web-application-proxy/Publishing-Applications-using-AD-FS-Preauthentication)</span><span class="sxs-lookup"><span data-stu-id="956ca-152">For more information, see [Web Application Proxy in Windows Server 2016](/windows-server/remote/remote-access/web-application-proxy/web-application-proxy-windows-server) and [Publishing Applications using AD FS Preauthentication](/windows-server/remote/remote-access/web-application-proxy/Publishing-Applications-using-AD-FS-Preauthentication).</span></span>

### <a name="configure-constrained-delegation"></a><span data-ttu-id="956ca-153">กำหนดค่าการมอบหมายที่มีข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="956ca-153">Configure constrained delegation</span></span>

<span data-ttu-id="956ca-154">เพื่อการเปลี่ยนจากการรับรองความถูกต้องของ Forms เป็นการรับรองความถูกต้องของ Windows เราจำเป็นต้องใช้การมอบหมายที่มีข้อจำกัดด้วยการเปลี่ยนโพรโทคอล</span><span class="sxs-lookup"><span data-stu-id="956ca-154">To transition from Forms authentication to Windows authentication, we need to use constrained delegation with protocol transitioning.</span></span> <span data-ttu-id="956ca-155">ขั้นตอนนี้คือส่วนหนึ่งของการกำหนดค่า Kerberos</span><span class="sxs-lookup"><span data-stu-id="956ca-155">This step is part of the Kerberos configuration.</span></span> <span data-ttu-id="956ca-156">เราได้กำหนดเซิร์ฟเวอร์รายงาน SPN ไว้ภายในการกำหนดค่าเซิร์ฟเวอร์รายงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="956ca-156">We already defined the report server SPN within the report server configuration.</span></span>

<span data-ttu-id="956ca-157">เราต้องกำหนดค่าการมอบหมายที่มีข้อจำกัดบนบัญชีผู้ใช้ภายในเครื่องของเซิร์ฟเวอร์ WAP ภายใน Active Directory</span><span class="sxs-lookup"><span data-stu-id="956ca-157">We need to configure constrained delegation on the WAP Server machine account within Active Directory.</span></span> <span data-ttu-id="956ca-158">คุณอาจจำเป็นต้องทำงานกับผู้ดูแลโดเมนถ้าคุณไม่มีสิทธิ์ใน Active Directory</span><span class="sxs-lookup"><span data-stu-id="956ca-158">You may need to work with a domain administrator if you don't have rights to Active Directory.</span></span>

<span data-ttu-id="956ca-159">ในการกำหนดค่าการมอบหมายที่มีการจำกัด ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="956ca-159">To configure constrained delegation, follow these steps.</span></span>

1. <span data-ttu-id="956ca-160">บนเครื่องที่มีเครื่องมือ Active Directory ติดตั้งไว้แล้ว ให้เปิดใช้**ผู้ใช้และคอมพิวเตอร์ Active Directory**</span><span class="sxs-lookup"><span data-stu-id="956ca-160">On a machine that has the Active Directory tools installed, launch **Active Directory Users and Computers**.</span></span>
2. <span data-ttu-id="956ca-161">ค้นหาบัญชีผู้ใช้ภายในเครื่องสำหรับเซิร์ฟเวอร์ WAP ของคุณ</span><span class="sxs-lookup"><span data-stu-id="956ca-161">Find the machine account for your WAP server.</span></span> <span data-ttu-id="956ca-162">ตามค่าเริ่มต้น บัญชีผู้ใช้ดังกล่าวจะอยู่ในคอนเทนเนอร์ของ **คอมพิวเตอร์**</span><span class="sxs-lookup"><span data-stu-id="956ca-162">By default, it will be in the **Computers** container.</span></span>
3. <span data-ttu-id="956ca-163">คลิกขวาที่เซิร์ฟเวอร์ WAP และไปที่ **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="956ca-163">Right-click the WAP server and go to **Properties**.</span></span>
4. <span data-ttu-id="956ca-164">บนแท็บ **การมอบหมาย** เลือก **เชื่อถือคอมพิวเตอร์เครื่องนี้สำหรับการมอบหมายบริการที่ระบุไว้เท่านั้น** แล้วเลือกใช้ **โพรโทคอลการรับรองความถูกต้องใดก็ตาม**</span><span class="sxs-lookup"><span data-stu-id="956ca-164">On the **Delegation** tab, select **Trust this computer for delegation to specified services only** and then **Use any authentication protocol**.</span></span>

    ![เชื่อถือคอมพิวเตอร์เครื่องนี้](media/connect-adfs-wap-report-server/report-server-adfs-delegation-use-any.png)

1. <span data-ttu-id="956ca-166">ตัวเลือกนี้ตั้งค่าการมอบหมายที่มีข้อจำกัดสำหรับบัญชีผู้ใช้ภายในเครื่องของเซิร์ฟเวอร์ WAP</span><span class="sxs-lookup"><span data-stu-id="956ca-166">This option sets up constrained delegation for this WAP Server machine account.</span></span> <span data-ttu-id="956ca-167">เราจึงต้องระบุบริการที่เครื่องนี้ได้รับอนุญาตให้ผู้รับมอบสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="956ca-167">We then need to specify the services that this machine is allowed to delegate to.</span></span>
2. <span data-ttu-id="956ca-168">เลือก **เพิ่ม** ใต้กล่องบริการ</span><span class="sxs-lookup"><span data-stu-id="956ca-168">Select **Add** under the services box.</span></span>

    ![AD FS เพิ่มความน่าเชื่อถือ](media/connect-adfs-wap-report-server/report-server-adfs-trust-add.png)

1. <span data-ttu-id="956ca-170">เลือก **ผู้ใช้หรือคอมพิวเตอร์**</span><span class="sxs-lookup"><span data-stu-id="956ca-170">Select **Users or Computers**.</span></span>
2. <span data-ttu-id="956ca-171">กรอกบัญชีบริการที่คุณกำลังใช้สำหรับเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="956ca-171">Enter the service account that you are using for the report server.</span></span> <span data-ttu-id="956ca-172">บัญชีนี้เป็นบัญชีเดียวกันกับที่คุณใช้ในการเพิ่ม HTTP SPN ในส่วน  [การกำหนดค่าเซิร์ฟเวอร์รายงาน](#1-configure-the-report-server) ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="956ca-172">This account is the same one you used to add the HTTP SPN in the earlier [report server configuration](#1-configure-the-report-server) section.</span></span> 

3. <span data-ttu-id="956ca-173">เลือก HTTP SPN สำหรับเซิร์ฟเวอร์รายงานจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="956ca-173">Select the HTTP SPN for the report server, then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="956ca-174">คุณอาจเห็นเพียง NetBIOS SPN</span><span class="sxs-lookup"><span data-stu-id="956ca-174">You may only see the NetBIOS SPN.</span></span> <span data-ttu-id="956ca-175">ซึ่งแท้จริงแล้วจะเลือกทั้ง NetBIOS และ FQDN SPNs ถ้ามีทั้งสองรายการอยู่</span><span class="sxs-lookup"><span data-stu-id="956ca-175">It will actually select both the NetBIOS and FQDN SPNs, if they both exist.</span></span>

1. <span data-ttu-id="956ca-176">เมื่อคุณเลือกกล่องกาเครื่องหมาย **ขยาย** ผลลัพธ์ที่ออกมาควรคล้ายคลึงกับตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="956ca-176">When you select the **Expanded** check box, the result should look similar to the following example.</span></span>

    ![คุณสมบัติ WAP](media/connect-adfs-wap-report-server/report-server-wap-properties.png)

### <a name="add-wap-application"></a><span data-ttu-id="956ca-178">เพิ่มแอปพลิเคชัน WAP</span><span class="sxs-lookup"><span data-stu-id="956ca-178">Add WAP Application</span></span>

1. <span data-ttu-id="956ca-179">บนเซิร์ฟเวอร์ Web Application Proxy เปิดคอนโซล **การจัดการการเข้าถึงระยะไกล** และเลือก **Web Application Proxy** ในบานหน้าต่างการนำทาง</span><span class="sxs-lookup"><span data-stu-id="956ca-179">On the Web Application Proxy server, open the **Remote Access Management** console and select **Web Application Proxy** in the Navigation pane.</span></span> 

2. <span data-ttu-id="956ca-180">ในบานหน้าต่าง **งาน** เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="956ca-180">In the **Tasks** pane, select **Publish**.</span></span>

2. <span data-ttu-id="956ca-181">บนหน้าต้อนรับ เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="956ca-181">On the Welcome page, select **Next**.</span></span>

    ![ยินดีต้อนรับสู่ Publish](media/connect-adfs-wap-report-server/report-server-welcome-publish-new-app-wizard.png)

3. <span data-ttu-id="956ca-183">บนหน้า **การรับรองความถูกต้องล่วงหน้า** เลือก **Active Directory Federation Services (AD FS)** จากนั้นเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="956ca-183">On the **Preauthentication** page, select **Active Directory Federation Services (AD FS)**, then select **Next**.</span></span>

    ![การตรวจสอบล่วงหน้า](media/connect-adfs-wap-report-server/report-server-preauthentication-new-app-wizard.png)

4. <span data-ttu-id="956ca-185">เลือกการรับรองความถูกต้องล่วงหน้า **เว็บและ MSOFBA** ในขณะที่เรากำลังจะตั้งค่าเฉพาะการเข้าถึงเบราว์เซอร์สำหรับเซิร์ฟเวอร์รายงาน และไม่รวมการเข้าถึงแอปสำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="956ca-185">Select **Web and MSOFBA** preauthentication as we are going to set up just the Browser access for the report server, and not mobile app access.</span></span>

    ![ลูกค้าที่ได้รับการสนับสนุน](media/connect-adfs-wap-report-server/report-server-supported-clients-publish-new-app-wizard.png)

5. <span data-ttu-id="956ca-187">เพิ่ม **ฝ่ายที่เกี่ยวข้อง**ที่เราสร้างขึ้นในเซิร์ฟเวอร์ AD FS ดังที่แสดงด้านล่างแล้วเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="956ca-187">Add the **Relying Party** that we created in the AD FS server as shown below, then select **Next**.</span></span>

    ![การเผยแพร่ของฝ่ายที่เกี่ยวข้อง](media/connect-adfs-wap-report-server/report-server-relying-party-publish-new-app-wizard.png)

6. <span data-ttu-id="956ca-189">ในส่วน **URL ภายนอก** ให้ใส่ URL ที่สามารถเข้าถึงได้แบบสาธารณะที่กำหนดค่าบนเซิร์ฟเวอร์ WAP</span><span class="sxs-lookup"><span data-stu-id="956ca-189">In the **External URL** section, put in the publicly accessible URL configured on the WAP server.</span></span> <span data-ttu-id="956ca-190">เพิ่ม URL ที่กำหนดค่าด้วยเซิร์ฟเวอร์รายงาน (ตัวจัดการการกำหนดค่าเซิร์ฟเวอร์รายงาน) ตามที่แสดงด้านล่างในส่วน **URL ของเซิร์ฟเวอร์ Backend**</span><span class="sxs-lookup"><span data-stu-id="956ca-190">Add the URL configured with the report server (Report Server Configuration Manager) as shown below in the **Backend Server URL** section.</span></span> <span data-ttu-id="956ca-191">เพิ่ม SPN ของเซิร์ฟเวอร์รายงานในส่วนของ **SPN ของ เซิร์ฟเวอร์ Backend** </span><span class="sxs-lookup"><span data-stu-id="956ca-191">Add the SPN of the report server in the **Backend server SPN** section.</span></span>

    ![การตั้งค่าการเผยแพร่](media/connect-adfs-wap-report-server/report-server-publishing-settings-new-app-wizard.png)

7. <span data-ttu-id="956ca-193">เลือก **ถัดไป** และ **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="956ca-193">Select **Next** and **Publish**.</span></span>
8. <span data-ttu-id="956ca-194">เรียกใช้คำสั่ง PowerShell ต่อไปนี้เพื่อตรวจสอบการกำหนดค่า WAP</span><span class="sxs-lookup"><span data-stu-id="956ca-194">Run the following PowerShell command to validate the WAP configuration.</span></span>

    ```
    Get-WebApplicationProxyApplication -Name "PBIRSWAP" | FL
    ```

    ![คำสั่ง PowerShell](media/connect-adfs-wap-report-server/report-server-powershell-get-webapplication.png)

## <a name="connect-to-the-report-server-through-the-browser"></a><span data-ttu-id="956ca-196">เชื่อมต่อไปยังเซิร์ฟเวอร์รายงานผ่านเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="956ca-196">Connect to the report server through the browser</span></span>

<span data-ttu-id="956ca-197">จากนั้นคุณสามารถเข้าถึง URL WAP สาธารณะได้ ตัวอย่างเช่น `https://reports.contosolab.com/ReportServer` สำหรับการบริการเว็บและ `https://reports.contosolab.com/Reports` สำหรับพอร์ทัลของเว็บจากเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="956ca-197">You can then access the Public WAP URL, for example, `https://reports.contosolab.com/ReportServer` for the web service and `https://reports.contosolab.com/Reports` for the web portal from the browser.</span></span> <span data-ttu-id="956ca-198">เมื่อคุณได้รับการรับรองความถูกต้องสำเร็จแล้ว คุณจะสามารถเรียกดูรายงานได้</span><span class="sxs-lookup"><span data-stu-id="956ca-198">When you've authenticated successfully, you can view the reports.</span></span>

![ลงชื่อเข้าใช้ AD FS ](media/connect-adfs-wap-report-server/report-server-adfs-sign-in.png)

## <a name="next-steps"></a><span data-ttu-id="956ca-200">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="956ca-200">Next steps</span></span>

* <span data-ttu-id="956ca-201">[กำหนดค่า OAuth เพื่อเชื่อมต่อกับ Power BI Server และ SSRS](../consumer/mobile/mobile-oauth-ssrs.md)
\*[ เซิร์ฟเวอร์รายงาน Power BI คืออะไร](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="956ca-201">[Configure OAuth to connect to Power BI Report Server and SSRS](../consumer/mobile/mobile-oauth-ssrs.md)
\*[What is Power BI Report Server?](get-started.md)</span></span>  

<span data-ttu-id="956ca-202">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="956ca-202">More questions?</span></span> [<span data-ttu-id="956ca-203">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="956ca-203">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
