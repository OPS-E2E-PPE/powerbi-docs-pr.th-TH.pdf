---
title: ข้อกำหนดฮาร์ดแวร์และซอฟต์แวร์สำหรับติดตั้งเซิร์ฟเวอร์รายงาน Power BI
description: บทความนี้จะให้คุณได้ดูข้อกำหนดขั้นต่ำของฮาร์ดแวร์และซอฟต์แวร์เพื่อใช้ในการติดตั้งเซิร์ฟเวอร์รายงาน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: conceptual
ms.date: 12/07/2020
ms.openlocfilehash: 10fb104d1c03ae5d08836b8e865178c347d848ce
ms.sourcegitcommit: 0bf42b6393cab7a37d21a52b934539cf300a08e2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/07/2020
ms.locfileid: "96781784"
---
# <a name="hardware-and-software-requirements-for-installing-power-bi-report-server"></a>ข้อกำหนดฮาร์ดแวร์และซอฟต์แวร์สำหรับติดตั้งเซิร์ฟเวอร์รายงาน Power BI

บทความนี้จะให้คุณได้ดูข้อกำหนดขั้นต่ำของฮาร์ดแวร์และซอฟต์แวร์เพื่อใช้ในการติดตั้งและเรียกใช้เซิร์ฟเวอร์รายงาน Microsoft Power BI

## <a name="processor-memory-and-operating-system-requirements"></a>ข้อกำหนดตัวประมวลผล หน่วยความจำ และระบบปฏิบัติการ

