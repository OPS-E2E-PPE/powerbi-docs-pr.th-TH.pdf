---
title: บริการ Power BI - แนวคิดพื้นฐานสำหรับผู้ใช้ทางธุรกิจ
description: พื้นที่ทำงาน แดชบอร์ด รายงาน ชุดข้อมูล และเวิร์กบุ๊กของแอปบริการ Power BI
author: mihart
ms.reviewer: mihart
featuredvideoid: B2vd4MQrz4M
ms.service: powerbi
ms.custom: seodec18
ms.subservice: powerbi-consumer
ms.topic: conceptual
ms.date: 10/08/2020
ms.author: mihart
LocalizationGroup: Get started
ms.openlocfilehash: 5c534436b93205d40251c26830be4d6acdfa034d
ms.sourcegitcommit: 6b436f6ed872cbc040ed6e2d3ac089c08fc78daf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/09/2020
ms.locfileid: "91928469"
---
# <a name="basic-concepts-for-the-power-bi-service-consumers"></a><span data-ttu-id="9ffc0-103">แนวคิดพื้นฐานสำหรับลูกค้าที่ใช้บริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="9ffc0-103">Basic concepts for the Power BI service consumers</span></span>

[!INCLUDE[consumer-appliesto-ynnm](../includes/consumer-appliesto-ynnm.md)]

[!INCLUDE [power-bi-service-new-look-include](../includes/power-bi-service-new-look-include.md)]

<span data-ttu-id="9ffc0-104">บทความนี้อนุมานว่าคุณได้อ่าน [ภาพรวม Power BI](../fundamentals/power-bi-overview.md) และได้ระบุว่าตัวเองเป็น[ผู้ใช้ทางธุรกิจของ Power BI](end-user-consumer.md)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-104">This article assumes that you've already read the [Power BI overview](../fundamentals/power-bi-overview.md) and have identified yourself as a [Power BI business user](end-user-consumer.md).</span></span> <span data-ttu-id="9ffc0-105">*ผู้ใช้ทางธุรกิจ* ได้รับเนื้อหา Power BI เช่น แดชบอร์ด รายงาน และแอปจากเพื่อนร่วมงาน</span><span class="sxs-lookup"><span data-stu-id="9ffc0-105">*Business users* receive Power BI content, like dashboards, reports, and apps, from colleagues.</span></span> <span data-ttu-id="9ffc0-106">*ผู้ใช้ทางธุรกิจ* ทำงานกับบริการของ Power BI (app.powerbi.com) ซึ่งเป็นเวอร์ชันที่ใช้ในเว็บไซต์ของ Power BI</span><span class="sxs-lookup"><span data-stu-id="9ffc0-106">*Business users* work with the Power BI service (app.powerbi.com), which is the website-based version of Power BI.</span></span>

<span data-ttu-id="9ffc0-107">การรับเนื้อหาจากผู้อื่นต้องใช้หนึ่งในรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9ffc0-107">Receiving content from others requires one of the following:</span></span>
- <span data-ttu-id="9ffc0-108">สิทธิการใช้งานผู้ใช้ Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="9ffc0-108">A Power BI Pro user license</span></span>
- <span data-ttu-id="9ffc0-109">องค์กรของคุณมีการสมัครใช้งานสำหรับ Power BI Premium และเนื้อหาที่จะใช้ร่วมกันกับคุณจากความจุ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="9ffc0-109">Your organization to have a subscription for Power BI Premium, and for the content to be shared with you from a Power BI Premium capacity.</span></span> <span data-ttu-id="9ffc0-110">[ค้นหาสิทธิการใช้งานและชนิดการสมัครใช้งานของคุณ](end-user-license.md)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-110">[Look up your license and subscription types](end-user-license.md).</span></span>

<span data-ttu-id="9ffc0-111">คุณจะได้ยินคำว่า "Power BI Desktop" หรือแค่ "Desktop"</span><span class="sxs-lookup"><span data-stu-id="9ffc0-111">You'll undoubtedly hear the term "Power BI Desktop" or just "Desktop."</span></span> <span data-ttu-id="9ffc0-112">เป็นเครื่องมือแบบสแตนด์อโลนใช้งานโดย *นักออกแบบ* ที่สร้างและแชร์แดชบอร์ดและรายงานกับคุณ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-112">It is the stand-alone tool used by *designers* who build and share dashboards and reports with you.</span></span> <span data-ttu-id="9ffc0-113">สิ่งสำคัญคือต้องทราบว่ายังมีเครื่องมือ Power BI อื่นๆ อีก</span><span class="sxs-lookup"><span data-stu-id="9ffc0-113">It's important to know that there are other Power BI tools out there.</span></span> <span data-ttu-id="9ffc0-114">ตราบใดที่คุณเป็นผู้ใช้ทางธุรกิจ\*\* คุณจะทำงานกับเฉพาะบริการ Power BI เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9ffc0-114">As long as you're a business user\*\*, you'll only work with the Power BI service.</span></span> <span data-ttu-id="9ffc0-115">บทความนี้นำไปใช้กับบริการ Power BI เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9ffc0-115">This article applies only to the Power BI service.</span></span>

## <a name="terminology-and-concepts"></a><span data-ttu-id="9ffc0-116">คำศัพท์และแนวคิด</span><span class="sxs-lookup"><span data-stu-id="9ffc0-116">Terminology and concepts</span></span>

<span data-ttu-id="9ffc0-117">บทความนี้ไม่ได้นำเสนอภาพของ Power BI หรือมีบทช่วยสอนแบบลงมือทำ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-117">This article isn't a visual tour of Power BI, nor is it a hands-on tutorial.</span></span> <span data-ttu-id="9ffc0-118">แต่เรานำเสนอเป็นบทความภาพรวมซึ่งจะทำให้คุณเข้าใจคำศัพท์และแนวคิดเกี่ยวกับ Power BI</span><span class="sxs-lookup"><span data-stu-id="9ffc0-118">Instead, it's an overview article that will get you comfortable with Power BI terminology and concepts.</span></span> <span data-ttu-id="9ffc0-119">การนำเสนอจะสอนคุณเกี่ยวกับคำศัพท์และลักษณะทั่วไป</span><span class="sxs-lookup"><span data-stu-id="9ffc0-119">It will teach you the lingo and the lay of the land.</span></span> <span data-ttu-id="9ffc0-120">สำหรับการแนะนำของบริการ Power BI และการนำทาง ให้ไปที่[เริ่มต้นใช้งานด่วน - ทัวร์ในบริการ Power BI](end-user-experience.md)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-120">For a tour of the Power BI service and its navigation, go to [Quickstart - Getting around in the Power BI service](end-user-experience.md).</span></span>

