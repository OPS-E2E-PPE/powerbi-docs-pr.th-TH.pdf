---
title: รายงานที่มีการแบ่งหน้าในบริการ Power BI
description: เอกสารที่อธิบายรายงานที่มีการแบ่งหน้าและวิธีการดูรายงานดังกล่าวในบริการ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: christopher.finlan
ms.service: powerbi
ms.subservice: pbi-explore
ms.topic: how-to
ms.date: 10/11/2020
LocalizationGroup: Common tasks
ms.openlocfilehash: 2be1c325d876c944c31d62a67771308d80dca69d
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96390529"
---
# <a name="paginated-reports-in-the-power-bi-service"></a><span data-ttu-id="800ba-103">รายงานที่มีการแบ่งหน้าในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="800ba-103">Paginated reports in the Power BI service</span></span>

[!INCLUDE[consumer-appliesto-yyny](../includes/consumer-appliesto-yyny.md)]

<span data-ttu-id="800ba-104">คุณได้เรียนรู้เกี่ยวกับ[รายงาน Power BI](end-user-reports.md) และรายงานเหล่านี้เป็นประเภทของรายงานที่คุณน่าจะพบบ่อยที่สุด</span><span class="sxs-lookup"><span data-stu-id="800ba-104">You've learned about [Power BI reports](end-user-reports.md), and those are the types of report you're most likely to encounter.</span></span> <span data-ttu-id="800ba-105">รายงาน power BI ได้รับการปรับให้เหมาะสำหรับการสำรวจและโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="800ba-105">Power BI reports are optimized for exploration and interactivity.</span></span> <span data-ttu-id="800ba-106">เมื่อพนักงานขายต้องการแบ่งส่วนข้อมูลในรายงานยอดขายตัวเดียวกันโดยแยกตามเขตพื้นที่/อุตสาหกรรม/ลูกค้า แล้วดูการเปลี่ยนแปลงของตัวเลข การสร้างรายงาน Power BI จะดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="800ba-106">A sales report where different salespeople want to slice the data in the same report for their specific region/industry/customer and see how the numbers change would be best served by a Power BI report.</span></span>

<span data-ttu-id="800ba-107">มีรายงานอีกประเภทหนึ่งที่เรียกว่า *รายงานที่มีการแบ่งหน้า*</span><span class="sxs-lookup"><span data-stu-id="800ba-107">However, there is another type of report called a *paginated report*.</span></span> <span data-ttu-id="800ba-108">การรับและการดูรายงานแบบแบ่งหน้าจำเป็นต้องมีสิทธิ์การใช้งาน Power BI Pro เพื่อให้รายงานสามารถบันทึกในความจุแบบ Premium ได้</span><span class="sxs-lookup"><span data-stu-id="800ba-108">Receiving and viewing paginated reports requires a Power BI Pro license of for the report to be saved in Premium capacity.</span></span>  <span data-ttu-id="800ba-109">[เรียนรู้เกี่ยวกับสิทธิ์การใช้งาน](end-user-license.md)</span><span class="sxs-lookup"><span data-stu-id="800ba-109">[Learn about licenses](end-user-license.md).</span></span>  

## <a name="identify-a-paginated-report"></a><span data-ttu-id="800ba-110">ระบุรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="800ba-110">Identify a paginated report</span></span>

<span data-ttu-id="800ba-111">ในรายการเนื้อหาและในหน้า Landing Page คุณสามารถระบุรายงานที่มีการแบ่งหน้าได้โดยไอคอนของรายงานเหล่านั้น ![ไอคอนรายงานที่มีการแบ่งหน้า](media/end-user-paginated-report/power-bi-report-icon.png)</span><span class="sxs-lookup"><span data-stu-id="800ba-111">In content lists and on your Home landing page, paginated reports can be identified by their icon ![paginated report icon](media/end-user-paginated-report/power-bi-report-icon.png).</span></span>  <span data-ttu-id="800ba-112">ซึ่งสามารถแชร์รายงานที่มีการแบ่งหน้ากับคุณได้โดยตรง หรือให้เป็นส่วนหนึ่งของ [แอป Power BI](end-user-apps.md)</span><span class="sxs-lookup"><span data-stu-id="800ba-112">A paginated report can be shared with you directly, or as part of a [Power BI app](end-user-apps.md).</span></span> <span data-ttu-id="800ba-113">หาก *ผู้ออกแบบ* รายงานให้สิทธิ์แก่คุณ คุณจะสามารถแชร์รายงานที่มีการแบ่งหน้า และสมัครใช้งานด้วยตัวคุณเองและผู้อื่นได้</span><span class="sxs-lookup"><span data-stu-id="800ba-113">If the report *designer* gave you permissions, you'll be able to re-share the paginated report and subscribe yourself and others.</span></span>


