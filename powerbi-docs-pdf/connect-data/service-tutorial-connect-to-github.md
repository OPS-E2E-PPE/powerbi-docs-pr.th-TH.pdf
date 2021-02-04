---
title: 'บทช่วยสอน: เชื่อมต่อกับพื้นที่เก็บของ GitHub ด้วย Power BI'
description: ในบทช่วยสอนนี้ คุณจะเชื่อมต่อกับข้อมูลจริงในบริการ GitHub ด้วย Power BI และ Power BI จะสร้างแดชบอร์ดและรายงานโดยอัตโนมัติ
author: paulinbar
ms.author: painbar
ms.reviewer: SarinaJoan
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.custom: connect-to-services
ms.topic: tutorial
ms.date: 10/30/2020
LocalizationGroup: Connect to services
ms.openlocfilehash: d8b6277c64f2f6c55f1ab622d129556fdfc4c600
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96401638"
---
# <a name="tutorial-connect-to-a-github-repo-with-power-bi"></a><span data-ttu-id="c1629-103">บทช่วยสอน: เชื่อมต่อกับพื้นที่เก็บของ GitHub ด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="c1629-103">Tutorial: Connect to a GitHub repo with Power BI</span></span>
<span data-ttu-id="c1629-104">ในบทช่วยสอนนี้ คุณเชื่อมต่อกับข้อมูลจริง: ที่เก็บข้อมูลสาธารณะของเนื้อหา Power BI (หรือที่เรียกว่า *ที่เก็บ*) ในบริการ GitHub</span><span class="sxs-lookup"><span data-stu-id="c1629-104">In this tutorial, you connect to real data: the Power BI content public repository (also known as a *repo*) in the GitHub service.</span></span> <span data-ttu-id="c1629-105">Power BI จะสร้างแดชบอร์ดและรายงานด้วยข้อมูลโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c1629-105">Power BI automatically creates a dashboard and report with the data.</span></span> <span data-ttu-id="c1629-106">คุณจะเห็นคำตอบสำหรับคำถามเช่น: มีบุคคลกี่คนให้การสนับสนุนที่เก็บสาธารณะของ Power BI</span><span class="sxs-lookup"><span data-stu-id="c1629-106">You see answers to questions like: How many people contribute to the Power BI public repo?</span></span> <span data-ttu-id="c1629-107">ใครให้การสนับสนุนมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="c1629-107">Who contributes the most?</span></span> <span data-ttu-id="c1629-108">วันใดในสัปดาห์ที่มีการสนับสนุนมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="c1629-108">Which day of the week has the most contributions?</span></span> <span data-ttu-id="c1629-109">และคำถามอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="c1629-109">And other questions.</span></span> 

<span data-ttu-id="c1629-110">คุณสามารถเชื่อมต่อกับที่เก็บ GitHub แบบส่วนตัวหรือสาธารณะของคุณเองได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="c1629-110">You can connect to your own private or public GitHub repos, too.</span></span> <span data-ttu-id="c1629-111">บทความ [เชื่อมต่อกับ GitHub ด้วย Power BI](service-connect-to-github.md) อธิบายวิธีใช้ *แอปเทมเพลต* Power BI เพื่อเชื่อมต่อกับที่เก็บของคุณ</span><span class="sxs-lookup"><span data-stu-id="c1629-111">The article [Connect to GitHub with Power BI](service-connect-to-github.md) explains how to use a Power BI *template app* to connect to your repos.</span></span>

![รายงาน GitHub ใน Power BI](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-punch-card.png)

