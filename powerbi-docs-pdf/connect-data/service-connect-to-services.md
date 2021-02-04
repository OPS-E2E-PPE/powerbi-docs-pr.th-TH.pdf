---
title: เชื่อมต่อกับบริการที่คุณใช้กับ Power BI
description: เชื่อมต่อกับบริการที่คุณใช้จำนวนมาก เพื่อเรียกใช้ธุรกิจของคุณ เช่น Salesforce, Microsoft Dynamics CRM และ Google Analytics
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 08/29/2019
LocalizationGroup: Connect to services
ms.openlocfilehash: a2151f80a9c8da7230338355fb10b9a0820286a1
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410516"
---
# <a name="connect-to-the-services-you-use-with-power-bi"></a><span data-ttu-id="c7f1f-103">เชื่อมต่อกับบริการที่คุณใช้กับ Power BI</span><span class="sxs-lookup"><span data-stu-id="c7f1f-103">Connect to the services you use with Power BI</span></span>
<span data-ttu-id="c7f1f-104">ด้วย Power BI คุณสามารถเชื่อมต่อกับบริการที่คุณใช้จำนวนมาก เพื่อเรียกใช้ธุรกิจของคุณ เช่น Salesforce, Microsoft Dynamics CRM และ Google Analytics</span><span class="sxs-lookup"><span data-stu-id="c7f1f-104">With Power BI, you can connect to many of the services you use to run your business, such as Salesforce, Microsoft Dynamics, and Google Analytics.</span></span> <span data-ttu-id="c7f1f-105">Power BI เริ่มต้นโดยใช้ข้อมูลประจำตัวของคุณเพื่อเชื่อมต่อกับบริการ</span><span class="sxs-lookup"><span data-stu-id="c7f1f-105">Power BI starts by using your credentials to connect to the service.</span></span> <span data-ttu-id="c7f1f-106">และจากนั้นสร้าง *พื้นที่ทำงาน* Power BI ด้วยแดชบอร์ดและชุดของรายงาน Power BI ที่แสดงข้อมูลของคุณและให้ข้อมูลภาพเชิงลึกเกี่ยวกับธุรกิจของคุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c7f1f-106">It creates a Power BI *workspace* with a dashboard and a set of Power BI reports that automatically show your data and provide visual insights about your business.</span></span>

>[!IMPORTANT]
><span data-ttu-id="c7f1f-107">ชุดเนื้อหาของบริการจะถูกแทนที่ด้วย [แอปเทมเพลต](./service-template-apps-overview.md)</span><span class="sxs-lookup"><span data-stu-id="c7f1f-107">Service content packs are being replaced by [Template apps](./service-template-apps-overview.md).</span></span> <span data-ttu-id="c7f1f-108">ตั้งแต่วันที่ 25 กันยายน 2019 มีชุดเนื้อหาจำนวนหนึ่งที่เลิกใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c7f1f-108">As of September 25, 2019, a number of content packs have already been deprecated.</span></span> <span data-ttu-id="c7f1f-109">ชุดเนื้อหาที่เลิกใช้แล้วที่คุณเคยติดตั้งจะยังคงอยู่ในบัญชีของคุณ แต่จะไม่มีเอกสารประกอบหรือการสนับสนุน และจะไม่สามารถติดตั้งได้อีก</span><span class="sxs-lookup"><span data-stu-id="c7f1f-109">Any deprecated content pack that you have installed will remain in your account, but no documentation or support will be provided for it, nor will it be possible to install it again.</span></span>

