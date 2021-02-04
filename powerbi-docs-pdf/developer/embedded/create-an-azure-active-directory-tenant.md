---
title: สร้างผู้เช่า Azure Active Directory เพื่อใช้กับ BI แบบฝังของการวิเคราะห์แบบฝังตัวของ Power BI
description: เรียนรู้วิธีการสร้างผู้เช่า Azure Active Directory (Azure AD) ใหม่สำหรับแอปพลิเคชันการวิเคราะห์แบบฝังตัวที่กำหนดเองที่เรียกใช้ Power BI REST API และเพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังสำหรับลูกค้า
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: how-to
ms.date: 05/28/2019
ms.openlocfilehash: 24e1d8678234b7b355d99985f8e8a567954d6211
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97889029"
---
# <a name="create-an-azure-active-directory-tenant-to-use-with-power-bi"></a><span data-ttu-id="eab2d-103">สร้างผู้เช่า Azure Active Directory เพื่อใช้กับ Power BI</span><span class="sxs-lookup"><span data-stu-id="eab2d-103">Create an Azure Active Directory tenant to use with Power BI</span></span>

<span data-ttu-id="eab2d-104">เรียนรู้วิธีการสร้างผู้เช่า Azure Active Directory (Azure AD) ใหม่สำหรับแอปพลิเคชันแบบกำหนดเองที่เรียกใช้ [Power BI REST API](../automation/rest-api-reference.md)</span><span class="sxs-lookup"><span data-stu-id="eab2d-104">Learn how to create a new Azure Active Directory (Azure AD) tenant for a custom application that calls [Power BI REST APIs](../automation/rest-api-reference.md).</span></span>

<span data-ttu-id="eab2d-105">ผู้เช่าเป็นตัวแทนองค์กรใน Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="eab2d-105">A tenant represents an organization in Azure Active Directory.</span></span> <span data-ttu-id="eab2d-106">ซึ่งเป็นอินสแตนซ์เฉพาะของบริการ Azure AD ที่องค์กรได้รับและเป็นเจ้าของเมื่อลงทะเบียนสมัครใช้บริการระบบคลาวด์ของ Microsoft เช่น Azure  Microsoft Intune หรือ Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="eab2d-106">It's a dedicated Azure AD service instance that an organization receives and owns when it signs up for a Microsoft cloud service such as Azure, Microsoft Intune, or Microsoft 365.</span></span> <span data-ttu-id="eab2d-107">ผู้เช่า Azure AD แต่ละรายจะแตกต่างกันและแยกต่างหากจากผู้เช่า Azure AD อื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="eab2d-107">Each Azure AD tenant is distinct and separate from other Azure AD tenants.</span></span>

<span data-ttu-id="eab2d-108">เมื่อมีผู้เช่า Azure AD คุณสามารถกำหนดแอปพลิเคชันและกำหนดสิทธิเพื่อให้แอปพลิเคชันของคุณสามารถเรียกใช้ [Power BI REST API](../automation/rest-api-reference.md) ได้</span><span class="sxs-lookup"><span data-stu-id="eab2d-108">Once you have an Azure AD tenant, you can define an application and assign it permissions so it can call [Power BI REST APIs](../automation/rest-api-reference.md).</span></span>

<span data-ttu-id="eab2d-109">องค์กรของคุณอาจมีผู้เช่า Azure AD ที่คุณสามารถใช้สำหรับแอปพลิเคชันของคุณอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="eab2d-109">Your organization may already have an Azure AD tenant that you can use for your application.</span></span> <span data-ttu-id="eab2d-110">นอกจากนี้คุณยังสามารถสร้างผู้เช่าใหม่เฉพาะสำหรับแอปพลิเคชันของคุณได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="eab2d-110">You can also create a new tenant specifically for your application.</span></span> <span data-ttu-id="eab2d-111">บทความนี้แสดงถึ่งวิธีการสร้างผู้เช่าใหม่</span><span class="sxs-lookup"><span data-stu-id="eab2d-111">This article shows how to create a new tenant.</span></span>

## <a name="create-an-azure-active-directory-tenant"></a><span data-ttu-id="eab2d-112">สร้างผู้เช่า Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="eab2d-112">Create an Azure Active Directory tenant</span></span>

