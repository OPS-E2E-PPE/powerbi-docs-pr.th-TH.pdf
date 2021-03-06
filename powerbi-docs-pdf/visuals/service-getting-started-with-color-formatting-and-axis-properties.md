---
title: เริ่มต้นใช้งานการจัดรูปแบบการแสดงข้อมูลด้วยภาพของรายงาน
description: เริ่มต้นใช้งานโดยใช้ตัวเลือกการจัดรูปแบบด้วยการแสดงข้อมูลด้วยภาพของรายงาน
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: conceptual
ms.date: 11/09/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 5ab8a9fdb0a7cdd373aad500950280ddaef655e4
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96409849"
---
# <a name="getting-started-with-the-formatting-pane"></a>เริ่มต้นใช้งานบานหน้าต่างการจัดรูปแบบ

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]    

หากคุณมีสิทธิ์แก้ไขสำหรับรายงาน มีตัวเลือกการจัดรูปแบบมากมายให้พร้อมใช้งาน ในรายงาน Power BI คุณสามารถเปลี่ยนสีของชุดข้อมูล จุดข้อมูล และแม้แต่พื้นหลังของการแสดงผลข้อมูลด้วยภาพได้ คุณสามารถเปลี่ยนวิธีการแสดงแกน x และแกน y คุณยังสามารถจัดรูปแบบคุณสมบัติแบบอักษรของการแสดงภาพ รูปร่าง และชื่อเรื่องได้ Power BI ช่วยให้คุณสามารถควบคุมวิธีที่รายงานของคุณปรากฏได้อย่างเต็มที่

ในการเริ่มต้น ให้เปิดรายงานใน Power BI Desktop หรือบริการ Power BI ทั้งสองมีตัวเลือกการจัดรูปแบบเกือบเหมือนกัน เมื่อคุณเปิดรายงานในบริการของ Power BI โปรดตรวจสอบให้แน่ใจว่าได้เลือก **แก้ไข** จากแถบเมนู 

![แถบเมนูที่แสดงตัวเลือกแก้ไข](media/service-getting-started-with-color-formatting-and-axis-properties/power-bi-edit.png)

เมื่อคุณกำลังแก้ไขรายงาน และคุณมีการแสดงภาพที่เลือกไว้ บานหน้าต่าง **การแสดงภาพ** จะปรากฏขึ้น ใช้บานหน้าต่างนี้เพื่อเปลี่ยนการแสดงภาพ ด้านล่างของบานหน้าต่าง **การแสดงภาพ** จะมีไอคอนสามไอคอน: ไอคอน **เขตข้อมูล** (แถบเรียงซ้อน) ไอคอน **รูปแบบ** (แปรงลูกกลิ้ง) และไอคอน **การวิเคราะห์** (แว่นขยาย) ในรูปด้านล่าง ไอคอน **เขตข้อมูล** ถูกเลือกไว้ โดยสังเกตได้จากแถบสีเหลืองที่อยู่ด้านล่างไอคอน

![บานหน้าต่างการแสดงภาพที่มีไอคอนเขตข้อมูลที่เลือก](media/service-getting-started-with-color-formatting-and-axis-properties/power-bi-format.png)

เมื่อคุณเลือก **รูปแบบ** พื้นที่ด้านล่างไอคอนจะแสดงการกำหนดรูปแบบที่พร้อมใช้งานสำหรับการแสดงภาพที่เลือกไว้ในปัจจุบัน  

![บานหน้าต่างการแสดงภาพที่มีไอคอนรูปแบบที่เลือก](media/service-getting-started-with-color-formatting-and-axis-properties/power-bi-format-selected.png)

คุณสามารถกำหนดองค์ประกอบของแต่ละการแสดงภาพเองได้มากมาย ตัวเลือกที่พร้อมใช้งานขึ้นอยู่กับประเภทของการแสดงภาพที่เลือก บางตัวเลือกเหล่านั้นคือ:

* คำอธิบายแผนภูมิ
* แกน X
* แกน Y
* สีข้อมูล
* ป้ายชื่อข้อมูล
* ป้ายชื่อทั้งหมด
* รูปร่าง
* พื้นที่การลงจุด
* ชื่อเรื่อง
* พื้นหลัง
* ล็อกอัตราส่วน
* เส้นขอบ
* คำแนะนำเครื่องมือ
* ส่วนหัวของวิชวล
* รูปร่าง
* ตำแหน่ง    
และอีกมากมาย


