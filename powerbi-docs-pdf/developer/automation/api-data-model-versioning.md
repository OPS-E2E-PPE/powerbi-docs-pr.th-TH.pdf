---
title: การกำหนดรุ่นแบบจำลองข้อมูล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: แบบจำลองข้อมูลที่แสดงโดยบริการ OData เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: 0c645774f7af1a8575ca3c755a74fd65b652031a
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887718"
---
# <a name="data-model-versioning"></a><span data-ttu-id="078b0-104">การกำหนดรุ่นแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="078b0-104">Data Model versioning</span></span>

<span data-ttu-id="078b0-105">แบบจำลองข้อมูลที่แสดงโดยบริการ OData เช่นแบบจำลองข้อมูล Power BI กำหนดสัญญาระหว่างบริการ OData และไคลเอ็นต์ของ OData</span><span class="sxs-lookup"><span data-stu-id="078b0-105">The Data Model exposed by an OData Service, such as the Power BI data model, defines a contract between the OData service and its clients.</span></span> <span data-ttu-id="078b0-106">บริการที่สามารถให้ขยายแบบจำลองของตนให้อยู่ในระดับที่ไม่ทำลายการคงอยู่ของไคลเอ็นต์</span><span class="sxs-lookup"><span data-stu-id="078b0-106">Services are allowed to extend their model only to the degree that it does not break existing clients.</span></span> <span data-ttu-id="078b0-107">การเปลี่ยนแปลงฉับพลันเช่นเอาคุณสมบัติออก หรือเปลี่ยนชนิดของคุณสมบัติที่มีอยู่จำเป็นต้องมีระบบบริการรุ่นใหม่ที่มีการให้บริการด้วย URL ที่ต่างกันสำหรับแบบจำลองใหม่</span><span class="sxs-lookup"><span data-stu-id="078b0-107">Breaking changes, such as removing properties or changing the type of existing properties, require that a new service version is provided at a different service root URL for the new model.</span></span>  
  
<span data-ttu-id="078b0-108">การเพิ่มรูปแบบข้อมูลดังต่อไปนี้ถือว่าเป็นการกระทำที่ปลอดภัย และไม่จำเป็นต้องมีบริการเพิ่มเติมมาตรวจสอบจุดที่เข้ามาของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="078b0-108">The following Data Model additions are considered safe and do not require services to version their entry point.</span></span>  
  
* <span data-ttu-id="078b0-109">เพิ่มคุณสมบัติที่ไม่มีการตั้งค่าใดๆ หรือเป็นค่าเริ่มต้น ถ้าคุณสมบัติที่เพิ่มเข้ามามีชื่อเดียวกันเป็นคุณสมบัติแบบไดนามิกที่มีอยู่แล้ว คุณสมบัติที่เพิ่มเข้ามาใหม่จะต้องเป็นประเภทเดียวกันกับ (หรือชนิดพื้นฐานเดียวกัน) คุณสมบัติแบบไดนามิกที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="078b0-109">Adding a property that is nullable or has a default value; if it has the same name as an existing dynamic property, it must have the same type (or base type) as the existing dynamic property</span></span>  
* <span data-ttu-id="078b0-110">เพิ่มคุณสมบัตินำทางที่ไม่มีการตั้งค่าใดๆ ถ้าคุณสมบัติที่เพิ่มเข้ามามีชื่อเดียวกันเป็นคุณสมบัตินำทางแบบไดนามิกที่มีอยู่แล้ว คุณสมบัติที่เพิ่มเข้ามาใหม่จะต้องเป็นประเภทเดียวกันกับ (หรือชนิดพื้นฐานเดียวกัน) คุณสมบัตินำทางแบบไดนามิกที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="078b0-110">Adding a navigation property that is nullable or collection-valued; if it has the same name as an existing dynamic navigation property, it must have the same type (or base type) as the existing dynamic navigation property</span></span>  
* <span data-ttu-id="078b0-111">เพิ่มประเภทเอนทิตีใหม่ลงในรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="078b0-111">Adding a new entity type to the model</span></span>  
* <span data-ttu-id="078b0-112">เพิ่มประเภทเอนทิตีซับซ้อนใหม่ลงในรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="078b0-112">Adding a new complex type to the model</span></span>  
* <span data-ttu-id="078b0-113">เพิ่มชุดเอนทิตีใหม่</span><span class="sxs-lookup"><span data-stu-id="078b0-113">Adding a new entity set</span></span>  
* <span data-ttu-id="078b0-114">เพิ่ม singleton ใหม่</span><span class="sxs-lookup"><span data-stu-id="078b0-114">Adding a new singleton</span></span>  
* <span data-ttu-id="078b0-115">เพิ่มการดำเนินการ ฟังก์ชัน การนำเข้าการดำเนินการ หรือนำเข้าฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="078b0-115">Adding an action, a function, an action import, or function import</span></span>
* <span data-ttu-id="078b0-116">เพิ่มพารามิเตอร์ดำเนินการที่ไม่มีการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="078b0-116">Adding an action parameter that is nullable</span></span>  
* <span data-ttu-id="078b0-117">เพิ่มประเภทข้อกำหนดหรือการแจกแจง</span><span class="sxs-lookup"><span data-stu-id="078b0-117">Adding a type definition or enumeration</span></span>  
* <span data-ttu-id="078b0-118">เพิ่มคำอธิบายประกอบใด ๆ ไปยังแบบจำลององค์ประกอบที่ไคลเอ็นต์ไม่จำเป็นต้องเข้าใจ เพื่อให้มีการโต้ตอบกับการบริการอย่างเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="078b0-118">Adding any annotation to a model element that does not need to be understood by the client to interact with the service correctly</span></span>  
  
