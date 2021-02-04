---
title: การรักษาความปลอดภัยระดับแถว (RLS) ในเซิร์ฟเวอร์รายงาน Power BI
description: เรียนรู้เกี่ยวกับการใช้การรักษาความปลอดภัยระดับแถว (RLS) ในเซิร์ฟเวอร์รายงาน Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-report-server
ms.topic: how-to
ms.date: 01/22/2019
ms.openlocfilehash: eb06bc41aaaeea9790c34bb808548506963b8cb8
ms.sourcegitcommit: 9350f994b7f18b0a52a2e9f8f8f8e472c342ea42
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/22/2020
ms.locfileid: "90861854"
---
# <a name="row-level-security-rls-in-power-bi-report-server"></a><span data-ttu-id="640a6-103">การรักษาความปลอดภัยระดับแถว (RLS) ในเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="640a6-103">Row-level security (RLS) in Power BI Report Server</span></span>

<span data-ttu-id="640a6-104">การตั้งค่าความปลอดภัยระดับแถว (RLS) กับเซิร์ฟเวอร์รายงาน Power BI สามารถจำกัดการเข้าถึงข้อมูลสำหรับผู้ใช้ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="640a6-104">Setting up row-level security (RLS) with Power BI Report Server can restrict data access for given users.</span></span> <span data-ttu-id="640a6-105">ตัวกรองจำกัดการเข้าถึงข้อมูลในระดับแถว และคุณสามารถกำหนดตัวกรองภายในบทบาทได้</span><span class="sxs-lookup"><span data-stu-id="640a6-105">Filters restrict data access at the row level, and you can define filters within roles.</span></span>  <span data-ttu-id="640a6-106">หากคุณใช้การอนุญาตเริ่มต้นในเซิร์ฟเวอร์รายงาน Power BI ผู้ใช้ใด ๆ ที่มีสิทธิ์ผู้เผยแพร่หรือตัวจัดการเนื้อหาสำหรับรายงาน Power BI สามารถกำหนดสมาชิกให้กับบทบาทสำหรับรายงานนั้น</span><span class="sxs-lookup"><span data-stu-id="640a6-106">If you're using the default permissions in Power BI Report Server, any user with Publisher or Content Manager permissions for the Power BI report can assign members to roles for that report.</span></span>    

<span data-ttu-id="640a6-107">คุณสามารถกำหนดค่า RLS สำหรับรายงานที่นำเข้าไปยัง Power BI ด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="640a6-107">You configure RLS for reports imported into Power BI with Power BI Desktop.</span></span> <span data-ttu-id="640a6-108">คุณยังสามารถกำหนดค่า RLS บนรายงานที่ใช้ DirectQuery เช่น SQL Server ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="640a6-108">You can also configure RLS on reports that use DirectQuery, such as SQL Server.</span></span>  <span data-ttu-id="640a6-109">โปรดทราบว่า RLS จะไม่ปฏิบัติตามหากการเชื่อมต่อ DirectQuery ของคุณใช้การตรวจสอบสิทธิ์แบบรวมสำหรับโปรแกรมอ่านรายงาน</span><span class="sxs-lookup"><span data-stu-id="640a6-109">Keep in mind that RLS isn't respected if your DirectQuery connection uses integrated authentication for report readers.</span></span> <span data-ttu-id="640a6-110">ในส่วนการเชื่อมต่อสดของ Analysis Services คุณสามารถกำหนดค่ารักษาความปลอดภัยระดับแถวบนแบบจำลองภายในองค์กรได้</span><span class="sxs-lookup"><span data-stu-id="640a6-110">For Analysis Services live connections, you configure row-level security on the on-premises model.</span></span> <span data-ttu-id="640a6-111">ตัวเลือกความปลอดภัยจะไม่แสดงสำหรับชุดข้อมูลที่เชื่อมต่อสด</span><span class="sxs-lookup"><span data-stu-id="640a6-111">The security option doesn't show up for live connection datasets.</span></span> 

[!INCLUDE [rls-desktop-define-roles](../includes/rls-desktop-define-roles.md)]

## <a name="bidirectional-cross-filtering"></a><span data-ttu-id="640a6-112">การกรองแบบข้ามสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="640a6-112">Bidirectional cross-filtering</span></span>

