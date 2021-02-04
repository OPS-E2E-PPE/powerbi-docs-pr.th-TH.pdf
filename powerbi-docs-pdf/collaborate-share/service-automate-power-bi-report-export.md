---
title: ส่งออกและส่งรายงานทางอีเมลด้วย Power Automate
description: ในบทความนี้ คุณจะใช้ Power Automate เพื่อปรับให้การส่งออกและการแจกจ่ายรายงาน Power BI เป็นไปโดยอัตโนมัติในรูปแบบและสถานการณ์ต่างๆ ที่รองรับ
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 12/10/2020
LocalizationGroup: Get started
ms.openlocfilehash: 45bccbefc6e499375d33aa049ead8a6c6e47bc8c
ms.sourcegitcommit: bbf7e9341a4e1cc96c969e24318c8605440282a5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/11/2020
ms.locfileid: "97098837"
---
# <a name="export-and-email-a-power-bi-report-with-power-automate"></a><span data-ttu-id="73cb0-103">ส่งออกและส่งรายงาน Power BI ทางอีเมลด้วย Power Automate</span><span class="sxs-lookup"><span data-stu-id="73cb0-103">Export and email a Power BI report with Power Automate</span></span>

<span data-ttu-id="73cb0-104">ด้วย [Power Automate](/power-automate/getting-started) คุณสามารถปรับให้การส่งออกและการกระจายรายงาน Power BI เป็นไปโดยอัตโนมัติตามรูปแบบและสถานการณ์ต่างๆ</span><span class="sxs-lookup"><span data-stu-id="73cb0-104">With [Power Automate](/power-automate/getting-started), you can automate exporting and distributing Power BI reports to a variety of formats and scenarios.</span></span> <span data-ttu-id="73cb0-105">ในบทความนี้ คุณจะสร้างโฟลว์ของคุณเองตั้งแต่ต้น</span><span class="sxs-lookup"><span data-stu-id="73cb0-105">In this article, you create your own flow from scratch.</span></span> <span data-ttu-id="73cb0-106">คุณจะใช้การดำเนินการส่งออกไปยังไฟล์สำหรับรายงาน Power BI เพื่อแจกจ่ายรายงาน Power BI ทางอีเมลโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="73cb0-106">You use the Export to File for Power BI Reports action to automatically distribute a Power BI report via email.</span></span>

:::image type="content" source="media/service-automate-power-bi-report-export/automate-power-bi-report-overview.png" alt-text="ขั้นตอนการส่งออกและการส่งรายงานทางอีเมลของ Power Automate":::

## <a name="prerequisites"></a><span data-ttu-id="73cb0-108">สิ่งที่จำเป็นต้องมี</span><span class="sxs-lookup"><span data-stu-id="73cb0-108">Prerequisites</span></span>  

<span data-ttu-id="73cb0-109">เพื่อดำเนินการต่อไป คุณควรตรวจสอบให้แน่ใจว่าคุณมีรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="73cb0-109">To follow along, make sure you have:</span></span>

- <span data-ttu-id="73cb0-110">พื้นที่ทำงานในผู้เช่า Power BI ของคุณที่ได้รับการสนับสนุนจากความจุที่สงวนไว้อย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="73cb0-110">At least one workspace in your Power BI tenant backed by a reserved capacity.</span></span> <span data-ttu-id="73cb0-111">ความจุนี้อาจเป็น A1/EM1 - A6/P3 SKUs</span><span class="sxs-lookup"><span data-stu-id="73cb0-111">This capacity can be any of the A1/EM1 - A6/P3 SKUs.</span></span> <span data-ttu-id="73cb0-112">อ่านเพิ่มเติมเกี่ยวกับ[ความจุที่สงวนไว้ใน Power BI Premium](../admin/service-premium-what-is.md)</span><span class="sxs-lookup"><span data-stu-id="73cb0-112">Read more about [reserved capacities in Power BI Premium](../admin/service-premium-what-is.md).</span></span>
- <span data-ttu-id="73cb0-113">เข้าถึงตัวเชื่อมต่อมาตรฐานใน Power Automate ซึ่งมาพร้อมกับการสมัครใช้งาน Office 365</span><span class="sxs-lookup"><span data-stu-id="73cb0-113">Access to the standard connectors in Power Automate, which come with any Office 365 subscription.</span></span>

