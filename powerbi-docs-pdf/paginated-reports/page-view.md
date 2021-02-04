---
title: ตั้งค่ามุมมองรายงานสำหรับรายงานที่มีการแบ่งหน้า - Power BI
description: ในบทความนี้ คุณจะได้เรียนรู้เกี่ยวกับมุมมองรายงานต่าง ๆ ที่ใช้ได้สำหรับรายงานที่มีการแบ่งหน้าในบริการของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: report-builder
ms.topic: how-to
ms.date: 05/14/2020
ms.openlocfilehash: 6c44c0252e954c9a3b78aaa620c93a9ea97f47e2
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418267"
---
# <a name="set-report-views-for-paginated-reports-in-the-power-bi-service"></a><span data-ttu-id="1355a-103">ตั้งค่ามุมมองรายงานสำหรับรายงานที่มีการแบ่งหน้าในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="1355a-103">Set report views for paginated reports in the Power BI service</span></span>

<span data-ttu-id="1355a-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span><span class="sxs-lookup"><span data-stu-id="1355a-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span></span> 

<span data-ttu-id="1355a-105">เมื่อคุณแสดงรายงานที่มีการแบ่งหน้าในบริการของ Power BI มุมมองเริ่มต้นคือมุมมองที่ยึดตาม HTML และโต้ตอบได้</span><span class="sxs-lookup"><span data-stu-id="1355a-105">When you render a paginated report in the Power BI service, the default view is HTML based and interactive.</span></span> <span data-ttu-id="1355a-106">มุมมองรายงานอื่นสำหรับรูปแบบหน้าแบบคงที่เช่น PDF คือตัวเลือกมุมมองหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="1355a-106">Another report view, for fixed page formats like PDF, is the new Page View option.</span></span>

<span data-ttu-id="1355a-107">**มุมมองแบบโต้ตอบเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="1355a-107">**Default interactive view**</span></span>

![มุมมองเริ่มต้น](media/page-view/power-bi-paginated-default-view.png)

<span data-ttu-id="1355a-109">**มุมมองหน้าเพจ**</span><span class="sxs-lookup"><span data-stu-id="1355a-109">**Page View**</span></span>

![มุมมองหน้าเพจ](media/page-view/power-bi-paginated-page-view.png)

<span data-ttu-id="1355a-111">ในมุมมองหน้าเพจ รายงานที่แสดงจะมีลักษณะแตกต่างกันเมื่อเปรียบเทียบกับมุมมองเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="1355a-111">In Page View, the rendered report looks different compared to the default view.</span></span> <span data-ttu-id="1355a-112">คุณสมบัติและแนวคิดในรายงานที่มีการแบ่งหน้าจะใช้กับหน้าเพจแบบคงที่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1355a-112">Some properties and concepts in paginated reports only apply to fixed pages.</span></span> <span data-ttu-id="1355a-113">มุมมองจะคล้ายกับเมื่อพิมพ์หรือส่งออกรายงาน</span><span class="sxs-lookup"><span data-stu-id="1355a-113">The view is similar to when the report is printed or exported.</span></span> <span data-ttu-id="1355a-114">คุณยังสามารถเปลี่ยนองค์ประกอบบางอย่างเช่น ค่าพารามิเตอร์ แต่ไม่มีคุณลักษณะแบบโต้ตอบอื่น ๆ เช่น การเรียงลำดับและการสลับคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="1355a-114">You can still change some elements, like parameter values, but it doesn't have other interactive features such as column sorting and toggles.</span></span>

<span data-ttu-id="1355a-115">มุมมองหน้าเพจจะสนับสนุนคุณลักษณะทั้งหมด การสนับสนุนตัวแสดง PDF ของเบราว์เซอร์ เช่น ย่อ ขยาย และพอดีกับหน้า</span><span class="sxs-lookup"><span data-stu-id="1355a-115">Page View supports all the features the browser's PDF Viewer supports, such as Zoom in, Zoom out, and Fit to page.</span></span>

## <a name="switch-to-page-view"></a><span data-ttu-id="1355a-116">สลับไปยังมุมมองหน้าเพจ</span><span class="sxs-lookup"><span data-stu-id="1355a-116">Switch to Page View</span></span>

<span data-ttu-id="1355a-117">เมื่อคุณเปิดรายงานที่มีการแบ่งหน้า จะแสดงในมุมมองแบบโต้ตอบตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="1355a-117">When you open a paginated report, it renders in interactive view by default.</span></span> <span data-ttu-id="1355a-118">ถ้ารายงานมีพารามิเตอร์ เลือกพารามิเตอร์แล้วดูรายงาน</span><span class="sxs-lookup"><span data-stu-id="1355a-118">If the report has parameters, select parameters, then view the report.</span></span>

