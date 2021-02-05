---
title: ปรับขนาดความจุ Power BI Embedded สำหรับโซลูชัน BI แบบฝังตัวของการวิเคราะห์แบบฝังของ Power BI ของคุณ
description: บทความนี้แนะนำเกี่ยวกับวิธีการปรับขนาดความจุ Power BI Embedded ใน Microsoft Azure สำหรับโซลูชัน BI แบบฝังตัวของการวิเคราะห์แบบฝังของ Power BI ของคุณ
author: KesemSharabi
ms.author: kesharab
services: power-bi-embedded
editor: ''
tags: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: how-to
ms.date: 01/31/2019
ms.openlocfilehash: 19dfff03e2ec17c2b969a80c9fe0d2087c189184
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887327"
---
# <a name="scale-your-power-bi-embedded-capacity-in-the-azure-portal"></a>ปรับขนาดความจุ Power BI Embedded ในพอร์ทัล Azure

บทความนี้แนะนำเกี่ยวกับวิธีการปรับขนาดความจุ Power BI Embedded ใน Microsoft Azure การปรับขนาดช่วยให้คุณสามารถเพิ่มหรือลดขนาดความจุของคุณได้

ซึ่งถือว่า คุณได้สร้างขีดความจุ Power BI Embedded แล้ว หากคุณยังไม่ได้สร้าง ให้ดู[สร้างความจุ Power BI Embedded ในพอร์ทัล Azure](azure-pbie-create-capacity.md) เพื่อเริ่มใช้งาน

> [!NOTE]
> การดำเนินการปรับขนาดอาจใช้เวลาประมาณหนึ่งนาที ในช่วงเวลานี้ จะไม่สามารถใช้งานความจุได้ การโหลดเนื้อหาแบบฝังตัวอาจล้มเหลว

## <a name="scale-a-capacity"></a>ปรับขนาดความจุ

1. ลงชื่อเข้าใช้[พอร์ทัล Azure](https://portal.azure.com/)

2. เลือก **บริการทั้งหมด** > **Power BI Embedded** เพื่อดูความจุของคุณ

    ![บริการทั้งหมดภายในพอร์ทัล Azure](media/azure-pbie-scale-capacity/azure-portal-more-services.png)

3. เลือกความจุที่คุณต้องการปรับขนาด

    ![รายการความจุ Power BI Embedded ในพอร์ทัล Azure](media/azure-pbie-scale-capacity/azure-portal-capacity-list.png)

4. เลือก **ระดับราคา** ภายใต้ **มาตราส่วน** ภายในความจุของคุณ

    ![ตัวเลือกระดับราคาภายใต้มาตราส่วน](media/azure-pbie-scale-capacity/azure-portal-scale-pricing-tier.png)

    ระดับการกำหนดราคาปัจจุบันของคุณจะมีกรอบเป็นสีฟ้า

    ![ระดับการกำหนดราคาปัจจุบันของคุณจะมีกรอบเป็นสีฟ้า](media/azure-pbie-scale-capacity/azure-portal-current-tier.png)

5. เมื่อต้องการปรับมาตราส่วนขึ้นหรือลง เลือกระดับใหม่เพื่อย้ายไปยังตำแหน่งที่ต้องการ การเลือกระดับใหม่จะวางเส้นขอบสีฟ้าล้อมรอบบริเวณที่เลือกไว้ เลือก **เลือก** เพื่อปรับขนาดเป็นระดับใหม่

    ![เลือกระดับใหม่](media/azure-pbie-scale-capacity/azure-portal-select-new-tier.png)

    การปรับขนาดความจุของคุณอาจใช้เวลาสักครู่หรือสองนาทีจึงจะเสร็จสมบูรณ์

6. ยืนยันระดับของคุณโดยดูจากแท็บภาพรวม ระดับการกำหนดราคาปัจจุบันจะแสดงอยู่ในรายการ

    ![ยืนยันระดับปัจจุบัน](media/azure-pbie-scale-capacity/azure-portal-confirm-tier.png)

## <a name="next-steps"></a>ขั้นตอนถัดไป

ในการหยุดชั่วคราวหรือเริ่มต้นความจุของคุณ ให้ดูที[่หยุดชั่วคราวและเริ่มต้นความจุ Power BI Embedded ในพอร์ทัล Azure](azure-pbie-pause-start.md)

ในการเริ่มต้นฝังเนื้อหา Power BI ในแอปพลิเคชันของคุณ โปรดดูที่[วิธีฝังแดชบอร์ด รายงาน และไทล์ใน Power BI ของคุณ](https://powerbi.microsoft.com/documentation/powerbi-developer-embedding-content/)

มีคำถามเพิ่มเติมหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)
