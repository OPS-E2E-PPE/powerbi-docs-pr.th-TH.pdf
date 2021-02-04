---
title: ทำงานกับการรวม (ผลรวม ค่าเฉลี่ย และอื่นๆ) ในบริการของ Power BI
description: เรียนรู้วิธีการเปลี่ยนการรวมในแผนภูมิ (ผลรวม ค่าเฉลี่ย ค่าสูงสุด และอื่นๆ) ในบริการของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 06/16/2020
ms.custom: seodec18
LocalizationGroup: Reports
ms.openlocfilehash: 4ed1d6c68549e621f42b23d05a061e7fe1c9e230
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96395428"
---
# <a name="work-with-aggregates-sum-average-and-so-on-in-the-power-bi-service"></a><span data-ttu-id="f60ac-103">ทำงานกับการรวม (ผลรวม ค่าเฉลี่ย และอื่นๆ) ในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="f60ac-103">Work with aggregates (sum, average, and so on) in the Power BI service</span></span>

## <a name="what-is-an-aggregate"></a><span data-ttu-id="f60ac-104">การรวมคืออะไร?</span><span class="sxs-lookup"><span data-stu-id="f60ac-104">What is an aggregate?</span></span>

<span data-ttu-id="f60ac-105">ในบางครั้งคุณต้องการรวมค่าต่าง ๆ ทางคณิตศาสตร์ในข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="f60ac-105">Sometimes you want to mathematically combine values in your data.</span></span> <span data-ttu-id="f60ac-106">การดำเนินการทางคณิตศาสตร์อาจเป็น การบวก การเฉลี่ย ค่าสูงสุด การนับจำนวน และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f60ac-106">The mathematical operation could be sum, average, maximum, count, and so on.</span></span> <span data-ttu-id="f60ac-107">เมื่อคุณรวมค่าในข้อมูลของคุณ นั่นเรียกว่า *การรวม*</span><span class="sxs-lookup"><span data-stu-id="f60ac-107">When you combine values in your data, it's called *aggregating*.</span></span> <span data-ttu-id="f60ac-108">ส่วนผลลัพธ์ของการดำเนินการทางคณิตศาสตร์คือ *การรวม หรือ ค่ารวม*</span><span class="sxs-lookup"><span data-stu-id="f60ac-108">The result of that mathematical operation is an *aggregate*.</span></span>

<span data-ttu-id="f60ac-109">เมื่อบริการของ Power BI และ Power BI Desktop สร้างการแสดงผล อาจมีการรวมข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="f60ac-109">When Power BI service and Power BI Desktop create visualizations, they may aggregate your data.</span></span> <span data-ttu-id="f60ac-110">การรวมมักจะเป็นสิ่งที่คุณต้องการ แต่บางครั้งคุณอาจต้องการรวมค่าในวิธีอื่น</span><span class="sxs-lookup"><span data-stu-id="f60ac-110">Often the aggregate is just what you need, but other times you may want to aggregate the values in a different way.</span></span>  <span data-ttu-id="f60ac-111">ตัวอย่างเช่น การบวก กับ การหาค่าเฉลี่ย</span><span class="sxs-lookup"><span data-stu-id="f60ac-111">For example, a sum versus an average.</span></span> <span data-ttu-id="f60ac-112">มีหลายวิธีที่จะจัดการ และเปลี่ยนการรวมที่ Power BI ใช้ในการแสดงผลข้อมูลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="f60ac-112">There are several different ways to manage and change the aggregate Power BI uses in a visualization.</span></span>

<span data-ttu-id="f60ac-113">ก่อนอื่น มาดูที่ *ชนิด* ของข้อมูล เนื่องจากชนิดของข้อมูลกำหนดวิธีการและ Power BI สามารถรวมได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="f60ac-113">First, let's take a look at data *types* because the type of data determines how, and whether, Power BI can aggregate it.</span></span>

## <a name="types-of-data"></a><span data-ttu-id="f60ac-114">ชนิดของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f60ac-114">Types of data</span></span>

<span data-ttu-id="f60ac-115">ชุดข้อมูลส่วนใหญ่มีชนิดของข้อมูลมากกว่าหนึ่งชนิด</span><span class="sxs-lookup"><span data-stu-id="f60ac-115">Most datasets have more than one type of data.</span></span> <span data-ttu-id="f60ac-116">ในระดับพื้นฐานสุด ข้อมูลเป็นตัวเลขหรือไม่เป็น</span><span class="sxs-lookup"><span data-stu-id="f60ac-116">At the most basic level, the data is either numeric or it isn't.</span></span> <span data-ttu-id="f60ac-117">Power BI สามารถรวบรวมข้อมูลตัวเลขโดยใช้การบวก การหาค่าเฉลี่ย การนับจำนวน ค่าต่ำสุด ค่าความแปรปรวน และอีกมากมาย</span><span class="sxs-lookup"><span data-stu-id="f60ac-117">Power BI can aggregate numeric data using a sum, average, count, minimum, variance, and much more.</span></span> <span data-ttu-id="f60ac-118">นอกจากนี้ บริการยังสามารถรวมข้อมูลที่เป็นข้อความ ซึ่งมักเรียกว่าข้อมูล *แบบจัดกลุ่ม* ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="f60ac-118">The service can even aggregate textual data, often called *categorical* data.</span></span> <span data-ttu-id="f60ac-119">หากคุณพยายามที่จะรวมเขตข้อมูลแบบจัดกลุ่มโดยการใส่ไว้ในบักเก็ตที่เป็นตัวเลขเท่านั้น เช่น **ค่า** หรือ **คำแนะนำเครื่องมือ** Power BI จะนับจำนวนครั้งของแต่ละประเภท หรือนับจำนวนครั้งที่ไม่ซ้ำกันสำหรับแต่ละประเภท</span><span class="sxs-lookup"><span data-stu-id="f60ac-119">If you try to aggregate a categorical field by placing it in a numeric-only bucket like **Values** or **Tooltips**, Power BI will count the occurrences of each category or count the distinct occurrences of each category.</span></span> <span data-ttu-id="f60ac-120">ข้อมูลชนิดพิเศษ เช่น วันที่ ก็มีตัวเลือกการรวมของตัวเอง เช่น: ก่อนสุด, หลังสุด, แรกสุด และสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="f60ac-120">Special types of data, like dates, have a few of their own aggregate options: earliest, latest, first, and last.</span></span>

