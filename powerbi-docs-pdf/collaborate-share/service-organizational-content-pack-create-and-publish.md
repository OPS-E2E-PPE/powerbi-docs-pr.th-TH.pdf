---
title: สร้างและเผยแพร่ชุดเนื้อหาขององค์กร Power BI
description: ในบทเรียนนี้ คุณสร้างชุดเนื้อหาองค์กร จำกัดการเข้าถึงกลุ่มระบุ และเผยแพร่ลงในไลบรารีชุดเนื้อหาขององค์กรของคุณใน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: lukaszp
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.date: 08/06/2019
LocalizationGroup: Share your work
ms.openlocfilehash: 0a72582a54903c97dd9594f6a4a1c5980aea8e16
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411735"
---
# <a name="tutorial-create-and-publish-a-power-bi-organizational-content-pack"></a><span data-ttu-id="55bfb-103">บทช่วยสอน: สร้าง และเผยแพร่ชุดเนื้อหาองค์กร Power BI</span><span class="sxs-lookup"><span data-stu-id="55bfb-103">Tutorial: Create and publish a Power BI organizational content pack</span></span>

<span data-ttu-id="55bfb-104">ในบทเรียนนี้ คุณสร้างชุดเนื้อหาองค์กร จำกัดการเข้าถึงกลุ่มเฉพาะและเผยแพร่ลงในไลบรารีของชุดเนื้อหาขององค์กรของคุณใน Power BI</span><span class="sxs-lookup"><span data-stu-id="55bfb-104">In this tutorial, you create an organizational content pack, give access to a specific group, and publish it to your organization's content pack library on Power BI.</span></span>

<span data-ttu-id="55bfb-105">กำลังสร้างชุดเนื้อหาที่จะแตกต่างจากการแชร์แดชบอร์ดหรือการทำงานร่วมกันบนชุดเนื้อหาเหล่านั้นในกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="55bfb-105">Creating content packs is different from sharing dashboards or collaborating on them in a group.</span></span> <span data-ttu-id="55bfb-106">อ่าน[วิธีการแชร์งานของคุณใน Power BI ](service-how-to-collaborate-distribute-dashboards-reports.md)เพื่อตัดสินใจเลือกตัวเลือกที่ดีที่สุดสำหรับสถานการณ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="55bfb-106">Read [Ways to share your work in Power BI](service-how-to-collaborate-distribute-dashboards-reports.md) to decide on the best option for your situation.</span></span>

