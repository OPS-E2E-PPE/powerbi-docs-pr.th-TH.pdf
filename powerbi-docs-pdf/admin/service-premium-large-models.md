---
title: ชุดข้อมูลขนาดใหญ่ใน Power BI Premium
description: รูปแบบพื้นที่จัดเก็บชุดข้อมูลขนาดใหญ่ช่วยให้ชุดข้อมูลใน Power BI Premium ขยายขนาดเกิน 10 GB ได้
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-premium
ms.topic: how-to
ms.date: 12/10/2020
ms.custom: references_regions
LocalizationGroup: Premium
ms.openlocfilehash: 7256e17f561aa79d63b7fefd268df560903de6b2
ms.sourcegitcommit: 772c65b7b440ab082510bf3f64b871d19139d451
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/12/2020
ms.locfileid: "97353116"
---
# <a name="large-datasets-in-power-bi-premium"></a><span data-ttu-id="20e49-103">ชุดข้อมูลขนาดใหญ่ใน Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="20e49-103">Large datasets in Power BI Premium</span></span>

<span data-ttu-id="20e49-104">ชุดข้อมูล Power BI สามารถเก็บข้อมูลในแคชที่บีบอัดสูง แคชในหน่วยความจำสำหรับประสิทธิภาพการค้นหาที่ดีที่สุดเพื่อเปิดใช้งานการโต้ตอบกับผู้ใช้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="20e49-104">Power BI datasets can store data in a highly compressed in-memory cache for optimized query performance, enabling fast user interactivity.</span></span> <span data-ttu-id="20e49-105">ด้วยความจุแบบ Premium ชุดข้อมูลขนาดใหญ่เกินขีดจำกัดค่าเริ่มต้น 10 GB สามารถเปิดใช้งานได้ด้วยการตั้งค่า **รูปแบบพื้นที่จัดเก็บชุดข้อมูลขนาดใหญ่**</span><span class="sxs-lookup"><span data-stu-id="20e49-105">With Premium capacities, large datasets beyond the default 10 GB limit can be enabled with the **Large dataset storage format** setting.</span></span> <span data-ttu-id="20e49-106">เมื่อเปิดใช้งาน ขนาดชุดข้อมูลจะถูกจํากัดตามขนาด *ความจุ* แบบพรีเมียมหรือขนาดสูงสุดที่กำหนดโดยผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="20e49-106">When enabled, dataset size is limited by the Premium *capacity* size or the maximum size set by the administrator.</span></span>

<span data-ttu-id="20e49-107">สามารถเปิดใช้งานชุดข้อมูลขนาดใหญ่สำหรับ Premium P SKUs และ Embedded A SKU ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="20e49-107">Large datasets can be enabled for all Premium P SKUs and Embedded A SKUs.</span></span> <span data-ttu-id="20e49-108">ขีดจำกัดขนาดชุดข้อมูลขนาดใหญ่ใน Premium เทียบได้กับ Azure Analysis Services ในแง่ของข้อจำกัดขนาดแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="20e49-108">The large dataset size limit in Premium is comparable to Azure Analysis Services, in terms of data model size limitations.</span></span>

<span data-ttu-id="20e49-109">แม้ว่าชุดข้อมูลจะต้องมีขนาดเกิน 10 GB แต่การเปิดใช้การตั้งค่ารูปแบบพื้นที่จัดเก็บข้อมูลขนาดใหญ่จะมีประโยชน์เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="20e49-109">While required for datasets to grow beyond 10 GB, enabling the Large dataset storage format setting has additional benefits.</span></span> <span data-ttu-id="20e49-110">หากคุณวางแผนที่จะใช้เครื่องมือที่ใช้ตำแหน่งข้อมูล XMLA สำหรับการดำเนินการเขียนชุดข้อมูล อย่าลืมเปิดใช้งานการตั้งค่าแม้แต่สำหรับชุดข้อมูลที่คุณไม่จำเป็นต้องกำหนดลักษณะเป็นชุดข้อมูล *ขนาดใหญ่*</span><span class="sxs-lookup"><span data-stu-id="20e49-110">If you're planning to use XMLA endpoint based tools for dataset write operations, be sure to enable the  setting, even for datasets that you wouldn't necessarily characterize as a *large* dataset.</span></span> <span data-ttu-id="20e49-111">เมื่อเปิดใช้งาน รูปแบบพื้นที่จัดเก็บชุดข้อมูลขนาดใหญ่สามารถปรับปรุงประสิทธิภาพการดำเนินการเขียน XMLA ได้</span><span class="sxs-lookup"><span data-stu-id="20e49-111">When enabled, the large dataset storage format can improve XMLA write operations performance.</span></span>

