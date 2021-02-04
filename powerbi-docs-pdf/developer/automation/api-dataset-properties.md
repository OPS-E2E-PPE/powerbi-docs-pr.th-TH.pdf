---
title: คุณสมบัติของชุดข้อมูล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: เรียนรู้เกี่ยวกับคุณสมบัติของชุดข้อมูล Power BI APIs เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: b4bd173c2f3730a0a6082214afbfdf5760048102
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887695"
---
# <a name="dataset-properties"></a><span data-ttu-id="37a05-104">คุณสมบัติของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="37a05-104">Dataset properties</span></span>

<span data-ttu-id="37a05-105">V1 ปัจจุบันของชุดข้อมูล API จะสร้างชุดข้อมูลด้วยชื่อและคอลเลกชันของตารางได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="37a05-105">The current v1 of datasets API only allows for a dataset to be created with a name and a collection of tables.</span></span> <span data-ttu-id="37a05-106">แต่ละตารางสามารถมีชื่อและคอลเลกชันของคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="37a05-106">Each table can have a name and a collection of columns.</span></span> <span data-ttu-id="37a05-107">แต่ละคอลัมน์มีชื่อและชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="37a05-107">Each column has a name and datatype.</span></span> <span data-ttu-id="37a05-108">เราจะขยายคุณสมบัติเหล่านี้ด้วยการสนับสนุนให้มีหน่วยวัดและความสัมพันธ์ระหว่างตาราง</span><span class="sxs-lookup"><span data-stu-id="37a05-108">We are expanding these properties most notably with support for measures and relationships between tables.</span></span> <span data-ttu-id="37a05-109">รายการทั้งหมดของคุณสมบัติที่ได้รับการสนับสนุนสำหรับรุ่นนี้มีดังนี้:</span><span class="sxs-lookup"><span data-stu-id="37a05-109">The complete list of supported properties for this release is as follows:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="37a05-110">สามารถเข้าถึงได้ที่หน้า[กลุ่มการดำเนินการชุดข้อมูล](/rest/api/power-bi/datasets)ได้</span><span class="sxs-lookup"><span data-stu-id="37a05-110">It can be accessed at the [Datasets Operation Groups](/rest/api/power-bi/datasets) page.</span></span>

## <a name="dataset"></a><span data-ttu-id="37a05-111">ชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="37a05-111">Dataset</span></span>

