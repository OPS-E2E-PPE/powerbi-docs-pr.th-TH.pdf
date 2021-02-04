---
title: ใช้บานหน้าต่างการวิเคราะห์ใน Power BI Desktop
description: สร้างสายการอ้างอิงแบบไดนามิกสำหรับวิชวลใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: how-to
ms.date: 01/10/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 1437e680ac7dc4114d68bd534ba8ec93dd8ae508
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96416059"
---
# <a name="use-the-analytics-pane-in-power-bi-desktop"></a><span data-ttu-id="44b41-103">ใช้บานหน้าต่างการวิเคราะห์ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="44b41-103">Use the Analytics pane in Power BI Desktop</span></span>

<span data-ttu-id="44b41-104">ด้วยแผง **การวิเคราะห์** ใน Power BI Desktop คุณสามารถเพิ่ม *สายการอ้างอิง* แบบไดนามิกกับวิชวล และเน้นให้เห็นแนวโน้มที่สำคัญหรือข้อมูลเชิงลึกได้</span><span class="sxs-lookup"><span data-stu-id="44b41-104">With the **Analytics** pane in Power BI Desktop, you can add dynamic *reference lines* to visuals, and provide focus for important trends or insights.</span></span> <span data-ttu-id="44b41-105">ไอคอนและแผง **การวิเคราะห์** จะอยู่ในพื้นที่ของ **การแสดงผลด้วยภาพ** ของ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="44b41-105">The **Analytics** icon and pane is found in the **Visualizations** area of Power BI Desktop.</span></span>

![แผงการวิเคราะห์ การแสดงผลด้วยภาพ Power BI Desktop](media/desktop-analytics-pane/analytics-pane_1.png)

> [!NOTE]
> <span data-ttu-id="44b41-107">บานหน้าต่าง **การวิเคราะห์** จะปรากฏเฉพาะเมื่อคุณเลือกวิชวลบนพื้นที่ทำงานของ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="44b41-107">The **Analytics** pane only appears when you select a visual on the Power BI Desktop canvas.</span></span>

## <a name="search-within-the-analytics-pane"></a><span data-ttu-id="44b41-108">ค้นหาภายในบานหน้าต่างการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="44b41-108">Search within the Analytics pane</span></span>

<span data-ttu-id="44b41-109">เริ่มตั้งแต่การเผยแพร่เดือนกุมภาพันธ์ 2018 ของ **Power BI Desktop** (เวอร์ชั่น 2.55.5010.201 หรือใหม่กว่า) คุณสามารถค้นหาภายในแผง **การวิเคราะห์** ซึ่งเป็นส่วนย่อยของแผงการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="44b41-109">Beginning with the February 2018 release of Power BI Desktop (version 2.55.5010.201 or later), you can search within the **Analytics** pane, which is a subsection of the **Visualizations** pane.</span></span> <span data-ttu-id="44b41-110">กล่องค้นหาจะปรากฏขึ้นเมื่อคุณเลือกไอคอน **การวิเคราะห์**</span><span class="sxs-lookup"><span data-stu-id="44b41-110">The search box appears when you select the **Analytics** icon.</span></span>

![กล่องค้นหา แผงการวิเคราะห์ การแสดงผลด้วยภาพ Power BI Desktop](media/desktop-analytics-pane/analytics-pane_1b.png)

## <a name="use-the-analytics-pane"></a><span data-ttu-id="44b41-112">การใช้บานหน้าต่างการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="44b41-112">Use the Analytics pane</span></span>

<span data-ttu-id="44b41-113">ด้วยแผง **การวิเคราะห์** คุณสามารถสร้างสายการอ้างอิงแบบไดนามิกชนิดต่างๆ :</span><span class="sxs-lookup"><span data-stu-id="44b41-113">With the **Analytics** pane, you can create the following types of dynamic reference lines:</span></span>

