---
title: ส่งออกรายงานจนด้วย Power อัตโนมัติ
description: เรียนรู้วิธีการสร้างโฟลว์ Power Automate เพื่อส่งออกรายงานที่มีการแบ่งหน้า Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 12/14/2020
LocalizationGroup: Get started
ms.openlocfilehash: 5c69abe925751e8b065f262e151bfee65c487238
ms.sourcegitcommit: 46cf62d9bb33ac7b7eae7910fbba6756f626c65f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/15/2020
ms.locfileid: "97492069"
---
# <a name="export-power-bi-paginated-reports-with-power-automate"></a>ส่งออกรายงานที่มีการแบ่งหน้า Power BI ด้วย Power Automate

ด้วย [Power Automate](/power-automate/getting-started) คุณสามารถทำให้การส่งออกและการแจกจ่ายรายงานที่มีการแบ่งหน้า Power BI ไปยังรูปแบบและสถานการณ์ที่ได้รับการสนับสนุนเป็นแบบอัตโนมัติ ในบทความนี้ คุณจะได้เรียนรู้ว่าเทมเพลตใดบ้างที่จะใช้สร้างโฟลว์ของคุณเองเพื่อส่งออกรายงานที่มีการแบ่งหน้าของคุณ  

## <a name="prerequisites"></a>สิ่งที่จำเป็นต้องมี  

เพื่อดำเนินการต่อไป คุณควรตรวจสอบให้แน่ใจว่าคุณมีรายการต่อไปนี้:

- พื้นที่ทำงานในผู้เช่า Power BI ของคุณที่ได้รับการสนับสนุนจากความจุที่สงวนไว้อย่างน้อยหนึ่งรายการ ความจุนี้สามารถเป็น SKU ใดก็ได้ตั้งแต่ A4/P1 – A6/P3 อ่านเพิ่มเติมเกี่ยวกับ[ความจุที่สงวนไว้ใน Power BI Premium](../admin/service-premium-what-is.md)
- เข้าถึงตัวเชื่อมต่อมาตรฐานใน Power Automate ซึ่งมาพร้อมกับการสมัครใช้งาน Office 365

## <a name="create-a-flow-from-a-template"></a>สร้างโฟลว์จากเทมเพลต 

1. ลงชื่อเข้าใช้ Power Automate [flow.microsoft.com](https://flow.microsoft.com/) 
1. เลือก **เทมเพลต** และค้นหา  **รายงานที่มีการแบ่งหน้า** 

    :::image type="content" source="media/service-automate-paginated-integration/power-bi-paginate-automate.png" alt-text="สกรีนช็อตของเทมเพลต Power Automate อื่น ๆ สำหรับรายงานที่มีการแบ่งหน้า Power BI":::

## <a name="select-a-template"></a>เลือกเทมเพลต 

เลือกเทมเพลตจากรายการเพื่อเริ่มต้นใช้งานด้วยคำแนะนำทีละขั้นตอน  

- [บันทึกรายงานที่มีการแบบแบ่งหน้า Power BI ไปยัง OneDrive for Business หรือโฟลเดอร์ SharePoint Online](service-automate-paginated-onedrive-sharepoint.md)  
- [ส่งออกรายงานที่มีการแบ่งหน้า Power BI สำหรับหน่วยข้อมูลในรายการ SharePoint Online หรือสำหรับแต่ละแถวในตาราง Excel Online](service-automate-paginated-excel-sharepoint-list.md)
- [บันทึกรายงานที่มีการแบ่งหน้า Power BI ไปยังโฟลเดอร์ระบบภายในเครื่อง](service-automate-paginated-local-file.md)

## <a name="next-steps"></a>ขั้นตอนถัดไป

- [API การส่งออก Power BI สำหรับรายงานที่มีการแบ่งหน้า](../developer/embedded/export-paginated-report.md)
- [เริ่มต้นใช้งาน Power Automate](/power-automate/getting-started/)
- มีคำถามเพิ่มเติมหรือไม่ [ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)
