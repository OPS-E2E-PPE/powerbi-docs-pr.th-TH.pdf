---
title: เชื่อมต่อกับข้อมูลที่สร้างขึ้นโดย Power Platform กระแสข้อมูลใน Power BI Desktop
description: เชื่อมต่อและใช้กระแสข้อมูลใน Power BI Desktop ได้อย่างง่ายดาย
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-dataflows
ms.topic: how-to
ms.date: 10/01/2020
LocalizationGroup: Connect to data
ms.openlocfilehash: 5d9f477c8b058dbe9a71eec1307b4a32863307a1
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96392967"
---
# <a name="connect-to-data-created-by-power-platform-dataflows-in-power-bi-desktop"></a><span data-ttu-id="5f88f-103">เชื่อมต่อกับข้อมูลที่สร้างขึ้นโดย Power Platform กระแสข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="5f88f-103">Connect to data created by Power Platform dataflows in Power BI Desktop</span></span>
<span data-ttu-id="5f88f-104">ใน **Power BI Desktop** คุณสามารถเชื่อมต่อกับ **กระแสข้อมูล Power Platform** เช่นเดียวกับแหล่งข้อมูลอื่นใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="5f88f-104">In **Power BI Desktop**, you can connect to data created by **Power Platform dataflows** just like any other data source in Power BI Desktop.</span></span>

![เชื่อมต่อกับกระแสข้อมูล](media/desktop-connect-dataflows/connect-dataflows_01.png)

<span data-ttu-id="5f88f-106">ตัวเชื่อมต่อ **กระแสข้อมูล Power Platform** จะให้คุณได้เชื่อมต่อกับเอนทิตีที่สร้างโดยกระแสข้อมูลในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="5f88f-106">The **Power Platform dataflows** connector lets you connect to entities created by dataflows in the Power BI service.</span></span> 

## <a name="considerations-and-limitations"></a><span data-ttu-id="5f88f-107">ข้อควรพิจารณาและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="5f88f-107">Considerations and limitations</span></span>

<span data-ttu-id="5f88f-108">หากต้องการใช้ **ตัวเชื่อมต่อกระแสข้อมูล Power Platform** คุณต้องใช้ **Power BI Desktop** รุ่นล่าสุด</span><span class="sxs-lookup"><span data-stu-id="5f88f-108">To use the **Power Platform dataflows connector**, you must be running a recent version of **Power BI Desktop**.</span></span> <span data-ttu-id="5f88f-109">คุณสามารถ[ดาวน์โหลด Power BI Desktop](../fundamentals/desktop-get-the-desktop.md) ได้ทุกเมื่อ และติดตั้งบนคอมพิวเตอร์ของคุณ เพื่อให้แน่ใจว่าคุณมีรุ่นล่าสุด</span><span class="sxs-lookup"><span data-stu-id="5f88f-109">You can always [download Power BI Desktop](../fundamentals/desktop-get-the-desktop.md) and install it on your computer to ensure you have the most recent version.</span></span>  

> [!NOTE]
> <span data-ttu-id="5f88f-110">ตัวเชื่อมต่อกระแสข้อมูล Power Platform เวอร์ชันก่อนหน้ากำหนดให้คุณดาวน์โหลดไฟล์ .MEZ และวางไว้ในโฟลเดอร์</span><span class="sxs-lookup"><span data-stu-id="5f88f-110">The previous version of the Power Platform dataflows connector required that you download a .MEZ file and place it in a folder.</span></span> <span data-ttu-id="5f88f-111">**Power BI Desktop** เวอร์ชันปัจจุบันมีตัวเชื่อมต่อกระแสข้อมูล Power Platform เพื่อไม่ต้องใช้ไฟล์นั้นอีกต่อไปและไม่ให้เกิดปัญหากับตัวเชื่อมต่อเวอร์ชันที่รวมมาด้วย</span><span class="sxs-lookup"><span data-stu-id="5f88f-111">Current versions of **Power BI Desktop** include the Power Platform dataflows connector, so that file is no longer required and can cause conflicts with the included version of the connector.</span></span> <span data-ttu-id="5f88f-112">หาคุณวางไฟล์ .MEZ ไว้ในโฟลเดอร์ด้วยตัวเอง คุณ *ต้อง* ลบไฟล์ .MEZ ที่ดาวน์โหลดมาออกจากโฟลเดอร์ **เอกสาร > Power BI Desktop > ตัวเชื่อมต่อแบบกำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="5f88f-112">If you manually placed that .MEZ file into the folder, you *must* delete that downloaded .MEZ file from your **Documents > Power BI Desktop > Custom connectors** folder to avoid conflicts.</span></span> 

