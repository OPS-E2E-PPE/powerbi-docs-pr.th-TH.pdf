---
title: รับการแจ้งเตือนในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่
description: ศูนย์การแจ้งเตือนรวบรวมข้อมูล Power BI ของคุณที่เกี่ยวข้อง และส่งข้อมูลนั้นไปยังอุปกรณ์เคลื่อนที่ของคุณ
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 03/11/2020
ms.openlocfilehash: 19cda3734ba56a5879dc10041d2ba9e9bdc4146e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414748"
---
# <a name="get-notifications-in-the-power-bi-mobile-apps"></a>รับการแจ้งเตือนในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่
นำไปใช้กับ:

| ![iPhone](./media/mobile-apps-notification-center/iphone-logo-50-px.png) | ![iPad](./media/mobile-apps-notification-center/ipad-logo-50-px.png) | ![โทรศัพท์ Android](./media/mobile-apps-notification-center/android-phone-logo-50-px.png) | ![แท็บเล็ต Android](./media/mobile-apps-notification-center/android-tablet-logo-50-px.png) | ![Windows 10](./media/mobile-apps-notification-center/win-10-logo-50-px.png) |
|:--- |:--- |:--- |:--- |:--- |
| iPhone |iPad |โทรศัพท์ Android |แท็บเล็ต Android |อุปกรณ์ Windows 10 |

>[!NOTE]
>การสนับสนุนแอปอุปกรณ์เคลื่อนที่ Power BI สำหรับ **โทรศัพท์ที่ใช้ Windows 10 Mobile** จะถูกยกเลิกในวันที่ 16 มีนาคม 2021 [ศึกษาเพิ่มเติม](/legal/powerbi/powerbi-mobile/power-bi-mobile-app-end-of-support-for-windows-phones)

การแจ้งเตือนจะนำข้อมูลที่เกี่ยวข้องกับประสบการณ์ Power BI ให้คุณ ในบริการของ Power BI หรือบนอุปกรณ์เคลื่อนที่ของคุณ เมื่อคุณเปิดการแจ้งเตือน คุณจะเห็นตัวดึงข้อมูลเรียงเป็นลำดับเกี่ยวกับ[การแจ้งเตือนที่คุณได้ตั้งค่า](mobile-set-data-alerts-in-the-mobile-apps.md)แดชบอร์ดใหม่ที่มีการแชร์กับคุณ การเปลี่ยนแปลงพื้นที่การทำงานกลุ่มของคุณ รายละเอียดเกี่ยวกับเหตุการณ์ใน Power BI และการประชุม และอื่นๆ

