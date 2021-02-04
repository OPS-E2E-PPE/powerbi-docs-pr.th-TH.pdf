---
title: เพิ่มหรือลบแหล่งข้อมูลเกตเวย์
description: เรียนรู้วิธีการเพิ่มแหล่งข้อมูลไปยังเกตเวย์ภายในองค์กรใน Power BI
author: arthiriyer
ms.author: arthii
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-gateways
ms.topic: how-to
ms.date: 11/03/2020
ms.custom: seodec18
LocalizationGroup: Gateways
ms.openlocfilehash: 55cdbfbe0572986de455ddb05c342af9e019de42
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96402857"
---
# <a name="add-or-remove-a-gateway-data-source"></a><span data-ttu-id="8a713-103">เพิ่มหรือลบแหล่งข้อมูลเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="8a713-103">Add or remove a gateway data source</span></span>

[!INCLUDE [gateway-rewrite](../includes/gateway-rewrite.md)]

<span data-ttu-id="8a713-104">Power BI สนับสนุน[แหล่งข้อมูลภายในองค์กร](power-bi-data-sources.md)มากมาย ซึ่งแต่ละชนิดข้อกำหนดของตนเอง</span><span class="sxs-lookup"><span data-stu-id="8a713-104">Power BI supports many [on-premises data sources](power-bi-data-sources.md), and each has its own requirements.</span></span> <span data-ttu-id="8a713-105">สามารถใช้เกตเวย์สำหรับแหล่งข้อมูลเดียวหรือหลายแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a713-105">A gateway can be used for a single data source or multiple data sources.</span></span> <span data-ttu-id="8a713-106">สำหรับตัวอย่างนี้ เราจะแสดงให้คุณเห็นวิธีการเพิ่ม SQL Server เป็นแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a713-106">For this example, we show you how to add SQL Server as a data source.</span></span> <span data-ttu-id="8a713-107">ขั้นตอนก็จะคล้ายกับแหล่งข้อมูลอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="8a713-107">The steps are similar for other data sources.</span></span>

<span data-ttu-id="8a713-108">การดำเนินการจัดการแหล่งข้อมูลส่วนใหญ่สามารถดำเนินการได้โดยใช้ API ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="8a713-108">Most data sources management operations can be performed by using APIs as well.</span></span> <span data-ttu-id="8a713-109">สำหรับข้อมูลเพิ่มเติม ดู[Rest APIs (เกตเวย์)](/rest/api/power-bi/gateways)</span><span class="sxs-lookup"><span data-stu-id="8a713-109">For more information, see [REST APIs (Gateways)](/rest/api/power-bi/gateways).</span></span>

<span data-ttu-id="8a713-110">หากคุณยังไม่ได้ติดตั้งเกตเวย์ โปรดดูที่[ติดตั้งเกตเวย์ข้อมูลภายในองค์กร](/data-integration/gateway/service-gateway-install)เพื่อเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8a713-110">If you don't have a gateway installed yet, see [Install an on-premises data gateway](/data-integration/gateway/service-gateway-install) to get started.</span></span>

## <a name="add-a-data-source"></a><span data-ttu-id="8a713-111">เพิ่มแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a713-111">Add a data source</span></span>

1. <span data-ttu-id="8a713-112">จากส่วนหัวของหน้าในบริการ Power BI ให้เลือก **การตั้งค่า**![ไอคอนรูปเฟืองการตั้งค่า](media/service-gateway-data-sources/icon-gear.png) > **จัดการเกตเวย์**</span><span class="sxs-lookup"><span data-stu-id="8a713-112">From the page header in the Power BI service, select  **Settings** ![Settings gear icon](media/service-gateway-data-sources/icon-gear.png) > **Manage gateways**.</span></span>

    ![จัดการเกตเวย์](media/service-gateway-data-sources/manage-gateways.png)

2. <span data-ttu-id="8a713-114">เลือกเกตเวย์แล้วเลือก **เพิ่มแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="8a713-114">Select a gateway and then select **Add data source**.</span></span> <span data-ttu-id="8a713-115">คุณสามารถเลือกข้อความส่วนหัว **เพิ่มแหล่งข้อมูล** หรือวางเคอร์เซอร์ของคุณถัดจากรายการเกตเวย์เพื่อแสดงเมนูตัวเลือกเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8a713-115">You can select the header text **ADD DATA SOURCE** or hover your cursor next to the gateway entry to reveal the more options menu.</span></span>

    ![เพิ่มแหล่งข้อมูล](media/service-gateway-data-sources/add-data-source.png)

