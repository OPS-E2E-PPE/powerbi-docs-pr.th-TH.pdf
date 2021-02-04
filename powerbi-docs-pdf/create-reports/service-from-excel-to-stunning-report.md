---
title: 'บทช่วยสอน: จากสมุดงาน Excel ไปยังบริการของ Power BI และต่อไปยัง Teams'
description: บทความนี้แสดงให้เห็นว่าคุณสามารถสร้างรายงานที่ ยอดเยี่ยมในบริการของ Power BI จากสมุดงาน Excel อย่างรวดเร็วและแชร์รายงานใน Teams ได้อย่างไร
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: tutorial
ms.date: 12/14/2020
LocalizationGroup: Data from files
ms.openlocfilehash: a3ee3ac5cd23942878395f942a32dbe573cb0798
ms.sourcegitcommit: 0711972326521944fdd8572403c0b15f31b916da
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/22/2020
ms.locfileid: "97721604"
---
# <a name="tutorial-from-excel-workbook-to-a-report-in-the-power-bi-service-to-microsoft-teams"></a><span data-ttu-id="0d0a9-103">บทช่วยสอน: จากสมุดงาน Excel ไปยังรายงานในบริการของ Power BI และต่อไปยัง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0d0a9-103">Tutorial: From Excel workbook to a report in the Power BI service to Microsoft Teams</span></span>
<span data-ttu-id="0d0a9-104">ผู้จัดการของคุณต้องการดูรายงานเกี่ยวกับยอดขายล่าสุดและตัวเลขกำไรของคุณภายในเย็นวันนี้</span><span class="sxs-lookup"><span data-stu-id="0d0a9-104">Your manager wants to see a report on your latest sales and profit figures by the end of the day.</span></span> <span data-ttu-id="0d0a9-105">แต่ข้อมูลล่าสุดอยู่ในไฟล์บนแล็ปท็อปของคุณ</span><span class="sxs-lookup"><span data-stu-id="0d0a9-105">But the latest data is in files on your laptop.</span></span> <span data-ttu-id="0d0a9-106">ในอดีตต้องใช้เวลาหลายชั่วโมงในการสร้างรายงานและคุณเริ่มรู้สึกตื่นตระหนก</span><span class="sxs-lookup"><span data-stu-id="0d0a9-106">In the past, it’s taken hours to create a report, and you’re beginning to feel anxious.</span></span>

<span data-ttu-id="0d0a9-107">ไม่ต้องกังวล</span><span class="sxs-lookup"><span data-stu-id="0d0a9-107">No worries.</span></span> <span data-ttu-id="0d0a9-108">ด้วย Power BI คุณสามารถสร้างรายงานที่สวยงามและแชร์รายงานใน Microsoft Teams ได้ในเวลาไม่นาน</span><span class="sxs-lookup"><span data-stu-id="0d0a9-108">With Power BI, you can create a stunning report and share it in Microsoft Teams in no time!</span></span>

:::image type="content" source="media/service-from-excel-to-stunning-report/power-bi-financial-report-service.png" alt-text="ภาพหน้าจอของรายงานตัวอย่างด้านการเงินที่เสร็จเรียบร้อยแล้ว":::

