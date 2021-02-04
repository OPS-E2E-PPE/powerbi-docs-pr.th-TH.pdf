---
title: คำแนะนำการใช้รูปภาพสำหรับรายงานที่มีการแบ่งหน้า
description: คำแนะนำสำหรับการใช้รูปภาพในรายงานที่มีการแบ่งหน้าใน Power BI
author: peter-myers
ms.author: v-pemyer
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 02/16/2020
ms.openlocfilehash: ccb61899337e5585d03d9297fbe8f8a5decc612e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418405"
---
# <a name="image-use-guidance-for-paginated-reports"></a><span data-ttu-id="0181e-103">คำแนะนำการใช้รูปภาพสำหรับรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="0181e-103">Image use guidance for paginated reports</span></span>

<span data-ttu-id="0181e-104">บทความนี้มุ่งไปที่คุณเช่นเดียวกับผู้เขียนรายงานที่ออกแบบ Power BI [รายงานที่มีเลขหน้า](../paginated-reports/paginated-reports-report-builder-power-bi.md).</span><span class="sxs-lookup"><span data-stu-id="0181e-104">This article targets you as a report author designing Power BI [paginated reports](../paginated-reports/paginated-reports-report-builder-power-bi.md).</span></span> <span data-ttu-id="0181e-105">โดยให้คำแนะนำเกี่ยวกับการทำงานกับรูปภาพต่างๆ</span><span class="sxs-lookup"><span data-stu-id="0181e-105">It provides suggestions when working with images.</span></span> <span data-ttu-id="0181e-106">โดยทั่วไป รูปภาพในเค้าโครงรายงานจะสามารถแสดงผลเป็นภาพกราฟิก เช่น โลโก้บริษัท หรือรูปภาพต่างๆ ได้</span><span class="sxs-lookup"><span data-stu-id="0181e-106">Commonly, images in report layouts can display a graphic like a company logo, or pictures.</span></span>

<span data-ttu-id="0181e-107">การจัดเก็บรูปภาพสามารถทำได้ในตำแหน่งที่ตั้งที่แตกต่างกันสามแห่ง:</span><span class="sxs-lookup"><span data-stu-id="0181e-107">Images can be stored in three different locations:</span></span>

- <span data-ttu-id="0181e-108">ภายในรายงาน (ฝังตัว)</span><span class="sxs-lookup"><span data-stu-id="0181e-108">Within the report (embedded)</span></span>
- <span data-ttu-id="0181e-109">บนเว็บเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="0181e-109">On a web server</span></span>
- <span data-ttu-id="0181e-110">ในฐานข้อมูล ซึ่งสามารถเรียกดูจากชุดข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="0181e-110">In a database, which can be retrieved by a dataset</span></span>

<span data-ttu-id="0181e-111">จากนั้น จะสามารถใช้รูปภาพดังกล่าวในสถานการณ์ต่างๆ ที่หลากหลาย ในเค้าโครงรายงานของคุณ:</span><span class="sxs-lookup"><span data-stu-id="0181e-111">They can then be used in a variety of scenarios in your report layouts:</span></span>

- <span data-ttu-id="0181e-112">โลโก้หรือรูปภาพเดี่ยว</span><span class="sxs-lookup"><span data-stu-id="0181e-112">Free-standing logo, or picture</span></span>
- <span data-ttu-id="0181e-113">รูปภาพที่เกี่ยวกับแถวของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0181e-113">Pictures associated with rows of data</span></span>
- <span data-ttu-id="0181e-114">ภาพพื้นหลังสำหรับรายการบางอย่างในรายงาน:</span><span class="sxs-lookup"><span data-stu-id="0181e-114">Background for certain report items:</span></span>
  - <span data-ttu-id="0181e-115">เนื้อความรายงาน</span><span class="sxs-lookup"><span data-stu-id="0181e-115">Report body</span></span>
  - <span data-ttu-id="0181e-116">กล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="0181e-116">Textbox</span></span>
  - <span data-ttu-id="0181e-117">สี่เหลี่ยมผืนผ้า</span><span class="sxs-lookup"><span data-stu-id="0181e-117">Rectangle</span></span>
  - <span data-ttu-id="0181e-118">ขอบเขตข้อมูล Tablix (ตาราง เมทริกซ์ หรือรายการ)</span><span class="sxs-lookup"><span data-stu-id="0181e-118">Tablix data region (table, matrix, or list)</span></span>

