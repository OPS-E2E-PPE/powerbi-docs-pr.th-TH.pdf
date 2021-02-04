---
title: 'บทช่วยสอน: นำเข้าและวิเคราะห์ข้อมูลจากเว็บเพจ'
description: 'บทช่วยสอน: นำเข้าและวิเคราะห์ข้อมูลจากเว็บเพจโดยใช้ Power BI Desktop'
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: tutorial
ms.date: 01/13/2020
LocalizationGroup: Learn more
ms.openlocfilehash: d407da8e11473180f21e62c94f0ab440050beedc
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96404835"
---
# <a name="tutorial-analyze-webpage-data-by-using-power-bi-desktop"></a><span data-ttu-id="024d4-103">บทช่วยสอน: วิเคราะห์ข้อมูลเว็บเพจโดยใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="024d4-103">Tutorial: Analyze webpage data by using Power BI Desktop</span></span>

<span data-ttu-id="024d4-104">ในฐานะที่เป็นแฟนฟุตบอลมานาน คุณต้องการรายงานของแชมป์ ฟุตบอลชิงแชมป์แห่งชาติยุโรป (ถ้วยฟุตบอลยูโร) ในแต่ละปี</span><span class="sxs-lookup"><span data-stu-id="024d4-104">As a long-time soccer fan, you want to report on the UEFA European Championship (Euro Cup) winners over the years.</span></span> <span data-ttu-id="024d4-105">ด้วย Power BI Desktop คุณสามารถนำเข้าข้อมูลนี้จากเว็บเพจลงในรายงาน และสร้างการแสดงภาพที่แสดงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="024d4-105">With Power BI Desktop, you can import this data from a web page into a report and create visualizations that show the data.</span></span> <span data-ttu-id="024d4-106">ในบทช่วยสอนนี้ คุณจะเรียนรู้วิธีการใช้ Power BI Desktop เพื่อ:</span><span class="sxs-lookup"><span data-stu-id="024d4-106">In this tutorial, you learn how to use Power BI Desktop to:</span></span>

- <span data-ttu-id="024d4-107">เชื่อมต่อแหล่งข้อมูลเว็ปและนำทางไปตารางที่ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="024d4-107">Connect to a web data source and navigate across its available tables.</span></span>
- <span data-ttu-id="024d4-108">ทำรูปร่างและปรับเปลี่ยนข้อมูลใน Power Query Editor</span><span class="sxs-lookup"><span data-stu-id="024d4-108">Shape and transform data in the Power Query Editor.</span></span>
- <span data-ttu-id="024d4-109">ตั้งชื่อแบบสอบถามและนำเข้าไปยังรายงาน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="024d4-109">Name a query and import it into a Power BI Desktop report.</span></span>
- <span data-ttu-id="024d4-110">สร้าง และกำหนดแผนที่และภาพแผนภูมิวงกลม</span><span class="sxs-lookup"><span data-stu-id="024d4-110">Create and customize a map and a pie chart visualization.</span></span>

## <a name="connect-to-a-web-data-source"></a><span data-ttu-id="024d4-111">เชื่อมต่อกับแหล่งข้อมูลบนเว็บ</span><span class="sxs-lookup"><span data-stu-id="024d4-111">Connect to a web data source</span></span>

<span data-ttu-id="024d4-112">คุณสามารถรับข้อมูลแชมป์ UEFA จากตารางผลลัพธ์บนหน้า UEFA European Football Championship ของวิกิพีเดียที่ https://en.wikipedia.org/wiki/UEFA_European_Football_Championship ได้</span><span class="sxs-lookup"><span data-stu-id="024d4-112">You can get the UEFA winners data from the Results table on the UEFA European Football Championship Wikipedia page at https://en.wikipedia.org/wiki/UEFA_European_Football_Championship.</span></span> 

![ตารางผลลัพธ์วิกิพีเดีย](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage1.png)

<span data-ttu-id="024d4-114">การเชื่อมต่อเว็ปเป็นการใช้สร้างเพียงการพิสูจน์ตัวตนเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="024d4-114">Web connections are only established using basic authentication.</span></span> <span data-ttu-id="024d4-115">เว็บไซต์ที่จำเป็นต้องรับรองความถูกต้องอาจไม่ทำงานกับตัวเชื่อมต่อเว็บ</span><span class="sxs-lookup"><span data-stu-id="024d4-115">Web sites requiring authentication may not work properly with the Web connector.</span></span>

