---
title: เกตเวย์ข้อมูลในองค์กรในเชิงลึก
description: บทความนี้จะดูที่เกตเวย์ภายในองค์กรแบบเชิงลึก ซึ่งจะดูวิธีการทำงานของบริการกับ Azure Active Directory และ Active Directory ภายในเครื่องของคุณเมื่อทำงานกับ Analysis Services
author: arthiriyer
ms.author: arthii
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-gateways
ms.topic: how-to
ms.date: 07/15/2019
LocalizationGroup: Gateways
ms.openlocfilehash: 0964ad3e391c8e066c31ea7bb53f67e97f254422
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96392369"
---
# <a name="on-premises-data-gateway-in-depth"></a><span data-ttu-id="4b95c-104">เกตเวย์ข้อมูลในองค์กรในเชิงลึก</span><span class="sxs-lookup"><span data-stu-id="4b95c-104">On-premises data gateway in-depth</span></span>

[!INCLUDE [gateway-rewrite](../includes/gateway-rewrite.md)]

<span data-ttu-id="4b95c-105">เราได้ย้ายข้อมูลจากบทความนี้ไปยังหลายบทความผ่าน Power BI และเอกสารทั่วไป ทำตามลิงก์ภายใต้หัวเรื่องแต่ละรายการเพื่อค้นหาเนื้อหาที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="4b95c-105">We moved the information from this article to several articles across the Power BI and general docs. Follow the links under each heading to find the relevant content.</span></span>

## <a name="how-the-gateway-works"></a><span data-ttu-id="4b95c-106">เกตเวย์ทำงานอย่างไร</span><span class="sxs-lookup"><span data-stu-id="4b95c-106">How the gateway works</span></span>

<span data-ttu-id="4b95c-107">ดูที่[สถาปัตยกรรมเกตเวย์ข้อมูลภายในองค์กร](/data-integration/gateway/service-gateway-onprem-indepth)</span><span class="sxs-lookup"><span data-stu-id="4b95c-107">See [On-premises data gateway architecture](/data-integration/gateway/service-gateway-onprem-indepth).</span></span>

## <a name="list-of-available-data-source-types"></a><span data-ttu-id="4b95c-108">รายการของชนิดแหล่งข้อมูลที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4b95c-108">List of available data source types</span></span>

<span data-ttu-id="4b95c-109">ดูที่ [จัดการแหล่งข้อมูล](service-gateway-data-sources.md)</span><span class="sxs-lookup"><span data-stu-id="4b95c-109">See [Manage data sources](service-gateway-data-sources.md).</span></span>

## <a name="authentication-to-on-premises-data-sources"></a><span data-ttu-id="4b95c-110">รับรองความถูกต้องไปยังแหล่งข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="4b95c-110">Authentication to on-premises data sources</span></span>

