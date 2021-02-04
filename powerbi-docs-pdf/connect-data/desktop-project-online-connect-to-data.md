---
title: 'Project Online: เชื่อมต่อกับข้อมูลผ่านทาง Power BI Desktop'
description: 'Project Online: เชื่อมต่อกับข้อมูลผ่านทาง Power BI Desktop'
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 04/01/2020
LocalizationGroup: Connect to data
ms.openlocfilehash: b6078a2122a77682af328f9935b23da0d0d0d945
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96404950"
---
# <a name="connect-to-project-online-data-through-power-bi-desktop"></a><span data-ttu-id="f005d-103">เชื่อมต่อกับข้อมูล Project Online ผ่าน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="f005d-103">Connect to Project Online data through Power BI Desktop</span></span>
<span data-ttu-id="f005d-104">คุณสามารถเชื่อมต่อไปยังข้อมูลใน Project Online ผ่านทาง Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="f005d-104">You can connect to data in Project Online through Power BI Desktop.</span></span>

## <a name="step-1-download-power-bi-desktop"></a><span data-ttu-id="f005d-105">ขั้นตอนที่ 1: ดาวน์โหลด Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="f005d-105">Step 1: Download Power BI Desktop</span></span>
1. <span data-ttu-id="f005d-106">[ดาวน์โหลด Power BI Desktop](https://go.microsoft.com/fwlink/?LinkID=521662) แล้วเรียกใช้ตัวติดตั้งเพื่อรับ **Power BI Desktop** บนคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f005d-106">[Download Power BI Desktop](https://go.microsoft.com/fwlink/?LinkID=521662), then run the installer to get **Power BI Desktop** on your computer.</span></span>

## <a name="step-2-connect-to-project-online-with-odata"></a><span data-ttu-id="f005d-107">ขั้นตอนที่ 2: เชื่อมต่อกับ Project Online ด้วย OData</span><span class="sxs-lookup"><span data-stu-id="f005d-107">Step 2: Connect to Project Online with OData</span></span>
1. <span data-ttu-id="f005d-108">เปิด **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="f005d-108">Open **Power BI Desktop**.</span></span>
2. <span data-ttu-id="f005d-109">บนหน้าจอ *ยินดีต้อนรับ* เลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="f005d-109">On the *Welcome* screen, select **Get Data**.</span></span>
3. <span data-ttu-id="f005d-110">เลือก **ตัวดึงข้อมูล OData** และเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="f005d-110">Choose **OData feed** and select **Connect**.</span></span>
4. <span data-ttu-id="f005d-111">ใส่ที่อยู่ของตัวดึงข้อมูล OData ของคุณในกล่อง URL แล้ว คลิกตกลง</span><span class="sxs-lookup"><span data-stu-id="f005d-111">Enter the address for your OData feed in the URL box, and then click OK.</span></span>
   
   <span data-ttu-id="f005d-112">หากที่อยู่สำหรับไซต์ Project Web App ของคุณเป็นรูปแบบ *https://\<tenantname\>.sharepoint.com/sites/pwa* จากนั้นที่อยู่ที่คุณจะป้อนใส่สำหรับฟีด OData ของคุณคือ *https://\<tenantname\>.sharepoint.com/sites/pwa/\_api/Projectdata*</span><span class="sxs-lookup"><span data-stu-id="f005d-112">If the address for your Project Web App site resembles *https://\<tenantname\>.sharepoint.com/sites/pwa*, then the address you’ll enter for your OData Feed is *https://\<tenantname\>.sharepoint.com/sites/pwa/\_api/Projectdata*.</span></span>
   
   <span data-ttu-id="f005d-113">สำหรับตัวอย่าง เรากำลังใช้:</span><span class="sxs-lookup"><span data-stu-id="f005d-113">For our example, we’re using:</span></span>

    `https://contoso.sharepoint.com/sites/pwa/default.aspx`

5. <span data-ttu-id="f005d-114">Power BI Desktop จะพร้อมท์ให้คุณรับรองสิทธิ์กับบัญชีที่ทำงานหรือบัญชีโรงเรียนของคุณ</span><span class="sxs-lookup"><span data-stu-id="f005d-114">Power BI Desktop will prompt you to authenticate with your work or school account.</span></span> <span data-ttu-id="f005d-115">เลือกบัญชีผู้ใช้ขององค์กร แล้วใส่ข้อมูลประจำตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="f005d-115">Select Organizational account and then enter your credentials.</span></span>
   
   ![ภาพหน้าจอของ Power BI Desktop ที่แสดงพรอมท์ข้อมูลประจำตัวเพื่อเชื่อมต่อ](media/desktop-project-online-connect-to-data/image.png)

<span data-ttu-id="f005d-117">บัญชีที่คุณใช้เพื่อเชื่อมต่อกับตัวดึงข้อมูล OData อย่างน้อยต้องมีตัวแสดงพอร์ตโครงการเพื่อข้าถึงไซต์ Project Web App</span><span class="sxs-lookup"><span data-stu-id="f005d-117">The account you use to connect to the OData feed must have at least Portfolio Viewer access to the Project Web App site.</span></span> 

<span data-ttu-id="f005d-118">จากที่นี่ คุณสามารถเลือกตารางที่คุณต้องการจะเชื่อมต่อและสร้างแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="f005d-118">From here, you can choose which tables you would like to connect to and build a query.</span></span>  <span data-ttu-id="f005d-119">อยากทราบวิธีการเริ่มต้นใช้งานใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="f005d-119">Want an idea of how to get started?</span></span>  <span data-ttu-id="f005d-120">โพสต์ในบล็อกต่อไปนี้จะแสดงวิธีการสร้างแผนภูมิการวัดความก้าวหน้าจากข้อมูล Project Online ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f005d-120">The following blog post shows how to build a burn down chart from your Project Online data.</span></span>  <span data-ttu-id="f005d-121">โพสต์ในบล็อกจะอ้างอิงเกี่ยวกับการใช้ Power Query เพื่อเชื่อมต่อกับ Project Online แต่ยังสามารถใช้กับ Power BI Desktop ได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="f005d-121">The blog post refers to using Power Query to connect to Project Online, but this applies to Power BI Desktop as well.</span></span>

[<span data-ttu-id="f005d-122">สร้างแผนภูมิการวัดความก้าวหน้าสำหรับโครงการโดยใช้ Power Pivot และ Power Query</span><span class="sxs-lookup"><span data-stu-id="f005d-122">Creating burn down charts for Project using Power Pivot and Power Query</span></span>](https://blogs.office.com/2014/03/24/creating-burndown-charts-for-project-using-power-pivot-and-power-query/)

