---
title: เผยแพร่จาก Power BI Desktop
description: เผยแพร่จาก Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 09/22/2020
LocalizationGroup: Create reports
ms.openlocfilehash: dc1914b8fce55de9bd6141c9cc8d44082779c9df
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412655"
---
# <a name="publish-datasets-and-reports-from-power-bi-desktop"></a><span data-ttu-id="75dc1-103">เผยแพร่ชุดข้อมูลและรายงานจาก Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="75dc1-103">Publish datasets and reports from Power BI Desktop</span></span>
<span data-ttu-id="75dc1-104">เมื่อคุณเผยแพร่เป็นไฟล์ Power BI Desktop ไปยังบริการ Power BI แสดงว่าคุณได้เผยแพร่ข้อมูลในแบบจำลองดังกล่าวไปยังพื้นที่ทำงาน Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="75dc1-104">When you publish a Power BI Desktop file to the Power BI service, you publish the data in the model to your Power BI workspace.</span></span> <span data-ttu-id="75dc1-105">ข้อมูลเดียวกันนี้จะเป็นจริงสำหรับรายงานใด ๆ ที่คุณสร้างไว้ในมุมมอง **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="75dc1-105">The same is true for any reports you created in **Report** view.</span></span> <span data-ttu-id="75dc1-106">คุณจะเห็นชุดข้อมูลใหม่ที่มีชื่อเดียวกัน และรายงานต่างๆในตัวนำทางของพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="75dc1-106">You’ll see a new dataset with the same name, and any reports in your Workspace navigator.</span></span>

<span data-ttu-id="75dc1-107">การเผยแพร่จาก Power BI Desktop จะให้ผลลัพธ์เดียวกันกับการใช้ **Get Data** ใน Power BI เพื่อเชื่อมต่อและอัปโหลดไฟล์ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="75dc1-107">Publishing from Power BI Desktop has the same effect as using **Get Data** in Power BI to connect to and upload a Power BI Desktop file.</span></span>

> [!NOTE]
> <span data-ttu-id="75dc1-108">การเปลี่ยนแปลงใดๆที่คุณทำกับรายงานใน Power BI จะไม่ถูกบันทึกกลับไปยังไฟล์ Power BI Desktop ต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="75dc1-108">Any changes you make to the report in Power BI won't be saved back to the original Power BI Desktop file.</span></span> <span data-ttu-id="75dc1-109">ซึ่งรวมถึงเวลาที่คุณเเพิ่ม ลบ หรือเปลี่ยนแปลงการแสดงภาพต่าง ๆ ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="75dc1-109">This includes when you add, delete, or change visualizations in reports.</span></span>

## <a name="to-publish-a-power-bi-desktop-dataset-and-reports"></a><span data-ttu-id="75dc1-110">เมื่อต้องการเผยแพร่ชุดข้อมูลและรายงาน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="75dc1-110">To publish a Power BI Desktop dataset and reports</span></span>
1. <span data-ttu-id="75dc1-111">ใน Power BI Desktop เลือก **ไฟล์** \> **เผยแพร่** \> **เผยแพร่ไปยัง Power BI** หรือเลือก **เผยแพร่** บน Ribbon</span><span class="sxs-lookup"><span data-stu-id="75dc1-111">In Power BI Desktop, choose **File** \> **Publish** \> **Publish to Power BI** or select **Publish** on the ribbon.</span></span>  

   ![ปุ่มเผยแพร่](media/desktop-upload-desktop-files/pbid_publish_publishbutton.png)


