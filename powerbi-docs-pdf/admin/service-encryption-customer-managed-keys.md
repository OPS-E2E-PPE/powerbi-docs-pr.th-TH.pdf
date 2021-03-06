---
title: ใช้คีย์ที่ลูกค้าจัดการใน Power BI
description: ศึกษาวิธีการใช้คีย์ที่ลูกค้าจัดการใน Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: how-to
ms.date: 11/11/2020
LocalizationGroup: Premium
ms.openlocfilehash: 215c84b9af9d3b785c055d633a41b99bbea2bb2f
ms.sourcegitcommit: cc20b476a45bccb870c9de1d0b384e2c39e25d24
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/11/2020
ms.locfileid: "94512596"
---
# <a name="use-customer-managed-keys-in-power-bi"></a>ใช้คีย์ที่ลูกค้าจัดการใน Power BI

Power BI เข้ารหัสข้อมูลที่พักอยู่และในระหว่างการดำเนินการ ตามค่าเริ่มต้น Power BI ใช้คีย์ที่จัดการโดย Microsoft เพื่อเข้ารหัสลับข้อมูลของคุณ องค์กรสามารถเลือกใช้คีย์ของตนเองเพื่อเข้ารหัสเนื้อหาของผู้ใช้ในทั้งหมดใน Power BI จากภาพรายงานเพื่อนำเข้าชุดข้อมูลในความจุแบบพรีเมียมได้ 

## <a name="why-use-customer-managed-keys"></a>เหตุใดจึงต้องใช้คีย์ที่ลูกค้าจัดการ

ด้วยการใช้คีย์ที่ลูกค้าจัดการของ Power BI (CMK) องค์กะรสามารถตอบสนองความต้องการด้านการปฏิบัติตามข้อกำหนดสำหรับการเข้ารหัสข้อมูลที่อยู่กับผู้บริการคลาวด์ของตน (ซึ่งในกรณีนี้คือ Microsoft) CMK จะถูกเสนอให้กับลูกค้า Power BI Premium ใหม่เท่านั้นและจะทำให้องค์กรสามารถเข้ารหัสเนื้อหาของผู้ใช้ Power BI ของพวกเขาด้วยการใช้คีย์ที่ให้และจัดการได้ การเลิกใช้คีย์ที่ลูกค้าจัดการจะทำให้ทุกคนไม่สามารถอ่านเนื้อหาของผู้ใช้ภายใน Power BI ได้ภายในเวลาหนึ่งชั่วโมงรวมถึง Microsoft ด้วย เมื่อเปรียบเทียบกับการเสนอ BYOK CMK ยังครอบคลุมเนื้อหาของผู้ใช้ที่สร้างขึ้นโดยบริการ นอกเหนือจากข้อมูลลูกค้าที่นำเข้าไปในรายงานและชุดข้อมูลที่โฮสต์บนความจุแบบพรีเมียม ซึ่งจะบังคับใช้นโยบายการแคชที่เข้มงวดขึ้นและสามารถใช้คีย์เดียวเพื่อเข้ารหัสข้อมูลทั้งหมดได้


## <a name="how-to-use-customer-managed-keys"></a>วิธีการใช้คีย์ที่ลูกค้าจัดการ
เมื่อต้องการเข้าร่วมในคีย์ Power BI ที่จัดการโดยลูกค้า องค์กรของคุณจะต้องติดต่อผู้จัดการบัญชี Microsoft ขององค์กรของคุณเพื่อตรวจสอบว่าองค์กรของคุณมีขนาดตรงตามข้อกำหนดที่จำเป็นสำหรับการเปิดใช้งาน CMK  


## <a name="next-steps"></a>ขั้นตอนถัดไป

สามารถดูข้อมูลต่าง ๆ ที่มีประโยชน์ต่อการใช้คีย์ที่ลูกค้าเป็นผู้จัดการได้ที่ลิงค์ต่าง ๆ ดังต่อไปนี้:

* [นำคีย์การเข้ารหัสลับของคุณเองมาใช้กับ Power BI](service-encryption-byok.md)
* [กำหนดค่าการสนับสนุน Multi-Geo สำหรับ Power BI Premium](service-admin-premium-multi-geo.md)
* [วิธีการทำงานของความจุ](service-premium-what-is.md#how-capacities-function)
* [การรีเฟรชแบบเพิ่มหน่วย](service-premium-incremental-refresh.md)
