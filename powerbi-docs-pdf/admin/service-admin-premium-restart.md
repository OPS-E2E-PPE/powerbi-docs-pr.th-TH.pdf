---
title: รีสตาร์ตความจุ Power BI Premium
description: เรียนรู้วิธีการรีสตาร์ทความจุ Power BI Premium เพื่อแก้ไขปัญหาด้านประสิทธิภาพการทำงาน
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-premium
ms.topic: how-to
ms.date: 11/11/2020
LocalizationGroup: Premium
ms.openlocfilehash: 367195e0e09bbfb7de20acfa71b8da9742664ca2
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413575"
---
# <a name="restart-a-power-bi-premium-capacity"></a><span data-ttu-id="3da2d-103">รีสตาร์ตความจุ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="3da2d-103">Restart a Power BI Premium capacity</span></span>

<span data-ttu-id="3da2d-104">คุณอาจต้องรีสตาร์ทความจุ Premium ในฐานะที่เป็นผู้ดูแล Power BI</span><span class="sxs-lookup"><span data-stu-id="3da2d-104">As a Power BI administrator, you might need to restart a Premium capacity.</span></span> <span data-ttu-id="3da2d-105">บทความนี้อธิบายวิธีการรีสตาร์ทความจุและตอบคำถามต่าง ๆ เกี่ยวกับการรีสตาร์ทระบบใหม่และประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="3da2d-105">This article explains how to restart a capacity and addresses several questions about restart and performance.</span></span>

## <a name="why-does-power-bi-provide-this-option"></a><span data-ttu-id="3da2d-106">เหตุใด Power BI จึงมีตัวเลือกนี้?</span><span class="sxs-lookup"><span data-stu-id="3da2d-106">Why does Power BI provide this option?</span></span>

<span data-ttu-id="3da2d-107">Power BI ช่วยให้ผู้ใช้งานสามารถทำการวิเคราะห์ที่ซับซ้อนกับข้อมูลจำนวนมหาศาลได้</span><span class="sxs-lookup"><span data-stu-id="3da2d-107">Power BI gives users the ability to perform complex analyses on huge amounts of data.</span></span> <span data-ttu-id="3da2d-108">น่าเสียดายที่ผู้ใช้สามารถทำให้เกิดปัญหาประสิทธิภาพการทำงานโดยการโหลดบริการ Power BI ด้วยงานจำนวนมากเกินไป เขียนคิวรี่ที่ซับซ้อนมากเกินไป สร้างการอ้างอิงแบบวงกลมและอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="3da2d-108">Unfortunately, users can cause performance issues by overloading the Power BI service with jobs, writing overly complex queries, creating circular references, and so on.</span></span>

<span data-ttu-id="3da2d-109">ความจุที่ใช้ร่วมกันของ Power BI ให้การป้องกันในบางกรณี เช่น การจำกัดขนาดไฟล์ การกำหนดตารางเวลาการรีเฟรช และลักษณะบริการอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="3da2d-109">Power BI shared capacity offers some protection from such cases by imposing limits on file sizes, refresh schedules, and other aspects of the service.</span></span> <span data-ttu-id="3da2d-110">สำหรับความจุของ Power BI Premium ในทางตรงกันข้าม ข้อจำกัดเหล่านั้นส่วนใหญ่จะเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="3da2d-110">In a Power BI Premium capacity, by contrast, most of those limits are raised.</span></span> <span data-ttu-id="3da2d-111">เป็นผลให้รายงานเดียวที่มีนิพจน์ DAX ไม่ดีหรือแบบจำลองที่ซับซ้อนมากอาจทำให้เกิดปัญหาประสิทธิภาพการทำงานที่มีนัยสำคัญ</span><span class="sxs-lookup"><span data-stu-id="3da2d-111">As a result, a single report with a bad DAX expression or a very complex model can cause significant performance issues.</span></span> <span data-ttu-id="3da2d-112">เมื่อประมวลผลแล้ว รายงานสามารถใช้ทรัพยากรทั้งหมดที่มีอยู่ในความจุได้</span><span class="sxs-lookup"><span data-stu-id="3da2d-112">When processed, the report can consume all of the resources available on the capacity.</span></span> 

