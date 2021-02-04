---
title: สรุปการรีเฟรชสำหรับ Power BI
description: เรียนรู้วิธีการใช้สรุปการรีเฟรชใน Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 08/27/2020
LocalizationGroup: Data refresh
ms.openlocfilehash: 285bc76ddb0a0afa571fba06096358c22781a121
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410792"
---
# <a name="refresh-summaries-for-power-bi"></a><span data-ttu-id="51a33-103">สรุปการรีเฟรชสำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="51a33-103">Refresh summaries for Power BI</span></span>

<span data-ttu-id="51a33-104">หน้า **สรุปการรีเฟรช** ของ Power BI ที่พบในพอร์ทัลผู้ดูแลระบบ Power BI มีการควบคุมและข้อมูลเชิงลึกเกี่ยวกับตารางเวลาการรีเฟรช ความจุ และการทับซ้อนของตารางเวลาการรีเฟรชที่อาจมี</span><span class="sxs-lookup"><span data-stu-id="51a33-104">The Power BI **refresh summaries** page, found in the Power BI Admin portal, provides control and insight into your refresh schedules, capacities, and potential refresh schedule overlaps.</span></span> <span data-ttu-id="51a33-105">คุณสามารถใช้หน้าสรุปการรีเฟรชเพื่อตรวจสอบว่าคุณควรปรับตารางเวลาการรีเฟรชหรือไม่ เรียนรู้รหัสข้อผิดพลาดที่เกี่ยวข้องกับปัญหาการรีเฟรช และจัดการการกำหนดตารางเวลาการรีเฟรชข้อมูลของคุณอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="51a33-105">You can use the refresh summaries page to determine whether you should adjust refresh schedules, learn error codes associated with refresh issues, and properly manage your data refresh scheduling.</span></span> 

<span data-ttu-id="51a33-106">หน้าสรุปการรีเฟรชมีสองมุมมองได้แก่:</span><span class="sxs-lookup"><span data-stu-id="51a33-106">The refresh summaries page has two views:</span></span>

* <span data-ttu-id="51a33-107">**ประวัติ**- แสดงประวัติสรุปการรีเฟรชสำหรับความจุ Power BI Premium ที่คุณเป็นผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="51a33-107">**History** - displays the refresh summary history for Power BI Premium capacities for which you are an administrator.</span></span>

* <span data-ttu-id="51a33-108">**ตารางเวลา** - แสดงมุมมองตารางเวลาสำหรับการรีเฟรชที่กำหนดไว้ ซึ่งยังสามารถค้นพบปัญหาเกี่ยวกับช่วงเวลาที่มีการสมัครรับข้อมูลมากเกินไป</span><span class="sxs-lookup"><span data-stu-id="51a33-108">**Schedule** - shows the schedule view for scheduled refresh, which also can uncover issues with time slots that are oversubscribed.</span></span>

<span data-ttu-id="51a33-109">คุณยังสามารถส่งออกข้อมูลเกี่ยวกับเหตุการณ์การรีเฟรชไปยังไฟล์ .CSV ซึ่งสามารถให้ข้อมูลที่สำคัญและความเข้าใจในเหตุการณ์การรีเฟรช หรือข้อผิดพลาดที่สามารถส่งผลกระทบต่อประสิทธิภาพการทำงานหรือการดำเนินการรีเฟรชที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="51a33-109">You can also export information about a refresh event to a .CSV file, which can provide significant information and insight into refresh events or errors that can be impacting the performance or completion of scheduled refresh events.</span></span>

<span data-ttu-id="51a33-110">ส่วนต่อไปนี้จะพิจารณามุมมองเหล่านี้ในแต่ละมุมมองเป็นลำดับ</span><span class="sxs-lookup"><span data-stu-id="51a33-110">The following sections look at each of these views in turn.</span></span> 

## <a name="refresh-history"></a><span data-ttu-id="51a33-111">รีเฟรชประวัติ</span><span class="sxs-lookup"><span data-stu-id="51a33-111">Refresh history</span></span>

