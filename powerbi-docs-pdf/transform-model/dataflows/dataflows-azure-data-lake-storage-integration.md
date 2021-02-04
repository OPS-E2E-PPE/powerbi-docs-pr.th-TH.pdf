---
title: การกำหนดค่าที่จัดเก็บกระแสข้อมูลเพื่อใช้ Azure Data Lake Gen 2
description: ภาพรวมของวิธีการกำหนดค่าพื้นที่ทำงานหรือผู้เช่ากับที่เก็บข้อมูล Azure Data Lake Gen 2
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-dataflows
ms.topic: how-to
ms.date: 12/10/2020
LocalizationGroup: Data from files
ms.openlocfilehash: bf9740e0f4f6a2e25e1d5d0cc49671bd6eb90b37
ms.sourcegitcommit: 1cad78595cca1175b82c04458803764ac36e5e37
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/19/2021
ms.locfileid: "98565395"
---
# <a name="configuring-dataflow-storage-to-use-azure-data-lake-gen-2"></a><span data-ttu-id="d5317-103">การกำหนดค่าที่จัดเก็บกระแสข้อมูลเพื่อใช้ Azure Data Lake Gen 2</span><span class="sxs-lookup"><span data-stu-id="d5317-103">Configuring dataflow storage to use Azure Data Lake Gen 2</span></span> 

<span data-ttu-id="d5317-104">ข้อมูลที่ใช้กับ Power BI จะถูกเก็บไว้ในที่เก็บข้อมูลภายในโดย Power BI ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d5317-104">Data used with Power BI is stored in internal storage provided by Power BI by default.</span></span> <span data-ttu-id="d5317-105">ด้วยการรวมกันของกระแสข้อมูลและ Azure Data Lake Storage Gen 2 (ADLS Gen2) คุณสามารถจัดเก็บกระแสข้อมูลของคุณในบัญชี Azure Data Lake Storage Gen2 ภายในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="d5317-105">With the integration of dataflows and Azure Data Lake Storage Gen 2 (ADLS Gen2), you can store your dataflows in your organization's Azure Data Lake Storage Gen2 account.</span></span>

<span data-ttu-id="d5317-106">มีวิธีการกำหนดค่าที่เก็บ ADLS Gen 2 ที่จะใช้สองวิธี: คุณสามารถใช้บัญชี ADLS gen 2 ที่กำหนดให้ผู้เช่า หรือคุณสามารถนำที่เก็บ ADLS Gen 2 ของคุณเองมาใช้ในระดับพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="d5317-106">There are two ways to configure which ADLS Gen 2 store to use: you can use a tenant assigned ADLS gen 2 account, or you can bring your own ADLS Gen 2 store at a workspace level.</span></span> 

## <a name="pre-requisites"></a><span data-ttu-id="d5317-107">การเตรียมปัจจัยที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="d5317-107">Pre-requisites</span></span>

<span data-ttu-id="d5317-108">หากต้องการนำบัญชี ADLS Gen 2 ของคุณเองมาใช้ คุณต้องมีสิทธิ์ระดับเจ้าของสำหรับบัญชีที่เก็บข้อมูล กลุ่มทรัพยากร หรือชั้นการสมัครสมาชิก</span><span class="sxs-lookup"><span data-stu-id="d5317-108">To bring your own ADLS Gen 2 account, you must have owner permissions at either the storage account, resource group or subscription layer.</span></span> <span data-ttu-id="d5317-109">หากคุณเป็นผู้ดูแลระบบ คุณยังต้องกำหนดสิทธิ์เจ้าของด้วยตัวคุณเอง</span><span class="sxs-lookup"><span data-stu-id="d5317-109">If you are an administrator, you still must assign yourself owner permission.</span></span> 

<span data-ttu-id="d5317-110">คุณต้องสร้างบัญชีที่เก็บข้อมูลด้วยการเปิดใช้งาน[เนมสเปซแบบลำดับชั้น (HNS)](/azure/storage/blobs/create-data-lake-storage-account)</span><span class="sxs-lookup"><span data-stu-id="d5317-110">The storage account must be created with the [Hierarchical Namespace (HNS)](/azure/storage/blobs/create-data-lake-storage-account) enabled.</span></span> 

<span data-ttu-id="d5317-111">นอกจากนี้ คุณต้องปรับใช้งานบัญชี ADLS Gen 2 ในภูมิภาคเดียวกันกับผู้เช่า Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d5317-111">Also, the ADLS Gen 2 account must be deployed in the same region as your Power BI tenant.</span></span> <span data-ttu-id="d5317-112">มีข้อผิดพลาดเกิดขึ้นถ้าตำแหน่งที่ตั้งของทรัพยากรไม่ได้อยู่ในภูมิภาคเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="d5317-112">An error occurs if the locations of the resources are not in the same region.</span></span>

