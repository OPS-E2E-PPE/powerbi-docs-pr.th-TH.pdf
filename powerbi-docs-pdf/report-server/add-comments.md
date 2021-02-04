---
title: เพิ่มข้อคิดเห็นไปยังรายงานในเซิร์ฟเวอร์รายงาน Power BI
description: เรียนรู้วิธีการเพิ่มข้อคิดเห็นไปยัง Power BI หรือรายงานที่มีการแบ่งหน้าบนเซิร์ฟเวอร์รายงาน Power BI หรือรีพอร์ตเซิร์ฟเวอร์ของ SQL Server Reporting Services
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.date: 11/15/2018
ms.openlocfilehash: 4d705176105013672bc89dc19620a1d67a3ce620
ms.sourcegitcommit: eef4eee24695570ae3186b4d8d99660df16bf54c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/23/2020
ms.locfileid: "85239477"
---
# <a name="add-comments-to-a-report-in-a-report-server---power-bi-report-server"></a><span data-ttu-id="df668-103">เพิ่มข้อคิดเห็นไปยังรายงานในรีพอร์ตเซิร์ฟเวอร์ - เซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="df668-103">Add comments to a report in a report server - Power BI Report Server</span></span>

<span data-ttu-id="df668-104">คุณสามารถเพิ่มข้อคิดเห็นเมื่อต้องการรายงาน รวมถึงรายงาน Power BI ภายในพอร์ทัลเว็บของรีพอร์ตเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="df668-104">You can add comments to reports, including Power BI reports, within the web portal of a report server.</span></span> <span data-ttu-id="df668-105">ข้อคิดเห็นสดพร้อมรายงาน และทุกคนที่มีสิทธิ์ที่เหมาะสม สามารถดูข้อคิดเห็นสำหรับรายงานได้</span><span class="sxs-lookup"><span data-stu-id="df668-105">The comments live with the report, and anyone with the right permissions can see the comments for the report.</span></span> <span data-ttu-id="df668-106">ดูส่วน[การให้สิทธิ์](#permissions)ด้านล่างสำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="df668-106">See the [Permissions](#permissions) section below for details.</span></span>

## <a name="add-or-view-comments"></a><span data-ttu-id="df668-107">เพิ่ม หรือดูข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="df668-107">Add or view comments</span></span>

1. <span data-ttu-id="df668-108">เปิดส่วนที่มีการแบ่งหน้าหรือรายงาน Power BI บนรีพอร์ตเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="df668-108">Open a paginated or Power BI report on a report server.</span></span>
2. <span data-ttu-id="df668-109">ในมุมขวาบน ให้เลือก**ข้อคิดเห็น**</span><span class="sxs-lookup"><span data-stu-id="df668-109">In the upper-right corner, select **Comments**.</span></span>

    ![เลือกข้อคิดเห็น](media/add-comments/report-server-web-portal-comments-button.png)

    <span data-ttu-id="df668-111">ในบานหน้าต่างข้อคิดเห็น คุณสามารถดูข้อคิดเห็นใดๆ ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="df668-111">In the Comments pane, you can see any existing comments.</span></span>
3. <span data-ttu-id="df668-112">เขียนข้อคิดเห็นของคุณ จากนั้นเลือก**โพสต์ข้อคิดเห็น**</span><span class="sxs-lookup"><span data-stu-id="df668-112">Write your comment, then select **Post Comment**.</span></span>

    ![โพสต์ข้อคิดเห็น](media/add-comments/report-server-web-portal-comments-pane.png)

    <span data-ttu-id="df668-114">ข้อคิดเห็นของคุณจะแสดงในบานหน้าต่างด้านบนพอร์ทัลเว็บ พร้อมกับข้อคิดเห็นก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="df668-114">Your comment shows in the pane on the web portal, along with any previous comments.</span></span> <span data-ttu-id="df668-115">ข้อคิดเห็นนั้นไม่ได้ปรากฏพร้อมกับรายงานในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="df668-115">They don't appear with the report on in the Power BI mobile apps.</span></span>

   > [!TIP]
   > <span data-ttu-id="df668-116">คุณทราบหรือไม่</span><span class="sxs-lookup"><span data-stu-id="df668-116">Did you know?</span></span> <span data-ttu-id="df668-117">คุณสามารถ[ใส่คำอธิบายประกอบรายงาน Power BI ในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่](../consumer/mobile/mobile-annotate-and-share-a-tile-from-the-mobile-apps.md)และแชร์รายงานที่มีคำอธิบายประกอบกับผู้อื่นได้</span><span class="sxs-lookup"><span data-stu-id="df668-117">You can [annotate Power BI reports in the Power BI mobile apps](../consumer/mobile/mobile-annotate-and-share-a-tile-from-the-mobile-apps.md) and share the annotated reports with others.</span></span>

## <a name="permissions"></a><span data-ttu-id="df668-118">สิทธิ์</span><span class="sxs-lookup"><span data-stu-id="df668-118">Permissions</span></span>

<span data-ttu-id="df668-119">ขึ้นอยู่กับสิทธิ์ของคุณ คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="df668-119">Depending on your permissions, you can:</span></span>

* <span data-ttu-id="df668-120">ไม่เห็นข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="df668-120">Not see comments.</span></span>
* <span data-ttu-id="df668-121">ดูข้อคิดเห็นทั้งหมด และโพสต์ แก้ไข และลบของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="df668-121">See all comments, and post, edit, and delete your own.</span></span>
* <span data-ttu-id="df668-122">ดูข้อคิดเห็นทั้งหมด โพสต์ แก้ไข และลบของคุณเอง และลบของบุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="df668-122">See all comments; post, edit, and delete your own; and delete other people’s.</span></span>

## <a name="next-steps"></a><span data-ttu-id="df668-123">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="df668-123">Next steps</span></span>
* [<span data-ttu-id="df668-124">เซิร์ฟเวอร์รายงาน Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="df668-124">What is Power BI Report Server?</span></span>](get-started.md)  

<span data-ttu-id="df668-125">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="df668-125">More questions?</span></span> [<span data-ttu-id="df668-126">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="df668-126">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)

