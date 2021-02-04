---
title: สร้างสำเนาของแดชบอร์ด Power BI
description: 'วิธีการทำซ้ำแดชบอร์ด Power BI '
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 03/02/2018
LocalizationGroup: Dashboards
ms.openlocfilehash: 8d687aa29f45ebf9b37187ae8296f5f931d3b63e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96417393"
---
# <a name="create-a-copy-of-a-dashboard-in-power-bi-service"></a><span data-ttu-id="cff8a-103">สร้างมุมมองโทรศัพท์สำหรับแดชบอร์ดใน Power BI</span><span class="sxs-lookup"><span data-stu-id="cff8a-103">Create a copy of a dashboard in Power BI service</span></span>
![แดชบอร์ด](media/service-dashboard-copy/power-bi-dashboard.png)

 <span data-ttu-id="cff8a-105">มีเหตุผลมากมายว่าทำไมต้องคำสำเนาแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="cff8a-105">There are many different reasons to make a copy of a dashboard.</span></span> <span data-ttu-id="cff8a-106">คุณอาจต้องการทำการเปลี่ยนแปลง และทดสอบของประสิทธิภาพการทำงานกับต้นฉบับ หรือสร้างเวอร์ชันที่ต่างกันเล็กน้อยเพื่อกระจาย ให้ผู้ร่วมงาน ภูมิภาค หรือทีม</span><span class="sxs-lookup"><span data-stu-id="cff8a-106">Maybe you want to make changes and test its performance against the original; or create slightly different versions to distribute by colleague, region, or team.</span></span> <span data-ttu-id="cff8a-107">บางครั้งเพื่อนร่วมงานชื่นชอบการออกแบบแดชบอร์ดของคุณ และต้องการใช้สำหรับรายงานเพื่อเสนอผู้จัดการของตน</span><span class="sxs-lookup"><span data-stu-id="cff8a-107">Perhaps a colleague admires your dashboard design and wants to use it for reporting out to their managers.</span></span> <span data-ttu-id="cff8a-108">อาจะมีอีกเหตุผลหนึ่งถ้าคุณมีฐานข้อมูลใหม่ว่ามีโครงสร้างข้อมูลเดียวกันกับชนิดข้อมูลและต้องการใช้แดชบอร์ดที่คุณเคยสร้างอีกครั้ง ซึ่งสามารถทำได้เช่นกัน แต่อาจจำเป็นต้องทำงานบางอย่างใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="cff8a-108">Another reason would be if you have a new database with the same data structure and data types and want to reuse the dashboard you've already created -- this too can be done but would require some work in Power BI Desktop.</span></span> 

<span data-ttu-id="cff8a-109">แดชบอร์ดที่ถูกสร้าง(และถูกคัดลอก)โดยใช้ Power BI service และสามารถดูได้ในอุปกรณ์เคลื่อนที่ Power BI และ Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="cff8a-109">Dashboards are created (and copied) using Power BI service and can be viewed in Power BI mobile and Power BI Embedded.</span></span>  <span data-ttu-id="cff8a-110">แดชบอร์ดใช้งานใน Power BI Desktop ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="cff8a-110">Dashboards are not available in Power BI Desktop.</span></span> 

<span data-ttu-id="cff8a-111">เพื่อทำสำเนาของแดชบอร์ด คุณต้องเป็น *ผู้สร้าง* แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="cff8a-111">To make a copy of a dashboard, you must be the dashboard *creator*.</span></span> <span data-ttu-id="cff8a-112">แดชบอร์ดที่มีการแชร์กับคุณเป็นแอปไม่สามารถซ้ำกันได้</span><span class="sxs-lookup"><span data-stu-id="cff8a-112">Dashboards that have been shared with you as an app cannot be duplicated.</span></span>

1. <span data-ttu-id="cff8a-113">เปิดแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="cff8a-113">Open the dashboard.</span></span>
2. <span data-ttu-id="cff8a-114">ที่มุมบนขวา ให้เลือก **ตัวเลือกเพิ่มเติม** (...) แล้วเลือก **ทำสำเนาแดชบอร์ด**</span><span class="sxs-lookup"><span data-stu-id="cff8a-114">From the top-right corner, select **More options** (...) and choose **Duplicate dashboard**.</span></span>
   
   ![เมนูจุดไข่ปลา](media/service-dashboard-copy/power-bi-dulicate.png)
3. <span data-ttu-id="cff8a-116">ตั้งชื่อแดชบอร์ดแล้วเลือก **ทำสำเนา**</span><span class="sxs-lookup"><span data-stu-id="cff8a-116">Give the dashboard a name and select **Duplicate**.</span></span> 
   
   ![กล่องโต้ตอบทำซ้ำแดชบอร์ด](media/service-dashboard-copy/power-bi-name.png)
