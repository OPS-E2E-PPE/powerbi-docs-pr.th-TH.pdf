---
title: ชนิดของข้อมูลเชิงลึกด่วนที่ได้รับการสนับสนุนโดย Power BI
description: ข้อมูลเชิงลึกด่วน และดูข้อมูลเชิงลึก ด้วย Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-explore
ms.topic: conceptual
ms.date: 10/12/2020
LocalizationGroup: Dashboards
ms.openlocfilehash: a5a3029a3afe3d48981338934090ad6b9719d6bb
ms.sourcegitcommit: 513c4b884a58e1da2680579339c24c46091bbfb2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/04/2020
ms.locfileid: "96613450"
---
# <a name="types-of-insights-supported-by-power-bi"></a><span data-ttu-id="03881-103">ชนิดของข้อมูลเชิงลึกด่วนที่ได้รับการสนับสนุนโดย Power BI</span><span class="sxs-lookup"><span data-stu-id="03881-103">Types of insights supported by Power BI</span></span>

[!INCLUDE[consumer-appliesto-yyny](../includes/consumer-appliesto-yyny.md)]

<span data-ttu-id="03881-104">คุณสามารถขอให้ Power BI ค้นหาข้อมูลของคุณ และค้นหาแนวโน้มและรูปแบบที่น่าสนใจได้</span><span class="sxs-lookup"><span data-stu-id="03881-104">You can ask Power BI to look through your data and find interesting trends and patterns.</span></span> <span data-ttu-id="03881-105">แนวโน้มและรูปแบบเหล่านี้จะแสดงในรูปแบบของวิชวลที่เรียกว่า *ข้อมูลเชิงลึก*</span><span class="sxs-lookup"><span data-stu-id="03881-105">These trends and patterns are presented in the form of visuals that are called *Insights*.</span></span> 

<span data-ttu-id="03881-106">หากต้องการเรียนรู้วิธีการใช้ข้อมูลเชิงลึก โปรดดู [Power BI Insights](end-user-insights.md)</span><span class="sxs-lookup"><span data-stu-id="03881-106">To learn how to use Insights, see [Power BI Insights](end-user-insights.md)</span></span>

![ชุดของข้อมูลเชิงลึก](media/end-user-insight-types/power-bi-insight-line.png)

## <a name="how-does-insights-work"></a><span data-ttu-id="03881-108">ข้อมูลเชิงลึกทำงานอย่างไร</span><span class="sxs-lookup"><span data-stu-id="03881-108">How does Insights work?</span></span>
<span data-ttu-id="03881-109">Power BI จะค้นหาชุดข้อมูลย่อยที่แตกต่างกันของคุณได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="03881-109">Power BI quickly searches different subsets of your dataset.</span></span> <span data-ttu-id="03881-110">ในขณะที่ค้นหา Power BI จะใช้ชุดของอัลกอริทึมที่มีความซับซ้อนเพื่อค้นหาข้อมูลเชิงลึกที่น่าสนใจ</span><span class="sxs-lookup"><span data-stu-id="03881-110">As it searches, Power BI applies a set of sophisticated algorithms to discover potentially interesting insights.</span></span> <span data-ttu-id="03881-111">*ผู้ใช้งาน Power BI แบบธุรกิจ* สามารถเรียกใช้ข้อมูลเชิงลึกบนไทล์แดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="03881-111">Power BI *business users* can run Insights on dashboard tiles.</span></span>

## <a name="some-terminology"></a><span data-ttu-id="03881-112">คำศัพท์บางคำ</span><span class="sxs-lookup"><span data-stu-id="03881-112">Some terminology</span></span>
<span data-ttu-id="03881-113">Power BI ใช้อัลกอริทึมเชิงสถิติเพื่อเปิดเผยข้อมูลเชิงลึก</span><span class="sxs-lookup"><span data-stu-id="03881-113">Power BI uses statistical algorithms to uncover  Insights.</span></span> <span data-ttu-id="03881-114">อัลกอริทึมอยู่ในรายการและอธิบายไว้ในส่วนถัดไปของบทความนี้</span><span class="sxs-lookup"><span data-stu-id="03881-114">The algorithms are listed and described in the next section of this article.</span></span> <span data-ttu-id="03881-115">ก่อนที่เราจะไปยังอัลกอริทึม ต่อไปนี้เป็นข้อกำหนดสำหรับคำศัพท์บางคำที่อาจไม่คุ้นเคย</span><span class="sxs-lookup"><span data-stu-id="03881-115">Before we get to the algorithms, here are definitions for some terms that may be unfamiliar.</span></span> 

