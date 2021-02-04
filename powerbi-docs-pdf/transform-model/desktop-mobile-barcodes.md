---
title: แท็กเขตข้อมูลบาร์โค้ดใน Power BI Desktop สำหรับแอปสำหรับอุปกรณ์เคลื่อนที่
description: เมื่อคุณแท็กเขตข้อมูลบาร์โค้ดในแบบจำลองของคุณใน Power BI Desktop คุณสามารถกรองข้อมูลสำหรับบาร์โค้ดได้โดยอัตโนมัติในแอป Power BI บน iPhone ของคุณ
author: paulinbar
ms.author: painbar
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: how-to
ms.date: 01/16/2018
LocalizationGroup: Model your data
ms.openlocfilehash: 91cf4fb4101b710ad49e49c914dbc4bcaa03682a
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413943"
---
# <a name="tag-barcodes-in-power-bi-desktop-for-use-in-the-mobile-app"></a><span data-ttu-id="d49f4-103">แท็กบาร์โค้ดใน Power BI Desktop สำหรับใช้ในแอปสำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="d49f4-103">Tag barcodes in Power BI Desktop for use in the mobile app</span></span>

<span data-ttu-id="d49f4-104">ใน Power BI Desktop คุณสามารถ [จัดประเภทข้อมูล](desktop-data-categorization.md) ในคอลัมน์ ดังนั้น Power BI Desktop จึงทราบวิธีการนำค่ามาใช้ในการแสดงผลด้วยภาพในรายงานได้</span><span class="sxs-lookup"><span data-stu-id="d49f4-104">In Power BI Desktop, you can [categorize data](desktop-data-categorization.md) in a column, so Power BI Desktop knows how to treat values in visuals in a report.</span></span> <span data-ttu-id="d49f4-105">นอกจากนี้ คุณยังสามารถจัดประเภทคอลัมน์เป็น **บาร์โค้ด** ได้</span><span class="sxs-lookup"><span data-stu-id="d49f4-105">You can also categorize a column as **Barcode**.</span></span> <span data-ttu-id="d49f4-106">เมื่อคุณหรือเพื่อนร่วมงาน [สแกนบาร์โค้ดบนผลิตภัณฑ์ด้วยแอป Power BI](../consumer/mobile/mobile-apps-scan-barcode-iphone.md) บน iPhone คุณก็จะเห็นรายงานใด ๆ ที่มีบาร์โค้ดนั้น</span><span class="sxs-lookup"><span data-stu-id="d49f4-106">When you or your colleagues [scan a barcode on a product with the Power BI app](../consumer/mobile/mobile-apps-scan-barcode-iphone.md) on the iPhone, you see any report that includes that barcode.</span></span> <span data-ttu-id="d49f4-107">เมื่อคุณเปิดรายงานในแอปสำหรับอุปกรณ์เคลื่อนที่ Power BI ก็จะกรองรายงานให้เป็นข้อมูลที่เกี่ยวข้องกับบาร์โค้ดนั้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d49f4-107">When you open the report in the mobile app, Power BI automatically filters the report to data related to that barcode.</span></span>

