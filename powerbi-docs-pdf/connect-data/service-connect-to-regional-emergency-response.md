---
title: เชื่อมต่อไปยังแดชบอร์ดการตอบสนองเหตุฉุกเฉินในระดับภูมิภาค
description: วิธีการรับและติดตั้งแดชบอร์ดการสนับสนุนการตัดสินใจของ COVID-19 สำหรับแอปเทมเพลตการตอบสนองเหตุฉุกเฉินในระดับภูมิภาคและวิธีการเชื่อมต่อกับข้อมูล
author: paulinbar
ms.author: painbar
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: how-to
ms.date: 04/24/2020
LocalizationGroup: Connect to services
ms.openlocfilehash: b8cb2be15d084bba3fc2a70152165ce3b2909dab
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410562"
---
# <a name="connect-to-the-regional-emergency-response-dashboard"></a><span data-ttu-id="d3cc5-103">เชื่อมต่อไปยังแดชบอร์ดการตอบสนองเหตุฉุกเฉินในระดับภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="d3cc5-103">Connect to the Regional Emergency Response Dashboard</span></span>
<span data-ttu-id="d3cc5-104">แดชบอร์ดการตอบสนองเหตุฉุกเฉินในระดับภูมิภาคคือคอมโพเนนต์รายงานของ[โซลูชันการตอบสนองเหตุฉุกเฉินของ Microsoft Power Platform](/powerapps/sample-apps/regional-emergency-response/overview)</span><span class="sxs-lookup"><span data-stu-id="d3cc5-104">The Regional Emergency Response Dashboard is the reporting component of the [Microsoft Power Platform Regional Emergency Response solution](/powerapps/sample-apps/regional-emergency-response/overview).</span></span> <span data-ttu-id="d3cc5-105">ผู้ดูแลระบบระดับภูมิภาคสามารถดูแดชบอร์ดในผู้เช่า Power BI ของตน เพื่อให้พวกเขาสามารถดูข้อมูลและเมตริกที่สำคัญที่จะช่วยให้พวกเขาตัดสินใจได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="d3cc5-105">Regional organization admins can view the dashboard in their Power BI tenant, enabling them to quickly view important data and metrics that will help them make efficient decisions.</span></span>

![รายงานของแอปแดชบอร์ดการตอบสนองเหตุฉุกเฉินในระดับภูมิภาค](media/service-connect-to-regional-emergency-response/service-regional-emergency-response-app-report.png)

<span data-ttu-id="d3cc5-107">บทความนี้บอกวิธีการติดตั้งแอปการตอบสนองเหตุฉุกเฉินในระดับภูมิภาคโดยใช้แอปแดชบอร์ดการตอบสนองเหตุฉุกเฉินในระดับภูมิภาคและวิธีการเชื่อมต่อกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d3cc5-107">This article tells  you how to install the Regional Emergency Response app using the Regional Emergency Response Dashboard template app, and how to connect to the data sources.</span></span>

