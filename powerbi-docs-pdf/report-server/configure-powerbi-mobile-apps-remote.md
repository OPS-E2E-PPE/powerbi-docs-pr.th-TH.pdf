---
title: กำหนดค่าการเข้าถึงแอปอุปกรณ์เคลื่อนที่ สำหรับเซิร์ฟเวอร์รายงานของคุณจากระยะไกล
description: เรียนรู้วิธีการกำหนดค่าแอปอุปกรณ์เคลื่อน สำหรับเซิร์ฟเวอร์รายงานของคุณจากระยะไกล
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.date: 11/07/2019
ms.openlocfilehash: c83ce0735e31e65a813723ce411281821680628d
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418106"
---
# <a name="configure-power-bi-mobile-app-access-to-report-server-remotely"></a><span data-ttu-id="c87f2-103">กำหนดค่าการเข้าถึงเซิร์ฟเวอร์รายงานจากระยะไกล สำหรับแอปอุปกรณ์เคลื่อนที่ ของ Power BI</span><span class="sxs-lookup"><span data-stu-id="c87f2-103">Configure Power BI mobile app access to Report Server remotely</span></span>

<span data-ttu-id="c87f2-104">ใช้ได้กับ:</span><span class="sxs-lookup"><span data-stu-id="c87f2-104">Applies to:</span></span>

| ![iPhone](./media/configure-powerbi-mobile-apps-remote/ios-logo-40-px.png) | ![มือถือ Android](./media/configure-powerbi-mobile-apps-remote/android-logo-40-px.png) |
|:--- |:--- |
| <span data-ttu-id="c87f2-107">iOS</span><span class="sxs-lookup"><span data-stu-id="c87f2-107">iOS</span></span> |<span data-ttu-id="c87f2-108">Android</span><span class="sxs-lookup"><span data-stu-id="c87f2-108">Android</span></span> |

<span data-ttu-id="c87f2-109">ในบทความนี้ เรียนรู้วิธีการใช้เครื่องมือ MDM ขององค์กรของคุณเพื่อกำหนดค่าการเข้าถึงแอปอุปกรณ์เคลื่อนที่ไปยังเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="c87f2-109">In this article, learn how to use your organization's MDM tool to configure Power BI mobile app access to Report Server.</span></span> <span data-ttu-id="c87f2-110">เมื่อต้องการกำหนดค่า ผู้ดูแลระบบ IT สร้างนโยบายการกำหนดค่าแอปด้วยข้อมูลที่จำเป็นเพื่อที่จะส่งไปยังแอป</span><span class="sxs-lookup"><span data-stu-id="c87f2-110">To configure it, IT administrators create an app configuration policy with the required information to be pushed to the app.</span></span> 

 <span data-ttu-id="c87f2-111">ผู้ใช้แอป Power BI สำหรับอุปกรณ์เคลื่อนที่ สามารถเชื่อมต่อกับเซิร์ฟเวอร์รายงานขององค์กรได้ง่ายขึ้น เนื่องจากมีการกำหนดค่าการเชื่อมต่อเซิร์ฟเวอร์รายงานไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c87f2-111">With the Report Server connection already configured, Power BI mobile app users can connect to their organization's Report Server more easily.</span></span> 

## <a name="create-the-app-configuration-policy-in-mdm-tool"></a><span data-ttu-id="c87f2-112">สร้างนโยบายการกำหนดค่าแอปในเครื่องมือ MDM</span><span class="sxs-lookup"><span data-stu-id="c87f2-112">Create the app configuration policy in MDM tool</span></span> 

<span data-ttu-id="c87f2-113">ในฐานะผู้ดูแลระบบ ต่อไปนี้คือขั้นตอนที่คุณทำตามใน Microsoft Intune เพื่อสร้างนโยบายการกำหนดค่าแอป</span><span class="sxs-lookup"><span data-stu-id="c87f2-113">As admin, here are the steps you follow in Microsoft Intune to create the app configuration policy.</span></span> <span data-ttu-id="c87f2-114">ขั้นตอนและประสบการณ์การสร้างนโยบายการกำหนดค่าแอปอาจแตกต่างกันในเครื่องมือ MDM อื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="c87f2-114">The steps and experience of building the app configuration policy may be different in other MDM tools.</span></span> 

