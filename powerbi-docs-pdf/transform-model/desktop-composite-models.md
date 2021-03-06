---
title: ใช้แบบจำลองแบบรวมใน Power BI Desktop
description: สร้างโมเดลข้อมูลที่มีการเชื่อมต่อข้อมูลและความสัมพันธ์แบบกลุ่ม-ต่อ-กลุ่มมากกว่าหนึ่งแห่งใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: conceptual
ms.date: 01/19/2021
LocalizationGroup: Transform and shape data
ms.openlocfilehash: cbf41315f6b33483b7fdd0797bf4dfbcebb605c3
ms.sourcegitcommit: 96080432af4c8e3fe46c23274478ccffa0970efb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/20/2021
ms.locfileid: "98597681"
---
# <a name="use-composite-models-in-power-bi-desktop"></a>ใช้แบบจำลองแบบรวมใน Power BI Desktop

ก่อนหน้านี้ในเดสก์ทอป Power BI Desktop เมื่อคุณใช้ DirectQuery ในรายงาน ไม่มีการเชื่อมต่อข้อมูลอื่น ไม่ว่าจะ DirectQuery หรือการนำเข้าถูกอนุญาตให้สำหรับรายงานนั้น ด้วยโมเดลแบบรวม ข้อกำจัดจะหายไป รายงานสามารถรวมกับการเชื่อมต่อข้อมูลอย่างแนบเนียนจากมากว่าหนึ่ง DirectQuery หรือการเชื่อมต่อการนำเข้าข้อมูลในทุกการผสมที่คุณเลือก

ความสามารถโมเดลแบบรวมใน Power BI Desktop ประกอบด้วยคุณลักษณะสามอย่างที่เกี่ยวข้องกัน:

* **โมเดลแบบรวม**: อนุญาตให้รายงานมีการเชื่อมต่อข้อมูลตั้งแต่สองกลุ่มขึ้นไปจากกลุ่มแหล่งที่มาที่แตกต่างกัน เช่น การเชื่อมต่อ DirectQuery อย่างน้อยหนึ่งรายการและการเชื่อมต่อ Import หนึ่งรายการ การเชื่อมต่อ DirectQuery อย่างน้อยสองรายการหรือการผสมรวมของการเชื่อมต่อดังกล่าว บทความนี้จะอธิบายโมเดลแบบรวมโดยละเอียด

* **ความสัมพันธ์แบบกลุ่มต่อกลุ่ม**: ด้วยโมเดลแบบรวม คุณสามารถตั้ง *ความสัมพันธ์ มาก-ไป-มาก* ระหว่างตาราง วิธีการนี้จะลบขอคำสำหรับค่าเฉพาะในตาราง นอกจากนี้ยังลบการแก้ปัญหาชั่วคราวก่อนหน้า เช่น การเริ่มตารางใหม่เพื่อสร้างความสัมพันธ์เท่านั้น สำหรับข้อมูลเพิ่มเติม ดู [ใช้ความสัมพันธ์ มาก-มาก ใน Power BI Desktop](desktop-many-to-many-relationships.md)

* **โหมดการจัดเก็บข้อมูล**: คุณสามารถระบุเฉพาะว่าวิชวลไหนสอบถามแหล่งข้อมูลส่วนหลัง วิชวลที่ไม่ต้องใช้คิวรีจะถูกนำเข้าแม้ว่าจะมาจาก DirectQuery คุณลักษณะนี้จะช่วยปรับปรุงประสิทธิภาพ และลดการโหลดระบบ Back-end ก่อนหน้านี้ทุกวิชวลเบื้องต้น เช่น ที่หั่น การสอบถามเริ่มต้นไปยังแหล่งข้อมูลส่วนหลัง สำหรับข้อมูล ดู [จัดการโหมดที่เก็บข้อมูลในเดสก์ทอป Power BI](desktop-storage-mode.md).

## <a name="use-composite-models"></a>ใช้โมเดลแบบรวม

