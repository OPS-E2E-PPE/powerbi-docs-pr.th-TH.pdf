---
title: 'บทช่วยสอน: ใช้แบบจำลอง Azure Machine Learning ใน Power BI'
titleSuffix: Azure Machine Learning
description: เรียนรู้วิธีใช้แบบจำลอง Azure Machine Learning ใน Power BI
services: machine-learning
ms.service: machine-learning
ms.subservice: core
ms.topic: tutorial
ms.author: samkemp
author: samuel100
ms.reviewer: sdgilley, maggies
ms.date: 12/10/2020
ms.openlocfilehash: 6c68fff575e4da0c9126904df2de5292747c209c
ms.sourcegitcommit: 46cf62d9bb33ac7b7eae7910fbba6756f626c65f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/15/2020
ms.locfileid: "97491793"
---
# <a name="tutorial-consume-azure-machine-learning-models-in-power-bi"></a><span data-ttu-id="6ac3e-103">บทช่วยสอน: ใช้แบบจำลอง Azure Machine Learning ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="6ac3e-103">Tutorial: Consume Azure Machine Learning models in Power BI</span></span>

<span data-ttu-id="6ac3e-104">บทช่วยสอนนี้จะแนะนำการสร้างรายงาน Power BI ตามแบบจำลองการเรียนรู้ของเครื่อง</span><span class="sxs-lookup"><span data-stu-id="6ac3e-104">This tutorial walks you through creating a Power BI report based on a machine learning model.</span></span> <span data-ttu-id="6ac3e-105">ในตอนท้ายของบทช่วยสอนนี้ คุณจะสามารถ:</span><span class="sxs-lookup"><span data-stu-id="6ac3e-105">By the end of this tutorial, you'll be able to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="6ac3e-106">ให้คะแนนแบบจำลองการเรียนรู้ของเครื่อง (ที่ปรับใช้โดยใช้ Azure Machine Learning) ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="6ac3e-106">Score machine learning models (deployed using Azure Machine Learning) in Power BI.</span></span>
> * <span data-ttu-id="6ac3e-107">เชื่อมต่อกับแบบจำลอง Azure Machine Learning ในตัวแก้ไข Power Query</span><span class="sxs-lookup"><span data-stu-id="6ac3e-107">Connect to an Azure Machine Learning model in the Power Query Editor.</span></span>
> * <span data-ttu-id="6ac3e-108">สร้างรายงานด้วยการจัดรูปแบบการแสดงข้อมูลตามแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="6ac3e-108">Create a report with a visualization based on that model.</span></span>
> * <span data-ttu-id="6ac3e-109">เผยแพร่รายงานดังกล่าวไปยังบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="6ac3e-109">Publish that report to the Power BI service.</span></span>
> * <span data-ttu-id="6ac3e-110">ตั้งค่าการรีเฟรชที่ตั้งกำหนดการแล้วสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="6ac3e-110">Set up scheduled refresh for the report.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6ac3e-111">สิ่งที่จำเป็นต้องมี</span><span class="sxs-lookup"><span data-stu-id="6ac3e-111">Prerequisites</span></span>

<span data-ttu-id="6ac3e-112">ก่อนที่จะเริ่มบทช่วยสอน คุณจำเป็นต้อง:</span><span class="sxs-lookup"><span data-stu-id="6ac3e-112">Before starting this tutorial, you need to:</span></span>