1. <span data-ttu-id="c87f2-115">เชื่อมต่อเครื่องมือ MDM ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c87f2-115">Connect your MDM tool.</span></span> 
2. <span data-ttu-id="c87f2-116">สร้างและตั้งชื่อนโยบายการกำหนดค่าแอปใหม่</span><span class="sxs-lookup"><span data-stu-id="c87f2-116">Create and name a new app configuration policy.</span></span> 
3. <span data-ttu-id="c87f2-117">เลือกผู้ใช้ที่คุณจะแจกจ่ายนโยบายกำหนดค่าแอปนี้ไปให้</span><span class="sxs-lookup"><span data-stu-id="c87f2-117">Choose which users to distribute this app configuration policy to.</span></span> 
4. <span data-ttu-id="c87f2-118">สร้างคู่คีย์-ค่า</span><span class="sxs-lookup"><span data-stu-id="c87f2-118">Create key-value pairs.</span></span> 

<span data-ttu-id="c87f2-119">ตารางต่อไปนี้กล่าวถึงคู่ต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="c87f2-119">The following table spells out the pairs.</span></span>

|<span data-ttu-id="c87f2-120">คีย์</span><span class="sxs-lookup"><span data-stu-id="c87f2-120">Key</span></span>  |<span data-ttu-id="c87f2-121">ประเภท</span><span class="sxs-lookup"><span data-stu-id="c87f2-121">Type</span></span>  |<span data-ttu-id="c87f2-122">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c87f2-122">Description</span></span>  |
|---------|---------|---------|
| <span data-ttu-id="c87f2-123">com.microsoft.powerbi.mobile.ServerURL</span><span class="sxs-lookup"><span data-stu-id="c87f2-123">com.microsoft.powerbi.mobile.ServerURL</span></span> | <span data-ttu-id="c87f2-124">สตริง</span><span class="sxs-lookup"><span data-stu-id="c87f2-124">String</span></span> | <span data-ttu-id="c87f2-125">URL เซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="c87f2-125">Report Server URL</span></span> <br> <span data-ttu-id="c87f2-126">ควรเริ่มต้นด้วย http/https</span><span class="sxs-lookup"><span data-stu-id="c87f2-126">Should start with http/https</span></span> |
| <span data-ttu-id="c87f2-127">com.microsoft.powerbi.mobile.ServerUsername</span><span class="sxs-lookup"><span data-stu-id="c87f2-127">com.microsoft.powerbi.mobile.ServerUsername</span></span> | <span data-ttu-id="c87f2-128">สตริง</span><span class="sxs-lookup"><span data-stu-id="c87f2-128">String</span></span> | <span data-ttu-id="c87f2-129">[เป็นทางเลือก]</span><span class="sxs-lookup"><span data-stu-id="c87f2-129">[optional]</span></span> <br> <span data-ttu-id="c87f2-130">ชื่อผู้ใช้เพื่อใช้สำหรับการเชื่อมต่อเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="c87f2-130">The username to use for connecting the server.</span></span> <br> <span data-ttu-id="c87f2-131">หากไม่มีชื่ออยู่ แอปจะปรากฏข้อควมให้ผู้ใช้ให้พิมพ์ชื่อผู้ใช้สำหรับการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="c87f2-131">If one does not exist, the app prompts the user to type the username for the connection.</span></span>| 
| <span data-ttu-id="c87f2-132">com.microsoft.powerbi.mobile.ServerDisplayName</span><span class="sxs-lookup"><span data-stu-id="c87f2-132">com.microsoft.powerbi.mobile.ServerDisplayName</span></span> | <span data-ttu-id="c87f2-133">สตริง</span><span class="sxs-lookup"><span data-stu-id="c87f2-133">String</span></span> | <span data-ttu-id="c87f2-134">[เป็นทางเลือก]</span><span class="sxs-lookup"><span data-stu-id="c87f2-134">[optional]</span></span> <br> <span data-ttu-id="c87f2-135">ค่าเริ่มต้นเป็น "เซิร์ฟเวอร์รายงาน"</span><span class="sxs-lookup"><span data-stu-id="c87f2-135">Default value is “Report server”</span></span> <br> <span data-ttu-id="c87f2-136">ชื่อที่เรียกง่ายที่ใช้ในแอปเพื่อเป็นตัวแทนเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="c87f2-136">A friendly name used in the app to represent the server</span></span> | 
| <span data-ttu-id="c87f2-137">com.microsoft.powerbi.mobile.OverrideServerDetails</span><span class="sxs-lookup"><span data-stu-id="c87f2-137">com.microsoft.powerbi.mobile.OverrideServerDetails</span></span> | <span data-ttu-id="c87f2-138">บูลีน</span><span class="sxs-lookup"><span data-stu-id="c87f2-138">Boolean</span></span> | <span data-ttu-id="c87f2-139">ค่าเริ่มต้นเป็น True</span><span class="sxs-lookup"><span data-stu-id="c87f2-139">Default value is True</span></span> <br><span data-ttu-id="c87f2-140">เมื่อตั้งค่าเป็น "True" จะแทนที่ข้อกำหนดของเซิร์ฟเวอร์รายงานใด ๆ ที่อยู่ในอุปกรณ์เคลื่อนที่อยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="c87f2-140">When set to “True”, it overrides any Report Server definition already in the mobile device.</span></span> <span data-ttu-id="c87f2-141">เซิร์ฟเวอร์ที่มีอยู่ที่ถูกกำหนดค่าไว้จะถูกลบ</span><span class="sxs-lookup"><span data-stu-id="c87f2-141">Existing servers that are already configured are deleted.</span></span> <br> <span data-ttu-id="c87f2-142">การแทนการตั้งค่าเป็น True ยังช่วยป้องกันไม่ให้ผู้ใช้ลบการกำหนดค่านั้นด้วย</span><span class="sxs-lookup"><span data-stu-id="c87f2-142">Override set to True also prevents the user from removing that configuration.</span></span> <br> <span data-ttu-id="c87f2-143">การตั้งค่าเป็น "False" จะเพิ่มค่าที่ส่ง โดยอปล่อยให้มีการใช้การตั้งค่าใด ๆ ที่มีอยู่ต่อไป</span><span class="sxs-lookup"><span data-stu-id="c87f2-143">Set to “False” adds the pushed values, leaving any existing settings.</span></span> <br> <span data-ttu-id="c87f2-144">หากมีการกำหนดค่า URL เซิร์ฟเวอร์เดียวกันในแอปสำหรับอุปกรณ์เคลื่อนที่แล้ว แอปจะปิดการกำหนดค่าดังกล่าวด้วย</span><span class="sxs-lookup"><span data-stu-id="c87f2-144">If the same server URL is already configured in the mobile app, the app leaves that configuration as is.</span></span> <span data-ttu-id="c87f2-145">แอปจะไม่ขอให้ผู้ใช้ตรวจสอบสิทธิ์ซ้ำสำหรับเซิร์ฟเวอร์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="c87f2-145">The app doesn't ask the user to reauthenticate  for the same server.</span></span> |

