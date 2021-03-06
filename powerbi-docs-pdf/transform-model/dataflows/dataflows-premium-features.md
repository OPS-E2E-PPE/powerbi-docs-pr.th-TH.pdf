---
title: ฟีเจอร์พรีเมียมของกระแสข้อมูล
description: ภาพรวมของคุณลักษณะ Premium ที่พร้อมใช้งานกับกระแสข้อมูล Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-dataflows
ms.topic: how-to
ms.date: 11/13/2020
LocalizationGroup: Data from files
ms.openlocfilehash: 2c8a5646f4831c77ac0f8fabed0d74f2a2cfba1f
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414081"
---
# <a name="premium-features-of-dataflows"></a>ฟีเจอร์พรีเมียมของกระแสข้อมูล

มีการสนับสนุนกระแสข้อมูลสำหรับผู้ใช้ Power BI Pro และ Power BI Premium คุณลักษณะบางอย่างสามารถใช้ได้กับการสมัครใช้งาน Power BI Premium เท่านั้น บทความนี้อธิบายและแสดงรายละเอียดคุณลักษณะเฉพาะ Premium และการใช้งานของคุณลักษณะดังกล่าวเท่านั้น 

คุณลักษณะต่อไปนี้พร้อมใช้งานกับ Power BI Premium เท่านั้น:

* กลไกการคำนวณขั้นสูง
* Direct Query
* เอนทิตีที่คำนวณ
* เอนทิตีที่เชื่อมโยง
* การรีเฟรชแบบเพิ่ม

ส่วนต่อไปนี้อธิบายคุณลักษณะแต่ละอย่างโดยละเอียด

## <a name="the-enhanced-compute-engine"></a>กลไกการคำนวณขั้นสูง

กลไกการคำนวณขั้นสูงใน Power BI ช่วยให้ผู้สมัครใช้งาน Power BI Premium สามารถใช้ความจุของพวกเขาเพื่อปรับใช้กระแสข้อมูลในระดับประสิทธิภาพสูงสุด การใช้กลไกการคำนวณขั้นสูงมีข้อดีดังต่อไปนี้:

* ลดเวลาการรีเฟรชที่จำเป็นสำหรับขั้นตอน ETL ที่ใช้งานเป็นเวลานานผ่านเอนทิตีที่มีการคำนวณลงได้อย่างมาก เช่น การดำเนินการ *รวม* *แยกแยะ* *กรอง* และ *จัดกลุ่มตาม*
* ดำเนินการคิวรี DirectQuery ผ่านเอนทิตี

โดยค่าเริ่มต้น กลไกการคำนวณขั้นสูงจะ **เปิด** หากกลไกการคำนวณขั้นสูงไม่ได้เปิดอยู่ การเปิดใช้งานกลไกการคำนวณขั้นสูงจะอธิบายไว้ในส่วนถัดไปพร้อมกับคำตอบสำหรับคำถามทั่วไป

### <a name="using-the-enhanced-compute-engine"></a>การใช้กลไกการคำนวณขั้นสูง

กลไกการคำนวณขั้นสูงเปิดใช้งานจากหน้า **การตั้งค่าความจุ** ในบริการของ Power BI ในส่วน **กระแสข้อมูล** โดยค่าเริ่มต้น กลไกการคำนวณขั้นสูงจะ **ปิด** เมื่อต้องการเปิดใช้งานกลไกการคำนวณขั้นสูง ให้สลับเป็น **เปิด** ดังที่แสดงในภาพต่อไปนี้ แล้วบันทึกการตั้งค่าของคุณ 

![เปิดกลไกการคำนวณขั้นสูง](media/dataflows-premium-features/compute-engine-settings.png)

> [!IMPORTANT]
> กลไกการคำนวณขั้นสูงทำงานเฉพาะสำหรับความจุ Power BI ของ A3 และใหญ่กว่า

เมื่อเปิดกลไกการคำนวณขั้นสูงแล้ว ให้กลับไปที่ **กระแสข้อมูล** คุณควรจะมองเห็นการปรับปรุงประสิทธิภาพที่ดีขึ้นในเอนทิตีที่คำนวณใดก็ตามซึ่งทำงานที่ซับซ้อนต่าง ๆ เช่น *รวม* หรือ *จัดกลุ่มตาม* การดำเนินการสำหรับกระแสข้อมูลที่สร้างจากเอนทิตีที่ลิงก์ซึ่งมีอยู่แล้วบนความจุเดียวกัน 

