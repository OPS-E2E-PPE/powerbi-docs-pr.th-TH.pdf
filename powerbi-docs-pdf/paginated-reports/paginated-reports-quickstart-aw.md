---
title: 'บทช่วยสอน: สร้างรายงานแบบแบ่งหน้าและอัปโหลดไปยังบริการของ Power BI'
description: ในบทช่วยสอนนี้ คุณจะได้เชื่อมต่อกับฐานข้อมูลตัวอย่าง Azure SQL จากนั้นคุณจะได้ใช้วิซาร์ดในตัวสร้างรายงานเพื่อสร้างรายงานแบบแบ่งหน้า และคุณจะได้อัปโหลดรายงานแบบแบ่งหน้าไปยังพื้นที่ทำงานในบริการของ Power BI ด้วยความจุพรีเมียม
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: report-builder
ms.topic: tutorial
ms.date: 11/06/2018
ms.openlocfilehash: baccdcae82fb56b2f7f7a9d6cb4839e941e99bf0
ms.sourcegitcommit: ccf53e87ff7cba1fcd9d2cca761a561e62933f90
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/04/2020
ms.locfileid: "93297521"
---
# <a name="tutorial-create-a-paginated-report-and-upload-it-to-the-power-bi-service"></a><span data-ttu-id="c61a6-105">บทช่วยสอน: สร้างรายงานแบบแบ่งหน้าและอัปโหลดไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="c61a6-105">Tutorial: Create a paginated report and upload it to the Power BI service</span></span>

<span data-ttu-id="c61a6-106">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span><span class="sxs-lookup"><span data-stu-id="c61a6-106">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span></span> 

<span data-ttu-id="c61a6-107">ในบทช่วยสอนนี้ คุณจะได้เชื่อมต่อกับฐานข้อมูลตัวอย่าง Azure SQL</span><span class="sxs-lookup"><span data-stu-id="c61a6-107">In this tutorial, you connect to a sample Azure SQL database.</span></span> <span data-ttu-id="c61a6-108">จากนั้นคุณจะได้ใช้วิซาร์ดในตัวสร้างรายงาน Power BI เพื่อสร้างรายงานแบบแบ่งหน้าพร้อมตารางที่ครอบคลุมพื้นที่หลายหน้า</span><span class="sxs-lookup"><span data-stu-id="c61a6-108">Then you use a wizard in Power BI Report Builder to create a paginated report with a table that wraps to multiple pages.</span></span> <span data-ttu-id="c61a6-109">และคุณจะได้อัปโหลดรายงานแบบแบ่งหน้าไปยังพื้นที่ทำงานในบริการของ Power BI ด้วยความจุพรีเมียม</span><span class="sxs-lookup"><span data-stu-id="c61a6-109">Then you upload the paginated report to a workspace in a Premium capacity in the Power BI service.</span></span>

![รายงานแบบแบ่งหน้าในบริการของ Power BI](media/paginated-reports-quickstart-aw/power-bi-paginated-report-service.png)

<span data-ttu-id="c61a6-111">โปรดใช้ขั้นตอนต่อไปนี้เพื่อทำตามบทช่วยสอน:</span><span class="sxs-lookup"><span data-stu-id="c61a6-111">Here are the steps you complete in this tutorial:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="c61a6-112">สร้างฐานข้อมูลตัวอย่าง Azure</span><span class="sxs-lookup"><span data-stu-id="c61a6-112">Create an Azure sample database.</span></span>
> * <span data-ttu-id="c61a6-113">สร้างเมทริกซ์ในตัวสร้างรายงาน Power BI โดยใช้วิซาร์ดช่วย</span><span class="sxs-lookup"><span data-stu-id="c61a6-113">Create a matrix in Power BI Report Builder with the help of a wizard.</span></span>
> * <span data-ttu-id="c61a6-114">จัดรูปแบบรายงานให้สวยงามด้วยการเพิ่มชื่อเรื่อง หมายเลขหน้าและหัวคอลัมน์ในแต่ละหน้า</span><span class="sxs-lookup"><span data-stu-id="c61a6-114">Format the report with title, page numbers, and column headings on each page.</span></span>
> * <span data-ttu-id="c61a6-115">จัดรูปแบบสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="c61a6-115">Format the currency.</span></span>
> * <span data-ttu-id="c61a6-116">อัปโหลดรายงานเข้าบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="c61a6-116">Upload the report to the Power BI service.</span></span>

