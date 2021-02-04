---
title: Power BI เริ่มใช้งานแอปของบริษัทอื่น
description: Power BI เริ่มใช้งานแอปของบริษัทอื่น
author: maggiesMSFT
ms.author: maggies
ms.service: powerbi
ms.subservice: pbi-collaborate-share
ms.topic: how-to
ms.reviewer: ''
ms.cunstom: ''
ms.date: 09/16/2019
LocalizationGroup: Get started
ms.openlocfilehash: 4b2ce1624bcbbc352ab4f4eaaeb97927c09c2d78
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411666"
---
# <a name="get-started-with-third-party-apps"></a><span data-ttu-id="4ce9f-103">เริ่มใช้งานแอปของบริษัทอื่น</span><span class="sxs-lookup"><span data-stu-id="4ce9f-103">Get started with third-party apps</span></span>

<span data-ttu-id="4ce9f-104">ด้วย Power BI คุณสามารถใช้แอปที่สร้างขึ้นโดยบริษัท หรือบุคคลอื่น นอกเหนือจาก Microsoft</span><span class="sxs-lookup"><span data-stu-id="4ce9f-104">With Power BI, you can use an app built by a company or individual other than Microsoft.</span></span> <span data-ttu-id="4ce9f-105">ตัวอย่างเช่น คุณอาจใช้แอปของบุคคลที่สาม ซึ่งเอารวมไทล์ Power BI ลงไปในเว็บแอปพลิเคชันที่สร้างขึ้นเอง</span><span class="sxs-lookup"><span data-stu-id="4ce9f-105">For example, you might use a third-party app which integrates Power BI tiles into a custom-built web application.</span></span> <span data-ttu-id="4ce9f-106">เมื่อคุณใช้แอปของบุคคลที่สาม คุณจะถูกร้องขอให้อนุญาตให้แอปพลิเคชันนั้น ได้สิทธิเกี่ยวกับบัญชี และแหล่งข้อมูล Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="4ce9f-106">When you use a third-party app, you will be asked to grant that application certain permissions to your Power BI account and resources.</span></span> <span data-ttu-id="4ce9f-107">สิ่งสำคัญคื่อ คุณให้สิทธิ์แก่แอปพลิเคชันที่คุณรู้จักและเชื่อถือเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4ce9f-107">It is important that you only grant permissions to applications that you know and trust.</span></span> <span data-ttu-id="4ce9f-108">คุณสามารถเพิกถอนสิทธิ์ที่อนุญาตให้แอปพลิเคชันสได้ทุกเมื่อ</span><span class="sxs-lookup"><span data-stu-id="4ce9f-108">Permissions to an application can be revoked at any time.</span></span> <span data-ttu-id="4ce9f-109">ดู[เพิกถอนสิทธิ์แอปของบุคคลที่สาม](#revoke)</span><span class="sxs-lookup"><span data-stu-id="4ce9f-109">See [Revoke third party app permissions](#revoke).</span></span>

<span data-ttu-id="4ce9f-110">ต่อไปนี้คือ ชนิดของการเข้าถึง ที่แอปพลิเคชันสามารถร้องขอได้</span><span class="sxs-lookup"><span data-stu-id="4ce9f-110">Here are the types of access an application can request.</span></span>

## <a name="power-bi-app-permissions"></a><span data-ttu-id="4ce9f-111">สิทธิ์ใน Power BI App</span><span class="sxs-lookup"><span data-stu-id="4ce9f-111">Power BI App permissions</span></span>

* <span data-ttu-id="4ce9f-112">**ดูแดชบอร์ดทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="4ce9f-112">**View all Dashboards**</span></span>
  
  * <span data-ttu-id="4ce9f-113">สิทธิ์นี้อนุญาตให้แอปพลิเคชันสามารถดูแดชบอร์ดทั้งหมดที่คุณสามารถเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="4ce9f-113">This permission gives an application the ability to view all dashboards you have access to.</span></span> <span data-ttu-id="4ce9f-114">ซึ่งรวมถึงแดชบอร์ดที่คุณเป็นเจ้าของ ได้รับจากชุดเนื้อหา และมีการแชร์ให้กับคุณ และอยู่ในกลุ่มเดียวกันกับคุณ</span><span class="sxs-lookup"><span data-stu-id="4ce9f-114">This includes dashboards that you own, have gotten from content packs, and have been shared to you and are in groups that you belong to.</span></span> <span data-ttu-id="4ce9f-115">แอปพลิเคชันไม่สามารถทำการแก้ไขใด ๆ ลงไปยังแดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="4ce9f-115">The application cannot make any modifications to the dashboard.</span></span> <span data-ttu-id="4ce9f-116">สิทธิ์นี้สามารถใช้โดยแอปพลิเคชัน เพื่อฝังเนื้อหาแดชบอร์ดของคุณลงในการใช้งานของมัน</span><span class="sxs-lookup"><span data-stu-id="4ce9f-116">Among other things, this permission can be used by an application to embed your dashboard content into its experiences.</span></span>

