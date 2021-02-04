---
title: เพิ่มคอลัมน์จากตัวอย่างใน Power BI Desktop
description: สร้างคอลัมน์ใหม่ใน Power BI Desktop ที่ใช้คอลัมน์ที่มีอยู่เป็นตัวอย่างได้อย่างรวดเร็ว
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 01/16/2019
LocalizationGroup: Create reports
ms.openlocfilehash: f33a9f5656875825b70c7e51202431ba268fe86a
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414518"
---
# <a name="add-a-column-from-examples-in-power-bi-desktop"></a><span data-ttu-id="2576d-103">เพิ่มคอลัมน์จากตัวอย่างใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2576d-103">Add a column from examples in Power BI Desktop</span></span>
<span data-ttu-id="2576d-104">ด้วย *เพิ่มคอลัมน์จากตัวอย่าง* ในตัวแก้ไข Power Query คุณสามารถเพิ่มคอลัมน์ใหม่ลงในแบบจำลองข้อมูลของคุณได้ง่ายๆ โดยการให้ค่าตัวอย่างอย่างน้อยหนึ่งรายการสำหรับคอลัมน์ใหม่</span><span class="sxs-lookup"><span data-stu-id="2576d-104">With *add column from examples* in Power Query Editor, you can add new columns to your data model simply by providing one or more example values for the new columns.</span></span> <span data-ttu-id="2576d-105">คุณสามารถสร้างตัวอย่างคอลัมน์ใหม่จากส่วนที่เลือกหรือใส่ค่าที่ยึดตามคอลัมน์ที่มีอยู่ทั้งหมดในตารางได้</span><span class="sxs-lookup"><span data-stu-id="2576d-105">You can create the new column examples from a selection, or provide input based on all existing columns in the table.</span></span>

![ภาพหน้าจอของ Power Query Editor ที่แสดงวิธีการเพิ่มคอลัมน์จากตัวอย่างใน Power B I Desktop](media/desktop-add-column-from-example/add-column-from-example_01.png)

<span data-ttu-id="2576d-107">การใช้ *เพิ่มคอลัมน์จากตัวอย่าง* ช่วยให้คุณสร้างคอลัมน์ใหม่ได้อย่างรวดเร็วและง่ายดาย และเหมาะสำหรับสถานการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2576d-107">Using *add column from example* lets you quickly and easily create new columns, and is great for the following situations:</span></span>

- <span data-ttu-id="2576d-108">คุณทราบข้อมูลผลลัพธ์ที่คุณต้องการในคอลัมน์ใหม่ของคุณ แต่คุณไม่แน่ใจว่าการแปลง หรือคอลเลกชันของการแปลงไหน ที่จะช่วยคุณให้ได้ผลลัพธ์นั้น</span><span class="sxs-lookup"><span data-stu-id="2576d-108">You know the data you want in your new column, but you're not sure which transformation, or collection of transformations, will get you there.</span></span>
- <span data-ttu-id="2576d-109">คุณทราบการแปลงที่จำเป็น แต่คุณไม่แน่ใจจะเลือกตำแหน่งไหน ในส่วนติดต่อผู้ใช้ เพื่อให้ได้ผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="2576d-109">You already know which transformations you need, but you're not sure what to select in the UI to make them happen.</span></span>
- <span data-ttu-id="2576d-110">คุณทราบทั้งหมดเกี่ยวกับการแปลงที่คุณต้องใช้ ด้วยนิพจน์ *คอลัมน์แบบกำหนดเอง* ในภาษา *M* แต่หนึ่ง (หรือหลาย) นิพจน์เหล่านั้นไม่มีอยู่ใน UI</span><span class="sxs-lookup"><span data-stu-id="2576d-110">You know all about the transformations you need using a *Custom Column* expression in *M* language, but one or more of those expressions aren't available in the UI.</span></span>

<span data-ttu-id="2576d-111">การเพิ่มคอลัมน์จากตัวอย่างนั้นเป็นเรื่องง่ายและตรงไปตรงมา</span><span class="sxs-lookup"><span data-stu-id="2576d-111">Adding a column from an example is easy and straightforward.</span></span> <span data-ttu-id="2576d-112">ส่วนต่อไปจะแสดงให้เห็นว่า สามารถทำได้ง่ายเพียงใด</span><span class="sxs-lookup"><span data-stu-id="2576d-112">The next sections show just how easy it is.</span></span>

