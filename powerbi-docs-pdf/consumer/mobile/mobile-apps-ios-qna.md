---
title: นักวิเคราะห์เสมือนของถามตอบ ในแอป iOS - Power BI
description: ถามคำถามเกี่ยวกับข้อมูลตัวอย่างด้วยคำพูดของคุณเอง กับนักวิเคราะห์เสมือนของถามตอบ ในแอปสำหรับอุปกรณ์เคลื่อนที่ Power BI ในอุปกรณ์ iOS ของคุณ
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 03/11/2020
ms.openlocfilehash: 2422e747fc47f9e9b51f723f5e7beeeceaf91baa
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96397337"
---
# <a name="qa-virtual-analyst-in-ios-apps---power-bi"></a><span data-ttu-id="d2f2e-103">นักวิเคราะห์เสมือนของถามตอบ ในแอป iOS - Power BI</span><span class="sxs-lookup"><span data-stu-id="d2f2e-103">Q&A virtual analyst in iOS apps - Power BI</span></span>

<span data-ttu-id="d2f2e-104">วิธีง่ายที่สุดในการเรียนรู้เกี่ยวกับข้อมูลของคุณ คือ การถามคำถามเกี่ยวกับข้อมูลของคุณโดยใช้ถ้อยคำของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="d2f2e-104">The easiest way to learn about your data is to ask questions about it in your own words.</span></span> <span data-ttu-id="d2f2e-105">ในบทความนี้ คุณจะถามคำถาม และดูข้อมูลเชิงลึกที่แนะนำเกี่ยวกับข้อมูลตัวอย่าง ด้วยนักวิเคราะห์เสมือนของถามตอบ ในแอปมือถือ Microsoft Power BI บน iPad, iPhone และ iPod Touch</span><span class="sxs-lookup"><span data-stu-id="d2f2e-105">In this article, you ask questions and view featured insights about sample data with the Q&A virtual analyst in the Microsoft Power BI mobile app on your iPad, iPhone, and iPod Touch.</span></span> 

<span data-ttu-id="d2f2e-106">นำไปใช้กับ:</span><span class="sxs-lookup"><span data-stu-id="d2f2e-106">Applies to:</span></span>

| ![iPhone](./media/mobile-apps-ios-qna/iphone-logo-50-px.png) | ![iPad](./media/mobile-apps-ios-qna/ipad-logo-50-px.png) |
|:--- |:--- |
| <span data-ttu-id="d2f2e-109">iPhone</span><span class="sxs-lookup"><span data-stu-id="d2f2e-109">iPhones</span></span> |<span data-ttu-id="d2f2e-110">iPad</span><span class="sxs-lookup"><span data-stu-id="d2f2e-110">iPads</span></span> |

