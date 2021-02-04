---
title: จัดการแหล่งข้อมูลของคุณ - SQL
description: วิธีการจัดการเกตเวย์ข้อมูลภายในองค์กร และข้อมูลแหล่งข้อมูล SQL Server ที่เป็นของเกตเวย์นั้น ๆ
author: arthiriyer
ms.author: arthii
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-gateways
ms.topic: how-to
ms.date: 07/15/2019
LocalizationGroup: Gateways
ms.openlocfilehash: 513b5b509328641e2c9f4965741b92939526aee1
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96402420"
---
# <a name="manage-your-data-source---sql-server"></a><span data-ttu-id="d9519-103">จัดการแหล่งข้อมูลของคุณ - SQL Server</span><span class="sxs-lookup"><span data-stu-id="d9519-103">Manage your data source - SQL Server</span></span>

[!INCLUDE [gateway-rewrite](../includes/gateway-rewrite.md)]

<span data-ttu-id="d9519-104">หลังจากคุณ[ติดตั้งเกตเวย์ข้อมูลภายในองค์กรแล้ว](/data-integration/gateway/service-gateway-install) คุณสามารถ[เพิ่มแหล่งข้อมูล](service-gateway-data-sources.md#add-a-data-source)ที่สามารถใช้ได้กับเกตเวย์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="d9519-104">After you [install the on-premises data gateway](/data-integration/gateway/service-gateway-install), you can [add data sources](service-gateway-data-sources.md#add-a-data-source) that can be used with the gateway.</span></span> <span data-ttu-id="d9519-105">บทความนี้จะดูวิธีการทำงานกับเกตเวย์และแหล่งข้อมูล SQL Server ที่ใช้สำหรับการรีเฟรชตามกำหนดการหรือสำหรับ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="d9519-105">This article looks at how to work with gateways and SQL Server data sources that are used either for scheduled refresh or for DirectQuery.</span></span>

## <a name="add-a-data-source"></a><span data-ttu-id="d9519-106">เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d9519-106">Add a data source</span></span>

<span data-ttu-id="d9519-107">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเพิ่มแหล่งข้อมูล ให้ดู[เพิ่มแหล่งข้อมูล](service-gateway-data-sources.md#add-a-data-source)</span><span class="sxs-lookup"><span data-stu-id="d9519-107">For more information about how to add a data source, see [Add a data source](service-gateway-data-sources.md#add-a-data-source).</span></span> <span data-ttu-id="d9519-108">ภายใต้ **ชนิดแหล่งข้อมูล** ให้เลือก **SQL Server**</span><span class="sxs-lookup"><span data-stu-id="d9519-108">Under **Data Source Type**, select **SQL Server**.</span></span>

![เลือกแหล่งข้อมูล SQL Server:](media/service-gateway-enterprise-manage-sql/datasourcesettings2.png)

> [!NOTE]
> <span data-ttu-id="d9519-110">เมื่อคุณใช้ DirectQuery เกตเวย์สนับสนุนเฉพาะ **SQL Server 2012 SP1** และเวอร์ชันถัดมา</span><span class="sxs-lookup"><span data-stu-id="d9519-110">When you use DirectQuery, the gateway supports only **SQL Server 2012 SP1** and subsequent versions.</span></span>

<span data-ttu-id="d9519-111">จากนั้นให้กรอกข้อมูลเกี่ยวกับแหล่งข้อมูล ซึ่งประกอบด้วย **เซิร์ฟเวอร์** และ **ฐานข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="d9519-111">Then fill in the information for the data source, which includes **Server** and **Database**.</span></span> 

<span data-ttu-id="d9519-112">ภายใต้ **วิธีการรับรองความถูกต้อง** ให้เลือก **Windows** หรือ **พื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="d9519-112">Under **Authentication Method**, choose either **Windows** or **Basic**.</span></span> <span data-ttu-id="d9519-113">เลือก **พื้นฐาน** ถ้าคุณวางแผนที่จะใช้การรับรองความถูกต้องของ SQL แทนการรับรองความถูกต้องของ Windows</span><span class="sxs-lookup"><span data-stu-id="d9519-113">Choose **Basic** if you plan to use SQL authentication instead of Windows authentication.</span></span> <span data-ttu-id="d9519-114">จากนั้นป้อนข้อมูลประจำตัวที่จะใช้สำหรับแหล่งข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="d9519-114">Then enter the credentials to be used for this data source.</span></span>

> [!NOTE]
> <span data-ttu-id="d9519-115">คิวรีทั้งหมดที่ไปยังแหล่งข้อมูลจะทำงานโดยใช้ข้อมูลประจำตัวเหล่านี้ เว้นแต่ว่า single sign-on (SSO) ของ Kerberos จะถูกกำหนดค่าและเปิดใช้งานสำหรับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d9519-115">All queries to the data source will run using these credentials, unless Kerberos single sign-on (SSO) is configured and enabled for the data source.</span></span> <span data-ttu-id="d9519-116">SSO จะทำให้ชุดข้อมูลนำเข้าใช้ข้อมูลประจำตัวที่จัดเก็บไว้ แต่ชุดข้อมูล DirectQuery จะใช้ผู้ใช้ Power BI ปัจจุบันเพื่อดำเนินการคิวรีโดยใช้ SSO</span><span class="sxs-lookup"><span data-stu-id="d9519-116">With SSO, import datasets use the stored credentials, but DirectQuery datasets use the current Power BI user to execute the queries using SSO.</span></span> <span data-ttu-id="d9519-117">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการจัดเก็บข้อมูลประจำตัว ให้ดู [การจัดเก็บข้อมูลประจำตัวที่เข้ารหัสไว้ในระบบคลาวด์](service-gateway-data-sources.md#store-encrypted-credentials-in-the-cloud)</span><span class="sxs-lookup"><span data-stu-id="d9519-117">To learn more about how credentials are stored, see [Store encrypted credentials in the cloud](service-gateway-data-sources.md#store-encrypted-credentials-in-the-cloud).</span></span> <span data-ttu-id="d9519-118">หรือดูบทความที่อธิบายวิธีการ [ใช้ Kerberos สำหรับ single sign-on (SSO) จาก Power BI ไปยังแหล่งข้อมูลภายในองค์กร](service-gateway-sso-kerberos.md)</span><span class="sxs-lookup"><span data-stu-id="d9519-118">Or, see the article that describes how to [use Kerberos for single sign-on (SSO) from Power BI to on-premises data sources](service-gateway-sso-kerberos.md).</span></span>

![การกรอกข้อมูลในการตั้งค่าแหล่งข้อมูล](media/service-gateway-enterprise-manage-sql/datasourcesettings3.png)

<span data-ttu-id="d9519-120">หลังจากที่คุณกรอกข้อมูลทุกอย่างแล้ว ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="d9519-120">After you fill in everything, select **Add**.</span></span> <span data-ttu-id="d9519-121">คุณสามารถใช้แหล่งข้อมูลนี้สำหรับการรีเฟรชตามกำหนดการหรือ DirectQuery เทียบกับ SQL Server ที่อยู่ภายในองค์กรได้</span><span class="sxs-lookup"><span data-stu-id="d9519-121">You can now use this data source for scheduled refresh or DirectQuery against a SQL Server that's on-premises.</span></span> <span data-ttu-id="d9519-122">คุณจะเห็น *การเชื่อมต่อสำเร็จ* หากการดำเนินการเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="d9519-122">You see *Connection Successful* if it succeeded.</span></span>

![การแสดงสถานะการเชื่อมต่อ](media/service-gateway-enterprise-manage-sql/datasourcesettings4.png)

### <a name="advanced-settings"></a><span data-ttu-id="d9519-124">การตั้งค่าขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="d9519-124">Advanced settings</span></span>

<span data-ttu-id="d9519-125">อีกทางหนึ่งคือคุณสามารถกำหนดค่าระดับความเป็นส่วนตัวให้กับแหล่งข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="d9519-125">Optionally, you can configure the privacy level for your data source.</span></span> <span data-ttu-id="d9519-126">การตั้งค่านี้จะช่วยควบคุมวิธีการรวมข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="d9519-126">This setting controls how data can be combined.</span></span> <span data-ttu-id="d9519-127">ซึ่งใช้ได้เฉพาะกับการรีเฟรชตามกำหนดการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d9519-127">It's only used for scheduled refresh.</span></span> <span data-ttu-id="d9519-128">การตั้งค่าระดับความเป็นส่วนตัวจะไม่นำไปใช้กับ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="d9519-128">The privacy-level setting doesn't apply to DirectQuery.</span></span> <span data-ttu-id="d9519-129">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับระดับความเป็นส่วนตัวสำหรับแหล่งข้อมูลของคุณ ให้ดู [ระดับความเป็นส่วนตัว (Power Query)](https://support.office.com/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540)</span><span class="sxs-lookup"><span data-stu-id="d9519-129">To learn more about privacy levels for your data source, see [Privacy levels (Power Query)](https://support.office.com/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540).</span></span>

![การตั้งค่าระดับความเป็นส่วนตัว](media/service-gateway-enterprise-manage-sql/datasourcesettings9.png)

## <a name="use-the-data-source"></a><span data-ttu-id="d9519-131">ใช้แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d9519-131">Use the data source</span></span>

<span data-ttu-id="d9519-132">หลังจากที่คุณสร้างแหล่งข้อมูล รายการนี้จะพร้อมใช้งานเมื่อต้องใช้ทั้งกับการเชื่อมต่อ DirectQuery หรือการเชื่อมต่อสดผ่านการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="d9519-132">After you create the data source, it's available to use with either DirectQuery connections or through scheduled refresh.</span></span>

> [!NOTE]
> <span data-ttu-id="d9519-133">ชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูลจะต้องตรงกับ Power BI Desktop และแหล่งข้อมูลภายในเกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="d9519-133">The server and database names must match between Power BI Desktop and the data source within the on-premises data gateway.</span></span>

<span data-ttu-id="d9519-134">การเชื่อมโยงระหว่างชุดข้อมูลของคุณและแหล่งข้อมูลภายในเกตเวย์จะเป็นไปตามชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="d9519-134">The link between your dataset and the data source within the gateway is based on your server name and database name.</span></span> <span data-ttu-id="d9519-135">ชื่อเหล่านี้ต้องตรงกัน</span><span class="sxs-lookup"><span data-stu-id="d9519-135">These names must match.</span></span> <span data-ttu-id="d9519-136">ตัวอย่างเช่น ถ้าคุณใส่ที่อยู่ IP สำหรับชื่อเซิร์ฟเวอร์ภายใน Power BI Desktop คุณต้องใช้ที่อยู่ IP สำหรับแหล่งข้อมูลภายในการกำหนดค่าเกตเวย์ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="d9519-136">For example, if you supply an IP address for the server name within Power BI Desktop, you must use the IP address for the data source within the gateway configuration.</span></span> <span data-ttu-id="d9519-137">ถ้าคุณใช้ *SERVER\INSTANCE* ใน Power BI Desktop คุณต้องใช้ภายในแหล่งข้อมูลที่กำหนดค่าไว้สำหรับเกตเวย์ดังกล่าวด้วย</span><span class="sxs-lookup"><span data-stu-id="d9519-137">If you use *SERVER\INSTANCE* in Power BI Desktop, you must use it within the data source configured for the gateway.</span></span>

<span data-ttu-id="d9519-138">ข้อกำหนดนี้เป็นกรณีสำหรับทั้ง DirectQuery และการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="d9519-138">This requirement is the case for both DirectQuery and scheduled refresh.</span></span>

### <a name="use-the-data-source-with-directquery-connections"></a><span data-ttu-id="d9519-139">ใช้แหล่งข้อมูลที่มีการเชื่อมต่อกับ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="d9519-139">Use the data source with DirectQuery connections</span></span>

<span data-ttu-id="d9519-140">ตรวจสอบให้แน่ใจว่าชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูลตรงกันระหว่าง Power BI Desktop และแหล่งข้อมูลที่กำหนดค่าไว้สำหรับเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="d9519-140">Make sure that the server and database names match between Power BI Desktop and the configured data source for the gateway.</span></span> <span data-ttu-id="d9519-141">คุณยังต้องตรวจสอบให้แน่ใจอีกว่า ผู้ใช้ของคุณแสดงอยู่ในแท็บ **ผู้ใช้** ของแหล่งข้อมูลเพื่อเผยแพร่ชุดข้อมูล DirectQuery</span><span class="sxs-lookup"><span data-stu-id="d9519-141">You also need to make sure your user is listed in the **Users** tab of the data source to publish DirectQuery datasets.</span></span> <span data-ttu-id="d9519-142">ตัวเลือกสำหรับ DirectQuery จะเกิดขึ้นภายใน Power BI Desktop ตอนที่คุณนำเข้าข้อมูลครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="d9519-142">The selection for DirectQuery occurs within Power BI Desktop when you first import data.</span></span> <span data-ttu-id="d9519-143">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้งาน DirectQuery โปรดดู [ใช้ DirectQuery ใน Power BI Desktop](desktop-use-directquery.md)</span><span class="sxs-lookup"><span data-stu-id="d9519-143">For more information about how to use DirectQuery, see [Use DirectQuery in Power BI Desktop](desktop-use-directquery.md).</span></span>

<span data-ttu-id="d9519-144">หลังจากที่คุณเผยแพร่ชุดข้อมูลจาก Power BI Desktop หรือ **รับข้อมูล** รายงานของคุณควรเริ่มการทำงาน</span><span class="sxs-lookup"><span data-stu-id="d9519-144">After you publish, either from Power BI Desktop or **Get Data**, your reports should start to work.</span></span> <span data-ttu-id="d9519-145">ซึ่งอาจจะใช้เวลาหลายนาทีเพื่อให้การเชื่อมต่อสามารถใช้งานได้ หลังจากคุณสร้างแหล่งข้อมูลภายในเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="d9519-145">It might take several minutes after you create the data source within the gateway for the connection to be usable.</span></span>

### <a name="use-the-data-source-with-scheduled-refresh"></a><span data-ttu-id="d9519-146">ใช้แหล่งข้อมูลที่มีการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="d9519-146">Use the data source with scheduled refresh</span></span>

<span data-ttu-id="d9519-147">ถ้าคุณอยู่ในแท็บ **ผู้ใช้** ของแหล่งข้อมูลที่กำหนดค่าไว้ภายในเกตเวย์ และชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูลตรงกัน คุณจะเห็นเกตเวย์เป็นตัวเลือกเพื่อใช้กับการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="d9519-147">If you're listed in the **Users** tab of the data source configured within the gateway and the server name and database name match, you see the gateway as an option to use with scheduled refresh.</span></span>

![การแสดงรายชื่อผู้ใช้](media/service-gateway-enterprise-manage-sql/powerbi-gateway-enterprise-schedule-refresh.png)

## <a name="next-steps"></a><span data-ttu-id="d9519-149">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d9519-149">Next steps</span></span>

* [<span data-ttu-id="d9519-150">เชื่อมต่อกับข้อมูลภายในองค์กรใน SQL Server</span><span class="sxs-lookup"><span data-stu-id="d9519-150">Connect to on-premises data in SQL Server</span></span>](service-gateway-sql-tutorial.md)
* [<span data-ttu-id="d9519-151">การแก้ไขปัญหาเกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="d9519-151">Troubleshooting the on-premises data gateway</span></span>](/data-integration/gateway/service-gateway-tshoot)
* [<span data-ttu-id="d9519-152">แก้ไขปัญหาเกตเวย์-Power BI</span><span class="sxs-lookup"><span data-stu-id="d9519-152">Troubleshoot gateways - Power BI</span></span>](service-gateway-onprem-tshoot.md)
* [<span data-ttu-id="d9519-153">ใช้ Kerberos สำหรับลงชื่อเข้าใช้ครั้งเดียว (SSO) จาก Power BI ไปยังแหล่งข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="d9519-153">Use Kerberos for single sign-on (SSO) from Power BI to on-premises data sources</span></span>](service-gateway-sso-kerberos.md)

<span data-ttu-id="d9519-154">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d9519-154">More questions?</span></span> <span data-ttu-id="d9519-155">ลองถาม[ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="d9519-155">Try asking the [Power BI Community](https://community.powerbi.com/).</span></span>
