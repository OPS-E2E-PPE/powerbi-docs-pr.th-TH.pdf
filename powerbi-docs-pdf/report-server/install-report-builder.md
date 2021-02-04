---
title: ติดตั้งตัวสร้างรายงาน - เซิร์ฟเวอร์รายงาน Power BI
description: บทความนี้อธิบายถึงวิธีการดาวน์โหลดและติดตั้ง ตัวสร้างรายงาน สำหรับเซิร์ฟเวอร์รายงาน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.date: 01/07/2020
ms.openlocfilehash: 0c71a2e6c7c21dc7dc447de804e7f771cebb5369
ms.sourcegitcommit: eef4eee24695570ae3186b4d8d99660df16bf54c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/23/2020
ms.locfileid: "85239278"
---
# <a name="install-report-builder---power-bi-report-server"></a><span data-ttu-id="486f7-103">ติดตั้งตัวสร้างรายงาน - เซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="486f7-103">Install Report Builder - Power BI Report Server</span></span>

<span data-ttu-id="486f7-104">ตัวสร้างรายงานเป็นแอปแบบสแตนด์อโลนที่ติดตั้งบนคอมพิวเตอร์ของคุณโดยคุณหรือผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="486f7-104">Report Builder is a stand-alone app, installed on your computer by you or an administrator.</span></span> <span data-ttu-id="486f7-105">คุณสามารถติดตั้งจากศูนย์ดาวน์โหลด Microsoft หรือจากเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="486f7-105">You can install it from the Microsoft Download Center or from Power BI Report Server.</span></span>  

<span data-ttu-id="486f7-106">กำลังมองหาความช่วยเหลือเกี่ยวกับการติดตั้งตัวสร้างรายงานสำหรับบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="486f7-106">Looking for help with installing Report Builder for the Power BI service?</span></span> <span data-ttu-id="486f7-107">ดู [ตัวสร้างรายงานใน Power BI](../paginated-reports/report-builder-power-bi.md) แทน</span><span class="sxs-lookup"><span data-stu-id="486f7-107">See [Power BI Report Builder](../paginated-reports/report-builder-power-bi.md) instead.</span></span>
  
<span data-ttu-id="486f7-108">โดยทั่วไป ผู้ดูแลระบบจะติดตั้งและกำหนดค่าเซิร์ฟเวอร์รายงาน Power BI อนุญาตการดาวน์โหลดตัวสร้างรายงานจากพอร์ทัลเว็บ และจัดการโฟลเดอร์และสิทธิ์อนุญาตต่างๆ ไปยังรายงาน และชุดข้อมูลที่ใช้ร่วมกันที่บันทึกไปยังเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="486f7-108">An administrator typically installs and configures Power BI Report Server, grants permission to download Report Builder from the web portal, and manages folders and permissions to reports, and shared datasets saved to the report server.</span></span> <span data-ttu-id="486f7-109">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการดูแลระบบเซิร์ฟเวอร์รายงาน Power BI ดู [ภาพรวมผู้ดูแลระบบ, เซิร์ฟเวอร์รายงาน Power BI](admin-handbook-overview.md)</span><span class="sxs-lookup"><span data-stu-id="486f7-109">For more information about Power BI Report Server administration, see the [Admin overview, Power BI Report Server](admin-handbook-overview.md).</span></span>  
  
