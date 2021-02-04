---
title: 'บทช่วยสอน: เริ่มต้นการสร้างในบริการ Power BI'
description: เริ่มต้นใช้งานบริการออนไลน์ Power BI (app.powerbi.com)
author: mihart
ms.author: mihart
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-fundamentals
ms.topic: tutorial
ms.date: 07/08/2020
LocalizationGroup: Get started
ms.openlocfilehash: 4e74bec243faad281c457caaa15a6edacf2b10cb
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96417140"
---
# <a name="tutorial-get-started-creating-in-the-power-bi-service"></a><span data-ttu-id="4a491-103">บทช่วยสอน: เริ่มต้นการสร้างในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="4a491-103">Tutorial: Get started creating in the Power BI service</span></span>
<span data-ttu-id="4a491-104">บทช่วยสอนนี้เป็นการแนะนำคุณสมบัติการทำงานบางรายการของ *บริการของ Power BI*</span><span class="sxs-lookup"><span data-stu-id="4a491-104">This tutorial is an introduction to some of the features of the *Power BI service*.</span></span> <span data-ttu-id="4a491-105">ในบทช่วยสอนนี้ คุณจะได้เชื่อมต่อกับข้อมูล สร้างรายงานและแดชบอร์ด และถามคำถามต่าง ๆ เกี่ยวกับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="4a491-105">In it, you connect to data, create a report and a dashboard, and ask questions of your data.</span></span> <span data-ttu-id="4a491-106">คุณสามารถทำสิ่งต่าง ๆ ได้มากมายด้วยบริการของ Power BI บทช่วยสอนนี้เป็นเพียงการทำงานเบื้องต้นสำหรับคุณเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4a491-106">You can do much more in the Power BI service; this tutorial is just to whet your appetite.</span></span> <span data-ttu-id="4a491-107">เพื่อทำความเข้าใจว่าบริการ Power BI นั้นเหมาะสมกับข้อเสนอ Power BI อื่นๆ อย่างไร เราขอแนะนำให้คุณอ่านเรื่อง [Power BI คืออะไร](power-bi-overview.md)</span><span class="sxs-lookup"><span data-stu-id="4a491-107">For an understanding of how the Power BI service fits in with the other Power BI offerings, we recommend reading [What is Power BI](power-bi-overview.md).</span></span>

<span data-ttu-id="4a491-108">คุณเป็น *ผู้อ่าน* รายงานมากกว่าผู้สร้างหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4a491-108">Are you a report *reader* rather than a creator?</span></span> <span data-ttu-id="4a491-109">[การเดินทางสำรวจบริการ Power BI](../consumer/end-user-experience.md) เป็นจุดเริ่มต้นที่ดีสำหรับคุณ</span><span class="sxs-lookup"><span data-stu-id="4a491-109">[Getting around in the Power BI service](../consumer/end-user-experience.md) is a good starting place for you.</span></span>

:::image type="content" source="media/service-get-started/power-bi-service-rearranged-dashboard.png" alt-text="ภาพหน้าจอของแดชบอร์ดตัวอย่างด้านการเงิน":::

<span data-ttu-id="4a491-111">ในบทช่วยสอนนี้ คุณจะทำขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="4a491-111">In this tutorial, you complete the following steps:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="4a491-112">ลงชื่อเข้าใช้บัญชีออนไลน์ Power BI ของคุณ หรือลงทะเบียน ถ้าคุณยังไม่มีบัญชี</span><span class="sxs-lookup"><span data-stu-id="4a491-112">Sign in to your Power BI online account, or sign up, if you don't have an account yet.</span></span>
> * <span data-ttu-id="4a491-113">เปิดบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="4a491-113">Open the Power BI service.</span></span>
> * <span data-ttu-id="4a491-114">รับข้อมูลบางอย่าง และเปิดในมุมมองรายงาน</span><span class="sxs-lookup"><span data-stu-id="4a491-114">Get some data and open it in report view.</span></span>
> * <span data-ttu-id="4a491-115">ใช้ข้อมูลนั้นเพื่อสร้างการแสดงภาพ และบันทึกเป็นรายงาน</span><span class="sxs-lookup"><span data-stu-id="4a491-115">Use that data to create visualizations and save it as a report.</span></span>
> * <span data-ttu-id="4a491-116">สร้างแดชบอร์ด โดยปักหมุดไทล์จากรายงาน</span><span class="sxs-lookup"><span data-stu-id="4a491-116">Create a dashboard by pinning tiles from the report.</span></span>
> * <span data-ttu-id="4a491-117">เพิ่มการแสดงภาพอื่น ๆ ที่แดชบอร์ดของคุณโดยใช้เครื่องมือการถามตอบตามภาษาธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="4a491-117">Add other visualizations to your dashboard by using the Q&A natural-language tool.</span></span>
> * <span data-ttu-id="4a491-118">ปรับขนาด จัดเรียงใหม่ และแก้ไขรายละเอียดสำหรับไทล์บนแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="4a491-118">Resize, rearrange, and edit details for the tiles on the dashboard.</span></span>
> * <span data-ttu-id="4a491-119">ล้างข้อมูล โดยการลบชุดข้อมูล รายงาน และแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="4a491-119">Clean up resources by deleting the dataset, report, and dashboard.</span></span>

