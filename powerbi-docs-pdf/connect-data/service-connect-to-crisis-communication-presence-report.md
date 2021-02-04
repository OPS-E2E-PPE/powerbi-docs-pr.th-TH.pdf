---
title: การเชื่อมต่อเข้ากับรายงานสภาพการณ์การสื่อสารในภาวะวิกฤติ
description: วิธีการรับและติดตั้งแอปเทมเพลตรายงานสภาพการณ์การสื่อสารในภาวะวิกฤติ COVID-19 และวิธีการเชื่อมต่อกับข้อมูล
author: paulinbar
ms.author: painbar
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: how-to
ms.date: 04/06/2020
LocalizationGroup: Connect to services
ms.openlocfilehash: e9fd1179dc15776cef701476d38b18823f3a8deb
ms.sourcegitcommit: 8250187368d3de48663eb516a816ff701119b579
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/10/2020
ms.locfileid: "96998810"
---
# <a name="connect-to-the-crisis-communication-presence-report"></a><span data-ttu-id="e8c01-103">การเชื่อมต่อเข้ากับรายงานสภาพการณ์การสื่อสารในภาวะวิกฤติ</span><span class="sxs-lookup"><span data-stu-id="e8c01-103">Connect to the Crisis Communication Presence Report</span></span>

<span data-ttu-id="e8c01-104">แอป Power BI นี้เป็นระบบรายงาน/แดชบอร์ดใน Microsoft Power Platform สำหรับการสื่อสารในภาวะวิกฤติ</span><span class="sxs-lookup"><span data-stu-id="e8c01-104">This Power BI app is the report/dashboard artifact in the Microsoft Power Platform solution for Crisis Communication.</span></span> <span data-ttu-id="e8c01-105">ซึ่งจะติดตามตำแหน่งของผู้ปฏิบัติงานสำหรับผู้ใช้งานแอปการสื่อสารในภาวะวิกฤติ</span><span class="sxs-lookup"><span data-stu-id="e8c01-105">It tracks worker location for Crisis Communication app users.</span></span> <span data-ttu-id="e8c01-106">โซลูชั่นนี้จะผสานรวมความจุของ Power Apps, Power Automate, Teams, SharePoint และ Power BI เข้าด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="e8c01-106">The solution combines capabilities of Power Apps, Power Automate, Teams, SharePoint and Power BI.</span></span> <span data-ttu-id="e8c01-107">ซึ่งสามารถใช้งานได้ทั้งบนเว็บ ในอุปกรณ์เคลื่อนที่ หรือใน Teams</span><span class="sxs-lookup"><span data-stu-id="e8c01-107">It can be used on the web, mobile or in Teams.</span></span>

![การรายงานแอปรายงานสภาพการณ์การสื่อสารในภาวะวิกฤติ](media/service-connect-to-crisis-communication-presence-report/service-crisis-communication-presence-report.png)

<span data-ttu-id="e8c01-109">แดชบอร์ดจะแสดงข้อมูลทั้งหมดไว้ในระบบสุขภาพของผู้จัดการกรณีฉุกเฉิน เพื่อช่วยให้พวกเขาได้ดูแล้วทำการตัดสินใจได้อย่างถูกต้องและทันเวลา</span><span class="sxs-lookup"><span data-stu-id="e8c01-109">The dashboard shows emergency managers aggregate data across their health system to help them to make timely, correct decisions.</span></span>

<span data-ttu-id="e8c01-110">บทความนี้จะแจ้งวิธีการติดตั้งแอปและวิธีการเชื่อมต่อกับแหล่งข้อมูลให้คุณทราบ</span><span class="sxs-lookup"><span data-stu-id="e8c01-110">This article tells  you how to install the app and how to connect to the data sources.</span></span> <span data-ttu-id="e8c01-111">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแอปการสื่อสารในภาวะวิกฤติ โปรดศึกษาจาก[การตั้งค่าและการเรียนรู้ตัวอย่างเทมเพลตของการสื่อสารในภาวะวิกฤติใน Power Apps](/powerapps/maker/canvas-apps/sample-crisis-communication-app)</span><span class="sxs-lookup"><span data-stu-id="e8c01-111">For more information about the Crisis Communication app, see [Set up and learn about the Crisis Communication sample template in Power Apps](/powerapps/maker/canvas-apps/sample-crisis-communication-app)</span></span>

