---
title: ใช้การดูรายละเอียดแบบเจาะลึกข้ามรายงานใน Power BI Desktop
description: เรียนรู้วิธีการดูรายละเอียดแบบเจาะลึกจากรายงานหนึ่งไปยังอีกรายงานหนึ่งใน Power BI Desktop
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 07/27/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 5cf1ed76f47eba9dc989b26fbb5dcc52f92ddd18
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414288"
---
# <a name="use-cross-report-drill-through-in-power-bi"></a><span data-ttu-id="2309f-103">ใช้การดูรายละเอียดแบบเจาะลึกข้ามรายงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="2309f-103">Use cross-report drill through in Power BI</span></span>

<span data-ttu-id="2309f-104">ด้วยคุณลักษณะ *การดูรายละเอียดแบบเจาะลึกข้ามรายงาน* ใน Power BI โดยบริบทแล้วคุณจะสามารถข้ามจากรายงานหนึ่งไปยังรายงานอื่นในแอปหรือพื้นที่ทำงานเดียวกันของบริการ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="2309f-104">With the Power BI *cross-report drill-through* feature, you can contextually jump from one report to another report in the same Power BI service workspace or app.</span></span> <span data-ttu-id="2309f-105">คุณสามารถใช้การดูรายละเอียดแบบเจาะลึกข้ามรายงาน เพื่อเชื่อมโยงรายงานสองรายการขึ้นไปที่มีเนื้อหาเกี่ยวข้องกัน และดำเนินการผ่านตัวกรองเนื้อหาพร้อมกับการเชื่อมโยงข้ามรายงาน</span><span class="sxs-lookup"><span data-stu-id="2309f-105">You can use cross-report drill through to connect two or more reports that have related content, and to pass filter context along with the cross-report connection.</span></span> 

<span data-ttu-id="2309f-106">หากต้องการเริ่มต้นดูรายละเอียดแบบเจาะลึกข้ามรายงาน ให้คุณเลือกจุดข้อมูลใน *วิชวลต้นทาง* ของ *รายงานต้นฉบับ* จากนั้นเลือกเป้าหมาย **การดูรายละเอียดแบบเจาะลึก** ข้ามรายงานจากเมนูบริบท</span><span class="sxs-lookup"><span data-stu-id="2309f-106">To initiate cross-report drill through, you select a data point in a *source visual* of a *source report*, and then select the cross-report **Drill through** target from the context menu.</span></span> 

![ตัวเลือกการดูรายละเอียดแบบเจาะลึกข้ามรายงานใน Power BI](media/desktop-cross-report-drill-through/cross-report-drill-through-01.png)

<span data-ttu-id="2309f-108">การดำเนินการในการดูรายละเอียดแบบเจาะลึกจะเปิด *หน้าเป้าหมาย* ใน *รายงานเป้าหมาย*</span><span class="sxs-lookup"><span data-stu-id="2309f-108">The drill-through action opens the *target page* in the *target report*.</span></span> 

![เป้าหมายการดูรายละเอียดแบบเจาะลึกข้ามรายงานใน Power BI Desktop](media/desktop-cross-report-drill-through/cross-report-drill-through-01a.png)

<span data-ttu-id="2309f-110">บทความนี้แสดงวิธีการตั้งค่าและใช้การดูรายละเอียดแบบเจาะลึกข้ามรายงานสำหรับรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="2309f-110">This article shows you how to set up and use cross-report drill through for Power BI reports.</span></span>

