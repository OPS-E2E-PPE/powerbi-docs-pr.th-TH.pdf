---
title: บริการ Power BI - แนวคิดพื้นฐานสำหรับผู้ใช้ทางธุรกิจ
description: พื้นที่ทำงาน แดชบอร์ด รายงาน ชุดข้อมูล และเวิร์กบุ๊กของแอปบริการ Power BI
author: mihart
ms.reviewer: mihart
featuredvideoid: B2vd4MQrz4M
ms.service: powerbi
ms.custom: seodec18
ms.subservice: powerbi-consumer
ms.topic: conceptual
ms.date: 10/08/2020
ms.author: mihart
LocalizationGroup: Get started
ms.openlocfilehash: 5c534436b93205d40251c26830be4d6acdfa034d
ms.sourcegitcommit: 6b436f6ed872cbc040ed6e2d3ac089c08fc78daf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/09/2020
ms.locfileid: "91928469"
---
# <a name="basic-concepts-for-the-power-bi-service-consumers"></a>แนวคิดพื้นฐานสำหรับลูกค้าที่ใช้บริการ Power BI

[!INCLUDE[consumer-appliesto-ynnm](../includes/consumer-appliesto-ynnm.md)]

[!INCLUDE [power-bi-service-new-look-include](../includes/power-bi-service-new-look-include.md)]

บทความนี้อนุมานว่าคุณได้อ่าน [ภาพรวม Power BI](../fundamentals/power-bi-overview.md) และได้ระบุว่าตัวเองเป็น[ผู้ใช้ทางธุรกิจของ Power BI](end-user-consumer.md) *ผู้ใช้ทางธุรกิจ* ได้รับเนื้อหา Power BI เช่น แดชบอร์ด รายงาน และแอปจากเพื่อนร่วมงาน *ผู้ใช้ทางธุรกิจ* ทำงานกับบริการของ Power BI (app.powerbi.com) ซึ่งเป็นเวอร์ชันที่ใช้ในเว็บไซต์ของ Power BI

การรับเนื้อหาจากผู้อื่นต้องใช้หนึ่งในรายการต่อไปนี้:
- สิทธิการใช้งานผู้ใช้ Power BI Pro
- องค์กรของคุณมีการสมัครใช้งานสำหรับ Power BI Premium และเนื้อหาที่จะใช้ร่วมกันกับคุณจากความจุ Power BI Premium [ค้นหาสิทธิการใช้งานและชนิดการสมัครใช้งานของคุณ](end-user-license.md)

คุณจะได้ยินคำว่า "Power BI Desktop" หรือแค่ "Desktop" เป็นเครื่องมือแบบสแตนด์อโลนใช้งานโดย *นักออกแบบ* ที่สร้างและแชร์แดชบอร์ดและรายงานกับคุณ สิ่งสำคัญคือต้องทราบว่ายังมีเครื่องมือ Power BI อื่นๆ อีก ตราบใดที่คุณเป็นผู้ใช้ทางธุรกิจ** คุณจะทำงานกับเฉพาะบริการ Power BI เท่านั้น บทความนี้นำไปใช้กับบริการ Power BI เท่านั้น

## <a name="terminology-and-concepts"></a>คำศัพท์และแนวคิด

บทความนี้ไม่ได้นำเสนอภาพของ Power BI หรือมีบทช่วยสอนแบบลงมือทำ แต่เรานำเสนอเป็นบทความภาพรวมซึ่งจะทำให้คุณเข้าใจคำศัพท์และแนวคิดเกี่ยวกับ Power BI การนำเสนอจะสอนคุณเกี่ยวกับคำศัพท์และลักษณะทั่วไป สำหรับการแนะนำของบริการ Power BI และการนำทาง ให้ไปที่[เริ่มต้นใช้งานด่วน - ทัวร์ในบริการ Power BI](end-user-experience.md)

