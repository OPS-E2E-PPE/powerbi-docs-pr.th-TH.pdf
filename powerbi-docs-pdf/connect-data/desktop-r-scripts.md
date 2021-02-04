---
title: เรียกใช้สคริปต์ R ใน Power BI Desktop
description: เรียกใช้สคริปต์ R ใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 01/14/2020
LocalizationGroup: Connect to data
ms.openlocfilehash: 604e90cf2f2c1010559c70df67a6cd54ac08fa36
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96404559"
---
# <a name="run-r-scripts-in-power-bi-desktop"></a><span data-ttu-id="9e5e1-103">เรียกใช้สคริปต์ R ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="9e5e1-103">Run R scripts in Power BI Desktop</span></span>

<span data-ttu-id="9e5e1-104">คุณสามารถเรียกใช้งานสคริปต์ R ได้โดยตรงใน Power BI Desktop และนำเข้าชุดข้อมูลผลลัพธ์ไปยังแบบจำลองข้อมูล Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="9e5e1-104">You can run R scripts directly in Power BI Desktop and import the resulting datasets into a Power BI Desktop data model.</span></span>

## <a name="install-r"></a><span data-ttu-id="9e5e1-105">ติดตั้ง R</span><span class="sxs-lookup"><span data-stu-id="9e5e1-105">Install R</span></span>

