---
title: เชื่อมต่อกับเมตริกความจุ Power BI Premium
description: วิธีการรับและติดตั้งแอปแบบเทมเพลต Power BI Premium และวิธีการเชื่อมต่อกับข้อมูล
author: paulinbar
ms.author: painbar
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: how-to
ms.date: 05/18/2020
LocalizationGroup: Connect to services
ms.openlocfilehash: f7bb6cdd3279ac15b2952d5e20b9c36a66a0c518
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410608"
---
# <a name="connect-to-power-bi-premium-capacity-metrics"></a><span data-ttu-id="38aa2-103">เชื่อมต่อกับเมตริกความจุ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="38aa2-103">Connect to Power BI Premium Capacity Metrics</span></span>

<span data-ttu-id="38aa2-104">การตรวจสอบความจุของคุณเป็นสิ่งสำคัญในการตัดสินใจอย่างชาญฉลาดว่าจะใช้ทรัพยากรความจุ Premium ของคุณให้ดีที่สุดได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="38aa2-104">Monitoring your capacities is essential to making informed decisions on how best to utilize your Premium capacity resources.</span></span> <span data-ttu-id="38aa2-105">แอปเมตริกความจุ Power BI Premium มีข้อมูลเชิงลึกมากที่สุดเกี่ยวกับวิธีการใช้งานความจุของคุณ</span><span class="sxs-lookup"><span data-stu-id="38aa2-105">The Power BI Premium Capacity Metrics app provides the most in-depth information into how your capacities are performing.</span></span>

![รายงานของแอปเมตริกความจุ Power BI Premium](media/service-connect-to-pbi-premium-capacity-metrics/service-pbi-premium-capacity-metrics-app-report.png)

