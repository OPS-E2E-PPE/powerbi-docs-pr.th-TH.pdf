---
title: การรวมแอปสำหรับอุปกรณ์เคลื่อนที่ของ Power BI ด้วยปุ่มลัด Siri
description: วิธีใช้ปุ่มลัด Siri เพื่อเข้าถึงเนื้อหา Power BI ที่คุณต้องการโดยตรง
author: paulinbar
ms.author: painbar
manager: rkarlin
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 12/01/2020
ms.openlocfilehash: 0bf1fb3f921b195be430e21f6f0b0bf2b0eeb473
ms.sourcegitcommit: 2fd64f96b5bfbc14ff47e5c892171e5c921fb525
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/02/2020
ms.locfileid: "96501983"
---
# <a name="using-siri-shortcuts-in-power-bi-mobile-ios-app"></a><span data-ttu-id="f7189-103">การใช้ปุ่มลัด Siri ในแอป Power BI บนมือถือสำหรับ iOS</span><span class="sxs-lookup"><span data-stu-id="f7189-103">Using Siri Shortcuts in Power BI Mobile iOS App</span></span>

<span data-ttu-id="f7189-104">ใช้ปุ่มลัด Siri เพื่อเข้าถึงเนื้อหา Power BI ที่คุณต้องการโดยตรง</span><span class="sxs-lookup"><span data-stu-id="f7189-104">Use Siri Shortcuts to directly access the Power BI content you need.</span></span>

<span data-ttu-id="f7189-105">เพื่อให้สามารถเข้าถึงรายงานหรือแดชบอร์ดที่ใช้บ่อยๆ ได้อย่างง่ายดายและรวดเร็ว คุณสามารถสร้างทางลัด Siri สำหรับการเข้าถึงเนื้อหา Power BI โดยตรงที่คุณต้องการได้</span><span class="sxs-lookup"><span data-stu-id="f7189-105">To get easy and quick access to your frequently used reports or dashboards, you can create a Siri Shortcut for direct access to the Power BI content you need.</span></span> <span data-ttu-id="f7189-106">ด้วยทางลัด Siri คุณเพียงแค่จำเป็นต้องขอให้ Siri เปิดเมื่อใดก็ตามที่คุณต้องการดูข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f7189-106">With a Siri Shortcut, you just need to ask Siri to open it whenever you need look at the data.</span></span>

> [!NOTE]
> <span data-ttu-id="f7189-107">การรวมทางลัด Siri กับแอป Power BI จะพร้อมใช้งานสำหรับ iPhone และ iPad ที่ทำงานบน iOS12 ขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="f7189-107">The Siri Shortcuts integration with the Power BI mobile app is available for iPhones and iPads running iOS12 and later.</span></span>

## <a name="create-siri-shortcut-for-a-report-or-dashboard"></a><span data-ttu-id="f7189-108">สร้างปุ่มลัด Siri สำหรับรายงานหรือแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="f7189-108">Create Siri shortcut for a report or dashboard</span></span>

<span data-ttu-id="f7189-109">มีสามวิธีในการสร้างปุ่มลัด Siri ไปยังรายงานและแดชบอร์ดของคุณ:</span><span class="sxs-lookup"><span data-stu-id="f7189-109">There are three ways to create Siri shortcuts to your reports and dashboards:</span></span>

- <span data-ttu-id="f7189-110">จะมีการเพิ่มแบนเนอร์พร้อมตัวเลือก **เพิ่มไปยัง Siri** ไปยังรายงานและแดชบอร์ดที่ใช้งานบ่อยของคุณ</span><span class="sxs-lookup"><span data-stu-id="f7189-110">A banner with an **Add to Siri** option will be added to your frequently used reports and dashboards.</span></span> <span data-ttu-id="f7189-111">แตะที่แอคชันเพื่อเปิดหน้า **เพิ่มไปยัง Siri**</span><span class="sxs-lookup"><span data-stu-id="f7189-111">Tap the action to open the **Add to Siri** page.</span></span>
    
- <span data-ttu-id="f7189-112">ใช้แอคชัน **ปุ่มลัด Siri** บน **รายงาน** หรือเมนูแอคชัน **แดชบอร์ด**(...)</span><span class="sxs-lookup"><span data-stu-id="f7189-112">Use the **Siri shortcut** action on the **Report** or **Dashboard** actions menu (...).</span></span>
    
