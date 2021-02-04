---
title: แชทใน Microsoft Teams โดยตรงจากบริการ Power BI
description: คุณสามารถแชร์แดชบอร์ดและรายงาน Power BI จากบริการของ Power BI ไปยัง Microsoft Teams ได้โดยตรง
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
LocalizationGroup: Share your work
ms.date: 01/04/2020
ms.openlocfilehash: 63ea4772610bd7112823f38c66abced1f0654b77
ms.sourcegitcommit: 932f6856849c39e34229dc9a49fb9379c56a888a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/06/2021
ms.locfileid: "97926966"
---
# <a name="chat-in-microsoft-teams-directly-from-the-power-bi-service"></a><span data-ttu-id="b29a6-103">แชทใน Microsoft Teams โดยตรงจากบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="b29a6-103">Chat in Microsoft Teams directly from the Power BI service</span></span>

<span data-ttu-id="b29a6-104">คุณสามารถพูดคุยเกี่ยวกับแดชบอร์ด รายงาน และภาพของ Power BI ใน Microsoft Teams ได้โดยตรงจากบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="b29a6-104">You can chat about Power BI dashboards, reports, and visuals directly to Microsoft Teams from the Power BI service.</span></span> <span data-ttu-id="b29a6-105">ใช้คุณลักษณะ **แชทใน Teams** เพื่อเริ่มการสนทนาอย่างรวดเร็วเมื่อคุณดูรายงานและแดชบอร์ดในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="b29a6-105">Use the **Chat in Teams** feature to quickly start conversations when you view reports and dashboards in the Power BI service.</span></span>

## <a name="requirements"></a><span data-ttu-id="b29a6-106">ข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="b29a6-106">Requirements</span></span>

<span data-ttu-id="b29a6-107">เมื่อต้องการใช้ฟังก์ชัน **แชทใน Teams** ใน Power BI ตรวจสอบให้แน่ใจว่าผู้ดูแลระบบ Power BI ของคุณไม่ได้ปิดใช้งานการตั้งค่าผู้เช่าสำหรับ **แชร์ไปยัง Teams** ในพอร์ทัลผู้ดูแลระบบ Power BI</span><span class="sxs-lookup"><span data-stu-id="b29a6-107">To use the **Chat in Teams** functionality in Power BI, make sure your Power BI administrator hasn't disabled the **Share to Teams** tenant setting in the Power BI admin portal.</span></span> <span data-ttu-id="b29a6-108">การตั้งค่านี้ช่วยให้องค์กรสามารถซ่อนปุ่ม **แชทใน Teams** ได้</span><span class="sxs-lookup"><span data-stu-id="b29a6-108">This setting allows organizations to hide the **Chat in Teams** buttons.</span></span> <span data-ttu-id="b29a6-109">ดูรายละเอียดที่บทความ[พอร์ทัลผู้ดูแลระบบ Power BI](../admin/service-admin-portal.md#share-to-teams)</span><span class="sxs-lookup"><span data-stu-id="b29a6-109">See the [Power BI admin portal](../admin/service-admin-portal.md#share-to-teams) article for details.</span></span>

<span data-ttu-id="b29a6-110">ดู [การทำงานร่วมกันใน Microsoft Teams ด้วย Power BI](service-collaborate-microsoft-teams.md) สำหรับเบื้องหลังเกี่ยวกับวิธีที่ระบบ Power Bi และ Microsoft Teams ทำงานร่วมกัน รวมถึงข้อกำหนดต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="b29a6-110">See [Collaborate in Microsoft Teams with Power BI](service-collaborate-microsoft-teams.md) for background on how Power BI and Microsoft Teams work together, including other requirements.</span></span>

## <a name="chat-about-power-bi-content-in-microsoft-teams"></a><span data-ttu-id="b29a6-111">พูดคุยเกี่ยวกับเนื้อหา Power BI ใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b29a6-111">Chat about Power BI content in Microsoft Teams</span></span>

