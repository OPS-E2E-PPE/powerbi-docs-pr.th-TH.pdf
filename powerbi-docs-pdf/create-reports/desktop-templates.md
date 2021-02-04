---
title: การใช้เทมเพลตใน Power BI Desktop
description: สร้างและแชร์เทมเพลตใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 08/16/2019
LocalizationGroup: Connect to data
ms.openlocfilehash: 71e7167be5f39868b36211fd906cccf482cada5c
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412724"
---
# <a name="create-report-templates-for-power-bi-desktop"></a><span data-ttu-id="5d8ce-103">สร้างเทมเพลตของรายงานสำหรับ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="5d8ce-103">Create report templates for Power BI Desktop</span></span>

<span data-ttu-id="5d8ce-104">ด้วย **Power BI Desktop** คุณสามารถสร้างรายงานที่น่าสนใจซึ่งแบ่งปันข้อมูลเชิงลึกทั่วทั้งองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="5d8ce-104">With **Power BI Desktop,** you can create compelling reports that share insights across your entire organization.</span></span> <span data-ttu-id="5d8ce-105">ด้วย **เทมเพลต** Power BI Desktop คุณสามารถทำให้งานของคุณคล่องตัวขึ้นด้วยการสร้างเทมเพลตรายงานโดยยึดตามเทมเพลตที่มีอยู่ ซึ่งคุณหรือผู้ใช้รายอื่นในองค์กรของคุณสามารถใช้เป็นจุดเริ่มต้นสำหรับโครงร่าง แบบจำลองข้อมูล และคิวรี่ของรายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="5d8ce-105">With Power BI Desktop **templates**, you can streamline your work by creating a report template, based on an existing template, which you or other users in your organization can use as a starting point for a new report's layout, data model, and queries.</span></span> <span data-ttu-id="5d8ce-106">เทมเพลตใน **Power BI Desktop** ช่วยให้คุณเริ่มต้นได้อย่างรวดเร็วและสร้างมาตรฐานรายงานได้</span><span class="sxs-lookup"><span data-stu-id="5d8ce-106">Templates in **Power BI Desktop** help you jump-start and standardize report creation.</span></span>

![ส่งออกรายงานเป็นเทมเพลต](media/desktop-templates/desktop-templates-01.png)

## <a name="creating-templates"></a><span data-ttu-id="5d8ce-108">การสร้างเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="5d8ce-108">Creating templates</span></span>

<span data-ttu-id="5d8ce-109">เทมเพลตรายงาน Power BI ประกอบด้วยข้อมูลต่อไปนี้จากรายงานที่สร้างขึ้น:</span><span class="sxs-lookup"><span data-stu-id="5d8ce-109">Power BI report templates contain the following information from the report from which they were generated:</span></span>

* <span data-ttu-id="5d8ce-110">**หน้า** รายงาน ภาพวิชวล และองค์ประกอบวิชวลอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="5d8ce-110">Report **pages**, visuals, and other visual elements</span></span>
* <span data-ttu-id="5d8ce-111">**คำนิยามแบบจำลองข้อมูล** รวมถึงสคีมา ความสัมพันธ์ หน่วยวัด และวัตถุคำนิยามแบบจำลองอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="5d8ce-111">The **data model definition**, including the schema, relationships, measures, and other model definition artifacts</span></span>
* <span data-ttu-id="5d8ce-112">**คำนิยามคิวรี** ทั้งหมด เช่น คิวรี พารามิเตอร์คิวรี และองค์ประกอบคิวรีอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="5d8ce-112">All **query definitions**, such as queries, Query Parameters, and other query elements</span></span>

<span data-ttu-id="5d8ce-113">สิ่งที่ *ไม่ได้* รวมอยู่ในเทมเพลตคือข้อมูลของรายงาน</span><span class="sxs-lookup"><span data-stu-id="5d8ce-113">What is *not* included in templates is the report's data.</span></span> 

<span data-ttu-id="5d8ce-114">เทมเพลตรายงานรายงานใช้ส่วนขยายไฟล์ .PBIT (เปรียบเทียบกับรายงาน Power BI Desktop ซึ่งใช้ส่วนขยาย .PBIX)</span><span class="sxs-lookup"><span data-stu-id="5d8ce-114">Report templates use the file extension .PBIT (compare to Power BI Desktop reports, which use the .PBIX extension).</span></span> 

