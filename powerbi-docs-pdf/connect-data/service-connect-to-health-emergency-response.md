---
title: การเชื่อมต่อเข้ากับแดชบอร์ดการสนับสนุนการตัดสินใจเกี่ยวกับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาล
description: วิธีการรับและติดตั้งแดชบอร์ดการสนับสนุนการตัดสินใจของ COVID-19 สำหรับแอปเทมเพลตกรณีฉุกเฉินเพื่อการดูแลสุขภาพและวิธีการเชื่อมต่อกับข้อมูล
author: paulinbar
ms.author: painbar
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: how-to
ms.date: 05/13/2020
LocalizationGroup: Connect to services
ms.openlocfilehash: 823c8429c95a0b4d858540b2cf1183ca1c7caac7
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96403156"
---
# <a name="connect-to-the-hospital-emergency-response-decision-support-dashboard"></a><span data-ttu-id="4d462-103">การเชื่อมต่อเข้ากับแดชบอร์ดการสนับสนุนการตัดสินใจเกี่ยวกับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาล</span><span class="sxs-lookup"><span data-stu-id="4d462-103">Connect to the Hospital Emergency Response Decision Support Dashboard</span></span>
<span data-ttu-id="4d462-104">แอปเทมเพลตแดชบอร์ดการสนับสนุนการตัดสินใจเกี่ยวกับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาลเป็นส่วนประกอบการรายงานของ[โซลูชั่น Microsoft Power Platform สำหรับการตอบสนองต่อสภาวะฉุกเฉินสำหรับการดูแลสุขภาพ](https://powerapps.microsoft.com/blog/emergency-response-solution-a-microsoft-power-platform-solution-for-healthcare-emergency-response/)</span><span class="sxs-lookup"><span data-stu-id="4d462-104">The Hospital Emergency Response Decision Support Dashboard template app is the reporting component of the [Microsoft Power Platform solution for healthcare emergency response](https://powerapps.microsoft.com/blog/emergency-response-solution-a-microsoft-power-platform-solution-for-healthcare-emergency-response/).</span></span> <span data-ttu-id="4d462-105">แดชบอร์ดจะแสดงข้อมูลทั้งหมดไว้ในระบบสุขภาพของผู้จัดการกรณีฉุกเฉิน เพื่อช่วยให้พวกเขาได้ดูแล้วทำการตัดสินใจได้อย่างถูกต้องและทันเวลา</span><span class="sxs-lookup"><span data-stu-id="4d462-105">The dashboard shows emergency managers aggregate data across their health system to help them to make timely, correct decisions.</span></span>

![รายงานของแอปแดชบอร์ดการสนับสนุนการตัดสินใจเกี่ยวกับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาล](media/service-connect-to-health-emergency-response/service-health-emergency-response-app-report.png)

<span data-ttu-id="4d462-107">บทความนี้จะแจ้งวิธีการติดตั้งแอปและวิธีการเชื่อมต่อกับแหล่งข้อมูลให้คุณทราบ</span><span class="sxs-lookup"><span data-stu-id="4d462-107">This article tells  you how to install the app and how to connect to the data sources.</span></span> <span data-ttu-id="4d462-108">หากต้องการเรียนรู้วิธีการใช้รายงานที่คุณจะเห็นจากแอปนี้ โปรดศึกษาจาก[เอกสารเรื่องแอปแดชบอร์ดการสนับสนุนการตัดสินใจเกี่ยวกับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาล](/powerapps/sample-apps/emergency-response/deploy-configure#view-the-power-bi-dashboard)</span><span class="sxs-lookup"><span data-stu-id="4d462-108">To learn how to use the report that you will see with this app, see the [Hospital Emergency Response Decision Support Dashboard documentation](/powerapps/sample-apps/emergency-response/deploy-configure#view-the-power-bi-dashboard).</span></span>

<span data-ttu-id="4d462-109">หลังจากที่คุณได้ติดตั้งแอปเทมเพลตและเชื่อมต่อกับแหล่งข้อมูลแล้ว คุณสามารถปรับแต่งรายงานได้ตามความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="4d462-109">After you've installed the template app and connected to the data sources, you can customize the report as per your needs.</span></span> <span data-ttu-id="4d462-110">จากนั้นคุณจะสามารถเผยแพร่รายงานออกเป็นแอปให้กับเพื่อนร่วมงานในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="4d462-110">You can then distribute it as an app to colleagues in your organization.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4d462-111">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="4d462-111">Prerequisites</span></span>

<span data-ttu-id="4d462-112">ก่อนที่จะติดตั้งแอปเทมเพลตนี้ คุณต้องติดตั้งและตั้งค่า[โซลูชั่น Power Platform สำหรับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาล](/powerapps/sample-apps/emergency-response/deploy-configure)ก่อน</span><span class="sxs-lookup"><span data-stu-id="4d462-112">Before installing this template app, you must first install and set up the [Hospital Emergency Response Power Platform solution](/powerapps/sample-apps/emergency-response/deploy-configure).</span></span> <span data-ttu-id="4d462-113">การติดตั้งโซลูชันนี้จะสร้างการอ้างอิงแหล่งข้อมูลที่จำเป็นเพื่อป้อนข้อมูลลงในแอป</span><span class="sxs-lookup"><span data-stu-id="4d462-113">Installing this solution creates the datasource references necessary to populate the app with data.</span></span>

<span data-ttu-id="4d462-114">เมื่อทำการติดตั้งโซลูชั่น Power Platform สำหรับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาลแล้ว ให้จดบันทึก [URL ของสภาพแวดล้อมอินสแตนซ์ Common Data Service ของคุณ](/powerapps/sample-apps/emergency-response/deploy-configure#publish-the-power-bi-dashboard)เอาไว้</span><span class="sxs-lookup"><span data-stu-id="4d462-114">When installing Hospital Emergency Response Power Platform solution, take note of the [URL of your Common Data Service environment instance](/powerapps/sample-apps/emergency-response/deploy-configure#publish-the-power-bi-dashboard).</span></span> <span data-ttu-id="4d462-115">คุณจะต้องใช้ข้อมูลนี้เพื่อเชื่อมต่อแอปเทมเพลตเข้ากับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4d462-115">You will need it to connect the template app to the data.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="4d462-116">ติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="4d462-116">Install the app</span></span>

1. <span data-ttu-id="4d462-117">คลิกที่ลิงก์ต่อไปนี้เพื่อเข้าถึงแอป: [แอปเทมเพลตแดชบอร์ดการสนับสนุนการตัดสินใจเกี่ยวกับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาล](https://aka.ms/AppSource_Hospital_offer)</span><span class="sxs-lookup"><span data-stu-id="4d462-117">Click the following link to get to the app: [Hospital Emergency Response Decision Support Dashboard template app](https://aka.ms/AppSource_Hospital_offer)</span></span>

1. <span data-ttu-id="4d462-118">บนหน้า AppSource สำหรับแอป ให้เลือก [**รับทันที**](https://aka.ms/AppSource_Hospital_offer)</span><span class="sxs-lookup"><span data-stu-id="4d462-118">On the AppSource page for the app, select [**GET IT NOW**](https://aka.ms/AppSource_Hospital_offer).</span></span>

    <span data-ttu-id="4d462-119">[![แอปแดชบอร์ดการสนับสนุนการตัดสินใจเกี่ยวกับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาลใน AppSource](media/service-connect-to-health-emergency-response/service-health-emergency-response-app-appsource-get-it-now.png)](https://aka.ms/AppSource_Hospital_offer)</span><span class="sxs-lookup"><span data-stu-id="4d462-119">[![Hospital Emergency Response Decision Support Dashboard app in AppSource](media/service-connect-to-health-emergency-response/service-health-emergency-response-app-appsource-get-it-now.png)](https://aka.ms/AppSource_Hospital_offer)</span></span>

1. <span data-ttu-id="4d462-120">อ่านข้อมูลใน **สิ่งสุดท้ายที่ต้องทำเพิ่มเติม** แล้วเลือก **ดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="4d462-120">Read the information in **One more thing**, and select **Continue**.</span></span>

    ![สิ่งสุดท้ายที่ต้องทำเพิ่มเติมของแอปแดชบอร์ดการสนับสนุนการตัดสินใจเกี่ยวกับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาล](media/service-connect-to-health-emergency-response/service-health-emergency-response-1-more-thing.png)

1. <span data-ttu-id="4d462-122">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="4d462-122">Select **Install**.</span></span> 

    ![ติดตั้งแอปแดชบอร์ดการสนับสนุนการตัดสินใจเกี่ยวกับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาล](media/service-connect-to-health-emergency-response/service-health-emergency-response-select-install.png)

    <span data-ttu-id="4d462-124">หลังจากที่ติดตั้งแอปแล้ว คุณจะเห็นแอปบนหน้าแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="4d462-124">Once the app has installed, you see it on your Apps page.</span></span>

   ![แอปแดชบอร์ดการสนับสนุนการตัดสินใจเกี่ยวกับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาลบนหน้าแอป](media/service-connect-to-health-emergency-response/service-health-emergency-response-app-apps-page-icon.png)

## <a name="connect-to-data-sources"></a><span data-ttu-id="4d462-126">เชื่อมต่อกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4d462-126">Connect to data sources</span></span>

1. <span data-ttu-id="4d462-127">เลือกไอคอนบนหน้าแอปของคุณเพื่อเปิดแอป</span><span class="sxs-lookup"><span data-stu-id="4d462-127">Select the icon on your Apps page to open the app.</span></span>

1. <span data-ttu-id="4d462-128">บนหน้าจอเริ่มต้น เลือก **สำรวจ**</span><span class="sxs-lookup"><span data-stu-id="4d462-128">On the splash screen, select **Explore**.</span></span>

   ![หน้าจอเริ่มต้นของแอปเทมเพลต](media/service-connect-to-health-emergency-response/service-health-emergency-response-app-splash-screen.png)

   <span data-ttu-id="4d462-130">แอปจะเปิดขึ้นและแสดงข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="4d462-130">The app opens, showing sample data.</span></span>

1. <span data-ttu-id="4d462-131">เลือกลิงก์ **เชื่อมต่อข้อมูลของคุณ** บนแบนเนอร์ที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="4d462-131">Select the **Connect your data** link on the banner at the top of the page.</span></span>

   ![แอปแดชบอร์ดการสนับสนุนการตัดสินใจเกี่ยวกับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาลเชื่อมต่อลิงก์ข้อมูลของคุณ](media/service-connect-to-health-emergency-response/service-health-emergency-response-app-connect-data.png)

1. <span data-ttu-id="4d462-133">ในกล่องโต้ตอบ:</span><span class="sxs-lookup"><span data-stu-id="4d462-133">In the dialog box:</span></span>
   1. <span data-ttu-id="4d462-134">ในช่องชื่อองค์กร ให้ป้อนชื่อองค์กรของคุณ เช่น "Contoso Health Systems"</span><span class="sxs-lookup"><span data-stu-id="4d462-134">In the organization name field, enter the name of your organization, for example, "Contoso Health Systems".</span></span> <span data-ttu-id="4d462-135">คุณสามารถป้อนข้อมูลช่องนี้หรือไม่ก็ได้</span><span class="sxs-lookup"><span data-stu-id="4d462-135">This field is optional.</span></span> <span data-ttu-id="4d462-136">ชื่อนี้จะปรากฏที่ด้านบนซ้ายของแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="4d462-136">This name appears in the upper-left side of the dashboard.</span></span>
   1. <span data-ttu-id="4d462-137">ในช่อง CDS_base_solution ให้พิมพ์ [URL ของอินสแตนซ์สภาพแวดล้อม Common Data Service ของคุณ](/powerapps/sample-apps/emergency-response/deploy-configure#publish-the-power-bi-dashboard)</span><span class="sxs-lookup"><span data-stu-id="4d462-137">In the CDS_base_solution field, Type the [URL of your Common Data Service environment instance](/powerapps/sample-apps/emergency-response/deploy-configure#publish-the-power-bi-dashboard).</span></span> <span data-ttu-id="4d462-138">เช่น: https://[myenv].crm.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="4d462-138">For example: https://[myenv].crm.dynamics.com.</span></span> <span data-ttu-id="4d462-139">เมื่อป้อนเสร็จเรียบร้อย ให้คลิก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="4d462-139">When done, click **Next**.</span></span>

   ![กล่องโต้ตอบ URL ของแอปแดชบอร์ดการสนับสนุนการตัดสินใจเกี่ยวกับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาล](media/service-connect-to-health-emergency-response/service-health-emergency-response-app-url-dialog.png)

1. <span data-ttu-id="4d462-141">ในกล่องโต้ตอบที่ปรากฏขึ้นถัดไป ให้ตั้งค่าวิธีการรับรองความถูกต้องให้กับ **OAuth2**</span><span class="sxs-lookup"><span data-stu-id="4d462-141">In the next dialog that appears, set the authentication method to **OAuth2**.</span></span> <span data-ttu-id="4d462-142">คุณไม่ต้องปรับเปลี่ยนการตั้งค่าระดับความเป็นส่วนตัวใด ๆ</span><span class="sxs-lookup"><span data-stu-id="4d462-142">You don't have to do anything to the privacy level setting.</span></span>

   <span data-ttu-id="4d462-143">เลือก **ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="4d462-143">Select **Sign in**.</span></span>

   ![กล่องโต้ตอบการรับรองความถูกต้องของแอปแดชบอร์ดการสนับสนุนการตัดสินใจเกี่ยวกับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาล](media/service-connect-to-health-emergency-response/service-health-emergency-response-app-authentication-dialog.png)

1. <span data-ttu-id="4d462-145">ที่หน้าจอลงชื่อเข้าใช้ของ Microsoft ใหลงชื่อเข้าใช้ Power BI</span><span class="sxs-lookup"><span data-stu-id="4d462-145">At the Microsoft sign-in screen, sign in to Power BI.</span></span>

   ![หน้าจอลงชื่อเข้าใช้ของ Microsoft](media/service-connect-to-health-emergency-response/service-health-emergency-response-app-microsoft-login.png)

   <span data-ttu-id="4d462-147">หลังจากที่คุณลงชื่อเข้าใช้แล้ว รายงานจะเชื่อมต่อเข้ากับแหล่งข้อมูลและจะได้รับข้อมูลล่าสุด</span><span class="sxs-lookup"><span data-stu-id="4d462-147">After you've signed in, the report connects to the data sources and is populated with up-to-date data.</span></span> <span data-ttu-id="4d462-148">ในช่วงเวลานี้ ตัวตรวจสอบกิจกรรมจะเปิดทำงาน</span><span class="sxs-lookup"><span data-stu-id="4d462-148">During this time, the activity monitor turns.</span></span>

   ![กำลังรีเพรชแอปแดชบอร์ดการสนับสนุนการตัดสินใจเกี่ยวกับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาล](media/service-connect-to-health-emergency-response/service-health-emergency-response-app-refresh-monitor.png)

## <a name="schedule-report-refresh"></a><span data-ttu-id="4d462-150">กำหนดเวลาการรีเฟรชรายงาน</span><span class="sxs-lookup"><span data-stu-id="4d462-150">Schedule report refresh</span></span>

<span data-ttu-id="4d462-151">เมื่อรีเฟรชข้อมูลแล้ว ให้[ตั้งค่ากำหนดเวลาการรีเฟรช](../connect-data/refresh-scheduled-refresh.md)เพื่อให้ข้อมูลรายงานเป็นข้อมูลล่าสุดอยู่เสมอ</span><span class="sxs-lookup"><span data-stu-id="4d462-151">When the data refresh has completed, [set up a refresh schedule](../connect-data/refresh-scheduled-refresh.md) to keep the report data up to date.</span></span>

1. <span data-ttu-id="4d462-152">ในแถบส่วนหัวด้านบนสุด เลือก **Power BI**</span><span class="sxs-lookup"><span data-stu-id="4d462-152">In the top header bar, select **Power BI**.</span></span>

   ![เส้นทางของ Power BI](media/service-connect-to-health-emergency-response/service-health-emergency-response-app-powerbi-breadcrumb.png)

1. <span data-ttu-id="4d462-154">ในหน้าต่างนำทางด้านซ้าย มองหาแดชบอร์ดการสนับสนุนการตัดสินใจเกี่ยวกับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาลที่อยู่ใน **พื้นที่ทำงาน** แล้วปฏิบัติตามคำแนะนำที่อธิบายไว้ในบทความ [การปรับค่าการรีเฟรชตามกำหนดเวลา](../connect-data/refresh-scheduled-refresh.md)</span><span class="sxs-lookup"><span data-stu-id="4d462-154">In the left navigation pane, look for the Hospital Emergency Response Decision Support Dashboard workspace under **Workspaces**, and follow the instructions described in the [Configure scheduled refresh](../connect-data/refresh-scheduled-refresh.md) article.</span></span>

## <a name="customize-and-share"></a><span data-ttu-id="4d462-155">ปรับแต่งตามความต้องการและแชร์</span><span class="sxs-lookup"><span data-stu-id="4d462-155">Customize and share</span></span>

<span data-ttu-id="4d462-156">คุณสามารถดูรายละเอียดได้ที่[ปรับแต่งและแชร์แอป](../connect-data/service-template-apps-install-distribute.md#customize-and-share-the-app)</span><span class="sxs-lookup"><span data-stu-id="4d462-156">See [Customize and share the app](../connect-data/service-template-apps-install-distribute.md#customize-and-share-the-app) for details.</span></span> <span data-ttu-id="4d462-157">ตรวจสอบให้มั่นใจว่าคุณได้อ่าน[ข้อความปฏิเสธความรับผิดชอบของรายงาน](../create-reports/sample-covid-19-us.md#disclaimers)ก่อนที่จะเผยแพร่หรือแจกจ่ายแอป</span><span class="sxs-lookup"><span data-stu-id="4d462-157">Be sure to review the [report disclaimers](../create-reports/sample-covid-19-us.md#disclaimers) before publishing or distributing the app.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4d462-158">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4d462-158">Next steps</span></span>
* [<span data-ttu-id="4d462-159">การทำความเข้าใจรายงานของการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาล</span><span class="sxs-lookup"><span data-stu-id="4d462-159">Understanding the Hospital Emergency Response report</span></span>](/powerapps/sample-apps/emergency-response/deploy-configure#view-the-power-bi-dashboard)
* [<span data-ttu-id="4d462-160">ตั้งค่าและเรียนรู้เกี่ยวกับตัวอย่างเทมเพลตของการสื่อสารในภาวะวิกฤติใน Power Apps</span><span class="sxs-lookup"><span data-stu-id="4d462-160">Set up and learn about the Crisis Communication sample template in Power Apps</span></span>](/powerapps/maker/canvas-apps/sample-crisis-communication-app)
* <span data-ttu-id="4d462-161">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4d462-161">Questions?</span></span> [<span data-ttu-id="4d462-162">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="4d462-162">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
* [<span data-ttu-id="4d462-163">แอปเทมเพลต Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="4d462-163">What are Power BI template apps?</span></span>](../connect-data/service-template-apps-overview.md)
* [<span data-ttu-id="4d462-164">ติดตั้งและแจกจ่ายแอปเทมเพลตในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="4d462-164">Install and distribute template apps in your organization</span></span>](../connect-data/service-template-apps-install-distribute.md)