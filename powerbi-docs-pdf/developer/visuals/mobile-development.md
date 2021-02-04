---
title: การพัฒนาบนอุปกรณ์เคลื่อนที่ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: วิธีการสร้างวิชวล Power BI ที่เหมาะกับอุปกรณ์เคลื่อนที่ เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: how-to
ms.date: 03/12/2019
ms.openlocfilehash: 63d2366f91398878af231c8dbb6ed07e8e623a03
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97885556"
---
# <a name="how-to-create-mobile-friendly-power-bi-visuals"></a><span data-ttu-id="4bb85-104">วิธีการสร้างวิชวล Power BI ที่ใช้งานง่ายบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="4bb85-104">How to create mobile-friendly Power BI visuals</span></span>
<span data-ttu-id="4bb85-105">การใช้อุปกรณ์เคลื่อนมีบทบาทสำคัญใน Power BI</span><span class="sxs-lookup"><span data-stu-id="4bb85-105">Mobile consumption has a major role in Power BI.</span></span> <span data-ttu-id="4bb85-106">หนึ่งในจุดแข็งคือการที่สามารถเชื่อมต่อกับข้อมูลของคุณได้ทุกที่ทุกเวลา</span><span class="sxs-lookup"><span data-stu-id="4bb85-106">One of its strengths is staying connected to your data anytime, anywhere.</span></span>

<span data-ttu-id="4bb85-107">ในฐานะนักพัฒนาที่สร้างวิชวล Power BI ข้อจำกัดที่ไม่ซ้ำกันของอุปกรณ์เคลื่อนที่แต่ละรายการจะต้องได้รับการแก้ไขเพื่อให้เข้าถึงผู้ใช้มากที่สุดเท่าที่เป็นไปได้ และมอบประสบการณ์การใช้งานบนอุปกรณ์เคลื่อนที่ที่ยอดเยี่ยม</span><span class="sxs-lookup"><span data-stu-id="4bb85-107">As a developer creating Power BI visuals, the unique constraints of each mobile device must be addressed to reach as many users as possible, and provide the best mobile experience.</span></span>

<span data-ttu-id="4bb85-108">ใช้ [แอป Power BI สำหรับ Windows, iOS และ Android](../../consumer/mobile/mobile-apps-for-mobile-devices.md) เพื่อให้ผู้ใช้ทางธุรกิจของคุณสามารถดูข้อมูลที่ครอบคลุมของพวกเขาได้ในขณะเดินทางเพียงปลายนิ้วสัมผัส</span><span class="sxs-lookup"><span data-stu-id="4bb85-108">Use the [Power BI app for Windows, iOS, and Android](../../consumer/mobile/mobile-apps-for-mobile-devices.md) to give your business users a comprehensive view of their data on the go, at the touch of their fingertips.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bb85-109">ข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="4bb85-109">Requirements</span></span>

<span data-ttu-id="4bb85-110">ข้อกำหนดต่อไปนี้เป็นสิ่งจำเป็นสำหรับการพัฒนาวิชวลที่ใช้งานง่ายบนอุปกรณ์เคลื่อนที่:</span><span class="sxs-lookup"><span data-stu-id="4bb85-110">The following requirements are essential for mobile friendly visual development:</span></span>

- <span data-ttu-id="4bb85-111">แสดง</span><span class="sxs-lookup"><span data-stu-id="4bb85-111">Render</span></span>

  <span data-ttu-id="4bb85-112">วิชวล Power BI ของคุณต้องแสดงบนอุปกรณ์เคลื่อนที่ที่รองรับทั้งหมด รวมถึงเบราว์เซอร์และแอปพลิเคชันที่รองรับโดยไม่มีข้อผิดพลาดในรายงาน แดชบอร์ด หรือเมื่อทำงานในโหมด **โฟกัส**</span><span class="sxs-lookup"><span data-stu-id="4bb85-112">Your Power BI visuals has to render on all supported mobile devices, including supported browsers and applications, with no errors in reports, dashboards, or when running in **Focus** mode.</span></span> 

