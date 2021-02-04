---
title: สร้างรายงานบนรายการ SharePoint
description: บทช่วยสอนนี้แสดงวิธีการแปลงข้อมูลในรายการ SharePoint ของคุณลงในรายงาน Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 01/10/2020
LocalizationGroup: Visualizations
ms.openlocfilehash: 5347405c13f71fa0932c48eb218618b28a9f03c8
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96404536"
---
# <a name="create-a-report-on-a-sharepoint-list"></a><span data-ttu-id="c7e01-103">สร้างรายงานบนรายการ SharePoint</span><span class="sxs-lookup"><span data-stu-id="c7e01-103">Create a report on a SharePoint List</span></span>

<span data-ttu-id="c7e01-104">ทีมและองค์กรจำนวนมากใช้รายการใน SharePoint Online เพื่อจัดเก็บข้อมูลเนื่องจากง่ายต่อการตั้งค่าและทำให้ผู้ใช้สามารถอัปเดตได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="c7e01-104">Many teams and organizations use Lists in SharePoint Online to store data because it's easy to set up and easy for users to update.</span></span>  <span data-ttu-id="c7e01-105">บางครั้งการใช้แผนภูมิเป็นแนวทางที่ง่ายกว่ามากสำหรับผู้ใช้เพื่อทำความเข้าใจข้อมูลอย่างรวดเร็วแทนที่จะดูตัวรายการเอง</span><span class="sxs-lookup"><span data-stu-id="c7e01-105">Sometimes a chart is a much easier way for users to quickly understand the data rather than looking at the list itself.</span></span> <span data-ttu-id="c7e01-106">ในบทช่วยสอนนี้ เราจะแสดงวิธีการแปลงข้อมูลในรายการ SharePoint ของคุณลงในรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="c7e01-106">In this tutorial, we show how to transform your SharePoint List data into a Power BI report.</span></span>

<span data-ttu-id="c7e01-107">ดูวิดีโอบทช่วยสอนห้านาทีนี้ หรือเลื่อนลงเพื่อดูคำแนะนำทีละขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="c7e01-107">Watch this five-minute tutorial video, or scroll down for step-by-step instructions.</span></span>

<iframe width="400" height="450" src="https://www.youtube.com/embed/OZO3x2NF8Ak" frameborder="0" allowfullscreen></iframe>

## <a name="part-1-connect-to-your-sharepoint-list"></a><span data-ttu-id="c7e01-108">ส่วนที่ 1: เชื่อมต่อไปยังรายการ SharePoint ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7e01-108">Part 1: Connect to your SharePoint List</span></span>

