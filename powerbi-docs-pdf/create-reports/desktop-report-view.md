---
title: มุมมองรายงานใน Power BI Desktop
description: มุมมองรายงานใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: conceptual
ms.date: 10/12/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 3b168eb0e6a475651f4f8fb6337c518812d8ffcf
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412885"
---
# <a name="work-with-report-view-in-power-bi-desktop"></a><span data-ttu-id="a016a-103">ทำงานกับมุมมองรายงานใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a016a-103">Work with Report view in Power BI Desktop</span></span>

<span data-ttu-id="a016a-104">ถ้าคุณเคยทำงานกับ Power BI คุณย่อมทราบว่า Power BI สามารถสร้างรายงานที่แสดงเปอร์สเปกทิฟแบบไดนามิกและข้อมูลเชิงลึกในข้อมูลของคุณได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="a016a-104">If you've been working with Power BI, you know how easy it's to create reports providing dynamic perspectives and insights into your data.</span></span> <span data-ttu-id="a016a-105">Power BI ยังมีคุณลักษณะขั้นสูงอื่น ๆ ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a016a-105">Power BI also has more advanced features in Power BI Desktop.</span></span> <span data-ttu-id="a016a-106">ด้วย Power BI Desktop คุณสามารถสร้างคิวรีขั้นสูง ผสมรวมข้อมูลจากหลายแหล่งข้อมูล สร้างความสัมพันธ์ระหว่างตาราง และอื่นๆ ได้</span><span class="sxs-lookup"><span data-stu-id="a016a-106">With Power BI Desktop, create advanced queries, mashup data from multiple sources, create relationships between tables, and more.</span></span>

<span data-ttu-id="a016a-107">Power BI Desktop รวมด้วยกับ *มุมมองรายงาน* ซึ่งคุณสามารถสร้างหน้ารายงานที่มีการแสดงผลด้วยภาพจำนวนกี่หน้าก็ได้</span><span class="sxs-lookup"><span data-stu-id="a016a-107">Power BI Desktop includes a *Report view*, where you can create any number of report pages with visualizations.</span></span> <span data-ttu-id="a016a-108">มุมมองรายงานใน  Power BI Desktop ให้ประสบการณ์ในการออกแบบที่ค่อนข้างเหมือนกับมุมมองการแก้ไขของรายงานใน *บริการ Power BI*</span><span class="sxs-lookup"><span data-stu-id="a016a-108">Report view in Power BI Desktop provides a similar design experience to the report's editing view in the *Power BI service*.</span></span> <span data-ttu-id="a016a-109">คุณสามารถย้ายการแสดงภาพไปรอบ ๆ คัดลอกและวาง ผสาน และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="a016a-109">You can move visualizations around, copy and paste, merge, and so on.</span></span>

<span data-ttu-id="a016a-110">ความแตกต่างคือ เมื่อใช้ Power BI Desktop คุณสามารถทำงานกับคิวรีของคุณ และสร้างแบบจำลองข้อมูลของคุณ เพื่อให้แน่ใจว่า ข้อมูลรองรับข้อมูลเชิงลึกที่ดีที่สุดในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="a016a-110">The difference between them is when using Power BI Desktop, you can work with your queries and model your data to make sure your data supports the best insights in your reports.</span></span> <span data-ttu-id="a016a-111">จากนั้นคุณสามารถบันทึกไฟล์ Power BI Desktop ของคุณเมื่อใดก็ตามที่คุณต้องการ ไม่ว่าจะบันทึกลงไดรฟ์ในเครื่อง หรือคลาวด์</span><span class="sxs-lookup"><span data-stu-id="a016a-111">You can then save your Power BI Desktop file wherever you like, whether it's your local drive or to the cloud.</span></span>

## <a name="lets-take-a-look"></a><span data-ttu-id="a016a-112">ลองมาดูกัน</span><span class="sxs-lookup"><span data-stu-id="a016a-112">Let's take a look!</span></span>

<span data-ttu-id="a016a-113">เมื่อคุณเริ่มโหลดข้อมูลใน Power BI Desktop คุณจะเห็นมุมมองรายงานกับพื้นที่ว่างเปล่า พร้อมกับลิงก์ที่ช่วยให้คุณเพิ่มข้อมูลไปยังรายงานของคุณได้</span><span class="sxs-lookup"><span data-stu-id="a016a-113">When you first load data in Power BI Desktop, you'll see the Report view with a blank canvas, with links to help you add data to your report.</span></span>

![Power BI Desktop](media/desktop-report-view/report-view-blank-canvas.png)

