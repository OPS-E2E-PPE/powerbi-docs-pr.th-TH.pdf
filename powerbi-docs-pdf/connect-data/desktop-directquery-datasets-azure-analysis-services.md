---
title: การใช้ DirectQuery สำหรับชุดข้อมูลและบริการวิเคราะห์ Azure (ตัวอย่าง)
description: การใช้ DirectQuery สำหรับชุดข้อมูล Power BI และารบริการด้านการวิเคราะห์ Azure (ตัวอย่าง)
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: conceptual
ms.date: 12/17/2020
LocalizationGroup: Connect to data
ms.openlocfilehash: 6e674d115c08e19044cfd5d7fe746f630bbc544b
ms.sourcegitcommit: 5c09d121d3205e65fb33a2eca0e60bc30e777773
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/18/2020
ms.locfileid: "97674924"
---
# <a name="using-directquery-for-power-bi-datasets-and-azure-analysis-services-preview"></a><span data-ttu-id="e2a96-103">การใช้ DirectQuery สำหรับชุดข้อมูล Power BI และ Azure Analysis Services (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="e2a96-103">Using DirectQuery for Power BI datasets and Azure Analysis Services (preview)</span></span>


<span data-ttu-id="e2a96-104">ด้วย **DirectQuery สำหรับชุดข้อมูล Power BI และบริการวิเคราะห์ Azure (AAS)** คุณสามารถใช้ DirectQuery ในการเชื่อมต่อกับชุดข้อมูล AAS หรือ Power BI และถ้าคุณต้องการรวมเข้าด้วยกันกับ DirectQuery และอื่นๆ ได้</span><span class="sxs-lookup"><span data-stu-id="e2a96-104">With **DirectQuery for Power BI datasets and Azure Analysis Services (AAS)**, you can use DirectQuery to connect to AAS or Power BI datasets and if you want, combine it with other DirectQuery and imported data.</span></span> <span data-ttu-id="e2a96-105">ผู้เขียนรายงานที่ต้องการรวมข้อมูลจากแบบจำลองเชิงความหมายขององค์กรกับข้อมูลอื่นที่พวกเขาเป็นเจ้าของเช่นสเปรดชีต Excel หรือต้องการปรับแต่งหรือเพิ่มข้อมูลเมตาจากแบบจำลองความหมายขององค์กร จะพบว่าฟีเจอร์นี้มีประโยชน์อย่างยิ่ง</span><span class="sxs-lookup"><span data-stu-id="e2a96-105">Report authors who want to combine the data from their enterprise semantic model with other data they own, such as an Excel spreadsheet, or want to personalize or enrich the metadata from their enterprise semantic model, will find this feature especially useful.</span></span>

## <a name="enable-the-preview-feature"></a><span data-ttu-id="e2a96-106">เปิดใช้งานคุณลักษณะตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="e2a96-106">Enable the preview feature</span></span>

<span data-ttu-id="e2a96-107">เนื่องจากฟังก์ชันนี้อยู่ในการแสดงตัวอย่าง คุณต้องเปิดใช้งานก่อน</span><span class="sxs-lookup"><span data-stu-id="e2a96-107">Since the functionality is currently in preview, you must first enable it.</span></span> <span data-ttu-id="e2a96-108">ในการดำเนินการดังกล่าวใน Power BI Desktop ให้ไปที่ **ไฟล์ > ตัวเลือกและการตั้งค่า > ตัวเลือก** และในส่วน **ฟีเจอร์การแสดงตัวอย่าง** ให้เลือกช่องทำเครื่องหมาย **DirectQuery สำหรับชุดข้อมูลและบริการวิเคราะห์ของ Power BI** เพื่อเปิดใช้งานฟีเจอร์การแสดงตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="e2a96-108">To do so, in Power BI Desktop go to **File > Options and settings > Options**, and in the **Preview features** section, select the **DirectQuery for Power BI datasets and Analysis Services** checkbox to enable this preview feature.</span></span> <span data-ttu-id="e2a96-109">คุณอาจจำเป็นต้องรีสตาร์ท Power BI Desktop เพื่อดำเนินการเปลี่ยนแปลงนี้</span><span class="sxs-lookup"><span data-stu-id="e2a96-109">You may need to restart Power BI Desktop for the change to take effect.</span></span>