## <a name="add-a-new-column-from-examples"></a><span data-ttu-id="2576d-113">เพิ่มคอลัมน์ใหม่จากตัวย่าง</span><span class="sxs-lookup"><span data-stu-id="2576d-113">Add a new column from examples</span></span>

<span data-ttu-id="2576d-114">หากต้องการรับข้อมูลตัวอย่างจากวิกิพีเดียเลือก **รับข้อมูล** > **เว็บ** จากแท็บ **หน้าแรก** ของ ribbon Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2576d-114">To get sample data from Wikipedia, select **Get Data** > **Web** from the **Home** tab of the Power BI Desktop ribbon.</span></span> 

![รับข้อมูลจากเว็บ](media/desktop-add-column-from-example/add-column-from-example_02.png)

<span data-ttu-id="2576d-116">วาง URL ต่อไปนี้ลงในกล่องโต้ตอบที่ปรากฏขึ้นและเลือก **ตกลง**:</span><span class="sxs-lookup"><span data-stu-id="2576d-116">Paste the following URL into the dialog that appears, and select **OK**:</span></span> 

<span data-ttu-id="2576d-117">*https:\//wikipedia.org/wiki/List_of_states_and_territories_of_the_United_States*</span><span class="sxs-lookup"><span data-stu-id="2576d-117">*https:\//wikipedia.org/wiki/List_of_states_and_territories_of_the_United_States*</span></span>

<span data-ttu-id="2576d-118">ในกล่องโต้ตอบ **ตัวนำทาง** เลือกตารางรัฐ **ของสหรัฐอเมริกา** และจากนั้นเลือก **แปลงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="2576d-118">In the **Navigator** dialog box, select the **States of the United States of America** table, and then select **Transform Data**.</span></span> <span data-ttu-id="2576d-119">ตารางเปิดในตัวแก้ไข Power Query</span><span class="sxs-lookup"><span data-stu-id="2576d-119">The table opens in Power Query Editor.</span></span>

<span data-ttu-id="2576d-120">หรือเมื่อต้องการเปิดข้อมูลที่โหลดแล้วจาก Power BI Desktop ให้เลือก **แก้ไขคิวรี** จากแท็บ **Home** ของ ribbon</span><span class="sxs-lookup"><span data-stu-id="2576d-120">Or, to open already-loaded data from Power BI Desktop, select **Edit Queries** from the **Home** tab of the ribbon.</span></span> <span data-ttu-id="2576d-121">ข้อมูลจะเปิดในตัวแก้ไข Power Query</span><span class="sxs-lookup"><span data-stu-id="2576d-121">The data opens in Power Query Editor.</span></span> 

![เลือกแก้ไขคิวรีจาก Power BI Desktop](media/desktop-add-column-from-example/add-column-from-example_05.png)

<span data-ttu-id="2576d-123">เมื่อเปิดข้อมูลตัวอย่างในตัวแก้ไข Power Query แล้ว เลือกแท็บ **เพิ่มคอลัมน์** บน ribbon แล้้วเลือก **คอลัมน์จากตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="2576d-123">Once the sample data opens in Power Query Editor, select the **Add Column** tab on the ribbon, and then select **Column from Examples**.</span></span> <span data-ttu-id="2576d-124">เลือกไอคอน **คอลัมน์จากตัวอย่าง** เพื่อสร้างคอลัมน์จากคอลัมน์ที่มีอยู่ หรือเลือกลูกศรแบบดรอปดาวน์เพื่อเลือกระหว่าง **จากคอลัมน์ทั้งหมด** หรือ **จากรายการเลือก**</span><span class="sxs-lookup"><span data-stu-id="2576d-124">Select the **Column From Examples** icon itself to create the column from all existing columns, or select the drop-down arrow to choose between **From All Columns** or **From Selection**.</span></span> <span data-ttu-id="2576d-125">สำหรับการฝึกปฏิบัตินี ้ให้ใช้ **จากคอลัมน์ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="2576d-125">For this walkthrough, use **From All Columns**.</span></span>

