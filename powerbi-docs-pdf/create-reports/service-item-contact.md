---
title: ตั้งค่าข้อมูลติดต่อสำหรับรายงานและแดชบอร์ด
description: เรียนรู้วิธีการตั้งค่าข้อมูลติดต่อสำหรับรายงานและแดชบอร์ด
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 10/08/2019
LocalizationGroup: Common tasks
ms.openlocfilehash: 4518ac8eff4b4f52ab2eeb715c0c460bb478678f
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96388344"
---
# <a name="set-contact-information-for-reports-and-dashboards-in-the-power-bi-service"></a><span data-ttu-id="f8d21-103">ตั้งค่าข้อมูลติดต่อสำหรับรายงานและแดชบอร์ดในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="f8d21-103">Set contact information for reports and dashboards in the Power BI service</span></span>
<span data-ttu-id="f8d21-104">บทความนี้สอนวิธีการตั้งค่าข้อมูลติดต่อสำหรับแดชบอร์ดหรือรายงานในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="f8d21-104">This article teaches you how to set contact information for a dashboard or report in the Power BI service.</span></span>

> [!NOTE]
> <span data-ttu-id="f8d21-105">สามารถตั้งค่าข้อมูลติดต่อสำหรับรายการต่าง ๆ ในพื้นที่ทำงานแบบคลาสสิคหรือแบบใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="f8d21-105">Contact information can be set for items in a classic or new workspace.</span></span> <span data-ttu-id="f8d21-106">คุณไม่สามารถตั้งค่าข้อมูลติดต่อสำหรับรายการต่าง ๆ ในพื้นที่ทำงานของฉัน</span><span class="sxs-lookup"><span data-stu-id="f8d21-106">You can't set contact information for items in your My Workspace.</span></span> <span data-ttu-id="f8d21-107">บัตรข้อมูลจะแสดงเมื่อดูรายงานหรือแดชบอร์ดใน[รูปลักษณ์ใหม่](../consumer/service-new-look.md)</span><span class="sxs-lookup"><span data-stu-id="f8d21-107">The info card is shown when viewing a report or dashboard in the [new look](../consumer/service-new-look.md).</span></span>

<span data-ttu-id="f8d21-108">คุณสามารถเพิ่มผู้ใช้หรือกลุ่มหลายรายลงในผู้ติดต่อสำหรับรายการต่าง ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="f8d21-108">You can add multiple users or groups to the contact for an item.</span></span> <span data-ttu-id="f8d21-109">พวกเขาสามารถเป็น:</span><span class="sxs-lookup"><span data-stu-id="f8d21-109">They can be:</span></span>
* <span data-ttu-id="f8d21-110">บุคคล</span><span class="sxs-lookup"><span data-stu-id="f8d21-110">A person</span></span>
* <span data-ttu-id="f8d21-111">Microsoft 365 Group</span><span class="sxs-lookup"><span data-stu-id="f8d21-111">A Microsoft 365 group</span></span>
* <span data-ttu-id="f8d21-112">อีเมลที่เปิดใช้งานกลุ่มความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="f8d21-112">An email enabled security group</span></span>
* <span data-ttu-id="f8d21-113">รายการแจกจ่าย</span><span class="sxs-lookup"><span data-stu-id="f8d21-113">A distribution list</span></span>

