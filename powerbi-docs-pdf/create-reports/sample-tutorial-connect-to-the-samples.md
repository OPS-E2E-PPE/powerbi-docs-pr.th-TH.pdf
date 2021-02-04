---
title: สำรวจตัวอย่างการวิเคราะห์ด้านการขายปลีก
description: เรียนรู้วิธีการติดตั้งและสำรวจตัวอย่างการวิเคราะห์ด้านการขายปลีกในบริการของ Power BI และใน Power BI Desktop
author: maggiesMSFT
ms.author: maggies
ms.reviewer: amac
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: conceptual
ms.date: 03/27/2020
LocalizationGroup: Samples
ms.openlocfilehash: 87296ca881550180ec62262def3aff44eead956b
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96395739"
---
# <a name="explore-the-retail-analysis-sample"></a><span data-ttu-id="d42cb-103">สำรวจตัวอย่างการวิเคราะห์ด้านการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="d42cb-103">Explore the Retail Analysis sample</span></span>

<span data-ttu-id="d42cb-104">บทช่วยสอนนี้สอนให้คุณรู้จักวิธี:</span><span class="sxs-lookup"><span data-stu-id="d42cb-104">This tutorial shows you how to:</span></span> 
- <span data-ttu-id="d42cb-105">นำเข้าชุดเนื้อหาตัวอย่าง เพิ่มไปยังบริการ Power BI และเปิดดูเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="d42cb-105">Import the Retail Analysis sample content pack, add it to the Power BI service, and open the contents.</span></span> <span data-ttu-id="d42cb-106">*ชุดเนื้อหา* คือตัวอย่างชนิดหนึ่ง ที่มีการรวมชุดข้อมูลกับแดชบอร์ดและรายงาน</span><span class="sxs-lookup"><span data-stu-id="d42cb-106">A *content pack* is a type of sample where the dataset is bundled with a dashboard and report.</span></span> 
- <span data-ttu-id="d42cb-107">เปิดไฟล์ .pbix ตัวอย่างการวิเคราะห์ด้านการขายปลีกใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d42cb-107">Open the Retail Analysis sample .pbix file in Power BI Desktop.</span></span>

<span data-ttu-id="d42cb-108">ถ้าคุณต้องการข้อมูลพื้นหลังเพิ่มเติม ดู [ตัวอย่างชุดข้อมูลสำหรับ Power BI](sample-datasets.md)</span><span class="sxs-lookup"><span data-stu-id="d42cb-108">If you'd like more background information, see [Sample datasets for Power BI](sample-datasets.md).</span></span> <span data-ttu-id="d42cb-109">ในบทความดังกล่าว คุณจะได้เรียนรู้เกี่ยวกับตัวอย่าง วิธีรับตัวอย่างเหล่านั้น พื้นที่ที่จะบันทึก วิธีการใช้งาน และเรื่องราวจากแต่ละตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="d42cb-109">In that article you'll learn all about the samples: how to get them, where to save them, how to use them, and some of the stories each sample can tell.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="d42cb-110">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="d42cb-110">Prerequisites</span></span>
<span data-ttu-id="d42cb-111">มีตัวอย่างให้สำหรับบริการ Power BI และ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d42cb-111">The samples are available for the Power BI service and Power BI Desktop.</span></span> <span data-ttu-id="d42cb-112">เรากำลังใช้ตัวอย่างการวิเคราะห์ด้านการขายปลีกถ้าคุณต้องการทำตาม</span><span class="sxs-lookup"><span data-stu-id="d42cb-112">We're using the Retail analysis sample, if you want to follow along.</span></span>

<span data-ttu-id="d42cb-113">ชุดเนื้อหาตัวอย่างการ *วิเคราะห์ด้านการขายปลีก* ที่ใช้ในบทช่วยสอนนี้ประกอบด้วยแดชบอร์ด รายงาน และชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d42cb-113">The *Retail Analysis* sample content pack used in this tutorial consists of a dashboard, report, and dataset.</span></span>
<span data-ttu-id="d42cb-114">ทำความคุ้นเคยกับชุดเนื้อหานี้ และสถานการณ์ คุณอาจต้องการชม [ตัวอย่างการวิเคราะห์ด้านการขายปลีกสำหรับ Power BI: ชมการแนะนำ ](sample-retail-analysis.md) ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d42cb-114">To familiarize yourself with this particular content pack and its scenario, see [Retail Analysis sample for Power BI: Take a tour](sample-retail-analysis.md) before you begin.</span></span>

