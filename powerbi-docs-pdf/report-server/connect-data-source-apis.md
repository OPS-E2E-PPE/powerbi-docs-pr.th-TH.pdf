---
title: เปลี่ยนแปลงชุดอักขระการเชื่อมต่อต้นทางของข้อมูลผ่าน PowerShell
description: เปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูลโดยใช้ API ใน PowerShell - เซิร์ฟเวอร์รายงาน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.date: 10/26/2020
ms.openlocfilehash: b7f431ba6b8f559380916c17689d0eab74a0c9a7
ms.sourcegitcommit: 7ed995eed0fd6e718748accf87bae384211cd95d
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2021
ms.locfileid: "99044321"
---
# <a name="change-data-source-connection-strings-in-power-bi-reports-with-powershell---power-bi-report-server"></a>เปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูลในรายงาน Power BI ด้วย PowerShell - เซิร์ฟเวอร์รายงาน Power BI


เริ่มต้นด้วยการเผยแพร่เดือนตุลาคม๒๐๒๐ของเซิร์ฟเวอร์รายงาน Power BI เราเปิดใช้งานความสามารถในการปรับปรุงการเชื่อมต่อสำหรับรายงาน Power BI สำหรับ DirectQuery และรีเฟรช

> [!IMPORTANT]
> นอกจากนี้ยังเป็นการเปลี่ยนแปลงอย่างสิ้นเชิงในการตั้งค่านี้ในรุ่นการเผยแพร่ก่อน ๆ อีกด้วย ถ้าคุณกำลังใช้ Power BI Report Server เวอร์ชันก่อนเดือนตุลาคม 2020 โปรดดูที่[เปลี่ยนสตริงการเชื่อมต่อแหล่งข้อมูลในรายงาน Power BI ด้วย PowerShell - Power BI Report Server ก่อนเดือนตุลาคม 2020](connect-data-source-apis-pre-oct-2020.md)

