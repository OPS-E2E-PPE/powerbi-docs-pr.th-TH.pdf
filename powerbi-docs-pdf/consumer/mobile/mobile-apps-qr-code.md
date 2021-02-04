---
title: สแกนคิวอาร์โค้ดของ Power BI จากอุปกรณ์เคลื่อนที่ของคุณ
description: คิวอาร์โค้ดใน Power BI สามารถเชื่อมต่อทุกอย่างในโลกแห่งความจริง เข้ากับข้อมูลที่เกี่ยวข้องกับ BI ในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่ได้โดยตรง iPhones โดยที่ไม่จำเป็นต้อง Android ใช้การค้นหา
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 12/02/2019
ms.openlocfilehash: 96859efbaf86c8c6e9abf459500c38d49ee4f112
ms.sourcegitcommit: 1cad78595cca1175b82c04458803764ac36e5e37
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/19/2021
ms.locfileid: "98565500"
---
# <a name="scan-a-power-bi-qr-code-from-your-mobile-device"></a><span data-ttu-id="1c39c-103">สแกนคิวอาร์โค้ดของ Power BI จากอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="1c39c-103">Scan a Power BI QR code from your mobile device</span></span>
<span data-ttu-id="1c39c-104">นำไปใช้กับ:</span><span class="sxs-lookup"><span data-stu-id="1c39c-104">Applies to:</span></span>

| ![iPhone](./media/mobile-apps-qr-code/ios-logo-40-px.png) | ![iPad](./media/mobile-apps-qr-code/ios-logo-40-px.png) | ![โทรศัพท์ Android](././media/mobile-apps-qr-code/android-logo-40-px.png) | ![แท็บเล็ต Android](././media/mobile-apps-qr-code/android-logo-40-px.png) |
|:--- |:--- |:--- |:--- |
|<span data-ttu-id="1c39c-109">iPhone</span><span class="sxs-lookup"><span data-stu-id="1c39c-109">iPhones</span></span> |<span data-ttu-id="1c39c-110">iPad</span><span class="sxs-lookup"><span data-stu-id="1c39c-110">iPads</span></span> |<span data-ttu-id="1c39c-111">โทรศัพท์ Android</span><span class="sxs-lookup"><span data-stu-id="1c39c-111">Android phones</span></span> |<span data-ttu-id="1c39c-112">แท็บเล็ต Android</span><span class="sxs-lookup"><span data-stu-id="1c39c-112">Android tablets</span></span> |

<span data-ttu-id="1c39c-113">คิวอาร์โค้ดใน Power BI สามารถเชื่อมต่อทุกอย่างในโลกแห่งความจริง เข้ากับข้อมูลที่เกี่ยวข้องกับ BI่ได้โดยตรง &#151; โดยที่ไม่จำเป็นต้องใช้การค้นหา</span><span class="sxs-lookup"><span data-stu-id="1c39c-113">QR codes in Power BI can connect any item in the real world directly to related BI information &#151; no navigation or search needed.</span></span>

<span data-ttu-id="1c39c-114">อย่างเช่น เพื่อนร่วมงานได้[สร้างคิวอาร์โค้ดในบริการ Power BI](../../create-reports/service-create-qr-code-for-tile.md)สำหรับรายงาน หรือไทล์ในแดชบอร์ด แชร์แดชบอร์ดหรือรายงานกับคุณ และวางคิวอาร์โค้ดในตำแหน่งที่ตั้งคีย์&#151;ตัวอย่างเช่น ในอีเมล หรือในรายการที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="1c39c-114">Say a colleague has [created a QR code in the Power BI service](../../create-reports/service-create-qr-code-for-tile.md) for a report or for a tile in a dashboard, shared the dashboard or report with you, and placed the QR code in a key location &#151; for example, in an email or on a specific item.</span></span> 

<span data-ttu-id="1c39c-115">คุณสามารถสแกนคิวอาร์โค้ด สำหรับการเข้าถึงไปยังไทลแบบทันที์ที่เกี่ยวข้องหรือรายงาน จากโทรศัพท์ของคุณโดยตรง ใช้เครื่องสแกนในแอป Power BI หรือสแกนเนอร์อื่น ๆ ที่ติดตั้งบนโทรศัพท์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="1c39c-115">You can scan the QR code for immediate access to the relevant tile or report, right from your phone, using either the scanner in the Power BI app, or any other scanner installed on your phone.</span></span> 

<span data-ttu-id="1c39c-116">ถ้าผู้ร่วมงานของคุณไม่ได้แชร์แดชบอร์ดหรือรายงานกับคุณ คุณสามารถร้องขอการเข้าถึงได้โดยตรงจากอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="1c39c-116">If your colleague hasn't shared the dashboard or report with you, you can request access directly from the mobile app.</span></span> 

