---
title: ปกป้องข้อมูล Power BI พร้อมการระบเดิมของอุปกรณ์
description: เรียนรู้วิธีการกำหนดค่าแอป iOS และแอปแอนดรอยด์ของคุณเพื่อกำหนดการระบุเพิ่มเติมก่อนที่คุณสามารถเข้าถึงข้อมูล Power BI ของคุณ
author: paulinbar
ms.author: painbar
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 04/07/2020
ms.openlocfilehash: 9ca31aa16d74ab89b9af374244d2696f77dedac6
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413069"
---
# <a name="protect-power-bi-app-with-face-id-touch-id-passcode-or-biometric-data"></a><span data-ttu-id="5554b-103">ปกป้องแอป Power BI ด้วย Face ID, Touch ID, รหัสผ่าน หรือข้อมูลทางชีวมิติ</span><span class="sxs-lookup"><span data-stu-id="5554b-103">Protect Power BI app with Face ID, Touch ID, passcode, or biometric data</span></span> 

<span data-ttu-id="5554b-104">ในหลายกรณี ข้อมูลที่จัดการใน Power BI จะถือเป็นความลับ และจำเป็นต้องได้รับการปกป้อง และการเข้าถึงได้โดยผู้ใช้ที่ได้รับอนุญาตเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5554b-104">In many cases, the data managed in Power BI is confidential and needs to be protected and accessed by authorized users only.</span></span> 

<span data-ttu-id="5554b-105">แอป Power BI สำหรับ iOS และแอนดรอยด์ช่วยให้คุณสามารถปกป้องข้อมูลของคุณได้โดยการกำหนดค่าการระบุเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5554b-105">The Power BI apps for iOS and Android let you protect your data by configuring additional identification.</span></span> <span data-ttu-id="5554b-106">จากนั้น ผู้ใช้จะต้องทำการยืนยันตัวตนทุกครั้งที่มีการเปิดใช้งานแอปหรือนำแอปขึ้นมาที่เบื้องหน้า</span><span class="sxs-lookup"><span data-stu-id="5554b-106">Then, every time the app is launched or brought to the foreground, identification will be required.</span></span> <span data-ttu-id="5554b-107">สำหรับ iOS กรณีนี้หมายความว่าคุณต้องให้ Face ID, Touch ID หรือรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="5554b-107">On iOS, this means providing Face ID, Touch ID, or a passcode.</span></span> <span data-ttu-id="5554b-108">สำหรับแอนดรอยด์ กรณีนี้หมายความว่าคุณต้องให้ข้อมูลทางชีวมิติ (Fingerprint ID)</span><span class="sxs-lookup"><span data-stu-id="5554b-108">On Android, it means providing biometric data (Fingerprint ID).</span></span>

<span data-ttu-id="5554b-109">ใช้ได้กับ:</span><span class="sxs-lookup"><span data-stu-id="5554b-109">Applies to:</span></span>

| ![iPhone](./media/mobile-native-secure-access/ios-logo-40-px.png) | ![iPad](./media/mobile-native-secure-access/ios-logo-40-px.png) | ![มือถือ Android](././media/mobile-native-secure-access/android-logo-40-px.png) | ![แท็บเล็ต Android](././media/mobile-native-secure-access/android-logo-40-px.png) |
|:--- |:--- |:--- |:--- |
|<span data-ttu-id="5554b-114">iPhones</span><span class="sxs-lookup"><span data-stu-id="5554b-114">iPhones</span></span> |<span data-ttu-id="5554b-115">iPad</span><span class="sxs-lookup"><span data-stu-id="5554b-115">iPads</span></span> |<span data-ttu-id="5554b-116">มือถือ Android</span><span class="sxs-lookup"><span data-stu-id="5554b-116">Android phones</span></span> |<span data-ttu-id="5554b-117">แท็บเล็ต Android</span><span class="sxs-lookup"><span data-stu-id="5554b-117">Android tablets</span></span> |

## <a name="turn-on-face-id-touch-id-or-passcode-on-ios"></a><span data-ttu-id="5554b-118">เปิด Face ID, Touch ID หรือรหัสผ่านบน iOS</span><span class="sxs-lookup"><span data-stu-id="5554b-118">Turn on Face ID, Touch ID, or passcode on iOS</span></span>

<span data-ttu-id="5554b-119">เพื่อใช้การยืนยันตัวตนเพิ่มเติมในแอป Power BI มือถือสำหรับ iOS ให้ไปที่การตั้งค่าแอปภายใต้ **ความเป็นส่วนตัวและการรักษาความปลอดภัย**</span><span class="sxs-lookup"><span data-stu-id="5554b-119">To use additional identification in the Power BI mobile app for iOS, go to the app setting under **Privacy and Security**.</span></span> <span data-ttu-id="5554b-120">คุณจะเห็นตัวเลือกในการเปิด Face ID, Touch ID หรือรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="5554b-120">You'll see the option to turn on Face ID, Touch ID, or passcode.</span></span> <span data-ttu-id="5554b-121">ซึ่งตัวเลือกต่าง ๆ ที่มีจะขึ้นอยู่กับความสามารถของอุปกรณ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5554b-121">The options you see depend on the capabilities of your device.</span></span>

