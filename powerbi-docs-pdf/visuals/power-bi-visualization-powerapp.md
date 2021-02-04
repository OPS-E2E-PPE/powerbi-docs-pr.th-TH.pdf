---
title: ฝัง Power App ใหม่ในรายงาน Power BI
description: ฝังแอปที่ใช้แหล่งข้อมูลเดียวกันและสามารถกรองได้เหมือนกับรายการรายงานอื่นๆ
author: mihart
ms.author: mihart
manager: kvivek
ms.reviewer: tapan maniar
ms.service: powerbi
ms.subservice: pbi-visuals
ms.topic: how-to
ms.date: 06/01/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 1c4086d6ab71bd96ba7ac6c6985161d28a4dcb8b
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418888"
---
# <a name="tutorial-embed-a-power-apps-visual-in-a-power-bi-report"></a><span data-ttu-id="d74e8-103">บทช่วยสอน: ฝังวิชวล Power App ในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="d74e8-103">Tutorial: Embed a Power Apps visual in a Power BI report</span></span>

<span data-ttu-id="d74e8-104">ในการแนะนำวิธีการใช้นี้ คุณใช้วิชวล Power Apps สร้างแอปใหม่ที่ถูกฝังในตัวอย่างรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="d74e8-104">In this tutorial, you use the Power Apps visual to create a new app that is embedded in a sample Power BI report.</span></span> <span data-ttu-id="d74e8-105">แอปนี้โต้ตอบกับวิชวลอื่นในรายงานดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="d74e8-105">This app interacts with other visuals in that report.</span></span>

