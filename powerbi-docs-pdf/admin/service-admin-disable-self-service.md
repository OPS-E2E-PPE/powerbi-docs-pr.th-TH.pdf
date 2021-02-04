---
title: เปิดหรือปิดใช้งานการลงชื่อสมัครใช้และการสั่งซื้อบริการด้วยตนเอง
description: วิธีการข้อมูลสำหรับผู้ดูแลระบบในการปิดความสามารถสำหรับผู้ใช้ในการสมัครใช้บริการ Power BI และซื้อหรืออัปเกรดสิทธิการใช้งาน
author: mihart
ms.author: mihart
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: how-to
ms.date: 04/08/2020
ms.custom: licensing support
LocalizationGroup: Administration
ms.openlocfilehash: ff695d49caeab7bed88b932cec6aaec11ec4df29
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413690"
---
# <a name="enable-or-disable-self-service-sign-up-and-purchasing"></a><span data-ttu-id="660f7-103">เปิดหรือปิดใช้งานการลงชื่อสมัครใช้และการสั่งซื้อบริการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="660f7-103">Enable or disable self-service sign-up and purchasing</span></span>

<span data-ttu-id="660f7-104">ในองค์กรส่วนใหญ่ จะเปิดใช้งานการลงชื่อสมัครใช้บริการด้วยตนเองไว้เป็นค่าเริ่มต้นอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="660f7-104">In most organizations, self-service sign-up is enabled by default.</span></span> <span data-ttu-id="660f7-105">ผู้ใช้แต่ละคนในองค์กรของคุณสามารถลงทะเบียน Power BI โดยใช้บัญชีของสถานที่ทำงานหรือของโรงเรียนของตนเองได้</span><span class="sxs-lookup"><span data-stu-id="660f7-105">Individual users in your organization can sign up for Power BI using their work or school account.</span></span> <span data-ttu-id="660f7-106">และผู้ใช้อาจได้รับการเสนอตัวเลือกเพื่อซื้อสิทธิการใช้งาน Power BI Pro โดยตรง ถ้าผู้ใช้พยายามใช้งานคุณลักษณะที่ต้องใช้ในระดับ Pro</span><span class="sxs-lookup"><span data-stu-id="660f7-106">Users may also be offered the option to directly purchase a Power BI Pro license if they try to use a feature that requires Pro.</span></span> <span data-ttu-id="660f7-107">ในฐานะผู้ดูแลระบบ คุณสามารถกำหนดได้ว่าจะเปิดหรือปิดใช้งานการลงชื่อสมัครใช้บริการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="660f7-107">As an administrator, you determine whether to enable or disable self-service sign-up.</span></span> <span data-ttu-id="660f7-108">และคุณยังสามารถควบคุมว่าผู้ใช้ในองค์กรของคุณสามารถทำการซื้อบริการต่าง ๆ ด้วยตนเองเพื่อรับสิทธิการใช้งานของตนเองได้หรือไม่อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="660f7-108">You can also control whether users in your organization can make self-service purchases to get their own license.</span></span>

> [!NOTE]
><span data-ttu-id="660f7-109">ถ้าคุณได้รับ Power BI ผ่านทางผู้ให้บริการโซลูชัน Cloud ของ Microsoft (CSP) การตั้งค่าอาจถูกปิดใช้งานไว้เพื่อไม่ให้ผู้ใช้สามารถลงทะเบียนเป็นรายบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="660f7-109">If you acquired Power BI through a Microsoft Cloud Solution Provider (CSP), the setting might be disabled to block users from signing up individually.</span></span> <span data-ttu-id="660f7-110">CSP ของคุณอาจทำหน้าที่เป็นผู้ดูแลระบบส่วนกลางสำหรับองค์กรของคุณด้วย ซึ่งทำให้คุณต้องติดต่อพวกเขาเพื่อช่วยคุณเปลี่ยนการตั้งค่านี้</span><span class="sxs-lookup"><span data-stu-id="660f7-110">Your CSP may also be acting as the global admin for your organization, requiring that you contact them to help you change this setting.</span></span>
>
>

