---
title: ขยายภาพด้วยคำแนะนำเครื่องมือของหน้ารายงาน
description: คำแนะนำสำหรับการทำงานกับคำแนะนำเครื่องมือของหน้ารายงาน
author: peter-myers
ms.author: v-pemyer
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 11/24/2019
ms.openlocfilehash: 919fc9cfa2bbdb55317fed0879347c929a723ce8
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96419072"
---
# <a name="extend-visuals-with-report-page-tooltips"></a><span data-ttu-id="beaa6-103">ขยายภาพด้วยคำแนะนำเครื่องมือของหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="beaa6-103">Extend visuals with report page tooltips</span></span>

<span data-ttu-id="beaa6-104">บทความนี้กำหนดเป้าหมายคุณในฐานะผู้สร้างรายงานที่ออกแบบรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="beaa6-104">This article targets you as a report author designing Power BI reports.</span></span> <span data-ttu-id="beaa6-105">ซึ่งมีข้อเสนอแนะและคำแนะนำเมื่อสร้าง [คำแนะนำเครื่องมือของหน้ารายงาน](../create-reports/desktop-tooltips.md)</span><span class="sxs-lookup"><span data-stu-id="beaa6-105">It provides suggestions and recommendations when creating [report page tooltips](../create-reports/desktop-tooltips.md).</span></span>

## <a name="suggestions"></a><span data-ttu-id="beaa6-106">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="beaa6-106">Suggestions</span></span>

<span data-ttu-id="beaa6-107">คำแนะนำเครื่องมือของหน้ารายงานสามารถยกระดับประสบการณ์สำหรับผู้ใช้รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="beaa6-107">Report page tooltips can enhance the experience for your report users.</span></span> <span data-ttu-id="beaa6-108">คำแนะนำเครื่องมือของหน้าช่วยให้ผู้ใช้รายงานของคุณได้รับข้อมูลเชิงลึกจากวิชวลได้อย่างรวดเร็วและมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="beaa6-108">Page tooltips allow your report users to quickly and efficiently gain deeper insights from a visual.</span></span> <span data-ttu-id="beaa6-109">ซึ่งสามารถเชื่อมโยงกับอ็อบเจ็กต์รายงานที่แตกต่างกันได้:</span><span class="sxs-lookup"><span data-stu-id="beaa6-109">They can be associated with different report objects:</span></span>

- <span data-ttu-id="beaa6-110">**วิชวล:** คุณสามารถกำหนดค่าว่าวิชวลใดที่จะแสดงคำแนะนำเครื่องมือบนหน้าของคุณ บนพื้นฐานของวิชวลต่อวิชวล</span><span class="sxs-lookup"><span data-stu-id="beaa6-110">**Visuals:** On a visual-by-visual basis, you can configure which visuals will reveal your page tooltip.</span></span> <span data-ttu-id="beaa6-111">สำหรับแต่ละวิชวล เป็นไปได้ที่วิชวลจะไม่แสดงคำแนะนำเครื่องมือ ตั้งค่าเริ่มต้นไปยังคำแนะนำเครื่องมือวิชวล (ที่กำหนดค่าในบานหน้าต่างเขตข้อมูลวิชวล) หรือใช้คำแนะนำเครื่องมือของหน้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="beaa6-111">Per visual, it's possible to have the visual reveal no tooltip, default to the visual tooltips (configured in the visual fields pane), or use a specific page tooltip.</span></span>
- <span data-ttu-id="beaa6-112">**ส่วนหัวของวิชวล:** คุณสามารถกำหนดค่าวิชวลเฉพาะเพื่อแสดงคำแนะนำเครื่องมือของหน้าได้</span><span class="sxs-lookup"><span data-stu-id="beaa6-112">**Visual headers:** You can configure specific visuals to display a page tooltip.</span></span> <span data-ttu-id="beaa6-113">ผู้ใช้รายงานของคุณสามารถแสดงคำแนะนำเครื่องมือของหน้าได้เมื่อเลื่อนเคอร์เซอร์ไปยังไอคอนส่วนหัวของวิชวล เพื่อช่วยให้ผู้ใช้ของคุณทราบข้อมูลเกี่ยวกับไอคอนนี้</span><span class="sxs-lookup"><span data-stu-id="beaa6-113">Your report users can reveal the page tooltip when they hover their cursor over the visual header icon—be sure to educate your users about this icon.</span></span>

