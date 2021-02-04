---
title: ใช้พารามิเตอร์การเรียงในรายงานที่มีเลขหน้า
description: คำแนะนำสำหรับรายงานที่มีเลขหน้าที่ออกแบบโดยการใช้พารามิเตอร์การเรียง
author: peter-myers
ms.author: v-pemyer
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 01/14/2020
ms.openlocfilehash: fca5d6556c296094e4536ecf965388e2a4224ed9
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96417922"
---
# <a name="use-cascading-parameters-in-paginated-reports"></a><span data-ttu-id="a0d73-103">ใช้พารามิเตอร์การเรียงในรายงานที่มีเลขหน้า</span><span class="sxs-lookup"><span data-stu-id="a0d73-103">Use cascading parameters in paginated reports</span></span>

<span data-ttu-id="a0d73-104">บทความนี้มุ่งไปที่คุณเช่นเดียวกับผู้เขียนรายงานที่ออกแบบ Power BI [รายงานที่มีเลขหน้า](../paginated-reports/paginated-reports-report-builder-power-bi.md).</span><span class="sxs-lookup"><span data-stu-id="a0d73-104">This article targets you as a report author designing Power BI [paginated reports](../paginated-reports/paginated-reports-report-builder-power-bi.md).</span></span> <span data-ttu-id="a0d73-105">มันมีเหตุการณ์สำหรับพารามิเตอร์การเรียงที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="a0d73-105">It provides scenarios for designing cascading parameters.</span></span> <span data-ttu-id="a0d73-106">พารามิเตอร์การเรียงคือพารามิเตอร์รายงานด้วยความเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="a0d73-106">Cascading parameters are report parameters with dependencies.</span></span> <span data-ttu-id="a0d73-107">เมื่อผู้ใช้การรายงานเลือกค่าพารามิเตอร์ (หรือค่า) มันถูกใช้เพื่อตั้งค่าที่มีอยู่สำหรับพารามิเตอร์อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="a0d73-107">When a report user selects a parameter value (or values), it's used to set available values for another parameter.</span></span>

> [!NOTE]
> <span data-ttu-id="a0d73-108">บทนำสู่พารามิเตอร์การเรียงและวิธีปรับ ไม่ได้ครอบคลุมในบทความนี้</span><span class="sxs-lookup"><span data-stu-id="a0d73-108">An introduction to cascading parameters, and how to configure them, isn't covered in this article.</span></span> <span data-ttu-id="a0d73-109">หากคุณไม่ได้คุ้นเคยทั้งหมดกับพารามิเตอร์การเรียง เราแนะนำให้คุณอ่าน [เพิ่มพารามิเตอร์การเรียงไปยังรายงาน (Report Builder และ SSRS)](/sql/reporting-services/report-design/add-cascading-parameters-to-a-report-report-builder-and-ssrs)</span><span class="sxs-lookup"><span data-stu-id="a0d73-109">If you're not completely familiar with cascading parameters, we recommend you first read [Add Cascading Parameters to a Report (Report Builder and SSRS)](/sql/reporting-services/report-design/add-cascading-parameters-to-a-report-report-builder-and-ssrs).</span></span>

## <a name="design-scenarios"></a><span data-ttu-id="a0d73-110">เหตุการณ์การออกแบบ</span><span class="sxs-lookup"><span data-stu-id="a0d73-110">Design scenarios</span></span>

<span data-ttu-id="a0d73-111">มีเหตุการณ์ออกแบบสองเหตุการณ์สำหรับการใช้พารามิเตอร์การเรียง</span><span class="sxs-lookup"><span data-stu-id="a0d73-111">There are two design scenarios for using cascading parameters.</span></span> <span data-ttu-id="a0d73-112">สิ่งเหล่านั้นสามารถมีประสิทธิผลใที่ช้กับ:</span><span class="sxs-lookup"><span data-stu-id="a0d73-112">They can be effectively used to:</span></span>

- <span data-ttu-id="a0d73-113">ตัวกรอง _กลุ่มใหญ่_ ของรายการ</span><span class="sxs-lookup"><span data-stu-id="a0d73-113">Filter _large sets_ of items</span></span>
- <span data-ttu-id="a0d73-114">รายการ _ที่สำคัญ_ ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="a0d73-114">Present _relevant_ items</span></span>

### <a name="example-database"></a><span data-ttu-id="a0d73-115">ฐานข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a0d73-115">Example database</span></span>