<span data-ttu-id="f60ac-121">ในตัวอย่างด้านล่าง:</span><span class="sxs-lookup"><span data-stu-id="f60ac-121">In the example below:</span></span>

- <span data-ttu-id="f60ac-122">**หน่วยที่ขาย** และ **ราคาผลิต** เป็นคอลัมน์ที่ประกอบด้วยข้อมูลตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f60ac-122">**Units Sold** and **Manufacturing Price** are columns that contain numeric data</span></span>

- <span data-ttu-id="f60ac-123">**เซกเมนต์**, **ประเทศ**, **ผลิตภัณฑ์**, **เดือน** และ **ชื่อเดือน** เป็นข้อมูลตามประเภท</span><span class="sxs-lookup"><span data-stu-id="f60ac-123">**Segment**, **Country**, **Product**, **Month**, and **Month Name** contain categorical data</span></span>

   ![สกรีนช็อตของชุดข้อมูลตัวอย่าง](media/service-aggregates/power-bi-aggregate-chart.png)

<span data-ttu-id="f60ac-125">เมื่อสร้างการแสดงผลข้อมูลด้วยภาพใน บริการจะรวมเขตข้อมูลตัวเลข (ค่าเริ่มต้นคือ *การบวก*) ตามเขตข้อมูลแบบจัดกลุ่มบางตัว</span><span class="sxs-lookup"><span data-stu-id="f60ac-125">When creating a visualization in Power BI, the service will aggregate numeric fields (the default is *sum*) over some categorical field.</span></span>  <span data-ttu-id="f60ac-126">ตัวอย่างเช่น "หน่วยที่ขาย **ตามผลิตภัณฑ์** _", “หน่วยที่ขาย _\*_ตามเดือน_*_”, และ "ราคาผลิต _*_ตามเซ็กเมนต์_\*_"</span><span class="sxs-lookup"><span data-stu-id="f60ac-126">For example, "Units Sold ***by Product** _", "Units Sold _*_by Month_*_" and "Manufacturing Price _*_by Segment_\*_".</span></span> <span data-ttu-id="f60ac-127">Power BI อ้างอิงถึงเขตข้อมูลตัวเลขบางตัวเป็น _*หน่วยวัด*\*</span><span class="sxs-lookup"><span data-stu-id="f60ac-127">Power BI refers to some numeric fields as _\*measures\*\*.</span></span> <span data-ttu-id="f60ac-128">ซึ่งง่ายต่อการระบุหน่วยวัดในตัวแก้ไขรายงาน Power BI - รายการ **เขตข้อมูล** แสดงหน่วยวัดที่มีสัญลักษณ์ ∑ ถัดจากรายการเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f60ac-128">It's easy to identify measures in the Power BI report editor -- The **Fields** list shows measures with the ∑ symbol next to them.</span></span> <span data-ttu-id="f60ac-129">โปรดดูหัวข้อ [ตัวแก้ไขรายงาน...ลองสำรวจดู](service-the-report-editor-take-a-tour.md) สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f60ac-129">See [The report editor... take a tour](service-the-report-editor-take-a-tour.md) for more info.</span></span>

![สกรีนช็อตของ Power BI พร้อมรายการเขตข้อมูลที่เรียกใช้](media/service-aggregates/power-bi-aggregate-fields.png)

## <a name="why-dont-aggregates-work-the-way-i-want-them-to"></a><span data-ttu-id="f60ac-131">ทำไมการรวมไม่ทำอย่างที่ฉันต้องการ?</span><span class="sxs-lookup"><span data-stu-id="f60ac-131">Why don't aggregates work the way I want them to?</span></span>

<span data-ttu-id="f60ac-132">การทำงานกับการรวมในบริการของ Power BI สามารถทำให้เกิดความสับสนได้</span><span class="sxs-lookup"><span data-stu-id="f60ac-132">Working with aggregates in Power BI service can be confusing.</span></span> <span data-ttu-id="f60ac-133">บางทีคุณอาจมีเขตข้อมูลตัวเลขและ Power BI จะไม่อนุญาตให้คุณเปลี่ยนแปลงการรวม</span><span class="sxs-lookup"><span data-stu-id="f60ac-133">Maybe you have a numeric field and Power BI won't let you change the aggregation.</span></span> <span data-ttu-id="f60ac-134">หรือบางทีคุณมีเขตข้อมูล เช่น ปี และคุณไม่ต้องการรวม คุณเพียงแค่ต้องการนับจำนวนครั้งที่ปรากฏ</span><span class="sxs-lookup"><span data-stu-id="f60ac-134">Or maybe you have a field, like a year, and you don't want to aggregate it, you just want to count the number of occurrences.</span></span>

