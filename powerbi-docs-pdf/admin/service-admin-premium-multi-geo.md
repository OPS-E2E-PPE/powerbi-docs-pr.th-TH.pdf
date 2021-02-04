---
title: การสนับสนุนหลายภาคภูมิศาสตร์สำหรับ Power BI Premium
description: เรียนรู้วิธีปรับใช้เนื้อหาไปยังศูนย์ข้อมูลในภูมิภาคนอกเหนือจากภูมิภาคเดิมของผู้เช่า Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-premium
ms.topic: how-to
ms.date: 11/11/2020
LocalizationGroup: Premium
ms.openlocfilehash: b0132996be1ed70f228ce96d413c4925dc1a3e48
ms.sourcegitcommit: cc20b476a45bccb870c9de1d0b384e2c39e25d24
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/11/2020
ms.locfileid: "94512780"
---
# <a name="configure-multi-geo-support-for-power-bi-premium"></a><span data-ttu-id="ad759-103">กำหนดค่าการสนับสนุน Multi-Geo สำหรับ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="ad759-103">Configure Multi-Geo support for Power BI Premium</span></span>

<span data-ttu-id="ad759-104">Multi-Geo เป็นคุณลักษณะของ Power BI Premium ที่ช่วยให้ลูกค้าข้ามชาติจัดการกับความต้องการด้านถิ่นที่อยู่ของข้อมูลในระดับภูมิภาค เฉพาะธุรกิจ หรือองค์กร</span><span class="sxs-lookup"><span data-stu-id="ad759-104">Multi-Geo is a Power BI Premium feature that helps multinational customers address regional, industry-specific, or organizational data residency requirements.</span></span> <span data-ttu-id="ad759-105">ในฐานะลูกค้า Power BI Premium คุณสามารถปรับใช้เนื้อหาไปยังศูนย์ข้อมูลในภูมิภาคนอกเหนือจากภูมิภาคเดิมของผู้เช่า Power BI</span><span class="sxs-lookup"><span data-stu-id="ad759-105">As a Power BI Premium customer, you can deploy content to datacenters in regions other than the home region of the Power BI tenant.</span></span> <span data-ttu-id="ad759-106">พิกัด (ภูมิศาสตร์) สามารถมีได้มากกว่าหนึ่งภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="ad759-106">A geo (geography) can contain more than one region.</span></span> <span data-ttu-id="ad759-107">ตัวอย่างเช่น สหรัฐอเมริกาเป็นพิกัด และสหรัฐอเมริกากลางทางตะวันตกและสหรัฐอเมริกากลางทางใต้เป็นภูมิภาคในสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="ad759-107">For example, the United States is a geo, and West Central US and South Central US are regions in the United States.</span></span> <span data-ttu-id="ad759-108">คุณอาจเลือกปรับใช้เนื้อหาไปยังพิกัดใดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ad759-108">You may choose to deploy content to any of the following geos:</span></span>

- <span data-ttu-id="ad759-109">สหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="ad759-109">United States</span></span>
- <span data-ttu-id="ad759-110">แคนาดา</span><span class="sxs-lookup"><span data-stu-id="ad759-110">Canada</span></span>
- <span data-ttu-id="ad759-111">สหราชอาณาจักร</span><span class="sxs-lookup"><span data-stu-id="ad759-111">United Kingdom</span></span>
- <span data-ttu-id="ad759-112">บราซิล</span><span class="sxs-lookup"><span data-stu-id="ad759-112">Brazil</span></span>
- <span data-ttu-id="ad759-113">ยุโรป</span><span class="sxs-lookup"><span data-stu-id="ad759-113">Europe</span></span>
- <span data-ttu-id="ad759-114">ญี่ปุ่น</span><span class="sxs-lookup"><span data-stu-id="ad759-114">Japan</span></span>
- <span data-ttu-id="ad759-115">อินเดีย</span><span class="sxs-lookup"><span data-stu-id="ad759-115">India</span></span>
- <span data-ttu-id="ad759-116">เอเชียแปซิฟิก</span><span class="sxs-lookup"><span data-stu-id="ad759-116">Asia Pacific</span></span>
- <span data-ttu-id="ad759-117">ออสเตรเลีย</span><span class="sxs-lookup"><span data-stu-id="ad759-117">Australia</span></span>
- <span data-ttu-id="ad759-118">แอฟริกา</span><span class="sxs-lookup"><span data-stu-id="ad759-118">Africa</span></span>

