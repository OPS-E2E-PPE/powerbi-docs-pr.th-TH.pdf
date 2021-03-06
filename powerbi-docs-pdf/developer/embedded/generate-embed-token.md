---
title: ข้อควรพิจารณาสําหรับการสร้างโทเค็นแบบฝังตัวในการวิเคราะห์แบบฝังตัวของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: เรียนรู้เกี่ยวกับข้อควรพิจารณา ข้อจำกัด และสิทธิ์ที่จำเป็นสำหรับการสร้างโทเค็นแบบฝัง เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.custom: ''
ms.date: 10/15/2020
ms.openlocfilehash: 2f8da415b40bc5d9a621e5a0df8c1edffbbc8791
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97886867"
---
# <a name="considerations-when-generating-an-embed-token"></a>ข้อควรพิจารณาเมื่อสร้างโทเค็นแบบฝัง

[สร้างโทเค็น](/rest/api/power-bi/embedtoken) คือ REST API ที่ให้คุณสร้างโทเค็นสำหรับฝังรายการ Power BI ในเว็บแอปหรือพอร์ทัล โทเค็นใช้เพื่ออนุญาตคำขอของคุณกับบริการ Power BI

API สร้างโทเค็นใช้ข้อมูลประจำตัวเดียว (ผู้ใช้หลักหรือหลักบริการ) เพื่อสร้างโทเค็นสำหรับผู้ใช้แต่ละรายขึ้นอยู่กับข้อมูลรับรองของผู้ใช้ในแอป (ข้อมูลประจำตัวที่มีประสิทธิภาพ)

หลังจากรับรองความถูกต้องสำเร็จแล้วจะได้รับสิทธิ์เข้าถึงข้อมูลที่เกี่ยวข้อง

>[!NOTE]
>โทเค็นสร้างจะใช้ได้เฉพาะเมื่อคุณ [*ฝังสำหรับลูกค้าของคุณ*](embed-sample-for-customers.md) (หรือที่เรียกว่าสถานการณ์ *แอปเป็นเจ้าของข้อมูล*)

คุณสามารถใช้ API ต่อไปนี้เพื่อสร้างโทเค็น:

* [แดชบอร์ด](/rest/api/power-bi/embedtoken/dashboards_generatetokeningroup)

* [ชุดข้อมูล](/rest/api/power-bi/embedtoken/datasets_generatetokeningroup)

* [สร้างโทเค็นสำหรับรายงานหลายรายการ](/rest/api/power-bi/embedtoken/generatetoken)


* [การสร้างรายงาน](/rest/api/power-bi/embedtoken/reports_generatetokenforcreateingroup)

* [รายงาน](/rest/api/power-bi/embedtoken/reports_generatetokeningroup)

* [ไทล์](/rest/api/power-bi/embedtoken/tiles_generatetokeningroup)

## <a name="workspace-versions"></a>เวอร์ชันพื้นที่ทำงาน

