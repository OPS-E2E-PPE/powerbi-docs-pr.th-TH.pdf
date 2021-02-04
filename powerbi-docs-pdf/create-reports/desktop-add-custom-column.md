---
title: เพิ่มคอลัมน์แบบกำหนดเองใน Power BI Desktop
description: สร้างคอลัมน์แบบกำหนดเองใหม่ใน Power BI Desktop ได้อย่างรวดเร็ว
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 12/14/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 88a77f7bb626b8e6395650c96cd957ab11600179
ms.sourcegitcommit: 46cf62d9bb33ac7b7eae7910fbba6756f626c65f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/15/2020
ms.locfileid: "97492138"
---
# <a name="add-a-custom-column-in-power-bi-desktop"></a><span data-ttu-id="ffb75-103">เพิ่มคอลัมน์แบบกำหนดเองใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ffb75-103">Add a custom column in Power BI Desktop</span></span>

<span data-ttu-id="ffb75-104">ใน Power BI Desktop คุณสามารถเพิ่มคอลัมน์ของข้อมูลแบบกำหนดเองใหม่ลงในแบบจำลองของคุณได้อย่างง่ายดายโดยใช้ตัวแก้ไขคิวรี</span><span class="sxs-lookup"><span data-stu-id="ffb75-104">In Power BI Desktop, you can easily add a new custom column of data to your model by using Query Editor.</span></span> <span data-ttu-id="ffb75-105">ด้วยตัวแก้ไขคิวรี คุณสามารถสร้างและเปลี่ยนชื่อคอลัมน์แบบกำหนดเองของคุณเพื่อสร้าง[คิวรีสูตร PowerQuery M](/powerquery-m/quick-tour-of-the-power-query-m-formula-language) สำหรับกำหนดคอลัมน์แบบกำหนดเองของคุณ</span><span class="sxs-lookup"><span data-stu-id="ffb75-105">With Query Editor, you create and rename your custom column to create [PowerQuery M formula queries](/powerquery-m/quick-tour-of-the-power-query-m-formula-language) to define your custom column.</span></span> <span data-ttu-id="ffb75-106">คิวรีสูตร PowerQuery M มี[ชุดเนื้อหาการอ้างอิงฟังก์ชันที่ครอบคลุม](/powerquery-m/power-query-m-function-reference)</span><span class="sxs-lookup"><span data-stu-id="ffb75-106">PowerQuery M formula queries have a [comprehensive function reference content set](/powerquery-m/power-query-m-function-reference).</span></span> 

<span data-ttu-id="ffb75-107">เมื่อคุณสร้างคอลัมน์แบบกำหนดเองในตัวแก้ไขคิวรีแล้ว Power BI Desktop จะเพิ่มคอลัมน์เป็น **ขั้นตอนที่ใช้** ใน **การตั้งค่าคิวรี** ของคิวรี</span><span class="sxs-lookup"><span data-stu-id="ffb75-107">When you create a custom column in Query Editor, Power BI Desktop adds it as an **Applied Step** in the **Query Settings** of the query.</span></span> <span data-ttu-id="ffb75-108">ซึ่งสามารถเปลี่ยนแปลง ย้าย หรือแก้ไขได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="ffb75-108">It can be changed, moved, or modified at any time.</span></span>

![สกรีนช็อตแสดงกล่องโต้ตอบเพิ่มคอลัมน์แบบกำหนดเอง](media/desktop-add-custom-column/add-custom-column_01.png)

## <a name="use-query-editor-to-add-a-custom-column"></a><span data-ttu-id="ffb75-110">ใช้ตัวแก้ไขคิวรีเพื่อเพิ่มคอลัมน์แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ffb75-110">Use Query Editor to add a custom column</span></span>

<span data-ttu-id="ffb75-111">เมื่อต้องการเริ่มต้นการสร้างคอลัมน์แบบกำหนดเอง ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="ffb75-111">To start creating a custom column, follow these steps:</span></span>

