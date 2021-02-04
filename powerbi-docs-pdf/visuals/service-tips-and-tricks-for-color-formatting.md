---
title: เคล็ดลับและลูกเล่นในการจัดรูปแบบในรายงาน
description: เคล็ดลับและลูกเล่นในการจัดรูปแบบในรายงาน Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: conceptual
ms.date: 10/29/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 0ab6b799c8c78ab2e76a63a3ec5ee3f37f960b03
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415760"
---
# <a name="tips-and-tricks-for-formatting-in-reports"></a><span data-ttu-id="5be0e-103">เคล็ดลับและลูกเล่นในการจัดรูปแบบในรายงาน</span><span class="sxs-lookup"><span data-stu-id="5be0e-103">Tips and tricks for formatting in reports</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]    

<span data-ttu-id="5be0e-104">Power BI มีหลายวิธีในการปรับแต่งรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="5be0e-104">Power BI provides many different ways to customize your reports.</span></span> <span data-ttu-id="5be0e-105">บทความนี้ให้รายละเอียดคอลเลกชันของเคล็ดลับที่สามารถทำให้การแสดงภาพ Power BI ของคุณดึงดูดใจ น่าสนใจ และตรงตามความต้องการของคุณมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="5be0e-105">This article details a collection of tips that can make your Power BI visualizations more compelling, interesting, and customized to your needs.</span></span>

<span data-ttu-id="5be0e-106">มีเคล็ดลับต่อไปนี้ให้</span><span class="sxs-lookup"><span data-stu-id="5be0e-106">The following tips are provided.</span></span> <span data-ttu-id="5be0e-107">มีเคล็ดลับที่ดีอื่น ๆ หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="5be0e-107">Have another great tip?</span></span> <span data-ttu-id="5be0e-108">เยี่ยม!</span><span class="sxs-lookup"><span data-stu-id="5be0e-108">Great!</span></span> <span data-ttu-id="5be0e-109">ส่งมาที่เราและเราจะดูว่าสามารถเพิ่มลงในรายการนี้ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="5be0e-109">Send it our way and we’ll see about adding it to this list.</span></span>

* <span data-ttu-id="5be0e-110">นำธีมไปใช้กับรายงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5be0e-110">Apply a theme to the entire report</span></span>
* <span data-ttu-id="5be0e-111">เปลี่ยนสีของจุดข้อมูลเดียว</span><span class="sxs-lookup"><span data-stu-id="5be0e-111">Change the color of a single data point</span></span>
* <span data-ttu-id="5be0e-112">การจัดรูปแบบแบบมีเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="5be0e-112">Conditional formatting</span></span>
* <span data-ttu-id="5be0e-113">ยึดตามสีของแผนภูมิสำหรับค่าตัวเลข</span><span class="sxs-lookup"><span data-stu-id="5be0e-113">Base the colors of a chart on a numeric value</span></span>
* <span data-ttu-id="5be0e-114">ยึดตามสีของจุดข้อมูลค่าสำหรับเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5be0e-114">Base the color of data points on a field value</span></span>
* <span data-ttu-id="5be0e-115">กำหนดสีที่ใช้ในระดับสีเอง</span><span class="sxs-lookup"><span data-stu-id="5be0e-115">Customize colors used in the color scale</span></span>
* <span data-ttu-id="5be0e-116">ใช้ระดับสีที่แยกออกจากกัน</span><span class="sxs-lookup"><span data-stu-id="5be0e-116">Use diverging color scales</span></span>
* <span data-ttu-id="5be0e-117">เพิ่มสีให้แถวตาราง</span><span class="sxs-lookup"><span data-stu-id="5be0e-117">Add color to table rows</span></span>
* <span data-ttu-id="5be0e-118">วิธีการยกเลิกการกระทำใน Power BI</span><span class="sxs-lookup"><span data-stu-id="5be0e-118">How to undo in Power BI</span></span>