Power BI มีพื้นที่ทำงานสองเวอร์ชันพื้นที่ทำงาน *คลาสสิก* และพื้นที่ทำงาน *ใหม่* คุณสามารถเรียนรู้เพิ่มเติมเกี่ยวกับความแตกต่างระหว่างพื้นที่ทำงานเหล่านี้ได้ใน [ความแตกต่างของพื้นที่ทำงานแบบใหม่และแบบคลาสสิก](../../collaborate-share/service-new-workspaces.md#new-and-classic-workspace-differences)

เมื่อสร้างโทเค็นแบบฝังพื้นที่ทำงานที่แตกต่างกันจะมีข้อควรพิจารณาที่แตกต่างกันและต้องการข้อควรพิจารณาที่แตกต่างกัน

|                  |พื้นที่ทำงาน *คลาสสิก* |พื้นที่ทำงาน *ใหม่*|
|------------------|---------|--------|
|**ข้อควรพิจารณา**|<li>ชุดข้อมูลและรายการต้องอยู่ในพื้นที่ทำงานเดียวกัน</li><li>ไม่สามารถใช้บริการหลักได้</li>  |ชุดข้อมูลและรายการอาจอยู่ในพื้นที่ทำงาน *ใหม่* สองแห่งที่แตกต่างกัน |
|**การอนุญาตของพื้นที่ทำงาน**|ผู้ใช้หลักต้องเป็นผู้ดูแลระบบของพื้นที่ทำงาน  |บริการหลักหรือผู้ใช้หลักต้องเป็นสมาชิกของพื้นที่ทำงานทั้งสองเป็นอย่างน้อย |

>[!NOTE]
>* คุณไม่สามารถสร้างโทเค็นฝังตัวสำหรับ [พื้นที่ทำงานของฉัน](../../consumer/end-user-workspaces.md#types-of-workspaces)
>* คำว่า *รายการ* หมายถึงรายการ Power BI เช่น แดชบอร์ด ไทล์ ถามตอบหรือรายงาน

## <a name="securing-your-data"></a>การรักษาความปลอดภัยข้อมูลของคุณ

เมื่อสร้างโซลูชันของคุณให้พิจารณาสองแนวทางนี้ในการรักษาความปลอดภัยข้อมูลของคุณ:

* [การแยกตามพื้นที่ทำงาน](embed-multi-tenancy.md#power-bi-workspace-based-isolation)

* [การแยกตามการรักษาความปลอดภัยระดับแถว](embed-multi-tenancy.md#row-level-security-based-isolation)

หากคุณจะใช้วิธีการ RLS โปรดอ่าน [ข้อควรพิจารณาและข้อ จำกัด ของ RLS](generate-embed-token.md#row-level-security) ที่ส่วนท้ายของบทความนี้

## <a name="token-permissions"></a>การอนุญาตของโทเค็น

ใน API สร้างโทเค็นส่วน *GenerateTokenRequest* จะอธิบายถึงการอนุญาตของโทเค็น

>[!NOTE]
>การอนุญาตของโทเค็นที่แสดงในส่วนนี้ไม่สามารถใช้ได้กับ API [สร้างโทเค็นสำหรับรายงานหลายรายงาน](/rest/api/power-bi/embedtoken/generatetoken)

### <a name="access-level"></a>ระดับการเข้าถึง

ใช้พารามิเตอร์ *accessLevel* เพื่อกำหนดระดับการเข้าถึงของผู้ใช้

* **มุมมอง** - มอบการอนุญาตของมุมมองผู้ใช้

* **แก้ไข** - ให้การอนุญาตแก่ผู้ใช้ในการดูและแก้ไข (ใช้ได้เฉพาะเมื่อสร้างโทเค็นแบบฝังสำหรับรายงาน)

    หากคุณกำลังใช้ API [สร้างโทเค็นสำหรับรายงานหลายรายการ](/rest/api/power-bi/embedtoken/generatetoken) ให้ใช้พารามิเตอร์ *allowEdit* เพื่อให้การอนุญาตแก่ผู้ใช้ในการดูและแก้ไข

* **สร้าง** - ให้การอนุญาตผู้ใช้ในการสร้างรายงาน (ใช้เฉพาะเมื่อสร้างโทเค็นแบบฝังสำหรับการสร้างรายงาน)

    สำหรับการสร้างรายงานคุณต้องระบุพารามิเตอร์ *datasetId* ด้วย

### <a name="saving-a-copy-of-the-report"></a>บันทึกสำเนาของรายงาน

ใช้บูลีน *allowSaveAs* เพื่อให้ผู้ใช้บันทึกรายงานเป็นรายงานใหม่ การตั้งค่านี้ถูกตั้งค่าเป็น *เท็จ* โดยค่าเริ่มต้น

พารามิเตอร์นี้ใช้ได้เฉพาะเมื่อสร้างโทเค็นแบบฝังสำหรับรายงาน

### <a name="row-level-security"></a>การรักษาความปลอดภัยระดับแถว

ด้วย [การรักษาความปลอดภัยระดับแถว (RLS)](embedded-row-level-security.md) คุณสามารถเลือกใช้ข้อมูลประจำตัวที่แตกต่างจากข้อมูลประจำตัวของบริการหลักหรือผู้ใช้หลักที่คุณสร้างโทเค็นด้วย เมื่อใช้ตัวเลือกนี้คุณสามารถแสดงข้อมูลที่ฝังไว้ตามผู้ใช้ที่คุณกำหนดเป้าหมาย ตัวอย่างเช่น ในแอปพลิเคชันของคุณ คุณสามารถขอให้ผู้ใช้ลงชื่อเข้าใช้จากนั้นแสดงรายงานที่มีเฉพาะข้อมูลการขายหากผู้ใช้ที่ลงชื่อเข้าใช้เป็นพนักงานขาย

หากคุณกำลังใช้ RLS ในบางกรณีคุณสามารถละเว้นข้อมูลประจำตัวของผู้ใช้ได้ (พารามิเตอร์ *EffectiveIdentity*) สิ่งนี้ช่วยให้โทเค็นสามารถเข้าถึงฐานข้อมูลทั้งหมดได้ วิธีนี้สามารถใช้เพื่อให้สิทธิ์อนุญาตให้เข้าถึงแก่ผู้ใช้เช่นผู้ดูแลระบบและผู้จัดการซึ่งมีการอนุญาตดูชุดข้อมูลทั้งหมด อย่างไรก็ตามคุณไม่สามารถใช้วิธีนี้ได้ในทุกสถานการณ์ ตารางด้านล่างแสดงรายการประเภท RLS ต่าง ๆ และแสดงวิธีการตรวจสอบสิทธิ์ที่สามารถใช้ได้โดยไม่ต้องระบุตัวตนของผู้ใช้

ตารางยังแสดงข้อควรพิจารณาและข้อจำกัดที่เกี่ยวข้องกับ RLS แต่ละประเภท

|ประเภท RLS  |ฉันสามารถสร้างโทเค็นแบบฝังโดยไม่ระบุ ID ผู้ใช้ที่ใช้ได้หรือไม่  |ข้อควรพิจารณาและข้อจำกัด  |
|---------|---------|---------|
|การรักษาความปลอดภัยระดับแถวของระบบคลาวด์ (Cloud RLS)      |✔ ผู้ใช้หลัก<br/>✖ บริการหลัก          |         |
|RDL (รายงานแบบแบ่งหน้า)     |✖ ผู้ใช้หลัก<br/>✔ บริการหลัก        |คุณไม่สามารถใช้ผู้ใช้หลักเพื่อสร้างโทเค็นฝังสำหรับ RDL ได้         |
|Analysis Services (AS) การเชื่อมต่อแบบสดในสถานที่    |✔ ผู้ใช้หลัก<br/>✖ บริการหลัก         |ผู้ใช้ที่สร้างโทเค็นแบบฝังยังต้องการการอนุญาตอย่างใดอย่างหนึ่งต่อไปนี้:<li>การอนุญาตผู้ดูแลระบบเกตเวย์</li><li>แหล่งข้อมูลเลียนแบบการอนุญาต (*ReadOverrideEffectiveIdentity*)</li>         |
|Analysis Services (AS) การเชื่อมต่อ Azure live    |✔ ผู้ใช้หลัก<br/>✖ บริการหลัก         |ไม่สามารถแทนที่ข้อมูลประจำตัวของผู้ใช้ที่สร้างโทเค็นสำหรับฝังได้ ข้อมูลที่กำหนดเองสามารถใช้เพื่อใช้ RLS แบบไดนามิกหรือการกรองที่ปลอดภัย<br/><br/>**หมายเหตุ:** หลักบริการต้องระบุ ID อ็อบเจ็กต์เป็นข้อมูลประจำตัวที่มีประสิทธิภาพ (ชื่อผู้ใช้ RLS)         |
|การลงชื่อเข้าระบบครั้งเดียว (SSO)     |✔ ผู้ใช้หลัก<br/>✖ บริการหลัก         |ข้อมูลประจำตัวที่ชัดเจน (SSO) สามารถระบุได้โดยใช้คุณสมบัติ blob ของข้อมูลประจำตัวในอ็อบเจ็กต์เอกลักษณ์ที่มีประสิทธิภาพ         |
|SSO และ cloud RLS     |✔ ผู้ใช้หลัก<br/>✖ บริการหลัก         |คุณต้องระบุดังต่อไปนี้:<li>ข้อมูลประจำตัวที่ชัดเจน (SSO) สามารถระบุได้โดยใช้คุณสมบัติ blob ของข้อมูลประจำตัวในใอ็อบเจ็กต์เอกลักษณ์ที่มีประสิทธิภาพ</li><li>ข้อมูลประจำตัว (RLS) ที่มีประสิทธิภาพ (ชื่อผู้ใช้)</li>         |

>[!NOTE]
>บริการหลักต้องให้ข้อมูลต่อไปนี้เสมอ:
>* ข้อมูลประจำตัวสำหรับรายการใด ๆ ที่มีชุดข้อมูล RLS
>* สำหรับชุดข้อมูล SSO ข้อมูลประจำตัว RLS ที่มีประสิทธิภาพพร้อมคุณสมบัติชื่อผู้ใช้ที่กำหนดไว้

## <a name="next-steps"></a>ขั้นตอนถัดไป

>[!div class="nextstepaction"]
>[ลงทะเบียนแอป](register-app.md)

> [!div class="nextstepaction"]
>[Power BI Embedded สำหรับลูกค้าของคุณ](embed-sample-for-customers.md)

>[!div class="nextstepaction"]
>[แอปพลิเคชันและออบเจ็กต์บริการหลักใน Azure Active Directory](/azure/active-directory/develop/app-objects-and-service-principals)

>[!div class="nextstepaction"]
>[ความปลอดภัยระดับแถวโดยใช้เกตเวย์ข้อมูลภายในองค์กรที่มีโครงร่างสำคัญของบริการ](embedded-row-level-security.md#on-premises-data-gateway-with-service-principal)

>[!div class="nextstepaction"]
>[ฝังเนื้อหา Power BI ด้วยองค์ประกอบหลักของบริการ](embed-service-principal.md)