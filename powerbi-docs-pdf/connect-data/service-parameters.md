---
title: แก้ไขการตั้งค่าพารามิเตอร์ในบริการ Power BI
description: พารามิเตอร์คิวรีถูกสร้างขึ้นใน Power BI Desktop แต่สามารถตรวจทาน และปรับปรุงในบริการ Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 08/04/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 29468ea50625b1d354bd431f77c5e89edf5a889d
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96402098"
---
# <a name="edit-parameter-settings-in-the-power-bi-service"></a><span data-ttu-id="87333-103">แก้ไขการตั้งค่าพารามิเตอร์ในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="87333-103">Edit parameter settings in the Power BI service</span></span>
<span data-ttu-id="87333-104">ผู้สร้างรายงานเพิ่มพารามิเตอร์คิวรีลงในรายงานใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="87333-104">Report creators add query parameters to reports in Power BI Desktop.</span></span> <span data-ttu-id="87333-105">พารามิเตอร์อนุญาตให้ผู้สร้างสามารถรายงานสร้างส่วนต่าง ๆ ของรายงาน ที่ขึ้นอยู่กับพารามิเตอร์อย่างน้อยหนึ่ง *ค่า*</span><span class="sxs-lookup"><span data-stu-id="87333-105">Parameters allow them to make parts of reports depend on one or more parameter *values*.</span></span> <span data-ttu-id="87333-106">ตัวอย่างเช่น ผู้สร้างรายงานอาจสร้างพารามิเตอร์ที่จำกัดข้อมูลไว้ที่ประเทศ/ภูมิภาคหนึ่ง ๆ หรือพารามิเตอร์ที่กำหนดรูปแบบที่ยอมรับได้สำหรับเขตข้อมูลเช่น วัน เวลา และข้อความ</span><span class="sxs-lookup"><span data-stu-id="87333-106">For example, a report creator may create a parameter that restricts the data to a single country/region, or a parameter that defines acceptable formats for fields like dates, time, and text.</span></span>

![แท็บหน้าแรกที่แสดงตัวเลือกจัดการพารามิเตอร์ในเดสก์ท็อป](media/service-parameters/power-bi-manage-parameters.png)

## <a name="review-and-edit-parameters-in-power-bi-service"></a><span data-ttu-id="87333-108">ตรวจสอบ และแก้ไขพารามิเตอร์ในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="87333-108">Review and edit parameters in Power BI service</span></span>

<span data-ttu-id="87333-109">ในฐานะผู้สร้างรายงาน คุณสามารถกำหนดพารามิเตอร์ใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="87333-109">As a report creator, you define parameters in Power BI Desktop.</span></span> <span data-ttu-id="87333-110">เมื่อคุณ [เผยแพร่รายงานนั้นไปยังบริการ Power BI](../create-reports/desktop-upload-desktop-files.md) การตั้งค่าและการเลือกพารามิเตอร์จะเดินทางไปด้วย</span><span class="sxs-lookup"><span data-stu-id="87333-110">When you [publish that report to Power BI service](../create-reports/desktop-upload-desktop-files.md), the parameter settings and selections travel with it.</span></span> <span data-ttu-id="87333-111">คุณสามารถตรวจทานและแก้ไขการตั้งค่าพารามิเตอร์ในบริการของ Power BI แต่ไม่สามารถสร้างได้</span><span class="sxs-lookup"><span data-stu-id="87333-111">You can review and edit parameter settings in the Power BI service, but not create them.</span></span>

1. <span data-ttu-id="87333-112">ในบริการ Power BI เลือกไอคอน cog ![ไอคอน cog](media/service-parameters/power-bi-cog.png)เพื่อเปิด **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="87333-112">In the Power BI service, select the cog icon ![cog icon](media/service-parameters/power-bi-cog.png) to open **Settings**.</span></span>

2. <span data-ttu-id="87333-113">เลือกแท็บสำหรับ **ชุดข้อมูล** และไฮไลต์ชุดข้อมูลในรายการ</span><span class="sxs-lookup"><span data-stu-id="87333-113">Select the tab for **Datasets** and highlight a dataset in the list.</span></span> 
    
    ![หน้าต่างการตั้งค่าพร้อมแท็บชุดข้อมูลจะถูกเลือก](media/service-parameters/power-bi-select-dataset2.png)

3. <span data-ttu-id="87333-115">ขยาย **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="87333-115">Expand **Parameters**.</span></span>  <span data-ttu-id="87333-116">ถ้าชุดข้อมูลที่เลือกไม่มีพารามิเตอร์ คุณจะเห็นข้อความที่มีลิงก์เพื่อเรียนรู้เพิ่มเติมเกี่ยวกับพารามิเตอรคิวรี</span><span class="sxs-lookup"><span data-stu-id="87333-116">If the selected dataset has no parameters, you see a message with a link to Learn more about query parameters.</span></span> <span data-ttu-id="87333-117">แต่ถ้าชุดข้อมูลมีพารามิเตอร์ ให้ขยายหัวข้อ **พารามิเตอร์** จะแสดงพารามิเตอร์เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="87333-117">If the dataset does have parameters, expand the **Parameters** heading to reveal those parameters.</span></span> 

    ![หน้าต่างการตั้งค่าที่มีพารามิเตอร์จะถูกขยาย](media/service-parameters/power-bi-settings.png)

    <span data-ttu-id="87333-119">ตรวจสอบการตั้งค่าพารามิเตอร์ และทำการเปลี่ยนแปลงถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="87333-119">Review the parameter settings and make changes if needed.</span></span> <span data-ttu-id="87333-120">เขตข้อมูลสีเทาไม่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="87333-120">Grayed-out fields aren't editable.</span></span> 


## <a name="next-steps"></a><span data-ttu-id="87333-121">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="87333-121">Next steps</span></span>
<span data-ttu-id="87333-122">วิธีเพิ่มพารามิเตอร์แบบง่ายคือ[ปรับเปลี่ยน URL](../collaborate-share/service-url-filters.md)</span><span class="sxs-lookup"><span data-stu-id="87333-122">An ad-hoc way to add simple parameters is by [modifying the URL](../collaborate-share/service-url-filters.md).</span></span>
