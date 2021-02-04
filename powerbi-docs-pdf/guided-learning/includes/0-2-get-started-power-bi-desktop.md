---
ms.openlocfilehash: 4c1a7bce8eb24534974fe6a06a8bada4ba9fb708
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2019
ms.locfileid: "61265199"
---
<span data-ttu-id="f8e3d-101">ในหัวข้อนี้ เราจะมาดูรายละเอียดของการทำงานร่วมกันของสองส่วนแรกของ Power BI</span><span class="sxs-lookup"><span data-stu-id="f8e3d-101">In this topic, we take a closer look at how the first two parts of Power BI fit together:</span></span>

* <span data-ttu-id="f8e3d-102">สร้างรายงานใน **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="f8e3d-102">Create a report in **Power BI Desktop**</span></span>
* <span data-ttu-id="f8e3d-103">เผยแพร่รายงานใน**บริการของ Power BI**</span><span class="sxs-lookup"><span data-stu-id="f8e3d-103">Publish the report in the **Power BI service**</span></span>

<span data-ttu-id="f8e3d-104">เราจะเริ่มต้นใน Power BI Desktop แล้วเลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="f8e3d-104">We’ll start in Power BI Desktop, and select **Get Data**.</span></span> <span data-ttu-id="f8e3d-105">คอลเลกชันของแหล่งข้อมูลจะปรากฏขึ้น ทำให้คุณเลือกแหล่งข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="f8e3d-105">The collection of data sources appears, allowing you to choose a data source.</span></span> <span data-ttu-id="f8e3d-106">รูปภาพต่อไปนี้แสดงการเลือกหน้าเว็บเป็นแหล่งข้อมูล ในวิดีโอทางด้านบน Will จะเลือกเวิร์กบุ๊ก **Excel**</span><span class="sxs-lookup"><span data-stu-id="f8e3d-106">The following image shows selecting a Web page as the source, in the video above, Will selected an **Excel** workbook.</span></span>

![](media/0-2-get-started-power-bi-desktop/c0a2_1.png)

<span data-ttu-id="f8e3d-107">ไม่ว่าคุณจะเลือกแหล่งข้อมูลใด Power BI จะเชื่อมต่อกับแหล่งข้อมูลนั้นและแสดงข้อมูลที่พร้อมใช้งานจากแหล่งข้อมูลดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="f8e3d-107">Regardless of which data source you choose, Power BI connects to that data source, and shows you the data available from that source.</span></span> <span data-ttu-id="f8e3d-108">รูปภาพต่อไปนี้เป็นอีกตัวอย่างหนึ่ง แหล่งข้อมูลนี้มาจากหน้าเว็บที่วิเคราะห์รัฐต่างๆ และสถิติการเกษียณที่น่าสนใจบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="f8e3d-108">The following image is another example, this one is from a Web page that analyzes different states and some interesting retirement statistics.</span></span>

![](media/0-2-get-started-power-bi-desktop/c0a2_2.png)

<span data-ttu-id="f8e3d-109">ในมุมมอง **รายงาน** ของ Power BI Desktop คุณสามารถเริ่มสร้างรายงานได้</span><span class="sxs-lookup"><span data-stu-id="f8e3d-109">In Power BI Desktop **Report** view, you can begin to build reports.</span></span>

<span data-ttu-id="f8e3d-110">มุมมอง **รายงาน** มีพื้นที่หลักห้าพื้นที่:</span><span class="sxs-lookup"><span data-stu-id="f8e3d-110">The **Report** view has five main areas:</span></span>

1. <span data-ttu-id="f8e3d-111">Ribbon ที่แสดงงานทั่วไปที่เชื่อมโยงกับรายงานและการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="f8e3d-111">The ribbon, which displays common tasks associated with reports and visualizations</span></span>
2. <span data-ttu-id="f8e3d-112">มุมมอง **รายงาน** หรือพื้นที่รายงาน คือพื้นที่สำหรับสร้างและจัดเรียงการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="f8e3d-112">The **Report** view, or canvas, where visualizations are created and arranged</span></span>
3. <span data-ttu-id="f8e3d-113">พื้นที่แท็บ **หน้า** ตลอดแนวด้านล่างมีไว้เพื่อให้คุณเลือกหรือเพิ่มหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="f8e3d-113">The **Pages** tab area along the bottom, which lets you select or add a report page</span></span>
4. <span data-ttu-id="f8e3d-114">ช่อง **การแสดงภาพ** คือที่ที่คุณสามารถเปลี่ยนการแสดงภาพ กำหนดค่าสีหรือแกน นำตัวกรองไปใช้ ลากเขตข้อมูล และอื่น ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="f8e3d-114">The **Visualizations** pane, where you can change visualizations, customize colors or axes, apply filters, drag fields, and more</span></span>
5. <span data-ttu-id="f8e3d-115">ช่อง **เขตข้อมูล** คือที่ที่สามารถลากองค์ประกอบคิวรี่และตัวกรองไปยังมุมมอง **รายงาน** หรือลากไปยังพื้นที่ **ตัวกรอง** ของช่อง **การแสดงภาพ** ได้</span><span class="sxs-lookup"><span data-stu-id="f8e3d-115">The **Fields** pane, where query elements and filters can be dragged onto the **Report** view, or dragged to the **Filters** area of the **Visualizations** pane</span></span>

