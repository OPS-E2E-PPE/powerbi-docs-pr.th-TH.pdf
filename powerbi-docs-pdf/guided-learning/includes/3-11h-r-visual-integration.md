---
ms.openlocfilehash: 226fdd59b00dc2daa625f9b1941599d21cc35087
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2019
ms.locfileid: "61397937"
---
<span data-ttu-id="6ab38-101">ด้วย Power BI Desktop คุณสามารถวิเคราะห์เชิงวิเคราะห์และวิเคราะห์เชิงสถิติและสร้างการแสดงผลด้วยภาพที่น่าสนใจโดยผสานรวมกับ R คุณสามารถโฮสต์การจัดรูปแบบการแสดงข้อมูลแบบ R เหล่านั้นภายในรายงาน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="6ab38-101">With Power BI Desktop, you can perform analytical and statistical analysis and create compelling visuals by integrating with R. You can host those R visualizations within the Power BI Desktop report.</span></span>

<span data-ttu-id="6ab38-102">เมื่อคุณเลือกไอคอน **การแสดงผลด้วยภาพแบบ R** จากบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล** Power BI จะสร้างตัวแทนบนพื้นที่ทำงานเพื่อโฮสต์การแสดงผลด้วยภาพแบบ R ของคุณ แล้วจึงแสดงตัวแก้ไขสคริปต์ R ให้คุณใช้บนพื้นที่ทำงานได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="6ab38-102">When you select the **R visual** icon from the **Visualizations** pane, Power BI creates a placeholder on the canvas to host your R visual, and then presents an R script editor for you to use right on the canvas.</span></span> <span data-ttu-id="6ab38-103">เมื่อคุณเพิ่มเขตข้อมูลลงในการแสดงผลด้วยภาพแบบ R, Power BI Desktop จะเพิ่มเขตข้อมูลลงในบานหน้าต่างตัวแก้ไขสคริปต์ R</span><span class="sxs-lookup"><span data-stu-id="6ab38-103">As you add fields to the R visual, Power BI Desktop adds them to the R script editor pane.</span></span>

![](media/3-11h-r-visual-integration/3-11h_1.png)

<span data-ttu-id="6ab38-104">ภายใต้สิ่งที่ Power BI สร้างขึ้นใน ตัวแก้ไขสคริปต์ R คุณสามารถเริ่มต้นสร้างสคริปต์ R ของคุณเพื่อสร้างการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="6ab38-104">Below what Power BI generates in the R script editor, you can begin creating your R script to generate the visual.</span></span> <span data-ttu-id="6ab38-105">เมื่อสคริปต์ของคุณเสร็จสมบูรณ์ ให้เลือก **เรียกใช้** แล้วเหตุการณ์ต่อไปนี้จะเกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="6ab38-105">Once your script is complete, select **Run** and the following occurs:</span></span>

1. <span data-ttu-id="6ab38-106">ข้อมูลที่เพิ่มเข้าไปยังการแสดงผลด้วยภาพ (จากบานหน้าต่าง **เขตข้อมูล**) ส่งมาจาก Power BI Desktop เพื่อการติดตั้ง R ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="6ab38-106">The data added to the visual (from the **Fields** pane) is sent from Power BI Desktop to the local installation of R</span></span>
2. <span data-ttu-id="6ab38-107">สคริปต์ที่สร้างในตัวแก้ไขสคริปต์ R ของ Power BI Desktop ทำงานบนการติดตั้ง R ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="6ab38-107">The script created in the Power BI Desktop R script editor is run on that local installation of R</span></span>
3. <span data-ttu-id="6ab38-108">จากนั้น Power BI Desktop จะได้รับการแสดงผลด้วยภาพกลับมาจากการติดตั้ง R และแสดงบนพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="6ab38-108">Then Power BI Desktop gets a visual back from the R installation, and displays it on the canvas</span></span>

<span data-ttu-id="6ab38-109">ทั้งหมดเกิดขึ้นค่อนข้างรวดเร็วและผลจะปรากฏในการจัดรูปแบบการแสดงข้อมูล**การแสดงผลด้วยภาพแบบ R** บนพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="6ab38-109">It all happens quite quickly, and the result appears in the **R visual** visualization on the canvas.</span></span>

![](media/3-11h-r-visual-integration/3-11h_2.png)

<span data-ttu-id="6ab38-110">คุณสามารถเปลี่ยนแปลงการแสดงผลด้วยภาพแบบ R โดยการปรับสคริปต์ R แล้วจึงเลือก **เรียกใช้** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="6ab38-110">You can change the R visual by adjusting the R script, and then selecting **Run** again.</span></span> <span data-ttu-id="6ab38-111">ในรูปต่อไปนี้ เราได้เปลี่ยนแปลงการแสดงผลด้วยภาพ เพื่อแสดงวงกลมแทนที่สี่เหลี่ยม</span><span class="sxs-lookup"><span data-stu-id="6ab38-111">In the following image, we changed the visual to display circles instead of squares.</span></span>

![](media/3-11h-r-visual-integration/3-11h_3.png)

