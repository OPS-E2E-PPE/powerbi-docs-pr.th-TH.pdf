---
title: เชื่อมต่อกับ Office365Mon ด้วย Power BI
description: Office365Mon for Power BI
author: paulinbar
ms.author: painbar
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: how-to
ms.date: 11/26/2019
LocalizationGroup: Connect to services
ms.openlocfilehash: c7433bcc75da316e2e705a63dbcc2f17745ad573
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96403064"
---
# <a name="connect-to-office365mon-with-power-bi"></a><span data-ttu-id="7b018-103">เชื่อมต่อกับ Office365Mon ด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="7b018-103">Connect to Office365Mon with Power BI</span></span>
<span data-ttu-id="7b018-104">การวิเคราะห์การหยุดการทำงานและข้อมูลสมรรถนะการทำงานของ Office 365 ของคุณทำได้ง่ายด้วย Power BI และแอปแม่แบบ Office365Mon</span><span class="sxs-lookup"><span data-stu-id="7b018-104">Analyzing your Office 365 outages and health performance data is easy with Power BI and the Office365Mon template app.</span></span> <span data-ttu-id="7b018-105">Power BI ดึงข้อมูลของคุณ ทั้งการหยุดทำงานและปัญหาด้านสุขภาพ จากนั้นสร้างแดชบอร์ดแบบคิดนอกกรอบและรายงานที่ยึดตามข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="7b018-105">Power BI retrieves your data, including outages and health probes, then builds an out-of-box dashboard and reports based on that data.</span></span>