<span data-ttu-id="5be0e-119">เพื่อทำการเปลี่ยนแปลง คุณต้องแก้ไขสิทธิ์สำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="5be0e-119">To make any changes, you must have edit permissions for the report.</span></span> <span data-ttu-id="5be0e-120">ใน Power BI Desktop เปิดรายงานในมุมมอง **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="5be0e-120">In Power BI Desktop, open the report in **Report** view.</span></span> <span data-ttu-id="5be0e-121">ในบริการของ Power BI นั่นหมายความว่าเปิดรายงานและเลือก **แก้ไข** จากแถบเมนูดังที่แสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5be0e-121">In the Power BI service, that means opening the report and selecting **Edit** from the menu bar, as shown in the following image.</span></span>

![ตำแหน่งที่พบเมนูแก้ไข](media/service-tips-and-tricks-for-color-formatting/power-bi-editing-view.png)

<span data-ttu-id="5be0e-123">เมื่อบานหน้าต่าง **ตัวกรอง** และ **การแสดงผลข้อมูลด้วยภาพ** ปรากฏทางด้านขวาของพื้นที่รายงาน คุณก็พร้อมที่จะเริ่มการกำหนดค่าเองได้</span><span class="sxs-lookup"><span data-stu-id="5be0e-123">When the **Filters** and **Visualizations** panes appear along the right side of the report canvas, you’re ready to start customizing.</span></span> <span data-ttu-id="5be0e-124">ถ้าบานหน้าต่างเมนูไม่ปรากฏ เลือกลูกศร จากมุมบนขวา เพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="5be0e-124">If the panes do not appear, select the arrow, from the top-right corner, to open them.</span></span>

![พื้นที่รายงานในมุมมองการแก้ไข](media/service-tips-and-tricks-for-color-formatting/power-bi-edit-filter.png)

## <a name="apply-a-theme"></a><span data-ttu-id="5be0e-126">นำธีมไปใช้</span><span class="sxs-lookup"><span data-stu-id="5be0e-126">Apply a theme</span></span>
<span data-ttu-id="5be0e-127">ด้วยธีมรายงาน คุณสามารถใช้การเปลี่ยนแปลงการออกแบบกับรายงานทั้งหมดของคุณได้ เช่น การใช้สีสำหรับองค์กร การเปลี่ยนชุดไอคอน หรือการใช้การจัดรูปแบบภาพตามค่าเริ่มต้นใหม่</span><span class="sxs-lookup"><span data-stu-id="5be0e-127">With report themes you can apply design changes to your entire report, such as using corporate colors, changing icon sets, or applying new default visual formatting.</span></span> <span data-ttu-id="5be0e-128">เมื่อคุณใช้ธีมรายงาน การแสดงผลด้วยภาพทั้งหมดในรายงานของคุณจะใช้สีและการจัดรูปแบบจากธีมที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="5be0e-128">When you apply a report theme, all visuals in your report use the colors and formatting from your selected theme.</span></span> <span data-ttu-id="5be0e-129">เมื่อต้องการเรียนรู้เพิ่มเติม โปรดดู [ใช้ธีมรายงาน](../create-reports/desktop-report-themes.md)</span><span class="sxs-lookup"><span data-stu-id="5be0e-129">To learn more, see [Use report themes](../create-reports/desktop-report-themes.md)</span></span>

![สลับไอคอนดังกล่าวในแถบเมนู](media/service-tips-and-tricks-for-color-formatting/power-bi-themes.png)

<span data-ttu-id="5be0e-131">ที่นี่ เราได้ใช้ธีม **Innovate** กับรายงานยอดขายและการตลาด</span><span class="sxs-lookup"><span data-stu-id="5be0e-131">Here, we've applied the **Innovate** theme to the Sales and Marketing report.</span></span>

![ธีม Innovate ถูกนำมาใช้](media/service-tips-and-tricks-for-color-formatting/power-bi-theme-innovate.png)