<span data-ttu-id="6ab38-112">และเนื่องจากการแสดงผลด้วยภาพแบบ R นั้นเหมือนกันกับการแสดงผลด้วยภาพอื่นๆ ใน Power BI Desktop คุณสามารถโต้ตอบกับการแสดงผลด้วยภาพแบบ R และเชื่อมต่อกับการแสดงผลด้วยภาพอื่นๆ บนพื้นที่ทำงานได้ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="6ab38-112">And since the R visual is just like any other visual in Power BI Desktop, you can interact with it and make connections with other visuals on the canvas as well.</span></span> <span data-ttu-id="6ab38-113">เมื่อคุณโต้ตอบกับการแสดงผลด้วยภาพอื่นๆ บนพื้นที่ทำงานผ่านตัวกรองหรือการเน้น การแสดงผลด้วยภาพแบบ R จะตอบสนองเหมือนการแสดงผลด้วยภาพ Power BI อื่นๆ โดยอัตโนมัติโดยไม่จำเป็นต้องปรับสคริปต์ R</span><span class="sxs-lookup"><span data-stu-id="6ab38-113">When you interact with other visuals on the canvas, through filtering or highlighting, the R visual automatically reacts just like any other Power BI visual, without needing to adjust the R script.</span></span>

<span data-ttu-id="6ab38-114">ซึ่งเป็นวิธีที่ยอดเยี่ยมในการใช้พลังของ R โดยตรงใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="6ab38-114">It's a great way to use the power of R, right in Power BI Desktop.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6ab38-115">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="6ab38-115">Next steps</span></span>
<span data-ttu-id="6ab38-116">**ยินดีด้วย!**</span><span class="sxs-lookup"><span data-stu-id="6ab38-116">**Congratulations!**</span></span> <span data-ttu-id="6ab38-117">คุณได้เรียนรู้ส่วน**การจัดรูปแบบการแสดงข้อมูล**ของหลักสูตร**การเรียนรู้ตามคำแนะนำ**สำหรับ Power BI เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="6ab38-117">You've completed this **Visualizations** section of the **Guided Learning** course for Power BI.</span></span> <span data-ttu-id="6ab38-118">คุณสามารถพิจารณาตัวเองว่ามีความรอบรู้ในการจัดรูปแบบการแสดงข้อมูลหลายแบบที่มีใน Power BI แล้ว และยังมีความรู้เกี่ยวกับวิธีการใช้ ปรับเปลี่ยน และกำหนดการจัดรูปแบบการแสดงข้อมูลด้วยตนเองอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="6ab38-118">You can consider yourself well-versed in the many visualizations offered in Power BI, and also knowledgeable about how to use, modify, and customize them.</span></span> <span data-ttu-id="6ab38-119">ข่าวดี: การจัดรูปแบบการแสดงข้อมูลมีพื้นฐานเหมือนกันใน Power BI Desktop และบริการของ Power BI ดังนั้นสิ่งที่คุณเรียนรู้สามารถนำไปใช้ได้กับทั้งคู่</span><span class="sxs-lookup"><span data-stu-id="6ab38-119">And good news: visualizations are essentially the same in Power BI Desktop and the Power BI service, so what you learned applies to both.</span></span>

<span data-ttu-id="6ab38-120">ตอนนี้คุณก็พร้อมแล้วที่จะไปยังระบบคลาวด์และจดจ่อกับบริการของ Power BI ที่คุณสามารถ**สำรวจข้อมูล**ได้</span><span class="sxs-lookup"><span data-stu-id="6ab38-120">You're now ready to head to the cloud and get immersed in the Power BI service, where you can **Explore Data**.</span></span> <span data-ttu-id="6ab38-121">ตามที่คุณทราบ โฟลว์ของงานมีลักษณะดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6ab38-121">As you know, the flow of work looks something like the following:</span></span>

* <span data-ttu-id="6ab38-122">นำข้อมูลเข้าไปยัง **Power BI Desktop** และสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="6ab38-122">Bring data into **Power BI Desktop**, and create a report.</span></span>
* <span data-ttu-id="6ab38-123">เผยแพร่ไปยังบริการของ Power BI ที่คุณสามารถสร้าง**การจัดรูปแบบการแสดงข้อมูล**ใหม่ได้ และสร้างแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="6ab38-123">Publish to the Power BI service, where you create new **visualizations** and build dashboards</span></span>
* <span data-ttu-id="6ab38-124">**แชร์**แดชบอร์ดของคุณกับผู้อื่น โดยเฉพาะผู้ที่กำลังเดินทาง</span><span class="sxs-lookup"><span data-stu-id="6ab38-124">**Share** your dashboards with others, especially people who are on the go</span></span>
* <span data-ttu-id="6ab38-125">ดูและโต้ตอบกับแดชบอร์ดและรายงานที่แชร์ในแอป **Power BI บนมือถือ**</span><span class="sxs-lookup"><span data-stu-id="6ab38-125">View and interact with shared dashboards and reports in **Power BI Mobile** apps</span></span>

![](media/3-11h-r-visual-integration/c0a1_1.png)

<span data-ttu-id="6ab38-126">ไม่ว่าคุณจะสร้างรายงานหรือเพียงแค่ดูและโต้ตอบกับรายงาน ตอนนี้คุณก็ได้รู้วิธีการสร้างการแสดงผลด้วยภาพสุดเจ๋ง และวิธีการเชื่อมต่อการแสดงผลด้วยภาพเข้ากับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6ab38-126">Whether you create reports or just view and interact with them, you now know how all those cool visuals are created, and how they connected to the data.</span></span> <span data-ttu-id="6ab38-127">ถัดไปเราจะได้เห็นการแสดงผลด้วยภาพและรายงานในการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="6ab38-127">Next we get to see those visuals and reports in action.</span></span>

<span data-ttu-id="6ab38-128">พบกันในส่วนถัดไป!</span><span class="sxs-lookup"><span data-stu-id="6ab38-128">See you in the next section!</span></span>

