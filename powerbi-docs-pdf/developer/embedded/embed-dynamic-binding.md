---
title: เชื่อมต่อรายงานกับชุดข้อมูลโดยใช้การผูกแบบไดนามิกสำหรับข้อมูลเชิงลึก BI แบบฝังในการวิเคราะห์แบบฝังของ Power BI
description: เรียนรู้วิธีการฝังรายงานโดยใช้การผูกแบบไดนามิกในการวิเคราะห์แบบฝังตัวของ Power BI การสร้างข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นสำหรับลูกค้าของคุณ
author: KesemSharabi
ms.author: kesharab
ms.topic: how-to
ms.service: powerbi
ms.subservice: powerbi-developer
ms.date: 11/07/2019
ms.openlocfilehash: aacae4dbfae30d72468419a717340c806c6c4bca
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888914"
---
# <a name="connect-a-report-to-a-dataset-using-dynamic-binding"></a><span data-ttu-id="c6578-103">เชื่อมต่อรายงานไปยังชุดข้อมูลโดยใช้การผูกแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="c6578-103">Connect a report to a dataset using dynamic binding</span></span> 

<span data-ttu-id="c6578-104">เมื่อเชื่อมต่อรายงานกับชุดข้อมูล คุณสามารถใช้การผูกแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="c6578-104">When a report is connected to a dataset, you can use dynamic binding.</span></span> <span data-ttu-id="c6578-105">การเชื่อมต่อระหว่างรายงานและชุดข้อมูล จะเรียกว่า *การผูก*</span><span class="sxs-lookup"><span data-stu-id="c6578-105">The connection between the report and the dataset, is known as *binding*.</span></span> <span data-ttu-id="c6578-106">เมื่อมีการกำหนดว่าจะผูกข้อมูลไว้ที่จุดของการฝัง ซึ่งตรงข้ามกับที่กำหนดไว้ก่อนหน้านี้ การผูกดังกล่าวจะเรียกว่า การผูกแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="c6578-106">When the binding is determined at the point of embedding, as opposed to being predetermined earlier, the binding is known as dynamic binding.</span></span>

<span data-ttu-id="c6578-107">เมื่อทำการฝังรายงาน Power BI โดยใช้ *การผูกแบบไดนามิก* คุณสามารถเชื่อมต่อรายงานเดียวกันกับชุดข้อมูลที่แตกต่างกันได้ ทั้งนี้ขึ้นอยู่กับข้อมูลประจำตัวของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="c6578-107">When embedding a Power BI report using *dynamic binding*, you can connect the same report to different datasets depending on the user's credentials.</span></span>

<span data-ttu-id="c6578-108">ซึ่งหมายความว่าคุณสามารถใช้รายงานเดียวเพื่อแสดงข้อมูลที่แตกต่างกันได้ ทั้งนี้ขึ้นอยู่กับชุดข้อมูลที่เชื่อมต่ออยู่</span><span class="sxs-lookup"><span data-stu-id="c6578-108">This means that you can use one report to display different information, depending on the dataset it's connected to.</span></span> <span data-ttu-id="c6578-109">ตัวอย่างเช่น รายงานที่แสดงมูลค่ายอดขายสำหรับการค้าปลีกสามารถเชื่อมต่อกับชุดข้อมูลผู้ค้าปลีกที่แตกต่างกัน และให้ผลลัพธ์ที่แตกต่างกันได้ โดยขึ้นอยู่กับชุดข้อมูลของผู้ค้าปลีกที่เชื่อมต่ออยู่</span><span class="sxs-lookup"><span data-stu-id="c6578-109">For example, a report showing retail sale values can be connected to different retailer datasets, and produce different results, depending on the dataset of the retailer it's connected to.</span></span>

<span data-ttu-id="c6578-110">รายงานและชุดข้อมูลไม่จำเป็นต้องอยู่ในพื้นที่ทำงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="c6578-110">The report and the dataset don't need to reside in the same workspace.</span></span> <span data-ttu-id="c6578-111">พื้นที่ทำงานทั้งสอง (พื้นที่หนึ่งประกอบด้วยรายงาน และอีกหนึ่งประกอบด้วยชุดข้อมูล) ต้องถูกกำหนดไปยัง[ความจุ](azure-pbie-create-capacity.md)</span><span class="sxs-lookup"><span data-stu-id="c6578-111">Both workspaces (the one containing the report, and the one containing the dataset) must be assigned to a [capacity](azure-pbie-create-capacity.md).</span></span>

<span data-ttu-id="c6578-112">ในฐานะที่เป็นส่วนหนึ่งของกระบวนการฝัง ตรวจสอบให้แน่ใจว่าคุณ *สร้างโทเค็นที่มีสิทธิ์เพียงพอ* และ *ปรับเปลี่ยนออบเจ็กต์การกำหนดค่า* แล้ว</span><span class="sxs-lookup"><span data-stu-id="c6578-112">As part of the embedding process, make sure you *generate a token with sufficient permissions*, and *adjust the config object*.</span></span>

## <a name="generating-a-token-with-sufficient-permissions"></a><span data-ttu-id="c6578-113">การสร้างโทเค็นที่มีสิทธิ์เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="c6578-113">Generating a token with sufficient permissions</span></span>

