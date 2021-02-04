---
title: สร้างเมทริกซ์วิชวลใน Power BI
description: เรียนรู้เพิ่มเติมเกี่ยวกับเมทริกซ์วิชวล ว่าสามารถทำให้การวางรูปแบบเป็นขั้นและการเน้นแกรนูลาร์ใน Power BI ได้อย่างไร
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: conceptual
ms.date: 06/18/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 401d8905c4fe2ca0f27a8f0c58bd756c87a10456
ms.sourcegitcommit: 0711972326521944fdd8572403c0b15f31b916da
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/22/2020
ms.locfileid: "97721512"
---
# <a name="create-matrix-visualizations-in-power-bi"></a><span data-ttu-id="a4e15-103">สร้างการแสดงข้อมูลเมทริกซ์ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="a4e15-103">Create matrix visualizations in Power BI</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="a4e15-104">เมทริกซ์วิชวลจะคล้ายกับตาราง</span><span class="sxs-lookup"><span data-stu-id="a4e15-104">The matrix visual is similar to a table.</span></span>  <span data-ttu-id="a4e15-105">ตารางสนับสนุนสองมิติและข้อมูลที่อยู่แบบแฟลตหมายความว่าการคัดลอกวิธีแสดงค่าจะไม่รวมกัน</span><span class="sxs-lookup"><span data-stu-id="a4e15-105">A table supports two dimensions and the data is flat, meaning duplicate values are displayed and not aggregated.</span></span> <span data-ttu-id="a4e15-106">เมทริกซ์ทำให้การแสดงข้อมูลง่ายและมีความหมายในทั้งหลายมิติและเมทริกซ์สนับสนุนการจัดวางอย่างเป็นขั้นเป็นตอน</span><span class="sxs-lookup"><span data-stu-id="a4e15-106">A matrix makes it easier to display data meaningfully across multiple dimensions -- it supports a stepped layout.</span></span> <span data-ttu-id="a4e15-107">เมทริกซ์จะรวมข้อมูลโดยอัตโนมัติและสามารถเจาะลึกลงไป</span><span class="sxs-lookup"><span data-stu-id="a4e15-107">The matrix automatically aggregates the data and enables drill down.</span></span> 

<span data-ttu-id="a4e15-108">คุณสามารถสร้างวิชวลเมทริกซ์ในรายงาน **Power BI Desktop** และทำไฮไลต์เชื่อมโยงองค์ประกอบภายในเมทริกซ์กับวิชวลอื่น ๆ ที่อยู่ในหน้ารายงานนั้น</span><span class="sxs-lookup"><span data-stu-id="a4e15-108">You can create matrix visuals in **Power BI Desktop** reports and cross-highlight elements within the matrix with other visuals on that report page.</span></span> <span data-ttu-id="a4e15-109">ยกตัวอย่างเช่นคุณยังสามารถเลือกแถว คอลัมน์ และแม้แต่ละเซลล์ และทำไฮไลต์เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="a4e15-109">For example, you can select rows, columns, and even individual cells and cross-highlight.</span></span> <span data-ttu-id="a4e15-110">และยังสามารถคัดลอกเซลล์เดียวและหลายเซลล์ และวางลงในแอปพลิเคชันอื่นได้</span><span class="sxs-lookup"><span data-stu-id="a4e15-110">Also, individual cells and multiple cell selections can be copied and pasted into other applications.</span></span> 

![ข้ามเมทริกซ์ที่ถูกเน้นและแผนภูมิโดนัท](media/desktop-matrix-visual/matrix-visual_2a.png)

<span data-ttu-id="a4e15-112">มีคุณลักษณะมากมายที่เกี่ยวข้องกับเมทริกซ์ และเราจะไปศึกษาในส่วนต่อ ๆ ไปของบทความนี้</span><span class="sxs-lookup"><span data-stu-id="a4e15-112">There are many features associated with the matrix, and we'll go through them in the following sections of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="a4e15-113">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="a4e15-113">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span>

## <a name="understanding-how-power-bi-calculates-totals"></a><span data-ttu-id="a4e15-114">ทำความเข้าใจวิธีที่ Power BI คำนวณผลรวม</span><span class="sxs-lookup"><span data-stu-id="a4e15-114">Understanding how Power BI calculates totals</span></span>

<span data-ttu-id="a4e15-115">ก่อนที่จะเข้าสู่เรื่องวิธีใช้วิชวลเมทริกซ์ คุณจำเป็นต้องเรียนรู้วิธีที่ Power BI คำนวณค่าผลรวมและผลรวมย่อยในตารางและเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="a4e15-115">Before jumping into how to use the matrix visual, it's important to learn how Power BI calculates total and subtotal values in tables and matrices.</span></span> <span data-ttu-id="a4e15-116">สำหรับแถวผลรวมและผลรวมย่อย Power Bi จะประเมิน หน่วยวัดจากแถวทั้งหมดในข้อมูลเบื้องต้น - ซึ่งไม่เพียงแค่การบวกค่าในแถวมองเห็นได้ หรือแถวที่แสดงตรง ๆ</span><span class="sxs-lookup"><span data-stu-id="a4e15-116">For total and subtotal rows, Power BI evaluates the measure over all rows in the underlying data – it isn't just a simple addition of the values in the visible or displayed rows.</span></span> <span data-ttu-id="a4e15-117">นี่หมายความว่า คุณอาจได้ค่าผลรวมที่ต่างจากที่คุณคาดหวัง</span><span class="sxs-lookup"><span data-stu-id="a4e15-117">This means you can end up with different values in the total row than you might expect.</span></span>

<span data-ttu-id="a4e15-118">ลองดูวิชวลเมทริกซ์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a4e15-118">Take a look at the following matrix visuals.</span></span> 

![เปรียบเทียบตารางและเมทริกซ์](media/desktop-matrix-visual/matrix-visual_3.png)

