---
title: วิธีการซื้อ Power BI Premium
description: เรียนรู้วิธีการซื้อ Power BI Premium และเปิดใช้งานการเข้าถึงเนื้อหาให้ทั้งองค์กรของคุณ
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-premium
ms.topic: how-to
ms.date: 01/28/2021
LocalizationGroup: Premium
ms.openlocfilehash: c4e50f7fa0c8f3313b3e7e58001ae33d8c327d85
ms.sourcegitcommit: 7ed995eed0fd6e718748accf87bae384211cd95d
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2021
ms.locfileid: "99043148"
---
# <a name="how-to-purchase-power-bi-premium"></a>วิธีการซื้อ Power BI Premium

บทความนี้อธิบายวิธีการซื้อความจุของ Power BI Premium สำหรับองค์กรของคุณ บทความนี้ครอบคลุมสถานการณ์ต่อไปนี้:

- การใช้ P SKU สำหรับสถานการณ์การผลิตทั่วไป P SKU กำหนดให้มีข้อผูกมัดรายเดือนหรือรายปี และจะเรียกเก็บเงินเป็นรายเดือน

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI Premium ดูที่ [Power BI Premium คืออะไร](service-premium-what-is.md) สำหรับข้อมูลการกำหนดราคาและการวางแผนปัจจุบันให้ดู[หน้าราคา POWER BI](https://powerbi.microsoft.com/pricing/) ผู้เขียนเนื้อหาจะยังคงจำเป็นต้องมี [สิทธิ์การใช้งาน Power BI Pro](service-admin-purchasing-power-bi-pro.md) แม้ว่าองค์กรของคุณจะใช้ Power BI Premium ก็ตาม ตรวจสอบให้แน่ใจว่าคุณซื้อสิทธิ์การใช้งาน Power BI Pro อย่างน้อยหนึ่งใบสำหรับองค์กรของคุณ เมื่อใช้ A SKU _ผู้ใช้ทั้งหมด_ ที่ใช้เนื้อหายังจำเป็นต้องมีสิทธิการใช้งาน Pro

> [!NOTE]
> ถ้าการสมัครใช้งานระดับ Premium หมดอายุ คุณมีเวลา 30 วันของการเข้าถึงความจุแบบเต็มของคุณ หลังจากนั้น เนื้อหาของคุณจะเปลี่ยนเป็นความจุที่ใช้ร่วมกัน แบบจำลองที่มีความจุมากกว่า 1 GB ไม่ได้รับการรับรองในความจุที่ใช้ร่วมกัน

> [!NOTE]
> Power BI Premium เพิ่งเปิดตัว Premium เวอร์ชันใหม่ชื่อ **Premium Gen2** ซึ่งกำลังอยู่ในช่วงการแสดงตัวอย่าง Premium Gen2 จะทำให้การจัดการความจุระดับพรีเมียมง่ายขึ้นและลดค่าใช้จ่ายในการจัดการ สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Power BI Premium Generation 2 (ตัวอย่าง)](service-premium-what-is.md#power-bi-premium-generation-2-preview)

## <a name="purchase-p-skus-for-typical-production-scenarios"></a>ซื้อ P SKU สำหรับสถานการณ์การผลิตทั่วไป

คุณสามารถสร้างผู้เช่าใหม่ด้วย Power BI Premium ที่กำหนดค่า SKU หรือคุณสามารถซื้อความจุ Power BI Premium สำหรับองค์กรที่มีอยู่ได้ ในทั้งสองกรณี คุณสามารถเพิ่มความจุได้หากคุณต้องการ

### <a name="create-a-new-tenant-with-power-bi-premium-p1"></a>สร้างลูกค้าใหม่ด้วย Power BI Premium P1

ถ้าคุณไม่มีผู้เช่าและต้องการสร้างหนึ่งรายการ คุณสามารถซื้อ Power BI Premium ได้ในเวลาเดียวกัน ลิงก์ต่อไปนี้จะนำคุณไปสู่กระบวนการสร้างผู้เช่ารายใหม่และช่วยให้คุณสามารถซื้อ Power BI Premium: [ข้อเสนอ Power BI Premium P1](https://signup.microsoft.com/Signup?OfferId=b3ec5615-cc11-48de-967d-8d79f7cb0af1) เมื่อคุณสร้างผู้เช่า คุณจะได้รับมอบหมายให้ทำหน้าที่เป็นผู้ดูแลระบบส่วนกลางของ Microsoft 365 โดยอัตโนมัติสำหรับผู้เช่ารายนั้น

หลังจากที่คุณซื้อความจุ ให้เรียนรู้วิธีการ [จัดการความจุ](service-admin-premium-manage.md#manage-capacity) และ [มอบหมายพื้นที่ทำงาน](service-admin-premium-manage.md#assign-a-workspace-to-a-capacity) ให้กับความจุ

### <a name="purchase-a-power-bi-premium-capacity-for-an-existing-organization"></a>ซื้อความจุ Power BI Premium สำหรับองค์กรที่มีอยู่

ถ้าคุณมีองค์กรที่มีอยู่แล้ว (ผู้เช่า) คุณต้องอยู่ในบทบาทผู้ดูแลระบบส่วนกลางของ Microsoft 365 หรือบทบาทของผู้ดูแลระบบการเรียกเก็บเงินเพื่อซื้อการสมัครรับข้อมูลและสิทธิ์การใช้งาน สำหรับข้อมูลเพิ่มเติม ให้ดู[เกี่ยวกับบทบาทผู้ดูแลระบบ Microsoft 365](https://support.office.com/article/About-Office-365-admin-roles-da585eea-f576-4f55-a1e0-87090b6aaa9d)

เมื่อต้องการซื้อความจุระดับพรีเมี่ยม ให้ทำตามขั้นตอนต่อไปนี้

1. จากภายใน Power BI service เลือกตัวเลือกแอป Microsoft 365 จากนั้นเลือก **ผู้ดูแลระบบ**

    ![ตัวเลือกแอป Microsoft 365](media/service-admin-premium-purchase/o365-app-picker.png)

    อีกวิธีหนึ่งคือ คุณสามารถเรียกดูศูนย์การจัดการ Microsoft 365

1. เลือก **การเรียกเก็บเงิน** > **ซื้อบริการ**

1. ภายใต้ **แผนอื่น ๆ** ค้นหาข้อเสนอของ Power BI Premium ซึ่งจะแสดงรายการเป็น P1 ผ่าน P3, EM3 และ P1 (แบบรายเดือน)

1. วางเคอร์เซอร์เหนือ จุดไข่ปลา ( **. . .** )แล้ว เลือก **ซื้อทันที**

    ![ซื้อเดี๋ยวนี้](media/service-admin-premium-purchase/premium-purchase.png)

1. ทำตามขั้นตอนเพื่อทำการซื้อให้เสร็จสมบูรณ์

หลังจากที่คุณเสร็จสิ้นการซื้อ **หน้าจอบริการการซื้อ** จะแสดงว่ารายการนั้นถูกซื้อและใช้งานได้

![ซื้อ Power BI Premium](media/service-admin-premium-purchase/premium-purchased.png)

หลังจากที่คุณซื้อความจุ ให้เรียนรู้วิธีการ [จัดการความจุ](service-admin-premium-manage.md#manage-capacity) และ [มอบหมายพื้นที่ทำงาน](service-admin-premium-manage.md#assign-a-workspace-to-a-capacity) ให้กับความจุ

### <a name="purchase-additional-capacities"></a>ซื้อความจุเพิ่มเติม

ขณะนี้คุณมีความจุแล้ว คุณสามารถเพิ่มความจุได้ตามที่คุณต้องการ คุณสามารถผสม Premium capacity SKUs (P1 ผ่าน P3) ภายในองค์กรของคุณได้ SKU ที่ต่างกันมีความสามารถด้านทรัพยากรที่แตกต่างกัน

1. ในศูนย์การจัดการ Microsoft 365 เลือก **การเรียกเก็บเงิน** > **ซื้อบริการ**

1. ค้นหารายการ Power BI Premium ที่คุณต้องการซื้อหนึ่งภายใต้ **แผนอื่นๆ**

1. วางเมาส์เหนือ **ตัวเลือกเพิ่มเติม** (...) แล้วเลือก **เปลี่ยนจำนวนสิทธิ์การใช้งาน**

    ![เปลี่ยนจำนวนสิทธิ์การใช้งาน](media/service-admin-premium-purchase/premium-purchase-more.png)

1. เปลี่ยนจำนวนของอินสแตนซ์ที่คุณต้องการสำหรับรายการนี้ แล้ว เลือก **ส่ง** เมื่อทำเสร็จแล้ว

   > [!IMPORTANT]
   > การเลือก **ส่ง** จะเรียกเก็บเงินจากบัตรเครดิตในไฟล์

หน้า **ซื้อบริการ** จะบ่งชี้ถึงจำนวนของอินสแตนซ์ที่คุณมี ภายในพอร์ทัลผู้ดูแล Power BI ภายใต้ **ตั้งค่าความจุ** แกน v ที่พร้อมใช้งานสะท้อนถึงความจุที่ซื้อใหม่

![แกน v ใช้งานได้สำหรับความจุ Power BI Premium](media/service-admin-premium-purchase/premium-capacities.png)

### <a name="cancel-your-subscription"></a>ยกเลิกการสมัครใช้งาน

คุณสามารถยกเลิกการสมัครใช้งานจากภายในศูนย์การจัดการ Microsoft 365 เพื่อยกเลิกการสมัครใช้งาน Premium ให้ทำสิ่งต่อไปนี้

1. ค้นหาศูนย์การจัดการ Microsoft 365

1. เลือก **การเรียกเก็บเงิน** > **การสมัครใช้งาน**

1. เลือกการสมัครใช้งาน Power BI Premium จากรายการ

1. เลือก **การดำเนินการเพิ่มเติม** > **ยกเลิกการสมัครใช้งาน**

1. หน้า **ยกเลิกการสมัครใช้งาน** จะระบุว่าที่คุณเป็นผู้รับผิดชอบสำหรับ [ค่าธรรมเนียมการหยุดใช้งานก่อน](https://support.office.com/article/early-termination-fees-6487d4de-401a-466f-8bc3-c0beb5cc40d3)หรือไม่ เพจนี้จะยังแจ้งให้คุณทราบเมื่อข้อมูลจะถูกลบเพื่อสมัครใช้งาน

1. อ่านผ่านข้อมูล และถ้าคุณต้องการดำเนินการ ให้เลือก **ยกเลิกการสมัครใช้งาน**

#### <a name="when-canceling-or-your-license-expires"></a>เมื่อยกเลิกหรือสิทธิ์การใช้งานของคุณหมดอายุ

เมื่อยกเลิกการสมัครใช้งานแบบพรีเมียม หรือสิทธิ์การใช้งานความจุของคุณหมดอายุ คุณยังสามารถเข้าถึงความจุพรีเมียมของคุณได้เป็นระยะเวลา 30 วันนับจากวันที่ยกเลิกหรือหมดอายุสิทธิ์การใช้งาน หลังจาก 30 วัน คุณจะไม่สามารถเข้าถึงความจุพรีเมียมหรือพื้นที่ทำงานภายในความจุดังกล่าวได้อีกต่อไป

## <a name="purchase-a-skus-for-testing-and-other-scenarios"></a>ซื้อ A SKU สำหรับการทดสอบและสถานการณ์อื่นๆ

คุณยังสามารถซื้อ SKU สำหรับการทดสอบและสถานการณ์อื่น ๆ ซึ่งให้ความจุแบบ Premium เป็นรายชั่วโมง สำหรับข้อมูลและขั้นตอนเพิ่มเติม โปรดดู[ซื้อ Power BI Premium สำหรับการทดสอบ](service-admin-premium-testing.md)

## <a name="next-steps"></a>ขั้นตอนถัดไป

[กำหนดค่าและจัดการความจุใน Power BI Premium](service-admin-premium-manage.md)\
[หน้าการกำหนดราคา Power BI](https://powerbi.microsoft.com/pricing/)\
[คำถามที่ถามบ่อยสำหรับ Power BI Premium](service-premium-faq.md)\
[เอกสารทางเทคนิคเรื่องการวางแผนการใช้ Power BI สำหรับองค์กร](https://aka.ms/pbienterprisedeploy)

มีคำถามเพิ่มเติมหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)

Power BI ได้แนะนำ Power BI Premium Gen2 เข้ามาใช้งานเป็นข้อเสนอการแสดงตัวอย่าง ซึ่งปรับปรุงประสบการณ์การใช้งาน Power BI Premium ด้วยการปรับปรุงในสิ่งต่อไปนี้:
* ประสิทธิภาพการทำงาน
* สิทธิการใช้งานต่อผู้ใช้
* ขนาดใหญ่ขึ้น
* เมตริกที่ดีขึ้น
* การปรับขนาดอัตโนมัติ
* ลดค่าใช้จ่ายในการจัดการ

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI Premium Gen2 โปรดดูที่ [Power BI Premium Generation 2 (ตัวอย่าง)](service-premium-what-is.md#power-bi-premium-generation-2-preview)