## <a name="using-directquery-for-live-connections"></a><span data-ttu-id="e2a96-110">การใช้ DirectQuery สำหรับการเชื่อมต่อสด</span><span class="sxs-lookup"><span data-stu-id="e2a96-110">Using DirectQuery for live connections</span></span>

<span data-ttu-id="e2a96-111">การใช้ DirectQuery สำหรับชุดข้อมูล Power BI และบริการวิเคราะห์ Azure (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="e2a96-111">Using DirectQuery for Power BI datasets and Azure Analysis Services requires  your report to have a local model.</span></span> <span data-ttu-id="e2a96-112">คุณสามารถเริ่มต้นจากการเชื่อมต่อสดและเพิ่มหรืออัปเกรดเป็นแบบจำลองภายในเครื่อง หรือเริ่มต้นด้วยการเชื่อมต่อ DirectQuery หรือข้อมูลที่นำเข้าซึ่งจะสร้างแบบจำลองภายในเครื่องในรายงานของคุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e2a96-112">You can start from a live connection and add or upgrade to a local model, or start with a DirectQuery connection or imported data, which  automatically creates a local model in your report.</span></span>

<span data-ttu-id="e2a96-113">หากต้องการดูว่ามีการใช้การเชื่อมต่อใดในแบบจำลองของคุณ ให้ตรวจสอบแถบสถานะที่มุมล่างขวาของ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e2a96-113">To see which connections are being used in your model, check the status bar in the bottom right corner of Power BI Desktop.</span></span> <span data-ttu-id="e2a96-114">ถ้าคุณเชื่อมต่อกับแหล่งบริการวิเคราะห์ Azure  เท่านั้น คุณจะเห็นข้อความดังภาพต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e2a96-114">If you're only connected to an Azure Analysis Services source, you see a message like the following image:</span></span>

![เชื่อมต่อกับบริการวิเคราะห์ Azure เท่านั้น](media/desktop-directquery-datasets-azure-analysis-services/directquery-datasets-01.png)

<span data-ttu-id="e2a96-116">ถ้าคุณเชื่อมต่อกับชุดข้อมูล Power BI คุณจะเห็นข้อความที่บอกให้คุณทราบว่าชุดข้อมูล Power BI ใดที่คุณกำลังเชื่อมต่อดังนี้:</span><span class="sxs-lookup"><span data-stu-id="e2a96-116">If you're connected to a Power BI dataset, you see a message telling you which Power BI dataset you're connected to:</span></span>

![การเชื่อมต่อชุดข้อมูล Power BI](media/desktop-directquery-datasets-azure-analysis-services/directquery-datasets-01b.png)

<span data-ttu-id="e2a96-118">ถ้าคุณต้องการกำหนดค่าเมตาดาต้าของเขตข้อมูลในชุดข้อมูลที่เชื่อมต่อสด ให้เลือก **ทำการเปลี่ยนแปลงในแบบจำลองนี้** ในแถบสถานะ</span><span class="sxs-lookup"><span data-stu-id="e2a96-118">If you want to customize the metadata of fields in your live connected dataset, select **Make changes to this model** in the status bar.</span></span> <span data-ttu-id="e2a96-119">อีกวิธีหนึ่งคือคุณสามารถคลิกที่ปุ่ม **ทำการเปลี่ยนแปลงในแบบจำลองนี้** ใน ribbon ดังที่แสดงในรูปภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e2a96-119">Alternatively, you can click the **Make changes to this model** button in the ribbon, as shown in the following image.</span></span> <span data-ttu-id="e2a96-120">ใน **มุมมองรายงาน** ปุ่ม **ทำการเปลี่ยนแปลงในแบบจำลองนี้** อยู่ในแท็บ **การสร้างโมเดล** ในมุมมองแบบจำลอง ปุ่มจะอยู่ใน แท็บ **หน้าแรก**</span><span class="sxs-lookup"><span data-stu-id="e2a96-120">In **Report View** the **Make changes to this model** button in the **Modeling** tab. In Model View, the button is in the **Home** tab.</span></span>

![ปุ่มทำการเปลี่ยนแปลงไปยังแบบจำลองนี้](media/desktop-directquery-datasets-azure-analysis-services/directquery-datasets-02.png)

<span data-ttu-id="e2a96-122">การเลือกปุ่มจะแสดงกล่องโต้ตอบที่ยืนยันการเพิ่มแบบจำลองภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="e2a96-122">Selecting the button displays a dialog confirming addition of a local model.</span></span> <span data-ttu-id="e2a96-123">เลือก **เพิ่มแบบจำลองภายในเครื่อง** เพื่อเปิดใช้งานการสร้างคอลัมน์ใหม่หรือปรับเปลี่ยนเมตาดาต้าสำหรับเขตข้อมูลจากชุดข้อมูล Power BI หรือบริการวิเคราะห์ Azure</span><span class="sxs-lookup"><span data-stu-id="e2a96-123">Select **Add a local model** to enable creating new columns or modifying the metadata, for fields from Power BI datasets or Azure Analysis Services.</span></span> <span data-ttu-id="e2a96-124">รูปภาพต่อไปนี้แสดงกล่องโต้ตอบที่แสดงขึ้นมา</span><span class="sxs-lookup"><span data-stu-id="e2a96-124">The following image shows the dialog that's displayed.</span></span> 

![สร้างกล่องโต้ตอบแบบจำลองภายในเครื่อง](media/desktop-directquery-datasets-azure-analysis-services/directquery-datasets-03.png)

<span data-ttu-id="e2a96-126">เมื่อคุณเชื่อมต่อสดไปยังแหล่งข้อมูลของบริการวิเคราะห์ จะไม่มีแบบจำลองภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="e2a96-126">When you're connected live to an Analysis Services source, there is no local model.</span></span> <span data-ttu-id="e2a96-127">หากต้องการใช้ DirectQuery สำหรับแหล่งข้อมูลที่เชื่อมต่อสด เช่น ชุดข้อมูล Power BI และบริการวิเคราะห์ Azure คุณต้องเพิ่มแบบจำลองภายในเครื่องลงในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="e2a96-127">To use DirectQuery for live connected sources, such as Power BI datasets and Azure Analysis Services, you must add a local model to your report.</span></span> <span data-ttu-id="e2a96-128">เมื่อคุณเผยแพร่รายงานด้วยแบบจำลองภายในเครื่องไปยังบริการของ Power BI ชุดข้อมูลสำหรับแบบจำลองภายในเครื่องนั้นได้รับการเผยแพร่เป็นอย่างดี</span><span class="sxs-lookup"><span data-stu-id="e2a96-128">When you publish a report with a local model to the Power BI service, a dataset for that local model is published a well.</span></span>

## <a name="chaining"></a><span data-ttu-id="e2a96-129">การเกี่ยวโยง</span><span class="sxs-lookup"><span data-stu-id="e2a96-129">Chaining</span></span>

<span data-ttu-id="e2a96-130">ชุดข้อมูล และชุดข้อมูลและแบบจำลองที่ยึดตามในรูปแบบ *เกี่ยวโยง*</span><span class="sxs-lookup"><span data-stu-id="e2a96-130">Datasets, and the datasets and models they are based, on form a *chain*.</span></span> <span data-ttu-id="e2a96-131">กระบวนการนี้เรียกว่า **การเกี่ยวโยง** ช่วยให้คุณสามารถเผยแพร่รายงานและชุดข้อมูลที่ยึดตาม Power BI อื่นๆ ซึ่งเป็นฟีเจอร์ที่ไม่สามารถใช้งานได้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="e2a96-131">This process, called **chaining** lets you publish a report and dataset based on other Power BI datasets, a feature that previously was not possible.</span></span>

<span data-ttu-id="e2a96-132">ตัวอย่างเช่น สมมติว่าเพื่อนร่วมงานของคุณเผยแพร่ชุดข้อมูล Power BI ที่เรียกว่า *ยอดขายและงบประมาณ* ที่ยึดตามแบบจำลองบริการวิเคราะห์ Azure ที่เรียกว่า *ยอดขาย* และรวมเข้ากับแผ่นงาน Excel ที่เรียกว่า *งบประมาณ*</span><span class="sxs-lookup"><span data-stu-id="e2a96-132">For example, imagine your colleague publishes a Power BI dataset called *Sales and Budget* that's based on an Azure Analysis Services model called *Sales*, and combines it with an Excel sheet called *Budget*.</span></span>

<span data-ttu-id="e2a96-133">เมื่อคุณเผยแพร่รายงานใหม่ (และชุดข้อมูล) ที่เรียกว่า *ยอดขายและงบประมาณของยุโรป* ที่ยึดตามชุดข้อมูล *ยอดขายและงบประมาณ* Power BI ที่เผยแพร่โดยเพื่อนร่วมงานของคุณ การทำการปรับเปลี่ยนหรือส่วนขยายเพิ่มเติม ในขณะที่คุณทำเช่นนั้นคุณจะเพิ่มรายงานและชุดข้อมูลลงในการเกี่ยวโยงของความยาวสามระดับ ซึ่งเริ่มต้นด้วย *ยอดขาย* แบบจำลองบริการวิเคราะห์ Azure และสิ้นสุดด้วยชุดข้อมูล Power BI *ยอดขายและงบประมาณของยุโรป* ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e2a96-133">When you publish a new report (and dataset) called *Sales and Budget Europe* that's based on the *Sales and Budget* Power BI dataset published by your colleague, making some further modifications or extensions as you do so, you're effectively adding a report and dataset to a chain of length three, which started with the *Sales* Azure Analysis Services model, and ends with your *Sales and Budget Europe* Power BI dataset.</span></span> <span data-ttu-id="e2a96-134">รูปภาพต่อไปนี้แสดงให้เห็นถึงกระบวนการเกี่ยวโยงนี้</span><span class="sxs-lookup"><span data-stu-id="e2a96-134">The following image visualizes this chaining process.</span></span>

![กระบวนการของชุดข้อมูลการเกี่ยวโยง](media/desktop-directquery-datasets-azure-analysis-services/directquery-datasets-04.png)

<span data-ttu-id="e2a96-136">การเกี่ยวโยงในรูปภาพก่อนหน้านี้มีความยาวสามระดับซึ่งเป็นความยาวสูงสุดในช่วงระยะเวลาการแสดงตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="e2a96-136">The chain in the previous image is of length three, which is the maximum length during this preview period.</span></span> <span data-ttu-id="e2a96-137">การขยายเกินความยาวการเกี่ยวโยงสามระดับไม่ได้รับการรองรับและส่งผลให้เกิดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="e2a96-137">Extending beyond a chain length of three is  not supported and results in errors.</span></span>

## <a name="security-warning"></a><span data-ttu-id="e2a96-138">คำเตือนด้านความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="e2a96-138">Security warning</span></span>

<span data-ttu-id="e2a96-139">การใช้ฟีเจอร์ **DirectQuery สำหรับชุดข้อมูล Power BI และบริการวิเคราะห์ Azure (AAS)** จะแสดงให้คุณเห็นกล่องโต้ตอบคำเตือนเกี่ยวกับความปลอดภัยที่แสดงในรูปภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e2a96-139">Using the **DirectQuery for Power BI datasets and Azure Analysis Services (AAS)** feature will present you with a security warning dialog, shown in the following image.</span></span>

![คำเตือนด้านความปลอดภัย](media/desktop-directquery-datasets-azure-analysis-services/directquery-datasets-05.png)

<span data-ttu-id="e2a96-141">อาจมีการส่งข้อมูลจากแหล่งข้อมูลหนึ่งไปยังอีกแหล่ง ซึ่งเป็นคำเตือนการรักษาความปลอดภัยเดียวกันสำหรับการรวม DirectQuery และนำเข้าแหล่งข้อมูลในรูปแบบแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e2a96-141">Data may be pushed from one data source to another, which is the same security warning for combining DirectQuery and import sources in a data model.</span></span> <span data-ttu-id="e2a96-142">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวฟีเจอร์การทำงานนี้ โปรดดู[การใช้โมเดลแบบรวมใน Power BI Desktop](../transform-model/desktop-composite-models.md)</span><span class="sxs-lookup"><span data-stu-id="e2a96-142">To learn more about this behavior, please see [using composite models in Power BI Desktop](../transform-model/desktop-composite-models.md).</span></span>

## <a name="features-and-scenarios-to-try"></a><span data-ttu-id="e2a96-143">ฟีเจอร์และสถานการณ์สมมติสำหรับทดลอง</span><span class="sxs-lookup"><span data-stu-id="e2a96-143">Features and scenarios to try</span></span>

<span data-ttu-id="e2a96-144">รายการต่อไปนี้จะให้คำแนะนำเกี่ยวกับวิธีที่คุณสามารถสำรวจ **DirectQuery สำหรับชุดข้อมูล Power BI และบริการวิเคราะห์ Azure (AAS)** สำหรับตัวคุณเอง:</span><span class="sxs-lookup"><span data-stu-id="e2a96-144">The following list provides suggestions on how you can explore **DirectQuery for Power BI datasets and Azure Analysis Services (AAS)** for yourself:</span></span>

- <span data-ttu-id="e2a96-145">การเชื่อมต่อกับข้อมูลจากแหล่งต่างๆ: นำเข้า (เช่นไฟล์), ชุดข้อมูล Power BI, บริการวิเคราะห์ Azure</span><span class="sxs-lookup"><span data-stu-id="e2a96-145">Connecting to data from various sources: Import (such as files), Power BI datasets, Azure Analysis Services</span></span>
- <span data-ttu-id="e2a96-146">การสร้างความสัมพันธ์ระหว่างแหล่งข้อมูลที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="e2a96-146">Creating relationships between different data sources</span></span>
- <span data-ttu-id="e2a96-147">การเขียนหน่วยวัดที่ใช้เขตข้อมูลจากแหล่งข้อมูลที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="e2a96-147">Writing measures that use fields from different data sources</span></span>
- <span data-ttu-id="e2a96-148">การสร้างคอลัมน์ใหม่สำหรับตารางจากชุดข้อมูล Power BI ของบริการวิเคราะห์ Azure</span><span class="sxs-lookup"><span data-stu-id="e2a96-148">Creating new columns for tables from Power BI datasets of Azure Analysis Services</span></span>
- <span data-ttu-id="e2a96-149">การเขียนหน่วยวัดที่ใช้เขตข้อมูลจากแหล่งข้อมูลที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="e2a96-149">Creating visuals that use columns from different data sources</span></span>

## <a name="considerations-and-limitations"></a><span data-ttu-id="e2a96-150">ข้อควรพิจารณาและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="e2a96-150">Considerations and limitations</span></span>

<span data-ttu-id="e2a96-151">มีข้อควรพิจารณา **ข้อควรพิจารณา** บางอย่าง ให้ทราบเมื่อใช้ **DirectQuery สำหรับชุดข้อมูล Power BI และบริการวิเคราะห์ Azure  (AAS)** ดังนี้:</span><span class="sxs-lookup"><span data-stu-id="e2a96-151">There are a few **considerations** to keep in mind when using **DirectQuery for Power BI datasets and Azure Analysis Services (AAS)**:</span></span>

- <span data-ttu-id="e2a96-152">ถ้าคุณรีเฟรชแหล่งข้อมูลของคุณและมีข้อผิดพลาดกับเขตข้อมูลที่ขัดแย้งกันหรือชื่อตาราง Power BI จะช่วยแก้ไขข้อผิดพลาดให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="e2a96-152">If you refresh your data sources, and there are errors with conflicting field or table names, Power BI resolves the errors for you.</span></span>

- <span data-ttu-id="e2a96-153">หากต้องการสร้างรายงานในบริการของ Power BI ในแบบจำลองรวมที่ยึดตามชุดข้อมูลอื่น ข้อมูลประจำตัวทั้งหมดจะต้องได้รับการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="e2a96-153">To build reports in the Power BI service on a composite model that's based on another dataset, all credentials must be set.</span></span> <span data-ttu-id="e2a96-154">ในหน้าการตั้งค่าข้อมูลประจำตัวรีเฟรช สำหรับแหล่งบริการวิเคราะห์ Azure ข้อผิดพลาดต่อไปนี้จะปรากฏขึ้นแม้ว่าข้อมูลประจำตัวได้รับการตั้งค่าแล้ว:</span><span class="sxs-lookup"><span data-stu-id="e2a96-154">On the refresh credential settings page, for Azure Analysis Services sources, the following error will appear, even though the credentials have been set:</span></span>
    
    ![คำเตือนเท็จของข้อมูลประจำตัว](media/desktop-directquery-datasets-azure-analysis-services/directquery-datasets-06.png)
- <span data-ttu-id="e2a96-156">เนื่องจากนี่คือความสับสนและไม่ถูกต้อง นี่คือสิ่งที่เราจะดูแลแก้ไขในเร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="e2a96-156">As this is confusing and incorrect, this is something we will take care of soon.</span></span>

- <span data-ttu-id="e2a96-157">กฎ RLS จะถูกนำไปใช้กับแหล่งข้อมูลซึ่งมีการกำหนดไว้แต่จะไม่ถูกนำไปใช้กับชุดข้อมูลอื่นๆ ในแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="e2a96-157">RLS rules will be applied on the source on which they are defined, but will not be applied to any other datasets in the model.</span></span> <span data-ttu-id="e2a96-158">RLS ที่กำหนดในรายงานจะไม่ถูกนำไปใช้กับแหล่งข้อมูลระยะไกลและ RLS ที่ตั้งค่าไว้ในแหล่งข้อมูลระยะไกลจะไม่ถูกนำไปใช้กับแหล่งข้อมูลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="e2a96-158">RLS defined in the report will not be applied to remote sources, and RLS set on remote sources will not be applied to other data sources.</span></span>

- <span data-ttu-id="e2a96-159">แสดงโฟลเดอร์ Kpi, ตารางวันที่, ระดับแถวการรักษาความปลอดภัย และการแปลจะไม่ถูกนำเข้าจากแหล่งข้อมูลในการเผยแพร่ตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="e2a96-159">Display folders, KPIs, date tables, row level security, and translations will not be imported from the source in this preview release.</span></span> <span data-ttu-id="e2a96-160">คุณยังสามารถสร้างโฟลเดอร์การแสดงผลในแบบจำลองภายในเครื่องได้</span><span class="sxs-lookup"><span data-stu-id="e2a96-160">You can still create display folders in the local model.</span></span>

- <span data-ttu-id="e2a96-161">คุณอาจเห็นพฤติกรรมการทำงานที่ไม่คาดคิดเมื่อใช้ลำดับชั้นวันที่</span><span class="sxs-lookup"><span data-stu-id="e2a96-161">You may see some unexpected behavior when using a date hierarchy.</span></span> <span data-ttu-id="e2a96-162">เมื่อต้องการแก้ไขปัญหานี้ให้ใช้คอลัมน์วันที่แทน</span><span class="sxs-lookup"><span data-stu-id="e2a96-162">To resolve this issue, use a date column instead.</span></span> <span data-ttu-id="e2a96-163">หลังจากเพิ่มลำดับชั้นวันที่ไปยังภาพ คุณสามารถสลับไปยังคอลัมน์วันที่ได้โดยการคลิกที่ลูกศรลงในชื่อเขตข้อมูลและจากนั้นคลิกที่ชื่อเขตข้อมูลนั้นแทนการใช้ *ลำดับชั้นวันที่*:</span><span class="sxs-lookup"><span data-stu-id="e2a96-163">After adding a date hierarchy to a visual, you can switch to a date column by clicking on the down arrow in the field name, and then clicking on the name of that field instead of using *Date Hierarchy*:</span></span>

    ![พฤติกรรมลำดับชั้นวันที่ที่ไม่คาดคิด](media/desktop-directquery-datasets-azure-analysis-services/directquery-datasets-07.png)

    <span data-ttu-id="e2a96-165">โปรดเยี่ยมชมบทความนี้สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการใช้คอลัมน์วันที่เทียบกับลำดับชั้นวันที่</span><span class="sxs-lookup"><span data-stu-id="e2a96-165">For more information on using date columns versus date hierarchies, visit this article.</span></span>

- <span data-ttu-id="e2a96-166">คุณอาจเห็นข้อความข้อผิดพลาดที่ไม่เป็นประโยชน์เมื่อใช้ฟีเจอร์ AI ด้วยแบบจำลองที่มีการเชื่อมต่อ DirectQuery ไปยังบริการวิเคราะห์ Azure</span><span class="sxs-lookup"><span data-stu-id="e2a96-166">You may see unuseful error messages when using AI features with a model that has a DirectQuery connection to Azure Analysis Services.</span></span> 

- <span data-ttu-id="e2a96-167">การใช้ ALLSELECTED กับผลลัพธ์แหล่งข้อมูล DirectQuery ในผลลัพธ์ที่ไม่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e2a96-167">Using ALLSELECTED with a DirectQuery source results in incomplete results.</span></span>

- <span data-ttu-id="e2a96-168">ตัวกรองและความสัมพันธ์:</span><span class="sxs-lookup"><span data-stu-id="e2a96-168">Filters and relationships:</span></span>
    - <span data-ttu-id="e2a96-169">สามารถตั้งค่าตัวกรองที่ใช้จากแหล่งข้อมูลไปยังตารางจากแหล่งข้อมูล DirectQuery อื่นได้เฉพาะในคอลัมน์เดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e2a96-169">A filter applied from a data source to a table from another DirectQuery source can only be set on a single column</span></span>

    - <span data-ttu-id="e2a96-170">การกรองข้ามสองตารางในแหล่งข้อมูล DirectQuery โดยการกรองด้วยตารางภายนอกแหล่งข้อมูลไม่ใช่การออกแบบที่แนะนำ และไม่ได้รับการรองรับ</span><span class="sxs-lookup"><span data-stu-id="e2a96-170">Cross-filtering two tables in a DirectQuery source by filtering them with a table outside of the source is not a recommended design, and is not supported.</span></span>

    - <span data-ttu-id="e2a96-171">ตัวกรองสามารถแตะตารางได้เพียงครั้งเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e2a96-171">A filter can only touch a table once.</span></span> <span data-ttu-id="e2a96-172">การใช้ตัวกรองเดียวกันกับตารางสองครั้ง ผ่านหนึ่งในตารางเพิ่มเติมภายนอกของแหล่งข้อมูล DirectQuery ไม่ได้รับการสรองรับ</span><span class="sxs-lookup"><span data-stu-id="e2a96-172">Applying the same filter to a table twice, through one of more tables outside of the DirectQuery source, is not supported.</span></span>

- <span data-ttu-id="e2a96-173">ในระหว่างการแสดงตัวอย่าง ความยาวสูงสุดของการเกี่ยวโยงแบบจำลองคือสาม</span><span class="sxs-lookup"><span data-stu-id="e2a96-173">During preview, the maximum length of a chain of models is three.</span></span> <span data-ttu-id="e2a96-174">การขยายเกินความยาวการเกี่ยวโยงสามระดับไม่ได้รับการรองรับและส่งผลให้เกิดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="e2a96-174">Extending beyond the chain length of three is not supported and results in errors.</span></span> 

- <span data-ttu-id="e2a96-175">การใช้เครื่องมือของบุคคลที่สามสามารถตั้งค่าสถานะ *กีดกันการเกี่ยวโยง* บนแบบจำลองเพื่อป้องกันไม่ให้มีการสร้างหรือขยายการเกี่ยวโยงได้</span><span class="sxs-lookup"><span data-stu-id="e2a96-175">Using third party tools, a *discourage chaining* flag can be set on a model to prevent a chain from being created or extended.</span></span> <span data-ttu-id="e2a96-176">หากต้องการตั้งค่านี้ ให้ค้นหาคุณสมบัติ *DiscourageCompositeModels* บนแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="e2a96-176">To set it, look for the *DiscourageCompositeModels* property on a model.</span></span> 

<span data-ttu-id="e2a96-177">นอกจากนี้ยังมี **ข้อจำกัด** บางอย่างที่คุณจำเป็นต้องทราบดังนี้:</span><span class="sxs-lookup"><span data-stu-id="e2a96-177">There are also a few **limitations** you need to keep in mind:</span></span>

- <span data-ttu-id="e2a96-178">พารามิเตอร์สำหรับฐานข้อมูลและชื่อเซิร์ฟเวอร์ถูกปิดใช้งานในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="e2a96-178">Parameters for database and server names are currently disabled.</span></span> 

- <span data-ttu-id="e2a96-179">การกำหนด RLS บนตารางจากแหล่งข้อมูลระยะไกลไม่ได้รับการรองรับ</span><span class="sxs-lookup"><span data-stu-id="e2a96-179">Defining RLS on tables from a remote source is not supported.</span></span>

- <span data-ttu-id="e2a96-180">การใช้บริการวิเคราะห์ Azure ของเซิร์ฟเวอร์ SQL (SSAS) เป็นแหล่งข้อมูล DirectQuery ไม่ได้รับการรองรับในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="e2a96-180">Using SQL Server Analysis Services (SSAS) as a DirectQuery source is not currently supported.</span></span> 

- <span data-ttu-id="e2a96-181">การใช้ DirectQuery บนชุดข้อมูลจาก "พื้นที่ทำงานของฉัน" ไม่ได้รับรองรับในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="e2a96-181">Using DirectQuery on datasets from “My workspace” is not currently supported.</span></span> 

- <span data-ttu-id="e2a96-182">การลบการเชื่อมต่อไปยังแหล่งข้อมูลระยะไกลที่ใช้ DirectQuery ไม่ได้รับการรองรับในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="e2a96-182">Deleting connections to remote sources that use DirectQuery is not currently supported.</span></span>

- <span data-ttu-id="e2a96-183">การใช้ Power BI แบบฝังตัวกับชุดข้อมูลที่มีการเชื่อมต่อ DirectQuery ไปยังชุดข้อมูล Power BI หรือแบบจำลองบริการวิเคราะห์ Azure ไม่ได้รับการรองรับในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="e2a96-183">Using Power BI Embedded with datasets that include a DirectQuery connection to a Power BI datasets or Azure Analysis Services model is not currently supported.</span></span>

- <span data-ttu-id="e2a96-184">สตริงรูปแบบบนคอลัมน์และหน่วยวัดจากแหล่งข้อมูลระยะไกลจะไม่ถูกนำเข้าไปยังแบบจำลองแบบรวม</span><span class="sxs-lookup"><span data-stu-id="e2a96-184">Format strings on columns and measures from a remote source are not imported to the composite model.</span></span>

- <span data-ttu-id="e2a96-185">กลุ่มการคำนวณบนแหล่งข้อมูลระยะไกลที่มีผลลัพธ์คิวรีที่ไม่ได้กำหนดไว้ไม่ได้รับการรองรับ</span><span class="sxs-lookup"><span data-stu-id="e2a96-185">Calculation groups on remote sources are not supported, with undefined query results.</span></span>

- <span data-ttu-id="e2a96-186">บางคิวรีอาจส่งกลับผลลัพธ์ที่ไม่ถูกต้องเมื่อมีความสัมพันธ์ระหว่างตารางและตารางที่มีการคำนวณในแหล่งข้อมูลระยะไกล</span><span class="sxs-lookup"><span data-stu-id="e2a96-186">Some queries may return wrong results when there's a relationship between calculated tables and table(s) in a remote source.</span></span> <span data-ttu-id="e2a96-187">การสร้างตารางที่มีการคำนวณบนชุดข้อมูลระยะไกลไม่ได้รับการรองรับแม้ว่าจะไม่มีการบล็อกในอินเทอร์เฟซอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="e2a96-187">Creating calculated tables over a remote dataset isn't supported, although it isn't currently blocked in the interface.</span></span>

- <span data-ttu-id="e2a96-188">ไม่รองรับการเรียงลำดับตามคอลัมน์ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="e2a96-188">Sort by column isn't supported at this time.</span></span>

- <span data-ttu-id="e2a96-189">การรีเฟรชหน้าอัตโนมัติ (APR) ได้รับการรองรับเฉพาะสำหรับบางสถานการณ์โดยขึ้นอยู่กับชนิดแหล่งข้อมูลเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e2a96-189">Automatic page refresh (APR) is only supported for some scenarios, depending on the data source type.</span></span> <span data-ttu-id="e2a96-190">ดูบทความ[การรีเฟรชหน้าอัตโนมัติใน Power BI](../create-reports/desktop-automatic-page-refresh.md) สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e2a96-190">See the article [Automatic page refresh in Power BI](../create-reports/desktop-automatic-page-refresh.md) for more information.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e2a96-191">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="e2a96-191">Next steps</span></span>

<span data-ttu-id="e2a96-192">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ DirectQuery โปรดดูที่ทรัพยากรดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e2a96-192">For more information about DirectQuery, check out the following resources:</span></span>

- [<span data-ttu-id="e2a96-193">ใช้ DirectQuery ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e2a96-193">Use DirectQuery in Power BI Desktop</span></span>](desktop-use-directquery.md)
- [<span data-ttu-id="e2a96-194">แบบจำลอง DirectQuery ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e2a96-194">DirectQuery models in Power BI Desktop</span></span>](desktop-directquery-about.md)
- [<span data-ttu-id="e2a96-195">คำแนะนำแบบจำลอง DirectQuery ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e2a96-195">DirectQuery model guidance in Power BI Desktop</span></span>](../guidance/directquery-model-guidance.md)
- <span data-ttu-id="e2a96-196">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="e2a96-196">Questions?</span></span> [<span data-ttu-id="e2a96-197">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="e2a96-197">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
