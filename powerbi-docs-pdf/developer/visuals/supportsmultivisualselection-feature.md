---
title: คุณลักษณะ supportsMultiVisualSelection ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการใช้ฟีเจอร์ supportsMultiVisualSelection ในวิชวล Power BI และข้อกำหนดของคุณลักษณะ เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.date: 04/30/2020
ms.openlocfilehash: 9e6b17a4576f2354a5cbecc0c3a965a5611784ee
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887948"
---
# <a name="use-the-supportsmultivisualselection-feature"></a><span data-ttu-id="3e6b0-104">ใช้ฟีเจอร์ supportsMultiVisualSelection</span><span class="sxs-lookup"><span data-stu-id="3e6b0-104">Use the supportsMultiVisualSelection feature</span></span>

<span data-ttu-id="3e6b0-105">ฟีเจอร์ `supportsMultiVisualSelection`ช่วยให้คุณสามารถใช้การเลือกในวิชวลหลายรายการในรายงานได้</span><span class="sxs-lookup"><span data-stu-id="3e6b0-105">The `supportsMultiVisualSelection` feature enables you to use selection in multiple visuals in a report.</span></span>

## <a name="example"></a><span data-ttu-id="3e6b0-106">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="3e6b0-106">Example</span></span>

<span data-ttu-id="3e6b0-107">ในรายงานที่มีวิชวลมากกว่าหนึ่งรายการ ให้เลือกสองค่าเพื่อให้ค่าเหล่านั้นนำไปใช้กับอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="3e6b0-107">In a report with more than one visual, select two values to have those values apply to other visuals.</span></span> <span data-ttu-id="3e6b0-108">ตัวอย่างเช่น ใน [ตัวอย่างการวิเคราะห์การค้าปลีก](../../create-reports/sample-retail-analysis.md) เลือก **Fashions Direct** ในหนึ่งวิชวล</span><span class="sxs-lookup"><span data-stu-id="3e6b0-108">For instance, in [Retail Analysis sample](../../create-reports/sample-retail-analysis.md), select **Fashions Direct** in one visual.</span></span> <span data-ttu-id="3e6b0-109">เลือก ctrl และเลือก **ม.ค.** ในอีกวิชวลหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3e6b0-109">Select ctrl and select **Jan** in another visual.</span></span> <span data-ttu-id="3e6b0-110">ในรายงานนั้น การเลือกของคุณจะนำไปใช้กับวิชวลอื่นๆ ที่สนับสนุนการใช้ฟีเจอร์นี้</span><span class="sxs-lookup"><span data-stu-id="3e6b0-110">In the report, your selections apply to the other visuals that support this feature usage.</span></span> <span data-ttu-id="3e6b0-111">วิชวลอื่นๆ จะได้รับการกำหนดขอบเขตเป็น **Fashions Direct** และ **ม.ค.**</span><span class="sxs-lookup"><span data-stu-id="3e6b0-111">Other visuals now scope to **Fashions Direct** and **Jan**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e6b0-112">ข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="3e6b0-112">Requirements</span></span>

<span data-ttu-id="3e6b0-113">ฟีเจอร์นี้ต้องการ API v3.2.0 หรือสูงกว่า</span><span class="sxs-lookup"><span data-stu-id="3e6b0-113">This feature requires API v3.2.0 or higher.</span></span>

<span data-ttu-id="3e6b0-114">คุณไม่สามารถนำฟีเจอร์นี้ไปใช้กับวิชวลภาพได้</span><span class="sxs-lookup"><span data-stu-id="3e6b0-114">You can't apply this feature to image visuals.</span></span> <span data-ttu-id="3e6b0-115">คุณไม่สามารถนำฟีเจอร์นี้ไปใช้กับวิชวลขั้นสูงบางรายการได้ เช่น Key Driver Decomposition Tree วิชวลแบบถามตอบ กล่องข้อความ และแผนภูมิหน้าปัด</span><span class="sxs-lookup"><span data-stu-id="3e6b0-115">You can't apply it to some advanced visuals such as key driver, decomposition tree, Q&A visuals, textbox, and gauge charts.</span></span>

## <a name="usage"></a><span data-ttu-id="3e6b0-116">การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3e6b0-116">Usage</span></span>

<span data-ttu-id="3e6b0-117">หากต้องการใช้ฟีเจอร์ `supportsMultiVisualSelection` ให้กรอกรหัสต่อไปนี้ลงในไฟล์ `capabilities.json` ของวิชวลของคุณ</span><span class="sxs-lookup"><span data-stu-id="3e6b0-117">To use the `supportsMultiVisualSelection` feature, add the following code to the `capabilities.json` file of your visual.</span></span>

```json
    {   
            ...
        "supportsMultiVisualSelection": true
            ...
    }
```

## <a name="next-steps"></a><span data-ttu-id="3e6b0-118">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3e6b0-118">Next steps</span></span>

<span data-ttu-id="3e6b0-119">หากต้องการเรียนรู้เกี่ยวกับแนวคิด Power BI ดู [วิชวลใน Power BI](power-bi-visuals-concept.md)</span><span class="sxs-lookup"><span data-stu-id="3e6b0-119">To learn about Power BI concepts, see [Visuals in Power BI](power-bi-visuals-concept.md).</span></span>

<span data-ttu-id="3e6b0-120">หากต้องการทดลองใช้การพัฒนา Power BI โปรดดูที่ [การพัฒนาการ์ดวงกลม Power BI](develop-circle-card.md)</span><span class="sxs-lookup"><span data-stu-id="3e6b0-120">To try out Power BI development, see [Developing a Power BI circle card](develop-circle-card.md).</span></span>