ด้วยโมเดลแบบรวม คุณสามารถเชื่อมต่อแหล่งข้อมูลประเภทที่แตกต่างกันเมื่อคุณใช้เดสก์ทอป Power BI หรือการบริการ Power BI คุณสามารถสร้างการเชื่อมต่อข้อมูลเหล่านี้ได้สองวิธี:

* โดยการนำเข้าข้อมูลไปยัง Power BI ซึ่งเป็นวิธีทั่วไปในการรับข้อมูล
* โดยการเชื่อมต่อโดยตรงไปยังข้อมูลในคลังแหล่งข้อมูลเดิมโดยการใช้ DirectQuery หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับ DirectQuery โปรดดู [ใช้ DirectQuery ใน Power BI](../connect-data/desktop-directquery-about.md)

เมื่อคุณใช้ DirectQuery โมเดลแบบรวมทำให้เป็นไปได้ที่จะสร้างโมเดล Power BI เช่น ไฟล์เดี่ยว *.pbix* ของ Power BI Desktop ที่ทั้งหนึ่งหรือสองอย่างของการดำเนินการต่อไปนี้:

* รวมข้อมูลจากแหล่งที่มา DirectQuery หนึ่งแห่งขึ้นไป
* การวมกันของข้อมูลจากแหล่ง DirectQuery และการนำเข้าข้อมูล

ตัวอย่างเช่น โดยการใช้โมเดลแบบรวม คุณสามารถสร้างโมเดลที่รวมประเภทของข้อมูลดังต่อไปนี้:

* ข้อมูลการขายจากคลังข้อมูลวิสาหกิจ
* ข้อมูลเป้าหมายการขายจากฐานข้อมูลแผนก SQL Server
* ข้อมูลที่นำเข้าจากสเปรดชีต

โมเดลที่รวมข้อมูลจากแหล่งข้อมูล DirectQuery ที่มากกว่าหนึ่งหรือรวม DirectQuery กับการนำเข้าข้อมูลที่เรียกใช้โมเดลแบบรวม

คุณสามารถสร้างความสัมพันธ์ระหว่างตารางได้ในขณะที่คุณมีอยู่เสมอแม้ว่าตารางเหล่านั้นมาจากแหล่งข้อมูลที่แตกต่างกัน ทุกความสัมพันธ์ที่ผสมข้ามแหล่งได้ถูกสร้างด้วยจำนวนของมาก-ไป-มาก ไม่ว่าจะเป็นจำนวนที่แท้จริงก็ตาม คุณสามารถเปลี่ยนเป็นแบบหนึ่งต่อกลุ่ม, กลุ่มต่อหนึ่ง หรือหนึ่งต่อหนึ่งได้ ไม่ว่าจำนวนไหนก็ตามที่คุณตั้งค่าวามสัมพันธ์ที่ผสมข้ามแหล่งมี	พฤติกรรมที่แตกต่างกัน คุณไม่สามารถใช้ฟังก์ชัน Data Analysis Expressions (DAX) กับการเรียกคืนค่า `one`จากด้านสู่อีกด้าน `many` นอกจากนี้ คุณอาจเห็นผลกระทบต่อประสิทธิภาพการทำงานเทียบกับความสัมพันธ์แบบกลุ่มต่อกลุ่มภายในแหล่งข้อมูลเดียวกัน

> [!NOTE]
> ด้วยบริบทของโมเดลแบบรวม ตารางที่นำเข้าทั้งหมดเป็นแหล่งเดียวที่ใช้ได้ผลไม่ว่าจะเป็นแหล่งข้อมูลเบื้องต้นที่แท้จริง

## <a name="example-of-a-composite-model"></a>ตัวอย่างของโมเดลแบบรวม

