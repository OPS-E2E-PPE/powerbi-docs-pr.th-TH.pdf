---
title: ลงชื่อเข้าระบบครั้งเดียวในแอปมือถือ Power BI สำหรับ Windows
description: อ่านเกี่ยวกับการลงชื่อเข้าระบบครั้งเดียว (SSO) ในแอปมือถือ Power BI สำหรับ Windows SSO หมายความว่าคุณเข้าถึงแอปพลิเคชันและทรัพยากรทั้งหมดที่คุณต้องทำธุรกิจโดยลงชื่อเข้าใช้เพียงครั้งเดียวโดยใช้บัญชีผู้ใช้คนเดียว
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 03/11/2020
ms.openlocfilehash: b316c7b95b28ecb31561b3fbb99eeafa6ffabdb5
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415277"
---
# <a name="single-sign-on-in-the-power-bi-mobile-windows-app"></a><span data-ttu-id="7563c-104">ลงชื่อเข้าระบบครั้งเดียวในแอปมือถือ Power BI สำหรับ Windows</span><span class="sxs-lookup"><span data-stu-id="7563c-104">Single Sign-On in the Power BI mobile Windows app</span></span>

<span data-ttu-id="7563c-105">อ่านเกี่ยวกับการลงชื่อเข้าระบบครั้งเดียว (SSO) ในแอปมือถือ Power BI สำหรับ Windows</span><span class="sxs-lookup"><span data-stu-id="7563c-105">Read about Single Sign-On (SSO) in the Power BI mobile Windows app.</span></span> <span data-ttu-id="7563c-106">SSO หมายความว่าคุณเข้าถึงแอปพลิเคชันและทรัพยากรทั้งหมดที่คุณต้องทำธุรกิจโดยลงชื่อเข้าใช้เพียงครั้งเดียวโดยใช้บัญชีผู้ใช้คนเดียว</span><span class="sxs-lookup"><span data-stu-id="7563c-106">SSO means you access all the applications and resources you need to do business by signing in only once, with a single user account.</span></span> <span data-ttu-id="7563c-107">เมื่อลงชื่อเข้าใช้แล้ว คุณสามารถเข้าถึงแอปพลิเคชันทั้งหมดได้โดยไม่ต้องตรวจสอบสิทธิ์อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="7563c-107">Once you're signed in, you can access all those applications without having to authenticate again.</span></span> 

<span data-ttu-id="7563c-108">เนื่องจากแอป Power BI Windows ถูกรวมเข้ากับ Azure Active Directory คุณจึงสามารถใช้บัญชีองค์กรหลักของคุณได้ไม่เพียงแต่จะลงชื่อเข้าใช้อุปกรณ์ที่ใช้โดเมนร่วมกันเท่านั้น แต่ยังลงชื่อเข้าใช้บริการ Power BI ด้วย</span><span class="sxs-lookup"><span data-stu-id="7563c-108">Because the Power BI Windows app is integrated into Azure Active Directory, you can use your primary organizational account not only to sign in to your domain-joined devices, but also to sign in to the Power BI service.</span></span> <span data-ttu-id="7563c-109">หากคุณกำลังดู Power BI บนวินโดว์โฟน คุณต้องตรวจสอบให้แน่ใจว่าบัญชีที่คุณใช้สำหรับ Power BI ได้รับการกำหนดค่าเป็นบัญชีที่ทำงานหรือบัญชีโรงเรียนในการตั้งค่าอุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="7563c-109">If you're viewing Power BI on a Windows phone, you make sure the account you use for Power BI is configured as a work or school account in the device settings.</span></span>  

<span data-ttu-id="7563c-110">SSO จะเปิดใช้งานสำหรับอุปกรณ์ Windows ที่จัดการโดย Azure Active Directory เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="7563c-110">SSO is enabled only for Windows devices managed by Azure Active Directory.</span></span>

