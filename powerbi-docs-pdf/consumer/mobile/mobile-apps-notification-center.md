---
title: รับการแจ้งเตือนในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่
description: ศูนย์การแจ้งเตือนรวบรวมข้อมูล Power BI ของคุณที่เกี่ยวข้อง และส่งข้อมูลนั้นไปยังอุปกรณ์เคลื่อนที่ของคุณ
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 03/11/2020
ms.openlocfilehash: 19cda3734ba56a5879dc10041d2ba9e9bdc4146e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414748"
---
# <a name="get-notifications-in-the-power-bi-mobile-apps"></a><span data-ttu-id="4fa17-103">รับการแจ้งเตือนในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="4fa17-103">Get notifications in the Power BI mobile apps</span></span>
<span data-ttu-id="4fa17-104">นำไปใช้กับ:</span><span class="sxs-lookup"><span data-stu-id="4fa17-104">Applies to:</span></span>

| ![iPhone](./media/mobile-apps-notification-center/iphone-logo-50-px.png) | ![iPad](./media/mobile-apps-notification-center/ipad-logo-50-px.png) | ![โทรศัพท์ Android](./media/mobile-apps-notification-center/android-phone-logo-50-px.png) | ![แท็บเล็ต Android](./media/mobile-apps-notification-center/android-tablet-logo-50-px.png) | ![Windows 10](./media/mobile-apps-notification-center/win-10-logo-50-px.png) |
|:--- |:--- |:--- |:--- |:--- |
| <span data-ttu-id="4fa17-110">iPhone</span><span class="sxs-lookup"><span data-stu-id="4fa17-110">iPhones</span></span> |<span data-ttu-id="4fa17-111">iPad</span><span class="sxs-lookup"><span data-stu-id="4fa17-111">iPads</span></span> |<span data-ttu-id="4fa17-112">โทรศัพท์ Android</span><span class="sxs-lookup"><span data-stu-id="4fa17-112">Android phones</span></span> |<span data-ttu-id="4fa17-113">แท็บเล็ต Android</span><span class="sxs-lookup"><span data-stu-id="4fa17-113">Android tablets</span></span> |<span data-ttu-id="4fa17-114">อุปกรณ์ Windows 10</span><span class="sxs-lookup"><span data-stu-id="4fa17-114">Windows 10 devices</span></span> |

