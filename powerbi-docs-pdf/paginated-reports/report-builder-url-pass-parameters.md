---
title: ส่งผ่านพารามิเตอร์รายงานใน URL สำหรับรายงานที่มีการแบ่งหน้า - ตัวสร้างรายงาน Power BI
description: หัวข้อนี้อธิบายวิธีการส่งผ่านพารามิเตอร์รายงานไปยังรายงานโดยรวมใน URL รายงานที่มีการแบ่งหน้า
author: maggiesMSFT
ms.author: maggies
ms.service: powerbi
ms.subservice: report-builder
ms.topic: how-to
ms.reviewer: cfinlan
ms.custom: ''
ms.date: 05/01/2020
ms.openlocfilehash: ac3cd10ec4c356da92aca6983292ff57b16f58b3
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415599"
---
# <a name="pass-a-report-parameter-in-a-url-for-a-paginated-report-in-power-bi"></a><span data-ttu-id="93af1-103">ส่งผ่านพารามิเตอร์รายงานใน URL สำหรับรายงานที่มีการแบ่งหน้าใน Power BI</span><span class="sxs-lookup"><span data-stu-id="93af1-103">Pass a report parameter in a URL for a paginated report in Power BI</span></span> 

<span data-ttu-id="93af1-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span><span class="sxs-lookup"><span data-stu-id="93af1-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span></span> 

<span data-ttu-id="93af1-105">คุณสามารถส่งผ่านพารามิเตอร์รายงานไปยังรายงานโดยรวมไว้ใน URL รายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="93af1-105">You can pass report parameters to a report by including them in a paginated report URL.</span></span> <span data-ttu-id="93af1-106">พารามิเตอร์คิวรีทั้งหมดสามารถมีพารามิเตอร์รายงานที่สอดคล้องกันได้</span><span class="sxs-lookup"><span data-stu-id="93af1-106">All query parameters can have corresponding report parameters.</span></span> <span data-ttu-id="93af1-107">ดังนั้นคุณส่งผ่านพารามิเตอร์คิวรีไปยังรายงานโดยผ่านพารามิเตอร์รายงานที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="93af1-107">Therefore, you pass a query parameter to a report by passing the corresponding report parameter.</span></span> <span data-ttu-id="93af1-108">คุณจำเป็นต้องใช้คำนำหน้าชื่อพารามิเตอร์ด้วย `rp:` สำหรับ Power BI เพื่อจดจำใน URL</span><span class="sxs-lookup"><span data-stu-id="93af1-108">You need to prefix the parameter name with `rp:` for Power BI to recognize it in the URL.</span></span> 

<span data-ttu-id="93af1-109">พารามิเตอร์รายงานต้องตรงตามตัวพิมพ์ใหญ่-เล็ก และใช้อักขระพิเศษเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="93af1-109">Report parameters are case-sensitive and use these special characters:</span></span> 

- <span data-ttu-id="93af1-110">ช่องว่างในส่วนพารามิเตอร์ของ URL จะถูกแทนที่ด้วยเครื่องหมายบวก (+)</span><span class="sxs-lookup"><span data-stu-id="93af1-110">A space in the parameter portion of the URL is replaced with a plus sign (+).</span></span>  <span data-ttu-id="93af1-111">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="93af1-111">For example:</span></span> 

    ```rp:Holiday=Christmas+Day```

- <span data-ttu-id="93af1-112">เครื่องหมายอัฒภาคในส่วนใด ๆ ของสตริงที่จะถูกแทนที่ด้วยอักขระ `%3A`</span><span class="sxs-lookup"><span data-stu-id="93af1-112">A semicolon in any portion of the string is replaced with the characters `%3A`.</span></span>

<span data-ttu-id="93af1-113">เบราว์เซอร์ควรดำเนินการเข้ารหัส URL ที่เหมาะสมโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="93af1-113">Browsers should automatically perform the proper URL encoding.</span></span> <span data-ttu-id="93af1-114">คุณไม่จำเป็นต้องเข้ารหัสอักขระใด ๆ ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="93af1-114">You don't have to encode any of the characters manually.</span></span> 

<span data-ttu-id="93af1-115">เมื่อต้องการตั้งค่าพารามิเตอร์รายงานภายใน URL ให้ใช้ไวยากรณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="93af1-115">To set a report parameter within a URL, use the following syntax:</span></span> 

```
rp:parameter=value
```

<span data-ttu-id="93af1-116">ตัวอย่างเช่น เมื่อต้องการระบุสองพารามิเตอร์ "Salesperson" และ "State" ที่กำหนดไว้ในรายงานในพื้นที่ทำงานของฉัน คุณจะต้องใช้ URL ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="93af1-116">For example, to specify two parameters, "Salesperson" and "State", defined in a report in your My Workspace,you'd use the following URL:</span></span> 

```
https://app.powerbi.com/groups/me/rdlreports/xxxxxxx-abc7-40f0-b456-febzf9cdda4d?rp:Salesperson=Tie+Bear&rp:State=Utah 
```

<span data-ttu-id="93af1-117">เมื่อต้องการระบุพารามิเตอร์สองรายการเดียวกันที่กำหนดในรายงานในแอป คุณจะต้องใช้ URL ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="93af1-117">To specify the same two parameters defined in a report in an app, you'd use the following URL:</span></span> 

```
https://app.powerbi.com/groups/me/apps/xxxxxxx-c4c4-4217-afd9-3920a0d1e2b0/rdlreports/b1d5e659-639e-41d0-b733-05d2bca9853c?rp:Salesperson=Tiggee&rp:State=Utah 
```