<span data-ttu-id="20e49-112">ชุดข้อมูลขนาดใหญ่ในบริการจะไม่ส่งผลต่อขนาดการอัปโหลดแบบจำลอง Power BI Desktop ซึ่งยังจำกัดไว้ที่ 10 GB</span><span class="sxs-lookup"><span data-stu-id="20e49-112">Large datasets in the service do not affect the Power BI Desktop model upload size, which is still limited to 10 GB.</span></span> <span data-ttu-id="20e49-113">แต่ชุดข้อมูลในบริการจะขยายเกินกว่า 10 GB เมื่อรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="20e49-113">Instead, datasets can grow beyond 10 GB in the service on refresh.</span></span>

## <a name="enable-large-datasets"></a><span data-ttu-id="20e49-114">เปิดใช้งานชุดข้อมูลขนาดใหญ่</span><span class="sxs-lookup"><span data-stu-id="20e49-114">Enable large datasets</span></span>

<span data-ttu-id="20e49-115">ขั้นตอนที่นี่อธิบายการเปิดใช้งานชุดข้อมูลขนาดใหญ่สำหรับแบบจำลองใหม่ที่เผยแพร่ไปยังบริการ</span><span class="sxs-lookup"><span data-stu-id="20e49-115">Steps here describe enabling large datasets for a new model published to the service.</span></span> <span data-ttu-id="20e49-116">สำหรับชุดข้อมูลที่มีอยู่ เฉพาะขั้นตอนที่สามเท่านั้นที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="20e49-116">For existing datasets, only step three is necessary.</span></span>

1. <span data-ttu-id="20e49-117">สร้างแบบจำลองใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="20e49-117">Create a model in Power BI Desktop.</span></span> <span data-ttu-id="20e49-118">หากชุดข้อมูลของคุณมีขนาดใหญ่ขึ้นและใช้หน่วยความจำมากขึ้นเรื่อย ๆ อย่าลืมกำหนดค่า[การรีเฟรชแบบเพิ่มหน่วย](service-premium-incremental-refresh.md)</span><span class="sxs-lookup"><span data-stu-id="20e49-118">If your dataset will become larger and progressively consume more memory, be sure to configure [Incremental refresh](service-premium-incremental-refresh.md).</span></span>

1. <span data-ttu-id="20e49-119">เผยแพร่แบบจำลองในฐานะชุดข้อมูลไปยังบริการ</span><span class="sxs-lookup"><span data-stu-id="20e49-119">Publish the model as a dataset to the service.</span></span>

1. <span data-ttu-id="20e49-120">ในบริการ > ชุดข้อมูล > **การตั้งค่า** ให้ขยาย **รูปแบบพื้นที่จัดเก็บชุดข้อมูลขนาดใหญ่** จากนั้นคลิกแถบเลื่อนไปที่ **เปิด** จากนั้นคลิก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="20e49-120">In the service > dataset > **Settings**, expand **Large dataset storage format**, click the slider to **On**, and then click **Apply**.</span></span>

    :::image type="content" source="media/service-premium-large-models/enable-large-dataset.png" alt-text="เปิดใช้งานตัวเลื่อนชุดข้อมูลขนาดใหญ่":::

1. <span data-ttu-id="20e49-122">เรียกใช้การรีเฟรชเพื่อโหลดข้อมูลที่ถูกเก็บมาก่อนหน้าโดยยึดตามนโยบายการรีเฟรชแบบเพิ่มหน่วย</span><span class="sxs-lookup"><span data-stu-id="20e49-122">Invoke a refresh to load historical data based on the incremental refresh policy.</span></span> <span data-ttu-id="20e49-123">การรีเฟรชครั้งแรกอาจใช้เวลาสักครู่เพื่อโหลดประวัติ</span><span class="sxs-lookup"><span data-stu-id="20e49-123">The first refresh could take a while to load the history.</span></span> <span data-ttu-id="20e49-124">การรีเฟรชที่ตามมาในภายหลังควรเร็วขึ้น ทั้งนี้ขึ้นอยู่กับนโยบายการรีเฟรชแบบเพิ่มหน่วยของคุณ</span><span class="sxs-lookup"><span data-stu-id="20e49-124">Subsequent refreshes should be faster, depending on your incremental refresh policy.</span></span>

## <a name="set-default-storage-format"></a><span data-ttu-id="20e49-125">กำหนดรูปแบบพื้นที่จัดเก็บเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="20e49-125">Set default storage format</span></span>

<span data-ttu-id="20e49-126">ชุดข้อมูลใหม่ทั้งหมดที่สร้างขึ้นในพื้นที่ทำงานที่กำหนดให้กับความจุระดับ Premium สามารถเปิดใช้งานรูปแบบพื้นที่จัดเก็บชุดข้อมูลขนาดใหญ่ได้ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="20e49-126">All new datasets created in a workspace assigned to Premium capacity can have the large dataset storage format enabled by default.</span></span>

