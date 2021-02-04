---
title: ข้อมูลสดของ SQL Server Analysis Services ใน Power BI
description: ข้อมูลสดของ SQL Server Analysis Services ใน Power BI สิ่งนี้สามารถทำได้ผ่านแหล่งข้อมูล ที่ถูกกำหนดค่าสำหรับเกตเวย์เอ็นเตอร์ไพรส์
author: Minewiskan
ms.author: davidi
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.reviewer: ''
ms.custom: ''
ms.date: 08/10/2017
LocalizationGroup: Data from databases
ms.openlocfilehash: 81d2f350c524335d3aa8c7fbb9c82a6cb045e9e5
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96391909"
---
# <a name="sql-server-analysis-services-live-data-in-power-bi"></a><span data-ttu-id="93f28-104">ข้อมูลสดของ SQL Server Analysis Services ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="93f28-104">SQL Server Analysis Services live data in Power BI</span></span>

<span data-ttu-id="93f28-105">ใน Power BI มีสองวิธีที่คุณสามารถเชื่อมต่อสดกับเซิร์ฟเวอร์ SQL Server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="93f28-105">In Power BI, there are two ways you can connect to a live SQL Server Analysis Services server.</span></span> <span data-ttu-id="93f28-106">ใน **รับข้อมูล** คุณสามารถเชื่อมต่อกับเซิร์ฟเวอร์ SQL Server Analysis Services หรือคุณสามารถเชื่อมต่อกับ [ไฟล์ Power BI Desktop](service-desktop-files.md) หรือ [สมุดงาน Excel](service-excel-workbook-files.md) ที่เชื่อมต่อกับเซิร์ฟเวอร์ Analysis Services อยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="93f28-106">In **Get data**, you can connect to a SQL Server Analysis Services server, or you can connect to a [Power BI Desktop file](service-desktop-files.md), or [Excel workbook](service-excel-workbook-files.md), that already connects to an Analysis Services server.</span></span> <span data-ttu-id="93f28-107">แนวทางปฏิบัติที่ดีที่สุด Microsoft ขอแนะนำให้ใช้ Power BI Desktop เนื่องจากความสมบูรณ์ของชุดเครื่องมือตัวและความสามารถในการรักษาสำเนาสำรองของไฟล์ Power BI Desktop ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="93f28-107">As a best practice, Microsoft strongly recommends using Power BI Desktop because of the richness of the toolset and the ability to maintain a backup copy of the Power BI Desktop file locally.</span></span>

>[!IMPORTANT]
> * <span data-ttu-id="93f28-108">เพื่อเชื่อมต่อสดไปยังเซิร์ฟเวอร์ Analysis Services เกตเวย์ข้อมูลภายในองค์กร ต้องถูกติดตั้งและกำหนดค่าโดยผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="93f28-108">In order to connect to a live Analysis Services server, an On-premises data gateway must be installed and configured by an administrator.</span></span> <span data-ttu-id="93f28-109">สำหรับข้อมูลเพิ่มเติม ดู[เกตเวย์ข้อมูลภายในองค์กร](service-gateway-onprem.md)</span><span class="sxs-lookup"><span data-stu-id="93f28-109">For more information, see [On-premises data gateway](service-gateway-onprem.md).</span></span>
> * <span data-ttu-id="93f28-110">เมื่อคุณใช้เกตเวย์ ข้อมูลของคุณยังคงอยู่ภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="93f28-110">When you use the gateway, your data remains on-premises.</span></span>  <span data-ttu-id="93f28-111">รายงานที่คุณสร้างขึ้นจากข้อมูลนั้น จะถูกบันทึกในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="93f28-111">The reports you create based on that data are saved in the Power BI service.</span></span> 
> * <span data-ttu-id="93f28-112">[ถามตอบ คิวรีด้วยภาษาธรรมชาติ](../create-reports/service-q-and-a-direct-query.md) ยังเป็นคุณลักษณะตัวอย่าง สำหรับการเชื่อมต่อ Analysis Services แบบสด</span><span class="sxs-lookup"><span data-stu-id="93f28-112">[Q&A natural language querying](../create-reports/service-q-and-a-direct-query.md) is in preview for Analysis Services live connections.</span></span>

## <a name="to-connect-to-a-model-from-get-data"></a><span data-ttu-id="93f28-113">เชื่อมต่อกับรูปแบบข้อมูลจาก รับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="93f28-113">To connect to a model from Get data</span></span>

1. <span data-ttu-id="93f28-114">ใน **พื้นที่ทำงานของฉัน** เลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="93f28-114">In **My Workspace**, select **Get data**.</span></span> <span data-ttu-id="93f28-115">คุณยังสามารถเปลี่ยนไปยังพื้นที่ทำงานกลุ่ม ถ้ามี</span><span class="sxs-lookup"><span data-stu-id="93f28-115">You can also change to a group workspace, if one is available.</span></span>

   ![เชื่อมต่อเพื่อรับปุ่มข้อมูล](media/sql-server-analysis-services-tabular-data/connecttoas_getdatabutton.png)

2. <span data-ttu-id="93f28-117">เลือก **ฐานข้อมูลและอื่นๆ อีกมากมาย**</span><span class="sxs-lookup"><span data-stu-id="93f28-117">Select **Databases & More**.</span></span>

   ![เชื่อมต่อเพื่อรับข้อมูล 1](media/sql-server-analysis-services-tabular-data/connecttoas_getdata_1.png)

