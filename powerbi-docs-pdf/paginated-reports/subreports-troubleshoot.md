---
title: แก้ไขปัญหารายงานย่อยในรายงานที่มีการแบ่งหน้าของ Power BI
description: เรียนรู้เกี่ยวกับวิธีแก้ไขปัญหาทั่วไปเมื่อใช้รายงานย่อย ซึ่งเป็นรายการรายงานภายในรายงานที่มีการแบ่งหน้า
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: report-builder
ms.topic: troubleshooting
ms.date: 04/29/2020
ms.openlocfilehash: 06d9b0fc60d9b44f98108cf46bc35c5de15316d6
ms.sourcegitcommit: ccf53e87ff7cba1fcd9d2cca761a561e62933f90
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/04/2020
ms.locfileid: "93297991"
---
# <a name="troubleshoot-subreports-in-power-bi-paginated-reports"></a><span data-ttu-id="4d03a-103">แก้ไขปัญหารายงานย่อยในรายงานที่มีการแบ่งหน้าของ Power BI</span><span class="sxs-lookup"><span data-stu-id="4d03a-103">Troubleshoot subreports in Power BI paginated reports</span></span>

<span data-ttu-id="4d03a-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span><span class="sxs-lookup"><span data-stu-id="4d03a-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span></span> 

<span data-ttu-id="4d03a-105">ในบางครั้ง เมื่อคุณใช้รายงานย่อยในรายงานที่มีการแบ่งหน้า คุณอาจได้รับผลลัพธ์ที่ไม่คาดคิดหรือคุณลักษณะการทำงานไม่ทำงานตามที่คุณคาดไว้</span><span class="sxs-lookup"><span data-stu-id="4d03a-105">Sometimes when using subreports in paginated reports, you may get an unexpected result, or the feature doesn't work as you expected.</span></span> <span data-ttu-id="4d03a-106">บทความนี้เสนอโซลูชันสำหรับปัญหาทั่วไปเมื่อใช้รายงานย่อย</span><span class="sxs-lookup"><span data-stu-id="4d03a-106">This article provides solutions for common issues when using subreports.</span></span> <span data-ttu-id="4d03a-107">*รายงานย่อย* เป็นรายการรายงานที่แสดงรายงานอื่นภายในเนื้อความของรายงานหลักที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="4d03a-107">A *subreport* is a report item that displays another report inside the body of a main paginated report.</span></span> <span data-ttu-id="4d03a-108">ดู[รายงานย่อยในรายงานที่มีการแบ่งหน้าของ Power BI](subreports.md) สำหรับพื้นหลังเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4d03a-108">See [Subreports in Power BI paginated reports](subreports.md) for more background.</span></span>

## <a name="subreport-couldnt-be-found"></a><span data-ttu-id="4d03a-109">ไม่พบรายงานย่อย</span><span class="sxs-lookup"><span data-stu-id="4d03a-109">Subreport couldn't be found</span></span>

<span data-ttu-id="4d03a-110">**คำอธิบาย:** รายงานย่อยไม่แสดง</span><span class="sxs-lookup"><span data-stu-id="4d03a-110">**Description:** Subreport doesn't render.</span></span> <span data-ttu-id="4d03a-111">แต่ข้อความแสดงข้อผิดพลาดจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="4d03a-111">Instead an error message appears.</span></span>

### <a name="message"></a><span data-ttu-id="4d03a-112">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="4d03a-112">Message</span></span>

<span data-ttu-id="4d03a-113">"ไม่พบรายงานย่อย 'Subreport1' ที่ตำแหน่งเฉพาะ 'CustomerDetails'</span><span class="sxs-lookup"><span data-stu-id="4d03a-113">"The subreport 'Subreport1' could not be found at the specified location 'CustomerDetails'.</span></span> <span data-ttu-id="4d03a-114">ตรวจสอบว่ารายงานย่อยได้รับการเผยแพร่แล้วและชื่อถูกต้อง"</span><span class="sxs-lookup"><span data-stu-id="4d03a-114">Verify that the subreport has been published and that the name is correct."</span></span>

### <a name="possible-reasons"></a><span data-ttu-id="4d03a-115">เหตุผลที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="4d03a-115">Possible reasons</span></span>

