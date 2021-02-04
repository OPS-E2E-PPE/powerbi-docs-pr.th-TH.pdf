---
title: นำเข้า และแสดง KPI ใน Power BI
description: นำเข้า และแสดง KPI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: how-to
ms.date: 05/08/2019
LocalizationGroup: Model your data
ms.openlocfilehash: c7aeb70d99b8ce32191d04d002c638c6bb69c7fb
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415645"
---
# <a name="import-and-display-kpis-in-power-bi"></a><span data-ttu-id="10fcd-103">นำเข้า และแสดง KPI ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="10fcd-103">Import and display KPIs in Power BI</span></span>
<span data-ttu-id="10fcd-104">ด้วย **Power BI Desktop** คุณสามารถนำเข้าและแสดง KPI ในตาราง, เมทริกซ์ และการ์ดได้</span><span class="sxs-lookup"><span data-stu-id="10fcd-104">With **Power BI Desktop**, you can import and display KPIs in tables, matrices, and cards.</span></span>

<span data-ttu-id="10fcd-105">ทำตามขั้นตอนเหล่านี้ เมื่อต้องการนำเข้า และแสดง KPI</span><span class="sxs-lookup"><span data-stu-id="10fcd-105">Follow these steps to import and display KPIs.</span></span>

1. <span data-ttu-id="10fcd-106">เริ่มต้นด้วยเวิร์กบุ๊ก Excel ที่มีแบบจำลอง Power Pivot และ KPI</span><span class="sxs-lookup"><span data-stu-id="10fcd-106">Start with an Excel workbook that has a Power Pivot model and KPIs.</span></span> <span data-ttu-id="10fcd-107">แบบทดสอบนี้ใช้ชื่อเวิร์กบุ๊กว่า *KPI*</span><span class="sxs-lookup"><span data-stu-id="10fcd-107">This exercise uses a workbook named *KPIs*.</span></span>

1. <span data-ttu-id="10fcd-108">นำเข้าเวิร์กบุ๊ก Excel ลงใน Power BI โดยใช้ **ไฟล์ -> นำเข้า -> เนื้อหาเวิร์กบุ๊ก Excel**</span><span class="sxs-lookup"><span data-stu-id="10fcd-108">Import the Excel workbook into Power BI, using **File -> Import -> Excel workbook contents**.</span></span> <span data-ttu-id="10fcd-109">คุณยังสามารถ[เรียนรู้วิธีการนำเข้าเวิร์กบุ๊ก](../connect-data/desktop-import-excel-workbooks.md)ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="10fcd-109">You can also [learn how to import workbooks](../connect-data/desktop-import-excel-workbooks.md).</span></span> 

1. <span data-ttu-id="10fcd-110">หลังจากนำเข้าลงใน Power BI, KPI ของคุณจะปรากฏขึ้นในบานหน้าต่าง **เขตข้อมูล** ที่ทำเครื่องหมายด้วยไอคอน![ไฟจราจร](media/desktop-import-and-display-kpis/traffic.png)</span><span class="sxs-lookup"><span data-stu-id="10fcd-110">After import into Power BI, your KPI will appear in the **Fields** pane, marked with the ![traffic light](media/desktop-import-and-display-kpis/traffic.png) icon.</span></span> <span data-ttu-id="10fcd-111">เพื่อใช้ KPI ในรายงานของคุณ ตรวจสอบให้แน่ใจว่าได้ขยายเนื้อหา ให้แสดงเขตข้อมูล **Value**, **Goal** และ **Status**</span><span class="sxs-lookup"><span data-stu-id="10fcd-111">To use a KPI in your report, be sure to expand its contents, exposing the **Value**, **Goal**, and **Status** fields.</span></span>

    ![ภาพหน้าจอของ Power BI Desktop ที่แสดง Delta KPI ที่ขยายในบานหน้าต่างเขตข้อมูล](media/desktop-import-and-display-kpis/desktoppreviewfeatureon2.png)
 
1. <span data-ttu-id="10fcd-113">KPI ที่นำเข้า เหมาะที่สุดสำหรับการแสดงภาพชนิดมาตรฐาน เช่น ชนิด **ตาราง**</span><span class="sxs-lookup"><span data-stu-id="10fcd-113">Imported KPIs are best used in standard visualization types, such as the **Table** type.</span></span> <span data-ttu-id="10fcd-114">Power BI ยังมีการแสดงภาพชนิด **KPI** ซึ่งควรใช้เพื่อสร้าง KPI ใหม่เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="10fcd-114">Power BI also includes the **KPI** visualization type, which should only be used to create new KPIs.</span></span>
   
    ![ภาพหน้าจอของ Power BI Desktop ที่แสดงเขตข้อมูล Table1 ที่เลือกในบานหน้าต่างเขตข้อมูล](media/desktop-import-and-display-kpis/desktoppreviewfeatureon3.png)

<span data-ttu-id="10fcd-116">ขั้นตอนทั้งหมดก็มีเพียงเท่านี้</span><span class="sxs-lookup"><span data-stu-id="10fcd-116">That's all there is to it.</span></span> <span data-ttu-id="10fcd-117">คุณสามารถใช้ KPI เพื่อเน้นแนวโน้มที่สำคัญ, ความคืบหน้า หรือตัวบ่งชี้ที่สำคัญอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="10fcd-117">You can use KPIs to highlight trends, progress, or other important indicators.</span></span>
