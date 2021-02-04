---
title: การแจ้งเตือนการหยุดชะงักของบริการ
description: เรียนรู้เกี่ยวกับวิธีการรับการแจ้งเตือนทางอีเมลเมื่อบริการของ Power BI หยุดทำงานหรือเสียหาย
author: kfollis
ms.author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 09/25/2020
ms.openlocfilehash: e5d8f43a8edb6dc05b58cb62836e98cf209c8b5c
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96407825"
---
# <a name="service-interruption-notifications"></a><span data-ttu-id="4ca98-103">การแจ้งเตือนการหยุดชะงักของบริการ</span><span class="sxs-lookup"><span data-stu-id="4ca98-103">Service interruption notifications</span></span>

<span data-ttu-id="4ca98-104">สิ่งสำคัญคือต้องมีข้อมูลเชิงลึกเกี่ยวกับความพร้อมใช้งานของแอปพลิเคชันทางธุรกิจที่สำคัญสำหรับภารกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="4ca98-104">It's important to have insight to availability of your mission-critical business applications.</span></span> <span data-ttu-id="4ca98-105">Power BI มีการแจ้งเตือนเหตุการณ์เพื่อให้คุณสามารถเลือกรับอีเมลได้ถ้ามีการหยุดทำงานหรือการลดประสิทธิภาพของบริการ</span><span class="sxs-lookup"><span data-stu-id="4ca98-105">Power BI provides incident notification so you can optionally receive emails if there's a service disruption or degradation.</span></span> <span data-ttu-id="4ca98-106">ในขณะที่ข้อตกลงระดับบริการของ Power BI (SLA) อยู่ที่ 99.9% ทำให้เกิดเหตุการณ์เหล่านี้ไม่บ่อย แต่เราต้องการให้แน่ใจว่าคุณได้รับการแจ้งให้ทราบ</span><span class="sxs-lookup"><span data-stu-id="4ca98-106">While the Power BI 99.9% service level agreement (SLA) makes these occurrences rare, we want to ensure that you're kept informed.</span></span> <span data-ttu-id="4ca98-107">หน้าจอต่อไปนี้แสดงชนิดของอีเมลที่คุณจะได้รับถ้าคุณเปิดใช้งานการแจ้งเตือน:</span><span class="sxs-lookup"><span data-stu-id="4ca98-107">The following screenshot shows the type of email you'll receive if you enable notifications:</span></span>

![รีเฟรชอีเมลแจ้งเตือน](media/service-interruption-notifications/refresh-notification-email.png)

<span data-ttu-id="4ca98-109">ในตอนนี้ เราจะส่งอีเมลสำหรับ _สถานการณ์ความน่าเชื่อถือ_ ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4ca98-109">At this time, we send emails for the following _reliability scenarios_:</span></span>

- <span data-ttu-id="4ca98-110">เปิดความน่าเชื่อถือของรายงาน</span><span class="sxs-lookup"><span data-stu-id="4ca98-110">Open report reliability</span></span>
- <span data-ttu-id="4ca98-111">ความน่าเชื่อถือของการรีเฟรชแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="4ca98-111">Model refresh reliability</span></span>
- <span data-ttu-id="4ca98-112">ความน่าเชื่อถือของการรีเฟรชคิวรี</span><span class="sxs-lookup"><span data-stu-id="4ca98-112">Query refresh reliability</span></span>

<span data-ttu-id="4ca98-113">การแจ้งเตือนจะถูกส่งไปเมื่อมี _ความล่าช้าที่ขยายออกไป_ ในการดำเนินงาน เช่น การเปิดรายงาน การรีเฟรชชุดข้อมูล หรือการดำเนินการคิวรี</span><span class="sxs-lookup"><span data-stu-id="4ca98-113">Notifications are sent when there's an _extended delay_ in operations like opening reports, dataset refresh, or query executions.</span></span> <span data-ttu-id="4ca98-114">หลังจากที่มีการแก้ไขปัญหาแล้ว คุณจะได้รับอีเมลการติดตามผล</span><span class="sxs-lookup"><span data-stu-id="4ca98-114">After an incident is resolved, you receive a follow-up email.</span></span>

> [!NOTE]
> <span data-ttu-id="4ca98-115">ปัจจุบัน คุณลักษณะนี้พร้อมใช้งานสำหรับความจุใน Power BI Premium เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4ca98-115">This feature is currently available only for capacities in Power BI Premium.</span></span> <span data-ttu-id="4ca98-116">ซึ่งไม่พร้อมใช้งานสำหรับความจุที่ใช้ร่วมกันหรือฝังไว้</span><span class="sxs-lookup"><span data-stu-id="4ca98-116">It's not available for shared or embedded capacity.</span></span>

## <a name="capacity-and-reliability-notifications"></a><span data-ttu-id="4ca98-117">ความจุและการแจ้งเตือนความมั่นคง</span><span class="sxs-lookup"><span data-stu-id="4ca98-117">Capacity and reliability notifications</span></span>

