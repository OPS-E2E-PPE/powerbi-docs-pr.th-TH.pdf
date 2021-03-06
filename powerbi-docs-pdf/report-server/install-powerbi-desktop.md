---
title: ติดตั้ง Power BI Desktop สำหรับเซิร์ฟเวอร์รายงาน Power BI
description: เรียนรู้วิธีการติดตั้ง Power BI Desktop สำหรับเซิร์ฟเวอร์รายงาน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.date: 10/16/2020
ms.openlocfilehash: 068d4a025bda878899e2d54f93bc56eaea336f3e
ms.sourcegitcommit: 7ed995eed0fd6e718748accf87bae384211cd95d
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2021
ms.locfileid: "99044091"
---
# <a name="install-power-bi-desktop-for-power-bi-report-server"></a>ติดตั้ง Power BI Desktop สำหรับเซิร์ฟเวอร์รายงาน Power BI

เมื่อต้องสร้างรายงาน Power BI สำหรับเซิร์ฟเวอร์รายงาน Power BI คุณจำเป็นต้องดาวน์โหลดและติดตั้ง Power BI Desktop เวอร์ชันที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI การเผยแพร่นี้จะแตกต่างจาก Power BI Desktop ที่ใช้กับบริการ Power BI ตัวอย่างเช่น เวอร์ชันของ Power BI Desktop สำหรับบริการของ Power BI ที่มีคุณลักษณะการแสดงตัวอย่าง คุณลักษณะเหล่านั้นไม่ได้อยู่ในเวอร์ชัน Power BI Report Server จนกว่าจะพร้อมใช้งานทั่วไป การใช้การเผยแพรนี้จะทำให้แน่ใจว่า เซิร์ฟเวอร์รายงานสามารถโต้ตอบกับรายงานและแบบจำลองเวอร์ชันที่ทราบแล้วได้ 

ไม่ต้องกังวล คุณสามารถติดตั้ง Power BI Desktop และ Power BI Desktop สำหรับเซิร์ฟเวอร์รายงาน Power BI แบบเคียงข้างกันบนคอมพิวเตอร์เครื่องนี้

## <a name="download-and-install-power-bi-desktop"></a>ดาวน์โหลด และติดตั้ง Power BI Desktop

วิธีที่ง่ายที่สุดในการตรวจสอบให้แน่ใจว่าคุณมี Power BI Desktop เวอร์ชันที่อัปเดตล่าสุดสำหรับเซิร์ฟเวอร์รายงาน Power BI คือการเริ่มต้นจากพอร์ทัลของเว็บของเซิร์ฟเวอร์รายงานของคุณ