<span data-ttu-id="d2f2e-111">นักวิเคราะห์เสมือนของถามตอบ เป็นประสบการณ์การสนทนาข่าวกรองธุรกิจ ที่เข้าถึงข้อมูลการถามตอบเบื้องต้นในบริการของ Power BI [(https://powerbi.com)](https://powerbi.com)</span><span class="sxs-lookup"><span data-stu-id="d2f2e-111">The Q&A virtual analyst is a conversational BI experience that accesses underlying Q&A data in the Power BI service [(https://powerbi.com)](https://powerbi.com).</span></span> <span data-ttu-id="d2f2e-112">ซึ่งแนะนำข้อมูลเชิงลึก และคุณสามารถพิมพ์ หรือพูดคำถามของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="d2f2e-112">It suggests data insights, and you can type or speak your own questions.</span></span>

![นักวิเคราะห์เสมือนของถามตอบสำหรับยอดขายสูงสุด](./media/mobile-apps-ios-qna/power-bi-ios-q-n-a-top-sale-intro.png)

<span data-ttu-id="d2f2e-114">ถ้าคุณไม่ได้ลงทะเบียน Power BI ให้[ลงทะเบียนรุ่นทดลองใช้ฟรี](https://app.powerbi.com/signupredirect?pbi_source=web)ก่อนที่คุณจะเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d2f2e-114">If you're not signed up for Power BI, [sign up for a free trial](https://app.powerbi.com/signupredirect?pbi_source=web) before you begin.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d2f2e-115">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="d2f2e-115">Prerequisites</span></span>

* <span data-ttu-id="d2f2e-116">**ติดตั้งแอป Power BI สำหรับ iOS**: [ดาวน์โหลดแอป iOS](https://go.microsoft.com/fwlink/?LinkId=522062) ไปยัง iPhone หรือ iPad ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d2f2e-116">**Install the Power BI for iOS app**: [Download the iOS app](https://go.microsoft.com/fwlink/?LinkId=522062) to your iPhone or iPad.</span></span>
<span data-ttu-id="d2f2e-117">เวอร์ชันเหล่านี้รองรับแอป Power BI สำหรับ iOS:</span><span class="sxs-lookup"><span data-stu-id="d2f2e-117">These versions support the Power BI app for iOS:</span></span>
    * <span data-ttu-id="d2f2e-118">iPad ที่มี iOS 11 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="d2f2e-118">iPad with iOS 11 or later.</span></span>
    * <span data-ttu-id="d2f2e-119">iPhone 5 และสูงกว่า ที่มี iOS 11 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="d2f2e-119">iPhone 5 and above, with iOS 11 or later.</span></span>
* <span data-ttu-id="d2f2e-120">**ดาวน์โหลดตัวอย่างการวิเคราะห์ด้านการขายปลีกและการวิเคราะห์โอกาสทางการขาย**: ขั้นตอนแรกในเริ่มต้นใช้งานนี้คือ การดาวน์โหลดตัวอย่างการวิเคราะห์การค้าปลีก และตัวอย่างการวิเคราะห์โอกาสทางการขายในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="d2f2e-120">**Download the Retail Analysis and Opportunity Analysis Samples**: The first step in this quickstart is to download the Retail Analysis and Opportunity Analysis samples in the Power BI service.</span></span> <span data-ttu-id="d2f2e-121">[เรียนรู้วิธีการดาวน์โหลดตัวอย่าง](./mobile-apps-download-samples.md) ลงในบัญชี Power BI ของคุณเพื่อเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d2f2e-121">[Learn how to download a sample](./mobile-apps-download-samples.md) into your Power BI account to get started.</span></span> <span data-ttu-id="d2f2e-122">ตรวจสอบให้แน่ใจว่าได้เลือกตัวอย่างการวิเคราะห์ร้านค้าปลีกและตัวอย่างการวิเคราะห์โอกาสทางการขาย</span><span class="sxs-lookup"><span data-stu-id="d2f2e-122">Be sure to choose the Retail Analysis Sample and the Opportunity Analysis Sample.</span></span>

<span data-ttu-id="d2f2e-123">เมื่อคุณทำข้อกำหนดเบื้องต้นเสร็จสมบูรณ์แล้ว คุณพร้อมที่จะลองใช้นักวิเคราะห์เสมือนของถามตอบ</span><span class="sxs-lookup"><span data-stu-id="d2f2e-123">Once you've completed the prerequisites you are ready to try the Q&A virtual analyst.</span></span>

## <a name="try-asking-questions-on-your-iphone-or-ipad"></a><span data-ttu-id="d2f2e-124">ลองถามคำถามผ่าน iPhone หรือ iPad ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d2f2e-124">Try asking questions on your iPhone or iPad</span></span>
1. <span data-ttu-id="d2f2e-125">ที่แถบนำทางด้านล่างบน iPhone หรือ iPad ของคุณ ให้แตะปุ่มพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="d2f2e-125">On the bottom navigation bar on your iPhone or iPad, tap the Workspaces button</span></span> ![ปุ่มพื้นที่ทำงาน](./media/mobile-apps-ios-qna/power-bi-iphone-workspaces-button.png)<span data-ttu-id="d2f2e-127">ไปที่ พื้นที่ทำงานของฉัน แล้วเปิดแดชบอร์ดตัวอย่างการวิเคราะห์ด้านการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="d2f2e-127">, go to My Workspace, and open the Retail Analysis Sample dashboard.</span></span>

2. <span data-ttu-id="d2f2e-128">แตะไอคอนนักวิเคราะห์เสมือนของถามตอบ ![ไอคอนนักวิเคราะห์เสมือนของถามตอบ](././media/mobile-apps-ios-qna/power-bi-ios-q-n-a-icon.png) จากเมนูการดำเนินการที่ด้านล่างของหน้า (ที่ด้านบนของหน้าใน iPad)</span><span class="sxs-lookup"><span data-stu-id="d2f2e-128">Tap the Q&A virtual analyst icon ![Q&A virtual analyst icon](././media/mobile-apps-ios-qna/power-bi-ios-q-n-a-icon.png) from the action menu at the bottom of the page (at the top of the page on an iPad).</span></span>
     <span data-ttu-id="d2f2e-129">นักวิเคราะห์เสมือนของถามตอบจะมีตัวอย่างคำแนะนำ เพื่อเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d2f2e-129">The Q&A virtual analyst offers some suggestions to get started.</span></span>
3. <span data-ttu-id="d2f2e-130">พิมพ์ **แสดง** แตะที่ **ยอดขาย** จากรายการแนะนำ > **ส่ง** ![ไอคอนส่ง](./media/mobile-apps-ios-qna/power-bi-ios-qna-send-icon.png)</span><span class="sxs-lookup"><span data-stu-id="d2f2e-130">Type **show**, tap **sales** from the suggestion list > **Send** ![Send icon](./media/mobile-apps-ios-qna/power-bi-ios-qna-send-icon.png).</span></span>

    ![แสดงยอดขาย](./media/mobile-apps-ios-qna/power-bi-ios-q-n-a-show-sales.png)
4. <span data-ttu-id="d2f2e-132">แตะที่ **ตาม** จากคำสำคัญ จากนั้นแตะที่ **รายการ** จากรายการแนะนำ > **ส่ง** ![ไอคอนส่ง](./media/mobile-apps-ios-qna/power-bi-ios-qna-send-icon.png)</span><span class="sxs-lookup"><span data-stu-id="d2f2e-132">Tap **by** from the keywords, then tap **item** from the suggestion list > **Send** ![Send icon](./media/mobile-apps-ios-qna/power-bi-ios-qna-send-icon.png).</span></span>

    ![ยอดขายตามรายการสินค้า](./media/mobile-apps-ios-qna/power-bi-ios-q-n-a-sale-by-item.png)
5. แตะ **เป็น** จากคำหลักแล้วแตะไอคอนแผนภูมิคอลัมน์ :::image type="icon" source="./media/mobile-apps-ios-qna/power-bi-ios-q-n-a-column-chart-icon.png" border="false":::จากนั้นแตะ **ส่ง** ![ไอคอนส่ง](./media/mobile-apps-ios-qna/power-bi-ios-qna-send-icon.png)
6. <span data-ttu-id="d2f2e-135">แตะแผนภูมิผลลัพธ์ค้างไว้ แล้วแตะ **ขยาย**</span><span class="sxs-lookup"><span data-stu-id="d2f2e-135">Long-tap the resulting chart, then tap **Expand**.</span></span>

    ![ภาพหน้าจอของแผนภูมิคอลัมน์ ที่แสดงตัวชี้เพื่อขยาย](media/mobile-apps-ios-qna/power-bi-ios-q-n-a-tap-expand-feedback.png)

    <span data-ttu-id="d2f2e-137">แผนภูมิก็จะเปิดในโหมดโฟกัสในแอป</span><span class="sxs-lookup"><span data-stu-id="d2f2e-137">The chart opens in focus mode in the app.</span></span>

    ![ภาพหน้าจอของแผนภูมิคอลัมน์ ที่แสดงโหมดโฟกัสของแผนภูมิ](media/mobile-apps-ios-qna/power-bi-ios-q-n-a-expanded-chart.png)
7. <span data-ttu-id="d2f2e-139">แตะลูกศรที่มุมซ้ายบน เพื่อกลับไปยังหน้าต่างการสนทนาสำหรับนักวิเคราะห์เสมือนของถามตอบ</span><span class="sxs-lookup"><span data-stu-id="d2f2e-139">Tap the arrow in the upper-left corner to go back to the Q&A virtual analyst chat window.</span></span>
8. <span data-ttu-id="d2f2e-140">แตะ X ที่ด้านขวาของกล่องข้อความ เพื่อลบข้อความ แล้วเริ่มต้นอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="d2f2e-140">Tap the X at the right of the text box to delete the text and start over.</span></span>
9. <span data-ttu-id="d2f2e-141">ลองตั้งคำถามใหม่: แตะที่ **สูงสุด** จากคำสำคัญ แตะที่ **ยอดขายโดยเฉลี่ย $/หน่วย** > **ส่ง** ![ไอคอนส่ง](./media/mobile-apps-ios-qna/power-bi-ios-qna-send-icon.png)</span><span class="sxs-lookup"><span data-stu-id="d2f2e-141">Try a new question: Tap **top** from the keywords, tap **sale by avg $/unit ly** > **Send** ![Send icon](./media/mobile-apps-ios-qna/power-bi-ios-qna-send-icon.png).</span></span>

    ![ภาพหน้าจอของคำถาม ที่แสดงยอดขายสูงสุดตามจำนวนค่าเฉลี่ยต่อหน่วย](media/mobile-apps-ios-qna/power-bi-ios-q-n-a-top-sale-2.png)
10. <span data-ttu-id="d2f2e-143">เลือก **ตาม** จากคำสำคัญ แตะที่ **เวลา** จากรายการคำแนะนำด้านบน > **ส่ง** ![ไอคอนส่ง](./media/mobile-apps-ios-qna/power-bi-ios-qna-send-icon.png)</span><span class="sxs-lookup"><span data-stu-id="d2f2e-143">Choose **by** from the keywords, tap **time** from the suggestion list at the top > **Send** ![Send icon](./media/mobile-apps-ios-qna/power-bi-ios-qna-send-icon.png).</span></span>

     ![ภาพหน้าจอของแผนภูมิ ที่แสดงยอดขายสูงสุดตามจำนวนค่าเฉลี่ยต่อหน่วยตามเวลา](media/mobile-apps-ios-qna/power-bi-ios-q-n-a-top-sale-by-time.png)
11. พิมพ์ **เป็น** เลือกไอคอนแผนภูมิเส้น :::image type="icon" source="./media/mobile-apps-ios-qna/power-bi-ios-q-n-a-line-chart-icon.png" border="false"::: จากรายการคำแนะนำ> **ส่ง** ![ไอคอนส่ง](./media/mobile-apps-ios-qna/power-bi-ios-qna-send-icon.png)

    ![ภาพหน้าจอของคอลัมน์และแผนภูมิเส้น ที่แสดงตัวชี้จากคอลัมน์ไปยังแผนภูมิเส้น](media/mobile-apps-ios-qna/power-bi-ios-q-n-a-top-sale-as-line.png)

## <a name="try-saying-your-questions"></a><span data-ttu-id="d2f2e-147">ลองพูดถามคำถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="d2f2e-147">Try saying your questions</span></span>
<span data-ttu-id="d2f2e-148">ถึงตอนี้ คุณก็สามารถถามคำถามเกี่ยวกับข้อมูลของคุณในแอปสำหรับอุปกรณ์เคลื่อนที่ Power BI ได้โดยการพูดแทนที่จะใช้วิธีพิมพ์</span><span class="sxs-lookup"><span data-stu-id="d2f2e-148">You can now ask questions about your data in the Power BI mobile app by speaking instead of typing.</span></span>

1. <span data-ttu-id="d2f2e-149">แตะไอคอนนักวิเคราะห์เสมือนของถามตอบ</span><span class="sxs-lookup"><span data-stu-id="d2f2e-149">Tap the Q&A virtual analyst icon</span></span> ![ไอคอนนักวิเคราะห์เสมือนของถามตอบ](././media/mobile-apps-ios-qna/power-bi-ios-q-n-a-icon.png) <span data-ttu-id="d2f2e-151">จากเมนูการดำเนินการที่ด้านล่างของหน้า (ที่ด้านบนของหน้าใน iPad)</span><span class="sxs-lookup"><span data-stu-id="d2f2e-151">from the action menu at the bottom of the page (at the top of the page on an iPad).</span></span>
2. <span data-ttu-id="d2f2e-152">แตะไอคอนไมโครโฟน</span><span class="sxs-lookup"><span data-stu-id="d2f2e-152">Tap the microphone icon</span></span> ![ไอคอนไมโครโฟน](media/mobile-apps-ios-qna/power-bi-ios-qna-mic-icon.png)<span data-ttu-id="d2f2e-154">.</span><span class="sxs-lookup"><span data-stu-id="d2f2e-154">.</span></span>

    ![ภาพหน้าจอของคำถาม ที่แสดงว่าไมโครโฟนทำงานอยู่](media/mobile-apps-ios-qna/power-bi-ios-qna-mic-on.png)

1. <span data-ttu-id="d2f2e-156">เมื่อไอคอนไมโครโฟนพร้อมใช้งาน ให้เริ่มพูด</span><span class="sxs-lookup"><span data-stu-id="d2f2e-156">When the microphone icon is active, start speaking.</span></span> <span data-ttu-id="d2f2e-157">ตัวอย่างเช่น พูดว่า "average unit price by time (ราคาเฉลี่ยต่อหน่วยตามระยะเวลา)" จากนั้นแตะที่ **ส่ง** ![ไอคอนส่ง](./media/mobile-apps-ios-qna/power-bi-ios-qna-send-icon.png)</span><span class="sxs-lookup"><span data-stu-id="d2f2e-157">For example, say "average unit price by time", then tap **Send** ![Send icon](./media/mobile-apps-ios-qna/power-bi-ios-qna-send-icon.png).</span></span>

    ![ภาพหน้าจอของคำถาม ที่แสดงว่าคำพูดเสร็จสมบูรณ์](media/mobile-apps-ios-qna/power-bi-ios-qna-speech-complete.png)

### <a name="questions-about-privacy-when-using-speech-to-text"></a><span data-ttu-id="d2f2e-159">มีคำถามเกี่ยวกับความเป็นส่วนตัว เมื่อใช้การเปลี่ยนคำพูดให้เป็นข้อความหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d2f2e-159">Questions about privacy when using speech-to-text?</span></span>
<span data-ttu-id="d2f2e-160">โปรดดูส่วนเนื้อหาการรู้จำเสียงของ[มีอะไรใหม่ใน iOS](https://go.microsoft.com/fwlink/?linkid=845624) ในคู่มือสำหรับนักพัฒนา Apple iOS</span><span class="sxs-lookup"><span data-stu-id="d2f2e-160">See the Speech Recognition section of [What's New in iOS](https://go.microsoft.com/fwlink/?linkid=845624) in the Apple iOS Developer Guides.</span></span>

## <a name="help-and-feedback"></a><span data-ttu-id="d2f2e-161">วิธีใช้และคำติชม</span><span class="sxs-lookup"><span data-stu-id="d2f2e-161">Help and feedback</span></span>
* <span data-ttu-id="d2f2e-162">ต้องการความช่วยเหลือหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d2f2e-162">Need help?</span></span> <span data-ttu-id="d2f2e-163">เพียงแค่พูดว่า "Hi (สวัสดี)" หรือ "Help (ช่วยด้วย)" แล้วคุณก็จะได้รับความช่วยเหลือเกี่ยวกับการเริ่มต้นถามคำถามใหม่</span><span class="sxs-lookup"><span data-stu-id="d2f2e-163">Just say "Hi" or "Help", and you'll get assistance with starting a new question.</span></span>
* <span data-ttu-id="d2f2e-164">มีความประสงค์จะส่งคำติชมเกี่ยวกับผลลัพธ์นี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="d2f2e-164">Care to provide feedback on the results?</span></span> <span data-ttu-id="d2f2e-165">แตะแผนภูมิหรือผลลัพธ์อื่นๆ ค้างไว้ แล้วแตะที่รูปหน้ายิ้มหรือหน้าบึ้ง</span><span class="sxs-lookup"><span data-stu-id="d2f2e-165">Long-tap a chart or other result, then tap the smiley or frowny face.</span></span>

    ![ภาพหน้าจอของแผนภูมิคอลัมน์ ที่แสดงข้อคิดเห็นพร้อมด้วยตัวชี้ไปยังหน้ายิ้ม](media/mobile-apps-ios-qna/power-bi-ios-q-n-a-tap-feedback.png)

    <span data-ttu-id="d2f2e-167">คำติชมของคุณเป็นแบบไม่ระบุชื่อ และจะช่วยให้เราปรับปรุงการตอบคำถามของเรา</span><span class="sxs-lookup"><span data-stu-id="d2f2e-167">Your feedback is anonymous, and helps us improve our answers to questions.</span></span>

## <a name="enhance-your-qa-virtual-analyst-results"></a><span data-ttu-id="d2f2e-168">ปรับปรุงผลลัพธ์นักวิเคราะห์เสมือนของถามตอบของคุณ</span><span class="sxs-lookup"><span data-stu-id="d2f2e-168">Enhance your Q&A virtual analyst results</span></span>
<span data-ttu-id="d2f2e-169">คุณสามารถปรับปรุงผลลัพธ์ที่คุณและลูกค้าของคุณได้รับ เมื่อมีการใช้นักวิเคราะห์เสมือนของถามตอบในชุดข้อมูลได้ด้วยการถามคำถามที่กำหนดเป้าหมายแล้วเพิ่มมากขึ้น หรือการปรับปรุงชุดข้อมูลดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="d2f2e-169">You can improve the results you and your customers get when they use the Q&A virtual analyst on a dataset, either by asking more targeted questions or by enhancing the dataset.</span></span>

### <a name="how-to-ask-questions"></a><span data-ttu-id="d2f2e-170">วิธีการถามคำถาม</span><span class="sxs-lookup"><span data-stu-id="d2f2e-170">How to ask questions</span></span>
* <span data-ttu-id="d2f2e-171">ทำตาม [เคล็ดลับเหล่านี้ในการถามคำถามในถามตอบ](../end-user-q-and-a-tips.md) ในบริการของ Power BI หรือนักวิเคราะห์เสมือนของถามตอบในแอปสำหรับอุปกรณ์เคลื่อนที่ระบบ iOS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d2f2e-171">Follow these [tips for asking questions in Q&A](../end-user-q-and-a-tips.md) in the Power BI service or the Q&A virtual analyst in your iOS mobile app.</span></span>

### <a name="how-to-enhance-the-dataset"></a><span data-ttu-id="d2f2e-172">วิธีการปรับปรุงชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d2f2e-172">How to enhance the dataset</span></span>
* <span data-ttu-id="d2f2e-173">ปรับปรุงชุดข้อมูลใน Power BI Desktop หรือในบริการของ Power BI เพื่อ [ทำให้ข้อมูลของคุณสามารถใช้งานได้อย่างมีประสิทธิภาพในการถามตอบและนักวิเคราะห์เสมือนของถามตอบ](../../create-reports/service-prepare-data-for-q-and-a.md)</span><span class="sxs-lookup"><span data-stu-id="d2f2e-173">Enhance the dataset in Power BI Desktop or in the Power BI service to [make your data work well with Q&A and the Q&A virtual analyst](../../create-reports/service-prepare-data-for-q-and-a.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="d2f2e-174">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d2f2e-174">Next steps</span></span>
* [<span data-ttu-id="d2f2e-175">การถามตอบในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="d2f2e-175">Q&A in the Power BI service</span></span>](../end-user-q-and-a.md)
* <span data-ttu-id="d2f2e-176">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="d2f2e-176">Questions?</span></span> <span data-ttu-id="d2f2e-177">โปรดดู [ส่วนเนื้อหาแอปสำหรับอุปกรณ์เคลื่อนที่ของชุมชน Power BI](https://go.microsoft.com/fwlink/?linkid=839277)</span><span class="sxs-lookup"><span data-stu-id="d2f2e-177">Check the [Mobile apps section of the Power BI Community](https://go.microsoft.com/fwlink/?linkid=839277)</span></span>
