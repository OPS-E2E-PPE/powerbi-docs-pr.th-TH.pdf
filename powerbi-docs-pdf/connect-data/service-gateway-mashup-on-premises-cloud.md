---
title: ผสาน หรือผนวก แหล่งข้อมูลภายในองค์กรและในระบบคลาวด์
description: ใช้เกตเวย์ข้อมูลภายในองค์กร เพื่อผสานหรือผนวก แหล่งข้อมูลภายในองค์กรและในระบบคลาวด์ ในคิวรีเดียวกัน
author: arthiriyer
ms.author: arthii
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-gateways
ms.topic: how-to
ms.date: 07/15/2019
LocalizationGroup: Gateways
ms.openlocfilehash: 4da44d0915b981c22b0c334fb5586b97c3b01ea2
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96402397"
---
# <a name="merge-or-append-on-premises-and-cloud-data-sources"></a><span data-ttu-id="06240-103">ผสาน หรือผนวก แหล่งข้อมูลภายในองค์กรและในระบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="06240-103">Merge or append on-premises and cloud data sources</span></span>

[!INCLUDE [gateway-rewrite](../includes/gateway-rewrite.md)]

<span data-ttu-id="06240-104">คุณสามารถใช้เกตเวย์ข้อมูลภายในองค์กร เพื่อผสานหรือผนวก แหล่งข้อมูลภายในองค์กรและในระบบคลาวด์ ในคิวรีเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="06240-104">You can use the on-premises data gateway to merge or append on-premises and cloud data sources in the same query.</span></span> <span data-ttu-id="06240-105">โซลูชันนี้จะมีประโยชน์เมื่อคุณต้องการรวมข้อมูลจากหลายแหล่งข้อมูลเข้าด้วยกัน โดยไม่ต้องใช้คิวรีที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="06240-105">This solution is helpful when you want to combine data from multiple sources without having to use separate queries.</span></span>

>[!NOTE]
><span data-ttu-id="06240-106">บทความนี้นำไปใช้กับชุดข้อมูลที่มีระบบคลาวด์และแหล่งข้อมูลภายในองค์กรที่ผสานหรือผนวกในคิวรีเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="06240-106">This article applies only to datasets that have cloud and on-premises data sources merged or appended in a single query.</span></span> <span data-ttu-id="06240-107">สำหรับชุดข้อมูลซึ่งรวมถึงคิวรีที่แยกต่างหาก - คิวรีหนึ่งซึ่งจะเชื่อมต่อไปยังแหล่งข้อมูลภายในองค์กรและอีกคิวรีหนึ่งไปยังแหล่งข้อมูลบนคลาวด์--เกตเวย์ไม่ได้ดำเนินการคิวรีสำหรับแหล่งข้อมูลบนคลาวด์</span><span class="sxs-lookup"><span data-stu-id="06240-107">For datasets that include separate queries--one that connects to an on-premises data source and the other to a cloud data source--the gateway doesn't execute the query for the cloud data source.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="06240-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="06240-108">Prerequisites</span></span>

- <span data-ttu-id="06240-109">[เกตเวย์ที่ติดตั้ง](/data-integration/gateway/service-gateway-install)ภายในคอมพิวเตอร์</span><span class="sxs-lookup"><span data-stu-id="06240-109">A [gateway installed](/data-integration/gateway/service-gateway-install) on a local computer.</span></span>
- <span data-ttu-id="06240-110">ไฟล์ Power BI Desktop ที่มีคิวรีที่รวมแหล่งข้อมูลภายในองค์กรและในระบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="06240-110">A Power BI Desktop file with queries that combine on-premises and cloud data sources.</span></span>

>[!NOTE]
><span data-ttu-id="06240-111">ในการเข้าถึงแหล่งข้อมูลระบบคลาวด์ใด ๆ คุณต้องตรวจสอบให้แน่ใจว่าเกตเวย์มีการเข้าถึงแหล่งข้อมูลเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="06240-111">To access any cloud data sources, you must ensure that the gateway has access to those data sources.</span></span>

1. <span data-ttu-id="06240-112">ที่มุมบนขวาของบริการ Power BI เลือกไอคอนรูปเฟือง ![ไอคอนเฟืองตั้งค่า](media/service-gateway-mashup-on-premises-cloud/icon-gear.png) > **จัดการเกตเวย์**</span><span class="sxs-lookup"><span data-stu-id="06240-112">In the upper-right corner of the Power BI service, select the gear icon ![Settings gear icon](media/service-gateway-mashup-on-premises-cloud/icon-gear.png) > **Manage gateways**.</span></span>

    ![จัดการเกตเวย์](media/service-gateway-mashup-on-premises-cloud/manage-gateways.png)

2. <span data-ttu-id="06240-114">เลือกเกตเวย์ที่คุณต้องการกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="06240-114">Select the gateway you want to configure.</span></span>

