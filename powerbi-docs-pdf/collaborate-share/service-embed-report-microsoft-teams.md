---
title: ฝังรายงาน Power BI ใน Microsoft Teams
description: คุณสามารถฝังรายงาน Power BI แบบโต้ตอบในช่องทางการสื่อสารและการสนทนาของ Microsoft Teams ได้อย่างง่ายดาย .
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: conceptual
LocalizationGroup: Share your work
ms.date: 09/21/2020
ms.openlocfilehash: 36973d52f94b806db860b739a84f0c94b2a8945d
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411873"
---
# <a name="embed-power-bi-content-in-microsoft-teams"></a><span data-ttu-id="7ab71-104">ฝังเนื้อหา Power BI ใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7ab71-104">Embed Power BI content in Microsoft Teams</span></span>

<span data-ttu-id="7ab71-105">คุณสามารถฝังรายงาน Power BI แบบโต้ตอบในช่องทางการสื่อสารและการสนทนาของ Microsoft Teams ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="7ab71-105">You can easily embed interactive Power BI reports in Microsoft Teams channels and chats.</span></span> 

## <a name="requirements"></a><span data-ttu-id="7ab71-106">ข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="7ab71-106">Requirements</span></span>

<span data-ttu-id="7ab71-107">หากต้องการใช้แท็บ **Power BI** ใน Microsoft Teams ให้ตรวจสอบองค์ประกอบต่าง ๆ เหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="7ab71-107">To use the **Power BI** tab in Microsoft Teams, ensure these elements:</span></span>