<span data-ttu-id="078b0-119">ไคลเอ็นต์ \***ควรจะ** _ เตรียมพร้อมสำหรับบริการเพื่อทำการเปลี่ยนแปลงเพิ่มเติมไปยังแบบจำลองของตน</span><span class="sxs-lookup"><span data-stu-id="078b0-119">Clients \***SHOULD** _ be prepared for services to make such incremental changes to their model.</span></span> <span data-ttu-id="078b0-120">โดยเฉพาะอย่างยิ่ง ไคลเอ็นต์ควรเตรียมพร้อมเพื่อรับมือกับประเภทหรือคุณสมบัติที่ไม่ได้ถูกนิยามไว้ในการบริการ</span><span class="sxs-lookup"><span data-stu-id="078b0-120">In particular, clients should be prepared to receive properties and derived types not previously defined by the service.</span></span>  
  
<span data-ttu-id="078b0-121">การบริการ _ *_ไม่ควรจะ_*\* เปลี่ยนแบบจำลองข้อมูลตามความพอใจของผู้ใช้งานที่ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="078b0-121">Services _ *_SHOULD NOT_*\* change their data model depending on the authenticated user.</span></span> <span data-ttu-id="078b0-122">ถ้าตัวแบบจำลองข้อมูลเป็นผู้ใช้หรือกลุ่มผู้ใช้ที่ขึ้นต่อกัน การเปลี่ยนแปลงทั้งหมดจะต้องเป็นไปอย่างปลอดภัยตามที่ได้กำหนดไว้ในส่วนนี้เมื่อมีการเปรียบเทียบระหว่างการใช้งานแบบจำลองอย่างเต็มประสิทธิภาพกับแบบจำลองที่ถูกจำกัดให้ผู้ใช้งานมองเห็นได้อย่างเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="078b0-122">If the data model is user or user group dependent, all changes MUST be safe changes as defined in this section when comparing the full model to the model visible to users with limited authorizations.</span></span>  
  
<span data-ttu-id="078b0-123">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับมาตรฐานแบบจำลองข้อมูล OData ให้ดูที่[OData เวอร์ชัน 4.0 ส่วนที่ 1: Protocol Plus Errata 02](https://docs.oasis-open.org/odata/odata/v4.0/odata-v4.0-part1-protocol.html)</span><span class="sxs-lookup"><span data-stu-id="078b0-123">For more about OData Data Model standards, see [OData Version 4.0 Part 1: Protocol Plus Errata 02](https://docs.oasis-open.org/odata/odata/v4.0/odata-v4.0-part1-protocol.html).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="078b0-124">นอกจากนี้ โปรดดู</span><span class="sxs-lookup"><span data-stu-id="078b0-124">See also</span></span>
[<span data-ttu-id="078b0-125">ภาพรวมของ Power BI REST API</span><span class="sxs-lookup"><span data-stu-id="078b0-125">Overview of Power BI REST API</span></span>](/rest/api/power-bi/)