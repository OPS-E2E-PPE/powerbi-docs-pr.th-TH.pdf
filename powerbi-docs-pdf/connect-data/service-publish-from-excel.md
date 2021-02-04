---
title: เผยแพร่ไปยัง Power BI จาก Microsoft Excel
description: เรียนรู้วิธีการเผยแพร่สมุดงาน Excel ไปยังไซต์ Power BI ของคุณ
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 05/05/2020
LocalizationGroup: Data from files
ms.openlocfilehash: 1473cdace4a1c6435ea7c2cf405785f144616d87
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410194"
---
# <a name="publish-to-power-bi-from-microsoft-excel"></a><span data-ttu-id="8dd4b-103">เผยแพร่ไปยัง Power BI จาก Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="8dd4b-103">Publish to Power BI from Microsoft Excel</span></span>
<span data-ttu-id="8dd4b-104">ด้วย Microsoft Excel 2016 และรุ่นใหม่กว่า คุณสามารถเผยแพร่สมุดงาน Excel ของคุณไปยังพื้นที่ทำงาน [Power BI](https://powerbi.microsoft.com) ได้โดยตรง ซึ่งเป็นที่ที่คุณสามารถสร้างรายงานและแดชบอร์ดแบบโต้ตอบสูงตามข้อมูลของสมุดงานของคุณได้</span><span class="sxs-lookup"><span data-stu-id="8dd4b-104">With Microsoft Excel 2016 and later, you can publish your Excel workbooks directly to your [Power BI](https://powerbi.microsoft.com) workspace, where you can create highly interactive reports and dashboards based on your workbook’s data.</span></span> <span data-ttu-id="8dd4b-105">จากนั้นคุณสามารถแชร์ข้อมูลเชิงลึกของคุณกับผู้อื่นในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="8dd4b-105">You can then share your insights with others in your organization.</span></span>

![อัปโหลดสมุดงานของคุณไปยัง Power BI](media/service-publish-from-excel/pbi_uploadexport2.png)

<span data-ttu-id="8dd4b-107">เมื่อเผยแพร่เวิร์กบุ๊กไปยัง Power BI มีบางสิ่งที่ควรพิจารณา:</span><span class="sxs-lookup"><span data-stu-id="8dd4b-107">When publishing a workbook to Power BI, there are few things to consider:</span></span>

* <span data-ttu-id="8dd4b-108">บัญชีที่คุณใช้เพื่อลงชื่อเข้าใช้ Office, OneDrive for Business และ Power BI ต้องเป็นบัญชีเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="8dd4b-108">The account you use to sign in to Office, OneDrive for Business (if using workbooks saved there), and Power BI must be the same account.</span></span>
* <span data-ttu-id="8dd4b-109">คุณไม่สามารถเผยแพร่สมุดงานเปล่าหรือสมุดงานที่มีเนื้อหาที่ไม่สนับสนุนใน Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="8dd4b-109">You cannot publish an empty workbook, or a workbook that doesn’t have any Power BI supported content.</span></span>
* <span data-ttu-id="8dd4b-110">คุณไม่สามารถเผยแพร่สมุดงานที่มีการเข้ารหัสลับ หรือป้องกันด้วยรหัสผ่าน หรือสมุดงานที่มีการจัดการการปกป้องข้อมูล ( Information Protection Management) ได้</span><span class="sxs-lookup"><span data-stu-id="8dd4b-110">You cannot publish encrypted or password protected workbooks, or workbooks with Information Protection Management.</span></span>
* <span data-ttu-id="8dd4b-111">การเผยแพร่ไปยัง Power BI จำเป็นต้องเปิดใช้งานการรับรองความถูกต้องสมัยใหม่ (ค่าเริ่มต้น)</span><span class="sxs-lookup"><span data-stu-id="8dd4b-111">Publishing to Power BI requires modern authentication be enabled (default).</span></span> <span data-ttu-id="8dd4b-112">หากปิดใช้งานอยู่ ตัวเลือกเผยแพร่จะไม่พร้อมใช้งานจากเมนูไฟล์</span><span class="sxs-lookup"><span data-stu-id="8dd4b-112">If disabled, the Publish option is not available from the File menu.</span></span>

## <a name="publish-your-excel-workbook"></a><span data-ttu-id="8dd4b-113">เผยแพร่เวิร์กบุ๊ก Excel ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8dd4b-113">Publish your Excel workbook</span></span>
<span data-ttu-id="8dd4b-114">ในการเผยแพร่สมุดงาน Excel ของคุณ ใน Excel ให้เลือก **ไฟล์** > **เผย่แพร่** และเลือก **อัปโหลด** หรือ **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="8dd4b-114">To publish your Excel workbook, in Excel, select **File** > **Publish** and select either **Upload** or **Export**.</span></span>

<span data-ttu-id="8dd4b-115">ถ้าคุณ **อัปโหลด** สมุดงานของคุณไปยัง Power BI คุณสามารถโต้ตอบกับเวิร์กบุ๊กได้เช่นเดียวกับที่คุณจะโต้ตอบโดยใช้ Excel Online</span><span class="sxs-lookup"><span data-stu-id="8dd4b-115">If you **Upload** your workbook to Power BI, you can interact with the workbook just as you would interact using Excel Online.</span></span> <span data-ttu-id="8dd4b-116">คุณยังสามารถปักหมุดสิ่งที่เลือกจากสมุดงานของคุณไปยังแดชบอร์ด Power BI และแชร์สมุดงานของคุณ หรือองค์ประกอบที่เลือกผ่าน Power BI</span><span class="sxs-lookup"><span data-stu-id="8dd4b-116">You can also pin selections from your workbook onto Power BI dashboards, and share your workbook, or selected elements, through Power BI.</span></span>

<span data-ttu-id="8dd4b-117">หากคุณเลือก **ส่งออก** คุณสามารถส่งออกข้อมูลตารางและรูปแบบข้อมูลไปยังชุดข้อมูล Power BI ซึ่งคุณสามารถใช้เพื่อสร้างรายงาน Power Dash และแดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="8dd4b-117">If you select **Export**, you can export table data and its data model into a Power BI dataset, which you can then use to create Power BI reports and dashboards.</span></span>

### <a name="local-file-publishing"></a><span data-ttu-id="8dd4b-118">เผยแพร่ไฟล์ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="8dd4b-118">Local file publishing</span></span>
<span data-ttu-id="8dd4b-119">Excel รองรับการเผยแพร่ไฟล์ Excel ในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="8dd4b-119">Excel supports publishing of local Excel files.</span></span> <span data-ttu-id="8dd4b-120">ไฟล์เหล่านี้ไม่จำเป็นต้องถูกบันทึกไปยัง OneDrive for Business หรือ SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="8dd4b-120">They do not need to be saved to OneDrive for Business or SharePoint Online.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8dd4b-121">คุณสามารถเผยแพร่ไฟล์ภายในเครื่องได้เฉพาะในกรณีที่คุณใช้ Excel 2016 (หรือใหม่กว่า) ด้วยการสมัครใช้งาน Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8dd4b-121">You can only publish local files if you're using Excel 2016 (or later) with a Microsoft 365 subscription.</span></span> <span data-ttu-id="8dd4b-122">การติดตั้งแบบสแตนด์อโลนของ Excel 2016 สามารถเผยแพร่ไปยัง Power BI ได้เฉพาะเมื่อบันทึกสมุดงานไปยัง OneDrive for Business หรือ SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="8dd4b-122">Excel 2016 standalone installations can Publish to Power BI, but only when the workbook is saved to OneDrive for Business or SharePoint Online.</span></span>
> 

<span data-ttu-id="8dd4b-123">เมื่อคุณเลือก **เผยแพร่** คุณสามารถเลือกพื้นที่ทำงานที่คุณต้องการเผยแพร่ได้</span><span class="sxs-lookup"><span data-stu-id="8dd4b-123">When you select **Publish**, you can select the workspace to which you want to publish.</span></span> <span data-ttu-id="8dd4b-124">หากไฟล์ Excel ของคุณจัดเก็บอยู่ใน OneDrive for Business คุณสามารถเผยแพร่ไปยัง *พื้นที่ทำงานของฉัน* ได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8dd4b-124">If your Excel file resides on OneDrive for Business, you can only publish to your *My Workspace*.</span></span> <span data-ttu-id="8dd4b-125">หากไฟล์ Excel ของคุณจัดเก็บอยู่บนไดรฟ์ภายในเครื่อง คุณสามารถเผยแพร่ไปยัง *พื้นที่ทำงานของฉัน* หรือพื้นที่ทำงานที่ใช้ร่วมกันซึ่งคุณสามารถเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="8dd4b-125">If your Excel file resides on a local drive, you can publish to *My Workspace* or a shared workspace to which you have access.</span></span>

![สกรีนช็อตแสดงการเผยแพร่ไปยัง Power BI กับพื้นที่ทำงานของฉันที่เลือก](media/service-publish-from-excel/pbi_choose_workspace.png)

<span data-ttu-id="8dd4b-127">สองตัวเลือกในการรับสมุดงานของคุณเข้าสู่ Power BI</span><span class="sxs-lookup"><span data-stu-id="8dd4b-127">Two options on how to get your workbook into Power BI.</span></span>

![สกรีนช็อตแสดงการเผยแพร่กับพื้นที่ทำงานของฉันที่เลือก](media/service-publish-from-excel/pbi_uploadexport3.png)

<span data-ttu-id="8dd4b-129">เมื่อเผยแพร่แล้วเนื้อหาเวิร์กบุ๊กที่คุณเผยแพร่จะถูกนำเข้าไปยัง Power BI โดยแยกจากไฟล์ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="8dd4b-129">Once published, the workbook content you publish is imported into Power BI, separate from the local file.</span></span> <span data-ttu-id="8dd4b-130">หากคุณต้องการอัปเดตไฟล์ใน Power BI คุณต้องเผยแพร่เวอร์ชันที่อัปเดตอีกครั้งหรือคุณสามารถรีเฟรชข้อมูลโดยกำหนดค่าการรีเฟรชตามกำหนดเวลาในสมุดงานหรือบนชุดข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8dd4b-130">If you want to update the file in Power BI, you must publish the updated version again, or you can refresh the data by configuring a scheduled refresh, on the workbook, or on the dataset in Power BI.</span></span>

### <a name="publishing-from-a-standalone-excel-installation"></a><span data-ttu-id="8dd4b-131">การเผยแพร่จากการติดตั้ง Excel แบบสแตนด์อโลน</span><span class="sxs-lookup"><span data-stu-id="8dd4b-131">Publishing from a standalone Excel installation</span></span>
<span data-ttu-id="8dd4b-132">เมื่อเผยแพร่จากการติดตั้ง Excel แบบสแตนด์อโลน จะต้องบันทึกสมุดงานลงใน OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="8dd4b-132">When publishing from a standalone Excel installation, the workbook must be saved to OneDrive for Business.</span></span> <span data-ttu-id="8dd4b-133">เลือก **บันทึกไปยังคลาวด์** และเลือกตำแหน่งใน OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="8dd4b-133">Select **Save to Cloud** and choose a location in OneDrive for Business.</span></span>

![บันทึกไปยัง OneDrive for Business](media/service-publish-from-excel/pbi_savetoonedrive2.png)

<span data-ttu-id="8dd4b-135">เมื่อบันทึกสมุดงานของคุณไปยัง OneDrive for Business แล้ว เมื่อคุณเลือก **เผยแพร่** คุณมีสองตัวเลือกในการรับสมุดงานของคุณลงใน Power BI **อัปโหลด** หรือ **ส่งออก**:</span><span class="sxs-lookup"><span data-stu-id="8dd4b-135">Once your workbook is saved to OneDrive for Business, when you select **Publish**, you have two options to get your workbook into Power BI, **Upload** or **Export**:</span></span>

![ตัวเลือกสำหรับ Power BI](media/service-publish-from-excel/pbi_uploadexport2.png)

#### <a name="upload-your-workbook-to-power-bi"></a><span data-ttu-id="8dd4b-137">อัปโหลดสมุดงานของคุณไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="8dd4b-137">Upload your workbook to Power BI</span></span>
<span data-ttu-id="8dd4b-138">เมื่อคุณเลือกตัวเลือก **อัปโหลด** สมุดงานของคุณจะปรากฏใน Power BI ในลักษณะเดียวกับใน Excel Online</span><span class="sxs-lookup"><span data-stu-id="8dd4b-138">When you choose the **Upload** option, your workbook will appear in Power BI just like it would in Excel Online.</span></span> <span data-ttu-id="8dd4b-139">แต่จะต่างจาก Excel Online คือ คุณจะมีตัวเลือกบางอย่างที่ช่วยให้คุณสามารถปักหมุดองค์ประกอบจากแผ่นงานของคุณไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="8dd4b-139">But, unlike Excel Online, you’ll have some options that enable you to help you pin elements from your worksheets to dashboards.</span></span>

<span data-ttu-id="8dd4b-140">คุณไม่สามารถแก้ไขสมุดงานของคุณใน Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="8dd4b-140">You can’t edit your workbook in Power BI.</span></span> <span data-ttu-id="8dd4b-141">หากคุณต้องการเปลี่ยนแปลงข้อมูล คุณสามารถเลือก **แก้ไข** จากนั้นเลือกแก้ไขสมุดงานของคุณใน Excel Online หรือเปิดใน Excel บนคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8dd4b-141">If you need to make some changes to the data, you can select **Edit** then choose to edit your workbook in Excel Online or open it in Excel on your computer.</span></span> <span data-ttu-id="8dd4b-142">การเปลี่ยนแปลงใดๆ ที่คุณทำจะถูกบันทึกไว้ในสมุดงานบน OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="8dd4b-142">Any changes you make are saved to the workbook on OneDrive for Business.</span></span>

<span data-ttu-id="8dd4b-143">เมื่อคุณ **อัปโหลด** จะไม่มีการสร้างชุดข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8dd4b-143">When you **Upload**, no dataset is created in Power BI.</span></span> <span data-ttu-id="8dd4b-144">สมุดงานของคุณจะปรากฏในรายงาน ในบานหน้าต่างนำทางของพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="8dd4b-144">Your workbook will appear in Reports, in your workspace nav pane.</span></span> <span data-ttu-id="8dd4b-145">สมุดงานที่อัปโหลดไปยัง Power BI มี Excel ไอคอนพิเศษ ระบุสมุดงานเหล่านั้นเป็นสมุดงาน Excel ที่มีการอัปโหลด</span><span class="sxs-lookup"><span data-stu-id="8dd4b-145">Workbooks uploaded to Power BI have a special Excel icon, identifying them as Excel workbooks that have been uploaded.</span></span>

<span data-ttu-id="8dd4b-146">เลือกตัวเลือก **อัปโหลด** หากคุณมีข้อมูลในแผ่นงานเท่านั้น หรือคุณมี PivotTables และแผนภูมิที่คุณต้องการเห็นใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8dd4b-146">Choose the **Upload** option if you only have data in worksheets, or you have PivotTables and Charts you want to see in Power BI.</span></span>

<span data-ttu-id="8dd4b-147">การใช้การอัปโหลดจากการเผยแพร่สู่ Power BI ใน Excel เป็นประสบการณ์ที่คล้ายคลึงกับ **รับข้อมูล > ไฟล์ > OneDrive for Business > เชื่อมต่อ จัดการ และดู Excel ใน Power BI** จาก Power BI ในเบราว์เซอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8dd4b-147">Using Upload from Publish to Power BI in Excel is a similar experience to **Get Data > File > OneDrive for Business > Connect, Manage and View Excel in Power BI** from Power BI in your browser.</span></span>

#### <a name="export-workbook-data-to-power-bi"></a><span data-ttu-id="8dd4b-148">ส่งออกข้อมูลในสมุดงานไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="8dd4b-148">Export workbook data to Power BI</span></span>
<span data-ttu-id="8dd4b-149">เมื่อคุณเลือกตัวเลือก **ส่งออก** ข้อมูลใดๆ ที่รองรับในตาราง และ/หรือ รูปแบบข้อมูลจะถูกส่งออกไปยังชุดข้อมูลใหม่ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8dd4b-149">When you choose the **Export** option, any supported data in tables and/or a data model are exported into a new dataset in Power BI.</span></span> <span data-ttu-id="8dd4b-150">แผ่นงาน PowerView ใดๆ ในสมุดงานจะถูกสร้างขึ้นใหม่ใน Power BI เป็นรายงาน</span><span class="sxs-lookup"><span data-stu-id="8dd4b-150">Any Power View sheets in the workbook are re-created in Power BI as reports.</span></span>

<span data-ttu-id="8dd4b-151">คุณสามารถทำการแก้ไขสมุดงานของคุณต่อได้</span><span class="sxs-lookup"><span data-stu-id="8dd4b-151">You can continue editing your workbook.</span></span> <span data-ttu-id="8dd4b-152">เมื่อบันทึกการเปลี่ยนแปลงของคุณแล้ว การเปลี่ยนแปลงเหล่านั้นจะถูกซิงโครไนซ์กับชุดข้อมูลใน Power BI ซึ่งโดยปกติจะใช้เวลาประมาณหนึ่งชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="8dd4b-152">When your changes are saved, they are synchronized with the dataset in Power BI, usually within about an hour.</span></span> <span data-ttu-id="8dd4b-153">หากคุณต้องการการอัพเดตเพิ่มเติมทันที คุณสามารถเลือก **เผยแพร่** อีกครั้งจาก Excel และการเปลี่ยนแปลงของคุณจะถูกส่งออกทันที</span><span class="sxs-lookup"><span data-stu-id="8dd4b-153">If you need more immediate updates, you can select **Publish** again from Excel, and your changes are exported immediately.</span></span> <span data-ttu-id="8dd4b-154">การแสดงภาพข้อมูลในรายงานและแดชบอร์ดนั้นจะได้รับการอัปเดตด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="8dd4b-154">Any visualizations in reports and dashboards are updated, too.</span></span>

<span data-ttu-id="8dd4b-155">เลือกตัวเลือก **เผยแพร่** หากคุณใช้คุณลักษณะรับและ แปลงข้อมูลหรือคุณลักษณะของ Power Pivot เพื่อโหลดข้อมูลลงในรูปแบบข้อมูล หรือหากสมุดงานของคุณมีแผ่นงาน Power View ที่มีการแสดงภาพที่คุณต้องการเห็นใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8dd4b-155">Choose the **Publish** option if you’ve used the Get & Transform data or Power Pivot features to load data into a data model, or if your workbook has Power View sheets with visualizations that you want to see in Power BI.</span></span>

<span data-ttu-id="8dd4b-156">การใช้ การ **ส่งออก** จะคล้ายกันมากกับการใช้ **รับไฟล์ > ข้อมูล > OneDrive for Business > ส่งออกข้อมูล Excel ลงใน Power BI** จาก Power BI ในเบราว์เซอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8dd4b-156">Using **Export** is very similar to using **Get Data > File > OneDrive for Business > Export Excel data into Power BI** from Power BI in your browser.</span></span>

## <a name="publishing"></a><span data-ttu-id="8dd4b-157">กำลังเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="8dd4b-157">Publishing</span></span>
<span data-ttu-id="8dd4b-158">เมื่อคุณเลือกตัวเลือกใดตัวเลือกหนึ่ง Excel จะลงชื่อเข้าใช้ไปยัง Power BI ด้วยบัญชีปัจจุบันของคุณ จากนั้นจะเผยแพร่สมุดงานของคุณไปยังพื้นที่ทำงาน Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8dd4b-158">When you choose either option, Excel signs in to Power BI with your current account, then publishes your workbook to your Power BI workspace.</span></span> <span data-ttu-id="8dd4b-159">คุณสามารถตรวจสอบแถบสถานะใน Excel เพื่อดูว่ากระบวนการเผยแพร่กำลังดำเนินไปอย่างไร</span><span class="sxs-lookup"><span data-stu-id="8dd4b-159">You can monitor the status bar in Excel to see how the publish process is progressing.</span></span>

![แถบสถานะสำหรับการเผยแพร่ไปยัง Power BI](media/service-publish-from-excel/pbi_publishingstatus.png)

<span data-ttu-id="8dd4b-161">เมื่อเสร็จแล้ว คุณสามารถไปที่ Power BI ได้โดยตรงจาก Excel</span><span class="sxs-lookup"><span data-stu-id="8dd4b-161">When complete, you can go to Power BI directly from Excel.</span></span>

![ไปที่ Power BI](media/service-publish-from-excel/pbi_gotopbi.png)

## <a name="next-steps"></a><span data-ttu-id="8dd4b-163">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="8dd4b-163">Next steps</span></span>
[<span data-ttu-id="8dd4b-164">ข้อมูล Excel ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8dd4b-164">Excel data in Power BI</span></span>](service-excel-workbook-files.md)  
<span data-ttu-id="8dd4b-165">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8dd4b-165">More questions?</span></span> [<span data-ttu-id="8dd4b-166">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="8dd4b-166">Try the Power BI Community</span></span>](https://community.powerbi.com/)

