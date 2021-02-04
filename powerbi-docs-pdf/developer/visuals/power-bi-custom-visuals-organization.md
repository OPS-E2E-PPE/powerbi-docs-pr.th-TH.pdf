---
title: วิชวลขององค์กรใน Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: ใช้ จัดการ และสร้างวิชวลองค์กรใน Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.date: 12/11/2018
LocalizationGroup: Visualizations
ms.openlocfilehash: 908225c772aee7e5697ba828c55b96f74c204c1d
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888155"
---
# <a name="organizational-visuals-in-power-bi"></a><span data-ttu-id="1d7ea-104">วิชวลองค์กรใน Power BI</span><span class="sxs-lookup"><span data-stu-id="1d7ea-104">Organizational visuals in Power BI</span></span>

<span data-ttu-id="1d7ea-105">คุณสามารถใช้ส่วนวิชวล Power BI ใน Power BI เพื่อสร้างวิชวลชนิดที่ไม่ซ้ำใครที่เหมาะกับคุณ</span><span class="sxs-lookup"><span data-stu-id="1d7ea-105">You can use Power BI visuals in Power BI to create a unique type of visual that's tailored to you.</span></span> <span data-ttu-id="1d7ea-106">วิชวล Power BI เหล่านี้จะถูกสร้างขึ้น โดยนักพัฒนา และพวกเขามักจะสร้างขึ้นเมื่อวิชวลมากมายที่มีอยู่ใน Power BI ไม่ตอบสนองของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="1d7ea-106">Power BI visuals are created by developers, and they're often created when the multitude of visuals that are included in Power BI don't quite meet their need.</span></span>

<span data-ttu-id="1d7ea-107">ในบางองค์กร ส่วนการแสดงผล BI มีความสำคัญมากยิ่งขึ้น มันอาจะจำเป็นในการสื่อข้อมูลที่เฉพาะเจาะจงหรือข้อมูลเชิงลึกที่มีเอกลักษณ์องค์กร มันอาจมีความต้องการข้อมูลพิเศษหรืออาจจะเน้นวิธการทำีธุรกิจแบบ่วนตัว</span><span class="sxs-lookup"><span data-stu-id="1d7ea-107">In some organizations, Power BI visuals are even more important – they might be necessary to convey specific data or insights unique to the organization, they may have special data requirements, or they may highlight private business methods.</span></span> <span data-ttu-id="1d7ea-108">องค์กรดังกล่าวต้องจัดทำส่วนวิชวล Power BI แล้วใช้ร่วมกันทั่วทั้งองค์กรและตรวจสอบให้แน่ใจว่า ได้รับการดูแลอย่างเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="1d7ea-108">Such organizations need to develop Power BI visuals, share them throughout their organization, and make sure they're properly maintained.</span></span> <span data-ttu-id="1d7ea-109">การแสดงผล Power BI ช่วยให้หน่วยงานสามารถดำเนินการได้ตามนี้</span><span class="sxs-lookup"><span data-stu-id="1d7ea-109">Power BI visuals  lets organizations do just that.</span></span>

<span data-ttu-id="1d7ea-110">รูปต่อไปนี้แสดงขั้นตอนการไหลของส่วนแสดงผล Power BI ขององค์กรใน Power BI จากขั้นตอนผู้ดูแล ผ่านขั้นตอนการพัฒนาและการบำรุงรักษา และไปยังขั้นตอนวิเคราะห์ข้อมูลเป็นลำดับสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="1d7ea-110">The following image shows the process by which organization Power BI visuals in Power BI flow from administrator, through development and maintenance, all finally make their way to the data analyst.</span></span>

![วิชวลแบบกำหนดเอง](media/power-bi-custom-visuals-organizational/custom-visual-org-01.jpg)

<span data-ttu-id="1d7ea-112">การจัดการแสดงผลด้วยภาพขององค์กรมีการปรับใช้ และจัดการ โดยผู้ดูแลระบบ Power BI จากพอร์ทัลผู้ดูแล</span><span class="sxs-lookup"><span data-stu-id="1d7ea-112">Organizational visuals are deployed and managed by the Power BI administrator from the Admin portal.</span></span> <span data-ttu-id="1d7ea-113">เมื่อเปิดใช้ในที่เก็บข้อมูลขององค์กร ผู้ใช้ในองค์กรสามารถรู้จักกับมันได้อย่างง่ายดาย และนำเข้าส่วนการแสดงผล Power BI ขององค์กรลงในรายงานของพวกเขาได้โดยตรงจาก Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="1d7ea-113">Once deployed into the organizational repository, users in the organization can easily discover them, and import the organizational Power BI visuals into their reports directly from Power BI Desktop.</span></span>

