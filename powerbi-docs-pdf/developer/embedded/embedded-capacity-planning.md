---
title: การวางแผนความจุการวิเคราะห์แบบฝังตัวของ Power BI ช่วยให้ได้ข้อมูลเชิงลึก BI แบบฝังตัวที่ดีขึ้น
description: เรียนรู้วิธีการวางแผนความจุของคุณในการวิเคราะห์แบบฝังตัวของ Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 03/03/2020
ms.openlocfilehash: 69eeae495f66a4f41f25d5234f1b995d1e3d4986
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888845"
---
# <a name="capacity-planning-in-power-bi-embedded-analytics"></a><span data-ttu-id="16349-104">ความจุและ SKU ในการวิเคราะห์แบบฝังของ Power BI</span><span class="sxs-lookup"><span data-stu-id="16349-104">Capacity planning in Power BI embedded analytics</span></span>

<span data-ttu-id="16349-105">การคำนวณชนิดของความจุที่จำเป็นสำหรับการปรับใช้การวิเคราะห์แบบฝังของ Power BI อาจซับซ้อนได้</span><span class="sxs-lookup"><span data-stu-id="16349-105">Calculating what type of capacity is needed for a Power BI embedded analytics deployment, can be complicated.</span></span> <span data-ttu-id="16349-106">ทั้งนี้ เนื่องจากการคำนวณนี้จะขึ้นอยู่กับพารามิเตอร์หลายพารามิเตอร์ ซึ่งยากต่อการคาดการณ์บางส่วน</span><span class="sxs-lookup"><span data-stu-id="16349-106">This is because this calculation is based on multiple parameters, some of them hard to predict.</span></span>

<span data-ttu-id="16349-107">บางสิ่งที่ต้องคำนึงถึงเมื่อวางแผนความจุของคุณ:</span><span class="sxs-lookup"><span data-stu-id="16349-107">Some of the things to take into consideration when planning your capacity are:</span></span>

* <span data-ttu-id="16349-108">รูปแบบข้อมูลที่คุณกำลังใช้</span><span class="sxs-lookup"><span data-stu-id="16349-108">The data models you're using</span></span>
* <span data-ttu-id="16349-109">ตัวเลขและความซับซ้อนของคิวรีที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="16349-109">The number and complexity of required queries</span></span>
* <span data-ttu-id="16349-110">การแจกจ่ายรายชั่วโมงของการใช้งานแอปพลิเคชันของคุณ</span><span class="sxs-lookup"><span data-stu-id="16349-110">The hourly distribution of the usage of your application</span></span>
* <span data-ttu-id="16349-111">อัตราการรีเฟรชข้อมูล</span><span class="sxs-lookup"><span data-stu-id="16349-111">Data refresh rates</span></span>
* <span data-ttu-id="16349-112">รูปแบบการใช้งานเพิ่มเติมที่ยากต่อการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="16349-112">Additional usage patterns that are hard to predict.</span></span>

