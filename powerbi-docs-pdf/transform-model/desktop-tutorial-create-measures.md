---
title: 'บทช่วยสอน: สร้างหน่วยวัดของคุณเองใน Power BI Desktop'
description: หน่วยวัดใน Power BI Desktop ช่วยคุณโดยการคำนวณบนข้อมูลของคุณ ตามที่คุณโต้ตอบกับรายงานของคุณ
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: tutorial
ms.date: 11/08/2019
LocalizationGroup: Learn more
ms.openlocfilehash: 16ce255f22d6242a1b8e78d34b27519d22fb5489
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413920"
---
# <a name="tutorial-create-your-own-measures-in-power-bi-desktop"></a><span data-ttu-id="2984f-103">บทช่วยสอน: สร้างหน่วยวัดของคุณเองใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2984f-103">Tutorial: Create your own measures in Power BI Desktop</span></span>
<span data-ttu-id="2984f-104">คุณสามารถสร้างโซลูชันของการวิเคราะห์ข้อมูลมีประสิทธิภาพที่สุดบางอย่างใน Power BI Desktop โดยใช้หน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="2984f-104">By using measures, you can create some of the most powerful data analysis solutions in Power BI Desktop.</span></span> <span data-ttu-id="2984f-105">หน่วยวัดที่ช่วยคุณด้วยการคำนวนบนข้อมูลของคุณ ตามที่คุณโต้ตอบกับรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="2984f-105">Measures help you by performing calculations on your data as you interact with your reports.</span></span> <span data-ttu-id="2984f-106">บทเรียนนี้จะแนะนำคุณโดยผ่านการทำความเข้าใจเกี่ยวกับหน่วยวัด และสร้างหน่วยวัดพื้นฐานของคุณเองใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2984f-106">This tutorial will guide you through understanding measures and creating your own basic measures in Power BI Desktop.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2984f-107">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="2984f-107">Prerequisites</span></span>

- <span data-ttu-id="2984f-108">บทเรียนนี้มีไว้สำหรับผู้ใช้ Power BI ที่คุณคุ้นเคยกับการใช้ Power BI Desktop เพื่อสร้างแบบจำลองที่ขั้นสูงขึ้น</span><span class="sxs-lookup"><span data-stu-id="2984f-108">This tutorial is intended for Power BI users already familiar with using Power BI Desktop to create more advanced models.</span></span> <span data-ttu-id="2984f-109">คุณควรจะคุ้นเคยกับการใช้ Get Data และตัวแก้ไขคิวรีเพื่อนำเข้าข้อมูล ทำงานกับหลายตารางที่เกี่ยวข้อง และเพิ่มเขตข้อมูลไปยังพื้นที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="2984f-109">You should already be familiar with using Get Data and Query Editor to import data, work with multiple related tables, and add fields to the report canvas.</span></span> <span data-ttu-id="2984f-110">ถ้าคุณยังไม่คุ้นเคยกับ Power BI Desktop ให้ตรวจดู[เริ่มต้นใช้งาน Power BI Desktop](../fundamentals/desktop-getting-started.md)</span><span class="sxs-lookup"><span data-stu-id="2984f-110">If you’re new to Power BI Desktop, be sure to check out [Getting Started with Power BI Desktop](../fundamentals/desktop-getting-started.md).</span></span>
  