3. <span data-ttu-id="93f28-119">เลือก **SQL Server Analysis Services** > **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="93f28-119">Select **SQL Server Analysis Services** > **Connect**.</span></span>

   ![เชื่อมต่อเพื่อรับข้อมูล 2](media/sql-server-analysis-services-tabular-data/connecttoas_getdata_2.png)

4. <span data-ttu-id="93f28-121">เลือกเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="93f28-121">Select a server.</span></span> <span data-ttu-id="93f28-122">ถ้าคุณไม่เห็นเซิร์ฟเวอร์ใดเลยในนี้ แสดงว่ายังไม่ได้กำหนดเกตเวย์และแหล่งข้อมูล หรือบัญชีของคุณไม่ได้อยู่ในรายการในแท็บ **ผู้ใช้** ของแหล่งข้อมูลในเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="93f28-122">If you don't see any servers listed here, it means either a gateway, and data source, are not configured, or your account is not listed in the **Users** tab of the data source, in the gateway.</span></span> <span data-ttu-id="93f28-123">ตรวจสอบกับผู้ดูแลของคุณ</span><span class="sxs-lookup"><span data-stu-id="93f28-123">Check with your administrator.</span></span>

5. <span data-ttu-id="93f28-124">เลือกรูปแบบที่คุณต้องการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="93f28-124">Select the model you want to connect to.</span></span> <span data-ttu-id="93f28-125">ซึ่งอาจเป็นแบบตาราง หรือแบบหลายมิติ</span><span class="sxs-lookup"><span data-stu-id="93f28-125">This could be either Tabular or Multidimensional.</span></span>

<span data-ttu-id="93f28-126">หลังจากคุณเชื่อมต่อกับรูปแบบแล้ว จะปรากฏในไซต์ Power BI ของคุณใน **พื้นที่ทำงาน/ชุดข้อมูลของฉัน**</span><span class="sxs-lookup"><span data-stu-id="93f28-126">After you connect to the model, it will appear in your Power BI site in **My Workspace/Datasets**.</span></span> <span data-ttu-id="93f28-127">ถ้าคุณสลับไปยังพื้นที่ทำงานกลุ่ม ชุดข้อมูลจะปรากฏขึ้นภายในกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="93f28-127">If you were switched to a group workspace, then the dataset will appear within the group.</span></span>

![เชื่อมต่อกับชุดข้อมูล](media/sql-server-analysis-services-tabular-data/connecttoas_dataset_5.png)

## <a name="dashboard-tiles"></a><span data-ttu-id="93f28-129">ไทล์แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="93f28-129">Dashboard tiles</span></span>

<span data-ttu-id="93f28-130">ถ้าคุณปักหมุดวิชวลจากรายงานไปยังแดชบอร์ด ไทล์ที่ปักหมุดไว้จะรีเฟรชทุก 10 นาทีโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="93f28-130">If you pin visuals from a report to the dashboard, the pinned tiles are automatically refreshed every 10 minutes.</span></span> <span data-ttu-id="93f28-131">ถ้ามีการอัปเดตข้อมูลในเซิร์ฟเวอร์ Analysis Services ภายในองค์กรของคุณ ไทล์จะได้รับการปรับปรุงอัตโนมัติหลังผ่านไป 10 นาที</span><span class="sxs-lookup"><span data-stu-id="93f28-131">If the data in your on-premises Analysis Services server is updated, the tiles will get auto-updated after 10 minutes.</span></span>

## <a name="common-issues"></a><span data-ttu-id="93f28-132">ปัญหาที่พบบ่อย</span><span class="sxs-lookup"><span data-stu-id="93f28-132">Common Issues</span></span>

* <span data-ttu-id="93f28-133">ข้อผิดพลาด ไม่สามารถโหลดเค้าร่างแบบจำลอง - ข้อผิดพลาดนี้เกิดขึ้นเมื่อผู้ใช้เชื่อมต่อกับ SSAS ไม่ได้รับอนุญาตให้เข้าถึงฐานข้อมูล SSAS, คิวบ์ และแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="93f28-133">Cannot load the model schema error - This error occurs when the user connecting to SSAS does not have access to the SSAS database, cube and model.</span></span>

## <a name="next-steps"></a><span data-ttu-id="93f28-134">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="93f28-134">Next steps</span></span>

* [<span data-ttu-id="93f28-135">เกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="93f28-135">On-premises data gateway</span></span>](service-gateway-onprem.md)  
* [<span data-ttu-id="93f28-136">จัดการแหล่งข้อมูล Analysis Services</span><span class="sxs-lookup"><span data-stu-id="93f28-136">Manage Analysis Services data sources</span></span>](service-gateway-enterprise-manage-ssas.md)  
* [<span data-ttu-id="93f28-137">การแก้ไขปัญหา เกตเวย์ข้อมูลในองค์กร</span><span class="sxs-lookup"><span data-stu-id="93f28-137">Troubleshooting the On-premises data gateway</span></span>](service-gateway-onprem-tshoot.md)  

<span data-ttu-id="93f28-138">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="93f28-138">More questions?</span></span> [<span data-ttu-id="93f28-139">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="93f28-139">Try the Power BI Community</span></span>](https://community.powerbi.com/)