สำหรับตัวอย่างของโมเดลแบบรวม พิจารณาจากรายงานที่ได้เชื่อมต่อไปยังแหล่งเก็บข้อมูลที่ใช้ร่วมกันในSQL Server โดยการใช้ DirectQuery ในตัวอย่างนี้ คลังข้อมูลบรรจุข้อมูล **การขายตามประเทศ**, **ไตรมาส** และ **จักรยาน (ผลิตภัณฑ์)** ดังแสดงในภาพต่อไปนี้:

![มุมมองความสัมพันธ์สำหรับโมเดลแบบรวม](media/desktop-composite-models/composite-models_04.png)

ณ จุดนี้คุณสามารถสร้างภาพง่ายๆ โดยการใช้เขตข้อมูลจากแหล่งที่มานี้ รูปภาพดังต่อไปนี้แสดงการขายทั้งหมดโดย *ชื่อผลิตภัณฑ์* สำหรับไตรมาสที่เลือก

![วิชวลที่อิงจากข้อมูล](media/desktop-composite-models/composite-models_05.png)

แต่หากคุณมีข้อมูลในสเปรดชีตของ Office Excel เกี่ยวกับผู้จัดการผลิตภัณฑ์ที่กำหนดแต่ละผลิตภัณฑ์พร้อมกับลำดับความสำคัญทางการตลาดล่ะ? หากคุณต้องการดู **จำนวนการขาย** โดย **ผู้จัดการผลิตภัณฑ์** อาจไม่มีความเป็นไปได้ที่จะเพิ่มข้อมูท้องถิ่นนี้ไปยังคลังข้อมูลบริษัท หรืออาจใช้เวลาอย่างน้อยเป็นเดือน

อาจไม่มีความเป็นไปได้ในการนำเข้าข้อมูลการขายจากคลังข้อมูลแทนการใช้ DirectQuery และข้อมูลการขายอาจถูกรวมกับข้อมูลที่คุณนำเข้าจากสเปรดชีต อย่างไรก็ตาม วิธีการนี้ไม่สมเหตุสมผลสำหรับสาเหตุที่นำไปสู่การใช้ DirectQuery ตั้งแต่แรก สาเหตุอาจรวมถึง:

* บางการรวมของกฎความปลอดภัยบังคับใช้ในแหล่งข้อมูลเบื้องต้น
* ความจำเป็นเพื่อที่จะสามารถดูข้อมูลล่าสุด
* ขนาดจำนวนมากของข้อมูล

และนี่คือจุดที่ โมเดลแบบรวม เข้ามาช่วย โมเดลแบบรวมส่วนให้คุณเชื่อมต่อแหล่งเก็บข้อมูลโดยการใช้ DirectQuery และต่อมาใช้ **รับข้อมูล** สำหรับแหล่งข้อมูลเพิ่มเติม ในตัวอย่างนี้ เราจะสร้างการเชื่อต่อ DirectQuery ไปยังคลังข้อมูลบริษัทเป็นอันดับแรก เราใช้ **รับข้อมูล** เลือก **Excel** และต่อมานำทางไปยังสเปรดชีตที่ประกอบด้วยข้อมูลท้องถื่นของเรา สุดท้ายนำเข้าสเปรดชีตที่มี *ชื่อผลิตภัณฑ์*, **ผู้จัดการการขาย** ที่กำหนด และ **ลำดับความสำคัญ**  

![หน้าต่างตัวนำทาง](media/desktop-composite-models/composite-models_06.png)

ในรายการ **เขตข้อมูล** คุณจะเห็นสองตาราง: ตาราง **จักรยาน** เดิมจาก SQL Server และตาราง **ProductManagers** ตารางใหม่จะมีข้อมูลที่นำเข้าจาก Excel

![มุมมองเขตข้อมูลของตาราง](media/desktop-composite-models/composite-models_07.png)

ในทำนองเดียวกัน ในมุมมอง **ความสัมพันธ์** ใน Power BI Desktop เราจะเห็นตารางเพิ่มเติมที่มีชื่อว่า **ProductManagers**

