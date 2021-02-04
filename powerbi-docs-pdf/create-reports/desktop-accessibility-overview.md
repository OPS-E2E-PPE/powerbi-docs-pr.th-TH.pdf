---
title: ข้อมูลทั่วไปเกี่ยวกับการเข้าถึงใน Power BI
description: 'คุณลักษณะและคำแนะนำสำหรับการสร้างรายงาน Power BI Desktop ที่สามารถเข้าถึงได้ รวมถึงข้อกำหนดการทำให้เนื้อหาเว็บสามารถเข้าถึงและใช้ประโยชน์ได้ (Web Content Accessibility Guidelines: WCAG)'
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: conceptual
ms.date: 02/21/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 3c07f27e1ed4a0a1d509aa93a67b2584ad20a6cc
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96417531"
---
# <a name="overview-of-accessibility-in-power-bi"></a><span data-ttu-id="73b92-103">ข้อมูลทั่วไปเกี่ยวกับการเข้าถึงใน Power BI</span><span class="sxs-lookup"><span data-stu-id="73b92-103">Overview of accessibility in Power BI</span></span>

<span data-ttu-id="73b92-104">เมื่อทำงานกับ Power BI ให้พิจารณาผู้ใช้ประเภทต่างๆ ที่อาจโต้ตอบกับรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="73b92-104">When working with Power BI, consider the different types of users who may interact with your reports.</span></span> <span data-ttu-id="73b92-105">คุณสามารถสร้างรายงานที่สำรวจและเข้าใจได้ง่ายโดยผู้ใช้คีย์บอร์ดหรือโปรแกรมอ่านหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="73b92-105">You can create reports that are easily navigated and understood by keyboard or screen reader users.</span></span> <span data-ttu-id="73b92-106">รายงานดังกล่าวช่วยให้ผู้ใช้ที่อาจมีความบกพร่องทางสายตาหรือทางกายภาพได้รับประโยชน์จากรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="73b92-106">Such reports enable users who may have visual or physical impairments to benefit from your reports.</span></span>

![การตั้งค่าความคมชัดสูงใน Windows](media/desktop-accessibility/accessibility-05b.png)

<span data-ttu-id="73b92-108">บทความนี้แสดงภาพรวมของ Power BI และการช่วยสำหรับการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="73b92-108">This article provides an overview of Power BI and accessibility.</span></span> <span data-ttu-id="73b92-109">บทความเพิ่มเติมมีคำแนะนำและเครื่องมือที่สามารถช่วยคุณสร้างรายงานที่ยอดเยี่ยมโดยคำนึงถึงการช่วยสำหรับการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="73b92-109">Additional articles provide guidance, and tools, that can help you create great reports with accessibility in mind.</span></span>

## <a name="universal-design"></a><span data-ttu-id="73b92-110">การออกแบบสากล</span><span class="sxs-lookup"><span data-stu-id="73b92-110">Universal design</span></span>

<span data-ttu-id="73b92-111">การออกแบบสากลคือการออกแบบผลิตภัณฑ์ที่ผู้ใช้สามารถใช้ได้มากที่สุดเท่าที่จะทำได้ โดยไม่จำเป็นต้องมีการปรับให้เหมาะสมหรือการออกแบบพิเศษ</span><span class="sxs-lookup"><span data-stu-id="73b92-111">Universal design is the design of products that are usable by as many people as reasonable possible, without the need for special adaptation or specialized design.</span></span> <span data-ttu-id="73b92-112">เมื่อสร้างรายงานหรือประสบการณ์การใช้งานใน Power BI เป็นสิ่งสำคัญที่ต้องพิจารณาความต้องการของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="73b92-112">When creating reports or experiences in Power BI, it’s important to consider the needs of your users.</span></span> <span data-ttu-id="73b92-113">การออกแบบประสบการณ์ที่เข้าถึงได้ไม่เพียง แต่จะเป็นประโยชน์ต่อผู้ใช้ที่อาจมีปัญหาด้านการได้ยิน การเคลื่อนไหว การรับรู้ หรือความบกพร่องทางสายตา</span><span class="sxs-lookup"><span data-stu-id="73b92-113">Designing an accessible experience won't only benefit your end users who may have hearing, motor, cognitive, or visual impairments.</span></span> <span data-ttu-id="73b92-114">ซึ่งสามารถช่วยผู้ใช้ทั้งหมดในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="73b92-114">It can help all the end users in your organization.</span></span> <span data-ttu-id="73b92-115">Power BI มีเครื่องมือในการสร้างและใช้รายงานที่เข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="73b92-115">Power BI gives you the tools to make and consume accessible reports.</span></span> <span data-ttu-id="73b92-116">ซึ่งขึ้นอยู่กับคุณในฐานะผู้สร้างรายงานที่จะใช้เครื่องมือเหล่านั้นเพื่อพัฒนาประสบการณ์การใช้งานของทุกคน</span><span class="sxs-lookup"><span data-stu-id="73b92-116">It’s up to you, as a report creator, to use those tools to improve everyone’s experience.</span></span>

## <a name="accessibility-standards"></a><span data-ttu-id="73b92-117">มาตรฐานการช่วยสำหรับการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="73b92-117">Accessibility standards</span></span>