<span data-ttu-id="a4e15-120">ในตัวอย่างนี้ แต่ละแถวในของวิชวลเมทริกซ์ที่อยู่ทางด้านขวาสุดแสดง *ยอดรวม* สำหรับแต่ละคู่ของ พนักงานขาย/วันที่</span><span class="sxs-lookup"><span data-stu-id="a4e15-120">In this example, each row in the matrix visual farthest to the right is showing the *Amount* for each salesperson/date combination.</span></span> <span data-ttu-id="a4e15-121">แต่เนื่องจากพนักงานขายปรากฏในวันที่หลาย ๆ วัน ตัวเลขอาจปรากฏขึ้นมากกว่าหนึ่งครั้ง</span><span class="sxs-lookup"><span data-stu-id="a4e15-121">However, since a salesperson shows up against multiple dates, the numbers can appear more than once.</span></span> <span data-ttu-id="a4e15-122">ดังนั้น ผลรวมที่ถูกต้องจากข้อมูลต้นแบบ กับการบวกง่าย ๆ ของค่าที่มองเห็น จะไม่เท่ากัน</span><span class="sxs-lookup"><span data-stu-id="a4e15-122">Thus, the accurate total from the underlying data, and a simple addition of the visible values, do not equate.</span></span> <span data-ttu-id="a4e15-123">นี่คือรูปแบบที่พบบ่อย เมื่อค่าที่คุณกำลังรวมอยู่บนด้าน 'หนึ่ง' ของความสัมพันธ์แบบหนึ่งต่อกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="a4e15-123">This is a common pattern when the value you’re summing is on the ‘one’ side of a one-to-many relationship.</span></span>

<span data-ttu-id="a4e15-124">เมื่อคุณดูผลรวมและผลรวมย่อย จำไว้ว่าค่าเหล่านั้นจะยึดตามข้อมูลเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="a4e15-124">When you look at totals and subtotals, remember that those values are based on the underlying data.</span></span> <span data-ttu-id="a4e15-125">ค่าเหล่านั้นไม่ได้ยึดตามตัวเลขที่มองเห็นเพียงอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="a4e15-125">They aren't solely based on the visible values.</span></span>


## <a name="expanding-and-collapsing-row-headers"></a><span data-ttu-id="a4e15-126">การขยายและการยุบส่วนหัวของแถว</span><span class="sxs-lookup"><span data-stu-id="a4e15-126">Expanding and collapsing row headers</span></span>
<span data-ttu-id="a4e15-127">มีสองวิธีที่คุณสามารถขยายส่วนหัวของแถวได้</span><span class="sxs-lookup"><span data-stu-id="a4e15-127">There are two ways you can expand row headers.</span></span> <span data-ttu-id="a4e15-128">ขั้นตอนแรกคือการคลิกขวาที่เมนู</span><span class="sxs-lookup"><span data-stu-id="a4e15-128">The first is through the right-click menu.</span></span> <span data-ttu-id="a4e15-129">คุณจะเห็นตัวเลือกเพื่อขยายส่วนหัวของแถวนั้นๆ ที่คุณเลือก ระดับทั้งหมด หรือทุกอย่างไปจนถึงระดับสุดท้ายของลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="a4e15-129">You’ll see options to expand the specific row header you selected, the entire level, or everything down to the very last level of the hierarchy.</span></span> <span data-ttu-id="a4e15-130">คุณมีตัวเลือกที่คล้ายกันสำหรับการยุบส่วนหัวของแถวเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="a4e15-130">You have similar options for collapsing row headers as well.</span></span>

![เมนูแสดงการขยายและการเลือก](media/desktop-matrix-visual/power-bi-expand1.png)

<span data-ttu-id="a4e15-132">คุณยังสามารถเพิ่มปุ่ม +/- ไปยังส่วนหัวของแถวผ่านบานหน้าต่างการจัดรูปแบบภายใต้การ์ด **ส่วนหัวของแถว** ได้</span><span class="sxs-lookup"><span data-stu-id="a4e15-132">You can also add +/- buttons to the row headers through the formatting pane under the **Row headers** card.</span></span> <span data-ttu-id="a4e15-133">ตามค่าเริ่มต้น ไอคอนจะตรงกับการจัดรูปแบบของส่วนหัวของแถว แต่คุณสามารถกำหนดสีและขนาดของไอคอนแยกต่างหากได้ถ้าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="a4e15-133">By default, the icons will match the formatting of the row header, but you can customize the icons’ colors and sizes separately if you want.</span></span>

<span data-ttu-id="a4e15-134">เมื่อเปิดไอคอนแล้ว จะทำงานคล้ายกับไอคอน PivotTable ใน Excel</span><span class="sxs-lookup"><span data-stu-id="a4e15-134">Once the icons are turned on, they work similar to PivotTable icons in Excel.</span></span>

![เมทริกซ์แสดงไอคอนที่เปิดอยู่](media/desktop-matrix-visual/power-bi-expand2.png)

<span data-ttu-id="a4e15-136">สถานะการขยายของเมทริกซ์จะบันทึกกับรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="a4e15-136">The expansion state of the matrix will save with your report.</span></span> <span data-ttu-id="a4e15-137">คุณสามารถปักหมุดเมทริกซ์ไปยังแดชบอร์ดที่ขยายหรือยุบได้</span><span class="sxs-lookup"><span data-stu-id="a4e15-137">A matrix can be pinned to a dashboard expanded or collapsed.</span></span> <span data-ttu-id="a4e15-138">เมื่อเลือกไทล์แดชบอร์ดและรายงานเปิดอยู่ ยังสามารถเปลี่ยนแปลงสถานะการขยายในรายงานได้</span><span class="sxs-lookup"><span data-stu-id="a4e15-138">When that dashboard tile is selected, and the report opens, the expansion state can still be changed in the report.</span></span> 

![เมทริกซ์แสดงสถานะการขยาย](media/desktop-matrix-visual/power-bi-expand3.png)

> [!NOTE]
> <span data-ttu-id="a4e15-140">ถ้าคุณกำลังสร้างรายงานเพิ่มเติมจากโมเดล Analysis Services หลายมิติ จะมีข้อควรพิจารณาพิเศษบางอย่างสำหรับการขยาย/ยุบ ในกรณีที่แบบจำลองนั้นใช้คุณลักษณะสมาชิกเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a4e15-140">If you're building a report on top of an Analysis Services multidimensional model, there are some special considerations for expand/collapse if the model uses the Default Member feature.</span></span> <span data-ttu-id="a4e15-141">สำหรับข้อมูลเพิ่มเติม โปรดอ่านที่[ทำงานกับแบบจำลองหลายมิติใน Power BI](../connect-data/desktop-default-member-multidimensional-models.md)</span><span class="sxs-lookup"><span data-stu-id="a4e15-141">For more information see [Work with multidimensional models in Power BI](../connect-data/desktop-default-member-multidimensional-models.md)</span></span>