<span data-ttu-id="a0d73-116">ตัวอย่างที่ได้แสดงในบทความนี้อยู่บนฐานของฐานข้อมูล Azure SQL</span><span class="sxs-lookup"><span data-stu-id="a0d73-116">The examples presented in this article are based on an Azure SQL Database.</span></span> <span data-ttu-id="a0d73-117">การดำเนินการขายการบันทึกฐานข้อมูลและประกอบด้วยตารางที่หลากหลายที่จัดเก็บตัวแทนจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="a0d73-117">The database records sales operations, and contains various tables storing resellers, products, and sales orders.</span></span>

<span data-ttu-id="a0d73-118">ตารางมีชื่อ **ตัวแทนจำหน่าย** ที่จัดเก็บหนึ่งบันทึกของแต่ละตัวแทนจำหน่าย และยังประกอบด้วยบันทึกอีกหลายพัน</span><span class="sxs-lookup"><span data-stu-id="a0d73-118">A table named **Reseller** stores one record for each reseller, and it contains many thousands of records.</span></span> <span data-ttu-id="a0d73-119">ตาราง **ตัวแทนจำนห่าย** มีแถวเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="a0d73-119">The **Reseller** table has these columns:</span></span>

- <span data-ttu-id="a0d73-120">โค้ดตัวแทนจำหน่าย (จำนวนเต็ม)</span><span class="sxs-lookup"><span data-stu-id="a0d73-120">ResellerCode (integer)</span></span>
- <span data-ttu-id="a0d73-121">ชื่อตัวแทนจำนห่าย</span><span class="sxs-lookup"><span data-stu-id="a0d73-121">ResellerName</span></span>
- <span data-ttu-id="a0d73-122">ประเทศ-ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="a0d73-122">Country-Region</span></span>
- <span data-ttu-id="a0d73-123">รัฐ-จังหวัด</span><span class="sxs-lookup"><span data-stu-id="a0d73-123">State-Province</span></span>
- <span data-ttu-id="a0d73-124">เมือง</span><span class="sxs-lookup"><span data-stu-id="a0d73-124">City</span></span>
- <span data-ttu-id="a0d73-125">รหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="a0d73-125">PostalCode</span></span>

<span data-ttu-id="a0d73-126">มีชื่อตาราง **การขาย** ด้วย</span><span class="sxs-lookup"><span data-stu-id="a0d73-126">There's a table named **Sales**, too.</span></span> <span data-ttu-id="a0d73-127">มีการจัดเก็บบันทึกการสั่งการขายและมีความสัมพันธ์หลักของต่างชาติไปยัง ตาราง **ตัวแทนจำหน่าย** ในแถว **โค้ดตัวแทนจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="a0d73-127">It stores sales order records, and has a foreign key relationship to the **Reseller** table, on the **ResellerCode** column.</span></span>

### <a name="example-requirement"></a><span data-ttu-id="a0d73-128">ตัวอย่างข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="a0d73-128">Example requirement</span></span>

<span data-ttu-id="a0d73-129">มีข้อกำหนดเพื่อปรับปรุงรายงานประวัติตัวแทนจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="a0d73-129">There's a requirement to develop a Reseller Profile report.</span></span> <span data-ttu-id="a0d73-130">รายงานต้องถูกออกแบบเพื่อแสดงข้อมูลสำหรับตัวแทนจำหน่ายผู้เดียว</span><span class="sxs-lookup"><span data-stu-id="a0d73-130">The report must be designed to display information for a single reseller.</span></span> <span data-ttu-id="a0d73-131">มันไม่เหมาะสมที่จะมีผู้ใช้การรายงานเข้าสู่โค้ดตัวแทนจำหน่าย เช่นเดียวกับที่นานๆ ครั้งจะบันทึก</span><span class="sxs-lookup"><span data-stu-id="a0d73-131">It's not appropriate to have the report user enter a reseller code, as they rarely memorize them.</span></span>

## <a name="filter-large-sets-of-items"></a><span data-ttu-id="a0d73-132">ตัวกรองกลุ่มใหญ่ของรายการ</span><span class="sxs-lookup"><span data-stu-id="a0d73-132">Filter large sets of items</span></span>

<span data-ttu-id="a0d73-133">มาดูสามตัวอย่างเพื่อช่วยคุณจำกัดกลุ่มใหญ่ของรายการที่มีอยู่ เช่นตัวแทนจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="a0d73-133">Let's take a look at three examples to help you limit large sets of available items, like resellers.</span></span> <span data-ttu-id="a0d73-134">คือ:</span><span class="sxs-lookup"><span data-stu-id="a0d73-134">They are:</span></span>

