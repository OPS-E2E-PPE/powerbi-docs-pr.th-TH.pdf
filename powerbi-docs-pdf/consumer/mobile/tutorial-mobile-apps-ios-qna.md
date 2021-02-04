---
title: 'บทช่วยสอน: ถามคำถามกับ Q&A นักวิเคราะห์เสมือนในแอป iOS'
description: ในบทช่วยสอนนี้ ถามคำถามเกี่ยวกับข้อมูลตัวอย่างในคำพูดของคุณเอง กับนักวิเคราะห์เสมือนของถามตอบ ในแอปมือถือ Power BI บนอุปกรณ์ iOS ของคุณ
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: tutorial
ms.date: 11/26/2019
ms.openlocfilehash: 6d69f4527b838136b54ccfbad43d27fa247804d9
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415300"
---
# <a name="tutorial-ask-questions-about-your-data-with-the-qa-virtual-analyst-in-the-power-bi-ios-apps"></a><span data-ttu-id="ded30-103">บทช่วยสอน: ถามเกี่ยวกับข้อมูลของคุณกับ Q&A นักวิเคราะห์เสมือนในแอป Power BI iOS</span><span class="sxs-lookup"><span data-stu-id="ded30-103">Tutorial: Ask questions about your data with the Q&A virtual analyst in the Power BI iOS apps</span></span>

<span data-ttu-id="ded30-104">วิธีง่ายที่สุดในการเรียนรู้เกี่ยวกับข้อมูลของคุณ คือ การถามคำถามเกี่ยวกับข้อมูลของคุณโดยใช้ถ้อยคำของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="ded30-104">The easiest way to learn about your data is to ask questions about it in your own words.</span></span> <span data-ttu-id="ded30-105">ในบทช่วยสอนนี้ คุณถามคำถามและดูข้อมูลเชิงลึกที่แนะนำเกี่ยวกับข้อมูลตัวอย่าง กับนักวิเคราะห์เสมือนของถามตอบ ในแอปมือถือ Microsoft Power BI บน iPad หรือ iPhone ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ded30-105">In this tutorial, you ask questions and view featured insights about sample data with the Q&A virtual analyst in the Microsoft Power BI mobile app on your iPad or iPhone.</span></span> 

<span data-ttu-id="ded30-106">นำไปใช้กับ:</span><span class="sxs-lookup"><span data-stu-id="ded30-106">Applies to:</span></span>

| ![iPhone](./media/tutorial-mobile-apps-ios-qna/iphone-logo-50-px.png) | ![iPad](./media/tutorial-mobile-apps-ios-qna/ipad-logo-50-px.png) |
|:--- |:--- |
| <span data-ttu-id="ded30-109">iPhone</span><span class="sxs-lookup"><span data-stu-id="ded30-109">iPhones</span></span> |<span data-ttu-id="ded30-110">iPad</span><span class="sxs-lookup"><span data-stu-id="ded30-110">iPads</span></span> |