<span data-ttu-id="e8c01-112">หลังจากที่คุณได้ติดตั้งแอปเทมเพลตและเชื่อมต่อกับแหล่งข้อมูลแล้ว คุณสามารถปรับแต่งรายงานได้ตามความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="e8c01-112">After you've installed the template app and connected to the data sources, you can customize the report as per your needs.</span></span> <span data-ttu-id="e8c01-113">จากนั้นคุณจะสามารถเผยแพร่รายงานออกเป็นแอปให้กับเพื่อนร่วมงานในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="e8c01-113">You can then distribute it as an app to colleagues in your organization.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e8c01-114">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="e8c01-114">Prerequisites</span></span>

<span data-ttu-id="e8c01-115">ก่อนที่จะติดตั้งแอปเทมเพลตนี้ คุณต้องติดตั้งและตั้งค่า[ตัวอย่างการสื่อสารในภาวะวิกฤติ](/powerapps/maker/canvas-apps/sample-crisis-communication-app)ก่อน</span><span class="sxs-lookup"><span data-stu-id="e8c01-115">Before installing this template app, you must first install and set up the [Crisis Communication sample](/powerapps/maker/canvas-apps/sample-crisis-communication-app).</span></span> <span data-ttu-id="e8c01-116">การติดตั้งโซลูชันนี้จะสร้างการอ้างอิงแหล่งข้อมูลที่จำเป็นเพื่อป้อนข้อมูลลงในแอป</span><span class="sxs-lookup"><span data-stu-id="e8c01-116">Installing this solution creates the datasource references necessary to populate the app with data.</span></span>

