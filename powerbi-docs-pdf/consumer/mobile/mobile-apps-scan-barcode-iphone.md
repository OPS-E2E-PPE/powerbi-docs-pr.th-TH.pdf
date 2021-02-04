---
title: สแกนบาร์โค้ดด้วยแอป Power BI สำหรับอุปกรณ์เคลื่อนที่
description: สแกนบาร์โค้ดในโลกแห่งความจริงเพื่อไปยังข้อมูล BI ที่ถูกกรองโดยตรงในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 12/02/2019
ms.openlocfilehash: 5d1534ec3b6ccdf730cd2b255ba1142e80a6f9f9
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413115"
---
# <a name="scan-a-barcode-with-your-device-from-the-power-bi-mobile-app"></a><span data-ttu-id="4748d-103">สแกนบาร์โค้ดด้วยอุปกรณ์ของคุณจากแอป Power BI สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="4748d-103">Scan a barcode with your device from the Power BI mobile app</span></span>
<span data-ttu-id="4748d-104">สแกนบาร์โค้ดในโลกแห่งความจริงเพื่อไปยังข้อมูล BI ที่ถูกกรองโดยตรงในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="4748d-104">Scan barcodes in the real world to go directly to filtered BI information in the Power BI mobile app.</span></span>


<span data-ttu-id="4748d-105">นำไปใช้กับ:</span><span class="sxs-lookup"><span data-stu-id="4748d-105">Applies to:</span></span>

| ![iPhone](./media/mobile-apps-qr-code/ios-logo-40-px.png) | ![iPad](./media/mobile-apps-qr-code/ios-logo-40-px.png) | ![โทรศัพท์ Android](././media/mobile-apps-qr-code/android-logo-40-px.png) | ![แท็บเล็ต Android](././media/mobile-apps-qr-code/android-logo-40-px.png) |
|:--- |:--- |:--- |:--- |
|<span data-ttu-id="4748d-110">iPhone</span><span class="sxs-lookup"><span data-stu-id="4748d-110">iPhones</span></span> |<span data-ttu-id="4748d-111">iPad</span><span class="sxs-lookup"><span data-stu-id="4748d-111">iPads</span></span> |<span data-ttu-id="4748d-112">โทรศัพท์ Android</span><span class="sxs-lookup"><span data-stu-id="4748d-112">Android phones</span></span> |<span data-ttu-id="4748d-113">แท็บเล็ต Android</span><span class="sxs-lookup"><span data-stu-id="4748d-113">Android tablets</span></span> |

<span data-ttu-id="4748d-114">บอกเพื่อนร่วมงานที่ถูก[แท็กเขตข้อมูลบาร์โค้ดในรายงาน Power BI Desktop](../../transform-model/desktop-mobile-barcodes.md)และแชร์รายงานกับคุณ</span><span class="sxs-lookup"><span data-stu-id="4748d-114">Say a colleague has [tagged a barcode field in a report Power BI Desktop](../../transform-model/desktop-mobile-barcodes.md) and shared the report with you.</span></span> 

![ภาพหน้าจอของการสแกนบาร์โค้ดผลิตภัณฑ์ ที่แสดงการใช้เครื่องสแกนบนบาร์โค้ดของเครื่องดื่มสี](media/mobile-apps-scan-barcode-iphone/power-bi-barcode-scanner.png)

<span data-ttu-id="4748d-116">เมื่อคุณสามารถสแกนบาร์โค้ดผลิตภัณฑด้วยตัวสแกนในแอป Power BI บนอุปกรณ์ของคุณ คุณจะเห็นรายงาน (หรือรายการของรายงาน) ด้วยบาร์โค้ดนั้น</span><span class="sxs-lookup"><span data-stu-id="4748d-116">When you scan a product barcode with the scanner in the Power BI app on your device, you see the report (or list of reports) with that barcode.</span></span> <span data-ttu-id="4748d-117">คุณสามารถเปิดรายงานนั้นซึ่งถูกกรองไปยังบาร์โค้ดนั้น</span><span class="sxs-lookup"><span data-stu-id="4748d-117">You can open that report filtered to that barcode.</span></span>

