---
title: การสนับสนุนหลายภูมิภาค (Multi-Geo) สำหรับการวิเคราะห์แบบฝังตัวของ Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังตัวที่ดีขึ้น
description: เรียนรู้วิธีปรับใช้เนื้อหาไปยังศูนย์ข้อมูลในภูมิภาคนอกเหนือจากภูมิภาคที่อยู่ของโซลูชันการวิเคราะห์แบบฝังตัวของ Power BI ใช้การสนับสนุนหลายภูมิภาค (Multi-Geo) เพื่อเพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังตัวที่ดีขึ้น
author: KesemSharabi
ms.author: kesharab
ms.reviewer: nishalit
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: how-to
ms.date: 02/05/2019
ms.openlocfilehash: 4b9aacb460966f633161238cae82ba6731196ed4
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888293"
---
# <a name="multi-geo-support-for-power-bi-embedded"></a><span data-ttu-id="558a8-104">การสนับสนุนหลายภูมิภาคสำหรับ Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="558a8-104">Multi-Geo support for Power BI Embedded</span></span>

<span data-ttu-id="558a8-105">**การสนับสนุนหลายภูมิภาคเพื่อ Power BI Embedded** หมายความว่า Isv และองค์กรที่สร้างแอปพลิเคชันโดยใช้ Power BI Embedded ฝังตัววิเคราะห์ลงในแอปของพวกเขา จะสามารถปรับใช้ข้อมูลของพวกเขาในภูมิภาคต่างๆ ได้ทั่วโลก</span><span class="sxs-lookup"><span data-stu-id="558a8-105">**Multi-Geo support for Power BI Embedded** means that ISVs and organizations that build applications using Power BI Embedded to embed analytics into their apps can now deploy their data in different regions around the world.</span></span>

<span data-ttu-id="558a8-106">ตอนนี้ลูกค้าที่ใช้ **Power BI Embedded** สามารถตั้งค่า **ความจุ** โดยใช้ตัวเลือก **หลายภูมิภาค** ตามคุณลักษณะและข้อจำกัดที่ [Power BI Premium สนับสนุน](../../admin/service-admin-premium-Multi-Geo.md)</span><span class="sxs-lookup"><span data-stu-id="558a8-106">Now customers using **Power BI Embedded** can set up an **A capacity** using **Multi-Geo** options, based on the same features and limitations that [Power BI Premium supports using Multi-Geo](../../admin/service-admin-premium-Multi-Geo.md).</span></span>

## <a name="creating-new-power-bi-embedded-capacity-resource-with-multi-geo"></a><span data-ttu-id="558a8-107">สร้างทรัพยากรความจุ Power BI Embedded ใหม่ด้วย Multi-Geo</span><span class="sxs-lookup"><span data-stu-id="558a8-107">Creating new Power BI Embedded Capacity resource with Multi-Geo</span></span>

<span data-ttu-id="558a8-108">ในหน้าจอ **สร้างทรัพยากร** คุณจำเป็นต้องเลือกตำแหน่งที่ตั้งของความจุของคุณ</span><span class="sxs-lookup"><span data-stu-id="558a8-108">In the **Create resource** screen, you need to choose the location of your capacity.</span></span> <span data-ttu-id="558a8-109">จนถึงตอนนี้ ความจุจะถูกจำกัดไว้ที่ตำแหน่งที่ตั้งของผู้เช่า Power BI ของคุณเท่านั้น ดังนั้นจึงสามารถใช้งานได้เฉพาะสถานที่เดียว</span><span class="sxs-lookup"><span data-stu-id="558a8-109">Until now, it was limited only to the location of your Power BI tenant, so only a single location was available.</span></span> <span data-ttu-id="558a8-110">ด้วย Multi-Geo คุณสามารถเลือกภูมิภาคต่างๆ เพื่อปรับใช้ความจุของคุณ</span><span class="sxs-lookup"><span data-stu-id="558a8-110">With Multi-Geo, you can choose between different regions to deploy your capacity.</span></span>

![ตั้งค่า Multi-Geo ของ Power BI Embedded](media/embedded-multi-geo/pbie-multi-geo-setup.png)

