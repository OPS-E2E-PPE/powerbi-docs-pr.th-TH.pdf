---
title: การแสดงผลด้วยภาพขององค์กร
description: บทความนี้อธิบายการแสดงผลด้วยภาพขององค์กรผู้ดูแลระบบ
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 08/11/2020
ms.openlocfilehash: c5b14cb4e979bcd0e69617e6ecf5949856dc9693
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96409527"
---
# <a name="manage-power-bi-visuals-admin-settings"></a><span data-ttu-id="a7df3-103">จัดการการตั้งค่าผู้ดูแลระบบวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="a7df3-103">Manage Power BI visuals admin settings</span></span>

<span data-ttu-id="a7df3-104">ในฐานะผู้ดูแลระบบ Power BI สำหรับองค์กรของคุณคุณสามารถควบคุมชนิดของวิชวล Power BI ที่ผู้ใช้สามารถเข้าถึงได้ทั่วทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="a7df3-104">As a Power BI admin for your organization, you can control which type of Power BI visuals users can access across the organization.</span></span>

<span data-ttu-id="a7df3-105">ในการจัดการวิชวล Power BI คุณต้องเป็นผู้ดูแลระบบส่วนกลางใน Office 365 หรือได้รับมอบหมายบทบาทผู้ดูแลระบบบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="a7df3-105">To manage Power BI visuals, you must be a Global Admin in Office 365, or have been assigned the Power BI service administrator role.</span></span> <span data-ttu-id="a7df3-106">โปรดดูที่[การทำความเข้าใจเกี่ยวกับบทบาทผู้ดูแลระบบ Power BI](service-admin-role.md)เพื่อศึกษาข้อมูลเพิ่มเติมเกี่ยวกับบทบาทผู้ดูแลระบบบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="a7df3-106">For more information about the Power BI service administrator role, see [Understanding the Power BI admin role](service-admin-role.md).</span></span>

## <a name="access-the-admin-portal"></a><span data-ttu-id="a7df3-107">เข้าถึงพอร์ทัลผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="a7df3-107">Access the admin portal</span></span>

<span data-ttu-id="a7df3-108">เมื่อต้องการเปิดใช้งานการตั้งค่าที่อธิบายไว้ในบทความคุณจะต้องเข้าถึงพอร์ทัลผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="a7df3-108">To enable the settings described in the article, you'll need to access the admin portal.</span></span>

1. <span data-ttu-id="a7df3-109">ในบริการของ Power BI เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="a7df3-109">In Power BI service, select **Settings**.</span></span>

2. <span data-ttu-id="a7df3-110">จากเมนูดรอปดาวน์การตั้งค่าเลือก **พอร์ทัลผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="a7df3-110">From the settings drop-down menu, select **Admin portal**.</span></span>

    ![แบบฟอร์มวิชวล Power BI](media/organizational-visuals/admin-portal.png)

## <a name="power-bi-visuals-tenant-settings"></a><span data-ttu-id="a7df3-112">การตั้งค่าผู้เช่าวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="a7df3-112">Power BI visuals tenant settings</span></span>

<span data-ttu-id="a7df3-113">ในฐานะผู้ดูแลระบบ Power BI สำหรับองค์กรของคุณคุณสามารถควบคุมชนิดของวิชวล Power BI ที่ผู้ใช้สามารถเข้าถึงได้ทั่วทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="a7df3-113">As a Power BI admin for your organization, you can control which type of Power BI visuals users will be able to access across the organization.</span></span>

<span data-ttu-id="a7df3-114">การตั้งค่าผู้เช่า UI มีผลต่อบริการของ Power BI เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a7df3-114">The UI tenant settings only affect Power BI service.</span></span> <span data-ttu-id="a7df3-115">ถ้าคุณต้องการให้การตั้งค่าเหล่านี้มีผลใน Power BI Desktop ให้ใช้นโยบายกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="a7df3-115">If you want these settings to take effect in Power BI Desktop, use group policies.</span></span> <span data-ttu-id="a7df3-116">ตารางในตอนท้ายของแต่ละส่วนจะแสดงรายละเอียดสำหรับการเปิดใช้งานการตั้งค่าใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a7df3-116">A table at the end of each section provides details for enabling the setting in Power BI Desktop.</span></span>

