---
title: แหล่งข้อมูลแบบฝังตัวสำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI
description: ในบทความนี้ คุณจะได้เรียนรู้วิธีการสร้างและปรับเปลี่ยนแหล่งข้อมูลแบบฝังตัวในรายงานแบบแบ่งหน้า ในบริการของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: report-builder
ms.topic: how-to
ms.date: 03/02/2020
ms.openlocfilehash: 29ed0a764773c2252989aa05bfcabe5976472d11
ms.sourcegitcommit: ccf53e87ff7cba1fcd9d2cca761a561e62933f90
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/04/2020
ms.locfileid: "93297823"
---
# <a name="create-an-embedded-data-source-for-paginated-reports-in-the-power-bi-service"></a><span data-ttu-id="a84d7-103">สร้างแหล่งข้อมูลแบบฝังตัวสำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="a84d7-103">Create an embedded data source for paginated reports in the Power BI service</span></span>

<span data-ttu-id="a84d7-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span><span class="sxs-lookup"><span data-stu-id="a84d7-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span></span> 

<span data-ttu-id="a84d7-105">ในบทความนี้ คุณจะได้เรียนรู้วิธีการสร้างและปรับเปลี่ยนแหล่งข้อมูลแบบฝังตัวสำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="a84d7-105">In this article, you learn how to create and modify an embedded data source for a paginated report in the Power BI service.</span></span> <span data-ttu-id="a84d7-106">คุณอาจกำหนดแหล่งข้อมูลแบบฝังตัวได้ในรายงาน และใช้เฉพาะในรายงานนั้น</span><span class="sxs-lookup"><span data-stu-id="a84d7-106">You define an embedded data source in a single report, and use it only in that report.</span></span> <span data-ttu-id="a84d7-107">ในตอนนี้ รายงานแบบแบ่งหน้าที่เผยแพร่ไปยังบริการของ Power BI ต้องใช้ชุดข้อมูลแบบฝังตัวและแหล่งข้อมูลแบบฝังตัว และสามารถเชื่อมต่อกับแหล่งข้อมูลเหล่านี้ได้:</span><span class="sxs-lookup"><span data-stu-id="a84d7-107">Currently, paginated reports published to the Power BI service need embedded datasets and embedded data sources, and can connect to these data sources:</span></span>

- <span data-ttu-id="a84d7-108">Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="a84d7-108">Azure Analysis Services</span></span>
- <span data-ttu-id="a84d7-109">ฐานข้อมูล Azure SQL และ</span><span class="sxs-lookup"><span data-stu-id="a84d7-109">Azure SQL Database and</span></span> 
- <span data-ttu-id="a84d7-110">คลังข้อมูล Azure SQL</span><span class="sxs-lookup"><span data-stu-id="a84d7-110">Azure SQL Data Warehouse</span></span>
- <span data-ttu-id="a84d7-111">SQL Server</span><span class="sxs-lookup"><span data-stu-id="a84d7-111">SQL Server</span></span>
- <span data-ttu-id="a84d7-112">SQL Server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="a84d7-112">SQL Server Analysis Services</span></span>
- <span data-ttu-id="a84d7-113">Oracle</span><span class="sxs-lookup"><span data-stu-id="a84d7-113">Oracle</span></span> 
- <span data-ttu-id="a84d7-114">Teradata</span><span class="sxs-lookup"><span data-stu-id="a84d7-114">Teradata</span></span> 

<span data-ttu-id="a84d7-115">สำหรับแหล่งข้อมูลต่อไปนี้ ให้ใช้ตัวเลือก[การเชื่อมต่อ SQL Server Analysis Services](../admin/service-premium-connect-tools.md):</span><span class="sxs-lookup"><span data-stu-id="a84d7-115">For the following data sources, use the [SQL Server Analysis Services connection](../admin/service-premium-connect-tools.md) option:</span></span>

- <span data-ttu-id="a84d7-116">ชุดข้อมูล Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="a84d7-116">Power BI Premium datasets</span></span>

<span data-ttu-id="a84d7-117">รายงานแบบแบ่งหน้าจะเชื่อมต่อกับแหล่งข้อมูลในองค์กรโดยใช้[เกตเวย์ของ Power BI](../connect-data/service-gateway-onprem.md)</span><span class="sxs-lookup"><span data-stu-id="a84d7-117">Paginated reports connect to on-premises data sources by way of a [Power BI gateway](../connect-data/service-gateway-onprem.md).</span></span> <span data-ttu-id="a84d7-118">คุณสามารถตั้งค่าเกตเวย์ได้หลังจากที่เผยแพร่รายงานไปยังบริการของ Power BI แล้ว</span><span class="sxs-lookup"><span data-stu-id="a84d7-118">You set up the gateway after you publish the report to the Power BI service.</span></span>

