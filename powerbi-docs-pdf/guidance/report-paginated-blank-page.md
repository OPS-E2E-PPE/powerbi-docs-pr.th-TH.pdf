---
title: หลีกเลี่ยงหน้าเปล่าเมื่อพิมพ์รายงานที่ระบุเลขหน้า
description: คำแนะนำสำหรับการออกแบบรายงานแบบแบ่งหน้า คือ หลีกเลี่ยงหน้าเปล่าเมื่อทำการพิมพ์
author: peter-myers
ms.author: v-pemyer
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 01/14/2020
ms.openlocfilehash: 0fa886973105bdb4bc8a35f145168c1775ca12cb
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418474"
---
# <a name="avoid-blank-pages-when-printing-paginated-reports"></a><span data-ttu-id="f1605-103">หลีกเลี่ยงหน้าเปล่าเมื่อพิมพ์รายงานที่ระบุเลขหน้า</span><span class="sxs-lookup"><span data-stu-id="f1605-103">Avoid blank pages when printing paginated reports</span></span>

<span data-ttu-id="f1605-104">บทความนี้มุ่งเป้ามาที่คุณในฐานะผู้เขียนรายงานที่ออกแบบ [รายงานแบบแบ่งหน้า](../paginated-reports/paginated-reports-report-builder-power-bi.md) ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="f1605-104">This article targets you as a report author designing Power BI [paginated reports](../paginated-reports/paginated-reports-report-builder-power-bi.md).</span></span> <span data-ttu-id="f1605-105">โดยมีคำแนะนำเพื่อช่วยให้คุณหลีกเลี่ยงหน้าเปล่าเมื่อรายงานของคุณถูกส่งออกไปในรูปแบบตัวแสดงผลแบบบังคับ เช่น PDF หรือ Microsoft Word หรือเมื่อพิมพ์รายงาน</span><span class="sxs-lookup"><span data-stu-id="f1605-105">It provides recommendations to help you avoid blank pages when your report is exported to a hard-page format—like PDF or Microsoft Word—or, is printed.</span></span>

## <a name="page-setup"></a><span data-ttu-id="f1605-106">การตั้งค่าหน้ากระดาษ</span><span class="sxs-lookup"><span data-stu-id="f1605-106">Page setup</span></span>

<span data-ttu-id="f1605-107">คุณสมบัติขนาดของหน้ารายงานจะกำหนดการวางแนวหน้ากระดาษ มิติ และระยะขอบ</span><span class="sxs-lookup"><span data-stu-id="f1605-107">Report page size properties determine the page orientation, dimensions, and margins.</span></span> <span data-ttu-id="f1605-108">เข้าถึงคุณสมบัติของรายงานเหล่านี้โดย:</span><span class="sxs-lookup"><span data-stu-id="f1605-108">Access these report properties by:</span></span>

