---
title: ตั้งค่าการแจ้งเตือนข้อมูลใน Power BI service
description: เรียนการตั้งค่าการแจ้งเตือน เมื่อมีข้อมูลในแดชบอร์ดของคุณเปลี่ยนเกินขีดจำกัดที่คุณตั้งไว้ใน Microsoft Power BI service
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: JbL2-HJ8clE
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 04/02/2020
LocalizationGroup: Dashboards
ms.openlocfilehash: cce9e351d468289b37f000159f846a5b2942b36a
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96387746"
---
# <a name="data-alerts-in-the-power-bi-service"></a><span data-ttu-id="56017-103">การแจ้งเตือนข้อมูลในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="56017-103">Data alerts in the Power BI service</span></span>

<span data-ttu-id="56017-104">ต้งค่าการแจ้งเตือน เมื่อมีข้อมูลในแดชบอร์ดของคุณเปลี่ยนเกินขีดจำกัดที่คุณตั้งไว</span><span class="sxs-lookup"><span data-stu-id="56017-104">Set alerts to notify you when data in your dashboards changes beyond limits you set.</span></span>

<span data-ttu-id="56017-105">คุณสามารถตั้งค่าการแจ้งเตือนบนตารางในพื้นที่ทำงานของฉันได้</span><span class="sxs-lookup"><span data-stu-id="56017-105">You can set alerts on tiles in your My Workspace.</span></span> <span data-ttu-id="56017-106">และคุณยังสามารถตั้งค่าการแจ้งเตือนถ้ามีคนแชร์แดชบอร์ดที่อยู่ใน[ความจุพรีเมียม](../admin/service-premium-what-is.md)ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="56017-106">You can also set alerts if someone shares a dashboard that's in a [Premium capacity](../admin/service-premium-what-is.md).</span></span> <span data-ttu-id="56017-107">คุณสามารถตั้งค่าการแจ้งเตือนบนตารางพื้นที่ทำงานอื่น ๆ ได้ด้วยเช่นกันหากคุณมีสิทธิ์การใช้งาน Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="56017-107">If you have a Power BI Pro license, you can set alerts on tiles in any other workspace, too.</span></span> <span data-ttu-id="56017-108">การแจ้งเตือนสามารถตั้งค่าบนหมุดไทล์ที่ปักหมุดจากวิชวลรายงานเท่านั้น และบนหน้าปัดวัด Kpi และการ์ดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="56017-108">Alerts can only be set on tiles pinned from report visuals, and only on gauges, KPIs, and cards.</span></span> <span data-ttu-id="56017-109">คุณสามารถตั้งค่าการแจ้งเตือนบนวิชวลที่สร้างขึ้นจากชุดข้อมูลการสตรีมที่คุณปักหมุดจากรายงานไปยังแดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="56017-109">Alerts can be set on visuals created from streaming datasets that you pin from a report to a dashboard.</span></span> <span data-ttu-id="56017-110">ไม่สามารถตั้งค่าการแจ้งเตือนบนไทล์การสตรีมที่สร้างขึ้นโดยตรงบนแดชบอร์ดโดยใช้ **เพิ่มไทล์** > **ข้อมูลการสตรีมแบบกำหนเอง**</span><span class="sxs-lookup"><span data-stu-id="56017-110">Alerts can't be set on streaming tiles created directly on the dashboard using **Add tile** > **Custom streaming data**.</span></span>

<span data-ttu-id="56017-111">มีเพียงคุณที่สามารถดูการแจ้งเตือนที่คุณตั้งไว้ แม้ว่าคุณได้แชร์แดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="56017-111">Only you can see the alerts you set, even if you share your dashboard.</span></span> <span data-ttu-id="56017-112">แม้แต่เจ้าของแดชบอร์ดก็มองไม่เห็นการแจ้งเตือนที่คุณตั้งไว้ในมุมมองแดชบอร์ดของพวกเขาได้</span><span class="sxs-lookup"><span data-stu-id="56017-112">Even the dashboard owner can't see alerts you set on your view of their dashboard.</span></span> <span data-ttu-id="56017-113">การแจ้งเตือนข้อมูลจะถูกซิงโครไนซ์เต็มรูปแบบข้ามแพลตฟอร์ม ตั้งค่าและดูการแจ้งเตือนข้อมูลได้[ในแอป mobile Power BI](../consumer/mobile/mobile-set-data-alerts-in-the-mobile-apps.md)และใน Power BI service</span><span class="sxs-lookup"><span data-stu-id="56017-113">Data alerts are fully synchronized across platforms; set and view data alerts [in the Power BI mobile apps](../consumer/mobile/mobile-set-data-alerts-in-the-mobile-apps.md) and in the Power BI service.</span></span> <span data-ttu-id="56017-114">ไม่สามารถใช้กับ Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="56017-114">They aren't available for Power BI Desktop.</span></span> <span data-ttu-id="56017-115">คุณสามารถทำให้เป็นอัตโนมัติและรวมการแจ้งเตือนด้วย Power Automate</span><span class="sxs-lookup"><span data-stu-id="56017-115">You can even automate and integrate alerts with Power Automate.</span></span> <span data-ttu-id="56017-116">คุณสามารถลองใช้งานด้วยตัวคุณเองในบทความ [Power Automate และ Power BI ](../collaborate-share/service-flow-integration.md)นี้ได้</span><span class="sxs-lookup"><span data-stu-id="56017-116">You can try it yourself in this [Power Automate and Power BI](../collaborate-share/service-flow-integration.md) article.</span></span>