<span data-ttu-id="5d8ce-115">เมื่อต้องการสร้างเทมเพลตรายงาน ให้เลือก **ไฟล์ > ส่งออกแม่ > เทมเพลต Power BI** จากเมนูซึ่งจะแสดงหน้าต่างต่อไปนี้ และแสดงพร้อมท์ให้คุณใส่คำอธิบายสำหรับเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="5d8ce-115">To create a report template, select **File > Export > Power BI template** from the menu, which brings up the following window, which prompts you to provide a description for the template.</span></span> <span data-ttu-id="5d8ce-116">ในตัวอย่างนี้ คำอธิบายสำหรับเทมเพลตของเราคือ *เทมเพลตรายงานการขายรายเดือน*</span><span class="sxs-lookup"><span data-stu-id="5d8ce-116">In this example, our description for the template is *Monthly sales report template.*</span></span>

![ส่งออกกล่องโต้ตอบคำอธิบายเทมเพลต](media/desktop-templates/desktop-templates-02.png)

<span data-ttu-id="5d8ce-118">เลือก **ตกลง** และคุณจะได้รับพร้อมท์ให้ระบุตำแหน่งไฟล์เพื่อจัดเก็บไฟล์เทมเพลต .PBIT</span><span class="sxs-lookup"><span data-stu-id="5d8ce-118">Select **OK** and you're prompted for a file location to store the .PBIT template file.</span></span>

![ตำแหน่งที่ตั้งเทมเพลต](media/desktop-templates/desktop-templates-03.png)

<span data-ttu-id="5d8ce-120">และนั่นคือเทมเพลตรายงาน Power BI ของคุณถูกสร้างขึ้นในตำแหน่งไฟล์ที่คุณระบุด้วยนามสกุล .PBIT</span><span class="sxs-lookup"><span data-stu-id="5d8ce-120">And that's it, your Power BI report template is created in the file location you specified, with the .PBIT extension.</span></span>

> [!NOTE]
> <span data-ttu-id="5d8ce-121">โดยทั่วไปไฟล์เทมเพลตรายงาน Power BI นั้นมีขนาดเล็กกว่ารายงาน Power BI Desktop มากเนื่องจากเทมเพลตจะไม่มีข้อมูลใดเลย มีเพียงแค่คำนิยามรายงานเท่านั้นเอง</span><span class="sxs-lookup"><span data-stu-id="5d8ce-121">Power BI report template files are generally much smaller than a Power BI Desktop report, because templates to not contain any data - just the report definitions themselves.</span></span> 

## <a name="using-templates"></a><span data-ttu-id="5d8ce-122">การใช้เทมเพลต</span><span class="sxs-lookup"><span data-stu-id="5d8ce-122">Using templates</span></span>

<span data-ttu-id="5d8ce-123">เมื่อต้องการใช้เทมเพลตรายงาน Power BI เพียงแค่เปิดเทมเพลตใน Power BI Desktop และเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="5d8ce-123">To use a Power BI report template, simply open it in Power BI Desktop and begin using it.</span></span> <span data-ttu-id="5d8ce-124">คุณสามารถเปิดเทมเพลรายงาน Power BI ได้สองวิธี:</span><span class="sxs-lookup"><span data-stu-id="5d8ce-124">You can open Power BI report templates in two ways:</span></span>

* <span data-ttu-id="5d8ce-125">ดับเบิลคลิกที่ไฟล์ .PBIT ใดก็ตามเพื่อเรียกใช้ Power BI Desktop โดยอัตโนมัติและโหลดเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="5d8ce-125">Double-click on any .PBIT file to automatically launch Power BI Desktop and load the template</span></span>
* <span data-ttu-id="5d8ce-126">เลือก **ไฟล์ > นำเข้า > เทมเพลต Power BI** จากภายใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="5d8ce-126">Select **File > Import > Power BI template** from within Power BI Desktop</span></span>

![นำเข้าเทมเพลต](media/desktop-templates/desktop-templates-04.png)

<span data-ttu-id="5d8ce-128">เมื่อคุณเปิดเทมเพลตรายงาน กล้องโต้ตอบจะปรากฏค่าสำหรับพารามิเตอร์ใดก็ตามที่กำหนดไว้ในรายงานที่มีการใช้เทมเพลต</span><span class="sxs-lookup"><span data-stu-id="5d8ce-128">When you open a report template, a dialog appears values for any parameters that are defined in the report on which the template is based.</span></span> <span data-ttu-id="5d8ce-129">ตัวอย่างเช่น หากรายงานวิเคราะห์ลูกค้ายึดตามประเทศหรือภูมิภาคและมีพารามิเตอร์ *ประเทศ* เพื่อระบุฐานลูกค้า พร้อมท์จะปรากฏข้อความแจ้งให้คุณเลือกค่า *ประเทศ* จากรายการค่าที่ระบุเมื่อกำหนดพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="5d8ce-129">For example, if a report analyzes customers based on country or region and has a *Country* parameter to specify the customer base, a prompt appears for you to select a *Country* value from the list of values that were specified when defining the parameter.</span></span> 