![มุมมองความสัมพันธ์ของตาราง](media/desktop-composite-models/composite-models_08.png)

เราต้องการเชื่อมตารางเหล่านี้ไปยังตารางอื่นๆ ในโมเดล เช่นเคย เราสร้างความสัมพันธ์ระหว่างตาราง **จักรยาน** จาก SQL Server และตารางนำเข้า **ProductManagers** กล่าวคือ จะเป็นความสัมพันธ์ระหว่าง **จักรยาน[ProductName]** และ **ProductManagers[ProductName]** ตามที่กล่าวมาก่อนหน้านี้ ทุกความสัมพันธ์ที่ไปผ่านแหล่งข้อมูลที่ตั้งค่าไว้จากจำนวนมาก-ไป-มาก

![หน้าต่าง "สร้างความสัมพันธ์"](media/desktop-composite-models/composite-models_09.png)

หลังจากที่สร้างความสัมพันธ์นี้แล้ว ความสัมพันธ์จะแสดงในมุมมอง **ความสัมพันธ์** ใน Power BI Desktop

![มุมมองความสัมพันธ์ใหม่](media/desktop-composite-models/composite-models_10.png)

เราสามารถสร้างวิชวลโดยการใช้ช่องใดๆ ในรายการ **เขตข้อมูล** ได้แล้ว วิธีการนี้จะผสมข้อมูลจากหลายๆ แหล่งเข้าด้วยกัน เช่น *SalesAmount* ทั้งหมดสำหรับแต่ละ *ผู้จัดการผลิตภัณฑ์* จะแสดงในภาพต่อไปนี้:

![พื้นที่ช่องข้อมูล](media/desktop-composite-models/composite-models_11.png)

การแสดงตัวอย่างกรณีดังต่อไปนี้ของ *ขนาด* ตารางเช่น **ผลิตภัณฑ์** หรือ **ลูกค้า** ที่ขยายด้วยบางข้อมูลที่เข้าพิเศษจากที่อื่น นอกจากนี้ยังสามารถมีตารางใช้ DirectQuery เพื่อเชื่อมต่อแหล่งข้อมูลหลากหลาย ในตัวอย่างเดียวกัน สมมติว่า **เป้าหมายการขาย** ต่อ **ประเทศ** และ **ช่วงเวลา** ถูกจัดเก็บไว้ในแผนกฐานข้อมูลที่แยกกัน โดยทั่วไป คุณสามารถใช้ **รับข้อมูล** เพื่อเชื่อมต่อไปยังข้อมูลนั้น ตามที่แสดงในรูปภาพดังต่อไปนี้:

![หน้าต่างตัวนำทาง](media/desktop-composite-models/composite-models_12.png)

ดังที่ทำก่อนหน้านี้ เราสามารถสร้างความสัมพันธ์ระหว่างตารางใหม่และตารางอื่นๆ ในโมเดล จากนั้นสร้างวิชวลที่รวมข้อมูลตาราง มาดูมุมมอง **ความสัมพันธ์** ที่สร้างความสัมพันธ์ใหม่เอาไว้อีกครั้ง:

![มุมมองความสัมพันธ์ที่มีหลายตาราง](media/desktop-composite-models/composite-models_13.png)

ภาพถัดไปอิงจากข้อมูลใหม่และความสัมพันธ์ที่ได้สร้างไว้ วิชวลด้านล่างซ้ายแสดง *จำนวนการขาย* เทียบกับ *เป้าหมาย* และการคำนวณความแปรปรวนแสดงความแตกต่าง ข้อมูล **จำนวนการขาย** และ **เป้าหมาย** มาจากสองฐานข้อมูลของ SQL Server ที่แตกต่างกัน

![ภาพแสดงข้อมูลเพิ่มเติม](media/desktop-composite-models/composite-models_14.png)

## <a name="set-the-storage-mode"></a>ตั้งค่าโหมดที่เก็บข้อมูล

