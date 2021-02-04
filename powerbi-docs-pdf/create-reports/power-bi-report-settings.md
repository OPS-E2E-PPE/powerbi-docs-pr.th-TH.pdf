---
title: เปลี่ยนการตั้งค่าสำหรับรายงาน Power BI
description: เปลี่ยนการตั้งค่าสำหรับรายงานในบริการของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 10/14/2020
LocalizationGroup: Reports
ms.openlocfilehash: dbb173c65ecfc5d1ca464387ed43ae615cdcbca1
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96396187"
---
# <a name="change-settings-for-power-bi-reports"></a><span data-ttu-id="19f89-103">เปลี่ยนการตั้งค่าสำหรับรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="19f89-103">Change settings for Power BI reports</span></span>

<span data-ttu-id="19f89-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-desktop](../includes/yes-desktop.md)] [!INCLUDE [yes-service](../includes/yes-service.md)]</span><span class="sxs-lookup"><span data-stu-id="19f89-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-desktop](../includes/yes-desktop.md)] [!INCLUDE [yes-service](../includes/yes-service.md)]</span></span>

<span data-ttu-id="19f89-105">ด้วยการตั้งค่ารายงานใน Power BI Desktop และบริการของ Power BI คุณจะสามารถควบคุมวิธีที่ผู้อ่านรายงานโต้ตอบกับรายงานของคุณได้</span><span class="sxs-lookup"><span data-stu-id="19f89-105">With the report settings in Power BI Desktop and the Power BI service, you can control how report readers interact with your report.</span></span> <span data-ttu-id="19f89-106">ตัวอย่างเช่น คุณสามารถอนุญาตให้ผู้ใช้บันทึกตัวกรองสำหรับรายงาน ปรับแต่งการแสดงผลด้วยภาพในรายงาน หรือแสดงหน้ารายงานเป็นแท็บที่อยู่ด้านล่างของรายงานแทนที่จะอยู่ด้านข้าง</span><span class="sxs-lookup"><span data-stu-id="19f89-106">For example, you can allow them to save filters for the report, personalize the visuals in the report, or display the report pages as tabs across the bottom of the report instead of along the side.</span></span>

:::image type="content" source="media/power-bi-report-settings/service-report-settings-pane.png" alt-text="สกรีนช็อตของบานหน้าต่างการตั้งค่ารายงานในบริการของ Power BI":::

<span data-ttu-id="19f89-108">ซึ่งการอ่านบทความเหล่านี้ก่อนอาจเป็นประโยชน์:</span><span class="sxs-lookup"><span data-stu-id="19f89-108">It might be helpful to read these articles first:</span></span>

- <span data-ttu-id="19f89-109">[สร้างรายงานในบริการของ Power BI โดยการนำเข้าชุดข้อมูล](service-report-create-new.md) เพื่อทำความเข้าใจเกี่ยวกับประสบการณ์การสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="19f89-109">[Create a report in the Power BI service by importing a dataset](service-report-create-new.md), to understand the report creation experience.</span></span>
- <span data-ttu-id="19f89-110">[รายงานใน Power BI](../consumer/end-user-reports.md) เพื่อทำความเข้าใจเกี่ยวกับประสบการณ์ของผู้อ่านรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="19f89-110">[Reports in Power BI](../consumer/end-user-reports.md), to understand your report readers' experience.</span></span>

 <span data-ttu-id="19f89-111">มาเริ่มกันเลย!</span><span class="sxs-lookup"><span data-stu-id="19f89-111">Let's get started!</span></span>

## <a name="prerequisites"></a><span data-ttu-id="19f89-112">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="19f89-112">Prerequisites</span></span>