## <a name="prerequisites"></a>สิ่งที่จำเป็นต้องมี
- ดาวน์โหลดเดือนตุลาคม๒๐๒๐หรือรุ่นที่ใหม่กว่าของ[เซิร์ฟเวอร์รายงาน Power BI และ Power BI Desktop สำหรับเซิร์ฟเวอร์รายงาน Power BI](https://powerbi.microsoft.com/report-server/)
- รายงานที่บันทึกด้วยการเผยแพร่เดือนตุลาคม๒๐๒๐หรือรุ่นที่ใหม่กว่าของ Power BI Desktop ที่ปรับให้เหมาะสมสำหรับเซิร์ฟเวอร์รายงานด้วย **เมตาดาต้าชุดข้อมูล** ที่ได้รับการสนับสนุน
- รายงานที่ใช้การเชื่อมต่อแบบกำหนดพารามิเตอร์ เฉพาะรายงานที่มีการเชื่อมต่อและฐานข้อมูลแบบกำหนดพารามิเตอร์เท่านั้นที่สามารถอัปเดตได้หลังจากเผยแพร่
- ตัวอย่างนี้ใช้เครื่องมือ Reporting Services PowerShell คุณสามารถทำสิ่งเดียวกันนี้ได้โดยใช้ REST API ใหม่

## <a name="create-a-report-with-parameterized-connections"></a>สร้างรายงานที่มีการเชื่อมต่อแบบกำหนดพารามิเตอร์
    
1. สร้างการเชื่อมต่อ SQL Server ไปยังเซิร์ฟเวอร์ ในตัวอย่างด้านล่าง เรากำลังเชื่อมต่อกับ localhost ในฐานข้อมูลที่เรียกว่า ReportServer และดึงข้อมูลจาก ExecutionLog

    :::image type="content" source="media/connect-data-source-apis/sql-server-connect-database.png" alt-text="เชื่อมต่อไปยังฐานข้อมูล SQL Server":::

    ต่อไปนี้เป็นลักษณะของคิวรี M:

    ```
    let
        Source = Sql.Database("localhost", "ReportServer"),
        dbo_ExecutionLog3 = Source{[Schema="dbo",Item="ExecutionLog3"]}[Data]
    in
        dbo_ExecutionLog3
    ```

2. เลือก **จัดการพารามิเตอร์** ในริบบอนตัวแก้ไข Power Query

    :::image type="content" source="media/connect-data-source-apis/power-query-manage-parameters.png" alt-text="เลือกจัดการพารามิเตอร์":::

1.  สร้างพารามิเตอร์สำหรับชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูล

    :::image type="content" source="media/connect-data-source-apis/report-server-manage-parameters.png" alt-text="จัดการพารามิเตอร์ ตั้งชื่อเซิร์ฟเวอร์และชื่อฐานข้อมูล":::


3. แก้ไขคิวรีสำหรับการเชื่อมต่อครั้งแรกและแมปฐานข้อมูลและชื่อเซิร์ฟเวอร์

    :::image type="content" source="media/connect-data-source-apis/report-server-map-database-server.png" alt-text="แมปชื่อเซิร์ฟเวอร์และฐานข้อมูล":::

    ตอนนี้คิวรีมีลักษณะดังนี้:

    ```
    let
        Source = Sql.Database(ServerName, Databasename),
        dbo_ExecutionLog3 = Source{[Schema="dbo",Item="ExecutionLog3"]}[Data]
    in
        dbo_ExecutionLog3
    ```
    
    4. เผยแพร่รายงานนั้นไปยังเซิร์ฟเวอร์ ในตัวอย่างนี้ รายงานมีชื่อว่า executionlogparameter รูปภาพต่อไปนี้เป็นตัวอย่างของหน้าการจัดการแหล่งข้อมูล

    :::image type="content" source="media/connect-data-source-apis/report-server-manage-data-source-credentials.png" alt-text="หน้าการจัดการแหล่งข้อมูล":::

## <a name="update-parameters-using-the-powershell-tools"></a>อัปเดตพารามิเตอร์โดยใช้เครื่องมือ PowerShell

1. เปิด PowerShell และติดตั้งเครื่องมือ Reporting Services ล่าสุดโดยทำตามคำแนะนำที่ [https://github.com/microsoft/ReportingServicesTools](https://github.com/microsoft/ReportingServicesTools)
    
2.  เมื่อต้องการรับพารามิเตอร์สำหรับรายงาน ให้ใช้ REST DataModelParameters API ใหม่โดยใช้การเรียกของ PowerShell ต่อไปนี้:

    ```powershell
    Get-RsRestItemDataModelParameters '/executionlogparameter'

        Name         Value
        ----         -----
        ServerName   localhost
        Databasename ReportServer
    ```

3. เราบันทึกผลลัพธ์ของการเรียกนี้ในตัวแปร:

    ```powershell
    $parameters = Get-RsRestItemDataModelParameters '/executionlogparameter'
    ```

4. ตัวแปรนี้ได้รับการอัปเดตด้วยค่าที่เราต้องการเปลี่ยนแปลง
5. เราบันทึกผลลัพธ์ของการเรียกนี้ในตัวแปร:

    ```powershell
    $parameters[0].Value = 'myproductionserver'
    $parameters[1].Value = 'myproductiondatabase'
    ```

6. เราสามารถใช้ commandlet `Set-RsRestItemDataModelParameters` เพื่ออัปเดตค่าในเซิร์ฟเวอร์ด้วยค่าที่อัปเดต:

    ```powershell
    Set-RsRestItemDataModelParameters -RsItem '/executionlogparameter' -DataModelParameters $parameters
    ```

7. เมื่ออัปเดตพารามิเตอร์แล้ว เซิร์ฟเวอร์จะอัปเดตแหล่งข้อมูลใดก็ตามที่ผูกไว้กับพารามิเตอร์ ย้อนกลับไปยังกล่องโต้ตอบ **แก้ไขแหล่งข้อมูล** คุณควรจะสามารถตั้งค่าข้อมูลประจำตัวสำหรับเซิร์ฟเวอร์และฐานข้อมูลที่อัปเดตแล้ว

    :::image type="content" source="media/connect-data-source-apis/report-server-manage-executionlogparameter-dialog.png" alt-text="ตั้งค่าข้อมูลประจำตัวสำหรับเซิร์ฟเวอร์และฐานข้อมูลที่อัปเดตแล้ว":::

## <a name="next-steps"></a>ขั้นตอนถัดไป

[แหล่งข้อมูลรายงานที่มีการแบ่งหน้าในเซิร์ฟเวอร์รายงาน Power BI](connect-data-sources.md) 

มีคำถามเพิ่มเติมหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)