## <a name="import-the-sample-in-the-power-bi-service"></a><span data-ttu-id="d42cb-115">นำเข้าตัวอย่างในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="d42cb-115">Import the sample in the Power BI service</span></span>

1. <span data-ttu-id="d42cb-116">เปิดบริการ Power BI (app.powerbi.com) ลงชื่อเข้าใช้ และเปิดพื้นที่ทำงานที่คุณต้องการบันทึกตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="d42cb-116">Open the Power BI service (app.powerbi.com), sign in, and open the workspace where you want to save the sample.</span></span> 

    <span data-ttu-id="d42cb-117">ถ้าคุณไม่มีสิทธิการใช้งาน Power BI Pro คุณสามารถบันทึกตัวอย่างไปยังพื้นที่ทำงานของฉัน</span><span class="sxs-lookup"><span data-stu-id="d42cb-117">If you don't have a Power BI Pro license, you can save the sample to your My Workspace.</span></span>

2. <span data-ttu-id="d42cb-118">เลือก **รับข้อมูล** ที่ด้านล่างของบานหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="d42cb-118">Select **Get Data** at the bottom of the nav pane.</span></span> 

   ![เลือกรับข้อมูล](media/sample-datasets/power-bi-get-data.png)

   <span data-ttu-id="d42cb-120">ถ้าคุณไม่เห็น **รับข้อมูล** ให้ขยายบานหน้าต่างนำทางโดยการเลือกไอคอนต่อไปนี้ที่ด้านบนของบานหน้าต่าง: ![ไอคอนแฮมเบอร์เกอร์](media/sample-tutorial-connect-to-the-samples/expand-nav.png)</span><span class="sxs-lookup"><span data-stu-id="d42cb-120">If you don't see **Get Data**, expand the nav pane by selecting the following icon at the top of the pane: ![hamburger icon](media/sample-tutorial-connect-to-the-samples/expand-nav.png).</span></span>

5. <span data-ttu-id="d42cb-121">บนหน้า **รับข้อมูล** ที่ปรากฏขึ้น เลือก **ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="d42cb-121">On the **Get Data** page that appears, select **Samples**.</span></span>
   
6. <span data-ttu-id="d42cb-122">เลือก **ตัวอย่างการวิเคราะห์ด้านการขายปลีก** และเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="d42cb-122">Select **Retail Analysis Sample**, and then choose **Connect**.</span></span>   
   
   ![ปุ่มเชื่อมต่อ](media/sample-tutorial-connect-to-the-samples/pbi_retailanalysissampleconnect.png)

## <a name="what-was-imported"></a><span data-ttu-id="d42cb-124">มีการนำเข้าอะไรบ้าง</span><span class="sxs-lookup"><span data-stu-id="d42cb-124">What was imported?</span></span>
<span data-ttu-id="d42cb-125">ด้วยตัวอย่างชุดเนื้อหา เมื่อคุณเลือก **เชื่อมต่อ** แล้ว Power BI จะนำสำเนาของชุดเนื้อหานั้น มาเก็บไว้ให้คุณในคลาวด์</span><span class="sxs-lookup"><span data-stu-id="d42cb-125">With the sample content packs, when you select **Connect**, Power BI gets a copy of that content pack and stores it for you in the cloud.</span></span> <span data-ttu-id="d42cb-126">เนื่องจากบุคคลที่สร้างชุดเนื้อหา รวมชุดข้อมูล รายงาน และแดชบอร์ดไว้ นั่นคือสิ่งที่คุณจะได้รับเมื่อคุณคลิก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="d42cb-126">Because the person who created the content pack included a dataset, a report, and a dashboard, that's what you get when you select **Connect**.</span></span> 

1. <span data-ttu-id="d42cb-127">เมื่อคุณเลือก **เชื่อมต่อ** Power BI จะสร้างแดชบอร์ดใหม่ และแสดงรายการในแท็บ **แดชบอร์ด** ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d42cb-127">When you select **Connect**, Power BI creates the new dashboard and lists it on your **Dashboards** tab.</span></span> 
   
   ![รายการตัวอย่างการวิเคราะห์การค้าปลีก](media/sample-retail-analysis/retail-entry.png)