![](media/0-2-get-started-power-bi-desktop/c0a2_3.png)

<span data-ttu-id="f8e3d-116">สามารถย่อช่อง **การแสดงภาพ** และ **เขตข้อมูล** ได้โดยการเลือกลูกศรขนาดเล็กที่ขอบ เพื่อให้มีพื้นที่มากขึ้นในมุมมอง **รายงาน** เพื่อสร้างการแสดงภาพที่ยอดเยี่ยม</span><span class="sxs-lookup"><span data-stu-id="f8e3d-116">The **Visualizations** and **Fields** pane can be collapsed by selecting the small arrow along the edge, providing more space in the **Report** view to build cool visualizations.</span></span> <span data-ttu-id="f8e3d-117">เมื่อปรับเปลี่ยนการแสดงภาพ คุณจะยังเห็นลูกศรเหล่านี้ชี้ขึ้นหรือลง ซึ่งหมายความว่าคุณสามารถขยายหรือย่อส่วนนั้นได้</span><span class="sxs-lookup"><span data-stu-id="f8e3d-117">When modifying visualizations, you'll also see these arrows pointing up or down, which means you can expand or collapse that section, accordingly.</span></span>

![](media/0-2-get-started-power-bi-desktop/c0a2_4.png)

<span data-ttu-id="f8e3d-118">เมื่อต้องการสร้างการจัดรูปแบบการแสดงข้อมูล ให้ลากเขตข้อมูลจากรายการ **เขตข้อมูล** ไปยังมุมมอง **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="f8e3d-118">To create a visualization, just drag a field from the **Fields** list onto the **Report** view.</span></span> <span data-ttu-id="f8e3d-119">ในกรณีนี้ เราจะลากเขตข้อมูล รัฐ จาก *RetirementStats* แล้วดูว่าจะเกิดอะไรขึ้น</span><span class="sxs-lookup"><span data-stu-id="f8e3d-119">In this case, let’s drag the State field from *RetirementStats*, and see what happens.</span></span>

![](media/0-2-get-started-power-bi-desktop/c0a2_5.png)

<span data-ttu-id="f8e3d-120">ดูนั่นสิ... Power BI Desktop สร้างการจัดรูปแบบการแสดงข้อมูลที่ยึดตามแผนที่ขึ้นโดยอัตโนมัติ เนื่องจากระบุได้ว่าเขตข้อมูล รัฐ นั้นเป็นข้อมูลทางภูมิศาสตร์</span><span class="sxs-lookup"><span data-stu-id="f8e3d-120">Look at that... Power BI Desktop automatically created a map-based visualization, because it recognized that the State field contained geolocation data.</span></span>

<span data-ttu-id="f8e3d-121">ในตอนนี้ เราจะเร่งความเร็วเล็กน้อย และหลังจากที่สร้างรายงานด้วยการจัดรูปแบบการแสดงข้อมูลแล้ว เราก็พร้อมที่จะเผยแพร่ไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="f8e3d-121">Now let’s fast-forward a bit, and after creating a report with a few visualizations, we’re ready to publish this to the Power BI service.</span></span> <span data-ttu-id="f8e3d-122">บน Ribbon **หน้าแรก** ใน Power BI Desktop ให้เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="f8e3d-122">On the **Home** ribbon in Power BI Desktop, select **Publish**.</span></span>

![](media/0-2-get-started-power-bi-desktop/c0a2_6.png)

<span data-ttu-id="f8e3d-123">คุณจะได้รับพร้อมท์ให้ลงชื่อเข้าใช้ Power BI</span><span class="sxs-lookup"><span data-stu-id="f8e3d-123">You’ll be prompted to sign in to Power BI.</span></span>

![](media/0-2-get-started-power-bi-desktop/c0a2_7.png)

