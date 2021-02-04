---
title: เกตเวย ์ข้อมูลภายในองค์กร
description: บทความนี้คือภาพรวมของเกตเวย์ข้อมูลภายในองค์กรสำหรับ Power BI คุณสามารถใช้เกตเวย์นี้เพื่อทำงานกับแหล่งข้อมูล DirectQuery คุณยังสามารถใช้เกตเวย์นี้เพื่อรีเฟรชชุดข้อมูลบนระบบคลาวด์กับข้อมูลภายในองค์กร
author: arthiriyer
ms.author: arthii
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-gateways
ms.topic: conceptual
LocalizationGroup: Gateways
ms.date: 07/15/2019
ms.openlocfilehash: 2d0b5ff4bbf14012eb0a60759007fa0d021befea
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96402167"
---
# <a name="what-is-an-on-premises-data-gateway"></a><span data-ttu-id="5a4a6-105">เกตเวย์ข้อมูลในองค์กรคืออะไร?</span><span class="sxs-lookup"><span data-stu-id="5a4a6-105">What is an on-premises data gateway?</span></span>

[!INCLUDE [gateway-rewrite](../includes/gateway-rewrite.md)]

<span data-ttu-id="5a4a6-106">เกตเวย์ข้อมูลภายในองค์กรทำหน้าที่เป็นสะพาน โดยให้บริการการถ่ายโอนข้อมูลที่รวดเร็วและปลอดภัยระหว่างข้อมูลภายในองค์กร (ข้อมูลที่ไม่ได้อยู่ในระบบคลาวด์) และบริการคลาวด์ของ Microsoft อีกหลายบริการ</span><span class="sxs-lookup"><span data-stu-id="5a4a6-106">The on-premises data gateway acts as a bridge to provide quick and secure data transfer between on-premises data (data that isn't in the cloud) and several Microsoft cloud services.</span></span> <span data-ttu-id="5a4a6-107">บริการคลาวด์เหล่านี้ประกอบรวมด้วย Power BI, PowerApps, Power Automate, Azure Analysis Services และ Azure Logic Apps</span><span class="sxs-lookup"><span data-stu-id="5a4a6-107">These cloud services include Power BI, PowerApps, Power Automate, Azure Analysis Services, and Azure Logic Apps.</span></span> <span data-ttu-id="5a4a6-108">โดยการใช้เกตเวย์ องค์กรสามารถเก็บฐานข้อมูลและแหล่งข้อมูลอื่น ๆ บนเครือข่ายภายในองค์กรของตนได้ และยังใช้ข้อมูลภายในองค์กรในบริการคลาวด์ได้อย่างปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="5a4a6-108">By using a gateway, organizations can keep databases and other data sources on their on-premises networks, yet securely use that on-premises data in cloud services.</span></span>

## <a name="how-the-gateway-works"></a><span data-ttu-id="5a4a6-109">เกตเวย์ทำงานอย่างไร</span><span class="sxs-lookup"><span data-stu-id="5a4a6-109">How the gateway works</span></span>

![ภาพรวมของเกตเวย์](media/service-gateway-onprem/on-premises-data-gateway.png)

<span data-ttu-id="5a4a6-111">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการทำงานของเกตเวย์ โปรดดูที่[สถาปัตยกรรมของเกตเวย์ข้อมูลภายในองค์กร](/data-integration/gateway/service-gateway-onprem-indepth)</span><span class="sxs-lookup"><span data-stu-id="5a4a6-111">For more information on how the gateway works, see [On-premises data gateway architecture](/data-integration/gateway/service-gateway-onprem-indepth).</span></span>

## <a name="types-of-gateways"></a><span data-ttu-id="5a4a6-112">เกตเวย์ประเภทต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="5a4a6-112">Types of gateways</span></span>

<span data-ttu-id="5a4a6-113">มีเกตเวย์สองชนิดที่แตกต่างกันสำหรับสถานการณ์ที่แตกต่างกัน:</span><span class="sxs-lookup"><span data-stu-id="5a4a6-113">There are two different types of gateways, each for a different scenario:</span></span>

* <span data-ttu-id="5a4a6-114">**เกตเวย์ข้อมูลภายในองค์กร** อนุญาตให้ผู้ใช้หลายรายเชื่อมต่อกับแหล่งข้อมูลภายในองค์กรหลายรายการได้</span><span class="sxs-lookup"><span data-stu-id="5a4a6-114">**On-premises data gateway** allows multiple users to connect to multiple on-premises data sources.</span></span> <span data-ttu-id="5a4a6-115">คุณสามารถใช้เกตเวย์ข้อมูลภายในองค์กรพร้อมด้วยบริการที่สนับสนุนทั้งหมดได้ด้วยการติดตั้งเกตเวย์เพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="5a4a6-115">You can use an on-premises data gateway with all supported services, with a single gateway installation.</span></span> <span data-ttu-id="5a4a6-116">เกตเวย์นี้เหมาะอย่างยิ่งสำหรับสถานการณ์ที่ซับซ้อน ซึ่งผู้ใช้หลายคนสามารถเข้าถึงแหล่งข้อมูลหลายรายการได้</span><span class="sxs-lookup"><span data-stu-id="5a4a6-116">This gateway is well-suited to complex scenarios with multiple people accessing multiple data sources.</span></span>

* <span data-ttu-id="5a4a6-117">**เกตเวย์ข้อมูลภายในองค์กร (โหมดส่วนบุคคล)** อนุญาตให้ผู้ใช้หนึ่งคนเชื่อมต่อกับแหล่งข้อมูล และไม่สามารถแชร์กับบุคคลอื่นได้</span><span class="sxs-lookup"><span data-stu-id="5a4a6-117">**On-premises data gateway (personal mode)** allows one user to connect to sources, and can’t be shared with others.</span></span> <span data-ttu-id="5a4a6-118">เกตเวย์ข้อมูลภายในองค์กร (โหมดส่วนบุคคล) สามารถใช้กับ Power BI ได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5a4a6-118">An on-premises data gateway (personal mode) can be used only with Power BI.</span></span> <span data-ttu-id="5a4a6-119">เกตเวย์นี้เหมาะที่สุดกับสถานการณ์ที่คุณเป็นเพียงบุคคลเดียวที่สร้างรายงาน และคุณไม่จำเป็นต้องใช้แหล่งข้อมูลใด ๆ ร่วมกันกับผู้อื่น</span><span class="sxs-lookup"><span data-stu-id="5a4a6-119">This gateway is well-suited to scenarios where you’re the only person who creates reports, and you don't need to share any data sources with others.</span></span>

## <a name="use-a-gateway"></a><span data-ttu-id="5a4a6-120">ใช้เกตเวย์</span><span class="sxs-lookup"><span data-stu-id="5a4a6-120">Use a gateway</span></span>

<span data-ttu-id="5a4a6-121">มีสี่ขั้นตอนหลักสำหรับการใช้เกตเวย์</span><span class="sxs-lookup"><span data-stu-id="5a4a6-121">There are four main steps for using a gateway.</span></span>

1. <span data-ttu-id="5a4a6-122">[ดาวน์โหลดและติดตั้งเกตเวย์](/data-integration/gateway/service-gateway-install)บนคอมพิวเตอร์เฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="5a4a6-122">[Download and install the gateway](/data-integration/gateway/service-gateway-install) on a local computer.</span></span>
1. <span data-ttu-id="5a4a6-123">[กำหนดค่า](/data-integration/gateway/service-gateway-app)เกตเวย์โดยอ้างอิงจากไฟร์วอลล์ของคุณและข้อกำหนดของเครือข่ายอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="5a4a6-123">[Configure](/data-integration/gateway/service-gateway-app) the gateway based on your firewall and other network requirements.</span></span>
1. <span data-ttu-id="5a4a6-124">[เพิ่มผู้ดูแลระบบเกตเวย์](/data-integration/gateway/service-gateway-manage) ซึ่งสามารถจัดการและดูแลข้อกำหนดของเครือข่ายอื่น ๆ ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="5a4a6-124">[Add gateway admins](/data-integration/gateway/service-gateway-manage) who can also manage and administer other network requirements.</span></span>
1. <span data-ttu-id="5a4a6-125">[ใช้เกตเวย์](service-gateway-sql-tutorial.md) เพื่อรีเฟรชแหล่งข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="5a4a6-125">[Use the gateway](service-gateway-sql-tutorial.md) to refresh an on-premises data source.</span></span>
1. <span data-ttu-id="5a4a6-126">[แก้ไขปัญหา](service-gateway-onprem-tshoot.md)เกตเวย์ในกรณีที่เกิดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="5a4a6-126">[Troubleshoot](service-gateway-onprem-tshoot.md) the gateway in case of errors.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5a4a6-127">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="5a4a6-127">Next steps</span></span>

* [<span data-ttu-id="5a4a6-128">ติดตั้งเกตเวย์ข้อมูลภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="5a4a6-128">Install the on-premises data gateway</span></span>](/data-integration/gateway/service-gateway-install)

<span data-ttu-id="5a4a6-129">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="5a4a6-129">More questions?</span></span> [<span data-ttu-id="5a4a6-130">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="5a4a6-130">Try the Power BI Community</span></span>](https://community.powerbi.com/)