1. <span data-ttu-id="20e49-127">ในพื้นที่ทำงาน ให้คลิก **การตั้งค่า** > **Premium**</span><span class="sxs-lookup"><span data-stu-id="20e49-127">In the workspace, click **Settings** > **Premium**.</span></span>

1. <span data-ttu-id="20e49-128">ใน **รูปแบบพื้นที่จัดเก็บเริ่มต้น** ให้เลือก **รูปแบบพื้นที่จัดเก็บชุดข้อมูลขนาดใหญ่** จากนั้นคลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="20e49-128">In **Default storage format**, select **Large dataset storage format**, and then click **Save**.</span></span>

    :::image type="content" source="media/service-premium-large-models/default-storage-format.png" alt-text="เปิดใช้งานรูปแบบพื้นที่จัดเก็บเริ่มต้น":::

### <a name="enable-with-powershell"></a><span data-ttu-id="20e49-130">เปิดใช้งานด้วย PowerShell</span><span class="sxs-lookup"><span data-stu-id="20e49-130">Enable with PowerShell</span></span>

<span data-ttu-id="20e49-131">คุณยังสามารถเปิดใช้งานรูปแบบพื้นที่จัดเก็บชุดข้อมูลขนาดใหญ่ได้โดยใช้ PowerShell</span><span class="sxs-lookup"><span data-stu-id="20e49-131">You can also enable large dataset storage format by using PowerShell.</span></span> <span data-ttu-id="20e49-132">คุณต้องมีสิทธิ์ของผู้ดูแลความจุและผู้ดูแลพื้นที่ทำงานของเพื่อเรียกใช้ cmdlet ของ PowerShell</span><span class="sxs-lookup"><span data-stu-id="20e49-132">You must have capacity admin and workspace admin privileges to run the PowerShell cmdlets.</span></span>

1. <span data-ttu-id="20e49-133">ค้นหา ID ของชุดข้อมูล (GUID)</span><span class="sxs-lookup"><span data-stu-id="20e49-133">Find the dataset ID (GUID).</span></span> <span data-ttu-id="20e49-134">บนแท็บ **ชุดข้อมูล** สำหรับพื้นที่ทำงานภายใต้การตั้งค่าชุดข้อมูล คุณสามารถดู ID ใน URL ได้</span><span class="sxs-lookup"><span data-stu-id="20e49-134">On the **Datasets** tab for the workspace, under the dataset settings, you can see the ID in the URL.</span></span>

    ![GUID ของชุดข้อมูล](media/service-premium-large-models/dataset-guid.png)

1. <span data-ttu-id="20e49-136">จากพร้อมท์ผู้ดูแลระบบ PowerShell ให้ติดตั้งโมดูล [MicrosoftPowerBIMgmt](/powershell/module/microsoftpowerbimgmt.data/)</span><span class="sxs-lookup"><span data-stu-id="20e49-136">From a PowerShell admin prompt, install the [MicrosoftPowerBIMgmt](/powershell/module/microsoftpowerbimgmt.data/) module.</span></span>

    ```powershell
    Install-Module -Name MicrosoftPowerBIMgmt
    ```

1. <span data-ttu-id="20e49-137">เรียกใช้ cmdlets ต่อไปนี้เพื่อลงชื่อเข้าใช้และตรวจสอบโหมดที่เก็บชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="20e49-137">Run the following cmdlets to sign in and check the dataset storage mode.</span></span>

    ```powershell
    Login-PowerBIServiceAccount

    (Get-PowerBIDataset -Scope Organization -Id <Dataset ID> -Include actualStorage).ActualStorage
    ```

    <span data-ttu-id="20e49-138">การตอบสนองควรเป็นดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="20e49-138">The response should be the following.</span></span> <span data-ttu-id="20e49-139">โหมดที่เก็บข้อมูลเป็น ABF (ไฟล์สำรองข้อมูล Analysis Services) ซึ่งเป็นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="20e49-139">The storage mode is ABF (Analysis Services backup file), which is the default.</span></span>

    ```
    Id                   StorageMode

    --                   -----------

    <Dataset ID>         Abf
    ```

1. <span data-ttu-id="20e49-140">เรียกใช้ cmdlets ต่อไปนี้เพื่อตั้งค่าโหมดพื้นที่เก็บข้อมูล</span><span class="sxs-lookup"><span data-stu-id="20e49-140">Run the following cmdlets to set the storage mode.</span></span> <span data-ttu-id="20e49-141">อาจใช้เวลาสองถึงสามวินาทีในการแปลงเป็น Premium Files</span><span class="sxs-lookup"><span data-stu-id="20e49-141">It can take a few seconds to convert to Premium Files.</span></span>

    ```powershell
    Set-PowerBIDataset -Id <Dataset ID> -TargetStorageMode PremiumFiles

    (Get-PowerBIDataset -Scope Organization -Id <Dataset ID> -Include actualStorage).ActualStorage
    ```

    <span data-ttu-id="20e49-142">การตอบสนองควรเป็นดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="20e49-142">The response should be the following.</span></span> <span data-ttu-id="20e49-143">ขณะนี้โหมดที่เก็บข้อมูลถูกตั้งค่าเป็น Premium Files</span><span class="sxs-lookup"><span data-stu-id="20e49-143">The storage mode is now set to Premium Files.</span></span>

    ```
    Id                   StorageMode
    
    --                   -----------
    
    <Dataset ID>         PremiumFiles
    ```