1. <span data-ttu-id="ffb75-112">เปิดใช้งาน Power BI Desktop และโหลดข้อมูลบางส่วน</span><span class="sxs-lookup"><span data-stu-id="ffb75-112">Launch Power BI Desktop and load some data.</span></span>

2. <span data-ttu-id="ffb75-113">จากแท็บ **หน้าแรก** บนริบบอน ให้เลือก **แก้ไขคิวรี** จากนั้นเลือก **แก้ไขคิวรี** จากเมนู</span><span class="sxs-lookup"><span data-stu-id="ffb75-113">From the **Home** tab on the ribbon, select **Edit Queries**, and then select **Edit Queries** from the menu.</span></span>

   ![เลือกแก้ไขคิวรี](media/desktop-add-custom-column/add-column-from-example_02.png)

   <span data-ttu-id="ffb75-115">หน้าต่าง **ตัวแก้ไขคิวรี** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="ffb75-115">The **Query Editor** window appears.</span></span> 

2. <span data-ttu-id="ffb75-116">จากแท็บ **เพิ่มคอลัมน์** บนริบบอน ให้เลือก **คอลัมน์แบบกำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="ffb75-116">From the **Add Column** tab on the ribbon, select **Custom Column**.</span></span>

   ![เลือกคอลัมน์แบบกำหนดเอง](media/desktop-add-custom-column/add-custom-column_02.png)

   <span data-ttu-id="ffb75-118">หน้าต่าง **เพิ่มคอลัมน์แบบกำหนดเอง** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="ffb75-118">The **Add Custom Column** window appears.</span></span>

## <a name="the-add-custom-column-window"></a><span data-ttu-id="ffb75-119">หน้าต่างเพิ่มคอลัมน์แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ffb75-119">The Add Custom Column window</span></span>

<span data-ttu-id="ffb75-120">หน้าต่าง **เพิ่มคอลัมน์แบบกำหนดเอง** มีคุณลักษณะดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ffb75-120">The **Add Custom Column** window has the following features:</span></span> 
- <span data-ttu-id="ffb75-121">รายการของคอลัมน์ที่มีให้เลือกใช้งาน ในรายการ **คอลัมน์ที่มีให้เลือกใช้งาน** ทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="ffb75-121">A list of available columns, in the **Available columns** list on the right.</span></span>

- <span data-ttu-id="ffb75-122">ชื่อเริ่มต้นของคอลัมน์แบบกำหนดเองของคุณ ในกล่อง **ชื่อคอลัมน์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="ffb75-122">The initial name of your custom column, in the **New column name** box.</span></span> <span data-ttu-id="ffb75-123">คุณสามารถเปลี่ยนชื่อคอลัมน์นี้ได้</span><span class="sxs-lookup"><span data-stu-id="ffb75-123">You can rename this column.</span></span>

- <span data-ttu-id="ffb75-124">[คิวรีสูตร PowerQuery M](/powerquery-m/power-query-m-function-reference) ในกล่อง **สูตรคอลัมน์แบบกำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="ffb75-124">[PowerQuery M formula queries](/powerquery-m/power-query-m-function-reference), in the **Custom column formula** box.</span></span> <span data-ttu-id="ffb75-125">คุณสามารถสร้างคิวรีเหล่านี้ด้วยการสร้างสูตรบนคอลัมน์แบบกำหนดเองที่คุณกำหนดขึ้นใหม่</span><span class="sxs-lookup"><span data-stu-id="ffb75-125">You create these queries by building the formula on which your new custom column is defined.</span></span> 

   ![สกรีนช็อตแสดงกล่องโต้ตอบเพิ่มคอลัมน์แบบกำหนดเอง ซึ่งประกอบด้วยคอลัมน์ที่มีให้เลือก](media/desktop-add-custom-column/add-custom-column_03.png)