เพื่อใช้กลไกการคำนวณให้ได้รับประโยชน์สูงสุด ให้แยกขั้นตอน ETL ออกเป็นกระแสข้อมูลที่แยกจากกันสองรายการด้วยวิธีการต่อไปนี้:

* **กระแสข้อมูล 1** - กระแสข้อมูลนี้ควรส่งถ่ายรายการที่จำเป็นทั้งหมดจากแหล่งข้อมูล และวางลงในกระแสข้อมูล 2
* **กระแสข้อมูล 2** - ดำเนินการ ETL ทั้งหมดในกระแสข้อมูลที่สองนี้ แต่ตรวจสอบให้แน่ใจว่าคุณกำลังอ้างอิงกระแสข้อมูล 1 ที่ควรมีความจุเดียวกันอยู่ นอกจากนี้ ตรวจสอบให้แน่ใจว่าคุณดำเนินงานที่สามารถพับได้ก่อน (กรอง, จัดกลุ่มตาม, แยกแยะ, รวม) ก่อนที่จะดำเนินการอืนใด เพื่อให้แน่ใจว่าสามารถใช้ประโยชน์จากกลไกการคำนวณได้

### <a name="common-questions-and-answers"></a>คำถามที่พบทั่วไปและคำตอบ

**คำถาม:** ฉันเปิดใช้กลไกการคำนวณขั้นสูง แต่ระบบรีเฟรชช้าลง ทำไม?

**คำตอบ:** หากคุณเปิดใช้กลไกการคำนวณขั้นสูง มีคำอธิบายสองแบบที่เป็นไปได้ ที่อาจทำให้เวลารีเฟรชช้าลง:

 * เมื่อเปิดใช้กลไกการคำนวณขั้นสูง ระบบต้องการหน่วยความจำบางส่วนเพื่อทำงานได้อย่างถูกต้อง ดังนั้น หน่วยความจำที่พร้อมสำหรับการรีเฟรชจะลดลง และจะเพิ่มความเป็นไปได้เช่นเดียวกันนี้ต่อรายการรีเฟรชที่รอต่อคิวดำเนินการอยู่ ซึ่งจะลดกระแสข้อมูลที่อาจรีเฟรชอยู่ในเวลาเดียวกันเช่นกัน เพื่อแก้ไขปัญหานี้ เมื่อเปิดใช้การคำนวณขั้นสูง ให้เพิ่มหน่วยความจำที่กำหนดมาสำหรับกระแสข้อมูล เพื่อให้แน่ใจว่าหน่วยข้อมูลที่พร้อมใช้งานสำหรับการรีเฟรชกระแสข้อมูลในเวลาเดียวกันจะยังคงเหมือนเดิม

 * อีกเหตุผลหนึ่งที่คุณอาจพบการรีเฟรชช้าลงคือว่ากลไกการคำนวณจะทำงานที่ด้านบนของเอนทิตีที่มีอยู่เท่านั้น ถ้ากระแสข้อมูลของคุณอ้างอิงแหล่งข้อมูลที่ไม่ใช่กระแสข้อมูล คุณจะไม่เห็นการปรับปรุง ประสิทธิภาพการทำงานจะไม่เพี่มขึ้น เนื่องจากในสถานการณ์สมมติครั้งใหญ่บางอย่าง ค่าเริ่มต้นจากแหล่งข้อมูลจะช้าลง เนื่องจากข้อมูลจำเป็นต้องผ่านไปยังกลไกการคำนวณขั้นสูง  

**คำถาม:** ฉันไม่เห็นการสลับกลไกการคำนวณขั้นสูง ทำไม?

**คำตอบ:** กลไกการคำนวณขั้นสูงถูกปล่อยออกมาในขั้นตอนต่างๆ ไปยังภูมิภาคต่าง ๆ ทั่วโลก เราคาดการณ์ว่า ระบบจะรองรับในทุกภูมิภาคภายในสิ้นปีค.ศ.2020

