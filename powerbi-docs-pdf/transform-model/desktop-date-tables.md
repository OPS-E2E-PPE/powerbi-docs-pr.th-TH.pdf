---
title: ตั้งค่า และใช้งานตารางวันที่ใน Power BI Desktop
description: เรียนรู้วิธีการตั้งค่าตารางเป็นตารางวันที่ และความหมายของมันใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: conceptual
ms.date: 05/08/2019
LocalizationGroup: Model your data
ms.openlocfilehash: 1a0782e7a80cc8d2cc824effe07a99df7ec64785
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415829"
---
# <a name="set-and-use-date-tables-in-power-bi-desktop"></a><span data-ttu-id="3cd43-103">ตั้งค่า และใช้งานตารางวันที่ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3cd43-103">Set and use date tables in Power BI Desktop</span></span>

<span data-ttu-id="3cd43-104">**Power BI Desktop** กำหนดคอลัมน์ที่แสดงวันที่อยู่เบื้องหลัง แล้วสร้างลำดับชั้นของวันที่ และเปิดให้ใช้เมตาดาต้าสำหรับรูปแบบข้อมูลของคุณ โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3cd43-104">**Power BI Desktop** works behind the scenes to automatically identify columns that represent dates, and then creates date hierarchies and other enabling metadata for your model, on your behalf.</span></span> <span data-ttu-id="3cd43-105">คุณสามารถใช้ลำดับชั้นที่มีอยู่แล้วเหล่านี้ตอนสร้างรายงาน เช่นวิชวล ตาราง การวัดผลด่วน ตัวแบ่งส่วนข้อมูล และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="3cd43-105">You can then use those built-in hierarchies when creating report features like visuals, tables, quick measures, slicers, and so on.</span></span> <span data-ttu-id="3cd43-106">Power BI Desktop ทำงานโดยการสร้างตารางที่ซ่อนอยู่ภายในให้กับคุณ ที่คุณสามารถนำไปใช้ต่อในรายงานและนิพจน์ DAX ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3cd43-106">Power BI Desktop does this by creating hidden tables on your behalf, which you can then use for your reports and DAX expressions.</span></span>

<span data-ttu-id="3cd43-107">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลักษณะการทำงานอัตโนมัตินี้ ให้อ่านบทความ [วันที่/เวลาอัตโนมัติใน Power BI Desktop](desktop-auto-date-time.md)</span><span class="sxs-lookup"><span data-stu-id="3cd43-107">For more information about this automatic behavior, read the [Auto date/time in Power BI Desktop](desktop-auto-date-time.md) article.</span></span>

<span data-ttu-id="3cd43-108">นักวิเคราะห์ข้อมูลหลายคนต้องการสร้างตารางวันที่ของพวกเขาเองมากกว่า ซึ่งก็สามารถทำได้</span><span class="sxs-lookup"><span data-stu-id="3cd43-108">Many data analysts prefer to create their own date tables, which is fine.</span></span> <span data-ttu-id="3cd43-109">ใน **Power BI Desktop** คุณสามารถระบุตารางที่คุณต้องการใช้เป็น **ตารางวันที่** และสร้างวิชวล ตาราง การวัดผลด่วน ฯลฯ ที่เกี่ยวกับวันที่ โดยใช้ข้อมูลของตารางดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="3cd43-109">In **Power BI Desktop**, you can specify the table you want your model to use as its **date table**, and subsequently create date-related visuals, tables, quick measures, and so on, using that table's date data.</span></span> <span data-ttu-id="3cd43-110">เมื่อคุณระบุตารางวันที่ของคุณเอง คุณควบคุมลำดับชั้นของวันที่ ที่สร้างขึ้นในรูปแบบของคุณ และใช้งานใน **การวัดผลด่วน** และการดำเนินการอื่น ๆ ที่ใช้ตารางวันที่ของรูปแบบคุณ</span><span class="sxs-lookup"><span data-stu-id="3cd43-110">When you specify your own date table, you control the date hierarchies created in your model, and use them in **quick measures** and other operations that use your model's date table.</span></span>

