---
title: ฉันสามารถใช้ Power BI API ทำอะไรได้บ้างในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: ฉันสามารถทำอะไรกับ Power BI API ได้บ้าง เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: overview
ms.date: 03/25/2019
ms.openlocfilehash: 122028b2ac838763318ab5a0c4e6208138d93188
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887626"
---
# <a name="what-can-developers-do-with-the-power-bi-api"></a><span data-ttu-id="cef71-104">นักพัฒนาสามารถใช้ Power BI API ทำอะไรได้บ้าง</span><span class="sxs-lookup"><span data-stu-id="cef71-104">What can developers do with the Power BI API?</span></span>

<span data-ttu-id="cef71-105">การใช้ Power BI REST API คุณสามารถสร้างแอปที่รวมกับรายงาน แดชบอร์ด และไทล์ของ Power BI</span><span class="sxs-lookup"><span data-stu-id="cef71-105">Using Power BI REST API, you can create apps that integrate with Power BI reports, dashboards, and tiles.</span></span>

<span data-ttu-id="cef71-106">ด้วย Power BI REST API คุณสามารถดำเนินการจัดการกับออบเจ็กต์ Power BI เช่น รายงาน ชุดข้อมูล และพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="cef71-106">With Power BI REST API, it is possible to perform management tasks on Power BI objects like reports, datasets, and workspaces.</span></span>

<span data-ttu-id="cef71-107">ต่อไปนี้เป็นตัวอย่าง สิ่งที่คุณสามารถทำได้ด้วย Power BI API</span><span class="sxs-lookup"><span data-stu-id="cef71-107">Here are some of the things you can do with the Power BI APIs.</span></span>

| <span data-ttu-id="cef71-108">**เมื่อต้องการเรียนรู้เพิ่มเติม**</span><span class="sxs-lookup"><span data-stu-id="cef71-108">**To learn more**</span></span> | <span data-ttu-id="cef71-109">**อ้างอิงข้อมูลนี้**</span><span class="sxs-lookup"><span data-stu-id="cef71-109">**Reference this information**</span></span> |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cef71-110">ฝังรายงาน แดชบอร์ด และไทล์สำหรับผู้ใช้ Power BI และผู้ที่ไม่ใช้ Power BI</span><span class="sxs-lookup"><span data-stu-id="cef71-110">Embed reports, dashboards, and tiles for Power BI users and Non-Power BI users.</span></span> | [<span data-ttu-id="cef71-111">วิธีฝังแดชบอร์ด รายงานและไทล์ Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cef71-111">How to embed your Power BI dashboards, reports, and tiles </span></span>](../embedded/embed-sample-for-customers.md) |
| <span data-ttu-id="cef71-112">ดำเนินการจัดการกับออบเจ็กต์ Power BI</span><span class="sxs-lookup"><span data-stu-id="cef71-112">Perform management tasks on Power BI objects.</span></span> | [<span data-ttu-id="cef71-113">การอ้างอิง Power BI REST API</span><span class="sxs-lookup"><span data-stu-id="cef71-113">Power BI REST API reference</span></span>](/rest/api/power-bi/) |
| <span data-ttu-id="cef71-114">ขยายเวิร์กโฟลว์ทางธุรกิจที่มีอยู่แล้ว โดยการพุชข้อมูลสำคัญลงในแดชบอร์ด Power BI</span><span class="sxs-lookup"><span data-stu-id="cef71-114">Extend an existing business workflow to push key data into a Power BI dashboard.</span></span> | [<span data-ttu-id="cef71-115">การพุชข้อมูลลงในแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="cef71-115">Push data into a dashboard </span></span>](walkthrough-push-data.md) |
| <span data-ttu-id="cef71-116">การรับรองความถูกต้องกับ Power BI</span><span class="sxs-lookup"><span data-stu-id="cef71-116">Authenticate to Power BI.</span></span> | [<span data-ttu-id="cef71-117">การรับรองความถูกต้องกับ Power BI</span><span class="sxs-lookup"><span data-stu-id="cef71-117">Authenticate to Power BI </span></span>](../embedded/get-azuread-access-token.md) |

> [!NOTE]
> <span data-ttu-id="cef71-118">Power BI API ยังคงอ้างอิงถึงพื้นที่ทำงานเป็นกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="cef71-118">The Power BI APIs still refer to workspaces as groups.</span></span> <span data-ttu-id="cef71-119">การอ้างอิงใด ๆ ถึงกลุ่มจะหมายความว่าคุณกำลังทำงานอยู่กับพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="cef71-119">Any references to groups mean that you are working with workspaces.</span></span>

## <a name="api-developer-tools"></a><span data-ttu-id="cef71-120">เครื่องมือสำหรับนักพัฒนา API</span><span class="sxs-lookup"><span data-stu-id="cef71-120">API Developer tools</span></span>

