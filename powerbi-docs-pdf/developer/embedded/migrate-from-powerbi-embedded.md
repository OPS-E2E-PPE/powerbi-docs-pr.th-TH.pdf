---
title: วิธีการโยกย้ายเนื้อหาคอลเลกชันพื้นที่ทำงาน Power BI ไปยังโซลูชันการวิเคราะห์แบบฝังตัวของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: เรียนรู้วิธีการโยกย้ายเนื้อหาจาก Power BI Workspace Collection ไปยัง Power BI Embedded และใช้ประโยชน์การพัฒนาเพื่อการฝังในแอป เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: how-to
ms.date: 06/30/2018
ms.openlocfilehash: a2e73ced427daa8aebf6b5c9836aa060d3591e3e
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97886384"
---
# <a name="how-to-migrate-power-bi-workspace-collection-content-to-power-bi-embedded"></a><span data-ttu-id="59023-104">วิธีการย้ายเนื้อหาจาก Power BI Workspace Collection ไปยัง Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="59023-104">How to migrate Power BI Workspace Collection content to Power BI Embedded</span></span>

<span data-ttu-id="59023-105">เรียนรู้วิธีการโยกย้ายจาก Power BI Workspace Collection ไปยัง Power BI Embedded และใช้ประโยชน์การพัฒนาเพื่อการฝังในแอป</span><span class="sxs-lookup"><span data-stu-id="59023-105">Learn how to migrate from Power BI Workspace Collection to Power BI Embedded and leverage advances for embedding in apps.</span></span>

