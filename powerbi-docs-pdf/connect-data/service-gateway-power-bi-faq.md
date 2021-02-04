---
title: คำถามที่ถามบ่อยเกี่ยวกับเกตเวย์ข้อมูลภายในองค์กร - Power BI
description: บทความนี้เป็นบทความเกี่ยวกับคำถามที่พบบ่อยสำหรับเกตเวย์ข้อมูลภายในองค์กรสำหรับ Power BI บทความนี้รวบรวมคำถามที่พบบ่อยสำหรับเกตเวย์ที่ใช้ใน Power BI ไว้ในที่เดียว
author: arthiriyer
ms.author: arthii
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-gateways
ms.topic: conceptual
ms.date: 07/15/2019
LocalizationGroup: Gateways
ms.openlocfilehash: f9a51e6150c7ae351cea968c0d7ea39d2d0d6c32
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96392231"
---
# <a name="on-premises-data-gateway-faq---power-bi"></a><span data-ttu-id="0b7bd-104">คำถามที่ถามบ่อยเกี่ยวกับเกตเวย์ข้อมูลภายในองค์กร - Power BI</span><span class="sxs-lookup"><span data-stu-id="0b7bd-104">On-premises data gateway FAQ - Power BI</span></span>

[!INCLUDE [gateway-rewrite](../includes/gateway-rewrite.md)]

## <a name="power-bi"></a><span data-ttu-id="0b7bd-105">Power BI</span><span class="sxs-lookup"><span data-stu-id="0b7bd-105">Power BI</span></span>

<span data-ttu-id="0b7bd-106">**คำถาม:** ฉันจำเป็นต้องอัปเกรดเกตเวย์ข้อมูลภายในองค์กร (โหมดส่วนบุคคล) หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="0b7bd-106">**Question:** Do I need to upgrade the on-premises data gateway (personal mode)?</span></span>

<span data-ttu-id="0b7bd-107">**คำตอบ:** ไม่ คุณสามารถใช้เกตเวย์ (โหมดส่วนบุคคล) สำหรับ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="0b7bd-107">**Answer:** No, you can keep using the gateway (personal mode) for Power BI.</span></span>

<span data-ttu-id="0b7bd-108">**คำถาม:** ต้องมีสิทธิ์พิเศษใด ๆ ในการติดตั้งเกตเวย์และจัดการในบริการของ Power BI หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0b7bd-108">**Question:** Are any special permissions required to install the gateway and manage it in the Power BI service?</span></span>

<span data-ttu-id="0b7bd-109">**คำตอบ:** ไม่จำเป็นต้องมีสิทธิ์พิเศษ</span><span class="sxs-lookup"><span data-stu-id="0b7bd-109">**Answer:** No special permissions are required.</span></span>

<span data-ttu-id="0b7bd-110">**คำถาม:** สามารถฉันอัปโหลดเวิร์กบุ๊ก Excel ด้วยแบบจำลองข้อมูล Power Pivot ที่เชื่อมต่อกับแหล่งข้อมูลภายในองค์กรได้หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="0b7bd-110">**Question:** Can I upload Excel workbooks with Power Pivot data models that connect to on-premises data sources?</span></span> <span data-ttu-id="0b7bd-111">ฉันต้องใช้เกตเวย์สำหรับสถานการณ์สมมตินี้หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="0b7bd-111">Do I need a gateway for this scenario?</span></span> 

<span data-ttu-id="0b7bd-112">**คำตอบ:** ใช่ คุณสามารถอัปโหลดเวิร์กบุ๊กได้</span><span class="sxs-lookup"><span data-stu-id="0b7bd-112">**Answer:** Yes, you can upload the workbook.</span></span> <span data-ttu-id="0b7bd-113">และไม่ คุณไม่จำเป็นต้องมีเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="0b7bd-113">And, no, you don’t need a gateway.</span></span> <span data-ttu-id="0b7bd-114">แต่เนื่องจากข้อมูลจะอยู่ในแบบจำลองข้อมูล Excel รายงานใน Power BI ที่ยึดตามเวิร์กบุ๊ก Excel จะไม่สามารถใช้งานแบบสดได้</span><span class="sxs-lookup"><span data-stu-id="0b7bd-114">But, because the data will reside in the Excel data model, reports in Power BI based on the Excel workbook won't be live.</span></span> <span data-ttu-id="0b7bd-115">เพื่อรีเฟรชรายงานใน Power BI แต่ละครั้งคุณจะต้องอัปโหลดเวิร์กบุ๊กที่อัปเดตแล้วอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="0b7bd-115">To refresh reports in Power BI, you have to re-upload an updated workbook each time.</span></span> <span data-ttu-id="0b7bd-116">หรือใช้เกตเวย์ที่มีการรีเฟรชตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="0b7bd-116">Or, use the gateway with scheduled refresh.</span></span>