<span data-ttu-id="c7f1f-110">เข้าสู่ระบบ Power BI เพื่อดู[บริการที่คุณสามารถเชื่อมต่อ](https://app.powerbi.com/getdata/services)ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c7f1f-110">Sign in to Power BI to view all of the [services you can connect to](https://app.powerbi.com/getdata/services).</span></span> 

![แอป AppSource](media/service-connect-to-services/overview.png)

<span data-ttu-id="c7f1f-112">หลังจากที่คุณติดตั้งแอป คุณสามารถดูแดชบอร์ดและรายงานในแอปและพื้นที่ทำงานในบริการของ Power BI ([https://app.powerbi.com](https://app.powerbi.com))</span><span class="sxs-lookup"><span data-stu-id="c7f1f-112">After you install the app, you can view the dashboard and reports in the app and the workspace in the Power BI service ([https://app.powerbi.com](https://app.powerbi.com)).</span></span> <span data-ttu-id="c7f1f-113">นอกจากนี้ คุณยังสามารถดูข้อมูลได้ในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="c7f1f-113">You can also view them in the Power BI mobile apps.</span></span> <span data-ttu-id="c7f1f-114">ในพื้นที่ทำงาน คุณสามารถปรับเปลี่ยนแดชบอร์ดและรายงานตามความต้องการขององค์กรของคุณ และแจกจ่ายให้เพื่อนร่วมงานของคุณเป็น *แอป* ได้</span><span class="sxs-lookup"><span data-stu-id="c7f1f-114">In the workspace, you can modify the dashboard and reports to meet the needs of your organization, and then distribute them to your colleagues as an *app*.</span></span> 

![แอป Google analytics ในแอปมือถือ Power BI](media/service-connect-to-services/power-bi-service-mobile-app-240.png)

## <a name="get-started"></a><span data-ttu-id="c7f1f-116">เริ่มใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c7f1f-116">Get started</span></span>
[!INCLUDE [powerbi-service-apps-get-more-apps](../includes/powerbi-service-apps-get-more-apps.md)]

## <a name="edit-the-dashboard-and-reports"></a><span data-ttu-id="c7f1f-117">แก้ไขแดชบอร์ดและรายงาน</span><span class="sxs-lookup"><span data-stu-id="c7f1f-117">Edit the dashboard and reports</span></span>
<span data-ttu-id="c7f1f-118">เมื่อการนำเข้าเสร็จสมบูรณ์ แอปใหม่จะปรากฏบนหน้าแอป</span><span class="sxs-lookup"><span data-stu-id="c7f1f-118">When the import is complete, the new app appears on the Apps page.</span></span>

1. <span data-ttu-id="c7f1f-119">เลือก **แอป** ในบานหน้าต่างนำทาง > เลือกแอป</span><span class="sxs-lookup"><span data-stu-id="c7f1f-119">Select **Apps** in the nav pane > select the app.</span></span>
   
     ![หน้าแอป](media/service-connect-to-services/power-bi-service-apps-open-app.png)
2. <span data-ttu-id="c7f1f-121">คุณสามารถถามคำถามโดยการพิมพ์ในกล่องถามตอบ หรือคลิกที่ไทล์เพื่อเปิดรายงานพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="c7f1f-121">You can ask a question by typing in the Q&A box, or click a tile to open the underlying report.</span></span> 
   
    ![แดชบอร์ Google Analytics](media/service-connect-to-services/googleanalytics2.png)
   
    <span data-ttu-id="c7f1f-123">เปลี่ยนแดชบอร์ดและรายงานเพื่อให้เหมาะสมกับความต้องการขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7f1f-123">Change the dashboard and report to fit the needs of your organization.</span></span> <span data-ttu-id="c7f1f-124">จากนั้น[แจกจ่ายแอปของคุณไปยังเพื่อนร่วมงานของคุณ](../collaborate-share/service-create-distribute-apps.md)</span><span class="sxs-lookup"><span data-stu-id="c7f1f-124">Then [distribute your app to your colleagues](../collaborate-share/service-create-distribute-apps.md)</span></span>

## <a name="whats-included"></a><span data-ttu-id="c7f1f-125">มีอะไรรวมอยู่บ้าง</span><span class="sxs-lookup"><span data-stu-id="c7f1f-125">What's included</span></span>
<span data-ttu-id="c7f1f-126">หลังจากเชื่อมต่อกับบริการ คุณเห็นแอปและพื้นที่ทำงานที่สร้างขึ้นใหม่ด้วยแดชบอร์ด รายงาน และชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c7f1f-126">After connecting to a service, you see a newly created app and workspace with a dashboard, reports, and dataset.</span></span> <span data-ttu-id="c7f1f-127">ข้อมูลจากบริการจะเน้นไปที่สถานการณ์เฉพาะ และอาจรวมถึงข้อมูลทั้งหมดจากบริการ</span><span class="sxs-lookup"><span data-stu-id="c7f1f-127">The data from the service is focused on a specific scenario and may not include all the information from the service.</span></span> <span data-ttu-id="c7f1f-128">ข้อมูลมีการจัดกำหนดการการรีเฟรชโดยอัตโนมัตหนึ่งครั้งต่อวัน</span><span class="sxs-lookup"><span data-stu-id="c7f1f-128">The data is scheduled to refresh automatically once per day.</span></span> <span data-ttu-id="c7f1f-129">คุณสามารถควบคุมการกำหนดเวลาโดยการเลือกชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c7f1f-129">You can control the schedule by selecting the dataset.</span></span>

<span data-ttu-id="c7f1f-130">คุณยังสามารถ[เชื่อมต่อกับบริการมากมายใน Power BI Desktop](desktop-data-sources.md) เช่น Google Analytics และสร้างแดชบอร์ดและรายงานที่กำหนดเองของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="c7f1f-130">You can also [connect to many services in Power BI Desktop](desktop-data-sources.md), such as Google Analytics, and create your own customized dashboards and reports.</span></span>  

<span data-ttu-id="c7f1f-131">สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับการเชื่อมต่อกับบริการที่เฉพาะเจาะจง โปรดดูที่หน้าช่วยเหลือส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="c7f1f-131">For more details on connecting to specific services, refer to the individual help pages.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="c7f1f-132">แนวทางการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="c7f1f-132">Troubleshooting</span></span>
<span data-ttu-id="c7f1f-133">**ไทล์ที่ว่างเปล่า**</span><span class="sxs-lookup"><span data-stu-id="c7f1f-133">**Empty tiles**</span></span>  
<span data-ttu-id="c7f1f-134">ขณะที่ Power BI เชื่อมต่อไปยังบริการครั้งแรก คุณอาจเห็นชุดที่ว่างเปล่าของไทล์บนแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7f1f-134">While Power BI is first connecting to the service, you may see an empty set of tiles on your dashboard.</span></span> <span data-ttu-id="c7f1f-135">ถ้าคุณยังคงเห็นแดชบอร์ดว่างเปล่าหลังจากชั่วโมง 2 อาจเป็นได้ว่าการเชื่อมต่อล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="c7f1f-135">If you still see an empty dashboard after 2 hours, it's likely the connection failed.</span></span> <span data-ttu-id="c7f1f-136">ถ้าคุณไม่เห็นข้อความแสดงข้อผิดพลาดที่มีรายละเอียดในการแก้ไขปัญหา ให้ยื่นตั๋วการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="c7f1f-136">If you didn't see an error message with information on correcting the issue, file a support ticket.</span></span>

* <span data-ttu-id="c7f1f-137">เลือกไอคอนเครื่องหมายคำถาม ( **?** ) ที่มุมบนขวา > **รับความช่วยเหลือ**</span><span class="sxs-lookup"><span data-stu-id="c7f1f-137">Select the question mark icon (**?**) in the upper-right corner >  **Get help**.</span></span>
  
    ![ไอคอนรับความช่วยเหลือ](media/service-connect-to-services/power-bi-service-get-help.png)

<span data-ttu-id="c7f1f-139">**ข้อมูลที่หายไป**</span><span class="sxs-lookup"><span data-stu-id="c7f1f-139">**Missing information**</span></span>  
<span data-ttu-id="c7f1f-140">แดชบอร์ดและรายงานมีเนื้อหาข้อมูลจากบริการจะเน้นไปที่สถานการณ์เฉพาะ และอาจรวมถึงข้อมูลทั้งหมดจากบริการ</span><span class="sxs-lookup"><span data-stu-id="c7f1f-140">The dashboard and reports include content from the service focused on a specific scenario.</span></span> <span data-ttu-id="c7f1f-141">หากคุณกำลังมองหาเมตริกเฉพาะในแอปและไม่เห็น ให้เพิ่มแนวคิดบนหน้า[การสนับสนุน Power BI](https://support.powerbi.com/forums/265200-power-bi)</span><span class="sxs-lookup"><span data-stu-id="c7f1f-141">If you're looking for a specific metric in the app and don't see it, add an idea on the [Power BI Support](https://support.powerbi.com/forums/265200-power-bi) page.</span></span>

## <a name="suggesting-services"></a><span data-ttu-id="c7f1f-142">บริการให้คำปรึกษา</span><span class="sxs-lookup"><span data-stu-id="c7f1f-142">Suggesting services</span></span>
<span data-ttu-id="c7f1f-143">คุณใช้บริการและคุณต้องการให้คำแนะนำแอป Power BI ใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c7f1f-143">Do you use a service you'd like to suggest for a Power BI app?</span></span> <span data-ttu-id="c7f1f-144">ไปที่[สนับสนุน Power BI ](https://support.powerbi.com/forums/265200-power-bi)หน้า และแจ้งให้เราทราบ</span><span class="sxs-lookup"><span data-stu-id="c7f1f-144">Go to the [Power BI Support](https://support.powerbi.com/forums/265200-power-bi) page and let us know.</span></span>

<span data-ttu-id="c7f1f-145">ถ้าคุณสนใจในการสร้างแอปแม่แบบเพื่อกระจายด้วยตนเอง ดู[สร้างแอปแม่แบบใน Power BI](service-template-apps-create.md)</span><span class="sxs-lookup"><span data-stu-id="c7f1f-145">If you're interested in creating template apps to distribute yourself, see [Create a template app in Power BI](service-template-apps-create.md).</span></span> <span data-ttu-id="c7f1f-146">คู่ค้า Power BI สามารถสร้างแอป Power BI ด้วยโค๊ดเพียงเล็กน้อยหรือไม่มีเลย และปรับใช้กับลูกค้า Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="c7f1f-146">Power BI partners can build Power BI apps with little or no coding, and deploy them to Power BI customers.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="c7f1f-147">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c7f1f-147">Next steps</span></span>
* [<span data-ttu-id="c7f1f-148">แจกจ่ายแอปไปยังเพื่อนร่วมงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7f1f-148">Distribute apps to your colleagues</span></span>](../collaborate-share/service-create-distribute-apps.md)
* [<span data-ttu-id="c7f1f-149">สร้างพื้นที่ทำงานใหม่ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="c7f1f-149">Create the new workspaces in Power BI</span></span>](../collaborate-share/service-create-the-new-workspaces.md)
* <span data-ttu-id="c7f1f-150">มีคำถามหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="c7f1f-150">Questions?</span></span> [<span data-ttu-id="c7f1f-151">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="c7f1f-151">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)