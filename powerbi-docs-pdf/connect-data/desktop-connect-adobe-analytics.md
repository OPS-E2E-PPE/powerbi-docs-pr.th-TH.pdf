---
title: เชื่อมต่อกับ Adobe Analytics ใน Power BI Desktop
description: เชื่อมต่อและใช้งาน Adobe Analytics ใน Power BI Desktop ได้อย่างง่ายดาย
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 05/07/2019
LocalizationGroup: Connect to data
ms.openlocfilehash: 89376902f1c37526ddf9376461871bcf27c2566d
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411505"
---
# <a name="connect-to-adobe-analytics-in-power-bi-desktop"></a><span data-ttu-id="ce331-103">เชื่อมต่อกับ Adobe Analytics ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ce331-103">Connect to Adobe Analytics in Power BI Desktop</span></span> 
<span data-ttu-id="ce331-104">ใน **Power BI Desktop** คุณสามารถเชื่อมต่อกับ **Adobe Analytics** และใช้ข้อมูลเบื้องต้นเช่นเดียวกับแหล่งข้อมูลอื่นใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="ce331-104">In **Power BI Desktop**, you can connect to **Adobe Analytics** and use the underlying data just like any other data source in Power BI Desktop.</span></span> 

![รับข้อมูลจาก Adobe Analytics](media/desktop-connect-adobe-analytics/connect-adobe-analytics_01.png)

## <a name="connect-to-adobe-analytics-data"></a><span data-ttu-id="ce331-106">เชื่อมต่อกับข้อมูล Adobe Analytics</span><span class="sxs-lookup"><span data-stu-id="ce331-106">Connect to Adobe Analytics data</span></span>
<span data-ttu-id="ce331-107">เพื่อเชื่อมต่อกับข้อมูล **Adobe Analytics** เลือก **รับข้อมูล** จาก ribbon **หน้าแรก** ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ce331-107">To connect to **Adobe Analytics** data, select **Get Data** from the **Home** ribbon in Power BI Desktop.</span></span> <span data-ttu-id="ce331-108">เลือก **บริการออนไลน์** จากประเภททางด้านซ้าย แล้วคุณจะเห็น **ตัวเชื่อมต่อ Adobe Analytics**</span><span class="sxs-lookup"><span data-stu-id="ce331-108">Select **Online Services** from the categories on the left, and you see **Adobe Analytics connector**.</span></span>

![รับข้อมูลจาก Adobe Analytics](media/desktop-connect-adobe-analytics/connect-adobe-analytics_01.png)

<span data-ttu-id="ce331-110">ในหน้าต่าง **Adobe Analytics** ที่ปรากฎขึ้น เลือกปุ่ม **ลงชื่อเข้าใช้** และระบุข้อมูลประจำตัวของคุณเพื่อลงชื่อเข้าใช้บัญชี Adobe Analytics ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ce331-110">In the **Adobe Analytics** window that appears, select the **Sign in** button, and provide your credentials to sign in to your Adobe Analytics account.</span></span> <span data-ttu-id="ce331-111">หน้าต่างลงชื่อเข้าใช้ Adobe จะปรากฏขึ้น ดังที่แสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ce331-111">The Adobe sign in window appears, as shown in the following image.</span></span>

![ลงชื่อเข้าใช้ Adobe Analytics](media/desktop-connect-adobe-analytics/connect-adobe-analytics_03.png)

<span data-ttu-id="ce331-113">เมื่อได้รับการถาม ให้ใส่ชื่อผู้ใช้และรหัสผ่านของคุณ</span><span class="sxs-lookup"><span data-stu-id="ce331-113">When prompted, put in your username and password.</span></span> <span data-ttu-id="ce331-114">ทันทีที่การเชื่อมต่อสำเร็จ คุณสามารถดูตัวอย่างและเลือกมิติและหน่วยวัดต่าง ๆ ภายในกล่องโต้ตอบ **ตัวนำทาง** Power BI เพื่อสร้างผลลัพธ์หนึ่งตาราง</span><span class="sxs-lookup"><span data-stu-id="ce331-114">Once the connection is established, you can preview and select multiple dimensions and measures within the Power BI **Navigator** dialog to create a single tabular output.</span></span> <span data-ttu-id="ce331-115">คุณยังสามารถใส่ค่าพารามิเตอร์ใด ๆ ที่จำเป็นสำหรับรายการที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="ce331-115">You can also provide any necessary input parameters required for the selected items.</span></span> 

![เลือกข้อมูลโดยใช้ตัวนำทาง](media/desktop-connect-adobe-analytics/connect-adobe-analytics_04.png)

<span data-ttu-id="ce331-117">คุณสามารถ **โหลด** ตารางที่เลือก ซึ่งจะรวมทั้งตารางลง ใน **Power BI Desktop** หรือคุณสามารถ **แก้ไข** คิวรี ซึ่งจะเปิด **ตัวแก้ไขคิวรี** เพื่อให้คุณสามารถกรองและปรับปรุงชุดข้อมูลที่ต้องการใช้ จากนั้นโหลดชุดข้อมูลที่ปรับปรุงแล้วลงใน **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="ce331-117">You can **Load** the selected table, which brings the entire table into **Power BI Desktop**, or you can **Edit** the query, which opens **Query Editor** so you can filter and refine the set of data you want to use, and then load that refined set of data into **Power BI Desktop**.</span></span>

![โหลดหรือแก้ไขข้อมูลในตัวนำทาง](media/desktop-connect-adobe-analytics/connect-adobe-analytics_05.png)


## <a name="next-steps"></a><span data-ttu-id="ce331-119">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="ce331-119">Next steps</span></span>
<span data-ttu-id="ce331-120">มีข้อมูลหลากหลายประเภทที่คุณสามารถเชื่อมต่อโดยใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ce331-120">There are all sorts of data you can connect to using Power BI Desktop.</span></span> <span data-ttu-id="ce331-121">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแหล่งข้อมูล โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ce331-121">For more information on data sources, check out the following resources:</span></span>

* [<span data-ttu-id="ce331-122">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="ce331-122">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="ce331-123">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ce331-123">Data Sources in Power BI Desktop</span></span>](desktop-data-sources.md)
* [<span data-ttu-id="ce331-124">จัดรูปทรง และรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ce331-124">Shape and Combine Data with Power BI Desktop</span></span>](desktop-shape-and-combine-data.md)
* [<span data-ttu-id="ce331-125">เชื่อมต่อกับเวิร์กบุ๊ก Excel ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ce331-125">Connect to Excel workbooks in Power BI Desktop</span></span>](desktop-connect-excel.md)   
* [<span data-ttu-id="ce331-126">ใส่ข้อมูลลงใน Power BI Desktop โดยตรง</span><span class="sxs-lookup"><span data-stu-id="ce331-126">Enter data directly into Power BI Desktop</span></span>](desktop-enter-data-directly-into-desktop.md)   
