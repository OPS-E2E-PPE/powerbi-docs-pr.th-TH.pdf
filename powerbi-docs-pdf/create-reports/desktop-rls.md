---
title: จำกัดการเข้าถึงข้อมูลที่มีการรักษาความปลอดภัยระดับแถว (RLS) สำหรับ Power BI Desktop
description: วิธีการกำหนดค่าความปลอดภัยระดับแถวสำหรับชุดข้อมูลที่นำเข้า และ DirectQuery ภายใน Power BI Desktop
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.custom: ''
ms.date: 01/31/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 0d5501ba8929318081a5db7e34e80722f2ffbf70
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412862"
---
# <a name="restrict-data-access-with-row-level-security-rls-for-power-bi-desktop"></a><span data-ttu-id="1e0c7-103">จำกัดการเข้าถึงข้อมูลที่มีการรักษาความปลอดภัยระดับแถว (RLS) สำหรับ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="1e0c7-103">Restrict data access with row-level security (RLS) for Power BI Desktop</span></span>

<span data-ttu-id="1e0c7-104">คุณสามารถใช้การรักษาความปลอดภัยระดับแถว (RLS) ด้วย Power BI Desktop เพื่อจำกัดการเข้าถึงข้อมูลสำหรับให้ผู้ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="1e0c7-104">You can use row-level security (RLS) with Power BI Desktop to restrict data access for given users.</span></span> <span data-ttu-id="1e0c7-105">ตัวกรองจะจำกัดข้อมูลในระดับแถว</span><span class="sxs-lookup"><span data-stu-id="1e0c7-105">Filters restrict data at the row level.</span></span> <span data-ttu-id="1e0c7-106">คุณสามารถกำหนดตัวกรองภายในบทบาท</span><span class="sxs-lookup"><span data-stu-id="1e0c7-106">You can define filters within roles.</span></span>

<span data-ttu-id="1e0c7-107">ในตอนนี้คุณสามารถกำหนดค่า RLS สำหรับรูปแบบข้อมูลที่นำเข้าลงใน Power BI ด้วย Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="1e0c7-107">You can now configure RLS for data models imported into Power BI with Power BI Desktop.</span></span> <span data-ttu-id="1e0c7-108">คุณยังสามารถกำหนดค่า RLS บนชุดข้อมูลที่กำลังใช้ [DirectQuery](../connect-data/desktop-use-directquery.md) เช่น SQL Server ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="1e0c7-108">You can also configure RLS on datasets that are using [DirectQuery](../connect-data/desktop-use-directquery.md), such as SQL Server.</span></span> <span data-ttu-id="1e0c7-109">ก่อนหน้านี้ คุณสามารถใช้ได้เฉพาะ RLS ภายในแบบจำลองภายในองค์กรของ Analysis Services ภายนอก Power BI เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1e0c7-109">Previously, you were only able to implement RLS within on-premises Analysis Services models outside Power BI.</span></span> <span data-ttu-id="1e0c7-110">ในส่วนการเชื่อมต่อสดของ Analysis Services คุณสามารถกำหนดค่ารักษาความปลอดภัยระดับแถวบนแบบจำลองภายในองค์กรได้</span><span class="sxs-lookup"><span data-stu-id="1e0c7-110">For Analysis Services live connections, you configure Row-level security on the on-premises model.</span></span> <span data-ttu-id="1e0c7-111">ตัวเลือกความปลอดภัยจะไม่แสดงสำหรับชุดข้อมูลที่เชื่อมต่อสด</span><span class="sxs-lookup"><span data-stu-id="1e0c7-111">The security option doesn't show up for live connection datasets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1e0c7-112">ถ้าคุณกำหนดบทบาทและกฎ ภายในบริการของ Power BI คุณจะต้องสร้างบทบาทเหล่านั้นภายใน Power BI Desktop และเผยแพร่รายงานนั้นไปยังบริการ</span><span class="sxs-lookup"><span data-stu-id="1e0c7-112">If you defined roles and rules within the Power BI service, you need to recreate those roles within Power BI Desktop and publish the report to the service.</span></span> <span data-ttu-id="1e0c7-113">เรียนรู้เพิ่มเติมเกี่ยวกับตัวเลือกสำหรับ [RLS ภายในบริการ Power BI](../admin/service-admin-rls.md)</span><span class="sxs-lookup"><span data-stu-id="1e0c7-113">Learn more about options for [RLS within the Power BI service](../admin/service-admin-rls.md).</span></span>

[!INCLUDE [include-short-name](../includes/rls-desktop-define-roles.md)]

[!INCLUDE [include-short-name](../includes/rls-desktop-view-as-roles.md)]

[!INCLUDE [include-short-name](../includes/rls-limitations.md)]

[!INCLUDE [include-short-name](../includes/rls-faq.md)]

## <a name="next-steps"></a><span data-ttu-id="1e0c7-114">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="1e0c7-114">Next steps</span></span>

<span data-ttu-id="1e0c7-115">สำหรับข้อมูลเพิ่มเติมที่เกี่ยวข้องกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1e0c7-115">For more information related to this article, check out the following resources:</span></span>

- [<span data-ttu-id="1e0c7-116">การรักษาความปลอดภัยระดับแถว (RLS) ด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="1e0c7-116">Row-level security (RLS) with Power BI</span></span>](../admin/service-admin-rls.md)
- [<span data-ttu-id="1e0c7-117">คำแนะนำในการรักษาความปลอดภัยระดับแถว (RLS) ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="1e0c7-117">Row-level security (RLS) guidance in Power BI Desktop</span></span>](../guidance/rls-guidance.md)
- <span data-ttu-id="1e0c7-118">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="1e0c7-118">Questions?</span></span> [<span data-ttu-id="1e0c7-119">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="1e0c7-119">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="1e0c7-120">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="1e0c7-120">Suggestions?</span></span> [<span data-ttu-id="1e0c7-121">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="1e0c7-121">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com/)