<span data-ttu-id="640a6-113">ตามค่าเริ่มต้น การกรอง row-level security จะใช้ตัวกรองทิศทางเดียว โดยไม่คำนึงว่าการตั้งค่าความสัมพันธ์เป็นแบบทิศทางเดียวหรือสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="640a6-113">By default, row-level security filtering uses single-directional filters, regardless of whether the relationships are set to single direction or bidirectional.</span></span> <span data-ttu-id="640a6-114">คุณสามารถเปิดใช้งานการกรองแบบข้ามสองทิศทาง ด้วยความปลอดภัยระดับแถวด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="640a6-114">You can manually enable bidirectional cross-filter with row-level security.</span></span>

- <span data-ttu-id="640a6-115">เลือกความสัมพันธ์ และทำเครื่องหมายบนกล่องกาเครื่องหมาย **ใช้ตัวกรองความปลอดภัยในทั้งสองทิศทาง**</span><span class="sxs-lookup"><span data-stu-id="640a6-115">Select the relationship and check the **Apply security filter in both directions** checkbox.</span></span> 

    ![ใช้ตัวกรองความปลอดภัย](media/row-level-security-report-server/rls-apply-security-filter.png)

<span data-ttu-id="640a6-117">ทำเครื่องหมายที่ช่องนี้เมื่อใช้งาน[การรักษาความปลอดภัยระดับแถวแบบไดนามิก](/analysis-services/tutorial-tabular-1200/supplemental-lesson-implement-dynamic-security-by-using-row-filters)ตามชื่อผู้ใช้หรือรหัสล็อกอิน</span><span class="sxs-lookup"><span data-stu-id="640a6-117">Check this box when implementing [dynamic row-level security](/analysis-services/tutorial-tabular-1200/supplemental-lesson-implement-dynamic-security-by-using-row-filters) based on user name or login ID.</span></span> 

