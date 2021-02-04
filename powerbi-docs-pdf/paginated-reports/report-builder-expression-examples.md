---
title: ตัวอย่างนิพจน์ในตัวสร้างรายงานใน Power BI
description: นิพจน์จะถูกนำมาใช้บ่อยในตัวสร้างรายงานที่มีการแบ่งหน้าของ Power BI เพื่อควบคุมเนื้อหาและลักษณะที่ปรากฏของรายงาน
author: maggiesMSFT
ms.author: maggies
ms.date: 11/08/2020
ms.service: powerbi
ms.subservice: report-builder
ms.topic: conceptual
ms.assetid: 87ddb651-a1d0-4a42-8ea9-04dea3f6afa4
ms.openlocfilehash: a919efad0b9656327a766986456c533242d40c2e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96416335"
---
# <a name="expression-examples-in-power-bi-report-builder"></a><span data-ttu-id="aaddb-103">ตัวอย่างนิพจน์ในตัวสร้างรายงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="aaddb-103">Expression examples in Power BI Report Builder</span></span>

<span data-ttu-id="aaddb-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span><span class="sxs-lookup"><span data-stu-id="aaddb-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span></span> 

<span data-ttu-id="aaddb-105">นิพจน์จะถูกนำมาใช้บ่อยในตัวสร้างรายงานที่มีการแบ่งหน้าของ Power BI เพื่อควบคุมเนื้อหาและลักษณะที่ปรากฏของรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-105">Expressions are used frequently in Power BI Report Builder paginated reports to control content and report appearance.</span></span> <span data-ttu-id="aaddb-106">นิพจน์จะถูกเขียนขึ้นใน Microsoft Visual Basic และสามารถใช้ฟังก์ชันที่มีอยู่ในตัว รหัสที่กำหนดเอง รายงานและตัวแปรของกลุ่ม รวมถึงตัวแปรที่ผู้ใช้กำหนด</span><span class="sxs-lookup"><span data-stu-id="aaddb-106">Expressions are written in Microsoft Visual Basic, and can use built-in functions, custom code, report and group variables, and user-defined variables.</span></span> <span data-ttu-id="aaddb-107">นิพจน์เริ่มต้นด้วยเครื่องหมายเท่ากับ (=)</span><span class="sxs-lookup"><span data-stu-id="aaddb-107">Expressions begin with an equal sign (=).</span></span>   

<span data-ttu-id="aaddb-108">หัวข้อนี้ให้ตัวอย่างของนิพจน์ที่สามารถนำมาใช้ได้สำหรับงานทั่วไปในรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-108">This topic provides examples of expressions that can be used for common tasks in a report.</span></span>  
  
