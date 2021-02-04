---
title: ติดตั้ง Power BI Desktop ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI
description: เรียนรู้วิธีติดตั้ง Power BI Desktop ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.date: 10/16/2020
ms.openlocfilehash: 62add0b1268b06bb227bdc1b8ec2e4ae59358c57
ms.sourcegitcommit: a5fa368abad54feb44a267fe26c383a731c7ec0d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/30/2020
ms.locfileid: "93044743"
---
# <a name="install-power-bi-desktop-optimized-for-power-bi-report-server"></a><span data-ttu-id="92d5b-103">ติดตั้ง Power BI Desktop ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="92d5b-103">Install Power BI Desktop optimized for Power BI Report Server</span></span>

<span data-ttu-id="92d5b-104">เมื่อต้องสร้างรายงาน Power BI สำหรับเซิร์ฟเวอร์รายงาน Power BI คุณจำเป็นต้องดาวน์โหลดและติดตั้ง Power BI Desktop เวอร์ชันที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="92d5b-104">To create Power BI reports for Power BI Report Server, you need to download and install the version of Power BI Desktop that's optimized for Power BI Report Server.</span></span> <span data-ttu-id="92d5b-105">การเผยแพร่นี้จะแตกต่างจาก Power BI Desktop ที่ใช้กับบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="92d5b-105">This release is different from the Power BI Desktop used with the Power BI service.</span></span> <span data-ttu-id="92d5b-106">ตัวอย่างเช่น เวอร์ชันของ Power BI Desktop สำหรับบริการของ Power BI ที่มีคุณลักษณะการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="92d5b-106">For example, the version of Power BI Desktop for the Power BI service includes preview features.</span></span> <span data-ttu-id="92d5b-107">คุณลักษณะเหล่านั้นไม่ได้อยู่ในเวอร์ชัน Power BI Report Server จนกว่าจะพร้อมใช้งานทั่วไป</span><span class="sxs-lookup"><span data-stu-id="92d5b-107">Those features aren't in the Power BI Report Server version until they're generally available.</span></span> <span data-ttu-id="92d5b-108">การใช้การเผยแพรนี้จะทำให้แน่ใจว่า เซิร์ฟเวอร์รายงานสามารถโต้ตอบกับรายงานและแบบจำลองเวอร์ชันที่ทราบแล้วได้</span><span class="sxs-lookup"><span data-stu-id="92d5b-108">Using this release makes sure that the report server can interact with a known version of the reports and model.</span></span> 

<span data-ttu-id="92d5b-109">ไม่ต้องกังวล</span><span class="sxs-lookup"><span data-stu-id="92d5b-109">Not to worry.</span></span> <span data-ttu-id="92d5b-110">เนื่องจากคุณสามารถติดตั้ง Power BI Desktop และ Power BI Desktop ที่ปรับให้เหมาะสมสำหรับ Power BI Report Server ได้โดยควบคู่กันไปบนคอมพิวเตอร์เครื่องเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="92d5b-110">You can install Power BI Desktop, and Power BI Desktop optimized for Power BI Report Server, side by side on the same computer.</span></span>

## <a name="download-and-install-power-bi-desktop"></a><span data-ttu-id="92d5b-111">ดาวน์โหลด และติดตั้ง Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="92d5b-111">Download and install Power BI Desktop</span></span>

<span data-ttu-id="92d5b-112">วิธีที่ง่ายที่สุดเพื่อให้แน่ใจว่าคุณมีเวอร์ชันล่าสุดของ Power BI Desktop ที่ปรับให้เหมาะสมสำหรับเซิร์ฟเวอร์รายงาน Power BI ก็คือ การเริ่มต้นจากพอร์ทัลเว็บของเซิร์ฟเวอร์รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="92d5b-112">The easiest way to be sure you have the most up-to-date version of Power BI Desktop optimized for Power BI Report Server is to start from the web portal of your report server.</span></span>

