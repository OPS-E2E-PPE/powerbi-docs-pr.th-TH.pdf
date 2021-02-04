---
title: อนุญาตให้ผู้ใช้สามารถตั้งค่าวิชวลส่วนบุคคลในรายงานได้
description: อนุญาตให้ผู้อ่านรายงานสร้างมุมมองรายงานของตนเอง โดยไม่ต้องแก้ไข
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 11/13/2020
LocalizationGroup: Reports
ms.openlocfilehash: 453fdcf91829d0877adf10e48d0a1ac9236340b3
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418037"
---
# <a name="let-users-personalize-visuals-in-a-report"></a><span data-ttu-id="efcfb-103">อนุญาตให้ผู้ใช้สามารถตั้งค่าวิชวลส่วนบุคคลในรายงานได้</span><span class="sxs-lookup"><span data-stu-id="efcfb-103">Let users personalize visuals in a report</span></span>

<span data-ttu-id="efcfb-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-desktop](../includes/yes-desktop.md)] [!INCLUDE [yes-service](../includes/yes-service.md)]</span><span class="sxs-lookup"><span data-stu-id="efcfb-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-desktop](../includes/yes-desktop.md)] [!INCLUDE [yes-service](../includes/yes-service.md)]</span></span>

<span data-ttu-id="efcfb-105">เมื่อคุณแชร์รายงานกับผู้ชมที่หลากหลาย ผู้ใช้บางส่วนของคุณอาจต้องการดูมุมมองวิชวลที่เฉพาะเจาะจงซึ่งแตกต่างกันเล็กน้อย</span><span class="sxs-lookup"><span data-stu-id="efcfb-105">When you share a report with a broad audience, some of your users may want to see slightly different views of particular visuals.</span></span> <span data-ttu-id="efcfb-106">บางทีผู้ใช้อาจต้องการสลับสิ่งที่อยู่บนแกน เปลี่ยนประเภทวิชวลหรือเพิ่มบางอย่างไปยังคำแนะนำเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="efcfb-106">Maybe they'd want to swap what's on the axis, change the visual type, or add something to the tooltip.</span></span> <span data-ttu-id="efcfb-107">เป็นเรื่องยากที่จะสร้างวิชวลซึ่งสามารถตอบสนองความต้องการของทุกคนได้</span><span class="sxs-lookup"><span data-stu-id="efcfb-107">It's hard to make one visual that satisfies everyone's requirements.</span></span> <span data-ttu-id="efcfb-108">ด้วยความสามารถใหม่นี้ คุณสามารถมอบอํานาจให้ผู้ใช้ทางธุรกิจสามารถสํารวจและปรับแต่งภาพได้ในมุมมองการอ่านรายงาน</span><span class="sxs-lookup"><span data-stu-id="efcfb-108">With this new capability, you can empower your business users to explore and personalize visuals, all in report reading view.</span></span> <span data-ttu-id="efcfb-109">พวกเขาสามารถปรับวิชวลตามที่ตนเองต้องการ และบันทึกวิชวลดังกล่าวเป็นบุ๊กมาร์กเพื่อกลับมาใช้งานภายหลังได้</span><span class="sxs-lookup"><span data-stu-id="efcfb-109">They can adjust the visual the way they want, and save it as a bookmark to come back to.</span></span> <span data-ttu-id="efcfb-110">พวกเขาไม่จำเป็นต้องมีสิทธิ์ในการแก้ไขรายงาน หรือกลับไปยังผู้เขียนรายงานเพื่อทำการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="efcfb-110">They don't need to have edit permission for the report, or to go back to the report author for a change.</span></span>

:::image type="content" source="media/power-bi-personalize-visuals/power-bi-personalize-visual.png" alt-text="ตั้งค่าวิชวลส่วนบุคคล":::
 
## <a name="what-report-users-can-change"></a><span data-ttu-id="efcfb-112">รายงานอะไรที่ผู้ใช้สามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="efcfb-112">What report users can change</span></span>

