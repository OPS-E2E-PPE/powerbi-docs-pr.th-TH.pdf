---
title: ดูพารามิเตอร์สำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI
description: ในบทความนี้ คุณจะได้เรียนรู้วิธีการโต้ตอบกับพารามิเตอร์สำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: maggies
ms.service: powerbi
ms.subservice: pbi-explore
ms.topic: how-to
ms.date: 09/28/2020
ms.openlocfilehash: db5e9ed91a61c26e9b118086ff6d970ebcc3306a
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415208"
---
# <a name="view-parameters-for-paginated-reports-in-the-power-bi-service"></a><span data-ttu-id="acf08-103">ดูพารามิเตอร์สำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="acf08-103">View parameters for paginated reports in the Power BI service</span></span>

<span data-ttu-id="acf08-104">ในบทความนี้ คุณจะได้เรียนรู้วิธีการโต้ตอบกับพารามิเตอร์สำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="acf08-104">In this article, you learn how to interact with parameters for paginated reports in the Power BI service.</span></span>  <span data-ttu-id="acf08-105">พารามิเตอร์รายงานจะให้วิธีการกรองข้อมูลรายงาน</span><span class="sxs-lookup"><span data-stu-id="acf08-105">A report parameter provides a way to filter report data.</span></span> <span data-ttu-id="acf08-106">พารามิเตอร์เสนอรายการค่าที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="acf08-106">Parameters offer a list of available values.</span></span> <span data-ttu-id="acf08-107">คุณสามารถเลือกค่าหนึ่งหรือหลายค่าหรือพิมพ์ในกล่องข้อความพารามิเตอร์เพื่อค้นหาค่า</span><span class="sxs-lookup"><span data-stu-id="acf08-107">You can choose one or many values, or type in a parameter text box to search for values.</span></span> <span data-ttu-id="acf08-108">บางครั้งพารามิเตอร์มีค่าเริ่มต้น และบางครั้งคุณต้องเลือกค่าก่อนคุณจึงจะเห็นรายงาน</span><span class="sxs-lookup"><span data-stu-id="acf08-108">Sometimes parameters have a default value, and sometimes you have to choose a value before you see the report.</span></span>  

<span data-ttu-id="acf08-109">เมื่อคุณดูรายงานที่มีพารามิเตอร์ แถบเครื่องมือตัวแสดงรายงานจะแสดงพารามิเตอร์แต่ละตัว เพื่อให้คุณระบุค่าได้แบบโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="acf08-109">When you view a report that has parameters, the report viewer toolbar displays each parameter so you can interactively specify values.</span></span> <span data-ttu-id="acf08-110">ภาพประกอบต่อไปนี้จะแสดงพื้นที่พารามิเตอร์สำหรับรายงานที่มีพารามิเตอร์สำหรับ **กลุ่มการซื้อ**, **พื้นที่**, **จากวันที่** และ **ไปยังวันที่**</span><span class="sxs-lookup"><span data-stu-id="acf08-110">The following illustration shows the parameter area for a report with parameters for **Buying Group**, **Location**, a **From Date**, and a **To Date**.</span></span>  

## <a name="parameters-pane-in-the-power-bi-service"></a><span data-ttu-id="acf08-111">แผงพารามิเตอร์ในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="acf08-111">Parameters pane in the Power BI service</span></span>

![ดูรายงานแบบแบ่งหน้าที่มีพารามิเตอร์](media/paginated-reports-view-parameters/power-bi-paginated-view-parameters.png)
  
1.  <span data-ttu-id="acf08-113">**แผงพารามิเตอร์** แถบเครื่องมือตัวดูรายงานจะแสดงการแจ้งเตือนเช่น "จำเป็น" หรือค่าเริ่มต้นสำหรับพารามิเตอร์แต่ละตัว</span><span class="sxs-lookup"><span data-stu-id="acf08-113">**Parameters pane** The report viewer toolbar displays a prompt such as "Required" or a default value for each parameter.</span></span>    
  
2.  <span data-ttu-id="acf08-114">**พารามิเตอร์ใบแจ้งหนี้ตั้งแต่วันที่ / ถึงวันที่** พารามิเตอร์วันที่สองตัวมีค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="acf08-114">**Invoices From / To Date parameters** The two date parameters have default values.</span></span> <span data-ttu-id="acf08-115">พิมพ์วันที่ในกล่องข้อความหรือเลือกวันที่จากปฏิทินเพื่อเปลี่ยนวันที่</span><span class="sxs-lookup"><span data-stu-id="acf08-115">To change the date, type a date in the text box or choose a date in the calendar.</span></span>  
  
3.  <span data-ttu-id="acf08-116">**พารามิเตอร์ตำแหน่ง** พารามิเตอร์ตำแหน่งได้รับการตั้งค่าเพื่อให้คุณได้เลือกค่าหนึ่งค่า หลายค่า หรือค่าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="acf08-116">**Location parameter** The Location parameter is set to allow you to select one, many, or all values.</span></span> 
  
4.  <span data-ttu-id="acf08-117">**ดูรายงาน** หลังจากที่คุณใส่หรือเปลี่ยนค่าพารามิเตอร์ ให้คลิกที่ **ดูรายงาน** เพื่อเรียกใช้รายงาน</span><span class="sxs-lookup"><span data-stu-id="acf08-117">**View Report**  After you enter or change parameter values, click **View Report** to run the report.</span></span> 

5. <span data-ttu-id="acf08-118">**ค่าเริ่มต้น** ถ้าพารามิเตอร์ทั้งหมดมีค่าเริ่มต้น รายงานจะทำงานอัตโนมัติในการดูครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="acf08-118">**Default values** If all parameters have default values, the report runs automatically on first view.</span></span> <span data-ttu-id="acf08-119">พารามิเตอร์บางตัวในรายงานนี้ไม่มีค่าเริ่มต้น คุณจึงจะไม่เห็นรายงานจนกว่าคุณจะเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="acf08-119">Some parameters in this report didn't have default values, so you don't see the report until you select values.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="acf08-120">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="acf08-120">Next steps</span></span>

[<span data-ttu-id="acf08-121">รายงานที่มีการแบ่งหน้าในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="acf08-121">Paginated reports in the Power BI service</span></span>](end-user-paginated-report.md)
