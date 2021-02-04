---
title: สร้างสิทธิการอนุญาตสำหรับชุดข้อมูลที่ใช้ร่วมกัน
description: เรียนรู้วิธีที่คุณสามารถควบคุมการเข้าถึงข้อมูลโดยใช้สิทธิ์ในการสร้าง
author: paulinbar
ms.author: painbar
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 10/21/2020
LocalizationGroup: Share your work
ms.openlocfilehash: 914477d8b4bed0b6f90f700afcbfdfbfc263bb1d
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410470"
---
# <a name="build-permission-for-shared-datasets"></a><span data-ttu-id="bfed3-103">สร้างสิทธิการอนุญาตสำหรับชุดข้อมูลที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="bfed3-103">Build permission for shared datasets</span></span>

<span data-ttu-id="bfed3-104">เมื่อคุณสร้างรายงานใน Power BI Desktop ข้อมูลในรายงานนั้นจะถูกจัดเก็บไว้ใน *แบบจำลองข้อมูล*</span><span class="sxs-lookup"><span data-stu-id="bfed3-104">When you create a report in Power BI Desktop, the data in that report is stored in a *data model*.</span></span> <span data-ttu-id="bfed3-105">เมื่อคุณเผยแพร่รายงานของคุณไปยังบริการ Power BI คุณยังได้เผยแพร่ข้อมูลเป็น *ชุดข้อมูล* ด้วย</span><span class="sxs-lookup"><span data-stu-id="bfed3-105">When you publish your reports to the Power BI service, you're also publishing the data as a *dataset*.</span></span> <span data-ttu-id="bfed3-106">คุณสามารถกำหนด *สิทธิ์ในการสร้าง* สำหรับรายงานดังกล่าวให้แก่ผู้อื่น เพื่อให้พวกเขาสามารถค้นหาและนำชุดข้อมูลที่คุณแชร์มาใช้ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="bfed3-106">You can give others *Build permission* for that report, so they can discover and reuse the dataset you've shared.</span></span> <span data-ttu-id="bfed3-107">บทความนี้อธิบายวิธีควบคุมการเข้าถึงข้อมูลโดยใช้สิทธิ์ในการสร้าง</span><span class="sxs-lookup"><span data-stu-id="bfed3-107">This article explains how you control access to the data by using the Build permission.</span></span>

<span data-ttu-id="bfed3-108">สิทธิ์ในการสร้างนำไปใช้กับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bfed3-108">Build permission applies to datasets.</span></span> <span data-ttu-id="bfed3-109">เมื่อคุณให้สิทธิ์ในการสร้างแก่ผู้ใช้ ผู้ใช้สามารถสร้างเนื้อหาใหม่ในชุดข้อมูลของคุณ เช่น รายงาน แดชบอร์ด ไทล์ที่ปักหมุดไว้จากฟังก์ชันถามตอบ และการค้นพบข้อมูลเชิงลึกได้</span><span class="sxs-lookup"><span data-stu-id="bfed3-109">When you give users Build permission, they can build new content on your dataset, such as reports, dashboards, pinned tiles from Q&A, and Insights Discovery.</span></span> 

<span data-ttu-id="bfed3-110">นอกจากนี้ผู้ใช้จำเป็นต้องมีสิทธิ์ในการสร้างเพื่อทำงานกับข้อมูล *ภายนอก* Power BI:</span><span class="sxs-lookup"><span data-stu-id="bfed3-110">Users also need Build permissions to work with the data *outside* Power BI:</span></span>

- <span data-ttu-id="bfed3-111">เมื่อต้องส่งออกข้อมูลเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="bfed3-111">To export the underlying data.</span></span>
- <span data-ttu-id="bfed3-112">เมื่อต้องสร้างเนื้อหาใหม่บนชุดข้อมูล เช่น สร้างด้วย [Analyze ใน Excel](../collaborate-share/service-analyze-in-excel.md)</span><span class="sxs-lookup"><span data-stu-id="bfed3-112">To build new content on the dataset such as with [Analyze in Excel](../collaborate-share/service-analyze-in-excel.md).</span></span>
- <span data-ttu-id="bfed3-113">เมื่อต้องเข้าถึงข้อมูลผ่านจุดสิ้นสุดของ XMLA</span><span class="sxs-lookup"><span data-stu-id="bfed3-113">To access the data via the XMLA endpoint.</span></span>