## <a name="scan-a-barcode-with-the-power-bi-scanner"></a><span data-ttu-id="4748d-118">สแกนบาร์โค้ดด้วยตัวสแกน Power BI</span><span class="sxs-lookup"><span data-stu-id="4748d-118">Scan a barcode with the Power BI scanner</span></span>
1. <span data-ttu-id="4748d-119">ที่แถบนำทาง แตะที่ **ตัวเลือกเพิ่มเติม** (...) และแตะที่ **สแกนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="4748d-119">On the navigation bar, tap **More options** (...) and then tap **Scanner**.</span></span>

    ![ภาพหน้าจอของตัวเลือกเพิ่มเติมในบานหน้าต่างการนำทาง ที่แสดงการเลือกเครื่องสแกน](media/mobile-apps-scan-barcode-iphone/power-bi-scanner.png)

2. <span data-ttu-id="4748d-121">ถ้ากล้องของคุณไม่ได้เปิดใช้งาน คุณจำเป็นต้องอนุมัติให้แอป Power BI ใช้กล้อง</span><span class="sxs-lookup"><span data-stu-id="4748d-121">If your camera is not enabled, you need to approve the Power BI app to use the camera.</span></span> <span data-ttu-id="4748d-122">นี่เป็นการอนุมัติครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="4748d-122">This is a one-time approval.</span></span> 
4. <span data-ttu-id="4748d-123">เล็งตัวสแกนไปที่บาร์โค้ดบนผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4748d-123">Point the scanner at a barcode on a product.</span></span> <span data-ttu-id="4748d-124">คุณจะเห็นรายชื่อรายงานที่เชื่อมโยงกับบาร์โค้ดนั้น</span><span class="sxs-lookup"><span data-stu-id="4748d-124">You will see a list of reports associated with that barcode.</span></span>
5. <span data-ttu-id="4748d-125">แตะที่ชื่อรายงานเพื่อเปิดบนอุปกรณ์ของคุณ ซึ่งจะถูกกรองโดยอัตโนมัติไปยังบาร์โค้ดนั้น</span><span class="sxs-lookup"><span data-stu-id="4748d-125">Tap the report name to open it on your device, automatically filtered according to that barcode.</span></span>

## <a name="filter-by-other-barcodes-while-in-a-report"></a><span data-ttu-id="4748d-126">กรองด้วยบาร์โค้ดอื่นๆ ในขณะอยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="4748d-126">Filter by other barcodes while in a report</span></span>
<span data-ttu-id="4748d-127">ในขณะที่กำลังดูรายงานที่ถูกกรองด้วยบาร์โค้ดบนอุปกรณ์ของคุณ คุณอาจต้องการกรองรายงานเดียวกันด้วยบาร์โค้ดที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="4748d-127">While looking at a report filtered by a barcode on your device, you may want to filter the same report by a different barcode.</span></span>

* <span data-ttu-id="4748d-128">หากไอคอนบาร์โค้ดมีตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="4748d-128">If the barcode icon has a filter</span></span> ![ไอคอนที่กรองแล้ว](media/mobile-apps-scan-barcode-iphone/power-bi-barcode-filtered-icon-black.png)<span data-ttu-id="4748d-130">ตัวกรองเปิดทำงานอยู่และรายงานถูกกรองด้วยบาร์โค้ดแล้ว</span><span class="sxs-lookup"><span data-stu-id="4748d-130">, the filter is active and report Is already filtered by a barcode.</span></span> 
* <span data-ttu-id="4748d-131">หากไอคอนไม่มีตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="4748d-131">If the icon doesn't contain a filter</span></span> ![ไอคอนที่ไม่ได้กรอง](media/mobile-apps-scan-barcode-iphone/power-bi-barcode-unfiltered-icon.png)<span data-ttu-id="4748d-133">ตัวกรองจะไม่เปิดทำงานและรายงานไม่ถูกกรองด้วยบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="4748d-133">, the filter isn't active and the report isn't filtered by a barcode.</span></span> 

