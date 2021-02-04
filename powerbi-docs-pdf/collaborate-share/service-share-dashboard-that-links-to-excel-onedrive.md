---
title: แชร์แดชบอร์ดที่เชื่อมโยงไปยังไฟล์ Excel ใน OneDrive - Power BI
description: อ่านเกี่ยวกับการแชร์แดชบอร์ดที่เชื่อมโยงไปยังเวิร์กบุ๊ก Excel บน OneDrive for Business พร้อมด้วยไทล์ที่ปักหมุดจากเวิร์กบุ๊กนั้น
author: maggiesMSFT
ms.author: maggies
ms.reviewer: lukaszp
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 08/02/2018
LocalizationGroup: Share your work
ms.openlocfilehash: ee70a90ee104f1144595bd346b85d858f0aed49f
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411597"
---
# <a name="share-a-power-bi-dashboard-that-links-to-an-excel-file-in-onedrive"></a><span data-ttu-id="fcdfa-103">แชร์แดชบอร์ด Power BI ที่เชื่อมโยงไปยังไฟล์ Excel ใน OneDrive</span><span class="sxs-lookup"><span data-stu-id="fcdfa-103">Share a Power BI dashboard that links to an Excel file in OneDrive</span></span>
<span data-ttu-id="fcdfa-104">ใน Power BI คุณสามารถ[เชื่อมต่อกับเวิร์กบุ๊ก Excel บน OneDrive for Business](../connect-data/service-excel-workbook-files.md)และปักหมุดไทล์ไปยังแดชบอร์ดจากเวิร์กบุ๊กนั้นได้</span><span class="sxs-lookup"><span data-stu-id="fcdfa-104">In Power BI, you can [connect to Excel workbooks on OneDrive for Business](../connect-data/service-excel-workbook-files.md) and pin tiles to a dashboard from that workbook.</span></span> <span data-ttu-id="fcdfa-105">เมื่อคุณแชร์แดชบอร์ดนั้น หรือสร้างชุดเนื้อหาที่ประกอบด้วยแดชบอร์ดนั้น:</span><span class="sxs-lookup"><span data-stu-id="fcdfa-105">When you share that dashboard, or create a content pack that includes that dashboard:</span></span>

