---
title: บันทึกการเปลี่ยนแปลงสำหรับ เซิร์ฟเวอร์รายงาน Power BI
description: บันทึกการเปลี่ยนแปลงนี้ สำหรับเซิร์ฟเวอร์รายงาน Power BI และแสดงรายการสิ่งใหม่ รวมไปถึงการแก้ไขข้อบกพร่อง ของการเผยแพร่แต่ละรุ่น
author: jtarquino
ms.author: jaimeta
ms.reviewer: maggies
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: conceptual
ms.date: 01/06/2021
ms.openlocfilehash: 51df40463a02c2c165ca6cde59ef2b16cda8860c
ms.sourcegitcommit: f791eef8e885f18c48997c9af63ab56211f1ceb8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/09/2021
ms.locfileid: "98053339"
---
# <a name="change-log-for-power-bi-report-server"></a><span data-ttu-id="5ad71-103">บันทึกการเปลี่ยนแปลงสำหรับ เซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ad71-103">Change log for Power BI Report Server</span></span>

<span data-ttu-id="5ad71-104">บันทึกการเปลี่ยนแปลงนี้ สำหรับเซิร์ฟเวอร์รายงาน Power BI และแสดงรายการสิ่งใหม่ รวมไปถึงการแก้ไขข้อบกพร่อง ของการเผยแพร่แต่ละรุ่น</span><span class="sxs-lookup"><span data-stu-id="5ad71-104">This change log is for Power BI Report Server and lists new items along with bug fixes for each released build.</span></span>

