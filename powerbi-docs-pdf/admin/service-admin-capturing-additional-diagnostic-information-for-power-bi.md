---
title: จับข้อมูลการวินิจฉัยสำหรับการสนับสนุน
description: คำแนะนำสำหรับการรวบรวมข้อมูลการวินิจฉัยจากบริการของ Power BI ด้วยตนเอง ส่งข้อมูลนี้ไปยังการสนับสนุนเพื่อช่วยแก้ไขปัญหา
author: kfollis
ms.author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 01/21/2021
ms.custom: seodec18
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 59e434d571c5b8d10c944bc385fb4e18ed89963c
ms.sourcegitcommit: 84f0e7f31e62cae3bea2dcf2d62c2f023cc2d404
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 01/26/2021
ms.locfileid: "98781203"
---
# <a name="capture-diagnostic-information-from-the-power-bi-service"></a>จับข้อมูลการวินิจฉัยจากบริการของ Power BI

ก่อนที่คุณจะติดต่อฝ่ายสนับสนุนของ Microsoft เพื่อขอความช่วยเหลือเกี่ยวกับปัญหาที่คุณพบกับบริการของ Power BI คุณสามารถรวบรวมไฟล์ที่จะช่วยให้เราแก้ไขปัญหาของคุณได้ เราขอแนะนำให้คุณรับการติดตามเบราว์เซอร์จากเซสชันเบราว์เซอร์ของคุณ การติดตามเบราว์เซอร์คือไฟล์การวินิจฉัยที่สามารถระบุรายละเอียดที่สำคัญเกี่ยวกับสิ่งที่เกิดขึ้นในบริการของ Power BI เมื่อเกิดปัญหาขึ้นได้

