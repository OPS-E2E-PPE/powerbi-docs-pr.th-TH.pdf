---
title: ตั้งค่าการแจ้งเตือนข้อมูลในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่
description: เรียนรู้วิธีการตั้งค่าการแจ้งเตือนในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่เพื่อแจ้งเตือนคุณเมื่อข้อมูลในแดชบอร์ดเปลี่ยนแปลงเกินขีดจำกัดที่คุณตั้งค่าไว้
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 12/11/2019
ms.openlocfilehash: 4e9820b8ebff411434d9d6c408f36a36a644ea9d
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418014"
---
# <a name="set-data-alerts-in-the-power-bi-mobile-apps"></a><span data-ttu-id="c53f2-103">ตั้งค่าการแจ้งเตือนข้อมูลในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="c53f2-103">Set data alerts in the Power BI mobile apps</span></span>
<span data-ttu-id="c53f2-104">นำไปใช้กับ:</span><span class="sxs-lookup"><span data-stu-id="c53f2-104">Applies to:</span></span>

| ![iPhone](./media/mobile-set-data-alerts-in-the-mobile-apps/iphone-logo-50-px.png) | ![iPad](./media/mobile-set-data-alerts-in-the-mobile-apps/ipad-logo-50-px.png) | ![โทรศัพท์ Android](./media/mobile-set-data-alerts-in-the-mobile-apps/android-phone-logo-50-px.png) | ![แท็บเล็ต Android](./media/mobile-set-data-alerts-in-the-mobile-apps/android-tablet-logo-50-px.png) | ![อุปกรณ์ Windows 10](./media/mobile-set-data-alerts-in-the-mobile-apps/win-10-logo-50-px.png) |
|:--- |:--- |:--- |:--- |:--- |
| <span data-ttu-id="c53f2-110">iPhone</span><span class="sxs-lookup"><span data-stu-id="c53f2-110">iPhones</span></span> |<span data-ttu-id="c53f2-111">iPad</span><span class="sxs-lookup"><span data-stu-id="c53f2-111">iPads</span></span> |<span data-ttu-id="c53f2-112">โทรศัพท์ Android</span><span class="sxs-lookup"><span data-stu-id="c53f2-112">Android phones</span></span> |<span data-ttu-id="c53f2-113">แท็บเล็ต Android</span><span class="sxs-lookup"><span data-stu-id="c53f2-113">Android tablets</span></span> |<span data-ttu-id="c53f2-114">อุปกรณ์ Windows 10</span><span class="sxs-lookup"><span data-stu-id="c53f2-114">Windows 10 devices</span></span> |

<span data-ttu-id="c53f2-115">คุณสามารถตั้งค่าการแจ้งเตือนบนแดชบอร์ดในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่และในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="c53f2-115">You can set alerts on dashboards in the Power BI mobile apps and in the Power BI service.</span></span> <span data-ttu-id="c53f2-116">ข้อความแจ้งเตือนจะเตือนคุณเมื่อมีการเปลี่ยนแปลงข้อมูลในไทล์เกินขีดจำกัดที่คุณตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="c53f2-116">Alerts notify you when data in a tile changes beyond limits you set.</span></span> <span data-ttu-id="c53f2-117">ข้อความแจ้งเตือนสำหรับไทล์ที่มีจำนวนเดียว เช่น บัตรและตัวประเมิน แต่ไม่มีข้อมูลการสตรีม</span><span class="sxs-lookup"><span data-stu-id="c53f2-117">Alerts work for tiles featuring a single number, such as cards and gauges, but not with streaming data.</span></span> <span data-ttu-id="c53f2-118">คุณสามารถตั้งค่าการแจ้งเตือนข้อมูลบนอุปกรณ์เคลื่อนที่ของคุณ และดูเอกสารเหล่านั้นในบริการของ Power BI และกลับกันได้</span><span class="sxs-lookup"><span data-stu-id="c53f2-118">You can set data alerts on your mobile device and see them in the Power BI service, and vice versa.</span></span> <span data-ttu-id="c53f2-119">มีเพียงคุณเท่านั้นที่สามารถดูการแจ้งเตือนข้อมูลที่คุณตั้งค่า แม้ว่าคุณแชร์แดชบอร์ดหรือสแนปช็อตของไทล์</span><span class="sxs-lookup"><span data-stu-id="c53f2-119">Only you can see the data alerts you set, even if you share a dashboard or a snapshot of a tile.</span></span>

