---
title: ข้อมูลเบื้องต้นเกี่ยวกับกระแสข้อมูลและการเตรียมข้อมูลด้วยตนเอง
description: ภาพรวมเกี่ยวกับกระแสข้อมูล Power BI คืออะไรและควรใช้เมื่อใด
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-dataflows
ms.topic: how-to
ms.date: 10/01/2020
LocalizationGroup: Data from files
ms.openlocfilehash: 5dde70b9834d990987e42c6aa945940a7f110949
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96416082"
---
# <a name="introduction-to-dataflows-and-self-service-data-prep"></a>ข้อมูลเบื้องต้นเกี่ยวกับกระแสข้อมูลและการเตรียมข้อมูลด้วยตนเอง

เมื่อปริมาณข้อมูลเพิ่มขึ้นเรื่อยๆ ความท้าทายในการทำ Data Wrangling ให้ข้อมูลนั้นเป็นระเบียบและสามารถดำเนินการได้ก็เพิ่มขึ้นเช่นกัน เราต้องการข้อมูลที่พร้อมสำหรับการวิเคราะห์ เพื่อใช้กับวิชวล รายงานและแดชบอร์ด เพื่อให้เราเปลี่ยนปริมาณข้อมูลให้เป็นข้อมูลเชิงลึกที่ดำเนินการได้อย่างรวดเร็ว ด้วยการเตรียมข้อมูลด้วยตนเอง สำหรับข้อมูลใหญ่ใน Power BI คุณสามารถเปลี่ยนข้อมูลให้เป็นข้อมูลเชิงลึกของ Power BI ได้โดยคลิกเพียงไม่กี่ครั้ง

![กระแสของข้อมูล](media/dataflows-introduction-self-service-flow.png)

## <a name="when-to-use-dataflows"></a>คุณควรใช้กระแสข้อมูลเมื่อใด

กระแสข้อมูลได้รับการออกแบบมาเพื่อรองรับสถานการณ์ต่อไปนี้:

* สร้างตรรกะการแปลงข้อมูลที่นำมาใช้ใหม่ได้ ซึ่งคุณสามารถแชร์กับชุดข้อมูลและรายงานจำนวนมากภายใน Power BI กระแสข้อมูลส่งเสริมความสามารถในการนำมาใช้ใหม่ขององค์ประกอบข้อมูลเบื้องต้น ทำให้ไม่จำเป็นต้องสร้างการเชื่อมต่อแยกกับระบบคลาวด์หรือแหล่งข้อมูลภายในองค์กร

* เปิดเผยข้อมูลในที่เก็บข้อมูล Azure Data Lake Gen 2 ของคุณเอง ทำให้คุณสามารถเชื่อมต่อบริการ Azure อื่น ๆ กับข้อมูลเบื้องต้นที่เป็นข้อมูลดิบได้

* สร้างแหล่งที่มาจริงเพียงแหล่งเดียวโดยบังคับให้นักวิเคราะห์เชื่อมต่อกับกระแสข้อมูล แทนที่จะเชื่อมต่อกับระบบเบื้องต้น ให้คุณควบคุมได้ว่าจะเข้าถึงข้อมูลใดและจะเปิดเผยข้อมูลอย่างไรกับผู้สร้างรายงาน นอกจากนี้ คุณยังสามารถแมปข้อมูลกับข้อกำหนดมาตรฐานอุตสาหกรรม ทำให้คุณสามารถสร้างมุมมองที่ดูแลจัดการอย่างเป็นระเบียบเรียบร้อย ซึ่งสามารถทำงานร่วมกับบริการและผลิตภัณฑ์อื่น ๆ ใน Power Platform ได้

* ถ้าคุณต้องการทำงานกับปริมาณข้อมูลขนาดใหญ่และดำเนินการ ETL ในระดับมาตราส่วน กระแสข้อมูลที่มีมาตราส่วน Power BI Premium มีประสิทธิภาพมากกว่าและช่วยให้คุณมีความยืดหยุ่นมากขึ้น กระแสข้อมูลสนับสนุนระบบคลาวด์และแหล่งข้อมูลภายในองค์กรที่หลากหลาย 

* ป้องกันไม่ให้นักวิเคราะห์เข้าถึงแหล่งข้อมูลเบื้องต้นได้โดยตรง เนื่องจากผู้สร้างรายงานสามารถสร้างส่วนบนของกระแสข้อมูลได้ จึงอาจสะดวกกว่าสำหรับคุณในการอนุญาตให้บุคคลเพียงไม่กี่คนเข้าถึงแหล่งข้อมูลเบื้องต้นได้ จากนั้นจึงให้การเข้าถึงกระแสข้อมูลเพื่อให้นักวิเคราะห์สร้างขึ้นอยู่ด้านบน วิธีนี้ช่วยลดภาระให้กับระบบเบื้องต้นและช่วยให้ผู้ดูแลระบบสามารถควบคุมได้ดียิ่งขึ้นเมื่อระบบโหลดจากการรีเฟรช

เมื่อคุณได้สร้างกระแสข้อมูล คุณจะสามารถใช้ Power BI Desktop และบริการของ Power BI เพื่อสร้างชุดข้อมูล รายงาน แดชบอร์ด และแอปที่ใช้ประโยชน์จาก Common Data Model เพื่อขับเคลื่อนข้อมูลเชิงลึกให้กับกิจกรรมทางธุรกิจของคุณ การวางกำหนดการรีเฟรชกระแสข้อมูลได้รับการจัดการโดยตรงจากพื้นที่ทำงานที่ใช้สร้างกระแสข้อมูล เช่นเดียวกับชุดข้อมูลของคุณ

## <a name="next-steps"></a>ขั้นตอนถัดไป
บทความนี้ใช้ภาพรวมของการเตรียมข้อมูลด้วยตนเองสำหรับข้อมูลขนาดใหญ่ใน Power BI และวิธีการใช้งานหลายวิธี 

บทความต่อไปนี้ให้ข้อมูลเพิ่มเติมเกี่ยวกับกระแสข้อมูลและ Power BI:

* [การสร้างกระแสข้อมูล](dataflows-create.md)
* [กำหนดค่าและใช้กระแสข้อมูล](dataflows-configure-consume.md)
* [การกำหนดค่าที่จัดเก็บกระแสข้อมูลเพื่อใช้ Azure Data Lake Gen 2](dataflows-azure-data-lake-storage-integration.md)
* [ฟีเจอร์พรีเมียมของกระแสข้อมูล](dataflows-premium-features.md)
* [AI กับกระแสข้อมูล](dataflows-machine-learning-integration.md)
* [ข้อจำกัดและข้อควรพิจารณาของกระแสข้อมูล](dataflows-features-limitations.md)
* [แนวทางปฏิบัติที่ดีที่สุดสำหรับกระแสข้อมูล](dataflows-best-practices.md)


สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Common Data Model สามารถดูได้ในบทความภาพรวม:
* [Common Data Model - ภาพรวม](/powerapps/common-data-model/overview)