- <span data-ttu-id="f7189-113">ใช้ **ปุ่มลัดที่แนะนำ** ในการตั้งค่าอุปกรณ์ (**การตั้งค่าอุปกรณ์** > **Siri และค้นหา**)</span><span class="sxs-lookup"><span data-stu-id="f7189-113">Use the **Suggested shortcuts** in the device settings (**Device Setting** > **Siri & Search**).</span></span> <span data-ttu-id="f7189-114">คุณสามารถเพิ่มปุ่มลัดไปยังรายการในคำแนะนำ โดยใช้ปุ่มเครื่องหมายบวก (+) ได้</span><span class="sxs-lookup"><span data-stu-id="f7189-114">You can add a shortcut to the item in the suggestion by using the plus (+) button.</span></span>
     
     ![สร้างปุ่มลัด](./media/mobile-apps-ios-siri-search/power-bi-siri-create-shortcut.png)

<span data-ttu-id="f7189-116">สำหรับรายงาน Power BI ปุ่มลัดจะจับภาพหน้าปัจจุบันที่คุณกำลังดูเมื่อสร้างปุ่มลัด</span><span class="sxs-lookup"><span data-stu-id="f7189-116">For a Power BI report, the shortcut will capture the current page that you're viewing when creating the shortcut.</span></span> 

<span data-ttu-id="f7189-117">ตัวเลือกทั้งหมดจะเปิดหน้า **เพิ่มไปยัง Siri**</span><span class="sxs-lookup"><span data-stu-id="f7189-117">All options will open the **Add to Siri** page.</span></span> <span data-ttu-id="f7189-118">ในหน้านี้ คุณจำเป็นต้องบันทึกวลีที่คุณจะใช้ในภายหลังด้วย Siri เพื่อเปิดรายงานหรือแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="f7189-118">In this page, you will need to record a phrase that you will use later with Siri to open the report or dashboard.</span></span> 
   
![เพิ่มไปยังหน้า Siri](./media/mobile-apps-ios-siri-search/power-bi-siri-add-page.png)
    

## <a name="use-siri-shortcuts-to-view-report-or-dashboard"></a><span data-ttu-id="f7189-120">ใช้ปุ่มลัด Siri เพื่อดูรายงานหรือแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="f7189-120">Use Siri Shortcuts to view report or dashboard</span></span>

<span data-ttu-id="f7189-121">ทันทีที่คุณสร้างปุ่มลัด ทุกครั้งที่คุณต้องการเข้าถึงแดชบอร์ดหรือรายงานที่คุณสร้างปุ่มลัดให้ แค่ถาม Siri</span><span class="sxs-lookup"><span data-stu-id="f7189-121">Once you create a shortcut, every time you’d like to access the dashboard or report that you created a shortcut for, just ask Siri.</span></span>
<span data-ttu-id="f7189-122">เปิดใช้งาน Siri และระบุวลีที่คุณบันทึกไว้สำหรับปุ่มลัด</span><span class="sxs-lookup"><span data-stu-id="f7189-122">Activate Siri and provide the phrase you recorded for the shortcut.</span></span> <span data-ttu-id="f7189-123">Siri จะเปิดใช้ Power BI และจะไปลงบนรายงานที่ร้องขอหรือแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="f7189-123">Siri will launch Power BI and land on the requested report or dashboard.</span></span> 

<span data-ttu-id="f7189-124">สำหรับรายงาน Power BI คุณจะไปลงยังหน้าที่จับภาพไว้เมื่อคุณสร้างปุ่มลัด</span><span class="sxs-lookup"><span data-stu-id="f7189-124">For a Power BI report, you will land on the page captured when you created the shortcut.</span></span>


  ![Siri เปิดใช้ Power BI เพื่อเปิดปุ่มลัด](./media/mobile-apps-ios-siri-search/power-bi-siri-open.png)
  

