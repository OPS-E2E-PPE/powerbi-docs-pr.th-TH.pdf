---
title: วิธีการซื้อ Power BI Premium
description: เรียนรู้วิธีการซื้อ Power BI Premium และเปิดใช้งานการเข้าถึงเนื้อหาให้ทั้งองค์กรของคุณ
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-premium
ms.topic: how-to
ms.date: 11/11/2020
LocalizationGroup: Premium
ms.openlocfilehash: f74d667cd95f1fd34d97c3942ac6ab44d083d4c3
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96408400"
---
# <a name="how-to-purchase-power-bi-premium"></a><span data-ttu-id="26187-103">วิธีการซื้อ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="26187-103">How to purchase Power BI Premium</span></span>

<span data-ttu-id="26187-104">บทความนี้อธิบายวิธีการซื้อความจุของ Power BI Premium สำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="26187-104">This article describes how to purchase Power BI Premium capacity for your organization.</span></span> <span data-ttu-id="26187-105">บทความนี้ครอบคลุมสถานการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="26187-105">The article covers the following scenario:</span></span>

- <span data-ttu-id="26187-106">การใช้ P SKU สำหรับสถานการณ์การผลิตทั่วไป</span><span class="sxs-lookup"><span data-stu-id="26187-106">Using P SKUs for typical production scenarios.</span></span> <span data-ttu-id="26187-107">P SKU กำหนดให้มีข้อผูกมัดรายเดือนหรือรายปี และจะเรียกเก็บเงินเป็นรายเดือน</span><span class="sxs-lookup"><span data-stu-id="26187-107">P SKUs require a monthly or yearly commitment, and are billed monthly.</span></span>

<span data-ttu-id="26187-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI Premium ดูที่ [Power BI Premium คืออะไร](service-premium-what-is.md)</span><span class="sxs-lookup"><span data-stu-id="26187-108">For more information about Power BI Premium, see [What is Power BI Premium?](service-premium-what-is.md).</span></span> <span data-ttu-id="26187-109">สำหรับข้อมูลการกำหนดราคาและการวางแผนในปัจจุบัน ดู [หน้าการกำหนดราคา Power BI](https://powerbi.microsoft.com/pricing/) และ [เครื่องคิดเลข Power BI Premium](https://powerbi.microsoft.com/calculator/)</span><span class="sxs-lookup"><span data-stu-id="26187-109">For current pricing and planning information, see the [Power BI pricing page](https://powerbi.microsoft.com/pricing/) and the [Power BI Premium calculator](https://powerbi.microsoft.com/calculator/).</span></span> <span data-ttu-id="26187-110">ผู้เขียนเนื้อหาจะยังคงจำเป็นต้องมี [สิทธิ์การใช้งาน Power BI Pro](service-admin-purchasing-power-bi-pro.md) แม้ว่าองค์กรของคุณจะใช้ Power BI Premium ก็ตาม</span><span class="sxs-lookup"><span data-stu-id="26187-110">Content creators still need a [Power BI Pro license](service-admin-purchasing-power-bi-pro.md), even if your organization uses Power BI Premium.</span></span> <span data-ttu-id="26187-111">ตรวจสอบให้แน่ใจว่าคุณซื้อสิทธิ์การใช้งาน Power BI Pro อย่างน้อยหนึ่งใบสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="26187-111">Ensure you purchase at least one Power BI Pro license for your organization.</span></span> <span data-ttu-id="26187-112">เมื่อใช้ A SKU _ผู้ใช้ทั้งหมด_ ที่ใช้เนื้อหายังจำเป็นต้องมีสิทธิการใช้งาน Pro</span><span class="sxs-lookup"><span data-stu-id="26187-112">With A SKUs, _all users_ who consume content also require Pro licenses.</span></span>

> [!NOTE]
> <span data-ttu-id="26187-113">ถ้าการสมัครใช้งานระดับ Premium หมดอายุ คุณมีเวลา 30 วันของการเข้าถึงความจุแบบเต็มของคุณ</span><span class="sxs-lookup"><span data-stu-id="26187-113">If a Premium subscription expires, you have 30 days of full access to your capacity.</span></span> <span data-ttu-id="26187-114">หลังจากนั้น เนื้อหาของคุณจะเปลี่ยนเป็นความจุที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="26187-114">After that, your content reverts to a shared capacity.</span></span> <span data-ttu-id="26187-115">แบบจำลองที่มีความจุมากกว่า 1 GB ไม่ได้รับการรับรองในความจุที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="26187-115">Models that are greater than 1 GB are not supported in shared capacity.</span></span>