<span data-ttu-id="eab2d-113">เพื่อรวม Power BI ลงในแอปพลิเคชันแบบกำหนดเองของคุณ คุณจำเป็นต้องกำหนดแอปพลิเคชันภายใน Azure AD ซึ่งจำเป็นต้องมีไดเรกทอรีของ Azure AD</span><span class="sxs-lookup"><span data-stu-id="eab2d-113">To integrate Power BI into your custom application, you need to define an application within Azure AD, which requires an Azure AD directory.</span></span> <span data-ttu-id="eab2d-114">ไดเรกทอรีนี้เป็น *ผู้เช่า* ของคุณ</span><span class="sxs-lookup"><span data-stu-id="eab2d-114">This directory is your *tenant*.</span></span> <span data-ttu-id="eab2d-115">ถ้าองค์กรของคุณยังไม่มีผู้เช่า เนื่องจากพวกเขาไม่ได้ใช้ Power BI หรือ Microsoft 365 [คุณต้องตั้งค่าเครื่องมือที่ช่วยพัฒนาโปรแกรม](/azure/active-directory/develop/active-directory-howto-tenant)</span><span class="sxs-lookup"><span data-stu-id="eab2d-115">If your organization doesn't have a tenant yet, because they aren't using Power BI or Microsoft 365, then [you need to set up a dev environment](/azure/active-directory/develop/active-directory-howto-tenant).</span></span> <span data-ttu-id="eab2d-116">นอกจากนี้ คุณยังต้องสร้างหนึ่งสภาพแวดล้อมถ้าไม่ต้องการให้แอปพลิเคชันของคุณผสมปะปนกับผู้เช่าขององค์กรของคุณ อนุญาตให้คุณเก็บสิ่งที่แยกออกมาต่างหากได้</span><span class="sxs-lookup"><span data-stu-id="eab2d-116">You also need to create one if you don't want your application mixing with your organization's tenant, allowing you to keep things isolated.</span></span> <span data-ttu-id="eab2d-117">หรือคุณอาจเพียงแค่ต้องการสร้างผู้เช่าเพื่อทำการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="eab2d-117">Or, you may just want to create a tenant for testing purposes.</span></span>

<span data-ttu-id="eab2d-118">เมื่อต้องสร้างผู้เช่า Azure AD ใหม่:</span><span class="sxs-lookup"><span data-stu-id="eab2d-118">To create a new Azure AD tenant:</span></span>

