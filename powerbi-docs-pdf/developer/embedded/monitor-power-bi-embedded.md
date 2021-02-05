---
title: ตรวจสอบ Power BI Embedded
description: เริ่มต้นที่นี่เพื่อเรียนรู้วิธีการตรวจสอบ Power BI Embedded
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: how-to
ms.date: 01/14/2021
ms.openlocfilehash: 1b8ebbd7913bc5763f9f4dd8576fbc4783e8d531
ms.sourcegitcommit: 77912d4f6ef2a2b1ef8ffccc50691fe5b38ee97a
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 01/22/2021
ms.locfileid: "98690796"
---
# <a name="monitor-power-bi-embedded"></a>ตรวจสอบ Power BI Embedded

เมื่อคุณมีแอปพลิเคชันและกระบวนการทางธุรกิจที่สำคัญอาศัยแหล่งข้อมูล Azure คุณต้องการตรวจสอบแหล่งข้อมูลเหล่านั้นสำหรับความพร้อมใช้งานประสิทธิภาพการทำงานและการดำเนินการของพวกเขา บทความนี้อธิบายการตรวจสอบข้อมูลที่สร้างขึ้นโดย Power BI Embedded และวิธีการที่คุณสามารถใช้คุณลักษณะของ Azure Monitor เพื่อวิเคราะห์และแจ้งเตือนเกี่ยวกับข้อมูลนี้

## <a name="monitor-overview"></a>ภาพรวมของการตรวจสอบ

หน้า **ภาพรวม** ในพอร์ทัล Azure สำหรับแต่ละอินสแตนซ์ *Power BI Embedded* ประกอบด้วยข้อมูลต่อไปนี้:

