---
title: เชื่อมต่อกับ Project Online ด้วย Power BI
description: Project Online สำหรับ Power BI
author: paulinbar
ms.author: painbar
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: how-to
ms.date: 07/25/2019
LocalizationGroup: Connect to services
ms.openlocfilehash: e5d97da4d643512396a17e95fb7cae2e841d7521
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96403294"
---
# <a name="connect-to-project-web-app-with-power-bi"></a><span data-ttu-id="fb060-103">เชื่อมต่อไปยัง Project Web App ด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="fb060-103">Connect to Project Web App with Power BI</span></span>
<span data-ttu-id="fb060-104">Microsoft Project Web App เป็นโซลูชันออนไลน์ที่ยืดหยุ่นสำหรับการจัดการพอร์ตโครงการ (PPM) และงานประจำวัน</span><span class="sxs-lookup"><span data-stu-id="fb060-104">Microsoft Project Web App is a flexible online solution for project portfolio management (PPM) and everyday work.</span></span> <span data-ttu-id="fb060-105">Project Web App ช่วยให้องค์กรสามารถเริ่มต้นและจัดลำดับความสำคัญการลงทุนในพอร์ตโครงการ และส่งมอบมูลค่าทางธุรกิจตามที่ต้องการได้</span><span class="sxs-lookup"><span data-stu-id="fb060-105">Project Web App enables organizations to get started, prioritize project portfolio investments and deliver the intended business value.</span></span> <span data-ttu-id="fb060-106">Project Web App Template App สำหรับ Power BI ช่วยให้คุณสามารถปลดล็อคข้อมูลเชิงลึกจาก Project Web App เพื่อจัดการโครงการ พอร์ตโครงการ และทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="fb060-106">The Project Web App Template App for Power BI allows you to unlock insight from Project Web App to help manage projects, portfolios and resources.</span></span>

