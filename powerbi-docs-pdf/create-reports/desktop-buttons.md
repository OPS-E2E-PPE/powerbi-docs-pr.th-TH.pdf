---
title: ใช้ปุ่มใน Power BI
description: คุณสามารถเพิ่มปุ่มต่าง ๆ ในรายงาน Power BI ที่ทำให้รายงานของคุณมีลักษณะเหมือนกับแอป และเพิ่มการมีส่วนร่วมกับผู้ใช้ในเชิงลึกมากขึ้น
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 05/21/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 77f16bedb45b0730a7007da19a427b1832bc9969
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414472"
---
# <a name="use-buttons-in-power-bi"></a><span data-ttu-id="77d99-103">ใช้ปุ่มใน Power BI</span><span class="sxs-lookup"><span data-stu-id="77d99-103">Use buttons in Power BI</span></span>
<span data-ttu-id="77d99-104">การใช้ **ปุ่ม** ใน Power BI ช่วยให้คุณสร้างรายงานที่ทำงานคล้ายกับแอป สร้างสภาพแวดล้อมที่น่าสนใจแก่ผู้ใช้ ให้ผู้ใช้สามารถโฮเวอร์ คลิก และโต้ตอบกับเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="77d99-104">Using **buttons** in Power BI lets you create reports that behave similar to apps, and thereby, create an engaging environment so users can hover, click, and further interact with Power BI content.</span></span> <span data-ttu-id="77d99-105">คุณสามารถเพิ่มปุ่มไปยังรายงานใน **Power BI Desktop** และใน **บริการของ Power BI** ได้</span><span class="sxs-lookup"><span data-stu-id="77d99-105">You can add buttons to reports in **Power BI Desktop** and in the **Power BI service**.</span></span> <span data-ttu-id="77d99-106">เมื่อคุณแชร์รายงานของคุณในบริการ Power BI ปุ่มเหล่านั้นจะช่วยสร้างประสบการณ์การใช้งานที่เหมือนกับแอปให้แก่ผู้ใช้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="77d99-106">When you share your reports in the Power BI service, they provide an app-like experience for your users.</span></span>

![ปุ่มใน Power BI](media/desktop-buttons/power-bi-buttons.png)

## <a name="create-buttons-in-reports"></a><span data-ttu-id="77d99-108">สร้างปุ่มต่าง ๆ ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="77d99-108">Create buttons in reports</span></span>

### <a name="create-a-button-in-power-bi-desktop"></a><span data-ttu-id="77d99-109">สร้างปุ่มใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="77d99-109">Create a button in Power BI Desktop</span></span>

<span data-ttu-id="77d99-110">หากต้องการสร้างปุ่มในรายงานของ **Power BI Desktop** ให้ไปที่ชุดแถบเครื่องมือ **แทรก** แล้วเลือก **ปุ่ม** และเมนูแบบหล่นลงจะปรากฏขึ้น ซึ่งคุณสามารถเลือกปุ่มที่คุณต้องการจากตัวเลือกต่าง ๆ ตามที่แสดงในรูปภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="77d99-110">To create a button in **Power BI Desktop**, on the **Insert** ribbon, select **Buttons** and a drop-down menu appears, where you can select the button you want from a collection of options, as shown in the following image.</span></span> 

![เพิ่มตัวควบคุมแบบปุ่มใน Power BI Desktop](media/desktop-buttons/power-bi-button-dropdown.png)

### <a name="create-a-button-in-the-power-bi-service"></a><span data-ttu-id="77d99-112">สร้างปุ่มในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="77d99-112">Create a button in the Power BI service</span></span>

<span data-ttu-id="77d99-113">หากต้องการสร้างปุ่มใน **บริการของ Power BI** ให้เปิดรายงานในมุมมองการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="77d99-113">To create a button in the **Power BI service**, open the report in Editing view.</span></span> <span data-ttu-id="77d99-114">เลือก **ปุ่ม** ในแถบเมนูด้านบนและเมนูแบบหล่นลงจะปรากฏขึ้น ซึ่งคุณสามารถเลือกปุ่มที่คุณต้องการจากตัวเลือกต่าง ๆ ตามที่แสดงในรูปภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="77d99-114">Select **Buttons** in the top menu bar and a drop-down menu appears, where you can select the button you want from a collection of options, as shown in the following image.</span></span> 

![เพิ่มการควบคุมปุ่มใน Power BI Desktop](media/desktop-buttons/power-bi-button-service-dropdown.png)

