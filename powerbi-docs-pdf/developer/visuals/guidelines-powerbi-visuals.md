---
title: แนวทางสำหรับวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: เรียนรู้วิธีที่คุณสามารถเผยแพร่วิชวลแบบกำหนดเองของคุณไปยัง Microsoft AppSource เพื่อให้บุคคลอื่นสามารถค้นหาและใช้งานผ่านการซื้อได้ เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.date: 08/12/2020
ms.openlocfilehash: adb238b918d01bcdefe247a5452a0432b97d2e0c
ms.sourcegitcommit: a5e98bc86915f7bea6a0ab5df282683840e63d2c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/07/2021
ms.locfileid: "97969523"
---
# <a name="guidelines-for-power-bi-visuals"></a><span data-ttu-id="47cd6-104">คำแนะนำสำหรับการแสดงภาพ Power BI</span><span class="sxs-lookup"><span data-stu-id="47cd6-104">Guidelines for Power BI visuals</span></span>
<span data-ttu-id="47cd6-105">ก่อนที่คุณจะ[เผยแพร่](office-store.md)วิชวล Power BI ของคุณไปยัง Microsoft AppSource เพื่อให้ผู้อื่นสามารถค้นหาและใช้งานได้ ต้องตรวจสอบให้แน่ใจว่าคุณได้ทำตามคำแนะนำเพื่อสร้างประสบการณ์ที่ยอดเยี่ยมสำหรับผู้ใช้ของคุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="47cd6-105">Before you [publish](office-store.md) your Power BI visual to Microsoft AppSource for others to discover and use, make sure that you follow the guidelines to create a great experience for your users.</span></span>

## <a name="power-bi-visuals-with-additional-purchases"></a><span data-ttu-id="47cd6-106">วิชวล Power BI ที่มีการซื้อเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="47cd6-106">Power BI visuals with additional purchases</span></span>

<span data-ttu-id="47cd6-107">คุณสามารถส่งวิชวล Power BI ที่ไม่มีค่าใช้จ่ายไปยัง Marketplace (Microsoft AppSource) ได้</span><span class="sxs-lookup"><span data-stu-id="47cd6-107">You can submit Power BI visuals that are free to the Marketplace (Microsoft AppSource).</span></span> <span data-ttu-id="47cd6-108">นอกจากนี้คุณยังสามารถส่งวิชวล Power BI ของ Microsoft AppSource ที่มีแท็กราคาเขียนว่า "อาจจำเป็นที่ต้องซื้อเพิ่ม" ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="47cd6-108">You can also submit to Microsoft AppSource Power BI visuals that have an "additional purchase may be required" price tag.</span></span> <span data-ttu-id="47cd6-109">วิชวล Power BI ที่มีแท็กราคา "อาจจำเป็นที่ต้องซื้อเพิ่ม" มีลักษณะคล้ายกับ Add-in ที่ซื้อเพิ่มภายในแอป (IAP) ในร้านค้าสำนักงาน</span><span class="sxs-lookup"><span data-stu-id="47cd6-109">"Additional purchase may be required" Power BI visuals, are similar to in-app purchase (IAP) add-ins in the Office Store.</span></span> 

<span data-ttu-id="47cd6-110">เช่นเดียวกับวิชวล Power BI แบบฟรี ซึ่งยังสามารถรับรองวิชวล IAP Power BI ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="47cd6-110">Similarly to a free Power BI visual, an IAP Power BI visual can also be certified.</span></span> <span data-ttu-id="47cd6-111">ก่อนที่จะส่งวิชวล IAP Power BI ของคุณ กรุณาตรวจสอบให้แน่ใจว่าวิชวลเป็นไปตาม [ข้อกำหนดการรับรอง](power-bi-custom-visuals-certified.md) หรือไม่</span><span class="sxs-lookup"><span data-stu-id="47cd6-111">Before submitting your IAP Power BI visual for certification, make sure it complies with the [certification requirements](power-bi-custom-visuals-certified.md).</span></span>

### <a name="what-is-a-power-bi-visual-with-iap-features"></a><span data-ttu-id="47cd6-112">วิชวล Power BI ที่มีคุณลักษณะ IAP คืออะไร?</span><span class="sxs-lookup"><span data-stu-id="47cd6-112">What is a Power BI visual with IAP features?</span></span>