* <span data-ttu-id="fcdfa-106">เพื่อนร่วมงานของคุณสามารถดูไทล์โดยไม่จำเป็นต้องมีสิทธิ์การใช้งานสำหรับเวิร์กบุ๊กนั้นได้</span><span class="sxs-lookup"><span data-stu-id="fcdfa-106">Your colleagues can view the tiles without needing permissions for the workbook itself.</span></span> <span data-ttu-id="fcdfa-107">ดังนั้นคุณสามารถสร้างชุดเนื้อหาได้ และโปรดทราบว่าเพื่อนร่วมงานของคุณสามารถดูมีไทล์ที่สร้างขึ้นจากเวิร์กบุ๊ก Excel บน OneDrive ได้</span><span class="sxs-lookup"><span data-stu-id="fcdfa-107">So you can create a content pack and know that your colleagues can see the tiles created from the Excel workbook on OneDrive.</span></span>
* <span data-ttu-id="fcdfa-108">การคลิกที่ไทล์จะเปิดเวิร์กบุ๊กภายใน Power BI</span><span class="sxs-lookup"><span data-stu-id="fcdfa-108">Clicking the tile opens the workbook inside of Power BI.</span></span> <span data-ttu-id="fcdfa-109">เวิร์กบุ๊กจะเปิดขึ้นเฉพาะเมื่อผู้ร่วมงานของคุณมี[สิทธิ์การอ่าน](https://support.office.com/article/Share-documents-or-folders-in-Office-365-1fe37332-0f9a-4719-970e-d2578da4941c)สำหรับเวิร์กบุ๊กบน OneDrive for Business เป็นอย่างน้อย</span><span class="sxs-lookup"><span data-stu-id="fcdfa-109">The workbook will only open if your colleagues have at least [read permissions](https://support.office.com/article/Share-documents-or-folders-in-Office-365-1fe37332-0f9a-4719-970e-d2578da4941c) to the workbook on OneDrive for Business.</span></span>

## <a name="share-a-dashboard-that-contains-workbook-tiles"></a><span data-ttu-id="fcdfa-110">แชร์แดชบอร์ดที่ประกอบด้วยไทล์เวิร์กบุ๊ก</span><span class="sxs-lookup"><span data-stu-id="fcdfa-110">Share a dashboard that contains workbook tiles</span></span>
<span data-ttu-id="fcdfa-111">เมื่อต้องการแชร์แดชบอร์ดที่เชื่อมโยงกลับไปยังเวิร์กบุ๊ก Excel บน OneDrive for Business ดู[แชร์แดชบอร์ด](service-share-dashboards.md)</span><span class="sxs-lookup"><span data-stu-id="fcdfa-111">To share a dashboard that links back to an Excel workbook on OneDrive for Business, see [Share a dashboard](service-share-dashboards.md).</span></span> <span data-ttu-id="fcdfa-112">ความแตกต่างก็คือ คุณมีตัวเลือกในการปรับเปลี่ยนสิทธิ์การใช้งานสำหรับเวิร์กบุ๊ก Excel ที่เชื่อมโยงก่อนการแชร์</span><span class="sxs-lookup"><span data-stu-id="fcdfa-112">The difference is that you have the option to modify the permissions for the linked Excel workbook before sharing.</span></span>

  ![แชร์กล่องโต้ตอบแดชบอร์ด](media/service-share-dashboard-that-links-to-excel-onedrive/pbi_share_workbk.png)

1. <span data-ttu-id="fcdfa-114">ใส่อีเมลของผู้ร่วมงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="fcdfa-114">Enter the email addresses for your colleagues.</span></span>
2. <span data-ttu-id="fcdfa-115">เพื่อให้เพื่อนร่วมงานของคุณสามารถดูเวิร์กบุ๊ก Excel จาก Power BI ได้ เลือก **ไปยัง OneDrive for Business เพื่อตั้งค่าสิทธิ์การใช้งานเวิร์กบุ๊ก**</span><span class="sxs-lookup"><span data-stu-id="fcdfa-115">To enable your colleagues to view the Excel workbook from Power BI, select **Go to OneDrive for Business to set workbook permissions**.</span></span>
3. <span data-ttu-id="fcdfa-116">บน OneDrive [แก้ไขสิทธิ์การใช้งาน](https://support.office.com/article/Share-files-and-folders-and-change-permissions-9fcc2f7d-de0c-4cec-93b0-a82024800c07)ตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="fcdfa-116">On OneDrive, [modify the permissions](https://support.office.com/article/Share-files-and-folders-and-change-permissions-9fcc2f7d-de0c-4cec-93b0-a82024800c07) as needed.</span></span>
4. <span data-ttu-id="fcdfa-117">เลือก **แชร์**</span><span class="sxs-lookup"><span data-stu-id="fcdfa-117">Select **Share**.</span></span>

>[!NOTE]
><span data-ttu-id="fcdfa-118">เพื่อนร่วมงานของคุณจะไม่สามารถปักหมุดไทล์เพิ่มเติมจากเวิร์กบุ๊กนั้น หรือทำการเปลี่ยนแปลงไปยังเวิร์กบุ๊ก Excel จาก Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="fcdfa-118">Your colleagues won't be able to pin additional tiles from that workbook, or make changes to the Excel workbook from Power BI.</span></span>
> 
> 

## <a name="create-an-organizational-content-pack-with-a-dashboard-that-contains-workbook-tiles"></a><span data-ttu-id="fcdfa-119">สร้างชุดเนื้อหาองค์กรด้วยแดชบอร์ดที่ประกอบด้วยไทล์เวิร์กบุ๊ก</span><span class="sxs-lookup"><span data-stu-id="fcdfa-119">Create an organizational content pack with a dashboard that contains workbook tiles</span></span>
<span data-ttu-id="fcdfa-120">เมื่อคุณ[เผยแพร่ชุดเนื้อหา](service-organizational-content-pack-create-and-publish.md) คุณให้การเข้าถึงกับเพื่อนร่วมงานแต่ละคนหรือแต่ละกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="fcdfa-120">When you [publish a content pack](service-organizational-content-pack-create-and-publish.md) you give access to individual colleagues or groups.</span></span> <span data-ttu-id="fcdfa-121">เมื่อคุณเผยแพร่ชุดเนื้อหาที่ประกอบด้วยลิงก์เวิร์กบุ๊ก คุณจะมีตัวเลือกในการปรับเปลี่ยนสิทธิ์การใช้งานสำหรับเวิร์กบุ๊ก Excel ที่เชืี่อมโยงก่อนการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="fcdfa-121">When you publish a content pack that contains workbook links, you'll have the option to modify the permissions for the linked Excel workbook before publishing.</span></span>

1. <span data-ttu-id="fcdfa-122">ที่หน้าจอ **สร้างชุดเนื้อหา** ใส่ที่อยู่อีเมล ใส่ชื่อเรื่องชุดเนื้อหาและคำอธิบาย จากนั้นอัปโหลดรูป</span><span class="sxs-lookup"><span data-stu-id="fcdfa-122">In the **Create content pack** screen, enter email addresses, give the content pack a title and description, and upload an image.</span></span>
2. <span data-ttu-id="fcdfa-123">เลือกแดชบอร์ดและ/หรือรายงานที่เชื่อมโยงไปยังเวิร์กบุ๊ก Excel บน OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="fcdfa-123">Select the dashboard and/or report that is linked to the Excel workbook on OneDrive for Business.</span></span>
   
    ![เวิร์กบุ๊ก Excel ในชุดเนื้อหา](media/service-share-dashboard-that-links-to-excel-onedrive/pbi_contpack_workbk.png)
3. <span data-ttu-id="fcdfa-125">เลือก **ไปยัง OneDrive for Business เพื่อตั้งค่าสิทธิ์เวิร์กบุ๊ก**</span><span class="sxs-lookup"><span data-stu-id="fcdfa-125">Select **Go to OneDrive for Business to set workbook permissions**.</span></span>
4. <span data-ttu-id="fcdfa-126">บน OneDrive [แก้ไขสิทธิ์การใช้งาน](https://support.office.com/article/Share-files-and-folders-and-change-permissions-9fcc2f7d-de0c-4cec-93b0-a82024800c07)ตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="fcdfa-126">On OneDrive, [modify the permissions](https://support.office.com/article/Share-files-and-folders-and-change-permissions-9fcc2f7d-de0c-4cec-93b0-a82024800c07) as needed.</span></span>
5. <span data-ttu-id="fcdfa-127">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="fcdfa-127">Select **Publish**.</span></span>

## <a name="share-a-dashboard-from-a-power-bi-workspace"></a><span data-ttu-id="fcdfa-128">แชร์แดชบอร์ดจากพื้นที่ทำงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="fcdfa-128">Share a dashboard from a Power BI workspace</span></span>
<span data-ttu-id="fcdfa-129">การแชร์แดชบอร์ดจากพื้นที่ทำงาน Power BI จะคล้ายกับการแชร์แดชบอร์ดจากพื้นที่ทำงานของคุณเอง เว้นแต่ว่าไฟล์ต่างๆ จะอยู่ในไซต์พื้นที่ทำงาน Microsoft 365 แทนการอยู่ใน OneDrive for Business ส่วนตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="fcdfa-129">Sharing a dashboard from a Power BI workspace is similar to sharing a dashboard from your own workspace, except that the files are located in a Microsoft 365 workspace site, instead of your private OneDrive for Business.</span></span> <span data-ttu-id="fcdfa-130">ปรับเปลี่ยนสิทธิ์การใช้งานสำหรับเวิร์กบุ๊ก Excel ก่อนที่จะแชร์แดชบอร์ดกับบุคคลภายนอกพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="fcdfa-130">Modify the permissions for the Excel workbook before sharing the dashboard with people outside the workspace.</span></span>

![แชร์จาก OneDrive](media/service-share-dashboard-that-links-to-excel-onedrive/pbi_onedriveshare.png)

## <a name="next-steps"></a><span data-ttu-id="fcdfa-132">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="fcdfa-132">Next steps</span></span>
* [<span data-ttu-id="fcdfa-133">ปักหมุดไทล์ไปที่แดชบอร์ด Power BI จาก Excel</span><span class="sxs-lookup"><span data-stu-id="fcdfa-133">Pin a tile to a Power BI dashboard from Excel</span></span>](../create-reports/service-dashboard-pin-tile-from-excel.md)
* [<span data-ttu-id="fcdfa-134">แนวคิดพื้นฐานสำหรับนักออกแบบในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="fcdfa-134">Basic concepts for designers in the Power BI service</span></span>](../fundamentals/service-basic-concepts.md)
* <span data-ttu-id="fcdfa-135">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="fcdfa-135">More questions?</span></span> [<span data-ttu-id="fcdfa-136">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="fcdfa-136">Try the Power BI Community</span></span>](https://community.powerbi.com/)
