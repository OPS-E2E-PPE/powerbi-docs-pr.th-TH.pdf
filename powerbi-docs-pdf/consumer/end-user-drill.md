---
title: การดูข้อมูลแบบเจาะลึกและข้อมูลสรุปในภาพ
description: บทความนี้แสดงวิธีการดูข้อมูลแบบเจาะลึกในการแสดงภาพในบริการของ Microsoft Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-explore
ms.topic: how-to
ms.date: 12/21/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 17fe24957dbcccd7038ea34566a8db8f5684cb18
ms.sourcegitcommit: 0711972326521944fdd8572403c0b15f31b916da
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/22/2020
ms.locfileid: "97721535"
---
# <a name="drill-mode-in-a-visual-in-power-bi"></a><span data-ttu-id="5ba64-103">โหมดการดูข้อมูลแบบเจาะลึกของภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ba64-103">Drill mode in a visual in Power BI</span></span>

[!INCLUDE[consumer-appliesto-yyny](../includes/consumer-appliesto-yyny.md)]


<span data-ttu-id="5ba64-104">บทความนี้แสดงวิธีการดูข้อมูลแบบเจาะลึกในการแสดงภาพในบริการของ Microsoft Power BI</span><span class="sxs-lookup"><span data-stu-id="5ba64-104">This article shows how to drill down in a visual in the Microsoft Power BI service.</span></span> <span data-ttu-id="5ba64-105">ใช้การดูรายละเอียดแนวลึกดูข้อมูลสรุปบนจุดข้อมูลของคุณ คุณสามารถสำรวจรายละเอียดเชิงลึกเกี่ยวกับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ba64-105">Using drill down and drill up on your data points, you can explore in-depth details about your data.</span></span> 

## <a name="drill-requires-a-hierarchy"></a><span data-ttu-id="5ba64-106">การดูรายละเอียดแนวลึก จำเป็นต้องมีลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="5ba64-106">Drill requires a hierarchy</span></span>

<span data-ttu-id="5ba64-107">เมื่อวิชวลมีลำดับชั้น คุณสามารถเจาะลงไปเพื่อดูรายละเอียดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5ba64-107">When a visual has a hierarchy, you can drill down to reveal additional details.</span></span> <span data-ttu-id="5ba64-108">ตัวอย่างเช่น คุณอาจมีภาพที่ดูการนับจำนวนเหรียญรางวัลโอลิมปิก โดยมีลำดับชั้นที่สร้างขึ้นจากชนิดกีฬา ประเภทกีฬา และรายการแข่งขัน</span><span class="sxs-lookup"><span data-stu-id="5ba64-108">For example, you might have a visual that looks at Olympic medal count by a hierarchy made up of sport, discipline, and event.</span></span> <span data-ttu-id="5ba64-109">ตามค่าเริ่มต้น ภาพจะแสดงจำนวนเหรียญรางวัลตามชนิดกีฬา: ยิมนาสติก, สกี, กีฬาทางน้ำ และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="5ba64-109">By default, the visual would show medal count by sport: gymnastics, skiing, aquatics, and so on.</span></span> <span data-ttu-id="5ba64-110">แต่เนื่องจากมีลำดับชั้น การเลือกองค์ประกอบหนึ่งของภาพ (ตัวอย่างเช่น แท่ง เส้น หรือฟอง) จะแสดงรูปภาพที่มีรายละเอียดเพิ่มขึ้นอย่างมาก</span><span class="sxs-lookup"><span data-stu-id="5ba64-110">But, because it has a hierarchy, selecting one of the visual elements (like a bar, line, or bubble), would display an increasingly more-detailed picture.</span></span> <span data-ttu-id="5ba64-111">การเลือกองค์ประกอบ **กีฬาทางน้ำ** จะแสดงข้อมูลสำหรับการว่ายน้ำ การกระโดดน้ำ และโปโลน้ำ</span><span class="sxs-lookup"><span data-stu-id="5ba64-111">Selecting the **aquatics** element would show you data for swimming, diving, and water polo.</span></span>  <span data-ttu-id="5ba64-112">การเลือกองค์ประกอบ **การกระโดดน้ำ** จะแสดงรายละเอียดสำหรับการแข่งขัน กระดานสปริงบอร์ด แพลตฟอร์ม และ กระโดดน้ำแบบคู่</span><span class="sxs-lookup"><span data-stu-id="5ba64-112">Selecting the **diving** element would show you details for springboard, platform, and synchronized diving events.</span></span>

