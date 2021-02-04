---
ms.openlocfilehash: c3b1b7288d0d277fc866ea47887335d10279c6cc
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/05/2020
ms.locfileid: "73800172"
---
<span data-ttu-id="f1ce8-101">ด้วย DAX คุณจะมีฟังก์ชันมากมายพร้อมให้ใช้งานสำหรับการสร้างรูปร่าง สร้างฟอร์ม หรือวิเคราะห์ข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="f1ce8-101">With DAX, there are many functions available to shape, form, or otherwise analyze your data.</span></span> <span data-ttu-id="f1ce8-102">ฟังก์ชันเหล่านี้สามารถถูกจัดกลุ่มเป็นประเภทได้ดังนี้:</span><span class="sxs-lookup"><span data-stu-id="f1ce8-102">These functions can be grouped into a handful of categories:</span></span>

* <span data-ttu-id="f1ce8-103">ฟังก์ชัน**การรวม**</span><span class="sxs-lookup"><span data-stu-id="f1ce8-103">**Aggregation** functions</span></span>
* <span data-ttu-id="f1ce8-104">ฟังก์ชัน**การตรวจนับ**</span><span class="sxs-lookup"><span data-stu-id="f1ce8-104">**Counting** functions</span></span>
* <span data-ttu-id="f1ce8-105">ฟังก์ชัน**ตรรกะ**</span><span class="sxs-lookup"><span data-stu-id="f1ce8-105">**Logical** functions</span></span>
* <span data-ttu-id="f1ce8-106">ฟังก์ชัน**ข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="f1ce8-106">**Information** functions</span></span>
* <span data-ttu-id="f1ce8-107">ฟังก์ชัน**ข้อความ**</span><span class="sxs-lookup"><span data-stu-id="f1ce8-107">**Text** functions</span></span>
* <span data-ttu-id="f1ce8-108">ฟังก์ชัน**วันที่**</span><span class="sxs-lookup"><span data-stu-id="f1ce8-108">**Date** functions</span></span>

<span data-ttu-id="f1ce8-109">เช่นเดียวกับ Excel เมื่อคุณเริ่มพิมพ์สูตรของคุณใน **แถบสูตร** ของ Power BI Desktop รายการของฟังก์ชันที่พร้อมใช้งานจะปรากฏขึ้นมาเพื่อช่วยให้คุณระบุว่าฟังก์ชันที่มีให้ฟังก์ชันใดที่คุณต้องการเลือก</span><span class="sxs-lookup"><span data-stu-id="f1ce8-109">Similar to Excel, when you start typing your formula into the Power BI Desktop **Formula Bar**, a list of available functions appears to help you determine which available function you want to select.</span></span> <span data-ttu-id="f1ce8-110">และด้วยการใช้แป้นลูกศร **ขึ้น** และ **ลง** บนคีย์บอร์ด คุณสามารถเน้นฟังก์ชันที่มีให้ได้ และคำอธิบายสั้นๆ จะแสดงขึ้นมา</span><span class="sxs-lookup"><span data-stu-id="f1ce8-110">And by using the **up** and **down** arrow keys on your keyboard, you can highlight any of the available functions, and a brief description is displayed.</span></span>

<span data-ttu-id="f1ce8-111">Power BI แสดงฟังก์ชันที่ตรงกับตัวอักษรที่คุณพิมพ์ ดังนั้นถ้าคุณพิมพ์ *S* เฉพาะฟังก์ชันที่ขึ้นต้นด้วย *S* จะปรากฏขึ้นมาบนรายการ</span><span class="sxs-lookup"><span data-stu-id="f1ce8-111">Power BI displays the functions that match the letters you've typed so far, so if you type *S* only functions that begin with *S* appear in the list.</span></span> <span data-ttu-id="f1ce8-112">ถ้าคุณพิมพ์ *Su* เฉพาะฟังก์ชันที่*มี*ลำดับตัวอักษร *Su* ในชื่อจะปรากฏขึ้นมาบนรายการ (ฟังก์ชันไม่จำเป็นต้องขึ้นต้นด้วย *Su* แต่เพียงต้องมีลำดับตัวอักษรนี้เท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="f1ce8-112">If you type *Su*, only functions that *contain* the letter sequence *Su* in their name appear in the list (they don't have to start with *Su*, they just have to contain that letter sequence).</span></span>

![](media/7-3-dax-functions/dax-functions_1.png)

