---
title: ใช้ฟีเจอร์วิเคราะห์เพื่ออธิบายการผันผวนในภาพรายงาน
description: รับข้อมูลเชิงลึกอย่างง่ายดายเพื่อพิ่มหรือลดการบริการ Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-explore
ms.topic: conceptual
ms.date: 08/12/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 9d66ec405ebec8c2da59a37cd986098444979c4b
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96401408"
---
# <a name="use-the-analyze-feature-to-explain-fluctuations-in-report-visuals"></a><span data-ttu-id="b97e0-103">ใช้ฟีเจอร์วิเคราะห์เพื่ออธิบายการผันผวนในภาพรายงาน</span><span class="sxs-lookup"><span data-stu-id="b97e0-103">Use the Analyze feature to explain fluctuations in report visuals</span></span>

[!INCLUDE[consumer-appliesto-yynn](../includes/consumer-appliesto-yynn.md)]

<span data-ttu-id="b97e0-104">บ่อยครั้งในการแสดงผลด้วยภาพของรายงาน คุณจะเห็นการเพิ่มขึ้นอย่างมากจากนั้นลดความคมชัดในค่า และสงสัยเกี่ยวกับสาเหตุของความผันผวนดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="b97e0-104">Often in report visuals, you see a large increase and then a sharp drop in values, and wonder about the cause of such fluctuations.</span></span> <span data-ttu-id="b97e0-105">คุณสามารถเรียนรู้สาเหตุด้วยการคลิกเพียงไม่กี่ครั้งด้วยการ **วิเคราะห์** ใน **บริการ Power BI**</span><span class="sxs-lookup"><span data-stu-id="b97e0-105">With **Analyze** in **the Power BI service**, you can learn the cause with just a few clicks.</span></span>

<span data-ttu-id="b97e0-106">ตัวอย่างเช่น พิจารณาภาพต่อไปนี้ที่แสดง *หน่วยทั้งหมด* ตาม *เดือน* และ *ผู้ผลิต*</span><span class="sxs-lookup"><span data-stu-id="b97e0-106">For example, consider the following visual that shows *Total units* by *Month* and *Manufacturer*.</span></span> <span data-ttu-id="b97e0-107">VanArsdel มีประสิทธิภาพเหนือกว่าคู่แข่ง แต่มีการลงลึกในเดือนมิถุนายน 2014</span><span class="sxs-lookup"><span data-stu-id="b97e0-107">VanArsdel is outperforming its competitors but has a deep dip in June 2014.</span></span> <span data-ttu-id="b97e0-108">ในกรณีดังกล่าว คุณสามารถสำรวจข้อมูล เพื่อช่วยอธิบายการเปลี่ยนแปลงที่เกิดขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="b97e0-108">In such cases you can explore the data, to help explain the change that occurred.</span></span> 

![การแสดงผลทางภาพด้วยการเพิ่มขึ้นและลดลง](media/end-user-analyze-visuals/power-bi-line-chart.png)

<span data-ttu-id="b97e0-110">คุณสามารถขอให้บริการของ Power BI อธิบายการเพิ่มขึ้น ลดลง หรือตวามผิดปกติในภาพ และได้รับการวิเคราะห์ที่รวดเร็ว อัตโนมัติ และการวิเคราะห์มีข้อมูลเชิงลึกเกี่ยวกับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="b97e0-110">You can ask the Power BI service to explain increases, decreases, or unusual distributions in visuals, and get fast, automated, insightful analysis about your data.</span></span> <span data-ttu-id="b97e0-111">คลิกขวาที่จุดข้อมูล และเลือก **วิเคราะห์ > อธิบายการลดลง** (หรือเพิ่มขึ้น หากเส้นก่อนหน้านี้ต่ำกว่า) หรือ **วิเคราะห์ > หาว่าการกระจายนี้ต่างกันตรงไหน** และข้อมูลเชิงลึกจะถูกส่งไปให้คุณในหน้าต่างที่ใช้งานง่าย</span><span class="sxs-lookup"><span data-stu-id="b97e0-111">Right-click on a data point, and select **Analyze > Explain the decrease** (or increase, if the previous bar was lower), or **Analyze > Find where this distribution is different** and the insight is delivered to you in an easy-to-use window.</span></span>