<span data-ttu-id="f60ac-135">โดยทั่วไปแล้ว ปัญหาเบื้องต้นคือการกำหนดเขตข้อมูลในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f60ac-135">Typically, the underlying issue is the field definition in the dataset.</span></span> <span data-ttu-id="f60ac-136">บางทีเจ้าของชุดข้อมูลได้กำหนดเขตข้อมูลเป็นข้อความและนั่นเป็นเหตุผลว่าทำไม Power BI จึงไม่สามารถหาผลรวมหรือหาค่าเฉลี่ยได้</span><span class="sxs-lookup"><span data-stu-id="f60ac-136">Maybe the dataset owner defined the field as text and that explains why Power BI can't sum or average it.</span></span> <span data-ttu-id="f60ac-137">ขออภัยที่ [เฉพาะเจ้าของชุดข้อมูลเท่านั้น ที่สามารถเปลี่ยนการจัดประเภทของเขตข้อมูลได้](../transform-model/desktop-measures.md)</span><span class="sxs-lookup"><span data-stu-id="f60ac-137">Unfortunately, [only the dataset owner can change the way a field is categorized](../transform-model/desktop-measures.md).</span></span> <span data-ttu-id="f60ac-138">ดังนั้น หากคุณมีสิทธิ์ระดับเจ้าของชุดข้อมูล คุณจะสามารถแก้ไขปัญหานี้ได้ ทั้งในเดสก์ท็อปหรือโปรแกรมที่ใช้สร้างชุดข้อมูล (เช่น Excel)</span><span class="sxs-lookup"><span data-stu-id="f60ac-138">So if you have owner permissions to the dataset, either in Desktop or the program used to create the dataset (for example, Excel), you can fix this problem.</span></span> <span data-ttu-id="f60ac-139">มิฉะนั้น คุณจะต้องติดต่อเจ้าของชุดข้อมูลเพื่อขอความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="f60ac-139">Otherwise, you'll need to contact the dataset owner for help.</span></span>  

<span data-ttu-id="f60ac-140">เรามีส่วนพิเศษที่ท้ายของบทความนี้ ที่เรียกว่า [**ข้อควรพิจารณาและการแก้ไขปัญหา**](#considerations-and-troubleshooting)</span><span class="sxs-lookup"><span data-stu-id="f60ac-140">There is a special section at the end of this article called [**Considerations and troubleshooting**](#considerations-and-troubleshooting).</span></span> <span data-ttu-id="f60ac-141">ซึ่งมีคำแนะนำและแนวทาง</span><span class="sxs-lookup"><span data-stu-id="f60ac-141">It provides tips and guidance.</span></span> <span data-ttu-id="f60ac-142">ถ้าคุณไม่พบคำตอบของคุณที่นั่น กรุณาโพสต์คำถามของคุณบน[ฟอรั่มชุมชน Power BI](https://community.powerbi.com)</span><span class="sxs-lookup"><span data-stu-id="f60ac-142">If you don't find your answer there, post your question on the [Power BI Community forum](https://community.powerbi.com).</span></span> <span data-ttu-id="f60ac-143">คุณจะได้รับคำตอบอย่างรวดเร็วจากทีมงาน Power BI โดยตรง</span><span class="sxs-lookup"><span data-stu-id="f60ac-143">You'll get a quick response directly from the Power BI team.</span></span>

## <a name="change-how-a-numeric-field-is-aggregated"></a><span data-ttu-id="f60ac-144">เปลี่ยนวิธีการรวมเขตข้อมูลตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f60ac-144">Change how a numeric field is aggregated</span></span>

<span data-ttu-id="f60ac-145">สมมุติว่าคุณมีแผนภูมิที่หาผลรวม จำนวนหน่วยที่ขายได้สำหรับผลิตภัณฑ์ต่าง ๆ แต่คุณอยากได้ค่าเฉลี่ยแทน</span><span class="sxs-lookup"><span data-stu-id="f60ac-145">Say you have a chart that sums the units sold for different products, but you'd rather have the average.</span></span>

1. <span data-ttu-id="f60ac-146">สร้าง **แผนภูมิคอลัมน์แบบคลัสเตอร์** ที่ใช้หน่วยวัดและประเภท</span><span class="sxs-lookup"><span data-stu-id="f60ac-146">Create a **Clustered column chart** that uses a measure and a category.</span></span> <span data-ttu-id="f60ac-147">ในตัวอย่างนี้ เรากำลังใช้หน่วยที่ขายเป็นผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f60ac-147">In this example, we're using Units Sold by Product.</span></span>  <span data-ttu-id="f60ac-148">ตามค่าเริ่มต้น Power BI สร้างแผนภูมิที่หาผลรวมหน่วยที่ขายได้ (ลากหน่วยวัดไปยังช่อง **ค่า**) สำหรับแต่ละผลิตภัณฑ์ (ลากประเภทไปยังช่อง **แกน**)</span><span class="sxs-lookup"><span data-stu-id="f60ac-148">By default, Power BI creates a chart that sums the units sold (drag the measure into the **Value** well) for each product (drag the category into the **Axis** well).</span></span>

   ![สกรีนช็อตของแผนภูมิ บานหน้าต่างการแสดงผลข้อมูลด้วยภาพและรายการเขตข้อมูลที่มีผลรวมที่เรียกใช้](media/service-aggregates/power-bi-aggregate-sum.png)

1. <span data-ttu-id="f60ac-150">ในบานหน้าต่าง **การแสดงผลข้อมูลด้วยภาพ** ให้คลิกขวาที่หน่วยวัด แล้วเลือกชนิดการรวมที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="f60ac-150">In the **Visualizations** pane, right-click the measure, and select the aggregate type you need.</span></span> <span data-ttu-id="f60ac-151">ในกรณีนี้ เรากำลังเลือก **ค่าเฉลี่ย**</span><span class="sxs-lookup"><span data-stu-id="f60ac-151">In this case, we're selecting **Average**.</span></span> <span data-ttu-id="f60ac-152">ถ้าคุณไม่เห็นการรวมที่คุณต้องการ โปรดดูส่วน [**ข้อควรพิจารณาและการแก้ไขปัญหา**](#considerations-and-troubleshooting)</span><span class="sxs-lookup"><span data-stu-id="f60ac-152">If you don't see the aggregation you need, see the [**Considerations and troubleshooting**](#considerations-and-troubleshooting) section.</span></span>

   ![สกรีนช็อตของรายการการรวมที่มีค่าเฉลี่ยที่เลือกและเรียกใช้](media/service-aggregates/power-bi-aggregate-average.png)

   > [!NOTE]
   > <span data-ttu-id="f60ac-154">ตัวเลือกที่มีอยู่ในรายการแบบหล่นลงจะแตกต่างกันไปขึ้นอยู่กับ 1) เขตข้อมูลที่เลือกและ 2) วิธีที่เจ้าของชุดข้อมูลจัดประเภทเขตข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="f60ac-154">The options available in the drop-down list will vary depending on 1) the field selected and 2) the way the dataset owner categorized that field.</span></span>

