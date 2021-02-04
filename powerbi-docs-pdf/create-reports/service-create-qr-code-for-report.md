---
title: สร้างคิวอาร์โค้ดให้แก่รายงานที่ใช้ในแอปสำหรับอุปกรณ์เคลื่อนที่ของ Power BI
description: คิวอาร์โค้ดใน Power BI สามารถเชื่อมต่อทุกอย่างในโลกแห่งความจริง เข้ากับข้อมูลที่เกี่ยวข้องกับ BI ในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่ได้โดยตรง โดยที่ไม่จำเป็นต้องใช้การค้นหา
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 03/13/2018
LocalizationGroup: Reports
ms.openlocfilehash: 6322876bec350ca3d7c3fde4586387d640423f07
ms.sourcegitcommit: 1cad78595cca1175b82c04458803764ac36e5e37
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/19/2021
ms.locfileid: "98565531"
---
# <a name="create-a-qr-code-for-a-report-in-power-bi-to-use-in-the-mobile-apps"></a><span data-ttu-id="b7f1d-103">สร้างคิวอาร์โค้ด ให้แก่รายงานที่ใช้ในแอปสำหรับอุปกรณ์เคลื่อนที่ของ Power BI</span><span class="sxs-lookup"><span data-stu-id="b7f1d-103">Create a QR code for a report in Power BI to use in the mobile apps</span></span>
<span data-ttu-id="b7f1d-104">คิวอาร์โค้ดใน Power BI สามารถเชื่อมต่อทุกอย่างในโลกแห่งความจริง เข้ากับข้อมูลที่เกี่ยวข้องกับ BI่ได้โดยตรง &#151; โดยที่ไม่จำเป็นต้องใช้การค้นหา</span><span class="sxs-lookup"><span data-stu-id="b7f1d-104">QR codes in Power BI can connect anything in the real world directly to related BI information &#151; no navigation or search needed.</span></span>

<span data-ttu-id="b7f1d-105">คุณสามารถสร้างคิวอาร์โค้ดในบริการ Power BI ให้แก่รายงานทุกชนิด แม้แต่รายงานคุณไม่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="b7f1d-105">You can create a QR code in the Power BI service for any report, even for a report you can't edit.</span></span> <span data-ttu-id="b7f1d-106">จากนั้น คุณใส่คิวอาร์โค้ดในตำแหน่งหลัก</span><span class="sxs-lookup"><span data-stu-id="b7f1d-106">Then you place the QR code in a key location.</span></span> <span data-ttu-id="b7f1d-107">ตัวอย่างเช่น คุณสามารถวางลงในอีเมล หรือพิมพ์ออกมาและวางในตำแหน่งที่เจาะจง</span><span class="sxs-lookup"><span data-stu-id="b7f1d-107">For example, you could paste it in an email, or print it out and paste it in a specific location.</span></span> 

<span data-ttu-id="b7f1d-108">เพื่อนร่วมงานที่คุณแชร์รายงานด้วยจะสามารถสแกนคิวอาร์โค้ดเพื่อเข้าถึงรายงาน ได้จาก[อุปกรณ์เคลื่อนที่ของพวกเขา](../consumer/mobile/mobile-apps-qr-code.md)</span><span class="sxs-lookup"><span data-stu-id="b7f1d-108">Colleagues you've shared the report with can scan the QR code for access to the report, right from [their mobile device](../consumer/mobile/mobile-apps-qr-code.md).</span></span> <span data-ttu-id="b7f1d-109">พวกเขาสามารถใช้ที่สแกนคิวอาร์โค้ดที่อยู่ในแอป Power BI หรือที่สแกนคิวอาร์โค้ดอื่น ๆ ที่ติดตั้งบนอุปกรณ์ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="b7f1d-109">They can use either the QR code scanner located in the Power BI app, or any other QR scanner installed on their device.</span></span> <span data-ttu-id="b7f1d-110">พวกเขายังสามารถ[สแกนคิวอาร์โค้ดด้วย Power BI สำหรับแอปความเป็นจริงผสม](../consumer/mobile/mobile-hololens2-app.md#open-reports-with-qr-codes)ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="b7f1d-110">They can also [scan a report QR code with the Power BI for Mixed Reality app](../consumer/mobile/mobile-hololens2-app.md#open-reports-with-qr-codes).</span></span>

## <a name="create-a-qr-code-for-a-report"></a><span data-ttu-id="b7f1d-111">สร้างคิวอาร์โค้ดสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="b7f1d-111">Create a QR code for a report</span></span>
1. <span data-ttu-id="b7f1d-112">เปิดรายงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="b7f1d-112">Open a report in the Power BI service.</span></span>
2. <span data-ttu-id="b7f1d-113">เลือก **ตัวเลือกเพิ่มเติม** (...) ที่มุมขวาบน แล้วเลือก **สร้างคิวอาร์โค้ด**</span><span class="sxs-lookup"><span data-stu-id="b7f1d-113">Select **More options** (...) in the top-right corner and select **Generate QR code**.</span></span> 
   
    ![ภาพหน้าจอของรายงาน ที่แสดงตัวชี้จากจุดไข่ปลาเพื่อสร้างรหัส QR](media/service-create-qr-code-for-report/power-bi-create-qr-code-report.png)