4. <span data-ttu-id="cff8a-118">แดชบอร์ดใหม่จะถูกบันทึกในพื้นที่ทำงานเดียวกันเป็นต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="cff8a-118">The new dashboard is saved in the same workspace as the original.</span></span> 
   
   ![แถบแดชบอร์ด](media/service-dashboard-copy/power-bi-copied.png)

5.    <span data-ttu-id="cff8a-120">เปิดแดชบอร์ดใหม่ละแก้ไขตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="cff8a-120">Open the new dashboard and edit as needed.</span></span> <span data-ttu-id="cff8a-121">นี่คือบางสิ่งที่คุณอาจต้องการทำต่อไป</span><span class="sxs-lookup"><span data-stu-id="cff8a-121">Here are some things you might want to do next:</span></span>    
    <span data-ttu-id="cff8a-122">ก.</span><span class="sxs-lookup"><span data-stu-id="cff8a-122">a.</span></span> <span data-ttu-id="cff8a-123">[ย้าย เปลี่ยนชื่อ ปรับขนาด หรือแม้กั่งลบไทล์](service-dashboard-edit-tile.md)</span><span class="sxs-lookup"><span data-stu-id="cff8a-123">[Move, rename, resize or even delete tiles](service-dashboard-edit-tile.md).</span></span>  
    <span data-ttu-id="cff8a-124">b.</span><span class="sxs-lookup"><span data-stu-id="cff8a-124">b.</span></span> <span data-ttu-id="cff8a-125">แก้ไขรายละเอียดไทล์และไฮเปอร์ลิงก์ โดยเลือก **ตัวเลือกเพิ่มเติม** (...) ของไทล์ แล้วเลือก **แก้ไขรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="cff8a-125">Edit tile details and hyperlinks by selecting the tile **More options** (...) and choosing **Edit details**.</span></span>  
    <span data-ttu-id="cff8a-126">c.</span><span class="sxs-lookup"><span data-stu-id="cff8a-126">c.</span></span> <span data-ttu-id="cff8a-127">[เพิ่มไทล์ใหม่จากแถบเมนูแดชบอร์ด](service-dashboard-add-widget.md) (**เพิ่มไทล์**)</span><span class="sxs-lookup"><span data-stu-id="cff8a-127">[Add new tiles from the dashboard menubar](service-dashboard-add-widget.md) (**Add tile**)</span></span>  
    <span data-ttu-id="cff8a-128">d.</span><span class="sxs-lookup"><span data-stu-id="cff8a-128">d.</span></span> <span data-ttu-id="cff8a-129">ปักหมุดไทล์ใหม่[จาก Q&A](service-dashboard-pin-tile-from-q-and-a.md)หรือ[จากรายงาน](service-dashboard-pin-tile-from-report.md)</span><span class="sxs-lookup"><span data-stu-id="cff8a-129">Pin new tiles [from Q&A](service-dashboard-pin-tile-from-q-and-a.md) or [from reports](service-dashboard-pin-tile-from-report.md).</span></span>  
    <span data-ttu-id="cff8a-130">e.</span><span class="sxs-lookup"><span data-stu-id="cff8a-130">e.</span></span> <span data-ttu-id="cff8a-131">เปลี่ยนชื่อแดชบอร์ด เปิดหรือปิด Q&A และตั้งค่าไทล์โฟลว์จากบานหน้าต่างการตั้งค่าแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="cff8a-131">Rename the dashboard, turn Q&A on or off, and set the tile flow from the dashboard Settings pane.</span></span>  <span data-ttu-id="cff8a-132">(เลือกดรอปดาวน์ **ตัวเลือกเพิ่มเติม** (... ) ของแดชบอร์ด และเลือก **การตั้งค่า**)</span><span class="sxs-lookup"><span data-stu-id="cff8a-132">(select the dashboard **More options** (...) dropdown and choose **Settings**)</span></span>  
    <span data-ttu-id="cff8a-133">f.</span><span class="sxs-lookup"><span data-stu-id="cff8a-133">f.</span></span> <span data-ttu-id="cff8a-134">แชร์แดชบอร์ดของคุณโดยตรงกับเพื่อนร่วมงาน หรือเป็นส่วนหนึ่งของแอป Power BI</span><span class="sxs-lookup"><span data-stu-id="cff8a-134">Share your dashboard directly with colleagues or as part of a Power BI app.</span></span> 


## <a name="next-steps"></a><span data-ttu-id="cff8a-135">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="cff8a-135">Next steps</span></span>
* [<span data-ttu-id="cff8a-136">เคล็ดลับสำหรับการออกแบบแดชบอร์ด ที่ยอดเยี่ยม</span><span class="sxs-lookup"><span data-stu-id="cff8a-136">Tips for designing a great dashboard</span></span>](service-dashboards-design-tips.md) 

<span data-ttu-id="cff8a-137">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="cff8a-137">More questions?</span></span> [<span data-ttu-id="cff8a-138">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="cff8a-138">Try the Power BI Community</span></span>](https://community.powerbi.com/)

