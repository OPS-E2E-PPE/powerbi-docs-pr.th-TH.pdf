---
title: จัดการแหล่งข้อมูลของคุณ - นำเข้า/รีเฟรชตามกำหนดการ
description: วิธีการจัดการเกตเวย์ข้อมูลภายในองค์กร และแหล่งข้อมูลของเกตเวย์นั้นๆ บทความนี้มีไว้เฉพาะสำหรับแหล่งข้อมูลที่สามารถใช้ได้กับการนำเข้า/การรีเฟรชที่กำหนดตารางเวลา
author: arthiriyer
ms.author: arthii
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-gateways
ms.topic: how-to
ms.date: 11/17/2020
LocalizationGroup: Gateways
ms.openlocfilehash: b6f7e3719678d0617f40b9a33f2de20a6b5010c0
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410309"
---
# <a name="manage-your-data-source---importscheduled-refresh"></a><span data-ttu-id="ebd49-104">จัดการแหล่งข้อมูลของคุณ - นำเข้า/รีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="ebd49-104">Manage your data source - Import/scheduled refresh</span></span>

[!INCLUDE [gateway-rewrite](../includes/gateway-rewrite.md)]

<span data-ttu-id="ebd49-105">หลังจากคุณ[ติดตั้งเกตเวย์ข้อมูลภายในองค์กรแล้ว](/data-integration/gateway/service-gateway-install) คุณจะต้อง[เพิ่มแหล่งข้อมูล](service-gateway-data-sources.md#add-a-data-source)ที่สามารถใช้ได้กับเกตเวย์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="ebd49-105">After you [install the on-premises data gateway](/data-integration/gateway/service-gateway-install), you need to [add data sources](service-gateway-data-sources.md#add-a-data-source) that can be used with the gateway.</span></span> <span data-ttu-id="ebd49-106">บทความนี้จะดูที่วิธีการทำงานกับเกตเวย์และแหล่งข้อมูลที่จะใช้สำหรับการรีเฟรชตามกำหนดการที่ตรงกันข้ามกับ DirectQuery หรือการเชื่อมต่อแบบสด</span><span class="sxs-lookup"><span data-stu-id="ebd49-106">This article looks at how to work with gateways and data sources that are used for scheduled refresh as opposed to DirectQuery or live connections.</span></span>

## <a name="add-a-data-source"></a><span data-ttu-id="ebd49-107">เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ebd49-107">Add a data source</span></span>

<span data-ttu-id="ebd49-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเพิ่มแหล่งข้อมูล ให้ดู[เพิ่มแหล่งข้อมูล](service-gateway-data-sources.md#add-a-data-source)</span><span class="sxs-lookup"><span data-stu-id="ebd49-108">For more information about how to add a data source, see [Add a data source](service-gateway-data-sources.md#add-a-data-source).</span></span> <span data-ttu-id="ebd49-109">เลือกชนิดแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ebd49-109">Select a data source type.</span></span>

<span data-ttu-id="ebd49-110">ชนิดแหล่งข้อมูลทั้งหมดที่อยู่ในรายการสามารถใช้สำหรับการรีเฟรชตามกำหนดการกับเกตเวย์ข้อมูลภายในองค์กรได้</span><span class="sxs-lookup"><span data-stu-id="ebd49-110">All of the data source types listed can be used for scheduled refresh with the on-premises data gateway.</span></span> <span data-ttu-id="ebd49-111">Analysis Services, SQL Server และ SAP HANA สามารถใช้กับทั้งการรีเฟรชตามกำหนดการ หรือกับการเชื่อมต่อ DirectQuery/การเชื่อมต่อสดได้</span><span class="sxs-lookup"><span data-stu-id="ebd49-111">Analysis Services, SQL Server, and SAP HANA can be used for either scheduled refresh or DirectQuery/live connections.</span></span>

![เลือกแหล่งข้อมูล](media/service-gateway-enterprise-manage-scheduled-refresh/datasourcesettings2.png)

<span data-ttu-id="ebd49-113">จากนั้นกรอกข้อมูลสำหรับแหล่งข้อมูล ซึ่งรวมถึงข้อมูลแหล่งที่มาและข้อมูลประจำตัวที่ใช้เพื่อเข้าถึงแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ebd49-113">Then fill in the information for the data source, which includes the source information and credentials that are used to access the data source.</span></span>

> [!NOTE]
> <span data-ttu-id="ebd49-114">คิวรีทั้งหมดที่ไปยังแหล่งข้อมูลจะทำงานโดยใช้ข้อมูลประจำตัวเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="ebd49-114">All queries to the data source run by using these credentials.</span></span> <span data-ttu-id="ebd49-115">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการจัดเก็บข้อมูลประจำตัว ให้ดู [การจัดเก็บข้อมูลประจำตัวที่เข้ารหัสไว้ในระบบคลาวด์](service-gateway-data-sources.md#store-encrypted-credentials-in-the-cloud)</span><span class="sxs-lookup"><span data-stu-id="ebd49-115">To learn more about how credentials are stored, see [Store encrypted credentials in the cloud](service-gateway-data-sources.md#store-encrypted-credentials-in-the-cloud).</span></span>

![การกรอกข้อมูลในการตั้งค่าแหล่งข้อมูล](media/service-gateway-enterprise-manage-scheduled-refresh/datasourcesettings3-oracle.png)

<span data-ttu-id="ebd49-117">สำหรับรายการของชนิดแหล่งข้อมูลที่สามารถใช้ได้กับการรีเฟรชตามกำหนดการ ดูที่ [รายการของชนิดแหล่งข้อมูลที่พร้อมใช้งาน](service-gateway-data-sources.md#list-of-available-data-source-types)</span><span class="sxs-lookup"><span data-stu-id="ebd49-117">For a list of data source types that can be used with scheduled refresh, see [List of available data source types](service-gateway-data-sources.md#list-of-available-data-source-types).</span></span>

<span data-ttu-id="ebd49-118">หลังจากที่คุณกรอกข้อมูลทุกอย่างแล้ว ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="ebd49-118">After you fill in everything, select **Add**.</span></span> <span data-ttu-id="ebd49-119">ตอนนี้คุณสามารถใช้แหล่งข้อมูลนี้สำหรับการรีเฟรชตามกำหนดการกับข้อมูลภายในองค์กรของคุณได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="ebd49-119">You can now use this data source for scheduled refresh with your on-premises data.</span></span> <span data-ttu-id="ebd49-120">คุณจะเห็น *การเชื่อมต่อสำเร็จ* หากการดำเนินการเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="ebd49-120">You see *Connection Successful* if it succeeded.</span></span>

![การแสดงสถานะการเชื่อมต่อ](media/service-gateway-enterprise-manage-scheduled-refresh/datasourcesettings4.png)

### <a name="advanced-settings"></a><span data-ttu-id="ebd49-122">การตั้งค่าขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="ebd49-122">Advanced settings</span></span>

<span data-ttu-id="ebd49-123">อีกทางหนึ่งคือคุณสามารถกำหนดค่าระดับความเป็นส่วนตัวให้กับแหล่งข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="ebd49-123">Optionally, you can configure the privacy level for your data source.</span></span> <span data-ttu-id="ebd49-124">การตั้งค่านี้จะช่วยควบคุมวิธีการรวมข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="ebd49-124">This setting controls how data can be combined.</span></span> <span data-ttu-id="ebd49-125">ซึ่งใช้ได้เฉพาะกับการรีเฟรชตามกำหนดการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ebd49-125">It's only used for scheduled refresh.</span></span> <span data-ttu-id="ebd49-126">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับระดับความเป็นส่วนตัวสำหรับแหล่งข้อมูลของคุณ ให้ดู [ระดับความเป็นส่วนตัว (Power Query)](https://support.office.com/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540)</span><span class="sxs-lookup"><span data-stu-id="ebd49-126">To learn more about privacy levels for your data source, see [Privacy levels (Power Query)](https://support.office.com/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540).</span></span>

![การตั้งค่าระดับความเป็นส่วนตัว](media/service-gateway-enterprise-manage-scheduled-refresh/datasourcesettings9.png)

## <a name="use-the-data-source-for-scheduled-refresh"></a><span data-ttu-id="ebd49-128">ใช้แหล่งข้อมูลสำหรับการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="ebd49-128">Use the data source for scheduled refresh</span></span>

<span data-ttu-id="ebd49-129">หลังจากที่คุณสร้างแหล่งข้อมูล รายการนี้จะพร้อมใช้งานเมื่อต้องใช้ทั้งกับการเชื่อมต่อ DirectQuery หรือการเชื่อมต่อสดผ่านการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="ebd49-129">After you create the data source, it's available to use with either DirectQuery connections or through scheduled refresh.</span></span>

> [!NOTE]
> <span data-ttu-id="ebd49-130">ชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูลจะต้องตรงกับ Power BI Desktop และแหล่งข้อมูลภายในเกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="ebd49-130">The server and database names must match between Power BI Desktop and the data source within the on-premises data gateway.</span></span>

<span data-ttu-id="ebd49-131">การเชื่อมโยงระหว่างชุดข้อมูลของคุณและแหล่งข้อมูลภายในเกตเวย์จะเป็นไปตามชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="ebd49-131">The link between your dataset and the data source within the gateway is based on your server name and database name.</span></span> <span data-ttu-id="ebd49-132">ชื่อเหล่านี้ต้องตรงกัน</span><span class="sxs-lookup"><span data-stu-id="ebd49-132">These names must match.</span></span> <span data-ttu-id="ebd49-133">ตัวอย่างเช่น ถ้าคุณใส่ที่อยู่ IP สำหรับชื่อเซิร์ฟเวอร์ภายใน Power BI Desktop คุณต้องใช้ที่อยู่ IP สำหรับแหล่งข้อมูลภายในการกำหนดค่าเกตเวย์ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="ebd49-133">For example, if you supply an IP address for the server name within Power BI Desktop, you must use the IP address for the data source within the gateway configuration.</span></span> <span data-ttu-id="ebd49-134">ถ้าคุณใช้ *SERVER\INSTANCE* ใน Power BI Desktop คุณต้องใช้ภายในแหล่งข้อมูลที่กำหนดค่าไว้สำหรับเกตเวย์ดังกล่าวด้วย</span><span class="sxs-lookup"><span data-stu-id="ebd49-134">If you use *SERVER\INSTANCE* in Power BI Desktop, you also must use it within the data source configured for the gateway.</span></span>

<span data-ttu-id="ebd49-135">ถ้าคุณอยู่ในแท็บ **ผู้ใช้** ของแหล่งข้อมูลที่กำหนดค่าไว้ภายในเกตเวย์ และชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูลตรงกัน คุณจะเห็นเกตเวย์เป็นตัวเลือกเพื่อใช้กับการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="ebd49-135">If you're listed in the **Users** tab of the data source configured within the gateway and the server name and database name match, you see the gateway as an option to use with scheduled refresh.</span></span>

![การแสดงรายชื่อผู้ใช้](media/service-gateway-enterprise-manage-scheduled-refresh/powerbi-gateway-enterprise-schedule-refresh.png)

> [!IMPORTANT]
> <span data-ttu-id="ebd49-137">เมื่อเผยแพร่ซ้ำ เจ้าของชุดข้อมูลจะต้องเชื่อมโยงชุดข้อมูลกับเกตเวย์และแหล่งข้อมูลที่เกี่ยวข้องอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="ebd49-137">Upon republish, the data set owner must reassociate the dataset to a gatweay and corresponding data source again.</span></span> <span data-ttu-id="ebd49-138">การเชื่อมโยงก่อนหน้านี้ไม่ได้รับการรักษาไว้เมื่อเผยแพร่ใหม่</span><span class="sxs-lookup"><span data-stu-id="ebd49-138">The previous association is not maintained upon republish.</span></span> 

> [!WARNING]
> <span data-ttu-id="ebd49-139">ถ้าชุดข้อมูลของคุณประกอบด้วยแหล่งข้อมูลหลายแหล่ง คุณต้องเพิ่มแต่ละแหล่งข้อมูลภายในเกตเวย์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="ebd49-139">If your dataset contains multiple data sources, each data source must be added within the gateway.</span></span> <span data-ttu-id="ebd49-140">ถ้าไม่ได้เพิ่มแหล่งข้อมูลอย่างน้อยหนึ่งแหล่งเข้าไปในเกตเวย์ คุณจะไม่เห็นเกตเวย์ดังกล่าวเป็นสถานะพร้อมใช้งานสำหรับการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="ebd49-140">If one or more data sources aren't added to the gateway, you won't see the gateway as available for scheduled refresh.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ebd49-141">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="ebd49-141">Next steps</span></span>

* [<span data-ttu-id="ebd49-142">การแก้ไขปัญหาเกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="ebd49-142">Troubleshooting the on-premises data gateway</span></span>](/data-integration/gateway/service-gateway-tshoot)
* [<span data-ttu-id="ebd49-143">แก้ไขปัญหาเกตเวย์-Power BI</span><span class="sxs-lookup"><span data-stu-id="ebd49-143">Troubleshoot gateways - Power BI</span></span>](service-gateway-onprem-tshoot.md)

<span data-ttu-id="ebd49-144">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="ebd49-144">More questions?</span></span> <span data-ttu-id="ebd49-145">ลองไปที่ [ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="ebd49-145">Try the [Power BI Community](https://community.powerbi.com/).</span></span>
