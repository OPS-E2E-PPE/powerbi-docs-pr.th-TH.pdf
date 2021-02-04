---
title: สร้างการลงจุดแบบกรวยจากสคริปต์ R เป็นวิชวลแบบ R ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการสร้างแผนภูมิกรวยจากสคริปต์ R ไปยังวิชวล R Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: tutorial
ms.date: 04/02/2020
ms.openlocfilehash: f1f8c037a3ceb66d8ffb5abab6bccd4ec9bc7adc
ms.sourcegitcommit: a5e98bc86915f7bea6a0ab5df282683840e63d2c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/07/2021
ms.locfileid: "97969569"
---
# <a name="tutorial-build-a-funnel-plot-from-r-script-to-r-visual"></a><span data-ttu-id="eea92-104">บทช่วยสอน: สร้างแผนภูมิกรวยจากสคริปต์ R ไปยังวิชวล R</span><span class="sxs-lookup"><span data-stu-id="eea92-104">Tutorial: Build a funnel plot from R script to R visual</span></span>
<span data-ttu-id="eea92-105">บทความนี้จะอธิบายวิธีสร้างแผนภูมิกรวยโดยใช้สคริปต์ R ในวิชวล R เป็นขั้นเป็นตอน</span><span class="sxs-lookup"><span data-stu-id="eea92-105">This article describes how to build a funnel plot using R script in R visual step by step.</span></span>

<span data-ttu-id="eea92-106">ในบทความนี้คุณเรียนรู้วิธีสร้าง:</span><span class="sxs-lookup"><span data-stu-id="eea92-106">In this article, you learn how to create:</span></span>

> [!div class="checklist"]
>
> * <span data-ttu-id="eea92-107">สคริปต์ R สำหรับ RStudio</span><span class="sxs-lookup"><span data-stu-id="eea92-107">an R-script for RStudio</span></span>
> * <span data-ttu-id="eea92-108">วิชวล R ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="eea92-108">an R-visual in Power BI</span></span>
> * <span data-ttu-id="eea92-109">วิชวลที่ขับเคลื่อนด้วย R *แบบใช้ PNG* ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="eea92-109">a *PNG-based* R-powered Visual in Power BI</span></span>
> * <span data-ttu-id="eea92-110">วิชวลที่ขับเคลื่อนด้วย R *แบบใช้ HTML* ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="eea92-110">a *HTML-based* R-powered Visual in Power BI</span></span>

<span data-ttu-id="eea92-111">แผนภูมิกรวยช่วยให้การใช้ แปล และแสดงปริมาณการเปลี่ยนแปลงที่คาดไว้ทำได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="eea92-111">The funnel plot provides an easy way to consume, interpret, and show the amount of expected variation.</span></span> <span data-ttu-id="eea92-112">**กรวย** ถูกสร้างขึ้นโดยใช้ขีดจำกัดความเชื่อมั่นและค่าผิดปกติจะแสดงเป็นจุดด้านนอกกรวย</span><span class="sxs-lookup"><span data-stu-id="eea92-112">The **funnel** is formed using confidence limits and outliers are shown as dots outside the funnel.</span></span>

<span data-ttu-id="eea92-113">ในตัวอย่างนี้ เราใช้แผนภูมิกรวยเพื่อเปรียบเทียบและวิเคราะห์ข้อมูลชุดต่างๆ</span><span class="sxs-lookup"><span data-stu-id="eea92-113">In this example the funnel plot is used to compare and analyze various sets data.</span></span>  

> [!NOTE]
> <span data-ttu-id="eea92-114">ไฟล์ต้นฉบับพร้อมใช้งานสำหรับการดาวน์โหลดภายใต้แต่ละชุดของขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="eea92-114">Source files are available for download under each set of steps.</span></span>

## <a name="build-an-r-script-with-dataset"></a><span data-ttu-id="eea92-115">สร้างสคริปต์ R ที่มีชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="eea92-115">Build an R script with dataset</span></span>

