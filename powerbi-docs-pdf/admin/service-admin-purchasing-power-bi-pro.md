---
title: ซื้อและมอบใบอนุญาตการใช้งาน Power BI Pro
description: เรียนรู้วิธีการซื้อและมอบสิทธิ์การใช้งานผู้ใช้ Power BI Pro ให้กับผู้ใช้ เพื่อที่พวกเขาสามารถเข้าถึงเนื้อหา และทำงานร่วมกันได้ในบริการของ Power BI
author: mihart
ms.author: mihart
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: how-to
ms.date: 04/08/2020
ms.custom: licensing support
LocalizationGroup: Administration
ms.openlocfilehash: 5845e56bdcb2257d67d541e35d26c9285a5e9319
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96408147"
---
# <a name="purchase-and-assign-power-bi-pro-user-licenses"></a><span data-ttu-id="56015-103">ซื้อและมอบสิทธิ์การใช้งานผู้ใช้ Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="56015-103">Purchase and assign Power BI Pro user licenses</span></span>

>[!IMPORTANT]
><span data-ttu-id="56015-104">บทความนี้เหมาะสำหรับผู้ดูแลระบบ!</span><span class="sxs-lookup"><span data-stu-id="56015-104">This article is for admins.</span></span> <span data-ttu-id="56015-105">คุณเป็นผู้ใช้พร้อมที่จะอัปเกรดเป็นสิทธิ์การใช้งาน Power BI Pro หรือไม่</span><span class="sxs-lookup"><span data-stu-id="56015-105">Are you a user ready to upgrade to a Power BI Pro license?</span></span> <span data-ttu-id="56015-106">ไปที่ [เริ่มต้นใช้งานด้วย Power BI Pro](https://go.microsoft.com/fwlink/?LinkId=2106428&clcid=0x409&cmpid=pbidocs-purchasing-power-bi-pro) โดยตรงเพื่อตั้งค่าบัญชีของคุณ</span><span class="sxs-lookup"><span data-stu-id="56015-106">Go directly to [Get started with Power BI Pro](https://go.microsoft.com/fwlink/?LinkId=2106428&clcid=0x409&cmpid=pbidocs-purchasing-power-bi-pro) to set up your account.</span></span>

<span data-ttu-id="56015-107">Power BI Pro เป็นสิทธิ์การใช้งานของผู้ใช้ส่วนบุคคล ที่อนุญาตให้ผู้ใช้อ่านและโต้ตอบกับรายงานและแดชบอร์ดที่ผู้ใช้อื่นเผยแพร่ไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="56015-107">Power BI Pro is an individual user license that lets users read and interact with reports and dashboards that others have published to the Power BI service.</span></span> <span data-ttu-id="56015-108">ผู้ใช้ที่มีสิทธิ์การใช้งานประเภทนี้สามารถแชร์เนื้อหาและทำงานร่วมกับผู้ใช้ Power BI Pro คนอื่นๆ ได้</span><span class="sxs-lookup"><span data-stu-id="56015-108">Users with this license type can share content and collaborate with other Power BI Pro users.</span></span> <span data-ttu-id="56015-109">เฉพาะผู้ใช้ที่มีสิทธิ์การใช้งาน Power BI Pro เท่านั้นที่สามารถเผยแพร่หรือแชร์เนื้อหากับผู้ใช้รายอื่นหรือนำเนื้อหาที่สร้างโดยผู้ใช้รายอื่นไปใช้ได้ ยกเว้นว่าเนื้อหานั้นโฮสต์อยู่ในความจุ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="56015-109">Only Power BI Pro users can publish or share content with other users or consume content that's created by others, unless a Power BI Premium capacity hosts that content.</span></span> <span data-ttu-id="56015-110">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับชนิดของสิทธิการใช้งานและการสมัครสมาชิกที่มีอยู่ ให้ดู [การให้สิทธิการใช้งาน Power BI ในองค์กรของคุณ](service-admin-licensing-organization.md)</span><span class="sxs-lookup"><span data-stu-id="56015-110">For more information about the available types of licenses and subscriptions, see [Power BI licensing in your organization](service-admin-licensing-organization.md).</span></span>

## <a name="purchase-power-bi-pro-user-licenses"></a><span data-ttu-id="56015-111">ซื้อสิทธิ์การใช้งานผู้ใช้ Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="56015-111">Purchase Power BI Pro user licenses</span></span>

<span data-ttu-id="56015-112">บทความนี้จะอธิบายวิธีซื้อสิทธิ์การใช้งานผู้ใช้ Power BI Pro ในศูนย์การจัดการ Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="56015-112">This article explains how to buy Power BI Pro user licenses in the Microsoft 365 admin center.</span></span> <span data-ttu-id="56015-113">หลังจากซื้อสิทธิ์ใช้งานแล้ว  คุณสามารถมอบสิทธิ์ให้ผู้ใช้ในศูนย์การจัดการ Microsoft 365 หรือในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="56015-113">After you buy licenses, you can assign them to users in either the Microsoft 365 admin center or the Azure portal.</span></span>

> [!NOTE]
> <span data-ttu-id="56015-114">ตั้งแต่วันที่14 มกราคม 2020 การซื้อแบบบริการตนเอง การสมัครสมาชิก และความสามารถในการจัดการสิทธิ์การใช้งานสำหรับผลิตภัณฑ์ Power Platform (Power BI, Power Apps และ Power Automate) จะมีให้บริการสำหรับลูกค้าระบบคลาวด์เชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="56015-114">Beginning January 14, 2020, self-service purchase, subscription, and license management capabilities for Power Platform products (Power BI, Power Apps, and Power Automate) are available for commercial cloud customers.</span></span> <span data-ttu-id="56015-115">สำหรับข้อมูลเพิ่มเติม โปรดดู [คำถามที่พบบ่อยเกี่ยวกับการซื้อแบบบริการตนเอง](/microsoft-365/commerce/subscriptions/self-service-purchase-faq)</span><span class="sxs-lookup"><span data-stu-id="56015-115">For more information, see [Self-service purchase FAQ](/microsoft-365/commerce/subscriptions/self-service-purchase-faq).</span></span> <span data-ttu-id="56015-116">หากต้องการเปิดใช้งานหรือปิดใช้งานความสามารถในการซื้อแบบบริการตนเอง ให้ดู [เปิดใช้งานหรือปิดใช้งานการลงทะเบียนและการซื้อแบบบริการตนเอง](./service-admin-disable-self-service.md)</span><span class="sxs-lookup"><span data-stu-id="56015-116">To enable or disable self-service purchasing capabilities, see [Enable or disable self-service sign-up and purchasing](./service-admin-disable-self-service.md).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="56015-117">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="56015-117">Prerequisites</span></span>

<span data-ttu-id="56015-118">หากต้องการซื้อและมอบสิทธิ์ใช้งานในศูนย์การจัดการ Microsoft 365 คุณต้องเป็นสมาชิกที่มีบทบาทเป็น [ผู้ดูแลระบบส่วนกลางหรือผู้ดูแลระบบสำหรับการเรียกเก็บเงิน](https://support.office.com/article/about-office-365-admin-roles-da585eea-f576-4f55-a1e0-87090b6aaa9d) ใน Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="56015-118">To purchase and assign licenses in the Microsoft 365 admin center, you must be a member of the [global administrator or Billing administrator](https://support.office.com/article/about-office-365-admin-roles-da585eea-f576-4f55-a1e0-87090b6aaa9d) role in Microsoft 365.</span></span>

<span data-ttu-id="56015-119">หากต้องการมอบสิทธิ์การใช้งานในพอร์ทัล Azure คุณต้องเป็นเจ้าของการสมัครใช้งาน Azure ที่ Power BI ใช้สำหรับการค้นหา Active Directory</span><span class="sxs-lookup"><span data-stu-id="56015-119">To assign licenses in the Azure portal, you must be an owner of the Azure subscription that Power BI uses for Azure Active Directory lookups.</span></span>

### <a name="purchase-licenses-in-microsoft-365"></a><span data-ttu-id="56015-120">ซื้อสิทธิ์การใช้งานใน Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="56015-120">Purchase licenses in Microsoft 365</span></span>

> [!NOTE]
> <span data-ttu-id="56015-121">หากคุณมักจะซื้อสิทธิการใช้งานผ่านข้อตกลง Volume Licensing เช่น Enterprise Agreement และต้องการรับใบแจ้งหนี้แทนการซื้อด้วยบัตรเครดิตหรือบัญชีธนาคาร คุณต้องส่งคำสั่งซื้อที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="56015-121">If you usually purchase licenses through a volume licensing agreement, such as an Enterprise Agreement, and want to receive an invoice instead of purchasing with a credit card or bank account, you need to submit the order differently.</span></span> <span data-ttu-id="56015-122">ทำงานกับผู้จำหน่าย Microsoft ของคุณหรือผ่านศูนย์บริการสิทธิ์การใช้งาน Volume เพื่อเพิ่มหรือเอาสิทธิการใช้งานออก</span><span class="sxs-lookup"><span data-stu-id="56015-122">Work with your Microsoft Reseller or go through the Volume Licensing Service Center to add or remove licenses.</span></span> <span data-ttu-id="56015-123">สำหรับข้อมูลเพิ่มเติม โปรดดู [จัดการสิทธิ์การใช้งานการสมัครใช้งาน](/microsoft-365/commerce/licenses/buy-licenses?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="56015-123">For more information, see [Manage subscription licenses](/microsoft-365/commerce/licenses/buy-licenses?view=o365-worldwide).</span></span>

<span data-ttu-id="56015-124">ทำตามขั้นตอนเหล่านี้เพื่อซื้อสิทธิ์การใช้งาน Power BI Pro ในศูนย์การจัดการ Microsoft 365:</span><span class="sxs-lookup"><span data-stu-id="56015-124">Follow these steps to purchase Power BI Pro licenses in the Microsoft 365 admin center:</span></span>

1. <span data-ttu-id="56015-125">ลงชื่อเข้าใช้ [ศูนย์การจัดการ Microsoft 365](https://admin.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="56015-125">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>

2. <span data-ttu-id="56015-126">บนเมนูการนำทาง เลือก **การเรียกเก็บเงิน** > **การซื้อบริการ**</span><span class="sxs-lookup"><span data-stu-id="56015-126">On the navigation menu, select **Billing** > **Purchase services**.</span></span>

3. <span data-ttu-id="56015-127">ค้นหาหรือเลื่อนเพื่อค้นหาการสมัครใช้งานที่คุณต้องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="56015-127">Search or scroll to find the subscription you want to buy.</span></span> <span data-ttu-id="56015-128">คุณจะพบ **Power BI** ภายใต้ **ประเภทอื่นๆ ที่คุณอาจสนใจ**  ใกล้กับด้านล่างของหน้า</span><span class="sxs-lookup"><span data-stu-id="56015-128">You'll find **Power BI** under **Other categories that might interest you** near the bottom of the page.</span></span> <span data-ttu-id="56015-129">เลือกลิงก์เพื่อดูการสมัครใช้งาน Power BI ที่มีให้สำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="56015-129">Select the link to view the Power BI subscriptions available to your organization.</span></span>

4. <span data-ttu-id="56015-130">เลือก **Power BI Pro**</span><span class="sxs-lookup"><span data-stu-id="56015-130">Select **Power BI Pro**.</span></span>

5. <span data-ttu-id="56015-131">บนหน้า **การซื้อบริการ** เลือก **ซื้อ**</span><span class="sxs-lookup"><span data-stu-id="56015-131">On the **Purchase services** page, select **Buy**.</span></span>

6. <span data-ttu-id="56015-132">เลือก **ชำระเงินรายเดือน** หรือ **ชำระเงินสำหรับทั้งปี** ตามลักษณะการเรียกเก็บเงินที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="56015-132">Choose **Pay monthly** or **Pay for a full year**, according to how you want to pay.</span></span>

7. <span data-ttu-id="56015-133">ในส่วน **คุณต้องการจำนวนผู้ใช้กี่ราย** ให้กรอกจำนวนสิทธิ์การเข้าถึงที่ต้องการซื้อ จากนั้นเลือก **ชำระเงินตอนนี้** เพื่อเสร็จสิ้นการทำธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="56015-133">Under **How many users do you want?** enter the number of licenses to buy, then select **Check out now** to complete the transaction.</span></span>

8. <span data-ttu-id="56015-134">หากต้องการตรวจสอบการซื้อของคุณ ให้ไปที่ **การเรียกเก็บเงิน** > **ผลิตภัณฑ์และบริการ** และค้นหา **Power BI Pro**</span><span class="sxs-lookup"><span data-stu-id="56015-134">To verify your purchase, go to **Billing** > **Products & services** and look for  **Power BI Pro**.</span></span>

9. <span data-ttu-id="56015-135">หากต้องการเพิ่มสิทธิ์การใช้งานเพิ่มในภายหลัง ให้ค้นหา **Power BI Pro** บนหน้า **ผลิตภัณฑ์และบริการ** จากนั้นเลือก **เพิ่ม/ลบสิทธิ์การใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="56015-135">To add more licenses later, locate **Power BI Pro** on the **Products & services** page, and then select **Add/Remove licenses**.</span></span>


## <a name="assign-licenses-in-the-microsoft-365-admin-center"></a><span data-ttu-id="56015-136">มอบสิทธิ์การใช้งานในศูนย์การจัดการ Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="56015-136">Assign licenses in the Microsoft 365 admin center</span></span>

<span data-ttu-id="56015-137">สำหรับข้อมูลเกี่ยวกับวิธีการกำหนดสิทธิ์การใช้งานในศูนย์การจัดการ Microsoft 365 ให้ดู [กำหนดสิทธิ์การใช้งานให้ผู้ใช้](/office365/admin/manage/assign-licenses-to-users)</span><span class="sxs-lookup"><span data-stu-id="56015-137">For information about assigning licenses in the Microsoft 365 admin center, see [Assign licenses to users](/office365/admin/manage/assign-licenses-to-users).</span></span>

<span data-ttu-id="56015-138">สำหรับผู้ใช้ที่เป็นผู้เยี่ยมชม ให้ดู [กำหนดสิทธิ์การใช้งานให้ผู้ใช้ในหน้าสิทธิการใช้งาน](/office365/admin/manage/assign-licenses-to-users#assign-licenses-to-users-on-the-licenses-page)</span><span class="sxs-lookup"><span data-stu-id="56015-138">For guest users, see [Assign licenses to users on the Licenses page](/office365/admin/manage/assign-licenses-to-users#assign-licenses-to-users-on-the-licenses-page).</span></span> <span data-ttu-id="56015-139">ก่อนที่จะกำหนดสิทธิ์การใช้งาน Pro ให้แก่ผู้ใช้ที่เป็นผู้เยี่ยมชม ให้ติดต่อเจ้าหน้าที่บัญชี Microsoft ของคุณเพื่อตรวจสอบให้แน่ใจว่าคุณได้ปฏิบัติตามข้อกำหนดของข้อตกลงของคุณกับ Microsoft</span><span class="sxs-lookup"><span data-stu-id="56015-139">Before assigning Pro licenses to guest users, contact your Microsoft account representative to make sure you're in compliance with the terms of your agreement with Microsoft.</span></span>

## <a name="assign-licenses-in-the-azure-portal"></a><span data-ttu-id="56015-140">มอบสิทธิ์การใช้งานในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="56015-140">Assign licenses in the Azure portal</span></span>

<span data-ttu-id="56015-141">ทำตามขั้นตอนต่อไปนี้เพื่อกำหนดสิทธิ์การใช้งาน Power BI Pro ให้กับบัญชีผู้ใช้แต่ละราย:</span><span class="sxs-lookup"><span data-stu-id="56015-141">Follow these steps to assign Power BI Pro licenses to individual user accounts:</span></span>

1. <span data-ttu-id="56015-142">ลงชื่อเข้าใช้ไปยัง [พอร์ทัล Azure](https://portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="56015-142">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>

2. <span data-ttu-id="56015-143">ค้นหาและเลือก **Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="56015-143">Search for and select **Azure Active Directory**.</span></span>

3. <span data-ttu-id="56015-144">ในส่วน **จัดการ** บนเมนูแหล่งข้อมูล **Azure Active Directory** **เลือกสิทธิ์การใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="56015-144">Under **Manage** on the **Azure Active Directory** resource menu, select **Licenses**.</span></span>

4. <span data-ttu-id="56015-145">เลือก **ผลิตภัณฑ์ทั้งหมด** จากเมนูแหล่งข้อมูล  **สิทธิ์การใช้งาน - ภาพรวม** จากนั้นเลือก **Power BI Pro** เพื่อแสดงรายการของผู้ใช้ที่มีสิทธิ์ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="56015-145">Select **All products** from the **Licenses - Overview** resource menu, then select **Power BI Pro** to display the list of licensed users.</span></span>

5. <span data-ttu-id="56015-146">จากแถบคำสั่ง เลือก **+มอบสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="56015-146">From the command bar, select **+ Assign**.</span></span> <span data-ttu-id="56015-147">บนหน้า **มอบสิทธิ์การใช้งาน** อันดับแรก ให้เลือกผู้ใช้ จากนั้นเลือก **ตัวเลือกการมอบสิทธิ์** เพื่อเปิดสิทธิ์การใช้งาน Power BI Pro สำหรับบัญชีผู้ใช้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="56015-147">On the **Assign license** page, first choose a user, then select **Assignment options** to turn on a Power BI Pro license for the selected user account.</span></span>

## <a name="next-steps"></a><span data-ttu-id="56015-148">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="56015-148">Next steps</span></span>

- [<span data-ttu-id="56015-149">สิทธิ์การใช้งาน Power BI สำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="56015-149">Power BI licensing in your organization</span></span>](service-admin-licensing-organization.md)

 - [<span data-ttu-id="56015-150">หาผู้ใช้ Power BI ที่ได้ลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="56015-150">Find Power BI users who have signed in</span></span>](service-admin-access-usage.md)

 - [<span data-ttu-id="56015-151">ลงทะเบียนใช้งาน Power BI เป็นรายบุคคล</span><span class="sxs-lookup"><span data-stu-id="56015-151">Sign up for Power BI as an individual</span></span>](../fundamentals/service-self-service-signup-for-power-bi.md)

<span data-ttu-id="56015-152">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="56015-152">More questions?</span></span> [<span data-ttu-id="56015-153">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="56015-153">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)