![รายการรายงานที่มีหนึ่งรายงานมาตรฐานและหนึ่งรายงานที่มีการแบ่งหน้า](./media/end-user-paginated-report/power-bi-report-lists.png)

## <a name="what-is-a-paginated-report"></a><span data-ttu-id="800ba-115">รายงานที่มีการแบ่งหน้าคืออะไร?</span><span class="sxs-lookup"><span data-stu-id="800ba-115">What is a paginated report?</span></span>

<span data-ttu-id="800ba-116">รายงานเหล่านี้ถูกเรียกว่ารายงาน *แบบแบ่งหน้า* เนื่องจากมีการจัดรูปแบบให้พอดีกับหน้าที่พิมพ์</span><span class="sxs-lookup"><span data-stu-id="800ba-116">These reports are called *paginated* because they're formatted to fit well on a printed page.</span></span> <span data-ttu-id="800ba-117">ข้อดีอย่างหนึ่งคือรายงานเหล่านี้แสดงข้อมูลทั้งหมดในตาราง แม้ว่าตารางนั้นต้องใช้พื้นที่หลายหน้า</span><span class="sxs-lookup"><span data-stu-id="800ba-117">One advantage is that they display all the data in a table, even if the table spans multiple pages.</span></span> <span data-ttu-id="800ba-118">รายงานที่มีการแบ่งหน้าบางครั้งเรียกว่า "พิกเซลสมบูรณ์แบบ" เนื่องจาก *นักออกแบบ* รายงานได้ควบคุมการจัดวางหน้ารายงานได้อย่างแม่นยำ</span><span class="sxs-lookup"><span data-stu-id="800ba-118">Paginated reports are sometimes called "pixel perfect" because report *designers* control the report page layout exactly.</span></span>

<span data-ttu-id="800ba-119">รายงานแบบแบ่งหน้าเหมาะที่สุดในสถานการณ์ที่ต้องใช้เอาต์พุตที่มีการจัดรูปแบบสูงและเป็นพิกเซลสมบูรณ์แบบที่เหมาะกับการพิมพ์หรือการสร้าง PDF</span><span class="sxs-lookup"><span data-stu-id="800ba-119">Paginated reports are best for scenarios that require a highly formatted, pixel-perfect output optimized for printing or PDF generation.</span></span> <span data-ttu-id="800ba-120">การสร้างงบกำไรขาดทุนเป็นตัวอย่างชนิดรายงานที่ดีที่คุณอาจต้องการดูเป็นตัวอย่างรูปแบบรายงานแบบแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="800ba-120">A profit and loss statement is a good example of the type of report you would probably want to see as a paginated report.</span></span>

## <a name="how-do-paginated-reports-work"></a><span data-ttu-id="800ba-121">รายงานแบบแบ่งหน้ามีการทำงานอย่างไร</span><span class="sxs-lookup"><span data-stu-id="800ba-121">How do paginated reports work?</span></span>

