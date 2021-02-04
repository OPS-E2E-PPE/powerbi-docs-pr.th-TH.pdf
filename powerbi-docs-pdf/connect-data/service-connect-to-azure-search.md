---
title: เชื่อมต่อกับ Azure Search ด้วย Power BI
description: Azure Search สำหรับ Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: conceptual
ms.date: 08/29/2019
LocalizationGroup: Connect to services
ms.openlocfilehash: 5c2c5d3b6382fdb85125a71829d62624dab31e83
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96403386"
---
# <a name="connect-to-azure-search-with-power-bi"></a><span data-ttu-id="3dc93-103">เชื่อมต่อกับ Azure Search ด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="3dc93-103">Connect to Azure Search with Power BI</span></span>
<span data-ttu-id="3dc93-104">การวิเคราะห์การรับส่งข้อมูล Azure Search (Azure Search Traffic Analytics) ช่วยให้คุณสามารถตรวจติดตามและทำความเข้าใจเกี่ยวกับการรับส่งข้อมูลไปยังบริการค้นหา Azure ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3dc93-104">Azure Search Traffic Analytics allows you to monitor and understand the traffic to your Azure Search service.</span></span> <span data-ttu-id="3dc93-105">ชุดเนื้อหา Azure Search สำหรับ Power BI ให้ข้อมูลเชิงลึกโดยละเอียดเกี่ยวกับข้อมูลการค้นหาของคุณ โดยรวมถึงการค้นหา การทำดัชนี สถิติการบริการ และเวลาแฝงในช่วงเวลส 30 วันที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="3dc93-105">The Azure Search content pack for Power BI provides detailed insights on your Search data, including Search, Indexing, Service Stats and Latency from the last 30 days.</span></span> <span data-ttu-id="3dc93-106">คุณสามารถพบรายละเอียดเพิ่มเติมใน[บล็อกโพสต์ Azure](https://azure.microsoft.com/blog/analyzing-your-azure-search-traffic/)</span><span class="sxs-lookup"><span data-stu-id="3dc93-106">More details can be found in the [Azure blog post](https://azure.microsoft.com/blog/analyzing-your-azure-search-traffic/).</span></span>

[!INCLUDE [include-short-name](../includes/service-deprecate-content-packs.md)]

