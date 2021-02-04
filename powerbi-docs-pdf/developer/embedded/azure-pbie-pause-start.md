---
title: เพื่อหยุดชั่วคราวและเริ่มต้นความจุ Power BI Embedded ในพอร์ทัล Azure สำหรับโซลูชัน BI แบบฝังตัวของการวิเคราะห์แบบฝังของ Power BI ของคุณ
description: บทความนี้แนะนำเกี่ยวกับวิธีการหยุดชั่วคราวและเริ่มต้นความจุ Power BI Embedded ใน Microsoft Azure เมื่อใช้งานโซลูชัน BI แบบฝังตัวของการวิเคราะห์แบบฝังของ Power BI
author: KesemSharabi
ms.author: kesharab
services: power-bi-embedded
editor: ''
tags: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: how-to
ms.date: 09/28/2017
ms.openlocfilehash: 0868d63f83f42bcfa9f394e782ffab56746e23cc
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887350"
---
# <a name="pause-and-start-your-power-bi-embedded-capacity-in-the-azure-portal"></a><span data-ttu-id="ec2a4-103">เพื่อหยุดชั่วคราวและเริ่มต้นความจุ Power BI Embedded ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="ec2a4-103">Pause and start your Power BI Embedded capacity in the Azure portal</span></span>

<span data-ttu-id="ec2a4-104">บทความนี้แนะนำเกี่ยวกับวิธีการหยุดชั่วคราวและเริ่มต้น Power BI Embedded ใน Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="ec2a4-104">This article walks through how to pause and start a Power BI Embedded capacity in Microsoft Azure.</span></span> <span data-ttu-id="ec2a4-105">ซึ่งถือว่า คุณได้สร้างขีดความจุ Power BI Embedded แล้ว</span><span class="sxs-lookup"><span data-stu-id="ec2a4-105">This assumes you have created a Power BI Embedded capacity.</span></span> <span data-ttu-id="ec2a4-106">หากคุณยังไม่ได้สร้าง ให้ดู[สร้างความจุ Power BI Embedded ในพอร์ทัล Azure](azure-pbie-create-capacity.md) เพื่อเริ่มใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ec2a4-106">If you have not, see [Create Power BI Embedded capacity in the Azure portal](azure-pbie-create-capacity.md) to get started.</span></span>

