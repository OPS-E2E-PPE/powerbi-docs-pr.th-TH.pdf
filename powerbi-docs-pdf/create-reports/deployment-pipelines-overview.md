---
title: ภาพรวมไปป์ไลน์การปรับใช้
description: เรียนรู้เกี่ยวกับไปป์ไลน์การปรับใช้ใน Power BI
author: KesemSharabi
ms.author: kesharab
ms.topic: conceptual
ms.service: powerbi
ms.subservice: pbi-deployment
ms.custom: contperf-fy21q1
ms.date: 10/21/2020
ms.openlocfilehash: ba2aedd4d503d468ba47640dd29fcfe004825ba5
ms.sourcegitcommit: 7bf09116163afaae312eb2b232eb7967baee2c92
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/17/2020
ms.locfileid: "97621130"
---
# <a name="introduction-to-deployment-pipelines"></a>บทนำเกี่ยวกับขั้นตอนการปรับใช้งาน

ในโลกปัจจุบัน การวิเคราะห์ถือเป็นส่วนสำคัญของการตัดสินใจในเกือบทุกองค์กร การใช้งาน Power BI ในฐานะเครื่องมือวิเคราะห์ ที่เพิ่มขึ้นนั้นจำเป็นต้องใช้ข้อมูลมากขึ้น ต้องให้ดูน่าสนใจ และใช้งานง่าย อย่างไรก็ตามเหนือสิ่งอื่นใดนั้น Power BI จำเป็นต้องพร้อมให้ใช้งาน และเชื่อถือได้อยู่เสมอ เพื่อให้เป็นไปตามข้อกำหนดเหล่านี้ ผู้สร้าง BI จำเป็นต้องทำงานร่วมกันอย่างมีประสิทธิภาพ

เครื่องมือไปป์ไลน์การปรับใช้จะช่วยให้ผู้สร้าง BI จัดการวงจรชีวิตของเนื้อหาเชิงองค์กรได้ เครื่องมือนี้เป็นเครื่องมือที่ทรงประสิทธิภาพและนำกลับมาใช้งานใหม่ได้สำหรับผู้สร้างในองค์กรที่ใช้ความจุแบบ Premium ไปป์ไลน์การปรับใช้ช่วยให้ผู้สร้างสามารถพัฒนาและทดสอบเนื้อหาของ Power BI ก่อนที่ผู้ใช้จะนำเนื้อหาไปใช้งานได้ ชนิดของเนื้อหาดังกล่าวประกอบด้วยรายงาน แดชบอร์ด และชุดข้อมูล

เครื่องมือได้รับการออกแบบมาเป็นไปป์ไลน์ที่มีสามขั้นตอนดังนี้:

* **<a name="development"></a>การพัฒนา**
    
    ขั้นตอนนี้ใช้เพื่อออกแบบ สร้าง และอัปโหลดเนื้อหาใหม่กับผู้สร้างคนอื่นๆ ขั้นตอนนี้เป็นขั้นแรกในไปป์ไลน์การปรับใช้

* **<a name="test"></a>การทดสอบ**

    คุณจะพร้อมเข้าสู่ขั้นตอนการทดสอบทันที หลังจากที่คุณทำการเปลี่ยนแปลงที่จำเป็นทั้งหมดต่อเนื้อหาของคุณแล้ว คุณเพียงแค่อัปโหลดเนื้อหาที่ปรับเปลี่ยนแล้วขึ้นไป เพื่อให้สามารถไปยังขั้นตอนการทดสอบนี้ได้ นี่คือตัวอย่างสามของสิ่งที่คุณสามารถทำได้ในสภาพแวดล้อมการทดสอบ:

    * แชร์เนื้อหากับผู้ทดสอบและผู้รีวิว

    * โหลดและเรียกใช้การทดสอบในปริมาณข้อมูลขนาดใหญ่

    * ทดสอบแอปของคุณเพื่อดูว่าผู้ใช้ของคุณจะมองเห็นแอปในลักษณะใด

* **<a name="production"></a>การผลิต**

    หลังทดสอบเนื้อหาแล้ว ให้ใช้ขั้นตอนการผลิตเพื่อแชร์เนื้อหาเวอร์ชันสุดท้ายของคุณกับผู้ใช้ทางธุรกิจทั่วทั้งองค์กร

![สกรีนช็อตของไปป์ไลน์การปรับใช้งานที่มีทั้งสามขั้นตอน ได้แก่ การพัฒนา การทดสอบและการผลิต การเพิ่มข้อมูล](media/deployment-pipelines-overview/deployment-pipelines.png)

## <a name="next-steps"></a>ขั้นตอนถัดไป

>[!div class="nextstepaction"]
>[เริ่มต้นกับไปป์ไลน์การปรับใช้](deployment-pipelines-get-started.md)

>[!div class="nextstepaction"]
>[ทำความเข้าใจกระบวนการไปป์ไลน์การปรับใช้](deployment-pipelines-process.md)

>[!div class="nextstepaction"]
>[การแก้ไขปัญหาไปป์ไลน์การปรับใช้](deployment-pipelines-troubleshooting.md)

>[!div class="nextstepaction"]
>[แนวทางปฏิบัติที่ดีที่สุดสำหรับไปป์ไลน์การปรับใช้](deployment-pipelines-best-practices.md)
