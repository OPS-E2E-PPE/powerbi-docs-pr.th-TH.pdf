---
title: การจัดประเภทข้อมูลใน Power BI Desktop
description: การจัดประเภทข้อมูลใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: how-to
ms.date: 01/15/2020
LocalizationGroup: Model your data
ms.openlocfilehash: d99eb0355d414a9e1627da0b5629eaf45cbaf18d
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415806"
---
# <a name="specify-data-categories-in-power-bi-desktop"></a><span data-ttu-id="ad363-103">ระบุหมวดหมู่ข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ad363-103">Specify data categories in Power BI Desktop</span></span>
<span data-ttu-id="ad363-104">ใน Power BI Desktop คุณสามารถระบุ *ประเภทของข้อมูล* สำหรับคอลัมน์ เพื่อให้ Power BI Desktop ทราบว่าควรจัดการกับค่าเหล่านั้นอย่างไรเมื่อดำเนินการแสดงผลเป็นภาพ</span><span class="sxs-lookup"><span data-stu-id="ad363-104">In Power BI Desktop, you can specify the *data category* for a column so Power BI Desktop knows how it should treat its values when in a visualization.</span></span>

<span data-ttu-id="ad363-105">เมื่อ Power BI Desktop นำเข้าข้อมูล จะได้รับข้อมูลอื่นนอกเหนือจากข้อมูลของตัวเอง เช่น ชื่อตารางและคอลัมน์ และระบุว่าข้อมูลเป็นคีย์หลักหรือไม่</span><span class="sxs-lookup"><span data-stu-id="ad363-105">When Power BI Desktop imports data, it gets other information than the data itself, like the table and column names, and whether the data is a primary key.</span></span> <span data-ttu-id="ad363-106">ด้วยข้อมูลนั้น Power BI Desktop สร้างสมมติฐานบางประการเกี่ยวกับวิธีแสดงผลเป็นภาพ เพื่อให้ได้คุณมีประสบการณ์เริ่มต้นที่ดี</span><span class="sxs-lookup"><span data-stu-id="ad363-106">With that information, Power BI Desktop makes some assumptions about how to give you a good default experience when creating a visualization.</span></span>
<span data-ttu-id="ad363-107">ตัวอย่างเช่น เมื่อคอลัมน์มีค่าตัวเลข คุณอาจต้องการหาผลรวมในวิธีใดวิธีหนึ่ง ดังนั้น Power BI Desktop วางไว้ในพื้นที่ **ค่า** ของบานหน้าต่าง **การแสดงผลข้อมูลด้วยภาพ**</span><span class="sxs-lookup"><span data-stu-id="ad363-107">For example, when a column has numeric values, you'll probably want to aggregate it in some way, so Power BI Desktop places it in the **Values** area of the **Visualizations** pane.</span></span> <span data-ttu-id="ad363-108">หรือ สำหรับคอลัมน์ที่มีค่าเป็นวันที่และเวลาบนแผนภูมิเส้น Power BI Desktop จะสันนิษฐานว่าคุณอยากจะใช้คอลัมน์ดังกล่าว เป็นแกนลำดับชั้นเวลา</span><span class="sxs-lookup"><span data-stu-id="ad363-108">Or, for a column with date-time values on a line chart, Power BI Desktop assumes you'll probably use it as a time hierarchy axis.</span></span>

<span data-ttu-id="ad363-109">แต่มีบางกรณีที่ท้าทายขึ้น เช่นข้อมูลภูมิศาสตร์</span><span class="sxs-lookup"><span data-stu-id="ad363-109">But, there are some cases that are a bit more challenging, like geography.</span></span> <span data-ttu-id="ad363-110">ลองพิจารณาตารางต่อไปนี้จากแผ่นงาน Excel:</span><span class="sxs-lookup"><span data-stu-id="ad363-110">Consider the following table from an Excel worksheet:</span></span>

![ภาพหน้าจอของ Excel ที่แสดงข้อมูลแบบตารางที่จะนำเข้าลงใน Power BI Desktop](media/desktop-data-categorization/datacategorizationtable.png)

