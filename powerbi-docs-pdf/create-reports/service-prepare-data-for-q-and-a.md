---
title: ทำให้ข้อมูล Excel ทำงานได้ดีกับการถามตอบ (Q&A) ใน Power BI
description: ทำให้ข้อมูลของคุณทำงานได้ดีกับการถามตอบใน Power BI ได้อย่างไร
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 05/13/2019
LocalizationGroup: Ask questions of your data
ms.openlocfilehash: 41672fa809544198a053ae41f935e890d83cfa72
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96388114"
---
# <a name="make-excel-data-work-well-with-qa-in-power-bi"></a><span data-ttu-id="f0601-103">ทำให้ข้อมูล Excel ทำงานได้ดีกับการถามตอบ (Q&A) ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="f0601-103">Make Excel data work well with Q&A in Power BI</span></span>
<span data-ttu-id="f0601-104">ถ้าคุณคือบุคคลที่สร้างตัวแบบข้อมูล หรือสร้างเวิร์กบุ๊ก Excel ที่จะใช้กับ Power BI อ่านที่</span><span class="sxs-lookup"><span data-stu-id="f0601-104">If you are a person who creates data models or builds Excel workbooks that will be used with Power BI, read on...</span></span>

<span data-ttu-id="f0601-105">ใน Power BI Q&A สามารถค้นหาข้อมูลที่มีโครงสร้าง และเลือกการแสดงภาพที่เหมาะสมสำหรับคำถามของคุณ - ที่ควรจะทำเครื่องมือดึงดูดความสนใจให้ใช้</span><span class="sxs-lookup"><span data-stu-id="f0601-105">In Power BI, Q&A can search structured data and choose the right visualization for your question -- that's what makes it a compelling tool to use.</span></span>   

<span data-ttu-id="f0601-106">Q&A สามารถทำงานไฟล์ Excel ที่ถูกอัปโหลด ใดๆ ที่มีตาราง ช่วง หรือมีแบบ จำลอง PowerPivot แต่การปรับให้เหมาะสมเพิ่มเติม และคุณคุณทำความสะอาดข้อมูลมากขึ้น ประสิทธิภาพ Q&A จะยิ่งสูงขึ้น</span><span class="sxs-lookup"><span data-stu-id="f0601-106">Q&A can work on any uploaded Excel file that has tables, ranges, or contains a PowerPivot model, but the more optimizations and data cleaning you do, the more robust Q&A performance is.</span></span>  <span data-ttu-id="f0601-107">ถ้าคุณวางแผนที่แชร์รายงานและแดชบอร์ดที่ยึดตามชุดข้อมูลของคุณ คุณจะต้องการให้เพื่อนร่วมงานของคุณมีเวลาถามคำถามที่ง่าย และมีคำตอบที่มีคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="f0601-107">If you plan on sharing reports and dashboards based on your dataset, you'll want your colleagues to have an easy time asking questions and getting quality answers.</span></span>

## <a name="how-qa-works-with-excel"></a><span data-ttu-id="f0601-108">วิธที่ Q&A ทำงานกับ Excel</span><span class="sxs-lookup"><span data-stu-id="f0601-108">How Q&A works with Excel</span></span>
<span data-ttu-id="f0601-109">Q&A มีชุดของหลักภาษาธรรมชาติที่เข้าใจความสามารถในการที่ทำงานกับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="f0601-109">Q&A has a set of core natural language understanding abilities that work across your data.</span></span> <span data-ttu-id="f0601-110">มีคำสำคัญขึ้นอยู่กับบริบทสำหรับการค้นหาในตาราง Excel คอลัมน์ และชื่อเขตข้อมูลจากการคำนวณของคุณ</span><span class="sxs-lookup"><span data-stu-id="f0601-110">It has context-dependent keyword search for your Excel table, column, and calculated field names.</span></span> <span data-ttu-id="f0601-111">นอกจากนี้ยังมีความรู้ที่มีอยู่ภายในวิธีการกรอง เรียงลำดับ จับกลุ่ม เรียงลำดับ และแสดงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f0601-111">It also has built-in knowledge for how to filter, sort, aggregate, group, and display data.</span></span> 

