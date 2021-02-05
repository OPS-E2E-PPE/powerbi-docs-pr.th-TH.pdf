---
title: ทำงานร่วมกันใน Microsoft Teams ด้วย Power BI
description: ในขณะที่พนักงานที่จัดไว้จะกลายเป็นบรรทัดฐานใหม่ มีองค์กรจำนวนมากขึ้นที่จำเป็นต้องขึ้นอยู่กับ Microsoft Teams เพื่อเปิดโอกาสในการทำงานทางไกลและเพื่อให้พนักงานสามารถซิงค์ข้อมูลได้
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: conceptual
LocalizationGroup: Share your work
ms.date: 12/14/2020
ms.openlocfilehash: 7c8fa59521be1cfc8bb25fb04c3904f257fb62be
ms.sourcegitcommit: 932f6856849c39e34229dc9a49fb9379c56a888a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/06/2021
ms.locfileid: "97926682"
---
# <a name="collaborate-in-microsoft-teams-with-power-bi"></a>ทำงานร่วมกันใน Microsoft Teams ด้วย Power BI

ในขณะที่พนักงานที่จัดไว้จะกลายเป็นบรรทัดฐานใหม่ มีองค์กรจำนวนมากขึ้นที่จำเป็นต้องขึ้นอยู่กับ Microsoft Teams เพื่อเปิดโอกาสในการทำงานทางไกลและเพื่อให้พนักงานสามารถซิงค์ข้อมูลได้ บทความนี้อธิบายถึงตัวเลือกในการแชร์และการทำงานร่วมกันในส่วนของเนื้อหา Power Bi แบบโต้ตอบในช่องทางการสื่อสารและการสนทนาของ Microsoft Teams 

- ด้วยแท็บ **Power BI** สำหรับ Microsoft Teams คุณสามารถ [ฝังรายงานแบบโต้ตอบในช่องทางการสื่อสารและการสนทนาของ Microsoft Teams](service-embed-report-microsoft-teams.md) แท็บ Power BI ช่วยให้เพื่อนร่วมงานของคุณสามารถค้นหาข้อมูลของทีมและหารือเกี่ยวกับข้อมูลภายในช่องทางการสื่อสารสำหรับทีมของคุณ 
- สร้าง[ตัวอย่างลิงก์](service-teams-link-preview.md) เมื่อคุณวางลิงก์ที่เชื่อมโยงไปยังรายงานของคุณ แดชบอร์ด และแอปต่าง ๆ ลงในกล่องข้อความ Microsoft Teams ตัวอย่างลิงก์แสดงข้อมูลเกี่ยวกับลิงก์ 
- ใช้[แชทใน Microsoft Teams](service-share-report-teams.md) เมื่อคุณดูรายงานและแดชบอร์ดในบริการ Power BI เพื่อเริ่มการสนทนาใน Microsoft Teams อย่างรวดเร็ว
- ใช้ [แอป Power BI ใน Microsoft Teams](service-microsoft-teams-app.md) เพื่อเปลี่ยนประสบการณ์การใช้งาน Power BI service แบบพื้นฐานของคุณให้เป็น Microsoft Teams
 
:::image type="content" source="media/service-collaborate-microsoft-teams/power-bi-embed-teams-report.png" alt-text="ภาพหน้าจอของ Power BI report ที่ฝังในช่องทาง Microsoft Teams":::

## <a name="requirements"></a>ข้อกำหนด

สำหรับ Power BI ที่จะทำงานใน Microsoft Teams ให้ตรวจสอบองค์ประกอบต่าง ๆ เหล่านี้:

- ผู้ใช้ของคุณสิทธิ์การใช้งาน Power BI Pro หรือรายงานที่มีอยู่ในความจุ [Power BI Premium (EM หรือ P SKU)](../admin/service-premium-what-is.md) พร้อมสิทธิ์การใช้งาน Power BI
- ผู้ใช้ลงชื่อเข้าใช้ในบริการของ Power BI เพื่อเปิดใช้สิทธิ์การใช้งาน Power BI ของตนเองแล้ว
- ผู้ใช้จะต้องปฏิบัติตามข้อกำหนดในการใช้งานแท็บ **Power BI** ใน Microsoft Teams

## <a name="grant-access-to-reports"></a>อนุญาตการเข้าถึงรายงาน

การฝังรายงานใน Microsoft Teams หรือการส่งลิงก์ไปยังรายการไม่ได้ให้สิทธิ์แก่ผู้ใช้ในการดูรายงานโดยอัตโนมัติ คุณจำเป็นต้อง[อนุญาตให้ผู้ใช้สามารถดูรายงานใน Power BI](service-share-dashboards.md) ได้ คุณสามารถใช้ Microsoft 365 Group สำหรับทีมของคุณเพื่อทำให้ง่ายขึ้น

> [!IMPORTANT]
> ให้ตรวจสอบให้แน่ใจว่าว่าใครสามารถดูรายงานภายใน Power BI service และอนุญาตให้เข้าถึงสิ่งที่ไม่ได้อยู่ในรายการ