## <a name="create-formulas-for-your-custom-column"></a><span data-ttu-id="ffb75-127">สร้างสูตรสำหรับคอลัมน์แบบกำหนดเองของคุณ</span><span class="sxs-lookup"><span data-stu-id="ffb75-127">Create formulas for your custom column</span></span>

1. <span data-ttu-id="ffb75-128">เลือกคอลัมน์จากรายการ **คอลัมน์ที่มีให้เลือกใช้งาน** ทางด้านขวา แล้วเลือก **แทรก** ใต้รายการเพื่อเพิ่มลงในสูตรของคอลัมน์แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ffb75-128">Select a column from the **Available columns** list on the right, and then select **Insert** below the list to add them to the custom column formula.</span></span> <span data-ttu-id="ffb75-129">นอกจากนี้ คุณยังสามารถเพิ่มคอลัมน์ได้โดยการดับเบิลคลิกคอลัมน์ในรายการด้วย</span><span class="sxs-lookup"><span data-stu-id="ffb75-129">You can also add a column by double-clicking it in the list.</span></span>

2. <span data-ttu-id="ffb75-130">เมื่อคุณป้อนสูตรและสร้างคอลัมน์ของคุณ ให้สังเกตตัวบ่งชี้ที่ด้านล่างของหน้าต่าง **เพิ่มคอลัมน์แบบกำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="ffb75-130">As you enter the formula and build your column, note the indicator in the bottom of the **Add Custom Column** window.</span></span> 

   <span data-ttu-id="ffb75-131">ถ้าไม่มีข้อผิดพลาด คุณจะเห็นเครื่องหมายถูกสีเขียวและข้อความ *ไม่ตรวจพบข้อผิดพลาดทางไวยากรณ์*</span><span class="sxs-lookup"><span data-stu-id="ffb75-131">If there are no errors, you'll see a green check mark and the message *No syntax errors have been detected*.</span></span>

   ![ตรวจสอบไวยากรณ์เรียบร้อยแล้วในหน้าเพิ่มคอลัมน์แบบกำหนดเอง](media/desktop-add-custom-column/add-custom-column_04.png)

   <span data-ttu-id="ffb75-133">ถ้ามีข้อผิดพลาดทางไวยากรณ์ คุณจะเห็นไอคอนคำเตือนสีเหลืองพร้อมกับลิงก์เชื่อมโยงไปยังตำแหน่งที่มีข้อผิดพลาดเกิดขึ้นในสูตรของคุณ</span><span class="sxs-lookup"><span data-stu-id="ffb75-133">If there's a syntax error, you'll see a yellow warning icon, along with a link to where the error occurred in your formula.</span></span>

   ![ข้อผิดพลาดในหน้าเพิ่มคอลัมน์แบบกำหนดเอง](media/desktop-add-custom-column/add-custom-column_05.png)

3. <span data-ttu-id="ffb75-135">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ffb75-135">Select **OK**.</span></span> 

   <span data-ttu-id="ffb75-136">Power BI Desktop จะเพิ่มคอลัมน์แบบกำหนดเองของคุณไปยังแบบจำลอง และเพิ่มขั้นตอน **แบบกำหนดเองที่เพิ่ม** เข้ามาในรายการ **ขั้นตอนที่ใช้** ของคิวรีของคุณใน **การตั้งค่าคิวรี**</span><span class="sxs-lookup"><span data-stu-id="ffb75-136">Power BI Desktop adds your custom column to the model, and adds the **Added Custom** step to your query's **Applied Steps** list in **Query Settings**.</span></span>

   ![คอลัมน์แบบกำหนดเองที่เพิ่มไปยังการตั้งค่าคิวรี](media/desktop-add-custom-column/add-custom-column_06.png)

