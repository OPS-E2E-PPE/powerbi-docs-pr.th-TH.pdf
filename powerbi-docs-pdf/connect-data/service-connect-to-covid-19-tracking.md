---
title: การเชื่อมต่อรายงานการติดตาม COVID-19 ในสหรัฐอเมริกา
description: วิธีการรับและติดตั้งแอปเทมเพลตของเคส COVID-19 และวิธีการเชื่อมต่อกับข้อมูล
author: paulinbar
ms.author: painbar
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: how-to
ms.date: 04/05/2020
LocalizationGroup: Connect to services
ms.openlocfilehash: fc421f7635a3d6e3b2336d5bce081d7914c0fad5
ms.sourcegitcommit: 8250187368d3de48663eb516a816ff701119b579
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/10/2020
ms.locfileid: "96998875"
---
# <a name="connect-to-the-covid-19-us-tracking-report"></a>การเชื่อมต่อรายงานการติดตาม COVID-19 ในสหรัฐอเมริกา
บทความนี้จะแจ้งวิธีการติดตั้งแอปเทมเพลตสำหรับรายงานการติดตาม COVID-19 และวิธีการเชื่อมต่อกับแหล่งข้อมูลให้คุณทราบ

![รายงานการติดตาม COVID-19 ในสหรัฐอเมริกา](media/service-connect-to-covid-19-tracking/service-covid-19-us-tracking-report-title-screen.png)

สำหรับข้อมูลโดยละเอียดเกี่ยวกับตัวรายงาน รวมถึงการปฏิเสธความรับผิดชอบและข้อมูลเกี่ยวกับข้อมูล โปรดศึกษาจาก[ตัวอย่างการติดตาม COVID-19 ของรัฐแห่งสหรัฐอเมริกาและรัฐบาลท้องถิ่น](../create-reports/sample-covid-19-us.md)

หลังจากที่คุณได้ติดตั้งแอปเทมเพลตและเชื่อมต่อกับแหล่งข้อมูลแล้ว คุณสามารถปรับแต่งรายงานได้ตามความต้องการของคุณ จากนั้นคุณจะสามารถเผยแพร่รายงานออกเป็นแอปให้กับเพื่อนร่วมงานในองค์กรของคุณได้

## <a name="install-the-app"></a>ติดตั้งแอป

