---
title: 'DAX: ใช้ SELECTEDVALUE แทน VALUES'
description: คำแนะนำเกี่ยวกับเมื่อใดที่คุณควรใช้ฟังก์ชัน SELECTEDVALUE
author: peter-myers
ms.author: kfollis
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 11/20/2019
ms.openlocfilehash: aa6c1c9c20a08eb8e30492642a12c74137795d85
ms.sourcegitcommit: fb529c4532fbbdfde7ce28e2b4b35f990e8f21d9
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "99088384"
---
# <a name="dax-use-selectedvalue-instead-of-values"></a>DAX: ใช้ SELECTEDVALUE แทน VALUES

ในฐานะผู้สร้างแบบจำลองข้อมูล บางครั้งคุณอาจจำเป็นต้องเขียนนิพจน์ DAX ที่ทดสอบว่ามีการกรองคอลัมน์จากค่าเฉพาะหรือไม่

ใน DAX รุ่นก่อนหน้า คุณสามารถบรรลุข้อกำหนดนี้ได้อย่างมั่นคงโดยใช้รูปแบบที่เกี่ยวข้องกับฟังก์ชัน DAX สามฟังก์ชัน ฟังก์ชันดังกล่าวคือ [IF](/dax/if-function-dax), [HASONEVALUE](/dax/hasonevalue-function-dax) และ [VALUES](/dax/values-function-dax) ข้อกำหนดหน่วยวัดต่อไปนี้แสดงถึงตัวอย่าง ซึ่งคำนวณค่าภาษีขาย แต่เฉพาะสำหรับยอดขายที่เกิดจากลูกค้าชาวออสเตรเลียเท่านั้น

```dax
Australian Sales Tax =
IF(
    HASONEVALUE(Customer[Country-Region]),
    IF(
        VALUES(Customer[Country-Region]) = "Australia",
        [Sales] * 0.10
    )
)
```

ในตัวอย่าง ฟังก์ชัน HASONEVALUE ส่งกลับ TRUE เฉพาะเมื่อค่าเดียวกรองคอลัมน์ **Country-Region** เมื่อค่าเป็น TRUE ฟังก์ชัน VALUES จะถูกเปรียบเทียบกับข้อความตัวอักษร "Australia" เมื่อฟังก์ชัน VALUES ส่งกลับ TRUE หน่วยวัด **Sales (ยอดขาย)** จะถูกคูณด้วย 0.10 (คิดเป็น 10%) ถ้าฟังก์ชัน HASONEVALUE ส่งกลับค่า FALSE เนื่องจากมีค่ามากกว่าหนึ่งค่ากรองคอลัมน์ ดังนั้นฟังก์ชัน IF แรกจะส่งกลับ BLANK

การใช้ HASONEVALUE เป็นเทคนิคเชิงป้องกัน ซึ่งเทคนิคนี้จำเป็นเนื่องจากเป็นไปได้ว่าค่าหลายค่าจะกรองคอลัมน์ **Country-Region** ในกรณีนี้ ฟังก์ชัน VALUES จะส่งกลับตารางหลายแถว การเปรียบเทียบตารางหลายแถวกับค่าสเกลาร์ทำให้เกิดข้อผิดพลาด

## <a name="recommendation"></a>คำแนะนำ

เราขอแนะนำให้คุณใช้ฟังก์ชัน [SELECTEDVALUE](/dax/selectedvalue-function) ซึ่งจะทำให้ได้ผลลัพธ์เดียวกันกับรูปแบบที่อธิบายไว้ในบทความนี้ แต่มีประสิทธิภาพและสวยงามยิ่งขึ้น

การใช้ฟังก์ชัน SELECTEDVALUE ข้อกำหนดหน่วยวัดตัวอย่างจะถูกเขียนใหม่ในขณะนี้

```dax
Australian Sales Tax =
IF(
    SELECTEDVALUE(Customer[Country-Region]) = "Australia",
    [Sales] * 0.10
)
```

> [!TIP]
> ซึ่งอาจเป็นไปได้ที่จะส่งผ่านค่า _ผลลัพธ์สำรอง_ ลงในฟังก์ชัน SELECTEDVALUE ฟังก์ชันจะส่งกลับค่าผลลัพธ์สำรองเมื่อไม่มีตัวกรองหรือตัวกรองหลายรายการถูกนำไปใช้กับคอลัมน์

## <a name="next-steps"></a>ขั้นตอนถัดไป

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:

- [ข้อมูลอ้างอิงเกี่ยวกับ Data Analysis Expressions (DAX)](/dax/)
- เส้นทางการเรียนรู้: [ใช้ DAX ใน Power BI Desktop](/learn/paths/dax-power-bi/)
- มีคำถามหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)
- มีข้อเสนอแนะไหม [สนับสนุนแนวคิดในการปรับปรุง Power BI](https://ideas.powerbi.com)