## <a name="change-the-color-of-a-single-data-point"></a><span data-ttu-id="5be0e-133">เปลี่ยนสีของจุดข้อมูลเดียว</span><span class="sxs-lookup"><span data-stu-id="5be0e-133">Change the color of a single data point</span></span>
<span data-ttu-id="5be0e-134">ในบางครั้งคุณต้องการไฮไลท์จุดข้อมูลจุดใดจุดหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5be0e-134">Sometimes you want to highlight one particular data point.</span></span> <span data-ttu-id="5be0e-135">อาจเป็นตัวเลขยอดขายสำหรับการเปิดตัวผลิตภัณฑ์ใหม่ หรือคะแนนคุณภาพที่เพิ่มขึ้นหลังจากเปิดตัวโปรแกรมใหม่</span><span class="sxs-lookup"><span data-stu-id="5be0e-135">Perhaps it’s a sales figure for the launch of a new product, or increased quality scores after launching a new program.</span></span> <span data-ttu-id="5be0e-136">ด้วย Power BI คุณสามารถไฮไลท์จุดข้อมูลเฉพาะได้โดยการเปลี่ยนสี</span><span class="sxs-lookup"><span data-stu-id="5be0e-136">With Power BI, you can highlight a particular data point by changing its color.</span></span>

<span data-ttu-id="5be0e-137">แสดงการจัดลำดับภาพต่อไปนี้ของหน่วยที่ขายตามส่วนของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5be0e-137">The following visualization ranks units sold by product segment.</span></span> 

![เปลี่ยนสีของข้อมูลเป็นสีเทา](media/service-tips-and-tricks-for-color-formatting/power-bi-format.png)

<span data-ttu-id="5be0e-139">ตอนนี้สมมติว่า คุณต้องการเรียกใช้เซกเมนต์ **ความสะดวกสบาย** เพื่อจะดูว่าเซกเมนต์ใหม่นี้แสดงผลโดยใช้สีออกมาได้ดี</span><span class="sxs-lookup"><span data-stu-id="5be0e-139">Now imagine you want to call out the **Convenience** segment to show how well this brand new segment is performing, by using color.</span></span> <span data-ttu-id="5be0e-140">ต่อไปนี้คือขั้นตอน:</span><span class="sxs-lookup"><span data-stu-id="5be0e-140">Here are the steps:</span></span>

<span data-ttu-id="5be0e-141">ขยายการ์ด **สีข้อมูล** และเปิดแถบเลื่อนสำหรับ **แสดงทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5be0e-141">Expand the **Data colors** card and turn the slider On for **Show all**.</span></span> <span data-ttu-id="5be0e-142">ขั้นตอนนี้จะแสดงสีต่าง ๆ สำหรับแต่ละองค์ประกอบข้อมูลในการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="5be0e-142">This displays the colors for each data element in the visualization.</span></span> <span data-ttu-id="5be0e-143">ตอนนี้คุณสามารถปรับเปลี่ยนจุดข้อมูลใดก็ตาม</span><span class="sxs-lookup"><span data-stu-id="5be0e-143">You can now modify any of the data points.</span></span>

![บานหน้าต่างจัดรูปแบบที่มีแสดงการตั้งค่าทั้งหมดเป็น เปิด](media/service-tips-and-tricks-for-color-formatting/power-bi-show-all.png)

<span data-ttu-id="5be0e-145">ตั้งค่า **ความสะดวกสบาย** ให้เป็นสีส้ม</span><span class="sxs-lookup"><span data-stu-id="5be0e-145">Set **Convenience** to orange.</span></span> 

![แผนภูมิคอลัมน์ที่มีหนึ่งคอลัมน์เป็นสีส้ม](media/service-tips-and-tricks-for-color-formatting/power-bi-one-color.png)

<span data-ttu-id="5be0e-147">เมื่อเลือกแล้ว จุดข้อมูล **ความสะดวกสบาย** จะเป็นสีส้มสวยงามและโดดเด่นมาก</span><span class="sxs-lookup"><span data-stu-id="5be0e-147">Once selected, the **Convenience** data point is a nice shade of orange, and certainly stands out.</span></span>

<span data-ttu-id="5be0e-148">แม้ว่าคุณจะเปลี่ยนชนิดการแสดงภาพ Power BI จะยังคงจดจำสิ่งที่คุณเลือกและทำให้ **ความสะดวกสบาย** ยังคงเป็นสีส้มอยู่</span><span class="sxs-lookup"><span data-stu-id="5be0e-148">Even if you change visualization types, then return, Power BI remembers your selection and keeps **Convenience** orange.</span></span>