- <span data-ttu-id="f1605-109">ใช้ **หน้าคุณสมบัติ** ของรายงาน: คลิกขวาที่พื้นที่สีเทาเข้มภายนอกพื้นที่ทำงานของรายงาน จากนั้นเลือก _คุณสมบัติรายงาน_</span><span class="sxs-lookup"><span data-stu-id="f1605-109">Using the report **Property Page**: Right-click the dark gray area outside the report canvas, and then select _Report Properties_.</span></span>
- <span data-ttu-id="f1605-110">ใช้ [**คุณสมบัติ** ในบานหน้าต่าง](../paginated-reports/paginated-reports-report-design-view.md#4-properties-pane) คลิกขวาที่พื้นที่สีเทาเข้มภายนอกพื้นที่ทำงานของรายงาน เพื่อเลือกวัตถุของรายงาน</span><span class="sxs-lookup"><span data-stu-id="f1605-110">Using the [**Properties** pane](../paginated-reports/paginated-reports-report-design-view.md#4-properties-pane): Click the dark gray area outside the report canvas to select the report object.</span></span> <span data-ttu-id="f1605-111">ตรวจสอบให้แน่ใจว่ามีการเปิดบานหน้าต่าง **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="f1605-111">Ensure the **Properties** pane is open.</span></span>

<span data-ttu-id="f1605-112">หน้า **การตั้งค่าหน้ากระดาษ** ของ **หน้าคุณสมบัติ** ของรายงาน  มีอินเทอร์เฟซที่ง่ายต่อการดูและอัปเดตคุณสมบัติการตั้งค่าหน้ากระดาษ</span><span class="sxs-lookup"><span data-stu-id="f1605-112">The **Page Setup** page of the report **Property Page** provides a friendly interface to view and update the page setup properties.</span></span>

![รูปภาพแสดงหน้าต่างคุณสมบัติของรายงาน โดยเน้นในส่วนหน้าการตั้งค่าหน้ากระดาษ](media/report-paginated-blank-page/report-page-setup-properties.png)

<span data-ttu-id="f1605-114">ตรวจสอบให้แน่ใจว่าคุณสมบัติขนาดหน้าทั้งหมดได้รับการกำหนดค่าอย่างถูกต้อง:</span><span class="sxs-lookup"><span data-stu-id="f1605-114">Ensure all page size properties are correctly configured:</span></span>

|<span data-ttu-id="f1605-115">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="f1605-115">Property</span></span>|<span data-ttu-id="f1605-116">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="f1605-116">Recommendation</span></span>|
|---------|---------|
|<span data-ttu-id="f1605-117">หน่วยของหน้ากระดาษ</span><span class="sxs-lookup"><span data-stu-id="f1605-117">Page units</span></span>|<span data-ttu-id="f1605-118">เลือกหน่วยที่เกี่ยวข้อง — นิ้วหรือเซนติเมตร</span><span class="sxs-lookup"><span data-stu-id="f1605-118">Select the relevant units—inches or centimeters.</span></span>|
|<span data-ttu-id="f1605-119">การวางแนว</span><span class="sxs-lookup"><span data-stu-id="f1605-119">Orientation</span></span>|<span data-ttu-id="f1605-120">เลือกตัวเลือกที่ถูกต้อง — แนวตั้งหรือแนวนอน</span><span class="sxs-lookup"><span data-stu-id="f1605-120">Select the correct option—portrait or landscape.</span></span>|
|<span data-ttu-id="f1605-121">ขนาดกระดาษ</span><span class="sxs-lookup"><span data-stu-id="f1605-121">Paper size</span></span>|<span data-ttu-id="f1605-122">เลือกขนาดกระดาษหรือกำหนดค่าความกว้างและความยาวแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="f1605-122">Select a paper size, or assign custom width and height values.</span></span>|
|<span data-ttu-id="f1605-123">ระยะขอบ</span><span class="sxs-lookup"><span data-stu-id="f1605-123">Margins</span></span>|<span data-ttu-id="f1605-124">ตั้งค่าที่เหมาะสมสำหรับระยะขอบด้านซ้าย ด้านขวา ด้านบน และด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="f1605-124">Set appropriate values for the left, right, top, and bottom margins.</span></span>|
|||

## <a name="report-body-width"></a><span data-ttu-id="f1605-125">ความกว้างเนื้อหารายงาน</span><span class="sxs-lookup"><span data-stu-id="f1605-125">Report body width</span></span>

<span data-ttu-id="f1605-126">คุณสมบัติขนาดหน้าจะกำหนดพื้นที่ว่างที่พร้อมใช้งานสำหรับวัตถุของรายงาน</span><span class="sxs-lookup"><span data-stu-id="f1605-126">The page size properties determine the available space available for report objects.</span></span> <span data-ttu-id="f1605-127">วัตถุของรายงานเป็นได้ทั้งขอบเขตข้อมูล การจัดรูปแบบข้อมูล หรือรายการของรายงานอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f1605-127">Report objects can be data regions, data visualizations, or other report items.</span></span>

<span data-ttu-id="f1605-128">สาเหตุทั่วไปที่ทำให้มีการแสดงหน้าเปล่าออกมา คือ เนื้อหารายงาน มีความกว้าง _เกินกว่าพื้นที่หน้าที่พร้อมใช้งาน_</span><span class="sxs-lookup"><span data-stu-id="f1605-128">A common reason why blank pages are output, is the report body width _exceeds the available page space_.</span></span>

<span data-ttu-id="f1605-129">คุณสามารถดูและตั้งค่าความกว้างของเนื้อหารายงานได้เท่านั้นโดยใช้บานหน้าต่าง **คุณสมบัติ** </span><span class="sxs-lookup"><span data-stu-id="f1605-129">You can only view and set the report body width using the **Properties** pane.</span></span> <span data-ttu-id="f1605-130">อันดับแรก ให้คลิกที่ใดก็ได้ในพื้นที่ว่างของเนื้อหารายงาน</span><span class="sxs-lookup"><span data-stu-id="f1605-130">First, click anywhere in an empty area of the report body.</span></span>

![รูปแสดงบานหน้าต่างคุณสมบัติการ โดยเน้นคุณสมบัติความกว้างของเนื้อหารายงาน](media/report-paginated-blank-page/report-body-properties-width.png)

<span data-ttu-id="f1605-132">ตรวจสอบให้แน่ใจว่าค่าความกว้างไม่เกินความกว้างของหน้าที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f1605-132">Ensure the width value doesn't exceed available page width.</span></span> <span data-ttu-id="f1605-133">รับคำแนะนำจากสูตรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f1605-133">Be guided by the following formula:</span></span>

```Report body width <= Report page width - (Left margin + Right margin)```

> [!NOTE]
> <span data-ttu-id="f1605-134">ไม่สามารถลดความกว้างของเนื้อหารายงานได้เมื่อมีวัตถุของรายงานอยู่ในพื้นที่ที่คุณต้องการนำออก</span><span class="sxs-lookup"><span data-stu-id="f1605-134">It's not possible to reduce the report body width when there are report objects already in the space you want to remove.</span></span> <span data-ttu-id="f1605-135">อันดับแรก คุณต้องจัดตำแหน่งหรือปรับขนาดวัตถุเหล่านั้นใหม่ ก่อนที่จะลดความกว้าง</span><span class="sxs-lookup"><span data-stu-id="f1605-135">You must first reposition or resize them before reducing the width.</span></span>
>
> <span data-ttu-id="f1605-136">นอกจากนี้ ความกว้างของเนื้อหารายงานจะเพิ่มโดยอัตโนมัติเมื่อคุณเพิ่มวัตถุใหม่ หรือปรับขนาดหรือจัดตำแหน่งวัตถุที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="f1605-136">Also, the report body width can increase automatically when you add new objects, or resize or reposition existing objects.</span></span> <span data-ttu-id="f1605-137">ผู้ออกแบบรายงานจะขยายเนื้อหาเพื่อรองรับตำแหน่งและขนาดของวัตถุที่มีอยู่เสมอ</span><span class="sxs-lookup"><span data-stu-id="f1605-137">The report designer always widens the body to accommodate the position and size of its contained objects.</span></span>

## <a name="report-body-height"></a><span data-ttu-id="f1605-138">ความยาวเนื้อหารายงาน</span><span class="sxs-lookup"><span data-stu-id="f1605-138">Report body height</span></span>

<span data-ttu-id="f1605-139">อีกเหตุผลหนึ่งที่เป็นสาเหตุให้มีการแสดงหน้าเปล่าออกมา คือ มีพื้นที่ส่วนเกินในเนื้อหารายงานถัดจากจากวัตถุสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="f1605-139">Another reason why a blank page is output, is there's excess space in the report body, after the last object.</span></span>

<span data-ttu-id="f1605-140">เราขอแนะนำให้คุณลดความยาวของเนื้อหาเพื่อนำพื้นที่ว่างส่วนท้ายออกเสมอ</span><span class="sxs-lookup"><span data-stu-id="f1605-140">We recommend you always reduce the height of the body to remove any trailing space.</span></span>

![รูปภาพแสดงการออกแบบรายงาน](media/report-paginated-blank-page/report-body-remove-trailing-space.png)

## <a name="page-break-options"></a><span data-ttu-id="f1605-143">ตัวเลือกการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="f1605-143">Page break options</span></span>

<span data-ttu-id="f1605-144">แต่ละขอบเขตข้อมูลและการจัดรูปแบบข้อมูลมีตัวเลือกการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="f1605-144">Each data region and data visualization has page break options.</span></span> <span data-ttu-id="f1605-145">คุณสามารถเข้าถึงตัวเลือกเหล่านี้ได้ในหน้าคุณสมบัติ หรือในบานหน้าต่าง **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="f1605-145">You can access these options in its property page, or in the **Properties** pane.</span></span>

<span data-ttu-id="f1605-146">ตรวจสอบให้แน่ใจว่า **เพิ่มตัวแบ่งหน้าหลังจาก** คุณสมบัติ ไม่ได้เปิดใช้งานอยู่โดยไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="f1605-146">Ensure the **Add a page break after** property isn't unnecessarily enabled.</span></span>

![รูปภาพแสดงหน้าต่างคุณสมบัติ tablix](media/report-paginated-blank-page/data-region-page-break-option-after.png)

## <a name="consume-container-whitespace"></a><span data-ttu-id="f1605-149">ใช้พื้นที่ว่างในที่บรรจุ</span><span class="sxs-lookup"><span data-stu-id="f1605-149">Consume Container Whitespace</span></span>

<span data-ttu-id="f1605-150">ถ้าพบปัญหาการแสดงหน้าเปล่าอยู่ คุณยังสามารถลองปิดใช้งานคุณสมบัติรายงาน **ใช้พื้นที่ว่างในที่บรรจุ** ได้</span><span class="sxs-lookup"><span data-stu-id="f1605-150">If the blank page issue persists, you can also try disabling the report **ConsumeContainerWhitespace** property.</span></span> <span data-ttu-id="f1605-151">สามารถตั้งค่าได้ในบานหน้าต่าง **คุณสมบัติ** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f1605-151">It can only be set in the **Properties** pane.</span></span>

![รูปภาพแสดงบานหน้าต่างคุณสมบัติการ โดยเน้นคุณสมบัติ ใช้พื้นที่ว่างในที่บรรจุ](media/report-paginated-blank-page/report-properties-consumecontainerwhitespace.png)

<span data-ttu-id="f1605-153">ตามค่าเริ่มต้นนั้น มีการเปิดใช้งานไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="f1605-153">By default, it's enabled.</span></span> <span data-ttu-id="f1605-154">ซึ่งจะเป็นแนะนำว่าพื้นที่ว่างขั้นต่ำในที่บรรจุ เช่น เนื้อหารายงานหรือสี่เหลี่ยมผืนผ้า ควรมีการใช้งานหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f1605-154">It directs whether minimum whitespace in containers, such as the report body or a rectangle, should be consumed.</span></span> <span data-ttu-id="f1605-155">เฉพาะพื้นที่ว่างทางด้านขวาและด้านล่างของเนื้อหาเท่านั้นที่จะได้รับผล</span><span class="sxs-lookup"><span data-stu-id="f1605-155">Only whitespace to the right of, and below, the contents is affected.</span></span>

## <a name="printer-paper-size"></a><span data-ttu-id="f1605-156">ขนาดกระดาษของเครื่องพิมพ์</span><span class="sxs-lookup"><span data-stu-id="f1605-156">Printer paper size</span></span>

<span data-ttu-id="f1605-157">สุดท้าย ถ้าคุณกำลังพิมพ์รายงานลงในกระดาษ ตรวจสอบให้แน่ใจว่าเครื่องพิมพ์มีกระดาษที่ถูกต้องบรรจุอยู่</span><span class="sxs-lookup"><span data-stu-id="f1605-157">Lastly, if you're printing the report to paper, ensure the printer has the correct paper loaded.</span></span> <span data-ttu-id="f1605-158">ขนาดกระดาษจริงควรสอดคล้องกับ[ขนาดของรายงาน](#page-setup)</span><span class="sxs-lookup"><span data-stu-id="f1605-158">The physical paper size should correspond to the [report paper size](#page-setup).</span></span>

## <a name="next-steps"></a><span data-ttu-id="f1605-159">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="f1605-159">Next steps</span></span>

<span data-ttu-id="f1605-160">สำหรับข้อมูลเพิ่มเติมที่เกี่ยวข้องกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f1605-160">For more information related to this article, check out the following resources:</span></span>

- [<span data-ttu-id="f1605-161">รายงานแบบแบ่งหน้าใน Power BI Premium คืออะไร</span><span class="sxs-lookup"><span data-stu-id="f1605-161">What are paginated reports in Power BI Premium?</span></span>](../paginated-reports/paginated-reports-report-builder-power-bi.md)
- [<span data-ttu-id="f1605-162">การแบ่งหน้าในรายงานแบบแบ่งหน้าของ Power BI</span><span class="sxs-lookup"><span data-stu-id="f1605-162">Pagination in Power BI paginated reports</span></span>](../paginated-reports/paginated-reports-pagination.md)
- <span data-ttu-id="f1605-163">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f1605-163">Questions?</span></span> [<span data-ttu-id="f1605-164">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="f1605-164">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="f1605-165">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="f1605-165">Suggestions?</span></span> [<span data-ttu-id="f1605-166">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="f1605-166">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com)
