---
title: ส่วนที่ 1 เพิ่มการแสดงภาพไปยังรายงาน Power BI
description: ส่วนที่ 1 เพิ่มการแสดงภาพไปยังรายงาน Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
featuredvideoid: ''
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 05/06/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 4d4b04b10e45d67fdd4d7cb183e300587d4f2cc6
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412494"
---
# <a name="add-visuals-to-a-power-bi-report-part-1"></a><span data-ttu-id="06b59-103">เพิ่มวิชวลไปยังรายงาน Power BI (ตอนที่ 1)</span><span class="sxs-lookup"><span data-stu-id="06b59-103">Add visuals to a Power BI report (part 1)</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]    

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="06b59-104">บทความนี้ให้คำแนะนำสั้น ๆ สำหรับการสร้างวิชวลในรายงาน</span><span class="sxs-lookup"><span data-stu-id="06b59-104">This article gives a quick introduction to creating a visualization in a report.</span></span> <span data-ttu-id="06b59-105">รายงานสามารถใช้ได้ทั้งบริการของ Power BI และ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="06b59-105">It applies to both the Power BI service and Power BI Desktop.</span></span> <span data-ttu-id="06b59-106">สำหรับเนื้อหาขั้นสูง ให้ดูที่ [ส่วนที่ 2](power-bi-report-add-visualizations-ii.md)ของชุดข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="06b59-106">For more-advanced content, [see Part 2](power-bi-report-add-visualizations-ii.md) of this series.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="06b59-107">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="06b59-107">Prerequisites</span></span>

