---
title: ใช้ตัวแบ่งส่วนข้อมูลช่วงตัวเลขใน Power BI
description: เรียนรู้วิธีการใช้ตัวแบ่งส่วนข้อมูลสำหรับกำหนดข้อจำกัดไปยังช่วงตัวเลขใน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: zIZPA0UrJyA
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 04/06/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 83ba0234ef4f4e350f413f3c934e2f09f0a9a3f2
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412793"
---
# <a name="use-the-numeric-range-slicer-in-power-bi"></a><span data-ttu-id="8759c-103">ใช้ตัวแบ่งส่วนข้อมูลช่วงตัวเลขใน Power BI</span><span class="sxs-lookup"><span data-stu-id="8759c-103">Use the numeric range slicer in Power BI</span></span>

<span data-ttu-id="8759c-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-desktop](../includes/yes-desktop.md)] [!INCLUDE [yes-service](../includes/yes-service.md)]</span><span class="sxs-lookup"><span data-stu-id="8759c-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-desktop](../includes/yes-desktop.md)] [!INCLUDE [yes-service](../includes/yes-service.md)]</span></span>

<span data-ttu-id="8759c-105">ด้วยตัวแบ่งส่วนข้อมูลช่วงตัวเลข คุณสามารถใช้ตัวกรองทุกประเภทในคอลัมน์ตัวเลขใดก็ตามในแบบจำลองข้อมูลของคุณได้</span><span class="sxs-lookup"><span data-stu-id="8759c-105">With the numeric range slicer, you can apply all sorts of filters to any numeric column in your data model.</span></span> <span data-ttu-id="8759c-106">มีสามตัวเลือกสำหรับการกรองข้อมูลตัวเลขของคุณ: ระหว่างตัวเลขน้อยกว่าหรือเท่ากับตัวเลข หรือมากกว่าหรือเท่ากับตัวเลข</span><span class="sxs-lookup"><span data-stu-id="8759c-106">There are three options for filtering your numeric data: between numbers, less than or equal to a number, or greater than or equal to a number.</span></span> <span data-ttu-id="8759c-107">เทคนิคง่าย ๆ นี้เป็นวิธีที่มีประสิทธิภาพในการกรองข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="8759c-107">This simple technique is a powerful way to filter your data.</span></span>

![วิชวลที่มีตัวแบ่งส่วนช่วงตัวเลข](media/desktop-slicer-numeric-range/desktop-slicer-numeric-range-0.png)

## <a name="video"></a><span data-ttu-id="8759c-109">Video</span><span class="sxs-lookup"><span data-stu-id="8759c-109">Video</span></span>

<span data-ttu-id="8759c-110">ในวิดีโอนี้ จะแสดงการสร้างตัวแบ่งส่วนข้อมูลช่วงตัวเลข</span><span class="sxs-lookup"><span data-stu-id="8759c-110">In this video, Will walks through creating a numeric range slicer.</span></span>

> [!NOTE]
> <span data-ttu-id="8759c-111">วิดีโอนี้ใช้ Power BI Desktop เวอร์ชันเก่า</span><span class="sxs-lookup"><span data-stu-id="8759c-111">This video uses an older version of Power BI Desktop.</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/zIZPA0UrJyA" frameborder="0" allowfullscreen></iframe> 


## <a name="add-a-numeric-range-slicer"></a><span data-ttu-id="8759c-112">เพิ่มตัวแบ่งส่วนข้อมูลช่วงตัวเลข</span><span class="sxs-lookup"><span data-stu-id="8759c-112">Add a numeric range slicer</span></span>

<span data-ttu-id="8759c-113">คุณสามารถใช้ตัวแบ่งส่วนข้อมูลช่วงตัวเลขได้เช่นเดียวกับที่คุณใช้ตัวแบ่งส่วนข้อมูลอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="8759c-113">You can use the numeric range slicer like you would use any other slicer.</span></span> <span data-ttu-id="8759c-114">เพียงแค่สร้างวิชวล **ตัวแบ่งส่วนข้อมูล** สำหรับรายงานของคุณ จากนั้นเลือกค่าตัวเลขสำหรับค่า **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="8759c-114">Just create a **Slicer** visual for your report, and then select a numeric value for the **Field** value.</span></span> <span data-ttu-id="8759c-115">ในรูปต่อไปนี้ เราได้เลือกเขตข้อมูล **LineTotal**</span><span class="sxs-lookup"><span data-stu-id="8759c-115">In the following image, we selected the **LineTotal** field.</span></span>

