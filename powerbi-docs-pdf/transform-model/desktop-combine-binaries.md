---
title: รวมไฟล์ (ไบนารี) ใน Power BI Desktop
description: รวมไฟล์ (ไบนารี) แหล่งข้อมูลใน Power BI Desktop ได้อย่างง่ายดาย
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: how-to
ms.date: 01/13/2020
LocalizationGroup: Transform and shape data
ms.openlocfilehash: bf75a5656de956be5ddd38330d659cba06e30455
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415852"
---
# <a name="combine-files-binaries-in-power-bi-desktop"></a><span data-ttu-id="7ffb0-103">รวมไฟล์ (ไบนารี) ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="7ffb0-103">Combine files (binaries) in Power BI Desktop</span></span>

<span data-ttu-id="7ffb0-104">นี่เป็นวิธีการทรงพลังในการนำเข้าข้อมูลสู่ **Power BI Desktop**: ถ้าคุณมีไฟล์หลายไฟล์ที่มีเค้าร่างเดียวกัน ให้รวมไฟล์เหล่านั้นลงในตารางแบบลอจิคัลเดียว</span><span class="sxs-lookup"><span data-stu-id="7ffb0-104">Here's a powerful approach to importing data into **Power BI Desktop**: If you have multiple files that have the same schema, combine them into a single logical table.</span></span> <span data-ttu-id="7ffb0-105">วิธีการยอดนิยมนี้ได้รับการปรับให้มีความสะดวกสบาย และใช้ได้อย่างกว้างขว้างมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="7ffb0-105">This popular technique has been made more convenient and more expansive.</span></span>

<span data-ttu-id="7ffb0-106">เพื่อเริ่มขั้นตอนการรวมไฟล์จากโฟลเดอร์เดียวกัน ให้เลือก **รับข้อมูล** และเลือก **ไฟล์** > **โฟลเดอร์** แล้วจึงเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="7ffb0-106">To start the process of combining files from the same folder, select **Get Data**, choose **File** > **Folder**, and then select **Connect**.</span></span>

![เชื่อมต่อกับไฟล์โฟลเดอร์ กล่องโต้ตอบรับข้อมูล Power BI Desktop](media/desktop-combine-binaries/combine-binaries_1.png)

<span data-ttu-id="7ffb0-108">ใส่เส้นทางของโฟลเดอร์ เลือก **ตกลง** จากนั้นเลือก **แปลงข้อมูล** เพื่อดูไฟล์ของโฟลเดอร์ในตัวแก้ไข Power Query</span><span class="sxs-lookup"><span data-stu-id="7ffb0-108">Enter the folder path, select **OK**, and then select **Transform Data** to see the folder's files in Power Query Editor.</span></span>

## <a name="combine-files-behavior"></a><span data-ttu-id="7ffb0-109">รูปแบบการรวมไฟล์</span><span class="sxs-lookup"><span data-stu-id="7ffb0-109">Combine files behavior</span></span>

<span data-ttu-id="7ffb0-110">เมื่อต้องการรวมไฟล์ไบนารีในตัวแก้ไข Power Query ให้เลือก **เนื้อหา** (ป้ายชื่อคอลัมน์แรก) และเลือก **หน้าแรก** > **รวมไฟล์**</span><span class="sxs-lookup"><span data-stu-id="7ffb0-110">To combine binary files in Power Query Editor, select **Content** (the first column label) and select **Home** > **Combine Files**.</span></span> <span data-ttu-id="7ffb0-111">หรือเพียงคุณเลือกไอคอน **รวมไฟล์** ที่อยู่ข้าง **เนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="7ffb0-111">Or you can just select the **Combine Files** icon next to **Content**.</span></span>

![คำสั่งรวมไฟล์ ตัวแก้ไข Power Query Power BI Desktop](media/desktop-combine-binaries/combine-binaries_2a.png)

<span data-ttu-id="7ffb0-113">*รวมไฟล์* จะมีการดำเนินการดังนี้:</span><span class="sxs-lookup"><span data-stu-id="7ffb0-113">The *combine files* transform behaves as follows:</span></span>

* <span data-ttu-id="7ffb0-114">การแปลงไฟล์รวมจะวิเคราะห์แต่ละไฟล์ที่นำเข้าเพื่อพิจารณารูปแบบไฟล์ที่ถูกต้องในการใช้งาน เช่น *ข้อความ* *เวิร์กบุ๊ก Excel* หรือ *ไฟล์ JSON*</span><span class="sxs-lookup"><span data-stu-id="7ffb0-114">The combine files transform analyzes each input file to determine the correct file format to use, such as *text*, *Excel workbook*, or *JSON file*.</span></span>
* <span data-ttu-id="7ffb0-115">การแปลงจะให้คุณเลือกวัตถุที่ระบุจากไฟล์แรก เช่น เวิร์กบุ๊ก Excel ที่จะดึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7ffb0-115">The transform allows you to select a specific object from the first file, such as an Excel workbook, to extract.</span></span>
  
  ![กล่องโต้ตอบรวมไฟล์ ตัวแก้ไข Power Query Power BI Desktop](media/desktop-combine-binaries/combine-binaries_3.png)
