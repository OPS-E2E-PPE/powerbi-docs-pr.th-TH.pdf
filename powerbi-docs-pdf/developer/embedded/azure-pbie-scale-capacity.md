---
title: ปรับขนาดความจุ Power BI Embedded สำหรับโซลูชัน BI แบบฝังตัวของการวิเคราะห์แบบฝังของ Power BI ของคุณ
description: บทความนี้แนะนำเกี่ยวกับวิธีการปรับขนาดความจุ Power BI Embedded ใน Microsoft Azure สำหรับโซลูชัน BI แบบฝังตัวของการวิเคราะห์แบบฝังของ Power BI ของคุณ
author: KesemSharabi
ms.author: kesharab
services: power-bi-embedded
editor: ''
tags: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: how-to
ms.date: 01/31/2019
ms.openlocfilehash: 19dfff03e2ec17c2b969a80c9fe0d2087c189184
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887327"
---
# <a name="scale-your-power-bi-embedded-capacity-in-the-azure-portal"></a><span data-ttu-id="0c208-103">ปรับขนาดความจุ Power BI Embedded ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="0c208-103">Scale your Power BI Embedded capacity in the Azure portal</span></span>

<span data-ttu-id="0c208-104">บทความนี้แนะนำเกี่ยวกับวิธีการปรับขนาดความจุ Power BI Embedded ใน Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="0c208-104">This article walks through how to scale a Power BI Embedded capacity in Microsoft Azure.</span></span> <span data-ttu-id="0c208-105">การปรับขนาดช่วยให้คุณสามารถเพิ่มหรือลดขนาดความจุของคุณได้</span><span class="sxs-lookup"><span data-stu-id="0c208-105">Scaling allows you to increase or decrease the size of your capacity.</span></span>

<span data-ttu-id="0c208-106">ซึ่งถือว่า คุณได้สร้างขีดความจุ Power BI Embedded แล้ว</span><span class="sxs-lookup"><span data-stu-id="0c208-106">This assumes you have created a Power BI Embedded capacity.</span></span> <span data-ttu-id="0c208-107">หากคุณยังไม่ได้สร้าง ให้ดู[สร้างความจุ Power BI Embedded ในพอร์ทัล Azure](azure-pbie-create-capacity.md) เพื่อเริ่มใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0c208-107">If you have not, see [Create Power BI Embedded capacity in the Azure portal](azure-pbie-create-capacity.md) to get started.</span></span>

> [!NOTE]
> <span data-ttu-id="0c208-108">การดำเนินการปรับขนาดอาจใช้เวลาประมาณหนึ่งนาที</span><span class="sxs-lookup"><span data-stu-id="0c208-108">A scaling operation can take about a minute.</span></span> <span data-ttu-id="0c208-109">ในช่วงเวลานี้ จะไม่สามารถใช้งานความจุได้</span><span class="sxs-lookup"><span data-stu-id="0c208-109">During this time, the capacity will not be available.</span></span> <span data-ttu-id="0c208-110">การโหลดเนื้อหาแบบฝังตัวอาจล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="0c208-110">Embedded content may fail to load.</span></span>

## <a name="scale-a-capacity"></a><span data-ttu-id="0c208-111">ปรับขนาดความจุ</span><span class="sxs-lookup"><span data-stu-id="0c208-111">Scale a capacity</span></span>