<span data-ttu-id="a84d7-119">ดู[ข้อมูลรายงานในตัวสร้างรายงาน Power BI](report-builder-data.md) สำหรับรายละเอียดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a84d7-119">See [Report Data in Power BI Report Builder](report-builder-data.md) for more detailed information.</span></span>

## <a name="create-an-embedded-data-source"></a><span data-ttu-id="a84d7-120">สร้างแหล่งข้อมูลแบบฝังตัว</span><span class="sxs-lookup"><span data-stu-id="a84d7-120">Create an embedded data source</span></span>
  
1. <span data-ttu-id="a84d7-121">เกิดตัวสร้างรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="a84d7-121">Open Power BI Report Builder.</span></span>

1. <span data-ttu-id="a84d7-122">ที่แถบเครื่องมือในแผงข้อมูลรายงาน ให้คุณเลือก **แหล่งข้อมูล** > **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="a84d7-122">On the toolbar in the Report Data pane, select **New** > **Data Source**.</span></span> <span data-ttu-id="a84d7-123">กล่องโต้ตอบ **คุณสมบัติแหล่งข้อมูล** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="a84d7-123">The **Data Source Properties** dialog box opens.</span></span>

   ![แหล่งข้อมูลใหม่](media/paginated-reports-embedded-data-source/power-bi-paginated-new-data-source.png)
  
1. <span data-ttu-id="a84d7-125">ในกล่องข้อความ **ชื่อ** พิมพ์ชื่อสำหรับแหล่งข้อมูลหรือยอมรับค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a84d7-125">In the **Name** text box, type a name for the data source or accept the default.</span></span>  
  
1. <span data-ttu-id="a84d7-126">เลือก **ใช้การเชื่อมต่อที่ฝังอยู่ในรายงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="a84d7-126">Select **Use a connection embedded in my report**.</span></span>  
  
1. <span data-ttu-id="a84d7-127">เลือกชนิดแหล่งข้อมูลจากรายการ **เลือกชนิดการเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="a84d7-127">From the **Select connection type** list, select a data source type.</span></span> 

1. <span data-ttu-id="a84d7-128">ระบุสตริงเชื่อมต่อโดยใช้วิธีการใดวิธีการหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a84d7-128">Specify a connection string by using one of these methods:</span></span>  
  
   - <span data-ttu-id="a84d7-129">พิมพ์สตริงเชื่อมต่อลงในกล่องข้อความ **สตริงการเชื่อมต่อ** โดยตรง</span><span class="sxs-lookup"><span data-stu-id="a84d7-129">Type the connection string directly in the **Connection string** text box.</span></span> 
  
   - <span data-ttu-id="a84d7-130">เลือก **สร้าง** เพื่อเปิดกล่องโต้ตอบ **คุณสมบัติการเชื่อมต่อ** สำหรับแหล่งข้อมูลที่คุณเลือกในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="a84d7-130">Select **Build** to open the **Connection Properties** dialog box for the data source you chose in step 2.</span></span>  
  
     <span data-ttu-id="a84d7-131">กรอกเขตข้อมูลลงในกล่องโต้ตอบ **คุณสมบัติการเชื่อมต่อ** ตามที่เหมาะสมกับชนิดของแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a84d7-131">Fill in the fields in the **Connection Properties** dialog box as appropriate for the data source type.</span></span> <span data-ttu-id="a84d7-132">คุณสมบัติการเชื่อมต่อประกอบไปด้วยชนิดของแหล่งข้อมูล ชื่อของแหล่งข้อมูล และข้อมูลประจำตัวที่ใช้</span><span class="sxs-lookup"><span data-stu-id="a84d7-132">Connection properties include the type of data source, the name of the data source, and the credentials to use.</span></span> <span data-ttu-id="a84d7-133">หลังจากที่คุณระบุค่าในกล่องโต้ตอบนี้แล้ว ให้เลือก **ทดสอบการเชื่อมต่อ** เพื่อยืนยันว่าแหล่งข้อมูลพร้อมใช้งานและข้อมูลประจำตัวที่คุณระบุนั้นถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a84d7-133">After you specify values in this dialog box, select **Test Connection** to verify that the data source is available and that the credentials you specified are correct.</span></span>  
  
