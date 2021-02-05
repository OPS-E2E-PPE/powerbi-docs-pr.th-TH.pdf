---
title: ควบคุมการใช้งานชุดข้อมูลทั่วทั้งพื้นที่ทำงาน - Power BI
description: เรียนรู้วิธีการจำกัดการไหลของข้อมูลในผู้เช่า Power BI
author: paulinbar
ms.author: painbar
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: how-to
ms.date: 04/30/2020
LocalizationGroup: Share your work
ms.openlocfilehash: d94be70bd61988f009900432e3bc77756a3821df
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96392576"
---
# <a name="control-the-use-of-datasets-across-workspaces"></a>ควบคุมการใช้งานชุดข้อมูลทั่วทั้งพื้นที่ทำงาน

การใช้ชุดข้อมูลทั้งพื้นที่ทำงานเป็นวิธีมีประสิทธิภาพเพื่อส่งเสริมวัฒนธรรมการเก็บข้อมูลและการพัฒนาข้อมูลให้เป็นระบบภายในองค์กร ถ้าคุณเป็นผู้ดูแลระบบ Power BI ในบางครั้งคุณต้องการจำกัดการไหลของข้อมูลภายในผู้เช่า Power BI ด้วยการตั้งค่าผู้เช่า **ใช้ชุดข้อมูลทั้งพื้นที่ทำงาน** คุณสามารถจำกัดการใช้ชุดข้อมูลซ้ำ ไม่ว่าจะทั้งหมดหรือบางส่วนต่อกลุ่มความปลอดภัยได้

![การตั้งค่าพื้นที่ทำงานของผู้ดูแลระบบ Power BI](media/service-datasets-admin-across-workspaces/power-bi-admin-workspace-settings.png)

หากคุณปิดการตั้งค่านี้ จะมีผลกระทบต่อผู้สร้างรายงาน:

- ปุ่มคัดลอกรายงานทั้งพื้นที่ทำงานไม่พร้อมใช้งาน 
- ในรายงานที่ยึดตามชุดข้อมูลที่ใช้ร่วมกัน ปุ่ม **แก้ไขรายงาน** ไม่พร้อมใช้งาน
- ในบริการของ Power BI ประสบการณ์การค้นหาจะแสดงเฉพาะชุดข้อมูลในพื้นที่ทำงานปัจจุบันเท่านั้น
- ใน Power BI Desktop ประสบการณ์การค้นหาจะแสดงเฉพาะชุดข้อมูลจากพื้นที่ทำงานที่คุณเป็นสมาชิกเท่านั้น
- ใน Power BI Desktop ถ้าผู้ใช้เปิดไฟล์.pbix ด้วยการเชื่อมต่อสดไปยังชุดข้อมูลที่อยู่นอกพื้นที่ทำงานใด ๆ ที่ผู้ใช้เป็นสมาชิกของ พวกเขาจะเห็นข้อความแสดงข้อผิดพลาด ซึ่งขอให้พวกเขาเชื่อมต่อกับชุดข้อมูลอื่น

## <a name="provide-a-link-for-the-certification-process"></a>มีลิงก์สำหรับกระบวนการออกใบรับรอง

ในฐานะผู้ดูแลระบบ Power BI คุณสามารถใส่ URL สำหรับลิงก์ **เรียนรู้เพิ่มเติม** บนหน้าการตั้งค่า **การรับรอง** ได้  ดู [เปิดการใช้งานใบรับรองเนื้อหา](../admin/service-admin-setup-certification.md) สำหรับรายละเอียด ลิงก์นี้สามารถไปที่เอกสารประกอบเกี่ยวกับกระบวนการออกใบรับรองของคุณ ถ้าคุณไม่กำหนดปลายทางสำหรับลิงก์ **เรียนรู้เพิ่มเติม** ตามค่าเริ่มต้นจะลิงก์ไปยังบทความ [รับรองเนื้อหาของคุณ](../collaborate-share/service-endorse-content.md)

![เรียนรู้เพิ่มเติมเกี่ยวกับใบรับรองชุดข้อมูล](media/service-datasets-admin-across-workspaces/service-admin-certification-setup-dialog.png)

## <a name="next-steps"></a>ขั้นตอนถัดไป

- [ใช้ชุดข้อมูลทั่วทั้งพื้นที่ทำงาน](service-datasets-across-workspaces.md)
- มีคำถามหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)