## <a name="create-a-flow-from-scratch"></a><span data-ttu-id="73cb0-114">สร้างโฟลว์ตั้งแต่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="73cb0-114">Create a flow from scratch</span></span> 

<span data-ttu-id="73cb0-115">ในงานนี้ คุณจะสร้างโฟลว์ง่ายๆ ตั้งแต่ต้น</span><span class="sxs-lookup"><span data-stu-id="73cb0-115">In this task, you create a simple flow from scratch.</span></span> <span data-ttu-id="73cb0-116">โฟลว์จะส่งออกรายงาน Power BI เป็น PDF และจะแนบไปกับอีเมลที่จะส่งเป็นรายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="73cb0-116">The flow exports a Power BI report as a PDF, and attaches it to an email to be sent on a weekly basis.</span></span>  

1. <span data-ttu-id="73cb0-117">ลงชื่อเข้าใช้ Power Automate (flow.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="73cb0-117">Sign in to Power Automate (flow.microsoft.com).</span></span>
2. <span data-ttu-id="73cb0-118">เลือก **สร้าง** > **โฟลว์ที่จัดกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="73cb0-118">Select **Create** > **Scheduled flow**.</span></span> 

    :::image type="content" source="media/service-automate-power-bi-report-export/automate-report-scheduled-flow-2.png" alt-text="สร้างโฟลว์ที่จัดกำหนดการใน Power Automate":::

3. <span data-ttu-id="73cb0-120">ใน **สร้างโฟลว์ที่จัดกำหนดการ** ให้ตั้งชื่อโฟลว์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="73cb0-120">In **Build a scheduled flow**, give your flow a name.</span></span> 
4. <span data-ttu-id="73cb0-121">ใน **เรียกใช้โฟลว์นี้** ให้เลือกวันที่และเวลาเริ่มต้นสำหรับโฟลว์ของคุณ รวมถึงความถี่การเกิดขึ้นประจำ</span><span class="sxs-lookup"><span data-stu-id="73cb0-121">In **Run this flow**, select the starting date and time for your flow, as well as the repetition frequency.</span></span>
5. <span data-ttu-id="73cb0-122">ใน **ในวันนี้** ให้เลือกวันที่ที่คุณต้องการให้โฟลว์ของคุณถูกเรียกใช้ แล้วเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="73cb0-122">In **On these days**, select which days you want your flow to run, and select **Create**.</span></span>

    :::image type="content" source="media/service-automate-power-bi-report-export/automate-report-build-flow-5.png" alt-text="Power Automate จัดกำหนดการโฟลว์":::

6. <span data-ttu-id="73cb0-124">ใน **การเกิดขึ้นประจำ** ให้เลือก **แสดงตัวเลือกขั้นสูง** และใส่ค่าใน **ในชั่วโมงนี้** และ **ในนาทีนี้** เพื่อกำหนดเวลาที่เฉพาะเจาะจงสำหรับโฟลว์ของคุณที่จะถูกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="73cb0-124">In **Recurrence**, select **Show advanced options** and enter a value in **At these hours** and **At these minutes** to set a specific time for your flow to run.</span></span>
 
    :::image type="content" source="media/service-automate-power-bi-report-export/automate-report-recurrence-6.png" alt-text="ตั้งค่าการเกิดขึ้นประจำใน Power Automate":::

7. <span data-ttu-id="73cb0-126">เลือก **ขั้นตอนใหม่**</span><span class="sxs-lookup"><span data-stu-id="73cb0-126">Select **New Step**.</span></span>
8. <span data-ttu-id="73cb0-127">ใน **เลือกการดำเนินการ** ให้ค้นหา **Power BI** แล้วเลือก **ส่งออกไปยังไฟล์สำหรับรายงาน Power BI**</span><span class="sxs-lookup"><span data-stu-id="73cb0-127">In **Choose an action**, search for **Power BI** and select **Export to File for Power BI Reports**.</span></span>
 
    :::image type="content" source="media/service-automate-power-bi-report-export/automate-report-choose-action-8.png" alt-text="เลือกการดำเนินการใน Power Automate":::

9. <span data-ttu-id="73cb0-129">ใน **ส่งออกไปยังไฟล์สำหรับรายงาน Power BI** ให้เลือก **พื้นที่ทำงาน** และ **รายงาน** จากรายการดรอปดาวน์</span><span class="sxs-lookup"><span data-stu-id="73cb0-129">In **Export to File for Power BI Reports**, select a **Workspace** and **Report** from the dropdowns.</span></span>
10. <span data-ttu-id="73cb0-130">เลือก **รูปแบบการส่งออก** ที่ต้องการสำหรับรายงาน Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="73cb0-130">Select the desired **Export Format** for your Power BI report.</span></span>
 
    :::image type="content" source="media/service-automate-power-bi-report-export/automate-report-export-file-10.png" alt-text="เลือกรูปแบบการส่งออกใน Power Automate":::

11. <span data-ttu-id="73cb0-132">หรือระบุหน้าเฉพาะที่จะส่งออกในเขตข้อมูล **Pages pageName -1**</span><span class="sxs-lookup"><span data-stu-id="73cb0-132">Optionally, indicate specific pages to export in the **Pages pageName -1** field.</span></span> <span data-ttu-id="73cb0-133">โปรดทราบว่าพารามิเตอร์ชื่อหน้าจะแตกต่างจากชื่อหน้าที่แสดง</span><span class="sxs-lookup"><span data-stu-id="73cb0-133">Note the page name parameter is different from the display page name.</span></span> <span data-ttu-id="73cb0-134">ค้นหาชื่อหน้าโดยการนำทางไปยังหน้าในบริการ Power BI และคัดลอกส่วนสุดท้ายของ URL</span><span class="sxs-lookup"><span data-stu-id="73cb0-134">Find the page name by navigating to the page in the Power BI service, and copying the last portion of the URL.</span></span>
 
     :::image type="content" source="media/service-automate-power-bi-report-export/automate-report-copy-url-11.png" alt-text="เลือกชื่อบานหน้าต่างใน U R L":::

12. <span data-ttu-id="73cb0-136">หรือระบุบุ๊กมาร์กเฉพาะที่จะแสดงในเขตข้อมูล **Pages Bookmark Name**</span><span class="sxs-lookup"><span data-stu-id="73cb0-136">Optionally, indicate a specific bookmark to display in the **Pages Bookmark Name** field.</span></span> <span data-ttu-id="73cb0-137">เช่นเดียวกับพารามิเตอร์ชื่อหน้า คุณจะพบพารามิเตอร์ชื่อบุ๊กมาร์กใน URL รายงาน</span><span class="sxs-lookup"><span data-stu-id="73cb0-137">As with the page name parameter, you find the bookmark name parameter in the report URL.</span></span> <span data-ttu-id="73cb0-138">คุณสามารถระบุพารามิเตอร์เพิ่มเติมสำหรับรายงาน Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="73cb0-138">You can specify additional parameters for the Power BI report.</span></span> <span data-ttu-id="73cb0-139">ค้นหาคำอธิบายโดยละเอียดเกี่ยวกับพารามิเตอร์เหล่านี้ใน[การอ้างอิงตัวเชื่อมต่อสำหรับ Power BI REST API](/connectors/powerbi/#export-to-file-for-power-bi-reports)</span><span class="sxs-lookup"><span data-stu-id="73cb0-139">Find detailed descriptions of these parameters in the [connector reference for the Power BI REST API](/connectors/powerbi/#export-to-file-for-power-bi-reports).</span></span>

    :::image type="content" source="media/service-automate-power-bi-report-export/automate-report-bookmark-url-12.png" alt-text="เลือกชื่อบุ๊กมาร์กใน U R L":::

13. <span data-ttu-id="73cb0-141">เลือก **ขั้นตอนใหม่**</span><span class="sxs-lookup"><span data-stu-id="73cb0-141">Select **New Step**.</span></span>
14. <span data-ttu-id="73cb0-142">ใน **เลือกการดำเนินการ** ให้ค้นหา **Outlook** แล้วเลือก **ส่งอีเมล (V2)**</span><span class="sxs-lookup"><span data-stu-id="73cb0-142">In **Choose an action**, search for **Outlook** and select **Send an email (V2)**.</span></span>
15. <span data-ttu-id="73cb0-143">ใน **ส่งอีเมล (V2)** ให้กรอกเขตข้อมูล **ถึง** **ชื่อเรื่อง** และ **เนื้อหา** สำหรับอีเมลของคุณ</span><span class="sxs-lookup"><span data-stu-id="73cb0-143">In **Send an email (V2)**, complete the **To**, **Subject**, and **Body** fields for your email.</span></span>
16. <span data-ttu-id="73cb0-144">เลือก **แสดงตัวเลือกขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="73cb0-144">Select **Show advanced options**.</span></span> <span data-ttu-id="73cb0-145">ใน **ชื่อสิ่งที่แนบมา – 1** ใส่ชื่อสิ่งที่แนบมาของคุณ</span><span class="sxs-lookup"><span data-stu-id="73cb0-145">In **Attachments Name – 1**, enter a name for your attachment.</span></span> <span data-ttu-id="73cb0-146">เพิ่มนามสกุลไฟล์ลงในชื่อไฟล์ (เช่น .PDF) ที่ตรงกับ **รูปแบบการส่งออก** ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="73cb0-146">Add a file extension to the file name (for example, .PDF) that matches your desired **Export Format**.</span></span>
17. <span data-ttu-id="73cb0-147">ใน **เนื้อหาสิ่งที่แนบมา** ให้เลือก **เนื้อหาไฟล์** เพื่อแนบรายงาน Power BI ที่ส่งออก</span><span class="sxs-lookup"><span data-stu-id="73cb0-147">In **Attachment Content**, select **File Content** to attach your exported Power BI report.</span></span>  
 
    :::image type="content" source="media/service-automate-power-bi-report-export/automate-report-send-email-17.png" alt-text="เลือกรายงานที่ส่งออกของคุณไปยังอีเมล":::

18. <span data-ttu-id="73cb0-149">เมื่อเสร็จสิ้นแล้ว ให้เลือก **ขั้นตอนถัดไป** หรือ **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="73cb0-149">When you're done, select **Next step** or **Save**.</span></span> <span data-ttu-id="73cb0-150">Power Automate สร้างและประเมินโฟลว์ และแจ้งให้คุณทราบว่าพบข้อผิดพลาดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="73cb0-150">Power Automate creates and evaluates the flow, and lets you know if it finds errors.</span></span>
1. <span data-ttu-id="73cb0-151">ถ้ามีข้อผิดพลาด ให้เลือก **แก้ไขโฟลว์** เพื่อแก้ไขโฟลว์เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="73cb0-151">If there are errors, select **Edit flow** to fix them.</span></span> <span data-ttu-id="73cb0-152">อีกทางหนึ่งคือ เลือกลูกศร **ย้อนกลับ** เพื่อดูรายละเอียดโฟลว์ และเรียกใช้โฟลว์ใหม่</span><span class="sxs-lookup"><span data-stu-id="73cb0-152">Otherwise, select the **Back** arrow to view the flow details and run the new flow.</span></span>
    <span data-ttu-id="73cb0-153">เมื่อคุณเรียกใช้โฟลว์ Power Automate จะส่งออกรายงาน Power BI ในรูปแบบที่ระบุไว้ และส่งเป็นสิ่งที่แนบมากับอีเมลตามที่กำหนดเวลาไว้</span><span class="sxs-lookup"><span data-stu-id="73cb0-153">When you run the flow, Power Automate exports a Power BI report in the specified format and sends it as an email attachment as scheduled.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="73cb0-154">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="73cb0-154">Next steps</span></span>

- [<span data-ttu-id="73cb0-155">รวมการแจ้งเตือนข้อมูล Power BI ด้วย Power Automate</span><span class="sxs-lookup"><span data-stu-id="73cb0-155">Integrate Power BI data alerts with Power Automate</span></span>](service-flow-integration.md)
- [<span data-ttu-id="73cb0-156">เริ่มต้นใช้งาน Power Automate</span><span class="sxs-lookup"><span data-stu-id="73cb0-156">Get started with Power Automate</span></span>](/power-automate/getting-started/)
- <span data-ttu-id="73cb0-157">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="73cb0-157">More questions?</span></span> [<span data-ttu-id="73cb0-158">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="73cb0-158">Try the Power BI Community</span></span>](https://community.powerbi.com/)