## <a name="using-drill-down-with-the-matrix-visual"></a><span data-ttu-id="a4e15-142">การดูรายละเอียดแนวลึกในภาพเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="a4e15-142">Using drill down with the matrix visual</span></span>
<span data-ttu-id="a4e15-143">ด้วยการแสดงผลด้วยภาพเมทริกซ์คุณสามารถทำการดูรายละเอียดแนวลึกที่น่าสนใจทุกประเภทที่ไม่เคยมีมาก่อน</span><span class="sxs-lookup"><span data-stu-id="a4e15-143">With the matrix visual, you can do all sorts of interesting drill-down activities that weren't available before.</span></span> <span data-ttu-id="a4e15-144">ซึ่งรวมถึงความสามารถในการดูรายละเอียดแนวลึกที่ระดับแถว คอลัมน์ และแม้แต่ส่วนและเซลล์</span><span class="sxs-lookup"><span data-stu-id="a4e15-144">This includes the ability to drill down using rows, columns, and even into individual sections and cells.</span></span> <span data-ttu-id="a4e15-145">ลองมาดูวิธีการดูรายละเอียดแนวลึก</span><span class="sxs-lookup"><span data-stu-id="a4e15-145">Let's take a look at how each of these works.</span></span>

### <a name="drill-down-on-row-headers"></a><span data-ttu-id="a4e15-146">การดูรายละเอียดแนวลึกที่ส่วนหัวของแถว</span><span class="sxs-lookup"><span data-stu-id="a4e15-146">Drill down on row headers</span></span>

<span data-ttu-id="a4e15-147">ในบานหน้าต่างการแสดงภาพเมื่อคุณเพิ่มหลายเขตข้อมูลให้กับส่วน **แถว** ของ **เขตข้อมูล** คุณจะสามารถดูรายละเอียดแนวลึกที่ระดับแถวของภาพเมทริกซ์ได้</span><span class="sxs-lookup"><span data-stu-id="a4e15-147">In the Visualizations pane, when you add multiple fields to the **Rows** section of the **Fields** well, you enable drill down on the rows of the matrix visual.</span></span> <span data-ttu-id="a4e15-148">ซึ่งจะคล้ายกับการสร้างลำดับชั้นซึ่งจะช่วยให้คุณสามารถดูรายละเอียดแนวลึก (และย้อนกลับ) ตามลำดับชั้นดังกล่าว และวิเคราะห์ข้อมูลในแต่ละระดับได้</span><span class="sxs-lookup"><span data-stu-id="a4e15-148">This is similar to creating a hierarchy, which then allows you to drill down (and then back up) through that hierarchy, and analyze the data at each level.</span></span>

<span data-ttu-id="a4e15-149">ในรูปภาพต่อไปนี้ส่วน **แถว** ประกอบด้วย *ระยะการขาย* และ *ขนาดโอกาส* ซึ่งสร้างการจัดกลุ่ม (หรือลำดับชั้น) ในแถวที่เราสามารถเจาะลึกเพื่อดูรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="a4e15-149">In the following image, the **Rows** section contains *Sales stage* and *Opportunity size*, creating a grouping (or hierarchy) in the rows that we can drill to see details.</span></span>

![บัตรตัวกรองแสดงแถวที่ถูกเลือก](media/desktop-matrix-visual/power-bi-rows-matrix.png)

<span data-ttu-id="a4e15-151">เมื่อวิชวลนี้มีการจัดกลุ่มที่สร้างขึ้นในส่วน **แถว** วิชวลจะแสดงไอคอน *ดูรายละเอียด* และ *ขยาย* ที่มุมบนซ้ายของวิชวล</span><span class="sxs-lookup"><span data-stu-id="a4e15-151">When the visual has grouping created in the **Rows** section, the visual itself displays the *drill* and *expand* icons in the top-left corner of the visual.</span></span>

![เมทริกซ์ที่มีตัวควบคุมการดูรายละเอียดให้เป็นไปตามที่ระบุไว้](media/desktop-matrix-visual/power-bi-matrix-drilldown.png)

<span data-ttu-id="a4e15-153">คล้ายกับการดูรายละเอียดและขยายดูข้อมูลในภาพอื่น ๆ การเลือกปุ่มเหล่านี้ช่วยให้เราสามารถดูรายละเอียดแนวลึก (หรือย้อนกลับ) ตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="a4e15-153">Similar to the drill and expand behavior in other visuals, selecting those buttons lets us drill down (or back up) through the hierarchy.</span></span> <span data-ttu-id="a4e15-154">ในกรณีนี้เราสามารถเจาะลึกตั้งแต่ *ขั้นตอนการขาย* จนถึง *ขนาดโอกาส* ดังที่แสดงในภาพต่อไปนี้โดยที่ไอคอน **เจาะลึกระดับหนึ่ง** (รูปแฉก ) ที่ถูกเลือกแล้ว</span><span class="sxs-lookup"><span data-stu-id="a4e15-154">In this case, we can drill down from *Sales stage* to *Opportunity size*, as shown in the following image, where the **drill down one level** icon (the pitchfork) has been selected.</span></span>

![เมทริกซ์ที่มีสัญลักษณ์รูปแฉกกำกับ](media/desktop-matrix-visual/power-bi-matrix-drill3.png)

<span data-ttu-id="a4e15-156">นอกจากการใช้ไอคอนเหล่านั้น คุณสามารถเลือกส่วนหัวของแถวใด ๆ และดูรายละเอียดแนวลึกโดยเลือกจากเมนูที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e15-156">In addition to using those icons, you can select any of those row headers and drill down by choosing from the menu that appears.</span></span>

![เมนูตัวเลือกสำหรับแถวในเมทริกซ์](media/desktop-matrix-visual/power-bi-matrix-menu.png)

<span data-ttu-id="a4e15-158">โปรดสังเกตว่า มีหลายตัวเลือกบนเมนูที่ปรากฏ ซึ่งสร้างผลลัพธ์ที่แตกต่างกัน:</span><span class="sxs-lookup"><span data-stu-id="a4e15-158">Notice there are a few options from the menu that appears, which generate different results:</span></span>

<span data-ttu-id="a4e15-159">เลือก **ดูรายละเอียดแนวลึก** ขยายเมทริกซ์สำหรับแถวระดับ *นั้น* *ยกเว้น* หัวแถวอื่น ๆ ทั้งหมดที่ไม่ใช้หัวแถวที่ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="a4e15-159">Selecting **Drill Down** expands the matrix for *that* row level, *excluding* all other row headings except the row header that was selected.</span></span> <span data-ttu-id="a4e15-160">ในรูปต่อไปนี้ **ข้อเสนอ** > **ที่เป็นรายละเอียดแนวลึก** จะถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="a4e15-160">In the following image, **Proposal** > **Drill Down** was selected.</span></span> <span data-ttu-id="a4e15-161">โปรดสังเกตว่า แถวอื่น ๆ ในระดับบนสุดจะไม่ปรากฏในเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="a4e15-161">Notice that other top-level rows no longer appear in the matrix.</span></span> <span data-ttu-id="a4e15-162">วิธีการดูรายละเอียดนี้เป็นคุณลักษณะที่มีประโยชน์ และกลายเป็นสิ่งที่น่าสนใจโดยเฉพาะอย่างยิ่งเมื่อเราไปยังส่วนการไฮไลต์แบบเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="a4e15-162">This way to drill is a useful feature, and becomes especially cool when we get to the cross-highlighting section.</span></span>