**คำถาม:** ประเภทข้อมูลที่ได้รับการสนับสนุนสำหรับกลไกการคำนวณคืออะไร

**คำตอบ:** ปัจจุบัน กลไกการคำนวณขั้นสูงและกระแสข้อมูลสนับสนุนประเภทข้อมูลต่อไปนี้ หากกระแสข้อมูลของคุณไม่ได้ใช้หนึ่งในประเภทข้อมูลต่อไปนี้ จะมีข้อผิดพลาดเกิดขึ้นระหว่างการรีเฟรช:

* วันที่/เวลา
* เลขทศนิยม
* ข้อความ
* จำนวนเต็ม
* วันที่/เวลา/โซน
* จริง/เท็จ
* วันที่
* เวลา

## <a name="use-directquery-with-dataflows-in-power-bi-preview"></a>ใช้ DirectQuery ด้วยกระแสข้อมูลใน Power BI (ตัวอย่าง)

คุณสามารถใช้ DirectQuery เพื่อเชื่อมต่อโดยตรงไปยังกระแสข้อมูล และเชื่อมต่อโดยตรงกับกระแสข้อมูลของคุณโดยไม่ต้องนำเข้าข้อมูล 

การใช้ DirectQuery กับกระแสข้อมูลช่วยให้สามารถปรับปรุงขั้นตอนต่อไปนี้ในกระบวนการ Power BI และกระแสข้อมูลของคุณได้เช่น:

* **หลีกเลี่ยงการกำหนดตารางเวลาการรีเฟรชแยกต่างหาก**-DirectQuery เชื่อมต่อโดยตรงกับกระแสข้อมูลโดยไม่จำเป็นต้องสร้างชุดข้อมูลที่นำเข้า เช่นเดียวกับการใช้ DirectQuery ด้วยกระแสข้อมูลของคุณหมายความว่าคุณไม่จำเป็นต้องกำหนดตารางเวลาการรีเฟรชแยกต่างหากสำหรับกระแสข้อมูลและชุดข้อมูล เพื่อให้แน่ใจว่าข้อมูลของคุณจะถูกซิงโครไนซ์

* **การกรองข้อมูล**- DirectQuery มีประโยชน์สำหรับการทำงานบนมุมมองที่กรองแล้วของข้อมูลภายในกระแสข้อมูล ถ้าคุณต้องการกรองข้อมูลและทำงานกับชุดย่อยของข้อมูลที่มีขนาดเล็กลงในกระแสข้อมูลของคุณ คุณสามารถใช้ DirectQuery (และโปรแกรมคำนวณ) เพื่อกรองข้อมูลของกระแสข้อมูล และทำงานกับชุดย่อยที่กรองแล้วที่คุณต้องการ


### <a name="using-directquery-for-dataflows"></a>การใช้ DirectQuery สำหรับกระแสข้อมูล

การใช้ DirectQuery ด้วยกระแสข้อมูลคือคุณลักษณะตัวอย่างที่พร้อมใช้งานเริ่มตั้งแต่ Power BI Desktop รุ่นเดือนพฤษภาคม 2020 

นอกจากนี้ ยังมีข้อกำหนดเบื้องต้นสำหรับการใช้ DirectQuery กับกระแสข้อมูล:

* กระแสข้อมูลของคุณต้องอยู่ภายในพื้นที่ทำงานที่เปิดใช้ Power BI Premium
* ต้องเปิดใช้งาน **กลไกการคำนวณ**

### <a name="enable-directquery-for-dataflows"></a>เปิดใช้งาน DirectQuery สำหรับกระแสข้อมูล

เพื่อให้แน่ใจว่ากระแสข้อมูลของคุณพร้อมใช้งานสำหรับการเข้าถึง DirectQuery โปรแกรมการคำนวณขั้นสูงจะต้องอยู่ในสถานะที่ปรับให้เหมาะสมแล้ว เมื่อต้องการเปิดใช้งาน DirectQuery สำหรับกระแสข้อมูล ให้ตั้งค่าตัวเลือก **การตั้งค่าโปรแกรมการคำนวณขั้นสูง** ใหม่เป็น **เปิด** รูปภาพต่อไปนี้แสดงการตั้งค่าที่เลือกอย่างถูกต้อง