> [!NOTE]
>  
> คุณจะไม่เห็นองค์ประกอบเหล่านี้ทั้งหมดรวมทั้งการแสดงภาพแต่ละชนิด การแสดงภาพที่คุณเลือกไว้จะมีผลต่อรูปแบบการกำหนดเองที่พร้อมใช้งาน ตัวอย่างเช่น คุณจะไม่เห็นแกน X ถ้าคุณมีแผนภูมิวงกลมที่เลือกไว้ เนื่องจากแผนภูมิวงกลมไม่มีแกน X

นอกจากนี้ โปรดทราบว่า ถ้าคุณไม่มีการแสดงภาพที่เลือกไว้ **ตัวกรอง** ก็จะปรากฏขึ้นแทนไอคอนซึ่งจะช่วยให้คุณสามารถนำตัวกรองไปใช้กับการแสดงภาพทั้งหมดในหน้าได้

วิธีที่ดีที่สุดในการเรียนรู้วิธีการใช้ตัวเลือกการจัดรูปแบบคือการลองใช้เครื่องมือเหล่านั้นดู คุณสามารถยกเลิกการเปลี่ยนแปลงของคุณหรือแปลงกลับเป็นค่าเริ่มต้นได้เสมอ มีตัวเลือกมากมายที่พร้อมใช้งานและมีการเพิ่มรายการใหม่ตลอดเวลา ซึ่งเป็นไปไม่ได้ที่จะอธิบายตัวเลือกการจัดรูปแบบทั้งหมดในหนึ่งบทความ แต่เพื่อให้คุณได้เริ่มต้นใช้งาน มาลองทบทวนด้วยกันสักสองสามรายการ 

1. เปลี่ยนสีที่ใช้ในวิชวล   
2. ใช้งานลักษณะ    
3. การเปลี่ยนแปลงคุณสมบัติแกน    
4. เพิ่มป้ายชื่อข้อมูล    
1. เพิ่มป้ายชื่อทั้งหมด




## <a name="working-with-colors"></a>การใช้งานแบบมีสีสัน

ลองทำตามขั้นตอนสำคัญที่จะต้องใช้ในการกำหนดรูปแบบสีบนการแสดงภาพ

1. เลือกการแสดงภาพเพื่อเปิดใช้งาน

2. เลือกไอคอนแปรงลูกกลิ้งเพื่อเปิดแท็บการจัดรูปแบบ แท็บการจัดรูปแบบจะแสดงองค์ประกอบของการจัดรูปแบบทั้งหมดที่พร้อมใช้งานสำหรับวิชวลที่เลือก

    ![แผนภูมิที่มีแท็บบานหน้าต่างการจัดรูปแบบที่เลือกไว้](media/service-getting-started-with-color-formatting-and-axis-properties/power-bi-formatting.png)

3. เลือก **สีข้อมูล** เพื่อขยายการกำหนดเองที่พร้อมใช้งาน  

    ![แผนภูมิที่มีบานหน้าต่างการจัดรูปแบบเปิดอยู่และสีข้อมูลที่มีการขยาย](media/service-getting-started-with-color-formatting-and-axis-properties/power-bi-data-colors.png)

4. เปลี่ยน **แสดงทั้งหมด** เป็นเปิด และเลือกสีที่แตกต่างกันสำหรับคอลัมน์

    ![แผนภูมิที่มีสีใหม่ที่ใช้กับบางคอลัมน์](media/service-getting-started-with-color-formatting-and-axis-properties/power-bi-change-colors.png)

ต่อไปนี้คือเคล็ดลับบางอย่างที่มีประโยชน์สำหรับการทำงานกับสี ตัวเลขในรายการต่อไปนี้จะยังปรากฏอยู่ในหน้าจอต่อไปนี้ โดยจะระบุว่าคุณจะสามารถเข้าใข้งานหรือเปลี่ยนแปลงองค์ประกอบใดบ้างในองค์ประกอบที่มีประโยขน์เหล่านี้

1. ไม่ชอบสีสันใช่ไหม ไม่มีปัญหา เพียงเลือก **แปลงกลับเป็นค่าเริ่มต้น** และสิ่งที่คุณเลือกจะเปลี่ยนกลับเป็นการตั้งค่าเริ่มต้น 

