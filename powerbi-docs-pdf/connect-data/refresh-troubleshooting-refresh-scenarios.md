---
title: การแก้ไขปัญหาสถานการณ์สมมติในการรีเฟรช
description: การแก้ไขปัญหาสถานการณ์สมมติในการรีเฟรช
author: davidiseminger
ms.author: davidi
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: troubleshooting
ms.date: 12/14/2020
LocalizationGroup: Data refresh
ms.openlocfilehash: eba044de4918ad3cc62ce8b47144eab25c34702a
ms.sourcegitcommit: 46cf62d9bb33ac7b7eae7910fbba6756f626c65f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/15/2020
ms.locfileid: "97491816"
---
# <a name="troubleshooting-refresh-scenarios"></a><span data-ttu-id="3c43f-103">การแก้ไขปัญหาสถานการณ์สมมติในการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="3c43f-103">Troubleshooting refresh scenarios</span></span>

<span data-ttu-id="3c43f-104">ที่นี่คุณสามารถค้นหาข้อมูลเกี่ยวกับสถานการณ์สมมติที่หลากหลายที่คุณอาจประสบเมื่อรีเฟรชข้อมูลภายในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="3c43f-104">Here you can find information regarding different scenarios you may face when refreshing data within the Power BI service.</span></span>