![เมทริกซ์เจาะลึกลงหนึ่งระดับ](media/desktop-matrix-visual/power-bi-drill-down-matrix.png)

<span data-ttu-id="a4e15-164">เลือกไอคอน **ดูรายละเอียดแบบเจาะลึก** เพื่อกลับไปที่มุมมองระดับบนสุดก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="a4e15-164">Select the **Drill-up** icon to get back to the previous top-level view.</span></span> <span data-ttu-id="a4e15-165">ถ้าคุณเลือก **ข้อเสนอ** > **แสดงระดับถัดไป** คุณจะได้รายการตามลำดับของรายการในระดับถัดไปทั้งหมด (ในกรณีนี้ คือเขตข้อมูล *ขนาดของโอกาส*) โดยไม่มีลำดับชั้นสูงกว่าของการจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="a4e15-165">If you then select **Proposal** > **Show Next Level**, you get an ascending listing of all the next-level items (in this case, the *Opportunity size* field), without the higher-level hierarchy categorization.</span></span>

![เมทริกซ์ที่ใช้แสดงระดับถัดไป](media/desktop-matrix-visual/power-bi-next-level-matrix.png)

<span data-ttu-id="a4e15-167">เลือกไอคอน **ดูรายละเอียดเลื่อนขึ้น** ที่มุมบนซ้ายเพื่อให้เมทริกซ์แสดงประเภทระดับบนสุดทั้งหมด แล้วเลือก **ข้อเสนอ** > **ขยายไปยังระดับถัดไป** เพื่อดูค่าทั้งหมดสำหรับทั้งสองระดับของลำดับชั้น - *ขั้นตอนการขาย* และ *ขนาดของโอกาส*</span><span class="sxs-lookup"><span data-stu-id="a4e15-167">Select the **Drill up** icon in the upper-left corner to have the matrix show all top-level categories, then select **Proposal** > **Expand to next level**, to see all the values for both levels of the hierarchy - *Sales stage* and *Opportunity size*.</span></span>

![เมทริกซ์ที่ใช้ขยายระดับถัดไป](media/desktop-matrix-visual/power-bi-matrix-expand-next.png)

<span data-ttu-id="a4e15-169">คุณยังสามารถใช้รายการเมนู **ขยาย** เพื่อควบคุมการแสดงเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="a4e15-169">You can also use the **Expand** menu item to control the display further.</span></span>  <span data-ttu-id="a4e15-170">ตัวอย่าง เลือก **ข้อเสนอ** > **การขยาย** > **การเลือก**</span><span class="sxs-lookup"><span data-stu-id="a4e15-170">For example, select  **Proposal** > **Expand** > **Selection**.</span></span> <span data-ttu-id="a4e15-171">Power BI แสดงผลรวมหนึ่งแถวสำหรับแต่ละ *ขั้นตอนการขาย* และตัวเลือก *ขนาดของโอกาส* สำหรับ *ข้อเสนอ* ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a4e15-171">Power BI displays one total row for each *Sales stage* and all the *Opportunity size* options for *Proposal*.</span></span>

![เมทริกซ์หลังจากการขยายที่นำไปใช้กับข้อเสนอ](media/desktop-matrix-visual/power-bi-matrix-expand.png)

### <a name="drill-down-on-column-headers"></a><span data-ttu-id="a4e15-173">ดูรายละเอียดแนวลึกที่ส่วนหัวของคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="a4e15-173">Drill down on column headers</span></span>
<span data-ttu-id="a4e15-174">คล้ายกับความสามารถในการเจาะดูรายละเอียดแนวลึกที่ระดับแถว คุณสามารถยังเจาะรายละเอียดแนวลึกที่ระดับคอลัมน์ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="a4e15-174">Similar to the ability to drill down on rows, you can also drill down on columns.</span></span> <span data-ttu-id="a4e15-175">ในรูปต่อไปนี้ มีสองเขตข้อมูลใน **คอลัมน์** ที่สร้างเป็นลำดับชั้นแบบเดียวกับที่เราใช้กับแถว ก่อนหน้านี้ในบทความ</span><span class="sxs-lookup"><span data-stu-id="a4e15-175">In the following image, there are two fields in the **Columns** field well, creating a hierarchy similar to what we used for the rows earlier in this article.</span></span> <span data-ttu-id="a4e15-176">ในเขตข้อมูล **คอลัมน์** เรามี *ภูมิภาค* และ *เซกเมนต์*</span><span class="sxs-lookup"><span data-stu-id="a4e15-176">In the **Columns** field well, we have *Region* and *Segment*.</span></span> <span data-ttu-id="a4e15-177">ทันทีที่เขตข้อมูลที่สองถูกเพิ่มไปยัง **คอลัมน์** เมนูดรอปดาวน์ใหม่จะแสดงบนวิชวล ขณะนี้กำลังแสดงข้อมูล **แถว** ให้ได้ชม</span><span class="sxs-lookup"><span data-stu-id="a4e15-177">As soon as the second field was added to **Columns**, a new dropdown menu displayed on the visual, it currently shows **Rows**.</span></span>

![เมทริกซ์หลังจากเพิ่มค่าคอลัมน์ที่สอง](media/desktop-matrix-visual/power-bi-matrix-row.png)

<span data-ttu-id="a4e15-179">เมื่อต้องดูรายละเอียดแนวลึกบนคอลัมน์ เลือก **คอลัมน์** จากการเมนู *ดูรายละเอียดเลื่อนขึ้น* ที่อยู่มุมบนซ้ายของเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="a4e15-179">To drill down on columns, select **Columns** from the *Drill on* menu that can be found in the upper left corner of the matrix.</span></span> <span data-ttu-id="a4e15-180">เลือกภูมิภาค *ตะวันออก* และเลือก **รายละเอียดแนวลึก**</span><span class="sxs-lookup"><span data-stu-id="a4e15-180">Select the *East* region and choose **Drill Down**.</span></span>

![เมนูรายละเอียดลึกสำหรับคอลัมน์](media/desktop-matrix-visual/power-bi-matrix-column.png)