## <a name="open-the-power-bi-service-for-the-first-time"></a><span data-ttu-id="9ffc0-121">เปิดบริการ Power BI เป็นครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="9ffc0-121">Open the Power BI service for the first time</span></span>

<span data-ttu-id="9ffc0-122">*ผู้ใช้ทางธุรกิจ* Power BI ส่วนใหญ่จะได้รับบริการ Power BI เนื่องจาก 1)บริษัทซื้อใบอนุญาตและ 2)ผู้ดูแลระบบมอบหมายใบอนุญาตแก่พนักงาน</span><span class="sxs-lookup"><span data-stu-id="9ffc0-122">Most Power BI *business users* get the Power BI service because 1) their company buys licenses and 2) an admin assigns the licenses to employees.</span></span>

<span data-ttu-id="9ffc0-123">เมื่อต้องเริ่มต้นใช้งาน เปิดเบราว์เซอร์และพิมพ์ **app.powerbi.com**</span><span class="sxs-lookup"><span data-stu-id="9ffc0-123">To get started, open a browser and enter **app.powerbi.com** .</span></span> <span data-ttu-id="9ffc0-124">ในครั้งแรกที่คุณเปิดบริการ Power BI คุณจะเห็นสิ่งนี้:</span><span class="sxs-lookup"><span data-stu-id="9ffc0-124">The first time you open the Power BI service, you'll see something like the following:</span></span>

![สกรีนช็อตของหน้าจอยินดีต้อนรับสำหรับบริการ Power BI](media/end-user-basic-concepts/power-bi-home-open.png)

<span data-ttu-id="9ffc0-126">เมื่อคุณใช้บริการ Power BI คุณจะต้องปรับเปลี่ยนสิ่งที่คุณเห็นเมื่อเปิดเว็บไซต์ในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="9ffc0-126">As you use the Power BI service, you'll personalize what you see when you open the website each time.</span></span> <span data-ttu-id="9ffc0-127">ตัวอย่างเช่น บางคนชอบ Power BI เพื่อเปิดไปยัง **หน้าแรก** ในขณะที่คนอื่นมีแดชบอร์ดที่ชื่นชอบที่พวกเขาต้องการเห็นเป็นอันดับแรก</span><span class="sxs-lookup"><span data-stu-id="9ffc0-127">For example, some people like Power BI to open to  **Home** , while others have a favorite dashboard they want to see first.</span></span> <span data-ttu-id="9ffc0-128">ไม่ต้องกังวล สองบทความนี้จะสอนวิธีการปรับแต่งประสบการณ์การใช้งานของคุณ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-128">Don't worry, these two article will teach you how to personalize your experience.</span></span>

