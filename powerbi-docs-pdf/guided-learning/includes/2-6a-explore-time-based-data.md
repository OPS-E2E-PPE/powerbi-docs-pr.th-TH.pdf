---
ms.openlocfilehash: 48e553ebd81632cb0baa9a2c9c6a761860c3c9c6
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2019
ms.locfileid: "61257125"
---
<span data-ttu-id="9936d-101">การวิเคราะห์ข้อมูลตามเวลาด้วย Power BI เป็นเรื่องง่าย</span><span class="sxs-lookup"><span data-stu-id="9936d-101">It's easy to analyze time-based data with Power BI.</span></span> <span data-ttu-id="9936d-102">เครื่องมือการวางรูปแบบใน Power BI Desktop จะใส่เขตข้อมูลที่สร้างขึ้นโดยอัตโนมัติ ซึ่งช่วยให้คุณสามารถดูรายละเอียดแนวลึกของปี ไตรมาส เดือน และวันได้ด้วยการคลิกเพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="9936d-102">The modeling tools in Power BI Desktop automatically include generated fields that let you drill down through years, quarters, months, and days with a single click.</span></span>  

<span data-ttu-id="9936d-103">เมื่อคุณสร้างการจัดรูปแบบการแสดงข้อมูลตารางในรายงานของคุณโดยใช้เขตข้อมูลวันที่ Power BI Desktop จะใส่การแบ่งตามช่วงเวลาโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9936d-103">When you create a table visualization in your report using a date field, Power BI Desktop automatically includes breakdowns by time period.</span></span> <span data-ttu-id="9936d-104">ตัวอย่างเช่น เขตข้อมูลวันที่เดียวในตาราง **วันที่** จะถูกแบ่งเป็นปี ไตรมาส เดือน และวันโดยอัตโนมัติด้วย Power BI ตามที่แสดงในรูปภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9936d-104">For example, the single date field in the **Date** table was automatically separated into Year, Quarter, Month and Day by Power BI, as shown in the following image.</span></span>

![](media/2-6a-explore-time-based-data/2-6a_1.png)

<span data-ttu-id="9936d-105">การจัดรูปแบบการแสดงข้อมูลจะแสดงข้อมูลที่ระดับ*ปี*ตามค่าเริ่มต้น แต่คุณสามารถเปลี่ยนได้โดยการเปิด **ดูรายละเอียดแนวลึก** ที่มุมขวาบนของการแสดงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9936d-105">Visualizations display data at the *year* level by default, but you can change that by turning on **Drill Down** in the top right-hand corner of the visual.</span></span>

![](media/2-6a-explore-time-based-data/2-6a_2.png)

<span data-ttu-id="9936d-106">ในตอนนี้ เมื่อคุณคลิกที่แถบหรือเส้นในแผนภูมิจะดูรายละเอียดแนวลึกลงในระดับถัดไปของลำดับชั้นเวลา ตัวอย่างเช่น จาก*ปี*เป็น*ไตรมาส*</span><span class="sxs-lookup"><span data-stu-id="9936d-106">Now when you click on the bars or lines in your chart, it drills down to the next level of time hierarchy, for example from *years* to *quarters*.</span></span> <span data-ttu-id="9936d-107">คุณสามารถดูรายละเอียดแนวลึกได้อย่างต่อเนื่องจนกว่าจะถึงระดับที่เล็กที่สุดของลำดับชั้น ซึ่งในตัวอย่างนี้คือ*วัน*</span><span class="sxs-lookup"><span data-stu-id="9936d-107">You can continue to drill down until you reach the most granular level of the hierarchy, which in this example is *days*.</span></span> <span data-ttu-id="9936d-108">เมื่อต้องการย้อนกลับผ่านลำดับชั้นเวลา ให้คลิก **เลื่อนขึ้น** ที่มุมซ้ายบนของการแสดงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9936d-108">To move back up through the time hierarchy, click on **Drill Up** in the top left-hand corner of the visual.</span></span>

![](media/2-6a-explore-time-based-data/2-6a_3.png)

<span data-ttu-id="9936d-109">แทนที่จะดูรายละเอียดแนวลึกเฉพาะช่วงเวลาที่เลือก คุณยังสามารถเจาะลึกผ่านข้อมูลทั้งหมดที่แสดงบนการแสดงข้อมูลได้โดยใช้ไอคอนลูกศรคู่ **เจาะลึกทั้งหมด** ที่มุมขวาบนของการแสดงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9936d-109">You can also drill down through all of the data shown on the visual, rather than one selected period, by using the **Drill All** double-arrow icon, also in the top right-hand corner of the visual.</span></span>

![](media/2-6a-explore-time-based-data/2-6a_4.png)

<span data-ttu-id="9936d-110">ตราบใดที่แบบจำลองของคุณมีเขตข้อมูลวันที่ Power BI จะสร้างมุมมองต่างๆ สำหรับลำดับชั้นเวลาโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9936d-110">As long as your model has a date field, Power BI will automatically generate different views for different time hierarchies.</span></span>

