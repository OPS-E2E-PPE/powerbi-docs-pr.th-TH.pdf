---
title: ภาพรวมคิวรีใน Power BI Desktop
description: ภาพรวมคิวรีใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: conceptual
ms.date: 01/11/2020
LocalizationGroup: Transform and shape data
ms.openlocfilehash: 9202b94808624ca9e3332ba7acdca29a3ce759ca
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414012"
---
# <a name="query-overview-in-power-bi-desktop"></a><span data-ttu-id="df6ad-103">ภาพรวมคิวรีใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="df6ad-103">Query overview in Power BI Desktop</span></span>
<span data-ttu-id="df6ad-104">ด้วย Power BI Desktop คุณสามารถเชื่อมต่อกับโลกของข้อมูล สร้างรายงานที่น่าสนใจ และแชร์ความพยายามของคุณกับผู้อื่น – ที่สามารถสร้างผลงานต่อจากงานของคุณ และขยายความพยายามอันชาญฉลาดทางธุรกิจของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="df6ad-104">With Power BI Desktop you can connect to the world of data, create compelling and foundational reports, and share your efforts with others – who can then build on your work, and expand their business intelligence efforts.</span></span>

<span data-ttu-id="df6ad-105">Power BI Desktop มีสามมุมมอง:</span><span class="sxs-lookup"><span data-stu-id="df6ad-105">Power BI Desktop has three views:</span></span>

* <span data-ttu-id="df6ad-106">มุมมอง **รายงาน** – เป็นที่ที่คุณใช้คิวรีที่คุณสร้างภาพที่แสดงข้อมูลที่ดึงดูดความสนใจ จัดเรียงการแสดงผลตามที่คุณต้องการให้ปรากฏในหลายหน้าที่คุณสามารถแบ่งปันกับผู้อื่น</span><span class="sxs-lookup"><span data-stu-id="df6ad-106">**Report** view – where you use queries you create to build compelling visualizations, arranged as you want them to appear, and with multiple pages, that you can share with others</span></span>
* <span data-ttu-id="df6ad-107">มุมมอง **ข้อมูล** ู – เป็นที่ที่ดูข้อมูลในรายงานของคุณในรูปแบบจำลองข้อมูล เป็นที่ที่ี่คุณสามารถเพิ่มการวัด สร้างคอลัมน์ใหม่ และจัดการความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="df6ad-107">**Data** view – see the data in your report in data model format, where you can add measures, create new columns, and manage relationships</span></span>
* <span data-ttu-id="df6ad-108">มุมมอง **ความสัมพันธ์** ู – เป็นที่แสดงภาพกราฟิกของความสัมพันธ้ในแบบจำลองข้อมูลของคุณ และจัดการ หรือปรับเปลี่ยนความสัมพันธ์นั้นได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="df6ad-108">**Relationships** view – get a graphical representation of the relationships that have been established in your data model, and manage or modify them as needed.</span></span>

<span data-ttu-id="df6ad-109">เข้าถึงมุมมองเหล่านี้โดยการเลือกไอคอนหนึ่งในสามทางด้านซ้ายของ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="df6ad-109">Access these views by selecting one of the three icons along the left side of Power BI Desktop.</span></span> <span data-ttu-id="df6ad-110">ในรูปต่อไปนี้ มุมมอง **รายงาน** ถูกเลือก ที่บ่งชี้ด้วยแถบสีเหลืองที่อยู่ด้านข้างไอคอน</span><span class="sxs-lookup"><span data-stu-id="df6ad-110">In the following image, **Report** view is selected, indicated by the yellow band beside the icon.</span></span>  

![ภาพหน้าจอของ Power B I Desktop ที่แสดงมมุมมองรายงานที่เลือกไว้](media/desktop-query-overview/queryoverview_viewicons.png)
 
