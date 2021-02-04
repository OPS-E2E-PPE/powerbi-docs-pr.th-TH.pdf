---
title: สร้างรายงานแบบแบ่งหน้าสำหรับเซิร์ฟเวอร์รายงาน Power BI
description: เรียนรู้วิธีการสร้างรายงานแบบแบ่งหน้าสำหรับเซิร์ฟเวอร์รายงาน Power BI ในขั้นตอนง่ายๆไม่กี่ขั้นตอน
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.date: 01/07/2020
ms.openlocfilehash: 72c52c5d9618411fcb696f5a1b6e2c9eddf81ded
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410010"
---
# <a name="create-a-paginated-report-for-power-bi-report-server"></a><span data-ttu-id="6aa29-103">สร้างรายงานแบบแบ่งหน้าสำหรับเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="6aa29-103">Create a paginated report for Power BI Report Server</span></span>
<span data-ttu-id="6aa29-104">ในบทความนี้ คุณสามารถสร้างรายงานแบบแบ่งหน้าสำหรับเซิร์ฟเวอร์รายงาน Power BI ในขั้นตอนง่าย ๆ ไม่กี่ขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="6aa29-104">In this article, you create a paginated report for Power BI Report Server in a few simple steps.</span></span>

<span data-ttu-id="6aa29-105">กำลังมองหาความช่วยเหลือเกี่ยวกับการสร้างรายงานแบบแบ่งหน้าในตัวสร้างรายงานสำหรับบริการของ Power BI หรือไม่</span><span class="sxs-lookup"><span data-stu-id="6aa29-105">Looking for help with creating paginated reports in Report Builder for the Power BI service?</span></span> <span data-ttu-id="6aa29-106">ดู [ตัวสร้างรายงานใน Power BI](../paginated-reports/report-builder-power-bi.md) แทน</span><span class="sxs-lookup"><span data-stu-id="6aa29-106">See [Power BI Report Builder](../paginated-reports/report-builder-power-bi.md) instead.</span></span>

<span data-ttu-id="6aa29-107">ตามชื่อแนะนำ รายงานแบบแบ่งหน้าสามารถเรียกใช้งานกับหน้ามากมาย</span><span class="sxs-lookup"><span data-stu-id="6aa29-107">As the name suggests, paginated reports can run to many pages.</span></span> <span data-ttu-id="6aa29-108">พวกเขากำลังวางเค้าโครงในรูปแบบคงที่ และเสนอการกำหนดค่าอย่างแม่นยำ</span><span class="sxs-lookup"><span data-stu-id="6aa29-108">They're laid out in a fixed format and offer precise customization.</span></span> <span data-ttu-id="6aa29-109">รายงานแบบแบ่งหน้าคือ ไฟล์ .rdl</span><span class="sxs-lookup"><span data-stu-id="6aa29-109">Paginated reports are .rdl files.</span></span>

<span data-ttu-id="6aa29-110">คุณสามารถจัดเก็บและจัดการกับรายงานแบบแบ่งหน้าในเว็บพอร์ทัลเซิร์ฟเวอร์รายงาน Power BI เหมือนกับที่คุณสามารถทำได้ในเว็บพอร์ทัล SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="6aa29-110">You can store and manage paginated reports in the Power BI Report Server web portal, just as you can in the SQL Server Reporting Services (SSRS) web portal.</span></span> <span data-ttu-id="6aa29-111">คุณสามารถสร้าง และแก้ไขไฟล์ใน “ตัวสร้างรายงาน” หรือ “ตัวออกแบบรายงาน” ในเครื่องมือข้อมูลเซิร์ฟเวอร์ SQL (SSDT), แล้วเผยแพร่ไปยังเว็บพอร์ทัล</span><span class="sxs-lookup"><span data-stu-id="6aa29-111">You create and edit them in Report Builder or Report Designer in SQL Server Data Tools (SSDT), then publish them to either web portal.</span></span> <span data-ttu-id="6aa29-112">จากนั้น ผู้อ่านรายงานในองค์กรของคุณสามารถดูข้อมูลได้ ในเบราว์เซอร์ หรือ ในแอป Power BI บนมือถือในอุปกรณ์เคลื่อนที่ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="6aa29-112">Then report readers in your organization can view them in a browser or in a Power BI mobile app on their mobile device.</span></span>