วิธีหนึ่งในการตรวจสอบให้แน่ใจว่าทุกคนในทีมมีสิทธิ์เข้าถึงรายงานคือการวางรายงานในพื้นที่ทำงานเดียวและให้การเข้าถึง Microsoft 365 Group กับทีมของคุณ

## <a name="share-with-external-users"></a>แชร์กับผู้ใช้ภายนอก

คุณสามารถรวมรายงาน Power BI ใน Teams และแชร์กับผู้ใช้ภายนอกได้ ต่อไปนี้คือขั้นตอนที่ต้องดำเนินการ

1.  คุณเชิญผู้ใช้ภายนอกไปยังองค์กรและพวกเขายอมรับคำเชิญของคุณ ดู[กระจายเนื้อหา Power BI ให้กับผู้ใช้ที่เป็นผู้เยี่ยมชมภายนอก โดยใช้ Azure Active Directory B2B](../guidance/whitepaper-azure-b2b-power-bi.md) สำหรับรายละเอียด
2.  ให้สิทธิ์ผู้ใช้ภายนอกไปยังรายงาน การกำหนดสิทธิ์ทีละรายมีประสิทธิภาพสูงสุด
3.  ตรวจสอบให้แน่ใจว่าผู้ใช้ภายนอกมีสิทธิ์การใช้งาน Power BI ที่กำหนดให้กับพวกเขา ถ้าเนื้อหาอยู่ในความจุ Premium ผู้ใช้ต้องมีสิทธิ์การใช้งานฟรีเท่านั้น หากไม่เป็นเช่นนั้น ผู้ใช้สามารถ[ลงทะเบียนเพื่อทดลองใช้ Power BI Pro ฟรีเป็นรายบุคคลได้](../fundamentals/service-self-service-signup-for-power-bi.md#sign-up-for-an-individual-trial-of-power-bi-pro)

## <a name="known-issues-and-limitations"></a>ปัญหาและขีดจำกัดที่ทราบแล้ว

- Power BI ไม่รองรับภาษาที่แปลเป็นภาษาท้องถิ่นเช่นเดียวกับที่ Microsoft Teams รองรับ ผลที่ได้คือคุณอาจไม่เห็นการแปลที่เหมาะสมภายในรายงานแบบฝังตัว
- คุณไม่สามารถฝังแดชบอร์ด Power BI ในแท็บ **Power BI** สำหรับ Microsoft Teams ได้
- ผู้ใช้ที่ไม่มีสิทธิ์การใช้งาน Power BI หรือสิทธิ์ในการเข้าถึงรายงานจะเห็นข้อความ "เนื้อหาไม่พร้อมใช้งาน"
- คุณอาจพบปัญหาถ้าคุณใช้ Internet Explorer 10 <!--You can look at the [browsers support for Power BI](../fundamentals/power-bi-browsers.md) and for [Microsoft 365](https://products.office.com/office-system-requirements#Browsers-section). -->
- ไม่รองรับ [ตัวกรอง URL](service-url-filters.md) ที่มีแท็บ **Power BI** สำหรับ Microsoft Teams
- ในระบบคลาวด์ภายในประเทศ แท็บ **Power BI** ใหม่ไม่พร้อมใช้งาน รุ่นที่เก่ากว่าอาจพร้อมใช้งานที่ไม่รองรับพื้นที่ทำงานใหม่ พื้นที่ทำงานที่เคยทำ หรือรายงานในแอป Power BI
- หลังจากที่คุณบันทึกแท็บแล้ว คุณจะไม่สามารถเปลี่ยนชื่อแท็บผ่านการตั้งค่าแท็บได้ ใช้ตัวเลือก **เปลี่ยนชื่อ** เพื่อดำเนินการเปลี่ยนชื่อ
- การลงชื่อเข้าระบบครั้งเดียวไม่ได้รับการรองรับสำหรับบริการการแสดงตัวอย่างลิงก์
- การแสดงตัวอย่างลิงก์ไม่ทำงานในแชทการประชุมหรือแชนเนลส่วนตัว

## <a name="microsoft-power-platform-in-microsoft-teams"></a>Microsoft Power Platform ใน Microsoft Teams

แอป Microsoft Power Platform อื่น ๆ ยังรวมกับ Microsoft Teams เช่นกัน

- [ประสบการณ์ผู้ดูแลระบบ Power Platform](/power-platform/admin/about-teams-environment)
- [Power  Automate](/power-automate/teams/overview)
- [Power Apps](/powerapps/teams/overview)
- [Power Virtual Agents](/power-virtual-agents/)

## <a name="next-steps"></a>ขั้นตอนถัดไป

- [ฝังเนื้อหา Power BI ใน Microsoft Teams](service-embed-report-microsoft-teams.md)
- [รับตัวอย่างลิงก์ Power BI ใน Microsoft Teams](service-teams-link-preview.md)
- [แชทใน Microsoft Teams โดยตรงจากบริการ Power BI](service-share-report-teams.md)

มีคำถามเพิ่มเติมหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)