1. <span data-ttu-id="f60ac-155">การแสดงภาพของคุณ ตอนนี้รวมโดยการเฉลี่ย</span><span class="sxs-lookup"><span data-stu-id="f60ac-155">Your visualization is now using aggregated by average.</span></span>

   ![สกรีนช็อตของแผนภูมิขณะนี้แสดงค่าเฉลี่ยของหน่วยที่ขายตามผลิตภัณฑ์](media/service-aggregates/power-bi-aggregate-average-2.png)

## <a name="ways-to-aggregate-your-data"></a><span data-ttu-id="f60ac-157">วิธีการรวมข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="f60ac-157">Ways to aggregate your data</span></span>

<span data-ttu-id="f60ac-158">บางตัวเลือกที่อาจมีให้สำหรับการรวมเขตข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="f60ac-158">Some of the options that may be available for aggregating a field:</span></span>

- <span data-ttu-id="f60ac-159">**ไม่ต้องทำการสรุป**</span><span class="sxs-lookup"><span data-stu-id="f60ac-159">**Do Not Summarize**.</span></span> <span data-ttu-id="f60ac-160">เมื่อเลือกตัวเลือกนี้ Power BI จะปฏิบัติต่อแต่ละค่าในเขตข้อมูลนั้นแยกกันและไม่ได้สรุปค่า</span><span class="sxs-lookup"><span data-stu-id="f60ac-160">With this option chosen, Power BI treats each value in that field  separately and doesn't summarize them.</span></span> <span data-ttu-id="f60ac-161">ใช้ตัวเลือกนี้ถ้าคุณมีคอลัมน์ตัวเลข ID ที่บริการไม่ควรนำมารวมผล</span><span class="sxs-lookup"><span data-stu-id="f60ac-161">Use this option if you have a numeric ID column that the service shouldn't sum.</span></span>

- <span data-ttu-id="f60ac-162">**ผลรวม**</span><span class="sxs-lookup"><span data-stu-id="f60ac-162">**Sum**.</span></span> <span data-ttu-id="f60ac-163">บวกค่าทั้งหมดในเขตข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="f60ac-163">Adds all the values in that field up.</span></span>

- <span data-ttu-id="f60ac-164">**ค่าเฉลี่ย**</span><span class="sxs-lookup"><span data-stu-id="f60ac-164">**Average**.</span></span> <span data-ttu-id="f60ac-165">คำนวนค่าเฉลี่ยเลขคณิตของค่าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f60ac-165">Takes an arithmetic mean of the values.</span></span>

- <span data-ttu-id="f60ac-166">**ต่ำสุด**</span><span class="sxs-lookup"><span data-stu-id="f60ac-166">**Minimum**.</span></span> <span data-ttu-id="f60ac-167">แสดงค่าที่น้อยที่สุด</span><span class="sxs-lookup"><span data-stu-id="f60ac-167">Shows the smallest value.</span></span>

- <span data-ttu-id="f60ac-168">**สูงสุด**</span><span class="sxs-lookup"><span data-stu-id="f60ac-168">**Maximum**.</span></span> <span data-ttu-id="f60ac-169">แสดงค่าที่มากที่สุด</span><span class="sxs-lookup"><span data-stu-id="f60ac-169">Shows the largest value.</span></span>

- <span data-ttu-id="f60ac-170">**นับจำนวน (ไม่เว้นว่าง)**</span><span class="sxs-lookup"><span data-stu-id="f60ac-170">**Count (Not Blanks).**</span></span> <span data-ttu-id="f60ac-171">นับจำนวนของค่าในเขตข้อมูลนั้นที่ไม่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="f60ac-171">Counts the number of values in that field that aren't blank.</span></span>

- <span data-ttu-id="f60ac-172">**นับจำนวน (ค่าที่แตกต่างกัน)**</span><span class="sxs-lookup"><span data-stu-id="f60ac-172">**Count (Distinct).**</span></span> <span data-ttu-id="f60ac-173">นับจำนวนค่าที่แตกต่างกันในเขตข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="f60ac-173">Counts the number of different values in that field.</span></span>

- <span data-ttu-id="f60ac-174">**ค่าเบี่ยงเบนมาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="f60ac-174">**Standard deviation.**</span></span>

- <span data-ttu-id="f60ac-175">**ผลต่าง**</span><span class="sxs-lookup"><span data-stu-id="f60ac-175">**Variance**.</span></span>

