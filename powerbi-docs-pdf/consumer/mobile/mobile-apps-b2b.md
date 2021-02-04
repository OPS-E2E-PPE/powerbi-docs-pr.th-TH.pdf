---
title: ดูเนื้อหา Power BI ในฐานะผู้ใช้ที่เป็นผู้เยี่ยมชมภายนอก (Azure AD B2B)
description: ใช้แอป Power BI สำหรับอุปกรณ์เคลื่อนที่เพื่อดูเนื้อหาที่แชร์กับคุณจากองค์กรภายนอก
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 12/09/2019
ms.openlocfilehash: effa9622896f44cff0cf37d7612c35f27e726ef7
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413253"
---
# <a name="view-power-bi-content-shared-with-you-from-an-external-organization"></a><span data-ttu-id="a66f4-103">ดูเนื้อหา Power BI ที่แชร์กับคุณจากองค์กรภายนอก</span><span class="sxs-lookup"><span data-stu-id="a66f4-103">View Power BI content shared with you from an external organization</span></span>

<span data-ttu-id="a66f4-104">Power BI บูรณาการรวมเข้ากับ Azure Active Directory แบบธุรกิจกับธุรกิจ (Azure AD B2B) เพื่ออนุญาตให้มีการกระจายความปลอดภัยของเนื้อหา Power BI ไปยังผู้ใช้เป็นผู้เยี่ยมชมภายนอกองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="a66f4-104">Power BI integrates with Azure Active Directory business-to-business (Azure AD B2B) to allow secure distribution of Power BI content to guest users outside your organization.</span></span> <span data-ttu-id="a66f4-105">และผู้ใช้ที่เป็นผู้เยี่ยมชมภายนอกสามารถใช้แอป Power BI เพื่อเข้าถึงเนื้อหา Power BI ที่แชร์กับพวกเขาได้</span><span class="sxs-lookup"><span data-stu-id="a66f4-105">And external guest users can use the Power BI mobile app to access that Power BI content shared with them.</span></span> 


<span data-ttu-id="a66f4-106">ใช้ได้กับ:</span><span class="sxs-lookup"><span data-stu-id="a66f4-106">Applies to:</span></span>

| ![iPhone](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/iphone-logo-50-px.png) | ![iPad](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/ipad-logo-50-px.png) | ![มือถือ Android](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/android-phone-logo-50-px.png) | ![แท็บเล็ต Android](./media/mobile-app-ssrs-kpis-mobile-on-premises-reports/android-tablet-logo-50-px.png) |
|:--- |:--- |:--- |:--- |
| <span data-ttu-id="a66f4-111">iPhones</span><span class="sxs-lookup"><span data-stu-id="a66f4-111">iPhones</span></span> |<span data-ttu-id="a66f4-112">iPad</span><span class="sxs-lookup"><span data-stu-id="a66f4-112">iPads</span></span> |<span data-ttu-id="a66f4-113">มือถือ Android</span><span class="sxs-lookup"><span data-stu-id="a66f4-113">Android phones</span></span> |<span data-ttu-id="a66f4-114">แท็บเล็ต Android</span><span class="sxs-lookup"><span data-stu-id="a66f4-114">Android tablets</span></span> |

## <a name="accessing-shared-content"></a><span data-ttu-id="a66f4-115">การเข้าถึงเนื้อหาที่แชร์</span><span class="sxs-lookup"><span data-stu-id="a66f4-115">Accessing shared content</span></span>

