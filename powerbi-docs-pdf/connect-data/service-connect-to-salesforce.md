---
title: เชื่อมต่อกับ Salesforce ด้วย Power BI
description: Salesforce สำหรับ Power BI
author: paulinbar
ms.author: painbar
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.subservice: powerbi-template-apps
ms.topic: how-to
ms.date: 05/30/2019
LocalizationGroup: Connect to services
ms.openlocfilehash: f43d60a22d436cc0be5aa57bc9b383d535dbfc0d
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96392898"
---
# <a name="connect-to-salesforce-with-power-bi"></a><span data-ttu-id="b9c5b-103">เชื่อมต่อกับ Salesforce ด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="b9c5b-103">Connect to Salesforce with Power BI</span></span>
<span data-ttu-id="b9c5b-104">ด้วย Power BI คุณสามารถเชื่อมต่อกับบัญชี Salesforce.com ของคุณได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="b9c5b-104">With Power BI, you can easily connect to your Salesforce.com account.</span></span> <span data-ttu-id="b9c5b-105">ด้วยการเชื่อมต่อนี้ คุณสามารถค้นคืนข้อมูล Salesforce ของคุณ และมีแดชบอร์ดและรายงานโดยอัตโนมัติที่ให้มา</span><span class="sxs-lookup"><span data-stu-id="b9c5b-105">With this connection, you can retrieve your Salesforce data and have a dashboard and reports automatically provided.</span></span>

