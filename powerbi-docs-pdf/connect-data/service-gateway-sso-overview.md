---
title: ภาพรวมของการลงชื่อเข้าใช้ครั้งเดียว (SSO) สำหรับเกตเวย์ใน Power BI
description: กำหนดค่าเกตเวย์ของคุณเมื่อต้องการเปิดใช้งานการลงชื่อเข้าใช้ครั้งเดียว (SSO) จาก Power BI ไปยังแหล่งข้อมูลในองค์กร
author: arthiriyer
ms.author: arthii
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-gateways
ms.topic: how-to
ms.date: 10/10/2019
LocalizationGroup: Gateways
ms.openlocfilehash: 4a4bb6ccb74ce08ea1ff63f44b1c2c5406c527ad
ms.sourcegitcommit: eef4eee24695570ae3186b4d8d99660df16bf54c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/23/2020
ms.locfileid: "85231302"
---
# <a name="overview-of-single-sign-on-sso-for-gateways-in-power-bi"></a><span data-ttu-id="28a4d-103">ภาพรวมของการลงชื่อเข้าใช้ครั้งเดียว (SSO) สำหรับเกตเวย์ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="28a4d-103">Overview of single sign-on (SSO) for gateways in Power BI</span></span>

<span data-ttu-id="28a4d-104">คุณสามารถเชื่อมต่อด้วยการลงชื่อเข้าใช้ครั้งเดียว ซึ่งเปิดใช้งานรายงานและแดชบอร์ดของ Power BI เพื่อปรับปรุงจากข้อมูลในองค์กรแบบเรียลไทม์ โดยการกำหนดค่าในเกตเวย์ข้อมูลในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="28a4d-104">You can get seamless single sign-on connectivity, enabling Power BI reports and dashboards to update in real time from on-premises data, by configuring your on-premises data gateway.</span></span> <span data-ttu-id="28a4d-105">คุณมีตัวเลือกในการกำหนดค่าเกตเวย์ของคุณด้วยการมอบสิทธิ์แบบจำกัดของ [Kerberos](service-gateway-sso-kerberos.md) หรือ Security Assertion Markup Language ([SAML](service-gateway-sso-saml.md))</span><span class="sxs-lookup"><span data-stu-id="28a4d-105">You have the option of configuring your gateway with either [Kerberos](service-gateway-sso-kerberos.md) constrained delegation or Security Assertion Markup Language ([SAML](service-gateway-sso-saml.md)).</span></span> <span data-ttu-id="28a4d-106">เกตเวย์ข้อมูลภายในองค์กรสนับสนุน SSO โดยใช้ [DirectQuery](desktop-directquery-about.md) หรือสำหรับการรีเฟรช ซึ่งเชื่อมต่อกับแหล่งข้อมูลในองค์กร</span><span class="sxs-lookup"><span data-stu-id="28a4d-106">The on-premises data gateway supports SSO by using [DirectQuery](desktop-directquery-about.md) or for Refresh, which connects to on-premises data sources.</span></span> 

<span data-ttu-id="28a4d-107">Power BI รองรับแหล่งข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="28a4d-107">Power BI supports the following data sources:</span></span>