- <span data-ttu-id="4d03a-116">ไม่มีรายงานย่อยซึ่งมีชื่อระบุอยู่ในพื้นที่ทำงานหรือแอปเดียวกันกับรายงานหลัก</span><span class="sxs-lookup"><span data-stu-id="4d03a-116">A subreport with the specified name doesn't exist in the same workspace or app as the main report.</span></span>
- <span data-ttu-id="4d03a-117">ผู้ใช้ไม่มีสิทธิ์ในการเข้าถึงรายงานย่อย</span><span class="sxs-lookup"><span data-stu-id="4d03a-117">The user doesn't have access to the subreport.</span></span>
- <span data-ttu-id="4d03a-118">จำนวนของรายงานย่อยในรายงานหลักถึงขีดจำกัดของรายงานย่อยแล้ว (รายงานย่อย 50 รายการ)</span><span class="sxs-lookup"><span data-stu-id="4d03a-118">The number of subreports in the main report has reached the subreport limit (50 subreports).</span></span>

### <a name="troubleshooting-steps"></a><span data-ttu-id="4d03a-119">ขั้นตอนการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="4d03a-119">Troubleshooting steps</span></span>

<span data-ttu-id="4d03a-120">**ในพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="4d03a-120">**In a workspace**</span></span>

- <span data-ttu-id="4d03a-121">ตรวจสอบว่ามีรายงานที่มีชื่อในข้อความแสดงข้อผิดพลาดอยู่</span><span class="sxs-lookup"><span data-stu-id="4d03a-121">Verify that the report with the name in the error message exists.</span></span> <span data-ttu-id="4d03a-122">ชื่อต้องตรงตามตัวอักษรพิมพ์ใหญ่-เล็ก</span><span class="sxs-lookup"><span data-stu-id="4d03a-122">The name is case insensitive.</span></span>

<span data-ttu-id="4d03a-123">**ในแอป**</span><span class="sxs-lookup"><span data-stu-id="4d03a-123">**In an app**</span></span>

- <span data-ttu-id="4d03a-124">ตรวจสอบว่ามีรายงานที่มีชื่อในข้อความแสดงข้อผิดพลาดอยู่ในแอป</span><span class="sxs-lookup"><span data-stu-id="4d03a-124">Verify that the report with the name in the error message exits in the app.</span></span> <span data-ttu-id="4d03a-125">ติดต่อผู้เขียนของแอปเพื่อขอความช่วยเหลือเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4d03a-125">Contact the author of the app for further assistance.</span></span>

<span data-ttu-id="4d03a-126">**หากมีการแชร์รายงาน**</span><span class="sxs-lookup"><span data-stu-id="4d03a-126">**If the report is shared**</span></span>

1. <span data-ttu-id="4d03a-127">ตรวจสอบว่ามีการแชร์รายงานที่มีชื่อในข้อความแสดงข้อผิดพลาดกับคุณ</span><span class="sxs-lookup"><span data-stu-id="4d03a-127">Verify that the report with the name in the error message is shared with you.</span></span>
2. <span data-ttu-id="4d03a-128">หากมีรายงานอยู่ ให้ตรวจสอบว่าชื่อเจ้าของสำหรับรายงานหลักและรายงานย่อยนั้นเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="4d03a-128">If the report exists, verify that the owner name is the same for the main report and the subreport.</span></span> <span data-ttu-id="4d03a-129">จากนั้นจึงติดต่อเจ้าของรายงานหลักที่มีข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="4d03a-129">Then contact the owner of the main report with that information.</span></span>

## <a name="subreport-renders-with-unexpected-content"></a><span data-ttu-id="4d03a-130">รายงานย่อยแสดงเนื้อหาที่ไม่คาดคิด</span><span class="sxs-lookup"><span data-stu-id="4d03a-130">Subreport renders with unexpected content</span></span>

### <a name="possible-reason"></a><span data-ttu-id="4d03a-131">เหตุผลที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="4d03a-131">Possible reason</span></span>

<span data-ttu-id="4d03a-132">Power BI อนุญาตให้ผู้ใช้มีรายงานหลายรายการซึ่งมีชื่อเดียวกันในพื้นที่ทำงานเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="4d03a-132">Power BI allows users to have multiple reports with the same name in the same workspace</span></span>

