---
title: การเชื่อมต่อรายงานการติดตาม COVID-19 ในสหรัฐอเมริกา
description: วิธีการรับและติดตั้งแอปเทมเพลตของเคส COVID-19 และวิธีการเชื่อมต่อกับข้อมูล
author: paulinbar
ms.author: painbar
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: how-to
ms.date: 04/05/2020
LocalizationGroup: Connect to services
ms.openlocfilehash: fc421f7635a3d6e3b2336d5bce081d7914c0fad5
ms.sourcegitcommit: 8250187368d3de48663eb516a816ff701119b579
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/10/2020
ms.locfileid: "96998875"
---
# <a name="connect-to-the-covid-19-us-tracking-report"></a><span data-ttu-id="8beed-103">การเชื่อมต่อรายงานการติดตาม COVID-19 ในสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="8beed-103">Connect to the COVID-19 US tracking report</span></span>
<span data-ttu-id="8beed-104">บทความนี้จะแจ้งวิธีการติดตั้งแอปเทมเพลตสำหรับรายงานการติดตาม COVID-19 และวิธีการเชื่อมต่อกับแหล่งข้อมูลให้คุณทราบ</span><span class="sxs-lookup"><span data-stu-id="8beed-104">This article tells  you how to install the template app for the COVID-19 tracking report, and how to connect to the data sources.</span></span>

![รายงานการติดตาม COVID-19 ในสหรัฐอเมริกา](media/service-connect-to-covid-19-tracking/service-covid-19-us-tracking-report-title-screen.png)

<span data-ttu-id="8beed-106">สำหรับข้อมูลโดยละเอียดเกี่ยวกับตัวรายงาน รวมถึงการปฏิเสธความรับผิดชอบและข้อมูลเกี่ยวกับข้อมูล โปรดศึกษาจาก[ตัวอย่างการติดตาม COVID-19 ของรัฐแห่งสหรัฐอเมริกาและรัฐบาลท้องถิ่น](../create-reports/sample-covid-19-us.md)</span><span class="sxs-lookup"><span data-stu-id="8beed-106">For detailed information about the report itself, including disclaimers and information about the data, see [COVID-19 tracking sample for US state and local governments](../create-reports/sample-covid-19-us.md).</span></span>

<span data-ttu-id="8beed-107">หลังจากที่คุณได้ติดตั้งแอปเทมเพลตและเชื่อมต่อกับแหล่งข้อมูลแล้ว คุณสามารถปรับแต่งรายงานได้ตามความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="8beed-107">After you've installed the template app and connected to the data sources, you can customize the report as per your needs.</span></span> <span data-ttu-id="8beed-108">จากนั้นคุณจะสามารถเผยแพร่รายงานออกเป็นแอปให้กับเพื่อนร่วมงานในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="8beed-108">You can then distribute it as an app to colleagues in your organization.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="8beed-109">ติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="8beed-109">Install the app</span></span>