![สร้างตัวแบ่งส่วนช่วงตัวเลข](media/desktop-slicer-numeric-range/desktop-slicer-numeric-range-1-create.png)

<span data-ttu-id="8759c-117">เลือกลูกศรชี้ลงที่มุมบนขวาของตัวแบ่งส่วนช่วงตัวเลขและเมนูจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="8759c-117">Select the down-arrow in the upper-right corner of the numeric range slicer and a menu appears.</span></span>

![เมนูตัวแบ่งส่วนช่วงตัวเลข](media/desktop-slicer-numeric-range/desktop-slicer-numeric-range-2-between.png)

<span data-ttu-id="8759c-119">สำหรับช่วงตัวเลข คุณสามารถเลือกจากตัวเลือกทั้งสามต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8759c-119">For the numeric range, you can select from the following three options:</span></span>

* <span data-ttu-id="8759c-120">**ระหว่าง**</span><span class="sxs-lookup"><span data-stu-id="8759c-120">**Between**</span></span>
* <span data-ttu-id="8759c-121">**น้อยกว่าหรือเท่ากับ**</span><span class="sxs-lookup"><span data-stu-id="8759c-121">**Less than or equal to**</span></span>
* <span data-ttu-id="8759c-122">**มากกว่าหรือเท่ากับ**</span><span class="sxs-lookup"><span data-stu-id="8759c-122">**Greater than or equal to**</span></span>

<span data-ttu-id="8759c-123">เมื่อคุณเลือก **ระหว่าง** จากเมนู แถบเลื่อนจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="8759c-123">When you select **Between** from the menu, a slider appears.</span></span> <span data-ttu-id="8759c-124">คุณสามารถใช้แถบเลื่อนเพื่อเลือกค่าตัวเลขที่อยู่ระหว่างตัวเลขต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="8759c-124">You can use the slider to select numeric values that fall between the numbers.</span></span> <span data-ttu-id="8759c-125">บางครั้งส่วนประกอบของการย้ายแถบตัวแบ่งส่วนข้อมูลจะทำให้ยากต่อการใช้ตัวเลขนั้น</span><span class="sxs-lookup"><span data-stu-id="8759c-125">Sometimes the granularity of moving the slicer bar makes it difficult to land exactly on that number.</span></span> <span data-ttu-id="8759c-126">คุณยังสามารถใช้แถบเลื่อนและเลือกกล่องใดก็ได้เพื่อพิมพ์ค่าที่เราต้องการ</span><span class="sxs-lookup"><span data-stu-id="8759c-126">You can also use the slider and select either box to type in the values we want.</span></span> <span data-ttu-id="8759c-127">ตัวเลือกนี้จะสะดวกเมื่อคุณต้องการแบ่งย่อยในตัวเลขที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="8759c-127">This option is convenient when you want to slice on specific numbers.</span></span>

<span data-ttu-id="8759c-128">ในรูปต่อไปนี้ หน้ารายงานจะกรองด้วยค่า **LineTotal** ที่อยู่ในช่วงระหว่าง 2500.00 และ 6000.00</span><span class="sxs-lookup"><span data-stu-id="8759c-128">In the following image, the report page filters for **LineTotal** values that range between 2500.00 and 6000.00.</span></span>

![ตัวแบ่งส่วนตัวเลขที่ใช้ช่วงระหว่าง](media/desktop-slicer-numeric-range/desktop-slicer-numeric-range-3-between-range.png)

<span data-ttu-id="8759c-130">เมื่อคุณเลือก **น้อยกว่าหรือเท่ากับ** ด้ามจับที่ด้านซ้าย (ค่าต่ำกว่า) ของแถบเลื่อนจะหายไป และคุณสามารถปรับเปลี่ยนเฉพาะขีดจำกัดขอบสูงสุดของแถบเลื่อนดังกล่าวได้</span><span class="sxs-lookup"><span data-stu-id="8759c-130">When you select **Less than or equal to**, the left (lower value) handle of the slider bar disappears, and you can adjust only the upper-bound limit of the slider bar.</span></span> <span data-ttu-id="8759c-131">ในรูปต่อไปนี้ เราตั้งค่าแถบเลื่อนเป็น 5928.19</span><span class="sxs-lookup"><span data-stu-id="8759c-131">In the following image, we set the slider bar maximum to 5928.19.</span></span>

