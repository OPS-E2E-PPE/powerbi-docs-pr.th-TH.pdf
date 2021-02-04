---
title: ข้อมูลขาออกของ Power BI และ Azure
description: ทำความเข้าใจเกี่ยวกับค่าใช้จ่ายในการเข้าถึง Azure และ Power BI ตามสถานที่ตั้งของผู้เช่าและ Power BI Premium
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 05/08/2019
LocalizationGroup: Data from databases
ms.openlocfilehash: 8fec8f4fa7a78a69693d4a200baa14e905cee943
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410700"
---
# <a name="power-bi-and-azure-egress"></a><span data-ttu-id="032d5-103">ข้อมูลขาออกของ Power BI และ Azure</span><span class="sxs-lookup"><span data-stu-id="032d5-103">Power BI and Azure egress</span></span>

<span data-ttu-id="032d5-104">เมื่อใช้ Power BI กับแหล่งข้อมูล Azure คุณสามารถหลีกเลี่ยงค่าใช้จ่ายในการเข้าถึง Azure ได้โดยตรวจสอบให้แน่ใจว่าผู้เช่า Power BI ของคุณอยู่ในพื้นที่เดียวกันกับแหล่งข้อมูล Azure ของคุณ</span><span class="sxs-lookup"><span data-stu-id="032d5-104">When using Power BI with Azure data sources, you can avoid Azure egress charges by making sure your Power BI tenant is in the same region as your Azure data sources.</span></span>

<span data-ttu-id="032d5-105">เมื่อผู้เช่า Power BI ของคุณใช้งานในพื้นที่ Azure เดียวกับที่คุณใช้แหล่งข้อมูลของคุณ คุณจะไม่ต้องเสียค่าใช้จ่ายในการเข้าถึงสำหรับการรีเฟรชตามกำหนดเวลาและการโต้ตอบระหว่าง DirectQuery</span><span class="sxs-lookup"><span data-stu-id="032d5-105">When your Power BI tenant is deployed in the same Azure region as you deploy your data sources, you do not incur egress charges for scheduled refresh and DirectQuery interactions.</span></span> 

## <a name="determining-where-your-power-bi-tenant-is-located"></a><span data-ttu-id="032d5-106">ตรวจสอบตำแหน่งที่ผู้เช่า Power BI ของคุณอยู่</span><span class="sxs-lookup"><span data-stu-id="032d5-106">Determining where your Power BI tenant is located</span></span>

<span data-ttu-id="032d5-107">เมื่อต้องการค้นหาว่าผู้เช่า Power BI ของคุณอยู่ที่ใด ดูบทความ [ผู้เช่า Power BI ของฉันอยู่ที่ไหน](../admin/service-admin-where-is-my-tenant-located.md)</span><span class="sxs-lookup"><span data-stu-id="032d5-107">To find out where your Power BI tenant is located, see the [where is my Power BI tenant located](../admin/service-admin-where-is-my-tenant-located.md) article.</span></span>

<span data-ttu-id="032d5-108">สำหรับลูกค้า Power BI Premium Multi-Geo หากผู้เช่า Power BI ของคุณไม่อยู่ในตำแหน่งที่เหมาะสมสำหรับแหล่งข้อมูลบางส่วนที่ใช้ Azure คุณสามารถปรับใช้ Power BI Premium Multi-Geo ในพื้นที่ Azure ที่ต้องการและได้รับประโยชน์จากการที่ผู้เช่า Power BI และแหล่งข้อมูล Azure อยู่ในภูมิภาค Azure เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="032d5-108">For Power BI Premium Multi-Geo customers, if your Power BI tenant is not in the optimal location for some of your Azure-based data sources, you can deploy Power BI Premium Multi-Geo in the desired Azure region and benefit from having your Power BI tenant and Azure data sources in the same Azure region.</span></span>

## <a name="next-steps"></a><span data-ttu-id="032d5-109">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="032d5-109">Next steps</span></span>

<span data-ttu-id="032d5-110">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI Premium หรือ Multi-Geo โปรดดูที่แหล่งข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="032d5-110">For more information about Power BI Premium or Multi-Geo, take a look at the following resources:</span></span>

* [<span data-ttu-id="032d5-111">Microsoft Power BI Premium คืออะไร?</span><span class="sxs-lookup"><span data-stu-id="032d5-111">What is Microsoft Power BI Premium?</span></span>](../admin/service-premium-what-is.md)
* [<span data-ttu-id="032d5-112">วิธีการซื้อ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="032d5-112">How to purchase Power BI Premium</span></span>](../admin/service-admin-premium-purchase.md)
* [<span data-ttu-id="032d5-113">การสนับสนุน Multi-Geo สำหรับ Power BI Premium (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="032d5-113">Multi-Geo support for Power BI Premium (Preview)</span></span>](../admin/service-admin-premium-multi-geo.md)
* [<span data-ttu-id="032d5-114">ผู้เช่า Power BI ของฉันอยู่ที่ไหน?</span><span class="sxs-lookup"><span data-stu-id="032d5-114">Where is my Power BI tenant located?</span></span>](../admin/service-admin-where-is-my-tenant-located.md)
* [<span data-ttu-id="032d5-115">Power BI Premium ถามที่ถามบ่อย</span><span class="sxs-lookup"><span data-stu-id="032d5-115">Power BI Premium FAQ</span></span>](../admin/service-premium-faq.md)