<span data-ttu-id="37a05-112">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="37a05-112">Name</span></span>  |<span data-ttu-id="37a05-113">พิมพ์</span><span class="sxs-lookup"><span data-stu-id="37a05-113">Type</span></span>  |<span data-ttu-id="37a05-114">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="37a05-114">Description</span></span>  |<span data-ttu-id="37a05-115">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="37a05-115">Read Only</span></span>  |<span data-ttu-id="37a05-116">จำเป็น</span><span class="sxs-lookup"><span data-stu-id="37a05-116">Required</span></span>
---------|---------|---------|---------|---------
<span data-ttu-id="37a05-117">id</span><span class="sxs-lookup"><span data-stu-id="37a05-117">id</span></span>     |  <span data-ttu-id="37a05-118">GUID</span><span class="sxs-lookup"><span data-stu-id="37a05-118">Guid</span></span>       | <span data-ttu-id="37a05-119">ตัวระบุชุดข้อมูลทั้งระบบ</span><span class="sxs-lookup"><span data-stu-id="37a05-119">System wide unique identifier for the dataset.</span></span>        | <span data-ttu-id="37a05-120">เป็นจริง</span><span class="sxs-lookup"><span data-stu-id="37a05-120">True</span></span>        | <span data-ttu-id="37a05-121">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-121">False</span></span>        
<span data-ttu-id="37a05-122">name</span><span class="sxs-lookup"><span data-stu-id="37a05-122">name</span></span>     | <span data-ttu-id="37a05-123">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-123">String</span></span>        | <span data-ttu-id="37a05-124">ชุดข้อมูลที่ผู้ใช้กำหนดชื่อเอง</span><span class="sxs-lookup"><span data-stu-id="37a05-124">User defined name of the dataset.</span></span>        | <span data-ttu-id="37a05-125">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-125">False</span></span>        | <span data-ttu-id="37a05-126">เป็นจริง</span><span class="sxs-lookup"><span data-stu-id="37a05-126">True</span></span>        
<span data-ttu-id="37a05-127">ตาราง</span><span class="sxs-lookup"><span data-stu-id="37a05-127">tables</span></span>     | <span data-ttu-id="37a05-128">ตาราง</span><span class="sxs-lookup"><span data-stu-id="37a05-128">Table[]</span></span>        | <span data-ttu-id="37a05-129">คอลเลกชันของตาราง</span><span class="sxs-lookup"><span data-stu-id="37a05-129">Collection of tables.</span></span>        |  <span data-ttu-id="37a05-130">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-130">False</span></span>       | <span data-ttu-id="37a05-131">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-131">False</span></span>        
<span data-ttu-id="37a05-132">ความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="37a05-132">relationships</span></span>     | <span data-ttu-id="37a05-133">ความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="37a05-133">Relationship[]</span></span>        | <span data-ttu-id="37a05-134">คอลเลกชันของความสัมพันธ์ระหว่างตาราง</span><span class="sxs-lookup"><span data-stu-id="37a05-134">Collection of relationships between tables.</span></span>        | <span data-ttu-id="37a05-135">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-135">False</span></span>        |  <span data-ttu-id="37a05-136">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-136">False</span></span>  
<span data-ttu-id="37a05-137">defaultMode</span><span class="sxs-lookup"><span data-stu-id="37a05-137">defaultMode</span></span>     | <span data-ttu-id="37a05-138">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-138">String</span></span>        | <span data-ttu-id="37a05-139">กำหนดว่า ชุดข้อมูลมีการส่งแบบพุช สตรีม หรือทั้งสองอย่าง ด้วยค่าของ "การส่งแบบพุช" "สตรีมมิ่ง"  "Push" และ "Streaming" หรือไม่</span><span class="sxs-lookup"><span data-stu-id="37a05-139">Determines whether the dataset is pushed, streamed, or both, with values of "Push" and "Streaming."</span></span>         | <span data-ttu-id="37a05-140">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-140">False</span></span>        |  <span data-ttu-id="37a05-141">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-141">False</span></span>

## <a name="table"></a><span data-ttu-id="37a05-142">ตาราง</span><span class="sxs-lookup"><span data-stu-id="37a05-142">Table</span></span>