<span data-ttu-id="5ba64-113">วันที่คือประเภทเฉพาะของลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="5ba64-113">Dates are a unique type of hierarchy.</span></span>  <span data-ttu-id="5ba64-114">*นักออกแบบ* รายงานมักจะเพิ่มลำดับชั้นของวันที่ไปยังวิชวล</span><span class="sxs-lookup"><span data-stu-id="5ba64-114">Report *designers* often add date hierarchies to visuals.</span></span> <span data-ttu-id="5ba64-115">ลำดับชั้นของวันที่ทั่วไปคือลำดับชั้นที่ประกอบด้วยปี ไตรมาส เดือน และวัน</span><span class="sxs-lookup"><span data-stu-id="5ba64-115">A common date hierarchy is one that contains year, quarter, month, and day.</span></span> 

## <a name="figure-out-which-visuals-can-be-drilled"></a><span data-ttu-id="5ba64-116">ตรวจสอบว่าภาพใดบ้างที่สามารถการดูข้อมูลแบบเจาะลึกได้</span><span class="sxs-lookup"><span data-stu-id="5ba64-116">Figure out which visuals can be drilled</span></span>
<span data-ttu-id="5ba64-117">ไม่แน่ใจว่าการแสดงภาพ Power BI ภาพใดที่มีลำดับชั้นใช่หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="5ba64-117">Not sure which Power BI visuals contain a hierarchy?</span></span> <span data-ttu-id="5ba64-118">เลื่อนเมาส์ไปบนภาพ</span><span class="sxs-lookup"><span data-stu-id="5ba64-118">Hover over a visual.</span></span> <span data-ttu-id="5ba64-119">หากคุณเห็นชุดข้อมูลการควบคุมการดูข้อมูลแบบเจาะลึกเหล่านี้ที่ด้านบน แสดงว่าภาพของคุณมีลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="5ba64-119">If you see a combination of these drill controls at the top, your visual has a hierarchy.</span></span>

![ภาพหน้าจอของไอคอนการดูข้อมูลแบบเจาะลึก](./media/end-user-drill/power-bi-drill-icons.png)  


## <a name="learn-how-to-drill-down-and-up"></a><span data-ttu-id="5ba64-121">เรียนรู้วิธการดูข้อมูลแบบเจาะลึกและข้อมูลสรุป</span><span class="sxs-lookup"><span data-stu-id="5ba64-121">Learn how to drill down and up</span></span>

<span data-ttu-id="5ba64-122">ในตัวอย่างนี้ เรากำลังใช้แผนที่ต้นไม้ที่มีลำดับชั้นซึ่งสร้างขึ้นจากเขตแดน เมือง รหัสไปรษณีย์ และชื่อร้านค้า</span><span class="sxs-lookup"><span data-stu-id="5ba64-122">In this example we're using a treemap that has a hierarchy made up of territory, city, postal code, and store name.</span></span> <span data-ttu-id="5ba64-123">แผนที่ต้นไม้แสดงหน่วยทั้งหมดที่ขายในปีนี้ตามเขตแดน ก่อนการดูข้อมูลแบบเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="5ba64-123">The treemap, before drilling, looks at total units sold this year by territory.</span></span> <span data-ttu-id="5ba64-124">เขตแดนคือระดับบนสุดของลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="5ba64-124">Territory is the top level of the hierarchy.</span></span>

![ภาพหน้าจอของไอคอนแผนที่ต้นไม้และตัวกรอง](./media/end-user-drill/power-bi-treemap.png)  


### <a name="two-ways-to-access-the-drill-features"></a><span data-ttu-id="5ba64-126">มีสองวิธีในการเข้าถึงคุณลักษณะการดูข้อมูลแบบเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="5ba64-126">Two ways to access the drill features</span></span>

<span data-ttu-id="5ba64-127">คุณมีสองวิธีสำหรับการเข้าถึงการดูข้อมูลแบบเจาะลึก ข้อมูลสรุป และขยายคุณลักษณะในการแสดงผลภาพที่มีลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="5ba64-127">You have two ways for accessing the drill-down, drill-up, and expand features for visuals that have hierarchies.</span></span> <span data-ttu-id="5ba64-128">ลองใช้งานทั้งสองวิธี และเลือกใช้หนึ่งวิธีที่คุณชื่นชอบมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="5ba64-128">Try them both, and use the one that you enjoy the most.</span></span>

