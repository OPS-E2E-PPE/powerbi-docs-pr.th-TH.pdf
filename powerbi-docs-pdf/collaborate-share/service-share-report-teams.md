---
title: แชทใน Microsoft Teams โดยตรงจากบริการ Power BI
description: คุณสามารถแชร์แดชบอร์ดและรายงาน Power BI จากบริการของ Power BI ไปยัง Microsoft Teams ได้โดยตรง
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
LocalizationGroup: Share your work
ms.date: 01/04/2020
ms.openlocfilehash: 63ea4772610bd7112823f38c66abced1f0654b77
ms.sourcegitcommit: 932f6856849c39e34229dc9a49fb9379c56a888a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/06/2021
ms.locfileid: "97926966"
---
# <a name="chat-in-microsoft-teams-directly-from-the-power-bi-service"></a>แชทใน Microsoft Teams โดยตรงจากบริการ Power BI

คุณสามารถพูดคุยเกี่ยวกับแดชบอร์ด รายงาน และภาพของ Power BI ใน Microsoft Teams ได้โดยตรงจากบริการ Power BI ใช้คุณลักษณะ **แชทใน Teams** เพื่อเริ่มการสนทนาอย่างรวดเร็วเมื่อคุณดูรายงานและแดชบอร์ดในบริการ Power BI

## <a name="requirements"></a>ข้อกำหนด

เมื่อต้องการใช้ฟังก์ชัน **แชทใน Teams** ใน Power BI ตรวจสอบให้แน่ใจว่าผู้ดูแลระบบ Power BI ของคุณไม่ได้ปิดใช้งานการตั้งค่าผู้เช่าสำหรับ **แชร์ไปยัง Teams** ในพอร์ทัลผู้ดูแลระบบ Power BI การตั้งค่านี้ช่วยให้องค์กรสามารถซ่อนปุ่ม **แชทใน Teams** ได้ ดูรายละเอียดที่บทความ[พอร์ทัลผู้ดูแลระบบ Power BI](../admin/service-admin-portal.md#share-to-teams)

ดู [การทำงานร่วมกันใน Microsoft Teams ด้วย Power BI](service-collaborate-microsoft-teams.md) สำหรับเบื้องหลังเกี่ยวกับวิธีที่ระบบ Power Bi และ Microsoft Teams ทำงานร่วมกัน รวมถึงข้อกำหนดต่าง ๆ

## <a name="chat-about-power-bi-content-in-microsoft-teams"></a>พูดคุยเกี่ยวกับเนื้อหา Power BI ใน Microsoft Teams

ทําตามขั้นตอนเหล่านี้เพื่อแชร์ลิงก์ไปยังรายงาน แดชบอร์ด และภาพในบริการ Power BI และพูดคุยเกี่ยวกับช่องและแชทของ Microsoft Teams

1. เลือกหนึ่งในตัวเลือกเหล่านี้:

   * **แชทใน Teams** ในแถบการดำเนินการของแดชบอร์ดหรือรายงาน:

       ![สกรีนช็อตของปุ่มสนทนาในทีมในแถบการดำเนินการ](media/service-share-report-teams/service-teams-share-to-teams-action-bar-button.png)
    
   * **แชทใน Teams** ในเมนูบริบทสําหรับวิชวลเดียว:
    
      ![สกรีนช็อตของปุ่มสนทนาในทีมในเมนูบริบทการแสดงผลด้วยภาพ](media/service-share-report-teams/service-teams-share-to-teams-visual-context-menu.png)

1. ในกล่องโต้ตอบ **แชร์กับ Microsoft Teams** ให้เลือกทีมหรือช่องที่คุณต้องการส่งลิงก์ไปให้ เพิ่มข้อความถ้าคุณต้องการ คุณอาจถูกขอให้ลงชื่อเข้าใช้ Microsoft Teams ก่อน

    ![ภาพหน้าจอของแชร์ไปยังกล่องโต้ตอบ Microsoft Teams ด้วยข้อมูลและข้อความ](media/service-share-report-teams/service-teams-share-to-teams-dialog.png)

1. เลือก **แชร์** เพื่อส่งลิงก์
    
1. ลิงก์จะถูกเพิ่มไปยังการสนทนาที่มีอยู่หรือเริ่มการสนทนาใหม่

    ![ภาพหน้าจอของการสนทนาของ Microsoft Teams ที่มีลิงก์ไปยังรายการ Power BI](media/service-share-report-teams/service-teams-share-to-teams-deep-link.png)

1. เลือกลิงก์เพื่อเปิดรายการในบริการ Power BI

1. ถ้าคุณใช้เมนูบริบทสำหรับภาพที่ระบุ ภาพจะถูกไฮไลท์เมื่อรายงานเปิดขึ้น

    ![ภาพหน้าจอของรายงาน Power BI ที่เปิดด้วยวิชวลเฉพาะที่มีการไฮไลต์ไว้](media/service-share-report-teams/service-teams-share-to-teams-spotlight-visual.png)


## <a name="known-issues-and-limitations"></a>ปัญหาและขีดจำกัดที่ทราบแล้ว

- ผู้ใช้ที่ไม่มีสิทธิ์การใช้งาน Power BI หรือสิทธิ์ในการเข้าถึงรายงานจะเห็นข้อความ "เนื้อหาไม่พร้อมใช้งาน"
- ปุ่ม **แชทใน Teams** อาจไม่ทำงาน หากเบราว์เซอร์ของคุณใช้การตั้งค่าความเป็นส่วนตัวที่เข้มงวด ใช้ **ยังพบปัญหาอยู่ใช่หรือไม่? ลองเปิดในตัวเลือกหน้าต่างใหม่** ถ้ากล่องโต้ตอบไม่เปิดอย่างถูกต้อง
- **แชทใน Teams** ไม่รวมการแสดงตัวอย่างลิงก์
- การแสดงตัวอย่างลิงก์และ **แชทใน Teams** ไม่อนุญาตให้ผู้ใช้ดูรายการ สิทธิ์ต้องได้รับการจัดการแยกต่างหาก
- ปุ่ม **แชทใน Teams** ไม่พร้อมใช้งานในเมนูบริบทวิชวล เมื่อผู้สร้างรายงานตั้งค่า **ตัวเลือกเพิ่มเติม** เป็น **ปิด** สำหรับวิชวล
- ดูปัญหาอื่น ๆ ที่หัวข้อ[ปัญหาที่ทราบแล้วและข้อจำกัดต่าง ๆ](service-collaborate-microsoft-teams.md#known-issues-and-limitations) ในบทความ “ทำงานร่วมกันใน Microsoft Teams"

## <a name="next-steps"></a>ขั้นตอนถัดไป

- [ทำงานร่วมกันใน Microsoft Teams ด้วย Power BI](service-collaborate-microsoft-teams.md)

มีคำถามเพิ่มเติมหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)
