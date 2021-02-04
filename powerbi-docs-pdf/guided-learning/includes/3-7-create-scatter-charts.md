---
ms.openlocfilehash: cab4d5f47c7e0518bae3c11b3f298802cb67f6d7
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2019
ms.locfileid: "61397940"
---
<span data-ttu-id="78116-101">ถ้าคุณต้องการเปรียบเทียบสองหน่วยวัดที่แตกต่างกัน เช่น ยอดขายเป็นหน่วยต่อรายได้ การจัดรูปแบบการแสดงข้อมูลทั่วไปที่จะใช้ได้คือ แผนภูมิกระจาย</span><span class="sxs-lookup"><span data-stu-id="78116-101">If you want to compare two different measures, such as unit sales verses revenue, a common visualization to use is a scatter chart.</span></span>

![](media/3-7-create-scatter-charts/3-7_1.png)

<span data-ttu-id="78116-102">เมื่อต้องการสร้างแผนภูมิว่างเปล่า ให้เลือก **แผนภูมิกระจาย** จากบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="78116-102">To create a blank chart, select **Scatter chart** from the **Visualizations** pane.</span></span> <span data-ttu-id="78116-103">ลากและปล่อยสองเขตข้อมูลที่คุณต้องการเปรียบเทียบจากบานหน้าต่าง **เขตข้อมูล** ไปยังบักเก็ตตัวเลือก *แกน X* และ *แกน Y*</span><span class="sxs-lookup"><span data-stu-id="78116-103">Drag and drop the two fields you want to compare from the **Fields** pane to the *X Axis* and *Y Axis* options buckets.</span></span> <span data-ttu-id="78116-104">ในตอนนี้แผนภูมิกระจายของคุณอาจมีฟองเล็กๆ อยู่ตรงกลางของการแสดงผลด้วยภาพ - คุณต้องเพิ่มหน่วยวัดไปยังบักเก็ต *รายละเอียด* เพื่อระบุวิธีที่คุณต้องการแยกส่วนข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="78116-104">At this point, your scatter chart probably just has a small bubble in the center of the visual - you need to add a measure to the *Details* bucket to indicate how you would like to segment your data.</span></span> <span data-ttu-id="78116-105">ตัวอย่างเช่น ถ้าเปรียบเทียบยอดขายของรายการและรายได้ คุณอาจต้องการแบ่งข้อมูลตามประเภท หรือตามผู้ผลิต หรือตามเดือนที่ขาย</span><span class="sxs-lookup"><span data-stu-id="78116-105">For example, if are comparing item sales and revenue, perhaps you want to split the data by category, or manufacturer, or month of sale.</span></span>

<span data-ttu-id="78116-106">การเพิ่มเขตข้อมูลเพิ่มเติมไปยังบักเก็ต *คำอธิบายแผนภูมิ* จะเป็นการให้รหัสสีแก่ฟองของคุณตามค่าของเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="78116-106">Adding an additional field to the *Legend* bucket color-codes your bubbles according to the field's value.</span></span> <span data-ttu-id="78116-107">นอกจากนี้คุณยังสามารถเพิ่มเขตข้อมูลไปยังบักเก็ต *ขนาด* เพื่อปรับขนาดฟองตามค่านั้น</span><span class="sxs-lookup"><span data-stu-id="78116-107">You can also add a field to the *Size* bucket to alter the bubble size according to that value.</span></span>

![](media/3-7-create-scatter-charts/3-7_2.png)

<span data-ttu-id="78116-108">แผนภูมิกระจายมีตัวเลือกการจัดรูปแบบการแสดงผลด้วยภาพมากมายเช่นกัน อย่างเช่นการเปิดเค้าร่างสำหรับแต่ละฟองสี และการสลับป้ายกำกับแต่ละป้าย</span><span class="sxs-lookup"><span data-stu-id="78116-108">Scatter charts have many visual formatting options as well, such as turning on an outline for each colored bubble and toggling individual labels.</span></span> <span data-ttu-id="78116-109">คุณสามารถเปลี่ยนสีของข้อมูลสำหรับชนิดแผนภูมิอื่นได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="78116-109">You can change the data colors for other chart types, as well.</span></span>

![](media/3-7-create-scatter-charts/3-7_3.png)

<span data-ttu-id="78116-110">คุณสามารถสร้างภาพเคลื่อนไหวของการเปลี่ยนแปลงแผนภูมิฟองของคุณเมื่อเวลาผ่านไปได้ โดยการเพิ่มเขตข้อมูลตามเวลาไปยังบักเก็ต *แกนเคลื่อนไหว*</span><span class="sxs-lookup"><span data-stu-id="78116-110">You can create an animation of your bubble chart's changes over time by adding a time-based field to the *Play Axis* bucket.</span></span> <span data-ttu-id="78116-111">คลิกที่ฟองระหว่างการเคลื่อนไหว เพื่อดูร่องรอยของเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="78116-111">Click on a bubble during an animation to see a trace of its path.</span></span>

![](media/3-7-create-scatter-charts/3-7_4.png)

>[!NOTE]
><span data-ttu-id="78116-112">อย่าลืมว่า ถ้าคุณเห็นฟองเพียงฟองเดียวในแผนภูมิกระจาย นั่นเป็นเพราะ Power BI กำลังรวบรวมข้อมูลของคุณ ซึ่งเป็นลักษณะการทำงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="78116-112">Remember, if you only see one bubble in your scatter chart, it's because Power BI is aggregating your data, which is the default behavior.</span></span> <span data-ttu-id="78116-113">เพิ่มประเภทไปยังบักเก็ต *รายละเอียด* ในบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล** เพื่อเพิ่มจำนวนฟอง</span><span class="sxs-lookup"><span data-stu-id="78116-113">Add a category to the *Details* bucket, in the **Visualizations** pane, to get more bubbles.</span></span>
> 
> 