## <a name="suggestions"></a><span data-ttu-id="0181e-119">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="0181e-119">Suggestions</span></span>

<span data-ttu-id="0181e-120">ลองพิจารณาคำแนะนำต่อไปนี้สำหรับส่งมอบเค้าโครงรายงานแบบมืออาชีพ โดยบำรุงรักษาได้ง่าย และมอบประสิทธิภาพรายงานที่ดีที่สุด:</span><span class="sxs-lookup"><span data-stu-id="0181e-120">Consider the following suggestions to deliver professional report layouts, ease of maintenance, and optimized report performance:</span></span>

- <span data-ttu-id="0181e-121">**ใช้ขนาดเล็กที่สุดเท่าที่จะเป็นไปได้**: เราแนะนำให้คุณจัดเตรียมรูปภาพที่มีขนาดเล็ก แต่ยังคงมีความคมชัด และชัดเจน</span><span class="sxs-lookup"><span data-stu-id="0181e-121">**Use smallest possible size**: We recommend you prepare images that are small in size, yet still look sharp, and crisp.</span></span> <span data-ttu-id="0181e-122">ทั้งหมดนี้เกี่ยวกับความสมดุลระหว่างคุณภาพและขนาด</span><span class="sxs-lookup"><span data-stu-id="0181e-122">It's all about a balance between quality and size.</span></span> <span data-ttu-id="0181e-123">ลองพิจารณาใช้โปรแกรมแก้ไขภาพกราฟิก (เช่น MS Paint) เพื่อลดขนาดไฟล์ภาพ</span><span class="sxs-lookup"><span data-stu-id="0181e-123">Consider using a graphics editor (like MS Paint) to reduce the image file size.</span></span>
- <span data-ttu-id="0181e-124">**หลีกเลี่ยงภาพแบบฝัง**: ขั้นตอนแรก รูปภาพที่ฝังตัวอาจไม่เข้ากับขนาดไฟล์รายงาน ซึ่งอาจทำให้การแสดงผลภาพของรายงานช้าลง</span><span class="sxs-lookup"><span data-stu-id="0181e-124">**Avoid embedded images**: First, embedded images can bloat the report file size, which can contribute to slower report rendering.</span></span> <span data-ttu-id="0181e-125">ขั้นตอนที่สอง รูปภาพที่ฝังตัวอาจสร้างความยุ่งยากในการบำรุงรักษา หากคุณต้องการอัปเดตรูปภาพในรายงานจำนวนมาก (ซึ่งอาจเกิดปัญหาได้ หากโลโก้บริษัทของคุณมีการเปลี่ยนแปลง)</span><span class="sxs-lookup"><span data-stu-id="0181e-125">Second, embedded images can quickly become a maintenance nightmare if you need to update many report images (as might be the case should your company logo change).</span></span>
- <span data-ttu-id="0181e-126">**ใช้พื้นที่เก็บข้อมูลของเว็บเซิร์ฟเวอร์**: การจัดเก็บรูปภาพบนเว็บเซิร์ฟเวอร์เป็นทางเลือกที่ดี โดยเฉพาะอย่างยิ่งสำหรับโลโก้บริษัท ซึ่งอาจมีที่มาจากเว็บไซต์บริษัท</span><span class="sxs-lookup"><span data-stu-id="0181e-126">**Use web server storage**: Storing images on a web server is a good option, especially for the company logo, which may be sourced from the company website.</span></span> <span data-ttu-id="0181e-127">อย่างไรก็ตาม โปรดระมัดระวัง หากผู้ใช้รายงานของคุณจะเข้าถึงรายงานภายนอกเครือข่ายของคุณ</span><span class="sxs-lookup"><span data-stu-id="0181e-127">However, take care if your report users will access reports outside your network.</span></span> <span data-ttu-id="0181e-128">ในกรณีนี้ โปรดแน่ใจว่ารูปภาพจะพร้อมใช้งานผ่านทางอินเทอร์เน็ต</span><span class="sxs-lookup"><span data-stu-id="0181e-128">In this case, be sure that the images are available over the Internet.</span></span>

    <span data-ttu-id="0181e-129">เมื่อรูปภาพมีความเกี่ยวข้องกับข้อมูลของคุณ (เช่น รูปภาพของพนักงานขาย) โปรดตั้งชื่อไฟล์ภาพ เพื่อให้นิพจน์รายงานสามารถสร้างเส้นทาง URL รูปภาพได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="0181e-129">When images relate to your data (like pictures of your salespeople), name image files so a report expression can dynamically produce the image URL path.</span></span> <span data-ttu-id="0181e-130">ตัวอย่างเช่น คุณอาจตั้งชื่อรูปภาพพนักงานขายโดยใช้หมายเลขพนักงานของพนักงานขายแต่ละคนได้</span><span class="sxs-lookup"><span data-stu-id="0181e-130">For example, you could name the salespeople pictures using each salesperson's employee number.</span></span> <span data-ttu-id="0181e-131">หากชุดข้อมูลรายงาน เรียกดูหมายเลขพนักงาน คุณจะสามารถเขียนนิพจน์สำหรับสร้างเส้นทาง URL รูปภาพแบบเต็มได้</span><span class="sxs-lookup"><span data-stu-id="0181e-131">Providing the report dataset retrieves the employee number, you can write an expression to produce the full image URL path.</span></span>
