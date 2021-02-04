---
title: วิธีรีเฟรชข้อมูลประจำตัวของชุดเนื้อหา Xero
description: ถ้าคุณใช้ชุดเนื้อหา Xero Power BI คุณอาจพบปัญหาเกี่ยวกับการรีเฟรชชุดเนื้อหาประจำวัน เนื่องปัญหาบริการของ Power BI เมื่อไม่นานมานี้
author: paulinbar
ms.author: painbar
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 08/10/2017
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 972340d4c9cca4507308aaac4c07f410ff8fc6fe
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96392116"
---
# <a name="how-to-refresh-your-xero-content-pack-credentials-if-refresh-failed"></a><span data-ttu-id="cbda6-103">วิธีรีเฟรชข้อมูลประจำตัวของชุดเนื้อหา Xero ถ้าการรีเฟรชล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="cbda6-103">How to refresh your Xero content pack credentials if refresh failed</span></span>
<span data-ttu-id="cbda6-104">ถ้าคุณใช้ชุดเนื้อหา Xero Power BI คุณอาจพบปัญหาบางอย่าง กับการรีเฟรชชุดเนื้อหาประจำวัน เนื่องจากปัญหาบริการของ Power BI เมื่อไม่นานมานี้</span><span class="sxs-lookup"><span data-stu-id="cbda6-104">If you use the Xero Power BI content pack, you may have experienced some problems with the content pack’s daily refresh due to a recent Power BI service incident.</span></span>

<span data-ttu-id="cbda6-105">คุณสามารถดูว่าชุดเนื้อหาของคุณรีเฟรชสำเร็จหรือไม่ โดยการตรวจสอบสถานะการรีเฟรชล่าสุด สำหรับชุดข้อมูล Xero ของคุณ ดังแสดงในภาพหน้าจอด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="cbda6-105">You can see if your content pack refreshed successfully by checking the last refresh status for your Xero dataset as shown in the screenshot below.</span></span>

![ภาพหน้าจอของกล่องโต้ตอบ Xero ที่แสดงสถานะสำหรับชุดข้อมูล Xero ของคุณ](media/service-refresh-xero-credentials/powerbi-xero-refresh-failed.png)

<span data-ttu-id="cbda6-107">ถ้าคุณเห็นการรีเฟรชที่ล้มเหลวตามที่แสดงด้านบน โปรดทำตามขั้นตอนเหล่านี้ เพื่อต่ออายุข้อมูลประจำตัวชุดเนื้อหาของคุณ</span><span class="sxs-lookup"><span data-stu-id="cbda6-107">If you do see that refresh failed as shown above, please follow these steps to renew your content pack credentials.</span></span>

1. <span data-ttu-id="cbda6-108">คลิกที่ **ตัวเลือกเพิ่มเติม** (...) ซึ่งอยู่ถัดจากชุดข้อมูล Xero ของคุณ แล้วคลิก **กำหนดตารางเวลาการรีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="cbda6-108">Click **More options** (...) next to your Xero dataset, then click **Schedule refresh**.</span></span> <span data-ttu-id="cbda6-109">ซึ่งจะเปิดหน้าการตั้งค่า สำหรับชุดเนื้อหา Xero</span><span class="sxs-lookup"><span data-stu-id="cbda6-109">This opens the settings page for the Xero content pack.</span></span>
   
    ![ภาพหน้าจอของกล่องโต้ตอบ Xero ที่แสดงการเลือกกำหนดเวลาการรีเฟรช](media/service-refresh-xero-credentials/powerbi-xero-schedule-refresh.png)
2. <span data-ttu-id="cbda6-111">ในหน้า **ตั้งค่าสำหรับ Xero** เลือก **ข้อมูลประจำตัวแหล่งข้อมูล** > **แก้ไขข้อมูลประจำตัว**</span><span class="sxs-lookup"><span data-stu-id="cbda6-111">In the **Settings for Xero** page, select **Data source credentials** > **Edit credentials**.</span></span>
   
    ![ภาพหน้าจอของกล่องโต้ตอบการตั้งค่า Xero ที่แสดงการตั้งค่าสำหรับ Xero พร้อมด้วยการแก้ไขข้อมูลประจำตัวที่เลือกไว้](media/service-refresh-xero-credentials/powerbi-xero-settings-page.png)