<span data-ttu-id="37a05-143">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="37a05-143">Name</span></span>  |<span data-ttu-id="37a05-144">พิมพ์</span><span class="sxs-lookup"><span data-stu-id="37a05-144">Type</span></span>  |<span data-ttu-id="37a05-145">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="37a05-145">Description</span></span>  |<span data-ttu-id="37a05-146">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="37a05-146">Read Only</span></span>  |<span data-ttu-id="37a05-147">จำเป็น</span><span class="sxs-lookup"><span data-stu-id="37a05-147">Required</span></span>
---------|---------|---------|---------|---------
<span data-ttu-id="37a05-148">name</span><span class="sxs-lookup"><span data-stu-id="37a05-148">name</span></span>     | <span data-ttu-id="37a05-149">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-149">String</span></span>        |  <span data-ttu-id="37a05-150">ชื่อตารางที่ผู้ใช้กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="37a05-150">User defined name of the table.</span></span> <span data-ttu-id="37a05-151">นอกจากนี้ยังใช้เป็นตัวระบุตารางด้วย</span><span class="sxs-lookup"><span data-stu-id="37a05-151">It is also used as the identifier of the table.</span></span>       | <span data-ttu-id="37a05-152">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-152">False</span></span>        |  <span data-ttu-id="37a05-153">เป็นจริง</span><span class="sxs-lookup"><span data-stu-id="37a05-153">True</span></span>       
<span data-ttu-id="37a05-154">คอลัมน์</span><span class="sxs-lookup"><span data-stu-id="37a05-154">columns</span></span>     |  <span data-ttu-id="37a05-155">คอลัมน์</span><span class="sxs-lookup"><span data-stu-id="37a05-155">column[]</span></span>       |  <span data-ttu-id="37a05-156">คอลเลกชันของตาราง</span><span class="sxs-lookup"><span data-stu-id="37a05-156">Collection of columns.</span></span>       | <span data-ttu-id="37a05-157">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-157">False</span></span>        |  <span data-ttu-id="37a05-158">เป็นจริง</span><span class="sxs-lookup"><span data-stu-id="37a05-158">True</span></span>       
<span data-ttu-id="37a05-159">หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="37a05-159">measures</span></span>     | <span data-ttu-id="37a05-160">หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="37a05-160">measure[]</span></span>        |  <span data-ttu-id="37a05-161">คอลเลกชันของตาราง</span><span class="sxs-lookup"><span data-stu-id="37a05-161">Collection of measures.</span></span>       | <span data-ttu-id="37a05-162">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-162">False</span></span>        |  <span data-ttu-id="37a05-163">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-163">False</span></span>       
<span data-ttu-id="37a05-164">isHidden</span><span class="sxs-lookup"><span data-stu-id="37a05-164">isHidden</span></span>     | <span data-ttu-id="37a05-165">บูลีน</span><span class="sxs-lookup"><span data-stu-id="37a05-165">Boolean</span></span>        | <span data-ttu-id="37a05-166">ถ้าเป็นจริง ตารางจะถูกซ่อนจากเครื่องมือไคลเอ็นต์</span><span class="sxs-lookup"><span data-stu-id="37a05-166">If true, table will be hidden from client tools.</span></span>        | <span data-ttu-id="37a05-167">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-167">False</span></span>        | <span data-ttu-id="37a05-168">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-168">False</span></span>        

## <a name="column"></a><span data-ttu-id="37a05-169">คอลัมน์แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="37a05-169">Column</span></span>

