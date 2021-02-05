---
title: เชื่อมต่อไปยังไฟล์ใน OneDrive สำหรับพื้นที่ทำงานคลาสสิก
description: อ่านเกี่ยวกับการจัดเก็บและการเชื่อมต่อกับไฟล์ Excel, CSV และ Power BI Desktop ของคุณบน OneDrive สำหรับพื้นที่ทำงานของ Power BI คลาสสิกของคุณ
author: maggiesMSFT
ms.author: maggies
ms.reviewer: lukasz
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 01/28/2021
LocalizationGroup: Share your work
ms.openlocfilehash: f6544a137b8f656e938db4516de5e8c0685394b4
ms.sourcegitcommit: fb529c4532fbbdfde7ce28e2b4b35f990e8f21d9
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "99085830"
---
# <a name="connect-to-files-stored-in-onedrive-for-a-classic-workspace"></a>เชื่อมต่อไปยังไฟล์ที่จัดเก็บไว้ใน OneDrive สำหรับพื้นที่ทำงานคลาสสิก
เมื่อคุณ [สร้างพื้นที่ทำงาน *คลาสสิก* ใน Power BI](service-create-workspaces.md)คุณยังสร้างกลุ่ม Microsoft 365 ด้วย OneDrive for Business ที่เชื่อมโยง บทความนี้อธิบายวิธีการจัดเก็บและอัปเดต Excel, CSV และไฟล์ Power BI Desktop ของคุณบน OneDrive for Business การอัปเดตเหล่านั้นมีผลในรายงาน Power BI และแดชบอร์ดที่ยึดตามไฟล์เหล่านั้นโดยอัตโนมัติ