1. <span data-ttu-id="0c208-112">ลงชื่อเข้าใช้[พอร์ทัล Azure](https://portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="0c208-112">Sign into the [Azure portal](https://portal.azure.com/).</span></span>

2. <span data-ttu-id="0c208-113">เลือก **บริการทั้งหมด** > **Power BI Embedded** เพื่อดูความจุของคุณ</span><span class="sxs-lookup"><span data-stu-id="0c208-113">Select **All services** > **Power BI Embedded** to see your capacities.</span></span>

    ![บริการทั้งหมดภายในพอร์ทัล Azure](media/azure-pbie-scale-capacity/azure-portal-more-services.png)

3. <span data-ttu-id="0c208-115">เลือกความจุที่คุณต้องการปรับขนาด</span><span class="sxs-lookup"><span data-stu-id="0c208-115">Select the capacity you want to scale.</span></span>

    ![รายการความจุ Power BI Embedded ในพอร์ทัล Azure](media/azure-pbie-scale-capacity/azure-portal-capacity-list.png)

4. <span data-ttu-id="0c208-117">เลือก **ระดับราคา** ภายใต้ **มาตราส่วน** ภายในความจุของคุณ</span><span class="sxs-lookup"><span data-stu-id="0c208-117">Select **Pricing tier** under **Scale** within your capacity.</span></span>

    ![ตัวเลือกระดับราคาภายใต้มาตราส่วน](media/azure-pbie-scale-capacity/azure-portal-scale-pricing-tier.png)

    <span data-ttu-id="0c208-119">ระดับการกำหนดราคาปัจจุบันของคุณจะมีกรอบเป็นสีฟ้า</span><span class="sxs-lookup"><span data-stu-id="0c208-119">Your current pricing tier is outlined in blue.</span></span>

    ![ระดับการกำหนดราคาปัจจุบันของคุณจะมีกรอบเป็นสีฟ้า](media/azure-pbie-scale-capacity/azure-portal-current-tier.png)

5. <span data-ttu-id="0c208-121">เมื่อต้องการปรับมาตราส่วนขึ้นหรือลง เลือกระดับใหม่เพื่อย้ายไปยังตำแหน่งที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0c208-121">To scale up or down, select the new tier to move to.</span></span> <span data-ttu-id="0c208-122">การเลือกระดับใหม่จะวางเส้นขอบสีฟ้าล้อมรอบบริเวณที่เลือกไว้</span><span class="sxs-lookup"><span data-stu-id="0c208-122">Selecting a new tier places a dashed blue outline around the selection.</span></span> <span data-ttu-id="0c208-123">เลือก **เลือก** เพื่อปรับขนาดเป็นระดับใหม่</span><span class="sxs-lookup"><span data-stu-id="0c208-123">Select **Select** to scale to the new tier.</span></span>

    ![เลือกระดับใหม่](media/azure-pbie-scale-capacity/azure-portal-select-new-tier.png)

    <span data-ttu-id="0c208-125">การปรับขนาดความจุของคุณอาจใช้เวลาสักครู่หรือสองนาทีจึงจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="0c208-125">Scaling your capacity may take a minute or two to complete.</span></span>

6. <span data-ttu-id="0c208-126">ยืนยันระดับของคุณโดยดูจากแท็บภาพรวม ระดับการกำหนดราคาปัจจุบันจะแสดงอยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="0c208-126">Confirm your tier by viewing the overview tab. The current pricing tier is listed.</span></span>

    ![ยืนยันระดับปัจจุบัน](media/azure-pbie-scale-capacity/azure-portal-confirm-tier.png)

## <a name="next-steps"></a><span data-ttu-id="0c208-128">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="0c208-128">Next steps</span></span>

<span data-ttu-id="0c208-129">ในการหยุดชั่วคราวหรือเริ่มต้นความจุของคุณ ให้ดูที[่หยุดชั่วคราวและเริ่มต้นความจุ Power BI Embedded ในพอร์ทัล Azure](azure-pbie-pause-start.md)</span><span class="sxs-lookup"><span data-stu-id="0c208-129">To pause or start your capacity, see [Pause and start your Power BI Embedded capacity in the Azure portal](azure-pbie-pause-start.md).</span></span>

<span data-ttu-id="0c208-130">ในการเริ่มต้นฝังเนื้อหา Power BI ในแอปพลิเคชันของคุณ โปรดดูที่[วิธีฝังแดชบอร์ด รายงาน และไทล์ใน Power BI ของคุณ](https://powerbi.microsoft.com/documentation/powerbi-developer-embedding-content/)</span><span class="sxs-lookup"><span data-stu-id="0c208-130">To begin embedding Power BI content within your application, see [How to embed your Power BI dashboards, reports, and tiles](https://powerbi.microsoft.com/documentation/powerbi-developer-embedding-content/).</span></span>

<span data-ttu-id="0c208-131">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0c208-131">More questions?</span></span> [<span data-ttu-id="0c208-132">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="0c208-132">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