<span data-ttu-id="93af1-118">เมื่อต้องการส่งค่า null สำหรับพารามิเตอร์ ให้ใช้ไวยากรณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="93af1-118">To pass a null value for a parameter, use the following syntax:</span></span> 

```
parameter:isnull=true
```

<span data-ttu-id="93af1-119">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="93af1-119">For example:</span></span>

```
rp:SalesOrderNumber:isnull=true
```

<span data-ttu-id="93af1-120">เมื่อต้องการส่งค่า Boolean ให้ใช้ 0 สำหรับ False และ 1 สำหรับ True</span><span class="sxs-lookup"><span data-stu-id="93af1-120">To pass a Boolean value, use 0 for false and 1 for true.</span></span> <span data-ttu-id="93af1-121">เมื่อต้องการส่งค่า Float ให้ใส่ตัวคั่นทศนิยมของตำแหน่งที่ตั้งเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="93af1-121">To pass a Float value, include the decimal separator of the server locale.</span></span>

> [!NOTE]
> <span data-ttu-id="93af1-122">ถ้ารายงานของคุณมีพารามิเตอร์รายงานที่มีค่าเริ่มต้นและค่าของคุณสมบัติ **พร้อมท์** เป็น **false** (นั่นคือ **ผู้ใช้พร้อมท์** ไม่ได้เลือกคุณสมบัติในโปรแกรมจัดการรายงาน) จากนั้นคุณจะไม่สามารถส่งค่าสำหรับพารามิเตอร์รายงานนั้นได้ภายใน URL</span><span class="sxs-lookup"><span data-stu-id="93af1-122">If your report contains a report parameter that has a default value, and the value of the **Prompt** property is **false** (that is, the **Prompt User** property isn't selected in Report Manager), then you can't pass a value for that report parameter within a URL.</span></span> <span data-ttu-id="93af1-123">ซึ่งช่วยให้ผู้ดูแลระบบมีตัวเลือกในการป้องกันผู้ใช้ปลายมิให้เพิ่มหรือแก้ไขค่าของพารามิเตอร์รายงานบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="93af1-123">This provides administrators the option of preventing end users from adding or modifying the values of certain report parameters.</span></span>
> 
> <span data-ttu-id="93af1-124">Power BI ไม่สนับสนุนสตริงการคิวรีมากกว่า 2,000 ตัวอักขระ</span><span class="sxs-lookup"><span data-stu-id="93af1-124">Power BI does not support a query string of more than 2,000 characters.</span></span>  <span data-ttu-id="93af1-125">ค่านี้สามารถเกินได้ถ้าคุณกำลังใช้พารามิเตอร์ url เพื่อดูรายงานที่มีการแบ่งหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="93af1-125">This value can be exceeded if you are using url parameters to view your paginated report.</span></span>  <span data-ttu-id="93af1-126">ซึ่งเป็นจริงโดยเฉพาะอย่างยิ่งถ้าคุณกำลังใช้พารามิเตอร์แบบหลายค่า</span><span class="sxs-lookup"><span data-stu-id="93af1-126">It is especially true if you are using multi-value parameters.</span></span>

## <a name="additional-examples"></a><span data-ttu-id="93af1-127">ตัวอย่างเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="93af1-127">Additional examples</span></span> 

<span data-ttu-id="93af1-128">ตัวอย่าง URL ต่อไปนี้ประกอบด้วยพารามิเตอร์แบบหลายค่า "Salesperson”</span><span class="sxs-lookup"><span data-stu-id="93af1-128">The following URL example includes a multi-value parameter "Salesperson”.</span></span> <span data-ttu-id="93af1-129">รูปแบบสำหรับพารามิเตอร์หลายค่าคือการทำซ้ำชื่อพารามิเตอร์สำหรับแต่ละค่า</span><span class="sxs-lookup"><span data-stu-id="93af1-129">The format for a multi-value parameter is to repeat the parameter name for each value.</span></span> 

```
https://app.powerbi.com/groups/me/rdlreports/xxxxxxx-abc7-40f0-b456-febzf9cdda4d?rp:Salesperson=Tie+Bear&rp:Salesperson=Mickey 
```

<span data-ttu-id="93af1-130">ตัวอย่าง URL ต่อไปนี้จะส่งพารามิเตอร์เดียวของ SellStartDate  ที่มีค่า "7/1/2005" สำหรับเซิร์ฟเวอร์รายงานโหมดเนทิฟ</span><span class="sxs-lookup"><span data-stu-id="93af1-130">The following URL example passes a single parameter of SellStartDate with a value of "7/1/2005", for a native mode report server.</span></span>

```
https://app.powerbi.com/groups/me/rdlreports/xxxxxxx-abc7-40f0-b456-febzf9cdda4d?rp:SellStartDate=7/1/2005
```

## <a name="next-steps"></a><span data-ttu-id="93af1-131">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="93af1-131">Next steps</span></span>

- [<span data-ttu-id="93af1-132">พารามิเตอร์ URL ในรายงานที่มีการแบ่งหน้าใน Power BI</span><span class="sxs-lookup"><span data-stu-id="93af1-132">URL parameters in paginated reports in Power BI</span></span>](report-builder-url-parameters.md)
- [<span data-ttu-id="93af1-133">รายงานแบบแบ่งหน้าใน Power BI Premium คืออะไร</span><span class="sxs-lookup"><span data-stu-id="93af1-133">What are paginated reports in Power BI Premium?</span></span>](paginated-reports-report-builder-power-bi.md)