<span data-ttu-id="660f7-111">คุณใช้คำสั่ง PowerShell เพื่อเปลี่ยนการตั้งค่าที่ควบคุมการลงชื่อสมัครใช้บริการและการซื้อด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="660f7-111">You use PowerShell commands to change the settings that control self-service sign-up and purchasing.</span></span> <span data-ttu-id="660f7-112">มีสองการตั้งค่าที่ควบคุมว่าผู้ใช้ในองค์กรของคุณสามารถทำการลงชื่อสมัครใช้บริการด้วยตนเองหรือทำการสั่งซื้อบริการของตนเองได้</span><span class="sxs-lookup"><span data-stu-id="660f7-112">There are two settings that control whether users in your organization can do self-service sign-up or make self-service purchases.</span></span>

- <span data-ttu-id="660f7-113">หากคุณต้องการปิดใช้งานการลงชื่อสมัครใช้บริการด้วยตนเองทั้งหมด ให้เปลี่ยนการตั้งค่าใน Azure Active Directory ที่ชื่อ **AllowAdHocSubscriptions** โดยใช้คำสั่ง Azure AD PowerShell</span><span class="sxs-lookup"><span data-stu-id="660f7-113">If you want to disable all self-service sign-ups, change a setting in Azure Active Directory named **AllowAdHocSubscriptions** by using Azure AD PowerShell commands.</span></span> <span data-ttu-id="660f7-114">ให้ปฏิบัติตามขั้นตอนในบทความนี้เพื่อ [เปิดหรือปิดใช้งานการลงชื่อสมัครใช้บริการด้วยตนเอง](#enable-or-disable-self-service-signup)</span><span class="sxs-lookup"><span data-stu-id="660f7-114">Follow the steps in this article to [enable or disable self-service signup](#enable-or-disable-self-service-signup).</span></span> <span data-ttu-id="660f7-115">ตัวเลือกนี้จะเปิดใช้งานการลงชื่อสมัครใช้บริการด้วยตนเองสำหรับแอปและบริการที่ใช้งานระบบคลาวด์ของ Microsoft *ทั้งหมด*</span><span class="sxs-lookup"><span data-stu-id="660f7-115">This option turns off self-service sign-up for *all* Microsoft cloud-based apps and services.</span></span>

- <span data-ttu-id="660f7-116">หากคุณต้องการป้องกันไม่ให้ผู้ใช้ซื้อสิทธิการใช้งาน Pro ของตนเอง ให้เปลี่ยนการตั้งค่า **AllowSelfServicePurchase** โดยใช้คำสั่ง MSCommerce PowerShell</span><span class="sxs-lookup"><span data-stu-id="660f7-116">If you want to prevent users from purchasing their own Pro license, change the **AllowSelfServicePurchase** setting using MSCommerce PowerShell commands.</span></span> <span data-ttu-id="660f7-117">การตั้งค่านี้ช่วยให้คุณปิดการสั่งซื้อบริการผลิตภัณฑ์ที่เฉพาะเจาะจงด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="660f7-117">This setting lets you turn off self-service purchase for specific products.</span></span> <span data-ttu-id="660f7-118">ให้ปฏิบัติตามขั้นตอนในบทความนี้เพื่อ[เปิดหรือปิดใช้งานการสั่งซื้อสิทธิการใช้งาน Power BI Pro ด้วยตนเอง](#enable-or-disable-self-service-purchase)</span><span class="sxs-lookup"><span data-stu-id="660f7-118">Follow the steps in this article to [enable or disable self-service purchase of Power BI Pro licenses](#enable-or-disable-self-service-purchase).</span></span>

## <a name="enable-or-disable-self-service-signup"></a><span data-ttu-id="660f7-119">เปิดหรือปิดใช้งานการลงชื่อสมัครใช้บริการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="660f7-119">Enable or disable self-service signup</span></span>

<span data-ttu-id="660f7-120">หากมีการเปิดใช้งานการลงชื่อสมัครใช้บริการด้วยตนเองไว้ ค่าของ **AllowAdHocSubscriptions** จะเป็น *จริง*</span><span class="sxs-lookup"><span data-stu-id="660f7-120">If self-service sign-up is enabled, the value of **AllowAdHocSubscriptions** is *true*.</span></span> <span data-ttu-id="660f7-121">มาดูกันว่าจะเกิดอะไรขึ้นหากคุณเปลี่ยนการตั้งค่านี้เป็น *เท็จ*:</span><span class="sxs-lookup"><span data-stu-id="660f7-121">Let's take a look at what happens when you change this setting to *false*:</span></span>

- <span data-ttu-id="660f7-122">หากคุณเปลี่ยนการตั้งค่าจากจริงไปเป็นเท็จ จะเป็นการปิดกั้นไม่ให้ผู้ใช้ใหม่ในองค์กรของคุณทำการลงทะเบียนเป็นรายบุคคล</span><span class="sxs-lookup"><span data-stu-id="660f7-122">If you change the setting from true to false, new users in your organization are blocked from signing up individually.</span></span> <span data-ttu-id="660f7-123">สำหรับผู้ใช้ที่ลงทะเบียน Power BI ก่อนเปลี่ยนแปลงการตั้งค่าจะยังคงมีสิทธิ์ในสิทธิการใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="660f7-123">Any users that signed up for Power BI before you change the setting keep their licenses.</span></span>

- <span data-ttu-id="660f7-124">หากคุณเปลี่ยนการตั้งค่าเป็นเท็จ ผู้ใช้ที่มีสิทธิการใช้งาน Power BI (ฟรี) อยู่แล้วจะยังคงสามารถลงทะเบียนสำหรับ Power BI Pro รุ่นทดลองเพื่อใช้เฉพาะรายบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="660f7-124">If you change the setting to false, users that already have a Power BI (free) license can still sign up for an individual Power BI Pro trial.</span></span>

- <span data-ttu-id="660f7-125">ผู้ดูแลระบบจำเป็นต้องกำหนดสิทธิการใช้งาน Power BI ทั้งหมดให้กับผู้ใช้ใหม่ที่ต้องการสิทธิ</span><span class="sxs-lookup"><span data-stu-id="660f7-125">An admin needs to assign all Power BI licenses to new users who need one.</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="660f7-126">ก่อนที่คุณเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="660f7-126">Before you begin</span></span>

<span data-ttu-id="660f7-127">ขั้นตอนเหล่านี้ใช้คำสั่ง PowerShell ของ Azure Active Directory เพื่อเปลี่ยนค่าของการตั้งค่า **AllowAdHocSubscriptions**</span><span class="sxs-lookup"><span data-stu-id="660f7-127">These steps use Azure Active Directory PowerShell commands to change the value of the **AllowAdHocSubscriptions** setting.</span></span> <span data-ttu-id="660f7-128">คุณต้องมีโมดูล Azure AD PowerShell ที่ติดตั้งไว้สำหรับคำสั่งเหล่านี้เพื่อให้สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="660f7-128">You must have the Azure AD PowerShell module installed for these commands to be available.</span></span> <span data-ttu-id="660f7-129">คุณสามารถศึกษาข้อมูลเพิ่มเติมเกี่ยวกับการใช้ PowerShell ได้ที่ [เริ่มต้นใช้งาน Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7)</span><span class="sxs-lookup"><span data-stu-id="660f7-129">For more information about using PowerShell, see [Getting started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7).</span></span>

<span data-ttu-id="660f7-130">ในการติดตั้งโมดูล Azure AD ให้เริ่มใช้งาน Windows PowerShell ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="660f7-130">To install the Azure AD module, start Windows PowerShell as an administrator.</span></span> <span data-ttu-id="660f7-131">ตรวจสอบให้มั่นใจว่านโยบายการดำเนินการภายในเครื่องของคุณอนุญาตให้คุณเรียกใช้สคริปต์ได้</span><span class="sxs-lookup"><span data-stu-id="660f7-131">Make sure your local execution policy allows you to run scripts.</span></span> <span data-ttu-id="660f7-132">หากคุณพบปัญหา โปรอ่าน[นโยบายการดำเนินการของ PowerShell](/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7#powershell-execution-policies) เพื่อเรียนรู้วิธีการเปลี่ยนแปลงนโยบายภายในเครื่องของคุณ</span><span class="sxs-lookup"><span data-stu-id="660f7-132">If you run into problems, see [PowerShell execution policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7#powershell-execution-policies) to learn how to change your local policy.</span></span>

<span data-ttu-id="660f7-133">เรียกใช้คำสั่งต่อไปนี้เพื่อติดตั้งโมดูล Azure AD:</span><span class="sxs-lookup"><span data-stu-id="660f7-133">Run the following command to install the Azure AD module:</span></span>

```powershell
Install-Module MSOnline
```

### <a name="change-the-self-service-signup-policy"></a><span data-ttu-id="660f7-134">เปลี่ยนนโยบายการลงชื่อสมัครใช้บริการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="660f7-134">Change the self-service signup policy</span></span>

<span data-ttu-id="660f7-135">ใน PowerShell ให้เรียกใช้คำสั่งต่อไปนี้เพื่อเชื่อมต่อไปยัง Azure AD:</span><span class="sxs-lookup"><span data-stu-id="660f7-135">In PowerShell, run the following command to connect to Azure AD:</span></span>

```powershell
Connect-MsolService
```

<span data-ttu-id="660f7-136">ป้อนข้อมูลประจำตัวผู้ดูแลระบบของคุณลงในกล่องโต้ตอบการลงชื่อเข้าใช้ จากนั้นดำเนินการรับรองความถูกต้องแบบสองปัจจัยที่อาจจำเป็นต้องทำ</span><span class="sxs-lookup"><span data-stu-id="660f7-136">Enter your admin credentials in the sign-in dialog, completing any two-factor authentication that may be needed.</span></span> <span data-ttu-id="660f7-137">หลังจากการตรวจสอบ คุณจะกลับไปยังหน้าต่าง PowerShell</span><span class="sxs-lookup"><span data-stu-id="660f7-137">After verification, you're returned to the PowerShell window.</span></span>

<span data-ttu-id="660f7-138">หากต้องการดูการตั้งค่าปัจจุบัน ให้เรียกใช้คำสั่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="660f7-138">To view the current setting, run the following command.</span></span> <span data-ttu-id="660f7-139">ผลลัพธ์จะถูกส่งไปยังรายการที่จัดรูปแบบไว้โดยใช้สวิตช์ "fl"</span><span class="sxs-lookup"><span data-stu-id="660f7-139">The output is piped to a formatted list by using the "fl" switch.</span></span>

```powershell
Get-MsolCompanyInformation | fl AllowAdHocSubscriptions
```

<span data-ttu-id="660f7-140">หากต้องการเปลี่ยนการตั้งค่าปัจจุบัน ให้เรียกใช้คำสั่งนี้:</span><span class="sxs-lookup"><span data-stu-id="660f7-140">To change the current setting, run this command:</span></span>

```powershell
Set-MsolCompanySettings -AllowAdHocSubscriptions $false
```

<span data-ttu-id="660f7-141">หลังจากเรียกใช้คำสั่งนี้ ระบบจะปิดการลงชื่อสมัครใช้บริการด้วยตนเองของผู้ใช้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="660f7-141">After running this command, self-service signup is disabled for all users.</span></span> <span data-ttu-id="660f7-142">หากต้องการเปิดใช้งานอีกครั้ง ให้เรียกใช้คำสั่งนี้ใหม่แล้วตั้งค่าให้เป็น $true</span><span class="sxs-lookup"><span data-stu-id="660f7-142">To turn it back on, run this command again and set the value to $true.</span></span>

## <a name="enable-or-disable-self-service-purchase"></a><span data-ttu-id="660f7-143">เปิดหรือปิดใช้งานการสั่งซื้อบริการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="660f7-143">Enable or disable self-service purchase</span></span>

<span data-ttu-id="660f7-144">หากเปิดใช้งานการสั่งซื้อบริการด้วยตนเองไว้ ค่าของ **AllowSelfServicePurchase** จะเป็น *จริง*</span><span class="sxs-lookup"><span data-stu-id="660f7-144">If self-service purchasing is enabled, the value of **AllowSelfServicePurchase** is *true*.</span></span> <span data-ttu-id="660f7-145">มาดูกันว่าจะเกิดอะไรขึ้นหากคุณเปลี่ยนการตั้งค่านี้เป็น *เท็จ*:</span><span class="sxs-lookup"><span data-stu-id="660f7-145">Let's take a look at what happens when you change this setting to *false*:</span></span>

- <span data-ttu-id="660f7-146">หากคุณเปลี่ยนการตั้งค่าจากจริงไปเป็นเท็จ จะเป็นการปิดกั้นไม่ให้ผู้ใช้ในองค์กรของคุณทำการสั่งซื้อสิทธิการใช้งาน Power BI Pro ของตนเองได้</span><span class="sxs-lookup"><span data-stu-id="660f7-146">If you change the setting from true to false,  users in your organization are blocked from buying their own Power BI Pro license.</span></span> <span data-ttu-id="660f7-147">สำหรับผู้ใช้ที่ซื้อ Power BI ก่อนเปลี่ยนแปลงการตั้งค่าจะยังคงมีสิทธิ์ในสิทธิการใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="660f7-147">Any users that bought a license before you change the setting keep their licenses.</span></span>

- <span data-ttu-id="660f7-148">หากคุณเปลี่ยนการตั้งค่าเป็นเท็จ ผู้ใช้ที่มีสิทธิการใช้งาน Power BI (ฟรี) จะไม่สามารถสั่งซื้อ Power BI Pro ของตนเองได้</span><span class="sxs-lookup"><span data-stu-id="660f7-148">If you change the setting to false, users that have a Power BI (free) license can't get an individual Power BI Pro license.</span></span> 

- <span data-ttu-id="660f7-149">ผู้ดูแลระบบจำเป็นต้องกำหนดสิทธิ์การใช้งานแบบ Pro ให้กับผู้ใช้ทั้งหมดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="660f7-149">An admin needs to assign a Pro license to all users that need one.</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="660f7-150">ก่อนที่คุณเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="660f7-150">Before you begin</span></span>

<span data-ttu-id="660f7-151">ขั้นตอนเหล่านี้ใช้คำสั่ง MSCommerce PowerShell เพื่อเปลี่ยนค่าในการตั้งค่าของ **AllowSelfServicePurchase**</span><span class="sxs-lookup"><span data-stu-id="660f7-151">These steps use MSCommerce PowerShell commands to change the value of the **AllowSelfServicePurchase** setting.</span></span> <span data-ttu-id="660f7-152">คุณต้องมีโมดูล MSCommerce PowerShell ที่ติดตั้งไว้สำหรับคำสั่งเหล่านี้เพื่อให้สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="660f7-152">You must have the MSCommerce PowerShell module installed for these commands to be available.</span></span> <span data-ttu-id="660f7-153">คุณสามารถศึกษาข้อมูลเพิ่มเติมเกี่ยวกับการใช้ PowerShell ได้ที่ [เริ่มต้นใช้งาน Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7)</span><span class="sxs-lookup"><span data-stu-id="660f7-153">For more information about using PowerShell, see [Getting started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7).</span></span>

<span data-ttu-id="660f7-154">ในการติดตั้งโมดูล MSCommerce ให้เริ่มใช้งาน Windows PowerShell ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="660f7-154">To install the MSCommerce module, start Windows PowerShell as an administrator.</span></span> <span data-ttu-id="660f7-155">ตรวจสอบให้มั่นใจว่านโยบายการดำเนินการภายในเครื่องของคุณอนุญาตให้คุณเรียกใช้สคริปต์ได้</span><span class="sxs-lookup"><span data-stu-id="660f7-155">Make sure your local execution policy allows you to run scripts.</span></span> <span data-ttu-id="660f7-156">หากคุณพบปัญหา โปรอ่าน[นโยบายการดำเนินการของ PowerShell](/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7#powershell-execution-policies) เพื่อเรียนรู้วิธีการเปลี่ยนแปลงนโยบายภายในเครื่องของคุณ</span><span class="sxs-lookup"><span data-stu-id="660f7-156">If you run into problems, see [PowerShell execution policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7#powershell-execution-policies) to learn how to change your local policy.</span></span>

<span data-ttu-id="660f7-157">เรียกใช้คำสั่งต่อไปนี้เพื่อติดตั้งโมดูล MSCommerce:</span><span class="sxs-lookup"><span data-stu-id="660f7-157">Run the following command to install the MSCommerce module:</span></span>

```powershell
Install-Module -name MSCommerce
```

### <a name="change-the-self-service-signup-policy"></a><span data-ttu-id="660f7-158">เปลี่ยนนโยบายการลงชื่อสมัครใช้บริการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="660f7-158">Change the self-service signup policy</span></span>

<span data-ttu-id="660f7-159">ใน PowerShell ให้เรียกใช้คำสั่งต่อไปนี้เพื่อเชื่อมต่อ:</span><span class="sxs-lookup"><span data-stu-id="660f7-159">In PowerShell, run the following command to connect:</span></span>

```powershell
Connect-MSCommerce
```

<span data-ttu-id="660f7-160">ป้อนข้อมูลประจำตัวผู้ดูแลระบบของคุณลงในกล่องโต้ตอบการลงชื่อเข้าใช้ จากนั้นดำเนินการรับรองความถูกต้องแบบสองปัจจัยที่อาจจำเป็นต้องทำ</span><span class="sxs-lookup"><span data-stu-id="660f7-160">Enter your admin credentials in the sign-in dialog, completing any two-factor authentication that may be needed.</span></span> <span data-ttu-id="660f7-161">หลังจากการตรวจสอบ หน้าต่าง PowerShell จะแสดงการเชื่อมต่อที่สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="660f7-161">After verification, the PowerShell window shows a successful connection.</span></span>

<span data-ttu-id="660f7-162">หากต้องการดูการตั้งค่าปัจจุบัน ให้เรียกใช้คำสั่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="660f7-162">To view the current setting, run the following command.</span></span> <span data-ttu-id="660f7-163">เพื่อป้องกันการตัดทอนข้อความ ผลลัพธ์จะถูกส่งไปยังรายการที่จัดรูปแบบไว้โดยใช้สวิตช์ "fl"</span><span class="sxs-lookup"><span data-stu-id="660f7-163">To prevent text from truncating, the output is piped to a formatted list by using the "fl" switch.</span></span>

```powershell
Get-MSCommercePolicy -PolicyId AllowSelfServicePurchase | fl
```

<span data-ttu-id="660f7-164">คุณสามารถปิดใช้งานการตั้งค่าที่อนุญาตให้มีการสั่งซื้อบริการของตนเองสำหรับแต่ละผลิตภัณฑ์โดยการแจ้ง **ProductId**</span><span class="sxs-lookup"><span data-stu-id="660f7-164">You can disable the setting that allows self-service purchase for an individual product by providing its **ProductId**.</span></span> <span data-ttu-id="660f7-165">เมื่อต้องการเปลี่ยนการตั้งค่าปัจจุบันสำหรับบริการของ Power BI ให้เรียกใช้คำสั่งนี้:</span><span class="sxs-lookup"><span data-stu-id="660f7-165">To change the current setting for the Power BI service, run this command:</span></span>

```powershell
Update-MSCommerceProductPolicy -PolicyId AllowSelfServicePurchase -ProductId CFQ7TTC0L3PB -Enabled $False
```

<span data-ttu-id="660f7-166">หลังจากเรียกใช้คำสั่งนี้ ระบบจะปิดการสั่งซื้อบริการด้วยตนเองของผู้ใช้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="660f7-166">After running this command, self-service purchase for Power BI is disabled for all users.</span></span> <span data-ttu-id="660f7-167">หากต้องการเปิดใช้งานอีกครั้ง ให้เรียกใช้คำสั่งนี้ใหม่แล้วตั้งค่าให้เป็น $true</span><span class="sxs-lookup"><span data-stu-id="660f7-167">To turn it back on, run this command again and set the value to $true.</span></span>

## <a name="next-steps"></a><span data-ttu-id="660f7-168">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="660f7-168">Next steps</span></span>

<span data-ttu-id="660f7-169">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสั่งซื้อบริการด้วยตนเองใน Power BI และส่วนอื่น ๆ ของ Power Platform ใหอ่านบทความเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="660f7-169">For more information about the self-service purchase in Power BI and the rest of the Power Platform, see these articles:</span></span>

- [<span data-ttu-id="660f7-170">คำถามที่พบบ่อยเกี่ยวกับการสั่งซื้อบริการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="660f7-170">Self-service purchase FAQ</span></span>](/microsoft-365/commerce/subscriptions/self-service-purchase-faq?view=o365-worldwide#admin-capabilities)
- [<span data-ttu-id="660f7-171">ใช้ AllowSelfServicePurchase สำหรับโมดูล MSCommerce PowerShell</span><span class="sxs-lookup"><span data-stu-id="660f7-171">Use AllowSelfServicePurchase for the MSCommerce PowerShell module</span></span>](/microsoft-365/commerce/subscriptions/allowselfservicepurchase-powershell?view=o365-worldwide)