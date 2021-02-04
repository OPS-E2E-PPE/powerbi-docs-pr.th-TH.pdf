---
title: ใช้ตัววิเคราะห์ประสิทธิภาพในการตรวจสอบประสิทธิภาพขององค์ประกอบรายงานใน Power BI Desktop
description: ค้นหาประสิทธิภาพของวิชวลและองค์ประกอบรายงานในแง่ของการใช้ทรัพยากรและการตอบสนอง
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 01/23/2020
LocalizationGroup: Create reports
ms.openlocfilehash: a622da545d4fa9fca8b9478f6d5293d2b34296e9
ms.sourcegitcommit: 396633fc5f7cff1f7d518f558b20043b2e05a513
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/14/2021
ms.locfileid: "98191716"
---
# <a name="use-performance-analyzer-to-examine-report-element-performance"></a><span data-ttu-id="1a9c8-103">ใช้ตัววิเคราะห์ประสิทธิภาพในการตรวจสอบประสิทธิภาพขององค์ประกอบรายงาน</span><span class="sxs-lookup"><span data-stu-id="1a9c8-103">Use Performance Analyzer to examine report element performance</span></span>

<span data-ttu-id="1a9c8-104">ใน **Power BI Desktop** คุณสามารถค้นหาว่าองค์ประกอบรายงานแต่ละรายการของคุณ เช่น วิชวลและสูตร DAX ทำงานอย่างไร</span><span class="sxs-lookup"><span data-stu-id="1a9c8-104">In **Power BI Desktop** you can find out how each of your report elements, such as visuals and DAX formulas, are performing.</span></span> <span data-ttu-id="1a9c8-105">การใช้ **ตัววิเคราะห์ประสิทธิภาพ** คุณสามารถดูและบันทึกข้อมูลบันทึกที่วัดว่าแต่ละองค์ประกอบของรายงานมีประสิทธิภาพอย่างไรเมื่อผู้ใช้โต้ตอบกับองค์ประกอบดังกล่าว และประสิทธิภาพการทำงานด้านใดที่ใช้ทรัพยากรมากที่สุด (หรือน้อยที่สุด)</span><span class="sxs-lookup"><span data-stu-id="1a9c8-105">Using the **Performance Analyzer**, you can see and record logs that measure how each of your report elements performs when users interact with them, and which aspects of their performance are most (or least) resource intensive.</span></span>

![ตัววิเคราะห์ประสิทธิภาพ](media/desktop-performance-analyzer/performance-analyzer-01.png)

<span data-ttu-id="1a9c8-107">ตัววิเคราะห์ประสิทธิภาพตรวจสอบและแสดงระยะเวลาที่จำเป็นสำหรับการอัปเดตหรือรีเฟรชวิชวลทั้งหมดเมื่อการโต้ตอบของผู้ใช้เริ่มต้นขึ้น และนำเสนอข้อมูลเพื่อให้คุณสามารถดู เจาะลึกรายละเอียด หรือส่งออกผลลัพธ์ได้</span><span class="sxs-lookup"><span data-stu-id="1a9c8-107">Performance Analyzer inspects and displays the duration necessary for updating or refreshing all visuals that user interactions initiate, and presents the information so you can view, drill down, or export the results.</span></span> <span data-ttu-id="1a9c8-108">ตัววิเคราะห์ประสิทธิภาพสามารถช่วยให้คุณระบุวิชวลที่มีผลกระทบต่อประสิทธิภาพการทำงานของรายงานของคุณ และระบุเหตุผลสำหรับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="1a9c8-108">Performance Analyzer can help you identify visuals that are impacting the performance of your reports, and identify the reason for the impact.</span></span>

## <a name="displaying-the-performance-analyzer-pane"></a><span data-ttu-id="1a9c8-109">แสดงบานหน้าต่างตัววิเคราะห์ประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="1a9c8-109">Displaying the Performance Analyzer pane</span></span>

<span data-ttu-id="1a9c8-110">ใน **Power BI Desktop** ให้เลือกริบบอน **มุมมอง**</span><span class="sxs-lookup"><span data-stu-id="1a9c8-110">In **Power BI Desktop** select the **View** ribbon.</span></span> <span data-ttu-id="1a9c8-111">ในพื้นที่ **แสดง** ของริบบอน **มุมมอง** คุณสามารถเลือกช่องทำเครื่องหมายถัดจาก **ตัววิเคราะห์ประสิทธิภาพ** เพื่อแสดงบานหน้าต่างตัววิเคราะห์ประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="1a9c8-111">In the **Show** area of the **View** ribbon you can select the checkbox next to **Performance Analyzer** to display the Performance Analyzer pane.</span></span>