<span data-ttu-id="b29a6-112">ทําตามขั้นตอนเหล่านี้เพื่อแชร์ลิงก์ไปยังรายงาน แดชบอร์ด และภาพในบริการ Power BI และพูดคุยเกี่ยวกับช่องและแชทของ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b29a6-112">Follow these steps to share links to reports, dashboards, and visuals in the Power BI service, and chat about Microsoft Teams channels and chats.</span></span>

1. <span data-ttu-id="b29a6-113">เลือกหนึ่งในตัวเลือกเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="b29a6-113">Select one of these options:</span></span>

   * <span data-ttu-id="b29a6-114">**แชทใน Teams** ในแถบการดำเนินการของแดชบอร์ดหรือรายงาน:</span><span class="sxs-lookup"><span data-stu-id="b29a6-114">**Chat in Teams** in the action bar of a dashboard or report:</span></span>

       ![สกรีนช็อตของปุ่มสนทนาในทีมในแถบการดำเนินการ](media/service-share-report-teams/service-teams-share-to-teams-action-bar-button.png)
    
   * <span data-ttu-id="b29a6-116">**แชทใน Teams** ในเมนูบริบทสําหรับวิชวลเดียว:</span><span class="sxs-lookup"><span data-stu-id="b29a6-116">**Chat in Teams** in the context menu for a single visual:</span></span>
    
      ![สกรีนช็อตของปุ่มสนทนาในทีมในเมนูบริบทการแสดงผลด้วยภาพ](media/service-share-report-teams/service-teams-share-to-teams-visual-context-menu.png)

1. <span data-ttu-id="b29a6-118">ในกล่องโต้ตอบ **แชร์กับ Microsoft Teams** ให้เลือกทีมหรือช่องที่คุณต้องการส่งลิงก์ไปให้</span><span class="sxs-lookup"><span data-stu-id="b29a6-118">In the **Share to Microsoft Teams** dialog box, select the team or channel you want to send the link to.</span></span> <span data-ttu-id="b29a6-119">เพิ่มข้อความถ้าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="b29a6-119">You can enter a message if you want.</span></span> <span data-ttu-id="b29a6-120">คุณอาจถูกขอให้ลงชื่อเข้าใช้ Microsoft Teams ก่อน</span><span class="sxs-lookup"><span data-stu-id="b29a6-120">You might be asked to sign in to Microsoft Teams first.</span></span>

    ![ภาพหน้าจอของแชร์ไปยังกล่องโต้ตอบ Microsoft Teams ด้วยข้อมูลและข้อความ](media/service-share-report-teams/service-teams-share-to-teams-dialog.png)

1. <span data-ttu-id="b29a6-122">เลือก **แชร์** เพื่อส่งลิงก์</span><span class="sxs-lookup"><span data-stu-id="b29a6-122">Select **Share** to send the link.</span></span>
    
1. <span data-ttu-id="b29a6-123">ลิงก์จะถูกเพิ่มไปยังการสนทนาที่มีอยู่หรือเริ่มการสนทนาใหม่</span><span class="sxs-lookup"><span data-stu-id="b29a6-123">The link is added to existing conversations or starts a new chat.</span></span>

    ![ภาพหน้าจอของการสนทนาของ Microsoft Teams ที่มีลิงก์ไปยังรายการ Power BI](media/service-share-report-teams/service-teams-share-to-teams-deep-link.png)

1. <span data-ttu-id="b29a6-125">เลือกลิงก์เพื่อเปิดรายการในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="b29a6-125">Select the link to open the item in the Power BI service.</span></span>

1. <span data-ttu-id="b29a6-126">ถ้าคุณใช้เมนูบริบทสำหรับภาพที่ระบุ ภาพจะถูกไฮไลท์เมื่อรายงานเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="b29a6-126">If you used the contextual menu for a specific visual, the visual is highlighted when the report opens.</span></span>

    ![ภาพหน้าจอของรายงาน Power BI ที่เปิดด้วยวิชวลเฉพาะที่มีการไฮไลต์ไว้](media/service-share-report-teams/service-teams-share-to-teams-spotlight-visual.png)


