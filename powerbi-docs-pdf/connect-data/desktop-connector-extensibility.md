---
title: การขยายของตัวเชื่อมต่อใน Power BI
description: ความสามารถในการขยายตัวของตัวเชื่อมต่อ คุณลักษณะ การตั้งค่าความปลอดภัย และตัวเชื่อมต่อที่ผ่านการรับรอง
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: conceptual
ms.date: 01/02/2020
LocalizationGroup: Connect to data
ms.openlocfilehash: 6b78309ad17446aabacd39006968b6d397a51037
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411252"
---
# <a name="connector-extensibility-in-power-bi"></a><span data-ttu-id="629b6-103">การขยายของตัวเชื่อมต่อใน Power BI</span><span class="sxs-lookup"><span data-stu-id="629b6-103">Connector extensibility in Power BI</span></span>

<span data-ttu-id="629b6-104">Power BI สามารถเชื่อมต่อกับข้อมูลโดยใช้ตัวเชื่อมต่อและแหล่งข้อมูลทั่วไป เช่น ODBC, OData, OLE DB, Web, CSV, XML และ JSON</span><span class="sxs-lookup"><span data-stu-id="629b6-104">Power BI can connect to data by using existing connectors and generic data sources, like ODBC, OData, OLE DB, Web, CSV, XML, and JSON.</span></span> <span data-ttu-id="629b6-105">หรือนักพัฒนาสามารถเปิดใช้งานแหล่งข้อมูลใหม่ด้วยส่วนขยายข้อมูลแบบกำหนดเองที่เรียกว่า *ตัวเชื่อมต่อแบบกำหนดเอง*</span><span class="sxs-lookup"><span data-stu-id="629b6-105">Or, developers can enable new data sources with custom data extensions called *custom connectors*.</span></span> <span data-ttu-id="629b6-106">ตัวเชื่อมต่อแบบกำหนดเองบางตัวจะได้รับการรับรองและเผยแพร่โดย Microsoft ในฐานะ *ตัวเชื่อมต่อที่ได้รับการรับรอง*</span><span class="sxs-lookup"><span data-stu-id="629b6-106">Some custom connectors are certified and distributed by Microsoft as *certified connectors*.</span></span>

<span data-ttu-id="629b6-107">เพื่อใช้ตัวเชื่อมต่อแบบกำหนดเองที่ยังไม่ผ่านการรับรอง ซึ่งคุณหรือบุคคลที่สามได้พัฒนาขึ้น คุณจะต้องปรับการตั้งค่าการรักษาความปลอดภัยของ Power BI Desktop เพื่ออนุญาตให้ส่วนขยายสามารถโหลดได้โดยไม่จำเป็นต้องตรวจสอบความถูกต้องหรือคำเตือน</span><span class="sxs-lookup"><span data-stu-id="629b6-107">To use non-certified custom connectors that you or a third party have developed, you must adjust the Power BI Desktop security settings to allow extensions to load without validation or warning.</span></span> <span data-ttu-id="629b6-108">เนื่องจากรหัสนี้สามารถจัดการข้อมูลประจำตัว รวมถึงการส่งข้อมูลประจำตัวผ่านทาง HTTP และเพิกเฉยระดับความเป็นส่วนตัว คุณควรใช้การตั้งค่าการรักษาความปลอดภัยนี้ ในกรณีที่คุณไว้วางใจในตัวเชื่อมต่อแบบกำหนดเองของคุณอย่างสมบูรณ์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="629b6-108">Because this code can handle credentials, including sending them over HTTP, and ignore privacy levels, you should only use this security setting if you absolutely trust your custom connectors.</span></span>

<span data-ttu-id="629b6-109">อีกตัวเลือกหนึ่งสำหรับนักพัฒนาคือ การลงชื่อเข้าใช้ตัวเชื่อมต่อที่มีใบรับรอง และระบุข้อมูลที่คุณจำเป็นต้องใช้โดยไม่เปลี่ยนแปลงการตั้งค่าการรักษาความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="629b6-109">Another option is for the developer to sign the connector with a certificate, and provide the information you need to use it without changing your security settings.</span></span> <span data-ttu-id="629b6-110">สำหรับข้อมูลเพิ่มเติม ดู [เกี่ยวกับตัวเชื่อมต่อบุคลที่สามที่เชื่อถือได้](desktop-trusted-third-party-connectors.md)</span><span class="sxs-lookup"><span data-stu-id="629b6-110">For more information, see [About trusted third-party connectors](desktop-trusted-third-party-connectors.md).</span></span>

