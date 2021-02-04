---
title: Purchase Power BI Premium สำหรับการทดสอบ
description: เรียนรู้วิธีที่คุณสามารถซื้อ Power BI Premium สำหรับการทดสอบและวัตถุประสงค์อื่น ๆ
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-premium
ms.topic: how-to
ms.date: 11/11/2020
LocalizationGroup: Premium
ms.openlocfilehash: 597ae36aaddcbabbedcd084061410dab9334a702
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413598"
---
# <a name="purchase-power-bi-premium-for-testing"></a><span data-ttu-id="c7a59-103">Purchase Power BI Premium สำหรับการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="c7a59-103">Purchase Power BI Premium for testing</span></span>

<span data-ttu-id="c7a59-104">บทความนี้อธิบายถึงวิธีการซื้อ Power BI Premium A SKU สำหรับสถานการณ์การทดสอบ และกรณีที่คุณไม่มีสิทธิ์ที่จำเป็นในการซื้อ P SKU (บทบาทผู้ดูแลระบบส่วนกลาง Microsoft 365 หรือบทบาทผู้ดูแลระบบการเรียกเก็บเงิน)</span><span class="sxs-lookup"><span data-stu-id="c7a59-104">This article describes how to purchase Power BI Premium A SKUs for testing scenarios, and for cases where you don't have the permissions necessary to purchase P SKUs (Microsoft 365 Global Administrator role or Billing Administrator role).</span></span> <span data-ttu-id="c7a59-105">A SKU ไม่จำเป็นต้องมีข้อผูกมัดเวลา และเรียกเก็บเงินเป็นรายชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="c7a59-105">A SKUs require no time commitment, and are billed hourly.</span></span> <span data-ttu-id="c7a59-106">คุณซื้อ A SKU ใน [พอร์ทัล Azure](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="c7a59-106">You purchase A SKUs in the [Azure portal](https://portal.azure.com).</span></span>

