---
title: เรียนรู้วิธีการทำงานของปุ่มในบริการ Power BI
description: สามารถใช้ปุ่มเพื่อเปิดการดำเนินการต่าง ๆ ซึ่งรวมถึงการนำทางในรายงาน การเข้าถึงรายละเอียด และการเข้าถึงรายละเอียดแบบข้ามรายงาน
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-explore
ms.topic: how-to
ms.date: 12/21/2020
LocalizationGroup: Reports
ms.openlocfilehash: 140ca42dc34e98133beac5fff671cf1ef244501c
ms.sourcegitcommit: 0711972326521944fdd8572403c0b15f31b916da
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/22/2020
ms.locfileid: "97721443"
---
# <a name="buttons-in-the-power-bi-service"></a>ปุ่มในบริการ Power BI
ในรายงานที่คุณได้รับจากเพื่อนร่วมงาน คุณอาจสังเกตเห็นปุ่มต่าง ๆ และสงสัยว่าจะใช้งานอย่างไร บางปุ่มมีคำศัพท์ บางปุ่มมีลูกศร บางปุ่มมีกราฟิก และบางปุ่มยังมีเมนูแบบดรอปดาวน์ด้วย บทความนี้จะสอนวิธีการรับรู้ปุ่มและวิธีการที่จะคิดออกว่าจะทำอย่างไรกับปุ่มดังกล่าว

## <a name="how-to-recognize-a-button"></a>วิธีการรับรู้ปุ่ม
ปุ่มสามารถมีลักษณะได้มากมาย เช่น รูปร่าง รูปภาพ หรือไอคอนในหน้ารายงาน แต่ถ้ามีการดำเนินการเกิดขึ้นเมื่อคุณเลือก (คลิก) วัตถุดังกล่าว อาจเป็นไปได้ว่าวัตถุนั้นอาจเป็นปุ่ม

## <a name="types-of-buttons"></a>ชนิดของปุ่ม
ผู้สร้างรายงานจะเพิ่มปุ่มในรายงานเพื่อช่วยให้คุณสามารถนำทางและสำรวจได้ ปุ่มบางประเภท ได้แก่ ย้อนกลับ บุ๊กมาร์ก ลูกศร ถามและ ตอบ วิธีใช้ และว่าง 

### <a name="back-buttons"></a>ปุ่ม ย้อนกลับ 
ปุ่มย้อนกลับอาจมีไอคอนลูกศรและเมื่อคุณเลือกแล้ว Power BI จะนำคุณกลับไปที่หน้าก่อนหน้า  ปุ่มย้อนกลับมักจะใช้กับการเข้าถึงรายละเอียด นี่คือตัวอย่างของปุ่มย้อนกลับที่ใช้กับการดูรายละเอียดเจาะลึก

1. ผู้ใช้ได้เลือก **Word** ในแผนภูมิแท่งและกำลังเจาะลึกถึง **การวิเคราะห์ตะกร้าตลาด**

    ![สกรีนช็อตของปุ่ม เข้าถึงรายละเอียด](media/end-user-buttons/power-bi-drillthrough.png)

2. โดยการเลือก **การวิเคราะห์ตะกร้าสินค้า** Power BI จะเปิดหน้ารายงาน *การวิเคราะห์ตะกร้าสินค้า* และใช้การเลือกที่สร้างขึ้นบนหน้าต้นทางเพื่อกรองสิ่งที่จะแสดงบนหน้าปลายทาง

    ![สกรีนช็อตของปุ่ม ย้อนกลับ](media/end-user-buttons/power-bi-back.png)

    ตอนนี้คุณอยู่ในหน้ารายงาน **การวิเคราะห์ตะกร้าตลาด** ซึ่งถูกกรองสำหรับ **Word** หากต้องการกลับไปที่หน้าก่อนหน้านี้ให้เลือกปุ่มย้อนกลับที่มีข้อความว่า **ย้อนกลับ** 