<span data-ttu-id="9936d-111">เมื่อต้องการย้อนกลับไปยังวันที่แต่ละวันแทนที่จะใช้ลำดับชั้นวันที่ ให้คลิกขวาที่ชื่อคอลัมน์ใน **เขตข้อมูล** (ในรูปภาพต่อไปนี้ ชื่อของคอลัมน์จะเป็น *InvoiceDate*) แล้วเลือกชื่อคอลัมน์จากเมนูที่ปรากฏขึ้น แทนที่จะเลือก **ลำดับชั้นวันที่**</span><span class="sxs-lookup"><span data-stu-id="9936d-111">To get back to individual dates rather than using the date hierarchy, simply right-click the column name in the **Fields** well (in the following image, the name of the column is *InvoiceDate*), then select the column name from the menu that appears, rather than **Date Hierarchy**.</span></span> <span data-ttu-id="9936d-112">การแสดงข้อมูลของคุณจะแสดงข้อมูลโดยยึดตามข้อมูลคอลัมน์โดยไม่ใช้ลำดับชั้นวันที่</span><span class="sxs-lookup"><span data-stu-id="9936d-112">Your visual then shows the data based on that column data, without using the date hierarchy.</span></span> <span data-ttu-id="9936d-113">ต้องการย้อนกลับไปใช้ลำดับชั้นวันที่ใช่ไหม</span><span class="sxs-lookup"><span data-stu-id="9936d-113">Need to go back to using the date hierarchy?</span></span> <span data-ttu-id="9936d-114">ไม่มีปัญหา เพียงคลิกขวาอีกครั้ง แล้วเลือก **ลำดับชั้นวันที่** จากเมนู</span><span class="sxs-lookup"><span data-stu-id="9936d-114">No problem - just right-click again and select **Date Hierarchy** from the menu.</span></span>

![](media/2-6a-explore-time-based-data/2-6a_5.png)

## <a name="next-steps"></a><span data-ttu-id="9936d-115">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="9936d-115">Next steps</span></span>
<span data-ttu-id="9936d-116">**ยินดีด้วย!**</span><span class="sxs-lookup"><span data-stu-id="9936d-116">**Congratulations!**</span></span> <span data-ttu-id="9936d-117">คุณได้สำเร็จส่วนนี้ของหลักสูตร **การเรียนรู้พร้อมคำแนะนำ** สำหรับ Power BI แล้ว</span><span class="sxs-lookup"><span data-stu-id="9936d-117">You've completed this section of the **Guided Learning** course for Power BI.</span></span> <span data-ttu-id="9936d-118">ในตอนนี้ คุณทราบเกี่ยวกับข้อมูล*การวางรูปแบบ*แล้ว คุณพร้อมที่จะเรียนรู้เกี่ยวกับสิ่งที่น่าสนุกที่กำลังรอคุณอยู่ในส่วนถัดไป:  **การจัดรูปแบบการแสดงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="9936d-118">Now that you know about *modeling* data, you're ready to learn about the fun stuff waiting in the next section: **Visualizations**.</span></span>

<span data-ttu-id="9936d-119">ตามที่เราเคยกล่าวไว้ก่อนหน้านี้ หลักสูตรนี้จะสร้างความรู้โดยการทำตามขั้นตอนการทำงานทั่วไปใน Power BI:</span><span class="sxs-lookup"><span data-stu-id="9936d-119">As mentioned before, this course builds your knowledge by following the common flow of work in Power BI:</span></span>

* <span data-ttu-id="9936d-120">นำข้อมูลเข้าสู่ **Power BI Desktop** แล้วสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="9936d-120">Bring data into **Power BI Desktop**, and create a report.</span></span>
* <span data-ttu-id="9936d-121">เผยแพร่ไปยังบริการของ Power BI ที่คุณสามารถสร้าง**การจัดรูปแบบการแสดงข้อมูล**ใหม่ได้ และสร้างแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="9936d-121">Publish to the Power BI service, where you create new **visualizations** and build dashboards</span></span>
* <span data-ttu-id="9936d-122">**แชร์**แดชบอร์ดของคุณกับผู้อื่น โดยเฉพาะผู้ที่กำลังเดินทาง</span><span class="sxs-lookup"><span data-stu-id="9936d-122">**Share** your dashboards with others, especially people who are on the go</span></span>
* <span data-ttu-id="9936d-123">ดูและโต้ตอบกับแดชบอร์ดและรายงานที่แชร์ในแอป **Power BI บนมือถือ**</span><span class="sxs-lookup"><span data-stu-id="9936d-123">View and interact with shared dashboards and reports in **Power BI Mobile** apps</span></span>

![](media/2-6a-explore-time-based-data/c0a1_1.png)

<span data-ttu-id="9936d-124">แม้ว่าคุณอาจไม่ต้องทำงานทั้งหมดด้วยตนเอง คุณต้อง*ทำความเข้าใจ*วิธีการสร้างแดชบอร์ดเหล่านั้น และวิธีการเชื่อมต่อกับข้อมูล... และเมื่อคุณสำเร็จหลักสูตรนี้แล้ว คุณจะสามารถสร้างแดชบอร์ดของคุณเองได้</span><span class="sxs-lookup"><span data-stu-id="9936d-124">While you might not do all that work yourself, you'll *understand* how those dashboards were created, and how they connected to the data... and when you're done with this course, you'll be able to create one of your own.</span></span>

<span data-ttu-id="9936d-125">เจอกันในส่วนถัดไป!</span><span class="sxs-lookup"><span data-stu-id="9936d-125">See you in the next section!</span></span>