<span data-ttu-id="f8d21-114">ตามค่าเริ่มต้น บุคคลที่สร้างรายงานหรือแดชบอร์ดใหม่คือผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="f8d21-114">By default the person who creates a new report or dashboard is the contact for it.</span></span> <span data-ttu-id="f8d21-115">หากคุณตั้งค่าค่าหนึ่ง ค่าดังกล่าวจะแทนที่ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f8d21-115">If you set a value, it overrides the default.</span></span> <span data-ttu-id="f8d21-116">แน่นอนว่าคุณสามารถลบบุคคลหรือกลุ่มทั้งหมดออกจากรายการผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="f8d21-116">You can of course remove all the people or groups from the contact list.</span></span> <span data-ttu-id="f8d21-117">เมื่อคุณทำเช่นนี้สำหรับพื้นที่ทำงานแบบคลาสสิก Microsoft 365 Group สำหรับพื้นที่ทำงานจะแสดงขึ้นมา</span><span class="sxs-lookup"><span data-stu-id="f8d21-117">When you do this, for classic workspaces, the Microsoft 365 group for the workspace will be shown.</span></span> <span data-ttu-id="f8d21-118">สำหรับพื้นที่ทำงานในประสบการณ์ในพื้นที่ทำงานใหม่ จะมีการใช้[รายการผู้ติดต่อของพื้นที่ทำงาน](../collaborate-share/service-create-the-new-workspaces.md#create-a-contact-list)</span><span class="sxs-lookup"><span data-stu-id="f8d21-118">For new workspace experience workspaces, the [workspace contact list](../collaborate-share/service-create-the-new-workspaces.md#create-a-contact-list) will be used.</span></span> <span data-ttu-id="f8d21-119">หากไม่ได้ตั้งค่ารายการผู้ติดต่อของพื้นที่ทำงาน ผู้ดูแลระบบพื้นที่ทำงานจะแสดงขึ้นมา</span><span class="sxs-lookup"><span data-stu-id="f8d21-119">If the workspace contact list is not set, then workspace admins are shown.</span></span>

<span data-ttu-id="f8d21-120">ข้อมูลติดต่อจะแสดงบุคคลที่กำลังดูรายการ</span><span class="sxs-lookup"><span data-stu-id="f8d21-120">The contact information is shown to people viewing the item.</span></span> 

 ![ผู้ติดต่อของรายงานการบริการ](media/service-item-contact/service-report-contact.png)

<span data-ttu-id="f8d21-122">เมื่อคุณคลิกที่รายชื่อผู้ติดต่อ จะมีการสร้างอีเมลเพื่อให้คุณสามารถถามข้อสงสัยหรือขอความช่วยเหลือได้</span><span class="sxs-lookup"><span data-stu-id="f8d21-122">When you click the list of contacts, an email is created so you can ask questions or get help.</span></span> 

 ![อีเมลผู้ติดต่อการบริการ](media/service-item-contact/service-contact-email.png)
 
<span data-ttu-id="f8d21-124">นอกจากนี้ ยังมีการใช้ข้อมูลรายการผู้ติดต่อในสถานที่อื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="f8d21-124">The contact list information is also used in other places.</span></span> <span data-ttu-id="f8d21-125">ตัวอย่างเช่น จะปรากฏขึ้นในบางสถานการณ์ข้อผิดพลาดในกล่องโต้ตอบข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="f8d21-125">For example, it is shown in some error scenarios in the error dialog box.</span></span> <span data-ttu-id="f8d21-126">ข้อความอีเมลแบบอัตโนมัติที่เกี่ยวข้องกับรายการจะถูกส่งไปยังรายการผู้ติดต่อ เช่น คำขอการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="f8d21-126">Automated email messages related to the item, like access requests, are sent to the contact list.</span></span> 

> [!NOTE]
> <span data-ttu-id="f8d21-127">เมื่อเผยแพร่แอป ข้อมูลติดต่อที่ตั้งค่าไว้ในแต่ละรายการจะถูกตั้งค่าเป็นบุคคลที่เผยแพร่หรืออัปเดตแอป</span><span class="sxs-lookup"><span data-stu-id="f8d21-127">When publishing an app, the contact information set on individual items is set to the person who published or updated the app.</span></span> <span data-ttu-id="f8d21-128">คุณสามารถตั้งค่า URL การสนับสนุนแอปได้ เพื่อให้ผู้ใช้แอปสามารถขอความช่วยเหลือตามที่จำเป็นได้</span><span class="sxs-lookup"><span data-stu-id="f8d21-128">You can set the app support URL so app users get the help they need.</span></span>

