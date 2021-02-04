---
title: 'เริ่มต้นใช้งานด่วน: สำรวจแดชบอร์ดและรายงานในแอปสำหรับอุปกรณ์เคลื่อนที่'
description: ในการเริ่มต้นใช้งานด่วนนี้ คุณสำรวจแดชบอร์ดและรายงานตัวอย่างได้ในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: quickstart
ms.date: 11/25/2019
ms.openlocfilehash: 35a942826c76ed1c202bcc5a3450c65374402c46
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96397567"
---
# <a name="quickstart-explore-dashboards-and-reports-in-the-power-bi-mobile-apps"></a><span data-ttu-id="547f3-103">เริ่มต้นใช้งานด่วน: สำรวจแดชบอร์ดและรายงานในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="547f3-103">Quickstart: Explore dashboards and reports in the Power BI mobile apps</span></span>
<span data-ttu-id="547f3-104">ในการเริ่มต้นใช้งานด่วนนี้ คุณจะได้เข้าชมแอป Power BI สำหรับอุปกรณ์เคลื่อนที่และสำรวจตัวอย่างแดชบอร์ดและรายงานได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="547f3-104">In this quickstart, you take a quick tour of the Power BI Mobile app and explore a sample dashboard and report.</span></span> <span data-ttu-id="547f3-105">แอป Power BI สำหรับ iOS จะแสดงขึ้นมาแต่คุณสามารถทำตามบนอุปกรณ์อื่นๆ ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="547f3-105">The Power BI app for iOS is shown, but you can easily follow along on other devices.</span></span>

<span data-ttu-id="547f3-106">นำไปใช้กับ:</span><span class="sxs-lookup"><span data-stu-id="547f3-106">Applies to:</span></span>

| ![iPhone](./media/mobile-apps-quickstart-view-dashboard-report/iphone-logo-30-px.png) | ![iPad](./media/mobile-apps-quickstart-view-dashboard-report/ipad-logo-30-px.png) | ![Android](./media/mobile-apps-quickstart-view-dashboard-report/android-logo-30-px.png) | ![อุปกรณ์ Windows 10](./media/mobile-apps-quickstart-view-dashboard-report/win-10-logo-30-px.png) |
|:--- |:--- |:--- |:--- |
| <span data-ttu-id="547f3-111">iPhone</span><span class="sxs-lookup"><span data-stu-id="547f3-111">iPhone</span></span> | <span data-ttu-id="547f3-112">iPad</span><span class="sxs-lookup"><span data-stu-id="547f3-112">iPad</span></span> | <span data-ttu-id="547f3-113">Android</span><span class="sxs-lookup"><span data-stu-id="547f3-113">Android</span></span> | <span data-ttu-id="547f3-114">Windows 10</span><span class="sxs-lookup"><span data-stu-id="547f3-114">Windows 10</span></span> |

>[!NOTE]
><span data-ttu-id="547f3-115">การสนับสนุนแอป Power BI สำหรับอุปกรณ์เคลื่อนที่ **เครื่องที่ใช้ Windows 10 Mobile** จะถูกยกเลิกในวันที่ 16 มีนาคม 2021</span><span class="sxs-lookup"><span data-stu-id="547f3-115">Power BI mobile app support for **phones using Windows 10 Mobile** will be discontinued on March 16, 2021.</span></span> [<span data-ttu-id="547f3-116">ศึกษาเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="547f3-116">Learn more</span></span>](/legal/powerbi/powerbi-mobile/power-bi-mobile-app-end-of-support-for-windows-phones)

<span data-ttu-id="547f3-117">แดชบอร์ดเป็นพอร์ทัลสำหรับอายุงานและกระบวนการของบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="547f3-117">A dashboard is a portal to your company's life cycle and processes.</span></span> <span data-ttu-id="547f3-118">คือภาพรวมหรือสถานที่เดียวที่สามารถตรวจสอบสถานะปัจจุบันของธุรกิจได้</span><span class="sxs-lookup"><span data-stu-id="547f3-118">It is an overview, a single place to monitor the current state of the business.</span></span> <span data-ttu-id="547f3-119">รายงาน คือ มุมมองแบบโต้ตอบของข้อมูลของคุณที่มีการแสดงผลด้วยภาพที่แสดงการค้นพบและข้อมูลเชิงลึกที่แตกต่างจากข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="547f3-119">Reports are interactive views of your data, with visuals representing different findings and insights from that data.</span></span> 

![รายงานในโหมดแนวนอน](././media/mobile-apps-quickstart-view-dashboard-report/power-bi-android-quickstart-report.png)

## <a name="prerequisites"></a><span data-ttu-id="547f3-121">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="547f3-121">Prerequisites</span></span>

