---
title: Power BI สำหรับ HoloLens 2 (ตัวอย่าง)
description: ดูแดชบอร์ดและรายงานของคุณในแอป Power BI สำหรับ HoloLens 2
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: conceptual
ms.date: 09/22/2020
ms.openlocfilehash: dffe3344fc10b0daceca629b5d5354f1b8419e81
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414541"
---
# <a name="power-bi-for-hololens-2-preview"></a><span data-ttu-id="35adc-103">Power BI สำหรับ HoloLens 2 (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="35adc-103">Power BI for HoloLens 2 (preview)</span></span>
<span data-ttu-id="35adc-104">แอป Power BI สำหรับ HoloLens 2 จะผสมผสานรายงานและแดชบอร์ด Power BI ของคุณเข้ากับสภาพแวดล้อมในโลกจริงของคุณเพื่อสร้างประสบการณ์แบบ 3D ที่ล้ำลึกและเป็นระบบแฮนด์ฟรี โดยที่คุณสามารถเคลื่อนที่ผ่านโลกจริงและสามารถรับข้อมูลที่จำเป็นในสถานที่และในเวลาที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="35adc-104">The Power BI app for HoloLens 2 blends your Power BI reports and dashboards with your physical environment to create a 3D, immersive, hands-free experience where you can move through the physical world and get your relevant data when and where you need it.</span></span>

![ภาพจาก HoloLens 2 แสดงให้เห็นรายงาน Power BI ที่กำลังลอยตัว](media/mobile-hololens2-app/power-bi-hololens2-floating-reports.png)

## <a name="get-the-power-bi-app-for-hololens-2"></a><span data-ttu-id="35adc-106">รับแอป Power BI สำหรับ HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="35adc-106">Get the Power BI app for HoloLens 2</span></span> 