4. <span data-ttu-id="ffb75-138">เมื่อต้องการปรับเปลี่ยนคอลัมน์แบบกำหนดเอง ให้ดับเบิลคลิกที่ขั้นตอน **แบบกำหนดเองที่เพิ่ม** ในรายการ **ขั้นตอนที่ใช้**</span><span class="sxs-lookup"><span data-stu-id="ffb75-138">To modify your custom column, double-click the **Added Custom** step in the **Applied Steps** list.</span></span> 

   <span data-ttu-id="ffb75-139">หน้าต่าง **เพิ่มคอลัมน์แบบกำหนดเอง** จะปรากฏขึ้นพร้อมสูตรคอลัมน์แบบกำหนดเองที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="ffb75-139">The **Add Custom Column** window appears with the custom column formula you created.</span></span>

## <a name="use-the-advanced-editor-for-custom-columns"></a><span data-ttu-id="ffb75-140">ใช้เครื่องมือแก้ไขขั้นสูงสำหรับคอลัมน์แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="ffb75-140">Use the Advanced Editor for custom columns</span></span>

<span data-ttu-id="ffb75-141">หลังจากที่คุณได้สร้างคิวรีของคุณแล้ว คุณยังสามารถใช้ **เครื่องมือแก้ไขขั้นสูง** เพื่อปรับเปลี่ยนขั้นตอนใดก็ตามของคิวรีของคุณได้</span><span class="sxs-lookup"><span data-stu-id="ffb75-141">After you've created your query, you can also use the **Advanced Editor** to modify any step of your query.</span></span> <span data-ttu-id="ffb75-142">ในการทำเช่นนั้น ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="ffb75-142">To do so, follow these steps:</span></span>

1. <span data-ttu-id="ffb75-143">ในหน้าต่าง **ตัวแก้ไขคิวรี** ให้เลือกแท็บ **มุมมอง** บนริบบอน</span><span class="sxs-lookup"><span data-stu-id="ffb75-143">In the **Query Editor** window, select the **View** tab on the ribbon.</span></span> 

2. <span data-ttu-id="ffb75-144">เลือก **ตัวแก้ไขขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="ffb75-144">Select **Advanced Editor**.</span></span>

   <span data-ttu-id="ffb75-145">หน้า **เครื่องมือแก้ไขขั้นสูง** จะปรากฏขึ้น ซึ่งช่วยให้คุณสามารถควบคุมคิวรีของคุณได้อย่างสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ffb75-145">The **Advanced Editor** page appears, which gives you full control over your query.</span></span> 

   ![หน้าเครื่องมือแก้ไขขั้นสูง](media/desktop-add-custom-column/add-custom-column_07.png)

   
## <a name="next-steps"></a><span data-ttu-id="ffb75-147">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="ffb75-147">Next steps</span></span>

- <span data-ttu-id="ffb75-148">คุณสามารถสร้างคอลัมน์แบบกำหนดเองได้ด้วยวิธีการอื่น เช่น การสร้างคอลัมน์ตามตัวอย่างที่คุณกำหนดไว้สำหรับตัวแก้ไขคิวรี</span><span class="sxs-lookup"><span data-stu-id="ffb75-148">You can create a custom column in other ways, such as creating a column based on examples you provide to Query Editor.</span></span> <span data-ttu-id="ffb75-149">สำหรับข้อมูลเพิ่มเติม โปรดดู[เพิ่มคอลัมน์จากตัวอย่างใน Power BI Desktop](desktop-add-column-from-example.md)</span><span class="sxs-lookup"><span data-stu-id="ffb75-149">For more information, see [Add a column from an example in Power BI Desktop](desktop-add-column-from-example.md).</span></span>

- <span data-ttu-id="ffb75-150">สำหรับข้อมูลการอ้างอิง Power Query M โปรดดู [การอ้างอิงฟังก์ชัน Power Query M](/powerquery-m/power-query-m-function-reference)</span><span class="sxs-lookup"><span data-stu-id="ffb75-150">For Power Query M reference information, see [Power Query M function reference](/powerquery-m/power-query-m-function-reference).</span></span>