<span data-ttu-id="51a33-112">คุณสามารถเลือกมุมมอง **ประวัติ** ได้โดยการคลิกที่ **ประวัติ** ในหน้าสรุปการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="51a33-112">You can select the **History** view by clicking on **History** in the refresh summaries page.</span></span>

![มุมมองประวัติในสรุปการรีเฟรช](media/refresh-summaries/refresh-summaries-01a.jpg)

<span data-ttu-id="51a33-114">ประวัติมีข้อมูลภาพรวมผลลัพธ์ของการรีเฟรชที่กำหนดไว้ล่าสุดในความจุที่คุณมีสิทธิ์ในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="51a33-114">The History provides an overview of the outcomes of recently scheduled refreshes on the capacities for which you have admin privilege.</span></span> <span data-ttu-id="51a33-115">คุณสามารถเรียงลำดับมุมมองตามคอลัมน์ใด ๆ ได้โดยการคลิกที่คอลัมน์</span><span class="sxs-lookup"><span data-stu-id="51a33-115">You can sort the view by any column by clicking the column.</span></span> <span data-ttu-id="51a33-116">คุณสามารถเลือกที่จะเรียงลำดับมุมมองตามคอลัมน์ที่เลือกโดยเรียงลำดับจากน้อยไปมาก มากไปน้อย หรือโดยใช้ตัวกรองข้อความ</span><span class="sxs-lookup"><span data-stu-id="51a33-116">You can choose to sort the view by the column selected by ascending order, descending, or by using text filters.</span></span>

![เรียงลำดับมุมมองประวัติ](media/refresh-summaries/refresh-summaries-01b.jpg)

<span data-ttu-id="51a33-118">ในมุมมองประวัติข้อมูลที่เกี่ยวข้องกับการรีเฟรชที่กำหนดไว้จะขึ้นอยู่กับบันทึกรายการล่าสุด 60 รายการสำหรับการรีเฟรชที่กำหนดไว้แต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="51a33-118">In history view, the data associated with a given refresh is based on up 60 most recent records for each scheduled refresh.</span></span>

<span data-ttu-id="51a33-119">นอกจากนี้ คุณยังสามารถส่งออกข้อมูลสำหรับการรีเฟรชที่กำหนดไว้ใด ๆ ไปยัง ไฟล์ .CSV ซึ่งประกอบด้วยข้อมูลรายละเอียด รวมถึงข้อความข้อผิดพลาดสำหรับเหตุการณ์การรีเฟรชแต่ครั้ง</span><span class="sxs-lookup"><span data-stu-id="51a33-119">You can also export information for any scheduled refresh to a .CSV file, which includes detailed information including error messages for each refresh event.</span></span> <span data-ttu-id="51a33-120">การส่งออกไปยังไฟล์ .CSV ช่วยให้คุณสามารถเรียงลำดับไฟล์ที่ยึดตามคอลัมน์ใด ๆ ค้นหาคำ เรียงลำดับตามรหัสข้อผิดพลาดหรือเจ้าของ และอื่น ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="51a33-120">Exporting to a .CSV file lets you sort the file based on any of the columns, search for words, sort based on error codes or owners, and so on.</span></span> <span data-ttu-id="51a33-121">รูปภาพต่อไปนี้แสดงตัวอย่างของไฟล์ .CSV ที่ส่งออก</span><span class="sxs-lookup"><span data-stu-id="51a33-121">The following image shows an example exported .CSV file.</span></span> 

![ส่งออกข้อมูลเกี่ยวกับการรีเฟรช](media/refresh-summaries/refresh-summaries-05.jpg)

<span data-ttu-id="51a33-123">ด้วยข้อมูลในไฟล์ที่ส่งออก คุณสามารถตรวจสอบความจุ ระยะเวลา และข้อความข้อผิดพลาดใด ๆ ที่บันทึกไว้สำหรับอินสแตนซ์ของรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="51a33-123">With the information in the exported file, you can review the capacity, duration, and any error messages recorded for the instance of refresh.</span></span> 


