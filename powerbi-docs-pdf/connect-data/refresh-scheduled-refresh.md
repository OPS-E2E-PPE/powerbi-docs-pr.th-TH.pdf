---
title: กำหนดค่าการรีเฟรชตามกำหนดเวลา
description: ซึ่งจะครอบคลุมขั้นตอนในการเลือกเกตเวย์ และกำหนดค่าการรีเฟรชตามกำหนดการ
author: davidiseminger
ms.author: davidi
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 06/06/2019
LocalizationGroup: Data refresh
ms.openlocfilehash: 9298171a98837a6e8dd16cc89865770e7d88c8c2
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96403915"
---
# <a name="configure-scheduled-refresh"></a><span data-ttu-id="8b8c1-103">กำหนดค่าการรีเฟรชตามกำหนดเวลา</span><span class="sxs-lookup"><span data-stu-id="8b8c1-103">Configure scheduled refresh</span></span>

>[!NOTE]
><span data-ttu-id="8b8c1-104">หลังจากสองเดือนที่ไม่ได้ใช้งาน การรีเฟรชตามกำหนดการบนชุดข้อมูลของคุณจะหยุดชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="8b8c1-104">After two months of inactivity, scheduled refresh on your dataset is paused.</span></span> <span data-ttu-id="8b8c1-105">สำหรับข้อมูลเพิ่มเติม ดู [*การรีเฟรชตามกำหนดการ*](#scheduled-refresh) ในภายหลังในบทความนี้</span><span class="sxs-lookup"><span data-stu-id="8b8c1-105">For more information, see [*Scheduled refresh*](#scheduled-refresh) later in this article.</span></span>

<span data-ttu-id="8b8c1-106">บทความนี้จะอธิบายถึงตัวเลือกที่พร้อมใช้งานสำหรับการรีเฟรชตามกำหนดเวลาทั้ง[เกตเวย์ข้อมูลภายในองค์กร (โหมดส่วนบุคคล)](service-gateway-personal-mode.md) และ[เกตเวย์ข้อมูลภายในองค์กร](service-gateway-onprem.md)</span><span class="sxs-lookup"><span data-stu-id="8b8c1-106">This article describes the options available for scheduled refresh for the [On-premises data gateway (personal mode)](service-gateway-personal-mode.md) and the [On-premises data gateway](service-gateway-onprem.md).</span></span> <span data-ttu-id="8b8c1-107">คุณระบุตัวเลือกการรีเฟรชในพื้นที่ต่อไปนี้ของบริการ Power BI: **การเชื่อมต่อเกตเวย์** **ข้อมูลประจำตัวของแหล่งข้อมูล** และ **การรีเฟรชตามกำหนดเวลา**</span><span class="sxs-lookup"><span data-stu-id="8b8c1-107">You specify refresh options in the following areas of the Power BI service: **Gateway connection**, **Data source credentials**, and **Scheduled refresh**.</span></span> <span data-ttu-id="8b8c1-108">เราจะมาดูกันตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="8b8c1-108">We'll look at each in turn.</span></span> <span data-ttu-id="8b8c1-109">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการรีเฟรชข้อมูล รวมถึงข้อจำกัดของกำหนดการรีเฟรช โปรดดู [การรีเฟรชข้อมูล](refresh-data.md#data-refresh)</span><span class="sxs-lookup"><span data-stu-id="8b8c1-109">For more information about data refresh, including limitations on refresh schedules, see [Data refresh](refresh-data.md#data-refresh).</span></span>

<span data-ttu-id="8b8c1-110">เมื่อต้องการไปยังหน้าจอ **การรีเฟรชตามกำหนดการ**:</span><span class="sxs-lookup"><span data-stu-id="8b8c1-110">To get to the **Scheduled refresh** screen:</span></span>

1. <span data-ttu-id="8b8c1-111">ในบานหน้าต่างนำทางภายใต้ **ชุดข้อมูล** ให้เลือก **ตัวเลือกเพิ่มเติม** (...) ถัดจากชุดข้อมูลที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="8b8c1-111">In the navigation pane, under **Datasets**, select **More options** (...) next to a dataset listed .</span></span>
2. <span data-ttu-id="8b8c1-112">เลือก **กำหนดเวลารีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="8b8c1-112">Select **Schedule Refresh**.</span></span>

    ![กำหนดตารางเวลาการรีเฟรช](media/refresh-scheduled-refresh/dataset-menu.png)

## <a name="gateway-connection"></a><span data-ttu-id="8b8c1-114">การเชื่อมต่อเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="8b8c1-114">Gateway connection</span></span>

<span data-ttu-id="8b8c1-115">คุณจะเห็นตัวเลือกที่แตกต่างกันต่อไปนี้โดยขึ้นอยู่กับว่าคุณมีเกตเวย์ส่วนบุคคล หรือ เกตเวย์องค์กรที่ออนไลน์ และพร้อมใช้งานหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8b8c1-115">You see different options here depending on whether you have a personal, or enterprise, gateway online and available.</span></span>

<span data-ttu-id="8b8c1-116">ถ้าไม่มีเกตเวย์ที่พร้อมใช้งาน คุณจะเห็น **การเชื่อมต่อเกตเวย์** ถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8b8c1-116">If no gateway is available, you see **Gateway connection** disabled.</span></span> <span data-ttu-id="8b8c1-117">นอกจากนี้คุณจะเห็นข้อความระบุวิธีการติดตั้งเกตเวย์ส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="8b8c1-117">You also see a message indicating how to install the personal gateway.</span></span>

![ไม่ได้กำหนดค่าเกตเวย์](media/refresh-scheduled-refresh/gateway-not-configured.png)

<span data-ttu-id="8b8c1-119">หากคุณมีเกตเวย์ส่วนบุคคลที่กำหนดค่าและเป็นออนไลน์ก็แสดงว่าสามารถเลือกได้</span><span class="sxs-lookup"><span data-stu-id="8b8c1-119">If you have a personal gateway configured and it's online, it's available to select.</span></span> <span data-ttu-id="8b8c1-120">ซึ่งจะแสดงแบบออฟไลน์ ถ้าไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8b8c1-120">It shows offline if it's not available.</span></span>

![การเชื่อมต่อเกตเวย์](media/refresh-scheduled-refresh/gateway-connection.png)

<span data-ttu-id="8b8c1-122">คุณยังสามารถเลือกเกตเวย์องค์กร ถ้าหากเกตเวย์พร้อมใช้งานสำหรับคุณ</span><span class="sxs-lookup"><span data-stu-id="8b8c1-122">You can also select the enterprise gateway if one is available for you.</span></span> <span data-ttu-id="8b8c1-123">คุณจะเห็นว่าเกตเวย์องค์กรพร้อมใช้งานเฉพาะเมื่อบัญชีของคุณแสดงอยู่ในแท็บ **ผู้ใช้** ของแหล่งข้อมูลที่กำหนดค่าไว้สำหรับเกตเวย์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="8b8c1-123">You only see an enterprise gateway available if your account is listed in the **Users** tab of the data source configured for a given gateway.</span></span>

## <a name="data-source-credentials"></a><span data-ttu-id="8b8c1-124">ข้อมูลประจำตัวของแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8b8c1-124">Data source credentials</span></span>

### <a name="power-bi-gateway---personal"></a><span data-ttu-id="8b8c1-125">Power BI Gateway - ส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="8b8c1-125">Power BI Gateway - Personal</span></span>

<span data-ttu-id="8b8c1-126">ถ้าคุณกำลังใช้เกตเวย์ส่วนบุคคลเพื่อรีเฟรชข้อมูล คุณต้องใส่ข้อมูลประจำตัวเพื่อเชื่อมต่อกับแหล่งข้อมูลหลังบ้าน</span><span class="sxs-lookup"><span data-stu-id="8b8c1-126">If you are using the personal gateway to refresh data, you must supply the credentials to connect to the back-end data source.</span></span> <span data-ttu-id="8b8c1-127">ถ้าคุณเชื่อมต่อกับชุดเนื้อหา ข้อมูลประจำตัวที่คุณใส่เพื่อเชื่อมต่อจะดำเนินการสำหรับการรีเฟรชตามกำหนดการจากบริการออนไลน์</span><span class="sxs-lookup"><span data-stu-id="8b8c1-127">If you connected to a content pack from an online service, the credentials you entered to connect are carried over for scheduled refresh.</span></span>

![ข้อมูลประจำตัวของแหล่งข้อมูล](media/refresh-scheduled-refresh/data-source-credentials-pgw.png)

<span data-ttu-id="8b8c1-129">คุณจำเป็นต้องลงชื่อเข้าใช้แหล่งข้อมูลในครั้งแรกที่คุณใช้การรีเฟรชบนชุดข้อมูลเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8b8c1-129">You're only required to sign in to a data source the first time you use refresh on that dataset.</span></span> <span data-ttu-id="8b8c1-130">เมื่อใส่แล้ว ข้อมูลประจำตัวเหล่านั้นจะยังคงอยู่กับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8b8c1-130">Once entered, those credentials are retained with the dataset.</span></span>

> [!NOTE]
> <span data-ttu-id="8b8c1-131">สำหรับวิธีการรับรองความถูกต้องบางวิธี ถ้ารหัสผ่านที่คุณใช้เพื่อลงชื่อเข้าใช้แหล่งข้อมูลหมดอายุ หรือมีการเปลี่ยนแปลง คุณจะต้องเปลี่ยนรหัสผ่านสำหรับแหล่งข้อมูลใน **ข้อมูลประจำตัวของแหล่งข้อมูล** ด้วย</span><span class="sxs-lookup"><span data-stu-id="8b8c1-131">For some authentication methods, if the password you use to sign into a data source expires or is changed, you need to change it for the data source in **Data source credentials** too.</span></span>

<span data-ttu-id="8b8c1-132">เมื่อเกิดสิ่งผิดปกติขึ้น ซึ่งโดยปกติปัญหาแล้วจะเกี่ยวกับเกตเวย์ที่ออฟไลน์เนื่องจากไม่สามารถลงชื่อเข้าใช้ Windows และเริ่มบริการ หรือเกี่ยวกับ Power BI ไม่สามารถไม่ลงชื่อเข้าใช้แหล่งข้อมูลเพื่อคิวรีสำหรับข้อมูลที่อัปเดต</span><span class="sxs-lookup"><span data-stu-id="8b8c1-132">When things go wrong, the problem usually has something to do with either the gateway being offline because it couldn't sign in to Windows and start the service, or Power BI couldn't sign in to the data sources to query for updated data.</span></span> <span data-ttu-id="8b8c1-133">ถ้าการรีเฟรชล้มเหลว ตรวจสอบการตั้งค่าของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8b8c1-133">If refresh fails, check the dataset settings.</span></span> <span data-ttu-id="8b8c1-134">ถ้าบริการเกตเวย์อยู่ในสถานะออฟไลน์ คุณจะเห็นข้อผิดพลาดที่ **สถานะ**</span><span class="sxs-lookup"><span data-stu-id="8b8c1-134">If the gateway service is offline, **Status** is where you see the error.</span></span> <span data-ttu-id="8b8c1-135">ถ้า Power BI ไม่สามารถลงชื่อเข้าใช้แหล่งข้อมูล คุณจะเห็นข้อผิดพลาดในข้อมูลประจำตัวของแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8b8c1-135">If Power BI can't sign into the data sources, you see an error in Data Source Credentials.</span></span>

### <a name="on-premises-data-gateway"></a><span data-ttu-id="8b8c1-136">เกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="8b8c1-136">On-premises data gateway</span></span>

<span data-ttu-id="8b8c1-137">ถ้าคุณกำลังใช้เกตเวย์ข้อมูลในองค์กรเพื่อรีเฟรชข้อมูล คุณไม่จำเป็นต้องใส่ข้อมูลประจำตัวเนื่องจากมีการกำหนดไว้แล้วสำหรับแหล่งข้อมูลโดยผู้ดูแลเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="8b8c1-137">If you are using the On-premises data gateway to refresh data, you do not need to supply credentials, as they are defined for the data source by the gateway administrator.</span></span>

![กำหนดตารางเวลาการรีเฟรชคำสั่ง](media/refresh-scheduled-refresh/data-source-credentials-egw.png)

> [!NOTE]
> <span data-ttu-id="8b8c1-139">เมื่อเชื่อมต่อกับ SharePoint ภายในองค์กรสำหรับการรีเฟรชข้อมูล Power BI สนับสนุนเฉพาะกลไกพิสูจน์ตัวตน *Anonymous*, *Basic* และ *Windows (NTLM/Kerberos)*</span><span class="sxs-lookup"><span data-stu-id="8b8c1-139">When connecting to on-premises SharePoint for data refresh, Power BI supports only *Anonymous*, *Basic*, and *Windows (NTLM/Kerberos)* authentication mechanisms.</span></span> <span data-ttu-id="8b8c1-140">Power BI ไม่รองรับ *ADFS* หรือ *กลไลการพิสูจน์ตัวตนพื้นฐานแบบฟอร์ม* กลไกสำหรับการรีเฟรชข้อมูลของแหล่งข้อมูล SharePoint ภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="8b8c1-140">Power BI does not support *ADFS* or any *Forms-Based Authentication* mechanisms for data refresh of on-premises SharePoint data sources.</span></span>

## <a name="scheduled-refresh"></a><span data-ttu-id="8b8c1-141">รีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="8b8c1-141">Scheduled refresh</span></span>

<span data-ttu-id="8b8c1-142">คุณสามารถกำหนดความถี่ที่และช่วงเวลาเพื่อรีเฟรชชุดข้อมูลได้ที่ส่วน **การรีเฟรชตามกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="8b8c1-142">The **Scheduled refresh** section is where you define the frequency and time slots to refresh the dataset.</span></span> <span data-ttu-id="8b8c1-143">บางแหล่งข้อมูลไม่จำเป็นต้องใช้เกตเวย์เพื่อให้สามารถกำหนดค่าในการรีเฟรช ส่วนแหล่งข้อมูลอื่น ๆ จำเป็นต้องใช้เกตเวย์</span><span class="sxs-lookup"><span data-stu-id="8b8c1-143">Some data sources do not require a gateway to be configurable for refresh; other data sources require a gateway.</span></span>

<span data-ttu-id="8b8c1-144">ตั้งค่าแถบ **อัปเดตข้อมูลของคุณอยู่เสมอ** โดยเลื่อนไปที่ **เปิด** เพื่อกำหนดค่าการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="8b8c1-144">Set the **Keep your data up to date** slider to **On** to configure the settings.</span></span>

> [!NOTE]
> <span data-ttu-id="8b8c1-145">เป้าหมายคือการเริ่มต้นการรีเฟรชภายใน 15 นาทีของช่วงเวลาที่กำหนดไว้ แต่อาจเกิดความล่าช้าได้ถึงหนึ่งชั่วโมงหากบริการไม่สามารถจัดสรรทรัพยากรที่ต้องการได้เร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="8b8c1-145">The target is to initiate the refresh within 15 minutes of the scheduled time slot, but a delay of up to one hour can occur if the service can't allocate the required resources sooner.</span></span>

![กล่องโต้ตอบการรีเฟรชตามกำหนดการ](media/refresh-scheduled-refresh/scheduled-refresh.png)

> [!NOTE]
> <span data-ttu-id="8b8c1-147">หลังจากสองเดือนที่ไม่ได้ใช้งาน การรีเฟรชตามกำหนดการบนชุดข้อมูลของคุณจะหยุดชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="8b8c1-147">After two months of inactivity, scheduled refresh on your dataset is paused.</span></span> <span data-ttu-id="8b8c1-148">หากไม่มีผู้ใช้เข้าเยี่ยมชมแดชบอร์ดหรือรายงานใด ๆ ที่สร้างบนชุดข้อมูล จะถือว่าชุดข้อมูลนั้นไม่ได้ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8b8c1-148">A dataset is considered inactive when no user has visited any dashboard or report built on the dataset.</span></span> <span data-ttu-id="8b8c1-149">ในเวลานั้น อีเมลจะส่งไปยังเจ้าของชุดข้อมูลเพื่อระบุว่าการรีเฟรชตามกำหนดการจะหยุดชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="8b8c1-149">At that time, the dataset owner is sent an email indicating the scheduled refresh is paused.</span></span> <span data-ttu-id="8b8c1-150">จากนั้น กำหนดการรีเฟรชสำหรับชุดข้อมูลจะแสดงเป็น **ถูกปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="8b8c1-150">The refresh schedule for the dataset is then displayed as **disabled**.</span></span> <span data-ttu-id="8b8c1-151">เมื่อต้องการทำการรีเฟรชตามกำหนดการต่อ เพียงแค่เข้าไปที่แดชบอร์ดหรือรายงานใด ๆ ที่สร้างบนชุดข้อมูลอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="8b8c1-151">To resume scheduled refresh, simply revisit any dashboard or report built on the dataset.</span></span>

## <a name="whats-supported"></a><span data-ttu-id="8b8c1-152">อะไรบ้างที่ได้รับการสนับสนุน?</span><span class="sxs-lookup"><span data-stu-id="8b8c1-152">What's supported?</span></span>


> [!NOTE]
> <span data-ttu-id="8b8c1-153">การรีเฟรชที่กำหนดเวลาไว้จะถูกปิดการใช้งานโดยอัตโนมัติหลังจากเกิดข้อผิดพลาดติดต่อกันสี่ครั้ง</span><span class="sxs-lookup"><span data-stu-id="8b8c1-153">Scheduled refresh will also get disabled automatically after four consecutive errors.</span></span>

<span data-ttu-id="8b8c1-154">ชุดข้อมูลบางชุดได้รับการสนับสนุนเกตเวย์ที่แตกต่างกันสำหรับการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="8b8c1-154">Certain datasets are supported against different gateways for scheduled refresh.</span></span> <span data-ttu-id="8b8c1-155">นี่คือข้อมูลอ้างอิงเพื่อทำความเข้าใจว่ามีอะไรพร้อมใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="8b8c1-155">Here is a reference to understand what is available.</span></span>

### <a name="power-bi-gateway---personal"></a><span data-ttu-id="8b8c1-156">Power BI Gateway - ส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="8b8c1-156">Power BI Gateway - Personal</span></span>

<span data-ttu-id="8b8c1-157">**Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="8b8c1-157">**Power BI Desktop**</span></span>

* <span data-ttu-id="8b8c1-158">แหล่งข้อมูลออนไลน์ทั้งหมดที่แสดงใน **รับข้อมูล** และตัวแก้ไขคิวรีของ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="8b8c1-158">All online data sources shown in Power BI Desktop's **Get Data** and Query Editor.</span></span>
* <span data-ttu-id="8b8c1-159">แหล่งข้อมูลภายในองค์กรทั้งหมดที่แสดงอยู่ใน **รับข้อมูล** และตัวแก้ไขคิวรีของ Power BI Desktop ยกเว้นไฟล์ Hadoop (HDFS) และ Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="8b8c1-159">All on-premises data sources shown in Power BI Desktop's **Get Data** and Query Editor except for Hadoop file (HDFS) and Microsoft Exchange.</span></span>

<span data-ttu-id="8b8c1-160">**Excel**</span><span class="sxs-lookup"><span data-stu-id="8b8c1-160">**Excel**</span></span>

* <span data-ttu-id="8b8c1-161">แหล่งข้อมูลออนไลน์ทั้งหมดที่แสดงใน Power Query</span><span class="sxs-lookup"><span data-stu-id="8b8c1-161">All online data sources shown in Power Query.</span></span>
* <span data-ttu-id="8b8c1-162">แหล่งข้อมูลภายในองค์กรทั้งหมดที่แสดงอยู่ใน Power Query ยกเว้นไฟล์ Hadoop (HDFS) และ Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="8b8c1-162">All on-premises data sources shown in Power Query except for Hadoop file (HDFS) and Microsoft Exchange.</span></span>
* <span data-ttu-id="8b8c1-163">แหล่งข้อมูลออนไลน์ทั้งหมดที่แสดงใน Power Pivot</span><span class="sxs-lookup"><span data-stu-id="8b8c1-163">All online data sources shown in Power Pivot.</span></span>
* <span data-ttu-id="8b8c1-164">แหล่งข้อมูลภายในองค์กรทั้งหมดที่แสดงอยู่ใน Power Pivot ยกเว้นไฟล์ Hadoop (HDFS) และ Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="8b8c1-164">All on-premises data sources shown in Power Pivot except for Hadoop file (HDFS) and Microsoft Exchange.</span></span>

> [!NOTE]
> <span data-ttu-id="8b8c1-165">สำหรับ Excel 2016 และรุ่นใหม่กว่า Power Query จะแสดงอยู่บนส่วน **ข้อมูล** ของริบบอน ใต้ **รับและแปลงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="8b8c1-165">In Excel 2016 and later, Power Query is listed on the **Data** section of the ribbon, under **Get & Transform Data**.</span></span>

### <a name="power-bi-gateway"></a><span data-ttu-id="8b8c1-166">เกตเวย์ Power BI</span><span class="sxs-lookup"><span data-stu-id="8b8c1-166">Power BI Gateway</span></span>

<span data-ttu-id="8b8c1-167">สำหรับข้อมูลเกี่ยวกับแหล่งข้อมูลที่ได้รับการสนับสนุน ให้ดู [แหล่งข้อมูล Power BI](power-bi-data-sources.md)</span><span class="sxs-lookup"><span data-stu-id="8b8c1-167">For information about supported data sources, see [Power BI data sources](power-bi-data-sources.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="8b8c1-168">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="8b8c1-168">Troubleshooting</span></span>
<span data-ttu-id="8b8c1-169">การรีเฟรชข้อมูลอาจไม่เป็นไปตามที่คาดไว้ในบางครั้ง</span><span class="sxs-lookup"><span data-stu-id="8b8c1-169">Sometimes refreshing data may not go as expected.</span></span> <span data-ttu-id="8b8c1-170">โดยทั่วไปแล้วจะเป็นปัญหาที่เกี่ยวข้องกับเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="8b8c1-170">Typically this will be an issue connected with a gateway.</span></span> <span data-ttu-id="8b8c1-171">โปรดดูที่บทความแก้ไขปัญหาเกตเวย์สำหรับเครื่องมือและปัญหาที่ทราบแล้ว</span><span class="sxs-lookup"><span data-stu-id="8b8c1-171">Take a look at the gateway troubleshooting articles for tools and known issues.</span></span>

- [<span data-ttu-id="8b8c1-172">การแก้ไขปัญหาเกตเวย์ข้อมูลในองค์กร</span><span class="sxs-lookup"><span data-stu-id="8b8c1-172">Troubleshooting the On-premises data gateway</span></span>](service-gateway-onprem-tshoot.md)
- [<span data-ttu-id="8b8c1-173">การแก้ไขปัญหา Power BI Gateway - ส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="8b8c1-173">Troubleshooting the Power BI Gateway - Personal</span></span>](service-admin-troubleshooting-power-bi-personal-gateway.md)

## <a name="next-steps"></a><span data-ttu-id="8b8c1-174">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="8b8c1-174">Next steps</span></span>

- [<span data-ttu-id="8b8c1-175">การรีเฟรชข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8b8c1-175">Data refresh in Power BI</span></span>](refresh-data.md)  
- [<span data-ttu-id="8b8c1-176">เกตเวย์ Power BI - ส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="8b8c1-176">Power BI Gateway - Personal</span></span>](service-gateway-personal-mode.md)  
- [<span data-ttu-id="8b8c1-177">เกตเวย์ข้อมูลภายในองค์กร (โหมดส่วนบุคคล)</span><span class="sxs-lookup"><span data-stu-id="8b8c1-177">On-premises data gateway (personal mode)</span></span>](service-gateway-onprem.md)  
- [<span data-ttu-id="8b8c1-178">การแก้ไขปัญหาเกตเวย์ข้อมูลในองค์กร</span><span class="sxs-lookup"><span data-stu-id="8b8c1-178">Troubleshooting the On-premises data gateway</span></span>](service-gateway-onprem-tshoot.md)  
- [<span data-ttu-id="8b8c1-179">แก้ไขปัญหาเกตเวย์ Power BI - ส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="8b8c1-179">Troubleshooting the Power BI Gateway - Personal</span></span>](service-admin-troubleshooting-power-bi-personal-gateway.md)  

<span data-ttu-id="8b8c1-180">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8b8c1-180">More questions?</span></span> [<span data-ttu-id="8b8c1-181">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="8b8c1-181">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)