-   <span data-ttu-id="aaddb-109">[ฟังก์ชัน Visual Basic](#VisualBasicFunctions) ตัวอย่างสำหรับวันที่ สตริง การแปลงและฟังก์ชัน Visual Basic ที่เป็นเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="aaddb-109">[Visual Basic Functions](#VisualBasicFunctions) Examples for date, string, conversion and conditional Visual Basic functions.</span></span>  
  
-   <span data-ttu-id="aaddb-110">[ฟังก์ชันรายงาน](#ReportFunctions) ตัวอย่างสำหรับค่ารวมและฟังก์ชันรายงานที่มีอยู่ในตัวอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="aaddb-110">[Report Functions](#ReportFunctions) Examples for aggregates and other built-in report functions.</span></span>  
  
-   <span data-ttu-id="aaddb-111">[ลักษณะที่ปรากฏของข้อมูลรายงาน](#AppearanceofReportData) ตัวอย่างสำหรับการเปลี่ยนลักษณะที่ปรากฏของรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-111">[Appearance of Report Data](#AppearanceofReportData) Examples for changing the appearance of a report.</span></span>  
  
-   <span data-ttu-id="aaddb-112">[คุณสมบัติ](#Properties) ตัวอย่างสำหรับการตั้งค่าคุณสมบัติหน่วยข้อมูลของรายงานในรูปแบบการควบคุมหรือการมองเห็น</span><span class="sxs-lookup"><span data-stu-id="aaddb-112">[Properties](#Properties) Examples for setting report item properties to control format or visibility.</span></span>  
  
-   <span data-ttu-id="aaddb-113">[พารามิเตอร์](#Parameters) ตัวอย่างสำหรับการใช้พารามิเตอร์ในนิพจน์</span><span class="sxs-lookup"><span data-stu-id="aaddb-113">[Parameters](#Parameters) Examples for using parameters in an expression.</span></span>  
  
-   <span data-ttu-id="aaddb-114">[รหัสที่กำหนดเอง](#CustomCode) ตัวอย่างรหัสที่กำหนดเองแบบฝังตัว</span><span class="sxs-lookup"><span data-stu-id="aaddb-114">[Custom Code](#CustomCode) Examples of embedded custom code.</span></span>  
  
<span data-ttu-id="aaddb-115">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับนิพจน์แบบธรรมดาและแบบซับซ้อนที่คุณสามาถใช้นิพจน์ได้ และชนิดการอ้างอิงที่คุณสามารถรวมอยู่ในนิพจน์ได้ ดูที่หัวข้อภายใต้[นิพจน์ในตัวสร้างรายงานของ Power BI](report-builder-expressions.md)</span><span class="sxs-lookup"><span data-stu-id="aaddb-115">For more information about simple and complex expressions, where you can use expressions, and the types of references that you can include in an expression, see topics under [Expressions in Power BI Report Builder](report-builder-expressions.md).</span></span> 
  
## <a name="functions"></a><span data-ttu-id="aaddb-116">ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="aaddb-116">Functions</span></span>  
 <span data-ttu-id="aaddb-117">นิพจน์หลายตัวในรายงานมีฟังก์ชันต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="aaddb-117">Many expressions in a report contain functions.</span></span> <span data-ttu-id="aaddb-118">คุณสามารถจัดรูปแบบข้อมูล นำตรรกะไปใช้และเข้าถึงรายงานเมตาดาต้าได้โดยการใช้ฟังก์ชันเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="aaddb-118">You can format data, apply logic, and access report metadata using these functions.</span></span> <span data-ttu-id="aaddb-119">คุณสามารถเขียนนิพจน์ที่ใช้ฟังก์ชันจากไลบรารีเวลาเรียกใช้งานของ Microsoft Visual Basic และจาก `xref:System.Convert` และ `xref:System.Math` Namespace ได้</span><span class="sxs-lookup"><span data-stu-id="aaddb-119">You can write expressions that use functions from the Microsoft Visual Basic run-time library, and from the `xref:System.Convert` and `xref:System.Math` namespaces.</span></span> <span data-ttu-id="aaddb-120">คุณสามารถเพิ่มการอ้างอิงไปยังฟังก์ชันในรหัสที่กำหนดเองได้</span><span class="sxs-lookup"><span data-stu-id="aaddb-120">You can add references to functions in custom code.</span></span> <span data-ttu-id="aaddb-121">นอกจากนี้ คุณยังสามารถใช้คลาสจาก Microsoft.NET Framework รวมถึง`xref:System.Text.RegularExpressions`</span><span class="sxs-lookup"><span data-stu-id="aaddb-121">You can also use classes from the Microsoft .NET Framework, including `xref:System.Text.RegularExpressions`.</span></span>  
  
##  <a name="visual-basic-functions"></a><a name="VisualBasicFunctions"></a> <span data-ttu-id="aaddb-122">ฟังก์ชัน Visual Basic</span><span class="sxs-lookup"><span data-stu-id="aaddb-122">Visual Basic functions</span></span>  
 <span data-ttu-id="aaddb-123">คุณสามารถใช้ฟังก์ชัน Visual Basic เพื่อจัดการข้อมูลที่แสดงในกล่องข้อความหรือที่ใช้สำหรับพารามิเตอร์ คุณสมบัติหรือพื้นที่อื่นๆ ของรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-123">You can use Visual Basic functions to manipulate the data that is displayed in text boxes or that is used for parameters, properties, or other areas of the report.</span></span> <span data-ttu-id="aaddb-124">ส่วนนี้มีตัวอย่างที่แสดงให้เห็นถึงฟังก์ชันบางอย่างเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="aaddb-124">This section provides examples demonstrating some of these functions.</span></span> <span data-ttu-id="aaddb-125">สำหรับข้อมูลเพิ่มเติม ดูที่[ สมาชิกไลบรารีเวลาเรียกใช้งาน Visual Basic](/dotnet/visual-basic/language-reference/runtime-library-members) บน MSDN</span><span class="sxs-lookup"><span data-stu-id="aaddb-125">For more information, see [Visual Basic Runtime Library Members](/dotnet/visual-basic/language-reference/runtime-library-members) on MSDN.</span></span>  
  
 <span data-ttu-id="aaddb-126">.NET Framework มีตัวเลือกรูปแบบที่กำหนดเองหลากหลาย ตัวอย่างเช่น สำหรับรูปแบบวันที่ที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="aaddb-126">The .NET Framework provides many custom format options, for example, for specific date formats.</span></span> <span data-ttu-id="aaddb-127">สำหรับข้อมูลเพิ่มเติม ดูที่[ชนิดของการจัดรูปแบบ](/dotnet/standard/base-types/formatting-types)</span><span class="sxs-lookup"><span data-stu-id="aaddb-127">For more information, see [Formatting Types](/dotnet/standard/base-types/formatting-types).</span></span>  
  
### <a name="math-functions"></a><span data-ttu-id="aaddb-128">ฟังก์ชันทางคณิตศาสตร์</span><span class="sxs-lookup"><span data-stu-id="aaddb-128">Math functions</span></span>  
  
-   <span data-ttu-id="aaddb-129">ฟังก์ชัน **Round** มีประโยชน์ในการปัดตัวเลขเป็นจำนวนเต็มที่ใกล้เคียงที่สุด</span><span class="sxs-lookup"><span data-stu-id="aaddb-129">The **Round** function is useful to round numbers to the nearest integer.</span></span> <span data-ttu-id="aaddb-130">นิพจน์ต่อไปนี้ปัด 1.3 เป็น 1:</span><span class="sxs-lookup"><span data-stu-id="aaddb-130">The following expression rounds a 1.3 to 1:</span></span>  
  
    ```  
    = Round(1.3)  
    ```  
  
     <span data-ttu-id="aaddb-131">นอกจากนี้ คุณยังสามารถเขียนนิพจน์เพื่อปัดค่าเป็นผลคูณที่คุณระบุ คล้ายกับฟังก์ชัน **MRound** ใน Excel</span><span class="sxs-lookup"><span data-stu-id="aaddb-131">You can also write an expression to round a value to a multiple that you specify, similar to the **MRound** function in Excel.</span></span> <span data-ttu-id="aaddb-132">คูณค่าโดยใช้ตัวคูณที่สร้างจำนวนเต็ม ปัดตัวเลข และจากนั้นหารโดยใช้ตัวคูณตัวเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="aaddb-132">Multiply the value by a factor that creates an integer, round the number, and then divide by the same factor.</span></span> <span data-ttu-id="aaddb-133">ตัวอย่างเช่น ในการปัด 1.3 เป็นผลคูณที่ใกล้เคียงที่สุดของ 0.2 (1.4) ให้ใช้นิพจน์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="aaddb-133">For example, to round 1.3 to the nearest multiple of .2 (1.4), use the following expression:</span></span>  
  
    ```  
    = Round(1.3*5)/5  
    ```  
  
###  <a name="date-functions"></a><a name="DateFunctions"></a> <span data-ttu-id="aaddb-134">ฟังก์ชันวันที่</span><span class="sxs-lookup"><span data-stu-id="aaddb-134">Date functions</span></span>  
  
-   <span data-ttu-id="aaddb-135">ฟังก์ชัน **Today** มีวันที่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="aaddb-135">The **Today** function provides the current date.</span></span> <span data-ttu-id="aaddb-136">นิพจน์นี้สามารถนำไปใช้ในกล่องข้อความเพื่อแสดงวันที่ในรายงาน หรือในพารามิเตอร์เพื่อกรองข้อมูลตามวันที่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="aaddb-136">This expression can be used in a text box to display the date on the report, or in a parameter to filter data based on the current date.</span></span>  
  
    ```  
    =Today()  
    ```  
  
-   <span data-ttu-id="aaddb-137">ใช้ฟังก์ชัน **DateInterval** ในการดึงส่วนที่เฉพาะเจาะจงของวันที่ออก</span><span class="sxs-lookup"><span data-stu-id="aaddb-137">Use the **DateInterval** function to pull out a specific part of a date.</span></span> <span data-ttu-id="aaddb-138">ต่อไปนี้คือพารามิเตอร์ **DateInterval** ที่ถูกต้องบางตัว:</span><span class="sxs-lookup"><span data-stu-id="aaddb-138">Here are some valid **DateInterval** parameters:</span></span>

    -   <span data-ttu-id="aaddb-139">DateInterval.Second</span><span class="sxs-lookup"><span data-stu-id="aaddb-139">DateInterval.Second</span></span>
    -   <span data-ttu-id="aaddb-140">DateInterval.Minute</span><span class="sxs-lookup"><span data-stu-id="aaddb-140">DateInterval.Minute</span></span>
    -   <span data-ttu-id="aaddb-141">DateInterval.Hour</span><span class="sxs-lookup"><span data-stu-id="aaddb-141">DateInterval.Hour</span></span>
    -   <span data-ttu-id="aaddb-142">DateInterval.Weekday</span><span class="sxs-lookup"><span data-stu-id="aaddb-142">DateInterval.Weekday</span></span>
    -   <span data-ttu-id="aaddb-143">DateInterval.Day</span><span class="sxs-lookup"><span data-stu-id="aaddb-143">DateInterval.Day</span></span>
    -   <span data-ttu-id="aaddb-144">DateInterval.DayOfYear</span><span class="sxs-lookup"><span data-stu-id="aaddb-144">DateInterval.DayOfYear</span></span>
    -   <span data-ttu-id="aaddb-145">DateInterval.WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="aaddb-145">DateInterval.WeekOfYear</span></span>
    -   <span data-ttu-id="aaddb-146">DateInterval.Month</span><span class="sxs-lookup"><span data-stu-id="aaddb-146">DateInterval.Month</span></span>
    -   <span data-ttu-id="aaddb-147">DateInterval.Quarter</span><span class="sxs-lookup"><span data-stu-id="aaddb-147">DateInterval.Quarter</span></span>
    -   <span data-ttu-id="aaddb-148">DateInterval.Year</span><span class="sxs-lookup"><span data-stu-id="aaddb-148">DateInterval.Year</span></span>

    <span data-ttu-id="aaddb-149">ตัวอย่างเช่น นิพจน์นี้จะแสดงหมายเลขของสัปดาห์ในปีปัจจุบันสำหรับวันที่วันนี้:</span><span class="sxs-lookup"><span data-stu-id="aaddb-149">For example, this expression will show the number of the week in the current year for today's date:</span></span>
  
    ```  
    =DatePart(DateInterval.WeekOfYear, today()) 
    ```  
  
-   <span data-ttu-id="aaddb-150">ฟังก์ชัน **DateAdd** มีประโยชน์สำหรับการจัดช่วงข้อมูลวันที่ตามพารามิเตอร์เดี่ยว</span><span class="sxs-lookup"><span data-stu-id="aaddb-150">The **DateAdd** function is useful for supplying a range of dates based on a single parameter.</span></span> <span data-ttu-id="aaddb-151">นิพจน์ต่อไปนี้มีวันที่ระยะหกเดือนหลังวันที่จากพารามิเตอร์ที่ชื่อ *วันที่เริ่มต้น*</span><span class="sxs-lookup"><span data-stu-id="aaddb-151">The following expression provides a date that is six months after the date from a parameter named *StartDate*.</span></span>  
  
    ```  
    =DateAdd(DateInterval.Month, 6, Parameters!StartDate.Value)  
    ```  
  
-   <span data-ttu-id="aaddb-152">ฟังก์ชัน **Year** แสดงปีสำหรับวันที่ที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="aaddb-152">The **Year** function displays the year for a particular date.</span></span> <span data-ttu-id="aaddb-153">คุณสามารถใช้ฟังก์ชันนี้เพื่อจัดกลุ่มวันที่ร่วมกันหรือเพื่อแสดงปีตามป้ายชื่อสำหรับชุดวันที่</span><span class="sxs-lookup"><span data-stu-id="aaddb-153">You can use this to group dates together or to display the year as a label for a set of dates.</span></span> <span data-ttu-id="aaddb-154">นิพจน์นี้มี้ปีสำหรับกลุ่มที่ระบุไว้ของวันที่บนใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="aaddb-154">This expression provides the year for a given group of sales order dates.</span></span> <span data-ttu-id="aaddb-155">ฟังก์ชัน **Month** และฟังก์ชันอื่นๆ ยังสามารถนำมาใช้เพื่อจัดการวันที่ได้</span><span class="sxs-lookup"><span data-stu-id="aaddb-155">The **Month** function and other functions can also be used to manipulate dates.</span></span> <span data-ttu-id="aaddb-156">สำหรับข้อมูลเพิ่มเติม ดูที่คู่มือ Visual Basic</span><span class="sxs-lookup"><span data-stu-id="aaddb-156">For more information, see the Visual Basic documentation.</span></span>  
  
    ```  
    =Year(Fields!OrderDate.Value)  
    ```  
  
-   <span data-ttu-id="aaddb-157">คุณสามารถรวมฟังก์ชันในนิพจน์เพื่อกำหนดรูปแบบได้</span><span class="sxs-lookup"><span data-stu-id="aaddb-157">You can combine functions in an expression to customize the format.</span></span> <span data-ttu-id="aaddb-158">นิพจน์ต่อไปนี้จะเปลี่ยนแปลงรูปแบบของวันที่ในฟอร์มเดือน-วัน-ปี เป็นเดือน-สัปดาห์-หมายเลขสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="aaddb-158">The following expression changes the format of a date in the form month-day-year to month-week-week number.</span></span> <span data-ttu-id="aaddb-159">ตัวอย่างเช่น 12/23/2009 เป็นสัปดาห์ที่ 3 ของเดือนธันวาคม:</span><span class="sxs-lookup"><span data-stu-id="aaddb-159">For example, 12/23/2009 to December Week 3:</span></span>  
  
    ```  
    =Format(Fields!MyDate.Value, "MMMM") & " Week " &   
    (Int(DateDiff("d", DateSerial(Year(Fields!MyDate.Value),   
    Month(Fields!MyDate.Value),1), Fields!FullDateAlternateKey.Value)/7)+1).ToString  
    ```  
  
     <span data-ttu-id="aaddb-160">เมื่อนำมาใช้เป็นเขตข้อมูลจาการคำนวณในชุดข้อมูล คุณสามารถใช้นิพจน์นี้บนแผนภูมิเพื่อรวมค่าตามสัปดาห์ภายในแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="aaddb-160">When used as a calculated field in a dataset, you can use this expression on a chart to aggregate values by week within each month.</span></span>  
  
-   <span data-ttu-id="aaddb-161">นิพจน์ต่อไปนี้จัดรูปแบบค่า SellStartDate เป็น ดดด-ปป</span><span class="sxs-lookup"><span data-stu-id="aaddb-161">The following expression formats the SellStartDate value as MMM-YY.</span></span> <span data-ttu-id="aaddb-162">เขตข้อมูล SellStartDate เป็นชนิดข้อมูลวันที่เวลา</span><span class="sxs-lookup"><span data-stu-id="aaddb-162">SellStartDate field is a datetime data type.</span></span>  
  
    ```  
    =FORMAT(Fields!SellStartDate.Value, "MMM-yy")  
    ```  
  
-   <span data-ttu-id="aaddb-163">นิพจน์ต่อไปนี้จัดรูปแบบค่าของ SellStartDate เป็น วว/ดด/ปปปป</span><span class="sxs-lookup"><span data-stu-id="aaddb-163">The following expression formats the SellStartDate value as dd/MM/yyyy.</span></span> <span data-ttu-id="aaddb-164">เขตข้อมูล SellStartDate เป็นชนิดข้อมูลวันที่เวลา</span><span class="sxs-lookup"><span data-stu-id="aaddb-164">The SellStartDate field is a datetime data type.</span></span>  
  
    ```  
    =FORMAT(Fields!SellStartDate.Value, "dd/MM/yyyy")  
    ```  
  
-   <span data-ttu-id="aaddb-165">ฟังก์ชัน **CDate** แปลงค่าเป็นวันที่</span><span class="sxs-lookup"><span data-stu-id="aaddb-165">The **CDate** function converts the value to a date.</span></span> <span data-ttu-id="aaddb-166">ฟังก์ชัน **Now** คืนค่าวันที่ที่มีวันที่และเวลาในปัจจุบันบนระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="aaddb-166">The **Now** function returns a date value containing the current date and time according to your system.</span></span> <span data-ttu-id="aaddb-167">**DateDiff** คืนค่าระยะยาวโดยการระบุจำนวนช่วงเวลาระหว่างค่าวันที่ทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="aaddb-167">**DateDiff** returns a Long value specifying the number of time intervals between two Date values.</span></span>  
  
     <span data-ttu-id="aaddb-168">ตัวอย่างต่อไปนี้แสดงวันที่เริ่มต้นของปีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="aaddb-168">The following example displays the start date of the current year</span></span>  
  
    ```  
    =DateAdd(DateInterval.Year,DateDiff(DateInterval.Year,CDate("01/01/1900"),Now()),CDate("01/01/1900"))  
    ```  
  
-   <span data-ttu-id="aaddb-169">ตัวอย่างต่อไปนี้แสดงวันที่เริ่มต้นสำหรับเดือนก่อนหน้านี้ตามเดือนปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="aaddb-169">The following example displays the start date for the previous month based on the current month.</span></span>  
  
    ```  
    =DateAdd(DateInterval.Month,DateDiff(DateInterval.Month,CDate("01/01/1900"),Now())-1,CDate("01/01/1900"))  
    ```  
  
-   <span data-ttu-id="aaddb-170">ตัวอย่างต่อไปนี้สร้างช่วงปีระหว่าง SellStartDate และ LastReceiptDate</span><span class="sxs-lookup"><span data-stu-id="aaddb-170">The following expression generates the interval years between SellStartDate and LastReceiptDate.</span></span> <span data-ttu-id="aaddb-171">เขตข้อมูลเหล่านี้อยู่ในชุดข้อมูลอื่นสองชุดได้แก่ DataSet1 และ DataSet2</span><span class="sxs-lookup"><span data-stu-id="aaddb-171">These fields are in two different datasets, DataSet1 and DataSet2.</span></span>  
  
    ```  
    =DATEDIFF("yyyy", First(Fields!SellStartDate.Value, "DataSet1"), First(Fields!LastReceiptDate.Value, "DataSet2"))  
    ```  
  
-   <span data-ttu-id="aaddb-172">ฟังก์ชัน **DatePart** คืนค่าจำนวนเต็มที่มีคอมโพเนนต์ที่ระบุของค่าวันที่ที่กำหนดไว้ นิพจน์ต่อไปนี้คืนค่าปีสำหรับค่าแรกของ SellStartDate ใน DataSet1</span><span class="sxs-lookup"><span data-stu-id="aaddb-172">The **DatePart** function returns an Integer value containing the specified component of a given Date value.The following expression returns the year for the first value of the SellStartDate in DataSet1.</span></span> <span data-ttu-id="aaddb-173">มีระบุขอบเขตชุดข้อมูลเนื่องจากมีหลายชุดข้อมูลในรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-173">The dataset scope is specified because there are multiple datasets in the report.</span></span>  
  
    ```  
    =Datepart("yyyy", First(Fields!SellStartDate.Value, "DataSet1"))  
  
    ```  
  
-   <span data-ttu-id="aaddb-174">ฟังก์ชัน **DateSerial** คืนค่าวันที่โดยการแสดงปี เดือนและวันที่ระบุ พร้อมด้วยข้อมูลเวลาที่ตั้งค่าถึงเที่ยงคืน</span><span class="sxs-lookup"><span data-stu-id="aaddb-174">The **DateSerial** function returns a Date value representing a specified year, month, and day, with the time information set to midnight.</span></span> <span data-ttu-id="aaddb-175">ตัวอย่างต่อไปนี้แสดงวันที่สิ้นสุดสำหรับเดือนก่อนตามเดือนปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="aaddb-175">The following example displays the ending date for the prior month, based on the current month.</span></span>  
  
    ```  
    =DateSerial(Year(Now()), Month(Now()), "1").AddDays(-1)  
    ```  
  
-   <span data-ttu-id="aaddb-176">นิพจน์ต่อไปนี้แสดงวันที่ต่าง ๆ ตามค่าพารามิเตอร์วันที่ที่ผู้ใช้เลือก</span><span class="sxs-lookup"><span data-stu-id="aaddb-176">The following expressions display various dates based on a date parameter value selected by the user.</span></span>  
  
|<span data-ttu-id="aaddb-177">คำอธิบายตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="aaddb-177">Example Description</span></span>|<span data-ttu-id="aaddb-178">ตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="aaddb-178">Example</span></span>|  
|-------------------------|-------------|  
|<span data-ttu-id="aaddb-179">เมื่อวานนี้</span><span class="sxs-lookup"><span data-stu-id="aaddb-179">Yesterday</span></span>|`=DateSerial(Year(Parameters!TodaysDate.Value),Month(Parameters!TodaysDate.Value),Day(Parameters!TodaysDate.Value)-1)`|  
|<span data-ttu-id="aaddb-180">สองวันที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="aaddb-180">Two Days Ago</span></span>|`=DateSerial(Year(Parameters!TodaysDate.Value),Month(Parameters!TodaysDate.Value),Day(Parameters!TodaysDate.Value)-2)`|  
|<span data-ttu-id="aaddb-181">หนึ่งเดือนที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="aaddb-181">One Month Ago</span></span>|`=DateSerial(Year(Parameters!TodaysDate.Value),Month(Parameters!TodaysDate.Value)-1,Day(Parameters!TodaysDate.Value))`|  
|<span data-ttu-id="aaddb-182">สองเดือนที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="aaddb-182">Two Months Ago</span></span>|`=DateSerial(Year(Parameters!TodaysDate.Value),Month(Parameters!TodaysDate.Value)-2,Day(Parameters!TodaysDate.Value))`|  
|<span data-ttu-id="aaddb-183">หนึ่งปีที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="aaddb-183">One Year Ago</span></span>|`=DateSerial(Year(Parameters!TodaysDate.Value)-1,Month(Parameters!TodaysDate.Value),Day(Parameters!TodaysDate.Value))`|  
|<span data-ttu-id="aaddb-184">สองปีที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="aaddb-184">Two Years Ago</span></span>|`=DateSerial(Year(Parameters!TodaysDate.Value)-2,Month(Parameters!TodaysDate.Value),Day(Parameters!TodaysDate.Value))`|  
  
###  <a name="string-functions"></a><a name="StringFunctions"></a> <span data-ttu-id="aaddb-185">ฟังก์ชันสตริง</span><span class="sxs-lookup"><span data-stu-id="aaddb-185">String functions</span></span>  
  
-   <span data-ttu-id="aaddb-186">รวมเขตข้อมูลมากกว่าหนึ่งรายการโดยใช้ตัวดำเนินการเรียงต่อกันและค่าคงที่ของ Visual Basic</span><span class="sxs-lookup"><span data-stu-id="aaddb-186">Combine more than one field by using concatenation operators and Visual Basic constants.</span></span> <span data-ttu-id="aaddb-187">นิพจน์ต่อไปนี้คืนค่าสองเขตข้อมูล แต่ละเขตข้อมูลอยู่บนบรรทัดที่แยกออกจากกันในกล่องข้อความเดียวกัน:</span><span class="sxs-lookup"><span data-stu-id="aaddb-187">The following expression returns two fields, each on a separate line in the same text box:</span></span>  
  
    ```  
    =Fields!FirstName.Value & vbCrLf & Fields!LastName.Value   
    ```  
  
-   <span data-ttu-id="aaddb-188">จัดรูปแบบวันที่และหมายเลขในสตริงด้วยฟังก์ชัน **Format**</span><span class="sxs-lookup"><span data-stu-id="aaddb-188">Format dates and numbers in a string with the **Format** function.</span></span> <span data-ttu-id="aaddb-189">นิพจน์ต่อไปนี้แสดงค่าของพารามิเตอร์ *StartDate* และ *EndDate* ในรูปแบบวันที่ระยะยาว:</span><span class="sxs-lookup"><span data-stu-id="aaddb-189">The following expression displays values of the *StartDate* and *EndDate* parameters in long date format:</span></span>  
  
    ```  
    =Format(Parameters!StartDate.Value, "D") & " through " &  Format(Parameters!EndDate.Value, "D")    
    ```  
  
     <span data-ttu-id="aaddb-190">หากกล่องข้อความมีเพียงวันที่หรือหมายเลข คุณควรใช้คุณสมบัติจัดรูปแบบของกล่องข้อความเพื่อนำการจัดรูปแบบมาใช้แทนฟังก์ชัน **Format** ที่อยู่ภายในกล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="aaddb-190">If the text box contains only a date or number, you should use the Format property of the text box to apply formatting instead of the **Format** function within the text box.</span></span>  
  
-   <span data-ttu-id="aaddb-191">ฟังก์ชัน **Right**, **Len** และ **InStr** มีประโยชน์สำหรับการคืนสตริงย่อย ตัวอย่างเช่น การตัดแต่ง *DOMAIN*\\*ชื่อผู้ใช้* เป็นเพียงชื่อผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="aaddb-191">The **Right**, **Len**, and **InStr** functions are useful for returning a substring, for example, trimming *DOMAIN*\\*username* to just the user name.</span></span> <span data-ttu-id="aaddb-192">นิพจน์ต่อไปนี้คืนสตริงบางส่วนกลับไปเป็นเครื่องหมายทับด้านขวา (\\) อักขระจากพารามิเตอร์ที่มีชื่อ *ผู้ใช้*:</span><span class="sxs-lookup"><span data-stu-id="aaddb-192">The following expression returns the part of the string to the right of a backslash (\\) character from a parameter named *User*:</span></span>  
  
    ```  
    =Right(Parameters!User.Value, Len(Parameters!User.Value) - InStr(Parameters!User.Value, "\"))  
    ```  
  
     <span data-ttu-id="aaddb-193">นิพจน์ต่อไปนี้ให้ผลลัพธ์เป็นค่าเดียวกันกับค่าก่อนหน้านี้ โดยใช้สมาชิกคลาส .NET Framework `xref:System.String` แทนฟังก์ชัน Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="aaddb-193">The following expression results in the same value as the previous one, using members of the .NET Framework `xref:System.String` class instead of Visual Basic functions:</span></span>  
  
    ```  
    =Parameters!User.Value.Substring(Parameters!User.Value.IndexOf("\")+1, Parameters!User.Value.Length-Parameters!User.Value.IndexOf("\")-1)  
    ```  
  
-   <span data-ttu-id="aaddb-194">แสดงค่าที่เลือกจากพารามิเตอร์ที่มีหลายค่า</span><span class="sxs-lookup"><span data-stu-id="aaddb-194">Display the selected values from a multivalue parameter.</span></span> <span data-ttu-id="aaddb-195">นิพจน์ต่อไปนี้ใช้ฟังก์ชัน **Join** เพื่อเชื่อมค่าของพารามิเตอร์ *MySelection* ที่เลือกเข้าด้วยกันเป็นสตริงเดียวที่สามารถนำมาตั้งค่าเป็นนิพจน์สำหรับค่าของกล่องข้อความในหน่วยข้อมูลของรายงาน:</span><span class="sxs-lookup"><span data-stu-id="aaddb-195">The following example uses the **Join** function to concatenate the selected values of the parameter *MySelection* into a single string that can be set as an expression for the value of a text box in a report item:</span></span>  
  
    ```  
    = Join(Parameters!MySelection.Value)  
    ```  
  
     <span data-ttu-id="aaddb-196">ตัวอย่างต่อไปนี้เหมือนกับตัวอย่างข้างต้น อีกทั้งยังแสดงสตริงข้อความก่อนรายการของค่าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="aaddb-196">The following example does the same as the above example, as well as displays a text string prior to the list of selected values.</span></span>  
  
    ```  
    ="Report for " & JOIN(Parameters!MySelection.Value, " & ")  
  
    ```  
  
-   <span data-ttu-id="aaddb-197">ฟังก์ชัน **Regex** จาก .NET Framework `xref:System.Text.RegularExpressions` มีประโยชน์สำหรับการเปลี่ยนแปลงการจัดรูปแบบของสตริงที่มีอยู่ ตัวอย่างเช่น การจัดรูปแบบหมายเลขโทรศัพท์</span><span class="sxs-lookup"><span data-stu-id="aaddb-197">The **Regex** functions from the .NET Framework `xref:System.Text.RegularExpressions` are useful for changing the format of existing strings, for example, formatting a telephone number.</span></span> <span data-ttu-id="aaddb-198">นิพจน์ต่อไปนี้ใช้ฟังก์ชัน **Replace** ในการเปลี่ยนแปลงการจัดรูปแบบหมายเลขโทรศัพท์ 10 ตัวในเขตข้อมูลจาก "*nnn*-*nnn*-*nnnn*" เป็น "(*nnn*) *nnn*-*nnnn*":</span><span class="sxs-lookup"><span data-stu-id="aaddb-198">The following expression uses the **Replace** function to change the format of a ten-digit telephone number in a field from "*nnn*-*nnn*-*nnnn*" to "(*nnn*) *nnn*-*nnnn*":</span></span>  
  
    ```  
    =System.Text.RegularExpressions.Regex.Replace(Fields!Phone.Value, "(\d{3})[ -.]*(\d{3})[ -.]*(\d{4})", "($1) $2-$3")  
    ```  
  
    > [!NOTE]  
    >  <span data-ttu-id="aaddb-199">ครวจสอบว่าค่าของ Fields!Phone.Value ไม่มีพื้นที่เพิ่มเติมและเป็นชนิด `xref:System.String`</span><span class="sxs-lookup"><span data-stu-id="aaddb-199">Verify that the value for Fields!Phone.Value has no extra spaces and is of type `xref:System.String`.</span></span>  
  
### <a name="lookup"></a><span data-ttu-id="aaddb-200">ค้นหา</span><span class="sxs-lookup"><span data-stu-id="aaddb-200">Lookup</span></span>  
  
-   <span data-ttu-id="aaddb-201">คุณสามารถใช้ฟังก์ชัน **Lookup** เพื่อกู้คืนค่าจากชุดข้อมูลสำหรับความสัมพันธ์แบบหนึ่ง-ต่อ-หนึ่ง ตัวอย่างเช่น คู่ค่าหลัก โดยการระบุเขตข้อมูลหลัก</span><span class="sxs-lookup"><span data-stu-id="aaddb-201">By specifying a key field, you can use the **Lookup** function to retrieve a value from a dataset for a one-to-one relationship, for example, a key-value pair.</span></span> <span data-ttu-id="aaddb-202">นิพจน์ต่อไปนี้แสดงชื่อผลิตภัณฑ์จากชุดข้อมูล ("ผลิตภัณฑ์") ซึ่งกำหนดตัวระบุผลิตภัณฑ์เพื่อให้ตรงกับ:</span><span class="sxs-lookup"><span data-stu-id="aaddb-202">The following expression displays the product name from a dataset ("Product"), given the product identifier to match on:</span></span>  
  
    ```  
    =Lookup(Fields!PID.Value, Fields!ProductID.Value, Fields.ProductName.Value, "Product")  
    ```  
  
### <a name="lookupset"></a><span data-ttu-id="aaddb-203">LookupSet</span><span class="sxs-lookup"><span data-stu-id="aaddb-203">LookupSet</span></span>  
  
-   <span data-ttu-id="aaddb-204">คุณสามารถใช้ฟังก์ชัน **LookupSet** เพื่อกู้คืนชุดค่าจากชุดข้อมูลสำหรับความสัมพันธ์แบบหนึ่งต่อกลุ่ม โดยการระบุเขตข้อมูลหลัก</span><span class="sxs-lookup"><span data-stu-id="aaddb-204">By specifying a key field, you can use the **LookupSet** function to retrieve a set of values from a dataset for a one-to-many relationship.</span></span> <span data-ttu-id="aaddb-205">ตัวอย่างเช่น บุคคลหนึ่งสามารถมีหมายเลขโทรศัพท์ได้หลายหมายเลข</span><span class="sxs-lookup"><span data-stu-id="aaddb-205">For example, a person can have multiple telephone numbers.</span></span> <span data-ttu-id="aaddb-206">ในตัวอย่างต่อไปนี้ ถือว่าชุดข้อมูล PhoneList มีตัวระบุบุคคลและหมายเลขโทรศัพท์ในแต่ละแถว</span><span class="sxs-lookup"><span data-stu-id="aaddb-206">In the following example, assume the dataset PhoneList contains a person identifier and a telephone number in each row.</span></span> <span data-ttu-id="aaddb-207">**LookupSet** คืนอาร์เรย์ของค่า</span><span class="sxs-lookup"><span data-stu-id="aaddb-207">**LookupSet** returns an array of values.</span></span> <span data-ttu-id="aaddb-208">นิพจน์ต่อไปนี้รวมค่าที่ส่งคืนเป็นสตริงเดียวและแสดงรายการหมายเลขโทรศัพท์สำหรับบุคคลที่ระบุโดย ContactID:</span><span class="sxs-lookup"><span data-stu-id="aaddb-208">The following expression combines the return values into a single string and displays the list of telephone numbers for the person specified by ContactID:</span></span>  
  
    ```  
    =Join(LookupSet(Fields!ContactID.Value, Fields!PersonID.Value, Fields!PhoneNumber.Value, "PhoneList"),",")  
    ```  
  
###  <a name="conversion-functions"></a><a name="ConversionFunctions"></a> <span data-ttu-id="aaddb-209">ฟังก์ชันการแปลง</span><span class="sxs-lookup"><span data-stu-id="aaddb-209">Conversion functions</span></span>  
 <span data-ttu-id="aaddb-210">คุณสามารถใช้ฟังก์ชัน Visual Basic ในการแปลงเขตข้อมูลจากชนิดข้อมูลหนึ่งไปเป็นชนิดข้อมูลอื่นได้</span><span class="sxs-lookup"><span data-stu-id="aaddb-210">You can use Visual Basic functions to convert a field from the one data type to a different data type.</span></span> <span data-ttu-id="aaddb-211">ฟังก์ชันการแปลงสามารถนำไปใช้ในการแปลงชนิดข้อมูลค่าเริ่มต้นสำหรับเขตข้อมูลไปเป็นชนิดข้อมูลที่จำเป็นสำหรับการคำนวณหรือในการรวมข้อความ</span><span class="sxs-lookup"><span data-stu-id="aaddb-211">Conversion functions can be used to convert the default data type for a field to the data type needed for calculations or to combine text.</span></span>  
  
-   <span data-ttu-id="aaddb-212">นิพจน์ต่อไปนี้แปลงค่าคงที่ 500 เป็นชนิดทศนิยมเพื่อเปรียบเทียบกับชนิดข้อมูลการเงิน Transact-SQL ในเขตข้อมูลค่าสำหรับนิพจน์ตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="aaddb-212">The following expression converts the constant 500 to type Decimal in order to compare it to a Transact-SQL money data type in the Value field for a filter expression.</span></span>  
  
    ```  
    =CDec(500)  
    ```  
  
-   <span data-ttu-id="aaddb-213">นิพจน์ต่อไปนี้แสดงจำนวนค่าที่เลือกสำหรับพารามิเตอร์ที่มีหลายค่า *MySelection*</span><span class="sxs-lookup"><span data-stu-id="aaddb-213">The following expression displays the number of values selected for the multivalue parameter *MySelection*.</span></span>  
  
    ```  
    =CStr(Parameters!MySelection.Count)  
    ```  
  
###  <a name="decision-functions"></a><a name="DecisionFunctions"></a> <span data-ttu-id="aaddb-214">ฟังก์ชันการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="aaddb-214">Decision functions</span></span>  
  
-   <span data-ttu-id="aaddb-215">ฟังก์ชัน **Iif** คืนค่าหนึ่งในสองค่า ทั้งนี้ขึ้นอยู่กับว่านิพจน์นั้นเป็นจริงหรือไม่</span><span class="sxs-lookup"><span data-stu-id="aaddb-215">The **Iif** function returns one of two values depending on whether the expression is true or not.</span></span> <span data-ttu-id="aaddb-216">นิพจน์ต่อไปนี้ใช้ฟังก์ชัน **Iif** ในการคืนค่าแบบบูลีนของ **True** หากค่า`LineTotal`ไม่เกิน 100</span><span class="sxs-lookup"><span data-stu-id="aaddb-216">The following expression uses the **Iif** function to return a Boolean value of **True** if the value of `LineTotal` exceeds 100.</span></span> <span data-ttu-id="aaddb-217">หรือไม่ก็จะคืนค่า **False**:</span><span class="sxs-lookup"><span data-stu-id="aaddb-217">Otherwise it returns **False**:</span></span>  
  
    ```  
    =IIF(Fields!LineTotal.Value > 100, True, False)  
    ```  
  
-   <span data-ttu-id="aaddb-218">ใช้ฟังก์ชัน **IIF** หลายครั้ง (หรือที่เรียกว่า "IIF ที่ซ้อนกัน") ในการส่งคืนค่าหนึ่งในสามค่า ทั้งนี้ขึ้นอยู่กับค่าของ `PctComplete`</span><span class="sxs-lookup"><span data-stu-id="aaddb-218">Use multiple **IIF** functions (also known as "nested IIFs") to return one of three values depending on the value of `PctComplete`.</span></span> <span data-ttu-id="aaddb-219">นิพจน์ต่อไปนี้สามารถวางในสีเติมของกล่องข้อความเพื่อเปลี่ยนสีพื้นหลัง ทั้งนี้ขึ้นอยู่กับค่าในกล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="aaddb-219">The following expression can be placed in the fill color of a text box to change the background color depending on the value in the text box.</span></span>  
  
    ```  
    =IIF(Fields!PctComplete.Value >= 10, "Green", IIF(Fields!PctComplete.Value >= 1, "Blue", "Red"))  
    ```  
  
     <span data-ttu-id="aaddb-220">ค่าที่มากกว่าหรือเท่ากับ 10 จะแสดงด้วยพื้นหลังสีเขียว ค่าระหว่าง 1 กับ 9 แสดงด้วยพื้นหลังสีฟ้า และค่าที่น้อยกว่า 1 แสดงด้วยพื้นหลังสีแดง</span><span class="sxs-lookup"><span data-stu-id="aaddb-220">Values greater than or equal to 10 display with a green background, between 1 and 9 display with a blue background, and less than 1 display with a red background.</span></span>  
  
-   <span data-ttu-id="aaddb-221">วิธีการอื่นในการรับฟังก์ชันเดียวกัน ให้ใช้ฟังก์ชัน **Switch**</span><span class="sxs-lookup"><span data-stu-id="aaddb-221">A different way to get the same functionality uses the **Switch** function.</span></span> <span data-ttu-id="aaddb-222">ฟังก์ชัน **Switch** มีประโยชน์เมื่อคุณมีเงื่อนไขสามอย่างหรือมากกว่านั้นในการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="aaddb-222">The **Switch** function is useful when you have three or more conditions to test.</span></span> <span data-ttu-id="aaddb-223">ฟังก์ชัน **Switch** คืนค่าที่เกี่ยวข้องด้วยนิพจน์แรกในซีรีส์ที่ประมวลผลว่าเป็นจริง:</span><span class="sxs-lookup"><span data-stu-id="aaddb-223">The **Switch** function returns the value associated with the first expression in a series that evaluates to true:</span></span>  
  
    ```  
    =Switch(Fields!PctComplete.Value >= 10, "Green", Fields!PctComplete.Value >= 1, "Blue", Fields!PctComplete.Value = 1, "Yellow", Fields!PctComplete.Value <= 0, "Red")  
    ```  
  
     <span data-ttu-id="aaddb-224">ค่าที่มากกว่าหรือเท่ากับ 10 จะแสดงด้วยพื้นหลังสีเขียว ค่าระหว่าง 1 กับ 9 แสดงด้วยพื้นหลังสีฟ้า ค่าที่เท่ากับ 1 แสดงด้วยพื้นหลังสีเหลือง และค่า 0 หรือค่าน้อยกว่านั้นแสดงด้วยพื้นหลังสีแดง</span><span class="sxs-lookup"><span data-stu-id="aaddb-224">Values greater than or equal to 10 display with a green background, between 1 and 9 display with a blue background, equal to 1 display with a yellow background, and 0 or less display with a red background.</span></span>  
  
-   <span data-ttu-id="aaddb-225">ทดสอบค่าของเขตข้อมูล `ImportantDate` และคืนค่า "สีแดง" หากมีอายุมากกว่าหนึ่งสัปดาห์ และ "สีฟ้า" สำหรับที่เป็นอย่างอื่น</span><span class="sxs-lookup"><span data-stu-id="aaddb-225">Test the value of the `ImportantDate` field and return "Red" if it's more than a week old, and "Blue" otherwise.</span></span> <span data-ttu-id="aaddb-226">นิพจน์นี้อาจสามารถใช้เพื่อควบคุมคุณสมบัติสีของกล่องข้อความในหน่วยข้อมูลของรายงาน:</span><span class="sxs-lookup"><span data-stu-id="aaddb-226">This expression can be used to control the Color property of a text box in a report item:</span></span>  
  
    ```  
    =IIF(DateDiff("d",Fields!ImportantDate.Value, Now())>7,"Red","Blue")  
    ```  
  
-   <span data-ttu-id="aaddb-227">ทดสอบค่าของเขตข้อมูล `PhoneNumber` และคืนค่า "ไม่มีค่า" หากเป็น **Null**(**Nothing** ใน Visual Basic) หรือไม่ก็คืนค่าหมายเลขโทรศัพท์</span><span class="sxs-lookup"><span data-stu-id="aaddb-227">Test the value of the `PhoneNumber` field and return "No Value" if it's **null** (**Nothing** in Visual Basic); otherwise return the phone number value.</span></span> <span data-ttu-id="aaddb-228">นิพจน์นี้อาจสามารถใช้เพื่อควบคุมค่าของกล่องข้อความในหน่วยข้อมูลของรายงาน:</span><span class="sxs-lookup"><span data-stu-id="aaddb-228">This expression can be used to control the value of a text box in a report item.</span></span>  
  
    ```  
    =IIF(Fields!PhoneNumber.Value Is Nothing,"No Value",Fields!PhoneNumber.Value)  
    ```  
  
-   <span data-ttu-id="aaddb-229">ทดสอบค่าของเขตข้อมูล `Department` และคืนค่าชื่อรายงานย่อยหรือ **Null**(**Nothing** ใน Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="aaddb-229">Test the value of the `Department` field and return either a subreport name or a **null** (**Nothing** in Visual Basic).</span></span> <span data-ttu-id="aaddb-230">นิพจน์นี้สามารถใช้สำหรับรายงานย่อยเข้าถึงรายละเอียดตามเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="aaddb-230">This expression can be used for conditional drillthrough subreports.</span></span>  
  
    ```  
    =IIF(Fields!Department.Value = "Development", "EmployeeReport", Nothing)  
    ```  
  
-   <span data-ttu-id="aaddb-231">ทำการทดสอบหากค่าเขตข้อมูลเป็น Null</span><span class="sxs-lookup"><span data-stu-id="aaddb-231">Test if a field value is null.</span></span> <span data-ttu-id="aaddb-232">นิพจน์นี้สามารถใช้สำหรับควบคุมคุณสมบัติ **ที่ซ่อนอยู่** ของหน่วยข้อมูลของรายงานรูป</span><span class="sxs-lookup"><span data-stu-id="aaddb-232">This expression can be used to control the **Hidden** property of an image report item.</span></span> <span data-ttu-id="aaddb-233">ตัวอย่างต่อไปนี้ รูปที่ระบุโดยเขตข้อมูล [LargePhoto] จะแสดงขึ้นมาก็ต่อเมื่อค่าของเขตข้อมูลไม่ใช่ Null</span><span class="sxs-lookup"><span data-stu-id="aaddb-233">In the following example, the image specified by the field [LargePhoto] is displayed only if the value of the field is not null.</span></span>  
  
    ```  
    =IIF(IsNothing(Fields!LargePhoto.Value),True,False)  
    ```  
  
-   <span data-ttu-id="aaddb-234">ฟังก์ชัน **MonthName** คืนค่าสตริงที่มีชื่อของเดือนที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="aaddb-234">The **MonthName** function returns a string value containing the name of the specified month.</span></span> <span data-ttu-id="aaddb-235">ตัวอย่างต่อไปนี้แสดง NA ในเขตข้อมูลของเดือนเมื่อเขตข้อมูลมีค่าเป็น 0</span><span class="sxs-lookup"><span data-stu-id="aaddb-235">The following example displays NA in the Month field when the field contains the value of 0.</span></span>  
  
    ```  
    IIF(Fields!Month.Value=0,"NA",MonthName(IIF(Fields!Month.Value=0,1,Fields!Month.Value)))  
  
    ```  
  
##  <a name="report-functions"></a><a name="ReportFunctions"></a> <span data-ttu-id="aaddb-236">ฟังก์ชันรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-236">Report functions</span></span>  
 <span data-ttu-id="aaddb-237">ในนิพจน์ คุณสามารถเพิ่มแหล่งอ้างอิงไปยังฟังก์ชันรายงานเพิ่มเติมที่จัดการข้อมูลในรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-237">In an expression, you can add a reference to additional report functions that manipulate data in a report.</span></span> <span data-ttu-id="aaddb-238">หัวข้อนี้มีตัวอย่างสำหรับสองฟังก์ชันในฟังก์ชันเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="aaddb-238">This section provides examples for two of these functions.</span></span> 
  
###  <a name="sum"></a><a name="Sum"></a> <span data-ttu-id="aaddb-239">Sum</span><span class="sxs-lookup"><span data-stu-id="aaddb-239">Sum</span></span>  
  
-   <span data-ttu-id="aaddb-240">ฟังก์ชัน **Sum** สามารถรวมค่าในกลุ่มหรือขอบเขตข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="aaddb-240">The **Sum** function can total the values in a group or data region.</span></span> <span data-ttu-id="aaddb-241">ฟังก์ชันนี้มีประโยชน์ในส่วนหัวหรือส่วนท้ายของกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="aaddb-241">This function can be useful in the header or footer of a group.</span></span> <span data-ttu-id="aaddb-242">นิพจน์ต่อไปนี้แสดงผลรวมของข้อมูลในกลุ่มคำสั่งหรือขอบเขตข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="aaddb-242">The following expression displays the sum of data in the Order group or data region:</span></span>  
  
    ```  
    =Sum(Fields!LineTotal.Value, "Order")  
    ```  
  
-   <span data-ttu-id="aaddb-243">นอกจากนี้ คุณยังสามารถใช้ฟังก์ชัน **Sum** สำหรับการคำนวณค่ารวมที่มีเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="aaddb-243">You can also use the **Sum** function for conditional aggregate calculations.</span></span> <span data-ttu-id="aaddb-244">ตัวอย่างเช่น หากชุดข้อมูลมีเขตข้อมูลที่มีชื่อสถานะพร้อมด้วยค่าที่เป็นไปได้เช่น ยังไม่เริ่มต้น เริ่มต้นแล้ว เสร็จสิ้น นิพจน์ต่อไปนี้เมื่อวางลงในส่วนหัวของกลุ่ม จะทำการคำนวณผลรวมสำหรับค่าที่เสร็จสิ้นเท่านั้น:</span><span class="sxs-lookup"><span data-stu-id="aaddb-244">For example, if a dataset has a field that is named State with possible values Not Started, Started, Finished, the following expression, when placed in a group header, calculates the aggregate sum for only the value Finished:</span></span>  
  
    ```  
    =Sum(IIF(Fields!State.Value = "Finished", 1, 0))  
    ```  
  
###  <a name="rownumber"></a><a name="RowNumber"></a> <span data-ttu-id="aaddb-245">RowNumber</span><span class="sxs-lookup"><span data-stu-id="aaddb-245">RowNumber</span></span>  
  
-   <span data-ttu-id="aaddb-246">ฟังก์ชัน **RowNumber** เมื่อนำมาใช้ในกล่องข้อความภายในขอบเขตข้อมูล จะแสดงจำนวนแถวสำหรับแต่ละอินสแตนซ์ของกล่องข้อความซึ่งนิพจน์ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="aaddb-246">The **RowNumber** function, when used in a text box within a data region, displays the row number for each instance of the text box in which the expression appears.</span></span> <span data-ttu-id="aaddb-247">ฟังก์ชันนี้มีประโยชน์เพื่อกำหนดหมายเลขแถวในตาราง</span><span class="sxs-lookup"><span data-stu-id="aaddb-247">This function can be useful to number rows in a table.</span></span> <span data-ttu-id="aaddb-248">นอกจากนี้ ยังมีประโยชน์สำหรับงานที่ซับซ้อนมากขึ้น เช่น การมีตัวแบ่งหน้าตามจำนวนแถว</span><span class="sxs-lookup"><span data-stu-id="aaddb-248">It can also be useful for more complex tasks, such as providing page breaks based on number of rows.</span></span> <span data-ttu-id="aaddb-249">สำหรับข้อมูลเพิ่มเติม ให้ดู [ตัวแบ่งหน้า](#PageBreaks) ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="aaddb-249">For more information, see [Page Breaks](#PageBreaks) in this topic.</span></span>  
  
     <span data-ttu-id="aaddb-250">ขอบเขตที่คุณระบุสำหรับตัวควบคุม **RowNumber** เมื่อเริ่มต้นการเรียงลำดับใหม่</span><span class="sxs-lookup"><span data-stu-id="aaddb-250">The scope you specify for **RowNumber** controls when renumbering begins.</span></span> <span data-ttu-id="aaddb-251">คำหลัก **Nothing** จะระบุว่าฟังก์ชันจะเริ่มต้นการนับที่แถวแรกในขอบเขตข้อมูลที่อยู่นอกสุด</span><span class="sxs-lookup"><span data-stu-id="aaddb-251">The **Nothing** keyword indicates that the function will start counting at the first row in the outermost data region.</span></span> <span data-ttu-id="aaddb-252">หากต้องการเริ่มต้นการนับภายในขอบเขตข้อมูลที่ซ้อนกัน ให้ใช้ชื่อของขอบเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="aaddb-252">To start counting within nested data regions, use the name of the data region.</span></span> <span data-ttu-id="aaddb-253">หากต้องการเริ่มต้นการนับภายในกลุ่ม ให้ใช้ชื่อของกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="aaddb-253">To start counting within a group, use the name of the group.</span></span>  
  
    ```  
    =RowNumber(Nothing)  
    ```  
  
##  <a name="appearance-of-report-data"></a><a name="AppearanceofReportData"></a> <span data-ttu-id="aaddb-254">ลักษณะของข้อมูลรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-254">Appearance of report data</span></span>  
 <span data-ttu-id="aaddb-255">คุณสามารถใช้นิพจน์เพื่อจัดการวิธีที่ข้อมูลจะปรากฏบนรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-255">You can use expressions to manipulate how data appears on a report.</span></span> <span data-ttu-id="aaddb-256">ตัวอย่างเช่น คุณสามารถแสดงค่าของสองเขตข้อมูลในกล่องข้อความเดียวได้ แสดงข้อมูลเกี่ยวกับรายงาน หรือผลกระทบจากการใส่ตัวแบ่งหน้าในรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-256">For example, you can display the values of two fields in a single text box, display information about the report, or affect how page breaks are inserted in the report.</span></span>  
  
###  <a name="page-headers-and-footers"></a><a name="PageHeadersandFooters"></a> <span data-ttu-id="aaddb-257">ส่วนหัวและส่วนท้ายของหน้า</span><span class="sxs-lookup"><span data-stu-id="aaddb-257">Page headers and footers</span></span>  
 <span data-ttu-id="aaddb-258">เมื่อออกแบบรายงาน คุณอาจต้องการแสดงชื่อของรายงานและหมายเลขหน้าในส่วนท้ายของรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-258">When designing a report, you may want to display the name of the report and page number in the report footer.</span></span> <span data-ttu-id="aaddb-259">ในการทำเช่นนี้ คุณสามารถใช้นิพจน์ต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="aaddb-259">To do this, you can use the following expressions:</span></span>  
  
-   <span data-ttu-id="aaddb-260">นิพจน์ต่อไปนี้มีชื่อของรายงานและเวลาที่เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="aaddb-260">The following expression provides the name of the report and the time it was run.</span></span> <span data-ttu-id="aaddb-261">ซึ่งสามารถนำมาวางในกล่องข้อความในส่วนท้ายของรายงานหรือในเนื้อความของรายงานได้</span><span class="sxs-lookup"><span data-stu-id="aaddb-261">It can be placed in a text box in the report footer or in the body of the report.</span></span> <span data-ttu-id="aaddb-262">เวลาถูกจัดรูปแบบด้วยสตริงการจัดรูปแบบใน .NET Framework สำหรับวันที่ระยะสั้น:</span><span class="sxs-lookup"><span data-stu-id="aaddb-262">The time is formatted with the .NET Framework formatting string for short date:</span></span>  
  
    ```  
    =Globals.ReportName & ", dated " & Format(Globals.ExecutionTime, "d")  
    ```  
  
-   <span data-ttu-id="aaddb-263">นิพจน์ต่อไปนี้ ซึ่งวางในกล่องข้อความในส่วนท้ายของรายงาน จะมีหมายเลขหน้าและหน้าทั้งหมดในรายงาน:</span><span class="sxs-lookup"><span data-stu-id="aaddb-263">The following expression, placed in a text box in the footer of a report, provides page number and total pages in the report:</span></span>  
  
    ```  
    =Globals.PageNumber & " of " & Globals.TotalPages  
    ```  
  
 <span data-ttu-id="aaddb-264">ตัวอย่างต่อไปนี้อธิบายวิธีแสดงค่าแรกและค่าสุดท้ายจากหน้าในส่วนหัวของหน้า คล้ายกับที่คุณอาจพบในรายการไดเรกทอรี</span><span class="sxs-lookup"><span data-stu-id="aaddb-264">The following examples describe how to display the first and last values from a page in the page header, similar to what you might find in a directory listing.</span></span> <span data-ttu-id="aaddb-265">ตัวอย่างจะถือว่าขอบเขตข้อมูลที่มีกล่องข้อความที่มีชื่อ `LastName`</span><span class="sxs-lookup"><span data-stu-id="aaddb-265">The example assumes a data region that contains a text box named `LastName`.</span></span>  
  
-   <span data-ttu-id="aaddb-266">นิพจน์ต่อไปนี้ที่วางในกล่องข้อความทางด้านซ้ายบนส่วนหัวของหน้า จะมีค่าแรกของกล่องข้อความ `LastName` บนหน้า:</span><span class="sxs-lookup"><span data-stu-id="aaddb-266">The following expression, placed in a text box on the left side of the page header, provides the first value of the `LastName` text box on the page:</span></span>  
  
    ```  
    =First(ReportItems("LastName").Value)  
    ```  
  
-   <span data-ttu-id="aaddb-267">นิพจน์ต่อไปนี้ที่วางในกล่องข้อความทางด้านขวาบนส่วนหัวของหน้า จะมีค่าล่าสุดของกล่องข้อความ `LastName` บนหน้า:</span><span class="sxs-lookup"><span data-stu-id="aaddb-267">The following expression, placed in a text box on the right side of the page header, provides the last value of the `LastName` text box on the page:</span></span>  
  
    ```  
    =Last(ReportItems("LastName").Value)  
    ```  
  
 <span data-ttu-id="aaddb-268">ตัวอย่างต่อไปนี้อธิบายวิธีการแสดงผลรวมของหน้า</span><span class="sxs-lookup"><span data-stu-id="aaddb-268">The following example describes how to display a page total.</span></span> <span data-ttu-id="aaddb-269">ตัวอย่างจะถือว่าขอบเขตข้อมูลที่มีกล่องข้อความที่มีชื่อ `Cost`</span><span class="sxs-lookup"><span data-stu-id="aaddb-269">The example assumes a data region that contains a text box named `Cost`.</span></span>  
  
-   <span data-ttu-id="aaddb-270">นิพจน์ต่อไปนี้วางในส่วนหัวหรือส่วนท้ายของหน้า จะมีผลรวมของค่าในกล่องข้อความ `Cost` สำหรับหน้า:</span><span class="sxs-lookup"><span data-stu-id="aaddb-270">The following expression, placed in the page header or footer, provides the sum of the values in the `Cost` text box for the page:</span></span>  
  
    ```  
    =Sum(ReportItems("Cost").Value)  
    ```  
  
> [!NOTE]  
>  <span data-ttu-id="aaddb-271">คุณสามารถอ้างอิงถึงหน่วยข้อมูลของรายงานได้เพียงหนึ่งหน่วยต่อนิพจน์ในส่วนหัวและส่วนท้ายของหน้า</span><span class="sxs-lookup"><span data-stu-id="aaddb-271">You can refer to only one report item per expression in a page header or footer.</span></span> <span data-ttu-id="aaddb-272">นอกจากนี้ คุณยังสามารถอ้างอิงถึงชื่อกล่องข้อความได้ แต่ไม่ใช่นิพจน์ข้อมูลจริงภายในกล่องข้อความ ในนิพจน์ส่วนหัวและส่วนท้ายของหน้า</span><span class="sxs-lookup"><span data-stu-id="aaddb-272">Also, you can refer to the text box name, but not the actual data expression within the text box, in page header and footer expressions.</span></span>  
  
###  <a name="page-breaks"></a><a name="PageBreaks"></a> <span data-ttu-id="aaddb-273">ตัวแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="aaddb-273">Page breaks</span></span>  
 <span data-ttu-id="aaddb-274">ในบางรายงาน คุณอาจต้องการวางตัวแบ่งหน้าที่ตอนท้ายของจำนวนแถวที่ระบุแทนหรือรวมถึงบนกลุ่มหรือหน่วยข้อมูลของรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-274">In some reports, you may want to place a page break at the end of a specified number of rows instead of, or in addition to, on groups or report items.</span></span> <span data-ttu-id="aaddb-275">ในการทำเช่นนี้ ให้สร้างกลุ่มที่มีกลุ่มหรือบันทึกรายละเอียดที่คุณต้องการ เพิ่มตัวแบ่งหน้าไปยังกลุ่ม และจากนั้นเพิ่มนิพจน์กลุ่มไปยังกลุ่มตามจำนวนแถวที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="aaddb-275">To do this, create a group that contains the groups or detail records you want, add a page break to the group, and then add a group expression to group by a specified number of rows.</span></span>  
  
-   <span data-ttu-id="aaddb-276">นิพจน์ต่อไปนี้เมื่อวางในนิพจน์กลุ่ม จะกำหนดจำนวนแถว 25 แถวสำหรับแต่ละชุด</span><span class="sxs-lookup"><span data-stu-id="aaddb-276">The following expression, when placed in the group expression, assigns a number to each set of 25 rows.</span></span> <span data-ttu-id="aaddb-277">เมื่อมีการกำหนดตัวแบ่งหน้าสำหรับกลุ่ม นิพจน์นี้ส่งผลให้มีตัวแบ่งหน้าทุก ๆ 25 แถว</span><span class="sxs-lookup"><span data-stu-id="aaddb-277">When a page break is defined for the group, this expression results in a page break every 25 rows.</span></span>  
  
    ```  
    =Ceiling(RowNumber(Nothing)/25)  
    ```  
  
     <span data-ttu-id="aaddb-278">หากต้องการอนุญาตให้ผู้ใช้สามารถตั้งค่าสำหรับจำนวนแถวแต่ละหน้า ให้สร้างพารามิเตอร์ที่มีชื่อ `RowsPerPage` และอิงนิพจน์กลุ่มตามพารามิเตอร์ ดังที่แสดงในนิพจน์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="aaddb-278">To allow the user to set a value for the number of rows per page, create a parameter named `RowsPerPage` and base the group expression on the parameter, as shown in the following expression:</span></span>  
  
    ```  
    =Ceiling(RowNumber(Nothing)/Parameters!RowsPerPage.Value)  
    ```  
  
##  <a name="properties"></a><a name="Properties"></a> <span data-ttu-id="aaddb-279">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="aaddb-279">Properties</span></span>  
 <span data-ttu-id="aaddb-280">นิพจน์ไม่เพียงแต่ใช้เพื่อแสดงข้อมูลในกล่องข้อความเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="aaddb-280">Expressions are not only used to display data in text boxes.</span></span> <span data-ttu-id="aaddb-281">ซึ่งอาจสามารถใช้เพื่อเปลี่ยนแปลงวิธีการนำคุณสมบัติไปใช้ในหน่วยข้อมูลของรายงานด้วย</span><span class="sxs-lookup"><span data-stu-id="aaddb-281">They can also be used to change how properties are applied to report items.</span></span> <span data-ttu-id="aaddb-282">คุณสามารถเปลี่ยนแปลงข้อมูลรูปแบบสำหรับหน่วยข้อมูลของรายงาน หรือเปลี่ยนแปลงการมองเห็นของรายงานได้</span><span class="sxs-lookup"><span data-stu-id="aaddb-282">You can change style information for a report item, or change its visibility.</span></span>  
  
###  <a name="formatting"></a><a name="Formatting"></a> <span data-ttu-id="aaddb-283">การจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="aaddb-283">Formatting</span></span>  
  
-   <span data-ttu-id="aaddb-284">นิพจน์ต่อไปนี้เมื่อนำไปใช้ในคุณสมบัติสีของกล่องข้อความ จะเปลี่ยนแปลงสีของข้อความ ทั้งนี้ขึ้นอยู่กับค่าของเขตข้อมูล `Profit` :</span><span class="sxs-lookup"><span data-stu-id="aaddb-284">The following expression, when used in the Color property of a text box, changes the color of the text depending on the value of the `Profit` field:</span></span>  
  
    ```  
    =Iif(Fields!Profit.Value < 0, "Red", "Black")  
    ```  
  
     <span data-ttu-id="aaddb-285">นอกจากนี้ คุณยังสามารถใช้ตัวแปรออบเจ็กต์ Visual Basic ได้ `Me`</span><span class="sxs-lookup"><span data-stu-id="aaddb-285">You can also use the Visual Basic object variable `Me`.</span></span> <span data-ttu-id="aaddb-286">ตัวแปรนี้เป็นอีกวิธีหนึ่งในการอ้างอิงถึงค่าของกล่องข้อความ</span><span class="sxs-lookup"><span data-stu-id="aaddb-286">This variable is another way of referring to the value of a text box.</span></span>  
  
     `=Iif(Me.Value < 0, "Red", "Black")`  
  
-   <span data-ttu-id="aaddb-287">นิพจน์ต่อไปนี้เมื่อนำมาใช้ในคุณสมบัติสีพื้นหลังของหน่วยข้อมูลรายงานในขอบเขตข้อมูล จะเปลี่ยนสีพื้นหลังของแต่ละแถวระหว่างสีเขียวอ่อนและสีขาว:</span><span class="sxs-lookup"><span data-stu-id="aaddb-287">The following expression, when used in the BackgroundColor property of a report item in a data region, alternates the background color of each row between pale green and white:</span></span>  
  
    ```  
    =Iif(RowNumber(Nothing) Mod 2, "PaleGreen", "White")  
    ```  
  
     <span data-ttu-id="aaddb-288">หากคุณใช้นิพจน์สำหรับขอบเขตที่ระบุ คุณอาจต้องระบุชุดข้อมูลสำหรับฟังก์ชันการรวม:</span><span class="sxs-lookup"><span data-stu-id="aaddb-288">If you are using an expression for a specified scope, you may have to indicate the dataset for the aggregate function:</span></span>  
  
    ```  
    =Iif(RowNumber("Employees") Mod 2, "PaleGreen", "White")  
    ```  
  
> [!NOTE]  
>  <span data-ttu-id="aaddb-289">สีที่มีอยู่มาจากการแจงนับของ KnownColor .NET Framework</span><span class="sxs-lookup"><span data-stu-id="aaddb-289">Available colors come from the .NET Framework KnownColor enumeration.</span></span>  
  
### <a name="chart-colors"></a><span data-ttu-id="aaddb-290">แผนภูมิสี</span><span class="sxs-lookup"><span data-stu-id="aaddb-290">Chart colors</span></span>  
 <span data-ttu-id="aaddb-291">ในการระบุสีสำหรับแผนภูมิรูปร่าง คุณสามารถใช้รหัสที่กำหนดเองในการควบคุมลำดับที่สีจะถูกแมปเข้ากับค่าของจุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="aaddb-291">To specify colors for a Shape chart, you can use custom code to control the order that colors are mapped to data point values.</span></span> <span data-ttu-id="aaddb-292">สิ่งนี้จะช่วยคุณในการใช้สีที่สอดคล้องกันสำหรับแผนภูมิหลายอันที่มีกลุ่มประเภทเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="aaddb-292">This helps you use consistent colors for multiple charts that have the same category groups.</span></span> 
  
###  <a name="visibility"></a><a name="Visibility"></a> <span data-ttu-id="aaddb-293">การมองเห็น</span><span class="sxs-lookup"><span data-stu-id="aaddb-293">Visibility</span></span>  
 <span data-ttu-id="aaddb-294">คุณสามารถแสดงและซ่อนหน่วยข้อมูลในรายงานโดยใช้คุณสมบัติการมองเห็นสำหรับหน่วยข้อมูลของรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-294">You can show and hide items in a report using the visibility properties for the report item.</span></span> <span data-ttu-id="aaddb-295">ในขอบเขตข้อมูล เช่น ตาราง คุณสามารถซ่อนแถวแสดงรายละเอียดในขั้นต้นได้ตามค่าในนิพจน์</span><span class="sxs-lookup"><span data-stu-id="aaddb-295">In a data region such as a table, you can initially hide detail rows based on the value in an expression.</span></span>  
  
-   <span data-ttu-id="aaddb-296">นิพจน์ต่อไปนี้เมื่อนำมาใช้สำหรับการมองเห็นเริ่มต้นของแถวรายละเอียดในกลุ่ม จะแสดงแถวรายละเอียดสำหรับยอดขายทั้งหมดไม่เกิน 90 เปอร์เซ็นต์ในเขตข้อมูล `PctQuota` :</span><span class="sxs-lookup"><span data-stu-id="aaddb-296">The following expression, when used for initial visibility of detail rows in a group, shows the detail rows for all sales exceeding 90 percent in the `PctQuota` field:</span></span>  
  
    ```  
    =Iif(Fields!PctQuota.Value>.9, False, True)  
    ```  
  
-   <span data-ttu-id="aaddb-297">นิพจน์ต่อไปนี้เมื่อตั้งค่าในคุณสมบัติที่ซ่อนอยู่ของตาราง จะแสดงตารางก็ต่อเมื่อมีมากกว่า 12 แถว:</span><span class="sxs-lookup"><span data-stu-id="aaddb-297">The following expression, when set in the Hidden property of a table, shows the table only if it has more than 12 rows:</span></span>  
  
    ```  
    =IIF(CountRows()>12,false,true)  
    ```  
  
-   <span data-ttu-id="aaddb-298">นิพจน์ต่อไปนี้ เมื่อตั้งค่าในคุณสมบัติที่ **ซ่อนอยู่** ของคอลัมน์ จะแสดงคอลัมน์ก็ต่อเมื่อมีเขตข้อมูลอยู่ในชุดข้อมูลของรายงานหลังจากข้อมูลถูกกู้คืนมาจากแหล่งข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="aaddb-298">The following expression, when set in the **Hidden** property of a column, shows the column only if the field exists in the report dataset after the data is retrieved from the data source:</span></span>  
  
    ```  
    =IIF(Fields!Column_1.IsMissing, true, false)  
    ```  
  
###  <a name="urls"></a><a name="Hyperlinks"></a> <span data-ttu-id="aaddb-299">URL</span><span class="sxs-lookup"><span data-stu-id="aaddb-299">URLs</span></span>  
 <span data-ttu-id="aaddb-300">คุณสามารถกำหนด URL เองได้โดยการใช้ข้อมูลรายงาน และยังสามารถควบคุมอย่างมีเงื่อนไขว่าจะเพิ่มเป็นการดำเนินการสำหรับกล่องข้อความหรือไม่</span><span class="sxs-lookup"><span data-stu-id="aaddb-300">You can customize URLs by using report data and also conditionally control whether URLs are added as an action for a text box.</span></span>  
  
-   <span data-ttu-id="aaddb-301">นิพจน์ต่อไปนี้ เมื่อนำมาใช้เป็นการดำเนินการบนกล่องข้อความ จะสร้าง URL ที่กำหนดเองซึ่งจะระบุเขตชุดข้อมูล `EmployeeID` เป็นพารามิเตอร์ URL</span><span class="sxs-lookup"><span data-stu-id="aaddb-301">The following expression, when used as an action on a text box, generates a customized URL that specifies the dataset field `EmployeeID` as a URL parameter.</span></span>  
  
    ```  
    ="https://adventure-works/MyInfo?ID=" & Fields!EmployeeID.Value  
    ```  
  
-   นิพจน์ต่อไปนี้ควบคุมอย่างมีเงื่อนไขว่าจะเพิ่ม URL ในกล่องข้อความหรือไม่ นิพจน์นี้ขึ้นอยู่กับพารามิเตอร์ที่มีชื่อ `IncludeURLs` ที่อนุญาตให้ผู้ใช้ตัดสินใจว่าจะรวม URL ที่ใช้งานอยู่ในรายงานหรือไม่ นิพจน์นี้จะตั้งค่าเป็นการดำเนินการในกล่องข้อความ <span data-ttu-id="aaddb-305">โดยการตั้งค่าพารามิเตอร์เป็นเท็จและจากนั้นดูที่รายงาน คุณสามารถส่งรายงาน Microsoft Excel ออกไปได้โดยไม่มีไฮเปอร์ลิงก์</span><span class="sxs-lookup"><span data-stu-id="aaddb-305">By setting the parameter to False and then viewing the report, you can export the report Microsoft Excel without hyperlinks.</span></span>  
  
    ```  
    =IIF(Parameters!IncludeURLs.Value,"https://adventure-works.com/productcatalog",Nothing)  
    ```  
  
> [!NOTE]
>  <span data-ttu-id="aaddb-306">รายงานที่มีการแบ่งหน้าของ Power BI ไม่สนับสนุนการใช้ JavaScript ภายในนิพจน์ **Go To URL**</span><span class="sxs-lookup"><span data-stu-id="aaddb-306">Power BI paginated reports don't support using JavaScript within a **Go To URL** expression.</span></span>  
  
##  <a name="report-data"></a><a name="ReportData"></a> <span data-ttu-id="aaddb-307">ข้อมูลรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-307">Report data</span></span>  
 <span data-ttu-id="aaddb-308">นิพจน์สามารถนำมาใช้ในการจัดการข้อมูลที่ใช้ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-308">Expressions can be used to manipulate the data that is used in the report.</span></span> <span data-ttu-id="aaddb-309">คุณสามารถอ้างอิงถึงพารามิเตอร์และข้อมูลรายงานอื่นๆ ได้</span><span class="sxs-lookup"><span data-stu-id="aaddb-309">You can refer to parameters and other report information.</span></span> <span data-ttu-id="aaddb-310">แล้วคุณยังสามารถเปลี่ยนแปลงการสอบถามที่นำมาใช้ในการกู้คืนข้อมูลสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-310">You can even change the query that is used to retrieve data for the report.</span></span>  
  
###  <a name="parameters"></a><a name="Parameters"></a> <span data-ttu-id="aaddb-311">พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="aaddb-311">Parameters</span></span>  
 <span data-ttu-id="aaddb-312">คุณสามารถใช้นิพจน์ในพารามิเตอร์เพื่อเปลี่ยนแปลงค่าเริ่มต้นสำหรับพารามิเตอร์ได้</span><span class="sxs-lookup"><span data-stu-id="aaddb-312">You can use expressions in a parameter to vary the default value for the parameter.</span></span> <span data-ttu-id="aaddb-313">ตัวอย่างเช่น คุณสามารถใช้พารามิเตอร์ในการกรองข้อมูลไปยังผู้ใช้ที่เฉพาะเจาะจงตามรหัสผู้ใช้ที่สามารถนำมาใช้ในการเรียกใช้รายงานได้</span><span class="sxs-lookup"><span data-stu-id="aaddb-313">For example, you can use a parameter to filter data to a particular user based on the user ID that is used to run the report.</span></span>  
  
-   <span data-ttu-id="aaddb-314">นิพจน์ต่อไปนี้เมื่อนำมาใช้เป็นค่าเริ่มต้นสำหรับพารามิเตอร์ จะรวบรวมรหัสผู้ใช้ของบุคคลที่เรียกใช้รายงาน:</span><span class="sxs-lookup"><span data-stu-id="aaddb-314">The following expression, when used as the default value for a parameter, collects the user ID of the person running the report:</span></span>  
  
    ```  
    =User!UserID  
    ```  
  
-   <span data-ttu-id="aaddb-315">เพื่ออ้างอิงถึงพารามิเตอร์ในพารามิเตอร์การคิวรี ตัวกรองนิพจน์ กล่องข้อความหรือพื้นที่อื่นๆ ของรายงาน ให้ใช้คอลเลกชันส่วนกลางของ **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="aaddb-315">To refer to a parameter in a query parameter, filter expression, text box, or other area of the report, use the **Parameters** global collection.</span></span> <span data-ttu-id="aaddb-316">ตัวอย่างนี้จะถือว่าพารามิเตอร์ถูกตั้งชื่อเป็น *แผนก*:</span><span class="sxs-lookup"><span data-stu-id="aaddb-316">This example assumes that the parameter is named *Department*:</span></span>  
  
    ```  
    =Parameters!Department.Value  
    ```  
  
-   <span data-ttu-id="aaddb-317">พารามิเตอร์อาจถูกสร้างในรายงาน แต่ตั้งค่าเป็นซ่อนอยู่</span><span class="sxs-lookup"><span data-stu-id="aaddb-317">Parameters can be created in a report but set to hidden.</span></span> <span data-ttu-id="aaddb-318">เมื่อรายงานเรียกใช้บนเซิร์ฟเวอร์รายงาน พารามิเตอร์จะไม่ปรากฏแถบเครื่องมือและโปรแกรมอ่านรายงานจะไม่สามารถเปลี่ยนแปลงค่าเริ่มต้นได้</span><span class="sxs-lookup"><span data-stu-id="aaddb-318">When the report runs on the report server, the parameter doesn't appear in the toolbar and the report reader cannot change the default value.</span></span> <span data-ttu-id="aaddb-319">คุณสามารถใช้พารามิเตอร์ที่ซ่อนอยู่ โดยตั้งค่าเป็นค่าเริ่มต้นที่เป็นค่าคงที่ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="aaddb-319">You can use a hidden parameter set to a default value as custom constant.</span></span> <span data-ttu-id="aaddb-320">คุณสามารถใช้ค่านี้ในนิพจน์ใดๆ รวมถึงนิพจน์ของเขตข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="aaddb-320">You can use this value in any expression, including a field expression.</span></span> <span data-ttu-id="aaddb-321">นิพจน์ต่อไปนี้ระบุเขตข้อมูลที่ระบุตามค่าพารามิเตอร์ค่าเริ่มต้นสำหรับพารามิเตอร์ที่มีชื่อ *ParameterField*:</span><span class="sxs-lookup"><span data-stu-id="aaddb-321">The following expression identifies the field specified by the default parameter value for the parameter named *ParameterField*:</span></span>  
  
    ```  
    =Fields(Parameters!ParameterField.Value).Value  
    ```  
  
##  <a name="custom-code"></a><a name="CustomCode"></a> <span data-ttu-id="aaddb-322">รหัสที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="aaddb-322">Custom code</span></span>  
 <span data-ttu-id="aaddb-323">คุณสามารถใช้รหัสที่กำหนดเองที่ฝังในรายงานได้</span><span class="sxs-lookup"><span data-stu-id="aaddb-323">You can use custom code embedded in a report.</span></span> 
  
### <a name="using-group-variables-for-custom-aggregation"></a><span data-ttu-id="aaddb-324">การใช้ตัวแปรกลุ่มสำหรับการรวมที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="aaddb-324">Using group variables for custom aggregation</span></span>  
 <span data-ttu-id="aaddb-325">คุณสามารถเริ่มต้นค่าสำหรับตัวแปรกลุ่มที่อยู่ภายในขอบเขตกลุ่มเฉพาะ แล้วรวมการอ้างอิงถึงตัวแปรนั้นในนิพจน์</span><span class="sxs-lookup"><span data-stu-id="aaddb-325">You can initialize the value for a group variable that is local to a particular group scope and then include a reference to that variable in expressions.</span></span> <span data-ttu-id="aaddb-326">หนึ่งในวิธีที่คุณสามารถใช้ตัวแปรกลุ่มด้วยรหัสที่กำหนดเองได้ คือ การนำค่ารวมที่กำหนดเองไปใช้</span><span class="sxs-lookup"><span data-stu-id="aaddb-326">One of the ways that you can use a group variable with custom code is to implement a custom aggregate.</span></span> 
  
## <a name="suppressing-null-or-zero-values-at-run-time"></a><span data-ttu-id="aaddb-327">การระงับค่า Null หรือค่าศูนย์ในเวลาที่เรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-327">Suppressing null or zero values at run time</span></span>  
 <span data-ttu-id="aaddb-328">บางค่าในนิพจน์อาจประเมินได้เป็น Null หรือระบุไม่ได้เมื่อถึงเวลาการประมวลผลรายงาน</span><span class="sxs-lookup"><span data-stu-id="aaddb-328">Some values in an expression can evaluate to null or undefined at report processing time.</span></span> <span data-ttu-id="aaddb-329">ซึ่งอาจก่อให้เกิดข้อผิดพลาดขณะทำงานที่ส่งผลให้ **#Error** แสดงในกล่องข้อความแทนนิพจน์ที่ประเมิน</span><span class="sxs-lookup"><span data-stu-id="aaddb-329">This can create run-time errors that result in **#Error** displaying in the text box instead of the evaluated expression.</span></span> <span data-ttu-id="aaddb-330">ฟังก์ชัน **IIF** มีความไวต่อพฤติกรรมนี้เป็นพิเศษ เนื่องจากการเลิกชอบคำสั่ง If-Then-Else แต่ละส่วนของคำสั่ง **IIF** จะถูกประเมินผล (รวมถึงฟังก์ชันการโทร) ก่อนที่จะทำการส่งไปยังรูทีนที่ทดสอบว่า **true** หรือ **false**</span><span class="sxs-lookup"><span data-stu-id="aaddb-330">The **IIF** function is particularly sensitive to this behavior because, unlike an If-Then-Else statement, each part of the **IIF** statement is evaluated (including function calls) before being passed to the routine that tests for **true** or **false**.</span></span> <span data-ttu-id="aaddb-331">คำสั่ง `=IIF(Fields!Sales.Value is NOTHING, 0, Fields!Sales.Value)` สร้าง **#Error** ในรายงานที่แสดงผลหาก `Fields!Sales.Value` เป็น NOTHING</span><span class="sxs-lookup"><span data-stu-id="aaddb-331">The statement `=IIF(Fields!Sales.Value is NOTHING, 0, Fields!Sales.Value)` generates **#Error** in the rendered report if `Fields!Sales.Value` is NOTHING.</span></span>  
  
 <span data-ttu-id="aaddb-332">หากต้องการหลีกเลี่ยงเงื่อนไขนี้ ให้ใช้หนึ่งในกลยุทธ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="aaddb-332">To avoid this condition, use one of the following strategies:</span></span>  
  
-   <span data-ttu-id="aaddb-333">ตั้งค่าตัวเศษเป็น 0 และตัวส่วนเป็น 1 หากค่าของเขตข้อมูล B เป็น 0 หรือไม่ได้ระบุ; หรือตั้งค่าตัวเศษเป็นค่าของเขตข้อมูล A และตัวส่วนเป็นค่าของเขตข้อมูล B</span><span class="sxs-lookup"><span data-stu-id="aaddb-333">Set the numerator to 0 and the denominator to 1 if the value for field B is 0 or undefined; otherwise, set the numerator to the value for field A and the denominator to the value for field B.</span></span>  
  
    ```  
    =IIF(Field!B.Value=0, 0, Field!A.Value / IIF(Field!B.Value =0, 1, Field!B.Value))  
    ```  
  
-   <span data-ttu-id="aaddb-334">ใช้ฟังก์ชันรหัสที่กำหนดเองในการคืนค่าสำหรับนิพจน์</span><span class="sxs-lookup"><span data-stu-id="aaddb-334">Use a custom code function to return the value for the expression.</span></span> <span data-ttu-id="aaddb-335">ตัวอย่างต่อไปนี้คืนค่าความแตกต่างเป็นเปอร์เซ็นต์ระหว่างค่าในปัจจุบันกับค่าก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="aaddb-335">The following example returns the percentage difference between a current value and a previous value.</span></span> <span data-ttu-id="aaddb-336">ซึ่งสามารถนำมาใช้ในการคำนวณค่าความแตกต่างระหว่างค่าต่อเนื่องสองค่าใดๆ และจัดการกับกรณีการเชื่อมต่อจากการเปรียบเทียบครั้งแรก (เมื่อไม่มีค่าก่อนหน้า) และกรณีไม่ว่าจะเป็นค่าก่อนหน้าหรือค่าในปัจจุบันที่เป็น **Null**(**Nothing** ใน Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="aaddb-336">This can be used to calculate the difference between any two successive values and it handles the edge case of the first comparison (when there is no previous value) and cases whether either the previous value or the current value is **null** (**Nothing** in Visual Basic).</span></span>  
  
    ```  
    Public Function GetDeltaPercentage(ByVal PreviousValue, ByVal CurrentValue) As Object  
        If IsNothing(PreviousValue) OR IsNothing(CurrentValue) Then  
            Return Nothing  
        Else if PreviousValue = 0 OR CurrentValue = 0 Then  
            Return Nothing  
        Else   
            Return (CurrentValue - PreviousValue) / CurrentValue  
        End If  
    End Function  
    ```  
  
     <span data-ttu-id="aaddb-337">นิพจน์ต่อไปนี้แสดงวิธีการเรียกใช้รหัสที่กำหนดเองจากกล่องข้อความ สำหรับคอนเทนเนอร์ "ColumnGroupByYear" (กลุ่มหรือขอบเขตข้อมูล)</span><span class="sxs-lookup"><span data-stu-id="aaddb-337">The following expression shows how to call this custom code from a text box, for the "ColumnGroupByYear" container (group or data region).</span></span>  
  
    ```  
    =Code.GetDeltaPercentage(Previous(Sum(Fields!Sales.Value),"ColumnGroupByYear"), Sum(Fields!Sales.Value))  
    ```  
  
     <span data-ttu-id="aaddb-338">ซึ่งจะช่วยหลีกเลี่ยงข้อยกเว้นในเวลาที่เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="aaddb-338">This helps to avoid run-time exceptions.</span></span> <span data-ttu-id="aaddb-339">ตอนนี้คุณสามารถใช้นิพจน์นิพจน์เช่น `=IIF(Me.Value < 0, "red", "black")` ในคุณสมบัติ **Color** ของกล่องข้อความสำหรับข้อความที่แสดงอย่างมีเงื่อนไข ขึ้นอยู่กับว่าค่ามากกว่าหรือน้อยกว่า 0 หรือไม่</span><span class="sxs-lookup"><span data-stu-id="aaddb-339">You can now use an expression like `=IIF(Me.Value < 0, "red", "black")` in the **Color** property of the text box to conditionally the display text based on whether the values are greater than or less than 0.</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="aaddb-340">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="aaddb-340">Next steps</span></span>

- [<span data-ttu-id="aaddb-341">รายงานแบบแบ่งหน้าใน Power BI Premium คืออะไร</span><span class="sxs-lookup"><span data-stu-id="aaddb-341">What are paginated reports in Power BI Premium?</span></span>](paginated-reports-report-builder-power-bi.md)
