---
title: รีเฟรชชุดข้อมูลที่สร้างจากไฟล์ Power BI Desktop - ภายในเครื่อง
description: รีเฟรชชุดข้อมูลที่สร้างจากไฟล์ Power BI Desktop ภายในไดรฟ์ของเครื่อง
author: davidiseminger
ms.author: davidi
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 06/04/2019
LocalizationGroup: Data refresh
ms.openlocfilehash: d836c8d85915332c58032cf535194ca5ce803567
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96404030"
---
# <a name="refresh-a-dataset-created-from-a-power-bi-desktop-file-on-a-local-drive"></a><span data-ttu-id="02d0b-103">รีเฟรชชุดข้อมูลที่สร้างจากไฟล์ Power BI Desktop ภายในไดรฟ์ของเครื่อง</span><span class="sxs-lookup"><span data-stu-id="02d0b-103">Refresh a dataset created from a Power BI Desktop file on a local drive</span></span>

## <a name="whats-supported"></a><span data-ttu-id="02d0b-104">รับรองอะไรบ้าง</span><span class="sxs-lookup"><span data-stu-id="02d0b-104">What’s supported?</span></span>

<span data-ttu-id="02d0b-105">ใน Power BI “รีเฟรชตอนนี้” และ “กำหนดเวลารีเฟรช” ใช้กับชุดข้อมูลที่สร้างจากไฟล์ Power BI Desktop ที่นำเข้าจากไดรฟ์ภายในเครื่องที่มีการใช้ “รับข้อมูล/ตัวแก้ไขคิวรี” เพื่อเชื่อมต่อและโหลดข้อมูลจากแหล่งข้อมูลหนึ่งจากหลายๆ แหล่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="02d0b-105">In Power BI, Refresh Now and Schedule Refresh is supported for datasets created from Power BI Desktop files imported from a local drive where Get Data/Query Editor is used to connect to and load data from any of the following data sources:</span></span>

### <a name="power-bi-gateway---personal"></a><span data-ttu-id="02d0b-106">Power BI Gateway - Personal</span><span class="sxs-lookup"><span data-stu-id="02d0b-106">Power BI Gateway - Personal</span></span>

- <span data-ttu-id="02d0b-107">แหล่งข้อมูลออนไลน์ทั้งหมดที่แสดงใน รับข้อมูลและตัวแก้ไขคิวรี ของ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="02d0b-107">All online data sources shown in Power BI Desktop’s Get Data and Query Editor.</span></span>
- <span data-ttu-id="02d0b-108">แหล่งข้อมูลภายในองค์กรทั้งหมดที่แสดงอยู่ใน รับข้อมูลและตัวแก้ไขคิวรี ของ Power BI Desktop ยกเว้นไฟล์ Hadoop (HDFS) และ Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="02d0b-108">All on-premises data sources shown in Power BI Desktop’s Get Data and Query Editor except for Hadoop file (HDFS) and Microsoft Exchange.</span></span>

<!-- Refresh Data sources-->
[!INCLUDE [refresh-datasources](../includes/refresh-datasources.md)]

> [!NOTE]
> <span data-ttu-id="02d0b-109">เกตเวย์ต้องได้รับการติดตั้ง และเรียกใช้เพื่อให้ Power BI เชื่อมต่อกับแหล่งข้อมูลภายในองค์กร และรีเฟรชชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="02d0b-109">A gateway must be installed and running in order for Power BI to connect to on-premises data sources and refresh the dataset.</span></span>
>
>

<span data-ttu-id="02d0b-110">คุณสามารถดำเนินการรีเฟรชครั้งเดียวด้วยตนเองใน Power BI Desktop ได้โดยเลือก **รีเฟรช** บนริบบอนหน้าแรก</span><span class="sxs-lookup"><span data-stu-id="02d0b-110">You can perform a one-time, manual refresh in Power BI Desktop by selecting **Refresh** on the Home ribbon.</span></span> <span data-ttu-id="02d0b-111">เมื่อคุณเลือก **รีเฟรช** ที่นี่ ข้อมูลในแบบจำลองของ *ไฟล์* จะถูกรีเฟรชด้วยข้อมูลที่อัปเดตจากแหล่งข้อมูลต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="02d0b-111">When you select **Refresh** here, the data in the *file’s* model is refreshed with updated data from the original data source.</span></span> <span data-ttu-id="02d0b-112">รีเฟรชแบบนี้ซึ่งมาจากภายในแอป Power BI Desktop แตกต่างไปจากการรีเฟรชด้วยตนเองหรือการรีเฟรชตามกำหนดการใน Power BI และเป็นสิ่งสำคัญที่ต้องทำความเข้าใจความแตกต่างนี้</span><span class="sxs-lookup"><span data-stu-id="02d0b-112">This kind of refresh, entirely from within the Power BI Desktop application itself, is different from manual or scheduled refresh in Power BI, and it’s important to understand the distinction.</span></span>

