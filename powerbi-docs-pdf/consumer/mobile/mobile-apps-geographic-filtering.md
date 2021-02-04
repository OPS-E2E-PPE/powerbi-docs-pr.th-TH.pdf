---
title: ตัวกรองรายงานตามตำแหน่งที่ตั้งทางภูมิศาสตร์ในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่
description: เรียนรู้วิธีที่คุณสามารถกรองรายงานตามตำแหน่งที่ตั้งทางภูมิศาสตร์ในแอป Microsoft Power BI สำหรับอุปกรณ์เคลื่อนที่ ถ้าเจ้าของรายงานกำหนดแท็กที่ตั้งทางภูมิศาสตร์
author: paulinbar
ms.author: painbar
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 03/11/2020
ms.openlocfilehash: fe5ab9befcf54a617aefa5ad281872f45a59229c
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96388988"
---
# <a name="filter-a-report-by-geographic-location-in-the-power-bi-mobile-apps"></a><span data-ttu-id="eac96-103">กรองรายงานตามตำแหน่งที่ตั้งทางภูมิศาสตร์ในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="eac96-103">Filter a report by geographic location in the Power BI mobile apps</span></span>
<span data-ttu-id="eac96-104">ใช้ได้กับ:</span><span class="sxs-lookup"><span data-stu-id="eac96-104">Applies to:</span></span>

| ![iPhone](./media/mobile-apps-geographic-filtering/iphone-logo-50-px.png) | ![iPad](./media/mobile-apps-geographic-filtering/ipad-logo-50-px.png) | ![โทรศัพท์ Android](./media/mobile-apps-geographic-filtering/android-phone-logo-50-px.png) | ![แท็บเล็ต Android](./media/mobile-apps-view-dashboard/android-tablet-logo-50-px.png) | ![โทรศัพท์ Windows](./media/mobile-apps-geographic-filtering/win-10-logo-50-px.png) |
|:--- |:--- |:--- |:--- |:--- |
| <span data-ttu-id="eac96-110">iPhone</span><span class="sxs-lookup"><span data-stu-id="eac96-110">iPhones</span></span> |<span data-ttu-id="eac96-111">iPad</span><span class="sxs-lookup"><span data-stu-id="eac96-111">iPads</span></span> |<span data-ttu-id="eac96-112">โทรศัพท์ Android</span><span class="sxs-lookup"><span data-stu-id="eac96-112">Android phones</span></span> |<span data-ttu-id="eac96-113">แท็บเล็ต Android</span><span class="sxs-lookup"><span data-stu-id="eac96-113">Android tablets</span></span> |<span data-ttu-id="eac96-114">มือถือ Windows 10</span><span class="sxs-lookup"><span data-stu-id="eac96-114">Windows 10 phones</span></span> |

<span data-ttu-id="eac96-115">เมื่อคุณดูที่รายงาน Power BI บนอุปกรณ์เคลื่อนที่ของคุณ คุณเห็นไอคอนรูปเข็มหมุดเล็ก ๆ ที่มุมบนขวาหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="eac96-115">When you look at a Power BI report on your mobile device, do you see a little pushpin icon in the upper-right corner?</span></span> <span data-ttu-id="eac96-116">ถ้าเป็นเช่นนั้น คุณสามารถกรองรายงานตามตำแหน่งที่ตั้งทางภูมิศาสตร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="eac96-116">If so, then you can filter that report based on your geographic location.</span></span>

> [!NOTE]
> <span data-ttu-id="eac96-117">คุณสามารถกรองตามตำแหน่ง ถ้าชื่อทางภูมิศาสตร์ในรายงานเป็นภาษาอังกฤษเท่านั้น ตัวอย่างเช่น "New York City" หรือ "Germany"</span><span class="sxs-lookup"><span data-stu-id="eac96-117">You can only filter by location if the geographic names in the report are in English; for example, "New York City" or "Germany".</span></span> <span data-ttu-id="eac96-118">แท็บเล็ต Windows 10 และพีซีไม่สนับสนุนการกรองทางภูมิศาสตร์ แต่มือถือ Windows 10 ทำได้</span><span class="sxs-lookup"><span data-stu-id="eac96-118">Windows 10 tablets and PCs don't support geographic filtering, but Windows 10 phones do.</span></span>

>[!NOTE]
><span data-ttu-id="eac96-119">การสนับสนุนแอปอุปกรณ์เคลื่อนที่ Power BI สำหรับ **โทรศัพท์ที่ใช้ Windows 10 Mobile** จะถูกยกเลิกในวันที่ 16 มีนาคม 2021</span><span class="sxs-lookup"><span data-stu-id="eac96-119">Power BI mobile app support for **phones using Windows 10 Mobile** will be discontinued on March 16, 2021.</span></span> [<span data-ttu-id="eac96-120">ศึกษาเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="eac96-120">Learn more</span></span>](/legal/powerbi/powerbi-mobile/power-bi-mobile-app-end-of-support-for-windows-phones)

