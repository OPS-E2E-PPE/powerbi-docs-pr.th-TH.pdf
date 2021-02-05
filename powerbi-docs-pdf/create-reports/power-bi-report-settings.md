---
title: เปลี่ยนการตั้งค่าสำหรับรายงาน Power BI
description: เปลี่ยนการตั้งค่าสำหรับรายงานในบริการของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 10/14/2020
LocalizationGroup: Reports
ms.openlocfilehash: dbb173c65ecfc5d1ca464387ed43ae615cdcbca1
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96396187"
---
# <a name="change-settings-for-power-bi-reports"></a>เปลี่ยนการตั้งค่าสำหรับรายงาน Power BI

[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-desktop](../includes/yes-desktop.md)] [!INCLUDE [yes-service](../includes/yes-service.md)]

ด้วยการตั้งค่ารายงานใน Power BI Desktop และบริการของ Power BI คุณจะสามารถควบคุมวิธีที่ผู้อ่านรายงานโต้ตอบกับรายงานของคุณได้ ตัวอย่างเช่น คุณสามารถอนุญาตให้ผู้ใช้บันทึกตัวกรองสำหรับรายงาน ปรับแต่งการแสดงผลด้วยภาพในรายงาน หรือแสดงหน้ารายงานเป็นแท็บที่อยู่ด้านล่างของรายงานแทนที่จะอยู่ด้านข้าง

:::image type="content" source="media/power-bi-report-settings/service-report-settings-pane.png" alt-text="สกรีนช็อตของบานหน้าต่างการตั้งค่ารายงานในบริการของ Power BI":::

ซึ่งการอ่านบทความเหล่านี้ก่อนอาจเป็นประโยชน์:

- [สร้างรายงานในบริการของ Power BI โดยการนำเข้าชุดข้อมูล](service-report-create-new.md) เพื่อทำความเข้าใจเกี่ยวกับประสบการณ์การสร้างรายงาน
- [รายงานใน Power BI](../consumer/end-user-reports.md) เพื่อทำความเข้าใจเกี่ยวกับประสบการณ์ของผู้อ่านรายงานของคุณ

 มาเริ่มกันเลย!

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