<span data-ttu-id="800ba-122">เมื่อ *ผู้ออกแบบ* รายงานสร้างรายงานที่มีการแบ่งหน้า คือพวกเขากำลังสร้าง *ข้อกำหนดของรายงาน* อย่างแท้จริง</span><span class="sxs-lookup"><span data-stu-id="800ba-122">When report *designers* create a paginated report, they're really creating a *report definition*.</span></span> <span data-ttu-id="800ba-123">ซึ่งไม่ได้มีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="800ba-123">It doesn't contain the data.</span></span> <span data-ttu-id="800ba-124">แต่จะระบุว่าต้องรับเอาข้อมูลจากที่ใด เอาข้อมูลใด และแสดงข้อมูลอย่างไร</span><span class="sxs-lookup"><span data-stu-id="800ba-124">It specifies where to get the data, which data to get, and how to display the data.</span></span> <span data-ttu-id="800ba-125">เมื่อคุณเรียกดูรายงาน ตัวประมวลผลรายงานจะใช้ข้อกำหนดของรายงาน ดึงข้อมูลออกมา แล้วรวมเข้ากับเค้าโครงรายงานเพื่อสร้างรายงานขึ้น</span><span class="sxs-lookup"><span data-stu-id="800ba-125">When you run the report, the report processor takes the report definition, retrieves the data, and combines it with the report layout to generate the report.</span></span> <span data-ttu-id="800ba-126">ในบางครั้ง รายงานจะแสดงข้อมูลเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="800ba-126">Sometimes, the report displays default data.</span></span> <span data-ttu-id="800ba-127">บางครั้งคุณจำเป็นต้องป้อนพารามิเตอร์ก่อนรายงานจึงสามารถแสดงข้อมูลใดก็ตามได้</span><span class="sxs-lookup"><span data-stu-id="800ba-127">Other times you need to enter parameters before the report can display any data.</span></span> 

<span data-ttu-id="800ba-128">เลือกรายงานที่มีการแบ่งหน้าเพื่อเปิดในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="800ba-128">Select a paginated report to open it in the Power BI service.</span></span> <span data-ttu-id="800ba-129">ถ้ามีพารามิเตอร์ คุณต้องเลือกก่อนที่คุณจะสามารถดูรายงานได้</span><span class="sxs-lookup"><span data-stu-id="800ba-129">If it has parameters, you need to select them before you can view the report.</span></span>

   ![พารามิเตอร์สำหรับรายงาน](./media/end-user-paginated-report/power-bi-select-parameters.png)

<span data-ttu-id="800ba-131">และโดยทั่วไปแล้ว นั่นคือขอบเขตของการโต้ตอบ - การตั้งค่าพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="800ba-131">And that's typically the extent of the interaction - setting the parameters.</span></span> <span data-ttu-id="800ba-132">หากคุณเป็นนักวิเคราะห์การเรียกเก็บเงิน คุณอาจใช้รายงานที่มีการแบ่งหน้าเพื่อสร้างหรือพิมพ์ใบแจ้งหนี้ได้</span><span class="sxs-lookup"><span data-stu-id="800ba-132">If you're a billing analyst, you may use paginated reports to create or print invoices.</span></span> <span data-ttu-id="800ba-133">หากคุณเป็นผู้จัดการฝ่ายขาย คุณสามารถใช้รายงานที่มีการแบ่งหน้าเพื่อดูคำสั่งซื้อตามร้านค้าหรือพนักงานขายได้</span><span class="sxs-lookup"><span data-stu-id="800ba-133">If you're a sales manager, you may use paginated reports to view orders by store or sales person.</span></span> 

<span data-ttu-id="800ba-134">รายงานที่มีการแบ่งหน้าแบบง่ายนี้จะสร้างผลกำไรตามปีหลังจากที่คุณเลือกพารามิเตอร์ **Year (ปี)**</span><span class="sxs-lookup"><span data-stu-id="800ba-134">This simple paginated report generates profit by year, after you select the **Year** parameter.</span></span> 

![รายงานอย่างง่ายแบบหนึ่งพารามิเตอร์](./media/end-user-paginated-report/power-bi-one-parameter.png)

<span data-ttu-id="800ba-136">เมื่อเปรียบเทียบกับรายงานที่มีการแบ่งหน้า Power BI นั้นตอบสนองได้มากกว่ามาก</span><span class="sxs-lookup"><span data-stu-id="800ba-136">Compared to paginated reports, Power BI reports are much more interactive.</span></span> <span data-ttu-id="800ba-137">รายงาน Power BI อนุญาตให้มีการรายงานแบบเฉพาะกิจ และรองรับวิชวลประเภทอื่น ๆ อีกมากมาย รวมถึงวิชวลแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="800ba-137">Power BI reports allow for ad hoc reporting, and support many more types of visuals, including custom visuals.</span></span>