## <a name="known-issues-and-limitations"></a><span data-ttu-id="b29a6-128">ปัญหาและขีดจำกัดที่ทราบแล้ว</span><span class="sxs-lookup"><span data-stu-id="b29a6-128">Known issues and limitations</span></span>

- <span data-ttu-id="b29a6-129">ผู้ใช้ที่ไม่มีสิทธิ์การใช้งาน Power BI หรือสิทธิ์ในการเข้าถึงรายงานจะเห็นข้อความ "เนื้อหาไม่พร้อมใช้งาน"</span><span class="sxs-lookup"><span data-stu-id="b29a6-129">Users without a Power BI license or permission to access the report see a "Content is not available" message.</span></span>
- <span data-ttu-id="b29a6-130">ปุ่ม **แชทใน Teams** อาจไม่ทำงาน หากเบราว์เซอร์ของคุณใช้การตั้งค่าความเป็นส่วนตัวที่เข้มงวด</span><span class="sxs-lookup"><span data-stu-id="b29a6-130">The **Chat in Teams** buttons might not work if your browser uses strict privacy settings.</span></span> <span data-ttu-id="b29a6-131">ใช้ **ยังพบปัญหาอยู่ใช่หรือไม่? ลองเปิดในตัวเลือกหน้าต่างใหม่** ถ้ากล่องโต้ตอบไม่เปิดอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="b29a6-131">Use the **Having trouble? Try opening in a new window** option if the dialog box doesn't open correctly.</span></span>
- <span data-ttu-id="b29a6-132">**แชทใน Teams** ไม่รวมการแสดงตัวอย่างลิงก์</span><span class="sxs-lookup"><span data-stu-id="b29a6-132">**Chat in Teams** doesn't include a link preview.</span></span>
- <span data-ttu-id="b29a6-133">การแสดงตัวอย่างลิงก์และ **แชทใน Teams** ไม่อนุญาตให้ผู้ใช้ดูรายการ</span><span class="sxs-lookup"><span data-stu-id="b29a6-133">Link previews and **Chat in Teams** don't give users permissions to view the item.</span></span> <span data-ttu-id="b29a6-134">สิทธิ์ต้องได้รับการจัดการแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="b29a6-134">Permissions must be managed separately.</span></span>
- <span data-ttu-id="b29a6-135">ปุ่ม **แชทใน Teams** ไม่พร้อมใช้งานในเมนูบริบทวิชวล เมื่อผู้สร้างรายงานตั้งค่า **ตัวเลือกเพิ่มเติม** เป็น **ปิด** สำหรับวิชวล</span><span class="sxs-lookup"><span data-stu-id="b29a6-135">The **Chat in Teams** button isn't available in visual context menus when a report author sets **More options** to **Off** for the visual.</span></span>
- <span data-ttu-id="b29a6-136">ดูปัญหาอื่น ๆ ที่หัวข้อ[ปัญหาที่ทราบแล้วและข้อจำกัดต่าง ๆ](service-collaborate-microsoft-teams.md#known-issues-and-limitations) ในบทความ “ทำงานร่วมกันใน Microsoft Teams"</span><span class="sxs-lookup"><span data-stu-id="b29a6-136">See the [Known issues and limitations](service-collaborate-microsoft-teams.md#known-issues-and-limitations) section of the "Collaborate in Microsoft Teams" article for other issues.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b29a6-137">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="b29a6-137">Next steps</span></span>

- [<span data-ttu-id="b29a6-138">ทำงานร่วมกันใน Microsoft Teams ด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="b29a6-138">Collaborate in Microsoft Teams with Power BI</span></span>](service-collaborate-microsoft-teams.md)

<span data-ttu-id="b29a6-139">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="b29a6-139">More questions?</span></span> <span data-ttu-id="b29a6-140">[ลองถามชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="b29a6-140">[Try asking the Power BI Community](https://community.powerbi.com/).</span></span>