ผู้ดูแลระบบ power BI สามารถใช้ประสบการณ์การ **ใช้งานความช่วยเหลือ + การสนับสนุน** ในศูนย์การ [จัดการ Power Platform](https://admin.powerplatform.microsoft.com/) เพื่อรับโซลูชันการช่วยเหลือตนเองและติดต่อฝ่ายสนับสนุน ไฟล์การวินิจฉัยที่คุณรวบรวมโดยใช้ขั้นตอนด้านล่างสามารถแนบไปกับคำขอการสนับสนุนของคุณเพื่อช่วยในการแก้ไขปัญหา สำหรับตัวเลือกการสนับสนุนเพิ่มเติมดู[ตัวเลือกการสนับสนุน POWER BI](service-support-options.md)

เมื่อต้องการรวบรวมการติดตามเบราว์เซอร์และข้อมูลเซสชันอื่นๆให้ทำตามขั้นตอนด้านล่างสำหรับเบราว์เซอร์ที่คุณใช้

## <a name="collect-a-browser-trace"></a>รวบรวมการติดตามเบราว์เซอร์

> [!IMPORTANT]
>ลงชื่อเข้าใช้ [บริการของ Power BI](https://app.powerbi.com) *ก่อน* ที่คุณจะเริ่มรวบรวมข้อมูลการติดตามเบราว์เซอร์ไม่ว่าคุณจะใช้เบราว์เซอร์ใด ขั้นตอนนี้จำเป็นต้องตรวจสอบให้แน่ใจว่าข้อมูลการติดตามไม่รวมข้อมูลที่สำคัญที่เกี่ยวข้องกับการลงชื่อเข้าใช้ของคุณ

#### <a name="google-chrome-or-microsoft-edge"></a>[Google Chrome หรือ Microsoft Edge](#tab/google-chrome-or-microsoft-edge)

Google Chrome และ Microsoft Edge (โครเมี่ยม) ทั้งสองจะขึ้นอยู่กับ[โครงการเปิดแหล่งที่มาของโครเมียม](https://www.chromium.org/Home) ขั้นตอนต่อไปนี้แสดงวิธีการใช้เครื่องมือสำหรับนักพัฒนาซึ่งคล้ายกับในสองเบราว์เซอร์ สำหรับข้อมูลเพิ่มเติมดูเครื่องมือสำหรับนักพัฒนา[Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools)และ[Microsoft Edge (โครเมียม)](/microsoft-edge/devtools-guide-chromium)

1. หลังจากลงชื่อเข้าใช้แล้วให้กด F12 บนแป้นพิมพ์ของคุณ หรือใน Microsoft Edge เลือก **การตั้งค่าและอื่นๆ (...)**  >  **เครื่องมือ**  >  เพิ่มเติม **เครื่องมือสำหรับนักพัฒนา** ใน Google Chrome เลือก **กำหนดเองและควบคุม**:::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/chromium-icon-settings.png" alt-text="เมนูการตั้งค่า Google chrome google chrome" border="false"::: > **เครื่องมือ**  >  เพิ่มเติม **เครื่องมือสำหรับนักพัฒนา**
1. เตรียมเพื่อรวบรวมการติดตามของเบราว์เซอร์โดยการตั้งค่าตัวเลือกการติดตาม นอกจากนี้คุณยังจะหยุดและล้างข้อมูลใดๆที่รวบรวมไว้ก่อนที่คุณจะเริ่มทำการทบทวนเกิดปัญหา ตามค่าเริ่มต้นเบราว์เซอร์จะเก็บข้อมูลการติดตามเฉพาะสำหรับหน้าที่กำลังโหลดอยู่ในขณะนี้ ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่าเบราว์เซอร์เพื่อเก็บข้อมูลการติดตามทั้งหมดแม้ว่า repro ของคุณจะไปยังหน้ามากกว่าหนึ่งเพจ:
    1. ในหน้าต่าง **เครื่องมือสำหรับนักพัฒนา** ให้เลือกแท็บ **เครือข่าย** จากนั้นเลือก **รักษาการบันทึก**
    
       :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/browser-trace-preserve-log.png" alt-text="เครื่องมือสำหรับนักพัฒนาด้วยแท็บเครือข่ายและรักษาบันทึกที่เลือก" :::

     2. เลือกแท็บ **คอนโซล** จากนั้นเลือก **การตั้งค่า**  >  **รักษาบันทึก** 
   
           :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/browser-trace-console-settings.png" alt-text="เครื่องมือสำหรับนักพัฒนาที่มีแท็บคอนโซลและรักษาบันทึกที่เลือกไว้" :::

        เลือก **การตั้งค่า** อีกครั้งเพื่อปิดการ **ตั้งค่าคอนโซล**

3. ถัดไปหยุดและล้างการบันทึกใดๆที่กำลังดำเนินการอยู่ เลือกแท็บ **เครือข่าย** เลือก **หยุดการบันทึกเครือข่าย** บันทึกแล้ว **ล้าง**
   
   :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/browser-trace-stop-recording.png" alt-text="เครื่องมือสำหรับนักพัฒนาที่มีแท็บเครือข่ายและหยุดและล้างตัวเลือกการบันทึกที่เลือก" :::
     
2. ในตอนนี้คุณจะทำซ้ำปัญหาที่คุณมีในบริการของ Power BI ในการเริ่มต้นใช้งาน **เครื่องมือสำหรับนักพัฒนา** เลือกแท็บ **เครือข่าย** เลือกบันทึก **เครือข่ายบันทึก**

    > [!IMPORTANT]
    >รีเฟรชหน้าเบราว์เซอร์ในบริการของ Power BI ก่อนที่คุณจะเริ่มทำการทบทวนเกิดปัญหาเพื่อให้การติดตามมีการจับภาพได้อย่างถูกต้อง

   ทำซ้ำขั้นตอนที่ส่งผลให้เกิดปัญหาที่คุณต้องการความช่วยเหลือ

     :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/browser-trace-record-network-log.png" alt-text="เครื่องมือสำหรับนักพัฒนาด้วยแท็บเครือข่ายและบันทึกเครือข่ายที่เลือก" :::

    ในขณะที่คุณทำซ้ำปัญหาคุณจะเห็นผลลัพธ์ที่คล้ายกับรูปภาพต่อไปนี้ในหน้าต่าง **เครื่องมือสำหรับนักพัฒนา**

    :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/browser-trace-output.png" alt-text="เครื่องมือสำหรับนักพัฒนาที่มีแท็บเครือข่ายแสดงผลลัพธ์ของเซสชัน" :::
    
3. หลังจากการทำซ้ำปัญหาแล้วคุณจำเป็นต้องบันทึกไฟล์บันทึกและแนบไปกับคำขอการสนับสนุนของคุณ
    1. หากต้องการส่งออกไฟล์บันทึกเครือข่ายใน **เครื่องมือสำหรับนักพัฒนา** ให้เลือกแท็บ **เครือข่าย** เลือก **หยุดการบันทึกเครือข่าย** บันทึก จากนั้นเลือก **ส่งออกฮาร์ ...** และบันทึกไฟล์

         :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/browser-trace-export-har.png" alt-text="เครื่องมือสำหรับนักพัฒนาที่มีแท็บเครือข่ายหยุดการบันทึกและส่งออกตัวเลือกฮาร์ที่เลือก" :::

    2. หากต้องการส่งออกคอนโซลผลลัพธ์ใน **เครื่องมือสำหรับนักพัฒนา** เลือกแท็บ **คอนโซล** คลิกขวาบนข้อความที่แสดงจากนั้นเลือก **บันทึกเป็น ...** และบันทึกผลลัพธ์ของคอนโซลลงในไฟล์ข้อความ
    
         :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/browser-trace-save-as.png" alt-text="เครื่องมือสำหรับนักพัฒนาที่มีแท็บคอนโซลที่เลือกและบันทึกเป็นตัวเลือกที่แสดง" :::

   แพคเกจไฟล์ฮาร์ที่บันทึก, เอาท์พุทคอนโซลและการบันทึกหน้าจอในรูปแบบที่บีบอัดเช่น .zip และแนบไฟล์กับคำขอการสนับสนุนของคุณ

#### <a name="apple-safari"></a>[Apple Safari](#tab/apple-safari)

ขั้นตอนต่อไปนี้แสดงวิธีการใช้เครื่องมือสำหรับนักพัฒนาใน Apple Safari สำหรับข้อมูลเพิ่มเติมให้ดู[ภาพรวมของเครื่องมือสำหรับนักพัฒนา Safari](https://support.apple.com/guide/safari-developer/safari-developer-tools-overview-dev073038698/11.0/mac)

1. หลังจากลงชื่อเข้าใช้แล้วให้เปิดการทำงานเครื่องมือสำหรับนักพัฒนาใน Apple Safari:
    1. จากส่วนหัวของหน้าให้เลือก  >  การ **กำหนดลักษณะ** Safari
    
       :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/safari-preferences.png" alt-text="เมนู Apple Safari ที่มีการกำหนดค่าที่เลือก" :::

    2. เลือก **ขั้นสูง** จากนั้นเลือก **แสดงเมนูพัฒนาในแถบเมนู** เพื่อเปิดใช้งานเครื่องมือสำหรับนักพัฒนา
    
       :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/safari-show-develop-menu.png" alt-text="เมนูขั้นสูงของ Safari ที่มีเมนูแสดงการพัฒนาในแถบเมนูที่เลือก" :::

2. ถัดไปคุณจะตั้งค่าตัวเลือกในตัวตรวจสอบ **เว็บ** เพื่อเปิดใช้งานเบราว์เซอร์ของคุณเพื่อเก็บข้อมูลการติดตามทั้งหมด ตามค่าเริ่มต้นเบราว์เซอร์จะเก็บข้อมูลการติดตามเฉพาะสำหรับหน้าที่กำลังโหลดอยู่ในขณะนี้ การตั้งค่าเหล่านี้ตรวจสอบให้แน่ใจว่ามีการเก็บรวบรวมข้อมูลการติดตามแม้ว่า repro ของคุณต้องการจะมีมากกว่าหนึ่งหน้า

    1. เลือก **พัฒนา** แสดงตัวตรวจสอบ  >  **เว็บ**
    
        :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/safari-web-inspector.png" alt-text="พัฒนาเมนูด้วยการแสดงเว็บตัวตรวจสอบที่เลือก" :::

    2. เลือก  >  **บันทึกการรักษา** เครือข่าย
       
         :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/safari-network-preserve-log.png" alt-text="เมนูตัวตรวจสอบเว็บที่มีเครือข่ายและรักษาบันทึกที่เลือก" :::

    1. เลือก  >  **บันทึก** การเก็บรักษาคอนโซล
   
       :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/safari-console-preserve-log.png" alt-text="เมนูตัวตรวจสอบเว็บที่มีคอนโซลและรักษาบันทึกที่เลือก" :::

3. หลังจากตั้งค่าตัวเลือกแล้วเลือก **เครือข่าย**  >  **ล้างข้อมูลรายการ** เพื่อให้แน่ใจว่าบันทึกของคุณมีเพียงรายละเอียดเกี่ยวกับปัญหา repro

    :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/safari-clear-network-items.png" alt-text="เมนูตัวตรวจสอบเว็บที่มีเครือข่ายและล้างรายการเครือข่ายที่เลือก" :::


4. ในตอนนี้คุณก็พร้อมที่จะทำให้เกิดปัญหา 
    > [!IMPORTANT]
    >รีเฟรชหน้าเบราว์เซอร์ในบริการของ Power BI ก่อนที่คุณจะเริ่มทำการทบทวนเกิดปัญหาเพื่อให้การติดตามมีการจับภาพได้อย่างถูกต้อง

    ทำตามขั้นตอนในการทบทวนเกิดปัญหาที่คุณกำลังประสบ ในขณะที่คุณทำซ้ำปัญหาคุณจะเห็นผลลัพธ์ที่คล้ายกับรูปภาพต่อไปนี้ในหน้าต่าง **เครือข่าย**

    :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/safari-session-output.png" alt-text="หน้าต่างเครือข่ายแสดงผลลัพธ์ตัวอย่าง" :::

5. หลังจากการทำซ้ำปัญหาแล้วคุณจำเป็นต้องบันทึกไฟล์บันทึกและแนบไปกับคำขอการสนับสนุนของคุณ

    1. หากต้องการส่งออกบันทึกเครือข่ายจากแท็บ **เครือข่าย** ให้เลือก **ส่งออก** และบันทึกไฟล์ในรูปแบบฮาร์

         :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/safari-export.png" alt-text="แท็บเครือข่ายที่มีการเลือกตัวเลือกการส่งออก" :::

    2. ในการส่งออกคอนโซลเอาท์พุทในบานหน้าต่างเครื่องมือการ **พัฒนา** เลือกแท็บ **คอนโซล** และขยายหน้าต่าง วางเคอร์เซอร์ของคุณที่จุดเริ่มต้นของผลลัพธ์ของคอนโซลแล้วลากและเลือกเนื้อหาทั้งหมดของผลลัพธ์ ใช้คำสั่ง-C เพื่อคัดลอกผลลัพธ์และบันทึกไปยังไฟล์ข้อความ

   แพคเกจไฟล์ฮาร์ที่บันทึก, เอาท์พุทคอนโซลและการบันทึกหน้าจอในรูปแบบที่บีบอัดเช่น .zip และแนบไฟล์กับคำขอการสนับสนุนของคุณ

#### <a name="firefox"></a>[Firefox](#tab/firefox)

ขั้นตอนต่อไปนี้แสดงวิธีการใช้เครื่องมือสำหรับนักพัฒนาใน Firefox สำหรับข้อมูลเพิ่มเติมดู[เครื่องมือสำหรับนักพัฒนา Firefox](https://developer.mozilla.org/docs/Tools)

1. หลังจากลงชื่อเข้าใช้แล้วให้กด F12 บนแป้นพิมพ์ของคุณ หรือใน Firefox เลือก **เปิดเมนู** :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/firefox-menu.png" alt-text="firefox ไอคอนเมนู" border="false"::: > **นักพัฒนาเว็บ**  >  **สลับเครื่องมือ** เครื่องมือจะปรากฏที่ด้านล่างของหน้าจอของคุณ

1. ถัดไปคุณจะตั้งค่าตัวเลือกในตัวตรวจสอบเพื่อเปิดใช้งานเบราว์เซอร์ของคุณเพื่อเก็บ **ข้อมูลการติดตาม** ทั้งหมด ตามค่าเริ่มต้นเบราว์เซอร์จะเก็บข้อมูลการติดตามเฉพาะสำหรับหน้าที่กำลังโหลดอยู่ในขณะนี้ การตั้งค่าเหล่านี้ตรวจสอบให้แน่ใจว่ามีการเก็บรวบรวมข้อมูลการติดตามแม้ว่า repro ของคุณต้องการจะมีมากกว่าหนึ่งหน้า

    1. ในหน้าต่าง **ตัวตรวจ** สอบเลือกแท็บ **เครือข่าย** จากนั้นเลือก **ยืนยันไฟล์บันทึก**
    
       :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/firefox-network-persist-logs.png" alt-text="เครื่องมือตรวจสอบที่มีแท็บเครือข่ายและยืนยันบันทึกที่เลือก" :::

     2. เลือกแท็บ **คอนโซล** จากนั้นเลือก **การตั้งค่าคอนโซล** ที่  >  **ยืนยันบันทึก** 
   
           :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/firefox-console-persist-logs.png" alt-text="เครื่องมือตรวจสอบที่มีแท็บคอนโซลและยืนยันบันทึกที่เลือก" :::

3. หลังจากตั้งค่าตัวเลือกแล้วให้ล้างการบันทึกใดๆที่กำลังดำเนินการอยู่ เลือกแท็บ **เครือข่าย** แล้ว **ล้าง**
   
   :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/browser-trace-stop-recording.png" alt-text="เครื่องมือสำหรับนักพัฒนาที่มีแท็บเครือข่ายและหยุดและล้างตัวเลือกการบันทึกที่เลือก" :::
     
2. ในตอนนี้คุณก็พร้อมที่จะทำให้เกิดปัญหา 
    > [!IMPORTANT]
    >รีเฟรชหน้าเบราว์เซอร์ในบริการของ Power BI ก่อนที่คุณจะเริ่มทำการทบทวนเกิดปัญหาเพื่อให้การติดตามมีการจับภาพได้อย่างถูกต้อง
 
    ทำตามขั้นตอนในการทบทวนเกิดปัญหาที่คุณกำลังประสบ
    
3. หลังจากการทำซ้ำปัญหาแล้วคุณจำเป็นต้องบันทึกไฟล์บันทึกและแนบไปกับคำขอการสนับสนุนของคุณ
    1. หากต้องการส่งออกบันทึกเครือข่ายให้เลือก **เครือข่าย**  >  **ฮาร์ส่งออก/นำเข้า** จากนั้น **บันทึกทั้งหมดเป็นฮาร์**

         :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/firefox-save-har.png" alt-text="แท็บเครือข่ายที่มีเมนูการส่งออก/นำเข้าฮาร์และบันทึกตัวเลือกทั้งหมดที่เลือก" :::

    2. เมื่อต้องการส่งออกผลลัพธ์ของคอนโซลให้เลือกแท็บ **คอนโซล** คลิกขวาบนข้อความที่แสดงจากนั้นเลือก **ส่งออกข้อความที่มองเห็นได้** และบันทึกผลลัพธ์ของคอนโซลลงในไฟล์ข้อความ
    
         :::image type="content" source="media/service-admin-capturing-additional-diagnostic-information-for-power-bi/firefox-export-visible-messages.png" alt-text="ตัวเลือกการแสดงผลของแท็บคอนโซลที่เลือกและส่งออกข้อความที่มองเห็น" :::

   แพคเกจไฟล์ฮาร์ที่บันทึก, เอาท์พุทคอนโซลและการบันทึกหน้าจอในรูปแบบที่บีบอัดเช่น .zip และแนบไฟล์กับคำขอการสนับสนุนของคุณ

---

หลังจากที่คุณรวบรวมไฟล์การวินิจฉัยให้แนบกับคำขอการสนับสนุนของคุณเพื่อช่วยวิศวกรฝ่ายสนับสนุนแก้ไขปัญหาของคุณ ไฟล์ฮาร์จะประกอบด้วยข้อมูลทั้งหมดเกี่ยวกับคำขอเครือข่ายระหว่างหน้าต่างเบราว์เซอร์และบริการของ Power BI รวมถึง:

* ID กิจกรรมสำหรับการร้องขอแต่ละรายการ

* ประทับเวลาที่แม่นยำสำหรับการร้องขอแต่ละรายการ

* ข้อมูลข้อผิดพลาดใดๆที่ส่งกลับไปยังไคลเอ็นต์

แฟ้มการติดตามที่ได้ ยังประกอบด้วยข้อมูลที่ใช้เพื่อแสดงภาพบนหน้าจอ

## <a name="next-steps"></a>ขั้นตอนถัดไป

* [ติดตามสถานภาพบริการ Power BI ใน Microsoft 365](service-admin-health.md)
* [เปิดใช้งานการแจ้งเตือนการหยุดชะงักของบริการ](service-interruption-notifications.md)
* [เข้าร่วมชุมชน Power BI](https://community.powerbi.com/)