## <a name="open-the-power-bi-service-for-the-first-time"></a>เปิดบริการ Power BI เป็นครั้งแรก

*ผู้ใช้ทางธุรกิจ* Power BI ส่วนใหญ่จะได้รับบริการ Power BI เนื่องจาก 1)บริษัทซื้อใบอนุญาตและ 2)ผู้ดูแลระบบมอบหมายใบอนุญาตแก่พนักงาน

เมื่อต้องเริ่มต้นใช้งาน เปิดเบราว์เซอร์และพิมพ์ **app.powerbi.com** ในครั้งแรกที่คุณเปิดบริการ Power BI คุณจะเห็นสิ่งนี้:

![สกรีนช็อตของหน้าจอยินดีต้อนรับสำหรับบริการ Power BI](media/end-user-basic-concepts/power-bi-home-open.png)

เมื่อคุณใช้บริการ Power BI คุณจะต้องปรับเปลี่ยนสิ่งที่คุณเห็นเมื่อเปิดเว็บไซต์ในแต่ละครั้ง ตัวอย่างเช่น บางคนชอบ Power BI เพื่อเปิดไปยัง **หน้าแรก** ในขณะที่คนอื่นมีแดชบอร์ดที่ชื่นชอบที่พวกเขาต้องการเห็นเป็นอันดับแรก ไม่ต้องกังวล สองบทความนี้จะสอนวิธีการปรับแต่งประสบการณ์การใช้งานของคุณ