2. <span data-ttu-id="75dc1-113">ลงชื่อเข้าใช้ Power BI หากคุณยังไม่ได้ลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="75dc1-113">Sign in to Power BI, if you aren't already signed in.</span></span>
3. <span data-ttu-id="75dc1-114">เลือกปลายทาง</span><span class="sxs-lookup"><span data-stu-id="75dc1-114">Select the destination.</span></span> <span data-ttu-id="75dc1-115">ตั้งแต่การเปิดตัวในเดือนกันยายน 2020 คุณจะสามารถค้นหารายการพื้นที่ทำงานที่มีอยู่ของคุณเพื่อค้นหาพื้นที่ทำงานที่คุณต้องการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="75dc1-115">Beginning with the September 2020 release, you can search your list of available workspaces to find the workspace into which you want to publish.</span></span> <span data-ttu-id="75dc1-116">กล่องค้นหาช่วยให้คุณกรองพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="75dc1-116">The search box lets you filter your workspaces.</span></span> <span data-ttu-id="75dc1-117">เลือกพื้นที่ทำงาน จากนั้นคลิกปุ่ม **เลือก** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="75dc1-117">Select the workspace, and then click the **Select** button to publish.</span></span>

   ![เลือกปลายทางของการเผยแพร่](media/desktop-upload-desktop-files/pbid_publish_select_destination.png)

<span data-ttu-id="75dc1-119">เมื่อการเผยแพร่เสร็จสมบูรณ์ คุณจะได้รับลิงก์ไปยังรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="75dc1-119">When publishing is complete, you receive a link to your report.</span></span> <span data-ttu-id="75dc1-120">เลือกลิงก์เพื่อเปิดรายงานในไซต์ Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="75dc1-120">Select the link to open the report in your Power BI site.</span></span>

![กล่องโต้ตอบเผยแพร่สำเร็จ](media/desktop-upload-desktop-files/pbid_publish_success.png)

## <a name="republish-or-replace-a-dataset-published-from-power-bi-desktop"></a><span data-ttu-id="75dc1-122">เผยแพร่อีกครั้งหรือแทนที่ชุดข้อมูลที่เผยแพร่จาก Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="75dc1-122">Republish or replace a dataset published from Power BI Desktop</span></span>
<span data-ttu-id="75dc1-123">ชุดข้อมูลและรายงานใดๆ ที่คุณสร้างขึ้นใน Power BI Desktop ให้อัปโหลดไปยังไซค์ Power BI ของคุณเมื่อเผยแพร่ไฟล์ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="75dc1-123">The dataset, and any reports you created in Power BI Desktop, upload to your Power BI site when you publish a Power BI Desktop file.</span></span> <span data-ttu-id="75dc1-124">เมื่อคุณเผยแพร่ไฟล์ Power BI Desktop ของคุณอีกครั้ง ชุดข้อมูลในไซต์ Power BI ของคุณจะถูกแทนที่ด้วยชุดข้อมูลที่อัปเดตแล้วจากไฟล์ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="75dc1-124">When you republish your Power BI Desktop file, the dataset in your Power BI site is replaced with the updated dataset from the Power BI Desktop file.</span></span>

<span data-ttu-id="75dc1-125">กระบวนการนี้ค่อนข้างจะตรงไปตรงมา แต่จะมีรายการ 2-3 รายการที่คุณควรทราบ:</span><span class="sxs-lookup"><span data-stu-id="75dc1-125">This process is straightforward, but there are a few things you should know:</span></span>