1. <span data-ttu-id="eea92-116">ดาวน์โหลด [สคริปต์ R น้อยที่สุด](https://github.com/PowerBi-Projects/PowerBI-visuals/raw/master/RVisualTutorial/TutorialFunnelPlot/chapter1_R/script_R_v1_00.r) และตารางข้อมูล [dataset.csv](https://github.com/PowerBi-Projects/PowerBI-visuals/raw/master/RVisualTutorial/TutorialFunnelPlot/chapter1_R/dataset.csv)</span><span class="sxs-lookup"><span data-stu-id="eea92-116">Download a [minimal R script](https://github.com/PowerBi-Projects/PowerBI-visuals/raw/master/RVisualTutorial/TutorialFunnelPlot/chapter1_R/script_R_v1_00.r) and its data table, [dataset.csv](https://github.com/PowerBi-Projects/PowerBI-visuals/raw/master/RVisualTutorial/TutorialFunnelPlot/chapter1_R/dataset.csv).</span></span>

1. <span data-ttu-id="eea92-117">ถัดไป แก้ไขสคริปต์เพื่อทำมิเรอร์ [สคริปต์นี้](https://github.com/PowerBi-Projects/PowerBI-visuals/raw/master/RVisualTutorial/TutorialFunnelPlot/chapter1_R/script_R_v1_01.r)</span><span class="sxs-lookup"><span data-stu-id="eea92-117">Next, edit the script to mirror [this script](https://github.com/PowerBi-Projects/PowerBI-visuals/raw/master/RVisualTutorial/TutorialFunnelPlot/chapter1_R/script_R_v1_01.r).</span></span> <span data-ttu-id="eea92-118">สิ่งนี้เพิ่มการจัดการข้อผิดพลาดของอินพุตและพารามิเตอร์ผู้ใช้เพื่อควบคุมลักษณะที่ปรากฏของกราฟ</span><span class="sxs-lookup"><span data-stu-id="eea92-118">This adds input error handling and user parameters to control the plot's appearance.</span></span>

## <a name="build-a-report"></a><span data-ttu-id="eea92-119">สร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="eea92-119">Build a report</span></span>

<span data-ttu-id="eea92-120">ถัดไป แก้ไขสคริปต์เพื่อทำมิเรอร์ [สคริปต์นี้](https://github.com/PowerBi-Projects/PowerBI-visuals/raw/master/RVisualTutorial/TutorialFunnelPlot/chapter2_Rvisual/script_RV_v2_00.r)</span><span class="sxs-lookup"><span data-stu-id="eea92-120">Next, edit the script to mirror [this script](https://github.com/PowerBi-Projects/PowerBI-visuals/raw/master/RVisualTutorial/TutorialFunnelPlot/chapter2_Rvisual/script_RV_v2_00.r).</span></span> <span data-ttu-id="eea92-121">การดำเนินการนี้จะโหลด *dataset.csv* แทนที่จะเป็น *read.csv* ลงในพื้นที่ทำงานของ Power BI desktop และสร้างตาราง **Cancer Mortality**</span><span class="sxs-lookup"><span data-stu-id="eea92-121">This loads *dataset.csv* instead of *read.csv* into the Power BI desktop workspace and creates a **Cancer Mortality** table.</span></span> <span data-ttu-id="eea92-122">ดูผลลัพธ์ใน[ไฟล์ PBIX](https://github.com/PowerBi-Projects/PowerBI-visuals/raw/master/RVisualTutorial/TutorialFunnelPlot/chapter2_Rvisual/funnelPlot_Rvisual.pbix) ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="eea92-122">See the results in the following [PBIX file](https://github.com/PowerBi-Projects/PowerBI-visuals/raw/master/RVisualTutorial/TutorialFunnelPlot/chapter2_Rvisual/funnelPlot_Rvisual.pbix).</span></span>

> [!NOTE]
> <span data-ttu-id="eea92-123">`dataset` เป็นชื่อแบบฮาร์ดโค้ดสำหรับการป้อนค่า `data.frame` ของวิชวล R</span><span class="sxs-lookup"><span data-stu-id="eea92-123">The `dataset` is a hard-coded name for the input `data.frame` of any R-visual.</span></span> 

## <a name="create-an-r-powered-visual-and-package-in-r-code"></a><span data-ttu-id="eea92-124">สร้างวิชวลและแพคเกจที่ขับเคลื่อนด้วย R ใน R code</span><span class="sxs-lookup"><span data-stu-id="eea92-124">Create an R-powered visual and package in R code</span></span>

1. <span data-ttu-id="eea92-125">ก่อนที่คุณจะเริ่มต้น โปรดตรวจสอบให้แน่ใจว่าได้ [ติดตั้งเครื่องมือ PBIVIZ](./environment-setup.md#install-pbiviz)</span><span class="sxs-lookup"><span data-stu-id="eea92-125">Before you begin, be sure to [install PBIVIZ tools](./environment-setup.md#install-pbiviz).</span></span>

1. <span data-ttu-id="eea92-126">เรียกใช้คำสั่งต่อไปนี้เพื่อสร้างวิชวลที่ขับเคลื่อนด้วย R ใหม่:</span><span class="sxs-lookup"><span data-stu-id="eea92-126">Run the following command to create a new R-powered visual:</span></span>

   ```bash
   pbiviz new funnel-visual -t rvisual
   cd funnel-visual
   npm install 
   pbiviz package
   ```

   <span data-ttu-id="eea92-127">คำสั่งนี้สร้างโฟลเดอร์ *วิชวลกรวย* ด้วยวิชวลเทมเพลตเริ่มต้น (`-t` สำหรับ **เทมเพลต**)</span><span class="sxs-lookup"><span data-stu-id="eea92-127">This command creates the folder *funnel-visual* with initial template visual (`-t` for **template**).</span></span> <span data-ttu-id="eea92-128">PBIVIZ สามารถพบได้ในโฟลเดอร์ *dist*, โค้ด R ภายในไฟล์ *script.r*</span><span class="sxs-lookup"><span data-stu-id="eea92-128">The PBIVIZ can be found in the *dist* folder, the R-code inside *script.r* file.</span></span> <span data-ttu-id="eea92-129">ลองนำเข้าลงใน Power BI และดูว่าเกิดอะไรขึ้น</span><span class="sxs-lookup"><span data-stu-id="eea92-129">Try to import it into Power BI and see what happens.</span></span>

1. <span data-ttu-id="eea92-130">แก้ไขไฟล์ *script.r* และแทนที่เนื้อหาด้วยสคริปต์ก่อนหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="eea92-130">Edit *script.r* file and replace the contents with your previous script.</span></span>

1. <span data-ttu-id="eea92-131">แก้ไข *capabilities.json* และแทนที่ `Values` สตริงด้วย `dataset`</span><span class="sxs-lookup"><span data-stu-id="eea92-131">Edit *capabilities.json* and replace the string `Values` with `dataset`.</span></span> <span data-ttu-id="eea92-132">การดำเนินการนี้จะแทนที่ชื่อ "บทบาท" ในเทมเพลตเหมือนในโค้ด R</span><span class="sxs-lookup"><span data-stu-id="eea92-132">This replaces the name of "Role" in the template to be like in R-code.</span></span>

   ![สกรีนช็อตแสดงการเปรียบเทียบที่แตกต่างกันของการเปลี่ยนแปลงในไฟล์ json](./samples/funnel-plot/chapter-3/funnel-r-visual-v01/capabilities-changes.PNG)

1. <span data-ttu-id="eea92-134">*(ไม่บังคับ)* แก้ไข *dependencies.json* และเพิ่มส่วนสำหรับแต่ละแพคเกจ R ที่จำเป็นโดยสคริปต์ R</span><span class="sxs-lookup"><span data-stu-id="eea92-134">*(optional)* Edit *dependencies.json* and add a section for each R package required by the R script.</span></span> <span data-ttu-id="eea92-135">การดำเนินการนี้จะเป็นการบอกให้ Power BI นำเข้าแพคเกจเหล่านี้โดยอัตโนมัติเมื่อมีการโหลดวิชวลเป็นครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="eea92-135">This tells Power BI to automatically import these packages when the visual is loaded for the first time.</span></span>

   ![สกรีนช็อตแสดงการเปรียบเทียบที่แตกต่างกันที่มีการเพิ่มเนื้อหาลงในรายการ cranPackages](./samples/funnel-plot/chapter-3/funnel-r-visual-v01/dependencies-changes.PNG)

1. <span data-ttu-id="eea92-137">บรรจุวิชวลเป็นแพคเกจอีกครั้งโดยใช้คำสั่ง `pbiviz package` และลองนำเข้าไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="eea92-137">Repackage the visual using the `pbiviz package` command and try to import it into Power BI.</span></span>

> [!NOTE]
> <span data-ttu-id="eea92-138">ดู [PBIX](https://github.com/PowerBi-Projects/PowerBI-visuals/blob/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelPlot_RCustomVisual.pbix) และ [โค้ดต้นฉบับ](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v01/) สำหรับการดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="eea92-138">See [PBIX](https://github.com/PowerBi-Projects/PowerBI-visuals/blob/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelPlot_RCustomVisual.pbix) and [source code](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v01/) for download.</span></span>

## <a name="make-r-based-visual-improvements"></a><span data-ttu-id="eea92-139">สร้างการปรับปรุงวิชวลแบบใช้ R</span><span class="sxs-lookup"><span data-stu-id="eea92-139">Make R-based visual improvements</span></span>

<span data-ttu-id="eea92-140">วิชวลยังไม่เป็นมิตรต่อผู้ใช้เพราะผู้ใช้จะต้องทราบลำดับของคอลัมน์ในตารางอินพุต</span><span class="sxs-lookup"><span data-stu-id="eea92-140">The visual isn't yet user-friendly because the user has to know the order of columns in the input table.</span></span>

1. <span data-ttu-id="eea92-141">แบ่งเขตข้อมูลอินพุต `dataset` ออกเป็นสามเขตข้อมูล (บทบาท): `Population`, `Number`และ `Tooltips`</span><span class="sxs-lookup"><span data-stu-id="eea92-141">Divide the input field `dataset` into three fields (roles): `Population`, `Number`, and `Tooltips`</span></span>

   ![CV01to02](./media/funnel-plot/diagram-one.PNG)

1. <span data-ttu-id="eea92-143">แก้ไข *capabilities.json* และแทนที่บทบาท `dataset` ด้วยบทบาทใหม่สามบทบาทหรือดาวน์โหลด [capabilities.json](https://github.com/PowerBi-Projects/PowerBI-visuals/raw/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v02/capabilities.json)</span><span class="sxs-lookup"><span data-stu-id="eea92-143">Edit *capabilities.json* and replace the `dataset` role with the three new roles, or download [capabilities.json](https://github.com/PowerBi-Projects/PowerBI-visuals/raw/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v02/capabilities.json).</span></span>

   <span data-ttu-id="eea92-144">คุณจะต้องอัปเดตส่วน: `dataRoles` และ `dataViewMappings`ซึ่งกำหนดชื่อ ชนิด คำแนะนำเครื่องมือ และคอลัมน์สูงสุดสำหรับแต่ละเขตข้อมูลป้อนเข้า</span><span class="sxs-lookup"><span data-stu-id="eea92-144">You'll need to update sections: `dataRoles` and `dataViewMappings`, which define names, types, tooltips, and maximum columns for each input field.</span></span>

   ![ก่อนและหลัง](./samples/funnel-plot/chapter-3/funnel-r-visual-v02/capabilities-before-vs-after.png)
   
   <span data-ttu-id="eea92-146">สำหรับข้อมูลเพิ่มเติม ให้ดู [capabilities](./capabilities.md)</span><span class="sxs-lookup"><span data-stu-id="eea92-146">For more information, see [capabilities](./capabilities.md).</span></span>

1. <span data-ttu-id="eea92-147">แก้ไข *script.r* เพื่อรองรับ `Population`, `Number` และ `Tooltips` ให้เป็นกรอบข้อมูลอินพุตแทนที่จะเป็น `dataset` หรือดาวน์โหลด [script.r](https://github.com/PowerBi-Projects/PowerBI-visuals/raw/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v02/script.r)</span><span class="sxs-lookup"><span data-stu-id="eea92-147">Edit *script.r* to support `Population`, `Number` and `Tooltips` as input dataframes instead of `dataset`, or download [script.r](https://github.com/PowerBi-Projects/PowerBI-visuals/raw/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v02/script.r).</span></span>

   ![สคริปต์](./samples/funnel-plot/chapter-3/funnel-r-visual-v02/script-r-before-vs-after.png)

   > [!TIP]
   > <span data-ttu-id="eea92-149">หากต้องการทำตามการเปลี่ยนแปลงในสคริปต์ R ให้ค้นหาบล็อกข้อคิดเห็น:</span><span class="sxs-lookup"><span data-stu-id="eea92-149">To follow the changes in R-script, search for comment blocks:</span></span> 
   > 
   > ```r
   > #RVIZ_IN_PBI_GUIDE:BEGIN: Added to enable visual fields
   > ...
   > #RVIZ_IN_PBI_GUIDE:END: Added to enable visual fields
   > 
   > #RVIZ_IN_PBI_GUIDE:BEGIN: Removed to enable visual fields 
   > ...
   > #RVIZ_IN_PBI_GUIDE:BEGIN: Removed to enable visual fields
   > ```

1. <span data-ttu-id="eea92-150">บรรจุวิชวลเป็นแพคเกจอีกครั้งโดยใช้คำสั่ง `pbiviz package` และลองนำเข้าไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="eea92-150">Repackage the visual using the `pbiviz package` command and try to import it into Power BI.</span></span>

> [!NOTE]
> <span data-ttu-id="eea92-151">ดู [PBIX](https://github.com/PowerBi-Projects/PowerBI-visuals/raw/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelPlot_RCustomVisual.pbix) และ [โค้ดต้นฉบับ](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v02) สำหรับการดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="eea92-151">See [PBIX](https://github.com/PowerBi-Projects/PowerBI-visuals/raw/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelPlot_RCustomVisual.pbix) and [source code](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v02) for download.</span></span>

## <a name="add-user-parameters"></a><span data-ttu-id="eea92-152">เพิ่มพารามิเตอร์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="eea92-152">Add user parameters</span></span>

1. <span data-ttu-id="eea92-153">เพิ่มความสามารถสำหรับผู้ใช้ในการควบคุมสีและขนาดขององค์ประกอบวิชวล รวมถึงพารามิเตอร์ภายในจาก UI</span><span class="sxs-lookup"><span data-stu-id="eea92-153">Add capabilities for the user to control colors and sizes of visual elements including internal parameters from the UI.</span></span>

   ![สกรีนช็อตแสดงบานหน้าต่างเครื่องมือสองเวอร์ชันพร้อมตัวเลือกที่เพิ่มเข้ามาในเวอร์ชันทางด้านขวา](./media/funnel-plot/diagram-two.PNG)

1. <span data-ttu-id="eea92-155">แก้ไข *capabilities.json* และอัปเดตส่วน `objects`</span><span class="sxs-lookup"><span data-stu-id="eea92-155">Edit *capabilities.json* and update the `objects` section.</span></span> <span data-ttu-id="eea92-156">ที่นี่เรากำหนดชื่อ คำแนะนำเครื่องมือ และชนิดของแต่ละพารามิเตอร์ และยังตัดสินใจเลือกพาร์ติชันของพารามิเตอร์ลงในกลุ่ม (สามกลุ่มในกรณีนี้)</span><span class="sxs-lookup"><span data-stu-id="eea92-156">Here we define names, tooltips and types of each parameter, and also decide on the partition of parameters into groups (three groups in this case).</span></span>

   <span data-ttu-id="eea92-157">ดาวน์โหลด [capabilities.json](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v03/capabilities.json) ดู [คุณสมบุติวัตถุ](./objects-properties.md) สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="eea92-157">download [capabilities.json](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v03/capabilities.json), see [object properties](./objects-properties.md) for more information</span></span>

   ![ความสามารถ](./samples/funnel-plot/chapter-3/funnel-r-visual-v03/capabilities-before-after.PNG)

1. <span data-ttu-id="eea92-159">แก้ไข *src/settings.ts* เพื่อมิเรอร์ [settings.ts นี้](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v03/src/settings.ts)</span><span class="sxs-lookup"><span data-stu-id="eea92-159">Edit *src/settings.ts* to mirror [this settings.ts](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v03/src/settings.ts).</span></span> <span data-ttu-id="eea92-160">ไฟล์นี้จะถูกเขียนใน TypeScript</span><span class="sxs-lookup"><span data-stu-id="eea92-160">This file is written in TypeScript.</span></span>  

   <span data-ttu-id="eea92-161">ที่นี่คุณจะพบบล็อกของโค้ดสองรายการที่เพิ่มเข้าไปเพื่อ:</span><span class="sxs-lookup"><span data-stu-id="eea92-161">Here you'll find two blocks of the code added to:</span></span>
   - <span data-ttu-id="eea92-162">ประกาศอินเทอร์เฟซใหม่เพื่อเก็บค่าคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="eea92-162">Declare new interface to hold the property value</span></span>
   - <span data-ttu-id="eea92-163">กำหนดคุณสมบัติสมาชิกและค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="eea92-163">Define a member property and default values</span></span>

   ![การตั้งค่า](./samples/funnel-plot/chapter-3/funnel-r-visual-v03/settings-ts-before-after.PNG)

1. <span data-ttu-id="eea92-165">แก้ไข *script.r* เพื่อมิเรอร์ [script.r นี้](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v03/script.r)</span><span class="sxs-lookup"><span data-stu-id="eea92-165">Edit *script.r* to mirror [this script.r](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v03/script.r).</span></span> <span data-ttu-id="eea92-166">ซึ่งเพิ่มการสนับสนุนสำหรับพารามิเตอร์ใน UI โดยการเพิ่มการเรียก `if.exists` ต่อพารามิเตอร์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="eea92-166">This adds support for the parameters in the UI by adding `if.exists` calls per user-parameter.</span></span>

   > [!TIP]
   > <span data-ttu-id="eea92-167">หากต้องการทำตามการเปลี่ยนแปลงในสคริปต์ R ให้ค้นหาความคิดเห็น:</span><span class="sxs-lookup"><span data-stu-id="eea92-167">To follow the changes in R-script, search for comments:</span></span>
   >
   > ```r
   > #RVIZ_IN_PBI_GUIDE:BEGIN:Added to enable user parameters
   >  ...
   > #RVIZ_IN_PBI_GUIDE:END:Added to enable user parameters
   >
   > #RVIZ_IN_PBI_GUIDE:BEGIN:Removed to enable user parameters 
   >  ...
   > #RVIZ_IN_PBI_GUIDE:END:Removed to enable user parameters
   > ```

   ![สคริปต์ก่อนและหลัง](https://raw.githubusercontent.com/PowerBi-Projects/PowerBI-visuals/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v03/script_r_before_after_1.png)

   <span data-ttu-id="eea92-169">คุณสามารถตัดสินใจที่จะไม่เปิดเผยพารามิเตอร์ไปยัง UI อย่างที่เราทำ</span><span class="sxs-lookup"><span data-stu-id="eea92-169">You can decide not to expose the parameters to the UI, like we did.</span></span>  

1. <span data-ttu-id="eea92-170">บรรจุวิชวลเป็นแพคเกจอีกครั้งโดยใช้คำสั่ง `pbiviz package` และลองนำเข้าไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="eea92-170">Repackage the visual using the `pbiviz package` command and try to import it into Power BI.</span></span>

> [!NOTE]
> <span data-ttu-id="eea92-171">ดู [PBIX](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelPlot_RCustomVisual.pbix) และ [โค้ดต้นฉบับ](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v03/) สำหรับการดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="eea92-171">See [PBIX](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelPlot_RCustomVisual.pbix) and [source code](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter3_RCustomVisual/funnelRvisual_v03/) for download.</span></span>

> [!TIP]
> <span data-ttu-id="eea92-172">ต่อไปนี้เราได้เพิ่มพารามิเตอร์ของหลายชนิด (บูลีน, ตัวเลข, สตริงและสี) ทั้งหมดในครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="eea92-172">Here we added parameters of several types (boolean, numeric, string, and color) all at once.</span></span> <span data-ttu-id="eea92-173">สำหรับกรณีอย่างง่าย โปรดดู [ตัวอย่างนี้](https://github.com/PowerBi-Projects/PowerBI-visuals/blob/master/RVisualTutorial/PropertiesPane.md) เกี่ยวกับวิธีการเพิ่มพารามิเตอร์เดียว</span><span class="sxs-lookup"><span data-stu-id="eea92-173">For a simple case, please see [this example](https://github.com/PowerBi-Projects/PowerBI-visuals/blob/master/RVisualTutorial/PropertiesPane.md) on how to add a single parameter.</span></span> 

## <a name="convert-visual-to-rhtml-based-visual"></a><span data-ttu-id="eea92-174">แปลงวิชวลเป็นวิชวลแบบใช้ RHTML</span><span class="sxs-lookup"><span data-stu-id="eea92-174">Convert visual to RHTML-based visual</span></span>

<span data-ttu-id="eea92-175">เนื่องจากวิชวลที่แสดงนั้นเป็นแบบ PNG จึงไม่ตอบสนองต่อการเลื่อนเมาส์ ไม่สามารถซูมเข้าและอื่นๆ ได้ ดังนั้นเราจำเป็นต้องแปลงเป็นวิชวลแบบใช้ HTML</span><span class="sxs-lookup"><span data-stu-id="eea92-175">Since the resulting visual is PNG-based, it isn't responsive to mouse hover, can't be zoomed in on, and so on, so we need to convert it to an HTML-based visual.</span></span> <span data-ttu-id="eea92-176">เราจะสร้างเทมเพลตการวิชวลแบบ HTML ที่ขับเคลื่อนด้วย R ที่ว่างเปล่า จากนั้นคัดลอกสคริปต์บางอย่างจากโครงการแบบใช้ PNG</span><span class="sxs-lookup"><span data-stu-id="eea92-176">We'll create an empty R-powered HTML-based Visual template, then copy some scripts from the PNG-based project.</span></span>

1. <span data-ttu-id="eea92-177">เรียกใช้คำสั่ง:</span><span class="sxs-lookup"><span data-stu-id="eea92-177">Run the command:</span></span>

   ```bash
   pbiviz new funnel-visual-HTML -t rhtml
   cd funnel-visual-HTML
   npm install 
   pbiviz package
   ```

1. <span data-ttu-id="eea92-178">เปิด *capabilities.json* และบันทึกบรรทัด `"scriptOutputType":"html"`</span><span class="sxs-lookup"><span data-stu-id="eea92-178">Open *capabilities.json* and note the `"scriptOutputType":"html"` line.</span></span>

1. <span data-ttu-id="eea92-179">เปิด *dependencies.json* และบันทึกชื่อของแพคเกจ R ที่อยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="eea92-179">Open *dependencies.json* and note the names of the listed R-packages.</span></span>

1. <span data-ttu-id="eea92-180">เปิด *script.r* และบันทึกโครงสร้าง</span><span class="sxs-lookup"><span data-stu-id="eea92-180">Open *script.r* and note the structure.</span></span> <span data-ttu-id="eea92-181">คุณสามารถเปิดและเรียกใช้ใน RStudio ได้เนื่องจากไม่ได้ใช้อินพุตภายนอก</span><span class="sxs-lookup"><span data-stu-id="eea92-181">You can open and run it in RStudio since it doesn't use external input.</span></span> 

   <span data-ttu-id="eea92-182">การดำเนินการนี้จะเป็นการสร้างและบันทึก *out.html*</span><span class="sxs-lookup"><span data-stu-id="eea92-182">This creates and saves *out.html*.</span></span> <span data-ttu-id="eea92-183">ไฟล์นี้มีอยู่ในตัวเอง (โดยไม่มีการอ้างอิงภายนอก) และกำหนดกราฟิกภายในวิดเจ็ต HTML</span><span class="sxs-lookup"><span data-stu-id="eea92-183">This file is self-contained (with no external dependencies) and defines the graphics inside the HTML widget.</span></span> 

   > [!IMPORTANT]
   > <span data-ttu-id="eea92-184">สำหรับผู้ใช้ `htmlWidgets`, อรรถประโยชน์ R จะปรากฏใน [โฟลเดอร์ r_files](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/funnelRHTMLvisual_v01/r_files) เพื่อช่วยในการแปลงวัตถุ `plotly` หรือ `widget` ลงใน HTML ที่มีทุกอย่างพร้อมในตัว</span><span class="sxs-lookup"><span data-stu-id="eea92-184">For `htmlWidgets` users, R-utilities are provided in the [r_files folder](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/funnelRHTMLvisual_v01/r_files) to help convert `plotly` or `widget` objects into self-content HTML.</span></span> 
   > 
   > <span data-ttu-id="eea92-185">วิชวลที่ขับเคลื่อนด้วย R เวอร์ชันนี้ยังสนับสนุนคำสั่ง `source` (แตกต่างจากวิชวลชนิดก่อนหน้า) เพื่อทำให้โค้ดของคุณอ่านได้ง่ายยิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="eea92-185">This version of R-powered visual also supports the `source` command (unlike previous types of visuals), to make your code more readable.</span></span>   
 
1. <span data-ttu-id="eea92-186">แทนที่ *capabilities.json* ด้วย *capabilities.json* จากขั้นตอนก่อนหน้านี้ หรือดาวน์โหลด [capabilities.json](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/funnelRHTMLvisual_v01/capabilities.json)</span><span class="sxs-lookup"><span data-stu-id="eea92-186">Replace *capabilities.json* with the *capabilities.json* from the previous step, or download [capabilities.json](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/funnelRHTMLvisual_v01/capabilities.json).</span></span>

   <span data-ttu-id="eea92-187">โปรดจดจำไว้ว่า:</span><span class="sxs-lookup"><span data-stu-id="eea92-187">Be sure to keep:</span></span>

   `"scriptOutputType": "html"`

1. <span data-ttu-id="eea92-188">ผสานรวม *script.r* เวอร์ชันล่าสุดกับ *script.r* จากเทมเพลตหรือดาวน์โหลด [script.r](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/funnelRHTMLvisual_v01/script.r)</span><span class="sxs-lookup"><span data-stu-id="eea92-188">Merge the latest version of *script.r* with the *script.r* from the template, or download [script.r](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/funnelRHTMLvisual_v01/script.r).</span></span>

   <span data-ttu-id="eea92-189">สคริปต์ใหม่ใช้แพคเกจ `plotly` เพื่อแปลงวัตถุ **ggplot** ลงในวัตถุ **plotly** แล้วแพคเกจ `htmlWidgets` เพื่อบันทึกไปยังไฟล์ HTML</span><span class="sxs-lookup"><span data-stu-id="eea92-189">The new script uses the `plotly` package to convert the **ggplot** object into a **plotly** object, then the `htmlWidgets` package to save it to an HTML file.</span></span> 

   <span data-ttu-id="eea92-190">ฟังก์ชันอรรถประโยชน์ส่วนใหญ่จะถูกย้ายไปยัง [_r_files/utils.r_](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/funnelRHTMLvisual_v01/r_files/utils.r) และมีการเพิ่มฟังก์ชัน `generateNiceTooltips` สำหรับลักษณะที่ปรากฏของวัตถุ **plotly**</span><span class="sxs-lookup"><span data-stu-id="eea92-190">Most of the utility functions are moved to [_r_files/utils.r_](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/funnelRHTMLvisual_v01/r_files/utils.r) and the `generateNiceTooltips` function is added for the appearance of the **plotly** object.</span></span>

   ![1](./samples/funnel-plot/chapter-4/RHTML-v01/script-before-after-1.PNG)
   
   ![2](./samples/funnel-plot/chapter-4/RHTML-v01/script-before-after-2.PNG)

   > [!TIP]
   > <span data-ttu-id="eea92-193">หากต้องการทำตามการเปลี่ยนแปลงในสคริปต์ R ให้ค้นหาความคิดเห็น:</span><span class="sxs-lookup"><span data-stu-id="eea92-193">To follow the changes in R-script, search for comments:</span></span>
   > 
   > ```r
   > #RVIZ_IN_PBI_GUIDE:BEGIN:Added to create HTML-based 
   >  ...
   > #RVIZ_IN_PBI_GUIDE:BEGIN:Added to create HTML-based
   >
   > #RVIZ_IN_PBI_GUIDE:BEGIN:Removed to create HTML-based  
   > ...
   > #RVIZ_IN_PBI_GUIDE:BEGIN:Removed to create HTML-based
   > ```

1. <span data-ttu-id="eea92-194">ผสาน *dependencies.json* เวอร์ชันล่าสุดกับ *dependencies.json* จากเทมเพลต เพื่อรวมการอ้างอิงแพคเกจ R ใหม่หรือดาวน์โหลด [dependencies.json](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/funnelRHTMLvisual_v01/dependencies.json)</span><span class="sxs-lookup"><span data-stu-id="eea92-194">Merge the latest version of *dependencies.json* with the *dependencies.json* from the template, to include new R-package dependencies, or download [dependencies.json](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/funnelRHTMLvisual_v01/dependencies.json).</span></span>

1. <span data-ttu-id="eea92-195">แก้ไข *src/settings.ts* ด้วยวิธีเดียวกันจากขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="eea92-195">Edit *src/settings.ts* the same way from previous steps.</span></span>

1. <span data-ttu-id="eea92-196">บรรจุวิชวลเป็นแพคเกจอีกครั้งโดยใช้คำสั่ง `pbiviz package` และลองนำเข้าไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="eea92-196">Repackage the visual using the `pbiviz package` command and try to import it into Power BI.</span></span>

> [!NOTE]
> <span data-ttu-id="eea92-197">ดู [PBIX และโค้ดต้นฉบับ](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/funnelRHTMLvisual_v01) สำหรับการดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="eea92-197">See [PBIX and source code](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/funnelRHTMLvisual_v01) for download.</span></span>

## <a name="build-additional-examples"></a><span data-ttu-id="eea92-198">สร้างตัวอย่างเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="eea92-198">Build additional examples</span></span>

1. <span data-ttu-id="eea92-199">เรียกใช้คำสั่งต่อไปนี้เพื่อสร้างโครงการว่างเปล่า:</span><span class="sxs-lookup"><span data-stu-id="eea92-199">Run the following command to create an empty project:</span></span> 

   ```bash
   pbiviz new example -t rhtml
   cd example
   npm install 
   pbiviz package
   ```

1. <span data-ttu-id="eea92-200">รับโค้ดจาก [การแสดง](http://www.htmlwidgets.org/showcase_networkD3.html) และทำการเปลี่ยนแปลงที่เน้นไว้:</span><span class="sxs-lookup"><span data-stu-id="eea92-200">Take code from this [showcase](http://www.htmlwidgets.org/showcase_networkD3.html) and make the highlighted changes:</span></span>

   ![การเปลี่ยนแปลงที่เน้น](./media/funnel-plot/diagram-three.PNG)

1. <span data-ttu-id="eea92-202">แทนที่ *script.r* ของเทมเพลตคุณ และเรียกใช้ `pbiviz package` อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="eea92-202">Replace your template's *script.r* and run `pbiviz package` again.</span></span> <span data-ttu-id="eea92-203">ตอนนี้วิชวลจะรวมอยู่ในรายงาน Power BI ของคุณ!</span><span class="sxs-lookup"><span data-stu-id="eea92-203">Now the visual is included in your Power BI report!</span></span>

## <a name="tips-and-tricks"></a><span data-ttu-id="eea92-204">คำแนะนำและเคล็ดลับ</span><span class="sxs-lookup"><span data-stu-id="eea92-204">Tips and tricks</span></span>

* <span data-ttu-id="eea92-205">เราขอแนะนำให้นักพัฒนาแก้ไข *pbiviz.json* เพื่อจัดเก็บเมตาดาต้าที่ถูกต้อง เช่น **เวอร์ชัน** **อีเมล** **ชื่อ** **ชนิดสิทธิการใช้งาน** และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="eea92-205">We recommend that developers edit *pbiviz.json* to store correct metadata, such as **version**, **email**, **name**, **license type**, and so on.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="eea92-206">เขตข้อมูล **guid** เป็นรหัสเฉพาะสำหรับวิชวล</span><span class="sxs-lookup"><span data-stu-id="eea92-206">The **guid** field is the unique identifier for a visual.</span></span> <span data-ttu-id="eea92-207">ถ้าคุณสร้างโครงการใหม่สำหรับแต่ละวิชวล GUID จะแตกต่างกันด้วย</span><span class="sxs-lookup"><span data-stu-id="eea92-207">If you create a new project for each visual, the GUID will be also be different.</span></span> <span data-ttu-id="eea92-208">ซึ่งจะเหมือนกับการใช้โครงการเก่าที่คัดลอกไปยังวิชวลใหม่ซึ่งคุณไม่ควรทำ</span><span class="sxs-lookup"><span data-stu-id="eea92-208">It's only the same when using an old project copied to a new visual, which you shouldn't do.</span></span>

* <span data-ttu-id="eea92-209">แก้ไข [*assets/icon.png*](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/funnelRHTMLvisual_v01/assets/icon.png) เพื่อสร้างไอคอนเฉพาะสำหรับวิชวลของคุณ</span><span class="sxs-lookup"><span data-stu-id="eea92-209">Edit [*assets/icon.png*](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/funnelRHTMLvisual_v01/assets/icon.png) to create unique icons for your visual.</span></span> 

* <span data-ttu-id="eea92-210">เมื่อต้องการตรวจแก้จุดบกพร่อง R code ใน RStudio โดยใช้ข้อมูลเดียวกันกับในรายงาน Power BI ของคุณ ให้เพิ่มสิ่งต่อไปนี้ลงในจุดเริ่มต้นของสคริปต์ R (แก้ไขตัวแปร `fileRda`):</span><span class="sxs-lookup"><span data-stu-id="eea92-210">To debug R-code in RStudio using the same data as in your Power BI report, add the following to the beginning of the R-script (edit the `fileRda` variable):</span></span>

   ```r
   #DEBUG in RStudio
   fileRda = "C:/Users/yourUserName/Temp/tempData.Rda"
   if(file.exists(dirname(fileRda)))
   {
     if(Sys.getenv("RSTUDIO")!="")
       load(file= fileRda)
     else
       save(list = ls(all.names = TRUE), file=fileRda)
   }
   ```

   <span data-ttu-id="eea92-211">สิ่งนี้ช่วยประหยัดสภาพแวดล้อมจากรายงาน Power BI และโหลดลงใน RStudio</span><span class="sxs-lookup"><span data-stu-id="eea92-211">This saves the environment from a Power BI report and loads it into RStudio.</span></span> 

* <span data-ttu-id="eea92-212">คุณไม่จำเป็นต้องพัฒนาวิชวลที่ขับเคลื่อนด้วย R จากจุดเริ่มต้นด้วยโค้ดที่พร้อมใช้งานบน [GitHub](https://github.com/Microsoft?utf8=%E2%9C%93&q=PowerBI&type=&language=R)</span><span class="sxs-lookup"><span data-stu-id="eea92-212">You don't need to develop R-powered Visuals from scratch with code available on [GitHub](https://github.com/Microsoft?utf8=%E2%9C%93&q=PowerBI&type=&language=R).</span></span> <span data-ttu-id="eea92-213">คุณสามารถเลือกวิชวลเพื่อใช้เป็นเทมเพลตและคัดลอกโค้ดลงในโครงการใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="eea92-213">You can select the visual to use as a template and copy the code into a new project.</span></span>

   <span data-ttu-id="eea92-214">ตัวอย่างเช่น ลองใช้ [วิชวล spline แบบกำหนดเอง](https://github.com/PowerBi-Projects/PowerBI-visuals-spline)</span><span class="sxs-lookup"><span data-stu-id="eea92-214">For example, try using the [spline custom visual](https://github.com/PowerBi-Projects/PowerBI-visuals-spline).</span></span>

* <span data-ttu-id="eea92-215">แต่ละวิชวล R จะใช้ตัวดำเนินการ `unique` กับตารางข้อมูลอินพุต</span><span class="sxs-lookup"><span data-stu-id="eea92-215">Each R Visual applies the `unique` operator to its input table.</span></span> <span data-ttu-id="eea92-216">หากต้องการหลีกเลี่ยงการลบแถวที่เหมือนกัน ให้พิจารณาเพิ่มเขตข้อมูลอินพุตพิเศษด้วย ID ที่ไม่ซ้ำกันและละเว้นในโค้ด R</span><span class="sxs-lookup"><span data-stu-id="eea92-216">To avoid identical rows being removed, consider adding an extra input field with a unique ID and ignore it in the R code.</span></span>   

* <span data-ttu-id="eea92-217">ถ้าคุณมีบัญชี Power BI ให้ใช้บริการ Power BI เพื่อพัฒนาวิชวล [on-the-fly](./develop-circle-card.md) แทนที่จะบรรจุเป็นแพคเกจอีกครั้งด้วยคำสั่ง `pbiviz package`</span><span class="sxs-lookup"><span data-stu-id="eea92-217">If you have a Power BI account, use the Power BI service to develop a visual [on-the-fly](./develop-circle-card.md) instead of repackaging them with the `pbiviz package` command.</span></span>

### <a name="html-widgets-gallery"></a><span data-ttu-id="eea92-218">แกลเลอรีวิดเจ็ต HTML</span><span class="sxs-lookup"><span data-stu-id="eea92-218">HTML widgets gallery</span></span>
<span data-ttu-id="eea92-219">สำรวจวิชวลใน[แกลเลอรีวิดเจ็ต HTML](http://gallery.htmlwidgets.org/) สำหรับการใช้งานในวิชวลถัดไปของคุณ</span><span class="sxs-lookup"><span data-stu-id="eea92-219">Explore visuals in the [HTML widgets gallery](http://gallery.htmlwidgets.org/) for use in your next visual.</span></span> <span data-ttu-id="eea92-220">เพื่อทำให้สิ่งต่างๆ เป็นเรื่องง่าย เราได้สร้าง [ที่เก็บโครงการของวิชวล](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/multipleRHTML) พร้อมวิชวล HTML แบบโต้ตอบมากกว่า 20 รายการให้เลือก!</span><span class="sxs-lookup"><span data-stu-id="eea92-220">To make things easy, we've created a [visuals project repo](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/multipleRHTML) with over 20 interactive HTML visuals to choose from!</span></span>

> [!TIP]
> <span data-ttu-id="eea92-221">เพื่อสลับระหว่างวิดเจ็ต html ให้ใช้ **รูปแบบ** > **การตั้งค่า** > **ชนิด**</span><span class="sxs-lookup"><span data-stu-id="eea92-221">To switch between html widgets use **Format** > **Settings** > **Type**.</span></span> <span data-ttu-id="eea92-222">ลองใช้งานด้วย [ไฟล์ .PBIX นี้](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/multipleRHTML/assets/sample.pbix)</span><span class="sxs-lookup"><span data-stu-id="eea92-222">Try it out with [this PBIX file](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/master/RVisualTutorial/TutorialFunnelPlot/chapter4_RHTMLCustomVisual/multipleRHTML/assets/sample.pbix).</span></span> 

#### <a name="to-use-a-sample-for-your-visual"></a><span data-ttu-id="eea92-223">เมื่อต้องการใช้ตัวอย่างสำหรับวิชวลของคุณ</span><span class="sxs-lookup"><span data-stu-id="eea92-223">To use a sample for your visual</span></span>

1. <span data-ttu-id="eea92-224">ดาวน์โหลดทั้งโฟลเดอร์</span><span class="sxs-lookup"><span data-stu-id="eea92-224">Download the entire folder.</span></span>
1. <span data-ttu-id="eea92-225">แก้ไข *script.r* และ *dependencies.json* เพื่อเก็บวิดเจ็ตเพียงหนึ่งเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="eea92-225">Edit *script.r* and *dependencies.json* to keep only one widget.</span></span>
1. <span data-ttu-id="eea92-226">แก้ไข *capabilities.json* และ *settings.ts* เพื่อเอาตัวเลือก `Type` ออก</span><span class="sxs-lookup"><span data-stu-id="eea92-226">Edit *capabilities.json* and *settings.ts* to remove the `Type` selector.</span></span>
1. <span data-ttu-id="eea92-227">เปลี่ยน `const updateHTMLHead: boolean = true;` เป็น `false` ใน *visual.ts*</span><span class="sxs-lookup"><span data-stu-id="eea92-227">Change `const updateHTMLHead: boolean = true;` to `false` in *visual.ts*.</span></span> <span data-ttu-id="eea92-228">*(เพื่อประสิทธิภาพการทำงานที่ดีขึ้น)*</span><span class="sxs-lookup"><span data-stu-id="eea92-228">*(for better performance)*</span></span>
1. <span data-ttu-id="eea92-229">เปลี่ยนเมตาดาต้าใน *pbiviz.json* ซึ่งสำคัญมากที่สุดเขตข้อมูล `guid`</span><span class="sxs-lookup"><span data-stu-id="eea92-229">Change metadata in *pbiviz.json*, most importantly the `guid` field.</span></span>
1. <span data-ttu-id="eea92-230">บรรจุเป็นแพคเกจอีกครั้งและดำเนินการต่อเพื่อปรับแต่งวิชวลตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="eea92-230">Repackage and continue to customize the visual as wanted.</span></span> 

![สกรีนช็อตแสดงวิดเจ็ตหกรายการที่อธิบายไว้ก่อนหน้าในบทความนี้](./media/funnel-plot/diagram-four.PNG)

![สกรีนช็อตแสดงวิดเจ็ตอีกหกรายการที่อธิบายไว้ก่อนหน้าในบทความนี้](./media/funnel-plot/diagram-five.PNG)

> [!NOTE]
> <span data-ttu-id="eea92-233">บริการไม่ได้สนับสนุนวิดเจ็ตทั้งหมดในโครงการนี้</span><span class="sxs-lookup"><span data-stu-id="eea92-233">Not all widgets in this project are supported by the service.</span></span>

## <a name="next-steps"></a><span data-ttu-id="eea92-234">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="eea92-234">Next steps</span></span>

<span data-ttu-id="eea92-235">หากต้องการเรียนรู้เพิ่มเติม โปรดดูบทช่วยสอน Power BI เพิ่มเติม [การพัฒนาวิชวลการ์ดวงกลมใน Power BI](./develop-circle-card.md) และ [วิชวล R](../../visuals/service-r-visuals.md)</span><span class="sxs-lookup"><span data-stu-id="eea92-235">To learn more, see additional Power BI tutorials, [Developing a Power BI circle card visual](./develop-circle-card.md) and [R visuals](../../visuals/service-r-visuals.md).</span></span>

<span data-ttu-id="eea92-236">เรียนรู้วิธีการ [พัฒนาและส่งวิชวล](https://powerbi.microsoft.com/documentation/powerbi-developer-office-store/) ไปยัง [Office Store (แกลเลอรี่)](https://store.office.com/appshome.aspx?ui=en-US&rs=en-US&ad=US&clickedfilter=OfficeProductFilter%3aPowerBI&productgroup=PowerBI) หรือสำหรับตัวอย่างเพิ่มเติม โปรดดู [การแสดงสคริปต์ R](https://community.powerbi.com/t5/R-Script-Showcase/bd-p/RVisuals)</span><span class="sxs-lookup"><span data-stu-id="eea92-236">Learn how to [develop and submit visuals](https://powerbi.microsoft.com/documentation/powerbi-developer-office-store/) to the [Office Store (gallery)](https://store.office.com/appshome.aspx?ui=en-US&rs=en-US&ad=US&clickedfilter=OfficeProductFilter%3aPowerBI&productgroup=PowerBI), or for further examples, see the [R-script showcase](https://community.powerbi.com/t5/R-Script-Showcase/bd-p/RVisuals)</span></span>
