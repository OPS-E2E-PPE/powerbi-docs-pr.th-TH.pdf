---
title: วิชวล Power BI ที่ผ่านการรับรองในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: ข้อกำหนดและกระบวนการที่จะส่งวิชวลแบบกำหนดเองสำหรับการรับรองและรายการของวิชวล Power BI ที่ผ่านการรับรอง เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: how-to
ms.date: 03/08/2020
ms.openlocfilehash: 5f337197655d41b830b237c04faa2642991c34ee
ms.sourcegitcommit: a5e98bc86915f7bea6a0ab5df282683840e63d2c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/07/2021
ms.locfileid: "97969822"
---
# <a name="get-a-power-bi-visual-certified"></a><span data-ttu-id="29ee4-104">รับการรับรองส่วนการจัดแสดง Power BI</span><span class="sxs-lookup"><span data-stu-id="29ee4-104">Get a Power BI visual certified</span></span>

<span data-ttu-id="29ee4-105">วิชวล Power BI ที่ได้รับการรับรองคือวิชวล Power BI ใน [AppSource](https://appsource.microsoft.com/en-us/marketplace/apps?page=1&product=power-bi-visuals) ที่ตรงตามข้อกำหนดโค้ดทีม Microsoft Power BI team [แล้ว](#certification-requirements)</span><span class="sxs-lookup"><span data-stu-id="29ee4-105">Certified Power BI visuals are Power BI visuals in [AppSource](https://appsource.microsoft.com/en-us/marketplace/apps?page=1&product=power-bi-visuals) that meet the Microsoft Power BI team [code requirements](#certification-requirements).</span></span> <span data-ttu-id="29ee4-106">วิชวลเหล่านี้จะได้รับการทดสอบเพื่อตรวจสอบว่าไม่สามารถเข้าถึงบริการภายนอกหรือแหล่งข้อมูล และทำตามรูปแบบการเขียนโค้ดที่ปลอดภัยและแนวทาง</span><span class="sxs-lookup"><span data-stu-id="29ee4-106">These visuals are tested to verify that they don't access external services or resources, and that they follow secure coding patterns and guidelines.</span></span>

<span data-ttu-id="29ee4-107">เมื่อการจัดแสดง Power BI ได้รับการรับรองแล้ว จะมีคุณลักษณะเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="29ee4-107">Once a Power BI visual is certified, it offers more features.</span></span> <span data-ttu-id="29ee4-108">เช่น คุณสามารถ[ส่งออกไปยัง PowerPoint](../../consumer/end-user-powerpoint.md) หรือแสดงวิชวลในอีเมลเมื่อผู้ใช้[สมัครใช้งานในหน้ารายงาน](../../consumer/end-user-subscribe.md)</span><span class="sxs-lookup"><span data-stu-id="29ee4-108">For example, you can [export to PowerPoint](../../consumer/end-user-powerpoint.md), or display the visual in received emails, when a user [subscribes to report pages](../../consumer/end-user-subscribe.md).</span></span>

<span data-ttu-id="29ee4-109">กระบวนการการรับรองที่เป็นทางเลือก</span><span class="sxs-lookup"><span data-stu-id="29ee4-109">The certification process is optional.</span></span> <span data-ttu-id="29ee4-110">วิชวล power BI ที่ไม่ได้รับการรับรองไม่จำเป็นต้องใช้วิชวล Power BI ที่ไม่ปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="29ee4-110">Power BI visuals that are not certified, are not necessarily unsafe Power BI visuals.</span></span> <span data-ttu-id="29ee4-111">การแสดงผลด้วยภาพของ Power BI บางอันไม่ผ่านการรับรองเนื่องจากไม่สอดคล้องกับ [ข้อกำหนดในการรับรอง](power-bi-custom-visuals-certified.md#certification-requirements)หนึ่งรายการหรือมากกว่านั้น</span><span class="sxs-lookup"><span data-stu-id="29ee4-111">Some Power BI visuals aren't certified because they don't comply with one or more of the [certification requirements](power-bi-custom-visuals-certified.md#certification-requirements).</span></span> <span data-ttu-id="29ee4-112">สำหรับตัวอย่าง เช่น แผนที่วิชวล Power BI ที่เชื่อมต่อกับบริการภายนอกหรือวิชวล Power BI ที่ใช้ไลบรารีเชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="29ee4-112">For example, a map Power BI visual connecting to an external service, or a Power BI visual using commercial libraries.</span></span>

> [!NOTE]
> <span data-ttu-id="29ee4-113">Microsoftไม่ใช่บริษัทบุคคลที่สามที่สร้าง Power BI วิชวล</span><span class="sxs-lookup"><span data-stu-id="29ee4-113">Microsoft is not the author of third-party Power BI visuals.</span></span> <span data-ttu-id="29ee4-114">เพื่อยืนยันการใช้งานอย่างเต็มประสิทธิภาพจากวิชวลบุคคลที่สาม แนะนำให้ลูกค้าติดต่อผู้เขียนของวิชวลโดยตรง</span><span class="sxs-lookup"><span data-stu-id="29ee4-114">To verify the functionality of third-party visuals, contact the author of the visual directly.</span></span>

## <a name="certification-requirements"></a><span data-ttu-id="29ee4-115">ข้อบังคับสำหรับการรับรอง</span><span class="sxs-lookup"><span data-stu-id="29ee4-115">Certification requirements</span></span>

<span data-ttu-id="29ee4-116">ในการรับ[การรับรอง](#get-a-power-bi-visual-certified) วิชวล Power BI ของคุณ ต้องแน่ใจว่าวิชวล Power BI ของคุณเป็นไปตามรายการข้อกำหนดในส่วนนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="29ee4-116">To get your Power BI visual [certified](#get-a-power-bi-visual-certified), your Power BI visual must comply with the requirements listed in this section.</span></span> 

### <a name="general-requirements"></a><span data-ttu-id="29ee4-117">ข้อกำหนดทั่วไป</span><span class="sxs-lookup"><span data-stu-id="29ee4-117">General requirements</span></span>

<span data-ttu-id="29ee4-118">วิชวล Power BI ของคุณต้องได้รับการอนุมัติจากศูนย์คู่ค้า</span><span class="sxs-lookup"><span data-stu-id="29ee4-118">Your Power BI visual has to be approved by Partner Center.</span></span> <span data-ttu-id="29ee4-119">เราขอแนะนำให้วิชวล Power BI ของคุณอยู่ใน [AppSource](https://appsource.microsoft.com/marketplace/apps?page=1&product=power-bi-visuals) แล้ว</span><span class="sxs-lookup"><span data-stu-id="29ee4-119">We recommend that your Power BI visual is already in [AppSource](https://appsource.microsoft.com/marketplace/apps?page=1&product=power-bi-visuals).</span></span> <span data-ttu-id="29ee4-120">ในการเรียนสิธีเผยแพร่วิชวล Power BI ไปยัง AppSource ดู[การเผยแพร่วิชวล Power BI ไปยังศูนย์คู่ค้า](office-store.md)</span><span class="sxs-lookup"><span data-stu-id="29ee4-120">To learn how to publish a Power BI visual to AppSource, see [Publish Power BI visuals to Partner Center](office-store.md).</span></span>

<span data-ttu-id="29ee4-121">ก่อนที่จะส่งวิชวล Power BI ของคุณเพื่อรับรองความถูกต้อง ตรวจสอบว่าเป็นไปตาม [แนวทางสำหรับวิชวล Power BI](guidelines-powerbi-visuals.md)</span><span class="sxs-lookup"><span data-stu-id="29ee4-121">Before submitting your Power BI visual to be certified, verify that it complies with the [guidelines for Power BI visuals](guidelines-powerbi-visuals.md).</span></span>

<span data-ttu-id="29ee4-122">เมื่อส่งวิชวล Power BI ให้ตรวจสอบให้แน่ใจว่าแพคเกจที่แปลแล้วตรงกับแพคเกจที่ส่งเข้าไป</span><span class="sxs-lookup"><span data-stu-id="29ee4-122">When submitting the Power BI visual, make sure that the compiled package exactly matches the submitted package.</span></span>

### <a name="code-repository-requirements"></a><span data-ttu-id="29ee4-123">ข้อกำหนดของที่เก็บโค้ด:</span><span class="sxs-lookup"><span data-stu-id="29ee4-123">Code repository requirements</span></span>

<span data-ttu-id="29ee4-124">แม้ว่าคุณจะไม่จำเป็นต้องแชร์รหัสของคุณใน GitHub แบบสาธารณะ การเก็บโค้ดก็จะพร้อมใช้งานสำหรับการตรวจทานโดยทีม Power BI</span><span class="sxs-lookup"><span data-stu-id="29ee4-124">Although you don't have to publicly share your code in GitHub, the code repository has to be available for a review by the Power BI team.</span></span> <span data-ttu-id="29ee4-125">วิธีที่ดีที่สุดในการทำเช่นนี้คือการให้แหล่งโค้ด (JavaScript หรือ TypeScript) ใน GitHub</span><span class="sxs-lookup"><span data-stu-id="29ee4-125">The best way to do this, is by providing the source code (JavaScript or TypeScript) in GitHub.</span></span>

<span data-ttu-id="29ee4-126">ที่เก็บต้องมีสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="29ee4-126">The repository must contain the following:</span></span>
* <span data-ttu-id="29ee4-127">รหัสสำหรับการแสดงผลด้วยภาพของ Power BI เดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="29ee4-127">Code for only one Power BI visual.</span></span> <span data-ttu-id="29ee4-128">ซึ่งไม่สามารถมีโค้ดสำหรับวิชวล Power BI หลายหรือรหัสที่ไม่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="29ee4-128">It can't contain code for multiple Power BI visuals, or unrelated code.</span></span>
* <span data-ttu-id="29ee4-129">สาขาที่ชื่อว่า **ใบรับรอง** (จำเป็นต้องใช้ตัวพิมพ์เล็ก)</span><span class="sxs-lookup"><span data-stu-id="29ee4-129">A branch named **certification** (lowercase required).</span></span> <span data-ttu-id="29ee4-130">แหล่งโค้ดในสาขานี้ต้องตรงกับแพคเกจที่ส่งไป</span><span class="sxs-lookup"><span data-stu-id="29ee4-130">The source code in this branch has to match the submitted package.</span></span> <span data-ttu-id="29ee4-131">โค้ดนี้สามารถอัปเดตได้ระหว่างขั้นตอนการส่งครั้งถัดไป ถ้าคุณกำลังส่งวิชวล Power BI ของคุณใหม่</span><span class="sxs-lookup"><span data-stu-id="29ee4-131">This code can only be updated during the next submission process, if you're resubmitting your Power BI visual.</span></span>

<span data-ttu-id="29ee4-132">ถ้าวิชวล Power BI ของคุณใช้แพคเกจ npm แบบส่วนตัวหรือโมดูลย่อย git คุณต้องให้การเข้าถึงที่เก็บข้อมูลเพิ่มเติมที่มีโค้ดนี้</span><span class="sxs-lookup"><span data-stu-id="29ee4-132">If your Power BI visual uses private npm packages, or git submodules, you must provide access to the additional repositories containing this code.</span></span>

<span data-ttu-id="29ee4-133">เพื่อทำความเข้าใจวิธีการดูที่เก็บข้อมูลการแสดงผลด้วยภาพของ Power BI ให้ตรวจสอบที่เก็บ GitHub สำหรับ [แผนภูมิแท่งตัวอย่างของ Power BI](https://github.com/microsoft/PowerBI-visuals-sampleBarChart)</span><span class="sxs-lookup"><span data-stu-id="29ee4-133">To understand how a Power BI visual repository looks, review the GitHub repository for the [Power BI visuals sample bar chart](https://github.com/microsoft/PowerBI-visuals-sampleBarChart).</span></span>

### <a name="file-requirements"></a><span data-ttu-id="29ee4-134">ข้อกำหนดไฟล์</span><span class="sxs-lookup"><span data-stu-id="29ee4-134">File requirements</span></span>

<span data-ttu-id="29ee4-135">ใช้ API รุ่นล่าสุดเพื่อเขียนวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="29ee4-135">Use the latest version of the API to write the Power BI visual.</span></span>

<span data-ttu-id="29ee4-136">ที่เก็บต้องมีไฟล์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="29ee4-136">The repository must include the following files:</span></span>
* <span data-ttu-id="29ee4-137">**gitignore**- เพิ่ม `node_modules` `.tmp` และ `dist` ไปยังไฟล์นี้</span><span class="sxs-lookup"><span data-stu-id="29ee4-137">**.gitignore** - Add `node_modules`, `.tmp` and  `dist` to this file.</span></span> <span data-ttu-id="29ee4-138">รหัสไม่สามารถมี *node_modules* *. tmp* หรือ *โฟลเดอร์  beta.dist* ได้</span><span class="sxs-lookup"><span data-stu-id="29ee4-138">The code cannot include the *node_modules*, *.tmp* or *dist* folders.</span></span>
* <span data-ttu-id="29ee4-139">**capabilities.json** - ถ้าคุณกำลังส่งเวอร์ชันที่ใหม่กว่าของวิชวล Power BI ของคุณด้วยการเปลี่ยนแปลงคุณสมบัติในไฟล์นี้ โปรดตรวจสอบว่าไฟล์นั้นไม่ได้แบ่งแยกรายงานสำหรับผู้ใช้ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="29ee4-139">**capabilities.json** - If you are submitting newer version of your Power BI visual with changes to the properties in this file, verify that they do not break reports for existing users.</span></span>
* <span data-ttu-id="29ee4-140">**pbiviz.json**</span><span class="sxs-lookup"><span data-stu-id="29ee4-140">**pbiviz.json**</span></span> 
* <span data-ttu-id="29ee4-141">**pbiviz.json**</span><span class="sxs-lookup"><span data-stu-id="29ee4-141">**package.json**.</span></span> <span data-ttu-id="29ee4-142">การแสดงผลด้วยภาพต้องมีการติดตั้งแพคเกจต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="29ee4-142">The visual must have the following package installed:</span></span>
   * <span data-ttu-id="29ee4-143">["tslint"](https://www.npmjs.com/package/tslint)- เวอร์ชัน 5.18.0 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="29ee4-143">["tslint"](https://www.npmjs.com/package/tslint) - Version 5.18.0 or higher</span></span>
   * <span data-ttu-id="29ee4-144">["typescript"](https://www.npmjs.com/package/typescript)- เวอร์ชัน 3.0.0 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="29ee4-144">["typescript"](https://www.npmjs.com/package/typescript) - Version 3.0.0 or higher</span></span>
   * <span data-ttu-id="29ee4-145">["tslint-microsoftcontrib"](https://www.npmjs.com/package/tslint-microsoft-contrib) - เวอร์ชัน 6.2.0 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="29ee4-145">["tslint-microsoftcontrib"](https://www.npmjs.com/package/tslint-microsoft-contrib) - Version 6.2.0 or higher</span></span>
   * <span data-ttu-id="29ee4-146">ไฟล์ต้องประกอบด้วยคำสั่งสำหรับการเรียกใช้ linter -  `"lint": "tslint -c tslint.json -p tsconfig.json"`</span><span class="sxs-lookup"><span data-stu-id="29ee4-146">The file must contain a command for running linter -  `"lint": "tslint -c tslint.json -p tsconfig.json"`</span></span>
* <span data-ttu-id="29ee4-147">**pbiviz.json**</span><span class="sxs-lookup"><span data-stu-id="29ee4-147">**package-lock.json**</span></span>
* <span data-ttu-id="29ee4-148">**pbiviz.json**</span><span class="sxs-lookup"><span data-stu-id="29ee4-148">**tsconfig.json**</span></span>

### <a name="command-requirements"></a><span data-ttu-id="29ee4-149">ข้อกำหนดคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="29ee4-149">Command requirements</span></span>

<span data-ttu-id="29ee4-150">ตรวจสอบให้แน่ใจว่าคำสั่งต่อไปนี้ไม่ได้ส่งกลับข้อผิดพลาดใดๆ</span><span class="sxs-lookup"><span data-stu-id="29ee4-150">Make sure that the following commands don't return any errors.</span></span>

* `npm install`
* `pbiviz package`
* <span data-ttu-id="29ee4-151">`npm audit` - ต้องไม่ส่งกลับคำเตือนใดๆ ที่มีระดับสูงหรือระดับปานกลาง</span><span class="sxs-lookup"><span data-stu-id="29ee4-151">`npm audit` - Must not return any warnings with high or moderate level.</span></span>
* <span data-ttu-id="29ee4-152">[TSlint จาก Microsoft](https://www.npmjs.com/package/tslint-microsoft-contrib) ที่มี[กำหนดค่าที่จำเป็น](https://github.com/microsoft/PowerBI-visuals-sampleBarChart/blob/master/tslint.json)</span><span class="sxs-lookup"><span data-stu-id="29ee4-152">[TSlint from Microsoft](https://www.npmjs.com/package/tslint-microsoft-contrib) with [the required configuration](https://github.com/microsoft/PowerBI-visuals-sampleBarChart/blob/master/tslint.json).</span></span> <span data-ttu-id="29ee4-153">คำสั่งนี้ต้องไม่ส่งข้อ lint ผิดพลาดใดๆ กลับมา</span><span class="sxs-lookup"><span data-stu-id="29ee4-153">This command must not return any lint errors.</span></span>

### <a name="compiling-requirements"></a><span data-ttu-id="29ee4-154">ข้อกำหนดตัวแปลโปรแกรม</span><span class="sxs-lookup"><span data-stu-id="29ee4-154">Compiling requirements</span></span>

<span data-ttu-id="29ee4-155">ใช้ [เครื่องมือ-วิชวล-powerbi](https://www.npmjs.com/package/powerbi-visuals-tools) รุ่นล่าสุดเพื่อเขียนวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="29ee4-155">Use the latest version of [powerbi-visuals-tools](https://www.npmjs.com/package/powerbi-visuals-tools) to write the Power BI visual.</span></span>

<span data-ttu-id="29ee4-156">คุณต้องคอมไพล์วิชวล Power BI ของคุณด้วย `pbiviz package`</span><span class="sxs-lookup"><span data-stu-id="29ee4-156">You must compile your Power BI visual with `pbiviz package`.</span></span> <span data-ttu-id="29ee4-157">ถ้าคุณกำลังใช้สคริปต์การสร้างของคุณเองให้  `npm run package`คำสั่งสร้างแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="29ee4-157">If you're using your own build scripts, provide a `npm run package` custom build command.</span></span>

### <a name="source-code-requirements"></a><span data-ttu-id="29ee4-158">ข้อกำหนดของแหล่งโค้ด</span><span class="sxs-lookup"><span data-stu-id="29ee4-158">Source code requirements</span></span>

<span data-ttu-id="29ee4-159">ตรวจสอบว่าคุณได้ทำตามรายการนโยบาย [ การรับรองความถูกต้องของ Power BI](/legal/marketplace/certification-policies#1200-power-bi-visuals-additional-certification)</span><span class="sxs-lookup"><span data-stu-id="29ee4-159">Verify that you follow the [Power BI visuals additional certification](/legal/marketplace/certification-policies#1200-power-bi-visuals-additional-certification) policy list.</span></span> <span data-ttu-id="29ee4-160">หากการส่งของคุณไม่เป็นไปตามหลักเกณฑ์เหล่านี้ อีเมลที่ใช้ในการปฏิเสธจากศูนย์คู่ค้าจะรวมถึงหมายเลขนโยบายที่แสดงรายการอยู่ในลิงก์นี้</span><span class="sxs-lookup"><span data-stu-id="29ee4-160">If your submission doesn't follow these guidelines, the rejection email from Partner Center will include the policy numbers listed in this link.</span></span>

<span data-ttu-id="29ee4-161">ปฏิบัติตามข้อกำหนดของโค้ดที่แสดงด้านล่างเพื่อตรวจสอบให้แน่ใจว่าโค้ดของคุณอยู่ในแนวทางด้วยนโยบายการรับรอง Power BI</span><span class="sxs-lookup"><span data-stu-id="29ee4-161">Follow the code requirements listed below to make sure that your code is in line with the Power BI certification policies.</span></span>  

<span data-ttu-id="29ee4-162">**ที่จำเป็น**</span><span class="sxs-lookup"><span data-stu-id="29ee4-162">**Required**</span></span>
* <span data-ttu-id="29ee4-163">มีเพียงการใช้องค์ประกอบ OSS ที่ตรวจสอบแล้วเท่านั้น เช่น Javascript หรือไลบราลี่ TypeScript</span><span class="sxs-lookup"><span data-stu-id="29ee4-163">Only use public reviewable OSS components such as public JavaScript or TypeScript libraries.</span></span>
* <span data-ttu-id="29ee4-164">โค้ดต้องสนับสนุน [การเรนเดอร์อีเวนท์ API](event-service.md)</span><span class="sxs-lookup"><span data-stu-id="29ee4-164">The code must support the [Rendering Events API](event-service.md).</span></span>
* <span data-ttu-id="29ee4-165">ตรวจสอบให้แน่ใจว่า DOM ได้รับการจัดการอย่างปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="29ee4-165">Ensure DOM is manipulated safely.</span></span> <span data-ttu-id="29ee4-166">ใช้สุขอนามัยสำหรับการข้อมูลที่ป้อนเข้าหรือข้อมูลของผู้ใช้ก่อนที่จะเพิ่มลงใน DOM</span><span class="sxs-lookup"><span data-stu-id="29ee4-166">Use sanitization for user input or user data, before adding it to DOM.</span></span>
* <span data-ttu-id="29ee4-167">สามารถใช้ [รายงานตัวอย่าง](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/gh-pages/assets) นี้เป็นตัวทดสอบชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="29ee4-167">Use the [sample report](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/gh-pages/assets) as a test dataset.</span></span>

<span data-ttu-id="29ee4-168">**ไม่ได้รับอนุญาต**</span><span class="sxs-lookup"><span data-stu-id="29ee4-168">**Not allowed**</span></span>
* <span data-ttu-id="29ee4-169">การเข้าถึงบริการหรือแหล่งข้อมูลภายนอก</span><span class="sxs-lookup"><span data-stu-id="29ee4-169">Accessing external services or resources.</span></span> <span data-ttu-id="29ee4-170">ยกตัวอย่างเช่น ไม่มีการใช้ HTTP/S หรือ WebSocket ที่สามารถออกไปจาก Power BI เพื่อไปยังบริการอื่นได้</span><span class="sxs-lookup"><span data-stu-id="29ee4-170">For example, no HTTP/S or WebSocket requests can go out of Power BI to any services.</span></span>
* <span data-ttu-id="29ee4-171">ใช้ `innerHTML`หรือ `D3.html(user data or user input)`</span><span class="sxs-lookup"><span data-stu-id="29ee4-171">Using `innerHTML`, or `D3.html(user data or user input)`.</span></span>
* <span data-ttu-id="29ee4-172">ข้อผิดพลาด JavaScript หรือข้อยกเว้นในคอนโซลของเบราว์เซอร์สำหรับข้อมูลที่ป้อนเข้าใดๆ</span><span class="sxs-lookup"><span data-stu-id="29ee4-172">JavaScript errors or exceptions in the browser console, for any input data.</span></span>
* <span data-ttu-id="29ee4-173">รหัสที่กำหนดเองหรือแบบไดนามิก เช่น `eval()`การใช้ที่ไม่ปลอดภัยของ `settimeout()` `requestAnimationFrame()` `setinterval(user input function)`และข้อมูลที่ป้อนเข้าหรือข้อมูลของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="29ee4-173">Arbitrary or dynamic code such as `eval()`, unsafe use of `settimeout()`, `requestAnimationFrame()`, `setinterval(user input function)`, and user input or user data.</span></span>
* <span data-ttu-id="29ee4-174">ทำให้ JavaScript files หรือโครงการเล็กลง</span><span class="sxs-lookup"><span data-stu-id="29ee4-174">Minified JavaScript files or projects.</span></span>

## <a name="submitting-a-power-bi-visual-for-certification"></a><span data-ttu-id="29ee4-175">การยื่นใบรับรองวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="29ee4-175">Submitting a Power BI visual for certification</span></span>

<span data-ttu-id="29ee4-176">คุณสามารถยื่นคำร้องเพื่อให้มีการรับรองวิชวล Power BI โดยทีม Power BI ผ่าน Partner Center</span><span class="sxs-lookup"><span data-stu-id="29ee4-176">You can request to have your Power BI visual certified by the Power BI team via Partner Center.</span></span>

>[!TIP]
><span data-ttu-id="29ee4-177">กระบวนการขอใบรับรองThe Power BI อาจใช้เวลาสักระยะ</span><span class="sxs-lookup"><span data-stu-id="29ee4-177">The Power BI certification process might take time.</span></span> <span data-ttu-id="29ee4-178">หากคุณกำลังสร้างวิชวล Power BI ใหม่ เราแนะนำให้คุณเผยแพร่วิชวล Power BI ผ่าน Partner Center ก่อนที่คุณจะขอใบรับรอง Power BI</span><span class="sxs-lookup"><span data-stu-id="29ee4-178">If you're creating a new Power BI visual, we recommend that you publish your Power BI visual via the Partner Center before you request Power BI certification.</span></span> <span data-ttu-id="29ee4-179">กระบวนการนี้เพื่อให้แน่ใจว่าการเผยแพร่วิชวลของคุณจะไม่ถูกเลื่อนออกไป</span><span class="sxs-lookup"><span data-stu-id="29ee4-179">This ensures that the publishing of your visual is not delayed.</span></span>

<span data-ttu-id="29ee4-180">การยื่นคำร้องขอการรับรอง Power BI:</span><span class="sxs-lookup"><span data-stu-id="29ee4-180">To request Power BI certification:</span></span>

1. <span data-ttu-id="29ee4-181">ลงชื่อเข้าใช้ใน Partner Center</span><span class="sxs-lookup"><span data-stu-id="29ee4-181">Sign in to Partner Center.</span></span>
2. <span data-ttu-id="29ee4-182">ตรงบริเวณ **หน้าเพจภาพรวม**, ให้เลือกวิชวล Power BI ของคุณและไปยังหน้าตั้งค่า **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="29ee4-182">On the **Overview page**, choose your Power BI visual, and go to the **Product** setup page.</span></span>
3. <span data-ttu-id="29ee4-183">เลือกทำเครื่องหมายในกล่องกาเครื่องหมาย **ยื่นคำร้องขอใบรับรอง Power BI**</span><span class="sxs-lookup"><span data-stu-id="29ee4-183">Select the **Request Power BI certification** check box.</span></span>
4. <span data-ttu-id="29ee4-184">ในหน้า **ตรวจสอบและเผยแพร่** ที่อยู่ในกล่องข้อความ **หมายเหตุสำหรับการขอใบรับรอง** ให้ระบุลิงก์ที่จะนำไปสู่โค้ดต้นทาง และต้องใช้ข้อมูลประจำตัวเพื่อเข้าสู่ลิงก์</span><span class="sxs-lookup"><span data-stu-id="29ee4-184">On the **Review and publish** page, in the **Notes for certification** text box, provide a link to the source code and the credentials required to access it.</span></span>

### <a name="private-repository-submission-process"></a><span data-ttu-id="29ee4-185">กระบวนการส่งที่เก็บแบบส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="29ee4-185">Private repository submission process</span></span>

<span data-ttu-id="29ee4-186">หากคุณกำลังใช้ที่เก็บส่วนตัวเช่น GitHub เพื่อส่งการแสดงผลด้วยภาพของ Power BI สำหรับใบรับรอง ให้ทำตามคำแนะนำในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="29ee4-186">If you're using a private repository such as GitHub to submit your Power BI visual for certification, follow the instructions in this section.</span></span>
1. <span data-ttu-id="29ee4-187">สร้างบัญชีใหม่สำหรับทีมการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="29ee4-187">Create a new account for the validation team.</span></span>
2. <span data-ttu-id="29ee4-188">กำหนดค่า[การรับรองความถูกต้องแบบสองปัจจัย](https://help.github.com/github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa)สำหรับบัญชีของคุณ</span><span class="sxs-lookup"><span data-stu-id="29ee4-188">Configure [two-factor authentication](https://help.github.com/github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa) for your account.</span></span>
3. <span data-ttu-id="29ee4-189">[สร้างชุดรหัสการกู้คืนใหม่](https://help.github.com/github/authenticating-to-github/configuring-two-factor-authentication-recovery-methods#generating-a-new-set-of-recovery-codes)</span><span class="sxs-lookup"><span data-stu-id="29ee4-189">[Generate a new set of recovery codes](https://help.github.com/github/authenticating-to-github/configuring-two-factor-authentication-recovery-methods#generating-a-new-set-of-recovery-codes).</span></span>
4. <span data-ttu-id="29ee4-190">เมื่อส่งการแสดงผลด้วยภาพของ Power BI ของคุณ ให้ป้อนข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="29ee4-190">When submitting your Power BI visual, provide the following:</span></span>
    * <span data-ttu-id="29ee4-191">ลิงก์ไปยังที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="29ee4-191">A link to the repository</span></span>
    * <span data-ttu-id="29ee4-192">ข้อมูลประจำตัวสำหรับเข้าสู่ระบบ (รวมถึงรหัสผ่าน)</span><span class="sxs-lookup"><span data-stu-id="29ee4-192">Login credentials (including a password)</span></span>
    * <span data-ttu-id="29ee4-193">รหัสการกู้คืน</span><span class="sxs-lookup"><span data-stu-id="29ee4-193">Recovery codes</span></span>
    * <span data-ttu-id="29ee4-194">สิทธิ์แบบอ่านเท่านั้นไปยังบัญชีของเรา ([pbicvsupport](https://github.com/pbicvsupport))</span><span class="sxs-lookup"><span data-stu-id="29ee4-194">Read-only permissions to our account ([pbicvsupport](https://github.com/pbicvsupport))</span></span>

## <a name="certified-power-bi-visual-badges"></a><span data-ttu-id="29ee4-195">ป้ายแสดงผลด้วยภาพ Power BI ที่ผ่านการรับรอง</span><span class="sxs-lookup"><span data-stu-id="29ee4-195">Certified Power BI visual badges</span></span>

<span data-ttu-id="29ee4-196">เมื่อการแสดงผลด้วยภาพของ Power BI ได้รับการรับรองแล้วจะได้รับป้ายที่กำหนดซึ่งระบุว่าได้การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="29ee4-196">Once a Power BI visual is certified, it gets a designated badge that indicates that it's certified.</span></span>

### <a name="certified-power-bi-visuals-in-appsource"></a><span data-ttu-id="29ee4-197">Power BI ที่ผ่านการรับรองใน AppSource</span><span class="sxs-lookup"><span data-stu-id="29ee4-197">Certified Power BI visuals in AppSource</span></span>

* <span data-ttu-id="29ee4-198">เมื่อค้นหาออนไลน์สำหรับ[การแสดงผลด้วยภาพของ Power BI ใน AppSource](https://appsource.microsoft.com/marketplace/apps?product=power-bi-visuals) ป้ายสีเหลืองขนาดเล็กบนการ์ดของภาพแสดงให้เห็นว่าเป็นภาพ Power BI ที่ได้รับการรับรอง</span><span class="sxs-lookup"><span data-stu-id="29ee4-198">When searching online for [Power BI visuals in AppSource](https://appsource.microsoft.com/marketplace/apps?product=power-bi-visuals), a small yellow badge on the visual's card indicates that it's a certified Power BI visual.</span></span>

    ![การแสดงผลด้วยภาพของ Power BI ที่ผ่านการรับรองใน AppSource](media/power-bi-custom-visuals-certified/certified-visual-yellow-small.png)

* <span data-ttu-id="29ee4-200">หลังจากคลิกการ์ดการแสดงผลด้วยภาพของ Power BI  ใน AppSource ป้ายสีเหลืองชื่อ *ได้รับการรับรองจาก PBI* จะแสดงว่าการแสดงผลด้วยภาพของ Power BI นี้ได้รับการรับรอง</span><span class="sxs-lookup"><span data-stu-id="29ee4-200">After clicking the Power BI visual card in AppSource, a yellow badge titled *PBI Certified* indicates that this Power BI visual is certified.</span></span>

    ![การแสดงผลด้วยภาพของ Power BI ที่ผ่านการรับรองในหน้าแอป](media/power-bi-custom-visuals-certified/certified-visual-yellow-big.png)

### <a name="certified-power-bi-visuals-in-the-power-bi-interface"></a><span data-ttu-id="29ee4-202">การแสดงผลด้วยภาพของ Power BI ที่ผ่านการรับรองในส่วนติดต่อ Power BI</span><span class="sxs-lookup"><span data-stu-id="29ee4-202">Certified Power BI visuals in the Power BI interface</span></span>

* <span data-ttu-id="29ee4-203">เมื่อนำการแสดงผลด้วยภาพของ Power BI จากภายใน Power BI (Desktop หรือบริการ) ป้ายชื่อสีน้ำเงินจะแสดงว่าการแสดงผลด้วยภาพของ Power BI นี้ได้รับการรับรอง</span><span class="sxs-lookup"><span data-stu-id="29ee4-203">When importing a Power BI visual from within Power BI (Desktop or service), a blue badge indicates that the Power BI visual is certified.</span></span>

    ![ส่วนติดต่อ Power BI การแสดงผลด้วยภาพของ Power BI ที่ผ่านการรับรอง](media/power-bi-custom-visuals-certified/certified-visual-blue.png)

* <span data-ttu-id="29ee4-205">คุณสามารถแสดงการแสดงผลด้วยภาพของ Power BI ที่ได้รับการรับรองได้โดยการเลือกตัวเลือกตัวกรอง *Power BI ที่ได้รับการรับรอง*</span><span class="sxs-lookup"><span data-stu-id="29ee4-205">You can display only certified Power BI visuals, by selecting the *Power BI Certified* filter option.</span></span>

## <a name="publication-timeline"></a><span data-ttu-id="29ee4-206">ไทม์ไลน์การเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="29ee4-206">Publication timeline</span></span>

<span data-ttu-id="29ee4-207">การปรับใช้ใน AppSource คือกระบวนการที่อาจต้องใช้เวลาสักครู่</span><span class="sxs-lookup"><span data-stu-id="29ee4-207">Deploying to AppSource is a process that may take some time.</span></span> <span data-ttu-id="29ee4-208">วิชวล Power BI พร้อมที่จะดาวน์โหลดจาก AppSource ได้เมื่อกระบวนการนี้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="29ee4-208">Your Power BI visual will be available to download from AppSource when this process is complete.</span></span>

### <a name="when-will-users-be-able-to-download-my-visual"></a><span data-ttu-id="29ee4-209">ผู้ใช้จะสามารถดาวน์โหลดวิชวลของฉันได้เมื่อใด</span><span class="sxs-lookup"><span data-stu-id="29ee4-209">When will users be able to download my visual?</span></span>

* <span data-ttu-id="29ee4-210">หากคุณส่งวิชวล Power BI เป็นครั้งแรก ผู้ใช้จะสามารถดาวน์โหลดวิชวลได้ภายในสองถึงสามชั่วโมงหลังจากที่คุณได้รับอีเมลจาก AppSource</span><span class="sxs-lookup"><span data-stu-id="29ee4-210">If you submitted a Power BI visual for the first time, users will be able to download it a few hours after you receive an email from AppSource.</span></span>

* <span data-ttu-id="29ee4-211">หากคุณส่งการอัปเดตไปยังวิชวล Power BI ที่มีอยู่ ผู้ใช้จะสามารถดาวน์โหลดวิชวลได้ภายในหนึ่งเดือนหลังจากการส่งของคุณ</span><span class="sxs-lookup"><span data-stu-id="29ee4-211">If you submitted an update to an existing Power BI visual, users will be able to download it within a month of your submission.</span></span>

    >[!NOTE]
    > <span data-ttu-id="29ee4-212">เขตข้อมูล *เวอร์ชัน* ใน AppSource จะอัปเดตในวันที่ Power BI ของคุณได้รับการอนุมัติโดย AppSource ประมาณหนึ่งสัปดาห์หลังจากที่คุณส่งวิชวลของคุณ</span><span class="sxs-lookup"><span data-stu-id="29ee4-212">The *version* field in AppSource will be updated with the day your Power BI was approved by AppSource, approximately a week after you submitted your visual.</span></span> <span data-ttu-id="29ee4-213">ผู้ใช้จะสามารถดาวน์โหลดวิชวลที่อัปเดตแล้วได้ แต่ความสามารถที่อัปเดตแล้วจะไม่มีผล</span><span class="sxs-lookup"><span data-stu-id="29ee4-213">Users will be able to download the updated visual but the updated capabilities will not take effect.</span></span> <span data-ttu-id="29ee4-214">ความสามารถใหม่ของวิชวลของคุณจะส่งผลกระทบต่อรายงานของผู้ใช้หลังจากผ่านไปประมาณหนึ่งเดือน</span><span class="sxs-lookup"><span data-stu-id="29ee4-214">Your visual's new capabilities will affect the user's reports after about a month.</span></span> 

### <a name="when-will-my-power-bi-visual-display-a-certification-badge"></a><span data-ttu-id="29ee4-215">วิชวล Power BI ของฉันจะแสดงตัวบอกสถานะใบรับรองเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="29ee4-215">When will my Power BI visual display a certification badge?</span></span>

* <span data-ttu-id="29ee4-216">หากคุณส่งวิชวล Power BI เป็นครั้งแรก ตัวบอกสถานะใบรับรองจะปรากฏขึ้นภายในหนึ่งวันหลังจากได้รับอีเมลการอนุมัติจาก AppSource</span><span class="sxs-lookup"><span data-stu-id="29ee4-216">If you submitted a Power BI visual for the first time, the certification badge will appear within a day of receiving the approval email from AppSource.</span></span>

* <span data-ttu-id="29ee4-217">หากคุณกำลังร้องขอการรับรองสำหรับวิชวล Power BI ที่มีอยู่ คุณจะเห็นตัวบอกสถานะใบรับรองได้ภายในหนึ่งเดือนหลังจากการส่งของคุณ</span><span class="sxs-lookup"><span data-stu-id="29ee4-217">If you're requesting certification for an existing Power BI visual, the certification badge will be visible within a month of your submission.</span></span>

## <a name="next-steps"></a><span data-ttu-id="29ee4-218">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="29ee4-218">Next steps</span></span>

* <span data-ttu-id="29ee4-219">หากคุณเป็นนักพัฒนาเว็บที่สนใจในการสร้างวิชวล Power BI ของคุณเองและต้องการเพิ่มงานของคุณไปยัง [Microsoft AppSource](https://appsource.microsoft.com) คุณสามารถเริ่มต้นใช้งานได้ในบทช่วยสอน  [การพัฒนาวิชวลการ์ดวงกลม a Power BI ](develop-circle-card.md)</span><span class="sxs-lookup"><span data-stu-id="29ee4-219">If you're a web developer interested in creating your own Power BI visuals and adding them to the [Microsoft AppSource](https://appsource.microsoft.com), start with the [Developing a Power BI circle card visual](develop-circle-card.md) tutorial.</span></span>

* <span data-ttu-id="29ee4-220">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแสดงผลด้วยภาพ ให้ดูที่[คำถามที่ถามบ่อยเกี่ยวกับการแสดงผลด้วยภาพที่ได้รับรองแล้ว](power-bi-custom-visuals-faq.md#certified-power-bi-visuals)</span><span class="sxs-lookup"><span data-stu-id="29ee4-220">For more information about visuals, see [Frequently asked questions about certified visuals](power-bi-custom-visuals-faq.md#certified-power-bi-visuals).</span></span>

* [<span data-ttu-id="29ee4-221">รายการเพลย์ลิสต์ วิชวล Power BI ของ Microsoft บน YouTube</span><span class="sxs-lookup"><span data-stu-id="29ee4-221">Microsoft's Power BI visual playlist on YouTube</span></span>](https://www.youtube.com/playlist?list=PL1N57mwBHtN1vIjfvuBIzZllrmKo-Vz6x)

* [<span data-ttu-id="29ee4-222">วิชวลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="29ee4-222">Visuals in Power BI</span></span>](power-bi-custom-visuals.md)

* [<span data-ttu-id="29ee4-223">การเผยแพร่ส่วนการจัดแสดง Power BI ไปยัง Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="29ee4-223">Publish Power BI visuals to Microsoft AppSource</span></span>](office-store.md)

* <span data-ttu-id="29ee4-224">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="29ee4-224">More questions?</span></span> [<span data-ttu-id="29ee4-225">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="29ee4-225">Try the Power BI Community</span></span>](https://community.powerbi.com/)
