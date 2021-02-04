---
ms.openlocfilehash: 3fd97374836978a4902a878da141865c271df643
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2019
ms.locfileid: "61397949"
---
<span data-ttu-id="b9494-101">โดยทั่วไปการจัดรูปแบบการแสดงข้อมูลจะใช้เพื่อเปรียบเทียบค่าที่แตกต่างกันอย่างน้อยสองค่า</span><span class="sxs-lookup"><span data-stu-id="b9494-101">Generally, visualizations are used to compare two or more different values.</span></span> <span data-ttu-id="b9494-102">อย่างไรก็ตาม บางครั้งเมื่อสร้างรายงาน คุณอาจต้องการติดตามดัชนีชี้วัดผลการปฏิบัติงานหลัก (KPI) หรือเมตริกเพียงรายการเดียวเมื่อเวลาผ่านไป</span><span class="sxs-lookup"><span data-stu-id="b9494-102">However, sometimes when building reports you may want to track a just single Key Performance Indicator (KPI) or metric over time.</span></span> <span data-ttu-id="b9494-103">ซึ่งวิธีที่จะสามารถทำเช่นนี้ได้ใน Power BI Desktop คือติดตามด้วย**มาตรวัด**หรือการแสดงผลด้วยภาพแบบบัตร**เลขตัวเดียว**</span><span class="sxs-lookup"><span data-stu-id="b9494-103">The way to do this in Power BI Desktop is with a **Gauge** or **single number** card visual.</span></span> <span data-ttu-id="b9494-104">เมื่อต้องการสร้างแผนภูมิว่างเปล่าประเภทใดก็ตาม ให้เลือกไอคอนจากบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="b9494-104">To create a blank chart of either type, select its icon from the **Visualizations** pane.</span></span>

![](media/3-9-create-gauges-cards/3-9_1.png)

<span data-ttu-id="b9494-105">มาตรวัดจะมีประโยชน์อย่างยิ่งเมื่อคุณกำลังสร้างหน้าแดชบอร์ดและต้องการแสดงความคืบหน้าไปสู่เป้าหมายที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="b9494-105">Gauges are particularly useful when you are building dashboards and want to show progress towards a particular target.</span></span> <span data-ttu-id="b9494-106">เมื่อต้องการสร้างมาตรวัด ให้เลืกไอคอนมาตรวัดจากบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล** แล้วลากเขตข้อมูลที่คุณต้องการติดตามไปในบักเก็ต *ค่า*</span><span class="sxs-lookup"><span data-stu-id="b9494-106">To create a gauge, select its icon from the **Visualizations** pane, and drag the field you want to track into the *Value* bucket.</span></span>

![](media/3-9-create-gauges-cards/3-9_1a.png)

<span data-ttu-id="b9494-107">มาตรวัดจะปรากฏตามค่าเริ่มต้นที่ 50% หรือเป็นสองเท่าของ*ค่า* และมีสองวิธีในการปรับการตั้งค่านี้</span><span class="sxs-lookup"><span data-stu-id="b9494-107">Gauges appear by default at 50%, or double the *Value*, and there are two ways to adjust this setting.</span></span> <span data-ttu-id="b9494-108">เมื่อต้องการตั้งค่าแบบไดนามิก ให้ลากเขตข้อมูลไปยังบักเก็ตค่า*ต่ำสุด* ค่า*สูงสุด* และค่า*เป้าหมาย*</span><span class="sxs-lookup"><span data-stu-id="b9494-108">To dynamically set the values, drag fields to the *Minimum*, *Maximum*, and *Target* Value buckets.</span></span> <span data-ttu-id="b9494-109">อีกทางเลือกหนึ่งคือใช้ตัวเลือกการจัดรูปแบบการแสดงผลด้วยภาพเพื่อกำหนดช่วงมาตรวัดของคุณด้วยตัวเอง</span><span class="sxs-lookup"><span data-stu-id="b9494-109">Alternatively, use the visual formatting options to manually customize the range of your gauge.</span></span>

![](media/3-9-create-gauges-cards/3-9_2.png)

<span data-ttu-id="b9494-110">การจัดรูปแบบการแสดงข้อมูลแบบบัตรจะแสดงเพียงการแสดงตัวเลขของเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9494-110">Card visualizations simply show a numeric representation of a field.</span></span> <span data-ttu-id="b9494-111">ตามค่าเริ่มต้น การแสดงผลด้วยภาพแบบบัตรจะใช้หน่วยแสดงผลเพื่อให้ตัวเลขสั้นลง เช่น แสดง "$5bn" แทนที่จะเป็น "$5,000,000,000"</span><span class="sxs-lookup"><span data-stu-id="b9494-111">By default card visuals use display units to keep the number short, for example displaying "$5bn" instead of "$5,000,000,000".</span></span> <span data-ttu-id="b9494-112">ใช้ตัวเลือกการจัดรูปแบบการแสดงผลด้วยภาพเพื่อเปลี่ยนหน่วยที่ใช้อยู่หรือปิดใช้งานหน่วยอย่างสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b9494-112">Use the visual formatting options to change the unit being used, or disable it completely.</span></span>

![](media/3-9-create-gauges-cards/3-9_3.png)

<span data-ttu-id="b9494-113">การใช้บัตรที่น่าสนใจอย่างหนึ่งคือให้บัตรแสดงหน่วยวัดแบบกำหนดเองที่คุณได้เชื่อมเข้ากับข้อความ</span><span class="sxs-lookup"><span data-stu-id="b9494-113">One interesting application of cards is to have them display a custom measure that you've concatenated with text.</span></span> <span data-ttu-id="b9494-114">เมื่อต้องการใช้ตัวอย่างก่อนหน้านี้ ด้วยหน่วยวัดแบบกำหนดเอง บัตรของคุณอาจมีฟังก์ชัน DAX ขั้นสูงและแสดงข้อมูลเช่น "รายได้รวมในปีนี้: $5bn" หรือ "ความคืบหน้าในการขายปีนี้" จากนั้นเพิ่มหมายเลขที่แสดงความคืบหน้า</span><span class="sxs-lookup"><span data-stu-id="b9494-114">To use the earlier example, with a custom measure your card could include advanced DAX functions and display something like, "Total revenue this year: $5bn" or "Progress on unit sales this year:" and then add the number that represents the progress.</span></span>

![](media/3-9-create-gauges-cards/3-9_4.png)

