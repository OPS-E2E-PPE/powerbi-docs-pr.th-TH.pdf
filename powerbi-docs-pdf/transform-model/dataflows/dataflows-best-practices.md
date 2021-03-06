---
title: แนวทางปฏิบัติที่ดีที่สุดสำหรับกระแสข้อมูล
description: คอลเลกชันของลิงก์แนวทางปฏิบัติที่ดีที่สุดและคำแนะนำสำหรับกระแสข้อมูล
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-dataflows
ms.topic: how-to
ms.date: 12/10/2020
LocalizationGroup: Data from files
ms.openlocfilehash: fb688b20fd8b5ee1288f670fba9f7f45fc058680
ms.sourcegitcommit: 1cad78595cca1175b82c04458803764ac36e5e37
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/19/2021
ms.locfileid: "98565364"
---
# <a name="dataflows-best-practices"></a>แนวทางปฏิบัติที่ดีที่สุดสำหรับกระแสข้อมูล

**กระแสข้อมูล** Power BI คือโซลูชันการเตรียมข้อมูลที่มุ่งเน้นองค์กร ทำให้เกิดระบบนิเวศของข้อมูลที่พร้อมสำหรับการใช้งาน การนำมาใช้ใหม่ และการรวมเข้าด้วยกัน บทความนี้แสดงรายการแนวทางปฏิบัติที่ดีที่สุดพร้อมลิงก์ไปยังบทความและข้อมูลอื่น ๆ ที่จะช่วยให้คุณเข้าใจและใช้กระแสข้อมูลได้อย่างเต็มประสิทธิภาพ

## <a name="dataflows-across-the-power-platform"></a>กระแสข้อมูลทั่วทั้ง Power Platform

กระแสข้อมูลสามารถใช้กับเทคโนโลยี Power Platform ต่าง ๆ เช่น Power Query, Microsoft Dynamics 365 และข้อเสนออื่น ๆ ของ Microsoft ได้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการทำงานของกระแสข้อมูลใน Power Platform โปรดดูที่[การใช้กระแสข้อมูลในผลิตภัณฑ์ต่าง ๆ ของ Microsoft](/power-query/dataflows/overview-dataflows-across-power-platform-dynamics-365)


## <a name="dataflows-best-practices-table-and-links"></a>ตารางและลิงก์แนวทางปฏิบัติที่ดีที่สุดสำหรับกระแสข้อมูล

ตารางต่อไปนี้มีคอลเลกชันของลิงก์ไปยังบทความที่อธิบายแนวทางปฏิบัติที่ดีที่สุดเมื่อสร้างหรือทำงานกับกระแสข้อมูล ลิงก์ประกอบด้วยข้อมูลเกี่ยวกับการพัฒนาตรรกะทางธุรกิจ การพัฒนากระแสข้อมูลที่ซับซ้อน การนำกระแสข้อมูลมาใช้ใหม่ และวิธีการทำให้ธุรกิจขนาดใหญ่บรรลุเป้าหมายด้วยกระแสข้อมูลของคุณ