![รายงานแบบแบ่งหน้าของเซิร์ฟเวอร์รายงาน power BI](media/quickstart-create-paginated-report/reportserver-paginated-report.png)

<span data-ttu-id="6aa29-114">ถ้าคุณเคยสร้างรายงานแบบแบ่งหน้าใน “ตัวสร้างรายงาน” หรือ “ตัวออกแบบรายงาน” ดังนั้นคุณก็พร้อมที่จะสร้างรายงานแบบแบ่งหน้าสำหรับเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="6aa29-114">If you've already created paginated reports in Report Builder or Report Designer, then you're ready to create paginated reports for Power BI Report Server.</span></span> <span data-ttu-id="6aa29-115">ถ้าไม่เคย นี่คือขั้นตอนด่วนที่จะช่วยคุณเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6aa29-115">If not, here are some quick steps to get you started.</span></span>

## <a name="step-1-start-report-builder"></a><span data-ttu-id="6aa29-116">ขั้นตอนที่ 1: เริ่มต้นใช้งานตัวสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="6aa29-116">Step 1: Start Report Builder</span></span>
<span data-ttu-id="6aa29-117">คุณอาจมีการติดตั้งตัวสร้างรายงานเพื่อสร้างรายงานสำหรับเซิร์ฟเวอร์ SSRS แล้ว</span><span class="sxs-lookup"><span data-stu-id="6aa29-117">You may already have installed Report Builder to create reports for an SSRS server.</span></span> <span data-ttu-id="6aa29-118">คุณสามารถใช้รุ่นเดียวกัน หรือใช้ตัวสร้างรายงานเพื่อสร้างรายงานสำหรับเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="6aa29-118">You can use the same version or Report Builder to create reports for Power BI Report Server.</span></span> <span data-ttu-id="6aa29-119">ถ้าคุณยังไม่ได้ทำการติดตั้ง คุณสามารถติดตั้งได้ง่ายๆ</span><span class="sxs-lookup"><span data-stu-id="6aa29-119">If you haven't installed it, the process is easy.</span></span>

1. <span data-ttu-id="6aa29-120">ในเว็บพอร์ทัลเซิร์ฟเวอร์ Power BI เลือก **สร้างรายงาน** > **แบบแบ่งหน้าใหม่**</span><span class="sxs-lookup"><span data-stu-id="6aa29-120">In the Power BI Report Server web portal, select **New** > **Paginated Report**.</span></span>
   
    ![เมนูสำหรับรายงานแบบแบ่งหน้าใหม่](media/quickstart-create-paginated-report/reportserver-new-paginated-report-menu.png)
   
    <span data-ttu-id="6aa29-122">ถ้าคุณยังไม่ได้ติดตั้ง “ตัวสร้างรายงาน” คุณจะถูกนำเข้าสู่กระบวนการติดตั้งตอนนี้</span><span class="sxs-lookup"><span data-stu-id="6aa29-122">If you don't have Report Builder installed already, it leads you through the installation process now.</span></span>
2. <span data-ttu-id="6aa29-123">หลังจากติดตั้งแล้ว “ตัวสร้างรายงาน” จะเปิดขึ้นใน **หน้าจอชุดข้อมูลหรือ** รายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="6aa29-123">After it's installed, Report Builder opens to the **New Report or Dataset** screen.</span></span>
   
    ![หน้าจอชุดข้อมูลหรือรายงานใหม่](media/quickstart-create-paginated-report/reportserver-paginated-new-report-screen.png)
