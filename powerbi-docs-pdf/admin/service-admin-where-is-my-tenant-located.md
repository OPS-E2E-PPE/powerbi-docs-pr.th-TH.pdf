---
title: ผู้เช่า Power BI ของฉันอยู่ที่ไหน?
description: เรียนรู้ตำแหน่งที่ผู้เช่า Power BI ของคุณอยู่และวิธีเลือกตำแหน่งที่ตั้ง เป็นเรื่องสำคัญที่ต้องเรียนรู้เพราะอาจส่งผลกระทบต่อการโต้ตอบที่คุณมีกับบริการ
author: kfollis
ms.author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 09/09/2019
LocalizationGroup: Administration
ms.openlocfilehash: 632eca1fdcb1bed380ad699a36264bc0239baef5
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412402"
---
# <a name="where-is-my-power-bi-tenant-located"></a><span data-ttu-id="f2b1b-104">ผู้เช่า Power BI ของฉันอยู่ที่ไหน?</span><span class="sxs-lookup"><span data-stu-id="f2b1b-104">Where is my Power BI tenant located?</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/0fOxaHJPvdM?showinfo=0" frameborder="0" allowfullscreen></iframe>

<span data-ttu-id="f2b1b-105">เรียนรู้ตำแหน่งที่ผู้เช่า Power BI ของคุณอยู่และวิธีเลือกตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="f2b1b-105">Learn where your Power BI tenant is located and how that location is selected.</span></span> <span data-ttu-id="f2b1b-106">การเรียนรู้ตำแหน่งที่ตั้งถือเป็นสิ่งสำคัญเนื่องจากสามารถส่งผลกระทบต่อการโต้ตอบที่คุณมีกับบริการได้</span><span class="sxs-lookup"><span data-stu-id="f2b1b-106">Learning the location is important, because it can affect the interactions you have with the service.</span></span>

## <a name="how-to-determine-where-your-power-bi-tenant-is-located"></a><span data-ttu-id="f2b1b-107">วิธีการตรวจสอบตำแหน่งที่ผู้เช่า Power BI ของคุณอยู่</span><span class="sxs-lookup"><span data-stu-id="f2b1b-107">How to determine where your Power BI tenant is located</span></span>

<span data-ttu-id="f2b1b-108">หากต้องการค้นหาภูมิภาคที่ผู้เช่าของคุณอยู่ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="f2b1b-108">To find the region your tenant is in, follow these steps.</span></span>

1. <span data-ttu-id="f2b1b-109">ในบริการของ Power BI ที่เมนูด้านบน เลือกความช่วยเหลือ ( **?** ) จากนั้นเลือก **เกี่ยวกับ Power BI**</span><span class="sxs-lookup"><span data-stu-id="f2b1b-109">In the Power BI service, in the top menu, select help (**?**) then **About Power BI**.</span></span>

1. <span data-ttu-id="f2b1b-110">ค้นหาค่าที่อยู่ถัดจาก **ข้อมูลของคุณถูกเก็บไว้ใน**</span><span class="sxs-lookup"><span data-stu-id="f2b1b-110">Look for the value next to **Your data is stored in**.</span></span> <span data-ttu-id="f2b1b-111">ค่านั้นคือภูมิภาคที่ผู้เช่าของคุณอยู่</span><span class="sxs-lookup"><span data-stu-id="f2b1b-111">It's the region where your tenant is located.</span></span> <span data-ttu-id="f2b1b-112">ค่านี้ยังมีภูมิภาคที่ข้อมูลของคุณถูกเก็บไว้ เว้นแต่ว่าคุณกำลังใช้ความจุในภูมิภาคอื่นสำหรับพื้นที่ทำงานของคุณด้วย</span><span class="sxs-lookup"><span data-stu-id="f2b1b-112">The value is also the region where your data is stored, unless you're using capacities in different regions for your workspaces.</span></span>

    ![ขอบเขตข้อมูล](media/service-admin-where-is-my-tenant-located/power-bi-data-region.png)

## <a name="how-the-data-region-is-selected"></a><span data-ttu-id="f2b1b-114">วิธีเลือกขอบเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f2b1b-114">How the data region is selected</span></span>

<span data-ttu-id="f2b1b-115">ขอบเขตข้อมูลจะยึดตามประเทศ/ภูมิภาคที่คุณเลือกเมื่อคุณสร้างผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="f2b1b-115">The data region is based on the country/region you select when you create the tenant.</span></span> <span data-ttu-id="f2b1b-116">การเลือกจะนำไปใช้เพื่อลงทะเบียนสำหรับทั้ง Microsoft 365 และ Power BI เนื่องจากข้อมูลนี้ถูกใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="f2b1b-116">The selection applies to sign up for both Microsoft 365 and to Power BI, because this information is shared.</span></span> <span data-ttu-id="f2b1b-117">หากเป็นผู้เช่าใหม่ ให้เลือกประเทศ/ภูมิภาคที่เหมาะสมจากรายการเมื่อคุณลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f2b1b-117">If this is a new tenant, select the appropriate country/region from the list when you sign up.</span></span>

![การเลือกประเทศ](media/service-admin-where-is-my-tenant-located/sign-up-country-selection.png)

<span data-ttu-id="f2b1b-119">Power BI จะเลือกขอบเขตข้อมูลที่ใกล้เคียงการเลือกของคุณมากที่สุด ซึ่งจะกำหนดตำแหน่งที่เก็บข้อมูลสำหรับผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="f2b1b-119">Power BI picks a data region closest to your selection, which determines where data is stored for your tenant.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f2b1b-120">คุณไม่สามารถเปลี่ยนการเลือกหลังจากที่สร้างผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="f2b1b-120">You cannot change the selection after you create the tenant.</span></span>

<span data-ttu-id="f2b1b-121">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f2b1b-121">More questions?</span></span> [<span data-ttu-id="f2b1b-122">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="f2b1b-122">Try the Power BI Community</span></span>](https://community.powerbi.com/)