<span data-ttu-id="df6ad-112">Power BI Desktop ยังมาพร้อมกับ Power Query Editor</span><span class="sxs-lookup"><span data-stu-id="df6ad-112">Power BI Desktop also comes with Power Query Editor.</span></span> <span data-ttu-id="df6ad-113">ใช้ Power Query Editor เพื่อเชื่อมต่อกับแหล่งข้อมูลหนึ่งหรือหลายแหล่ง จัดรูปร่างและแปลงข้อมูลตามความต้องการของคุณ จากนั้นโหลดแบบจำลองดังกล่าวเข้าไปใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="df6ad-113">Use Power Query Editor to connect to one or many data sources, shape and transform the data to meet your needs, then load that model into Power BI Desktop.</span></span>

<span data-ttu-id="df6ad-114">เอกสารนี้ให้ภาพรวมของการทำงานกับข้อมูลใน Power Query Editor แต่ยังมีอีกมากมายให้เรียนรู้</span><span class="sxs-lookup"><span data-stu-id="df6ad-114">This document provides an overview of the work with data in the Power Query Editor, but there's more to learn.</span></span> <span data-ttu-id="df6ad-115">ในตอนท้ายของเอกสารนี้ คุณจะพบลิงก์ไปยังคำแนะนำโดยละเอียดเกี่ยวกับชนิดข้อมูลที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="df6ad-115">At the end of this document, you'll find links to detailed guidance about supported data types.</span></span> <span data-ttu-id="df6ad-116">นอกจากนี้คุณยังจะได้พบกับคำแนะนำเกี่ยวกับการเชื่อมต่อกับข้อมูล การจัดรูปร่างข้อมูล การสร้างความสัมพันธ์ และวิธีการเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="df6ad-116">You'll also find guidance about connecting to data, shaping data, creating relationships, and how to get started.</span></span>

<span data-ttu-id="df6ad-117">แต่คุณต้องทำความคุ้นเคยกับ Power Query Editor ก่อน</span><span class="sxs-lookup"><span data-stu-id="df6ad-117">But first, let's see get acquainted with Power Query Editor.</span></span>

## <a name="power-query-editor"></a><span data-ttu-id="df6ad-118">ตัวแก้ไข Power Query</span><span class="sxs-lookup"><span data-stu-id="df6ad-118">Power Query Editor</span></span>
<span data-ttu-id="df6ad-119">เมื่อต้องการใช้ Power Query Editor ให้เลือก **แก้ไขคิวรี** จากแท็บ **หน้าแรก** ของ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="df6ad-119">To get to Power Query Editor, select **Edit Queries** from the **Home** tab of Power BI Desktop.</span></span>  

![ภาพหน้าจอของหน้าต่าง Power BI Desktop ที่แสดงแท็บหน้าแรกของ Power Query Editor](media/desktop-query-overview/queryoverview_queryview.png)

<span data-ttu-id="df6ad-121">เมื่อไม่มีการเชื่อมต่อข้อมูล Power Query Editor จะปรากฏเป็นบานหน้าต่างว่างที่พร้อมสำหรับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="df6ad-121">With no data connections, Power Query Editor appears as a blank pane, ready for data.</span></span>  

![ภาพหน้าจอของ Power B I Desktop ที่แสดง Power Query Editor ที่ไม่มีการเชื่อมต่อข้อมูล](media/desktop-query-overview/queryoverview_blankpane.png)

<span data-ttu-id="df6ad-123">เมื่อคิวรีถูกโหลด มุมมอง Power Query Editor จะกลายเป็นเรื่องน่าสนใจมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="df6ad-123">Once a query is loaded, Power Query Editor view becomes more interesting.</span></span> <span data-ttu-id="df6ad-124">ถ้าเราเชื่อมต่อกับแหล่งข้อมูลต่อไปนี้ของเว็บ Power Query Editor จะโหลดข้อมูลเกี่ยวกับข้อมูลที่คุณสามารถเริ่มต้นจัดรูปร่าง</span><span class="sxs-lookup"><span data-stu-id="df6ad-124">If we connect to the following Web data source, Power Query Editor loads information about the data, which you can then begin to shape:</span></span>