<span data-ttu-id="5be0e-149">คุณสามารถเปลี่ยนสีของจุดข้อมูลสำหรับจุดเดียว หลายๆ จุด หรือองค์ประกอบข้อมูลทั้งหมดในการแสดงภาพได้</span><span class="sxs-lookup"><span data-stu-id="5be0e-149">You can change the color of a data point for one, several, or all data elements in the visualization.</span></span> <span data-ttu-id="5be0e-150">บางทีคุณอาจต้องการให้วิชวลของคุณมีสีเหมือนกับสีขององค์กรคุณ สีเหลือง สีเขียว และสีน้ำเงิน</span><span class="sxs-lookup"><span data-stu-id="5be0e-150">Perhaps you want your visual to mimic your corporate colors of yellow, green, and blue.</span></span> 

![แผนภูมิแท่งที่มีแถบที่เป็นสีเขียว สีเหลือง และสีน้ำเงิน](media/service-tips-and-tricks-for-color-formatting/power-bi-corporate.png)

<span data-ttu-id="5be0e-152">มีหลากหลายสิ่งที่คุณสามารถทำได้ด้วยสี</span><span class="sxs-lookup"><span data-stu-id="5be0e-152">There are all sorts of things you can do with colors.</span></span> <span data-ttu-id="5be0e-153">ในส่วนถัดไป เราจะไปดูที่การจัดรูปแบบแบบมีเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="5be0e-153">In the next section, we take a look at conditional formatting.</span></span>

## <a name="conditional-formatting-for-visualizations"></a><span data-ttu-id="5be0e-154">การจัดรูปแบบตามเงื่อนไขสำหรับการแสดงผลข้อมูลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="5be0e-154">Conditional formatting for visualizations</span></span>
<span data-ttu-id="5be0e-155">การแสดงผลข้อมูลด้วยภาพมักจะได้รับประโยชน์จากการตั้งค่าสีแบบไดนามิกที่ยึดตามค่าตัวเลขของเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5be0e-155">Visualizations often benefit from dynamically setting color based on the numeric value of a field.</span></span> <span data-ttu-id="5be0e-156">ด้วยการทำเช่นนี้ คุณสามารถแสดงค่าที่แตกต่างจากค่าที่เคยใช้ได้สำหรับขนาดของแถบ และแสดงค่าสองค่าในกราฟเดียวได้</span><span class="sxs-lookup"><span data-stu-id="5be0e-156">By doing this, you could show a different value than what’s used for the size of a bar, and show two values on a single graph.</span></span> <span data-ttu-id="5be0e-157">หรือคุณสามารถใช้ขั้นตอนนี้เพื่อไฮไลท์จุดข้อมูลเหนือ (หรือใต้) ค่าบางค่าได้ โดยอาจไฮไลท์พื้นที่ของกาทำกำไรที่ต่ำ</span><span class="sxs-lookup"><span data-stu-id="5be0e-157">Or you can use this to highlight data points over (or under) a certain value – perhaps highlighting areas of low profitability.</span></span>

<span data-ttu-id="5be0e-158">ส่วนต่อไปนี้สาธิตวิธีการที่แตกต่างกันในการยึดสีตามค่าตัวเลข</span><span class="sxs-lookup"><span data-stu-id="5be0e-158">The following sections demonstrate different ways to base color on a numeric value.</span></span>

### <a name="base-the-color-of-data-points-on-a-value"></a><span data-ttu-id="5be0e-159">ยึดตามสีของจุดข้อมูลสำหรับค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5be0e-159">Base the color of data points on a value</span></span>
<span data-ttu-id="5be0e-160">หากต้องการเปลี่ยนสีตามค่า ให้เลือกการแสดงผลข้อมูลด้วยภาพเพื่อทำให้ใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="5be0e-160">To change color based on a value, select a visualization to make it active.</span></span> <span data-ttu-id="5be0e-161">เปิดบานหน้าต่างจัดรูปแบบโดยเลือกไอคอนแปรงลูกกลิ้ง และเลือกการ์ด **สีข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="5be0e-161">Open the Formatting pane by selecting the paint roller icon and then choose the **Data colors** card.</span></span> <span data-ttu-id="5be0e-162">ด้านล่าง **สีเริ่มต้น** ให้เลือกไอคอน fx</span><span class="sxs-lookup"><span data-stu-id="5be0e-162">Below **Default color**, select the fx icon.</span></span>  