1. <span data-ttu-id="1355a-119">เลือก **มุมมอง** บนแถบเครื่องมือ > **มุมมองหน้าเพจ**</span><span class="sxs-lookup"><span data-stu-id="1355a-119">Select **View** on the toolbar > **Page View**.</span></span>

    ![สลับไปยังมุมมองหน้าเพจ](media/page-view/power-bi-paginated-page-view-dropdown.png)

2. <span data-ttu-id="1355a-121">คุณสามารถเปลี่ยนการตั้งค่าของมุมมองหน้าเพจได้โดยการเลือก **การตั้งค่าหน้า** ในเมนู **มุมมอง** บนแถบเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="1355a-121">You can change the settings of the page view by selecting the **Page Settings** in **View** menu on the toolbar.</span></span> 

    ![เลือกการตั้งค่าหน้า](media/page-view/power-bi-paginated-page-settings-dropdown.png)
    
    <span data-ttu-id="1355a-123">กล่องโต้ตอบ **การตั้งค่าหน้า** มีตัวเลือกในการตั้งค่า **ขนาดหน้า**  และ **การวางแนว** สำหรับมุมมองหน้าเพจ</span><span class="sxs-lookup"><span data-stu-id="1355a-123">The **Page Settings** dialog box has options to set **Page Size** and **Orientation** for the Page View.</span></span> <span data-ttu-id="1355a-124">หลังจากที่คุณนำการตั้งค่าหน้าไปใช้แล้ว จะใช้ตัวเลือกเดียวกันเมื่อคุณพิมพ์หน้าในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="1355a-124">After you apply page settings, the same options apply when you print the page later.</span></span>
   
    ![กล่องโต้ตอบการตั้งค่าหน้า](media/page-view/power-bi-paginated-page-settings-dialog.png)

3. <span data-ttu-id="1355a-126">เมื่อต้องการสลับกลับไปยังมุมมองแบบโต้ตอบ ให้เลือก **ค่าเริ่มต้น** ในกล่องแบบหล่นลง **มุมมอง**</span><span class="sxs-lookup"><span data-stu-id="1355a-126">To switch back to the interactive view, select **Default** in the **View** dropdown box.</span></span>

## <a name="browser-support"></a><span data-ttu-id="1355a-127">การสนับสนุนเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="1355a-127">Browser support</span></span>

<span data-ttu-id="1355a-128">มุมมองหน้าเพจได้รับการสนับสนุนในเบราว์เซอร์ Google Chrome และ Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1355a-128">Page View is supported in Google Chrome and Microsoft Edge browsers.</span></span> <span data-ttu-id="1355a-129">ตรวจสอบให้แน่ใจว่ามีการเปิดใช้งานการดูไฟล์ PDF ในเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="1355a-129">Make sure that viewing PDFs in the browser is enabled.</span></span> <span data-ttu-id="1355a-130">ซึ่งเป็นการตั้งค่าเริ่มต้นสำหรับเบราว์เซอร์เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="1355a-130">It's the default setting for these browsers.</span></span>

<span data-ttu-id="1355a-131">มุมมองหน้าเพจไม่ได้รับการสนับสนุนใน Internet Explorer และ Safari ดังนั้นตัวเลือกจึงถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="1355a-131">Page View isn't supported in Internet Explorer and Safari, so the option is disabled.</span></span> <span data-ttu-id="1355a-132">นอกจากนี้ยังไม่ได้รับการสนับสนุนในเบราว์เซอร์บนอุปกรณ์เคลื่อนที่ หรือในแอปสำหรับอุปกรณ์เคลื่อนที่ Power BI ดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="1355a-132">It also isn't supported in browsers on mobile devices, or in the native Power BI mobile apps.</span></span>  


## <a name="next-steps"></a><span data-ttu-id="1355a-133">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="1355a-133">Next steps</span></span>

- [<span data-ttu-id="1355a-134">ดูรายงานแบบแบ่งหน้าในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="1355a-134">View a paginated report in the Power BI service</span></span>](../consumer/paginated-reports-view-power-bi-service.md)
- [<span data-ttu-id="1355a-135">รายงานแบบแบ่งหน้าใน Power BI Premium คืออะไร</span><span class="sxs-lookup"><span data-stu-id="1355a-135">What are paginated reports in Power BI Premium?</span></span>](paginated-reports-report-builder-power-bi.md)
