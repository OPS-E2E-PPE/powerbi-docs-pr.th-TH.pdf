---
title: วิธีการใช้ป้ายชื่อระดับความลับใน Power BI
description: เรียนรู้วิธีการใช้ป้ายชื่อระดับความลับใน Power BI
author: paulinbar
ms.author: painbar
ms.service: powerbi
ms.subservice: powerbi-eim
ms.topic: how-to
ms.date: 12/09/2020
LocalizationGroup: Data from files
ms.openlocfilehash: 09188b3b03fd5bfb720b98045ee9d895d337d677
ms.sourcegitcommit: a5e98bc86915f7bea6a0ab5df282683840e63d2c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/07/2021
ms.locfileid: "97969178"
---
# <a name="how-to-apply-sensitivity-labels-in-power-bi"></a><span data-ttu-id="3f5c1-103">วิธีการใช้ป้ายชื่อระดับความลับใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3f5c1-103">How to apply sensitivity labels in Power BI</span></span>

<span data-ttu-id="3f5c1-104">ป้ายชื่อระดับความลับของ Microsoft Information Protection บนรายงาน แดชบอร์ด ชุดข้อมูล กระแสข้อมูลและไฟล์ .pbix ของคุณสามารถปกป้องเนื้อหาที่ละเอียดอ่อนของคุณจากการเข้าถึงข้อมูลโดยไม่ได้รับอนุญาตและการรั่วไหล</span><span class="sxs-lookup"><span data-stu-id="3f5c1-104">Microsoft Information Protection sensitivity labels on your reports, dashboards, datasets, dataflows, and .pbix files can guard your sensitive content against unauthorized data access and leakage.</span></span> <span data-ttu-id="3f5c1-105">การติดป้ายข้อมูลด้วยป้ายชื่อระดับความลับอย่างถูกต้องช่วยให้มั่นใจได้ว่าเฉพาะผู้ที่ได้รับอนุญาตเท่านั้นที่สามารถเข้าถึงข้อมูลของคุณได้</span><span class="sxs-lookup"><span data-stu-id="3f5c1-105">Labeling your data correctly with sensitivity labels ensures that only authorized people can access your data.</span></span> <span data-ttu-id="3f5c1-106">บทความนี้แสดงวิธีการใช้ป้ายชื่อระดับความลับของข้อมูลในบริการ Power BI และใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3f5c1-106">This article shows you how to apply sensitivity labels in the Power BI service and in Power BI Desktop.</span></span>

<span data-ttu-id="3f5c1-107">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับป้ายชื่อระดับความลับใน Power BI โปรดดู [ป้ายชื่อระดับความลับใน Power BI](service-security-sensitivity-label-overview.md)</span><span class="sxs-lookup"><span data-stu-id="3f5c1-107">For more information about sensitivity labels in Power BI, see [Sensitivity labels in Power BI](service-security-sensitivity-label-overview.md).</span></span>

## <a name="apply-sensitivity-labels-in-the-power-bi-service"></a><span data-ttu-id="3f5c1-108">ใช้ป้ายชื่อระดับความลับของข้อมูลในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="3f5c1-108">Apply sensitivity labels in the Power BI service</span></span>

<span data-ttu-id="3f5c1-109">ในบริการ Power BI คุณจะสามารถใช้ป้ายชื่อระดับความลับของข้อมูลที่อยู่ในรายงาน แดชบอร์ด ชุดข้อมูล และกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3f5c1-109">In the Power BI service, you can apply sensitivity labels to reports, dashboards, datasets, and dataflows.</span></span>