- <span data-ttu-id="5ba64-129">วิธีแรก: เลื่อนเมาส์ไปบนภาพเพื่อดูและใช้ไอคอน</span><span class="sxs-lookup"><span data-stu-id="5ba64-129">First way: hover over a visual to see and use the icons.</span></span> <span data-ttu-id="5ba64-130">เปิดใช้งานการดูรายละเอียดแนวลึกก่อนโดยเลือกลูกศรชี้ลง</span><span class="sxs-lookup"><span data-stu-id="5ba64-130">Turn on drill down first by selecting the downward arrow.</span></span> <span data-ttu-id="5ba64-131">พื้นหลังสีเทาช่วยให้คุณทราบว่าการดูรายละเอียดแนวลึกทำงานอยู่</span><span class="sxs-lookup"><span data-stu-id="5ba64-131">The grey background lets you know that drill down is active.</span></span>   

    ![สกรีนช็อตของตัวอย่างโฮเวอร์](./media/end-user-drill/power-bi-drill-hover.png)

- <span data-ttu-id="5ba64-133">วิธีที่สอง: คลิกขวาที่ภาพเพื่อเปิดและใช้เมนู</span><span class="sxs-lookup"><span data-stu-id="5ba64-133">Second way: right-click a visual to reveal and use the menu.</span></span>

    ![สกรีนช็อตของตัวอย่างการคลิกขวา](./media/end-user-drill/power-bi-drill-action-menu.png)



## <a name="drill-pathways"></a><span data-ttu-id="5ba64-135">เส้นทางการดูรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="5ba64-135">Drill pathways</span></span>

### <a name="drill-down-all-fields-at-once"></a><span data-ttu-id="5ba64-136">ดูรายละเอียดแนวลึกทุกเขตข้อมูลในครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="5ba64-136">Drill down all fields at once</span></span>
![ไอคอนรายละเอียดแนวลึก](./media/end-user-drill/power-bi-drill-icon3.png)

<span data-ttu-id="5ba64-138">คุณมีหลายวิธีที่จะดูข้อมูลภาพของคุณแบบเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="5ba64-138">You have several ways to drill into your visual.</span></span> <span data-ttu-id="5ba64-139">การเลือกไอคอนลูกศรคู่ ![สำหรับการดูรายละเอียดระดับทั้งหมดในครั้งเดียว](./media/end-user-drill/power-bi-drill-icon3.png)ไอคอนดูรายละเอียดแนวลึกจะนำคุณไปยังระดับถัดไปในลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="5ba64-139">Selecting the double arrow ![icon for drill all levels at once](./media/end-user-drill/power-bi-drill-icon3.png)drill-down icon takes you to the next level in the hierarchy.</span></span> <span data-ttu-id="5ba64-140">หากคุณกำลังมองหาระดับ **เขตแดน** สำหรับเคนทักกีและเทนเนสซี คุณสามารถดูข้อมูลแบบเจาะลึกในระดับเมืองสำหรับทั้งสองรัฐ ตามด้วยระดับรหัสไปรษณีย์สำหรับทั้งสองรัฐ และสุดท้ายคือระดับชื่อร้านค้าสำหรับทั้งสองรัฐ</span><span class="sxs-lookup"><span data-stu-id="5ba64-140">If you're looking at the **Territory** level for Kentucky and Tennessee, you can drill down to city level for both states, then postal code level for both states, and, finally, the store name level for both states.</span></span> <span data-ttu-id="5ba64-141">แต่ละขั้นตอนในเส้นทางจะแสดงข้อมูลใหม่ให้คุณ</span><span class="sxs-lookup"><span data-stu-id="5ba64-141">Each step in the path shows you new information.</span></span>

![ไดอะแกรมแสดงรายละเอียดของเส้นทาง](./media/end-user-drill/power-bi-drill-path.png)

<span data-ttu-id="5ba64-143">เลือกไอคอนการดูข้อมูลสรุป</span><span class="sxs-lookup"><span data-stu-id="5ba64-143">Select the drill-up icon</span></span> ![ไอคอนการดูข้อมูลสรุป](./media/end-user-drill/power-bi-drill-icon5.png) <span data-ttu-id="5ba64-145">จนกว่าคุณจะย้อนกลับไปที่ “หน่วยรวมปีนี้ตามเขตแดน”</span><span class="sxs-lookup"><span data-stu-id="5ba64-145">until you get back to "Total units this year by territory".</span></span>

### <a name="expand-all-fields-at-once"></a><span data-ttu-id="5ba64-146">ขยายเขตข้อมูลทั้งหมดพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="5ba64-146">Expand all fields at once</span></span>
![ไอคอนขยาย](./media/end-user-drill/power-bi-drill-icon6.png)