<span data-ttu-id="0d0a9-110">ในบทช่วยสอนนี้ เราจะอัปโหลดไฟล์ Excel สร้างรายงานใหม่ และแชร์กับเพื่อนร่วมงานใน Microsoft Teams ซึ่งทั้งหมดนี้ทำได้ภายใน Power BI</span><span class="sxs-lookup"><span data-stu-id="0d0a9-110">In this tutorial, we upload an Excel file, create a new report, and share it with colleagues in Microsoft Teams, all from within Power BI.</span></span> <span data-ttu-id="0d0a9-111">คุณจะได้เรียนรู้วิธีการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0d0a9-111">You'll learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="0d0a9-112">จัดเตรียมข้อมูลของคุณใน Excel</span><span class="sxs-lookup"><span data-stu-id="0d0a9-112">Prepare your data in Excel.</span></span>
> * <span data-ttu-id="0d0a9-113">ดาวน์โหลดข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="0d0a9-113">Download sample data.</span></span>
> * <span data-ttu-id="0d0a9-114">สร้างรายงานในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="0d0a9-114">Build a report in the Power BI service.</span></span>
> * <span data-ttu-id="0d0a9-115">ปักหมุดวิชวลรายงานไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="0d0a9-115">Pin the report visuals to a dashboard.</span></span>
> * <span data-ttu-id="0d0a9-116">แชร์ลิงก์ไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="0d0a9-116">Share a link to the dashboard.</span></span>
> * <span data-ttu-id="0d0a9-117">แชร์แดชบอร์ดใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0d0a9-117">Share the dashboard in Microsoft Teams</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0d0a9-118">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="0d0a9-118">Prerequisites</span></span>
- <span data-ttu-id="0d0a9-119">[ลงทะเบียนสำหรับบริการของ Power BI](../fundamentals/service-self-service-signup-for-power-bi.md)</span><span class="sxs-lookup"><span data-stu-id="0d0a9-119">[Sign up for the Power BI service](../fundamentals/service-self-service-signup-for-power-bi.md).</span></span> 
- <span data-ttu-id="0d0a9-120">ดาวน์โหลด [สมุดงานตัวอย่างด้านการเงิน](https://go.microsoft.com/fwlink/?LinkID=521962) และบันทึกลงในคอมพิวเตอร์ของคุณหรือลงใน OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="0d0a9-120">Download the [Financial Sample workbook](https://go.microsoft.com/fwlink/?LinkID=521962) and save it your computer or to OneDrive for Business.</span></span>


## <a name="prepare-data-in-excel"></a><span data-ttu-id="0d0a9-121">จัดเตรียมข้อมูลใน Excel</span><span class="sxs-lookup"><span data-stu-id="0d0a9-121">Prepare data in Excel</span></span>
<span data-ttu-id="0d0a9-122">เราใช้ไฟล์ Excel ง่าย ๆ เพื่อแสดงเป็นตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="0d0a9-122">Let’s take a simple Excel file as an example.</span></span> 

1. <span data-ttu-id="0d0a9-123">ก่อนที่คุณสามารถโหลดไฟล์ Excel ของคุณลงใน Power BI คุณต้องจัดระเบียบข้อมูลของคุณในตารางเดียวก่อน</span><span class="sxs-lookup"><span data-stu-id="0d0a9-123">Before you can load your Excel file into Power BI, you must organize your data in a flat table.</span></span> <span data-ttu-id="0d0a9-124">ในตารางแบบคงที่ แต่ละคอลัมน์ประกอบด้วยข้อมูลประเภทเดียวกัน ตัวอย่างเช่น ข้อความ วันที่ ตัวเลข หรือสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="0d0a9-124">In a flat table, each column contains the same data type; for example, text, date, number, or currency.</span></span> <span data-ttu-id="0d0a9-125">ตารางของคุณควรมีแถวส่วนหัว แต่ไม่มีคอลัมน์หรือแถวที่แสดงผลรวม</span><span class="sxs-lookup"><span data-stu-id="0d0a9-125">Your table should have a header row, but not any columns or rows that display totals.</span></span>

   ![ภาพหน้าจอของข้อมูลที่มีการจัดระเบียบใน Excel](media/service-from-excel-to-stunning-report/pbi_excel_file.png)

2. <span data-ttu-id="0d0a9-127">ถัดไป จัดรูปแบบข้อมูลของคุณเป็นหนึ่งตาราง</span><span class="sxs-lookup"><span data-stu-id="0d0a9-127">Next, format your data as a table.</span></span> <span data-ttu-id="0d0a9-128">ใน Excel ที่แถบ **หน้าแรก** ในกลุ่ม **สไตล์** เลือก **จัดรูปแบบเป็นตาราง**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-128">In Excel, on the **Home** tab, in the **Styles** group, select **Format as Table**.</span></span> 

3. <span data-ttu-id="0d0a9-129">เลือกลักษณะตารางที่จะนำไปใช้กับแผ่นงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="0d0a9-129">Select a table style to apply to your worksheet.</span></span> 

   <span data-ttu-id="0d0a9-130">ขณะนี้แผ่นงาน Excel ของคุณพร้อมที่จะโหลดลงใน Power BI</span><span class="sxs-lookup"><span data-stu-id="0d0a9-130">Your Excel worksheet is now ready to load into Power BI.</span></span>

   ![ภาพหน้าจอของข้อมูลที่จัดรูปแบบเป็นตาราง](media/service-from-excel-to-stunning-report/pbi_excel_table.png)

## <a name="upload-your-excel-file-to-the-power-bi-service"></a><span data-ttu-id="0d0a9-132">อัปโหลดไฟล์ Excel ของคุณไปยังบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="0d0a9-132">Upload your Excel file to the Power BI service</span></span>
<span data-ttu-id="0d0a9-133">บริการ Power BI เชื่อมต่อกับแหล่งข้อมูลจำนวนมาก รวมถึงไฟล์ Excel ที่อยู่บนคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="0d0a9-133">The Power BI service connects to many data sources, including Excel files that live on your computer.</span></span>

1. <span data-ttu-id="0d0a9-134">ลงชื่อเข้าบริการ Power BI เพื่อเริ่มใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0d0a9-134">To get started, sign in to the Power BI service.</span></span> <span data-ttu-id="0d0a9-135">หากคุณยังไม่ได้ลงทะเบียน[คุณสามารถทำได้โดยไม่มีค่าใช้จ่าย](https://powerbi.com)</span><span class="sxs-lookup"><span data-stu-id="0d0a9-135">If you haven’t signed up, [you can do so for free](https://powerbi.com).</span></span>
1. <span data-ttu-id="0d0a9-136">ใน **พื้นที่ทำงานของฉัน** ให้เลือก **ใหม่** > **อัปโหลดไฟล์**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-136">In **My workspace**, select **New** > **Upload a file**.</span></span>

    :::image type="content" source="media/service-from-excel-to-stunning-report/power-bi-new-upload.png" alt-text="ภาพหน้าจอของตัวเลือกอัปโหลดไฟล์":::

1. <span data-ttu-id="0d0a9-138">เลือก **ไฟล์ภายในเครื่อง** เรียกดูตำแหน่งที่คุณบันทึกไฟล์ Excel ตัวอย่างการเงิน และเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-138">Select **Local File**, browse to where you saved the Financial Sample Excel file, and select **Open**.</span></span>
7. <span data-ttu-id="0d0a9-139">บนหน้า **ไฟล์ภายในเครื่อง** ให้เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-139">On the **Local File** page, select **Import**.</span></span>

    <span data-ttu-id="0d0a9-140">ในตอนนี้คุณมีชุดข้อมูลตัวอย่างการเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="0d0a9-140">Now you have a Financial Sample dataset.</span></span> <span data-ttu-id="0d0a9-141">และ Power BI จะสร้างแดชบอร์ดว่างโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="0d0a9-141">Power BI also automatically created a blank dashboard.</span></span> <span data-ttu-id="0d0a9-142">หากคุณไม่เห็นแดชบอร์ด ให้รีเฟรชเบราว์เซอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="0d0a9-142">If you don't see the dashboard, refresh your browser.</span></span>

    :::image type="content" source="media/service-from-excel-to-stunning-report/power-bi-financial-dataset.png" alt-text="ภาพหน้าจอของพื้นที่ทำงานของฉันที่มีชุดข้อมูลตัวอย่างการเงิน":::

2. <span data-ttu-id="0d0a9-144">คุณต้องการสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="0d0a9-144">You want to create a report.</span></span> <span data-ttu-id="0d0a9-145">ยังอยู่ใน **พื้นที่ทำงานของฉัน** ให้เลือก **รายงาน** > **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-145">Still in **My workspace**, select **New** > **Report**.</span></span>

   ![ภาพหน้าจอของตัวเลือกรายงานใหม่](media/service-from-excel-to-stunning-report/power-bi-new-report.png)

3. <span data-ttu-id="0d0a9-147">ในกล่องโต้ตอบ **เลือกชุดข้อมูลเพื่อสร้างรายงาน** ให้เลือกชุดข้อมูล **ตัวอย่างการเงิน** ของคุณ > **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-147">In the **Select a dataset to create a report** dialog box, select your **Financial Sample** dataset > **Create**.</span></span>

   ![ภาพหน้าจอของเลือกกล่องโต้ตอบชุดข้อมูล](media/service-from-excel-to-stunning-report/power-bi-select-dataset.png)

## <a name="build-your-report"></a><span data-ttu-id="0d0a9-149">บันทึกรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="0d0a9-149">Build your report</span></span>
 
<span data-ttu-id="0d0a9-150">รายงานเปิดขึ้นในมุมมองการแก้ไขและแสดงพื้นที่รายงานที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="0d0a9-150">The report opens in Editing view and displays the blank report canvas.</span></span> <span data-ttu-id="0d0a9-151">ที่ด้านขวาคือบานหน้าต่าง **การแสดงภาพ** **ตัวกรอง** และ **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-151">On the right are the **Visualizations**, **Filters**, and **Fields** panes.</span></span> <span data-ttu-id="0d0a9-152">ข้อมูลในตารางสมุดงาน Excel ของคุณปรากฏขึ้นในบานหน้าต่าง **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-152">Your Excel workbook table data appears in the **Fields** pane.</span></span> <span data-ttu-id="0d0a9-153">ที่ด้านบนคือชื่อของตาราง **การเงิน**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-153">At the top is the name of the table, **financials**.</span></span> <span data-ttu-id="0d0a9-154">ที่ด้านล่างชื่อ Power BI จะแสดงรายการส่วนหัวของคอลัมน์เป็นแขตข้อมูลแต่ละช่อง</span><span class="sxs-lookup"><span data-stu-id="0d0a9-154">Under that, Power BI lists the column headings as individual fields.</span></span>

<span data-ttu-id="0d0a9-155">คุณเห็นสัญลักษณ์ซิกมาในรายการเขตข้อมูลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0d0a9-155">You see the Sigma symbols in the Fields list?</span></span> <span data-ttu-id="0d0a9-156">Power BI ตรวจพบว่าเขตข้อมูลเหล่านั้นเป็นตัวเลข</span><span class="sxs-lookup"><span data-stu-id="0d0a9-156">Power BI has detected that those fields are numeric.</span></span> <span data-ttu-id="0d0a9-157">Power BI ยังระบุเขตข้อมูลทางภูมิศาสตร์ที่มีสัญลักษณ์ลูกโลก</span><span class="sxs-lookup"><span data-stu-id="0d0a9-157">Power BI also indicates a geographic field with a globe symbol.</span></span>

![ภาพหน้าจอของลักษณะข้อมูล Excel ในบานหน้าต่างเขตข้อมูลข้อมูล](media/service-from-excel-to-stunning-report/power-bi-fields-list-financial.png)

1. <span data-ttu-id="0d0a9-159">หากต้องการที่ว่างสำหรับพื้นที่รายงาน ให้เลือก **ซ่อนบานหน้าต่างการนำทาง** และลดขนาดบานหน้าต่าง **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-159">To have more room for the report canvas, select **Hide the navigation pane**, and minimize the **Filters** pane.</span></span>

    :::image type="content" source="media/service-from-excel-to-stunning-report/power-bi-hide-nav-pane.png" alt-text="ภาพหน้าจอของการลดขนาดบานหน้าต่างการนำทาง"::: 

1. <span data-ttu-id="0d0a9-161">ตอนนี้คุณสามารถเริ่มต้นสร้างการแสดงภาพได้</span><span class="sxs-lookup"><span data-stu-id="0d0a9-161">Now you can begin to create visualizations.</span></span> <span data-ttu-id="0d0a9-162">สมมติว่าผู้จัดการของคุณต้องการเห็นผลกำไรเมื่อเวลาผ่านไป</span><span class="sxs-lookup"><span data-stu-id="0d0a9-162">Let's say your manager wants to see profit over time.</span></span> <span data-ttu-id="0d0a9-163">ในบานหน้าต่าง **เขตข้อมูล** ลาก **กำไร** ไปยังพื้นที่ของรายงาน</span><span class="sxs-lookup"><span data-stu-id="0d0a9-163">In the **Fields** pane, drag **Profit** to the report canvas.</span></span> 

   <span data-ttu-id="0d0a9-164">ตามค่าเริ่มต้น Power BI จะแสดงแผนภูมิคอลัมน์ที่มีคอลัมน์เดียว</span><span class="sxs-lookup"><span data-stu-id="0d0a9-164">By default, Power BI displays a column chart with one column.</span></span> 

    :::image type="content" source="media/service-from-excel-to-stunning-report/power-bi-profit-column.png" alt-text="ภาพหน้าจอของแผนภูมิคอลัมน์ที่มีคอลัมน์เดียว":::

3. <span data-ttu-id="0d0a9-166">ลาก **วันที่** ไปยังพื้นที่ของรายงาน</span><span class="sxs-lookup"><span data-stu-id="0d0a9-166">Drag **Date** to the report canvas.</span></span> 

   <span data-ttu-id="0d0a9-167">Power BI อัปเดตแผนภูมิคอลัมน์เพื่อแสดงกำไรตามวันที่</span><span class="sxs-lookup"><span data-stu-id="0d0a9-167">Power BI updates the column chart to show profit by date.</span></span>

   ![ภาพหน้าจอของแผนภูมิคอลัมน์ในตัวแก้ไขรายงาน](media/service-from-excel-to-stunning-report/power-bi-profit-date.png)

    <span data-ttu-id="0d0a9-169">ธันวาคม 2014 เป็นเดือนที่มีกำไรมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="0d0a9-169">December 2014 was the most profitable month.</span></span>
   
    > [!TIP]
    > <span data-ttu-id="0d0a9-170">หากค่าแผนภูมิของคุณไม่เหมือนกับที่คุณคาดไว้ ให้ตรวจสอบการรวมข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="0d0a9-170">If your chart values don't look as you expect, check your aggregations.</span></span> <span data-ttu-id="0d0a9-171">ตัวอย่างเช่น ในบริเวณ **ค่า** เลือกเขตข้อมูล **กำไร** ที่คุณเพิ่งเพิ่มเข้ามา และตรวจสอบให้แน่ใจว่าการรวมข้อมูลดำเนินการตามวิธีที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="0d0a9-171">For example, in the **Values** well, select the **Profit** field you just added and ensure the data is being aggregated the way you'd like it.</span></span> <span data-ttu-id="0d0a9-172">ในตัวอย่างนี้ เรากำลังใช้ **ผลรวม**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-172">In this example, we're using **Sum**.</span></span>
    > 

### <a name="create-a-map"></a><span data-ttu-id="0d0a9-173">สร้างแผนที่</span><span class="sxs-lookup"><span data-stu-id="0d0a9-173">Create a map</span></span>

<span data-ttu-id="0d0a9-174">ผู้จัดการของคุณต้องการทราบว่าประเทศใดทำกำไรมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="0d0a9-174">Your manager wants to know which countries are the most profitable.</span></span> <span data-ttu-id="0d0a9-175">สร้างความประทับใจให้ผู้จัดการด้วยการแสดงภาพแผนที่</span><span class="sxs-lookup"><span data-stu-id="0d0a9-175">Impress your manager with a map visualization.</span></span> 

1. <span data-ttu-id="0d0a9-176">เลือกพื้นที่ว่างบนพื้นที่รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="0d0a9-176">Select a blank area on your report canvas.</span></span> 

2. <span data-ttu-id="0d0a9-177">จากบานหน้าต่าง **เขตข้อมูล** ให้ลากเขตข้อมูล **ประเทศ** ไปยังพื้นที่รายงานของคุณ จากนั้นจึงลากเขตข้อมูล **กำไร** ไปยังแผนที่</span><span class="sxs-lookup"><span data-stu-id="0d0a9-177">From the **Fields** pane, drag the **Country** field to your report canvas, then drag the **Profit** field to the map.</span></span>

   <span data-ttu-id="0d0a9-178">Power BI สร้างภาพแผนที่พร้อมฟองอากาศที่เป็นตัวแทนผลกำไรของแต่ละพื้นที่</span><span class="sxs-lookup"><span data-stu-id="0d0a9-178">Power BI creates a map visual with bubbles representing the relative profit of each location.</span></span>

   ![ภาพหน้าจอของวิชวลแผนที่ในตัวแก้ไขรายงาน](media/service-from-excel-to-stunning-report/power-bi-map-visual.png)

    <span data-ttu-id="0d0a9-180">ดูเหมือนว่าประเทศในแถบยุโรปจะมีประสิทธิภาพเหนือกว่าประเทศในอเมริกาเหนือ</span><span class="sxs-lookup"><span data-stu-id="0d0a9-180">Looks like the European countries are outperforming the North American countries.</span></span>

### <a name="create-a-visual-showing-sales"></a><span data-ttu-id="0d0a9-181">สร้างวิชวลที่แสดงยอดขาย</span><span class="sxs-lookup"><span data-stu-id="0d0a9-181">Create a visual showing sales</span></span>

<span data-ttu-id="0d0a9-182">คุณต้องการแสดงภาพที่นำเสนอยอดขายตามภาคส่วนผลิตภัณฑ์และการตลาดหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="0d0a9-182">What about displaying a visual showing sales by product and market segment?</span></span> <span data-ttu-id="0d0a9-183">ทำได้ง่าย</span><span class="sxs-lookup"><span data-stu-id="0d0a9-183">Easy.</span></span> 

1. <span data-ttu-id="0d0a9-184">เลือกพื้นที่ว่าง</span><span class="sxs-lookup"><span data-stu-id="0d0a9-184">Select the blank canvas.</span></span>

1. <span data-ttu-id="0d0a9-185">ในบานหน้าต่าง **เขตข้อมูล** ให้เลือกเขตข้อมูล **การขาย**, **ผลิตภัณฑ์** และ **ภาคส่วน**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-185">In the **Fields** pane, select the **Sales**, **Product**, and **Segment** fields.</span></span> 
   
   <span data-ttu-id="0d0a9-186">Power BI สร้างแผนภูมิคอลัมน์แบบคลัสเตอร์</span><span class="sxs-lookup"><span data-stu-id="0d0a9-186">Power BI creates a clustered column chart.</span></span> 

2. <span data-ttu-id="0d0a9-187">เปลี่ยนชนิดของแผนภูมิโดยการเลือกไอคอนใดไอคอนหนึ่งในเมนู **การแสดงข้อมูลด้วยภาพ**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-187">Change the type of chart by choosing one of the icons in the **Visualizations** menu.</span></span> <span data-ttu-id="0d0a9-188">เช่น เปลี่ยนเป็น **แผนภูมิคอลัมน์แบบเรียงซ้อนกัน**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-188">For instance, change it to a **Stacked column chart**.</span></span> 

   ![ภาพหน้าจอของแผนภูมิคอลัมน์แบบเรียงซ้อนกันในตัวแก้ไขรายงาน](media/service-from-excel-to-stunning-report/power-bi-stacked-column.png)

3. <span data-ttu-id="0d0a9-190">เมื่อต้องการเรียงลำดับแผนภูมิ เลือก **ตัวเลือกเพิ่มเติม** (...) > **เรียงลำดับตาม**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-190">To sort the chart, select **More options** (...) > **Sort by**.</span></span>

### <a name="spruce-up-the-visuals"></a><span data-ttu-id="0d0a9-191">จัดวิชวลให้เป็นระเบียบ</span><span class="sxs-lookup"><span data-stu-id="0d0a9-191">Spruce up the visuals</span></span>

<span data-ttu-id="0d0a9-192">ทำการเปลี่ยนแปลงต่อไปนี้บนแท็บ **จัดรูปแบบ** ในบานหน้าต่างการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="0d0a9-192">Make the following changes on the **Format** tab in the Visualizations pane.</span></span>

:::image type="content" source="media/desktop-excel-stunning-report/power-bi-format-tab-visualizations.png" alt-text="ภาพหน้าจอของแท็บจัดรูปแบบในบานหน้าต่างการแสดงภาพ":::

1. <span data-ttu-id="0d0a9-194">เลือกแผนภูมิคอลัมน์ **กำไรตามวันที่**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-194">Select the **Profit by Date** column chart.</span></span> <span data-ttu-id="0d0a9-195">ในส่วน **ชื่อเรื่อง** ให้เปลี่ยน **ขนาดข้อความ** เป็น **16 pt**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-195">In the **Title** section, change **Text size** to **16 pt**.</span></span> <span data-ttu-id="0d0a9-196">ตั้งค่า **เงา** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-196">Toggle **Shadow** to **On**.</span></span> 

1. <span data-ttu-id="0d0a9-197">เลือกแผนภูมิคอลัมน์แบบเรียงซ้อนของ **ยอดขายตามผลิตภัณฑ์และเซกเมนต์**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-197">Select the **Sales by Product and Segment** stacked column chart.</span></span> <span data-ttu-id="0d0a9-198">ในส่วน **ชื่อเรื่อง** ให้เปลี่ยน **ขนาดข้อความ** ของชื่อเรื่องเป็น **16 pt**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-198">In the **Title** section, change title **Text size** to **16 pt**.</span></span> <span data-ttu-id="0d0a9-199">ตั้งค่า **เงา** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-199">Toggle **Shadow** to **On**.</span></span>

1. <span data-ttu-id="0d0a9-200">เลือกแผนที่ **กำไรตามประเทศ**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-200">Select the **Profit by Country** map.</span></span> <span data-ttu-id="0d0a9-201">ในส่วน **ลักษณะแผนที่** ให้เปลี่ยน **ธีม** เป็น **โทนสีเทา**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-201">In the **Map styles** section, change **Theme** to **Grayscale**.</span></span> <span data-ttu-id="0d0a9-202">ในส่วน **ชื่อเรื่อง** ให้เปลี่ยน **ขนาดข้อความ** ของชื่อเรื่องเป็น **16 pt**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-202">In the **Title** section, change title **Text size** to **16 pt**.</span></span> <span data-ttu-id="0d0a9-203">ตั้งค่า **เงา** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-203">Toggle **Shadow** to **On**.</span></span>


## <a name="pin-to-a-dashboard"></a><span data-ttu-id="0d0a9-204">ปักหมุดไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="0d0a9-204">Pin to a dashboard</span></span>

<span data-ttu-id="0d0a9-205">ในตอนนี้ คุณสามารถปักหมุดวิชวลทั้งหมดของคุณไปยังแดชบอร์ดว่างที่ Power BI สร้างขึ้นตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="0d0a9-205">Now you can pin all of your visuals to the blank dashboard that Power BI created by default.</span></span> 

1. <span data-ttu-id="0d0a9-206">วางเมาส์เหนือวิชวลและเลือก **ปักหมุดวิชวล**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-206">Hover over a visual and select **Pin visual**.</span></span>

   ![ภาพหน้าจอของการปักหมุดวิชวลไปยังแดชบอร์ด](media/service-from-excel-to-stunning-report/power-bi-pin-visual.png)

1. <span data-ttu-id="0d0a9-208">คุณจะต้องบันทึกรายงานของคุณก่อน คุณจึงจะสามารถปักหมุดวิชวลไปยังแดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="0d0a9-208">You need to save your report before you can pin a visual to the dashboard.</span></span> <span data-ttu-id="0d0a9-209">ตั้งชื่อรายงานของคุณ และเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-209">Give your report a name and select **Save**.</span></span>
1. <span data-ttu-id="0d0a9-210">ปักหมุดวิชวลแต่ละภาพไปยังแดชบอร์ดที่ Power BI สร้างขึ้น **ตัวอย่างการเงิน.xlsx**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-210">Pin each visual to the dashboard that Power BI created, **Financial Sample.xlsx**.</span></span>
1. <span data-ttu-id="0d0a9-211">เมื่อคุณปักหมุดวิชวลล่าสุด ให้เลือก **ไปที่แดชบอร์ด**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-211">When you pin the last visual, select **Go to dashboard**.</span></span>
1. <span data-ttu-id="0d0a9-212">Power BI เพิ่มไทล์ข้อความตัวอย่างสำหรับตัวอย่างการเงิน.xlsx ไปยังแดชบอร์ดโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="0d0a9-212">Power BI added a placeholder Financial Sample.xlsx tile to the dashboard automatically.</span></span> <span data-ttu-id="0d0a9-213">เลือก **ตัวเลือกเพิ่มเติม (...)**  > **ลบไทล์**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-213">Select **More options (...)** > **Delete tile**.</span></span>

    :::image type="content" source="media/service-from-excel-to-stunning-report/power-bi-tile-more-options.png" alt-text="ภาพหน้าจอของตัวเลือกเพิ่มเติมสำหรับไทล์":::

1. <span data-ttu-id="0d0a9-215">จัดเรียงใหม่และปรับขนาดไทล์ในแบบที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="0d0a9-215">Rearrange and resize the tiles any way you want.</span></span>

<span data-ttu-id="0d0a9-216">แดชบอร์ดและรายงานพร้อมแล้ว</span><span class="sxs-lookup"><span data-stu-id="0d0a9-216">The dashboard and report are ready.</span></span>

## <a name="share-a-link-to-your-dashboard"></a><span data-ttu-id="0d0a9-217">แชร์ลิงก์ไปยังแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="0d0a9-217">Share a link to your dashboard</span></span>

<span data-ttu-id="0d0a9-218">ในตอนนี้ก็ถึงเวลาที่จะแชร์แดชบอร์ดของคุณกับผู้จัดการแล้ว</span><span class="sxs-lookup"><span data-stu-id="0d0a9-218">Now it's time to share your dashboard with your manager.</span></span> <span data-ttu-id="0d0a9-219">คุณสามารถแชร์แดชบอร์ดและรายงานที่สำคัญของคุณกับเพื่อนร่วมงานที่มีบัญชี Power BI</span><span class="sxs-lookup"><span data-stu-id="0d0a9-219">You can share your dashboard and underlying report with any colleague who has a Power BI account.</span></span> <span data-ttu-id="0d0a9-220">บุคคลเหล่านี้สามารถโต้ตอบกับรายงานของคุณ แต่ไม่สามารถบันทึกการเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="0d0a9-220">They can interact with your report, but can't save changes.</span></span> <span data-ttu-id="0d0a9-221">หากคุณอนุญาต พวกเขาสามารถแชร์ต่อกับผู้อื่นหรือสร้างรายงานใหม่ที่ยึดตามชุดข้อมูลพื้นฐานได้</span><span class="sxs-lookup"><span data-stu-id="0d0a9-221">If you allow it, they can reshare with others, or build a new report based on the underlying dataset.</span></span>

1. <span data-ttu-id="0d0a9-222">เมื่อต้องการแชร์รายงานของคุณ ที่ด้านบนสุดของแดชบอร์ด ให้เลือก **แชร์**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-222">To share your report, at the top of the dashboard, select **Share**.</span></span>

   ![ภาพหน้าจอของไอคอนแชร์](media/service-from-excel-to-stunning-report/power-bi-share-dashboard.png)

2. <span data-ttu-id="0d0a9-224">ในหน้า **แชร์แดชบอร์ด** ให้ป้อนที่อยู่อีเมลของผู้รับในกล่อง **ป้อนที่อยู่อีเมล** และเพิ่มข้อความในกล่องด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="0d0a9-224">In the **Share dashboard** page, enter the email addresses of the recipients in the **Enter email addresses** box and add a message in the box below it.</span></span> 

3. <span data-ttu-id="0d0a9-225">ตัดสินใจว่าคุณต้องการใช้ตัวเลือกใด หากมี:</span><span class="sxs-lookup"><span data-stu-id="0d0a9-225">Decide which of these options you want, if any:</span></span>

    - <span data-ttu-id="0d0a9-226">**อนุญาตให้ผู้รับแชร์แดชบอร์ดของคุณ**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-226">**Allow recipients to share your dashboard**.</span></span> 
    - <span data-ttu-id="0d0a9-227">**อนุญาตให้ผู้รับสร้างเนื้อหาใหม่โดยใช้ชุดข้อมูลพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-227">**Allow recipients to build new content using the underlying datasets**.</span></span>
    - <span data-ttu-id="0d0a9-228">**ส่งการแจ้งเตือนทางอีเมลไปยังผู้รับ**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-228">**Send an email notification to recipients.**</span></span>

   ![ภาพหน้าจอของบานหน้าต่างแชร์แดชบอร์ด](media/service-from-excel-to-stunning-report/power-bi-share-dashboard-pane.png)

1. <span data-ttu-id="0d0a9-230">เลือก **แชร์**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-230">Select **Share**.</span></span>

## <a name="share-to-microsoft-teams"></a><span data-ttu-id="0d0a9-231">แชร์ไปยัง Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0d0a9-231">Share to Microsoft Teams</span></span>

<span data-ttu-id="0d0a9-232">คุณยังสามารถแชร์รายงานและแดชบอร์ดให้เพื่อนร่วมงานของคุณได้โดยตรงใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0d0a9-232">You can also share reports and dashboards directly to your colleagues in Microsoft Teams.</span></span>

1. <span data-ttu-id="0d0a9-233">หากต้องการแชร์ใน Teams ที่ด้านบนสุดของแดชบอร์ดให้เลือก **สนทนาในทีม**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-233">To share in Teams, at the top of the dashboard, select **Chat in Teams**.</span></span>

   ![สกรีนช็อตของตัวเลือกสนทนาในทีม](media/service-from-excel-to-stunning-report/power-bi-share-teams.png)

2. <span data-ttu-id="0d0a9-235">Power BI แสดงกล่องโต้ตอบ **แชร์ไปยัง Teams**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-235">Power BI displays the **Share to Teams** dialog.</span></span> <span data-ttu-id="0d0a9-236">ใส่ชื่อของบุคคล กลุ่ม หรือช่อง และเลือก **แชร์**</span><span class="sxs-lookup"><span data-stu-id="0d0a9-236">Enter the name of a person, group, or channel and select **Share**.</span></span> 
   
    :::image type="content" source="media/service-from-excel-to-stunning-report/power-bi-share-teams-dialog.png" alt-text="ภาพหน้าจอของกล่องโต้ตอบแชร์ไปยัง Teams":::

3. <span data-ttu-id="0d0a9-238">ลิงก์จะปรากฏใน **โพสต์** สำหรับบุคคล กลุ่ม หรือช่องดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="0d0a9-238">The link appears in the **Posts** for that person, group, or channel.</span></span>

   ![ภาพหน้าจอของการโพสต์ใน Teams](media/service-from-excel-to-stunning-report/power-bi-teams-chat.png)

## <a name="next-steps"></a><span data-ttu-id="0d0a9-240">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="0d0a9-240">Next steps</span></span>

* <span data-ttu-id="0d0a9-241">ในตอนนี้คุณได้สร้างรายงานพื้นฐานในบริการของ Power BI แล้ววิธีการสร้างรายงานใน Power BI Desktop ล่ะ?</span><span class="sxs-lookup"><span data-stu-id="0d0a9-241">Now that you've created a basic report in the Power BI service, how about creating a report in Power BI Desktop?</span></span> <span data-ttu-id="0d0a9-242">ลองใช้บทช่วยสอน [จากเวิร์กบุ๊ก Excel ไปสู่รายงานอันน่าทึ่งใน Power BI Desktop](desktop-excel-stunning-report.md)</span><span class="sxs-lookup"><span data-stu-id="0d0a9-242">Try the tutorial, [From Excel workbook to stunning report in Power BI Desktop](desktop-excel-stunning-report.md).</span></span>

<span data-ttu-id="0d0a9-243">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0d0a9-243">More questions?</span></span> <span data-ttu-id="0d0a9-244">[ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="0d0a9-244">[Try the Power BI Community](https://community.powerbi.com/).</span></span>
