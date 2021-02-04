---
title: เริ่มต้นใช้งานด่วน เชื่อมต่อกับข้อมูลใน Power BI Desktop
description: วิธีการเชื่อมต่อกับแหล่งข้อมูลที่พร้อมใช้งานใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: quickstart
ms.date: 01/10/2020
LocalizationGroup: quickstart
ms.openlocfilehash: 94bd9d64ae7e85cb66e20ad44a03bf4ccf7e28df
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411068"
---
# <a name="quickstart-connect-to-data-in-power-bi-desktop"></a><span data-ttu-id="16c3c-103">เริ่มต้นใช้งานด่วน: เชื่อมต่อกับข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="16c3c-103">Quickstart: Connect to data in Power BI Desktop</span></span>

<span data-ttu-id="16c3c-104">ในเริ่มต้นใช้งานด่วนนี้ คุณเชื่อมต่อกับข้อมูลโดยใช้ Power BI Desktop ซึ่งเป็นขั้นตอนแรกในการสร้างรูปแบบข้อมูล และสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="16c3c-104">In this quickstart, you connect to data using Power BI Desktop, which is the first step in building data models and creating reports.</span></span>

![Power BI Desktop](media/desktop-what-is-desktop/what-is-desktop_01.png)

<span data-ttu-id="16c3c-106">ถ้าคุณไม่ได้ลงทะเบียน Power BI ให้[ลงทะเบียนรุ่นทดลองใช้ฟรี](https://app.powerbi.com/signupredirect?pbi_source=web)ก่อนที่คุณจะเริ่มต้นใช้งาน</span><span class="sxs-lookup"><span data-stu-id="16c3c-106">If you're not signed up for Power BI, [sign up for a free trial](https://app.powerbi.com/signupredirect?pbi_source=web) before you begin.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="16c3c-107">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="16c3c-107">Prerequisites</span></span>

<span data-ttu-id="16c3c-108">เพื่อทำตามขั้นตอนในบทความนี้ คุณจำเป็นต้องมีทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="16c3c-108">To complete the steps in this article, you need the following resources:</span></span>

* <span data-ttu-id="16c3c-109">ดาวน์โหลด และติดตั้ง Power BI Desktop ซึ่งเป็นโปรแกรมประยุกต์ฟรีที่ทำงานบนคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="16c3c-109">Download and install Power BI Desktop, which is a free application that runs on your local computer.</span></span> <span data-ttu-id="16c3c-110">คุณสามารถ[ดาวน์โหลด Power BI Desktop](https://powerbi.microsoft.com/desktop) ได้โดยตรง หรือคุณสามารถดาวน์โหลดได้จาก [Microsoft Store](https://aka.ms/pbidesktopstore) ได้</span><span class="sxs-lookup"><span data-stu-id="16c3c-110">You can [download Power BI Desktop](https://powerbi.microsoft.com/desktop) directly, or you can get it from [the Microsoft Store](https://aka.ms/pbidesktopstore).</span></span>
* <span data-ttu-id="16c3c-111">[ดาวน์โหลดเวิร์กบุ๊ก Excel ตัวอย่างนี้](https://go.microsoft.com/fwlink/?LinkID=521962) และสร้างโฟลเดอร์ที่ชื่อว่า *C:\PBID-qs* ซึ่งคุณสามารถเก็บไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="16c3c-111">[Download this sample Excel workbook](https://go.microsoft.com/fwlink/?LinkID=521962), and create a folder called *C:\PBID-qs* where you can store the Excel file.</span></span> <span data-ttu-id="16c3c-112">ขั้นตอนต่อ ๆ ไปในเริ่มต้นใช้งานด่วนนี้ ถือว่า นั่นคือตำแหน่งที่ตั้งไฟล์สำหรับเวิร์กบุ๊ก Excel ที่ดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="16c3c-112">Later steps in this quickstart assume that is the file location for the downloaded Excel workbook.</span></span>
* <span data-ttu-id="16c3c-113">สำหรับตัวเชื่อมต่อข้อมูลจำนวนมากใน Power BI Desktop จำเป็นต้องใช้ Internet Explorer 10 (หรือใหม่กว่า) สำหรับการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="16c3c-113">For many data connectors in Power BI Desktop, Internet Explorer 10 (or newer) is required for authentication.</span></span>

## <a name="launch-power-bi-desktop"></a><span data-ttu-id="16c3c-114">เปิดใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="16c3c-114">Launch Power BI Desktop</span></span>

<span data-ttu-id="16c3c-115">เมื่อคุณติดตั้ง Power BI Desktop แล้ว เปิดใช้แอปพลิเคชันเพื่อให้ทำงานบนคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="16c3c-115">Once you install Power BI Desktop, launch the application so it's running on your local computer.</span></span> <span data-ttu-id="16c3c-116">คุณจะเห็นบทช่วยสอน Power BI</span><span class="sxs-lookup"><span data-stu-id="16c3c-116">You're presented with a Power BI tutorial.</span></span> <span data-ttu-id="16c3c-117">ทำตามบทช่วยสอนหรือปิดกล่องโต้ตอบเพื่อเริ่มต้นด้วยพื้นที่ทำงานว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="16c3c-117">Follow the tutorial or close the dialog to start with a blank canvas.</span></span> <span data-ttu-id="16c3c-118">พื้นที่ทำงานคือพื้นที่ที่คุณสามารถสร้างวิชวลและรายงานต่าง ๆ จากข้อมูลของคุณได้</span><span class="sxs-lookup"><span data-stu-id="16c3c-118">The canvas is where you create visuals and reports from your data.</span></span>

![Power BI Desktop พร้อมพื้นที่ทำงานว่างเปล่า](media/desktop-quickstart-connect-to-data/qs-connect-data_01.png)

## <a name="connect-to-data"></a><span data-ttu-id="16c3c-120">เชื่อมต่อกับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="16c3c-120">Connect to data</span></span>

<span data-ttu-id="16c3c-121">ด้วย Power BI Desktop คุณสามารถเชื่อมต่อกับข้อมูลประเภทต่าง ๆ มากมาย</span><span class="sxs-lookup"><span data-stu-id="16c3c-121">With Power BI Desktop, you can connect to many different types of data.</span></span> <span data-ttu-id="16c3c-122">แหล่งข้อมูลเหล่านี้ หมายรวมถึงแหล่งข้อมูลพื้นฐาน เช่น ไฟล์ Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="16c3c-122">These sources include basic data sources, such as a Microsoft Excel file.</span></span> <span data-ttu-id="16c3c-123">คุณสามารถเชื่อมต่อกับบริการออนไลน์ที่ประกอบด้วยข้อมูลทุกประเภท เช่น Salesforce, Microsoft Dynamics, Azure Blob Storage และอื่น ๆ อีกมากมาย</span><span class="sxs-lookup"><span data-stu-id="16c3c-123">You can connect to online services that contain all sorts of data, such as Salesforce, Microsoft Dynamics, Azure Blob Storage, and many more.</span></span>

<span data-ttu-id="16c3c-124">เพื่อเชื่อมต่อกับข้อมูล ไปที่ ribbon **หน้าแรก** และเลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="16c3c-124">To connect to data, from the **Home** ribbon select **Get Data**.</span></span>

![รับข้อมูลบน ribbon หน้าหลัก](media/desktop-quickstart-connect-to-data/qs-connect-data_02.png)

<span data-ttu-id="16c3c-126">หน้าต่าง **รับข้อมูล** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="16c3c-126">The **Get Data** window appears.</span></span> <span data-ttu-id="16c3c-127">คุณสามารถเลือกได้จากแหล่งข้อมูลหลายประเภทมามกมายที่ Power BI Desktop สามารถเชื่อมต่อด้วยได้</span><span class="sxs-lookup"><span data-stu-id="16c3c-127">You can choose from the many different data sources to which Power BI Desktop can connect.</span></span> <span data-ttu-id="16c3c-128">ในเริ่มต้นใช้งานด่วนนี้ ให้ใชเวิร์กบุ๊ก Excel ที่คุณดาวน์โหลดใน [ข้อกำหนดเบื้องต้น](#prerequisites)</span><span class="sxs-lookup"><span data-stu-id="16c3c-128">In this quickstart, use the Excel workbook that you downloaded in [Prerequisites](#prerequisites).</span></span>

![รับข้อมูลจากแหล่งข้อมูลทั้งหมด](media/desktop-quickstart-connect-to-data/qs-connect-data_03.png)

<span data-ttu-id="16c3c-130">เนื่องจากแหล่งข้อมูลนี้เป็นไฟล์ Excel ให้เลือก **Excel** จากหน้าต่าง **รับข้อมูล** จากนั้น เลือกปุ่ม **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="16c3c-130">Since this data source is an Excel file, select **Excel** from the **Get Data** window, then select the **Connect** button.</span></span>

<span data-ttu-id="16c3c-131">Power BI จะแจ้งให้คุณระบุตำแหน่งที่ตั้งของไฟล์ Excel ที่ต้องการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="16c3c-131">Power BI prompts you to provide the location of the Excel file to which to connect.</span></span> <span data-ttu-id="16c3c-132">ไฟล์ที่ดาวน์โหลดจะเรียกว่า *ตัวอย่างทางการเงิน*</span><span class="sxs-lookup"><span data-stu-id="16c3c-132">The downloaded file is called *Financial Sample*.</span></span> <span data-ttu-id="16c3c-133">เลือกไฟล์ดังกล่าว จากนั้น เลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="16c3c-133">Select that file, and then select **Open**.</span></span>

![รับข้อมูลในตัวอย่างทางการเงิน](media/desktop-quickstart-connect-to-data/qs-connect-data_04.png)

<span data-ttu-id="16c3c-135">จากนั้น Power BI Desktop จะโหลดเวิร์กบุ๊กและอ่านเนื้อหาของตนเอง และแสดงข้อมูลที่มีอยู่ในไฟล์โดยใช้หน้าต่าง **ตัวนำทาง**</span><span class="sxs-lookup"><span data-stu-id="16c3c-135">Power BI Desktop then loads the workbook and reads its contents, and shows you the available data in the file using the **Navigator** window.</span></span> <span data-ttu-id="16c3c-136">ในหน้าต่างดังกล่าว คุณสามารถเลือกข้อมูลที่คุณต้องการโหลดไปยัง Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="16c3c-136">In that window, you can choose which data you would like to load into Power BI Desktop.</span></span> <span data-ttu-id="16c3c-137">เลือกตารางดังกล่าวโดยกาที่กล่องกาเครื่องหมายข้างแต่ละตารางที่คุณต้องการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="16c3c-137">Select the tables by marking the checkboxes beside each table you want to import.</span></span> <span data-ttu-id="16c3c-138">นำเข้าตารางที่พร้อมใช้งานทั้งคู่</span><span class="sxs-lookup"><span data-stu-id="16c3c-138">Import both available tables.</span></span>

![เลือกข้อมูลในหน้าต่างตัวนำทาง](media/desktop-quickstart-connect-to-data/qs-connect-data_05.png)

<span data-ttu-id="16c3c-140">เมื่อคุณเลือกเสร็จแล้ว เลือก **โหลด** เพื่อนำเข้าข้อมูลลงใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="16c3c-140">Once you've made your selections, select **Load** to import the data into Power BI Desktop.</span></span>

## <a name="view-data-in-the-fields-pane"></a><span data-ttu-id="16c3c-141">ดูข้อมูลในบานหน้าต่างเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="16c3c-141">View data in the Fields pane</span></span>

<span data-ttu-id="16c3c-142">เมื่อคุณโหลดตารางเสร็จ บานหน้าต่าง **เขตข้อมูล** จะแสดงข้อมูลให้คุณ</span><span class="sxs-lookup"><span data-stu-id="16c3c-142">Once you've loaded the tables, the **Fields** pane shows you the data.</span></span> <span data-ttu-id="16c3c-143">คุณสามารถขยายแต่ละตารางโดยเลือกที่ลูกศรข้างชื่อ</span><span class="sxs-lookup"><span data-stu-id="16c3c-143">You can expand each table by selecting the arrow beside its name.</span></span> <span data-ttu-id="16c3c-144">ในรูปต่อไปนี้ ตาราง *financials* ถูกขยาย แสดงแต่ละเขตข้อมูลของตารางนั้น</span><span class="sxs-lookup"><span data-stu-id="16c3c-144">In the following image, the *financials* table is expanded, showing each of its fields.</span></span>

![รับข้อมูล](media/desktop-quickstart-connect-to-data/qs-connect-data_06.png)

<span data-ttu-id="16c3c-146">เท่านี้ก็เรียบร้อย!</span><span class="sxs-lookup"><span data-stu-id="16c3c-146">And that's it!</span></span> <span data-ttu-id="16c3c-147">คุณได้เชื่อมต่อกับข้อมูลใน Power BI Desktop โหลดข้อมูลนั้น และตอนนี้ คุณเห็นเขตข้อมูลทั้งหมดที่มีในตารางเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="16c3c-147">You've connected to data in Power BI Desktop, loaded that data, and now you can see all the available fields within those tables.</span></span>

## <a name="next-steps"></a><span data-ttu-id="16c3c-148">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="16c3c-148">Next steps</span></span>

<span data-ttu-id="16c3c-149">คุณสามารถทำอะไรได้มากมายด้วย Power BI Desktop เมื่อคุณเชื่อมต่อกับข้อมูลแล้ว</span><span class="sxs-lookup"><span data-stu-id="16c3c-149">There are all sorts of things you can do with Power BI Desktop once you've connected to data.</span></span> <span data-ttu-id="16c3c-150">เช่น การสร้างวิชวลและรายงาน</span><span class="sxs-lookup"><span data-stu-id="16c3c-150">You can create visuals and reports.</span></span> <span data-ttu-id="16c3c-151">ลองดูที่ทรัพยากรต่อไปนี้เพื่อช่วยคุณเริ่มต้น:</span><span class="sxs-lookup"><span data-stu-id="16c3c-151">Take a look at the following resource to get you going:</span></span>

* [<span data-ttu-id="16c3c-152">เริ่มต้นใช้งาน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="16c3c-152">Get started with Power BI Desktop</span></span>](../fundamentals/desktop-getting-started.md)