<span data-ttu-id="fb060-107">เชื่อมต่อไปยัง [Project Web App Template App](https://appsource.microsoft.com/product/power-bi/pbi_msprojectonline.pbi-microsoftprojectwebapp) สำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="fb060-107">Connect to the [Project Web App Template App](https://appsource.microsoft.com/product/power-bi/pbi_msprojectonline.pbi-microsoftprojectwebapp) for Power BI.</span></span>

## <a name="how-to-connect"></a><span data-ttu-id="fb060-108">วิธีการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="fb060-108">How to connect</span></span>

1. <span data-ttu-id="fb060-109">เลือก **แอป** ในบานหน้าต่างนำทาง > เลือก **รับแอป** ในมุมบนขวา</span><span class="sxs-lookup"><span data-stu-id="fb060-109">Select **Apps** in the nav pane > select **Get apps** in the upper right corner.</span></span>

    ![รับแอป](media/service-connect-to-project-online/GetApps.png)

2. <span data-ttu-id="fb060-111">ในกล่อง **บริการ** เลือก **รับ**</span><span class="sxs-lookup"><span data-stu-id="fb060-111">In the **Services** box, select **Get**.</span></span>
   
   ![สกรีนช็อตจะแสดงหน้าต่าง AppSource พร้อมแอปห้ารายการที่พร้อมใช้งาน](media/service-connect-to-project-online/AppSource.png)
3. <span data-ttu-id="fb060-113">ใน AppSource เลือกแท็บ **Apps** และค้นหา/เลือก **Microsoft Project Web App**</span><span class="sxs-lookup"><span data-stu-id="fb060-113">In AppSource, select the **Apps** tab, and search/select **Microsoft Project Web App**.</span></span>
   
4. <span data-ttu-id="fb060-114">คุณจะได้รับข้อความที่บอกว่า - **ติดตั้งแอป Power BI นี้หรือไม่** เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="fb060-114">You will get a message saying - **Install this Power BI App?** select **Install**.</span></span> 

   ![ติดตั้งเว็บโครงการ](media/service-connect-to-project-online/ProjectTile.png)
5. <span data-ttu-id="fb060-116">ในบานหน้าต่าง **แอป** ให้เลือกไทล์ **Microsoft Project Web App**</span><span class="sxs-lookup"><span data-stu-id="fb060-116">In the **Apps** pane, select the **Microsoft Project Web App** tile.</span></span> 
   
   ![Microsoft Project Web App](media/service-connect-to-project-online/getstarted.png)
6. <span data-ttu-id="fb060-118">ใน **เริ่มต้นใช้งานแอปใหม่ของคุณ** ให้เลือก **เชื่อมต่อข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="fb060-118">In **Get started with your new app**, select **Connect data**.</span></span>
   
   ![เชื่อมต่อกับข้อมูล](media/service-connect-to-project-online/mproject.png)
7. <span data-ttu-id="fb060-120">ในกล่องข้อความ **Project Web App URL** ใส่ URL สำหรับ Project Web App (PWA) ที่คุณต้องการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="fb060-120">In the **Project Web App URL** text box, enter the URL for the Project Web App (PWA) you want to connect to.</span></span>  <span data-ttu-id="fb060-121">หมายเหตุ ส่วนนี้อาจแตกต่างจากตัวอย่างดังกล่าวถ้าคุณมีโดเมนแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="fb060-121">Note this may differ from the example if you have a custom domain.</span></span> <span data-ttu-id="fb060-122">ในกล่องข้อความ **PWA ไซต์ภาษา** พิมพ์หมายเลขที่แสดงภาษาของไซต์ PWA ของคุณ</span><span class="sxs-lookup"><span data-stu-id="fb060-122">In the **PWA Site Language** text box, type the number that corresponds to your PWA site language.</span></span> <span data-ttu-id="fb060-123">พิมพ์ตัวเลขหลักเดียว '1' สำหรับภาษาอังกฤษ '2' สำหรับภาษาฝรั่งเศส '3' สำหรับภาษาเยอรมัน '4' สำหรับภาษาโปรตุเกส (บราซิล), ' 5' สำหรับภาษาโปรตุเกส (โปรตุเกส) และ ' 6' สำหรับภาษาสเปน</span><span class="sxs-lookup"><span data-stu-id="fb060-123">Type the single digit '1' for English, '2' for French, '3' for German, '4' for Portuguese (Brazil), '5' for Portuguese (Portugal) and '6' for Spanish.</span></span> 
   
   ![เชื่อมต่อกับ Microsoft Project Online](media/service-connect-to-project-online/params.png)
8. <span data-ttu-id="fb060-125">สำหรับวิธีการรับรองความถูกต้อง ให้เลือก **oAuth2** \> **ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="fb060-125">For Authentication Method, select **oAuth2** \> **Sign In**.</span></span> <span data-ttu-id="fb060-126">เมื่อได้รับข้อความปรากฏขึ้น ให้ใส่ข้อมูลประจำตัวของ Project Web App และทำตามกระบวนการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="fb060-126">When prompted, enter your Project Web App credentials and follow the authentication process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb060-127">คุณจำเป็นต้องมีสิทธิ์การใช้งานสำหรับ Portfolio Viewer (ผู้ดูพอร์ตโครงการ) Portfolio Manager (ผู้จัดการพอร์ต) หรือ Administrator (ผู้ดูแลระบบ) สำหรับ Project Web App ที่คุณกำลังเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="fb060-127">You need to have Portfolio Viewer, Portfolio Manager, or Administrator permissions for the Project Web App you are connecting to.</span></span>

9. <span data-ttu-id="fb060-128">คุณจะเห็นการแจ้งเตือนที่ระบุว่า กำลังโหลดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="fb060-128">You’ll see a notification indicating your data is loading.</span></span> <span data-ttu-id="fb060-129">ขึ้นอยู่กับขนาดบัญชีของคุณ ซึ่งอาจใช้เวลาสักครู่</span><span class="sxs-lookup"><span data-stu-id="fb060-129">Depending on the size of your account this may take some time.</span></span> <span data-ttu-id="fb060-130">หลังจากที่ Power BI นำเข้าข้อมูลแล้ว คุณจะเห็นเนื้อหาของพื้นที่ทำงานใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="fb060-130">After Power BI imports the data, you will see the contents of your new workspace.</span></span> <span data-ttu-id="fb060-131">คุณอาจจำเป็นต้องรีเฟรชชุดข้อมูลเพื่อรับการอัปเดตล่าสุด</span><span class="sxs-lookup"><span data-stu-id="fb060-131">You may need to refresh the dataset to get the latest updates.</span></span> 

    <span data-ttu-id="fb060-132">หลังจากที่ Power BI นำเข้าข้อมูลแล้ว คุณจะเห็นรายงานที่มี 13 หน้า และชุดข้อมูลในบานหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="fb060-132">After Power BI imports the data you will see the report with 13 pages and dataset in the nav pane.</span></span> 

10. <span data-ttu-id="fb060-133">หลังจากรายงานของคุณพร้อม ดำเนินการต่อและเริ่มการสำรวจข้อมูล Project Web App!</span><span class="sxs-lookup"><span data-stu-id="fb060-133">Once your reports are ready, go ahead and start exploring your Project Web App data!</span></span> <span data-ttu-id="fb060-134">Template App มาพร้อมกับรายงาน 13 หน้าที่เป็นภาพรวมการจัดการพอร์ตโครงการ (6 หน้ารายงาน), ภาพรวมทรัพยากร (5 หน้ารายงาน) และ สถานะของโครงการ (2 หน้ารายงาน)</span><span class="sxs-lookup"><span data-stu-id="fb060-134">The Template App comes with 13 rich and detailed reports for the Portfolio Overview (6 report pages), Resource Overview (5 report pages) and Project Status (2 report pages).</span></span> 

    ![แดชบอร์ดพอร์ตโครงการ](media/service-connect-to-project-online/report1.png)
   
    ![ความพร้อมใช้งาน](media/service-connect-to-project-online/report3.png)
   
    ![สถานะของโครงการ](media/service-connect-to-project-online/report2.png)

<span data-ttu-id="fb060-138">**ฉันต้องทำอะไรตอนนี้**</span><span class="sxs-lookup"><span data-stu-id="fb060-138">**What now?**</span></span>

* <span data-ttu-id="fb060-139">แม้ว่าชุดข้อมูลของคุณจะถูกกำหนดให้รีเฟรชรายวัน แต่คุณสามารถเปลี่ยนกำหนดการรีเฟรช หรือลองรีเฟรชตามความต้องการได้โดยใช้ **รีเฟรชเดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="fb060-139">While your dataset will be scheduled to refresh daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

<span data-ttu-id="fb060-140">**ขยาย Template App**</span><span class="sxs-lookup"><span data-stu-id="fb060-140">**Expand the Template App**</span></span>

<span data-ttu-id="fb060-141">ดาวน์โหลด[GitHub PBIT ไฟล์](https://github.com/OfficeDev/Project-Power-BI-Content-Packs)เมื่อต้องการกำหนดค่า และปรับปรุงชุดเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="fb060-141">Download the [GitHub PBIT file](https://github.com/OfficeDev/Project-Power-BI-Content-Packs) to further customize and update the Content Pack.</span></span>

## <a name="next-steps"></a><span data-ttu-id="fb060-142">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="fb060-142">Next steps</span></span>
[<span data-ttu-id="fb060-143">เริ่มต้นใช้งานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="fb060-143">Get started in Power BI</span></span>](../fundamentals/service-get-started.md)

[<span data-ttu-id="fb060-144">รับข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="fb060-144">Get data in Power BI</span></span>](service-get-data.md)