<span data-ttu-id="d5317-113">สุดท้ายคุณสามารถเชื่อมต่อกับ ADLS gen 2 จากพอร์ทัลผู้ดูแลระบบ แต่ถ้าคุณเชื่อมต่อโดยตรงกับพื้นที่ทำงาน ก่อนอื่นคุณต้องตรวจสอบให้แน่ใจว่าไม่มีกระแสข้อมูลในพื้นที่ทำงานก่อนที่จะเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="d5317-113">Finally, you can connect to any ADLS gen 2 from the admin portal, but if you connect directly to a workspace, you must first ensure there are no dataflows in the workspace before connecting.</span></span>

## <a name="connecting-to-an-azure-data-lake-gen-2-at-a-workspace"></a><span data-ttu-id="d5317-114">การเชื่อมต่อกับ Azure Data Lake Gen 2 ในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="d5317-114">Connecting to an Azure Data Lake Gen 2 at a workspace</span></span>
<span data-ttu-id="d5317-115">นำทางไปยังพื้นที่ทำงานที่ไม่มีกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d5317-115">Navigate to a workspace that has no dataflows.</span></span> <span data-ttu-id="d5317-116">เลือก **การตั้งค่าพื้นที่ทำงาน** ไปที่แท็บใหม่ชื่อ **การเชื่อมต่อ Azure**</span><span class="sxs-lookup"><span data-stu-id="d5317-116">Select **Workspace settings** to a new tab called **Azure Connections**.</span></span> <span data-ttu-id="d5317-117">เลือกแท็บ **การเชื่อมต่อ Azure** จากนั้นเลือกส่วน **ที่จัดเก็บ**</span><span class="sxs-lookup"><span data-stu-id="d5317-117">Select the **Azure Connections** tab and then select the **Storage** section.</span></span>


![เชื่อมต่อไปยัง Azure](media/dataflows-azure-data-lake-storage-integration/connect-to-azure.png)
 
<span data-ttu-id="d5317-119">ตัวเลือก **ใช้การเชื่อมต่อ Azure ค่าเริ่มต้น** จะปรากฏให้เห็นหากผู้เช่าได้กำหนดค่า ADLS Gen 2 แล้ว</span><span class="sxs-lookup"><span data-stu-id="d5317-119">The **Use default Azure connection** option is  visible if the tenant has already configured ADLS Gen 2.</span></span> <span data-ttu-id="d5317-120">คุณมีสองทางเลือก: ใช้ผู้เช่าที่กำหนดค่า ADLS gen 2 โดยเลือกช่องที่เรียกว่า **ใช้การเชื่อมต่อ Azure ค่าเริ่มต้น** หรือเลือก **เชื่อมต่อกับ Azure** เพื่อชี้ไปที่บัญชี Azure Storage ใหม่</span><span class="sxs-lookup"><span data-stu-id="d5317-120">You have two options: use the tenant configured ADLS gen 2 by selecting the box called **Use the default Azure connection**, or select **Connect to Azure** to point to a new Azure Storage account.</span></span> 

<span data-ttu-id="d5317-121">เมื่อคุณเลือก **เชื่อมต่อกับ Azure** Power BI จะดึงรายการการสมัครใช้งาน Azure ที่คุณสามารถเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="d5317-121">When you select **Connect to Azure** Power BI retrieves a list of Azure subscriptions to which you have access.</span></span> <span data-ttu-id="d5317-122">กรอกข้อมูลในดรอปดาวน์และเลือกการสมัครใช้งาน Azure กลุ่มทรัพยากร และบัญชีหน่วยเก็บข้อมูลที่ถูกต้องซึ่งเปิดใช้งานตัวเลือกเนมสเปซแบบลำดับชั้นซึ่งเป็นแฟล็กหรือตัวแสดงสถานะ ADLS Gen2</span><span class="sxs-lookup"><span data-stu-id="d5317-122">Fill in the dropdowns and select a valid Azure subscription, resource group, and storage account which has hierarchical namespace option enabled, which is the ADLS Gen2 flag.</span></span>

![รายละเอียดการสมัครใช้งาน](media/dataflows-azure-data-lake-storage-integration/subscription-details-enter.png)
 
<span data-ttu-id="d5317-124">เมื่อเลือกแล้ว ให้เลือก **บันทึก** และตอนนี้คุณได้เชื่อมต่อพื้นที่ทำงานกับบัญชี ADLS Gen2 ของคุณเองเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="d5317-124">Once selected, select **Save** and you now have successfully attached the workspace to your own ADLS Gen2 account.</span></span> <span data-ttu-id="d5317-125">Power BI จะกำหนดค่าบัญชีที่จัดเก็บโดยอัตโนมัติด้วยสิทธิ์ที่จำเป็นและตั้งค่าระบบไฟล์ Power BI ที่จะเขียนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d5317-125">Power BI automatically configures the storage account with the required permissions, and sets up the Power BI filesystem to which  the data will be written.</span></span> <span data-ttu-id="d5317-126">ณ จุดนี้ข้อมูลทั้งหมดของกระแสข้อมูลภายในพื้นที่ทำงานนี้จะเขียนลงในระบบไฟล์นี้โดยตรง ซึ่งสามารถใช้กับบริการ Azure อื่น ๆ ได้โดยสร้างแหล่งข้อมูลเดียวสำหรับข้อมูลองค์กรหรือแผนกทั้งหมดของคุณ</span><span class="sxs-lookup"><span data-stu-id="d5317-126">At this point, every dataflow’s data inside this workspace will write directly to this filesystem, which can be used with other Azure services, creating a single source for all of your organizational or departmental data.</span></span>