![ภาพหน้าจอของ Power B I Desktop ที่แสดงกล่องโต้ตอบ “ทำเครื่องหมายเป็นตารางวันที่”](media/desktop-date-tables/date-tables_01.png)

## <a name="setting-your-own-date-table"></a><span data-ttu-id="3cd43-112">การตั้งค่าตารางวันของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="3cd43-112">Setting your own date table</span></span>

<span data-ttu-id="3cd43-113">เมื่อต้องการตั้งค่า **ตารางวันที่** เลือกตารางคุณต้องการใช้เป็นตารางวันที่ในบานหน้าต่าง **เขตข้อมูล** จากนั้นคลิกขวาที่ตารางแล้วเลือก **ทำเครื่องหมายเป็นตารางวันที่ > ทำเครื่องหมายเป็นตารางวันที่** ในเมนูที่ปรากฏขึ้น ดังแสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3cd43-113">To set a **date table** select the table you want to use as a date table in the **Fields** pane, then right-click the table and select **Mark as date table > Mark as date table** in the menu that appears, as shown in the following image.</span></span>

![ภาพหน้าจอของ Power B I Desktop ที่แสดงตัวเลือกตัวกรอง “ทำเครื่องหมายเป็นตารางวันที่” ในบานหน้าต่างเขตข้อมูล](media/desktop-date-tables/date-tables_02.png)

<span data-ttu-id="3cd43-115">คุณยังสามารถเลือกตาราง แล้วเลือก **ทำเครื่องหมายเป็นตารางวันที่** จาก ribbon **การวางรูปแบบ** ดังแสดงในที่นี้</span><span class="sxs-lookup"><span data-stu-id="3cd43-115">You can also select the table and then select **Mark as Date Table** from the **Modeling** ribbon, shown here.</span></span>

![ภาพหน้าจอของ Power B I Desktop ที่แสดงตัวกรองปุ่มและตัวเลือก “ทำเครื่องหมายเป็นตารางวันที่”](media/desktop-date-tables/date-tables_02b.png)

<span data-ttu-id="3cd43-117">เมื่อคุณระบุ **ตารางวันที่** ด้วยตนเอง Power BI Desktop จะทำการตรวจสอบคอลัมน์และข้อมูลของมัน เพื่อให้แน่ใจว่าข้อมูลดังกล่าว:</span><span class="sxs-lookup"><span data-stu-id="3cd43-117">When you specify your own **date table**, Power BI Desktop performs the following validations of that column and its data, to ensure that the data:</span></span>

* <span data-ttu-id="3cd43-118">มีค่าที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="3cd43-118">contains unique values</span></span>
* <span data-ttu-id="3cd43-119">ไม่มีค่า null</span><span class="sxs-lookup"><span data-stu-id="3cd43-119">contains no null values</span></span>
* <span data-ttu-id="3cd43-120">มีวันที่ต่อเนื่องกัน (จากเริ่มต้นถึงสิ้นสุด)</span><span class="sxs-lookup"><span data-stu-id="3cd43-120">contains contiguous date values (from beginning to end)</span></span>
* <span data-ttu-id="3cd43-121">ถ้าเป็นชนิดข้อมูล **วันที่/เวลา** แต่ละค่าจะต้องประทับเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="3cd43-121">if it is a **Date/Time** data type, it has the same timestamp across each value</span></span>

<span data-ttu-id="3cd43-122">มีสองสถานการณ์ที่คุณน่าจะได้การสร้างตารางวันที่ของคุณเอง ซึ่งล้วนสมเหตุสมผล:</span><span class="sxs-lookup"><span data-stu-id="3cd43-122">There are two likely scenarios for creating your own date table, either of which is a reasonable approach:</span></span>

