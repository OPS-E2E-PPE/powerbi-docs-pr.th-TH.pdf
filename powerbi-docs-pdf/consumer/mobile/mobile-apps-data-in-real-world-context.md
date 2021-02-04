---
title: รับข้อมูลตามโลกความจริง ด้วยแอป Power BI สำหรับโทรศัพท์เคลื่อนที่
description: แอป power BI สำหรับโทรศัพท์เคลื่อนที่สามารถเชื่อมโลกแห่งความจริงเข้ากับข้อมูลที่เกี่ยวข้องกับ BI ได้โดยตรง โดยไม่ต้องใช้การค้นหา
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: conceptual
ms.date: 03/11/2020
ms.openlocfilehash: 5710f70dafbb01aca68cfc03107a1f1ededaf015
ms.sourcegitcommit: 1cad78595cca1175b82c04458803764ac36e5e37
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/19/2021
ms.locfileid: "98565895"
---
# <a name="get-data-from-the-real-world-with-the-power-bi-mobile-apps"></a><span data-ttu-id="f08b8-103">รับข้อมูลจากโลกแห่งความจริงด้วยแอปโทรศัพท์เคลื่อนที่ Power BI</span><span class="sxs-lookup"><span data-stu-id="f08b8-103">Get data from the real world with the Power BI mobile apps</span></span>
<span data-ttu-id="f08b8-104">แอปโทรศัพท์เคลื่อนที่ Power BI สามารถเชื่อมโลกแห่งความจริงเข้ากับข้อมูล BI ที่เกี่ยวข้องได้โดยตรงในหลายวิธีที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="f08b8-104">Power BI mobile apps can connect the real world directly to related BI information, in a number of different ways.</span></span> 

## <a name="qr-codes-for-tiles"></a><span data-ttu-id="f08b8-105">คิวอาร์โค้ดสำหรับไทล์</span><span class="sxs-lookup"><span data-stu-id="f08b8-105">QR codes for tiles</span></span>
<span data-ttu-id="f08b8-106">สร้างคิวอาร์โค้ดสำหรับรายงาน หรือไทล์ในแดชบอร์ด และใส่คิวอาร์โค้ดที่ใดก็ได้คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="f08b8-106">Create a QR code for a report, or a tile in a dashboard, and put the QR code anywhere you want.</span></span> <span data-ttu-id="f08b8-107">เมื่อเพื่อนร่วมงานของคุณสแกนรหัสด้วย iPhones โทรศัพท์ Android หรือ Power BI เพื่อเข้าใช้แอปความเป็นจริงผสม พวกเขาจะเห็นไทล์ที่คุณได้โยงเข้ากับคิวอาร์โค้ดนั้น ๆ</span><span class="sxs-lookup"><span data-stu-id="f08b8-107">When your colleagues scan the code with their iPhones, Android phones, or the Power BI for Mixed Reality app, they see the tile you've associated with that QR code.</span></span> <span data-ttu-id="f08b8-108">บน iPhone พวกเขาเห็นไทล์แบบเทคโนโลยีความเป็นจริงเสริม</span><span class="sxs-lookup"><span data-stu-id="f08b8-108">On an iPhone, they see the tile in augmented reality.</span></span>

![คิวอาร์โค้ด](./media/mobile-apps-data-in-real-world-context/power-bi-ios-qr-ar-scanner-small.png)

<span data-ttu-id="f08b8-110">ข้อมูลเพิ่มเติมเกี่ยวกับ:</span><span class="sxs-lookup"><span data-stu-id="f08b8-110">More about:</span></span>