1. <span data-ttu-id="c7e01-109">หากคุณยังไม่มี ให้ดาวน์โหลดและติดตั้ง [Power BI Desktop](https://powerbi.microsoft.com/desktop/)</span><span class="sxs-lookup"><span data-stu-id="c7e01-109">If you don't have it already, download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span></span>
2. <span data-ttu-id="c7e01-110">เปิด Power BI Desktop และในแท็บหน้าแรกของริบบอน ให้เลือก **รับข้อมูล** > **เพิ่มเติม**</span><span class="sxs-lookup"><span data-stu-id="c7e01-110">Open Power BI Desktop and in the Home tab of the ribbon, select **Get Data** > **More**.</span></span>
3. <span data-ttu-id="c7e01-111">เลือก **บริการออนไลน์** จากนั้นเลือก **รายการ SharePoint Online**</span><span class="sxs-lookup"><span data-stu-id="c7e01-111">Select **Online Services**, then select **SharePoint Online List**.</span></span>  

    <img src="media/desktop-sharepoint-online-list/desktop-sharepoint-online-list-getdata.png" alt="Screenshot shows the Get Data dialog box with Online Services selected." width="350"/>

4. <span data-ttu-id="c7e01-112">เลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="c7e01-112">Select **Connect**.</span></span>
4. <span data-ttu-id="c7e01-113">ค้นหาที่อยู่ (หรือที่เรียกว่า URL) ของเว็บไซต์ SharePoint Online ที่มีรายการของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7e01-113">Find the address (also known as a URL) of your SharePoint Online site that contains your list.</span></span>  <span data-ttu-id="c7e01-114">จากหน้าเพจหนึ่งใน SharePoint Online โดยทั่วไปคุณสามารถรับที่อยู่ของไซต์ได้จากการเลือก **หน้าหลัก** ในบานหน้าต่างนำทาง หรือไอคอนสำหรับไซต์ที่ด้านบน จากนั้นคัดลอกที่อยู่จากแถบที่อยู่ของเว็บเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="c7e01-114">From a page in SharePoint Online, you can usually get the site address by selecting **Home** in the navigation pane, or the icon for the site at the top, then copying the address from your web browser's address bar.</span></span>

   <span data-ttu-id="c7e01-115">ดูวิดีโอของขั้นตอนนี้:</span><span class="sxs-lookup"><span data-stu-id="c7e01-115">Watch a video of this step:</span></span>
   <iframe width="400" height="300" src="https://www.youtube.com/embed/OZO3x2NF8Ak?start=48&end=90" frameborder="0" allowfullscreen></iframe>

5. <span data-ttu-id="c7e01-116">ใน Power BI Desktop ให้วางที่อยู่ลงในเขตข้อมูล **URL ของไซต์** ในกล่องโต้ตอบ open (เปิด)</span><span class="sxs-lookup"><span data-stu-id="c7e01-116">In Power BI Desktop, paste the address into the **Site URL** field in the open dialog box.</span></span>

6. <span data-ttu-id="c7e01-117">คุณอาจหรืออาจไม่เห็นหน้าจอการเข้าถึง SharePoint เหมือนรูปภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c7e01-117">You may or may not see a SharePoint access screen like the following image.</span></span>  <span data-ttu-id="c7e01-118">หากคุณไม่เห็น ให้ข้ามไปยังขั้นตอนที่ 10</span><span class="sxs-lookup"><span data-stu-id="c7e01-118">If you don't see it, skip to step 10.</span></span>  <span data-ttu-id="c7e01-119">หากคุณเห็น ให้เลือก **บัญชี Microsoft** ทางด้านซ้ายของหน้า</span><span class="sxs-lookup"><span data-stu-id="c7e01-119">If you do see it, select **Microsoft Account** on the left side of the page.</span></span>

    <img src="media/desktop-sharepoint-online-list/desktop-sharepoint-online-list-auth1.png" alt="choose Microsoft account" width="500"/>

7. <span data-ttu-id="c7e01-120">เลือก **ลงชื่อเข้าใช้** และป้อนชื่อผู้ใช้และรหัสผ่านที่คุณใช้ในการลงชื่อเข้าใช้ Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="c7e01-120">Select **Sign In** and enter the user name and password you use to sign in to Microsoft 365.</span></span>

    <img src="media/desktop-sharepoint-online-list/desktop-sharepoint-online-list-auth2.png" alt="sign in" width="500"/>

8. <span data-ttu-id="c7e01-121">เมื่อคุณเสร็จสิ้นการลงชื่อเข้าใช้ ให้เลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="c7e01-121">When you finish signing in, select **Connect**.</span></span>

9. <span data-ttu-id="c7e01-122">ที่ด้านซ้ายของตัวนำทาง ให้เลือกกล่องกาเครื่องหมายข้างรายการ SharePoint ที่คุณต้องการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="c7e01-122">On the left side of the Navigator, select the checkbox beside the SharePoint list you want to connect to.</span></span>

    <img src="media/desktop-sharepoint-online-list/desktop-sharepoint-online-list-select-list.png" alt="Screenshot shows the Navigator page with BudgetRequests selected." width="450"/>

10. <span data-ttu-id="c7e01-123">เลือก **โหลด**</span><span class="sxs-lookup"><span data-stu-id="c7e01-123">Select **Load**.</span></span>  <span data-ttu-id="c7e01-124">Power BI โหลดข้อมูลรายการของคุณลงในรายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="c7e01-124">Power BI loads your list data into a new report.</span></span>

## <a name="part-2-create-a-report"></a><span data-ttu-id="c7e01-125">ส่วนที่ 2: สร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="c7e01-125">Part 2: Create a report</span></span>

1. <span data-ttu-id="c7e01-126">ทางด้านซ้าย ให้เลือกไอคอน **ข้อมูล** เพื่อดูว่ามีการโหลดข้อมูลรายการ SharePoint ของคุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="c7e01-126">On the left side, select the **Data** icon to see that your SharePoint list data was loaded.</span></span>

2. <span data-ttu-id="c7e01-127">ตรวจสอบให้แน่ใจว่าคอลัมน์รายการที่มีตัวเลขแสดงไอคอน Sum หรือ Sigma ใน **บานหน้าต่างเขตข้อมูล** ทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="c7e01-127">Make sure your list columns with numbers show the Sum, or Sigma, icon in the **Fields pane** on the right.</span></span>  <span data-ttu-id="c7e01-128">หากไม่มีสิ่งใด ให้เลือกส่วนหัวของคอลัมน์ในมุมมองตาราง จากนั้นเลือกแท็บ **การสร้างแบบจำลอง** จากนั้นเปลี่ยน **ชนิดข้อมูล** เป็น **จำนวนทศนิยม** หรือ **จำนวนเต็ม** ทั้งนี้ขึ้นอยู่กับข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7e01-128">For any that don't, select the column header in the table view, select the **Modeling** tab, then change the **Data type** to **Decimal Number** or **Whole Number**, depending on the data.</span></span>  <span data-ttu-id="c7e01-129">ถ้าได้รับพร้อมท์ให้ยืนยันการเปลี่ยนแปลงของคุณ ให้เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="c7e01-129">If prompted to confirm your change, select **Yes**.</span></span>  <span data-ttu-id="c7e01-130">ถ้าตัวเลขของคุณเป็นรูปแบบพิเศษ เช่น สกุลเงิน คุณยังสามารถเลือกได้จากการตั้งค่า **รูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="c7e01-130">If your number is a special format, like currency, you can also choose that by setting the **Format**.</span></span>

   <span data-ttu-id="c7e01-131">ดูวิดีโอของขั้นตอนนี้:</span><span class="sxs-lookup"><span data-stu-id="c7e01-131">Watch a video of this step:</span></span>
   <iframe width="400" height="300" src="https://www.youtube.com/embed/OZO3x2NF8Ak?start=147&end=204" frameborder="0" allowfullscreen></iframe>

3. <span data-ttu-id="c7e01-132">ทางด้านซ้าย ให้เลือกไอคอน **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="c7e01-132">On the left side, select the **Report** icon.</span></span>
4. <span data-ttu-id="c7e01-133">เลือกคอลัมน์ที่คุณต้องการแสดงภาพโดยการเลือกกล่องกาเครื่องหมายด้านข้างบานหน้าต่าง **เขตข้อมูล** ทางด้านขวา</span><span class="sxs-lookup"><span data-stu-id="c7e01-133">Select columns you want to visualize by selecting the checkbox beside them in the **Fields** pane on the right.</span></span>

   <span data-ttu-id="c7e01-134">ดูวิดีโอของขั้นตอนนี้:</span><span class="sxs-lookup"><span data-stu-id="c7e01-134">Watch a video of this step:</span></span>
   <iframe width="400" height="300" src="https://www.youtube.com/embed/OZO3x2NF8Ak?start=215&end=252" frameborder="0" allowfullscreen></iframe>

5. <span data-ttu-id="c7e01-135">เปลี่ยนชนิดของวิชวล ถ้าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="c7e01-135">Change the visual type if you need to.</span></span>
6. <span data-ttu-id="c7e01-136">คุณสามารถสร้างการแสดงผลข้อมูลด้วยภาพหลายรายการในรายงานเดียวกันได้โดยการกดโดยยกเลิกการเลือกวิชวลที่มีอยู่ แล้วเลือกกล่องกาเครื่องหมายสำหรับคอลัมน์อื่นในบานหน้าต่าง **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="c7e01-136">You can create multiple visualizations in the same report by unselecting the existing visual then selecting checkboxes for other columns in the **Fields** pane.</span></span>
7. <span data-ttu-id="c7e01-137">เลือก **บันทึก** เพื่อบันทึกรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7e01-137">Select **Save** to save your report.</span></span>