<span data-ttu-id="024d4-116">เพื่อนำเข้าข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="024d4-116">To import the data:</span></span>

1. <span data-ttu-id="024d4-117">ใน Power BI Desktop แท็บ ribbon **หน้าแรก** ดรอปดาวน์ลูกศรที่อยู่ถัดจาก **รับข้อมูล** แล้วเลือก **เว็บ**</span><span class="sxs-lookup"><span data-stu-id="024d4-117">In the Power BI Desktop **Home** ribbon tab, drop down the arrow next to **Get Data**, and then select **Web**.</span></span>

   ![รับข้อมูลจาก ribbon](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web3.png) 

   >[!NOTE]
   ><span data-ttu-id="024d4-119">คุณสามรถเลือกรายการ **รับข้อมูล** ด้วยตัวมันเองหรือเลือก **รับข้อมูล** จากกล่องโต้ตอบตอนเริ่ม Power BI Desktop แล้วเลือก **เว็ป** จากส่วน **ทั้งหมด** หรือ **อื่นๆ** ของการโต้ตอบ **รับข้อความ** จากนั้นเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="024d4-119">You can also select the **Get Data** item itself, or select **Get Data** from the Power BI Desktop get started dialog, then select **Web** from the **All** or **Other** section of the **Get Data** dialog, and then select **Connect**.</span></span>

1. <span data-ttu-id="024d4-120">ในการโต้ตอบ **จากเว็ป** ให้ใส่ URL `https://en.wikipedia.org/wiki/UEFA_European_Football_Championship` ไปในกล่องข้อความ **URL** จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="024d4-120">In the **From Web** dialog, paste the URL `https://en.wikipedia.org/wiki/UEFA_European_Football_Championship` into the **URL** text box, and then select **OK**.</span></span>

    ![รับข้อมูลจากกล่องโต้ตอบ](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web2.png)

   <span data-ttu-id="024d4-122">หลังจากการเชื่อมต่อไปยังหน้าเว็ป Wikipedi การโต้ตอบ **ตัวนำทาง** แสดงรายการของตารางที่มีอยู่ในหน้าดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="024d4-122">After connecting to the Wikipedia web page, the **Navigator** dialog shows a list of available tables on the page.</span></span> <span data-ttu-id="024d4-123">คุณสามารถเลือกชื่อตารางใด ๆ เพื่อแสดงตัวอย่างของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="024d4-123">You can select any of the table names to preview its data.</span></span> <span data-ttu-id="024d4-124">ตาราง **ผล[แก้ไข]** มีข้อมูลที่คุณต้องการ แม้กระทั่งไม่ใช้ข้อมูลที่คุณต้องการด้วยซ้ำ</span><span class="sxs-lookup"><span data-stu-id="024d4-124">The **Results[edit]** table has the data you want, although it's not exactly in the shape you want.</span></span> <span data-ttu-id="024d4-125">คุณจะทำการเปลี่ยนรูปร่างและล้างข้อมูลก่อนการโหลดไปยังรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="024d4-125">You'll reshape and clean up the data before loading it into your report.</span></span>

   ![กล่องโต้ตอบการนำทาง](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/tutorialimanaly_navigator.png)

   >[!NOTE]
   ><span data-ttu-id="024d4-127">แผง **ตัวอย่าง** แสดงตารางที่เลือกปัจจุบันที่สุด แต่ตารางที่เลือกทั้งหมดจะโหลดไปยัง Power Query Editor เมื่อคุณเลือก **เปลี่ยนแปลงข้อมูล** หรือ **โหลด**</span><span class="sxs-lookup"><span data-stu-id="024d4-127">The **Preview** pane shows the most recent table selected, but all selected tables will load into the Power Query Editor when you select **Transform Data** or **Load**.</span></span>

1. <span data-ttu-id="024d4-128">เลือกตาราง **ผล[แก้ไข]** ในรายการ **ตัวนำทาง** แล้วเลือก **เปลี่ยนแปลงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="024d4-128">Select the **Results[edit]** table in the **Navigator** list, and then select **Transform Data**.</span></span>

   <span data-ttu-id="024d4-129">ตัวอย่างของตารางที่เปิดใน **Power Query Editor** ที่คุณจะสามารถใช้การเปลี่ยนรูปเพื่อล้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="024d4-129">A preview of the table opens in **Power Query Editor**, where you can apply transformations to clean up the data.</span></span>

   ![ตัวแก้ไข Power Query](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage3.png)

