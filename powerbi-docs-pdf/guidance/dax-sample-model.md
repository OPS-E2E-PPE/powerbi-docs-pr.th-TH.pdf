---
title: แบบจำลองตัวอย่าง DAX
description: แบบจำลองตัวอย่าง DAX เพื่อสนับสนุนบทความอ้างอิง
author: peter-myers
ms.author: v-pemyer
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 06/25/2020
ms.openlocfilehash: b2930003da1593ef5d5888c611af6700e00d3d07
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96394071"
---
# <a name="dax-sample-model"></a><span data-ttu-id="d46a2-103">แบบจำลองตัวอย่าง DAX</span><span class="sxs-lookup"><span data-stu-id="d46a2-103">DAX sample model</span></span>

<span data-ttu-id="d46a2-104">แบบจำลองตัวอย่าง **Adventure Works DW 2020** Power BI Desktop ถูกออกแบบมาเพื่อรองรับการเรียนรู้ DAX ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d46a2-104">The **Adventure Works DW 2020** Power BI Desktop sample model is designed to support your DAX learning.</span></span> <span data-ttu-id="d46a2-105">แบบจำลองนี้ใช้ [ตัวอย่างคลังข้อมูล  Adventure Works](/sql/samples/adventureworks-install-configure#data-warehouse-downloads) สำหรับ AdventureWorksDW2017— อย่างไรก็ตามข้อมูลได้ถูกแก้ไขเพื่อให้เหมาะกับวัตถุประสงค์ของแบบจำลองตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="d46a2-105">The model is based on the [Adventure Works data warehouse sample](/sql/samples/adventureworks-install-configure#data-warehouse-downloads) for AdventureWorksDW2017—however, the data has been modified to suit the objectives of the sample model.</span></span>

## <a name="scenario"></a><span data-ttu-id="d46a2-106">สถานการณ์สมมติ</span><span class="sxs-lookup"><span data-stu-id="d46a2-106">Scenario</span></span>

:::image type="content" source="media/dax-sample-model/adventure-works-logo-150x150.png" alt-text="รูปภาพของโลโก้บริษัท Adventure Works จะแสดงขึ้น":::

<span data-ttu-id="d46a2-108">บริษัท Adventure Works เป็นตัวแทนผู้ผลิตจักรยานที่จำหน่ายจักรยานและอุปกรณ์เสริมไปยังตลาดทั่วโลก</span><span class="sxs-lookup"><span data-stu-id="d46a2-108">The Adventure Works company represents a bicycle manufacturer that sells bicycles and accessories to global markets.</span></span> <span data-ttu-id="d46a2-109">บริษัทมีข้อมูลคลังข้อมูลของพวกเขาที่จัดเก็บไว้ในฐานข้อมูล Azure SQL</span><span class="sxs-lookup"><span data-stu-id="d46a2-109">The company has their data warehouse data stored in an Azure SQL Database.</span></span>

## <a name="model-structure"></a><span data-ttu-id="d46a2-110">โครงสร้างแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="d46a2-110">Model structure</span></span>

<span data-ttu-id="d46a2-111">แบบจำลองมีเจ็ดตาราง:</span><span class="sxs-lookup"><span data-stu-id="d46a2-111">The model has seven tables:</span></span>