<span data-ttu-id="16349-113">บทความนี้ออกแบบมาเพื่อทำให้การวางแผนกำลังการผลิตสำหรับการวิเคราะห์แบบฝังตัวของ Power BI ง่ายขึ้นโดยการแนะนำ [เครื่องมือประเมินการโหลดความจุ Power BI](https://github.com/microsoft/PowerBI-Tools-For-Capacities/tree/master/LoadTestingPowerShellTool/) ที่สร้างขึ้นสำหรับการทดสอบโหลดอัตโนมัติสำหรับความสามารถในการวิเคราะห์แบบฝังตัวของ Power BI (*A* *EM* หรือ *P* SKUs)</span><span class="sxs-lookup"><span data-stu-id="16349-113">This article is designed to make capacity planning for Power BI embedded analytics easier, by introducing the [Power BI Capacity Load Assessment Tool](https://github.com/microsoft/PowerBI-Tools-For-Capacities/tree/master/LoadTestingPowerShellTool/), created for automating load testing for Power BI embedded analytics capacities (*A*, *EM* or *P* SKUs).</span></span>

## <a name="planning-tool"></a><span data-ttu-id="16349-114">เครื่องมือการวางแผน</span><span class="sxs-lookup"><span data-stu-id="16349-114">Planning tool</span></span>

 <span data-ttu-id="16349-115">[เครื่องมือการประเมินความจุของ Power BI](https://github.com/microsoft/PowerBI-Tools-For-Capacities/tree/master/LoadTestingPowerShellTool/) สามารถช่วยให้คุณเข้าใจว่าผู้ใช้โหลดความจุของคุณได้มากเพียงใด</span><span class="sxs-lookup"><span data-stu-id="16349-115">The [Power BI Capacity Load Assessment Tool](https://github.com/microsoft/PowerBI-Tools-For-Capacities/tree/master/LoadTestingPowerShellTool/) can help you understand how much user load your capacity can handle.</span></span> <span data-ttu-id="16349-116">ใช้ PowerShell เพื่อสร้างการทดสอบการโหลดอัตโนมัติกับความจุของคุณ และช่วยให้คุณสามารถเลือกรายงานที่จะทดสอบและจำนวนผู้ใช้พร้อมกันหลายรายที่จะจำลองได้</span><span class="sxs-lookup"><span data-stu-id="16349-116">It uses PowerShell to create automated load tests against your capacities, and lets you choose which reports to test, and how many concurrent users to simulate.</span></span>

<span data-ttu-id="16349-117">เครื่องมือสร้างการโหลดความจุโดยการแสดงรายงานแต่ละครั้งอย่างต่อเนื่องด้วยค่าตัวกรองใหม่ (เพื่อป้องกันไม่ให้ประสิทธิภาพที่ดีเกินจริงรายงานแคช) จนโทเค็นที่จำเป็นสำหรับการตรวจสอบความถูกต้องของเครื่องมือกับบริการหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="16349-117">The tool generates load on a capacity by continuously rendering each report with new filter values (to prevent unrealistically good performance due to report caching), until the token required for authenticating the tool against the service, expires.</span></span>

### <a name="using-the-planning-tool"></a><span data-ttu-id="16349-118">การใช้เครื่องมือการวางแผน</span><span class="sxs-lookup"><span data-stu-id="16349-118">Using the planning tool</span></span>

<span data-ttu-id="16349-119">เมื่อเรียกใช้เครื่องมือ ให้ระวังการโหลดที่มีอยู่บนความจุของคุณและตรวจสอบให้แน่ใจว่าไม่ได้เรียกใช้การทดสอบการโหลดในช่วงเวลาการใช้งานสูงสุด</span><span class="sxs-lookup"><span data-stu-id="16349-119">When running the tool, be mindful of the existing load on your capacities and make sure not to run load tests during top usage times.</span></span>

<span data-ttu-id="16349-120">ต่อไปนี้คือตัวอย่างของวิธีที่คุณสามารถใช้เครื่องมือการวางแผนได้</span><span class="sxs-lookup"><span data-stu-id="16349-120">Here are some examples of how you can use the planning tool.</span></span>

* <span data-ttu-id="16349-121">ผู้ดูแลความจุสามารถรู้จำนวนผู้ใช้ที่สามารถจัดการได้ในรอบเวลาที่กำหนดได้ดีขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="16349-121">Capacity administrators can get a better understanding of how many users their capacity can handle in a given time frame.</span></span>
* <span data-ttu-id="16349-122">ผู้เขียนรายงานสามารถทำความเข้าใจลักษณะการทำงานของการโหลด โดยใช้การวัดด้วย[ตัววิเคราะห์ประสิทธิภาพ](../../create-reports/desktop-performance-analyzer.md)ของ Power BI desktop</span><span class="sxs-lookup"><span data-stu-id="16349-122">Report authors can understand the user load effect, as measured with Power BI desktop's [Performance Analyzer](../../create-reports/desktop-performance-analyzer.md).</span></span>
* <span data-ttu-id="16349-123">คุณสามารถเห็นการแสดงผลที่เกิดขึ้นตามเวลาจริงบนเบราว์เซอร์ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="16349-123">You can see renders happening in real time on your browser.</span></span>
* <span data-ttu-id="16349-124">ในการใช้ตัวสร้างโพรไฟล์ของ SQL Server คุณสามารถ[เชื่อมต่อกับปลายทาง XMLA](https://powerbi.microsoft.com/blog/power-bi-open-platform-connectivity-with-xmla-endpoints-public-preview/) ของความจุที่วัดเพื่อดูคิวรีที่กำลังดำเนินการได้</span><span class="sxs-lookup"><span data-stu-id="16349-124">Using SQL Server Profiler, you can [connect to the XMLA endpoints](https://powerbi.microsoft.com/blog/power-bi-open-platform-connectivity-with-xmla-endpoints-public-preview/) of the capacities being measured, to see the queries being executed.</span></span>
* <span data-ttu-id="16349-125">ผลการทดสอบการโหลดจะปรากฏในหน้าชุดข้อมูลแอปเมตริกของความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="16349-125">The load test effects are visible in the premium capacity metrics app's Datasets page.</span></span> <span data-ttu-id="16349-126">ผู้ดูแลความจุสามารถใช้เครื่องมือนี้เพื่อสร้างการโหลดและดูว่าการโหลดจะแสดงขึ้นได้อย่างไรได้</span><span class="sxs-lookup"><span data-stu-id="16349-126">Capacity admins can use this tool to generate load, and see how that load shows up.</span></span>

### <a name="reviewing-the-test-results"></a><span data-ttu-id="16349-127">ตรวจทานผลการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="16349-127">Reviewing the test results</span></span>

<span data-ttu-id="16349-128">หากต้องการดูผลกระทบของการทดสอบการโหลดในแอปเมตริกหลังจากการทดสอบ ให้ทำตามคำแนะนำด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="16349-128">To see the effects of the load test in the metrics app after the test runs, follow the instructions below.</span></span> <span data-ttu-id="16349-129">คาดว่าจะมีความล่าช้า 15 นาทีตั้งแต่เวลาที่การทดสอบเริ่มสร้างการโหลด จนกว่าเวลาที่โหลดจะปรากฏในเมตริก</span><span class="sxs-lookup"><span data-stu-id="16349-129">Expect up to a 15 minutes lag from the time the test starts generating load, until the time the load is visible in the metrics.</span></span>

1. <span data-ttu-id="16349-130">ขยายแถบ **ชุดข้อมูล** ของหน้าเริ่มต้น [แอปเมตริก](../../admin/service-admin-premium-monitor-capacity.md)ของคุณ</span><span class="sxs-lookup"><span data-stu-id="16349-130">Expand the **Datasets** tab of your [metrics app](../../admin/service-admin-premium-monitor-capacity.md) landing page.</span></span>
2. <span data-ttu-id="16349-131">เริ่มต้นการรีเฟรชตามความต้องการโดยการคลิก **รีเฟรชทันที**</span><span class="sxs-lookup"><span data-stu-id="16349-131">Initiate an on-demand refresh by clicking **refresh now**.</span></span> <span data-ttu-id="16349-132">ผู้ดูแลระบบควร</span><span class="sxs-lookup"><span data-stu-id="16349-132">Admins should.</span></span>

    ![เมตริกความจุ Power BI Premium](media/embedded-capacity-planning/embedded-capacity-planning.png)

## <a name="power-bi-capacity-tools-github-repository"></a><span data-ttu-id="16349-134">เครื่องมือความจุของ Power BI ที่เก็บ GitHub</span><span class="sxs-lookup"><span data-stu-id="16349-134">Power BI capacity tools GitHub repository</span></span>

<span data-ttu-id="16349-135">เครื่องมือความจุของ [Power BI ที่เก็บ GitHub](https://github.com/microsoft/PowerBI-Tools-For-Capacities) ถูกสร้างขึ้นเพื่อโฮสต์เครื่องมือการวางแผนความจุและเครื่องมือและโปรแกรมอรรถประโยชน์อื่นๆ ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="16349-135">The [Power BI capacity tools GitHub repository](https://github.com/microsoft/PowerBI-Tools-For-Capacities) was created to host the capacity planning tool and other future tools and utilities.</span></span>

<span data-ttu-id="16349-136">ที่เก็บข้อมูลเป็นโอเพ่นซอร์สและผู้ใช้ควรได้รับการสนับสนุน มีส่วนร่วม เพิ่มเครื่องมือเพิ่มเติมที่เกี่ยวข้องกับ Power BI Premium และความสามารถในการฝังและปรับปรุงเครื่องมือเดิมที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="16349-136">The repository is open source and users are encouraged to contribute, add additional tools related to Power BI Premium and Embedded capacities, and improve the existing ones.</span></span>

## <a name="next-steps"></a><span data-ttu-id="16349-137">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="16349-137">Next steps</span></span>

> [!div class="nextstepaction"]
>[<span data-ttu-id="16349-138">ความจุและ SKU ในการวิเคราะห์แบบฝังตัวของ Power BI</span><span class="sxs-lookup"><span data-stu-id="16349-138">Capacity and SKUs in Power BI embedded analytics</span></span>](embedded-capacity.md)

> [!div class="nextstepaction"]
>[<span data-ttu-id="16349-139">แนวทางปฏิบัติที่ดีที่สุดเพื่อประสิทธิภาพการทำงานของ Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="16349-139">Power BI Embedded performance best practices</span></span>](embedded-performance-best-practices.md)