<span data-ttu-id="1d7ea-114">เพื่อเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการแสดงผลด้วยส่วนการแสดงผล Power BI ขององค์กรในรายงานที่คุณสร้างขึ้น ให้ดูบทความต่อไปนี้: [เรียนรู้เพิ่มเติมเกี่ยวกับการนำภาพองค์กรลงในรายงานของคุณ](power-bi-custom-visuals.md)</span><span class="sxs-lookup"><span data-stu-id="1d7ea-114">To learn more about how to use organizational Power BI visuals in the reports that you created, see the following article: [Learn more about importing organizational visuals into your reports](power-bi-custom-visuals.md).</span></span>

## <a name="administer-organizational-power-bi-visuals"></a><span data-ttu-id="1d7ea-115">จัดการส่วนการแสดงผล Power BI ของหน่วยงาน</span><span class="sxs-lookup"><span data-stu-id="1d7ea-115">Administer organizational Power BI visuals</span></span>

<span data-ttu-id="1d7ea-116">เพื่อเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการจัดการ ปรับใช้ และจัดการส่วนการแสดงผล Power BI ขององค์กรในองค์กรของคุณ ให้ดูบทความต่อไปนี้: [เรียนรู้เพิ่มเติมเกี่ยวกับการปรับใช้และส่วนการแสดงผล Power BI ขององค์กร](../../admin/organizational-visuals.md)</span><span class="sxs-lookup"><span data-stu-id="1d7ea-116">To learn more about how to administer, deploy, and manage organizational Power BI visuals in your organization, see the following article: [Learn more about deployment and management of organization Power BI visuals](../../admin/organizational-visuals.md).</span></span>

> [!WARNING]
> <span data-ttu-id="1d7ea-117">วิชวล Power BI ที่ติดตั้งจากไฟล์อาจประกอบด้วยโค้ด ที่มีความเสี่ยงด้านความปลอดภัยหรือความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="1d7ea-117">A Power BI visual installed from a file, can contain code with security or privacy risks.</span></span> <span data-ttu-id="1d7ea-118">ตรวจสอบให้แน่ใจว่า คุณเชื่อถือผู้สร้างและแหล่งมาไฟล์วิชวล  ก่อนที่จะปรับใช้ไปยังที่เก็บขององค์กร</span><span class="sxs-lookup"><span data-stu-id="1d7ea-118">Make sure you trust the author and the source of the Power BI visual file, before deploying it to the organization repository.</span></span>

## <a name="considerations-and-limitations"></a><span data-ttu-id="1d7ea-119">ข้อควรพิจารณาและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="1d7ea-119">Considerations and limitations</span></span>

<span data-ttu-id="1d7ea-120">มีข้อควรพิจารณาและข้อจำกัดที่คุณจำเป็นต้องระวังมากมาย</span><span class="sxs-lookup"><span data-stu-id="1d7ea-120">There are several considerations and limitations that you need to be aware of.</span></span>

<span data-ttu-id="1d7ea-121">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="1d7ea-121">Admin:</span></span>

* <span data-ttu-id="1d7ea-122">หากวิชวล Power BI จาก ApSource หรือไฟล์ถูกลบจากที่เก็บ รายงานใด ๆ ที่มีอยู่ที่ใช้วิชวลที่ถูกลบนั้นจะหยุดการแสดงผล</span><span class="sxs-lookup"><span data-stu-id="1d7ea-122">If a Power BI visual from ApSource or a file is deleted from the repository, any existing reports that use the deleted visual will stop rendering.</span></span> <span data-ttu-id="1d7ea-123">ไม่สามารถย้อนกลับการลบจากที่เก็บได้</span><span class="sxs-lookup"><span data-stu-id="1d7ea-123">Deleting from the repository isn't reversible.</span></span> <span data-ttu-id="1d7ea-124">หากต้องการปิดใช้งานวิชวล Power BI ชั่วคราวจาก ApSource หรือไฟล์ ให้ใช้คุณลักษณะ "ปิดใช้งาน"</span><span class="sxs-lookup"><span data-stu-id="1d7ea-124">To temporarily disable a Power BI visual from ApSource or a file, use the "Disable" feature.</span></span>

