---
title: กรองและแชร์รายงาน Power BI
description: เรียนรู้วิธีการกรองรายงาน Power BI และแชร์รายงานกับเพื่อนร่วมงานในองค์กรของคุณ
author: maggiesMSFT
ms.author: maggies
ms.reviewer: lukaszp
featuredvideoid: 0tUwn8DHo3s
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 01/29/2020
LocalizationGroup: Share your work
ms.openlocfilehash: 0e086b6ab5ce3411697607bfbda25bb0b82c6dca
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96406629"
---
# <a name="filter-and-share-a-power-bi-report"></a><span data-ttu-id="2656f-103">กรองและแชร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="2656f-103">Filter and share a Power BI report</span></span>
<span data-ttu-id="2656f-104">*แชร์* เป็นวิธีที่ดีเมื่อต้องให้บางคนสามารถเข้าถึงแดชบอร์ดและรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="2656f-104">*Sharing* is a good way to give a few people access to your dashboards and reports.</span></span> <span data-ttu-id="2656f-105">จะเกิดอะไรขึ้นถ้าคุณต้องการแชร์รายงานที่ถูกกรอง</span><span class="sxs-lookup"><span data-stu-id="2656f-105">What if you want to share a filtered version of a report?</span></span> <span data-ttu-id="2656f-106">คุณอาจต้องการให้รายงานแสดงเฉพาะข้อมูลสำหรับเมือง หรือพนักงานขาย หรือปีที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="2656f-106">Maybe you want the report to show only data for a specific city or salesperson or year.</span></span> <span data-ttu-id="2656f-107">บทความนี้อธิบายวิธีการกรองรายงานและการแชร์เวอร์ชันที่กรองแล้วของรายงาน</span><span class="sxs-lookup"><span data-stu-id="2656f-107">This article explains how to filter a report and share the filtered version of the report.</span></span> <span data-ttu-id="2656f-108">อีกวิธีหนึ่งในการแชร์รายงานที่กรองแล้วคือการ [เพิ่มพารามิเตอร์คิวรีไปยัง URL ของรายงาน](service-url-filters.md)</span><span class="sxs-lookup"><span data-stu-id="2656f-108">Another way to share a filtered report is to [add query parameters to the report URL](service-url-filters.md).</span></span> <span data-ttu-id="2656f-109">ในทั้งสองกรณี รายงานจะถูกกรองเมื่อผู้รับเปิดเป็นครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="2656f-109">In both cases, the report is filtered when recipients first open it.</span></span> <span data-ttu-id="2656f-110">พวกเขาสามารถล้างตัวเลือกตัวกรองในรายงานได้</span><span class="sxs-lookup"><span data-stu-id="2656f-110">They can clear the filter selections in the report.</span></span>

![กรองรายงานแล้ว](media/service-share-reports/power-bi-share-filter-pane-report.png)

<span data-ttu-id="2656f-112">Power BI ยังนำเสนอ[วิธีอื่นๆ เพื่อที่จะทำงานร่วมกันและเผยแพร่แดชบอร์ดและรายงาน](service-how-to-collaborate-distribute-dashboards-reports.md)</span><span class="sxs-lookup"><span data-stu-id="2656f-112">Power BI also offers [other ways to collaborate and distribute your reports](service-how-to-collaborate-distribute-dashboards-reports.md).</span></span> <span data-ttu-id="2656f-113">ด้วยการแชร์ คุณและผู้รับของคุณต้องมี[สิทธิ์การใช้งาน Power BI Pro](../fundamentals/service-features-license-type.md)หรือเนื้อหาจำเป็นต้องเป็นแบบ[ความจุพรีเมียม](../admin/service-premium-what-is.md)</span><span class="sxs-lookup"><span data-stu-id="2656f-113">With sharing, you and your recipients need a [Power BI Pro license](../fundamentals/service-features-license-type.md), or the content needs to be in a [Premium capacity](../admin/service-premium-what-is.md).</span></span> 

## <a name="follow-along-with-sample-data"></a><span data-ttu-id="2656f-114">ติดตามพร้อมด้วยข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="2656f-114">Follow along with sample data</span></span>

<span data-ttu-id="2656f-115">บทความนี้ใช้แอปแม่แบบตัวอย่างการตลาดและการขาย</span><span class="sxs-lookup"><span data-stu-id="2656f-115">This article uses the Marketing and Sales sample template app.</span></span> <span data-ttu-id="2656f-116">ต้องการลองใช้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="2656f-116">Want to try it?</span></span> 