## <a name="shape-data-in-power-query-editor"></a><span data-ttu-id="024d4-131">จัดรูปร่างข้อมูลในตัวแก้ไข Power Query</span><span class="sxs-lookup"><span data-stu-id="024d4-131">Shape data in Power Query Editor</span></span>

<span data-ttu-id="024d4-132">คุณต้องการทำให้ข้อมูลง่ายต่อการอ่าน โดยการแสดงเฉพาะปีและประเทศที่ชนะ</span><span class="sxs-lookup"><span data-stu-id="024d4-132">You want to make the data easier to scan by displaying only the years and the countries that won.</span></span> <span data-ttu-id="024d4-133">คุณสามารถใช้ Power Query Editorใช้ดำเนินการขั้นตอนการสร้างรูปร่างและล้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="024d4-133">You can use the Power Query Editor to perform these data shaping and cleansing steps.</span></span>

<span data-ttu-id="024d4-134">สิ่งแรก ลบแถวทั้งหมดยกเว้นสองแถวจากตาราง</span><span class="sxs-lookup"><span data-stu-id="024d4-134">First, remove all the columns except for two from the table.</span></span> <span data-ttu-id="024d4-135">เปลี่ยนชื่อแถวเป็น *ปี* และ *ประเทศ* ภายหลังกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="024d4-135">Rename these columns as *Year* and *Country* later in the process.</span></span>

1. <span data-ttu-id="024d4-136">ในกริดของ **Power Query Editor** เลือกแถว</span><span class="sxs-lookup"><span data-stu-id="024d4-136">In the **Power Query Editor** grid, select the columns.</span></span> <span data-ttu-id="024d4-137">เลือก Ctrl เพื่อเลือกหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="024d4-137">Select Ctrl to select multiple items.</span></span>

1. <span data-ttu-id="024d4-138">คลิกขวาและเลือก **ลบแถวอื่น** หรือเลือก **ลบแถว** > **ลบแถวอื่น** จากกลุ่ม **จัดการแถว** ใน **หน้าแรก** แถบริบบิ้นเพื่อลบแถวอื่นทั้งหมดจากตาราง</span><span class="sxs-lookup"><span data-stu-id="024d4-138">Right-click and select **Remove Other Columns**, or select **Remove Columns** > **Remove Other Columns** from the **Manage Columns** group in the **Home** ribbon tab, to remove all other columns from the table.</span></span>

   ![ลบแถวอื่นด้านล่างเมนู](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web6.png)

   <span data-ttu-id="024d4-140">หรือ</span><span class="sxs-lookup"><span data-stu-id="024d4-140">or</span></span>

   ![ribbon เอาคอลัมน์อื่น ๆ ออก](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage4.png)

<span data-ttu-id="024d4-142">ต่อไป ลบ *รายละเอียด* คำพิเศษจากเซลล์แถวแรก</span><span class="sxs-lookup"><span data-stu-id="024d4-142">Next, remove the extra word *Details* from the first column cells.</span></span>

1. <span data-ttu-id="024d4-143">เลือกแถวแรก</span><span class="sxs-lookup"><span data-stu-id="024d4-143">Select the first column.</span></span>

1. <span data-ttu-id="024d4-144">คลิกขวาและเลือก **แทนที่ค่า** หรือเลืกอ **แทนที่ค่า** จากกลุ่ม **เปลี่ยนแปลง** ใน **หน้าหลัก** แถบของริบบิ้น</span><span class="sxs-lookup"><span data-stu-id="024d4-144">Right-click, and select **Replace Values**, or select **Replace Values** from the **Transform** group in the **Home** tab of the ribbon.</span></span> <span data-ttu-id="024d4-145">ตัวเลือกนี้ยังพบได้ในกลุ่ม **ทุกแถว** ในแถบ **เปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="024d4-145">This option is also found in the **Any Column** group in the **Transform** tab.</span></span>

   ![แทนที่ค่าด้านล่างเมนู](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web7.png) 

   <span data-ttu-id="024d4-147">หรือ</span><span class="sxs-lookup"><span data-stu-id="024d4-147">or</span></span>

   ![แทนที่ค่า จากribbon](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web8a.png)