* <span data-ttu-id="7ffb0-117">จากนั้นการแปลงไฟล์รวมจะใช้การดำเนินการเหล่านี้โดยอัตโนมัติ:</span><span class="sxs-lookup"><span data-stu-id="7ffb0-117">The combine files transform then automatically takes these actions:</span></span>
  
  * <span data-ttu-id="7ffb0-118">สร้างคิวรีต้นแบบที่ดำเนินการกับข้อมูลทุกขั้นตอนกับไฟล์เดียว</span><span class="sxs-lookup"><span data-stu-id="7ffb0-118">Creates an example query that performs all the required extraction steps in a single file.</span></span>
  * <span data-ttu-id="7ffb0-119">สร้างการ *การสอบถามฟังก์ชัน* ที่มีไฟล์ไบนารีเป็นพารามิเตอร์ไปยัง *คิวรีต้นแบบ*</span><span class="sxs-lookup"><span data-stu-id="7ffb0-119">Creates a *function query* that parameterizes the file/binary input to the *exemplar query*.</span></span> <span data-ttu-id="7ffb0-120">คิวรีต้นแบบและการสอบถามฟังก์ชัน มีการเชื่อมโยงกัน เพื่อให้เปลี่ยนแปลงในคิวรีต้นแบบ สะท้อนมาในแบบสอบถามฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="7ffb0-120">The exemplar query and the function query are linked, so that changes to the exemplar query are reflected in the function query.</span></span>
  * <span data-ttu-id="7ffb0-121">ใช้  *ฟังก์ชันคิวรี* กับคิวรีเดิมที่มีการป้อนข้อมูลไบนารี เช่น คิวรี *โฟลเดอร์* </span><span class="sxs-lookup"><span data-stu-id="7ffb0-121">Applies the *function query* to the original query with input binaries, such as the *Folder* query.</span></span> <span data-ttu-id="7ffb0-122">ซึ่งจะใช้ฟังก์ชันคิวรีสำหรับการนำเข้าข้อมูลไบนารีในแต่ละแถว จากนั้นจะขยายการแยกข้อมูลที่เป็นผลลัพธ์เป็นคอลัมน์ระดับบนสุด</span><span class="sxs-lookup"><span data-stu-id="7ffb0-122">It applies the function query for binary inputs on each row, then expands the resulting data extraction as top-level columns.</span></span>

    ![ผลลัพธ์การแปลงไฟล์รวม ตัวแก้ไข Power Query Power BI Desktop](media/desktop-combine-binaries/combine-binaries_4.png)

> [!NOTE]
> <span data-ttu-id="7ffb0-124">ขอบเขตรายการที่เลือกของคุณในเวิร์กบุ๊ก Excel จะมีผลต่อรูปแบบของการรวมไบนารี่</span><span class="sxs-lookup"><span data-stu-id="7ffb0-124">The scope of your selection in an Excel workbook will affect the behavior of combine binaries.</span></span> <span data-ttu-id="7ffb0-125">เช่น คุณสามารถเลือกเวิร์กชีตเพื่อรวมเวิร์กชีตดังกล่าว หรือเลือกรากเพื่อรวมไฟล์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7ffb0-125">For example, you can select a specific worksheet to combine that worksheet, or select the root to combine the full file.</span></span> <span data-ttu-id="7ffb0-126">การเลือกโฟลเดอร์เป็นการรวมไฟล์ที่พบในโฟลเดอร์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="7ffb0-126">Selecting a folder combines the files found in that folder.</span></span> 

<span data-ttu-id="7ffb0-127">ด้วยการทำงานของการรวมไฟล์ คุณสามารถรวมไฟล์ทั้งหมดภายในโฟลเดอร์ที่ระบุได้อย่างง่ายดาย ตราบใดที่มีชนิดไฟล์และโครงสร้าง (เช่นมีคอลัมน์เดียวกัน) เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="7ffb0-127">With the behavior of combine files, you can easily combine all files within a given folder if they have the same file type and structure (such as the same columns).</span></span>

<span data-ttu-id="7ffb0-128">นอกจากนี้ คุณสามารถใช้ขั้นตอนการแปลงหรือดึงข้อมูลเพิ่มเติม ได้โดยปรับเปลี่ยนคิวรีต้นแบบที่สร้างขึ้นโดยอัตโนมัติ โดยไม่ต้องกังวลเกี่ยวกับขั้นตอนการแก้ไขหรือการสร้างฟังก์ชันคิวรีเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7ffb0-128">In addition, you can easily apply additional transformation or extraction steps by modifying the automatically created exemplar query, without having to worry about modifying or creating additional function query steps.</span></span> <span data-ttu-id="7ffb0-129">การเปลี่ยนแปลงใดๆ กับคิวรีต้นแบบ จะถูกสร้างขึ้นในฟังก์ชันคิวรีที่เชื่อมโยงกันโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7ffb0-129">Any changes to the exemplar query are automatically generated in the linked function query.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7ffb0-130">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="7ffb0-130">Next steps</span></span>

<span data-ttu-id="7ffb0-131">คุณสามารถเชื่อมต่อข้อมูลทุกรูปแบบได้โดยใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="7ffb0-131">You can connect to all sorts of data using Power BI Desktop.</span></span> <span data-ttu-id="7ffb0-132">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแหล่งที่มาข้อมูล โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7ffb0-132">For more information on data sources, see the following resources:</span></span>

* [<span data-ttu-id="7ffb0-133">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="7ffb0-133">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="7ffb0-134">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="7ffb0-134">Data sources in Power BI Desktop</span></span>](../connect-data/desktop-data-sources.md)
* [<span data-ttu-id="7ffb0-135">จัดรูปร่างและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="7ffb0-135">Shape and combine data with Power BI Desktop</span></span>](../connect-data/desktop-shape-and-combine-data.md)
* [<span data-ttu-id="7ffb0-136">เชื่อมต่อกับไฟล์ CSV ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="7ffb0-136">Connect to CSV files in Power BI Desktop</span></span>](../connect-data/desktop-connect-csv.md)
* [<span data-ttu-id="7ffb0-137">ใส่ข้อมูลลงใน Power BI Desktop โดยตรง</span><span class="sxs-lookup"><span data-stu-id="7ffb0-137">Enter data directly into Power BI Desktop</span></span>](../connect-data/desktop-enter-data-directly-into-desktop.md)