- <span data-ttu-id="7ab71-108">Microsoft Teams มีแท็บ **Power BI**</span><span class="sxs-lookup"><span data-stu-id="7ab71-108">Microsoft Teams has the **Power BI** tab.</span></span>
- <span data-ttu-id="7ab71-109">หากต้องการเพิ่มรายงานใน Microsoft Teams ด้วยแท็บ **Power BI** อย่างน้อยคุณต้องมีบทบาทผู้ชมในพื้นที่ทำงานที่โฮสต์รายงาน</span><span class="sxs-lookup"><span data-stu-id="7ab71-109">To add a report in Microsoft Teams with the **Power BI** tab, you have at least a Viewer role in the workspace that hosts the report.</span></span> <span data-ttu-id="7ab71-110">ดู[บทบาทในพื้นที่ทำงานใหม่](service-new-workspaces.md#roles-in-the-new-workspaces)สำหรับข้อมูลเกี่ยวกับบทบาทที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="7ab71-110">For information about the different roles, see [Roles in the new workspaces](service-new-workspaces.md#roles-in-the-new-workspaces).</span></span>
- <span data-ttu-id="7ab71-111">หากต้องการดูรายงานในแท็บ **Power BI** ใน Microsoft Teams ผู้ใช้ต้องมีสิทธิ์ในการดูรายงาน</span><span class="sxs-lookup"><span data-stu-id="7ab71-111">To see the report in the **Power BI** tab in Microsoft Teams, users must have permission to view the report.</span></span>
- <span data-ttu-id="7ab71-112">ผู้ใช้จะต้องเป็นผู้ใช้  Microsoft Teams ที่มีสิทธิ์เข้าถึงช่องและการสนทนา</span><span class="sxs-lookup"><span data-stu-id="7ab71-112">Users must be Microsoft Teams users with access to channels and chats.</span></span>

<span data-ttu-id="7ab71-113">ดู[การทำงานร่วมกันใน Microsoft Teams ด้วย Power BI](service-embed-report-microsoft-teams.md) สำหรับเบื้องหลังเกี่ยวกับวิธีที่ระบบ Power Bi และ Microsoft Teams ทำงานร่วมกัน รวมถึงข้อกำหนดต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="7ab71-113">See [Collaborate in Microsoft Teams with Power BI](service-embed-report-microsoft-teams.md) for background on how Power BI and Microsoft Teams work together, including other requirements.</span></span>

## <a name="embed-a-report-in-microsoft-teams"></a><span data-ttu-id="7ab71-114">ฝังรายงานใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7ab71-114">Embed a report in Microsoft Teams</span></span>

<span data-ttu-id="7ab71-115">ทำตามขั้นตอนเหล่านี้เพื่อฝังรายงานของคุณลงในแชนเนลหรือแชทของ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7ab71-115">Follow these steps to embed your report in a Microsoft Teams channel or chat.</span></span>

1. <span data-ttu-id="7ab71-116">เปิดแชนเนลหรือแชทใน Microsoft Teams และเลือกไอคอน **+**</span><span class="sxs-lookup"><span data-stu-id="7ab71-116">Open a channel or chat in Microsoft Teams, and select the **+** icon.</span></span>

    ![ภาพหน้าจอของเพิ่มแท็บไปยังช่องทางการสื่อสารหรือการสนทนา](media/service-embed-report-microsoft-teams/service-embed-report-microsoft-teams-add.png)

1. <span data-ttu-id="7ab71-118">เลือกแท็บ **Power BI**</span><span class="sxs-lookup"><span data-stu-id="7ab71-118">Select the **Power BI** tab.</span></span>

    ![ภาพหน้าจอของรายการแท็บ Microsoft Teams ที่แสดง Power BI](media/service-embed-report-microsoft-teams/service-embed-report-microsoft-teams-tab.png)

1. <span data-ttu-id="7ab71-120">ใช้ตัวเลือกที่ให้มาเพื่อเลือกรายงานจากพื้นที่ทำงานหรือแอป Power BI</span><span class="sxs-lookup"><span data-stu-id="7ab71-120">Use the provided options to select a report from a workspace or a Power BI app.</span></span>

    ![ภาพหน้าจอของแท็บ Power B I สำหรับการตั้งค่า Microsoft Teams](media/service-embed-report-microsoft-teams/service-embed-report-microsoft-teams-tab-settings.png)

1. <span data-ttu-id="7ab71-122">ชื่อแท็บจะอัปเดตโดยอัตโนมัติเพื่อให้ตรงกับชื่อของชื่อรายงาน แต่คุณสามารถเปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="7ab71-122">The tab name updates automatically to match the name of the report name, but you can change it.</span></span>

1. <span data-ttu-id="7ab71-123">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7ab71-123">Select **Save**.</span></span>

### <a name="reports-you-can-embed-on-the-power-bi-tab"></a><span data-ttu-id="7ab71-124">รายงานที่คุณสามารถฝังบนแท็บ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="7ab71-124">Reports you can embed on the Power BI tab</span></span>

<span data-ttu-id="7ab71-125">คุณสามารถฝังรายงานประเภทต่อไปนี้ได้บนแท็บ **Power BI**:</span><span class="sxs-lookup"><span data-stu-id="7ab71-125">You can embed the following types of reports on the **Power BI** tab:</span></span>

- <span data-ttu-id="7ab71-126">รายงานแบบโต้ตอบและรายงานที่มีการแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="7ab71-126">Interactive and paginated reports.</span></span>
- <span data-ttu-id="7ab71-127">รายงานใน **พื้นที่ทำงานของฉัน** ประสบการณ์พื้นที่ทำงานใหม่ และพื้นที่ทำงานแบบคลาสสิก</span><span class="sxs-lookup"><span data-stu-id="7ab71-127">Reports in **My workspace**, new workspace experiences, and classic workspaces.</span></span>
- <span data-ttu-id="7ab71-128">รายงานในแอป Power BI</span><span class="sxs-lookup"><span data-stu-id="7ab71-128">Reports in Power BI apps.</span></span>

## <a name="start-a-conversation"></a><span data-ttu-id="7ab71-129">เริ่มการสนทนา</span><span class="sxs-lookup"><span data-stu-id="7ab71-129">Start a conversation</span></span>

<span data-ttu-id="7ab71-130">เมื่อคุณเพิ่มแท็บรายงาน Power BI ไปยัง Microsoft Teams จากนั้น Microsoft Teams จะสร้างแท็บการสนทนาสำหรับรายงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7ab71-130">When you add a Power BI report tab to Microsoft Teams, Microsoft Teams automatically creates a tab conversation for the report.</span></span>

- <span data-ttu-id="7ab71-131">เลือกไอคอน **แสดงแท็บการสนทนา** ในมุมบนขวา</span><span class="sxs-lookup"><span data-stu-id="7ab71-131">Select the **Show tab conversation** icon in the upper-right corner.</span></span>

    ![ภาพหน้าจอของไอคอนแสดงแท็บการสนทนา](media/service-embed-report-microsoft-teams/power-bi-teams-conversation-icon.png)

    <span data-ttu-id="7ab71-133">ข้อคิดเห็นแรกคือการเชื่อมโยงไปยังรายงาน</span><span class="sxs-lookup"><span data-stu-id="7ab71-133">The first comment is a link to the report.</span></span> <span data-ttu-id="7ab71-134">ทุกคนในช่องของ Microsoft Teams สามารถดูและพูดคุยเกี่ยวกับรายงานในการสนทนาได้</span><span class="sxs-lookup"><span data-stu-id="7ab71-134">Everyone in that Microsoft Teams channel can see and discuss the report in the conversation.</span></span>

    ![ภาพหน้าจอของแท็บการสนทนา](media/service-embed-report-microsoft-teams/power-bi-teams-conversation-tab.png)

## <a name="known-issues-and-limitations"></a><span data-ttu-id="7ab71-136">ปัญหาและขีดจำกัดที่ทราบแล้ว</span><span class="sxs-lookup"><span data-stu-id="7ab71-136">Known issues and limitations</span></span>

- <span data-ttu-id="7ab71-137">ใน Microsoft Teams เมื่อคุณส่งออกข้อมูลจากวิชวลในรายงาน Power BI ข้อมูลนั้นจะถูกบันทึกไว้ในโฟลเดอร์ ดาวน์โหลด โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7ab71-137">In Microsoft Teams, when you export data from a visual in a Power BI report, it's automatically saved to your Downloads folder.</span></span> <span data-ttu-id="7ab71-138">ซึ่งเป็นไฟล์ Excel ที่ชื่อว่า "data (*n*).xlsx" โดยที่ *n* หมายถึงจำนวนครั้งที่คุณส่งออกข้อมูลไปยังโฟลเดอร์เดียวกันนี้</span><span class="sxs-lookup"><span data-stu-id="7ab71-138">It's an Excel file called "data (*n*).xlsx" where *n* is the number of times you've exported data to the same folder.</span></span>
- <span data-ttu-id="7ab71-139">คุณไม่สามารถฝังแดชบอร์ด Power BI ลงในแท็บ **Power BI** สำหรับ Microsoft Teams ได้</span><span class="sxs-lookup"><span data-stu-id="7ab71-139">You can't embed Power BI dashboards in the **Power BI** tab for Microsoft Teams.</span></span>
- <span data-ttu-id="7ab71-140">ไม่รองรับ [ตัวกรอง URL](service-url-filters.md) ที่มีแท็บ **Power BI** สำหรับ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="7ab71-140">[URL filters](service-url-filters.md) aren't supported with the **Power BI** tab for Microsoft Teams.</span></span>
- <span data-ttu-id="7ab71-141">ในระบบคลาวด์ภายในประเทศ แท็บ **Power BI** ใหม่ไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7ab71-141">In national clouds, the new **Power BI** tab isn't available.</span></span> <span data-ttu-id="7ab71-142">รุ่นที่เก่ากว่าอาจพร้อมใช้งานที่ไม่รองรับพื้นที่ทำงานใหม่ พื้นที่ทำงานที่เคยทำ หรือรายงานในแอป Power BI</span><span class="sxs-lookup"><span data-stu-id="7ab71-142">An older version might be available that doesn't support the new workspace experience or reports in Power BI apps.</span></span>
- <span data-ttu-id="7ab71-143">หลังจากที่คุณบันทึกแท็บแล้ว คุณไม่สามารถเปลี่ยนชื่อแท็บผ่านการตั้งค่าแท็บได้</span><span class="sxs-lookup"><span data-stu-id="7ab71-143">After you save the tab, you don't change the tab name through the tab settings.</span></span> <span data-ttu-id="7ab71-144">ใช้ตัวเลือก **เปลี่ยนชื่อ** เพื่อดำเนินการเปลี่ยนชื่อ</span><span class="sxs-lookup"><span data-stu-id="7ab71-144">Use the **Rename** option to change it.</span></span>
- <span data-ttu-id="7ab71-145">ดูปัญหาอื่น ๆ ที่หัวข้อ[ปัญหาที่ทราบแล้วและข้อจำกัดต่าง ๆ](service-collaborate-microsoft-teams.md#known-issues-and-limitations) ในบทความ “ทำงานร่วมกันใน Microsoft Teams"</span><span class="sxs-lookup"><span data-stu-id="7ab71-145">See the [Known issues and limitations](service-collaborate-microsoft-teams.md#known-issues-and-limitations) section of the "Collaborate in Microsoft Teams" article for other issues.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7ab71-146">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="7ab71-146">Next steps</span></span>

- [<span data-ttu-id="7ab71-147">ทำงานร่วมกันใน Microsoft Teams ด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="7ab71-147">Collaborate in Microsoft Teams with Power BI</span></span>](service-collaborate-microsoft-teams.md)

<span data-ttu-id="7ab71-148">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="7ab71-148">More questions?</span></span> <span data-ttu-id="7ab71-149">[ลองถามชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="7ab71-149">[Try asking the Power BI Community](https://community.powerbi.com/).</span></span>