<span data-ttu-id="4748d-134">ไม่ว่าวิธีใด ให้แตะไอคอนเพื่อเปิดเมนูขนาดเล็กที่มีตัวสแกนแบบลอยตัวอยู่</span><span class="sxs-lookup"><span data-stu-id="4748d-134">Either way, tap the icon to open a small menu with a floating scanner.</span></span>

* <span data-ttu-id="4748d-135">โฟกัสตัวสแกนบนรายการใหม่เพื่อเปลี่ยนตัวกรองของรายงานเป็นค่าบาร์โค้ดที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="4748d-135">Focus the scanner on the new item to change the filter of the report to a different barcode value.</span></span> 
* <span data-ttu-id="4748d-136">เลือก **ล้างตัวกรองบาร์โค้ด** เพื่อกลับไปยังรายงานที่ไม่ถูกกรอง</span><span class="sxs-lookup"><span data-stu-id="4748d-136">Select **Clear barcode filter** to go back to the unfiltered report.</span></span>
* <span data-ttu-id="4748d-137">เลือก **กรองด้วยบาร์โค้ดล่าสุด** เพื่อเปลี่ยนตัวกรองรายงานเป็นหนึ่งในบาร์โค้ดที่คุณได้สแกนไปภายในเซสชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4748d-137">Select **Filter by recent barcodes** to change the report filter to one of the barcodes you've scanned within the current session.</span></span>

## <a name="issues-with-scanning-a-barcode"></a><span data-ttu-id="4748d-138">ปัญหาเกี่ยวกับการสแกนบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="4748d-138">Issues with scanning a barcode</span></span>
<span data-ttu-id="4748d-139">ต่อไปนี้เป็นข้อความบางอย่างที่คุณอาจเห็นเมื่อคุณสแกนบาร์โค้ดบนผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4748d-139">Here are some messages you may see when you scan a barcode on a product.</span></span>

### <a name="couldnt-filter-report"></a><span data-ttu-id="4748d-140">“ไม่สามารถกรองรายงานได้...”</span><span class="sxs-lookup"><span data-stu-id="4748d-140">"Couldn't filter report..."</span></span>
<span data-ttu-id="4748d-141">รายงานที่คุณเลือกที่จะกรองจะยึดตามรูปแบบข้อมูลที่ไม่ได้รวมค่าบาร์โค้ดนี้</span><span class="sxs-lookup"><span data-stu-id="4748d-141">The report you choose to filter is based on a data model that does not include this barcode value.</span></span> <span data-ttu-id="4748d-142">ตัวอย่างเช่น ผลิตภัณฑ์ “น้ำแร่” ไม่ได้รวมอยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="4748d-142">For example, the product "mineral water" isn't included in the report.</span></span>  

### <a name="allsome-of-the-visuals-in-the-report-dont-contain-any-value"></a><span data-ttu-id="4748d-143">รายการของภาพทั้งหมด/บางรายการในรายงานไม่มีค่าใด ๆ อยู่</span><span class="sxs-lookup"><span data-stu-id="4748d-143">All/some of the visuals in the report don't contain any value</span></span>
<span data-ttu-id="4748d-144">ค่าบาร์โค้ดที่คุณสแกนมีอยู่ในแบบจำลองของคุณ แต่รายการของภาพทั้งหมด/บางรายการในรายงานไม่มีค่าใด ๆ อยู่ ดังนั้นการกรองจะแสดงสถานะเป็นว่าง</span><span class="sxs-lookup"><span data-stu-id="4748d-144">The barcode value you scanned exists in your model but all/Some of the visuals on your report don't contain this value and therefore filtering will return an empty state.</span></span> <span data-ttu-id="4748d-145">ลองค้นหาหน้ารายงานอื่นๆ หรือแก้ไขรายงานของคุณใน Power BI Desktop ให้ประกอบด้วยค่านี้</span><span class="sxs-lookup"><span data-stu-id="4748d-145">Try looking into other report pages or edit your reports in Power BI desktop to contain this value</span></span> 

