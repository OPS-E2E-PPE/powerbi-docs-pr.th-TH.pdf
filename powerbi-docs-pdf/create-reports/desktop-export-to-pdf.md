---
title: ส่งรายงานของคุณเป็นรูปแบบ PDF จาก Power BI Desktop
description: ส่งออกเป็น PDF ได้อย่างง่ายดายจาก Power BI Desktop และพิมพ์รายงาน PDF เหล่านั้นได้อย่างง่ายดาย
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 02/28/2019
LocalizationGroup: Create reports
ms.openlocfilehash: 815b8557b640de70690dcb90570f7764ff8c47a0
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413000"
---
# <a name="export-reports-to-pdf-from-power-bi-desktop"></a><span data-ttu-id="4c38a-103">ส่งออกรายงานเป็น PDF จาก Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4c38a-103">Export reports to PDF from Power BI Desktop</span></span>
<span data-ttu-id="4c38a-104">ใน **Power BI Desktop** หรือ บริการ Power BI คุณสามารถส่งออกรายงานไปยังไฟล์ PDF และดังนั้นจึงได้อย่างง่ายดายแชร์ หรือพิมพ์รายงานของคุณจาก PDF นั้นได้</span><span class="sxs-lookup"><span data-stu-id="4c38a-104">In **Power BI Desktop** or the Power BI service, you can export reports to a PDF file, and thereby easily share or print your reports from that PDF.</span></span>

![ส่งออกเป็น PDF](media/desktop-export-to-pdf/export-to-pdf_01.png)

<span data-ttu-id="4c38a-106">กระบวนการส่งออกรายงานของคุณจาก **Power BI Desktop** เป็น PDF เป็นเรื่องไม่ยุ่งยาก เพื่อให้คุณสามารถพิมพ์เป็น PDF หรือแชร์เอกสาร PDF นั้นกับผู้อื่น</span><span class="sxs-lookup"><span data-stu-id="4c38a-106">The process of exporting your report from **Power BI Desktop** to a PDF, so that you can print the PDF or share that PDF document with others, is straightforward.</span></span> <span data-ttu-id="4c38a-107">เพียงแค่เลือก **ไฟล์ > ส่งออกเป็น PDF** จาก Power BI Deskop</span><span class="sxs-lookup"><span data-stu-id="4c38a-107">Simply select **File > Export to PDF** from Power BI Desktop.</span></span>

<span data-ttu-id="4c38a-108">กระบวนการ **ส่งออกเป็น PDF** จะส่งออกหน้าในรายงาน *ที่เห็น* ทั้งหมด พร้อมกับแต่ละหน้ารายงานที่ส่งออกเป็นหน้าเดียวใน PDF</span><span class="sxs-lookup"><span data-stu-id="4c38a-108">The **Export to PDF** process will export all *visible* pages in the report, with each report page exporting to a single page in the PDF.</span></span> <span data-ttu-id="4c38a-109">หน้ารายงานที่ไม่สามารถมองเห็นได้ในขณะนี้ เช่น หน้าคำแนะนำเครื่องมือหรือหน้าที่ซ่อน จะไม่ถูกส่งออกเป็นไฟล์ PDF</span><span class="sxs-lookup"><span data-stu-id="4c38a-109">Report pages that are currently not visible, such as any tooltips or hidden pages, are not exported to the PDF file.</span></span> 

![กำลังส่งออกเป็น PDF](media/desktop-export-to-pdf/export-to-pdf_02.png)

