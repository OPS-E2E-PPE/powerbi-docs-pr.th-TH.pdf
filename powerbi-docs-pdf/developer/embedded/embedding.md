---
title: การวิเคราะห์แบบฝังตัวด้วยการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: Power BI มี API เพื่อฝังแดชบอร์ดและรายงานการวิเคราะห์แบบฝังของ Power BI ลงในแอปพลิเคชัน เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: overview
helpviewer_keywords:
- embedded analytics
- embedding
- Power BI embedding
- app owns data
- user owns data
- Power BI APIs
ms.custom: seodec18
ms.date: 05/15/2019
ms.openlocfilehash: c7278dee5957e2b63b6821decec0171ba6b628a0
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887143"
---
# <a name="embedded-analytics-with-power-bi"></a><span data-ttu-id="41b99-104">การวิเคราะห์แบบฝังตัวด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="41b99-104">Embedded analytics with Power BI</span></span>

<span data-ttu-id="41b99-105">บริการ Power BI (SaaS) และบริการ Power BI Embedded ใน Azure (PaaS) มี API สำหรับการฝังสำหรับแดชบอร์ดและรายงาน</span><span class="sxs-lookup"><span data-stu-id="41b99-105">The Power BI service (SaaS) and the Power BI Embedded service in Azure (PaaS) have APIs for embedding your dashboards and reports.</span></span> <span data-ttu-id="41b99-106">เมื่อทำการฝังเนื้อหา คุณจะสามารถเข้าถึงคุณลักษณะล่าสุดของ Power BI เช่น แดชบอร์ด เกตเวย์ และพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="41b99-106">When embedding content, this gives you access to the latest Power BI features such as dashboards, gateways, and workspaces.</span></span>

