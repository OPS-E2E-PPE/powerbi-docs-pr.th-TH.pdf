---
title: Row-level security (RLS) กับ Power BI
description: วิธีการกำหนดค่า Row-level security สำหรับชุดข้อมูลที่นำเข้าและ DirectQuery ภายใน Power BI service
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: how-to
ms.date: 09/17/2020
ms.custom: seodec18
LocalizationGroup: Administration
ms.openlocfilehash: f1358cbafa08c0dbb3790322c414d7a746386f0f
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96408584"
---
# <a name="row-level-security-rls-with-power-bi"></a><span data-ttu-id="42376-103">Row-level security (RLS) กับ Power BI</span><span class="sxs-lookup"><span data-stu-id="42376-103">Row-level security (RLS) with Power BI</span></span>

<span data-ttu-id="42376-104">Row-level security (RLS) ด้วย Power BI สามารถใช้เพื่อจำกัดการเข้าถึงข้อมูลสำหรับผู้ใช้ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="42376-104">Row-level security (RLS) with Power BI can be used to restrict data access for given users.</span></span> <span data-ttu-id="42376-105">ตัวกรองจำกัดการเข้าถึงข้อมูลในระดับแถว และคุณสามารถกำหนดตัวกรองภายในบทบาทได้</span><span class="sxs-lookup"><span data-stu-id="42376-105">Filters restrict data access at the row level, and you can define filters within roles.</span></span> <span data-ttu-id="42376-106">ใน Power BI service สมาชิกของพื้นที่ทำงานจะเข้าถึงชุดข้อมูลในพื้นที่ทำงานได้</span><span class="sxs-lookup"><span data-stu-id="42376-106">In the Power BI service, members of a workspace have access to datasets in the workspace.</span></span> <span data-ttu-id="42376-107">RLS ไม่จำกัดการเข้าถึงข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="42376-107">RLS doesn't restrict this data access.</span></span>

<span data-ttu-id="42376-108">คุณสามารถกำหนดค่า RLS สำหรับแบบจำลองข้อมูลที่นำเข้าไปยัง Power BI ด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="42376-108">You can configure RLS for data models imported into Power BI with Power BI Desktop.</span></span> <span data-ttu-id="42376-109">และคุณยังสามารถกำหนดค่า RLS บนชุดข้อมูลที่กำลังใช้ DirectQuery เช่น SQL Server</span><span class="sxs-lookup"><span data-stu-id="42376-109">You can also configure RLS on datasets that are using DirectQuery, such as SQL Server.</span></span> <span data-ttu-id="42376-110">สำหรับการเชื่อมต่อสดของ Analysis Services หรือ Azure Analysis Services คุณกำหนดค่าการรักษาความปลอดภัยระดับแถวในแบบจำลอง ไม่ใช่ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="42376-110">For Analysis Services or Azure Analysis Services lives connections, you configure Row-level security in the model, not in Power BI Desktop.</span></span> <span data-ttu-id="42376-111">ตัวเลือกความปลอดภัยจะไม่แสดงสำหรับชุดข้อมูลแบบการเชื่อมต่อสด</span><span class="sxs-lookup"><span data-stu-id="42376-111">The security option will not show up for live connection datasets.</span></span>

[!INCLUDE [include-short-name](../includes/rls-desktop-define-roles.md)]

<span data-ttu-id="42376-112">ตามค่าเริ่มต้น การกรองการรักษาความปลอดภัยระดับแถวจะใช้ตัวกรองทิศทางเดียว ไม่ว่าการตั้งค่าความสัมพันธ์จะเป็นแบบทิศทางเดียวหรือสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="42376-112">By default, row-level security filtering uses single-directional filters, whether the relationships are set to single direction or bi-directional.</span></span> <span data-ttu-id="42376-113">คุณสามารถเปิดใช้ตัวกรองไขว้แบบสองทิศทางด้วย row-level security ได้ด้วยตนเองโดยการเลือกความสัมพันธ์ และทำเครื่องหมายในกล่อง **ใช้ตัวกรองความปลอดภัยในทั้งสองทิศทาง**</span><span class="sxs-lookup"><span data-stu-id="42376-113">You can manually enable bi-directional cross-filtering with row-level security by selecting the relationship and checking the **Apply security filter in both directions** checkbox.</span></span> <span data-ttu-id="42376-114">ทำเครื่องหมายที่ช่องนี้เมื่อคุณได้ใช้การรักษาความปลอดภัยระดับแถวแบบไดนามิกในระดับเซิร์ฟเวอร์แล้ว โดยที่การรักษาความปลอดภัยระดับแถวจะขึ้นอยู่กับชื่อผู้ใช้หรือรหัสการเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="42376-114">Select this option when you've also implemented dynamic row-level security at the server level, where row-level security is based on username or login ID.</span></span>