## <a name="refresh-schedule"></a><span data-ttu-id="51a33-124">กำหนดตารางเวลาการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="51a33-124">Refresh schedule</span></span>

<span data-ttu-id="51a33-125">คุณสามารถเลือกมุมมอง **ตารางเวลา** ได้โดยการคลิกที่ **ตารางเวลา** ในสรุปการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="51a33-125">You can select the **Schedule** view by clicking on **Schedule** in refresh summaries.</span></span> <span data-ttu-id="51a33-126">มุมมองตารางเวลาจะแสดงข้อมูลการกำหนดตารางเวลาสำหรับสัปดาห์ โดยแบ่งออกเป็นช่วงเวลาละ 30 นาที</span><span class="sxs-lookup"><span data-stu-id="51a33-126">The Schedule view displays scheduling information for the week, broken down into 30-minute time slots.</span></span> 

![สกรีนช็อตแสดงแท็บกำหนดการของหน้ากำหนดตารางเวลาการรีเฟรชในระยะใกล้](media/refresh-summaries/refresh-summaries-02a.jpg)

<span data-ttu-id="51a33-128">มุมมองตารางเวลามีประโยชน์อย่างมากในการพิจารณาว่าเหตุการณ์การรีเฟรชที่กำหนดไว้นั้นเว้นระยะไว้อย่างเหมาะสมหรือไม่ ทำให้การรีเฟรชทั้งหมดเสร็จสมบูรณ์โดยไม่ทับซ้อนกัน หรือคุณมีเหตุการณ์การรีเฟรชที่กำหนดไว้ที่ใช้เวลานานเกินไป และสร้างข้อขัดแย้งของทรัพยากรหรือไม่</span><span class="sxs-lookup"><span data-stu-id="51a33-128">The Schedule view is very useful in determining whether the refresh events scheduled are properly spaced, allowing for all refreshes to complete without overlap, or whether you have scheduled refresh events that are taking too long and creating resource contention.</span></span> <span data-ttu-id="51a33-129">ถ้าคุณพบข้อขัดแย้งของทรัพยากรดังกล่าว คุณควรปรับตารางเวลาการรีเฟรชของคุณเพื่อหลีกเลี่ยงความขัดแย้งหรือการซ้อนทับกัน ดังนั้นการรีเฟรชที่กำหนดไว้ของคุณสามารถดำเนินการให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="51a33-129">If you find such resource contention, you should adjust your refresh schedules to avoid the conflicts or overlap, so your scheduled refreshes can complete successfully.</span></span> 

![สกรีนช็อตแสดงแท็บกำหนดการของหน้ากำหนดตารางเวลาการรีเฟรช](media/refresh-summaries/refresh-summaries-02.jpg)

<span data-ttu-id="51a33-131">คอลัมน์ *เวลาการรีเฟรชที่จองไว้ (นาที)*  คือการคำนวณค่าเฉลี่ยของบันทึกรายการสูงสุดถึง 60 รายการสำหรับแต่ละชุดข้อมูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="51a33-131">The *Refresh time booked (minutes)* column is a calculation of the average of up to 60 records for each associated dataset.</span></span> <span data-ttu-id="51a33-132">ค่าตัวเลขสำหรับช่วงเวลา 30 นาทีแต่ละช่วง คือผลรวมของนาทีที่คำนวณสำหรับการรีเฟรชที่กำหนดไว้ทั้งหมดเพื่อเริ่มต้นในช่วงเวลา **และ** การรีเฟรชที่กำหนดไว้ใด ๆ เพื่อเริ่มต้นช่วงเวลา *ก่อนหน้านี้* แต่มีช่วงเวลาเฉลี่ยที่เกินออกไปในช่วงเวลาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="51a33-132">The numeric value for each 30-minute time slot is the sum of minutes calculated for all scheduled refreshes scheduled to start on the time slot **and** any scheduled refreshes set to start on the *previous* time slot, but whose average duration overflows into the time slot that's selected.</span></span>

