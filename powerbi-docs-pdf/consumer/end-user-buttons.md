---
title: เรียนรู้วิธีการทำงานของปุ่มในบริการ Power BI
description: สามารถใช้ปุ่มเพื่อเปิดการดำเนินการต่าง ๆ ซึ่งรวมถึงการนำทางในรายงาน การเข้าถึงรายละเอียด และการเข้าถึงรายละเอียดแบบข้ามรายงาน
author: mihart
ms.author: mihart
ms.reviewer: mihart
ms.service: powerbi
ms.subservice: pbi-explore
ms.topic: how-to
ms.date: 12/21/2020
LocalizationGroup: Reports
ms.openlocfilehash: 140ca42dc34e98133beac5fff671cf1ef244501c
ms.sourcegitcommit: 0711972326521944fdd8572403c0b15f31b916da
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/22/2020
ms.locfileid: "97721443"
---
# <a name="buttons-in-the-power-bi-service"></a><span data-ttu-id="ac927-103">ปุ่มในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="ac927-103">Buttons in the Power BI service</span></span>
<span data-ttu-id="ac927-104">ในรายงานที่คุณได้รับจากเพื่อนร่วมงาน คุณอาจสังเกตเห็นปุ่มต่าง ๆ และสงสัยว่าจะใช้งานอย่างไร</span><span class="sxs-lookup"><span data-stu-id="ac927-104">In the reports that you receive from colleagues, you may have noticed buttons and wondered how to use them.</span></span> <span data-ttu-id="ac927-105">บางปุ่มมีคำศัพท์ บางปุ่มมีลูกศร บางปุ่มมีกราฟิก และบางปุ่มยังมีเมนูแบบดรอปดาวน์ด้วย</span><span class="sxs-lookup"><span data-stu-id="ac927-105">Some have words, some have arrows, others have graphics, and some even have dropdown menus.</span></span> <span data-ttu-id="ac927-106">บทความนี้จะสอนวิธีการรับรู้ปุ่มและวิธีการที่จะคิดออกว่าจะทำอย่างไรกับปุ่มดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="ac927-106">This article will teach you how to recognize a button and how to figure out what to do with it.</span></span>

## <a name="how-to-recognize-a-button"></a><span data-ttu-id="ac927-107">วิธีการรับรู้ปุ่ม</span><span class="sxs-lookup"><span data-stu-id="ac927-107">How to recognize a button</span></span>
<span data-ttu-id="ac927-108">ปุ่มสามารถมีลักษณะได้มากมาย เช่น รูปร่าง รูปภาพ หรือไอคอนในหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="ac927-108">Buttons can look a lot like shapes, images, or icons on a report page.</span></span> <span data-ttu-id="ac927-109">แต่ถ้ามีการดำเนินการเกิดขึ้นเมื่อคุณเลือก (คลิก) วัตถุดังกล่าว อาจเป็นไปได้ว่าวัตถุนั้นอาจเป็นปุ่ม</span><span class="sxs-lookup"><span data-stu-id="ac927-109">But if an action occurs when you select (click) it -- then it's probably a button.</span></span>

## <a name="types-of-buttons"></a><span data-ttu-id="ac927-110">ชนิดของปุ่ม</span><span class="sxs-lookup"><span data-stu-id="ac927-110">Types of buttons</span></span>
<span data-ttu-id="ac927-111">ผู้สร้างรายงานจะเพิ่มปุ่มในรายงานเพื่อช่วยให้คุณสามารถนำทางและสำรวจได้</span><span class="sxs-lookup"><span data-stu-id="ac927-111">Report creators add buttons to reports to help you with navigation and exploration.</span></span> <span data-ttu-id="ac927-112">ปุ่มบางประเภท ได้แก่ ย้อนกลับ บุ๊กมาร์ก ลูกศร ถามและ ตอบ วิธีใช้ และว่าง</span><span class="sxs-lookup"><span data-stu-id="ac927-112">Just some of the button types are: back, bookmark, arrows, Q&A, help, and blank.</span></span> 

### <a name="back-buttons"></a><span data-ttu-id="ac927-113">ปุ่ม ย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="ac927-113">Back buttons</span></span> 
<span data-ttu-id="ac927-114">ปุ่มย้อนกลับอาจมีไอคอนลูกศรและเมื่อคุณเลือกแล้ว Power BI จะนำคุณกลับไปที่หน้าก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="ac927-114">A back button may have an arrow icon and when you select it, Power BI takes you back to the previous page.</span></span>  <span data-ttu-id="ac927-115">ปุ่มย้อนกลับมักจะใช้กับการเข้าถึงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="ac927-115">Back buttons are often used with drillthrough.</span></span> <span data-ttu-id="ac927-116">นี่คือตัวอย่างของปุ่มย้อนกลับที่ใช้กับการดูรายละเอียดเจาะลึก</span><span class="sxs-lookup"><span data-stu-id="ac927-116">Here's an example of a back button used with drillthrough.</span></span>