3. <span data-ttu-id="b7f1d-115">กล่องโต้ตอบที่มีคิวอาร์โค้ดจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="b7f1d-115">A dialog box with the QR code appears.</span></span> 
   
    ![ภาพหน้าจอของกล่องโต้ตอบ ที่แสดงว่ารหัส QR พร้อมที่จะดาวน์โหลดหรือบันทึก](media/service-create-qr-code-for-report/powerbi_report_qrcode.png)
4. <span data-ttu-id="b7f1d-117">จากที่นี่ คุณสามารถสแกนคิวอาร์โค้ด หรือดาวน์โหลด และบันทึกเพื่อให้คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="b7f1d-117">From here you can scan the QR code or download and save it so you can:</span></span> 
   
   * <span data-ttu-id="b7f1d-118">เพิ่มคิวอาร์โค้ดลงในอีเมลหรือเอกสารอื่น ๆ หรือ</span><span class="sxs-lookup"><span data-stu-id="b7f1d-118">Add it to an email or other document, or</span></span> 
   * <span data-ttu-id="b7f1d-119">พิมพคิวอาร์โค้ดและวางในตำแหน่งที่เจาะจง</span><span class="sxs-lookup"><span data-stu-id="b7f1d-119">Print it and place it in a specific location.</span></span> 

## <a name="print-the-qr-code"></a><span data-ttu-id="b7f1d-120">พิมพ์คิวอาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="b7f1d-120">Print the QR code</span></span>
<span data-ttu-id="b7f1d-121">Power BI สร้างคิวอาร์โค้ด เป็นไฟล์ JPG พร้อมที่จะพิมพ์</span><span class="sxs-lookup"><span data-stu-id="b7f1d-121">Power BI generates the QR code as a JPG file, ready to print.</span></span> 

1. <span data-ttu-id="b7f1d-122">เลือก **ดาวน์โหลด** แล้ว เปิดไฟล์ JPG บนคอมพิวเตอร์ที่เชื่อมต่อกับเครื่องพิมพ์</span><span class="sxs-lookup"><span data-stu-id="b7f1d-122">Select **Download**, then open the JPG file on a computer connected to a printer.</span></span>  
   
   <span data-ttu-id="b7f1d-123">ไฟล์ JPG จะมีชื่อเหมือนกันเป็นไทล</span><span class="sxs-lookup"><span data-stu-id="b7f1d-123">The JPG file has the same name as the tile.</span></span> <span data-ttu-id="b7f1d-124">ตัวอย่างเช่น “Sale and Marketing Sample.jpg”</span><span class="sxs-lookup"><span data-stu-id="b7f1d-124">For example, "Sales and Marketing Sample.jpg".</span></span>
   
1. <span data-ttu-id="b7f1d-125">พิมพ์ไฟล์ที่ขนาด 100 เปอร์เซ็นต์ หรือ “ขนาดตามจริง”</span><span class="sxs-lookup"><span data-stu-id="b7f1d-125">Print the file at 100% or “actual size”.</span></span>  
2. <span data-ttu-id="b7f1d-126">ตัดคิวอาร์โค้ดโดยรอบตามของของแผ่นงาน และใช้กาวติดไว้ตรงบริเวณที่เกี่ยวข้องกับรายงานนั้น ๆ</span><span class="sxs-lookup"><span data-stu-id="b7f1d-126">Cut out the QR code along its edge and glue it to a place relevant to the report.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="b7f1d-127">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="b7f1d-127">Next steps</span></span>
* <span data-ttu-id="b7f1d-128">[เชื่อมต่อกับข้อมูล Power BI จากโลกแห่งความจริง](../consumer/mobile/mobile-apps-data-in-real-world-context.md)ด้วยแอปโทรศัพท์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="b7f1d-128">[Connect to Power BI data from the real world](../consumer/mobile/mobile-apps-data-in-real-world-context.md) with the mobile apps</span></span>
* [<span data-ttu-id="b7f1d-129">สแกนคิวอาร์โค้ดของ Power BI จากอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="b7f1d-129">Scan a Power BI QR code from your mobile device</span></span>](../consumer/mobile/mobile-apps-qr-code.md)
* [<span data-ttu-id="b7f1d-130">สร้างคิวอาร์โค้ด สำหรับไทล์</span><span class="sxs-lookup"><span data-stu-id="b7f1d-130">Create a QR code for a tile</span></span>](service-create-qr-code-for-tile.md)
* <span data-ttu-id="b7f1d-131">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="b7f1d-131">Questions?</span></span> [<span data-ttu-id="b7f1d-132">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="b7f1d-132">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