<span data-ttu-id="b9c5b-106">อ่านเพิ่มเติมเกี่ยวกับ[การรวม Salesforce ](https://powerbi.microsoft.com/integrations/salesforce)ด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="b9c5b-106">Read more about the [Salesforce integration](https://powerbi.microsoft.com/integrations/salesforce) with Power BI.</span></span>

## <a name="how-to-connect"></a><span data-ttu-id="b9c5b-107">วิธีการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="b9c5b-107">How to connect</span></span>
1. <span data-ttu-id="b9c5b-108">ใน Power BI ให้เลือก **รับข้อมูล** ที่ด้านล่างของบานหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="b9c5b-108">In Power BI, select **Get Data** at the bottom of the nav pane.</span></span>
   
   ![ภาพหน้าจอของปุ่มรับข้อมูล ที่แสดงในบานหน้าต่างนำทาง](media/service-connect-to-salesforce/pbi_getdata.png) 
2. <span data-ttu-id="b9c5b-110">ในกล่อง **บริการ** เลือก **รับ**</span><span class="sxs-lookup"><span data-stu-id="b9c5b-110">In the **Services** box, select **Get**.</span></span>
   
   ![ภาพหน้าจอของกล่องโต้ตอบบริการ ที่แสดงปุ่มรับ](media/service-connect-to-salesforce/pbi_getservices.png) 
3. <span data-ttu-id="b9c5b-112">เลือก **วิเคราะห์สำหรับ Salesforce** และเลือก **รับ**</span><span class="sxs-lookup"><span data-stu-id="b9c5b-112">Select **Analytics for Salesforce** and select **Get**.</span></span>  
   
   ![ภาพหน้าจอของกล่องโต้ตอบการวิเคราะห์สำหรับ Salesforce ที่แสดงลิงก์รับทันที](media/service-connect-to-salesforce/salesforce.png)
4. <span data-ttu-id="b9c5b-114">เลือก **ลงชื่อเข้าใช้** เพื่อเริ่มการลงชื่อเข้าใช้ในโฟลว์</span><span class="sxs-lookup"><span data-stu-id="b9c5b-114">Select **Sign In** to start the sign in flow.</span></span>
   
    ![ภาพหน้าจอของกล่องโต้ตอบเชื่อมต่อกับ Salesforce ที่แสดงปุ่มลงชื่อเข้าใช้](media/service-connect-to-salesforce/dialog.png)
5. <span data-ttu-id="b9c5b-116">เมื่อมีข้อความถาม ให้ใส่ข้อมูลประจำตัวของ Salesforce</span><span class="sxs-lookup"><span data-stu-id="b9c5b-116">When prompted, enter your Salesforce credentials.</span></span> <span data-ttu-id="b9c5b-117">คลิก **อนุญาต** และอนุญาตให้ Power BI เข้าถึงข้อมูล Salesforce พื้นฐานและข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="b9c5b-117">Select **Allow** and let Power BI access your basic Salesforce information and data.</span></span>
   
   ![ภาพหน้าจอของข้อมูลประจำตัว Salesforce ที่แสดงว่า Power BI กำลังร้องขอสิทธิ์ในการเข้าถึงข้อมูลของคุณ](media/service-connect-to-salesforce/sf_authorize.png)
6. <span data-ttu-id="b9c5b-119">กำหนดค่าสิ่งที่คุณต้องการนำเข้าลงใน Power BI โดยใช้ตัวเลือกรายการเลือกแบบดึงลง</span><span class="sxs-lookup"><span data-stu-id="b9c5b-119">Configure what you'd like to import into Power BI using the drop-down option:</span></span>
   
   * <span data-ttu-id="b9c5b-120">**แดชบอร์ด**</span><span class="sxs-lookup"><span data-stu-id="b9c5b-120">**Dashboard**</span></span>
     
     <span data-ttu-id="b9c5b-121">เลือกแดชบอร์ดที่กำหนดไว้ล่วงหน้าโดยยึดตาม persona (เช่น **ผู้จัดการฝ่ายขาย**)</span><span class="sxs-lookup"><span data-stu-id="b9c5b-121">Select a predefined dashboard based on a persona (such as **Sales Manager**).</span></span> <span data-ttu-id="b9c5b-122">แดชบอร์ดเหล่านี้จะค้นคืนชุดข้อมูลมาตรฐานเฉพาะจาก Salesforce และจะไม่รวมเขตข้อมูลแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="b9c5b-122">These dashboards retrieve a specific set of Salesforce standard data, which doesn't include custom fields.</span></span>
     
     ![ภาพหน้าจอของแดชบอร์ด Salesforce ที่แสดงตัวเลือกเพื่อเลือกแดชบอร์ดที่กำหนดไว้ล่วงหน้าโดยยึดตามบุคคล](media/service-connect-to-salesforce/pbi_salesforcechooserole.png)
   * <span data-ttu-id="b9c5b-124">**รายงาน**</span><span class="sxs-lookup"><span data-stu-id="b9c5b-124">**Reports**</span></span>
     
     <span data-ttu-id="b9c5b-125">เลือกอย่างน้อยหนึ่งรายงานแบบกำหนดเองจากบัญชี Salesforce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="b9c5b-125">Select one or more custom reports from your Salesforce account.</span></span> <span data-ttu-id="b9c5b-126">รายงานเหล่านี้ตรงกับมุมมองของคุณใน Salesforce และสามารถรวมข้อมูลจากเขตข้อมูลแบบกำหนดเองหรือวัตถุ</span><span class="sxs-lookup"><span data-stu-id="b9c5b-126">These reports match your views in Salesforce and can include data from custom fields or objects.</span></span>
     
     ![ภาพหน้าจอของรายงาน Salesforce ที่แสดงรายการของรายงานแบบกำหนดเอง](media/service-connect-to-salesforce/pbi_salesforcereports.png)
     
     <span data-ttu-id="b9c5b-128">ถ้าคุณไม่เห็นรายงานใดๆ ให้เพิ่มหรือสร้าบัญชี Salesforce ของคุณ แล้วลองเชื่อมต่ออีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="b9c5b-128">If you don't see any reports, add or create them in your Salesforce account and try connecting again.</span></span>

7. <span data-ttu-id="b9c5b-129">คลิก **เชื่อมต่อ** เพื่อเริ่มกระบวนการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="b9c5b-129">Select **Connect** to begin the import process.</span></span> <span data-ttu-id="b9c5b-130">ในระหว่างการนำเข้า คุณเห็นการแจ้งเตือนที่แสดงว่าการนำเข้ากำลังดำเนินการอยู่</span><span class="sxs-lookup"><span data-stu-id="b9c5b-130">During the import, you see a notification showing the import is in progress.</span></span> <span data-ttu-id="b9c5b-131">เมื่อนำเข้าเสร็จสมบูรณ์ คุณจะเห็นแดชบอร์ด รายงาน และชุดข้อมูลสำหรับข้อมูล Salesforce ของคุณที่แสดงอยู่ในบานหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="b9c5b-131">When the import is complete, you see a dashboard, report, and dataset for your Salesforce data listed in the nav pane.</span></span>
   
   ![ภาพหน้าจอของแดชบอร์ดของผู้จัดการฝ่ายขาย ที่แสดงแดชบอร์ด รายงาน และชุดข้อมูล](media/service-connect-to-salesforce/pbi_getdatasalesforcedash.png)

<span data-ttu-id="b9c5b-133">คุณสามารถปรับเปลี่ยนแดชบอร์ดเพื่อแสดงข้อมูลของคุณด้วยวิธีที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="b9c5b-133">You can change the dashboard to display your data how you'd like.</span></span> <span data-ttu-id="b9c5b-134">คุณสามารถถามคำถาม Q&A หรือ [เลือกไทล์](../consumer/end-user-tiles.md) เพื่อเปิดรายงานด้านในและ[แก้ไข หรือลบไทล์ในแดชบอร์ดออก](../create-reports/service-dashboard-edit-tile.md)</span><span class="sxs-lookup"><span data-stu-id="b9c5b-134">You can ask questions with Q&A or [select a tile](../consumer/end-user-tiles.md) to open the underlying report and [edit or remove dashboard tiles](../create-reports/service-dashboard-edit-tile.md).</span></span>

<span data-ttu-id="b9c5b-135">**ฉันต้องทำอะไรตอนนี้**</span><span class="sxs-lookup"><span data-stu-id="b9c5b-135">**What now?**</span></span>

* <span data-ttu-id="b9c5b-136">ลอง[ถามคำถามในกล่อง Q&A](../consumer/end-user-q-and-a.md)ที่ด้านบนของแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="b9c5b-136">Try [asking a question in the Q&A box](../consumer/end-user-q-and-a.md) at the top of the dashboard</span></span>
* <span data-ttu-id="b9c5b-137">[แก้ไข หรือลบไทล์](../create-reports/service-dashboard-edit-tile.md)ในแดชบอร์ดออก</span><span class="sxs-lookup"><span data-stu-id="b9c5b-137">[Edit or remove a tile](../create-reports/service-dashboard-edit-tile.md) in the dashboard</span></span>
* <span data-ttu-id="b9c5b-138">[เลือกไทล์](../create-reports/service-dashboard-tiles.md)เพื่อเปิดรายงานด้านใน</span><span class="sxs-lookup"><span data-stu-id="b9c5b-138">[Select a tile](../create-reports/service-dashboard-tiles.md) to open the underlying report</span></span>
* <span data-ttu-id="b9c5b-139">แม้ว่าชุดข้อมูลของคุณถูกกำหนดให้รีเฟรชรายวัน แต่คุณสามารถปรับเปลี่ยนกำหนดการรีเฟรช หรือลองรีเฟรชตามความต้องการได้โดยใช้ **รีเฟรชตอนนี้**</span><span class="sxs-lookup"><span data-stu-id="b9c5b-139">While your dataset is scheduled to refresh daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**</span></span>

## <a name="system-requirements-and-considerations"></a><span data-ttu-id="b9c5b-140">ข้อกำหนดของระบบและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="b9c5b-140">System requirements and considerations</span></span>

- <span data-ttu-id="b9c5b-141">เชื่อมต่อกับบัญชีผลิตภัณฑ์ Salesforce ที่สามารถเข้าถึง API ที่เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="b9c5b-141">Connected with a production Salesforce account that has API access enabled</span></span>

- <span data-ttu-id="b9c5b-142">สิทธิที่มอบให้กับแอป Power BI ในระหว่างการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="b9c5b-142">Permission granted to the Power BI app during sign in</span></span>

- <span data-ttu-id="b9c5b-143">บัญชีมีการเรียกใช้ API เพียงพอที่สามารถใช้งานดึงและรีเฟรชข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9c5b-143">The account has sufficient API calls available to pull and refresh the data</span></span>

- <span data-ttu-id="b9c5b-144">โทเค็นรับรองตัวตนที่จำเป็นกับการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="b9c5b-144">A valid authentication token is required for refresh.</span></span> <span data-ttu-id="b9c5b-145">Salesforce มีขีดจำกัดของโทเค็นรับรองตัวตนห้าโทเค็นต่อแอปพลิเคชัน ดังนั้นเพื่อให้แน่ใจว่า คุณมีชุดข้อมูล Salesforce ที่นำเข้า 5 ชุดหรือน้อยกว่า</span><span class="sxs-lookup"><span data-stu-id="b9c5b-145">Salesforce has a limit of five authentication tokens per application so make sure you've five or less Salesforce data sets imported.</span></span>

- <span data-ttu-id="b9c5b-146">Salesforce Reports API มีข้อจำกัดที่สนับสนุนสูงสุด 2,000 แถวข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b9c5b-146">The Salesforce Reports API has a restriction that supports up to 2,000 rows of data.</span></span>


## <a name="troubleshooting"></a><span data-ttu-id="b9c5b-147">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="b9c5b-147">Troubleshooting</span></span>

<span data-ttu-id="b9c5b-148">ถ้าคุณพบข้อผิดพลาดใด ๆ โดยบังเอิญ ให้ตรวจสอบความต้องการด้านบน</span><span class="sxs-lookup"><span data-stu-id="b9c5b-148">If you come across any errors, review the requirements above.</span></span> 

<span data-ttu-id="b9c5b-149">ขณะนี้ยังไม่รองรับการลงชื่อเข้าใช้บนโดเมนระบบทดสอบหรือแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="b9c5b-149">Signing in to a custom or sandbox domain isn't currently supported.</span></span>

### <a name="unable-to-connect-to-the-remote-server-message"></a><span data-ttu-id="b9c5b-150">ข้อความ “ไม่สามารถเชื่อมต่อกับเซิร์ฟเวอร์ระยะไกลได้”</span><span class="sxs-lookup"><span data-stu-id="b9c5b-150">"Unable to connect to the remote server" message</span></span>

<span data-ttu-id="b9c5b-151">ถ้าคุณได้รับข้อความ "ไม่สามารถเชื่อมต่อกับเซิร์ฟเวอร์ระยะไกล" เมื่อพยายามเชื่อมต่อกับบัญชี Salesforce ของคุณ ให้ดูโซลูชันนี้บนฟอรั่มต่อไปนี้: [ข้อความข้อผิดพลาดการลงชื่อเข้าใช้ระบบตัวเชื่อมต่อ Salesforce: ไม่สามารถเชื่อมต่อกับเซิร์ฟเวอร์ระยะไกลได้](https://www.outsystems.com/forums/Forum_TopicView.aspx?TopicId=17674&TopicName=log-in-error-message-unable-to-connect-to-the-remote-server&)</span><span class="sxs-lookup"><span data-stu-id="b9c5b-151">If you get an "Unable to connect to the remote server" message when trying to connect to your Salesforce account, see this solution on the following forum: [Salesforce Connector sign in Error Message: Unable to connect to the remote server](https://www.outsystems.com/forums/Forum_TopicView.aspx?TopicId=17674&TopicName=log-in-error-message-unable-to-connect-to-the-remote-server&)</span></span>


## <a name="next-steps"></a><span data-ttu-id="b9c5b-152">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="b9c5b-152">Next steps</span></span>
[<span data-ttu-id="b9c5b-153">Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="b9c5b-153">What is Power BI?</span></span>](../fundamentals/power-bi-overview.md)

[<span data-ttu-id="b9c5b-154">แหล่งข้อมูลสำหรับบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="b9c5b-154">Data sources for the Power BI service</span></span>](service-get-data.md)