2. <span data-ttu-id="d42cb-129">เปิดแท็บ **รายงาน** ที่นี่คุณจะเห็นรายงานใหม่ที่มีชื่อ *ตัวอย่างการวิเคราะห์ด้านการขายปลีก*</span><span class="sxs-lookup"><span data-stu-id="d42cb-129">Open the **Reports** tab. Here, you'll see a new report named *Retail Analysis Sample*.</span></span>
   
   ![ป้อนรายงานตัวอย่างการวิเคราะห์ร้านค้าปลีก](media/sample-tutorial-connect-to-the-samples/power-bi-new-report.png)
   
   <span data-ttu-id="d42cb-131">ตรวจสอบแท็บ **ชุดข้อมูล** ซึ่งจะมีชุดข้อมูลใหม่อยู่ที่นั่นด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="d42cb-131">Check out the **Datasets** tab; there's a new dataset there as well.</span></span>
   
   ![ป้อนชุดข้อมูลตัวอย่างการวิเคราะห์การค้าปลีก](media/sample-tutorial-connect-to-the-samples/power-bi-new-dataset.png)

## <a name="explore-your-new-content"></a><span data-ttu-id="d42cb-133">สำรวจเนื้อหาใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d42cb-133">Explore your new content</span></span>
<span data-ttu-id="d42cb-134">ตอนนี้ ลองสำรวจแดชบอร์ด ชุดข้อมูล และรายงานด้วยตัวคุณเอง</span><span class="sxs-lookup"><span data-stu-id="d42cb-134">Now explore the dashboard, dataset, and report on your own.</span></span> <span data-ttu-id="d42cb-135">ระบบจะนำทางไปยังแดชบอร์ด รายงาน และชุดข้อมูลของคุณได้หลายวิธี</span><span class="sxs-lookup"><span data-stu-id="d42cb-135">There are many different ways to navigate to your dashboards, reports, and datasets.</span></span> <span data-ttu-id="d42cb-136">หนึ่งในวิธีเหล่านี้จะอธิบายไว้ในขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d42cb-136">One of these ways is described in the following procedure.</span></span>  

1. <span data-ttu-id="d42cb-137">ย้อนกลับไปยังแท็บ **แดชบอร์ด** จากนั้นเลือกแดชบอร์ด **ตัวอย่างการวิเคราะห์ด้านการขายปลีก** เพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="d42cb-137">Navigate back to the **Dashboards** tab, and then select the **Retail Analysis Sample** dashboard to open it.</span></span>       

   <span data-ttu-id="d42cb-138">แดชบอร์ดจะเปิดขึ้นซึ่งมีไทล์การแสดงภาพที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="d42cb-138">The dashboard opens, which has a variety of visualization tiles.</span></span>   
 
1. <span data-ttu-id="d42cb-139">เลือกไทล์หนึ่งในนั้นเพื่อเปิดรายงานพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="d42cb-139">Select one of the tiles in the dashboard to open the underlying report.</span></span> <span data-ttu-id="d42cb-140">ในตัวอย่างนี้เราจะเลือกแผนภูมิพื้นที่ **ยอดขายของปีนี้ ยอดขายของปีที่แล้วตามเดือนทางบัญชี**</span><span class="sxs-lookup"><span data-stu-id="d42cb-140">In this example, we'll select the area chart, **This Year's Sales, Last Year's Sales by Fiscal Month**.</span></span>  

   ![แดชบอร์ดตัวอย่างการวิเคราะห์ร้านค้าปลีกกับพร้อมการไฮไลท์การแสดงผลด้วยภาพ](media/sample-tutorial-connect-to-the-samples/power-bi-dashboards2new.png)

   <span data-ttu-id="d42cb-142">รายงานจะเปิดไปยังหน้าที่มีแผนภูมิพื้นที่ที่คุณเลือก ในกรณีนี้คือ หน้ารายงาน **ยอดขายรายเดือนของเขต**</span><span class="sxs-lookup"><span data-stu-id="d42cb-142">The report opens to the page that contains the area chart you selected; in this case, the **District Monthly Sales** page of the report.</span></span>
   
   ![หน้ารายงานยอดขายรายเดือนของเขต](media/sample-tutorial-connect-to-the-samples/power-bi-report.png)
   
   > [!NOTE]
   > <span data-ttu-id="d42cb-144">ถ้าไทล์ถูกสร้างขึ้นโดยใช้ [ถามตอบ Power BI](power-bi-tutorial-q-and-a.md) หน้าถามตอบจะเปิดขึ้นแทน</span><span class="sxs-lookup"><span data-stu-id="d42cb-144">If the tile was created by using [Power BI Q&A](power-bi-tutorial-q-and-a.md), the Q&A page will open instead.</span></span> <span data-ttu-id="d42cb-145">ถ้าไทล์เป็นการ [ปักหมุดจาก Excel](service-dashboard-pin-tile-from-excel.md) จะเปิด Excel Online ขึ้นภายใน Power BI</span><span class="sxs-lookup"><span data-stu-id="d42cb-145">If the tile was [pinned from Excel](service-dashboard-pin-tile-from-excel.md), Excel Online will open inside of Power BI.</span></span>
   > 
   > 