![ข้อมูลเชิงลึกที่แสดงด้วยภาพ](media/end-user-analyze-visuals/power-bi-decrease.png)

<span data-ttu-id="b97e0-113">ฟีเจอร์วิเคราะห์ข้อมูลเชิงลึกมีบริบท และขึ้นอยู่กับจุดข้อมูลก่อนหน้า - เช่นแถบก่อนหน้า  หรือคอลัมน์ก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="b97e0-113">The Analyze feature is contextual, and is based on the immediately previous data point - such as the previous bar, or column.</span></span>

> [!NOTE]
> <span data-ttu-id="b97e0-114">คุณลักษณะนี้ยังเป็นแค่ตัวอย่าง และอาจเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="b97e0-114">This feature is in preview, and is subject to change.</span></span> <span data-ttu-id="b97e0-115">เปิดใช้งานฟีเจอร์ข้อมูลเชิงลึกแล้วตามค่าเริ่มต้น (คุณไม่จำเป็นต้องตรวจสอบกล่องตัวอย่างเพื่อเปิดใช้งาน)</span><span class="sxs-lookup"><span data-stu-id="b97e0-115">The insight feature is enabled and on by default (you don't need to check a Preview box to enable it).</span></span>

### <a name="which-factors-and-categories-are-chosen"></a><span data-ttu-id="b97e0-116">มีการเลือกปัจจัยและหมวดหมู่ใด</span><span class="sxs-lookup"><span data-stu-id="b97e0-116">Which factors and categories are chosen</span></span>

<span data-ttu-id="b97e0-117">หลังจากตรวจสอบคอลัมน์ที่แตกต่างกัน Power BI จะเลือกและแสดงปัจจัยข้อมูลที่แสดงการเปลี่ยนแปลงที่ใหญ่ที่สุดกับการสนับสนุนที่สัมพันธ์กัน</span><span class="sxs-lookup"><span data-stu-id="b97e0-117">After examining different columns, Power BI selects and displays those factors that show the biggest change to relative contribution.</span></span> <span data-ttu-id="b97e0-118">สำหรับแต่ละหมวดหมู่ ค่าที่มีการเปลี่ยนแปลงของส่วนสนับสนุนอย่างมีนัยสำคัญที่สุดจะถูกนำไปใช้ในการอธิบาย</span><span class="sxs-lookup"><span data-stu-id="b97e0-118">For each, the values which had the most significant change to contribution are called out in the description.</span></span> <span data-ttu-id="b97e0-119">นอกจากนี้ ค่าที่มีการเพิ่มขึ้นและลดลงมากที่สุดตามที่เกิดขึ้นจริงจะถูกนำไปใช้ด้วย</span><span class="sxs-lookup"><span data-stu-id="b97e0-119">In addition, the values that had the largest actual increases and decreases are also called out.</span></span>

<span data-ttu-id="b97e0-120">หากต้องการดูข้อมูลเชิงลึกทั้งหมดที่สร้างขึ้นโดย Power BI ให้ใช้แถบเลื่อน</span><span class="sxs-lookup"><span data-stu-id="b97e0-120">To see all of the insights generated by Power BI, use the scrollbar.</span></span> <span data-ttu-id="b97e0-121">ลำดับคือการจัดอันดับด้วยผู้สนับสนุนที่สำคัญที่สุดจะแสดงก่อน</span><span class="sxs-lookup"><span data-stu-id="b97e0-121">The order is ranked with the most significant contributor displayed first.</span></span> 

## <a name="using-insights"></a><span data-ttu-id="b97e0-122">การใช้ข้อมูลเชิงลึก</span><span class="sxs-lookup"><span data-stu-id="b97e0-122">Using insights</span></span>
<span data-ttu-id="b97e0-123">หากต้องการใช้ข้อมูลเชิงลึกเพื่ออธิบายแนวโน้มที่เห็นในภาพ ให้คลิกขวาบนจุดข้อมูลใดๆ ก็ตามในแผนภูมิแท่งหรือเส้น และเลือก **วิเคราะห์**</span><span class="sxs-lookup"><span data-stu-id="b97e0-123">To use insights to explain trends seen on visuals, right-click on any data point in a bar or line chart, and select **Analyze**.</span></span> <span data-ttu-id="b97e0-124">จากนั้นเลือกตัวเลือกที่ปรากฏขึ้น: **อธิบายการเพิ่มขึ้น** **อธิบายการลดลง** หรือ **อธิบายส่วนต่าง**</span><span class="sxs-lookup"><span data-stu-id="b97e0-124">Then choose the option that appears: **explain the increase**, **explain the decrease**, or **explain the difference**.</span></span>

<span data-ttu-id="b97e0-125">Power BI Desktop จะเรียกใช้อัลกอริทึมการเรียนรู้ กับข้อมูล และเพิ่มวิชวลและคำอธิบายลงในหน้าต่าง ที่ใช้อธิบายว่าข้อมูลประเภทไหนส่งผลต่อการเพิ่มขึ้นหรือลดลงมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="b97e0-125">Power BI then runs its machine learning algorithms over the data, and populates a window with a visual and a description that describes which categories most influenced the increase or decrease or difference.</span></span>  <span data-ttu-id="b97e0-126">สำหรับตัวอย่างนี้ ข้อมูลเชิงลึกแรกคือแผนภูมิแบบน้ำตก</span><span class="sxs-lookup"><span data-stu-id="b97e0-126">For this example, the first insight is a waterfall chart.</span></span>

![หน้าต่างป็อปอัพข้อมูลเชิงลึก](media/end-user-analyze-visuals/power-bi-insight.png)

<span data-ttu-id="b97e0-128">โดยการเลือกไอคอนขนาดเล็กที่ด้านล่างของแผนแบบภูมิน้ำตก คุณสามารถเลือกให้แสดงข้อมูลเชิงลึก เป็น แผนภูมิกระจาย แผนภูมิคอลัมน์แบบเรียงซ้อน หรือแผนภูมิ ribbon</span><span class="sxs-lookup"><span data-stu-id="b97e0-128">By selecting the small icons at the bottom of the waterfall visual, you can choose to have insights display a scatter chart, stacked column chart, or a ribbon chart.</span></span>

![สกรีนช็อตแสดงไอคอนที่ด้านล่างของวิชวล](media/end-user-analyze-visuals/power-bi-options.png)

<span data-ttu-id="b97e0-130">ใช้ไอคอน *ยกนิ้วโป้งขึ้น* และ *คว่ำนิ้วโป้งลง* ที่ด้านบนของหน้า เพื่อเสนอแนะคำติชมภาพและฟีเจอร์นี้</span><span class="sxs-lookup"><span data-stu-id="b97e0-130">Use the *thumbs up* and *thumbs down* icons at the top of the page to provide feedback about the visual and the feature.</span></span>  

![ไอคอนยกนิ้วโป้งขึ้นและคว่ำนิ้วโป้งลง](media/end-user-analyze-visuals/power-bi-thumbs.png)


<span data-ttu-id="b97e0-132">คุณสามารถใช้ข้อมูลเชิงลึกเมื่อรายงานของคุณอยู่ในโหมดอ่านหรือแก้ไข ซึ่งทำให้มีความยืดหยุ่นในการวิเคราะห์ข้อมูล และสร้างภาพที่คุณสามารถเพิ่มในรายงานของคุณได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="b97e0-132">You can use insights when your report is in Reading or Editing view, making it versatile for both analyzing data, and for creating visuals you can easily add to your reports.</span></span> <span data-ttu-id="b97e0-133">ถ้าคุณมีรายงานที่เปิดอยู่ในมุมมองการแก้ไข คุณจะเห็นไอคอนเครื่องหมายบวกถัดจากไอคอนรูปนิ้วโป้ง</span><span class="sxs-lookup"><span data-stu-id="b97e0-133">If you have the report open in Editing view, you'll see a plus icon next to the thumb icons.</span></span> <span data-ttu-id="b97e0-134">เลือกไอคอนเครื่องหมายบวกเพื่อเพิ่มข้อมูลเชิงลึกลงในรายงานของคุณเป็นภาพใหม่</span><span class="sxs-lookup"><span data-stu-id="b97e0-134">Select the plus icon to add the insight to your report as a new visual.</span></span> 

![สกรีนช็อตแสดงไอคอนเครื่องหมายบวกที่ใช้ในการเพิ่มข้อมูลเชิงลึก](media/end-user-analyze-visuals/power-bi-add-visual.png)

## <a name="details-of-the-results-returned"></a><span data-ttu-id="b97e0-136">รายละเอียดของผลลัพธ์ที่ส่งกลับ</span><span class="sxs-lookup"><span data-stu-id="b97e0-136">Details of the results returned</span></span>

<span data-ttu-id="b97e0-137">รายละเอียดที่ส่งกลับโดยข้อมูลเชิงลึกมีจุดมุ่งหมายเพื่อเน้นสิ่งที่แตกต่างกันระหว่างสองช่วงเวลา เพื่อช่วยให้คุณเข้าใจการเปลี่ยนแปลงระหว่างกัน</span><span class="sxs-lookup"><span data-stu-id="b97e0-137">The details returned by insights are intended to highlight what was different between the two time periods, to help you understand the change between them.</span></span>  

<span data-ttu-id="b97e0-138">อัลกอริธึมสามารถคิดได้ว่าจะใช้คอลัมน์อื่นๆ ทั้งหมดในโมเดลและคำนวณรายละเอียดตามคอลัมน์นั้น *ก่อน* และ *หลัง* ช่วงเวลาโดยพิจารณาว่ามีการเปลี่ยนแปลงเกิดขึ้นในรายละเอียดนั้น และจากนั้นส่งคืนคอลัมน์เหล่านั้นที่มีขนาดการเปลี่ยนแปลงมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="b97e0-138">The algorithm can be thought of as taking all the other columns in the model, and calculating the breakdown by that column for the *before* and *after* time periods, determining how much change occurred in that breakdown, and then returning those columns with the biggest change.</span></span> <span data-ttu-id="b97e0-139">ตัวอย่างเช่น *รัฐ* ถูกเลือกในข้อมูลเชิงลึกแบบน้ำตกด้านบน เนื่องจากการสนับสนุนที่โดยรัฐหลุยเซียนา เท็กซัส และโคโลราโดลดลง 13% ถึง 19% จากเดือนมิถุนายนถึงเดือนกรกฎาคม และให้ประโยชน์สูงสุดในการลดลงของ *หน่วยรวม*</span><span class="sxs-lookup"><span data-stu-id="b97e0-139">For example, *State* was selected in the waterfall insight above, as the contribution made by Louisiana, Texas, and Colorado fell 13% to 19% from June to July, and contributed the most to the decrease in *Total units*.</span></span>  

<span data-ttu-id="b97e0-140">สำหรับข้อมูลเชิงลึกแต่ละรายการที่ถูกส่งกลับ มีสี่ภาพที่สามารถแสดงได้</span><span class="sxs-lookup"><span data-stu-id="b97e0-140">For each insight returned, there are four visuals that can be displayed.</span></span> <span data-ttu-id="b97e0-141">ภาพสามภาพเหล่านี้มีจุดมุ่งหมายเพื่อเน้นการเปลี่ยนแปลงของส่วนสนับสนุนระหว่างสองช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="b97e0-141">Three of those visuals are intended to highlight the change in contribution between the two periods.</span></span> <span data-ttu-id="b97e0-142">ตัวอย่าง เช่นสำหรับคำอธิบายการเพิ่มขึ้นจาก *ไตรมาส 2* ถึง *ไตรมาส 3*</span><span class="sxs-lookup"><span data-stu-id="b97e0-142">For example, for the explanation of the increase from *Qtr 2* to *Qtr 3*.</span></span> <span data-ttu-id="b97e0-143">แผนภูมิ ribbon แสดงการเปลี่ยนแปลงทั้งก่อนและหลังจุดข้อมูลที่ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="b97e0-143">The ribbon chart shows change both  before and after the selected data point.</span></span>

### <a name="the-scatter-plot"></a><span data-ttu-id="b97e0-144">แผนภูมกระจาย</span><span class="sxs-lookup"><span data-stu-id="b97e0-144">The scatter plot</span></span>

![ภาพหน้าจอขนาดเล็กแสดงไอคอนแผนภูมิกระจายที่เลือก](media/end-user-analyze-visuals/power-bi-scatter-icon.png)

<span data-ttu-id="b97e0-146">ภาพแผนภูมิกระจายจะแสดงค่าของการวัดในช่วงแรก (บนแกน x) เทียบกับค่าของการวัดในช่วงที่สอง (บนแกน y) สำหรับแต่ละค่าของคอลัมน์ (ในกรณีนี้คือ *รัฐ* ู่)</span><span class="sxs-lookup"><span data-stu-id="b97e0-146">The scatter plot visual shows the value of the measure in the first period (on the x-axis) against the value of the measure in the second period (on the y-axis), for each value of the column (*State* in this case).</span></span> <span data-ttu-id="b97e0-147">จุดข้อมูลอยู่ในภูมิภาคสีเขียวหากเพิ่มขึ้น และในภูมิภาคสีแดงหากลดลง</span><span class="sxs-lookup"><span data-stu-id="b97e0-147">Data points are in the green region if they have increased, and in the red region if they have decreased.</span></span> 

<span data-ttu-id="b97e0-148">เส้นประแสดงให้เห็นถึงจุดที่พอเหมาะที่สุด  จุดข้อมูลเหนือเส้นนี้เพิ่มขึ้นมากกว่าแนวโน้มโดยรวมและจุดข้อมูลต่ำกว่าเส้นลดน้อยลง</span><span class="sxs-lookup"><span data-stu-id="b97e0-148">The dotted line shows the best fit, and data points above this line increased by more than the overall trend, and those below it by less.</span></span>  

![แผนภูมิกระจายที่มีเส้นประ](media/end-user-analyze-visuals/power-bi-scatter.png)

<span data-ttu-id="b97e0-150">รายการข้อมูลที่มีค่าว่างในช่วงเวลาหนึ่งๆ จะไม่ปรากฏในแผนภูมิกระจาย</span><span class="sxs-lookup"><span data-stu-id="b97e0-150">Data items whose value was blank in either period will not appear on the scatter plot.</span></span>

### <a name="the-100-stacked-column-chart"></a><span data-ttu-id="b97e0-151">แผนภูมิคอลัมน์แบบเรียงซ้อน 100%</span><span class="sxs-lookup"><span data-stu-id="b97e0-151">The 100% stacked column chart</span></span>

![ภาพหน้าจอขนาดเล็กแสดงไอคอนแผนภูมิคอลัมน์ที่เลือก](media/end-user-analyze-visuals/power-bi-column-icon.png)

<span data-ttu-id="b97e0-153">ภาพแผนภูมิคอลัมน์แบบเรียงซ้อน 100% แสดงค่าของการสนับสนุนสำหรับผลรวม (100%) สำหรับจุดข้อมูลที่เลือกและก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="b97e0-153">The 100% stacked column chart visual shows the value of the contribution to the total (100%), for the selected data point and the previous.</span></span> <span data-ttu-id="b97e0-154">ซึ่งจะช่วยให้เปรียบเทียบการสนับสนุนสำหรับแต่ละจุดข้อมูลได้แบบแบบเคียงข้างกัน</span><span class="sxs-lookup"><span data-stu-id="b97e0-154">This allows side-by-side comparison of the contribution for each data point.</span></span> <span data-ttu-id="b97e0-155">ในตัวอย่างนี้ คำแนะนำเครื่องมือแสดงการสนับสนุนจริงสำหรับค่าที่เลือกของรัฐเท็กซัส</span><span class="sxs-lookup"><span data-stu-id="b97e0-155">In this example, the tooltips show the actual contribution for the selected value of Texas.</span></span> <span data-ttu-id="b97e0-156">เนื่องจากรายการของรัฐมีความยาว คำแนะนำเครื่องมือจะช่วยให้คุณเห็นรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="b97e0-156">Because the list of states is long, tooltips help you see the details.</span></span> <span data-ttu-id="b97e0-157">โดยใช้คำแนะนำเครื่องมือ เราเห็นว่ารัฐเท็กซัสมีส่วนเกี่ยวเนื่องกับจำนวนหน่วยรวม (31% และ 32%) แต่จำนวนของหน่วยทั้งหมดที่ลดลงจาก 89 เป็น 71</span><span class="sxs-lookup"><span data-stu-id="b97e0-157">By using the tooltips, we see that Texas contributed about the same percent to the total units (31% and 32%), but the actual number of total units decreased from 89 to 71.</span></span> <span data-ttu-id="b97e0-158">โปโปรดจำไว้ว่าแกน Y เป็นเปอร์เซ็นต์ ไม่ใช่ผลรวมและแต่ละแถบคอลัมน์เป็นเปอร์เซ็นต์ไม่ใช่ค่า</span><span class="sxs-lookup"><span data-stu-id="b97e0-158">Remember, the Y axis is a percentage, not a total, and each column band is a percentage, not a value.</span></span> 

![แผนภูมิคอลัมน์แบบเรียงซ้อน 100%](media/end-user-analyze-visuals/power-bi-stacked.png)

### <a name="the-ribbon-chart"></a><span data-ttu-id="b97e0-160">แผนภูมิริบบอน</span><span class="sxs-lookup"><span data-stu-id="b97e0-160">The ribbon chart</span></span>

![ภาพหน้าจอขนาดเล็กแสดงไอคอนแผนภูมิริบบอนที่เลือก](media/end-user-analyze-visuals/power-bi-ribbon-icon.png)

<span data-ttu-id="b97e0-162">ภาพแผนภูมิ ribbon แสดงค่าของหน่วยวัดก่อนและหลัง</span><span class="sxs-lookup"><span data-stu-id="b97e0-162">The ribbon chart visual shows the value of the measure before and after.</span></span> <span data-ttu-id="b97e0-163">ซึ่งมีประโยชน์โดยเฉพาะอย่างยิ่งในการแสดงการเปลี่ยนแปลงของส่วนสนับสนุนเมื่อ *การเรียงลำดับ* ของผู้สนับสนุนมีการเปลี่ยนแปลง (ตัวอย่างเช่น *LA* ลดลงจากจำนวนผู้สนับสนุนอันดับสองไปเป็นอันดับสิบเอ็ด)</span><span class="sxs-lookup"><span data-stu-id="b97e0-163">It's particularly useful in showing the changes in contributions when the *ordering* of contributors changed (for example, *LA* dropped from number two contributor to number eleven).</span></span>  <span data-ttu-id="b97e0-164">และแม้ว่า *TX* ถูกแสดงด้วยริบบอนแบบกว้างที่ด้านบนซึ่งบ่งบอกว่าเป็นผู้สนับสนุนที่สำคัญที่สุดก่อนและหลัง ค่าที่ลดลงแสดงให้เห็นว่าค่าของการสนับสนุนลดลงทั้งในช่วงระยะเวลาที่เลือกไว้และหลังจากนั้น</span><span class="sxs-lookup"><span data-stu-id="b97e0-164">And, though *TX* is represented by a wide ribbon at the top signifying that it is the most significant contributor before and after, the drop shows that the value of the contribution dropped both during the selected period and after.</span></span>

![แผนภูมิริบบอน](media/end-user-analyze-visuals/power-bi-ribbon-tooltip.png)

### <a name="the-waterfall-chart"></a><span data-ttu-id="b97e0-166">แผนภูมิน้ำตก</span><span class="sxs-lookup"><span data-stu-id="b97e0-166">The waterfall chart</span></span>

![ภาพหน้าจอขนาดเล็กแสดงไอคอนแผนภูมิแบบน้ำตกที่เลือก](media/end-user-analyze-visuals/power-bi-waterfall-icon.png)

<span data-ttu-id="b97e0-168">ภาพที่สี่คือแผนภูมิน้ำตก ซึ่งแสดงการเพิ่มขึ้นหรือลดลงระหว่างช่วงเวลาตามจริง</span><span class="sxs-lookup"><span data-stu-id="b97e0-168">The fourth visual is a waterfall chart, showing actual increases or decreases between the periods.</span></span> <span data-ttu-id="b97e0-169">ภาพนี้แสดงให้เห็นมีผู้มีสนับสนุนอย่างมีนัยสำคัญต่อการลดลงของเดือนมิถุนายน 2014 -- ในกรณีนี้คือ **รัฐ**</span><span class="sxs-lookup"><span data-stu-id="b97e0-169">This visual clearly shows one significant contributor to the decrease for June 2014 -- in this case, **State**.</span></span> <span data-ttu-id="b97e0-170">และผลกระทบของ **รัฐ** ในหน่วยรวมคือการปฏิเสธในรัฐหลุยเซียนา เท็กซัส และโคโลราโดที่มีบทบาทที่สำคัญที่สุด</span><span class="sxs-lookup"><span data-stu-id="b97e0-170">And the particulars of **State**'s influence on total units are that declines in Louisiana, Texas, and Colorado played the most significant role.</span></span>      

![แผนภูมิน้ำตก](media/end-user-analyze-visuals/power-bi-insight.png)


 



## <a name="considerations-and-limitations"></a><span data-ttu-id="b97e0-172">ข้อควรพิจารณาและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="b97e0-172">Considerations and limitations</span></span>
<span data-ttu-id="b97e0-173">เนื่องจากข้อมูลเชิงลึกเหล่านี้ขึ้นอยู่กับการเปลี่ยนแปลงจากจุดข้อมูลก่อนหน้า ดังนั้นจึงไม่สามารถใช้งานได้เมื่อคุณเลือกจุดข้อมูลแรกในภาพ</span><span class="sxs-lookup"><span data-stu-id="b97e0-173">Since these insights are based on the change from the previous data point, they aren't available when you select the first data point in a visual.</span></span> 

<span data-ttu-id="b97e0-174">การ **วิเคราะห์** ไม่พร้อมใช้งานสำหรับชนิดภาพทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b97e0-174">**Analyze** is not available for all visual types.</span></span> 

<span data-ttu-id="b97e0-175">รายการต่อไปนี้คือคอลเลกชันของสถานการณ์ที่ไม่ได้รับการสนับสนุนในขณะนี้สำหรับ **วิเคราะห์ - อธิบายการเพิ่ม/ลด/ส่วนต่าง**:</span><span class="sxs-lookup"><span data-stu-id="b97e0-175">The following list is the collection of currently unsupported scenarios for **Analyze - explain the increase/decrease/difference**:</span></span>

* <span data-ttu-id="b97e0-176">ตัวกรอง TopN</span><span class="sxs-lookup"><span data-stu-id="b97e0-176">TopN filters</span></span>
* <span data-ttu-id="b97e0-177">ตัวกรอง รวม/ไม่รวม</span><span class="sxs-lookup"><span data-stu-id="b97e0-177">Include/exclude filters</span></span>
* <span data-ttu-id="b97e0-178">ตัวกรองหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="b97e0-178">Measure filters</span></span>
* <span data-ttu-id="b97e0-179">หน่วยวัดที่ไม่ใช่ตัวเลข</span><span class="sxs-lookup"><span data-stu-id="b97e0-179">Non-numeric measures</span></span>
* <span data-ttu-id="b97e0-180">ใช้ "แสดงค่าเป็น"</span><span class="sxs-lookup"><span data-stu-id="b97e0-180">Use of "Show value as"</span></span>
* <span data-ttu-id="b97e0-181">การวัดที่กรองแล้ว - การวัดที่กรองแล้วคือการคำนวณระดับชั้นด้วยสายตาโดยใช้ตัวกรองเฉพาะ (ตัวอย่างเช่น *ยอดขายรวมสำหรับประเทศฝรั่งเศส*) และใช้กับภาพจริงบางส่วนที่สร้างโดยคุณลักษณะข้อมูลเชิงลึก</span><span class="sxs-lookup"><span data-stu-id="b97e0-181">Filtered measures - filtered measures are visual level calculations with a specific filter applied (for example, *Total Sales for France*), and are used on some of the visuals created by the insights feature</span></span>
* <span data-ttu-id="b97e0-182">คอลัมน์ประเภทที่ใช้เป็นแกน X เว้นแต่ว่าจะกำหนดการเรียงลำดับตามคอลัมน์ที่เป็นสเกลา</span><span class="sxs-lookup"><span data-stu-id="b97e0-182">Categorical columns on X-axis unless it defines a sort by column that is scalar.</span></span> <span data-ttu-id="b97e0-183">ถ้ามีการใช้ลำดับชั้น ทุกคอลัมน์ในลำดับชั้นที่ใช้งานจะต้องตรงกับเงื่อนไขนี้</span><span class="sxs-lookup"><span data-stu-id="b97e0-183">If using a hierarchy, then every column in the active hierarchy has to match this condition</span></span>


## <a name="next-steps"></a><span data-ttu-id="b97e0-184">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="b97e0-184">Next steps</span></span>
<span data-ttu-id="b97e0-185">[แผนภูมิน้ำตก](../visuals/power-bi-visualization-waterfall-charts.md)  </span><span class="sxs-lookup"><span data-stu-id="b97e0-185">[Waterfall charts](../visuals/power-bi-visualization-waterfall-charts.md)  </span></span>  
<span data-ttu-id="b97e0-186">[แผนภูมิกระจาย](../visuals/power-bi-visualization-scatter.md)  </span><span class="sxs-lookup"><span data-stu-id="b97e0-186">[Scatter charts](../visuals/power-bi-visualization-scatter.md)  </span></span>  
<span data-ttu-id="b97e0-187">[แผนภูมิคอลัมน์](../visuals/power-bi-report-visualizations.md)  </span><span class="sxs-lookup"><span data-stu-id="b97e0-187">[Column charts](../visuals/power-bi-report-visualizations.md)  </span></span>  
[<span data-ttu-id="b97e0-188">แผนภูมิ Ribbon</span><span class="sxs-lookup"><span data-stu-id="b97e0-188">Ribbon charts</span></span>](../visuals/desktop-ribbon-charts.md)