3. <span data-ttu-id="6aa29-125">เลือกตัวช่วยสร้างสำหรับชนิดของรายงานที่คุณต้องการสร้าง:</span><span class="sxs-lookup"><span data-stu-id="6aa29-125">Select the wizard for the kind of report you want to create:</span></span>
   
   * <span data-ttu-id="6aa29-126">ตารางหรือเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="6aa29-126">Table or matrix</span></span>
   * <span data-ttu-id="6aa29-127">แผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="6aa29-127">Chart</span></span>
   * <span data-ttu-id="6aa29-128">แผนที่</span><span class="sxs-lookup"><span data-stu-id="6aa29-128">Map</span></span>
   * <span data-ttu-id="6aa29-129">ว่าง</span><span class="sxs-lookup"><span data-stu-id="6aa29-129">Blank</span></span>
4. <span data-ttu-id="6aa29-130">มาเริ่มต้นด้วยตัวช่วยสร้างแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="6aa29-130">Let's start with the Chart wizard.</span></span>
   
    <span data-ttu-id="6aa29-131">ตัวช่วยสร้างแผนภูมิจะช่วยแนะนำขั้นตอนการสร้างแผนภูมิพื้นฐานในรายงานให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="6aa29-131">The Chart wizard walks you the steps of creating a basic chart in a report.</span></span> <span data-ttu-id="6aa29-132">จากที่นั่น คุณสามารถปรับแต่งรายงานของคุณได้เกือบทุกวิธีแบบไม่จำกัด</span><span class="sxs-lookup"><span data-stu-id="6aa29-132">From there, you can customize your report in almost unlimited ways.</span></span>

## <a name="step-2-go-through-the-chart-wizard"></a><span data-ttu-id="6aa29-133">ขั้นตอนที่ 2: ไปที่ตัวช่วยสร้างแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="6aa29-133">Step 2: Go through the Chart wizard</span></span>
<span data-ttu-id="6aa29-134">ตัวช่วยสร้างแผนภูมิจะช่วยแนะนำขั้นตอนพื้นฐานของการสร้างการแสดงภาพในรายงาน</span><span class="sxs-lookup"><span data-stu-id="6aa29-134">The Chart wizard walks you through the basic steps of creating a visualization in a report.</span></span>

<span data-ttu-id="6aa29-135">รายงานแบบแบ่งหน้าสามารถเชื่อมต่อกับแหล่งข้อมูลที่หลากหลาย จากเซิร์ฟเวอร์ Microsoft SQL และ ฐานข้อมูล Microsoft Azure SQL ไปยัง Oracle, Hyperion และอื่นๆ อีกมากมาย</span><span class="sxs-lookup"><span data-stu-id="6aa29-135">Paginated reports can connect to a wide variety of data sources, from Microsoft SQL Server and Microsoft Azure SQL Database to Oracle, Hyperion, and many more.</span></span> <span data-ttu-id="6aa29-136">อ่านเกี่ยวกับ [แหล่งข้อมูลที่ได้รับการสนับสนุนโดยรายงานแบบแบ่งหน้า](connect-data-sources.md)</span><span class="sxs-lookup"><span data-stu-id="6aa29-136">Read about [data sources supported by paginated reports](connect-data-sources.md).</span></span>

<span data-ttu-id="6aa29-137">ในหน้าแรกของช่วยสร้างแผนภูมิ **เลือกชุดข้อมูล** คุณสามารถสร้างชุดข้อมูลหรือเลือกชุดข้อมูลที่ใช้ร่วมกันบนเซิร์ฟเวอร์ได้</span><span class="sxs-lookup"><span data-stu-id="6aa29-137">In the first page in the Chart wizard, **Choose a dataset**, you can create a dataset or choose a shared dataset on a server.</span></span> <span data-ttu-id="6aa29-138">*ชุดข้อมูล* ส่งกลับข้อมูลรายงานจากแบบสอบถามบนแหล่งข้อมูลภายนอก</span><span class="sxs-lookup"><span data-stu-id="6aa29-138">*Datasets* return report data from a query on an external data source.</span></span>