2. ไม่ชอบสีที่เปลี่ยนใช่ไหม เลือก **แปลงกลับเป็นค่าเริ่มต้น** จากด้านล่างของส่วน   **สีข้อมูล** และสีของคุณแปลงกลับเป็นการตั้งค่าเริ่มต้น 

3. ต้องการสีที่คุณไม่เห็นในชุดแบบสีหรือไม่ เพียงเลือก **สีแบบกำหนดเอง** และเลือกจากแถบสเปกตรัมสี  

   ![ส่วนสีข้อมูลที่มีการจานสีเปิดอยู่](media/service-getting-started-with-color-formatting-and-axis-properties/power-bi-color-extras.png)

ไม่ได้ชื่นชอบกับการเปลี่ยนแปลงที่คุณเพิ่งทำใช่หรือไม่ ใช ้ **CTRL + Z** เมื่อต้องการเลิกทำ ในลักษณะเดียวกับที่คุณใช้ดำเนินการ

## <a name="applying-a-style-to-a-table"></a>ใช้งานลักษณะกับตาราง
การแสดงภาพ Power BI บางรายการจะมีตัวเลือก **ลักษณะ** ด้วยการคลิกเพียงครั้งเดียว จะมีการใช้ตัวเลือกการจัดรูปแบบเต็มรูปแบบกับการแสดงภาพของคุณทั้งหมดในครั้งเดียว 

1. เลือกตารางหรือเมทริกซ์เพื่อเปิดใช้งาน   
1. เปิดบานหน้าต่างการจัดรูปแบบ และเลือก **ลักษณะ**

   ![เลือกลักษณะจากแท็บการจัดรูปแบบ](media/service-getting-started-with-color-formatting-and-axis-properties/power-bi-style.png)


1. เลือกลักษณะจากรายการดรอปดาวน์ 

   ![ตารางเดียวกันที่มีการใช้แถวสีฉูดฉาดที่มีส่วนหัวเป็นตัวหนา](media/service-getting-started-with-color-formatting-and-axis-properties/power-bi-style-flashy.png)

แม้ว่าหลังจากที่คุณนำลักษณะไปใช้แล้ว คุณสามารถดำเนินการจัดรูปแบบคุณสมบัติต่อได้ ซึ่งรวมถึง สี สำหรับการแสดงภาพนั้น


## <a name="changing-axis-properties"></a>การเปลี่ยนแปลงคุณสมบัติแกน

มักจะมีประโยชน์ในการปรับเปลี่ยนแกน X หรือแกน Y คล้ายกับการใช้งานแบบมีสีสัน คุณสามารถปรับเปลี่ยนแกนได้โดยเลือกไอคอนลูกศรชี้ลงทางด้านซ้ายของแกนคุณต้องการเปลี่ยนแปลง ดังที่แสดงในรูปต่อไปนี้  
![บานหน้าต่างรูปแบบที่มีลูกศรไปยังการ์ดแกน Y](media/service-getting-started-with-color-formatting-and-axis-properties/power-bi-y-axis.png)

ในตัวอย่างด้านล่าง เราได้จัดรูปแบบแกน Y โดย:
- ย้ายป้ายชื่อไปยังด้านขวาของการแสดงภาพ

- เปลี่ยนค่าเริ่มต้นเป็นศูนย์

- เปลี่ยนสีตัวอักษรของป้ายชื่อเป็นสีดำ

- เพิ่มขนาดแบบอักษรของป้ายชื่อเป็น 12

- เพิ่มชื่อเรื่องแกน Y


    ![แผนภูมิคอลัมน์เดียวกันแต่มีการจัดรูปแบบแกน Y มากมาย](media/service-getting-started-with-color-formatting-and-axis-properties/power-bi-axis-changes.png)

คุณสามารถนำป้ายชื่อแกน X ออกได้ ทั้งหมด โดยสลับปุ่มตัวเลือกที่อยู่ด้านข้าง **แกน X** หรือ **แกน Y** คุณยังสามารถเลือกได้ว่าจะเปิดหรือปิดใช้งานชื่อแกนได้ โดยเลือกปุ่มตัวเลือกที่อยู่ถัดจาก **ชื่อเรื่อง** ได้  



## <a name="adding-data-labels"></a>เพิ่มป้ายชื่อข้อมูล    

ลองเพิ่มป้ายชื่อข้อมูลลงในแผนภูมิพื้นที่ 

ต่อไปนี้คือรูปภาพ *ก่อน* 

![แผนภูมิพื้นที่ไม่มีการจัดรูปแบบ](media/service-getting-started-with-color-formatting-and-axis-properties/power-bi-area-chart.png)


