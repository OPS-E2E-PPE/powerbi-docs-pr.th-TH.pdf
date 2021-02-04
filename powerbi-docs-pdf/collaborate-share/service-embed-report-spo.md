---
title: ฝังส่วนเว็บรายงานใน SharePoint Online
description: ด้วยส่วยรายงานเว็บ Power BI ใหม่ สำหรับ SharePoint Online คุณสามารถฝังรายงาน Power BI แบบโต้ตอบได้อย่างง่ายดายในหน้า SharePoint Online
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
LocalizationGroup: Share your work
ms.date: 01/04/2021
ms.openlocfilehash: e4d31a7bf83d4e94e2f3b71ca43924d468268f76
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888420"
---
# <a name="embed-a-report-web-part-in-sharepoint-online"></a><span data-ttu-id="94a5d-103">ฝังส่วนเว็บรายงานใน SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="94a5d-103">Embed a report web part in SharePoint Online</span></span>

<span data-ttu-id="94a5d-104">ด้วย web part ของรายงาน Power BI ใหม่สำหรับ SharePoint Online คุณสามารถฝังรายงาน Power BI แบบโต้ตอบได้อย่างง่ายดายในหน้า SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="94a5d-104">With the new Power BI report web part for SharePoint Online, you can easily embed interactive Power BI reports in SharePoint Online pages.</span></span>

<span data-ttu-id="94a5d-105">เมื่อใช้ตัวเลือกใหม่ **ฝังใน SharePoint Online** รายงานแบบฝังจะคำนึงถึงการอนุญาตรายการทั้งหมดและความปลอดภัยของข้อมูลผ่าน [การรักษาความปลอดภัยระดับแถว (RLS)](../admin/service-admin-rls.md) เพื่อให้คุณสามารถสร้างพอร์ทัลภายในที่ปลอดภัยได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="94a5d-105">When using the new **Embed in SharePoint Online** option, the embedded reports respect all item permissions and data security through [row-level security (RLS)](../admin/service-admin-rls.md), so you can easily create secure internal portals.</span></span>

## <a name="requirements"></a><span data-ttu-id="94a5d-106">ข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="94a5d-106">Requirements</span></span>

<span data-ttu-id="94a5d-107">สำหรับรายงาน **ที่ฝังใน SharePoint Online** เพื่อทำงาน ต้องมี:</span><span class="sxs-lookup"><span data-stu-id="94a5d-107">For **Embed in SharePoint Online** reports to work, the following is required:</span></span>