<span data-ttu-id="f1ce8-113">การทดลองกับ DAX ด้วยวิธีนี้และการค้นหาแต่ละฟังก์ชัน DAX ที่พร้อมใช้งานใน Power BI เป็นเรื่องง่าย</span><span class="sxs-lookup"><span data-stu-id="f1ce8-113">It's easy to experiment with DAX in this way, and to find each of the various DAX functions that are available in Power BI.</span></span> <span data-ttu-id="f1ce8-114">สิ่งที่คุณต้องทำมีเพียงเริ่มพิมพ์ และ Power BI จะช่วยคุณที่เหลือเอง</span><span class="sxs-lookup"><span data-stu-id="f1ce8-114">All you have to do is start typing, and Power BI helps you along.</span></span>

<span data-ttu-id="f1ce8-115">ในเมื่อเรารู้วิธีเริ่มต้นสูตร DAX แล้ว ลองมาดูประเภทฟังก์ชันแต่ละประเภทกัน</span><span class="sxs-lookup"><span data-stu-id="f1ce8-115">Now that we know how to get that DAX formula started, let's take a look at each of these function categories in turn.</span></span>

## <a name="aggregation-functions"></a><span data-ttu-id="f1ce8-116">ฟังก์ชันการรวม</span><span class="sxs-lookup"><span data-stu-id="f1ce8-116">Aggregation functions</span></span>
<span data-ttu-id="f1ce8-117">DAX มีฟังก์ชัน**การรวม**อยู่จำนวนหนึ่ง รวมถึงฟังก์ชันที่ใช้บ่อยต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f1ce8-117">DAX has a number of **aggregation** functions, including the following commonly used functions:</span></span>

* <span data-ttu-id="f1ce8-118">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="f1ce8-118">SUM</span></span>
* <span data-ttu-id="f1ce8-119">AVERAGE</span><span class="sxs-lookup"><span data-stu-id="f1ce8-119">AVERAGE</span></span>
* <span data-ttu-id="f1ce8-120">MIN</span><span class="sxs-lookup"><span data-stu-id="f1ce8-120">MIN</span></span>
* <span data-ttu-id="f1ce8-121">MAX</span><span class="sxs-lookup"><span data-stu-id="f1ce8-121">MAX</span></span>
* <span data-ttu-id="f1ce8-122">SUMX (และฟังก์ชัน *X* อื่นๆ)</span><span class="sxs-lookup"><span data-stu-id="f1ce8-122">SUMX (and other *X* functions)</span></span>

<span data-ttu-id="f1ce8-123">ฟังก์ชันเหล่านี้ทำงานกับคอลัมน์ตัวเลขเท่านั้น และมักจะรวมได้เพียงทีละคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="f1ce8-123">These functions work only on numeric columns, and generally can aggregate only one column at a time.</span></span>

<span data-ttu-id="f1ce8-124">อย่างไรก็ตาม ฟังก์ชันการรวมพิเศษที่ลงท้ายด้วย **X** เช่น **SUMX** สามารถทำงานกับหลายคอลัมน์ได้</span><span class="sxs-lookup"><span data-stu-id="f1ce8-124">However, special aggregation functions that end in **X**, such as **SUMX**, can work on multiple columns.</span></span> <span data-ttu-id="f1ce8-125">ฟังก์ชันเหล่านี้จะทำซ้ำตลอดทั้งตาราง และคำนวณนิพจน์ในแต่ละแถว</span><span class="sxs-lookup"><span data-stu-id="f1ce8-125">These functions iterate through the table, and evaluate the expression for each row.</span></span>

## <a name="counting-functions"></a><span data-ttu-id="f1ce8-126">ฟังก์ชันการตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="f1ce8-126">Counting functions</span></span>
<span data-ttu-id="f1ce8-127">ฟังก์ชัน**การตรวจนับ**ที่ใช้บ่อยใน DAX รวมถึงฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f1ce8-127">Often-used **counting** functions in DAX include the following:</span></span>

* <span data-ttu-id="f1ce8-128">COUNT</span><span class="sxs-lookup"><span data-stu-id="f1ce8-128">COUNT</span></span>
* <span data-ttu-id="f1ce8-129">COUNTA</span><span class="sxs-lookup"><span data-stu-id="f1ce8-129">COUNTA</span></span>
* <span data-ttu-id="f1ce8-130">COUNTBLANK</span><span class="sxs-lookup"><span data-stu-id="f1ce8-130">COUNTBLANK</span></span>
* <span data-ttu-id="f1ce8-131">COUNTROWS</span><span class="sxs-lookup"><span data-stu-id="f1ce8-131">COUNTROWS</span></span>
* <span data-ttu-id="f1ce8-132">DISTINCTCOUNT</span><span class="sxs-lookup"><span data-stu-id="f1ce8-132">DISTINCTCOUNT</span></span>