<span data-ttu-id="c87f2-146">นี่คือตัวอย่างของการตั้งค่านโยบายการกำหนดค่าโดยใช้ Intune</span><span class="sxs-lookup"><span data-stu-id="c87f2-146">Here's an example of setting the configuration policy using Intune.</span></span>

![การตั้งค่าการกำหนดค่า Intune](media/configure-powerbi-mobile-apps-remote/power-bi-ios-remote-configuration-settings.png)

## <a name="end-users-connecting-to-report-server"></a><span data-ttu-id="c87f2-148">ผู้ใช้ปลายทางที่เชื่อมต่อกับเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="c87f2-148">End users connecting to Report Server</span></span>

 <span data-ttu-id="c87f2-149">สมมติว่าคุณเผยแพร่นโยบายการกำหนดค่าแอปสำหรับรายชื่อการแจกจ่าย</span><span class="sxs-lookup"><span data-stu-id="c87f2-149">Say you publish the app configuration policy for a distribution list.</span></span> <span data-ttu-id="c87f2-150">เมื่อผู้ใช้และอุปกรณ์ในรายชื่อการแจกจ่ายดังกล่าวเริ่มต้นใช้งานแอปสำหรับอุปกรณ์เคลื่อนที่ พวกเขาจะได้รับประสบการณ์ดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c87f2-150">When users and devices on that distribution list start the mobile app, they have the following experience.</span></span> 