<span data-ttu-id="ec2a4-107">ถ้าคุณยังไม่มีการสมัครใช้งาน Azure สร้าง[บัญชีฟรี](https://azure.microsoft.com/free/)ก่อนที่คุณจะเริ่ม</span><span class="sxs-lookup"><span data-stu-id="ec2a4-107">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/) before you begin.</span></span>

## <a name="pause-your-capacity"></a><span data-ttu-id="ec2a4-108">หยุดความจุของคุณชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="ec2a4-108">Pause your capacity</span></span>

<span data-ttu-id="ec2a4-109">การหยุดความจุของคุณชั่วคราวช่วยป้องกันไม่ให้คุณถูกเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="ec2a4-109">Pausing your capacity prevents you from being billed.</span></span> <span data-ttu-id="ec2a4-110">การหยุดความจุของคุณชั่วคราวจะเป็นเรื่องที่เยี่ยมยอด ่ถ้าคุณไม่จำเป็นต้องใช้ความจุเป็นระยะเวลาหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ec2a4-110">Pausing your capacity is great if you do not need to use the capacity for a period of time.</span></span> <span data-ttu-id="ec2a4-111">ใช้ขั้นตอนต่อไปนี้เพื่อหยุดความจุของคุณชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="ec2a4-111">Use the following steps to pause your capacity.</span></span>

> [!NOTE]
> <span data-ttu-id="ec2a4-112">การหยุดความจุชั่วคราวอาจทำให้เนื้อหาไม่พร้อมใช้งานภายใน Power BI</span><span class="sxs-lookup"><span data-stu-id="ec2a4-112">Pausing a capacity may prevent content from being available within Power BI.</span></span> <span data-ttu-id="ec2a4-113">ตรวจสอบว่าได้ยกเลิกการมอบหมายพื้นที่ทำงานจากความจุของคุณก่อนที่จะหยุดชั่วคราวเพื่อป้องกันไม่ให้ถูกขัดจังหวะ</span><span class="sxs-lookup"><span data-stu-id="ec2a4-113">Make sure to unassign workspaces from your capacity before pausing to prevent interruption.</span></span>

1. <span data-ttu-id="ec2a4-114">ลงชื่อเข้าใช้[พอร์ทัล Azure](https://portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="ec2a4-114">Sign into the [Azure portal](https://portal.azure.com/).</span></span>

2. <span data-ttu-id="ec2a4-115">เลือก **บริการทั้งหมด** > **Power BI Embedded** เพื่อดูความจุของคุณ</span><span class="sxs-lookup"><span data-stu-id="ec2a4-115">Select **All services** > **Power BI Embedded** to see your capacities.</span></span>

    ![บริการทั้งหมดภายในพอร์ทัล Azure](media/azure-pbie-pause-start/azure-portal-more-services.png)

3. <span data-ttu-id="ec2a4-117">เลือกความจุที่คุณต้องการหยุดชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="ec2a4-117">Select the capacity you want to pause.</span></span>

    ![รายการความจุ Power BI Embedded ในพอร์ทัล Azure](media/azure-pbie-pause-start/azure-portal-capacity-list.png)

4. <span data-ttu-id="ec2a4-119">เลือก **หยุดชั่วคราว** ภายในรายละเอียดความจุ</span><span class="sxs-lookup"><span data-stu-id="ec2a4-119">Select **Pause** within the capacity details.</span></span>

    ![หยุดความจุของคุณชั่วคราว](media/azure-pbie-pause-start/azure-portal-pause-capacity.png)

5. <span data-ttu-id="ec2a4-121">เลือก **ใช่** ซึ่งยืนยันว่าคุณต้องการหยุดความจุชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="ec2a4-121">Select **Yes**, which confirms you want to pause the capacity.</span></span>

    ![ยืนยันหยุดชั่วคราว](media/azure-pbie-pause-start/azure-portal-confirm-pause.png)

## <a name="start-your-capacity"></a><span data-ttu-id="ec2a4-123">เริ่มต้นความจุของคุณชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="ec2a4-123">Start your capacity</span></span>

<span data-ttu-id="ec2a4-124">กลับมาใช้งานโดยเริ่มต้นความจุของคุณอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="ec2a4-124">Resume usage by starting your capacity.</span></span> <span data-ttu-id="ec2a4-125">เริ่มต้นความจุของคุณ รวมถึงดำเนินการเรียกเก็บเงินต่ออีกด้วย</span><span class="sxs-lookup"><span data-stu-id="ec2a4-125">Starting your capacity also resumes billing.</span></span>

1. <span data-ttu-id="ec2a4-126">ลงชื่อเข้าใช้[พอร์ทัล Azure](https://portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="ec2a4-126">Sign into the [Azure portal](https://portal.azure.com/).</span></span>

2. <span data-ttu-id="ec2a4-127">เลือก **บริการทั้งหมด** > **Power BI Embedded** เพื่อดูความจุของคุณ</span><span class="sxs-lookup"><span data-stu-id="ec2a4-127">Select **All services** > **Power BI Embedded** to see your capacities.</span></span>

    ![บริการทั้งหมดภายในพอร์ทัล Azure](media/azure-pbie-pause-start/azure-portal-more-services.png)

3. <span data-ttu-id="ec2a4-129">เลือกความจุที่คุณต้องการเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ec2a4-129">Select the capacity you want to start.</span></span>

    ![รายการความจุ Power BI Embedded ในพอร์ทัล Azure](media/azure-pbie-pause-start/azure-portal-capacity-list.png)

4. <span data-ttu-id="ec2a4-131">เลือก **เริ่มต้น** ภายในรายละเอียดความจุ</span><span class="sxs-lookup"><span data-stu-id="ec2a4-131">Select **Start** within the capacity details.</span></span>

    ![เริ่มต้นความจุของคุณชั่วคราว](media/azure-pbie-pause-start/azure-portal-start-capacity.png)

5. <span data-ttu-id="ec2a4-133">เลือก **ใช่** ซึ่งยืนยันว่าคุณต้องกาเริ่มต้นความจุ</span><span class="sxs-lookup"><span data-stu-id="ec2a4-133">Select **Yes**, which confirms you want to start the capacity.</span></span>

    ![ยืนยันการเริ่มต้น](media/azure-pbie-pause-start/azure-portal-confirm-start.png)

<span data-ttu-id="ec2a4-135">หากมีการกำหนดเนื้อหาไปยังความจุนี้ เนื้อหาจะสามารถใช้งานได้เมื่อเริ่มต้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="ec2a4-135">If any content is assigned to this capacity, it is available once started.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ec2a4-136">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="ec2a4-136">Next steps</span></span>

<span data-ttu-id="ec2a4-137">ถ้าคุณต้องการปรับขนาดความจุของคุณขึ้นหรือลงดู[ปรับขนาดความจุ Power BI Embedded ของคุณ](azure-pbie-scale-capacity.md)</span><span class="sxs-lookup"><span data-stu-id="ec2a4-137">If you want to scale your capacity up or down, see [Scale your Power BI Embedded capacity](azure-pbie-scale-capacity.md).</span></span>

<span data-ttu-id="ec2a4-138">ในการเริ่มต้นฝังเนื้อหา Power BI ในแอปพลิเคชันของคุณ โปรดดูที่[วิธีฝังแดชบอร์ด รายงาน และไทล์ใน Power BI ของคุณ](https://powerbi.microsoft.com/documentation/powerbi-developer-embedding-content/)</span><span class="sxs-lookup"><span data-stu-id="ec2a4-138">To begin embedding Power BI content within your application, see [How to embed your Power BI dashboards, reports and tiles](https://powerbi.microsoft.com/documentation/powerbi-developer-embedding-content/).</span></span>

<span data-ttu-id="ec2a4-139">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="ec2a4-139">More questions?</span></span> [<span data-ttu-id="ec2a4-140">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="ec2a4-140">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)