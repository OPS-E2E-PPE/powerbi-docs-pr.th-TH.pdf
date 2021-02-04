---
title: เชื่อมต่อกับ Zendesk ด้วย Power BI
description: Zendesk สำหรับ Power BI
author: paulinbar
ms.author: painbar
ms.reviewer: sarinas
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: how-to
ms.date: 05/04/2020
LocalizationGroup: Connect to services
ms.openlocfilehash: d5400830df44055a0f17de72385778a0c06fb06b
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96403041"
---
# <a name="connect-to-zendesk-with-power-bi"></a><span data-ttu-id="a4842-103">เชื่อมต่อกับ Zendesk ด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="a4842-103">Connect to Zendesk with Power BI</span></span>

<span data-ttu-id="a4842-104">บทความนี้จะแนะนำคุณในการดึงข้อมูลของคุณจากบัญชี Zendesk ของคุณด้วยแอปเทมเพลตของ Power BI</span><span class="sxs-lookup"><span data-stu-id="a4842-104">This article walks you through pulling your data from your Zendesk account with a Power BI template app.</span></span> <span data-ttu-id="a4842-105">แอป Zendesk นำเสนอแดชบอร์ด Power BI และชุดของรายงาน Power BI ที่มีข้อมูลเชิงลึกเกี่ยวกับปริมาณตั๋วและประสิทธิภาพการทำงานของบริษัทตัวแทน</span><span class="sxs-lookup"><span data-stu-id="a4842-105">The Zendesk app offers a Power BI dashboard and a set of Power BI reports that provide insights about your ticket volumes and agent performance.</span></span> <span data-ttu-id="a4842-106">ข้อมูลถูกรีเฟรชโดยอัตโนมัติวันละครั้ง</span><span class="sxs-lookup"><span data-stu-id="a4842-106">The data is refreshed automatically once a day.</span></span> 

<span data-ttu-id="a4842-107">หลังจากที่คุณได้ติดตั้งแอปแบบเทมเพลตคุณสามารถกำหนดแดชบอร์ดและรายงานเพื่อเน้นข้อมูลที่คุณสนใจมากที่สุดได้</span><span class="sxs-lookup"><span data-stu-id="a4842-107">After you've installed the template app, you can customize the dashboard and report to highlight the information you care about most.</span></span> <span data-ttu-id="a4842-108">จากนั้นคุณสามารถเผยแพร่เป็นแอปไปยังเพื่อนร่วมงานในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="a4842-108">Then you can distribute it as an app to colleagues in your organization.</span></span>