* <span data-ttu-id="44b41-114">เส้นคงที่แกน X</span><span class="sxs-lookup"><span data-stu-id="44b41-114">X-Axis constant line</span></span>
* <span data-ttu-id="44b41-115">เส้นคงที่แกน Y</span><span class="sxs-lookup"><span data-stu-id="44b41-115">Y-Axis constant line</span></span>
* <span data-ttu-id="44b41-116">เส้นต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="44b41-116">Min line</span></span>
* <span data-ttu-id="44b41-117">เส้นสูงสุด</span><span class="sxs-lookup"><span data-stu-id="44b41-117">Max line</span></span>
* <span data-ttu-id="44b41-118">เส้นเฉลี่ย</span><span class="sxs-lookup"><span data-stu-id="44b41-118">Average line</span></span>
* <span data-ttu-id="44b41-119">เส้นกึ่งกลาง</span><span class="sxs-lookup"><span data-stu-id="44b41-119">Median line</span></span>
* <span data-ttu-id="44b41-120">เส้นเปอร์เซ็นต์ไทล์</span><span class="sxs-lookup"><span data-stu-id="44b41-120">Percentile line</span></span>
* <span data-ttu-id="44b41-121">แรเงาสมมาตร</span><span class="sxs-lookup"><span data-stu-id="44b41-121">Symmetry shading</span></span>

> [!NOTE]
> <span data-ttu-id="44b41-122">บางบรรทัดไม่พร้อมใช้งานสำหรับทุกชนิดของวิชวล</span><span class="sxs-lookup"><span data-stu-id="44b41-122">Not all lines are available for all visual types.</span></span>

<span data-ttu-id="44b41-123">ส่วนต่อไปนี้แสดงให้เห็นว่า คุณสามารถใช้บานหน้าต่าง **การวิเคราะห์** และสายการอ้างอิงแบบไดนามิกในการแสดงภาพของคุณได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="44b41-123">The following sections show how you can use the **Analytics** pane and dynamic reference lines in your visualizations.</span></span>

<span data-ttu-id="44b41-124">เพื่อดูรายการ สายการอ้างอิงแบบไดนามิก ที่มีสำหรับแต่ละวิชาล ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="44b41-124">To view the available dynamic reference lines for a visual, follow these steps:</span></span>

1. <span data-ttu-id="44b41-125">เลือกหรือสร้างวิชวล จากนั้นเลือกไอคอน **การวิเคราะห์** จากส่วน **การจัดรูปแบบการแสดงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="44b41-125">Select or create a visual, then select the **Analytics** icon from the **Visualizations** section.</span></span>

    ![ดูการวิเคราะห์สำหรับวิชวล แผงการแสดงผลด้วยภาพ Power BI Desktop](media/desktop-analytics-pane/analytics-pane_2.png)

2. <span data-ttu-id="44b41-127">เลือกชนิดของเส้นที่คุณต้องการสร้าง เพื่อขยายตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="44b41-127">Select the type of line you want to create to expand its options.</span></span> <span data-ttu-id="44b41-128">ในกรณีนี้ เราจะเลือก **เส้นเฉลี่ย**</span><span class="sxs-lookup"><span data-stu-id="44b41-128">In this case, we'll select **Average line**.</span></span>

    ![เส้นเฉลี่ย แผงการวิเคราะห์ การแสดงผลด้วยภาพ Power BI Desktop](media/desktop-analytics-pane/analytics-pane_3.png)

