---
title: การตรวจสอบการอ้างอิงข้อมูล Power BI Embedded
description: วัสดุอ้างอิงที่สำคัญที่จำเป็นเมื่อคุณตรวจสอบ Power BI Embedded
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: how-to
ms.date: 01/14/2021
ms.openlocfilehash: fc6b9dd4d50d665211324d1b6c05e62468fc034d
ms.sourcegitcommit: 77912d4f6ef2a2b1ef8ffccc50691fe5b38ee97a
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 01/22/2021
ms.locfileid: "98690810"
---
# <a name="monitoring-power-bi-embedded-data-reference"></a>การตรวจสอบการอ้างอิงข้อมูล Power BI Embedded

ดูการ [ตรวจสอบ Power BI Embedded](monitor-power-bi-embedded.md) สำหรับรายละเอียดเกี่ยวกับการรวบรวมและวิเคราะห์ข้อมูลการตรวจสอบสำหรับ Power BI Embedded

## <a name="metrics"></a>เมตริก

ในส่วนนี้จะแสดงรายการเมตริกแพลตฟอร์มที่รวบรวมทั้งหมดที่รวบรวมไว้โดยอัตโนมัติสำหรับ Power BI Embedded  

|ชนิดการวัด | Namespace/ประเภทของผู้ให้บริการทรัพยากร<br/> และเชื่อมโยงไปยังเมตริกแต่ละรายการ |
|-------|-----|
| ความจุ | [PowerBIDedicated/ความจุของ Microsoft](/azure/azure-monitor/platform/metrics-supported#microsoftpowerbidedicatedcapacities) |

### <a name="capacities"></a>ความจุ

ผู้ให้บริการทรัพยากรและชนิด: [PowerBIDedicated/ความจุ](/azure/azure-monitor/platform/metrics-supported#microsoftpowerbidedicatedcapacities)

| ชื่อ | เมตริก | หน่วย | คำอธิบาย |
|:---|:-------|:-----|:------------|
|หน่วยความจำ (Storage) |memory_metric               |ไบต์        |หน่วยความจำ . ช่วง 0-3 GB สำหรับ A1, 0-5 GB สำหรับ A2, 0-10 GB สำหรับ A3, 0-25 GB สำหรับ A4, 0-50 GB สำหรับ A5 และ 0-100 GB สำหรับ A6 ได้รับการสนับสนุนเฉพาะสำหรับทรัพยากรที่สร้าง Power BI Embedded 1 |
|หน่วยความจำแธรชชิ่ง (ชุดข้อมูล) (Storage) |memory_thrashing_metric     |เปอร์เซ็นต์      |แธรชชิ่งหน่วยความจำโดยเฉลี่ย ได้รับการสนับสนุนเฉพาะสำหรับทรัพยากรที่สร้าง Power BI Embedded 1 |
|การใช้ประโยชน์ QPU สูง (Storage) |qpu_high_utilization_metric |Count        |QPU การใช้งานสูงในนาทีสุดท้าย1สำหรับการใช้ประโยชน์ QPU สูงหรือ0 ได้รับการสนับสนุนเฉพาะสำหรับทรัพยากรที่สร้าง Power BI Embedded 1 |
|ระยะเวลาแบบสอบถาม (ชุดข้อมูล) (Storage) |QueryDuration               |ลลิวินาที |ระยะเวลาแบบสอบถาม DAX ในช่วงที่ผ่านมา ได้รับการสนับสนุนเฉพาะสำหรับทรัพยากรที่สร้าง Power BI Embedded 1 |
|ความยาวคิวงานพูลการสอบถาม (ชุดข้อมูล) (Storage) |QueryPoolJobQueueLength     |Count        |จำนวนงานในคิวของพูลโปรแกรมเธรดแบบสอบถาม ได้รับการสนับสนุนเฉพาะสำหรับทรัพยากรที่สร้าง Power BI Embedded 1 |

## <a name="metric-dimensions"></a>มิติเมตริก

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับมิติการวัดใดให้ดู[เมตริกแบบหลายมิติ](/azure/azure-monitor/platform/data-platform-metrics#multi-dimensional-metrics)

Power BI Embedded ไม่มีเมตริกใดๆที่ประกอบด้วยมิติ

## <a name="resource-logs"></a>บันทึกทรัพยากร

ส่วนนี้แสดงรายการชนิดของบันทึกทรัพยากรที่คุณสามารถรวบรวมสำหรับ Power BI Embedded ได้

สำหรับการอ้างอิงดูรายการของ[ชนิดประเภทบันทึกทรัพยากรทั้งหมดที่ได้รับการสนับสนุนในตัวตรวจสอบ Azure](/azure/azure-monitor/platform/resource-logs-schema)

ส่วนนี้แสดงรายการชนิดของประเภทแฟ้มบันทึกทรัพยากรทั้งหมดที่รวบรวมสำหรับ Power BI Embedded  

|ชนิดแฟ้มบันทึกทรัพยากร | Namespace/ประเภทของผู้ให้บริการทรัพยากร<br/> และเชื่อมโยงไปยังเมตริกแต่ละรายการ |
|-------|-----|
| ความจุ | [PowerBIDedicated/ความจุของ Microsoft](/azure/azure-monitor/platform/resource-logs-categories#microsoftpowerbidedicatedcapacities) |

## <a name="azure-monitor-logs-tables"></a>ตารางบันทึกการตรวจสอบ Azure

ในหัวข้อนี้อ้างอิงถึงตารางทั้งหมดของ Azure Monitor บันทึก Kusto ที่เกี่ยวข้องกับ Power BI Embedded และพร้อมใช้งานสำหรับแบบสอบถามโดยการวิเคราะห์การเข้าสู่ระบบ

|ชนิดของทรัพยากร | บันทึกย่อ |
|-------|-----|
| [Power BI Embedded](/azure/azure-monitor/reference/tables/tables-resourcetype#power-bi-embedded) |ดูรายการของตารางด้านล่าง |

### <a name="power-bi-embedded"></a>Power BI แบบฝังตัว

| ตาราง |  คำอธิบาย |
|:---------|:-------------|------------------|
| [AzureActivity](/azure/azure-monitor/reference/tables/azureactivity) | รายการจากบันทึกกิจกรรม Azure ที่ให้ข้อมูลเชิงลึกลงในเหตุการณ์ระดับกลุ่มการสมัครใช้งานหรือการจัดการใดๆที่เกิดขึ้นใน Azure    |                             |                                                   | 
| [AzureDiagnostics](/azure/azure-monitor/reference/tables/azurediagnostics)   | จัดเก็บบันทึกทรัพยากรสำหรับบริการ Azure ที่ใช้โหมดการวินิจฉัยของ Azure บันทึกทรัพยากรอธิบายการดำเนินการภายในของทรัพยากร Azure |
| [AzureMetrics](/azure/azure-monitor/reference/tables/azuremetrics)   | ข้อมูลการวัดที่ออกโดยบริการของ Azure ที่วัดสุขภาพและประสิทธิภาพการทำงานของพวกเขา |

สำหรับการอ้างอิงทั้งหมดของ Azure Monitor บันทึก/บันทึกการวิเคราะห์ตารางให้ดูการ[อ้างอิงตารางบันทึกของตัวตรวจสอบ azure](/azure/azure-monitor/reference/tables/tables-resourcetype)

## <a name="activity-log"></a>บันทึกกิจกรรม

คุณสามารถเลือกประเภท **กลไก** / **AllMetrics** ได้

### <a name="engine"></a>กลไกจัดการ

ประเภทกลไกจะแนะนำให้ทรัพยากรในการบันทึกเหตุการณ์ที่แสดงด้านล่าง สำหรับแต่ละเหตุการณ์มีคุณสมบัติ

|     ชื่อเหตุการณ์     |     คำอธิบายเหตุการณ์     |
|----------------------------|----------------------------------------------------------------------------------|
|    เข้าสู่ระบบการตรวจสอบ    |    บันทึกการเชื่อมต่อใหม่ทั้งหมดลงในเหตุการณ์กลไกจัดการตั้งแต่เริ่มต้นใช้งานการติดตาม    |
|    เตรียมใช้งานเซสชัน    |    บันทึกเหตุการณ์เริ่มต้นเซสชันทั้งหมดตั้งแต่เริ่มต้นใช้งานการติดตาม    |
|    เริ่มต้นคิวรี Vertipaq    |    บันทึกเหตุการณ์เริ่มต้นคิวรี VertiPaq SE ทั้งหมด ตั้งแต่เริ่มต้นใช้งานการติดตาม    |
|    เริ่มต้นคิวรี    |    บันทึกเหตุการณ์เริ่มต้นคิวรีทั้งหมด ตั้งแต่เริ่มต้นใช้งานการติดตาม    |
|    คิวรีสิ้นสุด    |    บันทึกเหตุการณ์สิ้นสุดคิวรีทั้งหมด ตั้งแต่เริ่มต้นใช้งานการติดตาม    |
|    คิวรี Vertipaq สิ้นสุด    |    บันทึกเหตุการณ์สิ้นสุดคิวรี VertiPaq SE ทั้งหมด ตั้งแต่เริ่มต้นใช้งานการติดตาม    |
|    ออกจากระบบการตรวจสอบ    |    บันทึกเหตุการณ์ยกเลิกการเชื่อมจากกลไกจัดการทั้งหมดตั้งแต่เริ่มต้นใช้งานการติดตาม    |
|    ข้อผิดพลาด    |    บันทึกเหตุการณ์ข้อผิดพลาดโปรแกรมทั้งหมดตั้งแต่เริ่มต้นใช้งานการติดตาม    |

#### <a name="event-example"></a>ตัวอย่างเหตุการณ์

ตารางด้านล่างแสดงตัวอย่างเหตุการณ์

| ชื่อคุณสมบัติ | ตัวอย่างสิ้นสุดคิวรี Vertipaq | คำอธิบายคุณสมบัติ |
|---|---|---|
| EventClass | XM_SEQUERY_END | คลาสเหตุการณ์ถูกใช้เพื่อจัดประเภทเหตุการณ์ |
| EventSubclass | 0 | เหตุการณ์คลาสย่อยกิจกรรมมีข้อมูลเพิ่มเติมเกี่ยวกับแต่ละคลาสกิจกรรม (ตัวอย่าง 0: สแกน VertiPaq) |
| RootActivityId | ff217fd2-611d-43c0-9c12-19e202a94f70 | ID กิจกรรมราก |
| CurrentTime | 2018-04-06T18:30:11.9137358Z | เวลาที่เหตุการณ์เริ่มต้นเมื่อพร้อมใช้งาน |
| startTime | 2018-04-06T18:30:11.9137358Z | เวลาที่เหตุการณ์เริ่มต้นเมื่อพร้อมใช้งาน |
| JobID | 0 | ID งานสำหรับความคืบหน้า |
| ObjectID | 464 | ID ของออบเจ็กต์ |
| ObjectType | 802012 | ObjectType |
| เวลาสิ้นสุด | 2018-04-06T18:30:11.9137358Z | เวลาที่เหตุการณ์สิ้นสุด |
| ระยะเวลา | 0 | ระยะเวลา (ในหน่วยมิลลิวินาที) ที่ใช้โดยกิจกรรม |
| SessionType | User | ประเภทเซสชัน (เอนทิตีใดที่เป็นเหตุให้เกิดการดำเนินการ) |
| ProgressTotal | 0 | ความคืบหน้าทั้งหมด |
| IntegerData | 0 | ข้อมูลจำนวนเต็ม |
| ความรุนแรง | 0 | ระดับความรุนแรงของข้อยกเว้น |
| ความสำเร็จ | 1 | 1 = สำเร็จ 0 = ล้มเหลว (ตัวอย่างเช่น 1 หมายถึงการตรวจสอบสิทธิ์เสร็จเรียบร้อยแล้ว และ 0 หมายถึงการตรวจสอบล้มเหลว) |
| ข้อผิดพลาด | 0 | จำนวนข้อผิดพลาดของกิจกรรมที่ให้ไว้ |
| ConnectionID | 3 | ID การเชื่อมต่อเฉพาะ |
| DatasetID | 5eaa550e-06ac-4adf-aba9-dbf0e8fd1527 | ID ของฐานข้อมูลที่คำสั่งของผู้ใช้กำลังทำงานอยู่ |
| SessionID | 3D063F66-A111-48EE-B960-141DEBDA8951 | GUID เซสชัน |
| SPID | 180 | ID กระบวนการของเซิร์ฟเวอร์ ซึ่งระบุเซสชันผู้ใช้โดยเฉพาะ ซึ่งสอดคล้องกับเซสชัน GUID ที่ใช้ โดย XML/a โดยตรง |
| ClientProcessID | null | ID กระบวนการของแอปพลิเคชันไคลเอ็นต์ |
| ApplicationName | null | ชื่อของแอปพลิเคชันไคลเอ็นต์ที่สร้างการเชื่อมต่อกับเซิร์ฟเวอร์ |
| CapacityName | pbi641fb41260f84aa2b778a85891ae2d97 | ชื่อของทรัพยากรความจุ Power BI Embedded |

### <a name="allmetrics"></a>AllMetrics

ตรวจสอบตัวเลือก **AllMetrics** บันทึกข้อมูลของเมตริกทั้งหมดที่คุณสามารถใช้กับทรัพยากร Power BI Embedded

ตารางต่อไปนี้แสดงรายการการดำเนินการที่เกี่ยวข้องกับ Power BI Embedded ที่อาจถูกสร้างขึ้นในบันทึกกิจกรรม

## <a name="schemas"></a>Schema

Power BI Embedded ใช้ schema แบบ **เฉพาะของ POWER BI**

## <a name="next-steps"></a>ขั้นตอนถัดไป

>[!div class="nextstepaction"]
>[ตรวจสอบ Azure Power BI Embedded](monitor-power-bi-embedded.md)

>[!div class="nextstepaction"]
>[บันทึกการวินิจฉัยทรัพยากร azure](/azure/monitoring-and-diagnostics/monitoring-overview-of-diagnostic-logs)

>[!div class="nextstepaction"]
>[ชุด-AzureRmDiagnosticSetting](/powershell/module/azurerm.insights/Set-AzureRmDiagnosticSetting)