![เลือก เพิ่มคอลัมน์จากตัวอย่าง](media/desktop-add-column-from-example/add-column-from-example_03.png)

## <a name="add-column-from-examples-pane"></a><span data-ttu-id="2576d-127">บานหน้าต่าง เพิ่มคอลัมน์จากตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="2576d-127">Add Column From Examples pane</span></span>
<span data-ttu-id="2576d-128">เมื่อคุณเลือก **เพิ่มคอลัมน์** > **จากตัวอย่าง** บานหน้าต่าง **เพิ่มคอลัมน์จากตัวอย่าง** จะเปิดขึ้นที่ด้านบนของตาราง</span><span class="sxs-lookup"><span data-stu-id="2576d-128">When you select **Add Column** > **From Examples**, the **Add Column From Examples** pane opens at the top of the table.</span></span> <span data-ttu-id="2576d-129">**คอลัมน์่ 1** ใหม่จะปรากฏทางด้านขวาของคอลัมน์ที่มีอยู่ (คุณอาจต้องเลื่อนเพื่อดูทั้งหมด)</span><span class="sxs-lookup"><span data-stu-id="2576d-129">The new **Column 1** appears to the right of the existing columns (you may need to scroll to see them all).</span></span> <span data-ttu-id="2576d-130">เมื่อคุณใส่ค่าตัวอย่างของคุณในเซลล์ที่ว่างเปล่าของ **คอลัมน์ 1** Power BI จะสร้างกฎและการแปลงเพื่อให้ตรงกับตัวอย่างของคุณและใช้ข้อมูลเหล่านั้นเพื่อเติมส่วนที่เหลือของคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="2576d-130">When you enter your example values in the blank cells of **Column 1**, Power BI creates rules and transformations to match your examples, and uses them to fill the rest of the column.</span></span>

<span data-ttu-id="2576d-131">โปรดสังเกตว่า **คอลัมน์จากตัวอย่าง** จะปรากฏเป็น **ขั้นตอนที่ใช้** ในบานหน้าต่าง **การตั้งค่าคิวรี**</span><span class="sxs-lookup"><span data-stu-id="2576d-131">Notice that **Column From Examples** also appears as an **Applied Step** in the **Query Settings** pane.</span></span> <span data-ttu-id="2576d-132">ดังเช่นเคย ตัวแก้ไข Power Query จะบันทึกขั้นตอนการแปลงของคุณ และปรับใช้กับคิวรีตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="2576d-132">As always, Power Query Editor records your transformation steps and applies them to the query in order.</span></span>

![บานหน้าต่าง เพิ่มคอลัมน์จากตัวอย่าง](media/desktop-add-column-from-example/add-column-from-example_04.png)

<span data-ttu-id="2576d-134">ขณะที่คุณพิมพ์ตัวอย่างของคุณในคอลัมน์ใหม่ Power BI ให้คุณเห็นตัวอย่าง ว่าคอลัมน์ส่วนที่เหลือจะมีหน้าตาเป็นอย่างไรจากการแปลงที่ตรวจพบ</span><span class="sxs-lookup"><span data-stu-id="2576d-134">As you type your example in the new column, Power BI shows a preview of how the rest of the column will look, based on the transformations it creates.</span></span> <span data-ttu-id="2576d-135">ตัวอย่างเช่น ถ้าคุณพิมพ์ *Alabama* ในแถวแรก ที่สอดคล้องกับค่า **Alabama** ในคอลัมน์แรกของตาราง</span><span class="sxs-lookup"><span data-stu-id="2576d-135">For example, if you type *Alabama* in the first row, it corresponds to the **Alabama** value in the first column of the table.</span></span> <span data-ttu-id="2576d-136">ทันทีที่คุณกด Enter Power BI จะเติมในส่วนที่เหลือของคอลัมน์ใหม่โดยยึดตามค่าคอลัมน์แรก และตั้งชื่อคอลัมน์ **ชื่อและตัวย่อไปรษณีย์ [12]-สำเนา**</span><span class="sxs-lookup"><span data-stu-id="2576d-136">As soon as you press Enter, Power BI fills in the rest of the new column based on the first column value, and names the column **Name & postal abbreviation[12] - Copy**.</span></span>

