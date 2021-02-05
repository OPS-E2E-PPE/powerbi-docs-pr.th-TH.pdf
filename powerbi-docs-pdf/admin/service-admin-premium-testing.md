---
title: Purchase Power BI Premium สำหรับการทดสอบ
description: เรียนรู้วิธีที่คุณสามารถซื้อ Power BI Premium สำหรับการทดสอบและวัตถุประสงค์อื่น ๆ
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-premium
ms.topic: how-to
ms.date: 01/28/2021
LocalizationGroup: Premium
ms.openlocfilehash: 9e0cd283728afad43ddf37f765b1fda66c300270
ms.sourcegitcommit: 7ed995eed0fd6e718748accf87bae384211cd95d
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2021
ms.locfileid: "99043424"
---
# <a name="purchase-power-bi-premium-for-testing"></a>Purchase Power BI Premium สำหรับการทดสอบ

บทความนี้อธิบายถึงวิธีการซื้อ Power BI Premium A SKU สำหรับสถานการณ์การทดสอบ และกรณีที่คุณไม่มีสิทธิ์ที่จำเป็นในการซื้อ P SKU (บทบาทผู้ดูแลระบบส่วนกลาง Microsoft 365 หรือบทบาทผู้ดูแลระบบการเรียกเก็บเงิน) A SKU ไม่จำเป็นต้องมีข้อผูกมัดเวลา และเรียกเก็บเงินเป็นรายชั่วโมง คุณซื้อ A SKU ใน [พอร์ทัล Azure](https://portal.azure.com)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI Premium ดูที่ [Power BI Premium คืออะไร](service-premium-what-is.md) สำหรับข้อมูลการกำหนดราคาและการวางแผนปัจจุบันให้ดู[หน้าราคา POWER BI](https://powerbi.microsoft.com/pricing/) ผู้เขียนเนื้อหาจะยังคงจำเป็นต้องมี [สิทธิ์การใช้งาน Power BI Pro](service-admin-purchasing-power-bi-pro.md) แม้ว่าองค์กรของคุณจะใช้ Power BI Premium ก็ตาม ตรวจสอบให้แน่ใจว่าคุณซื้อสิทธิ์การใช้งาน Power BI Pro อย่างน้อยหนึ่งใบสำหรับองค์กรของคุณ เมื่อใช้ A SKU _ผู้ใช้ทั้งหมด_ ที่ใช้เนื้อหายังจำเป็นต้องมีสิทธิการใช้งาน Pro

> [!NOTE]
> ถ้าการสมัครใช้งานระดับ Premium หมดอายุ คุณมีเวลา 30 วันของการเข้าถึงความจุแบบเต็มของคุณ หลังจากนั้น เนื้อหาของคุณจะเปลี่ยนเป็นความจุที่ใช้ร่วมกัน แบบจำลองที่มีความจุมากกว่า 1 GB ไม่ได้รับการรับรองในความจุที่ใช้ร่วมกัน

## <a name="purchase-a-skus-for-testing-and-other-scenarios"></a>ซื้อ A SKU สำหรับการทดสอบและสถานการณ์อื่นๆ

มีการทำให้ A SKU พร้อมใช้งานผ่านทางบริการ Azure Power BI Embedded คุณสามารถใช้ A SKU ในวิธีการต่อไปนี้:

- เปิดใช้งานการฝังของ Power BI ในแอปพลิเคชันของบุคคลที่สาม สำหรับข้อมูลเพิ่มเติม ให้ดู [Power BI Embedded](../developer/embedded/azure-pbie-what-is-power-bi-embedded.md)

- ทดสอบฟังก์ชัน Premium ก่อนที่คุณจะซื้อ P SKU

- สร้างสภาพแวดล้อมการพัฒนาและการทดสอบควบคู่ไปกับสภาพแวดล้อมการผลิตที่ใช้ P SKU

- ซื้อ Power BI Premium แม้ว่าคุณจะไม่ใช่บทบาทผู้ดูแลระบบส่วนกลาง Microsoft 365 หรือบทบาทผู้ดูแลระบบการเรียกเก็บเงิน

> [!NOTE]
> ถ้าคุณซื้อ SKU ขนาด A4 หรือสูงกว่าคุณสามารถใช้ประโยชน์จากคุณลักษณะ Premium ทั้งหมด ยกเว้นการแชร์เนื้อหาได้ไม่จำกัด เมื่อใช้ A SKU _ผู้ใช้ทั้งหมด_ ที่ใช้เนื้อหาจำเป็นต้องมีสิทธิการใช้งาน Pro

ให้ปฏิบัติตามขั้นตอนเหล่านี้เพื่อซื้อ A SKU ในพอร์ทัล Azure

1. ลงชื่อเข้าใช้ [พอร์ทัล Azure](https://portal.azure.com) ด้วยบัญชีที่มีสิทธิ์ระดับผู้ดูแลระบบความจุเป็นอย่างน้อยใน Power BI

1. ค้นหา _Power BI Embedded_ และเลือกบริการในผลลัพธ์การค้นหา

    ![การค้นหาพอร์ทัล Azure](media/service-admin-premium-purchase/azure-portal-search.png)

1. เลือก **สร้าง Power BI Embedded**

    ![สร้าง Power BI Embedded](media/service-admin-premium-purchase/create-power-bi-embedded.png)

1. บนหน้าจอการสร้าง **Power BI Embedded** ให้ระบุข้อมูลต่อไปนี้:

    - **การสมัครรับข่าวสาร** ในการสร้างบริการ Power BI Embedded

    - **ตำแหน่งที่ตั้ง** ทางกายภาพ ในการสร้างกลุ่มทรัพยากรที่ประกอบด้วยบริการ เพื่อประสิทธิภาพที่ดีกว่า ตำแหน่งที่ตั้งนี้ควรอยู่ใกล้เคียงกับตำแหน่งที่ตั้งของผู้เช่า Azure Active Directory ของคุณสำหรับ Power BI

    - **กลุ่มทรัพยากร** ที่มีอยู่ ในการใช้หรือสร้างใหม่ตามที่แสดงในตัวอย่าง

    - **ผู้ดูแลระบบความจุ Power BI** ผู้ดูแลระบบความจุต้องเป็นผู้ใช้ที่เป็นสมาชิกหรือโครงร่างสำคัญของบริการในผู้เช่า Azure AD ของคุณ

    ![การสมัครรับข่าวสารและกลุ่มทรัพยากร](media/service-admin-premium-purchase/subscription-resource-group.png)

1. ถ้าคุณต้องการใช้คุณลักษณะทั้งหมดของ Power BI Premium (ยกเว้นการแชร์ที่ไม่จำกัด) คุณจำเป็นต้องมี A4 SKU เป็นอย่างน้อย เลือก **เปลี่ยนขนาด**

    ![เปลี่ยนขนาดความจุ](media/service-admin-premium-purchase/change-capacity-size.png)

1. เลือกขนาดความจุ A4, A5 หรือ A6 ซึ่งสอดคล้องกับ P1, P2 และ P3

    ![เลือกความจุ A3](media/service-admin-premium-purchase/select-a3-capacity.png)

1. เลือก **รีวิว + สร้าง** ตรวจทานตัวเลือกที่คุณเลืกอ จากนั้นเลือก **สร้าง**

    ![สร้างทรัพยากร](media/service-admin-premium-purchase/create-resource.png)

1. อาจใช้เวลาสองถึงสามนาทีเพื่อให้การปรับใช้เสร็จสมบูรณ์ เมื่อพร้อมแล้วให้เลือก **ไปที่ทรัพยากร**

    ![การปรับใช้เสร็จสมบูรณ์](media/service-admin-premium-purchase/deployment-complete.png)

1. บนหน้าจอการจัดการ ตรวจทานตัวเลือกที่คุณมีสำหรับการจัดการบริการ รวมถึงการหยุดบริการเมื่อคุณไม่ได้ใช้งาน

    ![จัดการความจุ](media/service-admin-premium-purchase/manage-capacity.png)

หลังจากที่คุณซื้อความจุ ให้เรียนรู้วิธีการ [จัดการความจุ](service-admin-premium-manage.md#manage-capacity) และ [มอบหมายพื้นที่ทำงาน](service-admin-premium-manage.md#assign-a-workspace-to-a-capacity) ให้กับความจุ

## <a name="next-steps"></a>ขั้นตอนถัดไป

[Power BI Premium คืออะไร](service-premium-what-is.md)
[วิธีการซื้อ Power BI Premium](service-admin-premium-purchase.md)
[กำหนดค่าและจัดการความจุใน Power BI Premium](service-admin-premium-manage.md)\
[หน้าการกำหนดราคา Power BI](https://powerbi.microsoft.com/pricing/)\
[คำถามที่ถามบ่อยสำหรับ Power BI Premium](service-premium-faq.md)\
[เอกสารทางเทคนิคเรื่องการวางแผนการใช้ Power BI สำหรับองค์กร](https://aka.ms/pbienterprisedeploy)

มีคำถามเพิ่มเติมหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)
