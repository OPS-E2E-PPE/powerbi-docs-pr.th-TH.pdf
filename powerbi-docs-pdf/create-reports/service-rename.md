---
title: เปลี่ยนชื่อแดชบอร์ด รายงาน พื้นที่ทำงาน หน้ารายงาน ชุดข้อมูล
description: เปลี่ยนชื่อเกือบทุกสิ่งใน Power BI service
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 03/01/2018
LocalizationGroup: Common tasks
ms.openlocfilehash: fc120b832fda05d822e57ace56b15fbd773a53ad
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96388045"
---
# <a name="rename-almost-anything-in-power-bi-service"></a><span data-ttu-id="8de7a-103">เปลี่ยนชื่อเกือบทุกสิ่งใน Power BI service</span><span class="sxs-lookup"><span data-stu-id="8de7a-103">Rename almost anything in Power BI service</span></span>
<span data-ttu-id="8de7a-104">บทความนี้สอนวิธีการเปลี่ยนชื่อแดชบอร์ด รายงาน หน้ารายงาน เวิร์กบุ๊ก ชุดข้อมูล แอปฯ และพื้นที่ทำงานในบริการ Power BI service</span><span class="sxs-lookup"><span data-stu-id="8de7a-104">This article teaches you how to rename a dashboard, report, report page, workbook, dataset, app, and workspace in Power BI service.</span></span>

<span data-ttu-id="8de7a-105">**ฉันสามารถเปลี่ยนชื่อได้อย่างไร**</span><span class="sxs-lookup"><span data-stu-id="8de7a-105">**Can I change the name?**</span></span>

| <span data-ttu-id="8de7a-106">ชนิดเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="8de7a-106">Content type</span></span> | <span data-ttu-id="8de7a-107">ฉันเป็นผู้เขียนหรือผู้สร้าง</span><span class="sxs-lookup"><span data-stu-id="8de7a-107">I'm the author or creator</span></span> | <span data-ttu-id="8de7a-108">แชร์กับฉันแล้ว</span><span class="sxs-lookup"><span data-stu-id="8de7a-108">Shared with me</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8de7a-109">แดชบอร์ดในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="8de7a-109">Dashboard in a workspace</span></span> |<span data-ttu-id="8de7a-110">ใช่</span><span class="sxs-lookup"><span data-stu-id="8de7a-110">Yes</span></span> |<span data-ttu-id="8de7a-111">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8de7a-111">No</span></span> |
| <span data-ttu-id="8de7a-112">รายงานในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="8de7a-112">Report in a workspace</span></span> |<span data-ttu-id="8de7a-113">ใช่</span><span class="sxs-lookup"><span data-stu-id="8de7a-113">Yes</span></span> |<span data-ttu-id="8de7a-114">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8de7a-114">No</span></span> |
| <span data-ttu-id="8de7a-115">สมุดงานในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="8de7a-115">Workbook in a workspace</span></span> |<span data-ttu-id="8de7a-116">ใช่</span><span class="sxs-lookup"><span data-stu-id="8de7a-116">Yes</span></span> |<span data-ttu-id="8de7a-117">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8de7a-117">No</span></span> |
| <span data-ttu-id="8de7a-118">ชุดข้อมูลในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="8de7a-118">Dataset in a workspace</span></span> |<span data-ttu-id="8de7a-119">ใช่</span><span class="sxs-lookup"><span data-stu-id="8de7a-119">Yes</span></span> |<span data-ttu-id="8de7a-120">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8de7a-120">No</span></span> |
| <span data-ttu-id="8de7a-121">พื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="8de7a-121">workspace</span></span> |<span data-ttu-id="8de7a-122">ใช่ ถ้าคุณเป็นเจ้าของ หรือมีสิทธิ์ระดับผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="8de7a-122">Yes, if you are the owner or have Admin permissions</span></span> |<span data-ttu-id="8de7a-123">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8de7a-123">No</span></span> |
| <span data-ttu-id="8de7a-124">แอปที่เผยแพร่แล้ว</span><span class="sxs-lookup"><span data-stu-id="8de7a-124">Published apps</span></span> |<span data-ttu-id="8de7a-125">ไม่ใช่จากหน้าจอแอป แต่ชื่อแอปสามารถเปลี่ยนจากพื้นที่ทำงาน และเผยแพร่ใหม่ด้วยชื่อใหม่ถ้าคุณมีสิทธิ์ระดับผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="8de7a-125">Not from the App screen, but the app name can be changed from the workspace and re-published with a new name if you have Admin permissions</span></span> |<span data-ttu-id="8de7a-126">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8de7a-126">No</span></span> |
| <span data-ttu-id="8de7a-127">เนื้อหาของแอป (แดชบอร์ด รายงาน เวิร์กบุ๊ก ชุดข้อมูล)</span><span class="sxs-lookup"><span data-stu-id="8de7a-127">App content (dashboard, report, workbook, dataset)</span></span> |<span data-ttu-id="8de7a-128">ไม่ใช่จากหน้าจอแอป แต่เนื้อหาของแอปสามารถเปลี่ยนชื่อได้จากพื้นที่ทำงาน และเผยแพร่ใหม่ด้วยชื่อใหม่ถ้าคุณมีสิทธิ์ระดับผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="8de7a-128">Not from the App screen, but the app's content can be renamed from the workspace and re-published with a new name if you have Admin permissions</span></span> |<span data-ttu-id="8de7a-129">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8de7a-129">No</span></span> |
| <span data-ttu-id="8de7a-130">เนื้อหาใน **แชร์กับฉัน**</span><span class="sxs-lookup"><span data-stu-id="8de7a-130">Content in **Shared with me**</span></span> |<span data-ttu-id="8de7a-131">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8de7a-131">No</span></span> |<span data-ttu-id="8de7a-132">ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="8de7a-132">No</span></span> |