> [!NOTE]
> บนอุปกรณ์ iOS ในครั้งแรกที่คุณลงชื่อเข้าใช้[ปรับปรุงเวอร์ชันของแอป Power BI](https://powerbi.microsoft.com/mobile/)คุณจะเห็นข้อความถามว่า คุณต้องการให้ Power BI ส่งการแจ้งเตือนหรือไม่ คุณยังสามารถกำหนดวิธีที่ี Power BI จะแจ้งเตือนคุณใน **ตั้งค่า** สำหรับอุปกรณ์ของคุณ 
> 
> 

## <a name="view-notifications-on-your-mobile-device"></a>ดูการแจ้งเตือนบนอุปกรณ์เคลื่อนที่ของคุณ
1. เมื่อคุณได้รับการแจ้งเตือนบนอุปกรณ์เคลื่อนที่ ค่าเริ่มต้นจะทำให้ Power BI ส่งเสียงและแสดงแบนเนอร์การแจ้งเตือน
   
   ![แบนเนอร์การแจ้งเตือน](./media/mobile-apps-notification-center/power-bi-mobile-notification-banner.png)
   

   คุณสามารถ[เปลี่ยนวิธีที่ Power BI จะแจ้งเตือนคุณ](mobile-apps-notification-center.md#change-or-turn-off-notifications-on-your-mobile-device)ได้
2. ถ้าคุณได้รับการแจ้งเตือนแล้ว เมื่อคุณลงชื่อเข้าใช้ Power BI บนอุปกรณ์เคลื่อนที่ของคุณ คุณจะเห็นจุดสีเหลืองบนไอคอนระฆังการแจ้งเตือน ![ระฆังการแจ้งเตือน](./media/mobile-apps-notification-center/powerbi-alert-tile-notification-icon.png) (iOS และ Android) หรือบนปุ่มนำทางสากล ![จุดการแจ้งเตือน](./media/mobile-apps-notification-center/power-bi-iphone-alert-global-nav-button.png) (อุปกรณ์ Windows 10) 

3. หากต้องการดูการแจ้งเตือนในศูนย์การแจ้งเตือน ให้แตะระฆังการแจ้งเตือน ![ระฆังการแจ้งเตือน](./media/mobile-apps-notification-center/powerbi-alert-tile-notification-icon.png) (iOS และ Android) หรือไอคอนศูนย์การแจ้งเตือน ![ไอคอนการแจ้งเตือน](./media/mobile-apps-notification-center/power-bi-windows-10-notification-icon.png) (อุปกรณ์ Windows 10)
   
    การแจ้งเตือนจะแสดงรายการล่าสุดที่ด้านบนสุด รวมถึงไฮไลท์ข้อความที่ยังไม่ได้อ่าน การแจ้งเตือนจะถูกเก็บไว้เป็น 90 วัน เว้นแต่ว่าคุณลบทิ้งเร็วกว่านั้น หรือเมื่อถึงขีดจำกัดสูงสุดที่ 100 การแจ้งเตือน
   
   ![รายการการแจ้งเตือน iOS](./media/mobile-apps-notification-center/power-bi-iphone-notifications-list.png)
4. หากต้องการยกเลิกการแจ้งเตือนบนอุปกรณ์ iOS และ Android ให้แตะค้างไว้แล้วปัดนิ้ว บนอุปกรณ์ Windows 10 ให้คลิกขวาและเลือก **ปิดเสียงเตือน**

## <a name="change-or-turn-off-notifications-on-your-mobile-device"></a>เปลี่ยน หรือปิดการแจ้งเตือนบนอุปกรณ์เคลื่อนที่ของคุณ
คุณสามารถเปลี่ยนวิธีที่ Power BI แจ้งเตือนคุณได้

1. บนอุปกรณ์ iOS ไปที่ **ตั้งค่า** > **การแจ้งเตือน** 
   
    บนโทรศัพท์ Android ไปที่ **ตั้งค่า** > **การแจ้งเตือน**
   
    บนอุปกรณ์ Windows ใน **ตั้งค่า** ไปยัง **ระบบ** > **การแจ้งเตือนและการดำเนินการ**
2. ในรายการแอป เลือก **Power BI** 
3. ที่นี่คุณสามารถปิดการแจ้งเตือนทั้งหมด หรือเลือกการแจ้งเตือนที่คุณต้องการ
   
    **บน iPhone**
   
    ![สกรีนช็อตแสดงหน้าจอ iPhone ที่ชื่อว่า Power B I ที่คุณสามารถอนุญาตและจัดการการแจ้งเตือนได้](./media/mobile-apps-notification-center/power-bi-notifications-iphone-settings.png)
   
    **บนโทรศัพท์ Android**
   
    ![สกรีนช็อตแสดงหน้าจอ Android ที่ชื่อว่า Power B I ที่คุณสามารถอนุญาตและจัดการการแจ้งเตือนได้](./media/mobile-apps-notification-center/power-bi-notifications-android-settings.png)

    **บนอุปกรณ์ Windows 10**

    ![สกรีนช็อตแสดงหน้าจออุปกรณ์ Windows 10 ที่คุณสามารถอนุญาตและจัดการการแจ้งเตือน Power B I ได้](./media/mobile-apps-notification-center/power-bi-notifications-windows10-settings.png)

## <a name="next-steps"></a>ขั้นตอนถัดไป
* [การแจ้งเตือนข้อมูลในบริการของ Power BI](../../create-reports/service-set-data-alerts.md)
* [ตั้งค่าการแจ้งเตือนข้อมูลในแอปบน iPhone (Power BI สำหรับ iOS)](mobile-set-data-alerts-in-the-mobile-apps.md)
* [ตั้งค่าการแจ้งเตือนข้อมูลในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่สำหรับ Windows 10](mobile-set-data-alerts-in-the-mobile-apps.md)
* [ดาวน์โหลดเวอร์ชันล่าสุดของแอป Power BI](https://powerbi.microsoft.com/mobile/)สำหรับอุปกรณ์เคลื่อนที่