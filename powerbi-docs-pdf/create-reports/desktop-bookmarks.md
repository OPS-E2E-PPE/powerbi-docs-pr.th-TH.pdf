---
title: ใช้บุ๊กมาร์ก Power BI Desktop เพื่อแชร์ข้อมูลเชิงลึก และสร้างเรื่องราว
description: บุ๊กมาร์กใน Power BI Desktop ให้คุณบันทึกมุมมองและการตั้งค่าในรายงานของคุณ และสร้างงานนำเสนอที่เป็นเรื่องราว
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 05/06/2020
LocalizationGroup: Create reports
ms.openlocfilehash: b1d9be5515680a199a2ae74c59aa1baeb30ef1f1
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414495"
---
# <a name="create-bookmarks-in-power-bi-desktop-to-share-insights-and-build-stories"></a><span data-ttu-id="b20a2-103">สร้างบุ๊กมาร์ก Power BI Desktop เพื่อแชร์ข้อมูลเชิงลึก และสร้างเรื่องราว</span><span class="sxs-lookup"><span data-stu-id="b20a2-103">Create bookmarks in Power BI Desktop to share insights and build stories</span></span>
<span data-ttu-id="b20a2-104">ด้วย *บุ๊กมาร์ก* ใน Power BI Desktop คุณสามารถจับภาพมุมมองที่กำหนดค่าไว้ในปัจจุบันของหน้ารายงาน รวมถึงการกรองและสถานะของวิชวล</span><span class="sxs-lookup"><span data-stu-id="b20a2-104">With *bookmarks* in Power BI Desktop, you capture the currently configured view of a report page, including filtering and the state of visuals.</span></span> <span data-ttu-id="b20a2-105">หลังจากนั้น คุณสามารถกลับไปยังสถานะดังกล่าวโดยการเลือกบุ๊กมาร์กที่บันทึกไว้</span><span class="sxs-lookup"><span data-stu-id="b20a2-105">Later, you can go back to that state by selecting the saved bookmark.</span></span> 

<span data-ttu-id="b20a2-106">นอกจากนี้คุณยังสามารถสร้างคอลเลกชันของบุ๊กมาร์ก จัดเรียงรายการต่าง ๆ ในลำดับที่คุณต้องการ และหลังจากนั้น คุณสามารถไปยังทีละบุ๊กมาร์กในงานนำเสนอเพื่อไฮไลต์ชุดข้อมูลเชิงลึก หรือเรื่องราวที่คุณต้องการบอกด้วยวิชวลและรายงานของคุณได้</span><span class="sxs-lookup"><span data-stu-id="b20a2-106">You can also create a collection of bookmarks, arrange them in the order you want, and later step through each bookmark in a presentation to highlight a series of insights, or the story you want to tell with your visuals and reports.</span></span> 

![บุ๊กมาร์กใน Power BI](media/desktop-bookmarks/bookmarks_01.png)

<span data-ttu-id="b20a2-108">บุ๊กมาร์กสามารถใช้งานได้หลายทาง</span><span class="sxs-lookup"><span data-stu-id="b20a2-108">There are many uses for bookmarking.</span></span> <span data-ttu-id="b20a2-109">ตัวอย่างเช่น คุณสามารถใช้บุ๊กมาร์กเพื่อติดตามความคืบหน้าของคุณเองในการสร้างรายงาน (บุ๊กมาร์ก เพิ่ม ลบ และเปลี่ยนชื่อง่าย) และคุณสามารถสร้างบุ๊กมาร์กเพื่อสร้างงานนำเสนอที่คล้ายกับ PowerPoint โดยการไปยังบุ๊กมาร์กต่าง ๆ ตามลำดับ เพื่อบอกเล่าเรื่องราวรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="b20a2-109">For example, you can use bookmarks to keep track of your own progress in creating reports (bookmarks are easy to add, delete, and rename) and you can create bookmarks to build a PowerPoint-like presentation that steps through bookmarks in order, thereby telling a story with your report.</span></span> 