<span data-ttu-id="4ca98-118">เมื่อความจุของ Power BI Premium ประสบกับปัญหาการใช้ทรัพยากรสูงในระยะยาวที่อาจส่งผลต่อความมั่นคงได้ ระบบจะส่งอีเมลแจ้งเตือนออกไป</span><span class="sxs-lookup"><span data-stu-id="4ca98-118">When a Power BI Premium capacity is experiencing extended periods of high resource use that potentially impacts reliability, a notification email is sent.</span></span> <span data-ttu-id="4ca98-119">ตัวอย่างของผลกระทบดังกล่าวหมายรวมถึงความล่าช้าในการทำงานมากยิ่งขึ้น เช่น การเปิดรายงาน การรีเฟรชชุดข้อมูล และการประมวลคำถาม</span><span class="sxs-lookup"><span data-stu-id="4ca98-119">Examples of such impacts include extended delays in operations such as opening a report, dataset refresh, and query executions.</span></span> 

<span data-ttu-id="4ca98-120">อีเมลแจ้งเตือนจะให้ข้อมูลเกี่ยวกับเหตุผลในการใช้ทรัพยากรสูง รวมถึงข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4ca98-120">The notification email provides information about the reason for the high resource usage, including the following details:</span></span>

* <span data-ttu-id="4ca98-121">รหัสชุดข้อมูลของชุดข้อมูลที่รับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="4ca98-121">Dataset ID of the responsible dataset</span></span>
* <span data-ttu-id="4ca98-122">ประเภทการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="4ca98-122">Operation type</span></span>
* <span data-ttu-id="4ca98-123">เวลาการใช้งาน CPU จะเกี่ยวข้องกับการใช้ทรัพยากรสูง</span><span class="sxs-lookup"><span data-stu-id="4ca98-123">CPU time associated with the high resource usage.</span></span> <span data-ttu-id="4ca98-124">นี่คือ[คำจำกัดความของเวลาของ CPU ](https://wikipedia.org/wiki/CPU_time) ในวิกิพีเดีย</span><span class="sxs-lookup"><span data-stu-id="4ca98-124">Here's the [definition of CPU time](https://wikipedia.org/wiki/CPU_time) in Wikipedia.</span></span>

<span data-ttu-id="4ca98-125">และ Power BI จะส่งการแจ้งเตือนทางอีเมลเมื่อตรวจพบว่ามีการใช้งาน Power BI Premium เกินความจุ</span><span class="sxs-lookup"><span data-stu-id="4ca98-125">Power BI also sends email notifications when an overload in a Power BI Premium capacity is detected.</span></span> <span data-ttu-id="4ca98-126">อีเมลจะอธิบายเหตุผลที่อาจก่อให้เกิดการโอเวอร์โหลด ซึ่งคือการดำเนินการที่ก่อโหลดในช่วง 10 นาทีก่อนหน้าและปริมาณของโหลดของแต่ละการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="4ca98-126">The email explains the likely reason for the overload, which operations generated the load in the previous 10 minutes, and how much load each operation generated.</span></span>

<span data-ttu-id="4ca98-127">ถ้าคุณมีความจุแบบพรีเมียมมากกว่าหนึ่งรายการ อีเมลจะประกอบด้วยข้อมูลเกี่ยวกับกำลังการผลิตเหล่านั้นในช่วงเวลาที่โอเวอร์โหลด</span><span class="sxs-lookup"><span data-stu-id="4ca98-127">If you have more than one Premium capacity, the email includes information about those capacities during the overloaded period.</span></span> <span data-ttu-id="4ca98-128">ข้อมูลนี้ช่วยให้คุณสามารถพิจารณาย้ายพื้นที่ทำงานที่มีรายการที่มีทรัพยากรที่มีความจุกับการโหลดน้อยที่สุด</span><span class="sxs-lookup"><span data-stu-id="4ca98-128">This info helps you consider moving the workspaces containing resource-intensive items to capacities with the least load.</span></span>

<span data-ttu-id="4ca98-129">ระบบจะส่งอีเมลแจ้งเตือนการโอเวอร์โหลดเฉพาะเมื่อมีการใช้งานถึงขีดจำกัดการโอเวอร์โหลดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4ca98-129">Overload email notifications are only sent when an overload threshold is triggered.</span></span> <span data-ttu-id="4ca98-130">คุณจะไม่ได้รับอีเมลฉบับต่อมาอีกในกรณีที่โหลดบนความจุแบบพรีเมียมคืนกลับสู่ระดับที่ไม่โอเวอร์โหลด</span><span class="sxs-lookup"><span data-stu-id="4ca98-130">You won't receive a second email when the load on that Premium capacity returns to non-overloaded levels.</span></span>

<span data-ttu-id="4ca98-131">รูปภาพต่อไปนี้แสดงตัวอย่างของอีเมลแจ้งเตือน:</span><span class="sxs-lookup"><span data-stu-id="4ca98-131">The following image shows an example notification email:</span></span>

![อีเมลแจ้งเตือนความจุโอเวอร์โหลด](media/service-interruption-notifications/refresh-notification-email-2.png)


## <a name="enable-notifications"></a><span data-ttu-id="4ca98-133">เปิดใช้งานการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="4ca98-133">Enable notifications</span></span>

<span data-ttu-id="4ca98-134">ผู้ดูแลระบบ Power BI จะเปิดใช้งานการแจ้งเตือนในพอร์ทัลผู้ดูแลระบบ:</span><span class="sxs-lookup"><span data-stu-id="4ca98-134">A Power BI admin enables notifications in the admin portal:</span></span>

1. <span data-ttu-id="4ca98-135">ระบุหรือสร้างกลุ่มความปลอดภัยที่เปิดใช้งานอีเมลซึ่งควรได้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="4ca98-135">Identify or create an email-enabled security group that should receive notifications.</span></span>

1. <span data-ttu-id="4ca98-136">ในพอร์ทัลผู้ดูแลระบบ ให้เลือก **การตั้งค่าผู้เช่า**</span><span class="sxs-lookup"><span data-stu-id="4ca98-136">In the admin portal, select **Tenant settings**.</span></span> <span data-ttu-id="4ca98-137">ภายใต้ **วิธีใช้และการตั้งค่าการสนับสนุน** ขยาย **รับการแจ้งเตือนทางอีเมลสำหรับบริการขัดข้องหรือเหตุการณ์**</span><span class="sxs-lookup"><span data-stu-id="4ca98-137">Under **Help and support settings**, expand **Receive email notifications for service outages or incidents**.</span></span>

1. <span data-ttu-id="4ca98-138">เปิดใช้งานการแจ้งเตือน ให้ใส่กลุ่มความปลอดภัยและเลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="4ca98-138">Enable notifications, enter a security group, and select **Apply**.</span></span>

    ![เปิดใช้งานการแจ้งเตือนบริการ](media/service-interruption-notifications/enable-notifications.png)

> [!NOTE]
> <span data-ttu-id="4ca98-140">Power BI ส่งการแจ้งเตือนจากบัญชีno-reply-powerbi@microsoft.com</span><span class="sxs-lookup"><span data-stu-id="4ca98-140">Power BI sends notifications from the account no-reply-powerbi@microsoft.com.</span></span> <span data-ttu-id="4ca98-141">ตรวจสอบให้แน่ใจว่าบัญชีนี้ถูกเพิ่มในรายการผู้ส่งที่ปลอดภัยของคุณเพื่อไม่ให้การแจ้งเตือนอีเมลปรากฏอยู่ในโฟลเดอร์อีเมลขยะ</span><span class="sxs-lookup"><span data-stu-id="4ca98-141">Ensure that this account is added to your safe sender list so that notifications don't end up in a junk email folder.</span></span>

## <a name="service-health-in-microsoft-365"></a><span data-ttu-id="4ca98-142">สถานภาพบริการใน Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4ca98-142">Service health in Microsoft 365</span></span>

<span data-ttu-id="4ca98-143">บทความนี้อธิบายวิธีการรับการแจ้งเตือนบริการผ่าน Power BI</span><span class="sxs-lookup"><span data-stu-id="4ca98-143">This article describes how to receive service notifications through Power BI.</span></span> <span data-ttu-id="4ca98-144">นอกจากนี้ คุณยังสามารถตรวจสอบสถานภาพบริการของ Power BI สุขภาพผ่าน Microsoft 365 ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="4ca98-144">You can also monitor Power BI service health through Microsoft 365.</span></span> <span data-ttu-id="4ca98-145">เข้าร่วมเพื่อรับการแจ้งเตือนทางอีเมลเกี่ยวกับสถานภาพบริการจาก Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4ca98-145">Opt in to receive email notifications about service health from Microsoft 365.</span></span> <span data-ttu-id="4ca98-146">เรียนรู้เพิ่มเติมใน [วิธีการตรวจสอบสถานภาพบริการใน Microsoft 365](/microsoft-365/enterprise/view-service-health)</span><span class="sxs-lookup"><span data-stu-id="4ca98-146">Learn more in [How to check Microsoft 365 service health](/microsoft-365/enterprise/view-service-health).</span></span>

## <a name="next-steps"></a><span data-ttu-id="4ca98-147">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4ca98-147">Next steps</span></span>

[<span data-ttu-id="4ca98-148">ตัวเลือกการสนับสนุน Power BI Pro และ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="4ca98-148">Power BI Pro and Power BI Premium support options</span></span>](service-support-options.md)

<span data-ttu-id="4ca98-149">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4ca98-149">More questions?</span></span> [<span data-ttu-id="4ca98-150">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="4ca98-150">Try the Power BI Community</span></span>](https://community.powerbi.com/)