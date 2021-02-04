---
title: บันทึกรายงานที่มีการแบบแบ่งหน้าไปยัง OneDrive for Business หรือ SharePoint Online
description: ในบทความนี้คุณสามารถใช้ Power Automate เพื่อทำให้การบันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยัง OneDrive for Business หรือโฟลเดอร์ SharePoint Online เป็นแบบอัตโนมัติ
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 11/17/2020
LocalizationGroup: Get started
ms.openlocfilehash: 6aaad48fb3e97aa6c1b4fc51834ee593a49a8192
ms.sourcegitcommit: bbf7e9341a4e1cc96c969e24318c8605440282a5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/11/2020
ms.locfileid: "97097742"
---
# <a name="save-a-paginated-report-to-onedrive-for-business-or-sharepoint-online"></a><span data-ttu-id="940b9-103">บันทึกรายงานที่มีการแบบแบ่งหน้าไปยัง OneDrive for Business หรือ SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="940b9-103">Save a paginated report to OneDrive for Business or SharePoint Online</span></span>

<span data-ttu-id="940b9-104">ด้วย [Power Automate](/power-automate/getting-started) คุณสามารถทำให้การส่งออกและการแจกจ่ายรายงานที่มีการแบ่งหน้า Power BI ไปยังรูปแบบและสถานการณ์ที่ได้รับการสนับสนุนเป็นแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="940b9-104">With [Power Automate](/power-automate/getting-started), you can automate exporting and distributing Power BI paginated reports to a variety of supported formats and scenarios.</span></span> <span data-ttu-id="940b9-105">ในบทความนี้คุณสามารถใช้ Power Automate เพื่อทำให้การบันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยัง OneDrive for Business หรือโฟลเดอร์ SharePoint Online เป็นแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="940b9-105">In this article, you use Power Automate to automate saving a Power BI paginated report to OneDrive for Business or a SharePoint Online folder.</span></span>


:::image type="content" source="media/service-automate-paginated-onedrive-sharepoint/paginated-onedrive-flow.png" alt-text="สกรีนช็อตของโฟลว์ Power Automate สำหรับการบันทึกรายงานที่มีการแบ่งหน้าไปยัง OneDrive หรือ SharePoint Online":::

<span data-ttu-id="940b9-107">คุณกำลังมองหาเทมเพลต Power Automate อื่น ๆ สำหรับรายงานที่มีการแบ่งหน้า Power BI ใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="940b9-107">Looking for other Power Automate templates for Power BI paginated reports?</span></span> <span data-ttu-id="940b9-108">โปรดดู[ส่งออกรายงานที่มีการแบ่งหน้า Power BI ด้วย Power Automate](service-automate-paginated-integration.md)</span><span class="sxs-lookup"><span data-stu-id="940b9-108">See [Export Power BI paginated reports with Power Automate](service-automate-paginated-integration.md).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="940b9-109">สิ่งที่จำเป็นต้องมี</span><span class="sxs-lookup"><span data-stu-id="940b9-109">Prerequisites</span></span>  

<span data-ttu-id="940b9-110">เพื่อดำเนินการต่อไป คุณควรตรวจสอบให้แน่ใจว่าคุณมีรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="940b9-110">To follow along, make sure you have:</span></span>