|<span data-ttu-id="d46a2-112">ตาราง</span><span class="sxs-lookup"><span data-stu-id="d46a2-112">Table</span></span>|<span data-ttu-id="d46a2-113">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="d46a2-113">Description</span></span>|
|-----|-------|
|<span data-ttu-id="d46a2-114">**ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="d46a2-114">**Customer**</span></span>|<span data-ttu-id="d46a2-115">อธิบายลูกค้าและตำแหน่งที่ตั้งทางภูมิศาสตร์ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="d46a2-115">Describes customers and their geographic location.</span></span> <span data-ttu-id="d46a2-116">ลูกค้าซื้อสินค้าออนไลน์ (ยอดขายอินเทอร์เน็ต)</span><span class="sxs-lookup"><span data-stu-id="d46a2-116">Customers purchase products online (Internet sales).</span></span>|
|<span data-ttu-id="d46a2-117">**วันที่**</span><span class="sxs-lookup"><span data-stu-id="d46a2-117">**Date**</span></span>|<span data-ttu-id="d46a2-118">มีสามความสัมพันธ์ระหว่าง **วันที่** และตาราง **ยอดขาย** สำหรับวันที่สั่งซื้อ วันที่จัดส่ง และวันครบกำหนด</span><span class="sxs-lookup"><span data-stu-id="d46a2-118">There are three relationships between the **Date** and **Sales** tables, for order date, ship date, and due date.</span></span> <span data-ttu-id="d46a2-119">ความสัมพันธ์ของวันที่สั่งซื้อเปิดใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="d46a2-119">The order date relationship is active.</span></span> <span data-ttu-id="d46a2-120">รายงานยอดขายของบริษัทโดยใช้ปีทางบัญชีที่เริ่มต้นในวันที่1เดือนกรกฎาคมของแต่ละปี</span><span class="sxs-lookup"><span data-stu-id="d46a2-120">The company's reports sales using a fiscal year that commences on July 1 of each year.</span></span> <span data-ttu-id="d46a2-121">ตารางถูกทำเครื่องหมายเป็นตารางวันที่โดยใช้คอลัมน์ **วันที่**</span><span class="sxs-lookup"><span data-stu-id="d46a2-121">The table is marked as a date table using the **Date** column.</span></span>|
|<span data-ttu-id="d46a2-122">**ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="d46a2-122">**Product**</span></span>|<span data-ttu-id="d46a2-123">จัดเก็บผลิตภัณฑ์ที่เสร็จสมบูรณ์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d46a2-123">Stores finished products only.</span></span>|
|<span data-ttu-id="d46a2-124">**ผู้จำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="d46a2-124">**Reseller**</span></span>|<span data-ttu-id="d46a2-125">อธิบายผู้จำหน่ายและตำแหน่งที่ตั้งทางภูมิศาสตร์ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="d46a2-125">Describes resellers and their geographic location.</span></span> <span data-ttu-id="d46a2-126">ผู้จำหน่ายในการขายผลิตภัณฑ์ให้กับลูกค้าของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="d46a2-126">Reseller on sell products to their customers.</span></span>|
|<span data-ttu-id="d46a2-127">**การขาย**</span><span class="sxs-lookup"><span data-stu-id="d46a2-127">**Sales**</span></span>|<span data-ttu-id="d46a2-128">จัดเก็บแถวที่หน่วยมาตราชั่งของรายการคำสั่งซื้อการขาย</span><span class="sxs-lookup"><span data-stu-id="d46a2-128">Stores rows at sales order line grain.</span></span> <span data-ttu-id="d46a2-129">ค่าทางการเงินทั้งหมดอยู่ในสกุลเงินดอลลาร์สหรัฐ (USD)</span><span class="sxs-lookup"><span data-stu-id="d46a2-129">All financial values are in US dollars (USD).</span></span> <span data-ttu-id="d46a2-130">วันที่สั่งซื้อแรกเริ่มคือ 1 กรกฎาคม 2017 และวันที่สั่งซื้อล่าสุดคือ 15 มิถุนายน 2020</span><span class="sxs-lookup"><span data-stu-id="d46a2-130">The earliest order date is July 1, 2017, and the latest order date is June 15, 2020.</span></span>|
|<span data-ttu-id="d46a2-131">**คำสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="d46a2-131">**Sales Order**</span></span>|<span data-ttu-id="d46a2-132">อธิบายคำสั่งซื้อและหมายเลขบรรทัดใบสั่งและช่องการขายอีกซึ่งเป็น **ผู้จำหน่าย** หรือ **อินเทอร์เน็ต**</span><span class="sxs-lookup"><span data-stu-id="d46a2-132">Describes sales order and order line numbers, and also the sales channel, which is either **Reseller** or **Internet**.</span></span> <span data-ttu-id="d46a2-133">ตารางนี้มีความสัมพันธ์แบบหนึ่งต่อหนึ่งกับตาราง **ยอดขาย**</span><span class="sxs-lookup"><span data-stu-id="d46a2-133">This table has a one-to-one relationship with the **Sales** table.</span></span>|
|<span data-ttu-id="d46a2-134">**อาณาเขตการขาย**</span><span class="sxs-lookup"><span data-stu-id="d46a2-134">**Sales Territory**</span></span>|<span data-ttu-id="d46a2-135">อาณาเขตการขายจะถูกจัดระเบียบเป็นกลุ่ม (อเมริกาเหนือ ยุโรป และแปซิฟิก) ประเทศ และภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="d46a2-135">Sales territories are organized into groups (North America, Europe, and Pacific), countries, and regions.</span></span> <span data-ttu-id="d46a2-136">เฉพาะประเทศสหรัฐอเมริกาจำหน่ายผลิตภัณฑ์ในระดับภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="d46a2-136">Only the United States sells products at the region level.</span></span>|

<span data-ttu-id="d46a2-137">แบบจำลองไม่มีการคำนวณ DAX ใดๆ</span><span class="sxs-lookup"><span data-stu-id="d46a2-137">The model doesn't contain any DAX calculations.</span></span>

## <a name="download-sample"></a><span data-ttu-id="d46a2-138">ดาวน์โหลดตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="d46a2-138">Download sample</span></span>

<span data-ttu-id="d46a2-139">คุณสามารถดาวน์โหลดไฟล์แบบจำลองตัวอย่าง Power BI Desktop [ที่นี่](https://aka.ms/dax-docs-sample-file)</span><span class="sxs-lookup"><span data-stu-id="d46a2-139">You can download the Power BI Desktop sample model file [here](https://aka.ms/dax-docs-sample-file).</span></span>

## <a name="next-steps"></a><span data-ttu-id="d46a2-140">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d46a2-140">Next steps</span></span>

<span data-ttu-id="d46a2-141">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d46a2-141">For more information about this article, check out the following resources:</span></span>

- [<span data-ttu-id="d46a2-142">ข้อมูลอ้างอิงเกี่ยวกับ Data Analysis Expressions (DAX)</span><span class="sxs-lookup"><span data-stu-id="d46a2-142">Data Analysis Expressions (DAX) Reference</span></span>](/dax/)
- <span data-ttu-id="d46a2-143">เส้นทางการเรียนรู้: [ใช้ DAX ใน Power BI Desktop](/learn/paths/dax-power-bi/)</span><span class="sxs-lookup"><span data-stu-id="d46a2-143">Learning path: [Use DAX in Power BI Desktop](/learn/paths/dax-power-bi/)</span></span>
- <span data-ttu-id="d46a2-144">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d46a2-144">Questions?</span></span> [<span data-ttu-id="d46a2-145">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="d46a2-145">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="d46a2-146">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="d46a2-146">Suggestions?</span></span> [<span data-ttu-id="d46a2-147">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="d46a2-147">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com)