> [!TIP]
> <span data-ttu-id="b20a2-110">สำหรับข้อมูลเกี่ยวกับการใช้บุ๊กมาร์กส่วนบุคคลในบริการของ Power BI โปรดดู[การประกาศเกี่ยวกับบุ๊กมาร์กส่วนบุคคลในบริการของ Power BI](https://powerbi.microsoft.com/blog/announcing-personal-bookmarks-in-the-power-bi-service/)</span><span class="sxs-lookup"><span data-stu-id="b20a2-110">For information about using personal bookmarks in the Power BI service, see [Announcing personal bookmarks in the Power BI Service](https://powerbi.microsoft.com/blog/announcing-personal-bookmarks-in-the-power-bi-service/).</span></span> 

## <a name="using-bookmarks"></a><span data-ttu-id="b20a2-111">การใช้บุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="b20a2-111">Using bookmarks</span></span>
<span data-ttu-id="b20a2-112">เพื่อใช้บุ๊กมาร์ก เลือกแท็บ **มุมมอง** จากริบบอน Power BI Desktop จากนั้นเลือก **บานหน้าต่างบุ๊กมาร์ก**</span><span class="sxs-lookup"><span data-stu-id="b20a2-112">To use bookmarks, select the **View** tab from the Power BI Desktop ribbon, then select **Bookmarks Pane**.</span></span> 

![เปิดบานหน้าต่างบุ๊กมาร์ก](media/desktop-bookmarks/bookmarks_03.png)

<span data-ttu-id="b20a2-114">เมื่อคุณสร้างบุ๊กมาร์ก องค์ประกอบต่อไปนี้จะถูกบันทึกพร้อมบุ๊กมาร์ก:</span><span class="sxs-lookup"><span data-stu-id="b20a2-114">When you create a bookmark, the following elements are saved with the bookmark:</span></span>

* <span data-ttu-id="b20a2-115">หน้าปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b20a2-115">The current page</span></span>
* <span data-ttu-id="b20a2-116">ตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="b20a2-116">Filters</span></span>
* <span data-ttu-id="b20a2-117">ตัวแบ่งส่วนข้อมูล รวมถึงชนิดตัวแบ่งส่วนข้อมูล (เช่น รายการดรอปดาวน์หรือรายการ) และสถานะของตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b20a2-117">Slicers, including slicer type (for example, dropdown or list) and slicer state</span></span>
* <span data-ttu-id="b20a2-118">สถานะการเลือกการแสดงผลด้วยภาพ (เช่น ตัวกรองการไฮไลต์เชื่อมโยง)</span><span class="sxs-lookup"><span data-stu-id="b20a2-118">Visual selection state (such as cross-highlight filters)</span></span>
* <span data-ttu-id="b20a2-119">ลำดับการจัดเรียง</span><span class="sxs-lookup"><span data-stu-id="b20a2-119">Sort order</span></span>
* <span data-ttu-id="b20a2-120">ตำแหน่งที่ดูรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="b20a2-120">Drill location</span></span>
* <span data-ttu-id="b20a2-121">การแสดงผลวัตถุ (โดยใช้บานหน้าต่าง **การเลือก**)</span><span class="sxs-lookup"><span data-stu-id="b20a2-121">Visibility of an object (by using the **Selection** pane)</span></span>
* <span data-ttu-id="b20a2-122">โหมดโฟกัส หรือ **สปอตไลต์** ของวัตถุใด ๆ ที่มองเห็นได้</span><span class="sxs-lookup"><span data-stu-id="b20a2-122">The focus or **Spotlight** modes of any visible object</span></span>

<span data-ttu-id="b20a2-123">กำหนดค่าหน้ารายงานตามที่คุณต้องการให้ปรากฏในบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="b20a2-123">Configure a report page as you want it to appear in the bookmark.</span></span> <span data-ttu-id="b20a2-124">หลังจากนั้น หน้ารายงานของคุณและวิชวลถูกจัดเรียงในแบบที่คุณต้องการแล้ว เลือก **เพิ่ม** จากบานหน้าต่าง **บุ๊กมาร์ก** เพื่อเพิ่มบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="b20a2-124">After your report page and visuals are arranged how you want them, select **Add** from the **Bookmarks** pane to add a bookmark.</span></span> 

![เพิ่มบุ๊กมาร์ก](media/desktop-bookmarks/bookmarks_04.png)

<span data-ttu-id="b20a2-126">Power BI Desktop สร้างบุ๊กมาร์ก และให้ตั้งชื่อทั่วไป</span><span class="sxs-lookup"><span data-stu-id="b20a2-126">Power BI Desktop creates a bookmark and gives it a generic name.</span></span> <span data-ttu-id="b20a2-127">คุณสามารถ **เปลี่ยนชื่อ** **ลบ** หรือ **อัปเดด** บุ๊กมาร์ก ได้อย่างง่ายดายโดยการเลือกจุดไข่ปลาที่อยู่ถัดจากชื่อบุ๊กมาร์ก จากนั้นเลือกการดำเนินการจากเมนูที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="b20a2-127">You can easily **Rename**, **Delete**, or **Update** a bookmark by selecting the ellipsis next to the bookmark's name, then selecting an action from the menu that appears.</span></span>

![เลือกเมนูบุ๊กมาร์กโดยใช้จุดไข่ปลา](media/desktop-bookmarks/bookmarks_05.png)

<span data-ttu-id="b20a2-129">หลังจากที่คุณได้สร้างบุ๊กมาร์กแล้ว ให้แสดงโดยการเลือกในบานหน้าต่าง **บุ๊กมาร์ก**</span><span class="sxs-lookup"><span data-stu-id="b20a2-129">After you've created a bookmark, display it by selecting it in the **Bookmarks** pane.</span></span> 

<span data-ttu-id="b20a2-130">นอกจากนี้ คุณยังสามารถเลือกบุ๊กมาร์กแต่ละรายการที่จะใช้กับคุณสมบัติ **ข้อมูล** เช่น ตัวกรอง และตัวแบ่งส่วนข้อมูล, คุณสมบัติ **แสดงผล** เช่น สปอตไลต์ และการแสดงผล รวมถึงการเปลี่ยนแปลง **หน้าปัจจุบัน** ซึ่งแสดงหน้าที่มองเห็นเมื่อเพิ่มบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="b20a2-130">You can also select whether each bookmark will apply **Data** properties, such as filters and slicers; **Display** properties, such as spotlight and its visibility; and **Current page** changes, which present the page that was visible when the bookmark was added.</span></span> <span data-ttu-id="b20a2-131">ความสามารถนี้มีประโยชน์ เมื่อคุณใช้บุ๊กมาร์กเพื่อสลับระหว่างมุมมองรายงานหรือการเลือกวิชวล ซึ่งในกรณีนี้คุณจะต้องการปิดคุณสมบัติของข้อมูล เพื่อให้ตัวกรองไม่ถูกตั้งค่าใหม่เมื่อผู้ใช้งานเปลี่ยนมุมมองโดยการเลือกบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="b20a2-131">These capabilities are useful when you use bookmarks to switch between report views or selections of visuals, in which case you'd likely want to turn off data properties, so that filters aren't reset when users switch views by selecting a bookmark.</span></span> 

<span data-ttu-id="b20a2-132">เพื่อเปลี่ยนแปลงดังกล่าว เลือกที่จุดไข่ปลาที่อยู่ถัดจากชื่อบุ๊กมาร์ก จากนั้นเลือกหรือยกเลิกการเลือกเครื่องหมายที่อยู่ถัดจาก **ข้อมูล**, **การแสดงผล** และตัวควบคุมอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="b20a2-132">To make such changes, select the ellipsis next to the bookmark's name, then select or unselect the checkmarks next to **Data**, **Display**, and other controls.</span></span> 

## <a name="arranging-bookmarks"></a><span data-ttu-id="b20a2-133">การจัดเรียงบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="b20a2-133">Arranging bookmarks</span></span>
<span data-ttu-id="b20a2-134">เมื่อคุณสร้างบุ๊กมาร์ก คุณอาจพบว่าลำดับที่คุณสร้างขึ้นแตกต่างจากลำดับที่คุณต้องการนำเสนอให้กับผู้ชมของคุณ</span><span class="sxs-lookup"><span data-stu-id="b20a2-134">As you create bookmarks, you might find that the order in which you create them is different from the order you'd like to present to your audience.</span></span> <span data-ttu-id="b20a2-135">ไม่เป็นไร คุณสามารถเรียงลำดับบุ๊กมาร์กใหม่ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="b20a2-135">No problem, you can easily rearrange the order of bookmarks.</span></span>

- <span data-ttu-id="b20a2-136">ในบานหน้าต่าง **บุ๊กมาร์ก** ลากแล้วปล่อยบุ๊กมาร์กเพื่อเปลี่ยนลำดับ</span><span class="sxs-lookup"><span data-stu-id="b20a2-136">In the **Bookmarks** pane, drag-and-drop bookmarks to change their order.</span></span> 

   <span data-ttu-id="b20a2-137">แถบสีเหลืองระหว่างบุ๊กมาร์ก แสดงตำแหน่งที่บุ๊กมาร์กที่กำลังลากจะถูกวาง</span><span class="sxs-lookup"><span data-stu-id="b20a2-137">The yellow bar between bookmarks designates where the dragged bookmark will be placed.</span></span>

   ![เปลี่ยนลำดับบุ๊กมาร์ก โดยการลากและปล่อย](media/desktop-bookmarks/bookmarks_06.png)

<span data-ttu-id="b20a2-139">ลำดับของบุ๊กมาร์กเป็นเรื่องสำคัญ เมื่อคุณใช้คุณลักษณะ **มุมมอง** ของบุ๊กมาร์ก ตามที่จะอธิบายในส่วนถัดไปได้</span><span class="sxs-lookup"><span data-stu-id="b20a2-139">The order of your bookmarks can be important when you use the **View** feature of bookmarks, as described in the next section.</span></span>

## <a name="bookmarks-as-a-slide-show"></a><span data-ttu-id="b20a2-140">ใช้บุ๊กมาร์กนำเสนอภาพนิ่ง</span><span class="sxs-lookup"><span data-stu-id="b20a2-140">Bookmarks as a slide show</span></span>
<span data-ttu-id="b20a2-141">เมื่อคุณมีคอลเลกชันบุ๊กมาร์ก ที่คุณต้องการนำเสนอตามลำดับ คุณสามารถเลือก **มุมมอง** จากบานหน้าต่าง **บุ๊กมาร์ก** เพื่อเริ่มการนำเสนอภาพนิ่ง</span><span class="sxs-lookup"><span data-stu-id="b20a2-141">When you have a collection of bookmarks you would like to present, in order, you can select **View** from the **Bookmarks** pane to begin a slideshow.</span></span>

<span data-ttu-id="b20a2-142">เมื่ออยู่ในโหมด **มุมมอง** มีบางคุณสมบัติที่สังเกตได้</span><span class="sxs-lookup"><span data-stu-id="b20a2-142">When in **View** mode, there are some features to notice.</span></span>

   ![คุณลักษณะ แถบชื่อเรื่องบุ๊กมาร์ก](media/desktop-bookmarks/bookmarks_07.png)

1. <span data-ttu-id="b20a2-144">ชื่อบุ๊กมาร์กปรากฏในแถบชื่อเรื่องบุ๊กมาร์ก ซึ่งอยู่ด้านล่างของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="b20a2-144">The name of the bookmark appears in the bookmark title bar, which appears at the bottom of the canvas.</span></span>

2. <span data-ttu-id="b20a2-145">แถบชื่อเรื่องบุ๊กมาร์ก มีลูกศรที่ช่วยให้คุณสามารถไปยังบุ๊กมาร์กถัดไป หรือก่อนหน้าได้</span><span class="sxs-lookup"><span data-stu-id="b20a2-145">The bookmark title bar has arrows that let you move to the next or previous bookmark.</span></span>

3. <span data-ttu-id="b20a2-146">คุณสามารถออกจากโหมด **มุมมอง** โดยการเลือก **ออกจาก** จากบานหน้าต่าง **บุ๊กมาร์ก** หรือโดยการเลือก **X** ในแถบชื่อเรื่องบุ๊กมาร์กได้</span><span class="sxs-lookup"><span data-stu-id="b20a2-146">You can exit **View** mode by selecting **Exit** from the **Bookmarks** pane or by selecting the **X** on the bookmark title bar.</span></span> 

<span data-ttu-id="b20a2-147">เมื่อคุณอยู่ในโหมด **มุมมอง** คุณสามารถปิดบานหน้าต่าง **บุ๊กมาร์ก** โดยการคลิก **X** บนบานหน้าต่างนั้นเพื่อให้มีพื้นที่เพิ่มเติมสำหรับงานนำเสนอของคุณได้</span><span class="sxs-lookup"><span data-stu-id="b20a2-147">When you're in **View** mode, you can close the **Bookmarks** pane, by selecting the **X** on that pane, to provide more space for your presentation.</span></span> <span data-ttu-id="b20a2-148">วิชวลทั้งหมดเป็นแบบโต้ตอบเมื่ออยู่ในโหมด **มุมมอง** และพร้อมสำหรับการไฮไลต์แบบเชื่อมโยง เช่นเดียวกับทีโต้ตอบกับวิชวลเหล่านั้นโดยตรง</span><span class="sxs-lookup"><span data-stu-id="b20a2-148">All visuals are interactive when they're in **View** mode and available for cross-highlighting, just as they would be when you interact directly with them.</span></span> 

## <a name="visibility-using-the-selection-pane"></a><span data-ttu-id="b20a2-149">การมองเห็น: การใช้งานบานหน้าต่างการเลือก</span><span class="sxs-lookup"><span data-stu-id="b20a2-149">Visibility: Using the Selection pane</span></span>
<span data-ttu-id="b20a2-150">เกี่ยวกับบานหน้าต่าง **บุ๊กมาร์ก** บานหน้าต่าง **การเลือก** แสดงรายการของวัตถุทั้งหมดบนหน้าปัจจุบัน และช่วยให้คุณสามารถเลือกวัตถุ และระบุว่าสามารถมองเห็นวัตถุได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="b20a2-150">Related to the **Bookmarks** pane, the **Selection** pane provides a list of all objects on the current page and allows you to select an object and specify whether it's visible.</span></span> 

![เปิดใช้งานบานหน้าต่างการเลือก](media/desktop-bookmarks/bookmarks_08.png)

<span data-ttu-id="b20a2-152">ในบานหน้าต่าง **การเลือก** คุณเลือกวัตถุและสลับว่าวัตถุสามารถมองเห็นได้หรือไม่ โดยการเลือกไอคอนรูปตาทางด้านขวาของวัตถุ</span><span class="sxs-lookup"><span data-stu-id="b20a2-152">In the **Selection** pane, you select an object and toggle whether the object is currently visible by selecting the eye icon to the right of the object.</span></span> 

![บานหน้าต่างการเลือก](media/desktop-bookmarks/bookmarks_09.png)

<span data-ttu-id="b20a2-154">เมื่อคุณเพิ่มบุ๊กมาร์ก สถานะการมองเห็นของแต่ละวัตถุจะถูกบันทึกโดยยึดตามการตั้งค่าในบานหน้าต่าง **การเลือก**</span><span class="sxs-lookup"><span data-stu-id="b20a2-154">When you add a bookmark, the visibility status of each object is also saved, based on its setting in the **Selection** pane.</span></span> 

<span data-ttu-id="b20a2-155">สิ่งสำคัญที่ต้องทราบคือตัวแบ่งส่วนข้อมูลยังคงกรองหน้ารายงาน โดยไม่คำนึงถึงว่าตัวแบ่งส่วนข้อมูลจะมองเห็นได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="b20a2-155">It's important to note that slicers continue to filter a report page, regardless of whether they're visible.</span></span> <span data-ttu-id="b20a2-156">ด้วยเหตุนี้ คุณสามารถสร้างบุ๊กมาร์กจำนวนมาก โดยมีการตั้งค่าตัวแบ่งส่วนข้อมูลที่แตกต่างกัน และทำให้หน้ารายงานดูแตกต่างกันได้ (และไฮไลต์ข้อมูลเชิงลึกที่แตกต่างกัน) ในแต่ละบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="b20a2-156">As such, you can create many different bookmarks, with different slicer settings, and make a single report page appear different (and highlight different insights) in various bookmarks.</span></span>

> [!NOTE]
> <span data-ttu-id="b20a2-157">เมื่อใช้บานหน้าต่าง **การเลือก** ร่วมกับบุ๊กมาร์ก และเปลี่ยนการมองเห็นของการเลือก จะส่งผลในการมองเห็นที่จะย้อนกลับไปยังการตั้งค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b20a2-157">When using the **Selection** pane in combination with bookmarks, changing the visibility of a selection results in its visibility reverting to the default setting.</span></span> <span data-ttu-id="b20a2-158">หลังจากทำการเปลี่ยนแปลงดังกล่าวแล้ว คุณสามารถคลิกขวาที่บุ๊กมาร์กและเลือก *อัปเดต* เพื่ออัปเดตการมองเห็นได้</span><span class="sxs-lookup"><span data-stu-id="b20a2-158">After making such changes, you can right-click a bookmark and select *update* to update its visibility.</span></span>


## <a name="bookmarks-for-shapes-and-images"></a><span data-ttu-id="b20a2-159">บุ๊กมาร์กสำหรับรูปร่างและรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="b20a2-159">Bookmarks for shapes and images</span></span>
<span data-ttu-id="b20a2-160">คุณยังสามารถเชื่อมโยงรูปร่างและรูปภาพไปยังบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="b20a2-160">You can also link shapes and images to bookmarks.</span></span> <span data-ttu-id="b20a2-161">ด้วยคุณลักษณะนี้ เมื่อคุณเลือกที่วัตถุ จะแสดงบุ๊กมาร์กที่เชื่อมโยงกับวัตถุนั้น</span><span class="sxs-lookup"><span data-stu-id="b20a2-161">With this feature, when you select an object, it shows the bookmark associated with that object.</span></span> <span data-ttu-id="b20a2-162">คุณลักษณะนี้จะมีประโยชน์โดยเฉพาะอย่างยิ่งเมื่อคุณทำงานกับปุ่ม</span><span class="sxs-lookup"><span data-stu-id="b20a2-162">This feature can be especially useful when you work with buttons.</span></span> <span data-ttu-id="b20a2-163">สำหรับข้อมูลเพิ่มเติม ให้ดู [การใช้ปุ่มใน Power BI](desktop-buttons.md)</span><span class="sxs-lookup"><span data-stu-id="b20a2-163">For more information, see [Using buttons in Power BI](desktop-buttons.md).</span></span> 

<span data-ttu-id="b20a2-164">วิธีการกำหนดบุ๊กมาร์กสำหรับวัตถุ:</span><span class="sxs-lookup"><span data-stu-id="b20a2-164">To assign a bookmark to an object:</span></span> 

1. <span data-ttu-id="b20a2-165">เลือกวัตถุในพื้นที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="b20a2-165">Select the object in the report canvas.</span></span> <span data-ttu-id="b20a2-166">แล้วจากบานหน้าต่าง **จัดรูปแบบรูปร่าง** ที่ปรากฏขึ้น ให้เปลี่ยนแถบเลื่อน **การดำเนินการ** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="b20a2-166">Then, from the **Format Shape** pane that appears, turn the **Action** slider to **On**.</span></span>

2. <span data-ttu-id="b20a2-167">ขยายส่วน **การดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="b20a2-167">Expand the **Action** section.</span></span> <span data-ttu-id="b20a2-168">ภายใต้ **ชนิด** เลือก **บุ๊กมาร์ก**</span><span class="sxs-lookup"><span data-stu-id="b20a2-168">Under **Type**, select **Bookmark**.</span></span>

3. <span data-ttu-id="b20a2-169">ภายใต้ **บุ๊กมาร์ก** เลือกบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="b20a2-169">Under **Bookmarks**, select a bookmark.</span></span>

   ![เพิ่มลิงค์บุ๊กมาร์กให้กับวัตถุ](media/desktop-bookmarks/bookmarks_10.png)

<span data-ttu-id="b20a2-171">มีหลายสิ่งที่น่าสนใจ ที่คุณสามารถทำได้ ด้วยการเชื่อมโยงจากวัตถุไปเป็นบุ๊กมาร์กได้</span><span class="sxs-lookup"><span data-stu-id="b20a2-171">There are all sorts of interesting things you can do with object-linked bookmarking.</span></span> <span data-ttu-id="b20a2-172">คุณสามารถสร้างสารบัญวิชวลบนหน้ารายงานของคุณ หรือคุณสามารถกำหนดมุมมองต่าง ๆ (เช่น ชนิดของวิชวล) ของข้อมูลเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="b20a2-172">You can create a visual table of contents on your report page, or you can provide different views (such as visual types) of the same information.</span></span>

<span data-ttu-id="b20a2-173">เมื่อคุณอยู่ในโหมดการแก้ไข ให้กด **Ctrl** และเลือกลิงก์เพื่อติดตาม</span><span class="sxs-lookup"><span data-stu-id="b20a2-173">When you're in editing mode, press **Ctrl** and select the link to follow it.</span></span> <span data-ttu-id="b20a2-174">เมื่อคุณไม่ได้อยู่ในโหมดการแก้ไข ให้เลือกวัตถุที่จะทำตามการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="b20a2-174">When you're not in editing mode, select the object to follow the link.</span></span> 

## <a name="bookmark-groups"></a><span data-ttu-id="b20a2-175">กลุ่มบุ๊คมาร์ก</span><span class="sxs-lookup"><span data-stu-id="b20a2-175">Bookmark groups</span></span>

<span data-ttu-id="b20a2-176">เริ่มด้วย Power BI Desktop รุ่นเดือนสิงหาคม 2018 คุณจะสามารถสร้างและใช้กลุ่มบุ๊กมาร์กได้</span><span class="sxs-lookup"><span data-stu-id="b20a2-176">Beginning with the August 2018 release of Power BI Desktop, you can create and use bookmark groups.</span></span> <span data-ttu-id="b20a2-177">กลุ่มบุ๊คมาร์กเป็นคอลเลกชันของบุ๊กมาร์กที่คุณระบุ ซึ่งสามารถแสดง และจัดระเบียบเป็นกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="b20a2-177">A bookmark group is a collection of bookmarks that you specify, which can be shown and organized as a group.</span></span> 

<span data-ttu-id="b20a2-178">วิธีการสร้างกลุ่มบุ๊กมาร์ก:</span><span class="sxs-lookup"><span data-stu-id="b20a2-178">To create a bookmark group:</span></span> 
1. <span data-ttu-id="b20a2-179">กด **Ctrl** และเลือกบุ๊กมาร์กที่คุณต้องการรวมไว้ในกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="b20a2-179">Press **Ctrl** and select the bookmarks you want to include in the group.</span></span> 

2. <span data-ttu-id="b20a2-180">เลือกจุดไข่ปลาถัดจากบุ๊กมาร์กที่คุณเลือก จากนั้นเลือก **กลุ่ม** จากเมนูที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="b20a2-180">Select the ellipsis next to your selected bookmarks, and then select **Group** from the menu that appears.</span></span>

   ![สร้างกลุ่มบุ๊คมาร์ก](media/desktop-bookmarks/bookmarks_15.png)

<span data-ttu-id="b20a2-182">Power BI Desktop จะตั้งชื่อกลุ่ม *กลุ่ม 1* โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b20a2-182">Power BI Desktop automatically names the group *Group 1*.</span></span> <span data-ttu-id="b20a2-183">คุณสามารถเลือกจุดไข่ปลาที่อยู่ถัดจากชื่อนี้ได้ เลือก **เปลี่ยนชื่อ** และเปลี่ยนชื่อเป็นสิ่งที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="b20a2-183">You can select the ellipsis next to this name, select **Rename**, and rename it to whatever you want.</span></span>

![เปลี่ยนชื่อกลุ่มบุ๊คมาร์ก](media/desktop-bookmarks/bookmarks_16.png)

<span data-ttu-id="b20a2-185">ด้วยกลุ่มบุ๊กมาร์กใด ๆ การขยายชื่อของกลุ่มบุ๊กมาร์กจะขยาย หรือยุบกลุ่มของบุ๊กมาร์กเท่านั้น และไม่แสดงบุ๊กมาร์กด้วยตัวเอง</span><span class="sxs-lookup"><span data-stu-id="b20a2-185">As with any bookmark group, expanding the bookmark group's name only expands or collapses the group of bookmarks, and doesn't represent a bookmark by itself.</span></span> 

<span data-ttu-id="b20a2-186">เมื่อคุณใช้คุณลักษณะ **มุมมอง** ของบุ๊กมาร์ก รายละเอียดต่อไปนี้จะนำไปใช้:</span><span class="sxs-lookup"><span data-stu-id="b20a2-186">When you use the **View** feature of bookmarks, the following details apply:</span></span>

* <span data-ttu-id="b20a2-187">ถ้าบุ๊กมาร์กที่เลือกอยู่ในกลุ่มเมื่อคุณเลือก **มุมมอง** จากบุ๊กมาร์ก เฉพาะบุ๊กมาร์ก *ในกลุ่มนั้น* จะแสดงในเซสชันการดู</span><span class="sxs-lookup"><span data-stu-id="b20a2-187">If the selected bookmark is in a group when you select **View** from bookmarks, only the bookmarks *in that group* are shown in the viewing session.</span></span> 

* <span data-ttu-id="b20a2-188">ถ้าบุ๊กมาร์กที่เลือกไม่ได้อยู่ในกลุ่ม หรืออยู่ในระดับบนสุด (เช่น ชื่อกลุ่มบุ๊กมาร์ก) จากนั้นบุ๊กมาร์กทั้งหมดสำหรับทั้งรายงานจะแสดงขึ้นมา รวมถึงบุ๊กมาร์กในทุกกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="b20a2-188">If the selected bookmark isn't in a group, or is on the top level (such as the name of a bookmark group), then all bookmarks for the entire report are played, including bookmarks in any group.</span></span> 

<span data-ttu-id="b20a2-189">วิธีการยกเลิกการจัดกลุ่มบุ๊กมาร์ก:</span><span class="sxs-lookup"><span data-stu-id="b20a2-189">To ungroup bookmarks:</span></span> 
1. <span data-ttu-id="b20a2-190">เลือกบุ๊กมาร์กใด ๆ ในกลุ่มและเลือกจุดไข่ปลา</span><span class="sxs-lookup"><span data-stu-id="b20a2-190">Select any bookmark in a group and select the ellipsis.</span></span> 

2. <span data-ttu-id="b20a2-191">เลือก **ยกเลิกการจัดกลุ่ม** จากเมนูที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="b20a2-191">Select **Ungroup** from the menu that appears.</span></span>

   ![ยกเลิกจัดกลุ่มบุ๊คมาร์ก](media/desktop-bookmarks/bookmarks_17.png)

   <span data-ttu-id="b20a2-193">การเลือก **ยกเลิกการจัดกลุ่ม** สำหรับบุ๊กมาร์กใด ๆ จากกลุ่มจะลบบุ๊กมาร์กทั้งหมดออกจากกลุ่ม ซึ่งจะลบกลุ่ม แต่ไม่ใช่ตัวบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="b20a2-193">Selecting **Ungroup** for any bookmark from a group removes all bookmarks from the group; it deletes the group, but not the bookmarks themselves.</span></span> 

<span data-ttu-id="b20a2-194">วิธีการลบบุ๊กมาร์กเดี่ยวออกจากกลุ่ม:</span><span class="sxs-lookup"><span data-stu-id="b20a2-194">To remove a single bookmark from a group:</span></span> 
1. <span data-ttu-id="b20a2-195">**ยกเลิกการจัดกลุ่ม** สมาชิกใดก็ตามจากกลุ่มดังกล่าว ซึ่งจะลบกลุ่มทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b20a2-195">**Ungroup** any member from that group, which deletes the entire grouping.</span></span> 

2. <span data-ttu-id="b20a2-196">เลือกสมาชิกที่คุณต้องการในกลุ่มใหม่โดยการกด **Ctrl** และเลือกแต่ละบุ๊กมาร์กแล้วเลือก **จัดกลุ่ม** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="b20a2-196">Select the members you want in the new group by pressing **Ctrl** and selecting each bookmark, then and select **Group** again.</span></span> 


## <a name="using-spotlight"></a><span data-ttu-id="b20a2-197">การใช้สปอตไลต์</span><span class="sxs-lookup"><span data-stu-id="b20a2-197">Using spotlight</span></span>
<span data-ttu-id="b20a2-198">อีกคุณลักษณะที่เผยแพร่พร้อมกับบุ๊กมาร์กคือ *สปอตไลต์*</span><span class="sxs-lookup"><span data-stu-id="b20a2-198">Another feature released with bookmarks is *spotlight*.</span></span> <span data-ttu-id="b20a2-199">ด้วยสปอตไลต์ คุณสามารถดึงดูดความสนใจลงในเฉพาะแผนภูมิ เช่น เมื่อนำเสนอบุ๊กมาร์กของคุณในโหมด **มุมมอง** ได้</span><span class="sxs-lookup"><span data-stu-id="b20a2-199">With spotlight, you can draw attention to a specific chart, for example, when presenting your bookmarks in **View** mode.</span></span>

<span data-ttu-id="b20a2-200">เรามาเปรียบเทียบโหมดสปอตไลต์กับโหมดโฟกัส เพื่อดูความแตกต่างของทั้งสองโหมด</span><span class="sxs-lookup"><span data-stu-id="b20a2-200">Let's compare spotlight to focus mode to see how they differ:</span></span>

1. <span data-ttu-id="b20a2-201">ด้วยโหมดโฟกัส คุณเลือกไอคอน **โหมดโฟกัส** ของวิชวล ซึ่งทำให้วิชวลเติมพื้นที่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b20a2-201">With focus mode, you select the **Focus mode** icon of a visual, which causes the visual to fill the entire canvas.</span></span>

2. <span data-ttu-id="b20a2-202">ด้วยสปอตไลต์ คุณเลือก **สปอตไลต์** จากจุดไข่ปลาของวิชวลเพื่อเน้นหนึ่งวิชวลในขนาดเดิม ซึ่งทำให้เกิดวิชวลอื่น ๆ ทั้งหมดบนหน้าเพื่อให้ใกล้เคียงกับความโปร่งใส</span><span class="sxs-lookup"><span data-stu-id="b20a2-202">With spotlight, you select **Spotlight** from the ellipsis of a visual to highlight one visual in its original size, which causes all other visuals on the page to fade to near transparency.</span></span> 

![เปรียบเทียบโหมดสปอตไลต์กับโหมดโฟกัส](media/desktop-bookmarks/bookmarks_11.png)

<span data-ttu-id="b20a2-204">เมื่อคุณเลือกไอคอน **โหมดโฟกัส** ของวิชวลในรูปก่อนหน้านี้ หน้าจะปรากฏเป็นดังนี้:</span><span class="sxs-lookup"><span data-stu-id="b20a2-204">When you select the **Focus mode** icon of the visual in the previous image, the page appears as follows:</span></span>

![โหมดโฟกัส](media/desktop-bookmarks/bookmarks_12.png)

<span data-ttu-id="b20a2-206">ในทางตรงข้าม เมื่อ **สปอตไลต์** ถูกเลือกจากเมนูจุดไข่ปลาของวิชวล หน้าจะปรากฎเป็นดังนี้:</span><span class="sxs-lookup"><span data-stu-id="b20a2-206">In contrast, when **Spotlight** is selected from the visual's ellipsis menu, the page appears as follows:</span></span>

![โหมดสปอตไลต์](media/desktop-bookmarks/bookmarks_13.png)

<span data-ttu-id="b20a2-208">ถ้าเลือกโหมดโฟกัสหรือสปอตไลต์เมื่อคุณเพิ่มบุ๊กมาร์ก โหมดดังกล่าวจะถูกเก็บไว้ในบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="b20a2-208">If either the focus or spotlight mode is selected when you add a bookmark, that mode is retained in the bookmark.</span></span>

## <a name="bookmarks-in-the-power-bi-service"></a><span data-ttu-id="b20a2-209">บุ๊กมาร์กในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="b20a2-209">Bookmarks in the Power BI service</span></span>
<span data-ttu-id="b20a2-210">เมื่อคุณเผยแพร่รายงานไปยังบริการของ Power BI ที่มีอย่างน้อยหนึ่งบุ๊กมาร์ก คุณสามารถดูและโต้ตอบกับบุ๊กมาร์กเหล่านั้นในบริการของ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="b20a2-210">When you publish a report to the Power BI service with at least one bookmark, you can view and interact with those bookmarks in the Power BI service.</span></span> <span data-ttu-id="b20a2-211">เมื่อบุ๊กมาร์กพร้อมใช้งานในรายงาน คุณจะแสดงบานหน้าต่าง **การเลือก** และ **บุ๊กมาร์ก** โดยการเลือก **มุมมอง** > **บานหน้าต่างการเลือก** หรือ **มุมมอง** > **บานหน้าต่างบุ๊กมาร์ก**</span><span class="sxs-lookup"><span data-stu-id="b20a2-211">When bookmarks are available in a report, you display the **Selection** and **Bookmarks** panes by selecting **View** > **Selection pane** or **View** > **Bookmarks pane**.</span></span> 

![ดูบานหน้าต่างบุ๊กมาร์ก และการเลือก ในบริการของ Power BI](media/desktop-bookmarks/bookmarks_14.png)

<span data-ttu-id="b20a2-213">ในบริการของ Power BI บานหน้าต่าง **บุ๊กมาร์ก** จะทำงานเหมือนกับที่ทำงานใน Power BI Desktop รวมไปถึงความสามารถในการเลือก **มุมมอง** เพื่อแสดงบุ๊กมาร์กของคุณตามลำดับ เหมือนกับการนำเสนอภาพนิ่ง</span><span class="sxs-lookup"><span data-stu-id="b20a2-213">In the Power BI service, the **Bookmarks** pane operates just as it does in Power BI Desktop, including the ability to select **View** to show your bookmarks in order, like a slide show.</span></span>

<span data-ttu-id="b20a2-214">ใช้แถบชื่อเรื่องบุ๊กมาร์กสีเทาแทนลูกศรสีดำเพื่อนำทางผ่านบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="b20a2-214">Use the gray bookmark title bar, instead of the black arrows, to navigate through the bookmarks.</span></span> <span data-ttu-id="b20a2-215">(ลูกศรสีดำย้ายคุณผ่านหน้ารายงาน ไม่ใช่บุ๊กมาร์ก)</span><span class="sxs-lookup"><span data-stu-id="b20a2-215">(The black arrows move you through report pages, not bookmarks.)</span></span>

## <a name="enable-the-bookmarks-preview-versions-prior-to-march-2018"></a><span data-ttu-id="b20a2-216">เปิดใช้งานตัวอย่าง บุ๊กมาร์ก (เวอร์ชันก่อนเดือนมีนาคม 2018)</span><span class="sxs-lookup"><span data-stu-id="b20a2-216">Enable the bookmarks preview (versions prior to March 2018)</span></span>
<span data-ttu-id="b20a2-217">เริ่มตั้งแต่เวอร์ชัน มีนาคม 2018 ของ Power BI Desktop บุ๊กมาร์กมีให้ใช้งานโดยทั่วไปแล้ว</span><span class="sxs-lookup"><span data-stu-id="b20a2-217">Beginning with the March 2018 version of Power BI Desktop, bookmarks are generally available.</span></span> 

<span data-ttu-id="b20a2-218">เราแนะนำให้คุณอัปเกรดเป็นการเผยแพร่ล่าสุดเสมอ</span><span class="sxs-lookup"><span data-stu-id="b20a2-218">We always suggest you upgrade to the most recent release.</span></span> <span data-ttu-id="b20a2-219">แต่ถ้าเวอร์ชัน Power BI Desktop ของคุณเป็นรุ่นก่อนหน้านั้น คุณยังสามารถลองคุณลักษณะบุ๊กมาร์ก เริ่มตั้งแต่รุ่นเดือนตุลาคม 2017 ของ Power BI Desktop และสำหรับรายงานที่เปิดใช้งานบุ๊กมาร์กใน บริการของ Power BI เช่นเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="b20a2-219">But, if your version of Power BI Desktop is earlier than that release, you can try the bookmarks feature beginning with the October 2017 release of Power BI Desktop, and for bookmark-enabled reports, in the Power BI service as well.</span></span> 

<span data-ttu-id="b20a2-220">วิธีการเปิดใช้งานคุณลักษณะบุ๊กมาร์กแสดงตัวอย่าง:</span><span class="sxs-lookup"><span data-stu-id="b20a2-220">To enable the preview bookmarks feature:</span></span> 

1. <span data-ttu-id="b20a2-221">เลือก **ไฟล์** > **ตัวเลือกและการตั้งค่า** > **ตัวเลือก** > **คุณลักษณะตัวอย่าง** แล้วเลือก **บุ๊กมาร์ก**</span><span class="sxs-lookup"><span data-stu-id="b20a2-221">Select **File** > **Options and Settings** > **Options** > **Preview Features**, then select **Bookmarks**.</span></span> 

   ![เปิดใช้งานบุ๊กมาร์กในหน้าต่างตัวเลือก](media/desktop-bookmarks/bookmarks_02.png)

2. <span data-ttu-id="b20a2-223">รีสตาร์ท Power BI Desktop เพื่อเปิดใช้งานเวอร์ชันตัวอย่างของบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="b20a2-223">Restart Power BI Desktop to enable the preview version of bookmarks.</span></span>

## <a name="limitations-and-considerations"></a><span data-ttu-id="b20a2-224">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="b20a2-224">Limitations and considerations</span></span>
<span data-ttu-id="b20a2-225">ในบุ๊กมาร์กรุ่นนี้ มีข้อจำกัดและข้อควรพิจารณาบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="b20a2-225">In this release of the bookmarks features, there are a few limitations and considerations to keep in mind.</span></span>

* <span data-ttu-id="b20a2-226">วิชวล Power BI ส่วนใหญ่ควรทำงานได้ดีกับการบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="b20a2-226">Most Power BI visuals should work well with bookmarking.</span></span> <span data-ttu-id="b20a2-227">อย่างไรก็ตาม ถ้าคุณพบปัญหาเกี่ยวกับการบุ๊กมาร์กและวิชวลแบบกำหนดเอง ให้ติดต่อผู้สร้างวิชวลนั้น และขอให้พวกเขาจะเพิ่มการสนับสนุนบุ๊กมาร์กในวิชวลของตน</span><span class="sxs-lookup"><span data-stu-id="b20a2-227">However, if you encounter problems with bookmarking and a custom visual, contact the creator of that custom visual and ask them to add support for bookmarks to their visual.</span></span> 
* <span data-ttu-id="b20a2-228">ถ้าคุณเพิ่มวิชวลบนหน้ารายงานหลังจากการสร้างบุ๊กมาร์ก วิชวลจะแสดงในสถานะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b20a2-228">If you add a visual on a report page after creating a bookmark, the visual is displayed in its default state.</span></span> <span data-ttu-id="b20a2-229">นั่นคือถ้าคุณเพิ่มตัวแบ่งส่วนข้อมูลลงในหน้าที่คุณเคยสร้างบุ๊กมาร์กไว้ก่อน ตัวแบ่งส่วนข้อมูลจะทำงานในสถานะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b20a2-229">That is, if you introduce a slicer into a page where you previously created bookmarks, the slicer behaves in its default state.</span></span>
* <span data-ttu-id="b20a2-230">การย้ายวิชวลหลังจากการสร้างบุ๊กมาร์กแล้วจะมีผลในบุ๊กมาร์กโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b20a2-230">Moving a visual after a bookmark has been created is automatically reflected in the bookmark.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="b20a2-231">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="b20a2-231">Next steps</span></span>
<span data-ttu-id="b20a2-232">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะที่คล้ายกัน หรือการโต้ตอบกับบุ๊กมาร์ก โปรดดูที่บทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b20a2-232">For more information about features that are similar or interact with bookmarks, see the following articles:</span></span>

* [<span data-ttu-id="b20a2-233">ใช้ตัวเจาะเข้าถึงรายละเอียดใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="b20a2-233">Use drillthrough in Power BI Desktop</span></span>](desktop-drillthrough.md)
* [<span data-ttu-id="b20a2-234">แสดงไทล์แดชบอร์ดหรือวิชวลรายงานในโหมดโฟกัส</span><span class="sxs-lookup"><span data-stu-id="b20a2-234">Display a dashboard tile or report visual in focus mode</span></span>](../consumer/end-user-focus.md)
