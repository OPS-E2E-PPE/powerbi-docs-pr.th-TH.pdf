---
title: ข้อจำกัดของ Power BI REST API ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: 'Power BI REST API มีข้อจำกัดดังต่อไปนี้: เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI'
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: 1196917f0223ccde012d203d75c4e96fbc3b9dcf
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887672"
---
# <a name="power-bi-rest-api-limitations"></a>ข้อจำกัดของ Power BI REST API  
  
**การโพสต์แถว**
  
* สูงสุด 75 คอลัมน์
* สูงสุด 75 ตาราง
* สามารถขอแถวได้สูงสุด 10,000 แถวต่อหนึ่งโพสต์  
* ภายใน 1 ชั่วโมงสามารถเพิ่มแถวได้ 1,000,000 แถวต่อหนึ่งชุดข้อมูล  
* สามารถส่งคำขอโพสต์แถวได้สูงสุด 5 คำขอต่อหนึ่งชุดข้อมูล  
* ภายใน 1 นาทีสามารถส่งคำขอ 120 โพสต์แถวต่อหนึ่งชุดข้อมูล
* ถ้าตารางมีแถว 250,000 แถวหรือมากกว่า จะสามารถส่งคำขอได้ 120 โพสต์แถวต่อ 1ชั่วโมงสำหรับแต่ละชุดข้อมูล
* สามารถเก็บแถวได้สูงสุด 200,000 แถวต่อ 1 ตารางในชุดข้อมูล FIFO
* สามารถเก็บแถวได้สูงสุด 5,000,000 แถวต่อ 1 ตารางในชุดข้อมูลที่ชื่อ ' ไม่มีข้อบังคับสำหรับการเก็บข้อมูล'  
* ขั้นตอนการโพสต์แถวอนุญาตให้มีเพียง 4000 ตัวอักษรต่อค่าตัวเลขในสตริงคอลัมน์
  
## <a name="see-also"></a>นอกจากนี้ โปรดดู

* [ข้อจำกัดและข้อปฏิบัติของบริการ Azure AD](/azure/active-directory/active-directory-service-limits-restrictions)   
* [ภาพรวมของ Power BI REST API](/rest/api/power-bi/)