<span data-ttu-id="2576d-137">ในตอนนี้ให้ไปที่แถว **แมสซาชูเซตส์ [E]** ของคอลัมน์ใหม่และลบส่วน **[E]** ของสตริง</span><span class="sxs-lookup"><span data-stu-id="2576d-137">Now go to the **Massachusetts[E]** row of the new column and delete the **[E]** portion of the string.</span></span> <span data-ttu-id="2576d-138">Power BI ตรวจพบการเปลี่ยนแปลง และใช้ตัวอย่างเพื่อสร้างการแปลง</span><span class="sxs-lookup"><span data-stu-id="2576d-138">Power BI detects the change and uses the example to create a transformation.</span></span> <span data-ttu-id="2576d-139">Power BI อธิบายการแปลงในบานหน้าต่าง **เพิ่มคอลัมน์จากตัวอย่าง** และเปลี่ยนชื่อคอลัมน์เป็น **ข้อความก่อนตัวคั่น**</span><span class="sxs-lookup"><span data-stu-id="2576d-139">Power BI describes the transformations in the **Add Column From Examples** pane, and renames the column to **Text Before Delimiter.**</span></span> 

![คอลัมน์ที่แปลงแล้วจากตัวอย่าง](media/desktop-add-column-from-example/add-column-from-example_06.png)

<span data-ttu-id="2576d-141">เมื่อคุณดำเนินการต่อกับตัวอย่าง ตัวแก้ไข Power Query ก็เพิ่มการแปลงที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="2576d-141">As you continue to provide examples, Power Query Editor adds to the transformations.</span></span> <span data-ttu-id="2576d-142">เมื่อคุณพอใจแล้ว เลือก **ตกลง** เพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="2576d-142">When you're satisfied, select **OK** to commit your changes.</span></span> 

<span data-ttu-id="2576d-143">คุณสามารถเปลี่ยนชื่อคอลัมน์ใหม่ได้ตามที่คุณต้องการโดยการคลิกสองครั้งที่ส่วนหัวของคอลัมน ์หรือคลิกขวาและเลือก **เปลี่ยนชื่อ**</span><span class="sxs-lookup"><span data-stu-id="2576d-143">You can rename the new column whatever you want by double-clicking the column heading, or right-clicking it and selecting **Rename**.</span></span> 

<span data-ttu-id="2576d-144">ดูวิดีโอนี้เพื่อดู **เพิ่มคอลัมน์จากตัวอย่าง** ในการดำเนินการโดยใช้แหล่งข้อมูลตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="2576d-144">Watch this video to see **Add Column From Examples** in action, using the sample data source:</span></span> 

