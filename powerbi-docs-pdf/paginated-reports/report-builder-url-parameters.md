---
title: พารามิเตอร์ URL ในรายงานที่มีการแบ่งหน้า - ตัวสร้างรายงาน Power BI
description: เรียนรู้วิธีการส่งคำสั่งไปยังรายงานที่มีการแบ่งหน้าใน Power BI โดยการเพิ่มพารามิเตอร์ลงใน URL ซึ่งคุณสามารถรวมไว้ในอีเมลหรือเว็บเพจได้
author: maggiesMSFT
ms.author: maggies
ms.service: powerbi
ms.subservice: report-builder
ms.topic: conceptual
ms.reviewer: cfinlan
ms.custom: ''
ms.date: 12/15/2020
ms.openlocfilehash: 4dc7d3dbb68a06f1b18714d2070b7c305390ef6b
ms.sourcegitcommit: fef29a5c5bf1e0dae663c42c9ce5ae50e29ae9be
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/16/2020
ms.locfileid: "97558481"
---
# <a name="url-parameters-in-paginated-reports-in-power-bi"></a><span data-ttu-id="5b981-103">พารามิเตอร์ URL ในรายงานที่มีการแบ่งหน้าใน Power BI</span><span class="sxs-lookup"><span data-stu-id="5b981-103">URL parameters in paginated reports in Power BI</span></span>

<span data-ttu-id="5b981-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span><span class="sxs-lookup"><span data-stu-id="5b981-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span></span> 

<span data-ttu-id="5b981-105">คุณสามารถส่งคำสั่งไปยังรายงานที่มีการแบ่งหน้าใน Power BI ได้โดยการเพิ่มพารามิเตอร์ลงใน URL</span><span class="sxs-lookup"><span data-stu-id="5b981-105">You can send commands to paginated reports in Power BI by adding a parameter to a URL.</span></span> <span data-ttu-id="5b981-106">ตัวอย่างเช่น คุณอาจมีการดูรายงานโดยใช้ชุดค่าพารามิเตอร์รายงานที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="5b981-106">For example, you may have viewed the report using a specific set of report parameter values.</span></span> <span data-ttu-id="5b981-107">คุณจะย่อส่วนข้อมูลนี้ใน URL โดยใช้พารามิเตอร์การเข้าถึง URL ที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="5b981-107">You encapsulate this information in the URL by using predefined URL access parameters.</span></span> <span data-ttu-id="5b981-108">คุณสามารถปรับแต่งวิธีการที่ Power BI ประมวลผลรายงานเพิ่มเติมได้ โดยการฝังพารามิเตอร์สำหรับรูปแบบการแสดงผล หรือสำหรับลักษณะที่แสดงกของแถบเครื่องมือรายงาน</span><span class="sxs-lookup"><span data-stu-id="5b981-108">You further customize how Power BI processes the report by embedding parameters for rendering formats, or for the look and feel of the report toolbar.</span></span> <span data-ttu-id="5b981-109">จากนั้นคุณสามารถวาง URL นี้ลงในอีเมลหรือหน้าเว็บโดยตร งเพื่อให้ผู้อื่นสามารถดูรายงานของคุณในลักษณะเดียวกันกับในเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="5b981-109">You then paste this URL directly into an email or Web page so others experience your report in the same manner in the browser.</span></span> 

<span data-ttu-id="5b981-110">ต่อไปนี้คือการดำเนินการที่คุณสามารถดำเนินการผ่านพารามิเตอร์การเข้าถึง URL:</span><span class="sxs-lookup"><span data-stu-id="5b981-110">Here are actions you can perform through URL access parameters:</span></span> 

- <span data-ttu-id="5b981-111">ส่งพารามิเตอร์รายงานไปยังรายงาน</span><span class="sxs-lookup"><span data-stu-id="5b981-111">Send report parameters to a report.</span></span> 
- <span data-ttu-id="5b981-112">เริ่มต้นการส่งออกเนื้อหารายงานในรูปแบบไฟล์ที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="5b981-112">Initiate the export of the report content in a supported file format.</span></span> 
- <span data-ttu-id="5b981-113">ซ่อนหรือดูบานหน้าต่างพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="5b981-113">Hide or view the parameters pane.</span></span> 
- <span data-ttu-id="5b981-114">ระบุการตั้งค่า DeviceInfo</span><span class="sxs-lookup"><span data-stu-id="5b981-114">Specify DeviceInfo setting.</span></span> 

