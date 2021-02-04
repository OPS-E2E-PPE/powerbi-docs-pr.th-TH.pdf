---
title: บทช่วยสอนเกี่ยวกับ Smart Narratives (คำบรรยายอัจฉริยะ)
description: 'บทช่วยสอน: สร้างการแสดงภาพสรุปคำบรรยายอัจฉริยะใน Power BI'
author: aphilip94
ms.author: anphil
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 11/06/2020
ms.custom: video-01UrT-z37sw
LocalizationGroup: Visualizations
ms.openlocfilehash: 43b2e9c33bf420c7446aa2eb198048101704a1ba
ms.sourcegitcommit: 396633fc5f7cff1f7d518f558b20043b2e05a513
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/14/2021
ms.locfileid: "98191946"
---
# <a name="create-smart-narrative-summaries-preview"></a><span data-ttu-id="e6144-103">สร้างสรุปคำบรรยายอัจฉริยะ (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="e6144-103">Create smart narrative summaries (preview)</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]    

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="e6144-104">การแสดงภาพคำบรรยายอัจฉริยะช่วยให้คุณสามารถสรุปวิชวลและรายงานได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="e6144-104">The smart narrative visualization helps you quickly summarize visuals and reports.</span></span> <span data-ttu-id="e6144-105">ซึ่งคุณสามารถกำหนดข้อมูลเชิงลึกที่เกี่ยวข้องได้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="e6144-105">It provides relevant innovative insights that you can customize.</span></span>

![สกรีนช็อตแสดงการสรุปคำบรรยายอัจฉริยะทางด้านขวาของรายงาน](media/power-bi-visualization-smart-narratives/1.png)

<span data-ttu-id="e6144-107">ใช้การสรุปคำบรรยายอัจฉริยะในรายงานของคุณเพื่อระบุประเด็นสำคัญ ชี้แนวโน้ม และเพื่อแก้ไขภาษาและรูปแบบสำหรับผู้ชมเฉพาะกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="e6144-107">Use smart narrative summaries in your reports to address key takeaways, to point out trends, and to edit the language and format for a specific audience.</span></span> <span data-ttu-id="e6144-108">ใน PowerPoint คุณสามารถเพิ่มคำบรรยายที่มีการอัปเดตในทุกครั้งที่รีเฟรชได้ แทนการวางสกรีนช็อตประเด็นสำคัญของรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="e6144-108">In PowerPoint, instead of pasting a screenshot of your report's key takeaways, you can add narratives that are updated with every refresh.</span></span> <span data-ttu-id="e6144-109">ผู้ชมของคุณสามารถการสรุปเพื่อทำความเข้าใจข้อมูล เข้าใจสาระสำคัญได้รวดเร็วยิ่งขึ้น และอธิบายข้อมูลให้กับผู้อื่นได้</span><span class="sxs-lookup"><span data-stu-id="e6144-109">Your audience can use the summaries to understand the data, get to key points faster, and explain the data to others.</span></span>

>[!NOTE]
> <span data-ttu-id="e6144-110">เนื่องจากคุณลักษณะคำบรรยายอัจฉริยะอยู่ในการแสดงตัวอย่าง คุณจะต้องเปิดใช้งานหากต้องการใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="e6144-110">Because the smart narrative feature is in preview, you must turn it on if you want to use it.</span></span> <span data-ttu-id="e6144-111">ใน Power BI ไปที่ **ไฟล์** > **ตัวเลือกและการตั้งค่า** > **ตัวเลือก** > **คุณลักษณะตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="e6144-111">In Power BI, go to **File** > **Options and Settings** > **Options** > **Preview features**.</span></span> <span data-ttu-id="e6144-112">จากนั้นเลือก **วิชวลคำบรรยายอัจฉริยะ**</span><span class="sxs-lookup"><span data-stu-id="e6144-112">Then select **Smart narrative visual**.</span></span>
>
>![สกรีนช็อตแสดงตัวเลือก Power BI](media/power-bi-visualization-smart-narratives/2.png)



