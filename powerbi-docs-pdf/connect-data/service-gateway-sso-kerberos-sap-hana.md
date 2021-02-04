---
title: ใช้ Kerberos สำหรับลงชื่อเข้าระบบครั้งเดียว (SSO) ไปยัง SAP HANA
description: กำหนดค่าเซิร์ฟเวอร์ SAP Hana ของคุณเพื่อเปิดใช้งาน SSO จากบริการของ Power BI
author: arthiriyer
ms.author: arthii
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-gateways
ms.topic: how-to
ms.date: 12/16/2020
LocalizationGroup: Gateways
ms.openlocfilehash: 3f50b174e8293d75a0077e1799cb64ff4fdcd696
ms.sourcegitcommit: 5c09d121d3205e65fb33a2eca0e60bc30e777773
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/18/2020
ms.locfileid: "97675131"
---
# <a name="use-kerberos-for-single-sign-on-sso-to-sap-hana"></a><span data-ttu-id="458f9-103">ใช้ Kerberos สำหรับลงชื่อเข้าระบบครั้งเดียว (SSO) ไปยัง SAP HANA</span><span class="sxs-lookup"><span data-stu-id="458f9-103">Use Kerberos for single sign-on (SSO) to SAP HANA</span></span>

> [!IMPORTANT]
> <span data-ttu-id="458f9-104">เพราะ [SAP ไม่รองรับ OpenSSL อีกต่อไป](https://help.sap.com/viewer/b3ee5778bc2e4a089d3299b82ec762a7/2.0.05/en-US/de15ffb1bb5710148386ffdfd857482a.html) Microsoft จึงยุติการรองรับด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="458f9-104">As [SAP no longer supports the OpenSSL](https://help.sap.com/viewer/b3ee5778bc2e4a089d3299b82ec762a7/2.0.05/en-US/de15ffb1bb5710148386ffdfd857482a.html), Microsoft also has discontinued its support.</span></span> <span data-ttu-id="458f9-105">การเชื่อมต่อที่มีอยู่จะยังคงใช้งานได้ แต่คุณจะไม่สามารถสร้างการเชื่อมต่อใหม่ได้ตั้งแต่เดือนกุมภาพันธ์ 2021 เป็นต้นไป</span><span class="sxs-lookup"><span data-stu-id="458f9-105">Existing connections will continue to work, but you won't be able to create new connections starting February 2021.</span></span> <span data-ttu-id="458f9-106">หากต้องการใช้งานในอนาคต โปรดใช้ CommonCryptoLib แทน</span><span class="sxs-lookup"><span data-stu-id="458f9-106">Going forward, please use CommonCryptoLib instead.</span></span>

<span data-ttu-id="458f9-107">บทความนี้อธิบายวิธีกำหนดค่าแหล่งข้อมูล SAP HANA ของคุณเพื่อเปิดใช้งาน SSO จากบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="458f9-107">This article describes how to configure your SAP HANA data source to enable SSO from the Power BI service.</span></span>

> [!NOTE]
> <span data-ttu-id="458f9-108">ก่อนที่คุณจะพยายามรีเฟรชรายงานที่ยึดกับ SAP HANA ที่ใช้ Kerberos SSO ให้ทำตามทั้งขั้นตอนในบทความนี้และขั้นตอนใน [กำหนดค่า Kerberos SSO](service-gateway-sso-kerberos.md)</span><span class="sxs-lookup"><span data-stu-id="458f9-108">Before you attempt to refresh a SAP HANA-based report that uses Kerberos SSO, complete both the steps in this article and the steps in [Configure Kerberos SSO](service-gateway-sso-kerberos.md).</span></span>

## <a name="enable-sso-for-sap-hana"></a><span data-ttu-id="458f9-109">เปิดใช้งาน SSO สำหรับ SAP HANA</span><span class="sxs-lookup"><span data-stu-id="458f9-109">Enable SSO for SAP HANA</span></span>

<span data-ttu-id="458f9-110">เพื่อเปิดใช้งาน SSO สำหรับ SAP HANA ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="458f9-110">To enable SSO for SAP HANA, follow these steps:</span></span>

1. <span data-ttu-id="458f9-111">ตรวจสอบให้แน่ใจว่า เซิร์ฟเวอร์ SAP HANA ทำงานด้วยเวอร์ชันขั้นต่ำ ซึ่งขึ้นอยู่กับระดับเซิร์ฟเวอร์แพลตฟอร์ม SAP HANA ของคุณ:</span><span class="sxs-lookup"><span data-stu-id="458f9-111">Ensure the SAP HANA server is running the required minimum version, which depends on your SAP HANA server platform level:</span></span>
   - [<span data-ttu-id="458f9-112">HANA 2 SPS 01 Rev 012.03</span><span class="sxs-lookup"><span data-stu-id="458f9-112">HANA 2 SPS 01 Rev 012.03</span></span>](https://launchpad.support.sap.com/#/notes/2557386)
   - [<span data-ttu-id="458f9-113">HANA 2 SPS 02 Rev 22</span><span class="sxs-lookup"><span data-stu-id="458f9-113">HANA 2 SPS 02 Rev 22</span></span>](https://launchpad.support.sap.com/#/notes/2547324)
   - [<span data-ttu-id="458f9-114">HANA 1 SP 12 Rev 122.13</span><span class="sxs-lookup"><span data-stu-id="458f9-114">HANA 1 SP 12 Rev 122.13</span></span>](https://launchpad.support.sap.com/#/notes/2528439)

2. <span data-ttu-id="458f9-115">บนเครื่องเกตเวย์ ติดตั้งโปรแกรมควบคุม SAP HANA ODBC ล่าสุด</span><span class="sxs-lookup"><span data-stu-id="458f9-115">On the gateway machine, install the latest SAP HANA ODBC driver.</span></span> <span data-ttu-id="458f9-116">เวอร์ชันขั้นต่ำคือ HANA ODBC เวอร์ชัน 2.00.020.00 ที่ออกเดือน สิงหาคม 2017</span><span class="sxs-lookup"><span data-stu-id="458f9-116">The minimum version is HANA ODBC version 2.00.020.00 from August 2017.</span></span>

3. <span data-ttu-id="458f9-117">ตรวจสอบให้แน่ใจว่าเซิร์ฟเวอร์ SAP Hana ได้รับการกำหนดค่าสำหรับ SSO ที่ใช้ Kerberos</span><span class="sxs-lookup"><span data-stu-id="458f9-117">Ensure that the SAP HANA server has been configured for Kerberos-based SSO.</span></span> <span data-ttu-id="458f9-118">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่า SSO สำหรับ SAP HANA โดยใช้ Kerberos โปรดดู [ลงชื่อเข้าระบบครั้งเดียวโดยใช้ Kerberos](https://help.sap.com/viewer/b3ee5778bc2e4a089d3299b82ec762a7/2.0.03/1885fad82df943c2a1974f5da0eed66d.html) ในคู่มือการรักษาความปลอดภัย SAP HANA</span><span class="sxs-lookup"><span data-stu-id="458f9-118">For more information about setting up SSO for SAP HANA by using Kerberos, see [Single Sign-on Using Kerberos](https://help.sap.com/viewer/b3ee5778bc2e4a089d3299b82ec762a7/2.0.03/1885fad82df943c2a1974f5da0eed66d.html) in the SAP HANA Security Guide.</span></span> <span data-ttu-id="458f9-119">โปรดดูลิงก์จากหน้านั้น โดยเฉพาะอย่างยิ่ง SAP Note 1837331 – HOWTO HANA DBSSO Kerberos/Active Directory</span><span class="sxs-lookup"><span data-stu-id="458f9-119">Also see the links from that page, particularly SAP Note 1837331 – HOWTO HANA DBSSO Kerberos/Active Directory.</span></span>

<span data-ttu-id="458f9-120">เราขอแนะนำให้ทำตามขั้นตอนเพิ่มเติมต่อไปนี้ ซึ่งสามารถเพิ่มประสิทธิภาพการปรับปรุงเล็กน้อย:</span><span class="sxs-lookup"><span data-stu-id="458f9-120">We also recommend following these additional steps, which can yield a small performance improvement:</span></span>

1. <span data-ttu-id="458f9-121">ในไดเรกทอรีการติดตั้งเกตเวย์ ค้นหาและเปิดไฟล์ที่มีการกำหนดค่าตามนี้: Microsoft.PowerBI.DataMovement.Pipeline.GatewayCore.dll.config.</span><span class="sxs-lookup"><span data-stu-id="458f9-121">In the gateway installation directory, find and open this configuration file: Microsoft.PowerBI.DataMovement.Pipeline.GatewayCore.dll.config.</span></span>

2. <span data-ttu-id="458f9-122">ค้นหาคุณสมบัติ `FullDomainResolutionEnabled` และเปลี่ยนค่าเป็น `True`</span><span class="sxs-lookup"><span data-stu-id="458f9-122">Find the `FullDomainResolutionEnabled` property, and change its value to `True`.</span></span>

    ```xml
    <setting name=" FullDomainResolutionEnabled " serializeAs="String">
          <value>True</value>
    </setting>
    ```

<span data-ttu-id="458f9-123">ตอนนี้ให้[เปิดใช้รายงาน Power BI](service-gateway-sso-kerberos.md#run-a-power-bi-report)</span><span class="sxs-lookup"><span data-stu-id="458f9-123">Now, [Run a Power BI report](service-gateway-sso-kerberos.md#run-a-power-bi-report).</span></span>

## <a name="next-steps"></a><span data-ttu-id="458f9-124">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="458f9-124">Next steps</span></span>

<span data-ttu-id="458f9-125">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเกตเวย์ข้อมูลภายในองค์กรและ DirectQuery ให้ดูแหล่งข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="458f9-125">For more information about the on-premises data gateway and DirectQuery, see the following resources:</span></span>

* [<span data-ttu-id="458f9-126">เกตเวย์ข้อมูลภายในองค์กรคืออะไร</span><span class="sxs-lookup"><span data-stu-id="458f9-126">What is an on-premises data gateway?</span></span>](/data-integration/gateway/service-gateway-onprem)
* [<span data-ttu-id="458f9-127">DirectQuery ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="458f9-127">DirectQuery in Power BI</span></span>](desktop-directquery-about.md)
* [<span data-ttu-id="458f9-128">แหล่งข้อมูลที่สนับสนุนโดย DirectQuery</span><span class="sxs-lookup"><span data-stu-id="458f9-128">Data sources supported by DirectQuery</span></span>](power-bi-data-sources.md)
* [<span data-ttu-id="458f9-129">DirectQuery และ SAP BW</span><span class="sxs-lookup"><span data-stu-id="458f9-129">DirectQuery and SAP BW</span></span>](desktop-directquery-sap-bw.md)
* [<span data-ttu-id="458f9-130">DirectQuery และ SAP HANA</span><span class="sxs-lookup"><span data-stu-id="458f9-130">DirectQuery and SAP HANA</span></span>](desktop-directquery-sap-hana.md)
