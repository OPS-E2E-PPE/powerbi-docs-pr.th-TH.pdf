---
title: ดูและจัดการใบอนุญาตของผู้ใช้ Power BI
description: วิธีการที่ข้อมูลสำหรับผู้ดูแลระบบดูและจัดการใบอนุญาตผู้ใช้ Power BI ในองค์กรของพวกเขา
author: mihart
ms.author: mihart
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: how-to
ms.date: 04/08/2020
ms.custom: licensing support
LocalizationGroup: Administration
ms.openlocfilehash: 6e00474d81d4de1c8316625c6e3a7ade1bf73197
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96408607"
---
# <a name="view-and-manage-power-bi-user-licenses"></a><span data-ttu-id="945ae-103">ดูและจัดการใบอนุญาตของผู้ใช้ Power BI</span><span class="sxs-lookup"><span data-stu-id="945ae-103">View and manage Power BI user licenses</span></span>

<span data-ttu-id="945ae-104">บทความนี้อธิบายว่าผู้ดูแลระบบสามารถใช้ศูนย์การจัดการ Microsoft 365 หรือพอร์ทัล Azure เพื่อดูและจัดการใบอนุญาตของผู้ใช้สำหรับบริการ Power BI ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="945ae-104">This article explains how admins can use the Microsoft 365 admin center or the Azure portal to view and manage user licenses for the Power BI service.</span></span>

> [!NOTE]
>
><span data-ttu-id="945ae-105">เป็นไปได้สำหรับผู้ใช้ที่มีทั้งสิทธิการใช้งาน Power BI (ฟรี) และ Power BI Pro ที่มอบหมาย</span><span class="sxs-lookup"><span data-stu-id="945ae-105">It's possible for a user to have both a Power BI (free) and a Power BI Pro license assigned.</span></span> <span data-ttu-id="945ae-106">ซึ่งสามารถเกิดขึ้นได้เมื่อผู้ใช้ลงทะเบียนสำหรับสิทธิการใช้งานฟรี และจากนั้นจะถูกมอบหมายสิทธิการใช้งาน Power BI Pro ให้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="945ae-106">This can happen when a user signs up for a free license and then is later assigned a Power BI Pro license.</span></span> <span data-ttu-id="945ae-107">ระดับสิทธิ์ใช้งานสูงสุดจะมีผลในกรณีนี้</span><span class="sxs-lookup"><span data-stu-id="945ae-107">The highest licensing level takes effect in this case.</span></span>
>

## <a name="view-your-subscriptions"></a><span data-ttu-id="945ae-108">ดูการสมัครใช้งานของคุณ</span><span class="sxs-lookup"><span data-stu-id="945ae-108">View your subscriptions</span></span>

<span data-ttu-id="945ae-109">หากต้องการดูการสมัครใช้งาน Power BI ที่องค์กรของคุณมี ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="945ae-109">To see which Power BI subscriptions your organization has, follow these steps.</span></span>