<span data-ttu-id="4c38a-111">เมื่อคุณเลือก **ไฟล์ > ส่งออกเป็น PDF** การส่งออกจะเริ่มขึ้น และกล่องโต้ตอบจะปรากฏขึ้นเพื่อแสดงกระบวนการส่งออกอยู่ในระหว่างดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="4c38a-111">When you select **File > Export to PDF** the export is initiated, and a dialog appears that shows the export process is underway.</span></span> <span data-ttu-id="4c38a-112">กล่องโต้ตอบยังคงอยู่บนหน้าจอจนกว่ากระบวนการส่งออกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4c38a-112">The dialog remains on the screen until the export process completes.</span></span> <span data-ttu-id="4c38a-113">ในระหว่างกระบวนการส่งออก การโต้ตอบกับรายงานที่จะถูกส่งออกทั้งหมดถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4c38a-113">During the export process, all interaction with the report being exported is disabled.</span></span> <span data-ttu-id="4c38a-114">วิธีเดียวที่จะโต้ตอบกับรายงานได้ คือ ต้องรอจนกว่ากระบวนการส่งออกเสร็จสมบูรณ์ หรือยกเลิกการส่งออก</span><span class="sxs-lookup"><span data-stu-id="4c38a-114">The only way to interact with the report is to wait until the export process completes, or to cancel the export.</span></span> 

<span data-ttu-id="4c38a-115">เมื่อการส่งออกเสร็จสมบูรณ์ PDF จะถูกโหลดลงในตัวแสดง PDF เริ่มต้นบนคอมพิวเตอร์</span><span class="sxs-lookup"><span data-stu-id="4c38a-115">When the export completes, the PDF is loaded into the default PDF viewer on the computer.</span></span> 

## <a name="considerations-and-limitations"></a><span data-ttu-id="4c38a-116">ข้อควรพิจารณาและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="4c38a-116">Considerations and limitations</span></span>
<span data-ttu-id="4c38a-117">มีข้อควรพิจารณาสองสามอย่างที่ควรคำนึงถึงกับคุณลักษณะ **การส่งออกเป็น PDF**:</span><span class="sxs-lookup"><span data-stu-id="4c38a-117">There are a few considerations to keep in mind with the **Export to PDF** feature:</span></span>

* <span data-ttu-id="4c38a-118">คุณลักษณะจะส่งออกวิชวล Power BI แต่ *ไม่* ส่งออกรูปพื้นหลังใด ๆ ที่คุณอาจใช้กับรายงาน</span><span class="sxs-lookup"><span data-stu-id="4c38a-118">The feature does export Power BI visuals, but it does *not* export any wallpaper you may have applied to the report.</span></span>

<span data-ttu-id="4c38a-119">เนื่องจากรูปพื้นหลังจะถูกส่งออกเป็น PDF คุณควรใส่ใจรายงานที่ใช้รูปพื้นหลังสีเข้มเป็นพิเศษ</span><span class="sxs-lookup"><span data-stu-id="4c38a-119">Since wallpaper is not exported to the PDF, you should pay special attention to reports that use dark wallpaper.</span></span> <span data-ttu-id="4c38a-120">ถ้าข้อความในรายงานของคุณเป็นสีขาวหรือสีอ่อนเพื่อให้โดดเด่นกับรูปพื้นหลังสีเข้มของคุณ จะสามารถอ่านได้ยากหรือไม่สามารถอ่านได้ในกระบวนการส่งออกเป็น PDF เนื่องจากรูปพื้นหลังจะไม่ถูกส่งออกไปกับรายงานที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="4c38a-120">If the text in your report is light or white, to have it stand out against your dark wallpaper, it will be difficult to read or unreadable in the export to PDF process since the wallpaper will not be exported with the rest of the report.</span></span> 



## <a name="next-steps"></a><span data-ttu-id="4c38a-121">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4c38a-121">Next steps</span></span>
<span data-ttu-id="4c38a-122">มีหลายองค์ประกอบภาพและคุณลักษณะใน **Power BI Desktop** ที่น่าสนใจ</span><span class="sxs-lookup"><span data-stu-id="4c38a-122">There are all sorts of interesting visual elements and features in **Power BI Desktop**.</span></span> <span data-ttu-id="4c38a-123">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับข้อมูล โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4c38a-123">For more information in information, check out the following resources:</span></span>

* [<span data-ttu-id="4c38a-124">ใช้องค์ประกอบภาพเพื่อปรับปรุงรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="4c38a-124">Use visual elements to enhance Power BI reports</span></span>](desktop-visual-elements-for-reports.md)
* [<span data-ttu-id="4c38a-125">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="4c38a-125">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