- <span data-ttu-id="940b9-111">พื้นที่ทำงานในผู้เช่า Power BI ของคุณที่ได้รับการสนับสนุนจากความจุที่สงวนไว้อย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="940b9-111">At least one workspace in your Power BI tenant backed by a reserved capacity.</span></span> <span data-ttu-id="940b9-112">ความจุนี้สามารถเป็น SKU ใดก็ได้ตั้งแต่ A4/P1 – A6/P3</span><span class="sxs-lookup"><span data-stu-id="940b9-112">This capacity can be any of the A4/P1 – A6/P3 SKUs.</span></span> <span data-ttu-id="940b9-113">อ่านข้อมูลเพิ่มเติมเกี่ยวกับ[ความจุสำรองสำหรับรายงานที่มีการแบ่งหน้าใน Power BI Premium](../admin/service-premium-what-is.md#paginated-reports)</span><span class="sxs-lookup"><span data-stu-id="940b9-113">Read more about [reserved capacities for paginated reports in Power BI Premium](../admin/service-premium-what-is.md#paginated-reports)</span></span>
- <span data-ttu-id="940b9-114">เข้าถึงตัวเชื่อมต่อมาตรฐานใน Power Automate ซึ่งมาพร้อมกับการสมัครใช้งาน Office 365</span><span class="sxs-lookup"><span data-stu-id="940b9-114">Access to the standard connectors in Power Automate, which come with any Office 365 subscription.</span></span>

## <a name="save-a-paginated-report-to-onedrive-for-business-or-a-sharepoint-online-folder"></a><span data-ttu-id="940b9-115">บันทึกรายงานที่มีการแบบแบ่งหน้าไปยัง OneDrive for Business หรือโฟลเดอร์ SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="940b9-115">Save a paginated report to OneDrive for Business or a SharePoint Online folder</span></span> 

<span data-ttu-id="940b9-116">คุณสามารถตั้งค่าการส่งออกรายงานที่มีการแบ่งหน้าที่เกิดขึ้นประจำในรูปแบบที่ต้องการไปยัง OneDrive for Business หรือโฟลเดอร์ SharePoint Online ได้ด้วยหนึ่งในเทมเพลตเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="940b9-116">With either of these templates, you set up recurring exports of a paginated report in a desired format to OneDrive for Business or a SharePoint Online folder.</span></span> <span data-ttu-id="940b9-117">ดูข้อกำหนดเบื้องต้นถ้าคุณใช้งานการดำเนินการส่งออกรายงานที่มีการแบ่งหน้าไปยังไฟล์ในโฟลว์ Power Automate เป็นครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="940b9-117">See the prerequisites if this is your first time using the Export to File for Paginated Reports action in a Power Automate flow.</span></span> 

> [!NOTE]
> <span data-ttu-id="940b9-118">ขั้นตอนและรูปภาพต่อไปนี้แสดงการตั้งค่าโฟลว์โดยใช้เทมเพลต **บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยัง OneDrive for Business**</span><span class="sxs-lookup"><span data-stu-id="940b9-118">The following steps and images show setting up a flow using the **Save a Power BI paginated report to OneDrive for Business** template.</span></span> <span data-ttu-id="940b9-119">ทำตามขั้นตอนเดียวกันนี้เพื่อสร้างโฟลว์โดยใช้เทมเพลต **บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยังโฟลเดอร์ SharePoint Online**</span><span class="sxs-lookup"><span data-stu-id="940b9-119">Follow the same steps to create a flow using the **Save a Power BI paginated report to a SharePoint Online folder** template.</span></span> <span data-ttu-id="940b9-120">เมื่อเลือกตำแหน่งที่คุณต้องการส่งออกรายงานที่มีการแบ่งหน้าของคุณ ให้เลือกโฟลเดอร์ SharePoint Online แทนที่จะเป็นโฟลเดอร์ OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="940b9-120">When selecting where you want to export your paginated report, select a SharePoint Online folder instead of a OneDrive for Business folder.</span></span> 

1. <span data-ttu-id="940b9-121">ลงชื่อเข้าใช้ Power Automate [flow.microsoft.com](https://flow.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="940b9-121">Sign in to Power Automate [flow.microsoft.com](https://flow.microsoft.com/).</span></span> 
1. <span data-ttu-id="940b9-122">เลือก **เทมเพลต** และค้นหา  **รายงานที่มีการแบ่งหน้า**</span><span class="sxs-lookup"><span data-stu-id="940b9-122">Select **Templates**, and search for **paginated reports**.</span></span> 

    :::image type="content" source="media/service-automate-paginated-integration/power-bi-paginate-automate.png" alt-text="สกรีนช็อตของเทมเพลต Power Automate อื่น ๆ สำหรับรายงานที่มีการแบ่งหน้า Power BI":::

1. <span data-ttu-id="940b9-124">เลือก **บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยัง OneDrive for Business** หรือ **บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยังโฟลเดอร์ SharePoint Online**</span><span class="sxs-lookup"><span data-stu-id="940b9-124">Select **Save a Power BI paginated report to OneDrive for Business** or **Save a Power BI paginated report to a SharePoint Online folder**.</span></span> <span data-ttu-id="940b9-125">ตรวจสอบให้แน่ใจว่าคุณได้ลงชื่อเข้าใช้ Power BI และ OneDrive for Business หรือ SharePoint Online แล้ว</span><span class="sxs-lookup"><span data-stu-id="940b9-125">Make sure you're signed into Power BI and OneDrive for Business or SharePoint Online.</span></span>

    :::image type="content" source="media/service-automate-paginated-onedrive-sharepoint/onedrive-template-step1.png" alt-text="สกรีนช็อตของการเลือกเทมเพลต Power BI และ OneDrive for Business":::
1. <span data-ttu-id="940b9-127">เลือก **ดำเนินต่อ**</span><span class="sxs-lookup"><span data-stu-id="940b9-127">Select **Continue**.</span></span>  


1. <span data-ttu-id="940b9-128">เมื่อต้องการตั้งค่า **การเกิดซ้ำ** สำหรับโฟลว์ของคุณ ให้เลือกตัวเลือกใน **ความถี่** และป้อนค่า **ช่วงเวลา** ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="940b9-128">To set the **Recurrence** for your flow, select an option in **Frequency** and enter a desired **Interval** value.</span></span>

    :::image type="content" source="media/service-automate-paginated-onedrive-sharepoint/onedrive-template-2-recurrence.png" alt-text="การเลือกการเกิดซ้ำสำหรับโฟลว์":::

1. <span data-ttu-id="940b9-130">(ไม่บังคับ) เลือก **แสดงตัวเลือกขั้นสูง** เพื่อตั้งค่าพารามิเตอร์ **การเกิดซ้ำ** เพิ่มเติม รวมถึง **เขตเวลา** **เวลาเริ่มต้น** **ในเหล่าวันนี้** **ในชั่วโมงเหล่านี้** และ **ในนาทีเหล่านี้**</span><span class="sxs-lookup"><span data-stu-id="940b9-130">(Optional) Select **Show advanced options** to set additional **Recurrence** parameters, including **Time zone**, **Start time**, **On these days**, **At these hours**, and **At these minutes**.</span></span>  

    :::image type="content" source="media/service-automate-paginated-onedrive-sharepoint/onedrive-template-3-advanced-recurrence.png" alt-text="แสดงตัวเลือกขั้นสูงสำหรับการเกิดซ้ำ":::

1. <span data-ttu-id="940b9-132">ในกล่อง **พื้นที่ทำงาน** ให้เลือกพื้นที่ทำงานในความจุที่สงวนไว้</span><span class="sxs-lookup"><span data-stu-id="940b9-132">In the **Workspace** box, select a workspace in a reserved capacity.</span></span> <span data-ttu-id="940b9-133">ในกล่อง **รายงาน** ให้เลือกรายงานที่มีการแบ่งหน้าในพื้นที่ทำงานที่คุณต้องการส่งออก</span><span class="sxs-lookup"><span data-stu-id="940b9-133">In the **Report** box, select the paginated report in the selected workspace you wish to export.</span></span> <span data-ttu-id="940b9-134">ในกล่อง **รูปแบบการส่งออก** ให้เลือกรูปแบบการส่งออกที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="940b9-134">In the **Export Format** box, select the desired export format.</span></span> <span data-ttu-id="940b9-135">อีกทางหนึ่งคือคุณสามารถระบุพารามิเตอร์สำหรับรายงานที่มีการแบ่งหน้าได้</span><span class="sxs-lookup"><span data-stu-id="940b9-135">Optionally, you can specify parameters for the paginated report.</span></span> <span data-ttu-id="940b9-136">ค้นหาคำอธิบายโดยละเอียดของพารามิเตอร์ใน[การอ้างอิงตัวเชื่อมต่อสำหรับ Power BI REST API](/connectors/powerbi/#export-to-file-for-paginated-reports)</span><span class="sxs-lookup"><span data-stu-id="940b9-136">Find detailed descriptions of the parameters in the [connector reference for the Power BI REST API](/connectors/powerbi/#export-to-file-for-paginated-reports).</span></span>  

    :::image type="content" source="media/service-automate-paginated-onedrive-sharepoint/onedrive-template-4-export-format.png" alt-text="เลือกรายงานที่มีการแบ่งหน้า พื้นที่ทำงาน และรูปแบบการส่งออก":::

1. <span data-ttu-id="940b9-138">ใน **เส้นทางโฟลเดอร์** ให้เลือกโฟลเดอร์ OneDrive for Business หรือ SharePoint Online ที่คุณต้องการส่งออกรายงานที่มีการแบ่งหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="940b9-138">In **Folder Path**, select the OneDrive for Business or SharePoint Online folder where you want to export your paginated report.</span></span>

    :::image type="content" source="media/service-automate-paginated-onedrive-sharepoint/onedrive-template-5-create-file.png" alt-text="เลือกปลายทางและสร้างไฟล์":::

1. <span data-ttu-id="940b9-140">Power Automate จะสร้าง **ชื่อไฟล์** และ **เนื้อหาไฟล์** ให้คุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="940b9-140">Power Automate automatically generates a **File Name** and **File Content** for you.</span></span> <span data-ttu-id="940b9-141">คุณสามารถเปลี่ยนชื่อไฟล์ได้ แต่คงค่า **เนื้อหาไฟล์** ที่สร้างขึ้นแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="940b9-141">You can change the file name, but keep the dynamically generated **File Content** value.</span></span> 

1. <span data-ttu-id="940b9-142">เมื่อคุณดำเนินการเสร็จแล้ว ให้เลือก  **ขั้นตอนถัดไป** หรือ **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="940b9-142">When you're done, select  **Next step** or **Save**.</span></span> <span data-ttu-id="940b9-143">Power Automate สร้างและประเมินโฟลว์ และแจ้งให้คุณทราบว่าพบข้อผิดพลาดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="940b9-143">Power Automate creates and evaluates the flow, and lets you know if it finds errors.</span></span> 

1. <span data-ttu-id="940b9-144">ถ้ามีข้อผิดพลาด ให้เลือก **แก้ไขโฟลว์** เพื่อแก้ไขโฟลว์เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="940b9-144">If there are errors, select **Edit flow** to fix them.</span></span> <span data-ttu-id="940b9-145">มิฉะนั้น ให้เลือกลูกศร **ย้อนกลับ** เพื่อดูรายละเอียดโฟลว์และเรียกใช้โฟลว์ใหม่</span><span class="sxs-lookup"><span data-stu-id="940b9-145">Otherwise, select the **Back** arrow to view the flow details and run the new flow.</span></span> 

    <span data-ttu-id="940b9-146">เมื่อคุณเรียกใช้โฟลว์ Power Automate จะส่งออกรายงานที่มีการแบ่งหน้าในรูปแบบที่ระบุไปยัง OneDrive for Business หรือ SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="940b9-146">When you run the flow, Power Automate exports a paginated report in the specified format to OneDrive for Business or SharePoint Online.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="940b9-147">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="940b9-147">Next steps</span></span>

- [<span data-ttu-id="940b9-148">ส่งออกรายงานที่มีการแบ่งหน้า Power BI ด้วย Power Automate</span><span class="sxs-lookup"><span data-stu-id="940b9-148">Export Power BI paginated reports with Power Automate</span></span>](service-automate-paginated-integration.md)
- [<span data-ttu-id="940b9-149">เริ่มต้นใช้งาน Power Automate</span><span class="sxs-lookup"><span data-stu-id="940b9-149">Get started with Power Automate</span></span>](/power-automate/getting-started/)
- <span data-ttu-id="940b9-150">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="940b9-150">More questions?</span></span> [<span data-ttu-id="940b9-151">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="940b9-151">Try the Power BI Community</span></span>](https://community.powerbi.com/)