1. <span data-ttu-id="ac927-117">ผู้ใช้ได้เลือก **Word** ในแผนภูมิแท่งและกำลังเจาะลึกถึง **การวิเคราะห์ตะกร้าตลาด**</span><span class="sxs-lookup"><span data-stu-id="ac927-117">The user has selected **Word** in the bar chart and is drilling through to  **Market basket analysis**.</span></span>

    ![สกรีนช็อตของปุ่ม เข้าถึงรายละเอียด](media/end-user-buttons/power-bi-drillthrough.png)

2. <span data-ttu-id="ac927-119">โดยการเลือก **การวิเคราะห์ตะกร้าสินค้า** Power BI จะเปิดหน้ารายงาน *การวิเคราะห์ตะกร้าสินค้า* และใช้การเลือกที่สร้างขึ้นบนหน้าต้นทางเพื่อกรองสิ่งที่จะแสดงบนหน้าปลายทาง</span><span class="sxs-lookup"><span data-stu-id="ac927-119">By choosing **Market basket analysis**, Power BI opens the *Market basket analysis* report page and uses the selections made on the source page to filter what is shown on the destination page.</span></span>

    ![สกรีนช็อตของปุ่ม ย้อนกลับ](media/end-user-buttons/power-bi-back.png)

    <span data-ttu-id="ac927-121">ตอนนี้คุณอยู่ในหน้ารายงาน **การวิเคราะห์ตะกร้าตลาด** ซึ่งถูกกรองสำหรับ **Word**</span><span class="sxs-lookup"><span data-stu-id="ac927-121">You're now on the **Market basket analysis** report page, which is filtered for **Word**.</span></span> <span data-ttu-id="ac927-122">หากต้องการกลับไปที่หน้าก่อนหน้านี้ให้เลือกปุ่มย้อนกลับที่มีข้อความว่า **ย้อนกลับ**</span><span class="sxs-lookup"><span data-stu-id="ac927-122">To return to the previous page, select the back button that is labeled **Go back**.</span></span> 

## <a name="bookmark-buttons"></a><span data-ttu-id="ac927-123">ปุ่ม บุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="ac927-123">Bookmark buttons</span></span>
<span data-ttu-id="ac927-124">รายงาน *นักออกแบบ* มักจะรวมบุ๊กมาร์กไว้ในรายงานของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="ac927-124">Report *designers* often include bookmarks with their reports.</span></span> <span data-ttu-id="ac927-125">คุณสามารถดูรายการบุ๊กมาร์กรายงานได้โดยเลือก **บุ๊กมาร์ก** จากมุมขวาบน</span><span class="sxs-lookup"><span data-stu-id="ac927-125">You can view the list of report bookmarks by selecting **Bookmarks** from the upper right corner.</span></span> <span data-ttu-id="ac927-126">เมื่อผู้ออกแบบรายงานเพิ่ม *ปุ่ม* บุ๊กมาร์ก ซึ่งเป็นเพียงอีกวิธีหนึ่งในการนำทางไปยังหน้ารายงานเฉพาะที่เกี่ยวข้องกับบุ๊กมาร์กนั้น</span><span class="sxs-lookup"><span data-stu-id="ac927-126">When a report designer adds a bookmark *button*, it's just an alternate way to navigate to the particular report page that's associated with that bookmark.</span></span> <span data-ttu-id="ac927-127">หน้านี้จะมีตัวกรองและการตั้งค่าที่ใช้งานอยู่ ซึ่งคั่นหน้าด้วยบุ๊กมาร์ก</span><span class="sxs-lookup"><span data-stu-id="ac927-127">The page will have the applied filters and settings that are captured by the bookmark.</span></span> <span data-ttu-id="ac927-128">[เรียนรู้เพิ่มเติมเกี่ยวกับบุ๊กมาร์กใน Power BI](end-user-bookmarks.md)</span><span class="sxs-lookup"><span data-stu-id="ac927-128">[Learn more about bookmarks in Power BI](end-user-bookmarks.md).</span></span> 