1. คลิกที่ลิงก์ต่อไปนี้เพื่อเข้าถึงแอป: [แอปเทมเพลตรายงานการติดตาม COVID-19 ในสหรัฐอเมริกา](https://app.powerbi.com/groups/me/getapps/services/pbi-contentpacks.covid19ms)

1. เมื่อคุณอยู่ในหน้า AppSource ของแอป ให้คลิกที่ [**รับทันที**](https://app.powerbi.com/groups/me/getapps/services/pbi-contentpacks.covid19ms)

    [![รายงานการติดตามข้อมูลเกี่ยวกับโควิด 19 ที่สหรัฐอเมริกาใน AppSource](media/service-connect-to-covid-19-tracking/service-covid-19-us-tracking-report-appsource-icon.png)](https://app.powerbi.com/groups/me/getapps/services/pbi-contentpacks.covid19ms)

1. เมื่อมีข้อความแสดงขึ้น ให้คลิก **Install** หลังจากที่ติดตั้งแอปแล้ว คุณจะเห็นแอปบนหน้าแอปของคุณ

   ![รายงานการติดตาม COVID-19 ในสหรัฐอเมริกาบนหน้าแอป](media/service-connect-to-covid-19-tracking/service-covid-19-us-tracking-report-apps-page-icon.png)

## <a name="connect-to-data-sources"></a>เชื่อมต่อกับแหล่งข้อมูล

1. คลิกที่ไอคอนบนหน้าแอปของคุณเพื่อเปิดแอป แอปจะเปิดขึ้นและแสดงข้อมูลตัวอย่าง

1. เลือกลิงก์ **เชื่อมต่อข้อมูลของคุณ** บนแบนเนอร์ที่ด้านบนของหน้า

   ![แอป GitHub เชื่อมโยงลิงก์ข้อมูลของคุณ](media/service-connect-to-covid-19-tracking/power-bi-covid-19-connect-data.png)

1. กล่องโต้ตอบพารามิเตอร์จะปรากฏขึ้น ไม่มีพารามิเตอร์ที่จำเป็น คลิก **ถัดไป**

   ![สกรีนช็อตของกล่องโต้ตอบพารามิเตอร์รายงานการติดตาม Covid-19 ในสหรัฐอเมริกา](media/service-connect-to-covid-19-tracking/service-covid-19-us-tracking-report-parameters-dialog.png)

1. กล่องโต้ตอบวิธีการรับรองความถูกต้องจะปรากฏขึ้น ระบบจะแสดงค่าที่แนะนำ อย่าเปลี่ยนแปลงข้อมูลเหล่านี ้เว้นแต่ว่าคุณมีความรู้เฉพาะเกี่ยวกับค่าต่าง ๆ

    คลิก **ถัดไป**

   ![สกรีนช็อตของกล่องโต้ตอบการรับรองความถูกต้องรายงานการติดตาม Covid-19 ในสหรัฐอเมริกา](media/service-connect-to-covid-19-tracking/service-covid-19-us-tracking-report-authentication-dialog.png)

1. คลิก **ลงชื่อเข้าใช้**

   ![สกรีนช็อตของกล่องโต้ตอบลงชื่อเข้าใช้รายงานการติดตาม Covid-19 ในสหรัฐอเมริกา](media/service-connect-to-covid-19-tracking/service-covid-19-us-tracking-report-signin-dialog.png)
 
   รายงานจะเชื่อมต่อกับแหล่งข้อมูล ซึ่งจะมีข้อมูลล่าสุดแจ้งเข้าไปอยู่เสมอ ในช่วงเวลานี้ คุณจะเห็นข้อมูลตัวอย่างและการรีเฟรชกำลังดำเนินการอยู่

   ![กำลังรีเฟรชรายงานการติดตาม COVID-19 ในสหรัฐอเมริกา](media/service-connect-to-covid-19-tracking/service-covid-19-us-tracking-report-refresh-monitor.png)

## <a name="schedule-report-refresh"></a>กำหนดเวลาการรีเฟรชรายงาน

เมื่อการรีเฟรชข้อมูลเสร็จสมบูรณ์ คุณจะอยู่ในพื้นที่ทำงานที่เชื่อมโยงกับแอป [ตั้งค่ากำหนดเวลาการรีเฟรช](../connect-data/refresh-scheduled-refresh.md)เพื่อให้ข้อมูลรายงานเป็นข้อมูลล่าสุดอยู่เสมอ

## <a name="customize-and-share"></a>ปรับแต่งตามความต้องการและแชร์

คุณสามารถดูรายละเอียดได้ที่[ปรับแต่งและแชร์แอป](../connect-data/service-template-apps-install-distribute.md#customize-and-share-the-app) ตรวจสอบให้มั่นใจว่าคุณได้อ่าน[ข้อความปฏิเสธความรับผิดชอบของรายงาน](../create-reports/sample-covid-19-us.md#disclaimers)ก่อนที่จะเผยแพร่หรือแจกจ่ายแอป

## <a name="next-steps"></a>ขั้นตอนถัดไป
* [ตัวอย่างการติดตาม COVID-19 สำหรับรัฐของสหรัฐอเมริกาและรัฐบาลในท้องถิ่น](../create-reports/sample-covid-19-us.md)
* มีคำถามหรือไม่? [ลองถามชุมชน Power BI](https://community.powerbi.com/)
* [แอปเทมเพลต Power BI คืออะไร](../connect-data/service-template-apps-overview.md)
* [ติดตั้งและแจกจ่ายแอปเทมเพลตในองค์กรของคุณ](../connect-data/service-template-apps-install-distribute.md)
