---
ms.openlocfilehash: 9aac366f04d53da56b62c10fdb85229d0d412834
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2019
ms.locfileid: "61397958"
---
<span data-ttu-id="47384-101">เมื่อคุณเพิ่มเขตข้อมูล*วันที่*ไปยังการแสดงผลด้วยภาพในบักเก็ตเขตข้อมูล*แกน* Power BI จะเพิ่มลำดับชั้นเวลาที่รวมถึง*ปี* *ไตรมาส* *เดือน* และ*วัน* โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="47384-101">When you add a *date* field to a visual in the *Axis* field bucket, Power BI automatically adds a time hierarchy that includes *Year*, *Quarter*, *Month* and *Day*.</span></span> <span data-ttu-id="47384-102">ด้วยการทำเช่นนี้ Power BI จะช่วยให้การแสดงผลด้วยภาพของคุณมีปฏิสัมพันธ์ตามเวลากับผู้ที่ดูรายงานของคุณ โดยให้ผู้ใช้ดูรายละเอียดแนวลึกผ่านระดับเวลาที่ต่างกัน</span><span class="sxs-lookup"><span data-stu-id="47384-102">By doing this, Power BI allows your visuals to have time-based interaction with those viewing your reports, by letting users drill-down through those different time levels.</span></span>

![](media/3-11g-visual-hierarchies-drilling/3-11g_1.png)

<span data-ttu-id="47384-103">ด้วยลำดับชั้นที่พร้อมแล้ว คุณสามารถเริ่มดูรายละเอียดแนวลึกผ่านลำดับชั้นของเวลาได้</span><span class="sxs-lookup"><span data-stu-id="47384-103">With a hierarchy in place, you can begin drilling down through the time hierarchy.</span></span> <span data-ttu-id="47384-104">ตัวอย่างเช่น การคลิกปีในแผนภูมิจะดูรายละเอียดแนวลึกไปยังระดับถัดไปในลำดับชั้น ซึ่งในกรณีนี้คือ*ไตรมาส*ที่จะแสดงในการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="47384-104">For example, clicking a year in the chart drills down to the next level in the hierarchy, in this case *Quarters*, which are then displayed in the visual.</span></span>

![](media/3-11g-visual-hierarchies-drilling/3-11g_2.png)

<span data-ttu-id="47384-105">ในลำดับชั้นที่สร้างขึ้นโดยอัตโนมัติ คุณยังสามารถจัดการว่ารายงานที่แชร์อนุญาตให้ผู้อื่นสามารถดูรายละเอียดแนวลึกได้ถึงระดับใด</span><span class="sxs-lookup"><span data-stu-id="47384-105">In that automatically created hierarchy, you can also manage to which level your shared report allows people to drill.</span></span> <span data-ttu-id="47384-106">เมื่อต้องการทำเช่นนี้ เพียงคลิก X ข้างลำดับชั้นที่คุณต้องการนำออกในบานหน้าต่างการจัดรูปแบบการแสดงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="47384-106">To do this, in the Visualizations pane, simply click the X beside the hierarchy that you want to remove.</span></span> <span data-ttu-id="47384-107">ระดับที่ถูกลบจะถูกนำออกจากรายงานและการดูรายละเอียดแนวลึกจะไม่แสดงระดับดังกล่าวอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="47384-107">The deleted level is removed from the report, and drilling no longer displays that level.</span></span>

![](media/3-11g-visual-hierarchies-drilling/3-11g_3.png)

<span data-ttu-id="47384-108">ถ้าคุณต้องการนำระดับของลำดับชั้นนั้นกลับมา เพียงนำเขตข้อมูล*วันที่* ออก จากนั้นเพิ่มเข้าไปอีกครั้งจากบานหน้าต่าง**เขตข้อมูล** แล้วลำดับชั้นจะสร้างขึ้นให้คุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="47384-108">If you need to get that level of the hierarchy back, just remove the *date* field, and then add it again from the **Fields** pane, and the hierarchy is once again created for you automatically.</span></span>

<span data-ttu-id="47384-109">บางครั้งคุณอาจไม่ต้องการใช้ลำดับชั้นสำหรับการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="47384-109">There may be times when you don't want the hierarchy to be used for a visual.</span></span> <span data-ttu-id="47384-110">คุณสามารถควบคุมได้โดยปุ่มลูกศรชี้ลงข้างเขตข้อมูล*วันที่* (เมื่อคุณได้เพิ่มเขตข้อมูลไปยังการแสดงผลด้วยภาพแล้ว) และเลือก**วันที่** แทนที่จะเป็น**ลำดับชั้นวันที่**</span><span class="sxs-lookup"><span data-stu-id="47384-110">You can control that by selecting the down-arrow button beside the *Date* field (once you've added it to a visual), and select **Date** rather than **Date Hierarchy**.</span></span> <span data-ttu-id="47384-111">ซึ่งจะพร้อมท์ให้ Power BI แสดงค่าวันที่ดิบในการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="47384-111">That prompts Power BI to show the raw date values in the visual.</span></span>

![](media/3-11g-visual-hierarchies-drilling/3-11g_4.png)

<span data-ttu-id="47384-112">นอกจากนี้คุณยังสามารถขยายองค์ประกอบข้อมูลทั้งหมดที่มองเห็นอยู่ได้ในครั้งเดียวแทนการเลือกไตรมาสเดียวหรือปีเดียว</span><span class="sxs-lookup"><span data-stu-id="47384-112">You can also expand all data elements currently visible at once, rather than selecting a single quarter, or a single year.</span></span> <span data-ttu-id="47384-113">เมื่อต้องการทำเช่นนั้น ให้เลือกไอคอน *ดูรายละเอียดแนวลึกทั้งหมด* ที่ด้านซ้ายบนของการแสดงผลด้วยภาพที่เป็นไอคอนลูกศรชี้ลงสองอัน</span><span class="sxs-lookup"><span data-stu-id="47384-113">To do that, select the *Drill all* icon in the top left of the visual, which is a double-down arrow icon.</span></span>

![](media/3-11g-visual-hierarchies-drilling/3-11g_5.png)