<span data-ttu-id="f8e3d-124">เมื่อคุณลงชื่อเข้าใช้และเผยแพร่เรียบร้อยแล้ว คุณจะเห็นกล่องโต้ตอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f8e3d-124">When you've signed in and the publish process is complete, you see the following dialog.</span></span> <span data-ttu-id="f8e3d-125">คุณสามารถเลือกลิงก์ (ทางด้านล่างของ**สำเร็จแล้ว!** ) เพื่อไปยังบริการของ Power BI ที่คุณสามารถดูรายงานที่คุณเผยแพร่ได้</span><span class="sxs-lookup"><span data-stu-id="f8e3d-125">You can select the link (below **Success!**) to be taken to the Power BI service, where you can see the report you just published.</span></span>

![](media/0-2-get-started-power-bi-desktop/c0a2_8.png)

<span data-ttu-id="f8e3d-126">เมื่อคุณลงชื่อเข้าใช้ Power BI คุณจะเห็นไฟล์ Power BI Desktop ที่คุณเพิ่งเผยแพร่ในบริการ</span><span class="sxs-lookup"><span data-stu-id="f8e3d-126">When you sign in to Power BI, you'll see Power BI Desktop file you just published in the service.</span></span> <span data-ttu-id="f8e3d-127">ในรูปภาพทางด้านล่าง รายงานที่สร้างขึ้นใน Power BI Desktop จะแสดงในส่วน **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="f8e3d-127">In the image below, the report created in Power BI Desktop is shown in the **Reports** section.</span></span>

![](media/0-2-get-started-power-bi-desktop/c0a2_9.png)

<span data-ttu-id="f8e3d-128">ในรายงานนั้น ผมสามารถเลือกไอคอน **ปักหมุด** เพื่อปักหมุดการแสดงผลด้วยภาพนั้นในแดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="f8e3d-128">In that report, I can choose the **Pin** icon to pin that visual to a dashboard.</span></span> <span data-ttu-id="f8e3d-129">รูปภาพต่อไปนี้แสดงไอคอนปักหมุดที่มีการไฮไลต์ไว้ด้วยกล่องสว่างและลูกศร</span><span class="sxs-lookup"><span data-stu-id="f8e3d-129">The following image shows the pin icon highlighted with a bright box and arrow.</span></span>

![](media/0-2-get-started-power-bi-desktop/c0a2_10.png)

<span data-ttu-id="f8e3d-130">เมื่อผมเลือกแล้ว กล่องโต้ตอบต่อไปนี้จะปรากฏขึ้น ทำให้ผมสามารถปักหมุดการแสดงผลด้วยภาพในแดชบอร์ดที่มีอยู่แล้วได้ หรือสร้างแดชบอร์ดใหม่</span><span class="sxs-lookup"><span data-stu-id="f8e3d-130">When I select that, the following dialog appears, letting me pin the visual to an existing dashboard, or to create a new dashboard.</span></span>

![](media/0-2-get-started-power-bi-desktop/c0a2_11.png)

<span data-ttu-id="f8e3d-131">เมื่อเราปักหมุดการแสดงผลด้วยภาพบางส่วนจากรายงานของเราแล้ว เราจะสามารถดูได้ในแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="f8e3d-131">When we pin a couple of visuals from our report, we can see them in the dashboard.</span></span>

![](media/0-2-get-started-power-bi-desktop/c0a2_12.png)

<span data-ttu-id="f8e3d-132">แน่นอนว่ายังมีอีกหลายอย่างที่คุณสามารถทำได้ด้วย Power BI เช่น การแชร์แดชบอร์ดที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f8e3d-132">There’s a lot more you can do with Power BI, of course, such as sharing the dashboards you create.</span></span> <span data-ttu-id="f8e3d-133">เราจะอธิบายการแชร์ในภายหลังในหลักสูตรนี้</span><span class="sxs-lookup"><span data-stu-id="f8e3d-133">We'll discuss sharing later on in this course.</span></span>

<span data-ttu-id="f8e3d-134">ถัดจากนี้ เราจะแนะนำฟีเจอร์ที่สามารถสร้างแดชบอร์ดให้คุณได้โดยอัตโนมัติ เพียงเชื่อมต่อกับบริการระบบคลาวด์ เช่น Facebook, Salesforce และอื่นๆ อีกมากมาย</span><span class="sxs-lookup"><span data-stu-id="f8e3d-134">Next, we look at a feature that can automatically create dashboards for you, just by connecting to a cloud service like Facebook, Salesforce, and many others.</span></span>