<span data-ttu-id="ad363-112">Power BI Desktop ควรถือว่ารหัสในคอลัมน์ **GeoCode** เป็นตัวอักษรย่อของประเทศ หรือของรัฐในสหรัฐอเมริกา?</span><span class="sxs-lookup"><span data-stu-id="ad363-112">Should Power BI Desktop treat the codes in the **GeoCode** column as an abbreviation for a Country or a US State?</span></span>  <span data-ttu-id="ad363-113">ซึ่งไม่ชัดเจนเนื่องจากรหัสแบบนี้อาจหมายถึงอย่างใดอย่างหนึ่งก็ได้</span><span class="sxs-lookup"><span data-stu-id="ad363-113">That's not clear because a code like this can mean either one.</span></span> <span data-ttu-id="ad363-114">ตัวอย่างเช่น AL อาจหมายถึง รัฐอลาบามา หรือประเทศแอลเบเนีย AR อาจหมายถึง รัฐอาคันซอ หรือประเทศอาร์เจนตินา หรือ CA อาจหมายถึง รัฐแคลิฟอร์เนีย หรือประเทศแคนาดา</span><span class="sxs-lookup"><span data-stu-id="ad363-114">For instance, AL can mean Alabama or Albania, AR can mean Arkansas or Argentina, or CA can mean California or Canada.</span></span> <span data-ttu-id="ad363-115">มันมีความแตกต่างกันเมื่อเราต้องการทำแผนภูมิที่มีเขตข้อมูล GeoCode บนแผนที่</span><span class="sxs-lookup"><span data-stu-id="ad363-115">It makes a difference when we go to chart our GeoCode field on a map.</span></span> 

<span data-ttu-id="ad363-116">Power BI Desktop จะแสดงรูปภาพของโลกที่มีการไฮไลต์ประเทศหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="ad363-116">Should Power BI Desktop show a picture of the world with countries highlighted?</span></span> <span data-ttu-id="ad363-117">หรือแสดงรูปภาพของสหรัฐอเมริกาที่มีการไฮไลต์รัฐหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="ad363-117">Or should it show a picture of the United States with states highlighted?</span></span>  <span data-ttu-id="ad363-118">คุณสามารถระบุหมวดหมู่ข้อมูลสำหรับข้อมูลเช่นนี้</span><span class="sxs-lookup"><span data-stu-id="ad363-118">You can specify a data category for data just like this.</span></span> <span data-ttu-id="ad363-119">การจัดประเภทข้อมูล ช่วยปรับแต่งข้อมูลที่ Power BI Desktop ใช้เพื่อให้การแสดงผลเป็นภาพ ทำได้ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="ad363-119">Data categorization further refines the information Power BI Desktop can use to provide the best visualizations.</span></span>  

<span data-ttu-id="ad363-120">**เมื่อต้องการระบุหมวดหมู่ข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="ad363-120">**To specify a data category**</span></span>

1. <span data-ttu-id="ad363-121">ในมุมมอง **รายงาน** หรือมุมมอง **ข้อมูล** ในรายการ **เขตข้อมูล** เลือกเขตข้อมูลคุณที่ต้องการจัดเรียงด้วยวิธีจัดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="ad363-121">In **Report** View or **Data** View, in the **Fields** list, select the field you want to be sorted by a different categorization.</span></span>
2. <span data-ttu-id="ad363-122">บนริบบอน ในพื้นที่ **คุณสมบัติ** ของแท็บ **การสร้างแบบจำลอง** ให้เลือกลูกศรดรอปดาวน์ที่อยู่ถัดจาก **หมวดหมู่ข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="ad363-122">On the ribbon, in the **Properties** area of the **Modeling** tab, select the drop-down arrow next to **Data Category**.</span></span>  <span data-ttu-id="ad363-123">รายการนี้จะแสดงหมวดหมู่ข้อมูลที่เป็นไปได้ทั้งหมด ที่คุณสามารถเลือกสำหรับคอลัมน์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ad363-123">This list shows the data categories you can choose for your column.</span></span> <span data-ttu-id="ad363-124">ตัวเลือกบางรายการอาจถูกปิดใช้งาน ถ้าตัวเลือกเหล่านั้นใช้ไม่ได้กับชนิดข้อมูลปัจจุบันของคอลัมน์คุณ</span><span class="sxs-lookup"><span data-stu-id="ad363-124">Some selections might be disabled if they won't work with the current data type of your column.</span></span>  <span data-ttu-id="ad363-125">ตัวอย่างเช่น ถ้าคอลัมน์เป็นข้อมูลประเภทวันที่หรือเวลา Power BI Desktop จะไม่อนุญาตให้คุณเลือกประเภทข้อมูลทางภูมิศาสตร์</span><span class="sxs-lookup"><span data-stu-id="ad363-125">For example, if a column is a date or time data type, Power BI Desktop won't let you choose geographic data categories.</span></span> 
3. <span data-ttu-id="ad363-126">เลือกหมวดหมู่ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="ad363-126">Select the category you want.</span></span>

   ![ภาพหน้าจอของ Power BI Desktop ที่แสดงตัวกรองหมวดหมู่ข้อมูล](media/desktop-data-categorization/desktop-data-categorization.png)

<span data-ttu-id="ad363-128">นอกจากนี้คุณอาจจะสนใจที่เรียนรู้เกี่ยวกับ[การกรองทางภูมิศาสตร์สำหรับแอปสำหรับอุปกรณ์เคลื่อนของ Power BI](desktop-mobile-geofiltering.md)ได้</span><span class="sxs-lookup"><span data-stu-id="ad363-128">You might also be interested in learning about [geographic filtering for Power BI mobile apps](desktop-mobile-geofiltering.md).</span></span>