![การควบคุมแยกย่อยสำหรับ Direct Query](media/dataflows-premium-features/compute-engine-granular-control.png)

เมื่อคุณใช้การตั้งค่าดังกล่าว ให้รีเฟรชกระแสข้อมูลเพื่อทำให้การปรับให้เหมาะสมมีผล

### <a name="considerations-and-limitations-for-directquery"></a>ข้อควรพิจารณาและข้อจำกัดสำหรับ DirectQuery

มีข้อจำกัดที่เป็นที่รู้กันสองสามประการในเรื่องของ DirectQuery และกระแสข้อมูล

* ในระหว่างช่วงเวลาการแสดงตัวอย่างของคุณลักษณะนี้ ลูกค้าบางรายอาจพบปัญหาเกี่ยวกับการหมดเวลา หรือประสิทธิภาพการทำงานเมื่อใช้ DirectQuery กับกระแสข้อมูล ปัญหาดังกล่าวจะได้รับการแก้ไขในระหว่างช่วงเวลาการแสดงตัวอย่างนี้

* ขณะนี้ยังไม่รองรับแบบจำลองแบบรวม/แบบผสมที่มีการนำเข้าและแหล่งข้อมูล DirectQuery

* กระแสข้อมูลขนาดใหญ่อาจมีปัญหาเกี่ยวกับปัญหาการหมดเวลาเมื่อดูการแสดงภาพ กระแสข้อมูลขนาดใหญ่ที่ประสบกับปัญหาการหมดเวลาควรใช้โหมดการนำเข้า

* ภายใต้การตั้งค่าแหล่งข้อมูล ตัวเชื่อมต่อกระแสข้อมูลจะแสดงข้อมูลประจำตัวที่ไม่ถูกต้องหากคุณกำลังใช้ DirectQuery การดำเนินการนี้จะไม่ส่งผลกระทบต่อลักษณะการทำงาน และชุดข้อมูลจะทำงานได้อย่างถูกต้อง 

## <a name="computed-entities"></a>เอนทิตีที่คำนวณ

คุณสามารถดำเนินการ **การประมวลผลในที่จัดเก็บ** ได้เมื่อใช้ **กระแสข้อมูล** ที่มีการสมัครใช้งาน Power BI Premium ซึ่งจะช่วยให้คุณคำนวณกระแสข้อมูลที่มีอยู่แล้วและส่งผลลัพธ์กลับได้ โดยจะทำให้คุณได้เพ่งความสนใจไปยังการสร้างและการวิเคราะห์รายงาน

![เอนทิตีที่คำนวณ](media/dataflows-premium-features/computed-entity.png)

เมื่อต้องการทำเนินการการคำนวณในที่จัดเก็บ คุณต้องสร้างกระแสข้อมูลและนำข้อมูลเข้าที่จัดเก็บกระแสข้อมูลของ Power BI ก่อนเป็นอันดับแรก เมื่อคุณมีกระแสข้อมูลที่มีข้อมูลแล้ว คุณก็จะสามารถสร้าง เอนทิตีที่คำนวณไว้ ได้ ซึ่งเป็นเอนทิตีที่ใช้ประมวลผลในที่จัดเก็บ

### <a name="considerations-and-limitations-of-computed-entities"></a>ข้อควรพิจารณาและข้อจำกัดของเอนทิตีที่คำนวณ

* เมื่อทำงานโดยใช้กระแสข้อมูลที่สร้างขึ้นในบัญชี Azure Data Lake Storage Gen2 ภายในองค์กร เอนทิตีที่มีลิงก์และเอนทิตีที่มีการคำนวณจะทำงานได้อย่างมีประสิทธิภาพต่อเมื่อเอนทิตี้ทั้งสองอยู่ในบัญชีที่เก็บข้อมูลเดียวกัน 

ตามแนวทางปฏิบัติที่ดีที่สุดเมื่อทำการคำนวณข้อมูลที่รวมเข้าด้วยกันโดยข้อมูลภายในองค์กรและข้อมูลบนคลาวด์ ให้สร้างกระแสข้อมูลใหม่สำหรับแหล่งข้อมูลแต่ละแหล่ง (หนึ่งรายการสำหรับภายในองค์กรและอีกแหล่งหนึ่งสำหรับระบบคลาวด์) จากนั้นสร้างกระแสข้อมูลที่สามเพื่อรวม/คำนวณทั้งสองแหล่งข้อมูล