1. <span data-ttu-id="d49f4-108">ใน Power BI Desktop สลับไปยังมุมมองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d49f4-108">In Power BI Desktop, switch to Data View.</span></span>
2. <span data-ttu-id="d49f4-109">เลือกคอลัมน์ที่มีข้อมูลบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="d49f4-109">Select a column with barcode data.</span></span> <span data-ttu-id="d49f4-110">ดูรายการของ [รูปแบบบาร์โค้ดที่สนับสนุน](#supported-barcode-formats) ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="d49f4-110">See the list of [supported barcode formats](#supported-barcode-formats) below.</span></span>
3. <span data-ttu-id="d49f4-111">บนแท็บ **การวางรูปแบบ** เลือก **บาร์โค้ด** > **ประเภทข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="d49f4-111">On the **Modeling** tab, select **Data Category** > **Barcode**.</span></span>
   
    ![รายการประเภทข้อมูล](media/desktop-mobile-barcodes/power-bi-desktop-barcode.png)
4. <span data-ttu-id="d49f4-113">ในมุมมองรายงาน เพิ่มเขตข้อมูลนี้ในการแสดงผลด้วยภาพที่คุณต้องการโดยกรองตามบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="d49f4-113">In Report view, add this field to the visuals you want filtered by the barcode.</span></span>
5. <span data-ttu-id="d49f4-114">บันทึกรายงานและเผยแพร่ไปยังบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="d49f4-114">Save the report and publish it to the Power BI service.</span></span>

<span data-ttu-id="d49f4-115">ในตอนนี้ เมื่อคุณเปิดสแกนเนอร์บน [แอป Power BI สำหรับ iPhone](../consumer/mobile/mobile-iphone-app-get-started.md) และสแกนบาร์โค้ด คุณจะเห็นรายงานนี้ในรายการของรายงาน</span><span class="sxs-lookup"><span data-stu-id="d49f4-115">Now when you open the scanner on the [Power BI app for iPhone](../consumer/mobile/mobile-iphone-app-get-started.md) and scan a barcode, you see this report in the list of reports.</span></span> <span data-ttu-id="d49f4-116">เมื่อคุณเปิดรายงาน การแสดงผลด้วยภาพจะถูกกรองตามบาร์โค้ดผลิตภัณฑ์ที่คุณสแกน</span><span class="sxs-lookup"><span data-stu-id="d49f4-116">When you open the report, its visuals are filtered by the product barcode you scanned.</span></span>

## <a name="supported-barcode-formats"></a><span data-ttu-id="d49f4-117">รูปแบบบาร์โค้ดที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="d49f4-117">Supported barcode formats</span></span>
<span data-ttu-id="d49f4-118">ต่อไปนี้เป็นบาร์โค้ดที่ Power BI จดจำถ้าคุณสามารถแท็กบาร์โค้ดเหล่านี้ในรายงาน Power BI:</span><span class="sxs-lookup"><span data-stu-id="d49f4-118">These are the barcodes Power BI recognizes if you can tag them in a Power BI report:</span></span> 

* <span data-ttu-id="d49f4-119">UPCECode</span><span class="sxs-lookup"><span data-stu-id="d49f4-119">UPCECode</span></span> 
* <span data-ttu-id="d49f4-120">Code39Code</span><span class="sxs-lookup"><span data-stu-id="d49f4-120">Code39Code</span></span>  
* <span data-ttu-id="d49f4-121">A39Mod43Code</span><span class="sxs-lookup"><span data-stu-id="d49f4-121">A39Mod43Code</span></span> 
* <span data-ttu-id="d49f4-122">EAN13Code</span><span class="sxs-lookup"><span data-stu-id="d49f4-122">EAN13Code</span></span> 
* <span data-ttu-id="d49f4-123">EAN8Code</span><span class="sxs-lookup"><span data-stu-id="d49f4-123">EAN8Code</span></span>  
* <span data-ttu-id="d49f4-124">93Code</span><span class="sxs-lookup"><span data-stu-id="d49f4-124">93Code</span></span>  
* <span data-ttu-id="d49f4-125">128Code</span><span class="sxs-lookup"><span data-stu-id="d49f4-125">128Code</span></span> 
* <span data-ttu-id="d49f4-126">PDF417Code</span><span class="sxs-lookup"><span data-stu-id="d49f4-126">PDF417Code</span></span> 
* <span data-ttu-id="d49f4-127">Interleaved2of5Code</span><span class="sxs-lookup"><span data-stu-id="d49f4-127">Interleaved2of5Code</span></span> 
* <span data-ttu-id="d49f4-128">ITF14Code</span><span class="sxs-lookup"><span data-stu-id="d49f4-128">ITF14Code</span></span> 

## <a name="next-steps"></a><span data-ttu-id="d49f4-129">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d49f4-129">Next steps</span></span>
* [<span data-ttu-id="d49f4-130">สแกนบาร์โค้ดจากแอป Power BI บน iPhone ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d49f4-130">Scan a barcode from the Power BI app on your iPhone</span></span>](../consumer/mobile/mobile-apps-scan-barcode-iphone.md)
* [<span data-ttu-id="d49f4-131">ปัญหาเกี่ยวกับการสแกนบาร์โค้ดบน iPhone</span><span class="sxs-lookup"><span data-stu-id="d49f4-131">Issues with scanning barcodes on an iPhone</span></span>](../consumer/mobile/mobile-apps-scan-barcode-iphone.md#issues-with-scanning-a-barcode)
* [<span data-ttu-id="d49f4-132">จัดประเภทข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d49f4-132">Data categorization in Power BI Desktop</span></span>](desktop-data-categorization.md)  
* <span data-ttu-id="d49f4-133">มีคำถามหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="d49f4-133">Questions?</span></span> [<span data-ttu-id="d49f4-134">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="d49f4-134">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
