---
title: ร่วมมือทำงานในพื้นที่ทำงานดั้งเดิม
description: อ่านเกี่ยวกับการทำงานร่วมกันบนไฟล์ Power BI Desktop ในพื้นที่ทำงาน และกับบริการของ Microsoft 365 เช่น การแชร์ไฟล์บน OneDrive for Business, การสนทนาใน Exchange, ปฏิทิน และงาน
author: maggiesMSFT
ms.author: maggies
ms.reviewer: lukaszp
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 07/25/2019
LocalizationGroup: Share your work
ms.openlocfilehash: 9017d5c938ec0382e2fb27b00e7fe08945e10a5b
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96407641"
---
# <a name="collaborate-in-a-classic-workspace"></a><span data-ttu-id="e2eff-103">ร่วมมือทำงานในพื้นที่ทำงานดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="e2eff-103">Collaborate in a classic workspace</span></span>
<span data-ttu-id="e2eff-104">พื้นที่ทำงาน Power BI คือตำแหน่งที่ยอดเยี่ยมเพื่อทำงานร่วมกับเพื่อนร่วมงานของคุณบนแดชบอร์ด รายงาน และชุดข้อมูลเพื่อสร้าง *แอป*</span><span class="sxs-lookup"><span data-stu-id="e2eff-104">Power BI workspaces are great places to collaborate with your colleagues on dashboards, reports, and datasets to create *apps*.</span></span> <span data-ttu-id="e2eff-105">บทความนี้เกี่ยวกับพื้นที่ทำงานดั้งเดิมแบบ *ดั้งเดิม*</span><span class="sxs-lookup"><span data-stu-id="e2eff-105">This article is about the original, *classic* workspaces.</span></span>  

<span data-ttu-id="e2eff-106">ทำงานร่วมกันไม่ได้จบด้วยพื้นที่ทำงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="e2eff-106">Collaboration doesn’t end with workspaces in Power BI.</span></span> <span data-ttu-id="e2eff-107">เมื่อคุณสร้างพื้นที่ทำงานแบบดั้งเดิมหนึ่งรายการใน Power BI คุณจะสร้าง Microsoft 365 Group ในพื้นหลังโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e2eff-107">When you create one of the classic workspaces in Power BI, you're automatically creating a Microsoft 365 group in the background.</span></span> <span data-ttu-id="e2eff-108">Microsoft 365 จะเสนอบริการของกลุ่มอื่น ๆ เช่น การแชร์ไฟล์บน OneDrive for Business, การสนทนาใน Exchange, ปฏิทินและงานที่แชร์ และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="e2eff-108">Microsoft 365 offers other group services, such as sharing files on OneDrive for Business, conversations in Exchange, shared calendar and tasks, and so on.</span></span> <span data-ttu-id="e2eff-109">อ่านเพิ่มเติมเกี่ยวกับ[กลุ่มใน Microsoft 365](https://support.office.com/article/Create-a-group-in-Office-365-7124dc4c-1de9-40d4-b096-e8add19209e9)</span><span class="sxs-lookup"><span data-stu-id="e2eff-109">Read more about [groups in Microsoft 365](https://support.office.com/article/Create-a-group-in-Office-365-7124dc4c-1de9-40d4-b096-e8add19209e9).</span></span>

> [!NOTE]
> <span data-ttu-id="e2eff-110">ประสบการณ์พื้นที่ทำงานใหม่จะเปลี่ยนความสัมพันธ์ระหว่างพื้นที่ทำงาน Power BI และ Microsoft 365 Group</span><span class="sxs-lookup"><span data-stu-id="e2eff-110">The new workspace experience changes the relationship between Power BI workspaces and Microsoft 365 groups.</span></span> <span data-ttu-id="e2eff-111">เมื่อคุณสร้างพื้นที่ทำงานแบบใหม่หนึ่งรายการใน Power BI คุณจะไม่สร้าง Microsoft 365 Group ในพื้นหลังโดยอัตโนมัติอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="e2eff-111">When you create one of the new workspaces in Power BI, you no longer automatically create a Microsoft 365 group in the background.</span></span> <span data-ttu-id="e2eff-112">สำหรับข้อมูลเพิ่มเติม ดู [สร้างพื้นที่ทำงานใหม่ใน Power BI](service-create-the-new-workspaces.md)</span><span class="sxs-lookup"><span data-stu-id="e2eff-112">For more information, see [Create the new workspaces in Power BI](service-create-the-new-workspaces.md).</span></span>