<span data-ttu-id="c61a6-117">ถ้าคุณยังไม่มีการสมัครใช้งาน Azure สร้าง[บัญชีฟรี](https://azure.microsoft.com/free/?WT.mc_id=A261C142F)ก่อนที่คุณจะเริ่ม</span><span class="sxs-lookup"><span data-stu-id="c61a6-117">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>
 
## <a name="prerequisites"></a><span data-ttu-id="c61a6-118">สิ่งที่จำเป็นต้องมี</span><span class="sxs-lookup"><span data-stu-id="c61a6-118">Prerequisites</span></span>  

<span data-ttu-id="c61a6-119">โปรดดูข้อกำหนดเบื้องต้นในการสร้างรายงานแบบแบ่งหน้า:</span><span class="sxs-lookup"><span data-stu-id="c61a6-119">Here are the prerequisites for creating the paginated report:</span></span>

- <span data-ttu-id="c61a6-120">ติดตั้ง[ตัวสร้างรายงาน Power BI จากศูนย์ดาวน์โหลด Microsoft](https://aka.ms/pbireportbuilder)</span><span class="sxs-lookup"><span data-stu-id="c61a6-120">Install [Power BI Report Builder from the Microsoft Download Center](https://aka.ms/pbireportbuilder).</span></span> 

- <span data-ttu-id="c61a6-121">ทำตามการเริ่มต้นด่วน[สร้างฐานข้อมูลตัวอย่าง Azure SQL ในพอร์ทัล Azure](/azure/sql-database/sql-database-get-started-portal)</span><span class="sxs-lookup"><span data-stu-id="c61a6-121">Follow the quickstart [Create an Azure SQL database sample  in the Azure portal](/azure/sql-database/sql-database-get-started-portal).</span></span> <span data-ttu-id="c61a6-122">คัดลอก และบันทึกค่าในกล่อง **ชื่อเซิร์ฟเวอร์** ในแท็บ **ภาพรวม** โปรดจดจำชื่อผู้ใช้และรหัสผ่านที่คุณสร้างใน Azure</span><span class="sxs-lookup"><span data-stu-id="c61a6-122">Copy and save the value in the **Server name** box on the **Overview** tab. Remember the user name and password you created in Azure.</span></span>

<span data-ttu-id="c61a6-123">โปรดดูข้อกำหนดเบื้องต้นในการอัปโหลดรายงานแบบแบ่งหน้าไปยังบริการของ Power BI:</span><span class="sxs-lookup"><span data-stu-id="c61a6-123">Here are the prerequisites for uploading your paginated report to the Power BI service:</span></span>

- <span data-ttu-id="c61a6-124">คุณต้องมี[สิทธิ์การใช้งาน Power BI Pro](../admin/service-admin-licensing-organization.md)</span><span class="sxs-lookup"><span data-stu-id="c61a6-124">You need a [Power BI Pro license](../admin/service-admin-licensing-organization.md).</span></span>
- <span data-ttu-id="c61a6-125">คุณต้องมีพื้นที่ทำงานบนบริการใน[ความจุ Power BI Premium](../admin/service-premium-what-is.md)</span><span class="sxs-lookup"><span data-stu-id="c61a6-125">You need a workspace on the service in a [Power BI Premium capacity](../admin/service-premium-what-is.md).</span></span> <span data-ttu-id="c61a6-126">มีไอคอนรูปข้าวหลามตัดที่หมายถึง![ไอคอนรูปข้าวหลามตัดพรีเมียม](media/paginated-reports-quickstart-aw/premium-diamond.png)อยู่ถัดจากชื่อของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="c61a6-126">It has a diamond icon ![Premium diamond icon](media/paginated-reports-quickstart-aw/premium-diamond.png) next to the workspace name.</span></span>

## <a name="create-the-matrix-with-a-wizard"></a><span data-ttu-id="c61a6-127">ใช้วิซาร์ดสร้างเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="c61a6-127">Create the matrix with a wizard</span></span>
  
1.  <span data-ttu-id="c61a6-128">เริ่มตัวสร้างรายงาน Power BI จากคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c61a6-128">Start Power BI Report Builder from your computer.</span></span>  
  
     <span data-ttu-id="c61a6-129">กล่องโต้ตอบ **เริ่มต้นใช้งาน** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="c61a6-129">The **Getting Started** dialog box opens.</span></span>  
  
     ![ตัวสร้างรายงานจะเริ่มต้นทำงาน](media/paginated-reports-create-embedded-dataset/power-bi-paginated-get-started.png)
  
1.  <span data-ttu-id="c61a6-131">ดูที่แผงข้างซ้ายและยืนยันว่าได้เลือก **รายงานใหม่** แล้ว จากนั้นดูที่แผงข้างขวาและเลือก **ตารางหรือวิซาร์ดเมทริกซ์**</span><span class="sxs-lookup"><span data-stu-id="c61a6-131">In the left pane, verify that **New Report** is selected, and in the right pane, select **Table or Matrix Wizard**.</span></span>  
  
4.  <span data-ttu-id="c61a6-132">ในหน้า **เลือกชุดข้อมูล** ให้คุณเลือก **สร้างชุดข้อมูล** > **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="c61a6-132">In the **Choose a dataset** page, select **Create a dataset** > **Next**.</span></span>  

    ![สร้างชุดข้อมูล](media/paginated-reports-quickstart-aw/power-bi-paginated-create-dataset.png)
  
5.  <span data-ttu-id="c61a6-134">ในหน้า **เลือกการเชื่อมต่อไปยังแหล่งข้อมูล** ให้คุณเลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c61a6-134">In the **Choose a connection to a data source** page, select **New**.</span></span> 

    ![แหล่งข้อมูลใหม่](media/paginated-reports-quickstart-aw/power-bi-paginated-new-data-source-connection.png)
  
     <span data-ttu-id="c61a6-136">กล่องโต้ตอบ **คุณสมบัติแหล่งข้อมูล** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="c61a6-136">The **Data Source Properties** dialog box opens.</span></span>  
  
6.  <span data-ttu-id="c61a6-137">คุณสามารถตั้งชื่อแหล่งข้อมูลได้ตามต้องการ โดยใช้อักขระและเส้นขีดล่าง</span><span class="sxs-lookup"><span data-stu-id="c61a6-137">You can name a data source anything you want, using characters and underscores.</span></span> <span data-ttu-id="c61a6-138">สำหรับบทช่วยสอนนี้ ให้คุณพิมพ์ **MyAzureDataSource** ในกล่อง **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="c61a6-138">For this tutorial, in the **Name** box, type **MyAzureDataSource**.</span></span>  
  
7.  <span data-ttu-id="c61a6-139">ในกล่อง **เลือกชนิดการเชื่อมต่อ** ให้คุณเลือก **Microsoft Azure SQL Database**</span><span class="sxs-lookup"><span data-stu-id="c61a6-139">In the **Select connection type** box, select **Microsoft Azure SQL Database**.</span></span>  
  
8.  <span data-ttu-id="c61a6-140">เลือก **สร้าง** ที่อยู่ถัดจากกล่อง **สตริงการเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="c61a6-140">Select **Build** next to the **Connection string** box.</span></span> 

    ![คุณสมบัติแหล่งข้อมูล - สร้าง](media/paginated-reports-quickstart-aw/power-bi-paginated-data-source-properties-build.png)

9. <span data-ttu-id="c61a6-142">**ใน Azure:** ให้คุณย้อนกลับไปที่พอร์ทัล Azure และเลือก **ฐานข้อมูล SQL**</span><span class="sxs-lookup"><span data-stu-id="c61a6-142">**In Azure:** Go back to the Azure portal and select **SQL databases**.</span></span>

1. <span data-ttu-id="c61a6-143">เลือกฐานข้อมูล Azure SQL ที่คุณสร้างขึ้นในการเริ่มต้นด่วน "สร้างฐานข้อมูลตัวอย่าง Azure SQL ในพอร์ทัล Azure" ในส่วน **ข้อกำหนดเบื้องต้น** ของบทความนี้</span><span class="sxs-lookup"><span data-stu-id="c61a6-143">Select the Azure SQL database you created in the quickstart "Create an Azure SQL database sample in the Azure portal" in the **Prerequisites** section of this article.</span></span>

1. <span data-ttu-id="c61a6-144">ที่แท็บ **ภาพรวม** ให้คุณคัดลอกค่าในกล่อง **ชื่อเซิร์ฟเวอร์**</span><span class="sxs-lookup"><span data-stu-id="c61a6-144">On the **Overview** tab, copy the value in the **Server name** box.</span></span>

2. <span data-ttu-id="c61a6-145">**ในตัวสร้างรายงาน** : ในกล่องโต้ตอบ **คุณสมบัติการเชื่อมต่อ** ให้วางชื่อเซิร์ฟเวอร์ที่คุณคัดลอกไว้ใต้ช่อง **ชื่อเซิร์ฟเวอร์**</span><span class="sxs-lookup"><span data-stu-id="c61a6-145">**In Report Builder** : In the **Connection Properties** dialog box, under **Server name** paste the server name you copied.</span></span> 

1. <span data-ttu-id="c61a6-146">ในการ **เข้าสู่เซิร์ฟเวอร์** โปรดแน่ใจว่าได้เลือก **ใช้การตรวจสอบสิทธิ์เซิร์ฟเวอร์ SQL** จากนั้นให้คุณพิมพ์ชื่อผู้ใช้และรหัสผ่านที่สร้างไว้ใน Azure เพื่อใช้กับฐานข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="c61a6-146">For **Log on to the server** , make sure **Use SQL Server Authentication** is selected, then type the user name and password you created in Azure for the sample database.</span></span>

1. <span data-ttu-id="c61a6-147">ที่ด้านล่างของ **เชื่อมต่อไปยังฐานข้อมูล** ให้คุณเลือกลูกศรดรอปดาวน์และเลือกชื่อฐานข้อมูลที่สร้างไว้ใน Azure</span><span class="sxs-lookup"><span data-stu-id="c61a6-147">Under **Connect to a database** , select the drop-down arrow and select the database name you created in Azure.</span></span>
 
    ![คุณสมบัติการเชื่อมต่อแหล่งข้อมูล](media/paginated-reports-quickstart-aw/power-bi-paginated-connection-properties.png)

1. <span data-ttu-id="c61a6-149">เลือก **ทดสอบการเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="c61a6-149">Select **Test Connection**.</span></span> <span data-ttu-id="c61a6-150">คุณจะเห็นข้อความ **ผลการทดสอบ** แสดงว่า **การทดสอบการเชื่อมต่อสำเร็จ**</span><span class="sxs-lookup"><span data-stu-id="c61a6-150">You see the **Test results** message that **Test connection succeeded**.</span></span>

1. <span data-ttu-id="c61a6-151">เลือก **ตกลง** > **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c61a6-151">Select **OK** > **OK**.</span></span> 

   <span data-ttu-id="c61a6-152">ขณะนี้ตัวสร้างรายงานจะแสดงสตริงการเชื่อมต่อที่เพิ่งสร้างไว้ในกล่อง **สตริงการเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="c61a6-152">Now in the **Connection string** box, Report Builder displays the connection string you just created.</span></span> 

    ![สตริงการเชื่อมต่อแหล่งข้อมูล](media/paginated-reports-quickstart-aw/power-bi-paginated-data-source-properties-connection-string.png)

1. <span data-ttu-id="c61a6-154">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c61a6-154">Select **OK**.</span></span>
  
9. <span data-ttu-id="c61a6-155">ในหน้า **เลือกการเชื่อมต่อไปยังแหล่งข้อมูล** คุณจะเห็นคำว่า "(ในรายงานนี้)" อยู่ใต้การเชื่อมต่อกับแหล่งข้อมูลที่เพิ่งสร้าง</span><span class="sxs-lookup"><span data-stu-id="c61a6-155">In the **Choose a connection to a data source** page, you see "(in this Report)" under the data source connection you just created.</span></span> <span data-ttu-id="c61a6-156">เลือกแหล่งข้อมูลนั้น > **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="c61a6-156">Select that data source  > **Next**.</span></span>  

    ![แหล่งข้อมูล Azure ของฉัน](media/paginated-reports-quickstart-aw/power-bi-paginated-my-azure-data-source.png)

10. <span data-ttu-id="c61a6-158">พิมพ์ชื่อผู้ใช้และรหัสผ่านเดียวกันนั้นลงในกล่อง</span><span class="sxs-lookup"><span data-stu-id="c61a6-158">Type the same user name and password in the box.</span></span> 
  
10. <span data-ttu-id="c61a6-159">ในหน้า **ออกแบบคิวรี** ให้คุณขยาย SaleIT และตาราง จากนั้นเลือกตารางเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="c61a6-159">In the **Design a query** page, expand SalesLT, expand Tables, and select these tables:</span></span>

    - <span data-ttu-id="c61a6-160">ที่อยู่</span><span class="sxs-lookup"><span data-stu-id="c61a6-160">Address</span></span>
    - <span data-ttu-id="c61a6-161">ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c61a6-161">Customer</span></span>
    - <span data-ttu-id="c61a6-162">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c61a6-162">Product</span></span>
    - <span data-ttu-id="c61a6-163">ประเภทของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c61a6-163">ProductCategory</span></span>
    - <span data-ttu-id="c61a6-164">SalesOrderDetail</span><span class="sxs-lookup"><span data-stu-id="c61a6-164">SalesOrderDetail</span></span>
    - <span data-ttu-id="c61a6-165">SalesOrderHeader</span><span class="sxs-lookup"><span data-stu-id="c61a6-165">SalesOrderHeader</span></span>

     <span data-ttu-id="c61a6-166">หากมีการเลือก **ตรวจจับอัตโนมัติ** เพื่อหา **ความสัมพันธ์** >  ตัวสร้างรายงานจะตรวจจับความสัมพันธ์ระหว่างตารางเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="c61a6-166">Because **Relationships** > **Auto Detect** is selected, Report Builder detects the relationships between these tables.</span></span> 
    
    ![ออกแบบคิวรี](media/paginated-reports-quickstart-aw/power-bi-paginated-design-query.png)
 
1.  <span data-ttu-id="c61a6-168">เลือก **เรียกใช้คิวรี**</span><span class="sxs-lookup"><span data-stu-id="c61a6-168">Select **Run Query**.</span></span> <span data-ttu-id="c61a6-169">ตัวสร้างรายงานจะแสดง **ผลลัพธ์คิวรี**</span><span class="sxs-lookup"><span data-stu-id="c61a6-169">Report Builder displays the **Query results**.</span></span> 
 
     ![ผลลัพธ์คิวรี](media/paginated-reports-quickstart-aw/power-bi-paginated-query-results.png)

18. <span data-ttu-id="c61a6-171">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="c61a6-171">Select **Next**.</span></span> 

19. <span data-ttu-id="c61a6-172">ในหน้า **เลือกชุดข้อมูล** ให้คุณเลือกชุดข้อมูลที่คุณเพิ่งสร้าง > **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="c61a6-172">In the **Choose a dataset** page, choose the dataset you just created > **Next**.</span></span>

    ![เลือกชุดข้อมูล](media/paginated-reports-quickstart-aw/power-bi-paginated-choose-dataset.png)

1. <span data-ttu-id="c61a6-174">ในหน้า **จัดเรียงเขตข้อมูล** ให้คุณลากเขตข้อมูลเหล่านี้จากกล่อง **เขตข้อมูลพร้อมใช้งาน** ไปยังกล่อง **กลุ่มแถว** :</span><span class="sxs-lookup"><span data-stu-id="c61a6-174">In the **Arrange fields** page, drag these fields from the **Available fields** box to the **Row groups** box:</span></span>

    - <span data-ttu-id="c61a6-175">CompanyName</span><span class="sxs-lookup"><span data-stu-id="c61a6-175">CompanyName</span></span>
    - <span data-ttu-id="c61a6-176">SalesOrderNumber</span><span class="sxs-lookup"><span data-stu-id="c61a6-176">SalesOrderNumber</span></span>
    - <span data-ttu-id="c61a6-177">Product_Name</span><span class="sxs-lookup"><span data-stu-id="c61a6-177">Product_Name</span></span>

1. <span data-ttu-id="c61a6-178">ลากเขตข้อมูลเหล่านี้จากกล่อง **เขตข้อมูลพร้อมใช้งาน** ไปยังกล่อง **ค่า** :</span><span class="sxs-lookup"><span data-stu-id="c61a6-178">Drag these fields from the **Available fields** box to the **Values** box:</span></span>

    - <span data-ttu-id="c61a6-179">OrderQty</span><span class="sxs-lookup"><span data-stu-id="c61a6-179">OrderQty</span></span>
    - <span data-ttu-id="c61a6-180">ราคาต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="c61a6-180">UnitPrice</span></span>
    - <span data-ttu-id="c61a6-181">ยอดรวมรายการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c61a6-181">LineTotal</span></span>

    <span data-ttu-id="c61a6-182">ตัวสร้างรายงานได้สร้างเขตข้อมูลเหล่านี้ไว้ในผลรวมกล่อง **ค่า** โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c61a6-182">Report Builder automatically made the fields in the **Values** box sums.</span></span>

    ![จัดเรียงเขตข้อมูล](media/paginated-reports-quickstart-aw/power-bi-paginated-drag-fields.png)

24. <span data-ttu-id="c61a6-184">ในหน้า **เลือกเค้าโครง** ให้คุณเก็บการตั้งค่าเริ่มต้นทั้งหมดเอาไว้ แต่ให้ล้าง **กลุ่มขยาย/ยุบ**</span><span class="sxs-lookup"><span data-stu-id="c61a6-184">In the **Choose the layout** page, keep all the default settings, but clear **Expand/collapse groups**.</span></span> <span data-ttu-id="c61a6-185">โดยทั่วไปแล้ว ฟีเจอร์กลุ่มขยาย/ยุบใช้งานได้ดีมาก แต่ในครั้งนี้คุณต้องการให้ตารางครอบคลุมพื้นที่หลายหน้า</span><span class="sxs-lookup"><span data-stu-id="c61a6-185">In general, the expand/collapse groups feature is great, but this time you want the table to wrap to multiple pages.</span></span>

1. <span data-ttu-id="c61a6-186">เลือก **ถัดไป** > **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="c61a6-186">Select **Next** > **Finish**.</span></span> <span data-ttu-id="c61a6-187">ตารางแสดงอยู่ในพื้นผิวการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="c61a6-187">The table is displayed on the design surface.</span></span>
 
## <a name="what-youve-created"></a><span data-ttu-id="c61a6-188">สิ่งที่คุณได้สร้างไว้</span><span class="sxs-lookup"><span data-stu-id="c61a6-188">What you've created</span></span>

<span data-ttu-id="c61a6-189">ลองดูผลลัพธ์ของวิซาร์ดกันสักครู่</span><span class="sxs-lookup"><span data-stu-id="c61a6-189">Let's pause for a moment to look at the results of the wizard.</span></span>

![ผลลัพธ์ของวิซาร์ดเมทริกซ์](media/paginated-reports-quickstart-aw/power-bi-paginated-wizard-results.png)

1. <span data-ttu-id="c61a6-191">ในแผงข้อมูลรายงาน คุณจะเห็นแหล่งข้อมูล Azure ที่ฝังตัวและชุดข้อมูลที่ฝังตัวที่อ้างอิงตามแหล่งข้อมูลนั้น ซึ่งคุณสร้างทั้งสองสิ่งนี้ไว้</span><span class="sxs-lookup"><span data-stu-id="c61a6-191">In the Report Data pane, you see the embedded Azure data source and the embedded dataset based on it, both of which you created.</span></span> 

2. <span data-ttu-id="c61a6-192">พื้นผิวออกแบบมีความกว้างประมาณ 6 นิ้ว</span><span class="sxs-lookup"><span data-stu-id="c61a6-192">The design surface is about 6 inches wide.</span></span> <span data-ttu-id="c61a6-193">ที่พื้นผิวออกแบบ คุณจะเห็นเมทริกซ์แสดงหัวคอลัมน์และค่าพื้นที่ที่สำรองไว้</span><span class="sxs-lookup"><span data-stu-id="c61a6-193">On the design surface, you see the matrix, displaying column headings and placeholder values.</span></span> <span data-ttu-id="c61a6-194">โดยเมทริกซ์มีคอลัมน์หกอันและดูเหมือนจะมีความสูงแค่ห้าแถว</span><span class="sxs-lookup"><span data-stu-id="c61a6-194">The matrix has six columns and appears to be only five rows tall.</span></span> 

3. <span data-ttu-id="c61a6-195">ปริมาณการสั่งซื้อ ราคาต่อหน่วย และผลรวมต่อบรรทัด ทั้งหมดที่กล่าวมานี้แสดงเป็นยอดรวม และมีผลรวมย่อยอยู่ในแต่ละกลุ่มแถว</span><span class="sxs-lookup"><span data-stu-id="c61a6-195">Order Qty, Unit Price, and Line Total are all sums, and each row group has a subtotal.</span></span> 

    <span data-ttu-id="c61a6-196">คุณจะยังไม่เห็นค่าข้อมูลจริง</span><span class="sxs-lookup"><span data-stu-id="c61a6-196">You still don't see actual data values.</span></span> <span data-ttu-id="c61a6-197">เมื่อต้องการดูค่าข้อมูลจริง ให้คุณเรียกใช้รายงาน</span><span class="sxs-lookup"><span data-stu-id="c61a6-197">You need to run the report to see them.</span></span>

4. <span data-ttu-id="c61a6-198">ในแผงคุณสมบัติ เมทริกซ์ที่เลือกไว้นั้นเรียกว่า Tablix1</span><span class="sxs-lookup"><span data-stu-id="c61a6-198">In the Properties pane, the selected matrix is called Tablix1.</span></span> <span data-ttu-id="c61a6-199">*Tablix* ในตัวสร้างรายงานคือขอบเขตข้อมูลที่จะแสดงข้อมูลในแถวและคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="c61a6-199">A *tablix* in Report Builder is a data region that displays data in rows and columns.</span></span> <span data-ttu-id="c61a6-200">ซึ่งอาจเป็นได้ทั้งตารางหรือเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="c61a6-200">It can be either a table or a matrix.</span></span>

5. <span data-ttu-id="c61a6-201">ในแผงจัดกลุ่ม คุณจะเห็นกลุ่มสามแถวที่คุณสร้างไว้ในวิซาร์ด:</span><span class="sxs-lookup"><span data-stu-id="c61a6-201">In the Grouping pane, you see the three row groups you created in the wizard:</span></span> 

    - <span data-ttu-id="c61a6-202">CompanyName</span><span class="sxs-lookup"><span data-stu-id="c61a6-202">CompanyName</span></span>
    - <span data-ttu-id="c61a6-203">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="c61a6-203">Sales Order</span></span>
    - <span data-ttu-id="c61a6-204">ชื่อผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c61a6-204">Product Name</span></span>

    <span data-ttu-id="c61a6-205">เมทริกซ์นี้ไม่มีกลุ่มคอลัมน์ใดๆ</span><span class="sxs-lookup"><span data-stu-id="c61a6-205">This matrix doesn't have any column groups.</span></span>

### <a name="run-the-report"></a><span data-ttu-id="c61a6-206">เรียกใช้รายงาน:</span><span class="sxs-lookup"><span data-stu-id="c61a6-206">Run the report</span></span>

<span data-ttu-id="c61a6-207">คุณต้องเรียกใช้รายงานเพื่อดูค่าจริง</span><span class="sxs-lookup"><span data-stu-id="c61a6-207">To see the actual values, you need to run the report.</span></span>

1. <span data-ttu-id="c61a6-208">เลือก **เรียกใช้** ในแถบเครื่องมือ **หน้าหลัก**</span><span class="sxs-lookup"><span data-stu-id="c61a6-208">Select **Run** in the **Home** toolbar.</span></span>

   <span data-ttu-id="c61a6-209">ในตอนนี้คุณดูค่าได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c61a6-209">Now you see the values.</span></span> <span data-ttu-id="c61a6-210">เมทริกซ์มีแถวมากกว่าที่คุณเห็นได้ในมุมมองออกแบบ!</span><span class="sxs-lookup"><span data-stu-id="c61a6-210">The matrix has many more rows than you saw in Design view!</span></span> <span data-ttu-id="c61a6-211">โปรดทราบว่า ตัวสร้างรายงานบอกว่าเป็นหน้า **1** จาก **2?**</span><span class="sxs-lookup"><span data-stu-id="c61a6-211">Note that Report Builder says it's page **1** of **2?**.</span></span> <span data-ttu-id="c61a6-212">ตัวสร้างรายงานจะโหลดรายงานโดยเร็วที่สุด ดังนั้นระบบจะดึงข้อมูลได้เพียงพอสำหรับแค่สองหรือสามหน้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c61a6-212">Report Builder loads the report as quickly as possible, so it only retrieves enough data for a few pages at a time.</span></span> <span data-ttu-id="c61a6-213">เครื่องหมายปรัศนีบ่งชี้ว่า ตัวสร้างรายงานยังโหลดข้อมูลทั้งหมดไม่เสร็จ</span><span class="sxs-lookup"><span data-stu-id="c61a6-213">The question mark indicates that Report Builder hasn't loaded all the data yet.</span></span>

   ![เรียกใช้รายงาน:](media/paginated-reports-quickstart-aw/power-bi-paginated-run-report.png)

2. <span data-ttu-id="c61a6-215">เลือก **เค้าโครงการพิมพ์**</span><span class="sxs-lookup"><span data-stu-id="c61a6-215">Select **Print Layout**.</span></span> <span data-ttu-id="c61a6-216">รายงานจะอยู่ในรูปแบบนี้เมื่อทำการพิมพ์</span><span class="sxs-lookup"><span data-stu-id="c61a6-216">The report will be in this format when you print it.</span></span> <span data-ttu-id="c61a6-217">ตอนนี้ตัวสร้างรายงานรู้แล้วว่ารายงานมีทั้งหมด 33 หน้า และได้เพิ่มสแตมป์วันที่และเวลาไว้ที่ส่วนท้ายแล้วโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c61a6-217">Report Builder now knows the report has 33 pages, and has automatically added a date and time stamp in the footer.</span></span>

## <a name="format-the-report"></a><span data-ttu-id="c61a6-218">จัดรูปแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="c61a6-218">Format the report</span></span>

<span data-ttu-id="c61a6-219">ในตอนนี้คุณก็มีรายงานพร้อมเมทริกซ์ที่ครอบคลุมทั้ง 33 หน้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="c61a6-219">Now you have a report with a matrix that wraps to 33 pages.</span></span> <span data-ttu-id="c61a6-220">มาเพิ่มฟีเจอร์อื่นๆ แล้วปรับปรุงหน้าตาของรายงานกันเถอะ</span><span class="sxs-lookup"><span data-stu-id="c61a6-220">Let's add some other features and improve how it looks.</span></span> <span data-ttu-id="c61a6-221">คุณสามารถเรียกใช้รายงานได้หลังจากทำขั้นตอนครบทุกขั้นตอน หากคุณต้องการดูผลว่าเป็นเช่นไร</span><span class="sxs-lookup"><span data-stu-id="c61a6-221">You can run the report after every step, if you want to see how it's coming along.</span></span>

- <span data-ttu-id="c61a6-222">ในแท็บ **เรียกใช้** ของริบบิ้น ให้คุณเลือก **การออกแบบ** เพื่อให้สามารถแก้ไขต่อได้</span><span class="sxs-lookup"><span data-stu-id="c61a6-222">On the **Run** tab of the Ribbon, select **Design** , so you can continue modifying it.</span></span>  

### <a name="set-page-width"></a><span data-ttu-id="c61a6-223">ตั้งความกว้างหน้าของหน้า</span><span class="sxs-lookup"><span data-stu-id="c61a6-223">Set page width</span></span>

<span data-ttu-id="c61a6-224">โดยทั่วไปแล้วจะมีการจัดรูปแบบรายงานแบบแบ่งหน้าไว้เพื่อการพิมพ์ และขนาดหน้าโดยปกติคือ 8 1/2 x 11 นิ้ว</span><span class="sxs-lookup"><span data-stu-id="c61a6-224">Typically a paginated report is formatted for printing, and a typical page is 8 1/2 X 11 inches.</span></span> 

1. <span data-ttu-id="c61a6-225">ลากไม้บรรทัดเพื่อปรับให้พื้นผิวออกแบบกว้าง 7 นิ้ว</span><span class="sxs-lookup"><span data-stu-id="c61a6-225">Drag the ruler to make the design surface 7 inches wide.</span></span> <span data-ttu-id="c61a6-226">ระยะขอบเริ่มต้นของแต่ละด้านคือ 1 นิ้ว ดังนั้นขอบด้านข้างจึงต้องแคบกว่านี้</span><span class="sxs-lookup"><span data-stu-id="c61a6-226">The default margins are 1 inch on each side, so the side margins need to be narrower.</span></span>

1. <span data-ttu-id="c61a6-227">คลิกในพื้นที่สีเทารอบๆ พื้นผิวการออกแบบเพื่อแสดงคุณสมบัติ **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="c61a6-227">Click in the gray area around the design surface to show the **Report** properties.</span></span>

    <span data-ttu-id="c61a6-228">ถ้าคุณไม่เห็นแผงคุณสมบัติ ให้คลิกที่แท็บ **มุมมอง** > **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="c61a6-228">If you don’t see the Properties pane, click the **View** tab > **Properties**.</span></span>

2. <span data-ttu-id="c61a6-229">ขยาย **ระยะขอบ** และเปลี่ยนขอบ **ซ้าย** และ **ขวา** จาก 1 นิ้วเป็น 0.75 นิ้ว</span><span class="sxs-lookup"><span data-stu-id="c61a6-229">Expand **Margins** and change **Left** and **Right** from 1in to 0.75in.</span></span> 

    ![ตั้งค่าระยะขอบกระดาษ](media/paginated-reports-quickstart-aw/power-bi-paginated-set-margins.png)
  
### <a name="add-a-report-title"></a><span data-ttu-id="c61a6-231">เพิ่มชื่อรายงาน</span><span class="sxs-lookup"><span data-stu-id="c61a6-231">Add a report title</span></span>  

1. <span data-ttu-id="c61a6-232">เลือกคำว่า **คลิกเพื่อเพิ่มชื่อเรื่อง** ที่ด้านบนของหน้า แล้วพิมพ์ว่า **ยอดขายแยกตามบริษัท**</span><span class="sxs-lookup"><span data-stu-id="c61a6-232">Select the words **Click to add title** at the top of the page, then type **Sales by Company**.</span></span>  

2. <span data-ttu-id="c61a6-233">เลือกข้อความชื่อเรื่อง และเปลี่ยน **สี** เป็น **สีฟ้า** โดยเลือกที่แผงคุณสมบัติด้านล่าง **ตัวอักษร**</span><span class="sxs-lookup"><span data-stu-id="c61a6-233">Select the title text, and in the Properties pane under **Font** , change **Color** to **Blue**.</span></span>
  
### <a name="add-a-page-number"></a><span data-ttu-id="c61a6-234">เพิ่มหมายเลขหน้า</span><span class="sxs-lookup"><span data-stu-id="c61a6-234">Add a page number</span></span>

<span data-ttu-id="c61a6-235">คุณจะสังเกตเห็นว่ารายงานมีสแตมป์วันที่และเวลาอยู่ที่ส่วนท้ายหน้า</span><span class="sxs-lookup"><span data-stu-id="c61a6-235">You noticed the report has a date and time stamp in the footer.</span></span> <span data-ttu-id="c61a6-236">คุณสามารถเพิ่มหมายเลขหน้าที่ส่วนท้ายหน้าได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="c61a6-236">You can add a page number to the footer, too.</span></span>

1. <span data-ttu-id="c61a6-237">ที่ด้านล่างของพื้นผิวการออกแบบ คุณจะเห็น [&ExecutionTime] ที่ด้านขวาในส่วนท้ายหน้า</span><span class="sxs-lookup"><span data-stu-id="c61a6-237">At the bottom of the design surface, you see [&ExecutionTime] on the right in the footer.</span></span> 

2. <span data-ttu-id="c61a6-238">ในแผงข้อมูลรายงาน ให้คุณขยายโฟลเดอร์เขตข้อมูลภายใน</span><span class="sxs-lookup"><span data-stu-id="c61a6-238">In the Report Data pane, expand the Built-in Fields folder.</span></span> <span data-ttu-id="c61a6-239">ลาก **หมายเลขหน้า** ไปยังด้านซ้ายของส่วนท้ายหน้า โดยให้อยู่ที่ความสูงเดียวกันกับ [&ExecutionTime]</span><span class="sxs-lookup"><span data-stu-id="c61a6-239">Drag **Page Number** to the left side of the footer, at the same height as [&ExecutionTime].</span></span>

3. <span data-ttu-id="c61a6-240">ลากด้านขวาของกล่อง [&PageNumber] เพื่อทำให้เป็นสี่เหลี่ยม</span><span class="sxs-lookup"><span data-stu-id="c61a6-240">Drag the right side of the [&PageNumber] box to make it square.</span></span>

4. <span data-ttu-id="c61a6-241">ที่แท็บ **แทรก** ให้คุณเลือก **กล่องข้อความ**</span><span class="sxs-lookup"><span data-stu-id="c61a6-241">On the **Insert** tab, select **Text Box**.</span></span>

5. <span data-ttu-id="c61a6-242">คลิกที่ด้านขวาของ [&PageNumber] แล้วพิมพ์ "ของ" จากนั้นทำให้กล่องข้อความเป็นสี่เหลี่ยม</span><span class="sxs-lookup"><span data-stu-id="c61a6-242">Click to the right of [&PageNumber], type "of", then make the text box square.</span></span>

6. <span data-ttu-id="c61a6-243">ลาก **หน้าทั้งหมดโดยรวม** ไปที่ส่วนท้ายหน้า ที่ด้านขวาของ "ของ" จากนั้นลากด้านขวานั้นให้เป็นสี่เหลี่ยมเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="c61a6-243">Drag **Overall Total Pages** to the footer, to the right of "of", then drag its right side to make it square, too.</span></span>

    ![ลากหมายเลขหน้า](media/paginated-reports-quickstart-aw/power-bi-paginated-add-page-numbers.png)

### <a name="make-the-table-wider"></a><span data-ttu-id="c61a6-245">ทำให้ตารางกว้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="c61a6-245">Make the table wider</span></span>  

<span data-ttu-id="c61a6-246">ในตอนนี้คุณสามารถสร้างเมทริกซ์ได้กว้างพอที่จะเติมเต็มความกว้างของหน้า และทำให้คอลัมน์ข้อความกว้างขึ้นเพื่อให้ไม่ต้องเลื่อนดูชื่อมากนัก</span><span class="sxs-lookup"><span data-stu-id="c61a6-246">Now you can make the matrix wide enough to fill the width of the page, and make the text columns wider so the names don't scroll as much.</span></span> 
 
1. <span data-ttu-id="c61a6-247">เลือกเมทริกซ์ จากนั้นเลือกคอลัมน์ชื่อบริษัท</span><span class="sxs-lookup"><span data-stu-id="c61a6-247">Select the matrix, then select the Company Name column.</span></span>

3. <span data-ttu-id="c61a6-248">เลื่อนเมาส์ไปเหนือแถบสีเทาที่ด้านบนของเมทริกซ์ที่ขอบข้างขวาของคอลัมน์ "ชื่อบริษัท"</span><span class="sxs-lookup"><span data-stu-id="c61a6-248">Hover over the gray bar at the top of the matrix at the right edge of the Company Name column.</span></span> <span data-ttu-id="c61a6-249">ลากไปทางขวา จนคอลัมน์ได้ขนาด 1 3/8 นิ้ว</span><span class="sxs-lookup"><span data-stu-id="c61a6-249">Drag to the right, until the column ends at 1 3/8 inches.</span></span> 

    ![ลากขอบข้างขวาของคอลัมน์](media/paginated-reports-quickstart-aw/power-bi-paginated-drag-column.png)

4. <span data-ttu-id="c61a6-251">ลากขอบข้างขวาของ "ชื่อผลิตภัณฑ์" จนกระทั่งคอลัมน์ได้ขนาด 3 3/4 นิ้ว</span><span class="sxs-lookup"><span data-stu-id="c61a6-251">Drag the right edge of Product name until the column ends at 3 3/4 inches.</span></span>   

<span data-ttu-id="c61a6-252">ตอนนี้เมทริกซ์ก็กว้างเกือบเท่ากับพื้นที่การพิมพ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="c61a6-252">Now the matrix is almost as wide as the print area.</span></span>

### <a name="format-the-currency"></a><span data-ttu-id="c61a6-253">จัดรูปแบบสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="c61a6-253">Format the currency</span></span>

<span data-ttu-id="c61a6-254">ถ้าคุณสังเกตเห็นว่าขณะที่เรียกใช้รายงานนั้น จำนวนเงินดอลลาร์ยังไม่ได้จัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="c61a6-254">If you noticed when you ran the report, the dollar amounts aren't formatted as currency yet.</span></span>

1. <span data-ttu-id="c61a6-255">เลือกเซลล์ [Sum(OrderQty)] ที่มุมซ้ายบน จากนั้นกดปุ่ม Shift ค้างไว้ แล้วเลือกเซลล์ [Sum(LineTotal)] ที่มุมขวาล่าง</span><span class="sxs-lookup"><span data-stu-id="c61a6-255">Select the upper-left [Sum(OrderQty)] cell, hold down the Shift key, and select lower-right [Sum(LineTotal)] cell.</span></span>

    ![เลือกเซลล์ที่มีค่าสกุลเงิน](media/paginated-reports-quickstart-aw/power-bi-paginated-select-money-cells.png)

2. <span data-ttu-id="c61a6-257">ที่แท็บ **หน้าหลัก** ให้คุณเลือกสัญลักษณ์สกุลเงินดอลลาร์ ( **$** ) จากนั้นเลือกลูกศรข้างๆ **สไตล์พื้นที่ที่สำรองไว้** > **ค่าตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="c61a6-257">On the **Home** tab, select the dollar sign ( **$** ) currency symbol, then select the arrow next to **Placeholder styles** > **Sample Values**.</span></span>
 
    ![แสดงค่าตัวอย่าง](media/paginated-reports-quickstart-aw/power-bi-paginated-format-currency.png)

    <span data-ttu-id="c61a6-259">ในตอนนี้คุณจะเห็นว่าค่านั้นจัดรูปแบบเป็นสกุลเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="c61a6-259">Now you can see the values are formatted as currency.</span></span>

    ![ค่าสกุลเงินตัวอย่าง](media/paginated-reports-quickstart-aw/power-bi-paginated-display-sample-values.png)

### <a name="add-column-headers-on-each-page"></a><span data-ttu-id="c61a6-261">เพิ่มหัวคอลัมน์ในแต่ละหน้า</span><span class="sxs-lookup"><span data-stu-id="c61a6-261">Add column headers on each page</span></span>

<span data-ttu-id="c61a6-262">การปรับปรุงการจัดรูปแบบอีกอย่างหนึ่งก่อนการเผยแพร่รายงานไปยังบริการของ Power BI: การทำให้หัวคอลัมน์แสดงในแต่ละหน้าของรายงาน</span><span class="sxs-lookup"><span data-stu-id="c61a6-262">One more formatting improvement before publishing the report to the Power BI service: making the column headers show up on each page in the report.</span></span>

1. <span data-ttu-id="c61a6-263">ที่ตรงขวาสุดของแถบด้านบนในแผง "การจัดกลุ่ม" ให้คุณเลือกลูกศรดรอปดาวน์ > **โหมดขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="c61a6-263">In the far-right end of the top bar in the Grouping pane, select the drop-down arrow > **Advanced Mode**.</span></span>

    ![เปิดโหมดขั้นสูง](media/paginated-reports-quickstart-aw/power-bi-paginated-advanced-mode.png)

2. <span data-ttu-id="c61a6-265">เลือกแถบ **สแตติก** ด้านบนใน **กลุ่มแถว**</span><span class="sxs-lookup"><span data-stu-id="c61a6-265">Select the top **Static** bar in the **Row Groups**.</span></span> <span data-ttu-id="c61a6-266">คุณจะเห็นว่ามีการเลือกเซลล์ชื่อบริษัทในเมทริกซ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="c61a6-266">You see that the Company Name cell in the matrix is selected.</span></span>

   ![เลือกกลุ่มสแตติก](media/paginated-reports-quickstart-aw/power-bi-paginated-static-group.png)

3. <span data-ttu-id="c61a6-268">ในแผง **คุณสมบัติ** คุณจะเห็นคุณสมบัติสำหรับ **สมาชิก Tablix**</span><span class="sxs-lookup"><span data-stu-id="c61a6-268">In the **Properties** pane, you're looking at the properties for **Tablix Member**.</span></span> <span data-ttu-id="c61a6-269">ตั้งค่า **KeepWithGroup** เป็น **After** และตั้งค่า **RepeatOnNewPage** เป็น **True**</span><span class="sxs-lookup"><span data-stu-id="c61a6-269">Set **KeepWithGroup** to **After** and **RepeatOnNewPage** to **True**.</span></span>

    ![ตั้งค่า RepeatOnNewPage](media/paginated-reports-quickstart-aw/power-bi-paginated-repeat-on-new-page.png)

    <span data-ttu-id="c61a6-271">ได้เวลาเรียกใช้รายงานแล้วดูว่าตอนนี้หน้าตาเป็นอย่างไร</span><span class="sxs-lookup"><span data-stu-id="c61a6-271">It's time to run the report and see how it looks now.</span></span>

5. <span data-ttu-id="c61a6-272">เลือก **เรียกใช้** ที่แท็บ **หน้าหลัก**</span><span class="sxs-lookup"><span data-stu-id="c61a6-272">Select **Run** on the **Home** tab.</span></span>

6. <span data-ttu-id="c61a6-273">เลือก **เค้าโครงการพิมพ์** ถ้ายังไม่ได้เลือก</span><span class="sxs-lookup"><span data-stu-id="c61a6-273">Select **Print Layout** , if it's not already selected.</span></span> <span data-ttu-id="c61a6-274">รายงานมีอยู่ด้วยกัน 29 หน้า</span><span class="sxs-lookup"><span data-stu-id="c61a6-274">Now the report has 29 pages.</span></span> <span data-ttu-id="c61a6-275">เลื่อนผ่านสักสองสามหน้า</span><span class="sxs-lookup"><span data-stu-id="c61a6-275">Scroll through a few pages.</span></span> <span data-ttu-id="c61a6-276">คุณจะเห็นว่าสกุลเงินจัดรูปแบบแล้ว ทุกหน้ามีหัวคอลัมน์ และรายงานมีส่วนท้ายหน้าที่ระบุหมายเลขหน้าและสแตมป์วันที่และเวลาทุกๆ หน้า</span><span class="sxs-lookup"><span data-stu-id="c61a6-276">You see the currency is formatted, the columns have headings on every page, and the report has a footer with page numbers and date and time stamp on every page.</span></span>
 
    ![หน้าที่เสร็จแล้ว](media/paginated-reports-quickstart-aw/power-bi-paginated-finished-page.png)

7. <span data-ttu-id="c61a6-278">บันทึกรายงานลงคอมพิวเตอร์</span><span class="sxs-lookup"><span data-stu-id="c61a6-278">Save the report to your computer.</span></span>
 
##  <a name="upload-the-report-to-the-service"></a><span data-ttu-id="c61a6-279">อัปโหลดรายงานเข้าส่วนบริการ</span><span class="sxs-lookup"><span data-stu-id="c61a6-279">Upload the report to the service</span></span>

<span data-ttu-id="c61a6-280">ในตอนนี้คุณได้สร้างรายงานแบบแบ่งหน้าแล้ว ได้เวลาอัปโหลดเข้าบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="c61a6-280">Now that you've created this paginated report, it's time to upload it to the Power BI service.</span></span>

1. <span data-ttu-id="c61a6-281">ในบริการ Power BI (`https://app.powerbi.com`) ในหน้าต่างนำทาง ให้เลือก **พื้นที่ทำงาน** > **สร้างพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="c61a6-281">In the Power BI service (`https://app.powerbi.com`) in the nav pane, select **Workspaces** > **Create workspace**.</span></span>

2. <span data-ttu-id="c61a6-282">ตั้งชื่อพื้นที่ทำงานของคุณว่า **Azure AW** หรือชื่อเฉพาะอย่างอื่น</span><span class="sxs-lookup"><span data-stu-id="c61a6-282">Name your workspace **Azure AW** , or other unique name.</span></span> <span data-ttu-id="c61a6-283">ตอนนี้มีเพียงคุณที่เป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="c61a6-283">You're the only member for now.</span></span> 

3. <span data-ttu-id="c61a6-284">เลือกลูกศรที่อยู่ถัดจาก **ขั้นสูง** แล้วเปิด **ความจุเฉพาะ**</span><span class="sxs-lookup"><span data-stu-id="c61a6-284">Select the arrow next to **Advanced** and turn on **Dedicated capacity**.</span></span> 

    ![สร้างพื้นที่ทำงานในความจุพรีเมียม](media/paginated-reports-quickstart-aw/power-bi-paginated-create-workspace-premium-capacity.png)

    <span data-ttu-id="c61a6-286">ถ้าไม่สามารถเปิดได้ คุณต้องขอให้ผู้ดูแลระบบ Power BI ให้อนุญาตคุณในการเพิ่มพื้นที่ทำงานเข้าความจุพรีเมียมเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="c61a6-286">If you can't turn it on, you need to ask your Power BI admin to give you permission to add the workspace to the dedicated Premium capacity.</span></span>

4. <span data-ttu-id="c61a6-287">เลือก **ความจุเฉพาะที่พร้อมใช้งานสำหรับพื้นที่ทำงานนี้** หากจำเป็นให้ > **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c61a6-287">Choose an **available dedicated capacity for this workspace** , if necessary > **Save**.</span></span>
    
    ![ไอคอนข้าวหลามตัดพรีเมียม](media/paginated-reports-quickstart-aw/power-bi-paginated-diamond-icon.png)

    <span data-ttu-id="c61a6-289">ถ้าพื้นที่ทำงานไม่ได้อยู่ในความจุพรีเมียม เมื่อคุณลองอัปโหลดรายงาน คุณจะเห็นข้อความ "ไม่สามารถอัปโหลดรายงานแบบแบ่งหน้าได้"</span><span class="sxs-lookup"><span data-stu-id="c61a6-289">If the workspace isn't in a Premium capacity, when you try to upload your report you see the message, "Unable to upload paginated report."</span></span> <span data-ttu-id="c61a6-290">โปรดติดต่อผู้ดูแลระบบ Power BI เพื่อย้ายพื้นที่ทำงานนั้น</span><span class="sxs-lookup"><span data-stu-id="c61a6-290">Contact your Power BI administrator to move the workspace.</span></span>

1. <span data-ttu-id="c61a6-291">ในพื้นที่ทำงานใหม่ของคุณ ให้เลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="c61a6-291">In your new workspace, select **Get Data**.</span></span>

2. <span data-ttu-id="c61a6-292">ในกล่อง **ไฟล์** > **รับ**</span><span class="sxs-lookup"><span data-stu-id="c61a6-292">In the **Files** box > **Get**.</span></span>

3. <span data-ttu-id="c61a6-293">เลือก **ไฟล์ภายในเครื่อง** ไปยังตำแหน่งที่คุณบันทึกไฟล์ไว้ > **เปิด**</span><span class="sxs-lookup"><span data-stu-id="c61a6-293">Select **Local File** , navigate to where you saved the file > **Open**.</span></span>

   <span data-ttu-id="c61a6-294">Power BI จะนำเข้าไฟล์ของคุณ และคุณจะเห็นไฟล์นั้นอยู่ใต้ **รายงาน** ในหน้ารายการแอป</span><span class="sxs-lookup"><span data-stu-id="c61a6-294">Power BI imports your file, and you see it under **Reports** on the App list page.</span></span>

    ![รายงานในรายการแอป](media/paginated-reports-quickstart-aw/power-bi-paginated-app-list.png)

4. <span data-ttu-id="c61a6-296">เลือกรายงานเพื่อดู</span><span class="sxs-lookup"><span data-stu-id="c61a6-296">Select the report to view it.</span></span>

5. <span data-ttu-id="c61a6-297">ถ้ามีข้อผิดพลาด คุณอาจต้องป้อนข้อมูลประจำตัวใหม่</span><span class="sxs-lookup"><span data-stu-id="c61a6-297">If you get an error, you may need to reenter your credentials.</span></span> <span data-ttu-id="c61a6-298">เลือกไอคอน **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="c61a6-298">Select the **Manage** icon.</span></span>

    ![จัดการรายงานของคุณ](media/paginated-reports-quickstart-aw/power-bi-paginated-manage-report.png)

6. <span data-ttu-id="c61a6-300">เลือก **แก้ไขข้อมูลประจำตัว** แล้วป้อนข้อมูลประจำตัวที่ใช้ใน Azure เมื่อทำการสร้างฐานข้อมูล Azure</span><span class="sxs-lookup"><span data-stu-id="c61a6-300">Select **Edit credentials** and enter the credentials you used in Azure when you created the Azure database.</span></span>

    ![แก้ไขข้อมูลประจำตัวของรายงาน](media/paginated-reports-quickstart-aw/power-bi-paginated-edit-credentials.png)

7. <span data-ttu-id="c61a6-302">ทีนี้คุณสามารถดูรายงานแบบแบ่งหน้าในบริการของ Power BI ได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c61a6-302">Now you can view your paginated report in the Power BI service.</span></span>

    ![รายงานแบบแบ่งหน้าในบริการของ Power BI](media/paginated-reports-quickstart-aw/power-bi-paginated-report-service.png)

## <a name="next-steps"></a><span data-ttu-id="c61a6-304">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c61a6-304">Next steps</span></span>

[<span data-ttu-id="c61a6-305">รายงานแบบแบ่งหน้าใน Power BI Premium คืออะไร</span><span class="sxs-lookup"><span data-stu-id="c61a6-305">What are paginated reports in Power BI Premium?</span></span>](paginated-reports-report-builder-power-bi.md)