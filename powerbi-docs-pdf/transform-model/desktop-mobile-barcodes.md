---
title: แท็กเขตข้อมูลบาร์โค้ดใน Power BI Desktop เพื่อเปิดใช้งานการกรองบาร์โค้ดในแอปสำหรับอุปกรณ์เคลื่อนที่
description: เมื่อคุณแท็กเขตข้อมูลบาร์โค้ดในแบบจำลองของคุณใน Power BI Desktop ผู้ใช้แอปสำหรับอุปกรณ์เคลื่อนที่สามารถสแกนบาร์โค้ดเพื่อรับข้อมูลที่กรองบนโทรศัพท์ iOS และ Android และแท็บเล็ตของพวกเขา
author: paulinbar
ms.author: painbar
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: how-to
ms.date: 01/20/2021
LocalizationGroup: Model your data
ms.openlocfilehash: 4674347d3acd6520d7d156a7d1634a13df611afe
ms.sourcegitcommit: f7330dabb9cd8bce90bb2efec3e3273a11578f10
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2021
ms.locfileid: "99494429"
---
# <a name="tag-barcode-fields-in-power-bi-desktop-to-enable-barcode-scan-filtering-in-the-mobile-apps"></a>แท็กเขตข้อมูลบาร์โค้ดใน Power BI Desktop เพื่อเปิดใช้งานการกรองบาร์โค้ดในแอปสำหรับอุปกรณ์เคลื่อนที่

ใน Power BI Desktop คุณสามารถ [จัดประเภทข้อมูล](desktop-data-categorization.md) ในคอลัมน์ ดังนั้น Power BI Desktop จึงทราบวิธีการนำค่ามาใช้ในการแสดงผลด้วยภาพในรายงานได้ นอกจากนี้ คุณยังสามารถจัดประเภทคอลัมน์เป็น **บาร์โค้ด** ได้ จากนั้นเมื่อมีคนในบริษัทหรือองค์กรของคุณ [สแกนบาร์โค้ด](../consumer/mobile/mobile-apps-scan-barcode-iphone.md) บนผลิตภัณฑ์โดยใช้แอป Power BI สำหรับอุปกรณ์เคลื่อนที่บนอุปกรณ์ IOS หรือ Android หรือแท็บเล็ตของพวกเขาจะเห็นรายงานใดๆที่มีบาร์โค้ดนั้น เมื่อพวกเขาเปิดรายงานจะมีการกรองโดยอัตโนมัติไปยังข้อมูลที่เกี่ยวข้องกับบาร์โค้ดนั้น

## <a name="categorize-barcode-data"></a>จัดประเภทข้อมูลบาร์โค้ด

สมมติว่าคุณมีรายงานที่มีบาร์โค้ด: 

1. ใน Power BI Desktop ให้สลับไปยังมุมมองข้อมูล
2. เลือกคอลัมน์ที่มีข้อมูลบาร์โค้ด ดูรายการของ [รูปแบบบาร์โค้ดที่สนับสนุน](#supported-barcode-formats) ด้านล่าง
3. บนแท็บ **เครื่องมือคอลัมน์** เลือก  >  **บาร์โค้ด** ประเภทข้อมูล
   
    ![รายการประเภทข้อมูล](media/desktop-mobile-barcodes/power-bi-desktop-barcode.png)

    >[!WARNING]
    >อย่าจัดประเภทมากกว่าหนึ่งคอลัมน์ในตารางข้อมูลทั้งหมดในรายงานเป็น **บาร์โค้ด** แอปสำหรับอุปกรณ์เคลื่อนที่สนับสนุนการกรองบาร์โค้ดเฉพาะสำหรับรายงานที่มีคอลัมน์บาร์โค้ดเดียวเท่านั้นในตารางข้อมูลรายงานทั้งหมด ถ้ารายงานมีมากกว่าหนึ่งคอลัมน์บาร์โค้ดไม่มีการกรองที่เกิดขึ้น

4. ในมุมมองรายงานเพิ่มเขตข้อมูลบาร์โค้ดไปยังวิชวลที่คุณต้องการกรองด้วยบาร์โค้ด
5. บันทึกรายงานและเผยแพร่ไปยังบริการ Power BI

ตอนนี้เมื่อคุณเปิดสแกนเนอร์บนแอป Power BI สำหรับ iOS และ Android โทรศัพท์และแท็บเล็ตและสแกนบาร์โค้ดคุณจะเห็นรายงานนี้ในรายการของรายงานที่มีบาร์โค้ด เมื่อคุณเปิดรายงานภาพจะถูกกรองด้วยบาร์โค้ดของผลิตภัณฑ์ที่คุณสแกน

## <a name="supported-barcode-formats"></a>รูปแบบบาร์โค้ดที่สนับสนุน
เหล่านี้คือรูปแบบบาร์โค้ด Power BI รู้ว่าคุณสามารถแท็กได้ในรายงาน Power BI: 

* UPCECode 
* Code39Code  
* A39Mod43Code 
* EAN13Code 
* EAN8Code  
* 93Code  
* 128Code 
* PDF417Code 
* Interleaved2of5Code 
* ITF14Code 

## <a name="next-steps"></a>ขั้นตอนถัดไป
* [สแกนบาร์โค้ดจากแอป Power BI บนโทรศัพท์ iOS หรือ Android แท็บเล็ตของคุณ](../consumer/mobile/mobile-apps-scan-barcode-iphone.md)
* [ปัญหาเกี่ยวกับการสแกนบาร์โค้ด](../consumer/mobile/mobile-apps-scan-barcode-iphone.md#issues-with-scanning-a-barcode)
* [การจัดประเภทข้อมูลใน Power BI Desktop](desktop-data-categorization.md)  
* มีคำถามหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)