<span data-ttu-id="47cd6-113">วิชวล IAP Power BI เป็นวิชวลแบบ *ฟรี* ที่ให้บริการ *คุณลักษณะแบบฟรี*</span><span class="sxs-lookup"><span data-stu-id="47cd6-113">An IAP Power BI visual is a *free* visual that offers *free features*.</span></span> <span data-ttu-id="47cd6-114">นอกจากนี้ยังมีคุณลักษณะขั้นสูงบางอย่างที่อาจมีค่าธรรมเนียมเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="47cd6-114">It also has some advanced features for which extra charges may be applied.</span></span> <span data-ttu-id="47cd6-115">ในการอธิบายวิชวล Power BI นักพัฒนาต้องแจ้งผู้ใช้ถึงคำอธิบายของวิชวลเกี่ยวกับคุณลักษณะที่ต้องซื้อเพิ่มเติมเพื่อใช้งาน</span><span class="sxs-lookup"><span data-stu-id="47cd6-115">In the Power BI visual's description, developers must notify users about the features that require additional purchases to operate.</span></span> <span data-ttu-id="47cd6-116">ปัจจุบัน Microsoft ไม่ได้มี APIs แบบเนทีฟเพื่อสนับสนุนการซื้อเพิ่มภายของแอปและ Add-ins</span><span class="sxs-lookup"><span data-stu-id="47cd6-116">Currently, Microsoft does not provide native APIs to support the purchase of apps and add-ins.</span></span>