![ระบุพารามิเตอร์สำหรับเทมเพลต](media/desktop-templates/desktop-templates-05a.png)

<span data-ttu-id="5d8ce-131">เมื่อมีการระบุพารามิเตอร์ที่จำเป็นแล้ว คุณจะได้รับพร้อมท์ให้ระบุตำแหน่งของข้อมูลพื้นฐานที่เกี่ยวข้องกับรายงาน</span><span class="sxs-lookup"><span data-stu-id="5d8ce-131">Once any required parameters are provided, you're prompted for the location of the underlying data associated with the report.</span></span> <span data-ttu-id="5d8ce-132">หลังจากนั้นผู้สร้างรายงานปัจจุบันสามารถเชื่อมต่อกับข้อมูลตามข้อมูลประจำตัวของพวกเขาได้</span><span class="sxs-lookup"><span data-stu-id="5d8ce-132">The current report creator can then connect to data based on their credentials.</span></span>

![ระบุตำแหน่งที่ตั้งข้อมูลสำหรับเทมเพลต](media/desktop-templates/desktop-templates-05.png)

<span data-ttu-id="5d8ce-134">เมื่อมีการระบุพารามิเตอร์และข้อมูลแล้ว รายงานจะถูกสร้างขึ้นซึ่งประกอบด้วยหน้า วิชวล วัตถุแบบจำลองข้อมูล และคิวรีทั้งหมดที่เป็นส่วนหนึ่งของรายงานที่มีการใช้เทมเพลต</span><span class="sxs-lookup"><span data-stu-id="5d8ce-134">Once parameters and data have been specified, a report is created containing all the pages, visuals, data model artifacts, and queries that were part of the report on which the template is based.</span></span> 

<span data-ttu-id="5d8ce-135">เสร็จแล้ว!</span><span class="sxs-lookup"><span data-stu-id="5d8ce-135">That's it.</span></span> <span data-ttu-id="5d8ce-136">การสร้างและการใช้เทมเพลตรายงานใน Power BI Desktop นั้นง่ายดาย ช่วยให้คุณสร้างเค้าโครงที่น่าสนใจและลักษณะอื่นของรายงาน และแบ่งปันกับผู้อื่นได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="5d8ce-136">Creating and using report templates in Power BI Desktop is easy, enabling you to easily reproduce compelling layouts and other report aspects, and share them with others.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5d8ce-137">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="5d8ce-137">Next steps</span></span>
<span data-ttu-id="5d8ce-138">นอกจากนี้ คุณอาจสนใจที่จะเรียนรู้เพิ่มเติมเกี่ยวกับ **พารามิเตอร์แบบสอบถาม**:</span><span class="sxs-lookup"><span data-stu-id="5d8ce-138">You might also be interested in learning about **Query Parameters**:</span></span>
* [<span data-ttu-id="5d8ce-139">การใช้พารามิเตอร์แบบสอบถามใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="5d8ce-139">Using Query Parameters in Power BI Desktop?</span></span>](/power-query/power-query-query-parameters)

<span data-ttu-id="5d8ce-140">นอกจากนี้ยังมีอีกหลายสิ่งที่คุณสามารถทำได้ด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="5d8ce-140">In addition, there are all sorts of things you can do with Power BI Desktop.</span></span> <span data-ttu-id="5d8ce-141">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับขีดความสามารถ กรุณาดูแหล่งทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5d8ce-141">For more information on its capabilities, check out the following resources:</span></span>

* [<span data-ttu-id="5d8ce-142">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="5d8ce-142">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="5d8ce-143">ภาพรวมคิวรี ด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="5d8ce-143">Query Overview with Power BI Desktop</span></span>](../transform-model/desktop-query-overview.md)
* [<span data-ttu-id="5d8ce-144">ชนิดข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="5d8ce-144">Data Types in Power BI Desktop</span></span>](../connect-data/desktop-data-types.md)
* [<span data-ttu-id="5d8ce-145">จัดรูปทรง และรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="5d8ce-145">Shape and Combine Data with Power BI Desktop</span></span>](../connect-data/desktop-shape-and-combine-data.md)
* [<span data-ttu-id="5d8ce-146">งานคิวรี่ทั่วไปใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="5d8ce-146">Common Query Tasks in Power BI Desktop</span></span>](../transform-model/desktop-common-query-tasks.md)