<span data-ttu-id="558a8-112">โปรดสังเกตว่า เมื่อเปิดเมนูดรอปดาวน์ตำแหน่งที่ตั้ง ตัวเลือกในค่าเริ่มต้นคือบ้านผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="558a8-112">Notice that when opening the location drop-down menu, your home tenant is the default selection.</span></span>
  
![ตำแหน่งที่ตั้งเริ่มต้นของ Multi-Geo ของ Power BI Embedded](media/embedded-multi-geo/pbie-multi-geo-default-location.png)

<span data-ttu-id="558a8-114">เมื่อเลือกตำแหน่งที่ตั้งอื่น ข้อความจะพร้อมท์ให้คุณทราบถึงสิ่งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="558a8-114">When choosing a different location, a message prompts you to make sure you're aware of the selection.</span></span>

![เปลี่ยนตำแหน่งที่ตั้ง](media/embedded-multi-geo/pbie-multi-geo-location-change.png)

## <a name="view-capacity-location"></a><span data-ttu-id="558a8-116">ดูตำแหน่งที่ตั้งความจุ</span><span class="sxs-lookup"><span data-stu-id="558a8-116">View Capacity location</span></span>

<span data-ttu-id="558a8-117">คุณสามารถดูตำแหน่งที่ตั้งความจุของคุณได้อย่างง่ายดายเมื่อไปที่หน้าการจัดการ Power BI Embedded หลัก ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="558a8-117">You can see your capacities location easily when going to the main Power BI Embedded management page in the Azure portal.</span></span>

![ความจุในตำแหน่งที่ตั้งอื่น](media/embedded-multi-geo/pbie-multi-geo-location-different.png)

<span data-ttu-id="558a8-119">จะพร้อมใช้งานในพอร์ทัลผู้ดูแลระบบใน Powerbi.com</span><span class="sxs-lookup"><span data-stu-id="558a8-119">It's also available in the Admin Portal in Powerbi.com.</span></span> <span data-ttu-id="558a8-120">ในพอร์ทัลผู้ดูแลระบบ เลือก 'ตั้งค่าความจุ' และจากนั้น สลับไปยังแท็บ 'Power BI Embedded '</span><span class="sxs-lookup"><span data-stu-id="558a8-120">In the Admin portal, choose 'Capacity settings,' and then switch to 'Power BI Embedded' tab.</span></span>

![ดูในพอร์ทัลผู้ดูแลระบบ](media/embedded-multi-geo/pbie-multi-geo-admin-portal.png)

[<span data-ttu-id="558a8-122">เรียนรู้เพิ่มเติมเกี่ยวกับการสร้างความจุด้วย Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="558a8-122">Learn more about creating capacities with Power BI Embedded.</span></span>](azure-pbie-create-capacity.md)

## <a name="manage-existing-capacities-location"></a><span data-ttu-id="558a8-123">จัดการตำแหน่งที่ตั้งความจุที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="558a8-123">Manage existing capacities location</span></span>

<span data-ttu-id="558a8-124">คุณไม่สามารถเปลี่ยนตำแหน่งที่ตั้งของทรัพยากรของ Power BI Embedded เมื่อคุณสร้างความจุใหม่</span><span class="sxs-lookup"><span data-stu-id="558a8-124">You can't change a Power BI Embedded resource location once you've created a new capacity.</span></span>

<span data-ttu-id="558a8-125">เมื่อต้องย้ายเนื้อหา Power BI ของคุณไปยังภูมิภาคอื่น ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="558a8-125">To move your Power BI content to a different region, follow these steps:</span></span>

1. <span data-ttu-id="558a8-126">[สร้างความจุใหม่](azure-pbie-create-capacity.md)ในภูมิภาคอื่น</span><span class="sxs-lookup"><span data-stu-id="558a8-126">[Create a new capacity](azure-pbie-create-capacity.md) in a different region.</span></span>

2. <span data-ttu-id="558a8-127">กำหนดพื้นที่ทำงานทั้งหมดจากความจุที่มีอยู่ให้กับความจุใหม่</span><span class="sxs-lookup"><span data-stu-id="558a8-127">Assign all workspaces from the existing capacity to the new capacity.</span></span>

3. <span data-ttu-id="558a8-128">ลบความจุเก่าหรือหยุดชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="558a8-128">Delete or pause the old capacity.</span></span>

