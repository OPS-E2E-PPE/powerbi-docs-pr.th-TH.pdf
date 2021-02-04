---
title: กำหนดค่าการตั้งค่าการโต้ตอบของรายงาน
description: เรียนรู้วิธีการแทนที่การตั้งค่าการโต้ตอบค่าเริ่มต้นสำหรับรายงาน
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 03/08/2020
ms.openlocfilehash: fdafc1cd5804bf62a715dc4161ce853c2690ce3a
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414656"
---
# <a name="configure-report-interaction-settings"></a><span data-ttu-id="cf1a6-103">กำหนดค่าการตั้งค่าการโต้ตอบของรายงาน</span><span class="sxs-lookup"><span data-stu-id="cf1a6-103">Configure report interaction settings</span></span>

## <a name="overview"></a><span data-ttu-id="cf1a6-104">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="cf1a6-104">Overview</span></span>

<span data-ttu-id="cf1a6-105">แอป Power BI สำหรับอุปกรณ์เคลื่อนที่มีจำนวนการตั้งค่า "การโต้ตอบ" ที่สามารถกำหนดค่าได้ที่ช่วยให้คุณสามารถควบคุมวิธีการที่คุณโต้ตอบกับข้อมูลของคุณ และเพื่อกำหนดวิธีที่องค์ประกอบบางอย่างในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="cf1a6-105">The Power BI mobile app has a number of configurable "interaction" settings that enable you to control how you interact with your data, and to define how some elements in the Power BI mobile app behave.</span></span> <span data-ttu-id="cf1a6-106">ตารางด้านล่างแสดงการตั้งค่าการโต้ตอบที่พร้อมใช้งานและอุปกรณ์ที่มีอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="cf1a6-106">The table below shows the interaction settings that are currently available and the devices which have them.</span></span>