* <span data-ttu-id="3cd43-123">สถานการณ์แรกคือ เมื่อคุณใช้ตารางวันที่และลำดับชั้น มาตรฐานหรือพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="3cd43-123">The first scenario is when you use a canonical, or basic date table and hierarchy.</span></span> <span data-ttu-id="3cd43-124">ซึ่งก็คือตารางในข้อมูลคุณ ที่ผ่านเกณฑ์การตรวจสอบตารางวันที่ ที่ได้อธิบายไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="3cd43-124">This is a table in your data that meets the previously described validation criteria for a date table.</span></span> 

* <span data-ttu-id="3cd43-125">สถานการณ์ที่สองคือ เมื่อคุณใช้ตารางจาก Analysis Services ที่มีเขตข้อมูล *dim date* ที่คุณต้องการใช้เป็นตารางวันที่ของคุณ เป็นต้น</span><span class="sxs-lookup"><span data-stu-id="3cd43-125">The second scenario is where you use a table from Analysis Services, for example, with a *dim date* field that you want to use as your date table.</span></span> 

<span data-ttu-id="3cd43-126">หลังจากที่คุณระบุตารางวันที่แล้ว คุณสามารถเลือกคอลัมน์ในตารางที่จะเป็นคอลัมน์วันที่</span><span class="sxs-lookup"><span data-stu-id="3cd43-126">Once you specify a date table, you can select which column in that table is the date column.</span></span> <span data-ttu-id="3cd43-127">คุณสามารถระบุคอลัมน์ที่จะใช้ โดยการเลือกตารางในบานหน้าต่าง **เขตข้อมูล** จากนั้นคลิกขวาที่ตาราง แล้วเลือก **ทำเครื่องหมายเป็นตารางวันที่ > การตั้งค่าตารางวันที่**</span><span class="sxs-lookup"><span data-stu-id="3cd43-127">You can specify which column to use by selecting the table in the **Fields** pane, then right-click the table and select **Mark as date table > Date table settings**.</span></span> <span data-ttu-id="3cd43-128">หน้าต่างต่อไปนี้จะปรากฏขึ้นมา ซึ่งคุณสามารถเลือกคอลัมน์ที่จะใช้เป็นตารางวันที่จากกล่องรายการดรอปดาวน์</span><span class="sxs-lookup"><span data-stu-id="3cd43-128">The following window appears, where you can select the column to use as the date table from the drop-down box.</span></span>

![ภาพหน้าจอของ Power B I Desktop ที่แสดงกล่องโต้ตอบ “ทำเครื่องหมายเป็นตารางวันที่” ที่มีหมายเหตุสำคัญ](media/desktop-date-tables/date-tables_03.png)

<span data-ttu-id="3cd43-130">สิ่งสำคัญที่ต้องทราบคือ เมื่อคุณระบุตารางวันที่ของคุณเอง **Power BI Desktop** จะไม่สร้างลำดับชั้นโดยอัตโนมัติลงในรูปแบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="3cd43-130">It's important to note that when you specify your own date table, **Power BI Desktop** does not auto-create the hierarchies that it would otherwise build into your model on your behalf.</span></span> <span data-ttu-id="3cd43-131">ถ้าคุณยกเลิกเลือกตารางวันที่ของคุณในภายหลัง (และไม่มีตารางวันที่ที่กำหนดด้วยตนเองอีก) Power BI Desktop จะสร้างตารางวันที่ใหม่ให้โดยอัตโนัติ สำหรับคอลัมน์วันที่ในตาราง</span><span class="sxs-lookup"><span data-stu-id="3cd43-131">If you later deselect your date table (and no longer have a manually set date table), Power BI Desktop recreates the automatically created built-in date tables for you, for the date columns in the table.</span></span>

<span data-ttu-id="3cd43-132">อีกสิ่งสำคัญที่ต้องทราบคือ เมื่อคุณกำหนดตารางให้เป็นตารางวันที่ ตารางวันที่ภายในที่ Power BI Desktop สร้างขึ้นโดยอัตโนมัติ จะถูกเอาออก และวิชวลหรือนิพจน์ DAX ที่คุณสร้างไว้ก่อนหน้านี้โดยใช้ตารางดังกล่าวจะไม่ทำงานอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="3cd43-132">Also important to note is that when you mark a table as a date table, the built-in (automatically created) date table that Power BI Desktop created is removed, and any visuals or DAX expressions you previously created based on those built-in tables will no longer work properly.</span></span> 

