---
title: ทัวร์ Power BI service
description: ภาพรวมของประสบการณ์การนำทาง Power BI
author: mihart
ms.reviewer: mihart
featuredvideoid: G26dr2PsEpk
ms.custom: seodec18
ms.service: powerbi
ms.subservice: powerbi-consumer
ms.topic: quickstart
ms.date: 10/12/2020
ms.author: mihart
LocalizationGroup: Get started
ms.openlocfilehash: 1c67ce91ce625bec3bb3be978bc553f2ff5a3eef
ms.sourcegitcommit: 02484b2d7a352e96213353702d60c21e8c07c6c0
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "91982521"
---
# <a name="quickstart---getting-around-in-power-bi-service"></a><span data-ttu-id="bdb5e-103">เริ่มต้นใช้งานด่วน - ทำความรู้จักบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="bdb5e-103">Quickstart - Getting around in Power BI service</span></span>

[!INCLUDE [power-bi-service-new-look-include](../includes/power-bi-service-new-look-include.md)]

<span data-ttu-id="bdb5e-104">ขณะนี้คุณทราบถึง [พื้นฐานของ Power BI](end-user-basic-concepts.md) แล้ว เรามาดู **บริการของ Power BI** กันบ้าง</span><span class="sxs-lookup"><span data-stu-id="bdb5e-104">Now that you know the [basics of Power BI](end-user-basic-concepts.md), let's take a look around the **Power BI service** .</span></span> <span data-ttu-id="bdb5e-105">ตามที่กล่าวไว้ในบทความก่อนหน้านี้ เพื่อนร่วมงานในทีมของคุณอาจใช้เวลาทั้งหมดใน **Power BI Desktop** เพื่อรวมข้อมูลและสร้างรายงาน แดชบอร์ด และแอปสำหรับบุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="bdb5e-105">As mentioned in the previous article, colleagues on your team might spend all of their time in **Power BI Desktop** , combining data and creating reports, dashboards, and apps for others.</span></span> <span data-ttu-id="bdb5e-106">พวกเขาคือ *นักออกแบบ*</span><span class="sxs-lookup"><span data-stu-id="bdb5e-106">They're *designers* .</span></span> <span data-ttu-id="bdb5e-107">ในทางกลับกัน คุณอาจใช้เวลาทั้งหมดของคุณในบริการของ Power BI เพื่อดูและโต้ตอบกับเนื้อหาที่สร้างโดยบุคคลอื่น (ประสบการณ์ **การใช้งาน** )</span><span class="sxs-lookup"><span data-stu-id="bdb5e-107">You, on the other hand, might spend all of your time in the Power BI service, viewing and interacting with content created by others ( **consuming** experience).</span></span> <span data-ttu-id="bdb5e-108">คุณคือ *ผู้ใช้ทางธุรกิจ*</span><span class="sxs-lookup"><span data-stu-id="bdb5e-108">You're a *business user* .</span></span> <span data-ttu-id="bdb5e-109">การเริ่มต้นใช้งานด่วนสำหรับ *ผู้ใช้ทางธุรกิจ*</span><span class="sxs-lookup"><span data-stu-id="bdb5e-109">This quickstart is for *business users* .</span></span> 


   
 
## <a name="prerequisites"></a><span data-ttu-id="bdb5e-110">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="bdb5e-110">Prerequisites</span></span>