## <a name="bookmark-buttons"></a>ปุ่ม บุ๊กมาร์ก
รายงาน *นักออกแบบ* มักจะรวมบุ๊กมาร์กไว้ในรายงานของพวกเขา คุณสามารถดูรายการบุ๊กมาร์กรายงานได้โดยเลือก **บุ๊กมาร์ก** จากมุมขวาบน เมื่อผู้ออกแบบรายงานเพิ่ม *ปุ่ม* บุ๊กมาร์ก ซึ่งเป็นเพียงอีกวิธีหนึ่งในการนำทางไปยังหน้ารายงานเฉพาะที่เกี่ยวข้องกับบุ๊กมาร์กนั้น หน้านี้จะมีตัวกรองและการตั้งค่าที่ใช้งานอยู่ ซึ่งคั่นหน้าด้วยบุ๊กมาร์ก [เรียนรู้เพิ่มเติมเกี่ยวกับบุ๊กมาร์กใน Power BI](end-user-bookmarks.md) 

ในตัวอย่างนี้ ปุ่มมีไอคอนบุ๊กมาร์กและชื่อของบุ๊กมาร์ก คือ *เมือง* 

![ภาพหน้าจอของปุ่ม บุ๊กมาร์ก](media/end-user-buttons/power-bi-bookmark.png)

เมื่อเลือกปุ่มบุ๊กมาร์ก Power BI จะนำคุณไปยังตำแหน่งที่ตั้งและการตั้งค่าตามที่กำหนดไว้สำหรับบุ๊กมาร์กนั้น  ในกรณีนี้ บุ๊กมาร์กอยู่บนหน้ารายงาน *โอกาสการเติบโต* และหน้านั้นจะถูกกรองข้ามสำหรับ **เมือง**

![ภาพหน้าจอของหน้ารายงานที่ถูกกรองสำหรับเมือง](media/end-user-buttons/power-bi-urban.png)


## <a name="drillthrough-buttons"></a>ปุ่มการเข้าถึงรายละเอียด
มีแนวทางสองวิธีในการเจาะลึกรายละเอียดผ่านในบริการ Power BI การเข้าถึงรายละเอียดจะนำคุณไปยังหน้ารายงานอื่นและข้อมูลในหน้าปลายทางนั้นจะแสดงตามตัวกรองและการเลือกที่คุณได้ทำบนหน้าต้นทาง

วิธีหนึ่งในการใช้การดูรายละเอียดเจาะลึกในรายงานคือคลิกขวาที่จุดข้อมูลในภาพเลือก **ดูข้อมูลรายละเอียด** และเลือกปลายทาง วิธีการนี้อธิบายไว้ข้างต้นในส่วนที่ชื่อ **ปุ่มย้อนกลับ** แต่บางครั้งผู้ออกแบบรายงานใช้ *ปุ่ม* การเข้าถึงรายละเอียดแทน เพื่อให้การดำเนินการชัดเจนมากขึ้น และเรียกความสนใจไปยังข้อมูลเชิงลึกที่สำคัญ  

ปุ่ม การเข้าถึงรายละเอียด สามารถมีข้อกำหนดเบื้องต้นได้มากกว่าหนึ่งรายการ หากคุณไม่ปฏิบัติตามข้อกำหนดเบื้องต้นทั้งหมด ปุ่มจะไม่ทำงาน มาลองดูตัวอย่างกัน

ต่อไปนี้คือปุ่ม การเข้าถึงรายละเอียด ที่จะนำเราไปยังหน้า *รายละเอียดร้านค้า* การวางเมาส์เหนือปุ่มจะแสดงคำแนะนำเครื่องมือที่ช่วยให้เราทราบว่าเราต้องเลือกทั้งร้านค้าและผลิตภัณฑ์ จนกว่าเราจะเลือกหนึ่งรายการ ปุ่มก็ยังคงไม่ทำงาน

![สกรีนช็อตของปุ่มการเข้าถึงรายละเอียดพร้อมคำแนะนำเครื่องมือแบบโฮเวอร์](media/end-user-buttons/power-bi-drill-two-selections.png)

ตอนนี้เราได้เลือกผลิตภัณฑ์หนึ่งรายการ (**Word**) และร้านค้าหนึ่งรายการ (**ลีโอ**) ปุ่มจะเปลี่ยนสีเพื่อแจ้งให้เราทราบว่าขณะนี้มีการใช้งานอยู่

![สกรีนช็อตของปุ่มการเข้าถึงรายละเอียดร้านค้า](media/end-user-buttons/power-bi-select-both.png)

