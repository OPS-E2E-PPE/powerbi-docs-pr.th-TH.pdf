---
title: เชื่อมต่อกับ Snowflake ด้วย Power BI
description: เรียนรู้วิธีการเชื่อมต่อกับ Snowflake สำหรับ Power BI โดยใช้การรับรองความถูกต้อง SSO
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 06/26/2020
LocalizationGroup: Connect to services
ms.openlocfilehash: 75d4a4db1d21297fcdfd675ca4eaaf82e5e611f5
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410585"
---
# <a name="connect-to-snowflake-in-power-bi-service"></a><span data-ttu-id="4c65d-103">เชื่อมต่อกับ Snowflake ในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="4c65d-103">Connect to Snowflake in Power BI Service</span></span>

## <a name="introduction"></a><span data-ttu-id="4c65d-104">บทนำ</span><span class="sxs-lookup"><span data-stu-id="4c65d-104">Introduction</span></span>

<span data-ttu-id="4c65d-105">การเชื่อมต่อกับ Snowflake ในบริการของ Power BI มีความแตกต่างจากตัวเชื่อมต่ออื่นๆ เพียงหนึ่งประการ</span><span class="sxs-lookup"><span data-stu-id="4c65d-105">Connecting to Snowflake in the Power BI service  differs from other connectors in only one way.</span></span> <span data-ttu-id="4c65d-106">Snowflake มีความสามารถเพิ่มเติมสำหรับ Azure Active Directory (AAD) ด้วยตัวเลือกสำหรับ SSO</span><span class="sxs-lookup"><span data-stu-id="4c65d-106">Snowflake has an additional capability for Azure Active Directory (AAD), with an option for SSO.</span></span> <span data-ttu-id="4c65d-107">ส่วนต่างๆ ของการรวมต้องมีบทบาทการดูแลที่แตกต่างกันใน Snowflake Power BI และ Azure</span><span class="sxs-lookup"><span data-stu-id="4c65d-107">Parts of the integration require different administrative roles across Snowflake, Power BI, and Azure.</span></span> <span data-ttu-id="4c65d-108">คุณยังสามารถเลือกเปิดใช้งานการรับรองความถูกต้อง AAD โดยไม่ต้องใช้ SSO ได้</span><span class="sxs-lookup"><span data-stu-id="4c65d-108">You can also choose to enable AAD authentication without using SSO.</span></span> <span data-ttu-id="4c65d-109">การรับรองความถูกต้องเบื้องต้นทำงานคล้ายกับตัวเชื่อมต่ออื่น ๆ ในบริการ</span><span class="sxs-lookup"><span data-stu-id="4c65d-109">Basic authentication works similarly to other connectors in the service.</span></span>

<span data-ttu-id="4c65d-110">ในการกำหนดค่าการรวม AAD และเลือกเปิดใช้งาน SSO ให้ทำตามขั้นตอนในบทความนี้:</span><span class="sxs-lookup"><span data-stu-id="4c65d-110">To configure AAD integration and optionally enable SSO, follow the steps in this article:</span></span>