3. <span data-ttu-id="06240-115">ภายใต้ **การตั้งค่าคลัสเตอร์เกตเวย์** เลือก **อนุญาตให้แหล่งข้อมูลระบบคลาวด์ของผู้ใช้รีเฟรชผ่านคลัสเตอร์เกตเวย์นี้** > **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="06240-115">Under **Gateway Cluster Settings**, select **Allow user's cloud data sources to refresh through this gateway cluster** > **Apply**.</span></span>

    ![รีเฟรชผ่านคลัสเตอร์เกตเวย์นี้](media/service-gateway-mashup-on-premises-cloud/refresh-gateway-cluster.png)

4. <span data-ttu-id="06240-117">ภายใต้คลัสเตอร์เกตเวย์นี้ เพิ่ม[แหล่งข้อมูลในองค์กร](service-gateway-enterprise-manage-scheduled-refresh.md#add-a-data-source)ใด ๆ ที่ใช้ในคิวรีของคุณ</span><span class="sxs-lookup"><span data-stu-id="06240-117">Under this gateway cluster, add any [on-premises data sources](service-gateway-enterprise-manage-scheduled-refresh.md#add-a-data-source) used in your queries.</span></span> <span data-ttu-id="06240-118">คุณไม่จำเป็นต้องเพิ่มแหล่งข้อมูลระบบคลาวด์ตรงนี้</span><span class="sxs-lookup"><span data-stu-id="06240-118">You don't need to add the cloud data sources here.</span></span>

5. <span data-ttu-id="06240-119">อัปโหลดไฟล์ Power BI Desktop พร้อมคิวรีที่รวมแหล่งข้อมูลภายในองค์กรและในระบบคลาวด์ของคุณ ไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="06240-119">Upload to the Power BI service your Power BI Desktop file with the queries that combine on-premises and cloud data sources.</span></span>

6. <span data-ttu-id="06240-120">บนหน้า **การตั้งค่าชุดข้อมูล** สำหรับชุดข้อมูลใหม่:</span><span class="sxs-lookup"><span data-stu-id="06240-120">On the **Dataset settings** page for the new dataset:</span></span>

   - <span data-ttu-id="06240-121">สำหรับแหล่งข้อมูลภายในองค์กร เลือกเกตเวย์ที่เกี่ยวข้องกับแหล่งข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="06240-121">For the on-premises source, select the gateway associated with this data source.</span></span>
   - <span data-ttu-id="06240-122">ภายใต้ **ข้อมูลประจำตัวของแหล่งข้อมูล** แก้ไขข้อมูลประจำตัวแหล่งข้อมูลคลาวด์ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="06240-122">Under **Data source credentials**, edit the cloud data source credentials, as necessary.</span></span>

    <span data-ttu-id="06240-123">ตรวจสอบให้แน่ใจว่าระดับความเป็นส่วนตัวสำหรับระบบคลาวด์และแหล่งข้อมูลภายในองค์กรได้รับการตั้งค่าอย่างเหมาะสมเพื่อให้แน่ใจว่ามีการจัดการการรวมอย่างปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="06240-123">Make sure privacy levels for both cloud and on-premises data sources are set appropriately to ensure the joins are handled securely.</span></span>

     ![การตั้งค่าชุดข้อมูล](media/service-gateway-mashup-on-premises-cloud/dataset-settings.png)

7. <span data-ttu-id="06240-125">เมื่อตั้งค่าข้อมูลประจำตัวบนระบบคลาวด์แล้ว คุณสามารถรีเฟรชชุดข้อมูลได้ โดยใช้ตัวเลือก **รีเฟรชเดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="06240-125">With the cloud credentials set, you can now refresh the dataset by using the **Refresh now** option.</span></span> <span data-ttu-id="06240-126">หรือกำหนดเวลาการรีเฟรชเป็นระยะได้</span><span class="sxs-lookup"><span data-stu-id="06240-126">Or, you can schedule it to refresh periodically.</span></span>

## <a name="next-steps"></a><span data-ttu-id="06240-127">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="06240-127">Next steps</span></span>

<span data-ttu-id="06240-128">เพื่อเรียนรู้เพิ่มเติมเกี่ยวกับการรีเฟรชข้อมูลสำหรับเกตเวย์ ดู[การใช้แหล่งข้อมูลสำหรับการรีเฟรชตามกำหนดเวลา](service-gateway-enterprise-manage-scheduled-refresh.md#use-the-data-source-for-scheduled-refresh)</span><span class="sxs-lookup"><span data-stu-id="06240-128">To learn more about data refresh for gateways, see [Use the data source for scheduled refresh](service-gateway-enterprise-manage-scheduled-refresh.md#use-the-data-source-for-scheduled-refresh).</span></span>
