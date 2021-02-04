---
title: รวมถึงไฟล์
description: รวมไฟล์
services: powerbi
author: davidiseminger
ms.service: powerbi
ms.topic: include
ms.date: 04/28/2020
ms.author: davidi
ms.openlocfilehash: ed87101fe7f5fadd24594d53bbd0ffb6f029faa4
ms.sourcegitcommit: 92b033ee7a6e36808371b247b7b41536cee6c2f6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/10/2020
ms.locfileid: "90012878"
---
## <a name="single-sign-on"></a><span data-ttu-id="3090e-103">ลงชื่อเข้าระบบครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="3090e-103">Single sign-on</span></span>

<span data-ttu-id="3090e-104">หลังจากที่คุณเผยแพร่ยังชุดข้อมูล Azure SQL DirectQuery ไปยังบริการแล้ว คุณสามารถอนุญาตให้ผู้ใช้งานของคุณลงชื่อเข้าระบบครั้งเดียว (SSO) ได้โดยใช้ OAuth2 ของ Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="3090e-104">After you publish an Azure SQL DirectQuery dataset to the service, you can enable single sign-on (SSO) using Azure Active Directory (Azure AD) OAuth2 for your end users.</span></span>

<span data-ttu-id="3090e-105">เมื่อต้องการเปิดใช้งาน SSO ไปที่การตั้งค่าสำหรับชุดข้อมูล เปิดแท็บ**แหล่งข้อมูล** แล้วเลือกกล่อง SSO</span><span class="sxs-lookup"><span data-stu-id="3090e-105">To enable SSO, go to settings for the dataset, open the **Data Sources** tab, and check the SSO box.</span></span>

![กำหนดค่ากล่องโต้ตอบ Azure SQL DQ](media/direct-query-sso/sso-dialog.png)

<span data-ttu-id="3090e-107">เมื่อเปิดใช้งานตัวเลือก SSO และผู้ใช้ของคุณเข้าถึงรายงานที่สร้างขึ้นบนยอดของแหล่งข้อมูล Power BI จะส่งข้อมูลประจำตัวที่รับรองความถูกต้อง Azure AD ของผู้ใช้ในการสอบถามไปยังฐานข้อมูล Azure SQL หรือคลังข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3090e-107">When the SSO option is enabled and your users access reports built atop the data source, Power BI sends their authenticated Azure AD credentials in the queries to the Azure SQL database or data warehouse.</span></span> <span data-ttu-id="3090e-108">ตัวเลือกนี้จะช่วยให้ Power BI เป็นไปตามการตั้งค่าความปลอดภัยที่มีการกำหนดค่าในระดับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3090e-108">This option enables Power BI to respect the security settings that are configured at the data source level.</span></span>

<span data-ttu-id="3090e-109">ตัวเลือก SSO จะมีผลต่อชุดข้อมูลทั้งหมดที่ใช้แหล่งข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="3090e-109">The SSO option takes affect across all datasets that use this data source.</span></span> <span data-ttu-id="3090e-110">แต่จะไม่มีผลต่อวิธีการรับรองความถูกต้องที่ใช้สำหรับสถานการณ์สมมติการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="3090e-110">It does not affect the authentication method used for import scenarios.</span></span>

> [!Note]
> <span data-ttu-id="3090e-111">ไม่รองรับ Azure Multi-Factor Authentication (MFA)</span><span class="sxs-lookup"><span data-stu-id="3090e-111">Azure Multi-Factor Authentication (MFA) is not supported.</span></span> <span data-ttu-id="3090e-112">ผู้ใช้ที่ต้องการใช้ SSO กับDirectQuery ต้องได้รับการยกเว้นจาก MFA</span><span class="sxs-lookup"><span data-stu-id="3090e-112">Users who want to use SSO with DirectQuery must be exempted from MFA.</span></span>
