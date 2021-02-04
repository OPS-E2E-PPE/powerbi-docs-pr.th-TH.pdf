---
title: ทำงานกับรายงานในมุมมองการแก้ไข
description: โต้ตอบกับรายงานในมุมมองการแก้ไขรายงานในบริการ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 10/14/2020
LocalizationGroup: Reports
ms.openlocfilehash: f1e162e0002051853081898f548864e751c5b429
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96388390"
---
# <a name="interact-with-a-report-in-editing-view-in-the-power-bi-service"></a><span data-ttu-id="32637-103">โต้ตอบกับรายงานในมุมมองการแก้ไขในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="32637-103">Interact with a report in Editing view in the Power BI service</span></span>

<span data-ttu-id="32637-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span><span class="sxs-lookup"><span data-stu-id="32637-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span></span>

<span data-ttu-id="32637-105">คุณสามารถสร้างและแก้ไขรายงานทั้งในบริการ Power BI และ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="32637-105">You can create and edit reports in both the Power BI service and Power BI Desktop.</span></span> <span data-ttu-id="32637-106">ในบริการ Power BI คุณสร้างและแก้ไขรายงานใน **มุมมองการแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="32637-106">In the Power BI service, you create and edit reports in **Editing view**.</span></span> <span data-ttu-id="32637-107">และใน Power BI Desktop คุณสร้างและแก้ไขรายงานใน [มุมมองรายงาน](desktop-report-view.md)</span><span class="sxs-lookup"><span data-stu-id="32637-107">And in Power BI Desktop, you create and edit reports in [Report view](desktop-report-view.md).</span></span> <span data-ttu-id="32637-108">บทความนี้ครอบคลุมถึงมุมมองการแก้ไขในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="32637-108">This article covers Editing view in the Power BI service.</span></span> 

<span data-ttu-id="32637-109">บริการ Power BI มีสองโหมดสำหรับการโต้ตอบกับรายงาน: [มุมมองการอ่าน](../consumer/end-user-reading-view.md) สำหรับ *ผู้ใช้ทางธุรกิจ* ของรายงาน และมุมมองการแก้ไขสำหรับเจ้าของและผู้สร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="32637-109">The Power BI service has two different modes for interacting with reports: [Reading view](../consumer/end-user-reading-view.md) for report *business users* and Editing view for report owners and creators.</span></span>  <span data-ttu-id="32637-110">คุณจำเป็นต้องใช้สิทธิการใช้งาน Power BI Pro เพื่อแชร์รายงาน รวมถึงแก้ไขรายงานที่ผู้อื่นสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="32637-110">You need a Power BI Pro license to share reports as well as to edit reports created by others.</span></span> <span data-ttu-id="32637-111">ถ้าคุณยังไม่มีสิทธิการใช้งาน Pro คุณยังสามารถสร้างรายงานในพื้นที่ทำงานของฉันได้ แต่คุณจะไม่สามารถ [แชร์รายงาน](../collaborate-share/service-share-reports.md) ได้</span><span class="sxs-lookup"><span data-stu-id="32637-111">Without a Pro license, you can still create reports in your My Workspace, but you can't [share them](../collaborate-share/service-share-reports.md).</span></span>

