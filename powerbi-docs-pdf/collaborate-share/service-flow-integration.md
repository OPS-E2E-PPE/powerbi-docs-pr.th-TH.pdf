---
title: รวมการแจ้งเตือนข้อมูล Power BI ด้วย Power Automate
description: เรียนรู้วิธีสร้างโฟลว์ Power Automate ที่ถูกทริกเกอร์ด้วยการแจ้งเตือนข้อมูล Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 12/08/2020
LocalizationGroup: Get started
ms.openlocfilehash: 8f73bd959691ea8359a8584966e0b83f439d8652
ms.sourcegitcommit: bbf7e9341a4e1cc96c969e24318c8605440282a5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/11/2020
ms.locfileid: "97097650"
---
# <a name="integrate-power-bi-data-alerts-with-power-automate"></a><span data-ttu-id="49917-103">รวมการแจ้งเตือนข้อมูล Power BI ด้วย Power Automate</span><span class="sxs-lookup"><span data-stu-id="49917-103">Integrate Power BI data alerts with Power Automate</span></span>

<span data-ttu-id="49917-104">ใช้ [Power Automate](/power-automate/getting-started) เพื่อรวม Power BI เข้ากับแอปและบริการที่คุณชื่นชอบ</span><span class="sxs-lookup"><span data-stu-id="49917-104">Use [Power Automate](/power-automate/getting-started) to integrate Power BI with your favorite apps and services.</span></span> <span data-ttu-id="49917-105">ด้วย Power Automate คุณสามารถสร้างเวิร์กโฟลว์อัตโนมัติเพื่อรับการแจ้งเตือน ซิงโครไนซ์ไฟล์ รวบรวมข้อมูล และอื่น ๆ อีกมากมายได้</span><span class="sxs-lookup"><span data-stu-id="49917-105">With Power Automate, you create automated workflows to get notifications, synchronize files, collect data, and more.</span></span> <span data-ttu-id="49917-106">ในบทความนี้ คุณจะสร้างอีเมลจากการแจ้งเตือนข้อมูล Power BI โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="49917-106">In this article, you automate generating an email from a Power BI data alert.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="49917-107">สิ่งที่จำเป็นต้องมี</span><span class="sxs-lookup"><span data-stu-id="49917-107">Prerequisites</span></span>
<span data-ttu-id="49917-108">บทความนี้จะแสดงวิธีการสร้างโฟลว์ที่แตกต่างกันสองโฟลว์ โฟลว์แรกจากเทมเพลต และอีกโฟลว์หนึ่งสร้างใหม่ตั้งแต่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="49917-108">This article shows how to create two different flows: one from a template and one from scratch.</span></span> <span data-ttu-id="49917-109">เพื่อทำตาม [สร้างการแจ้งเตือนข้อมูลใน Power BI](../create-reports/service-set-data-alerts.md) และ [ลงทะเบียนเพื่อใช้งาน Power Automate](https://flow.microsoft.com/#home-signup)</span><span class="sxs-lookup"><span data-stu-id="49917-109">To follow along, [create a data alert in Power BI](../create-reports/service-set-data-alerts.md), and [sign up for Power Automate](https://flow.microsoft.com/#home-signup).</span></span> <span data-ttu-id="49917-110">ฟรี!</span><span class="sxs-lookup"><span data-stu-id="49917-110">It's free!</span></span>

## <a name="create-a-flow-from-a-template"></a><span data-ttu-id="49917-111">สร้างโฟลว์จากเทมเพลต</span><span class="sxs-lookup"><span data-stu-id="49917-111">Create a flow from a template</span></span>
<span data-ttu-id="49917-112">ในงานนี้ เราจะใช้เทมเพลตเพื่อสร้างโฟลว์อย่างง่ายที่จะถูกทริกเกอร์ โดยการแจ้งเตือนข้อมูล Power BI (การแจ้งเตือน)</span><span class="sxs-lookup"><span data-stu-id="49917-112">In this task, we use a template to create a simple flow that is triggered by a Power BI data alert (notification).</span></span>

1. <span data-ttu-id="49917-113">ลงชื่อเข้าใช้ Power Automate (flow.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="49917-113">Sign in to Power Automate (flow.microsoft.com).</span></span>
2. <span data-ttu-id="49917-114">เลือก **เทมเพลต** ค้นหา **Power BI** > **ส่งอีเมลถึงผู้ชมทุกคน เมื่อการแจ้งเตือนข้อมูล Power BI ถูกทริกเกอร์**</span><span class="sxs-lookup"><span data-stu-id="49917-114">Select **Templates**, search for **Power BI** > **Send an e-mail to any audience when a Power BI data alert is triggered**.</span></span>
   
    :::image type="content" source="media/service-flow-integration/power-automate-templates.png" alt-text="สกรีนช็อตของเทมเพลต Power Automate ส่งอีเมลถึงผู้ชมทุกคนเมื่อการแจ้งเตือนข้อมูล Power BI ถูกทริกเกอร์":::

### <a name="build-the-flow"></a><span data-ttu-id="49917-116">สร้างโฟลว์</span><span class="sxs-lookup"><span data-stu-id="49917-116">Build the flow</span></span>
<span data-ttu-id="49917-117">เทมเพลตนี้มีหนึ่งทริกเกอร์ การแจ้งเตือนข้อมูล Power BI และหนึ่งการดำเนินการเพื่อส่งอีเมล</span><span class="sxs-lookup"><span data-stu-id="49917-117">This template has one trigger, a Power BI data alert, and one action, to send an email.</span></span> <span data-ttu-id="49917-118">เมื่อคุณเลือกเขตข้อมูล โฟลว์ Power Automate จะแสดงเนื้อหาแบบไดนามิกที่คุณสามารถรวมไว้ได้</span><span class="sxs-lookup"><span data-stu-id="49917-118">As you select a field, Power Automate displays dynamic content that you can include.</span></span>  <span data-ttu-id="49917-119">ในตัวอย่างนี้ เราจะรวมค่าไทล์และ URL ไทล์ในเนื้อหาข้อความ</span><span class="sxs-lookup"><span data-stu-id="49917-119">In this example, we include the tile value and the tile URL in the message body.</span></span>

1. <span data-ttu-id="49917-120">เลือก **ดำเนินต่อ**</span><span class="sxs-lookup"><span data-stu-id="49917-120">Select **Continue**.</span></span>

    :::image type="content" source="media/service-flow-integration/power-automate-power-bi-mail.png" alt-text="สกรีนช็อตของ Power Automate, Power BI ไปยังอีเมล":::

1. <span data-ttu-id="49917-122">ในกล่อง **ID การแจ้งเตือน** ให้เลือกการแจ้งเตือนข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="49917-122">In the **Alert ID** box, select a Power BI data alert.</span></span> <span data-ttu-id="49917-123">เมื่อต้องการเรียนรู้วิธีการสร้างการแจ้งเตือน ให้ดู[การแจ้งเตือนข้อมูลใน Power BI](../create-reports/service-set-data-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="49917-123">To learn how to create an alert, see [Data alerts in Power BI](../create-reports/service-set-data-alerts.md).</span></span>
   
    :::image type="content" source="media/service-flow-integration/power-automate-select-alert-id.png" alt-text="สกรีนช็อตของเลือกการแจ้งเตือนในกล่อง ID การแจ้งเตือน":::
2. <span data-ttu-id="49917-125">ใส่อีเมลแอดเดรสที่ถูกต้องอย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="49917-125">Enter one or more valid email addresses.</span></span>

3. <span data-ttu-id="49917-126">Power Automate สร้าง **หัวข้อ** และ **เนื้อความ** สำหรับคุณโดยอัตโนมัติซึ่งคุณสามารถใช้หรือปรับเปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="49917-126">Power Automate automatically generates a **Subject** and **Body** for you, which you can keep or modify.</span></span> <span data-ttu-id="49917-127">ข้อความเนื้อหาใช้ HTML สำหรับการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="49917-127">The body text uses HTML for formatting.</span></span>

    :::image type="content" source="media/service-flow-integration/power-automate-autogenerated-email.png" alt-text="สกรีนช็อตของข้อความอีเมลที่สร้างโดยอัตโนมัติของ Power Automate":::

1. <span data-ttu-id="49917-129">เมื่อคุณปรับเปลี่ยนข้อความเรียบร้อยแล้ว ให้เลือก **ขั้นตอนถัดไป** หรือ **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="49917-129">When you're done with the message, select **Next step** or **Save**.</span></span>  <span data-ttu-id="49917-130">ขั้นตอนถูกสร้างขึ้นและถูกประเมิน</span><span class="sxs-lookup"><span data-stu-id="49917-130">The flow is created and evaluated.</span></span>  <span data-ttu-id="49917-131">ขั้นตอน Power Automate จะแจ้งให้คุณทราบหากพบข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="49917-131">Power Automate lets you know if it finds errors.</span></span>
2. <span data-ttu-id="49917-132">ถ้าพบข้อผิดพลาด ให้เลือก **แก้ไขโฟลว์** เมื่อต้องการแก้ไขปัญหาเหล่านั้น ถ้าไม่ ให้เลือก **เสร็จแล้ว** เพื่อเรียกใช้โฟลว์ใหม่</span><span class="sxs-lookup"><span data-stu-id="49917-132">If errors are found, select **Edit flow** to fix them, otherwise, select **Done** to run the new flow.</span></span>
   
   ![สกรีนช็อตของข้อความสำเร็จเรียบร้อยของ Power Automate](media/service-flow-integration/power-bi-flow-running.png)
5. <span data-ttu-id="49917-134">เมื่อการแจ้งเตือนข้อมูลถูกทริกเกอร์ Power Automate จะส่งอีเมลไปยังที่อยู่คุณระบุไว้</span><span class="sxs-lookup"><span data-stu-id="49917-134">When the data alert is triggered, Power Automate sends an email to the addresses you indicated.</span></span>  
   
   ![สกรีนช็อตของอีเมลแจ้งเตือนของ Power Automate](media/service-flow-integration/power-bi-flow-email2.png)

## <a name="create-a-flow-from-scratch"></a><span data-ttu-id="49917-136">สร้างโฟลว์ตั้งแต่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="49917-136">Create a flow from scratch</span></span>
<span data-ttu-id="49917-137">ในงานนี้ เราจะสร้างโฟลว์ง่ายๆ ตั้งแต่เริ่มต้น ซึ่งจะถูกทริกเกอร์โดยการแจ้งเตือนข้อมูล Power BI (การแจ้งเตือน)</span><span class="sxs-lookup"><span data-stu-id="49917-137">In this task, we create a simple flow from scratch that is triggered by a Power BI data alert (notification).</span></span>

1. <span data-ttu-id="49917-138">ลงชื่อเข้าใช้ Power Automate (flow.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="49917-138">Sign in to Power Automate (flow.microsoft.com).</span></span>
2. <span data-ttu-id="49917-139">เลือก **สร้าง** > **โฟลว์อัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="49917-139">Select **Create** > **Automated flow**.</span></span>

    :::image type="content" source="media/service-flow-integration/power-automate-create-automated-flow.png" alt-text="สกรีนช็อตของ Power Automate > สร้างโฟลว์อัตโนมัติ":::   
3. <span data-ttu-id="49917-141">ใน **สร้างโฟลว์อัตโนมัติ** ให้ตั้งชื่อโฟลว์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="49917-141">In **Build an automated flow**, give your flow a name.</span></span>
1. <span data-ttu-id="49917-142">ใน **เลือกทริกเกอร์ของโฟลว์ของคุณ** ให้ค้นหา **Power BI**</span><span class="sxs-lookup"><span data-stu-id="49917-142">In the **Choose your flow's trigger**, search for **Power BI**.</span></span>
1. <span data-ttu-id="49917-143">เลือก  **Power BI - เมื่อการแจ้งเตือนการขับเคลื่อนข้อมูลได้รับการทริกเกอร์** > **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="49917-143">Select **Power BI - When a data driven alert is triggered** > **Create**.</span></span>

    :::image type="content" source="media/service-flow-integration/power-automate-build-automated-flow.png" alt-text="สกรีนช็อตของการสร้างโฟลว์อัตโนมัติ":::

### <a name="build-your-flow"></a><span data-ttu-id="49917-145">สร้างโฟลว์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="49917-145">Build your flow</span></span>
1. <span data-ttu-id="49917-146">ในกล่อง **ID การแจ้งเตือน** ให้เลือกชื่อของการแจ้งเตือนของคุณ</span><span class="sxs-lookup"><span data-stu-id="49917-146">In the **Alert ID** box, select the name of your alert.</span></span> <span data-ttu-id="49917-147">เมื่อต้องการเรียนรู้วิธีการสร้างการแจ้งเตือน ให้ดู[การแจ้งเตือนข้อมูลใน Power BI](../create-reports/service-set-data-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="49917-147">To learn how to create an alert, see [Data alerts in Power BI](../create-reports/service-set-data-alerts.md).</span></span>

    :::image type="content" source="media/service-flow-integration/power-automate-select-alert-id-scratch.png" alt-text="สกรีนช็อตของการเลือกชื่อของการแจ้งเตือน":::   

2. <span data-ttu-id="49917-149">เลือก **ขั้นตอนใหม่**</span><span class="sxs-lookup"><span data-stu-id="49917-149">Select **New step**.</span></span>
   
3. <span data-ttu-id="49917-150">ใน **เลือกการดำเนินการ** ค้นหา **Outlook** > **สร้างกิจกรรม**</span><span class="sxs-lookup"><span data-stu-id="49917-150">In **Choose an action**, search for **Outlook** > **Create event**.</span></span>

    :::image type="content" source="media/service-flow-integration/power-automate-choose-action-create-event.png" alt-text="สกรีนช็อตของการเลือกการดำเนินการ > สร้างเหตุการณ์":::   
4. <span data-ttu-id="49917-152">กรอกเขตข้อมูลในช่องเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="49917-152">Fill in the event fields.</span></span> <span data-ttu-id="49917-153">เมื่อคุณเลือกเขตข้อมูล โฟลว์ Power Automate จะแสดงเนื้อหาแบบไดนามิกที่คุณสามารถรวมไว้ได้</span><span class="sxs-lookup"><span data-stu-id="49917-153">As you select a field, Power Automate displays dynamic content that you can include.</span></span>
   
   ![สกรีนช็อตของการดำเนินต่อเพื่อสร้างโฟลว์](media/service-flow-integration/power-bi-flow-event.png)
5. <span data-ttu-id="49917-155">ให้เลือก **สร้างโฟลว์** เมื่อทำเสร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="49917-155">Select **Create flow** when done.</span></span>  <span data-ttu-id="49917-156">Power Automate จะบันทึกและประเมินโฟลว์</span><span class="sxs-lookup"><span data-stu-id="49917-156">Power Automate saves and evaluates the flow.</span></span> <span data-ttu-id="49917-157">ถ้าไม่ มีข้อผิดพลาด ให้เลือก **เสร็จสิ้น** เพื่อเรียกใช้โฟลว์นี้</span><span class="sxs-lookup"><span data-stu-id="49917-157">If there are no errors, select **Done** to run this flow.</span></span>  <span data-ttu-id="49917-158">ขั้นตอนใหม่ถูกเพิ่มลงในหน้า **โฟลว์ของฉัน**</span><span class="sxs-lookup"><span data-stu-id="49917-158">The new flow is added to your **My flows** page.</span></span>
   
   ![สกรีนช็อตของการเสร็จสิ้นการสร้างโฟลว์](media/service-flow-integration/power-bi-flow-running.png)
6. <span data-ttu-id="49917-160">เมื่อโฟลว์ถูกทริกเกอร์ โดยการแจ้งเตือนข้อมูล Power BI คุณจะได้รับการแจ้งเตือนเหตุการณ์บน Outlook ที่คล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="49917-160">When the flow is triggered by your Power BI data alert, you'll receive an Outlook event notification similar to this one.</span></span>
   
    ![สกรีนช็อตของ Power Automate ทริกเกอร์การแจ้งเตือนเหตุการณ์บน Outlook](media/service-flow-integration/power-bi-flow-notice.png)

## <a name="next-steps"></a><span data-ttu-id="49917-162">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="49917-162">Next steps</span></span>
* [<span data-ttu-id="49917-163">เริ่มต้นใช้งาน Power Automate</span><span class="sxs-lookup"><span data-stu-id="49917-163">Get started with Power Automate</span></span>](/power-automate/getting-started/)
* [<span data-ttu-id="49917-164">ส่งออกและส่งอีเมลรายงาน Power BI ด้วย Power Automate</span><span class="sxs-lookup"><span data-stu-id="49917-164">Export and email a Power BI report with Power Automate</span></span>](service-automate-power-bi-report-export.md)
* <span data-ttu-id="49917-165">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="49917-165">More questions?</span></span> [<span data-ttu-id="49917-166">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="49917-166">Try the Power BI Community</span></span>](https://community.powerbi.com/)
