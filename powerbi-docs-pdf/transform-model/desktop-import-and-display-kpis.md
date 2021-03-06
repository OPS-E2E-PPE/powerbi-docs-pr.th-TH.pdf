---
title: นำเข้า และแสดง KPI ใน Power BI
description: นำเข้า และแสดง KPI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: how-to
ms.date: 05/08/2019
LocalizationGroup: Model your data
ms.openlocfilehash: c7aeb70d99b8ce32191d04d002c638c6bb69c7fb
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415645"
---
# <a name="import-and-display-kpis-in-power-bi"></a>นำเข้า และแสดง KPI ใน Power BI
ด้วย **Power BI Desktop** คุณสามารถนำเข้าและแสดง KPI ในตาราง, เมทริกซ์ และการ์ดได้

ทำตามขั้นตอนเหล่านี้ เมื่อต้องการนำเข้า และแสดง KPI

1. เริ่มต้นด้วยเวิร์กบุ๊ก Excel ที่มีแบบจำลอง Power Pivot และ KPI แบบทดสอบนี้ใช้ชื่อเวิร์กบุ๊กว่า *KPI*

1. นำเข้าเวิร์กบุ๊ก Excel ลงใน Power BI โดยใช้ **ไฟล์ -> นำเข้า -> เนื้อหาเวิร์กบุ๊ก Excel** คุณยังสามารถ[เรียนรู้วิธีการนำเข้าเวิร์กบุ๊ก](../connect-data/desktop-import-excel-workbooks.md)ได้อีกด้วย 

1. หลังจากนำเข้าลงใน Power BI, KPI ของคุณจะปรากฏขึ้นในบานหน้าต่าง **เขตข้อมูล** ที่ทำเครื่องหมายด้วยไอคอน![ไฟจราจร](media/desktop-import-and-display-kpis/traffic.png) เพื่อใช้ KPI ในรายงานของคุณ ตรวจสอบให้แน่ใจว่าได้ขยายเนื้อหา ให้แสดงเขตข้อมูล **Value**, **Goal** และ **Status**

    ![ภาพหน้าจอของ Power BI Desktop ที่แสดง Delta KPI ที่ขยายในบานหน้าต่างเขตข้อมูล](media/desktop-import-and-display-kpis/desktoppreviewfeatureon2.png)
 
1. KPI ที่นำเข้า เหมาะที่สุดสำหรับการแสดงภาพชนิดมาตรฐาน เช่น ชนิด **ตาราง** Power BI ยังมีการแสดงภาพชนิด **KPI** ซึ่งควรใช้เพื่อสร้าง KPI ใหม่เท่านั้น
   
    ![ภาพหน้าจอของ Power BI Desktop ที่แสดงเขตข้อมูล Table1 ที่เลือกในบานหน้าต่างเขตข้อมูล](media/desktop-import-and-display-kpis/desktoppreviewfeatureon3.png)

ขั้นตอนทั้งหมดก็มีเพียงเท่านี้ คุณสามารถใช้ KPI เพื่อเน้นแนวโน้มที่สำคัญ, ความคืบหน้า หรือตัวบ่งชี้ที่สำคัญอื่นๆ
