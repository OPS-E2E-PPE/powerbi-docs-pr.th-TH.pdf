---
title: ตัวอย่างการติดตาม COVID-19 สำหรับรัฐของสหรัฐอเมริกาและรัฐบาลในท้องถิ่น
description: ดาวน์โหลดและแก้ไขรายงานตัวอย่างกับรัฐและข้อมูลท้องถิ่นของสหรัฐอเมริกาสำหรับ COVID-19 การแพร่ระบาด
author: maggiesMSFT
ms.author: maggies
ms.reviewer: maggies
ms.custom: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: conceptual
ms.date: 04/28/2020
LocalizationGroup: Samples
ms.openlocfilehash: e6f8e02efa7dc2e56a945aaffcf22d8497052404
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96396026"
---
# <a name="covid-19-tracking-sample-for-us-state-and-local-governments"></a><span data-ttu-id="17163-103">ตัวอย่างการติดตาม COVID-19 สำหรับรัฐของสหรัฐอเมริกาและรัฐบาลในท้องถิ่น</span><span class="sxs-lookup"><span data-stu-id="17163-103">COVID-19 tracking sample for US state and local governments</span></span>

<span data-ttu-id="17163-104">ทีม Power BI ได้สร้างตัวอย่างการติดตาม COVID 19 ที่ช่วยให้รัฐและรัฐบาลในท้องถิ่นสามารถเผยแพร่หรือกำหนดรายงานแบบโต้ตอบเกี่ยวกับ COVID-19 ได้</span><span class="sxs-lookup"><span data-stu-id="17163-104">The Power BI team has created a COVID-19 tracking sample that enables US state and local governments to publish or customize an interactive report about COVID-19.</span></span> <span data-ttu-id="17163-105">Using Power BI Desktop, they can analyze and visualize COVID-19 data  to keep their communities informed  at the city, county, state, and national levels.</span><span class="sxs-lookup"><span data-stu-id="17163-105">Using Power BI Desktop, they can analyze and visualize COVID-19 data  to keep their communities informed  at the city, county, state, and national levels.</span></span> <span data-ttu-id="17163-106">จากนั้นใช้ Power BI เผยแพร่ไปยังเว็บพวกเขาสามารถแชร์รายงานแบบสาธารณะเพื่อแจ้งให้ประชาชนทราบ</span><span class="sxs-lookup"><span data-stu-id="17163-106">Then using Power BI Publish to Web, they can share the report publicly to inform citizens.</span></span> <span data-ttu-id="17163-107">ในบทความจะมีตัวเลือกที่แตกต่างกันสำหรับการใช้การแสดงภาพแบบโต้ตอบของ Power BI ในเนื้อเรื่อง บล็อก หรือเว็บไซต์สาธารณะของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="17163-107">The article offers different options for using Power BI interactive visualizations in your own public story, blog, or website.</span></span>

:::image type="content" source="media/sample-covid-19-us/covid-19-us-tracking-sample.png" alt-text="COVID-19 sample with US data":::

<span data-ttu-id="17163-109">บทความนี้ครอบคลุมถึงวิธีการ:</span><span class="sxs-lookup"><span data-stu-id="17163-109">This article covers how to:</span></span>

- <span data-ttu-id="17163-110">คัดลอกโค้ดฝังตัวและใส่ลงในเว็บไซต์ของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="17163-110">Copy embed code and put it on your own site.</span></span> 
- <span data-ttu-id="17163-111">ทำการกำหนดเองเช่นการจัดรูปแบบสถานะที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="17163-111">Make customizations such as formatting a specific state.</span></span>
- <span data-ttu-id="17163-112">เผยแพร่ไปยังบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="17163-112">Publish to the Power BI service.</span></span>
- <span data-ttu-id="17163-113">เผยแพร่ไปยังเว็บ</span><span class="sxs-lookup"><span data-stu-id="17163-113">Publish to the web.</span></span> 
- <span data-ttu-id="17163-114">Mash up ข้อมูลนี้กับข้อมูลจากแหล่งอื่น</span><span class="sxs-lookup"><span data-stu-id="17163-114">Mash up this data with data from another source.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="17163-115">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="17163-115">Prerequisites</span></span>

<span data-ttu-id="17163-116">ก่อนที่คุณจะสามารถเริ่มต้นใช้งาน Power BI เพื่อบอกเล่าเรื่องราวของคุณคุณจำเป็นต้องมีข้อกำหนดเบื้องต้นเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="17163-116">Before you can get started using Power BI to tell your story, you need these prerequisites:</span></span>

