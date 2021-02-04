---
title: โหมดแก้ไขขั้นสูงของวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายถึงวิธีการตั้งค่าการควบคุม UI ขั้นสูงในวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.date: 06/18/2019
ms.openlocfilehash: 02f02f23d3dfd7ec514e17d1bab17be715e9cd7d
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97889144"
---
# <a name="advanced-edit-mode-in-power-bi-visuals"></a><span data-ttu-id="5d723-104">โหมดการแก้ไขขั้นสูงในวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="5d723-104">Advanced edit mode in Power BI visuals</span></span>

<span data-ttu-id="5d723-105">หากคุณต้องการการควบคุม UI ขั้นสูงในวิชวล Power BI คุณสามารถใช้ประโยชน์จากโหมดแก้ไขขั้นสูงได้</span><span class="sxs-lookup"><span data-stu-id="5d723-105">If you require advanced UI controls in your Power BI visual, you can take advantage of advanced edit mode.</span></span> <span data-ttu-id="5d723-106">เมื่อคุณอยู่ในโหมดแก้ไขรายงาน ให้คุณเลือกปุ่ม **แก้ไข** เพื่อตั้งโหมดแก้ไขเป็น **ขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="5d723-106">When you're in report editing mode, you select an **Edit** button to set the edit mode to **Advanced**.</span></span> <span data-ttu-id="5d723-107">ภาพสามารถใช้ค่าสถานะ `EditMode` เพื่อพิจารณาว่าควรแสดงการควบคุม UI นี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="5d723-107">The visual can use the `EditMode` flag to determine whether it should display this UI control.</span></span>

<span data-ttu-id="5d723-108">ตามค่าเริ่มต้น วิชวลไม่สนับสนุนโหมดการแก้ไขขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="5d723-108">By default, the visual doesn't support advanced edit mode.</span></span> <span data-ttu-id="5d723-109">คุณสามารถระบุสิ่งนี้ได้อย่างชัดเจนในไฟล์ *capabilities.json* ของวิชวลโดยการตั้งค่าคุณสมบัติ `advancedEditModeSupport`</span><span class="sxs-lookup"><span data-stu-id="5d723-109">If a different behavior is required, you can explicitly state this in the visual's *capabilities.json* file by setting the `advancedEditModeSupport` property.</span></span>

<span data-ttu-id="5d723-110">ค่าที่เป็นไปได้คือ:</span><span class="sxs-lookup"><span data-stu-id="5d723-110">The possible values are:</span></span>

- <span data-ttu-id="5d723-111">`0` - NotSupported</span><span class="sxs-lookup"><span data-stu-id="5d723-111">`0` - NotSupported</span></span>

- <span data-ttu-id="5d723-112">`1` - SupportedNoAction</span><span class="sxs-lookup"><span data-stu-id="5d723-112">`1` - SupportedNoAction</span></span>

- <span data-ttu-id="5d723-113">`2` - SupportedInFocus</span><span class="sxs-lookup"><span data-stu-id="5d723-113">`2` - SupportedInFocus</span></span>

## <a name="enter-advanced-edit-mode"></a><span data-ttu-id="5d723-114">ป้อนโหมดการแก้ไขขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="5d723-114">Enter advanced edit mode</span></span>

<span data-ttu-id="5d723-115">ปุ่ม **แก้ไข** จะแสดงขึ้นมาถ้า:</span><span class="sxs-lookup"><span data-stu-id="5d723-115">An **Edit** button is displayed if:</span></span>

* <span data-ttu-id="5d723-116">คุณสมบัติ `advancedEditModeSupport` ถูกตั้งค่าในไฟล์ *capabilities.json* เป็น `SupportedNoAction` หรือ `SupportedInFocus`</span><span class="sxs-lookup"><span data-stu-id="5d723-116">The `advancedEditModeSupport` property is set in the *capabilities.json* file to either `SupportedNoAction` or `SupportedInFocus`.</span></span>

* <span data-ttu-id="5d723-117">แสดงผลวิชวลในโหมดการแก้ไขรายงาน</span><span class="sxs-lookup"><span data-stu-id="5d723-117">The visual is viewed in report editing mode.</span></span>

<span data-ttu-id="5d723-118">หากคุณสมบัติ `advancedEditModeSupport` หายไปจากไฟล์ *capabilities.json* หรือตั้งค่าเป็น `NotSupported` ปุ่ม **แก้ไข** จะไม่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="5d723-118">If `advancedEditModeSupport` property is missing from the *capabilities.json* file or set to `NotSupported`, the **Edit** button is not displayed.</span></span>

![เข้าสู่โหมดการแก้ไข](media/advanced-edit-mode/edit-mode.png)

<span data-ttu-id="5d723-120">เมื่อคุณเลือก **แก้ไข** วิชวลจะทำการเรียกใช้ update() โดยมีการตั้งค่า EditMode เป็น `Advanced`</span><span class="sxs-lookup"><span data-stu-id="5d723-120">When you select **Edit**, the visual gets an update() call with EditMode set to `Advanced`.</span></span> <span data-ttu-id="5d723-121">ขึ้นอยู่กับค่าที่ตั้งไว้ในไฟล์ *capabilities.json* การดำเนินการต่อไปนี้เกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="5d723-121">Depending on the value that's set in the *capabilities.json* file, the following actions occur:</span></span>

* <span data-ttu-id="5d723-122">`SupportedNoAction`: ไม่ต้องการการดำเนินการเพิ่มเติมจากโฮสต์</span><span class="sxs-lookup"><span data-stu-id="5d723-122">`SupportedNoAction`: No further action is required by the host.</span></span>
* <span data-ttu-id="5d723-123">`SupportedInFocus`: โฮสต์จะเปิดหน้าต่างวิชวลใหม่ในโหมดโฟกัส</span><span class="sxs-lookup"><span data-stu-id="5d723-123">`SupportedInFocus`: The host pops out the visual into in focus mode.</span></span>

## <a name="exit-advanced-edit-mode"></a><span data-ttu-id="5d723-124">ออกจากโหมดการแก้ไขขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="5d723-124">Exit advanced edit mode</span></span>

<span data-ttu-id="5d723-125">ปุ่ม **กลับไปยังรายงาน** จะปรากฏขึ้น ถ้า:</span><span class="sxs-lookup"><span data-stu-id="5d723-125">The **Back to report** button is displayed if:</span></span>

* <span data-ttu-id="5d723-126">คุณสมบัติ `advancedEditModeSupport` ถูกตั้งค่าในไฟล์ *capabilities.json* เป็น `SupportedInFocus`</span><span class="sxs-lookup"><span data-stu-id="5d723-126">The `advancedEditModeSupport` property is set in the *capabilities.json* file to `SupportedInFocus`.</span></span>
