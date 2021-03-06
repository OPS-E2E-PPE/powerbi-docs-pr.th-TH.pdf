---
title: การพัฒนาบนอุปกรณ์เคลื่อนที่ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: วิธีการสร้างวิชวล Power BI ที่เหมาะกับอุปกรณ์เคลื่อนที่ เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: how-to
ms.date: 03/12/2019
ms.openlocfilehash: 63d2366f91398878af231c8dbb6ed07e8e623a03
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97885556"
---
# <a name="how-to-create-mobile-friendly-power-bi-visuals"></a>วิธีการสร้างวิชวล Power BI ที่ใช้งานง่ายบนอุปกรณ์เคลื่อนที่
การใช้อุปกรณ์เคลื่อนมีบทบาทสำคัญใน Power BI หนึ่งในจุดแข็งคือการที่สามารถเชื่อมต่อกับข้อมูลของคุณได้ทุกที่ทุกเวลา

ในฐานะนักพัฒนาที่สร้างวิชวล Power BI ข้อจำกัดที่ไม่ซ้ำกันของอุปกรณ์เคลื่อนที่แต่ละรายการจะต้องได้รับการแก้ไขเพื่อให้เข้าถึงผู้ใช้มากที่สุดเท่าที่เป็นไปได้ และมอบประสบการณ์การใช้งานบนอุปกรณ์เคลื่อนที่ที่ยอดเยี่ยม

ใช้ [แอป Power BI สำหรับ Windows, iOS และ Android](../../consumer/mobile/mobile-apps-for-mobile-devices.md) เพื่อให้ผู้ใช้ทางธุรกิจของคุณสามารถดูข้อมูลที่ครอบคลุมของพวกเขาได้ในขณะเดินทางเพียงปลายนิ้วสัมผัส

## <a name="requirements"></a>ข้อกำหนด

ข้อกำหนดต่อไปนี้เป็นสิ่งจำเป็นสำหรับการพัฒนาวิชวลที่ใช้งานง่ายบนอุปกรณ์เคลื่อนที่:

- แสดง

  วิชวล Power BI ของคุณต้องแสดงบนอุปกรณ์เคลื่อนที่ที่รองรับทั้งหมด รวมถึงเบราว์เซอร์และแอปพลิเคชันที่รองรับโดยไม่มีข้อผิดพลาดในรายงาน แดชบอร์ด หรือเมื่อทำงานในโหมด **โฟกัส** 

- แบบโต้ตอบ

  ฟังก์ชันการทำงานแบบโต้ตอบจะต้องได้รับการระบุไว้ในลักษณะเดียวกับที่ระบุไว้้สำหรับอุปกรณ์เดสก์ท็อป เหตุการณ์ทั้งหมดที่จัดการบนเบราว์เซอร์บนเดสก์ท็อปต้องได้รับการสนับสนุน หรือมีตัวจัดการเหตุการณ์ที่เปรียบเทียบได้สำหรับอุปกรณ์เคลื่อนที่
  
  ตัวอย่างเช่น การนำทางพื้นฐานและการเลือกจุดข้อมูลควรมีฟังก์ชันการทำงานเหมือนกับในเบราว์เซอร์เดสก์ท็อป ถ้าวิชวลรองรับการเลือกหลายรายการโดยใช้ **Ctrl** นักพัฒนาจำเป็นต้องพิจารณาเพิ่มตัวจัดการเหตุการณ์ที่คล้ายกันสำหรับอุปกรณ์เคลื่อนที่

  ตารางต่อไปนี้แสดงรายการเหตุการณ์ที่สอดคล้องกันบนอุปกรณ์เคลื่อนที่

  | ชื่อเหตุการณ์ของเมาส์ | ชื่อเหตุการณ์ของการสัมผัส |
  |:----------------:|:----------------:|
  | `click` | `click` |
  | `mousemove` | `touchmove` |
  | `mousedown` | `touchstart` |
  | `mouseup` | `touchend` |
  | `dblclick` | ใช้ไลบรารีภายนอก |
  | `contextmenu` | ใช้ไลบรารีภายนอก |
  | `mouseover` | `touchmove` |
  | `mouseout` | `touchmove` (หรือไลบรารีภายนอก) |
  | `wheel` | `NaN` |

  > [!NOTE]
  > ไม่ใช่ว่าอุปกรณ์เคลื่อนที่หรือหน้าจอสัมผัสทั้งหมดจะรองรับเหตุการณ์ของเมาส์ (หรือ *เมาส์* ที่นำหน้า) ในกรณีดังกล่าว ให้จัดการทั้งเหตุการณ์ของ *เมาส์* และ *การสัมผัส* ในเวลาเดียวกัน

