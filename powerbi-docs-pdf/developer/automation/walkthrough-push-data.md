---
title: ส่งข้อมูลไปยังชุดข้อมูลในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: ส่งข้อมูลไปยังชุดข้อมูล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: rkarlin
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: tutorial
ms.date: 05/22/2019
ms.openlocfilehash: 3c5805f4d498e8e2d8a788c5703a09a8109e024b
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887442"
---
# <a name="push-data-into-a-power-bi-dataset"></a><span data-ttu-id="9577a-104">ส่งข้อมูลลงในชุดข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="9577a-104">Push data into a Power BI dataset</span></span>

<span data-ttu-id="9577a-105">Power BI API ช่วยให้คุณสามารถส่งข้อมูลลงในชุดข้อมูล Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="9577a-105">The Power BI API lets you push data into a Power BI dataset.</span></span> <span data-ttu-id="9577a-106">ในบทความนี้ เราจะแสดงวิธีการส่งชุดข้อมูลการตลาดการขายที่มีตารางผลิตภัณฑ์ลงในชุดข้อมูลที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="9577a-106">In this article, we show you how to push a Sales Marketing dataset containing a Product table into an existing dataset.</span></span>

<span data-ttu-id="9577a-107">ก่อนที่คุณเริ่มต้นใช้งาน คุณจำเป็นต้องมี Azure Active Directory (Azure AD) และ[บัญชี Power BI](../embedded/create-an-azure-active-directory-tenant.md)</span><span class="sxs-lookup"><span data-stu-id="9577a-107">Before getting started, you need an Azure Active Directory (Azure AD) and a [Power BI account](../embedded/create-an-azure-active-directory-tenant.md).</span></span>

## <a name="steps-to-push-data-into-a-dataset"></a><span data-ttu-id="9577a-108">ขั้นตอนการส่งข้อมูลลงในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9577a-108">Steps to push data into a dataset</span></span>

* <span data-ttu-id="9577a-109">ขั้นตอนที่ 1: [ลงทะเบียนแอปกับ Azure AD](../embedded/register-app.md)</span><span class="sxs-lookup"><span data-stu-id="9577a-109">Step 1: [Register an app with Azure AD](../embedded/register-app.md)</span></span>
* <span data-ttu-id="9577a-110">ขั้นตอนที่ 2: [รับโทเค็นการเข้าถึงการรับรองความถูกต้อง](walkthrough-push-data-get-token.md)</span><span class="sxs-lookup"><span data-stu-id="9577a-110">Step 2: [Get an authentication access token](walkthrough-push-data-get-token.md)</span></span>
* <span data-ttu-id="9577a-111">ขั้นตอนที่ 3: [สร้างชุดข้อมูลใน Power BI](walkthrough-push-data-create-dataset.md)</span><span class="sxs-lookup"><span data-stu-id="9577a-111">Step 3: [Create a dataset in Power BI](walkthrough-push-data-create-dataset.md)</span></span>
* <span data-ttu-id="9577a-112">ขั้นตอนที่ 4: [รับชุดข้อมูลเพื่อเพิ่มแถวลงในตาราง Power BI](walkthrough-push-data-get-datasets.md)</span><span class="sxs-lookup"><span data-stu-id="9577a-112">Step 4: [Get a dataset to add rows into a Power BI table](walkthrough-push-data-get-datasets.md)</span></span>
* <span data-ttu-id="9577a-113">ขั้นตอนที่ 5: [เพิ่มแถวลงในตาราง Power BI](walkthrough-push-data-add-rows.md)</span><span class="sxs-lookup"><span data-stu-id="9577a-113">Step 5: [Add rows to a Power BI table](walkthrough-push-data-add-rows.md)</span></span>

<span data-ttu-id="9577a-114">ในส่วนถัดไปคือการสนทนาทั่วไปของการดำเนินการ Power BI API ที่ส่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9577a-114">The next section is a general discussion of Power BI API operations that push data.</span></span>

