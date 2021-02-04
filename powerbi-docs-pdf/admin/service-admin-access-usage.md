---
title: ค้นหาผู้ใช้ Power BI ที่มีการลงชื่อเข้าใช้
description: หากคุณเป็นผู้ดูแลระบบ และต้องการดูบุคคลที่ลงชื่อเข้าใช้ Power BI คุณสามารถใช้รายงานการเข้าถึงและการใช้งานของ Azure Active Directory ได้/
author: kfollis
ms.author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: how-to
ms.date: 09/25/2020
LocalizationGroup: Administration
ms.openlocfilehash: 84d4b0ab295f003c34937084bd93dd6f27992c31
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96409297"
---
# <a name="find-power-bi-users-that-have-signed-in"></a><span data-ttu-id="8018c-103">ค้นหาผู้ใช้ Power BI ที่มีการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="8018c-103">Find Power BI users that have signed in</span></span>

<span data-ttu-id="8018c-104">หากคุณเป็นผู้ดูแลระบบสำหรับองค์กรของคุณ และต้องการดูบุคคลที่ลงชื่อเข้าใช้ Power BI ให้ใช้ [รายงานการเข้าถึงและการใช้งานของ Azure Active Directory](/azure/active-directory/reports-monitoring/concept-sign-ins)</span><span class="sxs-lookup"><span data-stu-id="8018c-104">If you're an admin for your organization, and want to see who has signed into Power BI, use the [Azure Active Directory access and usage reports](/azure/active-directory/reports-monitoring/concept-sign-ins).</span></span>

> [!NOTE]
> <span data-ttu-id="8018c-105">แม้รายงาน **ลงชื่อเข้าใช้** จะให้ข้อมูลที่เป็นประโยชน์ แต่ก็ไม่สามารถระบุประเภทสิทธิการใช้งานที่ผู้ใช้แต่ละคนมีได้</span><span class="sxs-lookup"><span data-stu-id="8018c-105">The **Sign-ins** report provides useful info, but it doesn't identify the type of license for each user.</span></span> <span data-ttu-id="8018c-106">การใช้ศูนย์การจัดการ Microsoft 365 เพื่อดูสิทธิ์การใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8018c-106">Use the Microsoft 365 admin center to view licenses.</span></span>

## <a name="requirements"></a><span data-ttu-id="8018c-107">ข้อกำหนด</span><span class="sxs-lookup"><span data-stu-id="8018c-107">Requirements</span></span>

<span data-ttu-id="8018c-108">ผู้ใช้ทุกคนสามารถดูรายงานการลงชื่อเข้าใช้ของตนเองได้ เมื่อต้องการดูรายงานสำหรับผู้ใช้ทั้งหมด คุณต้องอยู่ในหนึ่งในบทบาทต่อไปนี้: ผู้ดูแลระบบส่วนกลาง, ผู้ดูแลระบบความปลอดภัย, ผู้มีสิทธิ์อ่านระบบความปลอดภัย, ผู้อ่านส่วนกลาง หรือโปรแกรมอ่านรายงาน</span><span class="sxs-lookup"><span data-stu-id="8018c-108">Any user can view a report of their own sign-ins. To see a report for all users you must be in one of the following roles: Global Admin, Security Admin, Security Reader, Global Reader, or Report Reader.</span></span>

## <a name="use-the-azure-active-directory-admin-center-to-view-sign-ins"></a><span data-ttu-id="8018c-109">ใช้ศูนย์การจัดการของผู้ดูแลระบบ Azure Active Directory เพื่อดูการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="8018c-109">Use the Azure Active Directory admin center to view sign-ins</span></span>

<span data-ttu-id="8018c-110">หากต้องการดูกิจกรรมการลงชื่อเข้าใช้ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8018c-110">To view sign-in activity, follow these steps.</span></span>