<span data-ttu-id="ac927-129">ในตัวอย่างนี้ ปุ่มมีไอคอนบุ๊กมาร์กและชื่อของบุ๊กมาร์ก คือ *เมือง*</span><span class="sxs-lookup"><span data-stu-id="ac927-129">In this example, the button has a bookmark icon and the name of the bookmark, *Urban*.</span></span> 

![ภาพหน้าจอของปุ่ม บุ๊กมาร์ก](media/end-user-buttons/power-bi-bookmark.png)

<span data-ttu-id="ac927-131">เมื่อเลือกปุ่มบุ๊กมาร์ก Power BI จะนำคุณไปยังตำแหน่งที่ตั้งและการตั้งค่าตามที่กำหนดไว้สำหรับบุ๊กมาร์กนั้น</span><span class="sxs-lookup"><span data-stu-id="ac927-131">By choosing the bookmark button, Power BI takes you to the location and settings as defined for that bookmark.</span></span>  <span data-ttu-id="ac927-132">ในกรณีนี้ บุ๊กมาร์กอยู่บนหน้ารายงาน *โอกาสการเติบโต* และหน้านั้นจะถูกกรองข้ามสำหรับ **เมือง**</span><span class="sxs-lookup"><span data-stu-id="ac927-132">In this case, the bookmark is on the *Growth opportunities* report page and that page is cross-filtered for **Urban**.</span></span>

![ภาพหน้าจอของหน้ารายงานที่ถูกกรองสำหรับเมือง](media/end-user-buttons/power-bi-urban.png)


## <a name="drillthrough-buttons"></a><span data-ttu-id="ac927-134">ปุ่มการเข้าถึงรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="ac927-134">Drillthrough buttons</span></span>
<span data-ttu-id="ac927-135">มีแนวทางสองวิธีในการเจาะลึกรายละเอียดผ่านในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="ac927-135">There are two ways to drill through in the Power BI service.</span></span> <span data-ttu-id="ac927-136">การเข้าถึงรายละเอียดจะนำคุณไปยังหน้ารายงานอื่นและข้อมูลในหน้าปลายทางนั้นจะแสดงตามตัวกรองและการเลือกที่คุณได้ทำบนหน้าต้นทาง</span><span class="sxs-lookup"><span data-stu-id="ac927-136">Drillthrough takes you to a different report page and the data on that destination page is presented according to the filters and selections you've made on the source page.</span></span>

<span data-ttu-id="ac927-137">วิธีหนึ่งในการใช้การดูรายละเอียดเจาะลึกในรายงานคือคลิกขวาที่จุดข้อมูลในภาพเลือก **ดูข้อมูลรายละเอียด** และเลือกปลายทาง</span><span class="sxs-lookup"><span data-stu-id="ac927-137">One way to use drillthrough in a report is to right-click a data point in a visual, select **Drill through**, and choose the destination.</span></span> <span data-ttu-id="ac927-138">วิธีการนี้อธิบายไว้ข้างต้นในส่วนที่ชื่อ **ปุ่มย้อนกลับ**</span><span class="sxs-lookup"><span data-stu-id="ac927-138">This method is described above in the section titled **Back button**.</span></span> <span data-ttu-id="ac927-139">แต่บางครั้งผู้ออกแบบรายงานใช้ *ปุ่ม* การเข้าถึงรายละเอียดแทน เพื่อให้การดำเนินการชัดเจนมากขึ้น และเรียกความสนใจไปยังข้อมูลเชิงลึกที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="ac927-139">But sometimes the report designers use a drillthrough *button* instead, to make the action more obvious and to call attention to important insights.</span></span>  

<span data-ttu-id="ac927-140">ปุ่ม การเข้าถึงรายละเอียด สามารถมีข้อกำหนดเบื้องต้นได้มากกว่าหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="ac927-140">Drillthrough buttons can have more than one prerequisite.</span></span> <span data-ttu-id="ac927-141">หากคุณไม่ปฏิบัติตามข้อกำหนดเบื้องต้นทั้งหมด ปุ่มจะไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="ac927-141">Unless you fulfill all the prerequisites, the button will not work.</span></span> <span data-ttu-id="ac927-142">มาลองดูตัวอย่างกัน</span><span class="sxs-lookup"><span data-stu-id="ac927-142">Let's look at an example.</span></span>