## <a name="power-bi-api-operations-to-push-data"></a><span data-ttu-id="9577a-115">การดำเนินการของ BI API power เพื่อส่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9577a-115">Power BI API operations to push data</span></span>

<span data-ttu-id="9577a-116">คุณสามารถส่งแหล่งข้อมูลไปยัง Power BI ได้โดยใช้ Power BI REST API</span><span class="sxs-lookup"><span data-stu-id="9577a-116">With the Power BI REST API, you can push data sources to Power BI.</span></span> <span data-ttu-id="9577a-117">เมื่อแอปจะเพิ่มแถวไปยังชุดข้อมูล ไทล์แดชบอร์ดจะอัปเดตโดยอัตโนมัติด้วยข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="9577a-117">When an app adds rows to a dataset, dashboard tiles update automatically with the new data.</span></span> <span data-ttu-id="9577a-118">เมื่อต้องการส่งข้อมูล ใช้การดำเนินการ [PostDataset](/rest/api/power-bi/pushdatasets/datasets_postdataset) และ [PostRows](/rest/api/power-bi/pushdatasets/datasets_postrows)</span><span class="sxs-lookup"><span data-stu-id="9577a-118">To push data, use the [PostDataset](/rest/api/power-bi/pushdatasets/datasets_postdataset) and [PostRows](/rest/api/power-bi/pushdatasets/datasets_postrows) operations.</span></span> <span data-ttu-id="9577a-119">เมื่อต้องการค้นหาชุดข้อมูล ให้ใช้การดำเนินการ[รับชุดข้อมูล](/rest/api/power-bi/datasets/getdatasets)</span><span class="sxs-lookup"><span data-stu-id="9577a-119">To find a dataset, use the [Get Datasets](/rest/api/power-bi/datasets/getdatasets) operation.</span></span> <span data-ttu-id="9577a-120">คุณสามารถส่ง ID ของกลุ่มเพื่อทำงานกับกลุ่มได้จากการดำเนินการเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="9577a-120">You can pass a group ID to work with a group for any of these operations.</span></span> <span data-ttu-id="9577a-121">ใช้การดำเนินการ[รับชุดข้อมูล](/rest/api/power-bi/groups/getgroups)เพื่อรับรายการของรหัสกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="9577a-121">To get a group ID list, use the [Get Groups](/rest/api/power-bi/groups/getgroups) operation.</span></span>

<span data-ttu-id="9577a-122">ต่อไปนี้เป็นการดำเนินการเพื่อส่งข้อมูลลงในชุดข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="9577a-122">Here are the operations to push data into a dataset:</span></span>