## <a name="marking-your-date-table-as-the-appropriate-data-type"></a><span data-ttu-id="3cd43-133">การกำหนดชนิดข้อมูลของตารางวันที่ให้เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="3cd43-133">Marking your date table as the appropriate data type</span></span>

<span data-ttu-id="3cd43-134">เมื่อคุณระบุ **ตารางวันที่** ของตัวเอง คุณจะต้องแน่ใจว่า ชนิดข้อมูลถูกตั้งค่าอย่างเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="3cd43-134">When you specify your own **date table**, you need to make sure the data type is properly set.</span></span> <span data-ttu-id="3cd43-135">คุณจะต้องการตั้งค่า **ชนิดข้อมูล** ไปเป็น **วันที่/เวลา** หรือ **วันที่**</span><span class="sxs-lookup"><span data-stu-id="3cd43-135">You want to set the **Data type** to **Date/Time** or **Date**.</span></span> <span data-ttu-id="3cd43-136">ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3cd43-136">Take the following steps to do so:</span></span>

1. <span data-ttu-id="3cd43-137">เลือก **ตารางวันที่** ของคุณจากบานหน้าต่าง **เขตข้อมูล** ขยายมันถ้าจำเป็น จากนั้นเลือกคอลัมน์ที่จะใช้เป็นวันที่</span><span class="sxs-lookup"><span data-stu-id="3cd43-137">Select your **date table** from the **Fields** pane, expand it if necessary, and then select the column to be used as the date.</span></span>
   
    ![ภาพหน้าจอของ Power B I Desktop ที่แสดงตัวกรองวันที่ในบานหน้าต่างเขตข้อมูล](media/desktop-date-tables/date-tables_04.png) 

2. <span data-ttu-id="3cd43-139">บนแท็บ **การวางรูปแบบ** เลือก **ชนิดข้อมูล:** แล้วคลิกลูกศรดรอปดาวน์เพื่อแสดงชนิดข้อมูลที่มีให้</span><span class="sxs-lookup"><span data-stu-id="3cd43-139">On the **Modeling** tab, select **Data type:** and then click the drop-down arrow to show available data types.</span></span>

    ![ภาพหน้าจอของ Power B I Desktop ที่แสดงแท็บการวางรูปแบบที่มีตัวกรองชนิดข้อมูลที่เลือกไว้](media/desktop-date-tables/date-tables_05.png)

3. <span data-ttu-id="3cd43-141">ระบุชนิดข้อมูลสำหรับคอลัมน์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3cd43-141">Specify the data type for your column.</span></span> 


## <a name="next-steps"></a><span data-ttu-id="3cd43-142">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3cd43-142">Next steps</span></span>

<span data-ttu-id="3cd43-143">สำหรับข้อมูลเพิ่มเติมที่เกี่ยวข้องกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3cd43-143">For more information related to this article, check out the following resources:</span></span>

* [<span data-ttu-id="3cd43-144">วันที่/เวลาอัตโนมัติใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3cd43-144">Auto date/time in Power BI Desktop</span></span>](desktop-auto-date-time.md)
* [<span data-ttu-id="3cd43-145">สร้างตารางวันที่ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3cd43-145">Create date tables in Power BI Desktop</span></span>](../guidance/model-date-tables.md)
* [<span data-ttu-id="3cd43-146">ชนิดข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3cd43-146">Data types in Power BI Desktop</span></span>](../connect-data/desktop-data-types.md)
* <span data-ttu-id="3cd43-147">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3cd43-147">Questions?</span></span> [<span data-ttu-id="3cd43-148">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="3cd43-148">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
* <span data-ttu-id="3cd43-149">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="3cd43-149">Suggestions?</span></span> [<span data-ttu-id="3cd43-150">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="3cd43-150">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com/)