แต่ละตารางในโมเดลแบบรวมมีโหมดที่เก็บข้อมูลที่แสดงตารางที่ขึ้นอยู่กับ DirectQuery หรือการนำเข้า สามารถดูและแก้ไขโหมดที่เก็บข้อมูลได้ในบานหน้าต่าง **คุณสมบัติ** หากต้องการแสดงโหมดที่เก็บข้อมูล ให้คลิกขวาที่ตารางในรายการ **เขตข้อมูล** จากนั้นเลือก **คุณสมบัติ** ภาพต่อไปนี้แสดงโหมดที่เก็บข้อมูลสำหรับตาราง **เป้าหมายการขาย**

สามารถดูโหมดที่เก็บข้อมูลได้จากคำแนะนำเครื่องมือสำหรับแต่ละตาราง

![คำแนะนำเครื่องมือที่แสดงโหมดที่เก็บข้อมูล](media/desktop-composite-models/composite-models_16.png)

สำหรับทุกไฟล์ Power BI Desktop (ไฟล์ *.pbix*) ที่ประกอบด้วยบางตารางจาก DirectQuery และบางตารางที่นำเข้า แท่งสถานะแสดงโหมดที่เก็บข้อมูลที่เรียกใช้ **ผสม** คุณสามารถคลิกที่ระยะเวลาในแท่งสถานะและเปลี่ยนตารางทั้งหมดเพื่อนำเข้าได้อย่างง่ายดาย

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโหมดที่เก็บข้อมูล ดู [จัดการโหมดที่เก็บข้อมูลใน Power BI Desktop](desktop-storage-mode.md)  

> [!NOTE]
> คุณสามารถใช้โหมดที่เก็บข้อมูล *ผสม* ใน Power BI Desktop และในบริการของ Power BI ได้

## <a name="calculated-tables"></a>ตารางที่ได้รับการคำนวณ

คุณสามารถเพิ่มตารางคำนวณไปยังโมเดลที่ใช้ DirectQuery ได้ Data Analysis Expressions (DAX) ที่กำหนดตารางคำนวณสามารถอ้างอิงได้ทั้งตารางนำเข้าและตาราง DirectQuery หรือผสมทั้งสองตารางก็ได้

ตารางคำนวณจะถูกนำเข้าเสมอ และข้อมูลจะถูกรีเฟรชเมื่อคุณรีเฟรชตาราง หากตารางคำนวณอ้างอิงถึงตาราง DirectQuery วิชวลที่อ้างถึงตาราง DirectQuery จะแสดงค่าล่าสุดในแหล่งข้อมูลเบื้องต้นเสมอ อีกทางหนึ่งคือ วิชวลที่อ้างอิงถึงตารางคำนวณจะแสดงค่าตามเวลาที่ตารางคำนวณรีเฟรชครั้งสุดท้าย

## <a name="security-implications"></a>ความหมายโดยนัยของความปลอดภัย

โมเดลแบบรวมมีความหมายโดยนัยของความปลอดภัยบางอย่าง คิวรีที่ส่งไปที่แหล่งข้อมูลหนึ่งแหล่งสามารถรวมค่าข้อมูลที่ได้รับจากแหล่งอื่นได้ ในตัวอย่างก่อนหน้านี้ วิชวลได้แสดง **(จำนวนการขาย)** โดย **การจัดการผลิตภัณฑ์** ส่งคำถาม SQL ไปยังฐานข้อมูลเชิงสัมพันธ์ของการขาย คำถาม SQL นั้นอาจประกอบด้วยชื่อของการจัดการผลิตภัณฑ์และผลิตภัณฑ์ที่เกี่ยวข้องของพวกเขา

![สคริปต์ที่แสดงความหมายโดยนัยของความปลอดภัย](media/desktop-composite-models/composite-models_17.png)