* <span data-ttu-id="28a4d-108">SQL Server (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="28a4d-108">SQL Server (Kerberos)</span></span>
* <span data-ttu-id="28a4d-109">SAP HANA (Kerberos และ SAML)</span><span class="sxs-lookup"><span data-stu-id="28a4d-109">SAP HANA (Kerberos and SAML)</span></span>
* <span data-ttu-id="28a4d-110">SAP BW Application Server (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="28a4d-110">SAP BW Application Server (Kerberos)</span></span>
* <span data-ttu-id="28a4d-111"> เซิร์ฟเวอร์ข้อความของ SAP BW (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="28a4d-111">SAP BW Message Server (Kerberos)</span></span> 
* <span data-ttu-id="28a4d-112">Oracle (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="28a4d-112">Oracle (Kerberos)</span></span> 
* <span data-ttu-id="28a4d-113">Teradata (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="28a4d-113">Teradata (Kerberos)</span></span>
* <span data-ttu-id="28a4d-114">Spark (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="28a4d-114">Spark (Kerberos)</span></span>
* <span data-ttu-id="28a4d-115">Impala (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="28a4d-115">Impala (Kerberos)</span></span>

<span data-ttu-id="28a4d-116">ขณะนี้เราไม่สนับสนุน SSO สำหรับ[ไฟล์นามสกุล M](https://github.com/microsoft/DataConnectors/blob/master/docs/m-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="28a4d-116">We don't currently support SSO for [M-extensions](https://github.com/microsoft/DataConnectors/blob/master/docs/m-extensions.md).</span></span>

<span data-ttu-id="28a4d-117">เมื่อผู้ใช้โต้ตอบกับรายงาน DirectQuery ในบริการของ Power BI การดำเนินการแก้ไขตัวกรองข้าม แบ่งส่วน เรียงลำดับ และรายงานแต่ละครั้งอาจส่งผลต่อคิวรีต่าง ๆ ที่ดำเนินการสดกับแหล่งข้อมูลพื้นฐานภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="28a4d-117">When a user interacts with a DirectQuery report in the Power BI Service, each cross-filter, slice, sort, and report editing operation can result in queries that execute live against the underlying on-premises data source.</span></span> <span data-ttu-id="28a4d-118">เมื่อคุณกำหนดค่า SSO สำหรับแหล่งข้อมูล คิวรีจะดำเนินการภายใต้ ข้อมูลประจำตัวของผู้ใช้ที่โต้ตอบกับ Power BI (นั่นคือเมื่อทำผ่านเว็บหรือแอปสำหรับอุปกรณ์เคลื่อนที่ของ Power BI)</span><span class="sxs-lookup"><span data-stu-id="28a4d-118">When you configure SSO for the data source, queries execute under the identity of the user that interacts with Power BI (that is, through the web experience or Power BI mobile apps).</span></span> <span data-ttu-id="28a4d-119">ดังนั้น ผู้ใช้แต่ละคนจะเห็นข้อมูลที่พวกเขามีสิทธิ์ในแหล่งข้อมูลพื้นฐานอย่างแม่นยำ</span><span class="sxs-lookup"><span data-stu-id="28a4d-119">Therefore, each user sees precisely the data for which they have permissions in the underlying data source.</span></span> 

<span data-ttu-id="28a4d-120">คุณยังสามารถกำหนดค่ารายงานที่ตั้งค่าสำหรับการรีเฟรชในบริการ Power BI เพื่อใช้ SSO ได้</span><span class="sxs-lookup"><span data-stu-id="28a4d-120">You can also configure a report which is set up for refresh in the Power BI Service to use SSO.</span></span> <span data-ttu-id="28a4d-121">เมื่อคุณกำหนดค่า SSO สำหรับแหล่งข้อมูลนี้แล้ว คิวรีจะดำเนินการภายใต้ข้อมูลประจำตัวของเจ้าของชุดข้อมูลภายใน Power BI</span><span class="sxs-lookup"><span data-stu-id="28a4d-121">When you configure SSO for this data source, queries execute under the identity of the dataset owner within Power BI.</span></span> <span data-ttu-id="28a4d-122">ดังนั้น การรีเฟรชจะเกิดขึ้นตามสิทธิ์ของเจ้าของชุดข้อมูลในแหล่งข้อมูลพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="28a4d-122">Therefore, the refresh happens based on the dataset owner's permissions on the underlying data source.</span></span> <span data-ttu-id="28a4d-123">ในขณะนี้การรีเฟรชโดยใช้ SSO เปิดใช้งานเฉพาะสำหรับแหล่งข้อมูลที่ใช้การมอบสิทธิ์แบบจำกัดของ [Kerberos](service-gateway-sso-kerberos.md)</span><span class="sxs-lookup"><span data-stu-id="28a4d-123">Refresh using SSO is currently enabled only for data sources using [Kerberos](service-gateway-sso-kerberos.md) constrained delegation</span></span> 

## <a name="query-steps-when-running-sso"></a><span data-ttu-id="28a4d-124">ขั้นตอนการคิวรีเมื่อเรียกใช้ SSO</span><span class="sxs-lookup"><span data-stu-id="28a4d-124">Query steps when running SSO</span></span>

<span data-ttu-id="28a4d-125">คิวรีที่ทำงานโดยใช้ SSO ประกอบด้วยสามขั้นตอน ดังที่แสดงในไดอะแกรมต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="28a4d-125">A query that runs with SSO consists of three steps, as shown in the following diagram.</span></span>

![ขั้นตอนการคิวรีของ SSO](media/service-gateway-sso-overview/sso-query-steps.png)

<span data-ttu-id="28a4d-127">นี่เป็นรายละเอียดเพิ่มเติมเกี่ยวกับแต่ละขั้นตอน:</span><span class="sxs-lookup"><span data-stu-id="28a4d-127">Here are additional details about each step:</span></span>

1. <span data-ttu-id="28a4d-128">สำหรับการคิวรีแต่ละครั้ง บริการของ Power BI ประกอบด้วย*ชื่อผู้ใช้หลัก (UPN)* ซึ่งเป็นชื่อผู้ใช้แบบเต็มที่ผ่านการรับรองของผู้ใช้ที่ลงชื่อเข้าใช้บริการของ Power BI ในปัจจุบัน เมื่อส่งการร้องขอคิวรีไปยังเกตเวย์ที่กำหนดค่าไว้</span><span class="sxs-lookup"><span data-stu-id="28a4d-128">For each query, the Power BI service includes the *user principal name (UPN)*, which is the fully qualified username of the user currently signed in to the Power BI service, when it sends a query request to the configured gateway.</span></span>

2. <span data-ttu-id="28a4d-129">เกตเวย์ต้องแมปค่า UPN ของ Azure Active Directory ไปยังข้อมูลประจำตัวของ Active Directory ในเครื่อง:</span><span class="sxs-lookup"><span data-stu-id="28a4d-129">The gateway must map the Azure Active Directory UPN to a local Active Directory identity:</span></span>

   <span data-ttu-id="28a4d-130">a.</span><span class="sxs-lookup"><span data-stu-id="28a4d-130">a.</span></span> <span data-ttu-id="28a4d-131">ถ้า Azure AD DirSync (หรือที่เรียกว่า*Azure AD Connect*) มีการกำหนดค่าแล้ว การแมปจะทำงานโดยอัตโนมัติในเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="28a4d-131">If Azure AD DirSync (also known as *Azure AD Connect*) is configured, then the mapping works automatically in the gateway.</span></span>

   <span data-ttu-id="28a4d-132">b.</span><span class="sxs-lookup"><span data-stu-id="28a4d-132">b.</span></span>  <span data-ttu-id="28a4d-133">มิฉะนั้น เกตเวย์สามารถค้นหาและแมป Azure AD UPN ไปยังผู้ใช้ AD ภายในเครื่อง โดยการค้นหากับโดเมน Active Directory ในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="28a4d-133">Otherwise, the gateway can look up and map the Azure AD UPN to a local AD user by performing a lookup against the local Active Directory domain.</span></span>

3. <span data-ttu-id="28a4d-134">กระบวนการบริการเกตเวย์จะเลียนแบบเป็นผู้ใช้ภายในเครื่องที่ถูกแมป เปิดการเชื่อมต่อกับฐานข้อมูลเบื้องต้น แล้วส่งคิวรี</span><span class="sxs-lookup"><span data-stu-id="28a4d-134">The gateway service process impersonates the mapped local user, opens the connection to the underlying database, and then sends the query.</span></span> <span data-ttu-id="28a4d-135">คุณไม่จำเป็นต้องติดตั้งเกตเวย์บนคอมพิวเตอร์เครื่องเดียวกับฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="28a4d-135">You don't need to install the gateway on the same machine as the database.</span></span>

## <a name="next-steps"></a><span data-ttu-id="28a4d-136">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="28a4d-136">Next steps</span></span>

<span data-ttu-id="28a4d-137">ตอนนี้คุณเข้าใจพื้นฐานของการเปิดใช้งาน SSO ผ่านเกตเวย์แล้ว โปรดอ่านข้อมูลโดยละเอียดเกี่ยวกับ Kerberos และ SAML:</span><span class="sxs-lookup"><span data-stu-id="28a4d-137">Now that you understand the basics of enabling SSO through the gateway, read more detailed information about Kerberos and SAML:</span></span>

* [<span data-ttu-id="28a4d-138">การลงชื่อเข้าใช้ครั้งเดียว (SSO) - Kerberos</span><span class="sxs-lookup"><span data-stu-id="28a4d-138">Single sign-on (SSO) - Kerberos</span></span>](service-gateway-sso-kerberos.md)
* [<span data-ttu-id="28a4d-139">การลงชื่อเข้าใช้ครั้งเดียว (SSO) - SAML</span><span class="sxs-lookup"><span data-stu-id="28a4d-139">Single sign-on (SSO) - SAML</span></span>](service-gateway-sso-saml.md)
