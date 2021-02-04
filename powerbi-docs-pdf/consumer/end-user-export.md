---
title: ส่งออกข้อมูลจาก Power BI visual
description: ส่งออกข้อมูลจากการแสดงผลด้วยภาพของรายงานและการแสดงผลด้วยภาพของแดชบอร์ด และดูข้อมูลนั้นใน Excel
author: mihart
ms.author: mihart
ms.reviewer: cmfinlan
featuredvideoid: removed
ms.service: powerbi
ms.subservice: pbi-explore
ms.topic: how-to
ms.date: 12/21/2020
LocalizationGroup: Consumers
ms.openlocfilehash: cd07004149afd2525c5830e04e5c2490eeebcb3c
ms.sourcegitcommit: 0711972326521944fdd8572403c0b15f31b916da
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/22/2020
ms.locfileid: "97721397"
---
# <a name="export-data-from-a-visual"></a><span data-ttu-id="170d1-103">ส่งออกข้อมูลจากการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="170d1-103">Export data from a visual</span></span>

[!INCLUDE[consumer-appliesto-yyny](../includes/consumer-appliesto-yyny.md)]


<span data-ttu-id="170d1-104">ถ้าคุณต้องการดูข้อมูลที่ใช้ในการสร้างการแสดงผลด้วยภาพ [คุณสามารถแสดงข้อมูลนั้นใน Power BI](end-user-show-data.md) หรือส่งออกข้อมูลนั้นไปยัง Excel ได้</span><span class="sxs-lookup"><span data-stu-id="170d1-104">To see the data that's used to create a visual, [you can display that data in Power BI](end-user-show-data.md), or export it to Excel.</span></span> <span data-ttu-id="170d1-105">ตัวเลือกในการส่งออกข้อมูลต้องมีประเภทเฉพาะบางอย่างหรือสิทธิ์การใช้งาน และแก้ไขสิทธิ์ในชุดข้อมูลและรายงาน</span><span class="sxs-lookup"><span data-stu-id="170d1-105">The option to export the data requires a certain type or license and edit permissions to the content.</span></span> <span data-ttu-id="170d1-106">หากคุณไม่สามารถส่งออกได้ ให้ตรวจสอบกับผู้ดูแลระบบ Power BI หรือฝ่าย IT ของคุณ</span><span class="sxs-lookup"><span data-stu-id="170d1-106">If you can't export, check with your Power BI administrator or IT help desk.</span></span> 

<span data-ttu-id="170d1-107">การส่งออกข้อมูลจำเป็นต้องมีสิทธิ์การใช้งาน Power BI Pro หรือสำหรับแดชบอร์ดหรือรายงานที่จะใช้ร่วมกันกับคุณโดยใช้ความจุพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="170d1-107">Exporting data requires a Power BI Pro license, or for the dashboard or report to be shared with you using Premium capacity.</span></span> <span data-ttu-id="170d1-108">หากต้องการเรียนรู้เพิ่มเติม โปรดดูหัวข้อ[ฉันมีสิทธิ์การใช้งานประเภทใดบ้าง](end-user-license.md)</span><span class="sxs-lookup"><span data-stu-id="170d1-108">To learn more, see [Which license do I have?](end-user-license.md).</span></span> <span data-ttu-id="170d1-109">ผู้เขียนรายงานอาจปิดการส่งออกข้อมูลสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="170d1-109">The report author may have turned off data export for a report.</span></span> <span data-ttu-id="170d1-110">ถ้าคุณไม่สามารถส่งออกข้อมูลได ้ให้ตรวจสอบกับผู้สร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="170d1-110">If you can't export data, check with the report author.</span></span>


## <a name="from-a-visual-on-a-power-bi-dashboard"></a><span data-ttu-id="170d1-111">จากการแสดงผลด้วยภาพบนแดชบอร์ด Power BI</span><span class="sxs-lookup"><span data-stu-id="170d1-111">From a visual on a Power BI dashboard</span></span>

1. <span data-ttu-id="170d1-112">เริ่มต้นที่จากแดชบอร์ด Power BI</span><span class="sxs-lookup"><span data-stu-id="170d1-112">Start on a Power BI dashboard.</span></span> <span data-ttu-id="170d1-113">ในส่วนนี้เราใช้แดชบอร์ดจากแอป \***ตัวอย่างการตลาดและการขาย**</span><span class="sxs-lookup"><span data-stu-id="170d1-113">Here we're using the dashboard from the \***Marketing and sales sample** _ app.</span></span> <span data-ttu-id="170d1-114">คุณสามารถ[ดาวน์โหลดแอปนี้ได้จาก AppSource.com](https://appsource.microsoft.com/en-us/product/power-bi/microsoft-retail-analysis-sample.salesandmarketingsample
)</span><span class="sxs-lookup"><span data-stu-id="170d1-114">You can [download this app from AppSource.com](https://appsource.microsoft.com/en-us/product/power-bi/microsoft-retail-analysis-sample.salesandmarketingsample
).</span></span>

    ![เพิ่มแดชบอร์ด](media/end-user-export/power-bi-dashboard.png)