1. <span data-ttu-id="945ae-110">ลงชื่อเข้าใช้ [ศูนย์การจัดการ Microsoft 365](https://admin.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="945ae-110">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>
2. <span data-ttu-id="945ae-111">บนเมนูการนำทาง ให้เลือก **การเรียกเก็บเงิน** > **ผลิตภัณฑ์และบริการ**</span><span class="sxs-lookup"><span data-stu-id="945ae-111">In the navigation menu, select **Billing** > **Products & services**.</span></span>

<span data-ttu-id="945ae-112">การสมัครใช้งาน Power BI ที่ใช้งานของคุณจะแสดงอยู่ในรายการพร้อมกับการสมัครใช้งานอื่น ๆ ที่คุณมี</span><span class="sxs-lookup"><span data-stu-id="945ae-112">Your active Power BI subscriptions are listed along with any other subscriptions you have.</span></span> <span data-ttu-id="945ae-113">คุณอาจเห็นการสมัครใช้งานที่ไม่คาดคิดสำหรับ Power BI (ฟรี) ดังที่แสดงไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="945ae-113">You may see an unexpected subscription for Power BI (free), as shown here.</span></span>

  ![ภาพหน้าจอของการสมัครใช้งาน Power B I ที่แสดงการสมัครใช้งานฟรี](media/service-admin-manage-licenses/power-bi-free-user-activated.png)

<span data-ttu-id="945ae-115">การสมัครใช้งานประเภทนี้จะถูกสร้างขึ้นสำหรับคุณเมื่อผู้ใช้ใช้ประโยชน์จากการลงทะเบียนแบบบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="945ae-115">This type of subscription is created for you when users take advantage of self-service sign-up.</span></span> <span data-ttu-id="945ae-116">หากต้องการอ่านเพิ่มเติม โปรดดู [Power BI ในองค์กรของคุณ](/microsoft-365/admin/misc/power-bi-in-your-organization?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="945ae-116">To read more, see [Power BI in your organization](/microsoft-365/admin/misc/power-bi-in-your-organization?view=o365-worldwide).</span></span>

## <a name="manage-user-licenses-in-microsoft-365"></a><span data-ttu-id="945ae-117">จัดการสิทธิการใช้งานผู้ใช้ใน Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="945ae-117">Manage user licenses in Microsoft 365</span></span>

<span data-ttu-id="945ae-118">หากต้องการใช้ศูนย์การจัดการ Microsoft 365 เพื่อจัดการสิทธิ์ใช้งานผู้ใช้ โปรดดู [เอกสารประกอบการสมัครสมาชิกธุรกิจและการเรียกเก็บเงิน](/microsoft-365/commerce/?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="945ae-118">To use Microsoft 365 admin center to manage user licenses, see the [Business subscriptions and billing documentation](/microsoft-365/commerce/?view=o365-worldwide).</span></span>

## <a name="manage-user-licenses-in-azure-portal"></a><span data-ttu-id="945ae-119">จัดการสิทธิการใช้งานผู้ใช้ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="945ae-119">Manage user licenses in Azure portal</span></span>

<span data-ttu-id="945ae-120">ทำตามขั้นตอนเหล่านี้เพื่อดูและกำหนดสิทธิ์ใช้งาน Power BI โดยใช้พอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="945ae-120">Follow these steps to view and assign Power BI licenses using the Azure portal.</span></span>

1. <span data-ttu-id="945ae-121">ลงชื่อเข้าใช้ไปยัง [พอร์ทัล Azure](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="945ae-121">Sign in to the [Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="945ae-122">ค้นหาและเลือก **Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="945ae-122">Search for and select **Azure Active Directory**.</span></span>

3. <span data-ttu-id="945ae-123">ในส่วน **จัดการ** บนเมนูแหล่งข้อมูล Azure Active Directory ให้เลือก **สิทธิการใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="945ae-123">Under **Manage** on the Azure Active Directory resource menu, select **Licenses**.</span></span>

4. <span data-ttu-id="945ae-124">เลือก **ผลิตภัณฑ์ทั้งหมด** จากเมนูแหล่งข้อมูล จากนั้นเลือกประเภทสิทธิการใช้งาน Power BI เพื่อแสดงรายการของผู้ใช้ที่มีสิทธิการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="945ae-124">Select **All products** from the resource menu, then select a Power BI license type to display the list of licensed users.</span></span>

5. <span data-ttu-id="945ae-125">ในการกำหนดสิทธิการใช้งาน ให้เลือก **+มอบสิทธิ์** จากแถบคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="945ae-125">To assign a license, from the command bar, select **+ Assign**.</span></span> <span data-ttu-id="945ae-126">บนหน้า **มอบสิทธิการใช้งาน** ให้เลือกผู้ใช้ จากนั้นเลือก **ตัวเลือกการมอบสิทธิ์** เพื่อเปิดสิทธิการใช้งาน Power BI สำหรับบัญชีผู้ใช้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="945ae-126">On the **Assign license** page, choose a user then select **Assignment options** to turn on a Power BI license for the selected user account.</span></span>

6. <span data-ttu-id="945ae-127">เมื่อต้องการลบสิทธิการใช้งานออก ให้เลือกกล่องกาเครื่องหมายที่อยู่ถัดจากชื่อของผู้ใช้ จากนั้นเลือก **ลบสิทธิการใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="945ae-127">To remove a license, select the checkbox next to the user's name, then select **Remove license**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="945ae-128">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="945ae-128">Next steps</span></span>

- [<span data-ttu-id="945ae-129">ซื้อ Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="945ae-129">Purchase Power BI Pro</span></span>](service-admin-purchasing-power-bi-pro.md)
- [<span data-ttu-id="945ae-130">การให้สิทธิ์สำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="945ae-130">Licensing for your organization</span></span>](service-admin-licensing-organization.md)