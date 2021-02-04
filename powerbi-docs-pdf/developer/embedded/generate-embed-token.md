---
title: ข้อควรพิจารณาสําหรับการสร้างโทเค็นแบบฝังตัวในการวิเคราะห์แบบฝังตัวของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: เรียนรู้เกี่ยวกับข้อควรพิจารณา ข้อจำกัด และสิทธิ์ที่จำเป็นสำหรับการสร้างโทเค็นแบบฝัง เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.custom: ''
ms.date: 10/15/2020
ms.openlocfilehash: 2f8da415b40bc5d9a621e5a0df8c1edffbbc8791
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97886867"
---
# <a name="considerations-when-generating-an-embed-token"></a><span data-ttu-id="c092e-104">ข้อควรพิจารณาเมื่อสร้างโทเค็นแบบฝัง</span><span class="sxs-lookup"><span data-stu-id="c092e-104">Considerations when generating an embed token</span></span>

<span data-ttu-id="c092e-105">[สร้างโทเค็น](/rest/api/power-bi/embedtoken) คือ REST API ที่ให้คุณสร้างโทเค็นสำหรับฝังรายการ Power BI ในเว็บแอปหรือพอร์ทัล</span><span class="sxs-lookup"><span data-stu-id="c092e-105">[Generate token](/rest/api/power-bi/embedtoken) is a REST API that lets you generate a token for embedding a Power BI item in a web app or a portal.</span></span> <span data-ttu-id="c092e-106">โทเค็นใช้เพื่ออนุญาตคำขอของคุณกับบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="c092e-106">The token is used to authorize your request against the Power BI service.</span></span>

<span data-ttu-id="c092e-107">API สร้างโทเค็นใช้ข้อมูลประจำตัวเดียว (ผู้ใช้หลักหรือหลักบริการ) เพื่อสร้างโทเค็นสำหรับผู้ใช้แต่ละรายขึ้นอยู่กับข้อมูลรับรองของผู้ใช้ในแอป (ข้อมูลประจำตัวที่มีประสิทธิภาพ)</span><span class="sxs-lookup"><span data-stu-id="c092e-107">The generate token API uses a single identity (a master user or service principal) to generate a token for an individual user, depending on that user's credentials in the app (effective identity).</span></span>

<span data-ttu-id="c092e-108">หลังจากรับรองความถูกต้องสำเร็จแล้วจะได้รับสิทธิ์เข้าถึงข้อมูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c092e-108">After successful authentication, access to the relevant data is granted.</span></span>

>[!NOTE]
><span data-ttu-id="c092e-109">โทเค็นสร้างจะใช้ได้เฉพาะเมื่อคุณ [*ฝังสำหรับลูกค้าของคุณ*](embed-sample-for-customers.md) (หรือที่เรียกว่าสถานการณ์ *แอปเป็นเจ้าของข้อมูล*)</span><span class="sxs-lookup"><span data-stu-id="c092e-109">Generate token is only applicable when you're [*embedding for your customers*](embed-sample-for-customers.md) (also known as the *app owns data* scenario).</span></span>

<span data-ttu-id="c092e-110">คุณสามารถใช้ API ต่อไปนี้เพื่อสร้างโทเค็น:</span><span class="sxs-lookup"><span data-stu-id="c092e-110">You can use the following APIs to generate a token:</span></span>

* [<span data-ttu-id="c092e-111">แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="c092e-111">Dashboards</span></span>](/rest/api/power-bi/embedtoken/dashboards_generatetokeningroup)