- <span data-ttu-id="19f89-113">สำหรับการสร้างรายงานโดยใช้ Power BI Desktop ให้ดู [มุมมองรายงานบนเดสก์ท็อป](desktop-report-view.md)</span><span class="sxs-lookup"><span data-stu-id="19f89-113">For creating reports using Power BI Desktop, see [Desktop report view](desktop-report-view.md).</span></span>
- <span data-ttu-id="19f89-114">[ลงทะเบียนสำหรับบริการของ Power BI](../fundamentals/service-self-service-signup-for-power-bi.md)</span><span class="sxs-lookup"><span data-stu-id="19f89-114">[Sign up for the Power BI service](../fundamentals/service-self-service-signup-for-power-bi.md).</span></span> 
- <span data-ttu-id="19f89-115">คุณจำเป็นต้องมีสิทธิ์ในการแก้ไขสำหรับรายงานในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="19f89-115">You need to have edit permission for the report in the Power BI service.</span></span> <span data-ttu-id="19f89-116">โปรดดู [บทบาทในพื้นที่ทำงานใหม่](../collaborate-share/service-new-workspaces.md#roles-in-the-new-workspaces) สำหรับรายละเอียดเกี่ยวกับสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="19f89-116">See [Roles in the new workspaces](../collaborate-share/service-new-workspaces.md#roles-in-the-new-workspaces) for details on permission.</span></span>
- <span data-ttu-id="19f89-117">ถ้าคุณยังไม่มีรายงานในบริการของ Power BI คุณสามารถ [ติดตั้งชุดเนื้อหาตัวอย่าง](sample-datasets.md#install-built-in-content-packs) ที่มีแดชบอร์ด รายงาน และชุดข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="19f89-117">If you don't already have a report in the Power BI service, you can [install a sample content pack](sample-datasets.md#install-built-in-content-packs) containing a dashboard, report, and dataset.</span></span>

## <a name="open-the-settings-pane-in-power-bi-desktop"></a><span data-ttu-id="19f89-118">เปิดบานหน้าต่างการตั้งค่าใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="19f89-118">Open the Settings pane in Power BI Desktop</span></span>

1. <span data-ttu-id="19f89-119">เลือกตัวเลือก **ไฟล์** >  **และตัวเลือก** > **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="19f89-119">Select **File** > **Options and settings** > **Options**.</span></span>
1. <span data-ttu-id="19f89-120">ภายใต้ **ไฟล์ปัจจุบัน** เลือก **การตั้งค่ารายงาน**</span><span class="sxs-lookup"><span data-stu-id="19f89-120">Under **Current file**, select **Report settings**.</span></span>

    :::image type="content" source="media/power-bi-report-settings/desktop-report-settings-pane.png" alt-text="สกรีนช็อตของบานหน้าต่างการตั้งค่ารายงานใน Power BI Desktop":::

    <span data-ttu-id="19f89-122">ส่วนที่เหลือของบทความนี้จะเรียกใช้การตั้งค่ารายงานเฉพาะบางรายการ</span><span class="sxs-lookup"><span data-stu-id="19f89-122">The rest of this article calls out some of the specific report settings.</span></span>

## <a name="open-the-settings-pane-in-the-power-bi-service"></a><span data-ttu-id="19f89-123">เปิดบานหน้าต่างการตั้งค่าในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="19f89-123">Open the Settings pane in the Power BI service</span></span>

1. <span data-ttu-id="19f89-124">ในมุมมองการอ่านรายงาน เลือก **ไฟล์** > **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="19f89-124">In report Reading view, select **File** > **Settings**.</span></span>

    :::image type="content" source="media/power-bi-report-settings/service-report-file-settings.png" alt-text="สกรีนช็อตของเมนูไฟล์ไปยังการตั้งค่า":::

1. <span data-ttu-id="19f89-126">ในบานหน้าต่าง **การตั้งค่า** คุณจะเห็นจำนวนการสลับที่คุณสามารถตั้งค่าได้เพียงสำหรับรายงานนี้</span><span class="sxs-lookup"><span data-stu-id="19f89-126">In the **Settings** pane, you see a number of toggles you can set, just for this report.</span></span> <span data-ttu-id="19f89-127">ส่วนที่เหลือของบทความนี้จะเรียกใช้การตั้งค่ารายงานเฉพาะบางรายการ</span><span class="sxs-lookup"><span data-stu-id="19f89-127">The rest of this article calls out some of them.</span></span>

## <a name="set-featured-content"></a><span data-ttu-id="19f89-128">กำหนดเนื้อหาเด่น</span><span class="sxs-lookup"><span data-stu-id="19f89-128">Set featured content</span></span>

<span data-ttu-id="19f89-129">คุณสามารถแสดงแดชบอร์ด รายงาน และแอปเพื่อให้ปรากฏในส่วนที่แนะนำของหน้าแรกของ Power BI ของเพื่อนร่วมงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="19f89-129">You can feature dashboards, reports, and apps so they appear in the Featured section of your colleagues' Power BI Home page.</span></span> <span data-ttu-id="19f89-130">อ่านเพิ่มเติมเกี่ยวกับ [วิธีการกำหนดคุณลักษณะของเนื้อหา](../collaborate-share/service-featured-content.md)</span><span class="sxs-lookup"><span data-stu-id="19f89-130">Read more about [how to feature content](../collaborate-share/service-featured-content.md).</span></span>

## <a name="set-the-pages-pane"></a><span data-ttu-id="19f89-131">ตั้งค่าบานหน้าต่างของหน้า</span><span class="sxs-lookup"><span data-stu-id="19f89-131">Set the Pages pane</span></span>

<span data-ttu-id="19f89-132">ในขณะนี้ คุณสามารถเปลี่ยนการตั้งค่าบานหน้าต่างของหน้าในบริการของ Power BI เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="19f89-132">Currently you can only change the Pages pane setting in the Power BI service.</span></span> <span data-ttu-id="19f89-133">เมื่อคุณสลับเปิด **บานหน้าต่างของหน้า** ผู้อ่านรายงานจะมองเห็นแท็บหน้ารายงานตามด้านล่างของรายงานในมุมมองการอ่านแทนที่จะอยู่ด้านข้าง</span><span class="sxs-lookup"><span data-stu-id="19f89-133">When you toggle **Pages pane** on, report readers see the report page tabs along the bottom of the report in Reading view, instead of along the side.</span></span> <span data-ttu-id="19f89-134">ในมุมมองแก้ไข แท็บหน้ารายงานจะมีอยู่แล้วตามด้านล่างของรายงาน</span><span class="sxs-lookup"><span data-stu-id="19f89-134">In Edit view, the report page tabs are already along the bottom of the report.</span></span>

:::image type="content" source="media/power-bi-report-settings/report-settings-pages-pane.png" alt-text="สกรีนช็อตของการตั้งค่าบานหน้าต่างของหน้า":::

## <a name="control-filters"></a><span data-ttu-id="19f89-136">ควบคุมตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="19f89-136">Control filters</span></span>

<span data-ttu-id="19f89-137">บานหน้าต่าง **การตั้งค่า** รายงานมีการตั้งค่าสามรายการ สำหรับควบคุมการโต้ตอบของผู้อ่านที่ทำกับตัวกรองในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="19f89-137">The report **Settings** pane has three settings for controlling reader interactions with the filters on your report.</span></span> <span data-ttu-id="19f89-138">ลิงก์ต่อไปนี้ไปที่บทความ [่ตัวกรองการออกแบบในรายงาน Power BI](power-bi-report-filter.md) สำหรับรายละเอียดเกี่ยวกับการตั้งค่าแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="19f89-138">The following links go to the [Design filters in Power BI reports](power-bi-report-filter.md) article for details on each setting.</span></span>

- <span data-ttu-id="19f89-139">**ตัวกรองแบบถาวร** อนุญาตให้ผู้อ่าน [บันทึกตัวกรองบนรายงาน](power-bi-report-filter.md#allow-saving-filters)</span><span class="sxs-lookup"><span data-stu-id="19f89-139">**Persistent filters** allow readers to [save filters on the report](power-bi-report-filter.md#allow-saving-filters).</span></span>
- <span data-ttu-id="19f89-140">**ประสบการณ์การกรอง** มีการตั้งค่าเพิ่มเติมสองรายการ:</span><span class="sxs-lookup"><span data-stu-id="19f89-140">**Filtering experience** has two more settings:</span></span>
    
    <span data-ttu-id="19f89-141">อนุญาตให้ผู้อ่านรายงาน [เปลี่ยนชนิดตัวกรอง](power-bi-report-filter.md#restrict-changes-to-filter-type)</span><span class="sxs-lookup"><span data-stu-id="19f89-141">Allow report readers to [change filter types](power-bi-report-filter.md#restrict-changes-to-filter-type).</span></span>

    <span data-ttu-id="19f89-142">เปิดใช้งาน [ค้นหาในบานหน้าต่างตัวกรอง](power-bi-report-filter.md#filters-pane-search)</span><span class="sxs-lookup"><span data-stu-id="19f89-142">Enable [search in the filter pane](power-bi-report-filter.md#filters-pane-search).</span></span>

## <a name="export-data"></a><span data-ttu-id="19f89-143">ส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="19f89-143">Export data</span></span>

<span data-ttu-id="19f89-144">ตามค่าเริ่มต้น [ผู้อ่านรายงานสามารถส่งออกข้อมูลสรุปหรือข้อมูลเบื้องต้น](../consumer/end-user-export.md) จากการแสดงผลด้วยภาพในรายงานของคุณได้</span><span class="sxs-lookup"><span data-stu-id="19f89-144">By default, [report readers can export summarized or underlying data](../consumer/end-user-export.md) from visuals in your report.</span></span> <span data-ttu-id="19f89-145">ด้วย **ส่งออกข้อมูล** คุณสามารถอนุญาตให้ผู้ใช้สามารถส่งออกข้อมูลสรุปได้เท่านั้น หรือไม่ส่งออกข้อมูลใด ๆ เลยจากรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="19f89-145">With **Export data**, you can allow them to export only summarized data, or to export no data at all from your report.</span></span>

## <a name="personalize-visuals"></a><span data-ttu-id="19f89-146">ปรับแต่งการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="19f89-146">Personalize visuals</span></span>

<span data-ttu-id="19f89-147">อนุญาตให้ผู้อ่านของคุณเปลี่ยนและปรับแต่งการแสดงผลด้วยภาพในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="19f89-147">Allow your readers to change and personalize the visuals in your report.</span></span> <span data-ttu-id="19f89-148">อ่านเพิ่มเติมเกี่ยวกับ [อนุญาตให้ผู้อ่านรายงานปรับแต่งการแสดงผลด้วยภาพ](power-bi-personalize-visuals.md)</span><span class="sxs-lookup"><span data-stu-id="19f89-148">Read more about [letting report readers personalize visuals](power-bi-personalize-visuals.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="19f89-149">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="19f89-149">Next steps</span></span>

* [<span data-ttu-id="19f89-150">กำหนดคุณลักษณะของเนื้อหาบนหน้าแรกของบุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="19f89-150">Feature content on others' Home pages</span></span>](../collaborate-share/service-featured-content.md)
* [<span data-ttu-id="19f89-151">อนุญาตให้ผู้อ่านรายงานปรับแต่งการแสดงผลด้วยภาพในรายงาน</span><span class="sxs-lookup"><span data-stu-id="19f89-151">Let report readers personalize visuals in a report</span></span>](power-bi-personalize-visuals.md)
* <span data-ttu-id="19f89-152">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="19f89-152">More questions?</span></span> [<span data-ttu-id="19f89-153">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="19f89-153">Try the Power BI Community</span></span>](https://community.powerbi.com/)