1. <span data-ttu-id="8beed-110">คลิกที่ลิงก์ต่อไปนี้เพื่อเข้าถึงแอป: [แอปเทมเพลตรายงานการติดตาม COVID-19 ในสหรัฐอเมริกา](https://app.powerbi.com/groups/me/getapps/services/pbi-contentpacks.covid19ms)</span><span class="sxs-lookup"><span data-stu-id="8beed-110">Click the following link to get to the app: [COVID-19 US Tracking Report template app](https://app.powerbi.com/groups/me/getapps/services/pbi-contentpacks.covid19ms)</span></span>

1. <span data-ttu-id="8beed-111">เมื่อคุณอยู่ในหน้า AppSource ของแอป ให้คลิกที่ [**รับทันที**](https://app.powerbi.com/groups/me/getapps/services/pbi-contentpacks.covid19ms)</span><span class="sxs-lookup"><span data-stu-id="8beed-111">Once you're on the App's AppSource page, click [**GET IT NOW**](https://app.powerbi.com/groups/me/getapps/services/pbi-contentpacks.covid19ms).</span></span>

    <span data-ttu-id="8beed-112">[![รายงานการติดตามข้อมูลเกี่ยวกับโควิด 19 ที่สหรัฐอเมริกาใน AppSource](media/service-connect-to-covid-19-tracking/service-covid-19-us-tracking-report-appsource-icon.png)](https://app.powerbi.com/groups/me/getapps/services/pbi-contentpacks.covid19ms)</span><span class="sxs-lookup"><span data-stu-id="8beed-112">[![Covid-19 US Tracking Report in AppSource](media/service-connect-to-covid-19-tracking/service-covid-19-us-tracking-report-appsource-icon.png)](https://app.powerbi.com/groups/me/getapps/services/pbi-contentpacks.covid19ms)</span></span>

1. <span data-ttu-id="8beed-113">เมื่อมีข้อความแสดงขึ้น ให้คลิก **Install**</span><span class="sxs-lookup"><span data-stu-id="8beed-113">When prompted , click **Install**.</span></span> <span data-ttu-id="8beed-114">หลังจากที่ติดตั้งแอปแล้ว คุณจะเห็นแอปบนหน้าแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="8beed-114">Once the app has installed, you will see it on your Apps page.</span></span>

   ![รายงานการติดตาม COVID-19 ในสหรัฐอเมริกาบนหน้าแอป](media/service-connect-to-covid-19-tracking/service-covid-19-us-tracking-report-apps-page-icon.png)

## <a name="connect-to-data-sources"></a><span data-ttu-id="8beed-116">เชื่อมต่อกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8beed-116">Connect to data sources</span></span>

1. <span data-ttu-id="8beed-117">คลิกที่ไอคอนบนหน้าแอปของคุณเพื่อเปิดแอป</span><span class="sxs-lookup"><span data-stu-id="8beed-117">Click the icon on your Apps page to open the app.</span></span> <span data-ttu-id="8beed-118">แอปจะเปิดขึ้นและแสดงข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8beed-118">The app opens, showing sample data.</span></span>

1. <span data-ttu-id="8beed-119">เลือกลิงก์ **เชื่อมต่อข้อมูลของคุณ** บนแบนเนอร์ที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="8beed-119">Select the **Connect your data** link on the banner at the top of the page.</span></span>

   ![แอป GitHub เชื่อมโยงลิงก์ข้อมูลของคุณ](media/service-connect-to-covid-19-tracking/power-bi-covid-19-connect-data.png)

1. <span data-ttu-id="8beed-121">กล่องโต้ตอบพารามิเตอร์จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="8beed-121">The parameters dialog will appear.</span></span> <span data-ttu-id="8beed-122">ไม่มีพารามิเตอร์ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="8beed-122">There are no required parameters.</span></span> <span data-ttu-id="8beed-123">คลิก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="8beed-123">Click **Next**.</span></span>

   ![สกรีนช็อตของกล่องโต้ตอบพารามิเตอร์รายงานการติดตาม Covid-19 ในสหรัฐอเมริกา](media/service-connect-to-covid-19-tracking/service-covid-19-us-tracking-report-parameters-dialog.png)

1. <span data-ttu-id="8beed-125">กล่องโต้ตอบวิธีการรับรองความถูกต้องจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="8beed-125">The authentication method dialog will appear.</span></span> <span data-ttu-id="8beed-126">ระบบจะแสดงค่าที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="8beed-126">Recommended values are prepopulated.</span></span> <span data-ttu-id="8beed-127">อย่าเปลี่ยนแปลงข้อมูลเหล่านี ้เว้นแต่ว่าคุณมีความรู้เฉพาะเกี่ยวกับค่าต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="8beed-127">Don't change these unless you have specific knowledge of different values.</span></span>

    <span data-ttu-id="8beed-128">คลิก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="8beed-128">Click **Next**.</span></span>

   ![สกรีนช็อตของกล่องโต้ตอบการรับรองความถูกต้องรายงานการติดตาม Covid-19 ในสหรัฐอเมริกา](media/service-connect-to-covid-19-tracking/service-covid-19-us-tracking-report-authentication-dialog.png)

1. <span data-ttu-id="8beed-130">คลิก **ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="8beed-130">Click **Sign in**.</span></span>

   ![สกรีนช็อตของกล่องโต้ตอบลงชื่อเข้าใช้รายงานการติดตาม Covid-19 ในสหรัฐอเมริกา](media/service-connect-to-covid-19-tracking/service-covid-19-us-tracking-report-signin-dialog.png)
 
   <span data-ttu-id="8beed-132">รายงานจะเชื่อมต่อกับแหล่งข้อมูล ซึ่งจะมีข้อมูลล่าสุดแจ้งเข้าไปอยู่เสมอ</span><span class="sxs-lookup"><span data-stu-id="8beed-132">The report will connect to the data sources and be populated with up-to-date data.</span></span> <span data-ttu-id="8beed-133">ในช่วงเวลานี้ คุณจะเห็นข้อมูลตัวอย่างและการรีเฟรชกำลังดำเนินการอยู่</span><span class="sxs-lookup"><span data-stu-id="8beed-133">During this time you will see sample data and that refresh is in progress.</span></span>

   ![กำลังรีเฟรชรายงานการติดตาม COVID-19 ในสหรัฐอเมริกา](media/service-connect-to-covid-19-tracking/service-covid-19-us-tracking-report-refresh-monitor.png)

## <a name="schedule-report-refresh"></a><span data-ttu-id="8beed-135">กำหนดเวลาการรีเฟรชรายงาน</span><span class="sxs-lookup"><span data-stu-id="8beed-135">Schedule report refresh</span></span>

<span data-ttu-id="8beed-136">เมื่อการรีเฟรชข้อมูลเสร็จสมบูรณ์ คุณจะอยู่ในพื้นที่ทำงานที่เชื่อมโยงกับแอป</span><span class="sxs-lookup"><span data-stu-id="8beed-136">When the data refresh has completed, you will be in the workspace associated with the app.</span></span> <span data-ttu-id="8beed-137">[ตั้งค่ากำหนดเวลาการรีเฟรช](../connect-data/refresh-scheduled-refresh.md)เพื่อให้ข้อมูลรายงานเป็นข้อมูลล่าสุดอยู่เสมอ</span><span class="sxs-lookup"><span data-stu-id="8beed-137">[Set up a refresh schedule](../connect-data/refresh-scheduled-refresh.md) to keep the report data up to date.</span></span>

## <a name="customize-and-share"></a><span data-ttu-id="8beed-138">ปรับแต่งตามความต้องการและแชร์</span><span class="sxs-lookup"><span data-stu-id="8beed-138">Customize and share</span></span>

<span data-ttu-id="8beed-139">คุณสามารถดูรายละเอียดได้ที่[ปรับแต่งและแชร์แอป](../connect-data/service-template-apps-install-distribute.md#customize-and-share-the-app)</span><span class="sxs-lookup"><span data-stu-id="8beed-139">See [Customize and share the app](../connect-data/service-template-apps-install-distribute.md#customize-and-share-the-app) for details.</span></span> <span data-ttu-id="8beed-140">ตรวจสอบให้มั่นใจว่าคุณได้อ่าน[ข้อความปฏิเสธความรับผิดชอบของรายงาน](../create-reports/sample-covid-19-us.md#disclaimers)ก่อนที่จะเผยแพร่หรือแจกจ่ายแอป</span><span class="sxs-lookup"><span data-stu-id="8beed-140">Be sure to review the [report disclaimers](../create-reports/sample-covid-19-us.md#disclaimers) before publishing or distributing the app.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8beed-141">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="8beed-141">Next steps</span></span>
* [<span data-ttu-id="8beed-142">ตัวอย่างการติดตาม COVID-19 สำหรับรัฐของสหรัฐอเมริกาและรัฐบาลในท้องถิ่น</span><span class="sxs-lookup"><span data-stu-id="8beed-142">COVID-19 tracking sample for US state and local governments</span></span>](../create-reports/sample-covid-19-us.md)
* <span data-ttu-id="8beed-143">มีคำถามหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="8beed-143">Questions?</span></span> [<span data-ttu-id="8beed-144">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="8beed-144">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
* [<span data-ttu-id="8beed-145">แอปเทมเพลต Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="8beed-145">What are Power BI template apps?</span></span>](../connect-data/service-template-apps-overview.md)
* [<span data-ttu-id="8beed-146">ติดตั้งและแจกจ่ายแอปเทมเพลตในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="8beed-146">Install and distribute template apps in your organization</span></span>](../connect-data/service-template-apps-install-distribute.md)
