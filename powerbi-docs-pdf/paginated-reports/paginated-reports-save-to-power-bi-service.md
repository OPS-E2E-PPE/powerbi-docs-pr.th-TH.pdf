---
title: เผยแพร่รายงานแบบแบ่งหน้าไปยังบริการของ Power BI
description: ในบทช่วยสอนนี้ คุณจะได้เรียนรู้วิธีการเผยแพร่รายงานแบบแบ่งหน้าไปยังบริการของ Power BI โดยการอัปโหลดจากคอมพิวเตอร์ของคุณเอง
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: report-builder
ms.topic: how-to
ms.date: 05/04/2020
ms.openlocfilehash: 28058161672de9db0cac5093e652e1d551f6a80a
ms.sourcegitcommit: ccf53e87ff7cba1fcd9d2cca761a561e62933f90
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/04/2020
ms.locfileid: "93297325"
---
# <a name="publish-a-paginated-report-to-the-power-bi-service"></a><span data-ttu-id="bcab5-103">เผยแพร่รายงานแบบแบ่งหน้าไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="bcab5-103">Publish a paginated report to the Power BI service</span></span>

<span data-ttu-id="bcab5-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span><span class="sxs-lookup"><span data-stu-id="bcab5-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span></span> 

<span data-ttu-id="bcab5-105">ในบทความนี้ คุณจะได้เรียนรู้เกี่ยวกับการเผยแพร่รายงานแบบแบ่งหน้าไปยังบริการของ Power BI โดยการอัปโหลดจากคอมพิวเตอร์ของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="bcab5-105">In this article, you learn about publishing a paginated report to the Power BI service by uploading it from your local computer.</span></span> <span data-ttu-id="bcab5-106">คุณสามารถอัปโหลดรายงานแบบแบ่งหน้าไปยัง "พื้นที่ทำงานของฉัน" หรือพื้นที่ทำงานอื่นได้ ตราบเท่าที่พื้นที่ทำงานนั้นอยู่ในความจุ Premium</span><span class="sxs-lookup"><span data-stu-id="bcab5-106">You can upload paginated reports to your My Workspace or any other workspace, as long as the workspace is in a Premium capacity.</span></span> <span data-ttu-id="bcab5-107">มองหาไอคอนรูปข้าวหลามตัด</span><span class="sxs-lookup"><span data-stu-id="bcab5-107">Look for the diamond icon</span></span> ![ไอคอนรูปข้าวหลามตัดของความจุ Power BI Premium](media/paginated-reports-save-to-power-bi-service/premium-diamond.png) <span data-ttu-id="bcab5-109">ถัดจากชื่อพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="bcab5-109">next to the workspace name.</span></span> 