## <a name="customize-a-button"></a><span data-ttu-id="77d99-116">ปรับแต่งปุ่ม</span><span class="sxs-lookup"><span data-stu-id="77d99-116">Customize a button</span></span>

<span data-ttu-id="77d99-117">ไม่ว่าคุณจะสร้างปุ่มใน Power BI Desktop หรือบริการ Power BI กระบวนการในส่วนที่เหลือนั้นเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="77d99-117">Whether you create the button in Power BI Desktop or the Power BI service, the rest of the process is the same.</span></span> <span data-ttu-id="77d99-118">เมื่อคุณเลือกปุ่มบนพื้นที่รายงาน บานหน้าต่าง **การแสดงภาพ** จะแสดงวิธีการหลายแบบที่คุณสามารถปรับแต่งปุ่มตามความต้องการของคุณได้</span><span class="sxs-lookup"><span data-stu-id="77d99-118">When you select the button on the report canvas, the **Visualizations** pane shows you the many ways you can customize the button to fit your requirements.</span></span> <span data-ttu-id="77d99-119">ตัวอย่างเช่น คุณสามารถเปิดหรือปิด **ข้อความปุ่ม** โดยการสลับแถบเลื่อนในการ์ดนั้นบนบานหน้าต่าง **การแสดงภาพ**</span><span class="sxs-lookup"><span data-stu-id="77d99-119">For example, you can turn **Button Text** on or off by toggling the slider in that card of the **Visualizations** pane.</span></span> <span data-ttu-id="77d99-120">คุณยังสามารถเปลี่ยนไอคอนของปุ่ม สีพื้นของปุ่ม ชื่อปุ่ม และการดำเนินการที่จะเกิดขึ้นเมื่อผู้ใช้เลือกปุ่มในรายงาน รวมไปถึงคุณสมบัติอื่น ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="77d99-120">You can also change the button icon, the button fill, the title, and the action that's taken when users select the button in a report, among other properties.</span></span>

![จัดรูปแบบปุ่มในรายงาน Power BI](media/desktop-buttons/power-bi-button-properties.png)

## <a name="set-button-properties-when-idle-hovered-over-or-selected"></a><span data-ttu-id="77d99-122">ตั้งค่าคุณสมบัติของปุ่มเมื่ออยู่เฉย ๆ เมื่อโฮเวอร์เหนือ หรือถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="77d99-122">Set button properties when idle, hovered over, or selected</span></span>

<span data-ttu-id="77d99-123">ปุ่มใน Power BI มีสามสถานะ: สถานะเริ่มต้น (ลักษณะที่ปรากฏเมื่อไม่ตัวชี้โฮเวอร์เหนือปุ่ม หรือถูกเลือก), เมื่อตัวชี้มาโฮเวอร์เหนือปุ่ม หรือเมื่อปุ่มถูกเลือก (มักจะเรียกว่าถูก *คลิก*)</span><span class="sxs-lookup"><span data-stu-id="77d99-123">Buttons in Power BI have three states: default (how they appear when not hovered over or selected), when hovered over, or when selected (often referred to as being *clicked*).</span></span> <span data-ttu-id="77d99-124">การ์ดจำนวนมากในบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล** สามารถแก้ไขแยกตามสถานะทั้งสามนี้ ช่วยให้มีความยืดหยุ่นในการกำหนดปุ่มของคุณได้</span><span class="sxs-lookup"><span data-stu-id="77d99-124">Many of the cards in the **Visualizations** pane can be modified individually based on those three states, providing plenty of flexibility for customizing your buttons.</span></span>

<span data-ttu-id="77d99-125">การ์ดต่อไปนี้ในบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล** ให้คุณปรับรูปแบบหรือลักษณะการทำงานของปุ่มที่ตามสถานะทั้งสามของมัน:</span><span class="sxs-lookup"><span data-stu-id="77d99-125">The following cards in the **Visualizations** pane let you adjust formatting or behavior of a button based on its three states:</span></span>

* <span data-ttu-id="77d99-126">ข้อความบนปุ่ม</span><span class="sxs-lookup"><span data-stu-id="77d99-126">Button Text</span></span>
* <span data-ttu-id="77d99-127">ไอคอน</span><span class="sxs-lookup"><span data-stu-id="77d99-127">Icon</span></span>
* <span data-ttu-id="77d99-128">เค้าร่าง</span><span class="sxs-lookup"><span data-stu-id="77d99-128">Outline</span></span>
* <span data-ttu-id="77d99-129">เติม</span><span class="sxs-lookup"><span data-stu-id="77d99-129">Fill</span></span>