* **กลุ่มทรัพยากร** - [กลุ่มทรัพยากร](/azure/azure-resource-manager/management/overview#resource-groups) ที่อินสแตนซ์เป็นสมาชิกอยู่
* **สถานะ** -สถานะของอินสแตนซ์ Power BI Embedded ของคุณ
* **ตำแหน่งที่** ตั้ง–ตำแหน่งที่ตั้งของอินสแตนซ์ Power BI Embedded ของคุณ
* **ชื่อทรัพยากร** -ชื่อของอินสแตนซ์ Power BI Embedded ของคุณ
* **Sku** -sku ที่อินสแตนซ์ Power BI Embedded ของคุณกำลังใช้
* **ชื่อการสมัคร** ใช้งาน-ชื่อการสมัครใช้งานอินสแตนซ์ Power BI Embedded ของคุณ
* **Id การสมัคร** ใช้งาน-id การสมัครใช้งานอินสแตนซ์ Power BI Embedded ของคุณ

## <a name="what-is-azure-monitor"></a>ตัวตรวจสอบ Azure คืออะไร

*Power BI Embedded* สร้างการตรวจสอบข้อมูลโดยใช้ตัว [ตรวจสอบ azure](/azure/azure-monitor/overview)ซึ่งเป็นบริการการตรวจสอบแบบสแต็คทั้งหมดใน Azure ที่ให้ชุดของคุณลักษณะทั้งหมดในการตรวจสอบแหล่งข้อมูล Azure ของคุณนอกเหนือจากแหล่งข้อมูลในเมฆและภายในองค์กร

เริ่มต้นด้วยบทความการ [ตรวจสอบทรัพยากร azure ด้วย Azure Monitor](/azure/azure-monitor/insights/monitor-azure-resource)ซึ่งอธิบายแนวคิดต่อไปนี้:

- ตัวตรวจสอบ Azure คืออะไร
- ค่าใช้จ่ายที่เกี่ยวข้องกับการตรวจสอบ
- การตรวจสอบข้อมูลที่รวบรวมใน Azure
- กำลังกำหนดค่าคอลเลกชันข้อมูล
- เครื่องมือมาตรฐานใน Azure สำหรับการวิเคราะห์และการแจ้งเตือนเกี่ยวกับการตรวจสอบข้อมูล

ส่วนต่อไปนี้สร้างในบทความนี้โดยการอธิบายข้อมูลเฉพาะที่รวบรวมสำหรับ Power BI Embedded และให้ตัวอย่างสำหรับการกำหนดค่าคอลเลกชันข้อมูลและวิเคราะห์ข้อมูลนี้ด้วยเครื่องมือ Azure

## <a name="monitoring-data"></a>การตรวจสอบข้อมูล

Power BI Embedded จะรวบรวมข้อมูลการตรวจสอบชนิดเดียวกันกับทรัพยากร Azure อื่นๆที่อธิบายไว้ในการ[ตรวจสอบข้อมูลจากแหล่งข้อมูล azure](/azure/azure-monitor/insights/monitor-azure-resource#monitoring-data-from-Azure-resources)

ดูการ [ตรวจสอบ *Power BI Embedded* การอ้างอิงข้อมูล](monitor-power-bi-embedded-reference.md) สำหรับข้อมูลโดยละเอียดเกี่ยวกับเมตริกและเมทริกซ์การบันทึกที่สร้างขึ้นโดย Power BI Embedded

## <a name="collection-and-routing"></a>คอลเลกชันและการกำหนดเส้นทาง

เมตริกของแพลตฟอร์มและบันทึกกิจกรรมจะถูกเก็บรวบรวมและจัดเก็บไว้โดยอัตโนมัติแต่สามารถกำหนดเส้นทางไปยังตำแหน่งที่ตั้งอื่นโดยใช้การตั้งค่าการวินิจฉัย  

ไม่มีการรวบรวมบันทึกทรัพยากรและจัดเก็บไว้จนกว่าคุณจะสร้างการตั้งค่าการวินิจฉัยและกำหนดเส้นทางไปยังตำแหน่งที่ตั้งอย่างน้อยหนึ่งแห่ง

ดู [สร้างการตั้งค่าการวินิจฉัยเพื่อรวบรวมบันทึกและเมตริกของแพลตฟอร์มใน Azure](/azure/azure-monitor/platform/diagnostic-settings) สำหรับขั้นตอนโดยละเอียดสำหรับการสร้างการตั้งค่าการวินิจฉัยโดยใช้พอร์ทัล AZURE, CLI หรือ PowerShell เมื่อคุณสร้างการตั้งค่าการวินิจฉัยคุณระบุประเภทของบันทึกที่จะรวบรวม ประเภทสำหรับ *Power BI Embedded* จะแสดงอยู่ใน [Power BI Embedded การตรวจสอบข้อมูลอ้างอิง](monitor-power-bi-embedded-reference.md#resource-logs)

### <a name="using-powershell-to-enable-diagnostics"></a>ใช้ PowerShell เพื่อเปิดใช้งานการวินิจฉัย

เมื่อต้องการเปิดใช้งานการบันทึกเมตริกและการวินิจฉัยโดยใช้ PowerShell ให้ใช้คำสั่งที่แสดงไว้ด้านล่าง หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับการใช้ PowerShell เพื่อเปิดใช้งานการวินิจฉัยให้ดู[สร้างและกำหนดค่าพื้นที่ทำงานการวิเคราะห์บันทึกใน Azure Monitor โดยใช้ PowerShell](/azure/azure-monitor/platform/powershell-workspace-configuration)

* เมื่อต้องการเปิดใช้งานการเก็บข้อมูลของแฟ้มบันทึกการวินิจฉัยในบัญชีเก็บข้อมูล ให้ใช้คำสั่งนี้:

    ```powershell
    Set-AzureRmDiagnosticSetting -ResourceId [your resource id] -StorageAccountId [your storage account id] -Enabled $true
    ```
    ID บัญชีที่เก็บข้อมูลเป็น ID ทรัพยากรสำหรับบัญชีเก็บข้อมูลที่คุณต้องการส่งบันทึก

* เมื่อต้องการเปิดใช้งานสตรีมของแฟ้มบันทึกการวินิจฉัยไปยังฮับเหตุการณ์ ให้ใช้คำสั่งนี้:

    ```powershell
    Set-AzureRmDiagnosticSetting -ResourceId [your resource id] -ServiceBusRuleId [your service bus rule id] -Enabled $true
    ```
* ID กฎ Azure Service Bus คือสตริงที่มีรูปแบบนี้:

    ```powershell
    {service bus resource ID}/authorizationrules/{key name}
    ```

* เมื่อต้องการเปิดใช้งานการส่งบันทึกการวินิจฉัยไปยังพื้นที่ทำงาน Log Analytics ให้ใช้คำสั่งนี้:

    ```powershell
        Set-AzureRmDiagnosticSetting -ResourceId [your resource id] -WorkspaceId [resource id of the log analytics workspace] -Enabled $true
    ```

* คุณสามารถขอรับ ID ทรัพยากรของพื้นที่ทำงาน Log Analytics ของคุณ โดยใช้คำสั่งต่อไปนี้:

    ```powershell
    (Get-AzureRmOperationalInsightsWorkspace).ResourceId
    ```

คุณสามารถรวมพารามิเตอร์เหล่านี้เข้าด้วยกันเพื่อเปิดใช้งานผลลัพธ์หลายตัวเลือก

เมตริกและบันทึกที่คุณสามารถรวบรวมได้จะกล่าวถึงในส่วนต่อไปนี้

## <a name="analyzing-metrics"></a>การวิเคราะห์เมตริก

คุณสามารถวิเคราะห์เมตริกสำหรับ *Power BI Embedded* ที่มีเมตริกจาก Azure services อื่นโดยใช้เมทริกซ์ตัวชี้วัดโดยการเปิดการ **วัด** จากเมนูตัว **ตรวจสอบ Azure** ดู [การเริ่มต้นใช้งาน Azure เมตริก Explorer](/azure/azure-monitor/platform/metrics-getting-started) สำหรับรายละเอียดเกี่ยวกับการใชเครื่องมือนี้

สำหรับรายการของเมตริกของแพลตฟอร์มที่รวบรวมสำหรับ Power BI Embedded ดูการ [ตรวจสอบการวัดข้อมูลอ้างอิง *Power BI Embedded*](monitor-power-bi-embedded-reference.md#metrics)  

สำหรับการอ้างอิงคุณสามารถดูรายการของ[เมตริกทรัพยากรทั้งหมดที่ได้รับการสนับสนุนในตัวตรวจสอบ Azure](/azure/azure-monitor/platform/metrics-supported)

## <a name="analyzing-logs"></a>การวิเคราะห์บันทึก

ข้อมูลในบันทึกการตรวจสอบ Azure จะถูกจัดเก็บไว้ในตารางที่แต่ละตารางมีชุดคุณสมบัติที่ไม่ซ้ำกันของตนเอง  

บันทึกทรัพยากรทั้งหมดในตัวตรวจสอบ Azure มีเขตข้อมูลเดียวกันตามด้วยเขตข้อมูลเฉพาะบริการ Schema ทั่วไปมีการระบุไว้ใน[schema ของแฟ้มบันทึกของตัวตรวจสอบ Azure resource](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-logs-schema#top-level-resource-logs-schema) schema สำหรับแฟ้มบันทึกทรัพยากร Power BI Embedded พบในการ[อ้างอิงข้อมูล Power BI Embedded](monitor-power-bi-embedded-reference.md#schemas)

[บันทึกกิจกรรม](/azure/azure-monitor/platform/activity-log)คือ Azure เข้าสู่ระบบแพลตฟอร์มที่ให้ข้อมูลเชิงลึกลงในเหตุการณ์ระดับการสมัครใช้งาน คุณสามารถดูได้อย่างอิสระหรือเส้นทางไปยังบันทึกการตรวจสอบ Azure ซึ่งคุณสามารถทำแบบสอบถามที่ซับซ้อนมากขึ้นได้โดยใช้การวิเคราะห์บันทึก  

สำหรับรายการของชนิดของบันทึกทรัพยากรที่รวบรวมสำหรับ Power BI Embedded ดูการ [ตรวจสอบการอ้างอิงข้อมูล Power BI Embedded](monitor-power-bi-embedded-reference.md#resource-logs)  

สำหรับรายการของตารางที่ใช้โดย Azure Monitor Log และ queryable โดยการวิเคราะห์การเข้าสู่ระบบดูการ [ตรวจสอบการอ้างอิงข้อมูล Power BI Embedded](monitor-power-bi-embedded-reference.md#azure-monitor-logs-tables)  

### <a name="sample-kusto-queries"></a>ตัวอย่างแบบสอบถาม Kusto

> [!IMPORTANT]
> เมื่อคุณเลือก **บันทึก** จากเมนู Power BI Embedded การวิเคราะห์บันทึกจะเปิดขึ้นด้วยขอบเขตแบบสอบถามที่ตั้งค่าเป็นทรัพยากร Power BI Embedded ปัจจุบัน ซึ่งหมายความว่าแบบสอบถามบันทึกจะรวมข้อมูลจากทรัพยากรนั้นเท่านั้น ถ้าคุณต้องการเรียกใช้แบบสอบถามที่มีข้อมูลจากทรัพยากร Power BI Embedded อื่นๆหรือข้อมูลจากบริการอื่นๆของ Azure เลือก **บันทึก** จากเมนูตัว **ตรวจสอบ Azure** ดู [ล็อกขอบเขตของคิวรีและช่วงเวลาในการวิเคราะห์การบันทึกการตรวจสอบ Azure](/azure/azure-monitor/log-query/scope/) สำหรับรายละเอียด

ด้านล่างคือตัวอย่างแบบสอบถามสำหรับการตรวจสอบ Power BI Embedded

* นี่คือแบบสอบถามที่เสร็จสมบูรณ์ในเวลาน้อยกว่าห้านาที (๓๐๐,๐๐๐มิลลิวินาที)

    ```Kusto
        search *
        | where Type == "AzureDiagnostics"
        | where ( OperationName == "QueryEnd" )
        | where toint(Duration_s) < 300000   
    ```
* ระบุชื่อกำลังการผลิต

    ```Kusto
        search *
        | where Type == "AzureDiagnostics"
        | where ( OperationName == "QueryEnd" )
        | where toint(Duration_s) < 300000   
    ```

## <a name="alerts"></a>การแจ้งเตือน

การแจ้งเตือนการตรวจสอบ Azure จะแจ้งให้คุณทราบเมื่อพบเงื่อนไขที่สำคัญในข้อมูลการตรวจสอบของคุณ พวกเขาช่วยให้คุณสามารถระบุและแก้ไขปัญหาในระบบของคุณก่อนที่ลูกค้าของคุณจะสังเกตเห็นได้ คุณสามารถตั้งค่าการแจ้งเตือนบน[เมตริก](/azure/azure-monitor/platform/alerts-metric-overview)[บันทึก](/azure/azure-monitor/platform/alerts-unified-log)และ[บันทึกกิจกรรม](/azure/azure-monitor/platform/activity-log-alerts)

## <a name="next-steps"></a>ขั้นตอนถัดไป

คุณสามารถเรียนรู้เพิ่มเติมเกี่ยวกับบันทึกการวินิจฉัยทรัพยากร Azure

>[!div class="nextstepaction"]
>[การตรวจสอบการอ้างอิงข้อมูล Power BI Embedded](monitor-power-bi-embedded-reference.md)

>[!div class="nextstepaction"]
>[การตรวจสอบทรัพยากร Azure ด้วยตัวตรวจสอบ Azure](/azure/azure-monitor/insights/monitor-azure-resource)