---
title: 'บทช่วยสอน: ตั้งค่าการแจ้งเตือนข้อมูลในแดชบอร์ดบริการของ Power BI'
description: ในโปรแกรมการสอนนี้คุณจะได้เรียนรู้การตั้งค่าการแจ้งเตือนเพื่อแจ้งให้คุณทราบเมื่อข้อมูลในแดชบอร์ดของคุณเปลี่ยนแปลงเกินขีด จำกัดที่คุณได้ตั้งไว้ในบริการ Microsoft Power BI
author: mihart
ms.author: mihart
ms.reviewer: mihart
featuredvideoid: removed
ms.service: powerbi
ms.subservice: pbi-explore
ms.topic: how-to
ms.date: 12/03/2020
LocalizationGroup: Dashboards
ms.openlocfilehash: 369eb05795262ad628b9dd89c23ac59269e6f6c3
ms.sourcegitcommit: cb6e0202de27f29dd622e47b305c15f952c5769b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/03/2020
ms.locfileid: "96577612"
---
# <a name="tutorial-set-alerts-on-power-bi-dashboards"></a><span data-ttu-id="21367-103">บทช่วยสอน: ตั้งค่าการแจ้งเตือนบนแดชบอร์ด Power BI</span><span class="sxs-lookup"><span data-stu-id="21367-103">Tutorial: Set alerts on Power BI dashboards</span></span>

[!INCLUDE[consumer-appliesto-yynn](../includes/consumer-appliesto-yynn.md)]


<span data-ttu-id="21367-104">ตั้งค่าการแจ้งเตือนในบริการ Power BI เพื่อแจ้งให้คุณทราบเมื่อข้อมูลบนแดชบอร์ดเปลี่ยนแปลงเหนือหรือต่ำกว่าขีดจำกัดที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="21367-104">Set alerts in the Power BI service to notify you when data on a dashboard changes above or below limits you set.</span></span> <span data-ttu-id="21367-105">การแจ้งเตือนสามารถตั้งค่าบนหมุดไทล์ที่ปักหมุดจากวิชวลรายงานเท่านั้น และบนหน้าปัดวัด Kpi และการ์ดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="21367-105">Alerts can only be set on tiles pinned from report visuals, and only on gauges, KPIs, and cards.</span></span> 

![ไทล์, การ์ด, KPI](media/end-user-alerts/card-gauge-kpi.png)

<span data-ttu-id="21367-107">สามารถสร้างการแจ้งเตือนบนแดชบอร์ด:</span><span class="sxs-lookup"><span data-stu-id="21367-107">Alerts can be created on dashboards:</span></span>
- <span data-ttu-id="21367-108">ที่คุณสร้างและบันทึกไว้ใน **พื้นที่ทำงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="21367-108">that you have created and saved in **My workspace**</span></span>
- <span data-ttu-id="21367-109">ที่แบ่งปันกับคุณใน [ความจุแบบพรีเมียม](end-user-license.md)</span><span class="sxs-lookup"><span data-stu-id="21367-109">that have been shared with you in a [Premium capacity](end-user-license.md).</span></span> 
- <span data-ttu-id="21367-110">ในพื้นที่ทำงานใด ๆ คุณก็สามารถเข้าถึงได้ ถ้าคุณมีสิทธิ์การใช้งาน Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="21367-110">in any workspace you can access, if you have a Power BI Pro license.</span></span>    

<span data-ttu-id="21367-111">ข้อความแจ้งเตือนทำงานกับข้อมูลที่ได้รับการรีเฟรชเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="21367-111">Alerts only work on data that is refreshed.</span></span> <span data-ttu-id="21367-112">เมื่อมีการรีเฟรชข้อมูล Power BI จะค้นหาเพื่อดูว่าข้อความแจ้งเตือนถูกตั้งค่าสำหรับข้อมูลนั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="21367-112">When data refreshes, Power BI looks to see if an alert is set for that data.</span></span> <span data-ttu-id="21367-113">ถ้าข้อมูลได้ถึงค่าเกณฑ์การแจ้งเตือน ข้อความแจ้งเตือนจะถูกเริ่ม</span><span class="sxs-lookup"><span data-stu-id="21367-113">If the data has reached an alert threshold, an alert is triggered.</span></span> 