* <span data-ttu-id="03881-116">**หน่วยวัด** - หน่วยวัดคือเขตข้อมูลเชิงปริมาณ (ตัวเลข) ที่สามารถใช้ในการคำนวณได้</span><span class="sxs-lookup"><span data-stu-id="03881-116">**Measure** - a measure is a quantitative (numeric) field that can be used to do calculations.</span></span> <span data-ttu-id="03881-117">การคำนวณทั่วไปคือ ผลรวม ค่าเฉลี่ย และต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="03881-117">Common calculations are sum, average, and minimum.</span></span> <span data-ttu-id="03881-118">ตัวอย่างเช่น หากบริษัทของเราผลิตและขายสเก็ตบอร์ด หน่วยวัดของเราอาจเป็นจำนวนสเก็ตบอร์ดที่ขายและกำไรเฉลี่ยต่อปี</span><span class="sxs-lookup"><span data-stu-id="03881-118">For example, if our company makes and sells skateboards, our measures might be number of skateboards sold and average profit per year.</span></span>  
* <span data-ttu-id="03881-119">**มิติ** - มิติคือข้อมูลจัดกลุ่ม (ข้อความ)</span><span class="sxs-lookup"><span data-stu-id="03881-119">**Dimension** - dimensions are categorical (text) data.</span></span> <span data-ttu-id="03881-120">มิติจะอธิบายบุคคล วัตถุ รายการ ผลิตภัณฑ์ สถานที่ และเวลา</span><span class="sxs-lookup"><span data-stu-id="03881-120">A dimension describes a person, object, item, products, place, and time.</span></span> <span data-ttu-id="03881-121">ในชุดข้อมูล มิติเป็นวิธีการจัดกลุ่ม *หน่วยวัด* เป็นหมวดหมู่ที่มีประโยชน์</span><span class="sxs-lookup"><span data-stu-id="03881-121">In a a dataset, dimensions are a way to group *measures* into useful categories.</span></span> <span data-ttu-id="03881-122">สำหรับบริษัทสเก็ตบอร์ดของเรา บางมิติอาจรวมถึงการดูยอดขาย (หน่วยวัด) ตามแบบจำลอง สี ประเทศ หรือแคมเปญการตลาด</span><span class="sxs-lookup"><span data-stu-id="03881-122">For our skateboard company, some dimensions might include looking at sales (a measure) by model, color, country, or marketing campaign.</span></span>   
* <span data-ttu-id="03881-123">**สหสัมพันธ์** - สหสัมพันธ์บอกให้เราทราบว่าพฤติกรรมของสิ่งต่างๆ มีความเกี่ยวข้องกันอย่างไร</span><span class="sxs-lookup"><span data-stu-id="03881-123">**Correlation** - a correlation tells us how the behavior of things are related.</span></span>  <span data-ttu-id="03881-124">ถ้ารูปแบบของการเพิ่มขึ้นและลดลงคล้ายกันแล้ว พวกเขาจะมีความสัมพันธ์เชิงบวก</span><span class="sxs-lookup"><span data-stu-id="03881-124">If their patterns of increase and decrease are similar, then they are positively correlated.</span></span> <span data-ttu-id="03881-125">และถ้ารูปแบบของพวกเขาตรงกันข้าม พวกเขาจะมีความสัมพันธ์เชิงลบ</span><span class="sxs-lookup"><span data-stu-id="03881-125">And if their patterns are opposite, then they are negatively correlated.</span></span> <span data-ttu-id="03881-126">ตัวอย่างเช่น ถ้ายอดขายของสเก็ตบอร์ดสีแดงของเราเพิ่มขึ้นแต่ละครั้งที่เราดำเนินแคมเปญการตลาดทางโทรทัศน์ หมายความว่ายอดขายของสเก็ตบอร์ดสีแดงและแคมเปญทางโทรทัศน์มีความสัมพันธ์เชิงบวกกัน</span><span class="sxs-lookup"><span data-stu-id="03881-126">For example, if sales of our red skateboard increase each time we run a tv marketing campaign, then sales of the red skateboard and the tv campaign are positively correlated.</span></span>
* <span data-ttu-id="03881-127">**อนุกรมเวลา** - อนุกรมเวลาคือวิธีการแสดงเวลาเป็นจุดข้อมูลที่ต่อเนื่องกัน</span><span class="sxs-lookup"><span data-stu-id="03881-127">**Time series** - a time series is a way of displaying time as successive data points.</span></span> <span data-ttu-id="03881-128">จุดข้อมูลเหล่านั้นอาจเพิ่มขึ้น เช่น วินาที ชั่วโมง เดือน หรือปี</span><span class="sxs-lookup"><span data-stu-id="03881-128">Those data points could be increments such as seconds, hours, months, or years.</span></span>  
* <span data-ttu-id="03881-129">**ตัวแปรต่อเนื่อง** - ตัวแปรแบบต่อเนื่องสามารถเป็นค่าใดก็ตามที่อยู่ระหว่างขีดจำกัดต่ำสุดและสูงสุด มิฉะนั้นจะเป็นตัวแปรที่ไม่ต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="03881-129">**Continuous variable** - a continuous variable can be any value between its minimum and maximum limits, otherwise it is a discrete variable.</span></span> <span data-ttu-id="03881-130">ตัวอย่างคือ อุณหภูมิ น้ำหนัก อายุ และเวลา</span><span class="sxs-lookup"><span data-stu-id="03881-130">Examples are temperature, weight, age, and time.</span></span> <span data-ttu-id="03881-131">ตัวแปรแบบต่อเนื่องสามารถประกอบด้วยเศษหรือส่วนของตัวแปรได้</span><span class="sxs-lookup"><span data-stu-id="03881-131">Continuous variables can include fractions or portions of the value.</span></span> <span data-ttu-id="03881-132">จำนวนสเก็ตบอร์ดสีน้ำเงินทั้งหมดที่ขายได้เป็นตัวแปรแบบไม่ต่อเนื่องเนื่องจากเราไม่สามารถขายสเก็ตบอร์ดครึ่งตัวได้</span><span class="sxs-lookup"><span data-stu-id="03881-132">The total number of blue skateboards sold is a discrete variable since we can't sell half a skateboard.</span></span>  