<span data-ttu-id="41b99-107">คุณสามารถเข้าถึง[เครื่องมือตั้งค่าการฝังตัว](https://aka.ms/embedsetup)เพื่อเริ่มต้นใช้งานได้อย่างรวดเร็ว และดาวน์โหลดแอปพลิเคชันตัวอย่างได้</span><span class="sxs-lookup"><span data-stu-id="41b99-107">You can go through the [Embedding setup tool](https://aka.ms/embedsetup) to quickly get started and download a sample application.</span></span>

<span data-ttu-id="41b99-108">เลือกโซลูชันที่เหมาะกับคุณ:</span><span class="sxs-lookup"><span data-stu-id="41b99-108">Choose the solution that is right for you:</span></span>

* <span data-ttu-id="41b99-109">[การฝังตัวสำหรับองค์กรของคุณ](embedding.md#embedding-for-your-organization) ให้คุณสามารถขยายบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="41b99-109">[Embedding for your organization](embedding.md#embedding-for-your-organization) allows you to extend the Power BI service.</span></span> <span data-ttu-id="41b99-110">เมื่อต้องการทำเช่นนี้ ให้ใช้โซลูชัน *ฝังตัวสำหรับองค์กรของคุณ* ใน [เครื่องมือตั้งค่าการฝังตัว](https://app.powerbi.com/embedsetup)</span><span class="sxs-lookup"><span data-stu-id="41b99-110">To do this, in the [Embedding setup tool](https://app.powerbi.com/embedsetup), implement the *Embed for your organization* solution.</span></span>
* <span data-ttu-id="41b99-111">[การฝังสำหรับลูกค้าของคุณ](embedding.md#embedding-for-your-customers)ช่วยให้คุณสามารถฝังแดชบอร์ดและรายงานสำหรับผู้ใช้ที่ไม่มีบัญชี Power BI</span><span class="sxs-lookup"><span data-stu-id="41b99-111">[Embedding for your customers](embedding.md#embedding-for-your-customers) allows you to embed dashboards and reports to users who don't have a Power BI account.</span></span> <span data-ttu-id="41b99-112">เมื่อต้องการทำเช่นนี้ ให้ใช้โซลูชัน *ฝังตัวสำหรับลูกค้าของคุณ* ใน [เครื่องมือตั้งค่าการฝังตัว](https://app.powerbi.com/embedsetup)</span><span class="sxs-lookup"><span data-stu-id="41b99-112">To do this, in the [Embedding setup tool](https://app.powerbi.com/embedsetup), implement the *Embed for your customers* solution.</span></span>

![ตัวอย่าง PBIE](media/embedding/what-can-you-do-02.png)

## <a name="use-apis"></a><span data-ttu-id="41b99-114">ใช้ API</span><span class="sxs-lookup"><span data-stu-id="41b99-114">Use APIs</span></span>

<span data-ttu-id="41b99-115">มีสองสถานการณ์หลักสำหรับการฝังเนื้อหา Power BI:</span><span class="sxs-lookup"><span data-stu-id="41b99-115">There are two main scenarios for embedding Power BI content:</span></span>
- <span data-ttu-id="41b99-116">การฝังสำหรับผู้ใช้ขององค์กรของคุณ (ที่มีสิทธิการใช้งาน Power BI)</span><span class="sxs-lookup"><span data-stu-id="41b99-116">Embedding for your organization's users (who have Power BI licenses).</span></span> 
 
- <span data-ttu-id="41b99-117">การฝังสำหรับผู้ใช้และลูกค้าของคุณโดยไม่จำเป็นต้องมีสิทธิการใช้งาน Power BI</span><span class="sxs-lookup"><span data-stu-id="41b99-117">Embedding for your users and customers without requiring Power BI licenses.</span></span> 

<span data-ttu-id="41b99-118">[Power BI REST API](/rest/api/power-bi/) ใช้ได้สำหรับทั้งสองสถานการณ์</span><span class="sxs-lookup"><span data-stu-id="41b99-118">The [Power BI REST API](/rest/api/power-bi/) allows for both scenarios.</span></span>

<span data-ttu-id="41b99-119">สำหรับลูกค้าและผู้ใช้ที่มีใบอนุญาต Power BI คุณสามารถฝังแดชบอร์ดและรายงานลงในแอปพลิเคชันแบบกำหนดเองโดยใช้ API เดียวกันเพื่อให้บริการแก่องค์กรหรือลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="41b99-119">For customers and users without Power BI licenses, you can embed dashboards and reports into your custom application, using the same API to either service your organization or your customers.</span></span> <span data-ttu-id="41b99-120">ลูกค้าของคุณจะเห็นข้อมูลที่จัดการโดยแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="41b99-120">Your customers see the application-managed data.</span></span> <span data-ttu-id="41b99-121">นอกจากนี้ ผู้ใช้ Power BI ในองค์กรของคุณจะมีทางเลือกเพิ่มเติมในการดู *ข้อมูลของพวกเขา* ได้โดยตรงใน Power BI หรือบริบทของแอปพลิเคชันแบบฝัง</span><span class="sxs-lookup"><span data-stu-id="41b99-121">Also, your organization's Power BI users have additional options to view *their data* directly in Power BI or in the  embedded application's context.</span></span> <span data-ttu-id="41b99-122">คุณสามารถใช้ประโยชน์สูงสุดจาก JavaScript และ REST API สำหรับความต้องการในการฝังของคุณ</span><span class="sxs-lookup"><span data-stu-id="41b99-122">You can take full advantage of the JavaScript and REST APIs for your embedding needs.</span></span>

<span data-ttu-id="41b99-123">เมื่อต้องการทำความเข้าใจวิธีการทำงานของการฝัง โปรดดู[ตัวอย่างการฝัง JavaScript](https://microsoft.github.io/PowerBI-JavaScript/demo/)</span><span class="sxs-lookup"><span data-stu-id="41b99-123">To understand how embedding works, see the [JavaScript embed sample](https://microsoft.github.io/PowerBI-JavaScript/demo/).</span></span>

## <a name="embedding-for-your-organization"></a><span data-ttu-id="41b99-124">การฝังสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="41b99-124">Embedding for your organization</span></span>

<span data-ttu-id="41b99-125">**การฝังตัวสำหรับองค์กรของคุณ** ให้คุณสามารถขยายบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="41b99-125">**Embedding for your organization** allows you to extend the Power BI service.</span></span> <span data-ttu-id="41b99-126">การฝังประเภทนี้ต้องการให้ผู้ใช้แอปพลิเคชันของคุณลงชื่อเข้าใช้บริการ Power BI เพื่อดูเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="41b99-126">This type of embedding requires your application's users sign into the Power BI service to view the content.</span></span> <span data-ttu-id="41b99-127">เมื่อบุคคลใดบุคคลหนึ่งในองค์กรลงชื่อเข้าใช้ พวกเขาสามารถเข้าถึงแดชบอร์ดและรายงานที่พวกเขาเป็นเจ้าของ หรือที่แชร์กับบุคคลเหล่านั้นในบริการ Power BI เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="41b99-127">Once someone in your organization signs in, they only have access to dashboards and reports that they own or that someone shared with them in the Power BI service.</span></span>

<span data-ttu-id="41b99-128">ตัวอย่างการฝังสำหรับองค์กรรวมถึงแอปพลิเคชันภายใน เช่น [SharePoint Online](https://powerbi.microsoft.com/blog/integrate-power-bi-reports-in-sharepoint-online/)[การทำงานร่วมกับ Microsoft Teams (คุณต้องมีสิทธิผู้ดูแลระบบ)](https://powerbi.microsoft.com/blog/power-bi-teams-up-with-microsoft-teams/) และ [Microsoft Dynamics](/dynamics365/customer-engagement/basics/add-edit-power-bi-visualizations-dashboard)</span><span class="sxs-lookup"><span data-stu-id="41b99-128">Organization embedding examples include internal applications such as [SharePoint Online](https://powerbi.microsoft.com/blog/integrate-power-bi-reports-in-sharepoint-online/), [Microsoft Teams integration (you must have Admin rights)](https://powerbi.microsoft.com/blog/power-bi-teams-up-with-microsoft-teams/), and [Microsoft Dynamics](/dynamics365/customer-engagement/basics/add-edit-power-bi-visualizations-dashboard).</span></span>

<span data-ttu-id="41b99-129">เมื่อต้องฝังสำหรับองค์กรของคุณ ดู[บทช่วยสอน: ฝังเนื้อหา Power BI ลงในแอปพลิเคชันสำหรับองค์กรของคุณ](embed-sample-for-your-organization.md)</span><span class="sxs-lookup"><span data-stu-id="41b99-129">To embed for your organization, see [Tutorial: Embed Power BI content into an application for your organization](embed-sample-for-your-organization.md).</span></span>

<span data-ttu-id="41b99-130">ความสามารถในการทำงานด้วยตนเอง เช่น แก้ไข บันทึก และอื่นๆ จะพร้อมใช้งานผ่าน [JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript) เมื่อมีการฝังสำหรับผู้ใช้ Power BI</span><span class="sxs-lookup"><span data-stu-id="41b99-130">Self-service capabilities, such as edit, save, and more, are available through the [JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript) when embedding for Power BI users.</span></span>

<span data-ttu-id="41b99-131">คุณสามารถใช้[เครื่องมือตั้งค่าการฝัง](https://app.powerbi.com/embedsetup)เพื่อเริ่มต้นและดาวน์โหลดแอปพลิเคชันตัวอย่างที่จะนำคุณไปสู่การรวมรายงานสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="41b99-131">You can go through the [Embedding setup tool](https://app.powerbi.com/embedsetup) to get started and download a sample application that walks you through integrating a report for your organization.</span></span>

## <a name="embedding-for-your-customers"></a><span data-ttu-id="41b99-132">การฝังสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="41b99-132">Embedding for your customers</span></span>

<span data-ttu-id="41b99-133">**การฝังสำหรับลูกค้าของคุณ** ช่วยให้คุณสามารถฝังแดชบอร์ดและรายงานสำหรับผู้ใช้ที่ไม่มีบัญชี Power BI</span><span class="sxs-lookup"><span data-stu-id="41b99-133">**Embedding for your customers** lets you embed dashboards and reports for users who don't have a Power BI account.</span></span> <span data-ttu-id="41b99-134">การฝังประเภทนี้ยังเรียกว่า *Power BI Embedded* ด้วย</span><span class="sxs-lookup"><span data-stu-id="41b99-134">This type of embedding is also known as *Power BI Embedded*.</span></span>

<span data-ttu-id="41b99-135">[Power BI Embedded](azure-pbie-what-is-power-bi-embedded.md) เป็นบริการของ **Microsoft Azure** ที่ช่วยให้นักพัฒนาและผู้จำหน่ายซอฟต์แวร์อิสระ (ISV) ฝังภาพ รายงาน และแดชบอร์ดลงในแอปพลิเคชันได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="41b99-135">[Power BI Embedded](azure-pbie-what-is-power-bi-embedded.md) is a **Microsoft Azure** service that lets independent software vendors (ISVs) and developers quickly embed visuals, reports, and dashboards into an application.</span></span> <span data-ttu-id="41b99-136">การฝังนี้สามารถทำผ่านแบบจำลองการวัดผลรายชั่วโมงตามความจุ</span><span class="sxs-lookup"><span data-stu-id="41b99-136">This embedding is done through a capacity-based, hourly metered model.</span></span>

![การฝังโฟลว์การฝังสำหรับลูกค้าของคุณ](media/embedding/powerbi-embed-flow.png)

<span data-ttu-id="41b99-138">Power BI Embedded มีประโยชน์สำหรับ ISV นักพัฒนาซอฟต์แวร์ และลูกค้า</span><span class="sxs-lookup"><span data-stu-id="41b99-138">Power BI Embedded has benefits for an ISV, their developers, and customers.</span></span> <span data-ttu-id="41b99-139">ตัวอย่างเช่น ISV สามารถเริ่มต้นสร้างภาพฟรีด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="41b99-139">For example, an ISV can start creating visuals for free with Power BI Desktop.</span></span> <span data-ttu-id="41b99-140">ISV สามารถบรรลุเวลาในการทำตลาดได้เร็วขึ้นโดยลดความพยายามในการพัฒนาเชิงวิเคราะห์ทางภาพให้เหลือน้อยที่สุดและโดดเด่นท่ามกลางการแข่งขันด้วยประสบการณ์ด้านข้อมูลที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="41b99-140">By minimizing visual analytic development efforts, ISVs achieve faster time to market and stand out from competitors with differentiated data experiences.</span></span> <span data-ttu-id="41b99-141">ISV ยังสามารถเลือกการชำระค่าบริการระดับพรีเมียมสำหรับค่าเพิ่มเติมที่สร้างโดยระบบการวิเคราะห์ที่ฝังมาด้วย</span><span class="sxs-lookup"><span data-stu-id="41b99-141">ISVs can also opt to charge a premium for the additional value they create with embedded analytics.</span></span>

<span data-ttu-id="41b99-142">ด้วย Power BI Embedded ลูกค้าของคุณไม่จำเป็นต้องทราบอะไรเลยเกี่ยวกับ Power BI</span><span class="sxs-lookup"><span data-stu-id="41b99-142">With Power BI Embedded, your customers don't need to know anything about Power BI.</span></span> <span data-ttu-id="41b99-143">คุณสามารถใช้สองวิธีการที่แตกต่างกันเพื่อสร้างแอปพลิเคชันแบบฝังตัว</span><span class="sxs-lookup"><span data-stu-id="41b99-143">You can use two different methods to create an embedded application:</span></span>
- <span data-ttu-id="41b99-144">บัญชี Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="41b99-144">Power BI Pro account</span></span> 
- <span data-ttu-id="41b99-145">โครงร่างสำคัญของบริการ</span><span class="sxs-lookup"><span data-stu-id="41b99-145">Service principal</span></span> 

<span data-ttu-id="41b99-146">บัญชี Power BI Pro ทำหน้าที่เป็นบัญชีหลักสำหรับแอปพลิเคชัน (ให้คิดว่านี่เป็นบัญชีพร็อกซี)</span><span class="sxs-lookup"><span data-stu-id="41b99-146">The Power BI Pro account acts as your application's master account (think of it as a proxy account).</span></span> <span data-ttu-id="41b99-147">บัญชีนี้ช่วยให้คุณสามารถสร้างโทเค็นแบบฝังที่มีการเข้าถึงแดชบอร์ดและรายงาน Power BI ของแอปพลิเคชั่น</span><span class="sxs-lookup"><span data-stu-id="41b99-147">This account allows you to generate embed tokens that provide access to your application's Power BI dashboards and reports.</span></span>

<span data-ttu-id="41b99-148">[บริการหลัก](embed-service-principal.md)สามารถฝังเนื้อหา Power BI ลงในแอปพลิเคชันโดยใช้โทเค็น **เฉพาะแอป** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="41b99-148">[Service principal](embed-service-principal.md) can embed Power BI content into an application using an **app-only** token.</span></span> <span data-ttu-id="41b99-149">นอกจากนี้ยังช่วยให้คุณสามารถสร้างโทเค็นแบบฝังที่มีการเข้าถึงแดชบอร์ดและรายงาน Power BI ของแอปพลิเคชั่น</span><span class="sxs-lookup"><span data-stu-id="41b99-149">It also allows you to generate embed tokens that provide access to your application's Power BI dashboards and reports.</span></span>

<span data-ttu-id="41b99-150">นักพัฒนาที่ใช้ Power BI Embedded สามารถเน้นการสร้างฟังก์ชันการทำงานหลักของแอปพลิเคชันแทนที่จะใช้เวลาพัฒนาภาพและการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="41b99-150">Developers using Power BI Embedded can spend time focused on building their application's core functionality rather than spending time developing visuals and analytics.</span></span> <span data-ttu-id="41b99-151">ซึ่งสามารถตอบสนองความต้องการด้านรายงานและแดชบอร์ดของลูกค้าได้อย่างรวดเร็วและสามารถฝังได้ง่ายด้วย API และ SDK ที่ได้รับการจัดทำขึ้นเป็นเอกสารอย่างครบถ้วน</span><span class="sxs-lookup"><span data-stu-id="41b99-151">They can rapidly meet customer report and dashboard demands and embed easily with fully documented APIs and SDKs.</span></span> <span data-ttu-id="41b99-152">การเปิดใช้งานการสำรวจข้อมูลที่ค้นหาได้ง่ายในแอปทำให้ ISV ช่วยให้ลูกค้าทำการตัดสินใจได้อย่างรวดเร็วเนื่องจากมีข้อมูลจากอุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="41b99-152">By enabling easy-to-navigate data exploration in apps, ISVs allow customers to make quick, data-driven decisions in context from any device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41b99-153">ในขณะที่การฝังจำเป็นต้องใช้บริการของ Power BI ลูกค้าของคุณไม่จำเป็นต้องมีบัญชี Power BI เพื่อดูเนื้อหาแบบฝังตัวของแอปพลิเคชั่น</span><span class="sxs-lookup"><span data-stu-id="41b99-153">While embedding requires the Power BI service, your customers do not need to have a Power BI account to view your application's embedded content.</span></span>

<span data-ttu-id="41b99-154">เมื่อคุณพร้อมที่จะย้ายไปยังการผลิต พื้นที่ทำงานของคุณจะต้องถูกกำหนดให้เป็นความจุ</span><span class="sxs-lookup"><span data-stu-id="41b99-154">When you're ready to move to production, your workspace must be assigned to a capacity.</span></span> <span data-ttu-id="41b99-155">[สร้างความจุ Power BI Embedded](azure-pbie-create-capacity.md) ใน Microsoft Azure เพื่อใช้กับแอปพลิเคชันของคุณ</span><span class="sxs-lookup"><span data-stu-id="41b99-155">[Create a Power BI Embedded capacity](azure-pbie-create-capacity.md) in Microsoft Azure, to use with your applications.</span></span>

<span data-ttu-id="41b99-156">สำหรับรายละเอียดการฝัง ดู[วิธีการฝังเนื้อหา Power BI](embed-sample-for-customers.md)</span><span class="sxs-lookup"><span data-stu-id="41b99-156">For embedding details, see [How to embed Power BI content](embed-sample-for-customers.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="41b99-157">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="41b99-157">Next steps</span></span>

<span data-ttu-id="41b99-158">ตอนนี้คุณสามารถลองฝังเนื้อหา Power BI ไปยังแอปพลิเคชัน หรือลองฝังเนื้อหา Power BI สำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="41b99-158">You can now try to embed Power BI content into an application, or try to embed Power BI content for your customers.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="41b99-159">ฝังตัวสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="41b99-159">Embed for your organization</span></span>](embed-sample-for-your-organization.md)

> [!div class="nextstepaction"]
> [<span data-ttu-id="41b99-160">Power BI Embedded คืออะไร</span><span class="sxs-lookup"><span data-stu-id="41b99-160">What is Power BI Embedded?</span></span>](azure-pbie-what-is-power-bi-embedded.md)

> [!div class="nextstepaction"]
>[<span data-ttu-id="41b99-161">ฝังสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="41b99-161">Embed for your customers</span></span>](embed-sample-for-customers.md)

<span data-ttu-id="41b99-162">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="41b99-162">More questions?</span></span> [<span data-ttu-id="41b99-163">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="41b99-163">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)