- <span data-ttu-id="4bb85-113">แบบโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="4bb85-113">Interactive</span></span>

  <span data-ttu-id="4bb85-114">ฟังก์ชันการทำงานแบบโต้ตอบจะต้องได้รับการระบุไว้ในลักษณะเดียวกับที่ระบุไว้้สำหรับอุปกรณ์เดสก์ท็อป</span><span class="sxs-lookup"><span data-stu-id="4bb85-114">Interactive functionality must be provided in the same way as it's provided for desktop devices.</span></span> <span data-ttu-id="4bb85-115">เหตุการณ์ทั้งหมดที่จัดการบนเบราว์เซอร์บนเดสก์ท็อปต้องได้รับการสนับสนุน หรือมีตัวจัดการเหตุการณ์ที่เปรียบเทียบได้สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="4bb85-115">All events handled on desktop browsers must be supported, or have comparable event handlers for mobile devices.</span></span>
  
  <span data-ttu-id="4bb85-116">ตัวอย่างเช่น การนำทางพื้นฐานและการเลือกจุดข้อมูลควรมีฟังก์ชันการทำงานเหมือนกับในเบราว์เซอร์เดสก์ท็อป</span><span class="sxs-lookup"><span data-stu-id="4bb85-116">For example, basic navigation and the selection of data points, should have the same functionality as in desktop browsers.</span></span> <span data-ttu-id="4bb85-117">ถ้าวิชวลรองรับการเลือกหลายรายการโดยใช้ **Ctrl** นักพัฒนาจำเป็นต้องพิจารณาเพิ่มตัวจัดการเหตุการณ์ที่คล้ายกันสำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="4bb85-117">If a visual supports multi-select using **Ctrl**, the developer needs to consider adding a similar event handler for mobile devices.</span></span>

  <span data-ttu-id="4bb85-118">ตารางต่อไปนี้แสดงรายการเหตุการณ์ที่สอดคล้องกันบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="4bb85-118">The following table provides a list of corresponding events on mobile devices.</span></span>

  | <span data-ttu-id="4bb85-119">ชื่อเหตุการณ์ของเมาส์</span><span class="sxs-lookup"><span data-stu-id="4bb85-119">Mouse event name</span></span> | <span data-ttu-id="4bb85-120">ชื่อเหตุการณ์ของการสัมผัส</span><span class="sxs-lookup"><span data-stu-id="4bb85-120">Touch event name</span></span> |
  |:----------------:|:----------------:|
  | `click` | `click` |
  | `mousemove` | `touchmove` |
  | `mousedown` | `touchstart` |
  | `mouseup` | `touchend` |
  | `dblclick` | <span data-ttu-id="4bb85-121">ใช้ไลบรารีภายนอก</span><span class="sxs-lookup"><span data-stu-id="4bb85-121">use external library</span></span> |
  | `contextmenu` | <span data-ttu-id="4bb85-122">ใช้ไลบรารีภายนอก</span><span class="sxs-lookup"><span data-stu-id="4bb85-122">use external library</span></span> |
  | `mouseover` | `touchmove` |
  | `mouseout` | <span data-ttu-id="4bb85-123">`touchmove` (หรือไลบรารีภายนอก)</span><span class="sxs-lookup"><span data-stu-id="4bb85-123">`touchmove` (or external library)</span></span> |
  | `wheel` | `NaN` |

  > [!NOTE]
  > <span data-ttu-id="4bb85-124">ไม่ใช่ว่าอุปกรณ์เคลื่อนที่หรือหน้าจอสัมผัสทั้งหมดจะรองรับเหตุการณ์ของเมาส์ (หรือ *เมาส์* ที่นำหน้า)</span><span class="sxs-lookup"><span data-stu-id="4bb85-124">Not all mobile or touch screen devices support mouse (or *mouse* prefixed) events.</span></span> <span data-ttu-id="4bb85-125">ในกรณีดังกล่าว ให้จัดการทั้งเหตุการณ์ของ *เมาส์* และ *การสัมผัส* ในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="4bb85-125">In such cases, handle both *mouse* and *touch* events at the same time.</span></span>

## <a name="optional"></a><span data-ttu-id="4bb85-126">เลือกหรือไม่เลือกก็ได้</span><span class="sxs-lookup"><span data-stu-id="4bb85-126">Optional</span></span>
<span data-ttu-id="4bb85-127">ต่อไปนี้จะถือว่าเป็นทางเลือกและใช้เพื่อสร้างประสบการณ์ผู้ใช้ปลายทางที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="4bb85-127">The following are considered optional and used to create a better end-user experience.</span></span>