## <a name="system-requirements"></a><span data-ttu-id="486f7-110">ข้อกำหนดของระบบ</span><span class="sxs-lookup"><span data-stu-id="486f7-110">System requirements</span></span>
  
 <span data-ttu-id="486f7-111">ดูส่วน **ความต้องการของระบบ** ของ [หน้าดาวน์โหลดตัวสร้างรายงาน](https://go.microsoft.com/fwlink/?LinkID=734968) ในศูนย์ดาวน์โหลดของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="486f7-111">See the **System requirements** section of the [Report Builder download page](https://go.microsoft.com/fwlink/?LinkID=734968) on the Microsoft Download Center.</span></span>
 
## <a name="install-report-builder-from-a-web-portal"></a><span data-ttu-id="486f7-112">ติดตั้งตัวสร้างรายงานจากพอร์ทัลเว็บ</span><span class="sxs-lookup"><span data-stu-id="486f7-112">Install Report Builder from a web portal</span></span>
  
<span data-ttu-id="486f7-113">คุณสามารถติดตั้งตัวสร้างรายงานได้จากพอร์ทัลเว็บเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="486f7-113">You can install Report Builder from a Power BI Report Server web portal.</span></span> <span data-ttu-id="486f7-114">คุณอาจมีการติดตั้งตัวสร้างรายงานเพื่อสร้างรายงานสำหรับเซิร์ฟเวอร์ SSRS แล้ว</span><span class="sxs-lookup"><span data-stu-id="486f7-114">You may already have installed Report Builder to create reports for an SSRS server.</span></span> <span data-ttu-id="486f7-115">คุณสามารถใช้รุ่นเดียวกัน หรือใช้ตัวสร้างรายงานเพื่อสร้างรายงานสำหรับเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="486f7-115">You can use the same version or Report Builder to create reports for Power BI Report Server.</span></span> <span data-ttu-id="486f7-116">ถ้าคุณยังไม่ได้ทำการติดตั้ง คุณสามารถติดตั้งได้ง่ายๆ</span><span class="sxs-lookup"><span data-stu-id="486f7-116">If you haven't installed it, the process is easy.</span></span>

1. <span data-ttu-id="486f7-117">ในเว็บพอร์ทัลเซิร์ฟเวอร์ Power BI เลือก**สร้างรายงาน** > **แบบแบ่งหน้าใหม่**</span><span class="sxs-lookup"><span data-stu-id="486f7-117">In the Power BI Report Server web portal, select **New** > **Paginated Report**.</span></span>
   
    ![เมนูสำหรับรายงานแบบแบ่งหน้าใหม่](media/quickstart-create-paginated-report/reportserver-new-paginated-report-menu.png)
   
    <span data-ttu-id="486f7-119">หากคุณไม่ได้ติดตั้งตัวสร้างรายงานอยู่แล้ว ตัวช่วยสร้างตัวสร้างรายงานของ Microsoft จะเริ่มทำงาน</span><span class="sxs-lookup"><span data-stu-id="486f7-119">If you don't have Report Builder installed already, the Microsoft Report Builder Wizard starts.</span></span>  
  
3.  <span data-ttu-id="486f7-120">ยอมรับข้อกำหนดในข้อตกลงสิทธิการใช้งาน > **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="486f7-120">Accept the terms in the license agreement > **Next**.</span></span>  
 
5.  <span data-ttu-id="486f7-121">เลือก **ติดตั้ง** เพื่อดำเนินการติดตั้งตัวสร้างรายงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="486f7-121">Select **Install** to complete the installation of Report Builder.</span></span>  

2. <span data-ttu-id="486f7-122">หลังจากติดตั้งแล้ว “ตัวสร้างรายงาน” จะเปิดขึ้นใน**หน้าจอชุดข้อมูลหรือ**รายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="486f7-122">After it's installed, Report Builder opens to the **New Report or Dataset** screen.</span></span>
   
    ![หน้าจอชุดข้อมูลหรือรายงานใหม่](media/quickstart-create-paginated-report/reportserver-paginated-new-report-screen.png)
 

##  <a name="install-report-builder-from-the-download-center"></a><a name="download"></a> <span data-ttu-id="486f7-124">ติดตั้งตัวสร้างรายงานจากศูนย์ดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="486f7-124">Install Report Builder from the Download Center</span></span>  
  
1.  <span data-ttu-id="486f7-125">บน [หน้าตัวสร้างรายงานของศูนย์ดาวน์โหลดของ Microsoft](https://go.microsoft.com/fwlink/?LinkID=734968) เลือก **ดาวน์โหลด**</span><span class="sxs-lookup"><span data-stu-id="486f7-125">On  the [Report Builder page of the Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkID=734968) , select **Download**.</span></span>  
  
2.  <span data-ttu-id="486f7-126">หลังจากตัวสร้างรายงานดาวน์โหลดเสร็จสิ้นแล้ว เลือก  **เรียกใช้**</span><span class="sxs-lookup"><span data-stu-id="486f7-126">After Report Builder has finished downloading, select  **Run**.</span></span>  
  
     <span data-ttu-id="486f7-127">ตัวช่วยสร้างตัวสร้างรายงานของ Microsoft จะเริ่มทำงาน</span><span class="sxs-lookup"><span data-stu-id="486f7-127">The Microsoft Report Builder Wizard starts.</span></span>  
  
3.  <span data-ttu-id="486f7-128">ยอมรับข้อกำหนดในข้อตกลงสิทธิการใช้งาน > **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="486f7-128">Accept the terms in the license agreement > **Next**.</span></span>  
 
5.  <span data-ttu-id="486f7-129">เลือก **ติดตั้ง** เพื่อดำเนินการติดตั้งตัวสร้างรายงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="486f7-129">Select **Install** to complete the installation of Report Builder.</span></span>  
 

## <a name="next-steps"></a><span data-ttu-id="486f7-130">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="486f7-130">Next steps</span></span>

[<span data-ttu-id="486f7-131">เซิร์ฟเวอร์รายงาน Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="486f7-131">What is Power BI Report Server?</span></span>](get-started.md)