## <a name="ways-to-give-build-permission"></a><span data-ttu-id="bfed3-114">วิธีการให้สิทธิ์ในการสร้าง</span><span class="sxs-lookup"><span data-stu-id="bfed3-114">Ways to give Build permission</span></span>

<span data-ttu-id="bfed3-115">คุณให้สิทธิ์ในการสร้างสำหรับชุดข้อมูลหนึ่ง ๆ ได้ด้วยสองสามวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bfed3-115">You give Build permission for a dataset in a few different ways:</span></span>

- <span data-ttu-id="bfed3-116">สมาชิกของพื้นที่ทำงานที่มีบทบาทผู้สนับสนุนอย่างน้อยหนึ่งบทบาทจะมีสิทธิ์ในการสร้างสำหรับชุดข้อมูลในพื้นที่ทำงานดังกล่าว และสิทธิ์ในการคัดลอกรายงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="bfed3-116">Members of a workspace with at least a Contributor role automatically have Build permission for datasets in that workspace, and permission to copy a report.</span></span> <span data-ttu-id="bfed3-117">อ่านเพิ่มเติมเกี่ยวกับ[บทบาทในพื้นที่ทำงานใหม่](../collaborate-share/service-new-workspaces.md#roles-in-the-new-workspaces)</span><span class="sxs-lookup"><span data-stu-id="bfed3-117">Read more about [roles in the new workspaces](../collaborate-share/service-new-workspaces.md#roles-in-the-new-workspaces).</span></span>
 
- <span data-ttu-id="bfed3-118">สมาชิกของพื้นที่ทำงานที่มีชุดข้อมูลสามารถกำหนดสิทธิ์ให้ผู้ใช้หรือกลุ่มความปลอดภัยที่เฉพาะเจาะจงในศูนย์การอนุญาต</span><span class="sxs-lookup"><span data-stu-id="bfed3-118">Members of the workspace where the dataset resides can assign the permission to specific users or security groups in the Permission center.</span></span> <span data-ttu-id="bfed3-119">หากคุณเป็นสมาชิกของพื้นที่ทำงาน เลือก **ตัวเลือกเพิ่มเติม** (...) ที่อยู่ถัดจากชุดข้อมูล > **จัดการสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="bfed3-119">If you're a member of the workspace, select **More options** (...) next to a dataset > **Manage Permissions**.</span></span>

    ![เลือกจุดไข่ปลา](media/service-datasets-build-permissions/power-bi-dataset-permissions-new-look.png)

    <span data-ttu-id="bfed3-121">ซึ่งจะเปิดศูนย์การอนุญาตสำหรับชุดข้อมูลนั้นที่คุณสามารถตั้งค่าและเปลี่ยนแปลงสิทธิ</span><span class="sxs-lookup"><span data-stu-id="bfed3-121">That opens the Permission center for that dataset, where you can set and change permissions.</span></span>

    ![ศูนย์การอนุญาต](media/service-datasets-build-permissions/power-bi-dataset-remove-permissions-no-callouts.png)

- <span data-ttu-id="bfed3-123">ผู้ดูแลระบบหรือสมาชิกของพื้นที่ทำงานที่มีชุดข้อมูลสามารถตัดสินใจในระหว่างการเผยแพร่แอปว่าผู้ใช้ที่มีสิทธิสำหรับแอปจะได้รับสิทธิในการสร้างสำหรับชุดข้อมูลเบื้องต้นด้วย</span><span class="sxs-lookup"><span data-stu-id="bfed3-123">An admin or member of the workspace where the dataset resides can decide during app publishing that users with permission for the app also get Build permission for the underlying datasets.</span></span> <span data-ttu-id="bfed3-124">ดูรายละเอียดได้ใน[แชร์ชุดข้อมูล](service-datasets-share.md)</span><span class="sxs-lookup"><span data-stu-id="bfed3-124">See [Share a dataset](service-datasets-share.md) for details.</span></span>

- <span data-ttu-id="bfed3-125">สมมติว่าคุณมีการแชร์ต่อและสิทธิ์ในการสร้างในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bfed3-125">Say you have Reshare and Build permission on a dataset.</span></span> <span data-ttu-id="bfed3-126">เมื่อคุณแชร์รายงานหรือแดชบอร์ดที่สร้างขึ้นในชุดข้อมูลนั้น คุณสามารถระบุว่าผู้รับจะได้รับสิทธิ์ในการสร้างสำหรับชุดข้อมูลเบื้องต้นด้วย</span><span class="sxs-lookup"><span data-stu-id="bfed3-126">When you share a report or dashboard built on that dataset, you can specify that the recipients also get Build permission for the underlying dataset.</span></span>

    ![สิทธิ์ในการสร้าง](media/service-datasets-build-permissions/power-bi-share-report-allow-users.png)

<span data-ttu-id="bfed3-128">คุณสามารถลบสิทธิ์ในการสร้างของบุคคลสำหรับชุดข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="bfed3-128">You can remove a person's Build permission for a dataset.</span></span> <span data-ttu-id="bfed3-129">ถ้าคุณทำเช่นนั้น พวกเขายังคงสามารถดูรายงานที่สร้างบนชุดข้อมูลที่ใช้ร่วมกัน แต่จะสามารถไม่แก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="bfed3-129">If you do, they can still see the report built on the shared dataset, but they can no longer edit it.</span></span> <span data-ttu-id="bfed3-130">ดูรายละเอียดได้ในส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="bfed3-130">See the next section for details.</span></span>

## <a name="remove-build-permission-for-a-dataset"></a><span data-ttu-id="bfed3-131">ลบสิทธิ์ในการสร้างสำหรับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="bfed3-131">Remove Build permission for a dataset</span></span>

<span data-ttu-id="bfed3-132">ในบางกรณี คุณอาจจำเป็นต้องลบสิทธิ์ในการสร้างสำหรับบางผู้ใช้ของชุดข้อมูลที่แชร์</span><span class="sxs-lookup"><span data-stu-id="bfed3-132">At some point, you may need to remove Build permission for some users of a shared dataset.</span></span> 

1. <span data-ttu-id="bfed3-133">ในพื้นที่ทำงาน ให้ไปที่หน้ารายการ **ชุดข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="bfed3-133">In a workspace, go to the **Datasets** list page.</span></span> 
1. <span data-ttu-id="bfed3-134">เลือก **ตัวเลือกเพิ่มเติม** (...) ที่อยู่ถัดจากชุดข้อมูล > **จัดการสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="bfed3-134">Select **More options** (...) next to the dataset > **Manage permission**.</span></span>

    ![จัดการการอนุญาต](media/service-datasets-build-permissions/power-bi-dataset-permissions-new-look.png)

1. <span data-ttu-id="bfed3-136">เลือก **ตัวเลือกเพิ่มเติม** (...) ที่อยู่ถัดจากชื่อ > **ลบการสร้าง**</span><span class="sxs-lookup"><span data-stu-id="bfed3-136">Select **More options** (...) next to a name > **Remove build**.</span></span>

    ![ลบสิทธิ์ในการสร้าง](media/service-datasets-build-permissions/power-bi-dataset-remove-build-permissions.png)

    <span data-ttu-id="bfed3-138">ผู้ใช้ยังคงสามารถดูรายงานที่สร้างไว้ในชุดข้อมูลที่แชร์ แต่จะไม่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="bfed3-138">They can still see the report built on the shared dataset, but they can no longer edit it.</span></span>

### <a name="remove-build-permission-for-a-dataset-in-an-app"></a><span data-ttu-id="bfed3-139">ลบสิทธิ์ในการสร้างสำหรับชุดข้อมูลในแอป</span><span class="sxs-lookup"><span data-stu-id="bfed3-139">Remove Build permission for a dataset in an app</span></span>

<span data-ttu-id="bfed3-140">สมมติว่าคุณแจกจ่ายแอปจากพื้นที่ทำงานไปยังกลุ่มบุคคล</span><span class="sxs-lookup"><span data-stu-id="bfed3-140">Say you've distributed an app from a workspace to a group of people.</span></span> <span data-ttu-id="bfed3-141">หลังจากนั้น คุณตัดสินใจที่จะลบการเข้าถึงแอปสำหรับบุคคลบางคน</span><span class="sxs-lookup"><span data-stu-id="bfed3-141">Later, you decide to remove access to the app for some people.</span></span> <span data-ttu-id="bfed3-142">การลบการเข้าถึงแอปของบุคคลจะไม่ลบสิทธิ์ในการสร้างและแชร์โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="bfed3-142">Removing their access to the app doesn't automatically remove their build and reshare permissions.</span></span> <span data-ttu-id="bfed3-143">นี่เป็นขั้นตอนพิเศษ</span><span class="sxs-lookup"><span data-stu-id="bfed3-143">That's an extra step.</span></span> 

1. <span data-ttu-id="bfed3-144">ในหน้ารายการพื้นที่ทำงาน ให้เลือก **อัปเดตแอป**</span><span class="sxs-lookup"><span data-stu-id="bfed3-144">In a workspace list page, select **Update app**.</span></span> 

    ![อัปเดตแอป](media/service-datasets-build-permissions/power-bi-app-update.png)

1. <span data-ttu-id="bfed3-146">ในแท็บ **สิทธิ์** ให้เลือก **X** เพื่อลบบุคคลหรือกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="bfed3-146">On the **Permissions** tab, select the **X** to delete the person or group.</span></span> 

    ![เลือก X](media/service-datasets-build-permissions/power-bi-app-delete-user.png)
1. <span data-ttu-id="bfed3-148">เลือก **อัปเดตแอป**</span><span class="sxs-lookup"><span data-stu-id="bfed3-148">Select **Update app**.</span></span>

    <span data-ttu-id="bfed3-149">คุณจะเห็นข้อความที่อธิบายว่าคุณจำเป็นต้องไปที่ **จัดการสิทธิ์** เพื่อลบสิทธิ์ในการสร้างสำหรับผู้ใช้ที่มีการเข้าถึงอยู่</span><span class="sxs-lookup"><span data-stu-id="bfed3-149">You see a message explaining that you need to go to **Manage permissions** to remove Build permission for users with existing access.</span></span> 

    ![ข้อความจัดการสิทธิ์](media/service-datasets-build-permissions/power-bi-dataset-app-remove-message.png)

1. <span data-ttu-id="bfed3-151">เลือก **อัปเดต**</span><span class="sxs-lookup"><span data-stu-id="bfed3-151">Select **Update**.</span></span>

1. <span data-ttu-id="bfed3-152">ในพื้นที่ทำงาน ให้ไปที่หน้ารายการ **ชุดข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="bfed3-152">In the workspace, go to the **Datasets** list page.</span></span> 
1. <span data-ttu-id="bfed3-153">เลือก **ตัวเลือกเพิ่มเติม** (...) ที่อยู่ถัดจากชุดข้อมูล > **จัดการสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="bfed3-153">Select **More options** (...) next to the dataset > **Manage permission**.</span></span>

    ![จัดการการอนุญาต](media/service-datasets-build-permissions/power-bi-dataset-permissions-new-look.png)

1. <span data-ttu-id="bfed3-155">เลือก **ตัวเลือกเพิ่มเติม** (...) ที่อยู่ถัดจากชื่อ > **ลบการสร้าง**</span><span class="sxs-lookup"><span data-stu-id="bfed3-155">Select **More options** (...) next to their name > **Remove build**.</span></span>

    ![ลบสิทธิ์ในการสร้าง](media/service-datasets-build-permissions/power-bi-dataset-remove-build-permissions.png)

    <span data-ttu-id="bfed3-157">ผู้ใช้ยังคงสามารถดูรายงานที่สร้างไว้ในชุดข้อมูลที่แชร์ แต่จะไม่สามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="bfed3-157">They can still see the report built on the shared dataset, but they can no longer edit it.</span></span>

## <a name="more-granular-permissions"></a><span data-ttu-id="bfed3-158">สิทธิที่แยกย่อยมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="bfed3-158">More granular permissions</span></span>

<span data-ttu-id="bfed3-159">Power BI เปิดตัวสิทธิ์ในการสร้างในเดือนมิถุนายน 2019 ซึ่งเป็นส่วนเสริมของสิทธิ์ที่มีอยู่ อ่านและแชร์ต่อ</span><span class="sxs-lookup"><span data-stu-id="bfed3-159">Power BI introduced Build permission in June 2019 as a complement to the existing permissions, Read and Reshare.</span></span> <span data-ttu-id="bfed3-160">ผู้ใช้ทั้งหมดที่อยู่มีสิทธิ์ในการอ่านสำหรับชุดข้อมูลผ่านการอนุญาตของแอป การแชร์ หรือการเข้าถึงพื้นที่ทำงานในขณะนั้น ยังได้รับสิทธิ์ในการสร้างสำหรับชุดข้อมูลเดียวกันเหล่านั้นด้วย</span><span class="sxs-lookup"><span data-stu-id="bfed3-160">All users who already had Read permission for datasets via app permissions, sharing, or workspace access at that time also got Build permission for those same datasets.</span></span> <span data-ttu-id="bfed3-161">โดยจะได้รับสิทธิในการสร้างอัตโนมัติเนื่องจากสิทธิในการอ่านได้ให้สิทธิในการสร้างเนื้อหาใหม่ที่ด้านบนของชุดข้อมูล โดยใช้การวิเคราะห์ใน Excel หรือส่งออก</span><span class="sxs-lookup"><span data-stu-id="bfed3-161">They got Build permission automatically because Read permission already granted them the right to build new content on top of the dataset, by using Analyze in Excel or Export.</span></span>

<span data-ttu-id="bfed3-162">ด้วยสิทธิในการสร้างที่แยกย่อยมากขึ้นนี้ คุณสามารถเลือกผู้ที่สามารถดูได้เฉพาะเนื้อหาในรายงานหรือแดชบอร์ดที่มีอยู่เท่านั้น และผู้ที่สามารถสร้างเนื้อหาที่เชื่อมต่อกับชุดข้อมูลเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="bfed3-162">With this more granular Build permission, you can choose who can only view the content in the existing report or dashboard and who can create content connected to the underlying datasets.</span></span>

<span data-ttu-id="bfed3-163">ถ้าชุดข้อมูลของคุณกำลังถูกใช้โดยรายงานที่อยู่นอกพื้นที่ทำงานชุดข้อมูล คุณไม่สามารถลบชุดข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="bfed3-163">If your dataset is being used by a report outside the dataset workspace, you can't delete that dataset.</span></span> <span data-ttu-id="bfed3-164">แต่คุณสามารถดูข้อความแสดงข้อผิดพลาดได้</span><span class="sxs-lookup"><span data-stu-id="bfed3-164">Instead, you see an error message.</span></span>

<span data-ttu-id="bfed3-165">คุณสามารถลบสิทธิ์ในการสร้างได้</span><span class="sxs-lookup"><span data-stu-id="bfed3-165">You can remove Build permission.</span></span> <span data-ttu-id="bfed3-166">ถ้าคุณทำเช่นนั้น บุคคลที่คุณยกเลิกสิทธิ์ไปแล้วจะยังสามารถเห็นรายงานได้ แต่ไม่สามารถแก้ไขรายงานหรือส่งออกข้อมูลพื้นฐานได้อีก</span><span class="sxs-lookup"><span data-stu-id="bfed3-166">If you do, the people whose permissions you have revoked can still see the report, but can no longer edit the report or export underlying data.</span></span> <span data-ttu-id="bfed3-167">เฉพาะผู้ใช้ที่มีสิทธิ์ในการอ่านเท่านั้นที่ยังสามารถส่งออกข้อมูลสรุปได้</span><span class="sxs-lookup"><span data-stu-id="bfed3-167">Users with only read permission can still export summarized data.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="bfed3-168">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="bfed3-168">Next steps</span></span>

- [<span data-ttu-id="bfed3-169">ใช้ชุดข้อมูลทั่วทั้งพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="bfed3-169">Use datasets across workspaces</span></span>](service-datasets-across-workspaces.md)
- <span data-ttu-id="bfed3-170">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="bfed3-170">Questions?</span></span> [<span data-ttu-id="bfed3-171">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="bfed3-171">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