## <a name="set-contact-information-for-a-report"></a><span data-ttu-id="f8d21-129">ตั้งค่าข้อมูลติดต่อสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="f8d21-129">Set contact information for a report</span></span>
1. <span data-ttu-id="f8d21-130">ในพื้นที่ทำงานของคุณ เลือกแถบ **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="f8d21-130">In your workspace, select the **Reports** tab.</span></span>
2. <span data-ttu-id="f8d21-131">ค้นหารายงานที่ต้องการและเลือกไอคอน **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="f8d21-131">Locate the desired report and select the **Settings** icon.</span></span>
3. <span data-ttu-id="f8d21-132">ค้นหาเขตข้อมูลการป้อนข้อมูลของ **ผู้ติดต่อ** และตั้งค่าค่า</span><span class="sxs-lookup"><span data-stu-id="f8d21-132">Locate the **Contact** input field and set a value.</span></span>

     ![การตั้งค่าผู้ติดต่อของรายงานการบริการ](media/service-item-contact/service-report-contact-setting.png)

## <a name="set-contact-information-for-a-dashboard"></a><span data-ttu-id="f8d21-134">ตั้งค่าข้อมูลติดต่อสำหรับแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="f8d21-134">Set contact information for a dashboard</span></span>
1. <span data-ttu-id="f8d21-135">ในพื้นที่ทำงานของคุณ เลือกแถบ **แดชบอร์ด**</span><span class="sxs-lookup"><span data-stu-id="f8d21-135">In your workspace, select the **Dashboards** tab.</span></span>
2. <span data-ttu-id="f8d21-136">ค้นหาแดชบอร์ดที่ต้องการและเลือกไอคอน **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="f8d21-136">Locate the desired dashboard and select the **Settings** icon</span></span>
3. <span data-ttu-id="f8d21-137">ค้นหาเขตข้อมูลการป้อนข้อมูลของ **ผู้ติดต่อ** และตั้งค่าค่า</span><span class="sxs-lookup"><span data-stu-id="f8d21-137">Locate the **Contact** input field and set a value.</span></span>

     ![การตั้งค่าผู้ติดต่อของแดชบอร์ดการบริการ](media/service-item-contact/service-dashboard-contact-setting.png)

## <a name="limitations-and-considerations"></a><span data-ttu-id="f8d21-139">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="f8d21-139">Limitations and considerations</span></span>
* <span data-ttu-id="f8d21-140">ผู้ติดต่อจะถูกตั้งค่าโดยอัตโนมัติสำหรับรายการใหม่ที่สร้างขึ้นในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="f8d21-140">The contact is set automatically for new items created in the Power BI service.</span></span> <span data-ttu-id="f8d21-141">รายการที่มีอยู่จะแสดงค่าเริ่มต้นของพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f8d21-141">Existing items will show the workspace default.</span></span>
* <span data-ttu-id="f8d21-142">คุณสามารถตั้งค่าผู้ใช้หรือกลุ่มใด ๆ ในรายการผู้ติดต่อ แต่จะไม่ได้รับสิทธิ์กับรายการโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f8d21-142">You can set any user or group in the contact list, but they will not be granted permission to the item automatically.</span></span> <span data-ttu-id="f8d21-143">ใช้การแชร์หรือให้ผู้ใช้ที่ต้องการเข้าถึงพื้นที่ทำงานผ่านบทบาท</span><span class="sxs-lookup"><span data-stu-id="f8d21-143">Use sharing or give user who need it access to the workspace through a role.</span></span> 
* <span data-ttu-id="f8d21-144">รายการผู้ติดต่อระดับรายการจะไม่ได้รับการส่งไปยังแอปเมื่อมีการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="f8d21-144">The item level contact list doesn’t get pushed into apps when they are published.</span></span> <span data-ttu-id="f8d21-145">ประสบการณ์การนำทางในแอปใหม่มี URL การสนับสนุนที่คุณกำหนดค่าเพื่อช่วยจัดการคำติชมจากผู้ใช้แอปจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="f8d21-145">The new app navigation experience provides a support URL you configure to help manage feedback from large number of app users.</span></span>


## <a name="next-steps"></a><span data-ttu-id="f8d21-146">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="f8d21-146">Next steps</span></span>

<span data-ttu-id="f8d21-147">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f8d21-147">More questions?</span></span> [<span data-ttu-id="f8d21-148">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="f8d21-148">Try the Power BI Community</span></span>](https://community.powerbi.com/)