1. <span data-ttu-id="2656f-117">ติดตั้ง [แอปแม่แบบตัวอย่างการตลาดและการขาย](https://appsource.microsoft.com/product/power-bi/microsoft-retail-analysis-sample.salesandmarketingsample?tab=Overview)</span><span class="sxs-lookup"><span data-stu-id="2656f-117">Install the [Marketing and Sales sample template app](https://appsource.microsoft.com/product/power-bi/microsoft-retail-analysis-sample.salesandmarketingsample?tab=Overview).</span></span>
2. <span data-ttu-id="2656f-118">เลือกแอปและเลือก **สำรวจแอป**</span><span class="sxs-lookup"><span data-stu-id="2656f-118">Select the app and select **Explore app**.</span></span>

   ![สำรวจข้อมูลตัวอย่าง](media/service-share-reports/power-bi-sample-explore-data.png)

3. <span data-ttu-id="2656f-120">เลือกไอคอนรูปดินสอเพื่อเปิดพื้นที่ทำงานที่คุณติดตั้งด้วยแอป</span><span class="sxs-lookup"><span data-stu-id="2656f-120">Select the pencil icon to open the workspace that you installed with the app.</span></span>

    ![ดินสอแก้ไขแอป](media/service-share-reports/power-bi-edit-pencil-app.png)

4. <span data-ttu-id="2656f-122">ในรายการเนื้อหาพื้นที่ทำงาน ให้เลือก **รายงาน** จากนั้นเลือกรายงาน **ตัวอย่าง PBIX การขายและการตลาด**</span><span class="sxs-lookup"><span data-stu-id="2656f-122">In the workspace content list, select **Reports**, then select the report **Sales and Marketing Sample PBIX**.</span></span>

    ![เปิดรายงานตัวอย่าง](media/service-share-reports/power-bi-open-sample-report.png)

    <span data-ttu-id="2656f-124">ในตอนนี้คุณก็พร้อมที่จะติดตามไปด้วยแล้ว</span><span class="sxs-lookup"><span data-stu-id="2656f-124">Now you're ready to follow along.</span></span>

## <a name="set-a-filter-in-the-report"></a><span data-ttu-id="2656f-125">ตั้งค่าตัวกรองในรายงาน</span><span class="sxs-lookup"><span data-stu-id="2656f-125">Set a filter in the report</span></span>

<span data-ttu-id="2656f-126">เปิดรายงานใน[มุมมองการแก้ไข](../consumer/end-user-reading-view.md)และใช้ตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="2656f-126">Open a report in [Editing view](../consumer/end-user-reading-view.md) and apply a filter.</span></span>

<span data-ttu-id="2656f-127">ในตัวอย่างนี้ เรากำลังกรองหน้าประเภท YTD ของแอปแม่แบบตัวอย่างการตลาดและการขายเพื่อแสดงเฉพาะค่าที่ **ภูมิภาค** นั้นคือ **ภาคกลาง**</span><span class="sxs-lookup"><span data-stu-id="2656f-127">In this example, we're filtering the YTD Category page of the Marketing and Sales sample template app to show only values where **Region** equals **Central**.</span></span> 
 
![บานหน้าต่างตัวกรองรายงาน](media/service-share-reports/power-bi-share-report-filter.png)

<span data-ttu-id="2656f-129">บันทึกรายงาน</span><span class="sxs-lookup"><span data-stu-id="2656f-129">Save the report.</span></span>

## <a name="share-the-filtered-report"></a><span data-ttu-id="2656f-130">แชร์รายงานี่กรองแล้ว</span><span class="sxs-lookup"><span data-stu-id="2656f-130">Share the filtered report</span></span>

1. <span data-ttu-id="2656f-131">เลือก **แชร์**</span><span class="sxs-lookup"><span data-stu-id="2656f-131">Select **Share**.</span></span>

   ![เลือก แชร์](media/service-share-reports/power-bi-share.png)

2. <span data-ttu-id="2656f-133">ล้าง **ส่งการแจ้งเตือนทางอีเมลไปยังผู้รับ** เพื่อที่คุณจะสามารถส่งการเชื่อมโยงที่ถูกกรองแล้วไปแทน เลือก **แชร์รายงานด้วยตัวกรองและตัวแบ่งส่วนข้อมูลปัจจุบัน** จากนั้นเลือก **แชร์**</span><span class="sxs-lookup"><span data-stu-id="2656f-133">Clear **Send email notification to recipients**, so you can send a filtered link instead, select **Share report with current filters and slicers**, then select **Share**.</span></span>

    ![แชร์รายงานด้วยตัวกรอง](media/service-share-reports/power-bi-share-with-filters.png)

4. <span data-ttu-id="2656f-135">เลือก **แชร์** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="2656f-135">Select **Share** again.</span></span>

   ![เลือก แชร์](media/service-share-reports/power-bi-share.png)

5. <span data-ttu-id="2656f-137">เลือกแท็บ **การเข้าถึง** จากนั้นเลือก **จัดการมุมมองรายงานที่แชร์**</span><span class="sxs-lookup"><span data-stu-id="2656f-137">Select the **Access** tab, then select **Manage shared report views**.</span></span>

    ![จัดการมุมมองรายงานที่แชร์](media/service-share-reports/power-bi-manage-shared-report-views.png)

6. <span data-ttu-id="2656f-139">คลิกขวาที่ URL ที่คุณต้องการ แล้วเลือก **คัดลอกลิงก์**</span><span class="sxs-lookup"><span data-stu-id="2656f-139">Right-click the URL you want, and select **Copy link**.</span></span>

    ![คัดลอกลิงก์ที่กรองแล้ว](media/service-share-reports/power-bi-copy-filtered-link.png)

7. <span data-ttu-id="2656f-141">เมื่อคุณแชร์ลิงก์นี้ ผู้รับจะเห็นรายงานที่กรองแล้วของคุณ</span><span class="sxs-lookup"><span data-stu-id="2656f-141">When you share this link, recipients will see your filtered report.</span></span> 

## <a name="limitations-and-considerations"></a><span data-ttu-id="2656f-142">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="2656f-142">Limitations and considerations</span></span>
<span data-ttu-id="2656f-143">สิ่งที่ควรทราบเกี่ยวกับการแชร์รายงาน:</span><span class="sxs-lookup"><span data-stu-id="2656f-143">Things to keep in mind about sharing reports:</span></span>

* <span data-ttu-id="2656f-144">เมื่อคุณแชร์ชุดข้อมูลโดยการจัดการสิทธิ์โดยการแชร์รายงานหรือแดชบอร์ดหรือโดยการเผยแพร่แอป คุณจะอนุญาตให้เข้าถึงชุดข้อมูลทั้งหมดยกเว้น [การรักษาความปลอดภัยระดับแถว (RLS)](../admin/service-admin-rls.md) จำกัดการเข้าถึงของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="2656f-144">When you share a dataset by managing permissions, by sharing reports or dashboards, or by publishing an app, you're granting access access to the entire dataset unless [row-level security (RLS)](../admin/service-admin-rls.md) limits their access.</span></span> <span data-ttu-id="2656f-145">ผู้เขียนรายงานอาจใช้ความสามารถที่กำหนดประสบการณ์ผู้ใช้เมื่อดูหรือโต้ตอบกับรายงาน เช่น การซ่อนคอลัมน์ การจำกัดการดำเนินงานในวิชวล และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="2656f-145">Report authors may use capabilities that customize user experiences when viewing or interacting with reports, for example hiding columns, limiting the actions on visuals, and others.</span></span> <span data-ttu-id="2656f-146">ประสบการณ์ผู้ใช้ที่กำหนดเองเหล่านี้ไม่จำกัดสิ่งที่ผู้ใช้สามารถเข้าถึงข้อมูลในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2656f-146">These customized user experience do not restrict what data users can access in the dataset.</span></span> <span data-ttu-id="2656f-147">ใช้ [การรักษาความปลอดภัยระดับแถว (RLS)](../admin/service-admin-rls.md) ในชุดข้อมูลเพื่อให้ข้อมูลประจำตัวของแต่ละบุคคลกำหนดว่าข้อมูลใดที่พวกเขาสามารถเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="2656f-147">Use [row-level security (RLS)](../admin/service-admin-rls.md) in the dataset so that each person's credentials determine which data they can access.</span></span>

## <a name="next-steps"></a><span data-ttu-id="2656f-148">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="2656f-148">Next steps</span></span>
* [<span data-ttu-id="2656f-149">วิธีการแชร์งานของคุณใน Power BI</span><span class="sxs-lookup"><span data-stu-id="2656f-149">Ways to share your work in Power BI</span></span>](service-how-to-collaborate-distribute-dashboards-reports.md)
* [<span data-ttu-id="2656f-150">แชร์แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="2656f-150">Share a dashboard</span></span>](service-share-dashboards.md)
* <span data-ttu-id="2656f-151">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="2656f-151">More questions?</span></span> <span data-ttu-id="2656f-152">[ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="2656f-152">[Try the Power BI Community](https://community.powerbi.com/).</span></span>
* <span data-ttu-id="2656f-153">มีคำติชมหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="2656f-153">Have feedback?</span></span> <span data-ttu-id="2656f-154">ไปที่[ไซต์ชุมชน Power BI](https://community.powerbi.com/) พร้อมกับคำแนะนำของคุณ</span><span class="sxs-lookup"><span data-stu-id="2656f-154">Go to the [Power BI Community site](https://community.powerbi.com/) with your suggestions.</span></span>