- [<span data-ttu-id="a0d73-135">ตัวกรองโดยแถวที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="a0d73-135">Filter by related columns</span></span>](#filter-by-related-columns)
- [<span data-ttu-id="a0d73-136">ตัวกรองโดยแถวที่จัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="a0d73-136">Filter by a grouping column</span></span>](#filter-by-a-grouping-column)
- [<span data-ttu-id="a0d73-137">ตัวกรองโดยรูปแบบการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a0d73-137">Filter by search pattern</span></span>](#filter-by-search-pattern)

### <a name="filter-by-related-columns"></a><span data-ttu-id="a0d73-138">ตัวกรองโดยแถวที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="a0d73-138">Filter by related columns</span></span>

<span data-ttu-id="a0d73-139">ในตัวอย่างนี้ ผู้ใช้การรายงานโต้ตอบกับห้าพารามิเตอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="a0d73-139">In this example, the report user interacts with five report parameters.</span></span> <span data-ttu-id="a0d73-140">ต้องเลือกประเทศ-ภูมิภาค รัฐ-จังหวัด เมือง และรหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="a0d73-140">They must select country-region, state-province, city, and then postal code.</span></span> <span data-ttu-id="a0d73-141">พรารามิเตอร์สุดท้ายที่รายการตัวแทนจำหน่ายที่มีอยู่ในตำแหน่งตามภูมิศาสตร์</span><span class="sxs-lookup"><span data-stu-id="a0d73-141">A final parameter then lists resellers that reside in that geographic location.</span></span>

![ภาพหน้าจอของพารามิเตอร์รายงานแบบแบ่งหน้าของ Power BI ที่แสดงตัวกรองตามคอลัมน์ที่เกี่ยวข้อง](media/paginated-report-cascading-parameter/filter-by-related-columns-example.png)

<span data-ttu-id="a0d73-143">นี่คือวิธีที่คุณสามารถปรับปรุงพารามิเตอร์การเรียง:</span><span class="sxs-lookup"><span data-stu-id="a0d73-143">Here's how you can develop the cascading parameters:</span></span>

1. <span data-ttu-id="a0d73-144">สร้างห้าพารามิเตอร์รายงาน ที่ถูกสั่งในลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a0d73-144">Create the five report parameters, ordered in the correct sequence.</span></span>
2. <span data-ttu-id="a0d73-145">สร้างกลุ่มข้อมูล **ประเทศภูมิภาค** ที่รับข้อมูลมาจากค่าประเทศ-ภูมิภาคที่แตกต่าง โดยการใช้คำสั่งคำถามดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a0d73-145">Create the **CountryRegion** dataset that retrieves distinct country-region values, using the following query statement:</span></span>

    ```sql
    SELECT DISTINCT
      [Country-Region]
    FROM
      [Reseller]
    ORDER BY
      [Country-Region]
    ```

3. <span data-ttu-id="a0d73-146">สร้างกลุ่มข้อมูล **รัฐจังหวัด** ที่รับข้อมูลมาจากค่ารัฐ-จังหวัดที่แตกต่างกันสำหรับประเทศ-ภูมิภาคที่เลือก โดยการใช้คำสั่งคำถามดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a0d73-146">Create the **StateProvince** dataset that retrieves distinct state-province values for the selected country-region, using the following query statement:</span></span>

    ```sql
    SELECT DISTINCT
      [State-Province]
    FROM
      [Reseller]
    WHERE
      [Country-Region] = @CountryRegion
    ORDER BY
      [State-Province]
    ```

4. <span data-ttu-id="a0d73-147">สร้างกลุ่มข้อมูล **เมือง** ที่รับข้อมูลมาจากค่าเมืองสำหรับประเทศ-ภูมิภาคและรัฐ-จังหวัดที่เลือก โดยการใช้คำสั่งคำถามดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a0d73-147">Create the **City** dataset that retrieves distinct city values for the selected country-region and state-province, using the following query statement:</span></span>

    ```sql
    SELECT DISTINCT
      [City]
    FROM
      [Reseller]
    WHERE
      [Country-Region] = @CountryRegion
      AND [State-Province] = @StateProvince
    ORDER BY
      [City]
    ```

5. <span data-ttu-id="a0d73-148">ดำเนินการรูปแบบนี้ต่อเพื่อสร้างกลุ่มข้อมูล **รหัสไปรษณีย์**</span><span class="sxs-lookup"><span data-stu-id="a0d73-148">Continue this pattern to create the **PostalCode** dataset.</span></span>
6. <span data-ttu-id="a0d73-149">สร้างกลุ่มข้อมูล **ตัวแทนจำหน่าย** ที่รับข้อมูลมาจากตัวแทนจำหน่ายทั้งหมดสำหรับค่าตามภูมิศาสตร์ที่เลือก โดยการใช้คำสั่งคำถามดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a0d73-149">Create the **Reseller** dataset to retrieve all resellers for the selected geographic values, using the following query statement:</span></span>

    ```sql
    SELECT
      [ResellerCode],
      [ResellerName]
    FROM
      [Reseller]
    WHERE
      [Country-Region] = @CountryRegion
      AND [State-Province] = @StateProvince
      AND [City] = @City
      AND [PostalCode] = @PostalCode
    ORDER BY
      [ResellerName]
    ```

7. <span data-ttu-id="a0d73-150">สำหรับแต่ละกลุ่มข้อมูลยกเว้นอันแรก แมปพารามิเตอร์คำถามไปยังพารามิเตอร์รายงานที่เหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="a0d73-150">For each dataset except the first, map the query parameters to the corresponding report parameters.</span></span>

> [!NOTE]
> <span data-ttu-id="a0d73-151">ทุกพารามิเตอร์คำถาม (ใส่คำนำหน้าด้วยสัญลักษณ์ @) ที่แสดงในตัวอย่างเหล่านี้ที่สามารถฝังตัวเข้ากับคำสั่ง เลือก หรือถูกส่งผ่านเข้าไปขั้นตอนการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="a0d73-151">All query parameters (prefixed with the @ symbol) shown in these examples could be embedded within SELECT statements, or passed to stored procedures.</span></span>
>
> <span data-ttu-id="a0d73-152">โดยทั่วไปขั้นตอนการจัดเก็บคือการเข้าสู่การออกแบบที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="a0d73-152">Generally, stored procedures are a better design approach.</span></span> <span data-ttu-id="a0d73-153">เพราะว่าแผนคำถามนั้นถูกแคชสำหรับการกระทำการแบบรวดเร็ว และยังอนุญาตให้คุณปรับปรุงตรรกะที่ซับซ้อนได้มากกว่าเมื่อต้องการ</span><span class="sxs-lookup"><span data-stu-id="a0d73-153">It's because their query plans are cached for quicker execution, and they allow you develop more sophisticated logic, when needed.</span></span> <span data-ttu-id="a0d73-154">อย่างไรก็ตามก็ไม่สามารถสนับสนุนได้ตอนนี้สำหรับแหล่งข้อมูลเกตเวย์ที่สัมพันธ์กัน ซึ่งหมายความว่า SQL Server Oracle และ Teradata</span><span class="sxs-lookup"><span data-stu-id="a0d73-154">However, they aren't currently supported for gateway relational data sources, which means SQL Server, Oracle, and Teradata.</span></span>
>
> <span data-ttu-id="a0d73-155">สุดท้ายแล้ว คุณควรแน่ใจว่าดัชนีที่เหมาะสมปรากฏในการสนับสนุนการกู้คืนข้อมูลที่มีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="a0d73-155">Lastly, you should always ensure suitable indexes exist to support efficient data retrieval.</span></span> <span data-ttu-id="a0d73-156">มิฉะนั้น พารามิเตอร์รายงานของคุณสามารถอาศัยอยู่อย่างช้าๆ และฐานข้อมูลจะเป็นภาระหนักเกินไป</span><span class="sxs-lookup"><span data-stu-id="a0d73-156">Otherwise, your report parameters could be slow to populate, and the database could become overburdened.</span></span> <span data-ttu-id="a0d73-157">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับดัชนีเซิร์ฟเวอร์ SQL ดู [คำแนะนำระบบโครงสร้างดัชนีเซิร์ฟเวอร์ SQL และการออกแบบ ](/sql/relational-databases/sql-server-index-design-guide)</span><span class="sxs-lookup"><span data-stu-id="a0d73-157">For more information about SQL Server indexing, see [SQL Server Index Architecture and Design Guide](/sql/relational-databases/sql-server-index-design-guide).</span></span>

### <a name="filter-by-a-grouping-column"></a><span data-ttu-id="a0d73-158">ตัวกรองโดยแถวที่จัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="a0d73-158">Filter by a grouping column</span></span>

<span data-ttu-id="a0d73-159">ในตัวอย่างนี้ ผู้ใช้การรายงานโต้ตอบกับพารามิเตอร์รายงานเพื่อเลือกตัวอักษรตัวแรกไปยังตัวแทนจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="a0d73-159">In this example, the report user interacts with a report parameter to select the first letter of the reseller.</span></span> <span data-ttu-id="a0d73-160">พารามิเตอร์ตัวที่สองได้แสดงรายการตัวแทนจำหน่ายเมื่อชื่อเริ่มต้นด้วยอักษรที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a0d73-160">A second parameter then lists resellers when the name commences with the selected letter.</span></span>

![ภาพหน้าจอของพารามิเตอร์รายงานแบบแบ่งหน้าของ Power BI ที่แสดงตัวกรองตามคอลัมน์การจัดกลุ่ม](media/paginated-report-cascading-parameter/filter-by-grouping-column-example.png)

<span data-ttu-id="a0d73-162">นี่คือวิธีที่คุณสามารถปรับปรุงพารามิเตอร์การเรียง:</span><span class="sxs-lookup"><span data-stu-id="a0d73-162">Here's how you can develop the cascading parameters:</span></span>

1. <span data-ttu-id="a0d73-163">สร้าง **กลุ่มรายงาน** และ **ตัวแทนจำหน่าย** ของพารามิเตอร์รายงานตามลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a0d73-163">Create the **ReportGroup** and **Reseller** report parameters, ordered in the correct sequence.</span></span>
2. <span data-ttu-id="a0d73-164">สร้างชุดข้อมูล **กลุ่มรายงาน** เพื่อดึงตัวอักษรแรกที่ใช้โดยผู้ตัวแทนจำหน่ายทั้งหมดโดยใช้คำสั่งแบบสอบถามต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a0d73-164">Create the **ReportGroup** dataset to retrieve the first letters used by all resellers, using the following query statement:</span></span>

    ```sql
    SELECT DISTINCT
      LEFT([ResellerName], 1) AS [ReportGroup]
    FROM
      [Reseller]
    ORDER BY
      [ReportGroup]
    ```

3. <span data-ttu-id="a0d73-165">สร้างกลุ่มข้อมูล **ตัวแทนจำหน่าย** ที่รับข้อมูลมาจากตัวแทนจำหน่ายทั้งหมดที่เริ่มด้วยตัวอักษรที่เลือก โดยการใช้คำสั่งคำถามดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a0d73-165">Create the **Reseller** dataset to retrieve all resellers that commence with the selected letter, using the following query statement:</span></span>

    ```sql
    SELECT
      [ResellerCode],
      [ResellerName]
    FROM
      [Reseller]
    WHERE
      LEFT([ResellerName], 1) = @ReportGroup
    ORDER BY
      [ResellerName]
    ```

4. <span data-ttu-id="a0d73-166">แมปพารามิเตอร์คำถามของชุดข้อมูล **ตัวแทนจำหน่าย** ไปยังพารามิเตอร์รายงานที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="a0d73-166">Map the query parameter of the **Reseller** dataset to the corresponding report parameter.</span></span>

<span data-ttu-id="a0d73-167">มีประสิทธิภาพมากขึ้นเมื่อเพิ่มแถวที่จัดกลุ่มไปยังตาราง **ตัวแทนจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="a0d73-167">It's more efficient to add the grouping column to the **Reseller** table.</span></span> <span data-ttu-id="a0d73-168">เมื่อยังคงมีอยู่และทำดัชนีจะมอบผลลัพธ์ที่ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="a0d73-168">When persisted and indexed, it delivers the best result.</span></span> <span data-ttu-id="a0d73-169">สำหรับข้อมูลเพิ่มเติม ดู[ระบุแถวที่ได้รับการคำนวณในตาราง](/sql/relational-databases/tables/specify-computed-columns-in-a-table)</span><span class="sxs-lookup"><span data-stu-id="a0d73-169">For more information, see [Specify Computed Columns in a Table](/sql/relational-databases/tables/specify-computed-columns-in-a-table).</span></span>

```sql
ALTER TABLE [Reseller]
ADD [ReportGroup] AS LEFT([ResellerName], 1) PERSISTED
```

<span data-ttu-id="a0d73-170">เทคนิคนี้สามารถส่งมอบศักยภาพได้มากยิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="a0d73-170">This technique can deliver even greater potential.</span></span> <span data-ttu-id="a0d73-171">พิจารณาสคริปต์ต่อไปนี้ที่เพิ่มคอลัมน์ที่จัดกลุ่มใหม่เพื่อกรองตัวแทนจำหน่ายโดย _ตัวอักษรที่กำหนดแถบไว้ล่วงหน้า_</span><span class="sxs-lookup"><span data-stu-id="a0d73-171">Consider the following script that adds a new grouping column to filter resellers by _pre-defined bands of letters_.</span></span> <span data-ttu-id="a0d73-172">นอกจากนี้ยังสร้างดัชนีเพื่อดึงข้อมูลที่จำเป็นโดยพารามิเตอร์รายงานอย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="a0d73-172">It also creates an index to efficiently retrieve the data required by the report parameters.</span></span>

```sql
ALTER TABLE [Reseller]
ADD [ReportGroup2] AS CASE
  WHEN [ResellerName] LIKE '[A-C]%' THEN 'A-C'
  WHEN [ResellerName] LIKE '[D-H]%' THEN 'D-H'
  WHEN [ResellerName] LIKE '[I-M]%' THEN 'I-M'
  WHEN [ResellerName] LIKE '[N-S]%' THEN 'N-S'
  WHEN [ResellerName] LIKE '[T-Z]%' THEN 'T-Z'
  ELSE '[Other]'
END PERSISTED
GO

CREATE NONCLUSTERED INDEX [Reseller_ReportGroup2]
ON [Reseller] ([ReportGroup2]) INCLUDE ([ResellerCode], [ResellerName])
GO
```

### <a name="filter-by-search-pattern"></a><span data-ttu-id="a0d73-173">ตัวกรองโดยรูปแบบการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a0d73-173">Filter by search pattern</span></span>

<span data-ttu-id="a0d73-174">ในตัวอย่างนี้ ผู้ใช้การรายงานโต้ตอบกับพารามิเตอร์รายงานเพื่อใส่การเลือกรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="a0d73-174">In this example, the report user interacts with a report parameter to enter a search pattern.</span></span> <span data-ttu-id="a0d73-175">พารามิเตอร์ตัวที่สองได้แสดงรายการตัวแทนจำหน่ายเมื่อชื่อประกอบด้วยรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="a0d73-175">A second parameter then lists resellers when the name contains the pattern.</span></span>

![ภาพหน้าจอของพารามิเตอร์รายงานแบบแบ่งหน้าของ Power BI ที่แสดงตัวกรองตามรูปแบบการค้นหา](media/paginated-report-cascading-parameter/filter-by-search-pattern-example.png)

<span data-ttu-id="a0d73-177">นี่คือวิธีที่คุณสามารถปรับปรุงพารามิเตอร์การเรียง:</span><span class="sxs-lookup"><span data-stu-id="a0d73-177">Here's how you can develop the cascading parameters:</span></span>

1. <span data-ttu-id="a0d73-178">สร้าง **การค้นหา** และ **ตัวแทนจำหน่าย** ของพารามิเตอร์รายงานตามลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a0d73-178">Create the **Search** and **Reseller** report parameters, ordered in the correct sequence.</span></span>
2. <span data-ttu-id="a0d73-179">สร้างกลุ่มข้อมูล **ตัวแทนจำหน่าย** ที่รับข้อมูลมาจากตัวแทนจำหน่ายทั้งหมดที่ประกอบด้วยข้อความค้นหา โดยการใช้คำสั่งคำถามดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a0d73-179">Create the **Reseller** dataset to retrieve all resellers that contain the search text, using the following query statement:</span></span>

    ```sql
    SELECT
      [ResellerCode],
      [ResellerName]
    FROM
      [Reseller]
    WHERE
      [ResellerName] LIKE '%' + @Search + '%'
    ORDER BY
      [ResellerName]
    ```

3. <span data-ttu-id="a0d73-180">แมปพารามิเตอร์คำถามของชุดข้อมูล **ตัวแทนจำหน่าย** ไปยังพารามิเตอร์รายงานที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="a0d73-180">Map the query parameter of the **Reseller** dataset to the corresponding report parameter.</span></span>

> [!TIP]
> <span data-ttu-id="a0d73-181">คุณสามารถปรับปรุงการออกแบบนี้เพื่อให้สามารถควบคุมผู้ใช้รายงานของคุณได้มากขึ้น</span><span class="sxs-lookup"><span data-stu-id="a0d73-181">You can improve upon this design to provide more control for your report users.</span></span> <span data-ttu-id="a0d73-182">ซึ่งช่วยให้พวกเขาสามารถกำหนดค่าการจับคู่รูปแบบของตนเอง</span><span class="sxs-lookup"><span data-stu-id="a0d73-182">It lets them define their own pattern matching value.</span></span> <span data-ttu-id="a0d73-183">สำหรับตัวอย่าง เช่น ค่าการค้นหา "สีแดง%" จะกรองให้กับตัวแทนจำหน่ายที่มีชื่อที่ _เริ่มต้น_ กับอักขระ "สีแดง"</span><span class="sxs-lookup"><span data-stu-id="a0d73-183">For example, the search value "red%" will filter to resellers with names that _commence_ with the characters "red".</span></span>
>
> <span data-ttu-id="a0d73-184">สำหรับข้อมูลเพิ่มเติม ดู [ถูกใจ (ทำการค้า-SQL)](/sql/t-sql/language-elements/like-transact-sql#using-the--wildcard-character)</span><span class="sxs-lookup"><span data-stu-id="a0d73-184">For more information, see [LIKE (Transact-SQL)](/sql/t-sql/language-elements/like-transact-sql#using-the--wildcard-character).</span></span>

<span data-ttu-id="a0d73-185">นี่คือวิธีที่คุณสามารถให้ผู้ใช้รายงานกำหนดรูปแบบของตนเอง</span><span class="sxs-lookup"><span data-stu-id="a0d73-185">Here's how you can let the report users define their own pattern.</span></span>

```sql
WHERE
  [ResellerName] LIKE @Search
```

<span data-ttu-id="a0d73-186">อย่างไรก็ตามสำหรับผู้เชี่ยวชาญที่ไม่ใช่ฐานข้อมูลจำนวนมากนั้น ก็ไม่ทราบเกี่ยวกับเปอร์เซ็นต์ของ (%) อักขระตัวแทน</span><span class="sxs-lookup"><span data-stu-id="a0d73-186">Many non-database professionals, however, don't know about the percentage (%) wildcard character.</span></span> <span data-ttu-id="a0d73-187">แต่พวกเขาจะคุ้นเคยกับอักขระเครื่องหมาย (\*)</span><span class="sxs-lookup"><span data-stu-id="a0d73-187">Instead, they're familiar with the asterisk (\*) character.</span></span> <span data-ttu-id="a0d73-188">โดยการปรับเปลี่ยนส่วนคำสั่ง WHERE คุณสามารถอนุญาตให้พวกเขาใช้อักขระนี้ได้</span><span class="sxs-lookup"><span data-stu-id="a0d73-188">By modifying the WHERE clause, you can let them use this character.</span></span>

```sql
WHERE
  [ResellerName] LIKE SUBSTITUTE(@Search, '%', '*')
```

## <a name="present-relevant-items"></a><span data-ttu-id="a0d73-189">รายการที่สำคัญปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="a0d73-189">Present relevant items</span></span>

<span data-ttu-id="a0d73-190">ในสถานการณ์นี้ คุณสามารถใช้ข้อมูลจริงเพื่อจำกัดค่าที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="a0d73-190">In this scenario, you can use fact data to limit available values.</span></span> <span data-ttu-id="a0d73-191">ผู้ใช้รายงานจะถูกแสดงด้วยรายการที่มีการบันทึกกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="a0d73-191">Report users will be presented with items where activity has been recorded.</span></span>

<span data-ttu-id="a0d73-192">ในตัวอย่างนี้ ผู้ใช้รายงานโต้ตอบกับสามพารามิเตอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="a0d73-192">In this example, the report user interacts with three report parameter.</span></span> <span data-ttu-id="a0d73-193">สองชุดแรกที่ตั้งค่าช่วงวันที่ของวันที่การสั่งการขาย</span><span class="sxs-lookup"><span data-stu-id="a0d73-193">The first two set a date range of sales order dates.</span></span> <span data-ttu-id="a0d73-194">พารามิเตอร์ที่สามแล้วแสดงรายการตัวแทนจำหน่ายที่การสั่งได้ถูกสร้างระหว่างระยะเวลานั้น</span><span class="sxs-lookup"><span data-stu-id="a0d73-194">The third parameter then lists resellers where orders have been created during that time period.</span></span>

![ภาพหน้าจอของพารามิเตอร์รายงานแบบแบ่งหน้าของ Power BI ที่แสดงพารามิเตอร์รายงานสามพารามิเตอร์: เริ่มวันที่คำสั่งซื้อ สิ้นสุดวันที่คำสั่งซื้อและตัวแทนจำหน่าย](media/paginated-report-cascading-parameter/filter-relevant-items-example.png)

<span data-ttu-id="a0d73-196">นี่คือวิธีที่คุณสามารถปรับปรุงพารามิเตอร์การเรียง:</span><span class="sxs-lookup"><span data-stu-id="a0d73-196">Here's how you can develop the cascading parameters:</span></span>

1. <span data-ttu-id="a0d73-197">สร้าง **เริ่มวันที่คำสั่งซื้อ** **สิ้นสุดวันที่คำสั่งซื้อ** และ **ตัวแทนจำหน่าย** ของพารามิเตอร์รายงานตามลำดับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a0d73-197">Create the **OrderDateStart**, **OrderDateEnd**, and **Reseller** report parameters, ordered in the correct sequence.</span></span>
2. <span data-ttu-id="a0d73-198">สร้างกลุ่มข้อมูล **ตัวแทนจำหน่าย** ที่รับข้อมูลมาจากตัวแทนจำหน่ายทั้งหมดที่สร้างการสั่งในระยะเวลาวันที่นั้น โดยการใช้คำสั่งคำถามดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a0d73-198">Create the **Reseller** dataset to retrieve all resellers that created orders in the date period, using the following query statement:</span></span>

    ```sql
    SELECT DISTINCT
      [r].[ResellerCode],
      [r].[ResellerName]
    FROM
      [Reseller] AS [r]
    INNER JOIN [Sales] AS [s]
      ON [s].[ResellerCode] = [r].[ResellerCode]
    WHERE
      [s].[OrderDate] >= @OrderDateStart
      AND [s].[OrderDate] < DATEADD(DAY, 1, @OrderDateEnd)
    ORDER BY
      [r].[ResellerName]
    ```

## <a name="recommendations"></a><span data-ttu-id="a0d73-199">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="a0d73-199">Recommendations</span></span>

<span data-ttu-id="a0d73-200">เราขอแนะนำให้คุณออกแบบรายงานของคุณด้วยพารามิเตอร์การเรียง เมื่อใดก็ตามที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="a0d73-200">We recommend you design your reports with cascading parameters, whenever possible.</span></span> <span data-ttu-id="a0d73-201">เนื่องจากพวกเขา:</span><span class="sxs-lookup"><span data-stu-id="a0d73-201">It's because they:</span></span>

- <span data-ttu-id="a0d73-202">มอบประสบการณ์ที่เกิดขึ้นได้เองและเป็นประโยชน์สำหรับผู้ใช้การรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="a0d73-202">Provide intuitive and helpful experiences for your report users</span></span>
- <span data-ttu-id="a0d73-203">มีประสิทธิภาพเนื่องจากพวกเขาดึงข้อมูลชุดที่มีขนาดเล็กกว่าของค่าที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="a0d73-203">Are efficient, because they retrieve smaller sets of available values</span></span>

<span data-ttu-id="a0d73-204">ตรวจสอบให้แน่ใจว่ามีการปรับให้เหมาะสมกับแหล่งข้อมูลของคุณโดย:</span><span class="sxs-lookup"><span data-stu-id="a0d73-204">Be sure to optimize your data sources by:</span></span>

- <span data-ttu-id="a0d73-205">การใช้ขั้นตอนที่จัดเก็บไว้ เมื่อใดก็ตามที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="a0d73-205">Using stored procedures, whenever possible</span></span>
- <span data-ttu-id="a0d73-206">การเพิ่มดัชนีที่เหมาะสมสำหรับการดึงข้อมูลที่มีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="a0d73-206">Adding appropriate indexes for efficient data retrieval</span></span>
- <span data-ttu-id="a0d73-207">ค่าคอลัมน์ที่ปรากฏจริง—และแม้แต่แถว—เพื่อหลีกเลี่ยงการประเมินเวลาแบบสอบถามที่มีราคาแพง</span><span class="sxs-lookup"><span data-stu-id="a0d73-207">Materializing column values—and even rows—to avoid expensive query-time evaluations</span></span>

## <a name="next-steps"></a><span data-ttu-id="a0d73-208">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a0d73-208">Next steps</span></span>

<span data-ttu-id="a0d73-209">สำหรับข้อมูลเพิ่มเติมที่เกี่ยวข้องกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a0d73-209">For more information related to this article, check out the following resources:</span></span>

- [<span data-ttu-id="a0d73-210">พารามิเตอร์รายงานในตัวสร้างรายงานของ Power BI </span><span class="sxs-lookup"><span data-stu-id="a0d73-210">Report parameters in Power BI Report Builder</span></span>](../paginated-reports/report-builder-parameters.md)
- [<span data-ttu-id="a0d73-211">เพิ่มพารามิเตอร์การเรียงลงในรายงาน (ตัวสร้างรายงานและ SSRS)</span><span class="sxs-lookup"><span data-stu-id="a0d73-211">Add Cascading Parameters to a Report (Report Builder and SSRS)</span></span>](/sql/reporting-services/report-design/add-cascading-parameters-to-a-report-report-builder-and-ssrs)
- <span data-ttu-id="a0d73-212">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a0d73-212">Questions?</span></span> [<span data-ttu-id="a0d73-213">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="a0d73-213">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="a0d73-214">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="a0d73-214">Suggestions?</span></span> [<span data-ttu-id="a0d73-215">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="a0d73-215">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com)