![Refresh](media/refresh-desktop-file-local-drive/pbix-refresh.png)

<span data-ttu-id="02d0b-114">เมื่อคุณนำเข้าไฟล์ Power BI Desktop ของคุณจากในไดรฟ์ภายใน ข้อมูลพร้อมกับข้อมูลอื่น ๆ ที่เกี่ยวกับรูปแบบจำลองจะถูกโหลดลงในชุดข้อมูลในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="02d0b-114">When you import your Power BI Desktop file from a local drive, data, along with other information about the model, is loaded into a dataset in the Power BI service.</span></span> <span data-ttu-id="02d0b-115">ใน Power BI service ไม่ใช่ Power BI Desktop คุณต้องการรีเฟรชข้อมูลในชุดข้อมูลเนื่องจากการรายงานของคุณจะอิง ใน Power BI service</span><span class="sxs-lookup"><span data-stu-id="02d0b-115">In the Power BI service, not Power BI Desktop, you want to refresh data in the dataset because that is what your reports, in the Power BI service, are based on.</span></span> <span data-ttu-id="02d0b-116">เนื่องจากแหล่งข้อมูลอยู่ภายนอก คุณสามารถรีเฟรชชุดข้อมูลด้วยตนเอง โดยใช้ **รีเฟรชตอนนี้** หรือคุณสามารถตั้งค่ากำหนดการรีเฟรช โดยใช้ **รีเฟรชตามกำหนดการ**</span><span class="sxs-lookup"><span data-stu-id="02d0b-116">Because the data sources are external, you can manually refresh the dataset by using **Refresh now** or you can set up a refresh schedule by using **Schedule Refresh**.</span></span>

<span data-ttu-id="02d0b-117">เมื่อคุณรีเฟรชชุดข้อมูล Power BI จะไม่มีการเชื่อมต่อไปยังไฟล์บน ไดรฟ์ในเครื่องเพื่อคิวรีให้ได้ข้อมูลที่ปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="02d0b-117">When you refresh the dataset, Power BI does not connect to the file on the local drive to query for updated data.</span></span> <span data-ttu-id="02d0b-118">Power BI ใช้ข้อมูลในชุดข้อมูลเพื่อเชื่อมต่อโดยตรงกับยังแหล่งข้อมูลเพื่อทำการคิวรีให้ได้ข้อมูลที่ปรับปรุง และจากนั้นก็โหลดข้อมูลที่ปรับปรุงแล้วลงในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="02d0b-118">It uses information in the dataset to connect directly to the data sources to query for updated data it then loads into the dataset.</span></span>

> [!NOTE]
> <span data-ttu-id="02d0b-119">ข้อมูลที่ถูกรีเฟรชในชุดข้อมูลจะไม่ถูกซิงโครไนซ์กลับไปยังไฟล์ใน ไดรฟ์ของเครืื่อง</span><span class="sxs-lookup"><span data-stu-id="02d0b-119">Refreshed data in the dataset is not synchronized back to the file on the local drive.</span></span>
>
>

## <a name="how-do-i-schedule-refresh"></a><span data-ttu-id="02d0b-120">ฉันจะกำหนดเวลารีเฟรชได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="02d0b-120">How do I schedule refresh?</span></span>

<span data-ttu-id="02d0b-121">เมื่อคุณตั้งค่ากำหนดการรีเฟรช Power BI จะเชื่อมต่อโดยตรงไปยังแหล่งข้อมูลโดยใช้ข้อมูลการเชื่อมต่อและข้อมูลประจำตัวในชุดข้อมูลเพื่อคิวรีข้อมูลที่อัปเดตแล้ว จากนั้นจึงโหลดข้อมูลที่อัปเดตแล้วลงในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="02d0b-121">When you set up a refresh schedule, Power BI connects directly to the data sources using connection information and credentials in the dataset to query for updated data, then loads the updated data into the dataset.</span></span> <span data-ttu-id="02d0b-122">การแสดงภาพด้วยข้อมูลในรายงานและแดชบอร์ดที่อิงชุดข้อมูลนั้นในบริการของ Power BI จะได้รับการอัปเดตตามไปด้วย</span><span class="sxs-lookup"><span data-stu-id="02d0b-122">Any visualizations in reports and dashboards based on that dataset in the Power BI service are also updated.</span></span>