1. <span data-ttu-id="c87f2-151">พวกเขาจะเห็นข้อความว่าแอปสำหรับอุปกรณ์เคลื่อนที่ของตนได้กำหนดค่าสำหรับเซิร์ฟเวอร์รายงานแล้ว และแตะ **ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="c87f2-151">They see a message that their mobile app is configured with a Report Server, and tap **Sign in**.</span></span>

    ![ลงชื่อเข้าใช้เซิร์ฟเวอร์รายงาน](media/configure-powerbi-mobile-apps-remote/power-bi-config-server-sign-in.png)

2.  <span data-ttu-id="c87f2-153">บนหน้า **เชื่อมต่อกับเซิร์ฟเวอร์** รายละเอียดของเซิร์ฟเวอร์รายงานได้ถูกกรอกให้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c87f2-153">On the **Connect to server** page, the report server details already filled in.</span></span> <span data-ttu-id="c87f2-154">ผู้ใช้แตะ **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="c87f2-154">They tap **Connect**.</span></span>

    ![รายละเอียดของเซิร์ฟเวอร์รายงานที่กรอกให้แล้ว](media/configure-powerbi-mobile-apps-remote/power-bi-ios-remote-configure-connect-server.png)

3. <span data-ttu-id="c87f2-156">ผู้ใช้พิมพ์รหัสผ่านเพื่อรับรองความถูกต้อง จากนั้นแตะ **ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="c87f2-156">They type a password to authenticate, then tap **Sign in**.</span></span> 

    ![สกรีนช็อตแสดงการป้อนรหัสผ่านด้วยปุ่มลงชื่อเข้าใช้](media/configure-powerbi-mobile-apps-remote/power-bi-config-server-address.png)

<span data-ttu-id="c87f2-158">ตอนนี้ ผู้ใช้สามารถดูและโต้ตอบกับ KPI และรายงาน Power BI ที่จัดเก็บบนเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="c87f2-158">Now they can view and interact with KPIs and Power BI reports stored on the Report Server.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c87f2-159">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c87f2-159">Next steps</span></span>

- [<span data-ttu-id="c87f2-160">เปิดใช้งานการเข้าถึงระยะไกลไปยัง Power BI Mobile ด้วยพร็อกซีแอปพลิเคชันของ Azure AD</span><span class="sxs-lookup"><span data-stu-id="c87f2-160">Enable remote access to Power BI Mobile with Azure AD Application Proxy</span></span>](/azure/active-directory/manage-apps/application-proxy-integrate-with-power-bi)
- [<span data-ttu-id="c87f2-161">ภาพรวมของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="c87f2-161">Administrator overview</span></span>](admin-handbook-overview.md)  
- [<span data-ttu-id="c87f2-162">ติดตั้ง Power BI Report Server</span><span class="sxs-lookup"><span data-stu-id="c87f2-162">Install Power BI Report Server</span></span>](install-report-server.md)  

<span data-ttu-id="c87f2-163">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c87f2-163">More questions?</span></span> [<span data-ttu-id="c87f2-164">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="c87f2-164">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)