![หน้าการตั้งค่าแอป iOS ของ Power BI](./media/mobile-native-secure-access/mobile-ios-native-secured-setting.png)

<span data-ttu-id="5554b-123">เมื่อเปิดใช้งานการตั้งค่านี้ ทุกครั้งที่คุณเปิดใช้งานแอป Power BI หรือนำแอปขึ้นมาสู่ด้านบน ระบบจะขอให้คุณระบุ ID ของคุณก่อนที่คุณสามารถเข้าถึงแอปได้</span><span class="sxs-lookup"><span data-stu-id="5554b-123">When this setting is turned on, every time you launch the app or bring it to the foreground, it will ask you to provide your ID before you can access the app.</span></span>

<span data-ttu-id="5554b-124">ชนิดของ ID ที่ระบบร้องขอจากคุณจะขึ้นอยู่กับความสามารถของอุปกรณ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5554b-124">The type of ID you will be asked to provide depends on your device's capabilities.</span></span> <span data-ttu-id="5554b-125">ถ้าอุปกรณ์ของคุณสนับสนุน Face ID คุณจำเป็นต้องใช้ Face ID</span><span class="sxs-lookup"><span data-stu-id="5554b-125">If your device supports Face ID, you'll need to use Face ID.</span></span> <span data-ttu-id="5554b-126">ถ้าสนับสนุน Touch ID คุณจำเป็นต้องใช้ Touch ID</span><span class="sxs-lookup"><span data-stu-id="5554b-126">If it supports Touch ID, you'll need to use Touch ID.</span></span> <span data-ttu-id="5554b-127">ถ้าอุปกรณ์ของคุณรองรับทั้งสองระบบ จากนั้นคุณจำเป็นต้องระบุรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="5554b-127">If neither are supported, then you'll need to provide a passcode.</span></span> <span data-ttu-id="5554b-128">รูปภาพด้านล่างแสดงให้เห็นถึงหน้าจอการรับรองความถูกต้องของ Face ID</span><span class="sxs-lookup"><span data-stu-id="5554b-128">The image below shows the Face ID authentication screen.</span></span>

![Face ID ระบบ iOS ของ Power BI](./media/mobile-native-secure-access/mobile-ios-native-secured-faceid.png)

## <a name="turn-on-biometric-data-fingerprint-id-on-android"></a><span data-ttu-id="5554b-130">เปิดใช้งานข้อมูลทางชีวมิติ (Fingerprint ID) บนแอนดรอยด์</span><span class="sxs-lookup"><span data-stu-id="5554b-130">Turn on biometric data (Fingerprint ID) on Android</span></span>

<span data-ttu-id="5554b-131">เพื่อใช้การยืนยันตัวตนเพิ่มเติมในแอป Power BI มือถือสำหรับแอนดรอยด์ ให้ไปที่การตั้งค่าแอปภายใต้ **ความเป็นส่วนตัวและการรักษาความปลอดภัย**</span><span class="sxs-lookup"><span data-stu-id="5554b-131">To use additional identification in the Power BI mobile app for Android, go to the app setting under **Privacy and Security**.</span></span> <span data-ttu-id="5554b-132">คุณจะเห็นตัวเลือกเพื่อเปิดใช้งานข้อมูลทางชีวมิติ</span><span class="sxs-lookup"><span data-stu-id="5554b-132">You'll see the option to turn on biometric data.</span></span>

![หน้าการตั้งค่าแอป Power BI สำหรับแอนดรอยด์](./media/mobile-native-secure-access/mobile-android-native-secured-setting.png)

<span data-ttu-id="5554b-134">เมื่อเปิดใช้งานการตั้งค่านี้ ทุกครั้งที่คุณเปิดใช้งานแอป Power BI หรือนำแอปขึ้นมาสู่ด้านบน ระบบจะขอให้คุณระบุข้อมูลทางชีวมิติ (Fingerprint ID) ของคุณก่อนที่คุณสามารถเข้าถึงแอปได้</span><span class="sxs-lookup"><span data-stu-id="5554b-134">When this setting is turned on, every time you launch the app or bring it to the foreground, it will ask you to provide your biometric data (Fingerprint ID) before you can access the app.</span></span>

<span data-ttu-id="5554b-135">รูปภาพด้านล่างแสดงให้เห็นถึงหน้าจอการรับรองความถูกต้องด้วยลายนิ้วมือ</span><span class="sxs-lookup"><span data-stu-id="5554b-135">The image below shows the fingerprint authentication screen.</span></span>

![สกรีนช็อตแสดงข้อความระบุตัวตนเพิ่มเติมบนโทรศัพท์ Android](./media/mobile-native-secure-access/mobile-android-native-secured-fingerprint-id.png)

