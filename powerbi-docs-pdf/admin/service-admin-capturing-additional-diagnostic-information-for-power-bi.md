---
title: การจับข้อมูลการวินิจฉัยเพิ่มเติม
description: คำแนะนำนี้ ให้สองทางเลือกในการรวบรวมข้อมูลเพิ่มเติมเพื่อการวินิจฉัยจาก เว็บไคลเอ็นต์ Power BI
author: kfollis
ms.author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 09/17/2019
ms.custom: seodec18
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 856eb4ca9b8c8afab90d351b5a025c2198b393b1
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413736"
---
# <a name="capture-additional-diagnostic-information-for-power-bi"></a><span data-ttu-id="4a466-103">จับข้อมูลการวินิจฉัยเพิ่มเติมสำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="4a466-103">Capture additional diagnostic information for Power BI</span></span>

<span data-ttu-id="4a466-104">บทความนี้ ให้ข้อมูลที่ได้ในการรวบรวมเพิ่มเติมเพื่อการวินิจฉัยจาก เว็บไคลเอ็นต์ Power BI</span><span class="sxs-lookup"><span data-stu-id="4a466-104">This article provides instructions for manually collecting additional diagnostic information from the Power BI web client.</span></span>

1. <span data-ttu-id="4a466-105">เรียกดู [Power BI](https://app.powerbi.com) ด้วย Microsoft Edge หรือ Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="4a466-105">Browse to [Power BI](https://app.powerbi.com) with Microsoft Edge or Internet Explorer.</span></span>

1. <span data-ttu-id="4a466-106">กด **F12** เพื่อเปิดเครื่องมือสำหรับนักพัฒนา Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4a466-106">Press **F12** to open the Microsoft Edge developer tools.</span></span>

   ![ภาพหน้าจอของแท็บองค์ประกอบเครื่องมือสำหรับนักพัฒนา Microsoft Edge](media/service-admin-capturing-additional-diagnostic-information-for-power-bi/edge-developer-tools.png)

1. <span data-ttu-id="4a466-108">เลือกแท็บ **เครือข่าย** จะแสดงรายการข้อมูลเครือข่ายที่ดักจับได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="4a466-108">Select the **Network** tab. It will list traffic it has already captured.</span></span>

   ![ภาพหน้าจอของแท็บเครือข่ายเครื่องมือสำหรับนักพัฒนา Microsoft Edge](media/service-admin-capturing-additional-diagnostic-information-for-power-bi/edge-network-tab.png)

    <span data-ttu-id="4a466-110">คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="4a466-110">You can:</span></span>

    * <span data-ttu-id="4a466-111">เรียกดูภายในหน้าต่าง และจำลองปัญหาใดก็ได้ที่คุณกำลังเจออยู่</span><span class="sxs-lookup"><span data-stu-id="4a466-111">Browse within the window and reproduce any problem you may come across.</span></span>

    * <span data-ttu-id="4a466-112">ซ่อนและแสดงหน้าต่าง เครื่องมือสำหรับนักพัฒนา ตลอดเวลาระหว่างเซสชัน โดยการกด F12</span><span class="sxs-lookup"><span data-stu-id="4a466-112">Hide and show the developer tools window at any time during the session by pressing F12.</span></span>

1. <span data-ttu-id="4a466-113">เมื่อต้องหยุดการการสร้างโปรไฟล์เซสซันคุณสามารถเลือกสี่เหลี่ยมสีแดงบนแท็บ **เครือข่าย** ในบริเวณของเครื่องมือสำหรับนักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="4a466-113">To stop profiling the session, you can select the red square on the **Network** tab of the developer tools area.</span></span>

   ![ภาพหน้าจอของแท็บเครือข่ายของเครื่องมือสำหรับนักพัฒนา Microsoft Edge ที่มีคำอธิบายภาพสำหรับไอคอนหยุด](media/service-admin-capturing-additional-diagnostic-information-for-power-bi/edge-network-tab-stop.png)

1. <span data-ttu-id="4a466-115">เลือกไอคอนดิสก์เพื่อส่งออกข้อมูลเป็นไฟล์ที่เก็บถาวรของ HTTP (ฮาร์)</span><span class="sxs-lookup"><span data-stu-id="4a466-115">Select the diskette icon to export the data as an HTTP Archive (HAR) file.</span></span>

   ![ภาพหน้าจอของแท็บเครือข่ายของเครื่องมือสำหรับนักพัฒนา Microsoft Edge ที่มีคำอธิบายภาพสำหรับไอคอนแผ่นดิสก์](media/service-admin-capturing-additional-diagnostic-information-for-power-bi/edge-network-tab-save.png)

1. <span data-ttu-id="4a466-117">ใส่ชื่อไฟล์ และบันทึกไฟล์ HAR</span><span class="sxs-lookup"><span data-stu-id="4a466-117">Provide a file name and save the HAR file.</span></span>

    <span data-ttu-id="4a466-118">ไฟล์ HAR จะประกอบด้วยข้อมูลทั้งหมดเกี่ยวกับคำขอเครือข่าย ระหว่างหน้าต่างเบราว์เซอร์และ Power BI ซึ่งรวมไปถึง:</span><span class="sxs-lookup"><span data-stu-id="4a466-118">The HAR file will contain all the information about network requests between the browser window and Power BI including:</span></span>

    * <span data-ttu-id="4a466-119">ID กิจกรรมสำหรับการร้องขอแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="4a466-119">The activity IDs for each request.</span></span>

    * <span data-ttu-id="4a466-120">ประทับเวลาที่แม่นยำสำหรับการร้องขอแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="4a466-120">The precise timestamp for each request.</span></span>

    * <span data-ttu-id="4a466-121">ข้อมูลข้อผิดพลาดใดๆที่ส่งกลับไปยังไคลเอ็นต์</span><span class="sxs-lookup"><span data-stu-id="4a466-121">Any error information returned to the client.</span></span>

    <span data-ttu-id="4a466-122">แฟ้มการติดตามที่ได้ ยังประกอบด้วยข้อมูลที่ใช้เพื่อแสดงภาพบนหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="4a466-122">This trace will also contain the data used to populate the visuals shown on the screen.</span></span>

1. <span data-ttu-id="4a466-123">คุณสามารถส่งไฟล์ HAR ให้ฝ่ายสนับสนุนสำหรับตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="4a466-123">You can provide the HAR file to support for review.</span></span>

<span data-ttu-id="4a466-124">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4a466-124">More questions?</span></span> [<span data-ttu-id="4a466-125">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="4a466-125">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