<span data-ttu-id="f1ce8-133">ฟังก์ชันเหล่านี้จะนับองค์ประกอบที่แตกต่างกัน เช่น ค่าเฉพาะ ค่าที่ไม่ว่าง และแถวของตาราง</span><span class="sxs-lookup"><span data-stu-id="f1ce8-133">These functions count different elements, such as distinct values, non-empty values, and table rows.</span></span>

## <a name="logical-functions"></a><span data-ttu-id="f1ce8-134">ฟังก์ชันตรรกะ</span><span class="sxs-lookup"><span data-stu-id="f1ce8-134">Logical functions</span></span>
<span data-ttu-id="f1ce8-135">ฟังก์ชัน**ตรรกะ**ใน DAX ประกอบด้วย:</span><span class="sxs-lookup"><span data-stu-id="f1ce8-135">The collection of **logical** functions in DAX include:</span></span>

* <span data-ttu-id="f1ce8-136">และ</span><span class="sxs-lookup"><span data-stu-id="f1ce8-136">AND</span></span>
* <span data-ttu-id="f1ce8-137">OR</span><span class="sxs-lookup"><span data-stu-id="f1ce8-137">OR</span></span>
* <span data-ttu-id="f1ce8-138">NOT</span><span class="sxs-lookup"><span data-stu-id="f1ce8-138">NOT</span></span>
* <span data-ttu-id="f1ce8-139">IF</span><span class="sxs-lookup"><span data-stu-id="f1ce8-139">IF</span></span>
* <span data-ttu-id="f1ce8-140">IFERROR</span><span class="sxs-lookup"><span data-stu-id="f1ce8-140">IFERROR</span></span>

<span data-ttu-id="f1ce8-141">ฟังก์ชันพิเศษเหล่านี้สามารถแสดงด้วย*ตัวดำเนินการ*ได้</span><span class="sxs-lookup"><span data-stu-id="f1ce8-141">These special functions can also be expressed with *operators*.</span></span> <span data-ttu-id="f1ce8-142">ตัวอย่างเช่น **AND** สามารถพิมพ์เป็น (แทนที่ด้วย) **&&** ในสูตร DAX ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f1ce8-142">For example, **AND** can be typed as (replaced with) **&&** in your DAX formula.</span></span>

<span data-ttu-id="f1ce8-143">คุณสามารถใช้ตัวดำเนินการ (เช่น **&&** ) เมื่อคุณต้องการเงื่อนไขมากกว่าสองเงื่อนไขในสูตรของคุณ มิฉะนั้น วิธีปฏิบัติที่ดีที่สุดคือการใช้ชื่อฟังก์ชันนั้น (เช่น **AND**) เพื่อให้โค้ด DAX ของคุณอ่านได้ง่าย</span><span class="sxs-lookup"><span data-stu-id="f1ce8-143">You can use operators (such as **&&**) when you need more than two conditions in your formula, but otherwise, it's best practice use the function name itself (such as **AND**) for readability of your DAX code.</span></span>

## <a name="information-functions"></a><span data-ttu-id="f1ce8-144">ฟังก์ชันข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f1ce8-144">Information functions</span></span>
<span data-ttu-id="f1ce8-145">ฟังก์ชัน**ข้อมูล**ใน DAX ประกอบด้วย:</span><span class="sxs-lookup"><span data-stu-id="f1ce8-145">**Information** functions in DAX include:</span></span>

* <span data-ttu-id="f1ce8-146">ISBLANK</span><span class="sxs-lookup"><span data-stu-id="f1ce8-146">ISBLANK</span></span>
* <span data-ttu-id="f1ce8-147">ISNUMBER</span><span class="sxs-lookup"><span data-stu-id="f1ce8-147">ISNUMBER</span></span>
* <span data-ttu-id="f1ce8-148">ISTEXT</span><span class="sxs-lookup"><span data-stu-id="f1ce8-148">ISTEXT</span></span>
* <span data-ttu-id="f1ce8-149">ISNONTEXT</span><span class="sxs-lookup"><span data-stu-id="f1ce8-149">ISNONTEXT</span></span>
* <span data-ttu-id="f1ce8-150">ISERROR</span><span class="sxs-lookup"><span data-stu-id="f1ce8-150">ISERROR</span></span>

<span data-ttu-id="f1ce8-151">แม้ฟังก์ชันเหล่านี้อาจมีประโยชน์ในบางสถานการณ์ คุณก็ควรรู้จักชนิดข้อมูลของคอลัมน์ของคุณล่วงหน้าแทนที่จะพึ่งพาฟังก์ชันเหล่านี้ให้ระบุชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f1ce8-151">While these functions can be situationally useful, there is value in knowing the data type of your columns ahead of time, rather than depending on these functions to provide the data type.</span></span>