> [!NOTE]
> <span data-ttu-id="beaa6-114">วิชวลรายงานสามารถแสดงคำแนะนำเครื่องมือของหน้าได้เฉพาะเมื่อตัวกรองหน้าคำแนะนำเครื่องมือเข้ากันได้กับการออกแบบของวิชวล</span><span class="sxs-lookup"><span data-stu-id="beaa6-114">A report visual can only reveal a page tooltip when tooltip page filters are compatible with the visual's design.</span></span> <span data-ttu-id="beaa6-115">ตัวอย่างเช่น วิชวลที่จัดกลุ่มตาม _ผลิตภัณฑ์_ เข้ากันได้กับหน้าคำแนะนำเครื่องมือที่กรองด้วย _ผลิตภัณฑ์_</span><span class="sxs-lookup"><span data-stu-id="beaa6-115">For example, a visual that groups by _product_ is compatible with a tooltip page that filters by _product_.</span></span>
>
> <span data-ttu-id="beaa6-116">คำแนะนำเครื่องมือของหน้าไม่สนับสนุนการโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="beaa6-116">Page tooltips don't support interactivity.</span></span> <span data-ttu-id="beaa6-117">หากคุณต้องการให้ผู้ใช้โต้ตอบกับรายงานของคุณ ให้สร้าง [หน้าการดูรายละเอียดแบบเจาะลึก](../create-reports/desktop-drillthrough.md) แทน</span><span class="sxs-lookup"><span data-stu-id="beaa6-117">If you want your report users to interact, create a [drillthrough page](../create-reports/desktop-drillthrough.md) instead.</span></span>
>
> <span data-ttu-id="beaa6-118">วิชวล Power BI ไม่สนับสนุนคำแนะนำเครื่องมือของหน้า</span><span class="sxs-lookup"><span data-stu-id="beaa6-118">Power BI visuals do not support page tooltips.</span></span>

<span data-ttu-id="beaa6-119">ต่อไปนี้คือสถานการณ์จำลองการออกแบบที่แนะนำบางส่วน:</span><span class="sxs-lookup"><span data-stu-id="beaa6-119">Here are some suggested design scenarios:</span></span>