<span data-ttu-id="a66f4-116">**ก่อนอื่น คุณต้องการใครสักคนจากองค์กรภายนอกเพื่อแชร์รายการกับคุณ**</span><span class="sxs-lookup"><span data-stu-id="a66f4-116">**First, you need someone from an external organization to share an item with you.**</span></span> <span data-ttu-id="a66f4-117">เมื่อมีคน [แชร์รายการกับคุณ](../../collaborate-share/service-share-dashboards.md) ไม่ว่าจะเป็นจากองค์กรเดียวกันหรือจากองค์กรภายนอก คุณจะได้รับอีเมลพร้อมลิงก์ไปยังรายการที่แชร์นั้น</span><span class="sxs-lookup"><span data-stu-id="a66f4-117">When someone [shares an item with you](../../collaborate-share/service-share-dashboards.md), either from the same organization or from an external organization, you receive an email with a link to that shared item.</span></span> <span data-ttu-id="a66f4-118">การกดเข้าลิงก์ในอุปกรณ์มือถือของคุณจะเปิดแอป Power BI สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="a66f4-118">Following that link in your mobile device opens the Power BI mobile app.</span></span> <span data-ttu-id="a66f4-119">หากแอปตระหนักว่ารายการนั้นแชร์จากองค์กรภายนอก แอปจะเชื่อมต่อกับองค์กรนั้นอีกครั้งด้วยข้อมูลประจำตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="a66f4-119">If the app recognizes that the item was shared from an external organization, the app reconnects to that organization with your identity.</span></span> <span data-ttu-id="a66f4-120">หลังจากนั้นแอปจะโหลดรายการทั้งหมดที่แชร์กับคุณจากองค์กรนั้น</span><span class="sxs-lookup"><span data-stu-id="a66f4-120">The app then loads all items that were shared with you from that organization.</span></span>

![<span data-ttu-id="a66f4-121">Power BI เปิดรายการที่แชร์จากอีเมล</span><span class="sxs-lookup"><span data-stu-id="a66f4-121">Power BI open shared item from email</span></span> ](./media/mobile-apps-b2b/mobile-b2b-open-item-email-new.png)

> [!NOTE]
> <span data-ttu-id="a66f4-122">หากนี่เป็นรายการแรกที่แชร์กับคุณในฐานะผู้ใช้ที่เป็นผู้เยี่ยมชมภายนอก คุณจะต้องอ้างสิทธิ์การเชิญในเบราว์เซอร์ก่อน</span><span class="sxs-lookup"><span data-stu-id="a66f4-122">If this is the first item shared with you as an external guest user, you must claim the invitation in a browser.</span></span> <span data-ttu-id="a66f4-123">คุณไม่สามารถอ้างสิทธิ์คำเชิญในแอป Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="a66f4-123">You can cannot claim the invitation in the Power BI app.</span></span>

<span data-ttu-id="a66f4-124">ตราบใดที่คุณเชื่อมต่อกับองค์กรภายนอก ส่วนหัวสีดำจะปรากฏขึ้นในแอป</span><span class="sxs-lookup"><span data-stu-id="a66f4-124">As long as you are connected to an external organization, a black header appears in the app.</span></span> <span data-ttu-id="a66f4-125">ส่วนหัวนี้บ่งชี้ว่าคุณไม่ได้เชื่อมต่อกับองค์กรหลักของคุณ</span><span class="sxs-lookup"><span data-stu-id="a66f4-125">This header indicates that you are not connected to your home organization.</span></span> <span data-ttu-id="a66f4-126">หากต้องการเชื่อมต่อกลับไปยังองค์กรหลักของคุณ ให้ออกจากโหมดผู้เยี่ยมชม</span><span class="sxs-lookup"><span data-stu-id="a66f4-126">To connect back to your home organization, exit from guest mode.</span></span>

![ส่วนหัวของผู้ใช้ที่เป็นผู้เยี่ยมชม Power BI](./media/mobile-apps-b2b/mobile-b2b-exit-home-new.png)

