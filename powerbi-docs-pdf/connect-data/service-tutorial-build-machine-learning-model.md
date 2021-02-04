---
title: 'บทช่วยสอน: สร้างแบบจำลอง Machine Learning ใน Power BI'
description: ในบทช่วยสอนนี้ คุณสร้างแบบจำลอง Machine Learning Studio ใน Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.custom: connect-to-services
ms.topic: tutorial
ms.date: 08/03/2020
LocalizationGroup: Connect to services
ms.openlocfilehash: 31b56f4888393c12f94eb4e6d8f819d992a04029
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96392355"
---
# <a name="tutorial-build-a-machine-learning-model-in-power-bi"></a><span data-ttu-id="db60b-103">บทช่วยสอน: สร้างแบบจำลอง Machine Learning ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="db60b-103">Tutorial: Build a Machine Learning model in Power BI</span></span>

<span data-ttu-id="db60b-104">ในบทความการบทช่วยสอนนี้คุณใช้ **Machine Learning อัตโนมัติ** เพื่อสร้างและใช้แบบจำลองการคาดการณ์ไบนารีใน Power BI</span><span class="sxs-lookup"><span data-stu-id="db60b-104">In this tutorial article, you use **Automated Machine Learning** to create and apply a binary prediction model in Power BI.</span></span> <span data-ttu-id="db60b-105">บทช่วยสอนประกอบด้วยคำแนะนำสำหรับการสร้าง Power BI dataflow และการใช้เอนทิตีที่กำหนดไว้ใน dataflow เพื่อฝึกและตรวจสอบแบบจำลองการเรียนรู้ของเครื่องได้โดยตรงใน Power BI</span><span class="sxs-lookup"><span data-stu-id="db60b-105">The tutorial includes guidance for creating a Power BI dataflow, and using the entities defined in the dataflow to train and validate a machine learning model directly in Power BI.</span></span> <span data-ttu-id="db60b-106">จากนั้นเราใช้แบบจำลองดังกล่าวสำหรับการให้คะแนนข้อมูลใหม่เพื่อสร้างการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="db60b-106">We then use that model for scoring new data to generate predictions.</span></span>

<span data-ttu-id="db60b-107">ก่อนอื่นคุณจะสร้างเครื่องแบบจำลองการเรียนรู้ไบนารีเพื่อคาดการณ์การซื้อของนักช็อปออนไลน์ที่ยึดตามชุดของแอตทริบิวต์เซสชันออนไลน์ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="db60b-107">First, you'll create a Binary Prediction machine learning model, to predict the purchase intent of online shoppers based on a set of their online session attributes.</span></span> <span data-ttu-id="db60b-108">ชุดข้อมูลการเรียนรู้ของเครื่อง benchmark ที่ใช้สำหรับการดำเนินการนี้</span><span class="sxs-lookup"><span data-stu-id="db60b-108">A benchmark machine learning dataset is used for this exercise.</span></span> <span data-ttu-id="db60b-109">เมื่อแบบจำลองได้รับการฝึกใช้งานแล้ว Power BI จะสร้างรายงานการตรวจสอบความถูกต้องโดยอัตโนมัติเพื่ออธิบายผลลัพธ์แบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="db60b-109">Once a model is trained, Power BI will automatically generate a validation report explaining the model results.</span></span> <span data-ttu-id="db60b-110">จากนั้นคุณสามารถตรวจสอบรายงานการตรวจสอบความถูกต้องและนำรูปแบบไปใช้กับข้อมูลของคุณสำหรับการให้คะแนนได้</span><span class="sxs-lookup"><span data-stu-id="db60b-110">You can then review the validation report and apply the model to your data for scoring.</span></span>

<span data-ttu-id="db60b-111">บทช่วยสอนนี้ประกอบด้วยขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="db60b-111">This tutorial consists of following steps:</span></span>
> [!div class="checklist"]

> * <span data-ttu-id="db60b-112">สร้างกระแสข้อมูลด้วยข้อมูลป้อนเข้า</span><span class="sxs-lookup"><span data-stu-id="db60b-112">Create a dataflow with the input data</span></span>
> * <span data-ttu-id="db60b-113">สร้างและฝึกอบรมโมเดลการเรียนรู้ของเครื่อง</span><span class="sxs-lookup"><span data-stu-id="db60b-113">Create and train a machine learning model</span></span>
> * <span data-ttu-id="db60b-114">ตรวจทานรายงานการตรวจสอบความถูกต้องของแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="db60b-114">Review the model validation report</span></span>
> * <span data-ttu-id="db60b-115">นำแบบจำลองไปใช้กับเอนทิตีกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="db60b-115">Apply the model to a dataflow entity</span></span>
> * <span data-ttu-id="db60b-116">การใช้ผลลัพธ์ที่ได้จากแบบจำลองในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="db60b-116">Using the scored output from the model in a Power BI report</span></span>

## <a name="create-a-dataflow-with-the-input-data"></a><span data-ttu-id="db60b-117">สร้างกระแสข้อมูลด้วยข้อมูลป้อนเข้า</span><span class="sxs-lookup"><span data-stu-id="db60b-117">Create a dataflow with the input data</span></span>