<span data-ttu-id="a4e15-182">เมื่อคุณเลือก **ดูรายละเอียดแนวลึก** ลำดับชั้นคอลัมน์ถัดไปของ *ภูมิภาค>ตะวันออก* จะแสดง ซึ่งในกรณีนี้คือ *จำนวนโอกาส*</span><span class="sxs-lookup"><span data-stu-id="a4e15-182">When you select **Drill Down**, the next level of the column hierarchy for *Region > East* displays, which in this case is *Opportunity count*.</span></span> <span data-ttu-id="a4e15-183">ภูมิภาคอื่น ๆ ถูกซ่อนไว้</span><span class="sxs-lookup"><span data-stu-id="a4e15-183">The other region is hidden.</span></span>

![เมทริกซ์ มีคอลัมน์รายละเอียดแนวลึกลงหนึ่งระดับ](media/desktop-matrix-visual/power-bi-matrix-column-drill.png)

<span data-ttu-id="a4e15-185">ส่วนที่เหลือของหน่วยข้อมูลของเมนูใช้งานกับคอลัมน์ในลักษณะเดียวกับที่ใช้กับแถว (ดูส่วนก่อนหน้า **ดูรายละเอียดแนวลึกที่ส่วนหัวของแถว**)</span><span class="sxs-lookup"><span data-stu-id="a4e15-185">The rest of the menu items work on columns in the same way they do for rows (see the previous section, **Drill down on row headers**).</span></span> <span data-ttu-id="a4e15-186">คุณสามารถ **แสดงระดับถัดไป**, **ขยายไประดับถัดไป** ด้วยคอลัมน์ของคุณเหมือนกับที่คุณสามารถทำได้กับแถวได้</span><span class="sxs-lookup"><span data-stu-id="a4e15-186">You can **Show Next Level** and **Expand to next level** with columns just as you can with rows.</span></span>

> [!NOTE]
> <span data-ttu-id="a4e15-187">ไอคอนดูรายละเอียดแนวลึก และดูข้อมูลสรุป ที่มุมบนซ้ายของวิชวลเมทริกซ์ ใช้กับแถวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a4e15-187">The drill-down and drill-up icons in the upper-left of the matrix visual only apply to rows.</span></span> <span data-ttu-id="a4e15-188">เมื่อต้องดูรายละเอียดแนวลึกที่ระดับคอลัมน์ คุณต้องใช้เมนูคลิกขวา</span><span class="sxs-lookup"><span data-stu-id="a4e15-188">In order to drill down on columns, you must use the right-click menu.</span></span>

## <a name="stepped-layout-with-matrix-visuals"></a><span data-ttu-id="a4e15-189">รูปแบบขั้น กับวิชวลเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="a4e15-189">Stepped layout with matrix visuals</span></span>

<span data-ttu-id="a4e15-190">วิชวลเมทริกซ์ทำการเยื้องประเภทย่อยในลำดับชั้นใต้แต่ละประเภทใหญ่ เรียกว่ารูปแบบขั้น</span><span class="sxs-lookup"><span data-stu-id="a4e15-190">The matrix visual automatically indents subcategories in a hierarchy beneath each parent, called a stepped layout.</span></span>

<span data-ttu-id="a4e15-191">ในวิชวลเมทริกซ์ เวอร์ชันเดิมประเภทย่อยจะถูกแสดงในคอลัมน์ต่างหาก และใช้พื้นที่วิชวลมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e15-191">In the original version of the matrix visual, subcategories were shown in an entirely different column, taking up much more space in the visual.</span></span> <span data-ttu-id="a4e15-192">รูปต่อไปนี้แสดงตารางในวิชวลเมทริกซ์ต้นฉบับ โปรดสังเกตว่าประเภทย่อยอยู่ในคอลัมน์แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="a4e15-192">The following image shows the table in original matrix visual; notice the subcategories in a separate column.</span></span>

![สกรีนช็อตของวิชวลเมทริกซ์เก่าแสดงประเภทย่อยอยู่ในคอลัมน์แยก](media/desktop-matrix-visual/matrix-visual_14.png)

<span data-ttu-id="a4e15-194">ในรูปต่อไปนี้ คุณจะเห็นวิชวลเมทริกซ์ที่แสดงในรูปแบบขั้น</span><span class="sxs-lookup"><span data-stu-id="a4e15-194">In the following image, you see a matrix visual, with stepped layout in action.</span></span> <span data-ttu-id="a4e15-195">โปรดสังเกตว่า ประเภท *คอมพิวเตอร์* มีประเภทย่อย (อุปกรณ์คอมพิวเตอร์ เดสก์ท็อป แล็ปท็อป จอ ฯลฯ) แสดงเยื้องเล็กน้อย ให้วิชวลดูสะอาดตา และดูแน่นขึ้น</span><span class="sxs-lookup"><span data-stu-id="a4e15-195">Notice the category *Computers* has its subcategories (Computers Accessories, Desktops, Laptops, Monitors, and so on) slightly indented, providing a cleaner and much more condensed visual.</span></span>

![รูปแบบข้อมูลเมทริกซ์ในปัจจุบัน](media/desktop-matrix-visual/matrix-visual_13.png)

<span data-ttu-id="a4e15-197">คุณสามารถปรับเปลี่ยนการตั้งค่ารูปแบบขั้นได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="a4e15-197">You can easily adjust the stepped layout settings.</span></span> <span data-ttu-id="a4e15-198">เมื่อเลือกวิชวลเมทริกซ์ ในส่วน **รูปแบบ** (ไอคอนลูกกลิ้งสี) ของบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล** ขยายส่วนส่วนหัวของแถว</span><span class="sxs-lookup"><span data-stu-id="a4e15-198">With the matrix visual selected, in the **Format** section (the paint roller icon) of the **Visualizations** pane, expand the row headers section.</span></span> <span data-ttu-id="a4e15-199">คุณมีสองตัวเลือก: การสลับรูปแบบขั้น (ให้เปิดหรือปิด) และการเยื้องเค้าโครงแบบขั้น (ระบุระยะของการเยื้องเป็นพิกเซล)</span><span class="sxs-lookup"><span data-stu-id="a4e15-199">You have two options: the stepped layout toggle (which turns it on or off), and the stepped layout indentation (specifies the indentation amount, in pixels).</span></span>

![การ์ดส่วนหัวของแถวที่แสดงตัวควบคุมขั้นตอนรูปแบบขั้น](media/desktop-matrix-visual/power-bi-stepped-matrix.png)