- <span data-ttu-id="2984f-111">บทช่วยสอนนี้ใช้ไฟล์[ตัวอย่างยอดขายของ Contoso สำหรับ Power BI Desktop](https://download.microsoft.com/download/4/6/A/46AB5E74-50F6-4761-8EDB-5AE077FD603C/Contoso%20Sales%20Sample%20for%20Power%20BI%20Desktop.zip) ซึ่งรวมถึงข้อมูลยอดขายออนไลน์จากบริษัทจำลอง Contoso</span><span class="sxs-lookup"><span data-stu-id="2984f-111">This tutorial uses the [Contoso Sales Sample for Power BI Desktop](https://download.microsoft.com/download/4/6/A/46AB5E74-50F6-4761-8EDB-5AE077FD603C/Contoso%20Sales%20Sample%20for%20Power%20BI%20Desktop.zip) file, which includes online sales data from the fictitious company, Contoso.</span></span> <span data-ttu-id="2984f-112">เนื่องจากข้อมูลนี้นำเข้ามาจากฐานข้อมูล ดังนั้นคุณจึงไม่สามารถเชื่อมต่อกับแหล่งข้อมูลหรือดูในตัวแก้ไขคิวรีได้</span><span class="sxs-lookup"><span data-stu-id="2984f-112">Because this data is imported from a database, you can't connect to the datasource or view it in Query Editor.</span></span> <span data-ttu-id="2984f-113">ดาวน์โหลดและแยกไฟล์บนคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2984f-113">Download and extract the file on your computer.</span></span>

## <a name="automatic-measures"></a><span data-ttu-id="2984f-114">หน่วยวัดอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2984f-114">Automatic measures</span></span>

<span data-ttu-id="2984f-115">เมื่อ Power BI Desktop สร้างหน่วยวัด หน่วยวัดมักจะถูกสร้างขึ้นสำหรับคุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="2984f-115">When Power BI Desktop creates a measure, it's most often created for you automatically.</span></span> <span data-ttu-id="2984f-116">เมื่อต้องการดูวิธีการที่ Power BI Desktop สร้างหน่วยวัด ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="2984f-116">To see how Power BI Desktop creates a measure, follow these steps:</span></span>

1. <span data-ttu-id="2984f-117">ในPower BI Desktop ให้เลือก **ไฟล์** > **เปิด**, เรียกดูไฟล์ *ตัวอย่างยอดขายของ Contoso สำหรับ Power BI Desktop.pbix* จากนั้นเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="2984f-117">In Power BI Desktop, select **File** > **Open**, browse to the *Contoso Sales Sample for Power BI Desktop.pbix* file, and then select **Open**.</span></span>

2. <span data-ttu-id="2984f-118">ในบานหน้าต่าง **เขตข้อมูล** ขยายตาราง **ยอดขาย**</span><span class="sxs-lookup"><span data-stu-id="2984f-118">In the **Fields** pane, expand the **Sales** table.</span></span> <span data-ttu-id="2984f-119">จากนั้นเลือกกล่องกาเครื่องหมายที่อยู่ถัดจากเขตข้อมูล **SalesAmount** หรือลาก **SalesAmount** ลงบนพื้นที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="2984f-119">Then, either select the check box next to the **SalesAmount** field or drag **SalesAmount** onto the report canvas.</span></span>

    <span data-ttu-id="2984f-120">การสร้างภาพแผนภูมิคอลัมน์ใหม่จะปรากฏขึ้นโดยแสดงผลรวมของค่าทั้งหมดในคอลัมน์ **SalesAmount** ของตาราง **ยอดขาย**</span><span class="sxs-lookup"><span data-stu-id="2984f-120">A new column chart visualization appears, showing the sum total of all values in the **SalesAmount** column of the **Sales** table.</span></span>

    ![แผนภูมิคอลัมน์ SalesAmount](media/desktop-tutorial-create-measures/meastut_salesamountchart.png)

<span data-ttu-id="2984f-122">เขตข้อมูล (คอลัมน์) ใน **เขตข้อมูล** บานหน้าต่างที่มีไอคอน sigma ![ไอคอน Sigma](media/desktop-tutorial-create-measures/meastut_sigma.png) และสามารถรวมค่าได้</span><span class="sxs-lookup"><span data-stu-id="2984f-122">Any field (column) in the **Fields** pane with a sigma icon ![Sigma icon](media/desktop-tutorial-create-measures/meastut_sigma.png) is numeric, and its values can be aggregated.</span></span> <span data-ttu-id="2984f-123">Power BI Desktop จะสร้างและคำนวณหน่วยวัดเพื่อรวมข้อมูลโดยอัตโนมัติหากตรวจพบชนิดข้อมูลที่เป็นตัวเลข แทนการแสดงตารางที่มีค่าจำนวนมาก (สองล้านแถวสำหรับ **SalesAmount**)</span><span class="sxs-lookup"><span data-stu-id="2984f-123">Rather than display a table with many values (two million rows for **SalesAmount**), Power BI Desktop automatically creates and calculates a measure to aggregate the data if it detects a numeric datatype.</span></span> <span data-ttu-id="2984f-124">ผลรวมคือ การรวมค่าแบบเริ่มต้นสำหรับชนิดข้อมูลที่เป็นตัวเลข แต่คุณสามารถใช้การรวมข้อมูลอื่นๆเช่นหาค่าเฉลี่ยหรือการนับค่าได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="2984f-124">Sum is the default aggregation for a numeric datatype, but you can easily apply different aggregations like average or count.</span></span> <span data-ttu-id="2984f-125">การทำความเข้าใจเกี่ยวกับรวมข้อมูลเป็นพื้นฐานเพื่อทำความเข้าใจเกี่ยวกับมาตรการวัด เนื่องจากหน่วยวัดทุกตัวมีการทำการรวมข้อมูลชนิดใดชนิดหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2984f-125">Understanding aggregations is fundamental to understanding measures, because every measure performs some type of aggregation.</span></span> 

<span data-ttu-id="2984f-126">เมื่อต้องการเปลี่ยนการรวมแผนภูมิ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="2984f-126">To change the chart aggregation, follow these steps:</span></span>

1. <span data-ttu-id="2984f-127">เลือกการแสดงภาพ **SalesAmount** ในพื้นที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="2984f-127">Select the **SalesAmount** visualization in the report canvas.</span></span>  

1. <span data-ttu-id="2984f-128">ในพื้นที่ **ค่า** ของบานหน้าต่าง **การสร้างภาพ** เลือกลูกศรลงทางด้านขวาของ **SalesAmount**</span><span class="sxs-lookup"><span data-stu-id="2984f-128">In the **Value** area of the **Visualizations** pane, select the down arrow to the right of **SalesAmount**.</span></span> 

1. <span data-ttu-id="2984f-129">จากเมนูที่ปรากฏขึ้น เลือก **ค่าเฉลี่ย**</span><span class="sxs-lookup"><span data-stu-id="2984f-129">From the menu that appears, select **Average**.</span></span> 

    <span data-ttu-id="2984f-130">การแสดงภาพจะเปลี่ยนเป็นค่าเฉลี่ยของยอดขายทั้งหมดในเขตข้อมูล **SalesAmount**</span><span class="sxs-lookup"><span data-stu-id="2984f-130">The visualization changes to an average of all sales values in the **SalesAmount** field.</span></span>

    ![แผนภูมิโดยเฉลี่ย SalesAmount](media/desktop-tutorial-create-measures/meastut_salesamountaveragechart.png)

<span data-ttu-id="2984f-132">คุณสามารถเปลี่ยนชนิดของการรวมได้โดยขึ้นอยู่กับผลลัพธ์ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="2984f-132">Depending on the result you want, you can change the type of aggregation.</span></span> <span data-ttu-id="2984f-133">อย่างไรก็ตาม การรวมไม่ได้มีผลกับประเภทข้อมูลที่เป็นตัวเลขทุกประเภท</span><span class="sxs-lookup"><span data-stu-id="2984f-133">However, not all types of aggregation apply to every numeric datatype.</span></span> <span data-ttu-id="2984f-134">ตัวอย่างเช่น สำหรับเขตข้อมูล **SalesAmount** ผลรวม และค่าเฉลี่ยจะมีประโยชน์ รวมถึงค่าต่ำสุดและสูงสุดจะมีตำแหน่งของตนเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="2984f-134">For example, for the **SalesAmount** field, Sum and Average are useful, and Minimum and Maximum have their place as well.</span></span> <span data-ttu-id="2984f-135">อย่างไรก็ตาม การนับไม่เหมาะสมกับเขตข้อมูล **SalesAmount** เนื่องจากในขณะที่ค่าเป็นตัวเลข แต่ที่จริงมันเป็นสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="2984f-135">However, Count doesn't make sense for the **SalesAmount** field, because while its values are numeric, they’re really currency.</span></span>

<span data-ttu-id="2984f-136">ค่าที่คำนวณจากการเปลี่ยนแปลงตัววัดได้ตอบสนองต่อการโต้ตอบกับรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="2984f-136">Values calculated from measures change in response to your interactions with your report.</span></span> <span data-ttu-id="2984f-137">ตัวอย่างเช่น ถ้าคุณลากเขตข้อมูล **RegionCountryName** จากตาราง **ภูมิศาสตร์** ไปยังแผนภูมิ **SalesAmount** ของคุณที่มีอยู่ การดำเนินการนี้จะมีการเปลี่ยนแปลงเพื่อแสดงยอดขายเฉลี่ยสำหรับแต่ละประเทศ</span><span class="sxs-lookup"><span data-stu-id="2984f-137">For example, if you drag the **RegionCountryName** field from the **Geography** table onto your existing **SalesAmount** chart, it changes to show the average sales amounts for each country.</span></span>

![SaleAmount ตามประเทศ](media/desktop-tutorial-create-measures/meastut_salesamountavchartbyrcn.png)

<span data-ttu-id="2984f-139">เมื่อผลลัพธ์ของหน่วยวัดมีการเปลี่ยนแปลงเนื่องจากการโต้ตอบกับรายงานของคุณ *บริบท* ของหน่วยวัดจะได้รับผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="2984f-139">When the result of a measure changes because of an interaction with your report, you've affected your measure’s *context*.</span></span> <span data-ttu-id="2984f-140">ทุกครั้งที่คุณโต้ตอบกับด้วยการแสดงภาพของคุณรายงาน คุณกำลังเปลี่ยนแปลงบริบท ซึ่งหน่วยวัดถูกคำนวณและแสดงผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="2984f-140">Every time you interact with your report visualizations, you're changing the context in which a measure calculates and displays its results.</span></span>

## <a name="create-and-use-your-own-measures"></a><span data-ttu-id="2984f-141">สร้าง และใช้หน่วยวัดของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="2984f-141">Create and use your own measures</span></span>

<span data-ttu-id="2984f-142">ในกรณีส่วนใหญ่ Power BI Desktop จะคำนวณและแสดงค่าโดยอัตโนมัติตามชนิดของเขตข้อมูลและการรวมที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="2984f-142">In most cases, Power BI Desktop automatically calculates and returns values according to the types of fields and aggregations you choose.</span></span> <span data-ttu-id="2984f-143">อย่างไรก็ตาม ในบางกรณีคุณอาจต้องการสร้างหน่วยวัดของคุณเองเพื่อทำการคำนวณที่ซับซ้อนและไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="2984f-143">However, in some cases you might want to create your own measures to perform more complex, unique calculations.</span></span> <span data-ttu-id="2984f-144">กับ คุณสามารถสร้างหน่วยวัดของคุณด้วยภาษาสูตร Data Analysis Expressions (DAX) ด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2984f-144">With Power BI Desktop, you can create your own measures with the Data Analysis Expressions (DAX) formula language.</span></span> 

<span data-ttu-id="2984f-145">สูตร DAX ใช้ฟังก์ชัน ตัวดำเนินการ และไวยากรณ์เดียวกับสูตร Excel เป็นจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="2984f-145">DAX formulas use many of the same functions, operators, and syntax as Excel formulas.</span></span> <span data-ttu-id="2984f-146">อย่างไรก็ตาม ฟังก์ชัน DAX ถูกออกแบบมาให้ทำงานกับข้อมูลแบบสัมพันธ์ และทำการคำนวณแบบไดนามิกมากกว่าที่คุณโต้ตอบกับรายงาน</span><span class="sxs-lookup"><span data-stu-id="2984f-146">However, DAX functions are designed to work with relational data and perform more dynamic calculations as you interact with your reports.</span></span> <span data-ttu-id="2984f-147">มีฟังก์ชัน DAX มากกว่า 200 ตัว ที่ทำทุกอย่างตั้งแต่การรวมข้อมูลอย่างง่าย เช่น ผลรวมและค่าเฉลี่ย ไปยังฟังก์ชันทางสถิติ และการกรองที่ซับซ้อนมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="2984f-147">There are over 200 DAX functions that do everything from simple aggregations like sum and average to more complex statistical and filtering functions.</span></span> <span data-ttu-id="2984f-148">มีแหล่งข้อมูลมากมายเพื่อช่วยให้คุณเรียนรู้เพิ่มเติมเกี่ยวกับ DAX</span><span class="sxs-lookup"><span data-stu-id="2984f-148">There are many resources to help you learn more about DAX.</span></span> <span data-ttu-id="2984f-149">หลังจากที่คุณเสร็จสิ้นบทช่วยสอนนี้ ดู[พื้นฐาน DAX ใน Power BI Desktop](desktop-quickstart-learn-dax-basics.md)</span><span class="sxs-lookup"><span data-stu-id="2984f-149">After you've finished this tutorial, see [DAX basics in Power BI Desktop](desktop-quickstart-learn-dax-basics.md).</span></span>

<span data-ttu-id="2984f-150">เมื่อคุณสร้างหน่วยวัดของคุณเอง การดำเนินการนี้จะเรียกว่าหน่วยวัดของ *แบบจำลอง* และจะถูกเพิ่มลงในรายการ **เขตข้อมูล** สำหรับตารางที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="2984f-150">When you create your own measure, it's called a *model* measure, and it's added to the **Fields** list for the table you select.</span></span> <span data-ttu-id="2984f-151">ข้อดีบางประการของหน่วยวัดแบบจำลอง ซึ่งจะให้คุณสามารถตั้งชื่อตามที่คุณต้องการได้ ทำให้สามารถระบุตัวได้ง่ายขึ้น คุณสามารถใช้เป็นอาร์กิวเมนต์ในนิพจน์ DAX อื่น ๆ และคุณสามารถดำเนินการคำนวณที่ซับซ้อนได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="2984f-151">Some advantages of model measures are that you can name them whatever you want, making them more identifiable; you can use them as arguments in other DAX expressions; and you can make them perform complex calculations quickly.</span></span>

### <a name="quick-measures"></a><span data-ttu-id="2984f-152">การวัดผลด่วน</span><span class="sxs-lookup"><span data-stu-id="2984f-152">Quick measures</span></span>

<span data-ttu-id="2984f-153">นับตั้งแต่ Power BI Desktop รุ่นเดือนกุมภาพันธ์ 2018 คุณสามารถใช้การคำนวณทั่วไปหลายแบบเช่น *ตัววัดแบบด่วน* ซึ่งเขียนสูตร DAX ให้คุณ โดยยึดตามข้อมูลที่คุณป้อนเข้าในหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="2984f-153">Starting with the February 2018 release of Power BI Desktop, many common calculations are available as *quick measures*, which write the DAX formulas for you based on your inputs in a window.</span></span> <span data-ttu-id="2984f-154">คำนวณที่รวดเร็วและมีประสิทธิภาพเหล่านี้เหมาะสำหรับการเรียนรู้ DAX หรือเริ่มหน่วยวัดแบบกำหนดเองของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="2984f-154">These quick, powerful calculations are also great for learning DAX or seeding your own customized measures.</span></span> 

<span data-ttu-id="2984f-155">สร้างการวัดผลด่วนโดยใช้วิธีใดวิธีหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2984f-155">Create a quick measure using one of these methods:</span></span> 
 - <span data-ttu-id="2984f-156">จากตารางในบานหน้าต่าง **เขตข้อมูล** ให้คลิกขวาหรือเลือกตัวเลือก **เพิ่มเติม** ( **...** ), จากนั้นเลือก **การวัดผลด่วนใหม่** จากรายการ</span><span class="sxs-lookup"><span data-stu-id="2984f-156">From a table in the **Fields** pane, right-click or select **More options** (**...**), and then select **New quick measure** from the list.</span></span>

 - <span data-ttu-id="2984f-157">ภายใต้ **การคำนวณ** ในแท็บ **Home** ของริบบอน Power BI Desktop ให้เลือก **การวัดผลด่วนใหม่**</span><span class="sxs-lookup"><span data-stu-id="2984f-157">Under **Calculations** in the **Home** tab of the Power BI Desktop ribbon, select **New Quick Measure**.</span></span>

<span data-ttu-id="2984f-158">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสร้างและการใช้การวัดผลด่วน ให้ดู [ใช้การวัดผลด่วน](desktop-quick-measures.md)</span><span class="sxs-lookup"><span data-stu-id="2984f-158">For more information about creating and using quick measures, see [Use quick measures](desktop-quick-measures.md).</span></span>

### <a name="create-a-measure"></a><span data-ttu-id="2984f-159">สร้างการวัด</span><span class="sxs-lookup"><span data-stu-id="2984f-159">Create a measure</span></span>

<span data-ttu-id="2984f-160">สมมติว่าคุณต้องการวิเคราะห์ยอดขายสุทธิของคุณโดยลบส่วนลดและผลลัพธ์จากยอดขายรวม</span><span class="sxs-lookup"><span data-stu-id="2984f-160">Suppose you want to analyze your net sales by subtracting discounts and returns from total sales amounts.</span></span> <span data-ttu-id="2984f-161">สำหรับบริบทที่มีอยู่ในการแสดงภาพของคุณ คุณจำเป็นต้องมีหน่วยวัดที่ลบผลรวมของ DiscountAmount และ ReturnAmount จากผลรวมของ SalesAmount</span><span class="sxs-lookup"><span data-stu-id="2984f-161">For the context that exists in your visualization, you need a measure that subtracts the sum of DiscountAmount and ReturnAmount from the sum of SalesAmount.</span></span> <span data-ttu-id="2984f-162">ไม่มีเขตข้อมูลสำหรับยอดขายสุทธิในรายการ **เขตข้อมูล** แต่คุณต้องมีบล็อกการสร้างเพื่อสร้างหน่วยวัดของคุณเองในการคำนวณยอดขายสุทธิ</span><span class="sxs-lookup"><span data-stu-id="2984f-162">There's no field for Net Sales in the **Fields** list, but you have the building blocks to create your own measure to calculate net sales.</span></span> 

<span data-ttu-id="2984f-163">แล้วทำตามขั้นตอนเหล่านี้เพื่อสร้างหน่วยวัด:</span><span class="sxs-lookup"><span data-stu-id="2984f-163">To create a measure, follow these steps:</span></span>

1. <span data-ttu-id="2984f-164">ในบานหน้าต่าง **เขตข้อมูล** ให้คลิกขวาที่ตาราง **ยอดขาย** หรือวางเมาส์เหนือตารางและเลือก **ตัวเลือกเพิ่มเติม** ( **...** )</span><span class="sxs-lookup"><span data-stu-id="2984f-164">In the **Fields** pane, right-click the **Sales** table, or hover over the table and select **More options** (**...**).</span></span> 

1. <span data-ttu-id="2984f-165">จากเมนูที่ปรากฏขึ้น เลือก **หน่วยวัดใหม่**</span><span class="sxs-lookup"><span data-stu-id="2984f-165">From the menu that appears, select **New measure**.</span></span> 

    <span data-ttu-id="2984f-166">การดำเนินการนี้จะเป็นการบันทึกหน่วยวัดใหม่ของคุณในตาราง **ยอดขาย** ซึ่งเป็นเรื่องง่ายที่จะค้นหา</span><span class="sxs-lookup"><span data-stu-id="2984f-166">This action saves your new measure in the **Sales** table, where it's easy to find.</span></span>
    
    ![หน่วยวัดใหม่จากรายการ](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure.png)
    
    <span data-ttu-id="2984f-168">คุณยังสามารถสร้างหน่วยวัดใหม่ได้โดยการเลือก **หน่วยวัดใหม่** ในกลุ่ม **การคำนวณ** บนแท็บ **Home** ของริบบอน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2984f-168">You can also create a new measure by selecting **New Measure** in the **Calculations** group on the **Home** tab of the Power BI Desktop ribbon.</span></span>
    
    ![หน่วยวัดใหม่จากริบบอน](media/desktop-tutorial-create-measures/meastut_netsales_newmeasureribbon.png)
    
    >[!TIP]
    ><span data-ttu-id="2984f-170">เมื่อคุณสร้างหน่วยวัดจากริบบอน คุณสามารถสร้างขึ้นในตารางใดก็ได้ แต่จะง่ายต่อการค้นหาถ้าคุณสร้างในที่ที่คุณวางแผนจะใช้</span><span class="sxs-lookup"><span data-stu-id="2984f-170">When you create a measure from the ribbon, you can create it in any of your tables, but it's easier to find if you create it where you plan to use it.</span></span> <span data-ttu-id="2984f-171">ในกรณีนี้ เลือกตาราง **ยอดขาย** ก่อนเพื่อเปิดใช้งาน จากนั้นเลือก **หน่วยวัดใหม่**</span><span class="sxs-lookup"><span data-stu-id="2984f-171">In this case, select the **Sales** table first to make it active, and then select **New measure**.</span></span> 
    
    <span data-ttu-id="2984f-172">แถบสูตรจะปรากฏขึ้นตามแนวด้านบนของพื้นที่รายงาน ตำแหน่งที่คุณสามารถเปลี่ยนชื่อหน่วยวัดของคุณ และใส่สูตร DAX</span><span class="sxs-lookup"><span data-stu-id="2984f-172">The formula bar appears along the top of the report canvas, where you can rename your measure and enter a DAX formula.</span></span>
    
    ![แถบสูตร](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure_formulabar.png)
    
1. <span data-ttu-id="2984f-174">ตามค่าเริ่มต้น หน่วยวัดใหม่แต่ละหน่วยจะมีชื่อว่า *Measure*</span><span class="sxs-lookup"><span data-stu-id="2984f-174">By default, each new measure is named *Measure*.</span></span> <span data-ttu-id="2984f-175">ถ้าคุณไม่ได้เปลี่ยนชื่อ หน่วยวัดใหม่เพิ่มเติมจะมีชื่อว่า *Measure 2*, *Measure 3* และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="2984f-175">If you don’t rename it, additional new measures are named *Measure 2*, *Measure 3*, and so on.</span></span> <span data-ttu-id="2984f-176">เนื่องจากเราต้องการให้หน่วยวัดนี้สามารถระบุได้มากขึ้น ให้ไฮไลท์ *Measure* ในแถบสูตรแล้วเปลี่ยนเป็น *ยอดขายสุทธิ*</span><span class="sxs-lookup"><span data-stu-id="2984f-176">Because we want this measure to be more identifiable, highlight *Measure* in the formula bar, and then change it to *Net Sales*.</span></span>
    
1. <span data-ttu-id="2984f-177">เริ่มต้นการใส่สูตรของคุณ</span><span class="sxs-lookup"><span data-stu-id="2984f-177">Begin entering your formula.</span></span> <span data-ttu-id="2984f-178">หลังจากเครื่องหมายเท่ากัน เริ่มพิมพ์ *Sum*</span><span class="sxs-lookup"><span data-stu-id="2984f-178">After the equals sign, start to type *Sum*.</span></span> <span data-ttu-id="2984f-179">ขณะที่คุณพิมพ์ รายการคำแนะนำแบบดรอปดาวน์จะปรากฏขึ้น ซึ่งแสดงฟังก์ชัน DAX ทั้งหมดที่ขึ้นต้นด้วยตัวอักษรที่คุณพิมพ์</span><span class="sxs-lookup"><span data-stu-id="2984f-179">As you type, a drop-down suggestion list appears, showing all the DAX functions, beginning with the letters you type.</span></span> <span data-ttu-id="2984f-180">เลื่อนลง ถ้าจำเป็น หากต้องการเลือก **SUM** จากรายการ จากนั้นกด **Enter**</span><span class="sxs-lookup"><span data-stu-id="2984f-180">Scroll down, if necessary, to select **SUM** from the list, and then press **Enter**.</span></span>
    
    ![เลือก SUM จากรายการ](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure_formula_s.png)
    
    <span data-ttu-id="2984f-182">วงเล็บเปิดจะปรากฏขึ้น พร้อมกับรายการแนะนำแบบดรอปดาวน์สำหรับคอลัมน์พร้อมใช้งานที่คุณสามารถส่งไปยังฟังก์ชัน SUM</span><span class="sxs-lookup"><span data-stu-id="2984f-182">An opening parenthesis appears, along with a drop-down suggestion list of the available columns you can pass to the SUM function.</span></span>
    
    ![เลือกคอลัมน์](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure_formula_sum.png)
    
1. <span data-ttu-id="2984f-184">นิพจน์ปรากฏตลอดเวลาระหว่างวงเล็บปิดและวงเล็บปิด</span><span class="sxs-lookup"><span data-stu-id="2984f-184">Expressions always appear between opening and closing parentheses.</span></span> <span data-ttu-id="2984f-185">ตัวอย่างเช่น นิพจน์ของคุณจะประกอบด้วยอาร์กิวเมนต์เดียว เพื่อส่งผ่านไปยังฟังก์ชัน SUM ของคอลัมน์ **SalesAmount**</span><span class="sxs-lookup"><span data-stu-id="2984f-185">For this example, your expression contains a single argument to pass to the SUM function: the **SalesAmount** column.</span></span> <span data-ttu-id="2984f-186">เริ่มพิมพ์ *SalesAmount* จนกว่า **Sales(SalesAmount)** จะเป็นค่าเดียวที่เหลืออยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="2984f-186">Begin typing *SalesAmount* until **Sales(SalesAmount)** is the only value left in the list.</span></span> 

    <span data-ttu-id="2984f-187">ชื่อคอลัมน์ที่นำหน้าด้วยชื่อตารางจะถือว่าเป็นชื่อที่ตรงตามหลักเกณฑ์ของคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="2984f-187">The column name preceded by the table name is called the fully qualified name of the column.</span></span> <span data-ttu-id="2984f-188">ชื่อคอลัมน์ที่ตรงตามหลักเกณฑ์ทำให้สูตรของคุณอ่านง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="2984f-188">Fully qualified column names make your formulas easier to read.</span></span>
    
    ![เลือก SalesAmount](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure_formula_salesam.png)
    
1. <span data-ttu-id="2984f-190">เลือก **Sales[SalesAmount]** จากรายการ จากนั้นใส่วงเล็บปิด</span><span class="sxs-lookup"><span data-stu-id="2984f-190">Select **Sales[SalesAmount]** from the list, and then enter a closing parenthesis.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="2984f-191">ข้อผิดพลาดทางไวยากรณ์มักเกิดขึ้นจากวงเล็บปิดที่วางผิดตำแหน่ง หรือขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="2984f-191">Syntax errors are most often caused by a missing or misplaced closing parenthesis.</span></span>
    
    
    
1. <span data-ttu-id="2984f-192">ลบสองคอลัมน์อื่นภายในสูตร:</span><span class="sxs-lookup"><span data-stu-id="2984f-192">Subtract the other two columns inside the formula:</span></span>

    <span data-ttu-id="2984f-193">a.</span><span class="sxs-lookup"><span data-stu-id="2984f-193">a.</span></span> <span data-ttu-id="2984f-194">หลังจากวงเล็บปิดในนิพจน์แรก พิมพ์ช่องว่าง ตัวดำเนินการลบ (-) และช่องว่างอีกช่อง</span><span class="sxs-lookup"><span data-stu-id="2984f-194">After the closing parenthesis for the first expression, type a space, a minus operator (-), and then another space.</span></span> 

    <span data-ttu-id="2984f-195">b.</span><span class="sxs-lookup"><span data-stu-id="2984f-195">b.</span></span> <span data-ttu-id="2984f-196">ใส่ฟังก์ชัน SUM อีกอัน และเริ่มพิมพ์ *DiscountAmount* จนกว่าคุณสามารถเลือกคอลัมน์ **Sales[DiscountAmount]** เป็นอาร์กิวเมนต์</span><span class="sxs-lookup"><span data-stu-id="2984f-196">Enter another SUM function, and start typing *DiscountAmount* until you can choose the **Sales[DiscountAmount]** column as the argument.</span></span> <span data-ttu-id="2984f-197">เพิ่มวงเล็บปิด</span><span class="sxs-lookup"><span data-stu-id="2984f-197">Add a closing parenthesis.</span></span> 

    <span data-ttu-id="2984f-198">c.</span><span class="sxs-lookup"><span data-stu-id="2984f-198">c.</span></span> <span data-ttu-id="2984f-199">พิมพ์ช่องว่าง ตัวดำเนินการลบ ช่องว่าง ฟังก์ชัน SUM อีกฟังก์ชัน พร้อมกับ **Sales[ReturnAmount]** เป็นอาร์กิวเมนต์ และวงเล็บปิด</span><span class="sxs-lookup"><span data-stu-id="2984f-199">Type a space, a minus operator, a space, another SUM function with **Sales[ReturnAmount]** as the argument, and then a closing parenthesis.</span></span>
    
    ![เติมสูตร](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure_formula_discamount.png)
    
1. <span data-ttu-id="2984f-201">กด **Enter** หรือเลือก **ยืนยัน** (ไอคอนเครื่องหมายถูก) ในแถบสูตรเพื่อทำให้เสร็จสมบูรณ์และตรวจสอบความถูกต้องสูตร</span><span class="sxs-lookup"><span data-stu-id="2984f-201">Press **Enter** or select **Commit** (checkmark icon) in the formula bar to complete and validate the formula.</span></span> 

    <span data-ttu-id="2984f-202">ขณะนี้หน่วยวัด **ยอดขายสุทธิ** ที่ตรวจสอบความถูกต้องแล้วพร้อมใช้งานในตาราง **ยอดขาย** ในบานหน้าต่าง **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="2984f-202">The validated **Net Sales** measure is now ready to use in the **Sales** table in the **Fields** pane.</span></span>
    
    ![หน่วยวัดยอดขายสุทธิในรายการเขตข้อมูลของตารางยอดขาย](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure_complete.png)
    
1. <span data-ttu-id="2984f-204">ถ้าคุณมีพื้นที่ไม่พอสำหรับการใส่สูตรหรือต้องการในบรรทัดที่แยกต่างหาก ให้เลือกลูกศรลงทางด้านขวาของแถบสูตรเพื่อให้มีช่องว่างมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="2984f-204">If you run out of room for entering a formula or want it on separate lines, select the down arrow on the right side of the formula bar to provide more space.</span></span> 

    <span data-ttu-id="2984f-205">ลูกศรลงจะเปลี่ยนเป็นลูกศรขึ้นและกล่องขนาดใหญ่จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="2984f-205">The down arrow turns into an up arrow and a large box appears.</span></span>

    ![ลูกศรขึ้นของสูตร](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure_formula_chevron.png)

1. <span data-ttu-id="2984f-207">แยกส่วนต่าง ๆ ของสูตรของคุณโดยการกด **Alt** + **Enter** สำหรับบรรทัดที่แยกต่างหาก หรือกด **Tab** เพื่อเพิ่มระยะห่างของแท็บ</span><span class="sxs-lookup"><span data-stu-id="2984f-207">Separate parts of your formula by pressing **Alt** + **Enter** for separate lines, or pressing **Tab** to add tab spacing.</span></span>

   ![สูตรที่ขยาย](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure_formula_expanded.png)

### <a name="use-your-measure-in-the-report"></a><span data-ttu-id="2984f-209">ใช้หน่วยวัดของคุณในรายงาน</span><span class="sxs-lookup"><span data-stu-id="2984f-209">Use your measure in the report</span></span>
<span data-ttu-id="2984f-210">เพิ่มหน่วยวัด **ยอดขายสุทธิ** ของคุณไปยังพื้นที่รายงาน และคำนวณยอดขายสุทธิสำหรับเขตข้อมูลอื่นใดก็ตามที่คุณเพิ่มลงในรายงาน</span><span class="sxs-lookup"><span data-stu-id="2984f-210">Add your new **Net Sales** measure to the report canvas, and calculate net sales for whatever other fields you add to the report.</span></span> 

<span data-ttu-id="2984f-211">เมื่อต้องดูยอดขายสุทธิตามประเทศ</span><span class="sxs-lookup"><span data-stu-id="2984f-211">To look at net sales by country:</span></span>

1. <span data-ttu-id="2984f-212">เลือก **ยอดขายสุทธิ** วัดจากการตาราง **Sales** หรือลากไปที่พื้นที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="2984f-212">Select the **Net Sales** measure from the **Sales** table, or drag it onto the report canvas.</span></span>
    
1. <span data-ttu-id="2984f-213">เลือกเขตข้อมูล **RegionCountryName** จากตาราง **ภูมิศาสตร์** หรือลากไปยังแผนภูมิ **ยอดขายสุทธิ**</span><span class="sxs-lookup"><span data-stu-id="2984f-213">Select the **RegionCountryName** field from the **Geography** table, or drag it onto the **Net Sales** chart.</span></span>
    
    ![ยอดขายสุทธิตามประเทศ](media/desktop-tutorial-create-measures/meastut_netsales_byrcn.png)
    
1. <span data-ttu-id="2984f-215">เมื่อต้องการดูความแตกต่างระหว่างยอดขายสุทธิและยอดขายรวมตามประเทศ เลือกเขตข้อมูล **SalesAmount** หรือลากไปยังแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="2984f-215">To see the difference between net sales and total sales by country, select the **SalesAmount** field or drag it onto the chart.</span></span> 

    ![ยอดขายและขายสุทธิตามประเทศ](media/desktop-tutorial-create-measures/meastut_netsales_byrcnandsalesamount.png)

    <span data-ttu-id="2984f-217">แผนภูมิตอนนี้ใช้หน่วยวัดสองตัวคือ: **SalesAmount** ซึ่ง Power BI จะรวมโดยอัตโนมัติและหน่วยวัด **ยอดขายสุทธิ** ที่คุณสร้างด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="2984f-217">The chart now uses two measures: **SalesAmount**, which Power BI summed automatically, and the **Net Sales** measure, which you manually created.</span></span> <span data-ttu-id="2984f-218">หน่วยวัดแต่ละหน่วยจะได้รับการคำนวณในบริบทของเขตข้อมูลอื่น **RegionCountryName**</span><span class="sxs-lookup"><span data-stu-id="2984f-218">Each measure was calculated in the context of another field, **RegionCountryName**.</span></span>
    
### <a name="use-your-measure-with-a-slicer"></a><span data-ttu-id="2984f-219">ใช้หน่วยวัดของคุณกับตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2984f-219">Use your measure with a slicer</span></span>

<span data-ttu-id="2984f-220">เพิ่มตัวแบ่งส่วนข้อมูลเพื่อกรองยอดขายสุทธิและยอดขายตามปีปฏิทินเพิ่มเติม:</span><span class="sxs-lookup"><span data-stu-id="2984f-220">Add a slicer to further filter net sales and sales amounts by calendar year:</span></span>
    
1. <span data-ttu-id="2984f-221">เลือกพื้นที่ว่างที่อยู่ถัดจากแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="2984f-221">Select a blank area next to the chart.</span></span> <span data-ttu-id="2984f-222">ในบานหน้าต่าง **การแสดงภาพ** ให้เลือกการแสดงภาพ **ตาราง**</span><span class="sxs-lookup"><span data-stu-id="2984f-222">In the **Visualizations** pane, select the **Table** visualization.</span></span> 

    <span data-ttu-id="2984f-223">การดำเนินการนี้จะเป็นการสร้างการแสดงภาพตารางที่ว่างเปล่าบนพื้นที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="2984f-223">This action creates a blank table visualization on the report canvas.</span></span>
    
    ![การแสดงภาพตารางที่ว่างเปล่าใหม่](media/desktop-tutorial-create-measures/meastut_netsales_blanktable.png)
    
1. <span data-ttu-id="2984f-225">ลากเขตข้อมูล **ปี** จากตาราง **ปฏิทิน** ไปยังการแสดงภาพตารางที่ว่างเปล่าใหม่</span><span class="sxs-lookup"><span data-stu-id="2984f-225">Drag the **Year** field from the **Calendar** table onto the new blank table visualization.</span></span> 
    
    <span data-ttu-id="2984f-226">เนื่องจาก **ปี** เป็นเขตข้อมูลตัวเลข Power BI Desktop จะสรุปค่า</span><span class="sxs-lookup"><span data-stu-id="2984f-226">Because **Year** is a numeric field, Power BI Desktop sums up its values.</span></span> <span data-ttu-id="2984f-227">การสรุปนี้ใช้งานไม่ได้เช่นเดียวกับการรวม เราจะจัดการเรื่องนั้นในขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="2984f-227">This summation doesn’t work well as an aggregation; we'll address that in the next step.</span></span>

    ![เพิ่มการรวมข้อมูล](media/desktop-tutorial-create-measures/meastut_netsales_yearaggtable.png)
    
3. <span data-ttu-id="2984f-229">ในกล่อง **ค่า** ในบานหน้าต่าง **การแสดงภาพ** เลือกลูกศรลงถัดจาก **ปี** จากนั้นเลือก **ไม่สรุป** จากรายการ</span><span class="sxs-lookup"><span data-stu-id="2984f-229">In the **Values** box in the **Visualizations** pane, select the down arrow next to **Year**, and then select **Don't summarize** from the list.</span></span> <span data-ttu-id="2984f-230">ตารางแสดงรายการของแต่ละปี</span><span class="sxs-lookup"><span data-stu-id="2984f-230">The table now lists individual years.</span></span>
    
    ![เลือกไม่สรุป](media/desktop-tutorial-create-measures/meastut_netsales_year_donotsummarize.png)
    
4.  <span data-ttu-id="2984f-232">เลือกไอคอน **ตัวแบ่งส่วนข้อมูล** ในบานหน้าต่าง **การแสดงภาพ** เพื่อเปลี่ยนตารางเป็นตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2984f-232">Select the **Slicer** icon in the **Visualizations** pane to convert the table to a slicer.</span></span> <span data-ttu-id="2984f-233">ถ้าการแสดงภาพแสดงแถบเลื่อนแทนที่จะเป็นรายการ ให้เลือก **รายการ** จากลูกศรลงในแถบเลื่อน</span><span class="sxs-lookup"><span data-stu-id="2984f-233">If the visualization displays a slider instead of a list, select **List** from the down arrow in the slider.</span></span>

    ![แปลงตารางเป็นตัวแบ่งส่วนข้อมูล](media/desktop-tutorial-create-measures/meastut_netsales_year_changetoslicer.png)
    
5.  <span data-ttu-id="2984f-235">เลือกค่าใด ๆ ในตัวแบ่งส่วนข้อมูลของ **ปี** เพื่อกรอง **ยอดขายสุทธิและจำนวนยอดขายตามแผนภูมิ RegionCountryName** ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="2984f-235">Select any value in the **Year** slicer to filter the **Net Sales and Sales Amount by RegionCountryName** chart accordingly.</span></span> <span data-ttu-id="2984f-236">หน่วยวัด **ยอดขายสุทธิ** และ **SalesAmount** ทำการคำนวณอีกครั้งและแสดงผลลัพธ์ในบริบทของเขตข้อมูล **ปี** ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2984f-236">The **Net Sales** and **SalesAmount** measures recalculate and display results in the context of the selected **Year** field.</span></span> 
    
    ![แผนภูมิส่วน ๆ ตามปี](media/desktop-tutorial-create-measures/meastut_netsales_chartslicedbyyear.png)

### <a name="use-your-measure-in-another-measure"></a><span data-ttu-id="2984f-238">ใช้การวัดในหน่วยวัดอื่น</span><span class="sxs-lookup"><span data-stu-id="2984f-238">Use your measure in another measure</span></span>

<span data-ttu-id="2984f-239">สมมติว่าคุณต้องการค้นหาผลิตภัณฑ์ที่มียอดขายสุทธิสูงสุดต่อหน่วยที่ขาย</span><span class="sxs-lookup"><span data-stu-id="2984f-239">Suppose you want to find out which products have the highest net sales amount per unit sold.</span></span> <span data-ttu-id="2984f-240">คุณจะต้องมีหน่วยวัดที่หารยอดขายสุทธิตามปริมาณของหน่วยที่ขาย</span><span class="sxs-lookup"><span data-stu-id="2984f-240">You'll need a measure that divides net sales by the quantity of units sold.</span></span> <span data-ttu-id="2984f-241">สร้างหน่วยวัดใหม่ที่หารผลลัพธ์ของหน่วยวัด **ยอดขายสุทธิ** ของคุณ ด้วยผลรวมของ **Sales[SalesQuantity]**</span><span class="sxs-lookup"><span data-stu-id="2984f-241">Create a new measure that divides the result of your **Net Sales** measure by the sum of **Sales[SalesQuantity]**.</span></span>

1.  <span data-ttu-id="2984f-242">ในบานหน้าต่าง **เขตข้อมูล** สร้างหน่วยวัดใหม่ที่ชื่อว่า **ยอดขายสุทธิต่อหน่วย** ในตาราง **ยอดขาย**</span><span class="sxs-lookup"><span data-stu-id="2984f-242">In the **Fields** pane, create a new measure named **Net Sales per Unit** in the **Sales** table.</span></span>
    
1. <span data-ttu-id="2984f-243">ในแถบสูตร เริ่มพิมพ์ *Net Sales*</span><span class="sxs-lookup"><span data-stu-id="2984f-243">In the formula bar, begin typing *Net Sales*.</span></span> <span data-ttu-id="2984f-244">รายการคำแนะนำจะแสดงสิ่งที่คุณสามารถเพิ่มได้</span><span class="sxs-lookup"><span data-stu-id="2984f-244">The suggestion list shows what you can add.</span></span> <span data-ttu-id="2984f-245">เลือก **[ยอดขายสุทธิ]**</span><span class="sxs-lookup"><span data-stu-id="2984f-245">Select **[Net Sales]**.</span></span>
    
    ![สูตรที่ใช้ยอดขายสุทธิ](media/desktop-tutorial-create-measures/meastut_nspu_formulastep2a.png)
    
1. <span data-ttu-id="2984f-247">คุณยังสามารถอ้างอิงหน่วยวัด โดยเพียงแค่พิมพ์วงเล็บเปิด ( **[** ) ได้</span><span class="sxs-lookup"><span data-stu-id="2984f-247">You can also reference measures by just typing an opening bracket (**[**).</span></span> <span data-ttu-id="2984f-248">รายการคำแนะนำจะแสดงเฉพาะหน่วยวัดที่จะเพิ่มลงในสูตรของคุณเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="2984f-248">The suggestion list shows only measures to add to your formula.</span></span>
    
    ![วงเล็บเหลี่ยมแสดงหน่วยวัดเท่านั้น](media/desktop-tutorial-create-measures/meastut_nspu_formulastep2b.png)
    
1. <span data-ttu-id="2984f-250">ใส่ช่องว่าง ตัวดำเนินการหาร (/) ช่องว่างอีกอัน ฟังก์ชัน SUM จากนั้นพิมพ์ *Quantity*</span><span class="sxs-lookup"><span data-stu-id="2984f-250">Enter a space, a divide operator (/), another space, a SUM function, and then type *Quantity*.</span></span> <span data-ttu-id="2984f-251">รายการคำแนะนำแสดงคอลัมน์ทั้งหมดทีมี *Quantity* อยู่ในชื่อ</span><span class="sxs-lookup"><span data-stu-id="2984f-251">The suggestion list shows all the columns with *Quantity* in the name.</span></span> <span data-ttu-id="2984f-252">เลือก **Sales[SalesQuantity]** พิมพ์วงเล็บปิดและกด **ENTER** หรือเลือก **ยืนยัน** (ไอคอนเครื่องหมายถูก) เพื่อตรวจสอบความถูกต้องสูตรของคุณ</span><span class="sxs-lookup"><span data-stu-id="2984f-252">Select **Sales[SalesQuantity]**, type the closing parenthesis, and press **ENTER** or select **Commit** (checkmark icon) to validate your formula.</span></span> 

    <span data-ttu-id="2984f-253">สูตรผลลัพธ์ควรปรากฏเป็น:</span><span class="sxs-lookup"><span data-stu-id="2984f-253">The resulting formula should appear as:</span></span>
    
    `Net Sales per Unit = [Net Sales] / SUM(Sales[SalesQuantity])`
    
1. <span data-ttu-id="2984f-254">เลือกหน่วยวัด **ยอดขายสุทธิต่อหน่วย** จากตาราง **ยอดขาย** หรือลากไปยังพื้นที่ว่างในพื้นที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="2984f-254">Select the **Net Sales per Unit** measure from the **Sales** table, or drag it onto a blank area in the report canvas.</span></span> 

    <span data-ttu-id="2984f-255">แผนภูมิแสดงยอดขายสุทธิต่อหน่วยในผลิตภัณฑ์ทั้งหมดที่ขาย</span><span class="sxs-lookup"><span data-stu-id="2984f-255">The chart shows the net sales amount per unit over all products sold.</span></span> <span data-ttu-id="2984f-256">แผนภูมินี้ไม่มีข้อมูลมากนัก เราจะจัดการเรื่องนั้นในขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="2984f-256">This chart isn't very informative; we'll   address it in the next step.</span></span>
    
    ![สุทธิยอดขายต่อหน่วยโดยรวม](media/desktop-tutorial-create-measures/meastut_nspu_chart.png)
    
1. <span data-ttu-id="2984f-258">เพื่อให้มีลักษณะแตกต่างกัน เปลี่ยนชนิดของการแสดงภาพแผนภูมิสำหรับ **ทรีแมป**</span><span class="sxs-lookup"><span data-stu-id="2984f-258">For a different look, change the chart visualization type to **Treemap**.</span></span>
    
    ![เปลี่ยนเป็นทรีแมป](media/desktop-tutorial-create-measures/meastut_nspu_changetotreemap.png)
    
1. <span data-ttu-id="2984f-260">เลือกเขตข้อมูล **ประเภทผลิตภัณฑ์** หรือลากไปยังเขตข้อมูลแผนที่ต้นไม้ หรือ **กลุ่ม** ของบานหน้าต่าง **การแสดงภาพ**</span><span class="sxs-lookup"><span data-stu-id="2984f-260">Select the **Product Category** field, or drag it onto the treemap or the **Group** field of the **Visualizations** pane.</span></span> <span data-ttu-id="2984f-261">ขณะนี้ คุณมีข้อมูลดีบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="2984f-261">Now you have some good info!</span></span>
    
    ![ทรีแมปตามประเภทผลิตภัณฑ์](media/desktop-tutorial-create-measures/meastut_nspu_byproductcat.png)
    
7. <span data-ttu-id="2984f-263">ให้พยายามลบเขตข้อมูล **ProductCategory** และลากเขตข้อมูล **ProductName** ไปยังแผนภูมิแทน</span><span class="sxs-lookup"><span data-stu-id="2984f-263">Try removing the **ProductCategory** field, and dragging the **ProductName** field onto the chart instead.</span></span> 
    
    ![ทรีแมปตามชื่อผลิตภัณฑ์](media/desktop-tutorial-create-measures/meastut_nspu_byproductname.png)
    
   <span data-ttu-id="2984f-265">ตกลง ขณะนี้เรากำลังเล่นอยู่เท่านั้น แต่คุณจำเป็นต้องยอมรับว่ามันยอดเยี่ยม</span><span class="sxs-lookup"><span data-stu-id="2984f-265">Ok, now we're just playing, but you have to admit that's cool!</span></span> <span data-ttu-id="2984f-266">ทดลองใช้วิธีอื่นๆ ในการกรองและจัดรูปแบบการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="2984f-266">Experiment with other ways to filter and format the visualization.</span></span>

## <a name="what-youve-learned"></a><span data-ttu-id="2984f-267">สิ่งที่คุณได้เรียนรู้</span><span class="sxs-lookup"><span data-stu-id="2984f-267">What you've learned</span></span>
<span data-ttu-id="2984f-268">หน่วยวัดจะช่วยให้คุณสามารถรับข้อมูลเชิงลึกที่คุณต้องการจากข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="2984f-268">Measures give you the power to get the insights you want from your data.</span></span> <span data-ttu-id="2984f-269">คุณได้เรียนรู้วิธีการสร้างหน่วยวัดโดยใช้แถบสูตร ตั้งชือให้เหมาะสมที่สุด และค้นหาและเลือกองค์ประกอบของสูตรที่ใช่ โดยใช้รายการคำแนะนำของ DAX</span><span class="sxs-lookup"><span data-stu-id="2984f-269">You've learned how to create measures by using the formula bar, name them whatever makes most sense, and find and select the right formula elements by using the DAX suggestion lists.</span></span> <span data-ttu-id="2984f-270">คุณถูกแนะนำให้รู้จักกับบริบท ซึ่งเป็นผลลัพธ์ของการคำนวณ ที่หน่วยวัดได้เปลี่ยนตามเขตข้อมูลอื่นๆ หรือนิพจน์อื่นๆในสูตรของคุณ</span><span class="sxs-lookup"><span data-stu-id="2984f-270">You've also been introduced to context, where the results of calculations in measures change according to other fields or other expressions in your formula.</span></span>

## <a name="next-steps"></a><span data-ttu-id="2984f-271">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="2984f-271">Next steps</span></span>
- <span data-ttu-id="2984f-272">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับตัววัดแบบด่วนของ Power BI Desktop ที่มีการคำนวณหน่วยวัดทั่วไปมากมายให้คุณ ให้ดู[ใช้ตัววัดแบบด่วนเพื่อดำเนินการการคำนวณทั่วไปและแบบมีประสิทธิภาพได้อย่างง่ายดาย](desktop-quick-measures.md)</span><span class="sxs-lookup"><span data-stu-id="2984f-272">To learn more about Power BI Desktop quick measures, which provide many common measure calculations for you, see [Use quick measures to easily perform common and powerful calculations](desktop-quick-measures.md).</span></span>
  
- <span data-ttu-id="2984f-273">ถ้าคุณต้องการเจาะลึกลงในสูตร DAX และสร้างหน่วยวัดขั้นสูงเพิ่มเติม ให้ดู[พื้นฐาน DAX ใน Power BI Desktop](desktop-quickstart-learn-dax-basics.md)</span><span class="sxs-lookup"><span data-stu-id="2984f-273">If you want to take a deeper dive into DAX formulas and create some more advanced measures, see [DAX basics in Power BI Desktop](desktop-quickstart-learn-dax-basics.md).</span></span> <span data-ttu-id="2984f-274">บทความนี้มุ่งเน้นแนวคิดพื้นฐานใน DAX เช่นไวยากรณ์ ฟังก์ชัน และทำความเข้าใจบริบทโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="2984f-274">This article focuses on fundamental concepts in DAX, such as syntax, functions, and a more thorough understanding of context.</span></span>
  
- <span data-ttu-id="2984f-275">โปรดให้แน่ใจว่าได้เพิ่ม[ข้ออ้างอิง Data Analysis Expressions (DAX)](/dax/index)ไปยังรายการโปรดของคุณ</span><span class="sxs-lookup"><span data-stu-id="2984f-275">Be sure to add the [Data Analysis Expressions (DAX) Reference](/dax/index) to your favorites.</span></span> <span data-ttu-id="2984f-276">การอ้างอิงนี้คือที่ที่คุณสามารถค้นหาข้อมูลโดยละเอียดเกี่ยวกับไวยากรณ์ DAX ตัวดำเนินการ และฟังก์ชัน DAX มากกว่า 200 ฟังก์ชันโดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="2984f-276">This reference is where you'll find detailed info on DAX syntax, operators, and over 200 DAX functions.</span></span>