## <a name="what-types-of-insights-can-you-find"></a><span data-ttu-id="03881-133">คุณสามารถพบข้อมูลเชิงลึกประเภทใดบ้าง?</span><span class="sxs-lookup"><span data-stu-id="03881-133">What types of insights can you find?</span></span>
<span data-ttu-id="03881-134">นี่คืออัลกอริทึมที่ Power BI ใช้</span><span class="sxs-lookup"><span data-stu-id="03881-134">These are the algorithms that Power BI uses.</span></span> 

### <a name="category-outliers-topbottom"></a><span data-ttu-id="03881-135">ประเภทข้อมูลที่ผิดปกติ (บน/ล่าง)</span><span class="sxs-lookup"><span data-stu-id="03881-135">Category outliers (top/bottom)</span></span>
<span data-ttu-id="03881-136">ไฮไลต์กรณีที่หนึ่งหรือสองหมวดหมู่มีค่ามากกว่าหมวดหมู่อื่น</span><span class="sxs-lookup"><span data-stu-id="03881-136">Highlights cases where one or two categories have much larger values than other categories.</span></span>  

![ตัวอย่างข้อมูลที่ผิดปกติ](./media/end-user-insight-types/pbi-auto-insight-type-category-outliers.png)

### <a name="change-points-in-a-time-series"></a><span data-ttu-id="03881-138">เปลี่ยนจุดในชุดข้อมูลเวลา</span><span class="sxs-lookup"><span data-stu-id="03881-138">Change points in a time series</span></span>
<span data-ttu-id="03881-139">ไฮไลต์เมื่อมีการเปลี่ยนแปลงที่สำคัญในแนวโน้มในชุดข้อมูลเวลา</span><span class="sxs-lookup"><span data-stu-id="03881-139">Highlights when there are significant changes in trends in a time series of data.</span></span>

![เปลี่ยนจุดในชุดข้อมูลเวลา](./media/end-user-insight-types/pbi-auto-insight-type-changepoint.png)

### <a name="correlation"></a><span data-ttu-id="03881-141">สหสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="03881-141">Correlation</span></span>
<span data-ttu-id="03881-142">ตรวจพบกรณีที่หน่วยวัดหลายตัวแสดงรูปแบบหรือแนวโน้มที่คล้ายกันเมื่อพล็อตกับหมวดหมู่หรือค่าในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="03881-142">Detects cases where multiple measures show a similar pattern or trend when plotted against a category or value in the dataset.</span></span>

![ตัวอย่างสหสัมพันธ์](./media/end-user-insight-types/pbi-auto-insight-type-correlation.png)

