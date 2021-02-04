---
title: สร้างพารามิเตอร์สำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI
description: ในบทความนี้ คุณจะได้เรียนวิธีการสร้างพารามิเตอร์สำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: report-builder
ms.topic: how-to
ms.date: 09/28/2020
ms.openlocfilehash: 7d874f2c9a7b8381ece151a4ac113bed5662c2e7
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418175"
---
# <a name="create-parameters-for-paginated-reports-in-the-power-bi-service"></a><span data-ttu-id="4d3a1-103">สร้างพารามิเตอร์สำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="4d3a1-103">Create parameters for paginated reports in the Power BI service</span></span>

<span data-ttu-id="4d3a1-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span><span class="sxs-lookup"><span data-stu-id="4d3a1-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span></span> 

<span data-ttu-id="4d3a1-105">ในบทความนี้ คุณจะได้เรียนวิธีการสร้างพารามิเตอร์สำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="4d3a1-105">In this article, you learn how to create parameters for paginated reports in the Power BI service.</span></span>  <span data-ttu-id="4d3a1-106">พารามิเตอร์ของรายงานให้วิธีการเลือกข้อมูลรายงานและทำให้การนำเสนอรายงานมีความหลากหลาย</span><span class="sxs-lookup"><span data-stu-id="4d3a1-106">A report parameter provides a way to choose report data and vary the report presentation.</span></span> <span data-ttu-id="4d3a1-107">คุณสามารถระบุค่าเริ่มต้นและรายการของค่าที่พร้อมใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="4d3a1-107">You can provide a default value and a list of available values.</span></span> <span data-ttu-id="4d3a1-108">ผู้อ่านรายงานของคุณสามารถเปลี่ยนแปลงรายการที่เลือกได้</span><span class="sxs-lookup"><span data-stu-id="4d3a1-108">Your report readers can change the selection.</span></span> <span data-ttu-id="4d3a1-109">นอกจากนี้ พวกเขายังสามารถพิมพ์ลงในกล่องข้อความพารามิเตอร์เพื่อค้นหาค่า</span><span class="sxs-lookup"><span data-stu-id="4d3a1-109">They can also type in the parameter text boxes to search for values.</span></span> <span data-ttu-id="4d3a1-110">ดูที่ [ดูพารามิเตอร์สำหรับรายงานที่มีการแบ่งหน้า](../consumer/paginated-reports-view-parameters.md) เพื่อดูว่า ผู้ใช้ทางธุรกิจของคุณโต้ตอบกับพารามิเตอร์ต่างๆ ในบริการของ Power BI อย่างไร</span><span class="sxs-lookup"><span data-stu-id="4d3a1-110">See [View parameters for paginated reports](../consumer/paginated-reports-view-parameters.md) to see how your business users interact with parameters in the Power BI service.</span></span>  

<span data-ttu-id="4d3a1-111">ภาพประกอบต่อไปนี้แสดงให้เห็นมุมมองออกแบบในตัวสร้างรายงาน Power BI สำหรับรายงานที่มีพารามิเตอร์ @BuyingGroup, @Customer, @FromDate และ @ToDate</span><span class="sxs-lookup"><span data-stu-id="4d3a1-111">The following illustration shows Design view in Power BI Report Builder for a report with the parameters @BuyingGroup, @Customer, @FromDate, and @ToDate.</span></span> 
  
![พารามิเตอร์ในตัวสร้างรายงาน](media/paginated-reports-parameters/power-bi-paginated-parameters-report-builder.png)
  
1.  <span data-ttu-id="4d3a1-113">พารามิเตอร์ของรายงานในแผงข้อมูลรายงาน</span><span class="sxs-lookup"><span data-stu-id="4d3a1-113">The report parameters in the Report Data pane.</span></span>  
  
2.  <span data-ttu-id="4d3a1-114">ตารางพร้อมพารามิเตอร์หนึ่งตัวในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4d3a1-114">The table with one of the parameters in the dataset.</span></span>  
  
3.  <span data-ttu-id="4d3a1-115">แผงพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="4d3a1-115">The Parameters pane.</span></span> <span data-ttu-id="4d3a1-116">คุณสามารถกำหนดเค้าโครงของพารามิเตอร์ในแผงพารามิเตอร์ได้</span><span class="sxs-lookup"><span data-stu-id="4d3a1-116">You can customize the layout of parameters in the parameters pane.</span></span> 
  
4.  <span data-ttu-id="4d3a1-117">พารามิเตอร์ @FromDate และ @ToDate มีประเภทข้อมูลเป็น **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4d3a1-117">The parameters @FromDate and @ToDate have the data type **DateTime**.</span></span> <span data-ttu-id="4d3a1-118">เมื่อดูรายงาน คุณสามารถพิมพ์วันที่ในกล่องข้อความหรือเลือกจากส่วนควบคุมปฏิทินได้</span><span class="sxs-lookup"><span data-stu-id="4d3a1-118">When viewing the report, you can either type a date in the text box or choose a date in the calendar control.</span></span> 

5.  <span data-ttu-id="4d3a1-119">พารามิเตอร์ตัวหนึ่งในกล่องโต้ตอบ **คุณสมบัติชุดข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="4d3a1-119">One of the parameters in the **Dataset Properties** dialog box.</span></span>  

  
## <a name="create-or-edit-a-report-parameter"></a><span data-ttu-id="4d3a1-120">สร้างหรือแก้ไขพารามิเตอร์ของรายงาน</span><span class="sxs-lookup"><span data-stu-id="4d3a1-120">Create or edit a report parameter</span></span>  
  
1.  <span data-ttu-id="4d3a1-121">เปิดรายงานแบบแบ่งหน้าในตัวสร้างรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="4d3a1-121">Open your paginated report in Power BI Report Builder.</span></span>

