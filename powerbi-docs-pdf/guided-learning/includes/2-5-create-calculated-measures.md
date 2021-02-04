---
ms.openlocfilehash: a4d51bb3295c2b5512b98fe2ac231ed1b3467c8a
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2019
ms.locfileid: "61257007"
---
<span data-ttu-id="807c2-101">*หน่วยวัด*คือการคำนวณที่มีอยู่ในแบบจำลองข้อมูล Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="807c2-101">A *measure* is a calculation that exists in your Power BI data model.</span></span> <span data-ttu-id="807c2-102">เมื่อต้องการสร้างหน่วยวัด ในมุมมอง**รายงาน** ให้เลือก **หน่วยวัดใหม่** จากแท็บ **การวางรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="807c2-102">To create a measure, in **Report** view select **New Measure** from the **Modeling** tab.</span></span>

![](media/2-5-create-calculated-measures/2-5_1.png)

<span data-ttu-id="807c2-103">หนึ่งในสิ่งที่ยอดเยี่ยมเกี่ยวกับ DAX ที่เป็นภาษานิพจน์วิเคราะห์ข้อมูลใน Power BI คือ มีฟังก์ชันที่เป็นประโยชน์จำนวนมาก โดยเฉพาะเกี่ยวกับการคำนวณตามเวลา เช่น *เริ่มต้นปีจนถึงปัจจุบัน* หรือ *ปีปัจจุบันกับปีที่ผ่านมา*</span><span class="sxs-lookup"><span data-stu-id="807c2-103">One of the great things about DAX, the Data Analysis Expression language in Power BI, is that it has lots of useful functions, particularly around time-based calculations such as *Year to Date* or *Year Over Year*.</span></span> <span data-ttu-id="807c2-104">เมื่อใช้ DAX คุณจะสามารถกำหนดหน่วยวัดเวลา แล้วแบ่งตามจำนวนเขตข้อมูลต่างๆ ที่คุณต้องการจากแบบจำลองข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="807c2-104">With DAX you can define a measure of time once, and then slice it by as many different fields as you want from your data model.</span></span>

<span data-ttu-id="807c2-105">ใน Power BI การคำนวณที่กำหนดไว้จะเรียกว่า*หน่วยวัด*</span><span class="sxs-lookup"><span data-stu-id="807c2-105">In Power BI, a defined calculation is called a *measure*.</span></span> <span data-ttu-id="807c2-106">เมื่อต้องการสร้าง*หน่วยวัด* ให้เลือก **หน่วยวัดใหม่** จากแท็บ **หน้าแรก** การทำเช่นนี้จะเปิดแถบสูตรที่คุณสามารถใส่นิพจน์ DAX ที่กำหนดหน่วยวัดของคุณ</span><span class="sxs-lookup"><span data-stu-id="807c2-106">To create a *measure*, select **New Measure** from the **Home** tab. This opens the Formula bar where you can enter the DAX expression that defines your measure.</span></span> <span data-ttu-id="807c2-107">เมื่อคุณพิมพ์ Power BI จะแนะนำฟังก์ชัน DAX และเขตข้อมูลที่เกี่ยวข้องเมื่อคุณใส่การคำนวณของคุณ และคุณยังจะได้รับคำแนะนำเครื่องมือที่อธิบายพารามิเตอร์ไวยากรณ์และฟังก์ชันบางอย่างอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="807c2-107">As you type, Power BI suggests relevant DAX functions and data fields as you enter your calculation, and you'll also get a tooltip explaining some of the syntax and function parameters.</span></span>

![](media/2-5-create-calculated-measures/2-5_2.png)

<span data-ttu-id="807c2-108">ถ้าการคำนวณของคุณมีความยาวมาก คุณสามารถเพิ่มตัวแบ่งบรรทัดในตัวแก้ไขนิพจน์ได้โดยการพิมพ์ **ALT-Enter**</span><span class="sxs-lookup"><span data-stu-id="807c2-108">If your calculation is particularly long, you can add extra line breaks in the Expression Editor by typing **ALT-Enter**.</span></span>

![](media/2-5-create-calculated-measures/2-5_3.png)

<span data-ttu-id="807c2-109">เมื่อคุณสร้างหน่วยวัดใหม่ จะปรากฏในหนึ่งในตารางบนบานหน้าต่าง **เขตข้อมูล** ที่อยู่ทางด้านขวาของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="807c2-109">Once you've created a new measure, it will appear in one of the tables on the **Fields** pane, found on the right side of the screen.</span></span> <span data-ttu-id="807c2-110">Power BI จะแทรกหน่วยวัดใหม่ลงในตารางใดก็ตามที่คุณเลือกอยู่ และไม่ว่าหน่วยวัดจะอยู่ที่ไหนในข้อมูลของคุณ คุณสามารถย้ายได้อย่างง่ายดายโดยการเลือกหน่วยวัดและใช้เมนูดรอปดาวน์ **ตารางหลัก**</span><span class="sxs-lookup"><span data-stu-id="807c2-110">Power BI inserts the new measure into whichever table you have currently selected, and while it doesn't matter exactly where the measure is in your data, you can easily move it by selecting the measure and using the **Home Table** drop-down menu.</span></span>

![](media/2-5-create-calculated-measures/2-5_4.png)

<span data-ttu-id="807c2-111">คุณสามารถใช้หน่วยวัดด้วยวิธีที่คล้ายกับคอลัมน์ตารางอื่นๆ คือ เพียงลากแล้วปล่อยลงในพื้นที่ทำงานของรายงานหรือเขตข้อมูลการจัดรูปแบบการแสดงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="807c2-111">You can use a measure like any other table column: just drag and drop it onto the report canvas or visualization fields.</span></span> <span data-ttu-id="807c2-112">หน่วยวัดยังรวมกับตัวแบ่งส่วนข้อมูล การแบ่งส่วนข้อมูลของคุณระหว่างเดินทางได้อย่างราบรื่น ซึ่งหมายความว่าคุณสามารถกำหนดหน่วยวัดหนึ่งครั้ง และใช้ในการจัดรูปแบบการแสดงข้อมูลต่างๆ ได้หลายครั้ง</span><span class="sxs-lookup"><span data-stu-id="807c2-112">Measures also integrate seamlessly with slicers, segmenting your data on the fly, which means you can define a measure once, and use it in many different visualizations.</span></span>

<span data-ttu-id="807c2-113">ฟังก์ชัน **คำนวณ** ของ DAX คือฟังก์ชันที่มีประสิทธิภาพที่สามารถทำการคำนวณที่เป็นประโยชน์ได้ทุกรูปแบบ โดยเฉพาะอย่างยิ่ง การทำรายงานและการแสดงข้อมูลด้านการเงิน</span><span class="sxs-lookup"><span data-stu-id="807c2-113">The **Calculate** DAX function is a powerful function that enables all sorts of useful calculations, which is especially useful for financial reporting and visuals.</span></span>