3. <span data-ttu-id="8a713-117">กำหนดชื่อให้กับแหล่งข้อมูลของคุณ จากนั้นเลือก **ชนิดแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="8a713-117">Assign a name to your data source, then select the **Data Source Type**.</span></span> <span data-ttu-id="8a713-118">ในตัวอย่างนี้ เราจะเลือก SQL Server</span><span class="sxs-lookup"><span data-stu-id="8a713-118">In this example, we'll choose SQL Server.</span></span>

    ![เลือก SQL Server](media/service-gateway-data-sources/select-sql-server.png)

4. <span data-ttu-id="8a713-120">ป้อนข้อมูลเกี่ยวกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a713-120">Enter information about the data source.</span></span> <span data-ttu-id="8a713-121">สำหรับ SQL Server ให้ระบุ **เซิร์ฟเวอร์** และ **ฐานข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="8a713-121">For SQL Server, provide the **Server** and **Database**.</span></span>

    ![การตั้งค่าแหล่งข้อมูล](media/service-gateway-data-sources/data-source-settings.png)

5. <span data-ttu-id="8a713-123">เลือก **วิธีการรับรองความถูกต้อง** เพื่อใช้เมื่อเชื่อมต่อกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a713-123">Select an **Authentication Method** to use when connecting to the data source.</span></span> <span data-ttu-id="8a713-124">สำหรับ SQL Server ให้เลือก **Windows** หรือ **Basic** (การรับรองความถูกต้อง SQL)</span><span class="sxs-lookup"><span data-stu-id="8a713-124">For SQL Server, choose **Windows** or **Basic** (SQL Authentication).</span></span> <span data-ttu-id="8a713-125">ใส่ข้อมูลประจำตัวสำหรับแหล่งข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="8a713-125">Enter the credentials for your data source.</span></span>

   :::image type="content" source="media/service-gateway-data-sources/basic-auth.png" alt-text="การตั้งค่าการรับรองความถูกต้องแบบ Basic":::

    > [!NOTE]
    > <span data-ttu-id="8a713-127">หากวิธีการรับรองความถูกต้องที่เลือกไว้คือ OAuth คิวรีใด ๆ ที่ใช้งานนานกว่านโยบายการหมดอายุโทเค็นของ OAuth อาจล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="8a713-127">If the selected authentication method is OAuth, any query that runs longer than the OAuth token expiration policy may fail.</span></span>