1. <span data-ttu-id="d42cb-146">เมื่อมีบางคนแชร์ชุดเนื้อหากับเพื่อนร่วมงาน พวกเขามักต้องการแชร์ข้อมูลเชิงลึก ไม่ได้ให้เพื่อนร่วมงานของพวกเขาเข้าถึงข้อมูลโดยตรง</span><span class="sxs-lookup"><span data-stu-id="d42cb-146">When someone shares a content pack with colleagues, they typically want to share only the insights, rather than provide direct access to the data.</span></span> <span data-ttu-id="d42cb-147">กลับไปที่แท็บ **ชุดข้อมูล** ของคุณ คุณมีหลายตัวเลือกในการสำรวจชุดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="d42cb-147">On the **Datasets** tab, you have several options for exploring your dataset.</span></span> <span data-ttu-id="d42cb-148">อย่างไรก็ตามคุณไม่สามารถดูแถวและคอลัมน์ของข้อมูลของคุณได้เช่นเดียวกับที่คุณสามารถทำได้ใน Power BI Desktop หรือ Excel</span><span class="sxs-lookup"><span data-stu-id="d42cb-148">However, you can't view the rows and columns of your data, as you can in Power BI Desktop or Excel.</span></span> 
   
   ![ป้อนชุดข้อมูลตัวอย่างการวิเคราะห์การค้าปลีก](media/sample-tutorial-connect-to-the-samples/power-bi-new-dataset.png)
   
1. <span data-ttu-id="d42cb-150">วิธีหนึ่งในการสำรวจชุดข้อมูล ก็โดยการสร้างการแสดงภาพและรายงานของคุณเองตั้งแต่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d42cb-150">One way of exploring the dataset is by creating your own visualizations and reports from scratch.</span></span> <span data-ttu-id="d42cb-151">เลือกไอคอนแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="d42cb-151">Select the chart icon</span></span> ![ไอคอนแผนภูมิ](media/sample-tutorial-connect-to-the-samples/power-bi-chart-icon4.png) <span data-ttu-id="d42cb-153">เพื่อเปิดชุดข้อมูลในโหมดการแก้ไขรายงาน</span><span class="sxs-lookup"><span data-stu-id="d42cb-153">to open the dataset in report editing mode.</span></span>
     
   ![สร้างรายงานใหม่](media/sample-tutorial-connect-to-the-samples/power-bi-report-editing.png)

1. <span data-ttu-id="d42cb-155">อีกวิธีหนึ่งในการสำรวจชุดข้อมูล คือการเรียกใช้ [ข้อมูลเชิงลึกด่วน](../consumer/end-user-insights.md)</span><span class="sxs-lookup"><span data-stu-id="d42cb-155">Another way of exploring the dataset is to run [quick insights](../consumer/end-user-insights.md).</span></span> <span data-ttu-id="d42cb-156">เลือก **ตัวเลือกเพิ่มเติม** (...) แล้วเลือก **รับข้อมูลเชิงลึกด่วน**</span><span class="sxs-lookup"><span data-stu-id="d42cb-156">Select **More options** (...), and then choose **Get quick insights**.</span></span> <span data-ttu-id="d42cb-157">เมื่อข้อมูลเชิงลึกพร้อมแล้ว เลือก **ดูข้อมูลเชิงลึก**</span><span class="sxs-lookup"><span data-stu-id="d42cb-157">When the insights are ready, select **View insights**.</span></span>
     
    ![รายงานข้อมูลเชิงลึก](media/sample-tutorial-connect-to-the-samples/power-bi-insights.png)