> [!NOTE]
> <span data-ttu-id="3c43f-105">ถ้าคุณพบกับสถานการณ์สมมติที่ไม่ได้แสดงอยู่ในรายการด้านล่างนี้ และทำให้เกิดปัญหากับคุณ คุณสามารถขอความช่วยเหลือเพิ่มเติมได้ใน[เว็บไซต์ชุมชน](https://community.powerbi.com/) หรือคุณสามารถสร้าง[ตั๋วสนับสนุน](https://powerbi.microsoft.com/support/)ได้</span><span class="sxs-lookup"><span data-stu-id="3c43f-105">If you encounter a scenario that is not listed below, and it's causing you issues, you can ask for further assistance on the [community site](https://community.powerbi.com/), or you can create a [support ticket](https://powerbi.microsoft.com/support/).</span></span>
>

<span data-ttu-id="3c43f-106">คุณควรตรวจสอบให้แน่ใจว่ามีการตอบสนองความต้องการพื้นฐานสำหรับการรีเฟรชและผ่านการตรวจสอบแล้ว</span><span class="sxs-lookup"><span data-stu-id="3c43f-106">You should always ensure that basic requirements for refresh are met and verified.</span></span> <span data-ttu-id="3c43f-107">ข้อกำหนดพื้นฐานเหล่านี้ประกอบด้วย:</span><span class="sxs-lookup"><span data-stu-id="3c43f-107">These basic requirements include:</span></span>

* <span data-ttu-id="3c43f-108">ตรวจสอบเวอร์ชันของเกตเวย์ว่าเป็นเวอร์ชันล่าสุด</span><span class="sxs-lookup"><span data-stu-id="3c43f-108">Verify the gateway version is up to date</span></span>
* <span data-ttu-id="3c43f-109">ตรวจสอบว่ารายงานได้เลือกเกตเวย์แล้ว ถ้าไม่ใช่ แหล่งข้อมูลอาจมีการเปลี่ยนแปลงหรืออาจหายไป</span><span class="sxs-lookup"><span data-stu-id="3c43f-109">Verify the report has a gateway selected - if not, the datasource may have changed or might be missing</span></span>

<span data-ttu-id="3c43f-110">หลังจากที่คุณยืนยันความต้องการเหล่านั้นแล้ว โปรดลองดูที่ส่วนต่อไปนี้เพื่อแก้ไขปัญหาเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3c43f-110">Once you've confirmed those requirements are met, take a look through the following sections for more troubleshooting.</span></span> 


## <a name="email-notifications"></a><span data-ttu-id="3c43f-111">การแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="3c43f-111">Email notifications</span></span>

<span data-ttu-id="3c43f-112">หากคุณเข้ามาในบทความนี้จากการแจ้งเตือนทางอีเมล และคุณไม่ต้องการรับอีเมลเกี่ยวกับปัญหาการรีเฟรชอีกต่อไป ให้ติดต่อผู้ดูแลระบบ Power BI ของคุณ ขอให้พวกเขาลบอีเมลของคุณหรือรายชื่ออีเมลที่คุณสมัครใช้งานจากชุดข้อมูลที่เหมาะสมใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3c43f-112">If you're coming to this article from an email notification, and you no longer want to receive emails about refresh issues, contact your Power BI admin. Ask them to remove your email or an email list you're subscribed to from the appropriate datasets in Power BI.</span></span> <span data-ttu-id="3c43f-113">พวกเขาสามารถทำสิ่งนี้ได้จากพื้นที่ต่อไปนี้ในพอร์ทัลผู้ดูแลระบบ Power BI</span><span class="sxs-lookup"><span data-stu-id="3c43f-113">They can do this from the following area in the Power BI admin portal.</span></span>

![อีเมลสำหรับการแจ้งเตือนการรีเฟรช](media/refresh-troubleshooting-refresh-scenarios/refresh-email.png)

## <a name="refresh-using-web-connector-doesnt-work-properly"></a><span data-ttu-id="3c43f-115">รีเฟรชโดยการใช้ตัวเชื่อมต่อเว็บ ไม่ทำงานอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="3c43f-115">Refresh using Web connector doesn't work properly</span></span>

<span data-ttu-id="3c43f-116">ถ้าคุณมีสคริปต์ตัวเชื่อมต่อเว็บที่ใช้ในฟังก์ชัน [**Web.Page**](/powerquery-m/web-page) และคุณได้อัปเดตชุดข้อมูลหรือรายงานของคุณหลังวันที่ 18 พฤศจิกายน 2016 คุณต้องใช้เกตเวย์สำหรับการรีเฟรชเพื่อให้ระบบทำงานอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="3c43f-116">If you have a Web connector script that's using the [**Web.Page**](/powerquery-m/web-page) function, and you have updated your dataset or report after November 18th, 2016, you must use a gateway for refresh to work properly.</span></span>

## <a name="unsupported-data-source-for-refresh"></a><span data-ttu-id="3c43f-117">แหล่งข้อมูลที่ไม่รับรองสำหรับการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="3c43f-117">Unsupported data source for refresh</span></span>

<span data-ttu-id="3c43f-118">เมื่อต้องการกำหนดค่าชุดข้อมูล อาจมีข้อผิดพลาดที่ระบุว่า ชุดข้อมูลใช้แหล่งข้อมูลที่ไม่รับรองสำหรับการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="3c43f-118">When configuring a dataset, you may get an error indicating the dataset uses an unsupported data source for refresh.</span></span> <span data-ttu-id="3c43f-119">สำหรับรายละเอียด ดู[การแก้ไขปัญหาแหล่งข้อมูลที่ไม่รับรองสำหรับการรีเฟรช](service-admin-troubleshoot-unsupported-data-source-for-refresh.md)</span><span class="sxs-lookup"><span data-stu-id="3c43f-119">For details, see [Troubleshooting unsupported data source for refresh](service-admin-troubleshoot-unsupported-data-source-for-refresh.md).</span></span>

## <a name="dashboard-doesnt-reflect-changes-after-refresh"></a><span data-ttu-id="3c43f-120">แดชบอร์ดไม่แสดงการเปลี่ยนแปลงหลังจากรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="3c43f-120">Dashboard doesn't reflect changes after refresh</span></span>

<span data-ttu-id="3c43f-121">โปรดรอประมาณ 10-15 นาทีสำหรับการรีเฟรชเพื่อให้มีผลในไทล์แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="3c43f-121">Please wait about 10-15 minutes for a refresh to be reflected in the dashboard tiles.</span></span> <span data-ttu-id="3c43f-122">ถ้ายังคงไม่ปรากฏขึ้น ให้ปักหมุดการแสดงภาพไปยังแดชบอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="3c43f-122">If it is still not showing up, re-pin the visualization to the dashboard.</span></span>

## <a name="gatewaynotreachable-when-setting-credentials"></a><span data-ttu-id="3c43f-123">GatewayNotReachable เมื่อตั้งค่าข้อมูลประจำตัว</span><span class="sxs-lookup"><span data-stu-id="3c43f-123">GatewayNotReachable when setting credentials</span></span>

<span data-ttu-id="3c43f-124">คุณอาจพบ `GatewayNotReachable` เมื่อพยายามตั้งค่าข้อมูลประจำตัวสำหรับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3c43f-124">You may encounter `GatewayNotReachable` when trying to set credentials for a data source.</span></span> <span data-ttu-id="3c43f-125">ซึ่งอาจเกิดจากเกตเวย์ที่ไม่อัปเดต</span><span class="sxs-lookup"><span data-stu-id="3c43f-125">This can be the result of an outdated gateway.</span></span> <span data-ttu-id="3c43f-126">ติดตั้งเกตเวย์ล่าสุด แล้วลองอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="3c43f-126">Install the latest gateway and try again.</span></span>

## <a name="processing-error-the-following-system-error-occurred-type-mismatch"></a><span data-ttu-id="3c43f-127">ข้อผิดพลาดเกี่ยวกับการประมวลผล: ระบบเกิดข้อผิดพลาดต่อไปนี้: ประเภทไม่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="3c43f-127">Processing Error: The following system error occurred: Type Mismatch</span></span>

<span data-ttu-id="3c43f-128">ซึ่งอาจเป็นปัญหาจากสคริปต์ M ของคุณภายในไฟล์ Power BI Desktop หรือสมุดงาน Excel ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3c43f-128">This could be an issue with your M script within your Power BI Desktop file or Excel workbook.</span></span> <span data-ttu-id="3c43f-129">นอกจากนี้ อาจเกิดจากเวอร์ชัน Power BI Desktop ที่ล้าสมัย</span><span class="sxs-lookup"><span data-stu-id="3c43f-129">It can also be due to an out-of-date Power BI Desktop version.</span></span>

## <a name="tile-refresh-errors"></a><span data-ttu-id="3c43f-130">ข้อผิดพลาดการรีเฟรชไทล์</span><span class="sxs-lookup"><span data-stu-id="3c43f-130">Tile refresh errors</span></span>

<span data-ttu-id="3c43f-131">สำหรับรายการและคำอธิบายของข้อผิดพลาดที่คุณอาจประสบไทล์แดชบอร์ด ดู[แก้ไขปัญหาข้อผิดพลาดไทล์](refresh-troubleshooting-tile-errors.md)</span><span class="sxs-lookup"><span data-stu-id="3c43f-131">For a list of errors you may encounter with dashboard tiles, and explanations, see [Troubleshooting tile errors](refresh-troubleshooting-tile-errors.md).</span></span>

## <a name="refresh-fails-when-updating-data-from-sources-that-use-aad-oauth"></a><span data-ttu-id="3c43f-132">รีเฟรชล้มเหลวเมื่อปรับปรุงข้อมูลจากแหล่งข้อมูลที่ใช้ AAD OAuth</span><span class="sxs-lookup"><span data-stu-id="3c43f-132">Refresh fails when updating data from sources that use AAD OAuth</span></span>

<span data-ttu-id="3c43f-133">โทเค็น OAuth ของ Azure Active Director (**AAD**) ที่ใช้งานโดยแหล่งข้อมูลต่าง ๆ มากมายจะหมดอายุในหนึ่งชั่วโมงโดยประมาณ</span><span class="sxs-lookup"><span data-stu-id="3c43f-133">The Azure Active Directory (**AAD**) OAuth token, used by many different data sources, expires in approximately one hour.</span></span> <span data-ttu-id="3c43f-134">คุณอาจอยู่ในสถานการณ์ที่การโหลดข้อมูลใช้เวลานานกว่าอายุการใช้งานของโทเค็น (มากกว่าหนึ่งชั่วโมง) เนื่องจากบริการ Power BI รอถึงสองชั่วโมงเมื่อโหลดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3c43f-134">You can run into situations where loading data takes longer than the token expiration (more than one hour), since the Power BI service waits for up to two hours when loading data.</span></span> <span data-ttu-id="3c43f-135">ในสถานการณ์เช่นนี้ กระบวนการในการโหลดข้อมูลอาจไม่สำเร้จและมีข้อผิดพลาดข้อมูลประจำตัว</span><span class="sxs-lookup"><span data-stu-id="3c43f-135">In that situation, the data loading process can fail with a credentials error.</span></span>

<span data-ttu-id="3c43f-136">แหล่งข้อมูลที่ใช้ AAD OAuth รวมถึง **Microsoft Dynamics CRM Online**, **SharePoint Online** (SPO) และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="3c43f-136">Data sources that use AAD OAuth include **Microsoft Dynamics CRM Online**, **SharePoint Online** (SPO), and others.</span></span> <span data-ttu-id="3c43f-137">ถ้าคุณกำลังเชื่อมต่อกับแหล่งข้อมูลดังกล่าวและเกิดความล้มเหลวของข้อมูลประจำตัวเมื่อโหลดข้อมูลใช้เวลามากกว่าหนึ่งชั่วโมง นี่อาจเป็นเหตุผล</span><span class="sxs-lookup"><span data-stu-id="3c43f-137">If you’re connecting to such data sources, and get a credentials failure when loading data takes more than an hour, this may be the reason.</span></span>

<span data-ttu-id="3c43f-138">Microsoft กำลังค้นหาโซลูชันที่ช่วยให้กระบวนหารโหลดข้อมูลทำการรีเฟรชโทเค็นและดำเนินต่อ</span><span class="sxs-lookup"><span data-stu-id="3c43f-138">Microsoft is investigating a solution that allows the data loading process to refresh the token and continue.</span></span> <span data-ttu-id="3c43f-139">อย่างไรก็ตาม หากตัวอย่าง Dynamics CRM Online หรือ SharePoint Online ของคุณ (หรือแหล่งข้อมูล AAD OAuth อื่น) มีขนาดใหญ่มากและอาจเข้าในเกณฑ์ค่าต่ำสุดการโหลดข้อมูล 2 ชั่วโมง คุณอาจประสบกับการหมดเวลาการโหลดข้อมูลจากบริการ Power BI ได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="3c43f-139">However, if your Dynamics CRM Online or SharePoint Online instance (or other AAD OAuth data source) is so large that it can run into the two-hour data-load threshold, you may experience a data load timeout from the Power BI service as well.</span></span>

<span data-ttu-id="3c43f-140">นอกจากนี้ โปรดทราบว่าสำหรับรีเฟรชเพื่อให้ทำงานได้อย่างเหมาะสม เมื่อเชื่อมต่อไปยังข้อมูลแหล่ง **SharePoint Online** โดยใช้ AAD OAuth คุณต้องใช้บัญชีเดียวกันกับที่คุณใช้เพื่อลงชื่อเข้าใช้ **บริการ Power BI**</span><span class="sxs-lookup"><span data-stu-id="3c43f-140">Also note that, for refresh to work properly, when connecting to a **SharePoint Online** data source using AAD OAuth, you must use the same account that you use to sign in to the **Power BI service**.</span></span>

## <a name="uncompressed-data-limits-for-refresh"></a><span data-ttu-id="3c43f-141">ขีดจำกัดข้อมูลที่ไม่มีการบีบอัดสำหรับรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="3c43f-141">Uncompressed data limits for refresh</span></span>

<span data-ttu-id="3c43f-142">ขนาดสูงสุดสำหรับชุดข้อมูลที่นำเข้าใน **บริการ Power BI** คือ 1 GB</span><span class="sxs-lookup"><span data-stu-id="3c43f-142">The maximum size for datasets imported into the **Power BI service** is 1 GB.</span></span> <span data-ttu-id="3c43f-143">ชุดข้อมูลเหล่านี้จะถูกบีบอัดเพื่อให้แน่ใจถึงประสิทธิภาพสูงสุดในการทำงาน</span><span class="sxs-lookup"><span data-stu-id="3c43f-143">These datasets are heavily compressed to ensure high performance.</span></span> <span data-ttu-id="3c43f-144">นอกจากนี้ ในความจุที่ใช้ร่วมกัน บริการจะวางขีดจำกัดจำนวนข้อมูลที่ไม่บีบอัดที่มีการประมวลผลในระหว่างการรีเฟรชเเป็น 10 GB</span><span class="sxs-lookup"><span data-stu-id="3c43f-144">In addition, in shared capacity, the service places a limit on the amount of uncompressed data that is processed during refresh to 10 GB.</span></span> <span data-ttu-id="3c43f-145">ซึ่งขั้นตอนนี้จะจำกัดบัญชีผู้ใช้ในการบีบอัด ดังนั้นจึงสูงกว่า 1 GB มาก</span><span class="sxs-lookup"><span data-stu-id="3c43f-145">This limit accounts for the compression, and therefore is much higher than 1 GB.</span></span> <span data-ttu-id="3c43f-146">ชุดข้อมูลใน Power BI Premium ไม่ขึ้นอยู่กับขีดจำกัดนี้</span><span class="sxs-lookup"><span data-stu-id="3c43f-146">Datasets in Power BI Premium are not subject to this limit.</span></span> <span data-ttu-id="3c43f-147">ถ้าการรีเฟรชในบริการ Power BI ล้มเหลวด้วยเหตุผลนี้ โปรดลดปริมาณข้อมูลที่จะนำเข้าไปยัง Power BI และลองอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="3c43f-147">If refresh in the Power BI service fails for this reason, please reduce the amount of data being imported to Power BI and try again.</span></span>

## <a name="scheduled-refresh-timeout"></a><span data-ttu-id="3c43f-148">หมดเวลารีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="3c43f-148">Scheduled refresh timeout</span></span>

<span data-ttu-id="3c43f-149">รีเฟรชตามกำหนดการสำหรับการหมดเวลาของชุดข้อมูลที่นำเข้าหลังจากสองชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="3c43f-149">Scheduled refresh for imported datasets timeout after two hours.</span></span> <span data-ttu-id="3c43f-150">การหมดเวลานี้จะเพิ่มเป็น 5 ชั่วโมงสำหรับชุดข้อมูลในพื้นที่ทำงาน **Premium**</span><span class="sxs-lookup"><span data-stu-id="3c43f-150">This timeout is increased to five hours for datasets in **Premium** workspaces.</span></span> <span data-ttu-id="3c43f-151">ถ้าคุณประสบกับขีดจำกัดนี้อาจต้องพิจารณาลดขนาดหรือความซับซ้อนของชุดข้อมูลของคุณ หรือพิจารณาแบ่งชุดข้อมูลเป็นขนาดที่เล็กลง</span><span class="sxs-lookup"><span data-stu-id="3c43f-151">If you  encounter this limit, consider reducing the size or complexity of your dataset, or consider breaking the dataset into smaller pieces.</span></span>

## <a name="scheduled-refresh-failures"></a><span data-ttu-id="3c43f-152">รีเฟรชตามกำหนดการล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="3c43f-152">Scheduled refresh failures</span></span>

<span data-ttu-id="3c43f-153">ถ้าการรีเฟรชตามกำหนดการล้มเหลวสี่ครั้งติดต่อกัน Power BI จะปิดใช้งานการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="3c43f-153">If a scheduled refresh fails four times in a row, Power BI disables the refresh.</span></span> <span data-ttu-id="3c43f-154">แก้ไขปัญหาพื้นฐาน และจากนั้นจึงเปิดใช้งานการรีเฟรชตามกำหนดการใหม่</span><span class="sxs-lookup"><span data-stu-id="3c43f-154">Address the underlying problem, and then re-enable the scheduled refresh.</span></span>

## <a name="access-to-the-resource-is-forbidden"></a><span data-ttu-id="3c43f-155">การเข้าถึงทรัพยากรถูกห้าม</span><span class="sxs-lookup"><span data-stu-id="3c43f-155">Access to the resource is forbidden</span></span>  

<span data-ttu-id="3c43f-156">ข้อผิดพลาดนี้สามารถเกิดขึ้นเนื่องจากข้อมูลประจำตัวที่แคชไว้หมดอายุแล้ว</span><span class="sxs-lookup"><span data-stu-id="3c43f-156">This error can occur because of expired cached credentials.</span></span> <span data-ttu-id="3c43f-157">ล้างแคชของเบราว์เซอร์อินเทอร์เน็ตของคุณ โดยลงชื่อเข้าใช้ Power BI แล้วไปที่ `https://app.powerbi.com?alwaysPromptForContentProviderCreds=true`</span><span class="sxs-lookup"><span data-stu-id="3c43f-157">Clear your internet browser cache by going signing into Power BI and going to `https://app.powerbi.com?alwaysPromptForContentProviderCreds=true`.</span></span> <span data-ttu-id="3c43f-158">ซึ่งเป็นการบังคับการปรับปรุงข้อมูลประจำตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="3c43f-158">This forces an update of your credentials.</span></span>

## <a name="data-refresh-failure-because-of-password-change-or-expired-credentials"></a><span data-ttu-id="3c43f-159">การรีเฟรชข้อมูลล้มเหลวเนื่องจากการเปลี่ยนรหัสผ่าน หรือข้อมูลประจำตัวที่หมดอายุ</span><span class="sxs-lookup"><span data-stu-id="3c43f-159">Data refresh failure because of password change or expired credentials</span></span>

<span data-ttu-id="3c43f-160">การรีเฟรชข้อมูลอาจล้มเหลวเนื่องจากข้อมูลประจำตัวที่แคชไว้หมดอายุแล้ว</span><span class="sxs-lookup"><span data-stu-id="3c43f-160">Data refresh can also fail due to expired cached credentials.</span></span> <span data-ttu-id="3c43f-161">ล้างแคชของเบราว์เซอร์อินเทอร์เน็ตของคุณ โดยลงชื่อเข้าใช้ Power BI แล้วไปที่ `https://app.powerbi.com?alwaysPromptForContentProviderCreds=true`</span><span class="sxs-lookup"><span data-stu-id="3c43f-161">Clear your internet browser cache by going signing into Power BI and going to `https://app.powerbi.com?alwaysPromptForContentProviderCreds=true`.</span></span> <span data-ttu-id="3c43f-162">ซึ่งเป็นการบังคับการปรับปรุงข้อมูลประจำตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="3c43f-162">This forces an update of your credentials.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3c43f-163">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3c43f-163">Next steps</span></span>

- [<span data-ttu-id="3c43f-164">การรีเฟรชข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3c43f-164">Data refresh in Power BI</span></span>](refresh-data.md)  
- [<span data-ttu-id="3c43f-165">การแก้ไขปัญหาเกตเวย์ข้อมูลในองค์กร</span><span class="sxs-lookup"><span data-stu-id="3c43f-165">Troubleshooting the On-premises data gateway</span></span>](service-gateway-onprem-tshoot.md)  
- [<span data-ttu-id="3c43f-166">แก้ไขปัญหาเกตเวย์ Power BI - ส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="3c43f-166">Troubleshooting the Power BI Gateway - Personal</span></span>](service-admin-troubleshooting-power-bi-personal-gateway.md)  

<span data-ttu-id="3c43f-167">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3c43f-167">More questions?</span></span> [<span data-ttu-id="3c43f-168">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="3c43f-168">Try asking the Microsoft Power BI Community</span></span>](https://community.powerbi.com/)