![เลือกตัวเลือกการจัดรูปแบบตามเงื่อนไข โดยคลิกที่จุดแนวตั้งสามจุด](media/service-tips-and-tricks-for-color-formatting/power-bi-conditional.png)

<span data-ttu-id="5be0e-164">ในบานหน้าต่าง **สีเริ่มต้น** ใช้ดรอปดาวน์เพื่อระบุเขตข้อมูลที่จะใช้การจัดรูปแบบตามเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="5be0e-164">In the **Default color** pane, use the dropdowns to identify the fields to use for conditional formatting.</span></span> <span data-ttu-id="5be0e-165">ในตัวอย่างนี้ เราได้เลือกเขตข้อมูล **ข้อเท็จจริงเกี่ยวกับยอดขาย** > **ผลรวมหน่วย** และเลือกสีฟ้าอ่อนสำหรับการ **ค่าต่ำสุด** และสีน้ำเงินเข้มสำหรับ **ค่าสูงสุด**</span><span class="sxs-lookup"><span data-stu-id="5be0e-165">In this example, we've selected the **Sales fact** > **Total Units** field and selected light blue for the **Lowest value** and dark blue for **Highest value**.</span></span> 

![การตั้งค่าการจัดรูปแบบตามเงื่อนไขตามสีข้อมูล](media/service-tips-and-tricks-for-color-formatting/power-bi-conditional-formatting2-new.png)

![ใช้แผนภูมิคอลัมน์ที่มีสีเริ่มต้น](media/service-tips-and-tricks-for-color-formatting/power-bi-default-colors.png)

<span data-ttu-id="5be0e-168">คุณยังสามารถจัดรูปแบบสีของภาพโดยใช้เขตข้อมูลที่ไม่ได้อยู่ในภาพ</span><span class="sxs-lookup"><span data-stu-id="5be0e-168">You can also format the color of the visual using a field that is not part of the visual.</span></span> <span data-ttu-id="5be0e-169">ในรูปต่อไปนี้ มีการใช้ **%Market Share SPLY YTD**</span><span class="sxs-lookup"><span data-stu-id="5be0e-169">In the following image, **%Market Share SPLY YTD** is being used.</span></span> 

![แผนภูมิคอลัมน์ที่มีสีน้ำเงินหลายเฉด](media/service-tips-and-tricks-for-color-formatting/power-bi-conditional-colors.png)


<span data-ttu-id="5be0e-171">อย่างที่คุณเห็น แม้ว่าเราขายต่อหน่วยได้มากกว่าทั้งในแง่ของ **ประสิทธิภาพ** และ **ระดับสุดยอด** (คอลัมน์ของทั้งคู่ขึ้นสูงกว่า) แต่ **การจัดการดูแล** มี **%Market Share SPLY YTD** ที่ใหญ่กว่า (คอลัมน์มีความเข้มของสีมากกว่า)</span><span class="sxs-lookup"><span data-stu-id="5be0e-171">As you can see, although we've sold more units of both **Productivity** and **Extreme** (their columns are higher), **Moderation** has a larger **%Market Share SPLY YTD** (its column has more color saturation).</span></span>

### <a name="customize-the-colors-used-in-the-color-scale"></a><span data-ttu-id="5be0e-172">กำหนดสีที่ใช้ในระดับสีเอง</span><span class="sxs-lookup"><span data-stu-id="5be0e-172">Customize the colors used in the color scale</span></span>
<span data-ttu-id="5be0e-173">คุณยังสามารถเปลี่ยนวิธีที่ค่าแมปไปยังสีเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="5be0e-173">You can also change the way the values map to these colors.</span></span> <span data-ttu-id="5be0e-174">ในรูปต่อไปนี้ สีสำหรับ **ต่ำสุด** และ **สูงสุด** จะถูกตั้งค่าเป็นสีส้มและสีเขียวตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="5be0e-174">In the following image, the colors for **Minimum** and **Maximum** are set to orange and green, respectively.</span></span>

