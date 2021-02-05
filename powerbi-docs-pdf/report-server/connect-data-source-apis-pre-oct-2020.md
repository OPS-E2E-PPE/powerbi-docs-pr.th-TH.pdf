---
title: เปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูลด้วย PowerShell - Power BI Report Server ก่อนเดือนตุลาคม 2020
description: เปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูลโดยใช้ API ใน PowerShell - Power BI Report Server ก่อนเดือนตุลาคม 2020
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.date: 10/26/2020
ms.openlocfilehash: f0dd30e721d8325fdbfd8b562083fbedef2af9c0
ms.sourcegitcommit: 7ed995eed0fd6e718748accf87bae384211cd95d
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2021
ms.locfileid: "99044206"
---
# <a name="change-data-source-connection-strings-in-power-bi-reports-with-powershell---power-bi-report-server-pre-october-2020"></a>เปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูลในรายงาน Power BI ด้วย PowerShell - Power BI Report Server ก่อนเดือนตุลาคม 2020


คุณสามารถเปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูลของรายงาน Power BI ที่โฮสต์ในเซิร์ฟเวอร์รายงาน Power BI โดยใช้ PowerShell เพื่อโต้ตอบกับ Api ที่จำเป็น 

> [!IMPORTANT]
> ถ้าคุณกำลังใช้เวอร์ชันล่าสุดของเซิร์ฟเวอร์รายงาน Power BI ให้ดู[เปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูลในรายงาน POWER BI ด้วย PowerShell-เซิร์ฟเวอร์รายงาน Power BI](connect-data-source-apis.md)

> [!NOTE]
> ตอนนี้ฟังก์ชันนี้ทำงานเพียงกับ DirectQuery การสนับสนุนสำหรับการนำเข้าและการรีเฟรชข้อมูลกำลังจะมา

1. ติดตั้งแอปเพล็ตคำสั่ง PowerShell ของเซิร์ฟเวอร์รายงาน Power BI  ค้นหาคำแนะนำเกี่ยวกับแอปเพล็ตคำสั่งและการติดตั้งที่ [https://github.com/Microsoft/ReportingServicesTools](https://github.com/Microsoft/ReportingServicesTools) 

    ติดตั้ง `ReportingServicesTools` มอดูลโดยตรงจาก [แกลเลอรี PowerShell](https://www.powershellgallery.com/packages/ReportingServicesTools/) โดยใช้คำสั่งต่อไปนี้

    ```powershell
    Install-Module ReportingServicesTools
    ```

2. ดึงข้อมูลแหล่งข้อมูลที่มีอยู่สำหรับไฟล์ Power BI ผ่านทางแอปเพล็ตคำสั่ง PowerShell

    ```powershell
    $dataSources = Get-RsRestItemDataSource -RsItem '/MyPbixReport'
    ```

    วิธีการดูข้อมูลสำหรับแหล่งข้อมูลแรกที่มีอยู่ในรายงาน Power BI: 

    ```powershell
    $dataSources[0]
    ```

3. อัปเดตข้อมูลการเชื่อมต่อและข้อมูลประจำตัวตามความจำเป็น ถ้าการอัปเดตสตริงการเชื่อมต่อและแหล่งข้อมูลทำให้ใช้ข้อมูลประจำตัวที่เก็บไว้ คุณจำเป็นต้องใส่รหัสผ่านของบัญชี 

    วิธีการอัปเดตสตริงการเชื่อมต่อแหล่งข้อมูล

    ```powershell
    $dataSources[0].ConnectionString = 'data source=myCatalogServer;initial catalog=ReportServer;persist security info=False' 
    ```

    วิธีการเปลี่ยนชนิดข้อมูลประจำตัวของแหล่งข้อมูล:

    ```powershell
    $dataSources[0].DataModelDataSource.AuthType = 'Integrated'
    ```

    วิธีการเปลี่ยนชื่อผู้ใช้/รหัสผ่านของแหล่งข้อมูล:

    ```powershell
    $dataSources[0].DataModelDataSource.Username = 'domain\user'
    ```
    ```powershell
    $dataSources[0].DataModelDataSource.Secret = 'password'
    ```

4. บันทึกข้อมูลประจำตัวที่อัปเดตแล้วกลับไปยังเซิร์ฟเวอร์

    ```powershell
    Set-RsRestItemDataSource -RsItem '/MyPbixReport' -RsItemType 'PowerBIReport' -DataSources $dataSources
    ```

## <a name="next-steps"></a>ขั้นตอนถัดไป

[แหล่งข้อมูลรายงานที่มีการแบ่งหน้าในเซิร์ฟเวอร์รายงาน Power BI](connect-data-sources.md) 

มีคำถามเพิ่มเติมหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)
