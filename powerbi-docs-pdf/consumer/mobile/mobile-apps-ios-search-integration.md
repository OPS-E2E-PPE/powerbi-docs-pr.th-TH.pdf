---
title: การรวมการค้นหาอุปกรณ์ iOS ด้วย Power BI
description: ใช้การค้นหาอุปกรณ์ (สปอตไลต์) เพื่อค้นหาและเข้าถึงเนื้อหาที่คุณต้องการ
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: how-to
ms.date: 03/11/2020
ms.openlocfilehash: c289395e5d5529c7951b9102722999dfe22d699e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96414587"
---
# <a name="ios-device-search-spotlight-integration-with-power-bi-mobile-ios-app-preview"></a><span data-ttu-id="5d8cd-103">การรวมการค้นหาอุปกรณ์ iOS (สปอตไลต์) ด้วยแอป Power BI บนมือถือระบบ iOS (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="5d8cd-103">iOS Device Search (Spotlight) integration with Power BI Mobile iOS App (preview)</span></span>
<span data-ttu-id="5d8cd-104">ใช้การค้นหาอุปกรณ์เพื่อค้นหาและเข้าถึงเนื้อหาที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="5d8cd-104">Use iOS device search to find and access the content you need.</span></span>

<span data-ttu-id="5d8cd-105">เมื่อคุณใช้การค้นหาอุปกรณ์ iOS (สปอตไลต์) เพื่อค้นหาเนื้อหาเฉพาะเ รายการ Power BI จะรวมอยู่ในรายการผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="5d8cd-105">When you use iOS device search (spotlight) to look for specific content, Power BI items are included in the result list.</span></span> <span data-ttu-id="5d8cd-106">เมื่อแตะรายการ Power BI จากรายการผลลัพธ์ ระบบจะนำคุณไปยังรายการภายในแอป Power BI โดยตรง</span><span class="sxs-lookup"><span data-stu-id="5d8cd-106">Tapping on a Power BI item from the result list takes you directly to that item inside the Power BI app.</span></span>

## <a name="find-items-using-device-search"></a><span data-ttu-id="5d8cd-107">ค้นหารายการโดยใช้การค้นหาอุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="5d8cd-107">Find items using device search</span></span>

<span data-ttu-id="5d8cd-108">หากต้องการค้นหารายการโดยใช้การค้นหาอุปกรณ์:</span><span class="sxs-lookup"><span data-stu-id="5d8cd-108">To find items using device search:</span></span>

1. <span data-ttu-id="5d8cd-109">ปัดลงจากตรงกลางของหน้าจอ **หน้าแรก** เพื่อไปที่การค้นหาอุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="5d8cd-109">Swipe down from the middle of the **Home** screen to get into the device search.</span></span>

2. <span data-ttu-id="5d8cd-110">แตะที่เขตข้อมูล **ค้นหา** แล้วพิมพ์ข้อความที่คุณกำลังค้นหา</span><span class="sxs-lookup"><span data-stu-id="5d8cd-110">Tap the **Search** field and type the text you're looking for.</span></span>
 
   <span data-ttu-id="5d8cd-111">ผลลัพธ์การค้นหาจะรวมรายการ Power BI ของประเภทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5d8cd-111">The search results will include Power BI items of the following types:</span></span>

    * <span data-ttu-id="5d8cd-112">แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="5d8cd-112">Dashboards</span></span>
    * <span data-ttu-id="5d8cd-113">รายงาน</span><span class="sxs-lookup"><span data-stu-id="5d8cd-113">Reports</span></span>
    * <span data-ttu-id="5d8cd-114">แอป</span><span class="sxs-lookup"><span data-stu-id="5d8cd-114">Apps</span></span>
    * <span data-ttu-id="5d8cd-115">พื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="5d8cd-115">Workspaces</span></span>
    * <span data-ttu-id="5d8cd-116">รายการที่แชร์โดยผู้ติดต่อที่คุณค้นหา</span><span class="sxs-lookup"><span data-stu-id="5d8cd-116">Items shared by the contact you search for</span></span>

    ![สกรีนช็อตที่แสดงผลลัพธ์การค้นหา Power BI ในการค้นหาอุปกรณ์ iOS](./media/mobile-apps-ios-siri-search/power-bi-spotlight-search.png)

 3. <span data-ttu-id="5d8cd-118">เมื่อคุณค้นหารายการที่คุณต้องการ ให้แตะที่รายการนั้น</span><span class="sxs-lookup"><span data-stu-id="5d8cd-118">Once you find the item you want, tap on it.</span></span> <span data-ttu-id="5d8cd-119">แอป Power BI จะเปิดที่รายการที่เลือกโดยตรง</span><span class="sxs-lookup"><span data-stu-id="5d8cd-119">The Power BI app will open directly on the selected item.</span></span> 

<span data-ttu-id="5d8cd-120">นอกจากนี้ การค้นหาอุปกรณ์ที่สนับสนุนโดย Siri จะมีคำแนะนำตามการดำเนินการของคุณใช้บ่อยในแอป Power BI</span><span class="sxs-lookup"><span data-stu-id="5d8cd-120">Device search, powered by Siri, will also include suggestions based on your frequent actions in the Power BI app.</span></span> <span data-ttu-id="5d8cd-121">คำแนะนำของ Siri จะแสดงในการค้นหาและหน้าจอเมื่อล็อก</span><span class="sxs-lookup"><span data-stu-id="5d8cd-121">Siri suggestions will be shown in the search and lock screen.</span></span>

>[!NOTE]
>
><span data-ttu-id="5d8cd-122">หากต้องการปิดใช้งานการค้นหาอุปกรณ์และคำแนะนำของ Siri ให้ไปที่ **การตั้งค่าอุปกรณ์**>**การตั้งค่า Power BI**>**Siri และการค้นหา** และปิดใช้งานการตั้งค่า **Siri และคำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="5d8cd-122">To disable device search and Siri suggestions, go to **Device settings** > **Power BI settings** > **Siri & Search**, and disable the **Siri & suggestions** setting.</span></span>
>

## <a name="next-steps"></a><span data-ttu-id="5d8cd-123">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="5d8cd-123">Next steps</span></span>
<span data-ttu-id="5d8cd-124">เรียนรู้เพิ่มเติมเกี่ยวกับแอป Power BI สำหรับอุปกรณ์เคลื่อนที่โดยดำเนินการดังนี้:</span><span class="sxs-lookup"><span data-stu-id="5d8cd-124">Learn more about the Power BI mobile app by doing the following:</span></span> 

* <span data-ttu-id="5d8cd-125">การดาวน์โหลด [แอป Power BI สำหรับ iPhone](https://go.microsoft.com/fwlink/?LinkId=522062)</span><span class="sxs-lookup"><span data-stu-id="5d8cd-125">Downloading the [Power BI iPhone mobile app](https://go.microsoft.com/fwlink/?LinkId=522062)</span></span>
* <span data-ttu-id="5d8cd-126">ติดตาม[@MSPowerBIบน Twitter](https://twitter.com/MSPowerBI)</span><span class="sxs-lookup"><span data-stu-id="5d8cd-126">Following [@MSPowerBI on Twitter](https://twitter.com/MSPowerBI)</span></span>
* <span data-ttu-id="5d8cd-127">การเข้าร่วมการสนทนาที่[ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="5d8cd-127">Joining the conversation at the [Power BI Community](https://community.powerbi.com/)</span></span>