1. <span data-ttu-id="024d4-149">ในการโต้ตอบ **แทนที่ค่า** ประเภท **รายละเอียด** ในกล่องข้อความของ **ค่าเพื่อการค้นหา** ออกจากกล่องข้อความ **แทนที่ด้วย** ที่ว่างเปล่า แล้วเลือก **ตกลง** เพื่อลบคำ *รายละเอียด* จากแถว</span><span class="sxs-lookup"><span data-stu-id="024d4-149">In the **Replace Values** dialog, type **Details** in the **Value To Find** text box, leave the **Replace With** text box empty, and then select **OK** to delete the word *Details* from this column.</span></span>

   ![ลบคำจากแถว](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage6.png)

<span data-ttu-id="024d4-151">บางเซลล์มีเพียงคำว่า "ปี" แทนที่ค่าปี</span><span class="sxs-lookup"><span data-stu-id="024d4-151">Some cells contain only the word "Year" rather than year values.</span></span> <span data-ttu-id="024d4-152">คุณสามารถกรองแถวเพื่อแสดงเพียงแถวที่ไม่มีคำว่า "ปี"</span><span class="sxs-lookup"><span data-stu-id="024d4-152">You can filter the column to only display rows that don't contain the word "Year".</span></span>

1. <span data-ttu-id="024d4-153">เลือกตัวกรองที่ลูกศรด้านล่างบนแถว</span><span class="sxs-lookup"><span data-stu-id="024d4-153">Select the filter drop-down arrow on the column.</span></span>

1. <span data-ttu-id="024d4-154">ในเมนูด้านล่าง เลื่อนลงมาและลบกล่องเลือกข้างๆ ตัวเลือก **ปี** จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="024d4-154">In the drop-down menu, scroll down and clear the checkbox next to the **Year** option, and then select **OK**.</span></span>

   ![กรองข้อมูล](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage7.png)

<span data-ttu-id="024d4-156">เมื่อคุณกำลังมองหาข้อมูลผู้ชนะที่สุดท้ายอยู่ตอนนี้ คุณสามารถเปลี่ยนชื่อแถวที่สองเป็น  **ประเทศ**</span><span class="sxs-lookup"><span data-stu-id="024d4-156">Since you're only looking at the final winners data now, you can rename the second column to **Country**.</span></span> <span data-ttu-id="024d4-157">เพื่อเปลี่ยนชื่อคอลัมน์:</span><span class="sxs-lookup"><span data-stu-id="024d4-157">To rename the column:</span></span>

1. <span data-ttu-id="024d4-158">คลิกสองครั้งหรือกดและค้างไว้ที่หัวข้อแถวที่สองหรือ</span><span class="sxs-lookup"><span data-stu-id="024d4-158">Double-click or tap and hold in the second column header, or</span></span>
   - <span data-ttu-id="024d4-159">คลิกขวามที่หัวข้อแถว และเลือก **เปลี่ยนชื่อ** หรือ</span><span class="sxs-lookup"><span data-stu-id="024d4-159">Right-click the column header, and select **Rename**, or</span></span>
   - <span data-ttu-id="024d4-160">เลือกแถว\* และเลือก **เปลี่ยนชื่อ** จากกลุ่ม **ทุกแถว** ในแถบ **เปลี่ยนแปลง** ของริบบิ้น</span><span class="sxs-lookup"><span data-stu-id="024d4-160">Select the \*column and select **Rename** from the **Any Column** group in the **Transform** tab of the ribbon.</span></span>

   ![เปลี่ยนชื่อเมนูด้านล่าง](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage7a.png) 
  
   <span data-ttu-id="024d4-162">หรือ</span><span class="sxs-lookup"><span data-stu-id="024d4-162">or</span></span>

   ![เปลี่ยนชื่อจาก ribbon](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web8.png)

1. <span data-ttu-id="024d4-164">พิมพ์ **Country** ในส่วนหัวแล้วกด **Enter** เพื่อเปลี่ยนชื่อคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="024d4-164">Type **Country** in the header and press **Enter** to rename the column.</span></span>

<span data-ttu-id="024d4-165">คุณยังต้องการกรองแถวเช่น "2020" ที่มีค่า null ในคอลัมน์ **Country**</span><span class="sxs-lookup"><span data-stu-id="024d4-165">You also want to filter out rows like "2020" that have null values in the **Country** column.</span></span> <span data-ttu-id="024d4-166">คุณสามารถใช้เมนูตัวกรอง เช่นเดียวกับที่คุณได้ทำกับค่า **Year** หรือคุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="024d4-166">You could use the filter menu as you did with the **Year** values, or you can:</span></span>

