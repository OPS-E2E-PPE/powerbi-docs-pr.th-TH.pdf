---
title: ดาวน์โหลดรายงานจากบริการของ Power BI ไปยังไฟล์ Power BI Desktop (ตัวอย่าง)
description: ดาวน์โหลดรายงานจากบริการ Power BI ไปยังไฟล์ Power BI Desktop
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 11/14/2020
LocalizationGroup: Reports
ms.openlocfilehash: 1a196d149a6519f9bcad6bd70ef02d62ef16f69b
ms.sourcegitcommit: b472236df99b490db30f0168bd7284ae6e6095fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/16/2020
ms.locfileid: "97600679"
---
# <a name="download-a-report-from-the-power-bi-service-to-power-bi-desktop-preview"></a><span data-ttu-id="ad32c-103">ดาวน์โหลดรายงานจากบริการของ Power BI ไปยังไฟล์ Power BI Desktop (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="ad32c-103">Download a report from the Power BI service to Power BI Desktop (preview)</span></span>
      
<span data-ttu-id="ad32c-104">ใน Power BI Desktop คุณสามารถเผยแพร่รายงาน (ไฟล์ *.pbix*) จากคอมพิวเตอร์ในเครื่องของคุณไปยังบริการของ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="ad32c-104">In Power BI Desktop, you can publish a report (a *.pbix* file) from your local computer to the Power BI service.</span></span> <span data-ttu-id="ad32c-105">รายงาน Power BI สามารถไปยังทิศทางอื่น ๆ ได้เช่นกัน: คุณสามารถดาวน์โหลดรายงานจากบริการของ Power BI ไปยังไฟล์ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ad32c-105">Power BI reports can go the other direction as well: You can download a report from the Power BI service to Power BI Desktop.</span></span> <span data-ttu-id="ad32c-106">ส่วนขยายสำหรับรายงาน Power BI ในกรณีใดก็ตามคือ .pbix</span><span class="sxs-lookup"><span data-stu-id="ad32c-106">The extension for a Power BI report, in either case, is .pbix.</span></span>