- <span data-ttu-id="6ac3e-113">ฝึกอบรมและปรับใช้แบบจำลองการเรียนรู้ของเครื่องใน Azure Machine Learning</span><span class="sxs-lookup"><span data-stu-id="6ac3e-113">Train and deploy a machine learning model in Azure Machine Learning.</span></span> <span data-ttu-id="6ac3e-114">ใช้หนึ่งในสามบทช่วยสอน Azure Machine Learning:</span><span class="sxs-lookup"><span data-stu-id="6ac3e-114">Use one of these three Azure Machine Learning tutorials:</span></span> 

    - [<span data-ttu-id="6ac3e-115">ตัวเลือก A: รหัส</span><span class="sxs-lookup"><span data-stu-id="6ac3e-115">Option A: Code</span></span>](/azure/machine-learning/tutorial-power-bi-custom-model)
    - [<span data-ttu-id="6ac3e-116">ตัวเลือก B: ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="6ac3e-116">Option B: Designer</span></span>](/azure/machine-learning/tutorial-power-bi-designer-model)
    - [<span data-ttu-id="6ac3e-117">ตัวเลือก C: ML อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6ac3e-117">Option C: Automated ML</span></span>](/azure/machine-learning/tutorial-power-bi-automated-model)

- <span data-ttu-id="6ac3e-118">ลงทะเบียนสำหรับ[รุ่นทดลองใช้ Power BI ฟรี](https://app.powerbi.com/signupredirect?pbi_source=web)</span><span class="sxs-lookup"><span data-stu-id="6ac3e-118">Sign up for a [free Power BI trial](https://app.powerbi.com/signupredirect?pbi_source=web).</span></span>
- <span data-ttu-id="6ac3e-119">[ติดตั้ง Power BI Desktop](https://powerbi.microsoft.com/desktop/) ภายในคอมพิวเตอร์</span><span class="sxs-lookup"><span data-stu-id="6ac3e-119">[Install Power BI Desktop](https://powerbi.microsoft.com/desktop/) on a local computer.</span></span>

## <a name="create-the-data-model"></a><span data-ttu-id="6ac3e-120">สร้างแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6ac3e-120">Create the data model</span></span>

<span data-ttu-id="6ac3e-121">เปิด Power BI Desktop แล้วเลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-121">Open Power BI Desktop and select **Get Data**.</span></span> <span data-ttu-id="6ac3e-122">ในกล่องโต้ตอบ **รับข้อมูล** ให้ค้นหา **เว็บ**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-122">In the **Get Data** dialog box, search for **web**.</span></span> <span data-ttu-id="6ac3e-123">เลือกแหล่งข้อมูล **เว็บ** > **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-123">Select the **Web** source > **Connect**.</span></span>

:::image type="content" source="media/service-aml-integrate/pbi-get-data.png" alt-text="สกรีนช็อตที่แสดงข้อมูลเว็บ":::

<span data-ttu-id="6ac3e-125">ในกล่องโต้ตอบ **จากเว็บ** ให้คัดลอกและวาง URL ต่อไปนี้ลงในกล่อง:</span><span class="sxs-lookup"><span data-stu-id="6ac3e-125">In the **From Web** dialog box, copy and paste the following URL in the box:</span></span>

```txt 
https://www4.stat.ncsu.edu/~boos/var.select/diabetes.tab.txt
```

:::image type="content" source="media/service-aml-integrate/pbi-data.png" alt-text="สกรีนช็อตที่แสดง URL เว็บ":::

<span data-ttu-id="6ac3e-127">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-127">Select **OK**.</span></span>

<span data-ttu-id="6ac3e-128">เลือก **แปลงข้อมูล** เพื่อเปิดหน้าต่าง **ตัวแก้ไข Power Query**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-128">Select **Transform data** to open the **Power Query Editor** window.</span></span>

<span data-ttu-id="6ac3e-129">ใน Ribbon หน้าแรกของตัวแก้ไข Power Query ให้เลือกปุ่ม **Azure Machine Learning**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-129">In the Home ribbon of the Power Query Editor, select the **Azure Machine Learning** button.</span></span>

:::image type="content" source="media/service-aml-integrate/aml-button.png" alt-text="สกรีนช็อตที่แสดงตัวแก้ไข Power Query":::

<span data-ttu-id="6ac3e-131">หลังจากลงชื่อเข้าใช้บัญชี Azure ของคุณโดยใช้การลงชื่อเข้าระบบครั้งเดียว คุณจะเห็นรายการของบริการที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6ac3e-131">After signing in to your Azure account using single sign-on, you see a list of available services.</span></span> <span data-ttu-id="6ac3e-132">เลือก **บริการ sklearn ของฉัน** ที่คุณสร้างขึ้นจากฝึกอบรมและปรับใช้บทช่วยสอนแบบจำลองการเรียนรู้ของเครื่อง</span><span class="sxs-lookup"><span data-stu-id="6ac3e-132">Select the **my-sklearn-service** that you created from the Train and deploy a machine learning model tutorial.</span></span> 

<span data-ttu-id="6ac3e-133">Power Query เติมข้อมูลคอลัมน์ให้คุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6ac3e-133">Power Query populates the columns automatically for you.</span></span> <span data-ttu-id="6ac3e-134">คุณจำไว้ว่าใน Schema ของเราสำหรับบริการ เรามีมัณฑนา Python ที่ระบุการป้อนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6ac3e-134">You remember that in our schema for the service, we had a Python decorator that specified the inputs.</span></span> <span data-ttu-id="6ac3e-135">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-135">Select **OK**.</span></span>

:::image type="content" source="media/service-aml-integrate/aml-pbi-run.png" alt-text="สกรีนช็อตที่แสดงแบบจำลอง Azure Machine Learning":::

<span data-ttu-id="6ac3e-137">การเลือก **ตกลง** จะเรียกใช้บริการ Azure Machine Learning</span><span class="sxs-lookup"><span data-stu-id="6ac3e-137">Selecting **OK** calls the Azure Machine Learning service.</span></span> <span data-ttu-id="6ac3e-138">ซึ่งจะทริกเกอร์คำเตือนเกี่ยวกับความเป็นส่วนตัวของข้อมูลสำหรับทั้งข้อมูลและจุดสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="6ac3e-138">It triggers a warning on data privacy for both the data and the endpoint.</span></span>

:::image type="content" source="media/service-aml-integrate/data_privacy_warning.png" alt-text="สกรีนช็อตที่แสดงคำเตือนความเป็นส่วนตัว":::

<span data-ttu-id="6ac3e-140">เลือก **ดำเนินต่อ**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-140">Select **Continue**.</span></span> <span data-ttu-id="6ac3e-141">ในหน้าจอถัดไป เลือก **ละเว้นระดับความเป็นส่วนตัวในการตรวจสอบไฟล์นี้** > **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-141">In the next screen, select **Ignore Privacy Levels checks for this file** > **Save**.</span></span>

<span data-ttu-id="6ac3e-142">เมื่อให้คะแนนข้อมูลแล้ว Power Query จะสร้างคอลัมน์เพิ่มเติมที่ชื่อว่า **AzureML.my-diabetes-model**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-142">Once the data is scored, Power Query creates an additional column named **AzureML.my-diabetes-model**.</span></span>

:::image type="content" source="media/service-aml-integrate/scored-data.png" alt-text="สกรีนช็อตที่แสดงคอลัมน์ที่ให้คะแนนแล้วที่เพิ่มเข้ามา":::

<span data-ttu-id="6ac3e-144">ข้อมูลที่บริการส่งกลับคือ **รายการ**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-144">The data that the service returns is a **list**.</span></span> 

> [!NOTE]
> <span data-ttu-id="6ac3e-145">หากคุณปรับใช้แบบจำลองตัวออกแบบ คุณจะเห็น **ระเบียน**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-145">If you deployed a designer model, you see a **record**.</span></span>

<span data-ttu-id="6ac3e-146">หากต้องการรับการคาดคะเน ใน Ribbon **แปลง** ให้เลือกปุ่ม **ขยายคอลัมน์** > **ขยายไปยังแถวใหม่**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-146">To get the predictions, on the **Transform** ribbon select the **Expand column** button > **Expand to New Rows**.</span></span>

<span data-ttu-id="6ac3e-147">หลังจากที่ขยายแล้ว คุณจะเห็นการคาดคะเนในคอลัมน์ AzureML.my-diabetes-model</span><span class="sxs-lookup"><span data-stu-id="6ac3e-147">After the expansion, you see the predictions in the AzureML.my-diabetes-model column.</span></span>

:::image type="content" source="media/service-aml-integrate/after-expand.png" alt-text="สกรีนช็อตที่แสดงการขยาย":::

<span data-ttu-id="6ac3e-149">ทำตามขั้นตอนถัดไปเพื่อล้างแบบจำลองข้อมูลของคุณให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6ac3e-149">Follow these next steps to finish cleaning up your data model.</span></span>

1. <span data-ttu-id="6ac3e-150">เปลี่ยนชื่อคอลัมน์ **AzureML.my-diabetes-model** เป็น **คาดคะเนแล้ว**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-150">Rename the **AzureML.my-diabetes-model** column to **predicted**.</span></span>
1. <span data-ttu-id="6ac3e-151">เปลี่ยนชื่อคอลัมน์ **Y** เป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-151">Rename the **Y** column to **actual**.</span></span>
1. <span data-ttu-id="6ac3e-152">เปลี่ยนชนิดของคอลัมน์ **จริง**: เลือกคอลัมน์ จากนั้นใน Ribbon **แปลง** ให้เลือก **ชนิดข้อมูล** > **เลขทศนิยม**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-152">Change the type of the **actual** column: Select the column, then on the **Transform** ribbon select **Data Type** > **Decimal Number**.</span></span>
1. <span data-ttu-id="6ac3e-153">เปลี่ยนชนิดของคอลัมน์ **คาดคะเนแล้ว**: เลือกคอลัมน์ดังกล่าว จากนั้นใน Ribbon **แปลง** ให้เลือก **ชนิดข้อมูล** > **เลขทศนิยม**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-153">Change the type of the **predicted** column: Select that column, then on the **Transform** ribbon select **Data Type** > **Decimal Number**.</span></span>
1. <span data-ttu-id="6ac3e-154">ใน Ribbon **หน้าแรก** ให้เลือก **ปิดและนำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-154">On the **Home** ribbon, select **Close & Apply**.</span></span>

## <a name="create-a-report-with-visualizations"></a><span data-ttu-id="6ac3e-155">สร้างรายงานที่มีการจัดรูปแบบการแสดงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6ac3e-155">Create a report with visualizations</span></span>

<span data-ttu-id="6ac3e-156">ตอนนี้คุณสามารถสร้างการจัดรูปแบบการแสดงข้อมูลบางส่วนได้เพื่อแสดงข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="6ac3e-156">Now you can create some visualizations to show your data.</span></span>

1. <span data-ttu-id="6ac3e-157">ในบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล** ให้เลือก **แผนภูมิเส้น**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-157">In the **Visualizations** pane, select a **Line chart**.</span></span> 
1. <span data-ttu-id="6ac3e-158">เมื่อเลือกการแสดงผลด้วยภาพแผนภูมิเส้นแล้ว:</span><span class="sxs-lookup"><span data-stu-id="6ac3e-158">With the line chart visual selected:</span></span>
1. <span data-ttu-id="6ac3e-159">ลากเขตข้อมูล **อายุ** ไปยัง **แกน**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-159">Drag the **AGE** field to the **Axis**.</span></span>
1. <span data-ttu-id="6ac3e-160">ลากเขตข้อมูล **จริง** ไปยัง **ค่า**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-160">Drag the **actual** field to **Values**.</span></span>
1. <span data-ttu-id="6ac3e-161">ลากเขตข้อมูล **คาดคะเนแล้ว** ไปยัง **ค่า**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-161">Drag the **predicted** field to **Values**.</span></span>

<span data-ttu-id="6ac3e-162">ปรับขนาดแผนภูมิเส้นเพื่อเติมหน้า</span><span class="sxs-lookup"><span data-stu-id="6ac3e-162">Resize the line chart to fill the page.</span></span> <span data-ttu-id="6ac3e-163">ในตอนนี้ รายงานของคุณมีหนึ่งแผนภูมิเส้นที่ประกอบด้วยเส้นสองเส้น โดยที่เส้นหนึ่งคือค่าที่คาดคะเนและอีกเส้นหนึ่งคือค่าจริง ซึ่งจะแจกจ่ายตามอายุ</span><span class="sxs-lookup"><span data-stu-id="6ac3e-163">Your report now has a single line chart with two lines, one for the predicted and one for the actual values, distributed by age.</span></span>

:::image type="content" source="media/service-aml-integrate/report-viz.png" alt-text="สกรีนช็อตที่แสดงการจัดรูปแบบการแสดงข้อมูลรายงาน":::

## <a name="publish-the-report"></a><span data-ttu-id="6ac3e-165">เผยแพร่รายงาน</span><span class="sxs-lookup"><span data-stu-id="6ac3e-165">Publish the report</span></span>

<span data-ttu-id="6ac3e-166">คุณสามารถเพิ่มการจัดรูปแบบการแสดงข้อมูลเพิ่มเติมได้ตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="6ac3e-166">You can add more visualizations if you wish.</span></span> <span data-ttu-id="6ac3e-167">เพื่อความกระชับ ในบทช่วยสอนนี้ เราจะเผยแพร่รายงาน</span><span class="sxs-lookup"><span data-stu-id="6ac3e-167">In the interest of brevity, in this tutorial we'll publish the report.</span></span>

1. <span data-ttu-id="6ac3e-168">บันทึกรายงาน</span><span class="sxs-lookup"><span data-stu-id="6ac3e-168">Save the report.</span></span>
1. <span data-ttu-id="6ac3e-169">เลือก **ไฟล์** > **เผยแพร่** > **เผยแพร่ไปยัง Power BI**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-169">Select **File** > **Publish** > **Publish to Power BI**.</span></span>
1. <span data-ttu-id="6ac3e-170">ลงชื่อเข้าใช้บริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="6ac3e-170">Sign in to the Power BI service.</span></span>
1. <span data-ttu-id="6ac3e-171">เลือก **พื้นที่ทำงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-171">Select **My Workspace**.</span></span>
1. <span data-ttu-id="6ac3e-172">เมื่อเผยแพร่รายงานสำเร็จแล้ว ให้เลือกลิงก์ **เปิด <MY_PBIX_FILE.pbix> ใน Power BI**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-172">When the report is published successfully, select the **Open <MY_PBIX_FILE.pbix> in Power BI** link.</span></span> <span data-ttu-id="6ac3e-173">รายงานจะเปิดรายงานใน Power BI ในเบราว์เซอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6ac3e-173">The report opens the report in Power BI in your browser.</span></span>

     :::image type="content" source="media/service-aml-integrate/publish-success.png" alt-text="สกรีนช็อตที่แสดงการเผยแพร่ที่สำเร็จ":::

## <a name="enable-datasets-to-refresh"></a><span data-ttu-id="6ac3e-175">เปิดใช้งานชุดข้อมูลเพื่อรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="6ac3e-175">Enable datasets to refresh</span></span>

<span data-ttu-id="6ac3e-176">ในสถานการณ์ที่มีการรรีเฟรชแหล่งข้อมูลด้วยข้อมูลใหม่เพื่อให้คะแนน คุณจำเป็นต้องอัปเดตข้อมูลประจำตัวของคุณเพื่อให้สามารถให้คะแนนข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="6ac3e-176">In a scenario where the data source is refreshed with new data to score, you need to update your credentials so the data can be scored.</span></span> 

<span data-ttu-id="6ac3e-177">ในพื้นที่ทำงานของฉันในบริการ Power BI ในแถบส่วนหัวสีดำ ให้เลือก **ตัวเลือกเพิ่มเติม (...)**  > **การตั้งค่า** > **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-177">In My Workspace in the Power BI service, in the black header bar, select **More options (...)** > **Settings** > **Settings**.</span></span>

:::image type="content" source="media/service-aml-integrate/settings-pbi.png" alt-text="สกรีนช็อตที่แสดงการตั้งค่า":::

<span data-ttu-id="6ac3e-179">เลือก **ชุดข้อมูล** ขยาย **ข้อมูลประจำตัวแหล่งข้อมูล** จากนั้นเลือก **แก้ไขข้อมูลประจำตัว**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-179">Select **Datasets**, expand **Data source credentials**, then select **Edit Credentials**.</span></span>

:::image type="content" source="media/service-aml-integrate/data-refresh.png" alt-text="สกรีนช็อตที่แสดงการรีเฟรชข้อมูลประจำตัว":::

<span data-ttu-id="6ac3e-181">ทำตามคำแนะนำสำหรับทั้ง **azureMLFunctions** และ **เว็บ**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-181">Follow the instructions for both **azureMLFunctions** and **Web**.</span></span> <span data-ttu-id="6ac3e-182">ตรวจสอบให้แน่ใจว่าคุณเลือกระดับความเป็นส่วนตัวแล้ว</span><span class="sxs-lookup"><span data-stu-id="6ac3e-182">Make sure that you select a privacy level.</span></span> <span data-ttu-id="6ac3e-183">ขณะนี้คุณสามารถตั้งค่า **การรีเฟรชที่ตั้งกำหนดการแล้ว** ของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6ac3e-183">You can now set a **Scheduled refresh** of the data.</span></span> <span data-ttu-id="6ac3e-184">เลือก **ความถี่การรีเฟรช** และ **โซนเวลา**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-184">Select a **Refresh frequency** and **Time zone**.</span></span> <span data-ttu-id="6ac3e-185">นอกจากนี้ คุณสามารถเลือกอีเมลแอดเดรสที่ Power BI สามารถส่งการแจ้งเตือนความล้มเหลวการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="6ac3e-185">You can also select an email address where Power BI can send refresh failure notifications.</span></span>

:::image type="content" source="media/service-aml-integrate/schedule-refresh.png" alt-text="สกรีนช็อตที่แสดงชุดข้อมูลและการรีเฟรชการให้คะแนน":::

<span data-ttu-id="6ac3e-187">เลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-187">Select **Apply**.</span></span>

>[!NOTE]
> <span data-ttu-id="6ac3e-188">เมื่อมีการรีเฟรชข้อมูล จะมีการส่งข้อมูลไปยังจุดสิ้นสุด Azure Machine Learning ของคุณสำหรับการให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="6ac3e-188">When the data is refreshed, it also sends the data to your Azure Machine Learning endpoint for scoring.</span></span>

## <a name="clean-up-resources"></a><span data-ttu-id="6ac3e-189">ล้างแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6ac3e-189">Clean up resources</span></span>

>[!IMPORTANT]
><span data-ttu-id="6ac3e-190">คุณสามารถใช้ทรัพยากรที่คุณสร้างขึ้นเป็นข้อกำหนดเบื้องต้นสำหรับบทช่วยสอน Azure Machine Learning และบทความเกี่ยวกับวิธีการอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="6ac3e-190">You can use the resources that you created as prerequisites for other Azure Machine Learning tutorials and how-to articles.</span></span>

<span data-ttu-id="6ac3e-191">หากคุณไม่ได้วางแผนที่จะใช้ทรัพยากรที่คุณสร้างขึ้น ให้ลบทรัพยากรออกเพื่อที่คุณจะไม่ต้องเสียค่าบริการใดๆ</span><span class="sxs-lookup"><span data-stu-id="6ac3e-191">If you don't plan to use the resources that you created, delete them so you don't incur any charges.</span></span>

1. <span data-ttu-id="6ac3e-192">ในพอร์ทัล Azure ให้เลือก **กลุ่มทรัพยากร** ทางด้านซ้ายสุด</span><span class="sxs-lookup"><span data-stu-id="6ac3e-192">In the Azure portal, select **Resource groups** on the far left.</span></span>
 
1. <span data-ttu-id="6ac3e-193">จากรายการ ให้เลือกกลุ่มทรัพยากรที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6ac3e-193">From the list, select the resource group that you created.</span></span>

1. <span data-ttu-id="6ac3e-194">เลือก **ลบกลุ่มทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-194">Select **Delete resource group**.</span></span>

   ![สกรีนช็อตของการเลือกเพื่อลบกลุ่มทรัพยากรในพอร์ทัล Azure](./media/service-aml-integrate/delete-resources.png)

1. <span data-ttu-id="6ac3e-196">ใส่ชื่อกลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="6ac3e-196">Enter the resource group name.</span></span> <span data-ttu-id="6ac3e-197">จากนั้นเลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="6ac3e-197">Then select **Delete**.</span></span>
1. <span data-ttu-id="6ac3e-198">ในพื้นที่ทำงานของฉันในบริการ Power BI ให้ลบรายงานและชุดข้อมูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="6ac3e-198">In My Workspace in the Power BI service, delete the report and the related dataset.</span></span> <span data-ttu-id="6ac3e-199">คุณไม่จำเป็นต้องลบ Power BI Desktop หรือรายงานในคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6ac3e-199">You don't need to delete Power BI Desktop or the report on your computer.</span></span> <span data-ttu-id="6ac3e-200">Power BI Desktop ฟรี</span><span class="sxs-lookup"><span data-stu-id="6ac3e-200">Power BI Desktop is free.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6ac3e-201">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="6ac3e-201">Next steps</span></span>

<span data-ttu-id="6ac3e-202">ในชุดบทช่วยสอนนี้ คุณจะได้เรียนรู้วิธีตั้งค่ากำหนดการใน Power BI เพื่อให้สามารถให้คะแนนข้อมูลใหม่ได้จากจุดสิ้นสุดการให้คะแนนของคุณใน Azure Machine Learning</span><span class="sxs-lookup"><span data-stu-id="6ac3e-202">In this tutorial series, you learnt how to set up a schedule in Power BI so that new data can be scored by your scoring endpoint in Azure Machine Learning.</span></span>