> [!NOTE]
> ประสบการณ์ในพื้นที่ทำงาน *ใหม่* เปลี่ยนความสัมพันธ์ระหว่างพื้นที่ดำเนินการ Power BI และกลุ่ม Microsoft 365 คุณจะไม่สามารถสร้าง Microsoft 365 Group โดยอัตโนมัติทุกครั้งที่คุณสร้างพื้นที่ทำงานใหม่ คุณยังสามารถ [ตั้งค่า OneDrive พื้นที่ทำงานสำหรับพื้นที่ทำงานใหม่](service-create-the-new-workspaces.md#set-a-workspace-onedrive)ได้

การเพิ่มไฟล์ลงในพื้นที่ทำงานคลาสสิกของคุณคือกระบวนการแบบสองขั้นตอน: 

1. ก่อนอื่น คุณ[อัปโหลดไฟล์ไปยัง OneDrive for Business](#1-upload-files-to-the-onedrive-for-business-for-your-workspace)สำหรับพื้นที่ทำงานของคุณ
2. แล้วคุณ[เชื่อมต่อกับไฟล์เหล่านั้นจาก Power BI](#2-import-excel-files-as-datasets-or-as-excel-online-workbooks)

> [!NOTE]
> พื้นที่ทำงานใช้ได้กับสิทธิ์การใช้งาน [Power BI Pro](../fundamentals/service-features-license-type.md) เท่านั้น
> 

## <a name="1-upload-files-to-the-onedrive-for-business-for-your-workspace"></a>1 อัปโหลดไฟล์ไปยัง OneDrive for Business สำหรับพื้นที่ทำงานของคุณ
1. ใน Power BI service เลือกลูกศรอยู่ถัดจากพื้นที่ทำงาน > เลือกจุดไข่ปลา ( **...** ) ถัดจากชื่อพื้นที่ทำงานของคุณ 
   
   ![ภาพหน้าจอของพื้นที่ทำงาน Power BI ที่แสดงชื่อพื้นที่ทำงานที่เลือก](media/service-connect-to-files-in-app-workspace-onedrive-for-business/power-bi-app-ellipsis.png)
2. เลือก **ไฟล์** เพื่อเปิด OneDrive for Business สำหรับพื้นที่ทำงานบน Microsoft 365
   
   > [!NOTE]
   > ถ้าคุณไม่เห็น **ไฟล์** บนเมนูพื้นที่ทำงาน ให้เลือก **สมาชิก** เพื่อเปิด OneDrive for Business สำหรับพื้นที่ทำงาน ที่นั่น เลือก **ไฟล์** Microsoft 365 ตั้งค่าตำแหน่งที่เก็บข้อมูล OneDrive สำหรับไฟล์พื้นที่ทำงานของกลุ่มของแอปของคุณ กระบวนการนี้อาจใช้เวลาสักครู่
   > 
   > 
3. ที่นี่ คุณสามารถอัปโหลดไฟล์ไปยัง OneDrive for Business สำหรับพื้นที่ทำงานของคุณ เลือก **อัปโหลด** และนำทางไปยังไฟล์ของคุณ
   
   ![ภาพหน้าจอของ OneDrive for Business ที่แสดงวิธีการนำทางเพื่ออัปโหลดไฟล์](media/service-connect-to-files-in-app-workspace-onedrive-for-business/pbi_grpfilesonedrive.png)

## <a name="2-import-excel-files-as-datasets-or-as-excel-online-workbooks"></a>2 นำเข้าไฟล์ Excel ในฐานะชุดข้อมูลหรือในฐานะสมุดงาน Excel Online
เมื่อไฟล์ของคุณอยู่ใน OneDrive for Business สำหรับพื้นที่ทำงาน คุณมีตัวเลือกดังนี้ คุณสามารถ: 

* [นำเข้าข้อมูลจากเวิร์กบุ๊ก Excel เป็นชุดข้อมูล](../connect-data/service-get-data-from-files.md) จากนั้นใช้ข้อมูลเพื่อสร้างรายงานและแดชบอร์ดที่คุณสามารถดูในเว็บเบราว์เซอร์ และบนอุปกรณ์มือถือ
* หรือ[เชื่อมต่อกับเวิร์กบุ๊ก Excel เต็มใน Power BI](../connect-data/service-excel-workbook-files.md)และแสดงไว้เหมือนกับที่จะปรากฏขึ้นใน Excel Online

### <a name="import-or-connect-to-the-files-in-your-workspace"></a>นำเข้า หรือเชื่อมต่อกับไฟล์ในพื้นที่ทำงานของคุณ
1. ใน Power BI ให้สลับไปยังพื้นที่ทำงาน ดังนั้นชื่อพื้นที่ทำงานจะอยู่ที่มุมบนซ้าย 
2. เลือก **รับข้อมูล** ที่ด้านล่างของบานหน้าต่างนำทาง 
   
   ![ภาพหน้าจอของปุ่มรับข้อมูล ที่แสดงในบานหน้าต่างนำทาง](media/service-connect-to-files-in-app-workspace-onedrive-for-business/power-bi-app-get-data-button.png)
3. ในกล่อง **ไฟล์** เลือก **รับ**
   
   ![ภาพหน้าจอของกล่องโต้ตอบไฟล์ ที่แสดงปุ่มรับ](media/service-connect-to-files-in-app-workspace-onedrive-for-business/pbi_getfiles.png)
4. เลือก **OneDrive** - *ชื่อพื้นที่ทำงานของคุณ*
   
    ![ภาพหน้าจอของไทล์สามตัวเพื่อเลือกพื้นที่ทำงานของคุณ ที่แสดงไฟล์ภายในเครื่อง OneDrive และ SharePoint](media/service-connect-to-files-in-app-workspace-onedrive-for-business/pbi_grp_one_drive_shrpt.png)
5. เลือกไฟล์คุณต้อง > **เชื่อมต่อ**
   
    ในจุดนี้คุณตัดสินใจว่า จะ[นำเข้าข้อมูลจากสมุดงาน Excel](../connect-data/service-get-data-from-files.md)หรือ[เชื่อมต่อไปยังเวิร์กบุ๊ก Excel ทั้งหมด](../connect-data/service-excel-workbook-files.md)
6. เลือก **นำเข้า** หรือ **เชื่อมต่อ**
   
    ![ภาพหน้าจอของกล่องโต้ตอบ OneDrive for Business ที่แสดงนำเข้าจาก Excel หรือเชื่อมต่อกับ Excel](media/service-connect-to-files-in-app-workspace-onedrive-for-business/pbi_importexceldataorwholecrop.png)
7. ถ้าคุณเลือก **นำเข้า** แล้วเวิร์กบุ๊กปรากฏขึ้นบนแท็บ **ชุดข้อมูล** 
   
    ![ภาพหน้าจอของพื้นที่ทำงานใน Power BI ที่แสดงแท็บชุดข้อมูล](media/service-connect-to-files-in-app-workspace-onedrive-for-business/power-bi-app-excel-file-import.png)
   
    ถ้าคุณเลือก **เชื่อมต่อ** แล้วเวิร์กบุ๊กอยู่บนแท็บ **สมุดงาน**
   
    ![ภาพหน้าจอของพื้นที่ทำงานใน Power BI ที่แสดงแท็บสมุดงาน](media/service-connect-to-files-in-app-workspace-onedrive-for-business/power-bi-app-excel-file-connect.png)

## <a name="next-steps"></a>ขั้นตอนถัดไป
* [สร้างแอปและพื้นที่ทำงานใน Power BI](../collaborate-share/service-create-distribute-apps.md)
* [นำเข้าข้อมูลจากเวิร์กบุ๊ก Excel](../connect-data/service-get-data-from-files.md)
* [Connect to whole Excel workbooks](../connect-data/service-excel-workbook-files.md
* มีคำถามเพิ่มเติมหรือไม่ [ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)
* มีคำติชมหรือไม่ เยี่ยมชม[แนวคิด Power BI](https://ideas.powerbi.com/forums/265200-power-bi)
