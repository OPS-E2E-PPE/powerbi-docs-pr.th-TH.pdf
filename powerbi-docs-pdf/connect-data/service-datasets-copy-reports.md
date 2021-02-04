---
title: คัดลอกรายงานจากแอปหรือพื้นที่ทำงานอื่น - Power BI
description: เรียนรู้วิธีที่คุณสามารถสร้างสำเนาของรายงานและบันทึกไปยังพื้นที่ทำงานของคุณเอง
author: paulinbar
ms.author: painbar
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 10/30/2020
LocalizationGroup: Share your work
ms.openlocfilehash: 3b635719fdce8f8b194593a2114808e08f34420f
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96402903"
---
# <a name="copy-reports-from-other-workspaces"></a><span data-ttu-id="3b0dd-103">คัดลอกรายงานจากพื้นที่ทำงานอื่น</span><span class="sxs-lookup"><span data-stu-id="3b0dd-103">Copy reports from other workspaces</span></span>

<span data-ttu-id="3b0dd-104">เมื่อคุณพบรายงานที่คุณชอบในพื้นที่ทำงานหรือแอป คุณสามารถทำสำเนา และบันทึกไว้ในพื้นที่ทำงานอื่นได้</span><span class="sxs-lookup"><span data-stu-id="3b0dd-104">When you find a report you like in a workspace or an app, you can make a copy of it and save it to a different workspace.</span></span> <span data-ttu-id="3b0dd-105">จากนั้นคุณสามารถปรับเปลี่ยนสำเนารายงานของคุณโดยการเพิ่มหรือลบภาพวิชวลและองค์ประกอบอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="3b0dd-105">Then you can modify your copy of the report, adding or deleting visuals and other elements.</span></span> <span data-ttu-id="3b0dd-106">คุณไม่ต้องกังวลเกี่ยวกับการสร้างแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3b0dd-106">You don't have to worry about creating the data model.</span></span> <span data-ttu-id="3b0dd-107">แบบจำลองจะถูกสร้างไว้แล้วสำหรับคุณ</span><span class="sxs-lookup"><span data-stu-id="3b0dd-107">It's already created for you.</span></span> <span data-ttu-id="3b0dd-108">และการแก้ไขรายงานที่มีอยู่นั้นง่ายกว่าการเริ่มจากศูนย์</span><span class="sxs-lookup"><span data-stu-id="3b0dd-108">And it's much easier to modify an existing report than it is to start from scratch.</span></span> <span data-ttu-id="3b0dd-109">อย่างไรก็ตาม เมื่อคุณสร้างแอปขึ้นจากพื้นที่ทำงานของคุณ ในบางครั้งคุณไม่สามารถเผยแพร่สำเนาของรายงานในแอปได้</span><span class="sxs-lookup"><span data-stu-id="3b0dd-109">However, when you make an app from your workspace, sometimes you can't publish your copy of the report in the app.</span></span> <span data-ttu-id="3b0dd-110">โปรดดู [ข้อควรพิจารณาและข้อจำกัดในบทความ "ใช้ชุดข้อมูลในพื้นที่ทำงาน"](service-datasets-across-workspaces.md#considerations-and-limitations) สำหรับรายละเอียดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3b0dd-110">See [Considerations and limitations in the article "Use datasets across workspaces"](service-datasets-across-workspaces.md#considerations-and-limitations) for details.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3b0dd-111">สิ่งที่จำเป็นต้องมี</span><span class="sxs-lookup"><span data-stu-id="3b0dd-111">Prerequisites</span></span>

- <span data-ttu-id="3b0dd-112">หากต้องการคัดลอกรายงาน คุณต้องมีสิทธิ์การใช้งานระดับ Pro แม้ว่ารายงานต้นฉบับจะอยู่ในพื้นที่ทำงานในความจุพรีเมียมก็ตาม</span><span class="sxs-lookup"><span data-stu-id="3b0dd-112">To copy a report, you need a Pro license, even if the original report is in a workspace in a Premium capacity.</span></span>
- <span data-ttu-id="3b0dd-113">หากต้องการคัดลอกรายงาน และสร้างรายงานในพื้นที่ทำงานหนึ่งโดยยึดตามชุดข้อมูลในพื้นที่ทำงานอื่น คุณจำเป็นต้องมีสิทธิ์การสร้างสำหรับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3b0dd-113">To copy a report, or to create a report in one workspace based on a dataset in another workspace, you need Build permission for the dataset.</span></span> <span data-ttu-id="3b0dd-114">สำหรับชุดข้อมูลในพื้นที่ทำงานดั้งเดิม ผู้ใช้ที่มีบทบาทผู้ดูแลระบบ สมาชิก และผู้สนับสนุนมีสิทธิ์การสร้างผ่านบทบาทพื้นที่ทำงานของตนเองโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3b0dd-114">For datasets in the original workspace, the people with Admin, Member, and Contributor roles automatically have Build permission through their workspace role.</span></span> <span data-ttu-id="3b0dd-115">โปรดดู [บทบาทในพื้นที่ทำงานใหม่](../collaborate-share/service-new-workspaces.md#roles-in-the-new-workspaces) สำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="3b0dd-115">See [Roles in the new workspaces](../collaborate-share/service-new-workspaces.md#roles-in-the-new-workspaces) for details.</span></span>

## <a name="save-a-copy-of-a-report-in-a-workspace"></a><span data-ttu-id="3b0dd-116">บันทึกสำเนาของรายงานในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="3b0dd-116">Save a copy of a report in a workspace</span></span>

1. <span data-ttu-id="3b0dd-117">ในพื้นที่ทำงาน ไปยังมุมมองรายการรายงาน</span><span class="sxs-lookup"><span data-stu-id="3b0dd-117">In a workspace, go to the Reports list view.</span></span>

    ![มุมมองรายการรายงาน](media/service-datasets-copy-reports/power-bi-report-list-view.png)

1. <span data-ttu-id="3b0dd-119">ภายใต้ **การดำเนินการ** เลือก **บันทึกสำเนา**</span><span class="sxs-lookup"><span data-stu-id="3b0dd-119">Under **Actions**, select **Save a copy**.</span></span>

    ![บันทึกสำเนาของรายงาน](media/service-datasets-copy-reports/power-bi-dataset-save-report-copy.png)

    <span data-ttu-id="3b0dd-121">คุณจะเห็นเฉพาะไอคอน **บันทึกสำเนา** หากรายงานอยู่ในพื้นที่ทำงานประสบการณ์ใหม่ และคุณได้รับ [สิทธิ์ในการสร้าง](service-datasets-build-permissions.md)</span><span class="sxs-lookup"><span data-stu-id="3b0dd-121">You only see the **Save a copy** icon if the report is in a new experience workspace, and you have [Build permission](service-datasets-build-permissions.md).</span></span> <span data-ttu-id="3b0dd-122">แม้ว่าคุณสามารถเข้าถึงพื้นที่ทำงานได้ แต่คุณจะต้องมีสิทธิ์ในการสร้างสำหรับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3b0dd-122">Even if you have access to the workspace, you have to have Build permission for the dataset.</span></span>

3. <span data-ttu-id="3b0dd-123">ใน **บันทึกสำเนาของรายงานนี้** ให้ตั้งชื่อรายงานและเลือกพื้นที่ทำงานปลายทาง</span><span class="sxs-lookup"><span data-stu-id="3b0dd-123">In **Save a copy of this report**, give the report a name and select the destination workspace.</span></span>

    ![บันทึกกล่องโต้ตอบการทำสำเนา](media/service-datasets-copy-reports/power-bi-dataset-save-report.png)

    <span data-ttu-id="3b0dd-125">คุณสามารถบันทึกรายงานไว้ในพื้นที่ทำงานปัจจุบันหรือที่อื่นในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="3b0dd-125">You can save the report to the current workspace or a different one in the Power BI service.</span></span> <span data-ttu-id="3b0dd-126">คุณเห็นเฉพาะพื้นที่ทำงานที่เป็นพื้นที่ทำงานประสบการณ์ใหม่ ซึ่งคุณเป็นสมาชิกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3b0dd-126">You only see workspaces that are new experience workspaces, in which you're a member.</span></span> 
  
4. <span data-ttu-id="3b0dd-127">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3b0dd-127">Select **Save**.</span></span>

    <span data-ttu-id="3b0dd-128">Power BI จะสร้างสำเนาของรายงานและรายการต่างๆ ในรายการของชุดข้อมูลโดยอัตโนมัติ หากรายงานนั้นอ้างอิงจากชุดข้อมูลที่อยู่ภายนอกพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="3b0dd-128">Power BI automatically creates a copy of the report, and an entry in the list of datasets if the report is based on a dataset outside of the workspace.</span></span> <span data-ttu-id="3b0dd-129">ไอคอนสำหรับชุดข้อมูลนี้จะแตกต่างจากไอคอนสำหรับชุดข้อมูลในพื้นที่ทำงาน:</span><span class="sxs-lookup"><span data-stu-id="3b0dd-129">The icon for this dataset is different from the icon for datasets in the workspace:</span></span> ![ไอคอนชุดข้อมูลที่ใช้ร่วมกัน](media/service-datasets-discover-across-workspaces/power-bi-shared-dataset-icon.png)
    
    <span data-ttu-id="3b0dd-131">ด้วยวิธี สมาชิกของพื้นที่ทำงานสามารถบอกว่ารายงานและแดชบอร์ดใดใช้ชุดข้อมูลที่อยู่นอกพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="3b0dd-131">That way, members of the workspace can tell which reports and dashboards use datasets that are outside the workspace.</span></span> <span data-ttu-id="3b0dd-132">รายการจะแสดงข้อมูลเกี่ยวกับชุดข้อมูลและการดำเนินการเลือกสองสามอย่าง</span><span class="sxs-lookup"><span data-stu-id="3b0dd-132">The entry shows information about the dataset, and a few select actions.</span></span>

    ![การดำเนินการของชุดข้อมูล](media/service-datasets-across-workspaces/power-bi-dataset-actions.png)

    <span data-ttu-id="3b0dd-134">โปรดดู [สำเนาของรายงานของคุณ](#your-copy-of-the-report) ในบทความนี้สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายงานและชุดข้อมูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3b0dd-134">See [Your copy of the report](#your-copy-of-the-report) in this article for more about the report and related dataset.</span></span>

## <a name="copy-a-report-in-an-app"></a><span data-ttu-id="3b0dd-135">คัดลอกรายงานในแอป</span><span class="sxs-lookup"><span data-stu-id="3b0dd-135">Copy a report in an app</span></span>

1. <span data-ttu-id="3b0dd-136">ภายในแอป ให้คุณเปิดรายงานที่คุณต้องการคัดลอก</span><span class="sxs-lookup"><span data-stu-id="3b0dd-136">In an app, open the report you want to copy.</span></span>
2. <span data-ttu-id="3b0dd-137">ในแถบเมนู เลือก **ตัวเลือกเพิ่มเติม** ( **...** ) > **บันทึกสำเนา**</span><span class="sxs-lookup"><span data-stu-id="3b0dd-137">In the menu bar, select **More options** (**...**) > **Save a copy**.</span></span>

    ![บันทึกสำเนาของรายงาน](media/service-datasets-copy-reports/power-bi-save-copy.png)

    <span data-ttu-id="3b0dd-139">คุณจะเห็นตัวเลือก **บันทึกสำเนา** เท่านั้นถ้ารายงานอยู่ในพื้นที่ทำงานใหม่และคุณมี [สิทธิ์ในการสร้าง](service-datasets-build-permissions.md)</span><span class="sxs-lookup"><span data-stu-id="3b0dd-139">You only see the **Save a copy** option if the report is in a new experience workspace, and you have [Build permission](service-datasets-build-permissions.md).</span></span>

3. <span data-ttu-id="3b0dd-140">ตั้งชื่อให้รายงานของคุณ > **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3b0dd-140">Give your report a name > **Save**.</span></span>

    ![ตั้งชื่อสำเนาของรายงานของคุณ](media/service-datasets-copy-reports/power-bi-save-report-from-app.png)

    <span data-ttu-id="3b0dd-142">สำเนาของคุณจะถูกบันทึกไปยัง พื้นที่ทำงานของฉัน โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3b0dd-142">Your copy is automatically saved to your My Workspace.</span></span>

4. <span data-ttu-id="3b0dd-143">เลือก **ไปยังรายงาน** เพื่อเปิดสำเนาของคุณ</span><span class="sxs-lookup"><span data-stu-id="3b0dd-143">Select **Go to report** to open your copy.</span></span>

## <a name="your-copy-of-the-report"></a><span data-ttu-id="3b0dd-144">สำเนาของรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="3b0dd-144">Your copy of the report</span></span>

<span data-ttu-id="3b0dd-145">เมื่อคุณบันทึกสำเนาของรายงาน คุณจะสร้างการเชื่อมต่อสดกับชุดข้อมูล และสามารถเปิดประสบการณ์ในการสร้างรายงานพร้อมกับชุดข้อมูลทั้งหมดที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3b0dd-145">When you save a copy of the report, you create a live connection to the dataset, and you can open the report creation experience with the full dataset available.</span></span> 

![แก้ไขสำเนาของรายงานของคุณ](media/service-datasets-copy-reports/power-bi-edit-report-copy.png)

<span data-ttu-id="3b0dd-147">คุณยังไม่ได้ทำสำเนาของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3b0dd-147">You haven't made a copy of the dataset.</span></span> <span data-ttu-id="3b0dd-148">ชุดข้อมูลยังคงอยู่ในตำแหน่งเดิม</span><span class="sxs-lookup"><span data-stu-id="3b0dd-148">The dataset still resides in its original location.</span></span> <span data-ttu-id="3b0dd-149">คุณสามารถใช้ตารางและหน่วยวัดทั้งหมดในชุดข้อมูลในรายงานของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="3b0dd-149">You can use all tables and measures in the dataset in your own report.</span></span> <span data-ttu-id="3b0dd-150">ข้อจำกัดด้านความปลอดภัยระดับแถว (RLS) บนชุดข้อมูลจะมีผล เพื่อให้คุณเท่านั้นดูข้อมูลที่คุณมีสิทธิในการดูตามบทบาท RLS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3b0dd-150">Row-level security (RLS) restrictions on the dataset are in effect, so you only see data you have permissions to see based on your RLS role.</span></span>

## <a name="view-related-datasets"></a><span data-ttu-id="3b0dd-151">ดูชุดข้อมูลที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3b0dd-151">View related datasets</span></span>

<span data-ttu-id="3b0dd-152">เมื่อคุณมีรายงานในพื้นที่ทำงานหนึ่งที่อ้างอิงจากชุดข้อมูลในพื้นที่ทำงานอื่น คุณอาจจำเป็นต้องทราบข้อมูลเพิ่มเติมเกี่ยวกับชุดข้อมูลอ้างอิงมานั้น</span><span class="sxs-lookup"><span data-stu-id="3b0dd-152">When you have a report in one workspace based on a dataset in another workspace, you may need to know more about the dataset it's based on.</span></span>

1. <span data-ttu-id="3b0dd-153">ในมุมมองรายการรายงาน เลือก **มุมมองที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="3b0dd-153">In the Reports list view, select **View related**.</span></span>

    ![แอคชันแสดงไอคอนที่เกี่ยวข้องกับมุมมองภายใต้การดำเนินการ](media/service-datasets-copy-reports/power-bi-dataset-view-related.png)

1. <span data-ttu-id="3b0dd-155">กล่องโต้ตอบ **เนื้อหาที่เกี่ยวข้อง** จะแสดงรายการที่เกี่ยวข้องทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3b0dd-155">The **Related content** dialog box shows all related items.</span></span> <span data-ttu-id="3b0dd-156">ในรายการนี้ ชุดข้อมูลมีลักษณะเป็นอย่างอื่น</span><span class="sxs-lookup"><span data-stu-id="3b0dd-156">In this list, the dataset looks like any other.</span></span> <span data-ttu-id="3b0dd-157">คุณไม่สามารถบอกได้ว่าชุดข้อมูลนั้นอยู่ในพื้นที่ทำงานอื่น</span><span class="sxs-lookup"><span data-stu-id="3b0dd-157">You can't tell it resides in a different workspace.</span></span> <span data-ttu-id="3b0dd-158">ปัญหานี้เป็นที่รู้จัก</span><span class="sxs-lookup"><span data-stu-id="3b0dd-158">This issue is known.</span></span>
 
    ![กล่องโต้ตอบเนื้อหาที่เกี่ยวข้อง](media/service-datasets-copy-reports/power-bi-dataset-related.png)

## <a name="delete-a-report-and-its-shared-dataset"></a><span data-ttu-id="3b0dd-160">ลบรายงานและชุดข้อมูลที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="3b0dd-160">Delete a report and its shared dataset</span></span>

<span data-ttu-id="3b0dd-161">คุณอาจตัดสินใจว่าคุณไม่ต้องการรายงานและชุดข้อมูลเชื่อมโยงที่ใช้ร่วมกันในพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="3b0dd-161">You may decide you no longer want the report and its associated shared dataset in workspace.</span></span>

1. <span data-ttu-id="3b0dd-162">ลบรายงาน</span><span class="sxs-lookup"><span data-stu-id="3b0dd-162">Delete the report.</span></span> <span data-ttu-id="3b0dd-163">ในรายการของรายงานในพื้นที่ทำงาน เลือกไอคอน **ลบ**</span><span class="sxs-lookup"><span data-stu-id="3b0dd-163">In the list of reports in the workspace, select the **Delete** icon.</span></span>

    ![ไอคอนลบรายงาน](media/service-datasets-across-workspaces/power-bi-datasets-delete-report.png)

2. <span data-ttu-id="3b0dd-165">ในรายการของชุดข้อมูล คุณจะเห็นว่าชุดข้อมูลที่ใช้ร่วมกันไม่มีไอคอน **ลบ**</span><span class="sxs-lookup"><span data-stu-id="3b0dd-165">In the list of datasets, you see the shared datasets don't have **Delete** icons.</span></span> <span data-ttu-id="3b0dd-166">รีเฟรชหน้า หรือไปยังหน้าอื่น และย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="3b0dd-166">Refresh the page, or go to a different page and return.</span></span> <span data-ttu-id="3b0dd-167">ชุดข้อมูลจะหายไป</span><span class="sxs-lookup"><span data-stu-id="3b0dd-167">The dataset will be gone.</span></span> <span data-ttu-id="3b0dd-168">หากไม่ ให้ตรวจสอบ **มุมมองที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="3b0dd-168">If not, check **View related**.</span></span> <span data-ttu-id="3b0dd-169">ซึ่งอาจเกี่ยวข้องกับตารางอื่นในพื้นที่ทำงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="3b0dd-169">It may be related to another table in your workspace.</span></span>

    ![สกรีนช็อตแสดงชุดข้อมูลที่มีตัวเลือกที่เกี่ยวข้องกับมุมมองที่เกี่ยวข้องเพื่อตรวจสอบตารางที่เกี่ยวข้อง](media/service-datasets-across-workspaces/power-bi-dataset-view-related-icon.png)

    > [!NOTE]
    > <span data-ttu-id="3b0dd-171">การลบข้อมูลที่ใช้ร่วมกันในพื้นที่ทำงานจะไม่ลบชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3b0dd-171">Deleting the shared dataset in this workspace doesn't delete the dataset.</span></span> <span data-ttu-id="3b0dd-172">โดยจะลบเฉพาะการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="3b0dd-172">It just deletes the reference to it.</span></span>


## <a name="next-steps"></a><span data-ttu-id="3b0dd-173">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3b0dd-173">Next steps</span></span>

- [<span data-ttu-id="3b0dd-174">ใช้ชุดข้อมูลทั่วทั้งพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="3b0dd-174">Use datasets across workspaces</span></span>](service-datasets-across-workspaces.md)
- <span data-ttu-id="3b0dd-175">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3b0dd-175">Questions?</span></span> [<span data-ttu-id="3b0dd-176">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="3b0dd-176">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
