---
title: ใช้การดูหน้ารายงานแบบเจาะลึก
description: คำแนะนำสำหรับการทำงานกับการดูรายละเอียดหน้ารายงานแบบเจาะลึก
author: peter-myers
ms.author: v-pemyer
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 11/28/2019
ms.openlocfilehash: 4aa7c3992183dad6fad30e31e31e935fbaa29c32
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418497"
---
# <a name="use-report-page-drillthrough"></a><span data-ttu-id="71223-103">ใช้การดูหน้ารายงานแบบเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="71223-103">Use report page drillthrough</span></span>

<span data-ttu-id="71223-104">บทความนี้กำหนดเป้าหมายคุณในฐานะผู้สร้างรายงานที่ออกแบบรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="71223-104">This article targets you as a report author who designs Power BI reports.</span></span> <span data-ttu-id="71223-105">ซึ่งมีข้อเสนอแนะและคำแนะนำเมื่อสร้าง [การดูรายละเอียดหน้ารายงานแบบเจาะลึก](../create-reports/desktop-drillthrough.md)</span><span class="sxs-lookup"><span data-stu-id="71223-105">It provides suggestions and recommendations when creating [report page drillthrough](../create-reports/desktop-drillthrough.md).</span></span>

<span data-ttu-id="71223-106">ขอแนะนำให้คุณออกแบบรายงานของคุณเพื่อให้ผู้ใช้รายงานได้รับโฟลว์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="71223-106">It's recommended that you design your report to allow report users to achieve the following flow:</span></span>

1. <span data-ttu-id="71223-107">ดูหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="71223-107">View a report page.</span></span>
2. <span data-ttu-id="71223-108">ระบุองค์ประกอบวิชวลเพื่อวิเคราะห์ได้ลึกมากยิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="71223-108">Identify a visual element to analyze more deeply.</span></span>
3. <span data-ttu-id="71223-109">คลิกขวาที่องค์ประกอบวิชวลเพื่อดูรายละเอียดเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="71223-109">Right-click the visual element to drillthrough.</span></span>
4. <span data-ttu-id="71223-110">ดำเนินการวิเคราะห์แบบฟรี</span><span class="sxs-lookup"><span data-stu-id="71223-110">Perform complimentary analysis.</span></span>
5. <span data-ttu-id="71223-111">กลับไปยังหน้ารายงานต้นทาง</span><span class="sxs-lookup"><span data-stu-id="71223-111">Return to the source report page.</span></span>

## <a name="suggestions"></a><span data-ttu-id="71223-112">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="71223-112">Suggestions</span></span>

<span data-ttu-id="71223-113">เราขอแนะนำว่าคุณควรพิจารณาสถานการณ์จำลองการเจาะลึกสองประเภท:</span><span class="sxs-lookup"><span data-stu-id="71223-113">We suggest that you consider two types of drillthrough scenarios:</span></span>