## <a name="rename-a-dashboard-report-or-workbook"></a><span data-ttu-id="8de7a-133">เปลี่ยนชื่อแดชบอร์ด รายงาน หรือเวิร์กบุ๊ก</span><span class="sxs-lookup"><span data-stu-id="8de7a-133">Rename a dashboard, report, or workbook</span></span>
1. <span data-ttu-id="8de7a-134">เริ่มต้นในพื้นที่ทำงานและเลือก **แดชบอร์ด** **รายงาน** หรือแท็บ **สมุดงาน** เลื่อนเมาส์หนือรายการที่จะเปลี่ยนชื่อ แล้วเลือกไอคอนรูปเฟือง![ไอคอนรูปเฟือง](media/service-rename/powerbi-cog-icon.png)</span><span class="sxs-lookup"><span data-stu-id="8de7a-134">Start in a workspace and select the **Dashboards**, **Reports**, or **Workbooks** tab. Hover over the item to rename, and select the gear icon ![gear icon](media/service-rename/powerbi-cog-icon.png).</span></span> <span data-ttu-id="8de7a-135">ถ้าไม่มีไม่มีไอคอนรูปเฟือง คุณไม่มีสิทธิ์ในการเปลี่ยนชื่อ</span><span class="sxs-lookup"><span data-stu-id="8de7a-135">If there is no gear icon, you do not have permissions to rename.</span></span>
   
   ![พื้นที่ทำงานของ Power BI service](media/service-rename/power-bi-workspace-dashboards.png)
2. <span data-ttu-id="8de7a-137">บนหน้าการตั้งค่า พิมพ์ชื่อใหม่ แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8de7a-137">On the Settings page, type the new name and select **Save**.</span></span>
   
   ![หน้าต่างการตั้งค่าสำหรับชุดข้อมูล](media/service-rename/power-bi-rename-dashboard2.png)

## <a name="rename-a-dataset"></a><span data-ttu-id="8de7a-139">เปลี่ยนชื่อชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8de7a-139">Rename a dataset</span></span>
1. <span data-ttu-id="8de7a-140">เริ่มต้นในพื้นที่ทำงานและเลือกแท็บ **ชุดข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="8de7a-140">Start in a workspace and select the **Datasets** tab.</span></span>
   
   ![พื้นที่ทำงาน แท็บชุดข้อมูล](media/service-rename/power-bi-ellipses.png)
2. <span data-ttu-id="8de7a-142">วางเมาส์เหนือรายการที่จะเปลี่ยนชื่อ เลือก **ตัวเลือกเพิ่มเติม** (...) และเลือก **เปลี่ยนชื่อ**</span><span class="sxs-lookup"><span data-stu-id="8de7a-142">Hover over the item to rename, select **More options** (...), and choose **Rename**.</span></span>  
   
      ![เลือก เปลี่ยนชื่อ](media/service-rename/power-bi-rename-datasets.png)
   
   > [!NOTE]
   > <span data-ttu-id="8de7a-144">ตัวเลือกในดรอปดาวน์ลงจะแตกต่างออกไป</span><span class="sxs-lookup"><span data-stu-id="8de7a-144">The options in the dropdown will vary.</span></span>
   > 
   > 
3. <span data-ttu-id="8de7a-145">บนหน้าการตั้งค่า พิมพ์ชื่อใหม่ แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8de7a-145">On the Settings page, type a new name and select **Save**.</span></span>
   
     ![ช่องเปลี่ยนชื่อ](media/service-rename/power-bi-rename.png)

## <a name="rename-a-workspace"></a><span data-ttu-id="8de7a-147">เปลี่ยนชื่อพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="8de7a-147">Rename a workspace</span></span>
<span data-ttu-id="8de7a-148">ทุกคนที่มีสิทธิ์ระดับผู้ดูแลระบบสามารถเปลี่ยนชื่อพื้นที่ทำงานได้</span><span class="sxs-lookup"><span data-stu-id="8de7a-148">Anyone with Admin permissions can rename a workspace.</span></span>

