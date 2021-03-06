---
title: การรวมแอปสำหรับอุปกรณ์เคลื่อนที่ของ Power BI ด้วยปุ่มลัด Siri
description: วิธีใช้ปุ่มลัด Siri เพื่อเข้าถึงเนื้อหา Power BI ที่คุณต้องการโดยตรง
author: paulinbar
ms.author: painbar
manager: rkarlin
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 12/01/2020
ms.openlocfilehash: 0bf1fb3f921b195be430e21f6f0b0bf2b0eeb473
ms.sourcegitcommit: 2fd64f96b5bfbc14ff47e5c892171e5c921fb525
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/02/2020
ms.locfileid: "96501983"
---
# <a name="using-siri-shortcuts-in-power-bi-mobile-ios-app"></a>การใช้ปุ่มลัด Siri ในแอป Power BI บนมือถือสำหรับ iOS

ใช้ปุ่มลัด Siri เพื่อเข้าถึงเนื้อหา Power BI ที่คุณต้องการโดยตรง

เพื่อให้สามารถเข้าถึงรายงานหรือแดชบอร์ดที่ใช้บ่อยๆ ได้อย่างง่ายดายและรวดเร็ว คุณสามารถสร้างทางลัด Siri สำหรับการเข้าถึงเนื้อหา Power BI โดยตรงที่คุณต้องการได้ ด้วยทางลัด Siri คุณเพียงแค่จำเป็นต้องขอให้ Siri เปิดเมื่อใดก็ตามที่คุณต้องการดูข้อมูล

> [!NOTE]
> การรวมทางลัด Siri กับแอป Power BI จะพร้อมใช้งานสำหรับ iPhone และ iPad ที่ทำงานบน iOS12 ขึ้นไป

## <a name="create-siri-shortcut-for-a-report-or-dashboard"></a>สร้างปุ่มลัด Siri สำหรับรายงานหรือแดชบอร์ด

มีสามวิธีในการสร้างปุ่มลัด Siri ไปยังรายงานและแดชบอร์ดของคุณ:

- จะมีการเพิ่มแบนเนอร์พร้อมตัวเลือก **เพิ่มไปยัง Siri** ไปยังรายงานและแดชบอร์ดที่ใช้งานบ่อยของคุณ แตะที่แอคชันเพื่อเปิดหน้า **เพิ่มไปยัง Siri**
    
- ใช้แอคชัน **ปุ่มลัด Siri** บน **รายงาน** หรือเมนูแอคชัน **แดชบอร์ด**(...)
    
- ใช้ **ปุ่มลัดที่แนะนำ** ในการตั้งค่าอุปกรณ์ (**การตั้งค่าอุปกรณ์** > **Siri และค้นหา**) คุณสามารถเพิ่มปุ่มลัดไปยังรายการในคำแนะนำ โดยใช้ปุ่มเครื่องหมายบวก (+) ได้
     
     ![สร้างปุ่มลัด](./media/mobile-apps-ios-siri-search/power-bi-siri-create-shortcut.png)

สำหรับรายงาน Power BI ปุ่มลัดจะจับภาพหน้าปัจจุบันที่คุณกำลังดูเมื่อสร้างปุ่มลัด 

ตัวเลือกทั้งหมดจะเปิดหน้า **เพิ่มไปยัง Siri** ในหน้านี้ คุณจำเป็นต้องบันทึกวลีที่คุณจะใช้ในภายหลังด้วย Siri เพื่อเปิดรายงานหรือแดชบอร์ด 
   
![เพิ่มไปยังหน้า Siri](./media/mobile-apps-ios-siri-search/power-bi-siri-add-page.png)
    

## <a name="use-siri-shortcuts-to-view-report-or-dashboard"></a>ใช้ปุ่มลัด Siri เพื่อดูรายงานหรือแดชบอร์ด

ทันทีที่คุณสร้างปุ่มลัด ทุกครั้งที่คุณต้องการเข้าถึงแดชบอร์ดหรือรายงานที่คุณสร้างปุ่มลัดให้ แค่ถาม Siri
เปิดใช้งาน Siri และระบุวลีที่คุณบันทึกไว้สำหรับปุ่มลัด Siri จะเปิดใช้ Power BI และจะไปลงบนรายงานที่ร้องขอหรือแดชบอร์ด 

สำหรับรายงาน Power BI คุณจะไปลงยังหน้าที่จับภาพไว้เมื่อคุณสร้างปุ่มลัด


  ![Siri เปิดใช้ Power BI เพื่อเปิดปุ่มลัด](./media/mobile-apps-ios-siri-search/power-bi-siri-open.png)
  

## <a name="edit-siri-shortcut-phrase"></a>แก้ไขวลีปุ่มลัด Siri 
คุณสามารถแก้ไขวลีปุ่มลัดของคุณได้โดยใช้ปุ่ม **ปุ่มลัด Siri** บน **รายงาน** หรือเมนูแอคชัน **แดชบอร์ด**(...) ได้ จะเปิดหน้าปุ่มลัด Siri พร้อมตัวเลือกเพื่อ **บันทึกวลีใหม่** 

## <a name="create-a-home-screen-shortcut-from-your-siri-shortcut"></a>สร้างทางลัดหน้าจอหลักจากทางลัด Siri ของคุณ 
หลังจากที่คุณได้สร้างทางลัด Siri ไปยังเนื้อหา Power BI แล้ว คุณสามารถเพิ่มลงในหน้าจอหลักของอุปกรณ์ของคุณได้ ดังนั้นคุณสามารถเปิดเนื้อหานั้นได้โดยตรงจากหน้าจอหลักของด้วยการแตะเพียงครั้งเดียว ทำตามคำแนะนำเหล่านี้ที่ https://support.apple.com/guide/shortcuts/apd735880972/ios

## <a name="delete-siri-shortcut"></a>ลบปุ่มลัด Siri 
ในการลบปุ่มลัด ไปที่รายการ และออกจากเมนูแอคชัน (...) แตะที่แอคชัน **ปุ่มลัด Siri** หน้า **ปุ่มลัด Siri** จะเปิดขึ้น เลือก **ลบปุ่มลัด**

## <a name="next-steps"></a>ขั้นตอนถัดไป
เรียนรู้เพิ่มเติมเกี่ยวกับแอป Power BI สำหรับอุปกรณ์เคลื่อนที่โดยดำเนินการดังนี้: 

* การดาวน์โหลด [แอป Power BI สำหรับ iPhone](https://go.microsoft.com/fwlink/?LinkId=522062)
* ติดตาม[@MSPowerBIบน Twitter](https://twitter.com/MSPowerBI)
* การเข้าร่วมการสนทนาที่[ชุมชน Power BI](https://community.powerbi.com/)