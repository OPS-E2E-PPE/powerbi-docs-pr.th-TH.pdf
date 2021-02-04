---
title: เพิ่มแอป Power BI ไปยัง Microsoft Teams
description: คุณสามารถเพิ่มแอป Power BI ไปยัง Microsoft Teams ได้อย่างง่ายดาย แอป Power BI ส่งต่อประสบการณ์การใช้งาน Power BI service พื้นฐาน ทั้งหมดให้กับ Microsoft Teams
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
LocalizationGroup: Share your work
ms.date: 09/15/2020
ms.openlocfilehash: 1c486e1967e1661840622c74f3b86bf7bf7f7738
ms.sourcegitcommit: 7bf09116163afaae312eb2b232eb7967baee2c92
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/17/2020
ms.locfileid: "97621521"
---
# <a name="add-the-power-bi-app-to-microsoft-teams"></a><span data-ttu-id="9a689-104">เพิ่มแอป Power BI ไปยัง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9a689-104">Add the Power BI app to Microsoft Teams</span></span>

<span data-ttu-id="9a689-105">ในขณะที่พนักงานถูกกระจายและอยู่ระยะไกลจะกลายเป็นบรรทัดฐานใหม่ มีองค์กรจำนวนมากขึ้นที่จำเป็นต้องขึ้นอยู่กับ Microsoft Teams เพื่อให้พนักงานสามารถรักษาการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="9a689-105">As a distributed and remote workforce becomes the norm, more organizations are relying on Microsoft Teams to keep employees connected.</span></span> <span data-ttu-id="9a689-106">บทความนี้อธิบายการติดตั้งและโต้ตอบกับแอป Power BI ใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9a689-106">This article describes installing and interacting with the Power BI app in Microsoft Teams.</span></span> <span data-ttu-id="9a689-107">แอป Power BI ส่งต่อประสบการณ์การใช้งาน Power BI service พื้นฐาน ทั้งหมดของคุณให้กับ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9a689-107">The Power BI app brings your entire basic Power BI service experience into Microsoft Teams.</span></span>

:::image type="content" source="media/service-microsoft-teams-app/power-bi-app-teams.png" alt-text="สกรีนช็อตของแอป Power BI ใน Microsoft Teams":::

<span data-ttu-id="9a689-109">ด้วยแอป Power BI ใน Microsoft Teams คุณจะสามารถโต้ตอบกับเนื้อหา Power BI ทั้งหมดของคุณใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9a689-109">With the Power BI app in Microsoft Teams, you interact with all of your Power BI content, right in Microsoft Teams.</span></span> <span data-ttu-id="9a689-110">ราวกับว่า Power BI service สิงสถิตอยู่ใน Microsoft Teams เลยทีเดียว</span><span class="sxs-lookup"><span data-stu-id="9a689-110">It's as if the Power BI service lived inside Microsoft Teams.</span></span> <span data-ttu-id="9a689-111">แอปนี้เป็นประสบการณ์ Power BI ส่วนตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="9a689-111">This app is your personal experience of Power BI.</span></span> <span data-ttu-id="9a689-112">หลังจากที่คุณติดตั้งแล้ว คุณสามารถทำสิ่งต่าง ๆ ใน Microsoft Teams ตามที่คุณสามารถทำใน Power BI service เกือบทุกอย่าง:</span><span class="sxs-lookup"><span data-stu-id="9a689-112">After you install it, you can do almost everything in Microsoft Teams that you can do in the Power BI service:</span></span>

- <span data-ttu-id="9a689-113">สร้าง ดู และแก้ไขแดชบอร์ด รายงาน และแอป</span><span class="sxs-lookup"><span data-stu-id="9a689-113">Create, view, and edit dashboards, reports, and apps.</span></span>
- <span data-ttu-id="9a689-114">สร้างและมีส่วนร่วมในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="9a689-114">Create and participate in workspaces.</span></span>
- <span data-ttu-id="9a689-115">แชร์เนื้อหาผ่านทางอีเมลหรือผ่าน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9a689-115">Share content, either through email or through Microsoft Teams.</span></span>

<span data-ttu-id="9a689-116">มีคุณลักษณะบางอย่างที่คุณสามารถเข้าถึงได้เฉพาะใน Power BI service ในเบราว์เซอร์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9a689-116">There are a few features that you can only access in the Power BI service in a browser.</span></span> <span data-ttu-id="9a689-117">ดูส่วน [ปัญหาและข้อจำกัดที่ทราบ](#known-issues-and-limitations) ของบทความนี้สำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="9a689-117">See the [Known issues and limitations](#known-issues-and-limitations) section of this article for details.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a689-118">ข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="9a689-118">Requirements</span></span>