* <span data-ttu-id="75dc1-126">ถ้าคุณมีชุดข้อมูลสองรายการ หรือมากกว่าใน Power BI โดยใช้ชื่อเดียวกันกับไฟล์ Power BI Desktop การเผยแพร่อาจล้มเหลวได้</span><span class="sxs-lookup"><span data-stu-id="75dc1-126">Two or more datasets in Power BI with the same name as the Power BI Desktop file could cause publishing to fail.</span></span> <span data-ttu-id="75dc1-127">ตรวจสอบให้แน่ใจว่า คุณมีชุดข้อมูลเดียวเท่านั้นใน Power BI ที่มีชื่อเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="75dc1-127">Make sure you have only one dataset in Power BI with the same name.</span></span> <span data-ttu-id="75dc1-128">นอกจากนี้คุณยังสามารถเปลี่ยนชื่อไฟล์และเผยแพร่ โดยสร้างชุดข้อมูลใหม่ชื่อเดียวกันกับไฟล์</span><span class="sxs-lookup"><span data-stu-id="75dc1-128">You can also rename the file and publish, creating a new dataset with same name as the file.</span></span>
* <span data-ttu-id="75dc1-129">ถ้าคุณเปลี่ยนชื่อหรือลบคอลัมน์หรือหน่วยวัด การแสดงภาพใดๆที่คุณมีใน Power BI ที่มีเขตข้อมูลนั้นอาจจะไม่สามารถใช้งาน</span><span class="sxs-lookup"><span data-stu-id="75dc1-129">If you rename or delete a column or measure, any visualizations you already have in Power BI with that field could be broken.</span></span> 
* <span data-ttu-id="75dc1-130">Power BI ละเว้นการเปลี่ยนแปลงการจัดรูปแบบบางอย่างของคอลัมน์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="75dc1-130">Power BI ignores some format changes of existing columns.</span></span> <span data-ttu-id="75dc1-131">ตัวอย่างเช่น หากคุณเปลี่ยนรูปแบบของคอลัมน์จาก 0.25% เป็น 25%</span><span class="sxs-lookup"><span data-stu-id="75dc1-131">For example, if you change a column’s format  from 0.25% to 25%.</span></span>
* <span data-ttu-id="75dc1-132">สมมติว่าคุณมีกำหนดการรีเฟรชที่มีการกำหนดค่าสำหรับชุดข้อมูลที่มีอยู่ของคุณใน Power BI</span><span class="sxs-lookup"><span data-stu-id="75dc1-132">Say you have a refresh schedule that is configured for your existing dataset in Power BI.</span></span> <span data-ttu-id="75dc1-133">เมื่อคุณเพิ่มแหล่งข้อมูลใหม่ลงในไฟล์ของคุณแล้วเผยแพร่อีกครั้ง คุณจะต้องลงชื่อเข้าใช้ก่อน่การรีเฟรชตามกำหนดการครั้งถัดไป</span><span class="sxs-lookup"><span data-stu-id="75dc1-133">When you add new data sources to your file and then republish, you’ll have to sign into them before the next scheduled refresh.</span></span>
* <span data-ttu-id="75dc1-134">เมื่อคุณเผยแพร่ชุดข้อมูลที่เผยแพร่จาก Power BI Desktop ใหม่ และมีการกำหนดตารางเวลาการรีเฟรช การรีเฟรชชุดข้อมูลจะเริ่มต้นทันทีที่คุณเผยแพร่อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="75dc1-134">When you republish a dataset published from Power BI Desktop and have a refresh schedule defined, a dataset refresh is started as soon as you republish.</span></span>
* <span data-ttu-id="75dc1-135">เมื่อคุณทำการเปลี่ยนแปลงกับชุดข้อมูล แล้วเผยแพร่ใหม่อีกครั้ง ข้อความจะแสดงจำนวนพื้นที่ทำงาน รายงาน และแดชบอร์ดที่อาจได้รับผลกระทบจากการเปลี่ยนแปลงนั้น และจะขอให้คุณยืนยันว่า คุณต้องการแทนที่ชุดข้อมูลที่เผยแพร่ในปัจจุบันด้วยรายการที่คุณปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="75dc1-135">When you make a change to a dataset and then republish it, a message shows you how many workspaces, reports, and dashboards are potentially impacted by the change, and asks you to confirm that you want to replace the currently published dataset with the one you modified.</span></span> <span data-ttu-id="75dc1-136">นอกจากนี้ ข้อความยังประกอบด้วยลิงก์ไปยังการวิเคราะห์ผลกระทบของชุดข้อมูลแบบเต็มรูปแบบในบริการ Power BI ที่คุณจะสามารถมองเห็นข้อมูลเพิ่มเติม และดำเนินการเพื่อบรรเทาความเสี่ยงจากการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="75dc1-136">The message also provides a link to the full dataset impact analysis in the Power BI service, where you can see more information and take action to mitigate the risks of your change.</span></span>

   ![คำเตือนเกี่ยวกับผลกระทบของการเผยแพร่ชุดข้อมูลใหม่อีกครั้ง](media/desktop-upload-desktop-files/pbid-dataset-impact-analysis-desktop-warning.png)

   <span data-ttu-id="75dc1-138">[เรียนรู้เพิ่มเติมเกี่ยวกับการวิเคราะห์ผลกระทบของชุดข้อมูล](../collaborate-share/service-dataset-impact-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="75dc1-138">[Learn more about Dataset impact analysis](../collaborate-share/service-dataset-impact-analysis.md).</span></span>

> [!NOTE]
> <span data-ttu-id="75dc1-139">การเชื่อมต่อข้อมูลบางอย่างในรายงาน Power BI อาจรวมถึงการเชื่อมโยงไปยังข้อมูล แทนที่จะรวมข้อมูลในชุดข้อมูลที่นำเข้าลงในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="75dc1-139">Some data connection in Power BI reports may include links to data, rather than including the data in the dataset that's imported into the Power BI service.</span></span> <span data-ttu-id="75dc1-140">ตัวอย่างเช่น ลิงก์การเชื่อมต่อ DirectQuery ไปยังข้อมูลเนื่องจากเกิดการอัปเดตหรือการโต้ตอบ แทนที่จะนำเข้าข้อมูลด้วยตัวเอง</span><span class="sxs-lookup"><span data-stu-id="75dc1-140">For example, DirectQuery connections link to data as updates or interactions occur, rather than importing the data itself.</span></span> <span data-ttu-id="75dc1-141">ถ้าแหล่งข้อมูลที่เชื่อมโยงในรายงานของคุณอยู่ภายในองค์กร คุณอาจจำเป็นต้องมีเกตเวย์เพื่อเข้าถึงจาก Power BI อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="75dc1-141">If linked data sources in your report are on premises, you may need a gateway to access them from Power BI.</span></span> <span data-ttu-id="75dc1-142">สำหรับข้อมูลเพิ่มเติม ดูที่ [เกตเวย์ข้อมูลภายในองค์กรคืออะไร](../connect-data/service-gateway-onprem.md)</span><span class="sxs-lookup"><span data-stu-id="75dc1-142">For more information, see [what is an on-premises data gateway?](../connect-data/service-gateway-onprem.md).</span></span>
> 

## <a name="next-steps"></a><span data-ttu-id="75dc1-143">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="75dc1-143">Next steps</span></span>

<span data-ttu-id="75dc1-144">คุณสามารถทำการเรียงลำดับของของต่างๆ ด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="75dc1-144">You can do all sorts of things with Power BI Desktop.</span></span> <span data-ttu-id="75dc1-145">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับขีดความสามารถ กรุณาดูแหล่งทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="75dc1-145">For more information on its capabilities, check out the following resources:</span></span>

* [<span data-ttu-id="75dc1-146">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="75dc1-146">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="75dc1-147">ภาพรวมคำถามด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="75dc1-147">Query overview with Power BI Desktop</span></span>](../transform-model/desktop-query-overview.md)
* [<span data-ttu-id="75dc1-148">ชนิดข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="75dc1-148">Data types in Power BI Desktop</span></span>](../connect-data/desktop-data-types.md)
* [<span data-ttu-id="75dc1-149">บทช่วยสอน: จัดรูปร่างและรวมข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="75dc1-149">Tutorial: Shape and combine data in Power BI Desktop</span></span>](../connect-data/desktop-shape-and-combine-data.md)
* [<span data-ttu-id="75dc1-150">งานแบบสอบถามทั่วไปใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="75dc1-150">Common query tasks in Power BI Desktop</span></span>](../transform-model/desktop-common-query-tasks.md)