1. ในพอร์ทัลเว็บเซิร์ฟเวอร์รายงาน เลือก **ดาวน์โหลด** ลูกศร > **Power BI Desktop**

    ![ดาวน์โหลด Power BI Desktop จากพอร์ทัลของเว็บ](media/install-powerbi-desktop/report-server-download-web-portal.png)

    หรือไปที่หน้าหลัก [เซิร์ฟเวอร์รายงาน Power BI](https://powerbi.microsoft.com/report-server/) แล้วเลือก **ตัวเลือกการดาวน์โหลดขั้นสูง**

2. ในหน้าศูนย์ดาวน์โหลด ให้เลือกภาษา จากนั้นเลือก **ดาวน์โหลด**

3. ขึ้นอยู่กับคอมพิวเตอร์ของคุณ เลือก: 

    - **PBIDesktopRS.msi** (เวอร์ชัน 32 บิต) หรือ
    - **PBIDesktopRS_x64.msi** (เวอร์ชัน 64 บิต)

1. หลังจากที่คุณดาวน์โหลดตัวติดตั้งแล้ว เรียกใช้ตัวช่วยสร้างการติดตั้ง Power BI Desktop

2. ในตอนท้ายของการติดตั้ง เลือก **เรียกใช้ Power BI Desktop**

    จะเริ่มต้นโดยอัตโนมัติ และคุณก็พร้อมที่จะไปต่อ

## <a name="verify-youre-using-the-correct-version"></a>ตรวจสอบว่าคุณกำลังใช้เวอร์ชันที่ถูกต้อง
เป็นเรื่องง่ายเมื่อต้องการตรวจสอบว่าคุณกำลังใช้ Power BI Desktop ที่ถูกต้องอยู่: ดูที่เปิดใช้งานหน้าจอหรือแถบชื่อเรื่องภายใน Power BI Desktop คุณสามารถบอกได้ว่าคุณมีเวอร์ชันที่ถูกต้องเนื่องจาก **Power BI Desktop (มกราคม๒๐๒๑)** หรือใหม่กว่าอยู่ในแถบชื่อเรื่อง นอกจากนี้ สีโลโก้ Power BI จะกลับกันโดยสีเหลืองจะอยู่บนพื้นดำแทนที่เป็นสีดำบนพื้นเหลือง

![Power BI Desktop มกราคม๒๐๒๑](media/install-powerbi-desktop/power-bi-report-server-desktop.png)

เวอร์ชั่น Power BI Desktop สำหรับบริการ Power BI ไม่มีเดือนและปีในแถบรายการชื่อ

## <a name="file-extension-association"></a>การเชื่อมโยงนามสกุลไฟล์
สมมติว่าคุณได้ติดตั้งทั้ง Power BI Desktop และ Power BI Desktop สำหรับเซิร์ฟเวอร์รายงาน Power BI บนเครื่องเดียวกัน การติดตั้ง Power BI Desktop ครั้งล่าสุดของคุณมีการเชื่อมโยงไฟล์กับไฟล์ .pbix ดังนั้นแล้วเมื่อคุณดับเบิลคลิกที่ไฟล ์.pbix ก็จะเปิดใช้ Power BI Desktop ที่คุณได้ทำการติดตั้งล่าสุด

ถ้าคุณมี Power BI Desktop และจากนั้นติดตั้ง Power BI Desktop สำหรับเซิร์ฟเวอร์รายงาน Power BI ไฟล์ .pbix เปิดใน Power BI Desktop สำหรับเซิร์ฟเวอร์รายงาน Power BI ตามค่าเริ่มต้น ถ้าคุณต้องการให้ Power BI Desktop เป็นค่าเริ่มต้นแทนสำหรับเปิดใช้งานเมื่อเปิดไฟล์ .pbix ให้ติดตั้ง [ Power BI Desktop จาก Microsoft Store ใหม่](https://aka.ms/pbidesktopstore)

คุณสามารถเปิด Power BI Desktop เวอร์ชันที่คุณต้องการใช้ก่อนได้เสมอ จากนั้น ให้เปิดไฟล์จากภายใน Power BI Desktop

นี่คือวิธีที่ปลอดภัยที่สุดในการเปิด Power BI Desktop เวอร์ชันที่ถูกต้อง เริ่มต้นการแก้ไขรายงาน Power BI จากภายใน Power BI Report Server หรือสร้างรายงาน Power BI ใหม่จากบริการของ Power BI

## <a name="considerations-and-limitations"></a>ข้อควรพิจารณาและข้อจำกัด

รายงาน Power BI ในเซิร์ฟเวอร์รายงาน Power BI ในบริการของ Power BI (`https://app.powerbi.com`) และในแอปสำหรับอุปกรณ์เคลื่อนที่ Power BI ทำงานในลักษณะที่ใกล้เคียงกัน  แต่จะมีบางคุณลักษณ์ที่แตกต่างกัน

### <a name="selecting-a-language"></a>การเลือกภาษา

สำหรับ Power BI Desktop สำหรับเซิร์ฟเวอร์รายงาน Power BI คุณเลือกภาษาเมื่อคุณติดตั้งแอป ซึ่งหลังจากนี้คุณจะไม่สามารถเปลี่ยนภาษาได้ แต่คุณสามารถติดตั้งเวอร์ชันในภาษาอื่นได้

### <a name="report-visuals-in-a-browser"></a>การแสดงภาพรายงานในเบราว์เซอร์

รายงานของเซิร์ฟเวอร์รายงาน Power BI รองรับส่วนการแสดงผลเกือบทั้งหมด รวมทั้งส่วนวิชวล Power BI รายงานในเซิร์ฟเวอร์รายงาน Power BI ไม่สนับสนุน:

* วิชวล R
* การนำทางแบบแสดงเส้นนำทาง
* คุณลักษณะที่เป็นตัวอย่างใน Power BI Desktop

### <a name="reports-in-the-power-bi-mobile-apps"></a>รายงานในแอปสำหรับอุปกรณ์เคลื่อนที่ Power BI

รายงานในเซิร์ฟเวอร์รายงาน Power BI สนับสนุนฟังก์ชันพื้นฐานทั้งหมดใน[แอปสำหรับอุปกรณ์เคลื่อนที่ Power BI](../consumer/mobile/mobile-apps-for-mobile-devices.md) รวมถึง:

* [เค้าโครงรายงานโทรศัพท์](../create-reports/desktop-create-phone-report.md): คุณสามารถปรับรายงานให้เหมาะสมกับแอปสำหรับอุปกรณ์เคลื่อนที่ Power BI ได้ บนโทรศัพท์มือถือของคุณ รายงานที่ปรับให้เหมาะสมมีไอคอนพิเศษ ![ไอคอนเค้าโครงรายงานโทรศัพท์](media/install-powerbi-desktop/power-bi-rs-mobile-optimized-icon.png) และเค้าโครงที่เหมาะกับมือถือ
  
    ![รายงานที่ปรับให้เหมาะสมสำหรับมือถือ](media/install-powerbi-desktop/power-bi-rs-mobile-optimized-report.png)

รายงานในเซิร์ฟเวอร์รายงาน Power BI ไม่สนับสนุนคุณลักษณะเหล่านี้ในแอปสำหรับอุปกรณ์เคลื่อนที่ Power BI:

* วิชวล R
* วิชวล Power BI
* การนำทางแบบแสดงเส้นนำทาง
* การกรองพรมแดนหรือบาร์โค้ด

### <a name="custom-security"></a>การรักษาความปลอดภัยแบบกำหนดเอง

Power BI Desktop สำหรับเซิร์ฟเวอร์รายงาน Power BI ไม่สนับสนุนการรักษาความปลอดภัยแบบกำหนดเอง ถ้ามีการกำหนดค่าเซิร์ฟเวอร์รายงาน Power BI ของคุณด้วยส่วนขยายการรักษาความปลอดภัยแบบกำหนดเอง คุณจะไม่สามารถบันทึกรายงาน Power BI จาก Power BI Desktop (ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI) ไปยังอินสแตนซ์เซิร์ฟเวอร์รายงาน Power BI ได้ คุณจำเป็นต้องบันทึกไฟล์รายงานนามสกุล .pbix จาก Power BI Desktop และอัปโหลดไปยังไซต์พอร์ทัลเซิร์ฟเวอร์รายงาน Power BI

### <a name="saving-reports-to-a-power-bi-report-server-in-a-different-domain"></a>การบันทึกรายงานไปยังเซิร์ฟเวอร์รายงาน Power BI ในโดเมนอื่น

เมื่อคุณบันทึกรายงาน Power BI ไปยังเซิร์ฟเวอร์รายงาน Power BI ข้อมูลประจำตัว Windows ของคุณจะถูกใช้ การบันทึกไปยังเซิร์ฟเวอร์รายงานในโดเมนอื่นโดยตรง ข้อมูลประจำตัว Windows ของคุณ จะไม่ได้รับการสนับสนุน คุณสามารถใช้เว็บเบราว์เซอร์เพื่อดูเซิร์ฟเวอร์รายงาน และอัปโหลดไฟล์จากเครื่องของคุณแทน

## <a name="next-steps"></a>ขั้นตอนถัดไป

หลังจากที่ติดตั้ง Power BI Desktop แล้ว คุณสามารถเริ่มการสร้างรายงาน Power BI ได้

[สร้างรายงาน Power BI สำหรับเซิร์ฟเวอร์รายงาน Power BI](quickstart-create-powerbi-report.md)  
[เซิร์ฟเวอร์รายงาน Power BI คืออะไร](get-started.md)

มีคำถามเพิ่มเติมหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)