- [<span data-ttu-id="71223-114">ความลึกเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="71223-114">Additional depth</span></span>](#additional-depth)
- [<span data-ttu-id="71223-115">มุมมองที่กว้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="71223-115">Broader perspective</span></span>](#broader-perspective)

### <a name="additional-depth"></a><span data-ttu-id="71223-116">ความลึกเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="71223-116">Additional depth</span></span>

<span data-ttu-id="71223-117">เมื่อหน้ารายงานของคุณแสดงผลลัพธ์สรุป หน้าการดูรายละเอียดแบบเจาะลึกสามารถนำผู้ใช้รายงานไปยังรายละเอียดระดับธุรกรรมได้</span><span class="sxs-lookup"><span data-stu-id="71223-117">When your report page displays summarized results, a drillthrough page can lead report users to transaction-level details.</span></span> <span data-ttu-id="71223-118">วิธีการออกแบบนี้ช่วยให้พวกเขาดูธุรกรรมที่สนับสนุนและเฉพาะเมื่อจำเป็นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="71223-118">This design approach allows them to view supporting transactions, and only when needed.</span></span>

<span data-ttu-id="71223-119">ตัวอย่างต่อไปนี้แสดงสิ่งที่เกิดขึ้นเมื่อผู้ใช้รายงานเจาะลึกผ่านการสรุปยอดขายรายเดือน</span><span class="sxs-lookup"><span data-stu-id="71223-119">The following example shows what happens when a report user drills through from a monthly sales summary.</span></span> <span data-ttu-id="71223-120">หน้าการดูรายละเอียดแบบเจาะลึกประกอบด้วยรายการคำสั่งซื้อโดยละเอียดสำหรับเดือนที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="71223-120">The drillthrough page contains a detailed list of orders for a specific month.</span></span>

![เมทริกซ์วิชวลที่มีชื่อว่า "สรุปยอดขาย" จัดกลุ่มยอดขายตามปีและเดือนในแถวและประเทศในคอลัมน์](media/report-drillthrough/suggestion-drillthrough-add-depth.png)

### <a name="broader-perspective"></a><span data-ttu-id="71223-123">มุมมองที่กว้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="71223-123">Broader perspective</span></span>

<span data-ttu-id="71223-124">หน้าการดูรายละเอียดแบบเจาะลึกสามารถให้ผลลัพธ์ที่ตรงกันข้ามกับความลึกเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="71223-124">A drillthrough page can achieve the opposite of additional depth.</span></span> <span data-ttu-id="71223-125">สถานการณ์นี้เหมาะสำหรับการเจาะลึกผ่านมุมมองแบบองค์รวม</span><span class="sxs-lookup"><span data-stu-id="71223-125">This scenario is great for drilling through to a holistic view.</span></span>

<span data-ttu-id="71223-126">ตัวอย่างต่อไปนี้แสดงสิ่งที่เกิดขึ้นเมื่อผู้ใช้รายงานเจาะลึกผ่านรหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="71223-126">The following example shows what happens when a report user drills through from a zip code.</span></span> <span data-ttu-id="71223-127">หน้าการดูรายละเอียดแบบเจาะลึกจะแสดงข้อมูลทั่วไปเกี่ยวกับรหัสไปรษณีย์นั้น</span><span class="sxs-lookup"><span data-stu-id="71223-127">The drillthrough page displays general information about that zip code.</span></span>

![ตารางวิชวลประกอบด้วยสามคอลัมน์: รหัสไปรษณีย์ ค่าเฉลี่ยของคะแนนการละเมิด และค่าเฉลี่ยของการจัดอันดับเกรด](media/report-drillthrough/suggestion-drillthrough-broader-perspective.png)

## <a name="recommendations"></a><span data-ttu-id="71223-130">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="71223-130">Recommendations</span></span>

<span data-ttu-id="71223-131">ในขณะออกแบบรายงาน เราขอแนะนำแนวทางปฏิบัติดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="71223-131">At report design time, we recommend the following practices:</span></span>

- <span data-ttu-id="71223-132">**สไตล์:** พิจารณาการออกแบบหน้าการดูรายละเอียดแบบเจาะลึกของคุณเพื่อใช้ธีมและสไตล์เดียวกันกับรายงาน</span><span class="sxs-lookup"><span data-stu-id="71223-132">**Style:** Consider designing your drillthrough page to use the same theme and style as the report.</span></span> <span data-ttu-id="71223-133">ด้วยวิธีนี้ผู้ใช้จะรู้สึกเหมือนกับอยู่ในรายงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="71223-133">This way, users feel like they are in the same report.</span></span>
- <span data-ttu-id="71223-134">**ตัวกรองการดูรายละเอียดแบบเจาะลึก:** ตั้งค่าตัวกรองการดูรายละเอียดแบบเจาะลึกเพื่อให้คุณสามารถดูตัวอย่างผลลัพธ์ที่สมจริงในขณะที่คุณออกแบบหน้าการดูรายละเอียดแบบเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="71223-134">**Drillthrough filters:** Set drillthrough filters so you can preview a realistic result as you design the drillthrough page.</span></span> <span data-ttu-id="71223-135">ตรวจสอบให้แน่ใจว่าคุณลบตัวกรองเหล่านี้ออกแล้วก่อนที่คุณจะเผยแพร่รายงาน</span><span class="sxs-lookup"><span data-stu-id="71223-135">Be sure to remove these filters before you publish the report.</span></span>
- <span data-ttu-id="71223-136">**ความสามารถเพิ่มเติม:** หน้าการดูรายละเอียดแบบเจาะลึกคล้ายกับหน้ารายงานใด ๆ</span><span class="sxs-lookup"><span data-stu-id="71223-136">**Additional capabilities:** A drillthrough page is like any report page.</span></span> <span data-ttu-id="71223-137">คุณยังสามารถปรับปรุงประสิทธิภาพให้ดีขึ้นได้ด้วยความสามารถการโต้ตอบเพิ่มเติม รวมถึง ตัวแบ่งส่วนข้อมูลหรือตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="71223-137">You can even enhance it with additional interactive capabilities, including slicers or filters.</span></span>
- <span data-ttu-id="71223-138">**Blanks (ค่าว่าง):** หลีกเลี่ยงการเพิ่มวิชวลที่อาจแสดง BLANK หรือสร้างข้อผิดพลาดเมื่อมีการใช้ตัวกรองการดูรายละเอียดแบบเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="71223-138">**Blanks:** Avoid adding visuals that could display BLANK, or produce errors when drillthrough filters are applied.</span></span>
- <span data-ttu-id="71223-139">**การมองเห็นหน้าเพจ:** พิจารณาการซ่อนหน้าการดูรายละเอียดแบบเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="71223-139">**Page visibility:** Consider hiding drillthrough pages.</span></span> <span data-ttu-id="71223-140">หากคุณตัดสินใจที่จะทำให้หน้าการดูรายละเอียดแบบเจาะลึกปรากฏขึ้นเสมอ ให้แน่ใจว่าคุณได้เพิ่มปุ่มที่อนุญาตให้ผู้ใช้ล้างตัวกรองการดูรายละเอียดแบบเจาะลึกที่ตั้งไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="71223-140">If you decide to keep a drillthrough page visible, be sure to add a button that allows users to clear any previously-set drillthrough filters.</span></span> <span data-ttu-id="71223-141">กำหนด [บุ๊กมาร์ก](../create-reports/desktop-bookmarks.md) ให้กับปุ่ม</span><span class="sxs-lookup"><span data-stu-id="71223-141">Assign a [bookmark](../create-reports/desktop-bookmarks.md) to the button.</span></span> <span data-ttu-id="71223-142">ควรกำหนดค่าบุ๊กมาร์กเพื่อลบตัวกรองทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="71223-142">The bookmark should be configured to remove all filters.</span></span>
- <span data-ttu-id="71223-143">**ปุ่มย้อนกลับ:** ปุ่มย้อนกลับ [ปุ่ม](../create-reports/desktop-buttons.md) ถูกเพิ่มโดยอัตโนมัติเมื่อคุณกำหนดตัวกรองการดูรายละเอียดแบบเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="71223-143">**Back button:** A back [button](../create-reports/desktop-buttons.md) is added automatically when you assign a drillthrough filter.</span></span> <span data-ttu-id="71223-144">เป็นความคิดที่ดีที่จะเก็บปุ่มนี้ไว้</span><span class="sxs-lookup"><span data-stu-id="71223-144">It's a good idea to keep it.</span></span> <span data-ttu-id="71223-145">ด้วยวิธีนี้ ผู้ใช้รายงานของคุณสามารถกลับไปยังหน้าแหล่งข้อมูลได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="71223-145">This way, your report users can easily return to the source page.</span></span>
- <span data-ttu-id="71223-146">**ค้นพบ:** ช่วยส่งเสริมการรับรู้ของหน้าการดูรายละเอียดแบบเจาะลึกโดยการตั้งค่าข้อความไอคอนส่วนหัวของวิชวล หรือการเพิ่มคำแนะนำลงในกล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="71223-146">**Discovery:** Help promote awareness of a drillthrough page by setting visual header icon text, or adding instructions to a text box.</span></span> <span data-ttu-id="71223-147">คุณยังสามารถออกแบบภาพซ้อนทับ ตามที่อธิบายไว้ใน [บล็อกโพสต์นี้](https://alluringbi.com/2019/10/23/overlays-for-true-self-serve-reporting/)</span><span class="sxs-lookup"><span data-stu-id="71223-147">You can also design an overlay, as described in [this blog post](https://alluringbi.com/2019/10/23/overlays-for-true-self-serve-reporting/).</span></span>

> [!TIP]
> <span data-ttu-id="71223-148">นอกจากนี้ยังสามารถกำหนดค่าการดูรายละเอียดแบบเจาะลึกให้กับรายงานที่มีการแบ่งหน้าใน Power BI ของคุณได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="71223-148">It's also possible to configure drillthrough to your Power BI paginated reports.</span></span> <span data-ttu-id="71223-149">คุณสามารถทำสิ่งนี้ได้โดยการเพิ่มลิงก์ไปยังรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="71223-149">You can do this be adding links to Power BI reports.</span></span> <span data-ttu-id="71223-150">ลิงก์สามารถกำหนด [พารามิเตอร์ URL](https://powerbi.microsoft.com/blog/url-parameters-for-paginated-reports-are-now-available/)</span><span class="sxs-lookup"><span data-stu-id="71223-150">Links can define [URL parameters](https://powerbi.microsoft.com/blog/url-parameters-for-paginated-reports-are-now-available/).</span></span>

## <a name="next-steps"></a><span data-ttu-id="71223-151">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="71223-151">Next steps</span></span>

<span data-ttu-id="71223-152">สำหรับข้อมูลเพิ่มเติมที่เกี่ยวข้องกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="71223-152">For more information related to this article, check out the following resources:</span></span>

- [<span data-ttu-id="71223-153">ใช้ตัวเจาะเข้าถึงรายละเอียดใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="71223-153">Use drillthrough in Power BI Desktop</span></span>](../create-reports/desktop-drillthrough.md)
- <span data-ttu-id="71223-154">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="71223-154">Questions?</span></span> [<span data-ttu-id="71223-155">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="71223-155">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="71223-156">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="71223-156">Suggestions?</span></span> [<span data-ttu-id="71223-157">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="71223-157">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com/)
