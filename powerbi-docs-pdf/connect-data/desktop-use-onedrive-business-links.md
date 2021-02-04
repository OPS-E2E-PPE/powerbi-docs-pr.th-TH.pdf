---
title: ใช้ลิงก์ OneDrive for Business ใน Power BI Desktop
description: ใช้ลิงก์ OneDrive for Business ใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 05/27/2020
LocalizationGroup: Connect to data
ms.openlocfilehash: 70607632dd4e93d1b0d5e53f19ef697c6599128d
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410861"
---
# <a name="use-onedrive-for-business-links-in-power-bi-desktop"></a><span data-ttu-id="ba116-103">ใช้ลิงก์ OneDrive for Business ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ba116-103">Use OneDrive for Business links in Power BI Desktop</span></span>
<span data-ttu-id="ba116-104">หลายคนมีเวิร์กบุ๊ก Excel ที่จัดเก็บไว้ใน OneDrive for Business ที่จะเหมาะสำหรับใช้งานกับ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ba116-104">Many people have Excel workbooks stored in OneDrive for Business that would be great for use with Power BI Desktop.</span></span> <span data-ttu-id="ba116-105">ด้วย Power BI Desktop คุณสามารถใช้ลิงก์ออนไลน์สำหรับไฟล์ Excel ที่จัดเก็บไว้ใน OneDrive for Business เพื่อสร้างรายงานและวิชวลได้</span><span class="sxs-lookup"><span data-stu-id="ba116-105">With Power BI Desktop, you can use online links for Excel files stored in OneDrive for Business to create reports and visuals.</span></span> <span data-ttu-id="ba116-106">คุณสามารถใช้บัญชีผู้ใช้กลุ่ม OneDrive for Business หรือบัญชีผู้ใช้บุคคล OneDrive for Business ของคุณก็ได้</span><span class="sxs-lookup"><span data-stu-id="ba116-106">You can use a OneDrive for Business group account or your individual OneDrive for Business account.</span></span>

<span data-ttu-id="ba116-107">การรับลิงก์ออนไลน์จาก OneDrive for Business ต้องใช้ขั้นตอนที่เฉพาะเจาะจงสองสามขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="ba116-107">Getting an online link from OneDrive for Business requires a few specific steps.</span></span> <span data-ttu-id="ba116-108">ส่วนต่อไปนี้จะอธิบายขั้นตอนดังกล่าว ให้คุณสามารถแชร์ลิงก์ของไฟล์ระหว่างกลุ่ม ระหว่างเครื่อง และกับเพื่อนร่วมงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="ba116-108">The following sections explain those steps, which let you share the file link among groups, across different machines, and with your coworkers.</span></span>

## <a name="get-a-link-from-excel"></a><span data-ttu-id="ba116-109">รับลิงก์จาก Excel</span><span class="sxs-lookup"><span data-stu-id="ba116-109">Get a link from Excel</span></span>
1. <span data-ttu-id="ba116-110">นำทางไปยังที่ตั้ง OneDrive for Business ของคุณโดยใช้เบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="ba116-110">Navigate to your OneDrive for Business location using a browser.</span></span> <span data-ttu-id="ba116-111">คลิกขวาไฟล์ที่คุณต้องการใช้ และเลือก **เปิดใน Excel**</span><span class="sxs-lookup"><span data-stu-id="ba116-111">Right-click the file you want to use, and select **Open in Excel**.</span></span>
   
   > [!NOTE]
   > <span data-ttu-id="ba116-112">อินเทอร์เฟซบนเบราว์เซอร์ของคุณอาจไม่เหมือนรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ba116-112">Your browser interface might not look exactly like the following image.</span></span> <span data-ttu-id="ba116-113">มีหลายวิธีในการเลือก **เปิดใน Excel** สำหรับไฟล์ในอินเทอร์เฟซบนเบราว์เซอร์ OneDrive for Business ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ba116-113">There are many ways to select **Open in Excel** for files in your OneDrive for Business browser interface.</span></span> <span data-ttu-id="ba116-114">คุณสามารถใช้ทางเลือกใด ๆ ที่ทำให้คุณสามารถเปิดไฟล์ใน Excel</span><span class="sxs-lookup"><span data-stu-id="ba116-114">You can use any option that allows you to open the file in Excel.</span></span>
   
   ![ภาพหน้าจอของ OneDrive ในเบราว์เซอร์ ที่แสดงการเลือกเปิดใน Excel](media/desktop-use-onedrive-business-links/odb-links_02.png)

2. <span data-ttu-id="ba116-116">ใน Excel เลือก **ไฟล์** > **ข้อมูล** จากนั้นเลือกปุ่ม **คัดลอกเส้นทาง** ดังที่แสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ba116-116">In Excel, select **File** > **Info**, and then select the **Copy path** button, as shown in the following image.</span></span>
   
   ![ภาพหน้าจอของเมนูข้อมูล ที่แสดงการเลือกปุ่มคัดลอกเส้นทาง](media/desktop-use-onedrive-business-links/onedrive-copy-path.png)

