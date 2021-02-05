---
title: เชื่อมต่อกับ Snowflake Computing Warehouse ใน Power BI Desktop
description: เชื่อมต่อและใช้งาน Snowflake Computing Warehouse ใน Power BI Desktop ได้อย่างง่ายดาย
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 01/04/2021
LocalizationGroup: Connect to data
ms.openlocfilehash: 377ede2171a721a33aa0b70819ef511d721f2590
ms.sourcegitcommit: f7330dabb9cd8bce90bb2efec3e3273a11578f10
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2021
ms.locfileid: "99494455"
---
# <a name="connect-to-snowflake-in-power-bi-desktop"></a>เชื่อมต่อกับ Snowflake ใน Power BI Desktop
ใน Power BI Desktop คุณสามารถเชื่อมต่อไปยัง **Snowflake** Computing Warehouse และใช้ข้อมูลพื้นฐานได้เช่นเดียวกับแหล่งข้อมูลอื่นๆ ใน Power BI Desktop 

## <a name="connect-to-a-snowflake-computing-warehouse"></a>เชื่อมต่อกับ Snowflake Computing Warehouse
เมื่อต้องการเชื่อมต่อกับ **Snowflake** Computing Warehouse ให้เลือก **เรียกใช้ข้อมูล** จากแถบ **หน้าหลัก** ใน Power BI Desktop เลือก **ฐานข้อมูล** จากประเภททางด้านซ้าย จากนั้นคุณจะเห็น **Snowflake**

![ภาพหน้าจอของกล่องโต้ตอบรับข้อมูล ที่แสดงการเลือกฐานข้อมูล Snowflake](media/desktop-connect-snowflake/connect-snowflake-2b.png)

ในหน้าต่าง **Snowflake** ที่ปรากฏขึ้น ให้พิมพ์หรือวางชื่อ Snowflake Computing Warehouse ลงในกล่อง แล้วเลือก **ตกลง** โปรดทราบว่าคุณสามารถเลือก **นำเข้า** ข้อมูลได้โดยตรงใน Power BI หรือจะใช้ **DirectQuery** ก็ได้ เรียนรู้เพิ่มเติมเกี่ยวกับ[การใช้ DirectQuery](desktop-use-directquery.md) โปรดทราบว่า AAD SSO สนับสนุนเฉพาะ DirectQuery เท่านั้น

![ภาพหน้าจอของกล่องโต้ตอบ Snowflake ที่แสดงปุ่มนำเข้าวิทยุที่เลือกไว้](media/desktop-connect-snowflake/connect-snowflake-3.png)

เมื่อได้รับการถาม ให้ใส่ชื่อผู้ใช้และรหัสผ่านของคุณ

![ภาพหน้าจอของข้อความแจ้งเตือนข้อมูลประจำตัว Snowflake ที่แสดงเขตข้อมูลชื่อผู้ใช้และรหัสผ่าน](media/desktop-connect-snowflake/connect-snowflake-4.png)

> [!NOTE]
> เมื่อคุณป้อนชื่อผู้ใช้และรหัสผ่านสำหรับเซิร์ฟเวอร์ **Snowflake** ที่เฉพาะเจาะจงแล้ว Power BI Desktop จะใช้ข้อมูลประจำตัวเดียวกันนั้นเพื่อพยายามเชื่อมต่ออีกครั้ง คุณสามารถปรับเปลี่ยนข้อมูลประจำตัวเหล่านั้นได้โดยไปที่ **ไฟล์ > ตัวเลือกและการตั้งค่า > การตั้งค่าแหล่งข้อมูล**
> 
> 

ถ้าคุณต้องการใช้ตัวเลือกบัญชี Microsoft จะต้องมีการกำหนดค่าการรวม Snowflake AAD ในฝั่ง Snowflake เมื่อต้องการทำเช่นนี้ ให้อ่านส่วนเริ่มต้นใช้งานของ [เอกสารประกอบ Snowflake บนหัวข้อนั้น](https://docs.snowflake.net/manuals/user-guide/oauth-powerbi.html#power-bi-sso-to-snowflake)

![ชนิดการรับรองความถูกต้องของบัญชี Microsoft ในตัวเชื่อมต่อ Snowflake](media/desktop-connect-snowflake/connect-snowflake-6.png)


เมื่อเชื่อมต่อเสร็จเรียบร้อยแล้ว หน้าต่าง **ตัวนำทาง** จะปรากฏขึ้น และแสดงข้อมูลที่พร้อมใช้งานบนเซิร์ฟเวอร์ ซึ่งคุณสามารถเลือกองค์ประกอบหนึ่งรายการหรือหลายรายการเพื่อนำเข้าและใช้ใน **Power BI Desktop** ได้

![ODBC Error 28000 ทำให้เกิดความผิดพลาดในการเชื่อมต่อ](media/desktop-connect-snowflake/connect-snowflake-5.png)

คุณสามารถ **โหลด** ตารางที่เลือก ซึ่งจะนำทั้งตารางลงใน **Power BI Desktop** หรือคุณสามารถ **แก้ไข** คิวรี ซึ่งจะเปิด **ตัวแก้ไขคิวรี** เพื่อให้คุณสามารถกรองและปรับปรุงชุดข้อมูลที่ต้องการใช้ จากนั้นจึงโหลดชุดข้อมูลที่ปรับปรุงแล้วลงใน **Power BI Desktop**

## <a name="custom-roles"></a>บทบาทแบบกำหนดเอง

ในขณะนี้การสนับสนุนสำหรับ ' บทบาทแบบกำหนดเอง ' ในตัวเชื่อมต่อเกล็ดหิมะจะทำงานกับการรับรองความถูกต้องพื้นฐานเท่านั้น การดำเนินการนี้จะได้รับการแก้ไขในอนาคตอันใกล้

## <a name="next-steps"></a>ขั้นตอนถัดไป
มีข้อมูลหลากหลายประเภทที่คุณสามารถเชื่อมต่อโดยใช้ Power BI Desktop สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแหล่งข้อมูล โปรดดูทรัพยากรต่อไปนี้:

* [Power BI Desktop คืออะไร](../fundamentals/desktop-what-is-desktop.md)
* [แหล่งข้อมูลใน Power BI Desktop](desktop-data-sources.md)
* [จัดรูปทรงและรวมข้อมูลด้วย Power BI Desktop](desktop-shape-and-combine-data.md)
* [เชื่อมต่อกับเวิร์กบุ๊ก Excel ใน Power BI Desktop](desktop-connect-excel.md)   
* [ป้อนข้อมูลลงใน Power BI Desktop โดยตรง](desktop-enter-data-directly-into-desktop.md)   