<span data-ttu-id="42376-115">สำหรับข้อมูลเพิ่มเติม ดูที่[ตัวกรองไขว้แบบสองทิศทางที่ใช้ DirectQuery ใน Power BI Desktop](../transform-model/desktop-bidirectional-filtering.md)และบทความเชิงเทคนิคของ[การรักษาความปลอดภัยแบบลำจองภาษา BI แบบตาราง](https://download.microsoft.com/download/D/2/0/D20E1C5F-72EA-4505-9F26-FEF9550EFD44/Securing%20the%20Tabular%20BI%20Semantic%20Model.docx)</span><span class="sxs-lookup"><span data-stu-id="42376-115">For more information, see [Bidirectional cross-filtering using DirectQuery in Power BI Desktop](../transform-model/desktop-bidirectional-filtering.md) and the [Securing the Tabular BI Semantic Model](https://download.microsoft.com/download/D/2/0/D20E1C5F-72EA-4505-9F26-FEF9550EFD44/Securing%20the%20Tabular%20BI%20Semantic%20Model.docx) technical article.</span></span>

![ใช้ตัวกรองความปลอดภัย](media/service-admin-rls/rls-apply-security-filter.png)


[!INCLUDE [include-short-name](../includes/rls-desktop-view-as-roles.md)]

## <a name="manage-security-on-your-model"></a><span data-ttu-id="42376-117">จัดการความปลอดภัยบนแบบจำลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="42376-117">Manage security on your model</span></span>

<span data-ttu-id="42376-118">เมื่อต้องจัดการความปลอดภัยบนแบบจำลองข้อมูลของคุณ ให้ทำสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="42376-118">To manage security on your data model, do the following steps:</span></span>

1. <span data-ttu-id="42376-119">ใน Power BI service ให้เลือกเมนู **ตัวเลือกเพิ่มเติม** สำหรับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="42376-119">In the Power BI service, select the **More options** menu for a dataset.</span></span> <span data-ttu-id="42376-120">เมนูนี้จะปรากฏเมื่อชี้ไปที่ชื่อชุดข้อมูล ไม่ว่าคุณจะเลือกจากเมนูนำทางหรือหน้าพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="42376-120">This menu appears when you hover on a dataset name, whether you select it from the navigation menu or the workspace page.</span></span>

    ![เมนูตัวเลือกเพิ่มเติมในพื้นที่ทำงาน](media/service-admin-rls/dataset-leftnav-more-options.png)

    ![เมนูตัวเลือกเพิ่มเติมในเมนูนำทาง](media/service-admin-rls/dataset-canvas-more-options.png)

1. <span data-ttu-id="42376-123">เลือก **ความปลอดภัย**</span><span class="sxs-lookup"><span data-stu-id="42376-123">Select **Security**.</span></span>

   ![เลือก ความปลอดภัย จากเมนูตัวเลือกเพิ่มเติม](media/service-admin-rls/dataset-more-options-menu.png)

<span data-ttu-id="42376-125">ระบบการรักษาความปลอดภัยจะนำคุณไปยังหน้า RLS เพื่อให้คุณเพิ่มสมาชิกให้กับบทบาทที่คุณสร้างไว้ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="42376-125">Security will take you to the RLS page where you add members to a role you created in Power BI Desktop.</span></span> <span data-ttu-id="42376-126">เฉพาะเจ้าของชุดข้อมูลเท่านั้นที่จะเห็นระบบความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="42376-126">Only the owners of the dataset will see Security.</span></span> <span data-ttu-id="42376-127">ถ้าชุดข้อมูลอยู่ในกลุ่ม จะมีเพียงผู้ดูแลระบบ ของกลุ่มเท่านั้นที่จะเห็นตัวเลือกความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="42376-127">If the dataset is in a Group, only administrators of the group will see the security option.</span></span>

<span data-ttu-id="42376-128">คุณสามารถสร้างหรือแก้ไขบทบาทภายใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="42376-128">You can only create or modify roles within Power BI Desktop.</span></span>

## <a name="working-with-members"></a><span data-ttu-id="42376-129">ทำงานกับสมาชิก</span><span class="sxs-lookup"><span data-stu-id="42376-129">Working with members</span></span>

### <a name="add-members"></a><span data-ttu-id="42376-130">เพิ่มสมาชิก</span><span class="sxs-lookup"><span data-stu-id="42376-130">Add members</span></span>

<span data-ttu-id="42376-131">เพิ่มสมาชิกให้กับบทบาทโดยการพิมพ์ลงในที่อยู่อีเมล์หรือชื่อของผู้ใช้ หรือพิมพ์ลงในกลุ่มความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="42376-131">Add a member to the role by typing in the email address or name of the user or security group.</span></span> <span data-ttu-id="42376-132">คุณไม่สามารถเพิ่มกลุ่มที่สร้างขึ้นภายใน Power BI</span><span class="sxs-lookup"><span data-stu-id="42376-132">You can't add Groups created in Power BI.</span></span> <span data-ttu-id="42376-133">คุณสามารถเพิ่มสมาชิก[ภายนอกองค์กรของคุณ](../guidance/whitepaper-azure-b2b-power-bi.md#data-security-for-external-partners)ได้</span><span class="sxs-lookup"><span data-stu-id="42376-133">You can add members [external to your organization](../guidance/whitepaper-azure-b2b-power-bi.md#data-security-for-external-partners).</span></span>

![เพิ่มสมาชิก](media/service-admin-rls/rls-add-member.png)

<span data-ttu-id="42376-135">คุณยังสามารถดูจำนวนสมาชิกที่เป็นส่วนหนึ่งของบทบาทจากเป็นตัวเลขในวงเล็บที่อยู่ถัดจากชื่อบทบาท หรือถัดจากสมาชิก</span><span class="sxs-lookup"><span data-stu-id="42376-135">You can also see how many members are part of the role by the number in parentheses next to the role name, or next to Members.</span></span>

![สมาชิกในบทบาท](media/service-admin-rls/rls-member-count.png)

### <a name="remove-members"></a><span data-ttu-id="42376-137">ลบสมาชิก</span><span class="sxs-lookup"><span data-stu-id="42376-137">Remove members</span></span>

<span data-ttu-id="42376-138">คุณสามารถลบสมาชิกได้โดยการเลือก X ที่อยู่ถัดจากชื่อของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="42376-138">You can remove members by selecting the X next to their name.</span></span> 

![ลบสมาชิกออก](media/service-admin-rls/rls-remove-member.png)

## <a name="validating-the-role-within-the-power-bi-service"></a><span data-ttu-id="42376-140">การตรวจสอบบทบาทภายใน บริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="42376-140">Validating the role within the Power BI service</span></span>

<span data-ttu-id="42376-141">คุณสามารถตรวจสอบว่าบทบาทที่คุณกำหนดทำงานถูกต้องหรือไม่ได้โดยการทดสอบบทบาท</span><span class="sxs-lookup"><span data-stu-id="42376-141">You can validate that the role you defined is working correctly by testing the role.</span></span>

1. <span data-ttu-id="42376-142">เลือก **ตัวเลือกเพิ่มเติม** (...) ที่อยู่ถัดจากบทบาท</span><span class="sxs-lookup"><span data-stu-id="42376-142">Select **More options** (...) next to the role.</span></span>
2. <span data-ttu-id="42376-143">เลือก **ทดสอบข้อมูลแบบเป็นบทบาท**</span><span class="sxs-lookup"><span data-stu-id="42376-143">Select **Test data as role**</span></span>

![ทดสอบในฐานะบทบาท](media/service-admin-rls/rls-test-role.png)

<span data-ttu-id="42376-145">คุณจะเห็นรายงานที่พร้อมใช้งานสำหรับบทบาทนี้</span><span class="sxs-lookup"><span data-stu-id="42376-145">You'll see reports that are available for this role.</span></span> <span data-ttu-id="42376-146">แดชบออร์ดจะไม่แสดงในมุมมองนี้</span><span class="sxs-lookup"><span data-stu-id="42376-146">Dashboards aren't shown in this view.</span></span> <span data-ttu-id="42376-147">ในส่วนหัวเรื่องของหน้า มีการแสดงบทบาทที่ใช้อยู่</span><span class="sxs-lookup"><span data-stu-id="42376-147">In the page header, the role being applied is shown.</span></span>

![ตอนนี้กำลังดูในฐานะเป็น <role>](media/service-admin-rls/rls-test-role2.png)

<span data-ttu-id="42376-149">ทดสอบบทบาทหรือการรวมบทบาทอื่น ๆ ได้โดยการเลือก **ตอนนี้ดูในฐานะ**</span><span class="sxs-lookup"><span data-stu-id="42376-149">Test other roles, or a combination of roles, by selecting **Now viewing as**.</span></span>

![ทดสอบบทบาทอื่น](media/service-admin-rls/rls-test-role3.png)

<span data-ttu-id="42376-151">คุณสามารถเลือกเพื่อดูข้อมูลเป็นรายบุคคลหรือคุณสามารถเลือกการรวมบทบาทที่พร้อมใช้งานเพื่อตรวจสอบว่ากำลังทำงานอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="42376-151">You can choose to view data as a specific person or you can select a combination of available roles to validate they're working.</span></span>

<span data-ttu-id="42376-152">เมื่อต้องการกลับไปยังมุมมองปกติ เลือก **กลับไปยัง Row-Level Security**</span><span class="sxs-lookup"><span data-stu-id="42376-152">To return to normal viewing, select **Back to Row-Level Security**.</span></span>

[!INCLUDE [include-short-name](../includes/rls-usernames.md)]

## <a name="using-rls-with-workspaces-in-power-bi"></a><span data-ttu-id="42376-153">ใช้ RLS กับพื้นที่ทำงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="42376-153">Using RLS with workspaces in Power BI</span></span>

<span data-ttu-id="42376-154">หากคุณเผยแพร่รายงาน Power BI Desktop ของคุณไปยังพื้นที่ทำงานภายใน Power BI service บทบาทดังกล่าวจะถูกนำไปใช้กับสมาชิกแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="42376-154">If you publish your Power BI Desktop report to a workspace in the Power BI service, the roles will be applied to read-only members.</span></span> <span data-ttu-id="42376-155">คุณจะต้องระบุว่าเฉพาะสมาชิกเท่านั้นที่สามารถดูเนื้อหา Power BI ภายในการตั้งค่าพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="42376-155">You'll need to indicate that members can only view Power BI content in the workspace settings.</span></span>

> [!WARNING]
> <span data-ttu-id="42376-156">ถ้าคุณกำหนดค่าพื้นที่ทำงานเพื่อให้สมาชิกมีสิทธิ์ในการแก้ไข บทบาท RLS จะไม่ถูกนำไปใช้กับพื้นที่ทำงานนั้นได้</span><span class="sxs-lookup"><span data-stu-id="42376-156">If you have configured the workspace so that members have edit permissions, the RLS roles won't be applied to them.</span></span> <span data-ttu-id="42376-157">ผู้ใช้สามารถมองเห็นข้อมูลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="42376-157">Users can see all of the data.</span></span>

![การตั้งค่ากลุ่ม](media/service-admin-rls/rls-group-settings.png)

[!INCLUDE [include-short-name](../includes/rls-limitations.md)]

[!INCLUDE [include-short-name](../includes/rls-faq.md)]

## <a name="next-steps"></a><span data-ttu-id="42376-159">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="42376-159">Next steps</span></span>

- [<span data-ttu-id="42376-160">จำกัดการเข้าถึงข้อมูลด้วยการรักษาความปลอดภัยระดับแถว (RLS) สำหรับ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="42376-160">Restrict data access with row-level security (RLS) for Power BI Desktop</span></span>](../create-reports/desktop-rls.md)
- [<span data-ttu-id="42376-161">คำแนะนำการรักษาความปลอดภัยระดับแถว (RLS) ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="42376-161">Row-level security (RLS) guidance in Power BI Desktop</span></span>](../guidance/rls-guidance.md)
- <span data-ttu-id="42376-162">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="42376-162">Questions?</span></span> [<span data-ttu-id="42376-163">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="42376-163">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="42376-164">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="42376-164">Suggestions?</span></span> [<span data-ttu-id="42376-165">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="42376-165">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com/)
