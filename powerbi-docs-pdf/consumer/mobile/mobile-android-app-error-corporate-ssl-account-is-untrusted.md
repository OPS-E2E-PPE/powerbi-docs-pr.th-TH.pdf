---
title: การแก้ไข “ไม่เชื่อถือใบรับรอง SSL ขององค์กรของคุณ”
description: เมื่อลงชื่อเข้าใช้แอป Android สำหรับ Power BI คุณอาจเห็นข้อความว่า "ไม่สามารถรับรองความถูกต้องเนื่องจากใบรับรอง SSL ขององค์กรของคุณไม่น่าเชื่อถือ
author: paulinbar
ms.author: painbar
.": ''
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 03/11/2020
ms.openlocfilehash: b435d3883207099287b6c0373f13063ebb23b694
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414679"
---
# <a name="fixing-corporate-ssl-certificate-is-untrusted---power-bi"></a><span data-ttu-id="809ba-103">การแก้ไข “ไม่เชื่อถือใบรับรอง SSL ขององค์กรของคุณ” - Power BI</span><span class="sxs-lookup"><span data-stu-id="809ba-103">Fixing "Corporate SSL certificate is untrusted" - Power BI</span></span>
<span data-ttu-id="809ba-104">เมื่อลงชื่อเข้าใช้แอป Android บนมือถือสำหรับ Microsoft Power BI คุณอาจเห็นข้อความว่า "ไม่สามารถรับรองความถูกต้องเนื่องจากใบรับรอง SSL ขององค์กรของคุณไม่น่าเชื่อถือโดยอุปกรณ์นี้</span><span class="sxs-lookup"><span data-stu-id="809ba-104">When signing in to the Android mobile app for Microsoft Power BI, you may see the message, "Could not authenticate because your corporate SSL certificate is untrusted by this device.</span></span> <span data-ttu-id="809ba-105">โปรดติดต่อผู้ดูแลระบบไอทีบริษัทของคุณ"</span><span class="sxs-lookup"><span data-stu-id="809ba-105">Contact your company IT admin."</span></span> 

<span data-ttu-id="809ba-106">สิ่งที่คุณต้องทำมักจะขึ้นอยู่กับระบบปฏิบัติการบนอุปกรณ Android ของคุณ แต่มีปัญหาอื่นๆที่อาจทำให้เกิดข้อผิดพลาดนี้</span><span class="sxs-lookup"><span data-stu-id="809ba-106">What you need to do usually depends on the operating system on your Android device, but there are a couple of other issues that may cause this error.</span></span>

## <a name="on-android-7-or-later"></a><span data-ttu-id="809ba-107">Android 7 หรือรุ่นใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="809ba-107">On Android 7 or later</span></span>
<span data-ttu-id="809ba-108">ค้นหาการอัปเดตสำหรับแอปที่มีชื่อว่า **Chrome** และติดตั้งการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="809ba-108">Look for an update for an app named **Chrome**, and install the update.</span></span>

## <a name="on-android-6-and-earlier"></a><span data-ttu-id="809ba-109">Android 6 และรุ่นก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="809ba-109">On Android 6 and earlier</span></span>
<span data-ttu-id="809ba-110">อุปกรณ์ของคุณอาจต้องใช้ System Webview รุ่นที่อัปเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="809ba-110">Your device may need an updated version of System Webview.</span></span> <span data-ttu-id="809ba-111">ซึ่งอาจติดตั้งในอุปกรณ์ของคุณและคุณเพียงแค่คลิก **อัปเดต**</span><span class="sxs-lookup"><span data-stu-id="809ba-111">It may be installed on your device, and you may just need to click **Update**.</span></span>

<span data-ttu-id="809ba-112">หากไม่ได้ติดตั้ง System Webview ไว้ในอุปกรณ์ของคุณ:</span><span class="sxs-lookup"><span data-stu-id="809ba-112">If System Webview isn't installed on your device:</span></span>

1. <span data-ttu-id="809ba-113">ปิด Power BI บนอุปกรณ์ Android ของคุณ</span><span class="sxs-lookup"><span data-stu-id="809ba-113">On your Android device, close Power BI.</span></span>
2. <span data-ttu-id="809ba-114">เปิด Google Play Store และค้นหา **System Webview** โดย Google Inc.</span><span class="sxs-lookup"><span data-stu-id="809ba-114">Open the Google Play Store and search for **System Webview** by Google Inc.</span></span>
3. <span data-ttu-id="809ba-115">ติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="809ba-115">Install it.</span></span>
4. <span data-ttu-id="809ba-116">รีสตาร์ทแอป Power BI และลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="809ba-116">Restart the Power BI app and sign in.</span></span>

## <a name="time-zone-settings"></a><span data-ttu-id="809ba-117">การตั้งค่าเขตเวลา</span><span class="sxs-lookup"><span data-stu-id="809ba-117">Time-zone settings</span></span>
<span data-ttu-id="809ba-118">การตั้งค่าเขตเวลาในอุปกรณ์อาจผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="809ba-118">Time-zone settings on your device may be wrong.</span></span> 

<span data-ttu-id="809ba-119">ไปที่ **การตั้งค่า** > **ระบบ** > **วันที่และเวลา** เพื่อตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="809ba-119">Go to **Settings** > **System** > **Date and time** to check them.</span></span>

## <a name="custom-authentication-server"></a><span data-ttu-id="809ba-120">เซิร์ฟเวอร์การรับรองความถูกต้องแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="809ba-120">Custom authentication server</span></span>
<span data-ttu-id="809ba-121">หากคุณใช้เซิร์ฟเวอร์การรับรองความถูกต้องแบบกำหนดเอง ใบรับรอง SSL ในเซิร์ฟเวอร์การรับรองความถูกต้องขององค์กรอาจไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="809ba-121">If you're using a custom authentication server, the SSL certificate in the corporate authentication server may not be valid.</span></span> <span data-ttu-id="809ba-122">ทำงานร่วมกันกับฝ่าย IT ในองค์กรของคุณ เพื่อทดสอบการรับรองความถูกต้องของการกำหนดค่าเซิร์ฟเวอร์องค์กร โดยทำตามคำแนะนำใน[บทความนี้](https://support.microsoft.com/help/3203929/using-adal-to-authenticate-from-android-devices-fails-if-additional-ce)</span><span class="sxs-lookup"><span data-stu-id="809ba-122">Work with your organization's IT to test the corporate authentication server configuration, by following the guidance in [this article](https://support.microsoft.com/help/3203929/using-adal-to-authenticate-from-android-devices-fails-if-additional-ce).</span></span>

## <a name="next-steps"></a><span data-ttu-id="809ba-123">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="809ba-123">Next steps</span></span>
* <span data-ttu-id="809ba-124">[ดาวน์โหลดแอป Android](https://go.microsoft.com/fwlink/?LinkID=544867) จาก Android app store.</span><span class="sxs-lookup"><span data-stu-id="809ba-124">[Download the Android app](https://go.microsoft.com/fwlink/?LinkID=544867) from the Android app store.</span></span>
* <span data-ttu-id="809ba-125">มีคำถามหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="809ba-125">Questions?</span></span> [<span data-ttu-id="809ba-126">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="809ba-126">Try asking the Power BI Community</span></span>](https://community.powerbi.com/) 