<span data-ttu-id="7b018-106">เชื่อมต่อไปยัง[แอปแม่แบบ Office365Mon](https://msit.powerbi.com/groups/me/getapps/services/office365mon.office365mon_powerbi_v3)สำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="7b018-106">Connect to the [Office365Mon template app](https://msit.powerbi.com/groups/me/getapps/services/office365mon.office365mon_powerbi_v3) for Power BI.</span></span>

>[!NOTE]
><span data-ttu-id="7b018-107">จำเป็นต้องมีบัญชีผู้ดูแลระบบ Office365Mon เพื่อเชื่อมต่อและโหลดแอปแม่แบบ Power BI</span><span class="sxs-lookup"><span data-stu-id="7b018-107">An Office365Mon admin account is required to connect and load the Power BI template app.</span></span>

## <a name="how-to-connect"></a><span data-ttu-id="7b018-108">วิธีการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="7b018-108">How to connect</span></span>
1. <span data-ttu-id="7b018-109">เลือก **รับข้อมูล** ที่ด้านล่างของบานหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="7b018-109">Select **Get Data** at the bottom of the nav pane.</span></span>
   
   ![ภาพหน้าจอของปุ่มรับข้อมูล ที่แสดงปุ่มในบานหน้าต่างการนำทาง](media/service-connect-to-office365mon/pbi_getdata.png)
2. <span data-ttu-id="7b018-111">ในกล่อง **บริการ** เลือก **รับ**</span><span class="sxs-lookup"><span data-stu-id="7b018-111">In the **Services** box, select **Get**.</span></span>
   
   ![ภาพหน้าจอของกล่องโต้ตอบบริการ ที่แสดงปุ่มรับ](media/service-connect-to-office365mon/pbi_getservices.png) 
3. <span data-ttu-id="7b018-113">เลือก **Office365Mon** \> **รับ**</span><span class="sxs-lookup"><span data-stu-id="7b018-113">Select **Office365Mon** \> **Get**.</span></span>
   
   ![ภาพหน้าจอของกล่องโต้ตอบ Office365Mon ที่แสดงลิงก์รับ](media/service-connect-to-office365mon/o365mon.png)
4. <span data-ttu-id="7b018-115">สำหรับวิธีการรับรองความถูกต้อง ให้เลือก **oAuth2** \> **ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="7b018-115">For Authentication Method, select **oAuth2** \> **Sign In**.</span></span>
   
   <span data-ttu-id="7b018-116">เมื่อไดถูกถาม ให้ใส่ข้อมูลประจำตัวของผู้ดูแลระบบ Office365Mon และทำตามกระบวนการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="7b018-116">When prompted, enter your Office365Mon admin credentials and follow the authentication process.</span></span>
   
   ![ภาพหน้าจอของกล่องโต้ตอบ Office365Mon ที่แสดง o Auth2 ในเขตข้อมูลวิธีการรับรองความถูกต้อง](media/service-connect-to-office365mon/creds.png)
   
   ![ภาพหน้าจอของการลงชื่อเข้าใช้ Office365Mon ที่แสดงการส่งข้อความแจ้งเตือนสำหรับข้อมูลประจำตัว](media/service-connect-to-office365mon/creds2.png)
5. <span data-ttu-id="7b018-119">หลังจากที่ Power BI นำเข้าข้อมูลแล้ว คุณจะเห็นแดชบอร์ด รายงาน และชุดข้อมูลใหม่ในบานหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="7b018-119">After Power BI imports the data you will see a new dashboard, report, and dataset in the nav pane.</span></span> <span data-ttu-id="7b018-120">รายการใหม่ถูกทำเครื่องหมายด้วยเครื่องหมายดอกจันสีเหลือง \* เลือกกรอก Office365Mon</span><span class="sxs-lookup"><span data-stu-id="7b018-120">New items are marked with a yellow asterisk \*, select the Office365Mon entry.</span></span>
   
   ![ภาพหน้าจอของบานหน้าต่างการนำทางใน Power B I ที่สดงแดชบอร์ด รายงาน และชุดข้อมูล](media/service-connect-to-office365mon/dashboard4.png)

<span data-ttu-id="7b018-122">**ฉันต้องทำอะไรตอนนี้**</span><span class="sxs-lookup"><span data-stu-id="7b018-122">**What now?**</span></span>

* <span data-ttu-id="7b018-123">ลอง[ถามคำถามในกล่อง Q&A](../consumer/end-user-q-and-a.md)ที่ด้านบนของแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="7b018-123">Try [asking a question in the Q&A box](../consumer/end-user-q-and-a.md) at the top of the dashboard</span></span>
* <span data-ttu-id="7b018-124">[เปลี่ยนไทล์](../create-reports/service-dashboard-edit-tile.md)ในแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="7b018-124">[Change the tiles](../create-reports/service-dashboard-edit-tile.md) in the dashboard.</span></span>
* <span data-ttu-id="7b018-125">[เลือกไทล์](../consumer/end-user-tiles.md)เพื่อเปิดรายงานด้านใน</span><span class="sxs-lookup"><span data-stu-id="7b018-125">[Select a tile](../consumer/end-user-tiles.md) to open the underlying report.</span></span>
* <span data-ttu-id="7b018-126">แม้ว่าชุดข้อมูลของคุณจะถูกกำหนดให้รีเฟรชรายวัน แต่คุณสามารถเปลี่ยนกำหนดการรีเฟรช หรือลองรีเฟรชตามความต้องการได้โดยใช้ **รีเฟรชเดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="7b018-126">While your dataset will be scheduled to refresh daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="7b018-127">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="7b018-127">Troubleshooting</span></span>
<span data-ttu-id="7b018-128">ถ้าคุณได้รับข้อผิดพลาด **"เข้าสู่ระบบล้มเหลว"** หลังจากใช้ข้อมูลประจำตัวของการสมัครใช้งาน Office365Mon เข้าระบบ จากนั้นบัญชีคุณไม่มีสิทธิ์ในการดึงข้อมูล Office365Mon จากบัญชีของคุณ</span><span class="sxs-lookup"><span data-stu-id="7b018-128">If you get a **"login failed"** error after using your Office365Mon subscription credentials to login, then the account you are using doesn't have permissions to retrieve the Office365Mon data from your account.</span></span> <span data-ttu-id="7b018-129">ตรวจสอบนี่เป็นบัญชีผู้ดูแลระบบ และลองอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="7b018-129">Verify it is an admin account and try again.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7b018-130">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="7b018-130">Next steps</span></span>
[<span data-ttu-id="7b018-131">Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="7b018-131">What is Power BI?</span></span>](../fundamentals/power-bi-overview.md)

[<span data-ttu-id="7b018-132">รับข้อมูลสำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="7b018-132">Get Data for Power BI</span></span>](service-get-data.md)