* <span data-ttu-id="4ce9f-117">**ดูรายงานทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="4ce9f-117">**View all Reports**</span></span>
  
  * <span data-ttu-id="4ce9f-118">สิทธิ์นี้อนุญาตให้แอปพลิเคชันสามารถดูรายงานทั้งหมดที่คุณสามารถเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="4ce9f-118">This permission gives an application the ability to view all reports you have access to.</span></span> <span data-ttu-id="4ce9f-119">ซึ่งรวมถึงรายงานที่คุณเป็นเจ้าของ ได้รับจากชุดเนื้อหา และอยู่ในกลุ่มเดียวกันกับคุณ</span><span class="sxs-lookup"><span data-stu-id="4ce9f-119">This includes reports that you own, have gotten from content packs, and are in groups that you belong to.</span></span> <span data-ttu-id="4ce9f-120">การที่ดูรายงานได้แสดงว่า แอปพลิเคชันสามารถดูข้อมูลที่อยู่ในนั้นได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="4ce9f-120">Part of viewing the report, means that the application can also see the data within it.</span></span> <span data-ttu-id="4ce9f-121">แอปพลิเคชันไม่สามารถทำการแก้ไขใด ๆ ลงไปยังรายงานด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="4ce9f-121">The application cannot make any modifications to the reports themselves.</span></span> <span data-ttu-id="4ce9f-122">สิทธิ์นี้สามารถใช้โดยแอปพลิเคชัน เพื่อฝังเนื้อหารายงานของคุณลงในการใช้งานของมัน</span><span class="sxs-lookup"><span data-stu-id="4ce9f-122">Among other things, this permission can be used by an application to embed your report content into its experiences.</span></span>

* <span data-ttu-id="4ce9f-123">**ดูชุดข้อมูลทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="4ce9f-123">**View all Datasets**</span></span>
  
  * <span data-ttu-id="4ce9f-124">สิทธิ์นี้อนุญาตให้แอปพลิเคชันสามารถดูชุดข้อมูลทั้งหมดที่คุณสามารถเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="4ce9f-124">This permission gives an application the ability to list all datasets that you have access to.</span></span> <span data-ttu-id="4ce9f-125">ซึ่งรวมถึงชุดข้อมูลที่คุณเป็นเจ้าของ ได้รับจากชุดเนื้อหา และอยู่ในกลุ่มเดียวกันกับคุณ</span><span class="sxs-lookup"><span data-stu-id="4ce9f-125">This includes datasets that you own, have gotten from content packs, and are in groups that you belong to.</span></span> <span data-ttu-id="4ce9f-126">แอปพลิเคชันสามารถเห็นชื่อของชุดข้อมูลทั้งหมดของคุณ โครงสร้างของมันรวมไปถึงชื่อตารางและคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="4ce9f-126">An application can see the names of all your datasets as well as their structure including table and column names.</span></span> <span data-ttu-id="4ce9f-127">สิทธิ์นี้ให้สิทธิ์ในการอ่านข้อมูลในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4ce9f-127">This permission gives rights to read the data in a dataset.</span></span> <span data-ttu-id="4ce9f-128">สิทธิ์นี้ไม่อนุญาตให้แอปพลิเคชันเพิ่ม หรือแก้ไขชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4ce9f-128">The permission does not give the application rights to add or make changes to a dataset.</span></span>