<span data-ttu-id="02d0b-123">สำหรับรายละเอียดเกี่ยวกับวิธีการตั้งค่าการรีเฟรชตามกำหนดการ ดูที่[กำหนดค่าการรีเฟรชตามกำหนดการ](refresh-scheduled-refresh.md)</span><span class="sxs-lookup"><span data-stu-id="02d0b-123">For details on how to set up scheduled refresh, see [Configure scheduled refresh](refresh-scheduled-refresh.md).</span></span>

## <a name="when-things-go-wrong"></a><span data-ttu-id="02d0b-124">เมื่อเกิดสิ่งผิดปกติขึ้น</span><span class="sxs-lookup"><span data-stu-id="02d0b-124">When things go wrong</span></span>

<span data-ttu-id="02d0b-125">เมื่อเกิดสิ่งผิดปกติขึ้น ซึ่งโดยปกติจะเกิดเนื่องจาก Power BI ไม่สามารถลงชื่อเข้าใช้แหล่งข้อมูล หรือถ้าชุดข้อมูลเชื่อมต่อกับแหล่งข้อมูลภายในองค์กร เกตเวย์จะออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="02d0b-125">When things go wrong, it’s usually because Power BI can’t sign into data sources, or if the dataset connects to an on-premises data source, the gateway is offline.</span></span> <span data-ttu-id="02d0b-126">ตรวจสอบให้แน่ใจว่า Power BI สามารถลงชื่อเข้าใช้แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="02d0b-126">Make sure Power BI can sign into data sources.</span></span> <span data-ttu-id="02d0b-127">ถ้ามีการเปลี่ยนแปลงรหัสผ่านที่คุณลงชื่อเพื่อเข้าใช้แหล่งข้อมูล หรือ Power BI ได้รับการให้ออกจากแหล่งข้อมูล กรุณาลองลงชื่อเข้าใช้แหล่งข้อมูลของคุณอีกครั้งในข้อมูลประจำตัวของแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="02d0b-127">If a password you use to sign into a data source changes, or Power BI gets signed out from a data source, be sure to try signing into your data sources again in Data Source Credentials.</span></span>

<span data-ttu-id="02d0b-128">โปรดแน่ใจว่า ได้เลือก **ส่งอีเมลแจ้งเตือนการรีเฟรชล้มเหลวให้ฉัน**</span><span class="sxs-lookup"><span data-stu-id="02d0b-128">Be sure to leave the **Send refresh failure notification email to me** checked.</span></span> <span data-ttu-id="02d0b-129">คุณต้องทราบทันทีว่าการรีเฟรชตามกำหนดการล้มเหลวหรือไม่</span><span class="sxs-lookup"><span data-stu-id="02d0b-129">You’ll want to know right away if a scheduled refresh fails.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="02d0b-130">แนวทางการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="02d0b-130">Troubleshooting</span></span>

<span data-ttu-id="02d0b-131">การรีเฟรชข้อมูลอาจไม่เป็นไปตามที่คาดไว้ในบางครั้ง</span><span class="sxs-lookup"><span data-stu-id="02d0b-131">Sometimes refreshing data may not go as expected.</span></span> <span data-ttu-id="02d0b-132">โดยทั่วไปแล้วเป็นปัญหาที่เกี่ยวข้องกับเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="02d0b-132">Typically this is an issue connected with a gateway.</span></span> <span data-ttu-id="02d0b-133">โปรดดูที่บทความแก้ไขปัญหาเกตเวย์สำหรับเครื่องมือและปัญหาที่ทราบแล้ว</span><span class="sxs-lookup"><span data-stu-id="02d0b-133">Take a look at the gateway troubleshooting articles for tools and known issues.</span></span>

- [<span data-ttu-id="02d0b-134">การแก้ไขปัญหา เกตเวย์ข้อมูลในองค์กร</span><span class="sxs-lookup"><span data-stu-id="02d0b-134">Troubleshooting the On-premises data gateway</span></span>](service-gateway-onprem-tshoot.md)
- [<span data-ttu-id="02d0b-135">แก้ไขปัญหาเกตเวย์ Power BI - ส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="02d0b-135">Troubleshooting the Power BI Gateway - Personal</span></span>](service-admin-troubleshooting-power-bi-personal-gateway.md)

<span data-ttu-id="02d0b-136">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="02d0b-136">More questions?</span></span> [<span data-ttu-id="02d0b-137">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="02d0b-137">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