การเลือกปุ่ม การเข้าถึงรายละเอียด จะนำเราไปยังหน้ารายงาน *Store* หน้า *ร้านค้า* ถูกกรองสำหรับการเลือก **Word** และ **Leo** ของเรา

![สกรีนช็อตของหน้ารายงานร้านค้า](media/end-user-buttons/power-bi-store.png)

ปุ่ม การเข้าถึงรายละเอียดข้อมูล ยังสามารถมีเมนูแบบดรอปดาวน์ที่ให้คุณเลือกจุดหมายปลายทางได้ เมื่อคุณทำการเลือกในหน้ารายงานต้นทางแล้ว ให้เลือกหน้ารายงานปลายทางสำหรับการเข้าถึงรายละเอียดข้อมูล ในตัวอย่างด้านล่าง เรากำลังเปลี่ยนการเลือกของเราเป็นการดูรายละเอียดเจาะลึกไปที่หน้ารายงาน *รายละเอียดตลาด* 

![ภาพหน้าจอของเมนูแบบดรอปดาวน์ของปุ่มการเข้าถึงรายละเอียดข้อมูลที่มีหลายจุดหมายปลายทาง](media/end-user-buttons/power-bi-destination.png)

## <a name="page-navigation"></a>การนำทางเพจ

ปุ่มการนำทางของหน้าจะนำคุณไปยังหน้าอื่นในรายงานเดียวกัน ผู้ออกแบบรายงานมักสร้างปุ่มการนำทางเพื่อเล่าเรื่องราวหรือแนะนำคุณผ่านข้อมูลเชิงลึกของรายงาน ในตัวอย่างด้านล่าง ผู้ออกแบบรายงานได้เพิ่มปุ่มบนหน้ารายงานแต่ละหน้าซึ่งจะนำคุณกลับไปที่หน้าแรกซึ่งเป็นหน้าสรุประดับบนสุดในรายงาน ปุ่มการนำทางของหน้านี้มีประโยชน์เนื่องจากมีหลายหน้าในรายงานนี้

![สกรีนช็อตของปุ่มการนำทางของหน้าที่ชื่อดัชนีชี้วัดของทีม](media/end-user-buttons/power-bi-nav-button.png)


## <a name="qa-buttons"></a>ปุ่ม Q&A 
การเลือกปุ่ม Q&A จะเปิดหน้าต่าง Power BI Q&A Explorer หน้าต่าง Q&A ปรากฏที่ด้านบนของหน้ารายงานและสามารถปิดได้โดยเลือก X [เรียนรู้เกี่ยวกับ Q&A](end-user-q-and-a.md)

![สกรีนช็อตของหน้าต่าง Power BI Q&A Explorer พร้อมข้อความถามคำถามเกี่ยวกับข้อมูลของคุณ](media/end-user-buttons/power-bi-qna.png)

## <a name="web-url"></a>URL ของเว็บ
ปุ่ม URL ของเว็บเปิดหน้าต่างเบราว์เซอร์ใหม่ ผู้ออกแบบรายงานอาจเพิ่มปุ่มประเภทนี้เป็นแหล่งอ้างอิง เพื่อเชื่อมโยงไปยังเว็บไซต์ขององค์กรหรือหน้าความช่วยเหลือหรือแม้กระทั่งเป็นลิงก์ไปยังรายงานหรือแดชบอร์ดอื่น ในตัวอย่างด้านล่าง ปุ่ม URL ของเว็บช่วยให้คุณดาวน์โหลดไฟล์ต้นฉบับสำหรับรายงาน 

เนื่องจากหน้าจะเปิดขึ้นในหน้าต่างแยกต่าง ให้ปิดหน้าต่างหรือเลือกแท็บ Power BI ของคุณเพื่อกลับไปที่รายงาน Power BI

![ภาพหน้าจอของปุ่มดาวน์โหลด PBIX และหน้าต่างเบราว์เซอร์ใหม่ที่มีลิงก์ดาวน์โหลด](media/end-user-buttons/power-bi-url.png)

## <a name="next-steps"></a>ขั้นตอนถัดไป
[บุ๊กมาร์ก](end-user-bookmarks.md)    
[เจาะดูข้อมูลลึกขึ้น เจาะดูรายละเอียดแนวลึก](end-user-drill.md)
