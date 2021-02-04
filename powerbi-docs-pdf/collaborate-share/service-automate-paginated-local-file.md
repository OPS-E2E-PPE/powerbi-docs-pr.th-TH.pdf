---
title: บันทึกรายงานที่มีการแบ่งหน้าไปยังโฟลเดอร์ภายในเครื่องด้วย Power Automate
description: ในบทความนี้ คุณจะใช้เทมเพลตเพื่อตั้งค่าการส่งออกที่เกิดซ้ำของรายงานที่มีการแบ่งหน้าไปยังระบบไฟล์ของคุณในรูปแบบที่ต้องการ
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 12/08/2020
LocalizationGroup: Get started
ms.openlocfilehash: a30f0df972c375af4fb284ce3bba5372870d6efb
ms.sourcegitcommit: bbf7e9341a4e1cc96c969e24318c8605440282a5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/11/2020
ms.locfileid: "97098816"
---
# <a name="save-a-power-bi-paginated-report-to-a-local-folder--with-power-automate"></a><span data-ttu-id="36b9c-103">บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยังโฟลเดอร์ภายในเครื่องด้วย Power Automate</span><span class="sxs-lookup"><span data-stu-id="36b9c-103">Save a Power BI paginated report to a local folder  with Power Automate</span></span>

<span data-ttu-id="36b9c-104">ด้วย [Power Automate](/power-automate/getting-started) คุณสามารถทำให้การส่งออกและการแจกจ่ายรายงานที่มีการแบ่งหน้า Power BI ไปยังรูปแบบและสถานการณ์ที่ได้รับการสนับสนุนเป็นแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="36b9c-104">With [Power Automate](/power-automate/getting-started), you can automate exporting and distributing Power BI paginated reports to a variety of supported formats and scenarios.</span></span> <span data-ttu-id="36b9c-105">ในบทความนี้ คุณจะใช้เทมเพลตเพื่อตั้งค่าการส่งออกที่เกิดซ้ำของรายงานที่มีการแบ่งหน้าไปยังระบบไฟล์ของคุณในรูปแบบที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="36b9c-105">In this article, you use a template to set up recurring exports of a paginated report to your file system, in a desired format.</span></span> <span data-ttu-id="36b9c-106">ดูข้อกำหนดเบื้องต้นหากคุณใช้งานการดำเนินการส่งออกรายงานที่มีการแบ่งหน้าไปยังไฟล์ในโฟลว์ Power Automate เป็นครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="36b9c-106">See the Prerequisites if it's your first time using the Export to File for Paginated Reports action in a Power Automate flow.</span></span>

:::image type="content" source="media/service-automate-paginated-local-file/paginated-local-file-overview.png" alt-text="ตั้งค่าการส่งออกที่เกิดซ้ำของรายงานที่มีการแบ่งหน้า":::