<span data-ttu-id="37a05-170">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="37a05-170">Name</span></span>  |<span data-ttu-id="37a05-171">พิมพ์</span><span class="sxs-lookup"><span data-stu-id="37a05-171">Type</span></span>  |<span data-ttu-id="37a05-172">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="37a05-172">Description</span></span>  |<span data-ttu-id="37a05-173">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="37a05-173">Read Only</span></span>  |<span data-ttu-id="37a05-174">จำเป็น</span><span class="sxs-lookup"><span data-stu-id="37a05-174">Required</span></span>
---------|---------|---------|---------|---------
<span data-ttu-id="37a05-175">name</span><span class="sxs-lookup"><span data-stu-id="37a05-175">name</span></span>     |  <span data-ttu-id="37a05-176">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-176">String</span></span>        | <span data-ttu-id="37a05-177">ชื่อคอลัมน์ที่ผู้ใช้กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="37a05-177">User defined name of the column.</span></span>        |  <span data-ttu-id="37a05-178">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-178">False</span></span>       | <span data-ttu-id="37a05-179">เป็นจริง</span><span class="sxs-lookup"><span data-stu-id="37a05-179">True</span></span>       
<span data-ttu-id="37a05-180">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="37a05-180">dataType</span></span>     |  <span data-ttu-id="37a05-181">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-181">String</span></span>       |  <span data-ttu-id="37a05-182">[ชนิดข้อมูล EDM](/dotnet/framework/data/adonet/entity-data-model-primitive-data-types)ที่ได้รับการสนับสนุนและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="37a05-182">Supported [EDM data types](/dotnet/framework/data/adonet/entity-data-model-primitive-data-types)  and restrictions.</span></span> <span data-ttu-id="37a05-183">ดู[ข้อจำกัดชนิดของข้อมูล](#data-type-restrictions)</span><span class="sxs-lookup"><span data-stu-id="37a05-183">See [Data type restrictions](#data-type-restrictions).</span></span>      |  <span data-ttu-id="37a05-184">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-184">False</span></span>       | <span data-ttu-id="37a05-185">เป็นจริง</span><span class="sxs-lookup"><span data-stu-id="37a05-185">True</span></span>        
<span data-ttu-id="37a05-186">formatString</span><span class="sxs-lookup"><span data-stu-id="37a05-186">formatString</span></span>     | <span data-ttu-id="37a05-187">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-187">String</span></span>        | <span data-ttu-id="37a05-188">สตริงที่อธิบายว่า ควรจัดรูปแบบค่าอย่างไรเมื่อแสดงค่านั้น</span><span class="sxs-lookup"><span data-stu-id="37a05-188">A string describing how the value should be formatted when it is displayed.</span></span> <span data-ttu-id="37a05-189">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับการจัดรูปแบบสตริง ดู[เนื้อหาFORMAT_STRING](/analysis-services/multidimensional-models/mdx/mdx-cell-properties-format-string-contents)</span><span class="sxs-lookup"><span data-stu-id="37a05-189">To learn more about string formatting, see [FORMAT_STRING Contents](/analysis-services/multidimensional-models/mdx/mdx-cell-properties-format-string-contents).</span></span>      | <span data-ttu-id="37a05-190">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-190">False</span></span>        | <span data-ttu-id="37a05-191">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-191">False</span></span>        
<span data-ttu-id="37a05-192">sortByColumn</span><span class="sxs-lookup"><span data-stu-id="37a05-192">sortByColumn</span></span>    | <span data-ttu-id="37a05-193">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-193">String</span></span>        |   <span data-ttu-id="37a05-194">ชื่อสตริงของคอลัมน์หนึ่งในตารางเดียวกันจะถูกใช้เพื่อจัดลำดับคอลัมน์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="37a05-194">String name of a column in the same table to be used to order the current column.</span></span>     | <span data-ttu-id="37a05-195">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-195">False</span></span>        | <span data-ttu-id="37a05-196">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-196">False</span></span>       
<span data-ttu-id="37a05-197">dataCategory</span><span class="sxs-lookup"><span data-stu-id="37a05-197">dataCategory</span></span>     | <span data-ttu-id="37a05-198">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-198">String</span></span>        |  <span data-ttu-id="37a05-199">ค่าสตริงที่จะใช้กับประเภทของข้อมูลซึ่งอธิบายเกี่ยวกับข้อมูลภายในคอลัมน์นี้</span><span class="sxs-lookup"><span data-stu-id="37a05-199">String value to be used for the data category which describes the data within this column.</span></span> <span data-ttu-id="37a05-200">ค่าบางค่าทั่วไปรวมถึง: ที่อยู่ เมือง ทวีป ประเทศ รูปภาพ ImageUrl ละติจูด ลองติจูด องค์กร ตำแหน่ง รหัสไปรษณีย์ รัฐหรือมณฑล WebUrl</span><span class="sxs-lookup"><span data-stu-id="37a05-200">Some common values include: Address, City, Continent, Country, Image, ImageUrl, Latitude, Longitude, Organization, Place, PostalCode, StateOrProvince, WebUrl</span></span>       |  <span data-ttu-id="37a05-201">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-201">False</span></span>       | <span data-ttu-id="37a05-202">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-202">False</span></span>        
<span data-ttu-id="37a05-203">isHidden</span><span class="sxs-lookup"><span data-stu-id="37a05-203">isHidden</span></span>    |  <span data-ttu-id="37a05-204">บูลีน</span><span class="sxs-lookup"><span data-stu-id="37a05-204">Boolean</span></span>       |  <span data-ttu-id="37a05-205">คุณสมบัติที่ระบุว่าคอลัมน์ถูกซ่อนจากมุมมองหรือไม่</span><span class="sxs-lookup"><span data-stu-id="37a05-205">Property indicating if the column is hidden from view.</span></span> <span data-ttu-id="37a05-206">ค่าเริ่มต้นเป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-206">Default is false.</span></span>       | <span data-ttu-id="37a05-207">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-207">False</span></span>        | <span data-ttu-id="37a05-208">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-208">False</span></span>        
<span data-ttu-id="37a05-209">summarizeBy</span><span class="sxs-lookup"><span data-stu-id="37a05-209">summarizeBy</span></span>     | <span data-ttu-id="37a05-210">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-210">String</span></span>        |  <span data-ttu-id="37a05-211">วิธีการรวมแบบเริ่มต้นสำหรับคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="37a05-211">Default aggregation method for the column.</span></span> <span data-ttu-id="37a05-212">ค่า รวมถึง: ค่าเริ่มต้น ไม่มีค่า ผลรวม ค่าน้อยสุด ค่าสูงสุด จำนวนนับ ค่าเฉลี่ย distinctCount</span><span class="sxs-lookup"><span data-stu-id="37a05-212">Values include: default, none, sum, min, max, count, average, distinctCount</span></span>     |  <span data-ttu-id="37a05-213">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-213">False</span></span>       | <span data-ttu-id="37a05-214">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-214">False</span></span>