<span data-ttu-id="e2eff-113">คุณต้องมี[สิทธิ์การใช้งาน Power BI Pro](../fundamentals/service-features-license-type.md) เพื่อสร้างพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="e2eff-113">You need a [Power BI Pro license](../fundamentals/service-features-license-type.md) to create a workspace.</span></span>

## <a name="collaborate-on-power-bi-desktop-files-in-a-workspace"></a><span data-ttu-id="e2eff-114">ทำงานร่วมกันบนไฟล์ Power BI Desktop ในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="e2eff-114">Collaborate on Power BI Desktop files in a workspace</span></span>
<span data-ttu-id="e2eff-115">หลังจากที่คุณสร้างไฟล์ Power BI Desktop คุณสามารถเผยแพร่ไปยังพื้นที่ทำงาน เพื่อให้ทุกคนในพื้นที่ทำงานของคุณจะสามารถทำงานร่วมกันได้</span><span class="sxs-lookup"><span data-stu-id="e2eff-115">After you create a Power BI Desktop file, you can publish it to a workspace so everyone in the workspace can collaborate on it.</span></span>

1. <span data-ttu-id="e2eff-116">ใน Power BI Desktop ให้เลือก **เผยแพร่** บนริบบอน **หน้าแรก** จากนั้นเลือกพื้นที่ทำงานในกล่อง **เลือกปลายทาง**</span><span class="sxs-lookup"><span data-stu-id="e2eff-116">In Power BI Desktop, select **Publish** on the **Home** ribbon, then select the workspace in the **Select a destination** box.</span></span>
   
    ![ไอคอนการเผยแพร่](media/service-collaborate-power-bi-workspace/power-bi-group-publish-pbix.png)
2. <span data-ttu-id="e2eff-118">ใน Power BI service เลือกลูกศรที่อยู่ถัดจาก **พื้นที่ทำงาน** > เลือกพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="e2eff-118">In the Power BI service, select the arrow next to **Workspaces** > select the workspace.</span></span>
   
    ![พื้นที่ทำงาน](media/service-collaborate-power-bi-workspace/power-bi-workspace-nav-arrow.png)
3. <span data-ttu-id="e2eff-120">เลือกแท็บ **รายงาน** จากนั้นเลือกรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="e2eff-120">Select the **Reports** tab, then choose your report.</span></span>
   
    ![แท็บรายงาน](media/service-collaborate-power-bi-workspace/power-bi-workspace-report.png)
   
    <span data-ttu-id="e2eff-122">จากที่นี่ มันเหมือนกับรายงานอื่นๆ ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="e2eff-122">From here, it's like any other report in Power BI.</span></span> <span data-ttu-id="e2eff-123">คุณและผู้อื่นในพื้นที่ทำงานสามารถปรับเปลี่ยนรายงาน และบันทึกไทล์ไปยังแดชบอร์ดที่คุณเลือกได้</span><span class="sxs-lookup"><span data-stu-id="e2eff-123">You and others in the workspace can modify the report and save tiles to a dashboard of your choosing.</span></span>

## <a name="collaborate-in-microsoft-365"></a><span data-ttu-id="e2eff-124">ทำงานร่วมกันใน Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="e2eff-124">Collaborate in Microsoft 365</span></span>
<span data-ttu-id="e2eff-125">การทำงานร่วมกันใน Microsoft 365 เริ่มต้นจากพื้นที่ทำงานแบบดั้งเดิมใน Power BI</span><span class="sxs-lookup"><span data-stu-id="e2eff-125">Collaborating in Microsoft 365 starts from the classic workspace in Power BI.</span></span>

