---
title: 'DAX: ใช้ COUNTROWS แทน COUNT'
description: คำแนะนำเกี่ยวกับเมื่อใดที่ควรใช้ฟังก์ชัน COUNTROWS
author: peter-myers
ms.author: kfollis
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 11/23/2019
ms.openlocfilehash: 8d3baba388900a9d57d6490db13c25cb363667ba
ms.sourcegitcommit: fb529c4532fbbdfde7ce28e2b4b35f990e8f21d9
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "99088522"
---
# <a name="dax-use-countrows-instead-of-count"></a>DAX: ใช้ COUNTROWS แทน COUNT

ในฐานะผู้สร้างแบบจำลองข้อมูล บางครั้งคุณอาจจำเป็นต้องเขียนนิพจน์ DAX ที่นับแถวของตาราง ตารางอาจเป็นตารางของแบบจำลองหรือนิพจน์ที่ส่งกลับตาราง

คุณสามารถบรรลุความต้องการของคุณได้ด้วยสองวิธี คุณสามารถใช้ฟังก์ชัน [COUNT](/dax/count-function-dax) เพื่อนับค่าคอลัมน์ หรือคุณสามารถใช้ฟังก์ชัน [COUNTROWS](/dax/countrows-function-dax) เพื่อนับแถวของตารางได้ ทั้งสองฟังก์ชันจะทำให้เกิดผลลัพธ์เดียวกัน ซึ่งคอลัมน์ที่นับไม่มี BLANK

ข้อกำหนดหน่วยวัดต่อไปนี้แสดงถึงตัวอย่าง ซึ่งคำนวณจำนวนค่าคอลัมน์ **OrderDate**

```dax
Sales Orders =
COUNT(Sales[OrderDate])
```

ระบุว่าความละเอียดของตาราง **ยอดขาย (Sales)** คือหนึ่งแถวต่อคำสั่งขาย และคอลัมน์ **OrderDate** ไม่มี BLANK จากนั้นหน่วยวัดจะส่งกลับผลลัพธ์ที่ถูกต้อง

อย่างไรก็ตามข้อกำหนดหน่วยวัดต่อไปนี้เป็นโซลูชันที่ดีกว่า

```dax
Sales Orders =
COUNTROWS(Sales)
```

มีสามเหตุผลที่ทำให้ข้อกำหนดหน่วยวัดที่สองดีกว่า:

- มีประสิทธิภาพมากกว่า และดังนั้นจึงทำงานได้ดียิ่งขึ้น
- ไม่พิจารณา BLANK ที่อยู่ในคอลัมน์ใดก็ตามของตาราง
- ความตั้งใจของสูตรมีความชัดเจนมากขึ้นจนถึงจุดที่อธิบายตัวเองได้

## <a name="recommendation"></a>คำแนะนำ

เมื่อคุณต้องการนับแถวของตาราง เราขอแนะนำให้คุณใช้ฟังก์ชัน COUNTROWS เสมอ

## <a name="next-steps"></a>ขั้นตอนถัดไป

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:

- [ข้อมูลอ้างอิงเกี่ยวกับ Data Analysis Expressions (DAX)](/dax/)
- เส้นทางการเรียนรู้: [ใช้ DAX ใน Power BI Desktop](/learn/paths/dax-power-bi/)
- มีคำถามหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)
- มีข้อเสนอแนะไหม [สนับสนุนแนวคิดในการปรับปรุง Power BI](https://ideas.powerbi.com)