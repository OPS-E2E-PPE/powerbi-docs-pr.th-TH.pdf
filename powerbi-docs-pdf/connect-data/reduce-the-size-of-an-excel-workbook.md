---
title: ลดขนาดของเวิร์กบุ๊ก Excel เพื่อดูใน Power BI
description: ลดขนาดของเวิร์กบุ๊ก Excel เพื่อดูใน Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 01/10/2019
LocalizationGroup: Data from files
ms.openlocfilehash: 9996b8e3f571a04dc41d138947532f3ab402057a
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96404099"
---
# <a name="reduce-the-size-of-an-excel-workbook-to-view-it-in-power-bi"></a><span data-ttu-id="57693-103">ลดขนาดของเวิร์กบุ๊ก Excel เพื่อดูใน Power BI</span><span class="sxs-lookup"><span data-stu-id="57693-103">Reduce the size of an Excel workbook to view it in Power BI</span></span>
<span data-ttu-id="57693-104">คุณสามารถอัปโหลดเวิร์กบุ๊ก Excel ต่างๆ ที่มีขนาดเล็กกว่า 1 GB ไปยัง Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="57693-104">You can upload any Excel workbook smaller than 1 GB to Power BI.</span></span> <span data-ttu-id="57693-105">เวิร์กบุ๊ก Excel สามารถมีส่วนประกอบสองส่วน ได้แก่: รูปแบบข้อมูล และส่วนเหลือของรายงาน ซึ่งเป็นเนื้อหาหลักของเวิร์กชีต</span><span class="sxs-lookup"><span data-stu-id="57693-105">An Excel workbook can have two parts: a Data Model, and the rest of the report—the core worksheet contents.</span></span> <span data-ttu-id="57693-106">ถ้ารายงานมีขนาดที่ตรงตามขีดจำกัดด้านขนาดต่อไปนี้ คุณก็สามารถบันทึกไปยัง **OneDrive for Business** ให้เชื่อมต่อจาก Power BI แล้วดูใน Excel Online:</span><span class="sxs-lookup"><span data-stu-id="57693-106">If the report meets the following size limits, you can save it to **OneDrive for Business**, connect to it from Power BI, and view it in Excel Online:</span></span>

* <span data-ttu-id="57693-107">ทั้งเวิร์กบุ๊กสามารถมีขนาดได้สูงสุดถึง 1 GB</span><span class="sxs-lookup"><span data-stu-id="57693-107">The workbook as a whole can be up to 1 GB.</span></span>
* <span data-ttu-id="57693-108">เนื้อหาหลักของเวิร์กชีตสามารถมีขนาดได้สูงสุดถึง 30 MB</span><span class="sxs-lookup"><span data-stu-id="57693-108">The core worksheet contents can be up to 30 MB.</span></span>

## <a name="what-makes-core-worksheet-contents-larger-than-30-mb"></a><span data-ttu-id="57693-109">สิ่งที่ทำให้เนื้อหาหลักของเวิร์กชีตมีขนาดใหญ่กว่า 30 MB</span><span class="sxs-lookup"><span data-stu-id="57693-109">What makes core worksheet contents larger than 30 MB</span></span>
<span data-ttu-id="57693-110">นี่คือองค์ประกอบบางอย่างที่สามารถทำใหเนื้อหาหลักของเวิร์กชีตมีขนาดใหญ่กว่า 30 MB:</span><span class="sxs-lookup"><span data-stu-id="57693-110">Here are some elements that can make the core worksheet contents larger than 30 MB:</span></span>