>[!NOTE]
><span data-ttu-id="7563c-111">การสนับสนุนแอปอุปกรณ์เคลื่อนที่ Power BI สำหรับ **โทรศัพท์ที่ใช้ Windows 10 Mobile** จะถูกยกเลิกในวันที่ 16 มีนาคม 2021</span><span class="sxs-lookup"><span data-stu-id="7563c-111">Power BI mobile app support for **phones using Windows 10 Mobile** will be discontinued on March 16, 2021.</span></span> [<span data-ttu-id="7563c-112">เรียนรู้เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7563c-112">Learn more</span></span>](/legal/powerbi/powerbi-mobile/power-bi-mobile-app-end-of-support-for-windows-phones)

## <a name="sign-in-with-sso"></a><span data-ttu-id="7563c-113">ลงชื่อเข้าใช้ด้วย SSO</span><span class="sxs-lookup"><span data-stu-id="7563c-113">Sign in with SSO</span></span>

<span data-ttu-id="7563c-114">เมื่อต้องการลดความซับซ้อนของกระบวนการลงชื่อเข้าใช้ เมื่อคุณติดตั้งแอปเป็นครั้งแรก แอปจะพยายามรับรองความถูกต้องไปยังบริการ Power BI โดยใช้ SSO โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7563c-114">To simplify the sign-in process, when you install the app for the first time the app automatically tries to authenticate you to the Power BI service using SSO.</span></span> <span data-ttu-id="7563c-115">เฉพาะในกรณีที่กระบวนการนี้ไม่ประสบความสำเร็จ แอปจะขอให้คุณระบุข้อมูลประจำตัวสำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="7563c-115">Only if this process doesn't succeed does the app ask you to provide your credentials for Power BI.</span></span>  

<span data-ttu-id="7563c-116">หากคุณใช้แอปมือถือ Power BI สำหรับ Windows แล้ว เมื่อคุณอัปเกรดเป็นแอปเวอร์ชันใหม่ คุณสามารถใช้ SSO ได้</span><span class="sxs-lookup"><span data-stu-id="7563c-116">If you're already using the Power BI mobile app for Windows, when you upgrade to the new version of the app you can also use SSO.</span></span> <span data-ttu-id="7563c-117">ลงชื่อออกจากแอป ปิดและเปิดอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="7563c-117">Sign out of the app, close it, and reopen it.</span></span> <span data-ttu-id="7563c-118">เมื่อเปิดแอปใหม่ ระบบจะพยายามใช้ข้อมูลประจำตัว Windows ปัจจุบันของคุณโดยอัตโนมัติเพื่อตรวจสอบความถูกต้องกับบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="7563c-118">When the app reopens, it automatically tries to use your current Windows credentials to authenticate against the Power BI service.</span></span> 

<span data-ttu-id="7563c-119">ถ้าคุณไม่ต้องการใช้ข้อมูลประจำตัวในเซสชั่นที่ใช้งานอยู่ของ Windows ในปัจจุบันเพื่อลงชื่อเข้าใช้ Power BI เพียงไปที่ **การตั้งค่า** ออกจากระบบ และลงชื่อเข้าใช้ด้วยข้อมูลประจำตัวที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="7563c-119">If you don't want to use your current Windows active session credentials to sign in to Power BI, just go to **Settings**, sign out, and sign in with different credentials.</span></span> 
 
## <a name="next-steps"></a><span data-ttu-id="7563c-120">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="7563c-120">Next steps</span></span>

- [<span data-ttu-id="7563c-121">เริ่มต้นใช้งานแอป Power BI สำหรับอุปกรณ์เคลื่อนที่สำหรับ Windows 10</span><span class="sxs-lookup"><span data-stu-id="7563c-121">Get started with the Power BI mobile app for Windows 10</span></span>](mobile-windows-10-phone-app-get-started.md)
- <span data-ttu-id="7563c-122">มีคำถามหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="7563c-122">Questions?</span></span> [<span data-ttu-id="7563c-123">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="7563c-123">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