* <span data-ttu-id="547f3-122">**ลงทะเบียนใช้งาน Power BI**: ถ้าคุณไม่ได้ลงทะเบียน Power BI ให้ [ลงทะเบียนรุ่นทดลองใช้ฟรี](https://app.powerbi.com/signupredirect?pbi_source=web)ก่อนที่คุณจะเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="547f3-122">**Sign up for Power BI**: If you're not signed up for Power BI, [sign up for a free trial](https://app.powerbi.com/signupredirect?pbi_source=web) before you begin.</span></span>
* <span data-ttu-id="547f3-123">**ติดตั้งแอป Power BI สำหรับอุปกรณ์ของคุณ**: ดาวน์โหลดแอป Power BI สำหรับอุปกรณ์เคลื่อนที่จาก [App store](https://apps.apple.com/app/microsoft-power-bi/id929738808) (iOS) และ [Google play](https://play.google.com/store/apps/details?id=com.microsoft.powerbim&amp;amp;clcid=0x409) (Android)</span><span class="sxs-lookup"><span data-stu-id="547f3-123">**Install the Power BI app for your device**: Download the Power BI mobile app\*\* from the [App store](https://apps.apple.com/app/microsoft-power-bi/id929738808) (iOS) or [Google play](https://play.google.com/store/apps/details?id=com.microsoft.powerbim&amp;amp;clcid=0x409) (Android).</span></span>
* <span data-ttu-id="547f3-124">**ดาวน์โหลดตัวอย่างการวิเคราะห์ร้านค้าปลีก**: ขั้นตอนแรกในการเริ่มต้นใช้งานด่วน คือ การดาวน์โหลดตัวอย่างการวิเคราะห์การค้าปลีกทางการขายในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="547f3-124">**Download the Retail Analysis Sample**: The first step in this quickstart is to download the Retail Analysis Sample in the Power BI service.</span></span> <span data-ttu-id="547f3-125">[เรียนรู้วิธีการดาวน์โหลดตัวอย่าง](./mobile-apps-download-samples.md) ลงในบัญชี Power BI ของคุณเพื่อเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="547f3-125">[Learn how to download a sample](./mobile-apps-download-samples.md) into your Power BI account to get started.</span></span> <span data-ttu-id="547f3-126">ตรวจสอบให้แน่ใจว่าได้เลือกตัวอย่างการวิเคราะห์ด้านการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="547f3-126">Be sure to choose the Retail Analysis Sample.</span></span>

<span data-ttu-id="547f3-127">หลังจากที่คุณเสร็จสิ้นข้อกำหนดเบื้องต้นและดาวน์โหลดตัวอย่างการวิเคราะห์ด้านการขายปลีกไปยังบัญชี Power BI ของคุณแล้ว คุณก็พร้อมที่จะเริ่มต้นทัวร์ด่วนนี้</span><span class="sxs-lookup"><span data-stu-id="547f3-127">Once you've completed the prerequisites and downloaded the Retail Analysis Sample to your Power BI account, you are ready to begin this quick tour.</span></span>

## <a name="view-a-dashboard-on-your-mobile-device"></a><span data-ttu-id="547f3-128">ดูแดชบอร์ดบนอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="547f3-128">View a dashboard on your mobile device</span></span>
1. <span data-ttu-id="547f3-129">บนอุปกรณ์ของคุณ เปิดแอป Power BI แล้วลงชื่อเข้าใช้ด้วยข้อมูลประจำตัวของบัญชีผู้ใช้ Power BI เดียวกันกับที่คุณใช้ในบริการ Power BI ในเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="547f3-129">On your device, open the Power BI app and sign in with your Power BI account credentials, the same ones you used in the Power BI service in the browser.</span></span>
 
1. <span data-ttu-id="547f3-130">ในตอนนี้ให้แตะที่ไอคอน **พื้นที่ทำงาน** ![ไอคอนพื้นที่ทำงาน](./media/mobile-apps-quickstart-view-dashboard-report/power-bi-iphone-workspaces-button.png) เลือก **พื้นที่ทำงานของฉัน** แล้วแตะตัวอย่างการวิเคราะห์ด้านการขายปลีกเพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="547f3-130">Now, tap the **Workspaces** icon ![workspaces icon](./media/mobile-apps-quickstart-view-dashboard-report/power-bi-iphone-workspaces-button.png), choose **My Workspaces**, and then tap the Retail Analysis Sample to open it.</span></span>

    ![แดชบอร์ดในพื้นที่ทำงานของฉัน](./media/mobile-apps-quickstart-view-dashboard-report/power-bi-android-quickstart-dashboard.png)
   
    <span data-ttu-id="547f3-132">แดชบอร์ด Power BI บนอุปกรณ์เคลื่อนที่ของคุณจะมีลักษณะแตกต่างกันเล็กน้อยจากบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="547f3-132">Power BI dashboards look a little different on your mobile device than they do on the Power BI service.</span></span> <span data-ttu-id="547f3-133">ไทล์ทั้งหมดจะปรากฏในขนาดเท่ากัน และถูกจัดเรียงทีละอันจากบนลงล่าง</span><span class="sxs-lookup"><span data-stu-id="547f3-133">All the tiles appear the same width, and they're arranged one after another from top to bottom.</span></span>

6. <span data-ttu-id="547f3-134">เลื่อนลงแล้วแตะแผนภูมิเส้นทึบ "ยอดขายของปีนี้ ยอดขายของปีที่แล้ว"</span><span class="sxs-lookup"><span data-stu-id="547f3-134">Scroll down and tap the "This Year's Sales, Last Year's Sales" filled line chart.</span></span>

    ![แตะไทล์เพื่อไปยังโหมดโฟกัส](./media/mobile-apps-quickstart-view-dashboard-report/power-bi-android-quickstart-tap-tile-fave.png)

    <span data-ttu-id="547f3-136">ไทล์จะเปิดขึ้นในโหมดโฟกัส</span><span class="sxs-lookup"><span data-stu-id="547f3-136">It opens in focus mode.</span></span>

7. <span data-ttu-id="547f3-137">ในโหมดโฟกัส แตะ **เม.ย.** ในแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="547f3-137">In focus mode, tap **Apr** in the chart.</span></span> <span data-ttu-id="547f3-138">ค่าสำหรับเดือนเมษายนจะปรากฏที่ด้านบนของแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="547f3-138">The values for April appear at the top of the chart.</span></span>

    ![ไทล์ในโหมดโฟกัส](./media/mobile-apps-quickstart-view-dashboard-report/power-bi-android-quickstart-tile-focus.png)

8. <span data-ttu-id="547f3-140">แตะไอคอนรายงาน</span><span class="sxs-lookup"><span data-stu-id="547f3-140">Tap the Report icon</span></span> ![ไอคอนรายงาน](./media/mobile-apps-quickstart-view-dashboard-report/power-bi-android-quickstart-report-icon.png) <span data-ttu-id="547f3-142">ที่ด้านล่างของหน้าจอ (บนอุปกรณ์ Android รายการนี้อาจอยู่ด้านบนของหน้าจอ)</span><span class="sxs-lookup"><span data-stu-id="547f3-142">at the bottom of the screen (on Android devices this may be at the top of the screen).</span></span> <span data-ttu-id="547f3-143">รายงานที่เกี่ยวข้องกับไทล์นี้จะเปิดขึ้นในโหมดแนวนอน</span><span class="sxs-lookup"><span data-stu-id="547f3-143">The report related to this tile opens in landscape mode.</span></span>

    ![รายงานในโหมดแนวนอน](././media/mobile-apps-quickstart-view-dashboard-report/power-bi-android-quickstart-report.png)

9. <span data-ttu-id="547f3-145">แตะฟองสีเหลือง "Juniors 040 -" ในแผนภูมิฟอง</span><span class="sxs-lookup"><span data-stu-id="547f3-145">Tap the yellow "040 - Juniors" bubble in the bubble chart.</span></span> <span data-ttu-id="547f3-146">สังเกตวิธีการไฮไลท์ค่าที่เกี่ยวข้องในแผนภูมิอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="547f3-146">Note how it highlights related values in the other charts.</span></span> 

    ![ไฮไลท์ค่าในรายงาน](./media/mobile-apps-quickstart-view-dashboard-report/power-bi-android-quickstart-cross-highlight.png)

10. <span data-ttu-id="547f3-148">ปัดขึ้นเพื่อดูแถบเครื่องมือที่ด้านล่าง และแตะ **ตัวเลือกเพิ่มเติม (...)**</span><span class="sxs-lookup"><span data-stu-id="547f3-148">Swipe up to see a toolbar across the bottom, and tap **More options (...)**.</span></span>

    ![สกรีนช็อตแสดงตำแหน่งที่ตั้งของตัวควบคุมตัวเลือกเพิ่มเติมที่มุมล่างขวา](./media/mobile-apps-quickstart-view-dashboard-report/power-bi-android-quickstart-tap-pencil.png)


11. <span data-ttu-id="547f3-150">เลื่อนดูรายการ แล้วเลือก **ใส่คำอธิบายประกอบ**</span><span class="sxs-lookup"><span data-stu-id="547f3-150">Scroll down the list and select **Annotate**.</span></span>

    ![แตะที่ดินสอ](./media/mobile-apps-quickstart-view-dashboard-report/power-bi-android-quickstart-tap-pencil2.png)

12. <span data-ttu-id="547f3-152">บนแถบเครื่องมือใส่คำอธิบายประกอบ ให้แตะไอคอนรูปหน้ายิ้ม จากนั้นแตะหน้ารายงานที่คุณต้องการเพิ่มใบหน้ายิ้มบางรายการ</span><span class="sxs-lookup"><span data-stu-id="547f3-152">On the annotate toolbar, tap the smiley-face icon and then tap the report page where you'd like to add some smiley faces.</span></span>
 
    ![ใส่คำอธิบายประกอบหน้า](./media/mobile-apps-quickstart-view-dashboard-report/power-bi-android-quickstart-annotate.png)

13. <span data-ttu-id="547f3-154">ในเวลานี้ ให้แตะ **แชร์** ที่มุมบนขวา</span><span class="sxs-lookup"><span data-stu-id="547f3-154">Now tap **Share** in the upper-right corner.</span></span>

14. <span data-ttu-id="547f3-155">เลือกวิธีที่คุณต้องการแชร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="547f3-155">Choose the way you'd like to share the report.</span></span>  

    ![ข้อความอีเมลใหม่พร้อมสแนปช็อตและลิงก์](./media/mobile-apps-quickstart-view-dashboard-report/power-bi-android-quickstart-send-snapshot.png)

    <span data-ttu-id="547f3-157">คุณสามาราถแชร์สแนปช็อตนี้กับใครก็ได้ ทั้งภายในและภายนอกองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="547f3-157">You can share this snapshot with anyone, in or out of your organization.</span></span> <span data-ttu-id="547f3-158">หากพวกเขาอยู่ในองค์กรของคุณและมีบัญชี Power BI ของตนเอง พวกเขาจะสามารถเปิดรายงานตัวอย่างการวิเคราะห์ด้านการขายปลีกได้ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="547f3-158">If they're in your organization and have their own Power BI account, they'll be able to open the Retail Analysis Sample report, too.</span></span>

## <a name="clean-up-resources"></a><span data-ttu-id="547f3-159">ล้างแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="547f3-159">Clean up resources</span></span>

<span data-ttu-id="547f3-160">หลังจากที่คุณดำเนินการเริ่มต้นด่วนนี้เสร็จสิ้นแล้ว คุณสามารถลบแดชบอร์ด รายงาน และชุดข้อมูลตัวอย่างการวิเคราะห์ด้านการขายปลีก ถ้าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="547f3-160">After you finish this quickstart, you can delete the Retail Analysis Sample dashboard, report, and dataset, if you wish.</span></span>

1. <span data-ttu-id="547f3-161">เปิดบริการ Power BI ([บริการ Power BI](https://app.powerbi.com)) และลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="547f3-161">Open the Power BI service ([Power BI service](https://app.powerbi.com)) and sign in.</span></span>

2. <span data-ttu-id="547f3-162">ในบานหน้าต่างการนำทาง ให้เลือก **พื้นที่ทำงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="547f3-162">In the navigation pane, select **My Workspace**.</span></span>

3. <span data-ttu-id="547f3-163">เลือกแท็บแดชบอร์ดและจากนั้นคลิกที่ถังขยะ</span><span class="sxs-lookup"><span data-stu-id="547f3-163">Select the dashboards tab and then click the trash can.</span></span>

    ![เลือกไอคอนลบ](./media/mobile-apps-quickstart-view-dashboard-report/power-bi-android-quickstart-delete-retail.png)

    <span data-ttu-id="547f3-165">ในเวลานี้ให้คลิกที่แท็บรายงานแล้วทำเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="547f3-165">Now click the reports tab and do the same.</span></span>

4. <span data-ttu-id="547f3-166">ในเวลานี้ให้เลือกแท็บชุดข้อมูล คลิก **ตัวเลือกเพิ่มเติม** (...) แล้วเลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="547f3-166">Now select the datasets tab, click **More options** (...), and choose **Delete**.</span></span> 


    ![เลือกชุดข้อมูลลบ](./media/mobile-apps-quickstart-view-dashboard-report/power-bi-android-quickstart-delete-retail-datasets.png)

## <a name="next-steps"></a><span data-ttu-id="547f3-168">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="547f3-168">Next steps</span></span>

<span data-ttu-id="547f3-169">ในการเริ่มต้นใช้งานด่วนนี้ คุณสำรวจแดชบอร์ดและรายงานตัวอย่างได้ในอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="547f3-169">In this quickstart, you explored a sample dashboard and report on your mobile device.</span></span> <span data-ttu-id="547f3-170">อ่านเพิ่มเติมเกี่ยวกับการทำงานในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="547f3-170">Read more about working in the Power BI service.</span></span> 

> [!div class="nextstepaction"]
> [<span data-ttu-id="547f3-171">เริ่มต้นใช้งานด่วน: สำรวจบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="547f3-171">Quickstart: Getting around in the Power BI service</span></span>](../end-user-experience.md)