## <a name="optional"></a>เลือกหรือไม่เลือกก็ได้
ต่อไปนี้จะถือว่าเป็นทางเลือกและใช้เพื่อสร้างประสบการณ์ผู้ใช้ปลายทางที่ดีขึ้น

- แสดง

  หากต้องการรองรับขนาดวิชวลที่เล็กลง ให้ลองเพิ่มตัวเลือกรูปแบบที่ผู้ใช้สามารถเปลี่ยนแปลงเพื่อปรับขนาดของแต่ละองค์ประกอบได้ ตัวอย่างเช่น เพิ่มตัวเลือกรูปแบบไปยังป้ายชื่อสำหรับใช้ในรายงานและแดชบอร์ด ซึ่งช่วยให้ผู้ใช้สามารถปรับแต่งวิชวลสำหรับอุปกรณ์เคลื่อนที่ของตนโดยเฉพาะ
  
  นอกจากนี้ยังสามารถใช้การตั้งค่าเดียวกันกับวิชวลในเบราว์เซอร์บนเดสก์ท็อป และถ้าจำเป็น จะถูกแทนที่เพื่อปรับวิชวลให้เป็นหน้าจอขนาดเล็กลง

  > [!NOTE]
  > หากต้องการปรับวิชวลให้เหมาะสมที่สุดในโหมด **โฟกัส** จะต้องพิจารณาทั้งการวางแนวขนาดหน้าจอในแนวตั้งและแนวนอน โปรดดู [เนื้อหาการแสดงผลในโหมดโฟกัส](../../consumer/end-user-focus.md)

- แบบโต้ตอบ

  พิจารณาการเพิ่มตัวจัดการเหตุการณ์เฉพาะสำหรับอุปกรณ์เคลื่อนที่เช่น การลาก และการเลื่อน

- การย้ายโหนดเมื่อเกิดข้อผิดพลาด

  วิชวลควรแสดงข้อผิดพลาดที่เป็นคำอธิบายถ้าไม่สามารถแสดงบนอุปกรณ์เคลื่อนที่ได้

## <a name="supported-browsers-and-devices"></a>เบราว์เซอร์และอุปกรณ์ที่รองรับ
วิชวล Power BI ต้องแสดงบนอุปกรณ์ทั้งหมดที่รองรับแอป Power BI สำหรับข้อมูลเพิ่มเติม โปรดดู [เบราว์เซอร์ที่รองรับสำหรับ Power BI](../../fundamentals/power-bi-browsers.md) และ [Power BI แอปสำหรับอุปกรณ์เคลื่อนที่ ](../../consumer/mobile/mobile-apps-for-mobile-devices.md)

เมื่อทดสอบกับอุปกรณ์ Windows, iOS และ Android รุ่นล่าสุด นักพัฒนาจำเป็นต้องพิจารณาด้านคุณภาพเหล่านี้มากที่สุด

## <a name="next-steps"></a>ขั้นตอนถัดไป
หากต้องการเริ่มต้น โปรดดู [การพัฒนาวิชวลการ์ดวงกลมใน Power BI](./develop-circle-card.md)