- <span data-ttu-id="f60ac-176">**ค่ากลาง**</span><span class="sxs-lookup"><span data-stu-id="f60ac-176">**Median**.</span></span>  <span data-ttu-id="f60ac-177">แสดงค่ามัธยฐาน (ค่าตรงกลาง)</span><span class="sxs-lookup"><span data-stu-id="f60ac-177">Shows the median (middle) value.</span></span> <span data-ttu-id="f60ac-178">ค่านี้มีจำนวนรายการด้านบนและด้านล่างเท่ากัน</span><span class="sxs-lookup"><span data-stu-id="f60ac-178">This value has the same number of items above and below.</span></span>  <span data-ttu-id="f60ac-179">หากมีค่ากลางสองค่า Power BI จะหาค่าเฉลี่ย</span><span class="sxs-lookup"><span data-stu-id="f60ac-179">If there are two medians, Power BI averages them.</span></span>

<span data-ttu-id="f60ac-180">ตัวอย่างเช่น ข้อมูลนี้:</span><span class="sxs-lookup"><span data-stu-id="f60ac-180">For example, this data:</span></span>

| <span data-ttu-id="f60ac-181">ประเทศ</span><span class="sxs-lookup"><span data-stu-id="f60ac-181">Country</span></span> | <span data-ttu-id="f60ac-182">ยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="f60ac-182">Amount</span></span> |
|:--- |:--- |
| <span data-ttu-id="f60ac-183">สหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="f60ac-183">USA</span></span> |<span data-ttu-id="f60ac-184">100</span><span class="sxs-lookup"><span data-stu-id="f60ac-184">100</span></span> |
| <span data-ttu-id="f60ac-185">สหราชอาณาจักร</span><span class="sxs-lookup"><span data-stu-id="f60ac-185">UK</span></span> |<span data-ttu-id="f60ac-186">150</span><span class="sxs-lookup"><span data-stu-id="f60ac-186">150</span></span> |
| <span data-ttu-id="f60ac-187">แคนาดา</span><span class="sxs-lookup"><span data-stu-id="f60ac-187">Canada</span></span> |<span data-ttu-id="f60ac-188">100</span><span class="sxs-lookup"><span data-stu-id="f60ac-188">100</span></span> |
| <span data-ttu-id="f60ac-189">เยอรมนี</span><span class="sxs-lookup"><span data-stu-id="f60ac-189">Germany</span></span> |<span data-ttu-id="f60ac-190">125</span><span class="sxs-lookup"><span data-stu-id="f60ac-190">125</span></span> |
| <span data-ttu-id="f60ac-191">ฝรั่งเศส</span><span class="sxs-lookup"><span data-stu-id="f60ac-191">France</span></span> | |
| <span data-ttu-id="f60ac-192">ญี่ปุ่น</span><span class="sxs-lookup"><span data-stu-id="f60ac-192">Japan</span></span> |<span data-ttu-id="f60ac-193">125</span><span class="sxs-lookup"><span data-stu-id="f60ac-193">125</span></span> |
| <span data-ttu-id="f60ac-194">ออสเตรเลีย</span><span class="sxs-lookup"><span data-stu-id="f60ac-194">Australia</span></span> |<span data-ttu-id="f60ac-195">150</span><span class="sxs-lookup"><span data-stu-id="f60ac-195">150</span></span> |

<span data-ttu-id="f60ac-196">จะให้ผลลัพธ์ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f60ac-196">Would give the following results:</span></span>

- <span data-ttu-id="f60ac-197">**ไม่ต้องสรุป**: จะแสดงค่าแต่ละรายการแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="f60ac-197">**Do Not Summarize**: Each value is shown separately</span></span>

- <span data-ttu-id="f60ac-198">**ผลรวม**: 750</span><span class="sxs-lookup"><span data-stu-id="f60ac-198">**Sum**: 750</span></span>

- <span data-ttu-id="f60ac-199">**ค่าเฉลี่ย**: 125</span><span class="sxs-lookup"><span data-stu-id="f60ac-199">**Average**: 125</span></span>

- <span data-ttu-id="f60ac-200">**สูงสุด**:  150</span><span class="sxs-lookup"><span data-stu-id="f60ac-200">**Maximum**:  150</span></span>

- <span data-ttu-id="f60ac-201">**ต่ำสุด**: 100</span><span class="sxs-lookup"><span data-stu-id="f60ac-201">**Minimum**: 100</span></span>

- <span data-ttu-id="f60ac-202">**นับจำนวน (ไม่เว้นว่าง):** 6</span><span class="sxs-lookup"><span data-stu-id="f60ac-202">**Count (Not Blanks):** 6</span></span>

- <span data-ttu-id="f60ac-203">**จำนวน (เขต):** 4</span><span class="sxs-lookup"><span data-stu-id="f60ac-203">**Count (Distinct):** 4</span></span>

- <span data-ttu-id="f60ac-204">**ค่าเบี่ยงเบนมาตรฐาน:** 20.4124145...</span><span class="sxs-lookup"><span data-stu-id="f60ac-204">**Standard deviation:** 20.4124145...</span></span>

- <span data-ttu-id="f60ac-205">**ผลต่าง:** 416.666...</span><span class="sxs-lookup"><span data-stu-id="f60ac-205">**Variance:** 416.666...</span></span>

- <span data-ttu-id="f60ac-206">**ค่ากลาง:** 125</span><span class="sxs-lookup"><span data-stu-id="f60ac-206">**Median:** 125</span></span>

## <a name="create-an-aggregate-using-a-category-text-field"></a><span data-ttu-id="f60ac-207">สร้างการรวมโดยใช้เขตข้อมูลประเภท (ข้อความ)</span><span class="sxs-lookup"><span data-stu-id="f60ac-207">Create an aggregate using a category (text) field</span></span>