<span data-ttu-id="5b981-115">สำหรับรายการทั้งหมดของคำสั่งและการตั้งค่าที่พร้อมใช้งานผ่านการเข้าถึง URL โปรดดูที่  [การอ้างอิงพารามิเตอร์การเข้าถึง URL](#url-access-parameter-reference) ภายหลังในบทความนี้</span><span class="sxs-lookup"><span data-stu-id="5b981-115">For the complete list of commands and settings available through URL access, see [URL access parameter reference](#url-access-parameter-reference) later in this article.</span></span> 

## <a name="url-access-concepts"></a><span data-ttu-id="5b981-116">แนวคิดการเข้าถึง URL</span><span class="sxs-lookup"><span data-stu-id="5b981-116">URL access concepts</span></span> 

<span data-ttu-id="5b981-117">คำขอ URL ไปยัง Power BI ประกอบด้วยพารามิเตอร์ที่ได้รับการประมวลผลโดยบริการ</span><span class="sxs-lookup"><span data-stu-id="5b981-117">URL requests to Power BI contain parameters that are processed by the service.</span></span> <span data-ttu-id="5b981-118">วิธีที่บริการจัดการกับคำขอ URL ขึ้นอยู่กับพารามิเตอร์ คำนำหน้าพารามิเตอร์ และประเภทของรายการที่รวมอยู่ใน URL</span><span class="sxs-lookup"><span data-stu-id="5b981-118">The way in which the service handles URL requests depends on the parameters, parameter prefixes, and types of items that are included in the URL.</span></span> <span data-ttu-id="5b981-119">ฟังก์ชัน URL ของรายงานที่มีการแบ่งหน้าเข้ากันได้กับเบราว์เซอร์และแอปพลิเคชันส่วนใหญ่ที่รองรับการจัดการ URL มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="5b981-119">Paginated report URL functionality is compatible with most browsers and applications that support standard URL addressing.</span></span> 

## <a name="url-access-syntax"></a><span data-ttu-id="5b981-120">ไวยากรณ์การเข้าถึง URL</span><span class="sxs-lookup"><span data-stu-id="5b981-120">URL access syntax</span></span> 

<span data-ttu-id="5b981-121">คำขอ URL อาจมีหลายพารามิเตอร์ที่แสดงอยู่ในลำดับใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="5b981-121">URL requests can contain multiple parameters, listed in any order.</span></span> <span data-ttu-id="5b981-122">พารามิเตอร์คิวรีจะต้องแยกด้วยเครื่องหมาย (&)</span><span class="sxs-lookup"><span data-stu-id="5b981-122">Parameters are separated by an ampersand (&).</span></span> <span data-ttu-id="5b981-123">คู่ชื่อและค่าจะต้องคั่นด้วยเครื่องหมายเท่ากับ (=)</span><span class="sxs-lookup"><span data-stu-id="5b981-123">Name and value pairs are separated by an equal sign (=).</span></span> <span data-ttu-id="5b981-124">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="5b981-124">For example:</span></span>

```
powerbiserviceurl?rp:parametervalueh&rdl:parameter=value  
```

## <a name="syntax-description"></a><span data-ttu-id="5b981-125">คำอธิบายไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="5b981-125">Syntax description</span></span> 

### <a name="powerbiserviceurl"></a><span data-ttu-id="5b981-126">powerbiserviceurl</span><span class="sxs-lookup"><span data-stu-id="5b981-126">powerbiserviceurl</span></span> 

<span data-ttu-id="5b981-127">URL บริการบนเว็บของผู้เช่า Power BI</span><span class="sxs-lookup"><span data-stu-id="5b981-127">The Web service URL of your Power BI tenant.</span></span> <span data-ttu-id="5b981-128">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="5b981-128">For example:</span></span> 

<span data-ttu-id="5b981-129">**&** ใช้เพื่อแยกคู่ชื่อและค่าของพารามิเตอร์การเข้าถึง URL</span><span class="sxs-lookup"><span data-stu-id="5b981-129">**&** Used to separate name and value pairs of URL access parameters.</span></span>

<span data-ttu-id="5b981-130">**คำนำหน้า** คำนำหน้าสำหรับพารามิเตอร์ URL (ตัวอย่างเช่น rp: หรือ rdl) ที่ระบุการดำเนินการในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="5b981-130">**prefix** A prefix for the URL parameter (for example, rp: or rdl:) that specifies an action in the Power BI service.</span></span> 

> [!NOTE]
> <span data-ttu-id="5b981-131">พารามิเตอร์รายงานจำเป็นต้องใช้คำนำหน้าพารามิเตอร์และตรงตามตัวพิมพ์ใหญ่-เล็ก</span><span class="sxs-lookup"><span data-stu-id="5b981-131">Report parameters require a parameter prefix and are case-sensitive.</span></span> 

<span data-ttu-id="5b981-132">**พารามิเตอร์** ชื่อพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="5b981-132">**parameter** The parameter name.</span></span> 

### <a name="value"></a><span data-ttu-id="5b981-133">ค่า</span><span class="sxs-lookup"><span data-stu-id="5b981-133">value</span></span> 

<span data-ttu-id="5b981-134">ข้อความ URL ที่สอดคล้องกับค่าของพารามิเตอร์ที่ใช้</span><span class="sxs-lookup"><span data-stu-id="5b981-134">URL text corresponding to the value of the parameter being used.</span></span> 

<span data-ttu-id="5b981-135">สำหรับตัวอย่างของการส่งพารามิเตอร์รายงานบน URL ให้ดู  [ส่งพารามิเตอร์รายงานใน URL](report-builder-url-pass-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="5b981-135">For examples of passing report parameters on the URL, see [Pass a report parameter in a URL](report-builder-url-pass-parameters.md).</span></span>

## <a name="url-access-parameter-reference"></a><span data-ttu-id="5b981-136">การอ้างอิงพารามิเตอร์การเข้าถึง URL</span><span class="sxs-lookup"><span data-stu-id="5b981-136">URL access parameter reference</span></span>

<span data-ttu-id="5b981-137">คุณสามารถใช้พารามิเตอร์ต่อไปนี้เป็นส่วนหนึ่งของ URL เพื่อกำหนดค่าลักษณะที่แสดงของรายงานที่มีการแบ่งหน้าใน Power BI</span><span class="sxs-lookup"><span data-stu-id="5b981-137">You can use the following parameters as part of a URL to configure the look and feel of your paginated reports in Power BI.</span></span> <span data-ttu-id="5b981-138">พารามิเตอร์ทั่วไปส่วนใหญ่จะแสดงอยู่ในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="5b981-138">The most common parameters are listed in this section.</span></span> <span data-ttu-id="5b981-139">พารามิเตอร์ต้องตรงตามตัวพิมพ์ใหญ่-เล็กและเริ่มต้นด้วยคำนำหน้าพารามิเตอร์ `rdl:` ถ้าเกี่ยวข้องกับรูปแบบเอาต์พุต</span><span class="sxs-lookup"><span data-stu-id="5b981-139">Parameters are case-insensitive and begin with the parameter prefix `rdl:` if related to the output format.</span></span>  

### <a name="report-commands-rdl"></a><span data-ttu-id="5b981-140">คำสั่งรายงาน (`rdl:`)</span><span class="sxs-lookup"><span data-stu-id="5b981-140">Report commands (`rdl:`)</span></span> 

<span data-ttu-id="5b981-141">**รูปแบบการส่งออก** ระบุรูปแบบที่จะแสดงและส่งออกรายงาน</span><span class="sxs-lookup"><span data-stu-id="5b981-141">**Export format** Specifies the format in which to render and export a report.</span></span>

<span data-ttu-id="5b981-142">ตัวอย่าง: rdl:format=PDF</span><span class="sxs-lookup"><span data-stu-id="5b981-142">Example: rdl:format=PDF</span></span>

<span data-ttu-id="5b981-143">ค่าที่ใช้ได้คือ:</span><span class="sxs-lookup"><span data-stu-id="5b981-143">Available values are:</span></span>
 
- <span data-ttu-id="5b981-144">PPTX (PowerPoint)</span><span class="sxs-lookup"><span data-stu-id="5b981-144">PPTX (PowerPoint)</span></span>
- <span data-ttu-id="5b981-145">MHTML</span><span class="sxs-lookup"><span data-stu-id="5b981-145">MHTML</span></span> 
- <span data-ttu-id="5b981-146">รูปภาพ</span><span class="sxs-lookup"><span data-stu-id="5b981-146">IMAGE</span></span> 
- <span data-ttu-id="5b981-147">EXCELOPENXML (EXCEL)</span><span class="sxs-lookup"><span data-stu-id="5b981-147">EXCELOPENXML (EXCEL)</span></span> 
- <span data-ttu-id="5b981-148">WORDOPENXML (WORD)</span><span class="sxs-lookup"><span data-stu-id="5b981-148">WORDOPENXML (WORD)</span></span> 
- <span data-ttu-id="5b981-149">CSV</span><span class="sxs-lookup"><span data-stu-id="5b981-149">CSV</span></span> 
- <span data-ttu-id="5b981-150">PDF</span><span class="sxs-lookup"><span data-stu-id="5b981-150">PDF</span></span> 
- <span data-ttu-id="5b981-151">ACCESSIBLEPDF (PDF)</span><span class="sxs-lookup"><span data-stu-id="5b981-151">ACCESSIBLEPDF (PDF)</span></span>
- <span data-ttu-id="5b981-152">XML</span><span class="sxs-lookup"><span data-stu-id="5b981-152">XML</span></span> 

<span data-ttu-id="5b981-153">**มุมมองรายงาน** ระบุชนิดของมุมมองที่ใช้เพื่อแสดงรายงาน</span><span class="sxs-lookup"><span data-stu-id="5b981-153">**Report View** Specifies the type of view use to displayed the report.</span></span>

-   <span data-ttu-id="5b981-154">rdl:reportView</span><span class="sxs-lookup"><span data-stu-id="5b981-154">rdl:reportView</span></span>

    - <span data-ttu-id="5b981-155">'interactive' (ค่าเริ่มต้น): โหลดรายงานในโหมดโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="5b981-155">'interactive' (default): load the report in interactive mode.</span></span>
    - <span data-ttu-id="5b981-156">'pageView': โหลดรายงานในโหมดมุมมองเพจ</span><span class="sxs-lookup"><span data-stu-id="5b981-156">'pageView': load the report in page view mode.</span></span>

<span data-ttu-id="5b981-157">**แผงพารามิเตอร์** จะแสดงให้คุณเห็นว่าแผงพารามิเตอร์นั้นปิดหรือเปิดอยู่เมื่อโหลดรายงาน หรือว่าซ่อนเอาไว้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5b981-157">**Parameter panel** Specifies whether the parameter panel is closed or open when the report loads, or is hidden altogether.</span></span>

-   <span data-ttu-id="5b981-158">rdl:parameterPanel</span><span class="sxs-lookup"><span data-stu-id="5b981-158">rdl:parameterPanel</span></span>

    - <span data-ttu-id="5b981-159">'ยุบ': โหลดรายงานโดยปิดแผงพารามิเตอร์ไว้</span><span class="sxs-lookup"><span data-stu-id="5b981-159">'collapsed': load the report with parameter panel closed.</span></span> <span data-ttu-id="5b981-160">ปุ่มพารามิเตอร์จะแสดงขึ้นเพื่อให้ผู้ใช้สามารถคลิกปุ่มเพื่อขยายพารามิเตอร์ได้</span><span class="sxs-lookup"><span data-stu-id="5b981-160">The parameter button is enabled so that users can click the button to expand;</span></span>
    - <span data-ttu-id="5b981-161">'ซ่อน': โหลดรายงานโดยปิดแผงพารามิเตอร์ไว้และปิดใช้งานปุ่มพารามิเตอร์ด้วย</span><span class="sxs-lookup"><span data-stu-id="5b981-161">'hidden': load the report with parameter panel closed and the parameter button disabled;</span></span>
    - <span data-ttu-id="5b981-162">'ขยาย': โหลดรายงานโดยเปิดแผงพารามิเตอร์ไว้และเปิดใช้งานปุ่มพารามิเตอร์ด้วย</span><span class="sxs-lookup"><span data-stu-id="5b981-162">'expanded' (default): load the report with parameter panel open and the parameter button enabled;</span></span>

<span data-ttu-id="5b981-163">**Device Info (ข้อมูลอุปกรณ์)** คุณอาจระบุพารามิเตอร์ผลลัพธ์เพิ่มเติมที่เฉพาะเจาะจงสำหรับรูปแบบการส่งออกต่อไปนี้ได้</span><span class="sxs-lookup"><span data-stu-id="5b981-163">**Device Info** You may specify additional output parameters for the following export formats.</span></span> 

<span data-ttu-id="5b981-164">PDF / ACCESSIBLEPDF:</span><span class="sxs-lookup"><span data-stu-id="5b981-164">PDF / ACCESSIBLEPDF:</span></span>

- <span data-ttu-id="5b981-165">rdl:AccessiblePDF=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-165">rdl:AccessiblePDF=true/false</span></span>
- <span data-ttu-id="5b981-166">rdl:Columns=integer</span><span class="sxs-lookup"><span data-stu-id="5b981-166">rdl:Columns=integer</span></span>
- <span data-ttu-id="5b981-167">rdl:ColumnSpacing=decimal(in)</span><span class="sxs-lookup"><span data-stu-id="5b981-167">rdl:ColumnSpacing=decimal(in)</span></span>
- <span data-ttu-id="5b981-168">rdl:DpiX=integer</span><span class="sxs-lookup"><span data-stu-id="5b981-168">rdl:DpiX=integer</span></span>
- <span data-ttu-id="5b981-169">rdl:DpiY=integer</span><span class="sxs-lookup"><span data-stu-id="5b981-169">rdl:DpiY=integer</span></span>
- <span data-ttu-id="5b981-170">rdl:EndPage=integer</span><span class="sxs-lookup"><span data-stu-id="5b981-170">rdl:EndPage=integer</span></span>
- <span data-ttu-id="5b981-171">rdl:HumanReadablePDF=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-171">rdl:HumanReadablePDF=true/false</span></span>
- <span data-ttu-id="5b981-172">rdl:MarginBottom=decimal(in)</span><span class="sxs-lookup"><span data-stu-id="5b981-172">rdl:MarginBottom=decimal(in)</span></span>
- <span data-ttu-id="5b981-173">rdl:MarginLeft=decimal(in)</span><span class="sxs-lookup"><span data-stu-id="5b981-173">rdl:MarginLeft=decimal(in)</span></span>
- <span data-ttu-id="5b981-174">rdl:MarginRight=decimal(in)</span><span class="sxs-lookup"><span data-stu-id="5b981-174">rdl:MarginRight=decimal(in)</span></span>
- <span data-ttu-id="5b981-175">rdl:MarginTop=decimal(in)</span><span class="sxs-lookup"><span data-stu-id="5b981-175">rdl:MarginTop=decimal(in)</span></span>
- <span data-ttu-id="5b981-176">rdl:PageHeight=decimal(in)</span><span class="sxs-lookup"><span data-stu-id="5b981-176">rdl:PageHeight=decimal(in)</span></span>
- <span data-ttu-id="5b981-177">rdl:PageWidth=decimal(in)</span><span class="sxs-lookup"><span data-stu-id="5b981-177">rdl:PageWidth=decimal(in)</span></span>
    - <span data-ttu-id="5b981-178">rdl:StartPage=integer</span><span class="sxs-lookup"><span data-stu-id="5b981-178">rdl:StartPage=integer</span></span>
    
<span data-ttu-id="5b981-179">CSV:</span><span class="sxs-lookup"><span data-stu-id="5b981-179">CSV:</span></span>

- <span data-ttu-id="5b981-180">rdl:Encoding=string</span><span class="sxs-lookup"><span data-stu-id="5b981-180">rdl:Encoding=string</span></span>
- <span data-ttu-id="5b981-181">rdl:ExcelMode=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-181">rdl:ExcelMode=true/false</span></span>
- <span data-ttu-id="5b981-182">rdl:FieldDelimiter=string</span><span class="sxs-lookup"><span data-stu-id="5b981-182">rdl:FieldDelimiter=string</span></span>
- <span data-ttu-id="5b981-183">rdl:NoHeader=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-183">rdl:NoHeader=true/false</span></span>
- <span data-ttu-id="5b981-184">rdl:Qualifier=string</span><span class="sxs-lookup"><span data-stu-id="5b981-184">rdl:Qualifier=string</span></span>
- <span data-ttu-id="5b981-185">rdl:RecordDelimiter=string</span><span class="sxs-lookup"><span data-stu-id="5b981-185">rdl:RecordDelimiter=string</span></span>
- <span data-ttu-id="5b981-186">rdl:SuppressLineBreaks=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-186">rdl:SuppressLineBreaks=true/false</span></span>
    - <span data-ttu-id="5b981-187">rdl:UseFormattedValues=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-187">rdl:UseFormattedValues=true/false</span></span>
    
<span data-ttu-id="5b981-188">WORDOPENXML (WORD):</span><span class="sxs-lookup"><span data-stu-id="5b981-188">WORDOPENXML (WORD):</span></span>

- <span data-ttu-id="5b981-189">rdl:AutoFit=string -> True/False/Never/Default</span><span class="sxs-lookup"><span data-stu-id="5b981-189">rdl:AutoFit=string -> True/False/Never/Default</span></span>
- <span data-ttu-id="5b981-190">rdl:ExpandToggles=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-190">rdl:ExpandToggles=true/false</span></span>
- <span data-ttu-id="5b981-191">rdl:FixedPageWidth=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-191">rdl:FixedPageWidth=true/false</span></span>
- <span data-ttu-id="5b981-192">rdl:OmitHyperlinks=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-192">rdl:OmitHyperlinks=true/false</span></span>
- <span data-ttu-id="5b981-193">rdl:OmitDrillthroughs=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-193">rdl:OmitDrillthroughs=true/false</span></span>

<span data-ttu-id="5b981-194">EXCELOPENXML (EXCEL):</span><span class="sxs-lookup"><span data-stu-id="5b981-194">EXCELOPENXML (EXCEL):</span></span>

- <span data-ttu-id="5b981-195">rdl:OmitDocumentMap=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-195">rdl:OmitDocumentMap=true/false</span></span>
- <span data-ttu-id="5b981-196">rdl:OmitFormulas=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-196">rdl:OmitFormulas=true/false</span></span>
    - <span data-ttu-id="5b981-197">rdl:SimplePageHeaders=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-197">rdl:SimplePageHeaders=true/false</span></span>
    
<span data-ttu-id="5b981-198">PPTX (PowerPoint):</span><span class="sxs-lookup"><span data-stu-id="5b981-198">PPTX (PowerPoint):</span></span>
 
- <span data-ttu-id="5b981-199">rdl:Columns=integer</span><span class="sxs-lookup"><span data-stu-id="5b981-199">rdl:Columns=integer</span></span>
- <span data-ttu-id="5b981-200">rdl:ColumnSpacing=decimal(in)</span><span class="sxs-lookup"><span data-stu-id="5b981-200">rdl:ColumnSpacing=decimal(in)</span></span>
- <span data-ttu-id="5b981-201">rdl:DpiX=integer</span><span class="sxs-lookup"><span data-stu-id="5b981-201">rdl:DpiX=integer</span></span>
- <span data-ttu-id="5b981-202">rdl:DpiY=integer</span><span class="sxs-lookup"><span data-stu-id="5b981-202">rdl:DpiY=integer</span></span>
- <span data-ttu-id="5b981-203">rdl:EndPage=integer</span><span class="sxs-lookup"><span data-stu-id="5b981-203">rdl:EndPage=integer</span></span>
- <span data-ttu-id="5b981-204">rdl:MarginBottom=decimal(in)</span><span class="sxs-lookup"><span data-stu-id="5b981-204">rdl:MarginBottom=decimal(in)</span></span>
- <span data-ttu-id="5b981-205">rdl:MarginLeft=decimal(in)</span><span class="sxs-lookup"><span data-stu-id="5b981-205">rdl:MarginLeft=decimal(in)</span></span>
- <span data-ttu-id="5b981-206">rdl:MarginRight=decimal(in)</span><span class="sxs-lookup"><span data-stu-id="5b981-206">rdl:MarginRight=decimal(in)</span></span>
- <span data-ttu-id="5b981-207">rdl:MarginTop=decimal(in)</span><span class="sxs-lookup"><span data-stu-id="5b981-207">rdl:MarginTop=decimal(in)</span></span>
- <span data-ttu-id="5b981-208">rdl:PageHeight=decimal(in)</span><span class="sxs-lookup"><span data-stu-id="5b981-208">rdl:PageHeight=decimal(in)</span></span>
- <span data-ttu-id="5b981-209">rdl:PageWidth=decimal(in)</span><span class="sxs-lookup"><span data-stu-id="5b981-209">rdl:PageWidth=decimal(in)</span></span>
- <span data-ttu-id="5b981-210">rdl:StartPage=integer</span><span class="sxs-lookup"><span data-stu-id="5b981-210">rdl:StartPage=integer</span></span>
    - <span data-ttu-id="5b981-211">rdl:UseReportPageSize=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-211">rdl:UseReportPageSize=true/false</span></span>

<span data-ttu-id="5b981-212">XML:</span><span class="sxs-lookup"><span data-stu-id="5b981-212">XML:</span></span>

- <span data-ttu-id="5b981-213">rdl:UseFormattedValues=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-213">rdl:UseFormattedValues=true/false</span></span>
- <span data-ttu-id="5b981-214">rdl:Indented=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-214">rdl:Indented=true/false</span></span>
- <span data-ttu-id="5b981-215">rdl:OmitNamespace=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-215">rdl:OmitNamespace=true/false</span></span>
- <span data-ttu-id="5b981-216">rdl:OmitSchema=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-216">rdl:OmitSchema=true/false</span></span>
- <span data-ttu-id="5b981-217">rdl:Encoding=string</span><span class="sxs-lookup"><span data-stu-id="5b981-217">rdl:Encoding=string</span></span>
- <span data-ttu-id="5b981-218">rdl:Schema=true/false</span><span class="sxs-lookup"><span data-stu-id="5b981-218">rdl:Schema=true/false</span></span>

<span data-ttu-id="5b981-219">**เปิดการเชื่อมโยงหลายมิติในหน้าต่างเบราว์เซอร์เดียวกัน** คุณสามารถผนวก 'rdl:targetSameWindow=true' ไปยัง URL การเชื่อมโยงหลายมิติในรายงานของคุณเพื่อทำให้ Power BI เปิดการเชื่อมโยงหลายมิตินี้ในหน้าต่างเบราว์เซอร์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="5b981-219">**Open hyperlink in same browser window** You can append 'rdl:targetSameWindow=true' to the hyperlink URL in your report to make Power BI to open this hyperlink in the same browser window.</span></span> <span data-ttu-id="5b981-220">สำหรับข้อมูลเกี่ยวกับการเพิ่มการเชื่อมโยงหลายมิติไปยังรายงาน ให้ดู [เพิ่มการเชื่อมโยงหลายมิติไปยัง URL](/sql/reporting-services/report-design/add-a-hyperlink-to-a-url-report-builder-and-ssrs) ในเอกสาร SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="5b981-220">For information on adding hyperlinks to a report, see [Add a hyperlink to a URL](/sql/reporting-services/report-design/add-a-hyperlink-to-a-url-report-builder-and-ssrs) in the SQL Server Reporting Services documentation.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5b981-221">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="5b981-221">Next steps</span></span>

- [<span data-ttu-id="5b981-222">ส่งพารามิเตอร์รายงานใน URL สำหรับรายงานที่มีการแบ่งหน้าใน Power BI</span><span class="sxs-lookup"><span data-stu-id="5b981-222">Pass a report parameter in a URL for a paginated report in Power BI</span></span>](report-builder-url-pass-parameters.md)
- [<span data-ttu-id="5b981-223">รายงานแบบแบ่งหน้าใน Power BI Premium คืออะไร</span><span class="sxs-lookup"><span data-stu-id="5b981-223">What are paginated reports in Power BI Premium?</span></span>](paginated-reports-report-builder-power-bi.md)
