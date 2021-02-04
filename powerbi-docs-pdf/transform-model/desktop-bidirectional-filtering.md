---
title: การกรองข้ามแบบสองทิศทางใน Power BI Desktop
description: เปิดใช้งานการกรองข้ามด้วย DirectQuery ใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: conceptual
ms.date: 01/15/2020
LocalizationGroup: Connect to data
ms.openlocfilehash: 96e0e60adcd1858fa031eb81e8f0762690cbe0c7
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415990"
---
# <a name="enable-bidirectional-cross-filtering-for-directquery-in-power-bi-desktop"></a><span data-ttu-id="5e652-103">เปิดใช้การกรองข้ามแบบสองทิศทางสำหรับ DirectQuery ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="5e652-103">Enable bidirectional cross-filtering for DirectQuery in Power BI Desktop</span></span>

<span data-ttu-id="5e652-104">ขณะกรองตารางเพื่อสร้างมุมมองข้อมูลที่เหมาะสม ผู้สร้างรายงานและผู้จัดรูปแบบข้อมูลจะพบกับความท้าทายในการกำหนดวิธีการใช้ตัวกรองต่างๆ กับรายงาน</span><span class="sxs-lookup"><span data-stu-id="5e652-104">When filtering tables to create the appropriate view of data, report creators and data modelers face challenges determining how to apply filters to a report.</span></span> <span data-ttu-id="5e652-105">ก่อนหน้านี้ บริบทของตัวกรองตารางจะขึ้นอยู่กับด้านหนึ่งของความสัมพันธ์ ไม่ใช่อีกด้านหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5e652-105">Previously, the table's filter context was held on one side of the relationship, but not the other.</span></span> <span data-ttu-id="5e652-106">การจัดการนี้มักจะต้องใช้สูตร DAX ที่ซับซ้อนเพื่อให้ได้ผลลัพธ์ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="5e652-106">This arrangement often required complex DAX formula to get the wanted results.</span></span>

<span data-ttu-id="5e652-107">ด้วยการกรองแบบไขว้สองทิศทาง ทำให้ขณะนี้ ผู้สร้างรายงานและผู้จัดรูปแบบข้อมูลสามารถควบคุมลักษณะการใช้ฟิลเตอร์ต่าง ๆ ขณะทำงานกับตารางที่เกี่ยวข้องได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="5e652-107">With bidirectional cross-filtering, report creators and data modelers now have more control over how they can apply filters when working with related tables.</span></span> <span data-ttu-id="5e652-108">การกรองแบบไขว้สองทิศทางจะทำให้พวกเขาสามารถใช้ตัวกรองกับความสัมพันธ์ของตารางได้ทั้ง *สอง* ด้าน</span><span class="sxs-lookup"><span data-stu-id="5e652-108">Bidirectional cross-filtering enables them to apply filters on *both* sides of a table relationship.</span></span> <span data-ttu-id="5e652-109">คุณสามารถปรับใช้ตัวกรองต่าง ๆ โดยการเผยแพร่บริบทตัวกรองไปยังตารางที่เกี่ยวข้องลำดับที่สอง ที่อีกด้านหนึ่งของความสัมพันธ์ของตาราง</span><span class="sxs-lookup"><span data-stu-id="5e652-109">You can apply the filters by propagating the filter context to a second related table on the other side of a table relationship.</span></span>

## <a name="enable-bidirectional-cross-filtering-for-directquery"></a><span data-ttu-id="5e652-110">เปิดใช้การกรองแบบไขว้สองทิศทางสำหรับ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="5e652-110">Enable bidirectional cross-filtering for DirectQuery</span></span>

<span data-ttu-id="5e652-111">คุณสามารถเปิดใช้การกรองแบบไขว้ในกล่องโต้ตอบ **แก้ไขความสัมพันธ์**</span><span class="sxs-lookup"><span data-stu-id="5e652-111">You can enable cross-filtering in the **Edit relationship** dialog box.</span></span> <span data-ttu-id="5e652-112">เพื่อเปิดใช้การกรองแบบไขว้สำหรับความสัมพันธ์ คุณจะต้องกำหนดค่าตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5e652-112">To enable cross-filtering for a relationship, you must configure the following options:</span></span>

* <span data-ttu-id="5e652-113">ตั้งค่า **ทิศทางตัวกรองแบบไขว้** เป็น **ทั้งคู่**</span><span class="sxs-lookup"><span data-stu-id="5e652-113">Set **Cross filter direction** to **Both**.</span></span>
* <span data-ttu-id="5e652-114">เลือก **ปรับใช้ตัวกรองด้านความปลอดภัยทั้งสองทิศทาง**</span><span class="sxs-lookup"><span data-stu-id="5e652-114">Select **Apply security filter in both directions**.</span></span>

  ![กำหนดค่าการกรองแบบสองทิศทางใน Power BI Desktop](media/desktop-bidirectional-filtering/bidirectional-filtering_2.png)

> [!NOTE]
> <span data-ttu-id="5e652-116">ขณะสร้างสูตร DAX สำหรับการกรองแบบไขว้ใน Power BI Desktop ให้ใช้ *UserPrincipalName*</span><span class="sxs-lookup"><span data-stu-id="5e652-116">When creating cross filtering DAX formulas in Power BI Desktop, use *UserPrincipalName*.</span></span> <span data-ttu-id="5e652-117">เขตข้อมูลนี้มักจะเป็นข้อมูลเดียวกับการเข้าสู่ระบบของผู้ใช้ ตัวอย่างเช่น <em>joe@contoso.com</em> แทนที่จะเป็น *UserName*</span><span class="sxs-lookup"><span data-stu-id="5e652-117">This field is often the same as a user's login, for example <em>joe@contoso.com</em>, instead of *UserName*.</span></span> <span data-ttu-id="5e652-118">ด้วยเหตุนี้ คุณจึงอาจจำเป็นต้องสร้างตารางที่เกี่ยวข้องที่แมป *UserName* หรือ *EmployeeID* ไปยัง *UserPrincipalName*</span><span class="sxs-lookup"><span data-stu-id="5e652-118">As such, you may need to create a related table that maps *UserName* or *EmployeeID* to *UserPrincipalName*.</span></span>

<span data-ttu-id="5e652-119">สำหรับข้อมูลเพิ่มเติม และตัวอย่างลักษณะการกรองแบบไขว้สองทิศทาง โปรดตรวจสอบ [การกรองไขว้แบบสองทิศทางสำหรับเอกสารทางเทคนิคเกี่ยวกับ Power BI Desktop](https://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx)</span><span class="sxs-lookup"><span data-stu-id="5e652-119">For more information and for examples of how bidirectional cross-filtering works, check out the [Bidirectional cross-filtering for Power BI Desktop whitepaper](https://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx).</span></span>

