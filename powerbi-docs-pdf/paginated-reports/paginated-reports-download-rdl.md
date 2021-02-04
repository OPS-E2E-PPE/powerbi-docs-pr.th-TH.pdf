---
title: ดาวน์โหลด .rdl สำหรับรายงานแบบแบ่งหน้าจากชุดข้อมูล
description: ในบทความนี้คุณจะได้เรียนรู้วิธีสร้าง .rdl สำหรับรายงานที่มีการแบ่งหน้าของ Power BI โดยการดาวน์โหลดจากชุดข้อมูลที่แชร์ในบริการ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: swgupt
ms.service: powerbi
ms.subservice: report-builder
ms.topic: how-to
ms.date: 10/15/2020
ms.openlocfilehash: c5c8f61a7253da46529a83276366044560d4f030
ms.sourcegitcommit: ccf53e87ff7cba1fcd9d2cca761a561e62933f90
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/04/2020
ms.locfileid: "93297615"
---
# <a name="download-the-rdl-for-a-power-bi-paginated-report-from-a-dataset"></a><span data-ttu-id="c17c2-103">ดาวน์โหลด .rdl สำหรับรายงานแบบแบ่งหน้าของ Power BI จากชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c17c2-103">Download the .rdl for a Power BI paginated report from a dataset</span></span>

<span data-ttu-id="c17c2-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span><span class="sxs-lookup"><span data-stu-id="c17c2-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span></span> 

<span data-ttu-id="c17c2-105">ในบทความนี้คุณจะได้เรียนรู้วิธีสร้าง .rdl สำหรับรายงานที่มีการแบ่งหน้าของ Power BI โดยการดาวน์โหลดจากชุดข้อมูลที่แชร์ในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="c17c2-105">In this article, you learn how to create the .rdl for a Power BI paginated report by downloading from a shared dataset in the Power BI service.</span></span> <span data-ttu-id="c17c2-106">รายงานแบบแบ่งหน้าอยู่ในรูปแบบไฟล์ *.rdl*</span><span class="sxs-lookup"><span data-stu-id="c17c2-106">Paginated reports have the file format *.rdl*.</span></span> <span data-ttu-id="c17c2-107">คุณสามารถสร้างไฟล์ .rdl ได้โดยตรงจากชุดข้อมูลใน Power BI service</span><span class="sxs-lookup"><span data-stu-id="c17c2-107">You can create an .rdl file directly from a  dataset in the Power BI service.</span></span>

1. <span data-ttu-id="c17c2-108">ไปที่มุมมองรายการสำหรับพื้นที่ทำงานใด ๆ รวมถึง My Workspace</span><span class="sxs-lookup"><span data-stu-id="c17c2-108">Go to list view for any workspace, including My Workspace.</span></span> 
1. <span data-ttu-id="c17c2-109">เลือก **ตัวเลือกเพิ่มเติม (...)** สำหรับชุดข้อมูล จากนั้นเลือก **ดาวน์โหลด .rdl**</span><span class="sxs-lookup"><span data-stu-id="c17c2-109">Select **More options (...)** for a dataset, then select **Download the .rdl**.</span></span>

    :::image type="content" source="media/paginated-reports-download-rdl/power-bi-paginated-download-rdl.png" alt-text="สกรีนช็อตของตัวเลือกดาวน์โหลด .rdl ใน Power BI service":::
1. <span data-ttu-id="c17c2-111">คุณจะเห็นข้อความที่ระบุว่าคุณจำเป็นต้องอัปเดต Power BI Report Builder</span><span class="sxs-lookup"><span data-stu-id="c17c2-111">You see a message that you need some Power BI Report Builder updates.</span></span> <span data-ttu-id="c17c2-112">เลือก **ดาวน์โหลด**</span><span class="sxs-lookup"><span data-stu-id="c17c2-112">Select **Download**.</span></span> 

    :::image type="content" source="media/paginated-reports-download-rdl/power-bi-report-builder-updates.png" alt-text="สกรีนช็อตของการติดตั้งอัปเดต Power BI Report Builder":::

    <span data-ttu-id="c17c2-114">หากคุณทราบว่าคุณมี Power BI Report Builder รุ่นล่าสุด ให้เลือก **ฉันติดตั้งอัปเดตเหล่านี้ไปแล้ว**</span><span class="sxs-lookup"><span data-stu-id="c17c2-114">If you know you have the most recent version of Power BI Report Builder, select **I've already installed these updates**.</span></span>