<span data-ttu-id="f1ce8-152">DAX ใช้ฟังก์ชัน **MAX** และ **MIN** เพื่อ*รวม*ค่า และเพื่อ*เปรียบเทียบ*ค่า</span><span class="sxs-lookup"><span data-stu-id="f1ce8-152">DAX uses the **MAX** and **MIN** functions to both *aggregate* values, and to *compare* values.</span></span>

## <a name="text-functions"></a><span data-ttu-id="f1ce8-153">ฟังก์ชันข้อความ</span><span class="sxs-lookup"><span data-stu-id="f1ce8-153">Text functions</span></span>
<span data-ttu-id="f1ce8-154">ฟังก์ชัน**ข้อความ**ใน DAX มีดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f1ce8-154">The **text** functions in DAX include the following:</span></span>

* <span data-ttu-id="f1ce8-155">CONCATENTATE</span><span class="sxs-lookup"><span data-stu-id="f1ce8-155">CONCATENTATE</span></span>
* <span data-ttu-id="f1ce8-156">REPLACE</span><span class="sxs-lookup"><span data-stu-id="f1ce8-156">REPLACE</span></span>
* <span data-ttu-id="f1ce8-157">SEARCH</span><span class="sxs-lookup"><span data-stu-id="f1ce8-157">SEARCH</span></span>
* <span data-ttu-id="f1ce8-158">UPPER</span><span class="sxs-lookup"><span data-stu-id="f1ce8-158">UPPER</span></span>
* <span data-ttu-id="f1ce8-159">FIXED</span><span class="sxs-lookup"><span data-stu-id="f1ce8-159">FIXED</span></span>

<span data-ttu-id="f1ce8-160">**ข้อความ**เหล่านี้ทำงานคล้ายกับฟังก์ชัน Excel ที่มีชื่อเดียวกัน ดังนั้นหากคุณคุ้นเคยกับวิธีที่ Excel จัดการกับฟังก์ชันข้อความ คุณก็ก้าวนำไปหนึ่งก้าวแล้ว</span><span class="sxs-lookup"><span data-stu-id="f1ce8-160">These **text** work very similarly to the Excel functions that have the same name, so if you're familiar with how Excel handles text functions, you're already a step ahead.</span></span> <span data-ttu-id="f1ce8-161">หากคุณไม่คุ้นเคย คุณสามารถทดลองฟังก์ชันเหล่านี้ได้ตลอดเวลาใน Power BI และเรียนรู้เพิ่มเติมเกี่ยวกับลักษณะการทำงานของฟังก์ชันเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="f1ce8-161">If not, you can always experiment with these functions in Power BI, and learn more about how they behave.</span></span>

## <a name="date-functions"></a><span data-ttu-id="f1ce8-162">ฟังก์ชันวันที่</span><span class="sxs-lookup"><span data-stu-id="f1ce8-162">Date functions</span></span>
<span data-ttu-id="f1ce8-163">ใน DAX มีฟังก์ชัน**วันที่**ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f1ce8-163">DAX includes the following **Date** functions:</span></span>

* <span data-ttu-id="f1ce8-164">DATE</span><span class="sxs-lookup"><span data-stu-id="f1ce8-164">DATE</span></span>
* <span data-ttu-id="f1ce8-165">HOUR</span><span class="sxs-lookup"><span data-stu-id="f1ce8-165">HOUR</span></span>
* <span data-ttu-id="f1ce8-166">NOW</span><span class="sxs-lookup"><span data-stu-id="f1ce8-166">NOW</span></span>
* <span data-ttu-id="f1ce8-167">EOMONTH</span><span class="sxs-lookup"><span data-stu-id="f1ce8-167">EOMONTH</span></span>
* <span data-ttu-id="f1ce8-168">WEEKDAY</span><span class="sxs-lookup"><span data-stu-id="f1ce8-168">WEEKDAY</span></span>

<span data-ttu-id="f1ce8-169">แม้ฟังก์ชันเหล่านี้จะมีประโยชน์ในการคำนวณและดึงข้อมูลจากค่า*วันที่* แต่ฟังก์ชันเหล่านี้ใช้กับตัวแสดงเวลาที่ใช้ตารางวันที่ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="f1ce8-169">While these functions are useful to calculate and extract information from *date* values, they do not apply to time intelligence, which uses a date table.</span></span>

> <span data-ttu-id="f1ce8-170">เนื้อหาวิดีโอโดย [Alberto Ferrari, SQBI](https://www.sqlbi.com/learning-dax)</span><span class="sxs-lookup"><span data-stu-id="f1ce8-170">Video content courtesy of [Alberto Ferrari, SQLBI](https://www.sqlbi.com/learning-dax)</span></span>
> 
> 