<span data-ttu-id="a66f4-128">แม้ว่าคุณจะต้องมีลิงก์วัตถุ Power BI เพื่อเชื่อมต่อกับองค์กรภายนอก แต่เมื่อมีการสลับแอปของคุณ คุณสามารถเข้าถึงรายการทั้งหมดที่แชร์กับคุณได้ (ไม่เฉพาะรายการที่คุณเปิดจากอีเมลเท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="a66f4-128">Even though you need to have a Power BI artifact link to connect to an external organization, once your app switches, you can access all items shared with you (not only the item you opened from the email).</span></span> <span data-ttu-id="a66f4-129">หากต้องการดูรายการทั้งหมดที่คุณสามารถเข้าถึงได้ในองค์กรภายนอก ให้ไปที่เมนูแอปและเลือก **แบ่งปันกับฉัน**</span><span class="sxs-lookup"><span data-stu-id="a66f4-129">To view all items you can access in the external organization, go to the app menu and select **Shared with me**.</span></span> <span data-ttu-id="a66f4-130">ภายใต้ **แอป** คุณจะพบแอปที่คุณสามารถใช้ได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="a66f4-130">Under **Apps**, you find apps that you can use as well.</span></span>

![เมนูแอป Power BI ในฐานะผู้ใช้ที่เป็นผู้เยี่ยมชมภายนอก](./media/mobile-apps-b2b/mobile-b2b-menu-new.png)

## <a name="limitations"></a><span data-ttu-id="a66f4-132">ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="a66f4-132">Limitations</span></span>

- <span data-ttu-id="a66f4-133">ผู้ใช้ต้องมีบัญชี Power BI ที่ใช้งานอยู่และผู้เช่าหลัก</span><span class="sxs-lookup"><span data-stu-id="a66f4-133">Users must have an active Power BI account and Home tenant.</span></span>
- <span data-ttu-id="a66f4-134">ผู้ใช้จะต้องลงชื่อเข้าใช้ผู้เช่าหลักของ Power BI ก่อนจึงจะสามารถเข้าถึงเนื้อหาที่แชร์กับผู้เช่าภายนอกได้</span><span class="sxs-lookup"><span data-stu-id="a66f4-134">Users must be signed in to their Power BI home tenant, before they can access the content shared with them from an external tenant.</span></span>
- <span data-ttu-id="a66f4-135">การเข้าถึงแบบมีเงื่อนไขและนโยบาย Intune อื่นไม่ได้รับการสนับสนุนใน Azure AD B2B และใน Power BI สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="a66f4-135">Conditional access and other Intune policies are not supported in Azure AD B2B and in Power BI mobile.</span></span> <span data-ttu-id="a66f4-136">ซึ่งหมายความว่าแอปจะบังคับใช้เฉพาะนโยบายขององค์กรหลักเท่านั้น ถ้ามีอยู่</span><span class="sxs-lookup"><span data-stu-id="a66f4-136">That means that the app enforces only the home organization's policies, if they exist.</span></span>
- <span data-ttu-id="a66f4-137">ผู้ใช้จะได้รับการแจ้งเตือนแบบพุชจากเว็บไซต์องค์กรหลักเท่านั้น (แม้ว่าผู้ใช้จะเชื่อมต่อในฐานะผู้เยี่ยมชมกับองค์กรภายนอก)</span><span class="sxs-lookup"><span data-stu-id="a66f4-137">Push notifications are received from the home organization site only (even when the user is connected as a guest to an external organization).</span></span> <span data-ttu-id="a66f4-138">การเปิดการแจ้งเตือนจะเชื่อมต่อแอปกับเว็บไซต์องค์กรหลักของผู้ใช้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="a66f4-138">Opening the notification reconnects the app to the user's home organization site.</span></span>
- <span data-ttu-id="a66f4-139">หากผู้ใช้ปิดแอป เมื่อเปิดใหม่อีกครั้ง แอปจะเชื่อมต่อกับองค์กรบหลักของผู้ใช้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a66f4-139">If the user shuts down the app, when reopened the app connects automatically to the user's home organization.</span></span>
- <span data-ttu-id="a66f4-140">เมื่อเชื่อมต่อกับองค์กรภายนอก การดำเนินการบางอย่างจะถูกปิดใช้งาน: รายการโปรด การแจ้งเตือนข้อมูล การแสดงข้อคิดเห็น และการแชร์</span><span class="sxs-lookup"><span data-stu-id="a66f4-140">When connected to an external organization, some actions are disabled: favorite items, data alerts, commenting, and sharing.</span></span>
- <span data-ttu-id="a66f4-141">ข้อมูลแบบออฟไลน์ไม่พร้อมใช้งานในขณะที่เชื่อมต่อกับองค์กรภายนอก</span><span class="sxs-lookup"><span data-stu-id="a66f4-141">Offline data is not available while connected to an external organization.</span></span>
- <span data-ttu-id="a66f4-142">หากคุณติดตั้งแอป Company Portal บนอุปกรณ์ของคุณคุณจะต้องลงทะเบียนอุปกรณ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a66f4-142">If you have the Company Portal app installed on your device, then your device must be enrolled.</span></span>