<span data-ttu-id="55bfb-107">สร้างแพ็คเนื้อหาขององค์กรต้องมี[บัญชี Power BI Pro](https://powerbi.microsoft.com/pricing)สำหรับคุณและเพื่อนร่วมงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="55bfb-107">Creating an organizational content pack requires a [Power BI Pro account](https://powerbi.microsoft.com/pricing) for you and your colleagues.</span></span>

> [!NOTE]
> <span data-ttu-id="55bfb-108">คุณไม่สามารถสร้างหรือติดตั้งชุดเนื้อหาขององค์กรในประสบการณ์ในพื้นที่ทำงานใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="55bfb-108">You can't create or install organizational content packs in the new workspace experiences.</span></span> <span data-ttu-id="55bfb-109">ตอนนี้เป็นเวลาที่เหมาะสมในการอัปเกรดชุดเนื้อหาของคุณไปยังแอป ถ้าคุณยังไม่ได้เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="55bfb-109">If you haven't started yet, Now is a good time to upgrade your content packs to apps.</span></span> <span data-ttu-id="55bfb-110">เรียนรู้[เพิ่มเติมเกี่ยวกับการใช้งานพื้นที่ทำงานใหม่](service-create-the-new-workspaces.md)</span><span class="sxs-lookup"><span data-stu-id="55bfb-110">Learn [more about the new workspace experience](service-create-the-new-workspaces.md).</span></span>

## <a name="create-and-publish-a-content-pack"></a><span data-ttu-id="55bfb-111">สร้างและเผยแพร่ชุดเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="55bfb-111">Create and publish a content pack</span></span>

<span data-ttu-id="55bfb-112">สมมติว่า คุณเป็นผู้จัดการเผยแพร่ของ Contoso และคุณกำลังเตรียมตัววางชายผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="55bfb-112">Imagine you're the Release Manager at Contoso and you're getting ready for a new product launch.</span></span>  <span data-ttu-id="55bfb-113">คุณได้สร้างแดชบอร์ดที่มีรายงานที่คุณต้องการแชร์</span><span class="sxs-lookup"><span data-stu-id="55bfb-113">You've created a dashboard with reports that you'd like to share.</span></span> <span data-ttu-id="55bfb-114">พนักงานอื่น ๆ ที่จัดการการเปิดใช้งานอาจพบว่ามีประโยชน์</span><span class="sxs-lookup"><span data-stu-id="55bfb-114">Other employees managing the launch may find them useful.</span></span> <span data-ttu-id="55bfb-115">คุณต้องการวิธีที่การแพคแดชบอร์ดและรายงานให้เป็นโซลูชันสำหรับเพื่อนร่วมงานของคุณจะได้ใช้</span><span class="sxs-lookup"><span data-stu-id="55bfb-115">You want a way to package up the dashboard and reports as a solution for your colleagues to use.</span></span>

<span data-ttu-id="55bfb-116">คุณต้องการทำตามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="55bfb-116">Want to follow along?</span></span> <span data-ttu-id="55bfb-117">ใน [บริการของ Power BI](https://powerbi.com) ไปที่ **พื้นที่ทำงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="55bfb-117">In the [Power BI service](https://powerbi.com), go to your **My Workspace**.</span></span> <span data-ttu-id="55bfb-118">จากนั้นไปที่ **รับข้อมูล** > **ตัวอย่าง** >  **ตัวอย่างการวิเคราะห์โอกาส** > **เชื่อมต่อ** เพื่อรับสำเนาของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="55bfb-118">Then go to **Get Data** > **Samples** > **Opportunity Analysis Sample** > **Connect** to get your own copy.</span></span>

1. <span data-ttu-id="55bfb-119">ในบานหน้าต่างนำทาง ให้เลือก **พื้นที่ทำงาน** > **พื้นที่ทำงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="55bfb-119">In the nav pane, select **Workspaces** > **My workspaces**.</span></span>

1. <span data-ttu-id="55bfb-120">จากบานหน้าต่างนำทางด้านบน ให้เลือกไอคอนรูปเฟือง ![สกรีนช็อตของไอคอนรูปเฟือง](media/service-organizational-content-pack-create-and-publish/cog.png)</span><span class="sxs-lookup"><span data-stu-id="55bfb-120">From the top nav pane, select the cog icon ![Screenshot of the cog icon.](media/service-organizational-content-pack-create-and-publish/cog.png)</span></span><span data-ttu-id="55bfb-121"> > **สร้างชุดเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="55bfb-121"> > **Create content pack**.</span></span>

   ![สกีนซ็อตของ UI ที่มีความสำคัญกับไอคอนรูปเฟืองและตัวเลือกสร้างชุดเนื้อหา](media/service-organizational-content-pack-create-and-publish/pbi_create_contpk.png)

1. <span data-ttu-id="55bfb-123">ในหน้าต่าง **สร้างชุดเนื้อหา** ให้ใส่ข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="55bfb-123">In the **Create content pack** window, enter the following information.</span></span>  

   <span data-ttu-id="55bfb-124">โปรดทราบว่าไลบรารีชุดเนื้อหาขององค์กรของคุณอาจเติมข้อมูลได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="55bfb-124">Keep in mind that your organization's content pack library might fill up quickly.</span></span> <span data-ttu-id="55bfb-125">ไลบรารีสามารถมีชุดเนื้อหาหลายร้อยชุดที่เผยแพรสำหรับองค์กรหรือกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="55bfb-125">The library could end up with hundreds of content packs published for the organization or for groups.</span></span> <span data-ttu-id="55bfb-126">ใส่ใจกับการตั้งชื่อที่สื่อความหมายเนื้อหาของคุณ เพิ่มคำอธิบายที่ดีและเพื่อเลือกผู้ชมที่ใช่</span><span class="sxs-lookup"><span data-stu-id="55bfb-126">Take time to give your content pack a meaningful name, add a good description, and select the right audience.</span></span>  <span data-ttu-id="55bfb-127">ใช้คำที่จะทำให้ชุดเนื้อหาของคุณสามารถค้นหาได้ง่ายผ่านเครื่องมือค้นหา</span><span class="sxs-lookup"><span data-stu-id="55bfb-127">Use words that makes your content pack easy to find via search.</span></span> <span data-ttu-id="55bfb-128">ซึ่งทำให้ง่ายต่อการค้นหาในอนาคต</span><span class="sxs-lookup"><span data-stu-id="55bfb-128">It makes it easier to find in the future.</span></span>

      ![สกรีนช็อตของแบบฟอร์มชุดเนื้อหาสร้างที่สมบูรณ์](media/service-organizational-content-pack-create-and-publish/cpwindow.png)

    1. <span data-ttu-id="55bfb-130">เลือก **กลุ่มเฉพาะ**</span><span class="sxs-lookup"><span data-stu-id="55bfb-130">Select **Specific Groups**.</span></span>

    1. <span data-ttu-id="55bfb-131">ใส่อยู่อีเมลแบบเต็มสำหรับบุคคล [กลุ่ม Microsoft 365](https://support.office.com/article/Create-a-group-in-Office-365-7124dc4c-1de9-40d4-b096-e8add19209e9) กลุ่มการกระจาย หรือกลุ่มความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="55bfb-131">Enter the full email addresses for individuals, [Microsoft 365 groups](https://support.office.com/article/Create-a-group-in-Office-365-7124dc4c-1de9-40d4-b096-e8add19209e9), distribution groups, or security groups.</span></span> <span data-ttu-id="55bfb-132">ตัวอย่างเช่น: salesmgrs@contoso.comsales@contoso.com</span><span class="sxs-lookup"><span data-stu-id="55bfb-132">For example: salesmgrs@contoso.com; sales@contoso.com</span></span>

        <span data-ttu-id="55bfb-133">สำหรับบทเรียนนี้ ลองใช้อีเมลหรือกลุ่มที่อยู่อีเมลของคุณ</span><span class="sxs-lookup"><span data-stu-id="55bfb-133">For this tutorial, try using your group's email address.</span></span>

    1. <span data-ttu-id="55bfb-134">ชื่อชุดเนื้อหา *โอกาสทางการขาย*</span><span class="sxs-lookup"><span data-stu-id="55bfb-134">Name the content pack *Sales Opportunities*.</span></span>

        > [!TIP]
        > <span data-ttu-id="55bfb-135">พิจารณารวมถึงชื่อของแดชบอร์ดในชื่อของชุดเนื้อหานี้</span><span class="sxs-lookup"><span data-stu-id="55bfb-135">Consider including the name of the dashboard in the name of the content pack.</span></span> <span data-ttu-id="55bfb-136">ด้วยวิธี เพื่อนร่วมงานของคุณจะค้นหาแดชบอร์ดได้ง่ายยิ่งขึ้นหลังจากที่พวกเขาเชื่อมต่อกับชุดเนื้อหาของคุณ</span><span class="sxs-lookup"><span data-stu-id="55bfb-136">That way, your colleagues can find the dashboard more easily after they connect to your content pack.</span></span>

    1. <span data-ttu-id="55bfb-137">แนะนำ: เพิ่มคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="55bfb-137">Recommended: Add a description.</span></span> <span data-ttu-id="55bfb-138">ซึ่งช่วยให้เพื่อนร่วมงานค้นหาชุดเนื้อหาเพิ่มเติมได้อย่างง่ายดายตามที่พวกเขาต้องการ</span><span class="sxs-lookup"><span data-stu-id="55bfb-138">It helps coworkers more easily find the content packs that they need.</span></span> <span data-ttu-id="55bfb-139">นอกเหนือจากคำอธิบาย ให้เพิ่มคำสำคัญที่เพื่อนร่วมงานของคุณอาจใช้เพื่อค้นหาชุดเนื้อหานี้</span><span class="sxs-lookup"><span data-stu-id="55bfb-139">Besides a description, add keywords your coworkers might use to search for this content pack.</span></span> <span data-ttu-id="55bfb-140">รวมถึงข้อมูลที่ติดต่อในกรณีที่เพื่อนร่วมงานของคุณมีคำถาม หรือต้องการความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="55bfb-140">Include contact information in case your coworkers have a question or need help.</span></span>

    1. <span data-ttu-id="55bfb-141">อัปโหลดรูปภาพหรือโลโก้เพื่อช่วยให้สมาชิกกลุ่มสามารถค้นหาชุดเนื้อหาได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="55bfb-141">Upload an image or logo to make it easier for group members to find the content pack.</span></span>

        <span data-ttu-id="55bfb-142">คุณสามารถสแกนรูปภาพได้รวดเร็วกว่าการสแกนข้อความ</span><span class="sxs-lookup"><span data-stu-id="55bfb-142">It's faster to scan for an image than to scan for text.</span></span> <span data-ttu-id="55bfb-143">สกรีนช็อตจะแสดงรูปภาพของไทล์แผนภูมิคอลัมน์ **จำนวนโอกาส**</span><span class="sxs-lookup"><span data-stu-id="55bfb-143">The screenshot shows an image of the **Opportunity Count** column chart tile.</span></span>

    1. <span data-ttu-id="55bfb-144">เลือกแดชบอร์ด **ตัวอย่างการวิเคราะห์โอกาส** เพื่อเพิ่มลงในชุดเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="55bfb-144">Select the **Opportunity Analysis Sample** dashboard to add it to the content pack.</span></span>

        <span data-ttu-id="55bfb-145">Power BI เพิ่มรายงานที่เกี่ยวข้องกับชุดข้อมูลโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="55bfb-145">Power BI automatically adds the associated report and dataset.</span></span> <span data-ttu-id="55bfb-146">คุณสามารถเพิ่มบุคคลอื่นได้ ถ้าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="55bfb-146">You can add others, if you want.</span></span>

       > [!NOTE]
       > <span data-ttu-id="55bfb-147">Power BI จะระบุเฉพาะแดชบอร์ด รายงาน ชุดข้อมูล และสมุดงานที่คุณสามารถแก้ไขได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="55bfb-147">Power BI only lists the dashboards, reports, datasets, and workbooks that you can edit.</span></span> <span data-ttu-id="55bfb-148">ดังนั้นแอปจะไม่แสดงผลใด ๆ ที่ใช้ร่วมกันกับคุณ</span><span class="sxs-lookup"><span data-stu-id="55bfb-148">Thus, the app doesn't display any that were shared with you.</span></span>

   1. <span data-ttu-id="55bfb-149">ถ้าคุณมีสมุดงาน Excel คุณเห็นค่าเหล่านั้นภายใต้ **รายงาน** ที่มีไอคอน Excel</span><span class="sxs-lookup"><span data-stu-id="55bfb-149">If you have Excel workbooks, you see them under **Reports**, with an Excel icon.</span></span> <span data-ttu-id="55bfb-150">คุณสามารถเพิ่มลงในชุดเนื้อหา เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="55bfb-150">You can add them to the content pack, too.</span></span>

      ![สกรีนช็อตของส่วนรายงานและรายงานที่คุณสามารถเลือกได้](media/service-organizational-content-pack-create-and-publish/pbi_orgcontpkexcel.png)

      > [!NOTE]
      > <span data-ttu-id="55bfb-152">ถ้าสมาชิกของกลุ่มไม่สามารถดูสมุดงาน Excel ได้ คุณอาจจำเป็นต้อง[แชร์เวิร์กบุ๊กกับบุคคลเหล่านั้นใน OneDrive for Business](https://support.office.com/article/Share-documents-or-folders-in-Office-365-1fe37332-0f9a-4719-970e-d2578da4941c)</span><span class="sxs-lookup"><span data-stu-id="55bfb-152">If members of the group can't view the Excel workbook, you may need to [share the workbook with them in OneDrive for Business](https://support.office.com/article/Share-documents-or-folders-in-Office-365-1fe37332-0f9a-4719-970e-d2578da4941c).</span></span>

1. <span data-ttu-id="55bfb-153">เลือก **เผยแพร่** เมื่อต้องเพิ่มชุดเนื้อหาลงในไลบรารีแพ็คเนื้อหาขององค์กรของกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="55bfb-153">Select **Publish** to add the content pack to the group's organizational content pack library.</span></span>  

   <span data-ttu-id="55bfb-154">คุณเห็นข้อความสำเร็จเมื่อการเผยแพร่เรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="55bfb-154">You see a success message when it publishes successfully.</span></span>

1. <span data-ttu-id="55bfb-155">เมื่อสมาชิกของกลุ่มของคุณไปที่ **รับข้อมูล** > **ชุดเนื้อหาขององค์กร** พวกเขาจะเห็นชุดเนื้อหาของคุณ</span><span class="sxs-lookup"><span data-stu-id="55bfb-155">When members of your group go to **Get Data** > **Organizational Content Packs**, they see your content pack.</span></span>

   ![สกรีนช็อตของชุดเนื้อหาของโอกาสทางการขายในกล่องโต้ตอบ AppSource](media/service-organizational-content-pack-create-and-publish/powerbi-find-content-pack-organization.png)

   > [!TIP]
   > <span data-ttu-id="55bfb-157">URL ที่ปรากฏในเบราว์เซอร์ของคุณคือที่อยู่ที่ไม่ซ้ำกันสำหรับชุดเนื้อหานี้</span><span class="sxs-lookup"><span data-stu-id="55bfb-157">The URL displayed in your browser is an unique address for this content pack.</span></span>  <span data-ttu-id="55bfb-158">ต้องการบอกเพื่อนร่วมงานของคุณเกี่ยวกับชุดเนื้อหาใหม่นี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="55bfb-158">Want to tell your coworkers about this new content pack?</span></span>  <span data-ttu-id="55bfb-159">วาง URL ลงในอีเมล</span><span class="sxs-lookup"><span data-stu-id="55bfb-159">Paste the URL into an email.</span></span>

1. <span data-ttu-id="55bfb-160">เมื่อสมาชิกของกลุ่มของคุณเลือก **เชื่อมต่อ** พวกเขาสามารถ [ดูและทำงานกับชุดเนื้อหาของคุณ](service-organizational-content-pack-copy-refresh-access.md)</span><span class="sxs-lookup"><span data-stu-id="55bfb-160">When your group members select **Connect**, they can [view and work with your content pack](service-organizational-content-pack-copy-refresh-access.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="55bfb-161">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="55bfb-161">Next steps</span></span>

* <span data-ttu-id="55bfb-162">[บทนำชุดเนื้อหาองค์กรใน Power BI](service-organizational-content-pack-introduction.md)</span><span class="sxs-lookup"><span data-stu-id="55bfb-162">[Intro to organizational content packs in Power BI](service-organizational-content-pack-introduction.md).</span></span>

* <span data-ttu-id="55bfb-163">[จัดการ อัปเดต และลบชุดเนื้อหาองค์กร](service-organizational-content-pack-manage-update-delete.md)</span><span class="sxs-lookup"><span data-stu-id="55bfb-163">[Manage, update, and delete organizational content packs](service-organizational-content-pack-manage-update-delete.md).</span></span>

* <span data-ttu-id="55bfb-164">[เผยแพร่แอปใน Power BI](service-create-distribute-apps.md)</span><span class="sxs-lookup"><span data-stu-id="55bfb-164">[Publish an app in Power BI](service-create-distribute-apps.md).</span></span>

* [<span data-ttu-id="55bfb-165">อะไรคือ OneDrive สำหรับธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="55bfb-165">What is OneDrive for Business?</span></span>](https://support.office.com/article/What-is-OneDrive-for-Business-187f90af-056f-47c0-9656-cc0ddca7fdc2)

* <span data-ttu-id="55bfb-166">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="55bfb-166">More questions?</span></span> [<span data-ttu-id="55bfb-167">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="55bfb-167">Try the Power BI Community</span></span>](https://community.powerbi.com/)