3. <span data-ttu-id="44b41-130">เมื่อต้องการสร้างเส้นใหม่ เลือก **+&nbsp;เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="44b41-130">To create a new line, select **+&nbsp;Add**.</span></span> <span data-ttu-id="44b41-131">จากนั้นคุณสามารถตั้งชื่อบรรทัดได้</span><span class="sxs-lookup"><span data-stu-id="44b41-131">Then you can name the line.</span></span> <span data-ttu-id="44b41-132">คลิกสองครั้งที่กล่องข้อความและใส่ชื่อของคุณ</span><span class="sxs-lookup"><span data-stu-id="44b41-132">Double-click the text box and enter your name.</span></span>

    <span data-ttu-id="44b41-133">ในตอนนี้คุณมีตัวเลือกสำหรับเส้นของคุณทั้งหมดแล้ว</span><span class="sxs-lookup"><span data-stu-id="44b41-133">Now you have all sorts of options for your line.</span></span> <span data-ttu-id="44b41-134">คุณสามารถระบุ **สี**,เปอร์เซ็นต์ **ความโปร่งใส** **ลักษณะเส้น** และ **ตำแหน่ง** (เทียบกับองค์ประกอบข้อมูลของภาพ)</span><span class="sxs-lookup"><span data-stu-id="44b41-134">You can specify its **Color**, **Transparency** percentage, **Line style**, and **Position** (compared to the visual's data elements).</span></span> <span data-ttu-id="44b41-135">คุณยังสามารถเลือกว่าจะรวม  **ป้ายชื่อข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="44b41-135">You may also choose whether to include the **Data label**.</span></span> <span data-ttu-id="44b41-136">เมื่อต้องการระบุการวัดผลด้วยภาพที่จะยึดตามเส้นของคุณ ให้เลือกรายการ **หน่วยวัด** ข้างล่าง ซึ่งจะถูกเติมโดยอัตโนมัติด้วยองค์ประกอบข้อมูลจากวิชวล</span><span class="sxs-lookup"><span data-stu-id="44b41-136">To specify the visual measure to base your line upon, select the **Measure** dropdown list, which is automatically populated with data elements from the visual.</span></span> <span data-ttu-id="44b41-137">เราจะเลือก **วัฒนธรรม** เป็นหน่วยวัด และตั้งชื่อว่า *วัฒนธรรมเฉลี่ย* และกำหนดตัวเลือกอื่นๆ สองสามตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="44b41-137">Here we'll select **Culture** as the measure, label it *Average of Culture*, and customize a few of the other options.</span></span>

    ![เส้นเฉลี่ยของวัฒนธรรมเฉลี่ย แผงการวิเคราะห์ การแสดงผลด้วยภาพ Power BI Desktop](media/desktop-analytics-pane/analytics-pane_4.png)

4. <span data-ttu-id="44b41-139">ถ้าคุณต้องการให้ป้ายชื่อข้อมูลปรากฏ เปลี่ยน **ป้ายชื่อข้อมูล** จาก **ปิด** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="44b41-139">If you want to have a data label appear, change **Data label** from **Off** to **On**.</span></span> <span data-ttu-id="44b41-140">เมื่อคุณทำเช่นนั้น คุณจะมีตัวเลือกสำหรับป้ายชื่อข้อมูลเพิ่มขึ้นอีก สำหรับป้ายชื่อข้อมุลของคุณ</span><span class="sxs-lookup"><span data-stu-id="44b41-140">When you do so, you get a whole host of additional options for your data label.</span></span>

    ![การตั้งค่าป้ายชื่อข้อมูล แผงการวิเคราะห์ การแสดงผลด้วยภาพ Power BI Desktop](media/desktop-analytics-pane/analytics-pane_5.png)

5. <span data-ttu-id="44b41-142">สังเกตว่ามีตัวเลขปรากฏถัดจากรายการ **เส้นเฉลี่ย** ในบานหน้าต่าง **การวิเคราะห์**</span><span class="sxs-lookup"><span data-stu-id="44b41-142">Notice the number that appears next to the **Average line** item in the **Analytics** pane.</span></span> <span data-ttu-id="44b41-143">ซึ่งบอกคุณว่ามีเส้นแบบไดนามิกแล้วกี่เส้นในวิชวลของคุณ และเป็นชนิดใดบ้าง</span><span class="sxs-lookup"><span data-stu-id="44b41-143">That tells you how many dynamic lines you currently have on your visual, and of which type.</span></span> <span data-ttu-id="44b41-144">ถ้าเราเพิ่ม **เส้นสูงสุด** สำหรับ **ค่าใช้จ่ายการดำรงชีพ** แผง **การวิเคราะห์** แสดงว่า ตอนนี้เรายังมี **เส้นสูงสุด** แบบไดนามิกอีกหนึ่งเส้นที่ใช้ในวิชวลนี้</span><span class="sxs-lookup"><span data-stu-id="44b41-144">If we add a **Max line** for **Affordability**, the **Analytics** pane shows that we now also have a **Max line** dynamic reference line applied to this visual.</span></span>

    ![เส้นสูงสุดและเส้นเฉลี่ยทั้งหทด แผงการวิเคราะห์ การแสดงผลด้วยภาพ Power BI Desktop](media/desktop-analytics-pane/analytics-pane_6.png)

<span data-ttu-id="44b41-146">ถ้าวิชวลที่คุณเลือกไม่สามารถมีสายการการอ้างอิงแบบไดนามิกที่ใช้กับ (ในกรณีนี้ วิชวล **แผนที่**) คุณจะเห็นข้อความต่อไปนี้เมื่อคุณเลือแผง **การวิเคราะห์**</span><span class="sxs-lookup"><span data-stu-id="44b41-146">If the visual you've selected can't have dynamic reference lines applied to it (in this case, a **Map** visual), you'll see the following message when you select the **Analytics** pane.</span></span>

![การวิเคราะห์ที่ไม่พร้อมใช้งานสำหรับวิชวลแผนที่ แผงการวิเคราะห์ การแสดงผลด้วยภาพ Power BI Desktop](media/desktop-analytics-pane/analytics-pane_7.png)

<span data-ttu-id="44b41-148">คุณสามารถเน้นได้โดยการสร้างสายการอ้างอิงแบบไดนามิก ด้วแผง **การวิเคราะห์**</span><span class="sxs-lookup"><span data-stu-id="44b41-148">You can highlight many interesting insights by creating dynamic reference lines with the **Analytics** pane.</span></span>

<span data-ttu-id="44b41-149">เรากำลังวางแผนคุณลักษณะและความสามารถเพิ่มเติม รวมถึงขยายวิชวลที่สามารถมีสายการการอ้างอิงแบบไดนามิกได้</span><span class="sxs-lookup"><span data-stu-id="44b41-149">We're planning more features and capabilities, including expanding which visuals can have dynamic reference lines applied to them.</span></span> <span data-ttu-id="44b41-150">ตรวจสอบย้อนกลับบ่อยครั้งเพื่อดูว่ามีอะไรใหม่</span><span class="sxs-lookup"><span data-stu-id="44b41-150">Check back often to see what's new.</span></span>

## <a name="apply-forecasting"></a><span data-ttu-id="44b41-151">การใช้การพยากรณ์</span><span class="sxs-lookup"><span data-stu-id="44b41-151">Apply forecasting</span></span>

<span data-ttu-id="44b41-152">ถ้าคุณมีข้อมูลเวลาในแหล่งข้อมูลของคุณ คุณสามารถใช้ฟีเจอร์ *การคาดการณ์* ได้</span><span class="sxs-lookup"><span data-stu-id="44b41-152">If you have time data in your data source, you can use the *forecasting* feature.</span></span> <span data-ttu-id="44b41-153">เพียงแค่เลือกวิชวล จากนั้นขยายส่วน **การคาดการณ์** ของแผง  **การวิเคราะห์**</span><span class="sxs-lookup"><span data-stu-id="44b41-153">Just select a visual, then expand the **Forecast** section of the **Analytics** pane.</span></span> <span data-ttu-id="44b41-154">คุณสามารถระบุค่ามากมายเพื่อปรับเปลี่ยนการพยากรณ์ เช่น **คาดการณ์ความยาว** หรือ **ช่วงความเชื่อมั่น**</span><span class="sxs-lookup"><span data-stu-id="44b41-154">You may specify many inputs to modify the forecast, such as the **Forecast length** or the **Confidence interval**.</span></span> <span data-ttu-id="44b41-155">รูปภาพต่อไปนี้แสดงวิชวลของเส้นที่ใช้การคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="44b41-155">The following image shows a basic line visual with forecasting applied.</span></span> <span data-ttu-id="44b41-156">ใช้จินตนาการของคุณ (และเล่นกับการคาดการณ์) เพื่อดูว่าอาจนำไปใช้กับโมเดลของคุณได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="44b41-156">Use your imagination (and play around with forecasting) to see how it may apply to your models.</span></span>

![ฟีเจอร์การคาดการณ์ แผงการวิเคราะห์ การแสดงผลด้วยภาพ Power BI Desktop](media/desktop-analytics-pane/analytics-pane_8.png)

> [!NOTE]
> <span data-ttu-id="44b41-158">ฟีเจอร์การคาดการณ์จะพร้อมใช้งานสำหรับวิชวลแผนภูมิเส้นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="44b41-158">The forecasting feature is only available for line chart visuals.</span></span>

## <a name="limitations"></a><span data-ttu-id="44b41-159">ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="44b41-159">Limitations</span></span>

<span data-ttu-id="44b41-160">ความสามารถในการใช้สายการอ้างอิงแบบไดนามิก จะขึ้นกับชนิดของวิชวลที่ใช้</span><span class="sxs-lookup"><span data-stu-id="44b41-160">The ability to use dynamic reference lines is based on the type of visual being used.</span></span> <span data-ttu-id="44b41-161">รายการต่อไปนี้อธิบายข้อจำกัดเหล่านี้โดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="44b41-161">The following lists describe these limitations more specifically.</span></span>

<span data-ttu-id="44b41-162">คุณอาจใช้ *เส้นคงที่แกน x* *เส้นคงที่แกน  y* และ *แรเงาแบบสมมาตร* บนวิชวลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="44b41-162">You may use *x-axis constant line*, *y-axis constant line*, and *symmetry shading* on the following visual:</span></span>

* <span data-ttu-id="44b41-163">แผนภูมิกระจาย</span><span class="sxs-lookup"><span data-stu-id="44b41-163">Scatter chart</span></span>

<span data-ttu-id="44b41-164">การใช้ *เส้นคงที่* *เส้นต่ำสุด* *เส้นสูงสุด* *เส้นเฉลี่ย* *เส้นตรงกลาง* และ *เส้นเปอร์เซ็นต์ไทล์* พร้อมใช้งานบนวิชวลเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="44b41-164">Use of *constant line*, *min line*, *max line*, *average line*, *median line*, and *percentile line* is available on these visuals:</span></span>

* <span data-ttu-id="44b41-165">แผนภูมิพื้นที่</span><span class="sxs-lookup"><span data-stu-id="44b41-165">Area chart</span></span>
* <span data-ttu-id="44b41-166">แผนภูมิแท่งแบบกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="44b41-166">Clustered bar chart</span></span>
* <span data-ttu-id="44b41-167">แผนภูมิคอลัมน์แบบกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="44b41-167">Clustered column chart</span></span>
* <span data-ttu-id="44b41-168">แผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="44b41-168">Line chart</span></span>
* <span data-ttu-id="44b41-169">แผนภูมิกระจาย</span><span class="sxs-lookup"><span data-stu-id="44b41-169">Scatter chart</span></span>

<span data-ttu-id="44b41-170">วิชวลต่อไปนี้สามารถใช้เฉพาะ *เส้นคงที่* จากบานหน้าต่าง **การวิเคราะห์**:</span><span class="sxs-lookup"><span data-stu-id="44b41-170">The following visuals can use only a *constant line* from the **Analytics** pane:</span></span>

* <span data-ttu-id="44b41-171">แผนภูมิพื้นที่แบบเรียงซ้อน</span><span class="sxs-lookup"><span data-stu-id="44b41-171">Stacked area chart</span></span>
* <span data-ttu-id="44b41-172">แผนภูมิแท่งแบบเรียงซ้อน</span><span class="sxs-lookup"><span data-stu-id="44b41-172">Stacked bar chart</span></span>
* <span data-ttu-id="44b41-173">แผนภูมิคอลัมน์แบบเรียงซ้อน</span><span class="sxs-lookup"><span data-stu-id="44b41-173">Stacked column chart</span></span>
* <span data-ttu-id="44b41-174">แผนภูมิน้ำตก</span><span class="sxs-lookup"><span data-stu-id="44b41-174">Waterfall chart</span></span>
* <span data-ttu-id="44b41-175">แผนภูมิแท่งแบบเรียงซ้อน 100%</span><span class="sxs-lookup"><span data-stu-id="44b41-175">100% Stacked bar chart</span></span>
* <span data-ttu-id="44b41-176">แผนภูมิคอลัมน์แบบเรียงซ้อน 100%</span><span class="sxs-lookup"><span data-stu-id="44b41-176">100% Stacked column chart</span></span>

<span data-ttu-id="44b41-177">วิชวลต่อไปนี้สามารถใช้  *เส้นแนวโน้ม* ถ้ามีข้อมูลเวลา:</span><span class="sxs-lookup"><span data-stu-id="44b41-177">The following visuals can use a *trend line* if there's time data:</span></span>

* <span data-ttu-id="44b41-178">แผนภูมิพื้นที่</span><span class="sxs-lookup"><span data-stu-id="44b41-178">Area chart</span></span>
* <span data-ttu-id="44b41-179">แผนภูมิคอลัมน์แบบกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="44b41-179">Clustered column chart</span></span>
* <span data-ttu-id="44b41-180">แผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="44b41-180">Line chart</span></span>
* <span data-ttu-id="44b41-181">เส้นและแผนภูมิคอลัมน์แบบกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="44b41-181">Line and clustered column chart</span></span>

<span data-ttu-id="44b41-182">ในที่สุด คุณไม่สามารถนำเส้นแบบไดนามิกใดๆ ไปใช้กับวิชวลจำนวนมากได้ ในขณะนี้รวมถึง (แต่ไม่จำกัดเพียง):</span><span class="sxs-lookup"><span data-stu-id="44b41-182">Lastly, you can't currently apply any dynamic lines to many visuals, including (but not limited to):</span></span>

* <span data-ttu-id="44b41-183">แผนภูมิกรวย</span><span class="sxs-lookup"><span data-stu-id="44b41-183">Funnel</span></span>
* <span data-ttu-id="44b41-184">เส้นและแผนภูมิคอลัมน์แบบกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="44b41-184">Line and clustered column chart</span></span>
* <span data-ttu-id="44b41-185">เส้นและแผนภูมิคอลัมน์แบบเรียงซ้อน</span><span class="sxs-lookup"><span data-stu-id="44b41-185">Line and stacked column chart</span></span>
* <span data-ttu-id="44b41-186">แผนภูมิริบบอน</span><span class="sxs-lookup"><span data-stu-id="44b41-186">Ribbon chart</span></span>
* <span data-ttu-id="44b41-187">วิชวลที่ไม่ใช่คาร์ทีเซียน เช่น แผนภูมิโดนัท เครื่องวัด เมทริกซ์ แผนภูมิวงกลมและตาราง</span><span class="sxs-lookup"><span data-stu-id="44b41-187">Non-Cartesian visuals, such as Donut chart, Gauge, Matrix, Pie chart, and Table</span></span>

<span data-ttu-id="44b41-188">*เส้นเปอร์เซ็นต์ไทล์* มีใช้งานเฉพาะเมื่อใช้ข้อมูลนำเข้าใน Power BI Desktop หรือเมื่อเชื่อมต่อสดไปยังโมเดลเซิร์ฟเวอร์ที่ดำเนินการ  **Analysis Service 2016** หรือภายหลัง **Azure Analysis Services** หรือชุดข้อมูลบนบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="44b41-188">The *percentile line* is only available when using imported data in Power BI Desktop or when connected live to a model on a server that's running **Analysis Service 2016** or later, **Azure Analysis Services**, or a dataset on the Power BI service.</span></span>

## <a name="next-steps"></a><span data-ttu-id="44b41-189">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="44b41-189">Next steps</span></span>

<span data-ttu-id="44b41-190">คุณสามารถทำการเรียงลำดับของของต่างๆ ด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="44b41-190">You can do all sorts of things with Power BI Desktop.</span></span> <span data-ttu-id="44b41-191">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับขีดความสามารถ กรุณาดูแหล่งทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="44b41-191">For more information on its capabilities, check out the following resources:</span></span>

* [<span data-ttu-id="44b41-192">มีอะไรใหม่ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="44b41-192">What's new in Power BI Desktop</span></span>](../fundamentals/desktop-latest-update.md)
* [<span data-ttu-id="44b41-193">รับ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="44b41-193">Get Power BI Desktop</span></span>](../fundamentals/desktop-get-the-desktop.md)
* [<span data-ttu-id="44b41-194">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="44b41-194">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="44b41-195">ภาพรวมคำถามด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="44b41-195">Query overview with Power BI Desktop</span></span>](desktop-query-overview.md)
* [<span data-ttu-id="44b41-196">ชนิดข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="44b41-196">Data types in Power BI Desktop</span></span>](../connect-data/desktop-data-types.md)
* [<span data-ttu-id="44b41-197">จัดรูปร่างและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="44b41-197">Shape and combine data with Power BI Desktop</span></span>](../connect-data/desktop-shape-and-combine-data.md)
* [<span data-ttu-id="44b41-198">ใช้งานทั่วไปใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="44b41-198">Perform common tasks in Power BI Desktop</span></span>](desktop-common-query-tasks.md)
