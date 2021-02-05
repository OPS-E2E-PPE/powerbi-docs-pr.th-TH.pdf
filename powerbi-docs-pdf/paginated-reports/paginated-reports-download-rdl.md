---
title: ดาวน์โหลด .rdl สำหรับรายงานแบบแบ่งหน้าจากชุดข้อมูล
description: ในบทความนี้คุณจะได้เรียนรู้วิธีสร้าง .rdl สำหรับรายงานที่มีการแบ่งหน้าของ Power BI โดยการดาวน์โหลดจากชุดข้อมูลที่แชร์ในบริการ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: swgupt
ms.service: powerbi
ms.subservice: report-builder
ms.topic: how-to
ms.date: 10/15/2020
ms.openlocfilehash: c5c8f61a7253da46529a83276366044560d4f030
ms.sourcegitcommit: ccf53e87ff7cba1fcd9d2cca761a561e62933f90
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/04/2020
ms.locfileid: "93297615"
---
# <a name="download-the-rdl-for-a-power-bi-paginated-report-from-a-dataset"></a>ดาวน์โหลด .rdl สำหรับรายงานแบบแบ่งหน้าของ Power BI จากชุดข้อมูล

[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)] 

ในบทความนี้คุณจะได้เรียนรู้วิธีสร้าง .rdl สำหรับรายงานที่มีการแบ่งหน้าของ Power BI โดยการดาวน์โหลดจากชุดข้อมูลที่แชร์ในบริการ Power BI รายงานแบบแบ่งหน้าอยู่ในรูปแบบไฟล์ *.rdl* คุณสามารถสร้างไฟล์ .rdl ได้โดยตรงจากชุดข้อมูลใน Power BI service

1. ไปที่มุมมองรายการสำหรับพื้นที่ทำงานใด ๆ รวมถึง My Workspace 
1. เลือก **ตัวเลือกเพิ่มเติม (...)** สำหรับชุดข้อมูล จากนั้นเลือก **ดาวน์โหลด .rdl**

    :::image type="content" source="media/paginated-reports-download-rdl/power-bi-paginated-download-rdl.png" alt-text="สกรีนช็อตของตัวเลือกดาวน์โหลด .rdl ใน Power BI service":::
1. คุณจะเห็นข้อความที่ระบุว่าคุณจำเป็นต้องอัปเดต Power BI Report Builder เลือก **ดาวน์โหลด** 

    :::image type="content" source="media/paginated-reports-download-rdl/power-bi-report-builder-updates.png" alt-text="สกรีนช็อตของการติดตั้งอัปเดต Power BI Report Builder":::

    หากคุณทราบว่าคุณมี Power BI Report Builder รุ่นล่าสุด ให้เลือก **ฉันติดตั้งอัปเดตเหล่านี้ไปแล้ว**

1. ไปยังกระบวนการติดตั้ง Power BI Report Builder: 

    1. เลือก **ดาวน์โหลด**  
    2. เลือก **เปิดไฟล์** และทำตามขั้นตอนในตัวช่วยติดตั้ง Power BI Report Builder

1. เมื่อการติดตั้ง Report Builder เสร็จสิ้น ให้ย้อนกลับไปยัง Power BI service และเลือก **ดาวน์โหลด .rdl**

    :::image type="content" source="media/paginated-reports-download-rdl/power-bi-report-builder-finished-installing.png" alt-text="สกรีนช็อตของกล่องข้อความดาวน์โหลด .rdl":::

1. เลือก **เปิดไฟล์** ในหน้าต่างเบราว์เซอร์

    :::image type="content" source="media/paginated-reports-download-rdl/power-bi-paginated-open-file.png" alt-text="สกรีนช็อตของการเลือกเปิดไฟล์ในเบราว์เซอร์":::

1. Power BI Report Builder จะเปิดโดยใช้ชื่อที่สร้างโดยอัตโนมัติ และไฟล์ Power BI dataset.pbix ในโฟลเดอร์ **แหล่งข้อมูล** แหล่งข้อมูลมีชื่อเดียวกับชุดข้อมูล Power BI

    :::image type="content" source="media/paginated-reports-download-rdl/power-bi-report-builder-design-canvas.png" alt-text="สกรีนช็อตของ Power BI Report Builder ในมุมมอง Design":::

    พื้นผิวการออกแบบยังมีลิงก์ที่นำไปยังหลักสูตรวิดีโอ [รายงานที่มีการแบ่งหน้าของ Power BI ในหนึ่งวัน](../learning-catalog/paginated-reports-online-course.md) หากคุณยังไม่คุ้นเกคยกับการสร้างรายงานที่มีการแบ่งหน้า หลักสูตรนี้จะช่วยเพิ่มทักษะของคุณ  สามารถลบเมื่อคุณเริ่มออกแบบรายงานของคุณ

    คุณพร้อมที่จะเริ่มออกแบบรายงานที่มีการแบ่งหน้าของคุณแล้ว
 
## <a name="next-steps"></a>ขั้นตอนถัดไป 

- [รายงานแบบแบ่งหน้าใน Power BI Premium คืออะไร](paginated-reports-report-builder-power-bi.md)  
- [บทช่วยสอน: สร้างรายงานแบบแบ่งหน้าและอัปโหลดไปยังบริการของ Power BI](paginated-reports-quickstart-aw.md)
- [เผยแพร่รายงานแบบแบ่งหน้าไปยังบริการของ Power BI](paginated-reports-save-to-power-bi-service.md)