## <a name="use-the-link-in-power-bi-desktop"></a><span data-ttu-id="ba116-118">ใช้ลิงก์ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ba116-118">Use the link in Power BI Desktop</span></span>
<span data-ttu-id="ba116-119">ใน Power BI Desktop คุณสามารถใช้ลิงก์ที่คุณเพิ่งคัดลอกไปยังคลิปบอร์ด</span><span class="sxs-lookup"><span data-stu-id="ba116-119">In Power BI Desktop, you can use the link you just copied to the clipboard.</span></span> <span data-ttu-id="ba116-120">ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ba116-120">Take the following steps:</span></span>

1. <span data-ttu-id="ba116-121">ใน Power BI Desktop ให้เลือก **รับข้อมูล** > **เว็บ**</span><span class="sxs-lookup"><span data-stu-id="ba116-121">In Power BI Desktop, select **Get Data** > **Web**.</span></span>
   
   ![ภาพหน้าจอของริบบอนรับข้อมูลใน Power BI Desktop ที่แสดงการเลือกเว็บ](media/desktop-use-onedrive-business-links/power-bi-web-link-onedrive.png)
2. <span data-ttu-id="ba116-123">ด้วยตัวเลือก **พื้นฐาน** ที่เลือกไว้ วางลิงก์ในกล่องโต้ตอบ **จากเว็บ**</span><span class="sxs-lookup"><span data-stu-id="ba116-123">With the **Basic** option selected, paste the link into the **From Web** dialog box.</span></span>
3. <span data-ttu-id="ba116-124">ลบสตริง *?web=1* ออกที่จุดสิ้นสุดของลิงก์เพื่อให้ Power BI Desktop สามารถนำทางไปยังไฟล์ของคุณอย่างถูกต้อง จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ba116-124">Remove the *?web=1* string at the end of the link so that Power BI Desktop can properly navigate to your file, and then select **OK**.</span></span>
   
    ![ภาพหน้าจอของกล่องโต้ตอบจากเว็บ ที่แสดงวิธีการลบสตริงออกจากเขตข้อมูล URL](media/desktop-use-onedrive-business-links/power-bi-web-link-confirmation.png) 
4. <span data-ttu-id="ba116-126">ถ้า Power BI Desktop พร้อมท์คุณสำหรับข้อมูลประจำตัว เลือก **Windows** (สำหรับไซต์ SharePoint ภายในองค์กร) หรือ **บัญชีองค์กร** (สำหรับ Microsoft 365 หรือ ไซต์ OneDrive for Business) อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ba116-126">If Power BI Desktop prompts you for credentials, choose either **Windows** (for on-premises SharePoint sites) or **Organizational Account** (for Microsoft 365 or OneDrive for Business sites).</span></span>
   
   ![ภาพหน้าจอของพรอมท์ข้อมูลประจำตัวของ Power BI Desktop ที่แสดงการเลือกบัญชีของ Windows หรือองค์กร](media/desktop-use-onedrive-business-links/odb-links_06.png)

   <span data-ttu-id="ba116-128">กล่องโต้ตอบ **ตัวนำทาง** จะปรากฏขึ้น ช่วยให้คุณสามารถเลือกจากรายการของตาราง แผ่นงาน และช่วงที่พบในเวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="ba116-128">A **Navigator** dialog box appears, allowing you to select from the list of tables, sheets, and ranges found in the Excel workbook.</span></span> <span data-ttu-id="ba116-129">จากที่นั่น คุณสามารถใช้ไฟล์ OneDrive for Business เช่นเดียวกับไฟล์ Excel อื่น ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="ba116-129">From there, you can use the OneDrive for Business file just like any other Excel file.</span></span> <span data-ttu-id="ba116-130">คุณสามารถสร้างรายงานและใช้ในชุดข้อมูลได้เช่นเดียวกับที่คุณต้องการกับแหล่งข้อมูลอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="ba116-130">You can create reports and use it in datasets like you would with any other data source.</span></span>

> [!NOTE]
> <span data-ttu-id="ba116-131">หากต้องการใช้ไฟล์ OneDrive for Business เป็นแหล่งข้อมูลในบริการของ Power BI ที่เปิดใช้งาน **การบริการรีเฟรช** สำหรับไฟล์ดังกล่าว ตรวจสอบให้แน่ใจว่า คุณเลือก **OAuth2** เป็น **วิธีการรับรองความถูกต้อง** เมื่อกำหนดค่าการตั้งค่าการรีเฟรชของคุณ</span><span class="sxs-lookup"><span data-stu-id="ba116-131">To use a OneDrive for Business file as a data source in the Power BI service, with **Service Refresh** enabled for that file, make sure you select **OAuth2** as the **Authentication method** when configuring your refresh settings.</span></span> <span data-ttu-id="ba116-132">มิฉะนั้น คุณอาจพบข้อผิดพลาด (เช่น *ไม่สามารถปรับปรุงข้อมูลประจำตัวสำหรับแหล่งข้อมูล*) เมื่อคุณพยายามเชื่อมต่อ หรือรีเฟรชได้</span><span class="sxs-lookup"><span data-stu-id="ba116-132">Otherwise, you may encounter an error (such as, *Failed to update data source credentials*) when you attempt to connect or to refresh.</span></span> <span data-ttu-id="ba116-133">การเลือก **OAuth2** ให้เป็นวิธีการรับรองความถูกต้อง เป็นการแก้ไขข้อผิดพลาดข้อมูลประจำตัวนั้น</span><span class="sxs-lookup"><span data-stu-id="ba116-133">Selecting **OAuth2** as the authentication method remedies that credentials error.</span></span>
>
