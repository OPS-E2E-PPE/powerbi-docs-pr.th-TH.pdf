---
title: ใช้ธีมแดชบอร์ดในบริการของ Power BI
description: เรียนรู้วิธีการใช้ชุดสีแบบกำหนดเอง และนำไปใช้กับทั้งแดชบอร์ดในบริการของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 12/02/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 23e0c37d6f2cefc7197a873138dadc2e8ef6968e
ms.sourcegitcommit: 513c4b884a58e1da2680579339c24c46091bbfb2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/04/2020
ms.locfileid: "96613957"
---
# <a name="use-dashboard-themes-in-the-power-bi-service"></a><span data-ttu-id="1885e-103">ใช้ธีมแดชบอร์ดในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="1885e-103">Use dashboard themes in the Power BI service</span></span>
<span data-ttu-id="1885e-104">ด้วย **ธีมแดชบอร์ด** คุณสามารถใช้ธีมสีกับทั้งแดชบอร์ดของคุณ เช่น สีขององค์กร การกำหนดสีตามฤดูกาล หรือธีมสีอื่น ๆ ที่คุณอาจต้องการนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="1885e-104">With **dashboard themes** you can apply a color theme to your entire dashboard, such as corporate colors, seasonal coloring, or any other color theme you might want to apply.</span></span> <span data-ttu-id="1885e-105">เมื่อคุณใช้ธีมแดชบอร์ด วิชวลทั้งหมดบนแดชบอร์ดของคุณจะใช้สีจากธีมที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="1885e-105">When you apply a dashboard theme, all visuals on your dashboard use the colors from your selected theme.</span></span> <span data-ttu-id="1885e-106">มีข้อยกเว้นบางประการซึ่งอธิบายไว้ในส่วน[ข้อควรพิจารณาและข้อจำกัด](#considerations-and-limitations)ของบทความนี้</span><span class="sxs-lookup"><span data-stu-id="1885e-106">A few exceptions apply, described in the [Considerations and limitations](#considerations-and-limitations) section of this article.</span></span>

![สกรีนช็อตของแดชบอร์ดตัวอย่างพร้อมภาพพื้นหลังของธีม](media/service-dashboard-themes/power-bi-full-dashboard-theme.png)

<span data-ttu-id="1885e-108">การเปลี่ยนสีของวิชวลรายงานบนแดชบอร์ดจะไม่มีผลกับวิชวลในรายงานที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="1885e-108">Changing the colors of the report visuals on a dashboard doesn't affect the visuals in the associated report.</span></span> <span data-ttu-id="1885e-109">นอกจากนี้ เมื่อคุณปักหมุดไทล์จากรายงานที่[ใช้ธีมรายงานอยู่แล้ว](desktop-report-themes.md) คุณสามารถเลือกเพื่อเก็บธีมปัจจุบัน หรือใช้ธีมแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="1885e-109">Also, when you pin tiles from a report that already has a [report theme applied](desktop-report-themes.md), you can choose to keep the current theme or use the dashboard theme.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="1885e-110">สิ่งที่จำเป็นต้องมี</span><span class="sxs-lookup"><span data-stu-id="1885e-110">Prerequisites</span></span>
* <span data-ttu-id="1885e-111">เพื่อทดลองทำตาม เปิด[ตัวอย่างแดชบอร์ดการขายและการตลาด](sample-datasets.md)</span><span class="sxs-lookup"><span data-stu-id="1885e-111">To follow along, open the [Sales and Marketing sample dashboard](sample-datasets.md).</span></span>


## <a name="how-dashboard-themes-work"></a><span data-ttu-id="1885e-112">วิธีการทำงานของธีมแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="1885e-112">How dashboard themes work</span></span>
<span data-ttu-id="1885e-113">หากต้องการเริ่มต้นใช้งาน ให้เปิดแดชบอร์ดที่คุณสร้างขึ้น หรือสามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="1885e-113">To get started, open a dashboard that you created, or can edit.</span></span> <span data-ttu-id="1885e-114">เลือก **แก้ไข** > **ธีมแดชบอร์ด**</span><span class="sxs-lookup"><span data-stu-id="1885e-114">Select **Edit** > **Dashboard theme**.</span></span> 

![ตัวเลือกธีมของแดชบอร์ด](media/service-dashboard-themes/power-bi-dashboard-theme.png)

<span data-ttu-id="1885e-116">ในบานหน้าต่างแดชบอร์ดที่ปรากฏขึ้น เลือกหนึ่งในธีมที่สร้างไว้ล่วงหน้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="1885e-116">In the dashboard pane that appears, select one of the pre-built themes.</span></span>  <span data-ttu-id="1885e-117">ในตัวอย่างด้านล่าง เราได้เลือกสี **เข้ม**</span><span class="sxs-lookup"><span data-stu-id="1885e-117">In the example below, we've selected **Dark**.</span></span>

![ตัวเลือกสีอ่อน ถูกเลือก](media/service-dashboard-themes/power-bi-theme-menu.png)

![ใช้ตัวเลือกสีเข้ม](media/service-dashboard-themes/power-bi-theme-dark.png)

## <a name="create-a-custom-theme"></a><span data-ttu-id="1885e-120">สร้างธีมแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="1885e-120">Create a custom theme</span></span>

<span data-ttu-id="1885e-121">ธีมเริ่มต้นสำหรับแดชบอร์ด Power BI คือสี **อ่อน**</span><span class="sxs-lookup"><span data-stu-id="1885e-121">The default theme for Power BI dashboards is **Light**.</span></span> <span data-ttu-id="1885e-122">ถ้าคุณต้องการกำหนดสี หรือสร้างธีมของคุณเอง เลือก **กำหนดเอง** ในรายการดรอปดาวน์</span><span class="sxs-lookup"><span data-stu-id="1885e-122">If you want to customize the colors or create your own theme, select **Custom** in the drop-down.</span></span> 

![เลือกแบบกำหนดเองจากรายการดรอปดาวน์](media/service-dashboard-themes/power-bi-theme-custom.png)

<span data-ttu-id="1885e-124">ใช้ตัวเลือกแบบกำหนดเองเพื่อสร้างธีมแดชบอร์ดของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="1885e-124">Use the custom options to create your own dashboard theme.</span></span> <span data-ttu-id="1885e-125">ถ้าต้องการเพิ่มรูปภาพพื้นหลัง เราขอแนะนำว่า รูปภาพของคุณมีความละเอียดอย่างน้อย 1920x1080</span><span class="sxs-lookup"><span data-stu-id="1885e-125">If adding a background image, we recommend that your image be at least 1920x1080 resolution.</span></span> <span data-ttu-id="1885e-126">หากต้องการใช้รูปภาพเป็นพื้นหลัง ให้อัปโหลดรูปภาพไปยังเว็บไซต์สาธารณะ จากนั้นคัดลอก URL และวางลงในเขตข้อมูล **URL ของรูปภาพ**</span><span class="sxs-lookup"><span data-stu-id="1885e-126">To use an image as a background, upload the image to a public website, copy the URL, and paste it into the **Image URL** field.</span></span> 

## <a name="use-a-json-theme"></a><span data-ttu-id="1885e-127">ใช้ธีม JSON</span><span class="sxs-lookup"><span data-stu-id="1885e-127">Use a JSON theme</span></span>
<span data-ttu-id="1885e-128">อีกวิธีในการสร้างธีมแบบกำหนดเอง คือการอัปโหลดไฟล์ JSON ที่มีการตั้งค่าสำหรับสีทั้งหมดที่คุณต้องการใช้สำหรับแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="1885e-128">Another way to create a custom theme is to upload a JSON file that has settings for all the colors you'd like to use for your dashboard.</span></span> <span data-ttu-id="1885e-129">ใน Power BI Desktop ผู้สร้างรายงานใช้ไฟล์ JSON [สร้างธีมสำหรับรายงาน](desktop-report-themes.md)</span><span class="sxs-lookup"><span data-stu-id="1885e-129">In Power BI Desktop, report creators use JSON files to [create themes for reports](desktop-report-themes.md).</span></span> <span data-ttu-id="1885e-130">คุณสามารถอัปโหลดไฟล์ JSON เดียวกันนี้สำหรับแดชบอร์ด หรือค้นหา และอัปโหลดไฟล์ JSON จาก[หน้าแกลเลอรีธีม](https://community.powerbi.com/t5/Themes-Gallery/bd-p/ThemesGallery)ในชุมชน Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="1885e-130">You can upload these same JSON files for dashboards, or find and upload JSON files from the [Theme gallery page](https://community.powerbi.com/t5/Themes-Gallery/bd-p/ThemesGallery) in the Power BI Community.</span></span> 

![ไซต์แกลเลอรีธีม](media/service-dashboard-themes/power-bi-theme-gallery.png)

<span data-ttu-id="1885e-132">คุณยังสามารถบันทึกธีมแบบกำหนดเองของคุณเป็นไฟล์ JSON และให้แชร์กับผู้สร้างแดชบอร์ดอื่น ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="1885e-132">You can also save your custom theme as a JSON file and then share it with other dashboard creators.</span></span> 

### <a name="use-a-theme-from-the-theme-gallery"></a><span data-ttu-id="1885e-133">ใช้ธีมจากแกลเลอรีธีม</span><span class="sxs-lookup"><span data-stu-id="1885e-133">Use a theme from the Theme Gallery</span></span>

<span data-ttu-id="1885e-134">เช่นเดียวกับตัวเลือกมีอยู่ภายในและแบบกำหนดเอง เมื่อคุณอัปโหลดธีม สีจะถูกนำไปใช้กับไทล์ทั้งหมดในแดชบอร์ดโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="1885e-134">As with the built-in and custom options, when you upload a theme, the colors are automatically applied to all tiles on the dashboard.</span></span> 

1. <span data-ttu-id="1885e-135">โฮเวอร์เหนือธีม และเลือก **ดูรายงาน**</span><span class="sxs-lookup"><span data-stu-id="1885e-135">Hover over a theme and choose **View report**.</span></span>

    ![ดูรายงาน](media/service-dashboard-themes/power-bi-choose-theme.png)

2. <span data-ttu-id="1885e-137">เลื่อนลง แล้วค้นหาลิงก์ไปยังไฟล์ JSON</span><span class="sxs-lookup"><span data-stu-id="1885e-137">Scroll down and find the link to the JSON file.</span></span>  <span data-ttu-id="1885e-138">เลือกไอคอนดาวน์โหลด และบันทึกไฟล์</span><span class="sxs-lookup"><span data-stu-id="1885e-138">Select the download icon and save the file.</span></span>

    ![Spring Day JSON](media/service-dashboard-themes/power-bi-theme-json.png)

3. <span data-ttu-id="1885e-140">กลับไปในบริการของ Power BI ในหน้าต่างธีมแดชบอร์ดแบบกำหนดเอง เลือก **อัปโหลดธีม JSON**</span><span class="sxs-lookup"><span data-stu-id="1885e-140">Back in Power BI service, in the Custom Dashboard theme window, select **Upload JSON theme**.</span></span>

    ![อัปโหลด JSON](media/service-dashboard-themes/power-bi-upload-theme.png)

4. <span data-ttu-id="1885e-142">นำทางไปยังตำแหน่งที่คุณบันทึกไฟล์ธีม JSON และเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="1885e-142">Navigate to the location where you saved the JSON theme file and select **Open**.</span></span>

5. <span data-ttu-id="1885e-143">บนหน้าธีมแดชบอร์ด เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="1885e-143">On the Dashboard theme page, select **Save**.</span></span> <span data-ttu-id="1885e-144">ธีมใหม่จะถูกนำมาใช้ในแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="1885e-144">The new theme is applied to your dashboard.</span></span>

    ![ธีมใหม่ที่ถูกนำมาใช้](media/service-dashboard-themes/power-bi-json.png)

## <a name="reports-and-dashboards-with-different-themes"></a><span data-ttu-id="1885e-146">รายงานและแดชบอร์ดที่มีธีมที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="1885e-146">Reports and dashboards with different themes</span></span>

<span data-ttu-id="1885e-147">ถ้ารายงานของคุณใช้ธีมที่แตกต่างจากธีมแดชบอร์ด ในกรณีส่วนใหญ่คุณสามารถควบคุมว่า วิชวลยังคงใช้ธีมของรายงานปัจจุบัน หรือใช้ธีมของแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="1885e-147">If your report uses a different theme from the dashboard theme, in most cases you can control whether the visual retains the current report theme or uses the dashboard theme.</span></span> <span data-ttu-id="1885e-148">แต่อย่างไรก็ตาม วิชวลการ์ดในแดชบอร์ดใช้ตระกูลฟอนต์ 'DIN' พร้อมข้อความสีดำ</span><span class="sxs-lookup"><span data-stu-id="1885e-148">However, card visuals in dashboards use the 'DIN' font family, with black text.</span></span> <span data-ttu-id="1885e-149">คุณสามารถเปลี่ยนสีข้อความสำหรับไทล์ทั้งหมดบนแดชบอร์ดรวมถึงการ์ดได้โดยการสร้างธีมแดชบอร์ดที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="1885e-149">You can change the text color for all the tiles on a dashboard, including the cards, by creating a custom dashboard theme.</span></span>

- <span data-ttu-id="1885e-150">เมื่อปักหมุดไทล์ไปยังแดชบอร์ด เลือก **คงชุดรูปแบบปัจจุบันไว้** เพื่อเก็บธีมรายงานไว้</span><span class="sxs-lookup"><span data-stu-id="1885e-150">When pinning a tile to a dashboard, to keep the report theme, select **Keep current theme**.</span></span> <span data-ttu-id="1885e-151">วิชวลบนแดชบอร์ด จะคงธีมรายงาน รวมถึงการตั้งค่าความโปร่งใส</span><span class="sxs-lookup"><span data-stu-id="1885e-151">The visual, on the dashboard, will retain the report theme, including transparency settings.</span></span>

    <span data-ttu-id="1885e-152">ครั้งเดียวที่คุณจะเห็นตัวเลือก **การกำหนดธีมไทล์** คือ ถ้าคุณสร้างรายงานใน Power BI Desktop [เพิ่มธีมรายงาน](desktop-report-themes.md) แล้วเผยแพร่รายงานไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="1885e-152">The only time you see **Tile Theming** options is if you created the report in Power BI Desktop, [added a report theme](desktop-report-themes.md), and then published the report to Power BI service.</span></span>

    ![เก็บธีมที่เลือกปัจจุบัน](media/service-dashboard-themes/power-bi-keep-current.png)

- <span data-ttu-id="1885e-154">ลองปักหมุดไทล์อีกครั้ง และเลือก **ใช้ธีมของแดชบอร์ด**</span><span class="sxs-lookup"><span data-stu-id="1885e-154">Try re-pinning the tile and selecting **Use dashboard theme**.</span></span>

    ![ใช้ธีมปลายทาง](media/service-dashboard-themes/power-bi-use-destination.png)

## <a name="dashboard-theme-json-file-format"></a><span data-ttu-id="1885e-156">รูปแบบไฟล์ JSON ของธีมแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="1885e-156">Dashboard theme JSON file format</span></span>

<span data-ttu-id="1885e-157">ในขั้นพื้นฐานที่สุด ธีมไฟล์ JSON มีบรรทัดที่จำเป็นต้องระบุเพียงหนึ่งรายการเท่านั้นคือ: **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="1885e-157">At its most basic level, the theme JSON file has only one required line: **name**.</span></span>

```json
{
    "name": "Custom Theme"
}
```

<span data-ttu-id="1885e-158">นอกเหนือจาก **ชื่อ** แล้ว สิ่งอื่นเป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="1885e-158">Other than **name**, everything else is optional.</span></span> <span data-ttu-id="1885e-159">คุณสามารถเพิ่มคุณสมบัติเฉพาะที่คุณต้องการจัดรูปแบบสำหรับไฟล์ธีมได้ตามใจ และสามารถใช้ค่าเริ่มต้นของ Power BI สำหรับส่วนที่เหลือได้</span><span class="sxs-lookup"><span data-stu-id="1885e-159">You're free to add only the properties you specifically want to format to the theme file, and continue to use the Power BI defaults for the rest.</span></span>

<span data-ttu-id="1885e-160">ไฟล์ JSON สำหรับการกำหนดธีมแดชบอร์ดประกอบด้วย:</span><span class="sxs-lookup"><span data-stu-id="1885e-160">The JSON file for dashboard theming includes:</span></span>

- <span data-ttu-id="1885e-161">ชื่อ: ชื่อธีม (เขตข้อมูลเดียวที่บังคับ)</span><span class="sxs-lookup"><span data-stu-id="1885e-161">name: The theme name (only required field).</span></span>
- <span data-ttu-id="1885e-162">ฉากหน้าและพื้นหลัง: สีสำหรับแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="1885e-162">foreground and background: Colors for the dashboard.</span></span>
- <span data-ttu-id="1885e-163">dataColors: รายการรหัสฐานสิบหกเพื่อใช้สำหรับข้อมูลในแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="1885e-163">dataColors: A list of hexcode to use for data in charts.</span></span> <span data-ttu-id="1885e-164">คุณสามารถรวมสีได้น้อยหรือมากตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="1885e-164">You can include as few or as many colors as you want.</span></span>
- <span data-ttu-id="1885e-165">ไทล์: การกำหนดค่าพื้นหลังและสีสำหรับแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="1885e-165">tiles: Background and color configurations for dashboards.</span></span>
- <span data-ttu-id="1885e-166">visualStyles: การจัดรูปแบบแบบละเอียดสำหรับวิชวล</span><span class="sxs-lookup"><span data-stu-id="1885e-166">visualStyles: Granular formatting for visuals.</span></span>

<span data-ttu-id="1885e-167">นี่คือตัวอย่างธีม JSON สำหรับธีมสีอ่อนเริ่มต้น:</span><span class="sxs-lookup"><span data-stu-id="1885e-167">Here is a sample theme JSON for the default Light theme:</span></span>

```json
{

"name":"Light",

"foreground":"#000000",

"background":"#EAEAEA",

"dataColors":["#01B8AA","#374649","#FD625E","#F2C80F","#5F6B6D","#8AD4EB","#FE9666","#A66999"],

"tiles":{"background":"#FFFFFF","color":"#000000"},

"visualStyles":{"*":{"*":{"*":[{"color":{"solid":{"color":"#000000"}}}]}}}

}
```

## <a name="considerations-and-limitations"></a><span data-ttu-id="1885e-168">ข้อควรพิจารณาและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="1885e-168">Considerations and limitations</span></span>

* <span data-ttu-id="1885e-169">คุณไม่สามารถใช้ธีมแดชบอร์ดได้กับรายงานสด ไทล์ iframe ไทล์ SSRS ไทล์เวิร์กบุ๊ก หรือรูปภาพที่ปักหมุดได้</span><span class="sxs-lookup"><span data-stu-id="1885e-169">You can't apply dashboard themes to pinned live report pages, iframe tiles, SSRS tiles, workbook tiles, or images.</span></span>
* <span data-ttu-id="1885e-170">คุณเห็นธีมแดชบอร์ดได้บนอุปกรณ์เคลื่อนที่ แต่คุณสามารถสร้างธีมแดชบอร์ดได้ในบริการของ Power BI เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1885e-170">You see dashboard themes on mobile devices, but you can only create a dashboard theme in Power BI service.</span></span>
* <span data-ttu-id="1885e-171">ธีมแดชบอร์ดแบบกำหนดเองทำงานกับเฉพาะไทล์ที่ปักหมุดจากรายงาน</span><span class="sxs-lookup"><span data-stu-id="1885e-171">Dashboard custom themes only work with tiles pinned from reports.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1885e-172">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="1885e-172">Next steps</span></span>

- [<span data-ttu-id="1885e-173">นำธีมไปใช้กับรายงาน</span><span class="sxs-lookup"><span data-stu-id="1885e-173">Apply themes to reports</span></span>](desktop-report-themes.md)