<span data-ttu-id="9a689-119">สำหรับ Power BI ที่จะทำงานใน Microsoft Teams ให้ตรวจสอบองค์ประกอบต่าง ๆ เหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="9a689-119">In general, for Power BI to work in Microsoft Teams, ensure these elements:</span></span>

- <span data-ttu-id="9a689-120">คุณมีสิทธิ์การใช้งาน Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="9a689-120">You have a Power BI Pro license.</span></span>
- <span data-ttu-id="9a689-121">คุณได้ลงชื่อเข้าใช้ใน Power BI service เพื่อเปิดใช้สิทธิ์การใช้งาน Power BI ของคุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="9a689-121">You have signed in to the Power BI service to activate your Power BI license.</span></span>

## <a name="install-the-power-bi-app"></a><span data-ttu-id="9a689-122">ติดตั้งแอป Power BI</span><span class="sxs-lookup"><span data-stu-id="9a689-122">Install the Power BI app</span></span>

<span data-ttu-id="9a689-123">เลือก **แอปที่เพิ่มเข้ามา (...)** ในแถบนำทางด้านซ้าย จากนั้นเลือก **Power BI**</span><span class="sxs-lookup"><span data-stu-id="9a689-123">Select **More added apps (...)** in the left navigation bar, then select **Power BI**.</span></span> <span data-ttu-id="9a689-124">ถ้าคุณไม่เห็น ให้พิมพ์ **Power BI** ในช่อง **ค้นหาแอป**</span><span class="sxs-lookup"><span data-stu-id="9a689-124">If you don't see it, type **Power BI** in the **Find an app** box.</span></span>

:::image type="content" source="media/service-microsoft-teams-app/power-bi-teams-app.png" alt-text="สกรีนช็อตของการติดตั้งแอป Power BI ใน Microsoft Teams":::

<span data-ttu-id="9a689-126">แค่นั้นเอง!</span><span class="sxs-lookup"><span data-stu-id="9a689-126">That's it!</span></span> <span data-ttu-id="9a689-127">แอป Power BI ได้รับการติดตั้งใน Microsoft Teams แล้ว</span><span class="sxs-lookup"><span data-stu-id="9a689-127">The Power BI app is installed in Microsoft Teams.</span></span>

## <a name="interact-with-your-content-in-microsoft-teams"></a><span data-ttu-id="9a689-128">โต้ตอบกับเนื้อหาของคุณใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9a689-128">Interact with your content in Microsoft Teams</span></span>

<span data-ttu-id="9a689-129">การโต้ตอบกับเนื้อหาของคุณใน Microsoft Teams จะเหมือนกับใน Power BI service</span><span class="sxs-lookup"><span data-stu-id="9a689-129">Interacting with your content in Microsoft Teams is the same as in the Power BI service.</span></span> <span data-ttu-id="9a689-130">คุณสามารถโต้ตอบกับแดชบอร์ด รายงาน แอป หรือพื้นที่ทำงานของคุณด้วยวิธีการเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="9a689-130">You interact with your dashboards, reports, apps, or workspaces in the same ways.</span></span> 

<span data-ttu-id="9a689-131">คุณยังสามารถแชร์รายงานให้กับเพื่อนร่วมงานของคุณใน Microsoft Teams จากแอป Power BI ใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9a689-131">You can even share a report to your coworkers in Microsoft Teams, from the Power BI app in Microsoft Teams.</span></span>

:::image type="content" source="media/service-microsoft-teams-app/power-bi-app-share-teams.png" alt-text="สกรีนช็อตของการใช้งานร่วมกันใน Microsoft Teams จากแอป Microsoft Teams":::

<span data-ttu-id="9a689-133">แอป Power BI ใน Microsoft Teams ยังมีฮับสำหรับการฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="9a689-133">The Power BI app in Microsoft Teams also features a hub for training.</span></span> <span data-ttu-id="9a689-134">เลือก **เรียนรู้** เพื่อดู **ศูนย์การเรียนรู้**</span><span class="sxs-lookup"><span data-stu-id="9a689-134">Select **Learn** to view the **Learning Center**.</span></span>

:::image type="content" source="media/service-microsoft-teams-app/power-bi-teams-learn-tab.png" alt-text="สกรีนช็อตของศูนย์การเรียนรู้ในแอป Power BI ใน Microsoft Teams":::