## <a name="custom-connectors"></a><span data-ttu-id="629b6-111">ตัวเชื่อมต่อแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="629b6-111">Custom connectors</span></span>

<span data-ttu-id="629b6-112">ตัวเชื่อมต่อแบบกำหนดเองที่ยังไม่ผ่านการรับรอง สามารถรวมการใช้งานได้อย่างกว้างขวาง ตั้งแต่ API ขนาดเล็กที่มีความสำคัญต่อธุรกิจของคุณไปจนถึงบริการเฉพาะของอุตสาหกรรมขนาดใหญ่ที่ Microsoft ยังไม่ได้เผยแพร่ตัวเชื่อมต่อให้</span><span class="sxs-lookup"><span data-stu-id="629b6-112">Non-certified custom connectors can range from small business-critical APIs to large industry-specific services that Microsoft hasn't released a connector for.</span></span> <span data-ttu-id="629b6-113">มีการเผยแพร่ตัวเชื่อมต่อจำนวนมากโดยผู้จำหน่าย</span><span class="sxs-lookup"><span data-stu-id="629b6-113">Many connectors are distributed by vendors.</span></span> <span data-ttu-id="629b6-114">ถ้าคุณจำเป็นต้องมีตัวเชื่อมต่อข้อมูลเฉพาะ ให้ติดต่อผู้จำหน่าย</span><span class="sxs-lookup"><span data-stu-id="629b6-114">If you need a specific data connector, contact the vendor.</span></span> 

<span data-ttu-id="629b6-115">เมื่อต้องการใช้ตัวเชื่อมต่อแบบกำหนดเองที่ยังไม่ผ่านการรับรอง ให้วางตัวเชื่อมต่อไฟล์ *.pq*, *.pqx*, *.m* หรือ *.mez* ในโฟลเดอร์ *\[Documents]\\Power BI Desktop\\ตัวเชื่อมต่อแบบกำหนดเอง*</span><span class="sxs-lookup"><span data-stu-id="629b6-115">To use a non-certified custom connector, put the connector *.pq*, *.pqx*, *.m*, or *.mez* file in the *\[Documents]\\Power BI Desktop\\Custom Connectors* folder.</span></span> <span data-ttu-id="629b6-116">หากไม่มีโฟลเดอร์ ให้สร้างใหม่</span><span class="sxs-lookup"><span data-stu-id="629b6-116">If the folder doesn't exist, create it.</span></span>

<span data-ttu-id="629b6-117">ปรับการตั้งค่าการรักษาความปลอดภัยของส่วนขยายข้อมูลดังนี้:</span><span class="sxs-lookup"><span data-stu-id="629b6-117">Adjust the data extension security settings as follows:</span></span>

<span data-ttu-id="629b6-118">ใน Power BI Desktop เลือก **ไฟล์** > **ตัวเลือกและการตั้งค่า** > **ตัวเลือก** > **การรักษาความปลอดภัย**</span><span class="sxs-lookup"><span data-stu-id="629b6-118">In Power BI Desktop, select **File** > **Options and settings** > **Options** > **Security**.</span></span>

<span data-ttu-id="629b6-119">ภายใต้ **ส่วนขยายข้อมูล** เลือก **(ไม่แนะนำ) อนุญาตให้โหลดส่วนขยายใด ๆ โดยไม่มีการตรวจสอบความถูกต้องหรือคำเตือน**</span><span class="sxs-lookup"><span data-stu-id="629b6-119">Under **Data Extensions**, select **(Not Recommended) Allow any extension to load without validation or warning**.</span></span> <span data-ttu-id="629b6-120">เลือก **ตกลง** จากนั้น รีสตาร์ท Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="629b6-120">Select **OK**, and then restart Power BI Desktop.</span></span> 

![อนุญาตตัวเชื่อมต่อแบบกำหนดเองที่ไม่ได้รับการรับรองในตัวเลือก การรักษาความปลอดภัยของส่วนขยายข้อมูล](media/desktop-connector-extensibility/data-extension-security-1.png)

