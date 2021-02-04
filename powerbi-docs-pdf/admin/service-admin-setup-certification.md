---
title: เปิดใช้งานใบรับรองเนื้อหา
description: เรียนรู้วิธีการเปิดใช้งานใบรับรองสำหรับชุดข้อมูล กระแสข้อมูล รายงาน และแอป
author: paulinbar
ms.author: painbar
ms.service: powerbi
ms.subservice: powerbi-eim
ms.topic: how-to
ms.date: 10/26/2020
LocalizationGroup: Share your work
ms.openlocfilehash: 520a3673d34019c6045988cd5d501e187849a5c6
ms.sourcegitcommit: 932f6856849c39e34229dc9a49fb9379c56a888a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/06/2021
ms.locfileid: "97927054"
---
# <a name="enable-content-certification"></a><span data-ttu-id="4720c-103">เปิดใช้งานใบรับรองเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="4720c-103">Enable content certification</span></span>

<span data-ttu-id="4720c-104">องค์กรของคุณสามารถรับรองเนื้อหาที่เลือก เพื่อระบุว่าเนื้อหาดังกล่าวเป็นแหล่งข้อมูลที่เชื่อถือได้สำหรับข้อมูลสำคัญหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4720c-104">Your organization can certify selected content to identify it an as authoritative source for critical information.</span></span> <span data-ttu-id="4720c-105">ในขณะนี้ ชนิดเนื้อหาต่อไปนี้สามารถได้รับการรับรอง:</span><span class="sxs-lookup"><span data-stu-id="4720c-105">Currently, the following content types can be certified:</span></span>
* <span data-ttu-id="4720c-106">ชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4720c-106">Datasets</span></span>
* <span data-ttu-id="4720c-107">กระแสข้อมูล (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="4720c-107">Dataflows (preview)</span></span>
* <span data-ttu-id="4720c-108">รายงาน (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="4720c-108">Reports (preview)</span></span>
* <span data-ttu-id="4720c-109">แอป (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="4720c-109">Apps (preview)</span></span>

<span data-ttu-id="4720c-110">ในฐานะผู้ดูแลระบบของ Power BI คุณมีหน้าที่รับผิดชอบสำหรับการเปิดใช้งานและตั้งค่ากระบวนการรับรองสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="4720c-110">As a Power BI admin, you are responsible for enabling and setting up the certification process for your organization.</span></span> <span data-ttu-id="4720c-111">ซึ่งหมายถึง:</span><span class="sxs-lookup"><span data-stu-id="4720c-111">This means:</span></span>
* <span data-ttu-id="4720c-112">การเปิดใช้งานการรับรองบนผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="4720c-112">Enabling certification on your tenant.</span></span>
* <span data-ttu-id="4720c-113">การกำหนดรายการของกลุ่มความปลอดภัยที่สมาชิกจะได้รับอนุญาตให้รับรองเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="4720c-113">Defining a list of security groups whose members will be authorized to certify content.</span></span>
* <span data-ttu-id="4720c-114">การกำหนดให้ URL ที่ชี้ไปยังคู่มือสำหรับกระบวนการรับรองเนื้อหาขององค์กร ถ้ามีเอกสารดังกล่าวอยู่</span><span class="sxs-lookup"><span data-stu-id="4720c-114">Providing a URL that points to the documentation for the organization's content certification process, if such documentation exists.</span></span>

<span data-ttu-id="4720c-115">การรับรองเป็นส่วนหนึ่งของคุณลักษณะ *การรับรอง* ของ Power BI</span><span class="sxs-lookup"><span data-stu-id="4720c-115">Certification is part of Power BI's *endorsement* feature.</span></span> <span data-ttu-id="4720c-116">ดูที่ [การรับรอง: การเลื่อนระดับและการรับรองเนื้อหา Power BI](../collaborate-share/service-endorsement-overview.md) สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4720c-116">See [Endorsement: Promoting and certifying Power BI content](../collaborate-share/service-endorsement-overview.md) for more information.</span></span>

## <a name="set-up-certification"></a><span data-ttu-id="4720c-117">ตั้งค่าการรับรอง</span><span class="sxs-lookup"><span data-stu-id="4720c-117">Set up certification</span></span>

1. <span data-ttu-id="4720c-118">ในพอร์ทัลผู้ดูแลระบบ ไปที่การตั้งค่าผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="4720c-118">In the Admin portal, go to Tenant settings.</span></span>
1. <span data-ttu-id="4720c-119">ภายใต้ส่วนการตั้งค่าการส่งออกและการแชร์ ขยายส่วนการรับรอง</span><span class="sxs-lookup"><span data-stu-id="4720c-119">Under the Export and sharing settings section, expand the Certification section.</span></span>

   ![ตั้งค่าชุดข้อมูลและใบรับรองกระแสข้อมูล](media/service-admin-setup-certification/service-admin-certification-setup-dialog.png)

1. <span data-ttu-id="4720c-121">ตั้งค่าการสลับเป็น **เปิดใช้งานแล้ว**</span><span class="sxs-lookup"><span data-stu-id="4720c-121">Set the toggle to **Enabled**.</span></span>
1. <span data-ttu-id="4720c-122">หากองค์กรของคุณมีนโยบายเกี่ยวกับใบรับรองที่เผยแพร่แล้ว คุณจะสามารถใส่ URL ได้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="4720c-122">If your organization has a published certification policy, provide its URL here.</span></span> <span data-ttu-id="4720c-123">การดำเนินการนี้จะกลายเป็นลิงก์ **เรียนรู้เพิ่มเติม** ในส่วนใบรับรองของ [กล่องโต้ตอบการตั้งค่าการรับรอง](../collaborate-share/service-endorse-content.md#request-content-certification)</span><span class="sxs-lookup"><span data-stu-id="4720c-123">This will become the **Learn more** link in the certification section of the [endorsement settings dialog](../collaborate-share/service-endorse-content.md#request-content-certification).</span></span> <span data-ttu-id="4720c-124">ถ้าคุณไม่ใส่ลิงก์ ผู้ใช้ที่ต้องการร้องขอใบรับรองเนื้อหาของพวกเขาจะได้รับคำแนะนำให้ติดต่อผู้ดูแลระบบ Power BI ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="4720c-124">If you do not supply a link, users who want to request certification of their content will be advised to contact their Power BI administrator.</span></span>
1. <span data-ttu-id="4720c-125">กำหนดกลุ่มความปลอดภัยที่สมาชิกจะได้รับอนุญาตให้รับรองเนื้อหาอย่างน้อยหนึ่งกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="4720c-125">Specify one or more security groups whose members will be authorized to certify content.</span></span> <span data-ttu-id="4720c-126">ผู้รับรองที่ได้รับอนุญาตอย่างเป็นทางการเหล่านี้ จะสามารถใช้ปุ่ม ใบรับรอง ในส่วนใบรับรองของ [กล่องโต้ตอบการตั้งค่าการรับรอง](../collaborate-share/service-endorse-content.md#certify-content)</span><span class="sxs-lookup"><span data-stu-id="4720c-126">These authorized certifiers will able to use the Certification button in the certification section of the [endorsement settings dialog](../collaborate-share/service-endorse-content.md#certify-content).</span></span> <span data-ttu-id="4720c-127">เขตข้อมูลนี้ยอมรับเฉพาะกลุ่มความปลอดภัยเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4720c-127">This field accepts security groups only.</span></span> <span data-ttu-id="4720c-128">คุณไม่สามารถป้อนผู้ใช้ที่มีชื่อ</span><span class="sxs-lookup"><span data-stu-id="4720c-128">You cannot enter named users.</span></span>
    
    <span data-ttu-id="4720c-129">ถ้ากลุ่มความปลอดภัยมีกลุ่มความปลอดภัยย่อยที่คุณไม่ต้องการให้สิทธิใบรับรอง คุณสามารถทำเครื่องหมายที่กล่อง **ยกเว้นกลุ่มความปลอดภัยเฉพาะ** และใส่ชื่อของกลุ่มเหล่านั้นในกล่องข้อความที่จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="4720c-129">If a security group contains sub-security groups that you do not want to give certification rights to, you can check the **Except specific security groups** box and enter the name(s) of those group(s) in a text box that will appear.</span></span>
1. <span data-ttu-id="4720c-130">คลิก **ใช้**</span><span class="sxs-lookup"><span data-stu-id="4720c-130">Click **Apply**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4720c-131">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4720c-131">Next steps</span></span>
* [<span data-ttu-id="4720c-132">เลื่อนระดับหรือรับรองเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="4720c-132">Promote or certify content</span></span>](../collaborate-share/service-endorse-content.md)
* [<span data-ttu-id="4720c-133">อ่านเกี่ยวกับการรับรองใน Power BI</span><span class="sxs-lookup"><span data-stu-id="4720c-133">Read about endorsement in Power BI</span></span>](../collaborate-share/service-endorsement-overview.md)
* <span data-ttu-id="4720c-134">มีคำถามหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="4720c-134">Questions?</span></span> [<span data-ttu-id="4720c-135">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="4720c-135">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
