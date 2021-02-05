---
title: 'บทช่วยสอน: ใช้แบบจำลอง Azure Machine Learning ใน Power BI'
titleSuffix: Azure Machine Learning
description: เรียนรู้วิธีใช้แบบจำลอง Azure Machine Learning ใน Power BI
services: machine-learning
ms.service: machine-learning
ms.subservice: core
ms.topic: tutorial
ms.author: samkemp
author: samuel100
ms.reviewer: sdgilley, maggies
ms.date: 12/10/2020
ms.openlocfilehash: 6c68fff575e4da0c9126904df2de5292747c209c
ms.sourcegitcommit: 46cf62d9bb33ac7b7eae7910fbba6756f626c65f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/15/2020
ms.locfileid: "97491793"
---
# <a name="tutorial-consume-azure-machine-learning-models-in-power-bi"></a>บทช่วยสอน: ใช้แบบจำลอง Azure Machine Learning ใน Power BI

บทช่วยสอนนี้จะแนะนำการสร้างรายงาน Power BI ตามแบบจำลองการเรียนรู้ของเครื่อง ในตอนท้ายของบทช่วยสอนนี้ คุณจะสามารถ:

> [!div class="checklist"]
> * ให้คะแนนแบบจำลองการเรียนรู้ของเครื่อง (ที่ปรับใช้โดยใช้ Azure Machine Learning) ใน Power BI
> * เชื่อมต่อกับแบบจำลอง Azure Machine Learning ในตัวแก้ไข Power Query
> * สร้างรายงานด้วยการจัดรูปแบบการแสดงข้อมูลตามแบบจำลอง
> * เผยแพร่รายงานดังกล่าวไปยังบริการ Power BI
> * ตั้งค่าการรีเฟรชที่ตั้งกำหนดการแล้วสำหรับรายงาน

## <a name="prerequisites"></a>สิ่งที่จำเป็นต้องมี

ก่อนที่จะเริ่มบทช่วยสอน คุณจำเป็นต้อง:

- ฝึกอบรมและปรับใช้แบบจำลองการเรียนรู้ของเครื่องใน Azure Machine Learning ใช้หนึ่งในสามบทช่วยสอน Azure Machine Learning: 

    - [ตัวเลือก A: รหัส](/azure/machine-learning/tutorial-power-bi-custom-model)
    - [ตัวเลือก B: ตัวออกแบบ](/azure/machine-learning/tutorial-power-bi-designer-model)
    - [ตัวเลือก C: ML อัตโนมัติ](/azure/machine-learning/tutorial-power-bi-automated-model)

