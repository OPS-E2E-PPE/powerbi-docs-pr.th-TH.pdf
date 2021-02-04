---
title: ข้อมูลพื้นฐานด้านความปลอดภัย Azure สำหรับ Power BI
description: ข้อมูลพื้นฐานด้านความปลอดภัยของ Power BI ให้คำแนะนำและทรัพยากรเกี่ยวกับขั้นตอนสำหรับการนำคำแนะนำด้านความปลอดภัยที่ระบุไว้ใน Azure Security Benchmark ไปใช้
author: mbaldwin
ms.author: margoc
ms.service: powerbi
ms.subservice: pbi-security
ms.topic: conceptual
ms.date: 11/20/2020
ms.custom: subject-security-benchmark
ms.openlocfilehash: a76c7f9d205fe47322768a514a1e5d89a36a2306
ms.sourcegitcommit: 1cad78595cca1175b82c04458803764ac36e5e37
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/19/2021
ms.locfileid: "98565750"
---
# <a name="azure-security-baseline-for-power-bi"></a><span data-ttu-id="cae0c-103">ข้อมูลพื้นฐานด้านความปลอดภัย Azure สำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-103">Azure security baseline for Power BI</span></span>

<span data-ttu-id="cae0c-104">ข้อมูลพื้นฐานด้านความปลอดภัยนี้ปรับใช้คำแนะนำจาก [Azure Security Benchmark เวอร์ชัน 2.0](/azure/security/benchmarks/overview) กับ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-104">This security baseline applies guidance from the [Azure Security Benchmark version 2.0](/azure/security/benchmarks/overview) to Power BI.</span></span> <span data-ttu-id="cae0c-105">Azure Security Benchmark ให้คำแนะนำเกี่ยวกับวิธีการที่คุณสามารถรักษาความปลอดภัยโซลูชันระบบคลาวด์ของคุณบน Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-105">The Azure Security Benchmark provides recommendations on how you can secure your cloud solutions on Azure.</span></span> <span data-ttu-id="cae0c-106">มีการจัดกลุ่มเนื้อหาตาม **ตัวควบคุมความปลอดภัย** ที่กำหนดโดย Azure Security Benchmark และคำแนะนำที่เกี่ยวข้อง ซึ่งใช้ได้กับ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-106">The content is grouped by the **security controls** defined by the Azure Security Benchmark and the related guidance applicable to Power BI.</span></span> <span data-ttu-id="cae0c-107">ไม่รวม **ตัวควบคุม** ที่ใช้ไม่ได้กับ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-107">**Controls** not applicable to Power BI have been excluded.</span></span>

<span data-ttu-id="cae0c-108">หากต้องการดูว่า Power BI แมปกับ Azure Security Benchmark โดยสมบูรณ์ได้อย่างไร โปรดดูที่[ไฟล์การแมปข้อมูลพื้นฐานด้านความปลอดภัย Power BI ฉบับเต็ม](https://github.com/MicrosoftDocs/SecurityBenchmarks/tree/master/Azure%20Offer%20Security%20Baselines)</span><span class="sxs-lookup"><span data-stu-id="cae0c-108">To see how Power BI completely maps to the Azure Security Benchmark, see the [full Power BI security baseline mapping file](https://github.com/MicrosoftDocs/SecurityBenchmarks/tree/master/Azure%20Offer%20Security%20Baselines).</span></span>

## <a name="network-security"></a><span data-ttu-id="cae0c-109">ความปลอดภัยเครือข่าย</span><span class="sxs-lookup"><span data-stu-id="cae0c-109">Network Security</span></span>

<span data-ttu-id="cae0c-110">*สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Azure Security Benchmark: ความปลอดภัยเครือข่าย](/azure/security/benchmarks/security-controls-v2-network-security)*</span><span class="sxs-lookup"><span data-stu-id="cae0c-110">*For more information, see the [Azure Security Benchmark: Network Security](/azure/security/benchmarks/security-controls-v2-network-security).*</span></span>

### <a name="ns-3-establish-private-network-access-to-azure-services"></a><span data-ttu-id="cae0c-111">NS-3: สร้างการเข้าถึงเครือข่ายส่วนตัวไปยังบริการ Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-111">NS-3: Establish private network access to Azure services</span></span>

<span data-ttu-id="cae0c-112">**คำแนะนำ**: Power BI สนับสนุนการเชื่อมต่อผู้เช่า Power BI ของคุณกับจุดสิ้นสุดลิงก์ส่วนตัว และปิดใช้งานการเข้าถึงอินเทอร์เน็ตสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="cae0c-112">**Guidance**: Power BI supports connecting your Power BI tenant to a Private link endpoint and disabling public internet access.</span></span>

- [<span data-ttu-id="cae0c-113">ใช้ลิงก์ส่วนตัวสำหรับการเข้าใช้งาน Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-113">Private links for accessing Power BI</span></span>](../admin/service-security-private-links.md)

<span data-ttu-id="cae0c-114">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-114">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-115">**ความรับผิดชอบ**: แชร์</span><span class="sxs-lookup"><span data-stu-id="cae0c-115">**Responsibility**: Shared</span></span>

## <a name="identity-management"></a><span data-ttu-id="cae0c-116">การจัดการข้อมูลเอกลักษณ์</span><span class="sxs-lookup"><span data-stu-id="cae0c-116">Identity Management</span></span>

<span data-ttu-id="cae0c-117">*สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Azure Security Benchmark: การจัดการข้อมูลเอกลักษณ์](/azure/security/benchmarks/security-controls-v2-identity-management)*</span><span class="sxs-lookup"><span data-stu-id="cae0c-117">*For more information, see the [Azure Security Benchmark: Identity Management](/azure/security/benchmarks/security-controls-v2-identity-management).*</span></span>

### <a name="im-1-standardize-azure-active-directory-as-the-central-identity-and-authentication-system"></a><span data-ttu-id="cae0c-118">IM-1: ทำให้ Azure Active Directory เป็นมาตรฐานในฐานะข้อมูลเอกลักษณ์ส่วนกลางและระบบการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="cae0c-118">IM-1: Standardize Azure Active Directory as the central identity and authentication system</span></span>

<span data-ttu-id="cae0c-119">**คำแนะนำ**: Power BI ถูกรวมเข้ากับ Azure Active Directory (Azure AD) ซึ่งเป็นข้อมูลเอกลักษณ์เริ่มต้นและบริการจัดการการเข้าถึงของ Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-119">**Guidance**: Power BI is integrated with Azure Active Directory (Azure AD) which is Azure's default identity and access management service.</span></span> <span data-ttu-id="cae0c-120">คุณควรสร้างมาตรฐานบน Azure AD เพื่อควบคุมข้อมูลเอกลักษณ์ขององค์กรและการจัดการการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="cae0c-120">You should standardize on Azure AD to govern your organization’s identity and access management.</span></span>

<span data-ttu-id="cae0c-121">การรักษาความปลอดภัย Azure AD ควรมีลำดับความสำคัญสูงในแนวทางปฏิบัติด้านความปลอดภัยบนคลาวด์ขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="cae0c-121">Securing Azure AD should be a high priority in your organization’s cloud security practice.</span></span> <span data-ttu-id="cae0c-122">Azure AD ให้คะแนนความปลอดภัยของข้อมูลเอกลักษณ์เพื่อช่วยคุณประเมินสภาวะความปลอดภัยของข้อมูลเอกลักษณ์ที่สัมพันธ์กับคำแนะนำแนวทางปฏิบัติที่ดีที่สุดของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="cae0c-122">Azure AD provides an identity secure score to help you assess identity security posture relative to Microsoft’s best practice recommendations.</span></span> <span data-ttu-id="cae0c-123">ใช้คะแนนเพื่อวัดว่าการกำหนดค่าของคุณตรงกับคำแนะนำแนวทางปฏิบัติที่ดีที่สุดเพียงใดและเพื่อปรับปรุงสภาวะความปลอดภัยของคุณ</span><span class="sxs-lookup"><span data-stu-id="cae0c-123">Use the score to gauge how closely your configuration matches best practice recommendations, and to make improvements in your security posture.</span></span>

<span data-ttu-id="cae0c-124">หมายเหตุ: Azure AD สนับสนุนข้อมูลประจำตัวภายนอกที่อนุญาตให้ผู้ใช้ที่ไม่มีบัญชี Microsoft สามารถลงชื่อเข้าใช้แอปพลิเคชันและทรัพยากรของพวกเขาด้วยข้อมูลประจำตัวภายนอกได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-124">Note: Azure AD supports external identities that allow users without a Microsoft account to sign in to their applications and resources with their external identity.</span></span>

- [<span data-ttu-id="cae0c-125">การเช่าใน Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="cae0c-125">Tenancy in Azure Active Directory</span></span>](/azure/active-directory/develop/single-and-multi-tenant-apps)

- [<span data-ttu-id="cae0c-126">วิธีการสร้างและกำหนดค่าอินสแตนซ์ Azure AD</span><span class="sxs-lookup"><span data-stu-id="cae0c-126">How to create and configure an Azure AD instance</span></span>](/azure/active-directory/fundamentals/active-directory-access-create-new-tenant)

- [<span data-ttu-id="cae0c-127">ใช้ผู้ให้บริการข้อมูลเอกลักษณ์ภายนอกสำหรับแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="cae0c-127">Use external identity providers for application</span></span>](/azure/active-directory/b2b/identity-providers)

- [<span data-ttu-id="cae0c-128">คะแนนความปลอดภัยของข้อมูลเอกลักษณ์ใน Azure Active Directory คืออะไร</span><span class="sxs-lookup"><span data-stu-id="cae0c-128">What is the identity secure score in Azure Active Directory</span></span>](/azure/active-directory/fundamentals/identity-secure-score)

<span data-ttu-id="cae0c-129">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-129">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-130">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-130">**Responsibility**: Customer</span></span>

### <a name="im-2-manage-application-identities-securely-and-automatically"></a><span data-ttu-id="cae0c-131">IM-2: จัดการข้อมูลเอกลักษณ์ของแอปพลิเคชันอย่างปลอดภัยและโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cae0c-131">IM-2: Manage application identities securely and automatically</span></span>

<span data-ttu-id="cae0c-132">**คำแนะนำ**: Power BI และ Power BI Embedded สนับสนุนการใช้องค์ประกอบหลักของบริการ</span><span class="sxs-lookup"><span data-stu-id="cae0c-132">**Guidance**: Power BI and Power BI Embedded support the use of Service Principals.</span></span> <span data-ttu-id="cae0c-133">จัดเก็บข้อมูลประจำตัวขององค์ประกอบหลักของบริการที่ใช้สำหรับเข้ารหัสหรือเข้าถึง Power BI ใน Key Vault กำหนดนโยบายการเข้าถึงที่เหมาะสมให้กับห้องนิรภัย (Vault) และตรวจสอบสิทธิ์การเข้าถึงอย่างสม่ำเสมอ</span><span class="sxs-lookup"><span data-stu-id="cae0c-133">Store any Service Principal credentials used for encrypting or accessing Power BI in a Key Vault, assign proper access policies to the vault and regularly review access permissions.</span></span>

<span data-ttu-id="cae0c-134">ทำให้พื้นที่ทำงานและชุดข้อมูลระดับ Premium ทำงานโดยอัตโนมัติด้วยองค์ประกอบหลักของบริการ https://docs.microsoft.com/power-bi/admin/service-premium-service-principal</span><span class="sxs-lookup"><span data-stu-id="cae0c-134">Automate Premium workspace and dataset tasks with service principals https://docs.microsoft.com/power-bi/admin/service-premium-service-principal</span></span>

<span data-ttu-id="cae0c-135">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-135">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-136">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-136">**Responsibility**: Customer</span></span>

### <a name="im-3-use-azure-ad-single-sign-on-sso-for-application-access"></a><span data-ttu-id="cae0c-137">IM-3: ใช้ลงชื่อเข้าระบบครั้งเดียว (single sign-on : SSO) ของ Azure AD สำหรับการเข้าถึงแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="cae0c-137">IM-3: Use Azure AD single sign-on (SSO) for application access</span></span>

<span data-ttu-id="cae0c-138">**คำแนะนำ**: Power BI ใช้ Azure Active Directory เพื่อจัดเตรียมข้อมูลเอกลักษณ์และการจัดการการเข้าถึงทรัพยากร Azure แอปพลิเคชันระบบคลาวด์ และแอปพลิเคชันภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="cae0c-138">**Guidance**: Power BI uses Azure Active Directory to provide identity and access management to Azure resources, cloud applications, and on-premises applications.</span></span> <span data-ttu-id="cae0c-139">ซึ่งรวมถึงข้อมูลเอกลักษณ์ขององค์กร เช่น พนักงาน ตลอดจนข้อมูลเอกลักษณ์ภายนอก เช่น คู่ค้า ผู้ขาย และซัพพลายเออร์</span><span class="sxs-lookup"><span data-stu-id="cae0c-139">This includes enterprise identities such as employees, as well as external identities such as partners, vendors, and suppliers.</span></span> <span data-ttu-id="cae0c-140">ซึ่งเป็นการเปิดใช้งานการลงชื่อเข้าระบบครั้งเดียว (SSO) เพื่อจัดการและรักษาความปลอดภัยการเข้าถึงข้อมูลและทรัพยากรขององค์กรของคุณภายในองค์กรและในระบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="cae0c-140">This enables single sign-on (SSO) to manage and secure access to your organization’s data and resources on-premises and in the cloud.</span></span> <span data-ttu-id="cae0c-141">เชื่อมต่อผู้ใช้ แอปพลิเคชัน และอุปกรณ์ทั้งหมดของคุณกับ Azure AD เพื่อการเข้าถึงที่ราบรื่น ปลอดภัย และความสามารถในการมองเห็นและการควบคุมที่ดีขึ้น</span><span class="sxs-lookup"><span data-stu-id="cae0c-141">Connect all your users, applications, and devices to the Azure AD for seamless, secure access and greater visibility and control.</span></span>

- [<span data-ttu-id="cae0c-142">ทำความเข้าใจ SSO สำหรับแอปพลิเคชันด้วย Azure AD</span><span class="sxs-lookup"><span data-stu-id="cae0c-142">Understand Application SSO with Azure AD</span></span>](/azure/active-directory/manage-apps/what-is-single-sign-on)

<span data-ttu-id="cae0c-143">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-143">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-144">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-144">**Responsibility**: Customer</span></span>

### <a name="im-4-use-strong-authentication-controls-for-all-azure-active-directory-based-access"></a><span data-ttu-id="cae0c-145">IM-4: ใช้ตัวควบคุมการรับรองความถูกต้องที่เข้มงวดสำหรับการเข้าถึงที่ใช้ Azure Active Directory ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="cae0c-145">IM-4: Use strong authentication controls for all Azure Active Directory based access</span></span>

<span data-ttu-id="cae0c-146">**คำแนะนำ**: Power BI ถูกรวมเข้ากับ Azure AD ที่สนับสนุนตัวควบคุมการรับรองความถูกต้องที่เข้มงวดผ่านการรับรองความถูกต้องโดยใช้หลายปัจจัย (MFA) และวิธีการแบบไม่ใช้รหัสผ่านที่เข้มงวด</span><span class="sxs-lookup"><span data-stu-id="cae0c-146">**Guidance**: Power BI is integrated with Azure AD that supports strong authentication controls through multi-factor authentication (MFA), and strong passwordless methods.</span></span>
- <span data-ttu-id="cae0c-147">การรับรองความถูกต้องโดยใช้หลายปัจจัย - เปิดใช้งาน Azure AD MFA และปฏิบัติตามคำแนะนำ Azure Security Center Identity และ Access Management สำหรับแนวทางปฏิบัติที่ดีที่สุดบางประการในการตั้งค่า MFA ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cae0c-147">Multi-factor authentication - Enable Azure AD MFA and follow Azure Security Center Identity and Access Management recommendations for some best practices in your MFA setup.</span></span> <span data-ttu-id="cae0c-148">คุณสามารถบังคับใช้ MFA ได้กับทุกคน เลือกผู้ใช้หรือในระดับต่อผู้ใช้ตามเงื่อนไขการลงชื่อเข้าใช้และปัจจัยความเสี่ยง</span><span class="sxs-lookup"><span data-stu-id="cae0c-148">MFA can be enforced on all, select users or at the per-user level based on sign-in conditions and risk factors.</span></span>
- <span data-ttu-id="cae0c-149">การรับรองความถูกต้องแบบไม่ใช้รหัสผ่าน - ตัวเลือกการรับรองความถูกต้องแบบไม่ใช้รหัสผ่านมีให้เลือกสามแบบ Windows Hello for Business, แอป Microsoft Authenticator และวิธีวิธีการรับรองความถูกต้องในองค์กร เช่น สมาร์ทการ์ด</span><span class="sxs-lookup"><span data-stu-id="cae0c-149">Passwordless authentication – Three passwordless authentication options are available: Windows Hello for Business, Microsoft Authenticator app, and on-premises authentication methods such as smart cards.</span></span>