1. <span data-ttu-id="6aa29-139">เลือก **เรียกดู** > เลือกชุดข้อมูลที่ใช้ร่วมกันบนเซิร์ฟเวอร์ > **เปิด** > **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="6aa29-139">Select **Browse** > select a shared dataset on a server > **Open** > **Next**.</span></span>
   
    ![ตัวช่วยสร้างแผนภูมิ: เลือกชุดข้อมูล](media/quickstart-create-paginated-report/reportserver-paginated-choose-dataset.png)
   
     <span data-ttu-id="6aa29-141">ต้องการสร้างชุดข้อมูลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6aa29-141">Need to create a dataset?</span></span> <span data-ttu-id="6aa29-142">ดูที่[สร้างชุดข้อมูลที่ใช้ร่วมกันหรือชุดข้อมูลที่ฝัง](/sql/reporting-services/report-data/create-a-shared-dataset-or-embedded-dataset-report-builder-and-ssrs)</span><span class="sxs-lookup"><span data-stu-id="6aa29-142">See [Create a shared or embedded dataset](/sql/reporting-services/report-data/create-a-shared-dataset-or-embedded-dataset-report-builder-and-ssrs).</span></span>
2. <span data-ttu-id="6aa29-143">เลือกชนิดแผนภูมิ - ในกรณีนี้ แผนภูมิแท่ง</span><span class="sxs-lookup"><span data-stu-id="6aa29-143">Choose a chart type -- in this case, a bar chart.</span></span>
   
    ![ตัวช่วยสร้างแผนภูมิ: ประเภทแผนภูมิ](media/quickstart-create-paginated-report/reportserver-paginated-choose-chart-type.png)
3. <span data-ttu-id="6aa29-145">จัดเรียงเขตข้อมูลโดยการลากไปยัง **ประเภท**, **ชุด** และ **กล่อง** ค่า</span><span class="sxs-lookup"><span data-stu-id="6aa29-145">Arrange the fields by dragging them to the **Categories**, **Series**, and **Values** boxes.</span></span>
   
    ![ตัวช่วยสร้างแผนภูมิ: จัดเรียงเขตข้อมูล](media/quickstart-create-paginated-report/reportserver-paginated-arrange-fields.png)
4. <span data-ttu-id="6aa29-147">เลือก **ถัดไป** > **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="6aa29-147">Select **Next** > **Finish**.</span></span>

## <a name="step-3-design-your-report"></a><span data-ttu-id="6aa29-148">ขั้นตอนที่ 3: ออกแบบรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="6aa29-148">Step 3: Design your report</span></span>
<span data-ttu-id="6aa29-149">ในตอนนี้คุณอยู่ในมุมมองการออกแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="6aa29-149">Now you're in Report Design view.</span></span> <span data-ttu-id="6aa29-150">จะสังเกตเห็นว่าข้อมูลเป็นข้อมูลตัวอย่างที่จะแสดงผล ไม่ใช่ข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="6aa29-150">Notice the data is placeholder data, not your data.</span></span>

![มุมมองการออกแบบรายงาน](media/quickstart-create-paginated-report/reportserver-paginated-preview-report.png)

* <span data-ttu-id="6aa29-152">เมื่อต้องการดูข้อมูลของคุณ เลือก **เรียกใช้**</span><span class="sxs-lookup"><span data-stu-id="6aa29-152">To view your data, select **Run**.</span></span>
  
     ![เรียกใช้รายงาน](media/quickstart-create-paginated-report/reportserver-paginated-run-report.png)
* <span data-ttu-id="6aa29-154">เมื่อต้องการย้อนกลับไปยังมุมมองการออกแบบ เลือก **ออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="6aa29-154">To go back to Design view, select **Design**.</span></span>