<span data-ttu-id="db60b-118">ส่วนแรกของบทช่วยสอนนี้สร้างกระแสข้อมูลด้วยข้อมูลนำเข้า</span><span class="sxs-lookup"><span data-stu-id="db60b-118">The first part of this tutorial is to create a dataflow with input data.</span></span> <span data-ttu-id="db60b-119">กระบวนการดังกล่าวใช้เวลาสองถึงสามขั้นตอนดังที่แสดงในส่วนต่อไปนี้โดยเริ่มต้นด้วยการรับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="db60b-119">That process takes a few steps, as shown in the following sections, beginning with getting data.</span></span>

### <a name="get-data"></a><span data-ttu-id="db60b-120">รับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="db60b-120">Get data</span></span>

<span data-ttu-id="db60b-121">ขั้นตอนแรกในการสร้างกระแสข้อมูล คือการให้แหล่งข้อมูลของคุณให้พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="db60b-121">The first step in creating a dataflow is to have your data sources ready.</span></span> <span data-ttu-id="db60b-122">ในกรณีของเราเราใช้ชุดข้อมูลการเรียนรู้ของเครื่องจากชุดของเซสชันออนไลน์ซึ่งบางส่วนถึงขั้นตอนสุดท้ายของการซื้อ</span><span class="sxs-lookup"><span data-stu-id="db60b-122">In our case, we use a machine learning dataset from a set of online sessions, some of which culminated in a purchase.</span></span> <span data-ttu-id="db60b-123">ชุดข้อมูลประกอบด้วยชุดของแอตทริบิวต์เกี่ยวกับเซสชันเหล่านี้ซึ่งเราจะใช้สำหรับการฝึกแบบจำลองของเรา</span><span class="sxs-lookup"><span data-stu-id="db60b-123">The dataset contains a set of attributes about these sessions, which we'll use for training our model.</span></span>