- สำหรับการสร้างรายงานโดยใช้ Power BI Desktop ให้ดู [มุมมองรายงานบนเดสก์ท็อป](desktop-report-view.md)
- [ลงทะเบียนสำหรับบริการของ Power BI](../fundamentals/service-self-service-signup-for-power-bi.md) 
- คุณจำเป็นต้องมีสิทธิ์ในการแก้ไขสำหรับรายงานในบริการของ Power BI โปรดดู [บทบาทในพื้นที่ทำงานใหม่](../collaborate-share/service-new-workspaces.md#roles-in-the-new-workspaces) สำหรับรายละเอียดเกี่ยวกับสิทธิ์
- ถ้าคุณยังไม่มีรายงานในบริการของ Power BI คุณสามารถ [ติดตั้งชุดเนื้อหาตัวอย่าง](sample-datasets.md#install-built-in-content-packs) ที่มีแดชบอร์ด รายงาน และชุดข้อมูลได้

## <a name="open-the-settings-pane-in-power-bi-desktop"></a>เปิดบานหน้าต่างการตั้งค่าใน Power BI Desktop

1. เลือกตัวเลือก **ไฟล์** >  **และตัวเลือก** > **การตั้งค่า**
1. ภายใต้ **ไฟล์ปัจจุบัน** เลือก **การตั้งค่ารายงาน**

    :::image type="content" source="media/power-bi-report-settings/desktop-report-settings-pane.png" alt-text="สกรีนช็อตของบานหน้าต่างการตั้งค่ารายงานใน Power BI Desktop":::

    ส่วนที่เหลือของบทความนี้จะเรียกใช้การตั้งค่ารายงานเฉพาะบางรายการ

## <a name="open-the-settings-pane-in-the-power-bi-service"></a>เปิดบานหน้าต่างการตั้งค่าในบริการของ Power BI

1. ในมุมมองการอ่านรายงาน เลือก **ไฟล์** > **การตั้งค่า**

    :::image type="content" source="media/power-bi-report-settings/service-report-file-settings.png" alt-text="สกรีนช็อตของเมนูไฟล์ไปยังการตั้งค่า":::

1. ในบานหน้าต่าง **การตั้งค่า** คุณจะเห็นจำนวนการสลับที่คุณสามารถตั้งค่าได้เพียงสำหรับรายงานนี้ ส่วนที่เหลือของบทความนี้จะเรียกใช้การตั้งค่ารายงานเฉพาะบางรายการ

## <a name="set-featured-content"></a>กำหนดเนื้อหาเด่น

คุณสามารถแสดงแดชบอร์ด รายงาน และแอปเพื่อให้ปรากฏในส่วนที่แนะนำของหน้าแรกของ Power BI ของเพื่อนร่วมงานของคุณ อ่านเพิ่มเติมเกี่ยวกับ [วิธีการกำหนดคุณลักษณะของเนื้อหา](../collaborate-share/service-featured-content.md)

## <a name="set-the-pages-pane"></a>ตั้งค่าบานหน้าต่างของหน้า

ในขณะนี้ คุณสามารถเปลี่ยนการตั้งค่าบานหน้าต่างของหน้าในบริการของ Power BI เท่านั้น เมื่อคุณสลับเปิด **บานหน้าต่างของหน้า** ผู้อ่านรายงานจะมองเห็นแท็บหน้ารายงานตามด้านล่างของรายงานในมุมมองการอ่านแทนที่จะอยู่ด้านข้าง ในมุมมองแก้ไข แท็บหน้ารายงานจะมีอยู่แล้วตามด้านล่างของรายงาน

:::image type="content" source="media/power-bi-report-settings/report-settings-pages-pane.png" alt-text="สกรีนช็อตของการตั้งค่าบานหน้าต่างของหน้า":::

## <a name="control-filters"></a>ควบคุมตัวกรอง

บานหน้าต่าง **การตั้งค่า** รายงานมีการตั้งค่าสามรายการ สำหรับควบคุมการโต้ตอบของผู้อ่านที่ทำกับตัวกรองในรายงานของคุณ ลิงก์ต่อไปนี้ไปที่บทความ [่ตัวกรองการออกแบบในรายงาน Power BI](power-bi-report-filter.md) สำหรับรายละเอียดเกี่ยวกับการตั้งค่าแต่ละรายการ

- **ตัวกรองแบบถาวร** อนุญาตให้ผู้อ่าน [บันทึกตัวกรองบนรายงาน](power-bi-report-filter.md#allow-saving-filters)
- **ประสบการณ์การกรอง** มีการตั้งค่าเพิ่มเติมสองรายการ:
    
    อนุญาตให้ผู้อ่านรายงาน [เปลี่ยนชนิดตัวกรอง](power-bi-report-filter.md#restrict-changes-to-filter-type)

    เปิดใช้งาน [ค้นหาในบานหน้าต่างตัวกรอง](power-bi-report-filter.md#filters-pane-search)

## <a name="export-data"></a>ส่งออกข้อมูล

ตามค่าเริ่มต้น [ผู้อ่านรายงานสามารถส่งออกข้อมูลสรุปหรือข้อมูลเบื้องต้น](../consumer/end-user-export.md) จากการแสดงผลด้วยภาพในรายงานของคุณได้ ด้วย **ส่งออกข้อมูล** คุณสามารถอนุญาตให้ผู้ใช้สามารถส่งออกข้อมูลสรุปได้เท่านั้น หรือไม่ส่งออกข้อมูลใด ๆ เลยจากรายงานของคุณ

## <a name="personalize-visuals"></a>ปรับแต่งการแสดงผลด้วยภาพ

อนุญาตให้ผู้อ่านของคุณเปลี่ยนและปรับแต่งการแสดงผลด้วยภาพในรายงานของคุณ อ่านเพิ่มเติมเกี่ยวกับ [อนุญาตให้ผู้อ่านรายงานปรับแต่งการแสดงผลด้วยภาพ](power-bi-personalize-visuals.md)

## <a name="next-steps"></a>ขั้นตอนถัดไป

* [กำหนดคุณลักษณะของเนื้อหาบนหน้าแรกของบุคคลอื่น](../collaborate-share/service-featured-content.md)
* [อนุญาตให้ผู้อ่านรายงานปรับแต่งการแสดงผลด้วยภาพในรายงาน](power-bi-personalize-visuals.md)
* มีคำถามเพิ่มเติมหรือไม่ [ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)