![ตัวแบ่งส่วนตัวเลขที่ใช้น้อยกว่า](media/desktop-slicer-numeric-range/desktop-slicer-numeric-range-4-less-than.png)

<span data-ttu-id="8759c-133">สุดท้ายถ้าคุณเลือก **มากกว่าหรือเท่ากับ** จากนั้นด้ามจับที่ด้านขวา (ค่าสูงกว่า) จะเลื่อนหายไป</span><span class="sxs-lookup"><span data-stu-id="8759c-133">Lastly, if you select **Greater than or equal to**, then the right (higher value) slider bar handle disappears.</span></span> <span data-ttu-id="8759c-134">จากนั้นคุณสามารถปรับค่าต่ำกว่าดังที่เห็นในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8759c-134">You can then adjust the lower value, as seen in the following image.</span></span> <span data-ttu-id="8759c-135">ตอนนี้ เฉพาะรายการที่มี **LineTotal** มากกว่าหรือเท่ากับ 4902.99 จะแสดงในภาพบนหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="8759c-135">Now, only items with a **LineTotal** greater than or equal to 4902.99 display in the visuals on the report page.</span></span>

![ตัวแบ่งส่วนตัวเลขที่ใช้มากกว่า](media/desktop-slicer-numeric-range/desktop-slicer-numeric-range-5-greater-than.png)

## <a name="snap-to-whole-numbers-with-the-numeric-range-slicer"></a><span data-ttu-id="8759c-137">จัดชิดเป็นเลขจำนวนเต็มด้วยตัวแบ่งส่วนช่วงตัวเลข</span><span class="sxs-lookup"><span data-stu-id="8759c-137">Snap to whole numbers with the numeric range slicer</span></span>

<span data-ttu-id="8759c-138">ตัวแบ่งส่วนช่วงตัวเลขจะจัดชิดเป็นเลขจำนวนเต็มถ้าชนิดข้อมูลของเขตข้อมูลเบื้องต้นเป็น *จำนวนเต็ม*</span><span class="sxs-lookup"><span data-stu-id="8759c-138">A numeric range slicer snaps to whole numbers if the data type of the underlying field is *Whole Number*.</span></span> <span data-ttu-id="8759c-139">คุณลักษณะนี้ช่วยให้ตัวแบ่งส่วนข้อมูลของคุณสามารถจัดพอดีกับจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="8759c-139">This feature lets your slicer cleanly align to whole numbers.</span></span> <span data-ttu-id="8759c-140">เขตข้อมูล *ตัวเลขทศนิยม* ช่วยให้คุณสามารถป้อนหรือเลือกเศษส่วนของจำนวนได้</span><span class="sxs-lookup"><span data-stu-id="8759c-140">*Decimal Number* fields let you enter or select fractions of a number.</span></span> <span data-ttu-id="8759c-141">การจัดรูปแบบที่ตั้งค่าในกล่องข้อความตรงกับชุดการจัดรูปแบบในเขตข้อมูล แม้ว่าคุณจะสามารถพิมพ์ลงหรือเลือกตัวเลขที่เที่ยงตรงกว่าได้</span><span class="sxs-lookup"><span data-stu-id="8759c-141">The formatting set in the text box matches the formatting set on the field, even though you can type in or select more precise numbers.</span></span>

## <a name="display-formatting-with-the-date-range-slicer"></a><span data-ttu-id="8759c-142">แสดงการจัดรูปแบบด้วยตัวแบ่งส่วนข้อมูลช่วงวันที่</span><span class="sxs-lookup"><span data-stu-id="8759c-142">Display formatting with the date range slicer</span></span>

<span data-ttu-id="8759c-143">เมื่อคุณใช้ตัวแบ่งส่วนข้อมูลเพื่อแสดงหรือตั้งค่าช่วงวันที่ วันที่จะแสดงในรูปแบบ *วันที่แบบสั้น*</span><span class="sxs-lookup"><span data-stu-id="8759c-143">When you use a slicer to display or set a range of dates, the dates display in the *Short Date* format.</span></span> <span data-ttu-id="8759c-144">ตำแหน่งที่ตั้งของเบราว์เซอร์หรือระบบปฏิบัติการของผู้ใช้จะกำหนดรูปแบบวันที่</span><span class="sxs-lookup"><span data-stu-id="8759c-144">The user's browser or operating system locale determine the date format.</span></span> <span data-ttu-id="8759c-145">ดังนั้น รูปแบบนี้จะเป็นรูปแบบการแสดงผล ไม่ว่าจะเป็นการตั้งค่าชนิดข้อมูลสำหรับข้อมูลเบื้องต้นหรือแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="8759c-145">As such, it will be the display format no matter what the data type settings are for the underlying data or model.</span></span>