## <a name="edit-siri-shortcut-phrase"></a><span data-ttu-id="f7189-126">แก้ไขวลีปุ่มลัด Siri</span><span class="sxs-lookup"><span data-stu-id="f7189-126">Edit Siri shortcut phrase</span></span> 
<span data-ttu-id="f7189-127">คุณสามารถแก้ไขวลีปุ่มลัดของคุณได้โดยใช้ปุ่ม **ปุ่มลัด Siri** บน **รายงาน** หรือเมนูแอคชัน **แดชบอร์ด**(...) ได้ จะเปิดหน้าปุ่มลัด Siri พร้อมตัวเลือกเพื่อ **บันทึกวลีใหม่**</span><span class="sxs-lookup"><span data-stu-id="f7189-127">You can edit your shortcut phrase by using the **Siri shortcut** button on the **Report** or **Dashboard** actions menu (...). The Siri shortcut page will be opened with an option to **Re-Record phrase**.</span></span> 

## <a name="create-a-home-screen-shortcut-from-your-siri-shortcut"></a><span data-ttu-id="f7189-128">สร้างทางลัดหน้าจอหลักจากทางลัด Siri ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f7189-128">Create a home screen shortcut from your Siri shortcut</span></span> 
<span data-ttu-id="f7189-129">หลังจากที่คุณได้สร้างทางลัด Siri ไปยังเนื้อหา Power BI แล้ว คุณสามารถเพิ่มลงในหน้าจอหลักของอุปกรณ์ของคุณได้ ดังนั้นคุณสามารถเปิดเนื้อหานั้นได้โดยตรงจากหน้าจอหลักของด้วยการแตะเพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="f7189-129">Once you’ve created a Siri shortcut to some Power BI content, you can add it to your device’s home screen as well, so you can open that content directly from your home screen with a single tap.</span></span> <span data-ttu-id="f7189-130">ทำตามคำแนะนำเหล่านี้ที่ https://support.apple.com/guide/shortcuts/apd735880972/ios</span><span class="sxs-lookup"><span data-stu-id="f7189-130">Follow the instructions at https://support.apple.com/guide/shortcuts/apd735880972/ios.</span></span>

## <a name="delete-siri-shortcut"></a><span data-ttu-id="f7189-131">ลบปุ่มลัด Siri</span><span class="sxs-lookup"><span data-stu-id="f7189-131">Delete Siri shortcut</span></span> 
<span data-ttu-id="f7189-132">ในการลบปุ่มลัด ไปที่รายการ และออกจากเมนูแอคชัน (...) แตะที่แอคชัน **ปุ่มลัด Siri**</span><span class="sxs-lookup"><span data-stu-id="f7189-132">To delete a shortcut, go to the item, and from the actions menu (...), tap the **Siri shortcut** action.</span></span> <span data-ttu-id="f7189-133">หน้า **ปุ่มลัด Siri** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="f7189-133">The **Siri shortcut** page will open.</span></span> <span data-ttu-id="f7189-134">เลือก **ลบปุ่มลัด**</span><span class="sxs-lookup"><span data-stu-id="f7189-134">Choose **Delete Shortcut**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f7189-135">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="f7189-135">Next steps</span></span>
<span data-ttu-id="f7189-136">เรียนรู้เพิ่มเติมเกี่ยวกับแอป Power BI สำหรับอุปกรณ์เคลื่อนที่โดยดำเนินการดังนี้:</span><span class="sxs-lookup"><span data-stu-id="f7189-136">Learn more about the Power BI mobile app by doing the following:</span></span> 

* <span data-ttu-id="f7189-137">การดาวน์โหลด [แอป Power BI สำหรับ iPhone](https://go.microsoft.com/fwlink/?LinkId=522062)</span><span class="sxs-lookup"><span data-stu-id="f7189-137">Downloading the [Power BI iPhone mobile app](https://go.microsoft.com/fwlink/?LinkId=522062)</span></span>
* <span data-ttu-id="f7189-138">ติดตาม[@MSPowerBIบน Twitter](https://twitter.com/MSPowerBI)</span><span class="sxs-lookup"><span data-stu-id="f7189-138">Following [@MSPowerBI on Twitter](https://twitter.com/MSPowerBI)</span></span>
* <span data-ttu-id="f7189-139">การเข้าร่วมการสนทนาที่[ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="f7189-139">Joining the conversation at the [Power BI Community](https://community.powerbi.com/)</span></span>