<span data-ttu-id="f60ac-208">คุณยังสามารถรวมเขตข้อมูลที่ไม่ใช่ตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f60ac-208">You can also aggregate a non-numeric field.</span></span> <span data-ttu-id="f60ac-209">ตัวอย่างเช่น ถ้าคุณมีเขตข้อมูลชื่อผลิตภัณฑ์ คุณสามารถเพิ่มเป็นค่า และตั้งค่าเป็น **นับจำนวน**, **นับจำนวนที่แตกต่างกัน**, **แรก** หรือ **สุดท้าย** ได้</span><span class="sxs-lookup"><span data-stu-id="f60ac-209">For example, if you have a product name field, you can add it as a value and then set it to **Count**, **Distinct count**, **First**, or **Last**.</span></span>

1. <span data-ttu-id="f60ac-210">ลากเขตข้อมูล **ผลิตภัณฑ์** ลงในช่อง **ค่า**</span><span class="sxs-lookup"><span data-stu-id="f60ac-210">Drag the **Product** field into the **Values** well.</span></span> <span data-ttu-id="f60ac-211">โดยทั่วไป ช่อง **ค่า** มักใช้กับเขตข้อมูลตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f60ac-211">The **Values** well is typically used for numeric fields.</span></span> <span data-ttu-id="f60ac-212">Power BI รู้ว่าเขตข้อมูลนี้เป็นเขตข้อมูลข้อความ ตั้งค่าการรวมเป็น **ไม่ต้องทำการสรุป** และแสดงตารางที่มีหนึ่งคอลัมน์ให้คุณ</span><span class="sxs-lookup"><span data-stu-id="f60ac-212">Power BI recognizes that this field is a text field, sets the aggregate to **Do not summarize**, and presents you with a single-column table.</span></span>

   ![สกรีนช็อตของเขตข้อมูลผลิตภัณฑ์ในช่องค่า](media/service-aggregates/power-bi-aggregate-value.png)

1. <span data-ttu-id="f60ac-214">ถ้าคุณเปลี่ยนการรวมจากค่าเริ่มต้น **ไม่ต้องทำการสรุป** ไปเป็น **นับจำนวน (ค่าที่แตกต่างกัน)** Power BI จะนับจำนวนของผลิตภัณฑ์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="f60ac-214">If you change the aggregation from the default **Do not summarize** to **Count (Distinct)**, Power BI counts the number of different products.</span></span> <span data-ttu-id="f60ac-215">ในกรณีนี้ มีค่าเป็นสี่</span><span class="sxs-lookup"><span data-stu-id="f60ac-215">In this case, there are four.</span></span>
  
   ![สกรีนช็อตของการนับจำนวนที่แตกต่างกันของผลิตภัณฑ์](media/service-aggregates/power-bi-aggregate-count.png)

1. <span data-ttu-id="f60ac-217">และ ถ้าคุณเปลี่ยนการรวมเป็น **นับจำนวน** Power BI จะนับจำนวนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f60ac-217">And if you change the aggregation to **Count**, Power BI counts the total number.</span></span> <span data-ttu-id="f60ac-218">ในกรณีนี้ มี **ผลิตภัณฑ์** เจ็ดรายการ</span><span class="sxs-lookup"><span data-stu-id="f60ac-218">In this case, there are seven entries for **Product**.</span></span>

   ![สกรีนช็อตของการนับจำนวนของผลิตภัณฑ์](media/service-aggregates/power-bi-aggregate-count-2.png)

1. <span data-ttu-id="f60ac-220">Power BI จะแบ่งการนับจำนวนตามผลิตภัณฑ์โดยการลากเขตข้อมูลเดียวกัน (ในกรณีนี้คือ **ผลิตภัณฑ์**) ลงในช่อง **ค่า** และปล่อยให้เป็นการรวมค่าเริ่มต้น **ไม่ต้องทำการสรุป**</span><span class="sxs-lookup"><span data-stu-id="f60ac-220">By dragging the same field (in this case **Product**) into the **Values** well, and leaving the default aggregation **Do not summarize**, Power BI breaks down the count by product.</span></span>

   ![สกรีนช็อตของผลิตภัณฑ์และการนับจำนวนของผลิตภัณฑ์](media/service-aggregates/power-bi-aggregate-final.png)

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="f60ac-222">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="f60ac-222">Considerations and Troubleshooting</span></span>

<span data-ttu-id="f60ac-223">Q:  เหตุใดฉันจึงไม่มีตัวเลือกให้ **ไม่ต้องทำการสรุป**?</span><span class="sxs-lookup"><span data-stu-id="f60ac-223">Q:  Why don't I have a **Do not summarize** option?</span></span>

<span data-ttu-id="f60ac-224">A:  เขตข้อมูลที่คุณเลือกมีแนวโน้มว่าเป็นหน่วยวัดที่คำนวณในแบบจำลองหลายมิติหรือหน่วยวัดที่สร้างขึ้นใน Excel หรือ [Power BI Desktop](../transform-model/desktop-measures.md)</span><span class="sxs-lookup"><span data-stu-id="f60ac-224">A:  The field you've selected is likely a calculated measure in a multidimensional model, or a measure created in Excel or [Power BI Desktop](../transform-model/desktop-measures.md).</span></span> <span data-ttu-id="f60ac-225">แต่ละหน่วยวัดจะมีสูตรคำนวณที่ตายตัวของตนเอง</span><span class="sxs-lookup"><span data-stu-id="f60ac-225">Each measure has its own hard-coded formula.</span></span> <span data-ttu-id="f60ac-226">คุณไม่สามารถเปลี่ยนการรวมที่ Power BI ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="f60ac-226">You can’t change the aggregation Power BI uses.</span></span> <span data-ttu-id="f60ac-227">ตัวอย่างเช่น ถ้าใช้ผลรวม จะต้องเป็นผลรวมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f60ac-227">For example, if it’s a sum, it can only be a sum.</span></span> <span data-ttu-id="f60ac-228">รายการ **เขตข้อมูล** แสดง *หน่วยวัด* ด้วยสัญลักษณ์เครื่องคิดเลข</span><span class="sxs-lookup"><span data-stu-id="f60ac-228">The **Fields** list shows *measures* with the calculator symbol.</span></span>