<span data-ttu-id="21367-114">คุณลักษณะนี้ยังคงได้รับการพัฒนา ดังนั้นโปรดดู[คำแนะนำและหัวข้อการแก้ไขปัญหาด้านล่าง](#tips-and-troubleshooting)</span><span class="sxs-lookup"><span data-stu-id="21367-114">This feature is still evolving, so refer to the [Tips and troubleshooting section below](#tips-and-troubleshooting).</span></span>



<span data-ttu-id="21367-115">มีเพียงคุณที่สามารถดูการแจ้งเตือนที่คุณตั้งไว้ แม้ว่าคุณได้แชร์แดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="21367-115">Only you can see the alerts you set, even if you share your dashboard.</span></span> <span data-ttu-id="21367-116">การแจ้งเตือนข้อมูลจะถูกซิงโครไนซ์เต็มรูปแบบข้ามแพลตฟอร์ม ตั้งค่าและดูการแจ้งเตือนข้อมูลได้[ในแอป mobile Power BI](mobile/mobile-set-data-alerts-in-the-mobile-apps.md)และใน Power BI service</span><span class="sxs-lookup"><span data-stu-id="21367-116">Data alerts are fully synchronized across platforms; set and view data alerts [in the Power BI mobile apps](mobile/mobile-set-data-alerts-in-the-mobile-apps.md) and in the Power BI service.</span></span> 

> [!WARNING]
> <span data-ttu-id="21367-117">การแจ้งเตือนเหล่านี้จะให้ข้อมูลเกี่ยวกับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="21367-117">These alerts provide information about your data.</span></span> <span data-ttu-id="21367-118">ถ้าคุณดูข้อมูล Power BI ของคุณบนอุปกรณ์เคลื่อนที่ และอุปกรณ์ที่ถูกขโมย เราขอแนะนำให้ใช้บริการของ Power BI เพื่อปิดการแจ้งเตือนทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="21367-118">If you view your Power BI data on a mobile device and that device gets stolen, we recommend using the Power BI service to turn off all alerts.</span></span>
> 

<span data-ttu-id="21367-119">บทช่วยสอนนี้ครอบคลุมเรื่องต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="21367-119">This tutorial covers the following.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="21367-120">ใครสามารถตั้งค่าการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="21367-120">Who can set alerts</span></span>
> * <span data-ttu-id="21367-121">ภาพที่รองรับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="21367-121">Which visuals support alerts</span></span>
> * <span data-ttu-id="21367-122">ผู้ที่สามารถดูการแจ้งเตือนของฉัน</span><span class="sxs-lookup"><span data-stu-id="21367-122">Who can see my alerts</span></span>
> * <span data-ttu-id="21367-123">การแจ้งเตือนการทำงาน บน Power BI Desktop และอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="21367-123">Do alerts work on Power BI Desktop and mobile</span></span>
> * <span data-ttu-id="21367-124">วิธีการสร้างการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="21367-124">How to create an alert</span></span>
> * <span data-ttu-id="21367-125">รับการแจ้งเตือนของฉันที่ไหน</span><span class="sxs-lookup"><span data-stu-id="21367-125">Where will I receive my alerts</span></span>

## <a name="prerequisites"></a><span data-ttu-id="21367-126">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="21367-126">Prerequisites</span></span>

<span data-ttu-id="21367-127">ถ้าคุณไม่ได้ลงทะเบียน Power BI ให้[ลงทะเบียนรุ่นทดลองใช้ฟรี](https://app.powerbi.com/signupredirect?pbi_source=web)ก่อนที่คุณจะเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="21367-127">If you're not signed up for Power BI, [sign up for a free trial](https://app.powerbi.com/signupredirect?pbi_source=web) before you begin.</span></span>

1. <span data-ttu-id="21367-128">ตัวอย่างนี้ใช้ไทล์การ์ดแดชบอร์ดจากตัวอย่างการขายและการตลาด</span><span class="sxs-lookup"><span data-stu-id="21367-128">This example uses a dashboard card tile from the Sales & Marketing sample.</span></span> <span data-ttu-id="21367-129">เปิดบริการ Power BI (app.powerbi.com) ลงชื่อเข้าใช้และเปิด **พื้นที่ทำงานของฉัน** ของคุณ</span><span class="sxs-lookup"><span data-stu-id="21367-129">Open the Power BI service (app.powerbi.com), sign in, and open your **My Workspace**.</span></span>    
    <span data-ttu-id="21367-130">![เปิดพื้นที่ทำงานของฉัน](media//end-user-alerts/power-bi-my-workspace.png)</span><span class="sxs-lookup"><span data-stu-id="21367-130">![Open My Workspace](media//end-user-alerts/power-bi-my-workspace.png)</span></span>

2. <span data-ttu-id="21367-131">ในมุมด้านล่างซ้าย เลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="21367-131">In the bottom-left corner, select **Get data**.</span></span>

    ![เลือกรับข้อมูล](media//end-user-alerts/power-bi-get-data.png)

3. <span data-ttu-id="21367-133">ในหน้ารับข้อมูลที่ปรากฏขึ้น ให้เลือก **ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="21367-133">On the Get data page that appears, select **Samples**.</span></span>

4. <span data-ttu-id="21367-134">เลือกตัวอย่างการขายและการตลาด จากนั้นเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="21367-134">Select the Sales and Marketing Sample, then choose **Connect**.</span></span>

    ![ดาวน์โหลดตัวอย่างการขายและการตลาด](media//end-user-alerts/power-bi-sample.png)

5. <span data-ttu-id="21367-136">หลังจาก Power BI เชื่อมต่อกับตัวอย่างแล้ว ให้เลือก **ไปที่แดชบอร์ด** จากกล่องโต้ตอบที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="21367-136">After Power BI has connected to the sample, select **Go to dashboard** from the dialog that appears.</span></span>     
    <span data-ttu-id="21367-137">![เปิดตัวอย่างการขายและการตลาด](media//end-user-alerts/power-bi-go-to-dashboard.png)</span><span class="sxs-lookup"><span data-stu-id="21367-137">![Open the Sales and Marketing sample](media//end-user-alerts/power-bi-go-to-dashboard.png)</span></span>

## <a name="add-an-alert-to-a-dashboard-tile"></a><span data-ttu-id="21367-138">เพิ่มการแจ้งเตือนไปยังไทล์แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="21367-138">Add an alert to a dashboard tile</span></span>

1. <span data-ttu-id="21367-139">จากแป้นวัดแดชบอร์ด KPI หรือการ์ดไทล์ เลือกจุดไข่ปลา</span><span class="sxs-lookup"><span data-stu-id="21367-139">From a dashboard gauge, KPI, or card tile, select the ellipsis.</span></span>
   
   ![ไทล์การ์ด](media/end-user-alerts/power-bi-card.png)

2. <span data-ttu-id="21367-141">เลือกไอคอนการแจ้งเตือน ![ไอคอนการแจ้งเตือน](media/end-user-alerts/power-bi-alert-icon.png) หรือ **จัดการการแจ้งเตือน** เพื่อเพิ่มการแจ้งเตือนอย่างน้อยหนึ่งรายการสำหรับการ์ด **ส่วนแบ่งทางการตลาด**</span><span class="sxs-lookup"><span data-stu-id="21367-141">Select the alert icon ![Alert icon](media/end-user-alerts/power-bi-alert-icon.png), or **Manage alerts**, to add one or more alerts for the **Market share** card.</span></span>

   ![ไทล์การ์ดพร้อมด้วยจุดไข่ปลาที่เลือก](media/end-user-alerts/power-bi-manage.png)

   
1. <span data-ttu-id="21367-143">บนบานหน้าต่าง **จัดการการแจ้งเตือน** เลือก **+ เพิ่มกฎการแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="21367-143">On the **Manage alerts** pane, select **+ Add alert rule**.</span></span>  <span data-ttu-id="21367-144">ตรวจสอบให้แน่ใจว่า แถบเลื่อนถูกตั้งค่าเป็น **เปิด** และตั้งชื่อให้การแจ้งเตือนของคุณ</span><span class="sxs-lookup"><span data-stu-id="21367-144">Ensure the slider is set to **On**, and give your alert a title.</span></span> <span data-ttu-id="21367-145">ชื่อช่วยให้คุณสามารถจดจำข้อความการแจ้งเตือนของคุณได้</span><span class="sxs-lookup"><span data-stu-id="21367-145">Titles help you easily recognize your alerts.</span></span>
   
   ![เพิ่มหน้าต่างกฎการแจ้งเตือน](media/end-user-alerts/power-bi-alert-manage.png)
4. <span data-ttu-id="21367-147">เลื่อนลง แล้วใส่รายละเอียดการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="21367-147">Scroll down and enter the alert details.</span></span>  <span data-ttu-id="21367-148">ในตัวอย่างนี้เราจะสร้างการแจ้งเตือนที่แจ้งให้เราทราบวันละครั้งหากส่วนแบ่งทางการตลาดของเราเพิ่มขึ้นเป็น 40 หรือสูงกว่า</span><span class="sxs-lookup"><span data-stu-id="21367-148">In this example we'll create an alert that notifies us once a day if our market share increases to 40 or higher.</span></span> <span data-ttu-id="21367-149">การแจ้งเตือนจะปรากฏใน [ศูนย์การแจ้งเตือน](end-user-notification-center.md) ของเรา</span><span class="sxs-lookup"><span data-stu-id="21367-149">Alerts will appear in our [Notification center](end-user-notification-center.md).</span></span> <span data-ttu-id="21367-150">และเราจะให้ Power BI ส่งอีเมลเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="21367-150">And we'll have Power BI send us an email as well.</span></span>
   
   ![จัดการหน้าต่างข้อความแจ้งเตือน ตั้งค่าเกณฑ](media/end-user-alerts/power-bi-manage-alert-detail.png)

5. <span data-ttu-id="21367-152">เลือก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="21367-152">Select **Save and close**.</span></span>
 


   > 

## <a name="receiving-alerts"></a><span data-ttu-id="21367-153">การรับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="21367-153">Receiving alerts</span></span>
<span data-ttu-id="21367-154">เมื่อติดตามข้อมูลถึงค่าเกณฑ์หนึ่งที่คุณตั้งไว้ เกิดหลายสิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="21367-154">When the data being tracked reaches one of the thresholds you've set, several things happen.</span></span> <span data-ttu-id="21367-155">ประการแรก Power BI จะตรวจสอบเพื่อดูว่าเกินหนึ่งชั่วโมงหรือ 24 ชั่วโมงแล้วหรือไม่ (ขึ้นอยู่กับตัวเลือกที่คุณเลือก) นับตั้งแต่มีการส่งการแจ้งเตือนล่าสุด</span><span class="sxs-lookup"><span data-stu-id="21367-155">First, Power BI checks to see if it has been more than an hour, or more than 24 hours (depending on the option you selected), since the last alert was sent.</span></span> <span data-ttu-id="21367-156">ตราบใดที่ข้อมูลเกินค่าเกณฑ์ คุณจะได้รับการแจ้งเตือนทุกชั่วโมงหรือทุกๆ 24 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="21367-156">As long as the data is past the threshold, you'll get an alert.</span></span>

<span data-ttu-id="21367-157">ถัดไป Power BI ส่งข้อความแจ้งเตือนไปยังศูนย์การแจ้งเตือนของคุณ และหรือในอีเมล</span><span class="sxs-lookup"><span data-stu-id="21367-157">Next, Power BI sends an alert to your Notification center and, optionally, in email.</span></span> <span data-ttu-id="21367-158">แต่ละข้อความแจ้งเตือนประกอบด้วยการเชื่อมโยงโดยตรงกับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="21367-158">Each alert contains a direct link to your data.</span></span> <span data-ttu-id="21367-159">เลือกลิงก์เพื่อดูไทล์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="21367-159">Select the link to see the relevant tile.</span></span>  

1. <span data-ttu-id="21367-160">ถ้าคุณได้ตั้งค่าการแจ้งเตือนให้ส่งอีเมล์ คุณจะพบสิ่งที่เหมือนสิ่งนี้้ในกล่องอีเมลเข้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="21367-160">If you've set the alert to send you an email, you'll find something like this in your Inbox.</span></span> <span data-ttu-id="21367-161">นี่คือการแจ้งเตือนที่เราตั้งไว้สำหรับการ์ด **ความคิดเห็น**</span><span class="sxs-lookup"><span data-stu-id="21367-161">This is an alert we set for the **Sentiment** card.</span></span>
   
   ![อีเมลแจ้งเตือน](media/end-user-alerts/power-bi-email.png)
2. <span data-ttu-id="21367-163">Power BI ยังเพิ่มข้อความใน **ศูนย์การแจ้งเตือน** ของคุณ</span><span class="sxs-lookup"><span data-stu-id="21367-163">Power BI also adds a message to your **Notification center**.</span></span>
   
   ![ไอคอนการแจ้งเตือนใน Power BI service](media/end-user-alerts/power-bi-task.png)
3. <span data-ttu-id="21367-165">เปิดศูนย์การแจ้งเตือนของคุณเพื่อดูรายละเอียดการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="21367-165">Open your Notification center to see the alert details.</span></span>
   
    ![อ่านการแจ้งเตืิอน](media/end-user-alerts/power-bi-notifications.png)
   
  

## <a name="managing-alerts"></a><span data-ttu-id="21367-167">การจัดการการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="21367-167">Managing alerts</span></span>

<span data-ttu-id="21367-168">มีหลายวิธีในการจัดการการแจ้งเตือนของคุณ: จากไทล์แดชบอร์ดเอง จากเมนูการตั้งค่า Power BI บนไทล์แต่ละรายการใน [แอปมือถือ Power BI บน iPhone](mobile/mobile-set-data-alerts-in-the-mobile-apps.md) หรือใน [แอปมือถือ Power BI สำหรับ Windows 10](mobile/mobile-set-data-alerts-in-the-mobile-apps.md)</span><span class="sxs-lookup"><span data-stu-id="21367-168">There are many ways to manage your alerts: from the dashboard tile itself, from the Power BI Settings menu, on an individual tile in the [Power BI mobile app on the iPhone](mobile/mobile-set-data-alerts-in-the-mobile-apps.md), or in the [Power BI mobile app for Windows 10](mobile/mobile-set-data-alerts-in-the-mobile-apps.md).</span></span>

### <a name="from-the-tile-itself"></a><span data-ttu-id="21367-169">จากตัวไทล์เอง</span><span class="sxs-lookup"><span data-stu-id="21367-169">From the tile itself</span></span>

1. <span data-ttu-id="21367-170">หากคุณต้องการเปลี่ยนหรือลบการแจ้งเตือนสำหรับไทล์ ให้เปิดหน้าต่าง **จัดการการแจ้งเตือน** อีกครั้งโดยเลือกไอคอนการแจ้งเตือน ![ไอคอนการแจ้งเตือน](media/end-user-alerts/power-bi-alert-icon.png)</span><span class="sxs-lookup"><span data-stu-id="21367-170">If you need to change or remove an alert for a tile, re-open the **Manage alerts** window by selecting the alert icon ![Alert icon](media/end-user-alerts/power-bi-alert-icon.png).</span></span> <span data-ttu-id="21367-171">แจ้งเตือนทั้งหมดที่คุณได้ตั้งค่าสำหรับไทล์ได้แสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="21367-171">All the alerts that you've set for that tile are displayed.</span></span>
   
    ![จัดการหน้าต่างการแจ้งเตือน](media/end-user-alerts/power-bi-manage-alert.png)<span data-ttu-id="21367-173">.</span><span class="sxs-lookup"><span data-stu-id="21367-173">.</span></span>
2. <span data-ttu-id="21367-174">เพื่อเปลี่ยนข้อความแจ้งเตือน ให้เลือกลูกศรทางด้านซ้ายของชื่อการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="21367-174">To modify an alert, select the arrow to the left of the alert name.</span></span>
   
    ![ลูกศรถัดจากชื่อการแจ้งเตือน](media/end-user-alerts/power-bi-alert-modify.png)<span data-ttu-id="21367-176">.</span><span class="sxs-lookup"><span data-stu-id="21367-176">.</span></span>
3. <span data-ttu-id="21367-177">เพื่อลบการแจ้งเตือน ให้เลือกถังขยะทางด้านขวาของชื่อการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="21367-177">To delete an alert, select the trashcan to the right of the alert name.</span></span>
   
      ![ไอคอนถังขยะถูกเลือก](media/end-user-alerts/power-bi-delete.png)

### <a name="from-the-power-bi-settings-menu"></a><span data-ttu-id="21367-179">จากเมนูการตั้งค่า Power BI</span><span class="sxs-lookup"><span data-stu-id="21367-179">From the Power BI settings menu</span></span>

1. <span data-ttu-id="21367-180">เลือกไอคอนรูปเฟืองจากแถบเมนู Power BI</span><span class="sxs-lookup"><span data-stu-id="21367-180">Select the gear icon from the Power BI menubar.</span></span>
   
    ![ไอคอนรูปเฟือง](media/end-user-alerts/power-bi-gear-icon.png)<span data-ttu-id="21367-182">.</span><span class="sxs-lookup"><span data-stu-id="21367-182">.</span></span>
2. <span data-ttu-id="21367-183">ภายใต้ **ตั้งค่า** ให้เลือก **การแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="21367-183">Under **Settings** select **Alerts**.</span></span>
   
    ![แท็บการแจ้งเตือนของหน้าต่างการตั้งค่า](media/end-user-alerts/power-bi-settings.png)
3. <span data-ttu-id="21367-185">จากที่นี่ คุณสามารถเปิดหรือปิดข้อความแจ้งเตือน เปิดตัว **จัดการการแจ้งเตือน** เพื่อทำการเปลี่ยนแปลง หรือลบการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="21367-185">From here you can turn alerts on and off, open the **Manage alerts** window to make changes, or delete the alert.</span></span>

## <a name="tips-and-troubleshooting"></a><span data-ttu-id="21367-186">เคล็ดลับและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="21367-186">Tips and troubleshooting</span></span> 

* <span data-ttu-id="21367-187">หากคุณไม่สามารถตั้งค่าการแจ้งเตือนสำหรับมาตรวัด KPI หรือการ์ดได้ โปรดติดต่อผู้ดูแลระบบ Powe BI หรือฝ่ายช่วยเหลือด้านไอทีเพื่อขอความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="21367-187">If you are unable to set an alert for a gauge, KPI, or card, contact your Power BI admin or IT help desk for help.</span></span> <span data-ttu-id="21367-188">บางครั้งการแจ้งเตือนจะถูกปิดหรือไม่พร้อมใช้งานสำหรับแดชบอร์ดของคุณหรือสำหรับไทล์แดชบอร์ดบางชนิด</span><span class="sxs-lookup"><span data-stu-id="21367-188">Sometimes alerts are turned off or unavailable for your dashboard or for specific types of dashboard tiles.</span></span>
* <span data-ttu-id="21367-189">ข้อความแจ้งเตือนทำงานกับข้อมูลที่ได้รับการรีเฟรชเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="21367-189">Alerts only work on data that is refreshed.</span></span> <span data-ttu-id="21367-190">การแจ้งเตือนจะไม่ทำงานกับข้อมูลแบบคงที่</span><span class="sxs-lookup"><span data-stu-id="21367-190">They do not work on static data.</span></span> <span data-ttu-id="21367-191">ส่วนใหญ่ของตัวอย่างที่ Microsoft กำหนดเป็นค่าคงที่</span><span class="sxs-lookup"><span data-stu-id="21367-191">Most of the samples supplied by Microsoft are static.</span></span> 
* <span data-ttu-id="21367-192">ความสามารถในการรับและดูเนื้อหาที่แชร์ต้องใช้สิทธิการใช้งาน Power BI Pro หรือ Premium</span><span class="sxs-lookup"><span data-stu-id="21367-192">The ability to receive and view shared content requires a Power BI Pro or Premium license.</span></span> <span data-ttu-id="21367-193">สำหรับข้อมูลเพิ่มเติม ให้อ่าน [ฉันมีสิทธิการใช้งานใดอยู่บ้าง](end-user-license.md)</span><span class="sxs-lookup"><span data-stu-id="21367-193">For more information, read [Which license do I have?](end-user-license.md).</span></span>
* <span data-ttu-id="21367-194">คุณสามารถตั้งค่าการแจ้งเตือนบนวิชวลที่สร้างขึ้นจากชุดข้อมูลการสตรีมที่คุณถูกปักหมุดจากรายงานไปยังแดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="21367-194">Alerts can be set on visuals created from streaming datasets that are pinned from a report to a dashboard.</span></span> <span data-ttu-id="21367-195">ไม่สามารถตั้งค่าการแจ้งเตือนบนไทล์การสตรีมที่สร้างขึ้นโดยตรงบนแดชบอร์ดโดยใช้ **เพิ่มไทล์** > **ข้อมูลการสตรีมแบบกำหนเอง**</span><span class="sxs-lookup"><span data-stu-id="21367-195">Alerts can't be set on streaming tiles created directly on the dashboard using **Add tile** > **Custom streaming data**.</span></span>


## <a name="clean-up-resources"></a><span data-ttu-id="21367-196">ล้างแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="21367-196">Clean up resources</span></span>
<span data-ttu-id="21367-197">คำแนะนำสำหรับการลบการแจ้งเตือนจะอธิบายไว้ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="21367-197">Instructions for deleting alerts are explained above.</span></span> <span data-ttu-id="21367-198">โดยย่อคือเลือกไอคอนรูปเฟืองจากแถบเมนู Power BI</span><span class="sxs-lookup"><span data-stu-id="21367-198">In brief, select the gear icon from the Power BI menubar.</span></span> <span data-ttu-id="21367-199">ภายใต้ **การตั้งค่า** เลือก **แจ้งเตือน** และลบการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="21367-199">Under **Settings** select **Alerts** and delete the alert.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="21367-200">ตั้งค่าการแจ้งเตือนข้อมูลบนอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="21367-200">Set data alerts on your mobile device</span></span>](mobile/mobile-set-data-alerts-in-the-mobile-apps.md)