<span data-ttu-id="51a33-133">คอลัมน์ *เวลาที่พร้อมใช้งานการรีเฟรช (นาที)* คือการคำนวณนาทีที่พร้อมใช้งานสำหรับการรีเฟรชในแต่ละครั้งที่มีการลบการรีเฟรชใดก็ตามที่มีการกำหนดเวลาไว้สำหรับช่องเวลานั้น</span><span class="sxs-lookup"><span data-stu-id="51a33-133">The *Refresh time available (minutes)* column is a calculation of the minutes available for refresh in each time slot, minus whatever refresh is already scheduled for that timeslot.</span></span> <span data-ttu-id="51a33-134">ตัวอย่างเช่นถ้าการสมัครใช้งาน P2 ของคุณให้การรีเฟรชที่มีจำนวน 12 แบบพร้อมกันคุณจะมีช่อง 1230 นาที ดังนั้น 12 รีเฟรช x 30 นาทีแต่ละครั้ง = 360 นาทีพร้อมใช้งานสำหรับการรีเฟรชในช่องเวลานั้น</span><span class="sxs-lookup"><span data-stu-id="51a33-134">For example, if your P2 subscription provides 12 concurrently running refreshes, you have 12 30-minute slots, so 12 refreshes x 30 minutes each = 360 minutes available for refresh in that time slot.</span></span> <span data-ttu-id="51a33-135">หากคุณมีการรีเฟรชหนึ่งรายการในช่องดังกล่าวที่ใช้เวลา 20 นาที การ *รีเฟรชของคุณพร้อมใช้งาน (นาที)* ในช่องดังกล่าวคือ 340 นาที (360 ทั้งหมดที่พร้อมใช้งานลบ 20 นาทีจองแล้ว = 340 นาทียังคงพร้อมใช้งาน)</span><span class="sxs-lookup"><span data-stu-id="51a33-135">If you have one refresh booked in that slot that takes 20 minutes, your *Refresh time available (minutes)* in that slot is 340 minutes (360 total minutes available, minus 20 minutes already booked = 340 minutes still available).</span></span> 

<span data-ttu-id="51a33-136">คุณสามารถเลือกช่วงเวลา จากนั้นเลือกปุ่ม **รายละเอียด** ที่เกี่ยวข้องเพื่อดูเหตุการณ์การรีเฟรชที่กำหนดไว้ที่มีส่วนเกี่ยวข้องกับเวลาการรีเฟรที่จองไว้ เจ้าของ และระยะเวลาที่ใช้ในการดำเนินการให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="51a33-136">You can select a time slot and then select the associated **details** button to see which scheduled refresh events contribute to the refresh time booked, their owners, and how long they take to complete.</span></span>

<span data-ttu-id="51a33-137">ลองดูตัวอย่างเพื่อดูวิธีการทำงาน</span><span class="sxs-lookup"><span data-stu-id="51a33-137">Let's look at an example, to see how this works.</span></span> <span data-ttu-id="51a33-138">กล่องโต้ตอบต่อไปนี้จะแสดงขึ้นเมื่อเราเลือกช่วงเวลา 20:30 น. วันอาทิตย์ และคลิก **รายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="51a33-138">The following dialog is displayed when we select the 8:30 PM time slot for Sunday, and click **details**.</span></span>

![สกรีนช็อตแสดงรายละเอียดสำหรับการรีเฟรชในช่วงเวลาที่เลือก](media/refresh-summaries/refresh-summaries-04.jpg)

<span data-ttu-id="51a33-140">มีสามเหตุการณ์การรีเฟรชที่กำหนดไว้ที่เกิดขึ้นในช่วงเวลานี้</span><span class="sxs-lookup"><span data-stu-id="51a33-140">There are three scheduled refresh events occurring in this time slot.</span></span> 