6. <span data-ttu-id="8a713-128">ภายใต้ **การตั้งค่าขั้นสูง** คุณสามารถกำหนดค่า [ลงชื่อเข้าระบบครั้งเดียว (SSO)](service-gateway-sso-overview.md) สำหรับแหล่งข้อมูลของคุณได้</span><span class="sxs-lookup"><span data-stu-id="8a713-128">Under **Advanced settings**, you could configure [Single Sign-On (SSO)](service-gateway-sso-overview.md) for your data source.</span></span> 

    ![การตั้งค่าขั้นสูง](media/service-gateway-data-sources/advanced-settings-02.png)

    <span data-ttu-id="8a713-130">คุณสามารถกำหนดค่า **ใช้ SSO ผ่าน Kerberos สำหรับคิวรีแบบ DirectQuery** หรือ **ใช้ SSO ผ่าน Kerberos สำหรับคิวรีแบบ DirectQuery และ Import** สำหรับรายงานที่ยึดตาม DirectQuery และ **ใช้ SSO ผ่าน Kerberos สำหรับคิวรีแบบ DirectQuery และ Import** สำหรับรายงานที่ยึดตามการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="8a713-130">You could either configure **Use SSO via Kerberos for DirectQuery queries**  or **Use SSO via Kerberos for DirectQuery And Import queries** for DirectQuery-based Reports and **Use SSO via Kerberos for DirectQuery And Import queries** for Refresh-based Reports.</span></span>

    <span data-ttu-id="8a713-131">ถ้าคุณใช้ **ใช้ SSO ผ่าน Kerberos สำหรับคิวรีแบบ DirectQuery** และใช้แหล่งข้อมูลนี้สำหรับรายงานที่ยึดตาม DirectQuery ซึ่งจะใช้ข้อมูลประจำตัวของผู้ใช้ที่ลงชื่อเข้าใช้บริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="8a713-131">If you use the **Use SSO via Kerberos for DirectQuery queries** and use this data source for a DirectQuery based Report, it will use the credentials of the user that signs in to the Power BI service.</span></span> <span data-ttu-id="8a713-132">สำหรับรายงานที่ยึดตามการรีเฟรช จะใช้ข้อมูลประจำตัวที่คุณป้อนในเขตข้อมูล **ชื่อผู้ใช้** และ **รหัสผ่าน**</span><span class="sxs-lookup"><span data-stu-id="8a713-132">For a Refresh-based Report, it will use the credentials that you enter in the **Username** and **Password** fields.</span></span>

    <span data-ttu-id="8a713-133">ถ้าคุณใช้ **ใช้ SSO ผ่าน Kerberos สำหรับคิวรีแบบ DirectQuery และ Import** คุณไม่จำเป็นต้องใส่ข้อมูลประจำตัวใดก็ตาม</span><span class="sxs-lookup"><span data-stu-id="8a713-133">When you use the **Use SSO via Kerberos for DirectQuery And Import queries**, you don't need to provide any credentials.</span></span> <span data-ttu-id="8a713-134">หากแหล่งข้อมูลนี้ใช้สำหรับรายงานที่ยึดตาม DirectQuery จะใช้ผู้ใช้ที่มีการแมปกับผู้ใช้ Active Directory (Azure) ที่ลงทะเบียนไว้ในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="8a713-134">If this data source is used for DirectQuery based Report, it will use the user that's mapped to the (Azure) Active Directory user that signs in to the Power BI service.</span></span>  <span data-ttu-id="8a713-135">สำหรับรายงานที่ยึดตามการรีเฟรช จะใช้บริบทความปลอดภัยของเจ้าของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a713-135">For a Refresh based Report, it will use the dataset owner's security context</span></span>

    > [!NOTE]
    ><span data-ttu-id="8a713-136">SSO สำหรับคิวรีนำเข้า จะพร้อมใช้งานสำหรับรายการแหล่งข้อมูล SSO โดยใช้ [การมอบหมายที่มีข้อจำกัดของ Kerberos](service-gateway-sso-kerberos.md) เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8a713-136">SSO for Import Queries is available only for the list of SSO data sources using [Kerberos constrained delegation](service-gateway-sso-kerberos.md).</span></span>