|**หัวข้อ**  |**พื้นที่คำแนะนำ**  |**ลิงก์ไปยังบทความหรือเนื้อหา**  |
|---------|---------|---------|
|Power Query     | คำแนะนำและเคล็ดลับเพื่อให้ได้รับประโยชน์สูงสุดจากประสบการณ์การจัดระเบียบข้อมูลของคุณ        |[แนวทางปฏิบัติที่ดีที่สุดสำหรับ Power Query](/power-query/best-practices)        |
|การใช้ประโยชน์จากเอนทิตีที่คำนวณ     |มีประโยชน์ด้านประสิทธิภาพสำหรับการใช้เอนทิตีที่คำนวณในกระแสข้อมูล         |[สถานการณ์สำหรับเอนทิตีที่คำนวณแล้ว](/power-query/dataflows/computed-entities-scenarios)         |
|การพัฒนากระแสข้อมูลที่ซับซ้อน     |รูปแบบสำหรับการพัฒนากระแสข้อมูลขนาดใหญ่ที่มีประสิทธิภาพ         |[กระแสข้อมูลที่ซับซ้อน](/power-query/dataflows/best-practices-developing-complex-dataflows)         |
|การนำกระแสข้อมูลมาใช้ใหม่     |รูปแบบ คำแนะนำ และกรณีการใช้งาน         |[การนำกระแสข้อมูลมาใช้ใหม่](/power-query/dataflows/best-practices-reusing-dataflows)         |
|การนำไปปฏิบัติในขนาดใหญ่     |การใช้งานในขนาดใหญ่และคำแนะนำเพื่อทำให้สถาปัตยกรรมองค์กรเกิดความสมบูรณ์         |[คลังข้อมูลที่ใช้กระแสข้อมูล](/power-query/dataflows/best-practices-for-data-warehouse-using-dataflows)         |
|การใช้ประโยชน์จากการคำนวณขั้นสูง     |อาจปรับปรุงประสิทธิภาพกระแสข้อมูลได้ถึง 25x         |[กลไกการคำนวณขั้นสูง](dataflows-premium-workload-configuration.md#using-the-compute-engine-to-improve-performance)         |
|การเพิ่มประสิทธิภาพการตั้งค่าปริมาณงานของคุณ     |รับประโยชน์สูงสุดจากโครงสร้างพื้นฐานกระแสข้อมูลของคุณโดยทำความเข้าใจกับคันโยกที่คุณสามารถดึงเพื่อเพิ่มประสิทธิภาพสูงสุด         |[การกำหนดค่าปริมาณงานกระแสข้อมูล](dataflows-premium-workload-configuration.md)         |
|การเข้าร่วมและขยายตาราง     |การสร้างการเข้าร่วมที่มีประสิทธิภาพ         |[ปรับการขยายการทำงานของตารางให้เหมาะสม](/power-query/optimize-expanding-table-columns)         |
|คำแนะนำการพับคิวรี     |เร่งการแปลงโดยใช้ระบบต้นทาง         |[การพับคิวรี](/power-query/power-query-folding)         |
|การใช้การสร้างโพรไฟล์ข้อมูล     |ทำความเข้าใจเกี่ยวกับคุณภาพของคอลัมน์ การกระจาย และโพรไฟล์         |[เครื่องมือการสร้างโพรไฟล์ข้อมูล](/power-query/data-profiling-tools)         |
|การใช้การจัดการข้อผิดพลาด     |การพัฒนากระแสข้อมูลที่แข็งแกร่งให้มีความยืดหยุ่นเพื่อรีเฟรชข้อผิดพลาด พร้อมคำแนะนำ         |[รูปแบบสำหรับข้อผิดพลาดทั่วไป](/power-query/dealing-with-errors)  </br> [การจัดการข้อผิดพลาดที่ซับซ้อน](/power-query/error-handling)      |
|ใช้มุมมอง Schema      |ปรับปรุงประสบการณ์การเขียนเมื่อทำงานกับตารางแบบกว้างและดำเนินการในระดับ Schema         |[มุมมอง Schema](/power-query/schema-view)         |
|เอนทิตีที่เชื่อมโยง      |การนํากลับมาใช้ใหม่และการอ้างอิงการแปลง         |[เอนทิตีที่เชื่อมโยง](/power-query/dataflows/linked-entities)         |
|การรีเฟรชแบบเพิ่ม      |โหลดข้อมูลล่าสุดหรือข้อมูลที่มีการเปลี่ยนแปลงเทียบกับการโหลดซ้ำเต็มรูปแบบ         |[การรีเฟรชแบบเพิ่มหน่วย](/power-query/dataflows/incremental-refresh)         |
|||


        
## <a name="next-steps"></a>ขั้นตอนถัดไป

บทความต่อไปนี้ให้ข้อมูลเพิ่มเติมเกี่ยวกับกระแสข้อมูลและ Power BI:

* [ข้อมูลเบื้องต้นเกี่ยวกับกระแสข้อมูลและการเตรียมข้อมูลด้วยตนเอง](dataflows-introduction-self-service.md)
* [การสร้างกระแสข้อมูล](dataflows-create.md)
* [กำหนดค่าและใช้กระแสข้อมูล](dataflows-configure-consume.md)
* [ฟีเจอร์พรีเมียมของกระแสข้อมูล](dataflows-premium-features.md)
* [การกำหนดค่าที่จัดเก็บกระแสข้อมูลเพื่อใช้ Azure Data Lake Gen 2](dataflows-azure-data-lake-storage-integration.md)
* [AI กับกระแสข้อมูล](dataflows-machine-learning-integration.md)
* [ข้อจำกัดและข้อควรพิจารณาของกระแสข้อมูล](dataflows-features-limitations.md)