---
title: ภาพรวมของการดูแลระบบ เซิร์ฟเวอร์รายงาน Power BI
description: บทความนี้เป็นภาพรวมของการดูแลระบบเซิร์ฟเวอร์รายงาน Power BI ที่ตั้งอยู่ภายในองค์กรสำหรับจัดเก็บและจัดการ รายงาน Power BI, Power BI สำหรับอุปกรณ์เคลื่อนที่ และรายงานที่มีการแบ่งหน้า
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: conceptual
ms.date: 05/22/2019
ms.openlocfilehash: a1c8e11fbf3b157a0d9fc1a897347875b82226fa
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96387269"
---
# <a name="admin-overview-power-bi-report-server"></a><span data-ttu-id="2b168-103">ภาพรวมของการดูแลระบบ เซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="2b168-103">Admin overview, Power BI Report Server</span></span>
<span data-ttu-id="2b168-104">บทความนี้เป็นภาพรวมของการดูแลระบบเซิร์ฟเวอร์รายงาน Power BI ที่ตั้งอยู่ภายในองค์กรสำหรับจัดเก็บและจัดการ รายงาน Power BI, Power BI สำหรับอุปกรณ์เคลื่อนที่ และรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="2b168-104">This article is the administration overview of Power BI Report Server, an on-premises location for storing and managing your Power BI, mobile, and paginated reports.</span></span> <span data-ttu-id="2b168-105">บทความนี้แนะนำแนวคิดของการวางแผน การปรับใช้ และการจัดการเซิร์ฟเวอร์รายงาน Power BI ของคุณ พร้อมลิงก์ไปยังข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2b168-105">This article introduces concepts of planning, deploying, and managing your Power BI Report Server, with links to more information.</span></span>

![ภาพหน้าจอของเซิร์ฟเวอร์รายงาน Power BI ที่แสดงตัวเลือกการลงชื่อเข้าใช้](media/admin-handbook-overview/admin-handbook.png)
 
## <a name="installing-and-migration"></a><span data-ttu-id="2b168-107">การติดตั้งและการโยกย้าย</span><span class="sxs-lookup"><span data-stu-id="2b168-107">Installing and migration</span></span>
<span data-ttu-id="2b168-108">คุณต้องติดตั้งเซิร์ฟเวอร์รายงาน Power BI เพื่อเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2b168-108">You need to install Power BI Report Server to start using it.</span></span> <span data-ttu-id="2b168-109">เรามีบทความที่อธิบายวิธีติดตั้งนี้</span><span class="sxs-lookup"><span data-stu-id="2b168-109">We have articles that explain how to handle this task.</span></span>

<span data-ttu-id="2b168-110">ก่อนที่คุณจะเริ่มการติดตั้ง, อัปเกรด หรือโยกย้ายไปยังเซิร์ฟเวอร์รายงาน Power BI ให้ดู[ความต้องการของระบบ](system-requirements.md)สำหรับเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="2b168-110">Before you start to install, upgrade, or migrate to Power BI Report Server, take a look at the [system requirements](system-requirements.md) for the report server.</span></span>

### <a name="installing"></a><span data-ttu-id="2b168-111">กำลังติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="2b168-111">Installing</span></span>
<span data-ttu-id="2b168-112">ถ้าคุณกำลังปรับใช้เซิร์ฟเวอร์รายงาน Power BI ใหม่ ให้ใช้เอกสารต่อไปนี้เพื่อช่วยคุณ</span><span class="sxs-lookup"><span data-stu-id="2b168-112">If you are deploying a new Power BI Report Server, you use the following document to help you.</span></span> 

[<span data-ttu-id="2b168-113">ติดตั้ง Power BI Report Server</span><span class="sxs-lookup"><span data-stu-id="2b168-113">Install Power BI Report Server</span></span>](install-report-server.md)

### <a name="migration"></a><span data-ttu-id="2b168-114">การโยกย้าย</span><span class="sxs-lookup"><span data-stu-id="2b168-114">Migration</span></span>
<span data-ttu-id="2b168-115">ไม่มีการอัปเกรดแบบแทนที่สำหรับ SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="2b168-115">There is no in-place upgrade for SQL Server Reporting Services.</span></span> <span data-ttu-id="2b168-116">ถ้าคุณมีอินสแตนซ์ของ SQL Server Reporting Services ที่คุณต้องการทำให้เป็นเซิร์ฟเวอร์รายงาน Power BI คุณต้องทำการโยกย้าย</span><span class="sxs-lookup"><span data-stu-id="2b168-116">If you have an existing SQL Server Reporting Services instance that you want to make a Power BI Report Server, you need to migrate it.</span></span> <span data-ttu-id="2b168-117">คุณอาจต้องทำการโยกย้ายด้วยเหตุผลอื่นเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="2b168-117">You may want to perform a migration for other reasons as well.</span></span> <span data-ttu-id="2b168-118">ทบทวนเอกสารการโยกย้ายสำหรับรายละเอียดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2b168-118">Review the migration document for more details.</span></span>