## <a name="measure"></a><span data-ttu-id="37a05-215">หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="37a05-215">Measure</span></span>

<span data-ttu-id="37a05-216">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="37a05-216">Name</span></span>  |<span data-ttu-id="37a05-217">พิมพ์</span><span class="sxs-lookup"><span data-stu-id="37a05-217">Type</span></span>  |<span data-ttu-id="37a05-218">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="37a05-218">Description</span></span>  |<span data-ttu-id="37a05-219">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="37a05-219">Read Only</span></span>  |<span data-ttu-id="37a05-220">จำเป็น</span><span class="sxs-lookup"><span data-stu-id="37a05-220">Required</span></span>
---------|---------|---------|---------|---------
<span data-ttu-id="37a05-221">name</span><span class="sxs-lookup"><span data-stu-id="37a05-221">name</span></span>     | <span data-ttu-id="37a05-222">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-222">String</span></span>        |  <span data-ttu-id="37a05-223">ชื่อหน่วยวัดที่ผู้ใช้กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="37a05-223">User defined name of the measure.</span></span>       |  <span data-ttu-id="37a05-224">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-224">False</span></span>       | <span data-ttu-id="37a05-225">เป็นจริง</span><span class="sxs-lookup"><span data-stu-id="37a05-225">True</span></span>        
<span data-ttu-id="37a05-226">นิพจน์</span><span class="sxs-lookup"><span data-stu-id="37a05-226">expression</span></span>     | <span data-ttu-id="37a05-227">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-227">String</span></span>        | <span data-ttu-id="37a05-228">นิพจน์ DAX ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="37a05-228">A valid DAX expression.</span></span>        | <span data-ttu-id="37a05-229">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-229">False</span></span>        |  <span data-ttu-id="37a05-230">เป็นจริง</span><span class="sxs-lookup"><span data-stu-id="37a05-230">True</span></span>       
<span data-ttu-id="37a05-231">formatString</span><span class="sxs-lookup"><span data-stu-id="37a05-231">formatString</span></span>     | <span data-ttu-id="37a05-232">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-232">String</span></span>        |  <span data-ttu-id="37a05-233">สตริงที่อธิบายว่า ควรจัดรูปแบบค่าอย่างไรเมื่อแสดงค่านั้น</span><span class="sxs-lookup"><span data-stu-id="37a05-233">A string describing how the value should be formatted when it is displayed.</span></span> <span data-ttu-id="37a05-234">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับการจัดรูปแบบสตริง ดู[เนื้อหาFORMAT_STRING](/analysis-services/multidimensional-models/mdx/mdx-cell-properties-format-string-contents)</span><span class="sxs-lookup"><span data-stu-id="37a05-234">To learn more about string formatting, see [FORMAT_STRING Contents](/analysis-services/multidimensional-models/mdx/mdx-cell-properties-format-string-contents).</span></span>       | <span data-ttu-id="37a05-235">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-235">False</span></span>        | <span data-ttu-id="37a05-236">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-236">False</span></span>        
<span data-ttu-id="37a05-237">isHidden</span><span class="sxs-lookup"><span data-stu-id="37a05-237">isHidden</span></span>     | <span data-ttu-id="37a05-238">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-238">String</span></span>        |  <span data-ttu-id="37a05-239">ถ้าเป็นจริง ตารางจะถูกซ่อนจากเครื่องมือไคลเอ็นต์</span><span class="sxs-lookup"><span data-stu-id="37a05-239">If true, table will be hidden from client tools.</span></span>       |  <span data-ttu-id="37a05-240">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-240">False</span></span>       | <span data-ttu-id="37a05-241">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-241">False</span></span>       