## <a name="download-the-sample-in-power-bi-desktop"></a><span data-ttu-id="d42cb-159">ดาวน์โหลดตัวอย่างใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d42cb-159">Download the sample in Power BI Desktop</span></span> 
<span data-ttu-id="d42cb-160">เมื่อคุณเริ่มเปิดไฟล์ .pbix ตัวอย่าง ใน Power BI Desktop จะแสดงในมุมมองรายงาน ที่คุณสามารถสำรวจ สร้าง และปรับเปลี่ยนตัวเลขใด ๆ ของหน้ารายงานที่มีการแสดงผลเป็นภาพ</span><span class="sxs-lookup"><span data-stu-id="d42cb-160">When you first open the sample .pbix file in Power BI Desktop, it displays in Report view where you can explore, create, and modify any number of report pages with visualizations.</span></span> <span data-ttu-id="d42cb-161">มุมมองรายงาน ออกแบบให้ได้ประสบการณ์แบบเดียวกับ มุมมองการแก้ไขรายงาน ในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="d42cb-161">Report view provides almost the same design experience as a report's Editing view in the Power BI service.</span></span> <span data-ttu-id="d42cb-162">คุณสามารถย้ายการแสดงภาพไปรอบ ๆ คัดลอกและวาง ผสาน และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="d42cb-162">You can move visualizations around, copy and paste, merge, and so on.</span></span> 

<span data-ttu-id="d42cb-163">ซึ่งต่างจากการแก้ไขในบริการ Power BI ใน Power BI Desktop คุณสามารถทำงานกับคิวรีของคุณ และสร้างแบบจำลองข้อมูลของคุณ เพื่อให้แน่ใจว่า ข้อมูลรองรับข้อมูลเชิงลึกที่ดีที่สุดในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="d42cb-163">Unlike editing a report in the Power BI service, in Power BI Desktop you can also work with your queries and model your data to ensure your data supports the best insights in your reports.</span></span> <span data-ttu-id="d42cb-164">จากนั้นคุณสามารถบันทึกไฟล์ Power BI Desktop ของคุณเมื่อใดก็ตามที่คุณต้องการ ไม่ว่าจะบันทึกลงไดรฟ์ในเครื่อง หรือคลาวด์</span><span class="sxs-lookup"><span data-stu-id="d42cb-164">You can then save your Power BI Desktop file wherever you like, whether it's to your local drive or to the cloud.</span></span>

1. <span data-ttu-id="d42cb-165">ดาวน์โหลดไฟล์ [Retail Analysis sample .pbix](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix) แล้วเปิดใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d42cb-165">Download the [Retail Analysis sample .pbix file](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix) and open it in Power BI Desktop.</span></span> 

    ![ตัวอย่างในมุมมองรายงาน Power BI](media/sample-tutorial-connect-to-the-samples/power-bi-samples-desktop.png)

1. <span data-ttu-id="d42cb-167">ไฟล์เปิดขึ้นในมุมมองรายงาน</span><span class="sxs-lookup"><span data-stu-id="d42cb-167">The file opens in Report view.</span></span> <span data-ttu-id="d42cb-168">สังเกตเห็นสี่แท็บที่ด้านล่างของตัวแก้ไขรายงาน แท็บเหล่านี้แสดงสี่หน้าในรายงานนี้</span><span class="sxs-lookup"><span data-stu-id="d42cb-168">Notice the four tabs at the bottom of the report editor; these tabs represent the four pages in this report.</span></span> <span data-ttu-id="d42cb-169">สำหรับตัวอย่างนี้ หน้า **ร้านค้าใหม่** ่ถูกเลือกอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="d42cb-169">For this example, the **New Stores** page is currently selected.</span></span> 

    ![ไอไลท์แท็บชุดข้อมูลใหม่](media/sample-tutorial-connect-to-the-samples/power-bi-sample-tabs.png)<span data-ttu-id="d42cb-171">.</span><span class="sxs-lookup"><span data-stu-id="d42cb-171">.</span></span>