<span data-ttu-id="ad759-119">Multi-Geo ไม่พร้อมให้บริการใน Power BI Germany, Power BI China ที่ดำเนินการโดย 21Vianet หรือ Power BI สำหรับรัฐบาลสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="ad759-119">Multi-Geo isn't available for Power BI Germany, Power BI China operated by 21Vianet, or Power BI for the US government.</span></span>

<span data-ttu-id="ad759-120">Multi-Geo ในขณะนี้พร้อมใช้งานใน Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="ad759-120">Multi-Geo is now also available in Power BI Embedded.</span></span> <span data-ttu-id="ad759-121">อ่านเพิ่มเติมที่[การสนับสนุน Multi-Geo ใน Power BI Embedded](../developer/embedded/embedded-multi-geo.md)</span><span class="sxs-lookup"><span data-stu-id="ad759-121">Read more at [Multi-Geo support in Power BI Embedded](../developer/embedded/embedded-multi-geo.md).</span></span>

> [!NOTE]
> <span data-ttu-id="ad759-122">Power BI Premium เพิ่งเปิดตัว Premium เวอร์ชันใหม่ชื่อ **Premium Gen2** ซึ่งกำลังอยู่ในช่วงการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="ad759-122">Power BI Premium recently released a new version of Premium, called **Premium Gen2**, which is currently in preview.</span></span> <span data-ttu-id="ad759-123">Premium Gen2 จะทำให้การจัดการความจุระดับพรีเมียมง่ายขึ้นและลดค่าใช้จ่ายในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="ad759-123">Premium Gen2 will simplify the management of Premium capacities, and reduce management overhead.</span></span> <span data-ttu-id="ad759-124">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Power BI Premium Generation 2 (ตัวอย่าง)](service-premium-what-is.md#power-bi-premium-generation-2-preview)</span><span class="sxs-lookup"><span data-stu-id="ad759-124">For more information, see [Power BI Premium Generation 2 (preview)](service-premium-what-is.md#power-bi-premium-generation-2-preview).</span></span>

## <a name="enable-and-configure"></a><span data-ttu-id="ad759-125">เปิดใช้งานและกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="ad759-125">Enable and configure</span></span>

<span data-ttu-id="ad759-126">เพื่อความจุใหม่ ๆ ให้เปิดใช้งาน Multi-Geo ด้วยการเลือกภูมิภาคนอกเหนือจากภูมิภาคเริ่มต้นจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="ad759-126">For new capacities, enable Multi-Geo by selecting a region other than the default region from the dropdown.</span></span>  <span data-ttu-id="ad759-127">ความจุที่ใช้ได้จะแสดงภูมิภาคที่พิกัดอยู่ อย่างเช่น **US ตอนกลางทางตะวันตก**</span><span class="sxs-lookup"><span data-stu-id="ad759-127">Each available capacity shows the region where it's currently located, such as **West Central US**.</span></span>

![ขนาดความจุ: เลือกภูมิภาค](media/service-admin-premium-multi-geo/power-bi-multi-geo-capacity-size.png)

<span data-ttu-id="ad759-130">หลังจากสร้างความจุแล้ว ความจุนั้นจะอยู่ในภูมิภาคนั้น และพื้นที่ทำงานใด ๆ ที่สร้างขึ้นจะเก็บเนื้อหาไว้ในภูมิภาคนั้น</span><span class="sxs-lookup"><span data-stu-id="ad759-130">After you've created capacity, it remains in that region, and any workspaces created will have their content stored in that region.</span></span> <span data-ttu-id="ad759-131">คุณสามารถย้ายพื้นที่ทำงานจากภูมิภาคหนึ่งไปยังอีกภูมิภาคผ่านเมนูแบบหล่นลงบนหน้าจอการตั้งค่าพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="ad759-131">You can migrate workspaces from one region to another through the dropdown on the workspace settings screen.</span></span>

![แก้ไขพื้นที่ทำงาน: เลือกความจุที่ใช้งานได้](media/service-admin-premium-multi-geo/power-bi-multi-geo-edit-workspace.png)

<span data-ttu-id="ad759-134">คุณเห็นข้อความนี้เพื่อยืนยันการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="ad759-134">You see this message to confirm the change.</span></span>

![เปลี่ยนการยืนยันพื้นที่ทำงานที่กำหนด](media/service-admin-premium-multi-geo/power-bi-multi-geo-change-assigned-workspace-capacity.png)

<span data-ttu-id="ad759-136">คุณไม่จำเป็นต้องรีเซ็ตข้อมูลประจำตัวเกตเวย์ในระหว่างการย้ายในเวลานี้</span><span class="sxs-lookup"><span data-stu-id="ad759-136">You don't need to reset the gateway credentials during a migration at this time.</span></span>  <span data-ttu-id="ad759-137">หลังจากที่ได้จัดเก็บไว้ในภูมิภาคความจุแบบ Premium แล้วคุณจะต้องทำการรีเซ็ตเมื่อทำการย้าย</span><span class="sxs-lookup"><span data-stu-id="ad759-137">After they're stored in the Premium capacity region, you will need to reset them upon migration.</span></span>

<span data-ttu-id="ad759-138">ในระหว่างการย้าย การดำเนินการบางอย่างอาจล้มเหลว อย่างเช่นการเผยแพร่ชุดข้อมูลใหม่หรือการกำหนดเวลารีเฟรชข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ad759-138">During migration, certain operations may fail, such as publishing new datasets or scheduled data refresh.</span></span>  

<span data-ttu-id="ad759-139">รายการต่อไปนี้จัดเก็บไว้ในภูมิภาค Premium เมื่อเปิดใช้งาน Multi-Geo:</span><span class="sxs-lookup"><span data-stu-id="ad759-139">The following items are stored in the Premium region when Multi-Geo is enabled:</span></span>

- <span data-ttu-id="ad759-140">โมเดล (ไฟล์ .ABF) สำหรับชุดข้อมูลนำเข้าหรือ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="ad759-140">Models (.ABF files) for import and Direct Query datasets</span></span>
- <span data-ttu-id="ad759-141">แคชคิวรี</span><span class="sxs-lookup"><span data-stu-id="ad759-141">Query cache</span></span>
- <span data-ttu-id="ad759-142">ภาพ R</span><span class="sxs-lookup"><span data-stu-id="ad759-142">R images</span></span>

<span data-ttu-id="ad759-143">รายการเหล่านั้นจะยังคงอยู่ในภูมิภาคเดิมของผู้เช่า:</span><span class="sxs-lookup"><span data-stu-id="ad759-143">These items remain in the home region for the tenant:</span></span>

- <span data-ttu-id="ad759-144">ส่งชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ad759-144">Push datasets</span></span>
- <span data-ttu-id="ad759-145">เวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="ad759-145">Excel workbooks</span></span>
- <span data-ttu-id="ad759-146">Metadata ของแดชบอร์ด/รายงาน: ตัวอย่างเช่น ชื่อไทล์ คิวรีไทล์</span><span class="sxs-lookup"><span data-stu-id="ad759-146">Dashboard/report metadata: e.g., tile names, tile queries</span></span>
- <span data-ttu-id="ad759-147">บัสบริการสำหรับคิวรีเกตเวย์หรืองานรีเฟรชที่กำหนดเวลาไว้</span><span class="sxs-lookup"><span data-stu-id="ad759-147">Service buses for gateway queries or scheduled refresh jobs</span></span>
- <span data-ttu-id="ad759-148">การอนุญาต</span><span class="sxs-lookup"><span data-stu-id="ad759-148">Permissions</span></span>
- <span data-ttu-id="ad759-149">ข้อมูลประจำตัวชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ad759-149">Dataset credentials</span></span>



## <a name="view-capacity-regions"></a><span data-ttu-id="ad759-150">ดูตำแหน่งที่ตั้งความจุ</span><span class="sxs-lookup"><span data-stu-id="ad759-150">View capacity regions</span></span>

<span data-ttu-id="ad759-151">ในพอร์ทัลผู้ดูแลระบบ คุณสามารถดูความจุทั้งหมดสำหรับผู้เช่า Power BI ของคุณและภูมิภาคที่พวกเขาอาศัยอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="ad759-151">In the Admin Portal, you can view all the capacities for your Power BI tenant and the regions where they're currently located.</span></span>

![ดูความจุแบบพรีเมียม](media/service-admin-premium-multi-geo/power-bi-multi-geo-premium-capacities.png) 

## <a name="change-the-region-for-existing-content"></a><span data-ttu-id="ad759-153">เปลี่ยนภูมิภาคสำหรับเนื้อหาที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="ad759-153">Change the region for existing content</span></span>

<span data-ttu-id="ad759-154">หากคุณต้องการเปลี่ยนภูมิภาคสำหรับเนื้อหาที่มีอยู่ คุณมีสองทางเลือก</span><span class="sxs-lookup"><span data-stu-id="ad759-154">If you need to change the region for existing content, you have two options.</span></span>

- <span data-ttu-id="ad759-155">สร้างความจุที่สองและย้ายพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="ad759-155">Create a second capacity and move workspaces.</span></span> <span data-ttu-id="ad759-156">ผู้ใช้ฟรีจะไม่พบระยะเวลาหยุดทำงานใด ๆ ตราบเท่าที่ผู้เช่ามี v-core สำรอง</span><span class="sxs-lookup"><span data-stu-id="ad759-156">Free users won't experience any downtime as long as the tenant has spare v-cores.</span></span>
- <span data-ttu-id="ad759-157">หากการสร้างความจุที่สองไม่ใช่ทางเลือกที่มี คุณสามารถย้ายเนื้อหากลับไปยังความจุที่แชร์กันจาก Premium ได้ชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="ad759-157">If creating a second capacity isn't an option, you can temporarily move the content back to shared capacity from Premium.</span></span> <span data-ttu-id="ad759-158">คุณไม่จำเป็นต้องมี v-core เพิ่ม แต่ผู้ใช้ฟรีจพบระยะเวลาหยุดทำงานบ้าง</span><span class="sxs-lookup"><span data-stu-id="ad759-158">You don't need extra v-cores, but free users will experience some downtime.</span></span>

## <a name="move-content-out-of-multi-geo"></a><span data-ttu-id="ad759-159">ย้ายเนื้อหาออกจาก Multi-Geo</span><span class="sxs-lookup"><span data-stu-id="ad759-159">Move content out of Multi-Geo</span></span>  

<span data-ttu-id="ad759-160">คุณสามารถนำพื้นที่ทำงานออกจากความจุ Multi-Geo ได้หนึ่งในสองวิธี:</span><span class="sxs-lookup"><span data-stu-id="ad759-160">You can take workspaces out of Multi-Geo capacity in one of two ways:</span></span>

- <span data-ttu-id="ad759-161">ลบความจุปัจจุบันที่พื้นที่ทำงานอยู่</span><span class="sxs-lookup"><span data-stu-id="ad759-161">Delete the current capacity where the workspace is located.</span></span>  <span data-ttu-id="ad759-162">การทำเช่นนี้จะย้ายพื้นที่ทำงานกลับไปยังความจุที่แชร์กันในภูมิภาคเดิม</span><span class="sxs-lookup"><span data-stu-id="ad759-162">This moves the workspace back to shared capacity in the home region.</span></span>
- <span data-ttu-id="ad759-163">ย้ายพื้นที่ทำงานเดี่ยวกลับไปยังความจุแบบ Premium ที่อยู่ผู้เช่าเดิม</span><span class="sxs-lookup"><span data-stu-id="ad759-163">Migrate individual workspaces back to Premium capacity located in the home tenant.</span></span>

<span data-ttu-id="ad759-164">ไม่ควรย้ายชุดข้อมูลรูปแบบพื้นที่จัดเก็บข้อมูลขนาดใหญ่ออกจากภูมิภาคที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="ad759-164">Large-storage format datasets should not be moved from the region where they were created.</span></span> <span data-ttu-id="ad759-165">รายงานที่ใช้ชุดข้อมูลรูปแบบขนาดใหญ่จะไม่สามารถโหลดชุดข้อมูลและส่งกลับข้อผิดพลาด *ไม่สามารถโหลดแบบจำลอง*</span><span class="sxs-lookup"><span data-stu-id="ad759-165">Reports based on a large-format dataset will not be able to load the dataset, and return a *Cannot load model* error.</span></span> <span data-ttu-id="ad759-166">ย้ายชุดข้อมูลรูปแบบพื้นที่เก็บข้อมูลขนาดใหญ่กลับไปที่ภูมิภาคเดิมเพื่อให้พร้อมใช้งานอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="ad759-166">Move the large-storage format dataset back to its original region to make it available again.</span></span>

## <a name="limitations-and-considerations"></a><span data-ttu-id="ad759-167">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="ad759-167">Limitations and considerations</span></span>

- <span data-ttu-id="ad759-168">ยืนยันว่าการเคลื่อนย้ายใด ๆ ที่คุณทำระหว่างภูมิภาคได้ปฏิบัติตามข้อกำหนดของรัฐบาลและบริษัทก่อนที่จะทำการโอนย้ายข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ad759-168">Confirm that any movement you initiate between regions follows all corporate and government compliance requirements prior to initiating data transfer.</span></span>
- <span data-ttu-id="ad759-169">คิวรีที่ได้รับการแคชที่เก็บอยู่ในภูมิภาคระยะไกลจะพักอยู่ในภูมิภาคนั้น</span><span class="sxs-lookup"><span data-stu-id="ad759-169">A cached query stored in a remote region stays in that region at rest.</span></span> <span data-ttu-id="ad759-170">อย่างไรก็ตาม ข้อมูลอื่นที่อยู่ในระหว่างการส่งต่ออาจเดินทางกลับไปกลับมาระหว่างเขตภูมิศาสตร์หลายเขต</span><span class="sxs-lookup"><span data-stu-id="ad759-170">However, other data in transit may go back and forth between multiple geographies.</span></span>
- <span data-ttu-id="ad759-171">เมื่อทำการย้ายข้อมูลจากภูมิภาคหนึ่งไปยังอีกภูมิภาคหนึ่งในสภาพแวดล้อม Multi-Geo ข้อมูลต้นทางอาจยังอยู่ในภูมิภาคที่ย้ายออกมานานถึง 30 วัน</span><span class="sxs-lookup"><span data-stu-id="ad759-171">When moving data from one region to another in a Multi-Geo environment, the source data may remain in the region from which the data was moved for up to 30 days.</span></span> <span data-ttu-id="ad759-172">ในระหว่างนั้นผู้ใช้ปลายทางจะไม่มีสิทธิ์เข้าถึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ad759-172">During that time end users don't have access to it.</span></span> <span data-ttu-id="ad759-173">ข้อมูลจะถูกลบออกจากภูมิภาคและทำลายในระยะเวลา 30 วันนั้น</span><span class="sxs-lookup"><span data-stu-id="ad759-173">It's removed from this region and destroyed during the 30-day period.</span></span>
- <span data-ttu-id="ad759-174">ข้อความคิวรีและการรับส่งผลลัพธ์คิวรีสำหรับรูปแบบข้อมูลที่นำเข้าไม่ได้ส่งผ่านภูมิภาคเดิม</span><span class="sxs-lookup"><span data-stu-id="ad759-174">Query text and query result traffic for imported data models does not transit through the home region.</span></span> <span data-ttu-id="ad759-175">เมตาดาต้าของรายงานยังมาจากภูมิภาคระยะไกล และบางสถานะการกำหนดเส้นทาง DNS อาจนำการรับส่งข้อมูลออกจากภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="ad759-175">The report metadata does still come from the remote region, and certain DNS routing states may take traffic out of the region.</span></span> 
- <span data-ttu-id="ad759-176">คุณลักษณะ[กระแสข้อมูล](../transform-model/dataflows/dataflows-introduction-self-service.md) ไม่ได้รับการสนับสนุนบน Multi-GEO ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="ad759-176">The [dataflows](../transform-model/dataflows/dataflows-introduction-self-service.md) feature is not supported on Multi-GEO at this time.</span></span>
- <span data-ttu-id="ad759-177">การย้ายชุดข้อมูลรูปแบบพื้นที่จัดเก็บขนาดใหญ่จากภูมิภาคที่สร้างขึ้นจะส่งผลให้รายงานไม่สามารถโหลดชุดข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="ad759-177">Moving large-storage format datasets from the region where they were created will result in reports failing to load the dataset.</span></span> <span data-ttu-id="ad759-178">ย้ายชุดข้อมูลพื้นที่เก็บข้อมูลขนาดใหญ่กลับไปที่ภูมิภาคเดิมเพื่อให้พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ad759-178">Move the large-storage dataset back to its original region to make it available.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="ad759-179">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="ad759-179">Next steps</span></span>

- [<span data-ttu-id="ad759-180">Power BI Premium คืออะไร?</span><span class="sxs-lookup"><span data-stu-id="ad759-180">What is Power BI Premium?</span></span>](service-premium-what-is.md)
- [<span data-ttu-id="ad759-181">Multi-Geo สำหรับความจุ Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="ad759-181">Multi-Geo for Power BI Embedded capacities</span></span>](../developer/embedded/embedded-multi-geo.md)

<span data-ttu-id="ad759-182">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="ad759-182">More questions?</span></span> [<span data-ttu-id="ad759-183">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="ad759-183">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)

<span data-ttu-id="ad759-184">Power BI ได้แนะนำ Power BI Premium Gen2 เข้ามาใช้งานเป็นข้อเสนอการแสดงตัวอย่าง ซึ่งปรับปรุงประสบการณ์การใช้งาน Power BI Premium ด้วยการปรับปรุงในสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ad759-184">Power BI has introduced Power BI Premium Gen2 as a preview offering, which improves the Power BI Premium experience with improvements in the following:</span></span>
* <span data-ttu-id="ad759-185">ประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="ad759-185">Performance</span></span>
* <span data-ttu-id="ad759-186">สิทธิการใช้งานต่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ad759-186">Per-user licensing</span></span>
* <span data-ttu-id="ad759-187">ขนาดใหญ่ขึ้น</span><span class="sxs-lookup"><span data-stu-id="ad759-187">Greater scale</span></span>
* <span data-ttu-id="ad759-188">เมตริกที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="ad759-188">Improved metrics</span></span>
* <span data-ttu-id="ad759-189">การปรับขนาดอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ad759-189">Autoscaling</span></span>
* <span data-ttu-id="ad759-190">ลดค่าใช้จ่ายในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="ad759-190">Reduced management overhead</span></span>

<span data-ttu-id="ad759-191">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI Premium Gen2 โปรดดูที่ [Power BI Premium Generation 2 (ตัวอย่าง)](service-premium-what-is.md#power-bi-premium-generation-2-preview)</span><span class="sxs-lookup"><span data-stu-id="ad759-191">For more information about Power BI Premium Gen2, see [Power BI Premium Generation 2 (preview)](service-premium-what-is.md#power-bi-premium-generation-2-preview).</span></span>