<span data-ttu-id="4b95c-111">ดูที่ [การรับรองความถูกต้องไปยังแหล่งข้อมูลภายในองค์กร](/data-integration/gateway/service-gateway-onprem-indepth#authentication-to-on-premises-data-sources)</span><span class="sxs-lookup"><span data-stu-id="4b95c-111">See [Authentication to on-premises data sources](/data-integration/gateway/service-gateway-onprem-indepth#authentication-to-on-premises-data-sources).</span></span>

## <a name="authentication-to-a-live-analysis-services-data-source"></a><span data-ttu-id="4b95c-112">รับรองความถูกต้องไปยังแหล่งข้อมูล Analysis Services แบบออนไลน์</span><span class="sxs-lookup"><span data-stu-id="4b95c-112">Authentication to a live Analysis Services data source</span></span>

<span data-ttu-id="4b95c-113">ดูที่ [รับรองความถูกต้องไปยังแหล่งข้อมูล Analysis Services แบบออนไลน์](service-gateway-enterprise-manage-ssas.md#authentication-to-a-live-analysis-services-data-source)</span><span class="sxs-lookup"><span data-stu-id="4b95c-113">See [Authentication to a live Analysis Services data source](service-gateway-enterprise-manage-ssas.md#authentication-to-a-live-analysis-services-data-source).</span></span>

## <a name="role-based-security"></a><span data-ttu-id="4b95c-114">รักษาความปลอดภัยตามบทบาท</span><span class="sxs-lookup"><span data-stu-id="4b95c-114">Role-based security</span></span>

<span data-ttu-id="4b95c-115">ดูที่ [การรักษาความปลอดภัยตามบทบาท](service-gateway-enterprise-manage-ssas.md#role-based-security)</span><span class="sxs-lookup"><span data-stu-id="4b95c-115">See [Role-based security](service-gateway-enterprise-manage-ssas.md#role-based-security).</span></span>

## <a name="row-level-security"></a><span data-ttu-id="4b95c-116">รักษาความปลอดภัยระดับแถว</span><span class="sxs-lookup"><span data-stu-id="4b95c-116">Row-level security</span></span>

<span data-ttu-id="4b95c-117">ดูที่ [การรักษาความปลอดภัยระดับแถว](service-gateway-enterprise-manage-ssas.md#row-level-security)</span><span class="sxs-lookup"><span data-stu-id="4b95c-117">See [Row-level security](service-gateway-enterprise-manage-ssas.md#row-level-security).</span></span>

## <a name="what-about-azure-active-directory"></a><span data-ttu-id="4b95c-118">แล้ว Azure Active Directory ล่ะ?</span><span class="sxs-lookup"><span data-stu-id="4b95c-118">What about Azure Active Directory?</span></span>

<span data-ttu-id="4b95c-119">ดูที่ [Azure Active Directory](/data-integration/gateway/service-gateway-onprem-indepth#azure-active-directory)</span><span class="sxs-lookup"><span data-stu-id="4b95c-119">See [Azure Active Directory](/data-integration/gateway/service-gateway-onprem-indepth#azure-active-directory).</span></span>

## <a name="how-do-i-tell-what-my-upn-is"></a><span data-ttu-id="4b95c-120">ฉันจะทราบได้อย่างไรว่า UPN ของฉันเป็นอะไร</span><span class="sxs-lookup"><span data-stu-id="4b95c-120">How do I tell what my UPN is?</span></span>

<span data-ttu-id="4b95c-121">ดูที่ [ฉันจะทราบได้อย่างไรว่า UPN ของฉันเป็นอะไร](/data-integration/gateway/service-gateway-onprem-indepth#how-do-i-tell-what-my-upn-is)</span><span class="sxs-lookup"><span data-stu-id="4b95c-121">See [How do I tell what my UPN is?](/data-integration/gateway/service-gateway-onprem-indepth#how-do-i-tell-what-my-upn-is).</span></span>

## <a name="map-user-names-for-analysis-services-data-sources"></a><span data-ttu-id="4b95c-122">แมปชื่อผู้ใช้สำหรับแหล่งข้อมูล Analysis Services</span><span class="sxs-lookup"><span data-stu-id="4b95c-122">Map user names for Analysis Services data sources</span></span>

<span data-ttu-id="4b95c-123">ดูที่ [แมปชื่อผู้ใช้สำหรับแหล่งข้อมูล Analysis Services](service-gateway-enterprise-manage-ssas.md#map-user-names-for-analysis-services-data-sources)</span><span class="sxs-lookup"><span data-stu-id="4b95c-123">See [Map user names for Analysis Services data sources](service-gateway-enterprise-manage-ssas.md#map-user-names-for-analysis-services-data-sources).</span></span>

## <a name="synchronize-an-on-premises-active-directory-with-azure-active-directory"></a><span data-ttu-id="4b95c-124">รวม Active Directory ภายในองค์กรเข้ากับ Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="4b95c-124">Synchronize an on-premises Active Directory with Azure Active Directory</span></span>

<span data-ttu-id="4b95c-125">ดูที่ [รวม Active Directory ภายในองค์กรเข้ากับ Azure Active Directory](/data-integration/gateway/service-gateway-onprem-indepth#synchronize-an-on-premises-active-directory-with-azure-active-directory)</span><span class="sxs-lookup"><span data-stu-id="4b95c-125">See [Synchronize an on-premises Active Directory with Azure Active Directory](/data-integration/gateway/service-gateway-onprem-indepth#synchronize-an-on-premises-active-directory-with-azure-active-directory).</span></span>

## <a name="what-to-do-next"></a><span data-ttu-id="4b95c-126">สิ่งที่ต้องทำต่อไปคืออะไร?</span><span class="sxs-lookup"><span data-stu-id="4b95c-126">What to do next?</span></span>

<span data-ttu-id="4b95c-127">ดูบทความในแหล่งข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="4b95c-127">See the articles on data sources:</span></span>

<span data-ttu-id="4b95c-128">[จัดการแหล่งข้อมูล](service-gateway-data-sources.md)
[จัดการแหล่งข้อมูลของคุณ - Analysis Services](service-gateway-enterprise-manage-ssas.md)</span><span class="sxs-lookup"><span data-stu-id="4b95c-128">[Manage data sources](service-gateway-data-sources.md)
[Manage your data source - Analysis Services](service-gateway-enterprise-manage-ssas.md)</span></span>  
[<span data-ttu-id="4b95c-129">จัดการแหล่งข้อมูลของคุณ - SAP HANA</span><span class="sxs-lookup"><span data-stu-id="4b95c-129">Manage your data source - SAP HANA</span></span>](service-gateway-enterprise-manage-sap.md)  
[<span data-ttu-id="4b95c-130">จัดการแหล่งข้อมูลของคุณ - SQL Server</span><span class="sxs-lookup"><span data-stu-id="4b95c-130">Manage your data source - SQL Server</span></span>](service-gateway-enterprise-manage-sql.md)  
[<span data-ttu-id="4b95c-131">จัดการแหล่งข้อมูลของคุณ - Oracle</span><span class="sxs-lookup"><span data-stu-id="4b95c-131">Manage your data source - Oracle</span></span>](service-gateway-onprem-manage-oracle.md)  
[<span data-ttu-id="4b95c-132">จัดการแหล่งข้อมูลของคุณ - นำเข้า/รีเฟรชตามตารางเวลา</span><span class="sxs-lookup"><span data-stu-id="4b95c-132">Manage your data source - Import/Scheduled refresh</span></span>](service-gateway-enterprise-manage-scheduled-refresh.md)  

## <a name="where-things-can-go-wrong"></a><span data-ttu-id="4b95c-133">นี่คือจุดที่สามารถเกิดข้อผิดพลาดได้</span><span class="sxs-lookup"><span data-stu-id="4b95c-133">Where things can go wrong</span></span>

<span data-ttu-id="4b95c-134">ดูที่ [แก้ไขปัญหาเกตเวย์ข้อมูลภายในองค์กร](/data-integration/gateway/service-gateway-tshoot)และ [แก้ไขปัญหาเกตเวย์ - Power BI](service-gateway-onprem-tshoot.md)</span><span class="sxs-lookup"><span data-stu-id="4b95c-134">See [Troubleshoot the on-premises data gateway](/data-integration/gateway/service-gateway-tshoot) and [Troubleshoot gateways - Power BI](service-gateway-onprem-tshoot.md).</span></span>

## <a name="sign-in-account"></a><span data-ttu-id="4b95c-135">ลงชื่อเข้าใช้บัญชี</span><span class="sxs-lookup"><span data-stu-id="4b95c-135">Sign in account</span></span>

<span data-ttu-id="4b95c-136">ดูที่ [ลงชื่อเข้าใช้บัญชี](/data-integration/gateway/service-gateway-onprem-indepth#sign-in-account)</span><span class="sxs-lookup"><span data-stu-id="4b95c-136">See [Sign in account](/data-integration/gateway/service-gateway-onprem-indepth#sign-in-account).</span></span>

## <a name="windows-service-account"></a><span data-ttu-id="4b95c-137">บัญชี Windows Service</span><span class="sxs-lookup"><span data-stu-id="4b95c-137">Windows Service account</span></span>

<span data-ttu-id="4b95c-138">ดูที่ [เปลี่ยนบัญชีบริการของเกตเวย์ข้อมูลภายในองค์กร](/data-integration/gateway/service-gateway-service-account)</span><span class="sxs-lookup"><span data-stu-id="4b95c-138">See [Change the on-premises data gateway service account](/data-integration/gateway/service-gateway-service-account).</span></span>

## <a name="ports"></a><span data-ttu-id="4b95c-139">พอร์ต</span><span class="sxs-lookup"><span data-stu-id="4b95c-139">Ports</span></span>

<span data-ttu-id="4b95c-140">ดูที่ [พอร์ต](/data-integration/gateway/service-gateway-communication#ports)</span><span class="sxs-lookup"><span data-stu-id="4b95c-140">See [Ports](/data-integration/gateway/service-gateway-communication#ports).</span></span>

## <a name="forcing-https-communication-with-azure-service-bus"></a><span data-ttu-id="4b95c-141">บังคับให้ HTTPS สื่อสารกับ Azure Service Bus</span><span class="sxs-lookup"><span data-stu-id="4b95c-141">Forcing HTTPS communication with Azure Service Bus</span></span>

<span data-ttu-id="4b95c-142">ดูที่ [บังคับใช้การสื่อสาร HTTPS กับ Azure Service Bus](/data-integration/gateway/service-gateway-communication#force-https-communication-with-azure-service-bus)</span><span class="sxs-lookup"><span data-stu-id="4b95c-142">See [Force HTTPS communication with Azure Service Bus](/data-integration/gateway/service-gateway-communication#force-https-communication-with-azure-service-bus).</span></span>

## <a name="support-for-tls-12"></a><span data-ttu-id="4b95c-143">สนับสนุน TLS 1.1/1.2</span><span class="sxs-lookup"><span data-stu-id="4b95c-143">Support for TLS 1.2</span></span>

<span data-ttu-id="4b95c-144">ดูที่ [TLS 1.2 สำหรับการรับส่งข้อมูลเกตเวย์](/data-integration/gateway/service-gateway-communication#tls-12-for-gateway-traffic)</span><span class="sxs-lookup"><span data-stu-id="4b95c-144">See [TLS 1.2 for gateway traffic](/data-integration/gateway/service-gateway-communication#tls-12-for-gateway-traffic).</span></span>

## <a name="how-to-restart-the-gateway"></a><span data-ttu-id="4b95c-145">วิธีการรีสตาร์ทเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="4b95c-145">How to restart the gateway</span></span>

<span data-ttu-id="4b95c-146">ดูที่ [รีสตาร์ทเกตเวย์](/data-integration/gateway/service-gateway-restart)</span><span class="sxs-lookup"><span data-stu-id="4b95c-146">See [Restart a gateway](/data-integration/gateway/service-gateway-restart).</span></span>

## <a name="next-steps"></a><span data-ttu-id="4b95c-147">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4b95c-147">Next steps</span></span>

[<span data-ttu-id="4b95c-148">เกตเวย์ข้อมูลภายในองค์กรคืออะไร</span><span class="sxs-lookup"><span data-stu-id="4b95c-148">What is the on-premises data gateway?</span></span>](service-gateway-onprem.md)

<span data-ttu-id="4b95c-149">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4b95c-149">More questions?</span></span> [<span data-ttu-id="4b95c-150">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="4b95c-150">Try the Power BI Community</span></span>](https://community.powerbi.com/)