ดังนั้นข้อมูลที่เก็บไว้ในสเปรดชีตจะถูกรวมอยู่ในคิวรีที่ส่งไปยังฐานข้อมูลเชิงสัมพันธ์ หากข้อมูลนี้เป็นความลับ คุณควรพิจารณาความหมายโดยนัยของความปลอดภัย โดยเฉพาะ ให้พิจารณาประเด็นต่อไปนี้:

* ผู้ดูแลฐานข้อมูลคนใดก็ตามที่สามารถตรวจสอบร่องรอยหรือบันทึกการตรวจสอบ จะสามารถดูข้อมูลนี้แม้จะไม่มีสิทธิ์การใช้งานข้อมูลของแหล่งเดิม ในตัวอย่างนี้ ผู้ดูแลจำเป็นต้องได้สิทธิ์ไปยังไฟล์ Excel

* ควรพิจารณาการตั้งค่าการเข้ารหัสลับสำหรับแต่ละแหล่งข้อมูล คุณต้องการที่จะหลีกเลี่ยงข้อมูลที่เรียกกลับคืนมาจากหนึ่งแหล่งโดยการเชื่อมต่อที่เข้ารหัสและต่อมาโดยที่ไม่ตั้งใจ รวมถึงในคำถามด้วย ซึ่งได้ส่งไปยังแหล่งอื่นโดยการเชื่อมต่อที่ไม่เข้ารหัส

ในการทำตามคำยืนยันที่คุณพิจารณาความเกี่ยวข้องที่มั่นคงใดๆ แล้ว Power BI Desktop แสดงข้อความเตือนเมื่อคุณสร้างโมเดลแบบรวม  

นอกจากนี้หากผู้เขียนเพิ่ม *Table1* จาก *Model A* ลงในแบบจำลองแบบรวม (เราจะเรียกมันว่า *Model C* เพื่อใช้อ้างอิง) จากนั้นผู้ใช้ที่ดูรายงานที่สร้างขึ้นจาก *Model C* สามารถคิวรี **ตารางใดก็ตาม** ใน *Model A* ที่ไม่ได้รับการป้องกันจาก RLS ได้

ด้วยเหตุเดียวกันนี้ ขอให้ระวังการเปิดไฟล์ Power BI Desktop ที่ส่งมาจากแหล่งที่ไม่น่าเชื่อถือ หากไฟล์มีโมเดลแบบรวม ข้อมูลที่มีใครบางคนเรียกดูจากแหล่งหนึ่งโดยการใช้ข้อมูลประจำตัวของผู้ใช้ที่เปิดไฟล์จะถูกส่งไปยังแหล่งข้อมูลอื่นถือเป็นส่วนหนึ่งของคิวรี ข้อมูลอาจได้ถูกดูจากผู้เขียนที่ประสงค์ร้ายต่อไฟล์ Power BI Desktop เมื่อคุณเปิดไฟล์ Power BI Desktop ในขั้นต้นที่ประกอบด้วยแหล่งที่หลากหลาย Power BI Desktop จะแสดงคำเตือน การเตือนนี้จะคล้ายกับการเตือนที่แสดงขึ้นเมื่อคุณเปิดไฟล์ที่มีคิวรี SQL ดั้งเดิม  

## <a name="performance-implications"></a>ความหมายโดยนัยของประสิทธิภาพ  

เมื่อใช้ DirectQuery ประสิทธิภาพควรจะได้รับการพิจารณาทุกครั้ง หลักๆ เพื่อทำให้แน่ใจว่าแหล่งที่มา Back-end มีทรัพยากรที่เพียงพอในการมอบประสบการณ์ที่ดีสำหรับผู้ใช้ ประสบการณ์ที่ดี หมายถึง วิชวลรีเฟรชในห้าวินาทีหรือน้อยกว่านั้น สำหรับคำแนะนำปฏิบัติการเพิ่มเติม ดู [เกี่ยวกับการใช้ DirectQuery ใน Power BI](../connect-data/desktop-directquery-about.md)

