---
title: คำแนะนำเกี่ยวกับการตั้งค่าของผู้เช่า
description: คำแนะนำสำหรับการตั้งค่าของผู้เช่า Power BI
author: paulinbar
ms.author: painbar
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 08/10/2020
ms.openlocfilehash: 39357ec461ae96ef566719739aa76a61c7e7c539
ms.sourcegitcommit: a5e98bc86915f7bea6a0ab5df282683840e63d2c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/07/2021
ms.locfileid: "97969799"
---
# <a name="tenant-settings-guidance"></a><span data-ttu-id="f9e88-103">คำแนะนำเกี่ยวกับการตั้งค่าของผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="f9e88-103">Tenant settings guidance</span></span>

<span data-ttu-id="f9e88-104">บทความนี้มีผู้อ่านเป้าหมายเป็นผู้ดูแลระบบของ Power BI ที่มีหน้าที่รับผิดชอบเกี่ยวกับการตั้งค่าและการกำหนดค่าสภาพแวดล้อมของ Power BI ในองค์กรของตนเอง</span><span class="sxs-lookup"><span data-stu-id="f9e88-104">This article targets Power BI administrators who are responsible for setting up and configuring the Power BI environment in their organization.</span></span>

<span data-ttu-id="f9e88-105">เราให้คำแนะนำสำหรับการตั้งค่าเฉพาะของผู้เช่า ซึ่งจะช่วยปรับปรุงประสบการณ์ใช้งานเกี่ยวกับ Power BI ให้ดียิ่งขึ้ หรืออาจทำให้องค์กรของคุณตกอยู่ในความเสี่ยงได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="f9e88-105">We provide guidance for specific tenant settings that help improve the Power BI experience, or could expose your organization to risk.</span></span> <span data-ttu-id="f9e88-106">เราขอแนะนำให้คุณกำหนดค่าผู้เช่าของคุณให้ตรงกับนโยบายและกระบวนการขององค์กรของคุณเสมอ</span><span class="sxs-lookup"><span data-stu-id="f9e88-106">We recommend you always configure your tenant to align with your organization's policies and processes.</span></span>

