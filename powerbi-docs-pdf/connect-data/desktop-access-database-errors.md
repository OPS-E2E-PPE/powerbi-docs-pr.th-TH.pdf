---
title: แก้ไขปัญหาการนำเข้า Access และ XLS ใน Power BI Desktop
description: แก้ไขปัญหาการนำเข้าฐานข้อมูล Access และสเปรดชีต Excel ใน Power BI Desktop และ Power Query
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 12/09/2020
LocalizationGroup: Troubleshooting
ms.openlocfilehash: b144412ee322aa9bec0a35bb3876a949abcd3f13
ms.sourcegitcommit: 8250187368d3de48663eb516a816ff701119b579
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/10/2020
ms.locfileid: "96998909"
---
# <a name="troubleshoot-importing-access-and-excel-xls-files-in-power-bi-desktop"></a><span data-ttu-id="99aa3-103">การแก้ไขปัญหาการนำเข้าไฟล์ Access และไฟล์ .xls ของ Excel ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="99aa3-103">Troubleshoot importing Access and Excel .xls files in Power BI Desktop</span></span>

<span data-ttu-id="99aa3-104">ใน Power BI Desktop ทั้งฐานข้อมูล Access และเวิร์กบุ๊ก Excel รุ่นก่อนหน้า (ไฟล์ .XLS ของ Excel 97-2003) ใช้ *กลไกจัดการฐานข้อมูล Access*</span><span class="sxs-lookup"><span data-stu-id="99aa3-104">In Power BI Desktop, both Access databases and early versions of Excel workbooks (.XLS files of type Excel 97-2003) use the *Access Database Engine*.</span></span> <span data-ttu-id="99aa3-105">มีสามสถานการณ์ทั่วไปที่ทำให้กลไกจัดการฐานข้อมูล Access ไม่สามารถทำงานอย่างถูกต้อง:</span><span class="sxs-lookup"><span data-stu-id="99aa3-105">There are three common situations that can prevent the Access Database Engine from working properly.</span></span>

## <a name="situation-1-no-access-database-engine-is-installed"></a><span data-ttu-id="99aa3-106">สถานการณ์ที่ 1: ไม่ติดตั้งกลไกจัดการฐานข้อมูล Access</span><span class="sxs-lookup"><span data-stu-id="99aa3-106">Situation 1: No Access Database Engine is installed</span></span>

<span data-ttu-id="99aa3-107">ถ้าข้อความแสดงความผิดพลาดของ Power BI Desktop ระบุว่าไม่ได้ติดตั้งกลไกจัดการฐานข้อมูล Access คุณต้องติดตั้งกลไกจัดการฐานข้อมูล Access แบบ 32 บิต หรือ 64 บิต ที่ตรงกับเวอร์ชัน Power BI Desktop ของคุณ</span><span class="sxs-lookup"><span data-stu-id="99aa3-107">If the Power BI Desktop error message indicates the Access Database Engine isn't installed, you must install the Access Database Engine version, either 32-bit or 64-bit, that matches your Power BI Desktop version.</span></span> <span data-ttu-id="99aa3-108">คุณสามารถติดตั้งกลไกจัดการฐานข้อมูล Access จาก[หน้าดาวน์โหลด](https://www.microsoft.com/download/details.aspx?id=13255)ได้</span><span class="sxs-lookup"><span data-stu-id="99aa3-108">You can install the Access Database Engine from the [downloads page](https://www.microsoft.com/download/details.aspx?id=13255).</span></span>

<span data-ttu-id="99aa3-109">หากคุณกำลังทำงานกับกระแสข้อมูลและใช้เกตเวย์เพื่อเชื่อมต่อกับข้อมูล คุณต้องติดตั้งกลไกจัดการฐานข้อมูล Access ลงในคอมพิวเตอร์ที่ใช้งานเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="99aa3-109">If you're working with dataflows and using a gateway to connect to the data, you must install the Access Database Engine onto the computer running the gateway.</span></span> 