<span data-ttu-id="3da2d-113">Power BI ปรับปรุงอย่างต่อเนื่องในวิธีที่จะปกป้องผู้ใช้ที่มีความจุระดับ Premium จากปัญหาดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="3da2d-113">Power BI is constantly improving in how it protects Premium capacity users against such issues.</span></span> <span data-ttu-id="3da2d-114">นอกจากนี้เรายังเพิ่มขีดความสามารถให้ผู้ดูแลระบบด้วยเครื่องมือในการวิเคราะห์เมื่อมีความจุมากเกินไปและสาเหตุ</span><span class="sxs-lookup"><span data-stu-id="3da2d-114">We are also empowering administrators with the tools to analyze when capacities are overburdened and why.</span></span> <span data-ttu-id="3da2d-115">สำหรับข้อมูลเพิ่มเติม โปรดดู [เซสชันการฝึกอบรมระยะสั้น](https://www.youtube.com/watch?v=UgsjMbhi_Bk&feature=youtu.be) และ [เซสชันการฝึกอบรมระยะยาว](https://powerbi.tips/2018/07/)</span><span class="sxs-lookup"><span data-stu-id="3da2d-115">For more information, see our [short training session](https://www.youtube.com/watch?v=UgsjMbhi_Bk&feature=youtu.be) and [longer training session](https://powerbi.tips/2018/07/).</span></span> <span data-ttu-id="3da2d-116">ในขณะเดียวกัน คุณจำเป็นต้องมีความสามารถทำให้ปัญหาที่สำคัญลดลงเมื่อเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="3da2d-116">At the same time, you need the ability to mitigate significant issues when they occur.</span></span> <span data-ttu-id="3da2d-117">แนวทางที่เร็วที่สุดในการทำให้ปัญหาเหล่านี้ลดลงคือการรีสตาร์ทความจุ</span><span class="sxs-lookup"><span data-stu-id="3da2d-117">The quickest way to mitigate these issues is to restart the capacity.</span></span>

> [!NOTE]
> <span data-ttu-id="3da2d-118">Power BI Premium เพิ่งเปิดตัว Premium เวอร์ชันใหม่ชื่อ **Premium Gen2** ซึ่งกำลังอยู่ในช่วงการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3da2d-118">Power BI Premium recently released a new version of Premium, called **Premium Gen2**, which is currently in preview.</span></span> <span data-ttu-id="3da2d-119">ความสามารถของ Preview Gen2 ไม่จำเป็นต้องรีสตาร์ท ดังนั้นคุณลักษณะนี้จึงไม่มีใน Premium Gen2</span><span class="sxs-lookup"><span data-stu-id="3da2d-119">Preview Gen2 capacities do not require restarts, so this feature is not available in Premium Gen2.</span></span>

## <a name="is-the-restart-process-safe-will-i-lose-any-data"></a><span data-ttu-id="3da2d-120">กระบวนการรีสตาร์ทปลอดภัยหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="3da2d-120">Is the restart process safe?</span></span> <span data-ttu-id="3da2d-121">ฉันจะสูญเสียข้อมูลใด ๆ หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="3da2d-121">Will I lose any data?</span></span>

<span data-ttu-id="3da2d-122">ข้อมูล คำจำกัดความ รายงาน และแดชบอร์ดที่บันทึกไว้ทั้งหมดในความจุของคุณยังคงไม่เปลี่ยนแปลงหลังจากรีสตาร์ท</span><span class="sxs-lookup"><span data-stu-id="3da2d-122">All the saved data, definitions, reports, and dashboards on your capacity remain fully intact after restart.</span></span> <span data-ttu-id="3da2d-123">เมื่อคุณเริ่มต้นความจุ การรีเฟรชแบบกำหนดเวลาและเฉพาะกิจที่ดำเนินอยู่จะหยุดลงชั่วคราวโดยกลไกการรีเฟรช ในกรณีส่วนใหญ่ จากนั้นจะเริ่มระบบใหม่เนื่องจากการรีเฟรชตรรกะใหม่ที่สร้างขึ้นใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3da2d-123">When you restart a capacity, ongoing scheduled and ad-hoc refreshes are stopped temporarily by the refresh engine, in most cases, then they restart due to refresh retry logic built into Power BI.</span></span> <span data-ttu-id="3da2d-124">บริการพยายามลองรีเฟรชที่ได้รับผลกระทบอีกครั้งเมื่อความจุพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3da2d-124">The service attempts to retry any impacted refreshes once the capacity becomes available.</span></span> <span data-ttu-id="3da2d-125">สถานะของการรีเฟรชอาจไม่เปลี่ยนแปลงในอินเทอร์เฟซผู้ใช้ระหว่างกระบวนการรีสตาร์ท</span><span class="sxs-lookup"><span data-stu-id="3da2d-125">The state of refreshes may not change in the user interface during the restart process.</span></span> 

<span data-ttu-id="3da2d-126">ผู้ใช้ที่โต้ตอบกับความจุจะสูญเสียงานที่ไม่ได้บันทึกไว้ระหว่างกระบวนการรีสตาร์ท</span><span class="sxs-lookup"><span data-stu-id="3da2d-126">Users interacting with the capacity will lose unsaved work during a restart process.</span></span> <span data-ttu-id="3da2d-127">ผู้ใช้ควรรีเฟรชเบราว์เซอร์ของพวกเขาหลังจากการรีสตาร์ทเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3da2d-127">Users should refresh their browsers after the restart is complete.</span></span>

## <a name="how-do-i-restart-a-capacity"></a><span data-ttu-id="3da2d-128">ฉันจะรีสตาร์ทความจุได้อย่างไร?</span><span class="sxs-lookup"><span data-stu-id="3da2d-128">How do I restart a capacity?</span></span>

<span data-ttu-id="3da2d-129">ทำตามขั้นตอนเหล่านี้เพื่อรีสตาร์ตความจุ</span><span class="sxs-lookup"><span data-stu-id="3da2d-129">Follow these steps to restart a capacity.</span></span>

1. <span data-ttu-id="3da2d-130">ในพอร์ทัลผู้ดูแลระบบ Power BI บนแถบ **การตั้งค่าความจุ** นำทางไปยังความจุของคุณ</span><span class="sxs-lookup"><span data-stu-id="3da2d-130">In the Power BI admin portal, on the **Capacity Settings** tab, navigate to your capacity.</span></span> 

1. <span data-ttu-id="3da2d-131">เพิ่ม *ธงคุณลักษณะ\*\*\*CapacityRestart*\* เข้ากับ URL ความจุของคุณ: `https://app.powerbi.com/admin-portal/capacities/<YourCapacityId>?capacityRestartButton=true`</span><span class="sxs-lookup"><span data-stu-id="3da2d-131">Add the **CapacityRestart** *feature flag* to your capacity URL: `https://app.powerbi.com/admin-portal/capacities/<YourCapacityId>?capacityRestartButton=true`.</span></span>

1. <span data-ttu-id="3da2d-132">ภายใต้ **การตั้งค่าขั้นสูง** > **CAPACITY RESTART** ให้เลือก **รีสตาร์ทความจุ**</span><span class="sxs-lookup"><span data-stu-id="3da2d-132">Under **Advanced Settings** > **CAPACITY RESTART**, select **Restart capacity**.</span></span>

    ![รีสตาร์ทความจุ](media/service-admin-premium-restart/restart-capacity.png)

1. <span data-ttu-id="3da2d-134">ในกล่องโต้ตอบ **รีสตาร์ทความจุ** ให้เลือก **ใช่ รีสตาร์ทความจุ**</span><span class="sxs-lookup"><span data-stu-id="3da2d-134">In the **Capacity restart** dialog box, select **Yes, restart capacity**.</span></span>

    ![ยืนยันการรีสตาร์ท](media/service-admin-premium-restart/confirm-restart.png)

## <a name="how-can-i-prevent-issues-from-happening-in-the-future"></a><span data-ttu-id="3da2d-136">ฉันจะป้องกันไม่ให้ปัญหาเกิดขึ้นในอนาคตได้อย่างไร?</span><span class="sxs-lookup"><span data-stu-id="3da2d-136">How can I prevent issues from happening in the future?</span></span>

<span data-ttu-id="3da2d-137">แนวทางที่ดีที่สุดในการป้องกันปัญหาคือการให้ความรู้แก่ผู้ใช้เกี่ยวกับการสร้างแบบจำลองข้อมูลที่มีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="3da2d-137">The best way to prevent issues is to educate users about efficient data modeling.</span></span> <span data-ttu-id="3da2d-138">สำหรับข้อมูลเพิ่มเติม ดู [เซสชั่นการฝึกอบรม](https://powerbi.tips/2018/07/) ของเรา</span><span class="sxs-lookup"><span data-stu-id="3da2d-138">For more information, see our [training session](https://powerbi.tips/2018/07/).</span></span>

<span data-ttu-id="3da2d-139">เราขอแนะนำให้คุณ [ตรวจสอบความจุของคุณ](service-admin-premium-monitor-capacity.md) เป็นประจำเพื่อค้นหาแนวโน้มที่บ่งบอกถึงปัญหาพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="3da2d-139">We also recommend that you [monitor your capacities](service-admin-premium-monitor-capacity.md) regularly to look for trends that indicate underlying issues.</span></span> <span data-ttu-id="3da2d-140">เราวางแผนเผยแพร่แอปตรวจสอบและเครื่องมืออื่น ๆ เป็นประจำเพื่อให้คุณสามารถตรวจสอบและจัดการความจุของคุณได้อย่างมีประสิทธิภาพยิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="3da2d-140">We plan regular releases of the monitoring app and other tools so that you can monitor and manage your capacities more effectively.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3da2d-141">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3da2d-141">Next steps</span></span>

[<span data-ttu-id="3da2d-142">Power BI Premium คืออะไร?</span><span class="sxs-lookup"><span data-stu-id="3da2d-142">What is Power BI Premium?</span></span>](service-premium-what-is.md)

<span data-ttu-id="3da2d-143">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3da2d-143">More questions?</span></span> [<span data-ttu-id="3da2d-144">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="3da2d-144">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
