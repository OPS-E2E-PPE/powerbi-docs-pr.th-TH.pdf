---
title: สร้างรายงาน Power BI สำหรับเซิร์ฟเวอร์รายงาน Power BI
description: เรียนรู้วิธีการสร้างรายงาน Power BI สำหรับเซิร์ฟเวอร์รายงาน Power BI ในขั้นตอนง่าย ๆ ไม่กี่ขั้นตอน
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.date: 07/24/2020
ms.openlocfilehash: 965c3837b2d0153716442ea37b52b468be9742fb
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414127"
---
# <a name="create-a-power-bi-report-for-power-bi-report-server"></a><span data-ttu-id="be24f-103">สร้างรายงาน Power BI สำหรับเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="be24f-103">Create a Power BI report for Power BI Report Server</span></span>
<span data-ttu-id="be24f-104">คุณสามารถจัดเก็บ และจัดการรายงาน Power BI ภายในองค์กร ในพอร์ทัลของเว็บเซิร์ฟเวอร์รายงาน Power BI เช่นเดียวกับที่คุณสามารถจัดเก็บรายงาน Power BI ในระบบคลาวด์ในบริการของ Power BI (https://powerbi.com) ได้</span><span class="sxs-lookup"><span data-stu-id="be24f-104">You can store and manage Power BI reports on premises in the Power BI Report Server web portal, just as you can store Power BI reports in the cloud in the Power BI service (https://powerbi.com).</span></span> <span data-ttu-id="be24f-105">คุณสร้างและแก้ไขรายงานใน Power BI Desktop แล้วเผยแพร่ไปยังพอร์ทัลของเว็บ</span><span class="sxs-lookup"><span data-stu-id="be24f-105">You create and edit reports in Power BI Desktop, and publish them to the web portal.</span></span> <span data-ttu-id="be24f-106">จากนั้น ผู้อ่านรายงานในองค์กรของคุณ สามารถดูรายงานได้ในเบราว์เซอร์ หรือในแอปมือถือ Power BI บนอุปกรณ์เคลื่อนที่ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="be24f-106">Then report readers in your organization can view them in a browser or in a Power BI mobile app on a mobile device.</span></span>

![รายงาน Power BI ในพอร์ทัลของเว็บ](media/quickstart-create-powerbi-report/report-server-powerbi-report.png)

<span data-ttu-id="be24f-108">ต่อไปนี้เป็นสี่ขั้นตอนด่วน ที่ช่วยให้คุณเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="be24f-108">Here are four quick steps to get you started.</span></span>

## <a name="step-1-install-power-bi-desktop-optimized-for-power-bi-report-server"></a><span data-ttu-id="be24f-109">ขั้นตอนที่ 1: ติดตั้ง Power BI Desktop ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="be24f-109">Step 1: Install Power BI Desktop optimized for Power BI Report Server</span></span>

<span data-ttu-id="be24f-110">ถ้าคุณเคยสร้างรายงาน Power BI ใน Power BI Desktop แล้ว คุณเกือบพร้อมที่จะสร้างรายงาน Power BI สำหรับเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="be24f-110">If you've already created Power BI reports in Power BI Desktop, then you're almost ready to create Power BI reports for Power BI Report Server.</span></span> <span data-ttu-id="be24f-111">เราขอแนะนำให้ติดตั้งเวอร์ชันของ Power BI Desktop ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI เพื่อให้คุณมั่นใจว่าเซิร์ฟเวอร์ และแอปจะซิงค์กันอยู่เสมอ คุณสามารถมี Power BI Desktop ทั้งสองเวอร์ชันบนคอมพิวเตอร์เครื่องเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="be24f-111">We recommend installing the version of Power BI Desktop optimized for Power BI Report Server so you know the server and the app are always in sync. You can have both versions of Power BI Desktop on the same computer.</span></span>

1. <span data-ttu-id="be24f-112">ในพอร์ทัลของเว็บเซิร์ฟเวอร์รายงาน เลือกลูกศร **ดาวน์โหลด** > **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="be24f-112">In the report server web portal, select the **Download** arrow > **Power BI Desktop**.</span></span>

    ![ดาวน์โหลด Power BI Desktop จากพอร์ทัลของเว็บ](media/quickstart-create-powerbi-report/report-server-download-web-portal.png)

    <span data-ttu-id="be24f-114">หรือไปที่หน้าหลัก [เซิร์ฟเวอร์รายงาน Power BI](https://powerbi.microsoft.com/report-server/) แล้วเลือก **ตัวเลือกการดาวน์โหลดขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="be24f-114">Or go to the [Power BI Report Server](https://powerbi.microsoft.com/report-server/) home page and select **Advanced download options**.</span></span>

2. <span data-ttu-id="be24f-115">ในหน้าศูนย์ดาวน์โหลด เลือก **ดาวน์โหลด**</span><span class="sxs-lookup"><span data-stu-id="be24f-115">In the Download Center page, select **Download**.</span></span>

3. <span data-ttu-id="be24f-116">ขึ้นอยู่กับคอมพิวเตอร์ของคุณ เลือก:</span><span class="sxs-lookup"><span data-stu-id="be24f-116">Depending on your computer, select:</span></span>

    - <span data-ttu-id="be24f-117">**PBIDesktopRS.msi** (เวอร์ชัน 32 บิต) หรือ</span><span class="sxs-lookup"><span data-stu-id="be24f-117">**PBIDesktopRS.msi** (the 32-bit version) or</span></span>

    - <span data-ttu-id="be24f-118">**PBIDesktopRS_x64.msi** (เวอร์ชัน 64 บิต)</span><span class="sxs-lookup"><span data-stu-id="be24f-118">**PBIDesktopRS_x64.msi** (the 64-bit version).</span></span>

4. <span data-ttu-id="be24f-119">หลังจากที่คุณดาวน์โหลดตัวติดตั้งแล้ว เรียกใช้ตัวช่วยสร้างการติดตั้ง Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="be24f-119">After you download the installer, run the Power BI Desktop Setup Wizard.</span></span>

2. <span data-ttu-id="be24f-120">ในตอนท้ายของการติดตั้ง ทำเครื่องหมายที่ **เริ่มต้น Power BI Desktop ทันที**</span><span class="sxs-lookup"><span data-stu-id="be24f-120">At the end of the installation, check **Start Power BI Desktop now**.</span></span>
   
    <span data-ttu-id="be24f-121">จะเริ่มต้นโดยอัตโนมัติ และคุณก็พร้อมที่จะไปต่อ</span><span class="sxs-lookup"><span data-stu-id="be24f-121">It starts automatically and you're ready to go.</span></span> <span data-ttu-id="be24f-122">คุณสามารถแจ้งว่าคุณมีเวอร์ชันที่ถูกต้องเนื่องจาก **Power BI Desktop (ตุลาคม 2020)** อยู่ในแถบชื่อ</span><span class="sxs-lookup"><span data-stu-id="be24f-122">You can tell you have the right version because **Power BI Desktop (October 2020)** is in the title bar.</span></span>

    ![Power BI Desktop ตุลาคม 2020](media/quickstart-create-powerbi-report/power-bi-report-server-desktop-may-2020.png)

3. <span data-ttu-id="be24f-124">ถ้าคุณไม่คุ้นเคยกับ Power BI Desktop ลองดูวิดีโอบนหน้าจอยินดีต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="be24f-124">If you're not familiar with Power BI Desktop, consider watching the videos on the welcome screen.</span></span>
   
    ![หน้าจอเริ่มต้น Power BI Desktop](media/quickstart-create-powerbi-report/report-server-powerbi-desktop-start.png)

## <a name="step-2-select-a-data-source"></a><span data-ttu-id="be24f-126">ขั้นตอนที่ 2: เลือกแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="be24f-126">Step 2: Select a data source</span></span>
<span data-ttu-id="be24f-127">คุณสามารถเชื่อมต่อกับแหล่งข้อมูลที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="be24f-127">You can connect to a variety of data sources.</span></span> <span data-ttu-id="be24f-128">อ่านเพิ่มเติมเกี่ยวกับ[การเชื่อมต่อกับแหล่งข้อมูล](connect-data-sources.md)</span><span class="sxs-lookup"><span data-stu-id="be24f-128">Read more about [connecting to data sources](connect-data-sources.md).</span></span>

1. <span data-ttu-id="be24f-129">จากหน้าจอยินดีต้อนรับ เลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="be24f-129">From the welcome screen, select **Get Data**.</span></span>
   
    <span data-ttu-id="be24f-130">หรือบนการแท็บ **หน้าแรก** เลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="be24f-130">Or on the **Home** tab, select **Get Data**.</span></span>
2. <span data-ttu-id="be24f-131">เลือกแหล่งข้อมูลของคุณ - ในตัวอย่างนี้เป็น **Analysis Services**</span><span class="sxs-lookup"><span data-stu-id="be24f-131">Select your data source -- in this example, **Analysis Services**.</span></span>
   
    ![เลือกแหล่งข้อมูล](media/quickstart-create-powerbi-report/power-bi-report-server-get-data-ssas.png)
3. <span data-ttu-id="be24f-133">กรอกค่า **เซิร์ฟเวอร์** และใส่ **ฐานข้อมูล** ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="be24f-133">Fill in **Server**, and optionally, **Database**.</span></span> <span data-ttu-id="be24f-134">ตรวจสอบให้แน่ใจว่าตัวเลือก **เชื่อมต่อแบบไลฟ์** ถูกเลือก > **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="be24f-134">Make sure **Connect live** is selected > **OK**.</span></span>
   
    ![ชื่อเซิร์ฟเวอร์](media/quickstart-create-powerbi-report/report-server-ssas-server-name.png)
4. <span data-ttu-id="be24f-136">เลือกเซิร์ฟเวอร์รายงานที่คุณจะบันทึกรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="be24f-136">Choose the report server where you'll save your reports.</span></span>
   
    ![เลือกเซิร์ฟเวอร์รายงาน](media/quickstart-create-powerbi-report/report-server-select-server.png)

## <a name="step-3-design-your-report"></a><span data-ttu-id="be24f-138">ขั้นตอนที่ 3: ออกแบบรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="be24f-138">Step 3: Design your report</span></span>
<span data-ttu-id="be24f-139">เรื่องสนุกๆ อยู่ในส่วนนี้: คุณจะสร้างวิชวลที่แสดงข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="be24f-139">Here's the fun part: You get to create visuals that illustrate your data.</span></span>

<span data-ttu-id="be24f-140">ตัวอย่างเช่น คุณสามารถสร้างแผนภูมิกรวยของลูกค้าและจัดกลุ่มตามรายได้รายปี</span><span class="sxs-lookup"><span data-stu-id="be24f-140">For example, you could create a funnel chart of customers and group values by yearly income.</span></span>

![ออกแบบรายงาน](media/quickstart-create-powerbi-report/report-server-create-funnel.png)

1. <span data-ttu-id="be24f-142">ใน **การจัดรูปแบบการแสดงข้อมูล** เลือก **แผนภูมิกรวย**</span><span class="sxs-lookup"><span data-stu-id="be24f-142">In **Visualizations**, select **Funnel chart**.</span></span>
2. <span data-ttu-id="be24f-143">ลากเขตข้อมูลที่จะนับลงใน **ค่า**</span><span class="sxs-lookup"><span data-stu-id="be24f-143">Drag the field to be counted to the **Values** well.</span></span> <span data-ttu-id="be24f-144">ถ้าเขตข้อมูลไม่ใช่ตัวเลข Power BI Desktop จะทำการ *นับจำนวน* ค่าให้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="be24f-144">If it's not a numeric field, Power BI Desktop automatically makes it a *Count of* the value.</span></span>
3. <span data-ttu-id="be24f-145">ลากเขตข้อมูลที่จะจัดกลุ่มลงใน **กลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="be24f-145">Drag the field to group on to the **Group** well.</span></span>

<span data-ttu-id="be24f-146">อ่านเพิ่มเติมเกี่ยวกับ[การออกแบบรายงาน Power BI](../create-reports/desktop-report-view.md)</span><span class="sxs-lookup"><span data-stu-id="be24f-146">Read much more about [designing a Power BI report](../create-reports/desktop-report-view.md).</span></span>

## <a name="step-4-save-your-report-to-the-report-server"></a><span data-ttu-id="be24f-147">ขั้นตอนที่ 4: บันทึกรายงานของคุณไปยังเซิร์ฟเวอร์รายงาน</span><span class="sxs-lookup"><span data-stu-id="be24f-147">Step 4: Save your report to the report server</span></span>
<span data-ttu-id="be24f-148">เมื่อรายงานของคุณพร้อมแล้ว คุณบันทึกไปยังเซิร์ฟเวอร์รายงาน Power BI ที่คุณเลือกในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="be24f-148">When your report is ready, you save it to the Power BI Report Server you chose in Step 2.</span></span>

1. <span data-ttu-id="be24f-149">บนเมนู **แฟ้ม** เลือก **บันทึกเป็น** > **เซิร์ฟเวอร์รายงาน Power BI**</span><span class="sxs-lookup"><span data-stu-id="be24f-149">On the **File** menu, select **Save as** > **Power BI Report Server**.</span></span>
   
    ![บันทึกไปยังเซิร์ฟเวอร์รายงาน](media/quickstart-create-powerbi-report/report-server-save-as-powerbi-report-server.png)
2. <span data-ttu-id="be24f-151">ตอนนี้ คุณสามารถดูรายงานได้ในพอร์ทัลของเว็บ</span><span class="sxs-lookup"><span data-stu-id="be24f-151">Now you can view it in the web portal.</span></span>
   
    ![ดูรายงานในพอร์ทัลของเว็บ](media/quickstart-create-powerbi-report/report-server-powerbi-report.png)
    
> [!NOTE]
> <span data-ttu-id="be24f-153">หากคุณเลือกที่จะแก้ไขรายงานในอนาคต ข้อมูลรายงานที่คุณเห็นในเดสก์ท็อปจะเป็นข้อมูลที่แคชเสมอเมื่อสร้างรายงานครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="be24f-153">If you choose to edit the report in the future, the report data you see in the desktop will always be the cached data from when the report was initially created.</span></span>  <span data-ttu-id="be24f-154">หากต้องการดูข้อมูลล่าสุดเมื่อแก้ไขรายงาน คุณต้องรีเฟรชข้อมูลในแอปพลิเคชัน Power BI Desktop ของคุณ</span><span class="sxs-lookup"><span data-stu-id="be24f-154">To view the latest data when editing the report, you must refresh the data in your Power BI Desktop application.</span></span>

## <a name="next-steps"></a><span data-ttu-id="be24f-155">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="be24f-155">Next steps</span></span>
### <a name="power-bi-desktop"></a><span data-ttu-id="be24f-156">Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="be24f-156">Power BI Desktop</span></span>
<span data-ttu-id="be24f-157">มีทรัพยากรที่ยอดเยี่ยมมากมายสำหรับการสร้างรายงานใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="be24f-157">There are so many great resources for creating reports in Power BI Desktop.</span></span> <span data-ttu-id="be24f-158">ลิงก์นี้เป็นจุดเริ่มต้นที่ดี</span><span class="sxs-lookup"><span data-stu-id="be24f-158">This link is a good starting point.</span></span>

* [<span data-ttu-id="be24f-159">เริ่มต้นใช้งาน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="be24f-159">Get started with Power BI Desktop</span></span>](../fundamentals/desktop-getting-started.md)
* <span data-ttu-id="be24f-160">การเรียนรู้ตามคำแนะนำ: [สำรวจ Power BI Desktop](/learn/modules/get-data-power-bi/2-getting-started-power-bi-desktop)</span><span class="sxs-lookup"><span data-stu-id="be24f-160">Guided learning: [Explore Power BI Desktop](/learn/modules/get-data-power-bi/2-getting-started-power-bi-desktop)</span></span>

### <a name="power-bi-report-server"></a><span data-ttu-id="be24f-161">เซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="be24f-161">Power BI Report Server</span></span>
* [<span data-ttu-id="be24f-162">ติดตั้ง Power BI Desktop ที่ปรับให้เหมาะสำหรับ Power BI Report Server</span><span class="sxs-lookup"><span data-stu-id="be24f-162">Install Power BI Desktop optimized for Power BI Report Server</span></span>](install-powerbi-desktop.md)  
* [<span data-ttu-id="be24f-163">เซิร์ฟเวอร์รายงาน Power BI คืออะไร</span><span class="sxs-lookup"><span data-stu-id="be24f-163">What is Power BI Report Server?</span></span>](get-started.md)  

<span data-ttu-id="be24f-164">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="be24f-164">More questions?</span></span> [<span data-ttu-id="be24f-165">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="be24f-165">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
