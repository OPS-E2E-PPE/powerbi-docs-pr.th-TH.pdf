---
title: คุณลักษณะ supportsKeyboardFocus ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการใช้คุณลักษณะ supportsKeyboardFocus ในวิชวล Power BI และข้อกำหนด เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.date: 04/30/2020
ms.openlocfilehash: 5ba87db8118076de4bf13abc0280223f9f04f871
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887971"
---
# <a name="use-the-supportskeyboardfocus-feature"></a><span data-ttu-id="181ab-104">ใช้คุณลักษณะ supportsKeyboardFocus</span><span class="sxs-lookup"><span data-stu-id="181ab-104">Use the supportsKeyboardFocus feature</span></span>

<span data-ttu-id="181ab-105">บทความนี้อธิบายวิธีการใช้คุณลักษณะ `supportsKeyboardFocus` ในวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="181ab-105">This article describes how to use the `supportsKeyboardFocus` feature in Power BI visuals.</span></span>
<span data-ttu-id="181ab-106">คุณลักษณะ `supportsKeyboardFocus` อนุญาตให้นำทางจุดข้อมูลของวิชวลโดยใช้แป้นพิมพ์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="181ab-106">The `supportsKeyboardFocus` feature allows navigating the data points of the visual using the keyboard only.</span></span>

<span data-ttu-id="181ab-107">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับการนำทางแป้นพิมพ์สำหรับวิชวล ดู [การนำทางแป้นพิมพ์](../../create-reports/desktop-accessibility-consuming-tools.md#keyboard-navigation)</span><span class="sxs-lookup"><span data-stu-id="181ab-107">To learn more about keyboard navigation for visuals, see [Keyboard Navigation](../../create-reports/desktop-accessibility-consuming-tools.md#keyboard-navigation).</span></span>

## <a name="example"></a><span data-ttu-id="181ab-108">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="181ab-108">Example</span></span>

<span data-ttu-id="181ab-109">เปิดวิชวลที่ใช้คุณลักษณะ `supportsKeyboardFocus`</span><span class="sxs-lookup"><span data-stu-id="181ab-109">Open a visual that uses the `supportsKeyboardFocus` feature.</span></span> <span data-ttu-id="181ab-110">เลือกจุดข้อมูลใดๆ ภายในวิชวลและเลือกแท็บ โฟกัสจะย้ายไปยังจุดข้อมูลถัดไปสำหรับแต่ละครั้งที่คุณเลือกแท็บ เลือก enter เพื่อเลือกจุดข้อมูลที่ไฮไลต์</span><span class="sxs-lookup"><span data-stu-id="181ab-110">Select any data point within the visual and select tab. The focus moves to the next data point for each time you select tab. Select enter to select the highlighted data point.</span></span>

![ตัวอย่าง Supports keyboard focus](./media/supportskeyboardfocus-feature/supports-keyboard-focus-example.png)

## <a name="requirements"></a><span data-ttu-id="181ab-112">ข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="181ab-112">Requirements</span></span>

<span data-ttu-id="181ab-113">คุณลักษณะนี้จำเป็นต้องใช้ API  v2.1.0 หรือสูงกว่า</span><span class="sxs-lookup"><span data-stu-id="181ab-113">This feature requires API v2.1.0 or higher.</span></span>

<span data-ttu-id="181ab-114">คุณลักษณะนี้สามารถนำไปใช้กับวิชวลทั้งหมดยกเว้นวิชวลภาพ</span><span class="sxs-lookup"><span data-stu-id="181ab-114">This feature can be applied to all visuals except image visuals.</span></span>

## <a name="usage"></a><span data-ttu-id="181ab-115">การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="181ab-115">Usage</span></span>

<span data-ttu-id="181ab-116">หากต้องการใช้คุณลักษณะ `supportsKeyboardFocus` ให้เพิ่มรหัสต่อไปนี้ลงในไฟล์ *capabilities.json* ของวิชวลของคุณ</span><span class="sxs-lookup"><span data-stu-id="181ab-116">To use the `supportsKeyboardFocus` feature, add the following code to the *capabilities.json* file of your visual.</span></span>
<span data-ttu-id="181ab-117">ความสามารถนี้อนุญาตให้วิชวลได้รับโฟกัสผ่านการนำทางแป้นพิมพ์</span><span class="sxs-lookup"><span data-stu-id="181ab-117">This capability allows the visual to receive focus through keyboard navigation.</span></span>

```json
    {   
            ...
        "supportsKeyboardFocus": true
            ...
    }

```

## <a name="next-steps"></a><span data-ttu-id="181ab-118">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="181ab-118">Next steps</span></span>

<span data-ttu-id="181ab-119">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะการช่วยสำหรับการเข้าถึงให้ดู [ออกแบบรายงาน Power BI สำหรับความสามารถในการเข้าถึง](../../create-reports/desktop-accessibility-creating-reports.md)</span><span class="sxs-lookup"><span data-stu-id="181ab-119">To learn more about accessibility features, see [Design Power BI reports for accessibility](../../create-reports/desktop-accessibility-creating-reports.md).</span></span>

<span data-ttu-id="181ab-120">หากต้องการลองใช้การพัฒนา Power BI โปรดดู [การพัฒนาวิชวลการ์ดวงกลมใน Power BI](develop-circle-card.md)</span><span class="sxs-lookup"><span data-stu-id="181ab-120">To try out Power BI development, see [Developing a Power BI circle card visual](develop-circle-card.md).</span></span>