### <a name="troubleshooting-steps-for-report-authors"></a><span data-ttu-id="4d03a-133">ขั้นตอนการแก้ไขปัญหา (สำหรับผู้เขียนรายงาน)</span><span class="sxs-lookup"><span data-stu-id="4d03a-133">Troubleshooting steps (for report authors)</span></span>

1. <span data-ttu-id="4d03a-134">เปิดรายงานหลักใน Power BI Report Builder และกำหนดชื่อของรายงานย่อย</span><span class="sxs-lookup"><span data-stu-id="4d03a-134">Open the main report in Power BI Report Builder and determine the name of the subreport.</span></span>
2. <span data-ttu-id="4d03a-135">ค้นหารายงานที่มีชื่อเดียวกันในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="4d03a-135">Look for reports with the same name in the workspace.</span></span>
3. <span data-ttu-id="4d03a-136">กำหนดตำแหน่งรายงานที่คาดไว้และเปลี่ยนชื่อส่วนที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="4d03a-136">Locate the expected report and rename the rest.</span></span>

<span data-ttu-id="4d03a-137">**สำหรับบุคคลที่ไม่ใช่ผู้เขียน:** ติดต่อผู้เขียน</span><span class="sxs-lookup"><span data-stu-id="4d03a-137">**For non-authors:** Contact the author.</span></span>

## <a name="data-retrieval-fails"></a><span data-ttu-id="4d03a-138">การเรียกข้อมูลล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="4d03a-138">Data retrieval fails</span></span>

<span data-ttu-id="4d03a-139">**คำอธิบาย:** การเรียกข้อมูลล้มเหลวขณะแสดงรายงานย่อย</span><span class="sxs-lookup"><span data-stu-id="4d03a-139">**Description:** Data retrieval fails while rendering the subreport.</span></span> <span data-ttu-id="4d03a-140">รายงานย่อยไม่แสดง</span><span class="sxs-lookup"><span data-stu-id="4d03a-140">Subreport doesn't render.</span></span> <span data-ttu-id="4d03a-141">แต่ข้อความแสดงข้อผิดพลาดจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="4d03a-141">Instead an error message appears.</span></span>

### <a name="message"></a><span data-ttu-id="4d03a-142">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="4d03a-142">Message</span></span>

<span data-ttu-id="4d03a-143">"การเรียกข้อมูลล้มเหลวสำหรับรายงานย่อย 'Subreport1' อยู่ที่: 'InvoiceDetails'.</span><span class="sxs-lookup"><span data-stu-id="4d03a-143">"Data retrieval failed for the subreport, 'Subreport1', located at: 'InvoiceDetails'.</span></span> <span data-ttu-id="4d03a-144">ตรวจสอบแฟ้มบันทึกสำหรับข้อมูลเพิ่มเติม"</span><span class="sxs-lookup"><span data-stu-id="4d03a-144">Check the log files for more information."</span></span>

### <a name="troubleshooting-steps"></a><span data-ttu-id="4d03a-145">ขั้นตอนการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="4d03a-145">Troubleshooting steps</span></span>

<span data-ttu-id="4d03a-146">เช่นเดียวกับขั้นตอนการแก้ไขปัญหาทั่วไปสำหรับรายงานที่มีปัญหาในการเข้าถึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4d03a-146">Same as the general troubleshooting steps for reports with data access issues.</span></span>

## <a name="rendering-fails-unspecified-parameters"></a><span data-ttu-id="4d03a-147">การแสดงล้มเหลว: ไม่ได้ระบุพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="4d03a-147">Rendering fails: Unspecified parameters</span></span>

<span data-ttu-id="4d03a-148">**คำอธิบาย:** การแสดงรายงานย่อยล้มเหลวเนื่องจากไม่ได้ระบุพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="4d03a-148">**Description:** Subreport rendering fails because of unspecified parameters.</span></span> <span data-ttu-id="4d03a-149">รายงานย่อยมีพารามิเตอร์บังคับ แต่รายงานหลักไม่ได้กำหนดพารามิเตอร์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4d03a-149">The subreport has mandatory parameters but the main report doesn't set all of them.</span></span>