3. <span data-ttu-id="cbda6-113">ใส่ชื่อองค์กรของคุณ > **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="cbda6-113">Enter your organization’s name > **Next**.</span></span>
   
    ![ภาพหน้าจอของกล่องโต้ตอบกำหนดค่า Xero ที่แสดงชื่อขององค์กร](media/service-refresh-xero-credentials/powerbi-xero-configure.png)
4. <span data-ttu-id="cbda6-115">ลงชื่อเข้าใช้ ด้วยบัญชี Xero ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cbda6-115">Sign in with your Xero account.</span></span>
   
    ![ภาพหน้าจอของกล่องโต้ตอบลงชื่อเข้าใช้ Xero ที่แสดงวิธีการลงชื่อเข้าใช้บัญชี Xero ของคุณ](media/service-refresh-xero-credentials/powerbi-xero-welcome.png)
5. <span data-ttu-id="cbda6-117">ตอนนี้ข้อมูลประจำตัวของคุณได้รับการปรับปรุงแล้ว ลองตรวจสอบว่า กำหนดเวลารีเฟรช ถูกตั้งค่าให้ทำงานทุกวัน</span><span class="sxs-lookup"><span data-stu-id="cbda6-117">Now that your credentials are updated, let’s make sure the refresh schedule is set to run daily.</span></span> <span data-ttu-id="cbda6-118">ตรวจสอบโดยคลิกที่ **ตัวเลือกเพิ่มเติม** (...) ซึ่งอยู่ถัดจากชุดข้อมูล Xero ของคุณ จาก นั้นคลิก **กำหนดตารางเวลาการรีเฟรช** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="cbda6-118">Check that by clicking **More options** (...) next to your Xero dataset, then clicking **Schedule refresh** again.</span></span>
   
    ![ภาพหน้าจอของกล่องโต้ตอบกำหนดเวลาการรีเฟรช ที่แสดงความถี่และโซนเวลาในการรีเฟรช](media/service-refresh-xero-credentials/powerbi-xero-refresh-schedule.png)
6. <span data-ttu-id="cbda6-120">คุณยังสามารถเลือกรีเฟรชชุดข้อมูลทันที</span><span class="sxs-lookup"><span data-stu-id="cbda6-120">You can also choose to refresh the dataset immediately.</span></span> <span data-ttu-id="cbda6-121">คลิกที่ **ตัวเลือกเพิ่มเติม** (...) ซึ่งอยู่ถัดจากชุดข้อมูล Xero ของคุณ แล้วคลิก **รีเฟรชทันที**</span><span class="sxs-lookup"><span data-stu-id="cbda6-121">Click **More options** (...) next to your Xero dataset, then click **Refresh now**.</span></span>
   
    ![ภาพหน้าจอของกล่องโต้ตอบ Xero ที่แสดงการเลือกรีเฟรชตอนนี้](media/service-refresh-xero-credentials/powerbi-xero-refresh-now.png)

<span data-ttu-id="cbda6-123">ถ้าคุณยังคงมีปัญหาการรีเฟรช โปรดอย่าลังเลที่จะติดต่อเราที่ [https://support.powerbi.com](https://support.powerbi.com)</span><span class="sxs-lookup"><span data-stu-id="cbda6-123">If you are still having refresh issues, please don’t hesitate to reach out to us at [https://support.powerbi.com](https://support.powerbi.com)</span></span> 

<span data-ttu-id="cbda6-124">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับชุดเนื้อหา Xero สำหรับ Power BI โปรดไป[หน้าความช่วยเหลือของชุดเนื้อหา Xero](service-connect-to-xero.md)</span><span class="sxs-lookup"><span data-stu-id="cbda6-124">To learn more about the Xero content pack for Power BI, please visit the [Xero content pack help page](service-connect-to-xero.md).</span></span>

### <a name="next-steps"></a><span data-ttu-id="cbda6-125">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="cbda6-125">Next steps</span></span>
* <span data-ttu-id="cbda6-126">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="cbda6-126">More questions?</span></span> [<span data-ttu-id="cbda6-127">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="cbda6-127">Try the Power BI Community</span></span>](https://community.powerbi.com/)