<span data-ttu-id="efcfb-113">คุณลักษณะนี้ช่วยให้ผู้ใช้ทางธุรกิจสามารถรับข้อมูลเชิงลึกเพิ่มเติมผ่านการสำรวจวิชวลแบบเฉพาะกิจบนรายงาน Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="efcfb-113">This feature allows business users to gain further insights through ad-hoc exploration of visuals on a Power BI report.</span></span> <span data-ttu-id="efcfb-114">หากต้องการเรียนรู้วิธีการใช้คุณลักษณะนี้ในฐานะผู้ใช้ ให้ดู [ตั้งค่าวิชวลส่วนบุคคลในรายงานของคุณ](../consumer/end-user-personalize-visuals.md)</span><span class="sxs-lookup"><span data-stu-id="efcfb-114">To learn how to use this feature as a user, see [Personalize visuals in your reports](../consumer/end-user-personalize-visuals.md).</span></span> <span data-ttu-id="efcfb-115">คุณลักษณะนี้เหมาะสำหรับผู้เขียนรายงานที่ต้องการเปิดใช้งานสถานการณ์การสำรวจพื้นฐานของตัวอ่านรายงานของตน</span><span class="sxs-lookup"><span data-stu-id="efcfb-115">The feature is ideal for report creators who want enable basic exploration scenarios for their report readers.</span></span> <span data-ttu-id="efcfb-116">ต่อไปนี้คือการปรับเปลี่ยนตัวอ่านรายงานที่สามารถทำได้:</span><span class="sxs-lookup"><span data-stu-id="efcfb-116">Here are modifications that report readers can make:</span></span>

- <span data-ttu-id="efcfb-117">การเปลี่ยนชนิดของการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="efcfb-117">Change the visualization type</span></span>
- <span data-ttu-id="efcfb-118">สลับหน่วยวัดหรือมิติ</span><span class="sxs-lookup"><span data-stu-id="efcfb-118">Swap out a measure or dimension</span></span>
- <span data-ttu-id="efcfb-119">เพิ่มหรือลบคำอธิบายแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="efcfb-119">Add or remove a legend</span></span>
- <span data-ttu-id="efcfb-120">เปรียบเทียบหน่วยวัดสองหน่วยขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="efcfb-120">Compare two or more measures</span></span>
- <span data-ttu-id="efcfb-121">เปลี่ยนการรวมและอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="efcfb-121">Change aggregations, etc.</span></span>

<span data-ttu-id="efcfb-122">ไม่เฉพาะคุณลักษณะนี้เท่านั้นที่อนุญาตให้ใช้งานสำหรับความสามารถในการสำรวจใหม่</span><span class="sxs-lookup"><span data-stu-id="efcfb-122">Not only does this feature allow for new exploration capabilities.</span></span> <span data-ttu-id="efcfb-123">แต่ยังมีวิธีการสำหรับผู้ใช้ในการบันทึกและแชร์การเปลี่ยนแปลงของตนเอง:</span><span class="sxs-lookup"><span data-stu-id="efcfb-123">It also includes ways for users to capture and share their changes:</span></span>

- <span data-ttu-id="efcfb-124">บันทึกการเปลี่ยนแปลงของตนเอง</span><span class="sxs-lookup"><span data-stu-id="efcfb-124">Capture their changes</span></span>
- <span data-ttu-id="efcfb-125">แชร์การเปลี่ยนแปลงของตนเอง</span><span class="sxs-lookup"><span data-stu-id="efcfb-125">Share their changes</span></span>
- <span data-ttu-id="efcfb-126">รีเซ็ตการเปลี่ยนแปลงทั้งหมดของตนเองสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="efcfb-126">Reset all their changes for a report</span></span>
- <span data-ttu-id="efcfb-127">รีเซ็ตการเปลี่ยนแปลงทั้งหมดของตนเองสำหรับวิชวล</span><span class="sxs-lookup"><span data-stu-id="efcfb-127">Reset all their changes for a visual</span></span>
- <span data-ttu-id="efcfb-128">ล้างการเปลี่ยนแปลงล่าสุดของตนเอง</span><span class="sxs-lookup"><span data-stu-id="efcfb-128">Clear out their recent changes</span></span>

## <a name="use-perspectives-for-a-more-focused-view"></a><span data-ttu-id="efcfb-129">ใช้มุมมองต่าง ๆ เพื่อให้ได้ภาพที่โฟกัสมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="efcfb-129">Use Perspectives for a more focused view</span></span>