1. <span data-ttu-id="a84d7-134">เลือก **ข้อมูลประจำตัว**</span><span class="sxs-lookup"><span data-stu-id="a84d7-134">Select **Credentials**.</span></span>  
  
   <span data-ttu-id="a84d7-135">ระบุข้อมูลประจำตัวเพื่อใช้กับแหล่งข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="a84d7-135">Specify the credentials to use for this data source.</span></span> <span data-ttu-id="a84d7-136">เจ้าของแหล่งข้อมูลจะเลือกชนิดของข้อมูลประจำตัวที่รองรับ</span><span class="sxs-lookup"><span data-stu-id="a84d7-136">The owner of the data source chooses the type of credentials that are supported.</span></span> <span data-ttu-id="a84d7-137">สำหรับข้อมูลเพิ่มเติม โปรดดู [ระบุข้อมูลประจำตัวและข้อมูลการเชื่อมต่อสำหรับแหล่งข้อมูลรายงาน](/sql/reporting-services/report-data/specify-credential-and-connection-information-for-report-data-sources)</span><span class="sxs-lookup"><span data-stu-id="a84d7-137">For more information, see [Specify Credential and Connection Information for Report Data Sources](/sql/reporting-services/report-data/specify-credential-and-connection-information-for-report-data-sources).</span></span>
  
1. <span data-ttu-id="a84d7-138">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a84d7-138">Select **OK**.</span></span>  
  
   <span data-ttu-id="a84d7-139">แหล่งข้อมูลจะปรากฏขึ้นในแผงข้อมูลรายงาน</span><span class="sxs-lookup"><span data-stu-id="a84d7-139">The data source appears in the Report Data pane.</span></span>

## <a name="limitations-and-considerations"></a><span data-ttu-id="a84d7-140">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="a84d7-140">Limitations and Considerations</span></span>

<span data-ttu-id="a84d7-141">รายงานแบบแบ่งหน้าที่เชื่อมต่อกับชุดข้อมูล Power BI ปฏิบัติตามกฎสำหรับชุดข้อมูลที่แชร์ร่วมกันใน Power BI พร้อมการเปลี่ยนแปลงเล็กน้องบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="a84d7-141">Paginated reports connecting to Power BI datasets follow the rules for shared datasets in Power BI with some minor changes.</span></span>  <span data-ttu-id="a84d7-142">สำหรับผู้ใช้เพื่อดูรายงานแบบแบ่งหน้าโดยใช้ชุดข้อมูล Power BI ได้อย่างเหมาะสม และเพื่อให้แน่ใจว่ามีการเปิดใช้งานและบังคับใช้การจำกัดสิทธิ์ในการเข้าถึงข้อมูลของผู้ใช้ในระดับแถวของข้อมูล (RLS)  สำหรับผู้ชมของคุณ ตรวจสอบให้แน่ใจว่าคุณปฏิบัติตามกฎเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="a84d7-142">For users to properly view paginated reports using Power BI datasets, and to ensure  row-level security (RLS) is enabled and enforced for your viewers, make sure you follow these rules:</span></span>

### <a name="classic-apps-and-workspaces"></a><span data-ttu-id="a84d7-143">แอปและพื้นที่ทำงานแบบคลาสสิก</span><span class="sxs-lookup"><span data-stu-id="a84d7-143">Classic apps and workspaces</span></span>

- <span data-ttu-id="a84d7-144">.rdl ในพื้นที่ทำงานเดียวกันเป็นชุดข้อมูล (เจ้าของรายเดิม): สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="a84d7-144">.rdl in same workspace as dataset (same owner): Supported</span></span>
- <span data-ttu-id="a84d7-145">.rdl ในพื้นที่ทำงานต่างกันเป็นชุดข้อมูล (เจ้าของรายเดิม): สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="a84d7-145">.rdl in different workspace as dataset (same owner): Supported</span></span>
- <span data-ttu-id="a84d7-146">.rdl ที่แชร์: คุณจำเป็นต้องมีสิทธิ์ในการอ่านที่กำหนดให้กับผู้ใช้แต่ละรายเพื่อดูรายงานในระดับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a84d7-146">Shared .rdl: You need Read permission assigned for each user viewing the report at the dataset level</span></span>
- <span data-ttu-id="a84d7-147">แอปที่แชร์: คุณจำเป็นต้องมีสิทธิ์ในการอ่านที่กำหนดให้กับผู้ใช้แต่ละรายเพื่อดูรายงานในระดับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a84d7-147">Shared app: You need Read permission assigned for each user viewing the report at the dataset level</span></span>
- <span data-ttu-id="a84d7-148">.rdl ในพื้นที่ทำงานเดียวกันเป็นชุดข้อมูล (ผู้ใช้งานที่แตกต่างกัน): สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="a84d7-148">.rdl in same workspace as dataset (different user): Supported</span></span>
- <span data-ttu-id="a84d7-149">.rdl ในพื้นที่ทำงานแตกต่างกันเป็นชุดข้อมูล (ผู้ใช้งานที่แตกต่างกัน): คุณจำเป็นต้องมีสิทธิ์ในการอ่านที่กำหนดให้กับผู้ใช้แต่ละรายเพื่อดูรายงานในระดับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a84d7-149">.rdl in different workspace as dataset (different user):You need Read permission assigned for each user viewing the report at the dataset level</span></span>
- <span data-ttu-id="a84d7-150">การรักษาความปลอดภัยในระดับบทบาท คุณจำเป็นต้องมีสิทธิ์ในการอ่านที่กำหนดให้กับผู้ใช้แต่ละรายเพื่อดูรายงานในระดับชุดข้อมูลเพื่อบังคับใช้สิทธิ์</span><span class="sxs-lookup"><span data-stu-id="a84d7-150">Role-level security: You need Read permission assigned for each user viewing the report at the dataset level to have it enforced.</span></span>