[*https://www.bankrate.com/retirement/best-and-worst-states-for-retirement/*](https://www.bankrate.com/retirement/best-and-worst-states-for-retirement/)

<span data-ttu-id="df6ad-125">นี่คือวิธีที่ Power Query Editor ปรากฏเมื่อมีการเชื่อมต่อข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="df6ad-125">Here's how Power Query Editor appears once a data connection is established:</span></span>

1. <span data-ttu-id="df6ad-126">ในริบบอน มีปุ่มจำนวนมากพร้อมใช้งานเพื่อโต้ตอบกับข้อมูลในคิวรี</span><span class="sxs-lookup"><span data-stu-id="df6ad-126">In the ribbon, many buttons are now active to interact with the data in the query.</span></span>
2. <span data-ttu-id="df6ad-127">ในบานหน้าต่างด้านซ้าย รายการคิวรี (สำหรับแต่ละตารางหรือรายการ) จะแสดงอยู่และพร้อมให้เลือก ดู และจัดรูปร่าง</span><span class="sxs-lookup"><span data-stu-id="df6ad-127">In the left pane, queries are listed and available for selection, viewing, and shaping.</span></span>
3. <span data-ttu-id="df6ad-128">ในบานหน้าต่างตรงกลาง ข้อมูลจากคิวรีที่เลือกจะแสดงและพร้อมให้จัดรูปร่าง</span><span class="sxs-lookup"><span data-stu-id="df6ad-128">In the center pane, data from the selected query is displayed and available for shaping.</span></span>
4. <span data-ttu-id="df6ad-129">บานหน้าต่าง **การตั้งค่าคิวรี** จะปรากฏ โดยแสดงรายการคุณสมบัติของคิวรีและขั้นตอนที่ใช้</span><span class="sxs-lookup"><span data-stu-id="df6ad-129">The **Query Settings** pane appears, listing the query's properties and applied steps.</span></span>  
   
   ![ภาพหน้าจอของหน้าต่าง Power B I Desktop ที่แสดงบานหน้าต่างการตั้งค่าคิวรีใน Power Query Editor](media/desktop-query-overview/queryoverview_withdataconnection.png)

<span data-ttu-id="df6ad-131">เราจะเรียนรู้เกี่ยวกับแต่ละด้านทั้งสี่เหล่านี้: แถบเครื่องมือริบบอน บานหน้าต่างคิวรี มุมมองข้อมูล และบานหน้าต่างการตั้งค่าคิวรี</span><span class="sxs-lookup"><span data-stu-id="df6ad-131">We'll look at each of these four areas: the ribbon, the Queries pane, the Data view, and the Query Settings pane.</span></span>

## <a name="the-query-ribbon"></a><span data-ttu-id="df6ad-132">Ribbon คิวรี</span><span class="sxs-lookup"><span data-stu-id="df6ad-132">The query ribbon</span></span>
<span data-ttu-id="df6ad-133">รอบบอนใน Power Query Editor ประกอบด้วยสี่แท็บ: **หน้าหลัก** **แปลง** **เพิ่มคอลัมน์** และ **ดู**</span><span class="sxs-lookup"><span data-stu-id="df6ad-133">The ribbon in Power Query Editor consists of four tabs: **Home**, **Transform**, **Add Column**, and **View**.</span></span>

<span data-ttu-id="df6ad-134">แท็บ **หน้าหลัก** ประกอบด้วยงานคิวรีทั่วไป</span><span class="sxs-lookup"><span data-stu-id="df6ad-134">The **Home** tab contains the common query tasks.</span></span>

![ภาพหน้าจอของ Power BI Desktop ที่แสดงแถบเครื่องมือริบบอนคิวรี Power Query Editor](media/desktop-query-overview/queryoverview_ribbon.png)

<span data-ttu-id="df6ad-136">เมื่อต้องการเชื่อมต่อกับข้อมูล และเริ่มขบวนการสร้างคิวรีเลือกปุ่ม **แหล่งใหม่ (New Source)**</span><span class="sxs-lookup"><span data-stu-id="df6ad-136">To connect to data and begin the query building process, select **New Source**.</span></span> <span data-ttu-id="df6ad-137">เมนูจะปรากฏ และให้แหล่งข้อมูลที่พบบ่อยที่สุด</span><span class="sxs-lookup"><span data-stu-id="df6ad-137">A menu appears, providing the most common data sources.</span></span>  

![ภาพหน้าจอของ Power B I Desktop ที่แสดงปุ่มแหล่งข้อมูลใหม่](media/desktop-query-overview/query-overview-new-source-menu.png)

<span data-ttu-id="df6ad-139">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแหล่งข้อมูลที่พร้อมใช้งาน ดู **แหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="df6ad-139">For more information about available data sources, see **Data Sources**.</span></span> <span data-ttu-id="df6ad-140">สำหรับข้อมูลเกี่ยวกับการเชื่อมต่อกับข้อมูล ที่รวมถึงตัวอย่างและขั้นตอน ดู **เชื่อมต่อกับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="df6ad-140">For information about connecting to data, including examples and steps, see **Connect to Data**.</span></span>

<span data-ttu-id="df6ad-141">แท็บ **แปลง** จัดเตรียมการเข้าถึงงานการแปลงข้อมูลทั่วไปเช่น:</span><span class="sxs-lookup"><span data-stu-id="df6ad-141">The **Transform** tab provides access to common data transformation tasks, such as:</span></span>

* <span data-ttu-id="df6ad-142">การเพิ่มและการลบคอลัมน์ออก</span><span class="sxs-lookup"><span data-stu-id="df6ad-142">Adding or removing columns</span></span>
* <span data-ttu-id="df6ad-143">การเปลี่ยนชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="df6ad-143">Changing data types</span></span> 
* <span data-ttu-id="df6ad-144">การแยกคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="df6ad-144">Splitting columns</span></span> 
* <span data-ttu-id="df6ad-145">งานที่มีการควบคุมข้อมูลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="df6ad-145">Other data-driven tasks</span></span>

![ภาพหน้าจอของ Power B I Desktop ที่แสดงแท็บหน้าแรก](media/desktop-query-overview/queryoverview_transformribbon.png)

<span data-ttu-id="df6ad-147">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแปลงข้อมูล ที่รวมถึงตัวอย่าง ดูที่บทช่วยสอน [: จัดรูปร่างและรวมข้อมูลใน Power BI Desktop](../connect-data/desktop-shape-and-combine-data.md)</span><span class="sxs-lookup"><span data-stu-id="df6ad-147">For more information about transforming data, including examples, see [Tutorial: Shape and combine data in Power BI Desktop](../connect-data/desktop-shape-and-combine-data.md).</span></span>

<span data-ttu-id="df6ad-148">แท็บ **เพิ่มคอลัมน์** เป็นการเพิ่มคอลัมน์ จัดรูปแบบข้อมูลคอลัมน์ และการเพิ่มคอลัมน์แบบกำหนดเองรวมทั้งงานอื่นๆที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="df6ad-148">The **Add Column** tab provides additional tasks associated with adding a column, formatting column data, and adding custom columns.</span></span> <span data-ttu-id="df6ad-149">รูปภาพต่อไปนี้แสดง แท็บ **เพิ่มคอลัมน์**</span><span class="sxs-lookup"><span data-stu-id="df6ad-149">The following image shows the **Add Column** tab.</span></span>  

![ภาพหน้าจอของ Power B I Desktop ที่แสดงแท็บเพิ่มคอลัมน์](media/desktop-query-overview/queryoverview_addcolumnribbon.png)

<span data-ttu-id="df6ad-151">แท็บ **มุมมอง** บน ribbon ถูกใช้เพื่อสลับว่าจะแสดงบานหน้าต่าง หรือ windows</span><span class="sxs-lookup"><span data-stu-id="df6ad-151">The **View** tab on the ribbon is used to toggle whether certain panes or windows are displayed.</span></span> <span data-ttu-id="df6ad-152">นอกจากนี้ยังใช้เพื่อแสดงเครื่องมือแก้ไขขั้นสูงด้วย</span><span class="sxs-lookup"><span data-stu-id="df6ad-152">It's also used to display the Advanced Editor.</span></span> <span data-ttu-id="df6ad-153">รูปภาพต่อไปนี้แสดง แท็บ **มุมมอง**</span><span class="sxs-lookup"><span data-stu-id="df6ad-153">The following image shows the **View** tab.</span></span>  

![ภาพหน้าจอของ Power B I Desktop ที่แสดงแท็บมุมมอง](media/desktop-query-overview/queryoverview_viewribbon.png)

<span data-ttu-id="df6ad-155">และคุณควรทราบว่างานต่าง ๆ มากมายที่สามารถใช้งานได้จากแถบเครื่องมือริบบอนนั้นยังสามารถเรียกใช้ได้โดยการคลิกขวาที่คอลัมน์ หรือข้อมูลอื่น ๆ ในบานหน้าต่างตรงกลางด้วย</span><span class="sxs-lookup"><span data-stu-id="df6ad-155">It's useful to know that many of the tasks available from the ribbon are also available by right-clicking a column, or other data, in the center pane.</span></span>

## <a name="the-left-queries-pane"></a><span data-ttu-id="df6ad-156">บานหน้าต่างด้านซ้าย (คิวรี)</span><span class="sxs-lookup"><span data-stu-id="df6ad-156">The left (Queries) pane</span></span>
<span data-ttu-id="df6ad-157">บานหน้าต่างด้านซ้าย หรือบานหน้าต่าง **Queries** แสดงจำนวนของคิวรีที่ใช้งานอยู่ และชื่อของคิวรี</span><span class="sxs-lookup"><span data-stu-id="df6ad-157">The left pane, or **Queries** pane, displays the number of active queries and the name of the query.</span></span> <span data-ttu-id="df6ad-158">เมื่อคุณเลือกคิวรีจากบานหน้าต่างด้านซ้าย ข้อมูลของคิวรีจะแสดงในบานหน้าต่างตรงกลาง ซึ่งคุณสามารถจัดรูปแบบ และแปลงข้อมูลนี้ตามความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="df6ad-158">When you select a query from the left pane, its data is displayed in the center pane, where you can shape and transform the data to meet your needs.</span></span> <span data-ttu-id="df6ad-159">รูปต่อไปนี้แสดงบานหน้าต่างด้านซ้ายที่มีคิวรี</span><span class="sxs-lookup"><span data-stu-id="df6ad-159">The following image shows the left pane with a query.</span></span>  

![ภาพหน้าจอของ Power B I Desktop ที่แสดงคิวรีในบานหน้าต่างด้านซ้าย](media/desktop-query-overview/queryoverview_theleftpane.png)

## <a name="the-center-data-pane"></a><span data-ttu-id="df6ad-161">บานหน้าต่างตรงกลาง (ข้อมูล)</span><span class="sxs-lookup"><span data-stu-id="df6ad-161">The center (Data) pane</span></span>
<span data-ttu-id="df6ad-162">บานหน้าต่างตรงกลาง หรือบานหน้าต่าง **ข้อมูล** จะแสดงข้อมูลจากคิวรีที่เลือก</span><span class="sxs-lookup"><span data-stu-id="df6ad-162">In the center pane, or **Data** pane, data from the selected query is displayed.</span></span> <span data-ttu-id="df6ad-163">บานหน้าต่างนี้คือตำแหน่งที่เห็นการทำงานของ **คิวรี**</span><span class="sxs-lookup"><span data-stu-id="df6ad-163">This pane is where much of the work of the **Query** view is accomplished.</span></span>

<span data-ttu-id="df6ad-164">ในรูปต่อไปนี้แสดงการเชื่อมต่อข้อมูลเว็บที่สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="df6ad-164">In the following image shows the Web data connection established earlier.</span></span> <span data-ttu-id="df6ad-165">คอลัมน์ **Product** ถูกเลือก และคลิกขวาที่ส่วนหัวเพื่อแสดงรายการเมนูที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="df6ad-165">The **Product** column is selected, and its header is right-clicked to show the available menu items.</span></span> <span data-ttu-id="df6ad-166">โปรดสังเกตว่า รายการเมนูคลิกขวาเหล่านี้หลายรายการจะเหมือนกับปุ่มในแท็บ ribbon</span><span class="sxs-lookup"><span data-stu-id="df6ad-166">Notice that many of these right-click menu items are the same as buttons in the ribbon tabs.</span></span>  

![ภาพหน้าจอของ Power B I Desktop ที่แสดงข้อมูลในบานหน้าต่างตรงกลาง](media/desktop-query-overview/queryoverview_thecenterpane.png)

<span data-ttu-id="df6ad-168">เมื่อคุณเลือกรายการเมนูคลิกขวา (หรือปุ่ม ribbon) คิวรีจะทำงานตามขั้นตอนกัับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="df6ad-168">When you select a right-click menu item (or a ribbon button), the query applies the step to the data.</span></span> <span data-ttu-id="df6ad-169">นอกจากนี้ยังบันทึกขั้นตอนเป็นส่วนหนึ่งของคิวรีนั้นด้วย</span><span class="sxs-lookup"><span data-stu-id="df6ad-169">It also saves step as part of the query itself.</span></span> <span data-ttu-id="df6ad-170">ขั้นตอนเหล่านี้จะถูกบันทึกในบานหน้าต่าง **การตั้งค่าคิวรี** อย่างเป็นลำดับ ตามที่อธิบายไว้ในหัวข้อถัดไป</span><span class="sxs-lookup"><span data-stu-id="df6ad-170">The steps are recorded in the **Query Settings** pane in sequential order, as described in the next section.</span></span>  

## <a name="the-right-query-settings-pane"></a><span data-ttu-id="df6ad-171">บานหน้าต่างด้านขวา (การตั้งค่าคิวรี)</span><span class="sxs-lookup"><span data-stu-id="df6ad-171">The right (Query Settings) pane</span></span>
<span data-ttu-id="df6ad-172">บานหน้าต่างด้านขวา หรือบานหน้าต่าง **การตั้งค่าคิวรี** แสดงขั้นตอนทั้งหมดที่เกี่ยวข้องกับคิวรี</span><span class="sxs-lookup"><span data-stu-id="df6ad-172">The right pane, or **Query Settings** pane, is where all steps associated with a query are displayed.</span></span> <span data-ttu-id="df6ad-173">ตัวอย่างเช่น ในรูปต่อไปนี้ หัวข้อ **ขั้นตอนที่นำไปใช้** ของบานหน้าต่าง **การตั้งค่าคิวรี** แสดงว่าเราเพิ่งเปลี่ยนชนิดของคอลัมน์ **คะแนนโดยรวม**</span><span class="sxs-lookup"><span data-stu-id="df6ad-173">For example, in the following image, the **Applied Steps** section of the **Query Settings** pane reflects the fact that we just changed the type of the **Overall score** column.</span></span>

![ภาพหน้าจอของ Power BI Desktop ที่แสดงการตั้งค่าคิวรีในบานหน้าต่างด้านขวา](media/desktop-query-overview/queryoverview_querysettingspane.png)

<span data-ttu-id="df6ad-175">ขั้นตอนการจัดรูปทรงจะอยู่ในหัวข้อ **ขั้นตอนที่นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="df6ad-175">As additional shaping steps are applied to the query, they're captured in the **Applied Steps** section.</span></span>

<span data-ttu-id="df6ad-176">สิ่งสำคัญคือต้องทราบว่าข้อมูลเบื้องต้น *ไม่* เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="df6ad-176">It's important to know that the underlying data *isn't* changed.</span></span> <span data-ttu-id="df6ad-177">แต่ Power Query Editor จะปรับและจัดรูปร่างมุมมองของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="df6ad-177">Rather, Power Query Editor adjusts and shapes its view of the data.</span></span> <span data-ttu-id="df6ad-178">นอกจากนี้ยังจัดรูปร่างและปรับมุมมองของการโต้ตอบใด ๆ ด้วยข้อมูลเบื้องต้นที่เกิดขึ้นตามมุมมองของข้อมูลดังกล่าวที่มีการจัดรูปร่างและแก้ไขแล้วของ Power Query Editor</span><span class="sxs-lookup"><span data-stu-id="df6ad-178">It also shapes and adjusts the view of any interaction with the underlying data that occurs based on Power Query Editor's shaped and modified view of that data.</span></span>

<span data-ttu-id="df6ad-179">ในบานหน้าต่าง **การตั้งค่าคิวรี** บานหน้าต่าง คุณสามารถเปลี่ยนชื่อขั้นตอน ลบขั้นตอน หรือจัดลำดับขั้นตอน ตามที่คุณเห็นว่าเหมาะสมได้</span><span class="sxs-lookup"><span data-stu-id="df6ad-179">In the **Query Settings** pane, you can rename steps, delete steps, or reorder the steps as you see fit.</span></span> <span data-ttu-id="df6ad-180">เมื่อต้องการทำเช่นนั้น คลิกขวาที่ขั้นตอนในหัวข้อ **ขั้นตอนท่่ีนำไปใช้** และเลือกจากเมนูที่ปรากฏ</span><span class="sxs-lookup"><span data-stu-id="df6ad-180">To do so, right-click the step in the **Applied Steps** section, and choose from the menu that appears.</span></span> <span data-ttu-id="df6ad-181">ขั้นตอนคิวรีทั้งหมดจะดำเนินการตามลำดับที่ปรากฏในบานหน้าต่าง **ขั้นตอนที่นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="df6ad-181">All query steps are carried out in the order they appear in the **Applied Steps** pane.</span></span>

![ภาพหน้าจอของ Power B I Desktop ที่แสดงคุณสมบัติการตั้งค่าคิวรีและตัวกรองขั้นตอนที่ใช้งาน](media/desktop-query-overview/queryoverview_querysettings_rename.png)

## <a name="advanced-editor"></a><span data-ttu-id="df6ad-183">เครื่องมือแก้ไขขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="df6ad-183">Advanced Editor</span></span>
<span data-ttu-id="df6ad-184">**เครื่องมือแก้ไขขั้นสูง** ช่วยให้คุณเห็นโค้ดที่ Power Query Editor กำลังสร้างขึ้นในแต่ละขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="df6ad-184">The **Advanced Editor** lets you see the code that Power Query Editor is creating with each step.</span></span> <span data-ttu-id="df6ad-185">นอกจากนี้ยังช่วยให้คุณสามารถสร้างโค้ดการจัดรูปร่างของคุณเองได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="df6ad-185">It also lets you create your own shaping code.</span></span> <span data-ttu-id="df6ad-186">เมื่อต้องการเปิดใช้ตัวแก้ไขขั้นสูง เลือก **มุมมอง** จาก ribbon แล้วเลือก **ตัวแก้ไขขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="df6ad-186">To launch the advanced editor, select **View** from the ribbon, then select **Advanced Editor**.</span></span> <span data-ttu-id="df6ad-187">หน้าต่างจะปรากฏขึ้น แสดงรหัสคิวรีที่่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="df6ad-187">A window appears, showing the existing query code.</span></span>  
<span data-ttu-id="df6ad-188">![ภาพหน้าจอของ Power BI Desktop ที่แสดงกล่องโต้ตอบเครื่องมือแก้ไขขั้นสูง](media/desktop-query-overview/queryoverview_advancededitor.png)</span><span class="sxs-lookup"><span data-stu-id="df6ad-188">![Screenshot of Power B I Desktop showing Advanced Editor dialog box.](media/desktop-query-overview/queryoverview_advancededitor.png)</span></span>

<span data-ttu-id="df6ad-189">คุณสามารถแก้ไขรหัสในหน้าต่าง **ตัวแก้ไขขั้นสูง** ได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="df6ad-189">You can directly edit the code in the **Advanced Editor** window.</span></span> <span data-ttu-id="df6ad-190">เมื่อต้องการปิดหน้าต่าง เลือกปุ่ม **เสร็จสิ้น** หรือ **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="df6ad-190">To close the window, select the **Done** or **Cancel** button.</span></span>  

## <a name="saving-your-work"></a><span data-ttu-id="df6ad-191">บันทึกงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="df6ad-191">Saving your work</span></span>
<span data-ttu-id="df6ad-192">เมื่อคิวรีของคุณอยู่ในตำแหน่งที่คุณต้องการ ให้เลือก **ปิด & ใช้** จากเมนู **ไฟล์** ของ Power Query Editor</span><span class="sxs-lookup"><span data-stu-id="df6ad-192">When your query is where you want it, select **Close & Apply** from Power Query Editor's **File** menu.</span></span> <span data-ttu-id="df6ad-193">การดำเนินการนี้จะนำการเปลี่ยนแปลงไปใช้และปิดตัวแก้ไข</span><span class="sxs-lookup"><span data-stu-id="df6ad-193">This action applies the changes and closes the editor.</span></span>  
<span data-ttu-id="df6ad-194">![ภาพหน้าจอของ Power B I Desktop ที่แสดงตัวเลือกปิดและใช้ที่ด้านล่างของแท็บไฟล์](media/desktop-query-overview/queryoverview_closenload.png)</span><span class="sxs-lookup"><span data-stu-id="df6ad-194">![Screenshot of Power B I Desktop showing Close and Apply option under File tab.](media/desktop-query-overview/queryoverview_closenload.png)</span></span>

<span data-ttu-id="df6ad-195">เมื่อเกิดความคืบหน้า Power BI Desktop จะแสดงกล่องโต้ตอบเพื่อแสดงสถานะ</span><span class="sxs-lookup"><span data-stu-id="df6ad-195">As progress is made, Power BI Desktop provides a dialog to display its status.</span></span>  
![ภาพหน้าจอของ Power B I Desktop ที่แสดงกล่องโต้ตอบการยืนยันการเปลี่ยนแปลงคิวรีที่ใช้งาน](media/desktop-query-overview/queryoverview_loading.png)

<span data-ttu-id="df6ad-197">เมื่อคุณพร้อมแล้ว Power BI Desktop สามารถบันทึกงานของคุณในรูปแบบของไฟล์ *.pbix* ได้</span><span class="sxs-lookup"><span data-stu-id="df6ad-197">When you're ready, Power BI Desktop can save your work in the form of a *.pbix* file.</span></span>

<span data-ttu-id="df6ad-198">เมื่อต้องการบันทึกงานของคุณ ให้เลือก **ไฟล์** \> **บันทึก** (หรือ **ไฟล์** \> **บันทึกเป็น**) ดังที่แสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="df6ad-198">To save your work, select **File** \> **Save** (or **File** \> **Save As**), as shown in the following image.</span></span>  
<span data-ttu-id="df6ad-199">![ภาพหน้าจอของ Power B I Desktop ที่แสดงแท็บไฟล์ของ Power Query Editor](media/desktop-query-overview/queryoverview_savework.png)</span><span class="sxs-lookup"><span data-stu-id="df6ad-199">![Screenshot of Power B I Desktop showing Power Query Editor File tab.](media/desktop-query-overview/queryoverview_savework.png)</span></span>

## <a name="next-steps"></a><span data-ttu-id="df6ad-200">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="df6ad-200">Next steps</span></span>
<span data-ttu-id="df6ad-201">มีมากมายหลากหลายสิ่งที่คุณสามารถทำได้ด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="df6ad-201">There are all sorts of things you can do with Power BI Desktop.</span></span> <span data-ttu-id="df6ad-202">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับขีดความสามารถ กรุณาดูแหล่งทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="df6ad-202">For more information on its capabilities, check out the following resources:</span></span>

* [<span data-ttu-id="df6ad-203">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="df6ad-203">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="df6ad-204">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="df6ad-204">Data sources in Power BI Desktop</span></span>](../connect-data/desktop-data-sources.md)
* [<span data-ttu-id="df6ad-205">เชื่อมต่อกับข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="df6ad-205">Connect to data in Power BI Desktop</span></span>](../connect-data/desktop-connect-to-data.md)
* [<span data-ttu-id="df6ad-206">บทช่วยสอน: จัดรูปร่างและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="df6ad-206">Tutorial: Shape and combine data with Power BI Desktop</span></span>](../connect-data/desktop-shape-and-combine-data.md)
* [<span data-ttu-id="df6ad-207">ใช้งานคิวรีที่ใช้บ่อยใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="df6ad-207">Perform common query tasks in Power BI Desktop</span></span>](desktop-common-query-tasks.md)