<span data-ttu-id="5ba64-148">**ขยาย** เป็นการเพิ่มระดับของลำดับชั้นในมุมมองปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="5ba64-148">**Expand** adds an additional hierarchy level to the current view.</span></span> <span data-ttu-id="5ba64-149">ดังนั้นถ้าคุณกำลังดูระดับ **เขตแดน** คุณสามารถขยายใบปัจจุบันทั้งหมดในต้นไม้ในเวลาเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="5ba64-149">So if you're looking at the **Territory** level, you can expand all current leaves in the tree at the same time.</span></span>  <span data-ttu-id="5ba64-150">การดูรายละเอียดแบบเจาะลึกแรกของคุณสำหรับทั้ง **KY** และ **TN**</span><span class="sxs-lookup"><span data-stu-id="5ba64-150">Your first drill adds city data for both **KY** and **TN**.</span></span> <span data-ttu-id="5ba64-151">การดูรายละเอียดแบบเจาะลึกต่อไปเพิ่มข้อมูลรหัสไปรษณีย์สำหรับทั้ง **KY** และ **TN** และเก็บข้อมูลเมืองไว้ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="5ba64-151">The next drill adds postal code data for both **KY** and **TN**, and keeps city data as well.</span></span> <span data-ttu-id="5ba64-152">แต่ละขั้นตอนในเส้นทางแสดงข้อมูลเดียวกัน และเพิ่มข้อมูลใหม่อีกหนึ่งระดับ</span><span class="sxs-lookup"><span data-stu-id="5ba64-152">Each step in the path shows you the same information and adds on one level of new information.</span></span>

![ไดอะแกรมแสดงการขยายของเส้นทาง](./media/end-user-drill/power-bi-expand-path.png)


### <a name="drill-down-one-field-at-a-time"></a><span data-ttu-id="5ba64-154">ดูรายละเอียดแนว﻿ลึกทีละเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5ba64-154">Drill down one field at a time</span></span>


1. <span data-ttu-id="5ba64-155">เลือกไอคอนดูรายละเอียดเพื่อเปิดใช้งานการดูรายละเอียดแนวลึก</span><span class="sxs-lookup"><span data-stu-id="5ba64-155">Select the drill-down icon to turn it on</span></span> ![สกรีนช็อตของไอคอนเปิด/ปิดการดูรายละเอียดแนวลึกที่เปิดใช้งานอยู่](./media/end-user-drill/power-bi-drill-icon2.png)<span data-ttu-id="5ba64-157">.</span><span class="sxs-lookup"><span data-stu-id="5ba64-157">.</span></span>

    <span data-ttu-id="5ba64-158">ในตอนนี้คุณมีตัวเลือกในการดูข้อมูลแบบเจาะลึก **ทีละหนึ่งเขตข้อมูล** โดยการเลือกองค์ประกอบการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="5ba64-158">Now you have the option of drilling down **one field at a time** by selecting a visual element.</span></span> <span data-ttu-id="5ba64-159">ตัวอย่างขององค์ประกอบการแสดงภาพคือ: แท่ง ฟอง และใบไม้</span><span class="sxs-lookup"><span data-stu-id="5ba64-159">Examples of visual elements are: bar, bubble, and leaf.</span></span>

    ![สกรีนช็อตของวิชวลที่มีลูกศรชี้ไปที่ไอคอนเปิด/ปิดการดูรายละเอียดเชิงลึกที่เปิดใช้งานอยู่](media/end-user-drill/power-bi-select-drill-icon.png)

    <span data-ttu-id="5ba64-161">ถ้าคุณไม่เปิดใช้งานการดูข้อมูลแบบเจาะลึก การเลือกองค์ประกอบภาพ (เช่น แท่ง ฟอง หรือใบไม้) จะไม่ดูข้อมูลแบบเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="5ba64-161">If you don't turn on drill down, selecting a visual element (like a bar, bubble, or leaf) won't drill down.</span></span> <span data-ttu-id="5ba64-162">แต่กลายเป็นว่าระบบจะกรองข้ามแผนภูมิอื่นๆ บนหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="5ba64-162">Instead, it will cross-filter the other charts on the report page.</span></span>

