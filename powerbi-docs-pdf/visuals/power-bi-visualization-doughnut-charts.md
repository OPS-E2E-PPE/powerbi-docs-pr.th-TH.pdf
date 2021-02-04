---
title: แผนภูมิโดนัทใน Power BI
description: แผนภูมิโดนัทใน Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 05/05/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 3ebd618011f8c7a5fefb1187283702a85dee407c
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96386200"
---
# <a name="create-and-use-doughnut-charts-in-power-bi"></a><span data-ttu-id="30558-103">สร้างและใช้แผนภูมิโดนัทใน Power BI</span><span class="sxs-lookup"><span data-stu-id="30558-103">Create and use doughnut charts in Power BI</span></span>

[!INCLUDE[consumer-appliesto-nyyn](../includes/consumer-appliesto-nyyn.md)]

[!INCLUDE [power-bi-visuals-desktop-banner](../includes/power-bi-visuals-desktop-banner.md)]

<span data-ttu-id="30558-104">แผนภูมิโดนัทจะคล้ายกับแผนภูมิวงกลมที่จะแสดงความสัมพันธ์ของข้อมูลองค์ประกอบต่างๆ กับข้อมูลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="30558-104">A doughnut chart is similar to a pie chart in that it shows the relationship of parts to a whole.</span></span> <span data-ttu-id="30558-105">ความแตกต่างเพียงประการเดียว คือ ส่วนตรงกลางนั้นว่างเปล่า และมีพื้นที่ว่างสำหรับระบุป้ายชื่อหรือไอคอน</span><span class="sxs-lookup"><span data-stu-id="30558-105">The only difference is that the center is blank and allows space for a label or icon.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="30558-106">เงื่อนไขเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="30558-106">Prerequisite</span></span>

<span data-ttu-id="30558-107">บทช่วยสอนนี้ใช้[ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix)</span><span class="sxs-lookup"><span data-stu-id="30558-107">This tutorial uses the [Retail Analysis sample PBIX file](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix).</span></span>

1. <span data-ttu-id="30558-108">จากด้านบนซ้ายของแถบเมนู เลือก **ไฟล์** > **เปิด**</span><span class="sxs-lookup"><span data-stu-id="30558-108">From the upper left section of the menubar, select **File** > **Open**</span></span>
   
2. <span data-ttu-id="30558-109">ค้นหาสำเนา **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก**</span><span class="sxs-lookup"><span data-stu-id="30558-109">Find your copy of the **Retail Analysis sample PBIX file**</span></span>

1. <span data-ttu-id="30558-110">เปิด **ไฟล์ PBIX ตัวอย่างการวิเคราะห์การค้าปลีก** ในมุมมองรายงาน ![ภาพหน้าจอไอคอนมุมมองรายงาน](media/power-bi-visualization-kpi/power-bi-report-view.png)</span><span class="sxs-lookup"><span data-stu-id="30558-110">Open the **Retail Analysis sample PBIX file** in report view ![Screenshot of the report view icon.](media/power-bi-visualization-kpi/power-bi-report-view.png).</span></span>

1. <span data-ttu-id="30558-111">เลือก</span><span class="sxs-lookup"><span data-stu-id="30558-111">Select</span></span> ![สกรีนช็อตของแท็บสีเหลือง](media/power-bi-visualization-kpi/power-bi-yellow-tab.png) <span data-ttu-id="30558-113">หากต้องการเพิ่มหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="30558-113">to add a new page.</span></span>


> [!NOTE]
> <span data-ttu-id="30558-114">การแชร์รายงานของคุณกับผู้ร่วมงาน Power BI กำหนดให้คุณต้องมีสิทธิ์การใช้งาน Power BI Pro แต่ละรายการ หรือรายงานจะถูกบันทึกในความจุแบบพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="30558-114">Sharing your report with a Power BI colleague requires that you both have individual Power BI Pro licenses or that the report is saved in Premium capacity.</span></span>    

## <a name="create-a-doughnut-chart"></a><span data-ttu-id="30558-115">สร้างแผนภูมิโดนัท</span><span class="sxs-lookup"><span data-stu-id="30558-115">Create a doughnut chart</span></span>