<span data-ttu-id="a4e15-201">ถ้าคุณปิดรูปแบบขั้น Power BI จะแสดงประเภทย่อยในอีกคอลัมน์ แทนที่จะเยื้องภายใต้ประเภทหลัก</span><span class="sxs-lookup"><span data-stu-id="a4e15-201">If you turn off stepped layout, Power BI shows the subcategories in another column rather than indented beneath the parent category.</span></span>

## <a name="subtotals-and-grand-totals-with-matrix-visuals"></a><span data-ttu-id="a4e15-202">ผลรวมย่อยและทั้งหมด ด้วยวิชวลเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="a4e15-202">Subtotals and grand totals with matrix visuals</span></span>

<span data-ttu-id="a4e15-203">คุณสามารถเปิดปิดผลรวมย่อย ในวิชวลเมทริกซ์ สำหรับทั้งแถวและคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="a4e15-203">You can turn subtotals on or off in matrix visuals, for both rows and columns.</span></span> <span data-ttu-id="a4e15-204">ในรูปต่อไปนี้ คุณเห็นการตั้งค่าผลรวมย่อยของแถว เป็น **เปิด** และตั้งค่าให้แสดงผลที่ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="a4e15-204">In the following image, you can see that the row subtotals are set to **On** and set to display at the bottom.</span></span>

![เมทริกซ์แสดงผลรวมและผลรวมย่อย](media/desktop-matrix-visual/power-bi-subtotals.png)

<span data-ttu-id="a4e15-206">เมื่อคุณเปิด **ผลรวมย่อย** และเพิ่มป้ายกำกับ Power BI ยังสามารถเพิ่มแถว และป้ายกำกับเดียวกัน สำหรับมูลค่าผลรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a4e15-206">When you turn on **Subtotals** and add a label, Power BI also adds a row, and the same label, for the grand total value.</span></span> <span data-ttu-id="a4e15-207">เมื่อต้องการจัดรูปแบบผลรวมทั้งหมดของคุณ ให้เลือกตัวเลือกรูปแบบสำหรับ **ผลรวมทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="a4e15-207">To format your grand total, select the format option for **Grand total**.</span></span> 

![เมทริกซ์ที่แสดงการ์ดผลรวมทั้งหมด](media/desktop-matrix-visual/power-bi-grand-total.png)

<span data-ttu-id="a4e15-209">หากคุณต้องการปิดผลรวมย่อยและผลรวมทั้งหมด ในส่วนจัดรูปแบบของบานหน้าต่างการจัดรูปแบบการแสดงข้อมูล ขยายการ์ด **ผลรวมย่อย**</span><span class="sxs-lookup"><span data-stu-id="a4e15-209">If you want to turn subtotals and grand total off, in the format section of the visualizations pane, expand the **Subtotals** card.</span></span> <span data-ttu-id="a4e15-210">เปลี่ยนแถบเลื่อนแถวผลรวมย่อยเป็น **ปิด**</span><span class="sxs-lookup"><span data-stu-id="a4e15-210">Turn the row subtotals slider to **Off**.</span></span> <span data-ttu-id="a4e15-211">เมื่อคุณทำเช่นนั้น จะไม่มีแสดงผลรวมย่อย</span><span class="sxs-lookup"><span data-stu-id="a4e15-211">When you do so, the subtotals aren't shown.</span></span>

![ปิดการใช้งานเมทริกซ์กับผลรวมย่อย](media/desktop-matrix-visual/power-bi-no-subtotals.png)

<span data-ttu-id="a4e15-213">กระบวนการเดียวกัน ใช้ได้กับผลรวมย่อยของคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="a4e15-213">The same process applies for column subtotals.</span></span>

## <a name="add-conditional-icons"></a><span data-ttu-id="a4e15-214">เพิ่มไอคอนที่แสดงเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="a4e15-214">Add conditional icons</span></span>
<span data-ttu-id="a4e15-215">เพิ่มการแสดงภาพลงในตารางหรือเมทริกซ์ของคุณด้วย *ไอคอนแบบมีเงื่อนไข*</span><span class="sxs-lookup"><span data-stu-id="a4e15-215">Add visual cues to your table or matrix with *conditional icons*.</span></span> 

<span data-ttu-id="a4e15-216">ในส่วนรูปแบบของบานหน้าต่างการแสดงภาพ ให้ขยายการ์ด **การจัดรูปแบบตามเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="a4e15-216">In the format section of the Visualizations pane, expand the **Conditional formatting** card.</span></span> <span data-ttu-id="a4e15-217">เลื่อนแถบเลื่อน **ไอคอน** ไปยัง **เปิด** และเลือก **ตัวควบคุมขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="a4e15-217">Turn the **Icons** slider to **On** and select **Advanced controls**.</span></span>

![เมทริกซ์ที่มีหน้าจอไอคอนที่แสดง](media/desktop-matrix-visual/power-bi-icons.png)

<span data-ttu-id="a4e15-219">ปรับเงื่อนไข ไอคอนและสีสำหรับเมทริกซ์ของคุณและเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a4e15-219">Adjust the conditions, icons, and colors for your matrix and select **OK**.</span></span> <span data-ttu-id="a4e15-220">ในตัวอย่างนี้ เราใช้ธงสีแดงสำหรับรายการที่มีมูลค่าน้อย วงกลมสีม่วงสำหรับรายการที่มีมูลค่าสูง และสามเหลี่ยมสีเหลืองสำหรับรายการอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="a4e15-220">In this example, we used a red flag for low values, purple circle for high values, and yellow triangle for everything in between.</span></span> 

![เมทริกซ์ที่มีไอคอนกำลังแสดงผลยู่](media/desktop-matrix-visual/power-bi-icons-applied.png)

## <a name="cross-highlighting-with-matrix-visuals"></a><span data-ttu-id="a4e15-222">การไฮไลต์เชื่อมโยง ด้วยวิชวลเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="a4e15-222">Cross-highlighting with matrix visuals</span></span>

<span data-ttu-id="a4e15-223">ด้วยวิชวลเมทริกซ์ คุณสามารถเลือกองค์ประกอบใด ๆ ในเมทริกซ์ให้เป็นพื้นฐานสำหรับการไฮไลต์เชื่อมโยงได้</span><span class="sxs-lookup"><span data-stu-id="a4e15-223">With the matrix visual, you can select any elements in the matrix as the basis for cross-highlighting.</span></span> <span data-ttu-id="a4e15-224">เลือกคอลัมน์ในเมทริกซ์และคอลัมน์นั้นจะถูกไฮไลต์โดย Power BI เช่นเดียวกับวิชวลอื่น ๆ ในหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="a4e15-224">Select a column in a matrix and Power BI highlights the column, as does any other visuals on the report page.</span></span> <span data-ttu-id="a4e15-225">ไฮไลต์เชื่อมโยงชนิดนี้เป็นคุณลักษณะทั่วไปของภาพและการเลือกจุดข้อมูลอื่น ๆ ดังนั้นวิชวลเมทริกซ์จะให้ฟังก์ชันเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="a4e15-225">This type of cross-highlighting has been a common feature of other visuals and data point selections, so now the matrix visual offers the same function.</span></span>

