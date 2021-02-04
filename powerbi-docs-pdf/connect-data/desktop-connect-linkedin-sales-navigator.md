---
title: เชื่อมต่อ LinkedIn Sales Navigator ใน Power BI Desktop
description: เชื่อมต่อและใช้ข้อมูลจาก LinkedIn ใน Power BI Desktop ได้อย่างง่ายดาย
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 01/04/2021
LocalizationGroup: Connect to data
ms.openlocfilehash: 6121e2050fdb4d9c94732508dc96c8719598fec3
ms.sourcegitcommit: 932f6856849c39e34229dc9a49fb9379c56a888a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/06/2021
ms.locfileid: "97926982"
---
# <a name="connect-to-linkedin-sales-navigator-in-power-bi-desktop"></a><span data-ttu-id="05581-103">เชื่อมต่อ LinkedIn Sales Navigator ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="05581-103">Connect to LinkedIn Sales Navigator in Power BI Desktop</span></span>

<span data-ttu-id="05581-104">ใน **Power BI Desktop** คุณสามารถเชื่อมต่อกับ **LinkedIn Sales Navigator** เพื่อช่วยในการค้นหาและสร้างความสัมพันธ์เช่นเดียวกับแหล่งข้อมูลอื่นๆ ใน Power BI Desktop และสร้างรายงานที่พร้อมใช้งานเกี่ยวกับความคืบหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="05581-104">In **Power BI Desktop**, you can connect to **LinkedIn Sales Navigator** to help find and build relationships just like any other data source in Power BI Desktop, and create ready-made reports about your progress.</span></span>

![แท็บการใช้งาน LinkedIn Sales Navigator](media/desktop-connect-linkedin-sales-navigator/linkedin-sales-navigator-01.png)


<span data-ttu-id="05581-106">หากต้องการเชื่อมต่อกับข้อมูล LinkedIn โดยใช้ **LinkedIn Sales Navigator** คุณต้องมีแพ็กเกจ LinkedIn Sales Navigator Enterprise และเป็นผู้ดูแลหรือผู้ใช้การรายงานในสัญญา Sales Navigator</span><span class="sxs-lookup"><span data-stu-id="05581-106">To connect to LinkedIn data using the **LinkedIn Sales Navigator**, you need to have a LinkedIn Sales Navigator Enterprise plan, and either be an Admin or Reporting User on the Sales Navigator Contract.</span></span>