<span data-ttu-id="ded30-111">นักวิเคราะห์เสมือนของถามตอบ เป็นประสบการณ์การสนทนาข่าวกรองธุรกิจ ที่เข้าถึงข้อมูลการถามตอบเบื้องต้นใน [บริการของ Power BI](https://powerbi.com)</span><span class="sxs-lookup"><span data-stu-id="ded30-111">The Q&A virtual analyst is a conversational BI experience that accesses underlying Q&A data in the [Power BI service](https://powerbi.com).</span></span> <span data-ttu-id="ded30-112">ซึ่งแนะนำข้อมูลเชิงลึก และคุณสามารถพิมพ์ หรือพูดคำถามของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="ded30-112">It suggests data insights, and you can type or speak your own questions.</span></span>

![นักวิเคราะห์เสมือนของถามตอบสำหรับยอดขายสูงสุด](./media/tutorial-mobile-apps-ios-qna/power-bi-ios-q-n-a-top-sale-intro.png)

<span data-ttu-id="ded30-114">ในบทช่วยสอนนี้ คุณจะได้:</span><span class="sxs-lookup"><span data-stu-id="ded30-114">In this tutorial, you will:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="ded30-115">ติดตั้งแอป Power BI บนมือถือสำหรับ iOS</span><span class="sxs-lookup"><span data-stu-id="ded30-115">Install the Power BI mobile app for iOS</span></span>
> * <span data-ttu-id="ded30-116">ดาวน์โหลดรายงานและแดชบอร์ดตัวอย่าง Power BI</span><span class="sxs-lookup"><span data-stu-id="ded30-116">Download a Power BI sample dashboard and report</span></span>
> * <span data-ttu-id="ded30-117">ดูข้อมูลเชิงลึกที่แนะนำโดยแอปสำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="ded30-117">See what featured insights the mobile app suggests</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ded30-118">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="ded30-118">Prerequisites</span></span>

* <span data-ttu-id="ded30-119">**ลงทะเบียนใช้งาน Power BI**: ถ้าคุณไม่ได้ลงทะเบียน Power BI ให้ [ลงทะเบียนรุ่นทดลองใช้ฟรี](https://app.powerbi.com/signupredirect?pbi_source=web)ก่อนที่คุณจะเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ded30-119">**Sign up for Power BI**: If you're not signed up for Power BI, [sign up for a free trial](https://app.powerbi.com/signupredirect?pbi_source=web) before you begin.</span></span>
* <span data-ttu-id="ded30-120">**ติดตั้งแอป Power BI สำหรับ iOS**: [ดาวน์โหลดแอป iOS](https://apps.apple.com/app/microsoft-power-bi/id929738808) จาก Apple App Store ไปยัง iPad, iPhone หรือ iPod Touch ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ded30-120">**Install the Power BI for iOS app**: [Download the iOS app](https://apps.apple.com/app/microsoft-power-bi/id929738808) from the Apple App Store to your iPad, iPhone, or iPod Touch.</span></span> <span data-ttu-id="ded30-121">เวอร์ชันต่อไปนี้รองรับแอป Power BI สำหรับ iOS:</span><span class="sxs-lookup"><span data-stu-id="ded30-121">The following versions support the Power BI for iOS app:</span></span>
  * <span data-ttu-id="ded30-122">iPad ที่มี iOS 11 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="ded30-122">iPad with iOS 11 or later.</span></span>
  * <span data-ttu-id="ded30-123">iPhone 5 และสูงกว่า ที่มี iOS 11 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="ded30-123">iPhone 5 and above, with iOS 11 or later.</span></span> 
  * <span data-ttu-id="ded30-124">iPod Touch ที่มี iOS 11 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="ded30-124">iPod Touch with iOS 11 or later.</span></span>
* <span data-ttu-id="ded30-125">**ดาวน์โหลดข้อมูลตัวอย่าง**: ขั้นตอนแรกคือดาวน์โหลด **ตัวอย่างการวิเคราะห์โอกาส** ไปยังบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="ded30-125">**Download sample data**: The first step is to download the **Opportunity Analysis Sample** to the Power BI service.</span></span> <span data-ttu-id="ded30-126">ดู [การดาวน์โหลดตัวอย่างไปยังพื้นที่ทำงานของฉันในบริการ Power BI](./mobile-apps-download-samples.md) สำหรับคำแนะนำเกี่ยวกับวิธีการดำเนินการนี้</span><span class="sxs-lookup"><span data-stu-id="ded30-126">See [Downloading samples to My workspace in the Power BI service](./mobile-apps-download-samples.md) for instructions on how to do this.</span></span>


<span data-ttu-id="ded30-127">เมื่อคุณดำเนินการข้อกำหนดเบื้องต้นเสร็จสิ้นและดาวน์โหลดข้อมูลตัวอย่างแล้ว คุณก็พร้อมที่จะดูตัวอย่างบนอุปกรณ์ iOS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ded30-127">Once you've completed the prerequisites and downloaded the sample data, you're ready to view the samples on your iOS device.</span></span>

## <a name="try-featured-insights"></a><span data-ttu-id="ded30-128">ลองใช้ข้อมูลเชิงลึกที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="ded30-128">Try featured insights</span></span>
1. <span data-ttu-id="ded30-129">บน iPhone หรือ iPad ของคุณ เปิดแอป Power BI แล้วลงชื่อเข้าใช้ด้วยข้อมูลประจำตัวของบัญชีผู้ใช้ Power BI ของคุณ ซึ่งเป็นบัญชีเดียวกันกับที่คุณใช้ในบริการของ Power BI ในเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="ded30-129">On your iPhone or iPad, open the Power BI app and sign in with your Power BI account credentials, the same ones you used in the Power BI service in the browser.</span></span>

2. <span data-ttu-id="ded30-130">บนแถบนำทางของหน้าหลัก ให้แตะไอคอน **พื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="ded30-130">On the home page navigation bar, tap the  **Workspaces** icon.</span></span>

    ![เปิดพื้นที่ทำงานของฉัน](./media/tutorial-mobile-apps-ios-qna/power-bi-qna-open-myworkspace.png)

3. <span data-ttu-id="ded30-132">เมื่อเปิดหน้าพื้นที่ทำงานแล้ว ให้แตะ **พื้นที่ทำงานของฉัน** จากนั้นแดชบอร์ด **ตัวอย่างการวิเคราะห์โอกาส** เพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="ded30-132">When the Workspaces page opens, tap **My Workspaces** and then the **Opportunity Analysis Sample** dashboard to open it.</span></span>


3. <span data-ttu-id="ded30-133">บนแดชบอร์ดตัวอย่างการวิเคราะห์โอกาส ให้แตะไอคอนนักวิเคราะห์เสมือนของถามตอบในเมนูการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="ded30-133">On the Opportunity Analysis Sample dashboard, tap the Q&A virtual analyst icon on the action menu.</span></span>

    ![เปิดนักวิเคราะห์เสมือนของถามตอบ](./media/tutorial-mobile-apps-ios-qna/power-bi-qna-open-qna.png)

    <span data-ttu-id="ded30-135">นักวิเคราะห์เสมือนของถามตอบจะมีตัวอย่างคำแนะนำ เพื่อเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ded30-135">The Q&A virtual analyst offers some suggestions to get started.</span></span>

    ![ข้อเสนอแนะนักวิเคราะห์เสมือนของถามตอบ](./media/tutorial-mobile-apps-ios-qna/power-bi-qna-suggestions.png)

3. <span data-ttu-id="ded30-137">แตะ **ข้อมูลเชิงลึกที่แนะนำ**</span><span class="sxs-lookup"><span data-stu-id="ded30-137">Tap **featured insights**.</span></span>

4. <span data-ttu-id="ded30-138">นักวิเคราะห์เสมือนของถามตอบจะแนะนำตัวอย่างข้อมูลเชิงลึกให้คุณทราบ</span><span class="sxs-lookup"><span data-stu-id="ded30-138">The Q&A virtual analyst suggests some insights.</span></span> <span data-ttu-id="ded30-139">เลื่อนไปทางขวา แล้วแตะ **ข้อมูลเชิงลึก 2**</span><span class="sxs-lookup"><span data-stu-id="ded30-139">Scroll to the right and tap **Insight 2**.</span></span>

    ![ข้อมูลเชิงลึกที่แนะนำ](./media/tutorial-mobile-apps-ios-qna/power-bi-ios-qna-suggest-insight-2.png)

   <span data-ttu-id="ded30-141">นักวิเคราะห์เสมือนของถามตอบจะแสดงข้อมูลเชิงลึก 2</span><span class="sxs-lookup"><span data-stu-id="ded30-141">The Q&A virtual analyst displays Insight 2.</span></span>

    ![แสดงข้อมูลเชิงลึกที่แนะนำ](./media/tutorial-mobile-apps-ios-qna/power-bi-ios-qna-show-insight-2.png)

5. <span data-ttu-id="ded30-143">แตะแผนภูมิเพื่อเปิดในโหมดโฟกัส</span><span class="sxs-lookup"><span data-stu-id="ded30-143">Tap the chart to open it in focus mode.</span></span>

    ![เปิดแผนภูมิในโหมดโฟกัส](./media/tutorial-mobile-apps-ios-qna/power-bi-ios-qna-open-insight-2.png)

6. <span data-ttu-id="ded30-145">แตะลูกศรที่มุมซ้ายบน เพื่อกลับไปยังประสบการการใช้งานของนักวิเคราะห์เสมือนของถามตอบ</span><span class="sxs-lookup"><span data-stu-id="ded30-145">Tap the arrow in the upper-left corner to go back to the Q&A virtual analyst experience.</span></span>

## <a name="clean-up-resources"></a><span data-ttu-id="ded30-146">ล้างแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ded30-146">Clean up resources</span></span>

<span data-ttu-id="ded30-147">เมื่อคุณจบบทช่วยสอนนี้แล้ว คุณสามารถลบแดชบอร์ด, รายงาน และชุดข้อมูลของตัวอย่างการวิเคราะห์โอกาสทางการขายได้</span><span class="sxs-lookup"><span data-stu-id="ded30-147">When you've finished the tutorial, you can delete the Opportunity Analysis sample dashboard, report, and dataset.</span></span>

1. <span data-ttu-id="ded30-148">เปิดบริการ Power BI ([บริการ Power BI](https://app.powerbi.com)) และลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="ded30-148">Open the Power BI service ([Power BI service](https://app.powerbi.com)) and sign in.</span></span>

2. <span data-ttu-id="ded30-149">ในบานหน้าต่างการนำทาง ให้เลือก **พื้นที่ทำงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="ded30-149">In the navigation pane, select **My Workspace**.</span></span>

3. <span data-ttu-id="ded30-150">คลิกที่แท็บแดชบอร์ด จากนั้นบนบรรทัดตัวอย่างการวิเคราะห์โอกาส ให้คลิกที่ถังขยะ</span><span class="sxs-lookup"><span data-stu-id="ded30-150">Click the dashboards tab, and then on the Opportunity Analysis Sample line click the trash can.</span></span>

    ![สกรีนช็อตแสดงพื้นที่ทำงาน Power B I โดยแดชบอร์ดที่ถูกเลือกและไอคอนลบจะถูกเรียกออกมา](./media/tutorial-mobile-apps-ios-qna/power-bi-tutorial-mobile-apps-ios-qna-delete-opportunity-analysis-sample.png)

    <span data-ttu-id="ded30-152">เวลานี้ให้เลือกแท็บรายงานและทำแบบเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="ded30-152">Now select the reports tab and do the same.</span></span>

4. <span data-ttu-id="ded30-153">เวลานี้ให้เลือกแท็บชุดข้อมูล คลิก **ตัวเลือกเพิ่มเติม** (...) จากนั้นเลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="ded30-153">Now select the datasets tab, click **More options** (...), and then choose **Delete**.</span></span>

    ![สกรีนช็อตแสดงพื้นที่ทำงาน Power B I พร้อมชุดข้อมูลที่เลือกและลบที่เลือกจากเมนูตัวเลือกเพิ่มเติม](./media/tutorial-mobile-apps-ios-qna/power-bi-tutorial-mobile-apps-ios-qna-delete-opportunity-analysis-sample-datasets.png)

## <a name="next-steps"></a><span data-ttu-id="ded30-155">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="ded30-155">Next steps</span></span>

<span data-ttu-id="ded30-156">คุณได้ลอง นักวิเคราะห์เสมือนของถามตอบ ในแอปมือถือ Power BI สำหรับ iOS แล้ว</span><span class="sxs-lookup"><span data-stu-id="ded30-156">You've tried the Q&A virtual assistant in the Power BI mobile apps for iOS.</span></span> <span data-ttu-id="ded30-157">เรียนรู้เพิ่มเติมเกี่ยวกับ ถามตอบในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="ded30-157">Learn more about Q&A in the Power BI service.</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="ded30-158">การถามตอบในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="ded30-158">Q&A in the Power BI service</span></span>](../end-user-q-and-a.md)