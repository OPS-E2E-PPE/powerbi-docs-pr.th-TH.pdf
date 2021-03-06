---
title: สร้างพารามิเตอร์สำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI
description: ในบทความนี้ คุณจะได้เรียนวิธีการสร้างพารามิเตอร์สำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: report-builder
ms.topic: how-to
ms.date: 09/28/2020
ms.openlocfilehash: 7d874f2c9a7b8381ece151a4ac113bed5662c2e7
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418175"
---
# <a name="create-parameters-for-paginated-reports-in-the-power-bi-service"></a>สร้างพารามิเตอร์สำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI

[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)] 

ในบทความนี้ คุณจะได้เรียนวิธีการสร้างพารามิเตอร์สำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI  พารามิเตอร์ของรายงานให้วิธีการเลือกข้อมูลรายงานและทำให้การนำเสนอรายงานมีความหลากหลาย คุณสามารถระบุค่าเริ่มต้นและรายการของค่าที่พร้อมใช้งานได้ ผู้อ่านรายงานของคุณสามารถเปลี่ยนแปลงรายการที่เลือกได้ นอกจากนี้ พวกเขายังสามารถพิมพ์ลงในกล่องข้อความพารามิเตอร์เพื่อค้นหาค่า ดูที่ [ดูพารามิเตอร์สำหรับรายงานที่มีการแบ่งหน้า](../consumer/paginated-reports-view-parameters.md) เพื่อดูว่า ผู้ใช้ทางธุรกิจของคุณโต้ตอบกับพารามิเตอร์ต่างๆ ในบริการของ Power BI อย่างไร  

ภาพประกอบต่อไปนี้แสดงให้เห็นมุมมองออกแบบในตัวสร้างรายงาน Power BI สำหรับรายงานที่มีพารามิเตอร์ @BuyingGroup, @Customer, @FromDate และ @ToDate 
  
![พารามิเตอร์ในตัวสร้างรายงาน](media/paginated-reports-parameters/power-bi-paginated-parameters-report-builder.png)
  
1.  พารามิเตอร์ของรายงานในแผงข้อมูลรายงาน  
  
2.  ตารางพร้อมพารามิเตอร์หนึ่งตัวในชุดข้อมูล  
  
3.  แผงพารามิเตอร์ คุณสามารถกำหนดเค้าโครงของพารามิเตอร์ในแผงพารามิเตอร์ได้ 
  
4.  พารามิเตอร์ @FromDate และ @ToDate มีประเภทข้อมูลเป็น **DateTime** เมื่อดูรายงาน คุณสามารถพิมพ์วันที่ในกล่องข้อความหรือเลือกจากส่วนควบคุมปฏิทินได้ 

5.  พารามิเตอร์ตัวหนึ่งในกล่องโต้ตอบ **คุณสมบัติชุดข้อมูล**  

  
## <a name="create-or-edit-a-report-parameter"></a>สร้างหรือแก้ไขพารามิเตอร์ของรายงาน  
  
1.  เปิดรายงานแบบแบ่งหน้าในตัวสร้างรายงาน Power BI

1. ที่แผง **ข้อมูลรายงาน** ให้คุณคลิกขวาที่โหนด **พารามิเตอร์** > **เพิ่มพารามิเตอร์** กล่องโต้ตอบ **คุณสมบัติพารามิเตอร์ของรายงาน** จะเปิดขึ้น  
  
2.  ใน **ชื่อ** ให้คุณพิมพ์ชื่อสำหรับพารามิเตอร์หรือกดยอมรับชื่อเริ่มต้น  
  
3.  ใน **ข้อความตอบรับ** ให้คุณพิมพ์ข้อความที่จะแสดงข้างกล่องข้อความพารามิเตอร์เมื่อผู้ใช้เรียกใช้รายงาน  
  
4.  ใน **ชนิดข้อมูล** ให้คุณเลือกชนิดข้อมูลสำหรับค่าพารามิเตอร์  
  
5.  ถ้าพารามิเตอร์สามารถมีค่าว่างได้ ให้เลือก **อนุญาตให้มีค่าว่าง**  
  
6.  ถ้าพารามิเตอร์สามารถมีค่า Null ได้ ให้เลือก **อนุญาตให้มีค่า Null**  
  
7.  เลือก **อนุญาตให้มีหลายค่า** เพื่อให้ผู้ใช้เลือกค่าสำหรับพารามิเตอร์ได้มากกว่าหนึ่งค่า  
  
8.  ตั้งค่าตัวเลือกการมองเห็น  
  
    -   เลือก **มองเห็นได้** เพื่อแสดงพารามิเตอร์ในแถบเครื่องมือที่ด้านบนของรายงาน  
  
    -   เลือก **ซ่อน** เพื่อซ่อนพารามิเตอร์ไม่ให้แสดงในแถบเครื่องมือ  
  
    -   เลือก **ภายใน** เพื่อซ่อนพารามิเตอร์และปกป้องไว้จากการถูกดัดแปลงในเซิร์ฟเวอร์รายงานหลังจากที่เผยแพร่รายงานแล้ว จากนั้นพารามิเตอร์ของรายงานจะเห็นได้ในข้อกำหนดของรายงาน สำหรับตัวเลือกนี้ คุณต้องตั้งค่าเป็นค่าเริ่มต้นหรืออนุญาตให้พารามิเตอร์มีค่า Null ได้  
  
9. เลือก **ตกลง** 

## <a name="next-steps"></a>ขั้นตอนถัดไป

ดูที่ [ดูพารามิเตอร์สำหรับรายงานแบบแบ่งหน้า](../consumer/paginated-reports-view-parameters.md) เพื่อดูว่าพารามิเตอร์มีหน้าตาอย่างไรในบริการของ Power BI

สำหรับข้อมูลเชิงลึกเกี่ยวกับพารามิเตอร์ในรายงานที่มีการแบ่งหน้า ดู[พารามิเตอร์ของรายงานในตัวสร้างรายงาน Power BI](report-builder-parameters.md)