1. <span data-ttu-id="024d4-167">คลิกขวาบนเซลล์ **Country** ในแถว **2020** ซึ่งมีค่าเป็น *null*</span><span class="sxs-lookup"><span data-stu-id="024d4-167">Right-click on the **Country** cell in the **2020** row, which has the value *null*.</span></span>

1. <span data-ttu-id="024d4-168">เลือก **ตัวกรองข้อความ** > **ไม่เท่ากับ** ในเมนูบริบทเพื่อเอาแถวใด ๆ ที่ประกอบด้วยค่าของเซลล์ดังกล่าวออก</span><span class="sxs-lookup"><span data-stu-id="024d4-168">Select **Text Filters** > **Does not Equal** in the context menu to remove any rows that contain that cell's value.</span></span>

   ![ตัวกรองข้อความ](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web11.png)

## <a name="import-the-query-into-report-view"></a><span data-ttu-id="024d4-170">นำเข้าคิวรีลงในมุมมองรายงาน</span><span class="sxs-lookup"><span data-stu-id="024d4-170">Import the query into Report View</span></span>

<span data-ttu-id="024d4-171">ตอนนี้คุณได้จัดรูปร่างข้อมูลตามที่คุณต้องการแล้ว คุณก็พร้อมที่จะตั้งชื่อคิวรีของคุณว่า "Euro Cup Winners" และนำเข้าข้อมูลลงในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="024d4-171">Now that you've shaped the data the way you want, you're ready to name your query "Euro Cup Winners" and import it into your report.</span></span>

1. <span data-ttu-id="024d4-172">ในพื้นที่ **ตั้งค่าแบบสอบถาม** ในกล่องข้อความ **ชื่อ** ใส่ **ผู้ชนะถ้วยรางวัลยูโร**</span><span class="sxs-lookup"><span data-stu-id="024d4-172">In the **Query Settings** pane, in the **Name** text box, enter **Euro Cup Winners**.</span></span>

   ![ตั้งชื่อคิวรี](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage8.png)

1. <span data-ttu-id="024d4-174">เลือก **ปิด & กำหนดใช้** > **ปิด & กำหนดใช้** จากแท็บ **หน้าแรก** ของ ribbon</span><span class="sxs-lookup"><span data-stu-id="024d4-174">Select **Close & Apply** > **Close & Apply** from the **Home** tab of the ribbon.</span></span>

   ![ปิดและนำไปใช้](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage9.png)

<span data-ttu-id="024d4-176">แบบสอบถามโหลดไปยังการแสดง *รายงาน* Power BI Desktop ที่คุณสามารถเห็นมันในแผง **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="024d4-176">The query loads into the Power BI Desktop *Report* view, where you can see it in the **Fields** pane.</span></span>

   ![บานหน้าต่างเขตข้อมูล](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage11.png)

>[!TIP]
><span data-ttu-id="024d4-178">คุณสามารถได้รับ Power Query Editor คืนมาหรือแก้ไขและทำให้แบบสอบถามคุณดีขึ้นโดย:</span><span class="sxs-lookup"><span data-stu-id="024d4-178">You can always get back to the Power Query Editor to edit and refine your query by:</span></span>
>- <span data-ttu-id="024d4-179">การเลือก **ตัวเลือกที่มากกว่า** การละไว้  ( **...** ) ข้างๆ **ผู้ชนะถ้วยยุโรป** ในแผง **เขตข้อมูล** แล้วเลือก **แก้ไขแบบสอบถาม** หรือ</span><span class="sxs-lookup"><span data-stu-id="024d4-179">Selecting the **More options** ellipsis (**...**) next to **Euro Cup Winners** in the **Fields** pane, and selecting **Edit Query**, or</span></span>
>- <span data-ttu-id="024d4-180">เลือก **แก้ไขคิวรี** > **แก้ไขคิวรี** ในกลุ่ม **ข้อมูลภายนอก** ของแท็บ ribbon **หน้าแรก** ในมุมมองรายงาน</span><span class="sxs-lookup"><span data-stu-id="024d4-180">Selecting **Edit Queries** > **Edit Queries** in the **External data** group of the **Home** ribbon tab in Report view.</span></span> 

## <a name="create-a-visualization"></a><span data-ttu-id="024d4-181">สร้างการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="024d4-181">Create a visualization</span></span>