<span data-ttu-id="efcfb-130">เพื่อการปรับแต่งภาพ คุณสามารถใช้ **มุมมอง** เพื่อเลือกชุดย่อยของโมเดลที่ให้มุมมองที่โฟกัสมากขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="efcfb-130">For Personalize visuals, you can use **Perspectives** to choose a subset of a model that provides a more focused view.</span></span> <span data-ttu-id="efcfb-131">การเลือกชุดย่อยจะเป็นประโยชน์เมื่อทำงานกับโมเดลข้อมูลขนาดใหญ่ และช่วยให้คุณสามารถมุ่งเน้นไปที่ชุดย่อยของเขตข้อมูลซึ่งสามารถบริหารจัดการได้และไม่มีการครอบงำผู้อ่านรายงานด้วยเขตข้อมูลเต็มรูปแบบเหมือนในโมเดลขนาดใหญ่</span><span class="sxs-lookup"><span data-stu-id="efcfb-131">Choosing a subset can be helpful when working with a large data model, allowing you to focus on a manageable subset of fields, and not overwhelm report readers with the full collection of fields in that large model.</span></span> 

![ปรับแต่งการแสดงผลด้วยภาพ](media/power-bi-personalize-visuals/power-bi-personalize-perspective-01.png)

<span data-ttu-id="efcfb-133">โปรดพิจารณาถึงสิ่งต่าง ๆ เหล่านี้เมื่อทำงานกับมุมมอง</span><span class="sxs-lookup"><span data-stu-id="efcfb-133">Keep the following considerations in mind when working with perspectives:</span></span>

* <span data-ttu-id="efcfb-134">มุมมองไม่ได้มีจุดประสงค์เพื่อใช้เป็นเครื่องมือในการรักษาความปลอดภ้ัย แต่เป็นเครื่องมือที่ช่วยมอบประสบการณ์ผู้ใช้ที่ดียิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="efcfb-134">Perspectives are not meant to be used as a security mechanism, they are a tool for providing a better end-user experience.</span></span> <span data-ttu-id="efcfb-135">การรักษาความปลอดภัยสำหรับมุมมองทั้งหมดนั้นได้มาจากโมเดลที่เป็นรากฐาน</span><span class="sxs-lookup"><span data-stu-id="efcfb-135">All security for a perspective is inherited from the underlying model.</span></span>

* <span data-ttu-id="efcfb-136">ระบบนี้สนับสนุนมุมมองทั้งแบบตารางและแบบหลายมิติ</span><span class="sxs-lookup"><span data-stu-id="efcfb-136">Perspectives in both tabular and multi-dimensional models are supported.</span></span> <span data-ttu-id="efcfb-137">อย่างไรก็ตาม สำหรับมุมมองในโมเดลแบบหลายมิติ คุณจะสามารถตั้งค่ามุมมองให้เหมือนกับรายงานพื้นฐานได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="efcfb-137">However, for perspectives in multi-dimensional models, you can only set the perspective to be the same as the base cube for the report.</span></span>

* <span data-ttu-id="efcfb-138">ก่อนที่จะลบมุมมองออกจากโมเดล โปรดตรวจสอบให้แน่ใจว่าไม่ใช้ใช้มุมมองดังกล่าวในการแสดงภาพแบบปรับแต่งเอง</span><span class="sxs-lookup"><span data-stu-id="efcfb-138">Before deleting a perspective from a model, be sure to check that the perspective is not being used in the Personalize visuals experience.</span></span> 

<span data-ttu-id="efcfb-139">หากต้องการใช้มุมมอง คุณต้องเปิดใช้งานมุมมองแบบปรับแต่งเองสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="efcfb-139">To use Perspectives, you must enable Personalize visuals for the report.</span></span> <span data-ttu-id="efcfb-140">คุณจำเป็นต้องสร้างมุมมองอย่างน้อยหนึ่งรายการที่มีมิติและหน่วยวัดที่คุณต้องการให้ผู้ใช้ได้ใช้สำหรับประสบการณ์การแสดงภาพแบบปรับแต่งเอง</span><span class="sxs-lookup"><span data-stu-id="efcfb-140">You also must create at least one Perspective that includes the dimensions and measures you want end-users to interact with for the Personalize visuals experience.</span></span>