7. <span data-ttu-id="8a713-137">ภายใต้ **การตั้งค่าขั้นสูง** อาจกำหนดค่า [ระดับความเป็นส่วนตัว](https://support.office.com/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540) สำหรับแหล่งข้อมูลของคุณ (ไม่ใช้กับ [DirectQuery](desktop-directquery-about.md))</span><span class="sxs-lookup"><span data-stu-id="8a713-137">Under **Advanced settings**, optionally configure the [privacy level](https://support.office.com/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540) for your data source (doesn't apply to [DirectQuery](desktop-directquery-about.md)).</span></span>

    :::image type="content" source="media/service-gateway-data-sources/privacy-level.png" alt-text="การเลือกระดับความเป็นส่วนตัว":::

8. <span data-ttu-id="8a713-139">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="8a713-139">Select **Add**.</span></span> <span data-ttu-id="8a713-140">คุณจะเห็นข้อความ *การเชื่อมต่อเป็นที่สำเร็จ* ถ้ากระบวนการสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="8a713-140">You see *Connection Successful* if the process succeeds.</span></span>

    ![การเชื่อมต่อเป็นที่สำเร็จ](media/service-gateway-data-sources/connection-successful.png)

<span data-ttu-id="8a713-142">ตอนนี้คุณสามารถใช้แหล่งข้อมูลนี้เพื่อรวมข้อมูลจาก SQL Server ลงในแดชบอร์ดและรายงาน Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8a713-142">You can now use this data source to include data from SQL Server in your Power BI dashboards and reports.</span></span>

## <a name="remove-a-data-source"></a><span data-ttu-id="8a713-143">ลบแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a713-143">Remove a data source</span></span>

<span data-ttu-id="8a713-144">คุณสามารถลบแหล่งข้อมูลออกถ้าคุณไม่ใช้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="8a713-144">You can remove a data source if you no longer use it.</span></span> <span data-ttu-id="8a713-145">การลบแหล่งข้อมูลออกจะทำให้แดชบอร์ดและรายงานที่ขึ้นกับแหล่งข้อมูลนั้นไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="8a713-145">Removing a data source breaks any dashboards and reports that rely on that data source.</span></span>

<span data-ttu-id="8a713-146">หากต้องการลบแหล่งข้อมูล ให้ไปที่แหล่งข้อมูลและจากนั้นเลือก **ลบ** จากเมนูตัวเลือกเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8a713-146">To remove a data source, go to the data source and then select **Remove** from the more options menu.</span></span> <span data-ttu-id="8a713-147">เมนูตัวเลือกเพิ่มเติมจะปรากฏขึ้นเมื่อคุณวางเคอร์เซอร์ถัดจากชื่อแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a713-147">The more options menu appears when you hover your cursor next to the data source name.</span></span>

![ลบแหล่งข้อมูล](media/service-gateway-data-sources/remove-data-source.png)

## <a name="use-the-data-source-for-scheduled-refresh-or-directquery"></a><span data-ttu-id="8a713-149">ใช้แหล่งข้อมูลสำหรับการรีเฟรชตามกำหนดการหรือ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="8a713-149">Use the data source for scheduled refresh or DirectQuery</span></span>

<span data-ttu-id="8a713-150">หลังจากที่คุณสร้างแหล่งข้อมูล รายการนี้จะพร้อมใช้งานเมื่อต้องใช้ทั้งกับการเชื่อมต่อ DirectQuery หรือการเชื่อมต่อสดผ่านการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="8a713-150">After you create the data source, it's available to use with either DirectQuery connections or through scheduled refresh.</span></span> <span data-ttu-id="8a713-151">คุณสามารถเรียนรู้เพิ่มเติมเกี่ยวกับการตั้งค่าการรีเฟรชตามกำหนดเวลาได้ใน[กำหนดค่าการรีเฟรชตามกำหนดเวลา](refresh-scheduled-refresh.md)</span><span class="sxs-lookup"><span data-stu-id="8a713-151">You can learn more about setting up scheduled refresh in [Configure scheduled refresh](refresh-scheduled-refresh.md).</span></span>

> [!NOTE]
><span data-ttu-id="8a713-152">ชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูลจะต้องตรงกับ Power BI Desktop และแหล่งที่เพิ่มไปยังเกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="8a713-152">Server and database names must match between Power BI Desktop and the data source added to the on-premises data gateway.</span></span>

<span data-ttu-id="8a713-153">การเชื่อมโยงระหว่างชุดข้อมูลของคุณและแหล่งข้อมูลในเกตเวย์จะเป็นไปตามชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="8a713-153">The link between your dataset and the data source in the gateway is based on your server name and database name.</span></span> <span data-ttu-id="8a713-154">ชื่อเหล่านี้ต้องตรงกัน</span><span class="sxs-lookup"><span data-stu-id="8a713-154">These names must match.</span></span> <span data-ttu-id="8a713-155">ตัวอย่างเช่น ถ้าคุณใส่ที่อยู่ IP สำหรับชื่อเซิร์ฟเวอร์ ใน Power BI Desktop คุณต้องใช้ที่อยู่ IP สำหรับแหล่งข้อมูลในการกำหนดค่าเกตเวย์ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="8a713-155">For example, if you supply an IP address for the server name, in Power BI Desktop, you must use the IP address for the data source in the gateway configuration.</span></span> <span data-ttu-id="8a713-156">ถ้าคุณใช้ *SERVER\INSTANCE* ใน Power BI Desktop คุณต้องใช้ชื่อเดียวกันในแหล่งข้อมูลที่กำหนดค่าไว้สำหรับเกตเวย์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="8a713-156">If you use *SERVER\INSTANCE* in Power BI Desktop, you must use the same in the data source configured for the gateway.</span></span>

<span data-ttu-id="8a713-157">ถ้าคุณอยู่ในแท็บ **ผู้ใช้** ของแหล่งข้อมูลที่กำหนดค่าไว้ในเกตเวย์ และชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูลตรงกัน คุณจะเห็นเกตเวย์เป็นตัวเลือกเพื่อใช้กับการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="8a713-157">If you're listed in the **Users** tab of the data source configured in the gateway, and the server and database name match, you see the gateway as an option to use with scheduled refresh.</span></span>

![การเชื่อมต่อเกตเวย์](media/service-gateway-data-sources/gateway-connection.png)

> [!WARNING]
> <span data-ttu-id="8a713-159">ถ้าชุดข้อมูลของคุณประกอบด้วยแหล่งข้อมูลหลายแหล่ง คุณต้องเพิ่มแต่ละแหล่งข้อมูลในเกตเวย์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="8a713-159">If your dataset contains multiple data sources, each data source must be added in the gateway.</span></span> <span data-ttu-id="8a713-160">ถ้าไม่ได้เพิ่มแหล่งข้อมูลอย่างน้อยหนึ่งแหล่งเข้าไปในเกตเวย์ คุณจะไม่เห็นเกตเวย์ดังกล่าวเป็นสถานะพร้อมใช้งานสำหรับการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="8a713-160">If one or more data sources aren't added to the gateway, you won't see the gateway as available for scheduled refresh.</span></span>

### <a name="limitations"></a><span data-ttu-id="8a713-161">ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="8a713-161">Limitations</span></span>

<span data-ttu-id="8a713-162">OAuth เป็นเค้าร่างการรับรองความถูกต้องที่ได้รับการสนับสนุนเฉพาะสำหรับการเชื่อมต่อกับเกตเวย์ข้อมูลภายในองค์กรเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8a713-162">OAuth is a supported authentication scheme only for custom connectors with the on-premises data gateway.</span></span> <span data-ttu-id="8a713-163">คุณไม่สามารถเพิ่มแหล่งข้อมูลที่ต้องใช้ OAuth ได้</span><span class="sxs-lookup"><span data-stu-id="8a713-163">You can't add other data sources that require OAuth.</span></span> <span data-ttu-id="8a713-164">ถ้าชุดข้อมูลของคุณมีแหล่งข้อมูลที่ต้องมี OAuth และชุดข้อมูลนี้ไม่ใช่ตัวเชื่อมต่อแบบกำหนดเอง คุณจะไม่สามารถใช้เกตเวย์ดังกล่าวสำหรับการรีเฟรชตามกำหนดเวลาได้</span><span class="sxs-lookup"><span data-stu-id="8a713-164">If your dataset has a data source that requires OAuth and this data source isn't a custom connector, you can't use the gateway for scheduled refresh.</span></span>

## <a name="manage-users"></a><span data-ttu-id="8a713-165">จัดการผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="8a713-165">Manage users</span></span>

<span data-ttu-id="8a713-166">หลังจากที่คุณเพิ่มแหล่งข้อมูลให้กับเกตเวย์แล้ว คุณสามารถให้สิทธิการเข้าถึงแหล่งข้อมูลที่กำหนดแก่ผู้ใช้และกลุ่มความปลอดภัยที่เปิดใช้งานอีเมล (ไม่ใช่ทั้งเกตเวย์)</span><span class="sxs-lookup"><span data-stu-id="8a713-166">After you add a data source to a gateway, you give users and email-enabled security groups access to the specific data source (not the entire gateway).</span></span> <span data-ttu-id="8a713-167">รายการเข้าถึงสำหรับแหล่งข้อมูลจะควบคุมว่าใครสามารถเผยแพร่รายงานที่รวมข้อมูลจากแหล่งข้อมูลนั้นได้บ้าง</span><span class="sxs-lookup"><span data-stu-id="8a713-167">The access list for the data source controls only who is allowed to publish reports that include data from the data source.</span></span> <span data-ttu-id="8a713-168">เจ้าของรายงานสามารถสร้างแดชบอร์ด ชุดเนื้อหา และแอป จากนั้นแชร์รายการเหล่านั้นให้กับผู้ใช้รายอื่นได้</span><span class="sxs-lookup"><span data-stu-id="8a713-168">Report owners can create dashboards, content packs, and apps, and then share those items with other users.</span></span>

<span data-ttu-id="8a713-169">คุณยังสามารถให้ผู้ใช้และกลุ่มความปลอดภัย เข้าถึงเกตเวย์ในระดับผู้ดูแล</span><span class="sxs-lookup"><span data-stu-id="8a713-169">You can also give users and security groups administrative access to the gateway.</span></span>

> [!NOTE]
> <span data-ttu-id="8a713-170">ผู้ใช้ที่สามารถเข้าถึงแหล่งข้อมูลสามารถเชื่อมโยงชุดข้อมูลกับแหล่งข้อมูลและเชื่อมต่อตามตัวเลือกความปลอดภัย (ข้อมูลประจำตัวที่เก็บไว้หรือการเข้าระบบครั้งเดียว) ที่เลือกขณะสร้างแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a713-170">Users with access to the data source can associate datasets to the data source, and connect, based on the security options (either the stored credentials or Single Sign-On) selected while creating a data source.</span></span>

### <a name="add-users-to-a-data-source"></a><span data-ttu-id="8a713-171">เพิ่มผู้ใช้ไปยังแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a713-171">Add users to a data source</span></span>

1. <span data-ttu-id="8a713-172">จากส่วนหัวของหน้าในบริการ Power BI ให้เลือก **การตั้งค่า**![ไอคอนรูปเฟืองการตั้งค่า](media/service-gateway-data-sources/icon-gear.png) > **จัดการเกตเวย์**</span><span class="sxs-lookup"><span data-stu-id="8a713-172">From the page header in the Power BI service, select  **Settings** ![Settings gear icon](media/service-gateway-data-sources/icon-gear.png) > **Manage gateways**.</span></span>

2. <span data-ttu-id="8a713-173">เลือกแหล่งข้อมูลที่คุณต้องการเพิ่มผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="8a713-173">Select the data source where you want to add users.</span></span>

3. <span data-ttu-id="8a713-174">เลือก **ผู้ใช้** และป้อนผู้ใช้และกลุ่มความปลอดภัยที่เปิดใช้งานอีเมลจากองค์กรของคุณซึ่งจะเข้าถึงแหล่งข้อมูลที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8a713-174">Select **Users**, and enter the users and mail-enabled security groups from your organization who will access the selected data source.</span></span> <span data-ttu-id="8a713-175">เลือก **เพิ่ม** และชื่อของสมาชิกที่เพิ่มจะถูกเพิ่มลงในรายการผู้ที่สามารถเผยแพร่รายงานที่ใช้แหล่งข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="8a713-175">Select **Add**, and the added member's name is added to the list of people who can publish reports that use this data source.</span></span>

    ![เพิ่มผู้ใช้](media/service-gateway-data-sources/add-user.png)

<span data-ttu-id="8a713-177">โปรดทราบคุณต้องเพิ่มผู้ใช้ไปยังแต่ละแหล่งข้อมูลที่คุณต้องการให้สิทธิ์เข้าใช้</span><span class="sxs-lookup"><span data-stu-id="8a713-177">Remember that you need to add users to each data source that you want to grant access to.</span></span> <span data-ttu-id="8a713-178">แต่ละแหล่งข้อมูลมีรายการชื่อผู้ใช้ที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="8a713-178">Each data source has a separate list of users.</span></span> <span data-ttu-id="8a713-179">เพิ่มผู้ใช้ไปยังแต่ละแหล่งข้อมูลแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="8a713-179">Add users to each data source separately.</span></span>

### <a name="remove-users-from-a-data-source"></a><span data-ttu-id="8a713-180">เอาผู้ใช้ออกจากแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a713-180">Remove users from a data source</span></span>

<span data-ttu-id="8a713-181">บนแท็บ **ผู้ใช้** สำหรับแหล่งข้อมูล คุณสามารถเอาผู้ใช้และกลุ่มความปลอดภัยที่ใช้แหล่งข้อมูลนี้ออกได้</span><span class="sxs-lookup"><span data-stu-id="8a713-181">On the **Users** tab for the data source, you can remove users and security groups that use this data source.</span></span>

![เอาผู้ใช้ออก](media/service-gateway-data-sources/remove-user.png)

## <a name="store-encrypted-credentials-in-the-cloud"></a><span data-ttu-id="8a713-183">จัดเก็บข้อมูลประจำตัวเข้ารหัสลับในระบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="8a713-183">Store encrypted credentials in the cloud</span></span>

<span data-ttu-id="8a713-184">เมื่อคุณเพิ่มแหล่งข้อมูลกับเกตเวย์ คุณต้องใส่ข้อมูลประจำตัวสำหรับแหล่งข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="8a713-184">When you add a data source to the gateway, you must provide credentials for that data source.</span></span> <span data-ttu-id="8a713-185">คิวรีทั้งหมดที่ไปยังแหล่งข้อมูลจะทำงานโดยใช้ข้อมูลประจำตัวเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8a713-185">All queries to the data source will run by using these credentials.</span></span> <span data-ttu-id="8a713-186">ข้อมูลประจำตัวจะมีการเข้ารหัสลับอย่างปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="8a713-186">The credentials are encrypted securely.</span></span> <span data-ttu-id="8a713-187">โดยการใช้การเข้ารหัสลับสมมาตรเพื่อให้ไม่สามารถถอดรหัสในระบบคลาวด์ก่อนที่จะถูกจัดเก็บในระบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="8a713-187">They use symmetric encryption so that they can't be decrypted in the cloud before they're stored in the cloud.</span></span> <span data-ttu-id="8a713-188">ข้อมูลประจำตัวถูกส่งไปยังเครื่องที่เรียกใช้เกตเวย์ภายในองค์กร ที่ข้อมูลเหล่านี้จะถูกถอดรหัสลับเมื่อมีการเข้าถึงแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a713-188">The credentials are sent to the machine that runs the gateway, on-premises, where they're decrypted when the data sources are accessed.</span></span>

## <a name="list-of-available-data-source-types"></a><span data-ttu-id="8a713-189">รายการของชนิดแหล่งข้อมูลที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8a713-189">List of available data source types</span></span>

<span data-ttu-id="8a713-190">สำหรับข้อมูลเกี่ยวกับแหล่งข้อมูลที่เกตเวย์ข้อมูลภายในองค์กรสนับสนุน ให้ดู [แหล่งข้อมูล Power BI](power-bi-data-sources.md)</span><span class="sxs-lookup"><span data-stu-id="8a713-190">For information about which data sources the on-premises data gateway supports, see [Power BI data sources](power-bi-data-sources.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="8a713-191">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="8a713-191">Next steps</span></span>

* [<span data-ttu-id="8a713-192">จัดการแหล่งข้อมูลของคุณ - Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8a713-192">Manage your data source - Analysis Services</span></span>](service-gateway-enterprise-manage-ssas.md)
* [<span data-ttu-id="8a713-193">จัดการแหล่งข้อมูลของคุณ - SAP HANA</span><span class="sxs-lookup"><span data-stu-id="8a713-193">Manage your data source - SAP HANA</span></span>](service-gateway-enterprise-manage-sap.md)
* [<span data-ttu-id="8a713-194">จัดการแหล่งข้อมูลของคุณ - SQL Server</span><span class="sxs-lookup"><span data-stu-id="8a713-194">Manage your data source - SQL Server</span></span>](service-gateway-enterprise-manage-sql.md)
* [<span data-ttu-id="8a713-195">จัดการแหล่งข้อมูลของคุณ - Oracle</span><span class="sxs-lookup"><span data-stu-id="8a713-195">Manage your data source - Oracle</span></span>](service-gateway-onprem-manage-oracle.md)
* [<span data-ttu-id="8a713-196">จัดการแหล่งข้อมูลของคุณ - นำเข้า/รีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="8a713-196">Manage your data source - Import/scheduled refresh</span></span>](service-gateway-enterprise-manage-scheduled-refresh.md)
* [<span data-ttu-id="8a713-197">คำแนะนำสำหรับการปรับใช้เกตเวย์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8a713-197">Guidance for deploying a data gateway</span></span>](service-gateway-deployment-guidance.md)

<span data-ttu-id="8a713-198">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8a713-198">More questions?</span></span> <span data-ttu-id="8a713-199">ลองไปที่ [ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="8a713-199">Try the [Power BI Community](https://community.powerbi.com/).</span></span>
