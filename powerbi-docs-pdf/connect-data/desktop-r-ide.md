---
title: ใช้ R IDE ภายนอกกับ Power BI
description: คุณสามารถเปิด IDE ภายนอกและใช้งาน IDE กับ Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 05/08/2019
LocalizationGroup: Connect to data
ms.openlocfilehash: 21b46a0c7637509fa54c3d7ed2b5551cde05f784
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96404881"
---
# <a name="use-an-external-r-ide-with-power-bi"></a><span data-ttu-id="df0a1-103">ใช้ R IDE ภายนอกกับ Power BI</span><span class="sxs-lookup"><span data-stu-id="df0a1-103">Use an external R IDE with Power BI</span></span>
<span data-ttu-id="df0a1-104">ด้วย **Power BI Desktop** คุณสามารถใช้ R IDE ภายนอกของคุณ (สภาพแวดล้อมรวมเพื่อการพัฒนา) เพื่อสร้าง และปรับปรุงสคริปต์ R จาก แล้วจะใช้สคริปต์เหล่านั้นใน Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="df0a1-104">With **Power BI Desktop**, you can use your external R IDE (Integrated Development Environment) to create and refine R scripts, then use those scripts in Power BI.</span></span>

![ภาพหน้าจอของกล่องโต้ตอบตัวเลือก ที่แสดงว่า R Studio ถูกป้อนในเขตข้อมูล R I D E ที่ตรวจพบ](media/desktop-r-ide/r-ide_1a.png)

## <a name="enable-an-external-r-ide"></a><span data-ttu-id="df0a1-106">เปิดใช้งานการ R IDE ภายนอก</span><span class="sxs-lookup"><span data-stu-id="df0a1-106">Enable an external R IDE</span></span>
<span data-ttu-id="df0a1-107">ก่อนหน้านี้ คุณจะต้องใช้ตัวแก้ไขสคริปต์ R ใน **Power BI Desktop** เพื่อสร้าง และเรียกใช้สคริปต์ R</span><span class="sxs-lookup"><span data-stu-id="df0a1-107">Previously, you had to use the R script editor in **Power BI Desktop** to create and run R scripts.</span></span> <span data-ttu-id="df0a1-108">กับการเผยแพร่นี้ คุณสามารถเปิดใช้ของคุณ R IDE ภายนอกจาก **Power BI Desktop** และจะนำเข้าข้อมูลของคุณโดยอัตโนมัติ และแสดงใน R IDE</span><span class="sxs-lookup"><span data-stu-id="df0a1-108">With this release, you can launch your external R IDE from **Power BI Desktop** and have your data automatically imported and displayed in the R IDE.</span></span> <span data-ttu-id="df0a1-109">จากที่นั่น คุณสามารถปรับเปลี่ยนสคริปต์ใน R IDE ภายนอก จากนั้นวางกลับลงใน **Power BI Desktop** เพื่อสร้างรูปภาพ Power BI และรายงานได้</span><span class="sxs-lookup"><span data-stu-id="df0a1-109">From there, you can modify the script in that external R IDE, then paste it back into **Power BI Desktop** to create Power BI visuals and reports.</span></span>

<span data-ttu-id="df0a1-110">ตั้งแต่ **Power BI Desktop** ที่วางจำหน่ายในเดือนกันยายน 2016(รุ่น 2.39.4526.362) คุณสามารถระบุ R IDE ที่คุณต้องการใช้ และได้เปิดใช้งานโดยอัตโนมัติจากภายใน **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="df0a1-110">Beginning with the September 2016 release of **Power BI Desktop** (version 2.39.4526.362), you can specify which R IDE you would like to use, and have it launch automatically from within **Power BI Desktop**.</span></span>