<span data-ttu-id="47cd6-117">นักพัฒนาอาจใช้ระบบการชำระเงินอื่นสำหรับการซื้อเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="47cd6-117">Developers may use any third-party payment system for these purchases.</span></span> <span data-ttu-id="47cd6-118">สำหรับข้อมูลเพิ่มเติม ให้ดูที่[นโยบายร้านค้าของเรา](/legal/marketplace/certification-policies#11002-displaying-ads)</span><span class="sxs-lookup"><span data-stu-id="47cd6-118">For more information, see [our store policy](/legal/marketplace/certification-policies#11002-displaying-ads).</span></span>


>[!IMPORTANT]  
> <span data-ttu-id="47cd6-119">หากคุณอัปเดตวิชวล Power BI ของคุณจากฟรีเป็น "อาจจำเป็นต้องซื้อเพิ่มเติม" ผู้ใช้จะต้องได้รับฟังก์ชันการใช้งานฟรีในระดับเดียวกับก่อนการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="47cd6-119">If you update your Power BI visual from free to "Additional purchase may be required", users must receive the same level of free functionality  as before the update.</span></span> <span data-ttu-id="47cd6-120">คุณอาจเพิ่มคุณลักษณะขั้นสูงแบบชำระเงินนอกเหนือจากคุณลักษณะฟรีแบบเก่าที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="47cd6-120">You may add optional advanced paid features in addition to the existing free features.</span></span>

### <a name="watermarks"></a><span data-ttu-id="47cd6-121">ลายน้ำ</span><span class="sxs-lookup"><span data-stu-id="47cd6-121">Watermarks</span></span>

<span data-ttu-id="47cd6-122">คุณสามารถใช้ลายน้ำเพื่อให้ลูกค้าใช้คุณสมบัติขั้นสูงของ IAP ต่อไปโดยไม่ต้องจ่ายเงินได้</span><span class="sxs-lookup"><span data-stu-id="47cd6-122">You can use watermarks so that customers continue using the IAP advanced features without paying.</span></span> 

<span data-ttu-id="47cd6-123">คุณสามารถใช้ลายน้ำเพื่อแสดงฟังก์ชันการทำงานของวิชวล Power BI เต็มรูปแบบก่อนทำการซื้อได้</span><span class="sxs-lookup"><span data-stu-id="47cd6-123">Watermarks can be used to showcase the full functionality of the Power BI visual, before a purchase is made.</span></span> 

* <span data-ttu-id="47cd6-124">ลายน้ำสามารถใช้ได้เฉพาะกับคุณลักษณะที่ต้องชำระซึ่งใช้โดยไม่ต้องมีใบอนุญาตที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="47cd6-124">Watermarks may only be used on paid features that are used without a valid license.</span></span>
* <span data-ttu-id="47cd6-125">ไม่อนุญาตให้ใช้ลายน้ำในวิชวล Power BI ที่มีแท็กราคา *ฟรี*</span><span class="sxs-lookup"><span data-stu-id="47cd6-125">Watermarks are not allowed in Power BI visuals with a *free* price tag.</span></span>
* <span data-ttu-id="47cd6-126">ไม่อนุญาตให้ใช้ลายน้ำในวิชวล IAP เมื่อผู้ใช้ใช้คุณลักษณะฟรี</span><span class="sxs-lookup"><span data-stu-id="47cd6-126">Watermarks are not allowed in IAP visuals, when the user uses free features.</span></span> 

### <a name="pop-up-window"></a><span data-ttu-id="47cd6-127">หน้าต่างป็อปอัพ</span><span class="sxs-lookup"><span data-stu-id="47cd6-127">Pop-up window</span></span>

<span data-ttu-id="47cd6-128">คุณสามารถใช้หน้าต่างป็อปอัพเพื่ออธิบายวิธีการซื้อสิทธิ์การใช้งานเมื่อมีการใช้ใบอนุญาตที่ไม่ถูกต้อง (หรือหมดอายุ) ด้วยวิชวล Power BI IAP ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="47cd6-128">You can use a pop-up window to explain how to purchase a license, when an invalid (or expired) license is used with your Power BI IAP visual.</span></span>

### <a name="submission-process"></a><span data-ttu-id="47cd6-129">กระบวนการส่ง</span><span class="sxs-lookup"><span data-stu-id="47cd6-129">Submission process</span></span>

<span data-ttu-id="47cd6-130">ทำตาม [กระบวนการส่งคำร้อง](office-store.md#submitting-to-appsource) และระบบจะพาไปยังแท็บ *การตั้งค่าผลิตภัณฑ์* และตรวจสอบกล่องกาเครื่องหมาย *ผลิตภัณฑ์ของฉันที่ต้องการบริการซื้อ*</span><span class="sxs-lookup"><span data-stu-id="47cd6-130">Follow the [submission process](office-store.md#submitting-to-appsource) and then navigate to the *Product setup* tab and check the *My product requires the purchase of a service* check box.</span></span>

<span data-ttu-id="47cd6-131">หลังจากตรวจสอบและอนุมัติวิชวล Power BI แล้ว การลงรายการ Microsoft AppSource สำหรับวิชวล IAP Power BI จะระบุว่า 'อาจจำเป็นต้องซื้อเพิ่ม' ภายใต้ตัวเลือกการกำหนดราคา</span><span class="sxs-lookup"><span data-stu-id="47cd6-131">After the Power BI visual is validated and approved, the Microsoft AppSource listing for the IAP Power BI visual states, "Additional purchase may be required" under the pricing options.</span></span>

## <a name="context-menu"></a><span data-ttu-id="47cd6-132">เมนูบริบท</span><span class="sxs-lookup"><span data-stu-id="47cd6-132">Context menu</span></span>
<span data-ttu-id="47cd6-133">เมนูบริบทคือเมนูคลิกขวาที่จะแสดงขึ้นเมื่อผู้ใช้วางเมาส์เหนือการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="47cd6-133">Context menu is the right-click menu that is displayed when the user is hovering over a visual.</span></span>
<span data-ttu-id="47cd6-134">การแสดงผลด้วยภาพของ Power BI ทั้งหมดควรเปิดใช้งานเมนูบริบทเพื่อนำเสนอประสบการณ์แบบครบวงจร</span><span class="sxs-lookup"><span data-stu-id="47cd6-134">All Power BI visuals should enable the context menu to bring a unified experience.</span></span>
<span data-ttu-id="47cd6-135">โปรดตรวจสอบ[บทความ](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/gh-pages/tutorials/building-bar-chart)นี้เพื่อเรียนรู้วิธีการเพิ่มเมนูบริบท</span><span class="sxs-lookup"><span data-stu-id="47cd6-135">Please check [this article](https://github.com/PowerBi-Projects/PowerBI-visuals/tree/gh-pages/tutorials/building-bar-chart) to learn how to add a context menu.</span></span>

>[!div class="mx-imgBorder"]
><span data-ttu-id="47cd6-136">![ภาพหน้าจอของเมนูบริบทการแสดงภาพของ Power BI](media/guidelines-powerbi-visuals/context-menu.png)</span><span class="sxs-lookup"><span data-stu-id="47cd6-136">![A screenshot of a Power BI visual context menu.](media/guidelines-powerbi-visuals/context-menu.png)</span></span>

## <a name="commercial-logo"></a><span data-ttu-id="47cd6-137">โลโก้เชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="47cd6-137">Commercial logo</span></span>
<span data-ttu-id="47cd6-138">ส่วนนี้จะอธิบายข้อกำหนดสำหรับการเพิ่มโลโก้เชิงพาณิชย์ในวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="47cd6-138">This section describes the specifications for adding commercial logos in Power BI visuals.</span></span> <span data-ttu-id="47cd6-139">โลโก้เชิงพาณิชย์ไม่ได้เป็นแบบบังคับ</span><span class="sxs-lookup"><span data-stu-id="47cd6-139">Commercial logos are not mandatory.</span></span> <span data-ttu-id="47cd6-140">ถ้าเพิ่ม จะต้องเป็นไปตามคำแนะนำเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="47cd6-140">If added they must follow these guidelines.</span></span>

> [!NOTE]
> * <span data-ttu-id="47cd6-141">ในบทความนี้ 'โลโก้เชิงพาณิชย์' หมายถึงไอคอนของบริษัทเชิงพาณิชย์ใด ๆ ตามที่อธิบายไว้ในภาพด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="47cd6-141">In this article, 'commercial logo' refers to any commercial company icon as described in the pictures below.</span></span>
> * <span data-ttu-id="47cd6-142">โลโก้เชิงพาณิชย์ของ Microsoft ที่ใช้ในบทความนี้เป็นเพียงตัวอย่างเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="47cd6-142">The Microsoft commercial logo is used in this article only as an example.</span></span> <span data-ttu-id="47cd6-143">ใช้โลโก้เชิงพาณิชย์ของคุณเองกับวิชวล Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="47cd6-143">Use your own commercial logo with your Power BI visual.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="47cd6-144">โลโก้เชิงพาณิชย์สามารถใช้ได้ *เฉพาะในโหมดแก้ไขเท่านั้น*</span><span class="sxs-lookup"><span data-stu-id="47cd6-144">Commercial logos are allowed in *edit mode only*.</span></span> <span data-ttu-id="47cd6-145">โลโก้เชิงพาณิชย์ *ไม่สามารถ* แสดงในโหมดมุมมองได้</span><span class="sxs-lookup"><span data-stu-id="47cd6-145">Commercial logos *can't* be displayed in view mode.</span></span>

### <a name="commercial-logo-type"></a><span data-ttu-id="47cd6-146">ประเภทของโลโก้เชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="47cd6-146">Commercial logo type</span></span>

<span data-ttu-id="47cd6-147">มีโลโก้เชิงพาณิชย์สามประเภท:</span><span class="sxs-lookup"><span data-stu-id="47cd6-147">There are three types of commercial logos:</span></span>
* <span data-ttu-id="47cd6-148">**โลโก้** - โลโก้มีองค์ประกอบสองอย่างที่ติดแน่นอยู่ด้วยกัน คือ ไอคอนและชื่อ</span><span class="sxs-lookup"><span data-stu-id="47cd6-148">**Logo** - A logo is comprised of two elements locked together, an icon and a name.</span></span>

    ![ภาพหน้าจอของโลโก้ Microsoft](media/guidelines-powerbi-visuals/microsoft-logo.png)

* <span data-ttu-id="47cd6-150">**สัญลักษณ์** - กราฟิกที่ไม่มีข้อความ</span><span class="sxs-lookup"><span data-stu-id="47cd6-150">**Symbol** - A graphic without any text.</span></span>

    ![ภาพหน้าจอของเครื่องมือ Microsoft](media/guidelines-powerbi-visuals/microsoft-symbol.png)

* <span data-ttu-id="47cd6-152">**คำโลโก้** - โลโก้ที่ไม่มีไอคอน แต่ประกอบด้วยข้อความเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="47cd6-152">**Logotype** - A logo without an icon, comprised only from text.</span></span>

    ![ภาพหน้าจอของโลโก้ Microsoft แบบไม่มีไอคอน](media/guidelines-powerbi-visuals/microsoft-logotype.png)

### <a name="commercial-logo-color"></a><span data-ttu-id="47cd6-154">สีของโลโก้เชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="47cd6-154">Commercial logo color</span></span>

<span data-ttu-id="47cd6-155">เมื่อใช้โลโก้เชิงพาณิชย์ สีของโลโก้จะต้องเป็นสีเทา (hex color #C8C8C8)</span><span class="sxs-lookup"><span data-stu-id="47cd6-155">When using a commercial logo, the color of the logo must be grey (hex color #C8C8C8).</span></span> <span data-ttu-id="47cd6-156">อย่าเพิ่มเอฟเฟกต์ เช่น การไล่ระดับสี แก่โลโก้เชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="47cd6-156">Don't add effects such as gradients to the commercial logo.</span></span>

* <span data-ttu-id="47cd6-157">**โลโก้**</span><span class="sxs-lookup"><span data-stu-id="47cd6-157">**Logo**</span></span>

    ![ภาพหน้าจอของโลโก้ Microsoft ในสีเทา](media/guidelines-powerbi-visuals/grey-microsoft-logo.png)

* <span data-ttu-id="47cd6-159">**สัญลักษณ์** - กราฟิกที่ไม่มีข้อความ</span><span class="sxs-lookup"><span data-stu-id="47cd6-159">**Symbol** - A graphic without any text.</span></span>

    ![ภาพหน้าจอของเครื่องหมาย Microsoft ในสีเทา](media/guidelines-powerbi-visuals/grey-microsoft-symbol.png)

* <span data-ttu-id="47cd6-161">**คำโลโก้** - โลโก้ที่ไม่มีไอคอน แต่ประกอบด้วยข้อความเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="47cd6-161">**Logotype** - A logo without an icon, comprised only from text.</span></span>

    ![ภาพหน้าจอของโลโก้ Microsoft แบบไม่มีไอคอน ในสีเทา](media/guidelines-powerbi-visuals/grey-microsoft-logotype.png)

> [!TIP]
> * <span data-ttu-id="47cd6-163">หากวิชวล Power BI ของคุณมีกราฟิก ให้พิจารณาเพิ่มพื้นหลังสีขาวที่มีระยะขอบ 10 px ให้กับโลโก้ของคุณ</span><span class="sxs-lookup"><span data-stu-id="47cd6-163">If your Power BI visual contains a graphic, consider adding a white background with 10 px margins to your logo.</span></span>
> * <span data-ttu-id="47cd6-164">พิจารณาเพิ่ม dropshadow ลงในโลโก้ของคุณ (ความทึบของสีดำ 30%)</span><span class="sxs-lookup"><span data-stu-id="47cd6-164">Consider adding dropshadow to your logo (30% opacity black).</span></span>

### <a name="commercial-logo-size"></a><span data-ttu-id="47cd6-165">ขนาดของโลโก้เชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="47cd6-165">Commercial logo size</span></span>

<span data-ttu-id="47cd6-166">วิชวล Power BI จำเป็นต้องใช้โลโก้เชิงพาณิชย์สองอัน อันหนึ่งสำหรับไทล์ขนาดใหญ่ และอีกหนึ่งอันสำหรับไทล์ขนาดเล็ก</span><span class="sxs-lookup"><span data-stu-id="47cd6-166">A Power BI visual requires two commercial logos, one for large tiles and one for small tiles.</span></span> <span data-ttu-id="47cd6-167">วางโลโก้ภายในกล่องแสดงขอบเขตที่อยู่มุมขวาด้านบนหรือด้านล่าง ด้วยระยะขอบ 4 px</span><span class="sxs-lookup"><span data-stu-id="47cd6-167">Place the logo within a bounding box placed at the top or bottom right corner, with 4 px margins.</span></span>

<span data-ttu-id="47cd6-168">ตารางต่อไปนี้อธิบายถึงข้อควรพิจารณาของขนาดสำหรับวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="47cd6-168">The following table describes the size considerations for Power BI visuals.</span></span>

|<span data-ttu-id="47cd6-169">ตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="47cd6-169">Settings</span></span>  |<span data-ttu-id="47cd6-170">วิชวล Power BI ขนาดเล็ก</span><span class="sxs-lookup"><span data-stu-id="47cd6-170">Small Power BI visual</span></span>  |<span data-ttu-id="47cd6-171">วิชวล Power BI ขนาดใหญ่</span><span class="sxs-lookup"><span data-stu-id="47cd6-171">Large Power BI visual</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="47cd6-172">*ความกว้างของโลโก้*</span><span class="sxs-lookup"><span data-stu-id="47cd6-172">*Logo width*</span></span>    |<span data-ttu-id="47cd6-173">สูงสุด 240 px</span><span class="sxs-lookup"><span data-stu-id="47cd6-173">Up to 240 px</span></span>         |<span data-ttu-id="47cd6-174">มากกว่า 240 px</span><span class="sxs-lookup"><span data-stu-id="47cd6-174">Greater than 240 px</span></span>         |
|<span data-ttu-id="47cd6-175">*ความสูงของโลโก้*</span><span class="sxs-lookup"><span data-stu-id="47cd6-175">*Logo height*</span></span>     |<span data-ttu-id="47cd6-176">สูงสุด 160 px</span><span class="sxs-lookup"><span data-stu-id="47cd6-176">Up to 160 px</span></span>         |<span data-ttu-id="47cd6-177">มากกว่า 160 px</span><span class="sxs-lookup"><span data-stu-id="47cd6-177">Greater than 160 px</span></span>         |
|<span data-ttu-id="47cd6-178">*ขนาดกล่องแสดงขอบเขต*</span><span class="sxs-lookup"><span data-stu-id="47cd6-178">*Bounding box size*</span></span>     |<span data-ttu-id="47cd6-179">40 x 15 px</span><span class="sxs-lookup"><span data-stu-id="47cd6-179">40 x 15 px</span></span>         |<span data-ttu-id="47cd6-180">101 x 30 px</span><span class="sxs-lookup"><span data-stu-id="47cd6-180">101 x 30 px</span></span>         |
|<span data-ttu-id="47cd6-181">*ตัวอย่างโลโก้เชิงพาณิชย์*</span><span class="sxs-lookup"><span data-stu-id="47cd6-181">*Commercial logo example*</span></span>     |![ภาพหน้าจอของโลโก้เชิงพาณิชย์ขนาดเล็กของ Microsoft](media/guidelines-powerbi-visuals/grey-microsoft-symbol.png)         |![ภาพหน้าจอของโลโก้เชิงพาณิชย์ของ Microsoft](media/guidelines-powerbi-visuals/grey-microsoft-logo.png)         |
|<span data-ttu-id="47cd6-184">*ตัวอย่างกล่องแสดงขอบเขต*</span><span class="sxs-lookup"><span data-stu-id="47cd6-184">*Bounding box example*</span></span>    |![ภาพหน้าจอของขนาดของโลโก้ขนาดเล็ก](media/guidelines-powerbi-visuals/small-logo-box.png)         |![ภาพหน้าจอของขนาดของโลโก้ขนาดใหญ่](media/guidelines-powerbi-visuals/big-logo-box.png)         |
|    |         |         |

### <a name="commercial-logo-behavior"></a><span data-ttu-id="47cd6-187">ลักษณะการทำงานของโลโก้เชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="47cd6-187">Commercial logo behavior</span></span>

<span data-ttu-id="47cd6-188">โลโก้เชิงพาณิชย์สามารถใช้ได้เฉพาะในโหมดแก้ไขเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="47cd6-188">Commercial logos are only allowed in edit mode.</span></span> <span data-ttu-id="47cd6-189">เมื่อคลิกแล้ว โลโก้เชิงพาณิชย์จะมีฟังก์ชันการทำงานต่อไปนี้เท่านั้น:</span><span class="sxs-lookup"><span data-stu-id="47cd6-189">When clicked, a commercial logo can only include the following functionality:</span></span>

* <span data-ttu-id="47cd6-190">การคลิกที่โลโก้เชิงพาณิชย์จะเปลี่ยนเส้นทางไปยังเว็บไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="47cd6-190">Clicking the commercial logo redirects to your website.</span></span>

* <span data-ttu-id="47cd6-191">การคลิกโลโก้เชิงพาณิชย์จะเปิดหน้าต่างป๊อปอัปพร้อมข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="47cd6-191">Clicking the commercial logo opens a popup window with additional information.</span></span> <span data-ttu-id="47cd6-192">หน้าต่างป๊อปอัปควรแบ่งออกเป็นสองส่วน:</span><span class="sxs-lookup"><span data-stu-id="47cd6-192">The popup window should be divided into two sections:</span></span>
    * <span data-ttu-id="47cd6-193">พื้นที่การตลาดซึ่งสามารถรวมโลโก้เชิงพาณิชย์ การจัดอันดับวิชวลและการตลาด</span><span class="sxs-lookup"><span data-stu-id="47cd6-193">A marketing area which can include the the commercial logo, a visual and market ratings.</span></span>
    * <span data-ttu-id="47cd6-194">พื้นที่ข้อมูลซึ่งสามารถรวมข้อมูลและลิงก์</span><span class="sxs-lookup"><span data-stu-id="47cd6-194">An information area which can include information and links.</span></span>    


### <a name="things-to-avoid"></a><span data-ttu-id="47cd6-195">สิ่งที่ต้องหลีกเลี่ยง</span><span class="sxs-lookup"><span data-stu-id="47cd6-195">Things to avoid</span></span>

* <span data-ttu-id="47cd6-196">โลโก้เชิงพาณิชย์ไม่สามารถแสดงในโหมดมุมมองได้</span><span class="sxs-lookup"><span data-stu-id="47cd6-196">Commercial logos cannot be displayed in view mode.</span></span>

* <span data-ttu-id="47cd6-197">โลโก้เชิงพาณิชย์แบบเคลื่อนไหวสามารถแสดงภาพเคลื่อนไหวได้สูงสุดห้าวินาที</span><span class="sxs-lookup"><span data-stu-id="47cd6-197">An animated commercial logo can display animation for up to five seconds.</span></span>

* <span data-ttu-id="47cd6-198">หากวิชวล Power BI ของคุณมีไอคอนข้อมูล (i) ในโหมดการอ่าน วิชวลควรเป็นไปตามสี ขนาด และตำแหน่งของโลโก้เชิงพาณิชย์ดังที่อธิบายไว้ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="47cd6-198">If your Power BI visual includes informative icons (i) in reading mode, they should comply to the color, size, and location of the commercial logo, as described above.</span></span>

* <span data-ttu-id="47cd6-199">หลีกเลี่ยงการใช้โลโก้เชิงพาณิชย์ที่มีสีสันหรือสีดำ</span><span class="sxs-lookup"><span data-stu-id="47cd6-199">Avoid a colorful or a black commercial logo.</span></span> <span data-ttu-id="47cd6-200">โลโก้เชิงพาณิชย์ต้องเป็นสีเทา (hex color #C8C8C8)</span><span class="sxs-lookup"><span data-stu-id="47cd6-200">The commercial logo must be grey (hex color #C8C8C8).</span></span>

    ![ภาพหน้าจอของโลโก้ Microsoft ที่มีสีสันที่ไม่ได้รับอนุญาต](media/guidelines-powerbi-visuals/no-color-logo.png) ![ภาพหน้าจอของโลโก้ Microsoft ที่มีสีดำที่ไม่ได้รับอนุญาต](media/guidelines-powerbi-visuals/black-logo.png)

* <span data-ttu-id="47cd6-203">โลโก้เชิงพาณิชย์ที่มีเอฟเฟกต์ เช่น การไล่ระดับสีหรือเงาที่เข้ม</span><span class="sxs-lookup"><span data-stu-id="47cd6-203">A commercial logo with effects such as gradients or strong shadows.</span></span>

    ![ภาพหน้าจอของตัวอย่างโลโก้สไตล์ Microsoft ที่ไม่ได้รับอนุญาต](media/guidelines-powerbi-visuals/no-style-logo.png)

## <a name="best-practices"></a><span data-ttu-id="47cd6-205">แนวทางปฏิบัติที่ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="47cd6-205">Best practices</span></span>

<span data-ttu-id="47cd6-206">เมื่อเผยแพร่วิชวล Power BI ให้พิจารณาคำแนะนำต่อไปนี้เพื่อมอบประสบการณ์ที่ยอดเยี่ยมแก่ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="47cd6-206">When publishing a Power BI visual, consider the following recommendations in order to provide users a great experience.</span></span>

### <a name="visual-landing-page"></a><span data-ttu-id="47cd6-207">หน้าเริ่มต้นของวิชวล</span><span class="sxs-lookup"><span data-stu-id="47cd6-207">Visual landing page</span></span>

<span data-ttu-id="47cd6-208">ใช้หน้าเริ่มต้นเพื่อชี้แจงให้ผู้ใช้ทราบว่าพวกเขาสามารถใช้วิชวล Power BI ของคุณได้อย่างไรและสามารถซื้อใบอนุญาตได้ที่ไหน</span><span class="sxs-lookup"><span data-stu-id="47cd6-208">Use the landing page to clarify to users how they can use your Power BI visual and where to purchase the license.</span></span> <span data-ttu-id="47cd6-209">อย่าใส่วิดีโอที่เรียกใช้งานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="47cd6-209">Don't include videos that are automatically triggered.</span></span> <span data-ttu-id="47cd6-210">เพิ่มเฉพาะเนื้อหาที่ช่วยเพิ่มประสบการณ์ของผู้ใช้ เช่น ข้อมูลหรือลิงก์ไปยังรายละเอียดการซื้อใบอนุญาตและวิธีใช้คุณลักษณะ IAP เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="47cd6-210">Add only material that helps improve the user's experience, such as information or links to license purchasing details and how to use IAP features.</span></span>

### <a name="license-key-and-token"></a><span data-ttu-id="47cd6-211">คีย์ใบอนุญาตและโทเค็น</span><span class="sxs-lookup"><span data-stu-id="47cd6-211">License key and token</span></span>

<span data-ttu-id="47cd6-212">เพื่อความสะดวกของผู้ใช้ เพิ่มคีย์ใบอนุญาตหรือโทเค็นที่เกี่ยวข้องกับเขตข้อมูลที่ด้านบนของบานหน้าต่างการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="47cd6-212">For the user's convenience, add the license key or token related fields at the top of the format pane.</span></span>

## <a name="faq"></a><span data-ttu-id="47cd6-213">คำถามที่ถามบ่อย</span><span class="sxs-lookup"><span data-stu-id="47cd6-213">FAQ</span></span>

<span data-ttu-id="47cd6-214">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิชวล Power BI โปรดดูที่ [คำถามที่ถามบ่อยเกี่ยวกับวิชวล Power BI ที่มีการซื้อเพิ่มเติม](power-bi-custom-visuals-faq.md#visuals-with-additional-purchases)</span><span class="sxs-lookup"><span data-stu-id="47cd6-214">For more information about Power BI visuals, see  [Frequently asked questions about Power BI visuals with additional purchases](power-bi-custom-visuals-faq.md#visuals-with-additional-purchases).</span></span>

## <a name="next-steps"></a><span data-ttu-id="47cd6-215">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="47cd6-215">Next steps</span></span>

<span data-ttu-id="47cd6-216">เรียนรู้วิธีการที่คุณสามารถเผยแพร่วิชวล Power BI ของคุณไปยัง Microsoft AppSource เพื่อให้บุคคลอื่นสามารถค้นหาและใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="47cd6-216">Learn how you can publish your Power BI visual to Microsoft AppSource for others to discover and use.</span></span>

>[!div class="nextstepaction"]
>[<span data-ttu-id="47cd6-217">เผยแพร่วิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="47cd6-217">Publish Power BI visuals</span></span>](office-store.md)
