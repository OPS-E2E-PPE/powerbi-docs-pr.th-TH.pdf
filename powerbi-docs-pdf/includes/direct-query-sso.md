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
## <a name="single-sign-on"></a>ลงชื่อเข้าระบบครั้งเดียว

หลังจากที่คุณเผยแพร่ยังชุดข้อมูล Azure SQL DirectQuery ไปยังบริการแล้ว คุณสามารถอนุญาตให้ผู้ใช้งานของคุณลงชื่อเข้าระบบครั้งเดียว (SSO) ได้โดยใช้ OAuth2 ของ Azure Active Directory (Azure AD)

เมื่อต้องการเปิดใช้งาน SSO ไปที่การตั้งค่าสำหรับชุดข้อมูล เปิดแท็บ**แหล่งข้อมูล** แล้วเลือกกล่อง SSO

![กำหนดค่ากล่องโต้ตอบ Azure SQL DQ](media/direct-query-sso/sso-dialog.png)

เมื่อเปิดใช้งานตัวเลือก SSO และผู้ใช้ของคุณเข้าถึงรายงานที่สร้างขึ้นบนยอดของแหล่งข้อมูล Power BI จะส่งข้อมูลประจำตัวที่รับรองความถูกต้อง Azure AD ของผู้ใช้ในการสอบถามไปยังฐานข้อมูล Azure SQL หรือคลังข้อมูล ตัวเลือกนี้จะช่วยให้ Power BI เป็นไปตามการตั้งค่าความปลอดภัยที่มีการกำหนดค่าในระดับแหล่งข้อมูล

ตัวเลือก SSO จะมีผลต่อชุดข้อมูลทั้งหมดที่ใช้แหล่งข้อมูลนี้ แต่จะไม่มีผลต่อวิธีการรับรองความถูกต้องที่ใช้สำหรับสถานการณ์สมมติการนำเข้า

> [!Note]
> ไม่รองรับ Azure Multi-Factor Authentication (MFA) ผู้ใช้ที่ต้องการใช้ SSO กับDirectQuery ต้องได้รับการยกเว้นจาก MFA