1. <span data-ttu-id="c17c2-115">ไปยังกระบวนการติดตั้ง Power BI Report Builder:</span><span class="sxs-lookup"><span data-stu-id="c17c2-115">Go through the Power BI Report Builder installation process:</span></span> 

    1. <span data-ttu-id="c17c2-116">เลือก **ดาวน์โหลด**</span><span class="sxs-lookup"><span data-stu-id="c17c2-116">Select **Download**.</span></span>  
    2. <span data-ttu-id="c17c2-117">เลือก **เปิดไฟล์** และทำตามขั้นตอนในตัวช่วยติดตั้ง Power BI Report Builder</span><span class="sxs-lookup"><span data-stu-id="c17c2-117">Select **Open file** and go through the steps in the Power BI Report Builder Setup Wizard.</span></span>

1. <span data-ttu-id="c17c2-118">เมื่อการติดตั้ง Report Builder เสร็จสิ้น ให้ย้อนกลับไปยัง Power BI service และเลือก **ดาวน์โหลด .rdl**</span><span class="sxs-lookup"><span data-stu-id="c17c2-118">When the Report Builder installation is finished, go back to the Power BI service and select **Download the .rdl**.</span></span>

    :::image type="content" source="media/paginated-reports-download-rdl/power-bi-report-builder-finished-installing.png" alt-text="สกรีนช็อตของกล่องข้อความดาวน์โหลด .rdl":::

1. <span data-ttu-id="c17c2-120">เลือก **เปิดไฟล์** ในหน้าต่างเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="c17c2-120">Select **Open file** in the browser window.</span></span>

    :::image type="content" source="media/paginated-reports-download-rdl/power-bi-paginated-open-file.png" alt-text="สกรีนช็อตของการเลือกเปิดไฟล์ในเบราว์เซอร์":::

1. <span data-ttu-id="c17c2-122">Power BI Report Builder จะเปิดโดยใช้ชื่อที่สร้างโดยอัตโนมัติ และไฟล์ Power BI dataset.pbix ในโฟลเดอร์ **แหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="c17c2-122">Power BI Report Builder opens with an automatically generated title, and the Power BI dataset .pbix file in the **Data Sources** folder.</span></span> <span data-ttu-id="c17c2-123">แหล่งข้อมูลมีชื่อเดียวกับชุดข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="c17c2-123">The data source has the same name as the Power BI dataset.</span></span>

    :::image type="content" source="media/paginated-reports-download-rdl/power-bi-report-builder-design-canvas.png" alt-text="สกรีนช็อตของ Power BI Report Builder ในมุมมอง Design":::

    <span data-ttu-id="c17c2-125">พื้นผิวการออกแบบยังมีลิงก์ที่นำไปยังหลักสูตรวิดีโอ [รายงานที่มีการแบ่งหน้าของ Power BI ในหนึ่งวัน](../learning-catalog/paginated-reports-online-course.md)</span><span class="sxs-lookup"><span data-stu-id="c17c2-125">The design surface also features a link to the [Power BI Paginated Reports in a Day](../learning-catalog/paginated-reports-online-course.md) video-based course.</span></span> <span data-ttu-id="c17c2-126">หากคุณยังไม่คุ้นเกคยกับการสร้างรายงานที่มีการแบ่งหน้า หลักสูตรนี้จะช่วยเพิ่มทักษะของคุณ</span><span class="sxs-lookup"><span data-stu-id="c17c2-126">If you're new to paginated report creation, the course is a good way to get up to speed.</span></span>  <span data-ttu-id="c17c2-127">สามารถลบเมื่อคุณเริ่มออกแบบรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="c17c2-127">You can delete it when you start designing your report.</span></span>

    <span data-ttu-id="c17c2-128">คุณพร้อมที่จะเริ่มออกแบบรายงานที่มีการแบ่งหน้าของคุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="c17c2-128">You're ready to start designing your paginated report.</span></span>
 
## <a name="next-steps"></a><span data-ttu-id="c17c2-129">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c17c2-129">Next steps</span></span> 

- [<span data-ttu-id="c17c2-130">รายงานแบบแบ่งหน้าใน Power BI Premium คืออะไร</span><span class="sxs-lookup"><span data-stu-id="c17c2-130">What are paginated reports in Power BI Premium?</span></span>](paginated-reports-report-builder-power-bi.md)  
- [<span data-ttu-id="c17c2-131">บทช่วยสอน: สร้างรายงานแบบแบ่งหน้าและอัปโหลดไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="c17c2-131">Tutorial: Create a paginated report and upload it to the Power BI service</span></span>](paginated-reports-quickstart-aw.md)
- [<span data-ttu-id="c17c2-132">เผยแพร่รายงานแบบแบ่งหน้าไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="c17c2-132">Publish a paginated report to the Power BI service</span></span>](paginated-reports-save-to-power-bi-service.md)