> [!NOTE]
> <span data-ttu-id="1c39c-117">พวกเขายังสามารถ[สแกนคิวอาร์โค้ดด้วย Power BI สำหรับแอปความเป็นจริงผสม](./mobile-hololens2-app.md#open-reports-with-qr-codes)ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="1c39c-117">You can also [scan a report QR code with the Power BI for Mixed Reality app](./mobile-hololens2-app.md#open-reports-with-qr-codes).</span></span>

## <a name="scan-a-power-bi-qr-code-on-your-iphone-with-the-power-bi-scanner"></a><span data-ttu-id="1c39c-118">สแกนรหัส Power BI QR บน iPhone ของคุณกับสแกนเนอร์ Power BI</span><span class="sxs-lookup"><span data-stu-id="1c39c-118">Scan a Power BI QR code on your iPhone with the Power BI scanner</span></span>

1. <span data-ttu-id="1c39c-119">ที่แถบนำทาง แตะที่ **ตัวเลือกเพิ่มเติม** (...) และแตะที่ **สแกนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="1c39c-119">On the navigation bar, tap **More options** (...) and then tap **Scanner**.</span></span>

    ![ภาพหน้าจอของตัวเลือกเพิ่มเติมในบานหน้าต่างการนำทาง ที่แสดงการเลือกเครื่องสแกน](media/mobile-apps-qr-code/power-bi-scanner.png)

2. <span data-ttu-id="1c39c-121">ถ้ากล้องของคุณไม่ได้เปิดใช้งาน คุณจำเป็นต้องอนุมัติให้แอป Power BI ใช้กล้อง</span><span class="sxs-lookup"><span data-stu-id="1c39c-121">If your camera is not enabled, you need to approve the Power BI app to use the camera.</span></span> <span data-ttu-id="1c39c-122">นี่เป็นการอนุมัติครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="1c39c-122">This is a one-time approval.</span></span> 
 
3. <span data-ttu-id="1c39c-123">วางตำแหน่งสแกนเนอร์ที่ Power BI QR โค้ด</span><span class="sxs-lookup"><span data-stu-id="1c39c-123">Point the scanner at the Power BI QR code.</span></span> 
   
    ![ภาพหน้าจอของกระดาษหนังสือพิมพ์ ที่แสดงเครื่องสแกนชี้ไปที่คิวอาร์โค้ดของ Power B I](media/mobile-apps-qr-code/power-bi-align-qr-code.png)
4. <span data-ttu-id="1c39c-125">ไทล์หรือรายงานปรากฏขึ้นเมื่อต้องการ เหนือพื้นหลังในความเป็นจริงเสริม</span><span class="sxs-lookup"><span data-stu-id="1c39c-125">The tile or report appears to hover over the background in augmented reality.</span></span>
   
    ![ภาพหน้าจอของรายงาน ที่แสดงการเลื่อนไปเหนือกระดาษหนังสือพิมพ์](media/mobile-apps-qr-code/power-bi-ios-qr-ar-scanner.png)

5. <span data-ttu-id="1c39c-127">แตะรายงานหรือไทล์เพื่อเปิดในโหมดโฟกัส หรือย้อนกลับไปยังสแกนเนอร์</span><span class="sxs-lookup"><span data-stu-id="1c39c-127">Tap the report or the tile to open it in focus mode, or go back to the scanner.</span></span>

### <a name="scan-a-qr-code-from-an-external-scanner-on-your-iphone"></a><span data-ttu-id="1c39c-128">สแกนคิวอาร์โค้ดจากสแกนเนอร์ภายนอกบน iPhone ของคุณ</span><span class="sxs-lookup"><span data-stu-id="1c39c-128">Scan a QR code from an external scanner on your iPhone</span></span>
1. <span data-ttu-id="1c39c-129">สแกนเนอร์ใดก็ได้ที่ติดตั้งบนโทรศัพท์ของคุณสามารถนำมาวางให้ตรงตำแหน่งคิวอาร์โค้ดสแกนเนอร์ Power BI ที่เกี่ยวข้องเพื่อการเข้าถึงไปยังไทล์หรือรายงานอย่างทันที</span><span class="sxs-lookup"><span data-stu-id="1c39c-129">From any scanner installed on your phone, point the scanner to the relevant Power BI QR code for immediate access to the tile or report.</span></span> 
2. <span data-ttu-id="1c39c-130">ถ้าคุณไม่ได้ติดตั้งแอป Power BI คุณจะถูกนำไปยัง[Apple App Store เพื่อดาวน์โหลด](https://go.microsoft.com/fwlink/?LinkId=522062)บน iPhone ของคุณ</span><span class="sxs-lookup"><span data-stu-id="1c39c-130">If you don't have the Power BI app installed, you are redirected to the [Apple App Store to download it](https://go.microsoft.com/fwlink/?LinkId=522062) on your iPhone.</span></span>

## <a name="scan-a-power-bi-qr-code-on-your-android-device-with-the-power-bi-scanner"></a><span data-ttu-id="1c39c-131">สแกนคิวอาร์โค้ด Power BI บน ของคุณกับสแกนเนอร ์Android Power BI</span><span class="sxs-lookup"><span data-stu-id="1c39c-131">Scan a Power BI QR code on your Android device with the Power BI scanner</span></span>

1. <span data-ttu-id="1c39c-132">ที่แถบนำทาง แตะที่ **ตัวเลือกเพิ่มเติม** (...) และแตะที่ **สแกนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="1c39c-132">On the navigation bar, tap **More options** (...) and then tap **Scanner**.</span></span>

    ![ภาพหน้าจอของตัวเลือกเพิ่มเติมในบานหน้าต่างการนำทาง ที่แสดงการเลือกเครื่องสแกน](media/mobile-apps-qr-code/power-bi-scanner.png)

2. <span data-ttu-id="1c39c-134">ถ้ากล้องของคุณไม่ได้เปิดใช้งาน คุณจำเป็นต้องอนุมัติให้แอป Power BI ใช้กล้อง</span><span class="sxs-lookup"><span data-stu-id="1c39c-134">If your camera is not enabled, you need to approve the Power BI app to use the camera.</span></span> <span data-ttu-id="1c39c-135">นี่เป็นการอนุมัติครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="1c39c-135">This is a one-time approval.</span></span> 

3. <span data-ttu-id="1c39c-136">วางตำแหน่งสแกนเนอร์ที่ Power BI QR โค้ด</span><span class="sxs-lookup"><span data-stu-id="1c39c-136">Point the scanner at the Power BI QR code.</span></span> 
   
    ![ภาพหน้าจอของเครื่องสแกนคิวอาร์โค้ด ที่แสดงเครื่องสแกนชี้ไปยังคิวอาร์โค้ดของ Power B I](media/mobile-apps-qr-code/pbi_iph_qrscan.png)
4. <span data-ttu-id="1c39c-138">ไทล์หรือรายงานเปิดโดยอัตโนมัติใน Power BI</span><span class="sxs-lookup"><span data-stu-id="1c39c-138">The tile or report opens automatically in Power BI.</span></span>
   
    ![ภาพหน้าจอของรายงานจำนวนโอกาส ที่แสดงแผนภูมิคอลัมน์ตามเดือนและสถานะของยอดขาย](media/mobile-apps-qr-code/power-bi-android-tile.png)

### <a name="scan-a-qr-code-from-an-external-scanner-on-your-android-device"></a><span data-ttu-id="1c39c-140">สแกนคิวอาร์โค้ดจากสแกนเนอร์ภายนอกบน Android ของคุณ</span><span class="sxs-lookup"><span data-stu-id="1c39c-140">Scan a QR code from an external scanner on your Android device</span></span>
1. <span data-ttu-id="1c39c-141">สแกนเนอร์ใดก็ได้ที่ติดตั้งบนโทรศัพท์แอนดรอยด์ของคุณ Android สามารถนำมาวางให้ตรงตำแหน่งคิวอาร์โค้ดสแกนเนอร์ Power BI ที่เกี่ยวข้องเพื่อการเข้าถึงไปยังไทล์หรือรายงานอย่างทันที</span><span class="sxs-lookup"><span data-stu-id="1c39c-141">From any scanner installed on your Android device, point the scanner to the relevant Power BI QR code for immediate access to the tile or report.</span></span> 
2. <span data-ttu-id="1c39c-142">ถ้าคุณไม่ได้ติดตั้งแอป Power BI คุณจะถูกนำไปยัง[Google Play เพื่อดาวน์โหลดแอป](https://go.microsoft.com/fwlink/?LinkID=544867)</span><span class="sxs-lookup"><span data-stu-id="1c39c-142">If you don't have the Power BI app installed, you are redirected to [Google Play to download it](https://go.microsoft.com/fwlink/?LinkID=544867).</span></span> 

## <a name="next-steps"></a><span data-ttu-id="1c39c-143">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="1c39c-143">Next steps</span></span>
* <span data-ttu-id="1c39c-144">[เชื่อมต่อกับข้อมูล Power BI จากโลกแห่งความจริง](mobile-apps-data-in-real-world-context.md)ด้วยแอปโทรศัพท์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="1c39c-144">[Connect to Power BI data from the real world](mobile-apps-data-in-real-world-context.md) with the mobile apps</span></span>
* [<span data-ttu-id="1c39c-145">สร้างคิวอาร์โค้ดสำหรับไทล์ในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="1c39c-145">Create a QR code for a tile in the Power BI service</span></span>](../../create-reports/service-create-qr-code-for-tile.md)
* [<span data-ttu-id="1c39c-146">สร้างคิวอาร์โค้ดสำหรับรายงานในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="1c39c-146">Create a QR code for a report in the Power BI service</span></span>](../../create-reports/service-create-qr-code-for-report.md)
* <span data-ttu-id="1c39c-147">คุณยังสามารถ[สแกนคิวอาร์โค้ดด้วย Power BI สำหรับแอปความเป็นจริงผสม](./mobile-hololens2-app.md)ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="1c39c-147">You can also [scan a QR code with the Power BI for Mixed Reality app](./mobile-hololens2-app.md)</span></span>
* <span data-ttu-id="1c39c-148">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="1c39c-148">Questions?</span></span> [<span data-ttu-id="1c39c-149">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="1c39c-149">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
