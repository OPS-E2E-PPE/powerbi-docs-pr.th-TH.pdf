---
title: ส่งออกรายงานจนด้วย Power อัตโนมัติ
description: เรียนรู้วิธีการสร้างโฟลว์ Power Automate เพื่อส่งออกรายงานที่มีการแบ่งหน้า Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 12/14/2020
LocalizationGroup: Get started
ms.openlocfilehash: 5c69abe925751e8b065f262e151bfee65c487238
ms.sourcegitcommit: 46cf62d9bb33ac7b7eae7910fbba6756f626c65f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/15/2020
ms.locfileid: "97492069"
---
# <a name="export-power-bi-paginated-reports-with-power-automate"></a><span data-ttu-id="645b8-103">ส่งออกรายงานที่มีการแบ่งหน้า Power BI ด้วย Power Automate</span><span class="sxs-lookup"><span data-stu-id="645b8-103">Export Power BI paginated reports with Power Automate</span></span>

<span data-ttu-id="645b8-104">ด้วย [Power Automate](/power-automate/getting-started) คุณสามารถทำให้การส่งออกและการแจกจ่ายรายงานที่มีการแบ่งหน้า Power BI ไปยังรูปแบบและสถานการณ์ที่ได้รับการสนับสนุนเป็นแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="645b8-104">With [Power Automate](/power-automate/getting-started), you can automate exporting and distributing Power BI paginated reports to a variety of supported formats and scenarios.</span></span> <span data-ttu-id="645b8-105">ในบทความนี้ คุณจะได้เรียนรู้ว่าเทมเพลตใดบ้างที่จะใช้สร้างโฟลว์ของคุณเองเพื่อส่งออกรายงานที่มีการแบ่งหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="645b8-105">In this article, you learn which templates to use to build your own flows to export your paginated reports.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="645b8-106">สิ่งที่จำเป็นต้องมี</span><span class="sxs-lookup"><span data-stu-id="645b8-106">Prerequisites</span></span>  

<span data-ttu-id="645b8-107">เพื่อดำเนินการต่อไป คุณควรตรวจสอบให้แน่ใจว่าคุณมีรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="645b8-107">To follow along, make sure you have:</span></span>

- <span data-ttu-id="645b8-108">พื้นที่ทำงานในผู้เช่า Power BI ของคุณที่ได้รับการสนับสนุนจากความจุที่สงวนไว้อย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="645b8-108">At least one workspace in your Power BI tenant backed by a reserved capacity.</span></span> <span data-ttu-id="645b8-109">ความจุนี้สามารถเป็น SKU ใดก็ได้ตั้งแต่ A4/P1 – A6/P3</span><span class="sxs-lookup"><span data-stu-id="645b8-109">This capacity can be any of the A4/P1 – A6/P3 SKUs.</span></span> <span data-ttu-id="645b8-110">อ่านเพิ่มเติมเกี่ยวกับ[ความจุที่สงวนไว้ใน Power BI Premium](../admin/service-premium-what-is.md)</span><span class="sxs-lookup"><span data-stu-id="645b8-110">Read more about [reserved capacities in Power BI Premium](../admin/service-premium-what-is.md).</span></span>
- <span data-ttu-id="645b8-111">เข้าถึงตัวเชื่อมต่อมาตรฐานใน Power Automate ซึ่งมาพร้อมกับการสมัครใช้งาน Office 365</span><span class="sxs-lookup"><span data-stu-id="645b8-111">Access to the standard connectors in Power Automate, which come with any Office 365 subscription.</span></span>

## <a name="create-a-flow-from-a-template"></a><span data-ttu-id="645b8-112">สร้างโฟลว์จากเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="645b8-112">Create a flow from a template</span></span> 

1. <span data-ttu-id="645b8-113">ลงชื่อเข้าใช้ Power Automate [flow.microsoft.com](https://flow.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="645b8-113">Sign in to Power Automate [flow.microsoft.com](https://flow.microsoft.com/).</span></span> 
1. <span data-ttu-id="645b8-114">เลือก **เทมเพลต** และค้นหา  **รายงานที่มีการแบ่งหน้า**</span><span class="sxs-lookup"><span data-stu-id="645b8-114">Select **Templates**, and search for **paginated reports**.</span></span> 

    :::image type="content" source="media/service-automate-paginated-integration/power-bi-paginate-automate.png" alt-text="สกรีนช็อตของเทมเพลต Power Automate อื่น ๆ สำหรับรายงานที่มีการแบ่งหน้า Power BI":::

## <a name="select-a-template"></a><span data-ttu-id="645b8-116">เลือกเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="645b8-116">Select a template</span></span> 

<span data-ttu-id="645b8-117">เลือกเทมเพลตจากรายการเพื่อเริ่มต้นใช้งานด้วยคำแนะนำทีละขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="645b8-117">Select a template from the list to get started with a step-by-step walkthrough.</span></span>  

- <span data-ttu-id="645b8-118">[บันทึกรายงานที่มีการแบบแบ่งหน้า Power BI ไปยัง OneDrive for Business หรือโฟลเดอร์ SharePoint Online](service-automate-paginated-onedrive-sharepoint.md)</span><span class="sxs-lookup"><span data-stu-id="645b8-118">[Save a Power BI paginated report to OneDrive for Business or a SharePoint Online folder](service-automate-paginated-onedrive-sharepoint.md).</span></span>  
- <span data-ttu-id="645b8-119">[ส่งออกรายงานที่มีการแบ่งหน้า Power BI สำหรับหน่วยข้อมูลในรายการ SharePoint Online หรือสำหรับแต่ละแถวในตาราง Excel Online](service-automate-paginated-excel-sharepoint-list.md)</span><span class="sxs-lookup"><span data-stu-id="645b8-119">[Export a Power BI paginated report for items in a SharePoint Online List, or for each row in an Excel Online table](service-automate-paginated-excel-sharepoint-list.md).</span></span>
- <span data-ttu-id="645b8-120">[บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยังโฟลเดอร์ระบบภายในเครื่อง](service-automate-paginated-local-file.md)</span><span class="sxs-lookup"><span data-stu-id="645b8-120">[Save a Power BI paginated report to a local system folder](service-automate-paginated-local-file.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="645b8-121">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="645b8-121">Next steps</span></span>

- <span data-ttu-id="645b8-122">[API การส่งออก Power BI สำหรับรายงานที่มีการแบ่งหน้า](../developer/embedded/export-paginated-report.md)</span><span class="sxs-lookup"><span data-stu-id="645b8-122">The [Power BI export API for paginated reports](../developer/embedded/export-paginated-report.md)</span></span>
- [<span data-ttu-id="645b8-123">เริ่มต้นใช้งาน Power Automate</span><span class="sxs-lookup"><span data-stu-id="645b8-123">Get started with Power Automate</span></span>](/power-automate/getting-started/)
- <span data-ttu-id="645b8-124">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="645b8-124">More questions?</span></span> [<span data-ttu-id="645b8-125">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="645b8-125">Try the Power BI Community</span></span>](https://community.powerbi.com/)