1. <span data-ttu-id="d42cb-172">สำหรับการเจาะลึกลงในตัวแก้ไขรายงาน ดู[ชมการแนะนำของตัวแก้ไขรายงาน](service-the-report-editor-take-a-tour.md)</span><span class="sxs-lookup"><span data-stu-id="d42cb-172">For a deep dive into the report editor, see [Take a tour of the report editor](service-the-report-editor-take-a-tour.md).</span></span>

## <a name="whats-in-your-report"></a><span data-ttu-id="d42cb-173">ในรายงานของคุณมีอะไร</span><span class="sxs-lookup"><span data-stu-id="d42cb-173">What's in your report?</span></span>
<span data-ttu-id="d42cb-174">เมื่อคุณดาวน์โหลดไฟล์ตัวอย่าง .pbix คุณไม่ได้ดาวน์โหลดเพียงรายงาน แต่ยังมี *ชุดข้อมูลพื้นฐาน*</span><span class="sxs-lookup"><span data-stu-id="d42cb-174">When you download a sample .pbix file, you've downloaded not just a report but also the *underlying dataset*.</span></span> <span data-ttu-id="d42cb-175">เมื่อคุณเปิดไฟล์ Power BI Desktop โหลดข้อมูลด้วยข้อซักถามและความสัมพันธ์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="d42cb-175">When you open the file, Power BI Desktop loads the data with its associated queries and relationships.</span></span> <span data-ttu-id="d42cb-176">คุณสามารถดูข้อมูลพื้นฐานและความสัมพันธ์ แต่คุณไม่สามารถดูข้อซักถามที่ซ่อนอยู่ในตัวแก้ไขข้อซักถาม</span><span class="sxs-lookup"><span data-stu-id="d42cb-176">You can view the underlying data and relationships, but you can't view the underlying queries in the Query Editor.</span></span>


1. <span data-ttu-id="d42cb-177">สลับไปยัง [มุมมองข้อมูล](../connect-data/desktop-data-view.md) โดยการเลือกไอคอนตาราง ![ไอคอนตาราง](media/sample-tutorial-connect-to-the-samples/power-bi-data-icon.png)</span><span class="sxs-lookup"><span data-stu-id="d42cb-177">Switch to [Data view](../connect-data/desktop-data-view.md) by selecting the table icon ![table icon](media/sample-tutorial-connect-to-the-samples/power-bi-data-icon.png).</span></span>
 
    ![มุมมองข้อมูล Desktop](media/sample-tutorial-connect-to-the-samples/power-bi-desktop-sample-data.png)

    <span data-ttu-id="d42cb-179">มุมมองข้อมูลช่วยให้คุณตรวจสอบ สำรวจ และทำความเข้าใจข้อมูลในแบบจำลอง Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d42cb-179">In Data view, you can inspect, explore, and understand data in your Power BI Desktop model.</span></span> <span data-ttu-id="d42cb-180">ซึ่งจะแตกต่างจากวิธีที่คุณดูตาราง คอลัมน์ และข้อมูลในตัวแก้ไขแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="d42cb-180">It's different from how you view tables, columns, and data in the Query Editor.</span></span> <span data-ttu-id="d42cb-181">ข้อมูลในมุมมองข้อมูลถูกโหลดลงในแบบจำลองแล้ว</span><span class="sxs-lookup"><span data-stu-id="d42cb-181">The data in Data view is already loaded into the model.</span></span>

    <span data-ttu-id="d42cb-182">เมื่อคุณทำแบบจำลองข้อมูลของคุณ บางครั้งคุณอาจต้องการดูว่ามีอะไรอยู่ในแถวหรือคอลัมน์ของตาราง โดยไม่ต้องสร้างภาพบนพื้นที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="d42cb-182">When you're modeling your data, sometimes you want to see what's actually in the rows and columns of a table, without creating a visual on the report canvas.</span></span> <span data-ttu-id="d42cb-183">โดยเฉพาะอย่างยิ่งเมื่อคุณกำลังจะสร้างการวัดและคอลัมน์จากการคำนวณ หรือคุณจำเป็นต้องระบุชนิดข้อมูลหรือประเภทข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d42cb-183">This is especially true when you're creating measures and calculated columns, or you need to identify a data type or data category.</span></span>