- [<span data-ttu-id="beaa6-120">มุมมองที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="beaa6-120">Different perspective</span></span>](#different-perspective)
- [<span data-ttu-id="beaa6-121">เพิ่มรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="beaa6-121">Add detail</span></span>](#add-detail)
- [<span data-ttu-id="beaa6-122">เพิ่มความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="beaa6-122">Add help</span></span>](#add-help)

### <a name="different-perspective"></a><span data-ttu-id="beaa6-123">มุมมองที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="beaa6-123">Different perspective</span></span>

<span data-ttu-id="beaa6-124">คำแนะนำเครื่องมือของหน้าสามารถแสดงวิชวลข้อมูลเดียวกันกับวิชวลต้นฉบับได้</span><span class="sxs-lookup"><span data-stu-id="beaa6-124">A page tooltip can visualize the same data as the source visual.</span></span> <span data-ttu-id="beaa6-125">ซึ่งทำได้โดยใช้วิชวลและกลุ่ม pivot เดียวกัน หรือโดยการใช้วิชวลชนิดที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="beaa6-125">It's done by using the same visual and pivoting groups, or by using different visual types.</span></span> <span data-ttu-id="beaa6-126">คำแนะนำเครื่องมือของหน้ายังสามารถใช้ตัวกรองที่แตกต่างจากตัวกรองที่ใช้กับวิชวลต้นฉบับได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="beaa6-126">Page tooltips can also apply different filters than those filters applied to the source visual.</span></span>

<span data-ttu-id="beaa6-127">ตัวอย่างต่อไปนี้แสดงสิ่งที่เกิดขึ้นเมื่อผู้ใช้รายงานเลื่อนเคอร์เซอร์ไปที่ค่า **EnabledUsers**</span><span class="sxs-lookup"><span data-stu-id="beaa6-127">The following example shows what happens when the report user hovers their cursor over the **EnabledUsers** value.</span></span> <span data-ttu-id="beaa6-128">บริบทตัวกรองสำหรับค่าคือ Yammer ในเดือนพฤศจิกายน 2018</span><span class="sxs-lookup"><span data-stu-id="beaa6-128">The filter context for the value is Yammer in November 2018.</span></span>

![วิชวลเมทริกซ์แสดงเส้นตารางของค่าที่จัดกลุ่มตามปีและเดือนในแถว](media/report-page-tooltips/suggestion-different-perspective.png)

<span data-ttu-id="beaa6-132">คำแนะนำเครื่องมือของหน้าแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="beaa6-132">A page tooltip is revealed.</span></span> <span data-ttu-id="beaa6-133">ซึ่งแสดงวิชวลข้อมูลที่แตกต่าง (แผนภูมิเส้นและแผนภูมิคอลัมน์แบบคลัสเตอร์) และใช้ตัวกรองเวลาที่ตัดกัน</span><span class="sxs-lookup"><span data-stu-id="beaa6-133">It presents a different data visual (line and clustered column chart) and applies a contrasting time filter.</span></span> <span data-ttu-id="beaa6-134">โปรดสังเกตว่าบริบทตัวกรองสำหรับจุดข้อมูลคือพฤศจิกายน 2018</span><span class="sxs-lookup"><span data-stu-id="beaa6-134">Notice that the filter context for the data point is November 2018.</span></span> <span data-ttu-id="beaa6-135">แต่คำแนะนำเครื่องมือของหน้ายังแสดงแนวโน้มมากกว่า _ของเดือนตลอดทั้งปี_</span><span class="sxs-lookup"><span data-stu-id="beaa6-135">Yet the page tooltip displays trend over _a full year of months_.</span></span>

### <a name="add-detail"></a><span data-ttu-id="beaa6-136">เพิ่มรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="beaa6-136">Add detail</span></span>

<span data-ttu-id="beaa6-137">คำแนะนำเครื่องมือของหน้าสามารถแสดงรายละเอียดเพิ่มเติมและเพิ่มบริบทได้</span><span class="sxs-lookup"><span data-stu-id="beaa6-137">A page tooltip can display additional details and add context.</span></span>

<span data-ttu-id="beaa6-138">ตัวอย่างต่อไปนี้แสดงสิ่งที่เกิดขึ้นเมื่อผู้ใช้รายงานเลื่อนเคอร์เซอร์ไปที่ค่า **Average of Violation Points** สำหรับรหัสไปรษณีย์ 98022</span><span class="sxs-lookup"><span data-stu-id="beaa6-138">The following example shows what happens when the report user hovers their cursor over the **Average of Violation Points** value, for zip code 98022.</span></span>

![วิชวลตารางแสดงเส้นตารางของค่าและตารางประกอบด้วยสามคอลัมน์](media/report-page-tooltips/suggestion-add-details.png)

<span data-ttu-id="beaa6-141">คำแนะนำเครื่องมือของหน้าแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="beaa6-141">A page tooltip is revealed.</span></span> <span data-ttu-id="beaa6-142">ซึ่งแสดงแอตทริบิวต์และสถิติเฉพาะสำหรับรหัสไปรษณีย์ 98022</span><span class="sxs-lookup"><span data-stu-id="beaa6-142">It presents specific attributes and statistics for zip code 98022.</span></span>

### <a name="add-help"></a><span data-ttu-id="beaa6-143">เพิ่มความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="beaa6-143">Add help</span></span>

<span data-ttu-id="beaa6-144">คุณสามารถกำหนดค่าส่วนหัวของวิชวลให้แสดงคำแนะนำเครื่องมือของหน้ากับส่วนหัวของวิชวลได้</span><span class="sxs-lookup"><span data-stu-id="beaa6-144">Visual headers can be configured to reveal page tooltips to visual headers.</span></span> <span data-ttu-id="beaa6-145">คุณสามารถเพิ่มเอกสารความช่วยเหลือให้กับคำแนะนำเครื่องมือของหน้าโดยใช้กล่องข้อความที่จัดรูปแบบ Rich Text Format</span><span class="sxs-lookup"><span data-stu-id="beaa6-145">You can add help documentation to a page tooltip by using richly formatted text boxes.</span></span> <span data-ttu-id="beaa6-146">นอกจากนี้ยังเป็นไปได้ที่จะเพิ่มรูปภาพและรูปร่าง</span><span class="sxs-lookup"><span data-stu-id="beaa6-146">It's also possible to add images and shapes.</span></span>

<span data-ttu-id="beaa6-147">น่าสนใจว่าคุณยังสามารถแสดงปุ่ม รูปภาพ กล่องข้อความ และรูปร่างไปยังคำแนะนำเครื่องมือของหน้าในส่วนหัวของวิชวลได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="beaa6-147">Interestingly, buttons, images, text boxes, and shapes can also reveal a visual header page tooltip.</span></span>

<span data-ttu-id="beaa6-148">ตัวอย่างต่อไปนี้แสดงสิ่งที่เกิดขึ้นเมื่อผู้ใช้รายงานเลื่อนเคอร์เซอร์ไปที่ [ไอคอนส่วนหัวของการแสดงผลด้วยภาพ](../create-reports/desktop-visual-elements-for-reports.md)</span><span class="sxs-lookup"><span data-stu-id="beaa6-148">The following example shows what happens when the report user hovers their cursor over the [visual header icon](../create-reports/desktop-visual-elements-for-reports.md).</span></span>

![ผู้ใช้รายงานวางเคอร์เซอร์ไว้เหนือไอคอนส่วนหัวของวิชวล (ไอคอนเครื่องหมายคำถาม)](media/report-page-tooltips/suggestion-add-help.png)

<span data-ttu-id="beaa6-151">คำแนะนำเครื่องมือของหน้าแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="beaa6-151">A page tooltip is revealed.</span></span> <span data-ttu-id="beaa6-152">จะแสดงรูปแบบ Rich Text Format ในกล่องข้อความสี่กล่อง และรูปร่าง (บรรทัด)</span><span class="sxs-lookup"><span data-stu-id="beaa6-152">It presents rich formatted text in four text boxes, and a shape (line).</span></span> <span data-ttu-id="beaa6-153">คำแนะนำเครื่องมือของหน้าจะถ่ายทอดความช่วยเหลือโดยการอธิบายตัวย่อแต่ละตัวที่แสดงในการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="beaa6-153">The page tooltip conveys help by describing each acronym displayed in the visual.</span></span>

## <a name="recommendations"></a><span data-ttu-id="beaa6-154">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="beaa6-154">Recommendations</span></span>

<span data-ttu-id="beaa6-155">ในขณะออกแบบรายงาน เราขอแนะนำแนวทางปฏิบัติดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="beaa6-155">At report design time, we recommend the following practices:</span></span>

- <span data-ttu-id="beaa6-156">**ขนาดหน้า:** กำหนดค่าคำแนะนำเครื่องมือของหน้าของคุณให้เป็นขนาดเล็ก</span><span class="sxs-lookup"><span data-stu-id="beaa6-156">**Page size:** Configure your page tooltip to be small.</span></span> <span data-ttu-id="beaa6-157">คุณสามารถใช้ตัวเลือก **คำแนะนำเครื่องมือ** ที่มีอยู่แล้วภายใน (กว้าง 320 พิกเซล, 240 พิกเซลสูง)</span><span class="sxs-lookup"><span data-stu-id="beaa6-157">You can use the built-in **Tooltip** option (320 pixels wide, 240 pixels high).</span></span> <span data-ttu-id="beaa6-158">หรือคุณสามารถตั้งค่าขนาดมิติแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="beaa6-158">Or, you can set custom dimensions.</span></span> <span data-ttu-id="beaa6-159">ระวังอย่าใช้ขนาดหน้ากระดาษที่ใหญ่เกินไปซึ่งสามารถบดบังวิชวลบนหน้าต้นทางได้</span><span class="sxs-lookup"><span data-stu-id="beaa6-159">Take care not to use a page size that's too large—it can obscure the visuals on the source page.</span></span>
- <span data-ttu-id="beaa6-160">**มุมมองหน้า:** ในตัวออกแบบรายงาน ให้ตั้งค่ามุมมองหน้าเป็น **ขนาดจริง** (มุมมองหน้าค่าเริ่มต้นคือ **พอดีกับหน้า**)</span><span class="sxs-lookup"><span data-stu-id="beaa6-160">**Page view:** In report designer, set the page view to **Actual Size** (page view defaults to **Fit to Page**).</span></span> <span data-ttu-id="beaa6-161">ด้วยวิธีนี้ คุณสามารถดูขนาดจริงของคำแนะนำเครื่องมือของหน้าในตามที่คุณออกแบบได้</span><span class="sxs-lookup"><span data-stu-id="beaa6-161">This way, you can see the true size of the page tooltip as you design it.</span></span>
- <span data-ttu-id="beaa6-162">**สไตล์:** พิจารณาการออกแบบคำแนะนำเครื่องมือของหน้าของคุณเพื่อใช้ธีมและสไตล์เดียวกันกับรายงาน</span><span class="sxs-lookup"><span data-stu-id="beaa6-162">**Style:** Consider designing your page tooltip to use the same theme and style as the report.</span></span> <span data-ttu-id="beaa6-163">ด้วยวิธีนี้ผู้ใช้จะรู้สึกเหมือนกับอยู่ในรายงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="beaa6-163">This way, users feel like they are in the same report.</span></span> <span data-ttu-id="beaa6-164">หรือออกแบบสไตล์แบบฟรีสำหรับคำแนะนำเครื่องมือของคุณ และอย่าลืมใช้สไตล์นี้กับคำแนะนำเครื่องมือทุกหน้า</span><span class="sxs-lookup"><span data-stu-id="beaa6-164">Or, design a complimentary style for your tooltips, and be sure to apply this style to all page tooltips.</span></span>
- <span data-ttu-id="beaa6-165">**ตัวกรองคำแนะนำเครื่องมือ:** กำหนดตัวกรองให้กับคำแนะนำเครื่องมือของหน้าเพื่อให้คุณสามารถแสดงตัวอย่างผลลัพธ์ที่เหมือนจริงได้ขณะที่คุณออกแบบ</span><span class="sxs-lookup"><span data-stu-id="beaa6-165">**Tooltip filters:** Assign filters to the page tooltip so that you can preview a realistic result as you design it.</span></span> <span data-ttu-id="beaa6-166">ตรวจสอบให้แน่ใจว่าคุณลบตัวกรองเหล่านี้ออกแล้วก่อนที่คุณจะเผยแพร่รายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="beaa6-166">Be sure to remove these filters before you publish your report.</span></span>
- <span data-ttu-id="beaa6-167">**การมองเห็นหน้าเพจ:** ซ่อนคำแนะนำเครื่องมือของหน้าเสมอ—ผู้ใช้ไม่ควรนำทางไปยังแอปเหล่านั้นโดยตรง</span><span class="sxs-lookup"><span data-stu-id="beaa6-167">**Page visibility:** Always hide tooltip pages—users shouldn't navigate directly to them.</span></span>

## <a name="next-steps"></a><span data-ttu-id="beaa6-168">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="beaa6-168">Next steps</span></span>

<span data-ttu-id="beaa6-169">สำหรับข้อมูลเพิ่มเติมที่เกี่ยวข้องกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="beaa6-169">For more information related to this article, check out the following resources:</span></span>

- [<span data-ttu-id="beaa6-170">สร้างคำแนะนำเครื่องมือตามหน้ารายงานใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="beaa6-170">Create tooltips based on report pages in Power BI Desktop</span></span>](../create-reports/desktop-tooltips.md)
- [<span data-ttu-id="beaa6-171">การกำหนดค่าคำแนะนำเครื่องมือเองใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="beaa6-171">Customizing tooltips in Power BI Desktop</span></span>](../create-reports/desktop-custom-tooltips.md)
- [<span data-ttu-id="beaa6-172">ใช้องค์ประกอบภาพเพื่อปรับปรุงรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="beaa6-172">Use visual elements to enhance Power BI reports</span></span>](../create-reports/desktop-visual-elements-for-reports.md)
- <span data-ttu-id="beaa6-173">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="beaa6-173">Questions?</span></span> [<span data-ttu-id="beaa6-174">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="beaa6-174">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="beaa6-175">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="beaa6-175">Suggestions?</span></span> [<span data-ttu-id="beaa6-176">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="beaa6-176">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com/)