<span data-ttu-id="2576d-145">[Power BI Desktop: เพิ่มคอลัมน์จากตัวอย่าง](https://www.youtube.com/watch?v=-ykbVW9wQfw)</span><span class="sxs-lookup"><span data-stu-id="2576d-145">[Power BI Desktop: Add Column From Examples](https://www.youtube.com/watch?v=-ykbVW9wQfw).</span></span> 

## <a name="list-of-supported-transformations"></a><span data-ttu-id="2576d-146">รายการการแปลงข้อมูลที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="2576d-146">List of supported transformations</span></span>
<span data-ttu-id="2576d-147">การเปลี่ยนแปลงจำนวนมากแต่ไม่สามารถใช้ได้เมื่อใช้ **เพิ่มคอลัมน์จากตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="2576d-147">Many but not all transformations are available when using **Add Column from Examples**.</span></span> <span data-ttu-id="2576d-148">รายการต่อไปนี้แสดงการแปลงข้อมูลที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="2576d-148">The following list shows the supported transformations:</span></span>

<span data-ttu-id="2576d-149">**ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="2576d-149">**General**</span></span>

- <span data-ttu-id="2576d-150">คอลัมน์แบบมีเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="2576d-150">Conditional Column</span></span>

<span data-ttu-id="2576d-151">**การอ้างอิง**</span><span class="sxs-lookup"><span data-stu-id="2576d-151">**Reference**</span></span>
  
- <span data-ttu-id="2576d-152">การอ้างอิงถึงคอลัมน์ที่กำหนด ซึ่งรวมถึงตัดแต่ง ทำความสะอาด และการแปลงกรณี</span><span class="sxs-lookup"><span data-stu-id="2576d-152">Reference to a specific column, including trim, clean, and case transformations</span></span>

<span data-ttu-id="2576d-153">**การแปลงข้อความ**</span><span class="sxs-lookup"><span data-stu-id="2576d-153">**Text transformations**</span></span>

- <span data-ttu-id="2576d-154">การรวม (สนับสนุนการผสมกันระหว่าง สตริงที่เป็นสัญพจน์ และค่าของทั้งคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="2576d-154">Combine (supports combination of literal strings and entire column values)</span></span>
- <span data-ttu-id="2576d-155">แทนที่</span><span class="sxs-lookup"><span data-stu-id="2576d-155">Replace</span></span>
- <span data-ttu-id="2576d-156">ความยาว</span><span class="sxs-lookup"><span data-stu-id="2576d-156">Length</span></span>
- <span data-ttu-id="2576d-157">แยก</span><span class="sxs-lookup"><span data-stu-id="2576d-157">Extract</span></span>   
  - <span data-ttu-id="2576d-158">อักษรหลายตัวแรก</span><span class="sxs-lookup"><span data-stu-id="2576d-158">First Characters</span></span>
  - <span data-ttu-id="2576d-159">อักษรหลายตัวสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="2576d-159">Last Characters</span></span>
  - <span data-ttu-id="2576d-160">ช่วง</span><span class="sxs-lookup"><span data-stu-id="2576d-160">Range</span></span>
  - <span data-ttu-id="2576d-161">ข้อความก่อนตัวคั่น</span><span class="sxs-lookup"><span data-stu-id="2576d-161">Text before Delimiter</span></span>
  - <span data-ttu-id="2576d-162">ข้อความหลังตัวคั่น</span><span class="sxs-lookup"><span data-stu-id="2576d-162">Text after Delimiter</span></span>
  - <span data-ttu-id="2576d-163">ข้อความระหว่างตัวคั่น</span><span class="sxs-lookup"><span data-stu-id="2576d-163">Text between Delimiters</span></span>
  - <span data-ttu-id="2576d-164">ความยาว</span><span class="sxs-lookup"><span data-stu-id="2576d-164">Length</span></span>
  - <span data-ttu-id="2576d-165">เอาตัวอักษรออก</span><span class="sxs-lookup"><span data-stu-id="2576d-165">Remove Characters</span></span>
  - <span data-ttu-id="2576d-166">เก็บตัวอักษรไว้</span><span class="sxs-lookup"><span data-stu-id="2576d-166">Keep Characters</span></span>

> [!NOTE]
> <span data-ttu-id="2576d-167">การแปลง *ข้อความ* ทั้งหมด โดยคำนึงถึงการแปลงค่าของคอลัมน์โดย การตัดแต่ง ทำความสะอาด หรือการตัวพิมพ์เล็ก/ใหญ่ ที่จำเป็นด้วย</span><span class="sxs-lookup"><span data-stu-id="2576d-167">All *Text* transformations take into account the potential need to trim, clean, or apply a case transformation to the column value.</span></span>

<span data-ttu-id="2576d-168">**แปลงวันที่**</span><span class="sxs-lookup"><span data-stu-id="2576d-168">**Date transformations**</span></span>

- <span data-ttu-id="2576d-169">วัน</span><span class="sxs-lookup"><span data-stu-id="2576d-169">Day</span></span>
- <span data-ttu-id="2576d-170">วันของสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="2576d-170">Day of Week</span></span>
- <span data-ttu-id="2576d-171">ชื่อวันของสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="2576d-171">Day of Week Name</span></span>
- <span data-ttu-id="2576d-172">วันของปี</span><span class="sxs-lookup"><span data-stu-id="2576d-172">Day of Year</span></span>
- <span data-ttu-id="2576d-173">เดือน</span><span class="sxs-lookup"><span data-stu-id="2576d-173">Month</span></span>
- <span data-ttu-id="2576d-174">ชื่อเดือน</span><span class="sxs-lookup"><span data-stu-id="2576d-174">Month Name</span></span>
- <span data-ttu-id="2576d-175">ไตรมาสของปี</span><span class="sxs-lookup"><span data-stu-id="2576d-175">Quarter of Year</span></span>
- <span data-ttu-id="2576d-176">สัปดาห์ของเดือน</span><span class="sxs-lookup"><span data-stu-id="2576d-176">Week of Month</span></span>
- <span data-ttu-id="2576d-177">สัปดาห์ของปี</span><span class="sxs-lookup"><span data-stu-id="2576d-177">Week of Year</span></span>
- <span data-ttu-id="2576d-178">ปี</span><span class="sxs-lookup"><span data-stu-id="2576d-178">Year</span></span>
- <span data-ttu-id="2576d-179">อายุ</span><span class="sxs-lookup"><span data-stu-id="2576d-179">Age</span></span>
- <span data-ttu-id="2576d-180">วันเริ่มต้นปี</span><span class="sxs-lookup"><span data-stu-id="2576d-180">Start of Year</span></span>
- <span data-ttu-id="2576d-181">วันสิ้นปี</span><span class="sxs-lookup"><span data-stu-id="2576d-181">End of Year</span></span>
- <span data-ttu-id="2576d-182">วันเริ่มต้นเดือน</span><span class="sxs-lookup"><span data-stu-id="2576d-182">Start of Month</span></span>
- <span data-ttu-id="2576d-183">วันสิ้นเดือน</span><span class="sxs-lookup"><span data-stu-id="2576d-183">End of Month</span></span>
- <span data-ttu-id="2576d-184">วันเริ่มต้นไตรมาส</span><span class="sxs-lookup"><span data-stu-id="2576d-184">Start of Quarter</span></span>
- <span data-ttu-id="2576d-185">จำนวนวันในเดือน</span><span class="sxs-lookup"><span data-stu-id="2576d-185">Days in Month</span></span>
- <span data-ttu-id="2576d-186">วันสิ้นไตรมาส</span><span class="sxs-lookup"><span data-stu-id="2576d-186">End of Quarter</span></span>
- <span data-ttu-id="2576d-187">วันเริ่มต้นสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="2576d-187">Start of Week</span></span>
- <span data-ttu-id="2576d-188">วันสิ้นสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="2576d-188">End of Week</span></span>
- <span data-ttu-id="2576d-189">วันของเดือน</span><span class="sxs-lookup"><span data-stu-id="2576d-189">Day of Month</span></span>
- <span data-ttu-id="2576d-190">เวลาเริ่มต้นของวัน</span><span class="sxs-lookup"><span data-stu-id="2576d-190">Start of Day</span></span>
- <span data-ttu-id="2576d-191">เวลาสิ้นสุดของวัน</span><span class="sxs-lookup"><span data-stu-id="2576d-191">End of Day</span></span>

<span data-ttu-id="2576d-192">**การแปลงเวลา**</span><span class="sxs-lookup"><span data-stu-id="2576d-192">**Time transformations**</span></span>

- <span data-ttu-id="2576d-193">Hour</span><span class="sxs-lookup"><span data-stu-id="2576d-193">Hour</span></span>
- <span data-ttu-id="2576d-194">นาที</span><span class="sxs-lookup"><span data-stu-id="2576d-194">Minute</span></span>
- <span data-ttu-id="2576d-195">วินาที</span><span class="sxs-lookup"><span data-stu-id="2576d-195">Second</span></span>  
- <span data-ttu-id="2576d-196">แปลงเป็นเวลาท้องถิ่น</span><span class="sxs-lookup"><span data-stu-id="2576d-196">To Local Time</span></span>

> [!NOTE]
> <span data-ttu-id="2576d-197">การแปลง *วันที่* และ *เวลา* ทั้งหมด โดยคำนึงถึงการแปลงค่าของคอลัมน์ไปเป็น *วันที่* หรือ *เวลา* หรือ *วันที่เวลา* ที่จำเป็นด้วย</span><span class="sxs-lookup"><span data-stu-id="2576d-197">All *Date* and *Time* transformations take into account the potential need to convert the column value to *Date* or *Time* or *DateTime*.</span></span>

<span data-ttu-id="2576d-198">**การแปลงตัวเลข**</span><span class="sxs-lookup"><span data-stu-id="2576d-198">**Number transformations**</span></span> 

- <span data-ttu-id="2576d-199">ค่าสัมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="2576d-199">Absolute Value</span></span>
- <span data-ttu-id="2576d-200">อาร์กโคไซน์</span><span class="sxs-lookup"><span data-stu-id="2576d-200">Arccosine</span></span>
- <span data-ttu-id="2576d-201">อาร์กไซน์</span><span class="sxs-lookup"><span data-stu-id="2576d-201">Arcsine</span></span>
- <span data-ttu-id="2576d-202">อาร์กแทนเจนต์</span><span class="sxs-lookup"><span data-stu-id="2576d-202">Arctangent</span></span>
- <span data-ttu-id="2576d-203">แปลงเป็นตัวเลข</span><span class="sxs-lookup"><span data-stu-id="2576d-203">Convert to Number</span></span>
- <span data-ttu-id="2576d-204">โคไซน์</span><span class="sxs-lookup"><span data-stu-id="2576d-204">Cosine</span></span>
- <span data-ttu-id="2576d-205">ยกกำลังสาม</span><span class="sxs-lookup"><span data-stu-id="2576d-205">Cube</span></span>
- <span data-ttu-id="2576d-206">หาร</span><span class="sxs-lookup"><span data-stu-id="2576d-206">Divide</span></span>
- <span data-ttu-id="2576d-207">เลขชี้กำลัง</span><span class="sxs-lookup"><span data-stu-id="2576d-207">Exponent</span></span>
- <span data-ttu-id="2576d-208">แฟกทอเรียล</span><span class="sxs-lookup"><span data-stu-id="2576d-208">Factorial</span></span>
- <span data-ttu-id="2576d-209">หารจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="2576d-209">Integer Divide</span></span>
- <span data-ttu-id="2576d-210">เป็นเลขคู่</span><span class="sxs-lookup"><span data-stu-id="2576d-210">Is Even</span></span>
- <span data-ttu-id="2576d-211">เป็นเลขคี่</span><span class="sxs-lookup"><span data-stu-id="2576d-211">Is Odd</span></span>
- <span data-ttu-id="2576d-212">ลอการิทึมฐานธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="2576d-212">Ln</span></span>
- <span data-ttu-id="2576d-213">ลอการิทึมฐาน 10</span><span class="sxs-lookup"><span data-stu-id="2576d-213">Base-10 Logarithm</span></span>
- <span data-ttu-id="2576d-214">มอดุโล</span><span class="sxs-lookup"><span data-stu-id="2576d-214">Modulo</span></span>
- <span data-ttu-id="2576d-215">คูณ</span><span class="sxs-lookup"><span data-stu-id="2576d-215">Multiply</span></span>
- <span data-ttu-id="2576d-216">ปัดเศษลง</span><span class="sxs-lookup"><span data-stu-id="2576d-216">Round Down</span></span>
- <span data-ttu-id="2576d-217">ปัดเศษขึ้น</span><span class="sxs-lookup"><span data-stu-id="2576d-217">Round Up</span></span>
- <span data-ttu-id="2576d-218">เครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="2576d-218">Sign</span></span>
- <span data-ttu-id="2576d-219">ไซน์</span><span class="sxs-lookup"><span data-stu-id="2576d-219">Sin</span></span>
- <span data-ttu-id="2576d-220">รากที่สอง</span><span class="sxs-lookup"><span data-stu-id="2576d-220">Square Root</span></span>
- <span data-ttu-id="2576d-221">ยกกำลังสอง</span><span class="sxs-lookup"><span data-stu-id="2576d-221">Square</span></span>
- <span data-ttu-id="2576d-222">ลบ</span><span class="sxs-lookup"><span data-stu-id="2576d-222">Subtract</span></span>
- <span data-ttu-id="2576d-223">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="2576d-223">Sum</span></span>
- <span data-ttu-id="2576d-224">แทนเจนต์</span><span class="sxs-lookup"><span data-stu-id="2576d-224">Tangent</span></span>
- <span data-ttu-id="2576d-225">บักเก็ต/ช่วง</span><span class="sxs-lookup"><span data-stu-id="2576d-225">Bucketing/Ranges</span></span>