การใช้โมเดลแบบรวมเพิ่มข้อควรพิจารณาด้านสมรรถภาพเพิ่มเติม การแสดงผลด้วยภาพเดี่ยวสามารถส่งผลให้เกิดการส่งแบบสอบถามไปยังหลายแหล่งข้อมูลได้ ซึ่งมักจะส่งผ่านผลลัพธ์จากแบบสอบถามหนึ่งไปยังแหล่งที่สอง สถานการณ์นี้สามารถทำให้เกิดการดำเนินการต่อไปนี้:

* **คำถาม SQL ที่รวมถึงจำนวนมากของค่าที่เป็นจริง**: เช่น วิชวลที่ต้องการ **จำนวนการขาย** ทั้งหมดสำหรับชุด **ผู้จัดการผลิตภัณฑ์** ที่เลือกจะต้องค้นหาว่า **ผลิตภัณฑ์** ใดที่ผู้จัดการผลิตภัณฑ์จัดการ เหตุการณ์นี้จะต้องเกิดก่อนที่วิชวลส่งคำถาม SQL ที่รวม ID ผลิตภัณฑ์ทั้งหมดในข้อความ `WHERE`

* **คำถาม SQL ที่ถามไปที่ระดับที่ต่ำกว่าของส่วนประกอบ ด้วยข้อมูลภายหลังที่ถูกรวบรวมแบบท้องถิ่น**: ตัวเลขของ **ผลิตภัณฑ์** ที่พอดีกับเกณฑ์ตัวกรอง **การจัดการผลิตภัณฑ์** เติบโตบใหญ่ขึ้น มันสามารถไร้ประสิทธิภาพหรือไม่เหมาะสมที่จะรวมผลิตภัณฑ์ทั้งหมดในข้อความ `WHERE` แทนที่ คุณจะสามารถส่งคำถามแหล่งข้อมูลเชิงสัมพันธ์ไปยังระดับที่ต่ำกว่าของ **ผลิตภัณฑ์** แล้วรวบรวมผลแบบท้องถิ่น หากคาร์ดินาลลิตี้ของ **ผลิตภัณฑ์** เกินขีดจำกัด 1 ล้าน คิวรีจะล้มเหลว

* **คิวรี SQL หลายคิวรี หนึ่งคิวรีต่อกลุ่มตามค่า**: เมื่อการรวบรวมใช้ **การนับที่แยกกัน** และจัดกลุ่มโดยแถวจากแหล่งอื่นและหากแหล่งภายนอกไม่สนับสนุนการส่งที่มีประสิทธิภาพของค่าที่แท้จริงหลายค่าที่อธิบายการจัดกลุ่ม มันจำเป็นที่จะส่งหนึ่งคำถาม SQL ต่อกลุ่มโดยค่านั้น

   วิชวลร้องขอการนับที่แยกกันของ **ตัวเลขบัญชีลูกค้า** จากตารางเซิร์ฟเวอร์ SQL โดย **การจัดการผลิตภัณฑ์** ที่นำเข้าจากสเปรดชีตที่ต้องการส่งผ่านในรายละเอียดจากตาราง **การจัดการผลิตภัณฑ์** ในคำถามที่ส่งไปยังเซิร์ฟเวอร์ SQL นอกเหนือแหล่งอื่น Redshift สำหรับตัวอย่าง การดำเนินนี้ไม่เหมาะสม แทนที่ จะมีหนึ่งคำถาม SQL ที่ส่งไปแต่ละ **การจัดการการขาย** ขึ้นอยู่กับบางขีดจำกัดที่ใช้ได้จริงซึ่งทำให้คำถามล้มเหลว

ในแต่ละกรณีดังกล่าวมีความหมายโดยนัยของตัวเองในเรื่องประสิทธิภาพและมีรายละเอียดที่แน่นอนต่างกันไปสำหรับแต่ละแหล่งที่มา ถึงแม้ว่าจำนวนของแถวที่ใช้ในความสัมพันธ์ที่ร่วมกันกับสองแหล่งที่เหลือน้อยไม่กี่พัน การปฏิบัติการไม่ควรได้รับผล ขณะที่นี้ดินาลลิตี้ขยาย คุณควรให้ความสำคัญไปยังผลกระทบของผลประสิทธิภาพมากขึ้น