<span data-ttu-id="3dc93-107">เชื่อมต่อไปยัง[ชุดเนื้อหา Azure Search](https://app.powerbi.com/getdata/services/azure-search)สำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="3dc93-107">Connect to the [Azure Search content pack](https://app.powerbi.com/getdata/services/azure-search) for Power BI.</span></span>

## <a name="how-to-connect"></a><span data-ttu-id="3dc93-108">วิธีการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="3dc93-108">How to connect</span></span>
1. <span data-ttu-id="3dc93-109">เลือก **รับข้อมูล** ที่ด้านล่างของบานหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="3dc93-109">Select **Get Data** at the bottom of the nav pane.</span></span>
   
   ![ภาพหน้าจอของรับข้อมูลใน Power BI Desktop ที่แสดงปุ่มในบานหน้าต่างตัวนำทาง](media/service-connect-to-azure-search/pbi_getdata.png) 
2. <span data-ttu-id="3dc93-111">ในกล่อง **บริการ** เลือก **รับ**</span><span class="sxs-lookup"><span data-stu-id="3dc93-111">In the **Services** box, select **Get**.</span></span>
   
   ![ภาพหน้าจอของกล่องโต้ตอบ Services ที่แสดงปุ่มรับ](media/service-connect-to-azure-search/pbi_getservices.png) 
3. <span data-ttu-id="3dc93-113">เลือก **Azure Search** \> **รับ**</span><span class="sxs-lookup"><span data-stu-id="3dc93-113">Select **Azure Search** \> **Get**.</span></span>
   
   ![ภาพหน้าจอของกล่องโต้ตอบ Azure Services ที่แสดงลิงก์รับ](media/service-connect-to-azure-search/azuresearch.png)
4. <span data-ttu-id="3dc93-115">ใส่ชื่อบัญชีเก็บข้อมูลตารางที่จัดเก็บการวิเคราะห์ Azure Search ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3dc93-115">Provide the name of the table storage account your Azure Search analysis is stored.</span></span>
   
   ![ภาพหน้าจอของกล่องโต้ตอบ Connect Azure Search ที่แสดงเขตข้อมูลชื่อบัญชีที่เก็บข้อมูล Azure](media/service-connect-to-azure-search/params.png)
5. <span data-ttu-id="3dc93-117">เลือก **คีย์** เป็นกลไกการรับรองความถูกต้อง และใส่คีย์บัญชีเก็บข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="3dc93-117">Select **Key** as the Authentication Mechanism and provide your storage account key.</span></span> <span data-ttu-id="3dc93-118">คลิก **ลงชื่อเข้าใช้** เพื่อเริ่มกระบวนการการโหลด</span><span class="sxs-lookup"><span data-stu-id="3dc93-118">Click **Sign In** and to begin the loading process.</span></span>
   
   ![ภาพหน้าจอของกล่องโต้ตอบ Connect Azure Search ที่แสดงการป้อนคีย์ในเขตข้อมูลวิธีการรับรองความถูกต้อง](media/service-connect-to-azure-search/creds.png)
6. <span data-ttu-id="3dc93-120">เมื่อการดาวน์โหลดเสร็จสิ้น แดชบอร์ดใหม่ รายงาน และแบบจำลองจะปรากฏในบานหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="3dc93-120">Once the loading is complete, a new dashboard, report and model will appear in the nav pane.</span></span> <span data-ttu-id="3dc93-121">เลือกแดชบอร์ดเพื่อดูข้อมูลที่นำเข้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="3dc93-121">Select the dashboard to view your imported data.</span></span>
   
    ![ภาพหน้าจอของบานหน้าต่างการนำทาง ที่แสดงแดชบอร์ด รายงาน และแบบจำลอง](media/service-connect-to-azure-search/dashboard2.png)

<span data-ttu-id="3dc93-123">**ฉันต้องทำอะไรตอนนี้**</span><span class="sxs-lookup"><span data-stu-id="3dc93-123">**What now?**</span></span>

* <span data-ttu-id="3dc93-124">ลอง[ถามคำถามในกล่อง Q&A](../consumer/end-user-q-and-a.md)ที่ด้านบนของแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="3dc93-124">Try [asking a question in the Q&A box](../consumer/end-user-q-and-a.md) at the top of the dashboard</span></span>
* <span data-ttu-id="3dc93-125">[เปลี่ยนไทล์](../create-reports/service-dashboard-edit-tile.md)ในแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="3dc93-125">[Change the tiles](../create-reports/service-dashboard-edit-tile.md) in the dashboard.</span></span>
* <span data-ttu-id="3dc93-126">[เลือกไทล์](../consumer/end-user-tiles.md)เพื่อเปิดรายงานด้านใน</span><span class="sxs-lookup"><span data-stu-id="3dc93-126">[Select a tile](../consumer/end-user-tiles.md) to open the underlying report.</span></span>
* <span data-ttu-id="3dc93-127">แม้ว่าชุดข้อมูลของคุณจะถูกกำหนดให้รีเฟรชรายวัน แต่คุณสามารถเปลี่ยนกำหนดการรีเฟรช หรือลองรีเฟรชตามความต้องการได้โดยใช้ **รีเฟรชเดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="3dc93-127">While your dataset will be scheduled to refresh daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**</span></span>

## <a name="system-requirements"></a><span data-ttu-id="3dc93-128">ความต้องการของระบบ</span><span class="sxs-lookup"><span data-stu-id="3dc93-128">System requirements</span></span>
<span data-ttu-id="3dc93-129">ชุดเนื้อหา Azure Search ต้องมีการวิเคราะห์การรับส่งข้อมูล Azure Search ที่เปิดใช้งานในบัญชีผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="3dc93-129">The Azure Search content pack requires Azure Search Traffic Analytics to be enabled on the account.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="3dc93-130">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="3dc93-130">Troubleshooting</span></span>
<span data-ttu-id="3dc93-131">ตรวจสอบให้แน่ใจว่าใส่ชื่อบัญชีเก็บข้อมูลได้อย่างถูกต้อง พร้อมกับคีย์การเข้าถึงแบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="3dc93-131">Ensure the storage account name is correctly provided along with the full access key.</span></span> <span data-ttu-id="3dc93-132">ชื่อบัญชีเก็บข้อมูลควรตรงกับบัญชีผู้ใช้ที่กำหนดค่าด้วยการวิเคราะห์การรับส่งข้อมูล Azure Search</span><span class="sxs-lookup"><span data-stu-id="3dc93-132">The storage account name should correspond to the account configured with Azure Search Traffic Analytics.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3dc93-133">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3dc93-133">Next steps</span></span>
[<span data-ttu-id="3dc93-134">Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="3dc93-134">What is Power BI?</span></span>](../fundamentals/power-bi-overview.md)

[<span data-ttu-id="3dc93-135">แนวคิดพื้นฐานสำหรับนักออกแบบในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="3dc93-135">Basic concepts for designers in the Power BI service</span></span>](../fundamentals/service-basic-concepts.md)