| <span data-ttu-id="cef71-121">เครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="cef71-121">Tool(s)</span></span> | <span data-ttu-id="cef71-122">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="cef71-122">Description</span></span> |
|---------|-------------|
| [<span data-ttu-id="cef71-123">เครื่องมือ Playground</span><span class="sxs-lookup"><span data-stu-id="cef71-123">Playground tool</span></span>](https://microsoft.github.io/PowerBI-JavaScript/demo) | <span data-ttu-id="cef71-124">ประสบการณ์การใช้งานตัวอย่าง Power BI JavaScript API แบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="cef71-124">Experience a full sample of using the Power BI JavaScript APIs.</span></span> <span data-ttu-id="cef71-125">เครื่องมือนี้คือ วิธีที่รวดเร็วเพื่อลองเล่นกับตัวอย่าง Power BI Embedded ชนิดต่าง ๆ กันอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="cef71-125">This tool is also a quick way to play with different types of Power BI Embedded samples.</span></span> |
| [<span data-ttu-id="cef71-126">วิกิสำหรับ Power BI JavaScript</span><span class="sxs-lookup"><span data-stu-id="cef71-126">Power BI JavaScript wiki</span></span>](https://github.com/Microsoft/powerbi-javascript/wiki) | <span data-ttu-id="cef71-127">เพื่อรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI JavaScript API</span><span class="sxs-lookup"><span data-stu-id="cef71-127">To get more Information about the Power BI JavaScript APIs.</span></span> |
| [<span data-ttu-id="cef71-128">Postman</span><span class="sxs-lookup"><span data-stu-id="cef71-128">Postman</span></span>](https://www.getpostman.com/) | <span data-ttu-id="cef71-129">เรียกใช้คำขอ การทดสอบ แก้จุดบกพร่อง ตรวจสอบ เรียกใช้การทดสอบอัตโนมัติและอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="cef71-129">Run requests, test, debug, monitor, run automated tests and more.</span></span> |

## <a name="push-data-into-power-bi"></a><span data-ttu-id="cef71-130">ส่งข้อมูลไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="cef71-130">Push data into Power BI</span></span>

<span data-ttu-id="cef71-131">คุณสามารถใช้ Power BI API เพื่อ[ส่งข้อมูลไปยังชุดข้อมูล ](walkthrough-push-data.md)</span><span class="sxs-lookup"><span data-stu-id="cef71-131">You can use the Power BI API to [push data into a dataset](walkthrough-push-data.md).</span></span> <span data-ttu-id="cef71-132">คุณลักษณะนี้ทำให้คุณสามารถเพิ่มแถวลงในตารางภายในชุดข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="cef71-132">This feature allows you to add a row to a table within a dataset.</span></span> <span data-ttu-id="cef71-133">จากนั้น ข้อมูลใหม่จะสะท้อนผลในไทล์บนแดชบอร์ด และในวิชวลภายในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="cef71-133">The new data is then reflected in tiles on a dashboard and within visuals within your report.</span></span>

![ตัวอย่างการส่งข้อมูล](media/overview-of-power-bi-rest-api/powerbi-push-data.png)

## <a name="github-repositories"></a><span data-ttu-id="cef71-135">ที่เก็บ GitHub</span><span class="sxs-lookup"><span data-stu-id="cef71-135">GitHub repositories</span></span>

* [<span data-ttu-id="cef71-136">ตัวอย่างสำหรับนักพัฒนา Power BI</span><span class="sxs-lookup"><span data-stu-id="cef71-136">Power BI Developer samples</span></span>](https://github.com/Microsoft/PowerBI-Developer-Samples)
* [<span data-ttu-id="cef71-137">.NET SDK</span><span class="sxs-lookup"><span data-stu-id="cef71-137">.NET SDK</span></span>](https://github.com/Microsoft/PowerBI-CSharp)
* [<span data-ttu-id="cef71-138">JavaScript API</span><span class="sxs-lookup"><span data-stu-id="cef71-138">JavaScript API</span></span>](https://github.com/Microsoft/PowerBI-JavaScript)

## <a name="next-steps"></a><span data-ttu-id="cef71-139">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="cef71-139">Next Steps</span></span>

* [<span data-ttu-id="cef71-140">การพุชข้อมูลลงในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cef71-140">Push data into a dataset</span></span>](walkthrough-push-data.md)
* [<span data-ttu-id="cef71-141">การพัฒนาวิชวลการ์ดวงกลมใน Power BI</span><span class="sxs-lookup"><span data-stu-id="cef71-141">Developing a Power BI circle card visual</span></span>](../visuals/develop-circle-card.md)
* [<span data-ttu-id="cef71-142">การอ้างอิง Power BI REST API</span><span class="sxs-lookup"><span data-stu-id="cef71-142">Power BI REST API Reference</span></span>](rest-api-reference.md)
* [<span data-ttu-id="cef71-143">Power BI REST APIs</span><span class="sxs-lookup"><span data-stu-id="cef71-143">Power BI REST APIs</span></span>](/rest/api/power-bi/)

<span data-ttu-id="cef71-144">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="cef71-144">More questions?</span></span> [<span data-ttu-id="cef71-145">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="cef71-145">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)