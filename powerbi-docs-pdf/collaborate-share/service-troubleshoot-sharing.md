---
title: แก้ไขปัญหาการแชร์แดชบอร์ดและรายงาน
description: วิธีการแก้ไขปัญหาในการแชร์แดชบอร์ดและรายงาน Power BI กับเพื่อนร่วมงานทั้งในและนอกองค์กรของคุณ
author: maggiesMSFT
ms.author: maggies
ms.reviewer: lukaszp
featuredvideoid: 0tUwn8DHo3s
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: troubleshooting
ms.date: 06/23/2020
LocalizationGroup: Share your work
ms.openlocfilehash: 89d0ddbbcdd5caf47256fc85864590e55a1caa86
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96406682"
---
# <a name="troubleshoot-sharing-dashboards-and-reports"></a><span data-ttu-id="42253-103">แก้ไขปัญหาการแชร์แดชบอร์ดและรายงาน</span><span class="sxs-lookup"><span data-stu-id="42253-103">Troubleshoot sharing dashboards and reports</span></span>

<span data-ttu-id="42253-104">ต่อไปนี้คือปัญหาทั่วไปบางอย่างที่อาจเกิดขึ้นเมื่อคุณแชร์แดชบอร์ดหรือรายงาน หรือเมื่อมีผู้อื่นแชร์กับคุณ</span><span class="sxs-lookup"><span data-stu-id="42253-104">Here are some common issues that may come up when you're sharing a dashboard or report, or when someone else is sharing with you.</span></span> 

## <a name="dashboard-recipients-see-a-lock-icon-in-a-tile"></a><span data-ttu-id="42253-105">ผู้รับแดชบอร์ดจะเห็นไอคอนล็อกในไทล์</span><span class="sxs-lookup"><span data-stu-id="42253-105">Dashboard recipients see a lock icon in a tile</span></span>

<span data-ttu-id="42253-106">บุคคลที่คุณแชรให้อาจเห็นไทล์ในแดชบอร์ด หรือข้อความ "ต้องมีการให้อนุญาต" ถูกล็อก เมื่อพวกเขาพยายามดูรายงาน</span><span class="sxs-lookup"><span data-stu-id="42253-106">The people you share with may see a locked tile in a dashboard, or a "Permission required" message when they try to view a report.</span></span>

![ไทล์ของ power BI ถูกล็อก](media/service-share-dashboards/power-bi-locked_tile_small.png)

<span data-ttu-id="42253-108">ถ้าเป็นเช่นนั้น คุณจำเป็นต้องให้สิทธิ์ในชุดข้อมูลด้านในแก่พวกเขา</span><span class="sxs-lookup"><span data-stu-id="42253-108">If so, you need to grant them permission to the underlying dataset.</span></span>

1. <span data-ttu-id="42253-109">ไปที่แท็บ **ชุดข้อมูล** ในรายการของคุณเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="42253-109">Go to the **Datasets** tab in your content list.</span></span>

1. <span data-ttu-id="42253-110">เลือกจุดไข่ปลา ( **...** ) ถัดจากชุดข้อมูล > จากนั้นเลือก **จัดการการอนุญาต**</span><span class="sxs-lookup"><span data-stu-id="42253-110">Select the ellipsis (**...**) next to the dataset, then select **Manage permissions**.</span></span>

    ![จัดการการอนุญาต](media/service-share-dashboards/power-bi-sharing-manage-permissions.png)

1. <span data-ttu-id="42253-112">เลือก **เพิ่มผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="42253-112">Select **Add user**.</span></span>

    ![เพิ่มผู้ใช้](media/service-share-dashboards/power-bi-share-dataset-add-user.png)