## <a name="relationship"></a><span data-ttu-id="37a05-242">ความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="37a05-242">Relationship</span></span>

<span data-ttu-id="37a05-243">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="37a05-243">Name</span></span>  |<span data-ttu-id="37a05-244">พิมพ์</span><span class="sxs-lookup"><span data-stu-id="37a05-244">Type</span></span>  |<span data-ttu-id="37a05-245">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="37a05-245">Description</span></span>  |<span data-ttu-id="37a05-246">อ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="37a05-246">Read Only</span></span>  |<span data-ttu-id="37a05-247">จำเป็น</span><span class="sxs-lookup"><span data-stu-id="37a05-247">Required</span></span> 
---------|---------|---------|---------|---------
<span data-ttu-id="37a05-248">name</span><span class="sxs-lookup"><span data-stu-id="37a05-248">name</span></span>     | <span data-ttu-id="37a05-249">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-249">String</span></span>        | <span data-ttu-id="37a05-250">ชื่อความสัมพันธ์ที่ผู้ใช้กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="37a05-250">User defined name of the relationship.</span></span> <span data-ttu-id="37a05-251">นอกจากนี้ยังใช้เป็นตัวระบุความสัมพันธ์ด้วย</span><span class="sxs-lookup"><span data-stu-id="37a05-251">It is also used as the identifier of the relationship.</span></span>        | <span data-ttu-id="37a05-252">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-252">False</span></span>       | <span data-ttu-id="37a05-253">เป็นจริง</span><span class="sxs-lookup"><span data-stu-id="37a05-253">True</span></span>        
<span data-ttu-id="37a05-254">crossFilteringBehavior</span><span class="sxs-lookup"><span data-stu-id="37a05-254">crossFilteringBehavior</span></span>     | <span data-ttu-id="37a05-255">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-255">String</span></span>        |    <span data-ttu-id="37a05-256">ทิศทางตัวกรองของความสัมพันธ์: ทางเดียว (ค่าเริ่มต้น), ทั้งสองทาง อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="37a05-256">The filter direction of the relationship: OneDirection (default), BothDirections, Automatic</span></span>       | <span data-ttu-id="37a05-257">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-257">False</span></span>        | <span data-ttu-id="37a05-258">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-258">False</span></span>        
<span data-ttu-id="37a05-259">fromTable</span><span class="sxs-lookup"><span data-stu-id="37a05-259">fromTable</span></span>     | <span data-ttu-id="37a05-260">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-260">String</span></span>        | <span data-ttu-id="37a05-261">ชื่อของตาราง foreign key</span><span class="sxs-lookup"><span data-stu-id="37a05-261">Name of the foreign key table.</span></span>        | <span data-ttu-id="37a05-262">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-262">False</span></span>        | <span data-ttu-id="37a05-263">เป็นจริง</span><span class="sxs-lookup"><span data-stu-id="37a05-263">True</span></span>         
<span data-ttu-id="37a05-264">fromColumn</span><span class="sxs-lookup"><span data-stu-id="37a05-264">fromColumn</span></span>    | <span data-ttu-id="37a05-265">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-265">String</span></span>        | <span data-ttu-id="37a05-266">ชื่อของคอลัมน์ foreign key</span><span class="sxs-lookup"><span data-stu-id="37a05-266">Name of the foreign key column.</span></span>        | <span data-ttu-id="37a05-267">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-267">False</span></span>        | <span data-ttu-id="37a05-268">เป็นจริง</span><span class="sxs-lookup"><span data-stu-id="37a05-268">True</span></span>         
<span data-ttu-id="37a05-269">toTable</span><span class="sxs-lookup"><span data-stu-id="37a05-269">toTable</span></span>    | <span data-ttu-id="37a05-270">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-270">String</span></span>        | <span data-ttu-id="37a05-271">ชื่อของตารางคีย์หลัก</span><span class="sxs-lookup"><span data-stu-id="37a05-271">Name of the primary key table.</span></span>        | <span data-ttu-id="37a05-272">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-272">False</span></span>        | <span data-ttu-id="37a05-273">เป็นจริง</span><span class="sxs-lookup"><span data-stu-id="37a05-273">True</span></span>         
<span data-ttu-id="37a05-274">toColumn</span><span class="sxs-lookup"><span data-stu-id="37a05-274">toColumn</span></span>     | <span data-ttu-id="37a05-275">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-275">String</span></span>        | <span data-ttu-id="37a05-276">ชื่อของคอลัมน์คีย์หลัก</span><span class="sxs-lookup"><span data-stu-id="37a05-276">Name of the primary key column.</span></span>        | <span data-ttu-id="37a05-277">เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-277">False</span></span>        | <span data-ttu-id="37a05-278">เป็นจริง</span><span class="sxs-lookup"><span data-stu-id="37a05-278">True</span></span>        