<span data-ttu-id="a016a-115">คุณสามารถสลับไปมาระหว่าง **รายงาน** **ข้อมูล** และ **ความสัมพันธ์** โดยการเลือกไอคอนในแผงนำทางด้านซ้าย:</span><span class="sxs-lookup"><span data-stu-id="a016a-115">You can switch between **Report**, **Data**, and **Relationship** views by selecting the icons in the left-hand navigation pane:</span></span>

![ไอคอนมุมมองรายงาน](media/desktop-report-view/pbi_reportviewinpbidesigner_changeview.png)

<span data-ttu-id="a016a-117">เมื่อคุณเพิ่มบางข้อมูลแล้ว คุณสามารถเพิ่มเขตข้อมูลไปยังการแสดงผลด้วยภาพแบบใหม่ในพื้นที่ว่าง</span><span class="sxs-lookup"><span data-stu-id="a016a-117">Once you've added some data, you can add fields to a new visualization in the canvas.</span></span>

![เพิ่มภาพโดยการลากจากบานหน้าต่างเขตข้อมูล](media/desktop-report-view/pbid_reportview_addvis.gif)

<span data-ttu-id="a016a-119">เมื่อต้องการเปลี่ยนชนิดของการแสดงผลด้วยภาพ คุณสามารถเลือกได้ในพื้นที่ว่าง จากนั้นเลือกชนิดใหม่ใน **การแสดงผลด้วยภาพ**</span><span class="sxs-lookup"><span data-stu-id="a016a-119">To change the type of visualization, you can select it on the canvas, then select a new type in **Visualizations**.</span></span>

![เปลี่ยนภาพโดยการเลือกภาพใหม่](media/desktop-report-view/pbid_reportview_changevis.gif)

> [!TIP]
> <span data-ttu-id="a016a-121">ตรวจสอบให้แน่ใจว่าได้ทดลองกับชนิดการแสดงภาพอื่น</span><span class="sxs-lookup"><span data-stu-id="a016a-121">Be sure to experiment with different visualization types.</span></span> <span data-ttu-id="a016a-122">การแสดงผลด้วยภาพของคุณควรจะต้องสื่อข้อมูลในข้อมูลของคุณอย่างชัดเจน</span><span class="sxs-lookup"><span data-stu-id="a016a-122">It's important your visualization convey information in your data clearly.</span></span>

<span data-ttu-id="a016a-123">รายงานจะมีหน้าเปล่าอย่างน้อยหนึ่งหน้าเพื่อเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a016a-123">A report will have at least one blank page to start.</span></span> <span data-ttu-id="a016a-124">หน้าที่ปรากฏในบานหน้าต่างตัวนำทางที่อยู่ทางด้านซ้ายของพื้นที่ว่าง</span><span class="sxs-lookup"><span data-stu-id="a016a-124">Pages appear in the navigator pane just to the left of the canvas.</span></span> <span data-ttu-id="a016a-125">คุณสามารถเพิ่มการเรียงลำดับทั้งหมดของการแสดงภาพลงในหน้า แต่จะต้องไม่เพิ่มมากเกินไป</span><span class="sxs-lookup"><span data-stu-id="a016a-125">You can add all sorts of visualizations to a page, but it's important not to overdo it.</span></span> <span data-ttu-id="a016a-126">การแสดงผลด้วยภาพมากเกินไปในหน้าจะทำให้ดูยุ่งเหยิง และยากในการค้นหาข้อมูลที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a016a-126">Too many visualizations on a page make it look busy and difficult to find the right information.</span></span> <span data-ttu-id="a016a-127">คุณสามารถเพิ่มหน้าใหม่ลงในรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="a016a-127">You can add new pages to your report.</span></span> <span data-ttu-id="a016a-128">เพียงแค่คลิกที่ **หน้าใหม่** บน ribbon</span><span class="sxs-lookup"><span data-stu-id="a016a-128">Just click **New Page** on the ribbon.</span></span>

![ไอคอนหน้าใหม่](media/desktop-report-view/pbidesignerreportviewnewpage.png)

<span data-ttu-id="a016a-130">เมื่อต้องการลบหน้า คลิกที่ **X** บนแท็บของหน้าที่ด้านล่างของมุมมองรายงาน</span><span class="sxs-lookup"><span data-stu-id="a016a-130">To delete a page, click the **X** on the page's tab at the bottom of the Report view.</span></span>

![เพิ่มหน้าในรายงาน](media/desktop-report-view/pbi_reportviewinpbidesigner_deletepage.png)