<span data-ttu-id="558a8-129">สิ่งสำคัญคือ ถ้าคุณตัดสินใจที่จะลบความจุโดยไม่กำหนดเนื้อหาของความจุนั้นใหม่ เนื้อหาทั้งหมดจะย้ายไปยังความจุที่แชร์ร่วมกัน ซึ่งอยู่ในภูมิภาคบ้านของคุณ</span><span class="sxs-lookup"><span data-stu-id="558a8-129">It's important to note that if you decide to delete a capacity without reassigning its content, all the content in that capacity moves to a shared capacity, which is in your home region.</span></span>

## <a name="api-support-for-multi-geo"></a><span data-ttu-id="558a8-130">การสนับสนุน API สำหรับ Multi-Geo</span><span class="sxs-lookup"><span data-stu-id="558a8-130">API support for Multi-Geo</span></span>

<span data-ttu-id="558a8-131">เพื่อสนับสนุนการจัดการความจุด้วย Multi-Geo ผ่าน API เราได้ทำการเปลี่ยนแปลง API ที่มีอยู่:</span><span class="sxs-lookup"><span data-stu-id="558a8-131">To support management of capacities with Multi-Geo through API, we have made some changes to existing APIs:</span></span>

1. <span data-ttu-id="558a8-132">**[รับความจุ](/rest/api/power-bi/capacities/getcapacities)** - API จะส่งกลับรายการความจุพร้อมด้วยการเข้าถึงให้แก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="558a8-132">**[Get Capacities](/rest/api/power-bi/capacities/getcapacities)** - The API returns a list of capacities with access to the user.</span></span> <span data-ttu-id="558a8-133">การตอบสนองตอนนี้มีคุณสมบัติเพิ่มเติมที่เรียกว่า 'ภูมิภาค' ที่ระบุตำแหน่งที่ตั้งของความจุ</span><span class="sxs-lookup"><span data-stu-id="558a8-133">The response now includes an additional property called 'region,' that specifies the capacity's location.</span></span>

2. <span data-ttu-id="558a8-134">**[กำหนดความจุ](/rest/api/power-bi/capacities)** - API จะอนุญาตให้กำหนดพื้นที่ทำงานให้กับความจุ</span><span class="sxs-lookup"><span data-stu-id="558a8-134">**[Assign To Capacity](/rest/api/power-bi/capacities)** - The API allows assigning a given workspace to a capacity.</span></span> <span data-ttu-id="558a8-135">การดำเนินการนี้ไม่อนุญาตให้คุณกำหนดพื้นที่ทำงานให้กับความจุภายนอกภูมิภาคบ้านของคุณ หรือย้ายพื้นที่ทำงานระหว่างความจุในภูมิภาคอื่น</span><span class="sxs-lookup"><span data-stu-id="558a8-135">This operation doesn't allow you to assign workspaces to a capacity outside of your home region or move workspaces between capacities in different regions.</span></span> <span data-ttu-id="558a8-136">เมื่อต้องดำเนินการนี้ ผู้ใช้หรือ[บริการหลัก](embed-service-principal.md)ยังคงต้องใช้สิทธิ์ระดับผู้ดูแลระบบบนพื้นที่ทำงาน และจัดการและกำหนดสิทธิ์บนความจุเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="558a8-136">To perform this operation, the user or [service principal](embed-service-principal.md) still needs admin permissions on the workspace, and admin or assign permissions on the target capacity.</span></span>

3. <span data-ttu-id="558a8-137">**[ Azure Resource Manager API](/rest/api/power-bi-embedded/capacities)** - :ซึ่งเป็นตัวดำเนินการ API การจัดการทรัพยากร Azure ทั้งหมด รวมทั้ง *สร้าง* และ *ลบ* ให้การสนับสนุน Multi-Geo</span><span class="sxs-lookup"><span data-stu-id="558a8-137">**[Azure Resource Manager API](/rest/api/power-bi-embedded/capacities)** - all of the Azure Resource Manager API operations, including *Create* and *Delete*, supports Multi-Geo.</span></span>

## <a name="limitations-and-considerations"></a><span data-ttu-id="558a8-138">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="558a8-138">Limitations and considerations</span></span>