### <a name="low-variance"></a><span data-ttu-id="03881-144">ผลต่างต่ำ</span><span class="sxs-lookup"><span data-stu-id="03881-144">Low Variance</span></span>
<span data-ttu-id="03881-145">ตรวจหากรณีที่จุดข้อมูลสำหรับมิติอยู่ไม่ไกลจากค่าเฉลี่ย ดังนั้น "ความแปรปรวน" จึงมีค่าต่ำ</span><span class="sxs-lookup"><span data-stu-id="03881-145">Detects cases where data points for a dimension aren't far from the mean, so the "variance" is low.</span></span> <span data-ttu-id="03881-146">สมมติว่าคุณมีหน่วยวัด "ยอดขาย" และมิติ "ภูมิภาค"</span><span class="sxs-lookup"><span data-stu-id="03881-146">Let's say you have the measure "sales" and a dimension "region".</span></span> <span data-ttu-id="03881-147">และเมื่อมองไปทั่วภูมิภาคคุณจะเห็นว่ามีจุดแตกต่างกันเล็กน้อยระหว่างจุดข้อมูลกับค่าเฉลี่ย (ของจุดข้อมูล)</span><span class="sxs-lookup"><span data-stu-id="03881-147">And looking across region you see that there is very little difference between the data points and the mean (of the data points).</span></span> <span data-ttu-id="03881-148">ข้อมูลเชิงลึกจะทริกเกอร์เมื่อความแปรปรวนของยอดขายในทุกภูมิภาคต่ำกว่าค่าเกณฑ์</span><span class="sxs-lookup"><span data-stu-id="03881-148">The insight triggers when the variance of sales across all regions is below a threshold.</span></span> <span data-ttu-id="03881-149">กล่าวคือ เมื่อยอดขายใกล้เคียงกันในทุกภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="03881-149">In other words, when sales are pretty similar across all regions.</span></span>

![ตัวอย่างผลต่างต่ำ](./media/end-user-insight-types/power-bi-insights-low-variance.png)

### <a name="majority-major-factors"></a><span data-ttu-id="03881-151">ส่วนหลัก (ปัจจัยหลัก)</span><span class="sxs-lookup"><span data-stu-id="03881-151">Majority (Major factors)</span></span>
<span data-ttu-id="03881-152">ค้นหากรณีที่ส่วนใหญ่ของค่าทั้งหมดสามารถเกิดจากการคูณเดียวเมื่อแบ่งย่อยตามขนาดอื่น</span><span class="sxs-lookup"><span data-stu-id="03881-152">Finds cases where a majority of a total value can be attributed to a single factor when broken down by another dimension.</span></span>  

![ตัวอย่างปัจจัยหลัก](./media/end-user-insight-types/pbi-auto-insight-type-majority.png)

### <a name="outliers"></a><span data-ttu-id="03881-154">ค่าผิดปกติ</span><span class="sxs-lookup"><span data-stu-id="03881-154">Outliers</span></span>
<span data-ttu-id="03881-155">ประเภทข้อมูลเชิงลึกนี้ใช้แบบจำลองคลัสเตอร์เพื่อค้นหาค่าผิดปกติในข้อมูลอนุกรมที่ไม่ใช่เวลา</span><span class="sxs-lookup"><span data-stu-id="03881-155">This insight type uses a clustering model to find outliers in non-time series data.</span></span> <span data-ttu-id="03881-156">ค่าผิดปกติตรวจพบเมื่อมีหมวดหมู่เฉพาะที่มีค่าแตกต่างจากหมวดหมู่อื่นอย่างมีนัยสำคัญ</span><span class="sxs-lookup"><span data-stu-id="03881-156">Outliers detects when there are specific categories with values significantly different than the other categories.</span></span>

![ตัวอย่างค่าผิดปกติ](./media/end-user-insight-types/power-bi-outliers.png)

### <a name="overall-trends-in-time-series"></a><span data-ttu-id="03881-158">แนวโน้มโดยรวมในชุดข้อมูลเวลา</span><span class="sxs-lookup"><span data-stu-id="03881-158">Overall trends in time series</span></span>
<span data-ttu-id="03881-159">ตรวจพบแนวโน้มขึ้น หรือลงในชุดข้อมูลเวลา</span><span class="sxs-lookup"><span data-stu-id="03881-159">Detects upward or downward trends in time series data.</span></span>

![แนวโน้มโดยรวมในชุดข้อมูลเวลา](./media/end-user-insight-types/pbi-auto-insight-type-trend.png)