- <span data-ttu-id="bdb5e-111">ถ้าคุณไม่ได้ลงทะเบียน Power BI ให้[ลงทะเบียนรุ่นทดลองใช้ฟรี](https://app.powerbi.com/signupredirect?pbi_source=web)ก่อนที่คุณจะเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bdb5e-111">If you're not signed up for Power BI, [sign up for a free trial](https://app.powerbi.com/signupredirect?pbi_source=web) before you begin.</span></span>

- <span data-ttu-id="bdb5e-112">อ่าน [แนวคิดพื้นฐานเกี่ยวกับบริการของ Power BI](end-user-basic-concepts.md)</span><span class="sxs-lookup"><span data-stu-id="bdb5e-112">Read [Power BI service basic concepts](end-user-basic-concepts.md)</span></span>

- <span data-ttu-id="bdb5e-113">การดูเนื้อหา Power BI (รายงาน แดชบอร์ด แอป) ที่สร้างขึ้นโดย *นักออกแบบ* ต้องการเป็นไปตามหนึ่งในเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bdb5e-113">Viewing Power BI content (reports, dashboards, apps) created by *designers* requires one of two conditions:</span></span>
    - <span data-ttu-id="bdb5e-114">สิทธิการใช้งาน Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="bdb5e-114">a Power BI Pro license</span></span>
    - <span data-ttu-id="bdb5e-115">เพื่อให้องค์กรของคุณมีการสมัครใช้งานสำหรับ Power BI Premium และเนื้อหาที่จะใช้ร่วมกันกับคุณจากความจุ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="bdb5e-115">Your organization to have a Power BI Premium subscription, and the content to be shared with you from Premium capacity.</span></span>    
    <span data-ttu-id="bdb5e-116">[เรียนรู้เกี่ยวกับสิทธิ์การใช้งานและการสมัครใช้งาน](end-user-license.md)</span><span class="sxs-lookup"><span data-stu-id="bdb5e-116">[Learn about licenses and subscriptions](end-user-license.md).</span></span>     

    <span data-ttu-id="bdb5e-117">สำหรับวัตถุประสงค์ของการเริ่มต้นใช้งานด่วนนี้ ไม่จำเป็นต้องมีเงื่อนไขใดๆ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-117">For the purposes of this quickstart, we aren't requiring either of these conditions to be met.</span></span> <span data-ttu-id="bdb5e-118">Microsoft ได้สร้างเนื้อหาตัวอย่างให้คุณโดยตรงจากอินเทอร์เฟซบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="bdb5e-118">Microsoft has made sample content available to you directly from the Power BI service interface.</span></span> <span data-ttu-id="bdb5e-119">เราจะใช้เนื้อหาตัวอย่างนี้เพื่อเรียนรู้วิธีการของเราในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="bdb5e-119">We'll use this sample content to learn our way around the Power BI service.</span></span> 

## <a name="open-the-power-bi-service"></a><span data-ttu-id="bdb5e-120">เปิดบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="bdb5e-120">Open the Power BI service</span></span>


<span data-ttu-id="bdb5e-121">หากต้องการเริ่มต้น ให้เปิดบริการของ Power BI (app.powerbi.com)</span><span class="sxs-lookup"><span data-stu-id="bdb5e-121">To begin, open the Power BI service (app.powerbi.com).</span></span> 
1. <span data-ttu-id="bdb5e-122">ถ้าบานหน้าต่างการนำทางด้านซ้ายถูกยุบ ให้เลือกไอคอนบานหน้าต่างการนำทาง</span><span class="sxs-lookup"><span data-stu-id="bdb5e-122">If the left navigation pane is collapsed, select the nav pane icon</span></span> ![ไอคอนที่มีเส้นแนวนอน 3 เส้น](./media/end-user-experience/power-bi-burger.png) <span data-ttu-id="bdb5e-124">เพื่อขยายบานหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="bdb5e-124">to expand it.</span></span> 


1. <span data-ttu-id="bdb5e-125">จากมุมล่างซ้าย เลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="bdb5e-125">From the lower left corner, select **Get data** .</span></span> <span data-ttu-id="bdb5e-126">เราจะนำข้อมูลตัวอย่างบางส่วนไปใช้สำหรับการนำเสนอบริการของ Power BI ของเรา</span><span class="sxs-lookup"><span data-stu-id="bdb5e-126">We'll grab some sample data to use for our tour of the Power BI service.</span></span> <span data-ttu-id="bdb5e-127">มีข้อมูลตัวอย่างทุกชนิดให้คุณได้ค้นหา และในครั้งนี้ เราจะใช้ข้อมูลเกี่ยวกับการตลาดและการขาย</span><span class="sxs-lookup"><span data-stu-id="bdb5e-127">There are all types of sample data provided for you to explore, and this time we'll use the data about marketing and sales.</span></span> 

   ![สกรีนช็อตแสดงปุ่มสำหรับรับข้อมูล](./media/end-user-experience/power-bi-get-data.png)

1. <span data-ttu-id="bdb5e-129">หลังจากหน้าจอ **รับข้อมูล** เปิดขึ้น เลือก **ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="bdb5e-129">After the **Get data** screen opens, select **Samples** .</span></span>

   ![สกรีนช็อตแสดงหน้าจอรับข้อมูลที่มีกล่องสีแดงรอบๆ ตัวอย่าง](./media/end-user-experience/power-bi-sample.png)

1. <span data-ttu-id="bdb5e-131">เลือก **การขายและการตลาด** > **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="bdb5e-131">Select **Sales and Marketing** > **Connect** .</span></span> 

   ![สกรีนช็อตแสดงตัวอย่างการขายและการตลาดที่เลือก](./media/end-user-experience/power-bi-sales.png)


5. <span data-ttu-id="bdb5e-133">บริการของ Power BI จะติดตั้งตัวอย่างใน **พื้นที่ทำงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="bdb5e-133">The Power BI service installs the sample in your **My workspace** .</span></span>  <span data-ttu-id="bdb5e-134">**พื้นที่ทำงานของฉัน** คือ sandbox ส่วนตัวของคุณสำหรับการเรียนรู้และการทดลองใช้</span><span class="sxs-lookup"><span data-stu-id="bdb5e-134">**My workspace** is your private sandbox for learning and experimenting.</span></span>  <span data-ttu-id="bdb5e-135">เฉพาะคุณเท่านั้นที่สามารถดูเนื้อหาใน **พื้นที่ทำงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="bdb5e-135">Only you can see the content in **My workspace** .</span></span> <span data-ttu-id="bdb5e-136">ตัวอย่างประกอบด้วยหนึ่งแดชบอร์ด หนึ่งรายงาน และหนึ่งชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bdb5e-136">The sample includes one dashboard, one report, and one dataset.</span></span> <span data-ttu-id="bdb5e-137">โดยทั่วไปแล้ว *ผู้ใช้ทางธุรกิจ* จะไม่ได้รับชุดข้อมูล แต่ตัวอย่างนี้ถูกออกแบบมาสำหรับผู้ใช้ทั้งหมด จึงมีชุดข้อมูลรวมอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="bdb5e-137">Typically, *business users* won't receive datasets, but this sample is designed for all users and it does include one.</span></span>

    ![สกรีนช็อตแสดงหน้าจอแอป Power B I พร้อมแอปที่เรียกว่าตัวอย่างการขายและการตลาด](./media/end-user-experience/power-bi-new-sample.png)




    <span data-ttu-id="bdb5e-139">ในฐานะที่เป็น *ผู้ใช้ทางธุรกิจ* เนื้อหาส่วนใหญ่ที่ใช้ร่วมกันกับคุณจะไม่รวมการเข้าถึงโดยตรงไปยังชุดข้อมูลเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="bdb5e-139">As a *business user* , most content that is shared with you won't include direct access to the underlying datasets.</span></span> <span data-ttu-id="bdb5e-140">เนื่องจากตัวอย่าง Power BI ถูกสร้างขึ้นสำหรับลูกค้า Power BI ทั้งหมด จึงมีการรวมชุดข้อมูลไว้</span><span class="sxs-lookup"><span data-stu-id="bdb5e-140">Because the Power BI samples are created for all Power BI customers, datasets are included.</span></span>   

    <span data-ttu-id="bdb5e-141">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับตัวอย่าง โปรดดู [รับตัวอย่างสำหรับ Power BI](../create-reports/sample-datasets.md)</span><span class="sxs-lookup"><span data-stu-id="bdb5e-141">To learn more about samples, see [Get samples for Power BI](../create-reports/sample-datasets.md).</span></span>

## <a name="view-content-dashboards-and-reports"></a><span data-ttu-id="bdb5e-142">ดูเนื้อหา (แดชบอร์ดและรายงาน)</span><span class="sxs-lookup"><span data-stu-id="bdb5e-142">View content (dashboards and reports)</span></span>
<span data-ttu-id="bdb5e-143">เนื้อหาได้รับการจัดระเบียบภายในบริบทของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="bdb5e-143">Content is organized within the context of a workspace.</span></span> <span data-ttu-id="bdb5e-144">ผู้ใช้ทางธุรกิจทุกคนมีพื้นที่ทำงานอย่างน้อยหนึ่งแห่ง และเรียกว่า **พื้นที่ทำงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="bdb5e-144">Every business user has at least one workspace, and it's called **My workspace** .</span></span> <span data-ttu-id="bdb5e-145">เมื่อเพื่อนร่วมงาน *นักออกแบบ* แชร์เนื้อหากับคุณ คุณมีอาจพื้นที่ทำงานอื่นๆ เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="bdb5e-145">When *designer* colleagues share content with you, you may end up with additional workspaces.</span></span>  <span data-ttu-id="bdb5e-146">ตัวอย่างเช่น ถ้า *นักออกแบบ* กำหนดสิทธิ์ในการเข้าถึงให้กับคุณไปยังพื้นที่ทำงานของพวกเขา พื้นที่ทำงานนั้นจะแสดงในไซต์ Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-146">For example, if a *designer* assigns you access permissions to one of their workspaces, that workspace will show up in your Power BI site.</span></span>  

<span data-ttu-id="bdb5e-147">**พื้นที่ทำงานของฉัน** จัดเก็บเนื้อหาทั้งหมดที่คุณเป็นเจ้าของและสร้าง</span><span class="sxs-lookup"><span data-stu-id="bdb5e-147">**My Workspace** stores all the content that you own and create.</span></span> <span data-ttu-id="bdb5e-148">ให้คิดว่าเป็น sandbox ส่วนบุคคลของคุณหรือพื้นที่ทำงานสำหรับเนื้อหาของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="bdb5e-148">Think of it as your personal sandbox or work area for your own content.</span></span> <span data-ttu-id="bdb5e-149">สำหรับ *ผู้ใช้ทางธุรกิจ* Power BI หลายคน **พื้นที่ทำงานของฉัน** ยังว่างเปล่าเพราะงานของคุณไม่เกี่ยวข้องกับการสร้างเนื้อหาใหม่</span><span class="sxs-lookup"><span data-stu-id="bdb5e-149">For many Power BI *business user* , **My workspace** remains empty because your job doesn't involve creating new content.</span></span>  <span data-ttu-id="bdb5e-150">*ผู้ใช้ทางธุรกิจ* โดยความหมายนั้น ใช้ข้อมูลที่สร้างขึ้นโดยผู้อื่นและใช้ข้อมูลนั้นเพื่อตัดสินใจทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-150">*Business users* , by definition, consume data created by others and use that data to make business decisions.</span></span> <span data-ttu-id="bdb5e-151">หากคุณกำลังสร้างเนื้อหา ลองอ่าน [บทความ Power BI สำหรับ *ผู้ออกแบบ*](../index.yml) แทน</span><span class="sxs-lookup"><span data-stu-id="bdb5e-151">If you find that you are creating content, consider reading the [Power BI articles for *report creators*](../index.yml) instead.</span></span>

<span data-ttu-id="bdb5e-152">พื้นที่ทำงานมีจำนวนมากกว่ารายการของเนื้อหาแบบง่ายอย่างมาก</span><span class="sxs-lookup"><span data-stu-id="bdb5e-152">A workspace is much more than a simple listing of content.</span></span> <span data-ttu-id="bdb5e-153">ในหน้านี้ คุณสามารถเรียนรู้มากมายเกี่ยวกับแดชบอร์ดและรายงานของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="bdb5e-153">On this page, you can learn a lot about the workspace's dashboards and reports.</span></span> <span data-ttu-id="bdb5e-154">ใช้เวลาสักครู่เพื่อระบุเจ้าของเนื้อหา วันที่รีเฟรชครั้งล่าสุด ความอ่อนไหวของข้อมูล และการประทับรับรอง ถ้ามี</span><span class="sxs-lookup"><span data-stu-id="bdb5e-154">Take a few minutes to identify the content owner, last refreshed date, data sensitivity, and endorsements, if any.</span></span> <span data-ttu-id="bdb5e-155">เลือก **การดำเนินการเพิ่มเติม (...)** เพื่อแสดงรายการของการดำเนินการสำหรับแดชบอร์ดและรายงาน</span><span class="sxs-lookup"><span data-stu-id="bdb5e-155">Select **More actions (...)** to display a list of actions for the dashboard and report.</span></span>   

<span data-ttu-id="bdb5e-156">หากต้องการเรียนรู้เพิ่มเติม โปรดดู [พื้นที่ทำงาน](end-user-workspaces.md)</span><span class="sxs-lookup"><span data-stu-id="bdb5e-156">To learn more, see [Workspaces](end-user-workspaces.md).</span></span>

![หน้าจอพื้นที่ทำงานของแอปที่มีเมนูการดำเนินการเพิ่มเติมปรากฏขึ้นสำหรับรายงาน](./media/end-user-experience/power-bi-more-actions.png)

<span data-ttu-id="bdb5e-158">พื้นที่ทำงานเป็นหนึ่งในเส้นทางของข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-158">A workspace is also one of the paths into your data.</span></span> <span data-ttu-id="bdb5e-159">จากพื้นที่ทำงาน คุณสามารถเปิดแดชบอร์ดหรือรายงานโดยการเลือกจากรายการ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-159">From a workspace you can open a dashboard or report by selecting it from the list.</span></span>  <span data-ttu-id="bdb5e-160">คุณสามารถสร้างรายการโปรดของแดชบอร์ดหรือรายงานได้โดยการวางเมาส์เหนือและเลือกไอคอนรูปดาว</span><span class="sxs-lookup"><span data-stu-id="bdb5e-160">You can favorite a dashboard or report by hovering and selecting the star icon.</span></span> <span data-ttu-id="bdb5e-161">ถ้า *นักออกแบบ* ให้ [สิทธิ์การแชร์](end-user-shared-with-me.md) แก่คุณ คุณสามารถแบ่งปันจากที่นี่ได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="bdb5e-161">If the *designer* gave you [sharing permissions](end-user-shared-with-me.md), you can share from here as well.</span></span> 

![เมนูที่ปรากฏเมื่อวางเมาส์เหนือวัตถุ](./media/end-user-experience/power-bi-dashboard.png)

1. <span data-ttu-id="bdb5e-163">เลือกชื่อแดชบอร์ดเพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="bdb5e-163">Select the name of the dashboard to open it.</span></span> <span data-ttu-id="bdb5e-164">แดชบอร์ดคือสิ่งที่ทำให้บริการของ Power BI แตกต่างจาก Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="bdb5e-164">Dashboards are something that differentiates the Power BI service from Power BI Desktop.</span></span> [<span data-ttu-id="bdb5e-165">เรียนรู้เกี่ยวกับแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="bdb5e-165">Learn about dashboards</span></span>](end-user-dashboards.md)

    ![แดชบอร์ดเปิดขึ้น](./media/end-user-experience/power-bi-dashboard-open.png)

2. <span data-ttu-id="bdb5e-167">การดำเนินการที่คุณสามารถทำได้ในแดชบอร์ดจะแสดงอยู่ในแถบเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="bdb5e-167">The actions you can take on a dashboard are displayed in the top menu bar.</span></span>    

    ![สกรีนช็อตของส่วนบนสุดของบริการของ Power BI](./media/end-user-experience/power-bi-top-menu.png)

3. <span data-ttu-id="bdb5e-169">วางเมาส์เหนือไทล์แดชบอร์ดและเลือก **ตัวเลือกเพิ่มเติม (...)** เพื่อดูตัวเลือกที่คุณมีสำหรับการโต้ตอบกับไทล์นั้น</span><span class="sxs-lookup"><span data-stu-id="bdb5e-169">Hover over a dashboard tile and select **More options (...)** to see the options you have for interacting with that tile.</span></span>

    ![สกรีนช็อตแสดงเมนูดรอปดาวน์สำหรับไทล์แดชบอร์ด](./media/end-user-experience/power-bi-tile-menu.png)

4. <span data-ttu-id="bdb5e-171">เลือกไทล์แดชบอร์ดเพื่อเปิดรายงานที่ถูกใช้เพื่อสร้างไทล์นั้น</span><span class="sxs-lookup"><span data-stu-id="bdb5e-171">Select a dashboard tile to open the report that was used to create that tile.</span></span> <span data-ttu-id="bdb5e-172">รายงานจะเปิดไปยังหน้าที่มีวิชวลที่อยู่บนไทล์นั้น</span><span class="sxs-lookup"><span data-stu-id="bdb5e-172">The report opens to the page that contains the visual that is on the tile.</span></span> <span data-ttu-id="bdb5e-173">นี่ไง ฉันได้เลือกไทล์แดชบอร์ดด้วยแผนที่ต้นไม้</span><span class="sxs-lookup"><span data-stu-id="bdb5e-173">Here, I've selected the dashboard tile with the treemap.</span></span> <span data-ttu-id="bdb5e-174">บริการของ Power BI เปิดหน้ารายงานของ **ประเภท YTD**</span><span class="sxs-lookup"><span data-stu-id="bdb5e-174">The Power BI service opens the **YTD Category** report page.</span></span>

    ![รายงานเปิดขึ้น](./media/end-user-experience/power-bi-report.png)

    <span data-ttu-id="bdb5e-176">รายงานมีหลายส่วน</span><span class="sxs-lookup"><span data-stu-id="bdb5e-176">Reports have several sections.</span></span> <span data-ttu-id="bdb5e-177">ทางด้านซ้ายคือรายการของหน้ารายงานที่คลิกได้</span><span class="sxs-lookup"><span data-stu-id="bdb5e-177">On the left is the clickable list of report pages.</span></span> <span data-ttu-id="bdb5e-178">ด้านบนคือแถบเมนูที่มีการดำเนินการที่คุณสามารถทำได้ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="bdb5e-178">Across the top is the menu bar containing actions you can take with the report.</span></span>  <span data-ttu-id="bdb5e-179">ตัวเลือกที่พร้อมใช้งานจะขึ้นอยู่กับบทบาทและสิทธิ์ของรายงานที่ *นักออกแบบ* มอบหมายให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-179">The options available will depend on the role and permission the report *designer* assigned to you.</span></span> <span data-ttu-id="bdb5e-180">ทางด้านขวาคือบานหน้าต่าง **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="bdb5e-180">On the right side is the **Filters** pane.</span></span> <span data-ttu-id="bdb5e-181">และพื้นที่กึ่งกลางคือส่วนของรายงาน</span><span class="sxs-lookup"><span data-stu-id="bdb5e-181">And the center canvas contains the report itself.</span></span> <span data-ttu-id="bdb5e-182">เช่นเดียวกันกับแดชบอร์ด มีการดำเนินการที่คุณสามารถใช้สำหรับรายงานทั้งหมด สำหรับแต่ละวิชวล และยังสำหรับแต่ละหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="bdb5e-182">Similar to the dashboard, there are actions that you can take for the entire report, for individual visuals, and also for a single report page.</span></span> 

    <span data-ttu-id="bdb5e-183">เรียนรู้เกี่ยวกับรายงาน [รายงาน Power BI](end-user-reports.md)</span><span class="sxs-lookup"><span data-stu-id="bdb5e-183">Learn about reports [Power BI reports](end-user-reports.md).</span></span>

## <a name="using-the-left-navigation-pane"></a><span data-ttu-id="bdb5e-184">การใช้บานหน้าต่างนำทางด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="bdb5e-184">Using the left navigation pane</span></span>
<span data-ttu-id="bdb5e-185">บานหน้าต่างนำทางจะเป็นประโยชน์มากขึ้นเมื่อเพื่อนร่วมงานแชร์เนื้อหากับคุณ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-185">The nav pane will become more useful as colleagues share content with you.</span></span> <span data-ttu-id="bdb5e-186">ในส่วนของการเริ่มต้นใช้งานด่วน เราจะวางตัวอย่าง *การขายและการตลาด* ไว้ก่อนและไปดูที่แดชบอร์ดและรายงานที่เป็นของ *ผู้ใช้ทางธุรกิจ* ของ Power BI ผู้มีเนื้อหาที่ใช้ร่วมกันจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="bdb5e-186">In this section of the Quickstart, we'll put the *Sales and marketing* sample aside, and look at a dashboard and report that belong to a Power BI *business user* who has a lot of shared content.</span></span>

1. <span data-ttu-id="bdb5e-187">**หน้าแรก** คือหน้า landing page เริ่มต้นเมื่อคุณเข้าสู่ระบบบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="bdb5e-187">**Home** is the default landing page when you log in to the Power BI service.</span></span> <span data-ttu-id="bdb5e-188">หน้าแรกเป็นจุดเริ่มต้นที่ยอดเยี่ยมและเป็นอีกวิธีในการนำทางไปยังเนื้อหาของคุณ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-188">Home is a great jumping off point and alternate way to navigate your content.</span></span> <span data-ttu-id="bdb5e-189">เนื้อหาบนหน้าแรกจะถูกจัดเรียงตามรายการโปรด ล่าสุด ที่เปิดบ่อย และความสำคัญ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-189">Content on Home is organized by favorite, recent, frequent, and featured.</span></span> <span data-ttu-id="bdb5e-190">นอกจากนี้หน้าแรกยังแสดงพื้นที่ทำงานและแอปล่าสุดของคุณ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-190">Home also displays your most recent workspaces and apps.</span></span> <span data-ttu-id="bdb5e-191">เพียงแค่เลือกรายการเพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="bdb5e-191">Just select an item to open it.</span></span>

    <span data-ttu-id="bdb5e-192">หน้าแรกรวบรวมเครื่องมือค้นหาและเรียงลำดับ บานหน้าต่างการนำทาง และพื้นที่การทำงานพร้อม *การ์ด* ที่คุณสามารถเลือกเพื่อเปิดแดชบอร์ด รายงาน และแอปของคุณเข้าด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="bdb5e-192">Home brings together the searching and sorting tools, the nav pane, and a canvas with *cards* that you can select to open your dashboards, reports, and apps.</span></span> <span data-ttu-id="bdb5e-193">ในตอนแรก คุณอาจไม่มีการ์ดจำนวนมากบนพื้นที่ทำงานของคุณ แต่จะเปลี่ยนไปเมื่อคุณเริ่มใช้ Power BI กับเพื่อนร่วมงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-193">At first, you might not have many cards on your Home canvas, but that will change as you start to use Power BI with your colleagues.</span></span> <span data-ttu-id="bdb5e-194">พื้นที่ทำงานของหน้าแรกของคุณจะมีการอัปเดตเนื้อหาที่แนะนำและแหล่งข้อมูลการเรียนรู้ให้ด้วย</span><span class="sxs-lookup"><span data-stu-id="bdb5e-194">Your Home canvas also updates with recommended content and learning resources.</span></span>

   ![สกรีนช็อตของหน้าแรกแบบเต็ม](./media/end-user-experience/power-bi-full-home.png)

    <span data-ttu-id="bdb5e-196">เมื่อต้องการเรียนรู้เพิ่มเติม ดู [หน้าแรก Power BI](end-user-home.md)</span><span class="sxs-lookup"><span data-stu-id="bdb5e-196">To learn more, see [Power BI Home](end-user-home.md)</span></span>

2. <span data-ttu-id="bdb5e-197">**รายการโปรด** และ **ล่าสุด** มีลูกศร</span><span class="sxs-lookup"><span data-stu-id="bdb5e-197">**Favorites** and **Recent** both have arrows.</span></span> <span data-ttu-id="bdb5e-198">เลือกลูกศรเพื่อดูรายการโปรดห้ารายการ หรือเนื้อหาที่เยี่ยมชมล่าสุดห้ารายการได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="bdb5e-198">Select an arrow to quickly see the top five favorites or five most recently visited content.</span></span> <span data-ttu-id="bdb5e-199">จากเมนูลอย ให้เลือกเนื้อหาเพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="bdb5e-199">From the flyout, select content to open it.</span></span> 

   ![รายการลอยสำหรับเนื้อหาล่าสุด](./media/end-user-experience/power-bi-recent.png)

    <span data-ttu-id="bdb5e-201">หากต้องการดูรายการโปรดหรือล่าสุดทั้งหมดของคุณ ให้เลือกคำหรือไอคอน</span><span class="sxs-lookup"><span data-stu-id="bdb5e-201">To see your full list of favorites or recents, select the word or icon.</span></span> <span data-ttu-id="bdb5e-202">รายการเนื้อหาเหล่านี้แสดงรายละเอียดเพิ่มเติมเกี่ยวกับรายงาน แอป และแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="bdb5e-202">These content lists provide additional details about the reports, apps, and dashboards.</span></span>

    ![รายการเนื้อหาสำหรับรายการโปรด](./media/end-user-experience/power-bi-favorites.png)


    <span data-ttu-id="bdb5e-204">หากต้องการเรียนรู้เพิ่มเติม ดู [ล่าสุดใน Power BI](end-user-recent.md) และ [รายการโปรดใน Power BI](end-user-recent.md)</span><span class="sxs-lookup"><span data-stu-id="bdb5e-204">To learn more, see [Recents in Power BI](end-user-recent.md) and [Favorites in Power BI](end-user-recent.md).</span></span>

4. <span data-ttu-id="bdb5e-205">เลือก **แอป** เพื่อแสดงแอปทั้งหมดที่แชร์กับคุณ หรือที่คุณได้ติดตั้งแล้ว</span><span class="sxs-lookup"><span data-stu-id="bdb5e-205">Select **Apps** to display all apps that have been shared with you or that you have installed.</span></span> <span data-ttu-id="bdb5e-206">และเลือก **แชร์กับฉัน** เพื่อดูแดชบอร์ดและรายงานที่ได้แชร์กับคุณ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-206">And select **Shared with me** to see dashboards and reports that have been shared with you.</span></span> <span data-ttu-id="bdb5e-207">เนื่องจากคุณเพิ่งเริ่มต้นใช้บริการของ Power BI พื้นที่เนื้อหาเหล่านี้จะว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="bdb5e-207">Since you're just starting out with the Power BI service, these content areas will be empty.</span></span> 

    <span data-ttu-id="bdb5e-208">เรียนรู้เกี่ยวกับ [แอป](end-user-apps.md) และ [แชร์กับฉัน](end-user-shared-with-me.md)</span><span class="sxs-lookup"><span data-stu-id="bdb5e-208">Learn about [Apps](end-user-apps.md) and [Shared with me](end-user-shared-with-me.md).</span></span>

### <a name="search-and-sort-content"></a><span data-ttu-id="bdb5e-209">ค้นหาและเรียงลำดับเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="bdb5e-209">Search and sort content</span></span>
<span data-ttu-id="bdb5e-210">เมื่อคุณเพิ่งเริ่มใช้บริการ Power BI คุณจะมีเนื้อหาเพียงไม่กี่ชิ้น</span><span class="sxs-lookup"><span data-stu-id="bdb5e-210">When you're new to the Power BI service, you'll have only a few pieces of content.</span></span> <span data-ttu-id="bdb5e-211">แต่ในขณะที่เพื่อนร่วมงานเริ่มแบ่งปันเนื้อหากับคุณ และคุณเริ่มดาวน์โหลดแอปคุณอาจจบลงด้วยรายการเนื้อหาที่ยาว</span><span class="sxs-lookup"><span data-stu-id="bdb5e-211">But as colleagues begin sharing content with you and you begin downloading apps, you may end up with long lists of content.</span></span> <span data-ttu-id="bdb5e-212">นั่นคือเวลาที่คุณจะพบการค้นหาและการเรียงลำดับที่เป็นประโยชน์อย่างยิ่ง</span><span class="sxs-lookup"><span data-stu-id="bdb5e-212">That's when you'll find searching and sorting extremely helpful.</span></span>

<span data-ttu-id="bdb5e-213">การค้นหาพร้อมใช้งานจากเกือบทุกส่วนของบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="bdb5e-213">Search is available from almost every part of the Power BI service.</span></span> <span data-ttu-id="bdb5e-214">เพียงแค่มองหากล่องค้นหาหรือเลือกไอคอนแว่นขยายการค้นหา</span><span class="sxs-lookup"><span data-stu-id="bdb5e-214">Just look for the search box or search magnifying glass icon.</span></span>    
![ไอคอนแว่นขยาย](./media/end-user-experience/power-bi-search-icon.png)

<span data-ttu-id="bdb5e-216">ในเขตข้อมูลการค้นหา ให้พิมพ์ชื่อทั้งหมดหรือบางส่วนของแดชบอร์ด รายงาน สมุดงาน แอป หรือเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-216">In the Search field, type all or part of the name of a dashboard, report, workbook, app, or owner.</span></span> <span data-ttu-id="bdb5e-217">Power BI ค้นหาเนื้อหาทั้งหมดของคุณ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-217">Power BI searches all of your content.</span></span>

![การค้นหารายงาน](./media/end-user-experience/power-bi-search-field.png)

<span data-ttu-id="bdb5e-219">นอกจากนี้ยังมีหลายวิธีในการเรียงลำดับเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="bdb5e-219">There are also many ways to sort content.</span></span> <span data-ttu-id="bdb5e-220">วางเมาส์เหนือส่วนหัวของคอลัมน์ และค้นหาลูกศรที่ระบุว่าคอลัมน์สามารถเรียงลำดับได้</span><span class="sxs-lookup"><span data-stu-id="bdb5e-220">Hover over column headers and look for arrows indicating that the column can be sorted.</span></span> <span data-ttu-id="bdb5e-221">ไม่ใช่ทุกคอลัมน์ที่จะสามารถจัดเรียงได้</span><span class="sxs-lookup"><span data-stu-id="bdb5e-221">Not all columns can be sorted.</span></span> 

![ลูกศรถัดจากส่วนหัวคอลัมน์ประเภท](./media/end-user-experience/power-bi-sort-icon.png)

<span data-ttu-id="bdb5e-223">หรือมองหา **ตัวกรอง** การค้นหา ใกล้กับมุมขวาบนของรายการเนื้อหาของคุณ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-223">Or, look for the Search **Filters** near the upper right corner of your content lists.</span></span> <span data-ttu-id="bdb5e-224">ค้นหาเนื้อหาได้อย่างรวดเร็วโดยการเลือกจากชนิดของเนื้อหา เจ้าของ หรือเขตข้อมูลอื่นๆ ที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bdb5e-224">Find content quickly by selecting from the type of content, owner, or any other available field.</span></span>

![เรียงลำดับเนื้อหา](./media/end-user-experience/power-bi-sort-date.png)


<span data-ttu-id="bdb5e-226">เมื่อต้องการเรียนรู้เพิ่มเติม ให้ดู [การนำทางใน Power BI: ค้นหาและจัดเรียง](end-user-search-sort.md)</span><span class="sxs-lookup"><span data-stu-id="bdb5e-226">To learn more, see [Power BI navigation: search and sort](end-user-search-sort.md)</span></span>

## <a name="find-the-owner"></a><span data-ttu-id="bdb5e-227">ค้นหาเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-227">Find the owner</span></span>
<span data-ttu-id="bdb5e-228">และเราจะจบการเริ่มต้นใช้งานด่วนนี้ด้วยคำแนะนำที่เป็นประโยชน์</span><span class="sxs-lookup"><span data-stu-id="bdb5e-228">And we'll end this quickstart with a helpful tip.</span></span> <span data-ttu-id="bdb5e-229">หากคุณมีคำถามเกี่ยวกับแดชบอร์ด รายงาน หรือแอป -- คุณสามารถค้นหาเจ้าของได้</span><span class="sxs-lookup"><span data-stu-id="bdb5e-229">If you have questions about a dashboard, report, or app -- you can look up the owner.</span></span> <span data-ttu-id="bdb5e-230">ด้วยการเปิดเนื้อหา ให้เลือกรายการดรอปดาวน์ของชื่อเรื่องเพื่อแสดงเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-230">With the content open, select the title dropdown to display the owner.</span></span> <span data-ttu-id="bdb5e-231">เจ้าของอาจเป็นบุคคลหรือกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="bdb5e-231">The owner may be a person or a group.</span></span>

![พื้นที่ทำงานของหน้าหลัก](./media/end-user-experience/power-bi-owner.png)


## <a name="clean-up-resources"></a><span data-ttu-id="bdb5e-233">เพิ่มพื้นที่ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="bdb5e-233">Clean up resources</span></span>
<span data-ttu-id="bdb5e-234">หลังจากที่คุณดำเนินการเริ่มต้นด่วนนี้เสร็จสิ้นแล้ว คุณสามารถลบแดชบอร์ดตัวอย่าง รายงาน และชุดข้อมูลได้หากต้องการ</span><span class="sxs-lookup"><span data-stu-id="bdb5e-234">After you finish this quickstart, you can delete the sample dashboard, report, and dataset, if you wish.</span></span>

1. <span data-ttu-id="bdb5e-235">เปิดบริการของ Power BI (app.powerbi.com) และลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="bdb5e-235">Open the Power BI service (app.powerbi.com) and sign in.</span></span>    
2. <span data-ttu-id="bdb5e-236">เปิดหน้าแรก Power BI เลื่อนลงและเลือก **พื้นที่ทำงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="bdb5e-236">Open Power BI Home, scroll down and select **My workspace** .</span></span>      

3. <span data-ttu-id="bdb5e-237">วางเมาส์เหนือแดชบอร์ด รายงาน หรือชุดข้อมูล และเลือก **ตัวเลือกเพิ่มเติม (...)**  > **ลบ**</span><span class="sxs-lookup"><span data-stu-id="bdb5e-237">Hover over the dashboard, report, or dataset and select **More options (...)** > **Delete** .</span></span> <span data-ttu-id="bdb5e-238">ทำซ้ำจนกว่าลบรายการทั้งสามออกหมด</span><span class="sxs-lookup"><span data-stu-id="bdb5e-238">Repeat until all three are removed.</span></span>

    ![ลบแดชบอร์ด](./media/end-user-experience/power-bi-cleanup.png)



## <a name="next-steps"></a><span data-ttu-id="bdb5e-240">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="bdb5e-240">Next steps</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="bdb5e-241">มุมมองการอ่านในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="bdb5e-241">Reading view in Power BI service</span></span>](end-user-reading-view.md)
