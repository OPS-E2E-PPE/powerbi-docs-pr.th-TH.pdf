---
title: API ของการวิเคราะห์แบบฝังตัวของ Power BI ที่ใช้นโยบายการเก็บรักษาข้อมูลอัตโนมัติสำหรับข้อมูลแบบเรียลไทม์เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังตัวที่ดีขึ้น
description: เรียนรู้เกี่ยวกับนโยบายการเก็บรักษาข้อมูลโดยอัตโนมัติในบริการ Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: 81c975332abc4cb599a7172f1697c1b06ea34eba
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887741"
---
# <a name="automatic-retention-policy-for-real-time-data"></a>นโยบายการเก็บข้อมูลโดยอัตโนมัติสำหรับข้อมูลแบบเรียลไทม์

นโยบายการเก็บข้อมูลโดยอัตโนมัติในบริการ Power BI คือ พารามิเตอร์สตริงคิวรีที่อนุญาตให้การเก็บข้อมูลใหม่สามารถล้างข้อมูลเก่าโดยอัตโนมัติในขณะที่ยังคงรักษาความต่อเนื่องของข้อมูลใหม่ที่จะลงในแดชบอร์ดของคุณ นโยบายการเก็บข้อมูลครั้งแรกจะเรียกว่า *ข้อมูลไหนเข้าก่อนข้อมูลนั้นออกก่อน (FIFO)* เมื่อเปิดใช้งานจะสามารถเก็บรวบรวมข้อมูลในตารางจนกว่าจะถึง 200,000 แถว เมื่อข้อมูลที่เกินกว่า 200,000 แถว ระบบจะค่อยๆ ทิ้งแถวเดิมในชุดข้อมูลออกไป ซึ่งจะอยู่ระหว่างแถวที่ 200,000 ถึงแถวที่ 210,000 ของข้อมูลล่าสุดเท่านั้น  
  
<center>

![นโยบายการเก็บข้อมูล](media/api-Automatic-retention-policy-for-real-time-data/retention-policy.png) 

</center>

นโยบายการเก็บข้อมูลจะเปิดใช้งานเมื่อคุณสร้างชุดข้อมูลครั้งแรก สิ่งที่คุณต้องทำคือการเพิ่มพารามิเตอร์คิวรี "นโยบายการเก็บข้อมูลค่าเริ่มต้น" เข้าไปยังชุดข้อมูล POST ของคุณจากนั้นให้เรียกใช้และตั้งค่าเท่ากับ *basicFIFO*  

```console
POST https://api.powerbi.com/v1.0/myorg/datasets?defaultRetentionPolicy={None | basicFIFO}
```