- [<span data-ttu-id="9ffc0-129">ขอแนะนำหน้าแรกของ Power BI และการค้นหาในส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="9ffc0-129">Introducing Power BI Home & Global Search</span></span>](https://powerbi.microsoft.com/blog/introducing-power-bi-home-and-global-search)

- [<span data-ttu-id="9ffc0-130">แดชบอร์ดแนะนำใน Power BI service</span><span class="sxs-lookup"><span data-stu-id="9ffc0-130">Featured dashboards in the Power BI service</span></span>](end-user-featured.md)

![สกรีนช็อตที่แสดงมุมมองหน้าแรกและมุมมองแดชบอร์ด](media/end-user-basic-concepts/power-bi-dash-home.png)

<span data-ttu-id="9ffc0-132">แต่ก่อนที่เราจะได้รับประโยชน์มากขึ้น ลองกลับมาพูดคุยเกี่ยวกับบล็อกการสร้างที่ประกอบเป็นบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="9ffc0-132">But before we get much further, let's back up and talk about the building blocks that make up the Power BI service.</span></span>

_______________________________________________________

## <a name="power-bi-content"></a><span data-ttu-id="9ffc0-133">เนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="9ffc0-133">Power BI content</span></span>

### <a name="introduction-to-building-blocks"></a><span data-ttu-id="9ffc0-134">ความรู้เบื้องต้นเกี่ยวกับบล็อกการสร้าง</span><span class="sxs-lookup"><span data-stu-id="9ffc0-134">Introduction to building blocks</span></span>

<span data-ttu-id="9ffc0-135">สำหรับ *ผู้ใช้ทางธุรกิจ* ของ Power BI บล็อกการสร้าง 5 กลุ่มคือ: **_การแสดงภาพข้อมูล_** , **_แดชบอร์ด_** , **_รายงาน_** , **_แอป_** และ **_ชุดข้อมูล_**</span><span class="sxs-lookup"><span data-stu-id="9ffc0-135">For a Power BI *business user* , the five building blocks are: **_visualizations_** , **_dashboards_** , **_reports_** , **_apps_** , and **_datasets_** .</span></span> <span data-ttu-id="9ffc0-136">สิ่งเหล่านี้บางครั้งเรียกว่าเนื้อหา *Power BI* **_content_**</span><span class="sxs-lookup"><span data-stu-id="9ffc0-136">These are sometimes referred to as *Power BI* **_content_** .</span></span> <span data-ttu-id="9ffc0-137">*เนื้อหา* มีอยู่ใน **_พื้นที่ทำงาน_**</span><span class="sxs-lookup"><span data-stu-id="9ffc0-137">*Content* exists in **_workspaces_** .</span></span> <span data-ttu-id="9ffc0-138">เวิร์กโฟลว์ทั่วไปที่เกี่ยวข้องกับบล็อกการสร้างทั้งหมด: *ผู้ออกแบบ* Power BI (สีเหลืองในแผนภาพด้านล่าง) จะรวบรวมข้อมูลจาก *ชุดข้อมูล* นำมาสู่ Power BI เพื่อการวิเคราะห์ สร้าง *รายงาน* ที่เต็มไปด้วย *การแสดงภาพข้อมูล* ที่เน้นข้อเท็จจริงและข้อมูลเชิงลึกที่น่าสนใจ ปักหมุดการแสดงภาพข้อมูลจากรายงานไปยัง *แดชบอร์ด* และแชร์รายงานและแดชบอร์ดกับ *ผู้ใช้ทางธุรกิจ* เช่นคุณ (สีดำในแผนภาพด้านล่าง)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-138">A typical workflow involves all of the building blocks: A Power BI *designer* (yellow in diagram below) collects data from *datasets* , brings it into Power BI for analysis, creates *reports* full of *visualizations* that highlight interesting facts and insights, pins visualizations from reports to *dashboards* , and shares the reports and dashboards with *business users* like you (black in diagram below).</span></span> <span data-ttu-id="9ffc0-139">*นักออกแบบ* แชร์ในรูปแบบของแดชบอร์ด รายงาน หรือแอป</span><span class="sxs-lookup"><span data-stu-id="9ffc0-139">The *designer* shares them in the form of dashboards, reports, or apps.</span></span>

![พื้นฐาน Power BI แผนภูมิลำดับงาน](media/end-user-basic-concepts/power-bi-workflow.png)

<span data-ttu-id="9ffc0-141">สำหรับคุณสมบัติพื้นฐานที่สุด:</span><span class="sxs-lookup"><span data-stu-id="9ffc0-141">At its most basic:</span></span>

- <span data-ttu-id="9ffc0-142">![สกรีนช็อตของไอคอนแสดงภาพ](media/end-user-basic-concepts/visual.png)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-142">![A screenshot of the visualization icon.](media/end-user-basic-concepts/visual.png)</span></span> <span data-ttu-id="9ffc0-143">**_การแสดงผลด้วยภาพ_** (หรือ *วิชวล* ) คือแผนภูมิประเภทหนึ่งที่สร้างด้วย *ตัวออกแบบ* Power BI</span><span class="sxs-lookup"><span data-stu-id="9ffc0-143">a **_visualization_** (or *visual* ), is a type of chart built by Power BI *designers* .</span></span> <span data-ttu-id="9ffc0-144">ภาพแสดงข้อมูลจาก *รายงาน* และ *ชุดข้อมูล*</span><span class="sxs-lookup"><span data-stu-id="9ffc0-144">The visuals display the data from *reports* and *datasets* .</span></span> <span data-ttu-id="9ffc0-145">โดยทั่วไปแล้ว *ผู้ออกแบบ* จะสร้างวิชวลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="9ffc0-145">Typically, *designers* build the visuals in Power BI Desktop.</span></span>

    <span data-ttu-id="9ffc0-146">สำหรับรายละเอียดเพิ่มเติม ให้ดูที่ [โต้ตอบกับการแสดงภาพในรายงาน แดชบอร์ด และแอป](end-user-visualizations.md)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-146">For more info, see [Interact with Visuals in reports, dashboards, and apps](end-user-visualizations.md).</span></span>

- <span data-ttu-id="9ffc0-147">![สกรีนช็อตของไอคอนฐานข้อมูล](media/end-user-basic-concepts/power-bi-dataset-icon.png)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-147">![A screenshot of the database icon.](media/end-user-basic-concepts/power-bi-dataset-icon.png)</span></span> <span data-ttu-id="9ffc0-148">*ชุดข้อมูล* คือที่เก็บข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9ffc0-148">A *dataset* is a container of data.</span></span> <span data-ttu-id="9ffc0-149">ตัวอย่างเช่น อาจเป็นไฟล์ Excel จากองค์กรอนามัยโลก</span><span class="sxs-lookup"><span data-stu-id="9ffc0-149">For example, it might be an Excel file from the World Health Organization.</span></span> <span data-ttu-id="9ffc0-150">อาจเป็นฐานข้อมูลของบริษัทของลูกค้า หรืออาจเป็นไฟล์ Salesforce</span><span class="sxs-lookup"><span data-stu-id="9ffc0-150">It could also be a company-owned database of customers or it might be a Salesforce file.</span></span> <span data-ttu-id="9ffc0-151">ชุดข้อมูลได้รับการจัดการโดย *นักออกแบบ*</span><span class="sxs-lookup"><span data-stu-id="9ffc0-151">Datasets are managed by *designers* .</span></span>

- <span data-ttu-id="9ffc0-152">![สกรีนช็อตของไอคอนแดชบอร์ด](media/end-user-basic-concepts/dashboard.png)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-152">![A screenshot of the dashboard icon.](media/end-user-basic-concepts/dashboard.png)</span></span> <span data-ttu-id="9ffc0-153">*แดชบอร์ด* เป็นหน้าจอเดียวที่มีภาพ ข้อความ และกราฟฟิคแบบโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-153">A *dashboard* is a single screen with interactive visuals, text, and graphics.</span></span> <span data-ttu-id="9ffc0-154">หน้าแดชบอร์ดจะเก็บรวบรวมเมตริกที่สำคัญที่สุดของคุณในหนึ่งหน้าจอเพื่อบอกเล่าเรื่องราวหรือตอบคำถาม</span><span class="sxs-lookup"><span data-stu-id="9ffc0-154">A dashboard collects your most important metrics, on one screen, to tell a story or answer a question.</span></span> <span data-ttu-id="9ffc0-155">เนื้อหาในหน้าแดชบอร์ดมาจากรายงานอย่างน้อยหนึ่งรายการและชุดข้อมูลอย่างน้อยหนึ่งชุด</span><span class="sxs-lookup"><span data-stu-id="9ffc0-155">The dashboard content comes from one or more reports and one or more datasets.</span></span>

    <span data-ttu-id="9ffc0-156">สำหรับข้อมูลเพิ่มเติม ให้ดูที่[แดชบอร์ดสำหรับ Power BI บริการผู้ใช้ทางธุรกิจ](end-user-dashboards.md)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-156">For more info, see [Dashboards for the Power BI service business users](end-user-dashboards.md).</span></span>

- <span data-ttu-id="9ffc0-157">![สกรีนช็อตของไอคอนรายงาน](media/end-user-basic-concepts/report.png)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-157">![A screenshot of the report icon.](media/end-user-basic-concepts/report.png)</span></span> <span data-ttu-id="9ffc0-158">*รายงาน* คือหน้าของภาพ ข้อความ และกราฟฟิคแบบโต้ตอบอย่างน้อยหนึ่งหน้าซึ่งรวมกันเป็นรายงานเดียว</span><span class="sxs-lookup"><span data-stu-id="9ffc0-158">A *report* is one or more pages of interactive visuals, text, and graphics that together make up a single report.</span></span> <span data-ttu-id="9ffc0-159">Power BI สร้างรายงานโดยอ้างอิงจากชุดข้อมูลเดียว</span><span class="sxs-lookup"><span data-stu-id="9ffc0-159">Power BI bases a report on a single dataset.</span></span> <span data-ttu-id="9ffc0-160">บ่อยครั้งที่ *นักออกแบบ* จัดระเบียบหน้ารายงานให้อยู่ในพื้นที่ส่วนกลางของความสนใจหรือตอบคำถามเดียว</span><span class="sxs-lookup"><span data-stu-id="9ffc0-160">Often, the *designer* organizes report pages to address a central area of interest or answer a single question.</span></span>

    <span data-ttu-id="9ffc0-161">สำหรับข้อมูลเพิ่มเติม ให้ดูที่[รายงานใน Power BI](end-user-reports.md)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-161">For more info, see [Reports in Power BI](end-user-reports.md).</span></span>

- <span data-ttu-id="9ffc0-162">![สกรีนช็อตของไอคอนแอป](media/end-user-basic-concepts/app.png)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-162">![A screenshot of the app icon.](media/end-user-basic-concepts/app.png)</span></span> <span data-ttu-id="9ffc0-163">*แอป* เป็นอีกวิธีหนึ่งสำหรับ *ผู้ออกแบบ* ในการจัดกลุ่มและแบ่งปันหน้าแดชบอร์ดและรายงานที่เกี่ยวข้องกัน</span><span class="sxs-lookup"><span data-stu-id="9ffc0-163">An *app* is a way for *designers* to bundle and share related dashboards and reports together.</span></span> <span data-ttu-id="9ffc0-164">*ผู้ใช้ทางธุรกิจ* ได้รับแอปบางอย่างโดยอัตโนมัติ แต่สามารถไปหาแอปอื่น ๆ ที่เพื่อนร่วมงานหรือชุมชนสร้างขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="9ffc0-164">*Business users* receive some apps automatically but can go search for other apps created by colleagues or by the community.</span></span> <span data-ttu-id="9ffc0-165">ตัวอย่างเช่นแอปพลิเคชันที่ใช้งานไม่ได้สำหรับบริการภายนอกที่คุณอาจใช้อยู่แล้วเช่น Google Analytics และ Microsoft Dynamics CRM</span><span class="sxs-lookup"><span data-stu-id="9ffc0-165">For example,out-of-the-box apps are available for external services you may already use, like Google Analytics and Microsoft Dynamics CRM.</span></span>

<span data-ttu-id="9ffc0-166">เพื่อความชัดเจน หากคุณเป็นผู้ใช้ใหม่ และคุณลงชื่อเข้าใช้บริการ Power BI เป็นครั้งแรก คุณอาจจะยังไม่เห็นแดชบอร์ด แอปพลิเคชัน หรือรายงานที่ถูกแชร์</span><span class="sxs-lookup"><span data-stu-id="9ffc0-166">To be clear, if you're a new user and you've logged in to the Power BI service for the first time, probably won't see any shared dashboards, apps, or reports yet.</span></span>

_______________________________________________________

## <a name="datasets"></a><span data-ttu-id="9ffc0-167">ชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9ffc0-167">Datasets</span></span>

<span data-ttu-id="9ffc0-168">*ชุดข้อมูล* คือคอลเลกชันข้อมูลที่ *ผู้ออกแบบ* นำเข้าหรือเชื่อมต่อและใช้เพื่อสร้างรายงานและแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="9ffc0-168">A *dataset* is a collection of data that *designers* import or connect to and then use to build reports and dashboards.</span></span> <span data-ttu-id="9ffc0-169">ในฐานะ *ผู้ใช้ทางธุรกิจ* คุณจะไม่โต้ตอบกับชุดข้อมูลโดยตรง แต่ก็ยังดีที่จะเรียนรู้ว่าชุดข้อมูลพอดีกับภาพที่ใหญ่ขึ้นอย่างไร</span><span class="sxs-lookup"><span data-stu-id="9ffc0-169">As a *business user* , you won't interact directly with datasets, but it's still nice to learn how they fit into the bigger picture.</span></span>  

<span data-ttu-id="9ffc0-170">ชุดข้อมูลแต่ละชุดแสดงมาจากแหล่งข้อมูลเดียว</span><span class="sxs-lookup"><span data-stu-id="9ffc0-170">Each dataset represents a single source of data.</span></span> <span data-ttu-id="9ffc0-171">ตัวอย่างเช่น แหล่งข้อมูลอาจเป็นสมุดงาน Excel บน OneDrive, ชุดข้อมูลแบบตาราง SQL Server Analysis Services ภายในองค์กร หรือชุดข้อมูล Salesforce</span><span class="sxs-lookup"><span data-stu-id="9ffc0-171">For example, the source could be an Excel workbook on OneDrive, an on-premises SQL Server Analysis Services tabular dataset, or a Salesforce dataset.</span></span> <span data-ttu-id="9ffc0-172">Power BI สนับสนุนแหล่งข้อมูลต่าง ๆ มากมาย</span><span class="sxs-lookup"><span data-stu-id="9ffc0-172">Power BI supports many different data sources.</span></span>

<span data-ttu-id="9ffc0-173">เมื่อนักออกแบบแชร์แอปกับคุณ คุณสามารถค้นหาชุดข้อมูลที่กำลังใช้งานได้โดยการเปิด **เนื้อหาที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="9ffc0-173">When a designer shares an app with you, you can look up which datasets are being used, by opening **Related content** .</span></span>  <span data-ttu-id="9ffc0-174">คุณจะไม่สามารถเพิ่มหรือเปลี่ยนแปลงสิ่งใดในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9ffc0-174">You won't be able to add or change anything in the dataset.</span></span> <span data-ttu-id="9ffc0-175">แต่ถ้านักออกแบบให้สิทธิ์คุณ คุณจะสามารถดาวน์โหลดรายงานให้ค้นหา [ข้อมูลเชิงลึก ในข้อมูล](end-user-insights.md)หรือแม้กระทั่ง [สร้างรายงานของคุณเอง](../create-reports/service-report-create-new.md) โดยยึดตามชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9ffc0-175">But, if the designer gives you permissions, you'll be able to download the the report, look for [insights in the data](end-user-insights.md), or even [create your own report](../create-reports/service-report-create-new.md) based on the dataset.</span></span>  

![สกรีนช็อตของหน้าผู้ใช้งาน Power BI และลูกศรชี้ไปยังส่วนชุดข้อมูลบนพื้นที่](media/end-user-basic-concepts/power-bi-datasets.png)

<span data-ttu-id="9ffc0-177">หนึ่งชุดข้อมูล...</span><span class="sxs-lookup"><span data-stu-id="9ffc0-177">One dataset...</span></span>

- <span data-ttu-id="9ffc0-178">ตัวออกแบบรายงานเพื่อสร้างแดชบอร์ดและรายงานสามารถใช้ซ้ำได้เรื่อยๆ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-178">Can be used over and over by a report designer to create dashboards and reports</span></span>

- <span data-ttu-id="9ffc0-179">สามารถใช้ในการสร้างรายงานต่าง ๆ ได้มากมาย</span><span class="sxs-lookup"><span data-stu-id="9ffc0-179">Can be used to create many different reports</span></span>

- <span data-ttu-id="9ffc0-180">การแสดงภาพจากชุดข้อมูลเดียวสามารถแสดงในหลายๆ แดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="9ffc0-180">Visuals from that one dataset can appear on many different dashboards</span></span>

  ![กราฟิกที่แสดงความสัมพันธ์ของชุดข้อมูลที่มีต่อหลายๆ กลุ่มและกลุ่มเดียว](media/end-user-basic-concepts/drawing2.png)

<span data-ttu-id="9ffc0-182">ไปที่บล็อกการสร้างถัดไป - การแสดงภาพข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9ffc0-182">On to the next building block -- visualizations.</span></span>

_______________________________________________________

## <a name="visualizations"></a><span data-ttu-id="9ffc0-183">การแสดงผลข้อมูลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-183">Visualizations</span></span>

<span data-ttu-id="9ffc0-184">การแสดงภาพ (หรือที่รู้จักกันในนามวิชวล) แสดงข้อมูลเชิงลึกที่ Power BI ค้นพบในข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9ffc0-184">Visualizations (also known as visuals) display insights that Power BI discovers in the data.</span></span> <span data-ttu-id="9ffc0-185">การแสดงภาพข้อมูลทำให้เข้าใจได้ง่ายขึ้นเนื่องจากสมองของคุณสามารถเข้าใจภาพได้เร็วกว่ากระดาษคำนวณตัวเลข</span><span class="sxs-lookup"><span data-stu-id="9ffc0-185">Visualizations make it easier to interpret the insight, because your brain can comprehend a picture quicker than a spreadsheet of numbers.</span></span>

<span data-ttu-id="9ffc0-186">เพียงบางส่วนของการแสดงภาพข้อมูลที่คุณพบใน Power BI ได้แก่ น้ำตก ริบบิ้น แผนที่ต้นไม้ พาย กรวย การ์ด กระจาย และเกจวัด</span><span class="sxs-lookup"><span data-stu-id="9ffc0-186">Just some of the visualizations you'll come across in Power BI are: waterfall, ribbon, treemap, pie, funnel, card, scatter, and gauge.</span></span>

   ![สกรีนช็อตของ 8 ตัวอย่างวิชวล](media/end-user-basic-concepts/power-bi-visuals.png)

<span data-ttu-id="9ffc0-188">ดู [รายการทั้งหมดของการแสดงภาพที่มาพร้อมกับ Power BI](end-user-visual-type.md)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-188">See the [full list of visualizations included with Power BI](end-user-visual-type.md).</span></span>

<span data-ttu-id="9ffc0-189">การแสดงภาพข้อมูลพิเศษที่เรียกว่า *ภาพแบบกำหนดเอง* สามารถเรียกใช้งานได้จากชุมชน</span><span class="sxs-lookup"><span data-stu-id="9ffc0-189">Special visualizations called *custom visuals* are available from the community.</span></span> <span data-ttu-id="9ffc0-190">หากคุณได้รับรายงานด้วยภาพที่คุณไม่รู้จัก เป็นไปได้ว่าอาจเป็นภาพแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="9ffc0-190">If you receive a report with a visual you don't recognize, likely it's a custom visual.</span></span> <span data-ttu-id="9ffc0-191">หากคุณต้องการความช่วยเหลือในการแปลภาพแบบกำหนดเองค้นหาชื่อ *ผู้ออกแบบ* ของรายงานหรือแดชบอร์ด และติดต่อเขา</span><span class="sxs-lookup"><span data-stu-id="9ffc0-191">If you need help with interpreting the custom visual, look up the name of the report or dashboard *designer* and contact them.</span></span> <span data-ttu-id="9ffc0-192">ข้อมูลที่ติดต่อพร้อมใช้งานโดยการเลือกชื่อเรื่องจากแถบเมนูด้านบน</span><span class="sxs-lookup"><span data-stu-id="9ffc0-192">Contact information is available by selecting the title from the top menu bar.</span></span>

<span data-ttu-id="9ffc0-193">หนึ่งจากการแสดงภาพในรายงาน...</span><span class="sxs-lookup"><span data-stu-id="9ffc0-193">One visualization in a report...</span></span>

- <span data-ttu-id="9ffc0-194">สามารถปรากฏหลายครั้งในรายงานเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="9ffc0-194">Can appear multiple times in the same report</span></span>

- <span data-ttu-id="9ffc0-195">สามารถปรากฏบนแดชบอร์ดที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="9ffc0-195">Can appear on many different dashboards</span></span>

_______________________________________________________

## <a name="reports"></a><span data-ttu-id="9ffc0-196">รายงาน</span><span class="sxs-lookup"><span data-stu-id="9ffc0-196">Reports</span></span>

<span data-ttu-id="9ffc0-197">รายงาน Power BI คือหน้าเพจที่แสดงภาพ กราฟิก และข้อความอย่างน้อยหนึ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="9ffc0-197">A Power BI report is one or more pages of visualizations, graphics, and text.</span></span> <span data-ttu-id="9ffc0-198">การแสดงภาพทั้งหมดในรายงานมาจากชุดข้อมูลเดียว</span><span class="sxs-lookup"><span data-stu-id="9ffc0-198">All of the visualizations in a report come from a single dataset.</span></span> <span data-ttu-id="9ffc0-199">*ผู้ออกแบบ* สร้างหน้ารายงานและแชร์ให้กับผู้อื่น; เป็นรายบุคคลหรือเป็นส่วนหนึ่งของแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="9ffc0-199">*Designers* build reports and share them with others; either individually or as part of an app.</span></span>  <span data-ttu-id="9ffc0-200">โดยทั่วไปแล้ว *ผู้ใช้ทางธุรกิจ* [โต้ตอบกับรายงานใน *มุมมองการอ่าน*](end-user-reading-view.md)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-200">Typically, *Business users* [interact with reports in *Reading view*](end-user-reading-view.md).</span></span>

![สกรีนช็อตของรายงานที่มีแท็บ](media/end-user-basic-concepts/power-bi-report.png)

<span data-ttu-id="9ffc0-202">หนึ่งรายงาน...</span><span class="sxs-lookup"><span data-stu-id="9ffc0-202">One report...</span></span>

- <span data-ttu-id="9ffc0-203">สามารถเชื่อมโยงกับหลายแดชบอร์ดได้ (ไทล์ที่ปักหมุดจากรายงานนั้นอาจปรากฏบนหลายแดชบอร์ด)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-203">Can be associated with multiple dashboards (tiles pinned from that one report can appear on multiple dashboards).</span></span>

- <span data-ttu-id="9ffc0-204">สามารถสร้างได้โดยใช้ข้อมูลจากชุดเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9ffc0-204">Can be created using data from only one dataset.</span></span>  

- <span data-ttu-id="9ffc0-205">สามารถเป็นส่วนหนึ่งของแอปได้หลายแอป</span><span class="sxs-lookup"><span data-stu-id="9ffc0-205">Can be part of multiple apps.</span></span>

  ![กราฟิกที่แสดงความสัมพันธ์สำหรับรายงาน](media/end-user-basic-concepts/drawing5.png)

_______________________________________________________

## <a name="dashboards"></a><span data-ttu-id="9ffc0-207">แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="9ffc0-207">Dashboards</span></span>

<span data-ttu-id="9ffc0-208">แดชบอร์ดรายการแสดงมุมมองแบบกราฟิกที่กำหนดเองของชุดย่อยบางรายการของชุดข้อมูลเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="9ffc0-208">A dashboard represents a customized graphical view of some subset of the underlying dataset(s).</span></span> <span data-ttu-id="9ffc0-209">*ผู้ออกแบบ* สร้างหน้าแดชบอร์ดและแชร์ให้กับ *ผู้ใช้ทางธุรกิจ* ; เป็นรายบุคคลหรือเป็นส่วนหนึ่งของแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="9ffc0-209">*Designers* build dashboards and share them with *business users* ; either individually or as part of an app.</span></span> <span data-ttu-id="9ffc0-210">แดชบอร์ดเป็นพื้นที่ทำงานเดี่ยวที่มี *ไทล์* กราฟิก และข้อความ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-210">A dashboard is a single canvas that has *tiles* , graphics, and text.</span></span>

  ![สกรีนช็อตของตัวอย่างแดชบอร์ด](media/end-user-basic-concepts/power-bi-dashboard.png)

<span data-ttu-id="9ffc0-212">ไทล์เป็นการแสดงผลภาพที่ *ผู้ออกแบบ* *ปัดหมุด* ตัวอย่างเช่น จากรายงานไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="9ffc0-212">A tile is a rendering of a visual that a *designer* *pins* , for example, from a report to a dashboard.</span></span> <span data-ttu-id="9ffc0-213">แต่ละไทล์ที่ปักหมุดจะแสดง [การแสดงภาพ](end-user-visualizations.md) ที่ผู้ออกแบบ สร้างขึ้นจากชุดข้อมูลและปักหมุดลงบนแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="9ffc0-213">Each pinned tile shows a [visualization](end-user-visualizations.md) that a designer created from a dataset and pinned to that dashboard.</span></span> <span data-ttu-id="9ffc0-214">ไทล์อาจประกอบด้วยทั้งหน้ารายงาน และสามารถประกอบด้วยข้อมูลการสตรีมแบบสดหรือวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-214">A tile can also contain an entire report page and can contain live streaming data or a video.</span></span> <span data-ttu-id="9ffc0-215">มีหลายวิธีที่ *ผู้ออกแบบ* เพิ่มไทล์ลงในแดชบอร์ด แต่มีจำนวนมากที่ครอบคลุมบทความภาพรวมนี้</span><span class="sxs-lookup"><span data-stu-id="9ffc0-215">There are many ways that *designers* add tiles to dashboards, too many to cover in this overview article.</span></span> <span data-ttu-id="9ffc0-216">เมื่อต้องการเรียนรู้เพิ่มเติม ดู[ไทล์แดชบอร์ดใน Power BI](end-user-tiles.md)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-216">To learn more, see [Dashboard tiles in Power BI](end-user-tiles.md).</span></span>

<span data-ttu-id="9ffc0-217">*ผู้ใช้ทางธุรกิจ* ไม่สามารถแก้ไขแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="9ffc0-217">*Business users* can't edit dashboards.</span></span> <span data-ttu-id="9ffc0-218">อย่างไรก็ตามคุณสามารถเพิ่มความคิดเห็น ดูข้อมูลที่เกี่ยวข้อง ตั้งค่าเป็นรายการโปรด สมัครรับข้อมูล และอื่น ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="9ffc0-218">You can however add comments, view related data, set it as favorite, subscribe, and more.</span></span>

<span data-ttu-id="9ffc0-219">จุดประสงค์บางส่วนสำหรับแดชบอร์ดคืออะไร</span><span class="sxs-lookup"><span data-stu-id="9ffc0-219">What are some purposes for dashboards?</span></span>  <span data-ttu-id="9ffc0-220">ต่อไปนี้เป็นเพียงตัวอย่างเล็กน้อย:</span><span class="sxs-lookup"><span data-stu-id="9ffc0-220">Here are just a few:</span></span>

- <span data-ttu-id="9ffc0-221">เพื่อดูข้อมูลทั้งหมดที่จำเป็นสำหรับการตัดสินใจอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="9ffc0-221">to see, in one glance, all the information needed to make decisions</span></span>

- <span data-ttu-id="9ffc0-222">เพื่อตรวจสอบข้อมูลที่สำคัญมากที่สุดเกี่ยวกับธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-222">to monitor the most-important information about your business</span></span>

- <span data-ttu-id="9ffc0-223">เพื่อให้แน่ใจว่าเพื่อนร่วมงานทั้งหมดเข้าใจตรงกัน ดู และใช้ข้อมูลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="9ffc0-223">to ensure all colleagues are on the same page; viewing and using the same information</span></span>

- <span data-ttu-id="9ffc0-224">เพื่อการตรวจสอบสถานภาพของธุรกิจ หรือผลิตภัณฑ์ หรือหน่วยธุรกิจ หรือแคมเปญการตลาด และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-224">to monitor the health of a business or product or business unit or marketing campaign, and so on</span></span>

- <span data-ttu-id="9ffc0-225">เพื่อสร้างมุมมองส่วนบุคคลของแดชบอร์ดที่ใหญ่กว่า เมตริกทั้งหมดที่เกี่ยวข้องกับคุณ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-225">to create a personalized view of a larger dashboard -- all the metrics that matter to you</span></span>

<span data-ttu-id="9ffc0-226">**หนึ่ง** แดชบอร์ด...</span><span class="sxs-lookup"><span data-stu-id="9ffc0-226">**ONE** dashboard...</span></span>

- <span data-ttu-id="9ffc0-227">สามารถแสดงภาพจากหลายชุดข้อมูลที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="9ffc0-227">can display visualizations from many different datasets</span></span>

- <span data-ttu-id="9ffc0-228">สามารถแสดงภาพจากหลายรายงานที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="9ffc0-228">can display visualizations from many different reports</span></span>

- <span data-ttu-id="9ffc0-229">สามารถแสดงภาพที่ปักหมุดจากเครื่องมืออื่น ๆ ได้ (ตัวอย่างเช่น Excel)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-229">can display visualizations pinned from other tools (for example, Excel)</span></span>

  ![กราฟิกความสัมพันธ์สำหรับแดชบอร์ด](media/end-user-basic-concepts/drawing1.png)

_______________________________________________________

## <a name="apps"></a><span data-ttu-id="9ffc0-231">แอป</span><span class="sxs-lookup"><span data-stu-id="9ffc0-231">Apps</span></span>

<span data-ttu-id="9ffc0-232">คอลเลกชันเหล่านี้ของแดชบอร์ดและรายงานจัดระเบียบเนื้อหาที่เกี่ยวข้องเข้าด้วยกันเป็นแพคเกจเดียว</span><span class="sxs-lookup"><span data-stu-id="9ffc0-232">These collections of dashboards and reports organize related content together into a single package.</span></span> <span data-ttu-id="9ffc0-233">*ผู้ออกแบบ* Power BI สร้างในพื้นที่ทำงานและแชร์แอปให้กับบุคคล กลุ่ม บริษัททั้งองค์กร หรือประชาชน</span><span class="sxs-lookup"><span data-stu-id="9ffc0-233">Power BI *designers* build them in workspaces and share apps with individuals, groups, entire organizations, or the public.</span></span> <span data-ttu-id="9ffc0-234">ในฐานะ *ผู้ใช้ทางธุรกิจ* คุณสามารถมั่นใจได้ว่าคุณและเพื่อนร่วมงานของคุณกำลังทำงานกับข้อมูลเดียวกัน เวอร์ชันของความจริงที่เชื่อถือได้เพียงเวอร์ชันเดียว</span><span class="sxs-lookup"><span data-stu-id="9ffc0-234">As a *business user* , you can be confident that you and your colleagues are working with the same information; a single trusted version of the truth.</span></span>

<span data-ttu-id="9ffc0-235">ในบางครั้งพื้นที่ทำงานของแอปจะถูกแชร์และสามารถทำให้มีผู้ใช้จำนวนมากและทำงานร่วมกันและอัปเดตได้ทั้งพื้นที่ทำงานและแอป</span><span class="sxs-lookup"><span data-stu-id="9ffc0-235">Sometimes, the app's workspace itself is shared, and there can be many people collaborating and updating both the workspace and the app.</span></span> <span data-ttu-id="9ffc0-236">ขอบเขตของสิ่งที่คุณสามารถทำได้ด้วยแอปจะถูกกำหนดโดยสิทธิ์และการเข้าถึงที่คุณได้รับ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-236">The extent of what you can do with an app will be determined by the permissions and access you are given.</span></span>

![สกรีนช็อตของหน้าจอสิทธิ์ของแอป](media/end-user-basic-concepts/power-bi-app-permissions.png)

> [!NOTE]
> <span data-ttu-id="9ffc0-238">การใช้งานแอปจะต้องมีสิทธิ์ใช้งาน Power BI Pro หรือสำหรับพื้นที่ทำงานแอปที่จะจัดเก็บไว้ในความจุระดับพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="9ffc0-238">The use of apps requires a Power BI Pro license, or for the app workspace to be stored in Premium capacity.</span></span> <span data-ttu-id="9ffc0-239">[เรียนรู้เกี่ยวกับสิทธิ์การใช้งาน](end-user-license.md)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-239">[Learn about licenses](end-user-license.md).</span></span>



<span data-ttu-id="9ffc0-240">สามารถหาแอปจากใน[บริการของ Power BI](https://powerbi.com) และจากอุปกรณ์มือถือของคุณและติดตั้งได้ง่ายๆ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-240">Apps are easy to find and install in the [Power BI service](https://powerbi.com) and on your mobile device.</span></span> <span data-ttu-id="9ffc0-241">หลังจากที่คุณติดตั้งแอป คุณไม่จำเป็นต้องจำชื่อของแดชบอร์ดและรายงานต่าง ๆ มากมาย</span><span class="sxs-lookup"><span data-stu-id="9ffc0-241">After you install an app, you don't have to remember the names of a lot of different dashboards and reports.</span></span> <span data-ttu-id="9ffc0-242">ทุกอย่างรวมกันอยู่ในแอปเดียว ในเบราว์เซอร์ของคุณ หรือ บนอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-242">They're all together in one app, in your browser, or on your mobile device.</span></span>

<span data-ttu-id="9ffc0-243">แอปนี้มีแดชบอร์ดสองรายการและรายงานสองชุดซึ่งประกอบกันเป็นแอปเดียว</span><span class="sxs-lookup"><span data-stu-id="9ffc0-243">This app has two dashboards and two reports that make up a single app.</span></span> <span data-ttu-id="9ffc0-244">หากคุณต้องการเลือกลูกศรทางด้านขวาของชื่อรายงานคุณจะเห็นรายการของเพจที่สร้างรายงานนั้น</span><span class="sxs-lookup"><span data-stu-id="9ffc0-244">If you were to select the arrow to the right of a report name, you'd see a list of pages that make up that report.</span></span>

![สกรีนช็อตของเนื้อหาที่เกี่ยวข้องสำหรับแอปที่เลือก](media/end-user-basic-concepts/power-bi-app-display.png)

<span data-ttu-id="9ffc0-246">เมื่อใดก็ตามที่มีการอัปเดตแอป คุณจะเห็นการเปลี่ยนแปลงโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-246">Whenever the app is updated, you automatically see the changes.</span></span> <span data-ttu-id="9ffc0-247">ผู้ออกแบบยังสามารถควบคุมกำหนดการสำหรับจำนวนครั้งที่ Power BI รีเฟรชข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9ffc0-247">Also, the designer controls the schedule for how often Power BI refreshes the data.</span></span> <span data-ttu-id="9ffc0-248">คุณไม่ต้องกังวลเกี่ยวกับการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="9ffc0-248">You don't need to worry about keeping it up-to-date.</span></span>

<span data-ttu-id="9ffc0-249">คุณสามารถรับแอปในสองสามวิธีที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="9ffc0-249">You can get apps in a few different ways:</span></span>

- <span data-ttu-id="9ffc0-250">ตัวออกแบบแอปสามารถติดตั้งแอปโดยอัตโนมัติในบัญชี Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-250">The app designer can install the app automatically in your Power BI account.</span></span>

- <span data-ttu-id="9ffc0-251">ผู้ออกแบบแอปสามารถส่งลิงก์โดยตรงไปยังแอปฯได้ให้กับคุณได้</span><span class="sxs-lookup"><span data-stu-id="9ffc0-251">The app designer can send you a direct link to an app.</span></span>

- <span data-ttu-id="9ffc0-252">คุณสามารถค้นหาจากภายในบริการของ Power BI สำหรับแอปที่พร้อมใช้งานสำหรับคุณจากองค์กรของคุณหรือจากชุมชน</span><span class="sxs-lookup"><span data-stu-id="9ffc0-252">You can search from within the Power BI service for apps available to you from your organization or from the community.</span></span> <span data-ttu-id="9ffc0-253">คุณสามารถเข้าชมใน [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps?product=power-bi) ที่ซึ่งคุณจะเห็นแอปทั้งหมดที่คุณสามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="9ffc0-253">You can also visit [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps?product=power-bi), where you will see all the apps that you can use.</span></span>

<span data-ttu-id="9ffc0-254">ใน Power BI บนอุปกรณ์เคลื่อนที่ของคุณ คุณสามารถเติดตั้งแอปได้ จากลิงก์โดยตรงเท่านั้น และไม่สามารถตัดตั้งจาก AppSource</span><span class="sxs-lookup"><span data-stu-id="9ffc0-254">In Power BI on your mobile device, you can only install apps from a direct link, and not from AppSource.</span></span> <span data-ttu-id="9ffc0-255">ถ้าผู้ออกแบบแอปติดตั้งแอปโดยอัตโนมัติ คุณจะเห็นได้ในรายการของแอป</span><span class="sxs-lookup"><span data-stu-id="9ffc0-255">If the app designer installs the app automatically, you'll see it in your list of apps.</span></span>

<span data-ttu-id="9ffc0-256">เมื่อติดตั้งแอปแล้ว เพียงเลือกแอปจากรายการแอปของคุณ และเลือกหน้าแดชบอร์ดหรือรายงานที่จะเปิดและสำรวจก่อน</span><span class="sxs-lookup"><span data-stu-id="9ffc0-256">Once you've installed the app, just select it from your Apps list and select which dashboard or report to open and explore first.</span></span>

![สกรีนช็อตของแอปที่เลือกในบานหน้าต่างด้านซ้ายของ Power BI](media/end-user-basic-concepts/power-bi-apps-card.png)

<span data-ttu-id="9ffc0-258">ฉันหวังว่าบทความนี้จะทำให้คุณเข้าใจเกี่ยวกับบล็อกการสร้างที่ประกอบกันเป็นบริการ Power BI สำหรับผู้ใช้ทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="9ffc0-258">I hope this article gave you an understanding of the building blocks that make up the Power BI service for business users.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9ffc0-259">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="9ffc0-259">Next steps</span></span>

- <span data-ttu-id="9ffc0-260">ตรวจทานและบุ๊กมาร์ก[อภิธานศัพท์](end-user-glossary.md)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-260">Review and bookmark the [Glossary](end-user-glossary.md)</span></span>

- <span data-ttu-id="9ffc0-261">ชม[การแนะนำบริการของ Power BI](end-user-experience.md)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-261">Take a [tour of the Power BI service](end-user-experience.md)</span></span>

- <span data-ttu-id="9ffc0-262">อ่าน [ภาพรวมของ Power BI ที่เขียนขึ้นโดยเฉพาะสำหรับผู้ใช้ทางธุรกิจ](end-user-consumer.md)</span><span class="sxs-lookup"><span data-stu-id="9ffc0-262">Read the [overview of Power BI written especially for business users](end-user-consumer.md)</span></span>

- <span data-ttu-id="9ffc0-263">ดูวิดีโอที่จะตรวจทานแนวคิดพื้นฐานและให้คำแนะนำของบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="9ffc0-263">Watch a video in which Will reviews the basic concepts and gives a tour of the Power BI service.</span></span>

    <iframe width="560" height="315" src="https://www.youtube.com/embed/B2vd4MQrz4M" frameborder="0" allowfullscreen></iframe>