### <a name="looks-like-you-dont-have-any-reports-that-can-be-filtered-by-barcodes"></a><span data-ttu-id="4748d-146">“ดูเหมือนว่าคุณไม่มีรายงานใด ๆ ที่สามารถใช้บาร์โค้ดกรองได้”</span><span class="sxs-lookup"><span data-stu-id="4748d-146">"Looks like you don't have any reports that can be filtered by barcodes."</span></span>
<span data-ttu-id="4748d-147">ซึ่งหมายความว่า คุณไม่มีรายงานใดๆ ที่เปิดใช้งานบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="4748d-147">This means you don't have any barcode-enabled reports.</span></span> <span data-ttu-id="4748d-148">ตัวสแกนบาร์โค้ดสามารถกรองรายงานที่มีคอลัมน์ที่ทำเครื่องหมายเป็น **บาร์โค้ด** ได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4748d-148">The barcode scanner can only filter reports that have a column marked as **Barcode**.</span></span>  

<span data-ttu-id="4748d-149">ตรวจสอบให้แน่ใจว่าคุณ หรือเจ้าของรายงานได้แท็กคอลัมน์เป็น **บาร์โค้ด** ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4748d-149">Make sure you or the report owner has tagged a column as **Barcode** in Power BI Desktop.</span></span> <span data-ttu-id="4748d-150">เรียนรู้เพิ่มเติมเกี่ยวกับ[การแท็กเขตข้อมูลบาร์โค้ดใน Power BI Desktop](../../transform-model/desktop-mobile-barcodes.md)</span><span class="sxs-lookup"><span data-stu-id="4748d-150">Learn more about [tagging a barcode field in Power BI Desktop](../../transform-model/desktop-mobile-barcodes.md)</span></span>

### <a name="couldnt-filter-report---looks-like-this-barcode-doesnt-exist-in-the-report-data"></a><span data-ttu-id="4748d-151">"ไม่สามารถกรองรายงานได้ ดูเหมือนว่าจะไม่มีบาร์โค้ดนี้อยู่ในข้อมูลรายงาน"</span><span class="sxs-lookup"><span data-stu-id="4748d-151">"Couldn't filter report - Looks like this barcode doesn't exist in the report data."</span></span>
<span data-ttu-id="4748d-152">รายงานที่คุณเลือกที่จะกรองจะยึดตามรูปแบบข้อมูลที่ไม่ได้รวมค่าบาร์โค้ดนี้</span><span class="sxs-lookup"><span data-stu-id="4748d-152">The report you chose to filter is based on a data model that doesn't include this barcode value.</span></span> <span data-ttu-id="4748d-153">ตัวอย่างเช่น ผลิตภัณฑ์ “น้ำแร่” ไม่ได้รวมอยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="4748d-153">For example, the product "mineral water" isn't included in the report.</span></span> <span data-ttu-id="4748d-154">คุณสามารถสแกนผลิตภัณฑ์ต่างๆ เลือกรายงานที่แตกต่างกัน (ถ้ามีรายงานพร้อมใช้งานมากกว่าหนึ่ง) หรือดูรายงานที่ยังไม่ได้กรองได้</span><span class="sxs-lookup"><span data-stu-id="4748d-154">You can scan a different product, choose a different report (if more than one report is available), or view the report unfiltered.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="4748d-155">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4748d-155">Next steps</span></span>
* [<span data-ttu-id="4748d-156">แท็กเขตข้อมูลบาร์โค้ดใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4748d-156">Tag a barcode field in Power BI Desktop</span></span>](../../transform-model/desktop-mobile-barcodes.md)
* [<span data-ttu-id="4748d-157">ไทล์แดชบอร์ดใน Power BI</span><span class="sxs-lookup"><span data-stu-id="4748d-157">Dashboard tiles in Power BI</span></span>](../end-user-tiles.md)
* [<span data-ttu-id="4748d-158">แดชบอร์ดใน Power BI</span><span class="sxs-lookup"><span data-stu-id="4748d-158">Dashboards in Power BI</span></span>](../end-user-dashboards.md)
