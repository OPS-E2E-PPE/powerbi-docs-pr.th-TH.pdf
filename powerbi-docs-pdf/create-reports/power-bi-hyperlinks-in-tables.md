---
title: เพิ่มไฮเปอร์ลิงก์ (URL) ไปยังตารางหรือเมทริกซ์
description: หัวข้อนี้จะสอนวิธีเพิ่มไฮเปอร์ลิงก์ (URL) ไปยังตาราง คุณใช้ Power BI Desktop เพื่อเพิ่มไฮเปอร์ลิงก์ (URL) ไปยังชุดข้อมูล จากนั้น ใน Power BI Desktop หรือบริการของ Power BI คุณสามารถเพิ่มไฮเปอร์ลิงก์เหล่านั้นไปยังตารางหรือเมทริกซ์รายงานของคุณได้
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 10/15/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: c60c5824f20edd6d596d23fed56f8cdfaa19a01a
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418060"
---
# <a name="add-hyperlinks-urls-to-a-table-or-matrix"></a><span data-ttu-id="d29ca-105">เพิ่มไฮเปอร์ลิงก์ (URL) ไปยังตารางหรือเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="d29ca-105">Add hyperlinks (URLs) to a table or matrix</span></span>
<span data-ttu-id="d29ca-106">หัวข้อนี้จะสอนวิธีเพิ่มไฮเปอร์ลิงก์ (URL) ไปยังตาราง</span><span class="sxs-lookup"><span data-stu-id="d29ca-106">This topic teaches how to add hyperlinks (URLs) to a table.</span></span> <span data-ttu-id="d29ca-107">คุณใช้ Power BI Desktop เพื่อเพิ่มไฮเปอร์ลิงก์ (URL) ไปยังชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d29ca-107">You use Power BI Desktop to add hyperlinks (URLs) to a dataset.</span></span> <span data-ttu-id="d29ca-108">คุณสามารถเพิ่มไฮเปอร์ลิงก์เหล่านั้นไปยังตารางหรือเมทริกซ์รายงานของคุณได้ในทั้ง Power BI Desktop หรือบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="d29ca-108">You can add those hyperlinks to your report tables and matrixes in either Power BI Desktop or the Power BI service.</span></span> <span data-ttu-id="d29ca-109">จากนั้น คุณสามารถแสดงไอคอนของ URL หรือลิงก์ หรือจัดรูปแบบคอลัมน์อื่นเป็นข้อความลิงก์ได้</span><span class="sxs-lookup"><span data-stu-id="d29ca-109">Then you can display the URL or a link icon, or format another column as link text.</span></span>

![ตารางที่มีไฮเปอร์ลิงก์](media/power-bi-hyperlinks-in-tables/power-bi-url-link-text.png)

<span data-ttu-id="d29ca-111">คุณยังสามารถสร้างไฮเปอร์ลิงก์ใน [กล่องข้อความในรายงาน](service-add-hyperlink-to-text-box.md) ในบริการของ Power BI และ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d29ca-111">You can also create hyperlinks in [text boxes in reports](service-add-hyperlink-to-text-box.md) in the Power BI service and Power BI Desktop.</span></span> <span data-ttu-id="d29ca-112">และในบริการ Power BI คุณสามารถเพิ่มไฮเปอร์ลิงก์ไปยัง [ไทล์บนแดชบอร์ด](service-dashboard-edit-tile.md) และ [กล่องข้อความบนแดชบอร์ด](service-dashboard-add-widget.md)</span><span class="sxs-lookup"><span data-stu-id="d29ca-112">And in the Power BI service, you can add hyperlinks to [tiles on dashboards](service-dashboard-edit-tile.md) and to [text boxes on dashboards](service-dashboard-add-widget.md).</span></span> 


## <a name="format-a-url-as-a-hyperlink-in-power-bi-desktop"></a><span data-ttu-id="d29ca-113">จัดรูปแบบ URL เป็นไฮเปอร์ลิงก์ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d29ca-113">Format a URL as a hyperlink in Power BI Desktop</span></span>

