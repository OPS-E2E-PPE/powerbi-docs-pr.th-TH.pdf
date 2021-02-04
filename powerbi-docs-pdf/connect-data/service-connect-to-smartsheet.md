---
title: เชื่อมต่อกับ Smartsheet ด้วย Power BI
description: Smartsheet สำหรับ Power BI
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: how-to
ms.date: 05/04/2020
LocalizationGroup: Connect to services
ms.openlocfilehash: 446c9dd1af2322cca164762ae212ba247b8916ba
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96392921"
---
# <a name="connect-to-smartsheet-with-power-bi"></a><span data-ttu-id="3259a-103">เชื่อมต่อกับ Smartsheet ด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="3259a-103">Connect to Smartsheet with Power BI</span></span>
<span data-ttu-id="3259a-104">บทความนี้จะแนะนำคุณในการดึงข้อมูลของคุณจากบัญชี Smartsheet ของคุณด้วยแอปเทมเพลตของ Power BI</span><span class="sxs-lookup"><span data-stu-id="3259a-104">This article walks you through pulling your data from your Smartsheet account with a Power BI template app.</span></span> <span data-ttu-id="3259a-105">Smartsheet มีแพลตฟอร์มอย่างง่าย สำหรับการทำงานร่วมกันและการแชร์ไฟล์</span><span class="sxs-lookup"><span data-stu-id="3259a-105">Smartsheet offers an easy platform for collaboration and file sharing.</span></span> <span data-ttu-id="3259a-106">แอปเทมเพลต Smartsheet สำหรับ Power BI มีแดชบอร์ด รายงาน และชุดข้อมูลที่แสดงภาพรวมของบัญชี Smartsheet ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3259a-106">The Smartsheet template app for Power BI provides a dashboard, reports, and dataset that show an overview of your Smartsheet account.</span></span> <span data-ttu-id="3259a-107">คุณยังสามารถใช้ [Power BI Desktop](desktop-connect-to-data.md) เพื่อเชื่อมต่อโดยตรงไปยังแต่ละแผ่นงานในบัญชีของคุณได้</span><span class="sxs-lookup"><span data-stu-id="3259a-107">You can also use [Power BI Desktop](desktop-connect-to-data.md) to connect directly to individual sheets in your account.</span></span> 

<span data-ttu-id="3259a-108">หลังจากที่คุณได้ติดตั้งแอปแบบเทมเพลตแล้ว คุณสามารถเปลี่ยนแดชบอร์ดและรายงานได้</span><span class="sxs-lookup"><span data-stu-id="3259a-108">After you've installed the template app, you can change the dashboard and report.</span></span> <span data-ttu-id="3259a-109">จากนั้นคุณสามารถเผยแพร่เป็นแอปไปยังเพื่อนร่วมงานในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="3259a-109">Then you can distribute it as an app to colleagues in your organization.</span></span>