<span data-ttu-id="ac927-143">ต่อไปนี้คือปุ่ม การเข้าถึงรายละเอียด ที่จะนำเราไปยังหน้า *รายละเอียดร้านค้า*</span><span class="sxs-lookup"><span data-stu-id="ac927-143">Here is a drillthrough button that will take us to the *Store details* page.</span></span> <span data-ttu-id="ac927-144">การวางเมาส์เหนือปุ่มจะแสดงคำแนะนำเครื่องมือที่ช่วยให้เราทราบว่าเราต้องเลือกทั้งร้านค้าและผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ac927-144">Hovering over the button reveals a tooltip that lets us know that we need to select both a store and a product.</span></span> <span data-ttu-id="ac927-145">จนกว่าเราจะเลือกหนึ่งรายการ ปุ่มก็ยังคงไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="ac927-145">Until we select one of each, the button remains inactive.</span></span>

![สกรีนช็อตของปุ่มการเข้าถึงรายละเอียดพร้อมคำแนะนำเครื่องมือแบบโฮเวอร์](media/end-user-buttons/power-bi-drill-two-selections.png)

<span data-ttu-id="ac927-147">ตอนนี้เราได้เลือกผลิตภัณฑ์หนึ่งรายการ (**Word**) และร้านค้าหนึ่งรายการ (**ลีโอ**) ปุ่มจะเปลี่ยนสีเพื่อแจ้งให้เราทราบว่าขณะนี้มีการใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="ac927-147">Now that we've selected one product (**Word**), and one store (**Leo**), the button changes color to let us know that it is now active.</span></span>

![สกรีนช็อตของปุ่มการเข้าถึงรายละเอียดร้านค้า](media/end-user-buttons/power-bi-select-both.png)

<span data-ttu-id="ac927-149">การเลือกปุ่ม การเข้าถึงรายละเอียด จะนำเราไปยังหน้ารายงาน *Store*</span><span class="sxs-lookup"><span data-stu-id="ac927-149">Selecting the drillthrough button takes us to the *Store* report page.</span></span> <span data-ttu-id="ac927-150">หน้า *ร้านค้า* ถูกกรองสำหรับการเลือก **Word** และ **Leo** ของเรา</span><span class="sxs-lookup"><span data-stu-id="ac927-150">The *Store* page is filtered for our selections of **Word** and **Leo**.</span></span>

![สกรีนช็อตของหน้ารายงานร้านค้า](media/end-user-buttons/power-bi-store.png)

<span data-ttu-id="ac927-152">ปุ่ม การเข้าถึงรายละเอียดข้อมูล ยังสามารถมีเมนูแบบดรอปดาวน์ที่ให้คุณเลือกจุดหมายปลายทางได้</span><span class="sxs-lookup"><span data-stu-id="ac927-152">Drillthrough buttons can also have dropdown menus that offer you a choice of destinations.</span></span> <span data-ttu-id="ac927-153">เมื่อคุณทำการเลือกในหน้ารายงานต้นทางแล้ว ให้เลือกหน้ารายงานปลายทางสำหรับการเข้าถึงรายละเอียดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ac927-153">Once you've made your selections on the source report page, select the destination report page for the drillthrough.</span></span> <span data-ttu-id="ac927-154">ในตัวอย่างด้านล่าง เรากำลังเปลี่ยนการเลือกของเราเป็นการดูรายละเอียดเจาะลึกไปที่หน้ารายงาน *รายละเอียดตลาด*</span><span class="sxs-lookup"><span data-stu-id="ac927-154">In the example below, we're changing our selection to drillthrough to the *Market details* report page.</span></span> 

![ภาพหน้าจอของเมนูแบบดรอปดาวน์ของปุ่มการเข้าถึงรายละเอียดข้อมูลที่มีหลายจุดหมายปลายทาง](media/end-user-buttons/power-bi-destination.png)

## <a name="page-navigation"></a><span data-ttu-id="ac927-156">การนำทางเพจ</span><span class="sxs-lookup"><span data-stu-id="ac927-156">Page navigation</span></span>

<span data-ttu-id="ac927-157">ปุ่มการนำทางของหน้าจะนำคุณไปยังหน้าอื่นในรายงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="ac927-157">Page navigation buttons take you to a different page in the same report.</span></span> <span data-ttu-id="ac927-158">ผู้ออกแบบรายงานมักสร้างปุ่มการนำทางเพื่อเล่าเรื่องราวหรือแนะนำคุณผ่านข้อมูลเชิงลึกของรายงาน</span><span class="sxs-lookup"><span data-stu-id="ac927-158">Report designers often create navigation buttons to tell a story or guide you through the report insights.</span></span> <span data-ttu-id="ac927-159">ในตัวอย่างด้านล่าง ผู้ออกแบบรายงานได้เพิ่มปุ่มบนหน้ารายงานแต่ละหน้าซึ่งจะนำคุณกลับไปที่หน้าแรกซึ่งเป็นหน้าสรุประดับบนสุดในรายงาน</span><span class="sxs-lookup"><span data-stu-id="ac927-159">In the example below, the report designer added a button on each report page that takes you back to the first page, the top-level summary page, in the report.</span></span> <span data-ttu-id="ac927-160">ปุ่มการนำทางของหน้านี้มีประโยชน์เนื่องจากมีหลายหน้าในรายงานนี้</span><span class="sxs-lookup"><span data-stu-id="ac927-160">This page navigation button is helpful because there are many pages in this report.</span></span>

