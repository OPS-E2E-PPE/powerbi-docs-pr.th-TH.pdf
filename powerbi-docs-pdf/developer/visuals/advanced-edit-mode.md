---
title: โหมดแก้ไขขั้นสูงของวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายถึงวิธีการตั้งค่าการควบคุม UI ขั้นสูงในวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.date: 06/18/2019
ms.openlocfilehash: 02f02f23d3dfd7ec514e17d1bab17be715e9cd7d
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97889144"
---
# <a name="advanced-edit-mode-in-power-bi-visuals"></a>โหมดการแก้ไขขั้นสูงในวิชวล Power BI

หากคุณต้องการการควบคุม UI ขั้นสูงในวิชวล Power BI คุณสามารถใช้ประโยชน์จากโหมดแก้ไขขั้นสูงได้ เมื่อคุณอยู่ในโหมดแก้ไขรายงาน ให้คุณเลือกปุ่ม **แก้ไข** เพื่อตั้งโหมดแก้ไขเป็น **ขั้นสูง** ภาพสามารถใช้ค่าสถานะ `EditMode` เพื่อพิจารณาว่าควรแสดงการควบคุม UI นี้หรือไม่

ตามค่าเริ่มต้น วิชวลไม่สนับสนุนโหมดการแก้ไขขั้นสูง คุณสามารถระบุสิ่งนี้ได้อย่างชัดเจนในไฟล์ *capabilities.json* ของวิชวลโดยการตั้งค่าคุณสมบัติ `advancedEditModeSupport`

ค่าที่เป็นไปได้คือ:

- `0` - NotSupported

- `1` - SupportedNoAction

- `2` - SupportedInFocus

## <a name="enter-advanced-edit-mode"></a>ป้อนโหมดการแก้ไขขั้นสูง

ปุ่ม **แก้ไข** จะแสดงขึ้นมาถ้า:

* คุณสมบัติ `advancedEditModeSupport` ถูกตั้งค่าในไฟล์ *capabilities.json* เป็น `SupportedNoAction` หรือ `SupportedInFocus`

* แสดงผลวิชวลในโหมดการแก้ไขรายงาน

หากคุณสมบัติ `advancedEditModeSupport` หายไปจากไฟล์ *capabilities.json* หรือตั้งค่าเป็น `NotSupported` ปุ่ม **แก้ไข** จะไม่ปรากฏขึ้น

![เข้าสู่โหมดการแก้ไข](media/advanced-edit-mode/edit-mode.png)

เมื่อคุณเลือก **แก้ไข** วิชวลจะทำการเรียกใช้ update() โดยมีการตั้งค่า EditMode เป็น `Advanced` ขึ้นอยู่กับค่าที่ตั้งไว้ในไฟล์ *capabilities.json* การดำเนินการต่อไปนี้เกิดขึ้น:

* `SupportedNoAction`: ไม่ต้องการการดำเนินการเพิ่มเติมจากโฮสต์
* `SupportedInFocus`: โฮสต์จะเปิดหน้าต่างวิชวลใหม่ในโหมดโฟกัส

## <a name="exit-advanced-edit-mode"></a>ออกจากโหมดการแก้ไขขั้นสูง

ปุ่ม **กลับไปยังรายงาน** จะปรากฏขึ้น ถ้า:

* คุณสมบัติ `advancedEditModeSupport` ถูกตั้งค่าในไฟล์ *capabilities.json* เป็น `SupportedInFocus`