<span data-ttu-id="c53f2-120">คุณสามารถกำหนดการแจ้งเตือนหากคุณมีสิทธิ์การใช้งาน Power BI Pro หรือหากแดชบอร์ดที่แชร์กันอยู่ในความจุแบบพรีเมี่ยม</span><span class="sxs-lookup"><span data-stu-id="c53f2-120">You can set alerts on tiles if you have a Power BI Pro license, or if the shared dashboard is in a Premium capacity.</span></span> 

> [!WARNING]
> <span data-ttu-id="c53f2-121">การแจ้งเตือนข้อมูลแสดงข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="c53f2-121">Data-driven alert notifications provide information about your data.</span></span> <span data-ttu-id="c53f2-122">ถ้าอุปกรณ์ของคุณถูกขโมย เราขอแนะนำให้ไปยังบริการของ Power BI เพื่อปิดกฎการแจ้งเตือนทั้งหมดที่อิงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c53f2-122">If your device gets stolen, we recommend going to the Power BI service to turn off all data-driven alert rules.</span></span> 
> 
> <span data-ttu-id="c53f2-123">เรียนรู้เพิ่มเติมเกี่ยวกับ[การจัดการการแจ้งเตือนข้อมูลในบริการของ Power BI](../../create-reports/service-set-data-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="c53f2-123">Learn more about [managing data alerts in the Power BI service](../../create-reports/service-set-data-alerts.md).</span></span>
> 
> 

## <a name="data-alerts-on-an-iphone-or-ipad"></a><span data-ttu-id="c53f2-124">การแจ้งเตือนข้อมูลบน iPhone หรือ iPad</span><span class="sxs-lookup"><span data-stu-id="c53f2-124">Data alerts on an iPhone or iPad</span></span>
### <a name="set-an-alert-on-an-iphone-or-ipad"></a><span data-ttu-id="c53f2-125">ตั้งค่าการแจ้งเตือนบน iPhone หรือ iPad</span><span class="sxs-lookup"><span data-stu-id="c53f2-125">Set an alert on an iPhone or iPad</span></span>
1. <span data-ttu-id="c53f2-126">แตะหมายเลขหรือไทล์ตัวประเมินในแดชบอร์ดเพื่อเปิดในโหมดโฟกัส</span><span class="sxs-lookup"><span data-stu-id="c53f2-126">Tap a number or gauge tile in a dashboard to open it in focus mode.</span></span>  
   
   ![ภาพหน้าจอของแดชบอร์ด ที่แสดงไทล์ตัววัดในโหมดโฟกัส](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-card-visual.png)
2. แตะไอคอน bell:::image type="icon" source="media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-alert-icon.png" border="false":::เพื่อเพิ่มข้อความแจ้งเตือน  
3. <span data-ttu-id="c53f2-129">แตะ **เพิ่มกฎการแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="c53f2-129">Tap **Add alert rule**.</span></span>
   
   ![ภาพหน้าจอของกฎการแจ้งเตือน ที่แสดงว่าไม่มีการตั้งค่าการแจ้งเตือน](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-add-alert-rule.png)
4. <span data-ttu-id="c53f2-131">เลือกรับการแจ้งเตือนที่มากหรือน้อยกว่าค่าหนึ่ง จากนั้นตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="c53f2-131">Choose to receive alerts above or below a value, then set the value.</span></span>
   
   ![ภาพหน้าจอของการตั้งค่าการแจ้งเตือน ที่แสดงชื่อการแจ้งเตือนและค่าที่จะตั้งค่า](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-set-alert-threshold.png)
5. <span data-ttu-id="c53f2-133">ตัดสินใจว่า จะรับการแจ้งเตือนเป็นรายชั่วโมงหรือรายวัน และเลือกว่าจะรับอีเมล์เมื่อคุณได้รับการแจ้งเตือนด้วยหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c53f2-133">Decide whether to receive hourly or daily alerts, and whether to also receive an email when you get the alert.</span></span>
   
   > [!NOTE]
   > <span data-ttu-id="c53f2-134">คุณไม่ได้รับข้อความแจ้งเตือนทุกชั่วโมงหรือทุกวันเว้นแต่ว่าข้อมูลมีการรีเฟรชจริงในเวลานั้น</span><span class="sxs-lookup"><span data-stu-id="c53f2-134">You don't receive alerts every hour or every day unless the data has actually refreshed in that time.</span></span>
   > 
   > 
6. <span data-ttu-id="c53f2-135">คุณสามารถเปลี่ยนชื่อเรื่องการแจ้งเตือนด้วย</span><span class="sxs-lookup"><span data-stu-id="c53f2-135">You can change the alert title, too.</span></span>
7. <span data-ttu-id="c53f2-136">แตะ **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c53f2-136">Tap **Save**.</span></span>
8. <span data-ttu-id="c53f2-137">ไทล์เดียวสามารถมีการแจ้งเตือนสำหรับค่าทั้งเหนือและต่ำกว่าค่าเกณฑ์</span><span class="sxs-lookup"><span data-stu-id="c53f2-137">A single tile can have alerts for values both above and below thresholds.</span></span> <span data-ttu-id="c53f2-138">ใน **จัดการการแจ้งเตือน** แตะ **เพิ่มกฎการแจ้งเตือน**</span><span class="sxs-lookup"><span data-stu-id="c53f2-138">In **Manage alerts**, tap **Add alert rule**.</span></span>
   
   ![ภาพหน้าจอของการจัดการการแจ้งเตือน ที่แสดงตัวชี้ไปยังการเพิ่มกฎการแจ้งเตือน](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-add-another-alert-rule.png)

### <a name="manage-alerts-on-your-iphone-or-ipad"></a><span data-ttu-id="c53f2-140">จัดการการแจ้งเตือนบน iPhone หรือ iPad ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c53f2-140">Manage alerts on your iPhone or iPad</span></span>
<span data-ttu-id="c53f2-141">คุณสามารถจัดการการแจ้งเตือนแต่ละรายการบนอุปกรณ์เคลื่อนที่ของคุณ หรือ[จัดการการแจ้งเตือนของคุณทั้งหมดในบริการของ Power BI](../../create-reports/service-set-data-alerts.md)ได้</span><span class="sxs-lookup"><span data-stu-id="c53f2-141">You can manage individual alerts on your mobile device or [manage all your alerts in the Power BI service](../../create-reports/service-set-data-alerts.md).</span></span>

1. <span data-ttu-id="c53f2-142">ในแดชบอร์ด แตะตัวเลขหรือไทล์ตัวประเมินที่มีข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="c53f2-142">In a dashboard, tap a number or gauge tile that has an alert.</span></span>  
   
   ![สกรีนช็อตของแดชบอร์ดบน iPhone หรือ iPad แสดงไทล์หมายเลขที่มีการแจ้งเตือน](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-card-visual_has_alert.png)

2. แตะไอคอน bell :::image type="icon" source="media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-has-alert-icon.png" border="false":::  
3. <span data-ttu-id="c53f2-145">แตะชื่อของการแจ้งเตือนเพื่อแก้ไข แตะตัวเลื่อนเพื่อปิดการแจ้งเตือนทางอีเมล์ หรือแตะถังขยะเพื่อลบการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="c53f2-145">Tap the name of the alert to edit it, tap the slider to turn off email alerts, or tap the garbage can to delete the alert.</span></span>
   
    ![ภาพหน้าจอของการแจ้งเตือน ที่ชี้ไปยังชื่อการแจ้งเตือน ถังขยะสำหรับการลบการแจ้งเตือน และแถบเลื่อนเพื่อปิดการแจ้งเตือน](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-edit-delete-alert.png)

## <a name="data-alerts-on-an-android-device"></a><span data-ttu-id="c53f2-147">การแจ้งเตือนข้อมูลบนอุปกรณ์ Android</span><span class="sxs-lookup"><span data-stu-id="c53f2-147">Data alerts on an Android device</span></span>
### <a name="set-an-alert-on-an-android-device"></a><span data-ttu-id="c53f2-148">ตั้งค่าการแจ้งเตือนบนอุปกรณ์ Android</span><span class="sxs-lookup"><span data-stu-id="c53f2-148">Set an alert on an Android device</span></span>
1. <span data-ttu-id="c53f2-149">ในแดชบอร์ด Power BI แตะตัวเลขหรือไทล์ตัวประเมินเพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="c53f2-149">In a Power BI dashboard, tap a number or gauge tile to open it.</span></span>  
2. แตะไอคอน bell:::image type="icon" source="media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-android-alert-icon.png" border="false":::เพื่อเพิ่มข้อความแจ้งเตือน  
   
   ![สกรีนช็อตของแดชบอร์ดบนอุปกรณ์ Android แสดงไทล์หมายเลขที่มีการแจ้งเตือน](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-android-tap-alert.png)
3. <span data-ttu-id="c53f2-152">แตะไอคอนเครื่องหมายบวก (+)</span><span class="sxs-lookup"><span data-stu-id="c53f2-152">Tap the plus icon (+).</span></span>
   
   ![ภาพหน้าจอของจัดการการแจ้งเตือน ที่แสดงตัวชี้ไปยังไอคอนเครื่องหมายบวก](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-android-plus-alert.png)
4. <span data-ttu-id="c53f2-154">เลือกเพื่อรับการแจ้งเตือนที่เหนือหรือต่ำกว่าค่าหนึ่ง และพิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c53f2-154">Choose to receive alerts above or below a value, and type the value.</span></span>
   
   ![ภาพหน้าจอของการตั้งค่าการแจ้งเตือน ที่แสดงตัวชี้ไปยังบันทึกและเสร็จสิ้น](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-android-tablet-set-alert-condition.png)
5. <span data-ttu-id="c53f2-156">แตะ **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="c53f2-156">Tap **Done**.</span></span>
6. <span data-ttu-id="c53f2-157">ตัดสินใจว่า จะรับการแจ้งเตือนเป็นรายชั่วโมงหรือรายวัน และเลือกว่าจะรับอีเมล์เมื่อคุณได้รับการแจ้งเตือนด้วยหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c53f2-157">Decide whether to receive hourly or daily alerts, and whether to also receive an email when you get the alert.</span></span>
   
   > [!NOTE]
   > <span data-ttu-id="c53f2-158">คุณไม่ได้รับข้อความแจ้งเตือนทุกชั่วโมงหรือทุกวันเว้นแต่ว่าข้อมูลมีการรีเฟรชจริงในเวลานั้น</span><span class="sxs-lookup"><span data-stu-id="c53f2-158">You don't receive alerts every hour or every day unless the data has actually refreshed in that time.</span></span>
   > 
   > 
7. <span data-ttu-id="c53f2-159">คุณสามารถเปลี่ยนชื่อเรื่องการแจ้งเตือนด้วย</span><span class="sxs-lookup"><span data-stu-id="c53f2-159">You can change the alert title, too.</span></span>
8. <span data-ttu-id="c53f2-160">แตะ **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c53f2-160">Tap **Save**.</span></span>

### <a name="manage-alerts-on-an-android-device"></a><span data-ttu-id="c53f2-161">จัดการการแจ้งเตือนบนอุปกรณ์ Android</span><span class="sxs-lookup"><span data-stu-id="c53f2-161">Manage alerts on an Android device</span></span>
<span data-ttu-id="c53f2-162">คุณสามารถจัดการการแจ้งเตือนแต่ละรายการในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่หรือ[จัดการการแจ้งเตือนของคุณทั้งหมดในบริการของ Power BI](../../create-reports/service-set-data-alerts.md) ได้</span><span class="sxs-lookup"><span data-stu-id="c53f2-162">You can manage individual alerts in the Power BI mobile app or [manage all your alerts in the Power BI service](../../create-reports/service-set-data-alerts.md).</span></span>

1. <span data-ttu-id="c53f2-163">ในแดชบอร์ด แตะตัวเลขหรือไทล์ตัวประเมินที่มีข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="c53f2-163">In a dashboard, tap a card or gauge tile that has an alert.</span></span>  
2. แตะไอคอน bell ทึบ:::image type="icon" source="media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-android-filled-alert-bell.png" border="false":::  
3. <span data-ttu-id="c53f2-165">แตะการแจ้งเตือนเพื่อเปลี่ยนแปลงค่า หรือปิดการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="c53f2-165">Tap the alert to change a value or turn it off.</span></span>
   
    ![ภาพหน้าจอของไทล์จัดการการแจ้งเตือน ที่แสดงไอคอนเครื่องหมายบวกสำหรับการเพิ่มการแจ้งเตือน](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-android-manage-alerts.png)
4. <span data-ttu-id="c53f2-167">แตะไอคอนเครื่องหมายบวก (+) เมื่อต้องเพิ่มการแจ้งเตือนอื่นให้ไทล์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="c53f2-167">Tap the plus icon (+) to add another alert to the same tile.</span></span>
5. <span data-ttu-id="c53f2-168">หากต้องลบการแจ้งเตือนทั้งหมด แตะไอคอนถังขยะ</span><span class="sxs-lookup"><span data-stu-id="c53f2-168">To delete the alert altogether, tap the garbage can icon</span></span> ![ไอคอนถังขยะ](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-android-delete-alert-icon.png)<span data-ttu-id="c53f2-170">.</span><span class="sxs-lookup"><span data-stu-id="c53f2-170">.</span></span>

## <a name="data-alerts-on-a-windows-device"></a><span data-ttu-id="c53f2-171">การแจ้งเตือนข้อมูลบนอุปกรณ์ Windows</span><span class="sxs-lookup"><span data-stu-id="c53f2-171">Data alerts on a Windows device</span></span>

>[!NOTE]
><span data-ttu-id="c53f2-172">การสนับสนุนแอปอุปกรณ์เคลื่อนที่ Power BI สำหรับ **โทรศัพท์ที่ใช้ Windows 10 Mobile** จะถูกยกเลิกในวันที่ 16 มีนาคม 2021</span><span class="sxs-lookup"><span data-stu-id="c53f2-172">Power BI mobile app support for **phones using Windows 10 Mobile** will be discontinued on March 16, 2021.</span></span> [<span data-ttu-id="c53f2-173">ศึกษาเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c53f2-173">Learn more</span></span>](/legal/powerbi/powerbi-mobile/power-bi-mobile-app-end-of-support-for-windows-phones)

### <a name="set-data-alerts-on-a-windows-device"></a><span data-ttu-id="c53f2-174">ตั้งค่าการแจ้งเตือนข้อมูลบนอุปกรณ์ Windows</span><span class="sxs-lookup"><span data-stu-id="c53f2-174">Set data alerts on a Windows device</span></span>
1. <span data-ttu-id="c53f2-175">แตะหมายเลขหรือไทล์ตัวประเมินในแดชบอร์ดเพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="c53f2-175">Tap a number or gauge tile in a dashboard to open it.</span></span>  
2. แตะไอคอน bell:::image type="icon" source="media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-windows-10-alert-bell-off.png" border="false":::เพื่อเพิ่มข้อความแจ้งเตือน  
   
   ![สกรีนช็อตของแดชบอร์ดบนอุปกรณ์ Windows แสดงไทล์หมายเลขที่มีการแจ้งเตือน](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-windows-10-tap-alert.png)
3. <span data-ttu-id="c53f2-178">แตะไอคอนเครื่องหมายบวก (+)</span><span class="sxs-lookup"><span data-stu-id="c53f2-178">Tap the plus icon (+).</span></span>
   
   ![ภาพหน้าจอของจัดการการแจ้งเตือน ที่แสดงว่าไม่มีการตั้งค่าการแจ้งเตือน](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-windows-10-no-alerts-yet.png)
4. <span data-ttu-id="c53f2-180">เลือกเพื่อรับการแจ้งเตือนที่เหนือหรือต่ำกว่าค่าหนึ่ง และพิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c53f2-180">Choose to receive alerts above or below a value, and type the value.</span></span>
   
   ![ภาพหน้าจอของการตั้งค่าการแจ้งเตือน ที่แสดงรายการต่าง ๆ เพื่อแก้ไขการแจ้งเตือน](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-windows-10-set-alert.png)
5. <span data-ttu-id="c53f2-182">ตัดสินใจว่า จะรับการแจ้งเตือนเป็นรายชั่วโมงหรือรายวัน และเลือกว่าจะรับอีเมล์เมื่อคุณได้รับการแจ้งเตือนด้วยหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c53f2-182">Decide whether to receive hourly or daily alerts, and whether to also receive an email when you get the alert.</span></span>
   
   > [!NOTE]
   > <span data-ttu-id="c53f2-183">คุณไม่ได้รับข้อความแจ้งเตือนทุกชั่วโมงหรือทุกวันเว้นแต่ว่าข้อมูลมีการรีเฟรชจริงในเวลานั้น</span><span class="sxs-lookup"><span data-stu-id="c53f2-183">You don't receive alerts every hour or every day unless the data has actually refreshed in that time.</span></span>
   > 
   > 
6. <span data-ttu-id="c53f2-184">คุณสามารถเปลี่ยนชื่อเรื่องการแจ้งเตือนด้วย</span><span class="sxs-lookup"><span data-stu-id="c53f2-184">You can change the alert title, too.</span></span>
7. <span data-ttu-id="c53f2-185">แตะตัวกาเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="c53f2-185">Tap the check mark.</span></span>
8. <span data-ttu-id="c53f2-186">ไทล์เดียวสามารถมีการแจ้งเตือนสำหรับค่าทั้งเหนือและต่ำกว่าค่าเกณฑ์</span><span class="sxs-lookup"><span data-stu-id="c53f2-186">A single tile can have alerts for values both above and below thresholds.</span></span> <span data-ttu-id="c53f2-187">ใน **จัดการการแจ้งเตือน** แตะเครื่องหมายบวก (+)</span><span class="sxs-lookup"><span data-stu-id="c53f2-187">In **Manage alerts**, tap the plus sign (+).</span></span>
   
   ![ภาพหน้าจอของจัดการการแจ้งเตือน ที่แสดงเครื่องหมายบวกสำหรับการเพิ่มการแจ้งเตือน](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-windows-10-add-another-alert.png)

### <a name="manage-alerts-on-a-windows-device"></a><span data-ttu-id="c53f2-189">จัดการการแจ้งเตือนบนอุปกรณ์ Windows</span><span class="sxs-lookup"><span data-stu-id="c53f2-189">Manage alerts on a Windows device</span></span>
<span data-ttu-id="c53f2-190">คุณสามารถจัดการการแจ้งเตือนแต่ละรายการในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่หรือ[จัดการการแจ้งเตือนของคุณทั้งหมดในบริการของ Power BI](../../create-reports/service-set-data-alerts.md) ได้</span><span class="sxs-lookup"><span data-stu-id="c53f2-190">You can manage individual alerts in the Power BI mobile app or [manage all your alerts in the Power BI service](../../create-reports/service-set-data-alerts.md).</span></span>

1. <span data-ttu-id="c53f2-191">ในแดชบอร์ด แตะตัวเลขหรือไทล์ตัวประเมินที่มีข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="c53f2-191">In a dashboard, tap a card or gauge tile that has an alert.</span></span>  
2. แตะไอคอน bell :::image type="icon" source="media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-windows-10-alert-bell-on.png" border="false":::  
   
   ![ภาพหน้าจอของแดชบอร์ด ที่แสดงไทล์ตัวเลขที่มีการแจ้งเตือน](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-windows-10-has-alerts.png)
3. <span data-ttu-id="c53f2-194">แตะการแจ้งเตือนเพื่อเปลี่ยนแปลงค่า หรือปิดการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="c53f2-194">Tap the alert to change a value or turn it off.</span></span>
   
    ![ภาพหน้าจอของจัดการการแจ้งเตือน ที่แสดงเครื่องหมายบวกสำหรับการเพิ่มการแจ้งเตือน](media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-windows-10-add-another-alert.png)
4. <span data-ttu-id="c53f2-196">เมื่อต้องลบการแจ้งเตือนทั้งหมด คลิกขวา หรือแตะ ค้าง > **ลบ**</span><span class="sxs-lookup"><span data-stu-id="c53f2-196">To delete the alert altogether, right-click or tap and hold > **Delete**.</span></span>

## <a name="receiving-alerts"></a><span data-ttu-id="c53f2-197">รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="c53f2-197">Receiving alerts</span></span>
<span data-ttu-id="c53f2-198">คุณจะได้รับข้อความแจ้งเตือนใน [ศูนย์การแจ้งเตือน](mobile-apps-notification-center.md)ของ Power BI บนอุปกรณ์เคลื่อนที่ของคุณ หรือ ในบริการของ Power BI พร้อมกับการแจ้งเตือนเกี่ยวกับแดชบอร์ดใหม่่มีคนแชร์กับคุณ</span><span class="sxs-lookup"><span data-stu-id="c53f2-198">You receive alerts in the Power BI [Notification Center](mobile-apps-notification-center.md) on your mobile device or in the Power BI service, along with notifications about new dashboards that someone has shared with you.</span></span>

<span data-ttu-id="c53f2-199">แหล่งข้อมูลจะถูกตั้งค่าการรีเฟรชรายวัน แม้ว่าบางแหล่งข้อมูลจะมีการรีเฟรชบ่อยกว่า</span><span class="sxs-lookup"><span data-stu-id="c53f2-199">Data sources are often set to refresh daily, although some refresh more often.</span></span> <span data-ttu-id="c53f2-200">เมื่อข้อมูลในแดชบอร์ดได้รับการรีเฟรช ถ้าข้อมูลที่มีการติดตามถึงค่าเกณฑ์หนึ่งใดที่คุณตั้ง หลายสิ่งที่จะเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="c53f2-200">When the data in the dashboard is refreshed, if the data being tracked reaches one of the thresholds you've set, several things will happen.</span></span>

1. <span data-ttu-id="c53f2-201">Power BI จะตรวจสอบเพื่อดูว่าเกินหนึ่งชั่วโมงหรือ 24 ชั่วโมงแล้วหรือไม่ (ขึ้นอยู่กับตัวเลือกที่คุณเลือก) นับตั้งแต่มีการส่งการแจ้งเตือนล่าสุด</span><span class="sxs-lookup"><span data-stu-id="c53f2-201">Power BI checks to see if it's been more than an hour or more than 24 hours (depending on the option you selected) since the last alert was sent.</span></span>
   
   <span data-ttu-id="c53f2-202">ตราบใดที่ข้อมูลเกินค่าเกณฑ์ คุณจะได้รับการแจ้งเตือนทุกชั่วโมงหรือทุกๆ 24 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="c53f2-202">As long as the data is past the threshold, you'll get an alert every hour or every 24 hours.</span></span>
2. <span data-ttu-id="c53f2-203">ถ้าคุณได้ตั้งค่าการแจ้งเตือนให้ส่งอีเมล์ คุณจะพบสิ่งที่เหมือนสิ่งนี้้ในกล่องอีเมลเข้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="c53f2-203">If you've set the alert to send you an email, you'll find something like this in your Inbox.</span></span>
   
   ![ภาพหน้าจอของการแจ้งเตือนทางอีเมล ที่แสดงการแจ้งเตือน](media/mobile-set-data-alerts-in-the-mobile-apps/powerbi-alerts-email.png)
3. Power BI จะเพิ่มข้อความใน [ศูนย์การแจ้งเตือน](mobile-apps-notification-center.md) ของคุณและเพิ่มจุดสีเหลืองที่ไอคอนกระดิ่ง :::image type="icon" source="media/mobile-set-data-alerts-in-the-mobile-apps/powerbi-alert-tile-notification-icon.png" border="false":::บนแถบชื่อเรื่อง (iOS และ Android) หรือไปที่ปุ่มการนำทางส่วนกลาง ![ปุ่มการนำทางส่วนกลาง](./media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-alert-global-nav-button.png) (อุปกรณ์ Windows 10)


4. แตะไอคอนกระดิ่ง :::image type="icon" source="media/mobile-set-data-alerts-in-the-mobile-apps/powerbi-alert-tile-notification-icon.png" border="false":::หรือปุ่มนำทางส่วนกลาง ![ปุ่มการนำทางส่วนกลาง](./media/mobile-set-data-alerts-in-the-mobile-apps/power-bi-iphone-alert-global-nav-button.png) เพื่อ [เปิด **ศูนย์การแจ้งเตือน** ของคุณ](mobile-apps-notification-center.md)และดูรายละเอียดการแจ้งเตือน
   
     

> [!NOTE]
> <span data-ttu-id="c53f2-207">ข้อความแจ้งเตือนทำงานกับข้อมูลที่ได้รับการรีเฟรชเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c53f2-207">Alerts only work on data that is refreshed.</span></span> <span data-ttu-id="c53f2-208">เมื่อมีการรีเฟรชข้อมูล Power BI จะค้นหาเพื่อดูว่าข้อความแจ้งเตือนถูกตั้งค่าสำหรับข้อมูลนั้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c53f2-208">When data refreshes, Power BI looks to see if an alert is set for that data.</span></span> <span data-ttu-id="c53f2-209">ถ้าข้อมูลได้ถึงค่าเกณฑ์การแจ้งเตือน ข้อความแจ้งเตือนจะถูกเริ่ม</span><span class="sxs-lookup"><span data-stu-id="c53f2-209">If the data has reached an alert threshold, an alert is triggered.</span></span>
> 
> 

## <a name="tips-and-troubleshooting"></a><span data-ttu-id="c53f2-210">เคล็ดลับและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="c53f2-210">Tips and troubleshooting</span></span>
* <span data-ttu-id="c53f2-211">ข้อความแจ้งเตือนในขณะนี้ไม่ได้สนับสนุนไทล์ Bing หรือไทล์การ์ด ที่มีหน่วยวัดวันที่/เวลา</span><span class="sxs-lookup"><span data-stu-id="c53f2-211">Alerts currently aren't supported for Bing tiles or card tiles with date/time measures.</span></span>
* <span data-ttu-id="c53f2-212">ข้อความแจ้งเตือนจะทำงานกับข้อมูลตัวเลขเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c53f2-212">Alerts only work with numeric data.</span></span>
* <span data-ttu-id="c53f2-213">ข้อความแจ้งเตือนทำงานกับข้อมูลที่ได้รับการรีเฟรชเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c53f2-213">Alerts only work on data that is refreshed.</span></span> <span data-ttu-id="c53f2-214">ข้อความแจ้งเตือนจะไม่ทำงานกับข้อมูลแบบคงที่</span><span class="sxs-lookup"><span data-stu-id="c53f2-214">They don't work on static data.</span></span>
* <span data-ttu-id="c53f2-215">ข้อความแจ้งเตือนจะไม่ทำงานกับไทล์ที่ประกอบด้วยข้อมูลสตรีม</span><span class="sxs-lookup"><span data-stu-id="c53f2-215">Alerts don't work with tiles that contain streaming data.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c53f2-216">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c53f2-216">Next steps</span></span>
* [<span data-ttu-id="c53f2-217">จัดการการแจ้งเตือนของคุณในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="c53f2-217">Manage your alerts in the Power BI service</span></span>](../../create-reports/service-set-data-alerts.md)
* [<span data-ttu-id="c53f2-218">ศูนย์การแจ้งเตือนอุปกรณ์เคลื่อนที่ power BI</span><span class="sxs-lookup"><span data-stu-id="c53f2-218">Power BI Mobile Notification Center</span></span>](mobile-apps-notification-center.md)
* <span data-ttu-id="c53f2-219">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="c53f2-219">Questions?</span></span> [<span data-ttu-id="c53f2-220">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="c53f2-220">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)