<span data-ttu-id="5ad71-105">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะใหม่ต่าง ๆ โปรดดูที่[มีอะไรใหม่ในเซิร์ฟเวอร์ Power BI Report](whats-new.md)</span><span class="sxs-lookup"><span data-stu-id="5ad71-105">See [What's new in Power BI Report Server](whats-new.md) for more information about new features.</span></span> 

## <a name="october-2020"></a><span data-ttu-id="5ad71-106">ตุลาคม 2020</span><span class="sxs-lookup"><span data-stu-id="5ad71-106">October 2020</span></span>
- <span data-ttu-id="5ad71-107">**เซิร์ฟเวอร์รายงาน Power BI**</span><span class="sxs-lookup"><span data-stu-id="5ad71-107">**Power BI Report Server**</span></span>
    - <span data-ttu-id="5ad71-108">*เวอร์ชัน: 1.9.7675.15620 (รุ่น 15.0.1104.300) เผยแพร่เมื่อ: 8 มกราคม 2021*</span><span class="sxs-lookup"><span data-stu-id="5ad71-108">*Version: 1.9.7675.15620 (Build 15.0.1104.300), Released: January 8, 2021*</span></span>
        - <span data-ttu-id="5ad71-109">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-109">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-110">แก้ไขปัญหาเกี่ยวกับการรีเฟรชรายงานที่มีแหล่งข้อมูลตั้งแต่สองแหล่งขึ้นไป ซึ่งแตกต่างกันเฉพาะการระบุโครงสร้างตัวอักษรเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5ad71-110">Fixed issue with refresh of reports with two or more datasources that differ only by the casing of the letters.</span></span>
            - <span data-ttu-id="5ad71-111">แก้ไขปัญหาเกี่ยวกับการรีเฟรชการรวมชุดรายงานบางประเภทที่มีการรวมซ้อนกันแล้ว</span><span class="sxs-lookup"><span data-stu-id="5ad71-111">Fixed issue with refresh of reports certain combinations of nested joins.</span></span>
    - <span data-ttu-id="5ad71-112">*เวอร์ชัน: 1.9.7627.11028 (รุ่น 15.0.1104.264) เผยแพร่เมื่อ: 18 พฤศจิกายน 2020*</span><span class="sxs-lookup"><span data-stu-id="5ad71-112">*Version: 1.9.7627.11028 (Build 15.0.1104.264), Released: November 18, 2020*</span></span>
        - <span data-ttu-id="5ad71-113">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-113">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-114">แก้ไขปัญหาที่ป้องกันไม่ให้ผู้ใช้เปลี่ยนแปลงเขตข้อมูลในการตั้งค่าไซต์ผ่านพอร์ทัล</span><span class="sxs-lookup"><span data-stu-id="5ad71-114">Fixed issue preventing users from changing fields in site settings via the portal.</span></span>
            - <span data-ttu-id="5ad71-115">แก้ไขปัญหาเกี่ยวกับการรีเฟรชรายงาน Power BI เมื่อใช้แหล่งข้อมูล 'EnterData'</span><span class="sxs-lookup"><span data-stu-id="5ad71-115">Fixed issue with refresh of Power BI Reports when using 'EnterData' data source.</span></span>
            - <span data-ttu-id="5ad71-116">แก้ไขปัญหาเกี่ยวกับการรีเฟรชแบบจำลองบางรุ่นโดยใช้เมตาดาต้าชุดข้อมูลที่ปรับปรุงประสิทธิภาพแล้ว</span><span class="sxs-lookup"><span data-stu-id="5ad71-116">Fixed issue with refresh of some models using enhanced dataset metadata.</span></span>
            - <span data-ttu-id="5ad71-117">แก้ไขปัญหาที่รายงาน Power BI บางรายงานไม่สามารถเผยแพร่ไปยังเซิร์ฟเวอร์รายงานได้</span><span class="sxs-lookup"><span data-stu-id="5ad71-117">Fixed issue where some Power BI reports could not be published to the Report Server.</span></span>
    - <span data-ttu-id="5ad71-118">*เวอร์ชัน: 1.9.7604.41261 (รุ่น 15.0.1104.239) เผยแพร่เมื่อ: 27 ตุลาคม 2020*</span><span class="sxs-lookup"><span data-stu-id="5ad71-118">*Version: 1.9.7604.41261 (Build 15.0.1104.239), Released: October 27, 2020*</span></span>
         - <span data-ttu-id="5ad71-119">คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="5ad71-119">Features</span></span>
            - <span data-ttu-id="5ad71-120">เปิดใช้งานการสนับสนุนสำหรับเมตาดาต้าชุดข้อมูลที่ปรับปรุงประสิทธิภาพแล้วใน Power BI Report Server</span><span class="sxs-lookup"><span data-stu-id="5ad71-120">Enabled support for enhanced dataset metadata in Power BI Report Server.</span></span>
            - <span data-ttu-id="5ad71-121">เปิดใช้ความสามารถในการอัปเดตการเชื่อมต่อสำหรับรายงาน Power BI สำหรับ DirectQuery และการรีเฟรช (โปรดดู[เปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูล](./connect-data-source-apis.md)สำหรับรายละเอียดเพิ่มเติม)</span><span class="sxs-lookup"><span data-stu-id="5ad71-121">Enabled the ability to update connections for Power BI reports for DirectQuery and refresh (see [Change data source connection strings](./connect-data-source-apis.md) for more details).</span></span>
        - <span data-ttu-id="5ad71-122">ปรับปรุงความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="5ad71-122">Security updates</span></span>
        - <span data-ttu-id="5ad71-123">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-123">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-124">แก้ไขปัญหาที่ป้องกันไม่ให้ผู้ใช้เปลี่ยนกำหนดการรีเฟรชรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ad71-124">Fixed issue preventing users from changing Power BI report refresh schedules.</span></span>
            - <span data-ttu-id="5ad71-125">แก้ไขข้อความแสดงข้อผิดพลาดที่ทำให้ผู้ใช้ที่ได้รับการจัดการรายงานเมื่อข้อมูลประจำตัวหมดอายุเกิดความสับสน</span><span class="sxs-lookup"><span data-stu-id="5ad71-125">Fixed confusing error message users got managing reports when credentials had expired.</span></span>
            - <span data-ttu-id="5ad71-126">แก้ไขปัญหาเกี่ยวกับการส่งออกรายงานที่มีระยะเวลาในชื่อของรายงานดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="5ad71-126">Fixed issue with exporting reports with periods in their name.</span></span>
            - <span data-ttu-id="5ad71-127">แก้ไขปัญหาโปรแกรมอ่านหน้าจอใน tablix</span><span class="sxs-lookup"><span data-stu-id="5ad71-127">Fixed screen reader issues in a tablix.</span></span>
            - <span data-ttu-id="5ad71-128">แก้ไขปัญหาไฟล์บันทึกว่างเปล่าในบางสถานการณ์</span><span class="sxs-lookup"><span data-stu-id="5ad71-128">Fixed issue with log files being blank in some circumstances.</span></span>
            - <span data-ttu-id="5ad71-129">แก้ไขปัญหาด้วยการเขียนทับไฟล์ Excel ในระหว่างการอัปโหลด</span><span class="sxs-lookup"><span data-stu-id="5ad71-129">Fixed issue with overwriting Excel file during upload.</span></span>
            - <span data-ttu-id="5ad71-130">แก้ไขปัญหาด้วยวิธีการแบบจำลอง UpdateCacheSnapshot REST API</span><span class="sxs-lookup"><span data-stu-id="5ad71-130">Fixed issue with Model.UpdateCacheSnapshot REST API method.</span></span>
            - <span data-ttu-id="5ad71-131">แก้ไขปัญหาด้วยการเชื่อมต่อกับแหล่งข้อมูล AP BW ผ่าน XMLA</span><span class="sxs-lookup"><span data-stu-id="5ad71-131">Fixed issue with SAP BW data source connections via XMLA.</span></span>
            - <span data-ttu-id="5ad71-132">แก้ไขปัญหาที่กล่องโต้ตอบ "เชื่อมต่อกับ Power BI" ไม่ปิด</span><span class="sxs-lookup"><span data-stu-id="5ad71-132">Fixed issue with "Connect to Power BI" dialog not closing.</span></span>
            - <span data-ttu-id="5ad71-133">แก้ไขปัญหาด้วยค่าเริ่มต้นของฟีเจอร์ขั้นสูง CustomHeaders</span><span class="sxs-lookup"><span data-stu-id="5ad71-133">Fixed issue with CustomHeaders advanced feature default value.</span></span>
            - <span data-ttu-id="5ad71-134">อัปเดตตัวแสดงผล MHTML เพื่อใช้ HTML DOCTYPE ที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="5ad71-134">Updated MHTML renderer to use newer HTML DOCTYPE.</span></span>

- <span data-ttu-id="5ad71-135">**Power BI Desktop (ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI)**</span><span class="sxs-lookup"><span data-stu-id="5ad71-135">**Power BI Desktop (optimized for Power BI Report Server)**</span></span>
   - <span data-ttu-id="5ad71-136">*เวอร์ชัน: 2.86.1321.0 (ตุลาคม 2020) เผยแพร่: 18 พฤศจิกายน 2020*</span><span class="sxs-lookup"><span data-stu-id="5ad71-136">*Version: 2.86.1321.0 (October 2020), Released: November 18, 2020*</span></span>
        - <span data-ttu-id="5ad71-137">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-137">Bug fixes</span></span>
   - <span data-ttu-id="5ad71-138">*เวอร์ชัน: 2.86.961.0 (ตุลาคม 2020) เผยแพร่เมื่อ: 27 ตุลาคม 2020* (รุ่นและเวอร์ชั่นใหม่)</span><span class="sxs-lookup"><span data-stu-id="5ad71-138">*Version: 2.86.961.0 (October 2020), Released: October 27, 2020* (new build and new version)</span></span>
        - <span data-ttu-id="5ad71-139">ประกอบด้วยการเปลี่ยนแปลงที่จำเป็นสำหรับการเชื่อมต่อกับ Power BI Report Server (ตุลาคม 2020)</span><span class="sxs-lookup"><span data-stu-id="5ad71-139">Contains changes required for connection with Power BI Report Server (October 2020)</span></span>        
   
## <a name="may-2020"></a><span data-ttu-id="5ad71-140">พฤษภาคม 2020</span><span class="sxs-lookup"><span data-stu-id="5ad71-140">May 2020</span></span>
- <span data-ttu-id="5ad71-141">**เซิร์ฟเวอร์รายงาน Power BI**</span><span class="sxs-lookup"><span data-stu-id="5ad71-141">**Power BI Report Server**</span></span>
    - <span data-ttu-id="5ad71-142">*เวอร์ชัน: 1.8.7485.35104 (รุ่น 15.0.1103.234), เผยแพร่เมื่อ: 30 มิถุนายน 2020*</span><span class="sxs-lookup"><span data-stu-id="5ad71-142">*Version: 1.8.7485.35104 (Build 15.0.1103.234), Released: June 30, 2020*</span></span>
        - <span data-ttu-id="5ad71-143">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-143">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-144">แก้ไขปัญหาในสถานการณ์ที่ไม่สามารถทำการแก้ไขได้ทันทีในเซิร์ฟเวอร์หลังจากอัปโหลด</span><span class="sxs-lookup"><span data-stu-id="5ad71-144">Fixed an issue in scale-out scenarios where reports weren't reflecting edits immediately in the server after upload.</span></span>
    - <span data-ttu-id="5ad71-145">*เวอร์ชัน: 1.8.7468.41510 (รุ่น 15.0.1103.232), เผยแพร่เมื่อ: 15 มิถุนายน 2020*</span><span class="sxs-lookup"><span data-stu-id="5ad71-145">*Version: 1.8.7468.41510 (Build 15.0.1103.232), Released: June 15, 2020*</span></span>
        - <span data-ttu-id="5ad71-146">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-146">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-147">แก้ไขปัญหาที่รายงานไม่สะท้อนการแก้ไขในเซิร์ฟเวอร์ทันทีหลังจากอัปโหลด</span><span class="sxs-lookup"><span data-stu-id="5ad71-147">Fixed an issue where reports weren't reflecting edits immediately in the server after upload.</span></span>
            - <span data-ttu-id="5ad71-148">แก้ไขปัญหาที่การรีเฟรชล้มเหลวเมื่อมีการใช้การจับคู่ที่ไม่ชัดเจนเพื่อผสานคิวรี</span><span class="sxs-lookup"><span data-stu-id="5ad71-148">Fixed an issue where refresh failed when fuzzy matching was used to merge queries.</span></span>
    - <span data-ttu-id="5ad71-149">*เวอร์ชัน: 1.8.7450.37410 (รุ่น 15.0.1103.227), เผยแพร่เมื่อ: 27 พฤษภาคม 2020*</span><span class="sxs-lookup"><span data-stu-id="5ad71-149">*Version: 1.8.7450.37410 (Build 15.0.1103.227), Released: May 27, 2020*</span></span>
         - <span data-ttu-id="5ad71-150">คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="5ad71-150">Features</span></span>
            -  <span data-ttu-id="5ad71-151">เพิ่มการสนับสนุนสำหรับขนาดพูลการเชื่อมต่อแค็ตตาล็อกที่ปรับแต่งได้ (ดู [การตั้งค่า MaxCatalogConnectionPoolSizePerProcess](/sql/reporting-services/report-server/rsreportserver-config-configuration-file#bkmk_service) สำหรับรายละเอียดเพิ่มเติม)</span><span class="sxs-lookup"><span data-stu-id="5ad71-151">Added support for customizable catalog connection pool size (see [MaxCatalogConnectionPoolSizePerProcess setting](/sql/reporting-services/report-server/rsreportserver-config-configuration-file#bkmk_service) for more details).</span></span>
            -  <span data-ttu-id="5ad71-152">ปรับปรุงลักษณะการทำงานเมื่อดูรายงานในระหว่างการดำเนินการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="5ad71-152">Improved behavior when viewing a report during a refresh operation.</span></span>
        - <span data-ttu-id="5ad71-153">ปรับปรุงความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="5ad71-153">Security updates</span></span>
        - <span data-ttu-id="5ad71-154">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-154">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-155">แก้ไขปัญหาสองเรื่องที่เกี่ยวข้องกับอัญประกาศเดี่ยวในชื่อโฟลเดอร์และรายงาน</span><span class="sxs-lookup"><span data-stu-id="5ad71-155">Fixed two issues relating to single quotes in folder and report names.</span></span>
            - <span data-ttu-id="5ad71-156">แก้ไขปัญหาที่เกี่ยวข้องกับการเลื่อนแนวนอนกับบางเบราว์เซอร์และคุณลักษณะดูระเบียน</span><span class="sxs-lookup"><span data-stu-id="5ad71-156">Fixed an issue relating the horizontal scroll with certain browsers and the See Records feature.</span></span>
            - <span data-ttu-id="5ad71-157">แก้ไขปัญหาที่การรีเฟรชตามกำหนดการในขณะที่เปิดรายงานบางครั้งอาจนำไปสู่ข้อผิดพลาดของ schema ในแบบจำลองเบื้องต้นได้</span><span class="sxs-lookup"><span data-stu-id="5ad71-157">Fixed an issue where scheduled refresh while report open can sometimes lead to schema errors in the underlying model.</span></span>
            - <span data-ttu-id="5ad71-158">แก้ไขปัญหาที่ข้อความแสดงแทนสำหรับการส่งออก PDF ไม่ได้รับการเข้ารหัสอย่างถูกต้องสำหรับอักขระแบบหลายไบต์</span><span class="sxs-lookup"><span data-stu-id="5ad71-158">Fixed an issue where alt text for PDF export were not correctly encoded for multi-byte characters.</span></span>
            - <span data-ttu-id="5ad71-159">แก้ไขปัญหาที่แอปพลิเคชันแบบกำหนดเองดำเนินการ LoadReport จะได้รับข้อผิดพลาด TrustedHeader อย่างไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-159">Fixed an issue where custom applications executing LoadReport would incorrectly receive a TrustedHeader error.</span></span>
            - <span data-ttu-id="5ad71-160">แก้ไขปัญหาที่โหลดจำนวนมากจากการรีเฟรชตามกำหนดเวลาอาจทำให้รีเฟรชล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="5ad71-160">Fixed an issue where heavy load from scheduled refresh could lead to failed refreshes.</span></span>
            - <span data-ttu-id="5ad71-161">แก้ไขปัญหาที่รายงานจะถูกบันทึกไปยังตำแหน่งที่ตั้งที่ไม่ถูกต้องหากชื่อรายงานตรงกับชื่อโฟลเดอร์</span><span class="sxs-lookup"><span data-stu-id="5ad71-161">Fixed an issue where reports would save to the wrong location if the report name matched the folder name.</span></span>
            - <span data-ttu-id="5ad71-162">แก้ไขปัญหาการแท็บในผังเอกสาร</span><span class="sxs-lookup"><span data-stu-id="5ad71-162">Fixed tabbing issues in the Document Map.</span></span>
            - <span data-ttu-id="5ad71-163">แก้ไขปัญหาการสมัครรับใช้งานที่ขับเคลื่อนด้วยข้อมูลล้มเหลวเมื่อใช้คิวรี DAX</span><span class="sxs-lookup"><span data-stu-id="5ad71-163">Fixed an issue with data-driven subscriptions failing when they used DAX queries.</span></span>
            - <span data-ttu-id="5ad71-164">แก้ไขปัญหาในการเข้าถึง URL ที่ทำให้ FindString ไม่พบรายการที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="5ad71-164">Fixed an issue in URL Access causing FindString to not locate matches.</span></span>
            - <span data-ttu-id="5ad71-165">แก้ไขปัญหาที่ทำให้แหล่งข้อมูลแบบฝังตัวหยุดทำงานเมื่อรายงานถูกย้าย</span><span class="sxs-lookup"><span data-stu-id="5ad71-165">Fixed an issue that broke embedded data sources when reports were moved.</span></span>
            - <span data-ttu-id="5ad71-166">แก้ไขปัญหาที่ทำให้การรีเฟรชตามกำหนดเวลาล้มเหลวสำหรับแหล่งข้อมูลบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="5ad71-166">Fixed an issue causing scheduled refresh to fail for certain data sources.</span></span>
            - <span data-ttu-id="5ad71-167">เพิ่มการตรวจสอบเพื่อรายงานกำหนดการเพื่อลดโอกาสสำหรับคำขอที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-167">Added validation to report scheduling to reduce opportunity for invalid requests.</span></span>


- <span data-ttu-id="5ad71-168">**Power BI Desktop (ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI)**</span><span class="sxs-lookup"><span data-stu-id="5ad71-168">**Power BI Desktop (optimized for Power BI Report Server)**</span></span>
   - <span data-ttu-id="5ad71-169">*เวอร์ชัน: 2.81.5831.1181 (พฤษภาคม 2020), เผยแพร่เมื่อ: 9 มิถุนายน 2020*</span><span class="sxs-lookup"><span data-stu-id="5ad71-169">*Version: 2.81.5831.1181 (May 2020), Released: June 9, 2020*</span></span>
        - <span data-ttu-id="5ad71-170">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-170">Bug Fix</span></span>
           -  <span data-ttu-id="5ad71-171">แก้ไขสำหรับวิชวล MarketPlace</span><span class="sxs-lookup"><span data-stu-id="5ad71-171">Fix for MarketPlace visuals</span></span>
   - <span data-ttu-id="5ad71-172">*เวอร์ชัน: 2.81.5831.941 (พฤษภาคม 2020), เผยแพร่เมื่อ: 27 พฤษภาคม 2020* (รุ่นใหม่และเวอร์ชันใหม่)</span><span class="sxs-lookup"><span data-stu-id="5ad71-172">*Version: 2.81.5831.941 (May 2020), Released: May 27, 2020* (new build and new version)</span></span>
        - <span data-ttu-id="5ad71-173">ประกอบด้วยการเปลี่ยนแปลงที่จำเป็นสำหรับการเชื่อมต่อกับ เซิร์ฟเวอร์รายงาน Power BI (พฤษภาคม 2020)</span><span class="sxs-lookup"><span data-stu-id="5ad71-173">Contains changes required for connection with Power BI Report Server (May 2020)</span></span>        
   
## <a name="january-2020"></a><span data-ttu-id="5ad71-174">มกราคม 2020</span><span class="sxs-lookup"><span data-stu-id="5ad71-174">January 2020</span></span>
- <span data-ttu-id="5ad71-175">**เซิร์ฟเวอร์รายงาน Power BI**</span><span class="sxs-lookup"><span data-stu-id="5ad71-175">**Power BI Report Server**</span></span>
    - <span data-ttu-id="5ad71-176">*เวอร์ชัน: 1.6.7364.4075 (รุ่น 15.0.1102.777) เผยแพร่เมื่อ: 2 มีนาคม 2020*</span><span class="sxs-lookup"><span data-stu-id="5ad71-176">*Version: 1.6.7364.4075 (Build 15.0.1102.777), Released: March 2, 2020*</span></span>
         - <span data-ttu-id="5ad71-177">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-177">Bug Fixes</span></span>
           -  <span data-ttu-id="5ad71-178">การแก้ไขสำหรับรายงาน Power BI ไม่สามารถอัปโหลดได้สำหรับแหล่งข้อมูลบางแหล่ง</span><span class="sxs-lookup"><span data-stu-id="5ad71-178">Fix for Power BI reports failing to upload for certain data sources</span></span>
           -  <span data-ttu-id="5ad71-179">การแก้ไขตำแหน่งลิงก์ดาวน์โหลด Power BI Report Server Desktop จากพอร์ทัล</span><span class="sxs-lookup"><span data-stu-id="5ad71-179">Fix for Power BI Report Server Desktop link download location from the portal</span></span>
           -  <span data-ttu-id="5ad71-180">การแก้ไขสำหรับ DynamicImageDPI สำหรับการแสดงภาพ Excel</span><span class="sxs-lookup"><span data-stu-id="5ad71-180">Fix for DynamicImageDPI for Excel rendering</span></span>
           -  <span data-ttu-id="5ad71-181">แก้ไขการเชื่อมต่อ Oracle โดยใช้ลักษณะเธรดที่ไม่ถูกต้องในสถานการณ์ที่มีผู้ใช้หลายคนบางสถานการณ์ (ดูรายละเอียดเพิ่มเติมที่ [UseInstalledUICulture documentation](./connect-data-sources.md))</span><span class="sxs-lookup"><span data-stu-id="5ad71-181">Fix for Oracle connections using incorrect thread culture in certain multi-user scenarios (see [UseInstalledUICulture documentation](./connect-data-sources.md) for more details)</span></span>
           -  <span data-ttu-id="5ad71-182">การแก้ไขสำหรับค่าเริ่มต้น CustomHeaders ที่ทำให้การฝังรายงานไม่สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="5ad71-182">Fix for CustomHeaders default value causing failures for report embedding</span></span>
           -  <span data-ttu-id="5ad71-183">การแก้ไขสำหรับชื่อพารามิเตอร์ SQL ที่ถูกสร้างขึ้นอย่างไม่ถูกต้องในบางกรณี</span><span class="sxs-lookup"><span data-stu-id="5ad71-183">Fix for SQL parameter names being incorrectly generated in certain cases</span></span>
    - <span data-ttu-id="5ad71-184">*เวอร์ชัน: 1.6.7327.3007 (รุ่น 15.0.1102.759) เผยแพร่เมื่อ: 23 มกราคม 2020*</span><span class="sxs-lookup"><span data-stu-id="5ad71-184">*Version: 1.6.7327.3007 (Build 15.0.1102.759), Released: January 23, 2020*</span></span>
         - <span data-ttu-id="5ad71-185">คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="5ad71-185">Features</span></span>
            -  <span data-ttu-id="5ad71-186">ส่งออกไปยัง Excel จากรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ad71-186">Export to Excel from Power BI reports.</span></span>
           -  <span data-ttu-id="5ad71-187">การสนับสนุนชุดข้อมูลใน Power BI Premium สำหรับรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="5ad71-187">Power BI Premium dataset support for paginated reports.</span></span>
           -  <span data-ttu-id="5ad71-188">AltText (ข้อความทางเลือก) สนับสนุนสำหรับองค์ประกอบรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="5ad71-188">AltText (alternative text) support for paginated report elements.</span></span>
           -  <span data-ttu-id="5ad71-189">สนับสนุนส่วนหัวแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="5ad71-189">Support for custom headers.</span></span>
           -  <span data-ttu-id="5ad71-190">การสนับสนุนสำหรับอินสแตนซ์ที่จัดการแล้วของ  Azure SQL โดยเป็นแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="5ad71-190">Support for Azure SQL Managed Instances as the catalog.</span></span>
           -  <span data-ttu-id="5ad71-191">การเข้ารหัสฐานข้อมูลโปร่งใสสำหรับแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="5ad71-191">Transparent Database Encryption for the catalog.</span></span>
        - <span data-ttu-id="5ad71-192">ปรับปรุงความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="5ad71-192">Security updates</span></span>
        - <span data-ttu-id="5ad71-193">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-193">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-194">การแก้ไขสำหรับการเข้าถึงสำหรับโปรแกรมอ่านหน้าจอ การแสดงภาพรายงาน และการนำทางของแป้นพิมพ์</span><span class="sxs-lookup"><span data-stu-id="5ad71-194">Fixes for accessibility for screen readers, report rendering, and keyboard navigation.</span></span>
            - <span data-ttu-id="5ad71-195">การแก้ไขสำหรับการบันทึกชื่อรายงานแบบหลายไบต์</span><span class="sxs-lookup"><span data-stu-id="5ad71-195">Fix for saving multi-byte Report titles.</span></span>
            - <span data-ttu-id="5ad71-196">การแก้ไขสำหรับการบันทึกแบบละเอียด ที่ส่งผลกระทบต่อความน่าเชื่อถือของเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="5ad71-196">Fix for verbose logging affecting report server reliability.</span></span>
          - <span data-ttu-id="5ad71-197">การแก้ไขเพื่อให้แน่ใจในข้อมูลแบบไลฟ์ในรายงาน Power BI บนมือถือ</span><span class="sxs-lookup"><span data-stu-id="5ad71-197">Fix for ensuring live data in Power BI reports on mobile.</span></span>
          - <span data-ttu-id="5ad71-198">การแก้ไขสำหรับการใช้การไฮไลต์ข้ามวิชวลเป็นภาพในการส่งออกรายงาน Power BI ที่ถูกกรอง</span><span class="sxs-lookup"><span data-stu-id="5ad71-198">Fix for applying cross-visual highlighting across as visuals in filtered export of Power BI reports.</span></span>
          - <span data-ttu-id="5ad71-199">การแก้ไขสำหรับการเขียนส่วนท้ายเมื่อส่งออกไปยัง Word ด้วยนิพจน์สำหรับการมองเห็นสำหรับรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="5ad71-199">Fix for writing footer when exporting to Word with expression for visibility for paginated reports.</span></span> 
     
- <span data-ttu-id="5ad71-200">**Power BI Desktop (ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI)**</span><span class="sxs-lookup"><span data-stu-id="5ad71-200">**Power BI Desktop (optimized for Power BI Report Server)**</span></span>
    - <span data-ttu-id="5ad71-201">*เวอร์ชัน: 2.76.5678.1521 (มกราคม 2020) เผยแพร่เมื่อ: 22 มกราคม 2020* (รุ่นใหม่และเวอร์ชันใหม่)</span><span class="sxs-lookup"><span data-stu-id="5ad71-201">*Version: 2.76.5678.1521 (January 2020), Released: January 23, 2020* (new build and new version)</span></span>
        - <span data-ttu-id="5ad71-202">ประกอบด้วยการเปลี่ยนแปลงที่จำเป็นสำหรับการเชื่อมต่อกับเซิร์ฟเวอร์รายงานของ Power BI (มกราคม 2020)</span><span class="sxs-lookup"><span data-stu-id="5ad71-202">Contains changes required for connection with Power BI Report Server (January 2020)</span></span>        


## <a name="september-2019"></a><span data-ttu-id="5ad71-203">กันยายน 2019</span><span class="sxs-lookup"><span data-stu-id="5ad71-203">September 2019</span></span>
- <span data-ttu-id="5ad71-204">**เซิร์ฟเวอร์รายงาน Power BI**</span><span class="sxs-lookup"><span data-stu-id="5ad71-204">**Power BI Report Server**</span></span>
    - <span data-ttu-id="5ad71-205">*เวอร์ชัน: 1.6.7236.4246 (รุ่น 15.0.1102.646), เผยแพร่เมื่อ: 25 ตุลาคม 2019*</span><span class="sxs-lookup"><span data-stu-id="5ad71-205">*Version: 1.6.7236.4246 (Build 15.0.1102.646), Released: October 25, 2019*</span></span>
        - <span data-ttu-id="5ad71-206">ปรับปรุงความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="5ad71-206">Security updates</span></span>
        - <span data-ttu-id="5ad71-207">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-207">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-208">ไม่ได้ติดตั้งการแก้ไขสำหรับ .net framework 4.7</span><span class="sxs-lookup"><span data-stu-id="5ad71-208">Fix for .net framework 4.7 not installed.</span></span>
            - <span data-ttu-id="5ad71-209">การแก้ไขสำหรับรายงานที่มีการแบ่งหน้าสำหรับ Teradata ด้วยพารามิเตอร์แบบหลายค่าที่มีข้อผิดพลาด 110083</span><span class="sxs-lookup"><span data-stu-id="5ad71-209">Fix for paginated reports for Teradata with multivalue parameters with error 110083.</span></span>
            - <span data-ttu-id="5ad71-210">การแก้ไขสำหรับค่า URLRoot ไม่สามารถใช้ได้ถ้ามีการเชื่อมโยง URL ของบริการบนเว็บหลายรายการและหนึ่งในนั้นคือ https://+80/reportserver</span><span class="sxs-lookup"><span data-stu-id="5ad71-210">Fix for URLRoot value not work if there are multiple web service URL bindings and one of them is https://+80/reportserver.</span></span>
          - <span data-ttu-id="5ad71-211">การแก้ไขสำหรับค่าพารามิเตอร์แบบหลายค่าที่แสดงอยู่ภายนอกพื้นที่ของรายงาน</span><span class="sxs-lookup"><span data-stu-id="5ad71-211">Fix for paginated reports multivalue parameter values showing up outside the report area.</span></span>
          
    - <span data-ttu-id="5ad71-212">*เวอร์ชัน: 1.6.7221.30698 (Build 15.0.1102.620) เผยแพร่: 9 ตุลาคม 2019*</span><span class="sxs-lookup"><span data-stu-id="5ad71-212">*Version: 1.6.7221.30698 (Build 15.0.1102.620), Released: October 9, 2019*</span></span>
        - <span data-ttu-id="5ad71-213">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-213">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-214">แก้ไขการแสดงผลด้วยภาพแบบกำหนดเองของตัวกรองข้อความ</span><span class="sxs-lookup"><span data-stu-id="5ad71-214">Fix for Text Filter custom visual.</span></span>
            - <span data-ttu-id="5ad71-215">แก้ไขประสิทธิภาพการทำงานของตัวแบ่งส่วนข้อมูลดรอปดาวน์</span><span class="sxs-lookup"><span data-stu-id="5ad71-215">Fix for the performance of drop-down slicers.</span></span>
            - <span data-ttu-id="5ad71-216">แก้ไขข้อมูล Strip PII จากการวัดและส่งข้อมูลทางไกล</span><span class="sxs-lookup"><span data-stu-id="5ad71-216">Fix for Strip PII from telemetry.</span></span>
          - <span data-ttu-id="5ad71-217">แก้ไขลิงก์ URL ที่ไม่ตรงตามกรณี</span><span class="sxs-lookup"><span data-stu-id="5ad71-217">Fix for URLs to not be case sensitive.</span></span>
          
    - <span data-ttu-id="5ad71-218">*เวอร์ชั่น 1.6.7206.38019 (Build 15.0.1102.597) เผยแพร่: 26 กันยายน 2019*</span><span class="sxs-lookup"><span data-stu-id="5ad71-218">*Version 1.6.7206.38019 (Build 15.0.1102.597), Released: September 26, 2019*</span></span>
        - <span data-ttu-id="5ad71-219">ปรับปรุงความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="5ad71-219">Security updates</span></span>
        - <span data-ttu-id="5ad71-220">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-220">Bug fixes</span></span>
           - <span data-ttu-id="5ad71-221">รายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="5ad71-221">Paginated reports</span></span>
             - <span data-ttu-id="5ad71-222">แก้ไขปัญหาการใช้งานที่พบขณะใช้ Internet Explorer และ Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5ad71-222">Fix for accessibility issues encountered while using Internet Explorer and Microsoft Edge.</span></span>
             - <span data-ttu-id="5ad71-223">แก้ไขปัญหา SAP HANA ขณะทดสอบการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="5ad71-223">Fix for SAP HANA issues while testing connection.</span></span>
             - <span data-ttu-id="5ad71-224">แก้ไขปัญหาที่พบขณะแจ้งรายการอีเมลแอดเดรส</span><span class="sxs-lookup"><span data-stu-id="5ad71-224">Fix for issues found while providing list of email addresses.</span></span>
             - <span data-ttu-id="5ad71-225">แก้ไขปัญหาสำหรับรายงาน Power BI ที่ใช้แหล่งข้อมูล DirectQuery และการรับรองความถูกต้องในตัว</span><span class="sxs-lookup"><span data-stu-id="5ad71-225">Fix for for Power BI reports that use a DirectQuery data source and integrated authentication.</span></span>
             - <span data-ttu-id="5ad71-226">แก้ไขปัญหาสำหรับรายงานแบบแบ่งหน้าเพื่อเรนเดอร์กับพารามิเตอร์ตัวกรองขณะเปิดใช้สแนปช็อต</span><span class="sxs-lookup"><span data-stu-id="5ad71-226">Fix for Paginated reports to render with filter parameters when snapshot is enabled.</span></span>
             - <span data-ttu-id="5ad71-227">แก้ไขปัญหาการดำเนินการซ้ำซ้อนสำหรับกระบวนการที่จัดเก็บไว้ระหว่างการจัดทำรายงาน</span><span class="sxs-lookup"><span data-stu-id="5ad71-227">Fix for double execution of stored procedures during report execution.</span></span>
             - <span data-ttu-id="5ad71-228">แก้ไขปัญหาบัญชีบริการเริ่มต้นได้รับอนุญาตให้ล็อกอินใน SQL Server ขณะที่บัญชีบริการกำหนดเองถูกกำหนดค่าให้เรียกใช้เซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ad71-228">Fix for default service account being granted SQL Server login permissions, when custom service account is configured to run the Power BI Report Server.</span></span>
             - <span data-ttu-id="5ad71-229">แก้ไขปัญหาสำหรับการใช้งานโมเดลและการรีเฟรชเขตเวลาสำหรับญี่ปุ่น</span><span class="sxs-lookup"><span data-stu-id="5ad71-229">Fix for accessing models meanwhile refreshing in Japanese time zone.</span></span>
             - <span data-ttu-id="5ad71-230">แก้ไขปัญหาสำหรับโมเดลล้าสมัยเมื่อมีรายงานเวอร์ชั่นใหม่ถูกอัปโหลดเข้ามาระหว่างการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="5ad71-230">Fix for stale models when a new version of the report is uploaded during refresh.</span></span>
             - <span data-ttu-id="5ad71-231">แก้ไขปัญหาสำหรับค่าพารามิเตอร์ที่มีอักขระ ‘&’</span><span class="sxs-lookup"><span data-stu-id="5ad71-231">Fix for parameter values that contain the '&' character'.</span></span>
         - <span data-ttu-id="5ad71-232">ความสามารถในการโปรแกรม</span><span class="sxs-lookup"><span data-stu-id="5ad71-232">Programmability</span></span>
             - <span data-ttu-id="5ad71-233">API ทางเว็บแบบอัปเดต: /PowerBIReports({Id})/DataSources (ชุดข้อมูลแก้ไข) สำหรับอัปเดตสติงการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="5ad71-233">Updated Web API: /PowerBIReports({Id})/DataSources (PATCH) to allow connection string updates.</span></span>
         
- <span data-ttu-id="5ad71-234">**Power BI Desktop (ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI)**</span><span class="sxs-lookup"><span data-stu-id="5ad71-234">**Power BI Desktop (optimized for Power BI Report Server)**</span></span>
    - <span data-ttu-id="5ad71-235">*เวอร์ชัน: 2.73.5586.1501 (กันยายน 2019) เผยแพร่เมื่อ: 25 ตุลาคม 2019*</span><span class="sxs-lookup"><span data-stu-id="5ad71-235">*Version: 2.73.5586.1501 (September 2019), Released: October 25, 2019*</span></span>
        - <span data-ttu-id="5ad71-236">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-236">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-237">การแก้ไขสำหรับ Telemetry</span><span class="sxs-lookup"><span data-stu-id="5ad71-237">Fix for Telemetry.</span></span>
            
    - <span data-ttu-id="5ad71-238">*เวอร์ชัน: 2.73.5586.1241 (กันยายน 2019) เผยแพร่: 9 ตุลาคม 2019*</span><span class="sxs-lookup"><span data-stu-id="5ad71-238">*Version: 2.73.5586.1241 (September 2019), Released: October 9, 2019*</span></span>
        - <span data-ttu-id="5ad71-239">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-239">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-240">แก้ไขการแสดงผลด้วยภาพแบบกำหนดเองของตัวกรองข้อความ</span><span class="sxs-lookup"><span data-stu-id="5ad71-240">Fix for Text Filter custom visual.</span></span>
            - <span data-ttu-id="5ad71-241">แก้ไขประสิทธิภาพการทำงานของตัวแบ่งส่วนข้อมูลดรอปดาวน์</span><span class="sxs-lookup"><span data-stu-id="5ad71-241">Fix for the performance of drop down slicers.</span></span>
            - <span data-ttu-id="5ad71-242">แก้ไขข้อมูล Strip PII จากการวัดและส่งข้อมูลทางไกล</span><span class="sxs-lookup"><span data-stu-id="5ad71-242">Fix for Strip PII from telemetry.</span></span>
            
    - <span data-ttu-id="5ad71-243">*เวอร์ชัน: 2.73.5586.821 (กันยายน 2019) เผยแพร่: 26 กันยายน 2019* (บิลท์และเวอร์ชั่นใหม่)</span><span class="sxs-lookup"><span data-stu-id="5ad71-243">*Version: 2.73.5586.821 (September 2019), Released: September 26, 2019* (new build and new version)</span></span>
        - <span data-ttu-id="5ad71-244">ประกอบด้วยการเปลี่ยนแปลงที่จำเป็นสำหรับการเชื่อมต่อกับเซิร์ฟเวอร์รายงาน Power BI (กันยายน 2019)</span><span class="sxs-lookup"><span data-stu-id="5ad71-244">Contains changes required for connection with Power BI Report Server (September 2019)</span></span>

    
## <a name="may-2019"></a><span data-ttu-id="5ad71-245">พฤษภาคม 2019</span><span class="sxs-lookup"><span data-stu-id="5ad71-245">May 2019</span></span>

- <span data-ttu-id="5ad71-246">**เซิร์ฟเวอร์รายงาน Power BI**</span><span class="sxs-lookup"><span data-stu-id="5ad71-246">**Power BI Report Server**</span></span>          
    - <span data-ttu-id="5ad71-247">*เวอร์ชัน 1.5.7074.36177 (รุ่น 15.0.1102.371), เผยแพร่: 21 พฤษภาคม 2019*</span><span class="sxs-lookup"><span data-stu-id="5ad71-247">*Version 1.5.7074.36177 (Build 15.0.1102.371), Released: May 21, 2019*</span></span>
        - <span data-ttu-id="5ad71-248">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-248">Bug Fixes</span></span>
            - <span data-ttu-id="5ad71-249">รายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="5ad71-249">Paginated Reports</span></span>
                - <span data-ttu-id="5ad71-250">แก้ไขเพื่อเปิดใช้งานการฝังฟอนต์ใน pdf เสมอ</span><span class="sxs-lookup"><span data-stu-id="5ad71-250">Fix to always enable pdf font-embedding.</span></span>
                - <span data-ttu-id="5ad71-251">แก้ไขเพื่อตั้งค่าคุกกี้ที่ส่งผ่านทาง https เป็นแบบปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="5ad71-251">Fix to set cookies sent over https as Secure</span></span>
                - <span data-ttu-id="5ad71-252">แก้ไขปัญหาเกี่ยวกับป็อปอัพเนื่องจากข้อผิดพลาดเกี่ยวกับสคริปต์</span><span class="sxs-lookup"><span data-stu-id="5ad71-252">Fix to issues with pop ups due to script errors</span></span>
                - <span data-ttu-id="5ad71-253">แก้ไขปัญหาการแสดงผลกับแอปบนโทรศัพท์ Android</span><span class="sxs-lookup"><span data-stu-id="5ad71-253">Fix for display issues with Mobile App on Android phones</span></span>
                - <span data-ttu-id="5ad71-254">แก้ไขตัวนำทางเวลาของรายงานอุปกรณ์มือถือเพื่อแสดงจำนวนสัปดาห์ที่ถูกต้องโดยไม่คำนึงถึงจุดเริ่มต้นของปีงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="5ad71-254">Fix for Mobile Report Time Navigator to show the correct week numbers irrespective of the start of Fiscal year</span></span>
                - <span data-ttu-id="5ad71-255">คุณสมบัติท่ีกำหนดค่าได้ 'RestrictedResourceMimeTypeForUpload' ที่เพิ่มสำหรับผู้ดูแลระบบเพื่อระบุประเภท mime ที่ถูกแบน</span><span class="sxs-lookup"><span data-stu-id="5ad71-255">Added 'RestrictedResourceMimeTypeForUpload' configurable property for admins to specify banned mime types</span></span>
         - <span data-ttu-id="5ad71-256">คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="5ad71-256">Features</span></span>
            - <span data-ttu-id="5ad71-257">การเพิ่มการสนับสนุนสำหรับการแสดงผลด้วยภาพที่เชื่อถือได้ใน PBIRS</span><span class="sxs-lookup"><span data-stu-id="5ad71-257">Adding support for Trusted Visuals to PBIRS</span></span>

- <span data-ttu-id="5ad71-258">**Power BI Desktop (ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI)**</span><span class="sxs-lookup"><span data-stu-id="5ad71-258">**Power BI Desktop (optimized for Power BI Report Server)**</span></span>
    - <span data-ttu-id="5ad71-259">*เวอร์ชัน: 2.69.5467.1801 (พฤษภาคม 2019), เผยแพร่: 21 พฤษภาคม 2019*</span><span class="sxs-lookup"><span data-stu-id="5ad71-259">*Version: 2.69.5467.1801 (May 2019), Released: May 21, 2019*</span></span>
        - <span data-ttu-id="5ad71-260">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-260">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-261">แก้ไขเพื่อหลีกเลี่ยงการป้อนข้อมูลประจำตัวซ้ำในระหว่างการอัปโหลด PBIX ใน PBIRS</span><span class="sxs-lookup"><span data-stu-id="5ad71-261">Fix to avoid re-entry of credentials during PBIX upload to PBIRS</span></span>
            - <span data-ttu-id="5ad71-262">แก้ไขเอกสารที่เปิดอยู่ที่ม # ในชื่อไฟล์</span><span class="sxs-lookup"><span data-stu-id="5ad71-262">Fixes opening documents with # in the filename</span></span>
            - <span data-ttu-id="5ad71-263">เพิ่มลิงก์ที่ง่ายขึ้นสำหรับการนำทางย้อนกลับบนหน้าต่างการเลือก PBIRS</span><span class="sxs-lookup"><span data-stu-id="5ad71-263">Added easier link for back navigation on PBIRS Selection window</span></span>
            - <span data-ttu-id="5ad71-264">แก้ไขโหมดความคมชัดสูงใน PBIRS เพื่อแสดงปุ่มย้อนกลับ แสดงภาพข้อความเตือน</span><span class="sxs-lookup"><span data-stu-id="5ad71-264">Fix to High Contrast mode in PBIRS to display Back button, show warning visual messages.</span></span>
            - <span data-ttu-id="5ad71-265">แก้ไข UI ในบานหน้าต่างตัวเลือก การปรับมาตราส่วนพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="5ad71-265">UI fixes to Selection pane, canvas scaling.</span></span>

    - <span data-ttu-id="5ad71-266">*เวอร์ชัน: 2.69.5467.5201 (พฤษภาคม 2019), เผยแพร่เมื่อ: 30 กรกฎาคม 2019*</span><span class="sxs-lookup"><span data-stu-id="5ad71-266">*Version: 2.69.5467.5201 (May 2019), Released: July 30, 2019*</span></span>
        - <span data-ttu-id="5ad71-267">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-267">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-268">แก้ไขสำหรับรายการบันทึกการวัดและส่งข้อมูลทางไกลที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-268">Fix for incorrect telemetry logging</span></span>

## <a name="january-2019"></a><span data-ttu-id="5ad71-269">มกราคม 2019</span><span class="sxs-lookup"><span data-stu-id="5ad71-269">January 2019</span></span>

- <span data-ttu-id="5ad71-270">**เซิร์ฟเวอร์รายงาน Power BI**</span><span class="sxs-lookup"><span data-stu-id="5ad71-270">**Power BI Report Server**</span></span>          
    - <span data-ttu-id="5ad71-271">*เวอร์ชัน 1.4.7024.16477 (รุ่น 15.0.1102.299), เผยแพร่: 28 มีนาคม 2019*</span><span class="sxs-lookup"><span data-stu-id="5ad71-271">*Version 1.4.7024.16477 (Build 15.0.1102.299), Released: March 28, 2019*</span></span>
        - <span data-ttu-id="5ad71-272">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-272">Bug Fixes</span></span>
            - <span data-ttu-id="5ad71-273">รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ad71-273">Power BI Reports</span></span>
                - <span data-ttu-id="5ad71-274">แก้ไขปัญหาเกี่ยวกับข้อมูลประจำตัวพื้นฐานเมื่อมีการใช้คิวรีโดยตรงสำหรับ SAP Hana และ SAP BW</span><span class="sxs-lookup"><span data-stu-id="5ad71-274">Fix for issue with basic credentials when using direct query for SAP Hana and SAP BW</span></span>
                - <span data-ttu-id="5ad71-275">แก้ไขสำหรับการรีเฟรชข้อมูลที่ดึงข้อมูล OData ที่ล้มเหลวด้วยข้อความ "ไม่สามารถโหลดไฟล์หรือแอสเซมบลี 'Microsoft.OData.Core.NetFX35.V7"</span><span class="sxs-lookup"><span data-stu-id="5ad71-275">Fix for OData feed data refresh fails with "Could not load file or assembly 'Microsoft.OData.Core.NetFX35.V7"</span></span>

- <span data-ttu-id="5ad71-276">**เซิร์ฟเวอร์รายงาน Power BI**</span><span class="sxs-lookup"><span data-stu-id="5ad71-276">**Power BI Report Server**</span></span>            
    - <span data-ttu-id="5ad71-277">*เวอร์ชัน 1.4.6969.7395 (รุ่น 15.0.1102.235), เผยแพร่: 30 มกราคม 2019*</span><span class="sxs-lookup"><span data-stu-id="5ad71-277">*Version 1.4.6969.7395 (Build 15.0.1102.235), Released: January 30, 2019*</span></span>
        - <span data-ttu-id="5ad71-278">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-278">Bug Fixes</span></span>
            - <span data-ttu-id="5ad71-279">รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ad71-279">Power BI Reports</span></span>
                - <span data-ttu-id="5ad71-280">แก้ไขปัญหาเกี่ยวกับข้อมูลประจำตัวพื้นฐานเมื่อมีการใช้คิวรีโดยตรง</span><span class="sxs-lookup"><span data-stu-id="5ad71-280">Fix for issue with basic credentials when using direct query</span></span>
                - <span data-ttu-id="5ad71-281">แก้ไขปัญหาเกี่ยวกับความสัมพันธ์แบบสองทิศทางโดยใช้ตัวกรองความปลอดภัยระดับแถว</span><span class="sxs-lookup"><span data-stu-id="5ad71-281">Fix for bidirectional relationships with row-level security filters applied</span></span>
                - <span data-ttu-id="5ad71-282">แก้ไขปัญหาเกี่ยวกับข้อมูลเก่าหลังจากรีเฟรชแบบจำลองในสภาพแวดล้อมแบบแนวกว้าง</span><span class="sxs-lookup"><span data-stu-id="5ad71-282">Fix for stale data after a model refresh in a scale-out environment</span></span>
                - <span data-ttu-id="5ad71-283">แก้ไขปัญหาเกี่ยวกับแถบเลื่อนที่สองสำหรับตาราง / เมทริกซ์บน Firefox 63 +</span><span class="sxs-lookup"><span data-stu-id="5ad71-283">Fix for double scrollbar for table/ matrix on Firefox 63+</span></span>
                - <span data-ttu-id="5ad71-284">แก้ไขปัญหาเกี่ยวกับขนาดไอคอน +/- ใน Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="5ad71-284">Fix for +/- icon size in Internet Explorer</span></span>
            - <span data-ttu-id="5ad71-285">รายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="5ad71-285">Paginated Reports</span></span>
                - <span data-ttu-id="5ad71-286">แก้ไขปัญหาเกี่ยวกับการอัปเดตเพื่อเป็นแหล่งข้อมูลที่ใช้ร่วมกันสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="5ad71-286">Fix for issue with updating usage of a shared datasource for a report</span></span>

    - <span data-ttu-id="5ad71-287">*เวอร์ชัน 1.4.6960.38798 (รุ่น 15.0.1102.222), เผยแพร่: 22 มกราคม 2019*</span><span class="sxs-lookup"><span data-stu-id="5ad71-287">*Version 1.4.6960.38798 (Build 15.0.1102.222), Released: January 22, 2019*</span></span>
        - <span data-ttu-id="5ad71-288">คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="5ad71-288">Features</span></span>
            - <span data-ttu-id="5ad71-289">รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ad71-289">Power BI Reports</span></span> 
                - <span data-ttu-id="5ad71-290">สนับสนุนสำหรับการรักษาความปลอดภัยระดับแถว</span><span class="sxs-lookup"><span data-stu-id="5ad71-290">Support for Row-level security</span></span>
                - <span data-ttu-id="5ad71-291">ขยายและยุบบนส่วนหัวของแถวเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="5ad71-291">Expand and collapse on matrix row headers</span></span>
                - <span data-ttu-id="5ad71-292">คัดลอกและวางระหว่างไฟล์ .pbix</span><span class="sxs-lookup"><span data-stu-id="5ad71-292">Copy and paste between .pbix files</span></span>
                - <span data-ttu-id="5ad71-293">เส้นบอกแนวสำหรับการจัดแนวแบบสมาร์ท</span><span class="sxs-lookup"><span data-stu-id="5ad71-293">Smart alignment guides</span></span>
                - <span data-ttu-id="5ad71-294">รองรับฟีเจอร์ SAP BW 2.0 Connector</span><span class="sxs-lookup"><span data-stu-id="5ad71-294">Support for SAP BW 2.0 Connector</span></span>
            - <span data-ttu-id="5ad71-295">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="5ad71-295">Administrators</span></span>
                - <span data-ttu-id="5ad71-296">ความสามารถในการจำกัดส่วนขยายของทรัพยากรที่สามารถอัปโหลดไปยังเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="5ad71-296">Ability to restrict extensions of resources that can be uploaded to the report server</span></span>
                - <span data-ttu-id="5ad71-297">ความสามารถในการจำกัดแผนการเชื่อมโยงหลายมิติที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="5ad71-297">Ability to restrict supported hyperlink schemes</span></span>
            - <span data-ttu-id="5ad71-298">ความสามารถในการโปรแกรม</span><span class="sxs-lookup"><span data-stu-id="5ad71-298">Programmability</span></span>
                - <span data-ttu-id="5ad71-299">API เว็บใหม่: / PowerBIReports({Id})/DataModelRoles (รับ)</span><span class="sxs-lookup"><span data-stu-id="5ad71-299">New Web API: /PowerBIReports({Id})/DataModelRoles (GET)</span></span>
                - <span data-ttu-id="5ad71-300">API เว็บใหม่: / PowerBIReports({Id})/DataModelRolesAssignments (รับ & ส่ง)</span><span class="sxs-lookup"><span data-stu-id="5ad71-300">New Web API: /PowerBIReports({Id})/DataModelRoleAssignments (GET & PUT)</span></span>
                - <span data-ttu-id="5ad71-301">ดู[REST API ของเซิร์ฟเวอร์รายงาน Power BI](https://app.swaggerhub.com/apis/microsoft-rs/PBIRS/2.0)สำหรับรายละเอียดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5ad71-301">See [Power BI Report Server REST API](https://app.swaggerhub.com/apis/microsoft-rs/PBIRS/2.0) for more details</span></span>
        - <span data-ttu-id="5ad71-302">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-302">Bug Fixes</span></span>
            - <span data-ttu-id="5ad71-303">ช่องโหว่สำหรับการโจมตีแบบ HTML Injection</span><span class="sxs-lookup"><span data-stu-id="5ad71-303">HTML Injection Vulnerability</span></span>
            - <span data-ttu-id="5ad71-304">ส่งออกเป็น PDF ไม่แสดงสัญลักษณ์สกุลเงินยูโร</span><span class="sxs-lookup"><span data-stu-id="5ad71-304">Export to PDF is not showing Euro symbol</span></span>
            - <span data-ttu-id="5ad71-305">การบันทึกรหัสผ่านด้วยแหล่งข้อมูลหลายแห่งในรายงาน Power BI ทำให้รหัสผ่านที่ไม่มีการเปลี่ยนแปลงไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-305">Saving a password with multiple data sources in Power BI reports invalidates non changed passwords</span></span>
            - <span data-ttu-id="5ad71-306">ภาพแสดงปัญหาใน Power BI Mobile App หลังจากไม่มีการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="5ad71-306">Visuals display issues in Power BI Mobile App after being idle</span></span>

- <span data-ttu-id="5ad71-307">**Power BI Desktop (ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI)**</span><span class="sxs-lookup"><span data-stu-id="5ad71-307">**Power BI Desktop (optimized for Power BI Report Server)**</span></span>
    - <span data-ttu-id="5ad71-308">*เวอร์ชัน: 2.65.5313.1562 (2019 มกราคม), เผยแพร่: 30 มกราคม 2019*</span><span class="sxs-lookup"><span data-stu-id="5ad71-308">*Version: 2.65.5313.1562 (January 2019), Released: January 30, 2019*</span></span>
        - <span data-ttu-id="5ad71-309">ทางลัดและไอคอนปักหมุดจะยังคงอยู่หลังจากถอนการติดตั้งเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ad71-309">Shortcut and pinned icons remain after uninstalling Power BI Report Server</span></span>
        - <span data-ttu-id="5ad71-310">แก้ไขการปักหมุดเซิร์ฟเวอร์รายงาน Power BI ไปยังเมนูเริ่มต้นจะทำให้ข้อความเป็นสีดำบนไอคอนสีดำ</span><span class="sxs-lookup"><span data-stu-id="5ad71-310">Fix for pinning Power BI Report Server to start menu giving black text on a black icon</span></span>

    - <span data-ttu-id="5ad71-311">*เวอร์ชัน: 2.65.5313.1421 (2019 มกราคม), เผยแพร่: 22 มกราคม 2019* (รุ่นใหม่และเวอร์ชันใหม่)</span><span class="sxs-lookup"><span data-stu-id="5ad71-311">*Version: 2.65.5313.1421 (January 2019), Released: January 22, 2019* (new build and new version)</span></span>
        - <span data-ttu-id="5ad71-312">ประกอบด้วยการเปลี่ยนแปลงที่จำเป็นสำหรับการเชื่อมต่อกับเซิร์ฟเวอร์รายงาน Power BI (มกราคม 2019)</span><span class="sxs-lookup"><span data-stu-id="5ad71-312">Contains changes required for connection with Power BI Report Server (January 2019)</span></span> 
    - <span data-ttu-id="5ad71-313">*เวอร์ชัน: 2.65.5313.5141 (มกราคม 2019), เผยแพร่เมื่อ: 31 กรกฎาคม 2019* (รุ่นใหม่และเวอร์ชันใหม่)</span><span class="sxs-lookup"><span data-stu-id="5ad71-313">*Version: 2.65.5313.5141 (January 2019), Released: July 31, 2019* (new build and new version)</span></span>
        - <span data-ttu-id="5ad71-314">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-314">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-315">แก้ไขสำหรับรายการบันทึกการวัดและส่งข้อมูลทางไกลที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-315">Fix for incorrect telemetry logging</span></span>

## <a name="august-2018"></a><span data-ttu-id="5ad71-316">สิงหาคม 2018</span><span class="sxs-lookup"><span data-stu-id="5ad71-316">August 2018</span></span>

- <span data-ttu-id="5ad71-317">**เซิร์ฟเวอร์รายงาน Power BI**</span><span class="sxs-lookup"><span data-stu-id="5ad71-317">**Power BI Report Server**</span></span>
    - <span data-ttu-id="5ad71-318">*เวอร์ชัน 1.3.6816.37243 (รุ่น 15.0.2.557), เผยแพร่: 30 สิงหาคม 2018*</span><span class="sxs-lookup"><span data-stu-id="5ad71-318">*Version 1.3.6816.37243 (Build 15.0.2.557), Released: August 30, 2018*</span></span>
        - <span data-ttu-id="5ad71-319">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-319">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-320">แก้ไขปัญหาเมื่อเซิร์ฟเวอร์มีการอัปเกรดจากเวอร์ชันก่อนหน้าของเซิร์ฟเวอร์รายงาน PBI ที่เปลี่ยนเส้นทางการผูกที่ไม่มีการอัปเดต ลูกค้าจะเห็นข้อความนี้:</span><span class="sxs-lookup"><span data-stu-id="5ad71-320">Fixed an issue when server was upgraded from earlier versions of PBI Report Server where a binding redirect was not updated, customers saw this message:</span></span>      
            *`
            Failed to load expression host assembly. Details: Could not load file or assembly 'Microsoft.ReportingServices.ProcessingObjectModel, Version=2018.7.0.0, Culture=neutral, PublicKeyToken=89845dcd8080cc91' or one of its dependencies. The located assembly's manifest definition does not match the assembly reference. (Exception from HRESULT: 0x80131040) (rsErrorLoadingExprHostAssembly)
             `*
             
            - <span data-ttu-id="5ad71-321">ข้อบกพร่องสำหรับความโปร่งใสของป้ายชื่อข้อมูลได้รับการแก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="5ad71-321">Bug for Data Label Transparency is now fixed.</span></span>
            
    - <span data-ttu-id="5ad71-322">*เวอร์ชัน 1.3.6801.38816 (รุ่น 15.0.2.540), เผยแพร่: 15 สิงหาคม 2018*</span><span class="sxs-lookup"><span data-stu-id="5ad71-322">*Version 1.3.6801.38816 (Build 15.0.2.540), Released: August 15, 2018*</span></span>
        - <span data-ttu-id="5ad71-323">คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="5ad71-323">Features</span></span>
            - <span data-ttu-id="5ad71-324">สนับสนุนคิวรีโดยตรง SAP HANA SSO ด้วย Kerberos สำหรับรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ad71-324">SAP HANA SSO Direct Query support with Kerberos now available for Power BI Reports</span></span>
            - <span data-ttu-id="5ad71-325">API ภาพแบบกำหนดเองที่จัดส่งพร้อมการเผยแพร่ - เวอร์ชัน 1.13.0</span><span class="sxs-lookup"><span data-stu-id="5ad71-325">Custom Visual API shipped with release  - version 1.13.0</span></span>
            - <span data-ttu-id="5ad71-326">วิชวล Power BI จะแสดงแทนเวอร์ชันก่อนหน้าที่สามารถเข้ากันได้กับรุ่นปัจจุบันของ API ของเซิร์ฟเวอร์ (ถ้ามี)</span><span class="sxs-lookup"><span data-stu-id="5ad71-326">Power BI visuals will fall back to a previous version compatible with the current version of the server API (if available)</span></span>

- <span data-ttu-id="5ad71-327">**Power BI Desktop (ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI)**</span><span class="sxs-lookup"><span data-stu-id="5ad71-327">**Power BI Desktop (optimized for Power BI Report Server)**</span></span>
    - <span data-ttu-id="5ad71-328">*เวอร์ชัน: 2.61.5192.641 (สิงหาคม 2018), เผยแพร่: 15 สิงหาคม 2018*</span><span class="sxs-lookup"><span data-stu-id="5ad71-328">*Version: 2.61.5192.641 (August 2018), Released: August 15, 2018*</span></span>
        - <span data-ttu-id="5ad71-329">ประกอบด้วยการเปลี่ยนแปลงที่จำเป็นสำหรับการเชื่อมต่อกับเซิร์ฟเวอร์รายงาน Power BI (สิงหาคม 2018)</span><span class="sxs-lookup"><span data-stu-id="5ad71-329">Contains changes required for connection with Power BI Report Server (August 2018)</span></span>         
    - <span data-ttu-id="5ad71-330">*เวอร์ชัน: 2.61.5192.7701 (สิงหาคม 2018), เผยแพร่เมื่อ: 8 สิงหาคม 2019* (รุ่นใหม่และเวอร์ชันใหม่)</span><span class="sxs-lookup"><span data-stu-id="5ad71-330">*Version: 2.61.5192.7701 (August 2018), Released: August 8, 2019* (new build and new version)</span></span>
        - <span data-ttu-id="5ad71-331">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-331">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-332">แก้ไขสำหรับรายการบันทึกการวัดและส่งข้อมูลทางไกลที่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-332">Fix for incorrect telemetry logging</span></span>
            
## <a name="march-2018"></a><span data-ttu-id="5ad71-333">มีนาคม 2018</span><span class="sxs-lookup"><span data-stu-id="5ad71-333">March 2018</span></span>

- <span data-ttu-id="5ad71-334">**เซิร์ฟเวอร์รายงาน Power BI**</span><span class="sxs-lookup"><span data-stu-id="5ad71-334">**Power BI Report Server**</span></span>
    - <span data-ttu-id="5ad71-335">*เวอร์ชัน 1.2.6690.34729 (รุ่น 15.0.2.402), เผยแพร่: 27 เมษายน 2018*</span><span class="sxs-lookup"><span data-stu-id="5ad71-335">*Version 1.2.6690.34729 (Build 15.0.2.402), Released: April 27, 2018*</span></span>
        - <span data-ttu-id="5ad71-336">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-336">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-337">เปิดใช้งานการโยกย้ายของแค็ตตาล็อก SQL Server Reporting Services 2017</span><span class="sxs-lookup"><span data-stu-id="5ad71-337">Enable migration of SQL Server Reporting Services 2017 catalogs</span></span>
            - <span data-ttu-id="5ad71-338">สำหรับรายงาน Power BI (PBIX)</span><span class="sxs-lookup"><span data-stu-id="5ad71-338">For Power BI Reports (PBIX)</span></span>
                - <span data-ttu-id="5ad71-339">รายงานสามารถรีเฟรชเมื่อเซิร์ฟเวอร์ถูกกำหนดค่าให้ใช้การรับรองความถูกต้องแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="5ad71-339">Reports can be refresh when a server is configured to use custom authentication</span></span>
                - <span data-ttu-id="5ad71-340">การปรับเปลี่ยนคุณสมบัติของรายงาน จะไม่รีเซ็ตข้อมูลประจำตัวของแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5ad71-340">Modifying the properties of a report does not reset data source credentials</span></span>
            - <span data-ttu-id="5ad71-341">สำหรับรายงานที่มีการแบ่งหน้า (RDL)</span><span class="sxs-lookup"><span data-stu-id="5ad71-341">For Paginated Reports (RDL)</span></span>
                - <span data-ttu-id="5ad71-342">การใช้ `Lookup()` หรือฟังก์ชันดัดแปลง เช่น `LookupSet()` และ `MultiLookup()` ที่แสดงใน RDL ไม่สามารถแสดงผลลัพธ์ `#Error`อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="5ad71-342">Usage of `Lookup()` or derivative functions such as `LookupSet()` and `MultiLookup()` in RDL Expressions no longer result in `#Error`</span></span>
                - <span data-ttu-id="5ad71-343">รายงานที่เชื่อมโยง เคารพขนาดหน้าของรายงานเป้าหมายเมื่อพิมพ์</span><span class="sxs-lookup"><span data-stu-id="5ad71-343">Linked reports respect the page size of the target report when printing</span></span>
                - <span data-ttu-id="5ad71-344">การสมัครสมาชิก สามารถสร้างสำหรับรายงานที่เชื่อมโยง ที่ใช้พารามิเตอร์ที่ต่อกันเป็นทอด</span><span class="sxs-lookup"><span data-stu-id="5ad71-344">Subscriptions can be created for linked reports that use cascading parameters</span></span>
                - <span data-ttu-id="5ad71-345">ค่าเริ่มต้นของพารามิเตอร์หลายค่า สามารถเปลี่ยนแปลงได้เมื่อใช้ IE11</span><span class="sxs-lookup"><span data-stu-id="5ad71-345">Multi-value parameter defaults can be modified when using IE11</span></span>
                - <span data-ttu-id="5ad71-346">ตัวเลือกการจัดส่ง การสมัครสมาชิกแบบให้ข้อมูล สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="5ad71-346">Data-driven subscription delivery options are editable</span></span>
                - <span data-ttu-id="5ad71-347">สามารถดู และแก้ไขการสมัครสมาชิก ในขณะที่กำลังดำเนินการกับสมาชิก</span><span class="sxs-lookup"><span data-stu-id="5ad71-347">Subscriptions can be viewed and edited while the subscription is executing</span></span>
                - <span data-ttu-id="5ad71-348">การตั้งค่าข้อมูลประจำตัวของแหล่งข้อมูล ไม่นำสตริงการเชื่อมต่อตามนิพจน์ออก</span><span class="sxs-lookup"><span data-stu-id="5ad71-348">Setting data source credentials does not remove expression-based connection strings</span></span>
            - <span data-ttu-id="5ad71-349">สำหรับ KPI</span><span class="sxs-lookup"><span data-stu-id="5ad71-349">For KPIs</span></span>
                - <span data-ttu-id="5ad71-350">เส้นแนวโน้มจะรีเฟรชเมื่อข้อมูลจะได้รับการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="5ad71-350">Trend lines are refreshed when data is updated</span></span>
            - <span data-ttu-id="5ad71-351">การปรับปรุงเสถียรภาพทั่วไป</span><span class="sxs-lookup"><span data-stu-id="5ad71-351">General stability improvements</span></span>

    - <span data-ttu-id="5ad71-352">*เวอร์ชัน 1.2.6660.39920 (รุ่น 15.0.2.389), เผยแพร่: 28 มีนาคม 2018*</span><span class="sxs-lookup"><span data-stu-id="5ad71-352">*Version 1.2.6660.39920 (Build 15.0.2.389), Released: March 28, 2018*</span></span>
        - <span data-ttu-id="5ad71-353">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-353">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-354">สำหรับรายงาน Power BI (PBIX) แก้ไขข้อมูลส่งออกที่ใช้ไม่ได้จากวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="5ad71-354">For Power BI Reports (PBIX), fix for Export Data not working from Power BI Visuals</span></span>
            - <span data-ttu-id="5ad71-355">สำหรับรายงาน Power BI (PBIX) แก้ไขตัวกรอง URL ที่ไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="5ad71-355">For Power BI Reports (PBIX), fix for URL filters not working</span></span>
            - <span data-ttu-id="5ad71-356">สำหรับรายงานที่มีการแบ่งหน้า (RDL) แก้ไขภาพที่ไม่แสดงผลอย่างถูกต้องใน IE11 หลังจากอัปเกรดเป็นเซิร์ฟเวอร์รายงาน Power BI รุ่นเดือนมีนาคม</span><span class="sxs-lookup"><span data-stu-id="5ad71-356">For Paginated Reports (RDL), fix for images not being displayed correctly in IE11 after upgrading to Power BI Report Server March release</span></span>

    - <span data-ttu-id="5ad71-357">*เวอร์ชัน 1.2.6648.38132 (รุ่น 15.0.2.378), เผยแพร่: 19 มีนาคม 2018*</span><span class="sxs-lookup"><span data-stu-id="5ad71-357">*Version 1.2.6648.38132 (Build 15.0.2.378), Released: March 19, 2018*</span></span>
        - <span data-ttu-id="5ad71-358">ปรับปรุงความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="5ad71-358">Security Updates</span></span>
        - <span data-ttu-id="5ad71-359">การปรับปรุงการช่วยสำหรับการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="5ad71-359">Accessibility Improvements</span></span>
        - <span data-ttu-id="5ad71-360">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-360">Bug fixes</span></span>
            - <span data-ttu-id="5ad71-361">สำหรับรายงานที่มีการแบ่งหน้า (RDL) แก้ไขการมองเห็นพารามิเตอร์ในรายงานที่เชื่อมโยง ที่มีการแปลงกลับหลังจากแก้ไขคุณสมบัติของรายงาน</span><span class="sxs-lookup"><span data-stu-id="5ad71-361">For Paginated Reports (RDL), fix for parameters visibility in a linked report that is reverted after editing its properties</span></span>
            - <span data-ttu-id="5ad71-362">แก้ไขปัญหาพอร์ทัลของเว็บ ที่มีการรับรองความถูกต้องของฟอร์มแบบกำหนดเอง ที่ละเลยคุกกี้หมดอายุแบบ sliding</span><span class="sxs-lookup"><span data-stu-id="5ad71-362">Fix for web portal with custom forms authentication that is ignoring the sliding expiration cookie</span></span>
            - <span data-ttu-id="5ad71-363">แก้ไขการส่งออกไปยัง Word ที่สร้างแถวที่มีความสูงไม่เท่ากัน ถ้าเนื้อหาของแถวว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="5ad71-363">Fix for export to Word that creates unequal row height if row content is empty</span></span>
            - <span data-ttu-id="5ad71-364">สำหรับรายงานที่มีการแบ่งหน้า (RDL) แก้ไขสตริงการเชื่อมต่อจากนิพจน์ถูกลบ เมื่อเราเปลี่ยนแปลงข้อมูลประจำตัวสำหรับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5ad71-364">For Paginated Reports (RDL), fix for expression-based connection string that is deleted when we change credential for data source</span></span>
            - <span data-ttu-id="5ad71-365">แก้ไขความสามารถในการใช้ KPI กับค่าที่เป็นข้อความ</span><span class="sxs-lookup"><span data-stu-id="5ad71-365">Fix for ability to use KPI with text values</span></span>
            - <span data-ttu-id="5ad71-366">สำหรับรายงานที่มีการแบ่งหน้า (RDL) แก้ไขความสามารถในการกำหนดชุดข้อมูลใหม่ ให้กับรายงานที่มีการแบ่งหน้า (RDL) ที่มีอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="5ad71-366">For Paginated Reports (RDL), fix for ability to assign a new dataset to an existing Paginated Report (RDL)</span></span>
            - <span data-ttu-id="5ad71-367">แก้ไขความเสถียรและปรับปรุงให้ใช้งานให้ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="5ad71-367">Other stability and usability fixes</span></span>

- <span data-ttu-id="5ad71-368">**Power BI Desktop (ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI)**</span><span class="sxs-lookup"><span data-stu-id="5ad71-368">**Power BI Desktop (optimized for Power BI Report Server)**</span></span>
    - <span data-ttu-id="5ad71-369">รุ่น: 2.56.5023.1043 การเผยแพร่ใน (เดือนมีนาคม 2018) 19 มีนาคม 2018</span><span class="sxs-lookup"><span data-stu-id="5ad71-369">Version: 2.56.5023.1043 (March 2018), Released: March 19, 2018</span></span>
        - <span data-ttu-id="5ad71-370">ประกอบด้วยการเปลี่ยนแปลงที่จำเป็นสำหรับการเชื่อมต่อกับ เซิร์ฟเวอร์รายงาน Power BI (มีนาคม 2018)</span><span class="sxs-lookup"><span data-stu-id="5ad71-370">Contains changes required for connection with Power BI Report Server (March 2018)</span></span>

## <a name="october-2017"></a><span data-ttu-id="5ad71-371">ตุลาคม 2017</span><span class="sxs-lookup"><span data-stu-id="5ad71-371">October 2017</span></span>

- <span data-ttu-id="5ad71-372">**เซิร์ฟเวอร์รายงาน Power BI**</span><span class="sxs-lookup"><span data-stu-id="5ad71-372">**Power BI Report Server**</span></span>
    - <span data-ttu-id="5ad71-373">*เวอร์ชัน 1.1.6582.41691 (รุ่น 14.0.600.442), เผยแพร่: 10 มกราคม 2018*</span><span class="sxs-lookup"><span data-stu-id="5ad71-373">*Version 1.1.6582.41691 (Build 14.0.600.442), Released: January 10, 2018*</span></span>
        - <span data-ttu-id="5ad71-374">ปรับปรุงความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="5ad71-374">Security Updates</span></span>
        - <span data-ttu-id="5ad71-375">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-375">Bug Fixes</span></span>
            - <span data-ttu-id="5ad71-376">แก้ไขปัญหา Model.GetParameters ที่ส่งค่า 400 กลับมา</span><span class="sxs-lookup"><span data-stu-id="5ad71-376">Fix for Model.GetParameters returning 400</span></span>
            - <span data-ttu-id="5ad71-377">แก้ไขการตั้งค่าชุดข้อมูลที่แชร์ ให้กับรายงานที่มีการแบ่งหน้า (RDL) ที่มีอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="5ad71-377">Fix for setting shared data set to existing Paginated Reports (RDL)</span></span>
            - <span data-ttu-id="5ad71-378">แก้ไขปัญหา ExecutionNotFoundException เมื่อส่งออกรายงานที่มีค่าพารามิเตอร์ต่างจากของ PDF</span><span class="sxs-lookup"><span data-stu-id="5ad71-378">Fix for ExecutionNotFoundException when exporting report with different parameter values to PDF</span></span>

    - <span data-ttu-id="5ad71-379">*เวอร์ชัน 1.1.6551.5155 (รุ่น 14.0.600.438), เผยแพร่: 11 ธันวาคม 2017*</span><span class="sxs-lookup"><span data-stu-id="5ad71-379">*Version 1.1.6551.5155 (Build 14.0.600.438), Released: December 11, 2017*</span></span>
        - <span data-ttu-id="5ad71-380">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-380">Bug Fixes</span></span>
            - <span data-ttu-id="5ad71-381">ความล้มเหลวในการบันทึกข้อมูล หลังการรีเฟรชรายงาน Power BI Desktop บางรายงาน</span><span class="sxs-lookup"><span data-stu-id="5ad71-381">Failure to save data after refreshing for certain Power BI Desktop reports.</span></span>

    - <span data-ttu-id="5ad71-382">*เวอร์ชัน 1.1.6530.30789 (รุ่น 14.0.600.437), เผยแพร่: 17 พฤศจิกายน 2017*</span><span class="sxs-lookup"><span data-stu-id="5ad71-382">*Version 1.1.6530.30789 (Build 14.0.600.437), Released: November 17, 2017*</span></span>
        - <span data-ttu-id="5ad71-383">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-383">Bug Fixes</span></span>
            - <span data-ttu-id="5ad71-384">แก้ไขการรับรองความถูกต้องในสถานการณ์พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="5ad71-384">Fix for Basic Authentication Scenarios</span></span> 
            - <span data-ttu-id="5ad71-385">แก้ไขปัญหาเลือกวันทำงานไม่ได้ จากหน้ากำหนดเวลาสำหรับ การสมัครใช้งาน แผนการรีเฟรชแคช และสแนปช็อตประวัติบนพอร์ทัล</span><span class="sxs-lookup"><span data-stu-id="5ad71-385">Fix for weekdays were not selectable on schedule page for Subscriptions, Cache Refresh Plans and History Snapshots on Portal</span></span>
            - <span data-ttu-id="5ad71-386">สำหรับรายงานที่มีการแบ่งหน้า (RDL) แก้ไขปัญหานิพจน์ในกล่องข้อความที่มีคุณสมบัติ CanGrow เป็นเท็จ ทำให้ไม่แสดงสีและฟอนต์ของค่าที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-386">For Paginated Reports (RDL), fix for having expressions in Textbox with CanGrow property set to false is resulting in values not showing colors and fonts not being proper</span></span>
            - <span data-ttu-id="5ad71-387">สำหรับรายงาน Power BI (PBIX) แก้ไขการเพิ่มคำอธิบายแผนภูมิให้แผนภูมิเส้น ทำให้วิชวลเป็นภาพว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="5ad71-387">For Power BI Reports (PBIX), fix for adding Legends to line chart renders an empty visual</span></span>

    - <span data-ttu-id="5ad71-388">*เวอร์ชัน 1.1.6514.9163 (รุ่น 14.0.600.434), เผยแพร่: 1 พฤศจิกายน 2017*</span><span class="sxs-lookup"><span data-stu-id="5ad71-388">*Version 1.1.6514.9163 (Build 14.0.600.434), Released: November 1, 2017*</span></span>
        - <span data-ttu-id="5ad71-389">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-389">Bug Fixes</span></span>
            - <span data-ttu-id="5ad71-390">แก้ไขปัญหาความน่าเชื่อถือการอัปโหลดสำหรับรายงาน PBIX ที่ขนาดใหญ่กว่า 500 MB</span><span class="sxs-lookup"><span data-stu-id="5ad71-390">Fix for upload reliability problems for PBIX reports over 500 MB</span></span>
            - <span data-ttu-id="5ad71-391">แก้ไขปัญหาการโหลดข้อมูลสำหรับรายงาน PBIX ที่ขนาดใหญ่กว่า 1 GB</span><span class="sxs-lookup"><span data-stu-id="5ad71-391">Fix for data loading issue for PBIX reports over 1 GB</span></span>

    - <span data-ttu-id="5ad71-392">*เวอร์ชัน 1.1.6513.3500 (รุ่น 14.0.600.433), เผยแพร่: 31 ตุลาคม 2017*</span><span class="sxs-lookup"><span data-stu-id="5ad71-392">*Version 1.1.6513.3500 (Build 14.0.600.433), Released: October 31, 2017*</span></span>
        - <span data-ttu-id="5ad71-393">คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="5ad71-393">Features</span></span>
            - <span data-ttu-id="5ad71-394">สนับสนุนรูปแบบข้อมูลแบบฝังตัว</span><span class="sxs-lookup"><span data-stu-id="5ad71-394">Embedded Data Model Support</span></span>
            - <span data-ttu-id="5ad71-395">การดูเวิร์กบุ๊ก Excel (ด้วยการเปิดใช้การทำงานร่วมกับ Office Online Server)</span><span class="sxs-lookup"><span data-stu-id="5ad71-395">Excel Workbook Viewing (with Office Online Server integration enabled)</span></span>
            - <span data-ttu-id="5ad71-396">การรีเฟรชข้อมูลตามกำหนดเวลา (PBIX)</span><span class="sxs-lookup"><span data-stu-id="5ad71-396">Scheduled Data Refresh (PBIX)</span></span>
            - <span data-ttu-id="5ad71-397">สนับสนุน Direct Query</span><span class="sxs-lookup"><span data-stu-id="5ad71-397">Direct Query Support</span></span>
            - <span data-ttu-id="5ad71-398">สนับสนุนไฟล์ขนาดใหญ่ (สูงสุด 2 กิกะไบต์)</span><span class="sxs-lookup"><span data-stu-id="5ad71-398">Large File Support (up to 2 GB)</span></span>
            - <span data-ttu-id="5ad71-399">REST API สาธารณะ</span><span class="sxs-lookup"><span data-stu-id="5ad71-399">Public REST API</span></span>
            - <span data-ttu-id="5ad71-400">สนับสนุนการแชร์ชุดข้อมูลใน Power BI Desktop (ผ่าน oData)</span><span class="sxs-lookup"><span data-stu-id="5ad71-400">Shared Dataset support in Power BI Desktop (via oData)</span></span>
            - <span data-ttu-id="5ad71-401">สนับสนุนพารามิเตอร์ URL สำหรับไฟล์ PBIX</span><span class="sxs-lookup"><span data-stu-id="5ad71-401">URL Parameter Support for PBIX files</span></span>
            - <span data-ttu-id="5ad71-402">การปรับปรุงการช่วยสำหรับการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="5ad71-402">Accessibility improvements</span></span>

- <span data-ttu-id="5ad71-403">**Power BI Desktop (ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI)**</span><span class="sxs-lookup"><span data-stu-id="5ad71-403">**Power BI Desktop (optimized for Power BI Report Server)**</span></span>
    - <span data-ttu-id="5ad71-404">*เวอร์ชัน: 2.51.4885.3981 การเผยแพร่ในเดือนตุลาคม 2017: 10 เมษายน 2018*</span><span class="sxs-lookup"><span data-stu-id="5ad71-404">*Version: 2.51.4885.3981 (October 2017), Released: April 10, 2018*</span></span>
        - <span data-ttu-id="5ad71-405">ปรับปรุงความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="5ad71-405">Security Updates</span></span>

    - <span data-ttu-id="5ad71-406">*เวอร์ชัน: 2.51.4885.2501 การเผยแพร่ในเดือนตุลาคม 2017: 10 มกราคม 2018*</span><span class="sxs-lookup"><span data-stu-id="5ad71-406">*Version: 2.51.4885.2501 (October 2017), Released: January 10, 2018*</span></span>
        - <span data-ttu-id="5ad71-407">ปรับปรุงความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="5ad71-407">Security Updates</span></span>

    - <span data-ttu-id="5ad71-408">*เวอร์ชัน: 2.51.4885.1423 การเผยแพร่ในเดือนตุลาคม 2017: 17 พฤศจิกายน 2017*</span><span class="sxs-lookup"><span data-stu-id="5ad71-408">*Version: 2.51.4885.1423 (October 2017), Released: November 17, 2017*</span></span>
        - <span data-ttu-id="5ad71-409">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-409">Bug Fixes</span></span>
            - <span data-ttu-id="5ad71-410">แก้ไขปัญหา Power BI Desktop เวอร์ชัน 32 บิต ไม่สามารถเรียกใช้งานบน x86 OS</span><span class="sxs-lookup"><span data-stu-id="5ad71-410">Fix for 32-bit Power BI Desktop failing to run on x86 OS</span></span>
            - <span data-ttu-id="5ad71-411">สำหรับรายงาน Power BI (PBIX) แก้ไขเพื่อแสดงเส้นตารางบนแกน X</span><span class="sxs-lookup"><span data-stu-id="5ad71-411">For Power BI Reports (PBIX), fix to show x-axis gridlines</span></span>
            - <span data-ttu-id="5ad71-412">แก้ไขข้อบกพร่องเล็ก ๆ อื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="5ad71-412">Other minor bug fixes</span></span>

    - <span data-ttu-id="5ad71-413">*เวอร์ชัน: 2.51.4885.1041 การเผยแพร่ในเดือนตุลาคม 2017: 31 ตุลาคม 2017*</span><span class="sxs-lookup"><span data-stu-id="5ad71-413">*Version: 2.51.4885.1041 (October 2017), Released: October 31, 2017*</span></span>
        - <span data-ttu-id="5ad71-414">คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="5ad71-414">Features</span></span>
            - <span data-ttu-id="5ad71-415">ประกอบด้วยการเปลี่ยนแปลงที่จำเป็นสำหรับการเชื่อมต่อกับเซิร์ฟเวอร์รายงาน Power BI (ตุลาคม 2017)</span><span class="sxs-lookup"><span data-stu-id="5ad71-415">Contains changes required for connection with Power BI Report Server (October 2017)</span></span>

## <a name="june-2017"></a><span data-ttu-id="5ad71-416">มิถุนายน ค.ศ. 2017</span><span class="sxs-lookup"><span data-stu-id="5ad71-416">June 2017</span></span>

- <span data-ttu-id="5ad71-417">**เซิร์ฟเวอร์รายงาน Power BI**</span><span class="sxs-lookup"><span data-stu-id="5ad71-417">**Power BI Report Server**</span></span>
    - <span data-ttu-id="5ad71-418">*รุ่น 14.0.600.309 เผยแพร่: 10 มกราคม 2018*</span><span class="sxs-lookup"><span data-stu-id="5ad71-418">*Build 14.0.600.309, Released: January 10, 2018*</span></span>
        - <span data-ttu-id="5ad71-419">ปรับปรุงความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="5ad71-419">Security Updates</span></span>

    - <span data-ttu-id="5ad71-420">*รุ่น 14.0.600.305 เผยแพร่: 19 กันยายน 2017*</span><span class="sxs-lookup"><span data-stu-id="5ad71-420">*Build 14.0.600.305, Released: September 19, 2017*</span></span>  
        - <span data-ttu-id="5ad71-421">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-421">Bug Fixes</span></span>
            - <span data-ttu-id="5ad71-422">ปรับปรุง [Bing Maps Web Control](/bingmaps/v8-web-control/) ให้เป็นรุ่นล่าสุด</span><span class="sxs-lookup"><span data-stu-id="5ad71-422">Update to the latest [Bing Maps Web Control](/bingmaps/v8-web-control/)</span></span>

    - <span data-ttu-id="5ad71-423">*รุ่น 14.0.600.301,เผยแพร่: 11 กรกฎาคม 2017*</span><span class="sxs-lookup"><span data-stu-id="5ad71-423">*Build 14.0.600.301, Released: July 11, 2017*</span></span>
        - <span data-ttu-id="5ad71-424">แก้ไขข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="5ad71-424">Bug Fixes</span></span>
            - <span data-ttu-id="5ad71-425">แท็ก `{{UserId}}` ถูกแปลงเป็นข้อมูลประจำตัวที่เก็บไว้ แทนที่จะเป็นผู้ใช้ ที่ดำเนินการรายงานในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ad71-425">The `{{UserId}}` tag resolves to the stored credentials instead of the user executing the report in Power BI Reports</span></span>
            - <span data-ttu-id="5ad71-426">รูปภาพบางภาพไม่แสดงในรายงานในเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ad71-426">Some images fail to render in Power BI Report Server reports</span></span>
            - <span data-ttu-id="5ad71-427">ไม่สามารถเปลี่ยนชื่อของรายงาน Power BI ในเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ad71-427">Unable to change the name of a Power BI Report in the Power BI Report Server</span></span>
            - <span data-ttu-id="5ad71-428">ไม่สามารถโหลดวิชวล Power BI ในแอปพลิเคชันสำหรับอุปกรณ์เคลื่อนที่ของ Power BI (จำเป็นต้องติดตั้งแอปสำหรับอุปกรณ์เคลื่อนที่ใหม่เพื่อล้างแคชภายในเครื่อง)</span><span class="sxs-lookup"><span data-stu-id="5ad71-428">Unable to load Power BI visuals in the Power BI mobile application (it requires reinstall of the mobile app to clear up the local cache)</span></span>

    - <span data-ttu-id="5ad71-429">*รุ่น 14.0.600.271 เผยแพร่เมื่อ: 12 มิถุนายน 2017*</span><span class="sxs-lookup"><span data-stu-id="5ad71-429">*Build 14.0.600.271, Released: June 12, 2017*</span></span>
        - <span data-ttu-id="5ad71-430">การเผยแพร่ครั้งแรกของเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ad71-430">Power BI Report Server initial release</span></span>

- <span data-ttu-id="5ad71-431">**Power BI Desktop (ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI)**</span><span class="sxs-lookup"><span data-stu-id="5ad71-431">**Power BI Desktop (optimized for Power BI Report Server)**</span></span>
    - <span data-ttu-id="5ad71-432">*เวอร์ชัน: 2.47.4766.4901 (2017 มิถุนายน), เผยแพร่: 10 มกราคม 2018*</span><span class="sxs-lookup"><span data-stu-id="5ad71-432">*Version: 2.47.4766.4901 (June 2017), Released: January 10, 2018*</span></span>
        - <span data-ttu-id="5ad71-433">ปรับปรุงความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="5ad71-433">Security Updates</span></span>

## <a name="next-steps"></a><span data-ttu-id="5ad71-434">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="5ad71-434">Next steps</span></span>

<span data-ttu-id="5ad71-435">[เซิร์ฟเวอร์รายงาน Power BI คืออะไร](get-started.md)
[ภาพรวมของผู้ดูแลระบบ](admin-handbook-overview.md)</span><span class="sxs-lookup"><span data-stu-id="5ad71-435">[What is Power BI Report Server?](get-started.md)
[Administrator overview](admin-handbook-overview.md)</span></span>  
[<span data-ttu-id="5ad71-436">ติดตั้ง Power BI Report Server</span><span class="sxs-lookup"><span data-stu-id="5ad71-436">Install Power BI Report Server</span></span>](install-report-server.md)  
[<span data-ttu-id="5ad71-437">ดาวน์โหลดตัวสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="5ad71-437">Download Report Builder</span></span>](https://www.microsoft.com/download/details.aspx?id=53613)  
[<span data-ttu-id="5ad71-438">ดาวน์โหลด SQL Server Data Tools (SSDT)</span><span class="sxs-lookup"><span data-stu-id="5ad71-438">Download SQL Server Data Tools (SSDT)</span></span>](/sql/ssdt/download-sql-server-data-tools-ssdt)

<span data-ttu-id="5ad71-439">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="5ad71-439">More questions?</span></span> [<span data-ttu-id="5ad71-440">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ad71-440">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