1. <span data-ttu-id="42253-114">ใส่อยู่อีเมลแบบเต็มของบุคคล กลุ่มการเผยแพร่หรือกลุ่มความปลอดภัยของคุณ</span><span class="sxs-lookup"><span data-stu-id="42253-114">Enter the full email addresses for individuals, distribution groups, or security groups.</span></span> <span data-ttu-id="42253-115">คุณไม่สามารถใช้ร่วมกับรายการการแจกแจงแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="42253-115">You can't share with dynamic distribution lists.</span></span>

    ![เพิ่มที่อยู่อีเมล](media/service-share-dashboards/power-bi-add-user-dataset.png)

1. <span data-ttu-id="42253-117">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="42253-117">Select **Add**.</span></span>

## <a name="i-cant-share-a-dashboard-or-report"></a><span data-ttu-id="42253-118">ฉันไม่สามารถแชร์แดชบอร์ดหรือรายงาน</span><span class="sxs-lookup"><span data-stu-id="42253-118">I can't share a dashboard or report</span></span>

<span data-ttu-id="42253-119">เมื่อต้องแชร์แดชบอร์ดหรือรายงาน คุณต้องได้รับอนุญาตแชร์เนื้อหาเบื้องต้นใด ๆ ที่เกี่ยวข้องกับรายงานและชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="42253-119">To share a dashboard or report, you need permission to reshare the underlying content; that is, any related reports and datasets.</span></span> <span data-ttu-id="42253-120">ถ้าคุณเห็นข้อความบอกว่า คุณไม่สามารถแชร์ได้ ขอให้ผู้เขียนรายงานให้แชร์สิทธิ์สำหรับรายงานและชุดข้อมูลเหล่านั้นแก่คุณอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="42253-120">If you see a message saying you can't share, ask the report author to give you reshare permission for those reports and datasets.</span></span>

![ข้อความ "ไม่สามารถแชร์"](media/service-share-dashboards/power-bi-sharing-unable-to-share.png)

## <a name="i-dont-have-access-to-a-dashboard-or-report"></a><span data-ttu-id="42253-122">ฉันไม่สามารถเข้าถึงแดชบอร์ดหรือรายงานได้</span><span class="sxs-lookup"><span data-stu-id="42253-122">I don't have access to a dashboard or report</span></span>

<span data-ttu-id="42253-123">ถ้าคุณเห็นข้อความ "ขอสิทธิ์การเข้าถึง" เมื่อคุณเลือกที่ลิงก์ไปยังรายงานหรือแดชบอร์ด แสดงว่าคุณไม่มีสิทธิ์ในการเข้าดูรายการ</span><span class="sxs-lookup"><span data-stu-id="42253-123">If you see a "Request access" message when you select the link to a report or dashboard, you don't have permission to view it.</span></span> <span data-ttu-id="42253-124">คุณจำเป็นต้อง [ขอสิทธิ์การเข้าถึง](service-request-access.md)</span><span class="sxs-lookup"><span data-stu-id="42253-124">You need to [request access to it](service-request-access.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="42253-125">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="42253-125">Next steps</span></span>

- [<span data-ttu-id="42253-126">แชร์แดชบอร์ดและรายงาน Power BI กับเพื่อนร่วมงานและคนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="42253-126">Share Power BI dashboards and reports with coworkers and others</span></span>](service-share-dashboards.md)
- [<span data-ttu-id="42253-127">ฉันควรทำงานร่วมกัน และแชร์แดชบอร์ดและรายงานได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="42253-127">How should I collaborate on and share dashboards and reports?</span></span>](service-how-to-collaborate-distribute-dashboards-reports.md)
-  [<span data-ttu-id="42253-128">แชร์รายงาน Power BI ที่ถูกกรอง</span><span class="sxs-lookup"><span data-stu-id="42253-128">Share a filtered Power BI report</span></span>](service-share-reports.md)
- <span data-ttu-id="42253-129">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="42253-129">Questions?</span></span> [<span data-ttu-id="42253-130">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="42253-130">Try the Power BI Community</span></span>](https://community.powerbi.com/)