<span data-ttu-id="35adc-107">แอป Power BI สำหรับ HoloLens 2 จะพร้อมใช้งานจาก [Microsoft Store](https://go.microsoft.com/fwlink/?linkid=526478)</span><span class="sxs-lookup"><span data-stu-id="35adc-107">The Power BI app for HoloLens 2 is available from the [Microsoft Store](https://go.microsoft.com/fwlink/?linkid=526478).</span></span>

<span data-ttu-id="35adc-108">แอปทำงานร่วมกับการลงชื่อเพียงครั้งเดียว ซึ่งหมายความว่าแอปใช้ข้อมูลประจำตัวของผู้ใช้ที่ลงชื่อเข้าใช้อุปกรณ์ HoloLens 2 เพื่อรับรองความถูกต้องเทียบกับบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="35adc-108">The app works with single sign on, meaning that the app uses the identity of the user currently signed in to the HoloLens 2 device to authenticate against the Power BI service.</span></span>

<span data-ttu-id="35adc-109">[เรียนรู้เพิ่มเติม](/hololens/holographic-store-apps) เกี่ยวกับการติดตั้งแอปบนอุปกรณ์ HoloLens 2 ของคุณ</span><span class="sxs-lookup"><span data-stu-id="35adc-109">[Learn more](/hololens/holographic-store-apps) about installing apps on your HoloLens 2 device.</span></span>

## <a name="open-the-power-bi-app-on-your-hololens-2"></a><span data-ttu-id="35adc-110">เปิดแอป Power BI บน HoloLens 2 ของคุณ</span><span class="sxs-lookup"><span data-stu-id="35adc-110">Open the Power BI app on your HoloLens 2</span></span>

<span data-ttu-id="35adc-111">เปิดเมนู **เริ่ม** และเลือกแอป Power BI</span><span class="sxs-lookup"><span data-stu-id="35adc-111">Open the **Start** menu and select the Power BI app.</span></span> <span data-ttu-id="35adc-112">แอปจะเปิดขึ้นโดยมีรายงานและแดชบอร์ดที่ชื่นชอบของคุณทั้งหมดที่โหลดลงในชุดเครื่องมือเสมือนของคุณไว้แล้ว ซึ่งคุณสามารถเลือกดู</span><span class="sxs-lookup"><span data-stu-id="35adc-112">The app will open with all your favorited reports and dashboards loaded into your virtual toolbelt, where you can select them for viewing.</span></span>

## <a name="using-the-power-bi-app-for-hololens-2"></a><span data-ttu-id="35adc-113">การใช้แอป Power BI สำหรับ HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="35adc-113">Using the Power BI app for HoloLens 2</span></span>

<span data-ttu-id="35adc-114">คุณสามารถใช้ระบบสัญญาณมือและการจับทิศทางดวงตาของ HoloLens 2 เพื่อปรับขนาด วาง และโต้ตอบกับเนื้อหา Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="35adc-114">You use the HoloLens 2 hand gestures and eye tracking to resize, place, and interact with your Power BI content.</span></span> <span data-ttu-id="35adc-115">[เรียนรู้เพิ่มเติม](/hololens/hololens2-basic-usage) เกี่ยวกับการโต้ตอบกับวัตถุในโลกของ HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="35adc-115">[Learn more](/hololens/hololens2-basic-usage) about interacting with objects in the HoloLens 2 world.</span></span>

### <a name="access-reports-and-dashboards"></a><span data-ttu-id="35adc-116">เข้าถึงรายงานและแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="35adc-116">Access reports and dashboards</span></span>

<span data-ttu-id="35adc-117">หากต้องการเข้าถึงรายงานหรือแดชบอร์ด ให้ดึงข้อมูลออกจากชุดเครื่องมือเสมือนของคุณและวางไว้ในตำแหน่งตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="35adc-117">To access a report or dashboard, grab it out of your virtual toolbelt and position it where you want.</span></span> <span data-ttu-id="35adc-118">[เรียนรู้เพิ่มเติม](/hololens/hololens2-basic-usage#moving-holograms) เกี่ยวกับหยิบและการจัดตำแหน่งหน้าต่างแอป</span><span class="sxs-lookup"><span data-stu-id="35adc-118">[Learn more](/hololens/hololens2-basic-usage#moving-holograms) about grabbing and positioning app windows.</span></span>

<span data-ttu-id="35adc-119">ต้องปรับรายงานหรือแดชบอร์ดให้เป็นรายการโปรดจึงจะอยู่ในชุดเครื่องมือเสมือนของคุณ</span><span class="sxs-lookup"><span data-stu-id="35adc-119">To be in your virtual toolbelt, a report or dashboard must be marked as a favorite.</span></span> <span data-ttu-id="35adc-120">ถ้าคุณไม่มีรายงานหรือแดชบอร์ดใด ๆ ในชุดเครื่องมือของคุณ หรือหากคุณต้องการเพิ่มรายงานและแดชบอร์ด เพียงแค่ทำเครื่องหมายรายการเหล่านั้นให้เป็นรายการโปรดใน [Power BI service](../end-user-favorite.md) หรือ [Power BI mobile apps](mobile-apps-favorites.md)</span><span class="sxs-lookup"><span data-stu-id="35adc-120">If you don’t have any reports or dashboards in your toolbelt, or if you want to add additional reports and dashboards, simply mark those items as favorites in either the [Power BI service](../end-user-favorite.md) or the [Power BI mobile apps](mobile-apps-favorites.md).</span></span> <span data-ttu-id="35adc-121">ซึ่งจากนั้นจะพร้อมใช้งานในชุดเครื่องมือเสมือนของ Power BI ของคุณใน HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="35adc-121">They will then be available in your Power BI virtual toolbelt in HoloLens 2.</span></span>

### <a name="resize-reports-and-dashboards"></a><span data-ttu-id="35adc-122">ปรับขนาดรายงานและแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="35adc-122">Resize reports and dashboards</span></span>

<span data-ttu-id="35adc-123">หากต้องการปรับขนาดรายงานหรือแดชบอร์ด ให้หยิบข้อมูลด้วยจุดจับปรับขนาดที่ปรากฏบนมุมของหน้าต่างแอปและปรับขนาดตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="35adc-123">To resize a report or dashboard, grab it by the resize handles that appear on the corners of the app window and adjust the size as desired.</span></span> <span data-ttu-id="35adc-124">[เรียนรู้เพิ่มเติม](/hololens/hololens2-basic-usage#resizing-holograms) เกี่ยวกับการปรับขนาดหน้าต่างของแอป</span><span class="sxs-lookup"><span data-stu-id="35adc-124">[Learn more](/hololens/hololens2-basic-usage#resizing-holograms) about resizing app windows.</span></span>

### <a name="position-reports-and-dashboards-in-space"></a><span data-ttu-id="35adc-125">จัดตำแหน่งรายงานและแดชบอร์ดในพื้นที่</span><span class="sxs-lookup"><span data-stu-id="35adc-125">Position reports and dashboards in space</span></span>

<span data-ttu-id="35adc-126">เมื่อต้องการจัดตำแหน่งรายงานหรือแดชบอร์ดของคุณในพื้นที่ ให้หยิบข้อมูลด้วยการบีบนิ้วชี้และนิ้วโป้งของคุณเข้าหาแถบชื่อเรื่องค้างไว้ และจากนั้นให้ย้ายมือของคุณไปยังตำแหน่งที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="35adc-126">To position your report or dashboard in space, grab it by pinching your index finger and thumb on its title bar and then, without letting go, move your hand to the desired position.</span></span> <span data-ttu-id="35adc-127">ปล่อยนิ้วของคุณเมื่อคุณได้ตำแหน่งที่ต้องการแล้ว</span><span class="sxs-lookup"><span data-stu-id="35adc-127">Release your fingers when you’ve got it to the desired place.</span></span> <span data-ttu-id="35adc-128">[เรียนรู้เพิ่มเติม](/hololens/hololens2-basic-usage#moving-holograms) เกี่ยวกับการย้ายหน้าต่างของแอป</span><span class="sxs-lookup"><span data-stu-id="35adc-128">[Learn more](/hololens/hololens2-basic-usage#moving-holograms) about moving app windows.</span></span>

<span data-ttu-id="35adc-129">เมื่อคุณวางรายงานหรือแดชบอร์ดของคุณในตำแหน่งที่คุณต้องการแล้ว อุปกรณ์ HoloLens 2 ของคุณจะจดจำตำแหน่งที่ตั้งนี้ในสภาพแวดล้อมนั้น</span><span class="sxs-lookup"><span data-stu-id="35adc-129">Once you’ve placed your report or dashboard where you want it, your HoloLens 2 device remembers its location in the environment.</span></span> <span data-ttu-id="35adc-130">เมื่อคุณเข้าสู่สถานที่นี้อีกครั้ง คุณจะพบว่าไฟล์ที่คุณวางไว้อยู่ในตำแหน่งเดิม</span><span class="sxs-lookup"><span data-stu-id="35adc-130">When you next visit the same place, you’ll find the item you placed in exactly the same location.</span></span>

### <a name="browse-report-pages"></a><span data-ttu-id="35adc-131">ค้นหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="35adc-131">Browse report pages</span></span>

<span data-ttu-id="35adc-132">แต่ละรายงานจะมีดัชนีหน้า ซึ่งคุณสามารถแสดงเพื่อให้สามารถข้ามจากหน้าหนึ่งไปยังอีกหน้าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="35adc-132">Each report has a page index that you can display in order to get from page to page.</span></span> <span data-ttu-id="35adc-133">เลือกปุ่ม **ดัชนีหน้า** ในมุมบนขวาของหน้าต่างรายงานเพื่อแสดงหรือซ่อนดัชนีหน้า</span><span class="sxs-lookup"><span data-stu-id="35adc-133">Select the **Page Index** button in the upper right corner of the report window to display or hide the page index.</span></span>

![รูปแสดงดัชนีหน้ารายงานใน Power BI สำหรับ HoloLens 2](media/mobile-hololens2-app/power-bi-hololens2-browse-report-pages.png)

### <a name="open-reports-with-qr-codes"></a><span data-ttu-id="35adc-135">เปิดรายงานที่มีรหัส QR</span><span class="sxs-lookup"><span data-stu-id="35adc-135">Open reports with QR codes</span></span>

<span data-ttu-id="35adc-136">ถ้ามีการสร้างคิวอาร์โค้ดสำหรับรายงานและติดไว้กับสิ่งของอย่างใดอย่างหนึ่ง เช่น ชิ้นส่วนของอุปกรณ์ที่มีข้อมูลอยู่ในรายงานนั้น คุณสามารถเปิดรายงานได้เพียงแค่มองดูที่คิวอาร์โค้ดบนรายการ</span><span class="sxs-lookup"><span data-stu-id="35adc-136">If a QR code has been created for a report and attached to an item, such as a piece of equipment whose data is contained in that report, you can open the report merely by looking at the QR code on the item.</span></span>

<span data-ttu-id="35adc-137">[เรียนรู้เพิ่มเติม](../../create-reports/service-create-qr-code-for-report.md) เกี่ยวกับการสร้างคิวอาร์โค้ดสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="35adc-137">[Learn more](../../create-reports/service-create-qr-code-for-report.md) about creating QR codes for reports.</span></span>

### <a name="data-refresh"></a><span data-ttu-id="35adc-138">การรีเฟรชข้อมูล</span><span class="sxs-lookup"><span data-stu-id="35adc-138">Data refresh</span></span>

<span data-ttu-id="35adc-139">รายงานและแดชบอร์ดจะทำการอัปเดตในขณะที่คุณกำลังใช้แอป ดังนั้นถ้ามีการเปลี่ยนแปลงข้อมูลใน Power BI ในขณะที่คุณกำลังใช้แอป คุณจะเห็นว่าการเปลี่ยนแปลงเหล่านั้นปรากฏในรายงานและแดชบอร์ดที่คุณกำลังดูอยู่</span><span class="sxs-lookup"><span data-stu-id="35adc-139">Reports and dashboards update while you’re using the app, so if data changes in Power BI while you’re using the app, you’ll see those changes reflected in the reports and dashboards you’re viewing.</span></span>

## <a name="next-steps"></a><span data-ttu-id="35adc-140">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="35adc-140">Next steps</span></span>

* [<span data-ttu-id="35adc-141">ทำความรู้จัก HoloLens 2</span><span class="sxs-lookup"><span data-stu-id="35adc-141">Getting around HoloLens 2</span></span>](/hololens/hololens2-basic-usage)