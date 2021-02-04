---
title: วิชวลของ Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิชวล Power BI แบบกำหนดเอง เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
manager: rkarlin
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: overview
ms.date: 07/14/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 3d2e8f46605238a87eb23c32765f0a4ffaa02400
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888086"
---
# <a name="visuals-in-power-bi"></a><span data-ttu-id="d928f-104">วิชวลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="d928f-104">Visuals in Power BI</span></span>

<span data-ttu-id="d928f-105">Power BI มาพร้อมกับวิชวล Power BI แบบนอกกรอบ</span><span class="sxs-lookup"><span data-stu-id="d928f-105">Power BI comes with many out-of-the box Power BI visuals.</span></span> <span data-ttu-id="d928f-106">วิชวลเหล่านี้จะพร้อมใช้งานในบานหน้าต่างการแสดงผลข้อมูลด้วยภาพทั้งของ [Power BI Desktop](https://powerbi.microsoft.com/desktop/) และ [บริการ Power BI](https://app.powerbi.com) และสามารถใช้สำหรับการสร้างและแก้ไขเนื้อหา Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="d928f-106">These visuals are available in the visualization pane of both [Power BI Desktop](https://powerbi.microsoft.com/desktop/) and [Power BI service](https://app.powerbi.com), and can be used for creating and editing Power BI content.</span></span>

:::image type="content" source="media/power-bi-custom-visuals/power-bi-visualizations.png" alt-text="สกรียนช็อตของ Power B I การแสดงภาพบานหน้าต่างที่ปรากฏใน Power B I Desktop และบริการของ Power B I":::

<span data-ttu-id="d928f-108">วิชวล Power BI อีกมากมายพร้อมใช้งานใน [AppSource](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fappsource.microsoft.com%2Fen-us%2Fmarketplace%2Fapps%3Fpage%3D1%26product%3Dpower-bi-visuals&data=02%7C01%7CKesem.Sharabi%40microsoft.com%7C6d9286afacb3468d4cde08d740b76694%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637049028749147718&sdata=igWm0e1vXdgGcbyvngQBrHQVAkahPnxPC1ZhUPntGI8%3D&reserved=0) ของ Microsoft หรือผ่าน Power BI</span><span class="sxs-lookup"><span data-stu-id="d928f-108">Many more Power BI visuals are available from the Microsoft [AppSource](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fappsource.microsoft.com%2Fen-us%2Fmarketplace%2Fapps%3Fpage%3D1%26product%3Dpower-bi-visuals&data=02%7C01%7CKesem.Sharabi%40microsoft.com%7C6d9286afacb3468d4cde08d740b76694%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637049028749147718&sdata=igWm0e1vXdgGcbyvngQBrHQVAkahPnxPC1ZhUPntGI8%3D&reserved=0) or through Power BI.</span></span> <span data-ttu-id="d928f-109">วิชวลเหล่านี้จะถูกสร้างขึ้นโดย Microsoft และคู่ค้าของ Microsoft และได้รับการทดสอบและตรวจสอบความถูกต้องโดยทีมตรวจสอบ AppSource</span><span class="sxs-lookup"><span data-stu-id="d928f-109">These visuals are created by Microsoft and Microsoft partners, and are tested and validated by the AppSource validation team.</span></span>

<span data-ttu-id="d928f-110">นอกจากนี้คุณยังสามารถพัฒนาวิชวล Power BI ของคุณเองเพื่อใช้โดยคุณ องค์กรของคุณ หรือชุมชน Power BI ทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="d928f-110">You can also develop your own Power BI visual, to be used by you, your organization, or the entire Power BI community.</span></span>

## <a name="default-power-bi-visuals"></a><span data-ttu-id="d928f-111">วิชวล Power BI ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d928f-111">Default Power BI visuals</span></span>

<span data-ttu-id="d928f-112">นี่คือวิชวล Power BI แบบนอกกรอบที่พร้อมใช้งานจากบานหน้าต่างการแสดงผลข้อมูลด้วยภาพใน *Power BI Desktop* และ *บริการ Power BI*</span><span class="sxs-lookup"><span data-stu-id="d928f-112">These are the out-of-the-box Power BI visuals available from the visualization pane in *Power BI Desktop* and *Power BI Service*.</span></span>

<span data-ttu-id="d928f-113">เมื่อต้องการถอนหมุดวิชวล Power BI ออกจากบานหน้าต่างการแสดงผลข้อมูลด้วยภาพ ให้คลิกขวาและเลือก **ถอนหมุด**</span><span class="sxs-lookup"><span data-stu-id="d928f-113">To unpin a Power BI visual from the visualization pane, right-click it and select **unpin**.</span></span>

<span data-ttu-id="d928f-114">เมื่อต้องการคืนค่าวิชวล Power BI ค่าเริ่มต้น ในบานหน้าต่างการแสดงผลข้อมูลด้วยภาพ ให้คลิก **นำเข้าวิชวลแบบกำหนดเอง** และเลือก **คืนค่าวิชวลค่าเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="d928f-114">To restore the default Power BI visuals in the visualization pane, click **Import a custom visual** and select **Restore default visuals**.</span></span> 

## <a name="appsource-power-bi-visuals"></a><span data-ttu-id="d928f-115">วิชวล Power BI ของ AppSource</span><span class="sxs-lookup"><span data-stu-id="d928f-115">AppSource Power BI visuals</span></span>

<span data-ttu-id="d928f-116">สมาชิกของชุมชนและ Microsoft มีส่วนร่วมในวิชวล Power BI เพื่อสาธารณประโยชน์และเผยแพร่ไปยัง [AppSource](https://appsource.microsoft.com/marketplace/apps?product=power-bi-visuals)</span><span class="sxs-lookup"><span data-stu-id="d928f-116">Microsoft and community members contribute Power BI visuals for public benefit, and publish them to the [AppSource](https://appsource.microsoft.com/marketplace/apps?product=power-bi-visuals).</span></span> <span data-ttu-id="d928f-117">คุณสามารถดาวน์โหลดวิชวลเหล่านี้ และเพิ่มลงในรายงาน Power BI ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="d928f-117">You can download these visuals and add them to your Power BI reports.</span></span> <span data-ttu-id="d928f-118">Microsoft ได้รับการทดสอบและอนุมัติส่วนแสดงผล Power BI เหล่านี้ทั้งหมด ทั้งฟังก์ชันการใช้งานและคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="d928f-118">Microsoft has tested and approved these Power BI visuals for functionality and quality.</span></span>

>[!NOTE]
>* <span data-ttu-id="d928f-119">ด้วยการใช้ วิชวลของ Power BI ซึ่งสร้างจาก SDK คุณอาจจะนำเข้าข้อมูลจาก หรือส่งข้อมูลไปสู่บุคคลที่สามหรือบริการอื่น ๆ ที่อยู่ภายนอกพื้นที่ทางกายภาพของผู้เช่า Power BI ขอบเขตการปฏิบัติตามข้อบังคับ หรือนอกเขตระบบคลาวด์แห่งชาติ</span><span class="sxs-lookup"><span data-stu-id="d928f-119">By using Power BI visuals created with our SDK, you may be importing data from, or sending data to, third party or other services located outside of your Power BI tenant’s geographic area, compliance boundary, or national cloud instance.</span></span>
>* <span data-ttu-id="d928f-120">วิชวล Power BI ที่ผ่านการรับรองคือวิชวลใน AppSource ที่มีการทดสอบเพื่อตรวจสอบว่าภาพไม่สามารถเข้าถึงบริการภายนอกหรือแหล่งข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="d928f-120">Power BI certified visuals are visuals in the AppSource that were additionally tested to check that the visual does not access external services or resources.</span></span>
>* <span data-ttu-id="d928f-121">เมื่อมีการนำเข้าวิชวล Power BI จาก AppSource ภาพอาจได้รับการอัปเดตโดยอัตโนมัติโดยไม่ต้องแจ้งให้ทราบเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d928f-121">Once Power BI visuals from AppSource are imported, visuals may be updated automatically without any additional notice.</span></span>

### <a name="what-is-appsource"></a><span data-ttu-id="d928f-122">AppSource คืออะไร</span><span class="sxs-lookup"><span data-stu-id="d928f-122">What is AppSource?</span></span>

<span data-ttu-id="d928f-123">[AppSource](https://appsource.microsoft.com/marketplace/apps?product=power-bi-visuals) เป็นสถานที่ค้นหาแอป add-in และส่วนขยายสำหรับซอฟต์แวร์ Microsoft ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d928f-123">[AppSource](https://appsource.microsoft.com/marketplace/apps?product=power-bi-visuals) is the place for apps, add-ins, and extensions for your Microsoft software.</span></span> <span data-ttu-id="d928f-124">AppSource เชื่อมต่อผู้ใช้ของผลิตภัณฑ์ เช่น Microsoft 365, Azure, Dynamics 365, Cortana และ Power BI นับล้านคน ไปยังโซลูชันที่ช่วยให้พวกเขาทำงานสำเร็จได้อย่างมีประสิทธิภาพขึ้น และเข้าใจได้ลึกซึ้งขึ้นกว่าที่เคย</span><span class="sxs-lookup"><span data-stu-id="d928f-124">AppSource connects millions of users of products such as Microsoft 365, Azure, Dynamics 365, Cortana, and Power BI, to solutions that help them get work done more efficiently and insightfully than before.</span></span>

### <a name="certified-power-bi-visuals"></a><span data-ttu-id="d928f-125">ส่วนจัดแสดง Power BI ที่ผ่านการรับรอง</span><span class="sxs-lookup"><span data-stu-id="d928f-125">Certified Power BI visuals</span></span>

<span data-ttu-id="d928f-126">ส่วนการจัดแสดง Power BI ที่ได้รับการรับรองคือวิชวลใน [AppSource](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fappsource.microsoft.com%2Fen-us%2Fmarketplace%2Fapps%3Fpage%3D1%26product%3Dpower-bi-visuals&data=02%7C01%7CKesem.Sharabi%40microsoft.com%7C6d9286afacb3468d4cde08d740b76694%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637049028749147718&sdata=igWm0e1vXdgGcbyvngQBrHQVAkahPnxPC1ZhUPntGI8%3D&reserved=0) ที่ตรงตามข้อกำหนดรหัสที่ระบุไว้ ซึ่งผ่านการทดสอบและได้รับอนุมัติจากทีม Microsoft Power BI team แล้ว</span><span class="sxs-lookup"><span data-stu-id="d928f-126">Certified Power BI visuals are visuals in [AppSource](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fappsource.microsoft.com%2Fen-us%2Fmarketplace%2Fapps%3Fpage%3D1%26product%3Dpower-bi-visuals&data=02%7C01%7CKesem.Sharabi%40microsoft.com%7C6d9286afacb3468d4cde08d740b76694%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637049028749147718&sdata=igWm0e1vXdgGcbyvngQBrHQVAkahPnxPC1ZhUPntGI8%3D&reserved=0) that meet certain specified code requirements that the Microsoft Power BI team has tested and approved.</span></span> <span data-ttu-id="d928f-127">มีการออกแบบการทดสอบที่ทำขึ้นเพื่อตรวจสอบวิชวลที่ไม่ได้เข้าถึงบริการหรือทรัพยากรภายนอก</span><span class="sxs-lookup"><span data-stu-id="d928f-127">The tests are designed to check that the visual doesn't access external services or resources.</span></span>

<span data-ttu-id="d928f-128">เมื่อต้องการดูรายการของส่วนแสดงผล Power BI ที่ผ่านการรับรอง หรือต้องการส่งวิชวลของคุณเอง ให้ดู [วิชวล Power BI ที่ผ่านการรับรองแล้ว](power-bi-custom-visuals-certified.md)</span><span class="sxs-lookup"><span data-stu-id="d928f-128">To view the list of certified Power BI visuals, or to submit your own, see [Certified Power BI visuals](power-bi-custom-visuals-certified.md).</span></span>

### <a name="samples-for-power-bi-visuals"></a><span data-ttu-id="d928f-129">ตัวอย่างสำหรับวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="d928f-129">Samples for Power BI visuals</span></span>

<span data-ttu-id="d928f-130">วิชวล Power BI แต่ละวิชวลบน AppSource มีตัวอย่างข้อมูลที่แสดงให้เห็นวิธีการทำงานของวิชวล</span><span class="sxs-lookup"><span data-stu-id="d928f-130">Each Power BI visual on AppSource has a data sample that illustrates how the visual works.</span></span> <span data-ttu-id="d928f-131">เมื่อต้องการดาวน์โหลดตัวอย่าง ให้เลือกวิชวล Power BI ใน [AppSource](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fappsource.microsoft.com%2Fen-us%2Fmarketplace%2Fapps%3Fpage%3D1%26product%3Dpower-bi-visuals&data=02%7C01%7CKesem.Sharabi%40microsoft.com%7C6d9286afacb3468d4cde08d740b76694%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637049028749147718&sdata=igWm0e1vXdgGcbyvngQBrHQVAkahPnxPC1ZhUPntGI8%3D&reserved=0) และจากส่วน *ลองตัวอย่าง* ให้คลิกลิงก์ **รายงานตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="d928f-131">To download the sample, in the [AppSource](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fappsource.microsoft.com%2Fen-us%2Fmarketplace%2Fapps%3Fpage%3D1%26product%3Dpower-bi-visuals&data=02%7C01%7CKesem.Sharabi%40microsoft.com%7C6d9286afacb3468d4cde08d740b76694%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637049028749147718&sdata=igWm0e1vXdgGcbyvngQBrHQVAkahPnxPC1ZhUPntGI8%3D&reserved=0) select a Power BI visual and from the *Try a sample* section, click the **sample report** link.</span></span>

## <a name="organizational-store"></a><span data-ttu-id="d928f-132">ที่เก็บข้อมูลขององค์กร</span><span class="sxs-lookup"><span data-stu-id="d928f-132">Organizational store</span></span>

<span data-ttu-id="d928f-133">ผู้ดูแลระบบ Power BI อนุมัติและปรับใช้วิชวล Power BI ไปยังองค์กรของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="d928f-133">Power BI admins approve and deploy Power BI visuals into their organization.</span></span> <span data-ttu-id="d928f-134">การดำเนินการนี้จะช่วยให้ผู้เขียนรายงานสามารถค้นหา อัปเดต และใช้วิชวล Power BI เหล่านี้ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="d928f-134">This allows report authors to easily discover, update, and use these Power BI visuals.</span></span> <span data-ttu-id="d928f-135">ผู้ดูแลระบบสามารถจัดการวิชวลเหล่านี้ได้อย่างง่ายดายด้วยการดำเนินการ เช่น อัปเดตเวอร์ชัน การปิดใช้งานและการเปิดใช้งานวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="d928f-135">Admins can easily manage these visuals with actions such as updating versions, disabling and enabling Power BI visuals.</span></span>

<span data-ttu-id="d928f-136">เมื่อต้องการเข้าถึงร้านค้าองค์กร ในบานหน้าต่าง *การแสดงผลข้อมูลด้วยภาพ* ให้คลิก **นำเข้าวิชวลแบบกำหนดเอง** เลือก **นำเข้าจาก marketplace** และที่ด้านบนของหน้าต่าง *วิชวล Power BI* ให้เลือกแท็บ **องค์กรของฉัน**</span><span class="sxs-lookup"><span data-stu-id="d928f-136">To access the organizational store, in the *Visualization* pane click **Import a custom visual**, select **Import from marketplace** and in the top of the *Power BI visuals* window, select the **My organization** tab.</span></span>

<span data-ttu-id="d928f-137">[อ่านเพิ่มเติมเกี่ยวกับการแสดงผลด้วยภาพขององค์กร](power-bi-custom-visuals-organization.md)</span><span class="sxs-lookup"><span data-stu-id="d928f-137">[Read more about organizational visuals](power-bi-custom-visuals-organization.md).</span></span>

## <a name="visual-files"></a><span data-ttu-id="d928f-138">ไฟล์วิชวล</span><span class="sxs-lookup"><span data-stu-id="d928f-138">Visual files</span></span>

<span data-ttu-id="d928f-139">ส่วนแสดงผล Power BI เป็นแพคเกจที่รวมเอาโค้ดสำหรับการนำเสนอข้อมูลที่ให้บริการในภาพ</span><span class="sxs-lookup"><span data-stu-id="d928f-139">Power BI visuals are packages that include code for rendering the data served to them.</span></span> <span data-ttu-id="d928f-140">ทุกคนสามารถสร้างภาพแบบกำหนดเองและรวมภาพนั้นเป็นไฟล์ `.pbiviz` เดียวที่สามารถนำเข้าไปในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="d928f-140">Anyone can create a custom visual and package it as a single `.pbiviz` file, that can then be imported into a Power BI report.</span></span>

<span data-ttu-id="d928f-141">เมื่อต้องการนำเข้าวิชวล Power BI ในบานหน้าต่าง *การแสดงผลข้อมูลด้วยภาพ* ให้คลิก **นำเข้า วิชวลแบบกำหนดเอง** และเลือก **นำเข้าจากไฟล์**</span><span class="sxs-lookup"><span data-stu-id="d928f-141">To import a Power BI visual, in the *Visualization* pane click **Import a custom visual** and select **Import from file**.</span></span>

<span data-ttu-id="d928f-142">ถ้าคุณเป็นนักพัฒนาเว็บและมีความสนใจในการสร้างวิชวลของคุณเองและเพิ่มลงใน AppSource คุณสามารถเรียนรู้วิธีการ [พัฒนาวิชวลของการ์ดวงกลม Power BI](develop-circle-card.md) และ [เผยแพร่วิชวล Power BI ไปยัง AppSource](office-store.md) ได้</span><span class="sxs-lookup"><span data-stu-id="d928f-142">If you are you a web developer and are interested in creating your own visual and adding it to AppSource, you can learn how to [develop a Power BI circle card visual](develop-circle-card.md) and [publish a Power BI visual to AppSource](office-store.md).</span></span>

> [!WARNING]
> <span data-ttu-id="d928f-143">วิชวล Power BI สามารถประกอบด้วยโค้ด ที่มีความเสี่ยงด้านความปลอดภัยหรือความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="d928f-143">A Power BI visual could contain code with security or privacy risks.</span></span> <span data-ttu-id="d928f-144">ตรวจสอบให้แน่ใจว่าคุณเชื่อถือผู้เขียนและแหล่งข้อมูลวิชวล Power BI ก่อนที่จะนำเข้าไปยังรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="d928f-144">Make sure you trust the author and Power BI visual source before importing it to your report.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d928f-145">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d928f-145">Next steps</span></span>

>[!div class="nextstepaction"]
>[<span data-ttu-id="d928f-146">พัฒนาวิชวลการ์ดวงกลม Power BI</span><span class="sxs-lookup"><span data-stu-id="d928f-146">Develop a Power BI circle card visual</span></span>](develop-circle-card.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="d928f-147">โครงสร้างของโครงการวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="d928f-147">Power BI visuals project structure</span></span>](visual-project-structure.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="d928f-148">คำแนะนำสำหรับวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="d928f-148">Guidelines for Power BI visuals</span></span>](guidelines-powerbi-visuals.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="d928f-149">คำถามที่ถามบ่อย</span><span class="sxs-lookup"><span data-stu-id="d928f-149">Frequently asked questions</span></span>](power-bi-custom-visuals-faq.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="d928f-150">ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="d928f-150">Power BI Community</span></span>](https://community.powerbi.com/)