<span data-ttu-id="c1629-113">ในบทช่วยสอนนี้ คุณจะทำขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="c1629-113">In this tutorial, you complete the following steps:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="c1629-114">ลงทะเบียนบัญชี GitHub ถ้าคุณยังไม่มีบัญชี</span><span class="sxs-lookup"><span data-stu-id="c1629-114">Sign up for a GitHub account, if you don't have one yet</span></span> 
> * <span data-ttu-id="c1629-115">ลงชื่อเข้าใช้บัญชี Power BI ของคุณ หรือลงทะเบียน ถ้าคุณยังไม่มีบัญชี</span><span class="sxs-lookup"><span data-stu-id="c1629-115">Sign in to your Power BI account, or sign up, if you don't have one yet</span></span>
> * <span data-ttu-id="c1629-116">เปิดบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="c1629-116">Open the Power BI service</span></span>
> * <span data-ttu-id="c1629-117">ค้นหาแอป GitHub</span><span class="sxs-lookup"><span data-stu-id="c1629-117">Find the GitHub app</span></span>
> * <span data-ttu-id="c1629-118">ใส่ข้อมูลสำหรับ Repo GitHub สาธารณะของ Power BI</span><span class="sxs-lookup"><span data-stu-id="c1629-118">Enter the information for the Power BI public GitHub repo</span></span>
> * <span data-ttu-id="c1629-119">ดูแดชบอร์ดและรายงานด้วยข้อมูล GitHub</span><span class="sxs-lookup"><span data-stu-id="c1629-119">View the dashboard and report with GitHub data</span></span>
> * <span data-ttu-id="c1629-120">เพิ่มพื้นที่ทรัพยากรโดยการลบแอป</span><span class="sxs-lookup"><span data-stu-id="c1629-120">Clean up resources by deleting the app</span></span>