> [!NOTE]
> <span data-ttu-id="a016a-132">รายงานและการแสดงผลด้วยภาพไม่สามารถปักหมุดลงในแดชบอร์ดจาก Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a016a-132">Reports and visualizations can't be pinned to a dashboard from Power BI Desktop.</span></span> <span data-ttu-id="a016a-133">เมื่อต้องการทำเช่นนั้น คุณจะต้องเผยแพร่จาก Power BI Desktopไปยังไซต์ Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a016a-133">To do that, you'll need to publish to your Power BI site.</span></span> <span data-ttu-id="a016a-134">สำหรับข้อมูลเพิ่มเติม ให้ดู [เผยแพร่ชุดข้อมูลและรายงานจาก Power BI Desktop](desktop-upload-desktop-files.md)</span><span class="sxs-lookup"><span data-stu-id="a016a-134">For more information, see [Publish datasets and reports from Power BI Desktop](desktop-upload-desktop-files.md).</span></span>

## <a name="copy-and-paste-between-reports"></a><span data-ttu-id="a016a-135">คัดลอกและวางระหว่างรายงาน</span><span class="sxs-lookup"><span data-stu-id="a016a-135">Copy and paste between reports</span></span>

<span data-ttu-id="a016a-136">คุณสามารถใช้วิชวลจากรายงาน Power BI Desktop หนึ่งรายงาน และวางลงในรายงานอื่นได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="a016a-136">You can easily take a visual from one Power BI Desktop report and paste it into another report.</span></span> <span data-ttu-id="a016a-137">เพียงแค่ใช้แป้นพิมพ์ลัด Ctrl + C เพื่อคัดลอกวิชวลรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="a016a-137">Simply use the Ctrl+C keyboard shortcut to copy your report visual.</span></span> <span data-ttu-id="a016a-138">ในรายงาน Power BI Desktop อื่นๆ ให้ใช้ Ctrl + V เพื่อวางวิชวลลงในรายงานอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="a016a-138">In the other Power BI Desktop report, use Ctrl+V to paste the visual into the other report.</span></span> <span data-ttu-id="a016a-139">คุณสามารถเลือกภาพได้ครั้งละหนึ่งวิชวลหรือสามารถเลือกภาพทั้งหมดบนหน้าเพื่อคัดลอก จากนั้นวางลงในรายงาน Power BI Desktop ปลายทาง</span><span class="sxs-lookup"><span data-stu-id="a016a-139">You can select one visual at a time, or all visuals on a page to copy, then paste into the destination Power BI Desktop report.</span></span>

<span data-ttu-id="a016a-140">ความสามารถในการคัดลอกและวางภาพจะมีประโยชน์สำหรับผู้ที่สร้าง และอัปเดตรายงานหลายรายงานเป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="a016a-140">The ability to copy and paste visuals is useful for people who build and updates multiple reports frequently.</span></span> <span data-ttu-id="a016a-141">เมื่อคัดลอกระหว่างไฟล์ การตั้งค่าและการจัดรูปแบบที่ตั้งไว้อย่างชัดเจนในบานหน้าต่างการจัดรูปแบบจะดำเนินการไปข้างหน้า</span><span class="sxs-lookup"><span data-stu-id="a016a-141">When copying between files, settings and formatting that have been explicitly set in the formatting pane will carry forward, while visual elements relying on a theme or the default settings automatically update to match the theme of the destination report.</span></span> <span data-ttu-id="a016a-142">ดังนั้นเมื่อคุณได้รับการจัดรูปแบบภาพในแบบที่คุณต้องการแล้ว คุณสามารถคัดลอกและวางภาพนั้นลงในรายงานใหม่และเก็บรักษางานการจัดรูปแบบที่ดีทั้งหมดไว้ได้</span><span class="sxs-lookup"><span data-stu-id="a016a-142">So when you get a visual formatted and looking just the way you want, you can copy and paste that visual into new reports and preserve all that good formatting work.</span></span>

<span data-ttu-id="a016a-143">หากเขตข้อมูลในแบบโมเดลของคุณแตกต่างกัน คุณจะเห็นข้อผิดพลาดบนวิชวลและคำเตือนเกี่ยวกับเขตข้อมูลนั้นๆ ที่ไม่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="a016a-143">If the fields in your model are different, you'll see an error on the visual and a warning about which fields don't exist.</span></span> <span data-ttu-id="a016a-144">ข้อผิดพลาดคล้ายกับสิ่งที่คุณเห็นเมื่อคุณลบเขตข้อมูลในแบบจำลองที่ใช้ภาพอยู่</span><span class="sxs-lookup"><span data-stu-id="a016a-144">The error is similar to the experience you see when you delete a field in the model that a visual is using.</span></span>

![ข้อผิดพลาดในการคัดลอก/วาง ภาพ - ไม่มีเขตข้อมูล](media/desktop-report-view/report-view_07.png)