## <a name="sign-up-for-the-power-bi-service"></a><span data-ttu-id="4a491-120">ลงชื่อออกจากบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="4a491-120">Sign up for the Power BI service</span></span>
<span data-ttu-id="4a491-121">คุณต้องมีสิทธิ์การใช้งาน Power BI Pro เพื่อสร้างเนื้อหาใน Power BI</span><span class="sxs-lookup"><span data-stu-id="4a491-121">You need a Power BI Pro license to create content in Power BI.</span></span> <span data-ttu-id="4a491-122">ถ้าคุณยังไม่มีบัญชี Power BI [ให้ลงทะเบียน Power BI Pro แบบทดลองใช้ฟรี](https://app.powerbi.com/signupredirect?pbi_source=web) ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="4a491-122">If you don't have a Power BI account, [sign up for a free Power BI Pro trial](https://app.powerbi.com/signupredirect?pbi_source=web) before you begin.</span></span>

## <a name="step-1-get-data"></a><span data-ttu-id="4a491-123">ขั้นตอนที่ 1: รับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4a491-123">Step 1: Get data</span></span>

<span data-ttu-id="4a491-124">เมื่อคุณต้องการสร้างรายงาน Power BI บ่อยครั้งที่คุณมักจะเริ่มต้นใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4a491-124">Often when you want to create a Power BI report, you start in Power BI Desktop.</span></span> <span data-ttu-id="4a491-125">Power BI Desktop ให้ประสิทธิภาพมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="4a491-125">Power BI Desktop offers more power.</span></span> <span data-ttu-id="4a491-126">คุณสามารถแปลง จัดรูปร่าง และสร้างแบบจำลองข้อมูลก่อนที่จะเริ่มออกแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="4a491-126">You can transform, shape, and model data, before you start designing report.</span></span> <span data-ttu-id="4a491-127">แต่ครั้งนี้ เราจะเริ่มต้นจากการสร้างรายงานในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="4a491-127">This time though, we're going to start from scratch creating a report in the Power BI service.</span></span>

<span data-ttu-id="4a491-128">ในบทช่วยสอนนี้ เราได้รับข้อมูลจากไฟล์ Microsoft Excel แบบง่าย</span><span class="sxs-lookup"><span data-stu-id="4a491-128">In this tutorial, we get data from a simple Microsoft Excel file.</span></span> <span data-ttu-id="4a491-129">คุณต้องการทำตามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4a491-129">Want to follow along?</span></span> <span data-ttu-id="4a491-130">[ดาวน์โหลดไฟล์ตัวอย่างทางการเงิน](https://go.microsoft.com/fwlink/?LinkID=521962)</span><span class="sxs-lookup"><span data-stu-id="4a491-130">[Download the Financial Sample file](https://go.microsoft.com/fwlink/?LinkID=521962).</span></span>

1. <span data-ttu-id="4a491-131">ในการเริ่มต้น ให้เปิดบริการ Power BI (app.powerbi.com) ในเบราว์เซอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="4a491-131">To begin, open the Power BI service (app.powerbi.com) in your browser.</span></span> 

    <span data-ttu-id="4a491-132">ไม่มีบัญชีใช่หรือ</span><span class="sxs-lookup"><span data-stu-id="4a491-132">Don’t have an account?</span></span> <span data-ttu-id="4a491-133">ไม่ต้องกังวล คุณสามารถ[ลงทะเบียนเพื่อรับสิทธิ์ทดลองใช้ Power BI Pro ฟรี](https://app.powerbi.com/signupredirect?pbi_source=web)</span><span class="sxs-lookup"><span data-stu-id="4a491-133">No worries, you can [sign up for a free Power BI Pro trial](https://app.powerbi.com/signupredirect?pbi_source=web)</span></span>

1. <span data-ttu-id="4a491-134">ให้เลือก **พื้นที่ทำงานของฉัน** ในบานหน้าต่างการนำทาง</span><span class="sxs-lookup"><span data-stu-id="4a491-134">Select **My workspace** in the navigation pane.</span></span>

1. <span data-ttu-id="4a491-135">ใน **พื้นที่ทำงานของฉัน** ให้เลือก **ใหม่** > **อัปโหลดไฟล์**</span><span class="sxs-lookup"><span data-stu-id="4a491-135">In **My workspace**, select **New** > **Upload a file**.</span></span>

    <span data-ttu-id="4a491-136">หน้า **รับข้อมูล** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="4a491-136">The **Get Data** page opens.</span></span>   

3. <span data-ttu-id="4a491-137">ภายใต้ส่วน **สร้างเนื้อหาใหม่** ตรวจสอบให้แน่ใจว่ามีการเลือก **ไฟล์** จากนั้นเลือกตำแหน่งที่คุณบันทึกไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="4a491-137">Under the **Create new content** section, make sure **Files** is selected, then select the location where you saved the Excel file.</span></span>
   
    :::image type="content" source="media/service-get-started/power-bi-service-get-data-local-file.png" alt-text="ภาพหน้าจอของสร้างเนื้อหาใหม่ > ไฟล์":::

5. <span data-ttu-id="4a491-139">เรียกดูไฟล์บนคอมพิวเตอร์ของคุณ และเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="4a491-139">Browse to the file on your computer, and choose **Open**.</span></span>

5. <span data-ttu-id="4a491-140">สำหรับบทช่วยสอนนี้ เราเลือก **นำเข้า** เพื่อเพิ่มไฟล์ Excel เป็นชุดข้อมูลที่เราสามารถใช้เพื่อสร้างรายงานและแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="4a491-140">For this tutorial, we select **Import** to add the Excel file as a dataset, which we can then use to create reports and dashboards.</span></span> <span data-ttu-id="4a491-141">ถ้าคุณเลือก **อัปโหลด** เวิร์กบุ๊ก Excel ทั้งหมดถูกอัปโหลดไปยัง Power BI ซึ่งคุณสามารถเปิด และแก้ไขใน Excel Online</span><span class="sxs-lookup"><span data-stu-id="4a491-141">If you select **Upload**, the entire Excel workbook is uploaded to Power BI, where you can open and edit it in Excel Online.</span></span>
   
   :::image type="content" source="media/service-get-started/power-bi-import.png" alt-text="ภาพหน้าจอของการเลือกนำเข้า":::
6. <span data-ttu-id="4a491-143">เมื่อชุดข้อมูลของคุณพร้อมแล้ว ให้เลือก **ตัวเลือกเพิ่มเติม (...)** ถัดจากชุดข้อมูลตัวอย่างทางการเงินของคุณ จากนั้นเลือก **สร้างรายงาน**</span><span class="sxs-lookup"><span data-stu-id="4a491-143">When your dataset is ready, select **More options (...)** next to your Financial Sample dataset, then select **Create report**.</span></span>
1. <span data-ttu-id="4a491-144">เปิดตัวแก้ไขรายงาน</span><span class="sxs-lookup"><span data-stu-id="4a491-144">open the report editor.</span></span> 

    :::image type="content" source="media/service-get-started/power-bi-service-datasets.png" alt-text="ภาพหน้าจอของเนื้อหาทั้งหมด > สร้างรายงาน":::

    <span data-ttu-id="4a491-146">พื้นที่ทำงานสำหรับรายงานว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="4a491-146">The report canvas is blank.</span></span> <span data-ttu-id="4a491-147">เราจะเห็นหน้าต่าง **ตัวกรอง** **การแสดงภาพ** และ **เขตข้อมูล** ทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="4a491-147">We see the **Filters**, **Visualizations**, and **Fields** panes on the right.</span></span>

    :::image type="content" source="media/service-get-started/power-bi-service-blank-report.png" alt-text="ภาพหน้าจอของผืนผ้าใบรายงานเปล่า":::

    > [!TIP]
    > <span data-ttu-id="4a491-149">เลือกปุ่มการนำทางส่วนกลางที่มุมซ้ายบนเพื่อยุบบานหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="4a491-149">Select the global navigation button in the upper-left corner to collapse the navigation pane.</span></span> <span data-ttu-id="4a491-150">วิธีที่ผืนผ้าใบของคุณมีพื้นที่มากขึ้น</span><span class="sxs-lookup"><span data-stu-id="4a491-150">That way your canvas has more room.</span></span>
    >
    >:::image type="content" source="media/service-get-started/power-bi-global-nav-button.png" alt-text="ปุ่มการนำทางส่วนกลาง":::
    >

7. <span data-ttu-id="4a491-152">ขณะนี้คุณอยู่ในมุมมองการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="4a491-152">You're currently in Editing view.</span></span> <span data-ttu-id="4a491-153">สังเกตเห็นตัวเลือก **มุมมองการอ่าน** ในแถบเมนู</span><span class="sxs-lookup"><span data-stu-id="4a491-153">Notice the **Reading view** option in the menu bar.</span></span> 

    :::image type="content" source="media/service-get-started/power-bi-service-reading-view.png" alt-text="ภาพหน้าจอของตัวเลือกมุมมองการอ่าน":::

    <span data-ttu-id="4a491-155">ขณะอยู่ในมุมมองการแก้ไข คุณสามารถแก้ไขรายงานได ้เนื่องจากคุณเป็น *เจ้าของ* และ *ผู้สร้าง* รายงาน</span><span class="sxs-lookup"><span data-stu-id="4a491-155">While in Editing view, you can modify reports, because you're the *owner* and *creator* of the report.</span></span> <span data-ttu-id="4a491-156">เมื่อคุณแชร์รายงานของคุณกับเพื่อนร่วมงาน บ่อยครั้งที่พวกเขาเท่านั้นจะสามารถโต้ตอบกับรายงานในมุมมองการอ่าน</span><span class="sxs-lookup"><span data-stu-id="4a491-156">When you share your report with colleagues, often they can only interact with the report in Reading view.</span></span> <span data-ttu-id="4a491-157">พวกเขาเป็น *ผู้บริโภค* รายงานใน **พื้นที่ทำงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="4a491-157">They are *consumers* of reports in your **My workspace**.</span></span> 

## <a name="step-2-create-a-chart-in-a-report"></a><span data-ttu-id="4a491-158">ขั้นตอนที่ 2: สร้างแผนภูมิในรายงาน</span><span class="sxs-lookup"><span data-stu-id="4a491-158">Step 2: Create a chart in a report</span></span>
<span data-ttu-id="4a491-159">หลังจากที่คุณเชื่อมต่อกับข้อมูลแล้ว เริ่มต้นสำรวจ</span><span class="sxs-lookup"><span data-stu-id="4a491-159">Now that you've connected to data, start exploring.</span></span> <span data-ttu-id="4a491-160">เมื่อคุณพบสิ่งที่น่าสนใจ คุณสามารถบันทึกลงในผืนผ้าใบรายงาน</span><span class="sxs-lookup"><span data-stu-id="4a491-160">When you've found something interesting, you can save it on the report canvas.</span></span> <span data-ttu-id="4a491-161">จากนั้นคุณสามารถปักหมุดมันไว้ที่แดชบอร์ดเพื่อตรวจสอบและดูว่าจะเปลี่ยนแปลงอย่างไรเมื่อเวลาผ่านไป</span><span class="sxs-lookup"><span data-stu-id="4a491-161">Then you can pin it to a dashboard to monitor it and see how it changes over time.</span></span> <span data-ttu-id="4a491-162">แต่สิ่งแรกที่ต้องทำ</span><span class="sxs-lookup"><span data-stu-id="4a491-162">But first things first.</span></span>
    
1. <span data-ttu-id="4a491-163">ในตัวแก้ไขรายงาน ให้เริ่มต้นในบานหน้าต่าง **เขตข้อมูล** ทางด้านขวาของหน้าเพื่อสร้างรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="4a491-163">In the report editor, start in the **Fields** pane on the right side of the page to build a visualization.</span></span> <span data-ttu-id="4a491-164">เลือกเขตข้อมูล **ยอดขายรวม** เขตข้อมูล **วันที่**</span><span class="sxs-lookup"><span data-stu-id="4a491-164">Select the  **Gross Sales** field, then the **Date** field.</span></span>
   
   :::image type="content" source="media/service-get-started/power-bi-service-fields-pane-selected.png" alt-text="ภาพหน้าจอของรายการเขตข้อมูล":::

    <span data-ttu-id="4a491-166">Power BI วิเคราะห์ข้อมูลและสร้างการแสดงข้อมูลด้วยภาพแผนภูมิคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="4a491-166">Power BI analyzes the data and creates a column chart visualization.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="4a491-167">ถ้าคุณเลือกเขตข้อมูล **วันที่** แทนที่ **ยอดขายรวม** มาก่อนแล้ว คุณจะเห็นตาราง</span><span class="sxs-lookup"><span data-stu-id="4a491-167">If you selected the **Date** field first instead of **Gross Sales**, you see a table.</span></span> <span data-ttu-id="4a491-168">ไม่ต้องกังวล!</span><span class="sxs-lookup"><span data-stu-id="4a491-168">No worries!</span></span> <span data-ttu-id="4a491-169">เรากำลังจะเปลี่ยนการแสดงข้อมูลด้วยภาพในขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4a491-169">We're going to change the visualization in the next step.</span></span>

    <span data-ttu-id="4a491-170">เขตข้อมูลบางอันมีสัญลักษณ์ซิกมาถัดจากเขตข้อมูลดังกล่าว เพราะ Power BI ตรวจพบว่าเขตข้อมูลประกอบด้วยค่าตัวเลข</span><span class="sxs-lookup"><span data-stu-id="4a491-170">Some fields have sigma symbols next to them because Power BI detected that they contain numeric values.</span></span>

    :::image type="content" source="media/service-get-started/power-bi-sigma-fields.png" alt-text="เขตข้อมูลที่มีสัญลักษณ์ซิกมา":::

2. <span data-ttu-id="4a491-172">สลับไปยังวิธีการแสดงข้อมูลของคุณแบบอื่นกันเถอะ</span><span class="sxs-lookup"><span data-stu-id="4a491-172">Let's switch to a different way of displaying this data.</span></span> <span data-ttu-id="4a491-173">แผนภูมิเส้นเป็นวิชวลที่ดีสำหรับการแสดงค่าเมื่อเวลาผ่านไป</span><span class="sxs-lookup"><span data-stu-id="4a491-173">Line charts are good visuals for displaying values over time.</span></span> <span data-ttu-id="4a491-174">เลือกไอคอน **แผนภูมิเส้น** จากบานหน้าต่าง **การแสดงข้อมูลด้วยภาพ**</span><span class="sxs-lookup"><span data-stu-id="4a491-174">Select the **Line chart** icon from the **Visualizations** pane.</span></span>
   
   :::image type="content" source="media/service-get-started/power-bi-service-select-line-chart.png" alt-text="ภาพหน้าจอของตัวแก้ไขรายงานที่มีแผนภูมิเส้นที่เลือก":::

3. <span data-ttu-id="4a491-176">แผนภูมินี้น่าสนใจ ดังนั้นให้ *ปักหมุด* ที่แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="4a491-176">This chart looks interesting, so let's *pin* it to a dashboard.</span></span> <span data-ttu-id="4a491-177">วางเมาส์เหนือการแสดงภาพแล้วเลือกไอคอนปักหมุด</span><span class="sxs-lookup"><span data-stu-id="4a491-177">Hover over the visualization and select the pin icon.</span></span>
   
   :::image type="content" source="media/service-get-started/power-bi-service-pin-visual.png" alt-text="ภาพหน้าจอของไอคอนหมุด":::

4. <span data-ttu-id="4a491-179">เนื่องจากเป็นรายงานใหม่ คุณจะได้รับแจ้งให้บันทึกก่อนที่คุณสามารถปักหมุดการแสดงภาพไปยังแดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="4a491-179">Because this report is new, you're prompted to save it before you can pin a visualization to a dashboard.</span></span> <span data-ttu-id="4a491-180">ตั้งชื่อรายงานของคุณ (ตัวอย่างเช่น *รายงานตัวอย่างทางการเงิน*) จากนั้น **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="4a491-180">Give your report a name (for example, *Financial Sample report*), then **Save**.</span></span> 

    <span data-ttu-id="4a491-181">ในตอนนี้คุณกำลังดูรายงานในมุมมองการอ่าน</span><span class="sxs-lookup"><span data-stu-id="4a491-181">Now you're looking at the report in Reading view.</span></span> 

6. <span data-ttu-id="4a491-182">เลือกไอคอน **หมุด** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="4a491-182">Select the **Pin** icon again.</span></span>
 
5. <span data-ttu-id="4a491-183">เลือก **แดชบอร์ดใหม่** และตั้งชื่อเป็น *แดชบอร์ดตัวอย่างด้านการเงิน* เป็นต้น</span><span class="sxs-lookup"><span data-stu-id="4a491-183">Select **New dashboard** and name it *Financial Sample dashboard*, for example.</span></span> 
   
   :::image type="content" source="media/service-get-started/power-bi-pin.png" alt-text="ภาพหน้าจอของชื่อแดชบอร์ด":::
  
    <span data-ttu-id="4a491-185">ข้อความว่าสำเร็จแล้ว (ใกล้กับมุมบนขวา) ช่วยให้คุณทราบว่าได้เพิ่มการแสดงภาพเป็นไทล์ลงในแดชบอร์ดของคุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="4a491-185">A success message (near the top-right corner) lets you know the visualization was added as a tile to your dashboard.</span></span>
   
    :::image type="content" source="media/service-get-started/power-bi-pin-success.png" alt-text="ภาพหน้าจอของกล่องโต้ตอบที่ปักหมุดไว้ที่แดชบอร์ด":::

    <span data-ttu-id="4a491-187">ตอนนี้คุณได้ตรึงการแสดงข้อมูลด้วยภาพนี้แล้ว ซึ่งถูกจัดเก็บไว้ในแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="4a491-187">Now that you've pinned this visualization, it's stored on your dashboard.</span></span> <span data-ttu-id="4a491-188">ข้อมูลจะยังคงเป็นปัจจุบันอยู่เสมอเพื่อให้คุณสามารถติดตามค่าล่าสุดได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="4a491-188">The data stays up-to-date so you can track the latest value at a glance.</span></span> <span data-ttu-id="4a491-189">อย่างไรก็ตาม ถ้าคุณเปลี่ยนประเภทการแสดงข้อมูลด้วยภาพในรายงาน การแสดงข้อมูลด้วยภาพบนแดชบอร์ดจะไม่เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="4a491-189">However, if you change the visualization type in the report, the visualization on the dashboard doesn't change.</span></span>

7. <span data-ttu-id="4a491-190">ให้เลือก **ไปยังแดชบอร์ด** เพื่อดูแดชบอร์ดใหม่ที่มีแผนภูมิเส้นที่คุณปักหมุดตามไทล์</span><span class="sxs-lookup"><span data-stu-id="4a491-190">Select **Go to dashboard** to see your new dashboard with the line chart that you pinned to it as a tile.</span></span> 
   
   :::image type="content" source="media/service-get-started/power-bi-service-dashboard-tile.png" alt-text="แดชบอร์ดที่มีการแสดงข้อมูลด้วยภาพถูกปักหมุดอยู่":::
   
8. <span data-ttu-id="4a491-192">เลือกไทล์ใหม่บนแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="4a491-192">Select the new tile on your dashboard.</span></span> <span data-ttu-id="4a491-193">Power BI นำคุณกลับสู่รายงานในมุมมองการอ่าน</span><span class="sxs-lookup"><span data-stu-id="4a491-193">Power BI returns you to the report in Reading view.</span></span>

1. <span data-ttu-id="4a491-194">เมื่อต้องการสลับกลับไปยังมุมมองการแก้ไข ให้เลือก **ตัวเลือกเพิ่มเติม** (...) ในแถบเมนู > **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="4a491-194">To switch back to Editing view, select **More options** (...) in the menu bar > **Edit**.</span></span>

    :::image type="content" source="media/service-get-started/power-bi-service-edit-report.png" alt-text="ภาพหน้าจอของเลือกแก้ไขเพื่อทำการแก้ไขรายงาน":::

    <span data-ttu-id="4a491-196">เมื่อกลับไปที่มุมมองการแก้ไข คุณสามารถทำการสำรวจและปักหมุดไทล์ได้ต่อไป</span><span class="sxs-lookup"><span data-stu-id="4a491-196">Back in Editing view, you can continue to explore and pin tiles.</span></span>

## <a name="step-3-explore-with-qa"></a><span data-ttu-id="4a491-197">ขั้นตอนที่ 3: สำรวจด้วยการถามตอบ</span><span class="sxs-lookup"><span data-stu-id="4a491-197">Step 3: Explore with Q&A</span></span>

<span data-ttu-id="4a491-198">หากต้องการสำรวจข้อมูลอย่างรวดเร็ว ลองถามคำถามในกล่องการถามตอบ</span><span class="sxs-lookup"><span data-stu-id="4a491-198">For a quick exploration of your data, try asking a question in the Q&A question box.</span></span> <span data-ttu-id="4a491-199">Q&A ช่วยให้คุณสามารถถามคิวรีได้ด้วยภาษาธรรมชาติเกี่ยวกับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="4a491-199">Q&A lets you ask natural-language queries about your data.</span></span> <span data-ttu-id="4a491-200">ในแดชบอร์ด กล่อง Q&A อยู่ที่ด้านบนสุด (**ถามคำถามเกี่ยวกับข้อมูลของคุณ**) ภายใต้แถบเมนู</span><span class="sxs-lookup"><span data-stu-id="4a491-200">In a dashboard, the Q&A box is at the top (**Ask a question about your data**) under the menu bar.</span></span> <span data-ttu-id="4a491-201">ในรายงาน กล่องนี้อยู่ที่แถบเมนูด้านบนสุด (**ถามคำถาม**)</span><span class="sxs-lookup"><span data-stu-id="4a491-201">In a report, it's in the top menu bar (**Ask a question**).</span></span>

1. <span data-ttu-id="4a491-202">ถ้าต้องการกลับไปยังแดชบอร์ด ให้เลือก **พื้นที่ทำงานของฉัน** ในแถบส่วนหัว **Power BI** สีดำ</span><span class="sxs-lookup"><span data-stu-id="4a491-202">To go back to the dashboard, select **My workspace** in the black **Power BI** header bar.</span></span>

    :::image type="content" source="media/service-get-started/power-bi-service-go-my-workspace.png" alt-text="ภาพหน้าจอของกลับไปยังพื้นที่ทำงานของฉัน":::

1. <span data-ttu-id="4a491-204">ใน **พื้นที่ทำงานของฉัน** ให้เลือกแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="4a491-204">In **My workspace**, select your dashboard.</span></span>

    :::image type="content" source="media/service-get-started/power-bi-service-dashboard-tab.png" alt-text="ภาพหน้าจอของเลือกแดชบอร์ดของคุณ":::

1. <span data-ttu-id="4a491-206">เลือก **ถามคำถามเกี่ยวกับข้อมูลของคุณ**</span><span class="sxs-lookup"><span data-stu-id="4a491-206">Select **Ask a question about your data**.</span></span> <span data-ttu-id="4a491-207">การถามตอบนำเสนอคำแนะนำจำนวนมากโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="4a491-207">Q&A automatically offers a number of suggestions.</span></span> 

    :::image type="content" source="media/service-get-started/power-bi-service-new-qanda.png" alt-text="ภาพหน้าจอของผืนผ้าใบ Q&A":::

    > [!NOTE]
    > <span data-ttu-id="4a491-209">หากคุณไม่เห็นคำแนะนำ ให้เปิดใช้งาน **ประสบการณ์การถามตอบใหม่**</span><span class="sxs-lookup"><span data-stu-id="4a491-209">If you don't see the suggestions, turn on **New Q&A experience**.</span></span>

    :::image type="content" source="media/service-get-started/power-bi-new-qna-experience.png" alt-text="ภาพหน้าจอของของการเปิดประสบการณ์ Q&A ใหม่":::

1. <span data-ttu-id="4a491-211">คำแนะนำบางอย่างจะเปลี่ยนกลับเป็นค่าเดียว</span><span class="sxs-lookup"><span data-stu-id="4a491-211">Some suggestions return a single value.</span></span> <span data-ttu-id="4a491-212">ตัวอย่างเช่น เลือก **ฟันเฟืองเฉลี่ยเป็นเท่าไร**</span><span class="sxs-lookup"><span data-stu-id="4a491-212">For example, select **what is the average cog**.</span></span>

    <span data-ttu-id="4a491-213">การถามตอบจะค้นหาคำตอบและแสดงในรูปแบบของการแสดงภาพ *การ์ด*</span><span class="sxs-lookup"><span data-stu-id="4a491-213">Q&A searches for an answer and presents it in the form of a *card* visualization.</span></span>

3. <span data-ttu-id="4a491-214">เลือก **ปักหมุดวิชวล** และปักหมุดการแสดงข้อมูลด้วยภาพนี้ไปยังแดชบอร์ดตัวอย่างทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="4a491-214">Select **Pin visual** and pin this visualization to the Financial Sample dashboard.</span></span>

    :::image type="content" source="media/service-get-started/power-bi-qna-pin-tile.png" alt-text="ภาพหน้าจอการปักหมุดวิชวล":::

1. <span data-ttu-id="4a491-216">กลับไปที่ Q&A และเลือก **แสดงคำแนะนำทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="4a491-216">Go back to Q&A and select **Show all suggestions**.</span></span>
1. <span data-ttu-id="4a491-217">เลือก **กำไรทั้งหมดตามประเทศ**</span><span class="sxs-lookup"><span data-stu-id="4a491-217">Select **total profit by country**.</span></span> 

    :::image type="content" source="media/service-get-started/power-bi-qna-total-profit-country.png" alt-text="ภาพหน้าจอของกำไรทั้งหมดตามประเทศ":::

1. <span data-ttu-id="4a491-219">ปักหมุดแผนผังไปยังแดชบอร์ดตัวอย่างทางการเงินด้วย</span><span class="sxs-lookup"><span data-stu-id="4a491-219">Pin the map to the Financial Sample dashboard, too.</span></span>

1. <span data-ttu-id="4a491-220">บนแดชบอร์ด ให้เลือกแผนที่คุณเพิ่งปักหมุด</span><span class="sxs-lookup"><span data-stu-id="4a491-220">On the dashboard, select the map you just pinned.</span></span> <span data-ttu-id="4a491-221">ดูว่าจะเปิด Q&A อีกครั้งได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="4a491-221">See how it opens Q&A again?</span></span> 
1. <span data-ttu-id="4a491-222">วางเคอร์เซอร์ด้านหลัง *ตามประเทศ* ในกล่องการถามตอบ และพิมพ์ *เป็นแท่ง*</span><span class="sxs-lookup"><span data-stu-id="4a491-222">Place the cursor after *by country* in the Q&A box and type *as bar*.</span></span> <span data-ttu-id="4a491-223">Power BI สร้างแผนภูมิแท่งพร้อมผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="4a491-223">Power BI creates a bar chart with the results.</span></span>

    :::image type="content" source="media/service-get-started/power-bi-qna-profit-country-bar.png" alt-text="ภาพหน้าจอของการแสดงข้อมูลด้วยภาพแผนภูมิแท่ง":::

1. <span data-ttu-id="4a491-225">ปักหมุดแผนภูมิแท่งไปยังแดชบอร์ดตัวอย่างทางการเงินด้วย</span><span class="sxs-lookup"><span data-stu-id="4a491-225">Pin the bar chart to your Financial Sample dashboard, too.</span></span>

4. <span data-ttu-id="4a491-226">เลือก **ออกจากการถามตอบ** เพื่อกลับไปยังแดชบอร์ดของคุณ ซึ่งคุณจะเห็นไทล์ใหม่ที่คุณสร้างไว้</span><span class="sxs-lookup"><span data-stu-id="4a491-226">Select **Exit Q&A** to return to your dashboard, where you see the new tiles you created.</span></span> 

   :::image type="content" source="media/service-get-started/power-bi-service-dashboard-qna.png" alt-text="ภาพหน้าจอของแดชบอร์ดที่มีวิชวล Q&A ปักหมุดอยู่":::

   <span data-ttu-id="4a491-228">แม้ว่าคุณจะเปลี่ยนแผนที่เป็นแผนภูมิแท่งใน Q&A แล้ว แต่ไทล์นั้นยังคงอยู่ในแผนที่เพราะเป็นแผนที่เมื่อคุณปักหมุด</span><span class="sxs-lookup"><span data-stu-id="4a491-228">You see that even though you changed the map to a bar chart in Q&A, that tile remained a map because it was a map when you pinned it.</span></span> 

## <a name="step-4-reposition-tiles"></a><span data-ttu-id="4a491-229">ขั้นตอนที่ 4: การจัดตำแหน่งไทล์ใหม่</span><span class="sxs-lookup"><span data-stu-id="4a491-229">Step 4: Reposition tiles</span></span>

<span data-ttu-id="4a491-230">เราสามารถจัดเรียงไทล์ใหม่เพื่อทำให้การใช้งานพื้นที่แดชบอร์ดดียิ่งขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="4a491-230">We can rearrange the tiles to make better use of the dashboard space.</span></span>

1. <span data-ttu-id="4a491-231">ลากมุมขวาล่างของไทล์แผนภูมิเส้น *ยอดขายรวม* ขึ้นไปด้านบน จนกว่าจะมีความสูงเท่ากับไทล์ยอดขาย จากนั้นจึงปล่อย</span><span class="sxs-lookup"><span data-stu-id="4a491-231">Drag the lower-right corner of the *Gross Sales* line chart tile upward, until it snaps at the same height as the Sales tile, then release it.</span></span>

    :::image type="content" source="media/service-get-started/power-bi-service-resize-tile.png" alt-text="ภาพหน้าจอของการปรับขนาดไทล์":::

    <span data-ttu-id="4a491-233">ในตอนนี้ ทั้งสองไทล์จึงมีความสูงเท่ากัน</span><span class="sxs-lookup"><span data-stu-id="4a491-233">Now the two tiles are the same height.</span></span>

1. <span data-ttu-id="4a491-234">เลือก **ตัวเลือกเพิ่มเติม (...)** สำหรับค่าเฉลี่ยของไทล์ COGS > **แก้ไขรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="4a491-234">Select **More options (...)** for the Average of COGS tile > **Edit details**.</span></span> 

    :::image type="content" source="media/service-get-started/power-bi-tile-edit-details.png" alt-text="ภาพหน้าจอของเมนูตัวเลือกเพิ่มเติมสำหรับไทล์":::

1. <span data-ttu-id="4a491-236">ในกล่อง **ชื่อ** ให้พิมพ์ *ต้นทุนเฉลี่ยของสินค้าที่ขาย* > **ใช้**</span><span class="sxs-lookup"><span data-stu-id="4a491-236">In the **Title** box, type *Average Cost of Goods Sold* > **Apply**.</span></span>

    :::image type="content" source="media/service-get-started/power-bi-tile-details-dialog.png" alt-text="ภาพหน้าจอของกล่องโต้ตอบแก้ไขรายละเอียด":::

1. <span data-ttu-id="4a491-238">จัดเรียงวิชวลอื่น ๆ ให้พอดีเข้าด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="4a491-238">Rearrange the other visuals to fit together.</span></span>

    <span data-ttu-id="4a491-239">การจัดตำแหน่งช่วยให้ดูดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="4a491-239">That looks better.</span></span>

    :::image type="content" source="media/service-get-started/power-bi-service-rearranged-dashboard.png" alt-text="ภาพหน้าจอของแดชบอร์ดที่ถูกจัดเรียง":::


## <a name="clean-up-resources"></a><span data-ttu-id="4a491-241">ล้างแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4a491-241">Clean up resources</span></span>
<span data-ttu-id="4a491-242">ในตอนนี้ คุณสำเร็จบทช่วยสอนแล้ว คุณสามารถลบชุดข้อมูล รายงานและแดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="4a491-242">Now that you've finished the tutorial, you can delete the dataset, report, and dashboard.</span></span> 

1. <span data-ttu-id="4a491-243">เลือก **พื้นที่ทำงานของฉัน** ในแถบส่วนหัว **Power BI** สีดำ</span><span class="sxs-lookup"><span data-stu-id="4a491-243">Select **My workspace** in the black **Power BI** header bar.</span></span>
2. <span data-ttu-id="4a491-244">เลือก **ตัวเลือกเพิ่มเติม (...)** ถัดจากชุดข้อมูลตัวอย่างทางการเงิน > **ลบ**</span><span class="sxs-lookup"><span data-stu-id="4a491-244">Select **More options (...)** next to the Financial Sample dataset > **Delete**.</span></span>

    :::image type="content" source="media/service-get-started/power-bi-service-delete-dataset.png" alt-text="ภาพหน้าจอของการลบชุดข้อมูล":::

    <span data-ttu-id="4a491-246">คุณจะเห็นคำเตือนว่า **รายงานทั้งหมดและแดชบอร์ดที่มีข้อมูลจากชุดข้อมูลจะถูกลบออกไป**</span><span class="sxs-lookup"><span data-stu-id="4a491-246">You see a warning that **All reports and dashboard tiles containing data from this dataset will also be deleted**.</span></span>

4. <span data-ttu-id="4a491-247">เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="4a491-247">Select **Delete**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4a491-248">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4a491-248">Next steps</span></span>

<span data-ttu-id="4a491-249">สำรวจคอลเลกชันของเนื้อหา Microsoft Learn เหล่านี้สำหรับ Power BI:</span><span class="sxs-lookup"><span data-stu-id="4a491-249">Explore these collections of Microsoft Learn content for Power BI:</span></span>

- [<span data-ttu-id="4a491-250">เรียนรู้เกี่ยวกับ Power BI</span><span class="sxs-lookup"><span data-stu-id="4a491-250">Learn Power BI</span></span>](/learn/powerplatform/power-bi?WT.mc_id=powerbi_landingpage-docs-link)
- [<span data-ttu-id="4a491-251">กลายเป็นนักวิเคราะห์ข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="4a491-251">Become a Power BI data analyst</span></span>](/users/microsoftpowerplatform-5978/collections/djwu3eywpk4nm)