## <a name="data-type-restrictions"></a><span data-ttu-id="37a05-279">ข้อจำกัดของชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="37a05-279">Data type restrictions</span></span>

<span data-ttu-id="37a05-280">ข้อจำกัดเหล่านี้นำไปใช้กับคุณสมบัติชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="37a05-280">These restrictions apply to dataType property.</span></span>

<span data-ttu-id="37a05-281">ชนิดของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="37a05-281">Data type</span></span>  |<span data-ttu-id="37a05-282">ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="37a05-282">Restrictions</span></span>  
---------|---------
<span data-ttu-id="37a05-283">Int64</span><span class="sxs-lookup"><span data-stu-id="37a05-283">Int64</span></span>     |   <span data-ttu-id="37a05-284">Int64.MaxValue และ Int64.MinValue ไม่ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="37a05-284">Int64.MaxValue and Int64.MinValue not allowed.</span></span>      
<span data-ttu-id="37a05-285">สองครั้ง</span><span class="sxs-lookup"><span data-stu-id="37a05-285">Double</span></span>     |  <span data-ttu-id="37a05-286">Double.MaxValue และค่า Double.MinValue ไม่ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="37a05-286">Double.MaxValue and Double.MinValue values not allowed.</span></span> <span data-ttu-id="37a05-287">NaN ที่ไม่ได้รับการสนับสนุน + ค่าอนันต์และ - ค่าอนันต์ที่ไม่ได้รับการสนับสนุนในบางฟังก์ชัน (เช่น Min, Max)</span><span class="sxs-lookup"><span data-stu-id="37a05-287">NaN not supported.+Infinity and -Infinity not supported in some functions (e.g. Min, Max).</span></span>       
<span data-ttu-id="37a05-288">บูลีน</span><span class="sxs-lookup"><span data-stu-id="37a05-288">Boolean</span></span>     |   <span data-ttu-id="37a05-289">เป็นจริง หรือ เป็นเท็จ</span><span class="sxs-lookup"><span data-stu-id="37a05-289">True or False.</span></span>
<span data-ttu-id="37a05-290">วันที่เวลา</span><span class="sxs-lookup"><span data-stu-id="37a05-290">Datetime</span></span>    |   <span data-ttu-id="37a05-291">ในระหว่างการโหลดข้อมูล เราแบ่งนับค่าด้วยเศษส่วนวันให้กับตัวคูณทั้งหมดของ 1/300 วินาที (3.33ms)</span><span class="sxs-lookup"><span data-stu-id="37a05-291">During data loading we quantize values with day fractions to whole multiples of 1/300 seconds (3.33ms).</span></span>      
<span data-ttu-id="37a05-292">สตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-292">String</span></span>     |  <span data-ttu-id="37a05-293">ในขณะนี้ อนุญาตให้สูงสุด 4000 ตัวอักขระสำหรับแต่ละค่าสตริง</span><span class="sxs-lookup"><span data-stu-id="37a05-293">Currently allows up to 4000 characters per string value.</span></span>
<span data-ttu-id="37a05-294">ทศนิยม</span><span class="sxs-lookup"><span data-stu-id="37a05-294">Decimal</span></span>|<span data-ttu-id="37a05-295">ความแม่นยำ = 28 สเกล = 4</span><span class="sxs-lookup"><span data-stu-id="37a05-295">precision=28, scale=4</span></span>

