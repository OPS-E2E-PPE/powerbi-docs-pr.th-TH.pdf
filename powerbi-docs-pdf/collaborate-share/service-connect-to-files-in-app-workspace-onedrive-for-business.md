---
title: เชื่อมต่อกับไฟล์ใน OneDrive สำหรับพื้นที่ทำงาน Power BI
description: อ่านเกี่ยวกับการจัดเก็บ และการเชื่อมต่อกับไฟล์ Excel, CSV และ Power BI Desktop บน OneDrive สำหรับพื้นที่ทำงานของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: lukasz
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 10/15/2020
LocalizationGroup: Share your work
ms.openlocfilehash: 6c3c43d8aad26249ac1b8afab09bdcbf1414f0cf
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411988"
---
# <a name="connect-to-files-stored-in-onedrive-for-your-power-bi-workspace"></a><span data-ttu-id="61447-103">เชื่อมต่อไปยังไฟล์ที่จัดเก็บไว้ใน OneDrive สำหรับพื้นที่ทำงานของ Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="61447-103">Connect to files stored in OneDrive for your Power BI workspace</span></span>
<span data-ttu-id="61447-104">เมื่อคุณ [สร้างพื้นที่ทำงานใน Power BI](service-create-workspaces.md) คุณยังได้สร้าง Microsoft 365 Group ด้วยการเชื่อมโยงกับ OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="61447-104">When you [create a workspace in Power BI](service-create-workspaces.md), you're also creating a Microsoft 365 group, with an associated OneDrive for Business.</span></span> <span data-ttu-id="61447-105">บทความนี้อธิบายวิธีการจัดเก็บและอัปเดต Excel, CSV และไฟล์ Power BI Desktop ของคุณบน OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="61447-105">This article explains how to store and update your Excel, CSV, and Power BI Desktop files on that OneDrive for Business.</span></span> <span data-ttu-id="61447-106">การอัปเดตเหล่านั้นมีผลในรายงาน Power BI และแดชบอร์ดที่ยึดตามไฟล์เหล่านั้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="61447-106">Those updates are automatically reflected in the Power BI reports and dashboards based on the files.</span></span>

> [!NOTE]
> <span data-ttu-id="61447-107">ประสบการณ์พื้นที่ทำงานใหม่จะเปลี่ยนความสัมพันธ์ระหว่างพื้นที่ทำงาน Power BI และ Microsoft 365 Group</span><span class="sxs-lookup"><span data-stu-id="61447-107">The new workspace experience changes the relationship between Power BI workspaces and Microsoft 365 groups.</span></span> <span data-ttu-id="61447-108">คุณจะไม่สามารถสร้าง Microsoft 365 Group โดยอัตโนมัติทุกครั้งที่คุณสร้างพื้นที่ทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="61447-108">You don't automatically create a Microsoft 365 group every time you create one of the new workspaces.</span></span> <span data-ttu-id="61447-109">อ่านเกี่ยวกับ [สร้างพื้นที่ทำงานใหม่](service-create-the-new-workspaces.md)</span><span class="sxs-lookup"><span data-stu-id="61447-109">Read about [creating the new workspaces](service-create-the-new-workspaces.md)</span></span>

<span data-ttu-id="61447-110">การเพิ่มไฟล์ลงในพื้นที่ทำงานของคุณเป็นกระบวนการแบบสองขั้นตอน:</span><span class="sxs-lookup"><span data-stu-id="61447-110">Adding files to your workspace is a two-step process:</span></span> 