![สกรีนช็อตของปุ่มการนำทางของหน้าที่ชื่อดัชนีชี้วัดของทีม](media/end-user-buttons/power-bi-nav-button.png)


## <a name="qa-buttons"></a><span data-ttu-id="ac927-162">ปุ่ม Q&A</span><span class="sxs-lookup"><span data-stu-id="ac927-162">Q&A buttons</span></span> 
<span data-ttu-id="ac927-163">การเลือกปุ่ม Q&A จะเปิดหน้าต่าง Power BI Q&A Explorer</span><span class="sxs-lookup"><span data-stu-id="ac927-163">Selecting a Q&A button opens the Power BI Q&A Explorer window.</span></span> <span data-ttu-id="ac927-164">หน้าต่าง Q&A ปรากฏที่ด้านบนของหน้ารายงานและสามารถปิดได้โดยเลือก X [เรียนรู้เกี่ยวกับ Q&A](end-user-q-and-a.md)</span><span class="sxs-lookup"><span data-stu-id="ac927-164">The Q&A window displays on top of the report page and can be closed by selecting the X. [Learn about Q&A](end-user-q-and-a.md)</span></span>

![สกรีนช็อตของหน้าต่าง Power BI Q&A Explorer พร้อมข้อความถามคำถามเกี่ยวกับข้อมูลของคุณ](media/end-user-buttons/power-bi-qna.png)

## <a name="web-url"></a><span data-ttu-id="ac927-166">URL ของเว็บ</span><span class="sxs-lookup"><span data-stu-id="ac927-166">Web URL</span></span>
<span data-ttu-id="ac927-167">ปุ่ม URL ของเว็บเปิดหน้าต่างเบราว์เซอร์ใหม่</span><span class="sxs-lookup"><span data-stu-id="ac927-167">Web URL buttons open a new browser window.</span></span> <span data-ttu-id="ac927-168">ผู้ออกแบบรายงานอาจเพิ่มปุ่มประเภทนี้เป็นแหล่งอ้างอิง เพื่อเชื่อมโยงไปยังเว็บไซต์ขององค์กรหรือหน้าความช่วยเหลือหรือแม้กระทั่งเป็นลิงก์ไปยังรายงานหรือแดชบอร์ดอื่น</span><span class="sxs-lookup"><span data-stu-id="ac927-168">Report designers might add this type of button as a reference source, to link to the corporate website or a help page, or even as a link to a different report or dashboard.</span></span> <span data-ttu-id="ac927-169">ในตัวอย่างด้านล่าง ปุ่ม URL ของเว็บช่วยให้คุณดาวน์โหลดไฟล์ต้นฉบับสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="ac927-169">In the example below, the Web URL button let's you download the source file for the report.</span></span> 

<span data-ttu-id="ac927-170">เนื่องจากหน้าจะเปิดขึ้นในหน้าต่างแยกต่าง ให้ปิดหน้าต่างหรือเลือกแท็บ Power BI ของคุณเพื่อกลับไปที่รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="ac927-170">Since the page opens in a separate window, close the window or select your Power BI tab to return to the Power BI report.</span></span>

![ภาพหน้าจอของปุ่มดาวน์โหลด PBIX และหน้าต่างเบราว์เซอร์ใหม่ที่มีลิงก์ดาวน์โหลด](media/end-user-buttons/power-bi-url.png)

## <a name="next-steps"></a><span data-ttu-id="ac927-172">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="ac927-172">Next steps</span></span>
<span data-ttu-id="ac927-173">[บุ๊กมาร์ก](end-user-bookmarks.md)  </span><span class="sxs-lookup"><span data-stu-id="ac927-173">[Bookmarks](end-user-bookmarks.md)  </span></span>  
[<span data-ttu-id="ac927-174">เจาะดูข้อมูลลึกขึ้น เจาะดูรายละเอียดแนวลึก</span><span class="sxs-lookup"><span data-stu-id="ac927-174">Drill up, drill down</span></span>](end-user-drill.md)