<span data-ttu-id="f0601-112">ตัวอย่างเช่น ในตาราง Excel ที่มีชื่อว่า "Sales" กับคอลัมน์ "Product", "Month", "Units Sold”, “Gross Sales” คุณสามารถถามคำถามเกี่ยวกับเอนทิตีใดๆ เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="f0601-112">For example, in an Excel table named “Sales”, with columns “Product”, “Month”, “Units Sold”, “Gross Sales”, and “Profit”, you could ask questions about any of those entities.</span></span>  <span data-ttu-id="f0601-113">คุณสามารถสอบถามเพื่อแสดงยอดขาย ผลกำไรรวมตามเดือน ผลิตภัณฑ์เรียงลำดับตามหน่วยที่ขายได้ และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="f0601-113">You could ask to show sales, total profit by month, sort products by units sold, and many others.</span></span> <span data-ttu-id="f0601-114">อ่านเพิ่มเติมเกี่ยวกับ[การใช้ถามตอบ (Q&A) ในแดชบอร์ดและรายงาน](power-bi-tutorial-q-and-a.md) และ [ชนิดการแสดงผลข้อมูลด้วยภาพที่คุณสามารถระบุในคิวรีของ Q&A](../visuals/power-bi-visualization-types-for-reports-and-q-and-a.md)</span><span class="sxs-lookup"><span data-stu-id="f0601-114">Read more about [using Q&A in dashboards and reports](power-bi-tutorial-q-and-a.md), and [visualization types you can specify in a Q&A query](../visuals/power-bi-visualization-types-for-reports-and-q-and-a.md).</span></span>

## <a name="prepare-an-excel-dataset-for-qa"></a><span data-ttu-id="f0601-115">เตรียมชุดข้อมูล Excel สำหรับ Q&A</span><span class="sxs-lookup"><span data-stu-id="f0601-115">Prepare an Excel dataset for Q&A</span></span>
<span data-ttu-id="f0601-116">Q&A ใช้ชื่อของตาราง คอลัมน์ และเขตข้อมูลจากการคำนวณเพื่อตอบคำถามเฉพาะข้อมูล ซึ่งหมายความว่าคุณเรียกอะไร เอนทิตีในเวิร์กบุ๊กของคุณมีความสำคัญ</span><span class="sxs-lookup"><span data-stu-id="f0601-116">Q&A relies on the names of tables, columns, and calculated fields to answer data-specific questions, meaning what you call entities in your workbook is important!</span></span>

<span data-ttu-id="f0601-117">ต่อไปนี้เป็นเคล็ดลับบางอย่างสำหรับการทำใช้ Q&A ในเวิร์กบุ๊กของคุณ</span><span class="sxs-lookup"><span data-stu-id="f0601-117">Here are some tips for making the most of Q&A in your workbook.</span></span>