2. <span data-ttu-id="170d1-116">วางเมาส์เหนือการแสดงผลด้วยภาพเพื่อแสดง_ *ตัวเลือกเพิ่มเติม*\* (...) แล้วคลิกเพื่อแสดงเมนูการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="170d1-116">Hover over a visual to reveal _ *More options*\* (...) and click to display the action menu.</span></span>

    ![เมนูที่ปรากฏขึ้นมาเมื่อเลือกจุดไข่ปลา](media/end-user-export/power-bi-option-menu.png)

3. <span data-ttu-id="170d1-118">เลือก **ส่งออกไปยัง .csvl**</span><span class="sxs-lookup"><span data-stu-id="170d1-118">Select  **Export to .csv**.</span></span>

4. <span data-ttu-id="170d1-119">สิ่งที่จะเกิดขึ้นต่อไปนั้นขึ้นอยู่กับเบราว์เซอร์ที่คุณกำลังใช้</span><span class="sxs-lookup"><span data-stu-id="170d1-119">What happens next depends on which browser you're using.</span></span> <span data-ttu-id="170d1-120">คุณอาจได้รับการแจ้งเตือนให้บันทึกไฟล์หรือคุณอาจเห็นลิงก์ไปยังไฟล์ที่ส่งออกอยู่ที่ด้านล่างของเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="170d1-120">You may be prompted to save the file or you may see a link to the exported file at the bottom of the browser.</span></span> <span data-ttu-id="170d1-121">ตามค่าเริ่มต้น การส่งออกของคุณจะถูกบันทึกไว้ในโฟลเดอร์ดาวน์โหลดในเครื่องของคุณ</span><span class="sxs-lookup"><span data-stu-id="170d1-121">By default, your export is saved to your local Downloads folder.</span></span> 

    ![เบราว์เซอร์ Chrome ที่แสดงลิงก์ของไฟล์ที่ส่งออก](media/end-user-export/power-bi-dashboards-export.png)

5. <span data-ttu-id="170d1-123">เปิดไฟล์ใน Excel</span><span class="sxs-lookup"><span data-stu-id="170d1-123">Open the file in Excel.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="170d1-124">ถ้าคุณไม่มีสิทธิ์ในการเข้าถึงข้อมูล คุณจะไม่สามารถส่งออกหรือเปิดใน Excel ได้</span><span class="sxs-lookup"><span data-stu-id="170d1-124">If you don't have permissions to the data, you won't be able to export or open in Excel.</span></span>  

    ![ผลรวมหน่วยตั้งแต่ต้นปีในรูปแบบ Excel](media/end-user-export/power-bi-excel.png)


## <a name="from-a-visual-in-a-report"></a><span data-ttu-id="170d1-126">จากการแสดงผลด้วยภาพในรายงาน</span><span class="sxs-lookup"><span data-stu-id="170d1-126">From a visual in a report</span></span>
<span data-ttu-id="170d1-127">คุณสามารถส่งออกข้อมูลจากการแสดงผลด้วยภาพในรายงานที่มีรูปแบบ .csv หรือ .xlsx (Excel) ได้</span><span class="sxs-lookup"><span data-stu-id="170d1-127">You can export data from a visual in a report as .csv or .xlsx (Excel) format.</span></span> 

1. <span data-ttu-id="170d1-128">บนแดชบอร์ด ให้เลือกไทล์เพื่อเปิดรายงานเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="170d1-128">On a dashboard, select a tile to open the underlying report.</span></span>  <span data-ttu-id="170d1-129">ในตัวอย่างนี้ เรากำลังเลือกการแสดงผลด้วยภาพเดียวกันกับที่แสดงข้างต้น *% ความแตกต่างของผลรวมหน่วยตั้งแต่ต้นปี*</span><span class="sxs-lookup"><span data-stu-id="170d1-129">In this example, we're selecting the same visual as above, *Total Units YTD Var %*.</span></span> 

    ![ไทล์แดชบอร์ดที่เน้นไว้](media/end-user-export/power-bi-export-tile.png)

    <span data-ttu-id="170d1-131">เนื่องจากไทล์นี้สร้างจากรายงาน *ตัวอย่างการขายและการตลาด* ซึ่งเป็นรายงานที่เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="170d1-131">Since this tile was created from the *Sales and Marketing Sample* report, that is the report that opens.</span></span> <span data-ttu-id="170d1-132">และจะเปิดไปยังหน้าที่มีการแสดงผลด้วยภาพของไทล์ที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="170d1-132">And, it opens to the page that contains the selected tile visual.</span></span> 

