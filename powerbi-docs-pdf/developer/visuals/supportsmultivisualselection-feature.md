---
title: คุณลักษณะ supportsMultiVisualSelection ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการใช้ฟีเจอร์ supportsMultiVisualSelection ในวิชวล Power BI และข้อกำหนดของคุณลักษณะ เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.date: 04/30/2020
ms.openlocfilehash: 9e6b17a4576f2354a5cbecc0c3a965a5611784ee
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887948"
---
# <a name="use-the-supportsmultivisualselection-feature"></a>ใช้ฟีเจอร์ supportsMultiVisualSelection

ฟีเจอร์ `supportsMultiVisualSelection`ช่วยให้คุณสามารถใช้การเลือกในวิชวลหลายรายการในรายงานได้

## <a name="example"></a>ตัวอย่าง:

ในรายงานที่มีวิชวลมากกว่าหนึ่งรายการ ให้เลือกสองค่าเพื่อให้ค่าเหล่านั้นนำไปใช้กับอื่นๆ ตัวอย่างเช่น ใน [ตัวอย่างการวิเคราะห์การค้าปลีก](../../create-reports/sample-retail-analysis.md) เลือก **Fashions Direct** ในหนึ่งวิชวล เลือก ctrl และเลือก **ม.ค.** ในอีกวิชวลหนึ่ง ในรายงานนั้น การเลือกของคุณจะนำไปใช้กับวิชวลอื่นๆ ที่สนับสนุนการใช้ฟีเจอร์นี้ วิชวลอื่นๆ จะได้รับการกำหนดขอบเขตเป็น **Fashions Direct** และ **ม.ค.**

## <a name="requirements"></a>ข้อกำหนด

ฟีเจอร์นี้ต้องการ API v3.2.0 หรือสูงกว่า

คุณไม่สามารถนำฟีเจอร์นี้ไปใช้กับวิชวลภาพได้ คุณไม่สามารถนำฟีเจอร์นี้ไปใช้กับวิชวลขั้นสูงบางรายการได้ เช่น Key Driver Decomposition Tree วิชวลแบบถามตอบ กล่องข้อความ และแผนภูมิหน้าปัด

## <a name="usage"></a>การใช้งาน

หากต้องการใช้ฟีเจอร์ `supportsMultiVisualSelection` ให้กรอกรหัสต่อไปนี้ลงในไฟล์ `capabilities.json` ของวิชวลของคุณ

```json
    {   
            ...
        "supportsMultiVisualSelection": true
            ...
    }
```

## <a name="next-steps"></a>ขั้นตอนถัดไป

หากต้องการเรียนรู้เกี่ยวกับแนวคิด Power BI ดู [วิชวลใน Power BI](power-bi-visuals-concept.md)

หากต้องการทดลองใช้การพัฒนา Power BI โปรดดูที่ [การพัฒนาการ์ดวงกลม Power BI](develop-circle-card.md)