## <a name="example"></a><span data-ttu-id="37a05-296">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="37a05-296">Example</span></span>
<span data-ttu-id="37a05-297">ตัวอย่างโค้ดต่อไปนี้รวมถึงคุณสมบัติเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="37a05-297">The following code sample includes a number of these properties:</span></span>

```json
{

  "name": "PushAdvanced",

  "tables": [

    {

      "name": "Date",

      "columns": [

        {

          "name": "Date",

          "dataType": "dateTime",

          "formatString": "dddd\\, mmmm d\\, yyyy",

          "summarizeBy": "none"

        }

      ]

    },

    {

      "name": "sales",

      "columns": [

        {

          "name": "Date",

          "dataType": "dateTime",

          "formatString": "dddd\\, mmmm d\\, yyyy",

          "summarizeBy": "none"

        },

        {

          "name": "Sales",

          "dataType": "int64",

          "formatString": "0",

          "summarizeBy": "sum"

        }

      ],

      "measures": [

        {

          "name": "percent to forecast",

          "expression": "SUM(sales[Sales])/SUM(forecast[forecast])",

          "formatString": "0.00 %;-0.00 %;0.00 %"

        }

      ]

    },

    {

      "name": "forecast",

      "columns": [

        {

          "name": "date",

          "dataType": "dateTime",

          "formatString": "m/d/yyyy",

          "summarizeBy": "none"

        },

        {

          "name": "forecast",

          "dataType": "int64",

          "formatString": "0",

          "summarizeBy": "sum"

        }

      ]

    }

  ],

  "relationships": [

    {

      "name": "2ea345ce-b147-436e-8ac2-9d3c4d82af8d",

      "fromTable": "sales",

      "fromColumn": "Date",

      "toTable": "Date",

      "toColumn": "Date",

      "crossFilteringBehavior": "bothDirections"

    },

    {

      "name": "5d95f419-e589-4345-9581-6e70670b1bba",

      "fromTable": "forecast",

      "fromColumn": "date",

      "toTable": "Date",

      "toColumn": "Date",

      "crossFilteringBehavior": "bothDirections"

    }

  ]

}
```