<span data-ttu-id="a4842-109">เชื่อมต่อไปยัง[แอปเทมเพลต Zendesk](https://app.powerbi.com/getdata/services/zendesk)หรืออ่านเพิ่มเติมเกี่ยวกับการ[รวม Zendesk](https://powerbi.microsoft.com/integrations/zendesk)กับ Power BI</span><span class="sxs-lookup"><span data-stu-id="a4842-109">Connect to the [Zendesk template app](https://app.powerbi.com/getdata/services/zendesk) or read more about the [Zendesk integration](https://powerbi.microsoft.com/integrations/zendesk) with Power BI.</span></span>

<span data-ttu-id="a4842-110">หลังจากที่คุณได้ติดตั้งแอปแบบเทมเพลตแล้ว คุณสามารถเปลี่ยนแดชบอร์ดและรายงานได้</span><span class="sxs-lookup"><span data-stu-id="a4842-110">After you've installed the template app, you can change the dashboard and report.</span></span> <span data-ttu-id="a4842-111">จากนั้นคุณสามารถเผยแพร่เป็นแอปไปยังเพื่อนร่วมงานในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="a4842-111">Then you can distribute it as an app to colleagues in your organization.</span></span>

>[!NOTE]
><span data-ttu-id="a4842-112">คุณจำเป็นต้องมีบัญชีผู้ดูแลระบบ Zendesk เพื่อเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="a4842-112">You need a Zendesk Admin account to connect.</span></span> <span data-ttu-id="a4842-113">รายละเอียดเพิ่มเติมเกี่ยวกับ[ข้อกำหนด](#system-requirements) อยู่ที่ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="a4842-113">More details on [requirements](#system-requirements) below.</span></span>

>[!WARNING]
><span data-ttu-id="a4842-114">ก่อนวันที่ 15 ต.ค. 2019 นั้น Zendesk Support Search API อนุญาตให้ได้รับผลลัพธ์รวม 200,000 รายการ ผ่านการแบ่งหน้าของคิวรีขนาดใหญ่</span><span class="sxs-lookup"><span data-stu-id="a4842-114">Before Oct 15, 2019, the Zendesk Support Search API allowed for a total of 200,000 results to be received through pagination of large queries.</span></span> <span data-ttu-id="a4842-115">เพื่อจัดแนวการใช้งานการค้นหาให้สอดคล้องกับขอบเขตที่ตั้งใจไว้ ตอนนี้ Zendesk จำกัดจำนวนผลลัพธ์สูงสุดที่ส่งคืนเท่ากับ 1,000 รายการ โดยมีผลลัพธ์สูงสุด 100 รายการต่อหน้า</span><span class="sxs-lookup"><span data-stu-id="a4842-115">To align search usage with its intended scope, Zendesk now limits the maximum number of results returned to 1,000 total results, with a maximum of 100 results per page.</span></span> <span data-ttu-id="a4842-116">อย่างไรก็ตาม ตัวเชื่อมต่อ Zendesk Power BI ปัจจุบันยังคงสามารถสร้างการเรียกใช้ API ที่เกินขีดจำกัดใหม่เหล่านี้ส่งผลให้เกิดผลลัพธ์ที่อาจทำให้เข้าใจผิดได้</span><span class="sxs-lookup"><span data-stu-id="a4842-116">However, the current Power BI Zendesk connector can still create API calls that exceed these new limits, resulting in possibly misleading results.</span></span>

## <a name="how-to-connect"></a><span data-ttu-id="a4842-117">วิธีการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="a4842-117">How to connect</span></span>

[!INCLUDE [powerbi-service-apps-get-more-apps](../includes/powerbi-service-apps-get-more-apps.md)]

3. <span data-ttu-id="a4842-118">เลือก **Zendesk** \> **รับทันที**</span><span class="sxs-lookup"><span data-stu-id="a4842-118">Select **Zendesk** \> **Get it now**.</span></span>
4. <span data-ttu-id="a4842-119">ใน **ติดตั้งแอป Power BI นี้หรือไม่** เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="a4842-119">In **Install this Power BI App?** select **Install**.</span></span>
4. <span data-ttu-id="a4842-120">ในบานหน้าต่าง **แอป** เลือกไทล์ **Zendesk**</span><span class="sxs-lookup"><span data-stu-id="a4842-120">In the **Apps** pane, select the **Zendesk** tile.</span></span>

    ![ไทล์แอป Zendesk ของ Power BI](media/service-connect-to-zendesk/power-bi-zendesk-tile.png)

6. <span data-ttu-id="a4842-122">ในส่วน **เริ่มต้นใช้งานแอปใหม่ของคุณ** ให้เลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="a4842-122">In **Get started with your new app**, select **Connect**.</span></span>

    ![เริ่มต้นใช้งานแอปใหม่ของคุณ](media/service-connect-to-zendesk/power-bi-new-app-connect-get-started.png)

4. <span data-ttu-id="a4842-124">ให้ URL ที่เชื่อมโยงกับบัญชีของคุณ</span><span class="sxs-lookup"><span data-stu-id="a4842-124">Provide the URL associated with your account.</span></span> <span data-ttu-id="a4842-125">URL มีฟอร์ม **https://company.zendesk.com**</span><span class="sxs-lookup"><span data-stu-id="a4842-125">The URL has the form **https://company.zendesk.com**.</span></span> <span data-ttu-id="a4842-126">ดูรายละเอียดที่ [การค้นหาพารามิเตอร์เหล่านี้](#finding-parameters) ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="a4842-126">See details on [finding these parameters](#finding-parameters) below.</span></span>
   
   ![เชื่อมต่อกับ Zendesk](media/service-connect-to-zendesk/pbi_zendeskconnect.png)

5. <span data-ttu-id="a4842-128">เมื่อมีข้อความปรากฏ ใส่ข้อมูลประจำตัวของ Zendesk</span><span class="sxs-lookup"><span data-stu-id="a4842-128">When prompted, enter your Zendesk credentials.</span></span>  <span data-ttu-id="a4842-129">เลือก **oAuth 2** เป็นกลไกการรับรองความถูกต้อง แล้วคลิก **ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="a4842-129">Select **oAuth 2** as the Authentication Mechanism and click **Sign In**.</span></span> <span data-ttu-id="a4842-130">ทำตามขั้นตอนการรับรองความถูกต้อง Zendesk</span><span class="sxs-lookup"><span data-stu-id="a4842-130">Follow the Zendesk authentication flow.</span></span> <span data-ttu-id="a4842-131">(ถ้าคุณลงชื่อเข้าใช้ Zendesk อยู่แล้วในเบราว์เซอร์ของคุณ คุณอาจไม่ได้รับข้อความปรากฏให้ใส่ข้อมูลประจำตัว)</span><span class="sxs-lookup"><span data-stu-id="a4842-131">(If you're already signed in to Zendesk in your browser, you may not be prompted for credentials.)</span></span>
   
   > [!NOTE]
   > <span data-ttu-id="a4842-132">แอปเทมเพลตนี้ต้องการให้คุณเชื่อมต่อกับบัญชีผู้ดูแลระบบ Zendesk</span><span class="sxs-lookup"><span data-stu-id="a4842-132">This template app requires that you connect with a Zendesk Admin account.</span></span> 
   > 
   
   ![ลงชื่อเข้าใช้ด้วย OAuth2](media/service-connect-to-zendesk/pbi_zendesksignin.png)
6. <span data-ttu-id="a4842-134">คลิก **อนุญาต** เพื่ออนุญาตให้ Power BI เข้าถึงข้อมูล Zendesk ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a4842-134">Click **Allow** to allow Power BI to access your Zendesk data.</span></span>
   
   ![คลิกอนุญาต](media/service-connect-to-zendesk/zendesk2.jpg)
7. <span data-ttu-id="a4842-136">คลิก **เชื่อมต่อ** เพื่อเริ่มกระบวนการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="a4842-136">Click **Connect** to begin the import process.</span></span> 
8. <span data-ttu-id="a4842-137">หลังจากที่ Power BI นำเข้าข้อมูลคุณจะเห็นรายการเนื้อหาสำหรับแอ Zendesk ของคุณ: แดชบอร์ด รายงานและชุดข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="a4842-137">After Power BI imports the data, you see the content list for your Zendesk app: a new dashboard, report, and dataset.</span></span>
9. <span data-ttu-id="a4842-138">เลือกแดชบอร์ดที่จะเริ่มต้นกระบวนการสำรวจ</span><span class="sxs-lookup"><span data-stu-id="a4842-138">Select the dashboard to start the exploration process.</span></span>

    ![แดชบอร์ด Zendesk](media/service-connect-to-zendesk/power-bi-zendesk-dashboard.png)
   
## <a name="modify-and-distribute-your-app"></a><span data-ttu-id="a4842-140">ปรับเปลี่ยนและเผยแพร่แอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="a4842-140">Modify and distribute your app</span></span>

<span data-ttu-id="a4842-141">คุณได้ติดตั้งแอปเทมเพลต Zendesk</span><span class="sxs-lookup"><span data-stu-id="a4842-141">You've installed the Zendesk template app.</span></span> <span data-ttu-id="a4842-142">ซึ่งหมายความว่าคุณยังได้สร้างพื้นที่ทำงานของ Zendesk อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="a4842-142">That means you've also created the Zendesk workspace.</span></span> <span data-ttu-id="a4842-143">ในพื้นที่ทำงาน คุณสามารถเปลี่ยนรายงานและแดชบอร์ด จากนั้นเผยแพร่เป็น *แอป* ไปยังเพื่อนร่วมงานในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="a4842-143">In the workspace, you can change the report and dashboard, and then distribute it as an *app* to colleagues in your organization.</span></span> 

1. <span data-ttu-id="a4842-144">หากต้องการดูเนื้อหาทั้งหมดของพื้นที่ทำงาน Zendesk ใหม่ของคุณในบานหน้าต่างนำทาง เลือก **พื้นที่ทำงาน** > **Zendesk**</span><span class="sxs-lookup"><span data-stu-id="a4842-144">To view all the contents of your new Zendesk workspace, in the nav pane, select **Workspaces** > **Zendesk**.</span></span> 

    ![พื้นที่ทำงาน Zendesk ในบานหน้าต่างนำทาง](media/service-connect-to-zendesk/power-bi-zendesk-workspace-left-nav.png)

    <span data-ttu-id="a4842-146">มุมมองนี้เป็นรายการเนื้อหาสำหรับพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="a4842-146">This view is the content list for the workspace.</span></span> <span data-ttu-id="a4842-147">ที่มุมบนขวา คุณจะเห็น **อัปเดตแอป**</span><span class="sxs-lookup"><span data-stu-id="a4842-147">In the upper-right corner, you see **Update app**.</span></span> <span data-ttu-id="a4842-148">เมื่อคุณพร้อมที่จะเผยแพร่แอปของคุณไปยังเพื่อนร่วมงานของคุณ นั่นคือที่ที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a4842-148">When you're ready to distribute your app to your colleagues, that's where you'll start.</span></span> 

    ![รายการเนื้อหา Zendesk](media/service-connect-to-zendesk/power-bi-zendesk-content-list.png)

2. <span data-ttu-id="a4842-150">เลือก **รายงาน** และ **ชุดข้อมูล** เพื่อดูองค์ประกอบอื่น ๆ ในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="a4842-150">Select **Reports** and **Datasets** to see the other elements in the workspace.</span></span>

    <span data-ttu-id="a4842-151">อ่านเกี่ยวกับ [การเผยแพร่แอป](../collaborate-share/service-create-distribute-apps.md) ให้เพื่อนร่วมงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="a4842-151">Read about [distributing apps](../collaborate-share/service-create-distribute-apps.md) to your colleagues.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="a4842-152">ความต้องการของระบบ</span><span class="sxs-lookup"><span data-stu-id="a4842-152">System requirements</span></span>
<span data-ttu-id="a4842-153">บัญชีผู้ดูแลระบบ Zendesk จำเป็นสำหรับการเข้าถึงแอปเทมเพลต Zendesk</span><span class="sxs-lookup"><span data-stu-id="a4842-153">A Zendesk Administrator account is required to access the Zendesk template app.</span></span> <span data-ttu-id="a4842-154">ถ้าคุณตัวแทนหรือเป็นผู้ใช้ปลายทาง และคุณสนใจดูข้อมูล Zendesk ของคุณ เพิ่มคำแนะนำและตรวจทานตัวเชื่อมต่อ Zendesk ใน [Power BI Desktop](desktop-connect-to-data.md)</span><span class="sxs-lookup"><span data-stu-id="a4842-154">If you're an agent or an end user and are interested in viewing your Zendesk data, add a suggestion and review the Zendesk connector in the [Power BI Desktop](desktop-connect-to-data.md).</span></span>

## <a name="finding-parameters"></a><span data-ttu-id="a4842-155">การค้นหาพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="a4842-155">Finding parameters</span></span>
<span data-ttu-id="a4842-156">URL ของ Zendesk ของคุณจะเหมือนกับ URL ที่คุณใช้เพื่อลงชื่อเข้าใช้บัญชี Zendesk ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a4842-156">Your Zendesk URL will be the same as the URL you use to sign into your Zendesk account.</span></span> <span data-ttu-id="a4842-157">ถ้าคุณไม่แน่ใจใน URL ของ Zendesk ของคุณ คุณสามารถใช้ตัว[ช่วยเหลือในการเข้าสู่ระบบ](https://www.zendesk.com/login/) สำหรับ Zendesk ได้</span><span class="sxs-lookup"><span data-stu-id="a4842-157">If you're not sure of your Zendesk URL, you can use the Zendesk [login help](https://www.zendesk.com/login/).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="a4842-158">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="a4842-158">Troubleshooting</span></span>
<span data-ttu-id="a4842-159">ถ้าคุณมีปัญหาในการเชื่อมต่อ ตรวจสอบ URL ของ Zendesk ของคุณ และยืนยันว่าคุณกำลังใช้บัญชีผู้ดูแลระบบ Zendesk</span><span class="sxs-lookup"><span data-stu-id="a4842-159">If you're having issues connecting, check your Zendesk URL and confirm you're using a Zendesk administrator account.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a4842-160">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a4842-160">Next steps</span></span>

* [<span data-ttu-id="a4842-161">สร้างพื้นที่ทำงานใหม่ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="a4842-161">Create the new workspaces in Power BI</span></span>](../collaborate-share/service-create-the-new-workspaces.md)
* [<span data-ttu-id="a4842-162">ติดตั้งและใช้แอปฯใน Power BI</span><span class="sxs-lookup"><span data-stu-id="a4842-162">Install and use apps in Power BI</span></span>](../consumer/end-user-apps.md)
* [<span data-ttu-id="a4842-163">เชื่อมต่อกับแอป Power BI สำหรับบริการภายนอก</span><span class="sxs-lookup"><span data-stu-id="a4842-163">COnnect to Power BI apps for external services</span></span>](service-connect-to-services.md)
* <span data-ttu-id="a4842-164">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a4842-164">Questions?</span></span> [<span data-ttu-id="a4842-165">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="a4842-165">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