![ไทล์](media/service-set-data-alerts/powerbi-alert-types-new.png)

> [!WARNING]
> <span data-ttu-id="56017-118">การแจ้งเตือนข้อมูลแสดงข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="56017-118">Data-driven alert notifications provide information about your data.</span></span> <span data-ttu-id="56017-119">ถ้าคุณดูข้อมูล Power BI ของคุณบนอุปกรณ์เคลื่อนที่ และอุปกรณ์ที่หายหรือถูกขโมย เราขอแนะนำให้ใช้บริการ Power BI เพื่อปิดการใช้งานแบบฎการแจ้งเตือนข้อมูลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="56017-119">If you view your Power BI data on a mobile device and that device is lost or stolen, we recommend using the Power BI service to turn off all data-driven alert rules.</span></span>

## <a name="set-data-alerts-in-the-power-bi-service"></a><span data-ttu-id="56017-120">ตั้งค่าการแจ้งเตือนข้อมูลใน Power BI service</span><span class="sxs-lookup"><span data-stu-id="56017-120">Set data alerts in the Power BI service</span></span>

<span data-ttu-id="56017-121">ดู Amanda เพิ่มการแจ้งเตือนบางอย่างไปยังไทล์บนแดชบอร์ดของเธอ</span><span class="sxs-lookup"><span data-stu-id="56017-121">Watch Amanda add some alerts to tiles on the dashboard.</span></span> <span data-ttu-id="56017-122">แล้วทำตามคำแนะนำทีละขั้นตอนด้านล่างวิดีโอเพื่อลองทำด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="56017-122">Then follow the step-by-step instructions below the video to try it out yourself.</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/JbL2-HJ8clE" frameborder="0" allowfullscreen></iframe>