<span data-ttu-id="d3cc5-108">สำหรับข้อมูลโดยละเอียดเกี่ยวกับสิ่งที่แสดงในแดชบอร์ด โปรดดู [รับข้อมูลเชิงลึก](/powerapps/sample-apps/regional-emergency-response/portals-admin-reporting#get-insights)</span><span class="sxs-lookup"><span data-stu-id="d3cc5-108">For detailed information about what is presented in the dashboard, see [Get insights](/powerapps/sample-apps/regional-emergency-response/portals-admin-reporting#get-insights).</span></span>

<span data-ttu-id="d3cc5-109">หลังจากที่คุณได้ติดตั้งแอปเทมเพลตและเชื่อมต่อกับแหล่งข้อมูลแล้ว คุณสามารถปรับแต่งรายงานได้ตามความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="d3cc5-109">After you've installed the template app and connected to the data sources, you can customize the report as per your needs.</span></span> <span data-ttu-id="d3cc5-110">จากนั้นคุณจะสามารถเผยแพร่รายงานออกเป็นแอปให้กับเพื่อนร่วมงานในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="d3cc5-110">You can then distribute it as an app to colleagues in your organization.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d3cc5-111">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="d3cc5-111">Prerequisites</span></span>

<span data-ttu-id="d3cc5-112">ก่อนที่จะติดตั้งแอปเทมเพลตนี้ คุณต้องติดตั้งและตั้งค่า[โซลูชันการตอบสนองเหตุฉุกเฉินในระดับภูมิภาค](/powerapps/sample-apps/regional-emergency-response/deploy)ก่อน</span><span class="sxs-lookup"><span data-stu-id="d3cc5-112">Before installing this template app, you must first install and set up the [Regional Emergency Response solution](/powerapps/sample-apps/regional-emergency-response/deploy).</span></span> <span data-ttu-id="d3cc5-113">การติดตั้งโซลูชันนี้จะสร้างการอ้างอิงแหล่งข้อมูลที่จำเป็นเพื่อป้อนข้อมูลลงในแอป</span><span class="sxs-lookup"><span data-stu-id="d3cc5-113">Installing this solution creates the datasource references necessary to populate the app with data.</span></span>

<span data-ttu-id="d3cc5-114">เมื่อทำการติดตั้งโซลูชันการตอบสนองเหตุฉุกเฉินในระดับภูมิภาคแล้ว ให้จดบันทึก [URL ของสภาพแวดล้อมอินสแตนซ์ Common Data Service ของคุณ](/powerapps/sample-apps/regional-emergency-response/deploy#step-5-configure-and-publish-power-bi-dashboard)เอาไว้</span><span class="sxs-lookup"><span data-stu-id="d3cc5-114">When installing Regional Emergency Response solution, take note of the [URL of your Common Data Service environment instance](/powerapps/sample-apps/regional-emergency-response/deploy#step-5-configure-and-publish-power-bi-dashboard).</span></span> <span data-ttu-id="d3cc5-115">คุณจะต้องใช้ข้อมูลนี้เพื่อเชื่อมต่อแอปเทมเพลตเข้ากับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d3cc5-115">You will need it to connect the template app to the data.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="d3cc5-116">ติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="d3cc5-116">Install the app</span></span>

1. <span data-ttu-id="d3cc5-117">คลิกที่ลิงก์ต่อไปนี้เพื่อเข้าถึงแอป: [แอปแดชบอร์ดการตอบสนองเหตุฉุกเฉินในระดับภูมิภาค](https://appsource.microsoft.com/product/power-bi/powerapps_cxo.regional_response)</span><span class="sxs-lookup"><span data-stu-id="d3cc5-117">Click the following link to get to the app: [Regional Emergency Response Dashboard template app](https://appsource.microsoft.com/product/power-bi/powerapps_cxo.regional_response)</span></span>

1. <span data-ttu-id="d3cc5-118">บนหน้า AppSource สำหรับแอป ให้เลือก [**รับทันที**](https://appsource.microsoft.com/product/power-bi/powerapps_cxo.regional_response)</span><span class="sxs-lookup"><span data-stu-id="d3cc5-118">On the AppSource page for the app, select [**GET IT NOW**](https://appsource.microsoft.com/product/power-bi/powerapps_cxo.regional_response).</span></span>

    <span data-ttu-id="d3cc5-119">[![แอปแดชบอร์ดการตอบสนองดหตุฉุกเฉินในระดับภูมิภาคใน AppSource](media/service-connect-to-regional-emergency-response/service-regional-emergency-response-app-appsource-get-it-now.png)](https://appsource.microsoft.com/product/power-bi/powerapps_cxo.regional_response)</span><span class="sxs-lookup"><span data-stu-id="d3cc5-119">[![Regional Emergency Response Dashboard app in AppSource](media/service-connect-to-regional-emergency-response/service-regional-emergency-response-app-appsource-get-it-now.png)](https://appsource.microsoft.com/product/power-bi/powerapps_cxo.regional_response)</span></span>

1. <span data-ttu-id="d3cc5-120">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="d3cc5-120">Select **Install**.</span></span> 

    ![ติดตั้งแอปแดชบอร์ดการตอบสนองเหตุฉุกเฉินในระดับภูมิภาค](media/service-connect-to-regional-emergency-response/service-regional-emergency-response-select-install.png)

    <span data-ttu-id="d3cc5-122">หลังจากที่ติดตั้งแอปแล้ว คุณจะเห็นแอปบนหน้าแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="d3cc5-122">Once the app has installed, you see it on your Apps page.</span></span>

   ![แอปแดชบอร์ดการตอบสนองเหตุฉุกเฉินในระดับภูมิภาคบนหน้าแอป](media/service-connect-to-regional-emergency-response/service-regional-emergency-response-app-apps-page-icon.png)

## <a name="connect-to-data-sources"></a><span data-ttu-id="d3cc5-124">เชื่อมต่อกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d3cc5-124">Connect to data sources</span></span>

1. <span data-ttu-id="d3cc5-125">เลือกไอคอนบนหน้าแอปของคุณเพื่อเปิดแอป</span><span class="sxs-lookup"><span data-stu-id="d3cc5-125">Select the icon on your Apps page to open the app.</span></span>

1. <span data-ttu-id="d3cc5-126">บนหน้าจอเริ่มต้น เลือก **สำรวจ**</span><span class="sxs-lookup"><span data-stu-id="d3cc5-126">On the splash screen, select **Explore**.</span></span>

   ![หน้าจอเริ่มต้นของแอปเทมเพลต](media/service-connect-to-regional-emergency-response/service-regional-emergency-response-app-splash-screen.png)

   <span data-ttu-id="d3cc5-128">แอปจะเปิดขึ้นและแสดงข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="d3cc5-128">The app opens, showing sample data.</span></span>

1. <span data-ttu-id="d3cc5-129">เลือกลิงก์ **เชื่อมต่อข้อมูลของคุณ** บนแบนเนอร์ที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="d3cc5-129">Select the **Connect your data** link on the banner at the top of the page.</span></span>

   ![แอปแดชบอร์ดการตอบสนองเหตุฉุกเฉินในระดับภูมิภาคจะเชื่อมโยงข้อมูลของคุณ](media/service-connect-to-regional-emergency-response/service-regional-emergency-response-app-connect-data.png)

1. <span data-ttu-id="d3cc5-131">ในกล่องโต้ตอบที่ปรากฏขึ้น ให้พิมพ์ [URL ของอินสแตนซ์ของสภาพแวดล้อม Common Data Service ของคุณ](/powerapps/sample-apps/emergency-response/deploy-configure#publish-the-power-bi-dashboard)</span><span class="sxs-lookup"><span data-stu-id="d3cc5-131">In the dialog box that appears, type the [URL of your Common Data Service environment instance](/powerapps/sample-apps/emergency-response/deploy-configure#publish-the-power-bi-dashboard).</span></span> <span data-ttu-id="d3cc5-132">เช่น: https://[myenv].crm.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="d3cc5-132">For example: https://[myenv].crm.dynamics.com.</span></span> <span data-ttu-id="d3cc5-133">เมื่อป้อนเสร็จเรียบร้อย ให้คลิก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="d3cc5-133">When done, click **Next**.</span></span>

   ![กล่องโต้ตอบ URL ของแอปแดชบอร์ดการตอบสนองเหตุฉุกเฉินในระดับภูมิภาค](media/service-connect-to-regional-emergency-response/service-regional-emergency-response-app-url-dialog.png)

1. <span data-ttu-id="d3cc5-135">ในกล่องโต้ตอบที่ปรากฏขึ้นถัดไป ให้ตั้งค่าวิธีการรับรองความถูกต้องให้กับ **OAuth2**</span><span class="sxs-lookup"><span data-stu-id="d3cc5-135">In the next dialog that appears, set the authentication method to **OAuth2**.</span></span> <span data-ttu-id="d3cc5-136">คุณไม่ต้องปรับเปลี่ยนการตั้งค่าระดับความเป็นส่วนตัวใด ๆ</span><span class="sxs-lookup"><span data-stu-id="d3cc5-136">You don't have to do anything to the privacy level setting.</span></span>

   <span data-ttu-id="d3cc5-137">เลือก **ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="d3cc5-137">Select **Sign in**.</span></span>

   ![กล่องโต้ตอบการรับรองความถูกต้องของแอปแดชบอร์ดการตอบสนองเหตุฉุกเฉินในระดับภูมิภาค](media/service-connect-to-regional-emergency-response/service-regional-emergency-response-app-authentication-dialog.png)

1. <span data-ttu-id="d3cc5-139">ที่หน้าจอลงชื่อเข้าใช้ของ Microsoft ใหลงชื่อเข้าใช้ Power BI</span><span class="sxs-lookup"><span data-stu-id="d3cc5-139">At the Microsoft sign-in screen, sign in to Power BI.</span></span>

   ![หน้าจอลงชื่อเข้าใช้ของ Microsoft](media/service-connect-to-regional-emergency-response/service-regional-emergency-response-app-microsoft-login.png)

   <span data-ttu-id="d3cc5-141">หลังจากที่คุณลงชื่อเข้าใช้แล้ว รายงานจะเชื่อมต่อเข้ากับแหล่งข้อมูลและจะได้รับข้อมูลล่าสุด</span><span class="sxs-lookup"><span data-stu-id="d3cc5-141">After you've signed in, the report connects to the data sources and is populated with up-to-date data.</span></span> <span data-ttu-id="d3cc5-142">ในช่วงเวลานี้ ตัวตรวจสอบกิจกรรมจะเปิดทำงาน</span><span class="sxs-lookup"><span data-stu-id="d3cc5-142">During this time, the activity monitor turns.</span></span>

   ![กำลังดำเนินการรีเฟรชแอปแดชบอร์ดการตอบสนองเหตุฉุกเฉินในระดับภูมิภาค](media/service-connect-to-regional-emergency-response/service-regional-emergency-response-app-refresh-monitor.png)

## <a name="schedule-report-refresh"></a><span data-ttu-id="d3cc5-144">กำหนดเวลาการรีเฟรชรายงาน</span><span class="sxs-lookup"><span data-stu-id="d3cc5-144">Schedule report refresh</span></span>

<span data-ttu-id="d3cc5-145">เมื่อรีเฟรชข้อมูลแล้ว ให้[ตั้งค่ากำหนดเวลาการรีเฟรช](../connect-data/refresh-scheduled-refresh.md)เพื่อให้ข้อมูลรายงานเป็นข้อมูลล่าสุดอยู่เสมอ</span><span class="sxs-lookup"><span data-stu-id="d3cc5-145">When the data refresh has completed, [set up a refresh schedule](../connect-data/refresh-scheduled-refresh.md) to keep the report data up to date.</span></span>

1. <span data-ttu-id="d3cc5-146">ในแถบส่วนหัวด้านบนสุด เลือก **Power BI**</span><span class="sxs-lookup"><span data-stu-id="d3cc5-146">In the top header bar, select **Power BI**.</span></span>

   ![เส้นทางของ Power BI](media/service-connect-to-regional-emergency-response/service-regional-emergency-response-app-powerbi-breadcrumb.png)

1. <span data-ttu-id="d3cc5-148">ในหน้าต่างนำทางด้านซ้าย มองหาพื้นที่ทำงานของแดชบอร์ดการตอบสนองเหตุฉุกเฉินในระดับภูมิภาคที่อยู่ใน **พื้นที่ทำงาน** แล้วปฏิบัติตามคำแนะนำที่อธิบายไว้ในบทความ [กำหนดค่าการรีเฟรชตามกำหนดเวลา](../connect-data/refresh-scheduled-refresh.md)</span><span class="sxs-lookup"><span data-stu-id="d3cc5-148">In the left navigation pane, look for the Regional Emergency Response Dashboard workspace under **Workspaces**, and follow the instructions described in the [Configure scheduled refresh](../connect-data/refresh-scheduled-refresh.md) article.</span></span>

## <a name="customize-and-share"></a><span data-ttu-id="d3cc5-149">ปรับแต่งตามความต้องการและแชร์</span><span class="sxs-lookup"><span data-stu-id="d3cc5-149">Customize and share</span></span>

<span data-ttu-id="d3cc5-150">คุณสามารถดูรายละเอียดได้ที่[ปรับแต่งและแชร์แอป](../connect-data/service-template-apps-install-distribute.md#customize-and-share-the-app)</span><span class="sxs-lookup"><span data-stu-id="d3cc5-150">See [Customize and share the app](../connect-data/service-template-apps-install-distribute.md#customize-and-share-the-app) for details.</span></span> <span data-ttu-id="d3cc5-151">ตรวจสอบให้มั่นใจว่าคุณได้อ่าน[ข้อความปฏิเสธความรับผิดชอบของรายงาน](/powerapps/sample-apps/regional-emergency-response/overview#disclaimer)ก่อนที่จะเผยแพร่หรือแจกจ่ายแอป</span><span class="sxs-lookup"><span data-stu-id="d3cc5-151">Be sure to review the [report disclaimers](/powerapps/sample-apps/regional-emergency-response/overview#disclaimer) before publishing or distributing the app.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d3cc5-152">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d3cc5-152">Next steps</span></span>
* [<span data-ttu-id="d3cc5-153">การทำความเข้าใจเกี่ยวกับแดชบอร์ดการตอบสนองเหตุฉุกเฉินในระดับภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="d3cc5-153">Understanding the Regional Emergency Response dashboard</span></span>](/powerapps/sample-apps/regional-emergency-response/portals-admin-reporting#get-insights)
* [<span data-ttu-id="d3cc5-154">ตั้งค่าและเรียนรู้เกี่ยวกับตัวอย่างเทมเพลตของการสื่อสารในภาวะวิกฤติใน Power Apps</span><span class="sxs-lookup"><span data-stu-id="d3cc5-154">Set up and learn about the Crisis Communication sample template in Power Apps</span></span>](/powerapps/maker/canvas-apps/sample-crisis-communication-app)
* <span data-ttu-id="d3cc5-155">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d3cc5-155">Questions?</span></span> [<span data-ttu-id="d3cc5-156">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="d3cc5-156">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
* [<span data-ttu-id="d3cc5-157">แอปเทมเพลต Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="d3cc5-157">What are Power BI template apps?</span></span>](../connect-data/service-template-apps-overview.md)
* [<span data-ttu-id="d3cc5-158">ติดตั้งและแจกจ่ายแอปเทมเพลตในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="d3cc5-158">Install and distribute template apps in your organization</span></span>](../connect-data/service-template-apps-install-distribute.md)