1. <span data-ttu-id="5ba64-163">เลือกใบไม้สำหรับ **TN**</span><span class="sxs-lookup"><span data-stu-id="5ba64-163">Select the leaf for **TN**.</span></span> <span data-ttu-id="5ba64-164">แผนที่ต้นไม้ของคุณจะแสดงเมืองทั้งหมดและเขตแดนในรัฐเทนเนสซีที่มีร้านค้า</span><span class="sxs-lookup"><span data-stu-id="5ba64-164">Your treemap now shows all the cities and territories in Tennessee that have a store.</span></span>

    ![สกรีนช็อตของแผนที่ต้นไม้ที่แสดงข้อมูลสำหรับ TN เท่านั้น](media/end-user-drill/power-bi-drill-down-first.png)

1. <span data-ttu-id="5ba64-166">ถึงจุดนี้ คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="5ba64-166">At this point, you can:</span></span>

    1. <span data-ttu-id="5ba64-167">ดูรายละเอียดแนวลึกต่อไปได้สำหรับ Tennessee</span><span class="sxs-lookup"><span data-stu-id="5ba64-167">Continue drilling down for Tennessee.</span></span>

    1. <span data-ttu-id="5ba64-168">ดูรายละเอียดแนวลึกสำหรับเมืองที่ระบุในรัฐ Tennessee</span><span class="sxs-lookup"><span data-stu-id="5ba64-168">Drill down for a particular city in Tennessee.</span></span>

    1. <span data-ttu-id="5ba64-169">ใช้การขยายแทน</span><span class="sxs-lookup"><span data-stu-id="5ba64-169">Expand instead.</span></span>

    <span data-ttu-id="5ba64-170">ลองดูรายละเอียดแนวลึกทีละเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5ba64-170">Let's continue to drill down one field at a time.</span></span>  <span data-ttu-id="5ba64-171">เลือก **Knoxville, TN** (เมือง Knoxville รัฐ Tennessee)</span><span class="sxs-lookup"><span data-stu-id="5ba64-171">Select **Knoxville, TN**.</span></span> <span data-ttu-id="5ba64-172">แผนที่ต้นไม้ของคุณขณะนี้ แสดงรหัสไปรษณีย์สำหรับร้านค้าของคุณใน Knoxville</span><span class="sxs-lookup"><span data-stu-id="5ba64-172">Your treemap now shows the postal code for your store in Knoxville.</span></span>

    ![สกรีนช็อตของแผนที่ต้นไม้ที่แสดงข้อมูลรหัสไปรษณีย์ 37919](media/end-user-drill/power-bi-drill-twice.png)

    <span data-ttu-id="5ba64-174">สังเกตว่า ชื่อเรื่องเปลี่ยนไปขณะที่คุณเจาะลึกลงรายละเอียด และย้อนกลับขึ้นมาอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="5ba64-174">Notice that the title changes as you drill down and back up again.</span></span>

    <span data-ttu-id="5ba64-175">และดูรายละเอียดแนวลึกอีกหนึ่งเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5ba64-175">And drill down one more field.</span></span> <span data-ttu-id="5ba64-176">เลือกรหัสไปรษณีย์ **37919** และดูรายละเอียดแนวลึกลงของชื่อร้านค้า</span><span class="sxs-lookup"><span data-stu-id="5ba64-176">Select postal code **37919** and drill down to store name.</span></span> 

    ![สกรีนช็อตของแผนที่ต้นไม้ที่แสดง Knoxville Lindsey](media/end-user-drill/power-bi-drill-last.png)    

    <span data-ttu-id="5ba64-178">สำหรับข้อมูลนี้โดยเฉพาะ การเจาะลึกระดับทั้งหมดในครั้งเดียวอาจไม่น่าสนใจ</span><span class="sxs-lookup"><span data-stu-id="5ba64-178">For this particular data, drilling down all levels at once may not be interesting.</span></span> <span data-ttu-id="5ba64-179">ลองขยายออกมาแทน</span><span class="sxs-lookup"><span data-stu-id="5ba64-179">Let's try expanding instead.</span></span>

### <a name="expand-all-and-expand-one-field-at-a-time"></a><span data-ttu-id="5ba64-180">ขยายทั้งหมด และขยายหนึ่งทีละเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="5ba64-180">Expand all and expand one field at a time</span></span>

<span data-ttu-id="5ba64-181">การมีแผนภูมิต้นไม้ที่แสดงเพียงรหัสไปรษณีย์ หรือชื่อของร้านค้าไม่ได้ให้ข้อมูลมากเท่าไหร่</span><span class="sxs-lookup"><span data-stu-id="5ba64-181">Having a treemap that shows us only a postal code or only a store name isn't informative.</span></span>  <span data-ttu-id="5ba64-182">ดังนั้นเรามา *ขยาย* ลำดับชั้นลงไปอีกหนึ่งระดับ</span><span class="sxs-lookup"><span data-stu-id="5ba64-182">So let's *expand* down one level in the hierarchy.</span></span>  