1. <span data-ttu-id="30558-116">เริ่มต้นที่หน้ารายงานเปล่า และจากบานหน้าต่างเขตข้อมูล เลือก **ยอดขาย** \> **ยอดขายปีล่าสุด**</span><span class="sxs-lookup"><span data-stu-id="30558-116">Start on a blank report page and from the Fields pane, select **Sales** \> **Last Year Sales**.</span></span>  
   
3. <span data-ttu-id="30558-117">ในส่วนบานหน้าต่างการแสดงภาพ ให้เลือกไอคอนสำหรับแผนภูมิโดนัท![ไอคอนแผนภูมิโดนัท](media/power-bi-visualization-doughnut-charts/power-bi-icon.png) เพื่อแปลงแผนภูมิแท่งของคุณให้กลายเป็นแผนภูมิโดนัท</span><span class="sxs-lookup"><span data-stu-id="30558-117">From the Visualizations pane, select the icon for doughnut chart ![doughnut chart icon](media/power-bi-visualization-doughnut-charts/power-bi-icon.png) to convert your bar chart to a doughnut chart.</span></span> <span data-ttu-id="30558-118">ถ้า **ยอดขายปีล่าสุด** ไม่อยู่ในพื้นที่ **ค่า** ให้ลากไปไว้ในส่วนนั้น</span><span class="sxs-lookup"><span data-stu-id="30558-118">If **Last Year Sales** is not in the **Values** area, drag it there.</span></span>
     
   ![บานหน้าต่างการแสดงภาพที่เลือกแผนภูมิโดนัทแล้ว](media/power-bi-visualization-doughnut-charts/power-bi-doughnut-chart.png)

4. <span data-ttu-id="30558-120">เลือก **หน่วยข้อมูล** \> **หมวดหมู่** เพิ่มเพิ่มรายการไปยังพื้นที่ **คำอธิบายแผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="30558-120">Select **Item** \> **Category** to add it to the **Legend** area.</span></span> 
     
    ![โดนัทถัดจากบานหน้าต่างเขตข้อมูล](media/power-bi-visualization-doughnut-charts/power-bi-doughnut-done.png)

5. <span data-ttu-id="30558-122">อีกวิธีหนึ่ง คือ [ปรับขนาดและสีของข้อความในแผนภูมิ](power-bi-visualization-customize-title-background-and-legend.md)</span><span class="sxs-lookup"><span data-stu-id="30558-122">Optionally, [adjust the size and color of the chart's text](power-bi-visualization-customize-title-background-and-legend.md).</span></span> 

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="30558-123">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="30558-123">Considerations and troubleshooting</span></span>
* <span data-ttu-id="30558-124">ผลรวมของค่าแผนภูมิโดนัทต้องเพิ่มเป็น 100%</span><span class="sxs-lookup"><span data-stu-id="30558-124">The sum of the doughnut chart values must add up to 100%.</span></span>
* <span data-ttu-id="30558-125">จำนวนประเภทที่มากเกินไปจะทำให้อ่านและตีความข้อมูลได้ยาก</span><span class="sxs-lookup"><span data-stu-id="30558-125">Too many categories make it difficult to read and interpret.</span></span>
* <span data-ttu-id="30558-126">แผนภูมิโดนัทเหมาะอย่างยิ่งที่จะใช้เพื่อเปรียบเทียบข้อมูลส่วนใดส่วนหนึ่งกับข้อมูลทั้งหมด มากกว่าจะใช้เปรียบเทียบระหว่างข้อมูลแต่ละส่วน</span><span class="sxs-lookup"><span data-stu-id="30558-126">Doughnut charts are best used to compare a particular section to the whole, rather than comparing individual sections with each other.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="30558-127">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="30558-127">Next steps</span></span>
[<span data-ttu-id="30558-128">แผนภูมิกรวยใน Power BI</span><span class="sxs-lookup"><span data-stu-id="30558-128">Funnel charts in Power BI</span></span>](power-bi-visualization-funnel-charts.md)

[<span data-ttu-id="30558-129">ชนิดการแสดงภาพใน Power BI</span><span class="sxs-lookup"><span data-stu-id="30558-129">Visualization types in Power BI</span></span>](power-bi-visualization-types-for-reports-and-q-and-a.md)