1. <span data-ttu-id="d42cb-184">สลับไปยัง[มุมมองความสัมพันธ์](../transform-model/desktop-relationship-view.md) โดยการเลือกไอคอนต่อไปนี้: ![ไอคอนมุมมองความสัมพันธ์](media/sample-tutorial-connect-to-the-samples/power-bi-desktop-relationship-icon.png)</span><span class="sxs-lookup"><span data-stu-id="d42cb-184">Switch to [Relationships view](../transform-model/desktop-relationship-view.md) by selecting the following icon: ![Relationship view icon](media/sample-tutorial-connect-to-the-samples/power-bi-desktop-relationship-icon.png).</span></span>
 
    ![มุมมองความสัมพันธ์ใน Power BI Desktop](media/sample-tutorial-connect-to-the-samples/power-bi-relationships.png)

    <span data-ttu-id="d42cb-186">มุมมองความสัมพันธ์ แสดงตาราง คอลัมน์ และความสัมพันธ์ทั้งหมดในรูปแบบข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="d42cb-186">Relationship view shows all of the tables, columns, and relationships in your model.</span></span> <span data-ttu-id="d42cb-187">จากที่นี่ คุณสามารถดู เปลี่ยน และสร้างความสัมพันธ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="d42cb-187">From here you can view, change, and create relationships.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d42cb-188">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d42cb-188">Next steps</span></span>
<span data-ttu-id="d42cb-189">สภาพแวดล้อมนี้มีความปลอดภัยให้ดำเนินการต่าง ๆ ได้ เนื่องจากคุณสามารถเลือกที่จะไม่บันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="d42cb-189">This environment is a safe one to play in, because you can choose not to save your changes.</span></span> <span data-ttu-id="d42cb-190">ถ้าคุณบันทึก คุณสามารถเลือก **รับข้อมูล** สำหรับสำเนาชุดใหม่ของตัวอย่างนี้ได้เสมอ</span><span class="sxs-lookup"><span data-stu-id="d42cb-190">But if you do save them, you can always select **Get Data** for a new copy of this sample.</span></span>

<span data-ttu-id="d42cb-191">เราหวังว่าการแนะนำนี้ได้แสดงให้เห็นว่าแดชบอร์ด Power BI ชุดข้อมูล ความสัมพันธ์ และรายงาน สามารถให้ข้อมูลเชิงลึกในข้อมูลตัวอย่างได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="d42cb-191">We hope this tour has shown how Power BI dashboards, datasets, relationships, and reports can provide insights into sample data.</span></span> <span data-ttu-id="d42cb-192">ตอนนี้ถึงตาคุณแล้ว ลองเชื่อมต่อกับข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="d42cb-192">Now it's your turn; connect to your own data.</span></span> <span data-ttu-id="d42cb-193">ด้วย Power BI คุณสามารถเชื่อมต่อกับแหล่งข้อมูลที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="d42cb-193">With Power BI, you can connect to a wide variety of data sources.</span></span> <span data-ttu-id="d42cb-194">หากต้องการเรียนรู้เพิ่มเติม ดู [เริ่มต้นด้วยบริการของ Power BI](../fundamentals/service-get-started.md) และ [เริ่มต้นด้วย Power BI Desktop](../fundamentals/desktop-getting-started.md)</span><span class="sxs-lookup"><span data-stu-id="d42cb-194">To learn more, see [Get started with the Power BI service](../fundamentals/service-get-started.md) and [Get started with Power BI Desktop](../fundamentals/desktop-getting-started.md).</span></span>  

<span data-ttu-id="d42cb-195">สำหรับข้อมูลเพิ่มเติม ให้ด:</span><span class="sxs-lookup"><span data-stu-id="d42cb-195">For more information, see:</span></span>  
- [<span data-ttu-id="d42cb-196">แนวคิดพื้นฐานสำหรับนักออกแบบในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="d42cb-196">Basic concepts for designers in the Power BI service</span></span>](../fundamentals/service-basic-concepts.md)
- [<span data-ttu-id="d42cb-197">ตัวอย่างสำหรับบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="d42cb-197">Samples for the Power BI service</span></span>](sample-datasets.md)
- [<span data-ttu-id="d42cb-198">แหล่งข้อมูลสำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="d42cb-198">Data sources for Power BI</span></span>](../connect-data/service-get-data.md)

<span data-ttu-id="d42cb-199">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d42cb-199">More questions?</span></span> [<span data-ttu-id="d42cb-200">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="d42cb-200">Try the Power BI Community</span></span>](https://community.powerbi.com/)