<span data-ttu-id="efcfb-141">เพื่อสร้างมุมมอง ให้ใช้[ตัวแก้ไขตาราง](https://tabulareditor.com/)ซึ่งคุณสามารถดาวน์โหลดได้จากตำแหน่งต่อไปนี้: ดาวน์โหลดตัวแก้ไขตาราง</span><span class="sxs-lookup"><span data-stu-id="efcfb-141">To create the perspective use [Tabular Editor](https://tabulareditor.com/), which you can download from the following location: Tabular Editor download</span></span>

<span data-ttu-id="efcfb-142">เมื่อคุณติดตั้ง **ตัวแก้ไขตาราง** แล้ว ให้เปิดรายงานของคุณใน **Power BI Desktop** แล้วเปิดใช้ **ตัวแก้ไขตาราง** จากแท็บ **เครื่องมือภายนอก** ของริบบอน ตามที่แสดงในภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="efcfb-142">Once you install **Tabular Editor**, open your report in **Power BI Desktop** and launch **Tabular Editor** from the **External Tools** tab of the ribbon, as shown in the following image.</span></span>

![ตัวแก้ไขตารางในริบบอนเครื่องมือภายนอก](media/power-bi-personalize-visuals/power-bi-personalize-perspective-02.png)

<span data-ttu-id="efcfb-144">ในตัวแก้ไขตาราง ให้คลิกขวาที่โฟลเดอร์ **มุมมอง** เพื่อสร้างมุมมองใหม่</span><span class="sxs-lookup"><span data-stu-id="efcfb-144">In Tabular Editor, right-click on the **Perspectives** folder to create a new perspective.</span></span>

![สร้างโฟลเดอร์มุมมองใหม่ในตัวแก้ไขตาราง](media/power-bi-personalize-visuals/power-bi-personalize-perspective-03.png)

<span data-ttu-id="efcfb-146">คุณสามารถดับเบิลคลิกที่ข้อความเพื่อเปลี่ยนชื่อมุมมองได้</span><span class="sxs-lookup"><span data-stu-id="efcfb-146">You can double-click the text to rename the perspective.</span></span>

![เปลี่ยนชื่อมุมมอง](media/power-bi-personalize-visuals/power-bi-personalize-perspective-04.png)

<span data-ttu-id="efcfb-148">ต่อมา ให้เพิ่มเขตข้อมูลเข้าสู่มุมมองโดยการเปิดโฟลเดอร์ **ตาราง** ในตัวแก้ไขตาราง คลิกขวาที่เขตข้อมูลที่คุณต้องการเพื่อแสดงในมุมมอง</span><span class="sxs-lookup"><span data-stu-id="efcfb-148">Next, add fields to the perspective by opening the **Tables** folder in Tabular Editor, the right-click on the fields you want to show in the perspective.</span></span>

![เพิ่มเขตข้อมูลในมุมมอง](media/power-bi-personalize-visuals/power-bi-personalize-perspective-05.png)

<span data-ttu-id="efcfb-150">ทำซ้ำกระบวนการดังกล่าวสำหรับแต่ละเขตข้อมูลที่คุณต้องการเพิ่มในมุมมอง</span><span class="sxs-lookup"><span data-stu-id="efcfb-150">Repeat that process for each field you want to add to the perspective.</span></span> <span data-ttu-id="efcfb-151">คุณไม่สามารถเพิ่มเขตข้อมูลซ้ำไว้ในมุมมองเดียวได้ ดังนั้นระบบจะปิดการใช้งานตัวเลือกในการเพิ่มเขตข้อมูลที่คุณเคยเพิ่มไปยังมุมมองแล้ว</span><span class="sxs-lookup"><span data-stu-id="efcfb-151">You can’t add duplicate fields in a perspective, so any fields you already added to a perspective will have the option to add it disabled.</span></span>

<span data-ttu-id="efcfb-152">หลังจากที่คุณได้เพิ่มเขตข้อมูลทั้งหมดที่คุณต้องการแล้ว ให้ตรวจสอบให้แน่ใจว่าได้บันทึกการตั้งค่าของคุณทั้งในตัวแก้ไขตารางและใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="efcfb-152">After you added all the fields you want, be sure to save your settings, both in Tabular Editor and then also in Power BI Desktop.</span></span>

![บันทึกการตั้งค่ามุมมองในตัวแก้ไขตารางและ Power BI Desktop](media/power-bi-personalize-visuals/power-bi-personalize-perspective-06.png)

<span data-ttu-id="efcfb-154">เมื่อคุณได้บันทึกมุมมองใหม่ไว้ในโมเดล และบันทึกใน Power BI Desktop แล้ว ให้ไปที่บานหน้าต่าง **รูปแบบ** ของหน้าซึ่งคุณจะเห็นส่วนใหม่สำหรับ **การกำหนดการแสดงผลด้วยภาพ**</span><span class="sxs-lookup"><span data-stu-id="efcfb-154">Once you save the new perspective to the model, and save the Power BI Desktop report, navigate to the **Format** pane for the page, where you see a new section for **Personalize visual**.</span></span>

![ส่วนการกำหนดการแสดงผลด้วยภาพในบานหน้าต่างรูปแบบ](media/power-bi-personalize-visuals/power-bi-personalize-perspective-07.png)

<span data-ttu-id="efcfb-156">ในเบื้องต้น ระบบจะตั้งค่าตัวเลือกสำหรับ *มุมมองรายงาน-ผู้อ่าน* เป็น *เขตข้อมูลตามค่าเริ่มต้น*</span><span class="sxs-lookup"><span data-stu-id="efcfb-156">The selection for *Report-reader perspective* is set to *Default fields* initially.</span></span> <span data-ttu-id="efcfb-157">เมื่อคุณเลือกลูกศรดรอปดาวน์ คุณจะเห็นมุมมองอื่น ๆ ที่คุณได้สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="efcfb-157">Once you select the drop down arrow, you see the other Perspectives you’ve created.</span></span>

![เลือกลูกศรดรอปดาวน์เพื่อดูมุมมองอื่น ๆ ของคุณ](media/power-bi-personalize-visuals/power-bi-personalize-perspective-08.png)

<span data-ttu-id="efcfb-159">เมื่อคุณตั้งค่ามุมมองสำหรับหน้ารายงาน ระบบจะกรองประสบการณ์กำหนดการแสดงผลด้วยภาพสำหรับหน้าดังกล่าวไปยังมุมมองที่เลือก</span><span class="sxs-lookup"><span data-stu-id="efcfb-159">Once you set the Perspective for the report page, the Personalize visuals experience for that page is filtered to the selected Perspective.</span></span> <span data-ttu-id="efcfb-160">การเลือก **นำไปใช้กับทุกหน้า** จะช่วยให้คุณสามารถใช้การตั้งค่ามุมมองของคุณกับหน้าที่มีอยู่ทั้งหมดในรายงานของคุณได้</span><span class="sxs-lookup"><span data-stu-id="efcfb-160">Selecting **Apply to all pages** lets you apply your Perspective setting to all existing pages in your report.</span></span>

![เลือกนำไปใช้กับทุกหน้าสำหรับมุมมองที่คุณต้องการนำไปใช้กับทุกส่วนของรายงาน](media/power-bi-personalize-visuals/power-bi-personalize-perspective-09.png)

## <a name="enable-personalization-in-a-report"></a><span data-ttu-id="efcfb-162">เปิดใช้งานการตั้งค่าส่วนบุคคลในรายงาน</span><span class="sxs-lookup"><span data-stu-id="efcfb-162">Enable personalization in a report</span></span>

<span data-ttu-id="efcfb-163">คุณสามารถเปิดใช้งานคุณลักษณะใน Power BI Desktop หรือบริการของ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="efcfb-163">You can enable the feature either in Power BI Desktop or the Power BI service.</span></span> <span data-ttu-id="efcfb-164">คุณยังสามารถเปิดใช้งานในรายงานแบบฝังได้</span><span class="sxs-lookup"><span data-stu-id="efcfb-164">You can also enable it in embedded reports.</span></span>

### <a name="in-power-bi-desktop"></a><span data-ttu-id="efcfb-165">ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="efcfb-165">In Power BI Desktop</span></span>

<span data-ttu-id="efcfb-166">หากต้องการเปิดใช้งานคุณลักษณะใน Power BI Desktop ให้ไปที่ **ไฟล์** > **ตัวเลือกและการตั้งค่า** > **ตัวเลือก** > **ไฟล์ปัจจุบัน** > **การตั้งค่ารายงาน**</span><span class="sxs-lookup"><span data-stu-id="efcfb-166">To enable the feature in Power BI Desktop, go to **File** > **Options and Settings** > **Options** > **Current file** > **Report settings**.</span></span> <span data-ttu-id="efcfb-167">ตรวจสอบให้แน่ใจว่า **ตั้งค่าวิชวลส่วนบุคคล** เปิดใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="efcfb-167">Make sure **Personalize visuals** is turned on.</span></span>

:::image type="content" source="media/power-bi-personalize-visuals/personalize-report-setting-desktop.png" alt-text="เปิดใช้งานการตั้งค่าส่วนบุคคลในรายงาน":::

### <a name="in-the-power-bi-service"></a><span data-ttu-id="efcfb-169">ในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="efcfb-169">In the Power BI service</span></span>

<span data-ttu-id="efcfb-170">หากต้องการเปิดใช้งานคุณลักษณะในบริการของ Power BI แทน ให้ไปที่ **การตั้งค่า** สำหรับรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="efcfb-170">To enable the feature in the Power BI service instead, go to **Settings** for your report.</span></span>

:::image type="content" source="media/power-bi-personalize-visuals/power-bi-report-service-settings-personalize-visual.png" alt-text="การตั้งค่ารายงานในบริการของ Power BI":::

<span data-ttu-id="efcfb-172">เปิด **การตั้งค่าวิชวลส่วนบุคคล** > **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="efcfb-172">Turn on **Personalize visuals** > **Save**.</span></span>

:::image type="content" source="media/power-bi-personalize-visuals/personalize-report-setting-service.png" alt-text="เปิด ตั้งค่าวิชวลส่วนบุคคลในรายงาน":::

## <a name="turn-the-feature-on-or-off-at-a-page-or-visual-level"></a><span data-ttu-id="efcfb-174">เปิดหรือปิดคุณสมบัติที่หน้าหรือระดับสายตา</span><span class="sxs-lookup"><span data-stu-id="efcfb-174">Turn the feature on or off at a page or visual level</span></span>

<span data-ttu-id="efcfb-175">เมื่อคุณเปิดใช้งานปรับแต่งภาพสําหรับรายงานที่กําหนดโดยค่าเริ่มต้นภาพทั้งหมดในรายงานนั้นสามารถเป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="efcfb-175">When you enable Personalize visuals for a given report, by default all visuals in that report can be personalized.</span></span> <span data-ttu-id="efcfb-176">ถ้าคุณไม่ต้องการให้ภาพทั้งหมดเป็นแบบส่วนบุคคล คุณสามารถเปิดหรือปิดการตั้งค่าต่อหน้าหรือต่อภาพ</span><span class="sxs-lookup"><span data-stu-id="efcfb-176">If you don't want all the visuals to be personalized, you can turn the setting on or off per page or per visual.</span></span>

### <a name="per-page"></a><span data-ttu-id="efcfb-177">แต่ละหน้า</span><span class="sxs-lookup"><span data-stu-id="efcfb-177">Per page</span></span>

<span data-ttu-id="efcfb-178">เลือกแท็บหน้า > เลือก **รูปแบบ** ในบานหน้าต่าง **การแสดงภาพ**</span><span class="sxs-lookup"><span data-stu-id="efcfb-178">Select the page tab > select **Format** in the **Visualizations** pane.</span></span>

:::image type="content" source="media/power-bi-personalize-visuals/personalize-page-level-setting.png" alt-text="เลือกการตั้งค่าวิชวลส่วนบุคคลสำหรับแต่ละหน้า":::
 
<span data-ttu-id="efcfb-180">เลื่อนแถบ **ตั้งค่าวิชวลส่วนบุคคล** >  **เพื่อเปิด** หรือ **ปิด**</span><span class="sxs-lookup"><span data-stu-id="efcfb-180">Slide **Personalize visual** >  **On** or **Off**.</span></span>

### <a name="per-visual"></a><span data-ttu-id="efcfb-181">แต่ละวิชวล</span><span class="sxs-lookup"><span data-stu-id="efcfb-181">Per visual</span></span>

<span data-ttu-id="efcfb-182">เลือกวิชวล > เลือก **รูปแบบ** ในบานหน้าต่าง **การแสดงภาพ** > ขยาย **ส่วนหัวของวิชวล**</span><span class="sxs-lookup"><span data-stu-id="efcfb-182">Select the visual > select **Format** in the **Visualizations** pane > expand **Visual header**.</span></span>

:::image type="content" source="media/power-bi-personalize-visuals/power-bi-format-visual-header-personalize.png" alt-text="เลือกส่วนหัวของวิชวล":::
 
<span data-ttu-id="efcfb-184">เลื่อนแถบ **ตั้งค่าวิชวลส่วนบุคคล** >  **เพื่อเปิด** หรือ **ปิด**</span><span class="sxs-lookup"><span data-stu-id="efcfb-184">Slide **Personalize visual** >  **On** or **Off**.</span></span>

:::image type="content" source="media/power-bi-personalize-visuals/power-bi-format-visual-personalize-on-off.png" alt-text="แถบเลื่อนสำหรับการเปิดหรือปิดการตั้งค่าวิชวลส่วนบุคคล":::


## <a name="limitations"></a><span data-ttu-id="efcfb-186">ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="efcfb-186">Limitations</span></span>

<span data-ttu-id="efcfb-187">คุณลักษณะมีข้อจำกัดบางอย่างที่ต้องระวังในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="efcfb-187">Currently the feature has a few limitations to be aware of.</span></span>

- <span data-ttu-id="efcfb-188">คุณลักษณะนี้ไม่รองรับการเผยแพร่ไปยังเว็บ</span><span class="sxs-lookup"><span data-stu-id="efcfb-188">This feature isn't supported for publish to web.</span></span>
- <span data-ttu-id="efcfb-189">การสำรวจของผู้ใช้ไม่ดำเนินการต่อโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="efcfb-189">User explorations don't automatically persist.</span></span> <span data-ttu-id="efcfb-190">คุณต้องบันทึกมุมมองของคุณเป็นบุ๊กมาร์กส่วนบุคคล เพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="efcfb-190">You need to save your view as a personal bookmark to capture your changes.</span></span>
- <span data-ttu-id="efcfb-191">คุณลักษณะนี้ได้รับการรองรับในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่สำหรับแท็บเล็ต iOS และ Android และในแอป Power BI Windows แต่ไม่ได้รับการรองรับในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่สำหรับโทรศัพท์</span><span class="sxs-lookup"><span data-stu-id="efcfb-191">This feature is supported in the Power BI mobile apps for iOS and Android tablets and in the Power BI Windows app; it is not supported in the Power BI mobile apps for phones.</span></span> <span data-ttu-id="efcfb-192">อย่างไรก็ตาม การเปลี่ยนแปลงใด ๆ ที่ทำกับวิชวล ซึ่งคุณได้บันทึกในบุ๊กมาร์กส่วนบุคคลขณะที่ใช้บริการของ Power BI นั้นจะสามารถดำเนินการในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่ทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="efcfb-192">However, any change to a visual you save in a personal bookmark while in the Power BI service is respected in all the Power BI mobile apps.</span></span>

## <a name="next-steps"></a><span data-ttu-id="efcfb-193">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="efcfb-193">Next steps</span></span>

<span data-ttu-id="efcfb-194">[ตั้งค่าวิชวลส่วนบุคคลในรายงานของคุณ](../consumer/end-user-personalize-visuals.md)</span><span class="sxs-lookup"><span data-stu-id="efcfb-194">[Personalize visuals in your reports](../consumer/end-user-personalize-visuals.md).</span></span>     

<span data-ttu-id="efcfb-195">ลองสัมผัสประสบการณ์การใช้งานการตั้งค่าวิชวลส่วนบุคคลใหม่</span><span class="sxs-lookup"><span data-stu-id="efcfb-195">Give the new visual personalization experience a try.</span></span> <span data-ttu-id="efcfb-196">ส่งคำติชมของคุณของคุณเกี่ยวกับคุณสมบัตินี้ และสิ่งที่เราสามารถปรับปรุงได้ ใน [ไซต์ Power BI Ideas](https://ideas.powerbi.com/forums/265200-power-bi)</span><span class="sxs-lookup"><span data-stu-id="efcfb-196">Give us your feedback for this feature, and how we can continue to improve it, on the [Power BI Ideas site](https://ideas.powerbi.com/forums/265200-power-bi).</span></span> 

<span data-ttu-id="efcfb-197">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="efcfb-197">More questions?</span></span> [<span data-ttu-id="efcfb-198">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="efcfb-198">Try the Power BI Community</span></span>](https://community.powerbi.com/)
