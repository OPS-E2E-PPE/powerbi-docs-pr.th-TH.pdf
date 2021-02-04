---
title: 'บทช่วยสอน: สำรวจ Power BI Report Server ใน VM'
description: ในบทช่วยสอนนี้ คุณสร้างเครื่องเสมือนที่มีการติดตั้ง Power BI Report Server แล้ว และสำรวจพอร์ทัลเว็บได้
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: tutorial
ms.date: 05/06/2019
ms.openlocfilehash: 85fcd6249a833c35cb98fca6abf2881ab1a4bf7e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418428"
---
# <a name="tutorial-explore-the-power-bi-report-server-web-portal-in-a-vm"></a><span data-ttu-id="c0c2e-103">บทช่วยสอน: สำรวจพอร์ทัลเว็บ Power BI Report Server ใน VM</span><span class="sxs-lookup"><span data-stu-id="c0c2e-103">Tutorial: Explore the Power BI Report Server web portal in a VM</span></span>
<span data-ttu-id="c0c2e-104">ในบทช่วยสอนนี้ คุณสร้างเครื่องเสมือน Azure ที่มีการติดตั้ง Power BI Report Server ไว้แล้วได้ ดังนั้นคุณสามารถดู แก้ไข และจัดการตัวอย่าง Power BI และรายงานที่มีการแบ่งหน้า และ KPI ได้</span><span class="sxs-lookup"><span data-stu-id="c0c2e-104">In this tutorial, you create an Azure virtual machine with Power BI Report Server already installed, so you can experience viewing, editing, and managing sample Power BI and paginated reports, and KPIs.</span></span>

![พอร์ทัลของเว็บเซิร์ฟเวอร์รายงาน](media/tutorial-explore-report-server-web-portal/power-bi-report-server-browser-in-vm-no-numbers.png)

<span data-ttu-id="c0c2e-106">นี่คืองานที่คุณต้องทำในบทช่วยสอนนี้:</span><span class="sxs-lookup"><span data-stu-id="c0c2e-106">Here are the tasks you'll do in this tutorial:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="c0c2e-107">สร้างและเชื่อมต่อกับ VM</span><span class="sxs-lookup"><span data-stu-id="c0c2e-107">Create and connect to a VM</span></span>
> * <span data-ttu-id="c0c2e-108">เริ่มและสำรวจพอร์ทัลเว็บ Power BI Report Server</span><span class="sxs-lookup"><span data-stu-id="c0c2e-108">Start and explore the Power BI Report Server web portal</span></span>
> * <span data-ttu-id="c0c2e-109">ติดแท็กรายการที่คุณชื่นชอบ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-109">Tag a favorite item</span></span>
> * <span data-ttu-id="c0c2e-110">ดูและแก้ไขรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="c0c2e-110">View and edit a Power BI report</span></span>
> * <span data-ttu-id="c0c2e-111">ดู จัดการ และแก้ไขรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="c0c2e-111">View, manage, and edit a paginated report</span></span>
> * <span data-ttu-id="c0c2e-112">ดูเวิร์กบุ๊ก Excel ใน Excel Online</span><span class="sxs-lookup"><span data-stu-id="c0c2e-112">View an Excel workbook in Excel Online</span></span>