>[!NOTE]
><span data-ttu-id="5554b-137">เพื่อให้คุณสามารถใช้แอปสำหรับอุปกรณ์เคลื่อนที่ได้ คุณจำเป็นต้องทำการตั้งค่าการยืนยันความถูกต้องทางชีวมิติ ซึ่งคุณจะต้องตั้งค่าชีวมิติบนอุปกรณ์แอนดรอยด์ของคุณก่อน</span><span class="sxs-lookup"><span data-stu-id="5554b-137">To be able to use mobile app's  Require Biometric Authentification setting, you must first set up biometrics on your Android device.</span></span> <span data-ttu-id="5554b-138">ถ้าอุปกรณ์ของคุณไม่รองรับชีวมิติ คุณจะไม่สามารถป้องกันการเข้าถึงข้อมูล Power BI ของคุณโดยใช้การตั้งค่าแอปสำหรับอุปกรณ์เคลื่อนที่นี้ได้</span><span class="sxs-lookup"><span data-stu-id="5554b-138">If your device doesn't support biometrics, you will not be able to secure access to your Power BI data using this mobile app setting.</span></span>
>
><span data-ttu-id="5554b-139">ถ้าผู้ดูแลระบบของคุณได้[เปิดใช้งานการเข้าถึงจากระยะไกลแบบปลอดภัย](#mdm-enforcement-of-secure-access-to-your-power-bi-mobile-app)ของแอปสำหรับอุปกรณ์เคลื่อนที่ และคุณยังไม่ได้ตั้งค่าชีวมิติบนอุปกรณ์ของคุณเพื่อเข้าถึงแอป คุณต้องตั้งค่าดังกล่าวก่อน</span><span class="sxs-lookup"><span data-stu-id="5554b-139">If your administrator has [remotely turned on secure access](#mdm-enforcement-of-secure-access-to-your-power-bi-mobile-app) for the mobile app, you must set up biometrics on your device in order to access the app, if you haven't already done so.</span></span> <span data-ttu-id="5554b-140">ถ้าอุปกรณ์ของคุณไม่รองรับชีวมิติ การตั้งค่าระยะไกลจะไม่ส่งผลกระทบใด ๆ ต่อคุณ</span><span class="sxs-lookup"><span data-stu-id="5554b-140">If your device doesn't support biometrics, the remote setting will not affect you.</span></span> <span data-ttu-id="5554b-141">แต่การเข้าถึงแอปของคุณจะไม่มีการรักษาความปลอดภัยใด ๆ</span><span class="sxs-lookup"><span data-stu-id="5554b-141">Access to your mobile app will remain unsecured.</span></span>

## <a name="mdm-enforcement-of-secure-access-to-your-power-bi-mobile-app"></a><span data-ttu-id="5554b-142">MDM จะบังคับให้มีการเข้าถึงแอป Power BI บนอุปกรณ์เคลื่อนที่ของคุณอย่างปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="5554b-142">MDM enforcement of secure access to your Power BI mobile app.</span></span>

<span data-ttu-id="5554b-143">บางองค์กรมีนโยบายด้านความปลอดภัยและข้อกำหนดการปฏิบัติตามข้อบังคับที่บังคับใช้กับการระบุเพิ่มเติมก่อนที่คุณสามารถเข้าถึงข้อมูลที่มีความละเอียดอ่อนทางธุรกิจได้</span><span class="sxs-lookup"><span data-stu-id="5554b-143">Some organizations have security policies and compliance requirements that enforce additional identification before you can access business sensitive data.</span></span>

<span data-ttu-id="5554b-144">เพื่อสนับสนุนเรื่องนี้ แอป Power BI สำหรับอุปกรณ์เคลื่อนช่วยให้ผู้ดูแลระบบสามารถควบคุมการตั้งค่าการเข้าถึงแอปอย่างปลอดภัย โดยเข้าใช้การตั้งค่าการกำหนดค่าแอปจาก Microsoft Intune และโซลูชันการจัดการอุปกรณ์เคลื่อนที่ (MDM) อื่น</span><span class="sxs-lookup"><span data-stu-id="5554b-144">To support this, the Power BI mobile app allows admins to control the mobile app secure access setting by pushing the app configuration settings from Microsoft Intune and other mobile device management (MDM) solutions.</span></span> <span data-ttu-id="5554b-145">ผู้ดูแลระบบสามารถใช้นโยบายการปกป้องแอปเพื่อเปิดการตั้งค่านี้สำหรับผู้ใช้ทั้งหมด หรือกลุ่มของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="5554b-145">Admins can use the app protection policy to turn on this setting for all users or for a group of users.</span></span> <span data-ttu-id="5554b-146">คุณสามารถศึกษารายละเอียดได้ที่ [การใช้ MDM เพื่อกำหนดค่าแอป Power BI จากระยะไกลสำหรับอุปกรณ์เคลื่อนที่](mobile-app-configuration.md#data-protection-settings-ios-and-android)</span><span class="sxs-lookup"><span data-stu-id="5554b-146">See [Use MDM to remotely configure the Power BI mobile app](mobile-app-configuration.md#data-protection-settings-ios-and-android) for detail.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5554b-147">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="5554b-147">Next steps</span></span>
* [<span data-ttu-id="5554b-148">การใช้ MDM เพื่อกำหนดค่าแอป Power BI จากระยะไกลสำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="5554b-148">Use MDM to remotely configure Power BI mobile app</span></span>](mobile-app-configuration.md)