<span data-ttu-id="3259a-110">เชื่อมต่อไปยัง[แอปเทมเพลต Smartsheet](https://app.powerbi.com/groups/me/getapps/services/pbi-contentpacks.pbiapps-smartsheet)สำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="3259a-110">Connect to the [Smartsheet template app](https://app.powerbi.com/groups/me/getapps/services/pbi-contentpacks.pbiapps-smartsheet) for Power BI.</span></span>

>[!NOTE]
><span data-ttu-id="3259a-111">บัญชีผู้ดูแลระบบ Smartsheet เป็นที่ต้องการสำหรับการเชื่อมต่อและการโหลดแอปเทมเพลต Power BI ที่มีการเข้าถึงเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3259a-111">A Smartsheet admin account is preferred for connecting and loading the Power BI template app as it has additional access.</span></span>

## <a name="how-to-connect"></a><span data-ttu-id="3259a-112">วิธีการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="3259a-112">How to connect</span></span>

[!INCLUDE [powerbi-service-apps-get-more-apps](../includes/powerbi-service-apps-get-more-apps.md)]

3. <span data-ttu-id="3259a-113">เลือก **Smartsheet** \> **รับทันที**</span><span class="sxs-lookup"><span data-stu-id="3259a-113">Select **Smartsheet** \> **Get it now**.</span></span>
4. <span data-ttu-id="3259a-114">ใน **ติดตั้งแอป Power BI นี้หรือไม่** เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="3259a-114">In **Install this Power BI App?** select **Install**.</span></span>
4. <span data-ttu-id="3259a-115">ในบานหน้าต่าง **แอป** เลือกไทล์ **Smartsheet**</span><span class="sxs-lookup"><span data-stu-id="3259a-115">In the **Apps** pane, select the **Smartsheet** tile.</span></span>

    ![ไทล์แอป Smartsheet ของ Power BI](media/service-connect-to-smartsheet/power-bi-smartsheet-tile.png)

6. <span data-ttu-id="3259a-117">ในส่วน **เริ่มต้นใช้งานแอปใหม่ของคุณ** ให้เลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="3259a-117">In **Get started with your new app**, select **Connect**.</span></span>

    ![เริ่มต้นใช้งานแอปใหม่ของคุณ](media/service-connect-to-zendesk/power-bi-new-app-connect-get-started.png)

4. <span data-ttu-id="3259a-119">สำหรับวิธีการรับรองความถูกต้อง เลือก **oAuth2 \> ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="3259a-119">For Authentication Method, select **oAuth2 \> Sign In**.</span></span>
   
   <span data-ttu-id="3259a-120">เมื่อได้รับพร้อมท์ ใส่ข้อมูลประจำตัวของ Smartsheet และทำตามกระบวนการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="3259a-120">When prompted, enter your Smartsheet credentials and follow the authentication process.</span></span>
   
   ![ข้อมูลประจำตัว Smartsheet](media/service-connect-to-smartsheet/creds.png)
   
   ![ลงชื่อเข้าใช้ Smartsheet](media/service-connect-to-smartsheet/creds2.png)

5. <span data-ttu-id="3259a-123">หลังจากที่ Power BI นำเข้าข้อมูลแล้วแดชบอร์ด Smartsheet จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="3259a-123">After Power BI imports the data, the Smartsheet dashboard opens.</span></span>
   
   ![แดชบอร์ด Smartsheet](media/service-connect-to-smartsheet/power-bi-smartsheet-dashboard.png)

## <a name="modify-and-distribute-your-app"></a><span data-ttu-id="3259a-125">ปรับเปลี่ยนและเผยแพร่แอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="3259a-125">Modify and distribute your app</span></span>

<span data-ttu-id="3259a-126">คุณได้ติดตั้งแอปเทมเพลต Smartsheet</span><span class="sxs-lookup"><span data-stu-id="3259a-126">You've installed the Smartsheet template app.</span></span> <span data-ttu-id="3259a-127">ซึ่งหมายความว่าคุณยังได้สร้างพื้นที่ทำงานของแอป Smartsheet อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="3259a-127">That means you've also created the Smartsheet workspace.</span></span> <span data-ttu-id="3259a-128">ในพื้นที่ทำงาน คุณสามารถเปลี่ยนรายงานและแดชบอร์ด จากนั้นเผยแพร่เป็น *แอป* ไปยังเพื่อนร่วมงานในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="3259a-128">In the workspace, you can change the report and dashboard, and then distribute it as an *app* to colleagues in your organization.</span></span> 

1. <span data-ttu-id="3259a-129">หากต้องการดูเนื้อหาทั้งหมดของพื้นที่ทำงาน Smartsheet ใหม่ของคุณในบานหน้าต่างนำทาง เลือก **พื้นที่ทำงาน** > **Smartsheet**</span><span class="sxs-lookup"><span data-stu-id="3259a-129">To view all the contents of your new Smartsheet workspace, in the nav pane, select **Workspaces** > **Smartsheet**.</span></span> 

    ![พื้นที่ทำงาน Smartsheet ในบานหน้าต่างนำทาง](media/service-connect-to-smartsheet/power-bi-smartsheet-workspace.png)

    <span data-ttu-id="3259a-131">มุมมองนี้เป็นรายการเนื้อหาสำหรับพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="3259a-131">This view is the content list for the workspace.</span></span> <span data-ttu-id="3259a-132">ที่มุมบนขวา คุณจะเห็น **อัปเดตแอป**</span><span class="sxs-lookup"><span data-stu-id="3259a-132">In the upper-right corner, you see **Update app**.</span></span> <span data-ttu-id="3259a-133">เมื่อคุณพร้อมที่จะเผยแพร่แอปของคุณไปยังเพื่อนร่วมงานของคุณ นั่นคือที่ที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3259a-133">When you're ready to distribute your app to your colleagues, that's where you'll start.</span></span> 

    ![รายการเนื้อหา Smartsheet](media/service-connect-to-smartsheet/power-bi-smartsheet-workspace-content.png)

2. <span data-ttu-id="3259a-135">เลือก **รายงาน** และ **ชุดข้อมูล** เพื่อดูองค์ประกอบอื่น ๆ ในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="3259a-135">Select **Reports** and **Datasets** to see the other elements in the workspace.</span></span>

    <span data-ttu-id="3259a-136">อ่านเกี่ยวกับ [การเผยแพร่แอป](../collaborate-share/service-create-distribute-apps.md) ให้เพื่อนร่วมงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="3259a-136">Read about [distributing apps](../collaborate-share/service-create-distribute-apps.md) to your colleagues.</span></span>

## <a name="whats-included"></a><span data-ttu-id="3259a-137">มีอะไรรวมอยู่บ้าง</span><span class="sxs-lookup"><span data-stu-id="3259a-137">What's included</span></span>
<span data-ttu-id="3259a-138">แอปเทมเพลต Smartsheet สำหรับ Power BI มีภาพรวมของบัญชี Smartsheet ของคุณ เช่น จำนวนของพื้นที่ทำงาน รายงาน และแผ่นงานที่คุณมี เมื่อใดที่ถูกแก้ไข ฯลฯ ผู้ใช้ที่เป็นผู้ดูแลระบบยังเห็นข้อมูลเกี่ยวกับผู้ใช้ในระบบของพวกเขา เช่น ผู้ที่สร้างแผ่นงานอันดับต้น ๆ</span><span class="sxs-lookup"><span data-stu-id="3259a-138">The Smartsheet template app for Power BI includes an overview of your Smartsheet account, such as the number of workspaces, reports, and sheets you have, when they're modified etc. Admin users also see some information around the users in their system, such as top sheet creators.</span></span>  

<span data-ttu-id="3259a-139">เพื่อเชื่อมต่อโดยตรงไปยังแต่ละแผ่นงานในบัญชีของคุณ คุณสามารถใช้ตัวเชื่อมต่อ Smartsheet ใน [Power BI Desktop](desktop-connect-to-data.md) ได้</span><span class="sxs-lookup"><span data-stu-id="3259a-139">To connect directly to individual sheets in your account, you can use the Smartsheet connector in the [Power BI Desktop](desktop-connect-to-data.md).</span></span>  

## <a name="next-steps"></a><span data-ttu-id="3259a-140">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3259a-140">Next steps</span></span>

* [<span data-ttu-id="3259a-141">สร้างพื้นที่ทำงานใหม่ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3259a-141">Create the new workspaces in Power BI</span></span>](../collaborate-share/service-create-the-new-workspaces.md)
* [<span data-ttu-id="3259a-142">ติดตั้งและใช้แอปฯใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3259a-142">Install and use apps in Power BI</span></span>](../consumer/end-user-apps.md)
* [<span data-ttu-id="3259a-143">เชื่อมต่อกับแอป Power BI สำหรับบริการภายนอก</span><span class="sxs-lookup"><span data-stu-id="3259a-143">COnnect to Power BI apps for external services</span></span>](service-connect-to-services.md)
* <span data-ttu-id="3259a-144">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3259a-144">Questions?</span></span> [<span data-ttu-id="3259a-145">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="3259a-145">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)