<span data-ttu-id="3f5c1-110">เพื่อให้สามารถใช้ป้ายชื่อระดับความลับของข้อมูลในบริการ Power BI:</span><span class="sxs-lookup"><span data-stu-id="3f5c1-110">To be able to apply sensitivity labels in the Power BI service:</span></span>
* <span data-ttu-id="3f5c1-111">คุณต้องมี [สิทธิการใช้งาน Power BI Pro](./service-admin-purchasing-power-bi-pro.md) และแก้ไขการอนุญาตที่คุณต้องการติดป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="3f5c1-111">You must have a [Power BI Pro license](./service-admin-purchasing-power-bi-pro.md) and edit permissions on the content you wish to label.</span></span>
* <span data-ttu-id="3f5c1-112">ป้ายชื่อระดับความลับของข้อมูลต้องเปิดใช้งานสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="3f5c1-112">Sensitivity labels must be enabled for your organization.</span></span> <span data-ttu-id="3f5c1-113">ติดต่อผู้ดูแลระบบ Power BI ของคุณถ้าคุณไม่แน่ใจเกี่ยวกับเรื่องนี้</span><span class="sxs-lookup"><span data-stu-id="3f5c1-113">Contact your Power BI admin if you aren’t sure about this.</span></span>
* <span data-ttu-id="3f5c1-114">คุณต้องเป็นสมาชิกของกลุ่มความปลอดภัยที่มีสิทธิ์ใช้ป้ายชื่อระดับความลับของข้อมูล ตามที่อธิบายไว้ใน [การเปิดใช้งานป้ายชื่อระดับความลับใน Power BI](./service-security-enable-data-sensitivity-labels.md)</span><span class="sxs-lookup"><span data-stu-id="3f5c1-114">You must belong to a security group that has permissions to apply sensitivity labels, as described in [Enable sensitivity labels in Power BI](./service-security-enable-data-sensitivity-labels.md).</span></span>
* <span data-ttu-id="3f5c1-115">ต้องเป็นไปตาม [ใบอนุญาตใช้งานและข้อกำหนดอื่น ๆ](./service-security-enable-data-sensitivity-labels.md#licensing-and-requirements) ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3f5c1-115">All [licensing and other requirements](./service-security-enable-data-sensitivity-labels.md#licensing-and-requirements) must have been met.</span></span>

<span data-ttu-id="3f5c1-116">เมื่อเปิดใช้งานการป้องกันข้อมูลในผู้เช่าของคุณ ป้ายชื่อระดับความลับจะปรากฏในคอลัมน์ความลับในมุมมองรายการของแดชบอร์ด รายงาน ชุดข้อมูล และกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3f5c1-116">When data protection is enabled on your tenant, sensitivity labels appear in the sensitivity column in the list view of dashboards, reports, datasets, and dataflows.</span></span>

![เปิดใช้งานป้ายชื่อระดับความลับ](media/service-security-apply-data-sensitivity-labels/apply-data-sensitivity-labels-01.png)

<span data-ttu-id="3f5c1-118">**เมื่อต้องการนำไปใช้หรือเปลี่ยนป้ายชื่อระดับความลับบนรายงานหรือแดชบอร์ด**</span><span class="sxs-lookup"><span data-stu-id="3f5c1-118">**To apply or change a sensitivity label on a report or dashboard**</span></span>
1. <span data-ttu-id="3f5c1-119">คลิก **ตัวเลือกเพิ่มเติม (... )**</span><span class="sxs-lookup"><span data-stu-id="3f5c1-119">Click **More options (...)**.</span></span>
1. <span data-ttu-id="3f5c1-120">เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="3f5c1-120">Select **Settings**.</span></span>
1. <span data-ttu-id="3f5c1-121">ในบานหน้าต่างด้านการตั้งค่า ให้เลือกป้ายชื่อระดับความลับที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="3f5c1-121">In the settings side pane choose the appropriate sensitivity label.</span></span>
1. <span data-ttu-id="3f5c1-122">บันทึกการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="3f5c1-122">Save the settings.</span></span>

<span data-ttu-id="3f5c1-123">รูปภาพต่อไปนี้อธิบายขั้นตอนเหล่านี้ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="3f5c1-123">The following image illustrates these steps on a report</span></span>

![ตั้งค่าป้ายชื่อระดับความลับ](media/service-security-apply-data-sensitivity-labels/apply-data-sensitivity-labels-02.png)

<span data-ttu-id="3f5c1-125">**เมื่อต้องการนำไปใช้หรือเปลี่ยนป้ายชื่อระดับความลับบนชุดข้อมูลหรือกระแสข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="3f5c1-125">**To apply or change a sensitivity label on a dataset or dataflow**</span></span>

1. <span data-ttu-id="3f5c1-126">คลิก **ตัวเลือกเพิ่มเติม (... )**</span><span class="sxs-lookup"><span data-stu-id="3f5c1-126">Click **More options (...)**.</span></span>
1. <span data-ttu-id="3f5c1-127">เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="3f5c1-127">Select **Settings**.</span></span>
1. <span data-ttu-id="3f5c1-128">เลือกแท็บชุดข้อมูลหรือกระแสข้อมูล แล้วแต่ว่าสิ่งใดจะเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3f5c1-128">Select the datasets or dataflows tab, whichever is relevant.</span></span>
1. <span data-ttu-id="3f5c1-129">ขยายส่วนป้ายชื่อระดับความลับและเลือกป้ายชื่อระดับความลับที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="3f5c1-129">Expand the sensitivity labels section and choose the appropriate sensitivity label.</span></span>
1. <span data-ttu-id="3f5c1-130">ใช้การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="3f5c1-130">Apply the settings.</span></span>

<span data-ttu-id="3f5c1-131">สองรูปต่อไปนี้แสดงขั้นตอนเหล่านี้ในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3f5c1-131">The following two images illustrate these steps on a dataset.</span></span>

<span data-ttu-id="3f5c1-132">เลือก **ตัวเลือกเพิ่มเติม (...)** จากนั้น **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="3f5c1-132">Choose **More options (...)** and then **Settings**.</span></span>

![เปิดการตั้งค่าชุดข้อมูล](media/service-security-apply-data-sensitivity-labels/apply-data-sensitivity-labels-05.png)

<span data-ttu-id="3f5c1-134">บนแท็บชุดข้อมูลการตั้งค่า ให้เปิดส่วนป้ายชื่อระดับความลับแล้วเลือกป้ายชื่อระดับความลับที่ต้องการแล้วคลิก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="3f5c1-134">On the settings datasets tab, open the sensitivity label section, choose the desired sensitivity label, and click **Apply**.</span></span>

![เลือกป้ายชื่อระดับความลับ](media/service-security-apply-data-sensitivity-labels/apply-data-sensitivity-labels-06.png)

## <a name="apply-sensitivity-labels-in-power-bi-desktop-preview"></a><span data-ttu-id="3f5c1-136">ใใช้ป้ายชื่อระดับความลับของข้อมูลใน Power BI Desktop (ดูตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="3f5c1-136">Apply sensitivity labels in Power BI Desktop (preview)</span></span>

<span data-ttu-id="3f5c1-137">ในการใช้ป้ายชื่อระดับความลับใน Power BI Desktop:</span><span class="sxs-lookup"><span data-stu-id="3f5c1-137">To use sensitivity labels in Power BI Desktop:</span></span>
* <span data-ttu-id="3f5c1-138">คุณต้องมี [สิทธิ์การใช้งาน Power BI Pro](./service-admin-purchasing-power-bi-pro.md)</span><span class="sxs-lookup"><span data-stu-id="3f5c1-138">You must have a [Power BI Pro license](./service-admin-purchasing-power-bi-pro.md).</span></span>
* <span data-ttu-id="3f5c1-139">ป้ายชื่อระดับความลับของข้อมูลต้องเปิดใช้งานสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="3f5c1-139">Sensitivity labels must be enabled for your organization.</span></span> <span data-ttu-id="3f5c1-140">ติดต่อผู้ดูแลระบบ Power BI ของคุณหากคุณไม่แน่ใจเกี่ยวกับเรื่องนี้</span><span class="sxs-lookup"><span data-stu-id="3f5c1-140">Contact your Power BI admin if you aren't sure about this.</span></span>
* <span data-ttu-id="3f5c1-141">คุณต้องเป็นสมาชิกของกลุ่มความปลอดภัยที่มีสิทธิ์ใช้ป้ายชื่อระดับความลับของข้อมูล ตามที่อธิบายไว้ใน [การเปิดใช้งานป้ายชื่อระดับความลับใน Power BI](./service-security-enable-data-sensitivity-labels.md)</span><span class="sxs-lookup"><span data-stu-id="3f5c1-141">You must belong to a security group that has permissions to apply sensitivity labels, as described in [Enable sensitivity labels in Power BI](./service-security-enable-data-sensitivity-labels.md).</span></span>
* <span data-ttu-id="3f5c1-142">ต้องเป็นไปตาม [ใบอนุญาตใช้งานและข้อกำหนดอื่น ๆ](./service-security-enable-data-sensitivity-labels.md#licensing-and-requirements) ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3f5c1-142">All [licensing and other requirements](./service-security-enable-data-sensitivity-labels.md#licensing-and-requirements) must have been met.</span></span>
* <span data-ttu-id="3f5c1-143">ต้องเปิดสวิตช์คุณลักษณะการแสดงตัวอย่างการป้องกันข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3f5c1-143">The information protection preview feature switch in Power BI Desktop must be turned on.</span></span> <span data-ttu-id="3f5c1-144">ถ้าคุณเห็นปุ่มระดับความลับในแท็บหน้าแรก คุณลักษณะการแสดงตัวอย่างจะเปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="3f5c1-144">If you see the sensitivity button on the home tab, the preview feature is on.</span></span> <span data-ttu-id="3f5c1-145">หากคุณไม่เห็นปุ่มให้ไปที่ **ไฟล์> ตัวเลือกและการตั้งค่า> ตัวเลือก> คุณสมบัติการแสดงตัวอย่าง** และทำเครื่องหมายที่ช่องถัดจาก **การปกป้องข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="3f5c1-145">If you don't see the button, go to **File > Options and settings > Options > Preview features**, and check the box next to **Information protection**.</span></span>

    ![สกรีนช็อตของหน้าคุณลักษณะการแสดงตัวอย่างเดสก์ท็อป](media/service-security-apply-data-sensitivity-labels/desktop-preview-features-page.png)

    >[!Important]
    ><span data-ttu-id="3f5c1-147">หลังจากเปิดใช้งานคุณลักษณะการแสดงตัวอย่างการปกป้องข้อมูลแล้ว คุณต้องรีสตาร์ทเดสก์ท็อปเพื่อเริ่มต้นด้วยป้ายชื่อระดับความลับ</span><span class="sxs-lookup"><span data-stu-id="3f5c1-147">After turning on the information protection preview feature, you must restart Desktop in order to start using sensitivity labels.</span></span>
    >
    ><span data-ttu-id="3f5c1-148">หากเดสก์ท็อปขัดข้องเมื่อคุณรีสตาร์ท อาจเป็นเพราะเครื่องของคุณไม่มีเวอร์ชันไลบรารีรันไทม์ Visual C ++ แบบแจกจ่ายต่อได้ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="3f5c1-148">If Desktop crashes when you restart it, it may be because your machine lacks the required Visual C++ redistributable runtime library version.</span></span> <span data-ttu-id="3f5c1-149">หากคุณพบการขัดข้องดังกล่าว ให้ไปที่ [หน้าดาวน์โหลด Microsoft Visual C ++ 2015 Redistributable Update 3](https://www.microsoft.com/download/details.aspx?id=53587) เพื่อดูคำแนะนำเกี่ยวกับวิธีดาวน์โหลดและติดตั้งอัปเดต</span><span class="sxs-lookup"><span data-stu-id="3f5c1-149">If you experience such a crash, visit the [Microsoft Visual C++ 2015 Redistributable Update 3 download page](https://www.microsoft.com/download/details.aspx?id=53587) for instructions about how to download and install the update.</span></span> <span data-ttu-id="3f5c1-150">หลังจากติดตั้งอัปเดตแล้ว ให้ลองเปิดใช้งานเดสก์ท็อปอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="3f5c1-150">After installing the update, try launching Desktop again.</span></span>

    <span data-ttu-id="3f5c1-151">หากคุณไม่เห็นตัวเลือกการแสดงตัวอย่างการปกป้องข้อมูล คุณลักษณะการแสดงตัวอย่างการปกป้องข้อมูลอาจถูกบล็อกสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="3f5c1-151">If you don't see the Information protection preview option, the information protection preview feature may be blocked for your organization.</span></span> <span data-ttu-id="3f5c1-152">ในกรณีนี้โปรดติดต่อผู้ดูแลระบบ Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3f5c1-152">In this case contact your Power BI administrator.</span></span>

* <span data-ttu-id="3f5c1-153">คุณต้องลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="3f5c1-153">You must be signed in.</span></span>

<span data-ttu-id="3f5c1-154">ในการใช้ป้ายชื่อระดับความลับกับไฟล์ที่คุณกำลังทำงานอยู่ให้คลิกปุ่มระดับความลับในแท็บหน้าแรกและเลือกป้ายกำกับที่ต้องการจากเมนูที่ปรากฏ</span><span class="sxs-lookup"><span data-stu-id="3f5c1-154">To apply a sensitivity label on the file you're working on, click the sensitivity button in the home tab and choose the desired label from the menu that appears.</span></span>

![สกรีนช็อตของเมนูป้ายชื่อระดับความลับในเดสก์ท็อป](media/service-security-apply-data-sensitivity-labels/sensitivity-label-menu-desktop.png)

>[!NOTE]
> <span data-ttu-id="3f5c1-156">หากคุณเปิดใช้งานคุณลักษณะป้ายชื่อระดับความลับในคุณลักษณะการแสดงตัวอย่าง แต่ยังไม่เห็นปุ่มระดับความลับอาจบ่งชี้ว่าคุณไม่มีใบอนุญาตให้ใช้งานที่เหมาะสมหรือคุณไม่ได้อยู่ในกลุ่มความปลอดภัยที่มีสิทธิ์ในการใช้ป้ายชื่อระดับความลับตามที่อธิบายไว้ใน [เปิดใช้งานป้ายชื่อระดับความลับใน Power BI](./service-security-enable-data-sensitivity-labels.md)</span><span class="sxs-lookup"><span data-stu-id="3f5c1-156">If you've turned on the sensitivity labels feature in Preview features but still don't see the sensitivity button, it may indicate that you don't have an appropriate license or that you do not belong to security group that has permissions to apply sensitivity labels, as described in [Enable sensitivity labels in Power BI](./service-security-enable-data-sensitivity-labels.md).</span></span>

<span data-ttu-id="3f5c1-157">หลังจากที่คุณใช้ป้ายชื่อแล้วป้ายชื่อจะปรากฏในแถบสถานะ</span><span class="sxs-lookup"><span data-stu-id="3f5c1-157">After you've applied the label, it will be visible in the status bar.</span></span>

![สกรีนช็อตของเมนูป้ายชื่อระดับความลับในแถบสถานะของเดสก์ท็อป](media/service-security-apply-data-sensitivity-labels/sensitivity-label-in-desktop-status-bar.png)

### <a name="sensitivity-labels-when-uploading-or-downloading-pbix-files-tofrom-the-service"></a><span data-ttu-id="3f5c1-159">ป้ายชื่อระดับความลับเมื่ออัปโหลดหรือดาวน์โหลดไฟล์ .pbix ไปยัง/จากบริการ</span><span class="sxs-lookup"><span data-stu-id="3f5c1-159">Sensitivity labels when uploading or downloading .pbix files to/from the service</span></span>
* <span data-ttu-id="3f5c1-160">เมื่อคุณเผยแพร่ไฟล์. pbix ไปยังบริการ Power BI จากเดสก์ท็อปหรือเมื่อคุณอัปโหลดไฟล์. pbix ไปยังบริการ Power BI โดยตรงโดยใช้ **รับข้อมูล** ป้ายกำกับชื่อของไฟล์. pbix จะถูกนำไปใช้กับทั้งรายงานและชุดข้อมูลที่สร้างขึ้นในบริการ</span><span class="sxs-lookup"><span data-stu-id="3f5c1-160">When you publish a .pbix file to the Power BI service from Desktop, or when you upload a .pbix file to the Power BI service directly using **Get data**, the .pbix file's label gets applied to both the report and the dataset that are created in the service.</span></span> <span data-ttu-id="3f5c1-161">หากไฟล์. pbix ที่คุณกำลังเผยแพร่หรืออัปโหลดแทนที่แอสเซทที่มีอยู่ (เช่น แอสเซทที่มีชื่อเดียวกับไฟล์. pbix) ป้ายกำกับชื่อของไฟล์. pbix จะเขียนทับป้ายกำกับในแอสเซทเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="3f5c1-161">If the .pbix file you’re publishing or uploading replaces existing assets (i.e. assets that have the same name as the .pbix file) the .pbix file's label will overwrite any labels on those assets.</span></span>
* <span data-ttu-id="3f5c1-162">เมื่อใช้ "ดาวน์โหลดเป็น. pbix" ในบริการของ Power BI หากรายงานและชุดข้อมูลที่ดาวน์โหลดทั้งคู่มีป้ายกำกับและป้ายกำกับเหล่านั้นต่างกัน ป้ายกำกับที่จะใช้กับไฟล์. pbix จะมีข้อจำกัด มากกว่าของทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="3f5c1-162">When using "Download to .pbix" in the Power BI service, if the report and dataset being downloaded both have labels, and those labels are different, the label that will be applied to the .pbix file is the more restrictive of the two.</span></span>

## <a name="remove-sensitivity-labels"></a><span data-ttu-id="3f5c1-163">เอาป้ายชื่อระดับความลับออก</span><span class="sxs-lookup"><span data-stu-id="3f5c1-163">Remove sensitivity labels</span></span>

### <a name="service"></a><span data-ttu-id="3f5c1-164">บริการ</span><span class="sxs-lookup"><span data-stu-id="3f5c1-164">Service</span></span>
<span data-ttu-id="3f5c1-165">หากต้องการลบป้ายชื่อระดับความลับออกจากรายงาน แดชบอร์ด ชุดข้อมูลหรือกระแสข้อมูลให้ทำตาม [ขั้นตอนเดียวกับที่ใช้สำหรับการใช้ป้ายชื่อในบริการ Power BI](#apply-sensitivity-labels-in-the-power-bi-service) แต่ให้เลือก **(ไม่มี)** เมื่อได้รับแจ้งให้จัดประเภทระดับความลับของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3f5c1-165">To remove a sensitivity label from a report, dashboard, dataset, or dataflow, follow the [same procedure used for applying labels in the Power BI service](#apply-sensitivity-labels-in-the-power-bi-service), but choose **(None)** when prompted to classify the sensitivity of the data.</span></span>

### <a name="desktop"></a><span data-ttu-id="3f5c1-166">เดสก์ท็อป</span><span class="sxs-lookup"><span data-stu-id="3f5c1-166">Desktop</span></span>
<span data-ttu-id="3f5c1-167">การลบป้ายชื่อระดับความลับออกจากไฟล์. pbix หลังจากที่บันทึกด้วยป้ายชื่อนั้นยังไม่ได้รับการสนับสนุนในเดสก์ท็อป</span><span class="sxs-lookup"><span data-stu-id="3f5c1-167">Removing the sensitivity label from a .pbix file after it has been saved with the label is currently not supported in Desktop.</span></span> <span data-ttu-id="3f5c1-168">ในกรณีดังกล่าวขอแนะนำให้เผยแพร่ไฟล์ไปยังบริการ Power BI แล้วจากนั้นในบริการเพื่อลบป้ายชื่อออกจากรายงานและชุดข้อมูลที่ตามมา</span><span class="sxs-lookup"><span data-stu-id="3f5c1-168">In such cases it is recommended to publish the file to the Power BI service and then there in the service to remove the label from the subsequent report and dataset.</span></span>

## <a name="considerations-and-limitations"></a><span data-ttu-id="3f5c1-169">ข้อควรพิจารณาและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="3f5c1-169">Considerations and limitations</span></span>

<span data-ttu-id="3f5c1-170">ดู [ป้ายชื่อระดับความลับใน Power BI](service-security-sensitivity-label-overview.md#limitations) สำหรับรายการขีดจำกัดของป้ายชื่อระดับความลับใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3f5c1-170">See [Sensitivity labels in Power BI](service-security-sensitivity-label-overview.md#limitations) for the list of sensitivity label limitations in Power BI.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3f5c1-171">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3f5c1-171">Next steps</span></span>

<span data-ttu-id="3f5c1-172">บทความนี้อธิบายวิธีการใช้งานป้ายชื่อระดับความลับใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3f5c1-172">This article described how to apply sensitivity labels in Power BI.</span></span> <span data-ttu-id="3f5c1-173">บทความต่อไปนี้แสดงรายละเอียดเพิ่มเติมเกี่ยวกับการป้องกันข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3f5c1-173">The following articles provide more details about data protection in Power BI.</span></span> 

* [<span data-ttu-id="3f5c1-174">ภาพรวมของป้ายชื่อระดับความลับใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3f5c1-174">Overview of sensitivity labels in Power BI</span></span>](./service-security-sensitivity-label-overview.md)
* [<span data-ttu-id="3f5c1-175">เปิดใช้งานป้ายชื่อระดับความลับใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3f5c1-175">Enable sensitivity labels in Power BI</span></span>](./service-security-enable-data-sensitivity-labels.md)
* [<span data-ttu-id="3f5c1-176">ใช้ตัวควบคุม Microsoft Cloud App Security ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="3f5c1-176">Using Microsoft Cloud App Security controls in Power BI</span></span>](./service-security-using-microsoft-cloud-app-security-controls.md)