<span data-ttu-id="38aa2-107">บทความนี้จะแจ้งวิธีการติดตั้งแอปและการเชื่อมต่อกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="38aa2-107">This article describes how to install the app and connect to data sources.</span></span> <span data-ttu-id="38aa2-108">สำหรับข้อมูลเกี่ยวกับเนื้อหาของรายงานและวิธีการใช้งาน ดู [ตรวจสอบความจุ Premium ด้วยแอป](../admin/service-admin-premium-monitor-capacity.md)และ [บล็อกโพสต์ของแอปเมตริกความจุ Power BI Premium](https://powerbi.microsoft.com/blog/premium-capacity-metrics-app-new-health-center-with-kpis-to-explore-relevant-metrics-and-steps-to-mitigate-issues/)</span><span class="sxs-lookup"><span data-stu-id="38aa2-108">For information about the contents of the report and how to use it, see [Monitor Premium capacities with the app](../admin/service-admin-premium-monitor-capacity.md), and the [Premium Capacity Metrics app blog post](https://powerbi.microsoft.com/blog/premium-capacity-metrics-app-new-health-center-with-kpis-to-explore-relevant-metrics-and-steps-to-mitigate-issues/).</span></span>

<span data-ttu-id="38aa2-109">หลังจากที่คุณได้ติดตั้งแอปและเชื่อมต่อกับแหล่งข้อมูลแล้ว คุณสามารถปรับแต่งรายงานได้ตามความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="38aa2-109">After you've installed the app and connected to the data sources, you can customize the report as per your needs.</span></span> <span data-ttu-id="38aa2-110">จากนั้นคุณจะสามารถเผยแพร่รายงานให้กับเพื่อนร่วมงานในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="38aa2-110">You can then distribute it to colleagues in your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="38aa2-111">การติดตั้งแอปเทมเพลตจำเป็นต้องใช้[สิทธิ์](./service-template-apps-install-distribute.md#prerequisites)</span><span class="sxs-lookup"><span data-stu-id="38aa2-111">Installing template apps requires [permissions](./service-template-apps-install-distribute.md#prerequisites).</span></span> <span data-ttu-id="38aa2-112">ติดต่อผู้ดูแลระบบ Power BI ของคุณ ถ้าคุณพบว่าคุณไม่มีสิทธิ์เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="38aa2-112">Contact your Power BI admin if you find you don't have sufficient permissions.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="38aa2-113">ติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="38aa2-113">Install the app</span></span>

1. <span data-ttu-id="38aa2-114">คลิกที่ลิงก์ต่อไปนี้เพื่อเข้าถึงแอป: [แอปเทมเพลตเมตริกความจุ Power BI Premium](https://app.powerbi.com/groups/me/getapps/services/pbi_pcmm.capacity-metrics-dxt)</span><span class="sxs-lookup"><span data-stu-id="38aa2-114">Click the following link to get to the app: [Power BI Premium Capacity Metrics template app](https://app.powerbi.com/groups/me/getapps/services/pbi_pcmm.capacity-metrics-dxt)</span></span>

1. <span data-ttu-id="38aa2-115">บนหน้า AppSource สำหรับแอป ให้เลือก [**รับทันที**](https://app.powerbi.com/groups/me/getapps/services/pbi_pcmm.capacity-metrics-dxt)</span><span class="sxs-lookup"><span data-stu-id="38aa2-115">On the AppSource page for the app, select [**GET IT NOW**](https://app.powerbi.com/groups/me/getapps/services/pbi_pcmm.capacity-metrics-dxt).</span></span>

    <span data-ttu-id="38aa2-116">[![แอปเมตริกความจุ Power BI Premium ใน AppSource](media/service-connect-to-pbi-premium-capacity-metrics/service-pbi-premium-capacity-metrics-app-appsource-get-it-now.png)](https://app.powerbi.com/groups/me/getapps/services/pbi_pcmm.capacity-metrics-dxt)</span><span class="sxs-lookup"><span data-stu-id="38aa2-116">[![Power BI Premium Capacity Metrics app in AppSource](media/service-connect-to-pbi-premium-capacity-metrics/service-pbi-premium-capacity-metrics-app-appsource-get-it-now.png)](https://app.powerbi.com/groups/me/getapps/services/pbi_pcmm.capacity-metrics-dxt)</span></span>

1. <span data-ttu-id="38aa2-117">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="38aa2-117">Select **Install**.</span></span> 

    ![ติดตั้งแอปเมตริกความจุ Power BI Premium](media/service-connect-to-pbi-premium-capacity-metrics/service-pbi-premium-capacity-metric-select-install.png)

    > [!NOTE]
    > <span data-ttu-id="38aa2-119">ถ้าคุณได้ติดตั้งแอปก่อนหน้านี้แล้ว คุณจะถูกถามว่าคุณต้องการ [เขียนทับการติดตั้ง](./service-template-apps-install-distribute.md#update-a-template-app) หรือติดตั้งไปยังพื้นที่ทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="38aa2-119">If you've installed the app previously, you will be asked whether you want to [overwrite that installation](./service-template-apps-install-distribute.md#update-a-template-app) or install to a new workspace.</span></span>

    <span data-ttu-id="38aa2-120">หลังจากที่ติดตั้งแอปแล้ว คุณจะเห็นแอปบนหน้าแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="38aa2-120">Once the app has installed, you see it on your Apps page.</span></span>

   ![แอปเมตริกความจุ Power BI Premium บนหน้าแอป](media/service-connect-to-pbi-premium-capacity-metrics/service-pbi-premium-capacity-metrics-app-apps-page-icon.png)

## <a name="connect-to-data-sources"></a><span data-ttu-id="38aa2-122">เชื่อมต่อกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="38aa2-122">Connect to data sources</span></span>

1. <span data-ttu-id="38aa2-123">เลือกไอคอนบนหน้าแอปของคุณเพื่อเปิดแอป</span><span class="sxs-lookup"><span data-stu-id="38aa2-123">Select the icon on your Apps page to open the app.</span></span>

1. <span data-ttu-id="38aa2-124">บนหน้าจอเริ่มต้น เลือก **สำรวจ**</span><span class="sxs-lookup"><span data-stu-id="38aa2-124">On the splash screen, select **Explore**.</span></span>

   ![หน้าจอเริ่มต้นของแอปเทมเพลต](media/service-connect-to-pbi-premium-capacity-metrics/service-pbi-premium-capacity-metrics-app-splash-screen.png)

   <span data-ttu-id="38aa2-126">แอปจะเปิดขึ้นและแสดงข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="38aa2-126">The app opens, showing sample data.</span></span>

1. <span data-ttu-id="38aa2-127">เลือกลิงก์ **เชื่อมต่อข้อมูลของคุณ** บนแบนเนอร์ที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="38aa2-127">Select the **Connect your data** link on the banner at the top of the page.</span></span>

   ![แอปเมตริกความจุ Power BI Premium จะเชื่อมต่อลิงก์ข้อมูลของคุณ](media/service-connect-to-pbi-premium-capacity-metrics/service-pbi-premium-capacity-metrics-app-connect-data.png)

1. <span data-ttu-id="38aa2-129">ในกล่องโต้ตอบที่ปรากฏขึ้น ให้ตั้งค่าออฟเซต UTC นั่นคือความแตกต่างของชั่วโมงระหว่างเวลามาตรฐานสากลและเวลาในตำแหน่งที่ตั้งของคุณ</span><span class="sxs-lookup"><span data-stu-id="38aa2-129">In the dialog box that appears, set the UTC offset, that is, the difference in hours between Coordinated Universal Time and the time in your location.</span></span> <span data-ttu-id="38aa2-130">จากนั้น คลิก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="38aa2-130">Then click **Next**.</span></span>
  
   <span data-ttu-id="38aa2-131">![กล่องโต้ตอบ UTC ของชุดแอปเมตริกความจุ Power BI Premium](media/service-connect-to-pbi-premium-capacity-metrics/service-pbi-premium-capacity-metrics-app-setutc-dialog.png)
   **หมายเหตุ: รูปแบบสำหรับครึ่งชั่วโมงควรเป็นทศนิยม (ตัวอย่างเช่น 5.5, 2.5, ฯลฯ)**</span><span class="sxs-lookup"><span data-stu-id="38aa2-131">![Power BI Premium Capacity Metrics app set UTC dialog](media/service-connect-to-pbi-premium-capacity-metrics/service-pbi-premium-capacity-metrics-app-setutc-dialog.png)
**Note: The format for half hours should be decimal (for example, 5.5, 2.5, etc.).**</span></span>

1. <span data-ttu-id="38aa2-132">ในกล่องโต้ตอบถัดไปที่ปรากฏขึ้น คุณไม่จำเป็นต้องทำอะไร</span><span class="sxs-lookup"><span data-stu-id="38aa2-132">In the next dialog that appears, you don't have to do anything.</span></span> <span data-ttu-id="38aa2-133">เพียงแค่เลือก **ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="38aa2-133">Just select **Sign in**.</span></span>

   ![กล่องโต้ตอบการตรวจสอบสิทธิ์ของแอปเมตริกความจุ Power BI Premium](media/service-connect-to-pbi-premium-capacity-metrics/service-pbi-premium-capacity-metrics-app-authentication-dialog.png)

1. <span data-ttu-id="38aa2-135">ที่หน้าจอลงชื่อเข้าใช้ของ Microsoft ใหลงชื่อเข้าใช้ Power BI</span><span class="sxs-lookup"><span data-stu-id="38aa2-135">At the Microsoft sign-in screen, sign in to Power BI.</span></span>

   ![หน้าจอลงชื่อเข้าใช้ของ Microsoft](media/service-connect-to-pbi-premium-capacity-metrics/service-pbi-premium-capacity-metrics-app-microsoft-login.png)

   <span data-ttu-id="38aa2-137">หลังจากที่คุณลงชื่อเข้าใช้แล้ว รายงานจะเชื่อมต่อเข้ากับแหล่งข้อมูลและจะได้รับข้อมูลล่าสุด</span><span class="sxs-lookup"><span data-stu-id="38aa2-137">After you've signed in, the report connects to the data sources and is populated with up-to-date data.</span></span> <span data-ttu-id="38aa2-138">ในช่วงเวลานี้ ตัวตรวจสอบกิจกรรมจะเปิดทำงาน</span><span class="sxs-lookup"><span data-stu-id="38aa2-138">During this time, the activity monitor turns.</span></span>

   ![กำลังดำเนินการรีเฟรชแอปเมตริกความจุ Power BI Premium](media/service-connect-to-pbi-premium-capacity-metrics/service-pbi-premium-capacity-metrics-app-refresh-monitor.png)

   <span data-ttu-id="38aa2-140">ข้อมูลรายงานของคุณจะรีเฟรชโดยอัตโนมัติหนึ่งครั้งต่อวัน เว้นแต่ว่าคุณจะปิดใช้งานการดำเนินการนี้ในระหว่างกระบวนการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="38aa2-140">Your report data will automatically refresh once a day, unless you disabled this during the sign-in process.</span></span> <span data-ttu-id="38aa2-141">นอกจากนี้ คุณยังสามารถ [ตั้งค่าตารางเวลาการรีเฟรชของคุณเอง](./refresh-scheduled-refresh.md) เพื่อรักษาข้อมูลรายงานให้เป็นปัจจุบันหากคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="38aa2-141">You can also [set up your own refresh schedule](./refresh-scheduled-refresh.md) to keep the report data up to date if you so desire.</span></span>

## <a name="customize-and-share"></a><span data-ttu-id="38aa2-142">ปรับแต่งตามความต้องการและแชร์</span><span class="sxs-lookup"><span data-stu-id="38aa2-142">Customize and share</span></span>

<span data-ttu-id="38aa2-143">เมื่อต้องการเริ่มต้นการปรับแต่งแอปตามความต้องการ ให้คลิกที่ไอคอนรูปดินสอในมุมบนขวา</span><span class="sxs-lookup"><span data-stu-id="38aa2-143">To start customizing the app, click the pencil icon in the upper right corner.</span></span>

 ![ไอคอน แก้ไข](media/service-connect-to-pbi-premium-capacity-metrics/service-pbi-premium-capacity-metrics-app-customize.png)

<span data-ttu-id="38aa2-145">คุณสามารถดูรายละเอียดได้ที่[ปรับแต่งและแชร์แอป](./service-template-apps-install-distribute.md#customize-and-share-the-app)</span><span class="sxs-lookup"><span data-stu-id="38aa2-145">See [Customize and share the app](./service-template-apps-install-distribute.md#customize-and-share-the-app) for details.</span></span>

## <a name="next-steps"></a><span data-ttu-id="38aa2-146">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="38aa2-146">Next steps</span></span>
* [<span data-ttu-id="38aa2-147">ตรวจสอบความจุ Premium ด้วยแอป</span><span class="sxs-lookup"><span data-stu-id="38aa2-147">Monitor Premium capacities with the app</span></span>](../admin/service-admin-premium-monitor-capacity.md)
* [<span data-ttu-id="38aa2-148">บล็อกโพสต์ของแอปเมตริกความจุ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="38aa2-148">Premium Capacity Metrics app blog post</span></span>](https://powerbi.microsoft.com/blog/premium-capacity-metrics-app-new-health-center-with-kpis-to-explore-relevant-metrics-and-steps-to-mitigate-issues/)
* [<span data-ttu-id="38aa2-149">แอปเทมเพลต Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="38aa2-149">What are Power BI template apps?</span></span>](./service-template-apps-overview.md)
* [<span data-ttu-id="38aa2-150">ติดตั้งและแจกจ่ายแอปเทมเพลตในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="38aa2-150">Install and distribute template apps in your organization</span></span>](./service-template-apps-install-distribute.md)
* <span data-ttu-id="38aa2-151">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="38aa2-151">Questions?</span></span> [<span data-ttu-id="38aa2-152">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="38aa2-152">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)