<span data-ttu-id="56017-123">ตัวอย่างนี้ใช้การ์ดไทล์จากแดชบอร์ดตัวอย่างการวิเคราะห์ร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="56017-123">This example uses a card tile from the Retail Analysis sample dashboard.</span></span> <span data-ttu-id="56017-124">[รับตัวอย่างวิเคราะห์ร้านค้าปลีก](sample-retail-analysis.md#get-the-content-pack-for-this-sample)หากคุณต้องการติดตาม</span><span class="sxs-lookup"><span data-stu-id="56017-124">[Get the Retail Analysis sample](sample-retail-analysis.md#get-the-content-pack-for-this-sample) if you want to follow along.</span></span>

1. <span data-ttu-id="56017-125">เริ่มต้นกับแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="56017-125">Start on a dashboard.</span></span> <span data-ttu-id="56017-126">จากไทล์ **ร้านค้ารวม** เลือกจุดไข่ปลา</span><span class="sxs-lookup"><span data-stu-id="56017-126">From the **Total stores** tile, select the ellipses.</span></span>

   ![ไทล์ร้านค้าทั้งหมด](media/service-set-data-alerts/powerbi-card.png)

1. <span data-ttu-id="56017-128">เลือกไอคอนระฆัง![ไอคอนการแจ้งเตือน](media/service-set-data-alerts/power-bi-bell-icon.png)เพื่อเพิ่มการแจ้งเตือนอย่างน้อยหนึ่งตัวสำหรับ **ร้านค้ารวม**</span><span class="sxs-lookup"><span data-stu-id="56017-128">Select the bell icon ![Alert icon](media/service-set-data-alerts/power-bi-bell-icon.png) to add one or more alerts for **Total Stores**.</span></span>

1. <span data-ttu-id="56017-129">เมื่อต้องการเริ่มต้น ให้เลือก **+ เพิ่มกฎการแจ้งเตือน** ตรวจสอบให้แน่ใจว่าแถบเลื่อน **ใช้งานอยู่** ถูกตั้งค่าเป็น **เปิด** และตั้งชื่อให้การแจ้งเตือนของคุณ</span><span class="sxs-lookup"><span data-stu-id="56017-129">To start, select **+ Add alert rule**, ensure the **Active** slider is set to **On**, and give your alert a title.</span></span> <span data-ttu-id="56017-130">ชื่อช่วยให้คุณสามารถจดจำข้อความการแจ้งเตือนของคุณได้</span><span class="sxs-lookup"><span data-stu-id="56017-130">Titles help you easily recognize your alerts.</span></span>

   ![สกรีนช็อตแสดงหน้าต่างจัดการการแจ้งเตือนพร้อมด้วยเพิ่มกฎการแจ้งเตือน การแจ้งเตือนสำหรับร้านค้าทั้งหมด และชื่อเรื่องการแจ้งเตือนที่ถูกเรียกออกมา](media/service-set-data-alerts/powerbi-alert-title.png)

1. <span data-ttu-id="56017-132">เลื่อนลง แล้วใส่รายละเอียดการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="56017-132">Scroll down and enter the alert details.</span></span>  <span data-ttu-id="56017-133">ในตัวอย่างนี้ คุณสามารถสร้างการแจ้งเตือนที่แจ้งให้คุณทราบวันละครั้ง ถ้าหมายเลขของร้านค้ารวมมากกว่า 100 ร้าน</span><span class="sxs-lookup"><span data-stu-id="56017-133">In this example, you'll create an alert that notifies you once a day if the number of total stores goes above 100.</span></span>

   ![จัดการหน้าต่างข้อความแจ้งเตือน ตั้งค่าเกณฑ](media/service-set-data-alerts/power-bi-set-alert-details.png)

    <span data-ttu-id="56017-135">ข้อความแจ้งเตือนจะปรากฏใน **ศูนย์การแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="56017-135">Alerts appear in your **Notification center**.</span></span> <span data-ttu-id="56017-136">Power BI ยังส่งอีเมลถึงคุณเกี่ยวกับการแจ้งเตือนถ้าคุณเลือกกล่องกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="56017-136">Power BI also sends you an email about the alert, if you select the check box.</span></span>

1. <span data-ttu-id="56017-137">เลือก **บันทึกและปิด**</span><span class="sxs-lookup"><span data-stu-id="56017-137">Select **Save and close**.</span></span>

## <a name="receiving-alerts"></a><span data-ttu-id="56017-138">การรับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="56017-138">Receiving alerts</span></span>

<span data-ttu-id="56017-139">เมื่อข้อมูลที่ติดตามถึงหนึ่งในค่าเกณฑ์ที่คุณตั้งไว้ มีหลายสิ่งเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="56017-139">When the tracked data reaches one of the thresholds you've set, several things happen.</span></span> <span data-ttu-id="56017-140">ลำดับแรก Power BI จะตรวจสอบเพื่อดูว่าเกินหนึ่งชั่วโมงหรือ 24 ชั่วโมงแล้วหรือไม่ (ขึ้นอยู่กับตัวเลือกที่คุณเลือก) นับตั้งแต่มีการส่งการแจ้งเตือนล่าสุด</span><span class="sxs-lookup"><span data-stu-id="56017-140">First, Power BI checks to see if it's been more than an hour or more than 24 hours (depending on the option you selected) since the last alert.</span></span> <span data-ttu-id="56017-141">หากข้อมูลเกินค่าเกณฑ์ คุณจะได้รับการแจ้งเตือนทุกชั่วโมงหรือทุกๆ 24 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="56017-141">If the data is past the threshold, you'll get an alert.</span></span>

<span data-ttu-id="56017-142">ถัดไป Power BI ส่งข้อความแจ้งเตือนไปยัง **ศูนย์การแจ้งเตือน** และหรือในอีเมล</span><span class="sxs-lookup"><span data-stu-id="56017-142">Next, Power BI sends an alert to your **Notification center** and, optionally, an email.</span></span> <span data-ttu-id="56017-143">แต่ละข้อความแจ้งเตือนประกอบด้วยการเชื่อมโยงโดยตรงกับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="56017-143">Each alert contains a direct link to your data.</span></span> <span data-ttu-id="56017-144">เลือกลิงก์เพื่อดูไทล์เกี่ยวข้องที่คุณสามารถสำรวจ แชร์ และเรียนรู้เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="56017-144">Select the link to see the relevant tile where you can explore, share, and learn more.</span></span>  

* <span data-ttu-id="56017-145">ถ้าคุณได้ตั้งค่าการแจ้งเตือนให้ส่งอีเมล์ คุณจะพบสิ่งที่เหมือนสิ่งนี้้ในกล่องอีเมลเข้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="56017-145">If you've set the alert to send you an email, you'll find something like this in your Inbox.</span></span>

   ![อีเมลแจ้งเตือน](media/service-set-data-alerts/powerbi-alerts-email.png)

* <span data-ttu-id="56017-147">Power BI จะเพิ่มข้อความไปยัง **ศูนย์การแจ้งเตือน** ของคุณและเพิ่มไอคอนการแจ้งเตือนใหม่ใหักับไทล์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="56017-147">Power BI adds a message to your **Notification center** and adds a new alert icon to the applicable tile.</span></span>

   ![ไอคอนการแจ้งเตือนใน Power BI service](media/service-set-data-alerts/powerbi-alert-notifications.png)

* <span data-ttu-id="56017-149">**ศูนย์การแจ้งเตือน** จะแสดงรายละเอียดการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="56017-149">Your **Notification center** displays the alert details.</span></span>

    ![อ่านการแจ้งเตืิอน](media/service-set-data-alerts/powerbi-alert-notification.png)

   > [!NOTE]
   > <span data-ttu-id="56017-151">การแจ้งเตือนจะทำงานกับข้อมูลที่รีเฟรชเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="56017-151">Alerts only work on refreshed data.</span></span> <span data-ttu-id="56017-152">เมื่อมีการรีเฟรชข้อมูล Power BI จะค้นหาเพื่อดูว่าข้อความแจ้งเตือนถูกตั้งค่าสำหรับข้อมูลนั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="56017-152">When data refreshes, Power BI looks to see if an alert is set for that data.</span></span> <span data-ttu-id="56017-153">ถ้าข้อมูลได้ถึงค่าเกณฑ์การแจ้งเตือน Power BI จะทริกเกอร์การแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="56017-153">If the data has reached an alert threshold, Power BI triggers an alert.</span></span>

## <a name="managing-alerts"></a><span data-ttu-id="56017-154">การจัดการการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="56017-154">Managing alerts</span></span>

<span data-ttu-id="56017-155">มีหลายวิธีในการจัดการการแจ้งเตือนของคุณ:</span><span class="sxs-lookup"><span data-stu-id="56017-155">There are many ways to manage your alerts:</span></span>

* <span data-ttu-id="56017-156">จากไทล์แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="56017-156">From the dashboard tile.</span></span>

* <span data-ttu-id="56017-157">จากเมนูการตั้งค่า Power BI</span><span class="sxs-lookup"><span data-stu-id="56017-157">From the Power BI Settings menu.</span></span>

* <span data-ttu-id="56017-158">บนไทล์ใน[แอป Power BI สำหรับอุปกรณ์เคลื่อนที่](../consumer/mobile/mobile-set-data-alerts-in-the-mobile-apps.md)</span><span class="sxs-lookup"><span data-stu-id="56017-158">On a tile in the [Power BI mobile apps](../consumer/mobile/mobile-set-data-alerts-in-the-mobile-apps.md).</span></span>

### <a name="from-the-dashboard-tile"></a><span data-ttu-id="56017-159">จากไทล์แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="56017-159">From the dashboard tile</span></span>

1. <span data-ttu-id="56017-160">ถ้าคุณต้องการเปลี่ยนหรือลบการแจ้งเตือนสำหรับไทล์ ให้เปิดหน้าต่าง **จัดการการแจ้งเตือน** ใหม่อีกครั้ง โดยการเลือกไอคอนระฆัง ![ไอคอนการแจ้งเตือน](media/service-set-data-alerts/power-bi-bell-icon.png)</span><span class="sxs-lookup"><span data-stu-id="56017-160">If you need to change or remove an alert for a tile, reopen the **Manage alerts** window by selecting the bell icon ![Alert icon](media/service-set-data-alerts/power-bi-bell-icon.png).</span></span>

    <span data-ttu-id="56017-161">Power BI จะแสดงการแจ้งเตือนทั้งหมดที่คุณได้ตั้งค่าสำหรับไทล์</span><span class="sxs-lookup"><span data-stu-id="56017-161">Power BI displays the alert(s) that you've set for that tile.</span></span>

    ![สกรีนช็อตแสดงหน้าต่างจัดการการแจ้งเตือน](media/service-set-data-alerts/powerbi-see-alerts.png)

1. <span data-ttu-id="56017-163">เพื่อเปลี่ยนข้อความแจ้งเตือน ให้เลือกลูกศรทางด้านซ้ายของชื่อการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="56017-163">To modify an alert, select the arrow to the left of the alert name.</span></span>

    ![ลูกศรถัดจากชื่อการแจ้งเตือน](media/service-set-data-alerts/powerbi-see-alerts-arrow.png)

1. <span data-ttu-id="56017-165">เพื่อลบการแจ้งเตือน ให้เลือกถังขยะทางด้านขวาของชื่อการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="56017-165">To delete an alert, select the trashcan to the right of the alert name.</span></span>

      ![ไอคอนถังขยะถูกเลือก](media/service-set-data-alerts/powerbi-see-alerts-delete.png)

### <a name="from-the-power-bi-settings-menu"></a><span data-ttu-id="56017-167">จากเมนูการตั้งค่า Power BI</span><span class="sxs-lookup"><span data-stu-id="56017-167">From the Power BI settings menu</span></span>

1. <span data-ttu-id="56017-168">เลือกไอคอนรูปเฟืองจากแถบเมนู Power BI และเลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="56017-168">Select the gear icon from the Power BI menu bar and select **Settings**.</span></span>

    ![ไอคอนรูปเฟือง](media/service-set-data-alerts/powerbi-gear-icon.png)<span data-ttu-id="56017-170">.</span><span class="sxs-lookup"><span data-stu-id="56017-170">.</span></span>

1. <span data-ttu-id="56017-171">ภายใต้ **ตั้งค่า** ให้เลือก **การแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="56017-171">Under **Settings** select **Alerts**.</span></span>

    ![แท็บการแจ้งเตือนของหน้าต่างการตั้งค่า](media/service-set-data-alerts/powerbi-alert-settings.png)

1. <span data-ttu-id="56017-173">จากที่นี่ คุณสามารถเปิดหรือปิดข้อความแจ้งเตือน เปิดตัว **จัดการการแจ้งเตือน** เพื่อทำการเปลี่ยนแปลง หรือลบการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="56017-173">From here you can turn alerts on and off, open the **Manage alerts** window to make changes, or delete the alert.</span></span>

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="56017-174">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="56017-174">Considerations and troubleshooting</span></span>

* <span data-ttu-id="56017-175">การแจ้งเตือนไม่ได้สนับสนุนไทล์การ์ดที่มีหน่วยวัดวันที่/เวลา</span><span class="sxs-lookup"><span data-stu-id="56017-175">Alerts aren't supported for card tiles with date/time measures.</span></span>
* <span data-ttu-id="56017-176">การแจ้งเตือนจะทำงานกับข้อมูลตัวเลขเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="56017-176">Alerts only work with numeric data types.</span></span>
* <span data-ttu-id="56017-177">การแจ้งเตือนจะทำงานกับข้อมูลที่รีเฟรชเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="56017-177">Alerts only work on refreshed data.</span></span> <span data-ttu-id="56017-178">ข้อความแจ้งเตือนจะไม่ทำงานกับข้อมูลแบบคงที่</span><span class="sxs-lookup"><span data-stu-id="56017-178">They don't work on static data.</span></span>
* <span data-ttu-id="56017-179">การแจ้งเตือนจะทำงานกับชุดข้อมูลสตรีมมิ่งถ้าคุณสร้างวิชวลของรายงาน KPI, การ์ด หรือหน่วยวัด และปักหมุดวิชวลนั้นในแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="56017-179">Alerts only work on streaming datasets if you build a KPI, card, or gauge report visual and then pin that visual to the dashboard.</span></span>


## <a name="next-steps"></a><span data-ttu-id="56017-180">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="56017-180">Next steps</span></span>

* <span data-ttu-id="56017-181">[สร้าง Power Automate ที่มีการแจ้งเตือนข้อมูล](../collaborate-share/service-flow-integration.md)</span><span class="sxs-lookup"><span data-stu-id="56017-181">[Create a Power Automate that includes a data alert](../collaborate-share/service-flow-integration.md).</span></span>

* <span data-ttu-id="56017-182">[ตั้งค่าการแจ้งเตือนข้อมูลบนอุปกรณ์เคลื่อนที่ของคุณ](../consumer/mobile/mobile-set-data-alerts-in-the-mobile-apps.md)</span><span class="sxs-lookup"><span data-stu-id="56017-182">[Set data alerts on your mobile device](../consumer/mobile/mobile-set-data-alerts-in-the-mobile-apps.md).</span></span>

* [<span data-ttu-id="56017-183">Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="56017-183">What is Power BI?</span></span>](../fundamentals/power-bi-overview.md)

<span data-ttu-id="56017-184">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="56017-184">More questions?</span></span> [<span data-ttu-id="56017-185">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="56017-185">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