- <span data-ttu-id="17163-117">ดาวน์โหลดตัวอย่างใน [Power BI Desktop](https://powerbi.microsoft.com/desktop/)</span><span class="sxs-lookup"><span data-stu-id="17163-117">Download the free [Power BI Desktop](https://powerbi.microsoft.com/desktop/) app.</span></span>
- <span data-ttu-id="17163-118">[ลงทะเบียนสำหรับบริการของ Power BI](https://powerbi.microsoft.com/get-started/)</span><span class="sxs-lookup"><span data-stu-id="17163-118">Sign up for the [Power BI service](https://powerbi.microsoft.com/get-started/).</span></span>

## <a name="option-1-pre-built-embed-code"></a><span data-ttu-id="17163-119">ตัวเลือกที่ 1: โค้ดฝังตัวที่สร้างไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="17163-119">Option 1: Pre-built embed code</span></span>

<span data-ttu-id="17163-120">Microsoft ได้เผยแพร่รายงานตัวอย่างและสร้างโค้ดฝังตัวที่เผยแพร่ไปยังเว็บ</span><span class="sxs-lookup"><span data-stu-id="17163-120">Microsoft has published the sample report and created a publish-to-web embed code.</span></span> <span data-ttu-id="17163-121">คุณสามารถใช้โค้ดฝังตัวเพื่อฝังตัวอย่างที่สมบูรณ์รวมถึงมุมมองของชาติและดูรายละเอียดแนวลึกไปยังระดับรัฐและเขตในเว็บไซต์ของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="17163-121">You can use the embed code to embed the complete sample, including the national view, and drill down to the state and county level in your own website.</span></span> <span data-ttu-id="17163-122">ก่อนที่จะเผยแพร่ข้อมูลนี้เราขอแนะนำให้ตรวจทาน การปฏิเสธความรับ[ผิด](#disclaimers)ชอบ</span><span class="sxs-lookup"><span data-stu-id="17163-122">Before publishing this data, we recommend reviewing the [disclaimers](#disclaimers) in this article.</span></span>

<span data-ttu-id="17163-123">เมื่อต้องการรวมกราฟิกแบบโต้ตอบบนไซต์ของคุณให้คัดลอกและวางโค้ดฝังตัวต่อไปนี้ไปยังตำแหน่งที่คุณต้องการให้กราฟิกแสดงบนเว็บเพจของคุณ</span><span class="sxs-lookup"><span data-stu-id="17163-123">To include the interactive graphic on your site, copy and paste the following embed code to where you would like the graphic to show up on your web page.</span></span>  

```
<iframe width="1600" height="900" src="https://app.powerbi.com/view?r=eyJrIjoiMmI2ZjExMzItZTcwNy00YmUwLWFlMTAtYTUxYzVjODZmYjA5IiwidCI6ImMxMzZlZWMwLWZlOTItNDVlMC1iZWFlLTQ2OTg0OTczZTIzMiIsImMiOjF9" frameborder="0" allowFullScreen="true"></iframe>
```

<span data-ttu-id="17163-124">โค้ดฝังตัวเป็นองค์ประกอบ iFrame ของ HTML ที่คุณสามารถแทรกลงในเพจ HTML ใดๆได้</span><span class="sxs-lookup"><span data-stu-id="17163-124">The embed code is an HTML iFrame element that you can insert into any HTML page.</span></span> <span data-ttu-id="17163-125">ปรับความกว้างและความสูงของ iFrame ให้พอดีภายในไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="17163-125">Adjust the width and height of the iFrame provided to fit within your site.</span></span> <span data-ttu-id="17163-126">รายงานตัวอย่างถูกสร้างขึ้นที่สัดส่วน16:9 ดังนั้นเลือกขนาดที่รักษามิตินี้</span><span class="sxs-lookup"><span data-stu-id="17163-126">The sample report is authored at 16:9 proportions, so pick a size that preserves this dimension.</span></span> <span data-ttu-id="17163-127">เมื่อใช้อย่างถูกต้องกราฟิกจะปรากฏขึ้นโดยไม่มีขอบสีเทาพิเศษใด ๆ</span><span class="sxs-lookup"><span data-stu-id="17163-127">When implemented correctly, the graphic appears without any extra grey borders.</span></span> <span data-ttu-id="17163-128">มีประโยชน์ในการ [ ตรวจทานเคล็ดลับและเทคนิคการปรับขนาดของ iFrame ](../collaborate-share/service-publish-to-web.md#tips-for-iframe-height-and-width) เมื่อทำการเปลี่ยนแปลงเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="17163-128">It is useful to [review the iFrame sizing tips and tricks](../collaborate-share/service-publish-to-web.md#tips-for-iframe-height-and-width) when making these changes.</span></span>

## <a name="option-2-customize-the-sample-power-bi-file"></a><span data-ttu-id="17163-129">ตัวเลือกที่ 2: ปรับแต่งไฟล์ Power BI ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="17163-129">Option 2: Customize the sample Power BI file</span></span>

<span data-ttu-id="17163-130">ไฟล์ Power BI มีข้อมูลและกราฟิกแบบโต้ตอบในรูปแบบไฟล์. pbix ที่คุณสามารถแก้ไขได้ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="17163-130">The Power BI file contains the data and interactive graphic in a .pbix file format you can edit in Power BI Desktop.</span></span>  

<span data-ttu-id="17163-131">การกำหนดเองทั่วไปคือการกรองรายงานไปยังสถานะที่ระบุและจากนั้นสร้างโค้ดฝังตัวสำหรับการเผยแพร่ไปยังเว็บของคุณเองสำหรับรายงานแบบกำหนดเองของคุณ</span><span class="sxs-lookup"><span data-stu-id="17163-131">A typical customization is to filter the report to a specific state, and then to create your own publish-to-web embed code for your customized report.</span></span>

<span data-ttu-id="17163-132">ข้อมูล USAFacts มีให้ภายใต้สิทธิ์การใช้งาน Creative Commons License ที่ต้องระบุแหล่งที่มา</span><span class="sxs-lookup"><span data-stu-id="17163-132">USAFacts data is provided under a Creative Commons License that requires attribution.</span></span> <span data-ttu-id="17163-133">Before publishing this data, review the [disclaimers](#disclaimers).</span><span class="sxs-lookup"><span data-stu-id="17163-133">Before publishing this data, review the [disclaimers](#disclaimers).</span></span>

<span data-ttu-id="17163-134">หากต้องการเริ่มต้นใช้งาน [ดาวน์โหลดไฟล์ .pbix (ที่นี่)](https://go.microsoft.com/fwlink/?linkid=2125058)</span><span class="sxs-lookup"><span data-stu-id="17163-134">To get started, [download the .pbix file (here)](https://go.microsoft.com/fwlink/?linkid=2125058).</span></span>

### <a name="update-your-report"></a><span data-ttu-id="17163-135">เลือกรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="17163-135">Update your report</span></span> 

1. <span data-ttu-id="17163-136">ดาวน์โหลดเวอร์ชันล่าสุดของแอปฟรี [Power BI Desktop](https://powerbi.microsoft.com/desktop/)ถ้าคุณยังไม่ได้ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="17163-136">Download the latest version of the free app, [Power BI Desktop](https://powerbi.microsoft.com/desktop/), if you haven't already.</span></span> 

2. <span data-ttu-id="17163-137">ดาวน์โหลดไฟล์ [Retail Analysis sample .pbix](https://go.microsoft.com/fwlink/?linkid=2125058) แล้วเปิดใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="17163-137">Download the [.pbix file](https://go.microsoft.com/fwlink/?linkid=2125058), if you haven't already, and open it in Power BI Desktop.</span></span>

3. <span data-ttu-id="17163-138">หากต้องการกรองรายงานของคุณในเฉพาะรัฐ ให้เลือกลูกศรเพื่อขยายบานหน้าต่างตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="17163-138">To filter your report to a specific state, select the arrow to expand the Filters pane.</span></span>

    :::image type="content" source="media/sample-covid-19-us/power-bi-covid-19-filters-pane.png" alt-text="ขยายบานหน้าต่างตัวกรอง":::

4. <span data-ttu-id="17163-140">เลือกรัฐที่คุณสนใจ</span><span class="sxs-lookup"><span data-stu-id="17163-140">Select a state that you are interested in.</span></span> 

    :::image type="content" source="media/sample-covid-19-us/power-bi-covid-19-filter-selection.png" alt-text="เลือกรัฐ":::

5. <span data-ttu-id="17163-142">หากต้องการบันทึกไฟล์ของคุณ ให้เลือก **ไฟล์** > **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="17163-142">To save your file, select **File** > **Save**.</span></span> 

### <a name="refresh-your-report"></a><span data-ttu-id="17163-143">รีเฟรชรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="17163-143">Refresh your report</span></span> 

1. <span data-ttu-id="17163-144">เลือกปุ่ม **รีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="17163-144">Select the **Refresh** button.</span></span>

    :::image type="content" source="media/sample-covid-19-us/power-bi-desktop-refresh-button.png" alt-text="ปุ่มรีเฟรช":::

2. <span data-ttu-id="17163-146">เลือก **แบบไม่ระบุชื่อ**  > **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="17163-146">Select **Anonymous** > **Connect**.</span></span> 

    :::image type="content" source="media/sample-covid-19-us/power-bi-covid-19-azure-blob.png" alt-text="เลือกแบบไม่ระบุชื่อ":::

 
3. <span data-ttu-id="17163-148">เลือก **ละเว้นระดับความเป็นส่วนตัว** ถ้าแสดง > **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="17163-148">Select **Ignore Privacy Levels**, if shown > **Save**.</span></span> 

    :::image type="content" source="media/sample-covid-19-us/power-bi-covid-19-privacy-levels.png" alt-text="เลือกระดับความเป็นส่วนตัว":::

### <a name="publish-your-report-to-the-power-bi-service"></a><span data-ttu-id="17163-150">จากนั้น คุณจะเผยแพร่รายงานไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="17163-150">Publish your report to the Power BI service</span></span>

<span data-ttu-id="17163-151">เมื่อคุณปรับแต่งรายงานตามความต้องการของคุณแล้ว [ให้ทำตามขั้นตอนที่อธิบายไว้ที่นี่เพื่อเผยแพร่รายงานของคุณ](../create-reports/desktop-upload-desktop-files.md) ไปยังบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="17163-151">Once you've customized your report to your liking, [follow the steps outlined here to publish your report](../create-reports/desktop-upload-desktop-files.md) to the Power BI service.</span></span>

### <a name="configure-scheduled-refresh"></a><span data-ttu-id="17163-152">กำหนดค่าการรีเฟรชตามกำหนดเวลา</span><span class="sxs-lookup"><span data-stu-id="17163-152">Configure scheduled refresh</span></span>

<span data-ttu-id="17163-153">เมื่อต้องการให้ข้อมูลในรายงานให้เป็นปัจจุบัน คุณสามารถ [กำหนดค่าการรีเฟรชตามกำหนดการ](../connect-data/refresh-scheduled-refresh.md) หลังจากที่คุณได้เผยแพร่รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="17163-153">To keep the data in the report up to date, you can [configure scheduled refresh](../connect-data/refresh-scheduled-refresh.md) after you publish your report.</span></span>

<span data-ttu-id="17163-154">เมื่อคุณทำตามขั้นตอน ให้เลือกตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="17163-154">When you follow the steps, choose the following options:</span></span>

1. <span data-ttu-id="17163-155">วิธีการรับรองความถูกต้องข้อมูลประจำตัวของแหล่งข้อมูล: ไม่ระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="17163-155">Data Source Credentials Authentication Method: Anonymous</span></span>
2. <span data-ttu-id="17163-156">การตั้งค่าระดับความเป็นส่วนตัวสำหรับแหล่งข้อมูลนี้: สาธารณะ</span><span class="sxs-lookup"><span data-stu-id="17163-156">Privacy level setting for this data source: Public</span></span>

<span data-ttu-id="17163-157">เมื่อต้องการทดสอบการตั้งค่าการรีเฟรชของคุณ ให้เลือกตัวเลือก [รีเฟรชทันที](../connect-data/refresh-data.md#data-refresh)ที่พร้อมใช้งานจากรายการชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="17163-157">To test your refresh setting, select the [Refresh now](../connect-data/refresh-data.md#data-refresh) option, available from the dataset item.</span></span>

<span data-ttu-id="17163-158">ข้อมูลที่รีเฟรชจะถูกโหลดในแต่ละครั้งที่มีการเรียกใช้กำหนดการ</span><span class="sxs-lookup"><span data-stu-id="17163-158">The refreshed data is loaded each time the schedule runs.</span></span> <span data-ttu-id="17163-159">ข้อมูลพื้นฐานนั้นจัดทำโดย USAFacts และอาจไม่มีการอัปเดตบ่อยเท่ากับกำหนดการรีเฟรชของคุณ</span><span class="sxs-lookup"><span data-stu-id="17163-159">The underlying data is provided by USAFacts and may not update as frequently as your refresh schedule.</span></span> <span data-ttu-id="17163-160">ตรวจสอบ [เว็บไซต์ USAFacts](https://usafacts.org/visualizations/coronavirus-covid-19-spread-map/)  เพื่อตรวจสอบเมื่อข้อมูลเบื้องต้นได้รับการอัปเดตล่าสุด</span><span class="sxs-lookup"><span data-stu-id="17163-160">Check the [USAFacts website](https://usafacts.org/visualizations/coronavirus-covid-19-spread-map/) to know when the underlying data was last updated.</span></span> 

<span data-ttu-id="17163-161">ถ้าคุณต้องการเผยแพร่รายงานแบบกำหนดเองบนเว็บไซต์ของคุณ จะเป็นการดีที่สุดที่จะกำหนดค่าการรีเฟรชตามกำหนดเวลาของคุณเพื่อให้ทำงานได้อย่างน้อยบ่อยครั้งเท่าการอัปเดตข้อมูล USAFacts</span><span class="sxs-lookup"><span data-stu-id="17163-161">If you intend to publish the customized report on your website, it is best to configure your scheduled refresh to run at least as frequently as the USAFacts data updates.</span></span> <span data-ttu-id="17163-162">เนื่องจาก USAFacts อาจรีเฟรชข้อมูลของพวกเขาในเวลาที่แตกต่างกันในแต่ละวันคุณอาจต้องการกำหนดค่ารีเฟรชหลายครั้งในแต่ละวัน</span><span class="sxs-lookup"><span data-stu-id="17163-162">Since USAFacts may refresh their data at different times each day, you may want to configure several refreshes each day.</span></span> 

### <a name="create-a-publish-to-web-embed-code"></a><span data-ttu-id="17163-163">สร้างโค้ดแบบฝังตัวที่เผยแพร่ไปยังเว็บ</span><span class="sxs-lookup"><span data-stu-id="17163-163">Create a publish-to-web embed code</span></span> 

<span data-ttu-id="17163-164">เมื่อต้องการฝังรายงานแบบกำหนดเองของคุณในเว็บไซต์ของคุณเอง ให้ทำตามคำแนะนำสำหรับวิธีการ [สร้างโค้ดแบบฝังตัวที่มีการเผยแพร่ในเว็บของคุณเอง](../collaborate-share/service-publish-to-web.md#create-embed-codes-with-publish-to-web)</span><span class="sxs-lookup"><span data-stu-id="17163-164">To embed your customized report in your own website, follow the instructions for how to [create your own publish-to-web embed code](../collaborate-share/service-publish-to-web.md#create-embed-codes-with-publish-to-web).</span></span>

<span data-ttu-id="17163-165">เมื่อคุณเผยแพร่โค้ดแบบฝังตัวของคุณแล้ว คุณสามารถใช้ iFrame ในกล่องโต้ตอบการยืนยันเพื่อฝังในเว็บไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="17163-165">Once you publish your embed code, you use the iFrame on the confirmation dialog to embed in your website.</span></span>

<span data-ttu-id="17163-166">ถ้าคุณทำการเปลี่ยนแปลงไปยังรายงานใน Power BI Desktop คุณสามารถเผยแพร่และแทนที่รายงานที่มีอยู่ในบริการ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="17163-166">If you make changes to the report in Power BI Desktop, you can publish and replace the existing report in the Power BI service.</span></span> <span data-ttu-id="17163-167">โค้ดแบบฝังตัวไม่มีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="17163-167">The embed code doesn't change.</span></span> <span data-ttu-id="17163-168">ใช้เวลาประมาณหนึ่งชั่วโมงในการเปลี่ยนแปลงรายงานหรือข้อมูลรีเฟรชเพื่อให้ปรากฏบนเว็บไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="17163-168">It takes approximately an hour for changes to the report or refreshed data to appear on your website.</span></span> 

## <a name="option-3-mash-up-data-from-another-source"></a><span data-ttu-id="17163-169">ตัวเลือกที่ 3: Mash up ข้อมูลจากแหล่งอื่น</span><span class="sxs-lookup"><span data-stu-id="17163-169">Option 3: Mash up data from another source</span></span> 

<span data-ttu-id="17163-170">คุณยังสามารถ mash up ข้อมูลในรายงานนี้ด้วยข้อมูลจากแหล่งอื่นได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="17163-170">You can also mash up the data in this report with data from another source.</span></span> <span data-ttu-id="17163-171">ตัวอย่างต่อไปนี้จะยึดตามข้อมูลจาก [มหาวิทยาลัยจอนส์ฮอปกินส์](https://github.com/CSSEGISandData/COVID-19)</span><span class="sxs-lookup"><span data-stu-id="17163-171">The following example is based on data from [Johns Hopkins University](https://github.com/CSSEGISandData/COVID-19).</span></span> <span data-ttu-id="17163-172">ก่อนที่จะเผยแพร่ข้อมูลนี้เราขอแนะนำให้ตรวจทาน การปฏิเสธความรับ[ผิด](#disclaimers)ชอบ</span><span class="sxs-lookup"><span data-stu-id="17163-172">Before publishing this data, we recommend reviewing the [disclaimers](#disclaimers) in this article.</span></span>

1. <span data-ttu-id="17163-173">เลือก **รับข้อมูล** > **เว็บ**</span><span class="sxs-lookup"><span data-stu-id="17163-173">Select **Get Data** > **Web**.</span></span>

    :::image type="content" source="media/sample-covid-19-us/power-bi-desktop-get-data.png" alt-text="ปุ่มรับข้อมูล":::

2. <span data-ttu-id="17163-175">กรอก URL ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="17163-175">Enter the following URL:</span></span>

    ```
    https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_confirmed_global.csv
    ```

    :::image type="content" source="media/sample-covid-19-us/power-bi-covid-19-from-web.png" alt-text="เลือกข้อมูลจากเว็บ":::

3. <span data-ttu-id="17163-177">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="17163-177">Select **OK**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="17163-178">ลิงก์ที่เผยแพร่โดยมหาวิทยาลัยจอนส์ฮอปกินส์สามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="17163-178">The link published by Johns Hopkins University can change.</span></span> <span data-ttu-id="17163-179">ตรวจสอบ [หน้า GitHub จอห์นฮอปกินส์](https://github.com/CSSEGISandData/COVID-19) สำหรับข้อมูลล่าสุด</span><span class="sxs-lookup"><span data-stu-id="17163-179">Check the [Johns Hopkins GitHub page](https://github.com/CSSEGISandData/COVID-19) for the latest information.</span></span>

4. <span data-ttu-id="17163-180">เลือก **โหลด** เพื่อโหลดชุดข้อมูลสำหรับกรณีที่ได้รับการยืนยันทั้งหมดทั่วโลก</span><span class="sxs-lookup"><span data-stu-id="17163-180">Select **Load** to load the dataset for total confirmed cases worldwide.</span></span>  

    :::image type="content" source="media/sample-covid-19-us/power-bi-covid-19-load-data.png" alt-text="โหลดข้อมูลจากเว็บ":::

    <span data-ttu-id="17163-182">บทความนี้ [เชื่อมต่อกับเว็บเพจต่างๆจาก](../connect-data/desktop-connect-to-web.md)Power BI Desktop ให้ข้อมูลเพิ่มเติมเกี่ยวกับการโหลดข้อมูลจากเว็บ</span><span class="sxs-lookup"><span data-stu-id="17163-182">This article, [Connect to webpages from Power BI Desktop](../connect-data/desktop-connect-to-web.md), provides more information about loading data from the web.</span></span>
    
<span data-ttu-id="17163-183">จากนั้นคุณสามารถใช้ Power BI Desktop เพื่อแสดงภาพข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="17163-183">You can then use Power BI Desktop to visualize the data.</span></span> <span data-ttu-id="17163-184">สุดท้ายให้ใช้ขั้นตอนใน **ตัวเลือก 2:** [เผยแพร่รายงานของคุณไปยังบริการ Power BI](#publish-your-report-to-the-power-bi-service)  เพื่อเผยแพร่รายงานและสร้างโค้ดแบบฝังตัวแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="17163-184">Finally, use the steps in **Option 2:** [Publish your report to the Power BI service](#publish-your-report-to-the-power-bi-service) to publish the report and create a custom embed code.</span></span> 

## <a name="option-4-use-the-covid-19-us-tracking-template-app"></a><span data-ttu-id="17163-185">ตัวเลือกที่ 4: ใช้แอปเทมเพลตการติดตาม COVID-19 ในสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="17163-185">Option 4: Use the COVID-19 US Tracking template app</span></span>

<span data-ttu-id="17163-186">สำหรับตัวเลือกเพิ่มเติมอีกหนึ่งตัวเลือก ทีม Power BI ได้สร้าง *แอปเทมเพลต* การติดตาม COVID-19 ในสหรัฐอเมริกาเพื่อให้คุณสามารถเริ่มต้นได้ทันที</span><span class="sxs-lookup"><span data-stu-id="17163-186">For one more option, the Power BI team created the COVID-19 US Tracking *template app* to get you started immediately.</span></span> <span data-ttu-id="17163-187">แอปเทมเพลคือชุดของรายงาน แดชบอร์ด และชุดข้อมูลสำหรับแหล่งข้อมูลเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="17163-187">Template apps are bundles of reports, dashboards, and datasets for a specific data source.</span></span> <span data-ttu-id="17163-188">คุณสามารถดาวน์โหลดแอปนี้ได้จาก AppSource ใช้งาน หรือปรับเปลี่ยนให้เหมาะสมกับความต้องการของคุณแล้วเผยแพร่ไปยังเพื่อนร่วมงานของคุณได้</span><span class="sxs-lookup"><span data-stu-id="17163-188">You download them from AppSource, use them or modify to suit your needs, and distribute them to your colleagues.</span></span> 

<span data-ttu-id="17163-189">แอปการติดตาม COVID-19 ในสหรัฐอเมริกานี้ประกอบด้วยรายงานการตรวจวัด COVID-19 ที่สร้างขึ้นล่วงหน้าที่คุณสามารถนำไปใช้งานได้ทันที หรือปรับได้โดยตรงจากในบริการของ Power BI หรือดาวน์โหลดเพื่อเพิ่มแหล่งข้อมูลอื่น ๆ ได้หากคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="17163-189">This COVID-19 US Tracking template app contains a pre-built report of COVID-19 metrics that you can use as is, personalize directly in the Power BI service, or download to add other data sources if desired.</span></span> <span data-ttu-id="17163-190">เรียนรู้เกี่ยวกับการติดตั้ง[แอปเทมเพลตการติดตาม COVID-19 ในสหรัฐอเมริกา](../connect-data/service-connect-to-covid-19-tracking.md) แล้วเริ่มใช้งานได้ทันที</span><span class="sxs-lookup"><span data-stu-id="17163-190">Learn about installing the [COVID-19 US Tracking template app](../connect-data/service-connect-to-covid-19-tracking.md) and getting started right away.</span></span>

## <a name="about-the-data-source-for-this-report"></a><span data-ttu-id="17163-191">เกี่ยวกับแหล่งข้อมูลสำหรับรายงานนนี้</span><span class="sxs-lookup"><span data-stu-id="17163-191">About the data source for this report</span></span>
<span data-ttu-id="17163-192">รายงานแบบโต้ตอบนี้จะรวมข้อมูลจากศูนย์ควบคุมและป้องกันโรค (CDC) รวมถึงหน่วยงานด้านสาธารณสุขของรัฐและระดับท้องถิ่น</span><span class="sxs-lookup"><span data-stu-id="17163-192">This interactive report aggregates data from the Centers for Disease Control and Prevention (CDC), and state- and local-level public health agencies.</span></span> <span data-ttu-id="17163-193">ข้อมูลระดับเขตได้รับการยืนยันโดยอ้างอิงจากหน่วยงานของรัฐและท้องถิ่นโดยตรง (ลิงก์)</span><span class="sxs-lookup"><span data-stu-id="17163-193">County-level data is confirmed by referencing state and local agencies directly (link).</span></span>

<span data-ttu-id="17163-194">ข้อมูลจัดหาโดย USAFacts</span><span class="sxs-lookup"><span data-stu-id="17163-194">Data is provided by USAFacts.</span></span> <span data-ttu-id="17163-195">เนื่องจากความถี่ของการอัปเดตข้อมูล จึงอาจไม่สามารถแสดงจำนวนที่แน่นอนที่รายงานโดยหน่วยงานราชการหรือสื่อข่าวสาร</span><span class="sxs-lookup"><span data-stu-id="17163-195">Because of the frequency of data updates, they may not reflect the exact numbers reported by government organizations or the news media.</span></span> <span data-ttu-id="17163-196">สำหรับข้อมูลเพิ่มเติมหรือดาวน์โหลดข้อมูล โปรดเยี่ยมชม [เว็บไซต์ USAFacts](https://usafacts.org/visualizations/coronavirus-covid-19-spread-map/)</span><span class="sxs-lookup"><span data-stu-id="17163-196">For more information or to download the data, visit the [USAFacts website](https://usafacts.org/visualizations/coronavirus-covid-19-spread-map/).</span></span> 

## <a name="disclaimers"></a><span data-ttu-id="17163-197">ผิด</span><span class="sxs-lookup"><span data-stu-id="17163-197">Disclaimers</span></span>

<span data-ttu-id="17163-198">รายงานและข้อมูลนี้มีให้ "ตามสภาพ" "พร้อมข้อผิดพลาดทั้งหมด" และไม่มีการรับประกันใดๆ</span><span class="sxs-lookup"><span data-stu-id="17163-198">This report and data are provided "as is", "with all faults", and without warranty of any kind.</span></span> <span data-ttu-id="17163-199">Microsoft ไม่มีการรับประกันหรือการการันตีที่ระบุไว้อย่างชัดเจน และไม่รับผิดชอบต่อการรับประกันโดยนัยทั้งหมด ซึ่งรวมถึงอรรถประโยชน์ในเชิงพาณิชย์ ความเหมาะสมสำหรับวัตถุประสงค์เฉพาะกิจ และการไม่ละเมิดลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="17163-199">Microsoft gives no express warranties or guarantees and expressly disclaims all implied warranties, including merchantability, fitness for a particular purpose, and non-infringement.</span></span>

<span data-ttu-id="17163-200">ข้อมูล USAFacts อยู่ภายใต้สิทธิ์การใช้งาน Creative Commons License</span><span class="sxs-lookup"><span data-stu-id="17163-200">USAFacts data is available under a Creative Commons license.</span></span> <span data-ttu-id="17163-201">หากต้องการใช้งาน ให้อ้างอิง USAFacts เป็นผู้ให้บริการข้อมูลและเชื่อมโยงกลับไปยัง USAFacts</span><span class="sxs-lookup"><span data-stu-id="17163-201">To use it, cite USAFacts as the data provider and link back to USAFacts.</span></span> <span data-ttu-id="17163-202">สำหรับขั้นตอนการระบุแหล่งที่มาโดยละเอียด โปรดดูส่วน **#MadewithUSAFacts** ของหน้า USAFacts [ ไวรัสโคโรนาในสหรัฐอเมริกา: การจัดทำแผนที่แสดงการแพร่ระบาดของ COVID-19 ในรัฐและประเทศต่างๆ](https://usafacts.org/visualizations/coronavirus-covid-19-spread-map/)</span><span class="sxs-lookup"><span data-stu-id="17163-202">For exact attribution steps, see the **#MadewithUSAFacts** section of the USAFacts page, [Coronavirus in the United States: Mapping the COVID-19 outbreak in the states and counties](https://usafacts.org/visualizations/coronavirus-covid-19-spread-map/).</span></span>

<span data-ttu-id="17163-203">ข้อมูลจากมหาวิทยาลัยจอนส์ฮอปกินส์เป็นลิขสิทธิ์ของ 2020 Johns Hopkins University,  All rights reserved</span><span class="sxs-lookup"><span data-stu-id="17163-203">Johns Hopkins University data is copyright 2020 Johns Hopkins University, all rights reserved.</span></span> <span data-ttu-id="17163-204">ข้อมูลมีให้บริการแก่สาธารณะ เพื่อจุดประสงค์ทางการศึกษาการวิจัยทางวิชาการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="17163-204">It's provided to the public strictly for educational and academic research purposes.</span></span> <span data-ttu-id="17163-205">นี่คือ [ข้อตกลงการใช้งาน](https://github.com/CSSEGISandData/COVID-19/blob/master/README.md) ฉบับเต็ม ของข้อมูลที่แสดงในตัวอย่าง mashup</span><span class="sxs-lookup"><span data-stu-id="17163-205">Here are the full [Terms of Use](https://github.com/CSSEGISandData/COVID-19/blob/master/README.md) of the data shown in the mashup example.</span></span> <span data-ttu-id="17163-206">สามารถดูข้อมูลเพิ่มเติมได้จาก [เว็บไซต์ของมหาวิทยาลัยจอนส์ฮอปกินส์](https://coronavirus.jhu.edu/map-faq.html)</span><span class="sxs-lookup"><span data-stu-id="17163-206">More information is available from the [Johns Hopkins University website](https://coronavirus.jhu.edu/map-faq.html).</span></span>

## <a name="next-steps"></a><span data-ttu-id="17163-207">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="17163-207">Next steps</span></span>

[<span data-ttu-id="17163-208">รับตัวอย่างสำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="17163-208">Get samples for Power BI</span></span>](../create-reports/sample-datasets.md)