<span data-ttu-id="629b6-122">การตั้งค่าความปลอดภัยของส่วนขยายข้อมูล Power BI Desktop ค่าเริ่มต้นคือ **(แนะนำ) อนุญาตให้ส่วนขยายของบุคคลที่สามที่เชื่อถือได้อื่น ๆ และได้รับการรับรองจาก Microsoft เท่านั้นที่จะโหลดได้**</span><span class="sxs-lookup"><span data-stu-id="629b6-122">The default Power BI Desktop data extension security setting is **(Recommended) Only allow Microsoft certified and other trusted third-party extensions to load**.</span></span> <span data-ttu-id="629b6-123">ด้วยการตั้งค่านี้ หากมีตัวเชื่อมต่อแบบกำหนดเองที่ไม่ได้รับการรับรองบนระบบของคุณ กล่องโต้ตอบ **ตัวเชื่อมต่อที่ไม่ได้รับการรับรอง** จะปรากฏขึ้นที่หน้าเริ่มต้นของ Power BI Desktop โดยแสดงรายการตัวเชื่อมต่อที่ไม่สามารถโหลดอย่างปลอดภัยได้</span><span class="sxs-lookup"><span data-stu-id="629b6-123">With this setting, if there are non-certified custom connectors on your system, the **Uncertified Connectors** dialog box appears at Power BI Desktop startup, listing the connectors that can't securely load.</span></span>

![กล่องโต้ตอบตัวเชื่อมต่อที่ไม่ได้รับการรับรอง](media/desktop-connector-extensibility/data-extension-security-2.png)

<span data-ttu-id="629b6-125">เมื่อต้องการแก้ไขข้อผิดพลาดนี้ คุณสามารถเปลี่ยนการตั้งค่าการรักษาความปลอดภัยของ **ส่วนขยายข้อมูล** ของคุณ หรือลบตัวเชื่อมต่อที่ไม่ผ่านการรับรองออกจากโฟลเดอร์ *ตัวเชื่อมต่อแบบกำหนดเอง* ของคุณ</span><span class="sxs-lookup"><span data-stu-id="629b6-125">To resolve the error, you can either change your **Data Extensions** security setting, or remove the uncertified connectors from your *Custom Connectors* folder.</span></span>

## <a name="certified-connectors"></a><span data-ttu-id="629b6-126">ตัวเชื่อมต่อที่ผ่านการรับรอง</span><span class="sxs-lookup"><span data-stu-id="629b6-126">Certified connectors</span></span>

<span data-ttu-id="629b6-127">ชุดย่อยที่จำกัดของส่วนขยายข้อมูลถือว่า *ผ่านการรับรอง*</span><span class="sxs-lookup"><span data-stu-id="629b6-127">A limited subset of data extensions is considered *certified*.</span></span> <span data-ttu-id="629b6-128">ในขณะที่ Microsoft เผยแพร่ตัวเชื่อมต่อเหล่านี้ เราไม่รับผิดชอบต่อประสิทธิภาพการทำงานหรือการใช้งานฟังก์ชันได้อย่างต่อเนื่องของตัวเชื่อมต่อดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="629b6-128">While Microsoft distributes the connectors, it's not responsible for their performance or continued function.</span></span> <span data-ttu-id="629b6-129">นักพัฒนาบุคคลที่สามที่สร้างตัวเชื่อมต่อนั้น มีหน้าที่รับผิดชอบเกี่ยวกับการบำรุงรักษาและการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="629b6-129">The third-party developer who created the connector is responsible for its maintenance and support.</span></span> 

<span data-ttu-id="629b6-130">ใน Power BI Desktop ตัวเชื่อมต่อของบุคคลที่สามที่ผ่านการรับรอง จะปรากฏในรายการในกล่องโต้ตอบ **รับข้อมูล** พร้อมกับตัวเชื่อมต่อทั่วไปและที่พบบ่อย</span><span class="sxs-lookup"><span data-stu-id="629b6-130">In Power BI Desktop, certified third-party connectors appear in the list in the **Get Data** dialog box, along with generic and common connectors.</span></span> <span data-ttu-id="629b6-131">คุณไม่จำเป็นต้องปรับการตั้งค่าการรักษาความปลอดภัยเพื่อใช้ตัวเชื่อมต่อที่ผ่านการรับรอง</span><span class="sxs-lookup"><span data-stu-id="629b6-131">You don't need to adjust security settings to use the certified connectors.</span></span>

<span data-ttu-id="629b6-132">หากคุณต้องการให้ตัวเชื่อมต่อแบบกำหนดเองผ่านการรับรอง โปรดสอบถามผู้จำหน่ายของคุณเพื่อทำการติดต่อ dataconnectors@microsoft.com</span><span class="sxs-lookup"><span data-stu-id="629b6-132">If you would like a custom connector to be certified, ask your vendor to contact dataconnectors@microsoft.com.</span></span>