<span data-ttu-id="ad32c-107">มีข้อจำกัดบางประการที่ควรคำนึงถึง ซึ่งจะกล่าวถึงในส่วน [ข้อควรพิจารณาและการแก้ไขปัญหา](#considerations-and-troubleshooting) ของบทความนี้</span><span class="sxs-lookup"><span data-stu-id="ad32c-107">There are a few limitations to keep in mind, which are discussed in the [Considerations and troubleshooting](#considerations-and-troubleshooting) section of this article.</span></span>

![รายการแบบเลื่อนลงของไฟล์](media/service-export-to-pbix/power-bi-file-export.png)

## <a name="download-the-report-as-a-pbix-file"></a><span data-ttu-id="ad32c-109">ดาวน์โหลดรายงานเป็นแบบ ไฟล์ .pbix</span><span class="sxs-lookup"><span data-stu-id="ad32c-109">Download the report as a .pbix file</span></span>

<span data-ttu-id="ad32c-110">คุณสามารถดาวน์โหลดได้เฉพาะรายงาน [ที่สร้างขึ้นด้วย Power BI Desktop ](/learn/modules/publish-share-power-bi/2-publish-reports) หลังจากวันที่ 23 พฤศจิกายน 2016 และได้รับการปรับปรุงนับตั้งแต่จากนั้น</span><span class="sxs-lookup"><span data-stu-id="ad32c-110">You can only download reports [created with Power BI Desktop](/learn/modules/publish-share-power-bi/2-publish-reports) after November 23, 2016, and updated since then.</span></span> <span data-ttu-id="ad32c-111">ถ้ามีการสร้างก่อน ตัวเลือกเมนู **ดาวน์โหลดรายงาน** ในบริการของ Power BI จะเป็นสีเทา</span><span class="sxs-lookup"><span data-stu-id="ad32c-111">If it was created before then, the **Download report** menu option in the Power BI service is grayed out.</span></span>

<span data-ttu-id="ad32c-112">การดาวน์โหลดไฟล์ .pbix ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="ad32c-112">To download the .pbix file, follow these steps:</span></span>

1. <span data-ttu-id="ad32c-113">ในบริการของ Power BI เปิดรายงานที่คุณต้องการดาวน์โหลดใน[มุมมองการแก้ไข](./service-interact-with-a-report-in-editing-view.md)</span><span class="sxs-lookup"><span data-stu-id="ad32c-113">In the Power BI service, open the report you want to download in [Editing view](./service-interact-with-a-report-in-editing-view.md).</span></span>

2. <span data-ttu-id="ad32c-114">จากบานหน้าต่างนำทางด้านบน ให้เลือก **ไฟล์ > ดาวน์โหลดรายงาน**</span><span class="sxs-lookup"><span data-stu-id="ad32c-114">From the top nav pane, select **File > Download report**.</span></span>
   
3. <span data-ttu-id="ad32c-115">ในขณะที่กำลังดาวน์โหลดรายงาน แบนเนอร์สถานะจะแสดงความคืบหน้า</span><span class="sxs-lookup"><span data-stu-id="ad32c-115">While the report is downloading, a status banner displays the progress.</span></span> <span data-ttu-id="ad32c-116">เมื่อไฟล์พร้อม คุณจะถูกขอให้เปิดหรือบันทึกไฟล์ .pbix</span><span class="sxs-lookup"><span data-stu-id="ad32c-116">When the file is ready, you're asked where to save the .pbix file.</span></span> <span data-ttu-id="ad32c-117">ชื่อค่าเริ่มต้นของไฟล์ตรงกับชื่อเรื่องของรายงาน</span><span class="sxs-lookup"><span data-stu-id="ad32c-117">The default name of the file matches the title of the report.</span></span>
   
4. <span data-ttu-id="ad32c-118">ถ้าคุณไม่พร้อม [ติดตั้ง Power BI Desktop ](../fundamentals/desktop-get-the-desktop.md) จากนั้นให้เปิดไฟล์ .pbix ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ad32c-118">If you haven't already, [install Power BI Desktop](../fundamentals/desktop-get-the-desktop.md), then open the .pbix file in Power BI Desktop.</span></span>
   
    <span data-ttu-id="ad32c-119">เมื่อคุณเปิดรายงานใน Power BI Desktop คุณอาจเห็นข้อความแจ้งเตือนให้คุณทราบว่าบางคุณลักษณะที่พร้อมใช้งานในรายงานการบริการของ Power BI อาจไม่พร้อมใช้งานใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ad32c-119">When you open the report in Power BI Desktop, you may see a warning message letting you know that some features available in the Power BI service report aren't available in Power BI Desktop.</span></span>
   
    ![กล่องโต้ตอบคำเตือน](media/service-export-to-pbix/power-bi-export-to-pbix_2.png)

5. <span data-ttu-id="ad32c-121">ตัวแก้ไขรายงานใน Power BI Desktop จะคล้ายคลึงกันตัวแก้ไขรายงานในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="ad32c-121">The report editor in Power BI Desktop is similar to the report editor in the Power BI service.</span></span>  
   
    ![ตัวแก้ไขรายงาน Power BI Desktop](media/service-export-to-pbix/power-bi-desktop.png)

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="ad32c-123">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="ad32c-123">Considerations and troubleshooting</span></span>

<span data-ttu-id="ad32c-124">มีข้อควรพิจารณาและขีดจำกัดที่สำคัญสองสามข้อที่เชื่อมโยงกับการดาวน์โหลดไฟล์ .pbix จากบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="ad32c-124">There are a few important considerations and limitations associated with downloading a .pbix file from the Power BI service.</span></span>

* <span data-ttu-id="ad32c-125">เมื่อต้องการดาวน์โหลดไฟล์ คุณต้องแก้ไขการเข้าถึงในรายงาน</span><span class="sxs-lookup"><span data-stu-id="ad32c-125">To download the file, you must have edit access to the report.</span></span>
* <span data-ttu-id="ad32c-126">ต้องมีการสร้างรายงานโดยใช้ Power BI Desktop และ *เผยแพร่* ไปยังบริการของ Power BI หรือไฟล์ .pbix ต้องได้รับ *การอัปโหลด* ไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="ad32c-126">The report must have been created by using Power BI Desktop and *published* to the Power BI service, or the .pbix file must have been *uploaded* to the Power BI service.</span></span>
* <span data-ttu-id="ad32c-127">ต้องมีการเผยแพร่หรืออัปเดตรายงานหลังจากวันที่ 23 พฤศจิกายน 2016</span><span class="sxs-lookup"><span data-stu-id="ad32c-127">Reports must be published or updated after November 23, 2016.</span></span> <span data-ttu-id="ad32c-128">รายงานที่เผยแพร่ก่อนหน้านี้ยังไม่สามารถดาวน์โหลดได้</span><span class="sxs-lookup"><span data-stu-id="ad32c-128">Reports published earlier aren't downloadable.</span></span>
* <span data-ttu-id="ad32c-129">คุณลักษณะนี้จะไม่สามารถใช้งานได้กับรายงานและชุดเนื้อหาที่สร้างขึ้นในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="ad32c-129">This feature won't work with reports and content packs originally created in the Power BI service.</span></span>
* <span data-ttu-id="ad32c-130">ใช้เวอร์ชันล่าสุดของ Power BI Desktop เสมอเมื่อเปิดไฟล์ที่ดาวน์โหลดแล้ว</span><span class="sxs-lookup"><span data-stu-id="ad32c-130">Always use the latest version of Power BI Desktop when you open downloaded files.</span></span> <span data-ttu-id="ad32c-131">ไฟล์ .pbix ที่ดาวน์โหลดแล้วอาจไม่สามารถเปิดได้ในเวอร์ชันที่ไม่ใช่เวอร์ชั่นปัจจุบันของ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ad32c-131">Downloaded .pbix files might not open in non-current versions of Power BI Desktop.</span></span> <span data-ttu-id="ad32c-132">ตัวอย่างเช่น คุณไม่สามารถเปิดไฟล์ .pbix ที่ดาวน์โหลดโดยใช้เวอร์ชันเดสก์ท็อปที่ไม่รองรับการป้องกันข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="ad32c-132">For example, you cannot open downloaded .pbix files using a Desktop version that does not support information protection.</span></span>
* <span data-ttu-id="ad32c-133">หากผู้ดูแลระบบของคุณปิดใช้งานความสามารถในการดาวน์โหลดข้อมูล คุณลักษณะนี้จะไม่ปรากฏในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="ad32c-133">If your administrator has turned off the ability to download data, this feature won't be visible in the Power BI service.</span></span>
* <span data-ttu-id="ad32c-134">ชุดข้อมูลที่มีการรีเฟรชแบบเพิ่มทีละหน่วยไม่สามารถดาวน์โหลดเป็นไฟล์ .pbix ได้</span><span class="sxs-lookup"><span data-stu-id="ad32c-134">Datasets with incremental refresh can't be downloaded to a .pbix file.</span></span>
* <span data-ttu-id="ad32c-135">ไม่สามารถดาวน์โหลดชุดข้อมูลที่เปิดใช้งานสำหรับ[แบบจำลองขนาดใหญ่](../admin/service-premium-large-models.md)ไปยังแฟ้ม .pbix ได้</span><span class="sxs-lookup"><span data-stu-id="ad32c-135">Datasets enabled for [large models](../admin/service-premium-large-models.md) can't be downloaded to a .pbix file.</span></span>
* <span data-ttu-id="ad32c-136">ไม่สามารถดาวน์โหลดชุดข้อมูลที่ปรับแก้โดยใช้[จุดสิ้นสุด XMLA](../admin/service-premium-connect-tools.md)ไปยังแฟ้ม .pbix ได้</span><span class="sxs-lookup"><span data-stu-id="ad32c-136">Datasets modified by using the [XMLA endpoint](../admin/service-premium-connect-tools.md) can't be downloaded to a .pbix file.</span></span>
* <span data-ttu-id="ad32c-137">หากคุณสร้างรายงาน Power BI โดยยึดตามชุดข้อมูลในพื้นที่ทำงานหนึ่งและเผยแพร่ไปยังพื้นที่ทำงานอื่น คุณและผู้ใช้ของคุณจะไม่สามารถดาวน์โหลดรายงานได้</span><span class="sxs-lookup"><span data-stu-id="ad32c-137">If you create a Power BI report based on a dataset in one workspace and publish to a different workspace, you and your users won't be able to download it.</span></span> <span data-ttu-id="ad32c-138">ในขณะนี้ คุณลักษณะการดาวน์โหลดไม่ได้รับการสนับสนุนในสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="ad32c-138">The download feature is currently not supported in this scenario.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ad32c-139">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="ad32c-139">Next steps</span></span>

<span data-ttu-id="ad32c-140">ดูวิดีโอความยาวหนึ่งนาที **Guy in a Cube** สำหรับคุณลักษณะนี้:</span><span class="sxs-lookup"><span data-stu-id="ad32c-140">View the **Guy in a Cube** one-minute video about this feature:</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/ymWqU5jiUl0" frameborder="0" allowfullscreen></iframe>

<span data-ttu-id="ad32c-141">ต่อไปนี้คือบทความเพิ่มเติมที่สามารถช่วยให้คุณเรียนรู้วิธีการใช้บริการของ Power BI:</span><span class="sxs-lookup"><span data-stu-id="ad32c-141">Here are some additional articles that can help you learn to use the Power BI service:</span></span>

* [<span data-ttu-id="ad32c-142">รายงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="ad32c-142">Reports in Power BI</span></span>](../consumer/end-user-reports.md)
* [<span data-ttu-id="ad32c-143">แนวคิดพื้นฐานสำหรับนักออกแบบในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="ad32c-143">Basic concepts for designers in the Power BI service</span></span>](../fundamentals/service-basic-concepts.md)

<span data-ttu-id="ad32c-144">เมื่อคุณได้ติดตั้ง Power BI Desktop แล้ว บทความต่อไปนี้สามารถช่วยให้คุณเริ่มต้น และใช้งานอย่างรวดเร็ว:</span><span class="sxs-lookup"><span data-stu-id="ad32c-144">After you've installed Power BI Desktop, see the following article to help you get up and running quickly:</span></span>

* [<span data-ttu-id="ad32c-145">เริ่มต้นใช้งาน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ad32c-145">Getting Started with Power BI Desktop</span></span>](../fundamentals/desktop-getting-started.md)

<span data-ttu-id="ad32c-146">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="ad32c-146">More questions?</span></span> <span data-ttu-id="ad32c-147">[ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="ad32c-147">[Try the Power BI Community](https://community.powerbi.com/).</span></span>