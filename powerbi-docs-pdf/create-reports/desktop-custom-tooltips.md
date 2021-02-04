---
title: การกำหนดคำแนะนำเครื่องมือเองใน Power BI Desktop
description: สร้างเครื่องมือคำแนะนำแบบกำหนดเองสำหรับภาพโดยใช้การลากและวาง
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 01/15/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 18658937d1e53340f4bdd5075479bd2926f295bd
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414219"
---
# <a name="customize-tooltips-in-power-bi-desktop"></a><span data-ttu-id="8cd8f-103">คำแนะนำเครื่องมือแบบกำหนดเองใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="8cd8f-103">Customize tooltips in Power BI Desktop</span></span>

<span data-ttu-id="8cd8f-104">คำแนะนำเครื่องมือเป็นวิธีที่เหมาะสมในการให้ข้อมูลตามบริบทและรายละเอียดไปยังจุดข้อมูลบนภาพได้มากกว่า</span><span class="sxs-lookup"><span data-stu-id="8cd8f-104">Tooltips are an elegant way of providing more contextual information and detail to data points on a visual.</span></span> <span data-ttu-id="8cd8f-105">รูปต่อไปนี้แสดงคำแนะนำเครื่องมือที่นำไปใช้กับแผนภูมิใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="8cd8f-105">The following image shows a tooltip applied to a chart in Power BI Desktop.</span></span>

![ค่าเริ่มต้นคำแนะนำเครื่องมือ](media/desktop-custom-tooltips/custom-tooltips-1.png)

<span data-ttu-id="8cd8f-107">เมื่อมีการสร้างภาพ คำแนะนำเครื่องมือเริ่มต้นจะแสดงค่าและประเภทของจุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8cd8f-107">When a visualization is created, the default tooltip displays the data point's value and category.</span></span> <span data-ttu-id="8cd8f-108">มีหลายกรณีเมื่อกำหนดข้อมูลคำแนะนำเครื่องมือให้เป็นประโยชน์</span><span class="sxs-lookup"><span data-stu-id="8cd8f-108">There are many instances when customizing the tooltip information is useful.</span></span> <span data-ttu-id="8cd8f-109">คำแนะนำเครื่องมือการกำหนดเองให้บริบทและข้อมูลเพิ่มเติมสำหรับผู้ใช้ที่ดูวิชวล</span><span class="sxs-lookup"><span data-stu-id="8cd8f-109">Customizing tooltips provides additional context and information for users viewing the visual.</span></span> <span data-ttu-id="8cd8f-110">คำแนะนำเครื่องมือแบบกำหนดเองช่วยให้คุณสามารถระบุจุดข้อมูลเพิ่มเติมที่แสดงเป็นส่วนหนึ่งของคำแนะนำดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="8cd8f-110">Custom tooltips enable you to specify additional data points that display as part of the tooltip.</span></span>

## <a name="how-to-customize-tooltips"></a><span data-ttu-id="8cd8f-111">วิธีการกำหนดคำแนะนำเครื่องมือด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="8cd8f-111">How to customize tooltips</span></span>

<span data-ttu-id="8cd8f-112">เมื่อต้องสร้างคำแนะนำแบบกำหนดเอง ในแอ่ง **เขตข้อมูล** ของแผง **การแสดงผลด้วยภาพ** ลากเขตข้อมูลลงในบักเก็ต **คำแนะนำเครื่องมือ** ที่แสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8cd8f-112">To create a customized tooltip, in the **Fields** well of the **Visualizations** pane, drag a field into the **Tooltips** bucket, shown in the following image.</span></span> <span data-ttu-id="8cd8f-113">ในรูปต่อไปนี้ มีสามเขตข้อมูลถูกใส่ไว้ในบักเก็ต **คำแนะนำเครื่องมือ**</span><span class="sxs-lookup"><span data-stu-id="8cd8f-113">In the following image, three fields have been placed into the **Tooltips** bucket.</span></span>

![เขตข้อมูลคำแนะนำเครื่องมือ](media/desktop-custom-tooltips/custom-tooltips-2.png)

<span data-ttu-id="8cd8f-115">เมื่อเพิ่มคำแนะนำเครื่องมือเข้าไปยัง **คำแนะนำเครื่องมือ** โฮเวอร์เหนือจุดข้อมูลบนการแสดงผลด้วยภาพ จะแสดงค่าสำหรับเขตข้อมูลเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="8cd8f-115">Once tooltips are added to **Tooltips**, hovering over a data point on the visualization shows the values for those fields.</span></span>

![คำแนะนำเครื่องมือแบบกำหนดเอง](media/desktop-custom-tooltips/custom-tooltips-3.png)

## <a name="customizing-tooltips-with-aggregation-or-quick-measures"></a><span data-ttu-id="8cd8f-117">กำหนดคำแนะนำเครื่องมือด้วยการรวมหรือการวัดผลด่วน</span><span class="sxs-lookup"><span data-stu-id="8cd8f-117">Customizing tooltips with aggregation or quick measures</span></span>

<span data-ttu-id="8cd8f-118">คุณสามารถกำหนดคำแนะนำเครื่องมือโดยการเลือกฟังก์ชันการรวมหรือ *การวัดด่วน*</span><span class="sxs-lookup"><span data-stu-id="8cd8f-118">You can further customize a tooltip by selecting an aggregation function or a *quick measure*.</span></span> <span data-ttu-id="8cd8f-119">เลือกลูกศรที่อยู่ข้างๆ เขตข้อมูลในบักเก็ต **คำแนะนำเครื่องมือ**</span><span class="sxs-lookup"><span data-stu-id="8cd8f-119">Select the arrow beside the field in the **Tooltips** bucket.</span></span> <span data-ttu-id="8cd8f-120">จากนั้นเลือกจากตัวเลือกที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8cd8f-120">Then, select from the available options.</span></span>

![คำแนะนำเครื่องมือที่มีการวัดผลด่วน](media/desktop-custom-tooltips/custom-tooltips-4.png)

<span data-ttu-id="8cd8f-122">มีหลายวิธีในการกำหนดคำแนะนำเครื่องมือด้วยตนเอง โดยการใช้เขตข้อมูลใดๆ ที่พร้อมใช้งานไปยังการสื่อข้อมูลอย่างรวดเร็วและข้อมูลเชิงลึกกับผู้ใช้ที่ดูแดชบอร์ดหรือรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="8cd8f-122">There are many ways to customize tooltips, using any field available in your dataset, to convey quick information and insights to users viewing your dashboards or reports.</span></span>