<span data-ttu-id="a4e15-226">นอกจากนี้ การใช้ Ctrl+คลิก ยังใช้ได้กับการไฮไลต์เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="a4e15-226">In addition, using Ctrl+Click also works for cross-highlighting.</span></span> <span data-ttu-id="a4e15-227">ตัวอย่างเช่น ในรูปต่อไปนี้ คอลเลกชันของประเภทย่อยถูกเลือกในวิชวลเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="a4e15-227">For example, in the following image a collection of subcategories were selected from the matrix visual.</span></span> <span data-ttu-id="a4e15-228">สังเกตได้ว่า รายการที่ไม่ได้เลือกในวิชวลจะเป็นสีเทา และวิชวลอื่น ๆ บนหน้าสะท้อนการเลือกในวิชวลเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="a4e15-228">Notice how items that weren't selected from the visual are grayed out, and how the other visuals on the page reflect the selections made in the matrix visual.</span></span>

![สกรีนช็อตของวิชวลเมทริกซ์พร้อมกับวิชวลอื่น ๆ กำลังแสดงฟังก์ชัน Ctrl + คลิกสำหรับไฮไลต์เชื่อมโยงแบบข้าม](media/desktop-matrix-visual/matrix-visual_16.png)

## <a name="copying-values-from-power-bi-for-use-in-other-applications"></a><span data-ttu-id="a4e15-230">คัดลอกค่าจาก Power BI เพื่อนำไปใช้ในแอปพลิเคชันอื่น</span><span class="sxs-lookup"><span data-stu-id="a4e15-230">Copying values from Power BI for use in other applications</span></span>

<span data-ttu-id="a4e15-231">ตารางหรือเมทริกซ์ของคุณอาจมีเนื้อหาที่คุณต้องการใช้ในแอปพลิเคชันอื่น ๆ: Dynamics CRM, Excel และรายงาน Power BI อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="a4e15-231">Your matrix or table may have content that you'd like to use in other applications: Dynamics CRM, Excel, and other Power BI reports.</span></span> <span data-ttu-id="a4e15-232">คุณสามารถคัดลอกเซลล์เดียวหรือหลายเซลล์ลงบนคลิปบอร์ดได้ด้วยการคลิกขวาที่ Power BI</span><span class="sxs-lookup"><span data-stu-id="a4e15-232">With the Power BI right-click, you can copy a single cell or a selection of cells onto your clipboard.</span></span> <span data-ttu-id="a4e15-233">จากนั้นวางลงในแอปพลิเคชันอื่น</span><span class="sxs-lookup"><span data-stu-id="a4e15-233">Then, paste them into the other application.</span></span>


* <span data-ttu-id="a4e15-234">เมื่อต้องการคัดลอกเซลล์เดียว ให้เลือกเซลล์นั้น คลิกขวา แล้วเลือก **คัดลอกค่า**</span><span class="sxs-lookup"><span data-stu-id="a4e15-234">To copy the value of a single cell, select the cell,  right-click, and choose **Copy value**.</span></span> <span data-ttu-id="a4e15-235">ในตอนนี้คุณก็สามารถวางค่าที่คัดลอกลงในแอปพลิเคชันอื่นได้ โดยจะได้ค่าเซลล์ที่ไม่ได้จัดรูปแบบในคลิปบอร์ด</span><span class="sxs-lookup"><span data-stu-id="a4e15-235">With the unformatted cell value on your clipboard, you can now paste it into another application.</span></span>

    ![สกรีนช็อตของการเรียกเมทริกซ์วิชวลที่มีลูกศรชี้ไปยังค่าและเมนูขยายด้วยค่าสำเนาและตัวเลือกการเลือกคัดลอกเมนูคลิกขวาออกมา](media/desktop-matrix-visual/power-bi-cell-copy.png)



* <span data-ttu-id="a4e15-237">เมื่อต้องการคัดลอกหลายเซลล์ ให้เลือกช่วงเซลล์ หรือใช้ปุ่ม CTRL เพื่อเลือกเซลล์อย่างน้อยหนึ่งเซลล์</span><span class="sxs-lookup"><span data-stu-id="a4e15-237">To copy more than a single cell, select a range of cells or use CTRL to select one or more cells.</span></span> 

    ![สกรีนช็อตของการเรียกเมทริกซ์วิชวลที่มีลูกศรชี้ไปยังค่าที่เรียกออกมา 3 ค่าไปยังเมนูขยายด้วยค่าสำเนาและตัวเลือกการเลือกคัดลอกเมนูคลิกขวาออกมา](media/desktop-matrix-visual/power-bi-copy.png)

* <span data-ttu-id="a4e15-239">ส่วนคัดลอกจะมีส่วนหัวของคอลัมน์และแถว</span><span class="sxs-lookup"><span data-stu-id="a4e15-239">The copy will include the column and row headers.</span></span>

    ![สกรีนช็อตแสดง Excel แถวและคอลัมน์ที่มีค่าที่วางลงไป](media/desktop-matrix-visual/power-bi-copy-selection.png)

* <span data-ttu-id="a4e15-241">ในการทำสำเนาของวิชวลที่มีเฉพาะเซลล์ที่คุณเลือกเท่านั้น ให้เลือกอย่างน้อยหนึ่งเซลล์โดยใช้ CTRL, คลิกขวา และเลือก **คัดลอกวิชวล**</span><span class="sxs-lookup"><span data-stu-id="a4e15-241">To make a copy  of the visual itself containing only your selected cells, select one or more cells using CTRL, right-click, and choose **Copy visual**</span></span>

    ![สกรีนช็อตที่แสดงตัวเลือกวิชวลสำเนา](media/desktop-matrix-visual/power-bi-copy-visual.png)

* <span data-ttu-id="a4e15-243">สำเนาจะเป็นการจัดรูปแบบการแสดงข้อมูลเมทริกซ์อื่น แต่มีเพียงข้อมูลที่เป็นสำเนาของคุณเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a4e15-243">The copy will be another matrix visualization, but contain only your copied data.</span></span>

    ![สกรีนช็อตที่แสดงตัวอย่างวิชวลสำเนา](media/desktop-matrix-visual/power-bi-copy-visual-example.png)

