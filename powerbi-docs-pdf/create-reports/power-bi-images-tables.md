---
title: แสดงรูปภาพต่าง ๆ ในตารางหรือเมทริกซ์ในรายงาน
description: ใน Power BI Desktop ให้คุณสร้างคอลัมน์ที่มีไฮเปอร์ลิงก์ไปยังรูปภาพ จากนั้นจึงเพิ่มไฮเปอร์ลิงก์ดังกล่าวไปยังตารางรายงาน เมทริกซ์ ตัวแบ่งส่วนข้อมูล หรือการ์ดแบบหลายแถวเพื่อแสดงรูปภาพใน Power BI Desktop หรือบริการของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.custom: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 09/11/2019
LocalizationGroup: Visualizations
ms.openlocfilehash: 4ba0042804d366ddfd80935c48246cadeadf3614
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96417968"
---
# <a name="display-images-in-a-table-matrix-or-slicer-in-a-report"></a><span data-ttu-id="678af-104">แสดงรูปภาพต่าง ๆ ในตาราง เมทริกซ์ หรือตัวแบ่งส่วนข้อมูลในรายงาน</span><span class="sxs-lookup"><span data-stu-id="678af-104">Display images in a table, matrix, or slicer in a report</span></span>

<span data-ttu-id="678af-105">วิธีที่ดีในการเพิ่มประสิทธิภาพให้กับรายงานของคุณคือการเพิ่มรูปภาพในรายงาน</span><span class="sxs-lookup"><span data-stu-id="678af-105">A good way to enhance your reports is to add images to them.</span></span> <span data-ttu-id="678af-106">รูปภาพแบบคงที่บนหน้ารายงานนั้นเหมาะสำหรับวัตถุประสงค์บางอย่าง</span><span class="sxs-lookup"><span data-stu-id="678af-106">Static images on the page are good for some purposes.</span></span> <span data-ttu-id="678af-107">แต่บางครั้งคุณก็ต้องใช้รูปภาพที่เกี่ยวข้องกับข้อมูลในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="678af-107">But sometimes you want images that relate to the data in your report.</span></span> <span data-ttu-id="678af-108">ในหัวข้อนี้จะสอนวิธีการแสดงรูปภาพต่าง ๆ ในตาราง เมทริกซ์ ตัวแบ่งส่วนข้อมูล หรือการ์ดแบบหลายแถว</span><span class="sxs-lookup"><span data-stu-id="678af-108">This topic teaches you how to display images in a table, matrix, slicer, or multi-row card.</span></span> 

![รูปภาพ URL ในตาราง](media/power-bi-images-tables/power-bi-url-images-table.png)

## <a name="add-images-to-your-report"></a><span data-ttu-id="678af-110">เพิ่มรูปภาพลงในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="678af-110">Add images to your report</span></span>

1. <span data-ttu-id="678af-111">สร้างคอลัมน์ที่มี Url ของรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="678af-111">Create a column with the URLs of the images.</span></span> <span data-ttu-id="678af-112">ดูข้อกำหนดต่าง ๆ ได้ที่[ข้อควรพิจารณา](#considerations)ในบทความนี้</span><span class="sxs-lookup"><span data-stu-id="678af-112">See [Considerations](#considerations) later in this article for requirements.</span></span>

1. <span data-ttu-id="678af-113">เลือกคอลัมน์นั้น</span><span class="sxs-lookup"><span data-stu-id="678af-113">Select that column.</span></span> <span data-ttu-id="678af-114">บนริบบอน **การวางรูปแบบ** สำหรับ **หมวดหมู่ข้อมูล** ให้เลือก **URL ของรูปภาพ**</span><span class="sxs-lookup"><span data-stu-id="678af-114">On the **Modeling** ribbon, for **Data category**, select **Image URL**.</span></span>

    ![ตั้งค่าหมวดหมู่ข้อมูลเป็น URL ของรูปภาพ](media/power-bi-images-tables/power-bi-set-url-image.png)

1. <span data-ttu-id="678af-116">เพิ่มคอลัมน์ไปที่ตาราง เมทริกซ์ ตัวแบ่งส่วนข้อมูล หรือการ์ดแบบหลายแถว</span><span class="sxs-lookup"><span data-stu-id="678af-116">Add the column to a table, matrix, slicer, or multi-row card.</span></span>

    ![ตัวแบ่งส่วนข้อมูลที่มีรูปภาพ](media/power-bi-images-tables/power-bi-url-images-slicer.png)

## <a name="considerations"></a><span data-ttu-id="678af-118">ข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="678af-118">Considerations</span></span>

- <span data-ttu-id="678af-119">รูปภาพต้องอยู่ในรูปแบบไฟล์เหล่านี้:  .bmp, .jpg, .jpeg, .gif, .png หรือ .svg</span><span class="sxs-lookup"><span data-stu-id="678af-119">The image needs to be in one of these file formats: .bmp, .jpg, .jpeg, .gif, .png, or  .svg</span></span>
- <span data-ttu-id="678af-120">URL ต้องสามารถเข้าถึงได้โดยไม่ระบุตัวตน และไม่อยู่ในเว็บไซต์ที่จำเป็นต้องลงชื่อเข้าใช้ เช่น SharePoint</span><span class="sxs-lookup"><span data-stu-id="678af-120">The URL needs to be anonymously accessible, not on a site that requires a sign-in, such as SharePoint.</span></span> <span data-ttu-id="678af-121">อย่างไรก็ตาม หากมีการโฮสต์รูปภาพบน SharePoint หรือ OneDrive คุณอาจได้รับรหัสฝังตัวซึ่งจะนำทางไปยังรูปภาพดังกล่าวโดยตรง</span><span class="sxs-lookup"><span data-stu-id="678af-121">However, if images are hosted on SharePoint or OneDrive, you may be able to get an embed code that points directly to them.</span></span> 


## <a name="next-steps"></a><span data-ttu-id="678af-122">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="678af-122">Next steps</span></span>

[<span data-ttu-id="678af-123">เค้าโครงและการจัดรูปแบบหน้า</span><span class="sxs-lookup"><span data-stu-id="678af-123">Page layout and formatting</span></span>](/learn/modules/visuals-in-power-bi/12-formatting)

[<span data-ttu-id="678af-124">แนวคิดพื้นฐานสำหรับนักออกแบบในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="678af-124">Basic concepts for designers in the Power BI service</span></span>](../fundamentals/service-basic-concepts.md)

<span data-ttu-id="678af-125">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="678af-125">More questions?</span></span> [<span data-ttu-id="678af-126">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="678af-126">Try the Power BI Community</span></span>](https://community.powerbi.com/)