<span data-ttu-id="73b92-118">Power BI จะปฏิบัติตามมาตรฐานการช่วยสำหรับการเข้าถึงต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="73b92-118">Power BI is committed to the following accessibility standards.</span></span> <span data-ttu-id="73b92-119">มาตรฐานนี้จะช่วยให้แน่ใจว่าประสบการณ์การใช้งาน Power BI สามารถเข้าถึงได้หลายคนเท่าที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="73b92-119">The standards help ensure that your Power BI experiences are accessible to as many people as possible.</span></span> <span data-ttu-id="73b92-120">เมื่อคุณสร้างรายงานหรือแดชบอร์ดที่สามารถเข้าถึงได้ เนื้อหานั้นจะสามารถเข้าถึงได้สำหรับทุกคนที่ดูรายงานดังกล่าวผ่าน Power BI บนมือถือ</span><span class="sxs-lookup"><span data-stu-id="73b92-120">When you build accessible reports or dashboards, that content is accessible for anyone who views them using Power BI Mobile.</span></span>

### <a name="wcag-21"></a><span data-ttu-id="73b92-121">WCAG 2.1</span><span class="sxs-lookup"><span data-stu-id="73b92-121">WCAG 2.1</span></span>

<span data-ttu-id="73b92-122">ข้อกำหนดการทำให้เนื้อหาเว็บสามารถเข้าถึงและใช้ประโยชน์ได้ (WCAG) ช่วยให้เนื้อหาบนเว็บสามารถเข้าถึงบุคคลที่มีความบกพร่องได้</span><span class="sxs-lookup"><span data-stu-id="73b92-122">Web Content Accessibility Guidelines (WCAG) help make web content accessible to people with disabilities.</span></span> <span data-ttu-id="73b92-123">ต่อไปนี้คือหลักการสำคัญของข้อกำหนด:</span><span class="sxs-lookup"><span data-stu-id="73b92-123">The following are key principles of the guidelines:</span></span>

1. <span data-ttu-id="73b92-124">**สามารถรับรู้ได้**</span><span class="sxs-lookup"><span data-stu-id="73b92-124">**Perceivable**.</span></span> <span data-ttu-id="73b92-125">ข้อมูลและคอมโพเนนต์ส่วนติดต่อผู้ใช้จะต้องแสดงให้ผู้ใช้เห็นวิธีการที่พวกเขาสามารถรับรู้ได้</span><span class="sxs-lookup"><span data-stu-id="73b92-125">Information and user interface components must be presentable to users in ways they can perceive.</span></span>
2. <span data-ttu-id="73b92-126">**สามารถใช้งานได้**</span><span class="sxs-lookup"><span data-stu-id="73b92-126">**Operable**.</span></span> <span data-ttu-id="73b92-127">คอมโพเนนต์ส่วนติดต่อผู้ใช้และการนำทางต้องเป็นสามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="73b92-127">User interface components and navigation must be operable.</span></span>
3. <span data-ttu-id="73b92-128">**สามารถเข้าใจได้**</span><span class="sxs-lookup"><span data-stu-id="73b92-128">**Understandable**.</span></span> <span data-ttu-id="73b92-129">ข้อมูลและการทำงานของส่วนติดต่อผู้ใช้จะต้องเข้าใจได้</span><span class="sxs-lookup"><span data-stu-id="73b92-129">Information and the operation of user interface must be understandable.</span></span>

### <a name="us-section-508"></a><span data-ttu-id="73b92-130">US Section 508</span><span class="sxs-lookup"><span data-stu-id="73b92-130">US Section 508</span></span>

<span data-ttu-id="73b92-131">US Section 508 เป็นมาตรฐานที่กำหนดให้รัฐบาลและหน่วยงานภาครัฐต้องทำให้เทคโนโลยีอิเล็กทรอนิกส์และข้อมูลของตนสามารถเข้าถึงบุคคลที่ทุพพลภาพได้</span><span class="sxs-lookup"><span data-stu-id="73b92-131">US Section 508 is a standard that requires governments and federal agencies to make their electronic and information technology accessible to people with disabilities.</span></span>

### <a name="en-301-549"></a><span data-ttu-id="73b92-132">EN 301 549</span><span class="sxs-lookup"><span data-stu-id="73b92-132">EN 301 549</span></span>

<span data-ttu-id="73b92-133">EN 301 549 เป็นมาตรฐานยุโรปที่สอดคล้องสำหรับข้อกำหนดการช่วยสำหรับการเข้าถึงผลิตภัณฑ์และบริการ ICT</span><span class="sxs-lookup"><span data-stu-id="73b92-133">EN 301 549 is the Harmonized European Standard for Accessibility requirements for ICT products and services.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="73b92-134">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="73b92-134">Next steps</span></span>

<span data-ttu-id="73b92-135">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับความสามารถในการเข้าถึงของ Power BI โปรดดูแหล่งทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="73b92-135">For more information about Power BI accessibility, see the following resources:</span></span>

* [<span data-ttu-id="73b92-136">ออกแบบรายงาน Power BI สำหรับความสามารถในการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="73b92-136">Design Power BI reports for accessibility</span></span>](desktop-accessibility-creating-reports.md)
* [<span data-ttu-id="73b92-137">ใช้รายงาน Power BI ด้วยคุณลักษณะความสามารถในการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="73b92-137">Consume Power BI reports by using accessibility features</span></span>](desktop-accessibility-consuming-tools.md)
* [<span data-ttu-id="73b92-138">สร้างรายงานใน Power BI โดยใช้เครื่องมือช่วยสำหรับการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="73b92-138">Creating reports in Power BI using accessibility tools</span></span>](desktop-accessibility-creating-tools.md)
* [<span data-ttu-id="73b92-139">แป้นพิมพ์ลัดใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="73b92-139">Keyboard shortcuts in Power BI Desktop</span></span>](desktop-accessibility-keyboard-shortcuts.md)
* [<span data-ttu-id="73b92-140">รายการตรวจสอบการช่วยสำหรับการเข้าถึงรายงาน</span><span class="sxs-lookup"><span data-stu-id="73b92-140">Report accessibility checklist</span></span>](desktop-accessibility-creating-reports.md#report-accessibility-checklist)


