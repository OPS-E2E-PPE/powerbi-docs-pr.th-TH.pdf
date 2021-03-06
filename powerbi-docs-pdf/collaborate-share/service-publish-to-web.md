---
title: เผยแพร่บนเว็บจาก Power BI
description: ด้วยตัวเลือกเผยแพร่บนเว็บจาก Power BI คุณสามารถฝังเนื้อหา Power BI แบบโต้ตอบ เช่น โพสต์ในบล็อก เว็บไซต์ อีเมล หรือสื่อทางสังคมได้อย่างง่ายดาย
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 01/14/2021
LocalizationGroup: Share your work
ms.openlocfilehash: 6b28537c9ea757fb43179196f9d7cb053955c5e0
ms.sourcegitcommit: ab28cf07b483cb4b01a42fa879b788932bba919d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "98227226"
---
# <a name="publish-to-web-from-power-bi"></a>เผยแพร่บนเว็บจาก Power BI

ด้วยตัวเลือก **เผยแพร่บนเว็บ** จาก Power BI คุณสามารถฝังเนื้อหา Power BI แบบโต้ตอบ เช่น โพสต์ในบล็อก เว็บไซต์ อีเมล หรือสื่อทางสังคมได้อย่างง่ายดาย คุณสามารถแก้ไข อัปเดต รีเฟรช หรือหยุดการแชร์การแสดงภาพที่คุณเผยแพร่ได้อย่างง่ายดาย

> [!WARNING]
> เมื่อคุณใช้ **การเผยแพร่บนเว็บ** ทุกคนบนอินเทอร์เน็ตสามารถดูรายงานหรือรูปภาพที่คุณเผยแพร่ การดูต้องไม่มีการตรวจสอบสิทธิ์ ซึ่งรวมถึงการดูข้อมูลระดับรายละเอียดที่รายงานของคุณรวม ก่อนที่จะเผยแพร่รายงาน ให้ตรวจสอบให้แน่ใจว่าคุณยินดีที่จะแชร์ข้อมูลและการจัดรูปแบบการแสดงข้อมูลแบบสาธารณะ อย่าเผยแพร่ข้อมูลที่เป็นความลับหรือมีกรรมสิทธิ์ ถ้ามีข้อสงสัย ให้ตรวจสอบนโยบายขององค์กรของคุณก่อนเผยแพร่

>[!Note]
>คุณสามารถฝังเนื้อหาของคุณได้อย่างปลอดภัยในพอร์ทัลหรือเว็บไซต์ภายใน ใช้ตัวเลือก [ฝังตัว](service-embed-secure.md) หรือ [ฝังใน SharePoint Online](service-embed-report-spo.md) ตัวเลือกเหล่านี้จะตรวจสอบให้แน่ใจว่ามีการบังคับใช้สิทธิ์และการรักษาความปลอดภัยของข้อมูลทั้งหมดเมื่อผู้ใช้ของคุณดูข้อมูลภายในของคุณ

## <a name="create-embed-codes-with-publish-to-web"></a>สร้างโค้ดฝังตัวที่มีการเผยแพร่บนเว็บ