<span data-ttu-id="51a33-141">ทั้งการรีเฟรชที่กำหนดไว้ครั้งที่ #1 และ #3 จะถูกกำหนดเวลาไว้สำหรับช่วงเวลา 20:30 น. นี้ ซึ่งเราสามารถตรวจสอบได้โดยดูที่ค่าในคอลัมน์ **ช่วงเวลาที่กำหนดไว้**</span><span class="sxs-lookup"><span data-stu-id="51a33-141">Scheduled refresh #1 and #3 are both scheduled for this 8:30 PM time slot, which we can determine by looking at the value in the **Scheduled time slot** column.</span></span> <span data-ttu-id="51a33-142">ระยะเวลาโดยเฉลี่ยคือ 4:39 และหกวินาที (0:06) ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="51a33-142">Their average durations are 4:39 and six seconds (0:06) respectively.</span></span> <span data-ttu-id="51a33-143">เป็นช่วงเวลาที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="51a33-143">All is good there.</span></span>

<span data-ttu-id="51a33-144">อย่างไรก็ตาม การรีเฟรชที่กำหนดไว้ครั้งที่ #2 มีการกำหนดเวลาไว้สำหรับช่วงเวลา 20:00 น. แต่เนื่องจากใช้เวลาโดยเฉลี่ยมากกว่า 48 นาทีในการดำเนินการให้เสร็จสมบูรณ์ (ที่เห็นในคอลัมน์ **ระยะเวลาเฉลี่ย**) ซึ่งจะทำให้เหตุการณ์การรีเฟรชเกินออกไปในช่วงเวลา 30 นาทีถัดไป</span><span class="sxs-lookup"><span data-stu-id="51a33-144">However, scheduled refresh #2 is scheduled for the 8:00 PM time slot, but because it takes an average of over 48 minutes to complete (seen in the **Average duration** column), that refresh event overflows into the next 30-minute time slot.</span></span> 

<span data-ttu-id="51a33-145">ซึ่งไม่ดี</span><span class="sxs-lookup"><span data-stu-id="51a33-145">That's not good.</span></span> <span data-ttu-id="51a33-146">ผู้ดูแลระบบในกรณีนี้ควรติดต่อเจ้าของของอินสแตนซ์การรีเฟรชที่กำหนดไว้ดังกล่าว และแนะนำให้พวกเขาค้นหาช่วงเวลาที่แตกต่างกันสำหรับการรีเฟรชที่กำหนดไว้ หรือกำหนดตารางเวลาใหม่อีกครั้งเพื่อไม่ให้มีการทับซ้อนกัน หรือค้นหาโซลูชันอื่น ๆ เพื่อป้องกันการทับซ้อนดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="51a33-146">The admin in this case should contact the owners of that scheduled refresh instance and suggest they find a different time slot for that scheduled refresh, or reschedule the other refreshes so there's no overlap, or find some other solution to prevent such overlap.</span></span> 


## <a name="next-steps"></a><span data-ttu-id="51a33-147">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="51a33-147">Next steps</span></span>

- [<span data-ttu-id="51a33-148">การรีเฟรชข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="51a33-148">Data refresh in Power BI</span></span>](refresh-data.md)  
- [<span data-ttu-id="51a33-149">เกตเวย์ Power BI - ส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="51a33-149">Power BI Gateway - Personal</span></span>](service-gateway-personal-mode.md)  
- [<span data-ttu-id="51a33-150">เกตเวย์ข้อมูลภายในองค์กร (โหมดส่วนบุคคล)</span><span class="sxs-lookup"><span data-stu-id="51a33-150">On-premises data gateway (personal mode)</span></span>](service-gateway-onprem.md)  
- [<span data-ttu-id="51a33-151">การแก้ไขปัญหาเกตเวย์ข้อมูลในองค์กร</span><span class="sxs-lookup"><span data-stu-id="51a33-151">Troubleshooting the On-premises data gateway</span></span>](service-gateway-onprem-tshoot.md)  
- [<span data-ttu-id="51a33-152">แก้ไขปัญหาเกตเวย์ Power BI - ส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="51a33-152">Troubleshooting the Power BI Gateway - Personal</span></span>](service-admin-troubleshooting-power-bi-personal-gateway.md)  

<span data-ttu-id="51a33-153">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="51a33-153">More questions?</span></span> [<span data-ttu-id="51a33-154">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="51a33-154">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)