- <span data-ttu-id="0181e-132">**ใช้พื้นที่เก็บข้อมูลของฐานข้อมูล**: เมื่อฐานข้อมูลเชิงสัมพันธ์จัดเก็บข้อมูลรูปภาพ จะให้ความรู้สึกในการใช้แหล่งข้อมูลรูปภาพโดยตรงจากตารางฐานข้อมูล โดยเฉพาะอย่างยิ่งเมื่อรูปภาพมีขนาดใหญ่เกินไป</span><span class="sxs-lookup"><span data-stu-id="0181e-132">**Use database storage**: When a relational database stores image data, it makes sense to source the image data directly from the database tables—especially when the images are not too large.</span></span>
- <span data-ttu-id="0181e-133">**รูปภาพพื้นหลังที่เหมาะสม**: หากคุณตัดสินใจใช้รูปภาพพื้นหลัง โปรดระมัดระวังอย่าดึงความสนใจของผู้ใช้รายงานไปจากข้อมูลรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="0181e-133">**Appropriate background images**: If you decide to use background images, take care not to distract the report user from your report data.</span></span> 

    <span data-ttu-id="0181e-134">นอกจากนี้ โปรดแน่ใจว่าได้ใช้ _รูปภาพที่มีลายน้ำ_</span><span class="sxs-lookup"><span data-stu-id="0181e-134">Also, be sure to use _watermark styled images_.</span></span> <span data-ttu-id="0181e-135">โดยทั่วไป รูปภาพที่มีลายน้ำจะมีพื้นหลังแบบโปร่งใส (หรือมีสีพื้นหลังเดียวกับที่ใช้ในรายงาน)</span><span class="sxs-lookup"><span data-stu-id="0181e-135">Generally, watermark styled images have a transparent background (or have the same background color used by the report).</span></span> <span data-ttu-id="0181e-136">นอกจากนี้ ยังมีการใช้สีแบบซีดอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="0181e-136">They also use faint colors.</span></span> <span data-ttu-id="0181e-137">ตัวอย่างทั่วไปของรูปภาพที่มีลายน้ำ จะรวมถึงโลโก้บริษัท หรือป้ายที่มีความอ่อนไหว เช่น ”ฉบับร่าง” หรือ ”ข้อมูลลับ“</span><span class="sxs-lookup"><span data-stu-id="0181e-137">Common examples of watermark styled images include the company logo, or sensitivity labels like "Draft" or "Confidential".</span></span>

## <a name="next-steps"></a><span data-ttu-id="0181e-138">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="0181e-138">Next steps</span></span>

<span data-ttu-id="0181e-139">สำหรับข้อมูลเพิ่มเติมที่เกี่ยวข้องกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0181e-139">For more information related to this article, check out the following resources:</span></span>

- [<span data-ttu-id="0181e-140">รายงานแบบแบ่งหน้าใน Power BI Premium คืออะไร</span><span class="sxs-lookup"><span data-stu-id="0181e-140">What are paginated reports in Power BI Premium?</span></span>](../paginated-reports/paginated-reports-report-builder-power-bi.md)
- <span data-ttu-id="0181e-141">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0181e-141">Questions?</span></span> [<span data-ttu-id="0181e-142">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="0181e-142">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="0181e-143">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="0181e-143">Suggestions?</span></span> [<span data-ttu-id="0181e-144">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="0181e-144">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com/)