## <a name="setting-a-matrix-value-as-a-custom-url"></a><span data-ttu-id="a4e15-245">ตั้งค่าเมทริกซ์เป็น URL ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="a4e15-245">Setting a matrix value as a custom URL</span></span>

<span data-ttu-id="a4e15-246">หากคุณมีคอลัมน์หรือหน่วยวัดที่ประกอบด้วย URL เว็บไซต์ คุณสามารถใช้การจัดรูปแบบตามเงื่อนไขเพื่อใช้ URL เหล่านั้นกับเขตข้อมูลเป็นลิงก์ที่ใช้งานอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="a4e15-246">If you have a column or measure that contains website URLs, you can use conditional formatting to apply those URLs to fields as active links.</span></span> <span data-ttu-id="a4e15-247">คุณจะพบตัวเลือกนี้ภายใต้การ์ด **การจัดรูปแบบตามเงื่อนไข** ในแถบการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="a4e15-247">You’ll find this option under the **Conditional formatting** card in the formatting pane.</span></span>

![สกรีนช็อตแสดงไอคอนการจัดรูปแบบที่เชื่อมโยงกับ URL ของเว็บ](media/desktop-matrix-visual/power-bi-web-url.png)

<span data-ttu-id="a4e15-249">เปิด  **URL ของเว็บ** และเลือกเขตข้อมูลที่จะใช้เป็น URL สำหรับคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="a4e15-249">Turn **Web URL** On, and select a field to use as the URL for the column.</span></span> <span data-ttu-id="a4e15-250">เมื่อนำไปใช้แล้ว ค่าในเขตข้อมูลนั้น (คอลัมน์) จะกลายเป็นลิงก์ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="a4e15-250">Once applied, the values in that field (column) become active links.</span></span> <span data-ttu-id="a4e15-251">เลื่อนวางเม้าส์เพื่อดูลิงก์และเลือกเพื่อข้ามไปยังหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="a4e15-251">Hover to see the link, and select to jump to that page.</span></span> 

<span data-ttu-id="a4e15-252">สำหรับข้อมูลเพิ่มเติม ดูที่ [การจัดรูปแบบตารางแบบมีเงื่อนไข](../create-reports/desktop-conditional-table-formatting.md)</span><span class="sxs-lookup"><span data-stu-id="a4e15-252">For more information, see [Conditional table formatting](../create-reports/desktop-conditional-table-formatting.md)</span></span>

## <a name="shading-and-font-colors-with-matrix-visuals"></a><span data-ttu-id="a4e15-253">การแรเงาและสีแบบอักษร กับวิชวลเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="a4e15-253">Shading and font colors with matrix visuals</span></span>
<span data-ttu-id="a4e15-254">ด้วยวิชวลเมทริกซ์ คุณสามารถใช้การจัดรูปแบบตามเงื่อนไข (สี แรเงา และแถบข้อมูล) ในพื้นหลังของเซลล์ภายในเมทริกซ์ และคุณสามารถใช้การจัดรูปแบบตามเงื่อนไขกับข้อความและค่า</span><span class="sxs-lookup"><span data-stu-id="a4e15-254">With the matrix visual, you can apply conditional formatting (colors and shading and data bars) to the background of cells within the matrix, and you can apply conditional formatting to the text and values themselves.</span></span>

<span data-ttu-id="a4e15-255">ในการใช้การจัดรูปแบบตามเงื่อนไข เลือกเมทริกซ์วิชวลและเปิดใน **รูปแบบ** บานหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="a4e15-255">To apply conditional formatting, select the matrix visual and open the **Format** pane.</span></span> <span data-ttu-id="a4e15-256">ขยายการ์ด **การจัดรูปแบบตามเงื่อนไข** และสำหรับ **สีพื้นหลัง** **สีฟอนต์** หรือ **แถบข้อมูล** เลื่อนแถบเลื่อนเพื่อ **เปิด**</span><span class="sxs-lookup"><span data-stu-id="a4e15-256">Expand the **Conditional formatting** card and for **Background color**, **Font color**, or **Data bars**, turn the slider to **On**.</span></span> <span data-ttu-id="a4e15-257">การเปิดใช้งานตัวเลือกตัวใดตัวหนึ่งจะแสดงลิงก์ของ *ตัวควบคุมขั้นสูง* ที่ให้คุณกำหนดสีและค่าสำหรับการจัดรูปแบบสี</span><span class="sxs-lookup"><span data-stu-id="a4e15-257">Turning on one of these options displays a link for *Advanced controls*, which lets you customize the colors and values for the color formatting.</span></span>
  
  ![รูปแบบบานหน้าต่างแสดงตัวควบคุมแถบข้อมูล](media/desktop-matrix-visual/power-bi-matrix-data-bars.png)

<span data-ttu-id="a4e15-259">การเลือก *การควบคุมขั้นสูง* จะแสดงกล่องโต้ตอบที่สามารถให้คุณทำการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="a4e15-259">Select *Advanced controls* to display a dialog, which lets you make adjustments.</span></span> <span data-ttu-id="a4e15-260">ตัวอย่างนี้แสดงกล่องโต้ตอบสำหรับ **แถบข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="a4e15-260">This example shows the dialog for **Data bars**.</span></span>

![บานหน้าต่างแถบข้อมูล](media/desktop-matrix-visual/power-bi-data-bars.png)

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="a4e15-262">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="a4e15-262">Considerations and troubleshooting</span></span>

* <span data-ttu-id="a4e15-263">หากข้อมูลข้อความในเซลล์หรือส่วนหัวของตารางของคุณมีอักขระบรรทัดใหม่ อักขระเหล่านั้นจะถูกละเว้นถ้าคุณสลับตัวเลือก 'การตัดคำ' ในการ์ดบานหน้าต่างการจัดรูปแบบที่เกี่ยวข้องขององค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="a4e15-263">If the text data in your matrix's cells or headers contain new line characters, those characters will be ignored unless you toggle on the 'Word Wrap' option in the element's associated formatting pane card.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="a4e15-264">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a4e15-264">Next steps</span></span>

[<span data-ttu-id="a4e15-265">วิชวล Power Apps สำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="a4e15-265">Power Apps visual for Power BI</span></span>](power-bi-visualization-powerapp.md)

[<span data-ttu-id="a4e15-266">ชนิดการแสดงภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="a4e15-266">Visualization types in Power BI</span></span>](power-bi-visualization-types-for-reports-and-q-and-a.md)