> [!NOTE]
> <span data-ttu-id="2309f-111">คุณไม่สามารถใช้การดูรายละเอียดแบบเจาะลึกข้ามรายงานด้วย[รายงานที่แชร์กับฉัน](../collaborate-share/service-share-dashboards.md#share-a-dashboard-or-report)แบบแชร์ทีละรายการได้</span><span class="sxs-lookup"><span data-stu-id="2309f-111">You can't use cross-report drill through with individually-shared [Shared with me reports](../collaborate-share/service-share-dashboards.md#share-a-dashboard-or-report).</span></span> <span data-ttu-id="2309f-112">เมื่อต้องการใช้การดูรายละเอียดแบบเจาะลึกข้ามรายงาน คุณต้องเข้าถึงรายงานในพื้นที่ทำงานที่คุณเป็นสมาชิกอยู่</span><span class="sxs-lookup"><span data-stu-id="2309f-112">To use cross-report drill through, you must access reports in workspaces that you’re a member of.</span></span>

## <a name="enable-cross-report-drill-through"></a><span data-ttu-id="2309f-113">เปิดใช้งานการดูรายละเอียดแบบเจาะลึกข้ามรายงาน</span><span class="sxs-lookup"><span data-stu-id="2309f-113">Enable cross-report drill through</span></span>

<span data-ttu-id="2309f-114">ขั้นตอนแรกในการเปิดใช้งานการดูรายละเอียดแบบเจาะลึกข้ามรายงานคือ การตรวจสอบรูปแบบข้อมูลสำหรับแหล่งข้อมูลและรายงานเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="2309f-114">The first step in enabling cross-report drill through is to validate the data models for the source and target reports.</span></span> <span data-ttu-id="2309f-115">แม้ว่า Schema ในแต่ละรายงานไม่จำเป็นต้องเหมือนกัน เขตข้อมูลที่คุณต้องการส่งต้องมีอยู่ในรูปแบบข้อมูลทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="2309f-115">Although the schemas in each report don't have to be the same, the fields you want to pass must exist in both data models.</span></span> <span data-ttu-id="2309f-116">ชื่อของเขตข้อมูลและชื่อของตารางที่พวกเขาเป็นสมาชิกต้องเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="2309f-116">The names of the fields, and the names of the tables they belong to, must be identical.</span></span> <span data-ttu-id="2309f-117">สตริงต้องตรงกัน และตรงตามตัวพิมพ์ใหญ่-เล็ก</span><span class="sxs-lookup"><span data-stu-id="2309f-117">The strings must match, and are case-sensitive.</span></span>

<span data-ttu-id="2309f-118">ตัวอย่างเช่น หากคุณต้องการส่งต่อตัวกรองในเขตข้อมูล **รัฐ** ภายในตาราง **รัฐของสหรัฐฯ** ทั้งสองรูปแบบต้องมีตาราง **รัฐของสหรัฐฯ** และเขตข้อมูล **รัฐ** อยู่ภายในตาราง</span><span class="sxs-lookup"><span data-stu-id="2309f-118">For example, if you want to pass a filter on a field **State** within a table **US States**, both models must have a **US States** table, and a **State** field within that table.</span></span> <span data-ttu-id="2309f-119">หากไม่เหมือนกัน คุณต้องอัปเดตชื่อเขตข้อมูลหรือชื่อตารางในรูปแบบพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="2309f-119">If not, you must update the field name or table name in the underlying model.</span></span> <span data-ttu-id="2309f-120">การอัปเดตแค่ชื่อเขตข้อมูลที่แสดง ส่งผลให้การดูรายละเอียดแบบเจาะลึกข้ามรายงานนั้นทำงานอย่างไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="2309f-120">Simply updating the display name of the fields won't work properly for cross-report drill through.</span></span>

<span data-ttu-id="2309f-121">หลังจากที่คุณตรวจสอบความถูกต้องของแบบจำลองของคุณ ให้เปิดใช้งานรายงานต้นฉบับเพื่อใช้การดูรายละเอียดแบบเจาะลึกข้ามรายงาน</span><span class="sxs-lookup"><span data-stu-id="2309f-121">After you validate your models, enable the source report to use cross-report drill through.</span></span> 

1. <span data-ttu-id="2309f-122">ใน Power BI Desktop ไปที่ตัวเลือก **แฟ้ม** > **และตัวเลือก** > **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="2309f-122">In Power BI Desktop, go to **File** > **Options and settings** > **Options**.</span></span> 
1. <span data-ttu-id="2309f-123">ในหน้าต่าง **ตัวเลือก** ทางด้านซ้ายของการนำทาง ที่ด้านล่างของส่วน **ไฟล์ปัจจุบัน** เลือก **การตั้งค่ารายงาน**</span><span class="sxs-lookup"><span data-stu-id="2309f-123">In the **Options** window left navigation, at the bottom of the **Current file** section, select **Report settings**.</span></span> 
1. <span data-ttu-id="2309f-124">ที่มุมล่างขวา ด้านล่าง **การดูรายละเอียดแบบเจาะลึกข้ามรายงาน** ให้เลือก **อนุญาตให้วิชวลในรายงานนี้ใช้เป้าหมายการดูรายละเอียดแบบเจาะลึกจากรายงานอื่น**</span><span class="sxs-lookup"><span data-stu-id="2309f-124">At bottom right, under **Cross-report drill through**, select **Allow visuals in this report to use drill-through targets from other reports**.</span></span> 
1. <span data-ttu-id="2309f-125">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2309f-125">Select **OK**.</span></span> 
   
   ![เปิดใช้งานการดูรายละเอียดแบบเจาะลึกข้ามรายงานใน Power BI Desktop](media/desktop-cross-report-drill-through/cross-report-drill-through-02.png)

<span data-ttu-id="2309f-127">คุณยังสามารถเปิดใช้งานการดูรายละเอียดแบบเจาะลึกข้ามรายงานจากบริการของ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="2309f-127">You can also enable cross-report drill through from the Power BI service.</span></span>
1. <span data-ttu-id="2309f-128">ในบริการของ Power BI ให้เลือกพื้นที่ทำงานที่มีรายงานเป้าหมายและต้นทางของคุณ</span><span class="sxs-lookup"><span data-stu-id="2309f-128">In Power BI service, select the workspace that contains your target and source reports.</span></span>
1. <span data-ttu-id="2309f-129">ถัดจากชื่อรายงานต้นทางในรายการพื้นที่ทำงาน เลือกสัญลักษณ์ **ตัวเลือกเพิ่มเติม** จากนั้น เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="2309f-129">Next to the source report name in the workspace list, select the **More options** symbol, and then select **Settings**.</span></span> 
1. <span data-ttu-id="2309f-130">ใกล้กับด้านล่างของบานหน้าต่าง **การตั้งค่า** ภายใต้ **การดูรายละเอียดแบบเจาะลึกข้ามรายงาน** ให้เลือก **อนุญาตให้วิชวลในรายงานนี้ใช้เป้าหมายการดูรายละเอียดแบบเจาะลึกจากรายงานอื่น** จากนั้นเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="2309f-130">Near the bottom of the **Settings** pane, under **Cross-report drill through**, select **Allow visuals in this report to use drill-through targets from other reports**, and then select **Save**.</span></span>
   
   ![เปิดใช้งานการดูรายละเอียดแบบเจาะลึกข้ามรายงานในบริการของ Power BI](media/desktop-cross-report-drill-through/cross-report-drill-through-02a.png)

## <a name="set-up-a-cross-report-drill-through-target"></a><span data-ttu-id="2309f-132">ตั้งค่าเป้าหมายการดูรายละเอียดแบบเจาะลึกข้ามรายงาน</span><span class="sxs-lookup"><span data-stu-id="2309f-132">Set up a cross-report drill-through target</span></span>

<span data-ttu-id="2309f-133">การตั้งค่าหน้าเป้าหมายสำหรับการดูรายละเอียดแบบเจาะลึกข้ามรายงานนั้นคล้ายกับการตั้งค่าการดูรายละเอียดแบบเจาะลึกภายในรายงาน</span><span class="sxs-lookup"><span data-stu-id="2309f-133">Setting up a target page for cross-report drill through is similar to setting up drill through within a report.</span></span> <span data-ttu-id="2309f-134">การเปิดใช้งานการดูรายละเอียดแบบเจาะลึกบนหน้าเป้าหมาย จะอนุญาตให้มีการแสดงผลด้วยวิชวลอื่น ๆ เพื่อกำหนดหน้าเป้าหมายสำหรับการดูรายละเอียดแบบเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="2309f-134">Enabling drill through on the target page allows other visuals to target the page for drill through.</span></span> <span data-ttu-id="2309f-135">หากต้องการสร้างการดูรายละเอียดแบบเจาะลึกภายในรายงานเดียว โปรดดูที่[ใช้การดูรายละเอียดแบบเจาะลึกใน Power BI Desktop](desktop-drillthrough.md)</span><span class="sxs-lookup"><span data-stu-id="2309f-135">To create drill through within a single report, see [Use drill through in Power BI Desktop](desktop-drillthrough.md).</span></span>

<span data-ttu-id="2309f-136">คุณสามารถตั้งค่าเป้าหมายสำหรับการดูรายละเอียดแบบเจาะลึกข้ามรายงานได้ใน Power BI Desktop หรือบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="2309f-136">You can set up a target for cross-report drill through in Power BI Desktop or Power BI service.</span></span> 
1. <span data-ttu-id="2309f-137">แก้ไขไฟล์เป้าหมายและบนหน้าเป้าหมายของรายงานเป้าหมาย ให้เลือกส่วน **เขตข้อมูล** ของบานหน้าต่าง **การแสดงภาพ**</span><span class="sxs-lookup"><span data-stu-id="2309f-137">Edit the target file, and on the target page of the target report, select the **Fields** section of the **Visualizations** pane.</span></span> 
1. <span data-ttu-id="2309f-138">ภายใต้ **การดูรายละเอียดแบบเจาะลึก** ให้ตั้งค่า **ข้ามรายงาน** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="2309f-138">Under **Drill through**, set the **Cross-report** toggle to **On**.</span></span> 
1. <span data-ttu-id="2309f-139">ลากเขตข้อมูลที่คุณต้องการใช้เป็นเป้าหมายการดูรายละเอียดแบบเจาะลึกไปที่ **เพิ่มเขตข้อมูลการดูรายละเอียดแบบเจาะลึกที่นี่**</span><span class="sxs-lookup"><span data-stu-id="2309f-139">Drag the fields you want to use as drill-through targets into **Add drill-through fields here**.</span></span> <span data-ttu-id="2309f-140">สำหรับแต่ละเขตข้อมูล เลือกรายการที่คุณต้องการอนุญาตการดูรายละเอียดแบบเจาะลึกเมื่อใช้เขตข้อมูลเป็นประเภท หรือเมื่อสรุปข้อมูลเป็นหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="2309f-140">For each field, select whether you want to allow drill through when the field is used as a category, or when it's summarized like a measure.</span></span> 
1. <span data-ttu-id="2309f-141">เลือกว่าคุณต้องการ **เก็บตัวกรองทั้งหมด** สำหรับวิชวลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2309f-141">Select whether you want to **Keep all filters** for the visual.</span></span> <span data-ttu-id="2309f-142">หากคุณไม่ต้องการส่งต่อตัวกรองที่ใช้จากวิชวลแหล่งที่มาไปที่วิชวลเป้าหมาย ให้เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="2309f-142">If you don't want to pass filters applied to the source visual to your target visual, select **Off**.</span></span>
   
   ![บานหน้าต่างการแสดงภาพ ที่ไฮไลต์ตัวเลือกการดูรายละเอียดแบบเจาะลึก](media/desktop-cross-report-drill-through/cross-report-drill-through-03.png)
   
1. <span data-ttu-id="2309f-144">หากคุณใช้เฉพาะหน้าสำหรับการดูรายละเอียดแบบเจาะลึกข้ามรายงาน คุณควรลบปุ่ม **ย้อนกลับ** ซึ่งถูกเพิ่มเข้าไปบนพื้นที่ทำงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2309f-144">If you're using the page for cross-report drill through only, delete the **Back** button that's automatically added to the canvas.</span></span> <span data-ttu-id="2309f-145">ปุ่ม **ย้อนกลับ** จะทำหน้าที่ในการนำทางภายในรายงานเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2309f-145">The **Back** button only works for navigation within a report.</span></span> 
1. <span data-ttu-id="2309f-146">หลังจากที่คุณได้กำหนดค่าหน้าเป้าหมายแล้ว ให้บันทึกรายงาน หากคุณกำลังใช้บริการของ Power BI หรือบันทึกและเผยแพร่รายงาน หากคุณกำลังใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2309f-146">After you configure the target page, save the report if you're using the Power BI service, or save and publish the report if you're using Power BI Desktop.</span></span>

<span data-ttu-id="2309f-147">เท่านี้ก็เรียบร้อย</span><span class="sxs-lookup"><span data-stu-id="2309f-147">That's it.</span></span> <span data-ttu-id="2309f-148">รายงานของคุณพร้อมสำหรับการดูรายละเอียดแบบเจาะลึกข้ามรายงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="2309f-148">Your reports are ready for cross-report drill through.</span></span> 

## <a name="use-cross-report-drill-through"></a><span data-ttu-id="2309f-149">ใช้การดูรายละเอียดแบบเจาะลึกข้ามรายงาน</span><span class="sxs-lookup"><span data-stu-id="2309f-149">Use cross-report drill through</span></span>

<span data-ttu-id="2309f-150">หากต้องการใช้การดูรายละเอียดแบบเจาะลึกข้ามรายงาน ให้เลือกรายงานต้นฉบับในบริการของ Power BI จากนั้นจึงเลือกวิชวลที่ใช้เขตข้อมูลการดูรายละเอียดแบบเจาะลึกตามลักษณะที่คุณระบุไว้ในขั้นตอนการตั้งค่าหน้าเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="2309f-150">To use cross-report drill through, select the source report in the Power BI service, and then select a visual that uses the drill-through field in the way you specified when you set up the target page.</span></span> <span data-ttu-id="2309f-151">คลิกขวาที่จุดข้อมูลเพื่อเปิดเมนูบริบทวิชวล เลือก **การดูรายละเอียดแบบเจาะลึก** จากนั้นเลือกเป้าหมายการดูรายละเอียดแบบเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="2309f-151">Right-click a data point to open the visual context menu, select **Drill through**, and then select the drill-through target.</span></span> <span data-ttu-id="2309f-152">เป้าหมายการดูรายละเอียดแบบเจาะลึกข้ามรายงานจะถูกจัดรูปแบบเป็น **ชื่อหน้า [ชื่อรายงาน]**</span><span class="sxs-lookup"><span data-stu-id="2309f-152">Cross-report drill-through targets are formatted as **Page name [Report name]**.</span></span>

![ตัวเลือกการดูรายละเอียดแบบเจาะลึกข้ามรายงานใน Power BI](media/desktop-cross-report-drill-through/cross-report-drill-through-01.png)

<span data-ttu-id="2309f-154">คุณจะเห็นผลลัพธ์ในหน้าการดูรายละเอียดแบบเจาะลึกข้ามรายงานตามเป้าหมาย เช่นเดียวกับที่คุณตั้งค่าไว้ในขั้นตอนที่คุณสร้างเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="2309f-154">You see the results in the target cross-report drill-through page, just as you set them up when you created the target.</span></span> <span data-ttu-id="2309f-155">ผลลัพธ์จะกรองตามการตั้งค่าการดูรายละเอียดแบบเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="2309f-155">The results are filtered according to the drill-through settings.</span></span>

![เป้าหมายการดูรายละเอียดแบบเจาะลึกข้ามรายงานใน Power BI Desktop](media/desktop-cross-report-drill-through/cross-report-drill-through-01a.png)

> [!IMPORTANT]
> <span data-ttu-id="2309f-157">Power BI บันทึกเป้าหมายการดูรายละเอียดแบบเจาะลึกข้ามรายงาน</span><span class="sxs-lookup"><span data-stu-id="2309f-157">Power BI caches cross-report drill-through targets.</span></span> <span data-ttu-id="2309f-158">หากคุณทำการเปลี่ยนแปลง อย่าลืมรีเฟรชเบราว์เซอร์ของคุณ หากคุณไม่เห็นเป้าหมายการดูรายละเอียดแบบเจาะลึกตามที่คาดการณ์ไว้</span><span class="sxs-lookup"><span data-stu-id="2309f-158">If you make changes, be sure to refresh your browser if you don't see the drill-through targets as expected.</span></span> 

<span data-ttu-id="2309f-159">ถ้าคุณตั้งค่า **เก็บตัวกรองทั้งหมด** เป็น **เปิด** เมื่อคุณตั้งค่าหน้าเป้าหมาย การกรองบริบทจากวิชวลต้นทางสามารถหมายรวมถึงรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2309f-159">If you set **Keep all filters** to **On** when you set up the target page, filter context from the source visual can include the following:</span></span> 

- <span data-ttu-id="2309f-160">รายงาน หน้า และตัวกรองระดับวิชวลที่ส่งผลต่อวิชวลต้นทาง</span><span class="sxs-lookup"><span data-stu-id="2309f-160">Report, page, and visual level filters that affect the source visual</span></span> 
- <span data-ttu-id="2309f-161">ตัวกรองแบบไขว้และการเน้นแบบข้ามทิศทางซึง่ส่งผลกระทบต่อวิชวลต้นทาง</span><span class="sxs-lookup"><span data-stu-id="2309f-161">Cross-filter and cross-highlighting that affect the source visual</span></span> 
- <span data-ttu-id="2309f-162">ตัวแบ่งส่วนข้อมูลและตัวแบ่งส่วนข้อมูลการซิงค์บนหน้า</span><span class="sxs-lookup"><span data-stu-id="2309f-162">Slicers and sync-slicers on the page</span></span>
- <span data-ttu-id="2309f-163">พารามิเตอร์ URL</span><span class="sxs-lookup"><span data-stu-id="2309f-163">URL parameters</span></span>

<span data-ttu-id="2309f-164">เมื่อคุณเข้าถึงรายงานเป้าหมายสำหรับการดูรายละเอียดแบบเจาะลึกแล้ว Power BI จะใช้ตัวกรองกับเขตข้อมูลซึ่งพบสตริงที่มีชื่อเขตข้อมูลและชื่อตารางตรงกันทั้งหมดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2309f-164">When you land on the target report for drill through, Power BI only applies filters for fields that have exact string matches for field name and table name.</span></span> 

<span data-ttu-id="2309f-165">Power BI ไม่ได้ใช้ตัวกรองแบบปักหมุดจากรายงานเป้าหมายแต่จะใช้ที่คั่นหน้าส่วนบุคคลเริ่มต้นของคุณ หากคุณมี</span><span class="sxs-lookup"><span data-stu-id="2309f-165">Power BI doesn't apply sticky filters from the target report, but it does apply your default personal bookmark if you have one.</span></span> <span data-ttu-id="2309f-166">ตัวอย่างเช่น หากที่คั่นหน้าส่วนบุคคลตามค่าเริ่มต้นของคุณนั้นรวมถึงตัวกรองระดับรายงานสำหรับ *ประเทศ = สหรัฐฯ* Power BI จะใช้ตัวกรองนั้นก่อนที่จะใช้บริบทตัวกรองจากวิชวลต้นทาง</span><span class="sxs-lookup"><span data-stu-id="2309f-166">For example, if your default personal bookmark includes a report-level filter for *Country = US*, Power BI applies that filter before applying the filter context from the source visual.</span></span> 

<span data-ttu-id="2309f-167">สำหรับการดูรายละเอียดแบบเจาะลึกข้ามรายงาน Power BI จะส่งต่อบริบทตัวกรองไปที่หน้ามาตรฐานในรายงานเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="2309f-167">For cross-report drill through, Power BI passes the filter context to standard pages in the target report.</span></span> <span data-ttu-id="2309f-168">Power BI จะไม่ส่งต่อบริบทตัวกรองสำหรับหน้าคำแนะนำเครื่องมือ เนื่องจากหน้าคำแนะนำเครื่องมือถูกกรองตามแหล่งที่มาของการแสดงผลด้วยภาพที่เรียกใช้คำแนะนำเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="2309f-168">Power BI doesn't pass filter context for tooltip pages, because tooltip pages are filtered based on the source visual that invokes the tooltip.</span></span>

<span data-ttu-id="2309f-169">หากคุณต้องการย้อนกลับไปยังรายงานต้นฉบับหลังจากที่ดำเนินการในการดูรายละเอียดแบบเจาะลึกข้ามรายงานแล้ว ให้ใช้ปุ่ม **ย้อนกลับ** ของเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="2309f-169">If you want to return to the source report after the cross-report drill-through action, use the browser's **Back** button.</span></span> 

## <a name="considerations-and-limitations"></a><span data-ttu-id="2309f-170">ข้อควรพิจารณาและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="2309f-170">Considerations and limitations</span></span>

<span data-ttu-id="2309f-171">การดูรายละเอียดแบบเจาะลึกข้ามรายงานไม่ทำงานในรายงาน Power BI ใน Power BI Report Server</span><span class="sxs-lookup"><span data-stu-id="2309f-171">Cross-report drill through doesn't work in Power BI reports in Power BI Report Server.</span></span>

## <a name="next-steps"></a><span data-ttu-id="2309f-172">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="2309f-172">Next steps</span></span>

<span data-ttu-id="2309f-173">คุณอาจสนใจบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2309f-173">You might also be interested in the following articles:</span></span>

- [<span data-ttu-id="2309f-174">ตัวแบ่งส่วนข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="2309f-174">Slicers in Power BI</span></span>](../visuals/power-bi-visualization-slicers.md)
- [<span data-ttu-id="2309f-175">ใช้การดูรายละเอียดแบบเจาะลึกใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2309f-175">Use drill through in Power BI Desktop</span></span>](desktop-drillthrough.md)