<span data-ttu-id="f60ac-229">Q:  เขตข้อมูลฉัน **เป็น** ตัวเลข ทำไมฉันมีตัวเลือกแค่ **นับจำนวน** และ **นับจำนวนที่แตกต่างกัน**?</span><span class="sxs-lookup"><span data-stu-id="f60ac-229">Q:  My field **is** numeric, why are my only choices **Count** and **Distinct count**?</span></span>

<span data-ttu-id="f60ac-230">คำตอบที่ 1:  เหตุผลที่เป็นไปได้คือ เจ้าชุดข้อมูล *ไม่* จัดประเภทเขตข้อมูลเป็นตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f60ac-230">A1:  The likely explanation is that the dataset owner has *not* classified the field as a number.</span></span> <span data-ttu-id="f60ac-231">ตัวอย่างเช่น ถ้าชุดข้อมูลมีเขตข้อมูล **ปี** เจ้าของชุดข้อมูลอาจจัดประเภทค่าเป็นข้อความ</span><span class="sxs-lookup"><span data-stu-id="f60ac-231">For example, if a dataset has a **year** field, the dataset owner may categorize the value as text.</span></span> <span data-ttu-id="f60ac-232">ซึ่งอาจเป็นไปได้ว่า Power BI จะนับเขตข้อมูล **ปี** (ตัวอย่างเช่น จำนวนคนที่เกิดในปี 1974)</span><span class="sxs-lookup"><span data-stu-id="f60ac-232">It's more likely that Power BI will count the **year** field (for example, number of people born in 1974).</span></span> <span data-ttu-id="f60ac-233">ซึ่งมีโอกาสน้อยที่ Power BI จะหาผลรวมหรือเฉลี่ย</span><span class="sxs-lookup"><span data-stu-id="f60ac-233">It's less likely that Power BI will sum or average it.</span></span> <span data-ttu-id="f60ac-234">ถ้าคุณเป็นเจ้าของ คุณสามารถเปิดชุดข้อมูลใน Power BI Desktop และใช้แท็บ **การสร้างแบบจำลอง** เพื่อเปลี่ยนชนิดข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="f60ac-234">If you're the owner, you can open the dataset in Power BI Desktop and use the **Modeling** tab to change the data type.</span></span>

<span data-ttu-id="f60ac-235">คำตอบที่ 2: ถ้าเขตข้อมูลมีไอคอนเครื่องคิดเลข นั่นหมายความว่าเป็น *หน่วยวัด*</span><span class="sxs-lookup"><span data-stu-id="f60ac-235">A2: If the field has a calculator icon, that means it's a *measure*.</span></span> <span data-ttu-id="f60ac-236">แต่ละหน่วยวัดมีสูตรของตนเองที่เฉพาะเจ้าของชุดข้อมูลเท่านั้นที่สามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="f60ac-236">Each measure has its own formula that only the dataset owner can change.</span></span> <span data-ttu-id="f60ac-237">การคำนวณที่ Power BI ใช้อาจเป็นการรวมอย่างง่าย เช่น ค่าเฉลี่ย หรือผลรวม</span><span class="sxs-lookup"><span data-stu-id="f60ac-237">The calculation Power BI uses may be a simple aggregation like an average or sum.</span></span> <span data-ttu-id="f60ac-238">ซึ่งยังอาจเป็นการคำนวณที่ซับซ้อนขึ้น เช่น "เปอร์เซ็นต์ของผลกระทบต่อประเภทหลัก" หรือ "ผลรวมสะสมตั้งแต่ต้นปี"</span><span class="sxs-lookup"><span data-stu-id="f60ac-238">It may also be something more complicated like a "percent of contribution to parent category" or "running total since start of the year".</span></span> <span data-ttu-id="f60ac-239">Power BI จะไม่หาผลรวมหรือค่าเฉลี่ยของผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="f60ac-239">Power BI isn't going to sum or average the results.</span></span> <span data-ttu-id="f60ac-240">แต่จะคำนวณใหม่ (โดยใช้สูตรคำนวณที่ตายตัว) สำหรับแต่ละจุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f60ac-240">Instead, it will just recalculate (using the hard-coded formula) for each data point.</span></span>

<span data-ttu-id="f60ac-241">คำตอบที่ 3:  อีกความเป็นไปได้คือ คุณได้ปล่อยเขตข้อมูลลงใน *บักเก็ต* ที่อนุญาตให้ใส่ค่าที่เป็นประเภทเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f60ac-241">A3:  Another possibility is that you've dropped the field into a *bucket* that only allows categorical values.</span></span>  <span data-ttu-id="f60ac-242">ในกรณีนั้น ตัวเลือกของคุณจะมีแค่ นับจำนวนและนับจำนวนที่แตกต่างกันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f60ac-242">In that case, your only options will be count and distinct count.</span></span>