* <span data-ttu-id="94a5d-108">สิทธิการใช้งาน Power BI Pro หรือความจุ [Power BI Premium (EM หรือ P SKU)](../admin/service-premium-what-is.md) พร้อมสิทธิการใช้งาน Power BI</span><span class="sxs-lookup"><span data-stu-id="94a5d-108">A Power BI Pro license or a [Power BI Premium capacity (EM or P SKU)](../admin/service-premium-what-is.md) with a Power BI license.</span></span>
* <span data-ttu-id="94a5d-109">Power BI web part สำหรับ SharePoint Online จำเป็นต้องใช้[หน้าที่ทันสมัย](https://support.office.com/article/Allow-or-prevent-creation-of-modern-site-pages-by-end-users-c41d9cc8-c5c0-46b4-8b87-ea66abc6e63b)</span><span class="sxs-lookup"><span data-stu-id="94a5d-109">The Power BI web part for SharePoint Online requires [Modern Pages](https://support.office.com/article/Allow-or-prevent-creation-of-modern-site-pages-by-end-users-c41d9cc8-c5c0-46b4-8b87-ea66abc6e63b).</span></span>
* <span data-ttu-id="94a5d-110">ในการใช้รายงานแบบฝัง ผู้ใช้ต้องลงชื่อเข้าใช้ในบริการของ Power BI เพื่อเปิดใช้สิทธิ์การใช้งาน Power BI ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="94a5d-110">To consume an embedded report, users must sign in to Power BI service to activate their Power BI license.</span></span>

> [!Note]
> <span data-ttu-id="94a5d-111">สำหรับองค์กรในระบบคลาวด์ Power BI National ไม่มีสิทธิ์การใช้งานฟรี</span><span class="sxs-lookup"><span data-stu-id="94a5d-111">For organizations in Power BI National clouds, there's no free license.</span></span> <span data-ttu-id="94a5d-112">ในสภาพแวดล้อมนี้ ผู้ใช้ทั้งหมดที่ต้องการเข้าถึงรายงานแบบฝังตัวใน Sharepoint ต้องมีสิทธิ์การใช้งาน Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="94a5d-112">In this environment, all users who want access to the embedded report in Sharepoint need to have a Power BI Pro license.</span></span>

## <a name="embed-your-report"></a><span data-ttu-id="94a5d-113">ฝังรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="94a5d-113">Embed your report</span></span>
<span data-ttu-id="94a5d-114">ในการฝังรายงานของคุณลงใน SharePoint Online คุณจะต้องได้รับ URL ของรายงานและใช้กับ Web Part ของ Power BI ของ SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="94a5d-114">To embed your report into SharePoint Online, you need to get the report URL and use it with SharePoint Online's Power BI web part.</span></span>

### <a name="get-a-report-url"></a><span data-ttu-id="94a5d-115">รับ URL ของรายงาน</span><span class="sxs-lookup"><span data-stu-id="94a5d-115">Get a report URL</span></span>

1. <span data-ttu-id="94a5d-116">เปิดรายงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="94a5d-116">Open a report in the Power BI service.</span></span>

2. <span data-ttu-id="94a5d-117">บนเมนู **แชร์** ให้เลือก **ฝังรายงาน** > **SharePoint Online**</span><span class="sxs-lookup"><span data-stu-id="94a5d-117">On the **Share** menu, select **Embed report** > **SharePoint Online**.</span></span>

    ![เมนูตัวเลือกเพิ่มเติม, SharePoint Online](media/service-embed-report-spo/power-bi-more-options-sharepoint-online.png)

3. <span data-ttu-id="94a5d-119">คัดลอก URL ของรายงานจากกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="94a5d-119">Copy the report URL from the dialog.</span></span>

    ![ลิงก์ที่ฝังไว้](media/service-embed-report-spo/powerbi-embed-link-sharepoint.png)

### <a name="add-the-power-bi-report-to-a-sharepoint-online-page"></a><span data-ttu-id="94a5d-121">เพิ่มรายงาน Power BI ลงในหน้า SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="94a5d-121">Add the Power BI report to a SharePoint Online page</span></span>

1. <span data-ttu-id="94a5d-122">เปิดหน้าเป้าหมายใน SharePoint Online และเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="94a5d-122">Open the target page in SharePoint Online and select **Edit**.</span></span>

    ![หน้าแก้ไข SP](media/service-embed-report-spo/powerbi-sharepoint-edit-page.png)

    <span data-ttu-id="94a5d-124">หรือสร้างไซต์ที่ทันสมัยใหม่โดยการเลือก **+ ใหม่** ภายใน SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="94a5d-124">Or, in Sharepoint Online, select **+ New**  to create a new modern site page.</span></span>

    ![หน้าใหม่ SP](media/service-embed-report-spo/powerbi-sharepoint-new-page.png)

2. <span data-ttu-id="94a5d-126">เลือกรายงานดรอปดาวน์ **+** แล้วเลือก Web Part ของ **Power BI**</span><span class="sxs-lookup"><span data-stu-id="94a5d-126">Select the **+** dropdown and then select the **Power BI** web part.</span></span>

    ![web part ใหม่ของ SP](media/service-embed-report-spo/powerbi-sharepoint-new-web-part.png)

3. <span data-ttu-id="94a5d-128">เลือก **เพิ่มรายงาน**</span><span class="sxs-lookup"><span data-stu-id="94a5d-128">Select **Add report**.</span></span>

    ![รายงานใหม่ของ SP](media/service-embed-report-spo/powerbi-sharepoint-new-report.png)  

4. <span data-ttu-id="94a5d-130">วาง URL ของรายงานที่คัดลอกก่อนหน้านี้ไว้ที่บานหน้าต่าง **ลิงก์รายงาน Power BI**</span><span class="sxs-lookup"><span data-stu-id="94a5d-130">Paste the previously-copied report URL into the **Power BI report link** pane.</span></span> <span data-ttu-id="94a5d-131">รายงานโหลดโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="94a5d-131">The report loads automatically.</span></span>

    ![คุณสมบัติ web part ใหม่ของ SP](media/service-embed-report-spo/powerbi-sharepoint-new-web-part-properties.png)

5. <span data-ttu-id="94a5d-133">เลือก **เผยแพร่** เพื่อทำการเปลี่ยนแปลงการมองเห็นให้ผู้ใช้ SharePoint Online ของคุณ</span><span class="sxs-lookup"><span data-stu-id="94a5d-133">Select **Publish** to make the change visible to your SharePoint Online users.</span></span>

    ![รายงาน SP โหลดแล้ว](media/service-embed-report-spo/powerbi-sharepoint-report-loaded.png)

## <a name="grant-access-to-reports"></a><span data-ttu-id="94a5d-135">อนุญาตการเข้าถึงรายงาน</span><span class="sxs-lookup"><span data-stu-id="94a5d-135">Grant access to reports</span></span>

<span data-ttu-id="94a5d-136">การฝังรายงานใน SharePoint Online ไม่ให้สิทธิผู้ใช้ในการดูรายงานโดยอัตโนมัติ คุณต้องตั้งค่าสิทธิการดูใน Power BI</span><span class="sxs-lookup"><span data-stu-id="94a5d-136">Embedding a report in SharePoint Online doesn't automatically give users permission to view the report - you need to set view permissions in Power BI.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94a5d-137">ให้ตรวจสอบให้แน่ใจว่าว่าใครสามารถดูรายงานภายใน Power BI service และอนุญาตให้เข้าถึงสิ่งที่ไม่ได้อยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="94a5d-137">Make sure to review who can see the report within the Power BI service and grant access to those not listed.</span></span>

<span data-ttu-id="94a5d-138">มีสองวิธีที่ให้สิทธิการเข้าถึงรายงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="94a5d-138">There are two ways to provide report access in Power BI.</span></span> <span data-ttu-id="94a5d-139">วิธีแรก ถ้าคุณกำลังใช้ Microsoft 365 Group เพื่อสร้างไซต์ทีม SharePoint Online ของคุณ แสดงว่าคุณได้สร้างรายการผู้ใช้ในฐานะสมาชิกของ **พื้นที่ทำงานภายในบริการของ Power BI** และ **หน้า SharePoint**</span><span class="sxs-lookup"><span data-stu-id="94a5d-139">The first way, if you're using a Microsoft 365 Group to build your SharePoint Online team site, is to list the user as a member of the **workspace within the Power BI service** and the **SharePoint page**.</span></span> <span data-ttu-id="94a5d-140">สำหรับข้อมูลเพิ่มเติม ดูวิธีการ[จัดการพื้นที่ทำงาน](service-manage-app-workspace-in-power-bi-and-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="94a5d-140">For more information, see how to [manage a workspace](service-manage-app-workspace-in-power-bi-and-office-365.md).</span></span>

<span data-ttu-id="94a5d-141">วิธีสองคือการฝังรายงานภายในแอป และแชร์โดยตรงกับผู้ใช้:</span><span class="sxs-lookup"><span data-stu-id="94a5d-141">The second way is to embed a report within an app and share it directly with users:</span></span>  

1. <span data-ttu-id="94a5d-142">ผู้เขียนซึ่งต้องเป็นผู้ใช้ระดับ Pro จะสร้างรายงานในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="94a5d-142">The author, who must be a Pro user, creates a report in a workspace.</span></span> <span data-ttu-id="94a5d-143">หากต้องการแชร์กับ *ผู้ใช้ฟรีของ Power BI* ให้ตั้งค่าพื้นที่ทำงานเป็น *พื้นที่ทำงานแบบพรีเมียม*</span><span class="sxs-lookup"><span data-stu-id="94a5d-143">To share with *Power BI free users*, the workspace needs to be set as a *Premium workspace*.</span></span>

2. <span data-ttu-id="94a5d-144">ผู้เขียนจะเผยแพร่แอป จากนั้นจะติดตั้งแอป</span><span class="sxs-lookup"><span data-stu-id="94a5d-144">The author publishes the app and installs it.</span></span> <span data-ttu-id="94a5d-145">ผู้เขียนต้องติดตั้งแอปเพื่อให้แอปเข้าถึง URL ของรายงานที่ใช้สำหรับการฝังใน SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="94a5d-145">The author must install the app so it has access to the report URL that is used for embedding in SharePoint Online.</span></span>

3. <span data-ttu-id="94a5d-146">ในขั้นนี้ ผู้ใช้ทั้งหมดจำเป็นต้องติดตั้งแอปเช่นเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="94a5d-146">Now all end users need to install the app too.</span></span> <span data-ttu-id="94a5d-147">คุณยังสามารถใช้คุณลักษณะ **ติดตั้งแอปโดยอัตโนมัติ** ซึ่งสามารถเปิดใช้งานได้ใน [พอร์ทัลผู้ดูแลระบบ Power BI](../admin/service-admin-portal.md) เพื่อให้แอปติดตั้งล่วงหน้าสำหรับผู้ใช้ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="94a5d-147">You can also use the **Install app automatically** feature, which you can enable in the [Power BI admin portal](../admin/service-admin-portal.md), to have the app pre-installed for end users.</span></span>

   ![ติดตั้งแอปโดยอัตโนมัติ](media/service-embed-report-spo/install-app-automatically.png)

4. <span data-ttu-id="94a5d-149">ผู้เขียนเปิดแอปและไปยังรายงาน</span><span class="sxs-lookup"><span data-stu-id="94a5d-149">The author opens the app and goes to the report.</span></span>

5. <span data-ttu-id="94a5d-150">ผู้เขียนคัดลอก URL ของรายงานแบบฝังตัวจากรายงานที่แอปติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="94a5d-150">The author copies the embed report URL from the report the app installed.</span></span> <span data-ttu-id="94a5d-151">อย่าใช้ URL ของรายงานต้นฉบับจากพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="94a5d-151">Don't use the original report URL from the workspace.</span></span>

6. <span data-ttu-id="94a5d-152">สร้างไซต์ทีมใหม่ใน SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="94a5d-152">Create a new team site in SharePoint Online.</span></span>

7. <span data-ttu-id="94a5d-153">เพิ่ม URL ของรายงานที่คัดลอกก่อนนี้ใน Web Part ของ Power BI</span><span class="sxs-lookup"><span data-stu-id="94a5d-153">Add the previously-copied report URL to the Power BI web part.</span></span>

8. <span data-ttu-id="94a5d-154">เพิ่มผู้ใช้ปลายทางและ/หรือกลุ่มทั้งหมดที่จะใช้ข้อมูลบนหน้า SharePoint Online และในแอป Power BI ที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="94a5d-154">Add all end users and/or groups who are going to consume the data on the SharePoint Online page and in the Power BI app you created.</span></span>

    > [!NOTE]
    > <span data-ttu-id="94a5d-155">**ผู้ใช้หรือกลุ่มจำเป็นต้องเข้าถึงทั้งหน้า SharePoint Online และรายงานในแอป Power BI เพื่อดูรายงานบนหน้า SharePoint**</span><span class="sxs-lookup"><span data-stu-id="94a5d-155">**Users or groups need access to both the SharePoint Online page and the report in the Power BI app to see the report on the SharePoint page.**</span></span>

<span data-ttu-id="94a5d-156">ในตอนนี้ ผู้ใช้ปลายทางสามารถไปยังไซต์ทีมใน SharePoint Online และดูรายงานบนหน้าได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="94a5d-156">Now the end user can go to the team site in SharePoint Online and view the reports on the page.</span></span>

## <a name="multi-factor-authentication"></a><span data-ttu-id="94a5d-157">การรับรองตัวตนแบบหลายปัจจัย</span><span class="sxs-lookup"><span data-stu-id="94a5d-157">Multi-factor authentication</span></span>

<span data-ttu-id="94a5d-158">ถ้าสภาพแวดล้อม Power BI ของคุณทำให้คุณต้องลงชื่อเข้าใช้ด้วยการใช้การรับรองความถูกต้องแบบหลายปัจจัย คุณอาจถูกขอให้ลงชื่อเข้าใช้ด้วยอุปกรณ์ความปลอดภัยเพื่อยืนยันข้อมูลประจำตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="94a5d-158">If your Power BI environment requires you to sign in using multi-factor authentication, you may be asked to sign in with a security device to verify your identity.</span></span> <span data-ttu-id="94a5d-159">ซึ่งเกิดขึ้นถ้าคุณไม่ได้ไม่ลงชื่อเข้าใช้ SharePoint Online โดยใช้การรับรองความถูกต้องแบบหลายปัจจัยแต่สภาพแวดล้อม Power BI ของคุณ กำหนดให้อุปกรณ์ความปลอดภัยตรวจสอบบัญชีผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="94a5d-159">This occurs if you did not sign in to SharePoint Online using multi-factor authentication, but your Power BI environment requires a security device to validate an account.</span></span>

> [!NOTE]
> <span data-ttu-id="94a5d-160">Power BI ยังไม่สนับสนุนการรับรองความถูกต้องโดยใช้หลายปัจจัยด้วย Azure Active Directory 2.0 - ผู้ใช้จะเห็นข้อความแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="94a5d-160">Power BI does not yet support multi-factor authentication with Azure Active Directory 2.0 - users will see an error message.</span></span> <span data-ttu-id="94a5d-161">ถ้าผู้ใช้ลงชื่อเข้าใช้ SharePoint Online อีกครั้งโดยใช้อุปกรณ์ความปลอดภัยของพวกเขา พวกเขาอาจสามารถดูรายงานได้</span><span class="sxs-lookup"><span data-stu-id="94a5d-161">If the user signs in again to SharePoint Online using their security device, they may be able to view the report.</span></span>

## <a name="web-part-settings"></a><span data-ttu-id="94a5d-162">ตั้งค่า web part</span><span class="sxs-lookup"><span data-stu-id="94a5d-162">Web part settings</span></span>

<span data-ttu-id="94a5d-163">ด้านล่างคือการตั้งค่าที่คุณสามารถปรับเปลี่ยนสำหรับ Web Part ของ Power BI สำหรับ SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="94a5d-163">Below are the settings you can adjust for the Power BI web part for SharePoint Online.</span></span>

![คุณสมบัติ web part ใหม่ของ SP](media/service-embed-report-spo/powerbi-sharepoint-web-part-properties.png)

| <span data-ttu-id="94a5d-165">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="94a5d-165">Property</span></span> | <span data-ttu-id="94a5d-166">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="94a5d-166">Description</span></span> |
| --- | --- |
| <span data-ttu-id="94a5d-167">ชื่อหน้า</span><span class="sxs-lookup"><span data-stu-id="94a5d-167">Page name</span></span> |<span data-ttu-id="94a5d-168">ตั้งค่าหน้าเริ่มต้นของ Web Part</span><span class="sxs-lookup"><span data-stu-id="94a5d-168">Sets the web part's default page.</span></span> <span data-ttu-id="94a5d-169">เลือกค่าจากรายการแบบดรอปดาวน์</span><span class="sxs-lookup"><span data-stu-id="94a5d-169">Select a value from the drop-down.</span></span> <span data-ttu-id="94a5d-170">ถ้าไม่มีการแสดงหน้า รายงานของคุณมีหน้าหนึ่ง หรือ URL ที่คุณวางมีชื่อหน้า</span><span class="sxs-lookup"><span data-stu-id="94a5d-170">If no pages are displayed, either your report has one page, or the URL you pasted contains a page name.</span></span> <span data-ttu-id="94a5d-171">ลบส่วนของรายงานจาก URL เมื่อต้องเลือกหน้าใดหน้าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="94a5d-171">Remove the report section from the URL to select a specific page.</span></span> |
| <span data-ttu-id="94a5d-172">แสดง</span><span class="sxs-lookup"><span data-stu-id="94a5d-172">Display</span></span> |<span data-ttu-id="94a5d-173">ปรับวิธีการจัดรายงานให้พอดีกับหน้า SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="94a5d-173">Adjusts how the report fits within the SharePoint Online page.</span></span> |
| <span data-ttu-id="94a5d-174">แสดงบานหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="94a5d-174">Show Nav Pane</span></span> |<span data-ttu-id="94a5d-175">แสดงหรือซ่อนบานหน้าหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="94a5d-175">Shows or hides the page nav pane.</span></span> |
| <span data-ttu-id="94a5d-176">แสดงบานหน้าต่างตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="94a5d-176">Show Filter Pane</span></span> |<span data-ttu-id="94a5d-177">แสดงหรือซ่อนบานหน้าต่างตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="94a5d-177">Shows or hides the filter pane.</span></span> |

## <a name="reports-that-do-not-load"></a><span data-ttu-id="94a5d-178">รายงานที่โหลดไม่ได้</span><span class="sxs-lookup"><span data-stu-id="94a5d-178">Reports that do not load</span></span>

<span data-ttu-id="94a5d-179">หากรายงานของคุณอาจไม่โหลดภายใน Web Part ของ Power BI คุณอาจแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="94a5d-179">If your report does not load within the Power BI web part, you may see the following message:</span></span>

![เนื้อหานี้ไม่มีข้อความ](media/service-embed-report-spo/powerbi-sharepoint-report-not-found.png)

<span data-ttu-id="94a5d-181">มีเหตุผลโดยทั่วไปสำหรับข้อความนี้สองตัว</span><span class="sxs-lookup"><span data-stu-id="94a5d-181">There are two common reasons for this message.</span></span>

1. <span data-ttu-id="94a5d-182">คุณไม่มีสิทธิเข้าถึงรายงาน</span><span class="sxs-lookup"><span data-stu-id="94a5d-182">You do not have report access.</span></span>
2. <span data-ttu-id="94a5d-183">รายงานถูกลบ</span><span class="sxs-lookup"><span data-stu-id="94a5d-183">The report was deleted.</span></span>

<span data-ttu-id="94a5d-184">ติดต่อกับเจ้าของหน้า SharePoint Online เพื่อช่วยแก้ไขปัญหาได้</span><span class="sxs-lookup"><span data-stu-id="94a5d-184">Contact the SharePoint Online page owner to help resolve the issue.</span></span>

## <a name="licensing"></a><span data-ttu-id="94a5d-185">สิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="94a5d-185">Licensing</span></span>

<span data-ttu-id="94a5d-186">การที่ผู้ใช้ดูรายงานใน SharePoint ต้องมี **ใบอนุญาตใช้งาน Power BI Pro** หรือไม่เช่นนั้นเนื้อหาต้องอยู่ในพื้นที่ทำงานที่อยู่ใน **[ความจุพรีเมียมของ Power BI (EM หรือ P SKU)](../admin/service-admin-premium-purchase.md)**</span><span class="sxs-lookup"><span data-stu-id="94a5d-186">Users viewing a report in SharePoint need either a **Power BI Pro license** or the content needs to be in a workspace that's in a **[Power BI Premium capacity (EM or P SKU)](../admin/service-admin-premium-purchase.md)**.</span></span>

## <a name="known-issues-and-limitations"></a><span data-ttu-id="94a5d-187">ปัญหาและขีดจำกัดที่ทราบแล้ว</span><span class="sxs-lookup"><span data-stu-id="94a5d-187">Known issues and limitations</span></span>

* <span data-ttu-id="94a5d-188">ข้อผิดพลาด: "เกิดข้อผิดพลาด โปรดลองออกจากระบบ และย้อนกลับมา แล้วเข้ามาเยี่ยมชมหน้านี้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="94a5d-188">Error: "An error occurred, please try logging out and back in and then revisiting this page.</span></span> <span data-ttu-id="94a5d-189">ID สหสัมพันธ์: ไม่ได้กำหนด http สถานะการตอบสนอง: 400 รหัสผิดพลาดของเซิร์ฟเวอร์ 10001 ข้อความ: รีเฟรชโทเค็นหายไป</span><span class="sxs-lookup"><span data-stu-id="94a5d-189">Correlation ID: undefined, http response status: 400, server error code 10001, message: Missing refresh token"</span></span>
  
  <span data-ttu-id="94a5d-190">ถ้าคุณได้รับข้อผิดพลาดนี้ โปรดทำตามขั้นตอนการแก้ปัญหาขั้นตอนใดขั้นตอนหนึ่งด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="94a5d-190">If you receive this error, try one of the troubleshooting steps below.</span></span>
  
  1. <span data-ttu-id="94a5d-191">ลงชื่อออกจาก SharePoint และลงชื่อกลับเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="94a5d-191">Sign out of SharePoint and sign back in.</span></span> <span data-ttu-id="94a5d-192">ตรวจสอบให้แน่ใจว่าปิดหน้าต่างเบราว์เซอร์ทั้งหมดก่อนที่ลงชื่อกลับเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="94a5d-192">Be sure to close all browser windows before signing back in.</span></span>

  2. <span data-ttu-id="94a5d-193">ถ้าบัญชีผู้ใช้ของคุณจำเป็นต้องใช้การรับรองความถูกต้องโดยใช้หลายปัจจัย (MFA) ให้ลงชื่อเข้าใช้ SharePoint โดยใช้อุปกรณ์ MFA (แอปโทรศัพท์ สมาร์ทการ์ด และอื่น ๆ)</span><span class="sxs-lookup"><span data-stu-id="94a5d-193">If your user account requires multi-factor authentication (MFA), then sign in to SharePoint using your MFA device (phone app, smart card, etc.).</span></span>
  
  3. <span data-ttu-id="94a5d-194">บัญชีผู้ใช้ Azure B2B Guest ไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="94a5d-194">Azure B2B Guest users accounts are not supported.</span></span> <span data-ttu-id="94a5d-195">ผู้ใช้เห็นโลโก้ Power BI ที่แสดงส่วนที่กำลังโหลด แต่ไม่ได้แสดงรายงาน</span><span class="sxs-lookup"><span data-stu-id="94a5d-195">Users see the Power BI logo that shows the part is loading, but it doesn't show the report.</span></span>

* <span data-ttu-id="94a5d-196">Power BI ไม่รองรับภาษาเดียวกับที่ SharePoint Online รองรับ</span><span class="sxs-lookup"><span data-stu-id="94a5d-196">Power BI does not support the same localized languages that SharePoint Online does.</span></span> <span data-ttu-id="94a5d-197">ผลที่ได้คือคุณอาจไม่เห็นการแปลที่เหมาะสมภายในรายงานแบบฝังตัว</span><span class="sxs-lookup"><span data-stu-id="94a5d-197">As a result, you may not see proper localization within the embedded report.</span></span>

* <span data-ttu-id="94a5d-198">คุณอาจพบปัญหาถ้าใช้ Internet Explorer 10</span><span class="sxs-lookup"><span data-stu-id="94a5d-198">You may encounter issues if using Internet Explorer 10.</span></span> <!--You can look at the [browsers support for Power BI](../fundamentals/power-bi-browsers.md) and for [Microsoft 365](https://products.office.com/office-system-requirements#Browsers-section). -->

* <span data-ttu-id="94a5d-199">Web part Power BI จะไม่พร้อมใช้งานสำหรับ [ระบบคลาวด์แห่งชาติ](https://powerbi.microsoft.com/clouds/)</span><span class="sxs-lookup"><span data-stu-id="94a5d-199">The Power BI web part is not available for [national clouds](https://powerbi.microsoft.com/clouds/).</span></span>

* <span data-ttu-id="94a5d-200">SharePoint Server แบบคลาสสิกไม่ได้รับการสนับสนุนด้วย web part นี้</span><span class="sxs-lookup"><span data-stu-id="94a5d-200">The classic SharePoint Server is not supported with this web part.</span></span>

* <span data-ttu-id="94a5d-201">[ตัวกรอง URL](service-url-filters.md) จะไม่ได้รับการสนับสนุนด้วย SPO web part</span><span class="sxs-lookup"><span data-stu-id="94a5d-201">[URL filters](service-url-filters.md) are not supported with the SPO web part.</span></span>

## <a name="next-steps"></a><span data-ttu-id="94a5d-202">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="94a5d-202">Next steps</span></span>

* [<span data-ttu-id="94a5d-203">อนุญาตหรือป้องกันไม่ให้สร้างไซต์แบบสมัยใหม่โดยผู้ใช้ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="94a5d-203">Allow or prevent creation of modern site pages by end users</span></span>](https://support.office.com/article/Allow-or-prevent-creation-of-modern-site-pages-by-end-users-c41d9cc8-c5c0-46b4-8b87-ea66abc6e63b)  
* [<span data-ttu-id="94a5d-204">สร้างและกระจายแอปฯใน Power BI</span><span class="sxs-lookup"><span data-stu-id="94a5d-204">Create and distribute an app in Power BI</span></span>](service-create-distribute-apps.md)  
* [<span data-ttu-id="94a5d-205">แชร์แดชบอร์ดกับเพื่อนร่วมงานและคนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="94a5d-205">Share a dashboard with colleagues and others</span></span>](service-share-dashboards.md)  
* [<span data-ttu-id="94a5d-206">Power BI Premium คืออะไร?</span><span class="sxs-lookup"><span data-stu-id="94a5d-206">What is Power BI Premium?</span></span>](../admin/service-premium-what-is.md)
* [<span data-ttu-id="94a5d-207">ฝังรายงานในพอร์ทัลความปลอดภัยหรือเว็บไซต์</span><span class="sxs-lookup"><span data-stu-id="94a5d-207">Embed report in a secure portal or website</span></span>](service-embed-secure.md)

<span data-ttu-id="94a5d-208">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="94a5d-208">More questions?</span></span> [<span data-ttu-id="94a5d-209">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="94a5d-209">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