<span data-ttu-id="32637-112">ในมุมมองการแก้ไขรายงาน คุณสามารถสำรวจและออกแบบรายงานได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="32637-112">In report Editing view, you have lots of flexibility in both exploring and designing a report.</span></span> <span data-ttu-id="32637-113">ฟังก์ชัน [มุมมองการอ่าน](../consumer/end-user-reading-view.md) ทั้งหมดพร้อมใช้งาน และอื่น ๆ อีกมากมาย</span><span class="sxs-lookup"><span data-stu-id="32637-113">All the [Reading view](../consumer/end-user-reading-view.md) functionality is available, plus lots more.</span></span> <span data-ttu-id="32637-114">มุมมองการแก้ไขจะพร้อมใช้งานสำหรับบุคคลที่สร้างรายงานหรือเพื่อนร่วมงานที่เป็นสมาชิก ผู้ดูแลระบบ หรือผู้สนับสนุนของพื้นที่ทำงานที่ใช้จัดเก็บรายงานดังกล่าวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="32637-114">Editing view is only available to the person who created the report or to colleagues who are members, admins, or contributors of the workspace where the report is stored.</span></span> <span data-ttu-id="32637-115">โปรดดู [บทบาทในพื้นที่ทำงานใหม่](../collaborate-share/service-new-workspaces.md#roles-in-the-new-workspaces) สำหรับรายละเอียดเกี่ยวกับสิทธิ์ต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="32637-115">See [Roles in the new workspaces](../collaborate-share/service-new-workspaces.md#roles-in-the-new-workspaces) for details on permissions.</span></span>

## <a name="functionality-only-available-in-editing-view"></a><span data-ttu-id="32637-116">ฟังก์ชันใช้งานได้เฉพาะในมุมมองการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="32637-116">Functionality only available in Editing view</span></span>
<span data-ttu-id="32637-117">ดูรายการของหัวข้อใต้ส่วนหัวของ **รายงาน Power BI** ในสารบัญ</span><span class="sxs-lookup"><span data-stu-id="32637-117">Take a look at the list of topics under the **Power BI reports** header in the Table of Contents.</span></span> <span data-ttu-id="32637-118">ซึ่งเป็นรายการที่ยาวและมีหัวข้อต่าง ๆ มากมายที่ครอบคลุมฟังก์ชันการทำงาน *ที่พร้อมใช้งานเฉพาะเมื่อคุณมีสิทธิ์การแก้ไขสำหรับรายงาน*</span><span class="sxs-lookup"><span data-stu-id="32637-118">It's a long list and many of the topics cover functionality *only available if you have editing permissions for a report*.</span></span>  <span data-ttu-id="32637-119">เพื่อช่วยคุณสำรวจสารบัญ จำเป็นต้องใช้มุมมองการแก้ไขสำหรับการดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="32637-119">To help you navigate the Table of Contents, Editing view is required for the following actions:</span></span>

* <span data-ttu-id="32637-120">สร้าง แก้ไข เปลี่ยนชื่อ แชร์ และการลบรายงาน</span><span class="sxs-lookup"><span data-stu-id="32637-120">Creating, editing, renaming, sharing, and deleting reports.</span></span>
* <span data-ttu-id="32637-121">การเพิ่ม เปลี่ยนชื่อ การจัดเรียง และลบหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="32637-121">Adding, renaming, rearranging, and deleting report pages.</span></span>
* <span data-ttu-id="32637-122">รายงานการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="32637-122">Formatting reports.</span></span>
* <span data-ttu-id="32637-123">เพิ่มการแสดงผลข้อมูลด้วยภาพ กล่องข้อความ รูปร่าง และปุ่มไปยังรายงาน</span><span class="sxs-lookup"><span data-stu-id="32637-123">Adding visualizations, text boxes, shapes, and buttons to a report.</span></span>
* <span data-ttu-id="32637-124">เพิ่มตัวกรอง ระดับภาพ ระดับหน้า และระดับรายงาน และการตั้งค่าการโต้ตอบแบบภาพ</span><span class="sxs-lookup"><span data-stu-id="32637-124">Adding visual-level, page-level, and report-level filters and setting visual interactions.</span></span>
* <span data-ttu-id="32637-125">สร้างกำหนดการการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="32637-125">Creating refresh schedules.</span></span>
* <span data-ttu-id="32637-126">การใช้ฟังก์ชันถามตอบ เพื่อสร้างการแสดงผลด้วยภาพในรายงาน</span><span class="sxs-lookup"><span data-stu-id="32637-126">Using Q&A functionality to create visuals in reports.</span></span>
* <span data-ttu-id="32637-127">แสดงข้อมูลที่ใช้เพื่อสร้างการแสดงผลข้อมูลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="32637-127">Showing data used to create the visualization.</span></span> 
* <span data-ttu-id="32637-128">การตั้งค่าการดูข้อมูลรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="32637-128">Setting up drill through.</span></span>
* <span data-ttu-id="32637-129">ทำซ้ำหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="32637-129">Duplicating a report page.</span></span>
* <span data-ttu-id="32637-130">[การใช้การตั้งค่ารายงาน](power-bi-report-settings.md) เพื่อควบคุมการโต้ตอบของผู้อ่านของคุณกับรายงาน</span><span class="sxs-lookup"><span data-stu-id="32637-130">[Using report settings](power-bi-report-settings.md) to control your readers' interactions with reports.</span></span>

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="32637-131">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="32637-131">Considerations and troubleshooting</span></span>
<span data-ttu-id="32637-132">จำเป็นต้องใช้สิทธิ์การใช้งาน Power BI Pro เพื่อแก้ไขรายงานที่สร้างโดยผู้อื่น รวมถึงการแชร์รายงานกับผู้อื่น</span><span class="sxs-lookup"><span data-stu-id="32637-132">A Power BI Pro license is required to edit reports created by others as well as to share your reports with others.</span></span>  <span data-ttu-id="32637-133">ถ้าคุณยังไม่มีสิทธิการใช้งาน Pro คุณยังสามารถสร้างรายงานแต่คุณไม่สามารถ [แชร์รายงาน](../collaborate-share/service-share-reports.md) ได้</span><span class="sxs-lookup"><span data-stu-id="32637-133">If you don't have a Pro license, you can still create reports, but you can't [share them](../collaborate-share/service-share-reports.md).</span></span>


## <a name="next-steps"></a><span data-ttu-id="32637-134">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="32637-134">Next steps</span></span>

[<span data-ttu-id="32637-135">ความสามารถของ Power BI สำหรับผู้ใช้ทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="32637-135">Power BI capabilities for business users</span></span>](../consumer/end-user-reading-view.md)

<span data-ttu-id="32637-136">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="32637-136">More questions?</span></span> [<span data-ttu-id="32637-137">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="32637-137">Try the Power BI Community</span></span>](https://community.powerbi.com/)