>[!NOTE]
><span data-ttu-id="a7df3-117">การเปลี่ยนแปลงการตั้งค่าผู้เช่าไม่มีผลกับวิชวล Power BI ที่แสดงอยู่ในแท็บ [วิชวลขององค์กร](#organizational-visuals)</span><span class="sxs-lookup"><span data-stu-id="a7df3-117">Changes to tenant settings do not affect Power BI visuals listed in the [organizational visuals](#organizational-visuals) tab.</span></span>

### <a name="visuals-from-appsource-or-a-file"></a><span data-ttu-id="a7df3-118">วิชวลจาก AppSource หรือจากไฟล์</span><span class="sxs-lookup"><span data-stu-id="a7df3-118">Visuals from AppSource or a file</span></span>

<span data-ttu-id="a7df3-119">จัดการการเข้าถึงองค์กรสำหรับวิชวล Power BI ประเภทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a7df3-119">Manage organizational access for the following type of Power BI visuals:</span></span>

* <span data-ttu-id="a7df3-120">วิชวลที่สร้างขึ้นโดยนักพัฒนาและบันทึกเป็นไฟล์ .pbiviz</span><span class="sxs-lookup"><span data-stu-id="a7df3-120">Visuals created by developers and saved as a .pbiviz file.</span></span>

* <span data-ttu-id="a7df3-121">วิชวลที่พร้อมใช้งานจาก AppSource</span><span class="sxs-lookup"><span data-stu-id="a7df3-121">Visuals available from AppSource.</span></span>

<span data-ttu-id="a7df3-122">ทำตามคำแนะนำด้านล่างเพื่อเปิดใช้งานผู้ใช้ในองค์กรของคุณให้สามารถอัปโหลดไฟล์ .pbiviz และเพิ่มภาพจาก AppSource ไปยังรายงานและแดชบอร์ดของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="a7df3-122">Follow the instructions below to enable users in your organization upload .pbiviz files, and add visuals from AppSource to their reports and dashboards.</span></span>

1. <span data-ttu-id="a7df3-123">ขยายการตั้งค่าส่วน **การอนุญาตให้สร้างวิชวลโดยใช้ Power BI SDK**</span><span class="sxs-lookup"><span data-stu-id="a7df3-123">Expand the **Allow visuals created using the Power BI SDK** settings.</span></span>

2. <span data-ttu-id="a7df3-124">คลิก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="a7df3-124">Click **Enabled**.</span></span>

3. <span data-ttu-id="a7df3-125">เลือกว่าใครสามารถอัปโหลด .pbiviz และ AppSource ได้:</span><span class="sxs-lookup"><span data-stu-id="a7df3-125">Choose who can upload .pbiviz and AppSource visuals:</span></span>

    * <span data-ttu-id="a7df3-126">เลือกตัวเลือก **ทั้งองค์กร** เพื่ออนุญาตให้ทุกคนในองค์กรของคุณอัปโหลดไฟล์ .pbiviz และเพิ่มวิชวลจาก AppSource</span><span class="sxs-lookup"><span data-stu-id="a7df3-126">Select **The entire organization** option to allow everyone in your organization to upload .pbiviz files, and add visuals from AppSource.</span></span>

     * <span data-ttu-id="a7df3-127">เลือกตัวเลือก **เฉพาะกลุ่มความปลอดภัย** เพื่อจัดการการอัปโหลดไฟล์ .pbiviz และการเพิ่มวิชวลจาก AppSource โดยใช้กลุ่มความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="a7df3-127">Select the **Specific security groups** option to manage uploading .pbiviz files, and adding visuals from AppSource using security groups.</span></span> <span data-ttu-id="a7df3-128">เพิ่มกลุ่มความปลอดภัยที่คุณต้องการจัดการไปยังแถบข้อความ *ใส่กลุ่มความปลอดภัย*</span><span class="sxs-lookup"><span data-stu-id="a7df3-128">Add the security groups you want to manage to the *Enter security groups* text bar.</span></span> <span data-ttu-id="a7df3-129">กลุ่มความปลอดภัยที่คุณระบุจะถูกแยกออกตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a7df3-129">The security groups you specified are excluded by default.</span></span> <span data-ttu-id="a7df3-130">ถ้าคุณต้องการรวมกลุ่มความปลอดภัยเหล่านี้และแยกบุคคลอื่นในองค์กรออกให้เลือกตัวเลือก **ยกเว้นกลุ่มความปลอดภัยที่เฉพาะเจาะจง**</span><span class="sxs-lookup"><span data-stu-id="a7df3-130">If you want to include these security groups and exclude everyone else in the organization, select the **Except specific security groups** option.</span></span>

4. <span data-ttu-id="a7df3-131">คลิก **ใช้**</span><span class="sxs-lookup"><span data-stu-id="a7df3-131">Click **Apply**.</span></span>

![วิชวลจากไฟล์หรือ AppSource](media/organizational-visuals/tenant-settings.png)

<span data-ttu-id="a7df3-133">การเปลี่ยนแปลง UI ไปยังการตั้งค่าผู้เช่าใช้เฉพาะกับบริการของ Power BI เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a7df3-133">UI changes to tenant settings apply only to Power BI service.</span></span> <span data-ttu-id="a7df3-134">เมื่อต้องการเปิดใช้งานผู้ใช้ในองค์กรในการอัปโหลดไฟล์ .pbiviz และเพิ่มวิชวลจาก AppSource ไปยังบานหน้าต่างการแสดงภาพของพวกเขาใน Power BI Desktop ให้ใช้ [Azure AD นโยบายกลุ่ม](/azure/active-directory-domain-services/manage-group-policy)</span><span class="sxs-lookup"><span data-stu-id="a7df3-134">To enable users in your organization upload .pbiviz files, and add visuals from AppSource to their visualization pane in  Power BI Desktop, use [Azure AD Group Policy](/azure/active-directory-domain-services/manage-group-policy).</span></span>

|<span data-ttu-id="a7df3-135">คีย์</span><span class="sxs-lookup"><span data-stu-id="a7df3-135">Key</span></span>  |<span data-ttu-id="a7df3-136">ชื่อค่า</span><span class="sxs-lookup"><span data-stu-id="a7df3-136">Value name</span></span>  |<span data-ttu-id="a7df3-137">ค่า</span><span class="sxs-lookup"><span data-stu-id="a7df3-137">Value</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="a7df3-138">Software\Policies\Microsoft\Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a7df3-138">Software\Policies\Microsoft\Power BI Desktop</span></span>\    |<span data-ttu-id="a7df3-139">EnableCustomVisuals</span><span class="sxs-lookup"><span data-stu-id="a7df3-139">EnableCustomVisuals</span></span>    |<span data-ttu-id="a7df3-140">0 - ปิดการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a7df3-140">0 - Disable</span></span> </br><span data-ttu-id="a7df3-141">1 - เปิดใช้งาน (ค่าเริ่มต้น)</span><span class="sxs-lookup"><span data-stu-id="a7df3-141">1 - Enable (default)</span></span>         |
|

### <a name="certified-power-bi-visuals"></a><span data-ttu-id="a7df3-142">ส่วนจัดแสดง Power BI ที่ผ่านการรับรอง</span><span class="sxs-lookup"><span data-stu-id="a7df3-142">Certified Power BI visuals</span></span>

<span data-ttu-id="a7df3-143">เมื่อเปิดใช้งานการตั้งค่านี้เฉพาะ [วิชวล Power BI ที่ผ่านการรับรอง](../developer/visuals/power-bi-custom-visuals-certified.md) เท่านั้นที่จะแสดงในรายงานและแดชบอร์ดขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="a7df3-143">When this setting is enabled, only [certified Power BI visuals](../developer/visuals/power-bi-custom-visuals-certified.md) will render in your organization's reports and dashboards.</span></span> <span data-ttu-id="a7df3-144">วิชวล Power BI จาก AppSource หรือไฟล์ที่ไม่ผ่านการรับรองจะส่งกลับข้อความข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="a7df3-144">Power BI visuals from AppSource or files, that are not certified, will return an error message.</span></span>

1. <span data-ttu-id="a7df3-145">จากพอร์ทัลผู้ดูแลระบบให้เลือก **เพิ่มและใช้วิชวลที่ผ่านการรับรองเท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="a7df3-145">From the admin portal, select **Add and use certified visuals only**.</span></span>

2. <span data-ttu-id="a7df3-146">คลิก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="a7df3-146">Click **Enabled**.</span></span>

3. <span data-ttu-id="a7df3-147">คลิก **ใช้**</span><span class="sxs-lookup"><span data-stu-id="a7df3-147">Click **Apply**.</span></span>

![วิชวลที่ผ่านการรับรองแล้ว](media/organizational-visuals/certified-visuals.png)

<span data-ttu-id="a7df3-149">การเปลี่ยนแปลง UI ไปยังการตั้งค่าผู้เช่าใช้เฉพาะกับบริการของ Power BI เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a7df3-149">UI changes to tenant settings apply only to Power BI service.</span></span> <span data-ttu-id="a7df3-150">หากต้องการจัดการการตั้งค่าผู้เช่าวิชวลที่่ผ่านการรับรองใน Power BI Desktop ให้ใช้ [นโยบายกลุ่ม Azure AD](/azure/active-directory-domain-services/manage-group-policy)</span><span class="sxs-lookup"><span data-stu-id="a7df3-150">To manage the certified visuals tenant setting in Power BI Desktop, use [Azure AD Group Policy](/azure/active-directory-domain-services/manage-group-policy).</span></span>

|<span data-ttu-id="a7df3-151">คีย์</span><span class="sxs-lookup"><span data-stu-id="a7df3-151">Key</span></span>  |<span data-ttu-id="a7df3-152">ชื่อค่า</span><span class="sxs-lookup"><span data-stu-id="a7df3-152">Value name</span></span>  |<span data-ttu-id="a7df3-153">ค่า</span><span class="sxs-lookup"><span data-stu-id="a7df3-153">Value</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="a7df3-154">Software\Policies\Microsoft\Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a7df3-154">Software\Policies\Microsoft\Power BI Desktop</span></span>\    |<span data-ttu-id="a7df3-155">EnableUncertifiedVisuals</span><span class="sxs-lookup"><span data-stu-id="a7df3-155">EnableUncertifiedVisuals</span></span>    |<span data-ttu-id="a7df3-156">0 - ปิดการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a7df3-156">0 - Disable</span></span> </br><span data-ttu-id="a7df3-157">1 - เปิดใช้งาน (ค่าเริ่มต้น)</span><span class="sxs-lookup"><span data-stu-id="a7df3-157">1 - Enable (default)</span></span>         |
|

## <a name="organizational-visuals"></a><span data-ttu-id="a7df3-158">การแสดงผลด้วยภาพขององค์กร</span><span class="sxs-lookup"><span data-stu-id="a7df3-158">Organizational visuals</span></span>

<span data-ttu-id="a7df3-159">ในฐานะผู้ดูแลระบบ Power BI คุณสามารถจัดการรายการของวิชวล Power BI ที่พร้อมใช้งานขององค์กรใน [ที่จัดเก็บขององค์กรของคุณ](../developer/visuals/power-bi-custom-visuals.md#organizational-store)</span><span class="sxs-lookup"><span data-stu-id="a7df3-159">As a Power BI admin, you can manage the list of Power BI visuals available in your organization's [organizational store](../developer/visuals/power-bi-custom-visuals.md#organizational-store).</span></span> <span data-ttu-id="a7df3-160">แท็บ **วิชวลขององค์กร** ใน *พอร์ทัลของผู้ดูแลระบบ* จะช่วยให้คุณเพิ่มและเอาวิชวลออก และตัดสินใจว่าจะแสดงวิชวลใดในบานหน้าต่างการแสดงภาพของผู้ใช้ในองค์กรโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a7df3-160">The **Organizational visuals** tab in the *Admin portal*, allows you to add and remove visuals, and decide which visuals will automatically display in the visualization pane of your organization's users.</span></span> <span data-ttu-id="a7df3-161">คุณสามารถเพิ่มรายการแสดงผลด้วยวิชวลชนิดใดก็ได้รวมถึงวิชวลที่ไม่ได้ผ่านการรับรองและวิชวล .pbiviz แม้ว่าพวกนี้จะขัดแย้งกับ [การตั้งค่าผู้เช่า](#power-bi-visuals-tenant-settings) ขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="a7df3-161">You can add to the list any type of visual including uncertified visuals and .pbiviz visuals, even if they contradict the [tenant settings](#power-bi-visuals-tenant-settings) of your organization.</span></span>

<span data-ttu-id="a7df3-162">การตั้งค่าวิชวลองค์กรจะถูกปรับใช้เป็น Power BI Desktop โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a7df3-162">Organizational visuals settings are automatically deployed to Power BI Desktop.</span></span>

>[!NOTE]
><span data-ttu-id="a7df3-163">วิชวลขององค์กรไม่ได้รับการสนับสนุนในเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="a7df3-163">Organizational visuals are not supported in Power BI Report Server.</span></span>

### <a name="add-a-visual-from-a-file"></a><span data-ttu-id="a7df3-164">นำเข้าวิชวลจากไฟล์</span><span class="sxs-lookup"><span data-stu-id="a7df3-164">Add a visual from a file</span></span>

<span data-ttu-id="a7df3-165">ใช้วิธีนี้เพื่อเพิ่มวิชวล Power BI ใหม่จากไฟล์ .pbiviz</span><span class="sxs-lookup"><span data-stu-id="a7df3-165">Use this method to add a new Power BI visual from a .pbiviz file.</span></span>

> [!WARNING]
> <span data-ttu-id="a7df3-166">วิชวล Power BI ที่อัปโหลดมาจากไฟล์อาจประกอบด้วยโค้ดที่มีความเสี่ยงด้านความปลอดภัยหรือความเป็นส่วนตัว ตรวจสอบให้แน่ใจว่าคุณเชื่อถือผู้เขียนและแหล่งที่มาของวิชวล ก่อนที่จะปรับใช้กับที่เก็บข้อมูลขององค์กร</span><span class="sxs-lookup"><span data-stu-id="a7df3-166">A Power BI visual uploaded from a file, could contain code with security or privacy risks; make sure you trust the author and the source of the visual, before deploying to the organization's repository.</span></span>

1. <span data-ttu-id="a7df3-167">เลือก **เพิ่มวิชวล** > **จากไฟล์**</span><span class="sxs-lookup"><span data-stu-id="a7df3-167">Select **Add visual** > **From a file**.</span></span>

    ![เพิ่มวิชวลจากไฟล์](media/organizational-visuals/add-from-file.png)

2. <span data-ttu-id="a7df3-169">กรอกข้อมูลในเขตข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a7df3-169">Fill in the following fields:</span></span>

    * <span data-ttu-id="a7df3-170">**เลือกไฟล์ .pbiviz** - เลือกไฟล์วิชวลเพื่ออัปโหลด</span><span class="sxs-lookup"><span data-stu-id="a7df3-170">**Choose a .pbiviz file** - Select a visual file to upload.</span></span>

    * <span data-ttu-id="a7df3-171">**ตั้งชื่อวิชวลของคุณ** - กำหนดชื่อย่อให้กับวิชวลเพื่อให้ผู้เขียนรายงานสามารถเข้าใจได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="a7df3-171">**Name your visual** - Give a short title to the visual, so that report authors can easily understand what it does.</span></span>

    * <span data-ttu-id="a7df3-172">**ไอคอน** - อัปโหลดไฟล์ไอคอนที่จะแสดงในบานหน้าต่างการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="a7df3-172">**Icon** - Upload an icon file to be displayed in the visualization pane.</span></span>

    * <span data-ttu-id="a7df3-173">**คำอธิบาย** - กำหนดคำอธิบายสั้น ๆ ของวิชวลเพื่อให้บริบทแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="a7df3-173">**Description** - Provide a short description of the visual to give more context for the user.</span></span>

    * <span data-ttu-id="a7df3-174">**Access** - ส่วนนี้มีสองตัวเลือก:</span><span class="sxs-lookup"><span data-stu-id="a7df3-174">**Access** - This section has two options:</span></span>
    
        * <span data-ttu-id="a7df3-175">เลือกว่าผู้ใช้ในองค์กรของคุณสามารถเข้าถึงวิชวลนี้ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a7df3-175">Select whether users in your organization can access this visual.</span></span> <span data-ttu-id="a7df3-176">การตั้งค่านี้จะเปิดใช้งานตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a7df3-176">This setting is enabled by default.</span></span>

        * <span data-ttu-id="a7df3-177">เลือกว่าวิชวลนี้จะปรากฏในบานหน้าต่างการแสดงภาพของผู้ใช้ในองค์กรของคุณหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a7df3-177">Select whether this visual will appear in the visualization pane of the users in your organization.</span></span> <span data-ttu-id="a7df3-178">การตั้งค่านี้จะถูกปิดการใช้งานตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a7df3-178">This setting is disabled by default.</span></span> <span data-ttu-id="a7df3-179">สำหรับข้อมูลเพิ่มเติมให้ดู [เพิ่มวิชวลลงในบานหน้าต่างการแสดงภาพ](#add-a-visual-to-the-visualization-pane).</span><span class="sxs-lookup"><span data-stu-id="a7df3-179">For more information, see [add a visual to the visualization pane](#add-a-visual-to-the-visualization-pane).</span></span>

    ![เพิ่มวิชวล](media/organizational-visuals/add-visual.png)

3. <span data-ttu-id="a7df3-181">เลือก **เพิ่ม** เพื่อเริ่มคำขอการอัปโหลด</span><span class="sxs-lookup"><span data-stu-id="a7df3-181">To initiate the upload request, select **Add** .</span></span> <span data-ttu-id="a7df3-182">เมื่ออัปโหลด วิชวลจะแสดงในรายการวิชวลองค์กร</span><span class="sxs-lookup"><span data-stu-id="a7df3-182">Once uploaded, the visual will display in the organizational visuals list.</span></span>

### <a name="add-a-visual-from-appsource"></a><span data-ttu-id="a7df3-183">เพิ่มวิชวลจาก AppSource</span><span class="sxs-lookup"><span data-stu-id="a7df3-183">Add a visual from AppSource</span></span>

<span data-ttu-id="a7df3-184">ใช้วิธีนี้เพื่อเพิ่มวิชวล Power BI ใหม่จาก AppSource</span><span class="sxs-lookup"><span data-stu-id="a7df3-184">Use this method to add a new Power BI visual from AppSource.</span></span>

<span data-ttu-id="a7df3-185">วิชวล Power BI ของ AppSource จะได้รับการอัปเดตโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a7df3-185">AppSource Power BI visuals are automatically updated.</span></span> <span data-ttu-id="a7df3-186">ผู้ใช้ในองค์กรของคุณจะมีวิชวลเวอร์ชันล่าสุดเสมอ</span><span class="sxs-lookup"><span data-stu-id="a7df3-186">Users in your organization will always have the latest version of the visual.</span></span>

1. <span data-ttu-id="a7df3-187">เลือก **เพิ่มวิชวล** > **จาก AppSource**</span><span class="sxs-lookup"><span data-stu-id="a7df3-187">Select **Add visual** > **From AppSource**.</span></span>

    ![เพิ่มวิชวลจาก AppSource](media/organizational-visuals/add-visual-from-appsource.png)

2. <span data-ttu-id="a7df3-189">ในหน้าต่าง **Power BI** ให้ค้นหาวิชวลของ AppSource ที่คุณต้องการเพิ่มแล้วคลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="a7df3-189">In the **Power BI visuals** window, find the AppSource visual you want to add, and click **Add**.</span></span> <span data-ttu-id="a7df3-190">เมื่ออัปโหลด วิชวลจะแสดงในรายการวิชวลองค์กร</span><span class="sxs-lookup"><span data-stu-id="a7df3-190">Once uploaded, the visual will display in the organizational visuals list.</span></span>

### <a name="add-a-visual-to-the-visualization-pane"></a><span data-ttu-id="a7df3-191">เพิ่มวิชวลไปยังบานหน้าต่างการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="a7df3-191">Add a visual to the visualization pane</span></span>

<span data-ttu-id="a7df3-192">คุณสามารถเลือกวิชวลจากหน้าวิชวลองค์กรเพื่อแสดงในบานหน้าต่างการแสดงภาพของผู้ใช้ทั้งหมดในองค์กรของคุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a7df3-192">You can pick visuals from the organizational visuals page to automatically show on the visualization pane of all the users in your organization.</span></span>

1. <span data-ttu-id="a7df3-193">ในแถวของวิชวลที่คุณต้องการเพิ่มให้คลิก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="a7df3-193">In the row of the visual you want to add , click **settings**.</span></span>

    ![สกรีนช็อตแสดงพอร์ทัลผู้ดูแลระบบที่มีวิชวลองค์กรที่เลือก และไอคอนการตั้งค่าที่แสดง](media/organizational-visuals/organizational-pane.png)<span data-ttu-id="a7df3-195">บานหน้าต่าง - องค์กร</span><span class="sxs-lookup"><span data-stu-id="a7df3-195">organizational-pane</span></span>

2. <span data-ttu-id="a7df3-196">เปิดใช้งานการตั้งค่าบานหน้าต่างการแสดงภาพแล้วคลิก **อัปเดต**</span><span class="sxs-lookup"><span data-stu-id="a7df3-196">Enable the visualization pane setting and click **Update**.</span></span>

    ![สกรีนช็อตแสดงกล่องโต้ตอบ การตั้งค่าวิชวล ซึ่งคุณสามารถเปิดใช้งานวิชวลให้ปรากฏแบบทั่วทั้งองค์กร](media/organizational-visuals/update-organizational-pane.png)

### <a name="delete-a-visual-uploaded-from-a-file"></a><span data-ttu-id="a7df3-198">ลบวิชวลที่อัปโหลดจากไฟล์</span><span class="sxs-lookup"><span data-stu-id="a7df3-198">Delete a visual uploaded from a file</span></span>

<span data-ttu-id="a7df3-199">หากต้องการลบวิชวลโดยถาวร ให้เลือกไอคอนถังขยะสำหรับวิชวลในที่เก็บข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a7df3-199">To permanently delete a visual, select the trash bin icon for the visual in the repository.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7df3-200">การลบจะไม่สามารถแก้ไขย้อนกลับได้</span><span class="sxs-lookup"><span data-stu-id="a7df3-200">Deletion is irreversible.</span></span> <span data-ttu-id="a7df3-201">เมื่อถูกลบ ภาพจะหยุดแสดงผลในรายงานที่มีอยู่ทันที</span><span class="sxs-lookup"><span data-stu-id="a7df3-201">Once deleted, the visual immediately stops rendering in existing reports.</span></span> <span data-ttu-id="a7df3-202">แม้ว่าคุณจะอัปโหลดวิชวลเดิมอีกครั้ง ก็จะไม่สามารถแทนที่วิชวลก่อนหน้านี้ที่ถูกลบได้</span><span class="sxs-lookup"><span data-stu-id="a7df3-202">Even if you upload the same visual again, it won't replace the one that was deleted.</span></span> <span data-ttu-id="a7df3-203">อย่างไรก็ตาม ผู้ใช้สามารถนำเข้าวิชวลใหม่อีกครั้ง และแทนที่อินสแตนซ์ที่มีในรายงาน</span><span class="sxs-lookup"><span data-stu-id="a7df3-203">However, users can import the new visual again and replace the instance they have in their reports.</span></span>

### <a name="disable-a-pbiviz-visual"></a><span data-ttu-id="a7df3-204">ปิดการใช้งานวิชวล .pbiviz</span><span class="sxs-lookup"><span data-stu-id="a7df3-204">Disable a .pbiviz visual</span></span>

<span data-ttu-id="a7df3-205">คุณสามารถปิดการใช้งานวิชวล .pbiviz จากที่มีอยู่โดยผ่าน [ที่จัดเก็บขององค์กร](../developer/visuals/power-bi-custom-visuals.md#organizational-store) ในขณะที่ทำการเก็บไว้ในรายการวิชวลองค์กร</span><span class="sxs-lookup"><span data-stu-id="a7df3-205">You can disable a .pbiviz visual from being available trough the [organizational store](../developer/visuals/power-bi-custom-visuals.md#organizational-store), while keeping it on the organizational visuals list.</span></span>

1. <span data-ttu-id="a7df3-206">ในแถวของวิชวล .pbiviz ที่คุณต้องการปิดการใช้งานให้คลิก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="a7df3-206">In the row of the .pbiviz visual you want to disable , click **settings**.</span></span>

2. <span data-ttu-id="a7df3-207">ในส่วน **เข้าถึง** ปิดการใช้งานการตั้งค่า: *ผู้ใช้ในองค์กรสามารถเข้าถึง ดู แชร์ และโต้ตอบกับวิชวลนี้ได้*</span><span class="sxs-lookup"><span data-stu-id="a7df3-207">In the **Access** section, disable the setting: *Users in the organization can access, view, share, and interact with this visual*.</span></span>

<span data-ttu-id="a7df3-208">หลังจากที่คุณปิดการใช้งานวิชวล .pbiviz ภาพจะไม่แสดงในรายงานที่มีอยู่ และจะแสดงข้อผิดพลาดดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a7df3-208">After you disable the .pbiviz visual, the visual won't render in existing reports, and it displays the following error message:</span></span>

<span data-ttu-id="a7df3-209">*ภาพแบบกำหนดเองนี้จะไม่พร้อมใช้งานอีกต่อไป โปรดติดต่อผู้ดูแลระบบของคุณสำหรับรายละเอียด*</span><span class="sxs-lookup"><span data-stu-id="a7df3-209">*This custom visual is no longer available. Please contact your administrator for details.*</span></span>

>[!NOTE]
><span data-ttu-id="a7df3-210">วิชวล .pbiviz ที่มีการคั่นหน้าดำเนินการทำงานหลังจากที่ปิดการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a7df3-210">.pbiviz visuals that are bookmarked carry on working after they've been disabled.</span></span>

### <a name="update-a-visual"></a><span data-ttu-id="a7df3-211">อัปเดตวิชวล</span><span class="sxs-lookup"><span data-stu-id="a7df3-211">Update a visual</span></span>

<span data-ttu-id="a7df3-212">วิชวลของ AppSource ได้รับการอัปเดตโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a7df3-212">AppSource visuals are updated automatically.</span></span> <span data-ttu-id="a7df3-213">เมื่อเวอร์ชันใหม่พร้อมใช้งานจาก AppSource จะแทนที่การปรับใช้รุ่นเก่ากว่าผ่านรายการวิชวลองค์กร</span><span class="sxs-lookup"><span data-stu-id="a7df3-213">Once a new version is available from AppSource, it will replace an older version deployed via the organizational visuals list.</span></span>

<span data-ttu-id="a7df3-214">หากต้องการอัปเดตวิชวล .pbiviz ให้ทำตามขั้นตอนเหล่านี้เพื่อแทนที่วิชวล</span><span class="sxs-lookup"><span data-stu-id="a7df3-214">To update a .pbiviz visual, follow these steps to replace the visual.</span></span>

1. <span data-ttu-id="a7df3-215">ในแถวของวิชวลที่คุณต้องการเพิ่มให้คลิก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="a7df3-215">In the row of the visual you want to add , click **settings**.</span></span>

2. <span data-ttu-id="a7df3-216">คลิก **เรียกดู** และเลือก .pbiviz ที่คุณต้องการแทนที่วิชวลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="a7df3-216">Click **Browse**, and select the .pbiviz you want to replace the current visual with.</span></span>

3. <span data-ttu-id="a7df3-217">คลิก **อัปเดต**</span><span class="sxs-lookup"><span data-stu-id="a7df3-217">Click **Update**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a7df3-218">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a7df3-218">Next steps</span></span>

> [!div class="nextstepaction"]
>[<span data-ttu-id="a7df3-219">การดูแล Power BI ในพอร์ทัลผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="a7df3-219">Administering Power BI in the admin portal</span></span>](service-admin-portal.md)

> [!div class="nextstepaction"]
>[<span data-ttu-id="a7df3-220">วิชวลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="a7df3-220">Visuals in Power BI</span></span>](../developer/visuals/power-bi-custom-visuals.md)

> [!div class="nextstepaction"]
>[<span data-ttu-id="a7df3-221">วิชวลองค์กรใน Power BI</span><span class="sxs-lookup"><span data-stu-id="a7df3-221">Organizational visuals in Power BI</span></span>](../developer/visuals/power-bi-custom-visuals-organization.md)