### <a name="requirements"></a><span data-ttu-id="df0a1-111">ข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="df0a1-111">Requirements</span></span>
<span data-ttu-id="df0a1-112">เมื่อต้องใช้คุณลักษณะนี้ คุณจำเป็นต้องติดตั้ง **R IDE** บนเครื่องคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="df0a1-112">To use this feature, you need to install an **R IDE** on your local computer.</span></span> <span data-ttu-id="df0a1-113">**Power BI Desktop** ไม่รวมการนำเข้าใช้หรือการติดตั้ง R engine ดังนั้นคุณต้องติดตั้ง **R** แบบบนเครื่องคอมพิวเตอร์ของคุณแบบแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="df0a1-113">**Power BI Desktop** does not include, deploy, or install the R engine, so you must separately install **R** on your local computer.</span></span> <span data-ttu-id="df0a1-114">คุณสามารถเลือก R IDE ที่จะใช้ ด้วยตัวเลือกต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="df0a1-114">You can choose which R IDE to use, with the following options:</span></span>

* <span data-ttu-id="df0a1-115">คุณสามารถติดตั้ง R IDE ตัวโปรดของคุณ ซึ่งมีจำนวนมากที่ใช้งานฟรี เช่น[Revolution Open download page](https://mran.revolutionanalytics.com/download/)และ[CRAN Repository](https://cran.r-project.org/bin/windows/base/) ได้</span><span class="sxs-lookup"><span data-stu-id="df0a1-115">You can install your favorite R IDE, many of which are available for free, such as the [Revolution Open download page](https://mran.revolutionanalytics.com/download/), and the [CRAN Repository](https://cran.r-project.org/bin/windows/base/).</span></span>
* <span data-ttu-id="df0a1-116">**Power BI Desktop** ยัง สนับสนุน [R Studio](https://www.rstudio.com/)และ **Visual Studio 2015** กับ [*เครื่องมือ R สำหรับ Visual Studio*](/visualstudio/rtvs)editor</span><span class="sxs-lookup"><span data-stu-id="df0a1-116">**Power BI Desktop** also supports [R Studio](https://www.rstudio.com/) and **Visual Studio 2015** with [*R Tools for Visual Studio*](/visualstudio/rtvs) editors.</span></span>
* <span data-ttu-id="df0a1-117">นอกจากนี้คุณสามารถติดตั้ง R IDE ที่แตกต่างกัน และมี **Power BI Desktop** เปิดใช้งานที่ **R IDE** โดยทำอย่างใดอย่างหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="df0a1-117">You can also install a different R IDE and have **Power BI Desktop** launch that **R IDE** by doing one of the following:</span></span>
  
  * <span data-ttu-id="df0a1-118">คุณสามารถเชื่อมโยงไฟล์ **.R** จาก IDE ภายนอกที่คุณต้องการให้ **Power BI Desktop** เพื่อเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="df0a1-118">You can associate **.R** files with the external IDE you want **Power BI Desktop** to launch.</span></span>
  * <span data-ttu-id="df0a1-119">คุณสามารถระบุ.exe ที่ **Power BI Desktop** สามารถใช้งาน โดยเลือก *อื่น ๆ* จากการ **ตัวเลือก R Script** ส่วนของ **ตัวเลือก** แบบโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="df0a1-119">You can specify the .exe that **Power BI Desktop** should launch by selecting *Other* from the **R Script Options** section of the **Options** dialog.</span></span> <span data-ttu-id="df0a1-120">คุณสามารถนำกล่องโต้ตอบ **ตัวเลือก** โดยไปที่ **ไฟล์ > ตัวเลือกและการตั้งค่า > ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="df0a1-120">You can bring up the **Options** dialog by going to **File > Options and settings > Options**.</span></span>
    
    ![ภาพหน้าจอของกล่องโต้ตอบตัวเลือก ที่แสดงว่าตัวเลือกอื่น ๆ ถูกป้อนในเขตข้อมูล R I D E ที่ตรวจพบเพื่อระบุ R I D E ที่ต้องการ](media/desktop-r-ide/r-ide_1b.png)

<span data-ttu-id="df0a1-122">ถ้าคุณมี R IDE หลายตัวติดตั้อยู่ง คุณสามารถระบุได้ว่าจะเปิดตัวใด โดยการเลือก *R IDE ที่ตรวจพบ* การดรอปดาวน์ในกล่องโต้ตอบ **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="df0a1-122">If you have multiple R IDEs installed, you can specify which will be launched by selecting it from the *Detected R IDEs* drop-down in the **Options** dialog.</span></span>

<span data-ttu-id="df0a1-123">ตามค่าเริ่มต้น ถ้ามีการติดตั้งบนคอมพิวเตอร์ของคุณภาย **Power BI Desktop** จะเปิด **R Studio** เป็นแบบ R IDE ภายนอก ถ้า **R Studio** ไม่ได้ติดตั้งและคุณมี **Visual Studio 2015** กับ **R Tools สำหรับ Visual Studio** มันจะเปิดใช้แทน</span><span class="sxs-lookup"><span data-stu-id="df0a1-123">By default, **Power BI Desktop** will launch **R Studio** as the external R IDE if it's installed on your local computer; if **R Studio** is not installed and you have **Visual Studio 2015** with **R Tools for Visual Studio**, that will be launched instead.</span></span> <span data-ttu-id="df0a1-124">ถ้าไม่มี R IDE ใดเลยติดตั้งอยู่ แอปพลิเคชันที่เชื่อมโยงกับไฟล์ **R** จะถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="df0a1-124">If neither of those R IDEs is installed, the application associated with **.R** files is launched.</span></span>

<span data-ttu-id="df0a1-125">และถ้าหากไม่มีความสัมพันธ์ของไฟล์ **.R** อาจเป็นไปได้ที่จะต้องระบุเส้นทางไปยัง IDE แบบกำหนดเอง ใน *เรียกดู R IDE ที่คุณต้องการ* ส่วนของ **กล่องโต้ตอบ** ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="df0a1-125">And if no **.R** file association exists, it's possible to specify a path to a custom IDE in the *Browse to your preferred R IDE* section of the **Options** dialog.</span></span> <span data-ttu-id="df0a1-126">คุณยังสามารถเปิดใช้ R IDE อื่น โดยการเลือกตัว **ตั้งค่า** ไอคอนรูปเฟืองด้านข้าง **เปิดใช้ R IDE** ไอคอนลูกศร ใน **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="df0a1-126">You can also launch a different R IDE by selecting the **Settings** gear icon beside the **Launch R IDE** arrow icon, in **Power BI Desktop**.</span></span>

## <a name="launch-an-r-ide-from-power-bi-desktop"></a><span data-ttu-id="df0a1-127">เปิดใช้การ R IDE จาก Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="df0a1-127">Launch an R IDE from Power BI Desktop</span></span>
<span data-ttu-id="df0a1-128">เมื่อต้องการเปิดใช้การ R IDE จาก **Power BI Desktop** ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="df0a1-128">To launch an R IDE from **Power BI Desktop**, take the following steps:</span></span>

1. <span data-ttu-id="df0a1-129">โหลดข้อมูลลงใน **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="df0a1-129">Load data into **Power BI Desktop**.</span></span>
2. <span data-ttu-id="df0a1-130">เลือกเขตข้อมูลบางอย่างจากบานหน้าต่าง **เขตข้อมูล** ที่คุณต้องการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="df0a1-130">Select some fields from the **Fields** pane that you want to work with.</span></span> <span data-ttu-id="df0a1-131">ถ้าคุณยังไม่ได้เปิดใช้งานรูปของสคริปต์ คุณจะได้ถูกถามให้ทำเช่นนั้น</span><span class="sxs-lookup"><span data-stu-id="df0a1-131">If you haven't enabled script visuals yet, you'll be prompted to do so.</span></span>
   
   ![ภาพหน้าจอของกล่องโต้ตอบเปิดใช้งานวิชวลสคริปต์ ที่แสดงการส่งข้อมูลแจ้งเตือนให้เปิดใช้งานวิชวลสคริปต์](media/desktop-r-ide/r-ide_3.png)
3. <span data-ttu-id="df0a1-133">เมื่อเปิดใช้งานรูปของสคริปต์ คุณจะสามารถเลือกรูป R จากบานหน้าต่าง **แสดงภาพ** ซึ่งสร้างภาพ R แบบว่างที่พร้อมที่จะแสดงผลลัพธ์ของสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="df0a1-133">When script visuals are enabled, you can select an R visual from the **Visualizations** pane, which creates a blank R visual that's ready to display the results of your script.</span></span> <span data-ttu-id="df0a1-134">บานหน้าต่าง **ตัวแก้ไขสคริปต์ R** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="df0a1-134">The **R script editor** pane also appears.</span></span>
   
   ![ภาพหน้าจอของบานหน้าต่างการแสดงภาพ ที่แสดงวิชวล R ที่ว่างเปล่า](media/desktop-r-ide/r-ide_4.png)
4. <span data-ttu-id="df0a1-136">ตอนนี้ คุณสามารถเลือกเขตข้อมูลคุณต้องการใช้ในสคริปต์ R ของคุณ</span><span class="sxs-lookup"><span data-stu-id="df0a1-136">Now you can select the fields you want to use in your R script.</span></span> <span data-ttu-id="df0a1-137">เมื่อคุณเลือกเขตข้อมูล เขตข้อมูล **ตัวแก้ไขสคริปต์ R** จะถูกสร้างขึ้นแบบอัตโนมัติโดยเป็นไปตามเขตข้อมูลที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="df0a1-137">When you select a field, the **R script editor** field automatically creates script code based on the field or fields you select.</span></span> <span data-ttu-id="df0a1-138">คุณสามารถสร้าง (หรือวาง) สคริปต์ R ของคุณโดยตรงในบานหน้าต่าง **ตัวแก้ไขสคริปต์ R** หรือคุณสามารถปล่อยให้ว่างเปล่าก็ได้</span><span class="sxs-lookup"><span data-stu-id="df0a1-138">You can either create (or paste) your R script directly in the **R script editor** pane, or you can leave it empty.</span></span>
   
   ![ภาพหน้าจอของบานหน้าต่างการแสดงภาพ ที่แสดงวิชวล R ที่ว่างเปล่าพร้อมด้วยสคริปต์ในเครื่องมือแก้ไขสคริปต์](media/desktop-r-ide/r-ide_5.png)
   
   > [!NOTE]
   > <span data-ttu-id="df0a1-140">ชนิดการรวมเริ่มต้นสำหรับวิชวล R คือ *ไม่ต้องทำการสรุป*</span><span class="sxs-lookup"><span data-stu-id="df0a1-140">The default aggregation type for R visuals is *do not summarize*.</span></span>
   > 
   > 
5. <span data-ttu-id="df0a1-141">ขณะนี้คุณสามารถเปิดใช้ R IDE ของคุณได้โดยตรงจาก **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="df0a1-141">You can now launch your R IDE directly from **Power BI Desktop**.</span></span> <span data-ttu-id="df0a1-142">เลือกปุ่ม **เปิดใช้ R IDE** พบบนด้านขวาของแถบชื่อ **R script editor** ตามที่แสดงด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="df0a1-142">Select the **Launch R IDE** button, found on the right side of the **R script editor** title bar, as shown below.</span></span>
   
   ![ภาพหน้าจอของบานหน้าต่าง R I D E ที่แสดงวิธีการเปิดใช้งานจากปุ่ม R I D E](media/desktop-r-ide/r-ide_6.png)
6. <span data-ttu-id="df0a1-144">R IDE ของคุณระบุจะเริ่มทำงาน โดย Power BI Desktop ดังที่แสดงในรูปต่อไปนี้ (ในรูปภาพนี้ **RStudio** เป็น R IDE เริ่มต้น)</span><span class="sxs-lookup"><span data-stu-id="df0a1-144">Your specified R IDE is launched by Power BI Desktop, as shown in the following image (in this image, **RStudio** is the default R IDE).</span></span>
   
   ![ภาพหน้าจอของ R I D E ที่เปิดใช้งานใน Power B I Desktop ที่แสดงใน R Studio](media/desktop-r-ide/r-ide_7.png)
   
   > [!NOTE]
   > <span data-ttu-id="df0a1-146">**Power BI Desktop** เพิ่มสามบรรทัดแรกของสคริปต์ แล้วจึงค่อยสามารถนำเข้าข้อมูลของคุณจาก **Power BI Desktop** เมื่อคุณเรียกใช้สคริปต์</span><span class="sxs-lookup"><span data-stu-id="df0a1-146">**Power BI Desktop** adds the first three lines of the script so it can import your data from **Power BI Desktop** once you run the script.</span></span>
   > 
   > 
7. <span data-ttu-id="df0a1-147">สคริปต์ใด ๆ ที่คุณสร้างขึ้นใน **บานหน้าต่างตัวแก้ไขสคริปต์ R** ของ **Power BI Desktop** จะปรากฏเริ่มต้นในบรรทัดที่ 4 ใน R IDE ของคุณ</span><span class="sxs-lookup"><span data-stu-id="df0a1-147">Any script you created in the **R script editor pane** of **Power BI Desktop** appears starting in line 4 in your R IDE.</span></span> <span data-ttu-id="df0a1-148">ในตอนนี้ คุณสามารถสร้างสคริปต์ R ของคุณใน R IDE</span><span class="sxs-lookup"><span data-stu-id="df0a1-148">At this point, you can create your R script in the R IDE.</span></span> <span data-ttu-id="df0a1-149">เมื่อสคริปต์ R ของคุณนั้สร้างเสร็จสมบูรณ์แล้วใน R IDE ของคุณ คุณจำเป็นต้องคัดลอก และวางไว้ **ตัวแก้ไขสคริปต์ R** บานหน้าต่างใน **Power BI Desktop** *ยกเว้น* สามบรรทัดแรกของตัว สคริปต์ที่ **Power BI Desktop** สร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="df0a1-149">Once your R script is complete in your R IDE, you need to copy and paste it back into the **R script editor** pane in **Power BI Desktop**, *excluding* the first three lines of the script that **Power BI Desktop** automatically generated.</span></span> <span data-ttu-id="df0a1-150">ห้ามคัดลอกสามบรรทัดแรกของสคริปต์กลับเข้าไปใน **Power BI Desktop** บรรทัดเหล่านั้นถูกใช้เพื่อนำเข้าข้อมูลของคุณไปยัง R IDE ของคุณจากเท่านั้น **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="df0a1-150">Do not copy the first three lines of script back into **Power BI Desktop**, those lines were only used to import your data to your R IDE from **Power BI Desktop**.</span></span>

### <a name="known-limitations"></a><span data-ttu-id="df0a1-151">ข้อจำกัดที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="df0a1-151">Known limitations</span></span>
<span data-ttu-id="df0a1-152">เปิดใช้งาน R IDE ได้โดยตรงจาก Power BI Desktop มีข้อจำกัดบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="df0a1-152">Launching an R IDE directly from Power BI Desktop has a few limitations:</span></span>

* <span data-ttu-id="df0a1-153">การส่งออกสคริปต์โดยอัตโนมัติจาก R IDE ของคุณไปยัง **Power BI Desktop** ยังทำไม่ได้</span><span class="sxs-lookup"><span data-stu-id="df0a1-153">Automatically exporting your script from your R IDE into **Power BI Desktop** is not supported.</span></span>
* <span data-ttu-id="df0a1-154">ตัวแก้ไข **ไคลเอ็นต์ R**(RGui.exe) ไม่ถูกรองรับ เนื่องจากตัวแก้ไขเองก็ไม่รองรับเปิดไฟล์</span><span class="sxs-lookup"><span data-stu-id="df0a1-154">**R Client** editor (RGui.exe) is not supported, because the editor itself does not support opening files.</span></span>

## <a name="next-steps"></a><span data-ttu-id="df0a1-155">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="df0a1-155">Next steps</span></span>
<span data-ttu-id="df0a1-156">ดูข้อมูลเพิ่มเติมเกี่ยวกับ R ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="df0a1-156">Take a look at the following additional information about R in Power BI.</span></span>

* [<span data-ttu-id="df0a1-157">การเรียกใช้สคริปต์ R ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="df0a1-157">Running R Scripts in Power BI Desktop</span></span>](desktop-r-scripts.md)
* [<span data-ttu-id="df0a1-158">สร้างภาพ Power BI ที่ใช้ R</span><span class="sxs-lookup"><span data-stu-id="df0a1-158">Create Power BI visuals using R</span></span>](../create-reports/desktop-r-visuals.md)