1. <span data-ttu-id="eab2d-119">เรียกดู [พอร์ทัล Azure](https://portal.azure.com)และลงชื่อเข้าใช้ด้วยบัญชีผู้ใช้ที่มีการสมัครใช้งาน Azure</span><span class="sxs-lookup"><span data-stu-id="eab2d-119">Browse to the [Azure portal](https://portal.azure.com) and sign in with an account that has an Azure subscription.</span></span>

2. <span data-ttu-id="eab2d-120">เลือก **ไอคอนเครื่องหมายบวก (+)**  และค้นหา **Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="eab2d-120">Select the **plus icon (+)** and search for **Azure Active Directory**.</span></span>

    ![ไอคอนบวก (+)](media/create-an-azure-active-directory-tenant/new-directory.png)

3. <span data-ttu-id="eab2d-122">เลือก **Azure Active Directory** ในผลลัพธ์การค้นหา</span><span class="sxs-lookup"><span data-stu-id="eab2d-122">Select **Azure Active Directory** in the search results.</span></span>

    ![ค้นหา AAD](media/create-an-azure-active-directory-tenant/new-directory2.png)

4. <span data-ttu-id="eab2d-124">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="eab2d-124">Select **Create**.</span></span>

5. <span data-ttu-id="eab2d-125">ระบุ **ชื่อองค์กร** และ **ชื่อโดเมนเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="eab2d-125">Provide an **Organization name** and an **Initial domain name**.</span></span> <span data-ttu-id="eab2d-126">แล้วเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="eab2d-126">Then select **Create**.</span></span> <span data-ttu-id="eab2d-127">ไดเรกทอรีของคุณจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="eab2d-127">Your directory is created.</span></span>

    ![องค์กรและโดเมน](media/create-an-azure-active-directory-tenant/organization-and-domain.png)

   > [!NOTE]
   > <span data-ttu-id="eab2d-129">โดเมนเริ่มต้นของคุณคือ ส่วนหนึ่งของ onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="eab2d-129">Your initial domain is part of onmicrosoft.com.</span></span> <span data-ttu-id="eab2d-130">คุณสามารถเพิ่มชื่อโดเมนอื่น ๆ ได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="eab2d-130">You can add other domain names later.</span></span> <span data-ttu-id="eab2d-131">ไดเรกทอรีผู้เช่าอาจมีได้หลายโดเมนที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="eab2d-131">A tenant directory can have multiple domains assigned to it.</span></span>

6. <span data-ttu-id="eab2d-132">หลังจากการสร้างไดเรกทอรีของคุณเสร็จสมบูรณ์ เลือกกล่องข้อมูลเพื่อจัดการไดเรกทอรีใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="eab2d-132">After directory creation is complete, select the information box to manage your new directory.</span></span>

<span data-ttu-id="eab2d-133">ถัดไป คุณกำลังจะเพิ่มผู้ใช้ที่เป็นผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="eab2d-133">Next, you're going to add tenant users.</span></span>

## <a name="create-azure-active-directory-tenant-users"></a><span data-ttu-id="eab2d-134">สร้างผู้ใช้ที่เป็นผู้เช่า Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="eab2d-134">Create Azure Active Directory tenant users</span></span>

<span data-ttu-id="eab2d-135">ตอนนี้เรามีไดเรกทอรีแล้ว มาสร้างผู้ใช้อย่างน้อยสองรายกัน</span><span class="sxs-lookup"><span data-stu-id="eab2d-135">Now that you have a directory, let's create at least two users.</span></span> <span data-ttu-id="eab2d-136">หนึ่งคือ ผู้ดูแลระบบส่วนกลางผู้เช่า และอีกรายคือ ผู้ใช้หลักสำหรับการฝังตัว</span><span class="sxs-lookup"><span data-stu-id="eab2d-136">One is a tenant Global Admin and another is a master user for embedding.</span></span> <span data-ttu-id="eab2d-137">คุณสามารถนึกภาพหลังจากนั้นเป็นบัญชีบริการได้</span><span class="sxs-lookup"><span data-stu-id="eab2d-137">You can think of the latter as a service account.</span></span>

1. <span data-ttu-id="eab2d-138">ภายในพอร์ทัล Azure ตรวจสอบให้แน่ใจว่าคุณกำลังอยู่บน Azure Active Directory ที่ปรากฎขึ้นทางด้านข้าง</span><span class="sxs-lookup"><span data-stu-id="eab2d-138">In the Azure portal, make sure you are on the Azure Active Directory fly out.</span></span>

    ![Azure AD ที่ปรากฏขึ้น](media/create-an-azure-active-directory-tenant/aad-flyout.png)

    <span data-ttu-id="eab2d-140">ถ้าไม่เป็นเช่นนั้น เลือกไอคอน Azure Active Directory จากแถบบริการทางด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="eab2d-140">If not, select the Azure Active Directory icon from the left services navigation.</span></span>

    ![ไอคอน Azure AD](media/create-an-azure-active-directory-tenant/aad-service.png)

2. <span data-ttu-id="eab2d-142">ภายใต้ **จัดการ** เลือก **ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="eab2d-142">Under **Manage**, select **Users**.</span></span>

    ![ผู้ใช้และกลุ่ม Azure AD](media/create-an-azure-active-directory-tenant/users-and-groups.png)

3. <span data-ttu-id="eab2d-144">เลือก **ผู้ใช้ทั้งหมด** แล้วเลือก **+ ผู้ใช้ใหม่**</span><span class="sxs-lookup"><span data-stu-id="eab2d-144">Select **All users** and then select **+ New user**.</span></span>

4. <span data-ttu-id="eab2d-145">ระบุ **ชื่อ** และ **ชื่อผู้ใช้** สำหรับผู้ดูแลระบบส่วนกลางผู้เช่าของคุณ เปลี่ยน **บทบาทไดเรกทอรี** ให้เป็น **ผู้ดูแลระบบส่วนกลาง**</span><span class="sxs-lookup"><span data-stu-id="eab2d-145">Provide a **Name** and **User name** for your tenant Global Admin. Change the **Directory role** to **Global administrator**.</span></span> <span data-ttu-id="eab2d-146">คุณยังสามารถแสดงรหัสผ่านชั่วคราวได้</span><span class="sxs-lookup"><span data-stu-id="eab2d-146">You can also show the temporary password.</span></span> <span data-ttu-id="eab2d-147">เมื่อคุณทำเสร็จแล้ว เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="eab2d-147">When you're done, select **Create**.</span></span>

    ![ผู้ดูแลระบบส่วนกลางของ Azure AD](media/create-an-azure-active-directory-tenant/global-admin.png)

5. <span data-ttu-id="eab2d-149">ให้ทำแบบเดียวกันสำหรับผู้ใช้ที่เป็นผู้เช่าทั่วไป</span><span class="sxs-lookup"><span data-stu-id="eab2d-149">Do the same thing for a regular tenant user.</span></span> <span data-ttu-id="eab2d-150">คุณสามารถใช้บัญชีนี้สำหรับบัญชีฝังตัวหลักของคุณ</span><span class="sxs-lookup"><span data-stu-id="eab2d-150">You can use this account for your master embedding account.</span></span> <span data-ttu-id="eab2d-151">ในเวลานี้ สำหรับ **บทบาทไดเรกทอรี** ปล่อยให้เป็น **ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="eab2d-151">This time, for **Directory role**, leave it as **User**.</span></span> <span data-ttu-id="eab2d-152">จดรหัสผ่าน จากนั้นเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="eab2d-152">Note the password, then select **Create**.</span></span>

    ![ผู้ใช้ Azure AD](media/create-an-azure-active-directory-tenant/pbiembed-user.png)

6. <span data-ttu-id="eab2d-154">ลงทะเบียนสมัครใช้สำหรับ Power BI ด้วยบัญชีผู้ใช้ที่คุณสร้างในขั้นตอนที่ 5</span><span class="sxs-lookup"><span data-stu-id="eab2d-154">Sign up for Power BI with the user account that you created in step 5.</span></span> <span data-ttu-id="eab2d-155">ไปที่ [powerbi.com](https://powerbi.microsoft.com/get-started/) และเลือก **ทดลองใช้ฟรี** ภายใต้ **Power BI - การทำงานร่วมกันและการแชร์บนระบบคลาวด์**</span><span class="sxs-lookup"><span data-stu-id="eab2d-155">Go to [powerbi.com](https://powerbi.microsoft.com/get-started/) and select **Try free** under **Power BI - Cloud collaboration and sharing**.</span></span>

    ![สร้างผู้เช่า](media/create-an-azure-active-directory-tenant/try-powerbi-free.png)

    <span data-ttu-id="eab2d-157">เมื่อคุณลงทะเบียนสมัครใช้ คุณจะได้รับแจ้งให้ทดลองใช้ Power BI Pro ฟรีเป็นเวลา 60 วัน</span><span class="sxs-lookup"><span data-stu-id="eab2d-157">When you sign up, you're prompted to try Power BI Pro free for 60 days.</span></span> <span data-ttu-id="eab2d-158">คุณสามารถเลือกเพื่อกลายเป็นผู้ใช้ระดับ Pro ซึ่งทำให้คุณมีตัวเลือกในการ[เริ่มต้นพัฒนาโซลูชันแบบฝังตัว](embed-sample-for-customers.md)ได้</span><span class="sxs-lookup"><span data-stu-id="eab2d-158">You can opt into that to become a Pro user, which gives you the option to [start developing an embedded solution](embed-sample-for-customers.md).</span></span>

   > [!NOTE]
   > <span data-ttu-id="eab2d-159">ตรวจสอบให้แน่ใจว่าคุณลงทะเบียนสมัครใช้ด้วยที่อยู่อีเมลของบัญชีผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="eab2d-159">Make sure you sign up with your user account's email address.</span></span>

## <a name="next-steps"></a><span data-ttu-id="eab2d-160">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="eab2d-160">Next steps</span></span>

<span data-ttu-id="eab2d-161">ตอนนี้คุณมีผู้เช่า Azure AD แล้ว คุณสามารถใช้ผู้เช่านี้เพื่อทดสอบรายการภายใน Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="eab2d-161">Now that you have an Azure AD tenant, you can use this tenant to test items within Power BI.</span></span> <span data-ttu-id="eab2d-162">คุณยังสามารถฝังแดชบอร์ด Power BI และรายงานในแอปพลิเคชันของคุณได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="eab2d-162">You can also embed Power BI dashboards and reports in your application.</span></span> <span data-ttu-id="eab2d-163">สำหรับข้อมูลเพิ่มเติม ดู [วิธีฝังแดชบอร์ด รายงานและไทล์ Power BI ของคุณ](embed-sample-for-customers.md)</span><span class="sxs-lookup"><span data-stu-id="eab2d-163">For more information, see [How to embed your Power BI dashboards, reports, and tiles](embed-sample-for-customers.md).</span></span>

[<span data-ttu-id="eab2d-164">แล้ว Azure Active Directory คืออะไร?</span><span class="sxs-lookup"><span data-stu-id="eab2d-164">What is an Azure Active directory?</span></span>](/azure/active-directory/active-directory-whatis) 
 
[<span data-ttu-id="eab2d-165">เริ่มต้นใช้งานด่วน: ตั้งค่าเครื่องมือที่ช่วยในการพัฒนาโปรแกรม</span><span class="sxs-lookup"><span data-stu-id="eab2d-165">Quickstart: Set up a dev environment</span></span>](/azure/active-directory/develop/active-directory-howto-tenant)  

<span data-ttu-id="eab2d-166">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="eab2d-166">More questions?</span></span> [<span data-ttu-id="eab2d-167">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="eab2d-167">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)