<span data-ttu-id="f60ac-243">คำตอบที่ 4:  และความเป็นไปได้ที่สี่คือ คุณกำลังใช้เขตข้อมูลสำหรับแกน</span><span class="sxs-lookup"><span data-stu-id="f60ac-243">A4:  And a fourth possibility is that you're using the field for an axis.</span></span> <span data-ttu-id="f60ac-244">ตัวอย่างเช่น บนแกนแผนภูมิแท่ง Power BI แสดงหนึ่งแท่งสำหรับแต่ละค่าที่ไม่ซ้ำกัน จะไม่มีรวมค่าของเขตข้อมูลเลย</span><span class="sxs-lookup"><span data-stu-id="f60ac-244">On a bar chart axis, for example, Power BI shows one bar for each distinct value -- it doesn't aggregate the field values at all.</span></span>

>[!NOTE]
><span data-ttu-id="f60ac-245">ข้อยกเว้นของกฎนี้คือ แผนภูมิกระจาย ซึ่ง *จำเป็นต้องมี* การรวมค่าสำหรับแกน X และ Y</span><span class="sxs-lookup"><span data-stu-id="f60ac-245">The exception to this rule is scatter charts, which *require* aggregated values for the X and Y axes.</span></span>

<span data-ttu-id="f60ac-246">Q:  เหตุใดฉันจึงไม่สามารถรวมเขตข้อมูลข้อความสำหรับแหล่งข้อมูล SQL Server Analysis Services (SSAS) ได้?</span><span class="sxs-lookup"><span data-stu-id="f60ac-246">Q:  Why can't I aggregate text fields for SQL Server Analysis Services (SSAS) data sources?</span></span>

<span data-ttu-id="f60ac-247">A:  การเชื่อมต่อแบบสดไปยังโมเดลหลายมิติของ SSAS ไม่อนุญาตให้มีการรวมฝั่งไคลเอ็นต์ใด ๆ รวมถึงครั้งแรก ครั้งสุดท้าย เฉลี่ย ต่ำสุด สูงสุดและผลรวม</span><span class="sxs-lookup"><span data-stu-id="f60ac-247">A:  Live connections to SSAS multidimensional models don't allow any client-side aggregations, including first, last, avg, min, max, and sum.</span></span>

<span data-ttu-id="f60ac-248">Q:  ฉันมีแผนภูมิกระจาย และฉันต้องการให้เขตข้อมูลของฉัน *ไม่* รวม</span><span class="sxs-lookup"><span data-stu-id="f60ac-248">Q:  I have a scatter chart and I want my field to *not* aggregate.</span></span>  <span data-ttu-id="f60ac-249">อย่างไร?</span><span class="sxs-lookup"><span data-stu-id="f60ac-249">How?</span></span>

<span data-ttu-id="f60ac-250">A:  เพิ่มเขตข้อมูลไปยังบักเก็ต **รายละเอียด** และไม่ใส่ในบักเก็ตแกน X หรือ Y</span><span class="sxs-lookup"><span data-stu-id="f60ac-250">A:  Add the field to the **Details** bucket and not to the X or Y axes buckets.</span></span>

<span data-ttu-id="f60ac-251">Q:  เมื่อฉันเพิ่มเขตข้อมูลตัวเลขลงในการแสดงภาพ ส่วนใหญ่ค่าเริ่มต้นคือผลรวม แต่บางทีค่าเริ่มต้นเป็นค่าเฉลี่ย บางทีเป็นการนับจำนวน หรือการรวมอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="f60ac-251">Q:  When I add a numeric field to a visualization, most of them default to sum but some default to average or count or some other aggregation.</span></span>  <span data-ttu-id="f60ac-252">เหตุใดค่าเริ่มต้นจึงไม่ได้เหมือนกันตลอด?</span><span class="sxs-lookup"><span data-stu-id="f60ac-252">Why isn't the default aggregation always the same?</span></span>

<span data-ttu-id="f60ac-253">A:  เจ้าของชุดข้อมูลสามารถตั้งค่าการสรุปเริ่มต้นสำหรับแต่ละเขตข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="f60ac-253">A:  Dataset owners can set the default summarization for each field.</span></span> <span data-ttu-id="f60ac-254">หากคุณเป็นเจ้าของชุดข้อมูล ให้เปลี่ยนการสรุปเริ่มต้นในแท็บ **การสร้างแบบจำลอง** ของ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="f60ac-254">If you're a dataset owner, change the default summarization in the **Modeling** tab of Power BI Desktop.</span></span>

<span data-ttu-id="f60ac-255">Q:  ฉันเป็นเจ้าของชุดข้อมูล และฉันต้องการให้แน่ใจว่า เขตข้อมูลหนึ่งจะไม่มีการรวมเลย</span><span class="sxs-lookup"><span data-stu-id="f60ac-255">Q:  I'm a dataset owner and I want to ensure that a field is never aggregated.</span></span>

<span data-ttu-id="f60ac-256">A:  ใน Power BI Desktop ในแท็บ **การวางรูปแบบ** ตั้งค่า **ชนิดข้อมูล** ให้เป็น **ข้อความ**</span><span class="sxs-lookup"><span data-stu-id="f60ac-256">A:  In Power BI Desktop, in the **Modeling** tab, set **Data type** to **Text**.</span></span>

<span data-ttu-id="f60ac-257">Q:  ฉันไม่เห็น **ไม่ต้องทำการสรุป** เป็นตัวเลือกในรายการแบบหล่นของฉัน</span><span class="sxs-lookup"><span data-stu-id="f60ac-257">Q:  I don't see **Do not summarize** as an option in my drop-down list.</span></span>

<span data-ttu-id="f60ac-258">A:  ลองเอาเขตข้อมูลออก และเพิ่มกลับเข้าไปอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="f60ac-258">A:  Try removing the field and adding it back in.</span></span>

<span data-ttu-id="f60ac-259">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f60ac-259">More questions?</span></span> [<span data-ttu-id="f60ac-260">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="f60ac-260">Try the Power BI Community</span></span>](https://community.powerbi.com/)
