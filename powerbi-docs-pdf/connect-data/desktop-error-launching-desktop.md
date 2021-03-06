---
title: แก้ไขปัญหาเมื่อเริ่มต้น Power BI Desktop
description: แก้ไขปัญหาเมื่อเริ่มต้น Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: troubleshooting
ms.date: 11/14/2020
LocalizationGroup: Troubleshooting
ms.openlocfilehash: c41f8f9b23ef57d5dd6fd4b851918b7ffa5904a0
ms.sourcegitcommit: ab28cf07b483cb4b01a42fa879b788932bba919d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "98226950"
---
# <a name="troubleshoot-opening-power-bi-desktop"></a>แก้ไขปัญหาการเปิด Power BI Desktop

บทความนี้อธิบายและให้วิธีการแก้ไขสำหรับตัวเลขของสถานการณ์ต่าง ๆ ที่ Power BI ไม่สามารถเปิดได้ 

## <a name="resolve-issues-with-opening-encrypted-pbix-files"></a>แก้ไขปัญหาเกี่ยวกับการเปิดไฟล์ PBIX ที่เข้ารหัสลับ

คุณไม่สามารถเปิดไฟล์ PBIX ที่เข้ารหัสลับโดยใช้เวอร์ชัน Power BI Desktop ที่ไม่สนับสนุนการปกป้องข้อมูล