* <span data-ttu-id="4c65d-111">ถ้าคุณเป็นผู้ดูแลระบบ Snowflake โปรดอ่านบทความ [Power BI SSO ถึง Snowflake - เริ่มต้นใช้งาน](https://docs.snowflake.com/en/user-guide/oauth-powerbi.html) ในเอกสารคู่มือ Snowflake</span><span class="sxs-lookup"><span data-stu-id="4c65d-111">If you're the Snowflake admin, read the [Power BI SSO to Snowflake - Getting Started](https://docs.snowflake.com/en/user-guide/oauth-powerbi.html) article in the Snowflake documentation.</span></span>
* <span data-ttu-id="4c65d-112">ถ้าคุณเป็นผู้ดูแลระบบ Power BI ให้อ้างอิง [การกำหนดค่าบริการของ Power BI - พอร์ทัลผู้ดูแลระบบ](service-connect-snowflake.md#admin-portal) เพื่อเรียนรู้วิธีการเปิดใช้งาน SSO</span><span class="sxs-lookup"><span data-stu-id="4c65d-112">If you're a Power BI admin, reference [Power BI Service configuration - Admin Portal](service-connect-snowflake.md#admin-portal) to learn how to enable SSO.</span></span>
* <span data-ttu-id="4c65d-113">ถ้าคุณเป็นผู้สร้างชุดข้อมูล Power BI ให้อ้างอิง [การกำหนดค่าบริการของ Power BI - การกำหนดค่าชุดข้อมูลด้วย AAD](service-connect-snowflake.md#configuring-a-dataset-with-aad) เพื่อเรียนรู้วิธีการเปิดใช้งาน SSO</span><span class="sxs-lookup"><span data-stu-id="4c65d-113">If you're a Power BI dataset creator, reference [Power BI Service configuration - Configuring a dataset with AAD](service-connect-snowflake.md#configuring-a-dataset-with-aad) to learn how to enable SSO.</span></span>

## <a name="power-bi-service-configuration"></a><span data-ttu-id="4c65d-114">การกำหนดค่าบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="4c65d-114">Power BI Service configuration</span></span>

### <a name="admin-portal"></a><span data-ttu-id="4c65d-115">พอร์ทัลผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="4c65d-115">Admin portal</span></span>

<span data-ttu-id="4c65d-116">เมื่อต้องการเปิดใช้งาน SSO ผู้ดูแลระบบส่วนกลางจะต้องเปิดการตั้งค่าในพอร์ทัลผู้ดูแลระบบ Power BI</span><span class="sxs-lookup"><span data-stu-id="4c65d-116">To enable SSO, a global admin has to turn on the setting in the Power BI Admin portal.</span></span> <span data-ttu-id="4c65d-117">การตั้งค่านี้จะอนุมัติการส่งข้อมูลประจำตัว AAD ไปยัง Snowflake สำหรับการรับรองความถูกต้องสำหรับทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="4c65d-117">This setting approves sending AAD credentials to Snowflake for authentication for the entire organization.</span></span> <span data-ttu-id="4c65d-118">ทำตามขั้นตอนเหล่านี้เพื่อเปิดใช้งาน SSO:</span><span class="sxs-lookup"><span data-stu-id="4c65d-118">Follow these steps to enable SSO:</span></span>

1. <span data-ttu-id="4c65d-119">[ลงชื่อเข้าใช้ Power BI](https://app.powerbi.com) โดยใช้ข้อมูลประจำตัวของผู้ดูแลระบบส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="4c65d-119">[Sign in to Power BI](https://app.powerbi.com) using global admin credentials.</span></span>
1. <span data-ttu-id="4c65d-120">เลือก **การตั้งค่า** จากเมนูส่วนหัวของหน้า จากนั้นเลือก **พอร์ทัลผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="4c65d-120">Select **Settings** from the page header menu, then select **Admin portal**.</span></span>
1. <span data-ttu-id="4c65d-121">เลือก **การตั้งค่าผู้เช่า** จากนั้นเลื่อนเพื่อค้นหา **การตั้งค่าการรวม**</span><span class="sxs-lookup"><span data-stu-id="4c65d-121">Select **Tenant settings**, then scroll to locate **Integration settings**.</span></span>

   ![การตั้งค่าผู้เช่าสำหรับ Snowflake SSO](media/service-connect-snowflake/snowflake-sso-tenant.png)

4. <span data-ttu-id="4c65d-123">ขยาย **Snowflake SSO** สลับการตั้งค่าเป็น **เปิดใช้งาน** จากนั้นเลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="4c65d-123">Expand **Snowflake SSO**, toggle the setting to **Enabled**, then select **Apply**.</span></span>

<span data-ttu-id="4c65d-124">ขั้นตอนนี้จะต้องยินยอมให้ส่งโทเค็น AAD ของคุณไปยังเซิร์ฟเวอร์ Snowflake</span><span class="sxs-lookup"><span data-stu-id="4c65d-124">This step is required to consent to sending your AAD token to the  Snowflake  servers.</span></span> <span data-ttu-id="4c65d-125">หลังจากที่คุณเปิดใช้งานการตั้งค่า อาจใช้เวลาถึงหนึ่งชั่วโมงจึงจะมีผลการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4c65d-125">After you enable the setting, it may take up to an hour for it to take effect.</span></span>

<span data-ttu-id="4c65d-126">หลังจากที่มีการเปิดใช้งาน SSO คุณสามารถใช้รายงานกับ SSO ได้</span><span class="sxs-lookup"><span data-stu-id="4c65d-126">After SSO is enabled you can use reports with SSO.</span></span>

### <a name="configuring-a-dataset-with-aad"></a><span data-ttu-id="4c65d-127">การกำหนดค่าชุดข้อมูลที่มี AAD</span><span class="sxs-lookup"><span data-stu-id="4c65d-127">Configuring a Dataset with AAD</span></span>

<span data-ttu-id="4c65d-128">หลังจากที่มีการเผยแพร่รายงานที่อิงตามตัวเชื่อมต่อ Snowflake ไปยังบริการของ Power BI ผู้สร้างชุดข้อมูลต้องอัปเดตตั้งค่าสำหรับพื้นที่ทำงานที่เหมาะสมเพื่อให้สามารถใช้ SSO ได้</span><span class="sxs-lookup"><span data-stu-id="4c65d-128">After a report that is based on the Snowflake connector is published to the Power BI service, the dataset creator has to update settings for the appropriate workspace so that it will use SSO.</span></span>

<span data-ttu-id="4c65d-129">เนื่องด้วยวิธีการทำงานของ Power BI นั้น SSO จะทำงานเฉพาะเมื่อไม่มีการเรียกใช้แหล่งข้อมูลผ่านเกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="4c65d-129">Because of the way that Power BI works, SSO will only work when no data sources are run through the on-premises data gateway.</span></span> <span data-ttu-id="4c65d-130">ข้อจำกัดแสดงดังรายการด้านล่าง:</span><span class="sxs-lookup"><span data-stu-id="4c65d-130">Limitations are listed below:</span></span>

* <span data-ttu-id="4c65d-131">หากคุณกำลังใช้เฉพาะแหล่งข้อมูล Snowflake ในแบบจำลองข้อมูลของคุณ คุณสามารถใช้ SSO ได้ถ้าคุณเลือกที่จะไม่ใช้เกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="4c65d-131">If you're using only a Snowflake source in your data model, then you can use SSO if you choose not to use the on-premises data gateway.</span></span>
* <span data-ttu-id="4c65d-132">หากคุณกำลังใช้แหล่งข้อมูล Snowflake กับแหล่งข้อมูลอื่น คุณสามารถใช้ SSO ได้หากไม่มีแหล่งข้อมูลใดที่ใช้เกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="4c65d-132">If you're using a Snowflake source and another source, then you can use SSO if none of the sources use the on-premises data gateway.</span></span>
* <span data-ttu-id="4c65d-133">หากคุณกำลังใช้แหล่งข้อมูล Snowflake ผ่านเกตเวย์ข้อมูลภายในองค์กร โปรดทราบว่าข้อมูลประจำตัว AAD ยังไม่รองรับในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="4c65d-133">If you're using a Snowflake source through the on-premises data gateway, AAD credentials aren't currently supported.</span></span> <span data-ttu-id="4c65d-134">การพิจารณานี้อาจมีความเกี่ยวข้องในกรณีที่คุณกำลังพยายามเข้าถึง VNet จาก IP เดียวกับเกตเวย์ที่ติดตั้งอยู่ในนั้น แทนที่จะเป็นจากช่วง IP ทั้งหมดของ Power BI</span><span class="sxs-lookup"><span data-stu-id="4c65d-134">This consideration might be relevant in case you're trying to access a VNet from a single IP with the gateway installed on it, rather than from the entire Power BI IP range.</span></span>
* <span data-ttu-id="4c65d-135">หากคุณกำลังใช้แหล่งข้อมูล Snowflake และแหล่งข้อมูลอื่นที่ต้องการใช้เกตเวย์ คุณจะต้องใช้ Snowflake ผ่านเกตเวย์ข้อมูลภายในองค์กรเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="4c65d-135">If you're using a Snowflake source and another source that requires a gateway, you need to use Snowflake through the on-premises data gateway as well.</span></span> <span data-ttu-id="4c65d-136">คุณจะไม่สามารถใช้ SSO ในกรณีนี้ได้</span><span class="sxs-lookup"><span data-stu-id="4c65d-136">You won't be able to use SSO in this case.</span></span>

<span data-ttu-id="4c65d-137">เรียนรู้เพิ่มเติมเกี่ยวกับวิธีการใช้เกตเวย์ข้อมูลภายในองค์กรใน [เกตเวย์ข้อมูลภายในองค์กรคืออะไร](service-gateway-onprem.md)</span><span class="sxs-lookup"><span data-stu-id="4c65d-137">Learn more about how to use the on-premises data gateway, in [What is an on-premises data gateway?](service-gateway-onprem.md)</span></span>

<span data-ttu-id="4c65d-138">หากคุณไม่ได้ใช้เกตเวย์นั้น คุณพร้อมใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="4c65d-138">If you aren't using the gateway, you're all set.</span></span> <span data-ttu-id="4c65d-139">เมื่อคุณมีการกำหนดค่าข้อมูลประจำตัว Snowflake บนเกตเวย์ข้อมูลภายในองค์กรของคุณแล้ว แต่คุณใช้เฉพาะแหล่งข้อมูลนั้นในแบบจำลองของคุณ คุณสามารถคลิกปุ่มสลับบนหน้าการตั้งค่าชุดข้อมูล เพื่อปิดเกตเวย์สำหรับแบบจำลองข้อมูลนั้นได้</span><span class="sxs-lookup"><span data-stu-id="4c65d-139">When you have Snowflake credentials configured on your on-premises data gateway, but are only using that data source in your model, you can click the toggle on the Dataset settings page to turn off the gateway for that data model.</span></span>

![การตั้งค่าชุดข้อมูลเพื่อสลับปิดเกตเวย์](media/service-connect-snowflake/snowflake-gateway-toggle-off.png)

<span data-ttu-id="4c65d-141">เมื่อต้องการเปิดใช้งาน SSO สำหรับชุดข้อมูล ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="4c65d-141">To turn on SSO for a dataset, follow these steps:</span></span>

1. <span data-ttu-id="4c65d-142">[ลงชื่อเข้าใช้ Power BI](https://app.powerbi.com) โดยใช้ข้อมูลประจำตัวของผู้สร้างชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4c65d-142">[Sign in to Power BI](https://app.powerbi.com) using dataset creator credentials.</span></span>
1. <span data-ttu-id="4c65d-143">เลือกพื้นที่ทำงานที่เหมาะสม จากนั้นเลือก **การตั้งค่า** จากเมนูตัวเลือกเพิ่มเติมที่อยู่ถัดจากชื่อชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4c65d-143">Select the appropriate workspace, then choose **Settings** from the more options menu that's located next to the dataset name.</span></span>
  <span data-ttu-id="4c65d-144">![เมนูตัวเลือกเพิ่มเติมจะปรากฏขึ้นเมื่อเลื่อนเมาส์](media/service-connect-snowflake/dataset-settings-2.png)</span><span class="sxs-lookup"><span data-stu-id="4c65d-144">![More options menu appears on hover](media/service-connect-snowflake/dataset-settings-2.png)</span></span>
1. <span data-ttu-id="4c65d-145">เลือก **ข้อมูลประจำตัวของแหล่งข้อมูล** และลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="4c65d-145">Select **Data source credentials** and sign in.</span></span> <span data-ttu-id="4c65d-146">คุณสามารถลงชื่อเข้าใช้ชุดข้อมูลไปยัง Snowflake ได้ด้วยข้อมูลประจำตัวพื้นฐานหรือข้อมูลประจำตัว OAuth2 (AAD)</span><span class="sxs-lookup"><span data-stu-id="4c65d-146">The dataset can be signed into Snowflake with Basic or OAuth2 (AAD) credentials.</span></span> <span data-ttu-id="4c65d-147">ถ้าคุณใช้ AAD คุณสามารถเปิดใช้งาน SSO ในขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4c65d-147">if you use AAD, you can enable SSO in the next step.</span></span>
1. <span data-ttu-id="4c65d-148">เลือกตัวเลือก **ผู้ใช้ใช้ข้อมูลประจำตัว OAuth2 ของตนเองเมื่อเข้าถึงแหล่งข้อมูลนี้ผ่านทาง DirectQuery**</span><span class="sxs-lookup"><span data-stu-id="4c65d-148">Select the option **End users use their own OAuth2 credentials when accessing this data source via DirectQuery**.</span></span> <span data-ttu-id="4c65d-149">การตั้งค่านี้จะเป็นการเปิดใช้งาน AAD SSO</span><span class="sxs-lookup"><span data-stu-id="4c65d-149">This setting will enable AAD SSO.</span></span> <span data-ttu-id="4c65d-150">ไม่ว่าผู้ใช้เริ่มต้นจะลงชื่อเข้าใช้ด้วยการรับรองความถูกต้องเบื้องต้นหรือ OAuth2 (AAD) ข้อมูลประจำตัวของ AAD ก็คือสิ่งที่จะถูกส่งไปยัง SSO</span><span class="sxs-lookup"><span data-stu-id="4c65d-150">Whether the first user signs in with Basic authentication or OAuth2 (AAD), the AAD credentials are what will be sent for SSO.</span></span>

    ![การตั้งค่าชุดข้อมูลสำหรับ Snowflake SSO](media/service-connect-snowflake/snowflake-sso-cred-ui.png)

<span data-ttu-id="4c65d-152">เมื่อเสร็จสิ้นขั้นตอนดังกล่าวแล้ว ผู้ใช้ควรใช้การรับรองความถูกต้อง AAD ของตนโดยอัตโนมัติเพื่อเชื่อมต่อกับข้อมูลจากชุดข้อมูลของ Snowflake นั้น</span><span class="sxs-lookup"><span data-stu-id="4c65d-152">After these steps are done, users should automatically use their AAD authentication to connect to data from that Snowflake dataset.</span></span>

<span data-ttu-id="4c65d-153">ถ้าคุณเลือกที่จะไม่เปิดใช้งาน SSO จากนั้นผู้ใช้จะรีเฟรชรายงานจะใช้ข้อมูลประจำตัวของผู้ใช้ที่เข้าสู่ระบบ เช่น รายงาน Power BI อื่นๆ ส่วนใหญ่</span><span class="sxs-lookup"><span data-stu-id="4c65d-153">If you choose not to enable SSO, then users refreshing the report will use the credentials of the user who signed in, like most other Power BI reports.</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="4c65d-154">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="4c65d-154">Troubleshooting</span></span>

<span data-ttu-id="4c65d-155">หากพบปัญหาใดก็ตามเกี่ยวกับการรวม โปรดอ้างอิง [คู่มือการแก้ไขปัญหา](https://docs.snowflake.com/en/user-guide/oauth-powerbi.html#troubleshooting) ของ Snowflake</span><span class="sxs-lookup"><span data-stu-id="4c65d-155">If you run into any issues with the integration, refer to the Snowflake [troubleshooting guide](https://docs.snowflake.com/en/user-guide/oauth-powerbi.html#troubleshooting).</span></span>

## <a name="next-steps"></a><span data-ttu-id="4c65d-156">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4c65d-156">Next steps</span></span>

* [<span data-ttu-id="4c65d-157">แหล่งข้อมูลสำหรับบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="4c65d-157">Data sources for the Power BI service</span></span>](service-get-data.md)
* [<span data-ttu-id="4c65d-158">เชื่อมต่อกับชุดข้อมูลในบริการของ Power BI จาก Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4c65d-158">Connect to datasets in the Power BI service from Power BI desktop</span></span>](desktop-report-lifecycle-datasets.md)
* [<span data-ttu-id="4c65d-159">เชื่อมต่อกับ Snowflake Computing Warehouse</span><span class="sxs-lookup"><span data-stu-id="4c65d-159">Connect to a Snowflake computing warehouse</span></span>](desktop-connect-snowflake.md)