<span data-ttu-id="77d99-130">วิธีเลือกว่าจะแสดงปุ่มในแต่ละสถานะอย่างไร ให้ขยายการ์ดหนึ่งในนั้น แล้วเลือกรายการแบบหล่นลงที่ปรากฏด้านบนของการ์ด</span><span class="sxs-lookup"><span data-stu-id="77d99-130">To select how the button should appear for each state, expand one of those cards and select the drop-down that appears at the top of the card.</span></span> <span data-ttu-id="77d99-131">ในรูปต่อไปนี้ คุณเห็นการ์ด **ไอคอน** ขยายออก โดยมีเมนูแบบหล่นลงที่เลือกไว้เพื่อแสดงสถานะสามรูปแบบ:</span><span class="sxs-lookup"><span data-stu-id="77d99-131">In the following image, you see the **Icon** card expanded, with the drop-down selected to show the three states.</span></span>

![สถานะของปุ่มสามรูปแบบในรายงาน Power BI](media/desktop-buttons/power-bi-button-format.png)

## <a name="select-the-action-for-a-button"></a><span data-ttu-id="77d99-133">เลือกการกระทำสำหรับปุ่ม</span><span class="sxs-lookup"><span data-stu-id="77d99-133">Select the action for a button</span></span>

<span data-ttu-id="77d99-134">คุณสามารถเลือกว่าจะดำเนินการอย่างไร เมื่อผู้ใช้เลือกปุ่มใน Power BI</span><span class="sxs-lookup"><span data-stu-id="77d99-134">You can select which action is taken when a user selects a button in Power BI.</span></span> <span data-ttu-id="77d99-135">คุณสามารถเข้าถึงตัวเลือกสำหรับการกระทำของปุ่ม จากการ์ด **การกระทำ** ในบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล** ได้</span><span class="sxs-lookup"><span data-stu-id="77d99-135">You can access the options for button actions from the **Action** card in the **Visualizations** pane.</span></span>

![การกระทำสำหรับปุ่มใน Power BI](media/desktop-buttons/power-bi-button-action.png)

<span data-ttu-id="77d99-137">ต่อไปนี้คือตัวเลือกสำหรับการดำเนินการของปุ่ม</span><span class="sxs-lookup"><span data-stu-id="77d99-137">Here are the options for button actions:</span></span>

