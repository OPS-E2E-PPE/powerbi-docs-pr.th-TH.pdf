---
title: จัดการแหล่งข้อมูลของคุณ - SAP HANA
description: วิธีการจัดการเกตเวย์ข้อมูลภายในองค์กร และแหล่งข้อมูลของเกตเวย์นั้นๆ บทความนี้มีไว้สำหรับ SAP HANA โดยเฉพาะ
author: arthiriyer
ms.author: arthii
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-gateways
ms.topic: how-to
ms.date: 07/16/2019
LocalizationGroup: Gateways
ms.openlocfilehash: e06f990c7b14cd27b182ebfd6bec2bba9741c99d
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96402719"
---
# <a name="manage-your-data-source---sap-hana"></a><span data-ttu-id="9bf46-104">จัดการแหล่งข้อมูลของคุณ - SAP HANA</span><span class="sxs-lookup"><span data-stu-id="9bf46-104">Manage your data source - SAP HANA</span></span>

[!INCLUDE [gateway-rewrite](../includes/gateway-rewrite.md)]

<span data-ttu-id="9bf46-105">หลังจากคุณ[ติดตั้งเกตเวย์ข้อมูลภายในองค์กรแล้ว](/data-integration/gateway/service-gateway-install) คุณจะต้อง[เพิ่มแหล่งข้อมูล](service-gateway-data-sources.md#add-a-data-source)ที่สามารถใช้ได้กับเกตเวย์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="9bf46-105">After you [install the on-premises data gateway](/data-integration/gateway/service-gateway-install), you need to [add data sources](service-gateway-data-sources.md#add-a-data-source) that can be used with the gateway.</span></span> <span data-ttu-id="9bf46-106">บทความนี้จะดูวิธีการทำงานกับเกตเวย์และแหล่งข้อมูล SAP HANA ที่ใช้สำหรับการรีเฟรชตามกำหนดการหรือสำหรับ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="9bf46-106">This article looks at how to work with gateways and SAP HANA data sources that are used either for scheduled refresh or for DirectQuery.</span></span>

## <a name="add-a-data-source"></a><span data-ttu-id="9bf46-107">เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9bf46-107">Add a data source</span></span>

<span data-ttu-id="9bf46-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเพิ่มแหล่งข้อมูล ให้ดู[เพิ่มแหล่งข้อมูล](service-gateway-data-sources.md#add-a-data-source)</span><span class="sxs-lookup"><span data-stu-id="9bf46-108">For more information about how to add a data source, see [Add a data source](service-gateway-data-sources.md#add-a-data-source).</span></span> <span data-ttu-id="9bf46-109">ภายใต้ **ชนิดแหล่งข้อมูล** เลือก  **SAP HANA**</span><span class="sxs-lookup"><span data-stu-id="9bf46-109">Under **Data Source Type**, select **SAP HANA**.</span></span>

![เพิ่มแหล่งข้อมูล SAP HANA](media/service-gateway-enterprise-manage-sap/datasourcesettings2-sap.png)

<span data-ttu-id="9bf46-111">หลังจากที่คุณเลือกชนิดแหล่งข้อมูล SAP HANA ให้กรอกข้อมูลลงใน **เซิร์ฟเวอร์** **ชื่อผู้ใช้** และ **รหัสผ่าน** สำหรับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9bf46-111">After you select the SAP HANA data source type, fill in the **Server**, **Username**, and **Password** information for the data source.</span></span>

> [!NOTE]
> <span data-ttu-id="9bf46-112">คิวรีทั้งหมดไปยังแหล่งข้อมูลจะทำงานโดยใช้ข้อมูลประจำตัวเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="9bf46-112">All queries to the data source will run using these credentials.</span></span> <span data-ttu-id="9bf46-113">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการจัดเก็บข้อมูลประจำตัว ให้ดู [การจัดเก็บข้อมูลประจำตัวที่เข้ารหัสไว้ในระบบคลาวด์](service-gateway-data-sources.md#store-encrypted-credentials-in-the-cloud)</span><span class="sxs-lookup"><span data-stu-id="9bf46-113">To learn more about how credentials are stored, see [Store encrypted credentials in the cloud](service-gateway-data-sources.md#store-encrypted-credentials-in-the-cloud).</span></span>

![การกรอกข้อมูลในการตั้งค่าแหล่งข้อมูล](media/service-gateway-enterprise-manage-sap/datasourcesettings3-sap.png)

<span data-ttu-id="9bf46-115">หลังจากที่คุณกรอกข้อมูลทุกอย่างแล้ว ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9bf46-115">After you fill in everything, select **Add**.</span></span> <span data-ttu-id="9bf46-116">คุณสามารถใช้แหล่งข้อมูลนี้สำหรับการรีเฟรชตามกำหนดการหรือ DirectQuery เทียบกับเซิร์ฟเวอร์ SAP HANA ที่อยู่ภายในองค์กรได้</span><span class="sxs-lookup"><span data-stu-id="9bf46-116">You can now use this data source for scheduled refresh or DirectQuery against an SAP HANA server that is on-premises.</span></span> <span data-ttu-id="9bf46-117">คุณจะเห็น *การเชื่อมต่อสำเร็จ* หากการดำเนินการเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="9bf46-117">You see *Connection Successful* if it succeeded.</span></span>

![การแสดงสถานะการเชื่อมต่อ](media/service-gateway-enterprise-manage-sap/datasourcesettings4.png)

### <a name="advanced-settings"></a><span data-ttu-id="9bf46-119">การตั้งค่าขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="9bf46-119">Advanced settings</span></span>

<span data-ttu-id="9bf46-120">อีกทางหนึ่งคือคุณสามารถกำหนดค่าระดับความเป็นส่วนตัวให้กับแหล่งข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="9bf46-120">Optionally, you can configure the privacy level for your data source.</span></span> <span data-ttu-id="9bf46-121">การตั้งค่านี้จะช่วยควบคุมวิธีการรวมข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="9bf46-121">This setting controls how data can be combined.</span></span> <span data-ttu-id="9bf46-122">ซึ่งใช้ได้เฉพาะกับการรีเฟรชตามกำหนดการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9bf46-122">It's only used for scheduled refresh.</span></span> <span data-ttu-id="9bf46-123">การตั้งค่าระดับความเป็นส่วนตัวจะไม่นำไปใช้กับ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="9bf46-123">The privacy-level setting doesn't apply to DirectQuery.</span></span> <span data-ttu-id="9bf46-124">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับระดับความเป็นส่วนตัวสำหรับแหล่งข้อมูลของคุณ ให้ดู [ระดับความเป็นส่วนตัว (Power Query)](https://support.office.com/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540)</span><span class="sxs-lookup"><span data-stu-id="9bf46-124">To learn more about privacy levels for your data source, see [Privacy levels (Power Query)](https://support.office.com/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540).</span></span>

![การตั้งค่าระดับความเป็นส่วนตัว](media/service-gateway-enterprise-manage-sap/datasourcesettings9.png)

## <a name="use-the-data-source"></a><span data-ttu-id="9bf46-126">ใช้แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9bf46-126">Use the data source</span></span>

<span data-ttu-id="9bf46-127">หลังจากที่คุณสร้างแหล่งข้อมูล รายการนี้จะพร้อมใช้งานเมื่อต้องใช้ทั้งกับการเชื่อมต่อ DirectQuery หรือการเชื่อมต่อสดผ่านการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="9bf46-127">After you create the data source, it's available to use with either DirectQuery connections or through scheduled refresh.</span></span>

> [!NOTE]
> <span data-ttu-id="9bf46-128">ชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูลจะต้องตรงกับ Power BI Desktop และแหล่งข้อมูลภายในเกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="9bf46-128">The server and database names must match between Power BI Desktop and the data source within the on-premises data gateway.</span></span>

<span data-ttu-id="9bf46-129">การเชื่อมโยงระหว่างชุดข้อมูลของคุณและแหล่งข้อมูลภายในเกตเวย์จะเป็นไปตามชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="9bf46-129">The link between your dataset and the data source within the gateway is based on your server name and database name.</span></span> <span data-ttu-id="9bf46-130">ชื่อเหล่านี้ต้องตรงกัน</span><span class="sxs-lookup"><span data-stu-id="9bf46-130">These names must match.</span></span> <span data-ttu-id="9bf46-131">ตัวอย่างเช่น ถ้าคุณใส่ที่อยู่ IP สำหรับชื่อเซิร์ฟเวอร์ภายใน Power BI Desktop คุณต้องใช้ที่อยู่ IP สำหรับแหล่งข้อมูลภายในการกำหนดค่าเกตเวย์ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="9bf46-131">For example, if you supply an IP address for the server name within Power BI Desktop, you must use the IP address for the data source within the gateway configuration.</span></span> <span data-ttu-id="9bf46-132">ถ้าคุณใช้ *SERVER\INSTANCE* ใน Power BI Desktop คุณต้องใช้ภายในแหล่งข้อมูลที่กำหนดค่าไว้สำหรับเกตเวย์ดังกล่าวด้วย</span><span class="sxs-lookup"><span data-stu-id="9bf46-132">If you use *SERVER\INSTANCE* in Power BI Desktop, you also must use it within the data source configured for the gateway.</span></span>

<span data-ttu-id="9bf46-133">ข้อกำหนดนี้เป็นกรณีสำหรับทั้ง DirectQuery และการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="9bf46-133">This requirement is the case for both DirectQuery and scheduled refresh.</span></span>

### <a name="use-the-data-source-with-directquery-connections"></a><span data-ttu-id="9bf46-134">ใช้แหล่งข้อมูลที่มีการเชื่อมต่อกับ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="9bf46-134">Use the data source with DirectQuery connections</span></span>

<span data-ttu-id="9bf46-135">ตรวจสอบให้แน่ใจว่าชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูลตรงกันระหว่าง Power BI Desktop และแหล่งข้อมูลที่กำหนดค่าไว้สำหรับเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="9bf46-135">Make sure that the server and database names match between Power BI Desktop and the configured data source for the gateway.</span></span> <span data-ttu-id="9bf46-136">คุณยังต้องตรวจสอบให้แน่ใจอีกว่า ผู้ใช้ของคุณแสดงอยู่ในแท็บ **ผู้ใช้** ของแหล่งข้อมูลเพื่อเผยแพร่ชุดข้อมูล DirectQuery</span><span class="sxs-lookup"><span data-stu-id="9bf46-136">You also need to make sure your user is listed in the **Users** tab of the data source to publish DirectQuery datasets.</span></span> <span data-ttu-id="9bf46-137">ตัวเลือกสำหรับ DirectQuery จะเกิดขึ้นภายใน Power BI Desktop ตอนที่คุณนำเข้าข้อมูลครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="9bf46-137">The selection for DirectQuery occurs within Power BI Desktop when you first import data.</span></span> <span data-ttu-id="9bf46-138">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้งาน DirectQuery โปรดดู [ใช้ DirectQuery ใน Power BI Desktop](desktop-use-directquery.md)</span><span class="sxs-lookup"><span data-stu-id="9bf46-138">For more information about how to use DirectQuery, see [Use DirectQuery in Power BI Desktop](desktop-use-directquery.md).</span></span>

<span data-ttu-id="9bf46-139">หลังจากที่คุณเผยแพร่ชุดข้อมูลจาก Power BI Desktop หรือ **รับข้อมูล** รายงานของคุณควรเริ่มการทำงาน</span><span class="sxs-lookup"><span data-stu-id="9bf46-139">After you publish, either from Power BI Desktop or **Get Data**, your reports should start to work.</span></span> <span data-ttu-id="9bf46-140">ซึ่งอาจจะใช้เวลาหลายนาทีเพื่อให้การเชื่อมต่อสามารถใช้งานได้ หลังจากคุณสร้างแหล่งข้อมูลภายในเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="9bf46-140">It might take several minutes after you create the data source within the gateway for the connection to be usable.</span></span>

### <a name="use-the-data-source-with-scheduled-refresh"></a><span data-ttu-id="9bf46-141">ใช้แหล่งข้อมูลที่มีการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="9bf46-141">Use the data source with scheduled refresh</span></span>

<span data-ttu-id="9bf46-142">ถ้าคุณอยู่ในแท็บ **ผู้ใช้** ของแหล่งข้อมูลที่กำหนดค่าไว้ภายในเกตเวย์ และชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูลตรงกัน คุณจะเห็นเกตเวย์เป็นตัวเลือกเพื่อใช้กับการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="9bf46-142">If you're listed in the **Users** tab of the data source configured within the gateway and the server name and database name match, you see the gateway as an option to use with scheduled refresh.</span></span>

![การแสดงรายชื่อผู้ใช้](media/service-gateway-enterprise-manage-sap/powerbi-gateway-enterprise-schedule-refresh.png)

## <a name="next-steps"></a><span data-ttu-id="9bf46-144">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="9bf46-144">Next steps</span></span>

* [<span data-ttu-id="9bf46-145">การแก้ไขปัญหาเกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="9bf46-145">Troubleshooting the on-premises data gateway</span></span>](/data-integration/gateway/service-gateway-tshoot)
* [<span data-ttu-id="9bf46-146">แก้ไขปัญหาเกตเวย์-Power BI</span><span class="sxs-lookup"><span data-stu-id="9bf46-146">Troubleshoot gateways - Power BI</span></span>](service-gateway-onprem-tshoot.md) 

<span data-ttu-id="9bf46-147">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="9bf46-147">More questions?</span></span> <span data-ttu-id="9bf46-148">ลองถาม[ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="9bf46-148">Try asking the [Power BI Community](https://community.powerbi.com/).</span></span>