- <span data-ttu-id="4bb85-128">แสดง</span><span class="sxs-lookup"><span data-stu-id="4bb85-128">Render</span></span>

  <span data-ttu-id="4bb85-129">หากต้องการรองรับขนาดวิชวลที่เล็กลง ให้ลองเพิ่มตัวเลือกรูปแบบที่ผู้ใช้สามารถเปลี่ยนแปลงเพื่อปรับขนาดของแต่ละองค์ประกอบได้</span><span class="sxs-lookup"><span data-stu-id="4bb85-129">To support smaller visual sizes, try adding format options that the user can change to adjust the size of each element.</span></span> <span data-ttu-id="4bb85-130">ตัวอย่างเช่น เพิ่มตัวเลือกรูปแบบไปยังป้ายชื่อสำหรับใช้ในรายงานและแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="4bb85-130">For example, add format options to labels, for use in reports and dashboards.</span></span> <span data-ttu-id="4bb85-131">ซึ่งช่วยให้ผู้ใช้สามารถปรับแต่งวิชวลสำหรับอุปกรณ์เคลื่อนที่ของตนโดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="4bb85-131">This allows users to customize a visual specifically for their mobile device.</span></span>
  
  <span data-ttu-id="4bb85-132">นอกจากนี้ยังสามารถใช้การตั้งค่าเดียวกันกับวิชวลในเบราว์เซอร์บนเดสก์ท็อป และถ้าจำเป็น จะถูกแทนที่เพื่อปรับวิชวลให้เป็นหน้าจอขนาดเล็กลง</span><span class="sxs-lookup"><span data-stu-id="4bb85-132">The same settings can also be applied to the visuals in desktop browsers, and if needed, be overridden to adapt the visual to smaller screens.</span></span>

  > [!NOTE]
  > <span data-ttu-id="4bb85-133">หากต้องการปรับวิชวลให้เหมาะสมที่สุดในโหมด **โฟกัส** จะต้องพิจารณาทั้งการวางแนวขนาดหน้าจอในแนวตั้งและแนวนอน โปรดดู [เนื้อหาการแสดงผลในโหมดโฟกัส](../../consumer/end-user-focus.md)</span><span class="sxs-lookup"><span data-stu-id="4bb85-133">To optimize a visual in **Focus** mode, both portrait and landscape screen size orientations need consideration, see [Display content in Focus mode](../../consumer/end-user-focus.md).</span></span>

- <span data-ttu-id="4bb85-134">แบบโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="4bb85-134">Interactive</span></span>

  <span data-ttu-id="4bb85-135">พิจารณาการเพิ่มตัวจัดการเหตุการณ์เฉพาะสำหรับอุปกรณ์เคลื่อนที่เช่น การลาก และการเลื่อน</span><span class="sxs-lookup"><span data-stu-id="4bb85-135">Consider the addition of mobile specific event handlers, such as dragging and scrolling.</span></span>

- <span data-ttu-id="4bb85-136">การย้ายโหนดเมื่อเกิดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="4bb85-136">Failover</span></span>

  <span data-ttu-id="4bb85-137">วิชวลควรแสดงข้อผิดพลาดที่เป็นคำอธิบายถ้าไม่สามารถแสดงบนอุปกรณ์เคลื่อนที่ได้</span><span class="sxs-lookup"><span data-stu-id="4bb85-137">A visual should show a descriptive error if it cannot render on the mobile device.</span></span>

## <a name="supported-browsers-and-devices"></a><span data-ttu-id="4bb85-138">เบราว์เซอร์และอุปกรณ์ที่รองรับ</span><span class="sxs-lookup"><span data-stu-id="4bb85-138">Supported browsers and devices</span></span>
<span data-ttu-id="4bb85-139">วิชวล Power BI ต้องแสดงบนอุปกรณ์ทั้งหมดที่รองรับแอป Power BI สำหรับข้อมูลเพิ่มเติม โปรดดู [เบราว์เซอร์ที่รองรับสำหรับ Power BI](../../fundamentals/power-bi-browsers.md) และ [Power BI แอปสำหรับอุปกรณ์เคลื่อนที่ ](../../consumer/mobile/mobile-apps-for-mobile-devices.md)</span><span class="sxs-lookup"><span data-stu-id="4bb85-139">The Power BI visual must render on all devices supporting Power BI Apps, for more information see [supported browsers for Power BI](../../fundamentals/power-bi-browsers.md) and [Power BI mobile apps](../../consumer/mobile/mobile-apps-for-mobile-devices.md).</span></span>

<span data-ttu-id="4bb85-140">เมื่อทดสอบกับอุปกรณ์ Windows, iOS และ Android รุ่นล่าสุด นักพัฒนาจำเป็นต้องพิจารณาด้านคุณภาพเหล่านี้มากที่สุด</span><span class="sxs-lookup"><span data-stu-id="4bb85-140">When testing against the latest models of Windows, iOS, and Android devices, the developer needs to consider most of these quality aspects.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4bb85-141">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4bb85-141">Next steps</span></span>
<span data-ttu-id="4bb85-142">หากต้องการเริ่มต้น โปรดดู [การพัฒนาวิชวลการ์ดวงกลมใน Power BI](./develop-circle-card.md)</span><span class="sxs-lookup"><span data-stu-id="4bb85-142">To get started, see [Developing a Power BI circle card visual](./develop-circle-card.md).</span></span>