* <span data-ttu-id="558a8-139">ยืนยันว่า การโยกย้ายที่คุณเริ่มต้นระหว่างภูมิภาคปฏิบัติตามข้อบังคับของบริษัทและภาครัฐของก่อนเริ่มต้นการถ่ายโอนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="558a8-139">Confirm that any movement you initiate between regions follows all corporate and government compliance requirements before initiating data transfer.</span></span>

* <span data-ttu-id="558a8-140">คิวรีที่ได้รับการแคชที่เก็บอยู่ในภูมิภาคระยะไกลจะพักอยู่ในภูมิภาคนั้น</span><span class="sxs-lookup"><span data-stu-id="558a8-140">A cached query stored in a remote region stays in that region at rest.</span></span> <span data-ttu-id="558a8-141">อย่างไรก็ตาม ข้อมูลอื่นๆ ในการส่งต่ออาจไปกลับมาระระหว่างพื้นที่ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="558a8-141">However, other data in transit may go back and forth between different geographies.</span></span>

* <span data-ttu-id="558a8-142">เมื่อมีการย้ายข้อมูลจากภูมิภาคหนึ่งไปอีกภูมิภาคหนึ่งในสภาพแวดล้อมของ Multi-Geo ข้อมูลต้นทางอาจอยู่ในภูมิภาคที่ใช้เวลาย้ายนานถึง 30 วัน</span><span class="sxs-lookup"><span data-stu-id="558a8-142">When moving data from one region to another in a Multi-Geo environment, the source data may stay in the region from which the data was moved for up to 30 days.</span></span> <span data-ttu-id="558a8-143">ในช่วงเวลาดังกล่าว ผู้ใช้ไม่สามารถเข้าถึงข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="558a8-143">During that time, users don't have access to it.</span></span> <span data-ttu-id="558a8-144">ข้อมูลจะถูกลบออกจากภูมิภาคและทำลายในระยะเวลา 30 วันนั้น</span><span class="sxs-lookup"><span data-stu-id="558a8-144">It's removed from this region and destroyed during the 30-day period.</span></span>

* <span data-ttu-id="558a8-145">Multi-Geo ไม่ได้ส่งผลให้เกิดประสิทธิภาพที่ดีขึ้นโดยทั่วไป</span><span class="sxs-lookup"><span data-stu-id="558a8-145">Multi-Geo doesn't result in better performance in general.</span></span> <span data-ttu-id="558a8-146">การโหลดรายงานและแดชบอร์ดยังเกี่ยวข้องกับคำร้องขอเมต้าดาต้าไปยังภูมิภาคบ้าน</span><span class="sxs-lookup"><span data-stu-id="558a8-146">Loading reports and dashboards still involve requests to the home region for metadata.</span></span>

* <span data-ttu-id="558a8-147">ในการฝังสำหรับสถานการณ์ลูกค้าของคุณข้อความคิวรีและผลลัพธ์คิวรีจะดำเนินการขนส่งต่อไปผ่านผู้เช่าหน้าแรก</span><span class="sxs-lookup"><span data-stu-id="558a8-147">In an embedding for your customers scenario, query text and query result continue to transit through the home tenant.</span></span>

## <a name="next-steps"></a><span data-ttu-id="558a8-148">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="558a8-148">Next steps</span></span>

<span data-ttu-id="558a8-149">เรียนรู้เพิ่มเติมเกี่ยวกับความจุ Power BI Embedded และตัวเลือก Multi-Geo สำหรับความจุทั้งหมด โดยอ้างอิงลิงก์ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="558a8-149">Learn more about Power BI Embedded capacities and Multi-Geo options for all capacities by referencing the links below.</span></span>

* [<span data-ttu-id="558a8-150">Power BI Embedded คืออะไร</span><span class="sxs-lookup"><span data-stu-id="558a8-150">What is Power BI Embedded?</span></span>](azure-pbie-what-is-power-bi-embedded.md)

* [<span data-ttu-id="558a8-151">สร้างความจุ Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="558a8-151">Create a Power BI Embedded capacity</span></span>](azure-pbie-create-capacity.md)

* [<span data-ttu-id="558a8-152">Multi-Geo ในความจุ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="558a8-152">Multi-Geo in Power BI Premium capacities</span></span>](../../admin/service-admin-premium-multi-geo.md)

<span data-ttu-id="558a8-153">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="558a8-153">More questions?</span></span> [<span data-ttu-id="558a8-154">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="558a8-154">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)