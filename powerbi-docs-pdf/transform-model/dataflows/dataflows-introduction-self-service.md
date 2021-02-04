---
title: ข้อมูลเบื้องต้นเกี่ยวกับกระแสข้อมูลและการเตรียมข้อมูลด้วยตนเอง
description: ภาพรวมเกี่ยวกับกระแสข้อมูล Power BI คืออะไรและควรใช้เมื่อใด
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-dataflows
ms.topic: how-to
ms.date: 10/01/2020
LocalizationGroup: Data from files
ms.openlocfilehash: 5dde70b9834d990987e42c6aa945940a7f110949
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96416082"
---
# <a name="introduction-to-dataflows-and-self-service-data-prep"></a><span data-ttu-id="73666-103">ข้อมูลเบื้องต้นเกี่ยวกับกระแสข้อมูลและการเตรียมข้อมูลด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="73666-103">Introduction to dataflows and self-service data prep</span></span>

<span data-ttu-id="73666-104">เมื่อปริมาณข้อมูลเพิ่มขึ้นเรื่อยๆ ความท้าทายในการทำ Data Wrangling ให้ข้อมูลนั้นเป็นระเบียบและสามารถดำเนินการได้ก็เพิ่มขึ้นเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="73666-104">As data volume continues to grow, so does the challenge of wrangling that data into well-formed, actionable information.</span></span> <span data-ttu-id="73666-105">เราต้องการข้อมูลที่พร้อมสำหรับการวิเคราะห์ เพื่อใช้กับวิชวล รายงานและแดชบอร์ด เพื่อให้เราเปลี่ยนปริมาณข้อมูลให้เป็นข้อมูลเชิงลึกที่ดำเนินการได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="73666-105">We want data that’s ready for analytics, to populate visuals, reports, and dashboards, so we can quickly turn our volumes of data into actionable insights.</span></span> <span data-ttu-id="73666-106">ด้วยการเตรียมข้อมูลด้วยตนเอง สำหรับข้อมูลใหญ่ใน Power BI คุณสามารถเปลี่ยนข้อมูลให้เป็นข้อมูลเชิงลึกของ Power BI ได้โดยคลิกเพียงไม่กี่ครั้ง</span><span class="sxs-lookup"><span data-stu-id="73666-106">With self-service data prep for big data in Power BI, you can go from data to Power BI insights with just a few clicks.</span></span>

![กระแสของข้อมูล](media/dataflows-introduction-self-service-flow.png)

## <a name="when-to-use-dataflows"></a><span data-ttu-id="73666-108">คุณควรใช้กระแสข้อมูลเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="73666-108">When to use dataflows</span></span>

<span data-ttu-id="73666-109">กระแสข้อมูลได้รับการออกแบบมาเพื่อรองรับสถานการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="73666-109">Dataflows are designed to support the following scenarios:</span></span>

* <span data-ttu-id="73666-110">สร้างตรรกะการแปลงข้อมูลที่นำมาใช้ใหม่ได้ ซึ่งคุณสามารถแชร์กับชุดข้อมูลและรายงานจำนวนมากภายใน Power BI</span><span class="sxs-lookup"><span data-stu-id="73666-110">Create reusable transformation logic that can be shared by many datasets and reports inside Power BI.</span></span> <span data-ttu-id="73666-111">กระแสข้อมูลส่งเสริมความสามารถในการนำมาใช้ใหม่ขององค์ประกอบข้อมูลเบื้องต้น ทำให้ไม่จำเป็นต้องสร้างการเชื่อมต่อแยกกับระบบคลาวด์หรือแหล่งข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="73666-111">Dataflows promote reusability of the underlying data elements, preventing the need to create separate connections with your cloud or on-premise data sources.</span></span>

* <span data-ttu-id="73666-112">เปิดเผยข้อมูลในที่เก็บข้อมูล Azure Data Lake Gen 2 ของคุณเอง ทำให้คุณสามารถเชื่อมต่อบริการ Azure อื่น ๆ กับข้อมูลเบื้องต้นที่เป็นข้อมูลดิบได้</span><span class="sxs-lookup"><span data-stu-id="73666-112">Expose the data in your own Azure Data Lake Gen 2 storage, enabling you to connect other Azure services to the raw underlying data.</span></span>

* <span data-ttu-id="73666-113">สร้างแหล่งที่มาจริงเพียงแหล่งเดียวโดยบังคับให้นักวิเคราะห์เชื่อมต่อกับกระแสข้อมูล แทนที่จะเชื่อมต่อกับระบบเบื้องต้น ให้คุณควบคุมได้ว่าจะเข้าถึงข้อมูลใดและจะเปิดเผยข้อมูลอย่างไรกับผู้สร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="73666-113">Create a single source of the truth by forcing analysts to connect to the dataflows, rather than connecting to the underlying systems, providing you with control over which data is accessed, and how data is exposed to report creators.</span></span> <span data-ttu-id="73666-114">นอกจากนี้ คุณยังสามารถแมปข้อมูลกับข้อกำหนดมาตรฐานอุตสาหกรรม ทำให้คุณสามารถสร้างมุมมองที่ดูแลจัดการอย่างเป็นระเบียบเรียบร้อย ซึ่งสามารถทำงานร่วมกับบริการและผลิตภัณฑ์อื่น ๆ ใน Power Platform ได้</span><span class="sxs-lookup"><span data-stu-id="73666-114">You can also map the data to industry standard definitions, enabling you to create tidy curated views, which can work with other services and products in the Power Platform.</span></span>