## <a name="linked-entities"></a>เอนทิตีที่เชื่อมโยง

คุณสามารถอ้างอิงกระแสข้อมูลที่มีอยู่เมื่อใช้กับการสมัครใช้งาน Power BI Premium ซึ่งช่วยให้คุณทำการคำนวณในเอนทิตีเหล่านี้โดยใช้เอนทิตีที่คำนวณหรืออนุญาตให้คุณสร้างตาราง "งแหล่งที่มาจริงเพียงแหล่งเดียว" ที่คุณสามารถใช้ซ้ำภายในกระแสข้อมูลหลายรายการได้

## <a name="incremental-refresh"></a>การรีเฟรชแบบเพิ่ม

คุณสามารถตั้งค่ากระแสข้อมูลให้รีเฟรชทีละน้อยเพื่อหลีกเลี่ยงการดึงข้อมูลทั้งหมดในทุกการรีเฟรช เมื่อต้องการทำเช่นนั้น ให้เลือกกระแสข้อมูล แล้วเลือกไอคอนรีเฟรชแบบเพิ่มหน่วย

![การรีเฟรชแบบเพิ่ม](media/dataflows-premium-features/incremental-refresh.png)

การตั้งค่าการรีเฟรชแบบเพิ่มหน่วยจะเพิ่มพารามิเตอร์ให้กับกระแสข้อมูลเพื่อระบุช่วงวันที่ สำหรับข้อมูลโดยละเอียดเกี่ยวกับวิธีตั้งค่าการรีเฟรชแบบเพิ่มหน่วย โปรดดูบทความ [การรีเฟรชแบบเพิ่มหน่วย](/power-query/dataflows/incremental-refresh)

### <a name="considerations-for-when-not-to-set-incremental-refresh"></a>ข้อควรพิจารณาเมื่อไม่ควรตั้งค่าการรีเฟรชแบบเพิ่มหน่วย

อย่าตั้งค่ากระแสข้อมูลเป็นการรีเฟรชแบบเพิ่มหน่วยในสถานการณ์ต่อไปนี้:

* เอนทิตีที่เชื่อมโยงไม่ควรใช้การรีเฟรชแบบเพิ่มหน่วยหากอ้างอิงกระแสข้อมูล กระแสข้อมูลไม่สนับสนุนการพับคิวรี (แม้ว่าเอนทิตีจะเปิดใช้งาน Direct Query) 
* ชุดข้อมูลที่อ้างอิงกระแสข้อมูลไม่ควรใช้การรีเฟรชแบบเพิ่มหน่วย โดยทั่วไปการรีเฟรชกระแสข้อมูลควรทำงานได้ดี ถ้าการรีเฟรชใช้เวลานานกว่าที่คาดไว้ ให้พิจารณาใช้กลไกการคำนวณและหรือโหมด DirectQuery

## <a name="next-steps"></a>ขั้นตอนถัดไป
บทความต่อไปนี้ให้ข้อมูลเพิ่มเติมเกี่ยวกับกระแสข้อมูลและ Power BI:

* [แนวทางปฏิบัติที่ดีที่สุดสำหรับกระแสข้อมูล](dataflows-best-practices.md)
* [กำหนดค่าปริมาณงานกระแสข้อมูลของ Power BI Premium](dataflows-premium-workload-configuration.md)
* [ข้อมูลเบื้องต้นเกี่ยวกับกระแสข้อมูลและการเตรียมข้อมูลด้วยตนเอง](dataflows-introduction-self-service.md)
* [การสร้างกระแสข้อมูล](dataflows-create.md)
* [กำหนดค่าและใช้กระแสข้อมูล](dataflows-configure-consume.md)
* [การกำหนดค่าที่จัดเก็บกระแสข้อมูลเพื่อใช้ Azure Data Lake Gen 2](dataflows-azure-data-lake-storage-integration.md)
* [AI กับกระแสข้อมูล](dataflows-machine-learning-integration.md)
* [ข้อจำกัดและข้อควรพิจารณาของกระแสข้อมูล](dataflows-features-limitations.md)