<span data-ttu-id="cae0c-150">สำหรับผู้ดูแลระบบและผู้ใช้ที่มีสิทธิ์พิเศษ ตรวจสอบให้แน่ใจว่ามีการใช้การรับรองความถูกต้องที่เข้มงวดระดับสูงสุด ตามด้วยการนำนโยบายการรับรองความถูกต้องที่เข้มงวดและเหมาะสมไปใช้กับผู้ใช้รายอื่น</span><span class="sxs-lookup"><span data-stu-id="cae0c-150">For administrator and privileged users, ensure the highest level of strong authentication is used, followed by rolling out the appropriate strong authentication policy to other users.</span></span>

<span data-ttu-id="cae0c-151">หมายเหตุ: คุณสามารถบังคับใช้ MFA สำหรับบัญชีผู้ใช้ที่เปิดใช้งานใน Azure AD เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="cae0c-151">Note: MFA can only be enforced for user accounts enabled in Azure AD.</span></span> <span data-ttu-id="cae0c-152">องค์ประกอบหลักของบริการของ Power BI ไม่สนับสนุนการใช้งาน MFA</span><span class="sxs-lookup"><span data-stu-id="cae0c-152">Power BI Service Principals do not support the use of MFA.</span></span>

- [<span data-ttu-id="cae0c-153">วิธีเปิดใช้งาน MFA ใน Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-153">How to enable MFA in Azure</span></span>](/azure/active-directory/authentication/howto-mfa-getstarted)

- [<span data-ttu-id="cae0c-154">บทนำเกี่ยวกับตัวเลือกการรับรองความถูกต้องโดยไม่ใช้รหัสผ่านสำหรับ Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="cae0c-154">Introduction to passwordless authentication options for Azure Active Directory</span></span>](/azure/active-directory/authentication/concept-authentication-passwordless)

<span data-ttu-id="cae0c-155">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-155">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-156">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-156">**Responsibility**: Customer</span></span>

### <a name="im-5-monitor-and-alert-on-account-anomalies"></a><span data-ttu-id="cae0c-157">IM-5: ตรวจสอบและแจ้งเตือนเกี่ยวกับความผิดปกติของบัญชี</span><span class="sxs-lookup"><span data-stu-id="cae0c-157">IM-5: Monitor and alert on account anomalies</span></span>

<span data-ttu-id="cae0c-158">**คำแนะนำ**: กำหนดนโยบายการตรวจจับความผิดปกติใน Microsoft Cloud App Security ที่สามารถกำหนดขอบเขตได้อย่างอิสระ เพื่อที่จะปรับใช้เฉพาะกับผู้ใช้และกลุ่มที่คุณต้องการรวม</span><span class="sxs-lookup"><span data-stu-id="cae0c-158">**Guidance**: Define anomaly detection policies in Microsoft Cloud App Security which can be independently scoped, so that they apply to only the users and groups that you want to include.</span></span> <span data-ttu-id="cae0c-159">นโยบายการตรวจจับความผิดปกติเหล่านี้สามารถช่วยตรวจหาและตรวจสอบความผิดปกติของพฤติกรรมที่เกี่ยวข้องกับผู้ใช้ที่เข้าถึงและใช้ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-159">These anomaly detection policies can help detect and monitor behavior anomalies related to users accessing and using Power BI.</span></span>

- [<span data-ttu-id="cae0c-160">ใช้ตัวควบคุม Microsoft Cloud App Security ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-160">Using Microsoft Cloud App Security Controls in Power BI</span></span>](../admin/service-security-using-microsoft-cloud-app-security-controls.md)

<span data-ttu-id="cae0c-161">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-161">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-162">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-162">**Responsibility**: Customer</span></span>

### <a name="im-6-restrict-azure-resource-access-based-on-conditions"></a><span data-ttu-id="cae0c-163">IM-6: จำกัดการเข้าถึงทรัพยากร Azure โดยยึดตามเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="cae0c-163">IM-6: Restrict Azure resource access based on conditions</span></span>

<span data-ttu-id="cae0c-164">**คำแนะนำ**: Power BI สนับสนุนการเข้าถึงแบบมีเงื่อนไขของ Azure AD สำหรับการควบคุมการเข้าถึงที่ละเอียดยิ่งขึ้นตามเงื่อนไขที่ผู้ใช้กำหนด เช่น การเข้าสู่ระบบของผู้ใช้จากช่วง IP บางช่วงจะต้องใช้ MFA สำหรับการเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="cae0c-164">**Guidance**: Power BI supports Azure AD conditional access for a more granular access control based on user-defined conditions, such as user logins from certain IP ranges will need to use MFA for login.</span></span> <span data-ttu-id="cae0c-165">นโยบายการจัดการเซสชันการรับรองความถูกต้องแบบละเอียดยังสามารถใช้สำหรับกรณีการใช้งานที่แตกต่างกันอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="cae0c-165">Granular authentication session management policy can also be used for different use cases.</span></span>

- [<span data-ttu-id="cae0c-166">ภาพรวมการเข้าถึงแบบมีเงื่อนไขของ Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-166">Azure conditional access overview</span></span>](/azure/active-directory/conditional-access/overview)

- [<span data-ttu-id="cae0c-167">นโยบายการเข้าถึงแบบมีเงื่อนไขทั่วไป</span><span class="sxs-lookup"><span data-stu-id="cae0c-167">Common conditional access policies</span></span>](/azure/active-directory/conditional-access/concept-conditional-access-policy-common)

- [<span data-ttu-id="cae0c-168">กำหนดค่าการจัดการเซสชันการรับรองความถูกต้องด้วยการเข้าถึงแบบมีเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="cae0c-168">Configure authentication session management with conditional access</span></span>](/azure/active-directory/conditional-access/howto-conditional-access-session-lifetime)

- [<span data-ttu-id="cae0c-169">ใช้ตัวควบคุม Microsoft Cloud App Security ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-169">Using Microsoft Cloud App Security Controls in Power BI</span></span>](../admin/service-security-using-microsoft-cloud-app-security-controls.md)

<span data-ttu-id="cae0c-170">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-170">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-171">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-171">**Responsibility**: Customer</span></span>

### <a name="im-7-eliminate-unintended-credential-exposure"></a><span data-ttu-id="cae0c-172">IM-7: กำจัดการเปิดเผยข้อมูลประจำตัวโดยไม่ได้ตั้งใจ</span><span class="sxs-lookup"><span data-stu-id="cae0c-172">IM-7: Eliminate unintended credential exposure</span></span>

<span data-ttu-id="cae0c-173">**คำแนะนำ**: สำหรับแอปพลิเคชันแบบฝังตัวของ Power BI ขอแนะนำให้ติดตั้งเครื่องสแกนข้อมูลประจำตัว (Credential Scanner) เพื่อระบุข้อมูลประจำตัวภายในโค้ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="cae0c-173">**Guidance**: For Power BI embedded applications it is recommended to implement Credential Scanner to identify credentials within your code.</span></span> <span data-ttu-id="cae0c-174">นอกจากนี้ เครื่องสแกนข้อมูลประจำตัวจะสนับสนุนให้ย้ายข้อมูลประจำตัวที่ค้นพบไปยังตำแหน่งที่ปลอดภัยมากขึ้น เช่น Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="cae0c-174">Credential Scanner will also encourage moving discovered credentials to more secure locations such as Azure Key Vault.</span></span>

<span data-ttu-id="cae0c-175">จัดเก็บคีย์การเข้ารหัสหรือข้อมูลประจำตัวขององค์ประกอบหลักของบริการที่ใช้สำหรับเข้ารหัสหรือเข้าถึง Power BI ใน Key Vault กำหนดนโยบายการเข้าถึงที่เหมาะสมให้กับห้องนิรภัย (Vault) และตรวจสอบสิทธิ์การเข้าถึงอย่างสม่ำเสมอ</span><span class="sxs-lookup"><span data-stu-id="cae0c-175">Store any encryption keys or Service Principal credentials used for encrypting or accessing Power BI in a Key Vault, assign proper access policies to the vault and regularly review access permissions.</span></span>
 
<span data-ttu-id="cae0c-176">สำหรับ GitHub คุณสามารถใช้คุณลักษณะการสแกนข้อมูลลับแบบเนทีฟเพื่อระบุข้อมูลประจำตัวหรือข้อมูลลับรูปแบบอื่น ๆ ภายในโค้ด</span><span class="sxs-lookup"><span data-stu-id="cae0c-176">For GitHub, you can use native secret scanning feature to identify credentials or other form of secrets within the code.</span></span>

- [<span data-ttu-id="cae0c-177">นำคีย์การเข้ารหัสลับของคุณเองมาใช้กับ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-177">Bring your own encryption keys for Power BI</span></span>](../admin/service-encryption-byok.md)

 
<span data-ttu-id="cae0c-178">วิธีการตั้งค่าข้อมูลประจำตัว</span><span class="sxs-lookup"><span data-stu-id="cae0c-178">How to set up Credential</span></span>
- [<span data-ttu-id="cae0c-179">เครื่องสแกน</span><span class="sxs-lookup"><span data-stu-id="cae0c-179">Scanner</span></span>](https://secdevtools.azurewebsites.net/helpcredscan.html) 

- [<span data-ttu-id="cae0c-180">การสแกนข้อมูลลับของ GitHub</span><span class="sxs-lookup"><span data-stu-id="cae0c-180">GitHub secret scanning</span></span>](https://docs.github.com/github/administering-a-repository/about-secret-scanning)

<span data-ttu-id="cae0c-181">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-181">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-182">**ความรับผิดชอบ**: แชร์</span><span class="sxs-lookup"><span data-stu-id="cae0c-182">**Responsibility**: Shared</span></span>

## <a name="privileged-access"></a><span data-ttu-id="cae0c-183">การเข้าถึงที่มีสิทธิ์พิเศษ</span><span class="sxs-lookup"><span data-stu-id="cae0c-183">Privileged Access</span></span>

<span data-ttu-id="cae0c-184">*สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Azure Security Benchmark: การเข้าถึงที่มีสิทธิ์พิเศษ](/azure/security/benchmarks/security-controls-v2-privileged-access)*</span><span class="sxs-lookup"><span data-stu-id="cae0c-184">*For more information, see the [Azure Security Benchmark: Privileged Access](/azure/security/benchmarks/security-controls-v2-privileged-access).*</span></span>

### <a name="pa-1-protect-and-limit-highly-privileged-users"></a><span data-ttu-id="cae0c-185">PA-1: ป้องกันและจำกัดผู้ใช้ที่มีสิทธิ์พิเศษสูง</span><span class="sxs-lookup"><span data-stu-id="cae0c-185">PA-1: Protect and limit highly privileged users</span></span>

<span data-ttu-id="cae0c-186">**คำแนะนำ**: เพื่อลดความเสี่ยงและปฏิบัติตามหลักการของสิทธิ์พิเศษน้อยที่สุด เราขอแนะนำให้คงความเป็นสมาชิกของผู้ดูแลระบบ Power BI ไว้กับคนจำนวนน้อย</span><span class="sxs-lookup"><span data-stu-id="cae0c-186">**Guidance**: To reduce risk and follow the principle of least privilege, it is recommended to keep membership of the Power BI administrators to a small number of people.</span></span> <span data-ttu-id="cae0c-187">ผู้ใช้ที่มีสิทธิ์พิเศษเหล่านี้อาจสามารถเข้าถึงและปรับเปลี่ยนคุณลักษณะการจัดการทั้งหมดสำหรับองค์กรได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-187">Users with these privileged permissions could potentially access and modify all any management feature for the organization.</span></span> <span data-ttu-id="cae0c-188">ผู้ดูแลระบบส่วนกลางมีสิทธิ์ของผู้ดูแลระบบในบริการ Power BI โดยปริยายเช่นกันผ่าน Microsoft 365 หรือ Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="cae0c-188">Global administrators, via Microsoft 365 or Azure Active Directory, implicitly possess administrator rights in the Power BI service as well.</span></span>

<span data-ttu-id="cae0c-189">Power BI มีบัญชีผู้ใช้ที่มีสิทธิ์พิเศษสูงด้านล่าง:</span><span class="sxs-lookup"><span data-stu-id="cae0c-189">Power BI has below highly privileged accounts:</span></span>
- <span data-ttu-id="cae0c-190">ผู้ดูแลระบบส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="cae0c-190">Global admin</span></span>
- <span data-ttu-id="cae0c-191">ผู้ดูแลการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="cae0c-191">Billing admin</span></span>
- <span data-ttu-id="cae0c-192">ผู้ดูแลสิทธิการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cae0c-192">License admin</span></span>
- <span data-ttu-id="cae0c-193">ผู้ดูแลระบบผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="cae0c-193">User admin</span></span>
- <span data-ttu-id="cae0c-194">ผู้ดูแลระบบ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-194">Power BI admin</span></span>
- <span data-ttu-id="cae0c-195">ผู้ดูแลระบบ Power BI Premium Capacity</span><span class="sxs-lookup"><span data-stu-id="cae0c-195">Power BI Premium Capacity admin</span></span>
- <span data-ttu-id="cae0c-196">ผู้ดูแลระบบ Power BI Embedded Capacity</span><span class="sxs-lookup"><span data-stu-id="cae0c-196">Power BI Embedded Capacity admin</span></span>

<span data-ttu-id="cae0c-197">Power BI สนับสนุนนโยบายเซสชันใน Azure AD เพื่อเปิดใช้งานนโยบายการเข้าถึงแบบมีเงื่อนไขและเซสชันเส้นทางที่ใช้ใน Power BI ผ่านทางบริการของ Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="cae0c-197">Power BI supports session policies in Azure AD to enable conditional access policies and route sessions used in Power BI through the Cloud App Security service.</span></span>

<span data-ttu-id="cae0c-198">เปิดใช้งานการเข้าถึงที่มีสิทธิ์พิเศษแบบทันเวลาพอดี (JIT) สำหรับบัญชีผู้ดูแลระบบ Power BI โดยใช้การจัดการการเข้าถึงที่มีสิทธิ์พิเศษ M365</span><span class="sxs-lookup"><span data-stu-id="cae0c-198">Enable just-in-time (JIT) privileged access for the Power BI admin accounts using M365 Privileged access management.</span></span>

- [<span data-ttu-id="cae0c-199">บทบาทผู้ดูแลระบบที่เกี่ยวข้องกับ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-199">Administrator roles related to Power BI</span></span>](../admin/service-admin-administering-power-bi-in-your-organization.md#administrator-roles-related-to-power-bi)

- [<span data-ttu-id="cae0c-200">การจัดการการเข้าถึงที่มีสิทธิ์พิเศษ M365</span><span class="sxs-lookup"><span data-stu-id="cae0c-200">M365 Privileged Access Management</span></span>](/microsoft-365/compliance/privileged-access-management-overview?amp;preserve-view=true&view=o365-worldwide)

- [<span data-ttu-id="cae0c-201">ตัวควบคุม Cloud App Security ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-201">Cloud App Security controls in Power BI</span></span>](../admin/service-security-using-microsoft-cloud-app-security-controls.md)

<span data-ttu-id="cae0c-202">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-202">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-203">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-203">**Responsibility**: Customer</span></span>

### <a name="pa-2-restrict-administrative-access-to-business-critical-systems"></a><span data-ttu-id="cae0c-204">PA-2: จำกัดการเข้าถึงระบบที่สำคัญทางธุรกิจด้วยระดับผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="cae0c-204">PA-2: Restrict administrative access to business-critical systems</span></span>

<span data-ttu-id="cae0c-205">**คำแนะนำ**: จำกัดจำนวนบัญชีที่มีสิทธิ์พิเศษสูงหรือบทบาทที่มีการเข้าถึง Power BI แบบยกระดับ</span><span class="sxs-lookup"><span data-stu-id="cae0c-205">**Guidance**: Limit the number of highly-privileged accounts or roles with elevated access to Power BI.</span></span>

<span data-ttu-id="cae0c-206">คุณสามารถเปิดใช้งานการเข้าถึงที่มีสิทธิ์พิเศษแบบทันเวลาพอดี (JIT) โดยใช้คำแนะนำการจัดการการเข้าถึงที่มีสิทธิ์พิเศษ M365 [ที่นี่](/microsoft-365/compliance/privileged-access-management-overview?amp;preserve-view=true&view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="cae0c-206">You can enable just-in-time (JIT) privileged access using the M365 Privileged access management guidance [here](/microsoft-365/compliance/privileged-access-management-overview?amp;preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="cae0c-207">คุณสามารถดูรายละเอียดเพิ่มเติมได้ที่หน้า 183 ของเอกสารการปรับใช้ Power BI Enterprise [ที่นี่](https://aka.ms/PBIEnterpriseDeploymentWP)</span><span class="sxs-lookup"><span data-stu-id="cae0c-207">Additional details can be found on page 183 of the Power BI Enterprise Deployment document [here](https://aka.ms/PBIEnterpriseDeploymentWP).</span></span>

<span data-ttu-id="cae0c-208">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-208">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-209">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-209">**Responsibility**: Customer</span></span>

### <a name="pa-3-review-and-reconcile-user-access-regularly"></a><span data-ttu-id="cae0c-210">PA-3: ตรวจทานและสร้างความสอดคล้องให้กับการเข้าถึงของผู้ใช้อย่างสม่ำเสมอ</span><span class="sxs-lookup"><span data-stu-id="cae0c-210">PA-3: Review and reconcile user access regularly</span></span>

<span data-ttu-id="cae0c-211">**คำแนะนำ**: ในฐานะผู้ดูแลระบบบริการ Power BI คุณสามารถวิเคราะห์การใช้งานสำหรับทรัพยากร Power BI ทั้งหมดที่ระดับผู้เช่าโดยใช้รายงานแบบกำหนดเองโดยยึดตามบันทึกกิจกรรมของ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-211">**Guidance**: As a Power BI service admin, you can analyze usage for all Power BI resources at the tenant level by using custom reports based on the Power BI activity log.</span></span> <span data-ttu-id="cae0c-212">คุณสามารถดาวน์โหลดกิจกรรมโดยใช้ REST API หรือ PowerShell cmdlet</span><span class="sxs-lookup"><span data-stu-id="cae0c-212">You can download the activities by using a REST API or PowerShell cmdlet.</span></span> <span data-ttu-id="cae0c-213">คุณยังสามารถกรองข้อมูลกิจกรรมตามช่วงวันที่ ผู้ใช้และประเภทกิจกรรมได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-213">You can also filter the activity data by date range, user, and activity type.</span></span>

<span data-ttu-id="cae0c-214">คุณต้องตรงตามข้อกำหนดเหล่านี้เพื่อเข้าถึงบันทึกกิจกรรมของ Power BI:</span><span class="sxs-lookup"><span data-stu-id="cae0c-214">You must meet these requirements to access the Power BI activity log:</span></span>
- <span data-ttu-id="cae0c-215">คุณต้องเป็นผู้ดูแลระบบส่วนกลางหรือผู้ดูแลระบบบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-215">You must either be a global admin or a Power BI service admin.</span></span>
- <span data-ttu-id="cae0c-216">คุณได้ติดตั้ง [cmdlets การจัดการ Power BI](https://www.powershellgallery.com/packages/MicrosoftPowerBIMgmt) ไว้ในเครื่องหรือใช้ cmdlets การจัดการ Power BI ใน Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="cae0c-216">You have installed the [Power BI Management cmdlets](https://www.powershellgallery.com/packages/MicrosoftPowerBIMgmt) locally or use the Power BI Management cmdlets in Azure Cloud Shell.</span></span>

<span data-ttu-id="cae0c-217">เมื่อตรงตามข้อกำหนดเหล่านี้แล้ว คุณสามารถทำตามคำแนะนำด้านล่างเพื่อติดตามกิจกรรมของผู้ใช้ภายใน Power BI:</span><span class="sxs-lookup"><span data-stu-id="cae0c-217">Once these requirements are met you can follow the guidance below to track user activity within Power BI:</span></span>

- [<span data-ttu-id="cae0c-218">ติดตามกิจกรรมผู้ใช้ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-218">Track users activity in Power BI</span></span>](../admin/service-admin-auditing.md)

<span data-ttu-id="cae0c-219">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-219">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-220">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-220">**Responsibility**: Customer</span></span>

### <a name="pa-4-set-up-emergency-access-in-azure-ad"></a><span data-ttu-id="cae0c-221">PA-4: ตั้งค่าการเข้าถึงฉุกเฉินใน Azure AD</span><span class="sxs-lookup"><span data-stu-id="cae0c-221">PA-4: Set up emergency access in Azure AD</span></span>

<span data-ttu-id="cae0c-222">**คำแนะนำ**: Power BI ถูกรวมเข้ากับ Azure Active Directory และ M365 เพื่อจัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="cae0c-222">**Guidance**: Power BI is integrated with Azure Active Directory and M365 to manage its resources.</span></span> <span data-ttu-id="cae0c-223">เพื่อป้องกันการถูกล็อกจากผู้เช่า M365 หรือองค์กร Azure AD โดยไม่ได้ตั้งใจ ให้ตั้งค่าบัญชีการเข้าถึงฉุกเฉินสำหรับการเข้าถึงเมื่อไม่สามารถใช้บัญชีผู้ดูแลระบบปกติได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-223">To prevent being accidentally locked out of your M365 tenant, or Azure AD organization, set up an emergency access account for access when normal administrative accounts cannot be used.</span></span> <span data-ttu-id="cae0c-224">บัญชีการเข้าถึงฉุกเฉินมักมีสิทธิ์พิเศษสูง และไม่ควรกำหนดให้กับบุคคลใดบุคคลหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cae0c-224">Emergency access accounts are usually highly privileged, and they should not be assigned to specific individuals.</span></span> <span data-ttu-id="cae0c-225">บัญชีการเข้าถึงฉุกเฉินถูกจำกัดไว้ในสถานการณ์ฉุกเฉินหรือ "กระจกแตก" ซึ่งไม่สามารถใช้บัญชีดูแลระบบปกติได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-225">Emergency access accounts are limited to emergency or "break glass"' scenarios where normal administrative accounts can't be used.</span></span>

<span data-ttu-id="cae0c-226">คุณควรตรวจสอบให้แน่ใจว่าข้อมูลประจำตัว (เช่น รหัสผ่าน ใบรับรอง หรือสมาร์ทการ์ด) สำหรับบัญชีการเข้าถึงฉุกเฉินนั้นปลอดภัยและเป็นที่รู้กันเฉพาะบุคคลที่ได้รับอนุญาตให้ใช้ในกรณีฉุกเฉินเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="cae0c-226">You should ensure that the credentials (such as password, certificate, or smart card) for emergency access accounts are kept secure and known only to individuals who are authorized to use them only in an emergency.</span></span>

- [<span data-ttu-id="cae0c-227">จัดการบัญชีการเข้าถึงฉุกเฉินใน Azure AD</span><span class="sxs-lookup"><span data-stu-id="cae0c-227">Manage emergency access accounts in Azure AD</span></span>](/azure/active-directory/users-groups-roles/directory-emergency-access)

- [<span data-ttu-id="cae0c-228">ปกป้องบัญชี M365 ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cae0c-228">Protect your M365 accounts</span></span>](/microsoft-365/campaigns/m365-campaigns-protect-admin-accounts)

<span data-ttu-id="cae0c-229">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-229">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-230">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-230">**Responsibility**: Customer</span></span>

### <a name="pa-6-use-privileged-access-workstations"></a><span data-ttu-id="cae0c-231">PA-6: ใช้เวิร์กสเตชันการเข้าถึงที่มีสิทธิ์พิเศษ</span><span class="sxs-lookup"><span data-stu-id="cae0c-231">PA-6: Use privileged access workstations</span></span>

<span data-ttu-id="cae0c-232">**คำแนะนำ**: เวิร์กสเตชันที่ปลอดภัยและแยกต่างหากมีความสำคัญอย่างยิ่งสำหรับการรักษาความปลอดภัยของบทบาทที่ละเอียดอ่อน เช่น ผู้ดูแลระบบ นักพัฒนา และผู้ให้บริการที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="cae0c-232">**Guidance**: Secured, isolated workstations are critically important for the security of sensitive roles like administrators, developers, and critical service operators.</span></span> <span data-ttu-id="cae0c-233">ใช้เวิร์กสเตชันของผู้ใช้ที่มีความปลอดภัยสูงและ/หรือ Azure Bastion สำหรับงานการดูแลระบบที่เกี่ยวข้องกับการจัดการ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-233">Use highly secured user workstations and/or Azure Bastion for administrative tasks related to managing Power BI.</span></span> <span data-ttu-id="cae0c-234">ใช้ Azure Active Directory, Microsoft Defender Advanced Threat Protection (ATP) และ/หรือ Microsoft Intune เพื่อปรับใช้เวิร์กสเตชันผู้ใช้ที่ปลอดภัยและมีการจัดการสำหรับงานด้านการดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="cae0c-234">Use Azure Active Directory, Microsoft Defender Advanced Threat Protection (ATP), and/or Microsoft Intune to deploy a secure and managed user workstation for administrative tasks.</span></span> <span data-ttu-id="cae0c-235">เวิร์กสเตชันที่ปลอดภัยสามารถจัดการได้จากส่วนกลางเพื่อบังคับใช้การกำหนดค่าที่ปลอดภัยรวมถึงการรับรองความถูกต้องที่แข็งแกร่ง ข้อมูลพื้นฐานด้านซอฟต์แวร์และฮาร์ดแวร์ การเข้าถึงแบบลอจิคัลและเครือข่ายที่ จำกัด</span><span class="sxs-lookup"><span data-stu-id="cae0c-235">The secured workstations can be centrally managed to enforce secured configuration including strong authentication, software and hardware baselines, restricted logical and network access.</span></span>

<span data-ttu-id="cae0c-236">ทำความเข้าใจการเข้าถึงที่มีสิทธิ์พิเศษ</span><span class="sxs-lookup"><span data-stu-id="cae0c-236">Understand privileged access</span></span>
- [<span data-ttu-id="cae0c-237">เวิร์กสเตชัน</span><span class="sxs-lookup"><span data-stu-id="cae0c-237">workstations</span></span>](/azure/active-directory/devices/concept-azure-managed-workstation)

- [<span data-ttu-id="cae0c-238">ปรับใช้เวิร์กสเตชันการเข้าถึงที่มีสิทธิ์พิเศษ</span><span class="sxs-lookup"><span data-stu-id="cae0c-238">Deploy a privileged access workstation</span></span>](/azure/active-directory/devices/howto-azure-managed-workstation)

<span data-ttu-id="cae0c-239">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-239">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-240">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-240">**Responsibility**: Customer</span></span>

## <a name="data-protection"></a><span data-ttu-id="cae0c-241">การป้องกันข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cae0c-241">Data Protection</span></span>

<span data-ttu-id="cae0c-242">*สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Azure Security Benchmark: การป้องกันข้อมูล](/azure/security/benchmarks/security-controls-v2-data-protection)*</span><span class="sxs-lookup"><span data-stu-id="cae0c-242">*For more information, see the [Azure Security Benchmark: Data Protection](/azure/security/benchmarks/security-controls-v2-data-protection).*</span></span>

### <a name="dp-1-discovery-classify-and-label-sensitive-data"></a><span data-ttu-id="cae0c-243">DP-1: การค้นพบ การจัดประเภท และการติดป้ายชื่อข้อมูลที่ละเอียดอ่อน</span><span class="sxs-lookup"><span data-stu-id="cae0c-243">DP-1: Discovery, classify and label sensitive data</span></span>

<span data-ttu-id="cae0c-244">**คำแนะนำ**: ใช้ป้ายชื่อระดับความลับของ Microsoft Information Protection กับรายงาน แดชบอร์ด ชุดข้อมูล และกระแสข้อมูลเพื่อป้องกันเนื้อหาที่สำคัญของคุณจากการเข้าถึงข้อมูลที่ไม่ได้รับอนุญาตและการรั่วไหล</span><span class="sxs-lookup"><span data-stu-id="cae0c-244">**Guidance**: Use Microsoft Information Protection sensitivity labels on your reports, dashboards, datasets, and dataflows to guard your sensitive content against unauthorized data access and leakage.</span></span>

<span data-ttu-id="cae0c-245">ใช้ป้ายชื่อระดับความลับของ Microsoft Information Protection เพื่อจัดประเภทและติดป้ายกำกับรายงาน แดชบอร์ด ชุดข้อมูล และกระแสข้อมูลในบริการ Power BI และเพื่อปกป้องเนื้อหาที่ละเอียดอ่อนของคุณจากการเข้าถึงข้อมูลโดยไม่ได้รับอนุญาตและการรั่วไหลเมื่อเนื้อหาถูกส่งออกจากบริการ Power BI ไปยังไฟล์ Excel, PowerPoint และ PDF</span><span class="sxs-lookup"><span data-stu-id="cae0c-245">Use Microsoft Information Protection sensitivity labels to classify and label your reports, dashboards, datasets, and dataflows in Power BI service and to protect your sensitive content from unauthorized data access and leakage when content is exported from Power BI service to Excel, PowerPoint and PDF files.</span></span>

- [<span data-ttu-id="cae0c-246">วิธีการใช้ป้ายชื่อระดับความลับใน Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-246">How to apply sensitivity labels in Power BI</span></span>](../admin/service-security-apply-data-sensitivity-labels.md)

<span data-ttu-id="cae0c-247">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-247">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-248">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-248">**Responsibility**: Customer</span></span>

### <a name="dp-2-protect-sensitive-data"></a><span data-ttu-id="cae0c-249">DP-2: ปกป้องข้อมูลที่ละเอียดอ่อน</span><span class="sxs-lookup"><span data-stu-id="cae0c-249">DP-2: Protect sensitive data</span></span>

<span data-ttu-id="cae0c-250">**คำแนะนำ**: Power BI ผสานรวมป้ายชื่อระดับความลับของ Microsoft Information Protection สำหรับการปกป้องข้อมูลที่ละเอียดอ่อน</span><span class="sxs-lookup"><span data-stu-id="cae0c-250">**Guidance**: Power BI integrates with Microsoft Information Protection sensitivity labels for sensitive data protection.</span></span> <span data-ttu-id="cae0c-251">สำหรับรายละเอียดเพิ่มเติมโปรดดู[ป้ายชื่อระดับความลับ Microsoft Information Protection ใน Power BI](../admin/service-security-sensitivity-label-overview.md)</span><span class="sxs-lookup"><span data-stu-id="cae0c-251">For more details see [Microsoft Information Protection sensitivity labels in Power BI](../admin/service-security-sensitivity-label-overview.md)</span></span>

<span data-ttu-id="cae0c-252">Power BI ช่วยให้ผู้ใช้บริการสามารถนำคีย์ของตนเองมาใช้เพื่อปกป้องข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-252">Power BI allows service users to bring their own key to protect data at rest.</span></span> <span data-ttu-id="cae0c-253">สำหรับรายละเอียดเพิ่มเติม โปรดดู[นำคีย์การเข้ารหัสลับของคุณเองมาใช้กับ Power BI](../admin/service-encryption-byok.md)</span><span class="sxs-lookup"><span data-stu-id="cae0c-253">For more details see [Bring your own encryption keys for Power BI](../admin/service-encryption-byok.md)</span></span>

<span data-ttu-id="cae0c-254">ลูกค้ามีตัวเลือกในการเก็บแหล่งข้อมูลไว้ภายในองค์กรและใช้ประโยชน์จาก Direct Query หรือ Live Connect ด้วยเกตเวย์ข้อมูลในองค์กรเพื่อลดการเปิดเผยข้อมูลไปยังบริการคลาวด์</span><span class="sxs-lookup"><span data-stu-id="cae0c-254">Customers have the option to keep data sources on-premise and leverage Direct Query or Live Connect with an on-premise data gateway to minimize data exposure to the cloud service.</span></span> <span data-ttu-id="cae0c-255">สำหรับรายละเอียดเพิ่มเติม โปรดดูที่[เกตเวย์ข้อมูลภายในองค์กรคืออะไร](/data-integration/gateway/service-gateway-onprem)</span><span class="sxs-lookup"><span data-stu-id="cae0c-255">For more details see [What is an on-premises data gateway?](/data-integration/gateway/service-gateway-onprem)</span></span>

<span data-ttu-id="cae0c-256">Power BI สนับสนุนความปลอดภัยระดับแถว</span><span class="sxs-lookup"><span data-stu-id="cae0c-256">Power BI supports Row Level Security.</span></span> <span data-ttu-id="cae0c-257">สำหรับรายละเอียดเพิ่มเติม โปรดดูที่[การรักษาความปลอดภัยระดับแถว (RLS) ด้วย Power BI](../admin/service-admin-rls.md)</span><span class="sxs-lookup"><span data-stu-id="cae0c-257">For more details see [Row-level security (RLS) with Power BI](../admin/service-admin-rls.md).</span></span> <span data-ttu-id="cae0c-258">โปรดทราบว่าคุณสามารถใช้งาน RLS ได้แม้กระทั่งกับแหล่งข้อมูล Direct Query ซึ่งในกรณีนี้ไฟล์ PBIX จะทำหน้าที่เป็นการรักษาความปลอดภัยที่เปิดใช้งานพร็อกซี</span><span class="sxs-lookup"><span data-stu-id="cae0c-258">Note that RLS can be applied even to Direct Query data sources in which case PBIX file acts as a security enabling proxy.</span></span>

<span data-ttu-id="cae0c-259">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-259">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-260">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-260">**Responsibility**: Customer</span></span>

### <a name="dp-3-monitor-for-unauthorized-transfer-of-sensitive-data"></a><span data-ttu-id="cae0c-261">DP-3: ตรวจสอบการถ่ายโอนข้อมูลที่ละเอียดอ่อนโดยไม่ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="cae0c-261">DP-3: Monitor for unauthorized transfer of sensitive data</span></span>

<span data-ttu-id="cae0c-262">**คำแนะนำ**: ตัวควบคุมนี้สามารถทำได้เพียงบางส่วนโดยใช้การสนับสนุน Microsoft Cloud App Security สำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-262">**Guidance**: This control can be partially achieved by using Microsoft Cloud App Security support for Power BI.</span></span>

<span data-ttu-id="cae0c-263">ด้วยการใช้ Cloud App Security กับ Power BI คุณสามารถช่วยปกป้องรายงาน ข้อมูล และบริการของ Power BI มิให้รั่วไหลโดยไม่ได้ตั้งใจหรือมิให้ถูกละเมิด</span><span class="sxs-lookup"><span data-stu-id="cae0c-263">Using Cloud App Security with Power BI, you can help protect your Power BI reports, data, and services from unintended leaks or breaches.</span></span> <span data-ttu-id="cae0c-264">ด้วย Cloud App Security คุณสามารถสร้างนโยบายการเข้าถึงตามเงื่อนไขสำหรับข้อมูลขององค์กรโดยใช้ตัวควบคุมเซสชันแบบเรียลไทม์ใน Azure Active Directory (Azure AD) ซึ่งช่วยให้มั่นใจได้ว่าการวิเคราะห์ Power BI ของคุณมีความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="cae0c-264">With Cloud App Security, you create conditional access policies for your organization’s data, using real-time session controls in Azure Active Directory (Azure AD), that help to ensure your Power BI analytics are secure.</span></span> <span data-ttu-id="cae0c-265">หลังจากที่มีการกำหนดนโยบายเหล่านี้ ผู้ดูแลระบบสามารถตรวจสอบการเข้าถึงและกิจกรรมของผู้ใช้ ทำการวิเคราะห์ความเสี่ยงแบบเรียลไทม์ และตั้งค่าตัวควบคุมเฉพาะป้ายชื่อได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-265">Once these policies have been set, administrators can monitor user access and activity, perform real-time risk analysis, and set label-specific controls.</span></span>

<span data-ttu-id="cae0c-266">การใช้ </span><span class="sxs-lookup"><span data-stu-id="cae0c-266">Using</span></span>
- [<span data-ttu-id="cae0c-267">ตัวควบคุม Microsoft Cloud App Security ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-267">Microsoft Cloud App Security controls in Power BI</span></span>](../admin/service-security-using-microsoft-cloud-app-security-controls.md)

<span data-ttu-id="cae0c-268">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-268">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-269">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-269">**Responsibility**: Customer</span></span>

### <a name="dp-4-encrypt-sensitive-information-in-transit"></a><span data-ttu-id="cae0c-270">DP-4: เข้ารหัสข้อมูลที่ละเอียดอ่อนระหว่างการส่งผ่าน</span><span class="sxs-lookup"><span data-stu-id="cae0c-270">DP-4: Encrypt sensitive information in transit</span></span>

<span data-ttu-id="cae0c-271">**คำแนะนำ**: ตรวจสอบการรับส่งข้อมูล HTTP ว่าไคลเอ็นต์และแหล่งข้อมูลใดก็ตามที่เชื่อมต่อกับทรัพยากร Power BI ของคุณสามารถเจรจา TLS v1.2 หรือสูงกว่าได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-271">**Guidance**: Ensure for HTTP traffic, that any clients and data sources connecting to your Power BI resources can negotiate TLS v1.2 or greater.</span></span>

- [<span data-ttu-id="cae0c-272">บังคับใช้รุ่น TLS</span><span class="sxs-lookup"><span data-stu-id="cae0c-272">Enforcing TLS version usage</span></span>](../admin/service-admin-power-bi-security.md#enforcing-tls-version-usage)

- [<span data-ttu-id="cae0c-273">ข้อมูลเกี่ยวกับการรักษาความปลอดภัย TLS</span><span class="sxs-lookup"><span data-stu-id="cae0c-273">Information on TLS Security</span></span>](/security/engineering/solving-tls1-problem)

<span data-ttu-id="cae0c-274">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-274">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-275">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-275">**Responsibility**: Customer</span></span>

### <a name="dp-5-encrypt-sensitive-data-at-rest"></a><span data-ttu-id="cae0c-276">DP-5: เข้ารหัสข้อมูลที่ละเอียดอ่อนในขณะพัก</span><span class="sxs-lookup"><span data-stu-id="cae0c-276">DP-5: Encrypt sensitive data at rest</span></span>

<span data-ttu-id="cae0c-277">**คำแนะนำ**: Power BI เข้ารหัสข้อมูลที่พักอยู่และในระหว่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="cae0c-277">**Guidance**: Power BI encrypts data at rest and in process.</span></span> <span data-ttu-id="cae0c-278">ตามค่าเริ่มต้น Power BI ใช้คีย์ที่จัดการโดย Microsoft เพื่อเข้ารหัสลับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="cae0c-278">By default, Power BI uses Microsoft-managed keys to encrypt your data.</span></span> <span data-ttu-id="cae0c-279">องค์กรสามารถเลือกใช้คีย์ของตนเองเพื่อเข้ารหัสเนื้อหาของผู้ใช้ในทั้งหมดใน Power BI จากภาพรายงานเพื่อนำเข้าชุดข้อมูลในความจุแบบพรีเมียมได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-279">Organizations can choose to use their own keys for encryption of user content at rest across Power BI, from report images to imported datasets in Premium capacities.</span></span>

- [<span data-ttu-id="cae0c-280">ใช้นำคีย์ของคุณเองมาใช้เองใน Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-280">Use bring-your-own-key in Power BI</span></span>](../admin/service-encryption-byok.md)

<span data-ttu-id="cae0c-281">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-281">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-282">**ความรับผิดชอบ**: แชร์</span><span class="sxs-lookup"><span data-stu-id="cae0c-282">**Responsibility**: Shared</span></span>

## <a name="asset-management"></a><span data-ttu-id="cae0c-283">การจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="cae0c-283">Asset Management</span></span>

<span data-ttu-id="cae0c-284">*สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Azure Security Benchmark: การจัดการสินทรัพย์](/azure/security/benchmarks/security-controls-v2-asset-management)*</span><span class="sxs-lookup"><span data-stu-id="cae0c-284">*For more information, see the [Azure Security Benchmark: Asset Management](/azure/security/benchmarks/security-controls-v2-asset-management).*</span></span>

### <a name="am-1-ensure-security-team-has-visibility-into-risks-for-assets"></a><span data-ttu-id="cae0c-285">AM-1: ตรวจสอบให้แน่ใจว่าทีมรักษาความปลอดภัยสามารถมองเห็นความเสี่ยงของสินทรัพย์ได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-285">AM-1: Ensure security team has visibility into risks for assets</span></span>

<span data-ttu-id="cae0c-286">**คำแนะนำ**: ใช้ Azure Sentinel กับบันทึกการตรวจสอบ Power BI Office ของคุณเพื่อให้แน่ใจว่าทีมรักษาความปลอดภัยของคุณสามารถมองเห็นความเสี่ยงสำหรับสินทรัพย์ของ Power BI ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-286">**Guidance**: Use Azure Sentinel with your Power BI Office Audit logs to ensure your security team has visibility into risks for your Power BI assets.</span></span>

- [<span data-ttu-id="cae0c-287">เชื่อมต่อบันทึก Office 365 กับ Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="cae0c-287">Connect Office 365 Logs to Azure Sentinel</span></span>](/azure/sentinel/connect-office-365)

<span data-ttu-id="cae0c-288">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-288">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-289">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-289">**Responsibility**: Customer</span></span>

### <a name="am-2-ensure-security-team-has-access-to-asset-inventory-and-metadata"></a><span data-ttu-id="cae0c-290">AM-2: ตรวจสอบว่าทีมรักษาความปลอดภัยสามารถเข้าถึงคลังสินทรัพย์และเมตาดาต้าได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-290">AM-2: Ensure security team has access to asset inventory and metadata</span></span>

<span data-ttu-id="cae0c-291">**คำแนะนำ**: ตรวจสอบให้แน่ใจว่าทีมรักษาความปลอดภัยสามารถเข้าถึงคลังที่อัปเดตอย่างต่อเนื่องของทรัพยากร Power BI Embedded ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="cae0c-291">**Guidance**: Ensure that security teams have access to a continuously updated inventory of Power BI Embedded resources.</span></span> <span data-ttu-id="cae0c-292">ทีมรักษาความปลอดภัยมักต้องคลังนี้เพื่อประเมินความเสี่ยงที่อาจเกิดขึ้นของการจัดการและเป็นข้อมูลป้อนเข้าในการปรับปรุงความปลอดภัยอย่างต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="cae0c-292">Security teams often need this inventory to evaluate their organization's potential exposure to emerging risks, and as an input to continuously security improvements.</span></span> 

<span data-ttu-id="cae0c-293">Azure Resource Graph สามารถคิวรีและค้นหาทรัพยากร Power BI Embedded ทั้งหมดในการสมัครใช้งานของคุณ</span><span class="sxs-lookup"><span data-stu-id="cae0c-293">Azure Resource Graph can query for and discover all Power BI Embedded resources in your subscriptions.</span></span>  

<span data-ttu-id="cae0c-294">จัดระเบียบสินทรัพย์อย่างมีเหตุผลตามการจัดหมวดหมู่ขององค์กรของคุณโดยใช้แท็กรวมถึงเมตาดาต้าอื่น ๆ ใน Azure (ชื่อ คำอธิบาย และหมวดหมู่)</span><span class="sxs-lookup"><span data-stu-id="cae0c-294">Logically organize assets according to your organization’s taxonomy using Tags as well as other metadata in Azure (Name, Description, and Category).</span></span>  

- [<span data-ttu-id="cae0c-295">วิธีสร้างคิวรีด้วย Azure Resource Graph Explorer</span><span class="sxs-lookup"><span data-stu-id="cae0c-295">How to create queries with Azure Resource Graph Explorer</span></span>](/azure/governance/resource-graph/first-query-portal)

- [<span data-ttu-id="cae0c-296">คู่มือการตัดสินใจสำหรับการตั้งชื่อและการติดแท็ก</span><span class="sxs-lookup"><span data-stu-id="cae0c-296">Resource naming and tagging decision guide</span></span>](/azure/cloud-adoption-framework/decision-guides/resource-tagging/?toc=%2fazure%2fazure-resource-manager%2fmanagement%2ftoc.json)

<span data-ttu-id="cae0c-297">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-297">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-298">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-298">**Responsibility**: Customer</span></span>

### <a name="am-3-use-only-approved-azure-services"></a><span data-ttu-id="cae0c-299">AM-3: ใช้เฉพาะบริการ Azure ที่ได้รับการอนุมัติเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="cae0c-299">AM-3: Use only approved Azure services</span></span>

<span data-ttu-id="cae0c-300">**คำแนะนำ**: Power BI สนับสนุนการปรับใช้ที่ใช้ Azure Resource Manager สำหรับ Power BI Embedded และคุณสามารถจำกัดการปรับใช้ทรัพยากรผ่านนโยบาย Azure โดยใช้ข้อกำหนดนโยบายที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="cae0c-300">**Guidance**: Power BI supports Azure Resource Manager-based deployments for Power BI Embedded, and you are able to restrict the deploying of its resources via Azure Policy using a custom Policy definition.</span></span>

<span data-ttu-id="cae0c-301">ใช้นโยบาย Azure เพื่อตรวจสอบและจำกัดบริการที่ผู้ใช้สามารถจัดเตรียมได้ในสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="cae0c-301">Use Azure Policy to audit and restrict which services users can provision in your environment.</span></span> <span data-ttu-id="cae0c-302">ใช้ Azure Resource Graph เพื่อคิวรีและค้นหาทรัพยากรภายในการสมัครใช้งานของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="cae0c-302">Use Azure Resource Graph to query for and discover resources within their subscriptions.</span></span> <span data-ttu-id="cae0c-303">คุณยังสามารถใช้ Azure Monitor เพื่อสร้างกฎสำหรับทริกเกอร์การแจ้งเตือนเมื่อตรวจพบบริการที่ไม่ได้รับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="cae0c-303">You can also use Azure Monitor to create rules to trigger alerts when a non-approved service is detected.</span></span>

- [<span data-ttu-id="cae0c-304">วิธีการกำหนดค่าและจัดการนโยบาย Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-304">How to configure and manage Azure Policy</span></span>](/azure/governance/policy/tutorials/create-and-manage)

<span data-ttu-id="cae0c-305">วิธีการปฏิเสธชนิดทรัพยากรที่ระบุด้วย</span><span class="sxs-lookup"><span data-stu-id="cae0c-305">How to deny a specific resource type with</span></span>
- [<span data-ttu-id="cae0c-306">นโยบายของ Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-306">Azure Policy</span></span>](/azure/governance/policy/samples/built-in-policies#general)

<span data-ttu-id="cae0c-307">วิธีการสร้างคิวรีด้วย Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-307">How to create queries with Azure</span></span>
- [<span data-ttu-id="cae0c-308">ตัวสำรวจกราฟของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="cae0c-308">Resource Graph Explorer</span></span>](/azure/governance/resource-graph/first-query-portal)

<span data-ttu-id="cae0c-309">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-309">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-310">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-310">**Responsibility**: Customer</span></span>

## <a name="logging-and-threat-detection"></a><span data-ttu-id="cae0c-311">การบันทึกและการตรวจหาภัยคุกคาม</span><span class="sxs-lookup"><span data-stu-id="cae0c-311">Logging and Threat Detection</span></span>

<span data-ttu-id="cae0c-312">*สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Azure Security Benchmark: การบันทึกและการตรวจหาภัยคุกคาม](/azure/security/benchmarks/security-controls-v2-logging-threat-detection)*</span><span class="sxs-lookup"><span data-stu-id="cae0c-312">*For more information, see the [Azure Security Benchmark: Logging and Threat Detection](/azure/security/benchmarks/security-controls-v2-logging-threat-detection).*</span></span>

### <a name="lt-2-enable-threat-detection-for-azure-identity-and-access-management"></a><span data-ttu-id="cae0c-313">LT-2: เปิดใช้งานการตรวจจับภัยคุกคามสำหรับข้อมูลเอกลักษณ์ Azure และการจัดการการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="cae0c-313">LT-2: Enable threat detection for Azure identity and access management</span></span>

<span data-ttu-id="cae0c-314">**คำแนะนำ**: ส่งต่อบันทึกใดก็ตามจาก Power BI ไปยัง SIEM ของคุณซึ่งสามารถใช้เพื่อตั้งค่าการตรวจจับภัยคุกคามที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="cae0c-314">**Guidance**: Forward any logs from Power BI to your SIEM which can be used to set up custom threat detections.</span></span> <span data-ttu-id="cae0c-315">นอกจากนี้ใช้ตัวควบคุม Microsoft Cloud App Security (MCAS) ใน Power BI เพื่อเปิดใช้งานการตรวจหาความผิดปกติโดยใช้คำแนะนำ[ที่นี่](../admin/service-security-using-microsoft-cloud-app-security-controls.md)</span><span class="sxs-lookup"><span data-stu-id="cae0c-315">Additionally, use Microsoft Cloud App Security (MCAS) controls in Power BI to enable anomaly detection using the guide [here](../admin/service-security-using-microsoft-cloud-app-security-controls.md).</span></span>

- [<span data-ttu-id="cae0c-316">ติดตามกิจกรรมของผู้ใช้ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-316">Track user activities in Power BI</span></span>](../admin/service-admin-auditing.md)

<span data-ttu-id="cae0c-317">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-317">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-318">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-318">**Responsibility**: Customer</span></span>

### <a name="lt-3-enable-logging-for-azure-network-activities"></a><span data-ttu-id="cae0c-319">LT-3: เปิดใช้งานการบันทึกสำหรับกิจกรรมเครือข่าย Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-319">LT-3: Enable logging for Azure network activities</span></span>

<span data-ttu-id="cae0c-320">**คำแนะนำ**: Power BI เป็นข้อเสนอ SaaS ที่มีการจัดการโดยสมบูรณ์และการกำหนดค่าเครือข่ายพื้นฐานและการบันทึกถือเป็นความรับผิดชอบของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="cae0c-320">**Guidance**: Power BI is a fully managed SaaS offering and the underlying network configuration and logging is Microsoft’s responsibility.</span></span> <span data-ttu-id="cae0c-321">สำหรับลูกค้าที่ใช้ประโยชน์จากลิงก์ส่วนตัวจะมีการบันทึกและการตรวจสอบบางอย่างที่สามารถกำหนดค่าได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-321">For customers utilizing Private Links some logging and monitoring is available that can be configured.</span></span>

- [<span data-ttu-id="cae0c-322">การบันทึกและการตรวจสอบลิงก์ส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="cae0c-322">Private Link logging and monitoring</span></span>](/azure/private-link/private-link-overview#logging-and-monitoring)

<span data-ttu-id="cae0c-323">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-323">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-324">**ความรับผิดชอบ**: แชร์</span><span class="sxs-lookup"><span data-stu-id="cae0c-324">**Responsibility**: Shared</span></span>

### <a name="lt-4-enable-logging-for-azure-resources"></a><span data-ttu-id="cae0c-325">LT-4: เปิดใช้งานการบันทึกสำหรับทรัพยากร Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-325">LT-4: Enable logging for Azure resources</span></span>

<span data-ttu-id="cae0c-326">**คำแนะนำ**: เมื่อใช้ Power BI คุณมีสองตัวเลือกในการติดตามกิจกรรมของผู้ใช้: บันทึกกิจกรรมของ Power BI และบันทึกการตรวจสอบแบบรวม</span><span class="sxs-lookup"><span data-stu-id="cae0c-326">**Guidance**: With Power BI, you have two options to track user activity: The Power BI activity log and the unified audit log.</span></span> <span data-ttu-id="cae0c-327">บันทึกเหล่านี้ทั้งคู่ประกอบด้วยสำเนาทั้งหมดของข้อมูลการตรวจสอบ Power BI แต่มีความแตกต่างที่สำคัญหลายอย่างตามที่สรุปด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="cae0c-327">These logs both contain a complete copy of the Power BI auditing data, but there are several key differences, as summarized below.</span></span>
 
<span data-ttu-id="cae0c-328">บันทึกการตรวจสอบแบบรวม:</span><span class="sxs-lookup"><span data-stu-id="cae0c-328">Unified Audit Log:</span></span>

 
- <span data-ttu-id="cae0c-329">รวมเหตุการณ์จาก SharePoint Online, Exchange Online, Dynamics 365 และบริการอื่น ๆ นอกเหนือจากเหตุการณ์การตรวจสอบ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-329">Includes events from SharePoint    Online, Exchange Online, Dynamics 365, and other services in addition to    the Power BI auditing events.</span></span>

 
- <span data-ttu-id="cae0c-330">เฉพาะผู้ใช้ที่มีสิทธิ์ในการบันทึกการตรวจสอบหรือบันทึกการตรวจสอบแบบดูเท่านั้นที่สามารถเข้าถึงได้ เช่น ผู้ดูแลระบบและผู้สอบบัญชีส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="cae0c-330">Only users with View-Only Audit    Logs or Audit Logs permissions have access, such as global admins and    auditors.</span></span>

 
- <span data-ttu-id="cae0c-331">ผู้ดูแลระบบส่วนกลางและผู้ตรวจสอบสามารถค้นหาบันทึกการตรวจสอบแบบรวมได้โดยใช้ศูนย์การรักษาความปลอดภัย Microsoft 365 และศูนย์การปฏิบัติตามข้อบังคับ Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cae0c-331">Global admins and auditors can    search the unified audit log by using the Microsoft 365 Security Center    and the Microsoft 365 Compliance Center.</span></span>

 
- <span data-ttu-id="cae0c-332">ผู้ดูแลระบบส่วนกลางและผู้ตรวจสอบสามารถดาวน์โหลดรายการบันทึกการตรวจสอบได้โดยใช้ API การจัดการของ Microsoft 365 และ cmdlets</span><span class="sxs-lookup"><span data-stu-id="cae0c-332">Global admins and auditors can    download audit log entries by using Microsoft 365 Management APIs and    cmdlets.</span></span>

 
- <span data-ttu-id="cae0c-333">เก็บข้อมูลการตรวจสอบเป็นเวลา 90 วัน</span><span class="sxs-lookup"><span data-stu-id="cae0c-333">Keeps audit data for 90 days.</span></span>

 
- <span data-ttu-id="cae0c-334">เก็บรักษาข้อมูลการตรวจสอบแม้ว่าผู้เช่าจะถูกย้ายไปยังภูมิภาค Azure อื่นก็ตาม</span><span class="sxs-lookup"><span data-stu-id="cae0c-334">Retains audit data, even if the    tenant is moved to a different Azure region.</span></span>
 
<span data-ttu-id="cae0c-335">บันทึกกิจกรรม Power BI:</span><span class="sxs-lookup"><span data-stu-id="cae0c-335">Power BI Activity Log:</span></span>

 
- <span data-ttu-id="cae0c-336">รวมเฉพาะเหตุการณ์การตรวจสอบ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-336">Includes only the Power BI auditing events.</span></span>

 
 
- <span data-ttu-id="cae0c-337">ผู้ดูแลระบบส่วนกลางและผู้ดูแลระบบบริการของ Power BI มีสิทธิ์เข้าถึง</span><span class="sxs-lookup"><span data-stu-id="cae0c-337">Global admins and Power BI service admins    have access.</span></span>

 
- <span data-ttu-id="cae0c-338">ยังไม่มีอินเทอร์เฟซผู้ใช้ในการค้นหาบันทึกกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="cae0c-338">There's    no user interface to search the activity log yet.</span></span>

 
- <span data-ttu-id="cae0c-339">ผู้ดูแลระบบส่วนกลางและผู้ดูแลระบบบริการของ Power BI สามารถดาวน์โหลดบันทึกรายการกิจกรรมโดยใช้ Power BI REST API และ cmdlet การจัดการ</span><span class="sxs-lookup"><span data-stu-id="cae0c-339">Global    admins and Power BI service admins can download activity log entries by    using a Power BI REST API and management cmdlet.</span></span>

 
- <span data-ttu-id="cae0c-340">เก็บข้อมูลกิจกรรมเป็นเวลา 30 วัน</span><span class="sxs-lookup"><span data-stu-id="cae0c-340">Keeps    activity data for 30 days.</span></span>

 
- <span data-ttu-id="cae0c-341">ไม่เก็บรักษาข้อมูลการตรวจสอบเมื่อผู้เช่าถูกย้ายไปยังภูมิภาค Azure อื่น</span><span class="sxs-lookup"><span data-stu-id="cae0c-341">Doesn't    retain activity data when the tenant is moved to a different Azure region.</span></span>

- [<span data-ttu-id="cae0c-342">ข้อมูลการตรวจสอบ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-342">Power BI Auditing data</span></span>](../admin/service-admin-auditing.md#operations-available-in-the-audit-and-activity-logs)

- [<span data-ttu-id="cae0c-343">บันทึกกิจกรรม Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-343">Power BI Activity Log</span></span>](../admin/service-admin-auditing.md#use-the-activity-log)

- [<span data-ttu-id="cae0c-344">บันทึกการตรวจสอบ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-344">Power BI Audit Log</span></span>](../admin/service-admin-auditing.md#use-the-audit-log)

<span data-ttu-id="cae0c-345">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-345">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-346">**ความรับผิดชอบ**: แชร์</span><span class="sxs-lookup"><span data-stu-id="cae0c-346">**Responsibility**: Shared</span></span>

### <a name="lt-5-centralize-security-log-management-and-analysis"></a><span data-ttu-id="cae0c-347">LT-5: รวมศูนย์การจัดการและการวิเคราะห์บันทึกความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="cae0c-347">LT-5: Centralize security log management and analysis</span></span>

<span data-ttu-id="cae0c-348">**คำแนะนำ**: Power BI รวมศูนย์บันทึกสองส่วน: บันทึกกิจกรรม Power BI และบันทึกการตรวจสอบแบบรวม</span><span class="sxs-lookup"><span data-stu-id="cae0c-348">**Guidance**: Power BI, centralizes logs in two places: the Power BI activity log and the unified audit log.</span></span> <span data-ttu-id="cae0c-349">บันทึกเหล่านี้ทั้งคู่ประกอบด้วยสำเนาทั้งหมดของข้อมูลการตรวจสอบ Power BI แต่มีความแตกต่างที่สำคัญหลายอย่างตามที่สรุปด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="cae0c-349">These logs both contain a complete copy of the Power BI auditing data, but there are several key differences, as summarized below.</span></span>
 

<span data-ttu-id="cae0c-350">บันทึกการตรวจสอบแบบรวม:</span><span class="sxs-lookup"><span data-stu-id="cae0c-350">Unified Audit Log:</span></span>

- <span data-ttu-id="cae0c-351">รวมเหตุการณ์จาก SharePoint Online, Exchange Online, Dynamics 365 และบริการอื่นๆ นอกเหนือจากเหตุการณ์การตรวจสอบ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-351">Includes events from SharePoint Online, Exchange Online, Dynamics 365, and other services in addition to the Power BI auditing events.</span></span>

- <span data-ttu-id="cae0c-352">เฉพาะผู้ใช้ที่มีสิทธิ์ในการบันทึกการตรวจสอบหรือบันทึกการตรวจสอบแบบดูเท่านั้นที่สามารถเข้าถึงได้ เช่น ผู้ดูแลระบบและผู้สอบบัญชีส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="cae0c-352">Only users with View-Only Audit Logs or Audit Logs permissions have access, such as global admins and auditors.</span></span>

- <span data-ttu-id="cae0c-353">ผู้ดูแลระบบส่วนกลางและผู้ตรวจสอบสามารถค้นหาบันทึกการตรวจสอบแบบรวมได้โดยใช้ศูนย์การรักษาความปลอดภัย Microsoft 365 และศูนย์การปฏิบัติตามข้อบังคับ Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cae0c-353">Global admins and auditors can search the unified audit log by using the Microsoft 365 Security Center and the Microsoft 365 Compliance Center.</span></span>

- <span data-ttu-id="cae0c-354">ผู้ดูแลระบบส่วนกลางและผู้ตรวจสอบสามารถดาวน์โหลดรายการบันทึกการตรวจสอบได้โดยใช้ API การจัดการของ Microsoft 365 และ cmdlets</span><span class="sxs-lookup"><span data-stu-id="cae0c-354">Global admins and auditors can download audit log entries by using Microsoft 365 Management APIs and cmdlets.</span></span>

- <span data-ttu-id="cae0c-355">เก็บข้อมูลการตรวจสอบเป็นเวลา 90 วัน</span><span class="sxs-lookup"><span data-stu-id="cae0c-355">Keeps audit data for 90 days.</span></span>

- <span data-ttu-id="cae0c-356">เก็บรักษาข้อมูลการตรวจสอบแม้ว่าผู้เช่าจะถูกย้ายไปยังภูมิภาค Azure อื่นก็ตาม</span><span class="sxs-lookup"><span data-stu-id="cae0c-356">Retains audit data, even if the tenant is moved to a different Azure region.</span></span>

 

<span data-ttu-id="cae0c-357">บันทึกกิจกรรม Power BI:</span><span class="sxs-lookup"><span data-stu-id="cae0c-357">Power BI Activity Log:</span></span>

- <span data-ttu-id="cae0c-358">รวมเฉพาะเหตุการณ์การตรวจสอบ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-358">Includes only the Power BI auditing events.</span></span>

- <span data-ttu-id="cae0c-359">ผู้ดูแลระบบส่วนกลางและผู้ดูแลระบบบริการของ Power BI มีสิทธิ์เข้าถึง</span><span class="sxs-lookup"><span data-stu-id="cae0c-359">Global admins and Power BI service admins have access.</span></span>

- <span data-ttu-id="cae0c-360">ยังไม่มีอินเทอร์เฟซผู้ใช้ในการค้นหาบันทึกกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="cae0c-360">There's no user interface to search the activity log yet.</span></span>

- <span data-ttu-id="cae0c-361">ผู้ดูแลระบบส่วนกลางและผู้ดูแลระบบบริการของ Power BI สามารถดาวน์โหลดบันทึกรายการกิจกรรมโดยใช้ Power BI REST API และ cmdlet การจัดการ</span><span class="sxs-lookup"><span data-stu-id="cae0c-361">Global admins and Power BI service admins can download activity log entries by using a Power BI REST API and management cmdlet.</span></span>

- <span data-ttu-id="cae0c-362">เก็บข้อมูลกิจกรรมเป็นเวลา 30 วัน</span><span class="sxs-lookup"><span data-stu-id="cae0c-362">Keeps activity data for 30 days.</span></span>

- <span data-ttu-id="cae0c-363">ไม่เก็บรักษาข้อมูลการตรวจสอบเมื่อผู้เช่าถูกย้ายไปยังภูมิภาค Azure อื่น</span><span class="sxs-lookup"><span data-stu-id="cae0c-363">Doesn't retain activity data when the tenant is moved to a different Azure region.</span></span>

- [<span data-ttu-id="cae0c-364">ข้อมูลการตรวจสอบ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-364">Power BI Auditing data</span></span>](../admin/service-admin-auditing.md#operations-available-in-the-audit-and-activity-logs)

- [<span data-ttu-id="cae0c-365">บันทึกกิจกรรม Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-365">Power BI Activity Log</span></span>](../admin/service-admin-auditing.md#use-the-activity-log)

- [<span data-ttu-id="cae0c-366">บันทึกการตรวจสอบ Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-366">Power BI Audit Log</span></span>](../admin/service-admin-auditing.md#use-the-audit-log)

<span data-ttu-id="cae0c-367">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-367">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-368">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-368">**Responsibility**: Customer</span></span>

### <a name="lt-6-configure-log-storage-retention"></a><span data-ttu-id="cae0c-369">LT-6: กำหนดค่าการเก็บรักษาพื้นที่เก็บข้อมูลบันทึก</span><span class="sxs-lookup"><span data-stu-id="cae0c-369">LT-6: Configure log storage retention</span></span>

<span data-ttu-id="cae0c-370">**คำแนะนำ**: กำหนดค่านโยบายการเก็บรักษาพื้นที่เก็บข้อมูลของคุณสำหรับบันทึกการตรวจสอบของ Office ของคุณตามการปฏิบัติตามกฎระเบียบ ข้อบังคับ และข้อกำหนดทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="cae0c-370">**Guidance**: Configure your storage retention policies for your Office Audit logs according to your compliance, regulation, and business requirements.</span></span>

- [<span data-ttu-id="cae0c-371">นโยบายการเก็บรักษาข้อมูลบันทึกการตรวจสอบของ Office</span><span class="sxs-lookup"><span data-stu-id="cae0c-371">Office Audit Log Retention Policies</span></span>](/microsoft-365/compliance/audit-log-retention-policies)

<span data-ttu-id="cae0c-372">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-372">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-373">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-373">**Responsibility**: Customer</span></span>

## <a name="incident-response"></a><span data-ttu-id="cae0c-374">การตอบสนองเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="cae0c-374">Incident Response</span></span>

<span data-ttu-id="cae0c-375">*สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Azure Security Benchmark: การตอบสนองเหตุการณ์](/azure/security/benchmarks/security-controls-v2-incident-response)*</span><span class="sxs-lookup"><span data-stu-id="cae0c-375">*For more information, see the [Azure Security Benchmark: Incident Response](/azure/security/benchmarks/security-controls-v2-incident-response).*</span></span>

### <a name="ir-1-preparation--update-incident-response-process-for-azure"></a><span data-ttu-id="cae0c-376">IR-1: การเตรียมการ - อัปเดตกระบวนการตอบสนองต่อเหตุการณ์สำหรับ Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-376">IR-1: Preparation – update incident response process for Azure</span></span>

<span data-ttu-id="cae0c-377">**คำแนะนำ**: ตรวจสอบให้แน่ใจว่าองค์กรของคุณมีกระบวนการในการตอบสนองต่อเหตุการณ์ด้านความปลอดภัย อัปเดตกระบวนการเหล่านี้สำหรับ Azure และมีการฝึกซ้อมเป็นประจำเพื่อให้แน่ใจว่ามีความพร้อม</span><span class="sxs-lookup"><span data-stu-id="cae0c-377">**Guidance**: Ensure your organization has processes to respond to security incidents, has updated these processes for Azure, and is regularly exercising them to ensure readiness.</span></span>

- [<span data-ttu-id="cae0c-378">นำการรักษาความปลอดภัยมาใช้ในสภาพแวดล้อมขององค์กร</span><span class="sxs-lookup"><span data-stu-id="cae0c-378">Implement security across the enterprise environment</span></span>](/azure/cloud-adoption-framework/security/security-top-10#4-process-update-incident-response-ir-processes-for-cloud)

- [<span data-ttu-id="cae0c-379">คู่มืออ้างอิงสำหรับการตอบสนองต่อเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="cae0c-379">Incident response reference guide</span></span>](/microsoft-365/downloads/IR-Reference-Guide.pdf)

<span data-ttu-id="cae0c-380">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-380">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-381">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-381">**Responsibility**: Customer</span></span>

### <a name="ir-2-preparation--setup-incident-notification"></a><span data-ttu-id="cae0c-382">IR-2: การเตรียมการ - ตั้งค่าการแจ้งเตือนเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="cae0c-382">IR-2: Preparation – setup incident notification</span></span>

<span data-ttu-id="cae0c-383">**คำแนะนำ**: ตั้งค่าข้อมูลติดต่อสำหรับเหตุการณ์ด้านความปลอดภัยใน Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="cae0c-383">**Guidance**: Set up security incident contact information in Azure Security Center.</span></span> <span data-ttu-id="cae0c-384">ข้อมูลที่ติดต่อนี้ถูกใช้โดย Microsoft เพื่อติดต่อคุณถ้าศูนย์ตอบสนองความปลอดภัยของ Microsoft (MSRC) พบว่าข้อมูลของคุณถูกเข้าถึงโดยบุคคลที่ผิดกฎหมายหรือไม่ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="cae0c-384">This contact information is used by Microsoft to contact you if the Microsoft Security Response Center (MSRC) discovers that your data has been accessed by an unlawful or unauthorized party.</span></span> <span data-ttu-id="cae0c-385">นอกจากนี้คุณยังมีตัวเลือกในการปรับแต่งการแจ้งเตือนเหตุการณ์ และการแจ้งเตือนในบริการ Azure ที่แตกต่างกันตามความต้องการในการตอบสนองต่อเหตุการณ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cae0c-385">You also have options to customize incident alert and notification in different Azure services based on your incident response needs.</span></span> 

- [<span data-ttu-id="cae0c-386">วิธีการตั้งค่าผู้ติดต่อด้านความปลอดภัยของ Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="cae0c-386">How to set the Azure Security Center security contact</span></span>](/azure/security-center/security-center-provide-security-contact-details)

<span data-ttu-id="cae0c-387">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-387">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-388">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-388">**Responsibility**: Customer</span></span>

### <a name="ir-3-detection-and-analysis--create-incidents-based-on-high-quality-alerts"></a><span data-ttu-id="cae0c-389">IR-3: การตรวจจับและวิเคราะห์ - สร้างเหตุการณ์ตามการแจ้งเตือนคุณภาพสูง</span><span class="sxs-lookup"><span data-stu-id="cae0c-389">IR-3: Detection and analysis – create incidents based on high quality alerts</span></span>

<span data-ttu-id="cae0c-390">**คำแนะนำ**: ตรวจสอบว่าคุณมีกระบวนการสร้างการแจ้งเตือนคุณภาพสูง และวัดคุณภาพของการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="cae0c-390">**Guidance**: Ensure you have a process to create high-quality alerts and measure the quality of alerts.</span></span> <span data-ttu-id="cae0c-391">ซึ่งช่วยให้คุณสามารถเรียนรู้บทเรียนจากเหตุการณ์ที่ผ่านมา และจัดลำดับความสำคัญการแจ้งเตือนสำหรับนักวิเคราะห์เพื่อไม่ให้พวกเขาต้องเสียเวลากับผลบวกที่ผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="cae0c-391">This allows you to learn lessons from past incidents and prioritize alerts for analysts, so they don’t waste time on false positives.</span></span>

<span data-ttu-id="cae0c-392">ตรวจสอบการแจ้งเตือนที่เกี่ยวข้องกับ Power BI ใน Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="cae0c-392">Monitor alerts related to Power BI in Microsoft Cloud App Security.</span></span> <span data-ttu-id="cae0c-393">การแจ้งเตือนคุณภาพสูงอาจเกิดขึ้นตามประสบการณ์จากเหตุการณ์ในอดีต แหล่งที่มาของชุมชนที่ผ่านการตรวจสอบแล้ว และเครื่องมือที่ออกแบบมาเพื่อสร้างและล้างการแจ้งเตือนโดยการหลอมรวมและเชื่อมโยงแหล่งสัญญาณที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="cae0c-393">High-quality alerts can be built based on experience from past incidents, validated community sources, and tools designed to generate and clean up alerts by fusing and correlating diverse signal sources.</span></span>

- [<span data-ttu-id="cae0c-394">ตรวจสอบการแจ้งเตือนใน Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="cae0c-394">Monitor alerts in Cloud App Security</span></span>](/cloud-app-security/monitor-alerts)

<span data-ttu-id="cae0c-395">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-395">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-396">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-396">**Responsibility**: Customer</span></span>

### <a name="ir-4-detection-and-analysis--investigate-an-incident"></a><span data-ttu-id="cae0c-397">IR-4: การตรวจจับและวิเคราะห์ - ตรวจสอบเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="cae0c-397">IR-4: Detection and analysis – investigate an incident</span></span>

<span data-ttu-id="cae0c-398">**คำแนะนำ**: สร้างคู่มือการตอบสนองต่อเหตุการณ์สำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="cae0c-398">**Guidance**: Build out an incident response guide for your organization.</span></span> <span data-ttu-id="cae0c-399">ทำการฝึกซ้อมเพื่อทดสอบความสามารถในการตอบสนองต่อเหตุการณ์ของระบบของคุณด้วยการใช้งานปกติ</span><span class="sxs-lookup"><span data-stu-id="cae0c-399">Conduct exercises to test your systems’ incident response capabilities on a regular cadence.</span></span> <span data-ttu-id="cae0c-400">ระบุจุดอ่อนและช่องว่างและแก้ไขแผนตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="cae0c-400">Identify weak points and gaps and revise plan as needed.</span></span>

<span data-ttu-id="cae0c-401">ตรวจสอบให้แน่ใจว่ามีแผนการตอบสนองต่อเหตุการณ์ที่เป็นลายลักษณ์อักษรที่กำหนดบทบาทของบุคลากรทั้งหมด ตลอดจนขั้นตอนของการรับมือ / การจัดการเหตุการณ์ตั้งแต่การตรวจจับไปจนถึงการทบทวนหลังเกิดเหตุ</span><span class="sxs-lookup"><span data-stu-id="cae0c-401">Ensure that there are written incident response plans that define all roles of personnel as well as phases of incident handling/management from detection to post-incident review.</span></span>

- [<span data-ttu-id="cae0c-402">ภาพรวมเหตุการณ์ใน Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="cae0c-402">Incidents overview in Microsoft Threat Protection</span></span>](/microsoft-365/security/mtp/incidents-overview)

<span data-ttu-id="cae0c-403">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-403">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-404">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-404">**Responsibility**: Customer</span></span>

### <a name="ir-5-detection-and-analysis--prioritize-incidents"></a><span data-ttu-id="cae0c-405">IR-5: การตรวจจับและวิเคราะห์ - จัดลำดับความสำคัญของเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="cae0c-405">IR-5: Detection and analysis – prioritize incidents</span></span>

<span data-ttu-id="cae0c-406">**คำแนะนำ**: กำหนดบริบทให้กับนักวิเคราะห์ว่าเหตุการณ์ใดควรมุ่งเน้นเป็นอันดับแรกโดยพิจารณาจากความรุนแรงของการแจ้งเตือนและความอ่อนไหวของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="cae0c-406">**Guidance**: Provide context to analysts on which incidents to focus on first based on alert severity and asset sensitivity.</span></span> 

 
<span data-ttu-id="cae0c-407">Microsoft Threat Protection ใช้การวิเคราะห์ความสัมพันธ์และรวบรวมการแจ้งเตือนและการตรวจสอบที่เกี่ยวข้องทั้งหมดจากผลิตภัณฑ์ต่าง ๆ ไว้ในเหตุการณ์เดียว</span><span class="sxs-lookup"><span data-stu-id="cae0c-407">Microsoft Threat Protection applies correlation analytics and aggregates all related alerts and investigations from different products into one incident.</span></span> <span data-ttu-id="cae0c-408">Microsoft Threat Protection ยังทริกเกอร์การแจ้งเตือนที่ไม่ซ้ำกันเกี่ยวกับกิจกรรมที่สามารถระบุได้ว่าเป็นอันตรายเท่านั้นเนื่องจากความสามารถในการมองเห็นครบวงจรที่ Microsoft Threat Protection มีอยู่ทั่วทั้งอสังหาริมทรัพย์และชุดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cae0c-408">Microsoft Threat Protection also triggers unique alerts on activities that can only be identified as malicious given the end-to-end visibility that Microsoft Threat Protection has across the entire estate and suite of products.</span></span> <span data-ttu-id="cae0c-409">ด้วยการทำเช่นนั้น Microsoft Threat Protection จะบรรยายเรื่องราวการโจมตีที่กว้างขึ้น ช่วยให้นักวิเคราะห์การดำเนินงานด้านความปลอดภัยเข้าใจและจัดการกับภัยคุกคามที่ซับซ้อนทั่วทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="cae0c-409">By doing so, Microsoft Threat Protection narrates the broader attack story, allowing a security operations analyst to understand and deal with complex threats across the organization.</span></span>

- [<span data-ttu-id="cae0c-410">จัดลำดับความสำคัญของเหตุการณ์ใน Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="cae0c-410">Prioritize incidents in Microsoft Threat Protection</span></span>](/microsoft-365/security/mtp/incident-queue?amp;preserve-view=true&view=o365-worldwide)

<span data-ttu-id="cae0c-411">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-411">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-412">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-412">**Responsibility**: Customer</span></span>

### <a name="ir-6-containment-eradication-and-recovery--automate-the-incident-handling"></a><span data-ttu-id="cae0c-413">IR-6: การกักกัน การกำจัด และการกู้คืน - จัดการเหตุการณ์โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cae0c-413">IR-6: Containment, eradication and recovery – automate the incident handling</span></span>

<span data-ttu-id="cae0c-414">**คำแนะนำ**: ทำให้งานแบบแมนวลที่เกิดขึ้นซ้ำเป็นแบบอัตโนมัติเพื่อเร่งเวลาตอบสนองและลดภาระให้กับนักวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="cae0c-414">**Guidance**: Automate manual repetitive tasks to speed up response time and reduce the burden on analysts.</span></span> <span data-ttu-id="cae0c-415">งานแบบแมนวลใช้เวลาในการดำเนินการนานกว่า ทำให้แต่ละเหตุการณ์ช้าลง และลดจำนวนเหตุการณ์ที่นักวิเคราะห์สามารถจัดการได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-415">Manual tasks take longer to execute, slowing each incident and reducing how many incidents an analyst can handle.</span></span> <span data-ttu-id="cae0c-416">นอกจากนี้งานแบบแมนวลยังเพิ่มความอ่อนเพลียของนักวิเคราะห์ ซึ่งจะเพิ่มความเสี่ยงต่อความผิดพลาดของมนุษย์ที่ทำให้เกิดความล่าช้า และลดความสามารถของนักวิเคราะห์ในการมุ่งเน้นไปที่งานที่ซับซ้อนให้มีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="cae0c-416">Manual tasks also increase analyst fatigue, which increases the risk of human error that causes delays, and degrades the ability of analysts to focus effectively on complex tasks.</span></span>  
 
<span data-ttu-id="cae0c-417">ใช้คุณลักษณะการทำงานอัตโนมัติของเวิร์กโฟลว์ใน Microsoft Threat Protection เพื่อทริกเกอร์การตรวจสอบและการแก้ไขโดยอัตโนมัติตามการแจ้งเตือนความปลอดภัยที่เข้ามา</span><span class="sxs-lookup"><span data-stu-id="cae0c-417">Use workflow automation features in Microsoft Threat Protection to automatically trigger investigations and remediation in response to incoming security alerts.</span></span> 
 
- [<span data-ttu-id="cae0c-418">การตรวจสอบและการตอบสนองอัตโนมัติใน Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="cae0c-418">Automated investigation and response in Microsoft Threat Protection</span></span>](/microsoft-365/security/mtp/mtp-autoir)

<span data-ttu-id="cae0c-419">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-419">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-420">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-420">**Responsibility**: Customer</span></span>

## <a name="posture-and-vulnerability-management"></a><span data-ttu-id="cae0c-421">การจัดการสภาวะและช่องโหว่</span><span class="sxs-lookup"><span data-stu-id="cae0c-421">Posture and Vulnerability Management</span></span>

<span data-ttu-id="cae0c-422">*สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Azure Security Benchmark: การจัดการสภาวะและช่องโหว่](/azure/security/benchmarks/security-controls-v2-posture-vulnerability-management)*</span><span class="sxs-lookup"><span data-stu-id="cae0c-422">*For more information, see the [Azure Security Benchmark: Posture and Vulnerability Management](/azure/security/benchmarks/security-controls-v2-posture-vulnerability-management).*</span></span>

### <a name="pv-1-establish-secure-configurations-for-azure-services"></a><span data-ttu-id="cae0c-423">PV-1: สร้างการกำหนดค่าความปลอดภัยสำหรับบริการ Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-423">PV-1: Establish secure configurations for Azure services</span></span> 

<span data-ttu-id="cae0c-424">**คำแนะนำ**: กำหนดค่าบริการ Power BI ของคุณด้วยการตั้งค่าที่เหมาะสมกับองค์กรและจุดยืนด้านความปลอดภัยของคุณ</span><span class="sxs-lookup"><span data-stu-id="cae0c-424">**Guidance**: Configure your Power BI service with the settings appropriate to your organization and security stance.</span></span> <span data-ttu-id="cae0c-425">การตั้งค่าสำหรับการเข้าถึงบริการและเนื้อหา ตลอดจนพื้นที่ทำงานและความปลอดภัยของแอปควรได้รับการพิจารณาอย่างรอบคอบ</span><span class="sxs-lookup"><span data-stu-id="cae0c-425">Settings for access to the service, and content, as well as workspace and app security should be carefully considered.</span></span> <span data-ttu-id="cae0c-426">โปรดดูการรักษาความปลอดภัย Power BI และการป้องกันข้อมูลในเอกสารการปรับใช้ Power BI Enterprise</span><span class="sxs-lookup"><span data-stu-id="cae0c-426">See Power BI Security and Data Protection in the Power BI Enterprise Deployment whitepaper.</span></span>

- [<span data-ttu-id="cae0c-427">เอกสารการปรับใช้ Power BI Enterprise</span><span class="sxs-lookup"><span data-stu-id="cae0c-427">Enterprise Deployment Whitepaper</span></span>](https://aka.ms/PBIEnterpriseDeploymentWP)

<span data-ttu-id="cae0c-428">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-428">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-429">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-429">**Responsibility**: Customer</span></span>

### <a name="pv-2-sustain-secure-configurations-for-azure-services"></a><span data-ttu-id="cae0c-430">PV-2: รักษาการกำหนดค่าความปลอดภัยสำหรับบริการ Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-430">PV-2: Sustain secure configurations for Azure services</span></span>

<span data-ttu-id="cae0c-431">**คำแนะนำ**: ตรวจสอบอินสแตนซ์ Power BI ของคุณโดยใช้ Power BI Admin REST APIs</span><span class="sxs-lookup"><span data-stu-id="cae0c-431">**Guidance**: Monitor your Power BI instance using the Power BI Admin REST APIs.</span></span>

- [<span data-ttu-id="cae0c-432">Power BI Admin REST APIs</span><span class="sxs-lookup"><span data-stu-id="cae0c-432">Power BI Admin REST APIs</span></span>](/rest/api/power-bi/admin)

- [<span data-ttu-id="cae0c-433">เอกสารการปรับใช้ Power BI enterprise</span><span class="sxs-lookup"><span data-stu-id="cae0c-433">Power BI enterprise deployment whitepaper</span></span>](https://aka.ms/PBIEnterpriseDeploymentWP)

<span data-ttu-id="cae0c-434">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-434">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-435">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-435">**Responsibility**: Customer</span></span>

### <a name="pv-8-conduct-regular-attack-simulation"></a><span data-ttu-id="cae0c-436">PV-8: ทำการจำลองการโจมตีปกติ</span><span class="sxs-lookup"><span data-stu-id="cae0c-436">PV-8: Conduct regular attack simulation</span></span>

<span data-ttu-id="cae0c-437">**คำแนะนำ**: ตามความจำเป็น ให้ดำเนินการทดสอบการเจาะระบบหรือกิจกรรมของทีมที่มีทักษะสูง (Red Team) สำหรับทรัพยากร Azure ของคุณ และตรวจสอบการแก้ไขข้อค้นพบด้านความปลอดภัยที่สำคัญทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="cae0c-437">**Guidance**: As required, conduct penetration testing or red team activities on your Azure resources and ensure remediation of all critical security findings.</span></span>

<span data-ttu-id="cae0c-438">ปฏิบัติตามกฎการทดสอบการเจาะระบบของ Microsoft Cloud เพื่อให้แน่ใจว่าการทดสอบการเจาะระบบของคุณจะไม่ละเมิดนโยบายของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="cae0c-438">Follow the Microsoft Cloud Penetration Testing Rules of Engagement to ensure your penetration tests are not in violation of Microsoft policies.</span></span> <span data-ttu-id="cae0c-439">ใช้กลยุทธ์และการดำเนินการจัดตั้งทีมที่มีทักษะสูงของ Microsoft และการทดสอบการเจาะไซต์แบบสดเทียบกับโครงสร้างพื้นฐาน บริการ และแอปพลิเคชันบนคลาวด์ที่จัดการโดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="cae0c-439">Use Microsoft's strategy and execution of Red Teaming and live site penetration testing against Microsoft-managed cloud infrastructure, services, and applications.</span></span>

- [<span data-ttu-id="cae0c-440">การทดสอบการเจาะระบบใน Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-440">Penetration testing in Azure</span></span>](/azure/security/fundamentals/pen-testing)

- [<span data-ttu-id="cae0c-441">กฎการทดสอบการเจาะระบบของการมีส่วนร่วม</span><span class="sxs-lookup"><span data-stu-id="cae0c-441">Penetration Testing Rules of Engagement</span></span>](https://www.microsoft.com/msrc/pentest-rules-of-engagement?rtc=1)

- [<span data-ttu-id="cae0c-442">การจัดตั้งทีมที่มีทักษะสูงของ Microsoft Cloud</span><span class="sxs-lookup"><span data-stu-id="cae0c-442">Microsoft Cloud Red Teaming</span></span>](https://gallery.technet.microsoft.com/Cloud-Red-Teaming-b837392e)

<span data-ttu-id="cae0c-443">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-443">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-444">**ความรับผิดชอบ**: แชร์</span><span class="sxs-lookup"><span data-stu-id="cae0c-444">**Responsibility**: Shared</span></span>

## <a name="backup-and-recovery"></a><span data-ttu-id="cae0c-445">สำรองและกู้ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cae0c-445">Backup and Recovery</span></span>

<span data-ttu-id="cae0c-446">*สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Azure Security Benchmark: สำรองและกู้ข้อมูล](/azure/security/benchmarks/security-controls-v2-backup-recovery)*</span><span class="sxs-lookup"><span data-stu-id="cae0c-446">*For more information, see the [Azure Security Benchmark: Backup and Recovery](/azure/security/benchmarks/security-controls-v2-backup-recovery).*</span></span>

### <a name="br-3-validate-all-backups-including-customer-managed-keys"></a><span data-ttu-id="cae0c-447">BR-3: ตรวจสอบการสำรองข้อมูลทั้งหมด รวมถึงคีย์ที่ลูกค้าจัดการ</span><span class="sxs-lookup"><span data-stu-id="cae0c-447">BR-3: Validate all backups including customer-managed keys</span></span>

<span data-ttu-id="cae0c-448">**คำแนะนำ**: ถ้าคุณกำลังใช้คุณลักษณะ Bring Your Own Key (BYOK) ใน Power BI คุณต้องตรวจสอบเป็นระยะว่าคุณสามารถเข้าถึงและกู้คืนคีย์ที่ลูกค้าจัดการได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-448">**Guidance**: If you are using the Bring Your Own Key (BYOK) feature in Power BI you need to periodically validate that you can access and restore your customer-managed keys.</span></span>

- [<span data-ttu-id="cae0c-449">BYOK ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-449">BYOK in Power BI</span></span>](../admin/service-encryption-byok.md)

<span data-ttu-id="cae0c-450">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-450">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-451">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-451">**Responsibility**: Customer</span></span>

### <a name="br-4-mitigate-risk-of-lost-keys"></a><span data-ttu-id="cae0c-452">BR-4: ลดความเสี่ยงจากคีย์สูญหาย</span><span class="sxs-lookup"><span data-stu-id="cae0c-452">BR-4: Mitigate risk of lost keys</span></span>

<span data-ttu-id="cae0c-453">**คำแนะนำ**: ถ้าคุณกำลังใช้คุณลักษณะ Bring Your Own Key (BYOK) ใน Power BI คุณต้องแน่ใจว่า Key Vault ที่ควบคุมคีย์ที่ลูกค้าจัดการของคุณได้รับการกำหนดค่าตามคำแนะนำของ BYOK ในเอกสาร Power BI ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="cae0c-453">**Guidance**: If you are using the Bring Your Own Key (BYOK) feature in Power BI you need to ensure the Key Vault controlling your customer-managed keys is configured with the guidance in the BYOK in Power BI documentation below.</span></span> <span data-ttu-id="cae0c-454">เปิดใช้งานการป้องกันการลบและการล้างข้อมูลแบบนุ่มนวลใน Azure Key Vault เพื่อป้องกันคีย์จากการลบโดยไม่ได้ตั้งใจหรือเป็นอันตราย</span><span class="sxs-lookup"><span data-stu-id="cae0c-454">Enable soft delete and purge protection in Azure Key Vault to protect keys against accidental or malicious deletion.</span></span>

- [<span data-ttu-id="cae0c-455">BYOK ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="cae0c-455">BYOK in Power BI</span></span>](../admin/service-encryption-byok.md)

- [<span data-ttu-id="cae0c-456">วิธีการเปิดใช้งานการป้องกันการลบและการล้างข้อมูลแบบนุ่มนวลใน Key Vault</span><span class="sxs-lookup"><span data-stu-id="cae0c-456">How to enable soft delete and purge protection in Key Vault</span></span>](/azure/storage/blobs/storage-blob-soft-delete?tabs=azure-portal)

<span data-ttu-id="cae0c-457">สำหรับแหล่งข้อมูลคีย์ของเกตเวย์ กรุณาทำให้แน่ใจว่าคุณปฏิบัติตามคำแนะนำในเอกสารเกี่ยวกับคีย์เพื่อการกู้คืนเกตเวย์ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="cae0c-457">For Gateway key resources ensure you are following the guidance in the Gateway recovery key documentation below.</span></span>

- [<span data-ttu-id="cae0c-458">คีย์เพื่อการกู้คืนเกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="cae0c-458">On-premises data gateway recovery key</span></span>](/data-integration/gateway/service-gateway-recovery-key)

<span data-ttu-id="cae0c-459">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-459">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-460">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-460">**Responsibility**: Customer</span></span>

## <a name="governance-and-strategy"></a><span data-ttu-id="cae0c-461">การกำกับดูแลและกลยุทธ์</span><span class="sxs-lookup"><span data-stu-id="cae0c-461">Governance and Strategy</span></span>

<span data-ttu-id="cae0c-462">*สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Azure Security Benchmark: การกำกับดูแลและกลยุทธ์](/azure/security/benchmarks/security-controls-v2-governance-strategy)*</span><span class="sxs-lookup"><span data-stu-id="cae0c-462">*For more information, see the [Azure Security Benchmark: Governance and Strategy](/azure/security/benchmarks/security-controls-v2-governance-strategy).*</span></span>

### <a name="gs-1-define-asset-management-and-data-protection-strategy"></a><span data-ttu-id="cae0c-463">GS-1: กำหนดกลยุทธ์การจัดการสินทรัพย์และการป้องกันข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cae0c-463">GS-1: Define asset management and data protection strategy</span></span> 

<span data-ttu-id="cae0c-464">**คำแนะนำ**: ตรวจสอบให้แน่ใจว่าคุณจัดทำเอกสารและสื่อสารกลยุทธ์ที่ชัดเจนสำหรับการตรวจสอบและการปกป้องระบบและข้อมูลอย่างต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="cae0c-464">**Guidance**: Ensure you document and communicate a clear strategy for continuous monitoring and protection of systems and data.</span></span> <span data-ttu-id="cae0c-465">จัดลำดับความสำคัญของการค้นหา การประเมิน การป้องกัน และการตรวจสอบข้อมูลและระบบที่สำคัญทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="cae0c-465">Prioritize discovery, assessment, protection, and monitoring of business-critical data and systems.</span></span> 

<span data-ttu-id="cae0c-466">กลยุทธ์นี้ควรมีคำแนะนำ นโยบาย และมาตรฐานสำหรับองค์ประกอบต่อไปนี้ในรูปแบบเอกสาร:</span><span class="sxs-lookup"><span data-stu-id="cae0c-466">This strategy should include documented guidance, policy, and standards for the following elements:</span></span> 

-   <span data-ttu-id="cae0c-467">มาตรฐานการจัดประเภทข้อมูลตามความเสี่ยงของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="cae0c-467">Data classification standard in accordance with the business risks</span></span>

-   <span data-ttu-id="cae0c-468">ความสามารถในการมองเห็นขององค์กรด้านความปลอดภัยสำหรับความเสี่ยงและคลังสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="cae0c-468">Security organization visibility into risks and asset inventory</span></span> 

-   <span data-ttu-id="cae0c-469">การอนุมัติองค์กรด้านความปลอดภัยของบริการ Azure สำหรับการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cae0c-469">Security organization approval of Azure services for use</span></span> 

-   <span data-ttu-id="cae0c-470">การรักษาความปลอดภัยของสินทรัพย์ผ่านวงจรชีวิตของสินทรัพย์เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="cae0c-470">Security of assets through their lifecycle</span></span>

-   <span data-ttu-id="cae0c-471">กลยุทธ์การควบคุมการเข้าถึงที่จำเป็นตามการจำแนกประเภทข้อมูลขององค์กร</span><span class="sxs-lookup"><span data-stu-id="cae0c-471">Required access control strategy in accordance with organizational data classification</span></span>

-   <span data-ttu-id="cae0c-472">การใช้ความสามารถในการป้องกันข้อมูลของ Azure แบบเนทีฟและบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="cae0c-472">Use of Azure native and third-party data protection capabilities</span></span>

-   <span data-ttu-id="cae0c-473">ข้อกำหนดการเข้ารหัสข้อมูลสำหรับกรณีการใช้งานระหว่างารส่งผ่านและการพัก</span><span class="sxs-lookup"><span data-stu-id="cae0c-473">Data encryption requirements for in-transit and at-rest use cases</span></span>

-   <span data-ttu-id="cae0c-474">มาตรฐานการเข้ารหัสที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="cae0c-474">Appropriate cryptographic standards</span></span>

<span data-ttu-id="cae0c-475">สำหรับข้อมูลเพิ่มเติม ให้ดูรายการอ้างอิงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cae0c-475">For more information, see the following references:</span></span>
- [<span data-ttu-id="cae0c-476">คำแนะนำเกี่ยวกับสถาปัตยกรรมความปลอดภัยของ Azure - การจัดเก็บ ข้อมูล และการเข้ารหัส</span><span class="sxs-lookup"><span data-stu-id="cae0c-476">Azure Security Architecture Recommendation - Storage, data, and encryption</span></span>](/azure/architecture/framework/security/storage-data-encryption?amp;bc=%2fsecurity%2fcompass%2fbreadcrumb%2ftoc.json&toc=%2fsecurity%2fcompass%2ftoc.json)

- [<span data-ttu-id="cae0c-477">ข้อมูลพื้นฐานเกี่ยวกับความปลอดภัยของ Azure - ความปลอดภัยของข้อมูล การเข้ารหัส และการจัดเก็บข้อมูลของ Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-477">Azure Security Fundamentals - Azure Data security, encryption, and storage</span></span>](/azure/security/fundamentals/encryption-overview)

- [<span data-ttu-id="cae0c-478">เฟรมเวิร์กการปรับใช้งานระบบคลาวด์ - แนวทางปฏิบัติที่ดีที่สุดสำหรับการรักษาความปลอดภัยของข้อมูลและการเข้ารหัส Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-478">Cloud Adoption Framework - Azure data security and encryption best practices</span></span>](/azure/security/fundamentals/data-encryption-best-practices?amp;bc=%2fazure%2fcloud-adoption-framework%2f_bread%2ftoc.json&toc=%2fazure%2fcloud-adoption-framework%2ftoc.json)

- [<span data-ttu-id="cae0c-479">Azure Security Benchmark - การจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="cae0c-479">Azure Security Benchmark - Asset management</span></span>](/azure/security/benchmarks/security-controls-v2-asset-management)

- [<span data-ttu-id="cae0c-480">Azure Security Benchmark - การป้องกันข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cae0c-480">Azure Security Benchmark - Data Protection</span></span>](/azure/security/benchmarks/security-controls-v2-data-protection)

<span data-ttu-id="cae0c-481">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-481">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-482">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-482">**Responsibility**: Customer</span></span>

### <a name="gs-2-define-enterprise-segmentation-strategy"></a><span data-ttu-id="cae0c-483">GS-2: กำหนดกลยุทธ์การแบ่งเซกเมนต์ขององค์กร</span><span class="sxs-lookup"><span data-stu-id="cae0c-483">GS-2: Define enterprise segmentation strategy</span></span> 

<span data-ttu-id="cae0c-484">**คำแนะนำ**: กำหนดกลยุทธ์ทั่วทั้งองค์กรเพื่อแบ่งเซกเมนต์การเข้าถึงสินทรัพย์โดยใช้การผสมผสานระหว่างข้อมูลเอกลักษณ์ เครือข่าย แอปพลิเคชัน การสมัครสมาชิก กลุ่มการจัดการ และการควบคุมอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="cae0c-484">**Guidance**: Establish an enterprise-wide strategy to segmenting access to assets using a combination of identity, network, application, subscription, management group, and other controls.</span></span>

<span data-ttu-id="cae0c-485">สร้างสมดุลระหว่างความจำเป็นในการแยกความปลอดภัยอย่างรอบคอบกับความจำเป็นในการเปิดใช้งานการทำงานประจำวันของระบบที่จำเป็นต้องสื่อสารกันและเข้าถึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cae0c-485">Carefully balance the need for security separation with the need to enable daily operation of the systems that need to communicate with each other and access data.</span></span>

<span data-ttu-id="cae0c-486">ตรวจสอบให้แน่ใจว่ากลยุทธ์การแบ่งเซกเมนต์ถูกนำไปใช้อย่างสม่ำเสมอทั่วประเภทการควบคุมรวมถึงความปลอดภัยของเครือข่าย โมเดลข้อมูลเอกลักษณ์และการเข้าถึง และโมเดลการอนุญาต/การเข้าถึงแอปพลิเคชัน และการควบคุมกระบวนการของมนุษย์</span><span class="sxs-lookup"><span data-stu-id="cae0c-486">Ensure that the segmentation strategy is implemented consistently across control types including network security, identity and access models, and application permission/access models, and human process controls.</span></span>

- [<span data-ttu-id="cae0c-487">คำแนะนำเกี่ยวกับกลยุทธ์การแบ่งเซกเมนต์ใน Azure (วิดีโอ)</span><span class="sxs-lookup"><span data-stu-id="cae0c-487">Guidance on segmentation strategy in Azure (video)</span></span>](/security/compass/microsoft-security-compass-introduction#azure-components-and-reference-model-2151)

- [<span data-ttu-id="cae0c-488">คำแนะนำเกี่ยวกับกลยุทธ์การแบ่งเซกเมนต์ใน Azure (เอกสาร)</span><span class="sxs-lookup"><span data-stu-id="cae0c-488">Guidance on segmentation strategy in Azure (document)</span></span>](/security/compass/governance#enterprise-segmentation-strategy)

- [<span data-ttu-id="cae0c-489">ปรับการแบ่งเซกเมนต์เครือข่ายให้สอดคล้องกับกลยุทธ์การแบ่งเซกเมนต์ขององค์กร</span><span class="sxs-lookup"><span data-stu-id="cae0c-489">Align network segmentation with enterprise segmentation strategy</span></span>](/security/compass/network-security-containment#align-network-segmentation-with-enterprise-segmentation-strategy)

<span data-ttu-id="cae0c-490">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-490">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-491">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-491">**Responsibility**: Customer</span></span>

### <a name="gs-3-define-security-posture-management-strategy"></a><span data-ttu-id="cae0c-492">GS-3: กำหนดกลยุทธ์การจัดการสภาวะความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="cae0c-492">GS-3: Define security posture management strategy</span></span>

<span data-ttu-id="cae0c-493">**คำแนะนำ**: วัดผลและลดความเสี่ยงต่อทรัพย์สินแต่ละรายการและสภาพแวดล้อมที่สินทรัพย์เหล่านั้นอยู่อย่างต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="cae0c-493">**Guidance**: Continuously measure and mitigate risks to your individual assets and the environment they are hosted in.</span></span> <span data-ttu-id="cae0c-494">จัดลำดับความสำคัญของทรัพย์สินที่มีมูลค่าสูงและลักษณะภายนอกของการโจมตีที่มีการเปิดเผยสูง เช่น แอปพลิเคชันที่เผยแพร่ จุดเข้าและออกของเครือข่าย จุดสิ้นสุดของผู้ใช้และผู้ดูแลระบบ เป็นต้น</span><span class="sxs-lookup"><span data-stu-id="cae0c-494">Prioritize high value assets and highly-exposed attack surfaces, such as published applications, network ingress and egress points, user and administrator endpoints, etc.</span></span>

- [<span data-ttu-id="cae0c-495">Azure Security Benchmark - การจัดการสภาวะความปลอดภัยและช่องโหว่</span><span class="sxs-lookup"><span data-stu-id="cae0c-495">Azure Security Benchmark - Posture and vulnerability management</span></span>](/azure/security/benchmarks/security-controls-v2-posture-vulnerability-management)

<span data-ttu-id="cae0c-496">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-496">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-497">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-497">**Responsibility**: Customer</span></span>

### <a name="gs-4-align-organization-roles-responsibilities-and-accountabilities"></a><span data-ttu-id="cae0c-498">GS-4: จัดตำแหน่งบทบาท ความรับผิดชอบ และภาระความรับผิดขององค์กร</span><span class="sxs-lookup"><span data-stu-id="cae0c-498">GS-4: Align organization roles, responsibilities, and accountabilities</span></span>

<span data-ttu-id="cae0c-499">**คำแนะนำ**: ตรวจสอบให้แน่ใจว่าคุณจัดทำเอกสารและสื่อสารกลยุทธ์ที่ชัดเจนสำหรับบทบาทและความรับผิดชอบในองค์กรด้านความปลอดภัยของคุณ</span><span class="sxs-lookup"><span data-stu-id="cae0c-499">**Guidance**: Ensure you document and communicate a clear strategy for roles and responsibilities in your security organization.</span></span> <span data-ttu-id="cae0c-500">จัดลำดับความสำคัญของการให้ความรับผิดชอบที่ชัดเจนสำหรับการตัดสินใจด้านความปลอดภัย การให้ความรู้แก่ทุกคนเกี่ยวกับรูปแบบความรับผิดชอบร่วมกัน และให้ความรู้แก่ทีมเทคนิคเกี่ยวกับเทคโนโลยีเพื่อรักษาความปลอดภัยบนคลาวด์</span><span class="sxs-lookup"><span data-stu-id="cae0c-500">Prioritize providing clear accountability for security decisions, educating everyone on the shared responsibility model, and educate technical teams on technology to secure the cloud.</span></span>

- [<span data-ttu-id="cae0c-501">แนวทางปฏิบัติที่ดีที่สุดสำหรับการรักษาความปลอดภัย Azure 1 – ผู้คน: ให้ความรู้แก่ทีมงานเกี่ยวกับเส้นทางความปลอดภัยบนคลาวด์</span><span class="sxs-lookup"><span data-stu-id="cae0c-501">Azure Security Best Practice 1 – People: Educate Teams on Cloud Security Journey</span></span>](/azure/cloud-adoption-framework/security/security-top-10#1-people-educate-teams-about-the-cloud-security-journey)

- [<span data-ttu-id="cae0c-502">แนวทางปฏิบัติที่ดีที่สุดสำหรับการรักษาความปลอดภัย Azure 2 – ผู้คน: ให้ความรู้แก่ทีมงานเกี่ยวกับเทคโนโลยีความปลอดภัยบนคลาวด์</span><span class="sxs-lookup"><span data-stu-id="cae0c-502">Azure Security Best Practice 2 - People: Educate Teams on Cloud Security Technology</span></span>](/azure/cloud-adoption-framework/security/security-top-10#2-people-educate-teams-on-cloud-security-technology)

- [<span data-ttu-id="cae0c-503">แนวทางปฏิบัติที่ดีที่สุดสำหรับการรักษาความปลอดภัย Azure 3 – กระบวนการ: กำหนดความรับผิดชอบสำหรับการตัดสินใจด้านความปลอดภัยบนคลาวด์</span><span class="sxs-lookup"><span data-stu-id="cae0c-503">Azure Security Best Practice 3 - Process: Assign Accountability for Cloud Security Decisions</span></span>](/azure/cloud-adoption-framework/security/security-top-10#4-process-update-incident-response-ir-processes-for-cloud)

<span data-ttu-id="cae0c-504">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-504">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-505">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-505">**Responsibility**: Customer</span></span>

### <a name="gs-5-define-network-security-strategy"></a><span data-ttu-id="cae0c-506">GS-5: กำหนดกลยุทธ์ความปลอดภัยของเครือข่าย</span><span class="sxs-lookup"><span data-stu-id="cae0c-506">GS-5: Define network security strategy</span></span>

<span data-ttu-id="cae0c-507">**คำแนะนำ**: กำหนดแนวทางการรักษาความปลอดภัยเครือข่าย Azure ในฐานะที่เป็นส่วนหนึ่งของกลยุทธ์การควบคุมการเข้าถึงความปลอดภัยโดยรวมขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="cae0c-507">**Guidance**: Establish an Azure network security approach as part of your organization’s overall security access control strategy.</span></span>  

<span data-ttu-id="cae0c-508">กลยุทธ์นี้ควรมีคำแนะนำ นโยบาย และมาตรฐานสำหรับองค์ประกอบต่อไปนี้ในรูปแบบเอกสาร:</span><span class="sxs-lookup"><span data-stu-id="cae0c-508">This strategy should include documented guidance, policy, and standards for the following elements:</span></span> 

-   <span data-ttu-id="cae0c-509">การจัดการเครือข่ายแบบรวมศูนย์และความรับผิดชอบด้านความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="cae0c-509">Centralized network management and security responsibility</span></span>

-   <span data-ttu-id="cae0c-510">รูปแบบการแบ่งเซกเมนต์เครือข่ายเสมือนที่สอดคล้องกับกลยุทธ์การแบ่งเซกเมนต์ขององค์กร</span><span class="sxs-lookup"><span data-stu-id="cae0c-510">Virtual network segmentation model aligned with the enterprise segmentation strategy</span></span>

-   <span data-ttu-id="cae0c-511">กลยุทธ์การแก้ไขสำหรับสถานการณ์คุกคามและการโจมตีที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="cae0c-511">Remediation strategy in different threat and attack scenarios</span></span>

-   <span data-ttu-id="cae0c-512">ขอบอินเทอร์เน็ตและกลยุทธ์การเข้าและออกของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cae0c-512">Internet edge and ingress and egress strategy</span></span>

-   <span data-ttu-id="cae0c-513">ระบบคลาวด์แบบไฮบริดและกลยุทธ์การเชื่อมต่อระหว่างกันในองค์กร</span><span class="sxs-lookup"><span data-stu-id="cae0c-513">Hybrid cloud and on-premises interconnectivity strategy</span></span>

-   <span data-ttu-id="cae0c-514">สิ่งประดิษฐ์ด้านความปลอดภัยเครือข่ายที่ทันสมัย (เช่น แผนภาพเครือข่าย สถาปัตยกรรมเครือข่ายอ้างอิง)</span><span class="sxs-lookup"><span data-stu-id="cae0c-514">Up-to-date network security artifacts (e.g. network diagrams, reference network architecture)</span></span>

<span data-ttu-id="cae0c-515">สำหรับข้อมูลเพิ่มเติม ให้ดูรายการอ้างอิงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cae0c-515">For more information, see the following references:</span></span>
- [<span data-ttu-id="cae0c-516">แนวทางปฏิบัติที่ดีที่สุดสำหรับการรักษาความปลอดภัย Azure 11 – สถาปัตยกรรม กลยุทธ์การรักษาความปลอดภัยแบบรวมหนึ่งเดียว</span><span class="sxs-lookup"><span data-stu-id="cae0c-516">Azure Security Best Practice 11 - Architecture. Single unified security strategy</span></span>](/azure/cloud-adoption-framework/security/security-top-10#11-architecture-establish-a-single-unified-security-strategy)

- [<span data-ttu-id="cae0c-517">Azure Security Benchmark - ความปลอดภัยของเครือข่าย</span><span class="sxs-lookup"><span data-stu-id="cae0c-517">Azure Security Benchmark - Network Security</span></span>](/azure/security/benchmarks/security-controls-v2-network-security)

- [<span data-ttu-id="cae0c-518">ภาพรวมความปลอดภัยของเครือข่าย Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-518">Azure network security overview</span></span>](/azure/security/fundamentals/network-overview)

- [<span data-ttu-id="cae0c-519">กลยุทธ์สถาปัตยกรรมเครือข่ายองค์กร</span><span class="sxs-lookup"><span data-stu-id="cae0c-519">Enterprise network architecture strategy</span></span>](/azure/cloud-adoption-framework/ready/enterprise-scale/architecture)

<span data-ttu-id="cae0c-520">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-520">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-521">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-521">**Responsibility**: Customer</span></span>

### <a name="gs-6-define-identity-and-privileged-access-strategy"></a><span data-ttu-id="cae0c-522">GS-6: กำหนดข้อมูลเอกลักษณ์และกลยุทธ์การเข้าถึงที่มีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="cae0c-522">GS-6: Define identity and privileged access strategy</span></span>

<span data-ttu-id="cae0c-523">**คำแนะนำ**: สร้างข้อมูลเอกลักษณ์ Azure และวิธีการเข้าถึงที่มีสิทธิ์ในฐานะที่เป็นส่วนหนึ่งของกลยุทธ์การควบคุมการเข้าถึงความปลอดภัยโดยรวมขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="cae0c-523">**Guidance**: Establish an Azure identity and privileged access approaches as part of your organization’s overall security access control strategy.</span></span>  

<span data-ttu-id="cae0c-524">กลยุทธ์นี้ควรมีคำแนะนำ นโยบาย และมาตรฐานสำหรับองค์ประกอบต่อไปนี้ในรูปแบบเอกสาร:</span><span class="sxs-lookup"><span data-stu-id="cae0c-524">This strategy should include documented guidance, policy, and standards for the following elements:</span></span> 

-   <span data-ttu-id="cae0c-525">ระบบข้อมูลเอกลักษณ์และการรับรองความถูกต้องแบบรวมศูนย์ และการเชื่อมต่อระหว่างกันกับระบบข้อมูลเอกลักษณ์ภายในและภายนอกอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="cae0c-525">A centralized identity and authentication system and its interconnectivity with other internal and external identity systems</span></span>

-   <span data-ttu-id="cae0c-526">วิธีการรับรองความถูกต้องที่แข็งแกร่งในกรณีการใช้งานและเงื่อนไขที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="cae0c-526">Strong authentication methods in different use cases and conditions</span></span>

-   <span data-ttu-id="cae0c-527">การคุ้มครองผู้ใช้ที่มีสิทธิ์พิเศษสูง</span><span class="sxs-lookup"><span data-stu-id="cae0c-527">Protection of highly privileged users</span></span>

-   <span data-ttu-id="cae0c-528">การตรวจสอบและจัดการกิจกรรมของผู้ใช้ที่ผิดปกติ</span><span class="sxs-lookup"><span data-stu-id="cae0c-528">Anomaly user activities monitoring and handling</span></span>  

-   <span data-ttu-id="cae0c-529">ข้อมูลเอกลักษณ์ของผู้ใช้และการตรวจสอบการเข้าถึงและกระบวนการสร้างความสอดคล้องต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="cae0c-529">User identity and access review and reconciliation process</span></span>

<span data-ttu-id="cae0c-530">สำหรับข้อมูลเพิ่มเติม ให้ดูรายการอ้างอิงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cae0c-530">For more information, see the following references:</span></span>

- [<span data-ttu-id="cae0c-531">Azure Security Benchmark - การจัดการข้อมูลเอกลักษณ์</span><span class="sxs-lookup"><span data-stu-id="cae0c-531">Azure Security Benchmark - Identity management</span></span>](/azure/security/benchmarks/security-controls-v2-identity-management)

- [<span data-ttu-id="cae0c-532">Azure Security Benchmark - การเข้าถึงที่มีสิทธิ์พิเศษ</span><span class="sxs-lookup"><span data-stu-id="cae0c-532">Azure Security Benchmark - Privileged access</span></span>](/azure/security/benchmarks/security-controls-v2-privileged-access)

- [<span data-ttu-id="cae0c-533">แนวทางปฏิบัติที่ดีที่สุดสำหรับการรักษาความปลอดภัย Azure 11 – สถาปัตยกรรม กลยุทธ์การรักษาความปลอดภัยแบบรวมหนึ่งเดียว</span><span class="sxs-lookup"><span data-stu-id="cae0c-533">Azure Security Best Practice 11 - Architecture. Single unified security strategy</span></span>](/azure/cloud-adoption-framework/security/security-top-10#11-architecture-establish-a-single-unified-security-strategy)

- [<span data-ttu-id="cae0c-534">ภาพรวมความปลอดภัยของการจัดการข้อมูลเอกลักษณ์ Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-534">Azure identity management security overview</span></span>](/azure/security/fundamentals/identity-management-overview)

<span data-ttu-id="cae0c-535">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-535">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-536">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-536">**Responsibility**: Customer</span></span>

### <a name="gs-7-define-logging-and-threat-response-strategy"></a><span data-ttu-id="cae0c-537">GS-7: กำหนดกลยุทธ์การบันทึกและการตอบสนองต่อภัยคุกคาม</span><span class="sxs-lookup"><span data-stu-id="cae0c-537">GS-7: Define logging and threat response strategy</span></span>

<span data-ttu-id="cae0c-538">**คำแนะนำ**: กำหนดกลยุทธ์การบันทึกและการตอบสนองต่อภัยคุกคามเพื่อตรวจจับและแก้ไขภัยคุกคามอย่างรวดเร็วในขณะที่ปฏิบัติตามข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="cae0c-538">**Guidance**: Establish a logging and threat response strategy to rapidly detect and remediate threats while meeting compliance requirements.</span></span> <span data-ttu-id="cae0c-539">จัดลำดับความสำคัญให้นักวิเคราะห์ด้วยการแจ้งเตือนที่มีคุณภาพสูงและประสบการณ์ที่ราบรื่นเพื่อให้พวกเขาสามารถมุ่งเน้นไปที่ภัยคุกคามมากกว่าการผสานรวมและขั้นตอนแบบแมนวล</span><span class="sxs-lookup"><span data-stu-id="cae0c-539">Prioritize providing analysts with high-quality alerts and seamless experiences so that they can focus on threats rather than integration and manual steps.</span></span> 

<span data-ttu-id="cae0c-540">กลยุทธ์นี้ควรมีคำแนะนำ นโยบาย และมาตรฐานสำหรับองค์ประกอบต่อไปนี้ในรูปแบบเอกสาร:</span><span class="sxs-lookup"><span data-stu-id="cae0c-540">This strategy should include documented guidance, policy, and standards for the following elements:</span></span> 

-   <span data-ttu-id="cae0c-541">บทบาทและความรับผิดชอบขององค์กรปฏิบัติการด้านความปลอดภัย (SecOps)</span><span class="sxs-lookup"><span data-stu-id="cae0c-541">The security operations (SecOps) organization’s role and responsibilities</span></span> 

-   <span data-ttu-id="cae0c-542">กระบวนการตอบสนองต่อเหตุการณ์ที่กำหนดไว้อย่างดีซึ่งสอดคล้องกับ NIST หรือกรอบงานอุตสาหกรรมอื่น</span><span class="sxs-lookup"><span data-stu-id="cae0c-542">A well-defined incident response process aligning with NIST or another industry framework</span></span> 

-   <span data-ttu-id="cae0c-543">การสกัดข้อมูลบันทึกและการเก็บรักษาบันทึกเพื่อรองรับการตรวจจับภัยคุกคาม การตอบสนองต่อเหตุการณ์ และความต้องการด้านการปฏิบัติตามกฎระเบียบ</span><span class="sxs-lookup"><span data-stu-id="cae0c-543">Log capture and retention to support threat detection, incident response, and compliance needs</span></span>

-   <span data-ttu-id="cae0c-544">ความสามารถในการมองเห็นและความสัมพันธ์ของข้อมูลภัยคุกคามแบบรวมศูนย์ โดยใช้ SIEM ความสามารถของ Azure แบบเนทีฟ และแหล่งข้อมูลอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="cae0c-544">Centralized visibility of and correlation information about threats, using SIEM, native Azure capabilities, and other sources</span></span> 

-   <span data-ttu-id="cae0c-545">แผนการสื่อสารและการแจ้งเตือนกับลูกค้า ซัพพลายเออร์ และบุคคลสาธารณะที่น่าสนใจ</span><span class="sxs-lookup"><span data-stu-id="cae0c-545">Communication and notification plan with your customers, suppliers, and public parties of interest</span></span>

-   <span data-ttu-id="cae0c-546">การใช้ Azure แบบเนทีฟและแพลตฟอร์มของบุคคลที่สามในการจัดการเหตุการณ์ เช่น การบันทึกและการตรวจจับภัยคุกคาม 
การพิสูจน์หลักฐาน และการแก้ไขและกำจัดการโจมตี</span><span class="sxs-lookup"><span data-stu-id="cae0c-546">Use of Azure native and third-party platforms for incident handling, such as logging and threat detection, forensics, and attack remediation and eradication</span></span>

-   <span data-ttu-id="cae0c-547">กระบวนการจัดการเหตุการณ์และกิจกรรมที่เกิดขึ้นหลังเหตุการณ์ เช่น บทเรียนที่ได้เรียนรู้และการเก็บรักษาหลักฐาน</span><span class="sxs-lookup"><span data-stu-id="cae0c-547">Processes for handling incidents and post-incident activities, such as lessons learned and evidence retention</span></span>

<span data-ttu-id="cae0c-548">สำหรับข้อมูลเพิ่มเติม ให้ดูรายการอ้างอิงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cae0c-548">For more information, see the following references:</span></span>

- [<span data-ttu-id="cae0c-549">Azure Security Benchmark - การบันทึกและการตรวจหาภัยคุกคาม</span><span class="sxs-lookup"><span data-stu-id="cae0c-549">Azure Security Benchmark - Logging and threat detection</span></span>](/azure/security/benchmarks/security-controls-v2-logging-threat-detection)

- [<span data-ttu-id="cae0c-550">Azure Security Benchmark - การตอบสนองต่อเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="cae0c-550">Azure Security Benchmark - Incident response</span></span>](/azure/security/benchmarks/security-controls-v2-incident-response)

- [<span data-ttu-id="cae0c-551">แนวทางปฏิบัติที่ดีที่สุดสำหรับการรักษาความปลอดภัย Azure 4 – กระบวนการ อัปเดตกระบวนการตอบสนองต่อเหตุการณ์สำหรับระบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="cae0c-551">Azure Security Best Practice 4 - Process. Update Incident Response Processes for Cloud</span></span>](/azure/cloud-adoption-framework/security/security-top-10#4-process-update-incident-response-ir-processes-for-cloud)

- [<span data-ttu-id="cae0c-552">เฟรมเวิร์กการปรับใช้งาน Azure การบันทึก และคู่มือการตัดสินใจในการรายงาน</span><span class="sxs-lookup"><span data-stu-id="cae0c-552">Azure Adoption Framework, logging, and reporting decision guide</span></span>](/azure/cloud-adoption-framework/decision-guides/logging-and-reporting/)

- [<span data-ttu-id="cae0c-553">ขนาดองค์กร การจัดการ และการตรวจสอบ Azure</span><span class="sxs-lookup"><span data-stu-id="cae0c-553">Azure enterprise scale, management, and monitoring</span></span>](/azure/cloud-adoption-framework/ready/enterprise-scale/management-and-monitoring)

<span data-ttu-id="cae0c-554">**การตรวจสอบศูนย์รักษาความปลอดภัย Azure**: ไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="cae0c-554">**Azure Security Center monitoring**: Not applicable</span></span>

<span data-ttu-id="cae0c-555">**ความรับผิดชอบ**: ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cae0c-555">**Responsibility**: Customer</span></span>

## <a name="next-steps"></a><span data-ttu-id="cae0c-556">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="cae0c-556">Next steps</span></span>

- <span data-ttu-id="cae0c-557">โปรดดู[ภาพรวมของ Azure Security Benchmark V2](/azure/security/benchmarks/overview)</span><span class="sxs-lookup"><span data-stu-id="cae0c-557">See the [Azure Security Benchmark V2 overview](/azure/security/benchmarks/overview)</span></span>
- <span data-ttu-id="cae0c-558">เรียนรู้เพิ่มเติมเกี่ยวกับ[อมูลพื้นฐานด้านความปลอดภัย Azure](/azure/security/benchmarks/security-baselines-overview)</span><span class="sxs-lookup"><span data-stu-id="cae0c-558">Learn more about [Azure security baselines](/azure/security/benchmarks/security-baselines-overview)</span></span>