1. <span data-ttu-id="e2eff-126">ในบริการของ Power BI เลือกลูกศรอยู่ถัดจาก **พื้นที่ทำงาน** > เลือก **ตัวเลือกเพิ่มเติม** (... ) ถัดจากชื่อพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="e2eff-126">In the Power BI service, select the arrow next to **Workspaces** > select **More options** (...) next to your workspace name.</span></span> 
   
   ![เมนูพื้นที่ทำงาน](media/service-collaborate-power-bi-workspace/power-bi-app-ellipsis.png)
2. <span data-ttu-id="e2eff-128">จากเมนูนี้ คุณสามารถทำงานร่วมกันกับกลุ่มของคุณในสองสามวิธี</span><span class="sxs-lookup"><span data-stu-id="e2eff-128">From this menu, you can collaborate with your group in a few ways:</span></span> 
   
   * <span data-ttu-id="e2eff-129">มี[กลุ่มการสนทนาใน Microsoft 365](#have-a-group-conversation-in-microsoft-365)</span><span class="sxs-lookup"><span data-stu-id="e2eff-129">Have a [group conversation in Microsoft 365](#have-a-group-conversation-in-microsoft-365).</span></span>
   * <span data-ttu-id="e2eff-130">[กำหนดเหตุการณ์](#schedule-an-event-on-the-group-workspace-calendar)บนปฏิทินของพื้นที่ทำงานของกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="e2eff-130">[Schedule an event](#schedule-an-event-on-the-group-workspace-calendar) on the group workspace calendar.</span></span>
   
   <span data-ttu-id="e2eff-131">ครั้งแรกที่คุณไปยังพื้นที่ทำงานของกลุ่มคุณใน Microsoft 365 ซึ่งอาจใช้เวลาสักครู่</span><span class="sxs-lookup"><span data-stu-id="e2eff-131">The first time you go to your group workspace in Microsoft 365, it may take some time.</span></span> <span data-ttu-id="e2eff-132">รอ 15 ถึง 30 นาที จากนั้นรีเฟรชเบราว์เซอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e2eff-132">Give it 15 to 30 minutes, then refresh your browser.</span></span>

## <a name="have-a-group-conversation-in-microsoft-365"></a><span data-ttu-id="e2eff-133">มีกลุ่มการสนทนาใน Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="e2eff-133">Have a group conversation in Microsoft 365</span></span>
1. <span data-ttu-id="e2eff-134">เลือก **ตัวเลือกเพิ่มเติม** (...) ที่อยู่ถัดจากชื่อพื้นที่ทำงานของคุณ\> **การสนทนา**</span><span class="sxs-lookup"><span data-stu-id="e2eff-134">Select **More options** (...) next to your workspace name \> **Conversations**.</span></span> 
   
    ![แท็บการสนทนา](media/service-collaborate-power-bi-workspace/power-bi-app-ellipsis.png)
   
   <span data-ttu-id="e2eff-136">เว็บไซต์อีเมลและการสนทนาสำหรับพื้นที่ทำงานของกลุ่มคุณเปิดขึ้นใน Outlook for Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="e2eff-136">The email and conversation site for your group workspace opens in Outlook for Microsoft 365.</span></span>
   
   ![รายการเมนูปฏิทิน](media/service-collaborate-power-bi-workspace/pbi_grps_o365convo.png)
2. <span data-ttu-id="e2eff-138">อ่านเพิ่มเติมเกี่ยวกับ[กลุ่มการสนทนาใน Outlook for Microsoft 365](https://support.office.com/Article/Have-a-group-conversation-a0482e24-a769-4e39-a5ba-a7c56e828b22)</span><span class="sxs-lookup"><span data-stu-id="e2eff-138">Read more about [group conversations in Outlook for Microsoft 365](https://support.office.com/Article/Have-a-group-conversation-a0482e24-a769-4e39-a5ba-a7c56e828b22).</span></span>

## <a name="schedule-an-event-on-the-group-workspace-calendar"></a><span data-ttu-id="e2eff-139">กำหนดเหตุการณ์บนปฏิทินของพื้นที่ทำงานของกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="e2eff-139">Schedule an event on the group workspace calendar</span></span>
1. <span data-ttu-id="e2eff-140">เลือก **ตัวเลือกเพิ่มเติม** (...) ที่อยู่ถัดจากชื่อพื้นที่ทำงาน\> **ปฏิทิน**</span><span class="sxs-lookup"><span data-stu-id="e2eff-140">Select **More options** (...) next to the workspace name \> **Calendar**.</span></span> 
   
   ![แท็บปฏิทิน](media/service-collaborate-power-bi-workspace/power-bi-app-ellipsis.png)
   
   <span data-ttu-id="e2eff-142">ปฏิทินสำหรับพื้นที่ทำงานของกลุ่มคุณจะเปิดขึ้นใน Outlook for Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="e2eff-142">The calendar for your group workspace opens in Outlook for Microsoft 365.</span></span>
   
   ![Outlook for Microsoft 365](media/service-collaborate-power-bi-workspace/pbi_grps_o365_calendar.png)
2. <span data-ttu-id="e2eff-144">อ่านเพิ่มเติมเกี่ยวกับ[กลุ่มปฏิทินใน Outlook ใน Microsoft 365](https://support.office.com/Article/Add-edit-and-subscribe-to-group-events-0cf1ad68-1034-4306-b367-d75e9818376a)</span><span class="sxs-lookup"><span data-stu-id="e2eff-144">Read more about [group calendars in Outlook in Microsoft 365](https://support.office.com/Article/Add-edit-and-subscribe-to-group-events-0cf1ad68-1034-4306-b367-d75e9818376a).</span></span>

## <a name="manage-a-classic-workspace"></a><span data-ttu-id="e2eff-145">จัดการพื้นที่ทำงานแบบดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="e2eff-145">Manage a classic workspace</span></span>
<span data-ttu-id="e2eff-146">ถ้าคุณเป็นเจ้าของหรือผู้ดูแลระบบของพื้นที่ทำงาน คุณสามารถเพิ่มหรือลบสมาชิกในพื้นที่ทำงานได้</span><span class="sxs-lookup"><span data-stu-id="e2eff-146">If you’re an owner or administrator for a workspace, you can also add or remove workspace members.</span></span> <span data-ttu-id="e2eff-147">อ่านเพิ่มเติมเกี่ยวกับ [การจัดการพื้นที่ทำงานของ Power BI](service-manage-app-workspace-in-power-bi-and-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="e2eff-147">Read more about [managing a Power BI workspace](service-manage-app-workspace-in-power-bi-and-office-365.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="e2eff-148">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="e2eff-148">Next steps</span></span>
* <span data-ttu-id="e2eff-149">[เผยแพร่แอปใน Power BI](service-create-distribute-apps.md)</span><span class="sxs-lookup"><span data-stu-id="e2eff-149">[Publish apps in Power BI](service-create-distribute-apps.md).</span></span>
* <span data-ttu-id="e2eff-150">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="e2eff-150">More questions?</span></span> <span data-ttu-id="e2eff-151">[ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="e2eff-151">[Try the Power BI Community](https://community.powerbi.com/).</span></span>
* <span data-ttu-id="e2eff-152">มีคำติชมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="e2eff-152">Feedback?</span></span> <span data-ttu-id="e2eff-153">เยี่ยมชม[แนวคิด Power BI](https://ideas.powerbi.com/forums/265200-power-bi)</span><span class="sxs-lookup"><span data-stu-id="e2eff-153">Visit [Power BI Ideas](https://ideas.powerbi.com/forums/265200-power-bi).</span></span>
