---
title: ใส่ข้อมูลโดยตรงลงใน Power BI Desktop
description: เพิ่มข้อมูลลงใน Power BI Desktop โดยตรงได้อย่างง่ายดาย
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 01/15/2020
LocalizationGroup: Connect to data
ms.openlocfilehash: 292404719c476e1397930e2a9b94101ba957119f
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411160"
---
# <a name="enter-data-directly-into-power-bi-desktop"></a><span data-ttu-id="de820-103">ใส่ข้อมูลโดยตรงลงใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="de820-103">Enter data directly into Power BI Desktop</span></span>

<span data-ttu-id="de820-104">ด้วย Power BI Desktop คุณก็สามารถใส่ข้อมูลได้โดยตรง และใช้ข้อมูลนั้นในรายงานและการแสดงภาพของคุณ</span><span class="sxs-lookup"><span data-stu-id="de820-104">With Power BI Desktop, you can enter data directly and use that data in your reports and visualizations.</span></span> <span data-ttu-id="de820-105">ตัวอย่างเช่น คุณสามารถคัดลอกเวิร์กบุ๊กหรือเว็บเพจบางส่วน จากนั้นวางลงใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="de820-105">For example, you can copy portions of a workbook or web page, then paste it into Power BI Desktop.</span></span>

<span data-ttu-id="de820-106">เมื่อต้องการใส่ข้อมูลลงใน Power BI Desktop โดยตรงในรูปแบบของตารางใหม่ให้ **เลือกป้อนข้อมูล** จาก ribbon **หน้าแรก**</span><span class="sxs-lookup"><span data-stu-id="de820-106">To enter data directly into Power BI Desktop in the form of a new table, select **Enter Data** from the **Home** ribbon.</span></span>

![เลือกป้อนข้อมูลในหน้าหลัด](media/desktop-enter-data-directly-into-desktop/enter-data-directly_1.png)

<span data-ttu-id="de820-108">Power BI Desktop อาจพยายามทำการเปลี่ยนแปลงข้อมูลเพียงเล็กน้อยตามความเหมาะสม ในลักษณะเดียวกับที่ดำเนินการ เมื่อคุณโหลดข้อมูลจากแหล่งข้อมูลต่างๆ</span><span class="sxs-lookup"><span data-stu-id="de820-108">Power BI Desktop may attempt to make minor transformations on the data, if appropriate, just like it does when you load data from any source.</span></span> <span data-ttu-id="de820-109">ตัวอย่างเช่น ในกรณีต่อไปนี้ จะมีการเลื่อนระดับแถวแรกของข้อมูลในหัวกระดาษ</span><span class="sxs-lookup"><span data-stu-id="de820-109">For example, in the following case it promoted the first row of data to headers.</span></span>

![ข้อมูลกับแถวแรกเช่นเดียวกับหัวข้อแถว](media/desktop-enter-data-directly-into-desktop/enter-data-directly_2.png)

<span data-ttu-id="de820-111">หากคุณต้องการทำให้ข้อมูลเป็นรูปร่างให้คุณป้อนหรือวาง เลือก **แก้ไข** เพื่อเปิด **ตัวแก้ไขแบบสอบถาม**.</span><span class="sxs-lookup"><span data-stu-id="de820-111">If you want to shape the data you entered or pasted, select **Edit** to open **Query Editor**.</span></span> <span data-ttu-id="de820-112">คุณสามารถทำให้เป็นรูปร่างและเปลี่ยนรูปข้อมูลก่อนนำเข้าไปสู่ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="de820-112">You can shape and transform the data before bringing it into Power BI Desktop.</span></span> <span data-ttu-id="de820-113">เลือก **โหลด** เพื่อนำเข้าข้อมูลที่ปรากฏ</span><span class="sxs-lookup"><span data-stu-id="de820-113">Select **Load** to import the data as it appears.</span></span>

<span data-ttu-id="de820-114">เมื่อคุณเลือก **โหลด** Power BI Desktop จะสร้างตารางใหม่จากข้อมูลของคุณ และทำให้ตาารางพร้อมใช้งานในบานหน้าต่าง **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="de820-114">When you select **Load**, Power BI Desktop creates a new table from your data, and makes it available in the **Fields** pane.</span></span> <span data-ttu-id="de820-115">ในรูปต่อไปนี้ Power BI Desktop จะแสดงตารางใหม่ของฉัน ซึ่งเรียกว่า *ตารางที่ 1* และเขตข้อมูลสองรายการภายในตารางดังกล่าวที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="de820-115">In the following image, Power BI Desktop shows my new table, called *Table1*, and the two fields within that table that were created.</span></span>

![เขตข้อมูลโหลดแล้วไปใน Power BI Desktop](media/desktop-enter-data-directly-into-desktop/enter-data-directly_3.png)

<span data-ttu-id="de820-117">เท่านี้ก็เรียบร้อย!</span><span class="sxs-lookup"><span data-stu-id="de820-117">And that’s it.</span></span> <span data-ttu-id="de820-118">เพียงเท่านี้เองในการป้อนข้อมูลเข้าไปใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="de820-118">It's that easy to enter data into Power BI Desktop.</span></span>

<span data-ttu-id="de820-119">ตอนนี้คุณพร้อมใช้ข้อมูลใน Power BI Desktop แล้ว</span><span class="sxs-lookup"><span data-stu-id="de820-119">You're now ready to use the data in Power BI Desktop.</span></span> <span data-ttu-id="de820-120">คุณสามารถสร้างวิชวล รายงาน หรือโต้ตอบกับข้อมูลอื่น ๆ ที่คุณอาจต้องการเชื่อมต่อและนำเข้า เช่น เวิร์กบุ๊ก Excel, ฐานข้อมูล หรือแหล่งข้อมูลอื่น</span><span class="sxs-lookup"><span data-stu-id="de820-120">You can create visuals, reports, or interact with any other data you might want to connect with and import, such as Excel workbooks, databases, or any other data source.</span></span>

## <a name="next-steps"></a><span data-ttu-id="de820-121">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="de820-121">Next steps</span></span>

<span data-ttu-id="de820-122">มีข้อมูลหลากหลายประเภทที่คุณสามารถเชื่อมต่อโดยใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="de820-122">There are all sorts of data you can connect to using Power BI Desktop.</span></span> <span data-ttu-id="de820-123">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแหล่งข้อมูล โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="de820-123">For more information on data sources, check out the following resources:</span></span>

* [<span data-ttu-id="de820-124">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="de820-124">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="de820-125">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="de820-125">Data sources in Power BI Desktop</span></span>](desktop-data-sources.md)
* [<span data-ttu-id="de820-126">จัดรูปร่างและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="de820-126">Shape and combine data with Power BI Desktop</span></span>](desktop-shape-and-combine-data.md)
* [<span data-ttu-id="de820-127">เชื่อมต่อกับเวิร์กบุ๊ก Excel ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="de820-127">Connect to Excel workbooks in Power BI Desktop</span></span>](desktop-connect-excel.md)
* [<span data-ttu-id="de820-128">เชื่อมต่อกับไฟล์ CSV ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="de820-128">Connect to CSV files in Power BI Desktop</span></span>](desktop-connect-csv.md)