## <a name="detaching-azure-data-lake-gen-2-from-a-workspace-or-tenant"></a><span data-ttu-id="d5317-127">การแยก Azure Data Lake Gen 2 ออกจากพื้นที่ทำงานหรือผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="d5317-127">Detaching Azure Data Lake Gen 2 from a workspace or tenant</span></span>

<span data-ttu-id="d5317-128">หากต้องการลบการเชื่อมต่อในระดับพื้นที่ทำงาน ก่อนอื่นคุณต้องแน่ใจว่าคุณได้ลบกระแสข้อมูลทั้งหมดในพื้นที่ทำงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="d5317-128">To remove a connection at a workspace level, you must first ensure all dataflows in the workspace are deleted.</span></span> <span data-ttu-id="d5317-129">เมื่อลบกระแสข้อมูลทั้งหมดแล้ว ให้เลือก **ยกเลิกการเชื่อมต่อ** ในการตั้งค่าพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="d5317-129">Once all the dataflows have been removed, select **Disconnect** in the workspace settings.</span></span> <span data-ttu-id="d5317-130">เช่นเดียวกันกับผู้เช่า แต่ก่อนอื่นคุณต้องแน่ใจว่าคุณได้ยกเลิกการเชื่อมต่อพื้นที่ทำงานทั้งหมดจากบัญชีที่เก็บข้อมูลของผู้เช่าแล้ว ก่อนที่คุณจะสามารถยกเลิกการเชื่อมต่อในระดับผู้เช่าได้</span><span class="sxs-lookup"><span data-stu-id="d5317-130">The same applies for a tenant, but you must first ensure all workspaces have also been disconnected from the tenant storage account before you are able to disconnect at a tenant level.</span></span>

## <a name="disabling-azure-data-lake-gen-2"></a><span data-ttu-id="d5317-131">การปิดใช้งาน Azure Data Lake Gen 2</span><span class="sxs-lookup"><span data-stu-id="d5317-131">Disabling Azure Data Lake Gen 2</span></span>

<span data-ttu-id="d5317-132">ใน **พอร์ทัลผู้ดูแลระบบ** ภายใต้ **กระแสข้อมูล** คุณสามารถปิดใช้งานการเข้าถึงสำหรับผู้ใช้เพื่อใช้คุณลักษณะนี้และสามารถไม่อนุญาตให้ผู้ดูแลระบบพื้นที่ทำงานนำ Azure Storage ของตนเองมาใช้ได้</span><span class="sxs-lookup"><span data-stu-id="d5317-132">In the **Admin portal**, under **dataflows**, you can disable access for users to either use this feature, and can disallow workspace admins to bring their own Azure Storage.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d5317-133">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d5317-133">Next steps</span></span>
<span data-ttu-id="d5317-134">บทความต่อไปนี้ให้ข้อมูลเพิ่มเติมเกี่ยวกับกระแสข้อมูลและ Power BI:</span><span class="sxs-lookup"><span data-stu-id="d5317-134">The following articles provide more information about dataflows and Power BI:</span></span>

* [<span data-ttu-id="d5317-135">ข้อมูลเบื้องต้นเกี่ยวกับกระแสข้อมูลและการเตรียมข้อมูลด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d5317-135">Introduction to dataflows and self-service data prep</span></span>](dataflows-introduction-self-service.md)
* [<span data-ttu-id="d5317-136">การสร้างกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d5317-136">Creating a dataflow</span></span>](dataflows-create.md)
* [<span data-ttu-id="d5317-137">กำหนดค่าและใช้กระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d5317-137">Configure and consume a dataflow</span></span>](dataflows-configure-consume.md)
* [<span data-ttu-id="d5317-138">ฟีเจอร์พรีเมียมของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d5317-138">Premium features of dataflows</span></span>](dataflows-premium-features.md)
* [<span data-ttu-id="d5317-139">AI กับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d5317-139">AI with dataflows</span></span>](dataflows-machine-learning-integration.md)
* [<span data-ttu-id="d5317-140">ข้อจำกัดและข้อควรพิจารณาของกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d5317-140">Dataflows limitations and considerations</span></span>](dataflows-features-limitations.md)
* [<span data-ttu-id="d5317-141">แนวทางปฏิบัติที่ดีที่สุดสำหรับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d5317-141">Dataflows best practices</span></span>](dataflows-best-practices.md)