<span data-ttu-id="8759c-146">ตัวอย่างเช่น คุณสามารถใช้รูปแบบวันที่แบบยาวสำหรับชนิดข้อมูลเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="8759c-146">You could, for example, have a long date format for the underlying data type.</span></span> <span data-ttu-id="8759c-147">ในกรณีนี้ รูปแบบวันที่เช่น  *dddd, MMMM d, yyyy* จะจัดรูปแบบวันที่ในภาพหรือสถานการณ์อื่นๆ *เป็นวันพุธที่ 14 มีนาคม 2001*</span><span class="sxs-lookup"><span data-stu-id="8759c-147">In this case, a date format such as *dddd, MMMM d, yyyy* would format a date in other visuals or circumstances as *Wednesday, March 14, 2001*.</span></span> <span data-ttu-id="8759c-148">แต่ในตัวแบ่งส่วนข้อมูลวันที่ วันที่นั้นจะแสดงในตัวแบ่งส่วนข้อมูลเป็น *03/14/2001*</span><span class="sxs-lookup"><span data-stu-id="8759c-148">But in the date range slicer, that date displays in the slicer as *03/14/2001*.</span></span>

<span data-ttu-id="8759c-149">การแสดงรูปแบบวันที่แบบสั้นในตัวแบ่งส่วนข้อมูลเพื่อให้มั่นใจถึงความยาวของสตริงคงที่และกระชับภายในตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8759c-149">Displaying the Short Date format in the slicer ensures the length of the string stays consistent and compact within the slicer.</span></span>

## <a name="limitations-and-considerations"></a><span data-ttu-id="8759c-150">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="8759c-150">Limitations and considerations</span></span>

<span data-ttu-id="8759c-151">ข้อจำกัดและข้อควรพิจารณาต่อไปนี้จะใช้กับตัวแบ่งส่วนข้อมูลช่วงตัวเลข:</span><span class="sxs-lookup"><span data-stu-id="8759c-151">The following limitations and considerations apply to the numeric range slicer:</span></span>

* <span data-ttu-id="8759c-152">ตัวแบ่งส่วนข้อมูลช่วงตัวเลขจะกรองทุกแถวต้นแบบในข้อมูลดังกล่าว ไม่ใช่ค่ารวมใด ๆ</span><span class="sxs-lookup"><span data-stu-id="8759c-152">The numeric range slicer filters every underlying row in the data, not any aggregated value.</span></span> <span data-ttu-id="8759c-153">ตัวอย่างเช่น สมมติว่าคุณใช้เขตข้อมูล *ยอดขาย*</span><span class="sxs-lookup"><span data-stu-id="8759c-153">For example, let's say that you use a *Sales Amount* field.</span></span> <span data-ttu-id="8759c-154">จากนั้นตัวแบ่งส่วนข้อมูลจะกรองธุรกรรมแต่ละรายการตามยอดขาย ไม่ใช่ผลรวมของยอดขายสำหรับแต่ละจุดข้อมูลของภาพ</span><span class="sxs-lookup"><span data-stu-id="8759c-154">The slicer then filters each transaction based on the sales amount, not the sum of the sales amount for each data point of a visual.</span></span>
* <span data-ttu-id="8759c-155">ปัจจุบันยังไม่สามารถทำงานร่วมกับหน่วยวัดได้</span><span class="sxs-lookup"><span data-stu-id="8759c-155">It doesn't currently work with measures.</span></span>
* <span data-ttu-id="8759c-156">คุณสามารถพิมพ์ตัวเลขต่าง ๆ ลงในตัวแบ่งส่วนตัวเลขได้ แม้ว่าจะอยู่นอกช่วงของค่าในคอลัมน์อ้างอิงก็ตาม</span><span class="sxs-lookup"><span data-stu-id="8759c-156">You can type any number into a numeric slicer, even if it is outside the range of values in the underlying column.</span></span> <span data-ttu-id="8759c-157">ตัวเลือกนี้จะช่วยให้คุณสามารถตั้งค่าตัวกรองได้ หากคุณทราบว่าข้อมูลอาจมีการเปลี่ยนแปลงในอนาคต</span><span class="sxs-lookup"><span data-stu-id="8759c-157">This option lets you set up filters if you know the data may change in future.</span></span>