### <a name="message"></a><span data-ttu-id="4d03a-150">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="4d03a-150">Message</span></span> 
<span data-ttu-id="4d03a-151">“ไม่ได้ระบุพารามิเตอร์อย่างน้อยหนึ่งรายการสำหรับรายงานย่อย 'Subreport1' ซึ่งอยู่ที่: 'SubreportAWithDS'"</span><span class="sxs-lookup"><span data-stu-id="4d03a-151">"One or more parameters were not specified for the subreport, 'Subreport1', located at: 'SubreportAWithDS'."</span></span>

### <a name="troubleshooting-steps-for-the-report-author"></a><span data-ttu-id="4d03a-152">ขั้นตอนการแก้ไขปัญหา (สำหรับผู้เขียนรายงาน)</span><span class="sxs-lookup"><span data-stu-id="4d03a-152">Troubleshooting steps (for the report author)</span></span>

1. <span data-ttu-id="4d03a-153">เปิดรายงานหลักใน Power BI Report Builder</span><span class="sxs-lookup"><span data-stu-id="4d03a-153">Open the main report in Power BI Report Builder.</span></span>
2. <span data-ttu-id="4d03a-154">เปิดรายงานย่อยใน Power BI Report Builder</span><span class="sxs-lookup"><span data-stu-id="4d03a-154">Open the subreport in Power BI Report Builder.</span></span>
3. <span data-ttu-id="4d03a-155">ตรวจสอบว่าชุดของพารามิเตอร์ที่ส่งผ่านภายในรายการรายงานของรายงานย่อยในรายงานหลักนั้นตรงกับชุดพารามิเตอร์ในรายงานย่อย</span><span class="sxs-lookup"><span data-stu-id="4d03a-155">Verify that the set of parameters passed inside the subreport report item in the main report matches the set of parameters in the subreport.</span></span>

<span data-ttu-id="4d03a-156">**สำหรับบุคคลที่ไม่ใช่ผู้เขียน:** ติดต่อผู้เขียน</span><span class="sxs-lookup"><span data-stu-id="4d03a-156">**For non-authors:** Contact the author.</span></span>

## <a name="rendering-fails-recursion-limit"></a><span data-ttu-id="4d03a-157">การแสดงล้มเหลว: ขีดจำกัดการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="4d03a-157">Rendering fails: Recursion limit</span></span>

<span data-ttu-id="4d03a-158">**คำอธิบาย:** การแสดงรายงานย่อยล้มเหลวเนื่องจากขีดจำกัดการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="4d03a-158">**Description:** Subreport rendering fails because of the recursion limit.</span></span> <span data-ttu-id="4d03a-159">รายงานย่อยไม่สามารถซ้อนกันได้ลึกกว่า 20 ระดับ</span><span class="sxs-lookup"><span data-stu-id="4d03a-159">Subreports can't be nested deeper than 20 levels.</span></span>

### <a name="message"></a><span data-ttu-id="4d03a-160">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="4d03a-160">Message</span></span>

<span data-ttu-id="4d03a-161">“รายงานหรือรายงานย่อยมีรายงานย่อยที่เกิดซ้ำ 'Subreport1' ซึ่งเกินขีดจำกัดการเกิดซ้ำสูงสุดที่อนุญาต”</span><span class="sxs-lookup"><span data-stu-id="4d03a-161">"The report or subreport has a recursive subreport, 'Subreport1', that exceeded the maximum recursion limit allowed."</span></span>

### <a name="troubleshooting-steps-for-report-authors"></a><span data-ttu-id="4d03a-162">ขั้นตอนการแก้ไขปัญหา (สำหรับผู้เขียนรายงาน)</span><span class="sxs-lookup"><span data-stu-id="4d03a-162">Troubleshooting steps (for report authors)</span></span>

- <span data-ttu-id="4d03a-163">ลดการซ้อน</span><span class="sxs-lookup"><span data-stu-id="4d03a-163">Reduce nesting.</span></span>
- <span data-ttu-id="4d03a-164">ออกแบบโครงสร้างรายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="4d03a-164">Redesign the report structure.</span></span>