**การเผยแพร่บนเว็บ** สามารถใช้งานได้สำหรับรายงานที่คุณแก้ไขในพื้นที่ทำงานส่วนตัวและกลุ่ม  ไม่สามารถใช้งานได้สำหรับรายงานที่แชร์กับคุณ หรือรายงานที่ใช้การรักษาความปลอดภัยระดับแถวเพื่อรักษาความปลอดภัยข้อมูล ดูหัวข้อ [**ข้อจำกัด**](#limitations)ด้านล่างสำหรับรายละเอียดกรณีทั้งห **มดที่ตัวเลือกการเผ** ยแพร่บนเว็บนั้นไม่รองรับ ตรวจสอบ **คำเตือน** ก่อนหน้าในบทความนี้ก่อนใช้ **การเผยแพร่บนเว็บ**

ขั้นตอนต่อไปนี้อธิบายวิธีการใช้ **เผยแพร่ไปยังเว็บ**

1. เปิดรายงานในพื้นที่ทำงานที่คุณสามารถแก้ไขได้และเลือก **ตัวเลือกเพิ่มเติม (...)**   > **ฝัง** > **เผยแพร่บนเว็บ (สาธารณะ)**

   ![เผยแพร่บนเว็บบนตัวเลือกเพิ่มเติม](media/service-publish-to-web/power-bi-more-options-publish-web.png)
   
2. ถ้าผู้ดูแลระบบ Power BI ของคุณไม่อนุญาตให้คุณสร้างโค้ดฝังตัว คุณอาจจำเป็นต้องติดต่อพวกเขา

   ![ติดต่อผู้ดูแลระบบ Power BI ของคุณ](media/service-publish-to-web/publish_to_web_admin_prompt.png)
   
   สำหรับความช่วยเหลือในการค้นหาบุคคลที่สามารถเปิดใช้งานเผยแพร่บนเว็บในองค์กรของคุณ โปรดดู [วิธีการค้นหาผู้ดูแลระบบ Power BI ของคุณ](#find-your-power-bi-administrator) ภายหลังในบทความนี้

3. ตรวจสอบเนื้อหากล่องโต้ตอบและเลือก **สร้างโค้ดฝังตัว**

   ![ตรวจสอบฝังในเว็บไซต์สาธารณะ](media/service-publish-to-web/publish_to_web2_ga.png)

4. ตรวจสอบคำเตือนที่แสดงในที่นี่ และยืนยันว่าข้อมูลสามารถฝังในเว็บไซต์สาธารณะได้ ถ้าเป็นเช่นนั้น เลือก **เผยแพร่**

   ![ตรวจสอบคำเตือน](media/service-publish-to-web/publish_to_web3_ga.png)

5. ในกล่องโต้ตอบ **ความสำเร็จ** คุณจะเห็นตัวอย่างว่ารายงานจะมีลักษณะอย่างไร เลือก **ขนาด** และ **หน้าเริ่มต้น** 

    คุณยังสามารถเพิ่มรูป **ตัวแทนข้อความ** เพื่อทำให้หน้าเว็บโหลดได้รวดเร็วขึ้น ด้วยรูปตัวแทนข้อความ ผู้คนที่ดูรายงานของคุณบนเว็บจะเห็นปุ่ม **ดูเนื้อหาเชิงโต้ตอบ** ที่พวกเขาสามารถเลือกดูรายงานได้ 

    ทำการเปลี่ยนแปลงเหล่านั้นก่อน จากนั้นคัดลอกลิงก์เพื่อส่งไปยังอีเมลหรือคัดลอก HTML ที่จะวางลงในเว็บไซต์ คุณสามารถฝังลิงก์ในโค้ดเช่น iFrame หรือวางไว้ในเว็บเพจหรือบล็อกโดยตรง

   ![ความสำเร็จ: ลิงก์และ HTML](media/service-publish-to-web/publish_to_web4.png)

6. ถ้าคุณเคยสร้างโค้ดฝังตัวสำหรับรายงาน และคุณเลือก **เผยแพร่บนเว็บ** มาก่อนแล้ว คุณจะไม่เห็นกล่องโต้ตอบในขั้นตอนที่ 2-4 แต่คุณจะเห็นกล่องโต้ตอบ **ฝังโค้ด** แทน

   ![กล่องโต้ตอบของโค้ดฝังตัว](media/service-publish-to-web/publish_to_web5.png)

   คุณสามารถสร้างโค้ดฝังตัวหนึ่งโค้ดสำหรับแต่ละรายงาน

### <a name="tips-for-view-modes"></a>เคล็ดลับสำหรับโหมดมุมมอง

เมื่อคุณฝังเนื้อหาภายในโพสต์ในบล็อก โดยทั่วไปแล้วจำเป็นต้องพอดีภายในขนาดหน้าจอที่เฉพาะเจาะจง  คุณสามารถปรับความสูงและความกว้างเป็นแท็ก iFrame ตามความจำเป็น อย่างไรก็ตาม คุณจำเป็นต้องให้แน่ใจว่ารายงานของคุณพอดีกับพื้นที่ของ iFrame ที่กำหนดไว้ ดังนั้นให้ตั้งค่าเป็นโหมดมุมมองที่เหมาะสมเมื่อคุณแก้ไขรายงาน

ตารางต่อไปนี้มีคำแนะนำเกี่ยวกับโหมดมุมมอง และวิธีจะปรากฏเมื่อถูกฝังตัว

| โหมดมุมมอง | มันจะเห็นอย่างไรเมื่อถูกฝังตัว |
| --- | --- |
| ![PtW6b](media/service-publish-to-web/publish_to_web6b.png) |**พอดีกับหน้า** ตามความสูงและความกว้างของหน้าในรายงานของคุณ ถ้าคุณตั้งค่าหน้าของคุณเป็นอัตราส่วน *แบบไดนามิก* เช่น 16:9 หรือ 4:3 เนื้อหาของคุณจะปรับขนาดให้พอดีภายใน iFrame เมื่อฝังใน iFrame โดยใช้ **ให้พอดีกับหน้า** อาจก่อให้เกิด *letterboxing* ที่พื้นหลังสีเทาถูกแสดงในพื้นที่ของ iFrame หลังจากเนื้อหาถูกปรับขนาดให้พอดีกับภายใน iFrame เมื่อต้องการย่อ letterboxing ให้เล็กที่สุด ให้ตั้งค่าความสูงและกว้างของ iFrame ของคุณให้เหมาะสม |
| ![PtW6d](media/service-publish-to-web/publish_to_web6d.png) |**ขนาดจริง** จะให้แน่ใจว่ารายงานรักษาขนาดตามที่ตั้งค่าหน้ารายงาน ซึ่งอาจทำให้แถบเลื่อนปรากฎใน iFrame ของคุณ ตั้งค่าความสูงและความกว้างของ iFrame เพื่อหลีกเลี่ยงแถบเลื่อน |
| ![PtW6c](media/service-publish-to-web/publish_to_web6c.png) |**จัดพอดีกับความกว้าง** ตรวจสอบให้แน่ใจว่าเนื้อหาพอดีกับพื้นที่แนวนอนของ iFrame เส้นขอบจะยังคงแสดงอยู่ แต่เนื้อหาจะปรับมาตราส่วนเพื่อใช้ช่องว่างแนวนอนที่มีทั้งหมด |

### <a name="tips-for-iframe-height-and-width"></a>เคล็ดลับสำหรับความกว้างและความสูงของ iFrame

โค้ดฝังตัว **เผยแพร่บนเว็บ** มีลักษณะดังต่อไปนี้:

![PtW7](media/service-publish-to-web/publish_to_web7.png)
 
คุณสามารถแก้ไขความกว้างและความสูงด้วยตนเอง เพื่อให้แน่ใจอย่างแม่นยำว่าคุณต้องการให้พอดีกับหน้าที่คุณกำลังฝัง

เพื่อให้ได้ขนาดที่พอดียิ่งขึ้น คุณสามารถลองเพิ่ม 56 พิกเซลไปที่ความสูงของ iFrame เพื่อให้สอดคล้องกับขนาดปัจจุบันของแถบด้านล่าง ถ้าหน้าของรายงานใช้ขนาดแบบไดนามิก ตารางด้านล่างแสดงขนาดบางอย่างคุณสามารถทำให้พอดีโดยไม่ต้องจัดแบบ letterbox

| อัตราส่วน | ขนาด | มิติ (ความกว้าง x ความสูง) |
| --- | --- | --- |
| 16:9 |ขนาดเล็ก |640 x 416 px |
| 16:9 |ขนาดปานกลาง |800 x 506 px |
| 16:9 |ขนาดใหญ่ |960 x 596 px |
| 4:3 |ขนาดเล็ก |640 x 536 px |
| 4:3 |ขนาดปานกลาง |800 x 656 px |
| 4:3 |ขนาดใหญ่ |960 x 776 px |

## <a name="manage-embed-codes"></a>จัดการโค้ดแบบฝังตัว

เมื่อคุณสร้างโค้ดฝังตัวของ **เผยแพร่บนเว็บ** คุณสามารถจัดการโค้ดจากเมนู **การตั้งค่า** ใน Power BI การจัดการโค้ดฝังตัวมีความสามารถในการลบภาพปลายทางหรือรายงานสำหรับโค้ด (แสดงโค้ดฝังตัวที่ไม่สามารถใช้งาน) หรือได้รับโค้ดฝังตัว

1. เพื่อจัดการฝังรหัส **เผยแพร่ไปยังเว็บ** ของคุณ เปิดเฟือง **การตั้งค่า** แล้วเลือก **จัดการโค้ดฝังตัว**

   ![จัดการโค้ดแบบฝังตัว](media/service-publish-to-web/publish_to_web8.png)

2. โค้ดฝังตัวของคุณจะปรากฏขึ้น

   ![PtW9](media/service-publish-to-web/publish_to_web9.png)

3. คุณสามารถเรียกใช้ หรือลบโค้ดฝังตัว การลบจะปิดใช้งานลิงก์ไปยังรายงานหรือรูปภาพ

   ![PtW10](media/service-publish-to-web/publish_to_web10.png)

4. ถ้าคุณเลือก **ลบ** ระบบจะสอบถามการยืนยันจากคุณ

   ![PtW11](media/service-publish-to-web/publish_to_web11.png)

## <a name="updates-to-reports-and-data-refresh"></a>อัปเดตรายงานและรีเฟรชข้อมูล

หลังจากที่คุณสร้างโค้ดฝังตัวของ **การเผยแพร่ไปยังเว็บ** ของคุณและแชร์ไฟล์แล้ว รายงานจะอัปเดตพร้อมกับการเปลี่ยนแปลงที่คุณทำ การเชื่อมโยงโค้ดแบบฝังตัวจะใช้งานได้ทันที ทุกคนที่เปิดลิงก์สามารถดูได้ ข้อมูลถูกแคชในหนึ่งชั่วโมงจากเวลาที่จะถูกเรียกใช้ เราไม่แนะนำให้ใช้การเผยแพร่ไปยังเว็บสำหรับข้อมูลที่จำเป็นต้องรีเฟรชบ่อยครั้ง เมื่อต้องการเรียนรู้เพิ่มเติม ให้ดูหัวข้อ [**วิธีการทำงาน**](#howitworks)ในภายหลังในบทความนี้ 

### <a name="data-refresh"></a>การรีเฟรชข้อมูล

รีเฟรชข้อมูลเป็นภาพสะท้อนในรายงานแบบฝังตัวหรือแบบรูปภาพอัตโนมัติของคุณ เมื่อข้อมูลถูกรีเฟรชสำหรับแบบจำลองข้อมูลนำเข้าในบริการ Power BI บริการจะล้างแคชข้อมูล ทำให้อัปเดตข้อมูลได้อย่างรวดเร็ว หากต้องการปิดการใช้งานรีเฟรชโดยอัตโนมัติ เลือก **อย่ารีเฟรช** ตามกำหนดการสำหรับชุดข้อมูลที่รายงานใช้  

### <a name="heavy-usage"></a>การใช้งานหนักหน่วง

ประสบการณ์การใช้งานหนักหน่วงอาจเกิดขึ้นได้เมื่อรายงานได้รับคิวรีมากเกินไปในช่วงเวลาสั้น ๆ เมื่อเกิดภาวะการใช้งานหนักหน่วง ผู้ใช้จะไม่สามารถดูหรือโต้ตอบกับรายงานได้จนกว่าจะผ่านพ้นช่วงเวลาของการใช้งานหนักหน่วงไป 

เราขอแนะนำให้ตั้งค่าภาพตัวแทนสำหรับรายงานของคุณ หากเกิดภาวะการใช้งานหนักหน่วง ผู้ใช้จะเห็นภาพตัวแทน 

เพื่อช่วยหลีกเลี่ยงประสบการณ์การใช้งานหนักหน่วง ให้จำกัดจำนวนคิวรีที่ไม่ซ้ำกันที่รายงานของคุณสามารถสร้างได้และความถี่ในการรีเฟรชข้อมูล ดู[คำแนะนำการปรับให้เหมาะสมของ Power BI](../guidance/power-bi-optimization.md) สำหรับเคล็ดลับในการปรับปรุงรายงานให้มีประสิทธิภาพขึ้น

## <a name="power-bi-visuals"></a>วิชวล Power BI

วิชวล Power BI รองรับ **การเผยแพร่ไปยังเว็บ** เมื่อคุณใช้ **การเผยแพร่ไปยังเว็บ** ผู้ใช้ที่คุณแชร์ภาพที่เผยแพร่ของคุณไม่จำเป็นต้องเปิดใช้งานวิชวล Power BI เพื่อดูรายงาน

## <a name="understanding-the-embed-code-status-column"></a>ทำความเข้าใจเกี่ยวกับคอลัมน์สถานะโค้ดฝังตัว

>[!Note]
>ตรวจสอบโค้ดฝังตัวที่คุณเผยแพร่บ่อยครั้ง ลบรายการใดๆ ที่ไม่จำเป็นต้องมีให้ใช้งานแบบสาธารณะอีกต่อไป

หน้า **จัดการโค้ดฝังตัว** ประกอบด้วยคอลัมน์สถานะ ตามค่าเริ่มต้น โค้ดฝังตัวจะ **เปิดใช้งานอยู่** แต่อาจอยู่ในสถานะใดสถานะหนึ่งดังที่แสดงอยู่ด้านล่าง

| สถานะ | คำอธิบาย |
| --- | --- |
| **ใช้งานอยู่** |รายงานจะพร้อมใช้งานสำหรับผู้ใช้อินเทอร์เน็ตเพื่อดูและโต้ตอบ |
| **ถูกบล็อก** |เนื้อหาของรายงานการละเมิด[ เงื่อนไขการใช้บริการ Power BI](https://powerbi.microsoft.com/terms-of-service) Microsoft ได้บล็อกไว้ ติดต่อฝ่ายสนับสนุนหากคุณเชื่อว่าเนื้อหาที่ถูกบล็อกมาจากความผิดพลาด |
| **ไม่รองรับ** |ชุดข้อมูลของรายงานใช้ความปลอดภัยระดับแถว หรือไม่รองรับการกำหนดค่าอื่น ดูหัวข้อ [**ข้อจำกัด**](#limitations)สำหรับรายการทั้งหมด |
| **ถูกละเมิด** |โค้ดฝังตัวอยู่นอกนโยบายที่กำหนดไว้โดยผู้เช่า สถานะนี้มักเกิดขึ้นเมื่อสร้างโค้ดฝังตัว และการตั้งค่าผู้เช่าของ **การเผยแพร่ไปยังเว็บ** มีการเปลี่ยนแปลงเพื่อไม่รวมผู้ใช้ที่เป็นเจ้าของโค้ดฝังตัว ถ้าการตั้งค่าผู้เช่าถูกปิด หรือผู้ใช้ไม่ได้รับอนุญาตให้สร้างโค้ดฝังตัว โค้ดฝังตัวที่มีอยู่จะแสดงสถานะ **ถูกละเมิด** ดูส่วน [ค้นหาผู้ดูแลระบบ Power BI ของคุณ](#find-your-power-bi-administrator) ในบทความนี้สำหรับรายละเอียด |

## <a name="report-a-concern-with-publish-to-web-content"></a>รายงานข้อจำกัดเกี่ยวกับเนื้อหาการเผยแพร่ไปยังเว็บ

เพื่อรายงานข้อจำกัดเกี่ยวกับเนื้อหา **เผยแพร่ไปยังเว็บ** แบบฝังหรือบล็อก เลือกไอคอน **ค่าสถานะ** ในแถบด้านล่างของรายงาน **เผยแพร่ไปยังเว็บ**

![PtW12](media/service-publish-to-web/publish_to_web12_ga.png)

คุณจะต้องส่งอีเมลไปยัง Microsoft เพื่ออธิบายสิ่งที่คุณเป็นกังวล Microsoft จะประเมินเนื้อหาที่ยึดตาม [เงื่อนไขการใช้บริการ Power BI ](https://powerbi.microsoft.com/terms-of-service) และดำเนินการที่เหมาะสม

## <a name="licensing"></a>สิทธิ์การใช้งาน

คุณจำเป็นต้องเป็นผู้ใช้ Microsoft Power BI เพื่อใช้ **เผยแพร่ไปยังเว็บ** ผู้ชมของรายงานของคุณไม่จำเป็นต้องเป็นผู้ใช้ Power BI

<a name="howitworks"></a>
## <a name="how-it-works-technical-details"></a>ทำงานอย่างไร (รายละเอียดทางเทคนิค)

เมื่อคุณสร้างโค้ดฝังตัวโดยใช้ **การเผยแพร่บนเว็บ** ผู้ใช้บนอินเทอร์เน็ตจะมองเห็นรายงานได้ ซึ่งสามารถใช้งานแบบสาธารณะได้ ดังนั้นคุณจึงสามารถคาดหวังให้ผู้ชมแชร์รายงานผ่านสื่อสังคมในอนาคตได้อย่างง่ายดาย ผู้ใช้ดูรายงานโดยการเปิด URL สาธารณะโดยตรงหรือดูรายงานที่ฝังอยู่ในหน้าเว็บหรือบล็อก เมื่อทำเช่นนั้น Power BI จะแคชข้อกำหนดของรายงานและผลลัพธ์ของคิวรีที่จำเป็นในการดูรายงาน การแคชข้อมูลนี้ทำให้แน่ใจว่าผู้ใช้พร้อมกันหลายพันคนสามารถดูรายงานโดยไม่ส่งผลกระทบต่อประสิทธิภาพการทำงาน

ข้อมูลถูกแคชในหนึ่งชั่วโมงจากเวลาที่จะถูกเรียกใช้ ถ้าคุณอัปเดตข้อกำหนดรายงาน (ตัวอย่างเช่น ถ้าคุณเปลี่ยนโหมดมุมมอง) หรือรีเฟรชข้อมูลรายงาน อาจใช้เวลาสักครู่ก่อนที่การเปลี่ยนแปลงจะปรากฏในเวอร์ชันของรายงานที่ผู้ใช้ของคุณดู เมื่อเกิดการรีเฟรชข้อมูลสำหรับแบบจำลองข้อมูลนำเข้า บริการจะล้างข้อมูลที่แคชและดึงข้อมูลใหม่ ในกรณีส่วนใหญ่ ข้อมูลจะได้รับการอัปเดตเกือบพร้อมกันกับการนำเข้าข้อมูล อย่างไรก็ตามสำหรับรายงานที่มีคิวรีที่ไม่ซ้ำกันมากมาย อาจใช้เวลาในการอัปเดตสักครู่ เนื่องจากแต่ละองค์ประกอบและค่าข้อมูลถูกแคชไว้อย่างอิสระเมื่อการอัปเดตข้อมูลเกิดขึ้น ผู้ใช้สามารถมองเห็นการผสมของค่าปัจจุบันและก่อนหน้านี้ได้ ดังนั้นจึงแนะนำให้คุณจัดลำดับการทำงานของคุณล่วงหน้า และสร้างโค้ดฝังตัวสำหรับการ **เผยแพร่ไปยังเว็บ** เฉพาะเมื่อคุณพอใจกับการตั้งค่าแล้วเท่านั้น ถ้าข้อมูลของคุณจะรีเฟรช ให้ลดจำนวนรีเฟรชและดำเนินการรีเฟรชในเวลาที่ออก เราไม่แนะนำให้ใช้การเผยแพร่ไปยังเว็บสำหรับข้อมูลที่จำเป็นต้องรีเฟรชบ่อยครั้ง

## <a name="find-your-power-bi-administrator"></a>ค้นหาผู้ดูแลระบบ Power BI ของคุณ

พอร์ทัลผู้ดูแลระบบ Power BI มีการตั้งค่าที่ควบคุมว่าใครใดสามารถเผยแพร่ไปยังเว็บได้ ทำงานกับ [ผู้ดูแลระบบ Power BI](../admin/service-admin-role.md) ขององค์กรเพื่อเปลี่ยน [การตั้งค่าผู้เช่าสำหรับเผยแพร่ไปยังเว็บ](../admin/service-admin-portal.md#publish-to-web) ในพอร์ทัลผู้ดูแลระบบ

สำหรับองค์กรที่มีขนาดเล็กกว่าหรือบุคคลที่ลงทะเบียนสำหรับ Power BI คุณอาจยังไม่มีผู้ดูแลระบบ Power BI ทำตาม [กระบวนการสำหรับการเข้าครองผู้ดูแลระบบ](/azure/active-directory/users-groups-roles/domains-admin-takeover)ของเรา เมื่อคุณมีผู้ดูแลระบบ Power BI แล้ว พวกเขาสามารถเปิดใช้งานการสร้างโค้ดฝังตัวให้คุณได้

องค์กรที่สร้างขึ้นมักจะมีผู้ดูแลระบบ Power BI อยู่แล้ว บุคคลในบทบาทต่อไปนี้สามารถทำหน้าที่เป็นผู้ดูแลระบบ Power BI ได้:

- ผู้ดูแลระบบส่วนกลาง
- ผู้ใช้ที่มีบทบาทผู้ดูแลระบบบริการของ Power BI ใน Azure Active Directory

คุณจำเป็นต้อง [ค้นหาหนึ่งในบุคคลเหล่านี้](/office365/admin/admin-overview/admin-overview#who-has-admin-permissions-in-my-business) ในองค์กรของคุณและขอให้พวกเขาอัปเดต [การตั้งค่าผู้เช่าสำหรับเผยแพร่ไปยังเว็บ](../admin/service-admin-portal.md#publish-to-web) ในพอร์ทัลผู้ดูแลระบบ

## <a name="limitations"></a>ข้อจำกัด

**การเผยแพร่ไปยังเว็บ** ได้รับการรองรับสำหรับแหล่งข้อมูลส่วนใหญ่และรายงานในบริการของ Power BI อย่างไรก็ตาม รายงานประเภทต่อไปนี้ยังไม่ได้รับการรองรับ หรือไม่พร้อมใช้งานสำหรับ **เผยแพร่ไปยังเว็บ** ในขณะนี้:

- รายงานที่ใช้การรักษาความปลอดภัยระดับแถว
- รายงานที่ใช้แหล่งข้อมูลแบบไลฟ์ใดๆ รวมถึง Analysis Services Tabular ที่โฮสต์ภายในองค์กร Analysis Services Multidimensional และ Azure Analysis Services
- รายงานที่ใช้[ชุดข้อมูลที่ใช้ร่วมกัน](../connect-data/service-datasets-across-workspaces.md) ซึ่งจัดเก็บไว้ในพื้นที่ทำงานที่แตกต่างกันจากรายงาน
- [ชุดข้อมูลที่ใช้ร่วมกันและได้รับการรับรอง](../connect-data/service-datasets-share.md)
- รายงานที่แชร์กับคุณโดยตรง หรือผ่านแอป
- รายงานในพื้นที่ทำงานที่คุณไม่ใช่สมาชิกที่มีสิทธิ์แก้ไข
- โดยในขณะนี้ ระบบยังไม่รองรับการใช้วิชวล "R" และ Python ในรายงานที่ **เผยแพร่ขึ้นบนเว็บ**
- การส่งออกข้อมูลจากวิชวลในรายงานที่เผยแพร่ไปยังเว็บ
- ArcGIS Maps สำหรับภาพ Power BI
- ถาม-ตอบ เกี่ยวกับ Power BI visuals
- รายงานที่ประกอบด้วยหน่วยวัดของ DAX ระดับรายงาน
- การลงชื่อเข้าระบบแบบจำลองคิวรีข้อมูลเพียงครั้งเดียว
- รักษาข้อมูลความลับหรือกรรมสิทธิ์
- ความสามารถในการรับรองความถูกต้องโดยอัตโนมัติที่มาพร้อมกับการ **ฝัง** ตัวเลือกที่ไม่ทำงานกับ Power BI JavaScript API สำหรับ Power BI JavaScript API ให้ใช้[ผู้ใช้เป็นเจ้าของข้อมูล](../developer/embedded/embed-sample-for-your-organization.md)ในการฝัง
- ผู้ดูแลระบบสามารถบล็อกการเข้าถึงอินเทอร์เน็ตสาธารณะตามที่อธิบายไว้ใน[ลิงก์ส่วนตัวสำหรับการเข้าถึง Power BI](../admin/service-security-private-links.md) ในกรณีนั้น ตัวเลือก **เผยแพร่ไปยังเว็บ** จะเป็นสีเทาสำหรับผู้เช่าของคุณในพอร์ทัลผู้ดูแลระบบ Power BI 

## <a name="next-steps"></a>ขั้นตอนถัดไป

- [Web part สำหรับรายงาน SharePoint Online](service-embed-report-spo.md) 

- [ฝังรายงานในพอร์ทัลความปลอดภัยหรือเว็บไซต์](service-embed-secure.md)

มีคำถามเพิ่มเติมหรือไม่ [ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)