<span data-ttu-id="0b7bd-117">**คำถาม:** ถ้าผู้ใช้แชร์แดชบอร์ดที่มีการเชื่อมต่อ DirectQuery ผู้ใช้บุคคลอื่นเหล่านั้นจะสามารถดูข้อมูลได้หรือไม่ แม้ว่าพวกเขาอาจไม่มีสิทธิ์การเข้าใช้งานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="0b7bd-117">**Question:** If users share dashboards that have a DirectQuery connection, will those other users be able to see the data even though they might not have the same permissions?</span></span> 

<span data-ttu-id="0b7bd-118">**คำตอบ:** สำหรับแดชบอร์ดที่เชื่อมต่อกับ Azure Analysis Services ผู้ใช้จะเห็นเฉพาะข้อมูลที่พวกเขามีสิทธิ์เข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="0b7bd-118">**Answer:** For a dashboard connected to Azure Analysis Services, users will see only the data they have access to.</span></span> <span data-ttu-id="0b7bd-119">ถ้าผู้ใช้ไม่มีสิทธิ์การเข้าใช้เดียวกัน พวกเขาจะไม่สามารถดูข้อมูลใด ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="0b7bd-119">If the users don't have the same permissions, they won't be able to see any data.</span></span> <span data-ttu-id="0b7bd-120">สำหรับแหล่งข้อมูลอื่น ๆ ผู้ใช้ทั้งหมดจะแชร์ข้อมูลประจำตัวที่ป้อนเข้าไปโดยผู้ดูแลระบบสำหรับแหล่งข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="0b7bd-120">For other data sources, all users will share the credentials entered by the admin for that data source.</span></span>

<span data-ttu-id="0b7bd-121">**คำถาม:** เหตุใดฉันจึงไม่สามารถเชื่อมต่อเซิร์ฟเวอร์ Oracle ของฉันได้?</span><span class="sxs-lookup"><span data-stu-id="0b7bd-121">**Question:** Why can't I connect to my Oracle server?</span></span> 