## <a name="interact-with-a-paginated-report"></a><span data-ttu-id="800ba-138">โต้ตอบกับรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="800ba-138">Interact with a paginated report</span></span>

<span data-ttu-id="800ba-139">วิธีที่คุณโต้ตอบกับรายงานที่มีการแบ่งหน้านั้นแตกต่างจากรายงานอื่น</span><span class="sxs-lookup"><span data-stu-id="800ba-139">The way you interact with a paginated report is different from other reports.</span></span> <span data-ttu-id="800ba-140">คุณสามารถทำสิ่งต่าง ๆ เช่น พิมพ์ บุ๊กมาร์ก ส่งออก และแสดงความคิดเห็น แต่มีการโต้ตอบน้อยลง</span><span class="sxs-lookup"><span data-stu-id="800ba-140">You can do things like print, bookmark, export, and comment, but there is less interactivity.</span></span> <span data-ttu-id="800ba-141">บ่อยครั้งที่รายงานที่มีการแบ่งหน้าต้องการอินพุตจากคุณเพื่อเติมข้อมูลลงในพื้นที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="800ba-141">Often, paginated reports require input from you to populate the report canvas.</span></span>  <span data-ttu-id="800ba-142">ในบางครั้งรายงานจะแสดงข้อมูลค่าเริ่มต้น และคุณสามารถป้อนพารามิเตอร์เพื่อดูข้อมูลที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="800ba-142">Other times the report displays default data and you can enter parameters to see different data.</span></span>

### <a name="print-a-paginated-report"></a><span data-ttu-id="800ba-143">พิมพ์รายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="800ba-143">Print a paginated report</span></span>

<span data-ttu-id="800ba-144">รายงาน *ที่มีการแบ่งหน้า* ถูกจัดรูปแบบเพื่อให้พอดีกับหน้าและพิมพ์ออกมาได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="800ba-144">*Paginated* reports are formatted to fit well on a page and to print well.</span></span> <span data-ttu-id="800ba-145">สิ่งที่คุณเห็นในเบราว์เซอร์คือสิ่งที่คุณเห็นเมื่อคุณพิมพ์ออกมา</span><span class="sxs-lookup"><span data-stu-id="800ba-145">What you see in the browser is what you see when you print.</span></span> <span data-ttu-id="800ba-146">นอกจากนี้ หากรายงานมีตารางยาว ทั้งตารางจะถูกพิมพ์ออกมาแม้ว่าจะครอบคลุมหลายหน้าก็ตาม</span><span class="sxs-lookup"><span data-stu-id="800ba-146">Plus, if the report has a long table, the entire table prints, even if it spans multiple pages.</span></span> 

<span data-ttu-id="800ba-147">รายงานแบบแบ่งหน้าสามารถมีหลายหน้าได้</span><span class="sxs-lookup"><span data-stu-id="800ba-147">Paginated reports can have many pages.</span></span> <span data-ttu-id="800ba-148">ตัวอย่าง รายงานฉบับนี้มี 563 หน้า</span><span class="sxs-lookup"><span data-stu-id="800ba-148">For example, this report has 563 pages.</span></span> <span data-ttu-id="800ba-149">แต่ละหน้ามีรูปแบบเหมือนกัน โดยใช้หนึ่งหน้าต่อใบแจ้งหนี้หนึ่งใบ และมีส่วนหัวกับส่วนท้ายหน้าซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="800ba-149">Each page is laid out exactly, with one page per invoice and repeating headers and footers.</span></span> <span data-ttu-id="800ba-150">เมื่อคุณพิมพ์รายงานนี้ คุณจะได้รับตัวแบ่งหน้าระหว่างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="800ba-150">When you print this report, you'll get page breaks between invoices.</span></span>

   ![หน้าหนึ่งของรรายงานที่มีการแบ่งหน้าสำหรับของเล่น Tailspin](./media/end-user-paginated-report/power-bi-paginated-500.png)


### <a name="navigate-the-paginated-report"></a><span data-ttu-id="800ba-152">นำทางไปยังรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="800ba-152">Navigate the paginated report</span></span>