และนี่คือรูปภาพ *หลัง*

![แผนภูมิพื้นที่มีการจัดรูปแบบ](media/service-getting-started-with-color-formatting-and-axis-properties/power-bi-data-labels.png)

เราเลือกการแสดงภาพเพื่อทำให้ใช้งานได้และเปิดแท็บการจัดรูปแบบ  เราเลือก **ป้ายชื่อข้อมูล** และเปิดใช้งาน และเรายังเพิ่มขนาดตัวอักษรเป็น 12 เปลี่ยนตระกูลแบบอักษรเป็น Arial Black เปิด **แสดงพื้นหลัง** และเปลี่ยนพื้นหลังเป็นสีขาวที่มีความโปร่งใส 5%

นี่เป็นเพียงบางส่วนของการจัดรูปแบบที่สามารถทำได้ เปิดรายงานในโหมดการแก้ไขและสนุกกับการสำรวจบานหน้าต่างการจัดรูปแบบเพื่อสร้างการแสดงภาพที่สวยงามและให้ข้อมูล

## <a name="adding-total-labels"></a>การเพิ่มป้ายชื่อทั้งหมด    

อีกหนึ่งตัวอย่างสุดท้ายของการจัดรูปแบบก่อนที่คุณจะเริ่มต้นลองทำด้วยตัวคุณเอง  ลองเพิ่มป้ายชื่อทั้งหมดลงในแผนภูมิคอลัมน์แบบเรียงซ้อน ป้ายชื่อทั้งหมดจะพร้อมใช้งานสำหรับแผนภูมิแบบเรียงซ้อน แผนภูมิผสม และแผนภูมิพื้นที่

เมื่อคุณเปิดใช้งานป้ายชื่อทั้งหมด Power BI จะแสดงการรวมหรือผลรวมของข้อมูล มาลองดูตัวอย่างกัน 

ที่นี่เรามีแผนภูมิคอลัมน์แบบเรียงซ้อนพร้อมป้ายชื่อข้อมูลที่แสดงค่าของแต่ละส่วนของสแต็กเต็มแต่ละชุด  นี่คือมุมมองค่าเริ่มต้น 

![แผนภูมิคอลัมน์พร้อมป้ายชื่อข้อมูล](media/service-getting-started-with-color-formatting-and-axis-properties/power-bi-column-charts.png)


ด้วยการเปิดวิชวลในมุมมองการแก้ไข คุณสามารถเปลี่ยนการแสดงผลสำหรับป้ายชื่อข้อมูลและป้ายชื่อทั้งหมดได้ เลือกภาพเพื่อเปิดใช้งานและเปิดพื้นที่การจัดรูปแบบ เลื่อนลงไปที่ **ป้ายชื่อข้อมูล** และ **ป้ายชื่อทั้งหมด** **ป้ายชื่อข้อมูล** เปิดอยู่ และ **ป้ายชื่อทั้งหมด** ปิดอยู่ 

![แผนภูมิคอลัมน์ที่ไม่มีการจัดรูปแบบ](media/service-getting-started-with-color-formatting-and-axis-properties/power-bi-total-label.png)

ปิด **ป้ายชื่อข้อมูล** และเปิด **ป้ายชื่อทั้งหมด** ตอนนี้ Power BI แสดงการรวมสำหรับแต่ละคอลัมน์    
![แผนภูมิคอลัมน์ที่มีการจัดรูปแบบ](media/service-getting-started-with-color-formatting-and-axis-properties/power-bi-totals.png)

นี่เป็นเพียงบางส่วนของการจัดรูปแบบที่สามารถทำได้ เปิดรายงานในโหมดการแก้ไขและสนุกกับการสำรวจบานหน้าต่างการจัดรูปแบบเพื่อสร้างการแสดงภาพที่สวยงามและให้ข้อมูล


## <a name="next-steps"></a>ขั้นตอนถัดไป
สำหรับข้อมูลเพิ่มเติม โปรดดูบทความต่อไปนี้: 

* [การแชร์รายงาน](../collaborate-share/service-share-reports.md)

* [คำแนะนำและเคล็ดลับในการจัดรูปแบบสีใน Power BI](service-tips-and-tricks-for-color-formatting.md)  
* [การจัดรูปแบบตามเงื่อนไขในตาราง](../create-reports/desktop-conditional-table-formatting.md)

