---
ms.openlocfilehash: 29a274bb847c6c0395d3cdba868024ded326290e
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2019
ms.locfileid: "61397943"
---
<span data-ttu-id="7c218-101">เมื่อคุณมีการจัดรูปแบบการแสดงข้อมูลหลายรายการอยู่บนหน้ารายงานเดียวกัน การเลือกส่วนเฉพาะโดยการคลิกหรือการใช้ตัวแบ่งส่วนข้อมูลจะส่งผลต่อการแสดงข้อมูลทั้งหมดบนหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="7c218-101">When you have multiple visualizations on the same report page, selecting a particular segment by clicking or using a slicer will affect all the visuals on that page.</span></span> <span data-ttu-id="7c218-102">ในบางกรณี คุณอาจต้องการแบ่งส่วนการแสดงผลด้วยภาพเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="7c218-102">In some cases, though, you may want to slice only specific visuals.</span></span> <span data-ttu-id="7c218-103">โดยเฉพาะอย่างยิ่งเมื่อใช้องค์ประกอบ เช่น แผนภูมิการลงจุดกระจาย ที่การจำกัดข้อมูลให้อยู่ในเฉพาะส่วนจะนำความหมายที่สำคัญออก</span><span class="sxs-lookup"><span data-stu-id="7c218-103">This is particularly true when using elements such as scatter plots, where limiting the data to a specific segment will remove crucial meaning.</span></span> <span data-ttu-id="7c218-104">โชคดีที่ Power BI Desktop ช่วยให้คุณสามารถควบคุมการโต้ตอบระหว่างการแสดงข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="7c218-104">Fortunately, Power BI Desktop lets you control how interactions flow between visuals.</span></span>

<span data-ttu-id="7c218-105">เมื่อต้องการเปลี่ยนการโต้ตอบระหว่างการจัดรูปแบบการแสดงข้อมูลของคุณ ให้เลือก **แก้ไข** จากส่วนการแสดงข้อมูลของ Ribbon **หน้าแรก** เพื่อเปิด **โหมดแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="7c218-105">To change the interaction between your visualizations, select **Edit** from the Visuals section of the **Home** ribbon to toggle **Edit Mode** on.</span></span>

>[!NOTE]
><span data-ttu-id="7c218-106">ไอคอน **แก้ไขการโต้ตอบ** ใน Power BI Desktop มีการเปลี่ยนแปลงตั้งแต่ตอนบันทึกวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="7c218-106">The **Edit Interactions** icon in Power BI Desktop has changed since the video was recorded.</span></span>
> 
> 

![](media/3-11a-create-interaction-between-visualizations/3-11a_1.png)

<span data-ttu-id="7c218-107">ในตอนนี้ เมื่อคุณเลือกการแสดงข้อมูลบนพื้นที่รายงานของคุณ คุณจะเห็นไอคอน*ตัวกรอง*ทึบแสงขนาดเล็กที่มุมขวาบนของการแสดงข้อมูลอื่นทั้งหมดที่ได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="7c218-107">Now when you select a visual on your report canvas, you'll see a small opaque *filter* icon in the top right-hand corner of every other visual it will affect.</span></span> <span data-ttu-id="7c218-108">เมื่อต้องการยกเว้นการแสดงผลด้วยภาพจากการโต้ตอบ ให้คลิกสัญลักษณ์ *ไม่มี* ที่มุมขวาบน ใกล้กับไอคอน*ตัวกรอง*</span><span class="sxs-lookup"><span data-stu-id="7c218-108">To exclude a visual from the interaction, click the *None* symbol in the upper right corner, near the *filter* icon.</span></span>

![](media/3-11a-create-interaction-between-visualizations/3-11a_2.png)

<span data-ttu-id="7c218-109">ในบางอินสแตนซ์ คุณสามารถปรับชนิดของการโต้ตอบตัวกรองที่เกิดขึ้นระหว่างการแสดงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7c218-109">In some instances you can adjust the type of filter interaction that happens between visuals.</span></span> <span data-ttu-id="7c218-110">เมื่อ**โหมดแก้ไข**เปิดอยู่ ให้เลือกการแสดงผลด้วยภาพที่คุณใช้ในการกรอง</span><span class="sxs-lookup"><span data-stu-id="7c218-110">With **Edit Mode** toggled on, select the visual you use to filter.</span></span> <span data-ttu-id="7c218-111">ถ้าคุณเปลี่ยนชนิดของการโต้ตอบบนการแสดงข้อมูลอื่น ไอคอน*แผนภูมิวงกลม*จะปรากฏอยู่ถัดจากไอคอนตัวกรองที่มุมขวาบน</span><span class="sxs-lookup"><span data-stu-id="7c218-111">If you can change the type of interaction on another visual, a *pie chart* icon will appear next to the filter icon in the top right-hand corner.</span></span>

![](media/3-11a-create-interaction-between-visualizations/3-11a_3.png)

<span data-ttu-id="7c218-112">คลิกไอคอน*แผนภูมิวงกลม*เพื่อเน้นข้อมูลที่แบ่งส่วนแล้ว</span><span class="sxs-lookup"><span data-stu-id="7c218-112">Click the *pie chart* icon to highlight the segmented data.</span></span> <span data-ttu-id="7c218-113">มิฉะนั้น ข้อมูลจะถูกกรอง</span><span class="sxs-lookup"><span data-stu-id="7c218-113">Otherwise, the data will be filtered.</span></span> <span data-ttu-id="7c218-114">เหมือนกับก่อนหน้านี้ คุณสามารถคลิกไอคอน *ไม่มี* เพื่อนำการโต้ตอบทั้งหมดออก</span><span class="sxs-lookup"><span data-stu-id="7c218-114">As before, you can click the *None* icon to remove all interaction.</span></span>

<span data-ttu-id="7c218-115">เคล็ดลับการออกแบบที่เป็นประโยชน์คือให้วาดรูปร่างโปร่งแสงรอบๆ การแสดงข้อมูลที่โต้ตอบกันและกัน ดังนั้น ผู้ใช้จึงเห็นได้อย่างชัดเจนว่ามีความสัมพันธ์การโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="7c218-115">A useful design tip is to draw a transparent shape around visuals that interact with each other, so it's clear to the user that they have an interactive relationship.</span></span>

![](media/3-11a-create-interaction-between-visualizations/3-11a_4.png)