* <span data-ttu-id="f0601-118">ตรวจสอบให้แน่ใจว่า ข้อมูลของคุณอยู่ในตาราง Excel</span><span class="sxs-lookup"><span data-stu-id="f0601-118">Make sure your data is in an Excel table.</span></span> <span data-ttu-id="f0601-119">นี่คือ[วิธีการสร้างตาราง Excel](https://support.office.com/article/Create-an-Excel-table-in-a-worksheet-e81aa349-b006-4f8a-9806-5af9df0ac664)</span><span class="sxs-lookup"><span data-stu-id="f0601-119">Here's [how to create an Excel table](https://support.office.com/article/Create-an-Excel-table-in-a-worksheet-e81aa349-b006-4f8a-9806-5af9df0ac664).</span></span>
* <span data-ttu-id="f0601-120">ตรวจสอบให้แน่ใจว่าชื่อของตาราง คอลัมน์ และเขตข้อมูลที่ถูกคำนวณของคุณ สามารถเข้าใจเป็นคำพูดตามภาษาธรรมชาติได้</span><span class="sxs-lookup"><span data-stu-id="f0601-120">Make sure the names of your tables, columns, and calculated field make sense in natural speech.</span></span>
  
  <span data-ttu-id="f0601-121">ตัวอย่างเช่น ถ้าคุณมีตารางที่มีข้อมูลยอดขาย ให้เรียกตาราง "Sales"</span><span class="sxs-lookup"><span data-stu-id="f0601-121">For example, if you have a table with sales data, call the table “Sales”.</span></span> <span data-ttu-id="f0601-122">ชื่อคอลัมน์เช่น Year”, “Product”, “Sales Rep” และ "Amount" จะทำงานได้ดีกับ Q&A</span><span class="sxs-lookup"><span data-stu-id="f0601-122">Column names like “Year”, “Product”, “Sales Rep”, and “Amount” will work well with Q&A.</span></span>

* <span data-ttu-id="f0601-123">ถ้าเวิร์กบุ๊กของคุณมีตัวแบบข้อมูล Power Pivot คุณสามารถทำการปรับให้เหมาะสมยิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="f0601-123">If your workbook has a Power Pivot data model, you can do even more optimizations.</span></span> <span data-ttu-id="f0601-124">อ่านเพิ่มเติมเกี่ยวกับ[Demystifying Power BI Q&A ส่วนที่ 2](https://powerbi.microsoft.com/blog/demystifying-power-bi-q-amp-a-part-2/)จากทีมของผู้เชี่ยวชาญภาษาธรรมชาติภายในองค์กรของเรา</span><span class="sxs-lookup"><span data-stu-id="f0601-124">Read more about [Demystifying Power BI Q&A part 2](https://powerbi.microsoft.com/blog/demystifying-power-bi-q-amp-a-part-2/) from our in-house team of natural language experts.</span></span>

* <span data-ttu-id="f0601-125">เปิดชุดข้อมูลใน Power BI Desktop และสร้างคอลัมน์ใหม่ สร้างหน่วยวัดเขตข้อมูลที่เชื่อมโยงเพื่อสร้างค่าที่ไม่ซ้ำแล้วจัดประเภทข้อมูลตามประเภท (เช่น วันที่ สตริง ภูมิศาสตร์ ภาพ URL) และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f0601-125">Open the dataset in Power BI Desktop and create new columns, create measures, concatenate fields to create unique values, classify data by type (e.g., dates, strings, geography, images, URLs), and more.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f0601-126">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="f0601-126">Next steps</span></span>

- [<span data-ttu-id="f0601-127">การถามตอบสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f0601-127">Q&A for consumers</span></span>](../consumer/end-user-q-and-a.md)  
- [<span data-ttu-id="f0601-128">ใช้การถามตอบในแดชบอร์ดและรายงาน</span><span class="sxs-lookup"><span data-stu-id="f0601-128">Use Q&A in dashboards and reports</span></span>](power-bi-tutorial-q-and-a.md)
- [<span data-ttu-id="f0601-129">เตรียมพร้อมชุดข้อมูลภายในองค์กรสำหรับ Q&A</span><span class="sxs-lookup"><span data-stu-id="f0601-129">Prepare on-premises datasets for Q&A</span></span>](service-q-and-a-direct-query.md)   
- [<span data-ttu-id="f0601-130">รับข้อมูล(Power BI)</span><span class="sxs-lookup"><span data-stu-id="f0601-130">Get data (for Power BI)</span></span>](../connect-data/service-get-data.md)  

<span data-ttu-id="f0601-131">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f0601-131">More questions?</span></span> [<span data-ttu-id="f0601-132">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="f0601-132">Try the Power BI Community</span></span>](https://community.powerbi.com/)