<span data-ttu-id="c6578-114">การผูกแบบไดนามิกสนับสนุนทั้งสถานการณ์ *การฝังสำหรับองค์กรของคุณ* และ *การฝังสำหรับลูกค้าของคุณ*</span><span class="sxs-lookup"><span data-stu-id="c6578-114">Dynamic binding is supported for both *Embedding for your organization* and *Embedding for your customers* scenarios.</span></span> <span data-ttu-id="c6578-115">ตารางด้านล่างนี้อธิบายถึงข้อควรพิจารณาสำหรับแต่ละสถานการณ์สมมติ</span><span class="sxs-lookup"><span data-stu-id="c6578-115">The table below describes the considerations for each scenario.</span></span>

|<span data-ttu-id="c6578-116">สถานการณ์สมมติ</span><span class="sxs-lookup"><span data-stu-id="c6578-116">Scenario</span></span>  |<span data-ttu-id="c6578-117">ความเป็นเจ้าของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c6578-117">Data ownership</span></span>  |<span data-ttu-id="c6578-118">โทเค็น</span><span class="sxs-lookup"><span data-stu-id="c6578-118">Token</span></span>  |<span data-ttu-id="c6578-119">ข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="c6578-119">Requirements</span></span>  |
|---------|---------|---------|---------|
|<span data-ttu-id="c6578-120">*การฝังสำหรับองค์กรของคุณ*</span><span class="sxs-lookup"><span data-stu-id="c6578-120">*Embedding for your organization*</span></span>    |<span data-ttu-id="c6578-121">ผู้ใช้เป็นเจ้าของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c6578-121">User owns data</span></span>         |<span data-ttu-id="c6578-122">โทเค็นการเข้าถึงสำหรับผู้ใช้ Power BI</span><span class="sxs-lookup"><span data-stu-id="c6578-122">Access token for Power BI users</span></span>         |<span data-ttu-id="c6578-123">ผู้ใช้ที่ใช้โทเค็น Azure AD ต้องมีสิทธิ์ที่เหมาะสมสำหรับอาร์ทิแฟกต์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c6578-123">The user who's Azure AD token is used, must have appropriate permissions for all artifacts.</span></span>         |
|<span data-ttu-id="c6578-124">*การฝังสำหรับลูกค้าของคุณ*</span><span class="sxs-lookup"><span data-stu-id="c6578-124">*Embedding for your customers*</span></span>     |<span data-ttu-id="c6578-125">แอปเป็นเจ้าของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c6578-125">App owns data</span></span>         |<span data-ttu-id="c6578-126">โทเค็นการเข้าถึงสำหรับผู้ใช้ที่ไม่ได้ใช้งาน Power BI</span><span class="sxs-lookup"><span data-stu-id="c6578-126">Access token for non-Power BI users</span></span>         |<span data-ttu-id="c6578-127">ต้องมีสิทธิ์สำหรับทั้งรายงานและชุดข้อมูลที่ผูกไว้แบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="c6578-127">Must include permissions for both the report and the dynamically bound dataset.</span></span> <span data-ttu-id="c6578-128">ใช้ [API เพื่อสร้างโทเค็นการฝังสำหรับหลายรายการ](/rest/api/power-bi/embedtoken/generatetoken) เพื่อสร้างโทเค็นการฝังที่สนับสนุนหลายอาติเฟค</span><span class="sxs-lookup"><span data-stu-id="c6578-128">Use the [API for generating an embed token for multiple items](/rest/api/power-bi/embedtoken/generatetoken), to generate an embed token that supports multiple artifacts.</span></span>         |

## <a name="adjusting-the-config-object"></a><span data-ttu-id="c6578-129">ปรับเปลี่ยนออบเจ็กต์การกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="c6578-129">Adjusting the config object</span></span>
<span data-ttu-id="c6578-130">เพิ่ม `datasetBinding` ไปยังออบเจ็กต์การกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="c6578-130">Add `datasetBinding` to the config object.</span></span> <span data-ttu-id="c6578-131">ใช้ตัวอย่างด้านล่างเป็นข้อมูลอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="c6578-131">Use the example below as a reference.</span></span>

```javascript
var config = {
    type: 'report',
    tokenType: models.TokenType.Embed,
    accessToken: accessToken,
    embedUrl: embedUrl,
    id: "reportId", // The wanted report id
    permissions: permissions,

    // -----  Adjustment required for dynamic binding ---- //
    datasetBinding: {
        datasetId: "notOriginalDatasetId",  // </The wanted dataset id
    }
    // ---- End of dynamic binding adjustment ---- //
};

// Get a reference to the embedded report HTML element
var embedContainer = $('#embedContainer')[0];

// Embed the report and display it within the div container
var report = powerbi.embed(embedContainer, config);
```

## <a name="next-steps"></a><span data-ttu-id="c6578-132">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c6578-132">Next steps</span></span>

<span data-ttu-id="c6578-133">หากคุณไม่คุ้นเคยกับการฝังใน Power BI ให้อ่านบทช่วยสอนเหล่านี้เพื่อเรียนรู้วิธีการฝังเนื้อหา Power BI ของคุณ:</span><span class="sxs-lookup"><span data-stu-id="c6578-133">If you're new to embedding in Power BI, review these tutorials to learn how to embed your Power BI content:</span></span>
* [<span data-ttu-id="c6578-134">บทช่วยสอน: เนื้อหา Power BI ที่ฝังลงในแอปพลิเคชันสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="c6578-134">Tutorial: Embed Power BI content into an application for your customers</span></span>](embed-sample-for-customers.md)
* [<span data-ttu-id="c6578-135">บทช่วยสอน: ฝังเนื้อหา Power BI ลงในแอปพลิเคชันสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="c6578-135">Tutorial: Embed Power BI content into an application for your organization</span></span>](embed-sample-for-your-organization.md)