---
title: ใช้ Python IDE ภายนอกกับ Power BI
description: คุณสามารถเปิดและใช้ IDE ภายนอกกับ Power BI
author: otarb
ms.author: otarb
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 06/18/2018
LocalizationGroup: Connect to data
ms.openlocfilehash: c93c358f79b77a9cdda51eb815c35e674150cc39
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411091"
---
# <a name="use-an-external-python-ide-with-power-bi"></a><span data-ttu-id="7b674-103">ใช้ Python IDE ภายนอกกับ Power BI</span><span class="sxs-lookup"><span data-stu-id="7b674-103">Use an external Python IDE with Power BI</span></span>
<span data-ttu-id="7b674-104">ด้วย **Power BI Desktop** คุณสามารถใช้ Python IDE ภายนอกของคุณ (สภาพแวดล้อมรวมเพื่อการพัฒนา) เพื่อสร้าง และปรับปรุงสคริปต์ Python แล้วจะใช้สคริปต์เหล่านั้นใน Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="7b674-104">With **Power BI Desktop**, you can use your external Python IDE (Integrated Development Environment) to create and refine Python scripts, then use those scripts in Power BI.</span></span>

![ภาพหน้าจอของกล่องโต้ตอบตัวเลือก ที่แสดง Visual Studio Code ที่ป้อนในเขตข้อมูล Python IDE ที่ตรวจพบ](media/desktop-python-ide/python-ide-1.png)

## <a name="enable-an-external-python-ide"></a><span data-ttu-id="7b674-106">เปิดใช้งานการ Python IDE ภายนอก</span><span class="sxs-lookup"><span data-stu-id="7b674-106">Enable an external Python IDE</span></span>
<span data-ttu-id="7b674-107">คุณสามารถเปิดใช้ของคุณ Python IDE ภายนอกจาก **Power BI Desktop** และจะนำเข้าข้อมูลของคุณโดยอัตโนมัติ และแสดงใน Python IDE</span><span class="sxs-lookup"><span data-stu-id="7b674-107">You can launch your external Python IDE from **Power BI Desktop** and have your data automatically imported and displayed in the Python IDE.</span></span> <span data-ttu-id="7b674-108">จากที่นั่น คุณสามารถปรับเปลี่ยนสคริปต์ใน Python IDE ภายนอก จากนั้นวางกลับลงใน **Power BI Desktop** เพื่อสร้างวิชวลและรายงาน Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="7b674-108">From there, you can modify the script in that external Python IDE, then paste it back into **Power BI Desktop** to create Power BI visuals and reports.</span></span>

<span data-ttu-id="7b674-109">คุณสามารถระบุว่าต้องการใช้ Python IDE แบบใดและเปิดใช้งานได้โดยอัตโนมัติภายใน **Power BI Desktop** หรือไม่</span><span class="sxs-lookup"><span data-stu-id="7b674-109">You can specify which Python IDE you would like to use, and have it launch automatically from within **Power BI Desktop**.</span></span>

### <a name="requirements"></a><span data-ttu-id="7b674-110">ข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="7b674-110">Requirements</span></span>
<span data-ttu-id="7b674-111">เมื่อต้องใช้คุณลักษณะนี้ คุณจำเป็นต้องติดตั้ง **Python IDE** บนเครื่องคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7b674-111">To use this feature, you need to install a **Python IDE** on your local computer.</span></span> <span data-ttu-id="7b674-112">**Power BI Desktop** ไม่รวมการนำเข้าใช้หรือการติดตั้ง Python engine ดังนั้นคุณต้องติดตั้ง **Python** แบบบนเครื่องคอมพิวเตอร์ของคุณแบบแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="7b674-112">**Power BI Desktop** does not include, deploy, or install the Python engine, so you must separately install **Python** on your local computer.</span></span> <span data-ttu-id="7b674-113">คุณสามารถเลือก Python IDE ที่จะใช้ ด้วยตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7b674-113">You can choose which Python IDE to use, with the following options:</span></span>