<span data-ttu-id="0b7bd-122">**คำตอบ:** คุณอาจจำเป็นต้องติดตั้ง Oracle Client และกำหนดค่าไฟล์ tnsnames.ora ด้วยข้อมูลเซิร์ฟเวอร์ที่เหมาะสมเพื่อให้สามารถเชื่อมต่อกับเซิร์ฟเวอร์ Oracle ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="0b7bd-122">**Answer:** You might need to install the Oracle client and configure the tnsnames.ora file with the proper server information in order to connect to your Oracle server.</span></span> <span data-ttu-id="0b7bd-123">นี่คือการติดตั้งแยกต่างหากภายนอกเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="0b7bd-123">This is a separate installation outside of the gateway.</span></span> <span data-ttu-id="0b7bd-124">สำหรับข้อมูลเพิ่มเติม โปรดดู [ติดตั้ง Oracle Client](service-gateway-onprem-manage-oracle.md#install-the-oracle-client)</span><span class="sxs-lookup"><span data-stu-id="0b7bd-124">For more information, see [Install the Oracle client](service-gateway-onprem-manage-oracle.md#install-the-oracle-client).</span></span>

<span data-ttu-id="0b7bd-125">**คำถาม:** ฉันกำลังใช้สคริปต์ R</span><span class="sxs-lookup"><span data-stu-id="0b7bd-125">**Question:** I'm using R scripts.</span></span> <span data-ttu-id="0b7bd-126">ระบบจะรองรับหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0b7bd-126">Is that supported?</span></span>

<span data-ttu-id="0b7bd-127">**คำตอบ**: สคริปต์ R ได้รับการรองรับสำหรับโหมดส่วนตัวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0b7bd-127">**Answer**: R scripts are supported only for personal mode.</span></span>

## <a name="analysis-services-in-power-bi"></a><span data-ttu-id="0b7bd-128">Analysis Services ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="0b7bd-128">Analysis Services in Power BI</span></span>

<span data-ttu-id="0b7bd-129">**คำถาม:** ฉันสามารถใช้ msdmpump.dll เพื่อสร้างแมปชื่อผู้ใช้ที่มีผลบังคับใช้แบบกำหนดเองสำหรับ Analysis Service ได้หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="0b7bd-129">**Question:** Can I use msmdpump.dll to create custom effective username mappings for Analysis Services?</span></span> 

<span data-ttu-id="0b7bd-130">**คำตอบ:** หมายเลข</span><span class="sxs-lookup"><span data-stu-id="0b7bd-130">**Answer:** No.</span></span> <span data-ttu-id="0b7bd-131">ปัจจุบัน ระบบยังไม่สนับสนุนการใช้งานนี้</span><span class="sxs-lookup"><span data-stu-id="0b7bd-131">This use isn't supported at this time.</span></span>

<span data-ttu-id="0b7bd-132">**คำถาม:** ฉันสามารถใช้เกตเวย์เพื่อเชื่อมต่อกับตัวอย่าง (OLAP) แบบหลายมิติได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="0b7bd-132">**Question:** Can I use the gateway to connect to a multidimensional (OLAP) instance?</span></span> 

<span data-ttu-id="0b7bd-133">**คำตอบ:** ใช่</span><span class="sxs-lookup"><span data-stu-id="0b7bd-133">**Answer:** Yes.</span></span> <span data-ttu-id="0b7bd-134">เกตเวย์ข้อมูลภายในองค์กรรองรับการเชื่อมต่อสดไปยังแบบจำลองทั้งตาราง Analysis Services และ Multidimensional (แบบหลายมิติ)</span><span class="sxs-lookup"><span data-stu-id="0b7bd-134">The on-premises data gateway supports live connections to both Analysis Services Tabular and Multidimensional models.</span></span>

<span data-ttu-id="0b7bd-135">**คำถาม:** จะเกิดอะไรขึ้นถ้าฉันติดตั้งเกตเวย์บนคอมพิวเตอร์ในโดเมนอื่นนอกเหนือจากเซิร์ฟเวอร์ภายในองค์กรของฉันที่ใช้การรับรองความถูกต้องของ Windows?</span><span class="sxs-lookup"><span data-stu-id="0b7bd-135">**Question:** What if I install the gateway on a computer in a different domain from my on-premises server that uses Windows authentication?</span></span> 

<span data-ttu-id="0b7bd-136">**คำตอบ:** ไม่รับประกันที่นี่</span><span class="sxs-lookup"><span data-stu-id="0b7bd-136">**Answer:** No guarantees here.</span></span> <span data-ttu-id="0b7bd-137">ทั้งหมดขึ้นอยู่กับความน่าเชื่อถือของความสัมพันธ์ระหว่างสองโดเมน</span><span class="sxs-lookup"><span data-stu-id="0b7bd-137">It all depends on the trust relationship between the two domains.</span></span> <span data-ttu-id="0b7bd-138">ถ้าโดเมนทั้งสองอยู่ในแบบจำลองโดเมนที่เชื่อถือได้ เกตเวย์อาจสามารถเชื่อมต่อไปยังเซิร์ฟเวอร์ Analysis Services และสามารถแก้ไขชื่อผู้ใช้ที่มีผลบังคับใช้ได้</span><span class="sxs-lookup"><span data-stu-id="0b7bd-138">If the two different domains are in a trusted domain model, the gateway might be able to connect to the Analysis Services server and the effective username can be resolved.</span></span> <span data-ttu-id="0b7bd-139">ถ้าไม่ใช่เป็นเช่นนั้น คุณอาจไม่สามารถเข้าสู่ระบบได้</span><span class="sxs-lookup"><span data-stu-id="0b7bd-139">If not, you might encounter a login failure.</span></span>

<span data-ttu-id="0b7bd-140">**คำถาม:** ฉันจะรู้ได้อย่างไรว่าชื่อผู้ใช้ที่มีผลบังคับใช้ใดที่กำลังถูกส่งผ่านไปยังเซิร์ฟเวอร์ Analysis Services ภายในองค์กรของฉัน?</span><span class="sxs-lookup"><span data-stu-id="0b7bd-140">**Question:** How can I find out what effective username is being passed to my on-premises Analysis Services server?</span></span> 

<span data-ttu-id="0b7bd-141">**คำตอบ:** เราตอบคำถามนี้ใน [บทความการแก้ไขปัญหา](service-gateway-onprem-tshoot.md)</span><span class="sxs-lookup"><span data-stu-id="0b7bd-141">**Answer:** We answer this question in the [troubleshooting article](service-gateway-onprem-tshoot.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="0b7bd-142">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="0b7bd-142">Next steps</span></span>

* [<span data-ttu-id="0b7bd-143">การแก้ไขปัญหาเกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="0b7bd-143">Troubleshooting the on-premises data gateway</span></span>](/data-integration/gateway/service-gateway-tshoot)

<span data-ttu-id="0b7bd-144">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0b7bd-144">More questions?</span></span> <span data-ttu-id="0b7bd-145">ลองไปที่ [ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="0b7bd-145">Try the [Power BI Community](https://community.powerbi.com/).</span></span>