<span data-ttu-id="024d4-182">เพื่อสร้างการแสดงภาพตามข้อมูลของคุณ:</span><span class="sxs-lookup"><span data-stu-id="024d4-182">To create a visualization based on your data:</span></span>

1. <span data-ttu-id="024d4-183">เลือกเขตข้อมูล **Country** ในบานหน้าต่าง **เขตข้อมูล** หรือลากเขตข้อมูลนี้ไปยังพื้นที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="024d4-183">Select the **Country** field in the **Fields** pane, or drag it to the report canvas.</span></span> <span data-ttu-id="024d4-184">Power BI Desktop รู้จักข้อมูลว่าเป็นชื่อประเทศ และสร้างแสดงภาพ **แผนที่** โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="024d4-184">Power BI Desktop recognizes the data as country names, and automatically creates a **Map** visualization.</span></span>

   ![การแสดงภาพของแผนที่](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web14.png)

1. <span data-ttu-id="024d4-186">ขยายแผนที่ โดยการลากจุดจับที่มุมเพื่อให้ชื่อประเทศที่เป็นแชมป์ทั้งหมดมองเห็นได้</span><span class="sxs-lookup"><span data-stu-id="024d4-186">Enlarge the map by dragging the handles in the corners so all the winning country names are visible.</span></span>  

   ![ขยายแผนที่](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage14.png)

1. <span data-ttu-id="024d4-188">แผนที่แสดงจุดข้อมูลสำหรับทุกประเทศที่เคยได้แชมป์ฟุตบอลยูโร</span><span class="sxs-lookup"><span data-stu-id="024d4-188">The map shows identical data points for every country that won a Euro Cup tournament.</span></span> <span data-ttu-id="024d4-189">เพื่อทำให้มีขนาดของแต่ละจุดข้อมูล แสดงจำนวนครั้งที่ประเทศได้แชมป์ ลากเขตข้อมูล **Year** ไปยัง **ลากเขตข้อมูลมาที่นี่** ภายใต้ **ขนาด** ในส่วนล่างของบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="024d4-189">To make the size of each data point reflect how often the country has won, drag the **Year** field to **Drag data fields here** under **Size** in the lower part of the **Visualizations** pane.</span></span> <span data-ttu-id="024d4-190">เขตข้อมูลจะเปลี่ยนเป็นหน่วยวัด **นับจำนวน Year** โดยอัตโนมัติ และการแสดงภาพของแผนที่ตอนนี้แสดงจุดข้อมูลขนาดใหญ่ขึ้นสำหรับประเทศที่เป็นแชมป์มากกว่า</span><span class="sxs-lookup"><span data-stu-id="024d4-190">The field automatically changes to a **Count of Year** measure, and the map visualization now shows larger data points for countries that have won more tournaments.</span></span>

   ![ลากจำนวนปีลงในขนาด](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage15.png)

## <a name="customize-the-visualization"></a><span data-ttu-id="024d4-192">การแสดงภาพที่กำหนดด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="024d4-192">Customize the visualization</span></span>

<span data-ttu-id="024d4-193">ตามที่คุณเห็น เป็นเรื่องง่ายมากที่จะสร้างการแสดงภาพจากข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="024d4-193">As you can see, it's very easy to create visualizations based on your data.</span></span> <span data-ttu-id="024d4-194">นอกจากนี้ยังเป็นเรื่องง่ายในการกำหนดการแสดงภาพของคุณ ให้นำเสนอข้อมูลในแบบที่คุณต้องการได้ดียิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="024d4-194">It's also easy to customize your visualizations to better present the data in ways that you want.</span></span>

### <a name="format-the-map"></a><span data-ttu-id="024d4-195">จัดรูปแบบแผนที่</span><span class="sxs-lookup"><span data-stu-id="024d4-195">Format the map</span></span>