>[!NOTE]
><span data-ttu-id="99aa3-110">ถ้าเวอร์ชันบิตของกลไกจัดการฐานข้อมูล Access ที่ติดตั้งแตกต่างจากเวอร์ชันบิตของ Microsoft Office ที่คุณติดตั้ง แอปพลิเคชัน Office จะไม่สามารถใช้กลไกจัดการฐานข้อมูล Access</span><span class="sxs-lookup"><span data-stu-id="99aa3-110">If the installed Access Database Engine bit-version is different from your Microsoft Office installation's bit-version, Office applications won't be able to use the Access Database Engine.</span></span>

## <a name="situation-2-the-access-database-engine-bit-version-32-bit-or-64-bit-is-different-from-your-power-bi-desktop-bit-version"></a><span data-ttu-id="99aa3-111">สถานการณ์ที่ 2: เวอร์ชันบิตของกลไกจัดการฐานข้อมูล Access (32 บิต หรือ 64 บิต) แตกต่างจากเวอร์ชันบิตของ Power BI Desktop ของคุณ</span><span class="sxs-lookup"><span data-stu-id="99aa3-111">Situation 2: The Access Database Engine bit-version (32-bit or 64-bit) is different from your Power BI Desktop bit-version</span></span>

<span data-ttu-id="99aa3-112">สถานการณ์นี้มักจะเกิดขึ้นเมื่อเวอร์ชั่นของ Microsoft Office ที่ติดตั้งเป็นแบบ 32 บิต และเวอร์ชันของ Power BI Desktop ที่ติดตั้งเป็นแบบ 64 บิต</span><span class="sxs-lookup"><span data-stu-id="99aa3-112">This situation often occurs when the installed version of Microsoft Office is 32-bit, and the version of Power BI Desktop installed is 64-bit.</span></span> <span data-ttu-id="99aa3-113">สถานการณ์ตรงกันข้ามสามารถเกิดขึ้นได้และเกิดการไม่สอดล้องกันของเวอร์ชันบิตในกรณีใดกรณีหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="99aa3-113">The opposite can occur as well and the bit-version mismatch will occur in either case.</span></span> <span data-ttu-id="99aa3-114">หากคุณใช้การสมัครใช้งาน Microsoft 365 ให้ดู [สถานการณ์ที่ 3](#situation-3-trouble-using-access-or-xls-files-with-a-microsoft-365-subscription) สำหรับปัญหาและวิธีแก้ไขที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="99aa3-114">If you're using a Microsoft 365 subscription, see [Situation 3](#situation-3-trouble-using-access-or-xls-files-with-a-microsoft-365-subscription) for a different issue and resolution.</span></span> <span data-ttu-id="99aa3-115">วิธีการแก้ไขหนึ่งจากหลายข้อต่อไปนี้สามารถแก้ไขข้อผิดพลาดเรื่องเวอร์ชันบิตที่ไม่ตรงกัน:</span><span class="sxs-lookup"><span data-stu-id="99aa3-115">Any of the following solutions can remedy this bit-version mismatch error:</span></span>

### <a name="solution-1"></a><span data-ttu-id="99aa3-116">วิธีการแก้ไขที่ 1</span><span class="sxs-lookup"><span data-stu-id="99aa3-116">Solution 1</span></span>

<span data-ttu-id="99aa3-117">เปลี่ยนเวอร์ชันของ Power BI Desktop เพื่อให้เข้ากับเวอร์ชันบิต Microsoft Office ที่ติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="99aa3-117">Change the version of Power BI Desktop to match the bit-version of your Microsoft Office installation.</span></span> 

1. <span data-ttu-id="99aa3-118">เมื่อต้องเปลี่ยนเวอร์ชันบิตของ Power BI Desktop ถอนการติดตั้ง Power BI Desktop และจากนั้น ติดตั้งเวอร์ชันของ Power BI Desktop ที่เข้ากับการติดตั้ง Office</span><span class="sxs-lookup"><span data-stu-id="99aa3-118">To change the bit-version of Power BI Desktop, uninstall Power BI Desktop, and then install the version of Power BI Desktop that matches your Office installation.</span></span> 

1. <span data-ttu-id="99aa3-119">เมื่อต้องเลือกเวอร์ชันของ Power BI Desktop ให้เลือก **ตัวเลือกการดาวน์โหลดขั้นสูง** บนหน้าดาวน์โหลด Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="99aa3-119">To select a version of Power BI Desktop, select **Advanced download options** on the Power BI Desktop download page.</span></span>
   
   ![ตัวเลือกการดาวน์โหลดขั้นสูงบนหน้าดาวน์โหลด Power BI Desktop](media/desktop-access-database-errors/desktop-access-errors-1.png)
   
1. <span data-ttu-id="99aa3-121">บนหน้าการดาวน์โหลดที่ปรากฏขึ้น เลือกภาษาของคุณ จากนั้น เลือกปุ่ม **ดาวน์โหลด**</span><span class="sxs-lookup"><span data-stu-id="99aa3-121">On the download page that appears, choose your language and then select the **Download** button.</span></span> 
 
1. <span data-ttu-id="99aa3-122">บนหน้าจอที่ปรากฏขึ้น เลือกกล่องกาเครื่องหมายข้าง PBIDesktop.msi สำหรับเวอร์ชัน 32 บิต หรือ PBIDesktop_x64.msi สำหรับเวอร์ชัน 64 บิต</span><span class="sxs-lookup"><span data-stu-id="99aa3-122">On the screen that appears, select the checkbox beside PBIDesktop.msi for the 32-bit version, or PBIDesktop_x64.msi for the 64-bit version.</span></span> 

   <span data-ttu-id="99aa3-123">ในภาพหน้าจอต่อไปนี้ ให้เลือกเวอร์ชัน 64 บิต</span><span class="sxs-lookup"><span data-stu-id="99aa3-123">In the following screenshot, the 64-bit version is selected.</span></span>
   
   ![เลือกประเภทของการดาวน์โหลด Power BI Desktop](media/desktop-access-database-errors/desktop-access-errors-2.png)
   
   >[!NOTE]
   ><span data-ttu-id="99aa3-125">หากคุณใช้ Power BI Desktop เวอร์ชัน 32 บิตเมื่อสร้างแบบจำลองข้อมูลที่มีขนาดใหญ่มาก คุณอาจประสบปัญหาหน่วยความจำไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="99aa3-125">If you use the 32-bit version of Power BI Desktop when creating very large data models, you might experience out-of-memory issues.</span></span>

### <a name="solution-2"></a><span data-ttu-id="99aa3-126">วิธีการแก้ไขที่ 2</span><span class="sxs-lookup"><span data-stu-id="99aa3-126">Solution 2</span></span>

<span data-ttu-id="99aa3-127">เปลี่ยนเวอร์ชันบิตของ Power BI Desktop เพื่อให้เข้ากับเวอร์ชันบิตของตัวติดตั้ง Microsoft Office:</span><span class="sxs-lookup"><span data-stu-id="99aa3-127">Change the bit-version of Microsoft Office to match the bit-version of your Power BI Desktop installation:</span></span>

1. <span data-ttu-id="99aa3-128">ถอนการติดตั้ง Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="99aa3-128">Uninstall Microsoft Office</span></span>

2. <span data-ttu-id="99aa3-129">ติดตั้ง Office เวอร์ชันที่ตรงกับตัวติดตั้ง Power BI Desktop ของคุณ</span><span class="sxs-lookup"><span data-stu-id="99aa3-129">Install the version of Office that matches your Power BI Desktop installation.</span></span>

### <a name="solution-3"></a><span data-ttu-id="99aa3-130">วิธีการแก้ไขที่ 3</span><span class="sxs-lookup"><span data-stu-id="99aa3-130">Solution 3</span></span>

<span data-ttu-id="99aa3-131">ถ้ามีข้อผิดพลาดเกิดขึ้นขณะที่คุณพยายามเปิดไฟล์ .XLS (เวิร์กบุ๊ก Excel 97-2003) คุณสามารถหลีกเลี่ยงการใช้กลไกจัดการฐานข้อมูล Access ด้วยการเปิดไฟล์ .XLS ใน Excel และบันทึกเป็นไฟล์ XLSX</span><span class="sxs-lookup"><span data-stu-id="99aa3-131">If the error occurs when you attempt to open an .XLS file (an Excel 97-2003 workbook), you can avoid using the Access Database Engine by opening the .XLS file in Excel, and saving it as an XLSX file.</span></span>

### <a name="solution-4"></a><span data-ttu-id="99aa3-132">วิธีการแก้ไขที่ 4</span><span class="sxs-lookup"><span data-stu-id="99aa3-132">Solution 4</span></span>

<span data-ttu-id="99aa3-133">ถ้าวิธีแก้ไขปัญหาสามข้อก่อนหน้านี้ไม่สามารถทำได้ เป็นไปได้ที่คุณจะติดตั้งกลไกจัดการฐานข้อมูล Access ทั้งสองเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="99aa3-133">If the previous three solutions are not feasible, it's possible to install both versions of the Access Database Engine.</span></span> <span data-ttu-id="99aa3-134">อย่างไรก็ตาม เราไม่ขอแนะนำการแก้ปัญหาเฉพาะหน้าแบบนี้</span><span class="sxs-lookup"><span data-stu-id="99aa3-134">However, this workaround isn't recommended.</span></span> <span data-ttu-id="99aa3-135">ถึงแม้ว่าการติดตั้งทั้งสองเวอร์ชันจะแก้ไขปัญหานี้สำหรับ Power Query สำหรับ Excel และ Power BI Desktop แต่จะสร้างข้อผิดพลาดและปัญหาสำหรับแอปพลิเคชันที่ใช้เวอร์ชันบิตของกลไกจัดการฐานข้อมูล Access ที่มีการติดตั้งในครั้งแรกโดยอัตโนมัติ (ตามค่าเริ่มต้น)</span><span class="sxs-lookup"><span data-stu-id="99aa3-135">Although installing both versions will resolve this issue for Power Query for Excel and Power BI Desktop, it will introduce errors and issues for any application that automatically (by default) uses the bit-version of the Access Database Engine that was installed first.</span></span> 

<span data-ttu-id="99aa3-136">หากต้องการติดตั้งกลไกจัดการฐานข้อมูล Access ทั้งสองเวอร์ชันบิต ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="99aa3-136">To install both bit-versions of the Access Database Engine, follow these steps:</span></span>

1. <span data-ttu-id="99aa3-137">ติดตั้งกลไกจัดการฐานข้อมูล Access ทั้งสองเวอร์ชันบิตจาก [หน้าดาวน์โหลด](https://www.microsoft.com/download/details.aspx?id=13255)</span><span class="sxs-lookup"><span data-stu-id="99aa3-137">Install both bit-versions of the Access Database Engine from the [download page](https://www.microsoft.com/download/details.aspx?id=13255).</span></span> 

1. <span data-ttu-id="99aa3-138">เรียกใช้กลไกจัดการฐานข้อมูล Access แต่ละเวอร์ชันโดยใช้สวิตช์ */passive*</span><span class="sxs-lookup"><span data-stu-id="99aa3-138">Run each version of the Access Database Engine by using the */passive* switch.</span></span> <span data-ttu-id="99aa3-139">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="99aa3-139">For example:</span></span>

   ```console
   c:\users\joe\downloads\AccessDatabaseEngine.exe /passive

   c:\users\joe\downloads\AccessDatabaseEngine_x64.exe /passive
   ```

## <a name="situation-3-trouble-using-access-or-xls-files-with-a-microsoft-365-subscription"></a><span data-ttu-id="99aa3-140">สถานการณ์ที่ 3: ปัญหาในการใช้ไฟล์ Access หรือ .XLS กับ Microsoft 365 แบบสมัครใช้งาน</span><span class="sxs-lookup"><span data-stu-id="99aa3-140">Situation 3: Trouble using Access or .XLS files with a Microsoft 365 subscription</span></span>

<span data-ttu-id="99aa3-141">ถ้าคุณกำลังใช้ Microsoft 365 แบบสมัครใช้งานไม่ว่าจะเป็น **Office 2013** หรือ **Office 2016** ตัวให้บริการของกลไกจัดการฐานข้อมูล Access จะได้รับการลงทะเบียนในตำแหน่งที่ตั้งของรีจิสทรีเสมือนจริงที่สามารถเข้าถึงได้ *เฉพาะ* กระบวนการต่าง ๆ ของ Microsoft Office เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="99aa3-141">If you're using a Microsoft 365 subscription, whether **Office 2013** or **Office 2016**, the Access Database Engine provider is registered in a virtual registry location that's *only* accessible to Microsoft Office processes.</span></span> <span data-ttu-id="99aa3-142">เป็นผลให้กลไกจัดการ Mashup (ซึ่งรับผิดชอบในการเรียกใช้งาน Excel ที่ไม่ใช่ Office 365 และ Power BI Desktop และไม่ใช่กระบวนการ Office) ไม่สามารถใช้งานตัวให้บริการของกลไกจัดการฐานข้อมูล Access ได้</span><span class="sxs-lookup"><span data-stu-id="99aa3-142">As a result, the Mashup Engine (which is responsible for running non-Office 365 Excel and Power BI Desktop, and isn't an Office process), can't use the Access Database Engine provider.</span></span>

<span data-ttu-id="99aa3-143">เพื่อแก้ไขสถานการณ์นี้ ให้[ดาวน์โหลดและติดตั้งกลไกจัดการฐานข้อมูล Access ชนิดสามารถเผยแพร่ต่อ](https://www.microsoft.com/download/details.aspx?id=13255)ที่เข้ากับเวอร์ชันบิตของ Power BI Desktop ที่ติดตั้งของคุณ</span><span class="sxs-lookup"><span data-stu-id="99aa3-143">To remedy this situation, [download and install the Access Database Engine redistributable](https://www.microsoft.com/download/details.aspx?id=13255) that matches the bit-version of your Power BI Desktop installation.</span></span> <span data-ttu-id="99aa3-144">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเวอร์ชันบิต ให้ดูส่วนก่อนหน้าในบทความนี้</span><span class="sxs-lookup"><span data-stu-id="99aa3-144">For more information about bit-versions, see the earlier sections in this article.</span></span>

## <a name="other-situations-that-can-cause-import-issues"></a><span data-ttu-id="99aa3-145">สถานการณ์อื่น ๆ ที่อาจทำให้เกิดปัญหาการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="99aa3-145">Other situations that can cause import issues</span></span>

<span data-ttu-id="99aa3-146">เราจะมุ่งมั่นที่จะครอบคลุมปัญหาที่เกิดขึ้นกับไฟล์ Access หรือ .XLS มากเท่าที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="99aa3-146">We strive to cover as many issues that occur with Access or .XLS files as possible.</span></span> <span data-ttu-id="99aa3-147">ถ้าคุณพบปัญหาที่ไม่ได้ครอบคลุมในบทความนี้ โปรดส่งคำถามเกี่ยวกับปัญหานั้นไปที่ [ศูนย์สนับสนุน Power BI](https://powerbi.microsoft.com/support/)</span><span class="sxs-lookup"><span data-stu-id="99aa3-147">If you encounter an issue that isn't covered in this article, submit a question about the issue to [Power BI Support](https://powerbi.microsoft.com/support/).</span></span> <span data-ttu-id="99aa3-148">เราดูปัญหาที่อาจจะมีผลกระทบต่อลูกค้าเป็นประจำ และรวมเอาไว้ในบทความของเรา</span><span class="sxs-lookup"><span data-stu-id="99aa3-148">We regularly look at issues that may be affecting many customers, and include them in our articles.</span></span>