<span data-ttu-id="05581-107">วิดีโอต่อไปนี้ให้ข้อมูลแบบย่อและการฝึกใช้งานแอปแม่แบบ **LinkedIn Sales Navigator** ซึ่งจะอธิบายอย่างละเอียด [ภายหลังในบทความนี้](#using-the-linkedin-sales-navigator-template-app)</span><span class="sxs-lookup"><span data-stu-id="05581-107">The following video provides a quick tour and tutorial for using the **LinkedIn Sales Navigator** template app, which is described in detail [later in this article](#using-the-linkedin-sales-navigator-template-app).</span></span> 

> [!VIDEO https://www.youtube.com/embed/ZqhmaiORLw0]

## <a name="connect-to-linkedin-sales-navigator"></a><span data-ttu-id="05581-108">เชื่อมต่อกับ LinkedIn Sales Navigator</span><span class="sxs-lookup"><span data-stu-id="05581-108">Connect to LinkedIn Sales Navigator</span></span>

<span data-ttu-id="05581-109">หากต้องการเชื่อมต่อกับข้อมูล **LinkedIn Sales Navigator** ให้เลือก **รับข้อมูล** จากริบบิ้น **หน้าแรก** ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="05581-109">To connect to **LinkedIn Sales Navigator** data, select **Get Data** from the **Home** ribbon in Power BI Desktop.</span></span> <span data-ttu-id="05581-110">เลือก **บริการออนไลน์** จากหมวดหมู่ทางด้านซ้าย จากนั้นเลื่อนลงมาจนเห็น **LinkedIn Sales Navigator (Beta)**</span><span class="sxs-lookup"><span data-stu-id="05581-110">Select **Online Services** from the categories on the left, then scroll until you see **LinkedIn Sales Navigator (Beta)**.</span></span>

![รับข้อมูลใน Power BI Desktop](media/desktop-connect-linkedin-sales-navigator/linkedin-sales-navigator-02.png)

<span data-ttu-id="05581-112">ระบบจะแนะนำคุณให้เชื่อมต่อกับตัวเชื่อมต่อบุคคลที่สามที่อยู่ในระหว่างการพัฒนา</span><span class="sxs-lookup"><span data-stu-id="05581-112">You'll be advised that you're connecting to a third-party connecter that's still under development.</span></span> 

![คำเตือนเกี่ยวกับบุคคลที่สาม](media/desktop-connect-linkedin-sales-navigator/linkedin-sales-navigator-03.png)

<span data-ttu-id="05581-114">เมื่อเลือก **ดำเนินการต่อ** ระบบจะแจ้งให้คุณระบุข้อมูลที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="05581-114">When you select **Continue**, you're prompted to specify which data you want.</span></span>

![ข้อความแจ้งสำหรับข้อมูลที่ต้องการ](media/desktop-connect-linkedin-sales-navigator/linkedin-sales-navigator-04.png)


<span data-ttu-id="05581-116">ในหน้าต่าง **LinkedIn Sales Navigator** ที่ปรากฎขึ้น ให้เลือกข้อมูลที่คุณต้องการให้แสดง เช่น *ผู้ติดต่อทั้งหมด* หรือ *ผู้ติดต่อที่เลือก* จากตัวเลือกแบบเลื่อนลงอันแรก</span><span class="sxs-lookup"><span data-stu-id="05581-116">In the **LinkedIn Sales Navigator** window that appears, select which data you want to return, either *All contacts* or *Selected contacts* from the first drop-down selector.</span></span> <span data-ttu-id="05581-117">จากนั้นระบุวันที่เริ่มต้นและวันสิ้นสุดเพื่อจำกัดข้อมูลที่ได้รับไปยังหน้าต่างเวลาเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="05581-117">You can then specify the start and end dates to constrain the data it receives to a particular time window.</span></span>

<span data-ttu-id="05581-118">เมื่อคุณให้ข้อมูลแล้ว Power BI Desktop จะเชื่อมต่อกับข้อมูลที่เชื่อมโยงกับสัญญา LinkedIn Sales Navigator</span><span class="sxs-lookup"><span data-stu-id="05581-118">Once you've provided the information, Power BI Desktop connects to the data associated with your LinkedIn Sales Navigator contract.</span></span> <span data-ttu-id="05581-119">ใช้อีเมลเดียวกันกับที่คุณใช้ลงชื่อเข้าใช้ LinkedIn Sales Navigator ผ่านเว็บไซต์</span><span class="sxs-lookup"><span data-stu-id="05581-119">Use the same email address you use to sign in to LinkedIn Sales Navigator through the website.</span></span> 

![ลงชื่อเข้าใช้ LinkedIn](media/desktop-connect-linkedin-sales-navigator/linkedin-sales-navigator-05.png)

<span data-ttu-id="05581-121">เมื่อเชื่อมต่อเรียบร้อยแล้ว คุณจะได้รับแจ้งให้เลือกข้อมูลจากสัญญา LinkedIn Sales Navigator จากหน้าต่าง **Navigator**{3}{4}</span><span class="sxs-lookup"><span data-stu-id="05581-121">When you connect successfully, you're prompted to select which data from your LinkedIn Sales Navigator contract from a **Navigator** window.</span></span>

![เลือกข้อมูลด้วย Navigator](media/desktop-connect-linkedin-sales-navigator/linkedin-sales-navigator-09.png)

<span data-ttu-id="05581-123">คุณจะสร้างรายงานที่คุณต้องการได้ด้วยข้อมูล LinkedIn Sales Navigator</span><span class="sxs-lookup"><span data-stu-id="05581-123">You can create whatever reports you like with your LinkedIn Sales Navigator data.</span></span> <span data-ttu-id="05581-124">เพื่อให้สิ่งต่างๆ ง่ายขึ้น นอกจากนี้ยังมีไฟล์ .PBIX ของ LinkedIn Sales Navigator ที่คุณดาวน์โหลดได้ซึ่งมีข้อมูลตัวอย่างอยู่แล้ว ดังนั้นคุณจึงทำความคุ้นเคยกับข้อมูลและรายงานได้โดยไม่ต้องเริ่มต้นใหม่</span><span class="sxs-lookup"><span data-stu-id="05581-124">To make things easier, there is also a LinkedIn Sales Navigator .PBIX file that you can download, that has sample data already provided, so you can get familiar with the data and the reports, without having to start from scratch.</span></span>

<span data-ttu-id="05581-125">คุณดาวน์โหลดไฟล์ .PBIX ได้จากตำแหน่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="05581-125">You can download the PBIX file from the following location:</span></span>
* [<span data-ttu-id="05581-126">PBIX for LinkedIn Sales Navigator</span><span class="sxs-lookup"><span data-stu-id="05581-126">PBIX for LinkedIn Sales Navigator</span></span>](service-template-apps-samples.md)

<span data-ttu-id="05581-127">นอกเหนือจากไฟล์ .PBIX แล้ว LinkedIn Sales Navigator ยังมีแอปแม่แบบที่คุณดาวน์โหลดและใช้งานได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="05581-127">In addition to the PBIX file, the LinkedIn Sales Navigator also has a template app that you can download and use, too.</span></span> <span data-ttu-id="05581-128">หัวข้อถัดไปจะอธิบายเกี่ยวกับแอปแม่แบบอย่างละเอียด</span><span class="sxs-lookup"><span data-stu-id="05581-128">The next section describes the template app in detail.</span></span>


## <a name="using-the-linkedin-sales-navigator-template-app"></a><span data-ttu-id="05581-129">การใช้แอปแม่แบบ LinkedIn Sales Navigator</span><span class="sxs-lookup"><span data-stu-id="05581-129">Using the LinkedIn Sales Navigator template app</span></span>

<span data-ttu-id="05581-130">หากต้องการใช้ **LinkedIn Sales Navigator** ให้ง่ายที่สุด คุณจะใช้ [แอปแม่แบบ](service-template-apps-overview.md)ที่สร้างรายงานพร้อมใช้โดยอัตโนมัติจากข้อมูล LinkedIn Sales Navigator ได้</span><span class="sxs-lookup"><span data-stu-id="05581-130">To make using the **LinkedIn Sales Navigator** as easy as possible, you can use the [template app](service-template-apps-overview.md) that automatically creates a ready-made report from your LinkedIn Sales Navigator data.</span></span>

![แอปแม่แบบสำหรับ LinkedIn Sales Navigator](media/desktop-connect-linkedin-sales-navigator/linkedin-sales-navigator-10.png)

<span data-ttu-id="05581-132">เมื่อดาวน์โหลดแอป คุณเลือกว่าจะเชื่อมต่อกับข้อมูลของคุณหรือสำรวจแอปด้วยข้อมูลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="05581-132">When you download the app, you can select whether to connect to your data, or explore the app with sample data.</span></span> <span data-ttu-id="05581-133">คุณย้อนกลับและเชื่อมต่อกับข้อมูล LinkedIn Sales Navigator ของคุณเองหลังจากที่คุณสำรวจข้อมูลตัวอย่างได้เสมอ</span><span class="sxs-lookup"><span data-stu-id="05581-133">You can always go back and connect to your own LinkedIn Sales Navigator data after you explore the sample data.</span></span> 

![เชื่อมต่อข้อมูลสำหรับ LinkedIn Sales Navigator](media/desktop-connect-linkedin-sales-navigator/linkedin-sales-navigator-11.png)



<span data-ttu-id="05581-135">คุณดาวน์โหลดแอปแม่แบบ **LinkedIn Sales Navigator** ได้จากลิงก์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="05581-135">You can get the **LinkedIn Sales Navigator** template app from the following link:</span></span>
* [<span data-ttu-id="05581-136">แอปแม่แบบ LinkedIn Sales Navigator</span><span class="sxs-lookup"><span data-stu-id="05581-136">LinkedIn Sales Navigator template app</span></span>](https://appsource.microsoft.com/en-us/product/power-bi/pbi-contentpacks.linkedin_navigator)

<span data-ttu-id="05581-137">แอปแม่แบบจะมีแท็บ 4 แบบเพื่อช่วยวิเคราะห์และแชร์ข้อมูลของคุณ ดังนี้</span><span class="sxs-lookup"><span data-stu-id="05581-137">The template app provides four tabs to help analyze and share your information:</span></span>

* <span data-ttu-id="05581-138">การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="05581-138">Usage</span></span>
* <span data-ttu-id="05581-139">Search</span><span class="sxs-lookup"><span data-stu-id="05581-139">Search</span></span>
* <span data-ttu-id="05581-140">InMail</span><span class="sxs-lookup"><span data-stu-id="05581-140">InMail</span></span>
* <span data-ttu-id="05581-141">SSI</span><span class="sxs-lookup"><span data-stu-id="05581-141">SSI</span></span>

<span data-ttu-id="05581-142">แท็บ **การใช้งาน** จะแสดงข้อมูล LinkedIn Sales Navigator โดยรวมของคุณ</span><span class="sxs-lookup"><span data-stu-id="05581-142">The **Usage** tab shows your overall LinkedIn Sales Navigator data.</span></span>

![แท็บการใช้งาน LinkedIn Sales Navigator จะแสดงข้อมูล LinkedIn Sales Navigator โดยรวมของคุณ](media/desktop-connect-linkedin-sales-navigator/linkedin-sales-navigator-12.png)

<span data-ttu-id="05581-144">แท็บ **ค้นหา** จะช่วยให้คุณดูผลลัพธ์การค้นหาได้ละเอียดยิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="05581-144">The **Search** tab lets you drill deeper into your search results:</span></span>

![แท็บค้นหา LinkedIn Sales Navigator](media/desktop-connect-linkedin-sales-navigator/linkedin-sales-navigator-13.png)

<span data-ttu-id="05581-146">**InMail** ให้ข้อมูลเชิงลึกเกี่ยวกับการใช้งาน InMail รวมถึงจำนวนการส่ง InMail อัตราการยอมรับ และข้อมูลอื่นๆ ที่เป็นประโยชน์</span><span class="sxs-lookup"><span data-stu-id="05581-146">The **InMail** provides insights into your InMail usage, including number of InMails sent, acceptance rates, and other useful information:</span></span>

![แท็บ InMail LinkedIn Sales Navigator](media/desktop-connect-linkedin-sales-navigator/linkedin-sales-navigator-14.png)

<span data-ttu-id="05581-148">แท็บ **SSI** ให้รายละเอียดเพิ่มเติมเกี่ยวกับดัชนีการขายทางสังคม (SSI)</span><span class="sxs-lookup"><span data-stu-id="05581-148">The **SSI** tab provides additional details into your social selling index (SSI):</span></span>

![แท็บ SSI LinkedIn Sales Navigator](media/desktop-connect-linkedin-sales-navigator/linkedin-sales-navigator-15.png)

<span data-ttu-id="05581-150">หากต้องการเปลี่ยนจากข้อมูลตัวอย่างปเป็นข้อมูลของคุณเอง ให้เลือก **แก้ไขแอป** ที่มุมขวาบน (ไอคอนดินสอ) และเลือก **เชื่อมต่อข้อมูล** จากหน้าจอที่ปรากฎขึ้น</span><span class="sxs-lookup"><span data-stu-id="05581-150">To go from the sample data to your own data, select **edit app** in the top-right corner (the pencil icon) and then select **Connect your data** from the screen that appears.</span></span>

![เชื่อมต่อข้อมูลของคุณ](media/desktop-connect-linkedin-sales-navigator/linkedin-sales-navigator-16.png)

<span data-ttu-id="05581-152">จากตรงนี้ คุณจะเชื่อมต่อข้อมูลของคุณได้โดยเลือกจำนวนวันของข้อมูลที่จะโหลด</span><span class="sxs-lookup"><span data-stu-id="05581-152">From there you can connect your own data, selecting how many days of data to load.</span></span> <span data-ttu-id="05581-153">คุณโหลดข้อมูลได้สูงสุดถึง 365 วัน</span><span class="sxs-lookup"><span data-stu-id="05581-153">You can load up to 365 days of data.</span></span> <span data-ttu-id="05581-154">คุณจะต้องลงชื่อเข้าใช้และใช้อีเมลเดิมที่คุณใช้ลงชื่อเข้าใช้ LinkedIn Sales Navigator ผ่านเว็บไซต์อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="05581-154">You'll need to sign in, again using the same email address you use to sign in to LinkedIn Sales Navigator through the website.</span></span> 

![เข้าสู่ระบบ](media/desktop-connect-linkedin-sales-navigator/linkedin-sales-navigator-17.png)

<span data-ttu-id="05581-156">แอปแม่แบบ จากนั้นรีเฟรชข้อมูลในแอปด้วยข้อมูลข้องคุณ</span><span class="sxs-lookup"><span data-stu-id="05581-156">the template app then refreshes the data in the app with your data.</span></span> <span data-ttu-id="05581-157">คุณยังตั้งค่าการรีเฟรชตามกำหนดการได้เพื่อให้ข้อมูลในแอปเป็นปัจจุบันตามความถี่การรีเฟรชที่คุณระบุ</span><span class="sxs-lookup"><span data-stu-id="05581-157">You can also set up a scheduled refresh, so the data in your app is as current as your refresh frequency specifies.</span></span> 

<span data-ttu-id="05581-158">เมื่อข้อมูลอัปเดต คุณจะเห็นข้อมูลของคุณปรากฎในแอป</span><span class="sxs-lookup"><span data-stu-id="05581-158">Once the data updates, you can see the app populated with your own data.</span></span>

## <a name="getting-help"></a><span data-ttu-id="05581-159">การขอความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="05581-159">Getting help</span></span>

<span data-ttu-id="05581-160">หากคุณประสบปัญหาเมื่อเชื่อมต่อกับข้อมูลของคุณ คุณสามารถติดต่อฝ่ายสนับสนุน LinkedIn Sales Navigator ได้ที่ https://www.linkedin.com/help/sales-navigator</span><span class="sxs-lookup"><span data-stu-id="05581-160">If you run into problems when connecting to your data, you can contact LinkedIn Sales Navigator support at https://www.linkedin.com/help/sales-navigator.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="05581-161">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="05581-161">Next steps</span></span>
<span data-ttu-id="05581-162">มีข้อมูลหลากหลายประเภทที่คุณสามารถเชื่อมต่อโดยใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="05581-162">There are all sorts of data you can connect to using Power BI Desktop.</span></span> <span data-ttu-id="05581-163">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแหล่งข้อมูล โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="05581-163">For more information on data sources, check out the following resources:</span></span>

* [<span data-ttu-id="05581-164">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="05581-164">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="05581-165">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="05581-165">Data Sources in Power BI Desktop</span></span>](desktop-data-sources.md)
* [<span data-ttu-id="05581-166">จัดรูปทรง และรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="05581-166">Shape and Combine Data with Power BI Desktop</span></span>](desktop-shape-and-combine-data.md)
* [<span data-ttu-id="05581-167">เชื่อมต่อกับเวิร์กบุ๊ก Excel ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="05581-167">Connect to Excel workbooks in Power BI Desktop</span></span>](desktop-connect-excel.md)   
* [<span data-ttu-id="05581-168">ใส่ข้อมูลลงใน Power BI Desktop โดยตรง</span><span class="sxs-lookup"><span data-stu-id="05581-168">Enter data directly into Power BI Desktop</span></span>](desktop-enter-data-directly-into-desktop.md)   