| คอมโพเนนต์ | ข้อกำหนด |
| --- | --- |
| .NET Framework |4.8<br><br>หากเซิร์ฟเวอร์ไม่มีการเข้าถึงอินเทอร์เน็ต คุณสามารถติดตั้ง .NET Framework จาก [Microsoft.NET Framework 4.8 (ตัวติดตั้งแบบออฟไลน์) สำหรับ Windows](https://support.microsoft.com/en-us/help/4503548/) ได้ด้วยตนเอง<br/><br/> สำหรับข้อมูลเพิ่มเติม คำแนะนำ และแนวทางเกี่ยวกับ .NET Framework 4.8 โปรดดู[คู่มือ .NET Framework Deployment สำหรับนักพัฒนา](/dotnet/framework/deployment/deployment-guide-for-developers)<br/><br/>Windows 8.1 และ Windows Server 2012 R2 จำเป็นต้องมี [KB2919355](https://support.microsoft.com/kb/2919355) ก่อนติดตั้ง .NET Framework 4.8 |
| ฮาร์ดดิสก์ |เซิร์ฟเวอร์รายงาน Power BI จำเป็นต้องมีเนื้อที่บนฮาร์ดดิสก์อย่างน้อย 1 กิกะไบต์<br><br>จะต้องเพิ่มเนื้อที่ว่างบนเซิร์ฟเวอร์ฐานข้อมูลที่โฮสต์ฐานข้อมูลของเซิร์ฟเวอร์รายงาน |
| หน่วยความจำ |**ต่ำสุด:** 1 GB<br/><br/> **แนะนำ:** อย่างน้อย 4 GB |
| ความเร็วในการประมวลผล |**ค่าต่ำสุด:** x64 ตัวประมวลผล: 1.4 GHz<br/><br/> **แนะนำ:** 2.0 GHz หรือเร็วกว่า |
| ชนิดตัวประมวลผล |x64 Processor: AMD Opteron, AMD Athlon 64, Xeon Intel with Intel EM64T support, IV Pentium Intel with EM64T support |
| ระบบปฏิบัติการ |Windows Server 2019 Datacenter<br><br>Windows Server 2019 Standard<br><br>Windows Server 2016 Datacenter<br><br>Windows Server 2016 Standard<br><br>Windows 10 Home<br><br>Windows 10 Professional<br><br>Windows 10 Enterprise<br> |

> [!NOTE]
> สนับสนุนการติดตั้งของเซิร์ฟเวอร์รายงาน Power BI บนตัวประมวลผล x64 เท่านั้น


## <a name="database-server-version-requirements"></a>ข้อกำหนดเวอร์ชันของเซิร์ฟเวอร์ฐานข้อมูล

SQL Server ถูกใช้เพื่อโฮสต์ฐานข้อมูลของเซิร์ฟเวอร์รายงาน สามารถมีอินสแตนซ์ของเครื่องมือฐานข้อมูล SQL Server ภายในเครื่องหรือระยะไกล ต่อไปนี้เป็นรุ่นของเครื่องมือฐานข้อมูล SQL Server ที่สามารถใช้โฮสต์ฐานข้อมูลของเซิร์ฟเวอร์รายงาน:

* อินสแตนซ์ที่มีการจัดการของ Azure SQL (เซิร์ฟเวอร์รายงาน Power BI เวอร์ชันมกราคม 2020 และเวอร์ชันที่ใหม่กว่า)
* SQL Server 2019
* SQL Server 2017
* SQL Server 2016
* SQL Server 2014
* SQL Server 2012

เมื่อคุณสร้างฐานข้อมูลรีพอร์ตเซิร์ฟเวอร์ในคอมพิวเตอร์ระยะไกล คุณต้องกำหนดค่าการเชื่อมต่อเพื่อใช้บัญชีผู้ใช้โดเมนหรือบัญชีการบริการกับการเข้าถึงเครือข่าย ถ้าคุณตัดสินใจที่จะใช้กับอินสแตนซ์ SQL Server ระยะไกล พิจารณาอย่างรอบคอบว่าเซิร์ฟเวอร์รายงานควรใช้ข้อมูลประจำตัวใดเพื่อเชื่อมต่อกับอินสแตนซ์ของ SQL Server สำหรับข้อมูลเพิ่มเติม ดู[กำหนดค่าการเชื่อมต่อฐานข้อมูลของเซิร์ฟเวอร์รายงาน](/sql/reporting-services/install-windows/configure-a-report-server-database-connection-ssrs-configuration-manager)

## <a name="considerations"></a>ข้อควรพิจารณา

เซิร์ฟเวอร์รายงาน Power BI จะติดตั้งค่าเริ่มต้นเป็นการตั้งค่าหลัก ซึ่งจำเป็นในการทำให้เซิร์ฟเวอร์รายงานสามารถใช้งานได้ มีข้อกำหนดดังต่อไปนี้:

* ภาษาที่ได้รับการสนับสนุนสำหรับเซิร์ฟเวอร์รายงาน Power BI คือ-อังกฤษ, เยอรมัน, สเปน, ญี่ปุ่น, อิตาลี, ฝรั่งเศส, รัสเซีย, จีนกลาง, จีนดั้งเดิม, โปรตุเกสบราซิล, เกาหลี
* กลไกจัดการฐานข้อมูล SQL Server ต้องพร้อมใช้งานหลังจากการติดตั้งและก่อนที่คุณจะกำหนดค่าฐานข้อมูลสำหรับเซิร์ฟเวอร์รายงาน อินสแตนซ์ Database Engine จะโฮสต์ฐานข้อมูลของเซิร์ฟเวอร์รายงานที่ Reporting Services Configuration Manager เป็นผู้สร้าง Database Engine ไม่จำเป็นสำหรับการติดตั้งค่าจริง
* [ฟีเจอร์ของ Reporting Services ที่รองรับโดยรุ่นต่างๆ ของ SQL Server](/sql/reporting-services/reporting-services-features-supported-by-the-editions-of-sql-server-2016) จะสรุปความแตกต่างระหว่างรุ่นต่างๆ ของ SQL Server เอาไว้
* บัญชีผู้ใช้ที่เรียกใช้การตั้งค่าต้องเป็นสมาชิกกลุ่มผู้ดูแลระบบของท้องถิ่น
* บัญชีผู้ใช้ที่เรียกใช้ Reporting Services Configuration Manager ต้องมีสิทธิ์ใช้งานในการเข้าถึงและสร้างฐานข้อมูลในอินสแตนซ์กลไกจัดการฐานข้อมูลที่โฮสต์ฐานข้อมูลของรีพอร์ตเซิร์ฟเวอร์อยู่
* การติดตั้งต้องสามารถใช้ค่าเริ่มต้นเพื่อจอง URL ที่จะทำให้เข้าถึงเซิร์ฟเวอร์รายงานและพอร์ทัลเว็บ ค่าเหล่านี้คือพอร์ต 80 และอักขระตัวแทนที่คาดเดายาก และชื่อไดเรกทอรีเสมือนในรูปแบบ **ReportServer** และ **รายงาน**

## <a name="read-only-domain-controller-rodc"></a>ตัวควบคุมโดเมนแบบอ่านอย่างเดียว (RODC)

 คุณสามารถติดตั้งรีพอร์ตเซิร์ฟเวอร์ในสภาพแวดล้อมที่มีตัวควบคุมโดเมนแบบอ่านอย่างเดียว (RODC) ได้ อย่างไรก็ตาม บริการรายงานต้องเข้าถึงตัวควบคุมโดเมนแบบอ่านและเขียน เพื่อให้ทำงานได้ปกติ ถ้า Reporting Services สามารถเข้าถึง RODC ได้เท่านั้นคุณอาจพบข้อผิดพลาดเมื่อพยายามจัดการบริการ

## <a name="power-bi-reports-and-analysis-services-live-connections"></a>การเชื่อมต่อสดของรายงาน Power BI และ Analysis Services

คุณสามารถใช้การเชื่อมต่อสดกับอินสแตนซ์ตารางหรืออินสแตนซ์หลายมิติ เซิร์ฟเวอร์ Analysis Services ของคุณต้องเป็นเวอร์ชันและรุ่นที่เหมาะสมเพื่อให้ทำงานได้ถูกต้อง

| **รุ่นของเซิร์ฟเวอร์** | **SKU ที่จำเป็นต้องมี** |
| --- | --- |
| 2012 SP1 CU4 หรือใหม่กว่า |เทคโนโลยีสำหรับการรวบรวมข้อมูล จัดเก็บ วิเคราะห์ และการเข้าถึงข้อมูล รวมถึงการดูในหลากหลายมุมมอง (BI) และ SKU องค์กร |
| 2014 |เทคโนโลยีสำหรับการรวบรวมข้อมูล จัดเก็บ วิเคราะห์ และการเข้าถึงข้อมูล รวมถึงการดูในหลากหลายมุมมอง (BI) และ SKU องค์กร |
| 2016 และเวอร์ชันที่ใหม่กว่า |SKU มาตรฐาน หรือสูงกว่า |

## <a name="next-steps"></a>ขั้นตอนถัดไป

[เซิร์ฟเวอร์รายงาน Power BI คืออะไร](get-started.md)  
[ภาพรวมของผู้ดูแลระบบ](admin-handbook-overview.md)  
[ติดตั้ง Power BI Report Server](install-report-server.md)  
[ดาวน์โหลดตัวสร้างรายงาน](https://www.microsoft.com/download/details.aspx?id=53613)  
[ดาวน์โหลด SQL Server Data Tools (SSDT)](/sql/ssdt/download-sql-server-data-tools-ssdt)

มีคำถามเพิ่มเติมหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)