<span data-ttu-id="5be0e-175">ในรูปภาพแรกนี้โปรดสังเกตว่า แท่งในแผนภูมิแสดงการไล่ระดับสีที่แสดงในแถบดังกล่าว โดยที่ค่าสูงสุดเป็นสีเขียว ค่าต่ำสุดเป็นสีส้ม และแต่ละแถบในระหว่างนี้จะเป็นหนึ่งสีในสเปกตรัมระหว่างสีเขียวและสีส้ม</span><span class="sxs-lookup"><span data-stu-id="5be0e-175">In this first image, notice how the bars in the chart reflect the gradient shown in the bar; the highest value is green, the lowest is orange, and each bar between is colored with a shade of the spectrum between green and orange.</span></span>

![แผนภูมิคอลัมน์แสดงการไล่ระดับสีที่เรียงจากสีเขียวถึงสีส้ม](media/service-tips-and-tricks-for-color-formatting/power-bi-conditional4.png)

<span data-ttu-id="5be0e-177">ตอนนี้ มาดูว่าจะเกิดอะไรขึ้นถ้าเรามีค่าตัวเลขในกล่องค่า **ต่ำสุด** และ **สูงสุด**</span><span class="sxs-lookup"><span data-stu-id="5be0e-177">Now, let’s see what happens if we provide numeric values in the **Minimum** and **Maximum** value boxes.</span></span> <span data-ttu-id="5be0e-178">เลือก **กำหนดเอง** จากดรอปบ็อกซ์สำหรับทั้ง **ต่ำสุด** และ **สูงสุด** และตั้งค่า **ต่ำสุด** เป็น 3,500 และตั้งค่า **สูงสุด** เป็น 6,000</span><span class="sxs-lookup"><span data-stu-id="5be0e-178">Select **Custom** from the dropboxes for both **Minimum** and **Maximum**, and set **Minimum** to 3,500, and set **Maximum** to 6,000.</span></span>

![จัดรูปแบบตามเงื่อนไขด้วยตัวเลข](media/service-tips-and-tricks-for-color-formatting/power-bi-conditional-formatting-numbers.png)

<span data-ttu-id="5be0e-180">ด้วยการตั้งค่าเหล่านั้น จะไม่นำการไล่ระดับสีไปใช้กับค่าบนแผนภูมิที่อยู่ด้านล่าง **ต่ำสุด** หรือสูงกว่า **สูงสุด** อีกต่อไป แถบใดที่มีค่าเหนือค่า **สูงสุด** จะเป็นสีเขียว และแถบใดที่มีค่าที่อยู่ต่ำกว่าค่า **ต่ำสุด** จะเป็นสีแดง</span><span class="sxs-lookup"><span data-stu-id="5be0e-180">By setting those values, gradient is no longer applied to values on the chart that are below **Minimum** or above **Maximum**; any bar with a value over **Maximum** value is colored green, and any bar with a value under **Minimum** value is colored red.</span></span>

![ผลลัพธ์ของจัดรูปแบบตามเงื่อนไขด้วยตัวเลข](media/service-tips-and-tricks-for-color-formatting/power-bi-conditional3.png)

### <a name="use-diverging-color-scales"></a><span data-ttu-id="5be0e-182">ใช้ระดับสีที่แยกออกจากกัน</span><span class="sxs-lookup"><span data-stu-id="5be0e-182">Use diverging color scales</span></span>
<span data-ttu-id="5be0e-183">ในบางครั้งข้อมูลของคุณอาจมีมาตราส่วนแยกออกจากกันอย่างเป็นธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="5be0e-183">Sometimes your data may have a naturally diverging scale.</span></span> <span data-ttu-id="5be0e-184">ตัวอย่างเช่น ช่วงอุณหภูมิมีศูนย์กลางที่เป็นธรรมชาติที่จุดการเยือกแข็ง และมีคะแนนกำไรจากจุดกลาง (ศูนย์) ที่เป็นธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="5be0e-184">For example, a temperate range has a natural center at freezing point, and a profitability score has a natural mid-point (zero).</span></span>

<span data-ttu-id="5be0e-185">หากต้องการใช้ระดับสีที่แยกออกจากกัน ให้เลือกช่องทำเครื่องหมายสำหรับ **เลือกแยกจากกัน**</span><span class="sxs-lookup"><span data-stu-id="5be0e-185">To use diverging color scales, select the checkbox for  **Diverging**.</span></span> <span data-ttu-id="5be0e-186">เมื่อเปิดใช้งาน **เลือกแยกจากกัน** แล้ว ตัวเลือกสีเพิ่มเติมที่เรียกว่า **ศูนย์** จะปรากฏขึ้น ดังที่แสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5be0e-186">When **Diverging** is turned on, an additional color selector, called **Center**, appears, as shown in the following image.</span></span>