* <span data-ttu-id="57693-111">รูปภาพ</span><span class="sxs-lookup"><span data-stu-id="57693-111">Images.</span></span>
* <span data-ttu-id="57693-112">เซลล์ที่แรเงา</span><span class="sxs-lookup"><span data-stu-id="57693-112">Shaded cells.</span></span> <span data-ttu-id="57693-113">[เอารูปแบบการแรเงาเซลล์ออก](https://support.office.com/article/Add-or-change-the-background-color-of-cells-ac10f131-b847-428f-b656-d65375fb815e)</span><span class="sxs-lookup"><span data-stu-id="57693-113">[Remove a cell shading format](https://support.office.com/article/Add-or-change-the-background-color-of-cells-ac10f131-b847-428f-b656-d65375fb815e).</span></span>
* <span data-ttu-id="57693-114">เวิร์กชีตที่มีการใช้สี</span><span class="sxs-lookup"><span data-stu-id="57693-114">Colored worksheets.</span></span> <span data-ttu-id="57693-115">[เอาพื้นหลังของแผ่นงานออก](https://support.office.com/article/add-or-remove-a-sheet-background-3577a762-8450-4556-96a2-cc265abc00a8)</span><span class="sxs-lookup"><span data-stu-id="57693-115">[Remove a sheet background](https://support.office.com/article/add-or-remove-a-sheet-background-3577a762-8450-4556-96a2-cc265abc00a8).</span></span>
* <span data-ttu-id="57693-116">กล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="57693-116">Text boxes.</span></span>
* <span data-ttu-id="57693-117">ภาพตัดปะ</span><span class="sxs-lookup"><span data-stu-id="57693-117">Clip art.</span></span>

<span data-ttu-id="57693-118">พิจารณาเอาองค์ประกอบเหล่านี้ออก ถ้าเป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="57693-118">Consider removing these elements, if possible.</span></span> 

<span data-ttu-id="57693-119">ถ้ารายงานมีรูปแบบข้อมูล คุณก็จะมีตัวเลือกอื่นๆ บางตัวเลือก ได้แก่:</span><span class="sxs-lookup"><span data-stu-id="57693-119">If the report has a Data Model, you have some other options:</span></span> 

* <span data-ttu-id="57693-120">เอาข้อมูลออกจากเวิร์กชีต Excel แล้วจัดเก็บไว้ในรูปแบบข้อมูลแทน</span><span class="sxs-lookup"><span data-stu-id="57693-120">Remove data from Excel worksheets, and store it in the Data Model instead.</span></span> <span data-ttu-id="57693-121">โปรดดู "เอาข้อมูลออกจากเวิร์กชีต" ที่ด้านล่าง สำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="57693-121">See “Remove data from worksheets” below for details.</span></span> 
* <span data-ttu-id="57693-122">[สร้างรูปแบบข้อมูลที่มีหน่วยความจำที่มีประสิทธิภาพ](https://support.office.com/article/Create-a-memory-efficient-Data-Model-using-Excel-2013-and-the-Power-Pivot-add-in-951c73a9-21c4-46ab-9f5e-14a2833b6a70) เพื่อลดขนาดโดยรวมของรายงาน</span><span class="sxs-lookup"><span data-stu-id="57693-122">[Create a memory-efficient Data Model](https://support.office.com/article/Create-a-memory-efficient-Data-Model-using-Excel-2013-and-the-Power-Pivot-add-in-951c73a9-21c4-46ab-9f5e-14a2833b6a70) to reduce the overall size of the report.</span></span>

<span data-ttu-id="57693-123">เมื่อต้องการให้เกิดการเปลี่ยนแปลงดังกล่าว คุณจะต้องแก้ไขเวิร์กบุ๊กใน Excel</span><span class="sxs-lookup"><span data-stu-id="57693-123">To make any of these changes, you need to edit the workbook in Excel.</span></span>

<span data-ttu-id="57693-124">อ่านข้อมูลเพิ่มเติมเกี่ยวกับ[ขีดจำกัดของขนาดไฟล์สำหรับเวิร์กบุ๊ก Excel ใน SharePoint Online](https://support.office.com/article/File-size-limits-for-workbooks-in-SharePoint-Online-9e5bc6f8-018f-415a-b890-5452687b325e)</span><span class="sxs-lookup"><span data-stu-id="57693-124">Read more about [file size limits for Excel workbooks in SharePoint Online](https://support.office.com/article/File-size-limits-for-workbooks-in-SharePoint-Online-9e5bc6f8-018f-415a-b890-5452687b325e).</span></span>

## <a name="remove-data-from-worksheets"></a><span data-ttu-id="57693-125">เอาข้อมูลออกจากเวิร์กชีต</span><span class="sxs-lookup"><span data-stu-id="57693-125">Remove data from worksheets</span></span>
<span data-ttu-id="57693-126">ถ้าคุณนำเข้าข้อมูลลงใน Excel จากแท็บ Power Query หรือแท็บข้อมูลของ Excel เวิร์กบุ๊กอาจมีข้อมูลเหมือนกับในตาราง Excel และในรูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="57693-126">If you import data into Excel from the Power Query tab or the Excel Data tab, the workbook might have the same data in an Excel table and in the Data Model.</span></span> <span data-ttu-id="57693-127">ตารางขนาดใหญ่ในเวิร์กชีต Excel อาจทำให้เนื้อหาหลักของเวิร์กชีตมีขนาดใหญ่เกินกว่า 30 MB</span><span class="sxs-lookup"><span data-stu-id="57693-127">Large tables in Excel worksheets may make the core worksheet contents more than 30 MB.</span></span> <span data-ttu-id="57693-128">การลบตารางใน Excel และการเก็บข้อมูลในรูปแบบข้อมูลสามารถลดเนื้อหาหลักของเวิร์กชีตในรายงานได้เป็นอย่างมาก</span><span class="sxs-lookup"><span data-stu-id="57693-128">Removing the table in Excel and keeping the data in the Data Model can greatly reduce the core worksheet contents of the report.</span></span> 

<span data-ttu-id="57693-129">เมื่อคุณนำเข้าข้อมูลลงใน Excel ให้ทำตามคำแนะนำเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="57693-129">When you import data into Excel, follow these tips:</span></span>

* <span data-ttu-id="57693-130">**ใน Power Query**: ล้างข้อมูลในกล่อง **การโหลดไปยังเวิร์กชีต**</span><span class="sxs-lookup"><span data-stu-id="57693-130">**In Power Query**: Clear the **Load to worksheet** box.</span></span>
  
  <span data-ttu-id="57693-131">ข้อมูลได้รับการนำเข้าเฉพาะในรูปแบบข้อมูลที่ไม่มีข้อมูลในเวิร์กชีต Excel เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="57693-131">The data is imported only into the Data Model, with no data in Excel worksheets.</span></span>
* <span data-ttu-id="57693-132">**จากแท็บข้อมูล Excel** ถ้าคุณได้เลือก **ตาราง** ไว้ก่อนหน้านี้ในตัวช่วยสร้างนำเข้า: ไปยัง **การเชื่อมต่อที่ยังคงอยู่** \>คลิกการเชื่อมต่อ\> **สร้างเฉพาะการเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="57693-132">**From the Excel Data tab**, if you previously checked **Table** in the import wizard: Go to **Existing Connections** \> click the connection \> **Only create connection**.</span></span> <span data-ttu-id="57693-133">ลบตารางต้นฉบับหรือตารางที่สร้างขึ้นในระหว่างการนำเข้าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="57693-133">Delete the original table or tables created during the initial import.</span></span>
* <span data-ttu-id="57693-134">**ในส่วนแท็บข้อมูล Excel**: ไม่ต้องทำเครื่องหมายเลือก **ตาราง** ในกล่อง **การนำเข้าข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="57693-134">**From the Excel Data tab**: don’t check **Table** in the **Import Data** box.</span></span>

## <a name="workbook-size-optimizer"></a><span data-ttu-id="57693-135">ตัวปรับเพิ่มขนาดเวิร์กบุ๊ก</span><span class="sxs-lookup"><span data-stu-id="57693-135">Workbook Size Optimizer</span></span>
<span data-ttu-id="57693-136">ถ้าเวิร์กบุ๊กของคุณประกอบด้วยรูปแบบข้อมูล คุณก็สามารถเรียกใช้ตัวปรับเพิ่มขนาดเวิร์กบุ๊กเพื่อลดขนาดเวิร์กบุ๊กของคุณได้</span><span class="sxs-lookup"><span data-stu-id="57693-136">If your workbook contains a data model, you can run the workbook size optimizer to reduce the size of your workbook.</span></span> <span data-ttu-id="57693-137">[ดาวน์โหลดตัวปรับเพิ่มขนาดเวิร์กบุ๊ก](https://www.microsoft.com/download/details.aspx?id=38793)</span><span class="sxs-lookup"><span data-stu-id="57693-137">[Download Workbook Size Optimizer](https://www.microsoft.com/download/details.aspx?id=38793).</span></span>

## <a name="related-info"></a><span data-ttu-id="57693-138">ข้อมูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="57693-138">Related info</span></span>
[<span data-ttu-id="57693-139">สร้างรูปแบบข้อมูลที่มีหน่วยความจำที่มีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="57693-139">Create a memory-efficient Data Model</span></span>](https://support.office.com/article/Create-a-memory-efficient-Data-Model-using-Excel-2013-and-the-Power-Pivot-add-in-951c73a9-21c4-46ab-9f5e-14a2833b6a70)

[<span data-ttu-id="57693-140">ใช้ลิงก์ OneDrive for Business ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="57693-140">Use OneDrive for Business links in Power BI Desktop</span></span>](desktop-use-onedrive-business-links.md)