<span data-ttu-id="e8c01-117">เมื่อติดตั้งตัวอย่างเทมเพลตของการสื่อสารในภาวะวิกฤติแล้ว ให้จดบันทึก[เส้นทางโฟลเดอร์รายการ SharePoint ของ "CI_Employee Status" และ ID รายการ](/powerapps/maker/canvas-apps/sample-crisis-communication-app#monitor-office-absences-with-power-bi)</span><span class="sxs-lookup"><span data-stu-id="e8c01-117">When installing the Crisis Communication sample, take note of the [SharePoint list folder path of "CI_Employee Status" and list ID](/powerapps/maker/canvas-apps/sample-crisis-communication-app#monitor-office-absences-with-power-bi).</span></span>

## <a name="install-the-app"></a><span data-ttu-id="e8c01-118">ติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="e8c01-118">Install the app</span></span>

1. <span data-ttu-id="e8c01-119">คลิกที่ลิงก์ต่อไปนี้เพื่อเข้าถึงแอป: [แอปเทมเพลตรายงานสภาพการณ์การสื่อสารในภาวะวิกฤติ](https://appsource.microsoft.com/en-us/product/power-bi/pbi-contentpacks.crisiscomms)</span><span class="sxs-lookup"><span data-stu-id="e8c01-119">Click the following link to get to the app: [Crisis Communication Presence Report template app](https://appsource.microsoft.com/en-us/product/power-bi/pbi-contentpacks.crisiscomms)</span></span>

1. <span data-ttu-id="e8c01-120">บนหน้า AppSource สำหรับแอป ให้เลือก [**รับทันที**](https://appsource.microsoft.com/en-us/product/power-bi/pbi-contentpacks.crisiscomms)</span><span class="sxs-lookup"><span data-stu-id="e8c01-120">On the AppSource page for the app, select [**GET IT NOW**](https://appsource.microsoft.com/en-us/product/power-bi/pbi-contentpacks.crisiscomms).</span></span>

    <span data-ttu-id="e8c01-121">[![แอปรายงานสภาพการณ์การสื่อสารในภาวะวิกฤติใน AppSource](media/service-connect-to-crisis-communication-presence-report/service-crisis-communication-presence-report-app-appsource-get-it-now.png)](https://appsource.microsoft.com/en-us/product/power-bi/pbi-contentpacks.crisiscomms)</span><span class="sxs-lookup"><span data-stu-id="e8c01-121">[![Crisis Communication Presence Report app in AppSource](media/service-connect-to-crisis-communication-presence-report/service-crisis-communication-presence-report-app-appsource-get-it-now.png)](https://appsource.microsoft.com/en-us/product/power-bi/pbi-contentpacks.crisiscomms)</span></span>

1. <span data-ttu-id="e8c01-122">อ่านข้อมูลใน **สิ่งสุดท้ายที่ต้องทำเพิ่มเติม** แล้วเลือก **ดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="e8c01-122">Read the information in **One more thing**, and select **Continue**.</span></span>

    ![สิ่งสุดท้ายที่ต้องทำเพิ่มเติมของแอปรายงานสภาพการณ์การสื่อสารในภาวะวิกฤติใน AppSource](media/service-connect-to-crisis-communication-presence-report/service-crisis-communication-presence-report-1-more-thing.png)

1. <span data-ttu-id="e8c01-124">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="e8c01-124">Select **Install**.</span></span> 

    ![ติดตั้งแอปรายงานสภาพการณ์การสื่อสารในภาวะวิกฤติ](media/service-connect-to-crisis-communication-presence-report/service-crisis-communication-presence-report-select-install.png)

    <span data-ttu-id="e8c01-126">หลังจากที่ติดตั้งแอปแล้ว คุณจะเห็นแอปบนหน้าแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="e8c01-126">Once the app has installed, you see it on your Apps page.</span></span>

   ![แอปรายงานสภาพการณ์การสื่อสารในภาวะวิกฤติบนหน้าแอป](media/service-connect-to-crisis-communication-presence-report/service-crisis-communication-presence-report-app-apps-page-icon.png)

## <a name="connect-to-data-sources"></a><span data-ttu-id="e8c01-128">เชื่อมต่อกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e8c01-128">Connect to data sources</span></span>

1. <span data-ttu-id="e8c01-129">เลือกไอคอนบนหน้าแอปของคุณเพื่อเปิดแอป</span><span class="sxs-lookup"><span data-stu-id="e8c01-129">Select the icon on your Apps page to open the app.</span></span>


   <span data-ttu-id="e8c01-130">แอปจะเปิดขึ้นและแสดงข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="e8c01-130">The app opens, showing sample data.</span></span>

1. <span data-ttu-id="e8c01-131">เลือกลิงก์ **เชื่อมต่อข้อมูลของคุณ** บนแบนเนอร์ที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="e8c01-131">Select the **Connect your data** link on the banner at the top of the page.</span></span>

   ![แอปรายงานสภาพการณ์การสื่อสารในภาวะวิกฤตเชื่อมต่อลิงก์ข้อมูลของคุณ](media/service-connect-to-crisis-communication-presence-report/service-crisis-communication-presence-report-app-connect-data.png)

1. <span data-ttu-id="e8c01-133">ในกล่องโต้ตอบ:</span><span class="sxs-lookup"><span data-stu-id="e8c01-133">In the dialog box:</span></span>
   1. <span data-ttu-id="e8c01-134">ในช่อง SharePoint_Folder ให้ป้อน[เส้นทางรายการ SharePoint ของ "CI_Employee Status"](/powerapps/maker/canvas-apps/sample-crisis-communication-app#monitor-office-absences-with-power-bi)</span><span class="sxs-lookup"><span data-stu-id="e8c01-134">In the SharePoint_Folder field, enter your ["CI_Employee Status" SharePoint list path](/powerapps/maker/canvas-apps/sample-crisis-communication-app#monitor-office-absences-with-power-bi).</span></span>
   1. <span data-ttu-id="e8c01-135">ในช่อง List_ID ให้ป้อน ID รายการที่คุณได้มาจากการตั้งค่ารายการ</span><span class="sxs-lookup"><span data-stu-id="e8c01-135">In the List_ID field, enter your list ID that you got from list settings.</span></span> <span data-ttu-id="e8c01-136">เมื่อป้อนเสร็จเรียบร้อย ให้คลิก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="e8c01-136">When done, click **Next**.</span></span>

   ![กล่องโต้ตอบ URL ของแอปรายงานสภาพการณ์การสื่อสารในภาวะวิกฤติ](media/service-connect-to-crisis-communication-presence-report/service-crisis-communication-presence-report-app-url-dialog.png)

1. <span data-ttu-id="e8c01-138">ในกล่องโต้ตอบที่ปรากฏขึ้นถัดไป ให้ตั้งค่าวิธีการรับรองความถูกต้องให้กับ **OAuth2**</span><span class="sxs-lookup"><span data-stu-id="e8c01-138">In the next dialog that appears, set the authentication method to **OAuth2**.</span></span> <span data-ttu-id="e8c01-139">คุณไม่ต้องปรับเปลี่ยนการตั้งค่าระดับความเป็นส่วนตัวใด ๆ</span><span class="sxs-lookup"><span data-stu-id="e8c01-139">You don't have to do anything to the privacy level setting.</span></span>

   <span data-ttu-id="e8c01-140">เลือก **ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="e8c01-140">Select **Sign in**.</span></span>

   ![กล่องโต้ตอบการรับรองความถูกต้องของแอปรายงานสภาพการณ์การสื่อสารในภาวะวิกฤติ](media/service-connect-to-crisis-communication-presence-report/service-crisis-communication-presence-report-app-authentication-dialog.png)

1. <span data-ttu-id="e8c01-142">ที่หน้าจอลงชื่อเข้าใช้ของ Microsoft ใหลงชื่อเข้าใช้ Power BI</span><span class="sxs-lookup"><span data-stu-id="e8c01-142">At the Microsoft sign-in screen, sign in to Power BI.</span></span>

   ![หน้าจอลงชื่อเข้าใช้ของ Microsoft](media/service-connect-to-crisis-communication-presence-report/service-crisis-communication-presence-report-app-microsoft-login.png)

   <span data-ttu-id="e8c01-144">หลังจากที่คุณลงชื่อเข้าใช้แล้ว รายงานจะเชื่อมต่อเข้ากับแหล่งข้อมูลและจะได้รับข้อมูลล่าสุด</span><span class="sxs-lookup"><span data-stu-id="e8c01-144">After you've signed in, the report connects to the data sources and is populated with up-to-date data.</span></span> <span data-ttu-id="e8c01-145">ในช่วงเวลานี้ ตัวตรวจสอบกิจกรรมจะเปิดทำงาน</span><span class="sxs-lookup"><span data-stu-id="e8c01-145">During this time, the activity monitor turns.</span></span>

   ![กำลังรีเฟรชแอปรายงานสภาพการณ์การสื่อสารในภาวะวิกฤติ](media/service-connect-to-crisis-communication-presence-report/service-crisis-communication-presence-report-app-refresh-monitor.png)

## <a name="schedule-report-refresh"></a><span data-ttu-id="e8c01-147">กำหนดเวลาการรีเฟรชรายงาน</span><span class="sxs-lookup"><span data-stu-id="e8c01-147">Schedule report refresh</span></span>

<span data-ttu-id="e8c01-148">เมื่อรีเฟรชข้อมูลแล้ว ให้[ตั้งค่ากำหนดเวลาการรีเฟรช](../connect-data/refresh-scheduled-refresh.md)เพื่อให้ข้อมูลรายงานเป็นข้อมูลล่าสุดอยู่เสมอ</span><span class="sxs-lookup"><span data-stu-id="e8c01-148">When the data refresh has completed, [set up a refresh schedule](../connect-data/refresh-scheduled-refresh.md) to keep the report data up to date.</span></span>

1. <span data-ttu-id="e8c01-149">ในแถบส่วนหัวด้านบนสุด เลือก **Power BI**</span><span class="sxs-lookup"><span data-stu-id="e8c01-149">In the top header bar, select **Power BI**.</span></span>

   ![เส้นทางของ Power BI](media/service-connect-to-crisis-communication-presence-report/service-crisis-communication-presence-report-app-powerbi-breadcrumb.png)

1. <span data-ttu-id="e8c01-151">ในหน้าต่างนำทางด้านซ้าย มองหาแดชบอร์ดการสนับสนุนการตัดสินใจเกี่ยวกับการตอบสนองต่อสภาวะฉุกเฉินของโรงพยาบาลที่อยู่ใน **พื้นที่ทำงาน** แล้วปฏิบัติตามคำแนะนำที่อธิบายไว้ในบทความ[การปรับค่าการรีเฟรชตามกำหนดเวลา](../connect-data/refresh-scheduled-refresh.md)</span><span class="sxs-lookup"><span data-stu-id="e8c01-151">In the left navigation pane, look for the Hospital Emergency Response Decision Support Dashboard workspace under **Workspaces**, and follow the instruction described in the [Configure scheduled refresh](../connect-data/refresh-scheduled-refresh.md) article.</span></span>

## <a name="customize-and-share"></a><span data-ttu-id="e8c01-152">ปรับแต่งตามความต้องการและแชร์</span><span class="sxs-lookup"><span data-stu-id="e8c01-152">Customize and share</span></span>

<span data-ttu-id="e8c01-153">คุณสามารถดูรายละเอียดได้ที่[ปรับแต่งและแชร์แอป](../connect-data/service-template-apps-install-distribute.md#customize-and-share-the-app)</span><span class="sxs-lookup"><span data-stu-id="e8c01-153">See [Customize and share the app](../connect-data/service-template-apps-install-distribute.md#customize-and-share-the-app) for details.</span></span> <span data-ttu-id="e8c01-154">ตรวจสอบให้มั่นใจว่าคุณได้อ่าน[ข้อความปฏิเสธความรับผิดชอบของรายงาน](../create-reports/sample-covid-19-us.md#disclaimers)ก่อนที่จะเผยแพร่หรือแจกจ่ายแอป</span><span class="sxs-lookup"><span data-stu-id="e8c01-154">Be sure to review the [report disclaimers](../create-reports/sample-covid-19-us.md#disclaimers) before publishing or distributing the app.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e8c01-155">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="e8c01-155">Next steps</span></span>
* [<span data-ttu-id="e8c01-156">ตั้งค่าและเรียนรู้เกี่ยวกับตัวอย่างเทมเพลตของการสื่อสารในภาวะวิกฤติใน Power Apps</span><span class="sxs-lookup"><span data-stu-id="e8c01-156">Set up and learn about the Crisis Communication sample template in Power Apps</span></span>](/powerapps/maker/canvas-apps/sample-crisis-communication-app)
* <span data-ttu-id="e8c01-157">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="e8c01-157">Questions?</span></span> [<span data-ttu-id="e8c01-158">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="e8c01-158">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
* [<span data-ttu-id="e8c01-159">แอปเทมเพลต Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="e8c01-159">What are Power BI template apps?</span></span>](../connect-data/service-template-apps-overview.md)
* [<span data-ttu-id="e8c01-160">ติดตั้งและแจกจ่ายแอปเทมเพลตในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="e8c01-160">Install and distribute template apps in your organization</span></span>](../connect-data/service-template-apps-install-distribute.md)