<span data-ttu-id="36b9c-108">คุณกำลังมองหาเทมเพลต Power Automate อื่น ๆ สำหรับรายงานที่มีการแบ่งหน้า Power BI ใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="36b9c-108">Looking for other Power Automate templates for Power BI paginated reports?</span></span> <span data-ttu-id="36b9c-109">โปรดดู[ส่งออกรายงานที่มีการแบ่งหน้า Power BI ด้วย Power Automate](service-automate-paginated-integration.md)</span><span class="sxs-lookup"><span data-stu-id="36b9c-109">See [Export Power BI paginated reports with Power Automate](service-automate-paginated-integration.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="36b9c-110">สิ่งที่จำเป็นต้องมี</span><span class="sxs-lookup"><span data-stu-id="36b9c-110">Prerequisites</span></span>  

<span data-ttu-id="36b9c-111">เพื่อดำเนินการต่อไป คุณควรตรวจสอบให้แน่ใจว่าคุณมีรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="36b9c-111">To follow along, make sure you have:</span></span>

- <span data-ttu-id="36b9c-112">พื้นที่ทำงานในผู้เช่า Power BI ของคุณที่ได้รับการสนับสนุนจากความจุที่สงวนไว้อย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="36b9c-112">At least one workspace in your Power BI tenant backed by a reserved capacity.</span></span> <span data-ttu-id="36b9c-113">ความจุนี้สามารถเป็น SKU ใดก็ได้ตั้งแต่ A4/P1 – A6/P3</span><span class="sxs-lookup"><span data-stu-id="36b9c-113">This capacity can be any of the A4/P1 – A6/P3 SKUs.</span></span> <span data-ttu-id="36b9c-114">อ่านข้อมูลเพิ่มเติมเกี่ยวกับ[ความจุสำรองสำหรับรายงานที่มีการแบ่งหน้าใน Power BI Premium](../admin/service-premium-what-is.md#paginated-reports)</span><span class="sxs-lookup"><span data-stu-id="36b9c-114">Read more about [reserved capacities for paginated reports in Power BI Premium](../admin/service-premium-what-is.md#paginated-reports).</span></span>
- <span data-ttu-id="36b9c-115">เข้าถึงตัวเชื่อมต่อมาตรฐานใน Power Automate ซึ่งมาพร้อมกับการสมัครใช้งาน Office 365</span><span class="sxs-lookup"><span data-stu-id="36b9c-115">Access to the standard connectors in Power Automate, which come with any Office 365 subscription.</span></span>

## <a name="save-a-power-bi-paginated-report-to-a-local-folder"></a><span data-ttu-id="36b9c-116">บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยังโฟลเดอร์ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="36b9c-116">Save a Power BI paginated report to a local folder</span></span>

1. <span data-ttu-id="36b9c-117">เลือก **บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยังเทมเพลตระบบไฟล์ภายในเครื่อง**</span><span class="sxs-lookup"><span data-stu-id="36b9c-117">Select the **Save a Power BI paginated report to a local file system** template.</span></span> <span data-ttu-id="36b9c-118">ตรวจสอบให้แน่ใจว่าคุณได้ลงชื่อเข้าใช้ Power BI และเชื่อมต่อกับระบบไฟล์ภายในเครื่องของคุณ</span><span class="sxs-lookup"><span data-stu-id="36b9c-118">Make sure you're signed into Power BI and connected to your local file system.</span></span> <span data-ttu-id="36b9c-119">เลือก **ดำเนินต่อ**</span><span class="sxs-lookup"><span data-stu-id="36b9c-119">Select **Continue**.</span></span> 

    :::image type="content" source="media/service-automate-paginated-local-file/paginated-local-file-save-report-local-file-1.png" alt-text="บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยังระบบไฟล์ภายในเครื่อง":::

2. <span data-ttu-id="36b9c-121">คุณอาจจำเป็นต้องเลือก **เพิ่มการเชื่อมต่อใหม่** เพื่อเชื่อมต่อกับระบบไฟล์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="36b9c-121">You may need to select **Add new connection** to connect to your file system.</span></span> 
1. <span data-ttu-id="36b9c-122">ใส่ **ชื่อการเชื่อมต่อ** เส้นทางไปยัง **โฟลเดอร์ราก** ที่คุณต้องการ และรับรองความถูกต้องโดยใส่ **ชื่อผู้ใช้** และ **รหัสผ่าน** ของคุณ</span><span class="sxs-lookup"><span data-stu-id="36b9c-122">Enter a **Connection Name**, the path to your desired **Root folder**, and authenticate by entering your **User name** and **Password**.</span></span> <span data-ttu-id="36b9c-123">เลือก **เกตเวย์** จากรายการดรอปดาวน์หากคุณกำลังใช้เกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="36b9c-123">Select a **gateway** from the dropdown if you're using an on-premises data gateway.</span></span>

    :::image type="content" source="media/service-automate-paginated-local-file/paginated-local-file-set-file-system-2.png" alt-text="ใส่ชื่อการเชื่อมต่อและโฟลเดอร์ราก":::
 
3. <span data-ttu-id="36b9c-125">เมื่อต้องการตั้งค่าความถี่ **การเกิดขึ้นประจำ** สำหรับโฟลว์ของคุณ ให้เลือกตัวเลือกจากรายการดรอปดาวน์ **ความถี่** และใส่ค่า **ช่วง** ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="36b9c-125">To set the **Recurrence** frequency for your flow, select an option from the **Frequency** dropdown and enter a desired **Interval** value.</span></span>  

    :::image type="content" source="media/service-automate-paginated-local-file/paginated-local-file-recurrence-frequency-3.png" alt-text="ตั้งค่าความถี่การเกิดขึ้นประจำสำหรับโฟลว์ของคุณ":::

4. <span data-ttu-id="36b9c-127">หรือเลือก **แสดงตัวเลือกขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="36b9c-127">Optionally, select **Show advanced options**.</span></span> <span data-ttu-id="36b9c-128">ตั้งค่าพารามิเตอร์ **การเกิดขึ้นประจำ** เพิ่มเติม เช่น **โซนเวลา** **เวลาเริ่มต้น** **ในวันนี้** **ในชั่วโมงนี้** และ **ในนาทีนี้**</span><span class="sxs-lookup"><span data-stu-id="36b9c-128">Set additional **Recurrence** parameters such as **Time zone**, **Start time**, **On these days,** **At these hours**, and **At these minutes**.</span></span> 
 
    :::image type="content" source="media/service-automate-paginated-local-file/paginated-local-file-recurrence-advanced-4.png" alt-text="ตั้งค่าตัวเลือกขั้นสูงสำหรับการเกิดขึ้นประจำ":::

5. <span data-ttu-id="36b9c-130">ในกล่อง **พื้นที่ทำงาน** ให้เลือกพื้นที่ทำงานในความจุสำรองที่มีรายงานอยู่</span><span class="sxs-lookup"><span data-stu-id="36b9c-130">In the **Workspace** box, select a workspace in a reserved capacity where the report is.</span></span> <span data-ttu-id="36b9c-131">ในกล่อง **รายงาน** ให้เลือกรายงานที่มีการแบ่งหน้าที่คุณต้องการส่งออกในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="36b9c-131">In the **Report** box, select the paginated report that you wish to export in the workspace.</span></span> <span data-ttu-id="36b9c-132">ในกล่อง **รูปแบบการส่งออก** ให้เลือกรูปแบบการส่งออกที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="36b9c-132">In the **Export Format** box, select the desired export format.</span></span> <span data-ttu-id="36b9c-133">อีกทางหนึ่งคือคุณสามารถระบุพารามิเตอร์สำหรับรายงานที่มีการแบ่งหน้าได้</span><span class="sxs-lookup"><span data-stu-id="36b9c-133">Optionally, you can specify parameters for the paginated report.</span></span> <span data-ttu-id="36b9c-134">ดูคำอธิบายโดยละเอียดเกี่ยวกับพารามิเตอร์ใน[การอ้างอิงตัวเชื่อมต่อสำหรับ Power BI REST API](/connectors/powerbi/#export-to-file-for-paginated-reports)</span><span class="sxs-lookup"><span data-stu-id="36b9c-134">See detailed descriptions of the parameters in the [connector reference for the Power BI REST API](/connectors/powerbi/#export-to-file-for-paginated-reports).</span></span>  
 
    :::image type="content" source="media/service-automate-paginated-local-file/paginated-local-file-select-workspace-report-5.png" alt-text="เลือกพื้นที่ทำงานและรายงาน":::

6. <span data-ttu-id="36b9c-136">ในกล่องโต้ตอบ **สร้างไฟล์** ใน **เส้นทางโฟลเดอร์** ให้เลือกโฟลเดอร์ที่คุณต้องการส่งออกรายงานที่มีการแบ่งหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="36b9c-136">In the **Create file** dialog, in **Folder Path**, select the folder where you want to export your paginated report.</span></span>
 
    :::image type="content" source="media/service-automate-paginated-local-file/paginated-local-file-create-file-6.png" alt-text="เลือกโฟลเดอร์ที่คุณต้องการส่งออกรายงานที่มีการแบ่งหน้าของคุณ":::

7. <span data-ttu-id="36b9c-138">Power Automate จะสร้าง **ชื่อไฟล์** และ **เนื้อหาไฟล์** ให้กับคุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="36b9c-138">Power Automate automatically generates a **File name** and **File content** for you.</span></span> <span data-ttu-id="36b9c-139">คุณสามารถปรับเปลี่ยน **ชื่อไฟล์** แต่คงค่า **เนื้อหาไฟล์** ที่สร้างขึ้นแบบไดนามิกได้</span><span class="sxs-lookup"><span data-stu-id="36b9c-139">You can modify the **File name**, but keep the dynamically generated **File content** value.</span></span>
8. <span data-ttu-id="36b9c-140">เมื่อเสร็จสิ้นแล้ว ให้เลือก **ขั้นตอนถัดไป** หรือ **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="36b9c-140">When you're done, select **Next step** or **Save**.</span></span> <span data-ttu-id="36b9c-141">Power Automate จะสร้างและประเมินโฟลว์</span><span class="sxs-lookup"><span data-stu-id="36b9c-141">Power Automate creates and evaluates the flow.</span></span>
9. <span data-ttu-id="36b9c-142">หาก Power Automate พบข้อผิดพลาด ให้เลือก **แก้ไขโฟลว์** เพื่อแก้ไขข้อผิดพลาดดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="36b9c-142">If Power Automate finds errors, select **Edit flow** to fix them.</span></span> <span data-ttu-id="36b9c-143">อีกทางหนึ่งคือ เลือกลูกศรย้อนกลับเพื่อดูรายละเอียดโฟลว์ และเรียกใช้โฟลว์ใหม่</span><span class="sxs-lookup"><span data-stu-id="36b9c-143">Otherwise, select the Back arrow to view the flow details and run the new flow.</span></span>
10. <span data-ttu-id="36b9c-144">เมื่อคุณเรียกใช้โฟลว์ Power Automate จะส่งออกรายงานที่มีการแบ่งหน้าในรูปแบบที่ระบุไว้ไปยังโฟลเดอร์ที่เลือกในระบบไฟล์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="36b9c-144">When you run the flow, Power Automate exports a paginated report in the specified format to the selected folder in your file system.</span></span>

    :::image type="content" source="media/service-automate-paginated-local-file/paginated-local-file-exported-10.png" alt-text="Power Automate จะส่งออกรายงานที่มีการแบ่งหน้าในรูปแบบที่ระบุไว้":::

## <a name="next-steps"></a><span data-ttu-id="36b9c-146">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="36b9c-146">Next steps</span></span>

- [<span data-ttu-id="36b9c-147">ส่งออกรายงานที่มีการแบ่งหน้า Power BI ด้วย Power Automate</span><span class="sxs-lookup"><span data-stu-id="36b9c-147">Export Power BI paginated reports with Power Automate</span></span>](service-automate-paginated-integration.md)
- [<span data-ttu-id="36b9c-148">เริ่มต้นใช้งาน Power Automate</span><span class="sxs-lookup"><span data-stu-id="36b9c-148">Get started with Power Automate</span></span>](/power-automate/getting-started/)
- <span data-ttu-id="36b9c-149">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="36b9c-149">More questions?</span></span> [<span data-ttu-id="36b9c-150">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="36b9c-150">Try the Power BI Community</span></span>](https://community.powerbi.com/)