## <a name="get-started"></a><span data-ttu-id="e6144-115">เริ่มใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e6144-115">Get started</span></span> 
<span data-ttu-id="e6144-116">ชม Justyna แสดงวิธีใช้เรื่องเล่าที่ชาญฉลาด จากนั้นลองใช้ด้วยตัวเองโดยใช้บทช่วยสอนด้านล่างวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="e6144-116">Watch Justyna show you how to use smart narratives, then try it out yourself using the tutorial, below the video.</span></span>  <span data-ttu-id="e6144-117">หากต้องการทำตามบทช่วยสอนนี้ ให้ดาวน์โหลด [ไฟล์ตัวอย่าง](https://github.com/microsoft/powerbi-desktop-samples/blob/main/Monthly%20Desktop%20Blog%20Samples/2020/2020SU09%20Blog%20Demo%20-%20September.pbix) ของสถานการณ์การขายออนไลน์</span><span class="sxs-lookup"><span data-stu-id="e6144-117">To follow along with this tutorial, download the [sample file](https://github.com/microsoft/powerbi-desktop-samples/blob/main/Monthly%20Desktop%20Blog%20Samples/2020/2020SU09%20Blog%20Demo%20-%20September.pbix) of an online-sales scenario.</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/01UrT-z37sw" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<span data-ttu-id="e6144-118">ในบานหน้าต่าง **การแสดงภาพ** เลือกไอคอน **คำบรรยายอัจฉริยะ** เพื่อสร้างสรุปโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e6144-118">In the **Visualizations** pane, select the **Smart narrative** icon to automatically generate a summary.</span></span>

![สกรีนช็อตแสดงบานหน้าต่างการแสดงภาพ](media/power-bi-visualization-smart-narratives/3.png)

<span data-ttu-id="e6144-121">คุณจะเห็นคำบรรยายที่สร้างขึ้นโดยยึดตามวิชวลทั้งหมดบนหน้า</span><span class="sxs-lookup"><span data-stu-id="e6144-121">You see a narrative that's based on all of the visuals on the page.</span></span> <span data-ttu-id="e6144-122">ตัวอย่างเช่นในไฟล์ตัวอย่าง คำบรรยายอัจฉริยะสามารถสร้างข้อมูลสรุปของวิชวลของรายงาน โดยระบุรายได้ การเยี่ยมชมเว็บไซต์ และการขายได้ โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e6144-122">For example, in the sample file, smart narratives can automatically generate a summary of the report's visuals that address revenue, website visits, and sales.</span></span> <span data-ttu-id="e6144-123">Power BI วิเคราะห์แนวโน้มโดยอัตโนมัติเพื่อแสดงให้เห็นว่าทั้งรายได้และการเยี่ยมชมมีการเติบโตขึ้น</span><span class="sxs-lookup"><span data-stu-id="e6144-123">Power BI automatically analyzes trends to show that revenue and visits have both grown.</span></span> <span data-ttu-id="e6144-124">นอกจากนี้ยังคำนวณการเติบโต ซึ่งในกรณีนี้คือ 72 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="e6144-124">It even calculates growth, which in this case is 72 percent.</span></span>
 
![สกรีนช็อตแสดงวิธีการสร้างสรุปคำบรรยายอัจฉริยะ](media/power-bi-visualization-smart-narratives/4.gif)
 
<span data-ttu-id="e6144-126">หากต้องการสร้างคำบรรยายอัจฉริยะของวิชวล ให้คลิกขวาแล้วเลือก **สรุป**</span><span class="sxs-lookup"><span data-stu-id="e6144-126">To generate a smart narrative of a visualization, right-click it and then select **Summarize**.</span></span> <span data-ttu-id="e6144-127">ตัวอย่างเช่นในไฟล์ตัวอย่าง ลองสรุปแผนภูมิกระจายที่แสดงการประกอบธุรกรรมต่างๆ</span><span class="sxs-lookup"><span data-stu-id="e6144-127">For example, in the sample file, try summarizing a scatter chart that shows various transactions.</span></span> <span data-ttu-id="e6144-128">Power BI วิเคราะห์ข้อมูลและแสดงว่าเมืองหรือภูมิภาคใดมีรายได้สูงสุดต่อธุรกรรม และมีจำนวนธุรกรรมสูงสุด</span><span class="sxs-lookup"><span data-stu-id="e6144-128">Power BI analyzes the data and shows which city or region has the highest revenue per transaction and the highest number of transactions.</span></span> <span data-ttu-id="e6144-129">คำบรรยายอัจฉริยะยังแสดงช่วงค่าที่คาดไว้สำหรับเมตริกเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="e6144-129">The smart narrative also shows the expected range of values for these metrics.</span></span> <span data-ttu-id="e6144-130">คุณจะเห็นว่าเมืองส่วนใหญ่ทำรายได้ได้น้อยกว่า $45 ต่อธุรกรรม และมีธุรกรรมน้อยกว่า 10 รายการ</span><span class="sxs-lookup"><span data-stu-id="e6144-130">You see that most cities produce less than $45 per transaction and have fewer than 10 transactions.</span></span>
 
  
![สกรีนช็อตแสดงคำบรรยายอัจฉริยะที่สรุปแผนภูมิกระจาย](media/power-bi-visualization-smart-narratives/5.gif)
 
## <a name="edit-the-summary"></a><span data-ttu-id="e6144-132">แก้ไขสรุป</span><span class="sxs-lookup"><span data-stu-id="e6144-132">Edit the summary</span></span>
 
<span data-ttu-id="e6144-133">สรุปคำบรรยายอัจฉริยะสามารถปรับแต่งได้หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="e6144-133">The smart narrative summary is highly customizable.</span></span> <span data-ttu-id="e6144-134">คุณสามารถแก้ไขหรือเพิ่มข้อความที่มีอยู่โดยใช้คำสั่งกล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="e6144-134">You can edit or add to the existing text by using the text box commands.</span></span> <span data-ttu-id="e6144-135">ตัวอย่างเช่น คุณสามารถทำให้ข้อความเป็นตัวหนาหรือเปลี่ยนสีข้อความได้</span><span class="sxs-lookup"><span data-stu-id="e6144-135">For example, you can make the text bold or change its color.</span></span>
 
![สกรีนช็อตแสดงคำสั่งการจัดรูปแบบข้อความบนแถบเครื่องมือ](media/power-bi-visualization-smart-narratives/6.png)
  
<span data-ttu-id="e6144-137">หากต้องการปรับแต่งการสรุปและเพิ่มข้อมูลเชิงลึกของคุณเอง ให้ใช้ *ค่าแบบไดนามิก*</span><span class="sxs-lookup"><span data-stu-id="e6144-137">To customize the summary or add your own insights, use *dynamic values*.</span></span> <span data-ttu-id="e6144-138">คุณสามารถโยงข้อความไปยังเขตข้อมูลและหน่วยวัดที่มีอยู่ หรือใช้ภาษาธรรมชาติเพื่อกำหนดหน่วยวัดใหม่ที่จะโยงไปยังข้อความ</span><span class="sxs-lookup"><span data-stu-id="e6144-138">You can map text to existing fields and measures or use natural language to define a new measure to map to text.</span></span> <span data-ttu-id="e6144-139">ตัวอย่างเช่น เมื่อต้องการเพิ่มข้อมูลเกี่ยวกับจำนวนของรายการที่ส่งคืนในไฟล์ตัวอย่าง ให้ทำการเพิ่มค่า</span><span class="sxs-lookup"><span data-stu-id="e6144-139">For example, to add information about the number of returned items in the sample file, add a value.</span></span> 

<span data-ttu-id="e6144-140">ในขณะที่คุณพิมพ์ชื่อค่า คุณสามารถเลือกจากรายการคำแนะนำตามที่คุณทำในวิชวลคำถามและคำตอบได้</span><span class="sxs-lookup"><span data-stu-id="e6144-140">As you type a value name, you can choose from a list of suggestions as you do in a Q&A visual.</span></span> <span data-ttu-id="e6144-141">ดังนั้นนอกเหนือจากการถามคำถามเกี่ยวกับข้อมูลของคุณในวิชวลคำถามและคำตอบแล้ว ตอนนี้คุณสามารถสร้างการคำนวณของคุณเองโดยไม่ต้องใช้ Data Analysis Expressions (DAX)</span><span class="sxs-lookup"><span data-stu-id="e6144-141">So, in addition to asking questions of your data in a Q&A visual, you can now create your own calculations without even using Data Analysis Expressions (DAX).</span></span> 
  
![สกรีนช็อตแสดงวิธีการสร้างค่าไดนามิกสำหรับการแสดงภาพคำบรรยายอัจฉริยะ](media/power-bi-visualization-smart-narratives/7.gif)
  
<span data-ttu-id="e6144-143">คุณยังสามารถจัดรูปแบบค่าไดนามิกได้</span><span class="sxs-lookup"><span data-stu-id="e6144-143">You can also format dynamic values.</span></span> <span data-ttu-id="e6144-144">ตัวอย่างเช่นในไฟล์ตัวอย่าง คุณสามารถแสดงค่าเป็นสกุลเงิน ระบุตำแหน่งทศนิยม และเลือกตัวคั่นสำหรับหลักพัน</span><span class="sxs-lookup"><span data-stu-id="e6144-144">For example, in the sample file, you can show values as currency, specify decimal places, and choose a separator for thousands.</span></span> 
   
![สกรีนช็อตแสดงวิธีการจัดรูปแบบค่าไดนามิก](media/power-bi-visualization-smart-narratives/8.gif)
   
<span data-ttu-id="e6144-146">เมื่อต้องการจัดรูปแบบค่าแบบไดนามิก ให้เลือกค่าในสรุปเพื่อดูตัวเลือกการแก้ไขของคุณบนแท็บ **ตรวจสอบ** หรือในกล่องข้อความที่อยู่ถัดจากค่าที่คุณต้องการแก้ไข ให้เลือกปุ่มแก้ไข</span><span class="sxs-lookup"><span data-stu-id="e6144-146">To format a dynamic value, select the value in the summary to see your editing options on the **Review** tab. Or in the text box, next to the value that you want to edit, select the edit button.</span></span> 
   
![สกรีนช็อตแสดงกล่องข้อความที่มีแท็บค่าที่เลือกไว้](media/power-bi-visualization-smart-narratives/9.png)
   
<span data-ttu-id="e6144-149">คุณยังสามารถใช้แท็บ **ตรวจสอบ** เพื่อตรวจสอบ ลบ หรือนำค่าที่กำหนดไว้ก่อนหน้านี้มาใช้ใหม่ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="e6144-149">You can also use the **Review** tab to review, delete, or reuse previously defined values.</span></span> <span data-ttu-id="e6144-150">เลือกเครื่องหมายบวก (+) เพื่อแทรกค่าลงในข้อมูลสรุป</span><span class="sxs-lookup"><span data-stu-id="e6144-150">Select the plus sign (+) to insert the value into the summary.</span></span> <span data-ttu-id="e6144-151">คุณยังสามารถแสดงค่าที่สร้างขึ้นโดยอัตโนมัติโดยการเปิดตัวเลือกที่ด้านล่างของแท็บ **ตรวจสอบ**</span><span class="sxs-lookup"><span data-stu-id="e6144-151">You can also show automatically generated values by turning on the option at the bottom of the **Review** tab.</span></span>

<span data-ttu-id="e6144-152">บางครั้งสัญลักษณ์สรุปที่ซ่อนอยู่จะปรากฏในคำบรรยายอัจฉริยะ</span><span class="sxs-lookup"><span data-stu-id="e6144-152">Sometimes a hidden-summary symbol appears in the smart narrative.</span></span> <span data-ttu-id="e6144-153">ซึ่งแสดงว่าข้อมูลและตัวกรองปัจจุบันไม่มีผลลัพธ์สำหรับค่า</span><span class="sxs-lookup"><span data-stu-id="e6144-153">It indicates that current data and filters produce no result for the value.</span></span> <span data-ttu-id="e6144-154">สรุปจะว่างเปล่าเมื่อไม่มีข้อมูลเชิงลึกที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e6144-154">A summary is empty when no insights are available.</span></span> <span data-ttu-id="e6144-155">ตัวอย่างเช่นในแผนภูมิเส้นของไฟล์ตัวอย่าง สรุปของค่าสูงและต่ำอาจว่างเปล่าเมื่อเส้นของแผนภูมิเป็นแบบแบน</span><span class="sxs-lookup"><span data-stu-id="e6144-155">For example, in the sample file's line chart, a summary of high and low values might be empty when the chart's line is flat.</span></span> <span data-ttu-id="e6144-156">แต่สรุปอาจปรากฏขึ้นภายใต้เงื่อนไขอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="e6144-156">But the summary might appear under other conditions.</span></span> <span data-ttu-id="e6144-157">สัญลักษณ์สรุปที่ซ่อนไว้จะมองเห็นได้เฉพาะเมื่อคุณพยายามแก้ไขสรุป</span><span class="sxs-lookup"><span data-stu-id="e6144-157">Hidden-summary symbols are visible only when you try to edit a summary.</span></span>


![สกรีนช็อตแสดงสองสัญลักษณ์ที่สรุปที่ซ่อนไว้ภายในสรุปคำบรรยายอัจฉริยะ](media/power-bi-visualization-smart-narratives/10.png)
   
## <a name="visual-interactions"></a><span data-ttu-id="e6144-159">การโต้ตอบกับวิชวล</span><span class="sxs-lookup"><span data-stu-id="e6144-159">Visual interactions</span></span>
<span data-ttu-id="e6144-160">สรุปเป็นระบบแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="e6144-160">A summary is dynamic.</span></span> <span data-ttu-id="e6144-161">ซึ่งสามารถอัปเดตข้อความและค่าไดนามิกที่เพิ่มเข้ามาได้โดยอัตโนมัติเมื่อคุณใช้ตัวกรองแบบข้าม</span><span class="sxs-lookup"><span data-stu-id="e6144-161">It automatically updates the generated text and dynamic values when you cross-filter.</span></span> <span data-ttu-id="e6144-162">ตัวอย่างเช่น ถ้าคุณเลือกผลิตภัณฑ์อิเล็กทรอนิกส์ในแผนภูมิโดนัทของไฟล์ตัวอย่าง ส่วนที่เหลือของรายงานจะเปลี่ยนเป็นตัวกรองแบบข้ามและข้อสรุปจะยังกรองข้ามเพื่อโฟกัสในผลิตภัณฑ์อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="e6144-162">For example, if you select electronics products in the sample file's donut chart, the rest of the report is cross-filtered, and the summary is also cross-filtered to focus on the electronics products.</span></span>  

<span data-ttu-id="e6144-163">ในกรณีนี้ การเยี่ยมชมและรายได้มีแนวโน้มที่แตกต่างกัน ดังนั้นข้อความสรุปจึงได้รับการอัปเดตเพื่อแสดงให้เห็นในเรื่องนี้</span><span class="sxs-lookup"><span data-stu-id="e6144-163">In this case, the visits and revenues have different trends, so the summary text is updated to reflect the trends.</span></span> <span data-ttu-id="e6144-164">จำนวนของค่าที่ส่งกลับที่เราเพิ่มจะได้รับการอัปเดตเป็น $4196</span><span class="sxs-lookup"><span data-stu-id="e6144-164">The count-of-returns value that we added is updated to $4196.</span></span> <span data-ttu-id="e6144-165">เมื่อคุณใช้การกรองข้าม จะสามารถอัปเดตส่วนการสรุปที่ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="e6144-165">Empty summaries can be updated when you cross-filter.</span></span>
   
![สกรีนช็อตแสดงวิธีที่การเลือกในแผนภูมิสามารถกรองข้ามสรุปได้](media/power-bi-visualization-smart-narratives/11.gif)
   
<span data-ttu-id="e6144-167">คุณยังสามารถทำการกรองในขั้นสูงกว่า</span><span class="sxs-lookup"><span data-stu-id="e6144-167">You can also do more advanced filtering.</span></span> <span data-ttu-id="e6144-168">ตัวอย่างเช่นในไฟล์ตัวอย่าง ดูที่วิชวลของแนวโน้มสำหรับหลายผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e6144-168">For example, in the sample file, look at the visual of trends for multiple products.</span></span> <span data-ttu-id="e6144-169">ถ้าคุณสนใจเฉพาะในแนวโน้มสำหรับไตรมาสใดไตรมาสหนึ่ง ให้เลือกจุดข้อมูลที่เกี่ยวข้องเพื่ออัปเดตสรุปสำหรับแนวโน้มนั้น</span><span class="sxs-lookup"><span data-stu-id="e6144-169">If you're interested only in a trend for a certain quarter, then select the relevant data points to update the summary for that trend.</span></span>
   
![สกรีนช็อตแสดงวิธีการเลือกเส้นแนวโน้มเพื่อกรองสรุปเพื่อแสดงเฉพาะแนวโน้มนั้น](media/power-bi-visualization-smart-narratives/12.gif)
   
## <a name="limitations"></a><span data-ttu-id="e6144-171">ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="e6144-171">Limitations</span></span>

<span data-ttu-id="e6144-172">คุณลักษณะคำบรรยายอัจฉริยะไม่สนับสนุนฟังก์ชันการทำงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e6144-172">The smart narrative feature doesn't support the following functionality:</span></span>
- <span data-ttu-id="e6144-173">ปักหมุดเข้าแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="e6144-173">Pinning to a dashboard</span></span> 
- <span data-ttu-id="e6144-174">การใช้ค่าแบบไดนามิกและการจัดรูปแบบตามเงื่อนไข (ตัวอย่างเช่น ชื่อเรื่องที่ผูกกับข้อมูล)</span><span class="sxs-lookup"><span data-stu-id="e6144-174">Using dynamic values and conditional formatting (for example, data bound title)</span></span>
- <span data-ttu-id="e6144-175">Azure Analysis Services และ AS ในองค์กร</span><span class="sxs-lookup"><span data-stu-id="e6144-175">Azure Analysis Services, on-premises AS</span></span>
- <span data-ttu-id="e6144-176">KPI, การ์ด, การ์ดหลายแถว, แผนที่, ตาราง, เมตริก, วิชวล R หรือ วิชวล Python, วิชวลแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="e6144-176">KPIs, cards, multiple-row cards, maps, tables, matrices, R visuals or Python visuals, custom visuals</span></span> 
- <span data-ttu-id="e6144-177">สรุปของวิชวลที่มีการจัดกลุ่มคอลัมน์ตามคอลัมน์อื่น และวิชวลที่สร้างขึ้นบนเขตข้อมูลของกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="e6144-177">Summaries of visuals whose columns are grouped by other columns and for visuals that are built on a data group field</span></span> 
- <span data-ttu-id="e6144-178">การกรองข้ามนอกวิชวล</span><span class="sxs-lookup"><span data-stu-id="e6144-178">Cross-filtering out of a visual</span></span>
- <span data-ttu-id="e6144-179">การเปลี่ยนชื่อค่าไดนามิกหรือการแก้ไขค่าไดนามิกโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e6144-179">Renaming dynamic values or editing automatically generated dynamic values</span></span>
- <span data-ttu-id="e6144-180">สรุปของวิชวลที่ประกอบด้วยการคำนวณพร้อมใช้ เช่น QnA เลขคณิต และเปอร์เซ็นต์ของยอดรวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e6144-180">Summaries of visuals that contain on-the-fly calculations like QnA arithmetic and percentage of grand total</span></span> 
- [<span data-ttu-id="e6144-181">เวลาการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="e6144-181">Calculation groups</span></span>](/analysis-services/tabular-models/calculation-groups)
   