<span data-ttu-id="a016a-146">เมื่อต้องการแก้ไขข้อผิดพลาด เพียงแค่แทนเขตข้อมูลที่ใช้งานไม่ได้ด้วยเขตข้อมูลที่คุณต้องการใช้จากแบบจำลองในรายงานที่คุณได้วางภาพไว้</span><span class="sxs-lookup"><span data-stu-id="a016a-146">To correct the error, just replace the broken fields with the fields you want to use from the model in the report to which you pasted the visual.</span></span> <span data-ttu-id="a016a-147">หากคุณกำลังใช้ภาพแบบกำหนดเอง คุณต้องนำเข้าภาพแบบกำหนดเองนั้นลงในรายงานปลายทาง</span><span class="sxs-lookup"><span data-stu-id="a016a-147">If you're using a custom visual, you must also import that custom visual to the destination report.</span></span>

## <a name="hide-report-pages"></a><span data-ttu-id="a016a-148">ซ่อนหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="a016a-148">Hide report pages</span></span>

<span data-ttu-id="a016a-149">เมื่อคุณสร้างรายงาน คุณสามารถซ่อนหน้าจากรายงาน</span><span class="sxs-lookup"><span data-stu-id="a016a-149">When you create a report, you can also hide pages from a report.</span></span> <span data-ttu-id="a016a-150">นี่อาจเป็นประโยชน์ถ้าคุณจำเป็นต้องสร้างข้อมูลพื้นฐานหรือวิชวลในรายงาน แต่ไม่ต้องการให้ผู้อื่นสามารถมองเห็นหน้าเหล่านั้น เช่น เมื่อคุณสร้างตารางหรือวิชวลสนับสนุนที่ใช้ในหน้ารายงานอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="a016a-150">This approach might be useful if you need to create underlying data or visuals in a report, but you don't want those pages to be visible to others, such as when you create tables or supporting visuals that are used in other report pages.</span></span> <span data-ttu-id="a016a-151">มีเหตุผลสร้างสรรค์มากมายที่คุณอาจต้องการสร้างหน้ารายงาน และซ่อนหน้ารายงานนั้นจากรายงานที่คุณต้องการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="a016a-151">There are many other creative reasons you might want to create a report page, then hide it from a report you want to publish.</span></span>

<span data-ttu-id="a016a-152">การซ่อนหน้ารายงานเป็นเรื่องง่าย</span><span class="sxs-lookup"><span data-stu-id="a016a-152">Hiding a report page is easy.</span></span> <span data-ttu-id="a016a-153">เพียงแค่คลิกขวาบนแท็บหน้ารายงาน และเลือก **ซ่อน** จากเมนูที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="a016a-153">Simply right-click on the report page tab, and select **Hide** from the menu that appears.</span></span>

![ซ่อนตัวเลือกหน้า](media/desktop-report-view/report-view_05.png)

<span data-ttu-id="a016a-155">คุณควรทราบข้อควรพิจารณาบางประการเมื่อทำการซ่อนหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="a016a-155">There are a few considerations to keep in mind when hiding a report page:</span></span>

* <span data-ttu-id="a016a-156">คุณยังคงสามารถดูมุมมองรายงานที่ซ่อนไว้ใน Power BI Desktop แม้ว่าชื่อของหน้าจะเป็นสีเทา ในรูปต่อไปนี้ หน้าที่ 4 ถูกซ่อนอยู่</span><span class="sxs-lookup"><span data-stu-id="a016a-156">You can still see a hidden report view when in Power BI Desktop, even though the page's title is grayed out. In the following image, Page 4 is hidden.</span></span>

    ![ทำให้หน้าที่ซ่อนอยู่เป็นสีทึบ](media/desktop-report-view/report-view_06.png)

* <span data-ttu-id="a016a-158">คุณ *ไม่สามารถ* ดูหน้ารายงานที่ซ่อนไว้เมื่อดูรายงานในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="a016a-158">You *cannot* see a hidden report page when viewing the report in the Power BI service.</span></span>

* <span data-ttu-id="a016a-159">การซ่อนหน้ารายงาน *ไม่ใช่* มาตรการรักษาความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="a016a-159">Hiding a report page is *not* a security measure.</span></span> <span data-ttu-id="a016a-160">ผู้ใช้ยังคงสามารถเข้าถึงหน้าได้ และเนื้อหาจะยังคงสามารถเข้าถึงได้โดยใช้ตัวเจาะเข้าถึงรายละเอียด และวิธีการอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="a016a-160">The page can still be accessed by users, and its content is still accessible using drill-through, and other methods.</span></span>

* <span data-ttu-id="a016a-161">เมื่อซ่อนหน้าแล้ว ในโหมดมุมมองจะไม่แสดงลูกศรนำทางโหมดมุมอง</span><span class="sxs-lookup"><span data-stu-id="a016a-161">When a page is hidden, when in View mode, no view-mode navigation arrows are shown.</span></span>
