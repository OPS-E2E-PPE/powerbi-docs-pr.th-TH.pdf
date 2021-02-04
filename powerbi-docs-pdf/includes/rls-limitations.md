---
author: davidiseminger
ms.service: powerbi
ms.topic: include
ms.date: 01/31/2020
ms.author: davidi
ms.openlocfilehash: 912b0213c328c623e7881f7f30fe7d67f6d889b3
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/13/2020
ms.locfileid: "83274659"
---
## <a name="limitations"></a><span data-ttu-id="e4ebd-101">ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="e4ebd-101">Limitations</span></span>

<span data-ttu-id="e4ebd-102">ข้อจำกัดปัจจุบันสำหรับการรักษาความปลอดภัยระดับแถวบนโมเดลระบบคลาวด์ มีดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e4ebd-102">The current limitations for row-level security on cloud models are as follows:</span></span>

* <span data-ttu-id="e4ebd-103">ถ้าก่อนหน้านี้คุณได้กำหนดบทบาทและกฎในบริการ Power BI แล้ว คุณต้องสร้างขึ้นใหม่ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e4ebd-103">If you previously defined roles and rules in the Power BI service, you must re-create them in Power BI Desktop.</span></span>

* <span data-ttu-id="e4ebd-104">คุณสามารถกำหนด RLS บนชุดข้อมูลที่สร้างขึ้นด้วย Power BI Desktop เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e4ebd-104">You can define RLS only on the datasets created with Power BI Desktop.</span></span> <span data-ttu-id="e4ebd-105">ถ้าคุณต้องการเปิดใช้งาน RLS สำหรับชุดข้อมูลที่สร้างขึ้นโดยใช้ Excel คุณจะต้องแปลงไฟล์ของคุณให้เป็นไฟล์ Power BI Desktop (PBIX) ก่อน</span><span class="sxs-lookup"><span data-stu-id="e4ebd-105">If you want to enable RLS for datasets created with Excel, you must convert your files into Power BI Desktop (PBIX) files first.</span></span> <span data-ttu-id="e4ebd-106">[เรียนรู้เพิ่มเติม](../connect-data/desktop-import-excel-workbooks.md)</span><span class="sxs-lookup"><span data-stu-id="e4ebd-106">[Learn more](../connect-data/desktop-import-excel-workbooks.md).</span></span>

* <span data-ttu-id="e4ebd-107">สนับสนุนเฉพาะการนำเข้าและการเชื่อมต่อ DirectQuery เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e4ebd-107">Only Import and DirectQuery connections are supported.</span></span> <span data-ttu-id="e4ebd-108">Live connection ไปถึง Analysis Services ได้รับการจัดการในแบบจำลองแบบภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="e4ebd-108">Live connections to Analysis Services are handled in the on-premises model.</span></span>

## <a name="known-issues"></a><span data-ttu-id="e4ebd-109">ปัญหาที่ทราบแล้ว</span><span class="sxs-lookup"><span data-stu-id="e4ebd-109">Known issues</span></span>

<span data-ttu-id="e4ebd-110">มีปัญหาที่รู้จัก ที่คุณจะได้รับข้อความแสดงข้อผิดพลาด หากคุณพยายามเผยแพร่รายงานที่เผยแพร่แล้วก่อนหน้านี้จาก Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e4ebd-110">There's a known issue where you'll get an error message if you try to publish a previously published report from Power BI Desktop.</span></span> <span data-ttu-id="e4ebd-111">ต่อไปนี้คือสถานการณ์สมมติ:</span><span class="sxs-lookup"><span data-stu-id="e4ebd-111">The scenario is as follows:</span></span>

1. <span data-ttu-id="e4ebd-112">แอนนามีชุดข้อมูลที่เผยแพร่ไปยังบริการ Power BI และมีการกำหนดค่า RLS แล้ว</span><span class="sxs-lookup"><span data-stu-id="e4ebd-112">Anna has a dataset that is published to the Power BI service and has configured RLS.</span></span>

1. <span data-ttu-id="e4ebd-113">เมื่อแอนนาทำการปรับปรุงรายงานใน Power BI Desktop และเผยแพร่อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="e4ebd-113">Anna updates the report in Power BI Desktop and republishes.</span></span>

1. <span data-ttu-id="e4ebd-114">Anna ได้รับข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="e4ebd-114">Anna receives an error.</span></span>

<span data-ttu-id="e4ebd-115">**วิธีแก้ปัญหา:** เผยแพร่ไฟล์ Power BI Desktop จากบริการ Power BI อีกครั้งจนกว่าปัญหานี้ได้รับการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="e4ebd-115">**Workaround:** Republish the Power BI Desktop file from the Power BI service until this issue is resolved.</span></span> <span data-ttu-id="e4ebd-116">คุณสามารถทำได้โดยการเลือก **รับข้อมูล** > **ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="e4ebd-116">You can do that by selecting **Get Data** > **Files**.</span></span>

