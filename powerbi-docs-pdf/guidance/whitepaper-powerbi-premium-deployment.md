---
title: การปรับใช้งานและการจัดการความจุของ Power BI Premium
description: ทำความเข้าใจศักยภาพของ Power BI Premium และเรียนรู้วิธีการออกแบบ ปรับใช้ ตรวจสอบ และแก้ไขปัญหาโซลูชันที่ปรับขนาดได้
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-premium
ms.topic: conceptual
ms.date: 03/06/2019
LocalizationGroup: Premium
ms.openlocfilehash: 70584413a63f8566137b5e71cdd86011ac6c1acc
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96416473"
---
# <a name="deploying-and-managing-power-bi-premium-capacities"></a><span data-ttu-id="f0dd6-103">การปรับใช้งานและการจัดการความจุของ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="f0dd6-103">Deploying and Managing Power BI Premium Capacities</span></span>

<span data-ttu-id="f0dd6-104">เราได้ยกเลิกเอกสารทางเทคนิคของ Power BI Premium เพื่อให้ได้ข้อมูลล่าสุดในบทความที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="f0dd6-104">We have retired the Power BI Premium whitepaper in favor of providing up-to-date information in separate articles.</span></span> <span data-ttu-id="f0dd6-105">ใช้ตารางต่อไปนี้เพื่อค้นหาเนื้อหาจากเอกสารทางเทคนิค</span><span class="sxs-lookup"><span data-stu-id="f0dd6-105">Use the following table to find content from the whitepaper.</span></span> 

| <span data-ttu-id="f0dd6-106">บทความ</span><span class="sxs-lookup"><span data-stu-id="f0dd6-106">Articles</span></span> | <span data-ttu-id="f0dd6-107">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f0dd6-107">Description</span></span> |
|-----|----|
| [<span data-ttu-id="f0dd6-108">แนวคิดพื้นฐานสำหรับนักออกแบบในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="f0dd6-108">Basic concepts for designers in the Power BI service</span></span>](../fundamentals/service-basic-concepts.md)</br>[<span data-ttu-id="f0dd6-109">ชุดข้อมูลในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="f0dd6-109">Datasets in the Power BI service</span></span>](../connect-data/service-datasets-understand.md)</br>[<span data-ttu-id="f0dd6-110">โหมดชุดข้อมูลในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="f0dd6-110">Dataset modes in the Power BI service</span></span>](../connect-data/service-dataset-modes-understand.md) | <span data-ttu-id="f0dd6-111">ข้อมูลพื้นหลังเกี่ยวกับความจุบริการของ Power BI พื้นที่ทำงานแดชบอร์ดรายงานเวิร์กบุ๊กชุดข้อมูลและกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f0dd6-111">Background information about Power BI service capacities, workspaces,   dashboards, reports, workbooks, datasets, and dataflows.</span></span> |
| [<span data-ttu-id="f0dd6-112">Power BI Premium คืออะไร?</span><span class="sxs-lookup"><span data-stu-id="f0dd6-112">What is Power BI Premium?</span></span>](../admin/service-premium-what-is.md) | <span data-ttu-id="f0dd6-113">ภาพรวมของ Power BI Premium ครอบคลุมพื้นฐานของความจุเฉพาะปริมาณงานที่ได้รับการสนับสนุนการแชร์เนื้อหาแบบไม่จำกัดและคุณลักษณะอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f0dd6-113">An overview of Power BI Premium, covering the basics of dedicated   capacities, supported workloads, unlimited content sharing, and other   features.</span></span>  |
| [<span data-ttu-id="f0dd6-114">การจัดการความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="f0dd6-114">Managing Premium capacities</span></span>](../admin/service-premium-capacity-manage.md)</br>[<span data-ttu-id="f0dd6-115">กำหนดค่าและจัดการความจุใน Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="f0dd6-115">Configure and manage capacities in Power BI Premium</span></span>](../admin/service-admin-premium-manage.md)
</br>[<span data-ttu-id="f0dd6-116">กำหนดค่าปริมาณงานในกำลังการผลิตแบบ Premium</span><span class="sxs-lookup"><span data-stu-id="f0dd6-116">Configure workloads in a Premium capacity</span></span>](../admin/service-admin-premium-workloads.md) | <span data-ttu-id="f0dd6-117">ข้อมูลรายละเอียดเกี่ยวกับการกำหนดค่าและการจัดการความจุและปริมาณงาน</span><span class="sxs-lookup"><span data-stu-id="f0dd6-117">Detailed information about configuring and managing capacities and workloads.</span></span> |
| [<span data-ttu-id="f0dd6-118">การปรับความจุแบบพรีเมียมให้เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="f0dd6-118">Optimizing Premium capacities</span></span>](../admin/service-premium-capacity-optimize.md) | <span data-ttu-id="f0dd6-119">แนวทางปฏิบัติที่ดีที่สุดสำหรับการปรับให้เหมาะสมประสิทธิภาพการทำงานแบบจำลองการวางแผนความจุและวิธีการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="f0dd6-119">Best practices for performance optimization, optimizing models, capacity   planning, and testing approaches.</span></span> |
| [<span data-ttu-id="f0dd6-120">สถานการณ์ความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="f0dd6-120">Premium capacity scenarios</span></span>](../admin/service-premium-capacity-scenarios.md) | <span data-ttu-id="f0dd6-121">ปัญหาที่พบบ่อยในสถานการณ์จริงในโลกโดยเน้นที่การระบุและแก้ไขปัญหาเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="f0dd6-121">Common issues in real-world scenarios, with a focus on identifying and   resolving those issues.</span></span> |
| [<span data-ttu-id="f0dd6-122">ตรวจสอบความจุในพอร์ทัลผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="f0dd6-122">Monitor capacities in the Admin portal</span></span>](../admin/service-admin-premium-monitor-portal.md) | <span data-ttu-id="f0dd6-123">ตรวจสอบด้วยแอปเมตริกความจุของ Power BI Premium และแปลเมตริกที่คุณเห็นในแอป</span><span class="sxs-lookup"><span data-stu-id="f0dd6-123">Monitoring with Power BI Premium Capacity Metrics app, and interpreting   the metrics you see in the app.</span></span> |
| [<span data-ttu-id="f0dd6-124">คำถามที่ถามบ่อยสำหรับ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="f0dd6-124">Power BI Premium FAQ</span></span>](../admin/service-premium-faq.md) | <span data-ttu-id="f0dd6-125">คำตอบสำหรับคำถามรอบการซื้อและสิทธิ์การใช้งานคุณลักษณะและสถานการณ์ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="f0dd6-125">Answers to questions around purchase and licensing, features, and common   scenarios.</span></span> |
| | |
