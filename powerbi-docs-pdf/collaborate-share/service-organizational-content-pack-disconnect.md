---
title: ตัดการเชื่อมต่อจากชุดเนื้อหาขององค์กร - Power BI
description: อ่านเกี่ยวกับการลบการเชื่อมต่อกับชุดเนื้อหาขององค์กรโดยการลบชุดข้อมูลใน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: lukaszp
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 08/02/2018
LocalizationGroup: Share your work
ms.openlocfilehash: 5cd1ebd1502241cf07e7de8cff5f0eb769a1b59f
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96406422"
---
# <a name="remove-your-connection-to-a-power-bi-organizational-content-pack"></a><span data-ttu-id="14358-103">ลบการเชื่อมต่อของคุณกับชุดเนื้อหา Power BI ขององค์กร</span><span class="sxs-lookup"><span data-stu-id="14358-103">Remove your connection to a Power BI organizational content pack</span></span>

> [!NOTE]
> <span data-ttu-id="14358-104">คุณไม่สามารถสร้างชุดเนื้อหาขององค์กร หรือติดตั้งชุดเนื้อหาดังกล่าวในประสบการณ์ในพื้นที่ทำงานใหม่</span><span class="sxs-lookup"><span data-stu-id="14358-104">You can't create organizational content packs or install them in the new workspace experiences.</span></span> <span data-ttu-id="14358-105">ตอนนี้ คือเวลาดีที่จะอัปเกรดชุดเนื้อหาของคุณไปยังแอป ถ้าคุณยังไม่ได้เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="14358-105">Now is a good time to upgrade your content packs to apps, if you haven't started yet.</span></span> <span data-ttu-id="14358-106">เรียนรู้[เพิ่มเติมเกี่ยวกับการใช้งานพื้นที่ทำงานใหม่](service-create-the-new-workspaces.md)</span><span class="sxs-lookup"><span data-stu-id="14358-106">Learn [more about the new workspace experience](service-create-the-new-workspaces.md).</span></span>
> 

<span data-ttu-id="14358-107">เพื่อนร่วมงานสร้างชุดเนื้อหาหนึ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="14358-107">A coworker created a content pack.</span></span> <span data-ttu-id="14358-108">คุณพบชุดเนื้อหานั้นใน AppSource และเพิ่มลงในพื้นที่ทำงาน Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="14358-108">You discovered it in AppSource and added it to your Power BI workspace.</span></span> <span data-ttu-id="14358-109">ตอนนี้คุณไม่ต้องการชุดเนื้อหานั้นอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="14358-109">Now you don't need it any longer.</span></span>  <span data-ttu-id="14358-110">คุณจะลบชุดเนื้อหานั้นได้อย่างไร?</span><span class="sxs-lookup"><span data-stu-id="14358-110">How do you remove it?</span></span>

<span data-ttu-id="14358-111">ในการลบชุดเนื้อหาหนึ่ง คุณจะลบชุดข้อมูลของชุดเนื้อหานั้น</span><span class="sxs-lookup"><span data-stu-id="14358-111">To remove a content pack, you remove its dataset.</span></span>  

* <span data-ttu-id="14358-112">ในบานหน้าต่างนำทาง ให้เลือกจุดไข่ปลาทางด้านขวาของชุดข้อมูล แล้วเลือก **ลบ\>ใช่**</span><span class="sxs-lookup"><span data-stu-id="14358-112">In the nav pane, select the ellipsis to the right of the dataset and select **Remove \> Yes**.</span></span>  
  
  ![ลบชุดเนื้อหา](media/service-organizational-content-pack-disconnect/power-bi-remove-organizational-content-pack-dataset.png)

<span data-ttu-id="14358-114">นอกจากนี้ การลบชุดข้อมูลยังเป็นการลบรายงานและแดชบอร์ดทั้งหมดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="14358-114">Removing the dataset also removes all associated reports and dashboards.</span></span> <span data-ttu-id="14358-115">อย่างไรก็ตาม การลบการเชื่อมต่อชุดเนื้อหานี้ไม่ได้ลบชุดเนื้อหาจาก AppSource ขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="14358-115">However, removing your connection to the content pack doesn't delete the content pack from your organization's AppSource.</span></span>  <span data-ttu-id="14358-116">คุณสามารถกลับไปยัง AppSource และเพิ่มชุดเนื้อหานี้กลับไปยังพื้นที่ทำงานของคุณได้เสมอ</span><span class="sxs-lookup"><span data-stu-id="14358-116">You can always return to AppSource and add the content pack back to your workspace.</span></span> <span data-ttu-id="14358-117">คุณสามารถ[ลบชุดเนื้อหาจาก AppSource](service-organizational-content-pack-manage-update-delete.md)ได้ ถ้าคุณเป็นผู้สร้างชุดเนื้อหานั้น</span><span class="sxs-lookup"><span data-stu-id="14358-117">You can only [delete a content pack from AppSource](service-organizational-content-pack-manage-update-delete.md) if you're the one who created it.</span></span>

## <a name="next-steps"></a><span data-ttu-id="14358-118">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="14358-118">Next steps</span></span>
* [<span data-ttu-id="14358-119">บทนำเกี่ยวกับชุดเนื้อหาองค์กร</span><span class="sxs-lookup"><span data-stu-id="14358-119">Introduction to organizational content packs</span></span>](service-organizational-content-pack-introduction.md) 
* [<span data-ttu-id="14358-120">สร้างและกระจายแอปฯใน Power BI</span><span class="sxs-lookup"><span data-stu-id="14358-120">Create and distribute an app in Power BI</span></span>](service-create-distribute-apps.md) 
* [<span data-ttu-id="14358-121">แนวคิดพื้นฐานสำหรับนักออกแบบในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="14358-121">Basic concepts for designers in the Power BI service</span></span>](../fundamentals/service-basic-concepts.md)  
* <span data-ttu-id="14358-122">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="14358-122">More questions?</span></span> [<span data-ttu-id="14358-123">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="14358-123">Try the Power BI Community</span></span>](https://community.powerbi.com/)