* <span data-ttu-id="4ce9f-129">**อ่านและเขียนชุดข้อมูลทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="4ce9f-129">**Read and Write all Datasets**</span></span>
  
  * <span data-ttu-id="4ce9f-130">สิทธิ์นี้อนุญาตให้แอปพลิเคชันสามารถดูชุดข้อมูลทั้งหมดที่คุณสามารถเข้าถึงได้</span><span class="sxs-lookup"><span data-stu-id="4ce9f-130">This permission gives an application the ability to list all datasets that you have access to.</span></span> <span data-ttu-id="4ce9f-131">ซึ่งรวมถึงชุดข้อมูลที่คุณเป็นเจ้าของ ได้รับจากชุดเนื้อหา และอยู่ในกลุ่มเดียวกันกับคุณ</span><span class="sxs-lookup"><span data-stu-id="4ce9f-131">This includes datasets that you own, have gotten from content packs, and are in groups that you belong to.</span></span> <span data-ttu-id="4ce9f-132">แอปพลิเคชันสามารถเห็นชื่อของชุดข้อมูลทั้งหมดของคุณ โครงสร้างของมันรวมไปถึงชื่อตารางและคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="4ce9f-132">An application can see the names of all your datasets as well as their structure including table and column names.</span></span> <span data-ttu-id="4ce9f-133">สิทธิ์นี้ให้สิทธิ์ในการอ่านและเขียนข้อมูลในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4ce9f-133">This permission gives rights to read and write the data in a dataset.</span></span> <span data-ttu-id="4ce9f-134">แอปพลิเคชันยังสามารถสร้างชุดข้อมูลใหม่ หรือทำการแก้ไขชุดข้อมูลที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="4ce9f-134">The application can also create new datasets, or make modifications to existing ones.</span></span> <span data-ttu-id="4ce9f-135">สิทธิ์นี้มักใช้โดยแอปพลิเคชันที่ส่งข้อมูลไปยัง Power BI โดยตรง</span><span class="sxs-lookup"><span data-stu-id="4ce9f-135">This is commonly used by an application to send to data directly to Power BI.</span></span>

* <span data-ttu-id="4ce9f-136">**ดูกลุ่มของผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="4ce9f-136">**View user's Groups**</span></span>
  
  * <span data-ttu-id="4ce9f-137">สิทธิ์นี้อนุญาตให้แอปพลิเคชันสามารถเห็นรายการกลุ่มทั้งหมดที่คุณเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="4ce9f-137">This permission gives the application the ability to list all groups that you are a member of.</span></span> <span data-ttu-id="4ce9f-138">ซึ่งสามารถใช้สิทธิ์นี้พร้อมกับบางสิทธิ์อื่น ๆ เพื่อดูหรือแก้ไขเนื้อหาของกลุ่มนั้น ๆ</span><span class="sxs-lookup"><span data-stu-id="4ce9f-138">It can use this permission along with some of the other permissions listed to view or update content for that particular group.</span></span> <span data-ttu-id="4ce9f-139">แอปพลิเคชันไม่สามารถทำการแก้ไขกลุ่มได้ด้วยตัวเอง</span><span class="sxs-lookup"><span data-stu-id="4ce9f-139">The application cannot make modifications to the group itself.</span></span>

<a name="revoke"/>

## <a name="revoke-third-party-app-permissions"></a><span data-ttu-id="4ce9f-140">เพิกถอนสิทธิ์ของแอปของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="4ce9f-140">Revoke third-party app permissions</span></span>

<span data-ttu-id="4ce9f-141">คุณยกเลิกสิทธิ์สำหรับแอปของบุคคลที่สาม โดยไปที่ไซต์ของ Office 365 My Apps</span><span class="sxs-lookup"><span data-stu-id="4ce9f-141">You revoke permissions for a third-party app by going to the Office 365 My Apps site.</span></span>

<span data-ttu-id="4ce9f-142">บนไซต์ **Office 365 My Apps** นี่คือวิธีการยกเลิกสิทธิ์ของบุคคลที่สาม:</span><span class="sxs-lookup"><span data-stu-id="4ce9f-142">On the **Office 365 My apps** site, here's how to revoke third-party permissions:</span></span>

1. <span data-ttu-id="4ce9f-143">ไปยัง[ไซต์ Office 365 My Apps](https://portal.office.com/myapps)</span><span class="sxs-lookup"><span data-stu-id="4ce9f-143">Go to [Office 365 My Apps site](https://portal.office.com/myapps).</span></span>

2. <span data-ttu-id="4ce9f-144">บนหน้า **แอปของฉัน** ค้นหาแอปของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="4ce9f-144">On the **My apps** page, locate the third-party app.</span></span>

3. <span data-ttu-id="4ce9f-145">โฮเวอร์เหนือไทล์ขอวแอป คลิกที่ปุ่ม **(...)**  แล้วคลิก **เอาออก**</span><span class="sxs-lookup"><span data-stu-id="4ce9f-145">Hover over the app tile, click the **(...)** button, and click **Remove**.</span></span>

   ![สกรีนช็อตแสดงตัวเลือกเอาออกเพื่อยกเลิกสิทธิ์ของบุคคลที่สาม](media/service-power-bi-get-started-third-party-apps/remove.png)