1. <span data-ttu-id="4d3a1-122">ที่แผง **ข้อมูลรายงาน** ให้คุณคลิกขวาที่โหนด **พารามิเตอร์** > **เพิ่มพารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="4d3a1-122">In the **Report Data** pane, right-click the **Parameters** node > **Add Parameter**.</span></span> <span data-ttu-id="4d3a1-123">กล่องโต้ตอบ **คุณสมบัติพารามิเตอร์ของรายงาน** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="4d3a1-123">The **Report Parameter Properties** dialog box opens.</span></span>  
  
2.  <span data-ttu-id="4d3a1-124">ใน **ชื่อ** ให้คุณพิมพ์ชื่อสำหรับพารามิเตอร์หรือกดยอมรับชื่อเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="4d3a1-124">In **Name**, type a name for the parameter or accept the default name.</span></span>  
  
3.  <span data-ttu-id="4d3a1-125">ใน **ข้อความตอบรับ** ให้คุณพิมพ์ข้อความที่จะแสดงข้างกล่องข้อความพารามิเตอร์เมื่อผู้ใช้เรียกใช้รายงาน</span><span class="sxs-lookup"><span data-stu-id="4d3a1-125">In **Prompt**, type text to appear next to the parameter text box when the user runs the report.</span></span>  
  
4.  <span data-ttu-id="4d3a1-126">ใน **ชนิดข้อมูล** ให้คุณเลือกชนิดข้อมูลสำหรับค่าพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="4d3a1-126">In **Data type**, select the data type for the parameter value.</span></span>  
  
5.  <span data-ttu-id="4d3a1-127">ถ้าพารามิเตอร์สามารถมีค่าว่างได้ ให้เลือก **อนุญาตให้มีค่าว่าง**</span><span class="sxs-lookup"><span data-stu-id="4d3a1-127">If the parameter can contain a blank value, select **Allow blank value**.</span></span>  
  
6.  <span data-ttu-id="4d3a1-128">ถ้าพารามิเตอร์สามารถมีค่า Null ได้ ให้เลือก **อนุญาตให้มีค่า Null**</span><span class="sxs-lookup"><span data-stu-id="4d3a1-128">If the parameter can contain a null value, select **Allow null value**.</span></span>  
  
7.  <span data-ttu-id="4d3a1-129">เลือก **อนุญาตให้มีหลายค่า** เพื่อให้ผู้ใช้เลือกค่าสำหรับพารามิเตอร์ได้มากกว่าหนึ่งค่า</span><span class="sxs-lookup"><span data-stu-id="4d3a1-129">To allow a user to select more than one value for the parameter, select **Allow multiple values**.</span></span>  
  
8.  <span data-ttu-id="4d3a1-130">ตั้งค่าตัวเลือกการมองเห็น</span><span class="sxs-lookup"><span data-stu-id="4d3a1-130">Set the visibility option.</span></span>  
  
    -   <span data-ttu-id="4d3a1-131">เลือก **มองเห็นได้** เพื่อแสดงพารามิเตอร์ในแถบเครื่องมือที่ด้านบนของรายงาน</span><span class="sxs-lookup"><span data-stu-id="4d3a1-131">To show the parameter on the toolbar at the top of the report, select **Visible**.</span></span>  
  
    -   <span data-ttu-id="4d3a1-132">เลือก **ซ่อน** เพื่อซ่อนพารามิเตอร์ไม่ให้แสดงในแถบเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="4d3a1-132">To hide the parameter so that it doesn't display on the toolbar, select **Hidden**.</span></span>  
  
    -   <span data-ttu-id="4d3a1-133">เลือก **ภายใน** เพื่อซ่อนพารามิเตอร์และปกป้องไว้จากการถูกดัดแปลงในเซิร์ฟเวอร์รายงานหลังจากที่เผยแพร่รายงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="4d3a1-133">To hide the parameter and protect it from being modified on the report server after the report is published, select **Internal**.</span></span> <span data-ttu-id="4d3a1-134">จากนั้นพารามิเตอร์ของรายงานจะเห็นได้ในข้อกำหนดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="4d3a1-134">The report parameter can then only be viewed in the report definition.</span></span> <span data-ttu-id="4d3a1-135">สำหรับตัวเลือกนี้ คุณต้องตั้งค่าเป็นค่าเริ่มต้นหรืออนุญาตให้พารามิเตอร์มีค่า Null ได้</span><span class="sxs-lookup"><span data-stu-id="4d3a1-135">For this option, you must set a default value or allow the parameter to accept a null value.</span></span>  
  
9. <span data-ttu-id="4d3a1-136">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4d3a1-136">Select **OK**.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="4d3a1-137">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4d3a1-137">Next steps</span></span>

<span data-ttu-id="4d3a1-138">ดูที่ [ดูพารามิเตอร์สำหรับรายงานแบบแบ่งหน้า](../consumer/paginated-reports-view-parameters.md) เพื่อดูว่าพารามิเตอร์มีหน้าตาอย่างไรในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="4d3a1-138">See [View parameters for paginated reports](../consumer/paginated-reports-view-parameters.md) to see how the parameters look in the Power BI service.</span></span>

<span data-ttu-id="4d3a1-139">สำหรับข้อมูลเชิงลึกเกี่ยวกับพารามิเตอร์ในรายงานที่มีการแบ่งหน้า ดู[พารามิเตอร์ของรายงานในตัวสร้างรายงาน Power BI](report-builder-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="4d3a1-139">For in-depth information about parameters in paginated reports, see [Report parameters in Power BI Report Builder](report-builder-parameters.md).</span></span>