![เลือกตัววิเคราะห์ประสิทธิภาพในริบบอนมุมมอง](media/desktop-performance-analyzer/performance-analyzer-02.png)

<span data-ttu-id="1a9c8-113">เมื่อเลือกแล้ว ตัววิเคราะห์ประสิทธิภาพจะแสดงในบานหน้าต่างของตัวเองทางด้านขวาของพื้นที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="1a9c8-113">Once selected, the Performance Analyzer is displayed in its own pane, to the right of the report canvas.</span></span>

## <a name="using-performance-analyzer"></a><span data-ttu-id="1a9c8-114">ใช้ตัววิเคราะห์ประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="1a9c8-114">Using Performance Analyzer</span></span>

<span data-ttu-id="1a9c8-115">ตัววิเคราะห์ประสิทธิภาพวัดเวลาการประมวลผล (รวมถึงเวลาในการสร้างหรืออัปเดตวิชวล) ที่จำเป็นในการอัปเดตองค์ประกอบรายงานที่เริ่มต้นขึ้นอันเป็นผลมาจากการโต้ตอบของผู้ใช้ที่ทำให้เกิดการเรียกใช้คิวรี</span><span class="sxs-lookup"><span data-stu-id="1a9c8-115">Performance analyzer measures the processing time (including the time to create or update a visual) required to update report elements initiated as a result of any user interaction that results in running a query.</span></span> <span data-ttu-id="1a9c8-116">ตัวอย่างเช่น การปรับตัวแบ่งส่วนข้อมูลจำเป็นต้องมีการปรับแต่งวิชวลของตัวแบ่งส่วนข้อมูล คิวรีที่จะส่งไปยังแบบจำลองข้อมูล และวิชวลที่ได้รับผลกระทบจะต้องมีการอัปเดตอันเป็นผลมาจากการตั้งค่าใหม่</span><span class="sxs-lookup"><span data-stu-id="1a9c8-116">For example, adjusting a slicer requires the slicer visual to be modified, a query to be sent to the data model, and affected visuals that must be updated as a result of the new settings.</span></span> 

<span data-ttu-id="1a9c8-117">เมื่อต้องการให้ตัววิเคราะห์ประสิทธิภาพเริ่มต้นการบันทึก เพียงแค่เลือก **เริ่มการบันทึก**</span><span class="sxs-lookup"><span data-stu-id="1a9c8-117">To have Performance Analyzer begin recording, simply select **Start recording**</span></span>

![เริ่มการบันทึก](media/desktop-performance-analyzer/performance-analyzer-03.png)

<span data-ttu-id="1a9c8-119">การดำเนินการใดก็ตามที่คุณทำในรายงานจะแสดงขึ้นและบันทึกในบานหน้าต่างตัววิเคราะห์ประสิทธิภาพตามลำดับที่มีการโหลดวิชวลโดย Power BI</span><span class="sxs-lookup"><span data-stu-id="1a9c8-119">Any actions you take in the report are displayed and logged in the Performance Analyzer pane, in the order that the visual is loaded by Power BI.</span></span> <span data-ttu-id="1a9c8-120">ตัวอย่างเช่น คุณอาจมีรายงานที่ผู้ใช้แจ้งว่าการรีเฟรชใช้เวลานาน</span><span class="sxs-lookup"><span data-stu-id="1a9c8-120">For example, perhaps you have a report that users have said takes a long time to refresh.</span></span> <span data-ttu-id="1a9c8-121">หรือการแสดงวิชวลในรายงานบางวิชวลใช้เวลานานเมื่อมีการปรับแถบเลื่อน</span><span class="sxs-lookup"><span data-stu-id="1a9c8-121">Or certain visuals in a report take a long time to display when a slider is adjusted.</span></span> <span data-ttu-id="1a9c8-122">ตัววิเคราะห์ประสิทธิภาพสามารถบอกคุณได้ว่าวิชวลใดเป็นสาเหตุ และระบุลักษณะของวิชวลที่ใช้เวลานานที่สุดในการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="1a9c8-122">Performance analyzer can tell you which visual is the culprit, and identifies which aspects of the visual is taking the longest duration to process.</span></span> 