* [<span data-ttu-id="9577a-123">โพสต์ชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9577a-123">PostDataset</span></span>](/rest/api/power-bi/pushdatasets/datasets_postdataset)
* [<span data-ttu-id="9577a-124">รับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9577a-124">Get Datasets</span></span>](/rest/api/power-bi/datasets/getdatasets)
* [<span data-ttu-id="9577a-125">โพสต์แถว</span><span class="sxs-lookup"><span data-stu-id="9577a-125">Post Rows</span></span>](/rest/api/power-bi/pushdatasets/datasets_postrows)
* [<span data-ttu-id="9577a-126">รับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="9577a-126">Get Groups</span></span>](/rest/api/power-bi/groups/getgroups)

<span data-ttu-id="9577a-127">คุณสามารถสร้างชุดข้อมูลใน Power BI ได้โดยการส่งสตริง JavaScript Object Notation (JSON) ไปยังบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="9577a-127">You create a dataset in Power BI by passing a JavaScript Object Notation (JSON) string to the Power BI service.</span></span> <span data-ttu-id="9577a-128">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับ JSON ดู[การแนะนำ JSON](https://json.org/)</span><span class="sxs-lookup"><span data-stu-id="9577a-128">To learn more about JSON, see [Introducing JSON](https://json.org/).</span></span>

<span data-ttu-id="9577a-129">สตริง JSON สำหรับชุดข้อมูลที่มีรูปแบบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9577a-129">The JSON string for a dataset has the following format:</span></span>

<span data-ttu-id="9577a-130">**Power BI ชุดข้อมูล JSON วัตถุ**</span><span class="sxs-lookup"><span data-stu-id="9577a-130">**Power BI Dataset JSON object**</span></span>

```json
{"name": "dataset_name", "tables":
    [{"name": "", "columns":
        [{ "name": "column_name1", "dataType": "data_type"},
         { "name": "column_name2", "dataType": "data_type"},
         { ... }
        ]
      }
    ]
}
```

<span data-ttu-id="9577a-131">สำหรับตัวอย่างชุดข้อมูลการขายและการตลาดของเรา คุณจะผ่านสตริง JSON ดังที่แสดงด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="9577a-131">For our Sales Marketing dataset example, you would pass a JSON string as shown below.</span></span> <span data-ttu-id="9577a-132">ในตัวอย่างนี้ **การขายและการตลาด** คือชื่อของชุดข้อมูล และ **ผลิตภัณฑ์** คือชื่อของตาราง</span><span class="sxs-lookup"><span data-stu-id="9577a-132">In this example, **SalesMarketing** is the dataset name, and **Product** is the table name.</span></span> <span data-ttu-id="9577a-133">หลังจากที่คุณกำหนดตาราง จากนั้นกำหนด schema ของตาราง</span><span class="sxs-lookup"><span data-stu-id="9577a-133">After defining the table, you define the table schema.</span></span> <span data-ttu-id="9577a-134">สำหรับ **ชุดข้อมูลการขายและการตลาด** และสคีของตารางมีคอลัมน์เหล่านี้: รหัสผลิตภัณฑ์ ผู้ผลิต ประเภท ส่วน ผลิตภัณฑ์ และ เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="9577a-134">For the **SalesMarketing** dataset, the table schema has these columns: ProductID, Manufacturer, Category, Segment, Product, and IsCompete.</span></span>

<span data-ttu-id="9577a-135">**ตัวอย่างชุดข้อมูลวัตถุ JSON**</span><span class="sxs-lookup"><span data-stu-id="9577a-135">**Example dataset object JSON**</span></span>

```json
{
    "name": "SalesMarketing",
    "tables": [
        {
            "name": "Product",
            "columns": [
            {
                "name": "ProductID",
                "dataType": "int"
            },
            {
                "name": "Manufacturer",
                "dataType": "string"
            },
            {
                "name": "Category",
                "dataType": "string"
            },
            {
                "name": "Segment",
                "dataType": "string"
            },
            {
                "name": "Product",
                "dataType": "string"
            },
            {
                "name": "IsCompete",
                "dataType": "bool"
            }
            ]
        }
    ]
}
```

<span data-ttu-id="9577a-136">คุณสามารถใช้ชนิดข้อมูลต่อไปนี้สำหรับสคีของตาราง Power BI</span><span class="sxs-lookup"><span data-stu-id="9577a-136">For a Power BI table schema, you can use the following data types.</span></span>

## <a name="power-bi-table-data-types"></a><span data-ttu-id="9577a-137">ชนิดข้อมูลตาราง Power BI</span><span class="sxs-lookup"><span data-stu-id="9577a-137">Power BI table data types</span></span>

| <span data-ttu-id="9577a-138">**ชนิดของข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="9577a-138">**Data type**</span></span> | <span data-ttu-id="9577a-139">**ข้อจำกัด**</span><span class="sxs-lookup"><span data-stu-id="9577a-139">**Restrictions**</span></span> |
| --- | --- |
| <span data-ttu-id="9577a-140">Int64</span><span class="sxs-lookup"><span data-stu-id="9577a-140">Int64</span></span> |<span data-ttu-id="9577a-141">Int64.MaxValue และ Int64.MinValue ไม่ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="9577a-141">Int64.MaxValue and Int64.MinValue not allowed.</span></span> |
| <span data-ttu-id="9577a-142">สองครั้ง</span><span class="sxs-lookup"><span data-stu-id="9577a-142">Double</span></span> |<span data-ttu-id="9577a-143">Double.MaxValue และค่า Double.MinValue ไม่ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="9577a-143">Double.MaxValue and Double.MinValue values not allowed.</span></span> <span data-ttu-id="9577a-144">NaN ที่ไม่ได้รับการสนับสนุน + ค่าอนันต์และ - ค่าอนันต์ที่ไม่ได้รับการสนับสนุนในบางฟังก์ชัน (เช่น  Min, Max)</span><span class="sxs-lookup"><span data-stu-id="9577a-144">NaN not supported.+Infinity and -Infinity not supported in some functions (for example, Min, Max).</span></span> |
| <span data-ttu-id="9577a-145">บูลีน</span><span class="sxs-lookup"><span data-stu-id="9577a-145">Boolean</span></span> |<span data-ttu-id="9577a-146">ไม่มี</span><span class="sxs-lookup"><span data-stu-id="9577a-146">None</span></span> |
| <span data-ttu-id="9577a-147">วันที่เวลา</span><span class="sxs-lookup"><span data-stu-id="9577a-147">Datetime</span></span> |<span data-ttu-id="9577a-148">ในระหว่างการโหลดข้อมูล เราแบ่งนับค่าด้วยเศษส่วนวันให้กับตัวคูณทั้งหมดของ 1/300 วินาที (3.33ms)</span><span class="sxs-lookup"><span data-stu-id="9577a-148">During data loading, we quantize values with day fractions to whole multiples of 1/300 seconds (3.33 ms).</span></span> |
| <span data-ttu-id="9577a-149">สตริง</span><span class="sxs-lookup"><span data-stu-id="9577a-149">String</span></span> |<span data-ttu-id="9577a-150">อนุญาตให้มีอักขระได้ถึง 128 K อักขระในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="9577a-150">Currently allows up to 128 K characters.</span></span> |

## <a name="learn-more-about-pushing-data-into-power-bi"></a><span data-ttu-id="9577a-151">เรียนรู้เพิ่มเติมเกี่ยวกับการส่งข้อมูลลงใน Power BI</span><span class="sxs-lookup"><span data-stu-id="9577a-151">Learn more about pushing data into Power BI</span></span>

<span data-ttu-id="9577a-152">เมื่อต้องเริ่มส่งข้อมูลลงในชุดข้อมูล ให้ดูที่[ขั้นตอนที่ 1: ลงทะเบียนแอปกับ Azure AD](../embedded/register-app.md) ซึ่งอยู่ในบานหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="9577a-152">To get started pushing data into a dataset, see [Step 1: Register an app with Azure AD](../embedded/register-app.md) in the nav pane.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9577a-153">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="9577a-153">Next steps</span></span>

* [<span data-ttu-id="9577a-154">ลงทะเบียนใช้งาน Power BI</span><span class="sxs-lookup"><span data-stu-id="9577a-154">Sign up for Power BI</span></span>](../embedded/create-an-azure-active-directory-tenant.md)  
* [<span data-ttu-id="9577a-155">การแนะนำ JSON</span><span class="sxs-lookup"><span data-stu-id="9577a-155">Introducing JSON</span></span>](https://json.org/)  
* [<span data-ttu-id="9577a-156">ภาพรวมของ Power BI REST API</span><span class="sxs-lookup"><span data-stu-id="9577a-156">Overview of Power BI REST API</span></span>](overview-of-power-bi-rest-api.md)  

<span data-ttu-id="9577a-157">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="9577a-157">More questions?</span></span> [<span data-ttu-id="9577a-158">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="9577a-158">Try the Power BI Community</span></span>](https://community.powerbi.com/)