1. <span data-ttu-id="5ba64-183">ก่อนอื่นให้ดูรายละเอียดย้อนกลับไปยังระดับรหัสไปรษณีย์</span><span class="sxs-lookup"><span data-stu-id="5ba64-183">First, drill back up to the postal code level.</span></span>     
1. <span data-ttu-id="5ba64-184">ด้วยแผนที่ต้นไม้ที่ถูกเลือกไว้ก่อนแล้ว เลือกไอคอน *ขยายลง* ![สกรีนช็อตของไอคอนขยายลง](./media/end-user-drill/power-bi-drill-icon6.png)</span><span class="sxs-lookup"><span data-stu-id="5ba64-184">With the treemap active, select the *expand down* icon ![Screenshot of the expand-down icon.](./media/end-user-drill/power-bi-drill-icon6.png).</span></span> <span data-ttu-id="5ba64-185">แผนภูมิต้นไม้ของคุณตอนนี้จะแสดง 2 ลำดับชั้น: คือ รหัสไปรษณีย์ และชื่อร้านค้า</span><span class="sxs-lookup"><span data-stu-id="5ba64-185">Your treemap now shows two levels of the hierarchy: postal code and store name.</span></span>

    ![สกรีนช็อตของแผนที่ต้นไม้ที่แสดงข้อมูลรหัสไปรษณีย์และชื่อร้านค้า](./media/end-user-drill/power-bi-expand.png)

1. <span data-ttu-id="5ba64-187">หากต้องการดูข้อมูลเกี่ยวกับ Tennesee ทั้ง 4 ลำดับชั้น ให้เลือกลูกศรการดูข้อมูลสรุปจนกว่าคุณไปถึงระดับที่สอง **จำนวนหน่วยรวมปีนี้ที่จำแนกตามเขตแดนและเมือง**</span><span class="sxs-lookup"><span data-stu-id="5ba64-187">To see all four hierarchy levels of data for Tennessee, select the drill-up arrow until you reach the second level, **Total units this year by territory and city**.</span></span>

    ![สกรีนช็อตของแผนที่ต้นไม้ที่แสดงข้อมูลสำหรับ TN](media/end-user-drill/power-bi-expand-second.png)

1. <span data-ttu-id="5ba64-189">ตรวจสอบให้แน่ใจว่าการดูรายละเอียดแนวลึกยังคงเปิดใช้งานอยู่![ไอคอนสกรีนช็อตของลึก เปิด/ปิดที่เปิดใช้งาน](./media/end-user-drill/power-bi-drill-icon2.png)</span><span class="sxs-lookup"><span data-stu-id="5ba64-189">Make sure drill down is still turned on, ![Screenshot of drill down on/off icon turned on.](./media/end-user-drill/power-bi-drill-icon2.png)</span></span> <span data-ttu-id="5ba64-190">และเลือกไอคอน *ขยายลง* ![สกรีนช็อตของไอคอนขยายลง](./media/end-user-drill/power-bi-drill-icon6.png)</span><span class="sxs-lookup"><span data-stu-id="5ba64-190">and select the *expand down* icon ![Screenshot of the expand-down icon.](./media/end-user-drill/power-bi-drill-icon6.png).</span></span> <span data-ttu-id="5ba64-191">ในตอนนี้แผนที่ต้นไม้ของคุณแสดงจำนวนใบไม้ (กล่อง) เท่ากัน แต่ใบไม้แต่ละใบนั้นมีรายละเอียดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5ba64-191">Your treemap now shows the same number of leaves (boxes), but each leaf has additional detail.</span></span> <span data-ttu-id="5ba64-192">นอกจากการแสดงผลแค่เมืองและรัฐแล้ว ยังแสดงรหัสไปรษณีย์อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="5ba64-192">Instead of only showing city and state, it now also shows us postal code.</span></span>

    ![สกรีนช็อตของการแสดงภาพเมือง สถานะ และรหัสไปรษณีย์](./media/end-user-drill/power-bi-expand-third.png)