* <span data-ttu-id="73666-115">ถ้าคุณต้องการทำงานกับปริมาณข้อมูลขนาดใหญ่และดำเนินการ ETL ในระดับมาตราส่วน กระแสข้อมูลที่มีมาตราส่วน Power BI Premium มีประสิทธิภาพมากกว่าและช่วยให้คุณมีความยืดหยุ่นมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="73666-115">If you want to work with large data volumes and perform ETL at scale, dataflows with Power BI Premium scales more efficiently and gives you more flexibility.</span></span> <span data-ttu-id="73666-116">กระแสข้อมูลสนับสนุนระบบคลาวด์และแหล่งข้อมูลภายในองค์กรที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="73666-116">Dataflows supports a wide range of cloud and on-premise sources.</span></span> 

* <span data-ttu-id="73666-117">ป้องกันไม่ให้นักวิเคราะห์เข้าถึงแหล่งข้อมูลเบื้องต้นได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="73666-117">Prevent analysts from having direct access to the underlying data source.</span></span> <span data-ttu-id="73666-118">เนื่องจากผู้สร้างรายงานสามารถสร้างส่วนบนของกระแสข้อมูลได้ จึงอาจสะดวกกว่าสำหรับคุณในการอนุญาตให้บุคคลเพียงไม่กี่คนเข้าถึงแหล่งข้อมูลเบื้องต้นได้ จากนั้นจึงให้การเข้าถึงกระแสข้อมูลเพื่อให้นักวิเคราะห์สร้างขึ้นอยู่ด้านบน</span><span class="sxs-lookup"><span data-stu-id="73666-118">Since report creators can build on top of dataflows, it may be more convenient for you to allow access to underlying data sources only to a few individuals, and then provide access to the dataflows for analysts to build on top of.</span></span> <span data-ttu-id="73666-119">วิธีนี้ช่วยลดภาระให้กับระบบเบื้องต้นและช่วยให้ผู้ดูแลระบบสามารถควบคุมได้ดียิ่งขึ้นเมื่อระบบโหลดจากการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="73666-119">This approach reduces the load to the underlying systems, and gives administrators finer control of when the systems get loaded from refreshes.</span></span>

<span data-ttu-id="73666-120">เมื่อคุณได้สร้างกระแสข้อมูล คุณจะสามารถใช้ Power BI Desktop และบริการของ Power BI เพื่อสร้างชุดข้อมูล รายงาน แดชบอร์ด และแอปที่ใช้ประโยชน์จาก Common Data Model เพื่อขับเคลื่อนข้อมูลเชิงลึกให้กับกิจกรรมทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="73666-120">Once you’ve created a dataflow, you can use Power BI Desktop and the Power BI service to create datasets, reports, dashboards, and apps that leverage the Common Data Model to drive deep insights into your business activities.</span></span> <span data-ttu-id="73666-121">การวางกำหนดการรีเฟรชกระแสข้อมูลได้รับการจัดการโดยตรงจากพื้นที่ทำงานที่ใช้สร้างกระแสข้อมูล เช่นเดียวกับชุดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="73666-121">Dataflow refresh scheduling is managed directly from the workspace in which your dataflow was created, just like your datasets.</span></span>

## <a name="next-steps"></a><span data-ttu-id="73666-122">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="73666-122">Next steps</span></span>
<span data-ttu-id="73666-123">บทความนี้ใช้ภาพรวมของการเตรียมข้อมูลด้วยตนเองสำหรับข้อมูลขนาดใหญ่ใน Power BI และวิธีการใช้งานหลายวิธี</span><span class="sxs-lookup"><span data-stu-id="73666-123">This article provided an overview of self-service data prep for big data in Power BI, and the many ways you can use it.</span></span> 

<span data-ttu-id="73666-124">บทความต่อไปนี้ให้ข้อมูลเพิ่มเติมเกี่ยวกับกระแสข้อมูลและ Power BI:</span><span class="sxs-lookup"><span data-stu-id="73666-124">The following articles provide more information about dataflows and Power BI:</span></span>

* [<span data-ttu-id="73666-125">การสร้างกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="73666-125">Creating a dataflow</span></span>](dataflows-create.md)
* [<span data-ttu-id="73666-126">กำหนดค่าและใช้กระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="73666-126">Configure and consume a dataflow</span></span>](dataflows-configure-consume.md)
* [<span data-ttu-id="73666-127">การกำหนดค่าที่จัดเก็บกระแสข้อมูลเพื่อใช้ Azure Data Lake Gen 2</span><span class="sxs-lookup"><span data-stu-id="73666-127">Configuring Dataflow storage to use Azure Data Lake Gen 2</span></span>](dataflows-azure-data-lake-storage-integration.md)
* [<span data-ttu-id="73666-128">ฟีเจอร์พรีเมียมของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="73666-128">Premium features of dataflows</span></span>](dataflows-premium-features.md)
* [<span data-ttu-id="73666-129">AI กับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="73666-129">AI with dataflows</span></span>](dataflows-machine-learning-integration.md)
* [<span data-ttu-id="73666-130">ข้อจำกัดและข้อควรพิจารณาของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="73666-130">Dataflows limitations and considerations</span></span>](dataflows-features-limitations.md)
* [<span data-ttu-id="73666-131">แนวทางปฏิบัติที่ดีที่สุดสำหรับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="73666-131">Dataflows best practices</span></span>](dataflows-best-practices.md)


<span data-ttu-id="73666-132">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Common Data Model สามารถดูได้ในบทความภาพรวม:</span><span class="sxs-lookup"><span data-stu-id="73666-132">For more information about the Common Data Model, you can read its overview article:</span></span>
* [<span data-ttu-id="73666-133">Common Data Model - ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="73666-133">Common Data Model - overview</span></span>](/powerapps/common-data-model/overview)