>[!NOTE]
><span data-ttu-id="4fa17-115">การสนับสนุนแอปอุปกรณ์เคลื่อนที่ Power BI สำหรับ **โทรศัพท์ที่ใช้ Windows 10 Mobile** จะถูกยกเลิกในวันที่ 16 มีนาคม 2021</span><span class="sxs-lookup"><span data-stu-id="4fa17-115">Power BI mobile app support for **phones using Windows 10 Mobile** will be discontinued on March 16, 2021.</span></span> [<span data-ttu-id="4fa17-116">ศึกษาเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4fa17-116">Learn more</span></span>](/legal/powerbi/powerbi-mobile/power-bi-mobile-app-end-of-support-for-windows-phones)

<span data-ttu-id="4fa17-117">การแจ้งเตือนจะนำข้อมูลที่เกี่ยวข้องกับประสบการณ์ Power BI ให้คุณ ในบริการของ Power BI หรือบนอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="4fa17-117">Notifications bring information related to your Power BI experience right to you, in the Power BI service or on your mobile device.</span></span> <span data-ttu-id="4fa17-118">เมื่อคุณเปิดการแจ้งเตือน คุณจะเห็นตัวดึงข้อมูลเรียงเป็นลำดับเกี่ยวกับ[การแจ้งเตือนที่คุณได้ตั้งค่า](mobile-set-data-alerts-in-the-mobile-apps.md)แดชบอร์ดใหม่ที่มีการแชร์กับคุณ การเปลี่ยนแปลงพื้นที่การทำงานกลุ่มของคุณ รายละเอียดเกี่ยวกับเหตุการณ์ใน Power BI และการประชุม และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="4fa17-118">When you open Notifications, you see a sequential feed of messages about [alerts you've set](mobile-set-data-alerts-in-the-mobile-apps.md), new dashboards that have been shared with you, changes to your group workspace, information about Power BI events and meetings, and more.</span></span>

> [!NOTE]
> <span data-ttu-id="4fa17-119">บนอุปกรณ์ iOS ในครั้งแรกที่คุณลงชื่อเข้าใช้[ปรับปรุงเวอร์ชันของแอป Power BI](https://powerbi.microsoft.com/mobile/)คุณจะเห็นข้อความถามว่า คุณต้องการให้ Power BI ส่งการแจ้งเตือนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4fa17-119">On an iOS device, the first time you sign in to the [updated version of the Power BI apps](https://powerbi.microsoft.com/mobile/), you see a message asking if you'd like Power BI to send notifications.</span></span> <span data-ttu-id="4fa17-120">คุณยังสามารถกำหนดวิธีที่ี Power BI จะแจ้งเตือนคุณใน **ตั้งค่า** สำหรับอุปกรณ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="4fa17-120">You can also configure how Power BI notifies you in **Settings** for your device.</span></span> 
> 
> 

## <a name="view-notifications-on-your-mobile-device"></a><span data-ttu-id="4fa17-121">ดูการแจ้งเตือนบนอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="4fa17-121">View notifications on your mobile device</span></span>
1. <span data-ttu-id="4fa17-122">เมื่อคุณได้รับการแจ้งเตือนบนอุปกรณ์เคลื่อนที่ ค่าเริ่มต้นจะทำให้ Power BI ส่งเสียงและแสดงแบนเนอร์การแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="4fa17-122">When you receive notifications on your mobile device, by default Power BI makes a sound and shows a notification banner.</span></span>
   
   ![แบนเนอร์การแจ้งเตือน](./media/mobile-apps-notification-center/power-bi-mobile-notification-banner.png)
   

   <span data-ttu-id="4fa17-124">คุณสามารถ[เปลี่ยนวิธีที่ Power BI จะแจ้งเตือนคุณ](mobile-apps-notification-center.md#change-or-turn-off-notifications-on-your-mobile-device)ได้</span><span class="sxs-lookup"><span data-stu-id="4fa17-124">You can [change how Power BI notifies you](mobile-apps-notification-center.md#change-or-turn-off-notifications-on-your-mobile-device).</span></span>
2. <span data-ttu-id="4fa17-125">ถ้าคุณได้รับการแจ้งเตือนแล้ว เมื่อคุณลงชื่อเข้าใช้ Power BI บนอุปกรณ์เคลื่อนที่ของคุณ คุณจะเห็นจุดสีเหลืองบนไอคอนระฆังการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="4fa17-125">If you've received notifications, when you sign in to Power BI on your mobile device you see a yellow dot on the notification bell icon</span></span> ![ระฆังการแจ้งเตือน](./media/mobile-apps-notification-center/powerbi-alert-tile-notification-icon.png) <span data-ttu-id="4fa17-127">(iOS และ Android) หรือบนปุ่มนำทางสากล</span><span class="sxs-lookup"><span data-stu-id="4fa17-127">(iOS and Android) or on the global navigation button</span></span> ![จุดการแจ้งเตือน](./media/mobile-apps-notification-center/power-bi-iphone-alert-global-nav-button.png) <span data-ttu-id="4fa17-129">(อุปกรณ์ Windows 10)</span><span class="sxs-lookup"><span data-stu-id="4fa17-129">(Windows 10 devices).</span></span> 

3. <span data-ttu-id="4fa17-130">หากต้องการดูการแจ้งเตือนในศูนย์การแจ้งเตือน ให้แตะระฆังการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="4fa17-130">To see notifications in the Notification center, tap the notifications bell</span></span> ![ระฆังการแจ้งเตือน](./media/mobile-apps-notification-center/powerbi-alert-tile-notification-icon.png) <span data-ttu-id="4fa17-132">(iOS และ Android) หรือไอคอนศูนย์การแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="4fa17-132">(iOS and Android) or the Notifications center icon</span></span> ![ไอคอนการแจ้งเตือน](./media/mobile-apps-notification-center/power-bi-windows-10-notification-icon.png) <span data-ttu-id="4fa17-134">(อุปกรณ์ Windows 10)</span><span class="sxs-lookup"><span data-stu-id="4fa17-134">(Windows 10 devices).</span></span>
   
    <span data-ttu-id="4fa17-135">การแจ้งเตือนจะแสดงรายการล่าสุดที่ด้านบนสุด รวมถึงไฮไลท์ข้อความที่ยังไม่ได้อ่าน</span><span class="sxs-lookup"><span data-stu-id="4fa17-135">Notifications are displayed with the most recent on top and unread messages highlighted.</span></span> <span data-ttu-id="4fa17-136">การแจ้งเตือนจะถูกเก็บไว้เป็น 90 วัน เว้นแต่ว่าคุณลบทิ้งเร็วกว่านั้น หรือเมื่อถึงขีดจำกัดสูงสุดที่ 100 การแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="4fa17-136">Notifications are retained for 90 days unless you delete them or reach the maximum limit of 100.</span></span>
   
   ![รายการการแจ้งเตือน iOS](./media/mobile-apps-notification-center/power-bi-iphone-notifications-list.png)
4. <span data-ttu-id="4fa17-138">หากต้องการยกเลิกการแจ้งเตือนบนอุปกรณ์ iOS และ Android ให้แตะค้างไว้แล้วปัดนิ้ว</span><span class="sxs-lookup"><span data-stu-id="4fa17-138">To dismiss a notification on iOS and Android devices, tap, hold, and swipe.</span></span> <span data-ttu-id="4fa17-139">บนอุปกรณ์ Windows 10 ให้คลิกขวาและเลือก **ปิดเสียงเตือน**</span><span class="sxs-lookup"><span data-stu-id="4fa17-139">On Windows 10 devices, right click and choose **Dismiss**.</span></span>

## <a name="change-or-turn-off-notifications-on-your-mobile-device"></a><span data-ttu-id="4fa17-140">เปลี่ยน หรือปิดการแจ้งเตือนบนอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="4fa17-140">Change or turn off notifications on your mobile device</span></span>
<span data-ttu-id="4fa17-141">คุณสามารถเปลี่ยนวิธีที่ Power BI แจ้งเตือนคุณได้</span><span class="sxs-lookup"><span data-stu-id="4fa17-141">You can change how Power BI notifies you.</span></span>

1. <span data-ttu-id="4fa17-142">บนอุปกรณ์ iOS ไปที่ **ตั้งค่า** > **การแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="4fa17-142">On an iOS device, go to **Settings** > **Notifications**.</span></span> 
   
    <span data-ttu-id="4fa17-143">บนโทรศัพท์ Android ไปที่ **ตั้งค่า** > **การแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="4fa17-143">On an Android phone, go to **Settings** > **Notifications**.</span></span>
   
    <span data-ttu-id="4fa17-144">บนอุปกรณ์ Windows ใน **ตั้งค่า** ไปยัง **ระบบ** > **การแจ้งเตือนและการดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="4fa17-144">On a Windows device, in **Settings** go to **System** > **Notifications & actions**.</span></span>
2. <span data-ttu-id="4fa17-145">ในรายการแอป เลือก **Power BI**</span><span class="sxs-lookup"><span data-stu-id="4fa17-145">In the list of apps, select **Power BI**.</span></span> 
3. <span data-ttu-id="4fa17-146">ที่นี่คุณสามารถปิดการแจ้งเตือนทั้งหมด หรือเลือกการแจ้งเตือนที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="4fa17-146">Here you can turn notifications off completely or choose which notifications you want.</span></span>
   
    <span data-ttu-id="4fa17-147">**บน iPhone**</span><span class="sxs-lookup"><span data-stu-id="4fa17-147">**On an iPhone**</span></span>
   
    ![สกรีนช็อตแสดงหน้าจอ iPhone ที่ชื่อว่า Power B I ที่คุณสามารถอนุญาตและจัดการการแจ้งเตือนได้](./media/mobile-apps-notification-center/power-bi-notifications-iphone-settings.png)
   
    <span data-ttu-id="4fa17-149">**บนโทรศัพท์ Android**</span><span class="sxs-lookup"><span data-stu-id="4fa17-149">**On an Android phone**</span></span>
   
    ![สกรีนช็อตแสดงหน้าจอ Android ที่ชื่อว่า Power B I ที่คุณสามารถอนุญาตและจัดการการแจ้งเตือนได้](./media/mobile-apps-notification-center/power-bi-notifications-android-settings.png)

    <span data-ttu-id="4fa17-151">**บนอุปกรณ์ Windows 10**</span><span class="sxs-lookup"><span data-stu-id="4fa17-151">**On a Windows 10 device**</span></span>

    ![สกรีนช็อตแสดงหน้าจออุปกรณ์ Windows 10 ที่คุณสามารถอนุญาตและจัดการการแจ้งเตือน Power B I ได้](./media/mobile-apps-notification-center/power-bi-notifications-windows10-settings.png)

## <a name="next-steps"></a><span data-ttu-id="4fa17-153">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="4fa17-153">Next steps</span></span>
* [<span data-ttu-id="4fa17-154">การแจ้งเตือนข้อมูลในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="4fa17-154">Data alerts in Power BI service</span></span>](../../create-reports/service-set-data-alerts.md)
* [<span data-ttu-id="4fa17-155">ตั้งค่าการแจ้งเตือนข้อมูลในแอปบน iPhone (Power BI สำหรับ iOS)</span><span class="sxs-lookup"><span data-stu-id="4fa17-155">Set data alerts in the iPhone app (Power BI for iOS)</span></span>](mobile-set-data-alerts-in-the-mobile-apps.md)
* [<span data-ttu-id="4fa17-156">ตั้งค่าการแจ้งเตือนข้อมูลในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่สำหรับ Windows 10</span><span class="sxs-lookup"><span data-stu-id="4fa17-156">Set data alerts in the Power BI mobile app for Windows 10</span></span>](mobile-set-data-alerts-in-the-mobile-apps.md)
* <span data-ttu-id="4fa17-157">[ดาวน์โหลดเวอร์ชันล่าสุดของแอป Power BI](https://powerbi.microsoft.com/mobile/)สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="4fa17-157">[Download the latest version of the Power BI apps](https://powerbi.microsoft.com/mobile/) for mobile devices</span></span>