2. <span data-ttu-id="170d1-133">เลือกวิชวลในรายงาน</span><span class="sxs-lookup"><span data-stu-id="170d1-133">Select the visual in the report.</span></span> <span data-ttu-id="170d1-134">สังเกตบานหน้าต่าง **ตัวกรอง** ทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="170d1-134">Notice the **Filters** pane to the right.</span></span> <span data-ttu-id="170d1-135">การแสดงผลด้วยภาพนี้มีการใช้ตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="170d1-135">This visual has filters applied.</span></span> <span data-ttu-id="170d1-136">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับตัวกรอง ให้ดูที่ [ใช้ตัวกรองในรายงาน](end-user-report-filter.md)</span><span class="sxs-lookup"><span data-stu-id="170d1-136">To learn more about filters, see [Use filters in a report](end-user-report-filter.md).</span></span>

    ![เลือกบานหน้าต่างตัวกรองแล้ว](media/end-user-export/power-bi-export-filter-pane.png)


3. <span data-ttu-id="170d1-138">เลือก **ตัวเลือกเพิ่มเติม (...)** จากมุมขวาบนของการแสดงผลข้อมูลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="170d1-138">Select **More options (...)** from the upper right corner of the visualization.</span></span> <span data-ttu-id="170d1-139">เลือก **ส่งออกข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="170d1-139">Choose **Export data**.</span></span>

    ![ส่งออกข้อมูลที่เลือกจากรายการแบบหล่นลง](media/end-user-export/power-bi-export-reports.png)

4. <span data-ttu-id="170d1-141">คุณจะเห็นตัวเลือกในการส่งออกข้อมูลสรุปหรือข้อมูลเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="170d1-141">You'll see options to export Summarized data or Underlying data.</span></span> <span data-ttu-id="170d1-142">หากคุณใช้แอป *ตัวอย่างการขายและการตลาด\*\*\*ข้อมูลเบื้องต้น*\* จะถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="170d1-142">If you're using the *Sales and marketing sample* app, **Underlying data** will be disabled.</span></span> <span data-ttu-id="170d1-143">แต่คุณอาจพบรายงานที่มีการเปิดใช้งานทั้งสองตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="170d1-143">But you may find reports where both options are enabled.</span></span> <span data-ttu-id="170d1-144">ต่อไปนี้คือคำอธิบายความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="170d1-144">Here's an explanation of the difference.</span></span>

    <span data-ttu-id="170d1-145">**ข้อมูลสรุป**: เลือกตัวเลือกนี้ถ้าคุณต้องการส่งออกข้อมูลสำหรับสิ่งที่คุณเห็นในวิชวลอย่างเป็นปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="170d1-145">**Summarized data**: select this option if you want to export data for what you currently see in the visual.</span></span>  <span data-ttu-id="170d1-146">การส่งออกชนิดนี้แสดงเฉพาะข้อมูลที่ใช้สร้างสถานะปัจจุบันของวิชวล</span><span class="sxs-lookup"><span data-stu-id="170d1-146">This type of export shows you only the data that was used to create the current state of the visual.</span></span> <span data-ttu-id="170d1-147">หากการแสดงผลด้วยภาพมีการใช้ตัวกรอง ข้อมูลที่คุณส่งออกก็จะถูกกรองด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="170d1-147">If the visual has filters applied, then the data you export will also be filtered.</span></span> <span data-ttu-id="170d1-148">ตัวอย่างเช่น สำหรับการแสดงผลด้วยภาพนี้ การส่งออกของคุณจะรวมเฉพาะข้อมูลสำหรับปี 2014 และภาคกลาง รวมถึงข้อมูลสำหรับผู้ผลิตสี่รายเท่านั้น: VanArsdel, Natura, Aliqui และ Pirum</span><span class="sxs-lookup"><span data-stu-id="170d1-148">For example, for this visual, your export will include only data for 2014 and the central region, and only data for four of the manufacturers: VanArsdel, Natura, Aliqui, and Pirum.</span></span> <span data-ttu-id="170d1-149">หากการแสดงผลด้วยภาพของคุณมีการรวม (ผลรวม ค่าเฉลี่ย เป็นต้น) การส่งออกจะถูกรวมเข้าไว้ด้วย</span><span class="sxs-lookup"><span data-stu-id="170d1-149">If your visual has aggregates (sum, average, and so on), the export will also be aggregated.</span></span> 
  

    <span data-ttu-id="170d1-150">**ข้อมูลเบื้องต้น**: เลือกตัวเลือกนี้ หากคุณต้องการส่งออกข้อมูลสำหรับสิ่งที่คุณเห็นในการแสดงผลด้วยภาพ **เสริมด้วย** ข้อมูลเพิ่มเติมจากชุดข้อมูลเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="170d1-150">**Underlying data**: select this option if you want to export data for what you see in the visual **plus** additional data from the underlying dataset.</span></span>  <span data-ttu-id="170d1-151">ซึ่งอาจรวมถึงข้อมูลที่มีอยู่ในชุดข้อมูล แต่ไม่ได้ใช้ในการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="170d1-151">This may include data that is contained in the dataset but not used in the visual.</span></span> <span data-ttu-id="170d1-152">หากการแสดงผลด้วยภาพมีการใช้ตัวกรอง ข้อมูลที่คุณส่งออกก็จะถูกกรองด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="170d1-152">If the visual has filters applied, then the data you export will also be filtered.</span></span>  <span data-ttu-id="170d1-153">หากวิชวลของคุณมีการรวม (ผลรวม เฉลี่ย เป็นต้น) การส่งออกจะลบการรวม; ทำให้ข้อมูลแบนราบเป็นหลัก</span><span class="sxs-lookup"><span data-stu-id="170d1-153">If your visual has aggregates (sum, average, etc.), the export will remove the aggregation; essentially flattening the data.</span></span> 

    ![เมนูที่คุณเลือกให้เป็นข้อมูลเบื้องต้นหรือข้อมูลสรุป](media/end-user-export/power-bi-export-underlying.png)