- <span data-ttu-id="77d99-138">**ย้อนกลับ** จะส่งผู้ใช้กลับไปยังหน้ารายงานก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="77d99-138">**Back** returns the user to the previous page of the report.</span></span> <span data-ttu-id="77d99-139">ซึ่งมีประโยชน์สำหรับหน้าการเข้าถึงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="77d99-139">This is useful for drill-through pages.</span></span>
- <span data-ttu-id="77d99-140">**บุ๊กมาร์ก** จะแสดงหน้ารายงานที่เชื่อมโยงกับบุ๊กมาร์กซึ่งกำหนดไว้สำหรับรายงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="77d99-140">**Bookmark** presents the report page that's associated with a bookmark that is defined for the current report.</span></span> <span data-ttu-id="77d99-141">เรียนรู้เพิ่มเติมเกี่ยวกับ[บุ๊กมาร์กใน Power BI](desktop-bookmarks.md)</span><span class="sxs-lookup"><span data-stu-id="77d99-141">Learn more about [bookmarks in Power BI](desktop-bookmarks.md).</span></span> 
- <span data-ttu-id="77d99-142">**การเข้าถึงรายละเอียด** จะนำทางผู้ใช้ไปยังหน้าการเข้าถึงรายละเอียดที่กรองตามการเลือกของผู้ใช้ โดยไม่ต้องใช้บุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="77d99-142">**Drill through** navigates the user to a drill-through page filtered to their selection, without using bookmarks.</span></span> <span data-ttu-id="77d99-143">เรียนรู้เพิ่มเติมเกี่ยวกับ[ปุ่มการเข้าถึงรายละเอียดในรายงาน](desktop-drill-through-buttons.md)</span><span class="sxs-lookup"><span data-stu-id="77d99-143">Learn more about [drill-through buttons in reports](desktop-drill-through-buttons.md).</span></span>
- <span data-ttu-id="77d99-144">**การนำทางไปยังหน้า** จะนำทางผู้ใช้ไปยังหน้าต่าง ๆ ภายในรายงาน โดยไม่ต้องใช้บุ๊กมาร์กเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="77d99-144">**Page navigation** navigates the user to a different page within the report, also without using bookmarks.</span></span> <span data-ttu-id="77d99-145">ดูรายละอียดที่ [สร้างการนำทางไปยังหน้า](#create-page-navigation) ในบทความนี้</span><span class="sxs-lookup"><span data-stu-id="77d99-145">See [Create page navigation](#create-page-navigation) in this article for details.</span></span>
- <span data-ttu-id="77d99-146">**ถามตอบ** จะเปิดหน้าต่าง **Q&A Explorer**</span><span class="sxs-lookup"><span data-stu-id="77d99-146">**Q&A** opens a **Q&A Explorer** window.</span></span> 

<span data-ttu-id="77d99-147">ปุ่มบางปุ่มมีการดำเนินการตามค่าเริ่มต้นที่เลือกไว้โดยอัตโนมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="77d99-147">Certain buttons have a default action selected automatically.</span></span> <span data-ttu-id="77d99-148">ตัวอย่างเช่น ปุ่มชนิด **ถามตอบ** จะเลือก **ถามตอบ** เป็นค่าเริ่มต้นของการกระทำ</span><span class="sxs-lookup"><span data-stu-id="77d99-148">For example, the **Q&A** button type automatically selects **Q&A** as the default action.</span></span> <span data-ttu-id="77d99-149">คุณสามารถเรียนรู้เพิ่มเติมเกี่ยวกับ **Q&A Explorer** ได้โดยศึกษาจาก [บล็อกโพสต์นี้](https://powerbi.microsoft.com/blog/power-bi-desktop-april-2018-feature-summary/#Q&AExplorer)</span><span class="sxs-lookup"><span data-stu-id="77d99-149">You can learn more about **Q&A Explorer** by checking out [this blog post](https://powerbi.microsoft.com/blog/power-bi-desktop-april-2018-feature-summary/#Q&AExplorer).</span></span>

<span data-ttu-id="77d99-150">คุณสามารถลองหรือทดสอบปุ่มที่คุณสร้างในรายงาน โดย *CTRL + คลิก* บนปุ่มคุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="77d99-150">You can try or test the buttons you create for your report by using *CTRL+CLICK* on the button you want to use.</span></span> 

## <a name="create-page-navigation"></a><span data-ttu-id="77d99-151">สร้างการนำทางไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="77d99-151">Create page navigation</span></span>

<span data-ttu-id="77d99-152">ด้วยประเภท **การดำเนินการ** ใน **การนำทางไปยังหน้า** คุณสามารถสร้างประสบการณ์การนำทางที่ครบถ้วนได้โดยไม่ต้องบันทึกหรือจัดการบุ๊กมาร์กใดๆ เลย</span><span class="sxs-lookup"><span data-stu-id="77d99-152">With the **Action** type **Page navigation**, you can build an entire navigation experience without having to save or manage any bookmarks at all.</span></span>

<span data-ttu-id="77d99-153">หากต้องการตั้งค่าปุ่มการนำทางไปยังหน้า ให้สร้างปุ่ม **การนำทางไปยังหน้า** เป็นประเภทการดำเนินการ และเลือกหน้า **ปลายทาง**</span><span class="sxs-lookup"><span data-stu-id="77d99-153">To set up a page navigation button, create a button with **Page navigation** as the action type, and select the **Destination** page.</span></span>

![การดำเนินการในการนำทางไปยังหน้า](media/desktop-buttons/power-bi-page-navigation.png)

<span data-ttu-id="77d99-155">คุณสามารถสร้างบานหน้าต่างการนำทางแบบกำหนดเองและเพิ่มปุ่มการนำทางลงไปได้</span><span class="sxs-lookup"><span data-stu-id="77d99-155">You can build a custom navigation pane, and add the navigation buttons to it.</span></span> <span data-ttu-id="77d99-156">คุณสามารถหลีกเลี่ยงการแก้ไขและการจัดการบุ๊กมาร์กได้ หากคุณต้องการเปลี่ยนหน้าที่จะแสดงในบานหน้าต่างการนำทางของคุณ</span><span class="sxs-lookup"><span data-stu-id="77d99-156">You avoid having to edit and manage bookmarks if you want to change which pages to show in your navigation pane.</span></span>

![สร้างหน้าการนำทาง](media/desktop-buttons/power-bi-build-navigation-pane.png)

<span data-ttu-id="77d99-158">นอกจากนี้ คุณยังสามารถจัดรูปแบบกล่องแสดงคำอธิบายตามเงื่อนไขซึ่งคุณสามารถดำเนินการกับปุ่มประเภทอื่นได้</span><span class="sxs-lookup"><span data-stu-id="77d99-158">Additionally, you can conditionally format the tooltip as you can do with other button types.</span></span>

## <a name="set-the-navigation-destination-conditionally"></a><span data-ttu-id="77d99-159">ตั้งค่าปลายทางการนำทางตามเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="77d99-159">Set the navigation destination conditionally</span></span>

<span data-ttu-id="77d99-160">คุณสามารถใช้การจัดรูปแบบตามเงื่อนไขเพื่อตั้งค่าปลายทางการนำทาง ตามผลลัพธ์ของหน่วยวัดได้</span><span class="sxs-lookup"><span data-stu-id="77d99-160">You can use conditional formatting to set the navigation destination, based on the output of a measure.</span></span> <span data-ttu-id="77d99-161">ตัวอย่างเช่น คุณอาจต้องการประหยัดเนื้อที่บนพื้นที่รายงานของคุณ ด้วยการมีเพียงปุ่มเดียวที่ใช้เพื่อนำทางไปยังหน้าอื่นๆ ตามการเลือกของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="77d99-161">For example, you may want to save space on your report canvas by having a single button to navigate to different pages based on the user’s selection.</span></span>

:::image type="content" source="media/desktop-buttons/button-navigate-go.png" alt-text="นำทางด้วยปุ่ม ไป":::
 
<span data-ttu-id="77d99-163">หากต้องการสร้างตัวอย่างดังแสดงด้านบน ให้เริ่มต้นโดยสร้างตารางแบบคอลัมน์เดียวที่มีชื่อของปลายทางการนำทาง:</span><span class="sxs-lookup"><span data-stu-id="77d99-163">To create the example shown above, start by creating a single-column table with the names of the navigation destinations:</span></span>

:::image type="content" source="media/desktop-buttons/button-create-table.png" alt-text="สร้างตาราง":::

<span data-ttu-id="77d99-165">Power BI ใช้การจับคู่สตริงที่เหมือนกันเพื่อตั้งค่าปลายทางการเข้าถึงรายละเอียด ดังนั้นโปรดตรวจสอบให้แน่ใจว่าค่าที่ป้อนตรงกับชื่อหน้าการเข้าถึงรายละเอียดของคุณ</span><span class="sxs-lookup"><span data-stu-id="77d99-165">Power BI uses exact string match to set the drill-through destination, so double-check that the entered values exactly align with your drill-through page names.</span></span>

<span data-ttu-id="77d99-166">หลังจากที่คุณได้สร้างตารางแล้ว ให้เพิ่มตารางลงในหน้าเป็นตัวแบ่งส่วนข้อมูลแบบเลือกครั้งเดียว:</span><span class="sxs-lookup"><span data-stu-id="77d99-166">After you've created the table, add it to the page as a single-select slicer:</span></span>

:::image type="content" source="media/desktop-buttons/button-navigate-slicer.png" alt-text="ตัวแบ่งส่วนข้อมูลการนำทาง":::

<span data-ttu-id="77d99-168">จากนั้นสร้างปุ่มการนำทางไปยังหน้าและเลือกตัวเลือกการจัดรูปแบบตามเงื่อนไขสำหรับปลายทาง:</span><span class="sxs-lookup"><span data-stu-id="77d99-168">Then create a page navigation button and select the conditional formatting option for the destination:</span></span>

:::image type="content" source="media/desktop-buttons/button-set-page-nav-destination.png" alt-text="ปุ่มการนำทางไปยังหน้า":::
 
<span data-ttu-id="77d99-170">เลือกชื่อของคอลัมน์ที่คุณสร้างขึ้น ในกรณีนี้ **เลือกปลายทาง**:</span><span class="sxs-lookup"><span data-stu-id="77d99-170">Select the name of the column you created, in this case, **Select a destination**:</span></span>

:::image type="content" source="media/desktop-buttons/button-select-destination.png" alt-text="เลือกปลายทาง":::

<span data-ttu-id="77d99-172">ตอนนี้ปุ่มสามารถนำทางไปยังหน้าอื่นๆ ได้โดยขึ้นอยู่กับการเลือกของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="77d99-172">Now the button can navigate to different pages, depending on the user’s selection.</span></span>

:::image type="content" source="media/desktop-buttons/button-navigate-go.png" alt-text="นำทางด้วยปุ่ม ไป":::
 
### <a name="shapes-and-images-for-navigation"></a><span data-ttu-id="77d99-174">รูปร่างและรูปภาพสำหรับการนำทาง</span><span class="sxs-lookup"><span data-stu-id="77d99-174">Shapes and images for navigation</span></span>

<span data-ttu-id="77d99-175">การดำเนินการนำทางไปยังหน้าสามารถรองรับรูปร่างและรูปภาพได้ ไม่ใช่เพียงแค่ปุ่มเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="77d99-175">Page navigation action is supported for shapes and images, not just buttons.</span></span> <span data-ttu-id="77d99-176">ต่อไปนี้เป็นตัวอย่างที่ใช้หนึ่งในรูปร่างที่มีอยู่ภายใน:</span><span class="sxs-lookup"><span data-stu-id="77d99-176">Here’s an example using one of the built-in shapes:</span></span>

:::image type="content" source="media/desktop-buttons/button-navigation-arrow.png" alt-text="ใช้ลูกศรสำหรับการนำทาง":::
 
<span data-ttu-id="77d99-178">ต่อไปนี้คือตัวอย่างที่ใช้รูปภาพ:</span><span class="sxs-lookup"><span data-stu-id="77d99-178">Here’s an example using an image:</span></span>

:::image type="content" source="media/desktop-buttons/button-navigation-image.png" alt-text="ใช้รูปภาพสำหรับการนำทาง":::
 
## <a name="buttons-support-fill-images"></a><span data-ttu-id="77d99-180">ปุ่มรองรับรูปภาพแบบ Fill image</span><span class="sxs-lookup"><span data-stu-id="77d99-180">Buttons support fill images</span></span>

<span data-ttu-id="77d99-181">ปุ่มรองรับรูปภาพแบบ Fill image</span><span class="sxs-lookup"><span data-stu-id="77d99-181">Buttons support fill images.</span></span> <span data-ttu-id="77d99-182">คุณสามารถปรับแต่งรูปลักษณ์และสัมผัสของปุ่มของคุณด้วยรูปภาพแบบ Fill image ร่วมกับสถานะปุ่มที่มีอยู่ภายในได้: ตามค่าเริ่มต้น เมื่อเลื่อนเมาส์ เมื่อกด และปิดใช้งาน (สำหรับการเข้าถึงรายละเอียด)</span><span class="sxs-lookup"><span data-stu-id="77d99-182">You can customize the look and feel of your button with fill images combined with the built-in button states: default, on hover, on press, and disabled (for drill through).</span></span>

:::image type="content" source="media/desktop-drill-through-buttons/drill-through-fill-images.png" alt-text="รูปภาพแบบ Fill image ของปุ่มการเข้าถึงรายละเอียด":::

<span data-ttu-id="77d99-184">ตั้งค่า **Fill** เป็น **เปิด** จากนั้นสร้างรูปภาพสำหรับสถานะที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="77d99-184">Set **Fill** to **On**, then create images for the different states.</span></span>

:::image type="content" source="media/desktop-drill-through-buttons/drill-through-fill-state-settings.png" alt-text="การตั้งค่ารูปภาพแบบ Fill image":::


## <a name="next-steps"></a><span data-ttu-id="77d99-186">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="77d99-186">Next steps</span></span>
<span data-ttu-id="77d99-187">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ คุณลักษณะที่คล้ายกัน หรือการโต้ตอบกับปุ่ม โปรดดูที่บทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="77d99-187">For more information about features that are similar or interact with buttons, take a look at the following articles:</span></span>

* [<span data-ttu-id="77d99-188">ใช้การเข้าถึงรายละเอียดในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="77d99-188">Use drill through in Power BI reports</span></span>](desktop-drillthrough.md)
* [<span data-ttu-id="77d99-189">ใช้บุ๊กมาร์กเพื่อแชร์ข้อมูลเชิงลึก และสร้างเรื่องราวใน Power BI</span><span class="sxs-lookup"><span data-stu-id="77d99-189">Use bookmarks to share insights and build stories in Power BI</span></span>](desktop-bookmarks.md)
* [<span data-ttu-id="77d99-190">สร้างปุ่มการเข้าถึงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="77d99-190">Create a drill-through button</span></span>](desktop-drill-through-buttons.md)