* <span data-ttu-id="1d7ea-125">วิชวล Power BI ขององค์กรไม่ได้รับการสนับสนุนในเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="1d7ea-125">Organizational Power BI visuals are not supported in Power BI report server.</span></span>

<span data-ttu-id="1d7ea-126">ผู้ใช้ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="1d7ea-126">End user:</span></span>

* <span data-ttu-id="1d7ea-127">ส่วนการแสดงผล Power BI ขององค์กรเป็นวิชวลส่วนตัว ที่นำเข้ามาจากที่จัดเก็บขององค์กร</span><span class="sxs-lookup"><span data-stu-id="1d7ea-127">Organizational Power BI visuals are private visuals imported from the organization repository.</span></span> <span data-ttu-id="1d7ea-128">ด้วยความที่เป็นวิชวลส่วนตัว จึงไม่อาจ[นำออกไปยัง PowerPoint](../../consumer/end-user-powerpoint.md) หรือแสดงในอีเมลที่รับเข้าเมื่อผู้ใช้[สมัครใช้งานหน้ารายงาน](../../consumer/end-user-subscribe.md)ได้</span><span class="sxs-lookup"><span data-stu-id="1d7ea-128">As any private visual they can't be [exported to PowerPoint](../../consumer/end-user-powerpoint.md) or displayed in emails received when a user [subscribes to report pages](../../consumer/end-user-subscribe.md).</span></span> <span data-ttu-id="1d7ea-129">เฉพาะ[ส่วนการแสดงผล Power BI ที่ได้รับการรับรอง](power-bi-custom-visuals-certified.md)ที่นำเข้าโดยตรงจาก Marketplace เท่านั้นจึงจะรองรับฟีเจอร์เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="1d7ea-129">Only [certified Power BI visuals](power-bi-custom-visuals-certified.md) imported directly from the marketplace supports these features.</span></span>

* <span data-ttu-id="1d7ea-130">การแสดงผลด้วยภาพของ Visio, ภาพของ PowerApps และภาพของ GlobeMap จาก AppSource Marketplace จะไม่แสดงผล ถ้ามีการเรียกใช้งานผ่านที่เก็บขององค์กร</span><span class="sxs-lookup"><span data-stu-id="1d7ea-130">Visio visual, PowerApps visual, the Map box visual, and the GlobeMap visual from AppSource marketplace don't render if deployed through the organization repository.</span></span>

## <a name="troubleshoot"></a><span data-ttu-id="1d7ea-131">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="1d7ea-131">Troubleshoot</span></span>

<span data-ttu-id="1d7ea-132">สำหรับข้อมูลเกี่ยวกับการแก้ไข เยี่ยมชม [แก้ไขปัญหาการแสดงผล Power BI ของคุณ](power-bi-custom-visuals-troubleshoot.md)</span><span class="sxs-lookup"><span data-stu-id="1d7ea-132">For information about troubleshooting, visit [Troubleshooting your Power BI visuals](power-bi-custom-visuals-troubleshoot.md).</span></span>

## <a name="faq"></a><span data-ttu-id="1d7ea-133">คำถามที่ถามบ่อย</span><span class="sxs-lookup"><span data-stu-id="1d7ea-133">FAQ</span></span>

<span data-ttu-id="1d7ea-134">สำหรับข้อมูลเพิ่มเติมและคำตอบที่คุณอยากรู้ โปรดเยี่ยมชม[คำถามที่ถามบ่อยเกี่ยวกับส่วนการแสดงผล Power BI](power-bi-custom-visuals-faq.md#organizational-power-bi-visuals)</span><span class="sxs-lookup"><span data-stu-id="1d7ea-134">For more information and answers to questions, visit [Frequently asked questions about Power BI visuals](power-bi-custom-visuals-faq.md#organizational-power-bi-visuals).</span></span>

<span data-ttu-id="1d7ea-135">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="1d7ea-135">More questions?</span></span> <span data-ttu-id="1d7ea-136">[ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="1d7ea-136">[Try the Power BI Community](https://community.powerbi.com/).</span></span>