<span data-ttu-id="6aa29-155">คุณสามารถปรับเปลี่ยนแผนภูมิคุณเพิ่งสร้าง เปลี่ยนเค้าโครง ค่า คำอธิบายแผนภูมิ...หรือปรับเปรี่ยนอะไรก็ได้</span><span class="sxs-lookup"><span data-stu-id="6aa29-155">You can modify the chart you just created, changing the layout, values, legend... really just about anything.</span></span>

<span data-ttu-id="6aa29-156">และคุณสามารถเพิ่มการเรียงลำดับทั้งหมดของการแสดงภาพต่างๆ เช่น ตัววัด ตาราง เมทริกซ์ ตาราง แผนที่ และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="6aa29-156">And you can add all sorts of other visualizations: gauges, tables, matrixes, tables, maps, and more.</span></span> <span data-ttu-id="6aa29-157">คุณสามารถเพิ่มหัวกระดาษและท้ายกระดาษสำหรับหลายหน้า</span><span class="sxs-lookup"><span data-stu-id="6aa29-157">You can add headers and footers for multiple pages.</span></span> <span data-ttu-id="6aa29-158">ดู[บทช่วยสอนตัวสร้างรายงาน](/sql/reporting-services/report-builder-tutorials)เพื่อลองด้วยตัวคุณเอง</span><span class="sxs-lookup"><span data-stu-id="6aa29-158">See the [Report Builder tutorials](/sql/reporting-services/report-builder-tutorials) to try them for yourself.</span></span>

![มุมมองการออกแบบของตัวสร้างรายงาน](media/quickstart-create-paginated-report/reportserver-paginated-finished-design-report.png)

## <a name="step-4-save-your-report-to-the-report-server"></a><span data-ttu-id="6aa29-160">ขั้นตอนที่ 4: บันทึกรายงานของคุณไปยังเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="6aa29-160">Step 4: Save your report to the report server</span></span>
<span data-ttu-id="6aa29-161">เมื่อรายงานของคุณพร้อมแล้ว บันทึกไปยังเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="6aa29-161">When your report is ready, save it to Power BI Report Server.</span></span>

1. <span data-ttu-id="6aa29-162">ไปที่ **เมนู** ไฟล์ เลือก **บันทึกเป็น** และบันทึกไปยังเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="6aa29-162">On the **File** menu, select **Save as**, and save it to the report server.</span></span> 
2. <span data-ttu-id="6aa29-163">ในตอนนี้คุณสามารถดูรายงานได้ในเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="6aa29-163">Now you can view it in the browser.</span></span>
   
    ![รายงานแบบแบ่งหน้าในเบราว์เซอร์](media/quickstart-create-paginated-report/reportserver-paginated-report.png)

## <a name="next-steps"></a><span data-ttu-id="6aa29-165">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="6aa29-165">Next steps</span></span>
<span data-ttu-id="6aa29-166">มีทรัพยากรที่ยอดเยี่ยมมากมายสำหรับการออกแบบรายงานใน “ตัวสร้างรายงาน” และใน “ตัวออกแบบรายงาน” ในเครื่องมือข้อมูลเซิร์ฟเวอร์ SQL</span><span class="sxs-lookup"><span data-stu-id="6aa29-166">There are many great resources for designing reports in Report Builder and in Report Designer in SQL Server Data Tools.</span></span> <span data-ttu-id="6aa29-167">บทช่วยสอนตัวสร้างรายงานเหมาะสำหรับการเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6aa29-167">The Report Builder tutorials are a good place to start.</span></span>

* [<span data-ttu-id="6aa29-168">บทช่วยสอนตัวสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="6aa29-168">Report Builder tutorials</span></span>](/sql/reporting-services/report-builder-tutorials)
* [<span data-ttu-id="6aa29-169">เซิร์ฟเวอร์รายงาน Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="6aa29-169">What is Power BI Report Server?</span></span>](get-started.md)  

<span data-ttu-id="6aa29-170">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6aa29-170">More questions?</span></span> [<span data-ttu-id="6aa29-171">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="6aa29-171">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)