## <a name="desktop-performance"></a><span data-ttu-id="5f88f-113">ประสิทธิภาพการทำงานของ Desktop</span><span class="sxs-lookup"><span data-stu-id="5f88f-113">Desktop performance</span></span>
<span data-ttu-id="5f88f-114">**Power BI Desktop** ทำงานภายในเครื่องบนคอมพิวเตอร์ที่มีติดตั้งโปรแกรมเอาไว้</span><span class="sxs-lookup"><span data-stu-id="5f88f-114">**Power BI Desktop** runs locally on the computer on which it is installed.</span></span> <span data-ttu-id="5f88f-115">ประสิทธิภาพการรวบรวมของกระแสข้อมูลถูกกำหนดโดยปัจจัยหลายอย่าง</span><span class="sxs-lookup"><span data-stu-id="5f88f-115">Ingestion performance of dataflows is determined by a variety of factors.</span></span> <span data-ttu-id="5f88f-116">ซึ่งปัจจัยเหล่านั้นประกอบไปด้วย ขนาดของข้อมูล, CPU และ RAM ของคอมพิวเตอร์, แบนด์วิดท์เครือข่าย, ระยะห่างจากศูนย์ข้อมูล และปัจจัยอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="5f88f-116">Those factors include the size of the data, your computer's CPU and RAM, network bandwidth, distance form the data center, and other factors.</span></span>

<span data-ttu-id="5f88f-117">คุณสามารถปรับปรุงประสิทธิภาพการรวบรวมข้อมูลสำหรับกระแสข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="5f88f-117">You can improve data ingestion performance for dataflows.</span></span> <span data-ttu-id="5f88f-118">ตัวอย่างเช่น ถ้าขนาดของข้อมูลที่รวบรวมนั้นใหญ่เกินกว่าที่ **Power BI Desktop** จะจัดการได้ในคอมพิวเตอร์ คุณอาจใช้เอนทิตีที่เชื่อมโยงและเอนทิตีที่คำนวณในกระแสข้อมูลเพื่อรวมข้อมูลนั้น (ภายในกระแสข้อมูล) แล้วเลือกดึงเอาเฉพาะข้อมูลที่รวมและเตรียมไว้ก่อนแล้ว</span><span class="sxs-lookup"><span data-stu-id="5f88f-118">For example, if the ingested data size is too large for **Power BI Desktop** to manage on your computer, you can use linked and computed entities in dataflows to aggregate the data (within dataflows) and ingest only the pre-prepared, aggregated data.</span></span> 

<span data-ttu-id="5f88f-119">เมื่อทำเช่นนั้น การประมวลผลข้อมูลขนาดใหญ่จะดำเนินการออนไลน์ในกระแสข้อมูล แทนที่จะดำเนินการภายในอินสแตนซ์ที่ทำงานอยู่ของ **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="5f88f-119">In that manner, the processing of large data is performed online in dataflows, rather than being performed locally in your running instance of **Power BI Desktop**.</span></span> <span data-ttu-id="5f88f-120">วิธีนั้นจะทำให้ Power BI Desktop รวบรวมข้อมูลได้ในขนาดที่เล็กลง และรักษาการใช้งานที่มีกระแสข้อมูลให้ตอบสนองรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="5f88f-120">That approach lets Power BI Desktop ingest smaller amounts of data, and keeps the experience with dataflows responsive and quick.</span></span>

## <a name="additional-considerations"></a><span data-ttu-id="5f88f-121">ข้อควรพิจารณาเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5f88f-121">Additional considerations</span></span>

<span data-ttu-id="5f88f-122">กระแสข้อมูลส่วนใหญ่อยู่ในผู้เช่าบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="5f88f-122">Most dataflows reside in the Power BI service tenant.</span></span> <span data-ttu-id="5f88f-123">อย่างไรก็ตาม ผู้ใช้ **Power BI Desktop** ไม่สามารถเข้าถึงกระแสข้อมูล ที่จัดเก็บในบัญชี Azure Data Lake Storage Gen2 เว้นแต่ว่าพวกเขาเป็นเจ้าของกระแสข้อมูล หรือได้รับอนุญาตอย่างถูกต้องให้เข้าถึงโฟลเดอร์ CDM ของ กระแสข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="5f88f-123">However, **Power BI Desktop** users cannot access dataflows that are stored in Azure Data Lake Storage Gen2 account, unless they are the owner of the dataflow, or they have been explicitly authorized to the dataflow’s CDM folder.</span></span> <span data-ttu-id="5f88f-124">พิจารณาสถานการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5f88f-124">Consider the following situation:</span></span>