1. <span data-ttu-id="92d5b-113">ในพอร์ทัลเว็บเซิร์ฟเวอร์รายงาน เลือก **ดาวน์โหลด** ลูกศร > **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="92d5b-113">In the report server web portal, select the **Download** arrow > **Power BI Desktop**.</span></span>

    ![ดาวน์โหลด Power BI Desktop จากพอร์ทัลของเว็บ](media/install-powerbi-desktop/report-server-download-web-portal.png)

    <span data-ttu-id="92d5b-115">หรือไปที่หน้าหลัก [เซิร์ฟเวอร์รายงาน Power BI](https://powerbi.microsoft.com/report-server/) แล้วเลือก **ตัวเลือกการดาวน์โหลดขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="92d5b-115">Or go to the [Power BI Report Server](https://powerbi.microsoft.com/report-server/) home page and select **Advanced download options**.</span></span>

2. <span data-ttu-id="92d5b-116">ในหน้าศูนย์ดาวน์โหลด ให้เลือกภาษา จากนั้นเลือก **ดาวน์โหลด**</span><span class="sxs-lookup"><span data-stu-id="92d5b-116">In the Download Center page, select a language, then select **Download**.</span></span>

3. <span data-ttu-id="92d5b-117">ขึ้นอยู่กับคอมพิวเตอร์ของคุณ เลือก:</span><span class="sxs-lookup"><span data-stu-id="92d5b-117">Depending on your computer, select:</span></span> 

    - <span data-ttu-id="92d5b-118">**PBIDesktopRS.msi** (เวอร์ชัน 32 บิต) หรือ</span><span class="sxs-lookup"><span data-stu-id="92d5b-118">**PBIDesktopRS.msi** (the 32-bit version) or</span></span>
    - <span data-ttu-id="92d5b-119">**PBIDesktopRS_x64.msi** (เวอร์ชัน 64 บิต)</span><span class="sxs-lookup"><span data-stu-id="92d5b-119">**PBIDesktopRS_x64.msi** (the 64-bit version).</span></span>

1. <span data-ttu-id="92d5b-120">หลังจากที่คุณดาวน์โหลดตัวติดตั้งแล้ว เรียกใช้ตัวช่วยสร้างการติดตั้ง Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="92d5b-120">After you download the installer, run the Power BI Desktop Setup Wizard.</span></span>

2. <span data-ttu-id="92d5b-121">ในตอนท้ายของการติดตั้ง เลือก **เรียกใช้ Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="92d5b-121">At the end of the installation, select **Launch Power BI Desktop**.</span></span>

    <span data-ttu-id="92d5b-122">จะเริ่มต้นโดยอัตโนมัติ และคุณก็พร้อมที่จะไปต่อ</span><span class="sxs-lookup"><span data-stu-id="92d5b-122">It starts automatically and you're ready to go.</span></span>

## <a name="verify-youre-using-the-correct-version"></a><span data-ttu-id="92d5b-123">ตรวจสอบว่าคุณกำลังใช้เวอร์ชันที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="92d5b-123">Verify you're using the correct version</span></span>
<span data-ttu-id="92d5b-124">เป็นเรื่องง่ายเมื่อต้องการตรวจสอบว่าคุณกำลังใช้ Power BI Desktop ที่ถูกต้องอยู่: ดูที่เปิดใช้งานหน้าจอหรือแถบชื่อเรื่องภายใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="92d5b-124">It's easy to verify that you're using the correct Power BI Desktop: Look at the launch screen or title bar within Power BI Desktop.</span></span> <span data-ttu-id="92d5b-125">คุณสามารถแจ้งว่าคุณมีเวอร์ชันที่ถูกต้องเนื่องจาก **Power BI Desktop (ตุลาคม 2020)** อยู่ในแถบชื่อ</span><span class="sxs-lookup"><span data-stu-id="92d5b-125">You can tell you have the right version because **Power BI Desktop (October 2020)** is in the title bar.</span></span> <span data-ttu-id="92d5b-126">นอกจากนี้ สีโลโก้ Power BI จะกลับกันโดยสีเหลืองจะอยู่บนพื้นดำแทนที่เป็นสีดำบนพื้นเหลือง</span><span class="sxs-lookup"><span data-stu-id="92d5b-126">Also, the Power BI logo colors are reversed, yellow on black instead of black on yellow.</span></span>

![Power BI Desktop ตุลาคม 2020](media/install-powerbi-desktop/power-bi-report-server-desktop-may-2020.png)

<span data-ttu-id="92d5b-128">เวอร์ชั่น Power BI Desktop สำหรับบริการ Power BI ไม่มีเดือนและปีในแถบรายการชื่อ</span><span class="sxs-lookup"><span data-stu-id="92d5b-128">The version of Power BI Desktop for the Power BI service doesn't have the month and year in the title bar.</span></span>

## <a name="file-extension-association"></a><span data-ttu-id="92d5b-129">การเชื่อมโยงนามสกุลไฟล์</span><span class="sxs-lookup"><span data-stu-id="92d5b-129">File extension association</span></span>
<span data-ttu-id="92d5b-130">เนื่องจากคุณสามารถติดตั้ง Power BI Desktop และ Power BI Desktop ที่ปรับให้เหมาะสมสำหรับ Power BI Report Server ได้โดยควบคู่กันไปบนคอมพิวเตอร์เครื่องเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="92d5b-130">Say you've installed both Power BI Desktop and Power BI Desktop optimized for Power BI Report Server on the same machine.</span></span> <span data-ttu-id="92d5b-131">การติดตั้ง Power BI Desktop ครั้งล่าสุดของคุณมีการเชื่อมโยงไฟล์กับไฟล์ .pbix</span><span class="sxs-lookup"><span data-stu-id="92d5b-131">Your most recent installation of Power BI Desktop has the file association with .pbix files.</span></span> <span data-ttu-id="92d5b-132">ดังนั้นแล้วเมื่อคุณดับเบิลคลิกที่ไฟล ์.pbix ก็จะเปิดใช้ Power BI Desktop ที่คุณได้ทำการติดตั้งล่าสุด</span><span class="sxs-lookup"><span data-stu-id="92d5b-132">Thus, when you double-click a .pbix file, it launches the Power BI Desktop you installed most recently.</span></span>

<span data-ttu-id="92d5b-133">ถ้าคุณมี Power BI Desktop อยู่ แล้วติดตั้ง Power BI Desktop ที่ปรับให้เหมาะสมสำหรับเซิร์ฟเวอร์รายงาน Power BI ไฟล์ pbix ทั้งหมดก็จะเปิดใน Power BI Desktop ที่ปรับให้เหมาะสมสำหรับเซิร์ฟเวอร์รายงาน Power BI ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="92d5b-133">If you have Power BI Desktop and then install Power BI Desktop optimized for Power BI Report Server, all .pbix files open in Power BI Desktop optimized for Power BI Report Server by default.</span></span> <span data-ttu-id="92d5b-134">ถ้าคุณต้องการให้ Power BI Desktop เป็นค่าเริ่มต้นแทนสำหรับเปิดใช้งานเมื่อเปิดไฟล์ .pbix ให้ติดตั้ง [ Power BI Desktop จาก Microsoft Store ใหม่](https://aka.ms/pbidesktopstore)</span><span class="sxs-lookup"><span data-stu-id="92d5b-134">If you would rather have Power BI Desktop be the default to launch when opening a .pbix file, reinstall [Power BI Desktop from the Microsoft Store](https://aka.ms/pbidesktopstore).</span></span>

<span data-ttu-id="92d5b-135">คุณสามารถเปิด Power BI Desktop เวอร์ชันที่คุณต้องการใช้ก่อนได้เสมอ</span><span class="sxs-lookup"><span data-stu-id="92d5b-135">You can always open the version of Power BI Desktop you want to use first.</span></span> <span data-ttu-id="92d5b-136">จากนั้น ให้เปิดไฟล์จากภายใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="92d5b-136">And then open the file from within Power BI Desktop.</span></span>

<span data-ttu-id="92d5b-137">นี่คือวิธีที่ปลอดภัยที่สุดในการเปิด Power BI Desktop เวอร์ชันที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="92d5b-137">Here's the safest way to always open the correct version of Power BI Desktop.</span></span> <span data-ttu-id="92d5b-138">เริ่มต้นการแก้ไขรายงาน Power BI จากภายใน Power BI Report Server หรือสร้างรายงาน Power BI ใหม่จากบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="92d5b-138">Start editing a Power BI report from within Power BI Report Server, or create a new Power BI report from the Power BI service.</span></span>

## <a name="considerations-and-limitations"></a><span data-ttu-id="92d5b-139">ข้อควรพิจารณาและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="92d5b-139">Considerations and limitations</span></span>

<span data-ttu-id="92d5b-140">รายงาน Power BI ในเซิร์ฟเวอร์รายงาน Power BI ในบริการของ Power BI (`https://app.powerbi.com`) และในแอปสำหรับอุปกรณ์เคลื่อนที่ Power BI ทำงานในลักษณะที่ใกล้เคียงกัน  แต่จะมีบางคุณลักษณ์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="92d5b-140">Power BI reports in Power BI Report Server, in the Power BI service (`https://app.powerbi.com`), and in the Power BI mobile apps act almost exactly the same, but a few features are different.</span></span>

### <a name="selecting-a-language"></a><span data-ttu-id="92d5b-141">การเลือกภาษา</span><span class="sxs-lookup"><span data-stu-id="92d5b-141">Selecting a language</span></span>

<span data-ttu-id="92d5b-142">สำหรับการ Power BI Desktop ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI คุณต้องเลือกภาษาเมื่อคุณติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="92d5b-142">For Power BI Desktop optimized for Power BI Report Server, you select the language when you install the app.</span></span> <span data-ttu-id="92d5b-143">ซึ่งหลังจากนี้คุณจะไม่สามารถเปลี่ยนภาษาได้ แต่คุณสามารถติดตั้งเวอร์ชันในภาษาอื่นได้</span><span class="sxs-lookup"><span data-stu-id="92d5b-143">You can't change it after, but you can install a version in another language.</span></span>

### <a name="report-visuals-in-a-browser"></a><span data-ttu-id="92d5b-144">การแสดงภาพรายงานในเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="92d5b-144">Report visuals in a browser</span></span>

<span data-ttu-id="92d5b-145">รายงานของเซิร์ฟเวอร์รายงาน Power BI รองรับส่วนการแสดงผลเกือบทั้งหมด รวมทั้งส่วนวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="92d5b-145">Power BI Report Server reports support almost all visualizations, including Power BI visuals.</span></span> <span data-ttu-id="92d5b-146">รายงานในเซิร์ฟเวอร์รายงาน Power BI ไม่สนับสนุน:</span><span class="sxs-lookup"><span data-stu-id="92d5b-146">Power BI Report Server reports don’t support:</span></span>

* <span data-ttu-id="92d5b-147">วิชวล R</span><span class="sxs-lookup"><span data-stu-id="92d5b-147">R visuals</span></span>
* <span data-ttu-id="92d5b-148">แผนที่ ArcGIS</span><span class="sxs-lookup"><span data-stu-id="92d5b-148">ArcGIS maps</span></span>
* <span data-ttu-id="92d5b-149">การนำทางแบบแสดงเส้นนำทาง</span><span class="sxs-lookup"><span data-stu-id="92d5b-149">Breadcrumbs</span></span>
* <span data-ttu-id="92d5b-150">คุณลักษณะที่เป็นตัวอย่างใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="92d5b-150">Power BI Desktop preview features</span></span>

### <a name="reports-in-the-power-bi-mobile-apps"></a><span data-ttu-id="92d5b-151">รายงานในแอปสำหรับอุปกรณ์เคลื่อนที่ Power BI</span><span class="sxs-lookup"><span data-stu-id="92d5b-151">Reports in the Power BI mobile apps</span></span>

<span data-ttu-id="92d5b-152">รายงานในเซิร์ฟเวอร์รายงาน Power BI สนับสนุนฟังก์ชันพื้นฐานทั้งหมดใน[แอปสำหรับอุปกรณ์เคลื่อนที่ Power BI](../consumer/mobile/mobile-apps-for-mobile-devices.md) รวมถึง:</span><span class="sxs-lookup"><span data-stu-id="92d5b-152">Power BI Report Server reports support all the basic functionality in the [Power BI mobile apps](../consumer/mobile/mobile-apps-for-mobile-devices.md), including:</span></span>

* <span data-ttu-id="92d5b-153">[เค้าโครงรายงานโทรศัพท์](../create-reports/desktop-create-phone-report.md): คุณสามารถปรับรายงานให้เหมาะสมกับแอปสำหรับอุปกรณ์เคลื่อนที่ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="92d5b-153">[Phone report layout](../create-reports/desktop-create-phone-report.md): You can optimize a report for the Power BI mobile apps.</span></span> <span data-ttu-id="92d5b-154">บนโทรศัพท์มือถือของคุณ รายงานที่ปรับให้เหมาะสมมีไอคอนพิเศษ ![ไอคอนเค้าโครงรายงานโทรศัพท์](media/install-powerbi-desktop/power-bi-rs-mobile-optimized-icon.png) และเค้าโครงที่เหมาะกับมือถือ</span><span class="sxs-lookup"><span data-stu-id="92d5b-154">On your mobile phone, optimized reports have a special icon ![Phone report layout icon](media/install-powerbi-desktop/power-bi-rs-mobile-optimized-icon.png), and layout.</span></span>
  
    ![รายงานที่ปรับให้เหมาะสมสำหรับมือถือ](media/install-powerbi-desktop/power-bi-rs-mobile-optimized-report.png)

<span data-ttu-id="92d5b-156">รายงานในเซิร์ฟเวอร์รายงาน Power BI ไม่สนับสนุนคุณลักษณะเหล่านี้ในแอปสำหรับอุปกรณ์เคลื่อนที่ Power BI:</span><span class="sxs-lookup"><span data-stu-id="92d5b-156">Power BI Report Server reports don’t support these features in the Power BI mobile apps:</span></span>

* <span data-ttu-id="92d5b-157">วิชวล R</span><span class="sxs-lookup"><span data-stu-id="92d5b-157">R visuals</span></span>
* <span data-ttu-id="92d5b-158">แผนที่ ArcGIS</span><span class="sxs-lookup"><span data-stu-id="92d5b-158">ArcGIS maps</span></span>
* <span data-ttu-id="92d5b-159">วิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="92d5b-159">Power BI visuals</span></span>
* <span data-ttu-id="92d5b-160">การนำทางแบบแสดงเส้นนำทาง</span><span class="sxs-lookup"><span data-stu-id="92d5b-160">Breadcrumbs</span></span>
* <span data-ttu-id="92d5b-161">การกรองพรมแดนหรือบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="92d5b-161">Geo filtering or bar codes</span></span>

### <a name="custom-security"></a><span data-ttu-id="92d5b-162">การรักษาความปลอดภัยแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="92d5b-162">Custom Security</span></span>

<span data-ttu-id="92d5b-163">Power BI Desktop ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI ไม่รองรับการรักษาความปลอดภัยแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="92d5b-163">Power BI Desktop optimized for Power BI Report Server does not support custom security.</span></span> <span data-ttu-id="92d5b-164">ถ้ามีการกำหนดค่าเซิร์ฟเวอร์รายงาน Power BI ของคุณด้วยส่วนขยายการรักษาความปลอดภัยแบบกำหนดเอง คุณจะไม่สามารถบันทึกรายงาน Power BI จาก Power BI Desktop (ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI) ไปยังอินสแตนซ์เซิร์ฟเวอร์รายงาน Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="92d5b-164">If your Power BI Report Server is configured with a custom security extension, you can't save a Power BI report from Power BI Desktop (optimized for Power BI Report Server) to the Power BI Report Server instance.</span></span> <span data-ttu-id="92d5b-165">คุณจำเป็นต้องบันทึกไฟล์รายงานนามสกุล .pbix จาก Power BI Desktop และอัปโหลดไปยังไซต์พอร์ทัลเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="92d5b-165">You need to save the .pbix report file from Power BI Desktop and upload it to the Power BI Report Server portal site.</span></span>

### <a name="saving-reports-to-a-power-bi-report-server-in-a-different-domain"></a><span data-ttu-id="92d5b-166">การบันทึกรายงานไปยังเซิร์ฟเวอร์รายงาน Power BI ในโดเมนอื่น</span><span class="sxs-lookup"><span data-stu-id="92d5b-166">Saving reports to a Power BI Report Server in a different domain</span></span>

<span data-ttu-id="92d5b-167">เมื่อคุณบันทึกรายงาน Power BI ไปยังเซิร์ฟเวอร์รายงาน Power BI ข้อมูลประจำตัว Windows ของคุณจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="92d5b-167">When you save a Power BI report to Power BI Report Server, your Windows credentials are used.</span></span> <span data-ttu-id="92d5b-168">การบันทึกไปยังเซิร์ฟเวอร์รายงานในโดเมนอื่นโดยตรง ข้อมูลประจำตัว Windows ของคุณ จะไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="92d5b-168">Saving directly to a report server in a different domain to your Windows credentials is not supported.</span></span> <span data-ttu-id="92d5b-169">คุณสามารถใช้เว็บเบราว์เซอร์เพื่อดูเซิร์ฟเวอร์รายงาน และอัปโหลดไฟล์จากเครื่องของคุณแทน</span><span class="sxs-lookup"><span data-stu-id="92d5b-169">You can use a web browser to view the report server and manually upload the file from your machine instead.</span></span>

## <a name="next-steps"></a><span data-ttu-id="92d5b-170">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="92d5b-170">Next steps</span></span>

<span data-ttu-id="92d5b-171">หลังจากที่ติดตั้ง Power BI Desktop แล้ว คุณสามารถเริ่มการสร้างรายงาน Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="92d5b-171">Now that you have Power BI Desktop installed, you can start creating Power BI reports.</span></span>

[<span data-ttu-id="92d5b-172">สร้างรายงาน Power BI สำหรับเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="92d5b-172">Create a Power BI report for Power BI Report Server</span></span>](quickstart-create-powerbi-report.md)  
[<span data-ttu-id="92d5b-173">เซิร์ฟเวอร์รายงาน Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="92d5b-173">What is Power BI Report Server?</span></span>](get-started.md)

<span data-ttu-id="92d5b-174">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="92d5b-174">More questions?</span></span> [<span data-ttu-id="92d5b-175">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="92d5b-175">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)