## <a name="other-errors"></a><span data-ttu-id="4d03a-165">ข้อผิดพลาดอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="4d03a-165">Other errors</span></span>

<span data-ttu-id="4d03a-166">**คำอธิบาย:** ข้อผิดพลาดที่ไมตรงกับประเภทใด ๆ ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="4d03a-166">**Description:** Errors that don't fall into any of the previous categories.</span></span>

### <a name="message"></a><span data-ttu-id="4d03a-167">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="4d03a-167">Message</span></span>

<span data-ttu-id="4d03a-168">"ข้อผิดพลาด: ไม่สามารถแสดงรายงานย่อยได้”</span><span class="sxs-lookup"><span data-stu-id="4d03a-168">"Error: Subreport could not be shown."</span></span>

### <a name="possible-reasons"></a><span data-ttu-id="4d03a-169">เหตุผลที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="4d03a-169">Possible reasons</span></span>

- <span data-ttu-id="4d03a-170">เกิดข้อผิดพลาดหลายอย่างระหว่างการแสดงรายงานย่อย เช่น พารามิเตอร์ไม่ตรงกับปัญหาการเรียกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4d03a-170">Multiple errors during subreport rendering, for example, parameter mismatch with data retrieval issues.</span></span>
- <span data-ttu-id="4d03a-171">ข้อผิดพลาดที่ไม่คาดคิด</span><span class="sxs-lookup"><span data-stu-id="4d03a-171">Unexpected errors.</span></span>

### <a name="troubleshooting-steps-for-report-authors"></a><span data-ttu-id="4d03a-172">ขั้นตอนการแก้ไขปัญหา (สำหรับผู้เขียนรายงาน)</span><span class="sxs-lookup"><span data-stu-id="4d03a-172">Troubleshooting steps (for report authors)</span></span>

1. <span data-ttu-id="4d03a-173">ตรวจสอบว่ารายงานย่อยสามารถแสดงได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="4d03a-173">Verify that the subreport can render directly.</span></span>
2. <span data-ttu-id="4d03a-174">หากรายงานย่อยสามารถแสดงได้ ให้ตรวจสอบพารามิเตอร์ทั้งในรายงานย่อยและข้อมูลหลัก</span><span class="sxs-lookup"><span data-stu-id="4d03a-174">If the subreport can render, check the parameters in both the subreport and main report.</span></span>
3. <span data-ttu-id="4d03a-175">ตรวจสอบให้แน่ใจว่ารายงานหลักไม่มีรายงานย่อยที่ไม่ซ้ำกันมากกว่า 50 รายการ และรายงานย่อยไม่มีการซ้อนกันลึกกว่า 20 ระดับ</span><span class="sxs-lookup"><span data-stu-id="4d03a-175">Make sure the main report doesn't have more than 50 unique subreports, and the subreport isn't nested deeper than 20 levels.</span></span>
4. <span data-ttu-id="4d03a-176">หากคุณไม่สามารถแก้ไขปัญหาได้ โปรดติดต่อฝ่ายสนับสนุนของ Power BI</span><span class="sxs-lookup"><span data-stu-id="4d03a-176">If you can't resolve the issue, contact Power BI support.</span></span>

<span data-ttu-id="4d03a-177">**สำหรับบุคคลที่ไม่ใช่ผู้เขียน:** ติดต่อผู้เขียน</span><span class="sxs-lookup"><span data-stu-id="4d03a-177">**For non-authors:** Contact the author.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4d03a-178">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4d03a-178">Next steps</span></span>

[<span data-ttu-id="4d03a-179">รายงานย่อยในรายงานที่มีการแบ่งหน้าของ Power BI</span><span class="sxs-lookup"><span data-stu-id="4d03a-179">Subreports in Power BI paginated reports</span></span>](subreports.md)

[<span data-ttu-id="4d03a-180">ดูรายงานแบบแบ่งหน้าในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="4d03a-180">View a paginated report in the Power BI service</span></span>](../consumer/paginated-reports-view-power-bi-service.md)

<span data-ttu-id="4d03a-181">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4d03a-181">More questions?</span></span> [<span data-ttu-id="4d03a-182">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="4d03a-182">Try the Power BI Community</span></span>](https://community.powerbi.com/)