1. <span data-ttu-id="5ba64-194">เลือกไอคอน *ขยายลง* อีกครั้งเพื่อแสดงลำดับชั้นทั้ง 4 เกี่ยวกับรายละเอียดของ Tennesee บนแผนภูมิต้นไม้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5ba64-194">Select the *expand down* icon one more time to display all four hierarchy levels of detail for Tennessee on your treemap.</span></span> <span data-ttu-id="5ba64-195">โฮเวอร์เหนือเป็นใบไม้เพื่อดูรายละเอียดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5ba64-195">Hover over a leaf to see even more detail.</span></span>

    ![สกรีนช็อตของแผนที่ต้นไม้ที่แสดงคำแนะนำด้วยข้อมูลเฉพาะโหนดปลายสุด](./media/end-user-drill/power-bi-expand-final.png)

## <a name="show-the-data-as-you-drill"></a><span data-ttu-id="5ba64-197">แสดงข้อมูลขณะที่คุณดูข้อมูลแบบเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="5ba64-197">Show the data as you drill</span></span>
<span data-ttu-id="5ba64-198">ใช้ตัวเลือก **แสดงเป็นตาราง** เพื่อดูเบื้องหลังฉาก</span><span class="sxs-lookup"><span data-stu-id="5ba64-198">Use **Show as a table** to get a look behind the scenes.</span></span> <span data-ttu-id="5ba64-199">แต่ละครั้งที่คุณดูข้อมูลแบบเจาะลึกหรือขยาย **แสดงเป็นตาราง** จะแสดงผลข้อมูลที่ใช้ในการสร้างวิชวล</span><span class="sxs-lookup"><span data-stu-id="5ba64-199">Each time you drill or expand, **Show as a table** displays the data being used to build the visual.</span></span> <span data-ttu-id="5ba64-200">ซึ่งอาจช่วยให้คุณเข้าใจวิธีการทำงานของลำดับชั้น การดูข้อมูลแบบเจาะลึก และขยายการทำงานร่วมกันเพื่อสร้างการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="5ba64-200">This may help you understand how hierarchies, drill, and expand work together to build visuals.</span></span> 

<span data-ttu-id="5ba64-201">ในมุมขวาบน เลือก **ตัวเลือกเพิ่มเติม** (...) แล้วเลือก **แสดงเป็นตาราง**</span><span class="sxs-lookup"><span data-stu-id="5ba64-201">In the upper-right corner, select **More actions** (...), and then select **Show as a table**.</span></span> 

![ภาพหน้าจอของเมนูจุดไข่ปลา](./media/end-user-drill/power-bi-more-actions.png)

<span data-ttu-id="5ba64-203">Power BI เปิดแผนที่ต้นไม้เพื่อให้เติมพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="5ba64-203">Power BI opens the treemap so that it fills the canvas.</span></span> <span data-ttu-id="5ba64-204">ข้อมูลในแผนที่ต้นไม้จะแสดงด้านล่างวิชวล</span><span class="sxs-lookup"><span data-stu-id="5ba64-204">The data that makes up the treemap displays below the visual.</span></span> 

![สกรีนช็อตของแผนที่ต้นไม้ที่มีตารางข้อมูลที่แสดงด้านล่าง](./media/end-user-drill/power-bi-show-table.png)

<span data-ttu-id="5ba64-206">ด้วยวิชวลเพียงอย่างเดียวในพื้นที่ทำงาน ให้เจาะลึกรายละเอียดต่อไป</span><span class="sxs-lookup"><span data-stu-id="5ba64-206">With the visual alone in the canvas, continue drilling.</span></span> <span data-ttu-id="5ba64-207">ดูข้อมูลในการเปลี่ยนแปลงตารางเพื่อแสดงให้เห็นถึงข้อมูลที่ใช้ในการสร้างแผนที่ต้นไม้</span><span class="sxs-lookup"><span data-stu-id="5ba64-207">Watch the data in the table change to reflect the data being used to create the treemap.</span></span> <span data-ttu-id="5ba64-208">ตารางต่อไปนี้แสดงผลลัพธ์ของการดูข้อมูลแบบเจาะลึกในเขตข้อมูลทั้งหมดพร้อม ๆ กันตั้งแต่เขตแดนไปจนถึงร้านค้า</span><span class="sxs-lookup"><span data-stu-id="5ba64-208">The following table shows the results of drilling down all fields at once from territory to store name.</span></span> <span data-ttu-id="5ba64-209">ตารางแรกแสดงระดับบนสุดของลำดับชั้น แผนที่ต้นไม้แสดงสองใบ หนึ่งใบสำหรับ **KY** และหนึ่งใบสำหรับ **TN**</span><span class="sxs-lookup"><span data-stu-id="5ba64-209">The first table represents the top level of the hierarchy, the treemap showing two leaves, one for **KY** and one for **TN**.</span></span> <span data-ttu-id="5ba64-210">ตารางสามรายการถัดไปแสดงข้อมูลของแผนที่ต้นไม้ในขณะที่คุณดูรายละเอียดระดับทั้งหมดในครั้งเดียว--จากเขตแดนไปยังเมืองไปยังรหัสไปรษณีย์ไปยังชื่อร้านค้า</span><span class="sxs-lookup"><span data-stu-id="5ba64-210">The next three tables represent the treemap's data as you drill down all levels at once--from territory to city to postal code to store name.</span></span>