* <span data-ttu-id="7b674-114">คุณสามารถติดตั้ง Python IDE ตัวโปรดของคุณ ซึ่งมีจำนวนมากที่ใช้งานฟรี เช่น [หน้าดาวน์โหลด Visual Studio Code](https://code.visualstudio.com/download/)</span><span class="sxs-lookup"><span data-stu-id="7b674-114">You can install your favorite Python IDE, many of which are available for free, such as the [Visual Studio Code download page](https://code.visualstudio.com/download/).</span></span>
* <span data-ttu-id="7b674-115">**Power BI Desktop** ยังรองรับ **Visual Studio** อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="7b674-115">**Power BI Desktop** also supports **Visual Studio**.</span></span>
* <span data-ttu-id="7b674-116">นอกจากนี้คุณยังสามารถติดตั้ง Python IDE ที่แตกต่างกันและมี **Power BI Desktop** ซึ่งเปิดใช้งานที่ **Python IDE** โดยทำอย่างใดอย่างหนึ่งต่อไปนี้ได้อีกด้วย:</span><span class="sxs-lookup"><span data-stu-id="7b674-116">You can also install a different Python IDE and have **Power BI Desktop** launch that **Python IDE** by doing one of the following:</span></span>
  
  * <span data-ttu-id="7b674-117">คุณสามารถเชื่อมโยงไฟล์ **.PY** จาก IDE ภายนอกที่คุณต้องการเปิดใช้งาน **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="7b674-117">You can associate **.PY** files with the external IDE you want **Power BI Desktop** to launch.</span></span>
  * <span data-ttu-id="7b674-118">คุณสามารถระบุไฟล์ .exe ที่ **Power BI Desktop** ควรเปิดใช้งานโดยเลือก *อื่น ๆ* จากส่วน **ตัวเลือกสคริปต์ Python** ในกล่องโต้ตอบ **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="7b674-118">You can specify the .exe that **Power BI Desktop** should launch by selecting *Other* from the **Python Script Options** section of the **Options** dialog.</span></span> <span data-ttu-id="7b674-119">คุณสามารถนำกล่องโต้ตอบ **ตัวเลือก** โดยไปที่ **ไฟล์ > ตัวเลือกและการตั้งค่า > ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="7b674-119">You can bring up the **Options** dialog by going to **File > Options and settings > Options**.</span></span>
    
    ![ภาพหน้าจอของกล่องโต้ตอบตัวเลือก ที่แสดงโปรแกรมอื่นที่ป้อนในเขตข้อมูล Python IDE ที่ตรวจพบ](media/desktop-python-ide/python-ide-2.png)

<span data-ttu-id="7b674-121">ถ้าคุณติดตั้ง Python IDE หลายตัว คุณสามารถระบุได้ว่าจะเปิดตัวใด โดยการเลือกเมนูดรอปดาวน์ *Python IDE ที่ตรวจพบ* ในกล่องโต้ตอบ **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="7b674-121">If you have multiple Python IDEs installed, you can specify which will be launched by selecting it from the *Detected Python IDEs* drop-down in the **Options** dialog.</span></span>

<span data-ttu-id="7b674-122">โดยค่าเริ่มต้น **Power BI Desktop** จะเรียกใช้งาน **Visual Studio Code** เป็น IDE ภายนอกของ Python หากมีการติดตั้งไว้ในเครื่องคอมพิวเตอร์ของคุณ ถ้าไม่ได้มีการติดตั้ง **Visual Studio Code** และคุณมี **Visual Studio** โปรแกรมนี้จะเริ่มทำงานแทน</span><span class="sxs-lookup"><span data-stu-id="7b674-122">By default, **Power BI Desktop** will launch **Visual Studio Code** as the external Python IDE if it's installed on your local computer; if **Visual Studio Code** is not installed and you have **Visual Studio**, that will be launched instead.</span></span> <span data-ttu-id="7b674-123">ถ้าไม่มีการติดตั้ง Python IDE อยู่เลย แอปพลิเคชันที่เชื่อมโยงกับไฟล์  **.PY** จะถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7b674-123">If neither of those Python IDEs is installed, the application associated with **.PY** files is launched.</span></span>

<span data-ttu-id="7b674-124">และถ้าหากไม่มีความสัมพันธ์ของไฟล์ **.PY** อาจเป็นไปได้ที่จะต้องระบุเส้นทางไปยัง IDE แบบกำหนดเอง ใน *เรียกดู Python IDE ที่คุณต้องการ* ส่วนของ **กล่องโต้ตอบ** ตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="7b674-124">And if no **.PY** file association exists, it's possible to specify a path to a custom IDE in the *Browse to your preferred Python IDE* section of the **Options** dialog.</span></span> <span data-ttu-id="7b674-125">คุณยังสามารถเปิดใช้ Python IDE อื่น โดยการเลือกไอคอนรูปเฟืองด้านข้าง **ตั้งค่า** **เปิดใช้ไอคอนลูกศรของ Python IDE** ใน **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="7b674-125">You can also launch a different Python IDE by selecting the **Settings** gear icon beside the **Launch Python IDE** arrow icon, in **Power BI Desktop**.</span></span>

## <a name="launch-a-python-ide-from-power-bi-desktop"></a><span data-ttu-id="7b674-126">เปิดใช้งาน Python IDE จาก Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="7b674-126">Launch a Python IDE from Power BI Desktop</span></span>
<span data-ttu-id="7b674-127">เมื่อต้องการเปิดใช้งาน Python IDE จาก **Power BI Desktop** ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7b674-127">To launch a Python IDE from **Power BI Desktop**, take the following steps:</span></span>

1. <span data-ttu-id="7b674-128">โหลดข้อมูลลงใน **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="7b674-128">Load data into **Power BI Desktop**.</span></span>
2. <span data-ttu-id="7b674-129">เลือกเขตข้อมูลบางอย่างจากบานหน้าต่าง **เขตข้อมูล** ที่คุณต้องการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7b674-129">Select some fields from the **Fields** pane that you want to work with.</span></span> <span data-ttu-id="7b674-130">ถ้าคุณยังไม่ได้เปิดใช้งานรูปของสคริปต์ คุณจะได้ถูกถามให้ทำเช่นนั้น</span><span class="sxs-lookup"><span data-stu-id="7b674-130">If you haven't enabled script visuals yet, you'll be prompted to do so.</span></span>
   
   ![ภาพหน้าจอของกล่องโต้ตอบเปิดใช้งานวิชวลสคริปต์ ที่พรอมท์คุณให้เปิดใช้งาน](media/desktop-python-ide/python-ide-3.png)
3. <span data-ttu-id="7b674-132">เมื่อเปิดใช้งานวิชวลของสคริปต์ คุณจะสามารถเลือกรูป Python จากบานหน้าต่าง **การแสดงวิชวล** ซึ่งสร้างวิชวล Python แบบว่างที่พร้อมที่จะแสดงผลลัพธ์ของสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7b674-132">When script visuals are enabled, you can select a Python visual from the **Visualizations** pane, which creates a blank Python visual that's ready to display the results of your script.</span></span> <span data-ttu-id="7b674-133">บานหน้าต่าง **ตัวแก้ไขสคริปต์ Python** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="7b674-133">The **Python script editor** pane also appears.</span></span>
   
   ![ภาพหน้าจอของบานหน้าต่างการแสดงผลข้อมูลด้วยภาพ ที่แสดงวิชวล Python ที่ว่างเปล่า](media/desktop-python-ide/python-ide-4.png)
4. <span data-ttu-id="7b674-135">ตอนนี้ คุณสามารถเลือกเขตข้อมูลที่คุณต้องการใช้ในสคริปต์ Python ได้</span><span class="sxs-lookup"><span data-stu-id="7b674-135">Now you can select the fields you want to use in your Python script.</span></span> <span data-ttu-id="7b674-136">เมื่อคุณเลือกเขตข้อมูล เขตข้อมูล **ตัวแก้ไขสคริปต์ Python** จะถูกสร้างขึ้นแบบอัตโนมัติโดยเป็นไปตามเขตข้อมูลที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="7b674-136">When you select a field, the **Python script editor** field automatically creates script code based on the field or fields you select.</span></span> <span data-ttu-id="7b674-137">คุณสามารถสร้าง (หรือวาง) สคริปต์ Python ของคุณโดยตรงในบานหน้าต่าง **ตัวแก้ไขสคริปต์ Python** หรือคุณสามารถปล่อยให้ว่างเปล่าก็ได้</span><span class="sxs-lookup"><span data-stu-id="7b674-137">You can either create (or paste) your Python script directly in the **Python script editor** pane, or you can leave it empty.</span></span>
   
   ![ภาพหน้าจอของบานหน้าต่างการแสดงผลข้อมูลด้วยภาพ ที่แสดงวิชวล Python ที่ว่างเปล่าพร้อมโค้ดสคริปต์ในตัวแก้ไขสคริปต์](media/desktop-python-ide/python-ide-5.png)
   
   > [!NOTE]
   > <span data-ttu-id="7b674-139">ชนิดการรวมเริ่มต้นสำหรับวิชวล Python คือ *ไม่ต้องทำการสรุป*</span><span class="sxs-lookup"><span data-stu-id="7b674-139">The default aggregation type for Python visuals is *do not summarize*.</span></span>
   > 
   > 
5. <span data-ttu-id="7b674-140">ขณะนี้คุณสามารถเปิดใช้ Python IDE ของคุณได้โดยตรงจาก **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="7b674-140">You can now launch your Python IDE directly from **Power BI Desktop**.</span></span> <span data-ttu-id="7b674-141">เลือกปุ่ม **เปิดใช้ Python IDE** ที่พบบนด้านขวาของแถบชื่อ **ตัวแก้ไขสคริปต์ Python** ตามที่แสดงด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="7b674-141">Select the **Launch Python IDE** button, found on the right side of the **Python script editor** title bar, as shown below.</span></span>
   
   ![ภาพหน้าจอของตัวแก้ไขสคริปต์ Python ที่แสดงวิธีการเปิดใช้งาน Python IDE](media/desktop-python-ide/python-ide-6.png)
6. <span data-ttu-id="7b674-143">Power BI Desktop เรียกใช้งาน Python IDE ที่ระบุของคุณ ดังที่แสดงในรูปต่อไปนี้ (ในภาพนี้ **Visual Studio Code** เป็น Python IDE ค่าเริ่มต้น)</span><span class="sxs-lookup"><span data-stu-id="7b674-143">Your specified Python IDE is launched by Power BI Desktop, as shown in the following image (in this image, **Visual Studio Code** is the default Python IDE).</span></span>
   
   ![ภาพหน้าจอของ Python IDE ที่แสดงใน Visual Studio Code](media/desktop-python-ide/python-ide-7.png)
   
   > [!NOTE]
   > <span data-ttu-id="7b674-145">**Power BI Desktop** เพิ่มสามบรรทัดแรกของสคริปต์ แล้วจึงค่อยสามารถนำเข้าข้อมูลของคุณจาก **Power BI Desktop** เมื่อคุณเรียกใช้สคริปต์</span><span class="sxs-lookup"><span data-stu-id="7b674-145">**Power BI Desktop** adds the first three lines of the script so it can import your data from **Power BI Desktop** once you run the script.</span></span>
   > 
   > 
7. <span data-ttu-id="7b674-146">สคริปต์ใด ๆ ที่คุณสร้างขึ้นใน **บานหน้าต่างตัวแก้ไขสคริปต์ Python** ของ **Power BI Desktop** จะปรากฏเริ่มต้นในบรรทัดที่ 4 ใน Python IDE ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7b674-146">Any script you created in the **Python script editor pane** of **Power BI Desktop** appears starting in line 4 in your Python IDE.</span></span> <span data-ttu-id="7b674-147">ในตอนนี้ คุณสามารถสร้างสคริปต์ Python ของคุณใน Python IDE ได้</span><span class="sxs-lookup"><span data-stu-id="7b674-147">At this point, you can create your Python script in the Python IDE.</span></span> <span data-ttu-id="7b674-148">เมื่อคุณสร้างสคริปต์ Python เสร็จสมบูรณ์แล้วใน Python IDE ของคุณ คุณจำเป็นต้องคัดลอกและวางสคริปต์กลับเข้าไปยังบานหน้าต่าง **ตัวแก้ไขสคริปต์ Python** ใน \**Power BI Desktop\*\*\*ยกเว้น* สามบรรทัดแรกของตัวสคริปต์ที่ **Power BI Desktop** สร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7b674-148">Once your Python script is complete in your Python IDE, you need to copy and paste it back into the **Python script editor** pane in **Power BI Desktop**, *excluding* the first three lines of the script that **Power BI Desktop** automatically generated.</span></span> <span data-ttu-id="7b674-149">ห้ามคัดลอกสามบรรทัดแรกของสคริปต์กลับเข้าไปใน **Power BI Desktop** ซึ่งบรรทัดเหล่านั้นถูกใช้เพื่อนำเข้าข้อมูลของคุณไปยัง Python IDE ของคุณเท่านั้นจาก **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="7b674-149">Do not copy the first three lines of script back into **Power BI Desktop**, those lines were only used to import your data to your Python IDE from **Power BI Desktop**.</span></span>

### <a name="known-limitations"></a><span data-ttu-id="7b674-150">ข้อจำกัดที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="7b674-150">Known limitations</span></span>
<span data-ttu-id="7b674-151">การเปิดใช้งาน Python IDE โดยตรงจาก Power BI Desktop มีข้อจำกัดบางอย่าง:</span><span class="sxs-lookup"><span data-stu-id="7b674-151">Launching a Python IDE directly from Power BI Desktop has a few limitations:</span></span>

* <span data-ttu-id="7b674-152">ระบบยังไม่รองรับการส่งออกสคริปต์จาก Python IDE ของคุณไปยัง **Power BI Desktop** โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7b674-152">Automatically exporting your script from your Python IDE into **Power BI Desktop** is not supported.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7b674-153">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="7b674-153">Next steps</span></span>
<span data-ttu-id="7b674-154">ดูข้อมูลเพิ่มเติมเกี่ยวกับ Python ใน Power BI ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7b674-154">Take a look at the following additional information about Python in Power BI.</span></span>

* [<span data-ttu-id="7b674-155">การเรียกใช้สคริปต์ Python ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="7b674-155">Running Python Scripts in Power BI Desktop</span></span>](desktop-python-scripts.md)
* [<span data-ttu-id="7b674-156">สร้างวิชวลของ Power BI โดยใช้ Python</span><span class="sxs-lookup"><span data-stu-id="7b674-156">Create Power BI visuals using Python</span></span>](desktop-python-visuals.md)