| <span data-ttu-id="cf1a6-107">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="cf1a6-107">Setting</span></span> | <span data-ttu-id="cf1a6-108">โทรศัพท์ Android</span><span class="sxs-lookup"><span data-stu-id="cf1a6-108">Android phone</span></span> | <span data-ttu-id="cf1a6-109">iPhone</span><span class="sxs-lookup"><span data-stu-id="cf1a6-109">iPhone</span></span> | <span data-ttu-id="cf1a6-110">แท็บเล็ต Android</span><span class="sxs-lookup"><span data-stu-id="cf1a6-110">Android tablet</span></span>  | <span data-ttu-id="cf1a6-111">iPad</span><span class="sxs-lookup"><span data-stu-id="cf1a6-111">iPad</span></span> |
|---------|:-:|:-:|:-:|:-:|
| [<span data-ttu-id="cf1a6-112">การโต้ตอบแบบแตะครั้งเดียวเทียบกับการโต้ตอบแบบแตะสองครั้งบนวิชวลรายงาน</span><span class="sxs-lookup"><span data-stu-id="cf1a6-112">Single versus double tap interaction on report visuals</span></span>](#single-tap) |<span data-ttu-id="cf1a6-113">✔</span><span class="sxs-lookup"><span data-stu-id="cf1a6-113">✔</span></span>|<span data-ttu-id="cf1a6-114">✔</span><span class="sxs-lookup"><span data-stu-id="cf1a6-114">✔</span></span>|||
| [<span data-ttu-id="cf1a6-115">การเลือกหลายรายการเทียบกับการเลือกจุดข้อมูลเพียงครั้งเดียวบนการแสดงผลด้วย รายงานวีชวล</span><span class="sxs-lookup"><span data-stu-id="cf1a6-115">Multi-select versus single select of data points on report visuals</span></span>](#multi-select) |<span data-ttu-id="cf1a6-116">✔</span><span class="sxs-lookup"><span data-stu-id="cf1a6-116">✔</span></span>|<span data-ttu-id="cf1a6-117">✔</span><span class="sxs-lookup"><span data-stu-id="cf1a6-117">✔</span></span>|<span data-ttu-id="cf1a6-118">✔</span><span class="sxs-lookup"><span data-stu-id="cf1a6-118">✔</span></span>|<span data-ttu-id="cf1a6-119">✔</span><span class="sxs-lookup"><span data-stu-id="cf1a6-119">✔</span></span>|
| [<span data-ttu-id="cf1a6-120">ส่วนท้ายของรายงานที่เทียบกับรายงานแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="cf1a6-120">Docked versus dynamic report footer</span></span>](#docked-report-footer) |<span data-ttu-id="cf1a6-121">✔</span><span class="sxs-lookup"><span data-stu-id="cf1a6-121">✔</span></span>|<span data-ttu-id="cf1a6-122">✔</span><span class="sxs-lookup"><span data-stu-id="cf1a6-122">✔</span></span>|||
| [<span data-ttu-id="cf1a6-123">ปุ่มการรีเฟรชรายงานปุ่มแบบดึงลง </span><span class="sxs-lookup"><span data-stu-id="cf1a6-123">Button-initiated report refresh versus pull-to-refresh</span></span>](#report-refresh) |<span data-ttu-id="cf1a6-124">✔</span><span class="sxs-lookup"><span data-stu-id="cf1a6-124">✔</span></span>||||

<span data-ttu-id="cf1a6-125">เมื่อต้องการไปที่การตั้งค่าการโต้ตอบ ให้แตะรูปภาพโปรไฟล์ของคุณเพื่อเปิด [แผงด้านข้าง](./mobile-apps-home-page.md#header) เลือก **การตั้งค่า** และค้นหาส่วน **การโต้ตอบ**</span><span class="sxs-lookup"><span data-stu-id="cf1a6-125">To get to the interaction settings, tap your profile picture to open the [side panel](./mobile-apps-home-page.md#header), choose **Settings**, and find the **Interaction** section.</span></span>

![การตั้งค่าการโต้ตอบ](./media/mobile-app-interaction-settings/powerbi-mobile-app-interactions-section.png)

<span data-ttu-id="cf1a6-127">การตั้งค่าการโต้ตอบได้รับการอธิบายไว้ในส่วนด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="cf1a6-127">The interaction settings are described in the sections below.</span></span>

## <a name="interaction-settings"></a><span data-ttu-id="cf1a6-128">การตั้งค่าการโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="cf1a6-128">Interaction settings</span></span>

### <a name="single-tap"></a><span data-ttu-id="cf1a6-129">แตะครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="cf1a6-129">Single tap</span></span>
<span data-ttu-id="cf1a6-130">เมื่อคุณดาวน์โหลดแอป Power BI สำหรับอุปกรณ์เคลื่อนที่ จะมีการตั้งค่าสำหรับการโต้ตอบแบบแตะครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="cf1a6-130">When you download the Power BI mobile app, it is set for single tap interaction.</span></span> <span data-ttu-id="cf1a6-131">ซึ่งหมายความว่าเมื่อคุณแตะในวิชวลเพื่อทำการดำเนินการบางอย่างเช่น การเลือกรายการตัวแบ่งส่วนข้อมูล การเน้นข้าม การคลิกที่ลิงก์หรือปุ่ม ฯลฯ การแตะทั้งสองเลือกวิชวลและดำเนินการตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="cf1a6-131">This means that when you tap in a visual to do some action, such as selecting a slicer item, cross highlighting, clicking on a link or button, etc., the tap both selects the visual and performs the action you wanted.</span></span>

<span data-ttu-id="cf1a6-132">ถ้าคุณต้องการ คุณสามารถปิดการโต้ตอบแบบแตะครั้งเดียวได้</span><span class="sxs-lookup"><span data-stu-id="cf1a6-132">If you prefer, you can switch off single tap interaction.</span></span> <span data-ttu-id="cf1a6-133">จากนั้นคุณจะสามารถใช้การแตะแบบสองครั้งได้</span><span class="sxs-lookup"><span data-stu-id="cf1a6-133">You then have double-tap interaction.</span></span> <span data-ttu-id="cf1a6-134">ด้วยการแตะสองครั้ง การแตะครั้งแรกที่วิชวลเพื่อเลือก และจากนั้นแตะอีกครั้งในวิชวลเพื่อดำเนินการตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="cf1a6-134">With double tap interaction, you first tap on a visual to select it, and then tap again in the visual to perform your desired action.</span></span>

### <a name="multi-select"></a><span data-ttu-id="cf1a6-135">เลือกหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="cf1a6-135">Multi-select</span></span>

<span data-ttu-id="cf1a6-136">ตัวเลือกแบบหลายตัวเลือกทำให้สามารถเลือกจุดข้อมูลหลาย ๆ จุดในหน้ารายงานได้</span><span class="sxs-lookup"><span data-stu-id="cf1a6-136">The multi-select option makes it possible to select multiple data points on a report page.</span></span> <span data-ttu-id="cf1a6-137">เมื่อเปิดใช้งานการเลือกได้หลายจุดข้อมูล แต่ละจุดที่คุณแตะจะถูกเพิ่มไปยังจุดข้อมูลอื่นที่เลือกพร้อมกับผลลัพธ์ที่รวมกันจะถูกไฮไลท์โดยอัตโนมัติในทุกๆ ภาพของหน้า</span><span class="sxs-lookup"><span data-stu-id="cf1a6-137">When multi-select is turned on, each data point you tap gets added to the other selected data points, with the combined results automatically highlighted in all the visuals on the page.</span></span> <span data-ttu-id="cf1a6-138">เมื่อเลือกหลายรายการปิดเมื่อคุณแตะเพื่อเลือกจุดข้อมูลการเลือกใหม่จะแทนที่การเลือกปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="cf1a6-138">When multi-select is off, when you tap to select a data point, the new selection replaces the current selection.</span></span>

<span data-ttu-id="cf1a6-139">หากต้องการยกเลิกการเลือกจุดข้อมูลให้แตะอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="cf1a6-139">To unselect a data point, tap it again.</span></span>

>[!NOTE]
><span data-ttu-id="cf1a6-140">การเลือกหลายรายการไม่ได้รับการสนับสนุนในวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="cf1a6-140">Multi-select is not supported in Power BI visuals.</span></span>
>
><span data-ttu-id="cf1a6-141">โหมดการเลือกได้หลายจุดข้อมูลจะได้รับการรองรับบนเซิร์ฟเวอร์รายงาน Power BI ในรุ่นเซิร์ฟเวอร์รายงานถัดไป</span><span class="sxs-lookup"><span data-stu-id="cf1a6-141">Multi-select mode will be supported on Power BI Report Server in the next Report Server release.</span></span>

### <a name="docked-report-footer"></a><span data-ttu-id="cf1a6-142">เทียบส่วนท้ายของรายงาน</span><span class="sxs-lookup"><span data-stu-id="cf1a6-142">Docked report footer</span></span>

<span data-ttu-id="cf1a6-143">การตั้งค่าส่วนท้ายของรายงานที่เทียบชิดขอบจะกำหนดว่าส่วนท้ายรายงานยังคงเทียบชิดขอบหรือไม่ (เช่น คงที่และมองเห็นได้เสมอ) ที่ด้านล่างของรายงาน หรือซ่อนและปรากฏขึ้นใหม่ตามการดำเนินการของคุณในรายงานเช่น การเลื่อน</span><span class="sxs-lookup"><span data-stu-id="cf1a6-143">The docked report footer setting determines whether the report footer remains docked (i.e. fixed and always visible) at the bottom of the report, or hides and reappears based on your actions in the report, such as scrolling.</span></span>

<span data-ttu-id="cf1a6-144">บนโทรศัพท์ Android การตั้งค่าส่วนท้ายของรายงานที่เทียบชิดขอบจะ **เปิด** ตามค่าเริ่มต้น ซึ่งหมายความว่าส่วนท้ายของรายงานจะถูกเทียบชิดขอบและแสดงอยู่ที่ด้านล่างของรายงานเสมอ</span><span class="sxs-lookup"><span data-stu-id="cf1a6-144">On Android phones the docked report footer setting is **on** by default, meaning that the report footer is docked and always visible at the bottom of the report.</span></span> <span data-ttu-id="cf1a6-145">สลับการตั้งค่าเป็น **ปิด** ถ้าคุณต้องการให้ส่วนท้ายรายงานแบบไดนามิกที่ปรากฏและหายไป โดยขึ้นอยู่กับการดำเนินการของคุณในรายงาน</span><span class="sxs-lookup"><span data-stu-id="cf1a6-145">Switch the setting to **off** if you prefer a dynamic report footer that appears and disappears, depending on your actions on the report.</span></span>

### <a name="report-refresh"></a><span data-ttu-id="cf1a6-146">การรีเฟรชรายงาน</span><span class="sxs-lookup"><span data-stu-id="cf1a6-146">Report refresh</span></span>

<span data-ttu-id="cf1a6-147">การตั้งค่าการรีเฟรชรายงานจะกำหนดวิธีการเริ่มต้นรีเฟรชรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="cf1a6-147">The report refresh setting defines how you initiate report refreshes.</span></span> <span data-ttu-id="cf1a6-148">คุณสามารถเลือกจะเพิ่มปุ่มรีเฟรชลงในส่วนหัวของรายงานทั้งหมด หรือใช้การดำเนินการดึงเพื่อรีเฟรช (ดึงลงเล็กน้อยจากบนลงล่าง) ในหน้ารายงานเพื่อรีเฟรชรายงาน</span><span class="sxs-lookup"><span data-stu-id="cf1a6-148">You can choose either to have a refresh button on all report headers, or to use the pull-to-refresh action (pulling down slightly from top to bottom) on the report page to refresh the report.</span></span> <span data-ttu-id="cf1a6-149">รูปด้านล่างแสดงทางเลือกสองทาง</span><span class="sxs-lookup"><span data-stu-id="cf1a6-149">The figure below illustrates the two alternatives.</span></span> 

![ปุ่มรีเฟรชเทียบกับการดึงเพื่อรีเฟรช](./media/mobile-app-interaction-settings/powerbi-mobile-app-interactions-refresh-button-versus-pull.png)

<span data-ttu-id="cf1a6-151">บนโทรศัพท์ Android ปุ่มรีเฟรชจะถูกเพิ่มตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="cf1a6-151">On Android phones a refresh button is added by default.</span></span>

<span data-ttu-id="cf1a6-152">เมื่อต้องการเปลี่ยนการตั้งค่าการรีเฟรชรายงาน ให้ไปที่รายการรีเฟรชรายงานในการตั้งค่าการโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="cf1a6-152">To change the report refresh setting, go to the report refresh item in the interaction settings.</span></span> <span data-ttu-id="cf1a6-153">การตั้งค่าปัจจุบันจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="cf1a6-153">The current setting is shown.</span></span> <span data-ttu-id="cf1a6-154">แตะค่าเพื่อเปิดป็อปอัพที่คุณสามารถเลือกค่าใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="cf1a6-154">Tap the value to open a pop-up where you can choose a new value.</span></span>

![ตั้งค่ารีเฟรช](./media/mobile-app-interaction-settings/powerbi-mobile-app-interactions-set-refresh.png)

## <a name="remote-configuration"></a><span data-ttu-id="cf1a6-156">การกำหนดค่าระยะไกล</span><span class="sxs-lookup"><span data-stu-id="cf1a6-156">Remote configuration</span></span>

<span data-ttu-id="cf1a6-157">การโต้ตอบยังสามารถกำหนดค่าจากระยะไกลโดยผู้ดูแลระบบโดยใช้เครื่องมือ MDM ที่มีไฟล์การกำหนดค่าแอป</span><span class="sxs-lookup"><span data-stu-id="cf1a6-157">Interactions can also be configured remotely by an administrator using an MDM tool with an app configuration file.</span></span> <span data-ttu-id="cf1a6-158">ด้วยวิธีนี้ คุณสามารถปรับมาตรฐานประสบการณ์การโต้ตอบรายงานทั่วทั้งองค์กร หรือกลุ่มผู้ใช้เฉพาะในองค์กร</span><span class="sxs-lookup"><span data-stu-id="cf1a6-158">In this way it is possible to standardize the report interaction experience across the organization or for specific groups of users in the organization.</span></span> <span data-ttu-id="cf1a6-159">ดู [กำหนดค่าการโต้ตอบโดยใช้การจัดการอุปกรณ์เคลื่อนที่](./mobile-app-configuration.md) สำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="cf1a6-159">See [Configure interaction using mobile device management](./mobile-app-configuration.md) for detail.</span></span>


## <a name="next-steps"></a><span data-ttu-id="cf1a6-160">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="cf1a6-160">Next steps</span></span>
* [<span data-ttu-id="cf1a6-161">การตอบโต้กับรายงาน</span><span class="sxs-lookup"><span data-stu-id="cf1a6-161">Interacting with reports</span></span>](./mobile-reports-in-the-mobile-apps.md#interact-with-reports)
* [<span data-ttu-id="cf1a6-162">กำหนดค่าการโต้ตอบโดยใช้การจัดการอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="cf1a6-162">Configure interaction using mobile device management</span></span>](./mobile-app-configuration.md)