- [ขอแนะนำหน้าแรกของ Power BI และการค้นหาในส่วนกลาง](https://powerbi.microsoft.com/blog/introducing-power-bi-home-and-global-search)

- [แดชบอร์ดแนะนำใน Power BI service](end-user-featured.md)

![สกรีนช็อตที่แสดงมุมมองหน้าแรกและมุมมองแดชบอร์ด](media/end-user-basic-concepts/power-bi-dash-home.png)

แต่ก่อนที่เราจะได้รับประโยชน์มากขึ้น ลองกลับมาพูดคุยเกี่ยวกับบล็อกการสร้างที่ประกอบเป็นบริการ Power BI

_______________________________________________________

## <a name="power-bi-content"></a>เนื้อหา Power BI

### <a name="introduction-to-building-blocks"></a>ความรู้เบื้องต้นเกี่ยวกับบล็อกการสร้าง

สำหรับ *ผู้ใช้ทางธุรกิจ* ของ Power BI บล็อกการสร้าง 5 กลุ่มคือ: **_การแสดงภาพข้อมูล_** , **_แดชบอร์ด_** , **_รายงาน_** , **_แอป_** และ **_ชุดข้อมูล_** สิ่งเหล่านี้บางครั้งเรียกว่าเนื้อหา *Power BI* **_content_** *เนื้อหา* มีอยู่ใน **_พื้นที่ทำงาน_** เวิร์กโฟลว์ทั่วไปที่เกี่ยวข้องกับบล็อกการสร้างทั้งหมด: *ผู้ออกแบบ* Power BI (สีเหลืองในแผนภาพด้านล่าง) จะรวบรวมข้อมูลจาก *ชุดข้อมูล* นำมาสู่ Power BI เพื่อการวิเคราะห์ สร้าง *รายงาน* ที่เต็มไปด้วย *การแสดงภาพข้อมูล* ที่เน้นข้อเท็จจริงและข้อมูลเชิงลึกที่น่าสนใจ ปักหมุดการแสดงภาพข้อมูลจากรายงานไปยัง *แดชบอร์ด* และแชร์รายงานและแดชบอร์ดกับ *ผู้ใช้ทางธุรกิจ* เช่นคุณ (สีดำในแผนภาพด้านล่าง) *นักออกแบบ* แชร์ในรูปแบบของแดชบอร์ด รายงาน หรือแอป

![พื้นฐาน Power BI แผนภูมิลำดับงาน](media/end-user-basic-concepts/power-bi-workflow.png)

สำหรับคุณสมบัติพื้นฐานที่สุด:

- ![สกรีนช็อตของไอคอนแสดงภาพ](media/end-user-basic-concepts/visual.png) **_การแสดงผลด้วยภาพ_** (หรือ *วิชวล* ) คือแผนภูมิประเภทหนึ่งที่สร้างด้วย *ตัวออกแบบ* Power BI ภาพแสดงข้อมูลจาก *รายงาน* และ *ชุดข้อมูล* โดยทั่วไปแล้ว *ผู้ออกแบบ* จะสร้างวิชวลใน Power BI Desktop

    สำหรับรายละเอียดเพิ่มเติม ให้ดูที่ [โต้ตอบกับการแสดงภาพในรายงาน แดชบอร์ด และแอป](end-user-visualizations.md)

- ![สกรีนช็อตของไอคอนฐานข้อมูล](media/end-user-basic-concepts/power-bi-dataset-icon.png) *ชุดข้อมูล* คือที่เก็บข้อมูล ตัวอย่างเช่น อาจเป็นไฟล์ Excel จากองค์กรอนามัยโลก อาจเป็นฐานข้อมูลของบริษัทของลูกค้า หรืออาจเป็นไฟล์ Salesforce ชุดข้อมูลได้รับการจัดการโดย *นักออกแบบ*

- ![สกรีนช็อตของไอคอนแดชบอร์ด](media/end-user-basic-concepts/dashboard.png) *แดชบอร์ด* เป็นหน้าจอเดียวที่มีภาพ ข้อความ และกราฟฟิคแบบโต้ตอบ หน้าแดชบอร์ดจะเก็บรวบรวมเมตริกที่สำคัญที่สุดของคุณในหนึ่งหน้าจอเพื่อบอกเล่าเรื่องราวหรือตอบคำถาม เนื้อหาในหน้าแดชบอร์ดมาจากรายงานอย่างน้อยหนึ่งรายการและชุดข้อมูลอย่างน้อยหนึ่งชุด

    สำหรับข้อมูลเพิ่มเติม ให้ดูที่[แดชบอร์ดสำหรับ Power BI บริการผู้ใช้ทางธุรกิจ](end-user-dashboards.md)

- ![สกรีนช็อตของไอคอนรายงาน](media/end-user-basic-concepts/report.png) *รายงาน* คือหน้าของภาพ ข้อความ และกราฟฟิคแบบโต้ตอบอย่างน้อยหนึ่งหน้าซึ่งรวมกันเป็นรายงานเดียว Power BI สร้างรายงานโดยอ้างอิงจากชุดข้อมูลเดียว บ่อยครั้งที่ *นักออกแบบ* จัดระเบียบหน้ารายงานให้อยู่ในพื้นที่ส่วนกลางของความสนใจหรือตอบคำถามเดียว

    สำหรับข้อมูลเพิ่มเติม ให้ดูที่[รายงานใน Power BI](end-user-reports.md)

- ![สกรีนช็อตของไอคอนแอป](media/end-user-basic-concepts/app.png) *แอป* เป็นอีกวิธีหนึ่งสำหรับ *ผู้ออกแบบ* ในการจัดกลุ่มและแบ่งปันหน้าแดชบอร์ดและรายงานที่เกี่ยวข้องกัน *ผู้ใช้ทางธุรกิจ* ได้รับแอปบางอย่างโดยอัตโนมัติ แต่สามารถไปหาแอปอื่น ๆ ที่เพื่อนร่วมงานหรือชุมชนสร้างขึ้นได้ ตัวอย่างเช่นแอปพลิเคชันที่ใช้งานไม่ได้สำหรับบริการภายนอกที่คุณอาจใช้อยู่แล้วเช่น Google Analytics และ Microsoft Dynamics CRM

เพื่อความชัดเจน หากคุณเป็นผู้ใช้ใหม่ และคุณลงชื่อเข้าใช้บริการ Power BI เป็นครั้งแรก คุณอาจจะยังไม่เห็นแดชบอร์ด แอปพลิเคชัน หรือรายงานที่ถูกแชร์

_______________________________________________________

## <a name="datasets"></a>ชุดข้อมูล

*ชุดข้อมูล* คือคอลเลกชันข้อมูลที่ *ผู้ออกแบบ* นำเข้าหรือเชื่อมต่อและใช้เพื่อสร้างรายงานและแดชบอร์ด ในฐานะ *ผู้ใช้ทางธุรกิจ* คุณจะไม่โต้ตอบกับชุดข้อมูลโดยตรง แต่ก็ยังดีที่จะเรียนรู้ว่าชุดข้อมูลพอดีกับภาพที่ใหญ่ขึ้นอย่างไร  

ชุดข้อมูลแต่ละชุดแสดงมาจากแหล่งข้อมูลเดียว ตัวอย่างเช่น แหล่งข้อมูลอาจเป็นสมุดงาน Excel บน OneDrive, ชุดข้อมูลแบบตาราง SQL Server Analysis Services ภายในองค์กร หรือชุดข้อมูล Salesforce Power BI สนับสนุนแหล่งข้อมูลต่าง ๆ มากมาย

เมื่อนักออกแบบแชร์แอปกับคุณ คุณสามารถค้นหาชุดข้อมูลที่กำลังใช้งานได้โดยการเปิด **เนื้อหาที่เกี่ยวข้อง**  คุณจะไม่สามารถเพิ่มหรือเปลี่ยนแปลงสิ่งใดในชุดข้อมูล แต่ถ้านักออกแบบให้สิทธิ์คุณ คุณจะสามารถดาวน์โหลดรายงานให้ค้นหา [ข้อมูลเชิงลึก ในข้อมูล](end-user-insights.md)หรือแม้กระทั่ง [สร้างรายงานของคุณเอง](../create-reports/service-report-create-new.md) โดยยึดตามชุดข้อมูล  

![สกรีนช็อตของหน้าผู้ใช้งาน Power BI และลูกศรชี้ไปยังส่วนชุดข้อมูลบนพื้นที่](media/end-user-basic-concepts/power-bi-datasets.png)

หนึ่งชุดข้อมูล...

- ตัวออกแบบรายงานเพื่อสร้างแดชบอร์ดและรายงานสามารถใช้ซ้ำได้เรื่อยๆ

- สามารถใช้ในการสร้างรายงานต่าง ๆ ได้มากมาย

- การแสดงภาพจากชุดข้อมูลเดียวสามารถแสดงในหลายๆ แดชบอร์ดได้

  ![กราฟิกที่แสดงความสัมพันธ์ของชุดข้อมูลที่มีต่อหลายๆ กลุ่มและกลุ่มเดียว](media/end-user-basic-concepts/drawing2.png)

ไปที่บล็อกการสร้างถัดไป - การแสดงภาพข้อมูล

_______________________________________________________

## <a name="visualizations"></a>การแสดงผลข้อมูลด้วยภาพ

การแสดงภาพ (หรือที่รู้จักกันในนามวิชวล) แสดงข้อมูลเชิงลึกที่ Power BI ค้นพบในข้อมูล การแสดงภาพข้อมูลทำให้เข้าใจได้ง่ายขึ้นเนื่องจากสมองของคุณสามารถเข้าใจภาพได้เร็วกว่ากระดาษคำนวณตัวเลข

เพียงบางส่วนของการแสดงภาพข้อมูลที่คุณพบใน Power BI ได้แก่ น้ำตก ริบบิ้น แผนที่ต้นไม้ พาย กรวย การ์ด กระจาย และเกจวัด

   ![สกรีนช็อตของ 8 ตัวอย่างวิชวล](media/end-user-basic-concepts/power-bi-visuals.png)

ดู [รายการทั้งหมดของการแสดงภาพที่มาพร้อมกับ Power BI](end-user-visual-type.md)

การแสดงภาพข้อมูลพิเศษที่เรียกว่า *ภาพแบบกำหนดเอง* สามารถเรียกใช้งานได้จากชุมชน หากคุณได้รับรายงานด้วยภาพที่คุณไม่รู้จัก เป็นไปได้ว่าอาจเป็นภาพแบบกำหนดเอง หากคุณต้องการความช่วยเหลือในการแปลภาพแบบกำหนดเองค้นหาชื่อ *ผู้ออกแบบ* ของรายงานหรือแดชบอร์ด และติดต่อเขา ข้อมูลที่ติดต่อพร้อมใช้งานโดยการเลือกชื่อเรื่องจากแถบเมนูด้านบน

หนึ่งจากการแสดงภาพในรายงาน...

- สามารถปรากฏหลายครั้งในรายงานเดียวกันได้

- สามารถปรากฏบนแดชบอร์ดที่แตกต่างกันได้

_______________________________________________________

## <a name="reports"></a>รายงาน

รายงาน Power BI คือหน้าเพจที่แสดงภาพ กราฟิก และข้อความอย่างน้อยหนึ่งหน้า การแสดงภาพทั้งหมดในรายงานมาจากชุดข้อมูลเดียว *ผู้ออกแบบ* สร้างหน้ารายงานและแชร์ให้กับผู้อื่น; เป็นรายบุคคลหรือเป็นส่วนหนึ่งของแอปพลิเคชัน  โดยทั่วไปแล้ว *ผู้ใช้ทางธุรกิจ* [โต้ตอบกับรายงานใน *มุมมองการอ่าน*](end-user-reading-view.md)

![สกรีนช็อตของรายงานที่มีแท็บ](media/end-user-basic-concepts/power-bi-report.png)

หนึ่งรายงาน...

- สามารถเชื่อมโยงกับหลายแดชบอร์ดได้ (ไทล์ที่ปักหมุดจากรายงานนั้นอาจปรากฏบนหลายแดชบอร์ด)

- สามารถสร้างได้โดยใช้ข้อมูลจากชุดเดียวเท่านั้น  

- สามารถเป็นส่วนหนึ่งของแอปได้หลายแอป

  ![กราฟิกที่แสดงความสัมพันธ์สำหรับรายงาน](media/end-user-basic-concepts/drawing5.png)

_______________________________________________________

## <a name="dashboards"></a>แดชบอร์ด

แดชบอร์ดรายการแสดงมุมมองแบบกราฟิกที่กำหนดเองของชุดย่อยบางรายการของชุดข้อมูลเบื้องต้น *ผู้ออกแบบ* สร้างหน้าแดชบอร์ดและแชร์ให้กับ *ผู้ใช้ทางธุรกิจ* ; เป็นรายบุคคลหรือเป็นส่วนหนึ่งของแอปพลิเคชัน แดชบอร์ดเป็นพื้นที่ทำงานเดี่ยวที่มี *ไทล์* กราฟิก และข้อความ

  ![สกรีนช็อตของตัวอย่างแดชบอร์ด](media/end-user-basic-concepts/power-bi-dashboard.png)

ไทล์เป็นการแสดงผลภาพที่ *ผู้ออกแบบ* *ปัดหมุด* ตัวอย่างเช่น จากรายงานไปยังแดชบอร์ด แต่ละไทล์ที่ปักหมุดจะแสดง [การแสดงภาพ](end-user-visualizations.md) ที่ผู้ออกแบบ สร้างขึ้นจากชุดข้อมูลและปักหมุดลงบนแดชบอร์ด ไทล์อาจประกอบด้วยทั้งหน้ารายงาน และสามารถประกอบด้วยข้อมูลการสตรีมแบบสดหรือวิดีโอ มีหลายวิธีที่ *ผู้ออกแบบ* เพิ่มไทล์ลงในแดชบอร์ด แต่มีจำนวนมากที่ครอบคลุมบทความภาพรวมนี้ เมื่อต้องการเรียนรู้เพิ่มเติม ดู[ไทล์แดชบอร์ดใน Power BI](end-user-tiles.md)

*ผู้ใช้ทางธุรกิจ* ไม่สามารถแก้ไขแดชบอร์ด อย่างไรก็ตามคุณสามารถเพิ่มความคิดเห็น ดูข้อมูลที่เกี่ยวข้อง ตั้งค่าเป็นรายการโปรด สมัครรับข้อมูล และอื่น ๆ ได้

จุดประสงค์บางส่วนสำหรับแดชบอร์ดคืออะไร  ต่อไปนี้เป็นเพียงตัวอย่างเล็กน้อย:

- เพื่อดูข้อมูลทั้งหมดที่จำเป็นสำหรับการตัดสินใจอย่างรวดเร็ว

- เพื่อตรวจสอบข้อมูลที่สำคัญมากที่สุดเกี่ยวกับธุรกิจของคุณ

- เพื่อให้แน่ใจว่าเพื่อนร่วมงานทั้งหมดเข้าใจตรงกัน ดู และใช้ข้อมูลเดียวกัน

- เพื่อการตรวจสอบสถานภาพของธุรกิจ หรือผลิตภัณฑ์ หรือหน่วยธุรกิจ หรือแคมเปญการตลาด และอื่น ๆ

- เพื่อสร้างมุมมองส่วนบุคคลของแดชบอร์ดที่ใหญ่กว่า เมตริกทั้งหมดที่เกี่ยวข้องกับคุณ

**หนึ่ง** แดชบอร์ด...

- สามารถแสดงภาพจากหลายชุดข้อมูลที่แตกต่างกันได้

- สามารถแสดงภาพจากหลายรายงานที่แตกต่างกันได้

- สามารถแสดงภาพที่ปักหมุดจากเครื่องมืออื่น ๆ ได้ (ตัวอย่างเช่น Excel)

  ![กราฟิกความสัมพันธ์สำหรับแดชบอร์ด](media/end-user-basic-concepts/drawing1.png)

_______________________________________________________

## <a name="apps"></a>แอป

คอลเลกชันเหล่านี้ของแดชบอร์ดและรายงานจัดระเบียบเนื้อหาที่เกี่ยวข้องเข้าด้วยกันเป็นแพคเกจเดียว *ผู้ออกแบบ* Power BI สร้างในพื้นที่ทำงานและแชร์แอปให้กับบุคคล กลุ่ม บริษัททั้งองค์กร หรือประชาชน ในฐานะ *ผู้ใช้ทางธุรกิจ* คุณสามารถมั่นใจได้ว่าคุณและเพื่อนร่วมงานของคุณกำลังทำงานกับข้อมูลเดียวกัน เวอร์ชันของความจริงที่เชื่อถือได้เพียงเวอร์ชันเดียว

ในบางครั้งพื้นที่ทำงานของแอปจะถูกแชร์และสามารถทำให้มีผู้ใช้จำนวนมากและทำงานร่วมกันและอัปเดตได้ทั้งพื้นที่ทำงานและแอป ขอบเขตของสิ่งที่คุณสามารถทำได้ด้วยแอปจะถูกกำหนดโดยสิทธิ์และการเข้าถึงที่คุณได้รับ

![สกรีนช็อตของหน้าจอสิทธิ์ของแอป](media/end-user-basic-concepts/power-bi-app-permissions.png)

> [!NOTE]
> การใช้งานแอปจะต้องมีสิทธิ์ใช้งาน Power BI Pro หรือสำหรับพื้นที่ทำงานแอปที่จะจัดเก็บไว้ในความจุระดับพรีเมียม [เรียนรู้เกี่ยวกับสิทธิ์การใช้งาน](end-user-license.md)



สามารถหาแอปจากใน[บริการของ Power BI](https://powerbi.com) และจากอุปกรณ์มือถือของคุณและติดตั้งได้ง่ายๆ หลังจากที่คุณติดตั้งแอป คุณไม่จำเป็นต้องจำชื่อของแดชบอร์ดและรายงานต่าง ๆ มากมาย ทุกอย่างรวมกันอยู่ในแอปเดียว ในเบราว์เซอร์ของคุณ หรือ บนอุปกรณ์เคลื่อนที่ของคุณ

แอปนี้มีแดชบอร์ดสองรายการและรายงานสองชุดซึ่งประกอบกันเป็นแอปเดียว หากคุณต้องการเลือกลูกศรทางด้านขวาของชื่อรายงานคุณจะเห็นรายการของเพจที่สร้างรายงานนั้น

![สกรีนช็อตของเนื้อหาที่เกี่ยวข้องสำหรับแอปที่เลือก](media/end-user-basic-concepts/power-bi-app-display.png)

เมื่อใดก็ตามที่มีการอัปเดตแอป คุณจะเห็นการเปลี่ยนแปลงโดยอัตโนมัติ ผู้ออกแบบยังสามารถควบคุมกำหนดการสำหรับจำนวนครั้งที่ Power BI รีเฟรชข้อมูล คุณไม่ต้องกังวลเกี่ยวกับการอัปเดต

คุณสามารถรับแอปในสองสามวิธีที่แตกต่างกัน

- ตัวออกแบบแอปสามารถติดตั้งแอปโดยอัตโนมัติในบัญชี Power BI ของคุณ

- ผู้ออกแบบแอปสามารถส่งลิงก์โดยตรงไปยังแอปฯได้ให้กับคุณได้

- คุณสามารถค้นหาจากภายในบริการของ Power BI สำหรับแอปที่พร้อมใช้งานสำหรับคุณจากองค์กรของคุณหรือจากชุมชน คุณสามารถเข้าชมใน [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps?product=power-bi) ที่ซึ่งคุณจะเห็นแอปทั้งหมดที่คุณสามารถใช้งานได้

ใน Power BI บนอุปกรณ์เคลื่อนที่ของคุณ คุณสามารถเติดตั้งแอปได้ จากลิงก์โดยตรงเท่านั้น และไม่สามารถตัดตั้งจาก AppSource ถ้าผู้ออกแบบแอปติดตั้งแอปโดยอัตโนมัติ คุณจะเห็นได้ในรายการของแอป

เมื่อติดตั้งแอปแล้ว เพียงเลือกแอปจากรายการแอปของคุณ และเลือกหน้าแดชบอร์ดหรือรายงานที่จะเปิดและสำรวจก่อน

![สกรีนช็อตของแอปที่เลือกในบานหน้าต่างด้านซ้ายของ Power BI](media/end-user-basic-concepts/power-bi-apps-card.png)

ฉันหวังว่าบทความนี้จะทำให้คุณเข้าใจเกี่ยวกับบล็อกการสร้างที่ประกอบกันเป็นบริการ Power BI สำหรับผู้ใช้ทางธุรกิจ

## <a name="next-steps"></a>ขั้นตอนถัดไป

- ตรวจทานและบุ๊กมาร์ก[อภิธานศัพท์](end-user-glossary.md)

- ชม[การแนะนำบริการของ Power BI](end-user-experience.md)

- อ่าน [ภาพรวมของ Power BI ที่เขียนขึ้นโดยเฉพาะสำหรับผู้ใช้ทางธุรกิจ](end-user-consumer.md)

- ดูวิดีโอที่จะตรวจทานแนวคิดพื้นฐานและให้คำแนะนำของบริการ Power BI

    <iframe width="560" height="315" src="https://www.youtube.com/embed/B2vd4MQrz4M" frameborder="0" allowfullscreen></iframe>