<span data-ttu-id="800ba-153">ในรายงานคำสั่งขายนี้ มีพารามิเตอร์สามตัวดังนี้ ประเภทธุรกิจ ผู้ค้าปลีก และหมายเลขคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="800ba-153">In this sales order report, there are three parameters: Business type, Reseller, and Order number.</span></span> 

![รายงานที่มีสามพารามิเตอร์](./media/end-user-paginated-report/power-bi-parameter-bar.png)

<span data-ttu-id="800ba-155">หากต้องการเปลี่ยนแปลงข้อมูลที่แสดง ให้ป้อนค่าใหม่สำหรับพารามิเตอร์สามรายการและเลือก **ดูรายงาน**</span><span class="sxs-lookup"><span data-stu-id="800ba-155">To change the information being displayed, enter new values for the three parameters and select **View report**.</span></span> <span data-ttu-id="800ba-156">ที่นี่ เราได้เลือก **ร้านจักรยานชนิดพิเศษ**, **Alpine Ski House** และหมายเลขคำสั่งซื้อ **SO46085**</span><span class="sxs-lookup"><span data-stu-id="800ba-156">Here, we've selected **Specialty bike shop**, **Alpine Ski House**, and order number **SO46085**.</span></span> <span data-ttu-id="800ba-157">การเลือก **ดูรายงาน** รีเฟรชพื้นที่รายงานของเราด้วยคำสั่งขายใหม่นี้</span><span class="sxs-lookup"><span data-stu-id="800ba-157">Selecting **View report** refreshes our report canvas with this new sales order.</span></span>

![เปลี่ยนพารามิเตอร์](./media/end-user-paginated-report/power-bi-orders.png)

<span data-ttu-id="800ba-159">คำสั่งขายใหม่จะแสดงขึ้นโดยใช้พารามิเตอร์ที่เราเลือก</span><span class="sxs-lookup"><span data-stu-id="800ba-159">The new sales order displays, using the parameters we selected.</span></span> 

![คำสั่งขายใหม่](./media/end-user-paginated-report/power-bi-new-orders.png)

<span data-ttu-id="800ba-161">รายงานที่มีการแบ่งหน้าบางรายงานมีหลายหน้า</span><span class="sxs-lookup"><span data-stu-id="800ba-161">Some paginated reports have many pages.</span></span>  <span data-ttu-id="800ba-162">ใช้ตัวควบคุมหน้าเพื่อนำทางไปยังรายงาน</span><span class="sxs-lookup"><span data-stu-id="800ba-162">Use the page controls to navigate through the report.</span></span> 

![ตัวควบคุมหน้า](./media/end-user-paginated-report/power-bi-page-control.png)

### <a name="export-the-paginated-report"></a><span data-ttu-id="800ba-164">ส่งออกรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="800ba-164">Export the paginated report</span></span>
<span data-ttu-id="800ba-165">คุณมีตัวเลือกมากมายสำหรับการส่งออกรายงานที่มีการแบ่งหน้า รวมทั้ง PDF, Word, XML, PowerPoint, Excel และอื่นๆ อีกมากมาย</span><span class="sxs-lookup"><span data-stu-id="800ba-165">You have a variety of options for exporting paginated reports, including PDF, Word, XML, PowerPoint, Excel, and more.</span></span> <span data-ttu-id="800ba-166">เมื่อส่งออกรายงาน จะมีการเก็บรักษาการจัดรูปแบบให้มากที่สุดเท่าที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="800ba-166">When exporting, as much of the formatting as possible is preserved.</span></span> <span data-ttu-id="800ba-167">รายงานที่มีการแบ่งหน้าที่ส่งออกไปยัง Excel, Word, PowerPoint, MHTML และ PDF ตัวอย่างเช่น เก็บรักษาการจัดรูปแบบ "พิกเซลสมบูรณ์แบบ"</span><span class="sxs-lookup"><span data-stu-id="800ba-167">Paginated reports exported to Excel, Word, PowerPoint, MHTML, and PDF, for example, keep the "pixel perfect" formatting.</span></span> 

![ภาพหน้าจอที่แสดงรายงานที่มีการแบ่งหน้าที่ส่งออกแล้ว](./media/end-user-paginated-report/power-bi-export-choices.png)