1. <span data-ttu-id="8018c-111">ลงชื่อเข้าใช้ [ศูนย์การจัดการ Azure Active Directory](https://aad.portal.azure.com) จากนั้นเลือก **Azure Active Directory** จากเมนูพอร์ทัล</span><span class="sxs-lookup"><span data-stu-id="8018c-111">Sign in to the [Azure Active Directory admin center](https://aad.portal.azure.com), then select **Azure Active Directory** from the portal menu.</span></span>

1. <span data-ttu-id="8018c-112">จากเมนูทรัพยากร เลือก **การตรวจสอบ** > **ลงชื่อเข้าใช้**</span><span class="sxs-lookup"><span data-stu-id="8018c-112">From the resource menu, select **Monitoring** > **Sign-ins**.</span></span>
   
    ![สกรีนช็อตของศูนย์การจัดการ Azure Active Directory ซึ่งเน้นตัวเลือกการลงชื่อเข้าใช้ไว้](media/service-admin-access-usage/azure-portal-sign-ins.png)

1. <span data-ttu-id="8018c-114">ตามค่าเริ่มต้น การลงชื่อเข้าใช้ทั้งหมดจาก 24 ชั่วโมงที่ผ่านมาสำหรับผู้ใช้และแอปพลิเคชันทั้งหมดจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="8018c-114">By default, all sign-ins from the last 24 hours for all users and all applications are shown.</span></span> <span data-ttu-id="8018c-115">เมื่อต้องการเลือกช่วงเวลาอื่น ให้เลือก **วันที่** ในบานหน้าต่างการทำงานและเลือกช่วงเวลาที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8018c-115">To select a different time period, select **Date** in the working pane and choose from the available time intervals.</span></span> <span data-ttu-id="8018c-116">สามารถใช้ได้เฉพาะข้อมูลจากเจ็ดวันที่ผ่านมาเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8018c-116">Only info from the last seven days is available.</span></span> <span data-ttu-id="8018c-117">หากต้องการดูเฉพาะการลงชื่อเข้าใช้ Power BI ให้เพิ่มตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="8018c-117">To see only sign-ins to Power BI, add filters.</span></span> <span data-ttu-id="8018c-118">เลือก **เพิ่มตัวกรอง** > เลือก **แอปพลิเคชัน** เป็นเขตข้อมูลที่จะกรองตาม และเลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="8018c-118">Select **Add filter** > pick **Application** as the field to filter by, and select **Apply**.</span></span> <span data-ttu-id="8018c-119">เลือก **แอปพลิเคชันที่ขึ้นต้นด้วย** จากด้านบนของบานหน้าต่างการทำงาน แล้วป้อนชื่อแอป</span><span class="sxs-lookup"><span data-stu-id="8018c-119">Select **Application starts with** from the top of the working pane, and enter the app name.</span></span> <span data-ttu-id="8018c-120">เลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="8018c-120">Select **Apply**.</span></span>

    <span data-ttu-id="8018c-121">**Microsoft Power BI** จะกรองเพื่อลงชื่อเข้าใช้กิจกรรมที่เกี่ยวข้องกับบริการ</span><span class="sxs-lookup"><span data-stu-id="8018c-121">**Microsoft Power BI** filters to sign-in activity related to the service.</span></span> <span data-ttu-id="8018c-122">**Power BI Gateway** จะกรองเพื่อลงชื่อเข้าใช้กิจกรรมเฉพาะเกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="8018c-122">**Power BI Gateway** filters to sign-in activity specific to the on-premises data gateway.</span></span>
   
    ![สกรีนช็อตของตัวกรองลงชื่อเข้าพร้อมด้วยเขตข้อมูลของแอปพลิเคชันที่เน้น](media/service-admin-access-usage/sign-in-filter.png)

## <a name="export-the-data"></a><span data-ttu-id="8018c-124">ส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8018c-124">Export the data</span></span>

<span data-ttu-id="8018c-125">คุณสามารถ[ดาวน์โหลดรายงานลงชื่อเข้าใช้](/azure/active-directory/reports-monitoring/quickstart-download-sign-in-report)ในรูปแบบไฟล์ CSV หรือไฟล์ JSON ได้</span><span class="sxs-lookup"><span data-stu-id="8018c-125">You can [download a sign-in report](/azure/active-directory/reports-monitoring/quickstart-download-sign-in-report) in either of two formats: a CSV file, or a JSON file.</span></span>

1. <span data-ttu-id="8018c-126">จากแถบคำสั่งสำหรับรายงาน **ลงชื่อเข้าใช้** เลือก **ดาวน์โหลด** แล้วเลือกหนึ่งในตัวเลือกต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8018c-126">From the command bar for the **Sign-ins** report, select **Download** and then select one of the following options:</span></span>

   * <span data-ttu-id="8018c-127">**CSV** เพื่อดาวน์โหลดไฟล์ CSV สำหรับข้อมูลที่ถูกกรองในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="8018c-127">**CSV** to download a CSV file for the currently filtered data.</span></span>

   * <span data-ttu-id="8018c-128">**JSON** เพื่อดาวน์โหลดไฟล์ JSON สำหรับข้อมูลที่ถูกกรองในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="8018c-128">**JSON** to download a JSON file for the currently filtered data.</span></span>

2. <span data-ttu-id="8018c-129">พิมพ์ชื่อไฟล์ จากนั้นเลือก **ดาวน์โหลด**</span><span class="sxs-lookup"><span data-stu-id="8018c-129">Type a file name, then select **Download**.</span></span>

![ภาพหน้าจอของการส่งออกข้อมูลพร้อมตัวเลือกการดาวน์โหลดที่ถูกเน้น](media/service-admin-access-usage/download-sign-in-data-csv.png)

## <a name="data-retention"></a><span data-ttu-id="8018c-131">การเก็บรักษาข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8018c-131">Data retention</span></span>

<span data-ttu-id="8018c-132">ข้อมูลที่เกี่ยวข้องกับการลงชื่อเข้าใช้มีได้ถึงเจ็ดวัน เว้นแต่ว่าองค์กรของคุณไม่มีสิทธิ์การใช้งาน Azure AD Premium</span><span class="sxs-lookup"><span data-stu-id="8018c-132">Sign-in-related data is available for up to seven days, unless your organization has an Azure AD premium license.</span></span> <span data-ttu-id="8018c-133">หากคุณกำลังใช้ Azure AD Premium P1 หรือ Azure AD Premium P2 คุณสามารถดูข้อมูลสำหรับ 30 วันที่ผ่านมาได้</span><span class="sxs-lookup"><span data-stu-id="8018c-133">If you're using Azure AD Premium P1 or Azure AD Premium P2, you can see data for the past 30 days.</span></span> <span data-ttu-id="8018c-134">สำหรับข้อมูลเพิ่มเติม ดู[นโยบายการเก็บรักษาข้อมูลรายงานของ Azure Active Directory](/azure/active-directory/reports-monitoring/reference-reports-data-retention)</span><span class="sxs-lookup"><span data-stu-id="8018c-134">For more info, see [Azure Active Directory report retention policies](/azure/active-directory/reports-monitoring/reference-reports-data-retention).</span></span>

## <a name="next-steps"></a><span data-ttu-id="8018c-135">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="8018c-135">Next steps</span></span>

[<span data-ttu-id="8018c-136">ตรวจสอบกิจกรรมของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="8018c-136">Audit user activity</span></span>](service-admin-auditing.md)

<span data-ttu-id="8018c-137">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8018c-137">More questions?</span></span> [<span data-ttu-id="8018c-138">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="8018c-138">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)