<span data-ttu-id="9e5e1-106">เพื่อเรียกใช้สคริปต์ R ใน  Power BI Desktop คุณต้องทำการติดตั้ง R ลงบนเครื่องของคุณก่อน</span><span class="sxs-lookup"><span data-stu-id="9e5e1-106">To run R scripts in Power BI Desktop, you need to install R on your local machine.</span></span> <span data-ttu-id="9e5e1-107">คุณสามารถดาวน์โหลดและติดตั้ง R ได้ฟรีจากหลายตำแหน่ง ประกอบด้วย [Microsoft R Application Network](https://mran.revolutionanalytics.com/download/) และ [CRAN Repository](https://cran.r-project.org/bin/windows/base/)</span><span class="sxs-lookup"><span data-stu-id="9e5e1-107">You can download and install R for free from many locations, including the [Microsoft R Application Network](https://mran.revolutionanalytics.com/download/) and the [CRAN Repository](https://cran.r-project.org/bin/windows/base/).</span></span> <span data-ttu-id="9e5e1-108">การเผยแพร่ในปัจจุบันสนับสนุนอักขระ Unicode และช่องว่าง (อักขระว่าง) ในเส้นทางการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="9e5e1-108">The current release supports Unicode characters and spaces (empty characters) in the installation path.</span></span>

## <a name="run-r-scripts"></a><span data-ttu-id="9e5e1-109">เรียกใช้สคริปต์ R</span><span class="sxs-lookup"><span data-stu-id="9e5e1-109">Run R scripts</span></span>

<span data-ttu-id="9e5e1-110">เพียงไม่กี่ขั้นตอนใน Power BI Desktop คุณก็สามารถเรียกใช้งานสคริปต์ R และสร้างแบบจำลองข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="9e5e1-110">Using just a few steps in Power BI Desktop, you can run R scripts and create a data model.</span></span> <span data-ttu-id="9e5e1-111">ด้วยแบบจำลองข้อมูลนั้น คุณสามารถสร้างรายงานและแชร์ไปยังบริการของ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="9e5e1-111">With the data model, you can create reports and share them on the Power BI service.</span></span> <span data-ttu-id="9e5e1-112">สคริปต์ R ใน Power BI Desktop ตอนนี้สนับสนุนรูปแบบตัวเลขที่มีจุดทศนิยม (.) และเครื่องหมายจุลภาค (,)</span><span class="sxs-lookup"><span data-stu-id="9e5e1-112">R scripting in Power BI Desktop now supports number formats that contain decimals (.) and commas (,).</span></span>

### <a name="prepare-an-r-script"></a><span data-ttu-id="9e5e1-113">เตรียมสคริปต์ R</span><span class="sxs-lookup"><span data-stu-id="9e5e1-113">Prepare an R script</span></span>

<span data-ttu-id="9e5e1-114">เพื่อเรียกใช้สคริปต์ R ใน Power BI Desktop สร้างสคริปต์ R ของคุณในสภาพแวดล้อมการพัฒนา และการตรวจสอบให้แน่ใจว่าการเรียกใช้สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="9e5e1-114">To run an R script in Power BI Desktop, create the script in your local R development environment, and make sure it runs successfully.</span></span>

<span data-ttu-id="9e5e1-115">เพื่อเรียกใช้สคริปต์ใน Power BI Desktop ตรวจสอบให้แน่ใจว่าสคริปต์ทำงานสำเร็จในพื้นที่ทำงานที่สร้างขึ้นใหม่และยังไม่ได้เปลี่ยนแปลงอะไร</span><span class="sxs-lookup"><span data-stu-id="9e5e1-115">To run the script in Power BI Desktop, make sure the script runs successfully in a new and unmodified workspace.</span></span> <span data-ttu-id="9e5e1-116">ข้อกำหนดเบื้องต้นนี้หมายความว่า ทุกแพคเกจและสคริปต์ที่ขึ้นต่อกัน ต้องโหลดและทำงานได้อย่างชัดเจน</span><span class="sxs-lookup"><span data-stu-id="9e5e1-116">This prerequisite means that all packages and dependencies must be explicitly loaded and run.</span></span> <span data-ttu-id="9e5e1-117">คุณสามารถใช้ `source()` เพื่อเรียกใช้สคริปต์ที่ขึ้นต่อกันได้</span><span class="sxs-lookup"><span data-stu-id="9e5e1-117">You can use `source()` to run dependent scripts.</span></span>

<span data-ttu-id="9e5e1-118">ในการเตรียมการและเรียกใช้สคริปต์ R ใน Power BI Desktop นั้น มีข้อจำกัดอยู่บางประการ:</span><span class="sxs-lookup"><span data-stu-id="9e5e1-118">When you prepare and run an R script in Power BI Desktop, there are a few limitations:</span></span>

* <span data-ttu-id="9e5e1-119">เฉพาะเฟรมข้อมูลเท่านั้นที่ถูกนำเข้า ดังนั้นให้ตรวจสอบแน่ใจว่าข้อมูลที่คุณต้องการนำเข้าไปยัง Power BI อยู่ในรูปเฟรมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9e5e1-119">Because only data frames are imported, remember to represent the data you want to import to Power BI in a data frame.</span></span>
* <span data-ttu-id="9e5e1-120">คอลัมน์ที่มีชนิดเป็นจำนวนเชิงซ้อนและเวกเตอร์จะไม่ถูกนำเข้า และจะถูกแทนที่ด้วยค่าผิดพลาดในตารางที่สร้างใหม่</span><span class="sxs-lookup"><span data-stu-id="9e5e1-120">Columns typed as Complex and Vector aren't imported, and they're replaced with error values in the created table.</span></span>
* <span data-ttu-id="9e5e1-121">ค่าที่เป็น `N/A`จะถูกแปลเป็นค่า`NULL` ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="9e5e1-121">Values that are `N/A` are translated to `NULL` values in Power BI Desktop.</span></span>
* <span data-ttu-id="9e5e1-122">ถ้าการเรียกใช้สคริปต์ R ทำงานนานกว่า 30 นาที จะหมดเวลา</span><span class="sxs-lookup"><span data-stu-id="9e5e1-122">If an R script runs longer than 30 minutes, it times out.</span></span>
* <span data-ttu-id="9e5e1-123">การเรียกแบบโต้ตอบในสคริปต์ R เช่นรอให้ผู้ใช้ป้อนข้อมูล จะหยุดการทำงานของสคริปต์</span><span class="sxs-lookup"><span data-stu-id="9e5e1-123">Interactive calls in the R script, such as waiting for user input, halts the script’s execution.</span></span>
* <span data-ttu-id="9e5e1-124">เมื่อตั้งค่าไดเรกทอรีการทำงานภายในสคริปต์ R คุณ *ต้อง* กำหนดเส้นทางแบบเต็มไปยังไดเรกทอรีการทำงาน แทนที่จะเป็นเส้นทางสัมพัทธ์</span><span class="sxs-lookup"><span data-stu-id="9e5e1-124">When setting the working directory within the R script, you *must* define a full path to the working directory, rather than a relative path.</span></span>

### <a name="run-your-r-script-and-import-data"></a><span data-ttu-id="9e5e1-125">เรียกใช้สคริปต์ R ของคุณ และนำเข้าข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9e5e1-125">Run your R script and import data</span></span>

<span data-ttu-id="9e5e1-126">ตอนนี้คุณสามารถเรียกใช้สคริปต์ R เพื่อนำเข้าข้อมูลไปยัง  Power BI Desktop ได้:</span><span class="sxs-lookup"><span data-stu-id="9e5e1-126">Now you can run your R script to import data into Power BI Desktop:</span></span>

1. <span data-ttu-id="9e5e1-127">ใน Power BI Desktop เลือก **รับข้อมูล** เลือก **สคริปต์ R** > **อื่นๆ**  จากนั้นเลือก **เชื่อมต่อ**:</span><span class="sxs-lookup"><span data-stu-id="9e5e1-127">In Power BI Desktop, select **Get Data**, choose **Other** > **R script**, and then select **Connect**:</span></span>

    ![เชื่อมต่อกับสคริปต์ R ประเภทอื่นๆ  กล่องข้อความรับข้อมูล Power BI Desktop](media/desktop-r-scripts/r-scripts-1.png)

2. <span data-ttu-id="9e5e1-129">ถ้า R ได้รับการติดตั้งลงในเครื่องของคุณ เพียงแค่คัดลอกสคริปต์ของคุณไปยังหน้าต่างสคริปต์ และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9e5e1-129">If R is installed on your local machine, just copy your script into the script window and select **OK**.</span></span> <span data-ttu-id="9e5e1-130">เวอร์ชันที่ติดตั้งล่าสุดจะแสดงเป็นเครื่องมือ R ของคุณ</span><span class="sxs-lookup"><span data-stu-id="9e5e1-130">The latest installed version is displayed as your R engine.</span></span>

    ![กล่องข้อความสคริปต์ R Power BI Desktop](media/desktop-r-scripts/r-scripts-2.png)

3. <span data-ttu-id="9e5e1-132">เลือก **ตกลง** เพื่อเรียกใช้สคริปต์ R</span><span class="sxs-lookup"><span data-stu-id="9e5e1-132">Select **OK** to run the R Script.</span></span> <span data-ttu-id="9e5e1-133">เมื่อสคริปต์ทำงานเสร็จเรียบร้อย คุณสามารถเลือกเฟรมข้อมูลผลลัพธ์ เพื่อเพิ่มไปยังรูปแบบ Power BI</span><span class="sxs-lookup"><span data-stu-id="9e5e1-133">When the script runs successfully, you can then choose the resulting data frames to add to the Power BI model.</span></span>

<span data-ttu-id="9e5e1-134">คุณสามารถควบคุมได้ว่าจะใช้การติดตั้ง R ใดในการเรียกใช้งานสคริปต์ข้อคุณ</span><span class="sxs-lookup"><span data-stu-id="9e5e1-134">You can control which R installation to use to run your script.</span></span> <span data-ttu-id="9e5e1-135">เพื่อระบุการตั้งค่าการติดตั้ง R ของคุณ เลือก **ไฟล์** > **ตัวเลือกและตั้งค่า** > **ตัวเลือก** จากนั้นเลือก **สคริปต์ R**</span><span class="sxs-lookup"><span data-stu-id="9e5e1-135">To specify your R installation settings, choose **File** > **Options and settings** > **Options**, then select **R scripting**.</span></span> <span data-ttu-id="9e5e1-136">ภายใต้ **ตัวเลือกของสคริปต์ R** รายการแบบดรอปดาวน์ **ไดเรกทอรีหน้าหลัก R ที่ตรวจพบ** แสดงตัวเลือกการติดตั้ง R ปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="9e5e1-136">Under **R script options**, the **Detected R home directories** dropdown list shows your current R installation choices.</span></span> <span data-ttu-id="9e5e1-137">ถ้าการติดตั้ง R ที่คุณต้องการไม่ได้อยู่ในรายการ ให้เลือก **อื่นๆ** จากนั้นเรียกดูหรือใส่โฟลเดอร์การติดตั้ง R ที่คุณต้องการใน **ตั้งค่าไดเรกทอรีหน้าหลัก R**</span><span class="sxs-lookup"><span data-stu-id="9e5e1-137">If the R installation you want isn't listed, pick **Other**, and then browse to or enter your preferred R installation folder in **Set an R home directory**.</span></span>

![ตัวเลือกสคริปต์ R กล่องข้อความตัวเลือก Power BI Desktop](media/desktop-r-scripts/r-scripts-4.png)

### <a name="refresh"></a><span data-ttu-id="9e5e1-139">Refresh</span><span class="sxs-lookup"><span data-stu-id="9e5e1-139">Refresh</span></span>

<span data-ttu-id="9e5e1-140">คุณสามารถรีเฟรชสคริปต์ R ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="9e5e1-140">You can refresh an R script in Power BI Desktop.</span></span> <span data-ttu-id="9e5e1-141">เมื่อคุณรีเฟรชสคริปต์ R, Power BI Desktop เรียกใช้สคริปต์ R อีกครั้งในสภาพแวดล้อมของ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="9e5e1-141">When you refresh an R script, Power BI Desktop runs the R script again in the Power BI Desktop environment.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9e5e1-142">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="9e5e1-142">Next steps</span></span>

<span data-ttu-id="9e5e1-143">ดูข้อมูลเพิ่มเติมเกี่ยวกับ R ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="9e5e1-143">Take a look at the following additional information about R in Power BI.</span></span>

* [<span data-ttu-id="9e5e1-144">สร้างภาพ Power BI ที่ใช้ R</span><span class="sxs-lookup"><span data-stu-id="9e5e1-144">Create Power BI visuals using R</span></span>](../create-reports/desktop-r-visuals.md)
* [<span data-ttu-id="9e5e1-145">ใช้ R IDE ภายนอกกับ Power BI</span><span class="sxs-lookup"><span data-stu-id="9e5e1-145">Use an external R IDE with Power BI</span></span>](desktop-r-ide.md)