<span data-ttu-id="20e49-144">คุณสามารถตรวจสอบสถานะของการแปลงชุดข้อมูลไปยังและจากไฟล์พรีเมียมโดยใช้ cmdlet [Get-PowerBIWorkspaceMigrationStatus](/powershell/module/microsoftpowerbimgmt.workspaces/get-powerbiworkspacemigrationstatus)</span><span class="sxs-lookup"><span data-stu-id="20e49-144">You can check the status of dataset conversions to and from Premium Files by using the [Get-PowerBIWorkspaceMigrationStatus](/powershell/module/microsoftpowerbimgmt.workspaces/get-powerbiworkspacemigrationstatus) cmdlet.</span></span>

## <a name="dataset-eviction"></a><span data-ttu-id="20e49-145">การลดสัดส่วนชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="20e49-145">Dataset eviction</span></span>

<span data-ttu-id="20e49-146">Power BI ใช้การจัดการหน่วยความจำแบบไดนามิกเพื่อลดสันส่วนชุดข้อมูลที่ไม่ใช้งานจากหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="20e49-146">Power BI uses dynamic memory management to evict inactive datasets from memory.</span></span> <span data-ttu-id="20e49-147">Power BI ลดสันส่วนชุดข้อมูลเพื่อให้สามารถโหลดชุดข้อมูลอื่น ๆ เพื่อจัดการกับคิวรีของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="20e49-147">Power BI evicts datasets so it can load other datasets to address user queries.</span></span> <span data-ttu-id="20e49-148">การจัดการหน่วยความจำแบบไดนามิกช่วยให้ผลรวมของขนาดชุดข้อมูลมากกว่าหน่วยความจำที่มีอยู่ในความจุอย่างมีนัยสำคัญ แต่ชุดข้อมูลเดียวจะต้องพอดีกับหน่วยความจำ</span><span class="sxs-lookup"><span data-stu-id="20e49-148">Dynamic memory management allows the sum of dataset sizes to be significantly greater than the memory available on the capacity, but a single dataset must fit into memory.</span></span> <span data-ttu-id="20e49-149">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดการหน่วยความจำแบบไดนามิก โปรดดูที่ [วิธีการทำงานของความจุ](service-premium-what-is.md#how-capacities-function)</span><span class="sxs-lookup"><span data-stu-id="20e49-149">For more info on dynamic memory management, see [How capacities function](service-premium-what-is.md#how-capacities-function).</span></span>

<span data-ttu-id="20e49-150">คุณควรพิจารณาผลกระทบของการลดสัดส่วนในแบบจำลองขนาดใหญ่</span><span class="sxs-lookup"><span data-stu-id="20e49-150">You should consider the impact of eviction on large models.</span></span> <span data-ttu-id="20e49-151">แม้ว่าเวลาโหลดชุดข้อมูลจะค่อนข้างเร็ว แต่ก็อาจมีความล่าช้าที่เห็นได้ชัดสำหรับผู้ใช้หากต้องรอการโหลดชุดข้อมูลขนาดใหญ่ที่ถูกตัดออก</span><span class="sxs-lookup"><span data-stu-id="20e49-151">Despite relatively fast dataset load times, there could still be a noticeable delay for users if they have to wait for large evicted datasets to be reloaded.</span></span> <span data-ttu-id="20e49-152">ด้วยเหตุผลนี้ ในรูปแบบปัจจุบัน ฟีเจอร์โมเดลขนาดใหญ่จึงเป็นที่แนะนำอย่างมากสำหรับความจุที่เฉพาะกับข้อกำหนด BI ขององค์กรแทนอันที่ผสมกับข้อกำหนด BI แบบบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="20e49-152">For this reason, in its current form, the large models feature is recommended primarily for capacities dedicated to enterprise BI requirements rather than capacities mixed with self-service BI requirements.</span></span> <span data-ttu-id="20e49-153">ความจุที่เฉพาะกับข้อกำหนดด้าน BI ขององค์กรมีโอกาสน้อยที่จะทำให้เกิดการลดสัดส่วนข้อมูลและต้องการโหลดชุดข้อมูลซ้ำ</span><span class="sxs-lookup"><span data-stu-id="20e49-153">Capacities dedicated to enterprise BI requirements are less likely to frequently trigger eviction and need to reload datasets.</span></span> <span data-ttu-id="20e49-154">ในทางกลับกันความจุสำหรับ BI แบบบริการตนเองอาจมีชุดข้อมูลขนาดเล็กจำนวนมากที่โหลดเข้าและออกจากหน่วยความจำบ่อยกว่า</span><span class="sxs-lookup"><span data-stu-id="20e49-154">Capacities for self-service BI on the other hand can have many small datasets that are more frequently loaded in and out of memory.</span></span>

## <a name="checking-dataset-size"></a><span data-ttu-id="20e49-155">ตรวจสอบขนาดของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="20e49-155">Checking dataset size</span></span>

<span data-ttu-id="20e49-156">หลังจากโหลดข้อมูลที่ถูกเก็บมาก่อนหน้าแล้ว คุณสามารถใช้ [SSMS](/sql/ssms/download-sql-server-management-studio-ssms) ถึง [จุดปลายทาง XMLA](service-premium-connect-tools.md) เพื่อตรวจสอบขนาดชุดข้อมูลโดยประมาณในหน้าต่างคุณสมบัติของแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="20e49-156">After loading historical data, you can use [SSMS](/sql/ssms/download-sql-server-management-studio-ssms) through the [XMLA endpoint](service-premium-connect-tools.md) to check the estimated dataset size in the model properties window.</span></span>

![ขนาดของชุดข้อมูลโดยประมาณ](media/service-premium-large-models/estimated-dataset-size.png)

<span data-ttu-id="20e49-158">คุณยังสามารถตรวจสอบขนาดของชุดข้อมูลโดยการเรียกใช้คิวรี DMV ต่อไปนี้จาก SSMS ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="20e49-158">You can also check the dataset size by running the following DMV queries from SSMS.</span></span> <span data-ttu-id="20e49-159">รวมขคอลัมน์ DICTIONARY\_SIZE และ USED\_SIZE จากผลผลิตเพื่อดูขนาดของชุดข้อมูลเป็นหน่วยไบต์</span><span class="sxs-lookup"><span data-stu-id="20e49-159">Sum the DICTIONARY\_SIZE and USED\_SIZE columns from the output to see the dataset size in bytes.</span></span>

```sql
SELECT * FROM SYSTEMRESTRICTSCHEMA
($System.DISCOVER_STORAGE_TABLE_COLUMNS,
 [DATABASE_NAME] = '<Dataset Name>') //Sum DICTIONARY_SIZE (bytes)

SELECT * FROM SYSTEMRESTRICTSCHEMA
($System.DISCOVER_STORAGE_TABLE_COLUMN_SEGMENTS,
 [DATABASE_NAME] = '<Dataset Name>') //Sum USED_SIZE (bytes)
```

## <a name="limitations-and-considerations"></a><span data-ttu-id="20e49-160">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="20e49-160">Limitations and considerations</span></span>

<span data-ttu-id="20e49-161">โปรดคำนึงถึงข้อจำกัดต่อไปนี้เมื่อใช้ชุดข้อมูลขนาดใหญ่:</span><span class="sxs-lookup"><span data-stu-id="20e49-161">Keep in mind the following restrictions when using large datasets:</span></span>

- <span data-ttu-id="20e49-162">**จำเป็นต้องมีพื้นที่ทำงานใหม่**: ชุดข้อมูลขนาดใหญ่สามารถใช้งานได้กับ [พื้นที่ทำงานใหม่](../collaborate-share/service-create-the-new-workspaces.md)เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="20e49-162">**New workspaces are required**: Large datasets only work with [New workspaces](../collaborate-share/service-create-the-new-workspaces.md).</span></span>

- <span data-ttu-id="20e49-163">**ดาวน์โหลดไปยัง Power BI Desktop** : ถ้ามีการจัดเก็บชุดข้อมูลบน Premium Files [การดาวน์โหลดเป็นไฟล์ .pbix](../create-reports/service-export-to-pbix.md) จะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="20e49-163">**Download to Power BI Desktop**: If a dataset is stored on Premium Files, [downloading as a .pbix](../create-reports/service-export-to-pbix.md) file will fail.</span></span>
- <span data-ttu-id="20e49-164">**ภูมิภาคที่รองรับ**: ชุดข้อมูลขนาดใหญ่ได้รับการสนับสนุนในภูมิภาค Azure ทั้งหมดที่สนับสนุนการจัดเก็บไฟล์ Premium</span><span class="sxs-lookup"><span data-stu-id="20e49-164">**Supported regions**: Large datasets are supported in all Azure regions that support Premium Files Storage.</span></span> <span data-ttu-id="20e49-165">หากต้องการเรียนรู้เพิ่มเติม โปรดดู[ผลิตภัณฑ์ที่พร้อมใช้งานตามภูมิภาค](https://azure.microsoft.com/global-infrastructure/services/?products=storage)และดูตารางในส่วนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="20e49-165">To learn more, see [Products available by region](https://azure.microsoft.com/global-infrastructure/services/?products=storage), and consult the table in the following section.</span></span>

- <span data-ttu-id="20e49-166">**การตั้งค่าขนาดชุดข้อมูลสูงสุด**: ขนาดชุดข้อมูลสูงสุดสามารถตั้งค่าได้โดยผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="20e49-166">**Setting maximum dataset size**: Maximum dataset size can be set by administrators.</span></span> <span data-ttu-id="20e49-167">ค่าสูงสุดสามารถตั้งค่าได้ตั้งแต่ 0.1 GB จนถึงความจุสูงสุดของ SKU</span><span class="sxs-lookup"><span data-stu-id="20e49-167">Maximum value can be set from 0.1 GB up to the maximum capacity of the SKU.</span></span>

## <a name="region-availability"></a><span data-ttu-id="20e49-168">ความพร้อมใช้งานของภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="20e49-168">Region availability</span></span>

<span data-ttu-id="20e49-169">ชุดข้อมูลขนาดใหญ่ใน Power BI สามารถใช้งานได้ในเฉพาะในภูมิภาคของ Azure ที่รองรับ[พื้นที่เก็บข้อมูลไฟล์ Azure Premium](/azure/storage/files/storage-files-planning#storage-tiers)</span><span class="sxs-lookup"><span data-stu-id="20e49-169">Large datasets in Power BI are only available in certain Azure regions that support [Azure Premium Files Storage](/azure/storage/files/storage-files-planning#storage-tiers).</span></span>

<span data-ttu-id="20e49-170">รายการต่อไปนี้แสดงภูมิภาคที่มีชุดข้อมูลขนาดใหญ่ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="20e49-170">The following list provides regions where large datasets in Power BI are available.</span></span> <span data-ttu-id="20e49-171">ภูมิภาคที่ไม่ได้อยู่ในรายการต่อไปนี้ไม่ได้รับการรองรับสำหรับโมเดลที่มีขนาดใหญ่:</span><span class="sxs-lookup"><span data-stu-id="20e49-171">Regions not in the following list are not supported for large models:</span></span>

|<span data-ttu-id="20e49-172">ภูมิภาค Azure</span><span class="sxs-lookup"><span data-stu-id="20e49-172">Azure region</span></span>  |<span data-ttu-id="20e49-173">ตัวย่อภูมิภาคของ Azure</span><span class="sxs-lookup"><span data-stu-id="20e49-173">Azure region abbreviation</span></span>  |
|---------|---------|
|<span data-ttu-id="20e49-174">ออสเตรเลียตะวันออก</span><span class="sxs-lookup"><span data-stu-id="20e49-174">Australia East</span></span>     | <span data-ttu-id="20e49-175">ออสเตรเลียตะวันออก</span><span class="sxs-lookup"><span data-stu-id="20e49-175">australiaeast</span></span>        |
|<span data-ttu-id="20e49-176">ออสเตรเลียตะวันออกเฉียงใต้</span><span class="sxs-lookup"><span data-stu-id="20e49-176">Australia Southeast</span></span>     | <span data-ttu-id="20e49-177">ออสเตรเลียตะวันออกเฉียงใต้</span><span class="sxs-lookup"><span data-stu-id="20e49-177">australiasoutheast</span></span>        |
|<span data-ttu-id="20e49-178">แคนาดาตะวันออก</span><span class="sxs-lookup"><span data-stu-id="20e49-178">Canada East</span></span>     | <span data-ttu-id="20e49-179">แคนาดาตะวันออก</span><span class="sxs-lookup"><span data-stu-id="20e49-179">canadaeast</span></span>        |
|<span data-ttu-id="20e49-180">แคนาดาตอนกลาง</span><span class="sxs-lookup"><span data-stu-id="20e49-180">Canada Central</span></span>     | <span data-ttu-id="20e49-181">แคนาดาตอนกลาง</span><span class="sxs-lookup"><span data-stu-id="20e49-181">canadacentral</span></span>        |
|<span data-ttu-id="20e49-182">อินเดียตอนกลาง</span><span class="sxs-lookup"><span data-stu-id="20e49-182">Central India</span></span>     | <span data-ttu-id="20e49-183">อินเดียตอนกลาง</span><span class="sxs-lookup"><span data-stu-id="20e49-183">centralindia</span></span>        |
|<span data-ttu-id="20e49-184">สหรัฐอเมริกาตอนกลาง</span><span class="sxs-lookup"><span data-stu-id="20e49-184">Central US</span></span>     | <span data-ttu-id="20e49-185">สหรัฐอเมริกาตอนกลาง</span><span class="sxs-lookup"><span data-stu-id="20e49-185">centralus</span></span>        |
|<span data-ttu-id="20e49-186">เอเชียตะวันออก</span><span class="sxs-lookup"><span data-stu-id="20e49-186">East Asia</span></span>     | <span data-ttu-id="20e49-187">เอเชียตะวันออก</span><span class="sxs-lookup"><span data-stu-id="20e49-187">eastasia</span></span>        |
|<span data-ttu-id="20e49-188">สหรัฐอเมริกาฝั่งตะวันออก</span><span class="sxs-lookup"><span data-stu-id="20e49-188">East US</span></span>     | <span data-ttu-id="20e49-189">สหรัฐอเมริกาตะวันออก</span><span class="sxs-lookup"><span data-stu-id="20e49-189">eastus</span></span>        |
|<span data-ttu-id="20e49-190">สหรัฐอเมริกาฝั่งตะวันออก 2</span><span class="sxs-lookup"><span data-stu-id="20e49-190">East US 2</span></span>     | <span data-ttu-id="20e49-191">สหรัฐอเมริกาตะวันออก 2</span><span class="sxs-lookup"><span data-stu-id="20e49-191">eastus2</span></span>        |
|<span data-ttu-id="20e49-192">ญี่ปุ่นฝั่งตะวันออก</span><span class="sxs-lookup"><span data-stu-id="20e49-192">Japan East</span></span>     | <span data-ttu-id="20e49-193">ญี่ปุ่นตะวันออก</span><span class="sxs-lookup"><span data-stu-id="20e49-193">japaneast</span></span>        |
|<span data-ttu-id="20e49-194">ญี่ปุ่นตะวันตก</span><span class="sxs-lookup"><span data-stu-id="20e49-194">Japan West</span></span>     | <span data-ttu-id="20e49-195">ญี่ปุ่นตะวันออก</span><span class="sxs-lookup"><span data-stu-id="20e49-195">japanwest</span></span>        |
|<span data-ttu-id="20e49-196">เกาหลีตอนกลาง</span><span class="sxs-lookup"><span data-stu-id="20e49-196">Korea Central</span></span>     | <span data-ttu-id="20e49-197">เกาหลีตอนกลาง</span><span class="sxs-lookup"><span data-stu-id="20e49-197">koreacentral</span></span>        |
|<span data-ttu-id="20e49-198">เกาหลีตอนใต้</span><span class="sxs-lookup"><span data-stu-id="20e49-198">Korea South</span></span>     | <span data-ttu-id="20e49-199">เกาหลีตอนใต้</span><span class="sxs-lookup"><span data-stu-id="20e49-199">koreasouth</span></span>        |
|<span data-ttu-id="20e49-200">สหรัฐอเมริกาตอนกลางทางเหนือ</span><span class="sxs-lookup"><span data-stu-id="20e49-200">North Central US</span></span>     | <span data-ttu-id="20e49-201">สหรัฐอเมริกากลางตอนเหนือ</span><span class="sxs-lookup"><span data-stu-id="20e49-201">northcentralus</span></span>        |
|<span data-ttu-id="20e49-202">ยุโรปเหนือ</span><span class="sxs-lookup"><span data-stu-id="20e49-202">North Europe</span></span>     | <span data-ttu-id="20e49-203">ยุโรปตอนเหนือ</span><span class="sxs-lookup"><span data-stu-id="20e49-203">northeurope</span></span>        |
|<span data-ttu-id="20e49-204">สหรัฐอเมริกาตอนกลางทางใต้</span><span class="sxs-lookup"><span data-stu-id="20e49-204">South Central US</span></span>     | <span data-ttu-id="20e49-205">สหรัฐอเมริกากลางตอนใต้</span><span class="sxs-lookup"><span data-stu-id="20e49-205">southcentralus</span></span>        |
|<span data-ttu-id="20e49-206">เอเชียตะวันออกเฉียงใต้</span><span class="sxs-lookup"><span data-stu-id="20e49-206">Southeast Asia</span></span>     | <span data-ttu-id="20e49-207">เอเชียตะวันออกเฉียงใต้</span><span class="sxs-lookup"><span data-stu-id="20e49-207">southeastasia</span></span>        |
|<span data-ttu-id="20e49-208">สหราชอาณาจักรตอนใต้</span><span class="sxs-lookup"><span data-stu-id="20e49-208">UK South</span></span>     | <span data-ttu-id="20e49-209">สหราชอาณาจักรตอนใต้</span><span class="sxs-lookup"><span data-stu-id="20e49-209">uksouth</span></span>        |
|<span data-ttu-id="20e49-210">สหราชอาณาจักรตะวันตก</span><span class="sxs-lookup"><span data-stu-id="20e49-210">UK West</span></span>     | <span data-ttu-id="20e49-211">สหราชอาณาจักรตะวันตก</span><span class="sxs-lookup"><span data-stu-id="20e49-211">ukwest</span></span>        |
|<span data-ttu-id="20e49-212">ยุโรปตะวันตก</span><span class="sxs-lookup"><span data-stu-id="20e49-212">West Europe</span></span>     | <span data-ttu-id="20e49-213">ยุโรปตะวันตก</span><span class="sxs-lookup"><span data-stu-id="20e49-213">westeurope</span></span>        |
|<span data-ttu-id="20e49-214">อินเดียตะวันตก</span><span class="sxs-lookup"><span data-stu-id="20e49-214">West India</span></span>     | <span data-ttu-id="20e49-215">อินเดียตะวันตก</span><span class="sxs-lookup"><span data-stu-id="20e49-215">westindia</span></span>        |
|<span data-ttu-id="20e49-216">สหรัฐอเมริกาตะวันตก</span><span class="sxs-lookup"><span data-stu-id="20e49-216">West US</span></span>     | <span data-ttu-id="20e49-217">สหรัฐอเมริกาตะวันตก</span><span class="sxs-lookup"><span data-stu-id="20e49-217">westus</span></span>        |
|<span data-ttu-id="20e49-218">US 2 ตะวันตก</span><span class="sxs-lookup"><span data-stu-id="20e49-218">West US 2</span></span>     | <span data-ttu-id="20e49-219">สหรัฐอเมริกาตะวันตก 2</span><span class="sxs-lookup"><span data-stu-id="20e49-219">westus2</span></span>        |

## <a name="next-steps"></a><span data-ttu-id="20e49-220">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="20e49-220">Next steps</span></span>

<span data-ttu-id="20e49-221">ลิงก์ต่อไปนี้จะให้ข้อมูลที่มีประโยชน์สำหรับการทำงานกับโมเดลขนาดใหญ่:</span><span class="sxs-lookup"><span data-stu-id="20e49-221">The following links provide information that can be useful for working with large models:</span></span>

* [<span data-ttu-id="20e49-222">ที่เก็บไฟล์ Azure Premium</span><span class="sxs-lookup"><span data-stu-id="20e49-222">Azure Premium Files Storage</span></span>](/azure/storage/files/storage-files-planning#storage-tiers)
* [<span data-ttu-id="20e49-223">กำหนดค่าการสนับสนุน Multi-Geo สำหรับ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="20e49-223">Configure Multi-Geo support for Power BI Premium</span></span>](service-admin-premium-multi-geo.md)
* [<span data-ttu-id="20e49-224">นำคีย์การเข้ารหัสลับของคุณเองมาใช้กับ Power BI</span><span class="sxs-lookup"><span data-stu-id="20e49-224">Bring your own encryption keys for Power BI</span></span>](service-encryption-byok.md)
* [<span data-ttu-id="20e49-225">วิธีการทำงานของความจุ</span><span class="sxs-lookup"><span data-stu-id="20e49-225">How capacities function</span></span>](service-premium-what-is.md#how-capacities-function)
* <span data-ttu-id="20e49-226">[การรีเฟรชแบบเพิ่มหน่วย](service-premium-incremental-refresh.md)</span><span class="sxs-lookup"><span data-stu-id="20e49-226">[Incremental refresh](service-premium-incremental-refresh.md).</span></span>

<span data-ttu-id="20e49-227">Power BI ได้แนะนำ Power BI Premium Gen2 เข้ามาใช้งานเป็นข้อเสนอการแสดงตัวอย่าง ซึ่งปรับปรุงประสบการณ์การใช้งาน Power BI Premium ด้วยการปรับปรุงในสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="20e49-227">Power BI has introduced Power BI Premium Gen2 as a preview offering, which improves the Power BI Premium experience with improvements in the following:</span></span>
* <span data-ttu-id="20e49-228">ประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="20e49-228">Performance</span></span>
* <span data-ttu-id="20e49-229">สิทธิการใช้งานต่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="20e49-229">Per-user licensing</span></span>
* <span data-ttu-id="20e49-230">ขนาดใหญ่ขึ้น</span><span class="sxs-lookup"><span data-stu-id="20e49-230">Greater scale</span></span>
* <span data-ttu-id="20e49-231">เมตริกที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="20e49-231">Improved metrics</span></span>
* <span data-ttu-id="20e49-232">การปรับขนาดอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="20e49-232">Autoscaling</span></span>
* <span data-ttu-id="20e49-233">ลดค่าใช้จ่ายในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="20e49-233">Reduced management overhead</span></span>

<span data-ttu-id="20e49-234">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI Premium Gen2 โปรดดูที่ [Power BI Premium Generation 2 (ตัวอย่าง)](service-premium-what-is.md#power-bi-premium-generation-2-preview)</span><span class="sxs-lookup"><span data-stu-id="20e49-234">For more information about Power BI Premium Gen2, see [Power BI Premium Generation 2 (preview)](service-premium-what-is.md#power-bi-premium-generation-2-preview).</span></span>