<span data-ttu-id="d29ca-114">คุณสามารถจัดรูปแบบเขตข้อมูล URL เป็นไฮเปอร์ลิงก์ได้ใน Power BI Desktop แต่ไม่สามารถทำได้ในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="d29ca-114">You can format a field with URLs as hyperlinks in Power BI Desktop, but not in the Power BI service.</span></span> <span data-ttu-id="d29ca-115">คุณยังสามารถ [จัดรูปแบบไฮเปอร์ลิงก์ใน Excel Power Pivot](#create-a-table-or-matrix-hyperlink-in-excel-power-pivot) ก่อนนำเข้าเวิร์กบุ๊กไปยัง Power BI.</span><span class="sxs-lookup"><span data-stu-id="d29ca-115">You can also [format hyperlinks in Excel Power Pivot](#create-a-table-or-matrix-hyperlink-in-excel-power-pivot) before you import the workbook into Power BI.</span></span>

1. <span data-ttu-id="d29ca-116">ใน Power BI Desktop ถ้าเขตข้อมูลที่มีไฮเปอร์ลิงก์ไม่ปรากฏในชุดข้อมูลของคุณอยู่แล้ว ให้เพิ่ทเป็น[คอลัมน์แบบกำหนดเอง](../transform-model/desktop-common-query-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="d29ca-116">In Power BI Desktop, if a field with a hyperlink doesn't already exist in your dataset, add it as a [custom column](../transform-model/desktop-common-query-tasks.md).</span></span>

    > [!NOTE]
    > <span data-ttu-id="d29ca-117">คุณไม่สามารถสร้างคอลัมน์ในโหมด DirectQuery ได้</span><span class="sxs-lookup"><span data-stu-id="d29ca-117">You can't create a column in DirectQuery mode.</span></span>  <span data-ttu-id="d29ca-118">แต่ถ้าข้อมูลของคุณมี URL อยู่แล้ว คุณสามารถทำให้ URL เหล่านั้นเป็นไฮเปอร์ลิงก์ได้</span><span class="sxs-lookup"><span data-stu-id="d29ca-118">But if your data already contains URLs, you can turn them into hyperlinks.</span></span>

2. <span data-ttu-id="d29ca-119">ในมุมมองข้อมูลหรือมุมมองรายงาน ให้เลือกคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="d29ca-119">In Data view or Report view, select the column.</span></span> 

3. <span data-ttu-id="d29ca-120">บนแท็บ **การสร้างแบบจำลอง** เลือก **ประเภทข้อมูล** > **URL เว็บ**</span><span class="sxs-lookup"><span data-stu-id="d29ca-120">On the **Modeling** tab, select **Data Category** > **Web URL**.</span></span>
   
    ![รายการประเภทข้อมูลแบบดรอปดาวน์](media/power-bi-hyperlinks-in-tables/power-bi-format-web-url.png)

    > [!NOTE]
    > <span data-ttu-id="d29ca-122">URL ต้องเริ่มต้นด้วยเลขนำหน้าบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="d29ca-122">URLS must start with certain prefixes.</span></span> <span data-ttu-id="d29ca-123">โปรดดู [ข้อควรพิจารณาและข้อจำกัด](#considerations-and-troubleshooting) ในบทความนี้สำหรับรายการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d29ca-123">See [Considerations and troubleshooting](#considerations-and-troubleshooting) in this article for the complete list.</span></span>

## <a name="create-a-table-or-matrix-with-a-hyperlink"></a><span data-ttu-id="d29ca-124">สร้างตารางหรือเมทริกซ์ด้วยไฮเปอร์ลิงก์</span><span class="sxs-lookup"><span data-stu-id="d29ca-124">Create a table or matrix with a hyperlink</span></span>

1. <span data-ttu-id="d29ca-125">หลังจากคุณได้ [จัดรูปแบบไฮเปอร์ลิงก์เป็น URL](#format-a-url-as-a-hyperlink-in-power-bi-desktop) แล้ว ให้สลับไปที่มุมมองรายงาน</span><span class="sxs-lookup"><span data-stu-id="d29ca-125">After you've [formatted a hyperlink as a URL](#format-a-url-as-a-hyperlink-in-power-bi-desktop), switch to Report view.</span></span>
2. <span data-ttu-id="d29ca-126">สร้างตารางหรือเมทริกซ์ด้วยเขตข้อมูลที่คุณจัดหมวดหมู่เป็น URL เว็บ</span><span class="sxs-lookup"><span data-stu-id="d29ca-126">Create a table or matrix with the field that you categorized as a Web URL.</span></span> <span data-ttu-id="d29ca-127">ไฮเปอร์ลิงก์จะมีสีน้ำเงินและขีดเส้นใต้</span><span class="sxs-lookup"><span data-stu-id="d29ca-127">The hyperlinks are blue and underlined.</span></span>

    ![ลิงก์สีน้ำเงินและขีดเส้นใต้](media/power-bi-hyperlinks-in-tables/power-bi-url-blue-underline.png)


## <a name="display-a-hyperlink-icon-instead-of-a-url"></a><span data-ttu-id="d29ca-129">แสดงไฮเปอร์ลิงก์ไอคอนแทน URL</span><span class="sxs-lookup"><span data-stu-id="d29ca-129">Display a hyperlink icon instead of a URL</span></span>

<span data-ttu-id="d29ca-130">ถ้าคุณไม่ต้องการแสดง URL ยาวในตาราง คุณสามารถแสดงเป็นไฮเปอร์ลิงก์แทนได้</span><span class="sxs-lookup"><span data-stu-id="d29ca-130">If you don't want to display a long URL in a table, you can display a hyperlink icon</span></span> ![ไฮเปอร์ลิงก์ไอคอน](media/power-bi-hyperlinks-in-tables/power-bi-hyperlink-icon.png) <span data-ttu-id="d29ca-132">แทน</span><span class="sxs-lookup"><span data-stu-id="d29ca-132">instead.</span></span> 

> [!NOTE]
> <span data-ttu-id="d29ca-133">คุณไม่สามารถแสดงไอคอนในเมทริกซ์ได้</span><span class="sxs-lookup"><span data-stu-id="d29ca-133">You can't display icons in a matrix.</span></span>
   
1. <span data-ttu-id="d29ca-134">อันดับแรก [สร้างตารางที่มีไฮเปอร์ลิงก์](#create-a-table-or-matrix-with-a-hyperlink)</span><span class="sxs-lookup"><span data-stu-id="d29ca-134">First, [create a table with a hyperlink](#create-a-table-or-matrix-with-a-hyperlink).</span></span>

2. <span data-ttu-id="d29ca-135">เลือกตารางเพื่อเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d29ca-135">Select the table to make it active.</span></span>

    <span data-ttu-id="d29ca-136">เลือกไอคอน **จัดรูปแบบ** ![ไอคอนแปรงลูกกลิ้ง](media/power-bi-hyperlinks-in-tables/power-bi-paintroller.png) เพื่อเปิดแถบจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="d29ca-136">Select the **Format** icon ![Paint roller icon](media/power-bi-hyperlinks-in-tables/power-bi-paintroller.png) to open the Formatting tab.</span></span>

    <span data-ttu-id="d29ca-137">ขยาย **ค่า** ค้นหา **ไอคอน URL** และตั้งค่าการใช้งานเป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="d29ca-137">Expand **Values**, locate **URL icon**, and turn it to **On**.</span></span>

    ![เปิดไอคอน URL](media/power-bi-hyperlinks-in-tables/power-bi-url-icon-on.png)

1. <span data-ttu-id="d29ca-139">(ไม่บังคับ) [เผยแพร่รายงาน](desktop-upload-desktop-files.md) จาก Power BI Desktop ไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="d29ca-139">(Optional) [Publish the report](desktop-upload-desktop-files.md) from Power BI Desktop to the Power BI service.</span></span> <span data-ttu-id="d29ca-140">เมื่อคุณเปิดรายงานในบริการของ Power BI ไฮเปอร์ลิงก์จะทำงานด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="d29ca-140">When you open the report in the Power BI service, the hyperlinks work there, too.</span></span>

## <a name="format-link-text-as-a-hyperlink"></a><span data-ttu-id="d29ca-141">จัดรูปแบบข้อความลิงก์เป็นไฮเปอร์ลิงก์</span><span class="sxs-lookup"><span data-stu-id="d29ca-141">Format link text as a hyperlink</span></span>

<span data-ttu-id="d29ca-142">คุณยังสามารถจัดรูปแบบเขตข้อมูลอื่นในตารางเป็นไฮเปอร์ลิงก์และไม่มีคอลัมน์สำหรับ URL เลย</span><span class="sxs-lookup"><span data-stu-id="d29ca-142">You can also format another field in a table as the hyperlink, and not have a column for the URL at all.</span></span> <span data-ttu-id="d29ca-143">ในกรณีนี้ คุณไม่จัดรูปแบบคอลัมน์เป็น URL เว็บ</span><span class="sxs-lookup"><span data-stu-id="d29ca-143">In this case, you don't format the column as a Web URL.</span></span>

> [!NOTE]
> <span data-ttu-id="d29ca-144">คุณไม่สามารถจัดรูปแบบเขตข้อมูลอื่นเป็นไฮเปอร์ลิงก์ในเมทริกซ์ได้</span><span class="sxs-lookup"><span data-stu-id="d29ca-144">You can't format another field as the hyperlink in a matrix.</span></span>

1. <span data-ttu-id="d29ca-145">ในเขตข้อมูลที่ไม่มีไฮเปอร์ลิงก์ปรากฏในชุดข้อมูลของคุณ ให้ใช้ Power BI Desktop เพื่อเพิ่มเป็น [คอลัมน์แบบกำหนดเอง](../transform-model/desktop-common-query-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="d29ca-145">If a field with a hyperlink doesn't already exist in your dataset, use Power BI Desktop to add it as a [custom column](../transform-model/desktop-common-query-tasks.md).</span></span> <span data-ttu-id="d29ca-146">อีกครั้ง คุณไม่สามารถสร้างคอลัมน์ในโหมด DirectQuery ได้</span><span class="sxs-lookup"><span data-stu-id="d29ca-146">Again, you can't create a column in DirectQuery mode.</span></span>  <span data-ttu-id="d29ca-147">แต่ถ้าข้อมูลของคุณมี URL อยู่แล้ว คุณสามารถทำให้ URL เหล่านั้นเป็นไฮเปอร์ลิงก์ได้</span><span class="sxs-lookup"><span data-stu-id="d29ca-147">But if your data already contains URLs, you can turn them into hyperlinks.</span></span>

2. <span data-ttu-id="d29ca-148">ในมุมมองข้อมูลหรือมุมมองรายงาน ให้เลือกคอลัมน์ที่ประกอบด้วย URL</span><span class="sxs-lookup"><span data-stu-id="d29ca-148">In Data view or Report view, select the column that contains the URL.</span></span> 

3. <span data-ttu-id="d29ca-149">บนแท็บ **การสร้างแบบจำลอง** ให้เลือก **ประเภทข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="d29ca-149">On the **Modeling** tab, select **Data Category**.</span></span> <span data-ttu-id="d29ca-150">ตรวจสอบให้แน่ใจว่าคอลัมน์ถูกจัดรูปแบบเป็น **ไม่มีประเภท**</span><span class="sxs-lookup"><span data-stu-id="d29ca-150">Make sure the column is formatted as **Uncategorized**.</span></span>

2. <span data-ttu-id="d29ca-151">ในมุมมองรายงาน สร้างตารางหรือเมทริกซ์ด้วยคอลัมน์ URL และคอลัมน์ที่คุณจะจัดรูปแบบเป็นข้อความลิงก์</span><span class="sxs-lookup"><span data-stu-id="d29ca-151">In Report view, create a table or matrix with the URL column and the column you're going to format as link text.</span></span>

3. <span data-ttu-id="d29ca-152">ในตารางที่เลือกไว้ เลือกไอคอน **จัดรูปแบบ** ![ไอคอนแปรงลูกกลิ้ง](media/power-bi-hyperlinks-in-tables/power-bi-paintroller.png) เพื่อเปิดแถบจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="d29ca-152">With the table selected, select the **Format** icon ![Paint roller icon](media/power-bi-hyperlinks-in-tables/power-bi-paintroller.png) to open the Formatting tab.</span></span>

4. <span data-ttu-id="d29ca-153">ขยาย **การจัดรูปแบบตามเงื่อนไข** ตรวจสอบให้แน่ใจว่าชื่อในกล่องเป็นคอลัมน์ที่คุณต้องการให้เป็นข้อความลิงก์</span><span class="sxs-lookup"><span data-stu-id="d29ca-153">Expand **Conditional formatting**, making sure the name in the box is the column you want as link text.</span></span> <span data-ttu-id="d29ca-154">ค้นหา **URL เว็บ** และเปลี่ยนเป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="d29ca-154">Locate **Web URL**, and turn it to **On**.</span></span>

    ![URL เว็บการกำหนดรูปแบบตามเงื่อนไข](media/power-bi-hyperlinks-in-tables/power-bi-format-conditional-web-url.png)

    > [!NOTE]
    > <span data-ttu-id="d29ca-156">หากคุณไม่เห็นตัวเลือก **URL เว็บ** ตรวจสอบให้แน่ใจว่าคอลัมน์ที่มีไฮเปอร์ลิงก์ *ไม่* ได้จัดรูปแบบเป็น **URL เว็บ** ในกล่องดรอปดาวน์ **ประเภทข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="d29ca-156">If you don't see a **Web URL** option, make sure the column that contains the hyperlinks is *not* formatted as **Web URL** in the **Data Category** dropdown box.</span></span>

5. <span data-ttu-id="d29ca-157">ในกล่องข้อความ **URL เว็บ** เลือกเขตข้อมูลที่มี URL ในกล่อง **เขตข้อมูล อิงตาม** > **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d29ca-157">In the **Web URL** dialog box, select the field that contains the URL in the **Based on field** box > **OK**.</span></span>

    ![กล่องข้อความ URL เว็บ](media/power-bi-hyperlinks-in-tables/power-bi-format-web-url-dialog.png)

    <span data-ttu-id="d29ca-159">ตอนนี้ข้อความในคอลัมน์นั้นจะได้รับการจัดรูปแบบเป็นลิงก์</span><span class="sxs-lookup"><span data-stu-id="d29ca-159">Now the text in that column is formatted as the link.</span></span>

    ![ข้อความที่จัดรูปแบบเป็นไฮเปอร์ลิงก์](media/power-bi-hyperlinks-in-tables/power-bi-url-link-text.png)

1. <span data-ttu-id="d29ca-161">(ไม่บังคับ) [เผยแพร่รายงาน](desktop-upload-desktop-files.md) จาก Power BI Desktop ไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="d29ca-161">(Optional) [Publish the report](desktop-upload-desktop-files.md) from Power BI Desktop to the Power BI service.</span></span> <span data-ttu-id="d29ca-162">เมื่อคุณเปิดรายงานในบริการของ Power BI ไฮเปอร์ลิงก์จะทำงานด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="d29ca-162">When you open the report in the Power BI service, the hyperlinks work there, too.</span></span>

## <a name="create-a-table-or-matrix-hyperlink-in-excel-power-pivot"></a><span data-ttu-id="d29ca-163">สร้างไฮเปอร์ลิงก์ตารางหรือเมทริกซ์ใน Power Pivot ของ Excel</span><span class="sxs-lookup"><span data-stu-id="d29ca-163">Create a table or matrix hyperlink in Excel Power Pivot</span></span>

<span data-ttu-id="d29ca-164">อีกวิธีในการเพิ่มไฮเปอร์ลิงก์ไปยัง Power BI ตารางและเมทริกซ์คือ การสร้างไฮเปอร์ลิงก์ในชุดข้อมูลก่อนที่คุณนำเข้า/เชื่อมต่อกับชุดข้อมูลนั้นจาก Power BI</span><span class="sxs-lookup"><span data-stu-id="d29ca-164">Another way to add hyperlinks to your Power BI tables and matrixes is to create the hyperlinks in the dataset before you import/connect to that dataset from Power BI.</span></span> <span data-ttu-id="d29ca-165">ตัวอย่างนี้ใช้สมุดงาน Excel</span><span class="sxs-lookup"><span data-stu-id="d29ca-165">This example uses an Excel workbook.</span></span>

1. <span data-ttu-id="d29ca-166">เปิดสมุดงานใน Excel</span><span class="sxs-lookup"><span data-stu-id="d29ca-166">Open the workbook in Excel.</span></span>
2. <span data-ttu-id="d29ca-167">เลือกแถบ **PowerPivot** และจากนั้น เลือก **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="d29ca-167">Select the **PowerPivot** tab and then choose **Manage**.</span></span>
   
   ![เปิด PowerPivot ใน Excel](media/power-bi-hyperlinks-in-tables/createhyperlinkinpowerpivot2.png)
1. <span data-ttu-id="d29ca-169">เมื่อ PowerPivot เปิดขึ้น เลือกแถบ **ขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="d29ca-169">When PowerPivot opens, select the **Advanced** tab.</span></span>
   
   ![แท็บ PowerPivot ขั้นสูง](media/power-bi-hyperlinks-in-tables/createhyperlinkinpowerpivot3.png)
4. <span data-ttu-id="d29ca-171">วางเคอร์เซอร์ในคอลัมน์ที่ประกอบด้วย URL ที่คุณต้องการเปลี่ยนเป็นไฮเปอร์ลิงก์ในตาราง Power BI</span><span class="sxs-lookup"><span data-stu-id="d29ca-171">Place your cursor in the column that contains the URLs that you'd like to turn into hyperlinks in Power BI tables.</span></span>
   
   > [!NOTE]
   > <span data-ttu-id="d29ca-172">URL ต้องเริ่มต้นด้วยเลขนำหน้าบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="d29ca-172">URLS must start with certain prefixes.</span></span> <span data-ttu-id="d29ca-173">โปรดดู [ข้อควรพิจารณาและการแก้ไขปัญหา](#considerations-and-troubleshooting) สำหรับรายการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d29ca-173">See [Considerations and troubleshooting](#considerations-and-troubleshooting) for the complete list.</span></span>
   > 
   
5. <span data-ttu-id="d29ca-174">ในกลุ่ม **รายงานคุณสมบัติ** เลือก **ประเภทข้อมูล** แบบเลื่อนลง แล้วเลือก **URL เว็บ**</span><span class="sxs-lookup"><span data-stu-id="d29ca-174">In the **Reporting Properties** group, select the **Data Category** dropdown and choose **Web URL**.</span></span> 
   
   ![ดรอปดาวน์ประเภทข้อมูลใน Excel](media/power-bi-hyperlinks-in-tables/createhyperlinksnew.png)

6. <span data-ttu-id="d29ca-176">จากบริการ Power BI หรือ Power BI Desktop เชื่อมต่อไปยัง หรือนำเข้าสมุดงานนี้</span><span class="sxs-lookup"><span data-stu-id="d29ca-176">From the Power BI service or Power BI Desktop, connect to or import this workbook.</span></span>
7. <span data-ttu-id="d29ca-177">สร้างการแสดงภาพตารางที่มีเขตข้อมูล URL</span><span class="sxs-lookup"><span data-stu-id="d29ca-177">Create a table visualization that includes the URL field.</span></span>
   
   ![สร้างตารางใน Power BI ด้วย URL เขตข้อมูล](media/power-bi-hyperlinks-in-tables/hyperlinksintables.gif)

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="d29ca-179">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="d29ca-179">Considerations and troubleshooting</span></span>

<span data-ttu-id="d29ca-180">URL ต้องเริ่มต้นด้วยหนึ่งในรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d29ca-180">URLS must start with one of the following:</span></span>
- <span data-ttu-id="d29ca-181">http</span><span class="sxs-lookup"><span data-stu-id="d29ca-181">http</span></span>
- <span data-ttu-id="d29ca-182">https</span><span class="sxs-lookup"><span data-stu-id="d29ca-182">https</span></span>
- <span data-ttu-id="d29ca-183">mailto</span><span class="sxs-lookup"><span data-stu-id="d29ca-183">mailto</span></span>
- <span data-ttu-id="d29ca-184">ftp</span><span class="sxs-lookup"><span data-stu-id="d29ca-184">ftp</span></span>
- <span data-ttu-id="d29ca-185">news</span><span class="sxs-lookup"><span data-stu-id="d29ca-185">news</span></span>
- <span data-ttu-id="d29ca-186">telnet</span><span class="sxs-lookup"><span data-stu-id="d29ca-186">telnet</span></span>

<span data-ttu-id="d29ca-187">คำถาม: ฉันสามารถใช้ URL ที่กำหนดเองเป็นไฮเปอร์ลิงก์ในตารางหรือเมทริกซ์ได้หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="d29ca-187">Q: Can I use a custom URL as a hyperlink in a table or matrix?</span></span>    
<span data-ttu-id="d29ca-188">คำตอบ: ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="d29ca-188">A: No.</span></span> <span data-ttu-id="d29ca-189">คุณสามารถใช้ไอคอนลิงก์หนึ่งได้</span><span class="sxs-lookup"><span data-stu-id="d29ca-189">You can use a link icon.</span></span> <span data-ttu-id="d29ca-190">ถ้าคุณต้องการข้อความแบบกำหนดเองสำหรับไฮเปอร์ลิงก์ของคุณ และรายการของ URL เป็นรายการที่สั้น ให้พิจารณาการใช้กล่องข้อความแทน</span><span class="sxs-lookup"><span data-stu-id="d29ca-190">If you need custom text for your hyperlinks and your list of URLs is short, consider using a text box instead.</span></span>


## <a name="next-steps"></a><span data-ttu-id="d29ca-191">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d29ca-191">Next steps</span></span>
[<span data-ttu-id="d29ca-192">การแสดงภาพในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="d29ca-192">Visualizations in Power BI reports</span></span>](../visuals/power-bi-report-visualizations.md)

[<span data-ttu-id="d29ca-193">แนวคิดพื้นฐานสำหรับนักออกแบบในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="d29ca-193">Basic concepts for designers in the Power BI service</span></span>](../fundamentals/service-basic-concepts.md)

<span data-ttu-id="d29ca-194">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d29ca-194">More questions?</span></span> [<span data-ttu-id="d29ca-195">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="d29ca-195">Try the Power BI Community</span></span>](https://community.powerbi.com/)