<span data-ttu-id="bcab5-110">หากแหล่งข้อมูลของรายงานของคุณอยู่ในองค์กร คุณต้องสร้างเกตเวย์หลังจากที่อัปโหลดรายงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="bcab5-110">If your report data source is on premises, you need to create a gateway after you upload the report.</span></span> <span data-ttu-id="bcab5-111">ดูที่ส่วน [สร้างเกตเวย์](#create-a-gateway) ในภายหลังในบทความนี้</span><span class="sxs-lookup"><span data-stu-id="bcab5-111">See the [Create a gateway](#create-a-gateway) section later in this article.</span></span>

## <a name="add-a-workspace-to-a-premium-capacity"></a><span data-ttu-id="bcab5-112">เพิ่มพื้นที่ทำงานไปยังความจุพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="bcab5-112">Add a workspace to a Premium capacity</span></span>

<span data-ttu-id="bcab5-113">ถ้าพื้นที่ทำงานไม่มีไอคอนรูปข้าวหลามตัด</span><span class="sxs-lookup"><span data-stu-id="bcab5-113">If the workspace doesn't have the diamond icon</span></span> ![ไอคอนรูปข้าวหลามตัดของความจุ Power BI Premium](media/paginated-reports-save-to-power-bi-service/premium-diamond.png) <span data-ttu-id="bcab5-115">อยู่ถัดจากชื่อ คุณต้องเพิ่มพื้นที่ทำงานไปยังความจุพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="bcab5-115">next to the name, you need to add the workspace to a Premium capacity.</span></span> 

1. <span data-ttu-id="bcab5-116">เลือก **พื้นที่ทำงาน** เลือกจุดไข่ปลา ( **...** ) ที่อยู่ถัดจากชื่อของพื้นที่ทำงาน จากนั้นเลือก **แก้ไขพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="bcab5-116">Select **Workspaces** , select the ellipsis ( **...** ) next to the workspace name, then select **Edit workspace**.</span></span>

    ![เลือก แก้ไขพื้นที่ทำงาน](media/paginated-reports-save-to-power-bi-service/power-bi-paginated-edit-workspace.png)

1. <span data-ttu-id="bcab5-118">ในกล่องโต้ตอบ **แก้ไขพื้นที่ทำงาน** ให้คุณขยาย **ขั้นสูง** จากนั้นเลื่อน **ความจุเฉพาะ** ไปยัง **เปิด**</span><span class="sxs-lookup"><span data-stu-id="bcab5-118">In the **Edit workspace** dialog box, expand **Advanced** , then slide **Dedicated capacity** to **On**.</span></span>

    ![เลือกความจุเฉพาะ](media/paginated-reports-save-to-power-bi-service/power-bi-paginated-edit-workspace-dialog.png)

   <span data-ttu-id="bcab5-120">คุณอาจไม่สามารถเปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="bcab5-120">You may not be able to change it.</span></span> <span data-ttu-id="bcab5-121">ถ้าเปลี่ยนไม่ได้ โปรดติดต่อผู้ดูแลความจุ Power BI Premium เพื่อให้สิทธิ์ในการกำหนดกับคุณ เพื่อเพิ่มพื้นที่ทำงานไปยังความจุพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="bcab5-121">If not, then contact your Power BI Premium capacity admin to give you assignment rights to add your workspace to a Premium capacity.</span></span>

## <a name="from-report-builder-publish-a-paginated-report"></a><span data-ttu-id="bcab5-122">จากตัวสร้างรายงาน เผยแพร่รายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="bcab5-122">From Report Builder, publish a paginated report</span></span>

1. <span data-ttu-id="bcab5-123">สร้างรายงานแบบแบ่งหน้าในตัวสร้างรายงานและบันทึกลงคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="bcab5-123">Create your paginated report in Report Builder and save it to your local computer.</span></span>

1. <span data-ttu-id="bcab5-124">บนเมนู **ไฟล์** ของตัวสร้างรายงาน เลือก **บันทึกเป็น**</span><span class="sxs-lookup"><span data-stu-id="bcab5-124">On the Report Builder **File** menu, select **Save as**.</span></span>

    ![เมนู ไฟล์ > บันทึก > บันทึกเป็น](media/paginated-reports-save-to-power-bi-service/power-bi-paginated-save-as.png)

    <span data-ttu-id="bcab5-126">ถ้าคุณยังไม่ได้ลงชื่อเข้าใช้ Power BI คุณจำเป็นต้องลงชื่อเข้าใช้หรือสร้างบัญชีตอนนี้</span><span class="sxs-lookup"><span data-stu-id="bcab5-126">If you aren't signed in to Power BI yet, you need to sign in or create an account now.</span></span> <span data-ttu-id="bcab5-127">ในมุมขวาบนของตัวสร้างรายงาน เลือก **ลงชื่อเข้าใช้** และดำเนินการตามขั้นตอนให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bcab5-127">In the upper-right corner of Report Builder, select **Sign in** and complete the steps.</span></span>

2. <span data-ttu-id="bcab5-128">ในรายการของพื้นที่ทำงานทางด้านซ้าย ให้เลือกพื้นที่ทำงานที่มีไอคอนรูปเพชร ![ไอคอนรูปเพชรความจุของ Power BI Premium](media/paginated-reports-save-to-power-bi-service/premium-diamond.png) ที่อยู่ถัดจากชื่อ</span><span class="sxs-lookup"><span data-stu-id="bcab5-128">In the list of workspaces on the left, select a workspace with the diamond icon ![Power BI Premium capacity diamond icon](media/paginated-reports-save-to-power-bi-service/premium-diamond.png) next to its name.</span></span> <span data-ttu-id="bcab5-129">พิมพ์ **ชื่อไฟล์** ในกล่อง > **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="bcab5-129">Type a **File name** in the box > **Save**.</span></span> 

    ![เลือกพื้นที่ทำงานแบบ Premium](media/paginated-reports-save-to-power-bi-service/power-bi-paginated-select-workspace.png)

4. <span data-ttu-id="bcab5-131">เปิดบริการของ Power BI ในเบราว์เซอร์และเรียกดูไปที่พื้นที่ทำงานแบบ Premium ซึ่งคุณสามารถเผยแพร่รายงานที่มีการแบ่งหน้าได้</span><span class="sxs-lookup"><span data-stu-id="bcab5-131">Open the Power BI service in a browser and browse to the Premium workspace where you published the paginated report.</span></span> <span data-ttu-id="bcab5-132">บนแท็บ **รายงาน** คุณจะมองเห็นรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="bcab5-132">On the **Reports** tab, you see your report.</span></span>

    ![รายงานแบบแบ่งหน้าในรายการรายงาน](media/paginated-reports-save-to-power-bi-service/power-bi-paginated-wwi-report.png)

5. <span data-ttu-id="bcab5-134">เลือกรายงานที่มีการแบ่งหน้าเพื่อเปิดในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="bcab5-134">Select the paginated report to open it in the Power BI service.</span></span> <span data-ttu-id="bcab5-135">ถ้ามีพารามิเตอร์ คุณต้องเลือกก่อนที่คุณจะสามารถดูรายงานได้</span><span class="sxs-lookup"><span data-stu-id="bcab5-135">If it has parameters, you need to select them before you can view the report.</span></span>

    ![เลือกพารามิเตอร์](media/paginated-reports-save-to-power-bi-service/power-bi-paginated-select-parameters.png)

6. <span data-ttu-id="bcab5-137">หากแหล่งข้อมูลรายงานของคุณอยู่ภายในองค์กร ให้อ่านเกี่ยวกับวิธีการ[สร้างเกตเวย์](#create-a-gateway)ในบทความนี้ เพื่อเข้าถึงแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bcab5-137">If your report data source is on premises, read about how to [create a gateway](#create-a-gateway) in this article to access the data source.</span></span>

## <a name="from-the-power-bi-service-upload-a-paginated-report"></a><span data-ttu-id="bcab5-138">จากบริการของ Power BI อัปโหลดรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="bcab5-138">From the Power BI service, upload a paginated report</span></span>

<span data-ttu-id="bcab5-139">นอกจากนี้ คุณยังสามารถเริ่มต้นจากบริการของ Power BI และอัปโหลดรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="bcab5-139">You can also start from the Power BI service and upload a paginated report.</span></span>

1. <span data-ttu-id="bcab5-140">สร้างรายงานแบบแบ่งหน้าในตัวสร้างรายงานและบันทึกลงคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="bcab5-140">Create your paginated report in Report Builder and save it to your local computer.</span></span>

1. <span data-ttu-id="bcab5-141">เปิดบริการของ Power BI ในเบราเซอร์และเรียกดูพื้นที่ทำงาน Premium ที่คุณต้องการเผยแพร่รายงาน</span><span class="sxs-lookup"><span data-stu-id="bcab5-141">Open the Power BI service in a browser and browse to the Premium workspace where you want to publish the report.</span></span> <span data-ttu-id="bcab5-142">มองหาไอคอนรูปข้าวหลามตัด</span><span class="sxs-lookup"><span data-stu-id="bcab5-142">Note the diamond icon</span></span> ![ไอคอนรูปข้าวหลามตัดของความจุ Power BI Premium](media/paginated-reports-save-to-power-bi-service/premium-diamond.png) <span data-ttu-id="bcab5-144">ที่อยู่ถัดจากชื่อ</span><span class="sxs-lookup"><span data-stu-id="bcab5-144">next to the name.</span></span> 

1. <span data-ttu-id="bcab5-145">เลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="bcab5-145">Select **Get Data**.</span></span>

    ![รับข้อมูลด้วย Power BI](media/paginated-reports-save-to-power-bi-service/power-bi-paginated-get-data.png)

1. <span data-ttu-id="bcab5-147">ในกล่อง **ไฟล์** เลือก **รับ**</span><span class="sxs-lookup"><span data-stu-id="bcab5-147">In the **Files** box, select **Get**.</span></span>

    ![การรับไฟล์ของ Power BI](media/paginated-reports-save-to-power-bi-service/power-bi-paginated-files-get.png)

1. <span data-ttu-id="bcab5-149">เลือก **ไฟล์ภายในเครื่อง** > เรียกดูรายงานแบบแบ่งหน้า > **เปิด**</span><span class="sxs-lookup"><span data-stu-id="bcab5-149">Select **Local file** > browse to the paginated report > **Open**.</span></span>

    ![เลือกไฟล์ภายในเครื่อง](media/paginated-reports-save-to-power-bi-service/power-bi-paginated-local-file.png)

1. <span data-ttu-id="bcab5-151">เลือก **ดำเนินการต่อ** > **แก้ไขข้อมูลประจำตัว**</span><span class="sxs-lookup"><span data-stu-id="bcab5-151">Select **Continue** > **Edit credentials**.</span></span>

    ![เลือกแก้ไขข้อมูลประจำตัว](media/paginated-reports-save-to-power-bi-service/power-bi-paginated-select-edit-credentials.png)

1. <span data-ttu-id="bcab5-153">กำหนดข้อมูลประจำตัว > **ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="bcab5-153">Configure your credentials > **Sign in**.</span></span>

    ![แก้ไขข้อมูลประจำตัว](media/paginated-reports-save-to-power-bi-service/power-bi-paginated-credentials.png)

   <span data-ttu-id="bcab5-155">บนแท็บ **รายงาน** คุณจะมองเห็นรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="bcab5-155">On the **Reports** tab, you see your report.</span></span>

    ![รายงานแบบแบ่งหน้าในรายการรายงาน](media/paginated-reports-save-to-power-bi-service/power-bi-paginated-wwi-report.png)

1. <span data-ttu-id="bcab5-157">เลือกเพื่อเปิดในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="bcab5-157">Select it to open it in the Power BI service.</span></span> <span data-ttu-id="bcab5-158">ถ้ามีพารามิเตอร์ คุณต้องเลือกก่อนที่คุณจะสามารถดูรายงานได้</span><span class="sxs-lookup"><span data-stu-id="bcab5-158">If it has parameters, you need to select them before you can view the report.</span></span>
 
    ![เลือกพารามิเตอร์](media/paginated-reports-save-to-power-bi-service/power-bi-paginated-select-parameters.png)

6. <span data-ttu-id="bcab5-160">หากแหล่งข้อมูลรายงานของคุณอยู่ภายในองค์กร ให้อ่านเกี่ยวกับวิธีการ[สร้างเกตเวย์](#create-a-gateway)ในบทความนี้ เพื่อเข้าถึงแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bcab5-160">If your report data source is on premises, read about how to [create a gateway](#create-a-gateway) in this article to access the data source.</span></span>

## <a name="create-a-gateway"></a><span data-ttu-id="bcab5-161">สร้างเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="bcab5-161">Create a gateway</span></span>

<span data-ttu-id="bcab5-162">เช่นเดียวกันกับรายงาน Power BI อื่นๆ หากแหล่งข้อมูลของรายงานอยู่ในองค์กร คุณต้องสร้างหรือเชื่อมต่อเกตเวย์เพื่อเข้าถึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bcab5-162">Just like any other Power BI report, if the report data source is on premises, then you need to create or connect to a gateway to access the data.</span></span>

1. <span data-ttu-id="bcab5-163">ที่ถัดจากชื่อรายงาน ให้คุณเลือก **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="bcab5-163">Next to the report name, select **Manage**.</span></span>

   ![จัดการรายงานแบบแบ่งหน้า](media/paginated-reports-save-to-power-bi-service/power-bi-paginated-manage.png)

1. <span data-ttu-id="bcab5-165">ดูบทความบริการของ Power BI [เกตเวย์ข้อมูลภายในองค์กรคืออะไร](../connect-data/service-gateway-onprem.md) สำหรับรายละเอียดและขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="bcab5-165">See the Power BI service article [What is an on-premises data gateway](../connect-data/service-gateway-onprem.md) for details and next steps.</span></span>



## <a name="next-steps"></a><span data-ttu-id="bcab5-166">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="bcab5-166">Next steps</span></span>

- [<span data-ttu-id="bcab5-167">ดูรายงานแบบแบ่งหน้าในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="bcab5-167">View a paginated report in the Power BI service</span></span>](../consumer/paginated-reports-view-power-bi-service.md)
- [<span data-ttu-id="bcab5-168">รายงานแบบแบ่งหน้าใน Power BI Premium คืออะไร</span><span class="sxs-lookup"><span data-stu-id="bcab5-168">What are paginated reports in Power BI Premium?</span></span>](paginated-reports-report-builder-power-bi.md)
- [<span data-ttu-id="bcab5-169">บทช่วยสอน: ฝังรายงานที่มีการแบ่งหน้าของ Power BI ในแอปพลิเคชันสำหรับลูกค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="bcab5-169">Tutorial: Embed Power BI paginated reports into an application for your customers</span></span>](../developer/embedded/embed-paginated-reports-customers.md)