* [<span data-ttu-id="f08b8-111">การสร้างคิวอาร์โค้ดสำหรับไทล์ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="f08b8-111">Creating a QR code for a tile in Power BI</span></span>](../../create-reports/service-create-qr-code-for-tile.md)
* [<span data-ttu-id="f08b8-112">การสแกนคิวอาร์โค้ดของ Power BI จากอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f08b8-112">Scanning a Power BI QR code from your mobile device</span></span>](mobile-apps-qr-code.md)
* <span data-ttu-id="f08b8-113">[การสแกนคิวอาร์โค้ด ด้วย Power BI สำหรับแอปความเป็นจริงผสม](./mobile-hololens2-app.md#open-reports-with-qr-codes)</span><span class="sxs-lookup"><span data-stu-id="f08b8-113">[Scanning a QR code with the Power BI for Mixed Reality app](./mobile-hololens2-app.md#open-reports-with-qr-codes).</span></span>

## <a name="qr-codes-for-reports"></a><span data-ttu-id="f08b8-114">คิวอาร์โค้ดสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="f08b8-114">QR codes for reports</span></span>
<span data-ttu-id="f08b8-115">สร้างคิวอาร์โค้ดสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="f08b8-115">Create a QR code for a report.</span></span>  <span data-ttu-id="f08b8-116">เมื่อเพื่อนร่วมงานของคุณสแกนรหัสด้วย iPhones ของพวกเขา (โทรศัพท์ Android กำลังมาในเร็ว ๆ นี้) พวกเขาจะเห็นรายงานคุณได้โยงเข้ากับคิวอาร์โค้ดนั้น ๆ</span><span class="sxs-lookup"><span data-stu-id="f08b8-116">When your colleagues scan the code with their iPhones (Android phones are coming soon), they see the report you've associated with that QR code.</span></span> 

<span data-ttu-id="f08b8-117">ข้อมูลเพิ่มเติมเกี่ยวกับ[การสร้างคิวอาร์โค้ดสำหรับรายงานใน Power BI](../../create-reports/service-create-qr-code-for-report.md)</span><span class="sxs-lookup"><span data-stu-id="f08b8-117">More about [creating a QR code for a report in Power BI](../../create-reports/service-create-qr-code-for-report.md)</span></span>

## <a name="barcodes"></a><span data-ttu-id="f08b8-118">บาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="f08b8-118">Barcodes</span></span>
<span data-ttu-id="f08b8-119">ติดป้ายข้อมูลบาร์โค้ดในรายงานของคุณเพื่อให้เพื่อนร่วมงานสามารถสแกนบาร์โค้ดที่อยู่บนผลิตภัณฑ์ และสามารถเข้าตรงไปยังรายงานที่ได้รับการกรองสำหรับผลิตภัณฑ์นั้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="f08b8-119">Tag barcode data in your report so your colleagues can scan a barcode on a product and go straight to that report, filtered for that product.</span></span>

![บาร์โค้ด](./media/mobile-apps-data-in-real-world-context/power-bi-barcode-scanner.png)

<span data-ttu-id="f08b8-121">ข้อมูลเพิ่มเติมเกี่ยวกับ:</span><span class="sxs-lookup"><span data-stu-id="f08b8-121">More about:</span></span>

* [<span data-ttu-id="f08b8-122">ติดป้ายข้อมูลบาร์โค้ดในรายงาน</span><span class="sxs-lookup"><span data-stu-id="f08b8-122">Tagging barcode data in a report</span></span>](../../transform-model/desktop-mobile-barcodes.md)
* [<span data-ttu-id="f08b8-123">การสแกนบาร์โค้ดจากแอป Power BI บน iPhone ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f08b8-123">Scanning a barcode from the Power BI app on your iPhone</span></span>](mobile-apps-scan-barcode-iphone.md)

## <a name="filter-by-location"></a><span data-ttu-id="f08b8-124">กรองข้อมูลตามตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="f08b8-124">Filter by location</span></span>
<span data-ttu-id="f08b8-125">จัดประเภทข้อมูลทางภูมิศาสตร์ในรายงานใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="f08b8-125">Categorize geographical data in a report in Power BI Desktop.</span></span> <span data-ttu-id="f08b8-126">เมื่อเพื่อนร่วมงานของคุณดูรายงานนั้นในแอปโทรศัพท์เคลื่อนที่ Power BI สำหรับ iOS แอป Power BI จะให้การกรองข้อมูลทางภูมิศาสตร์ที่เข้ากับสถานที่ที่คุณอยู่ในตอนนั้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f08b8-126">Then your colleagues view that report in the Power BI mobile app for iOS, Power BI automatically provides geographical filters that match where they are.</span></span>

<span data-ttu-id="f08b8-127">ข้อมูลเพิ่มเติมเกี่ยวกับ[การกรองตามตำแหน่งที่ตั้ง](mobile-apps-geographic-filtering.md)</span><span class="sxs-lookup"><span data-stu-id="f08b8-127">More about [filtering by location](mobile-apps-geographic-filtering.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="f08b8-128">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="f08b8-128">Next steps</span></span>
* [<span data-ttu-id="f08b8-129">การสร้างคิวอาร์โค้ดสำหรับไทล์ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="f08b8-129">Create a QR code for a tile in Power BI</span></span>](../../create-reports/service-create-qr-code-for-tile.md)
* [<span data-ttu-id="f08b8-130">การสร้างคิวอาร์โค้ดสำหรับรายงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="f08b8-130">Create a QR code for a report in Power BI</span></span>](../../create-reports/service-create-qr-code-for-report.md)