![ภาพหน้าจอของการแสดงข้อมูลสำหรับการดูข้อมูลแบบเจาะลึกทั้งสี่ระดับ](./media/end-user-drill/power-bi-show-data.png)

<span data-ttu-id="5ba64-212">โปรดสังเกตว่าผลรวมจะเหมือนกันสำหรับ **เมือง\*\*\*\*รหัสไปรษณีย์** และ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="5ba64-212">Notice that the totals are the same for **City**, **PostalCode**, and **Name**.</span></span> <span data-ttu-id="5ba64-213">ผลรวมที่ตรงกันจะไม่เป็นเช่นนี้เสมอไป</span><span class="sxs-lookup"><span data-stu-id="5ba64-213">Matching totals won't always be the case.</span></span>  <span data-ttu-id="5ba64-214">แต่สำหรับข้อมูลนี้ มีร้านค้าเพียงแห่งเดียวในแต่ละรหัสไปรษณีย์และในแต่ละเมือง</span><span class="sxs-lookup"><span data-stu-id="5ba64-214">But for this data, there's only one store in each postal code and in each city.</span></span>  



## <a name="considerations-and-limitations"></a><span data-ttu-id="5ba64-215">ข้อควรพิจารณาและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="5ba64-215">Considerations and limitations</span></span>
- <span data-ttu-id="5ba64-216">ตามค่าเริ่มต้น การดูรายละเอียดจะไม่กรองวิชวลอื่น ๆ ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="5ba64-216">By default, drilling won't filter other visuals in a report.</span></span> <span data-ttu-id="5ba64-217">อย่างไรก็ตาม ผู้ออกแบบรายงานสามารถเปลี่ยนลักษณะการทำงานเริ่มต้นนี้ได้</span><span class="sxs-lookup"><span data-stu-id="5ba64-217">However, the report designer can change this default behavior.</span></span> <span data-ttu-id="5ba64-218">ในขณะที่คุณดูข้อมูลแบบเจาะลึก ให้ดูว่าการแสดงภาพอื่น ๆ บนหน้านั้นมีการกรองข้ามหรือไฮไลท์ข้ามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="5ba64-218">As you drill, look to see if the other visuals on the page are cross-filtering or cross-highlighting.</span></span>

- <span data-ttu-id="5ba64-219">การดูรายงานที่มีการแชร์กับคุณต้องมีสิทธิ์การใช้งาน Power BI Pro หรือใบอนุญาตแบบ Premium หรือสำหรับรายงานต้องจัดเก็บอยู่ในความจุ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="5ba64-219">Viewing a report that has been shared with you requires a Power BI Pro or Premium license or for the report to be stored in Power BI Premium capacity.</span></span> [<span data-ttu-id="5ba64-220">ฉันมีสิทธิการใช้งานใดอยู่บ้าง</span><span class="sxs-lookup"><span data-stu-id="5ba64-220">Which license do I have?</span></span>](end-user-license.md)


## <a name="next-steps"></a><span data-ttu-id="5ba64-221">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="5ba64-221">Next steps</span></span>

[<span data-ttu-id="5ba64-222">การแสดงผลด้วยภาพในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ba64-222">Visuals in Power BI reports</span></span>](../visuals/power-bi-report-visualizations.md)

[<span data-ttu-id="5ba64-223">รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ba64-223">Power BI reports</span></span>](end-user-reports.md)

[<span data-ttu-id="5ba64-224">Power BI แนวคิดพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="5ba64-224">Power BI - Basic Concepts</span></span>](end-user-basic-concepts.md)

<span data-ttu-id="5ba64-225">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="5ba64-225">More questions?</span></span> [<span data-ttu-id="5ba64-226">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="5ba64-226">Try the Power BI Community</span></span>](https://community.powerbi.com/)