<span data-ttu-id="c1629-121">ถ้าคุณไม่ได้ลงทะเบียน Power BI ให้[ลงทะเบียนรุ่นทดลองใช้ฟรี](https://app.powerbi.com/signupredirect?pbi_source=web)ก่อนที่คุณจะเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c1629-121">If you're not signed up for Power BI, [sign up for a free trial](https://app.powerbi.com/signupredirect?pbi_source=web) before you begin.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c1629-122">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="c1629-122">Prerequisites</span></span>

<span data-ttu-id="c1629-123">เมื่อต้องการเรียนรู้บทช่วยสอนนี้ให้เสร็จสมบูรณ์ คุณต้องมีบัญชี GitHub ถ้าคุณยังไม่มีบัญชี</span><span class="sxs-lookup"><span data-stu-id="c1629-123">To complete this tutorial, you need a GitHub account, if you don't already have one.</span></span> 

- <span data-ttu-id="c1629-124">ลงทะเบียน [บัญชี GitHub](/contribute/get-started-setup-github)</span><span class="sxs-lookup"><span data-stu-id="c1629-124">Sign up for a [GitHub account](/contribute/get-started-setup-github).</span></span>


## <a name="how-to-connect"></a><span data-ttu-id="c1629-125">วิธีการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="c1629-125">How to connect</span></span>
1. <span data-ttu-id="c1629-126">ลงชื่อเข้าใช้บริการ Power BI (`https://app.powerbi.com`)</span><span class="sxs-lookup"><span data-stu-id="c1629-126">Sign in to the Power BI service (`https://app.powerbi.com`).</span></span> 
2. <span data-ttu-id="c1629-127">ในบานหน้าต่างนำทาง > เลือก **แอป** จากนั้นเลือก **รับแอป**</span><span class="sxs-lookup"><span data-stu-id="c1629-127">In the nav pane, select **Apps**, then **Get apps**.</span></span>
   
   ![รับแอปใน Power BI](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial.png) 

3. <span data-ttu-id="c1629-129">เลือก **แอป** พิมพ์ **GitHub** ในกล่องค้นหา > **รับทันที**</span><span class="sxs-lookup"><span data-stu-id="c1629-129">Select **Apps**, type **GitHub** in the search box > **Get it now**.</span></span>
   
   ![รับ GitHub ใน Power BI](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-app-source.png) 

4. <span data-ttu-id="c1629-131">ใน **ติดตั้งแอป Power BI นี้หรือไม่** เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="c1629-131">In **Install this Power BI App?** select **Install**.</span></span>
5. <span data-ttu-id="c1629-132">ในส่วน **แอปใหม่ของคุณพร้อมแล้ว** เลือก **ไปที่แอป**</span><span class="sxs-lookup"><span data-stu-id="c1629-132">In **Your new app is ready**, select **Go to app**.</span></span>
6. <span data-ttu-id="c1629-133">ในส่วน **เริ่มต้นใช้งานแอปใหม่ของคุณ** ให้เลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="c1629-133">In **Get started with your new app**, select **Connect**.</span></span>

    ![เริ่มต้นใช้งานแอปใหม่ของคุณ](media/service-tutorial-connect-to-github/power-bi-new-app-connect-get-started.png)

7. <span data-ttu-id="c1629-135">ป้อนชื่อที่เก็บและเจ้าของที่เก็บ Repo</span><span class="sxs-lookup"><span data-stu-id="c1629-135">Enter the repository name and repository owner of the repo.</span></span> <span data-ttu-id="c1629-136">URL สำหรับ Repo นี้คือ https://github.com/MicrosoftDocs/powerbi-docs ดังนั้น **เจ้าของที่เก็บ** จะเป็น **MicrosoftDocs** และ **ที่เก็บ** จะเป็น **powerbi-docs**</span><span class="sxs-lookup"><span data-stu-id="c1629-136">The URL for this repo is https://github.com/MicrosoftDocs/powerbi-docs, so **Repository Owner** is **MicrosoftDocs**, and **Repository** is **powerbi-docs**.</span></span> 
   
    ![ชื่อ Repo GitHub ใน Power BI](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-connect.png)

5. <span data-ttu-id="c1629-138">ป้อนข้อมูลประจำตัว GitHub ที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="c1629-138">Enter the GitHub credentials you created.</span></span> <span data-ttu-id="c1629-139">Power BI อาจข้ามขั้นตอนนี้ ถ้าคุรลงชื่อเข้าใช้ GitHub ในเบราว์เซอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c1629-139">Power BI might skip this step if you're already signed in to GitHub in your browser.</span></span> 

6. <span data-ttu-id="c1629-140">สำหรับ **วิธีการรับรองความถูกต้อง** ให้เลือก **oAuth2**\> **ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="c1629-140">For **Authentication Method**, keep **oAuth2** selected \> **Sign In**.</span></span>

7. <span data-ttu-id="c1629-141">ทำตามหน้าจอการรับรองความถูกต้องของ GitHub</span><span class="sxs-lookup"><span data-stu-id="c1629-141">Follow the GitHub authentication screens.</span></span> <span data-ttu-id="c1629-142">มอบสิทธิ์ Power BI ให้กับข้อมูล GitHub</span><span class="sxs-lookup"><span data-stu-id="c1629-142">Grant Power BI permission to the GitHub data.</span></span>
   
   <span data-ttu-id="c1629-143">ในตอนนี้ Power BI สามารถเชื่อมต่อกับ GitHub และเชื่อมต่อกับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c1629-143">Now Power BI can connect with GitHub and connect to the data.</span></span>  <span data-ttu-id="c1629-144">ข้อมูลจะถูกรีเฟรชวันละหนึ่งครั้ง</span><span class="sxs-lookup"><span data-stu-id="c1629-144">The data is refreshed once a day.</span></span>

8. <span data-ttu-id="c1629-145">หลังจากที่ Power BI นำเข้าข้อมูลแล้ว คุณจะเห็นเนื้อหาของพื้นที่ทำงาน GitHub ใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c1629-145">After Power BI imports the data, you see the contents of your new GitHub workspace.</span></span> 
9. <span data-ttu-id="c1629-146">เลือกลูกศรที่อยู่ถัดจากชื่อพื้นที่ทำงานในหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="c1629-146">Select the arrow next to the workspace name in the nav pane.</span></span> <span data-ttu-id="c1629-147">คุณเห็นพื้นที่ทำงานประกอบด้วยแดชบอร์ดและรายงาน</span><span class="sxs-lookup"><span data-stu-id="c1629-147">You see the workspace contains a dashboard and a report.</span></span> 

    ![แอปในบานหน้าต่างนำทาง](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-left-nav-expanded.png)

10. <span data-ttu-id="c1629-149">เลือก **ตัวเลือกเพิ่มเติม** (...) ที่อยู่ถัดจากชื่อแดชบอร์ด > **เปลี่ยนชื่อ** > พิมพ์ **แดชบอร์ด GitHub**</span><span class="sxs-lookup"><span data-stu-id="c1629-149">Select **More options** (...) next to the dashboard name > **Rename** > type **GitHub dashboard**.</span></span>
 
    ![ไทล์ GitHub ใน Power BI](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-left-nav.png) 

8. <span data-ttu-id="c1629-151">เลือกไอคอนนำทางส่วนกลางเพื่อลดหน้าต่างนำทาง เพื่อให้มีพื้นที่ว่างเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c1629-151">Select the global navigation icon to minimize the nav pane, so you have more room.</span></span>

    ![ไอคอนการนำทางส่วนกลาง](media/service-tutorial-connect-to-github/power-bi-global-navigation-icon.png)

10. <span data-ttu-id="c1629-153">เลือกแดชบอร์ด GitHub</span><span class="sxs-lookup"><span data-stu-id="c1629-153">Select your GitHub dashboard.</span></span>
    
    <span data-ttu-id="c1629-154">แดชบอร์ด GitHub ประกอบด้วยข้อมูลสด ดังนั้นค่าที่คุณเห็นอาจแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="c1629-154">The GitHub dashboard contains live data, so the values you see may be different.</span></span>

    ![แดชบอร์ด GitHub ใน Power BI](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-new-dashboard.png)

    

## <a name="ask-a-question"></a><span data-ttu-id="c1629-156">ถามคำถาม</span><span class="sxs-lookup"><span data-stu-id="c1629-156">Ask a question</span></span>

1. <span data-ttu-id="c1629-157">วางเคอร์เซอร์ของคุณใน **ถามคำถามเกี่ยวกับข้อมูลของคุณ**</span><span class="sxs-lookup"><span data-stu-id="c1629-157">Put your cursor in **Ask a question about your data**.</span></span> <span data-ttu-id="c1629-158">Power BI มี **คำถามเพื่อให้คุณเริ่มต้นใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="c1629-158">Power BI offers **Questions to get your started**.</span></span> 

1. <span data-ttu-id="c1629-159">เลือก **จำนวนผู้ใช้ที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="c1629-159">Select **how many users are there**.</span></span>
 
    ![จำนวนผู้ใช้ที่มีอยู่](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-qna-how-many-users.png)

13. <span data-ttu-id="c1629-161">ในระหว่าง **จำนวน** และ **ผู้ใช้ที่มีอยู่** ให้พิมพ์ **คำขอดึงข้อมูลต่อ**</span><span class="sxs-lookup"><span data-stu-id="c1629-161">In between **how many** and **users are there**, type **pull requests per**.</span></span> 

     <span data-ttu-id="c1629-162">Power BI จะสร้างแผนภูมิแท่งที่แสดงจำนวนคำขอดึงข้อมูลต่อบุคคล</span><span class="sxs-lookup"><span data-stu-id="c1629-162">Power BI creates a bar chart showing the number of pull requests per person.</span></span>

    ![จำนวนคำขอดึงข้อมูลต่อผู้ใช้ที่มีอยู่](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-qna-how-many-prs.png)


13. <span data-ttu-id="c1629-164">เลือกปักหมุดเพื่อปักหมุดไปยังแดชบอร์ดของคุณจากนั้น **ออกจาก Q&A**</span><span class="sxs-lookup"><span data-stu-id="c1629-164">Select the pin to pin it to your dashboard, then **Exit Q&A**.</span></span>

## <a name="view-the-github-report"></a><span data-ttu-id="c1629-165">ดูรายงาน GitHub</span><span class="sxs-lookup"><span data-stu-id="c1629-165">View the GitHub report</span></span> 

1. <span data-ttu-id="c1629-166">ในแดชบอร์ด GitHub ให้เลือกแผนภูมิคอลัมน์ **ดึงข้อมูลคำขอตามเดือน** เพื่อเปิดรายงานที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c1629-166">In the GitHub dashboard, select the column chart **Pull Requests by Month** to open the related report.</span></span>

    ![แผนภูมิคอลัมน์คำขอดึงข้อมูลตามเดือน](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-column-chart.png)

2. <span data-ttu-id="c1629-168">เลือกชื่อผู้ใช้ในแผนภูมิ **คำขอดึงข้อมูลทั้งหมดตามผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="c1629-168">Select a user name in the **Total pull requests by user** chart.</span></span> <span data-ttu-id="c1629-169">ในตัวอย่างนี้ เราเห็นว่าเวลาส่วนใหญ่ของพวกเขาอยู่ในเดือนกุมภาพันธ์</span><span class="sxs-lookup"><span data-stu-id="c1629-169">In this example, we see most of their hours were in February.</span></span>

    ![การเน้นรายงาน GitHub ใน Power BI](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-cross-filter-total-prs.png)

3. <span data-ttu-id="c1629-171">เลือกแท็บ **บัตรเจาะรู** เพื่อดูหน้าถัดไปในรายงาน</span><span class="sxs-lookup"><span data-stu-id="c1629-171">Select the **Punch Card** tab to view the next page in the report.</span></span> 
 
    ![บัตรเจาะรูของรายงาน GitHub ใน Power BI](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-tues-3pm.png)

    <span data-ttu-id="c1629-173">คุณจะเห็นว่าวันอังคารเวลาบ่าย 3 คือเวลาและวันในสัปดาห์ที่มีการ *ยอมรับ* มากที่สุด เมื่อผู้ใช้เช็คอินงานของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="c1629-173">Apparently Tuesday at 3 pm is the most common time and day of the week for *commits*, when people check in their work.</span></span>

## <a name="clean-up-resources"></a><span data-ttu-id="c1629-174">เพิ่มพื้นที่ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="c1629-174">Clean up resources</span></span>

<span data-ttu-id="c1629-175">ในตอนนี้ คุณสำเร็จบทช่วยสอนแล้ว คุณสามารถลบแอป GitHub ได้</span><span class="sxs-lookup"><span data-stu-id="c1629-175">Now that you've finished the tutorial, you can delete the GitHub app.</span></span> 

1. <span data-ttu-id="c1629-176">ในบานหน้าต่างนำทาง ให้เลือก **Apps**</span><span class="sxs-lookup"><span data-stu-id="c1629-176">In the nav pane, select **Apps**.</span></span>
2. <span data-ttu-id="c1629-177">วางเมาส์เหนือไทล์ GitHub และเลือกถังขยะ **ลบ**</span><span class="sxs-lookup"><span data-stu-id="c1629-177">Hover over the GitHub tile and select the **Delete** garbage can.</span></span>

    ![ลบแอป GitHub](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-delete.png)

## <a name="next-steps"></a><span data-ttu-id="c1629-179">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c1629-179">Next steps</span></span>

<span data-ttu-id="c1629-180">ในบทช่วยสอนนี้ คุณได้เชื่อมต่อกับ Repo สาธารณะของ GitHub และข้อมูลที่ได้รับ ซึ่ง Power BI ได้จัดรูปแบบในแดชบอร์ดและรายงาน</span><span class="sxs-lookup"><span data-stu-id="c1629-180">In this tutorial, you've connected to a GitHub public repo and gotten data, which Power BI has formatted in a dashboard and report.</span></span> <span data-ttu-id="c1629-181">คุณได้ตอบคำถามบางอย่างเกี่ยวกับข้อมูลโดยการสำรวจแดชบอร์ดและรายงาน</span><span class="sxs-lookup"><span data-stu-id="c1629-181">You've answered some questions about the data by exploring the dashboard and report.</span></span> <span data-ttu-id="c1629-182">ในตอนนี้ คุณสามารถเรียนรู้เพิ่มเติมเกี่ยวกับการเชื่อมต่อกับบริการอื่นๆ เช่น Salesforce, Microsoft Dynamics และ Google Analytics</span><span class="sxs-lookup"><span data-stu-id="c1629-182">Now you can learn more about connecting to other services, such as Salesforce, Microsoft Dynamics, and Google Analytics.</span></span> 
 
> [!div class="nextstepaction"]
> [<span data-ttu-id="c1629-183">เชื่อมต่อกับ GitHub ด้วยแอปเทมเพลต Power BI</span><span class="sxs-lookup"><span data-stu-id="c1629-183">Connect to GitHub with a Power BI template app</span></span>](service-connect-to-github.md)