1. <span data-ttu-id="61447-111">ก่อนอื่น คุณ[อัปโหลดไฟล์ไปยัง OneDrive for Business](#1-upload-files-to-the-onedrive-for-business-for-your-workspace)สำหรับพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="61447-111">First you [upload files to the OneDrive for Business](#1-upload-files-to-the-onedrive-for-business-for-your-workspace) for your workspace.</span></span>
2. <span data-ttu-id="61447-112">แล้วคุณ[เชื่อมต่อกับไฟล์เหล่านั้นจาก Power BI](#2-import-excel-files-as-datasets-or-as-excel-online-workbooks)</span><span class="sxs-lookup"><span data-stu-id="61447-112">Then you [connect to those files from Power BI](#2-import-excel-files-as-datasets-or-as-excel-online-workbooks).</span></span>

> [!NOTE]
> <span data-ttu-id="61447-113">พื้นที่ทำงานใช้ได้กับสิทธิ์การใช้งาน [Power BI Pro](../fundamentals/service-features-license-type.md) เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="61447-113">Workspaces are only available with a [Power BI Pro](../fundamentals/service-features-license-type.md) license.</span></span>
> 

## <a name="1-upload-files-to-the-onedrive-for-business-for-your-workspace"></a><span data-ttu-id="61447-114">1 อัปโหลดไฟล์ไปยัง OneDrive for Business สำหรับพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="61447-114">1 Upload files to the OneDrive for Business for your workspace</span></span>
1. <span data-ttu-id="61447-115">ใน Power BI service เลือกลูกศรอยู่ถัดจากพื้นที่ทำงาน > เลือกจุดไข่ปลา ( **...** ) ถัดจากชื่อพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="61447-115">In the Power BI service, select the arrow next to Workspaces > select the ellipsis (**…**) next to your workspace name.</span></span> 
   
   ![ภาพหน้าจอของพื้นที่ทำงาน Power BI ที่แสดงชื่อพื้นที่ทำงานที่เลือก](media/service-connect-to-files-in-app-workspace-onedrive-for-business/power-bi-app-ellipsis.png)
2. <span data-ttu-id="61447-117">เลือก **ไฟล์** เพื่อเปิด OneDrive for Business สำหรับพื้นที่ทำงานบน Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="61447-117">Select **Files** to open the OneDrive for Business for your workspace on Microsoft 365.</span></span>
   
   > [!NOTE]
   > <span data-ttu-id="61447-118">ถ้าคุณไม่เห็น **ไฟล์** บนเมนูพื้นที่ทำงาน ให้เลือก **สมาชิก** เพื่อเปิด OneDrive for Business สำหรับพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="61447-118">If you don't see **Files** on the workspace menu, select **Members** to open the OneDrive for Business for your workspace.</span></span> <span data-ttu-id="61447-119">ที่นั่น เลือก **ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="61447-119">There, select **Files**.</span></span> <span data-ttu-id="61447-120">Microsoft 365 ตั้งค่าตำแหน่งที่เก็บข้อมูล OneDrive สำหรับไฟล์พื้นที่ทำงานของกลุ่มของแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="61447-120">Microsoft 365 sets up a OneDrive storage location for your app's group workspace files.</span></span> <span data-ttu-id="61447-121">กระบวนการนี้อาจใช้เวลาสักครู่</span><span class="sxs-lookup"><span data-stu-id="61447-121">This process may take some time.</span></span>
   > 
   > 
3. <span data-ttu-id="61447-122">ที่นี่ คุณสามารถอัปโหลดไฟล์ไปยัง OneDrive for Business สำหรับพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="61447-122">Here, you can upload your files to the OneDrive for Business for your workspace.</span></span> <span data-ttu-id="61447-123">เลือก **อัปโหลด** และนำทางไปยังไฟล์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="61447-123">Select **Upload**, and navigate to your files.</span></span>
   
   ![ภาพหน้าจอของ OneDrive for Business ที่แสดงวิธีการนำทางเพื่ออัปโหลดไฟล์](media/service-connect-to-files-in-app-workspace-onedrive-for-business/pbi_grpfilesonedrive.png)

## <a name="2-import-excel-files-as-datasets-or-as-excel-online-workbooks"></a><span data-ttu-id="61447-125">2 นำเข้าไฟล์ Excel ในฐานะชุดข้อมูลหรือในฐานะสมุดงาน Excel Online</span><span class="sxs-lookup"><span data-stu-id="61447-125">2 Import Excel files as datasets or as Excel Online workbooks</span></span>
<span data-ttu-id="61447-126">เมื่อไฟล์ของคุณอยู่ใน OneDrive for Business สำหรับพื้นที่ทำงาน คุณมีตัวเลือกดังนี้</span><span class="sxs-lookup"><span data-stu-id="61447-126">Now that your files are in the OneDrive for Business for your workspace, you have a choice.</span></span> <span data-ttu-id="61447-127">คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="61447-127">You can:</span></span> 

* <span data-ttu-id="61447-128">[นำเข้าข้อมูลจากเวิร์กบุ๊ก Excel เป็นชุดข้อมูล](../connect-data/service-get-data-from-files.md)</span><span class="sxs-lookup"><span data-stu-id="61447-128">[Import the data from the Excel workbook as a dataset](../connect-data/service-get-data-from-files.md).</span></span> <span data-ttu-id="61447-129">จากนั้นใช้ข้อมูลเพื่อสร้างรายงานและแดชบอร์ดที่คุณสามารถดูในเว็บเบราว์เซอร์ และบนอุปกรณ์มือถือ</span><span class="sxs-lookup"><span data-stu-id="61447-129">Then use the data to build reports and dashboards you can view in a web browser and on mobile devices.</span></span>
* <span data-ttu-id="61447-130">หรือ[เชื่อมต่อกับเวิร์กบุ๊ก Excel เต็มใน Power BI](../connect-data/service-excel-workbook-files.md)และแสดงไว้เหมือนกับที่จะปรากฏขึ้นใน Excel Online</span><span class="sxs-lookup"><span data-stu-id="61447-130">Or [connect to a whole Excel workbook in Power BI](../connect-data/service-excel-workbook-files.md) and display it exactly as it appears in Excel Online.</span></span>

### <a name="import-or-connect-to-the-files-in-your-workspace"></a><span data-ttu-id="61447-131">นำเข้า หรือเชื่อมต่อกับไฟล์ในพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="61447-131">Import or connect to the files in your workspace</span></span>
1. <span data-ttu-id="61447-132">ใน Power BI ให้สลับไปยังพื้นที่ทำงาน ดังนั้นชื่อพื้นที่ทำงานจะอยู่ที่มุมบนซ้าย</span><span class="sxs-lookup"><span data-stu-id="61447-132">In Power BI, switch to the workspace, so the workspace name is in the top-left corner.</span></span> 
2. <span data-ttu-id="61447-133">เลือก **รับข้อมูล** ที่ด้านล่างของบานหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="61447-133">Select **Get Data** at the bottom of the nav pane.</span></span> 
   
   ![ภาพหน้าจอของปุ่มรับข้อมูล ที่แสดงในบานหน้าต่างนำทาง](media/service-connect-to-files-in-app-workspace-onedrive-for-business/power-bi-app-get-data-button.png)
3. <span data-ttu-id="61447-135">ในกล่อง **ไฟล์** เลือก **รับ**</span><span class="sxs-lookup"><span data-stu-id="61447-135">In the **Files** box, select **Get**.</span></span>
   
   ![ภาพหน้าจอของกล่องโต้ตอบไฟล์ ที่แสดงปุ่มรับ](media/service-connect-to-files-in-app-workspace-onedrive-for-business/pbi_getfiles.png)
4. <span data-ttu-id="61447-137">เลือก **OneDrive** - *ชื่อพื้นที่ทำงานของคุณ*</span><span class="sxs-lookup"><span data-stu-id="61447-137">Select **OneDrive** - *Your Workspace Name*.</span></span>
   
    ![ภาพหน้าจอของไทล์สามตัวเพื่อเลือกพื้นที่ทำงานของคุณ ที่แสดงไฟล์ภายในเครื่อง OneDrive และ SharePoint](media/service-connect-to-files-in-app-workspace-onedrive-for-business/pbi_grp_one_drive_shrpt.png)
5. <span data-ttu-id="61447-139">เลือกไฟล์คุณต้อง > **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="61447-139">Select the file you want > **Connect**.</span></span>
   
    <span data-ttu-id="61447-140">ในจุดนี้คุณตัดสินใจว่า จะ[นำเข้าข้อมูลจากสมุดงาน Excel](../connect-data/service-get-data-from-files.md)หรือ[เชื่อมต่อไปยังเวิร์กบุ๊ก Excel ทั้งหมด](../connect-data/service-excel-workbook-files.md)</span><span class="sxs-lookup"><span data-stu-id="61447-140">At this point, you decide whether to [import the data from the Excel workbook](../connect-data/service-get-data-from-files.md), or [connect to the whole Excel workbooks](../connect-data/service-excel-workbook-files.md).</span></span>
6. <span data-ttu-id="61447-141">เลือก **นำเข้า** หรือ **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="61447-141">Select **Import** or **Connect**.</span></span>
   
    ![ภาพหน้าจอของกล่องโต้ตอบ OneDrive for Business ที่แสดงนำเข้าจาก Excel หรือเชื่อมต่อกับ Excel](media/service-connect-to-files-in-app-workspace-onedrive-for-business/pbi_importexceldataorwholecrop.png)
7. <span data-ttu-id="61447-143">ถ้าคุณเลือก **นำเข้า** แล้วเวิร์กบุ๊กปรากฏขึ้นบนแท็บ **ชุดข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="61447-143">If you select **Import**, then the workbook appears on the **Datasets** tab.</span></span> 
   
    ![ภาพหน้าจอของพื้นที่ทำงานใน Power BI ที่แสดงแท็บชุดข้อมูล](media/service-connect-to-files-in-app-workspace-onedrive-for-business/power-bi-app-excel-file-import.png)
   
    <span data-ttu-id="61447-145">ถ้าคุณเลือก **เชื่อมต่อ** แล้วเวิร์กบุ๊กอยู่บนแท็บ **สมุดงาน**</span><span class="sxs-lookup"><span data-stu-id="61447-145">If you select **Connect**, then the workbook is on the **Workbooks** tab.</span></span>
   
    ![ภาพหน้าจอของพื้นที่ทำงานใน Power BI ที่แสดงแท็บสมุดงาน](media/service-connect-to-files-in-app-workspace-onedrive-for-business/power-bi-app-excel-file-connect.png)

## <a name="next-steps"></a><span data-ttu-id="61447-147">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="61447-147">Next steps</span></span>
* [<span data-ttu-id="61447-148">สร้างแอปและพื้นที่ทำงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="61447-148">Create apps and workspaces in Power BI</span></span>](../collaborate-share/service-create-distribute-apps.md)
* [<span data-ttu-id="61447-149">นำเข้าข้อมูลจากเวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="61447-149">Import data from Excel workbooks</span></span>](../connect-data/service-get-data-from-files.md)
* <span data-ttu-id="61447-150">[Connect to whole Excel workbooks](../connect-data/service-excel-workbook-files.md</span><span class="sxs-lookup"><span data-stu-id="61447-150">[Connect to whole Excel workbooks](../connect-data/service-excel-workbook-files.md</span></span>
* <span data-ttu-id="61447-151">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="61447-151">More questions?</span></span> [<span data-ttu-id="61447-152">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="61447-152">Try the Power BI Community</span></span>](https://community.powerbi.com/)
* <span data-ttu-id="61447-153">มีคำติชมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="61447-153">Feedback?</span></span> <span data-ttu-id="61447-154">เยี่ยมชม[แนวคิด Power BI](https://ideas.powerbi.com/forums/265200-power-bi)</span><span class="sxs-lookup"><span data-stu-id="61447-154">Visit [Power BI Ideas](https://ideas.powerbi.com/forums/265200-power-bi)</span></span>