นอกจากนี้ การใช้ความสัมพันธ์มาก-ไป-มากหมายความว่าคำถามที่แยกกันจะต้องส่งไปยังแหล่งที่อยู่ใต้กว่าสำหรับแต่ละผลรวมหรือระดับยอดรวมของส่วนหนึ่ง มากกว่าการรวบรวมค่ารายละเอียดแบบท้องถิ่น ภาพตารางง่าย ๆ พร้อมจำนวนทั้งหมดจะส่งคิวรี SQL สองคิวรี แทนที่จะเป็นคิวรีเดียว

## <a name="limitations-and-considerations"></a>ข้อจำกัดและข้อควรพิจารณา

รุ่นของแบบจำลองแบบรวมนี้มีข้อจำกัดเล็กน้อย

ในปัจจุบัน โมเดลแบบรวมที่เชื่อมต่อกับ SQL, Oracle และแหล่งข้อมูล Teradata เท่านั้นที่รองรับ[การรีเฟรชแบบเพิ่ม](../admin/service-premium-incremental-refresh.md)

แหล่งขนาดที่หลากหลายของ Live Connect ดังต่อไปนี้ไม่สามารถใช้กับโมเดลแบบรวม:

* SAP HANA
* SAP Business Warehouse
* SQL Server Analysis Services
* ชุดข้อมูล Power BI
* Azure Analysis Services

เมื่อคุณเชื่อมต่อไปยังแหล่งขนาดที่หลากหลายเหล่านี้โดยการใช้ DirectQuery คุณไม่สามารถเชื่อมต่อแหล่ง DirectQuery อื่นๆ หรือรวมกับการนำเข้าข้อมูล

ข้อจำกัดของ DirectQuery ที่มีอยู่ยังคงมีผลเมื่อใช้โมเดลแบบรวม ข้อจำกัดจำนวนมากเหล่านี้เป็นข้อจำกัดต่อตาราง โดยขึ้นอยู่กับโหมดที่เก็บข้อมูลของตาราง สำหรับตัวอย่าง แถวที่ถูกคำนวณในตารางที่นำเข้าสามารถอ้างถึงตารางอื่นๆ แต่แถวที่ถูกคำนวณในตาราง DirectQuery สามารถยังคงอ้างถึงเพียงแถวในตารางเดียวกัน ข้อจำกัดอื่น ๆ มีผลกับโมเดลทั้งหมด หากมีตารางใดภายในโมเดลที่เป็น DirectQuery ตัวอย่างเช่น คุณลักษณะ QuickInsights และ Q&A จะไม่สามารถใช้งานได้บนโมเดลหากมีตารางใดภายในโมเดลมีโหมดที่เก็บข้อมูลของ DirectQuery

## <a name="next-steps"></a>ขั้นตอนถัดไป

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับโมเดลแบบรวมและ DirectQuery โปรดดูบทความต่อไปนี้:

* [ความสัมพันธ์แบบกลุ่มต่อกลุ่มใน Power BI Desktop](desktop-many-to-many-relationships.md)
* [โหมดที่เก็บข้อมูลใน Power BI Desktop](desktop-storage-mode.md)
* [ใช้ DirectQuery ใน Power BI](../connect-data/desktop-directquery-about.md)
* [แหล่งข้อมูลที่ได้รับการรองรับโดย DirectQuery ใน Power BI](../connect-data/power-bi-data-sources.md)
* [การใช้ DirectQuery สำหรับชุดข้อมูล Power BI และ Azure Analysis Services (ตัวอย่าง)](../connect-data/desktop-directquery-datasets-azure-analysis-services.md)