### <a name="new-experience-apps-and-workspaces"></a><span data-ttu-id="a84d7-151">แอปและพื้นที่ทำงานประสบการณ์การใช้งานใหม่</span><span class="sxs-lookup"><span data-stu-id="a84d7-151">New experience apps and workspaces</span></span>

- <span data-ttu-id="a84d7-152">.rdl ในพื้นที่ทำงานเดียวกันเป็นชุดข้อมูล: สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="a84d7-152">.rdl in same workspace as dataset: Supported</span></span>
- <span data-ttu-id="a84d7-153">.rdl ในพื้นที่ทำงานต่างกันเป็นชุดข้อมูล (เจ้าของรายเดิม): สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="a84d7-153">.rdl in different workspace as dataset (same owner): Supported</span></span>
- <span data-ttu-id="a84d7-154">.rdl ที่แชร์: คุณจำเป็นต้องมีสิทธิ์ในการอ่านที่กำหนดให้กับผู้ใช้แต่ละรายเพื่อดูรายงานในระดับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a84d7-154">Shared .rdl: You need Read permission assigned for each user viewing the report at the dataset level</span></span>
- <span data-ttu-id="a84d7-155">แอปที่แชร์: คุณจำเป็นต้องมีสิทธิ์ในการอ่านที่กำหนดให้กับผู้ใช้แต่ละรายเพื่อดูรายงานในระดับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a84d7-155">Shared app: You need Read permission assigned for each user viewing the report at the dataset level</span></span>
- <span data-ttu-id="a84d7-156">.rdl ในพื้นที่ทำงานเดียวกันเป็นชุดข้อมูล (ผู้ใช้งานที่แตกต่างกัน) - ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="a84d7-156">.rdl in same workspace as dataset (different user) - Supported</span></span>
- <span data-ttu-id="a84d7-157">.rdl ในพื้นที่ทำงานต่างกันเป็นชุดข้อมูล (ผู้ใช้งานที่แตกต่างกัน): คุณจำเป็นต้องมีสิทธิ์ในการอ่านที่กำหนดให้กับผู้ใช้แต่ละรายเพื่อดูรายงานในระดับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a84d7-157">.rdl in different workspace as dataset (different user): You need Read permission assigned for each user viewing the report at the dataset level</span></span>
- <span data-ttu-id="a84d7-158">การรักษาความปลอดภัยในระดับบทบาท คุณจำเป็นต้องมีสิทธิ์ในการอ่านที่กำหนดให้กับผู้ใช้แต่ละรายเพื่อดูรายงานในระดับชุดข้อมูลเพื่อบังคับใช้สิทธิ์</span><span class="sxs-lookup"><span data-stu-id="a84d7-158">Role-level security: You need Read permission assigned for each user viewing the report at the dataset level to have it enforced</span></span>

## <a name="next-steps"></a><span data-ttu-id="a84d7-159">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a84d7-159">Next steps</span></span>

- [<span data-ttu-id="a84d7-160">สร้างชุดข้อมูลแบบฝังตัวสำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="a84d7-160">Create an embedded dataset for a paginated report in the Power BI service</span></span>](paginated-reports-create-embedded-dataset.md)
- [<span data-ttu-id="a84d7-161">รายงานแบบแบ่งหน้าใน Power BI Premium คืออะไร</span><span class="sxs-lookup"><span data-stu-id="a84d7-161">What are paginated reports in Power BI Premium?</span></span>](paginated-reports-report-builder-power-bi.md)