5. <span data-ttu-id="170d1-155">สิ่งที่จะเกิดขึ้นต่อไปนั้นขึ้นอยู่กับเบราว์เซอร์ที่คุณกำลังใช้</span><span class="sxs-lookup"><span data-stu-id="170d1-155">What happens next depends on which browser you're using.</span></span> <span data-ttu-id="170d1-156">คุณอาจได้รับการแจ้งเตือนให้บันทึกไฟล์ หรือคุณอาจเห็นลิงก์ไปยังไฟล์ที่ส่งออกอยู่ที่ด้านล่างของเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="170d1-156">You might be prompted to save the file or you might see a link to the exported file at the bottom of the browser.</span></span> <span data-ttu-id="170d1-157">หากคุณกำลังใช้แอป Power BI ใน Microsoft Teams ไฟล์ที่ส่งออกของคุณจะถูกบันทึกไว้ในโฟลเดอร์ดาวน์โหลดในเครื่องของคุณ</span><span class="sxs-lookup"><span data-stu-id="170d1-157">If you're using the Power BI app in Microsoft Teams, your exported file is saved in your local Downloads folder.</span></span> 

    ![ไฟล์ที่ส่งออกซึ่งแสดงในเบราว์เซอร์ Microsoft Edge](media/end-user-export/power-bi-export-edge-screen.png)

    > [!NOTE]
    > <span data-ttu-id="170d1-159">ถ้าคุณไม่มีสิทธิ์ในการเข้าถึงข้อมูล คุณจะไม่สามารถส่งออกหรือเปิดใน Excel ได้</span><span class="sxs-lookup"><span data-stu-id="170d1-159">If you don't have permissions to the data, you won't be able to export or open in Excel.</span></span>  


6. <span data-ttu-id="170d1-160">เปิดไฟล์ใน Excel</span><span class="sxs-lookup"><span data-stu-id="170d1-160">Open the file in Excel.</span></span> <span data-ttu-id="170d1-161">เปรียบเทียบจำนวนข้อมูลที่ส่งออกกับข้อมูลที่เราส่งออกจากการแสดงผลด้วยภาพเดียวกันบนแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="170d1-161">Compare the amount of data exported to the data we exported from the same visual on the dashboard.</span></span> <span data-ttu-id="170d1-162">ความแตกต่างก็คือการส่งออกนี้รวม **ข้อมูลเบื้องต้น** ด้วย</span><span class="sxs-lookup"><span data-stu-id="170d1-162">The difference is that this export includes **Underlying data**.</span></span> 

    ![ตัวอย่าง Excel](media/end-user-export/power-bi-underlying.png)

## <a name="next-steps"></a><span data-ttu-id="170d1-164">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="170d1-164">Next steps</span></span>

[<span data-ttu-id="170d1-165">แสดงข้อมูลที่ใช้เพื่อสร้างวิชวล</span><span class="sxs-lookup"><span data-stu-id="170d1-165">Display the data used to create a visual</span></span>](end-user-show-data.md)