<span data-ttu-id="db60b-124">คุณสามารถดาวน์โหลดชุดข้อมูลจากเว็บไซต์ UC เออร์ไวน์ได้</span><span class="sxs-lookup"><span data-stu-id="db60b-124">You can download the dataset from the UC Irvine website.</span></span> <span data-ttu-id="db60b-125">นอกจากนี้เรายังมีการใช้งาน UC เออร์ไวน์เพื่อเป็นวัตถุประสงค์ของบทช่วยสอนนี้จากการเชื่อมโยงต่อไปนี้:[ online_shoppers_intention.csv](https://raw.githubusercontent.com/santoshc1/PowerBI-AI-samples/master/Tutorial_AutomatedML/online_shoppers_intention.csv)</span><span class="sxs-lookup"><span data-stu-id="db60b-125">We also have this available, for the purpose of this tutorial, from the following link: [online_shoppers_intention.csv](https://raw.githubusercontent.com/santoshc1/PowerBI-AI-samples/master/Tutorial_AutomatedML/online_shoppers_intention.csv).</span></span>

### <a name="create-the-entities"></a><span data-ttu-id="db60b-126">สร้างเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="db60b-126">Create the entities</span></span>

<span data-ttu-id="db60b-127">หากต้องสร้างเอนทิตีในกระแสข้อมูลของคุณ ให้ลงชื่อเข้าใช้บริการของ Power BI และนำทางไปยังพื้นที่ทำงานบนความจุของคุณที่มี AI เปิดการใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="db60b-127">To create the entities in your dataflow, sign into the Power BI service and navigate to a workspace on your capacity that has AI enabled.</span></span>

<span data-ttu-id="db60b-128">หากคุณยังไม่มีพื้นที่ทำงาน คุณสามารถสร้างได้โดยเลือก **พื้นที่ทำงาน** ในหน้าต่างนำทางในบริการ Power BI แล้วเลือก **สร้างพื้นที่ทำงาน** ในบานหน้าต่างด้านล่างที่ปรากฏ</span><span class="sxs-lookup"><span data-stu-id="db60b-128">If you don't already have a workspace, you can create one by selecting **Workspaces** in the nav pane menu in the Power BI service, and select **Create workspace** at the bottom of the panel that appears.</span></span> <span data-ttu-id="db60b-129">ซึ่งจะเปิดแผงทางด้านขวาเพื่อป้อนรายละเอียดพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="db60b-129">This opens a panel on the right to enter the workspace details.</span></span> <span data-ttu-id="db60b-130">ป้อนชื่อพื้นที่ทำงาน และเลือก **ขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="db60b-130">Enter a workspace name and select **Advanced**.</span></span> <span data-ttu-id="db60b-131">ยืนยันว่าพื้นที่ทำงานใช้ความจุเฉพาะโดยใช้ปุ่มเรดิโอและกำหนดให้กับอินสแตนซ์ความจุที่มีการเปิดใช้งานการแสดงตัวอย่าง AI</span><span class="sxs-lookup"><span data-stu-id="db60b-131">Confirm that the workspace uses Dedicated Capacity using the radio button, and that it's assigned to a capacity instance that has the AI preview turned on.</span></span> <span data-ttu-id="db60b-132">จากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="db60b-132">Then select **Save**.</span></span>

![สร้างพื้นที่ทำงาน](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-01.png)

<span data-ttu-id="db60b-134">เมื่อสร้างพื้นที่ทำงานแล้ว คุณสามารถเลือก **ข้าม** ที่ด้านขวาล่างของหน้าจอต้อนรับตามที่แสดงในภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="db60b-134">Once the workspace is created, you can select **Skip** in the bottom right of the Welcome screen, as shown in the following image.</span></span>

![ข้ามถ้าคุณมีพื้นที่ทำงานอยู่แล้ว](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-02.png)

 <span data-ttu-id="db60b-136">เลือกปุ่ม **สร้าง** ที่ด้านขวาบนของพื้นที่ทำงาน และเลือก **กระแสข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="db60b-136">Select the **Create** button at the top right of the workspace, and then select **Dataflow**.</span></span>

![สร้างกระแสข้อมูล](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-03.png)

<span data-ttu-id="db60b-138">เลือก **เอนทิตีใหม่**</span><span class="sxs-lookup"><span data-stu-id="db60b-138">Select **Add new entities**.</span></span> <span data-ttu-id="db60b-139">การดำเนินการนี้จะเป็นการเปิดใช้งานตัวแก้ไข **Power Query** ในเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="db60b-139">This launches a **Power Query** editor in the browser.</span></span>

![เพิ่มเอนทิตีใหม่](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-04.png)

<span data-ttu-id="db60b-141">เลือกไฟล์ **ข้อความ/CSV** เป็นแหล่งข้อมูลที่แสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="db60b-141">Select **Text/CSV File** as a data source, shown in the following image.</span></span>

![เลือกไฟล์ข้อความ/CSF](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-05.png)

<span data-ttu-id="db60b-143">ในหน้า **เชื่อมต่อกับแหล่งข้อมูล** ที่ปรากฏถัดไป วางลิงก์ต่อไปนี้ไปยัง _online_shoppers_intention.csv_ ลงในกล่องของ **ไฟล์พาธหรือ URL** แล้วเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="db60b-143">In the **Connect to a data source** page that appears next, paste the following link to the _online_shoppers_intention.csv_ into the **File path or URL** box, and then select **Next**.</span></span>

`https://raw.githubusercontent.com/santoshc1/PowerBI-AI-samples/master/Tutorial_AutomatedML/online_shoppers_intention.csv`

![เส้นทางไฟล์](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-06.png)

<span data-ttu-id="db60b-145">ตัวแก้ไข Power Query จะแสดงตัวอย่างของข้อมูลจากไฟล์ CSV</span><span class="sxs-lookup"><span data-stu-id="db60b-145">The Power Query Editor shows a preview of the data from the CSV file.</span></span> <span data-ttu-id="db60b-146">คุณสามารถเปลี่ยนชื่อคิวรีให้เป็นชื่อเรียกง่ายขึ้นได้โดยการเปลี่ยนแปลงค่าในกล่องชื่อที่พบในบานหน้าต่างด้านขวา</span><span class="sxs-lookup"><span data-stu-id="db60b-146">You can rename the query to a friendlier name by changing the value in the Name box found in the right pane.</span></span> <span data-ttu-id="db60b-147">ตัวอย่างเช่น คุณสามารถเปลี่ยนชื่อคิวรีเป็น _ผู้เยี่ยมชมออนไลน์_</span><span class="sxs-lookup"><span data-stu-id="db60b-147">For example, you could change the Query name to _Online Visitors_.</span></span>

![เปลี่ยนเป็นชื่อที่เรียกง่าย](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-07.png)

<span data-ttu-id="db60b-149">Power Query อ้างถึงชนิดของคอลัมน์โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="db60b-149">Power Query automatically infers the type of columns.</span></span> <span data-ttu-id="db60b-150">คุณสามารถเปลี่ยนชนิดคอลัมน์ได้โดยการคลิกที่ไอคอนชนิดแอตทริบิวต์ที่ด้านบนของส่วนหัวของคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="db60b-150">You can change the column type by clicking on the attribute type icon at the top of the column header.</span></span> <span data-ttu-id="db60b-151">ในตัวอย่างนี้ เราจะเปลี่ยนชนิดของคอลัมน์รายได้เป็น True/False</span><span class="sxs-lookup"><span data-stu-id="db60b-151">In this example, we change the type of the Revenue column to True/False.</span></span>

![เปลี่ยนชนิดข้อมูล](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-08.png)

<span data-ttu-id="db60b-153">เลือกปุ่ม **บันทึกและปิด** เพื่อปิดตัวแก้ไข Power Query</span><span class="sxs-lookup"><span data-stu-id="db60b-153">Select the **Save & close** button to close Power Query Editor.</span></span> <span data-ttu-id="db60b-154">ตั้งชื่อกระแสข้อมูล จากนั้นเลือก **บันทึก** ในกล่องตอบโต้ดังที่แสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="db60b-154">Provide a name for the dataflow, and then select **Save** on the dialog, as shown in the following image.</span></span>

![บันทึกกระแสข้อมูล](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-09.png)

## <a name="create-and-train-a-machine-learning-model"></a><span data-ttu-id="db60b-156">สร้างและฝึกอบรมโมเดลการเรียนรู้ของเครื่อง</span><span class="sxs-lookup"><span data-stu-id="db60b-156">Create and train a machine learning model</span></span>

<span data-ttu-id="db60b-157">หากต้องการเพิ่มแบบจำลองการเรียนรู้ของเครื่องให้เลือกปุ่ม **ใช้แบบจำลอง ML** ในรายการการ **ดำเนินการ** สำหรับเอนทิตีพื้นฐานที่ประกอบด้วยข้อมูลการฝึกอบรมและข้อมูลป้ายชื่อของคุณจากนั้นเลือก **เพิ่ม แบบจำลองการเรียนรู้ของเครื่อง**</span><span class="sxs-lookup"><span data-stu-id="db60b-157">To add a machine learning model, Select the **Apply ML model** button in the **Actions** list for the base entity that contains your training data and label information, and then select **Add a machine learning model**.</span></span>

![เพิ่มแบบจำลองการเรียนรู้ของเครื่อง](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-10.png)

<span data-ttu-id="db60b-159">ขั้นตอนแรกในการสร้างแบบจำลองการเรียนรู้ของเครื่องของเราคือการระบุข้อมูลในอดีตซึ่งรวมถึงเขตข้อมูลผลลัพธ์ที่คุณต้องการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="db60b-159">The first step for creating our machine learning model is to identify the historical data including the outcome field that you want to predict.</span></span> <span data-ttu-id="db60b-160">แบบจำลองจะถูกสร้างขึ้นโดยการเรียนรู้จากข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="db60b-160">The model will be created by learning from this data.</span></span>

<span data-ttu-id="db60b-161">ในกรณีของชุดข้อมูลที่เรากำลังใช้นี่คือเขตข้อมูล **รายได้**</span><span class="sxs-lookup"><span data-stu-id="db60b-161">In the case of the dataset we're using, this is the **Revenue** field.</span></span> <span data-ttu-id="db60b-162">เลือก **รายได้** เป็นค่า ' เขตข้อมูลผลลัพธ์' จากนั้นเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="db60b-162">Select **Revenue** as the 'Outcome field' value and then select **Next**.</span></span>

![เลือกข้อมูลในอดีต](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-11.png)

<span data-ttu-id="db60b-164">จากนั้น เราจะต้องเลือกชนิดของแบบจำลองการเรียนรู้ของเครื่องที่จะสร้าง</span><span class="sxs-lookup"><span data-stu-id="db60b-164">Next, we must select the type of machine learning model to create.</span></span> <span data-ttu-id="db60b-165">Power BI วิเคราะห์ค่าในเขตข้อมูลผลลัพธ์ที่คุณระบุและแนะนำชนิดของแบบจำลองการเรียนรู้ของเครื่องที่สามารถสร้างขึ้นเพื่อคาดการณ์เขตข้อมูลนั้นได้</span><span class="sxs-lookup"><span data-stu-id="db60b-165">Power BI analyzes the values in the outcome field that you've identified and suggests the types of machine learning models that can be created to predict that field.</span></span>

<span data-ttu-id="db60b-166">ในกรณีนี้เนื่องจากเรากำลังคาดคะเนผลลัพธ์ไบนารีว่าผู้ใช้จะทำการซื้อหรือไม่ ขอแนะนำให้ใช้การคาดการณ์ไบนารี</span><span class="sxs-lookup"><span data-stu-id="db60b-166">In this case since we're predicting a binary outcome of whether a user will make a purchase or not, Binary Prediction is recommended.</span></span> <span data-ttu-id="db60b-167">เนื่องจากเรามีความสนใจในการคาดการณ์ผู้ใช้ที่จะทำการซื้อ ให้เลือก True เป็นผลลัพธ์ด้านรายได้ที่คุณสนใจมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="db60b-167">Since we are interested in predicting users who will make a purchase, select True as the Revenue outcome that you're most interested in.</span></span> <span data-ttu-id="db60b-168">นอกจากนี้ คุณสามารถกำหนดป้ายชื่อที่เรียกง่ายสำหรับผลลัพธ์ที่จะใช้ในรายงานที่สร้างขึ้นโดยอัตโนมัติ ซึ่งจะสรุปผลลัพธ์ของการตรวจสอบแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="db60b-168">Additionally, you can provide friendly labels for the outcomes to be used in the automatically generated report that will summarize the results of the model validation.</span></span> <span data-ttu-id="db60b-169">จากนั้นเลือกถัดไป</span><span class="sxs-lookup"><span data-stu-id="db60b-169">Then select Next.</span></span>

![เลือกการคาดการณ์ไบนารีแล้ว](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-12.png)

<span data-ttu-id="db60b-171">ถัดไป Power BI จะทำการสแกนตัวอย่างข้อมูลเบื้องต้น และแนะนำการป้อนค่าที่อาจสร้างการคาดการณ์ที่ถูกต้องมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="db60b-171">Next, Power BI does a preliminary scan of a sample of your data and suggests the inputs that may produce more accurate predictions.</span></span> <span data-ttu-id="db60b-172">ถ้า Power BI ไม่แนะนำเขตข้อมูล จะมีการกำหนดคำอธิบายไว้ข้าง ๆ</span><span class="sxs-lookup"><span data-stu-id="db60b-172">If Power BI doesn't recommend a field, an explanation would be provided next to it.</span></span> <span data-ttu-id="db60b-173">คุณมีตัวเลือกในการเปลี่ยนการเลือกเพื่อรวมเฉพาะเขตข้อมูลที่คุณต้องการให้แบบจำลองศึกษา หรือคุณสามารถเลือกเขตข้อมูลทั้งหมดโดยเลือกกล่องกาเครื่องหมายถัดจากชื่อเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="db60b-173">You have the option to change the selections to include only the fields you want the model to study, or you can select all the fields by selecting the checkbox next to the entity name.</span></span> <span data-ttu-id="db60b-174">เลือก **ถัดไป** เพื่อยอมรับข้อมูลป้อนเข้า</span><span class="sxs-lookup"><span data-stu-id="db60b-174">Select **Next** to accept the inputs.</span></span>

![เลือกกล่องกาเครื่องหมายถัดไป](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-13.png)

<span data-ttu-id="db60b-176">ในขั้นตอนสุดท้าย เราต้องใส่ชื่อสำหรับแบบจำลองของเรา</span><span class="sxs-lookup"><span data-stu-id="db60b-176">In the final step, we must provide a name for our model.</span></span> <span data-ttu-id="db60b-177">ตั้งชื่อแบบจำลอง _การคาดการณ์จุดประสงค์ในการซื้อไปใช้_</span><span class="sxs-lookup"><span data-stu-id="db60b-177">Name the model _Purchase Intent Prediction_.</span></span> <span data-ttu-id="db60b-178">คุณสามารถเลือกที่จะลดเวลาการฝึกเพื่อดูผลลัพธ์อย่างรวดเร็วหรือเพิ่มระยะเวลาที่ใช้ในการฝึกเพื่อให้ได้แบบจำลองที่ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="db60b-178">You can choose to reduce the training time to see quick results or increase the amount of time spent in training to get the best model.</span></span> <span data-ttu-id="db60b-179">จากนั้นเลือก **บันทึกและฝึก** เพื่อเริ่มต้นการฝึกแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="db60b-179">Then select **Save and train** to start training the model.</span></span>

![บันทึกแบบจำลอง](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-14.png)

<span data-ttu-id="db60b-181">กระบวนการฝึกอบรมจะเริ่มต้นด้วยการสุ่มตัวอย่างและ normalizing ข้อมูลในอดีตของคุณและแยกชุดข้อมูลของคุณลงในสองเอนทิตีใหม่ _การซื้อการคาดการณ์การดำเนินการ_ และ _การทดสอบการคาดการณ์เจตนาการซื้อข้อมูล_ ได้</span><span class="sxs-lookup"><span data-stu-id="db60b-181">The training process will begin by sampling and normalizing your historical data and splitting your dataset into two new entities _Purchase Intent Prediction Training Data_ and _Purchase Intent Prediction Testing Data_.</span></span>

<span data-ttu-id="db60b-182">ทั้งขึ้นอยู่กับขนาดของชุดข้อมูล กระบวนการฝึกอบรมสามารถใช้ที่ใดก็ได้จากไม่กี่นาทีจนถึงเวลาการฝึกอบรมที่เลือกในหน้าจอก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="db60b-182">Depending on the size of the dataset, the training process can take anywhere from a few minutes to the training time selected at the previous screen.</span></span> <span data-ttu-id="db60b-183">ในขั้นตอนนี้คุณสามารถดูแบบจำลองในแท็บ **แบบจำลองการเรียนรู้ของเครื่อง** ของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="db60b-183">At this point, you can see the model in the **Machine learning models** tab of the dataflow.</span></span> <span data-ttu-id="db60b-184">สถานะพร้อมแล้วแสดงว่าแบบจำลองได้รับการจัดคิวสำหรับการฝึกหรืออยู่ระหว่างการฝึก</span><span class="sxs-lookup"><span data-stu-id="db60b-184">The Ready status indicates that the model has been queued for training or is under training.</span></span>

<span data-ttu-id="db60b-185">คุณสามารถยืนยันว่าแบบจำลองกำลังได้รับการฝึกและผ่านการตรวจสอบความถูกต้องผ่านสถานะของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="db60b-185">You can confirm that the model is being trained and validated through the status of the dataflow.</span></span> <span data-ttu-id="db60b-186">การดำเนินการนี้จะปรากฏขึ้นเป็นการรีเฟรชข้อมูลในแท็บ **กระแสข้อมูล** ของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="db60b-186">This appears as a data refresh in progress in the **Dataflows** tab of the workspace.</span></span>

![พร้อมสำหรับการฝึก](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-15.png)

<span data-ttu-id="db60b-188">เมื่อการฝึกแบบจำลองเสร็จสมบูรณ์กระแสข้อมูล จะแสดงเวลาการรีเฟรชที่อัปเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="db60b-188">Once the model training is completed, the dataflow displays an updated refresh time.</span></span> <span data-ttu-id="db60b-189">คุณสามารถยืนยันว่าแบบจำลองได้รับการฝึกแล้วโดยการนำทางไปยังแท็บ **แบบจำลองการเรียนรู้ของเครื่อง** ในกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="db60b-189">You can confirm that the model is trained, by navigating to the **Machine learning models** tab in the dataflow.</span></span> <span data-ttu-id="db60b-190">แบบจำลองที่คุณสร้างขึ้นควรแสดงสถานะเป็น **ฝึกแล้ว** และ **เวลาที่ฝึกครั้งล่าสุด** ควรได้รับการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="db60b-190">The model you created should show status as **Trained** and the **Last Trained time** should now be updated.</span></span>

![ฝึกแบบจำลองล่าสุดเมื่อ](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-16.png)

## <a name="review-the-model-validation-report"></a><span data-ttu-id="db60b-192">ตรวจทานรายงานการตรวจสอบความถูกต้องของแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="db60b-192">Review the model validation report</span></span>
<span data-ttu-id="db60b-193">หากต้องการตรวจสอบรายงานการตรวจสอบความถูกต้องของแบบจำลองในแท็บแบบจำลองการเรียนรู้ของเครื่อง ให้เลือกปุ่มรายงานการฝึกในคอลัมน์การดำเนินการสำหรับแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="db60b-193">To review the model validation report, in the Machine learning models tab, select the View training report button in the Actions column for the model.</span></span> <span data-ttu-id="db60b-194">รายงานนี้จะอธิบายวิธีการแบบจำลองการเรียนรู้ของเครื่องของคุณมีแนวโน้มที่จะดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="db60b-194">This report describes how your machine learning model is likely to perform.</span></span>

<span data-ttu-id="db60b-195">ในหน้า **ประสิทธิภาพของแบบจำลอง** ของรายงาน ให้เลือก **ตัวคาดการณ์ยอดนิยม** เพื่อดูตัวคาดการณ์ยอดนิยมสำหรับแบบจำลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="db60b-195">In the **Model Performance** page of the report, select See **top predictors** to view the top predictors for your model.</span></span> <span data-ttu-id="db60b-196">คุณสามารถเลือกหนึ่งในตัวคาดการณ์เพื่อดูว่าการกระจายผลลัพธ์เกี่ยวข้องกับตัวคาดการณ์นั้นได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="db60b-196">You can select one of the predictors to see how the outcome distribution is associated with that predictor.</span></span>

![ประสิทธิภาพของแบบจำลอง](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-17.png)

<span data-ttu-id="db60b-198">คุณสามารถใช้ตัวแบ่งส่วน **ขีดจำกัดความน่าจะเป็น** บนหน้าประสิทธิภาพของแบบจำลองเพื่อตรวจสอบอิทธิพลของความแม่นยำและการเรียกคืนสำหรับแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="db60b-198">You can use the **Probability Threshold** slicer on the Model Performance page to examine its influence on the Precision and Recall for the model.</span></span>

![ค่าเกณฑ์ของความน่าเป็น](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-18.png)

<span data-ttu-id="db60b-200">หน้าอื่นๆของรายงานอธิบายเมตริกประสิทธิภาพเชิงสถิติสำหรับแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="db60b-200">The other pages of the report describe the statistical performance metrics for the model.</span></span>

<span data-ttu-id="db60b-201">รายงานยังรวมถึงหน้ารายละเอียดการฝึกอบรมที่อธิบายการเกิดซ้ำต่างๆที่มีการเรียกใช้วิธีการแยกลักษณะการทำงานออกจากอินพุทและ hyperparameters สำหรับแบบจำลองขั้นสุดท้ายที่ใช้</span><span class="sxs-lookup"><span data-stu-id="db60b-201">The report also includes a Training Details page that describes the different iterations that were run, how features were extracted from the inputs, and the hyperparameters for the final model used.</span></span>

## <a name="apply-the-model-to-a-dataflow-entity"></a><span data-ttu-id="db60b-202">นำแบบจำลองไปใช้กับเอนทิตีกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="db60b-202">Apply the model to a dataflow entity</span></span>

<span data-ttu-id="db60b-203">เลือกปุ่ม **ใช้แบบจำลอง** ที่ด้านบนของรายงานเพื่อเรียกแบบจำลองนี้</span><span class="sxs-lookup"><span data-stu-id="db60b-203">Select the **Apply model** button at the top of the report to invoke this model.</span></span> <span data-ttu-id="db60b-204">ในกล่องโต้ตอบ **นำไปใช้** คุณสามารถระบุเอนทิตีเป้าหมายที่มีข้อมูลต้นทางที่ควรใช้แบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="db60b-204">In the **Apply** dialog, you can specify the target entity that has the source data to which the model should be applied.</span></span>

![นำแบบจำลองไปใช้](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-19.png)

<span data-ttu-id="db60b-206">เมื่อได้รับพร้อมท์คุณจะต้อง **รีเฟรช** กระแสข้อมูล เพื่อแสดงตัวอย่างผลลัพธ์ของแบบจำลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="db60b-206">When prompted, you must **Refresh** the dataflow to preview the results of your model.</span></span>

<span data-ttu-id="db60b-207">การใช้แบบจำลองจะสร้างเอนทิตีใหม่สองตัวที่มีส่วนต่อท้าย  **<model_name> ที่สมบูรณ์** และ **คำอธิบาย <model_name> ที่สมบูรณ์**.</span><span class="sxs-lookup"><span data-stu-id="db60b-207">Applying the model will create two new entities, with the suffix **enriched <model_name>** and **enriched <model_name> explanations**.</span></span> <span data-ttu-id="db60b-208">ในกรณีของเรา การนำแบบจำลองไปใช้กับเอนทิตีของ **ผู้เยี่ยมชม ออนไลน์** จะสร้าง **การคาดการณ์จุดประสงค์ในการซื้อที่สมบูรณ์ของผู้เยี่ยมชมออนไลน์** ซึ่งรวมถึงผลลัพธ์ที่คาดการณ์จากแบบจำลอง และ **คำอธิบายการคาดการณ์จุดประสงค์ในการซื้อที่สมบูรณ์ของผู้เยี่ยมชมออนไลผู้เยี่ยมชมออนไลน์** ซึ่งประกอบด้วยอิทธิพลที่เฉพาะเจาะจงของไฟล์ข้อมูลสำหรับการคาดการณ์.</span><span class="sxs-lookup"><span data-stu-id="db60b-208">In our case, applying the model to the **Online Visitors** entity will create **Online Visitors enriched Purchase Intent Prediction** which includes the predicted output from the model, and **Online Visitors enriched Purchase Intent Prediction explanations** which contains top record-specific influencers for the prediction.</span></span> 

<span data-ttu-id="db60b-209">การใช้แบบจำลองการคาดการณ์ไบนารีจะเพิ่มคอลัมน์ที่สี่ที่มีผลลัพธ์ที่คาดการณ์ คะแนนความน่าจะเป็น อิทธิพลที่เฉพาะเจาะจงของไฟล์ข้อมูล และดัชนีคำอธิบายสำหรับการคาดการณ์ ซึ่งแต่ละคอลัมน์จะขึ้นต้นด้วยชื่อคอลัมน์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="db60b-209">Applying a Binary Prediction model adds four columns with predicted outcome, probability score, the top record-specific influencers for the prediction, and explanation index each prefixed with the column name specified.</span></span>  

![สามคอลัมน์ของผลลัพธ์](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-20.png)

<span data-ttu-id="db60b-211">เมื่อรีเฟรชกระแสข้อมูลเสร็จสมบูรณ์ คุณสามารถเลือกเอนทิตี **การคาดการณ์จุดประสงค์ในการสั่งซื้อที่สมบูรณ์ของผู้เยี่ยมชมออนไลน์** เพื่อดูผลลัพธ์ได้</span><span class="sxs-lookup"><span data-stu-id="db60b-211">Once the dataflow refresh is completed, you can select the **Online Visitors enriched Purchase Intent Prediction** entity to view the results.</span></span>

![ดูผลลัพธ์](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-21.png)

<span data-ttu-id="db60b-213">คุณยังสามารถเรียกใช้แบบจำลอง AutoML ในพื้นที่ทำงานได้โดยตรงจากตัวแก้ไข Power Query ในกระแสข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="db60b-213">You can also invoke any AutoML model in the workspace, directly from the Power Query Editor in your dataflow.</span></span> <span data-ttu-id="db60b-214">ในการเข้าถึงแบบจำลอง AutoML ให้เลือกปุ่มแก้ไขสำหรับเอนทิตีที่คุณต้องการเสริมด้วยข้อมูลเชิงลึกจากโมเดล AutoML ของคุณ ตามที่แสดงในภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="db60b-214">To access the AutoML models, select the Edit button for the entity that you want to enrich with insights from your AutoML model, as shown in the following image.</span></span>

![แก้ไขเอนทิตี](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-22.png)

<span data-ttu-id="db60b-216">การเลือกปุ่ม แก้ไข เพื่อเปิดตัวแก้ไข Power Query สำหรับเอนทิตีในกระแสข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="db60b-216">Selecting the Edit button opens the Power Query Editor for the entities in your dataflow.</span></span> <span data-ttu-id="db60b-217">เลือกปุ่ม AI Insights ใน Ribbon</span><span class="sxs-lookup"><span data-stu-id="db60b-217">Select the AI Insights button in the ribbon.</span></span>

![ข้อมูลเชิงลึกของ AI](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-23.png)

 <span data-ttu-id="db60b-219">เลือกโฟลเดอร์แบบจำลองการเรียนรู้ของเครื่อง Power BI จากเมนูบานหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="db60b-219">Select the Power BI Machine Learning Models folder from the nav pane menu.</span></span> <span data-ttu-id="db60b-220">แบบจำลอง AutoML ทั้งหมดที่คุณสามารถเข้าถึงจะแสดงรายการที่นี่โดยเป็นฟังก์ชัน Power Query</span><span class="sxs-lookup"><span data-stu-id="db60b-220">All the AutoML models to which you have access are listed here as Power Query functions.</span></span> <span data-ttu-id="db60b-221">นอกจากนี้พารามิเตอร์อินพุตสำหรับโมเดล AutoML จะถูกแมปโดยอัตโนมัติเป็นพารามิเตอร์ของฟังก์ชัน Power Query ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="db60b-221">Also, the input parameters for the AutoML model are automatically mapped as parameters of the corresponding Power Query function.</span></span> <span data-ttu-id="db60b-222">โปรดทราบว่าการแมปพารามิเตอร์อัตโนมัติจะเกิดขึ้นก็ต่อเมื่อชื่อและชนิดข้อมูลของพารามิเตอร์ที่เหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="db60b-222">Note that automatic mapping of parameters happens only if the name and data type of the parameter is the same.</span></span>
 
<span data-ttu-id="db60b-223">ในการเรียกใช้แบบจำลอง AutoML คุณสามารถระบุคอลัมน์ของเอนทิตีที่เลือกมาเป็นข้อมูลเข้าจากเมนูแบบเลื่อนลง</span><span class="sxs-lookup"><span data-stu-id="db60b-223">To invoke an AutoML model, you can specify any of the selected entity's columns as an input from the drop-down.</span></span> <span data-ttu-id="db60b-224">นอกจากนี้คุณยังสามารถระบุค่าคงที่เพื่อใช้เป็นข้อมูลป้อนเข้าได้ โดยสลับไอคอนคอลัมน์ไปทางซ้ายของกล่องโต้ตอบที่ป้อนเข้า</span><span class="sxs-lookup"><span data-stu-id="db60b-224">You can also specify a constant value to be used as an input by toggling the column icon to the left of the input dialog.</span></span>

![เบราว์เซอร์ฟังก์ชัน PQO](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-24.png)

<span data-ttu-id="db60b-226">เลือกนำไปใช้ เพื่อดูตัวอย่างผลลัพธ์ของแบบจำลอง AutoML ตามคอลัมน์ใหม่ในตารางเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="db60b-226">Select Apply to view the preview of the AutoML model's output as a new columns in the entity table.</span></span> <span data-ttu-id="db60b-227">นอกจากนี้คุณจะเห็นการเรียกแบบจำลองเป็นขั้นตอนที่นำไปใช้สำหรับคิวรี</span><span class="sxs-lookup"><span data-stu-id="db60b-227">You will also see the model invocation as an applied step for the query.</span></span>

![ดูผลลัพธ์](media/service-tutorial-build-machine-learning-model/tutorial-machine-learning-model-25.png)

<span data-ttu-id="db60b-229">เมื่อบันทึกกระแสข้อมูลของคุณแล้ว ระบบจะเรียกแบบจำลองโดยอัตโนมัติเมื่อมีการรีเฟรชกระแสข้อมูล สำหรับแถวใหม่หรือแถวที่ได้รับการอัปเดตใดๆ ในตารางเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="db60b-229">Once you save your dataflow, the model is automatically invoked when the dataflow is refreshed, for any new or updated rows in the entity table.</span></span>

## <a name="using-the-scored-output-from-the-model-in-a-power-bi-report"></a><span data-ttu-id="db60b-230">การใช้ผลลัพธ์ที่ได้จากแบบจำลองในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="db60b-230">Using the scored output from the model in a Power BI report</span></span>

<span data-ttu-id="db60b-231">ในการใช้ผลลัพธ์ที่ได้จากการเรียนรู้ของเครื่อง คุณสามารถเชื่อมต่อกับกระแสข้อมูลของคุณจาก Power BI desktop โดยใช้ตัวเชื่อมต่อกระแสข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="db60b-231">To use the scored output from your machine learning model you can connect to your dataflow from the Power BI desktop, using the Dataflows connector.</span></span> <span data-ttu-id="db60b-232">เอนทิตี **การคาดการณ์จุดประสงค์ในการซื้อของผู้เยี่ยมชมออนไลน์** สามารถใช้เพื่อรวมการคาดการณ์จากแบบจำลองของคุณในรายงาน Power BI ได้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="db60b-232">The **Online Visitors enriched Purchase Intent Prediction** entity can now be used to incorporate the predictions from your model in Power BI reports.</span></span>

## <a name="next-steps"></a><span data-ttu-id="db60b-233">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="db60b-233">Next steps</span></span>

<span data-ttu-id="db60b-234">ในบทช่วยสอนนี้คุณสร้างและนำไปใช้แบบจำลองการคาดการณ์ไบนารีใน Power BI โดยใช้ขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="db60b-234">In this tutorial, you created and applied a binary prediction model in Power BI using these steps:</span></span>

* <span data-ttu-id="db60b-235">สร้างกระแสข้อมูลด้วยข้อมูลป้อนเข้า</span><span class="sxs-lookup"><span data-stu-id="db60b-235">Create a dataflow with the input data</span></span>
* <span data-ttu-id="db60b-236">สร้างและฝึกอบรมโมเดลการเรียนรู้ของเครื่อง</span><span class="sxs-lookup"><span data-stu-id="db60b-236">Create and train a machine learning model</span></span>
* <span data-ttu-id="db60b-237">ตรวจทานรายงานการตรวจสอบความถูกต้องของแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="db60b-237">Review the model validation report</span></span>
* <span data-ttu-id="db60b-238">นำแบบจำลองไปใช้กับเอนทิตีกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="db60b-238">Apply the model to a dataflow entity</span></span>
* <span data-ttu-id="db60b-239">การใช้ผลลัพธ์ที่ได้จากแบบจำลองในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="db60b-239">Using the scored output from the model in a Power BI report</span></span>

<span data-ttu-id="db60b-240">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Machine Learning อัตโนมัติใน Power BI โปรดดูข้อมูลเกี่ยวกับ [ Machine Learning อัตโนมัติใน Power BI](../transform-model/dataflows/dataflows-machine-learning-integration.md)</span><span class="sxs-lookup"><span data-stu-id="db60b-240">For more information about Machine Learning automation in Power BI, see [Automated Machine Learning in Power BI](../transform-model/dataflows/dataflows-machine-learning-integration.md).</span></span>