* [<span data-ttu-id="c092e-112">ชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c092e-112">Datasets</span></span>](/rest/api/power-bi/embedtoken/datasets_generatetokeningroup)

* [<span data-ttu-id="c092e-113">สร้างโทเค็นสำหรับรายงานหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="c092e-113">Generate token for multiple reports</span></span>](/rest/api/power-bi/embedtoken/generatetoken)


* [<span data-ttu-id="c092e-114">การสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="c092e-114">Report creation</span></span>](/rest/api/power-bi/embedtoken/reports_generatetokenforcreateingroup)

* [<span data-ttu-id="c092e-115">รายงาน</span><span class="sxs-lookup"><span data-stu-id="c092e-115">Reports</span></span>](/rest/api/power-bi/embedtoken/reports_generatetokeningroup)

* [<span data-ttu-id="c092e-116">ไทล์</span><span class="sxs-lookup"><span data-stu-id="c092e-116">Tiles</span></span>](/rest/api/power-bi/embedtoken/tiles_generatetokeningroup)

## <a name="workspace-versions"></a><span data-ttu-id="c092e-117">เวอร์ชันพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c092e-117">Workspace versions</span></span>

<span data-ttu-id="c092e-118">Power BI มีพื้นที่ทำงานสองเวอร์ชันพื้นที่ทำงาน *คลาสสิก* และพื้นที่ทำงาน *ใหม่*</span><span class="sxs-lookup"><span data-stu-id="c092e-118">Power BI has two workspace versions, a *classic* workspace, and a *new* workspace.</span></span> <span data-ttu-id="c092e-119">คุณสามารถเรียนรู้เพิ่มเติมเกี่ยวกับความแตกต่างระหว่างพื้นที่ทำงานเหล่านี้ได้ใน [ความแตกต่างของพื้นที่ทำงานแบบใหม่และแบบคลาสสิก](../../collaborate-share/service-new-workspaces.md#new-and-classic-workspace-differences)</span><span class="sxs-lookup"><span data-stu-id="c092e-119">You can learn more about the differences between these workspaces in [new and classic workspace differences](../../collaborate-share/service-new-workspaces.md#new-and-classic-workspace-differences).</span></span>

<span data-ttu-id="c092e-120">เมื่อสร้างโทเค็นแบบฝังพื้นที่ทำงานที่แตกต่างกันจะมีข้อควรพิจารณาที่แตกต่างกันและต้องการข้อควรพิจารณาที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="c092e-120">When creating an embed token, different workspaces have different considerations and require different permissions.</span></span>

|                  |<span data-ttu-id="c092e-121">พื้นที่ทำงาน *คลาสสิก*</span><span class="sxs-lookup"><span data-stu-id="c092e-121">*Classic* workspace</span></span> |<span data-ttu-id="c092e-122">พื้นที่ทำงาน *ใหม่*</span><span class="sxs-lookup"><span data-stu-id="c092e-122">*New* workspace</span></span>|
|------------------|---------|--------|
|<span data-ttu-id="c092e-123">**ข้อควรพิจารณา**</span><span class="sxs-lookup"><span data-stu-id="c092e-123">**Considerations**</span></span>|<li><span data-ttu-id="c092e-124">ชุดข้อมูลและรายการต้องอยู่ในพื้นที่ทำงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="c092e-124">The dataset and the item must be in the same workspace</span></span></li><li><span data-ttu-id="c092e-125">ไม่สามารถใช้บริการหลักได้</span><span class="sxs-lookup"><span data-stu-id="c092e-125">Service principal cannot be used</span></span></li>  |<span data-ttu-id="c092e-126">ชุดข้อมูลและรายการอาจอยู่ในพื้นที่ทำงาน *ใหม่* สองแห่งที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="c092e-126">The dataset and the item can be in two different *new* workspaces</span></span> |
|<span data-ttu-id="c092e-127">**การอนุญาตของพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="c092e-127">**Workspace permissions**</span></span>|<span data-ttu-id="c092e-128">ผู้ใช้หลักต้องเป็นผู้ดูแลระบบของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c092e-128">The master user must be an admin of the workspace</span></span>  |<span data-ttu-id="c092e-129">บริการหลักหรือผู้ใช้หลักต้องเป็นสมาชิกของพื้นที่ทำงานทั้งสองเป็นอย่างน้อย</span><span class="sxs-lookup"><span data-stu-id="c092e-129">The service principal or master user must be at least a member of both workspaces</span></span> |

>[!NOTE]
>* <span data-ttu-id="c092e-130">คุณไม่สามารถสร้างโทเค็นฝังตัวสำหรับ [พื้นที่ทำงานของฉัน](../../consumer/end-user-workspaces.md#types-of-workspaces)</span><span class="sxs-lookup"><span data-stu-id="c092e-130">You cannot create an embed token for [My workspace](../../consumer/end-user-workspaces.md#types-of-workspaces).</span></span>
>* <span data-ttu-id="c092e-131">คำว่า *รายการ* หมายถึงรายการ Power BI เช่น แดชบอร์ด ไทล์ ถามตอบหรือรายงาน</span><span class="sxs-lookup"><span data-stu-id="c092e-131">The word *item* refers to a Power BI item such as a dashboard, tile, Q&A or report.</span></span>

## <a name="securing-your-data"></a><span data-ttu-id="c092e-132">การรักษาความปลอดภัยข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="c092e-132">Securing your data</span></span>

<span data-ttu-id="c092e-133">เมื่อสร้างโซลูชันของคุณให้พิจารณาสองแนวทางนี้ในการรักษาความปลอดภัยข้อมูลของคุณ:</span><span class="sxs-lookup"><span data-stu-id="c092e-133">When creating your solution, consider these two approaches for securing your data:</span></span>

* [<span data-ttu-id="c092e-134">การแยกตามพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c092e-134">Workspace-based isolation</span></span>](embed-multi-tenancy.md#power-bi-workspace-based-isolation)

* [<span data-ttu-id="c092e-135">การแยกตามการรักษาความปลอดภัยระดับแถว</span><span class="sxs-lookup"><span data-stu-id="c092e-135">Row-level security-based isolation</span></span>](embed-multi-tenancy.md#row-level-security-based-isolation)

<span data-ttu-id="c092e-136">หากคุณจะใช้วิธีการ RLS โปรดอ่าน [ข้อควรพิจารณาและข้อ จำกัด ของ RLS](generate-embed-token.md#row-level-security) ที่ส่วนท้ายของบทความนี้</span><span class="sxs-lookup"><span data-stu-id="c092e-136">If you're going to use the RLS approach, review the [RLS considerations and limitations](generate-embed-token.md#row-level-security) at the end of this article.</span></span>

## <a name="token-permissions"></a><span data-ttu-id="c092e-137">การอนุญาตของโทเค็น</span><span class="sxs-lookup"><span data-stu-id="c092e-137">Token permissions</span></span>

<span data-ttu-id="c092e-138">ใน API สร้างโทเค็นส่วน *GenerateTokenRequest* จะอธิบายถึงการอนุญาตของโทเค็น</span><span class="sxs-lookup"><span data-stu-id="c092e-138">In the generate token APIs, the *GenerateTokenRequest* section describes the token permissions.</span></span>

>[!NOTE]
><span data-ttu-id="c092e-139">การอนุญาตของโทเค็นที่แสดงในส่วนนี้ไม่สามารถใช้ได้กับ API [สร้างโทเค็นสำหรับรายงานหลายรายงาน](/rest/api/power-bi/embedtoken/generatetoken)</span><span class="sxs-lookup"><span data-stu-id="c092e-139">The token permissions listed in this section are not applicable for the [Generate token for multiple reports](/rest/api/power-bi/embedtoken/generatetoken) API.</span></span>

### <a name="access-level"></a><span data-ttu-id="c092e-140">ระดับการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="c092e-140">Access Level</span></span>

<span data-ttu-id="c092e-141">ใช้พารามิเตอร์ *accessLevel* เพื่อกำหนดระดับการเข้าถึงของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c092e-141">Use the *accessLevel* parameter to determine the user's access level.</span></span>

* <span data-ttu-id="c092e-142">**มุมมอง** - มอบการอนุญาตของมุมมองผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c092e-142">**View** - Grant the user viewing permissions.</span></span>

* <span data-ttu-id="c092e-143">**แก้ไข** - ให้การอนุญาตแก่ผู้ใช้ในการดูและแก้ไข (ใช้ได้เฉพาะเมื่อสร้างโทเค็นแบบฝังสำหรับรายงาน)</span><span class="sxs-lookup"><span data-stu-id="c092e-143">**Edit** - Grant the user viewing and editing permissions (only applies when generating an embed token for a report).</span></span>

    <span data-ttu-id="c092e-144">หากคุณกำลังใช้ API [สร้างโทเค็นสำหรับรายงานหลายรายการ](/rest/api/power-bi/embedtoken/generatetoken) ให้ใช้พารามิเตอร์ *allowEdit* เพื่อให้การอนุญาตแก่ผู้ใช้ในการดูและแก้ไข</span><span class="sxs-lookup"><span data-stu-id="c092e-144">If you're using the [Generate token for multiple reports](/rest/api/power-bi/embedtoken/generatetoken) API, use the *allowEdit* parameter to grant the user viewing and editing permissions.</span></span>

* <span data-ttu-id="c092e-145">**สร้าง** - ให้การอนุญาตผู้ใช้ในการสร้างรายงาน (ใช้เฉพาะเมื่อสร้างโทเค็นแบบฝังสำหรับการสร้างรายงาน)</span><span class="sxs-lookup"><span data-stu-id="c092e-145">**Create** - Grant the user permissions to create a report (only applies when generating an embed token for creating a report).</span></span>

    <span data-ttu-id="c092e-146">สำหรับการสร้างรายงานคุณต้องระบุพารามิเตอร์ *datasetId* ด้วย</span><span class="sxs-lookup"><span data-stu-id="c092e-146">For report creation, you must also supply the *datasetId* parameter.</span></span>

### <a name="saving-a-copy-of-the-report"></a><span data-ttu-id="c092e-147">บันทึกสำเนาของรายงาน</span><span class="sxs-lookup"><span data-stu-id="c092e-147">Saving a copy of the report</span></span>

<span data-ttu-id="c092e-148">ใช้บูลีน *allowSaveAs* เพื่อให้ผู้ใช้บันทึกรายงานเป็นรายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="c092e-148">Use the *allowSaveAs* boolean to let users save the report as a new report.</span></span> <span data-ttu-id="c092e-149">การตั้งค่านี้ถูกตั้งค่าเป็น *เท็จ* โดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c092e-149">This setting is set to *false* by default.</span></span>

<span data-ttu-id="c092e-150">พารามิเตอร์นี้ใช้ได้เฉพาะเมื่อสร้างโทเค็นแบบฝังสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="c092e-150">This parameter is only applicable when generating an embed  token for a report.</span></span>

### <a name="row-level-security"></a><span data-ttu-id="c092e-151">การรักษาความปลอดภัยระดับแถว</span><span class="sxs-lookup"><span data-stu-id="c092e-151">Row Level Security</span></span>

<span data-ttu-id="c092e-152">ด้วย [การรักษาความปลอดภัยระดับแถว (RLS)](embedded-row-level-security.md) คุณสามารถเลือกใช้ข้อมูลประจำตัวที่แตกต่างจากข้อมูลประจำตัวของบริการหลักหรือผู้ใช้หลักที่คุณสร้างโทเค็นด้วย</span><span class="sxs-lookup"><span data-stu-id="c092e-152">With [Row Level Security (RLS)](embedded-row-level-security.md), you can choose to use a different identity than the identity of the service principal or master user you're generating the token with.</span></span> <span data-ttu-id="c092e-153">เมื่อใช้ตัวเลือกนี้คุณสามารถแสดงข้อมูลที่ฝังไว้ตามผู้ใช้ที่คุณกำหนดเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="c092e-153">Using this option, you can display embedded information according to the user you're targeting.</span></span> <span data-ttu-id="c092e-154">ตัวอย่างเช่น ในแอปพลิเคชันของคุณ คุณสามารถขอให้ผู้ใช้ลงชื่อเข้าใช้จากนั้นแสดงรายงานที่มีเฉพาะข้อมูลการขายหากผู้ใช้ที่ลงชื่อเข้าใช้เป็นพนักงานขาย</span><span class="sxs-lookup"><span data-stu-id="c092e-154">For example, in your application you can ask users to sign in, and then display a report that only contains sales information if the signed in user is a sales employee.</span></span>

<span data-ttu-id="c092e-155">หากคุณกำลังใช้ RLS ในบางกรณีคุณสามารถละเว้นข้อมูลประจำตัวของผู้ใช้ได้ (พารามิเตอร์ *EffectiveIdentity*)</span><span class="sxs-lookup"><span data-stu-id="c092e-155">If you're using RLS, you can in some cases leave out the user's identity (the *EffectiveIdentity* parameter).</span></span> <span data-ttu-id="c092e-156">สิ่งนี้ช่วยให้โทเค็นสามารถเข้าถึงฐานข้อมูลทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="c092e-156">This allows the token to have access to the entire database.</span></span> <span data-ttu-id="c092e-157">วิธีนี้สามารถใช้เพื่อให้สิทธิ์อนุญาตให้เข้าถึงแก่ผู้ใช้เช่นผู้ดูแลระบบและผู้จัดการซึ่งมีการอนุญาตดูชุดข้อมูลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c092e-157">This method can be used to grant access to users such as admins and managers, who have the permissions to view the entire dataset.</span></span> <span data-ttu-id="c092e-158">อย่างไรก็ตามคุณไม่สามารถใช้วิธีนี้ได้ในทุกสถานการณ์</span><span class="sxs-lookup"><span data-stu-id="c092e-158">However, you cannot use this method in every scenario.</span></span> <span data-ttu-id="c092e-159">ตารางด้านล่างแสดงรายการประเภท RLS ต่าง ๆ และแสดงวิธีการตรวจสอบสิทธิ์ที่สามารถใช้ได้โดยไม่ต้องระบุตัวตนของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c092e-159">The table below lists the different RLS types, and shows which authentication method can be used without specifying a user's identity.</span></span>

<span data-ttu-id="c092e-160">ตารางยังแสดงข้อควรพิจารณาและข้อจำกัดที่เกี่ยวข้องกับ RLS แต่ละประเภท</span><span class="sxs-lookup"><span data-stu-id="c092e-160">The table also shows the considerations and limitation applicable to each RLS type.</span></span>

|<span data-ttu-id="c092e-161">ประเภท RLS</span><span class="sxs-lookup"><span data-stu-id="c092e-161">RLS type</span></span>  |<span data-ttu-id="c092e-162">ฉันสามารถสร้างโทเค็นแบบฝังโดยไม่ระบุ ID ผู้ใช้ที่ใช้ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="c092e-162">Can I generate an embed token without specifying the effective user ID?</span></span>  |<span data-ttu-id="c092e-163">ข้อควรพิจารณาและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="c092e-163">Considerations and limitations</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="c092e-164">การรักษาความปลอดภัยระดับแถวของระบบคลาวด์ (Cloud RLS)</span><span class="sxs-lookup"><span data-stu-id="c092e-164">Cloud Row Level Security (Cloud RLS)</span></span>      |<span data-ttu-id="c092e-165">✔ ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="c092e-165">✔ Master user</span></span><br/><span data-ttu-id="c092e-166">✖ บริการหลัก</span><span class="sxs-lookup"><span data-stu-id="c092e-166">✖ Service principal</span></span>          |         |
|<span data-ttu-id="c092e-167">RDL (รายงานแบบแบ่งหน้า)</span><span class="sxs-lookup"><span data-stu-id="c092e-167">RDL (paginated reports)</span></span>     |<span data-ttu-id="c092e-168">✖ ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="c092e-168">✖ Master user</span></span><br/><span data-ttu-id="c092e-169">✔ บริการหลัก</span><span class="sxs-lookup"><span data-stu-id="c092e-169">✔ Service principal</span></span>        |<span data-ttu-id="c092e-170">คุณไม่สามารถใช้ผู้ใช้หลักเพื่อสร้างโทเค็นฝังสำหรับ RDL ได้</span><span class="sxs-lookup"><span data-stu-id="c092e-170">You cannot use a master user to generate an embed token for RDL.</span></span>         |
|<span data-ttu-id="c092e-171">Analysis Services (AS) การเชื่อมต่อแบบสดในสถานที่</span><span class="sxs-lookup"><span data-stu-id="c092e-171">Analysis Services (AS) on premises live connection</span></span>    |<span data-ttu-id="c092e-172">✔ ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="c092e-172">✔ Master user</span></span><br/><span data-ttu-id="c092e-173">✖ บริการหลัก</span><span class="sxs-lookup"><span data-stu-id="c092e-173">✖ Service principal</span></span>         |<span data-ttu-id="c092e-174">ผู้ใช้ที่สร้างโทเค็นแบบฝังยังต้องการการอนุญาตอย่างใดอย่างหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c092e-174">The user generating the embed token also needs one of the following permissions:</span></span><li><span data-ttu-id="c092e-175">การอนุญาตผู้ดูแลระบบเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="c092e-175">Gateway admin permissions</span></span></li><li><span data-ttu-id="c092e-176">แหล่งข้อมูลเลียนแบบการอนุญาต (*ReadOverrideEffectiveIdentity*)</span><span class="sxs-lookup"><span data-stu-id="c092e-176">Datasource impersonate permission (*ReadOverrideEffectiveIdentity*)</span></span></li>         |
|<span data-ttu-id="c092e-177">Analysis Services (AS) การเชื่อมต่อ Azure live</span><span class="sxs-lookup"><span data-stu-id="c092e-177">Analysis Services (AS) Azure live connection</span></span>    |<span data-ttu-id="c092e-178">✔ ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="c092e-178">✔ Master user</span></span><br/><span data-ttu-id="c092e-179">✖ บริการหลัก</span><span class="sxs-lookup"><span data-stu-id="c092e-179">✖ Service principal</span></span>         |<span data-ttu-id="c092e-180">ไม่สามารถแทนที่ข้อมูลประจำตัวของผู้ใช้ที่สร้างโทเค็นสำหรับฝังได้</span><span class="sxs-lookup"><span data-stu-id="c092e-180">The identity of the user generating the embed token cannot be overridden.</span></span> <span data-ttu-id="c092e-181">ข้อมูลที่กำหนดเองสามารถใช้เพื่อใช้ RLS แบบไดนามิกหรือการกรองที่ปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="c092e-181">Custom data can be used to implement dynamic RLS or secure filtering.</span></span><br/><br/><span data-ttu-id="c092e-182">**หมายเหตุ:** หลักบริการต้องระบุ ID อ็อบเจ็กต์เป็นข้อมูลประจำตัวที่มีประสิทธิภาพ (ชื่อผู้ใช้ RLS)</span><span class="sxs-lookup"><span data-stu-id="c092e-182">**Note:** Service principal must provide its object ID as the effective identity (RLS username).</span></span>         |
|<span data-ttu-id="c092e-183">การลงชื่อเข้าระบบครั้งเดียว (SSO)</span><span class="sxs-lookup"><span data-stu-id="c092e-183">Single Sign On (SSO)</span></span>     |<span data-ttu-id="c092e-184">✔ ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="c092e-184">✔ Master user</span></span><br/><span data-ttu-id="c092e-185">✖ บริการหลัก</span><span class="sxs-lookup"><span data-stu-id="c092e-185">✖ Service principal</span></span>         |<span data-ttu-id="c092e-186">ข้อมูลประจำตัวที่ชัดเจน (SSO) สามารถระบุได้โดยใช้คุณสมบัติ blob ของข้อมูลประจำตัวในอ็อบเจ็กต์เอกลักษณ์ที่มีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="c092e-186">An explicit (SSO) identity can be provided using the identity blob property in an effective identity object</span></span>         |
|<span data-ttu-id="c092e-187">SSO และ cloud RLS</span><span class="sxs-lookup"><span data-stu-id="c092e-187">SSO and cloud RLS</span></span>     |<span data-ttu-id="c092e-188">✔ ผู้ใช้หลัก</span><span class="sxs-lookup"><span data-stu-id="c092e-188">✔ Master user</span></span><br/><span data-ttu-id="c092e-189">✖ บริการหลัก</span><span class="sxs-lookup"><span data-stu-id="c092e-189">✖ Service principal</span></span>         |<span data-ttu-id="c092e-190">คุณต้องระบุดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c092e-190">You must provide the following:</span></span><li><span data-ttu-id="c092e-191">ข้อมูลประจำตัวที่ชัดเจน (SSO) สามารถระบุได้โดยใช้คุณสมบัติ blob ของข้อมูลประจำตัวในใอ็อบเจ็กต์เอกลักษณ์ที่มีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="c092e-191">Explicit (SSO) identity in the identity blob property property in an effective identity object</span></span></li><li><span data-ttu-id="c092e-192">ข้อมูลประจำตัว (RLS) ที่มีประสิทธิภาพ (ชื่อผู้ใช้)</span><span class="sxs-lookup"><span data-stu-id="c092e-192">Effective (RLS) identity (username)</span></span></li>         |

>[!NOTE]
><span data-ttu-id="c092e-193">บริการหลักต้องให้ข้อมูลต่อไปนี้เสมอ:</span><span class="sxs-lookup"><span data-stu-id="c092e-193">Service principal must always provide the following:</span></span>
>* <span data-ttu-id="c092e-194">ข้อมูลประจำตัวสำหรับรายการใด ๆ ที่มีชุดข้อมูล RLS</span><span class="sxs-lookup"><span data-stu-id="c092e-194">An identity for any item with an RLS dataset.</span></span>
>* <span data-ttu-id="c092e-195">สำหรับชุดข้อมูล SSO ข้อมูลประจำตัว RLS ที่มีประสิทธิภาพพร้อมคุณสมบัติชื่อผู้ใช้ที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="c092e-195">For an SSO dataset, an effective RLS identity with the username property defined.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c092e-196">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c092e-196">Next steps</span></span>

>[!div class="nextstepaction"]
>[<span data-ttu-id="c092e-197">ลงทะเบียนแอป</span><span class="sxs-lookup"><span data-stu-id="c092e-197">Register an app</span></span>](register-app.md)

> [!div class="nextstepaction"]
>[<span data-ttu-id="c092e-198">Power BI Embedded สำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="c092e-198">Power BI Embedded for your customers</span></span>](embed-sample-for-customers.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="c092e-199">แอปพลิเคชันและออบเจ็กต์บริการหลักใน Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="c092e-199">Application and service principal objects in Azure Active Directory</span></span>](/azure/active-directory/develop/app-objects-and-service-principals)

>[!div class="nextstepaction"]
>[<span data-ttu-id="c092e-200">ความปลอดภัยระดับแถวโดยใช้เกตเวย์ข้อมูลภายในองค์กรที่มีโครงร่างสำคัญของบริการ</span><span class="sxs-lookup"><span data-stu-id="c092e-200">Row-level security using on-premises data gateway with service principal</span></span>](embedded-row-level-security.md#on-premises-data-gateway-with-service-principal)

>[!div class="nextstepaction"]
>[<span data-ttu-id="c092e-201">ฝังเนื้อหา Power BI ด้วยองค์ประกอบหลักของบริการ</span><span class="sxs-lookup"><span data-stu-id="c092e-201">Embed Power BI content with service principal</span></span>](embed-service-principal.md)