หากคุณต้องการใช้ Power BI Desktop ต่อไป ความละเอียดที่แนะนำคือการอัปเดตเป็นเวอร์ชันที่รองรับการปกป้องข้อมูล คุณสามารถดาวน์โหลด [Power BI Desktop เวอร์ชันล่าสุด](https://www.microsoft.com/download/confirmation.aspx?id=58494) (ลิงก์นี้เป็นลิงก์ดาวน์โหลดโดยตรงไปยังโปรแกรมปฏิบัติการติดตั้ง) เวอร์ชันล่าสุดของ Power BI Desktop สนับสนุนการปกป้องข้อมูลและสามารถถอดรหัสและเปิดไฟล์ .PBIX ที่เข้ารหัสลับใด ๆ ได้

###

## <a name="resolve-issues-with-the-on-premises-data-gateway-and-power-bi-desktop"></a>แก้ไขปัญหาด้วยเกตเวย์ข้อมูลในองค์กรและ Power BI Desktop

ใน Power BI Desktop, ผู้ใช้ที่ติดตั้งและใช้งานเวอร์ชั่นก่อนหน้านี้ของ *บริเวณทางเข้าออกข้อมูลของ Power BI* ที่สามารถถูกปิดกั้นจากการเปิด Power BI Desktop เนื่องจากข้อห้ามนโยบายการบริหารที่บริเวณทางเข้าออกข้อมูลของ Power BI ตั้งอยู่ที่การประมวลคำสั่งในเครื่อง

คุณมีสามตัวเลือกในการแก้ไขปัญหาที่เกี่ยวกับบริเวณทางเข้าออกข้อมูล และเปิดใช้งาน Power BI Desktop เพื่อเปิด:

### <a name="resolution-1-install-the-latest-version-of-power-bi-on-premises-data-gateway"></a>การแก้ปัญหาที่ 1: ติดตั้งเกตเวย์ข้อมูลภายในองค์กร Power BI เวอร์ชันล่าสุด

เวอร์ชั่นล่าสุดของบริเวณทางเข้าออกข้อมูลของ Power BI ไม่ได้ตั้งอยู่ที่ข้อจำกัดการประมวลคำสั่งในเครื่อง และอนุญาตให้ Power BI Desktop เปิดได้ หากคุณต้องการใช้บริเวณทางเข้าออกข้อมูลของ Power BI ต่อ การแก้ไขที่แนะนำคือทำการอัปเดต คุณสามารถดาวน์โหลด [เวอร์ชั่นล่าสุดของ บริเวณทางเข้าออกข้อมูลของ Power BI](https://go.microsoft.com/fwlink/?LinkId=698863) ลิงก์เป็นลิงก์ดาวน์โหลดโดยตรงไปยังคำสั่งติดตั้ง

### <a name="resolution-2-uninstall-or-stop-the-power-bi-on-premises-data-gateway-microsoft-service"></a>การแก้ปัญหาที 2: ถอนการติดตั้งหรือหยุดบริการการใช้บริเวณทางเข้าออกข้อมูลของ Power BI ของ Microsoft

คุณสามารถถอนการติดตั้งการใช้บริเวณทางเข้าออกข้อมูลของ Power BI หากคุณไม่ต้องการใช้มันแล้ว หรือคุณสามารถหยุดบริการการใช้บริเวณทางเข้าออกข้อมูลของ Power BI ของ Microsoft ที่ลบนโยบายข้อจำกัดออกและอนุญาตให้ Power BI Desktop ทำการเปิด

### <a name="resolution-3-run-power-bi-desktop-with-administrator-privilege"></a>การแก้ปัญหาที่ 3: เรียกใช้ Power BI Desktop กับสิทธิ์ผู้ดูแลระบบ

คุณสามารถเปิดใช้งาน Power BI Desktop ได้สมบูรณ์ เช่นเดียวกับผู้ดูแล ที่ยังอนุญาตให้ Power BI Desktop เปิดได้อย่างสมบูรณ์ ยังคงได้รับการแนะนำให้คุณติดตั้งเวอร์ชั่นล่าสุดของ รการใช้บริเวณทางเข้าออกข้อมูลของ Power BI ตามที่อธิบายไว้ก่อนหน้านี้

Power BI Desktop ถูกออกแบบให้เป็นโครงสร้างหลากหลายกระบวนการ และกระบวนการที่หลากหลายนี้ได้สื่อสารการใช้การประมวลคำสั่งของชื่อ Windows อาจมีกระบวนการอื่นที่รบกวนเนมไปป์เหล่านั้น เหตุผลโดยทั่วไปเกือบทั้งหมดสำหรับการแทรกแซงคือความปลอดภัย รวมทั้งเหตุการณ์ที่ซอฟท์แวร์ป้องกันไวรัสหรือไฟร์เออร์วอลส์จะปิดกั้นการประมวลคำสั่งหรือเปลี่ยนการประมวลผลไปยังช่องทางเฉพาะ การเปิด Power BI Desktop ด้วยสิทธิพิเศษของผู้ดูแลอาจจะแก้ไขปัญหานั้นได้ หากคุณไม่สามารถเปิดด้วยสิทธิพิเศษของผู้ดูแล ให้สอบถามไปยังผู้ดูแลของคุณเพื่อกำหนดกฎความปลอดภัยที่ป้องกันการประมวลคำสั่งจากการสื่อสารที่เหมาะสม จากนั้นเพิ่ม Power BI Desktop และกระบวนการย่อย ที่เกี่ยวข้องเพื่ออนุญาตรายการ

## <a name="resolve-issues-when-connecting-to-sql-server"></a>แก้ไขปัญหาเมื่อเชื่อมต่อกับ SQL Server

เมื่อคุณพยามเชื่อมต่อไปยังฐานข้อมูล SQL Server คุณอาจจะผ่านข้อความที่ผิดพลาดที่คล้ายกับข้อความดังต่อไปนี้:

`"An error happened while reading data from the provider:`\
`'Could not load file or assembly 'System.EnterpriseServices, Version=4.0.0.0, Culture=neutral, PublicKeyToken=xxxxxxxxxxxxx' or one of its dependencies.`\
`Either a required impersonation level was not provided, or the provided impersonation level is invalid. (Exception from HRESULT: 0x80070542)'"`

คุณสามารถแก้ไขปัญหาได้บ่อยขึ้นหากคุณเปิด Power BI Desktop แบบผู้ดูแลก่อนที่คุณจะสร้างการเชื่อมต่อ SQL Server

หลังจากคุณเปิด  Power BI Desktop แบบผู้ดูแลและสร้างการเชื่อมต่อ DLLs ที่ต้องการจะถูกลงทะเบียนอย่างเหมาะสม หลังจากนั้น การเปิด Power BI Desktop แบบผู้ดูแลก็ไม่จำเป็นต่อไป ในกรณีที่คุณกำลังเชื่อมต่อกับเซิร์ฟเวอร์ SQL ด้วยข้อมูลประจำตัวของ windows สำรอง คุณจะต้องเปิด Power BI Desktop ในฐานะผู้ดูแลระบบทุกครั้งที่คุณเชื่อมต่อ

## <a name="get-help-with-other-launch-issues"></a>รับการช่วยเหลือจากการแก้ไขปัญหาของผู้อื่น

เราพยามอย่างหนักที่จะครอบคลุมปัญหาให้มากเท่าที่ Power BI Desktop จะทำได้ เราดูปัญหาที่อาจจะมีผลกระทบต่อลูกค้าเป็นประจำ และรวมเอาไว้ในบทความของเรา

หากปัญหากับการเปิด Power BI Desktop ไม่ได้เกี่ยวข้องกับบริเวณทางเข้าออกข้อมูล หรือเมื่อการแก้ไขปัญหาก่อนหน้านี้ใช้ไม่ได้ คุณสามารถส่งการสนับสนุนไปยัง *การสนับสนุน Power BI* (<https://support.powerbi.com>) เพื่อช่วยระบุและแก้ไขปัญหาของคุณ

คุณควรผ่านปัญหาอื่นในอนาคตด้วย Power BI Desktop มันมีประโยชน์ในการเปิดการบันทึกอัตโนมัติและรวมไฟล์ล็อก ไฟล์ล็อกอาจช่วยให้แยกออกและระบุปัญหาได้ เปิดการบันทึกอัตโนมัติ เลือก **ไฟล์** > **ตัวเลือกและการตั้งค่า** > **ตัวเลือก** เลือก **การวินิจฉัย** จากนั้นเลือก **เปิดการบันทึกอัตโนมัติ** Power BI Desktop ต้องใช้งานในการตั้งค่าตัวเลือกนี้ แต่มันมีประโยชน์สำหรับปัญหาในอนาคตที่เกี่ยวกับการเปิดใช้ Power BI Desktop