<span data-ttu-id="024d4-196">คุณสามารถเปลี่ยนลักษณะของการแสดงภาพโดยเลือกที่วิชวล แล้วเลือกไอคอน **รูปแบบ** (รูปลูกกลิ้งทาสี) ในบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล** ได้</span><span class="sxs-lookup"><span data-stu-id="024d4-196">You can change the appearance of a visualization by selecting it and then selecting the **Format** (paint roller) icon in the **Visualizations** pane.</span></span> <span data-ttu-id="024d4-197">ตัวอย่างเช่น จุดข้อมูล "Germany" ในการแสดงภาพของคุณอาจทำให้เข้าใจผิดได้ เนื่องจากเยอรมนีตะวันตกชนะสองครั้ง และเยอรมนีชนะหนึ่งครั้ง และแผนที่แสดงเป็นจุดสองจุดซ้อนทับกัน แทนที่จะมาแยกหรือบวกเข้าด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="024d4-197">For example, the "Germany" data points in your visualization could be misleading, because West Germany won two tournaments and Germany won one, and the map superimposes the two points rather than separating or adding them together.</span></span> <span data-ttu-id="024d4-198">คุณสามารถลงสีให้สองจุดนี้มีสีแตกต่างกันเพื่อเน้นตรงนี้</span><span class="sxs-lookup"><span data-stu-id="024d4-198">You can color these two points differently to highlight this fact.</span></span> <span data-ttu-id="024d4-199">คุณยังสามารถตั้งชื่อให้แผนที่ เพื่อให้สื่อความหมายและน่าสนใจมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="024d4-199">You can also give the map a more descriptive and attractive title.</span></span>

1. <span data-ttu-id="024d4-200">เลือกที่การแสดงภาพ แล้วเลือกไอคอน **รูปแบบ** จากนั้นเลือก **สีของข้อมูล** เพื่อขยายตัวเลือกสีของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="024d4-200">With the visualization selected, select the **Format** icon, and then select **Data colors** to expand the data color options.</span></span>

   ![ไอคอนรูปแบบและการเลือกสีข้อมูล](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web15.png)

1. <span data-ttu-id="024d4-202">เปลี่ยนตัวเลือก **แสดงทั้งหมด** ให้เป็น **เปิด** จากนั้นเลือกรายการด้านล่างที่อยู่ถัดจาก **เยอรมนีตะวันตก** แล้วเลือกสีเหลือง</span><span class="sxs-lookup"><span data-stu-id="024d4-202">Turn **Show all** to **On**, and then select the drop-down menu next to **West Germany** and choose a yellow color.</span></span>

   ![เปลี่ยนสี](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web16.png)

1. <span data-ttu-id="024d4-204">เลือก **ชื่อเรื่อง** เพื่อขยายตัวเลือกชื่อเรื่อง และในเขตข้อมูล **ข้อความสำหรับชื่อเรื่อง** พิมพ์ **Euro Cup Winners** แทนชื่อเรื่องปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="024d4-204">Select **Title** to expand the title options, and in the **Title text** field, type **Euro Cup Winners** in place of the current title.</span></span>

1. <span data-ttu-id="024d4-205">เปลี่ยน **สีแบบอักษร** เป็นสีแดง **ขนาดของข้อความ** เป็น **12** และ **ตระกูลแบบอักษร** เป็น **Segoe (Bold)**</span><span class="sxs-lookup"><span data-stu-id="024d4-205">Change **Font color** to red, **Text size** to **12**, and **Font family** to **Segoe (Bold)**.</span></span>

   ![สีฟอนต์ ขนาด และครอบครัว](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web17.png)

<span data-ttu-id="024d4-207">การแสดงภาพแผนที่ของคุณ ตอนนี้มีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="024d4-207">Your map visualization now looks like this:</span></span>

![การแสดงภาพแผนที่ที่จัดรูปแบบแล้ว](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web18.png)

### <a name="change-the-visualization-type"></a><span data-ttu-id="024d4-209">การเปลี่ยนชนิดของการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="024d4-209">Change the visualization type</span></span>

<span data-ttu-id="024d4-210">คุณสามารถเปลี่ยนชนิดของการแสดงภาพ โดยเลือกที่ภาพดังกล่าว จากนั้น เลือกอีกไอคอนที่ด้านบนของแผง **การแสดงผลด้วยภาพ**</span><span class="sxs-lookup"><span data-stu-id="024d4-210">You can change the type of a visualization by selecting it and then selecting a different icon at the top of the **Visualizations** pane.</span></span> <span data-ttu-id="024d4-211">ตัวอย่างเช่น การแสดงภาพแผนที่ของคุณไม่มีข้อมูลสำหรับสหภาพโซเวียต และเชโกสโลวาเกีย เนื่องจากประเทศเหล่านั้นไม่มีอยู่บนแผนที่โลกอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="024d4-211">For example, your map visualization is missing the data for the Soviet Union and Czechoslovakia, because those countries no longer exist on the world map.</span></span> <span data-ttu-id="024d4-212">การแสดงภาพอื่น เช่นแผนที่ต้นไม้ หรือแผนภูมิวงกลม อาจแม่นยำกว่าเนื่องจากจะแสดงทุกค่า</span><span class="sxs-lookup"><span data-stu-id="024d4-212">Another type of visualization like a treemap or pie chart may be more accurate, because it shows all the values.</span></span>