[<span data-ttu-id="2b168-119">โยกย้ายการติดตั้งเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="2b168-119">Migrate a report server installation</span></span>](migrate-report-server.md)

## <a name="configuring-your-report-server"></a><span data-ttu-id="2b168-120">กำหนดค่าเซิร์ฟเวอร์รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="2b168-120">Configuring your report server</span></span>
<span data-ttu-id="2b168-121">คุณมีหลายตัวเลือกเมื่อทำการกำหนดค่าเซิร์ฟเวอร์รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="2b168-121">You have many options when configuring your report server.</span></span> <span data-ttu-id="2b168-122">คุณจะใช้ SSL หรือไม่</span><span class="sxs-lookup"><span data-stu-id="2b168-122">Will you use SSL?</span></span> <span data-ttu-id="2b168-123">คุณกำลังกำหนดค่าเซิร์ฟเวอร์อีเมลใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="2b168-123">Are you configuring an email server?</span></span> <span data-ttu-id="2b168-124">คุณต้องการรวมเข้ากับบริการ Power BI เพื่อปักหมุดการแสดงภาพหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2b168-124">Do you want to integrate with the Power BI service to pin visualizations?</span></span>

<span data-ttu-id="2b168-125">ส่วนใหญ่ของการกำหนดค่าจะเกิดขึ้นภายในตัวจัดการการกำหนดค่าเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="2b168-125">The majority of your configuration will occur within the Report Server Configuration Manager.</span></span> <span data-ttu-id="2b168-126">ลองดูเอกสารประกอบ[การจัดการการกำหนดค่า](/sql/reporting-services/install-windows/reporting-services-configuration-manager-native-mode)สำหรับรายละเอียดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2b168-126">Check out the [configuration manager](/sql/reporting-services/install-windows/reporting-services-configuration-manager-native-mode) documentation for more details.</span></span>

## <a name="security"></a><span data-ttu-id="2b168-127">ความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="2b168-127">Security</span></span>
<span data-ttu-id="2b168-128">ความปลอดภัยและการป้องกันมีความสำคัญสำหรับทุกองค์กร</span><span class="sxs-lookup"><span data-stu-id="2b168-128">Security and protection are important to every organization.</span></span> <span data-ttu-id="2b168-129">คุณสามารถเรียนรู้เกี่ยวกับการรับรองความถูกต้อง การอนุญาต บทบาท และสิทธิ์ได้ในเอกสารประกอบด้าน[ความปลอดภัย](/sql/reporting-services/security/reporting-services-security-and-protection)</span><span class="sxs-lookup"><span data-stu-id="2b168-129">You can learn about authentication, authorization, roles, and permissions over in the [security](/sql/reporting-services/security/reporting-services-security-and-protection) documentation.</span></span>

## <a name="next-steps"></a><span data-ttu-id="2b168-130">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="2b168-130">Next steps</span></span>
[<span data-ttu-id="2b168-131">ติดตั้ง Power BI Report Server</span><span class="sxs-lookup"><span data-stu-id="2b168-131">Install Power BI Report Server</span></span>](install-report-server.md)  
[<span data-ttu-id="2b168-132">ค้นหาคีย์ผลิตภัณฑ์ของเซิร์ฟเวอร์รายงานคุณ</span><span class="sxs-lookup"><span data-stu-id="2b168-132">Find your report server product key</span></span>](find-product-key.md)  
[<span data-ttu-id="2b168-133">ติดตั้ง Power BI Desktop ที่ปรับให้เหมาะสำหรับ Power BI Report Server</span><span class="sxs-lookup"><span data-stu-id="2b168-133">Install Power BI Desktop optimized for Power BI Report Server</span></span>](install-powerbi-desktop.md)  
[<span data-ttu-id="2b168-134">ดาวน์โหลดตัวสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="2b168-134">Download Report Builder</span></span>](https://www.microsoft.com/download/details.aspx?id=53613)  
[<span data-ttu-id="2b168-135">ดาวน์โหลด SQL Server Data Tools (SSDT)</span><span class="sxs-lookup"><span data-stu-id="2b168-135">Download SQL Server Data Tools (SSDT)</span></span>](/sql/ssdt/download-sql-server-data-tools-ssdt)

<span data-ttu-id="2b168-136">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2b168-136">More questions?</span></span> [<span data-ttu-id="2b168-137">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="2b168-137">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)