![กล่องโต้ตอบสีเริ่มต้นที่มีสเกลสีที่เลือกไว้](media/service-tips-and-tricks-for-color-formatting/power-bi-diverging-colors.png)

<span data-ttu-id="5be0e-188">เมื่อเปิดใช้งานตัวเลื่อน **เลือกแยกจากกัน** แล้ว คุณสามารถตั้งค่าสีต่าง ๆ สำหรับ **ต่ำสุด**, **สูงสุด** และ **ศูนย์** แยกกันได้</span><span class="sxs-lookup"><span data-stu-id="5be0e-188">When the **Diverging** slider is on, you can set the colors for **Minimum**, **Maximum** and **Center** separately.</span></span> <span data-ttu-id="5be0e-189">ในรูปต่อไปนี้ **ศูนย์** ถูกตั้งค่าเป็น .2 สำหรับ **% Market Share SPLY YTD** ดังนั้น แถบที่มีค่ามากกว่า .2 จะมีสีไล่ระดับเป็นสีเขียว และแถบที่น้อยกว่าหนึ่งจะมีสีไล่ระดับเป็นสีแดง</span><span class="sxs-lookup"><span data-stu-id="5be0e-189">In the following image, **Center** is set to .2 for **% Market Share SPLY YTD**, so bars with values above .2 are a gradient shade of green, and bars below one are shades of red.</span></span>

![แผนภูมิคอลัมน์ที่มีแถบสีแดงและสีเขียว](media/service-tips-and-tricks-for-color-formatting/power-bi-diverging.png)

## <a name="add-color-to-table-rows"></a><span data-ttu-id="5be0e-191">เพิ่มสีให้แถวตาราง</span><span class="sxs-lookup"><span data-stu-id="5be0e-191">Add color to table rows</span></span>
<span data-ttu-id="5be0e-192">ตารางและเมทริกซ์มีตัวเลือกมากมายสำหรับการจัดรูปแบบสี</span><span class="sxs-lookup"><span data-stu-id="5be0e-192">Tables and matrixes offer many options for color formatting.</span></span> 

![สกรีนช็อตแสดงตารางที่มีแถวสีขาวและสีเทาสลับกัน](media/service-tips-and-tricks-for-color-formatting/power-bi-table.png)

<span data-ttu-id="5be0e-194">หนึ่งในวิธีที่เร็วที่สุดในการนำสีไปใช้กับตารางหรือเมทริกซ์คือการเปิดแท็บการจัดรูปแบบและเลือก **ลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="5be0e-194">One of the quickest ways to apply color to a table or matrix is to open the Formatting tab and select **Style**.</span></span>  <span data-ttu-id="5be0e-195">ในรูปด้านล่างเราได้เลือก **แถวสีฉูดฉาดที่มีส่วนหัวเป็นตัวหนา**</span><span class="sxs-lookup"><span data-stu-id="5be0e-195">In the image below, we've selected **Bold header flashy rows**.</span></span>

![สกรีนช็อตแสดงตัวเลือกลักษณะของแถวฉูดฉาดส่วนหัวที่เป็นตัวหนาซึ่งทำให้แถวส่วนหน้าเป็นสีดำ และแถวอื่นจะสว่างและเป็นสีเขียวเข้ม](media/service-tips-and-tricks-for-color-formatting/power-bi-table-style.png)

<span data-ttu-id="5be0e-197">ทดลองใช้ตัวเลือกการจัดรูปแบบสีอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="5be0e-197">Experiment with other color formatting options.</span></span> <span data-ttu-id="5be0e-198">ในรูปนี้เราได้เปลี่ยนสีพื้นหลังภายใต้ **ส่วนหัวของคอลัมน์** และเปลี่ยนทั้ง **สีพื้นหลัง** และ **สีพื้นหลังสำรอง** สำหรับ **ค่า** (แถว)</span><span class="sxs-lookup"><span data-stu-id="5be0e-198">In this image, we've changed the background color under **Column headers** and changed both the **Background color** and **Alternate background color** for the **Values** (rows).</span></span>