> [!NOTE]
> <span data-ttu-id="26187-116">Power BI Premium เพิ่งเปิดตัว Premium เวอร์ชันใหม่ชื่อ **Premium Gen2** ซึ่งกำลังอยู่ในช่วงการแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="26187-116">Power BI Premium recently released a new version of Premium, called **Premium Gen2**, which is currently in preview.</span></span> <span data-ttu-id="26187-117">Premium Gen2 จะทำให้การจัดการความจุระดับพรีเมียมง่ายขึ้นและลดค่าใช้จ่ายในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="26187-117">Premium Gen2 will simplify the management of Premium capacities, and reduce management overhead.</span></span> <span data-ttu-id="26187-118">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Power BI Premium Generation 2 (ตัวอย่าง)](service-premium-what-is.md#power-bi-premium-generation-2-preview)</span><span class="sxs-lookup"><span data-stu-id="26187-118">For more information, see [Power BI Premium Generation 2 (preview)](service-premium-what-is.md#power-bi-premium-generation-2-preview).</span></span>

## <a name="purchase-p-skus-for-typical-production-scenarios"></a><span data-ttu-id="26187-119">ซื้อ P SKU สำหรับสถานการณ์การผลิตทั่วไป</span><span class="sxs-lookup"><span data-stu-id="26187-119">Purchase P SKUs for typical production scenarios</span></span>

<span data-ttu-id="26187-120">คุณสามารถสร้างผู้เช่าใหม่ด้วย Power BI Premium ที่กำหนดค่า SKU หรือคุณสามารถซื้อความจุ Power BI Premium สำหรับองค์กรที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="26187-120">You can create a new tenant with a Power BI Premium P1 SKU configured, or you can purchase a Power BI Premium capacity for an existing organization.</span></span> <span data-ttu-id="26187-121">ในทั้งสองกรณี คุณสามารถเพิ่มความจุได้หากคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="26187-121">In both cases, you can then add capacity if you need it.</span></span>

### <a name="create-a-new-tenant-with-power-bi-premium-p1"></a><span data-ttu-id="26187-122">สร้างลูกค้าใหม่ด้วย Power BI Premium P1</span><span class="sxs-lookup"><span data-stu-id="26187-122">Create a new tenant with Power BI Premium P1</span></span>

<span data-ttu-id="26187-123">ถ้าคุณไม่มีผู้เช่าและต้องการสร้างหนึ่งรายการ คุณสามารถซื้อ Power BI Premium ได้ในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="26187-123">If you don't have an existing tenant and want to create one, you can purchase Power BI Premium at the same time.</span></span> <span data-ttu-id="26187-124">ลิงก์ต่อไปนี้จะนำคุณไปสู่กระบวนการสร้างผู้เช่ารายใหม่และช่วยให้คุณสามารถซื้อ Power BI Premium: [ข้อเสนอ Power BI Premium P1](https://signup.microsoft.com/Signup?OfferId=b3ec5615-cc11-48de-967d-8d79f7cb0af1)</span><span class="sxs-lookup"><span data-stu-id="26187-124">The following link walks you through the process of creating a new tenant and enables you to purchase Power BI Premium: [Power BI Premium P1 offer](https://signup.microsoft.com/Signup?OfferId=b3ec5615-cc11-48de-967d-8d79f7cb0af1).</span></span> <span data-ttu-id="26187-125">เมื่อคุณสร้างผู้เช่า คุณจะได้รับมอบหมายให้ทำหน้าที่เป็นผู้ดูแลระบบส่วนกลางของ Microsoft 365 โดยอัตโนมัติสำหรับผู้เช่ารายนั้น</span><span class="sxs-lookup"><span data-stu-id="26187-125">When you create your tenant, you will automatically be assigned to the Microsoft 365 Global Administrator role for that tenant.</span></span>

<span data-ttu-id="26187-126">หลังจากที่คุณซื้อความจุ ให้เรียนรู้วิธีการ [จัดการความจุ](service-admin-premium-manage.md#manage-capacity) และ [มอบหมายพื้นที่ทำงาน](service-admin-premium-manage.md#assign-a-workspace-to-a-capacity) ให้กับความจุ</span><span class="sxs-lookup"><span data-stu-id="26187-126">After you purchase capacity, learn how to [manage capacities](service-admin-premium-manage.md#manage-capacity) and [assign workspaces](service-admin-premium-manage.md#assign-a-workspace-to-a-capacity) to a capacity.</span></span>

### <a name="purchase-a-power-bi-premium-capacity-for-an-existing-organization"></a><span data-ttu-id="26187-127">ซื้อความจุ Power BI Premium สำหรับองค์กรที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="26187-127">Purchase a Power BI Premium capacity for an existing organization</span></span>

<span data-ttu-id="26187-128">ถ้าคุณมีองค์กรที่มีอยู่แล้ว (ผู้เช่า) คุณต้องอยู่ในบทบาทผู้ดูแลระบบส่วนกลางของ Microsoft 365 หรือบทบาทของผู้ดูแลระบบการเรียกเก็บเงินเพื่อซื้อการสมัครรับข้อมูลและสิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="26187-128">If you have an existing organization (tenant), you must be in the Microsoft 365 Global Administrator role or Billing Administrator role to purchase subscriptions and licenses.</span></span> <span data-ttu-id="26187-129">สำหรับข้อมูลเพิ่มเติม ให้ดู[เกี่ยวกับบทบาทผู้ดูแลระบบ Microsoft 365](https://support.office.com/article/About-Office-365-admin-roles-da585eea-f576-4f55-a1e0-87090b6aaa9d)</span><span class="sxs-lookup"><span data-stu-id="26187-129">For more information, see [About Microsoft 365 admin roles](https://support.office.com/article/About-Office-365-admin-roles-da585eea-f576-4f55-a1e0-87090b6aaa9d).</span></span>

<span data-ttu-id="26187-130">เมื่อต้องการซื้อความจุระดับพรีเมี่ยม ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="26187-130">To purchase Premium capacity, follow these steps.</span></span>

1. <span data-ttu-id="26187-131">จากภายใน Power BI service เลือกตัวเลือกแอป Microsoft 365 จากนั้นเลือก **ผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="26187-131">From within the Power BI service, select the Microsoft 365 app picker then **Admin**.</span></span>

    ![ตัวเลือกแอป Microsoft 365](media/service-admin-premium-purchase/o365-app-picker.png)

    <span data-ttu-id="26187-133">อีกวิธีหนึ่งคือ คุณสามารถเรียกดูศูนย์การจัดการ Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="26187-133">Alternatively, you can browse to the Microsoft 365 admin center.</span></span>

1. <span data-ttu-id="26187-134">เลือก **การเรียกเก็บเงิน** > **ซื้อบริการ**</span><span class="sxs-lookup"><span data-stu-id="26187-134">Select **Billing** > **Purchase services**.</span></span>

1. <span data-ttu-id="26187-135">ภายใต้ **แผนอื่น ๆ** ค้นหาข้อเสนอของ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="26187-135">Under **Other plans**, look for Power BI Premium offerings.</span></span> <span data-ttu-id="26187-136">ซึ่งจะแสดงรายการเป็น P1 ผ่าน P3, EM3 และ P1 (แบบรายเดือน)</span><span class="sxs-lookup"><span data-stu-id="26187-136">This will list as P1 through P3, EM3 and P1 (month to month).</span></span>

1. <span data-ttu-id="26187-137">วางเคอร์เซอร์เหนือ จุดไข่ปลา ( **. . .** )แล้ว เลือก **ซื้อทันที**</span><span class="sxs-lookup"><span data-stu-id="26187-137">Hover over the ellipsis (**. . .**) and then select **Buy now**.</span></span>

    ![ซื้อเดี๋ยวนี้](media/service-admin-premium-purchase/premium-purchase.png)

1. <span data-ttu-id="26187-139">ทำตามขั้นตอนเพื่อทำการซื้อให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="26187-139">Follow the steps to complete the purchase.</span></span>

<span data-ttu-id="26187-140">หลังจากที่คุณเสร็จสิ้นการซื้อ **หน้าจอบริการการซื้อ** จะแสดงว่ารายการนั้นถูกซื้อและใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="26187-140">After you have completed the purchase, the **Purchase services** page shows that the item is purchased and active.</span></span>

![ซื้อ Power BI Premium](media/service-admin-premium-purchase/premium-purchased.png)

<span data-ttu-id="26187-142">หลังจากที่คุณซื้อความจุ ให้เรียนรู้วิธีการ [จัดการความจุ](service-admin-premium-manage.md#manage-capacity) และ [มอบหมายพื้นที่ทำงาน](service-admin-premium-manage.md#assign-a-workspace-to-a-capacity) ให้กับความจุ</span><span class="sxs-lookup"><span data-stu-id="26187-142">After you purchase capacity, learn how to [manage capacities](service-admin-premium-manage.md#manage-capacity) and [assign workspaces](service-admin-premium-manage.md#assign-a-workspace-to-a-capacity) to a capacity.</span></span>

### <a name="purchase-additional-capacities"></a><span data-ttu-id="26187-143">ซื้อความจุเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="26187-143">Purchase additional capacities</span></span>

<span data-ttu-id="26187-144">ขณะนี้คุณมีความจุแล้ว คุณสามารถเพิ่มความจุได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="26187-144">Now that you have a capacity, you can add more as your needs grow.</span></span> <span data-ttu-id="26187-145">คุณสามารถผสม Premium capacity SKUs (P1 ผ่าน P3) ภายในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="26187-145">You can use any combination of Premium capacity SKUs (P1 through P3) within your organization.</span></span> <span data-ttu-id="26187-146">SKU ที่ต่างกันมีความสามารถด้านทรัพยากรที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="26187-146">The different SKUs provide different resource capabilities.</span></span>

1. <span data-ttu-id="26187-147">ในศูนย์การจัดการ Microsoft 365 เลือก **การเรียกเก็บเงิน** > **ซื้อบริการ**</span><span class="sxs-lookup"><span data-stu-id="26187-147">In the Microsoft 365 admin center, select **Billing** > **Purchase services**.</span></span>

1. <span data-ttu-id="26187-148">ค้นหารายการ Power BI Premium ที่คุณต้องการซื้อหนึ่งภายใต้ **แผนอื่นๆ**</span><span class="sxs-lookup"><span data-stu-id="26187-148">Find the Power BI Premium item you want to purchase more of under **Other plans**.</span></span>

1. <span data-ttu-id="26187-149">วางเมาส์เหนือ **ตัวเลือกเพิ่มเติม** (...) แล้วเลือก **เปลี่ยนจำนวนสิทธิ์การใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="26187-149">Hover over **More options** (...) and then select **Change license quantity**.</span></span>

    ![เปลี่ยนจำนวนสิทธิ์การใช้งาน](media/service-admin-premium-purchase/premium-purchase-more.png)

1. <span data-ttu-id="26187-151">เปลี่ยนจำนวนของอินสแตนซ์ที่คุณต้องการสำหรับรายการนี้</span><span class="sxs-lookup"><span data-stu-id="26187-151">Change the number of instances that you want to have for this item.</span></span> <span data-ttu-id="26187-152">แล้ว เลือก **ส่ง** เมื่อทำเสร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="26187-152">Then select **Submit** when finished.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="26187-153">การเลือก **ส่ง** จะเรียกเก็บเงินจากบัตรเครดิตในไฟล์</span><span class="sxs-lookup"><span data-stu-id="26187-153">Selecting **Submit** charges the credit card on file.</span></span>

<span data-ttu-id="26187-154">หน้า **ซื้อบริการ** จะบ่งชี้ถึงจำนวนของอินสแตนซ์ที่คุณมี</span><span class="sxs-lookup"><span data-stu-id="26187-154">The **Purchase services** page will then indicate the number of instances you have.</span></span> <span data-ttu-id="26187-155">ภายในพอร์ทัลผู้ดูแล Power BI ภายใต้ **ตั้งค่าความจุ** แกน v ที่พร้อมใช้งานสะท้อนถึงความจุที่ซื้อใหม่</span><span class="sxs-lookup"><span data-stu-id="26187-155">Within the Power BI admin portal, under **Capacity settings**, the available v-cores reflects the new capacity purchased.</span></span>

![แกน v ใช้งานได้สำหรับความจุ Power BI Premium](media/service-admin-premium-purchase/premium-capacities.png)

### <a name="cancel-your-subscription"></a><span data-ttu-id="26187-157">ยกเลิกการสมัครใช้งาน</span><span class="sxs-lookup"><span data-stu-id="26187-157">Cancel your subscription</span></span>

<span data-ttu-id="26187-158">คุณสามารถยกเลิกการสมัครใช้งานจากภายในศูนย์การจัดการ Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="26187-158">You can cancel your subscription from within the Microsoft 365 admin center.</span></span> <span data-ttu-id="26187-159">เพื่อยกเลิกการสมัครใช้งาน Premium ให้ทำสิ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="26187-159">To cancel your Premium subscription, do the following.</span></span>

1. <span data-ttu-id="26187-160">ค้นหาศูนย์การจัดการ Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="26187-160">Browse to the Microsoft 365 admin center.</span></span>

1. <span data-ttu-id="26187-161">เลือก **การเรียกเก็บเงิน** > **การสมัครใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="26187-161">Select **Billing** > **Subscriptions**.</span></span>

1. <span data-ttu-id="26187-162">เลือกการสมัครใช้งาน Power BI Premium จากรายการ</span><span class="sxs-lookup"><span data-stu-id="26187-162">Select your Power BI Premium subscription from the list.</span></span>

1. <span data-ttu-id="26187-163">เลือก **การดำเนินการเพิ่มเติม** > **ยกเลิกการสมัครใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="26187-163">Select **More actions** > **Cancel subscription**.</span></span>

1. <span data-ttu-id="26187-164">หน้า **ยกเลิกการสมัครใช้งาน** จะระบุว่าที่คุณเป็นผู้รับผิดชอบสำหรับ [ค่าธรรมเนียมการหยุดใช้งานก่อน](https://support.office.com/article/early-termination-fees-6487d4de-401a-466f-8bc3-c0beb5cc40d3)หรือไม่</span><span class="sxs-lookup"><span data-stu-id="26187-164">The **Cancel subscription** page will indicate whether or not you are responsible for an [early termination fee](https://support.office.com/article/early-termination-fees-6487d4de-401a-466f-8bc3-c0beb5cc40d3).</span></span> <span data-ttu-id="26187-165">เพจนี้จะยังแจ้งให้คุณทราบเมื่อข้อมูลจะถูกลบเพื่อสมัครใช้งาน</span><span class="sxs-lookup"><span data-stu-id="26187-165">This page will also let you know when the data will be deleted for the subscription.</span></span>

1. <span data-ttu-id="26187-166">อ่านผ่านข้อมูล และถ้าคุณต้องการดำเนินการ ให้เลือก **ยกเลิกการสมัครใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="26187-166">Read through the information, and if you want to proceed, select **Cancel subscription**.</span></span>

#### <a name="when-canceling-or-your-license-expires"></a><span data-ttu-id="26187-167">เมื่อยกเลิกหรือสิทธิ์การใช้งานของคุณหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="26187-167">When canceling or your license expires</span></span>

<span data-ttu-id="26187-168">เมื่อยกเลิกการสมัครใช้งานแบบพรีเมียม หรือสิทธิ์การใช้งานความจุของคุณหมดอายุ คุณยังสามารถเข้าถึงความจุพรีเมียมของคุณได้เป็นระยะเวลา 30 วันนับจากวันที่ยกเลิกหรือหมดอายุสิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="26187-168">When you cancel your Premium subscription, or your capacity license expires, you can continue to access your Premium capacities for a period of 30 days from the date of cancellation or license expiration.</span></span> <span data-ttu-id="26187-169">หลังจาก 30 วัน คุณจะไม่สามารถเข้าถึงความจุพรีเมียมหรือพื้นที่ทำงานภายในความจุดังกล่าวได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="26187-169">After 30 days, you will no longer be able to access your Premium capacities or workspaces in them.</span></span>

## <a name="purchase-a-skus-for-testing-and-other-scenarios"></a><span data-ttu-id="26187-170">ซื้อ A SKU สำหรับการทดสอบและสถานการณ์อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="26187-170">Purchase A SKUs for testing and other scenarios</span></span>

<span data-ttu-id="26187-171">คุณยังสามารถซื้อ SKU สำหรับการทดสอบและสถานการณ์อื่น ๆ ซึ่งให้ความจุแบบ Premium เป็นรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="26187-171">You can also purchase A SKUs for testing and other scenarios, which provides Premium capacity on an hourly basis.</span></span> <span data-ttu-id="26187-172">สำหรับข้อมูลและขั้นตอนเพิ่มเติม โปรดดู[ซื้อ Power BI Premium สำหรับการทดสอบ](service-admin-premium-testing.md)</span><span class="sxs-lookup"><span data-stu-id="26187-172">For more information and steps, see [Purchase Power BI Premium for testing](service-admin-premium-testing.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="26187-173">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="26187-173">Next steps</span></span>

<span data-ttu-id="26187-174">[กำหนดค่าและจัดการความจุใน Power BI Premium](service-admin-premium-manage.md)</span><span class="sxs-lookup"><span data-stu-id="26187-174">[Configure and manage capacities in Power BI Premium](service-admin-premium-manage.md)</span></span>\
<span data-ttu-id="26187-175">[หน้าการกำหนดราคา Power BI](https://powerbi.microsoft.com/pricing/)</span><span class="sxs-lookup"><span data-stu-id="26187-175">[Power BI pricing page](https://powerbi.microsoft.com/pricing/)</span></span>\
<span data-ttu-id="26187-176">[เครื่องคิดเลข Power BI Premium](https://powerbi.microsoft.com/calculator/)</span><span class="sxs-lookup"><span data-stu-id="26187-176">[Power BI Premium calculator](https://powerbi.microsoft.com/calculator/)</span></span>\
<span data-ttu-id="26187-177">[คำถามที่ถามบ่อยสำหรับ Power BI Premium](service-premium-faq.md)</span><span class="sxs-lookup"><span data-stu-id="26187-177">[Power BI Premium FAQ](service-premium-faq.md)</span></span>\
[<span data-ttu-id="26187-178">เอกสารทางเทคนิคเรื่องการวางแผนการใช้ Power BI สำหรับองค์กร</span><span class="sxs-lookup"><span data-stu-id="26187-178">Planning a Power BI Enterprise Deployment whitepaper</span></span>](https://aka.ms/pbienterprisedeploy)

<span data-ttu-id="26187-179">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="26187-179">More questions?</span></span> [<span data-ttu-id="26187-180">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="26187-180">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)

<span data-ttu-id="26187-181">Power BI ได้แนะนำ Power BI Premium Gen2 เข้ามาใช้งานเป็นข้อเสนอการแสดงตัวอย่าง ซึ่งปรับปรุงประสบการณ์การใช้งาน Power BI Premium ด้วยการปรับปรุงในสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="26187-181">Power BI has introduced Power BI Premium Gen2 as a preview offering, which improves the Power BI Premium experience with improvements in the following:</span></span>
* <span data-ttu-id="26187-182">ประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="26187-182">Performance</span></span>
* <span data-ttu-id="26187-183">สิทธิการใช้งานต่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="26187-183">Per-user licensing</span></span>
* <span data-ttu-id="26187-184">ขนาดใหญ่ขึ้น</span><span class="sxs-lookup"><span data-stu-id="26187-184">Greater scale</span></span>
* <span data-ttu-id="26187-185">เมตริกที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="26187-185">Improved metrics</span></span>
* <span data-ttu-id="26187-186">การปรับขนาดอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="26187-186">Autoscaling</span></span>
* <span data-ttu-id="26187-187">ลดค่าใช้จ่ายในการจัดการ</span><span class="sxs-lookup"><span data-stu-id="26187-187">Reduced management overhead</span></span>

<span data-ttu-id="26187-188">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI Premium Gen2 โปรดดูที่ [Power BI Premium Generation 2 (ตัวอย่าง)](service-premium-what-is.md#power-bi-premium-generation-2-preview)</span><span class="sxs-lookup"><span data-stu-id="26187-188">For more information about Power BI Premium Gen2, see [Power BI Premium Generation 2 (preview)](service-premium-what-is.md#power-bi-premium-generation-2-preview).</span></span>