![การส่งออกที่แตกต่างกันสี่ประเภท](./media/end-user-paginated-report/power-bi-four.png)

### <a name="subscribe-to-the-paginated-report"></a><span data-ttu-id="800ba-170">สมัครใช้งานรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="800ba-170">Subscribe to the paginated report</span></span>
<span data-ttu-id="800ba-171">เมื่อคุณสมัครใช้งานรายงานที่มีการแบ่งหน้า Power BI จะส่งอีเมลพร้อมกับรายงานเป็นเอกสารแนบมาให้</span><span class="sxs-lookup"><span data-stu-id="800ba-171">When you subscribe to a paginated report, Power BI sends you an email with the report as an attachment.</span></span> <span data-ttu-id="800ba-172">ในการตั้งค่าการสมัครใช้งานของคุณ คุณเลือกจำนวนครั้งที่คุณต้องการรับอีเมล: รายวัน รายสัปดาห์ รายชั่วโมง หรือรายเดือน</span><span class="sxs-lookup"><span data-stu-id="800ba-172">In setting up your subscription, you choose how often you want to receive the emails: daily, weekly, hourly, or monthly.</span></span> <span data-ttu-id="800ba-173">การสมัครใช้งานประกอบด้วยเอกสารแนบของเอาต์พุตรายงานทั้งหมด ขนาดสูงสุด 25 MB</span><span class="sxs-lookup"><span data-stu-id="800ba-173">The subscription contains an attachment of the entire report output, up to 25MB in size.</span></span> <span data-ttu-id="800ba-174">ส่งออกรายงานทั้งหมดหรือเลือกพารามิเตอร์ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="800ba-174">Export the entire report or choose the parameters ahead of time.</span></span> <span data-ttu-id="800ba-175">เลือกจากไฟล์แนบที่แตกต่างกันมากมาย ได้แก่ Excel, PDF, PowerPoint และอื่น ๆ อีกมากมาย</span><span class="sxs-lookup"><span data-stu-id="800ba-175">Choose from many different attachment types, including Excel, PDF, PowerPoint, and more.</span></span>  

![รูปแบบสำหรับการสมัครใช้งาน](./media/end-user-paginated-report/power-bi-export-choices.png)

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="800ba-177">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="800ba-177">Considerations and troubleshooting</span></span>

- <span data-ttu-id="800ba-178">รายงานที่มีการแบ่งหน้าสามารถปรากฏขึ้นเป็นรายงานว่างเปล่าจนกว่าคุณจะเลือกพารามิเตอร์ และเลือก **ดูรายงาน**</span><span class="sxs-lookup"><span data-stu-id="800ba-178">A paginated report can appear blank until you select parameters and choose **View report**.</span></span>

- <span data-ttu-id="800ba-179">หากคุณไม่มีรายงานที่มีการแบ่งหน้า อาจเป็นเพราะไม่มีใครแบ่งปันรายงานประเภทนี้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="800ba-179">If you don't have any paginated reports, it could be because nobody has shared this type of report with you.</span></span> <span data-ttu-id="800ba-180">นอกจากนี้ยังอาจหมายความว่าผู้ดูแลระบบของคุณยังไม่ได้เปิดใช้งานรายงานที่มีการแบ่งหน้าสำหรับคุณอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="800ba-180">It could also mean that your system administrator hasn't enabled paginated reports for you.</span></span> 

 

## <a name="next-steps"></a><span data-ttu-id="800ba-181">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="800ba-181">Next steps</span></span>
- [<span data-ttu-id="800ba-182">รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="800ba-182">Power BI reports</span></span>](end-user-reports.md)
- [<span data-ttu-id="800ba-183">รายงานที่มีการแบ่งหน้าใน Power BI คำถามที่ถามบ่อย</span><span class="sxs-lookup"><span data-stu-id="800ba-183">Paginated reports in Power BI: FAQ</span></span>](../paginated-reports/paginated-reports-faq.md)
- <span data-ttu-id="800ba-184">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="800ba-184">More questions?</span></span> <span data-ttu-id="800ba-185">ลองไปที่ [ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="800ba-185">Try the [Power BI Community](https://community.powerbi.com/).</span></span>