1. <span data-ttu-id="8de7a-149">เริ่มในพื้นที่ทำงานแอปฯที่คุณต้องการเปลี่ยนชื่อ</span><span class="sxs-lookup"><span data-stu-id="8de7a-149">Start in the workspace you'd like to rename.</span></span>
2. <span data-ttu-id="8de7a-150">ที่มุมบนขวา เลือก **ตัวเลือกเพิ่มเติม** (...) แล้วเลือก **แก้ไขพื้นที่ทำงาน**</span><span class="sxs-lookup"><span data-stu-id="8de7a-150">In the top-right corner, select **More options** (...) and choose **Edit workspace**.</span></span> <span data-ttu-id="8de7a-151">ถ้าคุณไม่เห็นตัวเลือกนี้ คุณไม่มีสิทธิ์ในการเปลี่ยนชื่อพื้นที่ทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="8de7a-151">If you don't see this option, then you don't have permissions to rename this workspace.</span></span> 
   
    ![เลือก แก้ไขพื้นที่ทำงาน](media/service-rename/power-bi-edit-workspace.png)
3. <span data-ttu-id="8de7a-153">พิมพ์ชื่อพื้นที่ทำงานใหม่ และเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8de7a-153">Type a new workspace name and select **Save**.</span></span>
   
   ![แก้ไขช่องพื้นที่ทำงาน](media/service-rename/power-bi-workspace-rename.png)

## <a name="rename-a-page-in-a-report"></a><span data-ttu-id="8de7a-155">เปลี่ยนชื่อหน้าในรายงาน</span><span class="sxs-lookup"><span data-stu-id="8de7a-155">Rename a page in a report</span></span>
<span data-ttu-id="8de7a-156">ไม่ชอบชื่อของหน้าในรายงาน Power BI ของคุณใช่ไหม</span><span class="sxs-lookup"><span data-stu-id="8de7a-156">Don't like the name of a page in your Power BI report?</span></span>  <span data-ttu-id="8de7a-157">เปลี่ยนชื่อใหม่ เพียงคลิกเดียว</span><span class="sxs-lookup"><span data-stu-id="8de7a-157">A new name is just a click away.</span></span> <span data-ttu-id="8de7a-158">สามารถเปลี่ยนชื่อใน[มุมมองการแก้ไขรายงาน](service-interact-with-a-report-in-editing-view.md)ได้</span><span class="sxs-lookup"><span data-stu-id="8de7a-158">Pages can be renamed in [report Editing view ](service-interact-with-a-report-in-editing-view.md).</span></span>

1. <span data-ttu-id="8de7a-159">เปิดรายงานใน[มุมมองการแก้ไข](../consumer/end-user-reading-view.md)</span><span class="sxs-lookup"><span data-stu-id="8de7a-159">Open the report in [Editing View](../consumer/end-user-reading-view.md).</span></span>
2. <span data-ttu-id="8de7a-160">ค้นหาแท็บหน้ารายงานที่ด้านล่างของหน้าต่าง Power BI</span><span class="sxs-lookup"><span data-stu-id="8de7a-160">Locate the report page tabs at the bottom of the Power BI window.</span></span>
   
    ![รายงานทีมีแท็บที่ไฮไลต์ไว้](media/service-rename/report-page-tabs-new.png)
3. <span data-ttu-id="8de7a-162">เปิดหน้ารายงานที่คุณต้องการเปลี่ยนชื่อ โดยเลือกแท็บ</span><span class="sxs-lookup"><span data-stu-id="8de7a-162">Open the report page that you'd like to rename by selecting the tab.</span></span>
4. <span data-ttu-id="8de7a-163">ดับเบิลคลิกชื่อบนแท็บเพื่อไฮไลต์</span><span class="sxs-lookup"><span data-stu-id="8de7a-163">Double-click the name on the tab to highlight it.</span></span>  
   
    ![เข้าไปใกล้แท็บชื่อ](media/service-rename/hilite-tab.png)
5. <span data-ttu-id="8de7a-165">พิมพ์ชื่อหน้ารายงานใหม่ แล้วเลือก ENTER</span><span class="sxs-lookup"><span data-stu-id="8de7a-165">Type a new report page name and select ENTER.</span></span>
   
    ![พิมพ์ชื่อหน้าใหม่](media/service-rename/new-name.png)

## <a name="considerations-and-troubleshooting"></a><span data-ttu-id="8de7a-167">ข้อควรพิจารณาและการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="8de7a-167">Considerations and troubleshooting</span></span>
* <span data-ttu-id="8de7a-168">ถ้ารายการที่ถูกเปลี่ยนชื่อได้แชร์กับคุณ หรือเป็นส่วนหนึ่งของชุดเนื้อหา คุณจะไม่เห็นไอคอนรูปเฟือง และคุณจะไม่สามารถเข้าถึงการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="8de7a-168">If the item to be renamed has been shared with you, or is part of a content pack, you won't see the gear icon and you won't have access to Settings.</span></span>
* <span data-ttu-id="8de7a-169">บนแท็บ **ชุดข้อมูล** ถ้าคุณไม่เห็น **ตัวเลือกเพิ่มเติม** (...) ให้ขยายหน้าต่างเบราว์เซอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8de7a-169">On the **Datasets** tab, if you don't see **More options** (...), expand your browser window.</span></span>

<span data-ttu-id="8de7a-170">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8de7a-170">More questions?</span></span> [<span data-ttu-id="8de7a-171">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="8de7a-171">Try the Power BI Community</span></span>](https://community.powerbi.com/)