- ลงทะเบียนสำหรับ[รุ่นทดลองใช้ Power BI ฟรี](https://app.powerbi.com/signupredirect?pbi_source=web)
- [ติดตั้ง Power BI Desktop](https://powerbi.microsoft.com/desktop/) ภายในคอมพิวเตอร์

## <a name="create-the-data-model"></a>สร้างแบบจำลองข้อมูล

เปิด Power BI Desktop แล้วเลือก **รับข้อมูล** ในกล่องโต้ตอบ **รับข้อมูล** ให้ค้นหา **เว็บ** เลือกแหล่งข้อมูล **เว็บ** > **เชื่อมต่อ**

:::image type="content" source="media/service-aml-integrate/pbi-get-data.png" alt-text="สกรีนช็อตที่แสดงข้อมูลเว็บ":::

ในกล่องโต้ตอบ **จากเว็บ** ให้คัดลอกและวาง URL ต่อไปนี้ลงในกล่อง:

```txt 
https://www4.stat.ncsu.edu/~boos/var.select/diabetes.tab.txt
```

:::image type="content" source="media/service-aml-integrate/pbi-data.png" alt-text="สกรีนช็อตที่แสดง URL เว็บ":::

เลือก **ตกลง**

เลือก **แปลงข้อมูล** เพื่อเปิดหน้าต่าง **ตัวแก้ไข Power Query**

ใน Ribbon หน้าแรกของตัวแก้ไข Power Query ให้เลือกปุ่ม **Azure Machine Learning**

:::image type="content" source="media/service-aml-integrate/aml-button.png" alt-text="สกรีนช็อตที่แสดงตัวแก้ไข Power Query":::

หลังจากลงชื่อเข้าใช้บัญชี Azure ของคุณโดยใช้การลงชื่อเข้าระบบครั้งเดียว คุณจะเห็นรายการของบริการที่พร้อมใช้งาน เลือก **บริการ sklearn ของฉัน** ที่คุณสร้างขึ้นจากฝึกอบรมและปรับใช้บทช่วยสอนแบบจำลองการเรียนรู้ของเครื่อง 

Power Query เติมข้อมูลคอลัมน์ให้คุณโดยอัตโนมัติ คุณจำไว้ว่าใน Schema ของเราสำหรับบริการ เรามีมัณฑนา Python ที่ระบุการป้อนข้อมูล เลือก **ตกลง**

:::image type="content" source="media/service-aml-integrate/aml-pbi-run.png" alt-text="สกรีนช็อตที่แสดงแบบจำลอง Azure Machine Learning":::

การเลือก **ตกลง** จะเรียกใช้บริการ Azure Machine Learning ซึ่งจะทริกเกอร์คำเตือนเกี่ยวกับความเป็นส่วนตัวของข้อมูลสำหรับทั้งข้อมูลและจุดสิ้นสุด

:::image type="content" source="media/service-aml-integrate/data_privacy_warning.png" alt-text="สกรีนช็อตที่แสดงคำเตือนความเป็นส่วนตัว":::

เลือก **ดำเนินต่อ** ในหน้าจอถัดไป เลือก **ละเว้นระดับความเป็นส่วนตัวในการตรวจสอบไฟล์นี้** > **บันทึก**

เมื่อให้คะแนนข้อมูลแล้ว Power Query จะสร้างคอลัมน์เพิ่มเติมที่ชื่อว่า **AzureML.my-diabetes-model**

:::image type="content" source="media/service-aml-integrate/scored-data.png" alt-text="สกรีนช็อตที่แสดงคอลัมน์ที่ให้คะแนนแล้วที่เพิ่มเข้ามา":::

ข้อมูลที่บริการส่งกลับคือ **รายการ** 

> [!NOTE]
> หากคุณปรับใช้แบบจำลองตัวออกแบบ คุณจะเห็น **ระเบียน**

หากต้องการรับการคาดคะเน ใน Ribbon **แปลง** ให้เลือกปุ่ม **ขยายคอลัมน์** > **ขยายไปยังแถวใหม่**

หลังจากที่ขยายแล้ว คุณจะเห็นการคาดคะเนในคอลัมน์ AzureML.my-diabetes-model

:::image type="content" source="media/service-aml-integrate/after-expand.png" alt-text="สกรีนช็อตที่แสดงการขยาย":::

ทำตามขั้นตอนถัดไปเพื่อล้างแบบจำลองข้อมูลของคุณให้เสร็จสมบูรณ์

1. เปลี่ยนชื่อคอลัมน์ **AzureML.my-diabetes-model** เป็น **คาดคะเนแล้ว**
1. เปลี่ยนชื่อคอลัมน์ **Y** เป็น **จริง**
1. เปลี่ยนชนิดของคอลัมน์ **จริง**: เลือกคอลัมน์ จากนั้นใน Ribbon **แปลง** ให้เลือก **ชนิดข้อมูล** > **เลขทศนิยม**
1. เปลี่ยนชนิดของคอลัมน์ **คาดคะเนแล้ว**: เลือกคอลัมน์ดังกล่าว จากนั้นใน Ribbon **แปลง** ให้เลือก **ชนิดข้อมูล** > **เลขทศนิยม**
1. ใน Ribbon **หน้าแรก** ให้เลือก **ปิดและนำไปใช้**

## <a name="create-a-report-with-visualizations"></a>สร้างรายงานที่มีการจัดรูปแบบการแสดงข้อมูล

ตอนนี้คุณสามารถสร้างการจัดรูปแบบการแสดงข้อมูลบางส่วนได้เพื่อแสดงข้อมูลของคุณ

1. ในบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล** ให้เลือก **แผนภูมิเส้น** 
1. เมื่อเลือกการแสดงผลด้วยภาพแผนภูมิเส้นแล้ว:
1. ลากเขตข้อมูล **อายุ** ไปยัง **แกน**
1. ลากเขตข้อมูล **จริง** ไปยัง **ค่า**
1. ลากเขตข้อมูล **คาดคะเนแล้ว** ไปยัง **ค่า**

ปรับขนาดแผนภูมิเส้นเพื่อเติมหน้า ในตอนนี้ รายงานของคุณมีหนึ่งแผนภูมิเส้นที่ประกอบด้วยเส้นสองเส้น โดยที่เส้นหนึ่งคือค่าที่คาดคะเนและอีกเส้นหนึ่งคือค่าจริง ซึ่งจะแจกจ่ายตามอายุ

:::image type="content" source="media/service-aml-integrate/report-viz.png" alt-text="สกรีนช็อตที่แสดงการจัดรูปแบบการแสดงข้อมูลรายงาน":::

## <a name="publish-the-report"></a>เผยแพร่รายงาน

คุณสามารถเพิ่มการจัดรูปแบบการแสดงข้อมูลเพิ่มเติมได้ตามที่ต้องการ เพื่อความกระชับ ในบทช่วยสอนนี้ เราจะเผยแพร่รายงาน

1. บันทึกรายงาน
1. เลือก **ไฟล์** > **เผยแพร่** > **เผยแพร่ไปยัง Power BI**
1. ลงชื่อเข้าใช้บริการ Power BI
1. เลือก **พื้นที่ทำงานของฉัน**
1. เมื่อเผยแพร่รายงานสำเร็จแล้ว ให้เลือกลิงก์ **เปิด <MY_PBIX_FILE.pbix> ใน Power BI** รายงานจะเปิดรายงานใน Power BI ในเบราว์เซอร์ของคุณ

     :::image type="content" source="media/service-aml-integrate/publish-success.png" alt-text="สกรีนช็อตที่แสดงการเผยแพร่ที่สำเร็จ":::

## <a name="enable-datasets-to-refresh"></a>เปิดใช้งานชุดข้อมูลเพื่อรีเฟรช

ในสถานการณ์ที่มีการรรีเฟรชแหล่งข้อมูลด้วยข้อมูลใหม่เพื่อให้คะแนน คุณจำเป็นต้องอัปเดตข้อมูลประจำตัวของคุณเพื่อให้สามารถให้คะแนนข้อมูลได้ 

ในพื้นที่ทำงานของฉันในบริการ Power BI ในแถบส่วนหัวสีดำ ให้เลือก **ตัวเลือกเพิ่มเติม (...)**  > **การตั้งค่า** > **การตั้งค่า**

:::image type="content" source="media/service-aml-integrate/settings-pbi.png" alt-text="สกรีนช็อตที่แสดงการตั้งค่า":::

เลือก **ชุดข้อมูล** ขยาย **ข้อมูลประจำตัวแหล่งข้อมูล** จากนั้นเลือก **แก้ไขข้อมูลประจำตัว**

:::image type="content" source="media/service-aml-integrate/data-refresh.png" alt-text="สกรีนช็อตที่แสดงการรีเฟรชข้อมูลประจำตัว":::

ทำตามคำแนะนำสำหรับทั้ง **azureMLFunctions** และ **เว็บ** ตรวจสอบให้แน่ใจว่าคุณเลือกระดับความเป็นส่วนตัวแล้ว ขณะนี้คุณสามารถตั้งค่า **การรีเฟรชที่ตั้งกำหนดการแล้ว** ของข้อมูล เลือก **ความถี่การรีเฟรช** และ **โซนเวลา** นอกจากนี้ คุณสามารถเลือกอีเมลแอดเดรสที่ Power BI สามารถส่งการแจ้งเตือนความล้มเหลวการรีเฟรช

:::image type="content" source="media/service-aml-integrate/schedule-refresh.png" alt-text="สกรีนช็อตที่แสดงชุดข้อมูลและการรีเฟรชการให้คะแนน":::

เลือก **นำไปใช้**

>[!NOTE]
> เมื่อมีการรีเฟรชข้อมูล จะมีการส่งข้อมูลไปยังจุดสิ้นสุด Azure Machine Learning ของคุณสำหรับการให้คะแนน

## <a name="clean-up-resources"></a>ล้างแหล่งข้อมูล

>[!IMPORTANT]
>คุณสามารถใช้ทรัพยากรที่คุณสร้างขึ้นเป็นข้อกำหนดเบื้องต้นสำหรับบทช่วยสอน Azure Machine Learning และบทความเกี่ยวกับวิธีการอื่นๆ

หากคุณไม่ได้วางแผนที่จะใช้ทรัพยากรที่คุณสร้างขึ้น ให้ลบทรัพยากรออกเพื่อที่คุณจะไม่ต้องเสียค่าบริการใดๆ

1. ในพอร์ทัล Azure ให้เลือก **กลุ่มทรัพยากร** ทางด้านซ้ายสุด
 
1. จากรายการ ให้เลือกกลุ่มทรัพยากรที่คุณสร้างขึ้น

1. เลือก **ลบกลุ่มทรัพยากร**

   ![สกรีนช็อตของการเลือกเพื่อลบกลุ่มทรัพยากรในพอร์ทัล Azure](./media/service-aml-integrate/delete-resources.png)

1. ใส่ชื่อกลุ่มทรัพยากร จากนั้นเลือก **ลบ**
1. ในพื้นที่ทำงานของฉันในบริการ Power BI ให้ลบรายงานและชุดข้อมูลที่เกี่ยวข้อง คุณไม่จำเป็นต้องลบ Power BI Desktop หรือรายงานในคอมพิวเตอร์ของคุณ Power BI Desktop ฟรี

## <a name="next-steps"></a>ขั้นตอนถัดไป

ในชุดบทช่วยสอนนี้ คุณจะได้เรียนรู้วิธีตั้งค่ากำหนดการใน Power BI เพื่อให้สามารถให้คะแนนข้อมูลใหม่ได้จากจุดสิ้นสุดการให้คะแนนของคุณใน Azure Machine Learning