<span data-ttu-id="06b59-108">บทช่วยสอนนี้ใช้ [ไฟล์ PBIX ตัวอย่างการขายและการตลาด](https://download.microsoft.com/download/9/7/6/9767913A-29DB-40CF-8944-9AC2BC940C53/Sales%20and%20Marketing%20Sample%20PBIX.pbix)</span><span class="sxs-lookup"><span data-stu-id="06b59-108">This tutorial uses the [Sales & marketing PBIX file](https://download.microsoft.com/download/9/7/6/9767913A-29DB-40CF-8944-9AC2BC940C53/Sales%20and%20Marketing%20Sample%20PBIX.pbix).</span></span>

1. <span data-ttu-id="06b59-109">จากด้านบนซ้ายของแถบเมนู Power BI Desktop เลือก **ไฟล์** > **เปิด**</span><span class="sxs-lookup"><span data-stu-id="06b59-109">From the upper left section of the Power BI Desktop menu bar, select **File** > **Open**</span></span>
   
2. <span data-ttu-id="06b59-110">ค้นหาสำเนาของ **ไฟล์ PBIX ตัวอย่างการขายและการตลาด** ของคุณ</span><span class="sxs-lookup"><span data-stu-id="06b59-110">Find your copy of the **Sales and marketing sample PBIX file**</span></span>

1. <span data-ttu-id="06b59-111">เปิด **ไฟล์ PBIX ตัวอย่างการขายและการตลาด** ในมุมมองรายงาน ![สกรีนช็อตไอคอนมุมมองรายงาน](media/power-bi-visualization-kpi/power-bi-report-view.png)</span><span class="sxs-lookup"><span data-stu-id="06b59-111">Open the **Sales and marketing sample PBIX file** in report view ![Screenshot of the report view icon.](media/power-bi-visualization-kpi/power-bi-report-view.png).</span></span>

1. <span data-ttu-id="06b59-112">เลือก</span><span class="sxs-lookup"><span data-stu-id="06b59-112">Select</span></span> ![สกรีนช็อตของแท็บสีเหลือง](media/power-bi-visualization-kpi/power-bi-yellow-tab.png) <span data-ttu-id="06b59-114">หากต้องการเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="06b59-114">to add a new page.</span></span>

> [!NOTE]
> <span data-ttu-id="06b59-115">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="06b59-115">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span> <span data-ttu-id="06b59-116">ดู [การแชร์รายงาน](../collaborate-share/service-share-reports.md)</span><span class="sxs-lookup"><span data-stu-id="06b59-116">See [sharing reports](../collaborate-share/service-share-reports.md)</span></span>

## <a name="add-visualizations-to-the-report"></a><span data-ttu-id="06b59-117">เพิ่มการแสดงภาพลงในรายงาน</span><span class="sxs-lookup"><span data-stu-id="06b59-117">Add visualizations to the report</span></span>

1. <span data-ttu-id="06b59-118">สร้างการแสดงภาพ โดยการเลือกเขตข้อมูลจากบานหน้าต่าง **เขตข้อมูล** บานหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="06b59-118">Create a visualization by selecting a field from the **Fields** pane.</span></span>

    <span data-ttu-id="06b59-119">เริ่มต้นด้วยเขตข้อมูลตัวเลข เช่น **Sales** > **TotalSales**</span><span class="sxs-lookup"><span data-stu-id="06b59-119">Start with a numeric field like **Sales** > **TotalSales**.</span></span> <span data-ttu-id="06b59-120">Power BI จะสร้างแผนภูมิคอลัมน์ที่มีคอลัมน์เดียว</span><span class="sxs-lookup"><span data-stu-id="06b59-120">Power BI creates a column chart with a single column.</span></span>

    ![สกรีนช็อตของแผนภูมิคอลัมน์ที่มีคอลัมน์เดียว](media/power-bi-report-add-visualizations-i/power-bi-column-chart.png)

    <span data-ttu-id="06b59-122">หรือ เริ่มต้น ด้วยประเภทของเขตข้อมูลเช่น **ชื่อ** หรือ **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="06b59-122">Or, start with a category field, such as **Name** or **Product**.</span></span> <span data-ttu-id="06b59-123">Power BI สร้างตารางและเพิ่มเขตข้อมูลนั้นไปยังส่วนที่เป็น **ค่าตัวเลข** ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="06b59-123">Power BI creates a table and adds that field to the **Values** well.</span></span>

    ![สกรีนช็อตของตารางที่มีสี่หมวดหมู่](media/power-bi-report-add-visualizations-i/power-bi-product.png)

    <span data-ttu-id="06b59-125">หรือเริ่มต้น ด้วยเขตข้อมูลภูมิศาสตร์เช่น **ภูมิศาสตร์** > **เมือง**</span><span class="sxs-lookup"><span data-stu-id="06b59-125">Or, start with a geography field, such as **Geo** > **City**.</span></span> <span data-ttu-id="06b59-126">Power BI และ Bing Maps จะสร้างการแสดงภาพแผนที่ให้</span><span class="sxs-lookup"><span data-stu-id="06b59-126">Power BI and Bing Maps create a map visualization.</span></span>

    ![สกรีนช๊อตของการแสดงภาพของแผนที่](media/power-bi-report-add-visualizations-i/power-bi-maps.png)

## <a name="change-the-type-of-visualization"></a><span data-ttu-id="06b59-128">เปลี่ยนชนิดของการแสดงผลข้อมูลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="06b59-128">Change the type of visualization</span></span>

 <span data-ttu-id="06b59-129">สร้างการแสดงภาพ แล้วเปลี่ยนชนิดของการแสดงภาพนั้น</span><span class="sxs-lookup"><span data-stu-id="06b59-129">Create a visualization and then change its type.</span></span> 
 
 1. <span data-ttu-id="06b59-130">เลือก **ผลิตภัณฑ์** > **ประเภท** จากนั้น **ผลิตภัณฑ์**  >  **จำนวนผลิตภัณฑ์** เพื่อเพิ่มไปยัง **ค่า**</span><span class="sxs-lookup"><span data-stu-id="06b59-130">Select **Product** > **Category** and then **Product** > **Count of Product** to add them both to the **Values** well.</span></span>

    ![สกรีนช็อตของการเรียกบานหน้าต่างเขตข้อมูลที่มีค่าด้วยเช่นกันออกมา](media/power-bi-report-add-visualizations-i/power-bi-create-visual.png)

1. <span data-ttu-id="06b59-132">เปลี่ยนการแสดงภาพเป็นในแผนภูมิคอลัมน์ โดยการเลือกไอคอน **แผนภูมิคอลัมน์แบบเรียงซ้อน**</span><span class="sxs-lookup"><span data-stu-id="06b59-132">Change the visualization to a column chart by selecting the **Stacked column chart** icon.</span></span>

   ![สกรีนช็อตของการเรียกบานหน้าต่างการแสดงภาพที่มีไอคอนแผนภูมิคอลัมน์แบบเรียงซ้อนออกมา](media/power-bi-report-add-visualizations-i/power-bi-convert.png)

1. <span data-ttu-id="06b59-134">เมื่อต้องการเปลี่ยนวิธีการเรียงลำดับวิชวล ให้เลือก **การดำเนินการเพิ่มเติม** (...)  ใช้ตัวเลือกการเรียงลำดับเพื่อเปลี่ยนทิศทางของการเรียงลำดับ (จากน้อยไปหามากหรือมากไปหาน้อย) และเปลี่ยนคอลัมน์ที่ใช้ในการเรียงลำดับ (**เรียงลำดับตาม**)</span><span class="sxs-lookup"><span data-stu-id="06b59-134">To change the way the visual is sorted, select **More actions** (...).  Use the sort options to change the direction of the sort (ascending or descending) and change the column being used to sort (**Sort by**).</span></span>

   ![สกรีนช็อตของรายการดรอปดาวน์การดำเนินการเพิ่มเติม](media/power-bi-report-add-visualizations-i/power-bi-sort.png)
  
## <a name="next-steps"></a><span data-ttu-id="06b59-136">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="06b59-136">Next steps</span></span>

 <span data-ttu-id="06b59-137">ไปต่อยัง:</span><span class="sxs-lookup"><span data-stu-id="06b59-137">Continue on to:</span></span>

* [<span data-ttu-id="06b59-138">ส่วนที่ 2: เพิ่มภาพไปยังรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="06b59-138">Part 2: Add visualizations to a Power BI report</span></span>](power-bi-report-add-visualizations-ii.md)

* <span data-ttu-id="06b59-139">[โต้ตอบกับการแสดงภาพ](../consumer/end-user-reading-view.md)ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="06b59-139">[Interact with the visualizations](../consumer/end-user-reading-view.md) in the report.</span></span>