## <a name="filter-your-report-by-your-geographic-location"></a><span data-ttu-id="eac96-121">กรองรายงานของคุณตามที่ตั้งทางภูมิศาสตร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="eac96-121">Filter your report by your geographic location</span></span>
1. <span data-ttu-id="eac96-122">เปิดรายงานในแอป Power BI สำหรับอุปกรณ์เคลื่อนที บนอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="eac96-122">Open a report in the Power BI mobile app on your mobile device.</span></span>
2. <span data-ttu-id="eac96-123">ถ้ารายงานมีข้อมูลทางภูมิศาสตร์ คุณเห็นข้อความขออนุญาตให้ Power BI เข้าถึงตำแหน่งที่ตั้งของคุณ</span><span class="sxs-lookup"><span data-stu-id="eac96-123">If the report has geographic data, you see a message asking to allow Power BI to access your location.</span></span> <span data-ttu-id="eac96-124">คลิกที่ **อนุญาต** จากนั้นกดเลือก **อนุญาต** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="eac96-124">Click **Allow**, then tap **Allow** again.</span></span>
3. <span data-ttu-id="eac96-125">แตะที่เข็มหมุด</span><span class="sxs-lookup"><span data-stu-id="eac96-125">Tap the push pin</span></span> ![ไอคอนเข็มหมุด](./media/mobile-apps-geographic-filtering/power-bi-mobile-geo-icon.png)<span data-ttu-id="eac96-127">.</span><span class="sxs-lookup"><span data-stu-id="eac96-127">.</span></span> <span data-ttu-id="eac96-128">คุณสามารถกรองตาม เมือง รัฐ/จังหวัด หรือ ประเทศ/ภูมิภาค ขึ้นอยู่กับข้อมูลในรายงาน</span><span class="sxs-lookup"><span data-stu-id="eac96-128">You can filter by city, state/province, or country/region, depending on the data in the report.</span></span> <span data-ttu-id="eac96-129">ตัวกรองแสดงรายการตัวเลือก เฉพาะที่ตรงกับตำแหน่งปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="eac96-129">The filter only lists options that match your current location.</span></span>
   
    ![ตัวกรองเข็มหมุด](./media/mobile-apps-geographic-filtering/power-bi-mobile-geo-map-set-filter.png)

## <a name="why-dont-i-see-location-tags-on-a-report"></a><span data-ttu-id="eac96-131">ทำไมฉันจึงไม่เห็นแท็กตำแหน่งที่ตั้งในรายงาน</span><span class="sxs-lookup"><span data-stu-id="eac96-131">Why don't I see location tags on a report?</span></span>
<span data-ttu-id="eac96-132">จะต้องปฏิบัติตามเงื่อนไขทั้งหมดสามข้อต่อไปนี้เพื่อให้คุณเห็นแท็กตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="eac96-132">All three of the conditions below must be met for you to see location tags.</span></span> 

* <span data-ttu-id="eac96-133">บุคคลที่สร้างรายงานใน Power BI Desktop จะต้องมีการ[จัดประเภทข้อมูลทางภูมิศาสตร์](../../transform-model/desktop-mobile-geofiltering.md)ให้กับคอลัมน์อย่างน้อยหนึ่งคอลัมน์ เช่น เมือง รัฐ หรือประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="eac96-133">The person who created the report in Power BI Desktop  must have [categorized geographical data](../../transform-model/desktop-mobile-geofiltering.md) for at least one column, such as City, State, or Country/Region.</span></span>
* <span data-ttu-id="eac96-134">คุณอยู่ในตำแหน่งที่มีข้อมูลในคอลัมน์นั้น</span><span class="sxs-lookup"><span data-stu-id="eac96-134">You are in one of the locations that has data in that column.</span></span>
* <span data-ttu-id="eac96-135">คุณกำลังใช้อุปกรณ์เคลื่อนที่อย่างใดอย่างหนึ่งในนี้:</span><span class="sxs-lookup"><span data-stu-id="eac96-135">You're using one of these mobile devices:</span></span>
  * <span data-ttu-id="eac96-136">iOS (iPad, iPhone, iPod)</span><span class="sxs-lookup"><span data-stu-id="eac96-136">iOS (iPad, iPhone, iPod).</span></span>
  * <span data-ttu-id="eac96-137">Android (โทรศัพท์, แท็บเล็ต)</span><span class="sxs-lookup"><span data-stu-id="eac96-137">Android (phone, tablet).</span></span>
  * <span data-ttu-id="eac96-138">มือถือ Windows 10 (อุปกรณ์ Windows 10 อื่น ๆ เช่นพีซีและแท็บเล็ตไม่สนับสนุนการกรองทางภูมิศาสตร์)</span><span class="sxs-lookup"><span data-stu-id="eac96-138">Windows 10 phone (other Windows 10 devices such as PCs and tablets don't support geographic filtering).</span></span>

<span data-ttu-id="eac96-139">อ่านเพิ่มเติมเกี่ยวกับ[การตั้งค่าการกรองทางภูมิศาสตร์](../../transform-model/desktop-mobile-geofiltering.md)ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="eac96-139">Read more about [setting up geographic filtering](../../transform-model/desktop-mobile-geofiltering.md) in Power BI Desktop.</span></span>

### <a name="next-steps"></a><span data-ttu-id="eac96-140">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="eac96-140">Next steps</span></span>
* <span data-ttu-id="eac96-141">[เชื่อมต่อกับข้อมูล Power BI จากโลกแห่งความจริง](mobile-apps-data-in-real-world-context.md)ด้วยแอปสำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="eac96-141">[Connect to Power BI data from the real world](mobile-apps-data-in-real-world-context.md) with the mobile apps</span></span>
* [<span data-ttu-id="eac96-142">จัดประเภทข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="eac96-142">Data categorization in Power BI Desktop</span></span>](../../transform-model/desktop-data-categorization.md) 
* <span data-ttu-id="eac96-143">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="eac96-143">Questions?</span></span> [<span data-ttu-id="eac96-144">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="eac96-144">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)