<span data-ttu-id="f9e88-107">[การตั้งค่าผู้เช่า](../admin/service-admin-portal.md#tenant-settings) สามารถจัดการได้ใน [พอร์ทัลผู้ดูแลระบบ](https://app.powerbi.com/admin-portal/tenantSettings) และสามารถกำหนดค่าโดย [ผู้ดูแลระบบบริการ Power BI](../admin/service-admin-administering-power-bi-in-your-organization.md#administrator-roles-related-to-power-bi)</span><span class="sxs-lookup"><span data-stu-id="f9e88-107">[Tenant settings](../admin/service-admin-portal.md#tenant-settings) are managed in the [Admin portal](https://app.powerbi.com/admin-portal/tenantSettings), and can be configured by a [Power BI service administrator](../admin/service-admin-administering-power-bi-in-your-organization.md#administrator-roles-related-to-power-bi).</span></span> <span data-ttu-id="f9e88-108">การตั้งค่าผู้เช่าจำนวนมากอาจจำกัดความสามารถและคุณลักษณะต่า ๆ สำหรับชุดผู้ใช้ที่จำกัด</span><span class="sxs-lookup"><span data-stu-id="f9e88-108">Many tenant settings can restrict capabilities and features to a limited set of users.</span></span> <span data-ttu-id="f9e88-109">ดังนั้น เราขอแนะนำให้คุณทำความคุ้นเคยกับการตั้งค่าต่าง ๆ ก่อน เพื่อวางแผนกลุ่มความปลอดภัยที่คุณจะต้องใช้</span><span class="sxs-lookup"><span data-stu-id="f9e88-109">So, we recommend you first become familiar with the settings to plan the security groups you'll need.</span></span> <span data-ttu-id="f9e88-110">คุณอาจพบว่า คุณสามารถปรับใช้กลุ่มความปลอดภัยเดียวกันกับการตั้งค่าหลายอย่าง</span><span class="sxs-lookup"><span data-stu-id="f9e88-110">You might find that you can apply the same security group to multiple settings.</span></span>

## <a name="improve-power-bi-experience"></a><span data-ttu-id="f9e88-111">ปรับปรุงประสบการณ์ใช้งาน Power BI ให้ดียิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="f9e88-111">Improve Power BI experience</span></span>

### <a name="publish-get-help-information"></a><span data-ttu-id="f9e88-112">เผยแพร่ข้อมูล "รับความช่วยเหลือ"</span><span class="sxs-lookup"><span data-stu-id="f9e88-112">Publish "Get Help" information</span></span>

<span data-ttu-id="f9e88-113">เราสนับสนุนให้คุณตั้งค่าไซต์ที่เกี่ยวข้องกับ Power BI ภายใน โดยใช้ [Microsoft Teams](/microsoftteams) หรือแพลตฟอร์มอื่น ๆ ที่ทำงานร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="f9e88-113">We encourage you to set up internal Power BI-related sites using [Microsoft Teams](/microsoftteams), or other collaboration platform.</span></span> <span data-ttu-id="f9e88-114">ไซต์เหล่านี้อาจใช้สำหรับจัดเก็บเอกสารการฝึกอบรม เป็นพื้นที่ในการอภิปราย ส่งคำขอรับใบอนุญาต หรือตอบสนองเพื่อให้ความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="f9e88-114">These sites can be used to store training documentation, host discussions, make requests for licenses, or respond to help.</span></span>

<span data-ttu-id="f9e88-115">หากคุณดำเนินการดังกล่าวด้วย เราขอแนะนำให้คุณเปิดใช้งานการตั้งค่า **เผยแพร่ข้อมูล "รับความช่วยเหลือ"** _สำหรับทั้งองค์กร_</span><span class="sxs-lookup"><span data-stu-id="f9e88-115">If you do so, we recommend you then enable the **Publish "Get Help" information** setting _for the entire organization_.</span></span> <span data-ttu-id="f9e88-116">โดยเข้าไปได้ในกลุ่ม **การตั้งค่าความช่วยเหลือและการสนับสนุน**</span><span class="sxs-lookup"><span data-stu-id="f9e88-116">It's found in the **Help and support settings** group.</span></span> <span data-ttu-id="f9e88-117">คุณสามารถตั้งค่า URL สำหรับ:</span><span class="sxs-lookup"><span data-stu-id="f9e88-117">You can set URLs for your:</span></span>

- <span data-ttu-id="f9e88-118">เอกสารการฝึกอบรม</span><span class="sxs-lookup"><span data-stu-id="f9e88-118">Training documentation</span></span>
- <span data-ttu-id="f9e88-119">ฟอรัมการอภิปราย</span><span class="sxs-lookup"><span data-stu-id="f9e88-119">Discussion forum</span></span>
- <span data-ttu-id="f9e88-120">คำขอสิทธิ์อนุญาตการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f9e88-120">Licensing requests</span></span>
- <span data-ttu-id="f9e88-121">บริการช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="f9e88-121">Help desk</span></span>

<span data-ttu-id="f9e88-122">URL เหล่านี้จะมีให้ใช้งานในรูปแบบลิงก์ในเมนูความช่วยเหลือของ Power BI</span><span class="sxs-lookup"><span data-stu-id="f9e88-122">These URLs will become available as links in the Power BI help menu.</span></span>

> [!NOTE]
> <span data-ttu-id="f9e88-123">การจัดหา URL **คำขอสิทธิ์การใช้งาน** จะป้องกันไม่ให้ผู้ใช้แต่ละรายซื้อใบอนุญาตให้ใช้งาน Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="f9e88-123">Supplying the **Licensing requests** URL prevents individual users from buying a Power BI Pro license.</span></span> <span data-ttu-id="f9e88-124">แต่จะนำไปยังเว็บไซต์ภายในของคุณพร้อมข้อมูลเกี่ยวกับวิธีการขอใบอนุญาตให้ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f9e88-124">Instead, they'll be directed to your internal site with information on how to acquire a license.</span></span> <span data-ttu-id="f9e88-125">การตั้งค่า **อนุญาตให้ผู้ใช้ลองใช้ Power BI Pro** ที่เปิดใช้งานโดยค่าเริ่มต้นและแยกประสบการณ์การซื้อและการใช้รุ่นทดลอง</span><span class="sxs-lookup"><span data-stu-id="f9e88-125">The setting **Allow users to try Power BI Pro** is enabled by default and separates the purchase and trial experiences.</span></span> <span data-ttu-id="f9e88-126">ในการเรียนรู้เพิ่มเติมเกี่ยวกับธีการทำงานร่วมกันของการตั้งค่าเหล่านี้ให้ดูที่ [อนุญาตให้ผู้ใช้ลองใช้ Power BI Pro](../admin/service-admin-portal.md#allow-users-to-try-power-bi-paid-features) ได้</span><span class="sxs-lookup"><span data-stu-id="f9e88-126">To learn more about how these settings work together, see [Allow users to try Power BI Pro](../admin/service-admin-portal.md#allow-users-to-try-power-bi-paid-features).</span></span>
>
>

![ภาพหน้าจอของ Power B I Desktop ที่แสดงความช่วยเหลือและการตั้งค่าการสนับสนุน](media/admin-tenant-settings/publish-get-help-information.png)

<span data-ttu-id="f9e88-128">สำหรับข้อมูลเพิ่มเติมให้ดู [การตั้งค่าความช่วยเหลือและการสนับสนุน](../admin/service-admin-portal.md#help-and-support-settings)</span><span class="sxs-lookup"><span data-stu-id="f9e88-128">For more information, see [Help and support settings](../admin/service-admin-portal.md#help-and-support-settings).</span></span>

## <a name="manage-risk"></a><span data-ttu-id="f9e88-129">จัดการความเสี่ยง</span><span class="sxs-lookup"><span data-stu-id="f9e88-129">Manage risk</span></span>
<span data-ttu-id="f9e88-130">การตั้งค่าเพื่อจัดการความเสี่ยงสามารถช่วยคุณในการสร้างนโยบายการกำกับดูแลในผู้เช่า Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f9e88-130">The settings to manage risks can help you establish governance policies in your Power BI tenant.</span></span> <span data-ttu-id="f9e88-131">อย่างไรก็ตาม โปรดทราบว่าการตั้งค่าการกำกับดูแลดังกล่าวไม่ใช่หน่วยวัดความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="f9e88-131">Keep in mind, however, that governance settings are not a security measure.</span></span> <span data-ttu-id="f9e88-132">ตัวอย่างเช่น การปิดใช้งานการตั้งค่า **การส่งออกข้อมูล** จะลบคุณลักษณะจากส่วนติดต่อผู้ใช้ Power BI และช่วยด้วยวิธีนี้ให้ผู้ใช้ Power BI สามารถปฏิบัติตามนโยบายการกำกับดูแลขององค์กรของคุณ แต่ไม่ได้ป้องกันผู้ใช้โดยจากการกำหนดไม่ให้ส่งออกข้อมูลโดยใช้ตัวเลือกอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="f9e88-132">For example, disabling the **Export data** setting removes the feature from the Power BI user interface and helps in this way Power BI users to work in compliance with your organization's governance policies, but it does not prevent determined users from exporting data using other options.</span></span> <span data-ttu-id="f9e88-133">จากมุมมองด้านความปลอดภัย ผู้ใช้ Power BI ที่มีการเข้าถึงชุดข้อมูลแบบอ่านมีสิทธิ์ในการคิวรีชุดข้อมูลนี้ และสามารถยืนยันผลลัพธ์ได้โดยไม่คำนึงถึงคุณลักษณะที่พร้อมใช้งานในอินเทอร์เฟซผู้ใช้ Power BI</span><span class="sxs-lookup"><span data-stu-id="f9e88-133">From a security viewpoint, a Power BI user with read access to a dataset has the permission to query this dataset and can persist the results regardless of the features available in the Power BI user interface.</span></span>
### <a name="receive-email-notification-service-outages-or-incidents"></a><span data-ttu-id="f9e88-134">รับการแจ้งเตือนทางอีเมลสำหรับการหยุดทำงานหรือเหตุขัดข้องของการบริการ</span><span class="sxs-lookup"><span data-stu-id="f9e88-134">Receive email notification service outages or incidents</span></span>

<span data-ttu-id="f9e88-135">คุณอาจได้รับการแจ้งเตือนทางอีเมล หากผู้เช่าของคุณได้รับผลกระทบจากการหยุดทำงานหรือเหตุขัดข้องของการบริการ</span><span class="sxs-lookup"><span data-stu-id="f9e88-135">You can be notified by email if your tenant is impacted by a service outage or incident.</span></span> <span data-ttu-id="f9e88-136">หากเป็นเช่นนี้ คุณอาจตอบสนองในเชิงรุกต่อเหตุขัดข้องดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="f9e88-136">This way, you can proactively respond to incidents.</span></span>

<span data-ttu-id="f9e88-137">เราขอแนะนำให้คุณเปิดใช้การตั้งค่า **รับการแจ้งเตือนทางอีเมลสำหรับการหยุดทำงานหรือเหตุขัดข้องของการบริการ**</span><span class="sxs-lookup"><span data-stu-id="f9e88-137">We recommend you enable the **Receive email notification service outages or incidents** setting.</span></span> <span data-ttu-id="f9e88-138">โดยเข้าไปได้ในกลุ่ม **การตั้งค่าความช่วยเหลือและการสนับสนุน**</span><span class="sxs-lookup"><span data-stu-id="f9e88-138">It's found in the **Help and support settings** group.</span></span> <span data-ttu-id="f9e88-139">กำหนดกลุ่มความปลอดภัยที่ _เปิดใช้งานเมล_ อย่างน้อยหนึ่งกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="f9e88-139">Assign one or more _mail-enabled_ security groups.</span></span>

![ภาพหน้าจอ Power B I Desktop ที่แสดงการตั้งค่า “รับการแจ้งเตือนอีเมลสำหรับการหยุดทำงานหรือเหตุขัดข้องของบริการ”](media/admin-tenant-settings/receive-email-notifications-for-service-outages-or-incidents.png)

### <a name="information-protection"></a><span data-ttu-id="f9e88-141">การปกป้องข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f9e88-141">Information protection</span></span>

<span data-ttu-id="f9e88-142">การปกป้องข้อมูล จะอนุญาตการเปิดใช้การตั้งค่าการป้องกันต่าง ๆ เช่น การเข้ารหัสหรือลายน้ำ ขณะทำการส่งออกข้อมูลจากบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="f9e88-142">Information protection allows enforcing protection settings—such as encryption or watermarks—when exporting data from the Power BI service.</span></span>

<span data-ttu-id="f9e88-143">โดยมีการตั้งค่าผู้เช่าสองแบบที่เกี่ยวข้องกับการปกป้องข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f9e88-143">There are two tenant settings related to information protection.</span></span> <span data-ttu-id="f9e88-144">ตามค่าเริ่มต้นแล้ว การตั้งค่าทั้งสองรายการจะปิดใช้งานสำหรับทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="f9e88-144">By default, both settings are disabled for the entire organization.</span></span>

<span data-ttu-id="f9e88-145">เราขอแนะนำให้คุณเปิดใช้การตั้งค่าดังกล่าวเมื่อคุณต้องการจัดการและปกป้องข้อมูลที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="f9e88-145">We recommend you enable these settings when you need to handle and protect sensitive data.</span></span> <span data-ttu-id="f9e88-146">สำหรับข้อมูลเพิ่มเติม โปรดดู [การปกป้องข้อมูลใน Power BI](../admin/service-security-data-protection-overview.md)</span><span class="sxs-lookup"><span data-stu-id="f9e88-146">For more information, see [Data protection in Power BI](../admin/service-security-data-protection-overview.md).</span></span>

### <a name="create-workspaces"></a><span data-ttu-id="f9e88-147">สร้างพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f9e88-147">Create workspaces</span></span>

<span data-ttu-id="f9e88-148">คุณสามารถจำกัดผู้ใช้ไม่ให้สร้างพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f9e88-148">You can restrict users from creating workspaces.</span></span> <span data-ttu-id="f9e88-149">ด้วยวิธีนี้ คุณจะสามารถควบคุมสิ่งที่สร้างขึ้นภายในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="f9e88-149">This way, you can govern what is created within your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="f9e88-150">ปัจจุบัน จะมีระยะเวลาการเปลี่ยนผ่านระหว่างประสบการณ์ใช้งานพื้นที่ทำงานแบบเดิมกับแบบใหม่</span><span class="sxs-lookup"><span data-stu-id="f9e88-150">Currently there's a transition period between the old workspace experience and the new.</span></span> <span data-ttu-id="f9e88-151">ทั้งนี้ การตั้งค่าผู้เช่านี้จะปรับใชักับประสบการณ์ใช้งานแบบใหม่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f9e88-151">This tenant setting applies only to the new experience.</span></span>

<span data-ttu-id="f9e88-152">ตามค่าเริ่มต้น การตั้งค่า **สร้างพื้นที่ทำงาน** จะเปิดใช้งานสำหรับทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="f9e88-152">The **Create workspaces** setting is enabled by default for the entire organization.</span></span> <span data-ttu-id="f9e88-153">โดยพบได้ในกลุ่ม **การตั้งค่าพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="f9e88-153">It's found in the **Workspace settings** group.</span></span>

<span data-ttu-id="f9e88-154">เราขอแนะนำให้คุณกำหนดกลุ่มความปลอดภัยอย่างน้อยหนึ่งกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="f9e88-154">We recommend you assign one or more security groups.</span></span> <span data-ttu-id="f9e88-155">กลุ่มเหล่านี้อาจมีสิทธิ์อนุญาตทั้งแบบอนุญาต _หรือปฏิเสธ_ ในการสร้างพื้นที่ทำงานก็ได้</span><span class="sxs-lookup"><span data-stu-id="f9e88-155">These groups can be granted _or denied_ permission to create workspaces.</span></span>

<span data-ttu-id="f9e88-156">โปรดแน่ใจว่าได้ระบุคำชี้แจงไว้ในเอกสารของคุณ เพื่อแจ้งให้ผู้ใช้ (บุคคลที่ไม่มีสิทธิ์ในการสร้างพื้นที่ทำงาน) ทราบวิธีการส่งคำขอพื้นที่ทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="f9e88-156">Be sure to include instructions in your documentation letting users (who don't have workspace creation rights) know how they can request a new workspace.</span></span>

![ภาพหน้าจอของ Power B I Desktop ที่แสดงการตั้งค่า “สร้างพื้นที่ทำงาน”](media/admin-tenant-settings/create-workspaces.png)

### <a name="share-content-with-external-users"></a><span data-ttu-id="f9e88-158">แชร์เนื้อหาไปยังผู้ใช้ภายนอก</span><span class="sxs-lookup"><span data-stu-id="f9e88-158">Share content with external users</span></span>

<span data-ttu-id="f9e88-159">ผู้ใช้สามารถแชร์รายงานและแดชบอร์ดกับผู้คนที่อยู่ภายนอกองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="f9e88-159">Users can share reports and dashboards with people outside your organization.</span></span>

<span data-ttu-id="f9e88-160">ตามค่าเริ่มต้น การตั้งค่า **แชร์เนื้อหากับผู้ใช้ภายนอก** จะเปิดใช้งานสำหรับทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="f9e88-160">The **Share content with external users** setting is enabled by default for the entire organization.</span></span> <span data-ttu-id="f9e88-161">โดยพบได้ในกลุ่ม **การตั้งค่าการส่งออกและการแชร์**</span><span class="sxs-lookup"><span data-stu-id="f9e88-161">It's found in the **Export and sharing settings** group.</span></span>

<span data-ttu-id="f9e88-162">เราขอแนะนำให้คุณกำหนดกลุ่มความปลอดภัยอย่างน้อยหนึ่งกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="f9e88-162">We recommend you assign one or more security groups.</span></span> <span data-ttu-id="f9e88-163">กลุ่มเหล่านี้อาจมีสิทธิ์อนุญาตเป็นแบบอนุญาต _หรือปฏิเสธ_ ในการแชร์เนื้อหากับผู้ใช้ภายนอกก็ได้</span><span class="sxs-lookup"><span data-stu-id="f9e88-163">These groups can be granted _or denied_ permission to share content with external users.</span></span>

![ภาพหน้าจอของ Power B I Desktop ที่แสดงการตั้งค่า "แชร์เนื้อหากับผู้ใช้ภายนอก"](media/admin-tenant-settings/share-content-with-external-users.png)

### <a name="publish-to-web"></a><span data-ttu-id="f9e88-165">เผยแพร่ไปยังเว็บ</span><span class="sxs-lookup"><span data-stu-id="f9e88-165">Publish to web</span></span>

<span data-ttu-id="f9e88-166">คุณลักษณะ [เผยแพร่ไปยังเว็บ](../collaborate-share/service-publish-to-web.md) จะอนุญาตการเผยแพร่รายงานสาธารณะบนเว็บ</span><span class="sxs-lookup"><span data-stu-id="f9e88-166">The [publish to web](../collaborate-share/service-publish-to-web.md) feature allows publishing public reports on the web.</span></span> <span data-ttu-id="f9e88-167">ถ้ามีการใช้อย่างไม่เหมาะสม มีความเสี่ยงที่ข้อมูลลับอาจรั่วไหลไปบนเว็บ</span><span class="sxs-lookup"><span data-stu-id="f9e88-167">If used inappropriately, there's risk that confidential information could be made available live on the web.</span></span>

<span data-ttu-id="f9e88-168">ตามค่าเริ่มต้น การตั้งค่า **เผยแพร่ไปยังเว็บ** นี้จะเปิดใช้งานสำหรับทั้งองค์กร แต่จะจำกัดความสามารถในการสร้างโค้ดฝังตัวสำหรับผู้ใชที่ไม่ใช่ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="f9e88-168">The **Publish to web** setting is enabled by default for the entire organization, but restricting the ability for non-admin users to create embed codes.</span></span> <span data-ttu-id="f9e88-169">โดยพบได้ในกลุ่ม **การตั้งค่าการส่งออกและการแชร์**</span><span class="sxs-lookup"><span data-stu-id="f9e88-169">It's found in the **Export and sharing settings** group.</span></span>

<span data-ttu-id="f9e88-170">หากเปิดใช้งาน เราขอแนะนำให้คุณกำหนดกลุ่มความปลอดภัยอย่างน้อยหนึ่งกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="f9e88-170">If enabled, we recommend you assign one or more security groups.</span></span> <span data-ttu-id="f9e88-171">กลุ่มเหล่านี้อาจมีสิทธิ์อนุญาตทั้งแบบอนุญาต _หรือปฏิเสธ_ ในการเผยแพร่รายงานก็ได้</span><span class="sxs-lookup"><span data-stu-id="f9e88-171">These groups can be granted _or denied_ permission to publish reports.</span></span>

<span data-ttu-id="f9e88-172">นอกจากนี้ ยังมีตัวเลือกสำหรับเลือกลักษณะการทำงานของโค้ดฝังตัวของคุณอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="f9e88-172">Further, there's an option to choose how your embed codes work.</span></span> <span data-ttu-id="f9e88-173">ตามค่าเริ่มต้น จะมีการตั้งค่าเป็น **อนุญาตเฉพาะโค้ดที่มีอยู่เท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="f9e88-173">By default, it's set to **Only allow existing codes**.</span></span> <span data-ttu-id="f9e88-174">หมายความว่า ผู้ใช้จะได้รับการร้องขอให้ติดต่อผู้ดูแลระบบ Power BI สร้างโค้ดฝังตัว</span><span class="sxs-lookup"><span data-stu-id="f9e88-174">It means users will be asked to contact a Power BI admin to create an embed code.</span></span>

![ภาพหน้าจอของ Power B I Desktop ที่แสดงการตั้งค่า “เผยแพร่ไปยังเว็บ”](media/admin-tenant-settings/publish-to-web.png)

<span data-ttu-id="f9e88-176">นอกจากนี้ เราขอแนะนำให้คุณตรวจสอบ [โค้ดฝังตัวของการเผยแพร่ไปยังเว็บ](https://app.powerbi.com/admin-portal/embedCodes) เป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="f9e88-176">We also recommend you review [publish to web embed codes](https://app.powerbi.com/admin-portal/embedCodes) regularly.</span></span> <span data-ttu-id="f9e88-177">โปรดลบโค้ดออก หากมีการเผยแพร่ข้อมูลส่วนตัวหรือข้อมูลลับ</span><span class="sxs-lookup"><span data-stu-id="f9e88-177">Remove codes if they result in the publication of private or confidential information.</span></span>

### <a name="export-data"></a><span data-ttu-id="f9e88-178">ส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f9e88-178">Export data</span></span>

<span data-ttu-id="f9e88-179">คุณสามารถจำกัดผู้ใช้ไม่ให้ส่งออกข้อมูลจากไทล์แดชบอร์ดหรือวิชวลรายงานได้</span><span class="sxs-lookup"><span data-stu-id="f9e88-179">You can restrict users from exporting data from dashboard tiles or report visuals.</span></span>

<span data-ttu-id="f9e88-180">ตามค่าเริ่มต้น การตั้งค่า **ส่งออกข้อมูล** จะเปิดใช้งานสำหรับทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="f9e88-180">The **Export data** setting is enabled by default for the entire organization.</span></span> <span data-ttu-id="f9e88-181">โดยพบได้ในกลุ่ม **การตั้งค่าการส่งออกและการแชร์**</span><span class="sxs-lookup"><span data-stu-id="f9e88-181">It's found in the **Export and sharing settings** group.</span></span>

<span data-ttu-id="f9e88-182">เราขอแนะนำให้คุณกำหนดกลุ่มความปลอดภัยอย่างน้อยหนึ่งกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="f9e88-182">We recommend you assign one or more security groups.</span></span> <span data-ttu-id="f9e88-183">กลุ่มเหล่านี้อาจมีสิทธิ์อนุญาตทั้งแบบอนุญาต _หรือปฏิเสธ_ ในการเผยแพร่รายงานก็ได้</span><span class="sxs-lookup"><span data-stu-id="f9e88-183">These groups can be granted _or denied_ permission to publish reports.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f9e88-184">นอกจากนี้ การปิดใช้งานการตั้งค่านี้จะจำกัดการใช้คุณลักษณะ [การวิเคราะห์ใน Excel](../collaborate-share/service-analyze-in-excel.md) และ[การเชื่อมต่อแบบสด](../connect-data/desktop-report-lifecycle-datasets.md#using-a-power-bi-service-live-connection-for-report-lifecycle-management)ของบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="f9e88-184">Disabling this setting also restricts the use of the [Analyze in Excel](../collaborate-share/service-analyze-in-excel.md) and Power BI service [live connection](../connect-data/desktop-report-lifecycle-datasets.md#using-a-power-bi-service-live-connection-for-report-lifecycle-management) features.</span></span>

![ภาพหน้าจอของ Power B I Desktop ที่แสดงการตั้งค่า “ส่งออกข้อมูล”](media/admin-tenant-settings/export-data.png)

> [!NOTE]
> <span data-ttu-id="f9e88-186">หากผู้ใช้อนุญาตให้ผู้ใช้ส่งออกข้อมูลได้ คุณจะสามารถเพิ่มระดับชั้นการปกป้องได้โดยการเปิดใช้ [การปกป้องข้อมูล](../admin/service-security-data-protection-overview.md)</span><span class="sxs-lookup"><span data-stu-id="f9e88-186">If users allow users to export data, you can add a layer of protection by enforcing [data protection](../admin/service-security-data-protection-overview.md).</span></span> <span data-ttu-id="f9e88-187">หลังจากกำหนดค่าแล้ว ระบบจะบล็อกผู้ใช้ที่ไม่ได้รับอนุญาต ไม่ให้ส่งออกเนื้อหาที่มีป้ายกำกับว่าเป็นข้อมูลสำคัญ</span><span class="sxs-lookup"><span data-stu-id="f9e88-187">When configured, unauthorized users will be blocked from exporting content with sensitivity labels.</span></span>

### <a name="allow-external-guest-users-to-edit-and-manage-content-in-the-organization"></a><span data-ttu-id="f9e88-188">อนุญาตให้ผู้ใช้ที่เป็นผู้เยี่ยมชมภายนอกแก้ไขและจัดการเนื้อหาในองค์กร</span><span class="sxs-lookup"><span data-stu-id="f9e88-188">Allow external guest users to edit and manage content in the organization</span></span>

<span data-ttu-id="f9e88-189">มีความเป็นไปได้ที่ผู้ใช้ที่เป็นผู้เยี่ยมชมจากภายนอกสามารถแก้ไขและจัดการเนื้อหา Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="f9e88-189">It's possible that external guest users can edit and manage Power BI content.</span></span> <span data-ttu-id="f9e88-190">สำหรับข้อมูลเพิ่มเติม โปรดดู [กระจายเนื้อหา Power BI ไปยังผู้ใช้ที่เป็นผู้เยี่ยมชมจากภายนอกด้วย Azure AD B2B](../admin/service-admin-azure-ad-b2b.md)</span><span class="sxs-lookup"><span data-stu-id="f9e88-190">For more information, see [Distribute Power BI content to external guest users with Azure AD B2B](../admin/service-admin-azure-ad-b2b.md).</span></span>

<span data-ttu-id="f9e88-191">ตามค่าเริ่มต้น การตั้งค่า **อนุญาตให้ผู้ใช้ที่เป็นผู้เยี่ยมชมภายนอกแก้ไขและจัดการเนื้อหาในองค์กร** จะปิดใช้งานสำหรับทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="f9e88-191">The **Allow external guest users to edit and manage content in the organization** setting is disabled by default for the entire organization.</span></span> <span data-ttu-id="f9e88-192">โดยพบได้ในกลุ่ม **การตั้งค่าการส่งออกและการแชร์**</span><span class="sxs-lookup"><span data-stu-id="f9e88-192">It's found in the **Export and sharing settings** group.</span></span>

<span data-ttu-id="f9e88-193">หากคุณต้องการอนุญาตให้ผู้ใช้ภายนอกสามารถแก้ไขและจัดการเนื้อหาได้ เราขอแนะนำให้คุณกำหนดกลุ่มความปลอดภัยอย่างน้อยหนึ่งกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="f9e88-193">If you need to authorize external users to edit and manage content, we recommend you assign one or more security groups.</span></span> <span data-ttu-id="f9e88-194">กลุ่มเหล่านี้อาจมีสิทธิ์อนุญาตทั้งแบบอนุญาต _หรือปฏิเสธ_ ในการเผยแพร่รายงานก็ได้</span><span class="sxs-lookup"><span data-stu-id="f9e88-194">These groups can be granted _or denied_ permission to publish reports.</span></span>

![ภาพหน้าจอของ Power B I Desktop ที่แสดงการตั้งค่า "อนุญาตให้ผู้ใช้ที่เป็นผู้เยี่ยมชมภายนอกแก้ไขและจัดการเนื้อหาในองค์กร"](media/admin-tenant-settings/allow-external-guest-users.png)

### <a name="developer-settings"></a><span data-ttu-id="f9e88-196">การตั้งค่าผู้พัฒนา</span><span class="sxs-lookup"><span data-stu-id="f9e88-196">Developer settings</span></span>

<span data-ttu-id="f9e88-197">มีการตั้งค่าผู้เช่าที่เกี่ยวกับ [การฝังเนื้อหา Power BI](../developer/embedded/embedding.md) สองแบบ</span><span class="sxs-lookup"><span data-stu-id="f9e88-197">There are two tenant settings related to [embedding Power BI content](../developer/embedded/embedding.md).</span></span> <span data-ttu-id="f9e88-198">คือ:</span><span class="sxs-lookup"><span data-stu-id="f9e88-198">They are:</span></span>

- <span data-ttu-id="f9e88-199">เนื้อหาที่ฝังในแอป (เปิดใช้งานตามค่าเริ่มต้น)</span><span class="sxs-lookup"><span data-stu-id="f9e88-199">Embed content in apps (enabled by default)</span></span>
- <span data-ttu-id="f9e88-200">อนุญาตให้ผู้ใช้บริการหลักใช้ API ของ Power BI (ปิดใช้งานตามค่าเริ่มต้น)</span><span class="sxs-lookup"><span data-stu-id="f9e88-200">Allow service principals to user Power BI APIs (disabled by default)</span></span>

<span data-ttu-id="f9e88-201">หากคุณไม่ต้องการใช้ API ของนักพัฒนาในการฝังเนื้อหา เราขอแนะนำให้คุณปิดการใช้งานฟังก์ชันนี้</span><span class="sxs-lookup"><span data-stu-id="f9e88-201">If you have no intention of using the developer APIs to embed content, we recommend you disable them.</span></span> <span data-ttu-id="f9e88-202">หรืออย่างน้อย กำหนดค่ากลุ่มความปลอดภัยเฉพาะที่จะทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="f9e88-202">Or, at least configure specific security groups that would be doing this work.</span></span>

![ภาพหน้าจอของ Power B I Desktop ที่แสดงการตั้งค่านักพัฒนา](media/admin-tenant-settings/developer-settings.png)

## <a name="next-steps"></a><span data-ttu-id="f9e88-204">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="f9e88-204">Next steps</span></span>

<span data-ttu-id="f9e88-205">สำหรับข้อมูลเพิ่มเติมที่เกี่ยวข้องกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f9e88-205">For more information related to this article, check out the following resources:</span></span>

- [<span data-ttu-id="f9e88-206">การดูแลระบบ Power BI คืออะไร?</span><span class="sxs-lookup"><span data-stu-id="f9e88-206">What is Power BI administration?</span></span>](../admin/service-admin-administering-power-bi-in-your-organization.md)
- [<span data-ttu-id="f9e88-207">การดูแล Power BI ในพอร์ทัลผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="f9e88-207">Administering Power BI in the admin portal</span></span>](../admin/service-admin-portal.md)
- <span data-ttu-id="f9e88-208">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f9e88-208">Questions?</span></span> [<span data-ttu-id="f9e88-209">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="f9e88-209">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="f9e88-210">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="f9e88-210">Suggestions?</span></span> [<span data-ttu-id="f9e88-211">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="f9e88-211">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com)