### <a name="differences-in-interactions"></a><span data-ttu-id="9a689-136">ความแตกต่างในการโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="9a689-136">Differences in interactions</span></span>

<span data-ttu-id="9a689-137">การโต้ตอบบางอย่างในแอป Teams จะแตกต่างกับในเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="9a689-137">A few interactions are different in the Teams app than they are in the browser</span></span>

- <span data-ttu-id="9a689-138">เมื่อคุณกำลังดูแดชบอร์ดหรือรายงาน คุณจะไม่เห็นแผงนำทางของ Power BI</span><span class="sxs-lookup"><span data-stu-id="9a689-138">When you're looking at a dashboard or report, you don't see the Power BI navigation pane.</span></span> <span data-ttu-id="9a689-139">เลือกปุ่ม **ปิด** เพื่อกลับไปยังหน้าแรกหรือพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="9a689-139">Select the **Close** button to go back to Home or the workspace.</span></span>

    :::image type="content" source="media/service-microsoft-teams-app/power-bi-teams-close-report.png" alt-text="สกรีนช็อตของปุ่มปิดในแอป Power BI ใน Microsoft Teams":::

- <span data-ttu-id="9a689-141">คุณสามารถเลือกที่จะเปิดรายงานใน Power BI service แทนที่จะดูใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9a689-141">You can choose to open the report in the Power BI service instead of viewing it in Microsoft Teams.</span></span> <span data-ttu-id="9a689-142">เลือก **เปิดรายการนี้บนเว็บ**</span><span class="sxs-lookup"><span data-stu-id="9a689-142">Select **Open this on the web**.</span></span>

    :::image type="content" source="media/service-microsoft-teams-app/power-bi-teams-open-web.png" alt-text="สกรีนช็อตของปุ่มเปิดรายการนี้บนเว็บในแอป Power BI ใน Microsoft Teams":::

## <a name="known-issues-and-limitations"></a><span data-ttu-id="9a689-144">ปัญหาและขีดจำกัดที่ทราบแล้ว</span><span class="sxs-lookup"><span data-stu-id="9a689-144">Known issues and limitations</span></span>

- <span data-ttu-id="9a689-145">ตัวเลือกบางอย่างใน Power BI service ไม่พร้อมใช้งานใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9a689-145">Some options in the Power BI service aren't available in Microsoft Teams.</span></span> <span data-ttu-id="9a689-146">ตัวเลือกเหล่านี้ได้แก่:</span><span class="sxs-lookup"><span data-stu-id="9a689-146">These options include:</span></span>
    - <span data-ttu-id="9a689-147">การแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="9a689-147">Notifications.</span></span>
    - <span data-ttu-id="9a689-148">การดาวน์โหลดแอปต่าง ๆ เช่น Power BI Desktop และ Power BI Paginated Report Builder</span><span class="sxs-lookup"><span data-stu-id="9a689-148">Downloading apps such as Power BI Desktop and Power BI Paginated Report Builder.</span></span>
    - <span data-ttu-id="9a689-149">การส่งคำติชม</span><span class="sxs-lookup"><span data-stu-id="9a689-149">Sending feedback.</span></span>
    - <span data-ttu-id="9a689-150">การตั้งค่าต่าง ๆ เช่น การจัดการพื้นที่เก็บข้อมูลส่วนบุคคลและการเข้าถึงพอร์ทัลผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="9a689-150">Settings such as managing personal storage and accessing the admin portal.</span></span>
- <span data-ttu-id="9a689-151">Power BI ไม่รองรับภาษาที่แปลเป็นภาษาท้องถิ่นเช่นเดียวกับที่ Microsoft Teams รองรับ</span><span class="sxs-lookup"><span data-stu-id="9a689-151">Power BI doesn't support the same localized languages that Microsoft Teams does.</span></span> <span data-ttu-id="9a689-152">ผลที่ได้คือ คุณอาจไม่เห็นการแปลที่เหมาะสมภายในรายงาน</span><span class="sxs-lookup"><span data-stu-id="9a689-152">As a result, you might not see proper localization within a report.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9a689-153">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="9a689-153">Next steps</span></span>

- [<span data-ttu-id="9a689-154">เปิดโอกาสในการทำงานทางไกลใน Microsoft Teams ด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="9a689-154">Enable remote work in Microsoft Teams with Power BI</span></span>](service-collaborate-microsoft-teams.md)

<span data-ttu-id="9a689-155">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="9a689-155">More questions?</span></span> <span data-ttu-id="9a689-156">[ลองถามชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="9a689-156">[Try asking the Power BI Community](https://community.powerbi.com/).</span></span>