<span data-ttu-id="c7a59-107">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI Premium ดูที่ [Power BI Premium คืออะไร](service-premium-what-is.md)</span><span class="sxs-lookup"><span data-stu-id="c7a59-107">For more information about Power BI Premium, see [What is Power BI Premium?](service-premium-what-is.md).</span></span> <span data-ttu-id="c7a59-108">สำหรับข้อมูลการกำหนดราคาและการวางแผนในปัจจุบัน ดู [หน้าการกำหนดราคา Power BI](https://powerbi.microsoft.com/pricing/) และ [เครื่องคิดเลข Power BI Premium](https://powerbi.microsoft.com/calculator/)</span><span class="sxs-lookup"><span data-stu-id="c7a59-108">For current pricing and planning information, see the [Power BI pricing page](https://powerbi.microsoft.com/pricing/) and the [Power BI Premium calculator](https://powerbi.microsoft.com/calculator/).</span></span> <span data-ttu-id="c7a59-109">ผู้เขียนเนื้อหาจะยังคงจำเป็นต้องมี [สิทธิ์การใช้งาน Power BI Pro](service-admin-purchasing-power-bi-pro.md) แม้ว่าองค์กรของคุณจะใช้ Power BI Premium ก็ตาม</span><span class="sxs-lookup"><span data-stu-id="c7a59-109">Content creators still need a [Power BI Pro license](service-admin-purchasing-power-bi-pro.md), even if your organization uses Power BI Premium.</span></span> <span data-ttu-id="c7a59-110">ตรวจสอบให้แน่ใจว่าคุณซื้อสิทธิ์การใช้งาน Power BI Pro อย่างน้อยหนึ่งใบสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7a59-110">Ensure you purchase at least one Power BI Pro license for your organization.</span></span> <span data-ttu-id="c7a59-111">เมื่อใช้ A SKU _ผู้ใช้ทั้งหมด_ ที่ใช้เนื้อหายังจำเป็นต้องมีสิทธิการใช้งาน Pro</span><span class="sxs-lookup"><span data-stu-id="c7a59-111">With A SKUs, _all users_ who consume content also require Pro licenses.</span></span>

> [!NOTE]
> <span data-ttu-id="c7a59-112">ถ้าการสมัครใช้งานระดับ Premium หมดอายุ คุณมีเวลา 30 วันของการเข้าถึงความจุแบบเต็มของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7a59-112">If a Premium subscription expires, you have 30 days of full access to your capacity.</span></span> <span data-ttu-id="c7a59-113">หลังจากนั้น เนื้อหาของคุณจะเปลี่ยนเป็นความจุที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="c7a59-113">After that, your content reverts to a shared capacity.</span></span> <span data-ttu-id="c7a59-114">แบบจำลองที่มีความจุมากกว่า 1 GB ไม่ได้รับการรับรองในความจุที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="c7a59-114">Models that are greater than 1 GB are not supported in shared capacity.</span></span>

## <a name="purchase-a-skus-for-testing-and-other-scenarios"></a><span data-ttu-id="c7a59-115">ซื้อ A SKU สำหรับการทดสอบและสถานการณ์อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="c7a59-115">Purchase A SKUs for testing and other scenarios</span></span>

<span data-ttu-id="c7a59-116">มีการทำให้ A SKU พร้อมใช้งานผ่านทางบริการ Azure Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="c7a59-116">A SKUs are made available through the Azure Power BI Embedded service.</span></span> <span data-ttu-id="c7a59-117">คุณสามารถใช้ A SKU ในวิธีการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c7a59-117">You can use A SKUs in the following ways:</span></span>

- <span data-ttu-id="c7a59-118">เปิดใช้งานการฝังของ Power BI ในแอปพลิเคชันของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="c7a59-118">Enable embedding of Power BI in third party applications.</span></span> <span data-ttu-id="c7a59-119">สำหรับข้อมูลเพิ่มเติม ให้ดู [Power BI Embedded](../developer/embedded/azure-pbie-what-is-power-bi-embedded.md)</span><span class="sxs-lookup"><span data-stu-id="c7a59-119">For more information, see [Power BI Embedded](../developer/embedded/azure-pbie-what-is-power-bi-embedded.md).</span></span>

- <span data-ttu-id="c7a59-120">ทดสอบฟังก์ชัน Premium ก่อนที่คุณจะซื้อ P SKU</span><span class="sxs-lookup"><span data-stu-id="c7a59-120">Test Premium functionality before you buy a P SKU.</span></span>

- <span data-ttu-id="c7a59-121">สร้างสภาพแวดล้อมการพัฒนาและการทดสอบควบคู่ไปกับสภาพแวดล้อมการผลิตที่ใช้ P SKU</span><span class="sxs-lookup"><span data-stu-id="c7a59-121">Create development and test environments alongside a production environment that uses P SKUs.</span></span>

- <span data-ttu-id="c7a59-122">ซื้อ Power BI Premium แม้ว่าคุณจะไม่ใช่บทบาทผู้ดูแลระบบส่วนกลาง Microsoft 365 หรือบทบาทผู้ดูแลระบบการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="c7a59-122">Purchase Power BI Premium even though you're not a Microsoft 365 Global Administrator role or Billing Administrator role.</span></span>

> [!NOTE]
> <span data-ttu-id="c7a59-123">ถ้าคุณซื้อ SKU ขนาด A4 หรือสูงกว่าคุณสามารถใช้ประโยชน์จากคุณลักษณะ Premium ทั้งหมด ยกเว้นการแชร์เนื้อหาได้ไม่จำกัด</span><span class="sxs-lookup"><span data-stu-id="c7a59-123">If you purchase an A4 or higher SKU, you can take advantage of all Premium features except for unlimited sharing of content.</span></span> <span data-ttu-id="c7a59-124">เมื่อใช้ A SKU _ผู้ใช้ทั้งหมด_ ที่ใช้เนื้อหาจำเป็นต้องมีสิทธิการใช้งาน Pro</span><span class="sxs-lookup"><span data-stu-id="c7a59-124">With A SKUs, _all users_ who consume content require Pro licenses.</span></span>

<span data-ttu-id="c7a59-125">ให้ปฏิบัติตามขั้นตอนเหล่านี้เพื่อซื้อ A SKU ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="c7a59-125">Follow these steps to purchase A SKUs in the Azure portal:</span></span>

1. <span data-ttu-id="c7a59-126">ลงชื่อเข้าใช้ [พอร์ทัล Azure](https://portal.azure.com) ด้วยบัญชีที่มีสิทธิ์ระดับผู้ดูแลระบบความจุเป็นอย่างน้อยใน Power BI</span><span class="sxs-lookup"><span data-stu-id="c7a59-126">Sign in to the [Azure portal](https://portal.azure.com) with an account that has at least capacity admin permissions in Power BI.</span></span>

1. <span data-ttu-id="c7a59-127">ค้นหา _Power BI Embedded_ และเลือกบริการในผลลัพธ์การค้นหา</span><span class="sxs-lookup"><span data-stu-id="c7a59-127">Search for _Power BI Embedded_ and select the service in the search results.</span></span>

    ![การค้นหาพอร์ทัล Azure](media/service-admin-premium-purchase/azure-portal-search.png)

1. <span data-ttu-id="c7a59-129">เลือก **สร้าง Power BI Embedded**</span><span class="sxs-lookup"><span data-stu-id="c7a59-129">Select **Create Power BI Embedded**.</span></span>

    ![สร้าง Power BI Embedded](media/service-admin-premium-purchase/create-power-bi-embedded.png)

1. <span data-ttu-id="c7a59-131">บนหน้าจอการสร้าง **Power BI Embedded** ให้ระบุข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c7a59-131">On the **Power BI Embedded** create screen, specify the following information:</span></span>

    - <span data-ttu-id="c7a59-132">**การสมัครรับข่าวสาร** ในการสร้างบริการ Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="c7a59-132">The **Subscription** in which to create the Power BI Embedded service.</span></span>

    - <span data-ttu-id="c7a59-133">**ตำแหน่งที่ตั้ง** ทางกายภาพ ในการสร้างกลุ่มทรัพยากรที่ประกอบด้วยบริการ</span><span class="sxs-lookup"><span data-stu-id="c7a59-133">The physical **Location** in which to create the resource group that contains the service.</span></span> <span data-ttu-id="c7a59-134">เพื่อประสิทธิภาพที่ดีกว่า ตำแหน่งที่ตั้งนี้ควรอยู่ใกล้เคียงกับตำแหน่งที่ตั้งของผู้เช่า Azure Active Directory ของคุณสำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="c7a59-134">For better performance, this location should be close to the location of your Azure Active Directory tenant for Power BI.</span></span>

    - <span data-ttu-id="c7a59-135">**กลุ่มทรัพยากร** ที่มีอยู่ ในการใช้หรือสร้างใหม่ตามที่แสดงในตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="c7a59-135">The existing **Resource group** to use, or create a new one as shown in the example.</span></span>

    - <span data-ttu-id="c7a59-136">**ผู้ดูแลระบบความจุ Power BI**</span><span class="sxs-lookup"><span data-stu-id="c7a59-136">The **Power BI capacity administrator**.</span></span> <span data-ttu-id="c7a59-137">ผู้ดูแลระบบความจุต้องเป็นผู้ใช้ที่เป็นสมาชิกหรือโครงร่างสำคัญของบริการในผู้เช่า Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7a59-137">The capacity admin must be a member user or a service principal in your Azure AD tenant.</span></span>

    ![การสมัครรับข่าวสารและกลุ่มทรัพยากร](media/service-admin-premium-purchase/subscription-resource-group.png)

1. <span data-ttu-id="c7a59-139">ถ้าคุณต้องการใช้คุณลักษณะทั้งหมดของ Power BI Premium (ยกเว้นการแชร์ที่ไม่จำกัด) คุณจำเป็นต้องมี A4 SKU เป็นอย่างน้อย</span><span class="sxs-lookup"><span data-stu-id="c7a59-139">If you want to use all features of Power BI Premium (except unlimited sharing), you need at at least an A4 SKU.</span></span> <span data-ttu-id="c7a59-140">เลือก **เปลี่ยนขนาด**</span><span class="sxs-lookup"><span data-stu-id="c7a59-140">Select **Change size**.</span></span>

    ![เปลี่ยนขนาดความจุ](media/service-admin-premium-purchase/change-capacity-size.png)

1. <span data-ttu-id="c7a59-142">เลือกขนาดความจุ A4, A5 หรือ A6 ซึ่งสอดคล้องกับ P1, P2 และ P3</span><span class="sxs-lookup"><span data-stu-id="c7a59-142">Select a capacity size of A4, A5, or A6, which correspond to P1, P2, and P3.</span></span>

    ![เลือกความจุ A3](media/service-admin-premium-purchase/select-a3-capacity.png)

1. <span data-ttu-id="c7a59-144">เลือก **รีวิว + สร้าง** ตรวจทานตัวเลือกที่คุณเลืกอ จากนั้นเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c7a59-144">Select **Review + Create**, review the options you chose, then select **Create**.</span></span>

    ![สร้างทรัพยากร](media/service-admin-premium-purchase/create-resource.png)

1. <span data-ttu-id="c7a59-146">อาจใช้เวลาสองถึงสามนาทีเพื่อให้การปรับใช้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="c7a59-146">It can take a few minutes to complete the deployment.</span></span> <span data-ttu-id="c7a59-147">เมื่อพร้อมแล้วให้เลือก **ไปที่ทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="c7a59-147">When it's ready, select **Go to resource**.</span></span>

    ![การปรับใช้เสร็จสมบูรณ์](media/service-admin-premium-purchase/deployment-complete.png)

1. <span data-ttu-id="c7a59-149">บนหน้าจอการจัดการ ตรวจทานตัวเลือกที่คุณมีสำหรับการจัดการบริการ รวมถึงการหยุดบริการเมื่อคุณไม่ได้ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c7a59-149">On the management screen, review the options you have for managing the service, including pausing the service when you're not using it.</span></span>

    ![จัดการความจุ](media/service-admin-premium-purchase/manage-capacity.png)

<span data-ttu-id="c7a59-151">หลังจากที่คุณซื้อความจุ ให้เรียนรู้วิธีการ [จัดการความจุ](service-admin-premium-manage.md#manage-capacity) และ [มอบหมายพื้นที่ทำงาน](service-admin-premium-manage.md#assign-a-workspace-to-a-capacity) ให้กับความจุ</span><span class="sxs-lookup"><span data-stu-id="c7a59-151">After you purchase capacity, learn how to [manage capacities](service-admin-premium-manage.md#manage-capacity) and [assign workspaces](service-admin-premium-manage.md#assign-a-workspace-to-a-capacity) to a capacity.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c7a59-152">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c7a59-152">Next steps</span></span>

<span data-ttu-id="c7a59-153">[Power BI Premium คืออะไร](service-premium-what-is.md)
[วิธีการซื้อ Power BI Premium](service-admin-premium-purchase.md)
[กำหนดค่าและจัดการความจุใน Power BI Premium](service-admin-premium-manage.md)\</span><span class="sxs-lookup"><span data-stu-id="c7a59-153">[What is Power BI Premium?](service-premium-what-is.md)
[How to purchase Power BI Premium](service-admin-premium-purchase.md)
[Configure and manage capacities in Power BI Premium](service-admin-premium-manage.md)\</span></span>
<span data-ttu-id="c7a59-154">[หน้าการกำหนดราคา Power BI](https://powerbi.microsoft.com/pricing/)</span><span class="sxs-lookup"><span data-stu-id="c7a59-154">[Power BI pricing page](https://powerbi.microsoft.com/pricing/)</span></span>\
<span data-ttu-id="c7a59-155">[เครื่องคิดเลข Power BI Premium](https://powerbi.microsoft.com/calculator/)</span><span class="sxs-lookup"><span data-stu-id="c7a59-155">[Power BI Premium calculator](https://powerbi.microsoft.com/calculator/)</span></span>\
<span data-ttu-id="c7a59-156">[คำถามที่ถามบ่อยสำหรับ Power BI Premium](service-premium-faq.md)</span><span class="sxs-lookup"><span data-stu-id="c7a59-156">[Power BI Premium FAQ](service-premium-faq.md)</span></span>\
[<span data-ttu-id="c7a59-157">เอกสารทางเทคนิคเรื่องการวางแผนการใช้ Power BI สำหรับองค์กร</span><span class="sxs-lookup"><span data-stu-id="c7a59-157">Planning a Power BI Enterprise Deployment whitepaper</span></span>](https://aka.ms/pbienterprisedeploy)

<span data-ttu-id="c7a59-158">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c7a59-158">More questions?</span></span> [<span data-ttu-id="c7a59-159">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="c7a59-159">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