<span data-ttu-id="c0c2e-113">สำหรับบทช่วยสอนนี้ คุณจำเป็นต้องมีการสมัครใช้งาน Azure</span><span class="sxs-lookup"><span data-stu-id="c0c2e-113">For this tutorial, you need an Azure subscription.</span></span> <span data-ttu-id="c0c2e-114">ถ้าคุณยังไม่มีการสมัครใช้งาน Azure สร้าง[บัญชีฟรี](https://azure.microsoft.com/free/?WT.mc_id=A261C142F)ก่อนที่คุณจะเริ่ม</span><span class="sxs-lookup"><span data-stu-id="c0c2e-114">If you don’t have one, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>

## <a name="create-a-power-bi-report-server-vm"></a><span data-ttu-id="c0c2e-115">สร้าง Power BI Report Server VM</span><span class="sxs-lookup"><span data-stu-id="c0c2e-115">Create a Power BI Report Server VM</span></span>

<span data-ttu-id="c0c2e-116">โชคดีที่ทีม Power BI ได้สร้าง VM ที่มาพร้อมกับ Power BI Report Server แบบติดตั้งไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="c0c2e-116">Luckily, the Power BI team has created a VM that comes with Power BI Report Server already installed.</span></span>

1. <span data-ttu-id="c0c2e-117">ใน Azure Marketplace เลือกเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="c0c2e-117">In the Azure Marketplace, select Power BI Report Server.</span></span> <span data-ttu-id="c0c2e-118">ลิงก์นี้จะเปิดขึ้นโดยตรง: [เซิร์ฟเวอร์รายงาน Power BI](https://azuremarketplace.microsoft.com/marketplace/apps/reportingservices.technical-preview?tab=Overview)</span><span class="sxs-lookup"><span data-stu-id="c0c2e-118">This link opens it directly: [Power BI Report Server](https://azuremarketplace.microsoft.com/marketplace/apps/reportingservices.technical-preview?tab=Overview).</span></span>  

2. <span data-ttu-id="c0c2e-119">เลือก **รับทันที**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-119">Select **Get it now**.</span></span>
3. <span data-ttu-id="c0c2e-120">ในการยอมรับข้อตกลงการใช้งานและนโยบายความเป็นส่วนตัวของผู้ให้บริการ เลือก **ดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-120">To agree to the provider's terms of use and privacy policy, select **Continue**.</span></span>

4. <span data-ttu-id="c0c2e-121">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-121">Select **Create**.</span></span>

    ![สร้าง Power BI Report Server VM](media/tutorial-explore-report-server-web-portal/power-bi-report-server-create.png)

5. <span data-ttu-id="c0c2e-123">ใน **ขั้นตอนที่ 1 ข้อมูลพื้นฐาน** สำหรับ **ชื่อ VM** เรียกว่า **reportservervm**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-123">In **Step 1 Basics**, for **VM Name**, call it **reportservervm**.</span></span>

    <span data-ttu-id="c0c2e-124">ชื่อ Power BI Report Server VM ไม่สามารถมีเครื่องหมายขีดคั่นได้</span><span class="sxs-lookup"><span data-stu-id="c0c2e-124">The Power BI Report Server VM name can't contain dashes.</span></span>

5. <span data-ttu-id="c0c2e-125">สร้างชื่อผู้ใช้และรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="c0c2e-125">Create a user name and password.</span></span>

6. <span data-ttu-id="c0c2e-126">สำหรับ **กลุ่มทรัพยากร** เลือก **สร้างใหม่** ต่อไป และเรียกว่า **reportserverresourcegroup** > **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-126">For **Resource group**, select **Create new**, and call it **reportserverresourcegroup** > **OK**.</span></span>

    <span data-ttu-id="c0c2e-127">ถ้าคุณเลื่อนผ่านบทช่วยสอนมากกว่าหนึ่งครั้ง คุณจำเป็นต้องตั้งชื่อกลุ่มทรัพยากรเป็นชื่ออื่นหลังจากครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="c0c2e-127">If you go through the tutorial more than once, you need to give the resource group a different name after the first time.</span></span> <span data-ttu-id="c0c2e-128">คุณไม่สามารถใช้ชื่อกลุ่มทรัพยากรเดียวกันสองครั้งในการสมัครใช้งานหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c0c2e-128">You can't use the same resource group name twice in one subscription.</span></span> 

    ![ตั้งชื่อ VM และกลุ่มทรัพยากร](media/tutorial-explore-report-server-web-portal/power-bi-report-server-create-resource-group.png)

7. <span data-ttu-id="c0c2e-130">ใช้ค่าเริ่มต้นอื่น ๆ ต่อไป > **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-130">Keep the other defaults > **OK**.</span></span>

8. <span data-ttu-id="c0c2e-131">ใน **ขั้นตอนที่ 2 การตั้งค่า** ใช้ค่าเริ่มต้นต่อไป > **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-131">In **Step 2 Settings**, keep the defaults > **OK**.</span></span>
 
    <span data-ttu-id="c0c2e-132">บัญชี **ที่เก็บข้อมูล SQL** และ **ค่าบัญชีที่เก็บข้อมูลการวินิจฉัย** ต้องไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="c0c2e-132">The **SQL Storage account** and **Diagnostics Storage account** values must also be unique.</span></span> <span data-ttu-id="c0c2e-133">ถ้าคุณเลื่อนผ่านบทช่วยสอนมากกว่าหนึ่งครั้ง คุณจำเป็นต้องตั้งเป็นชื่ออื่น</span><span class="sxs-lookup"><span data-stu-id="c0c2e-133">If you go through the tutorial more than once, you need to give them different names.</span></span>

9. <span data-ttu-id="c0c2e-134">ใน **สรุปขั้นตอนที่ 3** ตรวจสอบการเลือกของคุณ >**ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-134">In **Step 3 Summary**, review your selections > **OK**.</span></span>

10. <span data-ttu-id="c0c2e-135">ใน **ขั้นตอนซื้อที่ 4** ตรวจทานข้อกำหนดของนโยบายผู้ใช้และความเป็นส่วนตัว > **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-135">In **Step 4 Buy**, review the Terms of user and privacy policy > **Create**.</span></span>

    <span data-ttu-id="c0c2e-136">กระบวนการ **ส่งการปรับใช้สำหรับเซิร์ฟเวอร์รายงาน Power BI** อาจใช้เวลาหลายนาที</span><span class="sxs-lookup"><span data-stu-id="c0c2e-136">The **Submitting deployment for Power BI Report Server** process may take several minutes.</span></span>

## <a name="connect-to-your-virtual-machine"></a><span data-ttu-id="c0c2e-137">เชื่อมต่อกับเครื่องเสมือนของคุณ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-137">Connect to your virtual machine</span></span>

1. <span data-ttu-id="c0c2e-138">ในแผงนำทาง Azure ให้เลือก **เครื่องเสมือน**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-138">In the Azure nav pane, select **Virtual machines**.</span></span> 

2. <span data-ttu-id="c0c2e-139">ในกล่อง **กรองตามชื่อ** พิมพ์ "รายงาน"</span><span class="sxs-lookup"><span data-stu-id="c0c2e-139">In the **Filter by name** box, type "report".</span></span> 

3. <span data-ttu-id="c0c2e-140">เลือก VM ที่ชื่อว่า **REPORTSERVERVM**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-140">Select the VM named **REPORTSERVERVM**.</span></span>

    ![ดูเครื่องเสมือน](media/tutorial-explore-report-server-web-portal/power-bi-report-server-view-virtual-machine.png)

4. <span data-ttu-id="c0c2e-142">ใต้เครื่องเสมือน REPORTSERVERVM เลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-142">Under REPORTSERVERVM Virtual machine, select **Connect**.</span></span>

    ![เชื่อมต่อกับเครื่องเสมือน](media/tutorial-explore-report-server-web-portal/power-bi-report-server-connect-to-virtual-machine.png)

5. <span data-ttu-id="c0c2e-144">ในบานหน้าต่าง **เชื่อมต่อกับเครื่องเสมือน** ให้เก็บค่าเริ่มต้นและเลือก **ดาวน์โหลดไฟล์ RDP**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-144">In the **Connect to virtual machine** pane, keep the defaults and select **Download RDP File**.</span></span>

1. <span data-ttu-id="c0c2e-145">ในกล่องโต้ตอบการ **เชื่อมต่อเดสก์ท็อประยะไกล** เลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-145">In the **Remote Desktop Connection** dialog box, select **Connect**.</span></span>

6. <span data-ttu-id="c0c2e-146">ใส่ชื่อและรหัสผ่านที่คุณสร้างขึ้นสำหรับการ VM > **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-146">Enter the name and password you created for the VM > **OK**.</span></span>

7. <span data-ttu-id="c0c2e-147">กล่องโต้ตอบถัดไประบุว่า **ไม่สามารถระบุข้อมูลประจำตัวของคอมพิวเตอร์ระยะไกลได้**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-147">The next dialog box says **The identity of the remote computer cannot be identified**.</span></span> <span data-ttu-id="c0c2e-148">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-148">Select **Yes**.</span></span>

   <span data-ttu-id="c0c2e-149">Voila, VM ใหม่ของคุณเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="c0c2e-149">Voila, your new VM opens.</span></span>

## <a name="power-bi-report-server-on-the-vm"></a><span data-ttu-id="c0c2e-150">เซิร์ฟเวอร Power BI Report บน VM</span><span class="sxs-lookup"><span data-stu-id="c0c2e-150">Power BI Report Server on the VM</span></span>

<span data-ttu-id="c0c2e-151">เมื่อ VM ของคุณเปิดขึ้น ต่อไปนี้คือรายการที่คุณเห็นบนเดสก์ท็อป</span><span class="sxs-lookup"><span data-stu-id="c0c2e-151">When your VM opens, here are the items you see on the desktop.</span></span>

![เครื่องเสมือนของเซิร์ฟเวอร์รายงานของ Power BI เริ่มต้นขึ้น](media/tutorial-explore-report-server-web-portal/power-bi-report-server-vm-5-numbers.png)

|<span data-ttu-id="c0c2e-153">ตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c0c2e-153">Number</span></span>  |<span data-ttu-id="c0c2e-154">คืออะไร</span><span class="sxs-lookup"><span data-stu-id="c0c2e-154">What it is</span></span>  |
|---------|---------|
|![เลขที่ 1](media/tutorial-explore-report-server-web-portal/number-1.png) | <span data-ttu-id="c0c2e-156">รายงาน Power BI ตัวอย่าง (.PBIX)</span><span class="sxs-lookup"><span data-stu-id="c0c2e-156">Sample Power BI (.PBIX) reports</span></span> |
|![เลขที่ 2](media/tutorial-explore-report-server-web-portal/number-2.png) | <span data-ttu-id="c0c2e-158">ลิงก์ไปยังเอกสารประกอบเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="c0c2e-158">Links to Power BI Report Server documentation</span></span> |
|![เลขที่ 3](media/tutorial-explore-report-server-web-portal/number-3.png) | <span data-ttu-id="c0c2e-160">เริ่มต้น Power BI Desktop ที่ปรับให้เหมาะสมสำหรับเซิร์ฟเวอร์รายงาน Power BI (มกราคม 2019)</span><span class="sxs-lookup"><span data-stu-id="c0c2e-160">Starts Power BI Desktop optimized for Power BI Report Server (January 2019)</span></span> |
|![เลขที่ 4](media/tutorial-explore-report-server-web-portal/number-4.png) | <span data-ttu-id="c0c2e-162">พอร์ทัลเว็บเซิร์ฟเวอร์รายงาน Power BI เปิดขึ้นในเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="c0c2e-162">Opens Power BI Report Server web portal in the browser</span></span> |
|![เลขที่ 5](media/tutorial-explore-report-server-web-portal/number-5.png) | <span data-ttu-id="c0c2e-164">เริ่มต้นเครื่องมือข้อมูล SQL Server สำหรับสร้างรายงานที่มีการแบ่งหน้า (.RDL)</span><span class="sxs-lookup"><span data-stu-id="c0c2e-164">Starts SQL Server Data Tools, for creating paginated (.RDL) reports</span></span> |

<span data-ttu-id="c0c2e-165">ดับเบิลคลิกที่ไอคอน **พอร์ทัลเว็บเซิร์ฟเวอร์รายงาน**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-165">Double-click the **Report Server Web Portal** icon.</span></span> <span data-ttu-id="c0c2e-166">เบราว์เซอร์เปิดขึ้น`https://localhost/reports/browse`</span><span class="sxs-lookup"><span data-stu-id="c0c2e-166">The browser opens `https://localhost/reports/browse`.</span></span> <span data-ttu-id="c0c2e-167">ในพอร์ทัลเว็บคุณจะเห็นไฟล์ต่าง ๆ ที่ถูกจัดกลุ่มแยกตามประเภท</span><span class="sxs-lookup"><span data-stu-id="c0c2e-167">In the web portal, you see various files grouped by type.</span></span> 

![พอร์ทัลเว็บของ Power BI Report Server](media/tutorial-explore-report-server-web-portal/power-bi-report-server-browser-in-vm.png)

|<span data-ttu-id="c0c2e-169">ตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c0c2e-169">Number</span></span>  |<span data-ttu-id="c0c2e-170">คืออะไร</span><span class="sxs-lookup"><span data-stu-id="c0c2e-170">What it is</span></span>  |
|---------|---------|
|![เลขที่ 1](media/tutorial-explore-report-server-web-portal/number-1.png) | <span data-ttu-id="c0c2e-172">KPI ที่สร้างขึ้นในพอร์ทัลเว็บ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-172">KPIs created in the web portal</span></span> |
|![เลขที่ 2](media/tutorial-explore-report-server-web-portal/number-2.png) |  <span data-ttu-id="c0c2e-174">รายงาน Power BI (.PBIX)</span><span class="sxs-lookup"><span data-stu-id="c0c2e-174">Power BI (.PBIX) reports</span></span>  |
|![เลขที่ 3](media/tutorial-explore-report-server-web-portal/number-3.png) | <span data-ttu-id="c0c2e-176">รายงานมือถือที่สร้างขึ้นใน SQL Server Mobile Report Publisher</span><span class="sxs-lookup"><span data-stu-id="c0c2e-176">Mobile reports created in SQL Server Mobile Report Publisher</span></span>  |
|![เลขที่ 4](media/tutorial-explore-report-server-web-portal/number-4.png) |  <span data-ttu-id="c0c2e-178">รายงานที่มีการแบ่งหน้าที่สร้างขึ้นในตัวสร้างรายงานหรือเครื่องมือข้อมูล SQL Server</span><span class="sxs-lookup"><span data-stu-id="c0c2e-178">Paginated reports created in Report Builder or SQL Server Data Tools</span></span>  |
|![เลขที่ 5](media/tutorial-explore-report-server-web-portal/number-5.png) | <span data-ttu-id="c0c2e-180">เวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="c0c2e-180">Excel workbooks</span></span>   | 
|![เลขที่ 6](media/tutorial-explore-report-server-web-portal/number-6.png) | <span data-ttu-id="c0c2e-182">แหล่งข้อมูลสำหรับรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="c0c2e-182">Data sources for paginated reports</span></span> | 


## <a name="tag-your-favorites"></a><span data-ttu-id="c0c2e-183">แท็กรายการโปรดของคุณ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-183">Tag your favorites</span></span>
<span data-ttu-id="c0c2e-184">คุณสามารถแท็กรายงานและ KPI ที่คุณต้องการทำให้เป็นรายการโปรด</span><span class="sxs-lookup"><span data-stu-id="c0c2e-184">You can tag the reports and KPIs that you want to be favorites.</span></span> <span data-ttu-id="c0c2e-185">ง่ายต่อการค้นหาเนื่องจากทั้งหมดถูกรวบรวมไว้ในโฟลเดอร์รายการโปรดเดียว ทั้งในพอร์ทัลของเว็บ และในแอป Power BI สำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="c0c2e-185">They're easier to find because they're all gathered in a single Favorites folder, both in the web portal and in the Power BI mobile apps.</span></span> 

1. <span data-ttu-id="c0c2e-186">เลือกจุดไข่ปลา ( **...** ) ที่มุมขวาบนของ **อัตราผลกำไร** KPI > **เพิ่มไปยังรายการโปรด**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-186">Select the ellipsis (**…**) in the upper-right corner of the **Profit Margin** KPI > **Add to Favorites**.</span></span>
   
    ![เพิ่มในรายการโปรด](media/tutorial-explore-report-server-web-portal/power-bi-report-server-add-to-favorites.png)
2. <span data-ttu-id="c0c2e-188">เลือก **รายการโปรด** บน Ribbon พอร์ทัลของเว็บเพื่อดูพร้อมกับรายการโปรดอื่นๆ ของคุณบนหน้ารายการโปรดในพอร์ทัลของเว็บ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-188">Select **Favorites** on the web portal ribbon to see it along with your other favorites on the Favorites page in the web portal.</span></span>
   
    ![ดูรายการโปรด](media/tutorial-explore-report-server-web-portal/power-bi-report-server-favorites.png)

3. <span data-ttu-id="c0c2e-190">เลือก **เรียกดู** เพื่อกลับไปยังพอร์ทัลเว็บ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-190">Select **Browse** to go back to the web portal.</span></span>
   
## <a name="view-items-in-list-view"></a><span data-ttu-id="c0c2e-191">ดูรายการในมุมมองรายการ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-191">View items in List view</span></span>
<span data-ttu-id="c0c2e-192">ตามค่าเริ่มต้น พอร์ทัลของเว็บจะแสดงเนื้อหาในมุมมองไทล์</span><span class="sxs-lookup"><span data-stu-id="c0c2e-192">By default, the web portal displays its contents in Tile view.</span></span>

<span data-ttu-id="c0c2e-193">คุณสามารถสลับเป็นมุมมองรายการ ซึ่งเป็นเรื่องง่ายเมื่อต้องย้าย หรือลบหลายรายการในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="c0c2e-193">You can switch to List view, where it's easy to move or delete multiple items at a time.</span></span> 

1. <span data-ttu-id="c0c2e-194">เลือก **รายการ** > **ไทล์**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-194">Select **Tiles** > **List**.</span></span>
   
    ![สลับมุมมอง](media/tutorial-explore-report-server-web-portal/report-server-web-portal-list-view.png)

2. <span data-ttu-id="c0c2e-196">ย้อนกลับไปยังมุมมองไทล์: เลือก **รายการ** > **ไทล์**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-196">Go back to Tiles view: Select **List** > **Tiles**.</span></span>

## <a name="power-bi-reports"></a><span data-ttu-id="c0c2e-197">รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="c0c2e-197">Power BI reports</span></span>

<span data-ttu-id="c0c2e-198">คุณสามารถดูและโต้ตอบกับรายงาน Power BI ในพอร์ทัลเว็บ และเริ่มต้น Power BI Desktop ได้โดยตรงจากพอร์ทัลเว็บ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-198">You can view and interact with Power BI reports in the web portal, and start Power BI Desktop right from the web portal.</span></span>

### <a name="view-power-bi-reports"></a><span data-ttu-id="c0c2e-199">ดูรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="c0c2e-199">View Power BI reports</span></span>

1. <span data-ttu-id="c0c2e-200">ในพอร์ทัลเว็บใต้ **รายงาน Power BI** เลือก **รายงานภาพรวมของลูกค้าตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-200">In the web portal under **Power BI reports**, select **Sample Customer Overview Report**.</span></span> <span data-ttu-id="c0c2e-201">รายงานเปิดขึ้นในเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="c0c2e-201">The report opens in the browser.</span></span>

1. <span data-ttu-id="c0c2e-202">เลือกช่วงสหรัฐอเมริกาในแผนภูมิต้นไม้เพื่อดูวิธีดังกล่าวไฮไลต์ค่าที่เกี่ยวข้องในภาพอื่น</span><span class="sxs-lookup"><span data-stu-id="c0c2e-202">Select the United States block in the tree map to see how it highlights related values in the other visuals.</span></span>

    ![รายงาน Power BI ที่ทำไฮไลท์](media/tutorial-explore-report-server-web-portal/power-bi-report-server-power-bi.png)

### <a name="edit-in-power-bi-desktop"></a><span data-ttu-id="c0c2e-204">แก้ไขใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="c0c2e-204">Edit in Power BI Desktop</span></span>

1. <span data-ttu-id="c0c2e-205">เลือก **แก้ไขใน Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-205">Select **Edit in Power BI Desktop**.</span></span>

1. <span data-ttu-id="c0c2e-206">เลือก **อนุญาต** เพื่ออนุญาตให้เว็บไซต์นี้เปิดโปรแกรมบนคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-206">Select **Allow** to allow this web site to open a program on your computer.</span></span> 

     <span data-ttu-id="c0c2e-207">หน้ารายงานเปิดขึ้นใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="c0c2e-207">The report opens in Power BI Desktop.</span></span> <span data-ttu-id="c0c2e-208">โปรดสังเกตชื่อในแถบด้านบน "Power BI Desktop (มกราคม 2019)"</span><span class="sxs-lookup"><span data-stu-id="c0c2e-208">Note the name in the top bar, "Power BI Desktop (January 2019)".</span></span> <span data-ttu-id="c0c2e-209">นี่เป็นเวอร์ชันที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="c0c2e-209">That's the version optimized for Power BI Report Server.</span></span>

    <span data-ttu-id="c0c2e-210">ใช้เวอร์ชัน Power BI Desktop ที่ติดตั้งไว้บน VM</span><span class="sxs-lookup"><span data-stu-id="c0c2e-210">Use the version of Power BI Desktop that's installed on the VM.</span></span> <span data-ttu-id="c0c2e-211">คุณไม่สามารถอัปโหลดรายงานข้ามโดเมนได้</span><span class="sxs-lookup"><span data-stu-id="c0c2e-211">You can't go across domains to upload a report.</span></span>

3. <span data-ttu-id="c0c2e-212">ในบานหน้าต่างเขตข้อมูล ขยายตารางลูกค้าและลากเขตข้อมูลอาชีพไปยังตัวกรองระดับรายงาน</span><span class="sxs-lookup"><span data-stu-id="c0c2e-212">In the Fields pane, expand the Customers table and drag the Occupation field to Report level filters.</span></span>

    ![ลากเขตข้อมูลหนึ่งไปยังบานหน้าต่างตัวกรอง](media/tutorial-explore-report-server-web-portal/power-bi-report-server-desktop-filter.png)

1. <span data-ttu-id="c0c2e-214">บันทึกรายงาน</span><span class="sxs-lookup"><span data-stu-id="c0c2e-214">Save the report.</span></span>

1. <span data-ttu-id="c0c2e-215">กลับไปยังรายงานในเบราว์เซอร์แล้วเลือกไอคอน **รีเฟรช** เบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="c0c2e-215">Go back to the report in the browser and select the browser **Refresh** icon.</span></span>

    ![ไอคอนรีเฟรชเบราว์เซอร์](media/tutorial-explore-report-server-web-portal/power-bi-report-server-browser-refresh.png)

8. <span data-ttu-id="c0c2e-217">ขยายบานหน้าต่าง **ตัวกรอง** ทางด้านขวาเพื่อดูตัวกรอง **อาชีพ** ที่คุณเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="c0c2e-217">Expand the **Filters** pane on the right to see the **Occupation** filter you added.</span></span> <span data-ttu-id="c0c2e-218">เลือก **Professional**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-218">Select **Professional**.</span></span>

    ![รายงาน Power BI ที่กรองแล้ว](media/tutorial-explore-report-server-web-portal/power-bi-report-server-power-bi-filtered.png)

3. <span data-ttu-id="c0c2e-220">เลือก **เรียกดู** เพื่อกลับไปยังพอร์ทัลเว็บ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-220">Select **Browse** to go back to the web portal.</span></span>

## <a name="paginated-rdl-reports"></a><span data-ttu-id="c0c2e-221">รายงานที่มีการแบ่งหน้า (.RDL)</span><span class="sxs-lookup"><span data-stu-id="c0c2e-221">Paginated (.RDL) reports</span></span>

<span data-ttu-id="c0c2e-222">คุณสามารถดูและจัดการรายงานที่มีการแบ่งหน้าและเปิดใช้ตัวสร้างรายงาน จากพอร์ทัลเว็บได้</span><span class="sxs-lookup"><span data-stu-id="c0c2e-222">You can view and manage paginated reports, and launch Report Builder, from the web portal.</span></span>

### <a name="manage-a-paginated-report"></a><span data-ttu-id="c0c2e-223">จัดการรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="c0c2e-223">Manage a paginated report</span></span>

1. <span data-ttu-id="c0c2e-224">ในพอร์ทัลเว็บใต้ **รายงานที่มีการแบ่งหน้า** ให้เลือก **ตัวเลือกเพิ่มเติม** (...) ถัดจาก **ใบสั่งขาย** > **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-224">In the web portal under **Paginated reports**, select **More options** (...) next to **Sales Order** > **Manage**.</span></span>

1. <span data-ttu-id="c0c2e-225">เลือก **พารามิเตอร์** เปลี่ยนค่าเริ่มต้นสำหรับ **SalesOrderNumber** เป็น **SO50689** > **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-225">Select **Parameters**, change the default value for **SalesOrderNumber** to **SO50689** > **Apply**.</span></span>

   ![ตั้งค่าพารามิเตอร์รายงาน](media/tutorial-explore-report-server-web-portal/power-bi-report-server-set-parameters.png)

3. <span data-ttu-id="c0c2e-227">เลือก **เรียกดู** เพื่อกลับไปยังพอร์ทัลเว็บ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-227">Select **Browse** to go back to the web portal.</span></span>

### <a name="view-a-paginated-report"></a><span data-ttu-id="c0c2e-228">ดูรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="c0c2e-228">View a paginated report</span></span>

1. <span data-ttu-id="c0c2e-229">เลือก **ใบสั่งซื้อ** ในพอร์ทัลเว็บ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-229">Select **Sales Order** in the web portal.</span></span>
 
3.  <span data-ttu-id="c0c2e-230">คุณจะเห็นว่าเปิดไปยังพารามิเตอร์ **คำสั่งซื้อ** ที่คุณตั้งค่า **SO50689**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-230">You see it opened to the **Order** parameter you set, **SO50689**.</span></span> 

    ![พารามิเตอร์รายงานที่มีการแบ่งหน้า](media/tutorial-explore-report-server-web-portal/power-bi-report-server-paginated.png)

    <span data-ttu-id="c0c2e-232">คุณสามารถเปลี่ยนพารามิเตอร์ได้ที่นี่พร้อมกับพารามิเตอร์อื่น ๆ โดยไม่ต้องเปลี่ยนค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c0c2e-232">You can change that parameter here, along with the other parameters, without changing the defaults.</span></span>

1. <span data-ttu-id="c0c2e-233">เลือก **คำสั่ง** **SO48339** > **ดูรายงาน**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-233">Select **Order** **SO48339** > **View Report**.</span></span>

4. <span data-ttu-id="c0c2e-234">คุณจะเห็นว่านี่คือหน้า 1 จาก 2 หน้า</span><span class="sxs-lookup"><span data-stu-id="c0c2e-234">You see that this is page 1 of 2.</span></span> <span data-ttu-id="c0c2e-235">เลือกลูกศรขวาเพื่อดูหน้าที่สอง</span><span class="sxs-lookup"><span data-stu-id="c0c2e-235">Select the right arrow to see the second page.</span></span> <span data-ttu-id="c0c2e-236">ตารางมีต่อไปยังหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="c0c2e-236">The table continues on that page.</span></span>

    ![รายงานที่มีการแบ่งหน้า หน้า 2 จาก 2 หน้า](media/tutorial-explore-report-server-web-portal/power-bi-report-server-paginated-2-of-2.png)

5. <span data-ttu-id="c0c2e-238">เลือก **เรียกดู** เพื่อกลับไปยังพอร์ทัลเว็บ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-238">Select **Browse** to go back to the web portal.</span></span>

### <a name="edit-a-paginated-report"></a><span data-ttu-id="c0c2e-239">แก้ไขรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="c0c2e-239">Edit a paginated report</span></span>

<span data-ttu-id="c0c2e-240">คุณสามารถแก้ไขรายงานที่มีการแบ่งหน้าได้ในตัวสร้างรายงาน และคุณสามารถเริ่มตัวสร้างรายงานได้จากเบราว์เซอร์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="c0c2e-240">You can edit paginated reports in Report Builder, and you can start Report Builder right from the browser.</span></span>

1. <span data-ttu-id="c0c2e-241">ในพอร์ทัลเว็บ ให้เลือก **ตัวเลือกเพิ่มเติม** (...) ถัดจาก **ใบสั่งขาย** > **แก้ไขในตัวสร้างรายงาน**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-241">In the web portal, select **More options** (...) next to **Sales Order** > **Edit in Report Builder**.</span></span>

1. <span data-ttu-id="c0c2e-242">เลือก **อนุญาต** เพื่ออนุญาตให้เว็บไซต์นี้เปิดโปรแกรมบนคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-242">Select **Allow** to allow this web site to open a program on your computer.</span></span>

1. <span data-ttu-id="c0c2e-243">รายงานใบสั่งซื้อเปิดขึ้นในมุมมองออกแบบในตัวสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="c0c2e-243">The Sales Order report opens in Design View in Report Builder.</span></span>

    ![มุมมองออกแบบรายงานที่มีการแบ่งหน้า](media/tutorial-explore-report-server-web-portal/power-bi-report-server-paginated-design-view.png)

1. <span data-ttu-id="c0c2e-245">เลือก **เรียกใช้** เพื่อแสดงตัวอย่างรายงาน</span><span class="sxs-lookup"><span data-stu-id="c0c2e-245">Select **Run** to preview the report.</span></span>

    ![ดูตัวอย่างรายงานที่มีการแบ่งหน้า](media/tutorial-explore-report-server-web-portal/power-bi-report-server-paginated-preview.png)

5. <span data-ttu-id="c0c2e-247">ปิดตัวสร้างรายงานและย้อนกลับไปยังเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="c0c2e-247">Close Report Builder and go back to the browser.</span></span>

## <a name="view-excel-workbooks"></a><span data-ttu-id="c0c2e-248">ดูเวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="c0c2e-248">View Excel workbooks</span></span>

<span data-ttu-id="c0c2e-249">คุณสามารถดูและโต้ตอบกับเวิร์กบุ๊ก Excel ได้ใน Excel Online ในเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="c0c2e-249">You can view and interact with Excel workbooks in Excel Online in Power BI Report Server.</span></span> 

1. <span data-ttu-id="c0c2e-250">เลือกเวิร์กบุ๊ก Excel **Office Liquidation Sale.xlsx**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-250">Select the Excel workbook **Office Liquidation Sale.xlsx**.</span></span> <span data-ttu-id="c0c2e-251">ระบบอาจขอให้กรอกข้อมูลประจำตัว</span><span class="sxs-lookup"><span data-stu-id="c0c2e-251">It may ask for credentials.</span></span> <span data-ttu-id="c0c2e-252">เลือก **ยกเลิก**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-252">Select **Cancel**.</span></span> 
    <span data-ttu-id="c0c2e-253">จะเปิดขึ้นในพอร์ทัลเว็บ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-253">It opens in the web portal.</span></span>
1. <span data-ttu-id="c0c2e-254">เลือก **อุปกรณ์** ในตัวแบ่งส่วนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c0c2e-254">Select **Appliance** in the slicer.</span></span>

    ![Excel Online ในพอร์ทัลเว็บ](media/tutorial-explore-report-server-web-portal/power-bi-report-server-excel-online.png)

1. <span data-ttu-id="c0c2e-256">เลือก **เรียกดู** เพื่อกลับไปยังพอร์ทัลเว็บ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-256">Select **Browse** to go back to the web portal.</span></span>

## <a name="clean-up-resources"></a><span data-ttu-id="c0c2e-257">ล้างแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c0c2e-257">Clean up resources</span></span>

<span data-ttu-id="c0c2e-258">ตอนนี้คุณได้เรียนรู้บทช่วยสอนนี้เสร็จสิ้นแล้ว ลบกลุ่มทรัพยากร เครื่องเสมือน และแหล่งข้อมูลทั้งหมดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c0c2e-258">Now that you've finished this tutorial, delete the resource group, virtual machine, and all related resources.</span></span> 

- <span data-ttu-id="c0c2e-259">เมื่อต้องการทำเช่นนั้น เลือกกลุ่มทรัพยากรสำหรับ VM และเลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="c0c2e-259">To do so, select the resource group for the VM and select **Delete**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c0c2e-260">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c0c2e-260">Next steps</span></span>

<span data-ttu-id="c0c2e-261">ในบทช่วยสอนนี้คุณได้สร้าง VM ด้วยเซิร์ฟเวอร์รายงาน Microsoft Power BI</span><span class="sxs-lookup"><span data-stu-id="c0c2e-261">In this tutorial, you've created a VM with Power BI Report Server.</span></span> <span data-ttu-id="c0c2e-262">คุณได้ลองใช้ฟังก์ชันการทำงานของพอร์ทัลเว็บบางส่วน และคุณได้เปิดรายงาน Power BI และรายงานที่แบ่งหน้าในตัวแก้ไขที่เกี่ยวข้องแล้ว</span><span class="sxs-lookup"><span data-stu-id="c0c2e-262">You've tried some of the functionality of the web portal, and you've opened a Power BI report and a paginated report in their respective editors.</span></span> <span data-ttu-id="c0c2e-263">VM นี้มีการติดตั้งแหล่งข้อมูลของ SQL Server Analysis Services ดังนั้นคุณสามารถลองสร้าง Power BI และรายงานที่แบ่งหน้าของคุณเองได้ด้วยแหล่งข้อมูลเดียวกันเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="c0c2e-263">This VM has SQL Server Analysis Services data sources installed, so you can try creating your own Power BI and paginated reports with those same data sources.</span></span> 

<span data-ttu-id="c0c2e-264">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับการสร้างรายงานสำหรับเซิร์ฟเวอร์รายงาน Power BI ให้ไปต่อ</span><span class="sxs-lookup"><span data-stu-id="c0c2e-264">To learn more about creating reports for Power BI Report Server, continue on.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="c0c2e-265">สร้างรายงาน Power BI สำหรับเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="c0c2e-265">Create a Power BI report for Power BI Report Server</span></span>](./quickstart-create-powerbi-report.md)