<span data-ttu-id="1a9c8-123">เมื่อคุณเริ่มการบันทึกแล้ว ปุ่ม **เริ่มการบันทึก** จะเป็นสีเทา (ไม่ทำงานเนื่องจากคุณได้เริ่มการบันทึกแล้ว) และปุ่ม **หยุด** ทำงานอยู่</span><span class="sxs-lookup"><span data-stu-id="1a9c8-123">Once you start recording, the **Start recording** button is grayed out (inactive, since you've already begun recording) and the **Stop** button is active.</span></span> 

<span data-ttu-id="1a9c8-124">ตัววิเคราะห์ประสิทธิภาพจะรวบรวมและแสดงข้อมูลการวัดประสิทธิภาพในแบบเรียลไทม์</span><span class="sxs-lookup"><span data-stu-id="1a9c8-124">Performance analyzer collects and displays the performance measurement information in real time.</span></span> <span data-ttu-id="1a9c8-125">ดังนั้นแต่ละครั้งที่คุณคลิกบนวิชวล ย้ายตัวแบ่งส่วนข้อมูล หรือโต้ตอบในวิธีอื่น ตัววิเคราะห์ประสิทธิภาพจะแสดงผลลัพธ์ของประสิทธิภาพการทำงานในบานหน้าต่างทันที</span><span class="sxs-lookup"><span data-stu-id="1a9c8-125">So each time you click on a visual, move a slicer, or interact in any other way, Performance Analyzer immediately displays the performance results in its pane.</span></span>

<span data-ttu-id="1a9c8-126">ถ้าบานหน้าต่างมีข้อมูลมากกว่าที่สามารถแสดงได้ แถบเลื่อนจะปรากฏขึ้นเพื่อนำทางไปยังข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1a9c8-126">If the pane has more information than can be displayed, a scroll bar appears to navigate to additional information.</span></span>

<span data-ttu-id="1a9c8-127">การโต้ตอบแต่ละรายการจะมีตัวระบุส่วนในบานหน้าต่าง อธิบายการดำเนินการที่เริ่มต้นรายการบันทึก</span><span class="sxs-lookup"><span data-stu-id="1a9c8-127">Each interaction has a section identifier in the pane, describing the action that initiated the log entries.</span></span> <span data-ttu-id="1a9c8-128">ในรูปภาพต่อไปนี้ การโต้ตอบคือ ผู้ใช้ปรับตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1a9c8-128">In the following image, the interaction was that the users changed a slicer.</span></span>

![ส่วนขึ้นอยู่กับชนิดของการโต้ตอบ](media/desktop-performance-analyzer/performance-analyzer-04.png)

<span data-ttu-id="1a9c8-130">ข้อมูลบันทึกของแต่ละวิชวลจะประกอบด้วยเวลาที่ใช้ (ระยะเวลา) ในการดำเนินงานตามหมวดหมู่ต่อไปนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="1a9c8-130">Each visual's log information includes the time spent (duration) to complete the following categories of tasks:</span></span>

* <span data-ttu-id="1a9c8-131">**คิวรี DAX** - ถ้าจำเป็นต้องมีคิวรี DAX นี่คือเวลาระหว่างวิชวลที่ส่งคิวรี และสำหรับ Analysis Services เพื่อส่งคืนผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="1a9c8-131">**DAX query** - if a DAX query was required, this is the time between the visual sending the query, and for Analysis Services to return the results.</span></span>
* <span data-ttu-id="1a9c8-132">**การแสดงวิชวล** - เวลาที่ต้องใช้ในการวาดวิชวลลงบนหน้าจอ รวมถึงเวลาที่ต้องใช้เพื่อดึงรูปภาพของเว็บหรือการเข้ารหัสภูมิศาสตร์</span><span class="sxs-lookup"><span data-stu-id="1a9c8-132">**Visual display** - time required for the visual to draw on the screen, including time required to retrieve any web images or geocoding.</span></span> 
* <span data-ttu-id="1a9c8-133">**อื่น ๆ** - เวลาที่วิชวลต้องการสำหรับการจัดเตรียมคิวรี รอให้วิชวลอื่นเสร็จสมบูรณ์ หรือดำเนินการประมวลผลเบื้องหลังอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="1a9c8-133">**Other** - time required by the visual for preparing queries, waiting for other visuals to complete, or performing other background processing.</span></span>

<span data-ttu-id="1a9c8-134">ค่า **ช่วงเวลา (ms)** แสดงความแตกต่างระหว่างประทับเวลา *เริ่มต้น* และ *สิ้นสุด* สำหรับแต่ละการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="1a9c8-134">The **Duration (ms)** values indicate the difference between a *start* and *end* timestamp for each operation.</span></span> <span data-ttu-id="1a9c8-135">พื้นที่ทำงานและการดำเนินการวิชวลส่วนใหญ่ทำงานตามลำดับบนเธรดอินเทอร์เฟซผู้ใช้เดียว ซึ่งใช้ร่วมกันหลายการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="1a9c8-135">Most canvas and visual operations execute sequentially on a single User Interface thread, which is shared by multiple operations.</span></span> <span data-ttu-id="1a9c8-136">ช่วงเวลาที่รายงานรวมประกอบด้วยที่อยู่ในคิวขณะที่การดำเนินการอื่นเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="1a9c8-136">The reported durations include time spent queued while other operations complete.</span></span> <span data-ttu-id="1a9c8-137">[ตัวอย่างตัววิเคราะห์ประสิทธิภาพ](https://github.com/microsoft/powerbi-desktop-samples/tree/main/Performance%20Analyzer)บน GitHub และ[เอกสาร](https://github.com/microsoft/powerbi-desktop-samples/blob/main/Performance%20Analyzer/Power%20BI%20Performance%20Analyzer%20Export%20File%20Format.docx)ที่เกี่ยวข้องให้รายละเอียดเกี่ยวกับวิธีการสร้างวิชวลข้อมูลคิวรี และวิธีการแสดงผลข้อมูลดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="1a9c8-137">The [Performance Analyzer sample](https://github.com/microsoft/powerbi-desktop-samples/tree/main/Performance%20Analyzer) on GitHub and its associated [documentation](https://github.com/microsoft/powerbi-desktop-samples/blob/main/Performance%20Analyzer/Power%20BI%20Performance%20Analyzer%20Export%20File%20Format.docx) provide details about how visuals query data, and how they render.</span></span>


![องค์ประกอบของข้อมูลบันทึก](media/desktop-performance-analyzer/performance-analyzer-06.png)

<span data-ttu-id="1a9c8-139">หลังจากที่คุณโต้ตอบกับองค์ประกอบของรายงานที่คุณต้องการวัดผลด้วยตัววิเคราะห์ประสิทธิภาพ แล้วคุณสามารถเลือกปุ่ม **หยุด**</span><span class="sxs-lookup"><span data-stu-id="1a9c8-139">After you've interacted with elements of the report you want to measure with Performance Analyzer, you can select the **Stop** button.</span></span> <span data-ttu-id="1a9c8-140">ข้อมูลประสิทธิภาพยังคงอยู่ในบานหน้าต่างหลังจากคุณเลือก **หยุด** เพื่อให้คุณนำไปวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="1a9c8-140">The performance information remains in the pane after you select **Stop** for you to analyze.</span></span>

<span data-ttu-id="1a9c8-141">หากต้องการล้างข้อมูลในบานหน้าต่างตัววิเคราะห์ประสิทธิภาพ ให้เลือก **ล้าง**</span><span class="sxs-lookup"><span data-stu-id="1a9c8-141">To clear out the information in the Performance Analyzer pane, select **Clear**.</span></span> <span data-ttu-id="1a9c8-142">ข้อมูลทั้งหมดจะถูกลบออกและไม่ได้รับการบันทึกเมื่อคุณเลือก **ล้าง**</span><span class="sxs-lookup"><span data-stu-id="1a9c8-142">All information is erased and is not saved when you select **Clear**.</span></span> <span data-ttu-id="1a9c8-143">ดูหัวข้อถัดไปเพื่อเรียนรู้วิธีการบันทึกข้อมูลในรายการบันทึก</span><span class="sxs-lookup"><span data-stu-id="1a9c8-143">See the next section to learn how to save information in logs.</span></span> 

## <a name="refreshing-visuals"></a><span data-ttu-id="1a9c8-144">การรีเฟรชวิชวล</span><span class="sxs-lookup"><span data-stu-id="1a9c8-144">Refreshing visuals</span></span>

<span data-ttu-id="1a9c8-145">คุณสามารถเลือก **รีเฟรชวิชวล** ในบานหน้าต่างตัววิเคราะห์ประสิทธิภาพเพื่อรีเฟรชวิชวลทั้งหมดในหน้าปัจจุบันของรายงาน และด้วยเหตุนี้ ตัววิเคราะห์ประสิทธิภาพจึงรวบรวมข้อมูลเกี่ยวกับวิชวลดังกล่าวทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="1a9c8-145">You can select **Refresh visuals** in the Performance Analyzer pane to refresh all visuals on the current page of the report, and thereby have Performance Analyzer gather information about all such visuals.</span></span>

<span data-ttu-id="1a9c8-146">คุณยังสามารถรีเฟรชวิชวลแต่ละอันแยกต่างหากได้</span><span class="sxs-lookup"><span data-stu-id="1a9c8-146">You can also refresh individual visuals.</span></span> <span data-ttu-id="1a9c8-147">เมื่อตัววิเคราะห์ประสิทธิภาพกำลังบันทึก คุณสามารถเลือก **รีเฟรชวิชวลนี้** ที่มุมขวาบนของแต่ละวิชวล เพื่อรีเฟรชวิชวลนั้น และเก็บข้อมูลประสิทธิภาพของวิชวลดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="1a9c8-147">When Performance Analyzer is recording, you can select **Refresh this visual** found in the top-right corner of each visual, to refresh that visual, and capture its performance information.</span></span>

![รีเฟรชวิชวลแต่ละอันแยกต่างหาก](media/desktop-performance-analyzer/performance-analyzer-07.png)

## <a name="saving-performance-information"></a><span data-ttu-id="1a9c8-149">การบันทึกข้อมูลประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="1a9c8-149">Saving performance information</span></span>

<span data-ttu-id="1a9c8-150">คุณสามารถบันทึกข้อมูลที่ตัววิเคราะห์ประสิทธิภาพสร้างเกี่ยวกับรายงานได้โดยการเลือกปุ่ม **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="1a9c8-150">You can save the information that Performance Analyzer creates about a report by selecting the **Export** button.</span></span> <span data-ttu-id="1a9c8-151">การเลือก **ส่งออก** จะสร้างไฟล์ .json ที่มีข้อมูลจากบานหน้าต่างตัววิเคราะห์ประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="1a9c8-151">Selecting **Export** creates a .json file with information from the Performance Analyzer pane.</span></span> 

![บันทึกไฟล์บันทึกสำหรับตัววิเคราะห์ประสิทธิภาพ](media/desktop-performance-analyzer/performance-analyzer-05.png)


## <a name="next-steps"></a><span data-ttu-id="1a9c8-153">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="1a9c8-153">Next steps</span></span>
<span data-ttu-id="1a9c8-154">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ **Power BI Desktop** และวิธีการเริ่มต้นใช้งาน ตรวจสอบบทความต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1a9c8-154">For more information about **Power BI Desktop**, and how to get started, check out the following articles.</span></span>

* [<span data-ttu-id="1a9c8-155">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="1a9c8-155">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="1a9c8-156">ภาพรวมคิวรี ด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="1a9c8-156">Query Overview with Power BI Desktop</span></span>](../transform-model/desktop-query-overview.md)
* [<span data-ttu-id="1a9c8-157">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="1a9c8-157">Data Sources in Power BI Desktop</span></span>](../connect-data/desktop-data-sources.md)
* [<span data-ttu-id="1a9c8-158">เชื่อมต่อกับข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="1a9c8-158">Connect to Data in Power BI Desktop</span></span>](../connect-data/desktop-connect-to-data.md)
* [<span data-ttu-id="1a9c8-159">จัดรูปทรง และรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="1a9c8-159">Shape and Combine Data with Power BI Desktop</span></span>](../connect-data/desktop-shape-and-combine-data.md)
* [<span data-ttu-id="1a9c8-160">งานคิวรี่ทั่วไปใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="1a9c8-160">Common Query Tasks in Power BI Desktop</span></span>](../transform-model/desktop-common-query-tasks.md)   

<span data-ttu-id="1a9c8-161">สำหรับข้อมูลเกี่ยวกับตัวอย่างตัววิเคราะห์ประสิทธิภาพ ให้ดูแหล่งข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1a9c8-161">For information about the Performance Analyzer sample, check out the following resources.</span></span>

* [<span data-ttu-id="1a9c8-162">ตัวอย่างตัววิเคราะห์ประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="1a9c8-162">Performance Analyzer sample</span></span>](https://github.com/microsoft/powerbi-desktop-samples/tree/main/Performance%20Analyzer)
* [<span data-ttu-id="1a9c8-163">เอกสารตัวอย่างตัววิเคราะห์ประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="1a9c8-163">Performance Analyzer sample documentation</span></span>](https://github.com/microsoft/powerbi-desktop-samples/blob/main/Performance%20Analyzer/Power%20BI%20Performance%20Analyzer%20Export%20File%20Format.docx)