<span data-ttu-id="640a6-118">เพื่อเรียนรู้เพิ่มเติม ดูที่[ตัวกรองไขว้แบบสองทิศทางที่ใช้ DirectQuery ใน Power BI Desktop](../transform-model/desktop-bidirectional-filtering.md)และบทความเชิงเทคนิคของ[การรักษาความปลอดภัยแบบลำจองภาษา BI แบบตาราง](https://download.microsoft.com/download/D/2/0/D20E1C5F-72EA-4505-9F26-FEF9550EFD44/Securing%20the%20Tabular%20BI%20Semantic%20Model.docx)</span><span class="sxs-lookup"><span data-stu-id="640a6-118">To learn more, see [Bidirectional cross-filtering using DirectQuery in Power BI Desktop](../transform-model/desktop-bidirectional-filtering.md) and the [Securing the Tabular BI Semantic Model](https://download.microsoft.com/download/D/2/0/D20E1C5F-72EA-4505-9F26-FEF9550EFD44/Securing%20the%20Tabular%20BI%20Semantic%20Model.docx) technical whitepaper.</span></span>

[!INCLUDE [rls-desktop-view-as-roles](../includes/rls-desktop-view-as-roles.md)]


## <a name="add-members-to-roles"></a><span data-ttu-id="640a6-119">เพิ่มสมาชิกไปยังบทบาท</span><span class="sxs-lookup"><span data-stu-id="640a6-119">Add members to roles</span></span> 

<span data-ttu-id="640a6-120">หลังจากคุณบันทึกรายงานของคุณใน Power BI Report Server แล้วคุณจะจัดการความปลอดภัยและเพิ่มหรือลบสมาชิกบนเซิร์ฟเวอร์ได้</span><span class="sxs-lookup"><span data-stu-id="640a6-120">After you save your report in Power BI Report Server, you manage security and add or remove members on the server.</span></span> <span data-ttu-id="640a6-121">เฉพาะผู้ใช้ที่ มีสิทธิ์ผู้เผยแพร่หรือผู้จัดการเนื้อหาสำหรับรายงานที่มีตัวเลือกการรักษาความปลอดภัยระดับแถวพร้อมใช้งานและไม่เป็นสีเทาเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="640a6-121">Only users with either Publisher or Content Manager permissions for the report have the row-level security option available and not greyed out.</span></span>

 <span data-ttu-id="640a6-122">ถ้ารายงานไม่มีบทบาทจำเป็น คุณจำเป็นเมื่อต้องเปิดใน Power BI Desktop เพิ่มหรือปรับเปลี่ยนบทบาท จาก นั้นบันทึกกลับไปยังเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="640a6-122">If the report doesn't have the roles it needs, you need to open it in Power BI Desktop, add or modify roles, then save it back to Power BI Report Server.</span></span> 

1. <span data-ttu-id="640a6-123">ใน Power BI Desktop บันทึกรายงานไปยังเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="640a6-123">In Power BI Desktop, save the report to Power BI Report Server.</span></span> <span data-ttu-id="640a6-124">คุณจะต้องมีเวอร์ชั่น Power BI Desktop ที่ปรับให้เหมาะสำหรับเซิร์ฟเวอร์รายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="640a6-124">You need to use the version of Power BI Desktop optimized for Power BI Report Server.</span></span>
2. <span data-ttu-id="640a6-125">ในบริการ Power BI รายงาน เลือกจุดไข่ปลา ( **...** ) ถัดจากรายงาน</span><span class="sxs-lookup"><span data-stu-id="640a6-125">In Power BI Report Service, select the ellipsis (**…**) next to the report.</span></span> 

3. <span data-ttu-id="640a6-126">เลือก**จัดการ** > **ความปลอดภัยระดับแถว**</span><span class="sxs-lookup"><span data-stu-id="640a6-126">Select **Manage** > **Row-level security**.</span></span> 

     ![จัดการความปลอดภัยระดับแถว](media/row-level-security-report-server/power-bi-report-server-rls-dialog.png)

    <span data-ttu-id="640a6-128">บนหน้า **การรักษาความปลอดภัยระดับแถว** คุณสามารถเพิ่มสมาชิกบทบาทที่คุณสร้างขึ้นใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="640a6-128">On the **Row-level security** page, you add members to a role you created in Power BI Desktop.</span></span>

5. <span data-ttu-id="640a6-129">เมื่อต้องเพิ่มสมาชิก เลือก**เพิ่มสมาชิก**</span><span class="sxs-lookup"><span data-stu-id="640a6-129">To add a member, select **Add Member**.</span></span>

1. <span data-ttu-id="640a6-130">ป้อนผู้ใช้หรือกลุ่มในกล่องข้อความในรูปแบบชื่อผู้ใช้ (DOMAIN\user) และเลือกบทบาทที่คุณต้องการกำหนดให้กับพวกเขา</span><span class="sxs-lookup"><span data-stu-id="640a6-130">Enter the user or group in the text box in the Username format (DOMAIN\user) and select the roles you wish to assign to them.</span></span> <span data-ttu-id="640a6-131">สมาชิกรายนี้จะต้องอยู่ภายในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="640a6-131">The member has to be within your organization.</span></span>   

    ![เพิ่มสมาชิกไปยังบทบาท](media/row-level-security-report-server/power-bi-report-server-add-members.png)

    <span data-ttu-id="640a6-133">ทั้งนี้ขึ้นอยู่กับวิธีที่คุณตั้งค่า Active Directory ไว้ การป้อนชื่อผู้ใช้หลักที่นี่ก็ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="640a6-133">Depending on how you have Active Directory configured, entering the User Principal Name here also works.</span></span> <span data-ttu-id="640a6-134">ในกรณีนั้น เซิร์ฟเวอร์รายงานจะแสดงชื่อผู้ใช้ที่เกี่ยวข้องในรายการ</span><span class="sxs-lookup"><span data-stu-id="640a6-134">In that case, the Report Server shows the corresponding username in the list.</span></span>

1. <span data-ttu-id="640a6-135">คลิก**ตกลง**เพื่อนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="640a6-135">Click **OK** to apply.</span></span>   

8. <span data-ttu-id="640a6-136">หากต้องการลบสมาชิก ให้ทำเครื่องหมายที่ช่องถัดจากชื่อและเลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="640a6-136">To remove members, check the box next to their names and select **Delete**.</span></span>  <span data-ttu-id="640a6-137">คุณสามารถลบสมาชิกหลายคนพร้อมกันได้</span><span class="sxs-lookup"><span data-stu-id="640a6-137">You can delete multiple members at a time.</span></span> 

    ![ลบสมาชิก](media/row-level-security-report-server/power-bi-report-server-delete-members.png)


## <a name="username-and-userprincipalname"></a><span data-ttu-id="640a6-139">username () และ userprincipalname ()</span><span class="sxs-lookup"><span data-stu-id="640a6-139">username() and userprincipalname()</span></span>

<span data-ttu-id="640a6-140">คุณสามารถใช้ประโยชน์จากฟังก์ชัน DAX username() หรือ userprincipalname() ภายในชุดข้อมูลของคุณได้</span><span class="sxs-lookup"><span data-stu-id="640a6-140">You can take advantage of the DAX functions username() or userprincipalname() within your dataset.</span></span> <span data-ttu-id="640a6-141">คุณสามารถใช้กับนิพจน์ใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="640a6-141">You can use them within expressions in Power BI Desktop.</span></span> <span data-ttu-id="640a6-142">เมื่อคุณเผยแพร่โมเดลของคุณ เซิร์ฟเวอร์ Power BI Report จะใช้โมเดลเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="640a6-142">When you publish your model, Power BI Report Server uses them.</span></span>

<span data-ttu-id="640a6-143">ภายใน Power BI Desktop username() จะส่งผู้ใช้กลับในรูปแบบของ DOMAIN\User และ userprincipalname() จะส่งผู้ใช้กลับในรูปแบบของ user@contoso.com</span><span class="sxs-lookup"><span data-stu-id="640a6-143">Within Power BI Desktop, username() returns a user in the format of DOMAIN\User and userprincipalname() returns a user in the format of user@contoso.com.</span></span>

<span data-ttu-id="640a6-144">ภายในเซิร์ฟเวอร์รายงาน Power BI ชื่อผู้ใช้ () และ userprincipalname () ทั้งคู่ส่งคืนชื่อผู้ใช้หลัก (UPN) ของผู้ใช้ซึ่งคล้ายกับที่อยู่อีเมล</span><span class="sxs-lookup"><span data-stu-id="640a6-144">Within Power BI Report Server, username() and userprincipalname() both return the user's User Principal Name (UPN), which is similar to an email address.</span></span>

<span data-ttu-id="640a6-145">หากคุณใช้การรับรองความถูกต้องที่กำหนดเองใน Power BI Report Server จะส่งคืนรูปแบบชื่อผู้ใช้ที่คุณตั้งค่าสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="640a6-145">If you're using custom authentication in Power BI Report Server, it returns the username format you’ve set up for users.</span></span>  

## <a name="limitations"></a><span data-ttu-id="640a6-146">ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="640a6-146">Limitations</span></span> 

<span data-ttu-id="640a6-147">นี่คือข้อจำกัดในปัจจุบันสำหรับการรักษาความปลอดภัยระดับแถวในโมเดล Power BI</span><span class="sxs-lookup"><span data-stu-id="640a6-147">Here are the current limitations for row-level security on Power BI models.</span></span> 

<span data-ttu-id="640a6-148">ผู้ใช้ที่มีรายงานโดยใช้ชื่อผู้ใช้ () ฟังก์ชั่น DAX จะสังเกตเห็นพฤติกรรมใหม่ในขณะนี้ซึ่งชื่อผู้ใช้หลัก (UPN) จะถูกส่งคืนยกเว้นเมื่อใช้ DirectQuery กับการรักษาความปลอดภัยแบบรวม</span><span class="sxs-lookup"><span data-stu-id="640a6-148">Users that had reports using the username() DAX function will notice new behavior now where the User Principal Name (UPN) is returned EXCEPT when using DirectQuery with integrated security.</span></span>  <span data-ttu-id="640a6-149">เนื่องจาก RLS ไม่ได้ปฏิบัติตามในสถานการณ์นั้น ลักษณะการทำงานในสถานการณ์นั้นจะไม่เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="640a6-149">Since RLS isn't respected in that scenario, the behavior in that scenario is unchanged.</span></span>

<span data-ttu-id="640a6-150">คุณสามารถกำหนด RLS บนชุดข้อมูลที่สร้างขึ้นด้วย Power BI Desktop เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="640a6-150">You can define RLS only on datasets created with Power BI Desktop.</span></span> <span data-ttu-id="640a6-151">เพื่อเปิดใช้งาน RLS สำหรับชุดข้อมูลที่สร้างขึ้นโดยใช้ Excel คุณจะต้องแปลงไฟล์ของคุณให้เป็นไฟล์ Power BI Desktop (PBIX) ก่อน</span><span class="sxs-lookup"><span data-stu-id="640a6-151">To enable RLS for datasets created with Excel, you must convert your files into Power BI Desktop (PBIX) files first.</span></span> <span data-ttu-id="640a6-152">เรียนรู้เพิ่มเติมเกี่ยวกับ[การแปลงแฟ้ม Excel](../connect-data/desktop-import-excel-workbooks.md)</span><span class="sxs-lookup"><span data-stu-id="640a6-152">Learn more about [converting Excel files](../connect-data/desktop-import-excel-workbooks.md).</span></span>

<span data-ttu-id="640a6-153">เฉพาะการสกัด แปลง และโหลดข้อมูล (ETL) และการเชื่อมต่อ DirectQuery โดยใช้ข้อมูลประจำตัวจะได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="640a6-153">Only Extract, Transform, Load (ETL) and DirectQuery connections using stored credentials are supported.</span></span> <span data-ttu-id="640a6-154">การเชื่อมต่อแบบสดไปยังบริการการวิเคราะห์และการเชื่อมต่อ DirectQuery โดยใช้การรับรองความถูกต้องแบบรวมถูกจัดการในแหล่งข้อมูลพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="640a6-154">Live connections to Analysis Services and DirectQuery connections using integrated authentication are handled in the underlying data source.</span></span> 

<span data-ttu-id="640a6-155">ถ้าคุณกำลังใช้การรักษาความปลอดภัยแบบรวมกับ DirectQuery แล้วผู้ใช้ของคุณอาจสังเกตเห็น:</span><span class="sxs-lookup"><span data-stu-id="640a6-155">If you're using integrated security with DirectQuery, then your users may notice:</span></span>
- <span data-ttu-id="640a6-156">RLS ถูกปิดใช้งาน และข้อมูลทั้งหมดจะถูกส่งกลับ</span><span class="sxs-lookup"><span data-stu-id="640a6-156">RLS is disabled and all data is returned.</span></span>
- <span data-ttu-id="640a6-157">ผู้ใช้ไม่สามารถอัปเดตการกำหนดบทบาทและรับข้อผิดพลาดในหน้า RLS Manage ได้</span><span class="sxs-lookup"><span data-stu-id="640a6-157">Users can't update their role assignments, and get an error on the RLS Manage page.</span></span>
- <span data-ttu-id="640a6-158">สำหรับฟังก์ชั่นชื่อผู้ใช้ DAX คุณจะได้รับชื่อผู้ใช้เป็น DOMAIN \ USER ต่อไป</span><span class="sxs-lookup"><span data-stu-id="640a6-158">For the DAX username function, you continue to receive the username as DOMAIN\USER.</span></span> 

<span data-ttu-id="640a6-159">ผู้เขียนรายงานไม่มีสิทธิ์เข้าถึงเพื่อดูข้อมูลรายงานใน Power BI Report Server จนกว่าพวกเขาจะกำหนดบทบาทให้ตัวเองหลังจากอัปโหลดรายงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="640a6-159">Report authors don't have access to view the report data in Power BI Report Server until they've assigned themselves roles accordingly after uploading the report.</span></span> 

 

## <a name="faq"></a><span data-ttu-id="640a6-160">คำถามที่ถามบ่อย</span><span class="sxs-lookup"><span data-stu-id="640a6-160">FAQ</span></span> 

### <a name="can-i-create-these-roles-for-analysis-services-data-sources"></a><span data-ttu-id="640a6-161">ฉันสามารถสร้างบทบาทเหล่านี้สำหรับแหล่งข้อมูล Analysis Services ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="640a6-161">Can I create these roles for Analysis Services data sources?</span></span> 

<span data-ttu-id="640a6-162">คุณสามารถสร้างได้ถ้าคุณนำเข้าข้อมูลลงใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="640a6-162">You can if you imported the data into Power BI Desktop.</span></span> <span data-ttu-id="640a6-163">ถ้าคุณกำลังใช้ข้อมูลแบบ live connection คุณไม่สามารถกำหนดค่า RLS ภายในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="640a6-163">If you're using a live connection, you can't configure RLS within the Power BI service.</span></span> <span data-ttu-id="640a6-164">RLS จะได้รับการกำหนดภายใน Analysis Services แบบจำลองภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="640a6-164">RLS is defined within the Analysis Services model on-premises.</span></span> 

### <a name="can-i-use-rls-to-limit-the-columns-or-measures-accessible-by-my-users"></a><span data-ttu-id="640a6-165">ฉันสามารถใช้ RLS เพื่อจำกัดคอลัมน์หรือหน่วยวัดที่สามารถเข้าถึงโดยผู้ใช้ของฉันได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="640a6-165">Can I use RLS to limit the columns or measures accessible by my users?</span></span> 

<span data-ttu-id="640a6-166">หมายเลข</span><span class="sxs-lookup"><span data-stu-id="640a6-166">No.</span></span> <span data-ttu-id="640a6-167">ถ้าผู้ใช้มีสิทธิ์เข้าถึงแถวเฉพาะของข้อมูล พวกเขาสามารถเห็นคอลัมน์ทั้งหมดของข้อมูลสำหรับแถวนั้น</span><span class="sxs-lookup"><span data-stu-id="640a6-167">If a user has access to a particular row of data, they can see all the columns of data for that row.</span></span> 

### <a name="does-rls-let-me-hide-detailed-data-but-give-access-to-data-summarized-in-visuals"></a><span data-ttu-id="640a6-168">RLS อนุญาตให้ฉันซ่อนข้อมูลรายละเอียด แต่ให้สิทธิ์การเข้าถึงข้อมูลที่สรุปไว้ในภาพหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="640a6-168">Does RLS let me hide detailed data but give access to data summarized in visuals?</span></span> 

<span data-ttu-id="640a6-169">ไม่ ถึงแม่ว่าคุณรักษาข้อมูลของแต่ละแถว แต่ผู้ใช้สามารถดูรายละเอียดหรือข้อมูลสรุปได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="640a6-169">No, you secure individual rows of data but users can always see either the details or the summarized data.</span></span> 

### <a name="can-i-add-new-roles-in-power-bi-desktop-if-i-already-have-existing-roles-and-members-assigned"></a><span data-ttu-id="640a6-170">ฉันสามารถเพิ่มบทบาทใหม่ใน Power BI Desktop ได้หรือไม่ถ้าฉันมีบทบาทและสมาชิกที่กำหนดอยู่แล้ว?</span><span class="sxs-lookup"><span data-stu-id="640a6-170">Can I add new roles in Power BI Desktop if I already have existing roles and members assigned?</span></span> 

<span data-ttu-id="640a6-171">ใช่ ถ้าคุณมีการกำหนดบทบาทที่มีอยู่แล้วและสมาชิกที่ได้รับมอบหมายใน Power BI Report Server คุณสามารถสร้างบทบาทเพิ่มเติมและเผยแพร่รายงานของคุณโดยไม่มีผลกับการมอบหมายปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="640a6-171">Yes, if you already have existing roles defined and members assigned in Power BI Report Server, you can make additional roles and republish your report with no effect on your current assignments.</span></span> 
 

## <a name="next-steps"></a><span data-ttu-id="640a6-172">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="640a6-172">Next steps</span></span>

<span data-ttu-id="640a6-173">[เซิร์ฟเวอร์รายงาน Power BI คืออะไร](get-started.md) 
[ภาพรวมของผู้ดูแลระบบ](admin-handbook-overview.md)</span><span class="sxs-lookup"><span data-stu-id="640a6-173">[What is Power BI Report Server?](get-started.md) 
[Administrator handbook](admin-handbook-overview.md)</span></span>  

<span data-ttu-id="640a6-174">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="640a6-174">More questions?</span></span> [<span data-ttu-id="640a6-175">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="640a6-175">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)