### <a name="seasonality-in-time-series"></a><span data-ttu-id="03881-161">กาลในชุดข้อมูลเวลา</span><span class="sxs-lookup"><span data-stu-id="03881-161">Seasonality in time series</span></span>
<span data-ttu-id="03881-162">ค้นหารูปแบบเป็นครั้งคราวในข้อมูลชุดข้อมูลเวลา เช่นกาลรายสัปดาห์ เดือน หรือรายปี</span><span class="sxs-lookup"><span data-stu-id="03881-162">Finds periodic patterns in time series data, such as weekly, monthly, or yearly seasonality.</span></span>

![ตัวอย่างกาล](./media/end-user-insight-types/pbi-auto-insight-type-seasonality-new.png)

### <a name="steady-share"></a><span data-ttu-id="03881-164">การแชร์แบบคงที่</span><span class="sxs-lookup"><span data-stu-id="03881-164">Steady share</span></span>
<span data-ttu-id="03881-165">ไฮไลต์กรณีมีความสัมพันธ์หลัก-รองระหว่างใช้ร่วมกันของค่ารองสัมพันธ์กับค่าโดยรวมของค่าหลักระหว่างตัวแปรอย่างต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="03881-165">Highlights cases where there is a parent-child correlation between the share of a child value in relation to the overall value of the parent across a continuous variable.</span></span> <span data-ttu-id="03881-166">ข้อมูลเชิงลึกเกี่ยวกับการแชร์แบบคงที่จะนำไปใช้กับบริบทของหน่วยวัด มิติ และมิติวันที่/เวลาอื่น</span><span class="sxs-lookup"><span data-stu-id="03881-166">The steady share insight applies to the context of a measure, a dimension, and another date/time dimension.</span></span> <span data-ttu-id="03881-167">ข้อมูลเชิงลึกนี้จะทริกเกอร์เมื่อมีค่ามิติเฉพาะเช่น "ภูมิภาคตะวันออก" มีเปอร์เซ็นต์คงที่ของยอดขายโดยรวมในมิติวันที่/เวลานั้น</span><span class="sxs-lookup"><span data-stu-id="03881-167">This insight triggers when a particular dimension value, e.g. "the east region", has a steady percentage of overall sales across that date/time dimension.</span></span>

<span data-ttu-id="03881-168">ข้อมูลเชิงลึกเกี่ยวกับการแชร์แบบคงที่จะคล้ายกับข้อมูลเชิงลึกผลต่างต่ำเนื่องจากทั้งสองเกี่ยวข้องกับการขาดความแปรปรวนของค่าตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="03881-168">The steady share insight is similar to the low variance insight, because they both relate to the lack of variance of a value across time.</span></span> <span data-ttu-id="03881-169">อย่างไรก็ตามข้อมูลเชิงลึกที่ใช้ร่วมกันจะวัดความแตกต่างของ **เปอร์เซ็นต์ของทั้งหมด** ในระหว่างช่วงเวลา ในขณะที่ข้อมูลเชิงลึกของผลต่างต่ำวัดความแปรปรวนของค่าหน่วยวัดแบบสัมบูรณ์ในมิติ</span><span class="sxs-lookup"><span data-stu-id="03881-169">However, the steady share insight measures the lack of variance of the **percentage of overall** across time, while the low variance insight measures the lack of variance of the absolute measure values across a dimension.</span></span>

![การแชร์แบบคงที่](./media/end-user-insight-types/pbi-auto-insight-type-steadyshare.png)

### <a name="time-series-outliers"></a><span data-ttu-id="03881-171">ข้อมูลชุดเวลาที่ผิดปกติ</span><span class="sxs-lookup"><span data-stu-id="03881-171">Time series outliers</span></span>
<span data-ttu-id="03881-172">สำหรับข้อมูลทั่วทั้งชุดข้อมูลเวลา ตรวจพบเมื่อมีการระบุวันที่หรือเวลา ด้วยค่าที่แตกต่างอย่างมากจากค่าวันที่/เวลาอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="03881-172">For data across a time series, detects when there are specific dates or times with values significantly different than the other date/time values.</span></span>

![ข้อมูลชุดเวลาที่ผิดปกติ](./media/end-user-insight-types/pbi-auto-insight-type-time-series-outliers-purple.png)


## <a name="next-steps"></a><span data-ttu-id="03881-174">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="03881-174">Next steps</span></span>
[<span data-ttu-id="03881-175">ข้อมูลเชิงลึกที่ power BI</span><span class="sxs-lookup"><span data-stu-id="03881-175">Power BI insights</span></span>](end-user-insights.md)

<span data-ttu-id="03881-176">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="03881-176">More questions?</span></span> [<span data-ttu-id="03881-177">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="03881-177">Try the Power BI Community</span></span>](https://community.powerbi.com/)