<span data-ttu-id="d74e8-106">หากคุณไม่มีการสมัครสมาชิก Power Apps [สร้างบัญชีฟรี](https://make.powerapps.com/signup?redirect=marketing&email=) ก่อนที่คุณจะเริ่มใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d74e8-106">If you don't have a Power Apps subscription, [create a free account](https://make.powerapps.com/signup?redirect=marketing&email=) before you begin.</span></span>

<span data-ttu-id="d74e8-107">ในบทช่วยสอนนี้ คุณจะเรียนรู้วิธีการ:</span><span class="sxs-lookup"><span data-stu-id="d74e8-107">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="d74e8-108">เพิ่มวิชวล Power Apps ไปยังรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="d74e8-108">Add a Power Apps visual to a Power BI report</span></span>
> * <span data-ttu-id="d74e8-109">ทำงานใน Power Apps เพื่อสร้างแอปใหม่ที่ใช้ข้อมูลจากรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="d74e8-109">Work in Power Apps to create a new app that uses data from the Power BI report</span></span>
> * <span data-ttu-id="d74e8-110">ดูและโต้ตอบกับวิชวล Power Apps ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="d74e8-110">View and interact with the Power Apps visual in the report</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d74e8-111">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="d74e8-111">Prerequisites</span></span>

* <span data-ttu-id="d74e8-112">เบราว์เซอร์ [Google Chrome](https://www.google.com/chrome/browser/) หรือ [Microsoft Edge](https://www.microsoft.com/windows/microsoft-edge)</span><span class="sxs-lookup"><span data-stu-id="d74e8-112">[Google Chrome](https://www.google.com/chrome/browser/) or [Microsoft Edge](https://www.microsoft.com/windows/microsoft-edge) browser</span></span>
* <span data-ttu-id="d74e8-113">[การสมัครใช้งาน Power BI](../fundamentals/service-self-service-signup-for-power-bi.md) ที่ติดตั้ง [ตัวอย่างการวิเคราะห์โอกาสทางการขาย](../create-reports/sample-opportunity-analysis.md#get-the-content-pack-for-this-sample)</span><span class="sxs-lookup"><span data-stu-id="d74e8-113">A [Power BI subscription](../fundamentals/service-self-service-signup-for-power-bi.md), with the [Opportunity Analysis Sample](../create-reports/sample-opportunity-analysis.md#get-the-content-pack-for-this-sample) installed</span></span>
* <span data-ttu-id="d74e8-114">การเข้าใจวิธีการ [สร้างแอปใน Power Apps](/powerapps/maker/canvas-apps/data-platform-create-app-scratch) และวิธีการ [แก้ไขรายงาน Power BI](../create-reports/service-the-report-editor-take-a-tour.md)</span><span class="sxs-lookup"><span data-stu-id="d74e8-114">An understanding of how to [create apps in Power Apps](/powerapps/maker/canvas-apps/data-platform-create-app-scratch) and how to [edit Power BI reports](../create-reports/service-the-report-editor-take-a-tour.md)</span></span>



## <a name="create-a-new-app"></a><span data-ttu-id="d74e8-115">สร้างแอปใหม่</span><span class="sxs-lookup"><span data-stu-id="d74e8-115">Create a new app</span></span>
<span data-ttu-id="d74e8-116">เมื่อคุณเพิ่มวิชวล Power Apps ไปยังรายงานของคุณ ระบบจะเปิดใช้งาน Power Apps Studio ด้วยการเชื่อมต่อข้อมูลสดระหว่าง Power Apps และ Power BI</span><span class="sxs-lookup"><span data-stu-id="d74e8-116">When you add the Power Apps visual to your report, it launches Power Apps Studio with a live data connection between Power Apps and Power BI.</span></span>

1. <span data-ttu-id="d74e8-117">เปิดตัวอย่างรายงานตัวอย่างการวิเคราะห์โอกาสทางการขายและเลือกหน้า *โอกาสที่จะเข้ามาถึง*</span><span class="sxs-lookup"><span data-stu-id="d74e8-117">Open the Opportunity Analysis sample report and select the *Upcoming Opportunities* page.</span></span> 


2. <span data-ttu-id="d74e8-118">เคลื่อนย้ายและปรับขนาดบางไทล์รายงานเพื่อสร้างช่องว่างสำหรับวิชวลใหม่</span><span class="sxs-lookup"><span data-stu-id="d74e8-118">Move and resize some of the report tiles to make space for the new visual.</span></span>

    ![ย้ายและปรับขนาดไทล์รายงาน](media/power-bi-visualization-powerapp/power-bi-report-page.jpg)

2. <span data-ttu-id="d74e8-120">จากแผงการแสดงผลด้วยภาพ เลือกไอคอน Power Apps แล้วรปับขนาดวิชวลให้พอดีกับช่องว่างที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="d74e8-120">From the Visualizations pane, select the Power Apps icon, then resize the visual to fit the space you made.</span></span>

    ![บานหน้าต่างการแสดงผลด้วยภาพพร้อมกับไอคอน Power Apps ที่เลือก](media/power-bi-visualization-powerapp/power-bi-powerapps-icon.jpg)

3. <span data-ttu-id="d74e8-122">ในบานหน้าต่าง **เขตข้อมูล** ให้เลือก **ชื่อ** **รหัสผลิตภัณฑ์** และ **ขั้นตอนการขาย**</span><span class="sxs-lookup"><span data-stu-id="d74e8-122">In the **Fields** pane, select **Name**, **Product Code**, and **Sales Stage**.</span></span> 

    ![เลือกเขตข้อมูล](media/power-bi-visualization-powerapp/power-bi-fields.png)

4. <span data-ttu-id="d74e8-124">ในวิชวล Power Apps เลือกสภาพแวดล้อม Power Apps ที่คุณต้องการสร้างแอป จากนั้นเลือก **สร้างขึ้นใหม่**.</span><span class="sxs-lookup"><span data-stu-id="d74e8-124">On the Power Apps visual, select the Power Apps environment where you want to create the app, then select **Create new**.</span></span>

    ![สร้างแอปใหม่](media/power-bi-visualization-powerapp/power-bi-create-new-powerapp.png)

    <span data-ttu-id="d74e8-126">ใน Power Apps Studio  คุณจะพบแอปเบื้องต้นที่สร้างไว้แล้ว ที่ *แกลเลอรี* ที่จะแสดงหนึ่งในเขตข้อมูลที่คุณเลือกใน Power BI.</span><span class="sxs-lookup"><span data-stu-id="d74e8-126">In Power Apps Studio, you see that a basic app is created, with a *gallery* that shows one of the fields you selected in Power BI.</span></span>

    ![การเปิด Power Apps](media/power-bi-visualization-powerapp/power-bi-power-app.png)

5.  <span data-ttu-id="d74e8-128">ปรับขนาดแกลเลอรีเพื่อให้ใช้พื้นที่เพียงครึ่งหนึ่งของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="d74e8-128">Resize the gallery so it takes up only half of the screen.</span></span> 

6. <span data-ttu-id="d74e8-129">ในแผงด้านซ้าย เลือก **หน้าจอ1** จากนั้นตั้งค่าคุณสมบัติ **การเพิ่ม** ของหน้าจอเป็น "แสงสีฟ้า" (ดังที่แสดงขึ้นในรายงาน)</span><span class="sxs-lookup"><span data-stu-id="d74e8-129">In the left pane, select **Screen1**, then set the screen's **Fill** property to "LightBlue" (so it shows up better in the report).</span></span>

    ![จานสี](media/power-bi-visualization-powerapp/power-bi-powerapps-fill.png)

6. <span data-ttu-id="d74e8-131">สร้างบางพื้นที่ว่างสำหรับการควบคุมป้าย</span><span class="sxs-lookup"><span data-stu-id="d74e8-131">Make some room for a label control.</span></span> 

    ![เปลี่ยนขนาดแกลเลอรี](media/power-bi-visualization-powerapp/power-bi-powerapps-gallery.png)


8. <span data-ttu-id="d74e8-133">ใต้ **แกลเลอรี** ให้แทรกการควบคุมป้ายข้อความ</span><span class="sxs-lookup"><span data-stu-id="d74e8-133">Under **gallery**, insert a text label control.</span></span>

   ![การควบคุมป้าย](media/power-bi-visualization-powerapp/power-bi-label.png)

7. <span data-ttu-id="d74e8-135">ลากป้ายไปยังด้านล่างของวิชวลของคุณ</span><span class="sxs-lookup"><span data-stu-id="d74e8-135">Drag the label to the bottom of your visual.</span></span> <span data-ttu-id="d74e8-136">Set the **Text** property to `"Opportunity Count: " & CountRows(Gallery1.AllItems)`.</span><span class="sxs-lookup"><span data-stu-id="d74e8-136">Set the **Text** property to `"Opportunity Count: " & CountRows(Gallery1.AllItems)`.</span></span> <span data-ttu-id="d74e8-137">ในตอนนี้ จะแสดงจำนวนโอกาสทั้งหมดในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d74e8-137">It now shows the total number of opportunities in the data set.</span></span>

    ![แอปที่มีแกลเลอรีที่ปรับขนาดแล้ว](media/power-bi-visualization-powerapp/power-bi-power-app-label.png)

    ![แอปกับป้ายที่อัปเดตแล้ว](media/power-bi-visualization-powerapp/power-bi-label-live.png)

7. <span data-ttu-id="d74e8-140">บันทึกแอปด้วยชื่อของ "แอปโอกาสทางการขาย"</span><span class="sxs-lookup"><span data-stu-id="d74e8-140">Save the app with the name "Opportunities app".</span></span> 

    ![บันทึกแอป](media/power-bi-visualization-powerapp/power-bi-save-powerapp.png)


## <a name="view-the-app-in-the-report"></a><span data-ttu-id="d74e8-142">ดูแอปในรายงาน</span><span class="sxs-lookup"><span data-stu-id="d74e8-142">View the app in the report</span></span>
<span data-ttu-id="d74e8-143">แอปสามารถใช้งานได้แล้วในรายงาน Power BI และสามารถโต้ตอบกับวิชวลอื่นๆ เพราะว่าสามารถแชร์แหล่งข้อมูลเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="d74e8-143">The app is now available in the Power BI report, and it interacts with other visuals because it shares the same data source.</span></span>

![แอปในรายงาน Power BI](media/power-bi-visualization-powerapp/power-bi-powerapps-visual.png)

<span data-ttu-id="d74e8-145">ในรายงาน Power BI ให้เลือก **ม.ค.** ในตัวแบ่งส่วนข้อมูล ซึ่งจะกรองทั้งหมด รวมถึงข้อมูลในแอป</span><span class="sxs-lookup"><span data-stu-id="d74e8-145">In the Power BI report, select **Jan** in the slicer, which filters the whole report, including the data in the app.</span></span>

![รายงานที่ถูกกรอง](media/power-bi-visualization-powerapp/power-bi-last.png)

<span data-ttu-id="d74e8-147">โปรดสังเกตว่าจำนวนโอกาสในแอปจะตรงกับจำนวนที่มุมซ้ายบนของรายงาน</span><span class="sxs-lookup"><span data-stu-id="d74e8-147">Notice that the opportunity count in the app matches the count in the upper left of the report.</span></span> <span data-ttu-id="d74e8-148">คุณสามารถเลือกรายการอื่นๆ ในรายงาน และข้อมูลในแอปจะอัปเดต</span><span class="sxs-lookup"><span data-stu-id="d74e8-148">You can select other items in the report, and the data in the app updates.</span></span>


## <a name="clean-up-resources"></a><span data-ttu-id="d74e8-149">ล้างแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d74e8-149">Clean up resources</span></span>
<span data-ttu-id="d74e8-150">ถ้าคุณไม่ต้องการใช้ตัวอย่างการวิเคราะห์โอกาสทางการขายอีกต่อไป คุณสามารถลบแดชบอร์ด รายงาน และชุดข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="d74e8-150">If you don't want to use the Opportunity Analysis Sample anymore, you can delete the dashboard, report, and dataset.</span></span>

## <a name="limitations-and-considerations"></a><span data-ttu-id="d74e8-151">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="d74e8-151">Limitations and considerations</span></span>
<span data-ttu-id="d74e8-152">สำหรับข้อมูลการแก้ไขปัญหา โปรดดูที่ [วิชวล Power Apps สำหรับ Power BI](/powerapps/maker/canvas-apps/powerapps-custom-visual#limitations-of-the-power-apps-visual)</span><span class="sxs-lookup"><span data-stu-id="d74e8-152">For troubleshooting information, see [Power Apps visual for Power BI](/powerapps/maker/canvas-apps/powerapps-custom-visual#limitations-of-the-power-apps-visual)</span></span>

## <a name="next-steps"></a><span data-ttu-id="d74e8-153">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d74e8-153">Next steps</span></span>
<span data-ttu-id="d74e8-154">[วิชวลการถามตอบ](power-bi-visualization-types-for-reports-and-q-and-a.md)  </span><span class="sxs-lookup"><span data-stu-id="d74e8-154">[Q&A visual](power-bi-visualization-types-for-reports-and-q-and-a.md)  </span></span>  
[<span data-ttu-id="d74e8-155">บทช่วยสอน: ฝังวิชวล Power Apps ในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="d74e8-155">Tutorial: Embed a Power Apps visual in a Power BI report</span></span>](/powerapps/maker/canvas-apps/powerapps-custom-visual)