1.  <span data-ttu-id="5f88f-125">แอนนาสร้างพื้นที่ทำงานใหม่และกำหนดค่าเพื่อจัดเก็บกระแสข้อมูลในทะเลสาบข้อมูล (Data Lake) ขององค์กร</span><span class="sxs-lookup"><span data-stu-id="5f88f-125">Anna creates a new workspace and configures it to store dataflows in the organization’s data lake.</span></span>
2.  <span data-ttu-id="5f88f-126">เบน (สมาชิกคนหนึ่งของพื้นที่ทำงานที่แอนนาสร้าง) ต้องการใช้ Power BI Desktop และตัวเชื่อมต่อกระแสข้อมูลเพื่อรับข้อมูลจากกระแสข้อมูลที่ แอนนาสร้าง</span><span class="sxs-lookup"><span data-stu-id="5f88f-126">Ben, who is also a member of the workspace Anna created, wants to use Power BI Desktop and the dataflow connector to get data from the dataflow Anna created.</span></span>
3.  <span data-ttu-id="5f88f-127">เบนเจอข้อผิดพลาดเนื่องจากไม่ได้ถูกเพิ่มหรือได้รับอนุญาตไปยังโฟลเดอร์ CDM ของกระแสข้อมูลใน data lake</span><span class="sxs-lookup"><span data-stu-id="5f88f-127">Ben receives an error caused by not being added as an authorized user to the dataflow’s CDM folder in the data lake.</span></span>

<span data-ttu-id="5f88f-128">เพื่อแก้ไขปัญหานี้ เบนได้รับมอบสิทธิ์ให้สามารถเข้าถึงโฟลเดอร์และไฟล์ CDM</span><span class="sxs-lookup"><span data-stu-id="5f88f-128">To resolve this issue, Ben must be granted reader permissions to the CDM Folder and its files.</span></span> <span data-ttu-id="5f88f-129">คุณสามารถเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการให้สิทธิ์เข้าถึงโฟลเดอร์ CDM ใน [กำหนดค่าและใช้กระแสข้อมูล](dataflows/dataflows-configure-consume.md)</span><span class="sxs-lookup"><span data-stu-id="5f88f-129">You can learn more about how to grant access to the CDM Folder in [configure and consume a dataflow](dataflows/dataflows-configure-consume.md).</span></span>




## <a name="next-steps"></a><span data-ttu-id="5f88f-130">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="5f88f-130">Next steps</span></span>
<span data-ttu-id="5f88f-131">มีสิ่งน่าสนใจหลายอย่างที่คุณสามารถทำได้โดยใช้กระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5f88f-131">There are all sorts of interesting things you can do with dataflows.</span></span> <span data-ttu-id="5f88f-132">สำหรับข้อมูลเพิ่มเติม โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5f88f-132">For more information, check out the following resources:</span></span>

* [<span data-ttu-id="5f88f-133">ข้อมูลเบื้องต้นเกี่ยวกับกระแสข้อมูลและการเตรียมข้อมูลด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="5f88f-133">Introduction to dataflows and self-service data prep</span></span>](dataflows/dataflows-introduction-self-service.md)
* [<span data-ttu-id="5f88f-134">การสร้างกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5f88f-134">Creating a dataflow</span></span>](dataflows/dataflows-create.md)
* [<span data-ttu-id="5f88f-135">กำหนดค่าและใช้กระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5f88f-135">Configure and consume a dataflow</span></span>](dataflows/dataflows-configure-consume.md)
* [<span data-ttu-id="5f88f-136">การกำหนดค่าที่จัดเก็บกระแสข้อมูลเพื่อใช้ Azure Data Lake Gen 2</span><span class="sxs-lookup"><span data-stu-id="5f88f-136">Configuring Dataflow storage to use Azure Data Lake Gen 2</span></span>](dataflows/dataflows-azure-data-lake-storage-integration.md)
* [<span data-ttu-id="5f88f-137">ฟีเจอร์พรีเมียมของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5f88f-137">Premium features of dataflows</span></span>](dataflows/dataflows-premium-features.md)
* [<span data-ttu-id="5f88f-138">AI กับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5f88f-138">AI with dataflows</span></span>](dataflows/dataflows-machine-learning-integration.md)


<span data-ttu-id="5f88f-139">ยังมีบทความเกี่ยวกับ **Power BI Desktop** ที่อาจเป็นประโยชน์กับคุณ:</span><span class="sxs-lookup"><span data-stu-id="5f88f-139">There are also articles about **Power BI Desktop** that you might find useful:</span></span>

* [<span data-ttu-id="5f88f-140">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="5f88f-140">Data Sources in Power BI Desktop</span></span>](../connect-data/desktop-data-sources.md)
* [<span data-ttu-id="5f88f-141">จัดรูปร่างและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="5f88f-141">Shape and Combine Data with Power BI Desktop</span></span>](../connect-data/desktop-shape-and-combine-data.md)
* [<span data-ttu-id="5f88f-142">ป้อนข้อมูลลงใน Power BI Desktop โดยตรง</span><span class="sxs-lookup"><span data-stu-id="5f88f-142">Enter data directly into Power BI Desktop</span></span>](../connect-data/desktop-enter-data-directly-into-desktop.md)