<span data-ttu-id="024d4-213">เพื่อเปลี่ยนแผนที่ให้เป็นแผนภูมิวงกลม เลือกที่แผนที่ จากนั้นเลือกไอคอน **แผนภูมิวงกลม** ในแผง **การแสดงผลด้วยภาพ**</span><span class="sxs-lookup"><span data-stu-id="024d4-213">To change the map to a pie chart, select the map and then select the **Pie chart** icon in the **Visualizations** pane.</span></span>

![เปลี่ยนการแสดงผลด้วยภาพลงในแผนภูมิวงกลม](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/get-data-web19.png)

>[!TIP]
>- <span data-ttu-id="024d4-215">คุณสามารถใช้ตัวเลือกการจัดรูปแบบ **สีข้อมูล** เพื่อทำให้ "Germany" และ "West Germany" เป็นสีเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="024d4-215">You can use the **Data colors** formatting options to make "Germany" and "West Germany" the same color.</span></span> 
>- <span data-ttu-id="024d4-216">เพื่อจัดกลุ่มประเทศที่ได้แชมป์มากที่สุดไว้ด้วยกันบนแผนภูมิวงกลม เลือกที่การละไว้ ( **...** ) ที่มุมบนขวาของการแสดงผลด้วยภาพ จากนั้นเลือก **เรียงลำดับตามจำนวนของปี**</span><span class="sxs-lookup"><span data-stu-id="024d4-216">To group the countries with the most wins together on the pie chart, select the ellipsis (**...**) at the upper right of the visualization, and then select **Sort by Count of Year**.</span></span>

<span data-ttu-id="024d4-217">Power BI Desktop ให้ประสบการณ์ที่ราบรื่น ตั้งแต่การรับข้อมูลจากแหล่งข้อมูลต่าง ๆ และจัดรูปทรงให้ตรงกับความต้องการการวิเคราะห์ของคุณ ไปจนถึงการแสดงข้อมูลนี้ในแบบที่สวยงามและโต้ตอบได้</span><span class="sxs-lookup"><span data-stu-id="024d4-217">Power BI Desktop provides a seamless end-to-end experience, from getting data from a wide range of data sources and shaping it to meet your analysis needs, to visualizing this data in rich and interactive ways.</span></span> <span data-ttu-id="024d4-218">เมื่อรายงานของคุณพร้อมแล้ว คุณสามารถ[อัปโหลดไปยัง Power BI](../create-reports/desktop-upload-desktop-files.md)ได้ และสร้างแดชบอร์ดโดยยึดตามรายงานดังกล่าวที่คุณสามารถใช้ร่วมกันกับผู้ใช้ Power BI อื่นได้</span><span class="sxs-lookup"><span data-stu-id="024d4-218">Once your report is ready, you can [upload it to Power BI](../create-reports/desktop-upload-desktop-files.md) and create dashboards based on it, which you can share with other Power BI users.</span></span>

## <a name="see-also"></a><span data-ttu-id="024d4-219">อาจดูได้จาก</span><span class="sxs-lookup"><span data-stu-id="024d4-219">See also</span></span>

* [<span data-ttu-id="024d4-220">Microsoft Learn สำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="024d4-220">Microsoft Learn for Power BI</span></span>](/learn/powerplatform/power-bi?WT.mc_id=powerbi_landingpage-docs-link)
* [<span data-ttu-id="024d4-221">ดูวิดีโอ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="024d4-221">Watch Power BI Desktop videos</span></span>](../fundamentals/desktop-videos.md)
* [<span data-ttu-id="024d4-222">เยี่ยมชมกระดานสนทนา Power BI</span><span class="sxs-lookup"><span data-stu-id="024d4-222">Visit the Power BI Forum</span></span>](https://go.microsoft.com/fwlink/?LinkID=519326)
* [<span data-ttu-id="024d4-223">อ่านบล็อก Power BI</span><span class="sxs-lookup"><span data-stu-id="024d4-223">Read the Power BI Blog</span></span>](https://go.microsoft.com/fwlink/?LinkID=519327)