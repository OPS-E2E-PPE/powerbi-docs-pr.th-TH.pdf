---
title: 'สร้างรายงานจากไฟล์ Excel ในบริการของ Power BI '
description: สร้างรายงาน Power BI จากไฟล์ Excel ในบริการของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 10/14/2020
LocalizationGroup: Reports
ms.openlocfilehash: a971e0d0b35b0a3988a1c10ea2b7b801830229d6
ms.sourcegitcommit: 0711972326521944fdd8572403c0b15f31b916da
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/22/2020
ms.locfileid: "97721558"
---
# <a name="create-a-report-from-an-excel-file-in-the-power-bi-service"></a>สร้างรายงานจากไฟล์ Excel ในบริการของ Power BI
คุณได้อ่าน[รายงานใน Power BI](../consumer/end-user-reports.md)และตอนนี้ คุณต้องการสร้างรายงานของคุณเอง มีหลายวิธีในการสร้างรายงาน ในบทความนี้ เราจะเริ่มต้นด้วยการสร้างรายงานพื้นฐานในบริการของ Power BI จากไฟล์ Excel เมื่อคุณทำความเข้าใจพื้นฐานของการสร้างรายงาน ตรวจดู[ขั้นตอนถัดไป](#next-steps)ที่ด้านล่างสำหรับหัวข้อการรายงานขั้นสูงเพิ่มเติม  

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น
- [ลงทะเบียนสำหรับบริการของ Power BI](../fundamentals/service-self-service-signup-for-power-bi.md) 
- [ดาวน์โหลดไฟล์ Excel ตัวอย่างการวิเคราะห์การค้าปลีก](https://go.microsoft.com/fwlink/?LinkId=529778) และบันทึกลงในคอมพิวเตอร์ของคุณหรือไปยัง OneDrive for Business

## <a name="import-the-excel-file"></a>นำเข้าไฟล์ Excel
วิธีการสร้างรายงานนี้เริ่มต้น ด้วยไฟล์และพื้นทีรายงานที่ว่างเปล่า คุณสามารถทำตามในไฟล์ Excel ตัวอย่างของการวิเคราะห์ร้านค้าปลีก

1. ในบานหน้าต่างการนำทาง ให้เลือก **พื้นที่ทำงานของฉัน**
   
   :::image type="content" source="media/service-report-create-new/power-bi-select-my-workspace.png" alt-text="สกรีนช็อตของการเลือก พื้นที่ทำงานของฉัน":::
2. จากด้านล่างของบานหน้าต่างนำทาง เลือก **รับข้อมูล**
   
   ![รับข้อมูล](media/service-report-create-new/power-bi-get-data3.png)
3. เลือก **แฟ้ม** และนำทางไปยังตำแหน่งที่คุณบันทึกตัวอย่างการวิเคราะห์ร้านค้าปลีก
   
    ![เลือกไฟล์](media/service-report-create-new/power-bi-select-files.png)
4. สำหรับการดำเนินการนี้ เลือก **นำเข้า**
   
   ![เลือกนำเข้า](media/service-report-create-new/power-bi-import.png)
5. เลือก **เปิด**

   เมื่อนำเข้าไฟล์ Excel แล้ว ระบบจะแสดงเป็น *ชุดข้อมูล* ในรายการพื้นที่ทำงาน

1. เลือก **ตัวเลือกเพิ่มเติม (...)** ที่อยู่ถัดจากชุดข้อมูล แล้วเลือก **สร้างรายงาน**
   
   :::image type="content" source="media/service-report-create-new/power-bi-dataset-create-report.png" alt-text="สกรีนช็อตของการเลือก สร้างรายงาน":::
6. ตัวแก้ไขรายงานจะเปิดขึ้น 
   
   ![สกรีนช็อตของตัวแก้ไขรายงาน](media/service-report-create-new/power-bi-blank-report.png)

> [!TIP]
> เลือกไอคอนเมนูเพื่อซ่อนบานหน้าต่างนำทาง เพื่อให้คุณมีพื้นที่มากขึ้น
> 
> :::image type="content" source="../media/power-bi-hide-navigation-pane.png" alt-text="สกรีนช็อตของเลือกไอคอนเมนู เพื่อซ่อนบานหน้าต่างนำทาง":::


## <a name="add-a-radial-gauge-to-the-report"></a>เพิ่มการวัดรัศมีลงในรายงาน
หลังจากที่ชุดข้อมูลของเราจะถูกนำเข้า มาเริ่มต้นการตอบคำถามบางอย่าง  เราหัวหน้าฝ่ายตลาดเจ้าหน้าที่ (CMO) ต้องการทราบเกี่ยวกับวิธีปิดเราที่การประชุมเป้าหมายการขายของปีนี้ การวัดจะเป็น[ตัวเลือกการแสดงภาพที่ดี](../visuals/power-bi-report-visualizations.md)สำหรับการแสดงข้อมูลชนิดนี้

1. ในบานหน้าต่างเขตข้อมูล เลือก **ยอดขาย** > **ค่ายอดขายของปี** > **นี้**
   
    ![แผนภูมิคอลัมน์ในตัวแก้ไขรายงาน](media/service-report-create-new/power-bi-report-step1.png)
2. แปลงภาพเป็นการวัด โดยการเลือกเทมเพลวัด![ไอคอนตัววัด](media/service-report-create-new/powerbi-gauge-icon.png)จาก **หน้าต่าง** แสดงภาพ
   
    ![ภาพแผนที่ในตัวแก้ไขรายงาน](media/service-report-create-new/power-bi-report-step2.png)
3. ลาก **ยอดขาย** > **เป้าหมายยอดขาย** > **ของปีนี้** เพื่อ **ค่าเป้าหมาย** กัน ดูเหมือนว่าเรากำลังใกล้เคียงกับเป้าหมายของเรามาก
   
    ![ตัววัดแบบภาพ ด้วยเป้าหมายเป็นค่าเป้าหมาย](media/service-report-create-new/power-bi-report-step3.png)
4. ในตอนนี้เป็นเวลาที่เหมาะสมที่จะบันทึกรายงานของคุณ
   
   ![เมนูไฟล์](media/service-report-create-new/powerbi-save.png)

## <a name="add-an-area-chart-and-slicer-to-the-report"></a>เพิ่มชาร์ตพื้นที่และ slicer ในรายงาน
CMO ของเรามีคำถามบางอย่างเพิ่มเติมให้แก่เรา พวกเขาต้องการทราบวิธีการเปรียบเทียบยอดขายของปีนี้กับปีที่แล้ว และพวกเขาต้องการดูผลลัพธ์ตามเขต

1. ก่อนอื่น มาสร้างพื้นที่ว่างในพื้นที่รายงานก่อน เลือกตัววัด และย้ายไปมุมบนขวา จากนั้น จับ และลากมุมหนึ่ง และทำให้เล็กลง
2. ยกเลิกเลือกตัววัด ในบานหน้าต่างเขตข้อมูล เลือก **ยอดขาย** > **ค่ายอดขายของปีนี้** > **นี้** เลือก **ขาย** > **ยอดขายของปีที่แล้ว**
   
    ![ตัวแก้ไขรายงาน ด้วยตัววัดและแผนภูมิแท่ง](media/service-report-create-new/power-bi-report-step4.png)
3. แปลงภาพเป็นแผนภูมิพื้นที่โดยเลือกเทมเพลตแผนภูมิพื้นที่![
ไอคอนแผนภูมิ](media/service-report-create-new/power-bi-areachart-icon.png)จาก **หน้าต่าง** แสดงภาพ
4. เลือก **เวลา** > **รอบระยะเวลา** เพื่อเพิ่มไปยัง **แกน** กัน
   
    ![ตัวแก้ไขรายงาน ด้วยแผนภูมิพื้นที่ที่ใช้งานอยู่](media/service-report-create-new/power-bi-report-step5.png)
5. เมื่อต้องการเรียงลำดับการแสดงภาพ โดยรอบระยะเวลา เลือกจุดไข่ปลา แล้วเลือก **เรียงลำดับตามระยะเวลา**
6. ตอนนี้มาเพิ่มตัวแบ่งส่วนข้อมูล เลือกพื้นที่ว่างบนพื้นที่รายงาน และเลือกตัวแบ่งส่วนข้อมูล ![ไอคอนตัวแบ่งส่วนข้อมูล](media/service-report-create-new/power-bi-slicer-icon.png) แม่แบบ ตอนนี้เรามีตัวแบ่งส่วนข้อมูลที่ว่างเปล่าบนพื้นที่ทำงานของเรา
   
    ![พื้นที่รายงาน](media/service-report-create-new/power-bi-report-step6.png)    
7. จากบานหน้าต่างเขตข้อมูล เลือก **เขต** > **เขต** ย้าย และปรับขนาดตัวแบ่งส่วนข้อมูล
   
    ![ตัวแก้ไขรายงาน เพิ่มเขต](media/service-report-create-new/power-bi-report-step7.png)  
8. ใช้ตัวแบ่งส่วนข้อมูลเพื่อค้นหารูปแบบและข้อมูลเชิงลึก โดยเขต
   
   ![วิดีโอของการใช้ตัวแบ่งส่วนข้อมูล](media/service-report-create-new/power-bi-slicer-video2.gif)  

สำรวจข้อมูลของคุณ และเพิ่มการแสดงภาพต่อไป เมื่อคุณค้นหาข้อมูลเชิงลึกที่น่าสนใจโดยเฉพาะอย่างยิ่ง[ปักหมุดเหล่านั้นไปยังแดชบอร์ด](service-dashboard-pin-tile-from-report.md)

## <a name="next-steps"></a>ขั้นตอนถัดไป

* [ปักหมุดภาพไปยังแดชบอร์ด](service-dashboard-pin-tile-from-report.md)
* [เปลี่ยนการตั้งค่ารายงานในบริการของ Power BI](power-bi-report-settings.md)
* มีคำถามเพิ่มเติมหรือไม่ [ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)