<span data-ttu-id="59023-106">เมื่อไม่นานมานี้ Microsoft [ประกาศเปิดตัว Power BI Embedded](https://powerbi.microsoft.com/blog/power-bi-embedded-capacity-based-skus-coming-to-azure/) ซึ่งเป็นแบบจำลองิ์ความสามารถใหม่่ที่ให้สิทธเพื่อเพิ่มวิธีที่ผู้ใช้เข้าถึง แชร์ และแจกจ่ายเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="59023-106">Microsoft recently [announced Power BI Embedded](https://powerbi.microsoft.com/blog/power-bi-embedded-capacity-based-skus-coming-to-azure/), a new capacity-based licensing model that increases flexibility for how users access, share and distribute content.</span></span> <span data-ttu-id="59023-107">นอกจากนียังทำให้ปรับขนาดและทำงานเพิ่มเติมได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="59023-107">The offering also delivers additional scalability and performance.</span></span>

<span data-ttu-id="59023-108">ซึ่งหมายความว่า ด้วย Power BI Embedded คุณจะมี API surface ซึ่งเป็นชุดความสามารถและการเข้าถึงคุณสมบัติล่าสุดของ Power BI – เช่น แดชบอร์ด เกตเวย์ และพื้นที่ทำงาน – เมื่อทำการฝังเนื้อหาของคุณ</span><span class="sxs-lookup"><span data-stu-id="59023-108">With Power BI Embedded, you will have one API surface, a consistent set of capabilities and access to the latest Power BI features – such as dashboards, gateways and workspaces – when embedding your content.</span></span> <span data-ttu-id="59023-109">ดำเนินการในขั้นตอนต่อไป แล้วคุณจะสามารถเริ่มต้นใช้งาน Power BI Desktop และย้ายไปใช้ Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="59023-109">Moving forward you'll be able to start with Power BI Desktop and move to deployment with Power BI Embedded.</span></span>

<span data-ttu-id="59023-110">Power BI Workspace Collection รุ่นปัจจุบันจะยังคงมีให้ใช้งานในช่วงเวลาที่จำกัด</span><span class="sxs-lookup"><span data-stu-id="59023-110">The current Power BI Workspace Collection will continue to be available for a limited time.</span></span> <span data-ttu-id="59023-111">ลูกค้าภายใต้ข้อตกลงขององค์กรจะสามารถใช้งานได้จนกว่าข้อตกลงที่มีอยู่จะหมดอายุ ลูกค้าที่ได้ซื้อ Power BI Workspace Collection ทางช่องทาง Direct หรือ CSP จะยังคงใช้งานได้อีกหนึ่งปีนับจากเปิดตัว Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="59023-111">Customers under an Enterprise Agreement will have access through the expiration of their existing agreements; customers that acquired Power BI Workspace Collection through Direct or CSP channels will maintain access for one year from the General Availability release of Power BI Embedded.</span></span>  <span data-ttu-id="59023-112">บทความนี้จะให้คำแนะนำบางอย่างสำหรับการโยกย้ายเนื้อหาจาก Power BI Workspace Collection ไปยัง Power BI Embedded และการเปลี่ยนแปลงใหม่ๆที่คาดได้ในแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="59023-112">This article will provide some guidance for migrating from Power BI Workspace Collection to the new Power BI Embedded experience and what to expect for changes in your application.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59023-113">ในขณะที่การโยกย้ายเนื้อหาจะขึ้นอยู่กับ Power BI Embedded ผู้ใช้แอปของคุณจะไม่จำเป็นต้องใช้ Power BI เมื่อใช้ **โทเค็นการฝัง**</span><span class="sxs-lookup"><span data-stu-id="59023-113">While the migration will take a dependency on Power BI Embedded, there is not a dependency on Power BI for the users of your application when using an **embed token**.</span></span> <span data-ttu-id="59023-114">พวกเขาจึงไม่ต้องลงทะเบียนใช้งาน Power BI เพื่อดูเนื้อหาที่ฝังในแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="59023-114">They do not need to sign up for Power BI to view the embedded content in your application.</span></span> <span data-ttu-id="59023-115">คุณสามารถใช้วิธีฝังนี้กับผู้ใช้ที่ไม่ใช้ Power BI</span><span class="sxs-lookup"><span data-stu-id="59023-115">You can use this embedding approach to Embedded non-Power BI users.</span></span>

![โฟลว์แบบฝัง](media/migrate-from-powerbi-embedded/powerbi-embed-flow.png)

<span data-ttu-id="59023-117">ก่อนที่คุณจะเริ่มต้นย้ายไปยัง Power BI Embedded ใหม่ คุณสามารถไปยังคำแนะนำที่ช่วยให้คุณตั้งค่าสภาพแวดล้อม Power BI Embedded ใหม่ของคุณ โดยใช้[เครื่องมือตั้งค่าการฝังตัว](https://aka.ms/embedsetup)ได้</span><span class="sxs-lookup"><span data-stu-id="59023-117">Before you get started migrating to the new Power BI Embedded, you can quickly go through a walkthrough that helps you set up your new Power BI Embedded environment using the [Embedding setup tool](https://aka.ms/embedsetup).</span></span>

<span data-ttu-id="59023-118">เลือกโซลูชันที่เหมาะกับคุณ:</span><span class="sxs-lookup"><span data-stu-id="59023-118">Choose the solution that is right for you:</span></span>
* <span data-ttu-id="59023-119">**การฝังตัวสำหรับลูกค้าของคุณ** - เมื่อคุณกำลังสนใจโซลูชันที่ *แอปเป็นเจ้าของข้อมูล*</span><span class="sxs-lookup"><span data-stu-id="59023-119">**Embed for your customers** - when you are interested in an *app owns data* solution.</span></span> <span data-ttu-id="59023-120">[การฝังตัวสำหรับลูกค้าของคุณ](embedding.md#embedding-for-your-customers) จะมอบความสามารถในการฝังแดชบอร์ดและรายงานสำหรับผู้ใช้ที่ไม่มีบัญชี Power BI</span><span class="sxs-lookup"><span data-stu-id="59023-120">[Embedding for your customers](embedding.md#embedding-for-your-customers) provides the ability to embed dashboards and reports to users who don't have an account for Power BI.</span></span> 

* <span data-ttu-id="59023-121">**การฝังตัวสำหรับองค์กรของคุณ** - เมื่อคุณกำลังสนใจโซลูชันที่ *ผู้ใช้เป็นเจ้าของข้อมูล*</span><span class="sxs-lookup"><span data-stu-id="59023-121">**Embed for your organization** - when you are interested in a *user owns data* solution.</span></span> <span data-ttu-id="59023-122">[การฝังตัวสำหรับองค์กรของคุณ](embedding.md#embedding-for-your-organization) ให้คุณสามารถขยายบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="59023-122">[Embedding for your organization](embedding.md#embedding-for-your-organization) allows you to extend the Power BI service.</span></span>

## <a name="prepare-for-the-migration"></a><span data-ttu-id="59023-123">เตรียมพร้อมสำหรับการโยกย้ายเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="59023-123">Prepare for the migration</span></span>

<span data-ttu-id="59023-124">มีบางสิ่งที่คุณจำเป็นต้องทำเพื่อเตรียมพร้อมสำหรับการโยกย้ายเนื้อหาจาก Power BI Workspace Collection ไปยัง Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="59023-124">There are a few things you need to do to prepare for migrating from Power BI Workspace Collection to Power BI Embedded.</span></span> <span data-ttu-id="59023-125">คุณจะต้องมีผู้เช่าที่พร้อมใช้งาน พร้อมกับผู้ใช้ที่มีสิทธิ์การใช้งาน Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="59023-125">You will need a tenant available, along with a user that has a Power BI Pro license.</span></span>

1. <span data-ttu-id="59023-126">ตรวจสอบให้แน่ใจว่า คุณสามารถเข้าถึงผู้เช่าของ Azure Active Directory (Azure AD) ได้</span><span class="sxs-lookup"><span data-stu-id="59023-126">Make sure you have access to an Azure Active Directory (Azure AD) tenant.</span></span>

    <span data-ttu-id="59023-127">คุณจำเป็นต้องระบุการตั้งค่าผู้เช่าเมื่อต้องใช้</span><span class="sxs-lookup"><span data-stu-id="59023-127">You need to determine which tenant setup to use.</span></span>

   * <span data-ttu-id="59023-128">ใช้ผู้เช่าของ Power BI ขององค์กรของคุณที่มีอยู่ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="59023-128">Use your existing corporate Power BI tenant?</span></span>
   * <span data-ttu-id="59023-129">ใช้ผู้เช่าที่แยกต่างหากสำหรับแอปพลิเคชันของคุณ?</span><span class="sxs-lookup"><span data-stu-id="59023-129">Use a separate tenant for your application?</span></span>
   * <span data-ttu-id="59023-130">ใช้ผู้เช่าที่แยกต่างหากสำหรับลูกค้าแต่ละรายการได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="59023-130">Use a separate tenant for each customer?</span></span>

     <span data-ttu-id="59023-131">ถ้าคุณตัดสินใจที่จะสร้างผู้เช่าใหม่สำหรับแอปของคุณหรือสำหรับลูกค้าแต่ละราย ดู[สร้างผู้เช่า Azure Active Directory](create-an-azure-active-directory-tenant.md) หรือ[วิธีการได้รับผู้เช่า Azure Active Directory](/azure/active-directory/develop/active-directory-howto-tenant)</span><span class="sxs-lookup"><span data-stu-id="59023-131">If you decide to create a new tenant for your application, or each customer, see [Create an Azure Active Directory tenant](create-an-azure-active-directory-tenant.md) or [How to get an Azure Active Directory tenant](/azure/active-directory/develop/active-directory-howto-tenant).</span></span>
2. <span data-ttu-id="59023-132">สร้างผู้ใช้ภายในผู้เช่าใหม่นี้ซึ่งจะทำหน้าที่เป็นบัญชีแอป "หลัก" ของคุณ</span><span class="sxs-lookup"><span data-stu-id="59023-132">Create a user within this new tenant that will act as your application "master" account.</span></span> <span data-ttu-id="59023-133">บัญชีผู้ใช้นี้จำเป็นต้องลงทะเบียนใน Power BI และจำเป็นต้องมีสิทธิ์การใช้งานใน Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="59023-133">That account needs to sign up for Power BI and needs to have a Power BI Pro license assigned to it.</span></span>

## <a name="accounts-within-azure-ad"></a><span data-ttu-id="59023-134">บัญชีผู้ใช้ภายใน Azure AD</span><span class="sxs-lookup"><span data-stu-id="59023-134">Accounts within Azure AD</span></span>

<span data-ttu-id="59023-135">บัญชีผู้ใช้ต่อไปนี้จะต้องอยูในผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="59023-135">The following accounts will need to exist within your tenant.</span></span>

> [!NOTE]
> <span data-ttu-id="59023-136">บัญชีเหล่านี้จะต้องมีสิทธิ์การใช้งาน Power BI Pro เพื่อใช้งานพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="59023-136">These accounts will need to have Power BI Pro licenses in order to use workspaces.</span></span>

1. <span data-ttu-id="59023-137">ผู้ดูแลระบบ Power BI</span><span class="sxs-lookup"><span data-stu-id="59023-137">A Power BI admin.</span></span>

    <span data-ttu-id="59023-138">ขอแนะนำให้ผู้ใช้รายนี้เป็นสมาชิกของพื้นที่ทำงานทั้งหมดที่สร้างขึ้นเพื่อการฝัง</span><span class="sxs-lookup"><span data-stu-id="59023-138">It is recommended that this user be a member of all workspaces created for the purpose of embedding.</span></span>

2. <span data-ttu-id="59023-139">บัญชีผู้ใช้สำหรับนักวิเคราะห์ที่จะสร้างเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="59023-139">Accounts for analysts that will create content.</span></span>

    <span data-ttu-id="59023-140">ผู้ใช้เหล่านี้ควรที่จะกำหนดไว้สำหรับพื้นที่ทำงานตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="59023-140">These users should be assigned to workspaces as needed.</span></span>

3. <span data-ttu-id="59023-141">บัญชีผู้ใช้ *หลัก* หรือบัญชีผู้ใช้แบบฝังตัว</span><span class="sxs-lookup"><span data-stu-id="59023-141">An application *master* user account, or Embedded account.</span></span>

    <span data-ttu-id="59023-142">Backend แอปพลิเคชันจะจัดเก็บข้อมูลประจำตัวสำหรับบัญชีนี้ และใช้บัญชีนี้ขอรับโทเค็น Azure AD เพื่อใช้กับ Power BI REST API</span><span class="sxs-lookup"><span data-stu-id="59023-142">The applications backend will store the credentials for this account and use it for acquiring an Azure AD token for use with the Power BI REST APIs.</span></span> <span data-ttu-id="59023-143">บัญชีนี้จะถูกใช้เพื่อสร้างโทเค็นฝังตัวสำหรับแอป</span><span class="sxs-lookup"><span data-stu-id="59023-143">This account will be used to generate the embed token for the application.</span></span> <span data-ttu-id="59023-144">บัญชีนี้ยังต้องเป็นผู้ดูแลระบบของพื้นที่ทำงานที่สร้างขึ้นสำหรับการฝังด้วย</span><span class="sxs-lookup"><span data-stu-id="59023-144">This account also needs to be an admin of the workspaces created for embedding.</span></span>

> [!NOTE]
> <span data-ttu-id="59023-145">นี่คือบัญชีผู้ใช้ทั่วไปในองค์กรของคุณที่จะถูกใช้เพื่อทำการฝัง(embedding)</span><span class="sxs-lookup"><span data-stu-id="59023-145">This is just a regular user account in your organization that will be used for the purposes of embedding.</span></span>

## <a name="app-registration-and-permissions"></a><span data-ttu-id="59023-146">การลงทะเบียนแอปและสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="59023-146">App registration and permissions</span></span>

<span data-ttu-id="59023-147">คุณจะต้องลงทะเบียนแอปภายใน Azure AD และให้สิทธิ์บางอย่าง</span><span class="sxs-lookup"><span data-stu-id="59023-147">You will need to register an application within Azure AD and grant certain permissions.</span></span>

### <a name="register-an-application"></a><span data-ttu-id="59023-148">ลงทะเบียนแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="59023-148">Register an application</span></span>

<span data-ttu-id="59023-149">คุณจะต้องลงทะเบียนแอปพลิเคชันของคุณกับ Azure AD เพื่อเรียกใช้ REST API</span><span class="sxs-lookup"><span data-stu-id="59023-149">You will need to register your application with Azure AD in order to make REST API calls.</span></span> <span data-ttu-id="59023-150">ซึ่งรวมถึงการไปยังพอร์ทัล Azure เพื่อใช้ค่าคอนฟิกเพิ่มเติมนอกเหนือจากไปหน้าการลงทะเบียนแอป Power BI</span><span class="sxs-lookup"><span data-stu-id="59023-150">This includes going to the Azure portal to apply additional configuration in addition to the Power BI app registration page.</span></span> <span data-ttu-id="59023-151">สำหรับข้อมูลเพิ่มเติม ดู[ลงทะเบียนแอป Azure AD เมื่อต้องการฝังเนื้อหา Power BI](register-app.md)</span><span class="sxs-lookup"><span data-stu-id="59023-151">For more information, see [Register an Azure AD app to embed Power BI content](register-app.md).</span></span>

<span data-ttu-id="59023-152">คุณควรลงทะเบียนแอปด้วยบัญชีแอป **หลัก**</span><span class="sxs-lookup"><span data-stu-id="59023-152">You should register the application using the application **master** account.</span></span>

## <a name="create-workspaces-required"></a><span data-ttu-id="59023-153">สร้างพื้นที่ทำงาน (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="59023-153">Create workspaces (Required)</span></span>

<span data-ttu-id="59023-154">คุณสามารถใช้ประโยชน์จากพื้นที่ทำงานเพื่อทำการแบ่งแยกให้ดีขึ้นหากแอปพลิเคชันของคุณให้บริการลูกค้าหลายราย</span><span class="sxs-lookup"><span data-stu-id="59023-154">You can take advantage of workspaces to provide better isolation if your application is servicing multiple customers.</span></span> <span data-ttu-id="59023-155">ลูกค้าแต่ละรายของคุณจะได้รับแดชบอร์ดและรายงานที่ต่างกัน</span><span class="sxs-lookup"><span data-stu-id="59023-155">Dashboards and reports would be isolated between your customers.</span></span> <span data-ttu-id="59023-156">จากนั้นคุณสามารถใช้บัญชี Power BI ต่อพื้นที่ทำงานเพื่อทำให้ลูกค้าแต่ละรายได้รับประสบการณ์ในการใช้งานแอปพลิเคชันแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="59023-156">You could then use a Power BI account per workspace to further isolate application experiences between your customers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59023-157">คุณไม่สามารถใช้พื้นที่ทำงานส่วนบุคคลเพื่อใช้งานการฝังสำหรับผู้ใช้ที่ไม่ใช่ Power BI</span><span class="sxs-lookup"><span data-stu-id="59023-157">You cannot use a personal workspace to take advantage of embedding to non-Power BI users.</span></span>

<span data-ttu-id="59023-158">คุณจะต้องเป็นผู้ใช้ที่มีสิทธิ์การใช้งานรุ่น Pro เมื่อต้องสร้างพื้นที่ทำงานภายใน Power BI</span><span class="sxs-lookup"><span data-stu-id="59023-158">You will need a user that has a Pro license in order to create a workspace within Power BI.</span></span> <span data-ttu-id="59023-159">ผู้ใช้ Power BI ที่สร้างพื้นที่ทำงานจะเป็นผู้ดูแลระบบของพื้นที่ทำงานนั้นตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="59023-159">The Power BI user that creates the workspace will be an admin of that workspace by default.</span></span>

> [!NOTE]
> <span data-ttu-id="59023-160">บัญชีแอป *หลัก* ต้องเป็นผู้ดูแลระบบของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="59023-160">The application *master* account needs to be an admin of the workspace.</span></span>

## <a name="content-migration"></a><span data-ttu-id="59023-161">การโยกย้ายเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="59023-161">Content migration</span></span>

<span data-ttu-id="59023-162">การย้ายเนื้อหาของคุณจากคอลเลกชันพื้นที่ทำงานของคุณไปยัง Power BI Embedded สามารถทำได้ควบคู่ไปกับโซลูชันปัจจุบันของคุณ และไม่จำเป็นต้องหยุดการทำงานใดๆ</span><span class="sxs-lookup"><span data-stu-id="59023-162">Migrating your content from your workspace collections to Power BI Embedded can be done in parallel to your current solution and doesn't require any downtime.</span></span>

<span data-ttu-id="59023-163">**เครื่องมือการโยกย้าย** จะพร้อมใช้งานเพื่อช่วยคุณคัดลอกเนื้อหาจาก Power BI Workspace Collection ไปยัง Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="59023-163">A **migration tool** is available for you to use in order to assist with copying content from Power BI Workspace Collection to Power BI Embedded.</span></span> <span data-ttu-id="59023-164">โดยเฉพาะอย่างยิ่ง ถ้าคุณมีเนื้อหาจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="59023-164">Especially if you have a lot of content.</span></span> <span data-ttu-id="59023-165">สำหรับข้อมูลเพิ่มเติม ดู[เครื่องมือการโยกย้ายของ Power BI Embedded](migrate-tool.md)</span><span class="sxs-lookup"><span data-stu-id="59023-165">For more information, see [Power BI Embedded migration tool](migrate-tool.md).</span></span>

<span data-ttu-id="59023-166">การโยกย้ายเนื้อหามักใช้ API สองตัว</span><span class="sxs-lookup"><span data-stu-id="59023-166">Content migration relies mainly on two APIs.</span></span>

1. <span data-ttu-id="59023-167">ดาวน์โหลด PBIX - API นี้สามารถดาวน์โหลดไฟล์ PBIX ซึ่งถูกอัปโหลดไปยัง Power BI หลังจากเดือนตุลาคม 2016</span><span class="sxs-lookup"><span data-stu-id="59023-167">Download PBIX - this API can download PBIX files which were uploaded to Power BI after October 2016.</span></span>
2. <span data-ttu-id="59023-168">นำเข้า PBIX - API นี้อัปโหลดไฟล์ PBIX ใดๆ ไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="59023-168">Import PBIX - this API uploads any PBIX to Power BI.</span></span>

<span data-ttu-id="59023-169">สำหรับรหัสชุดย่อยที่เกี่ยวข้องบางอย่าง ดู[รหัสชุดย่อยเพื่อการโยกย้ายเนื้อหาจาก Power BI Workspace Collection](migrate-code-snippets.md)</span><span class="sxs-lookup"><span data-stu-id="59023-169">For some related code snippets, see [Code snippets for migrating content from Power BI Workspace Collection](migrate-code-snippets.md).</span></span>

### <a name="report-types"></a><span data-ttu-id="59023-170">ชนิดของรายงาน</span><span class="sxs-lookup"><span data-stu-id="59023-170">Report types</span></span>

<span data-ttu-id="59023-171">มีรายงานหลายชนิด แต่ละชนิดใช้โฟลว์การโยกย้ายที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="59023-171">There are several types of reports, each requiring a somewhat different migration flow.</span></span>

#### <a name="cached-dataset--report"></a><span data-ttu-id="59023-172">ชุดข้อมูลและรายงานที่แคชไว้</span><span class="sxs-lookup"><span data-stu-id="59023-172">Cached dataset & report</span></span>

<span data-ttu-id="59023-173">ชุดข้อมูลที่แคชหมายถึงไฟล์ PBIX ที่มีข้อมูลนำเข้าซึ่งตรงกันข้ามกับการเชื่อมต่อแบบสดหรือการเชื่อมต่อของ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="59023-173">Cached datasets refer to PBIX files that had imported data as opposed to a live connection or DirectQuery connection.</span></span>

<span data-ttu-id="59023-174">**ขั้นตอน**</span><span class="sxs-lookup"><span data-stu-id="59023-174">**Flow**</span></span>

1. <span data-ttu-id="59023-175">เรียก ดาวน์โหลด PBIX API จากพื้นที่ทำงาน PaaS</span><span class="sxs-lookup"><span data-stu-id="59023-175">Call Download PBIX API from PaaS workspace.</span></span>
2. <span data-ttu-id="59023-176">บันทึก PBIX</span><span class="sxs-lookup"><span data-stu-id="59023-176">Save PBIX.</span></span>
3. <span data-ttu-id="59023-177">เรียก นำเข้า PBIX ไปยังพื้นที่ทำงาน SaaS</span><span class="sxs-lookup"><span data-stu-id="59023-177">Call Import PBIX to SaaS workspace.</span></span>

#### <a name="directquery-dataset--report"></a><span data-ttu-id="59023-178">ชุดข้อมูลและรายงาน DirectQuery</span><span class="sxs-lookup"><span data-stu-id="59023-178">DirectQuery dataset & report</span></span>

<span data-ttu-id="59023-179">**ขั้นตอน**</span><span class="sxs-lookup"><span data-stu-id="59023-179">**Flow**</span></span>

1. <span data-ttu-id="59023-180">เรียก รับ `https://api.powerbi.com/v1.0/collections/{collection_id}/workspaces/{wid}/datasets/{dataset_id}/Default.GetBoundGatewayDataSources` และบันทึกสตริงการเชื่อมต่อที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="59023-180">Call GET `https://api.powerbi.com/v1.0/collections/{collection_id}/workspaces/{wid}/datasets/{dataset_id}/Default.GetBoundGatewayDataSources` and save connection string received.</span></span>
2. <span data-ttu-id="59023-181">เรียก ดาวน์โหลด PBIX API จากพื้นที่ทำงาน PaaS</span><span class="sxs-lookup"><span data-stu-id="59023-181">Call Download PBIX API from PaaS workspace.</span></span>
3. <span data-ttu-id="59023-182">บันทึก PBIX</span><span class="sxs-lookup"><span data-stu-id="59023-182">Save PBIX.</span></span>
4. <span data-ttu-id="59023-183">เรียก นำเข้า PBIX ไปยังพื้นที่ทำงาน SaaS</span><span class="sxs-lookup"><span data-stu-id="59023-183">Call Import PBIX to SaaS workspace.</span></span>
5. <span data-ttu-id="59023-184">อัปเดตสตริงการเชื่อมต่อโดยการเรียก - โพสต์  `https://api.powerbi.com/v1.0/myorg/datasets/{dataset_id}/Default.SetAllConnections`</span><span class="sxs-lookup"><span data-stu-id="59023-184">Update connection string by calling - POST  `https://api.powerbi.com/v1.0/myorg/datasets/{dataset_id}/Default.SetAllConnections`</span></span>
6. <span data-ttu-id="59023-185">รับ GW และตัวระบุแหล่งข้อมูลโดยการเรียก - รับ `https://api.powerbi.com/v1.0/myorg/datasets/{dataset_id}/Default.GetBoundGatewayDataSources`</span><span class="sxs-lookup"><span data-stu-id="59023-185">Get GW and datasource identifiers by calling - GET `https://api.powerbi.com/v1.0/myorg/datasets/{dataset_id}/Default.GetBoundGatewayDataSources`</span></span>
7. <span data-ttu-id="59023-186">ปรับปรุงข้อมูลประจำตัวของผู้ใช้โดยการเรียก - โปรแกรมแก้ไข `https://api.powerbi.com/v1.0/myorg/gateways/{gateway_id}/datasources/{datasource_id}`</span><span class="sxs-lookup"><span data-stu-id="59023-186">Update user's credentials by calling - PATCH `https://api.powerbi.com/v1.0/myorg/gateways/{gateway_id}/datasources/{datasource_id}`</span></span>

#### <a name="old-dataset--reports"></a><span data-ttu-id="59023-187">ชุดข้อมูลและรายงานเก่า</span><span class="sxs-lookup"><span data-stu-id="59023-187">Old dataset & reports</span></span>

<span data-ttu-id="59023-188">ต่อไปนี้เป็นชุดข้อมูล/รายงานที่สร้างขึ้นก่อนเดือนตุลาคม 2016</span><span class="sxs-lookup"><span data-stu-id="59023-188">These are datasets/reports created before October 2016.</span></span> <span data-ttu-id="59023-189">ดาวน์โหลด PBIX ไม่สนับสนุนไฟล์ PBIXs ซึ่งถูกอัปโหลดก่อนเดือนตุลาคม 2016</span><span class="sxs-lookup"><span data-stu-id="59023-189">Download PBIX doesn't support PBIXs which were uploaded before October 2016</span></span>

<span data-ttu-id="59023-190">**ขั้นตอน**</span><span class="sxs-lookup"><span data-stu-id="59023-190">**Flow**</span></span>

1. <span data-ttu-id="59023-191">รับ PBIX จากสภาพแวดล้อมการพัฒนาของคุณ (ตัวควบคุมแหล่งข้อมูลภายในของคุณ)</span><span class="sxs-lookup"><span data-stu-id="59023-191">Get PBIX from your development environment (your internal source control).</span></span>
2. <span data-ttu-id="59023-192">เรียก นำเข้า PBIX ไปยังพื้นที่ทำงาน SaaS</span><span class="sxs-lookup"><span data-stu-id="59023-192">Call Import PBIX to SaaS workspace.</span></span>

#### <a name="push-dataset--report"></a><span data-ttu-id="59023-193">พุช (Push) ชุดข้อมูลและรายงาน</span><span class="sxs-lookup"><span data-stu-id="59023-193">Push Dataset & report</span></span>

<span data-ttu-id="59023-194">ดาวน์โหลด PBIX ไม่สนับสนุนชุดข้อมูล *API พุช*</span><span class="sxs-lookup"><span data-stu-id="59023-194">Download PBIX doesn't support *Push API* datasets.</span></span> <span data-ttu-id="59023-195">ข้อมูลของชุดข้อมูล API พุชไม่สามารถโอนย้ายจาก PaaS ไปยัง SaaS ได้</span><span class="sxs-lookup"><span data-stu-id="59023-195">Push API dataset data can't be ported from PaaS to SaaS.</span></span>

<span data-ttu-id="59023-196">**ขั้นตอน**</span><span class="sxs-lookup"><span data-stu-id="59023-196">**Flow**</span></span>

1. <span data-ttu-id="59023-197">เรียก "สร้างชุดข้อมูล" API ด้วยชุดข้อมูล json เมื่อต้องสร้างชุดข้อมูลในพื้นที่ทำงาน SaaS</span><span class="sxs-lookup"><span data-stu-id="59023-197">Call "Create dataset" API with dataset Json to create dataset in SaaS workspace.</span></span>
2. <span data-ttu-id="59023-198">สร้างรายงานอีกครั้งสำหรับชุดข้อมูลที่ถูกสร้าง\*</span><span class="sxs-lookup"><span data-stu-id="59023-198">Rebuild report for the created dataset\*.</span></span>

<span data-ttu-id="59023-199">โดยใช้วิธีแก้ไขปัญหาบางอย่าง คุณสามารถโยกย้ายรายงาน API พุชจาก PaaS ไปยัง SaaS ด้วยการทำต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="59023-199">It is possible, using some workarounds, to migrate the push api report from PaaS to SaaS by trying the following.</span></span>

1. <span data-ttu-id="59023-200">อัปโหลด PBIX บางตัวอย่างไปยังพื้นที่ทำงาน PaaS</span><span class="sxs-lookup"><span data-stu-id="59023-200">Uploading some dummy PBIX to PaaS workspace.</span></span>
2. <span data-ttu-id="59023-201">โคลนรายงาน API พุชและผูกกับ PBIX ตัวอย่างจากขั้นตอนที่ 1</span><span class="sxs-lookup"><span data-stu-id="59023-201">Clone the push api report and bind it to the dummy PBIX from step 1.</span></span>
3. <span data-ttu-id="59023-202">ดาวน์โหลดรายงาน API พุชด้วย PBIX ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="59023-202">Download push API report with the dummy PBIX.</span></span>
4. <span data-ttu-id="59023-203">อัปโหลด PBIX ตัวอย่างไปยังพื้นที่ทำงานของ SaaS</span><span class="sxs-lookup"><span data-stu-id="59023-203">Upload dummy PBIX to your SaaS workspace.</span></span>
5. <span data-ttu-id="59023-204">สร้างชุดข้อมูลแบบพุชในพื้นที่ทำงาน SaaS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="59023-204">Create push dataset in your SaaS workspace.</span></span>
6. <span data-ttu-id="59023-205">ผูกรายงานกับชุดข้อมูล API พุชอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="59023-205">Rebind report to push api dataset.</span></span>

## <a name="create-and-upload-new-reports"></a><span data-ttu-id="59023-206">สร้างและอัปโหลดรายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="59023-206">Create and upload new reports</span></span>

<span data-ttu-id="59023-207">นอกเหนือจากเนื้อหาที่คุณโยกย้ายจากคอลเลกชันพื้นที่ทำงานของ Power BI คุณสามารถสร้างรายงานและชุดข้อมูลโดยใช้ Power BI Desktop แล้วเผยแพร่รายงานเหล่านั้นไปยังพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="59023-207">In addition to the content you migrated from the Power BI Workspace Collection, you can create your reports and datasets using Power BI Desktop and then publish those reports to a workspace.</span></span> <span data-ttu-id="59023-208">ผู้ใช้ปลายทางที่เผยแพร่รายงานจำเป็นต้องมีสิทธิ์การใช้งาน Power BI Pro เพื่อเผยแพร่ไปยังพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="59023-208">The end user publishing the reports need to have a Power BI Pro license in order to publish to a workspace.</span></span>

## <a name="rebuild-your-application"></a><span data-ttu-id="59023-209">สร้างแอปพลิเคชันของคุณอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="59023-209">Rebuild your application</span></span>

1. <span data-ttu-id="59023-210">คุณจะต้องปรับเปลี่ยนแอปของคุณเมื่อต้องใช้ Power BI REST API และตำแหน่งที่ตั้งของรายงานภายใน powerbi.com</span><span class="sxs-lookup"><span data-stu-id="59023-210">You will need to modify your application to use the Power BI REST APIs and the report location inside powerbi.com.</span></span>
2. <span data-ttu-id="59023-211">สร้างการรับรองสิทธิ์ AuthN/AuthZ ของคุณอีกครั้งโดยใช้บัญชีผู้ใช้ *หลัก* ของแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="59023-211">Rebuild your AuthN/AuthZ authentication using the *master* account for your application.</span></span> <span data-ttu-id="59023-212">คุณสามารถใช้[โทเค็นการฝัง](/rest/api/power-bi/embedtoken)เพื่ออนุญาตให้ผู้ใช้รายนี้ดำเนินการในนามของผู้ใช้อื่นได้</span><span class="sxs-lookup"><span data-stu-id="59023-212">You can take advantage of using an [embed token](/rest/api/power-bi/embedtoken) to allow this user to act on behalf of other users.</span></span>
3. <span data-ttu-id="59023-213">ฝังรายงานของคุณจาก powerbi.com ลงในแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="59023-213">Embed your reports from powerbi.com into your application.</span></span>

## <a name="map-your-users-to-a-power-bi-user"></a><span data-ttu-id="59023-214">แมปผู้ใช้ของคุณให้กับผู้ใช้ Power BI</span><span class="sxs-lookup"><span data-stu-id="59023-214">Map your users to a Power BI user</span></span>

<span data-ttu-id="59023-215">ภายในแอปของคุณ คุณจะแมปผู้ใช้ที่คุณจัดการภายในแอปไปยังข้อมูลประจำตัว *หลัก* ของ Power BI เพื่อใช้งานแอปพลิเคชันของคุณ</span><span class="sxs-lookup"><span data-stu-id="59023-215">Within your application, you will map users that you manage within the application to a *master* Power BI credential for the purposes of your application.</span></span> <span data-ttu-id="59023-216">ข้อมูลประจำตัวสำหรับบัญชี *หลัก* Power BI นี้ีจะถูกเก็บไว้ภายในแอปพลิเคชันของคุณ และใช้เพื่อสร้างโทเค็นแบบฝัง</span><span class="sxs-lookup"><span data-stu-id="59023-216">The credentials for this Power BI *master* account will be stored within your application and be used to creating embed tokens.</span></span>

## <a name="what-to-do-when-you-are-ready-for-production"></a><span data-ttu-id="59023-217">สิ่งที่ต้องทำเมื่อคุณพร้อมสำหรับการผลิต</span><span class="sxs-lookup"><span data-stu-id="59023-217">What to do when you are ready for production</span></span>

<span data-ttu-id="59023-218">เมื่อคุณพร้อมที่จะทำการผลิต คุณจะต้องทำสิ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="59023-218">When you are ready to move to production, you will need to do the following.</span></span>

* <span data-ttu-id="59023-219">ถ้าคุณกำลังใช้ผู้เช่าที่แยกต่างหากเพื่อการทำงานนี้ คุณจะต้องตรวจสอบให้แน่ใจว่าพื้นที่ทำงานของคุณ และแดชบอร์ดและรายงานพร้อมใช้งานในสภาพแวดล้อมการผลิตของคุณ</span><span class="sxs-lookup"><span data-stu-id="59023-219">If you are using a separate tenant for development, then you will need to make sure your workspaces, along with dashboards and reports, are available in your production environment.</span></span> <span data-ttu-id="59023-220">นอกจากนี้ คุณจะจำเป็นต้องตรวจสอบให้แน่ใจว่าคุณได้สร้างแอปใน Azure AD สำหรับผู้เช่าการผลิตของคุณ และกำหนดสิทธิ์ app ที่เหมาะสมตามที่ระบุในขั้นตอนที่ 1</span><span class="sxs-lookup"><span data-stu-id="59023-220">You will also need to make sure that you created the application in Azure AD for your production tenant and assigned the proper app permissions as indicated in Step 1.</span></span>
* <span data-ttu-id="59023-221">ซื้อความสามารถการผลิต (capacity) ที่เหมาะสมกับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="59023-221">Purchase a capacity that fits your needs.</span></span> <span data-ttu-id="59023-222">เพื่อให้เข้าใจว่าคุณต้องใช้ปริมาณและชนิดของความสามารถการผลิตอย่างไร ดูเอกสารทางเทคนิคเรื่องการวางแผนความสามารถวิเคราะห์ของ[Power BI Embedded](./embedded-capacity-planning.md)</span><span class="sxs-lookup"><span data-stu-id="59023-222">To better understand how the amount and type of capacity you need, see the [Power BI Embedded analytics capacity planning whitepaper](./embedded-capacity-planning.md).</span></span> <span data-ttu-id="59023-223">คุณสามารถ[ซื้อความสามารถการผลิต](https://portal.azure.com/#create/Microsoft.PowerBIDedicated)ใน Azure ได้</span><span class="sxs-lookup"><span data-stu-id="59023-223">You can [purchase capacity](https://portal.azure.com/#create/Microsoft.PowerBIDedicated) in Azure.</span></span>
* <span data-ttu-id="59023-224">แก้ไขพื้นที่ทำงาน และกำหนดพื้นที่นี้เป็นความจุแบบพรีเมียมภายใต้ขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="59023-224">Edit the workspace and assign it to a Premium capacity under advanced.</span></span>

    ![ความจุแบบพรีเมียม](media/migrate-from-powerbi-embedded/powerbi-embedded-premium-capacity02.png)

* <span data-ttu-id="59023-226">ปรับใช้แอปของคุณที่อัปเดตแล้วกับการผลิต และเริ่มต้นฝังรายงานจาก Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="59023-226">Deploy your updated application to production and begin embedding reports from the Power BI Embedded.</span></span>

## <a name="after-migration"></a><span data-ttu-id="59023-227">หลังจากการโยกย้าย</span><span class="sxs-lookup"><span data-stu-id="59023-227">After migration</span></span>

<span data-ttu-id="59023-228">คุณควรทำการล้างข้อมูลบางอย่างภายใน Azure</span><span class="sxs-lookup"><span data-stu-id="59023-228">You should do some cleanup within Azure.</span></span>

* <span data-ttu-id="59023-229">ลบพื้นที่ทำงานทั้งหมดออกจากโซลูชันที่ถูกใช้ภายใน Azure Embedded ของ Power BI Workspace Collection</span><span class="sxs-lookup"><span data-stu-id="59023-229">Remove all workspaces off of the deployed solution within the Azure Embedded of Power BI Workspace Collection.</span></span>
* <span data-ttu-id="59023-230">ลบคอลเลกชันพื้นที่ทำงานใดๆ ที่มีอยู่ภายใน Azure</span><span class="sxs-lookup"><span data-stu-id="59023-230">Delete any Workspace Collections that exist within Azure.</span></span>

## <a name="next-steps"></a><span data-ttu-id="59023-231">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="59023-231">Next steps</span></span>

[<span data-ttu-id="59023-232">ฝังด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="59023-232">Embedding with Power BI</span></span>](embedding.md)  
[<span data-ttu-id="59023-233">เครื่องมือการโยกย้ายเนื้อหาของ Power BI Worksapce Collection</span><span class="sxs-lookup"><span data-stu-id="59023-233">Power BI Workspace Collection migration tool</span></span>](migrate-tool.md)  
[<span data-ttu-id="59023-234">รหัสชุดย่อยสำหรับการโยกย้ายเนื้อหาจาก Power BI Workspace Collection</span><span class="sxs-lookup"><span data-stu-id="59023-234">Code snippets for migrating content from Power BI Workspace Collection</span></span>](migrate-code-snippets.md)  
[<span data-ttu-id="59023-235">วิธีฝัง แดชบอร์ด รายงาน และไทล์ Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="59023-235">How to embed your Power BI dashboards, reports and tiles</span></span>](embed-sample-for-your-organization.md)  
[<span data-ttu-id="59023-236">Power BI Premium คืออะไร</span><span class="sxs-lookup"><span data-stu-id="59023-236">Power BI Premium - what is it?</span></span>](../../admin/service-premium-what-is.md)  
[<span data-ttu-id="59023-237">JavaScript API Git repo</span><span class="sxs-lookup"><span data-stu-id="59023-237">JavaScript API Git repo</span></span>](https://github.com/Microsoft/PowerBI-JavaScript)  
[<span data-ttu-id="59023-238">Power BI C# Git repo</span><span class="sxs-lookup"><span data-stu-id="59023-238">Power BI C# Git repo</span></span>](https://github.com/Microsoft/PowerBI-CSharp)  
[<span data-ttu-id="59023-239">ตัวอย่างการฝัง JavaScript</span><span class="sxs-lookup"><span data-stu-id="59023-239">JavaScript embed sample</span></span>](https://microsoft.github.io/PowerBI-JavaScript/demo/)  
[<span data-ttu-id="59023-240">เอกสารทางเทคนิคเรื่องการวางแผนความสามารถวิเคราะห์ของ Workspace Collection</span><span class="sxs-lookup"><span data-stu-id="59023-240">Workspace Collection analytics capacity planning whitepaper</span></span>](./embedded-capacity-planning.md)  
[<span data-ttu-id="59023-241">เอกสารบรรยายแนวความคิดของ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="59023-241">Power BI Premium whitepaper</span></span>](https://aka.ms/pbipremiumwhitepaper)  

<span data-ttu-id="59023-242">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="59023-242">More questions?</span></span> [<span data-ttu-id="59023-243">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="59023-243">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)