![สกรีนช็อตแสดงตัวเลือกค่าสำหรับสีพื้นหลังและสีพื้นหลังสำรอง](media/service-tips-and-tricks-for-color-formatting/power-bi-table-rows.png)

## <a name="how-to-undo-in-power-bi"></a><span data-ttu-id="5be0e-200">วิธีการยกเลิกการกระทำใน Power BI</span><span class="sxs-lookup"><span data-stu-id="5be0e-200">How to undo in Power BI</span></span>
<span data-ttu-id="5be0e-201">เช่นเดียวกับบริการและซอฟต์แวร์อื่น ๆ อีกมากมายของ Microsoft, Power BI มีวิธีง่าย ๆ ในการยกเลิกคำสั่งล่าสุดของคุณ</span><span class="sxs-lookup"><span data-stu-id="5be0e-201">Like many other Microsoft services and software, Power BI provides an easy way to undo your last command.</span></span> <span data-ttu-id="5be0e-202">ตัวอย่างเช่น สมมติว่าคุณเปลี่ยนสีของจุดข้อมูลหรือชุดของจุดข้อมูล และคุณไม่ชอบสีดังกล่าวเมื่อปรากฏขึ้นในการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="5be0e-202">For example, let’s say you change the color of a data point, or a series of data points, and you don’t like the color when it appears in the visualization.</span></span> <span data-ttu-id="5be0e-203">คุณจำไม่ได้แน่ชัดว่าสีใดที่ใช้ก่อนหน้านี้ คุณรู้แค่ว่าคุณต้องการให้สีนั้นกลับมา</span><span class="sxs-lookup"><span data-stu-id="5be0e-203">You don’t recall exactly which color it was before, but you know you want that color back!</span></span>

<span data-ttu-id="5be0e-204">หากต้องการ **เลิกทำ** การกระทำล่าสุด หรือสองสามการกระทำล่าสุด สิ่งที่คุณต้องทำคือพิมพ์ CTRL + Z</span><span class="sxs-lookup"><span data-stu-id="5be0e-204">To **undo** your last action, or the last few actions, all you have to do is type CTRL+Z.</span></span>

<span data-ttu-id="5be0e-205">หากต้องการละทิ้งการเปลี่ยนแปลงทั้งหมดที่คุณทำบนการ์ดการจัดรูปแบบ ให้เลือก **แปลงกลับเป็นค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="5be0e-205">To discard all the changes you made on a Formatting card, select **Revert to default**.</span></span>

![การ์ดการจัดรูปแบบจะแสดงการแปลงกลับเป็นค่าเริ่มต้นที่ด้านล่าง](media/service-tips-and-tricks-for-color-formatting/power-bi-revert.png)

## <a name="give-us-your-feedback"></a><span data-ttu-id="5be0e-207">ให้คำติชมของคุณแก่เรา</span><span class="sxs-lookup"><span data-stu-id="5be0e-207">Give us your feedback</span></span>
<span data-ttu-id="5be0e-208">คุณมีคำแนะนำที่คุณต้องการแชร์หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="5be0e-208">Do you have a tip you’d like to share?</span></span> <span data-ttu-id="5be0e-209">โปรดส่งมาหาเรา และเราจะดูว่าสามารถรวมไว้ที่นี่ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="5be0e-209">Please send it our way, and we’ll see about including it here.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5be0e-210">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="5be0e-210">Next steps</span></span>
[<span data-ttu-id="5be0e-211">เริ่มใช้งานด้วยคุณสมบัติแกนและการจัดรูปแบบสี</span><span class="sxs-lookup"><span data-stu-id="5be0e-211">Getting started with color formatting and axis properties</span></span>](service-getting-started-with-color-formatting-and-axis-properties.md)

<span data-ttu-id="5be0e-212">[การแชร์รายงาน](../collaborate-share/service-share-reports.md)</span><span class="sxs-lookup"><span data-stu-id="5be0e-212">[Sharing reports](../collaborate-share/service-share-reports.md).</span></span>

