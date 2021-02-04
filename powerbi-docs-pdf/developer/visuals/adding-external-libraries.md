---
title: การเพิ่มไลบรารีภายนอกไปยังวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการใช้ไลบรารีภายนอกในการแสดงผลด้วยภาพของ Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.date: 02/24/2020
ms.openlocfilehash: b9a443040384e4d38bd7440eae0a5582cc422836
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97889190"
---
# <a name="adding-external-libraries"></a><span data-ttu-id="9265d-104">การเพิ่มไลบรารีภายนอก</span><span class="sxs-lookup"><span data-stu-id="9265d-104">Adding external libraries</span></span>

<span data-ttu-id="9265d-105">บทความนี้อธิบายวิธีการใช้ไลบรารีภายนอกในการแสดงผลด้วยภาพของ Power BI</span><span class="sxs-lookup"><span data-stu-id="9265d-105">This article describes how to use external libraries in Power BI visuals.</span></span> <span data-ttu-id="9265d-106">ซึ่งรวมถึงข้อมูลเกี่ยวกับการติดตั้ง การนำเข้า และเรียกใช้ไลบรารีภายนอกจากรหัสของการแสดงผลด้วยภาพของ Power BI</span><span class="sxs-lookup"><span data-stu-id="9265d-106">It includes information about installing, importing, and calling external libraries from the Power BI visual's code.</span></span>

## <a name="javascript-libraries"></a><span data-ttu-id="9265d-107">ไลบรารี JavaScript</span><span class="sxs-lookup"><span data-stu-id="9265d-107">JavaScript libraries</span></span>

1. <span data-ttu-id="9265d-108">ติดตั้งไลบรารี JavaScript ภายนอกโดยใช้ตัวจัดการแพคเกจต่างๆ เช่น *npm* หรือ *yarn*</span><span class="sxs-lookup"><span data-stu-id="9265d-108">Install an external JavaScript library by using any package manager such as *npm* or *yarn*.</span></span>
2. <span data-ttu-id="9265d-109">นำเข้าโมดูลที่จำเป็นลงในไฟล์ต้นฉบับโดยใช้ไลบรารีภายนอก</span><span class="sxs-lookup"><span data-stu-id="9265d-109">Import the required modules into the source files using the external library.</span></span>

>[!NOTE]
><span data-ttu-id="9265d-110">ถ้าคุณต้องการเพิ่ม typings ไปยังไลบรารี JavaScript ของคุณและรับข้อมูลความปลอดภัยและการคอมไพล์ในขณะนี้ โปรดตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งแพคเกจที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="9265d-110">If you'd like to add typings to your JavaScript library, and get intellisense and compile-time safety, make sure that you install the appropriate package.</span></span>

### <a name="installing-the-d3-library"></a><span data-ttu-id="9265d-111">การติดตั้งไลบรารี d3</span><span class="sxs-lookup"><span data-stu-id="9265d-111">Installing the d3 library</span></span>

<span data-ttu-id="9265d-112">นี่คือตัวอย่างของการติดตั้ง[ไลบรารี d3](https://www.npmjs.com/package/d3) [และแพคเกจ@types/d3](https://www.npmjs.com/package/@types/d3) โดยใช้ [npm](https://www.npmjs.com/)</span><span class="sxs-lookup"><span data-stu-id="9265d-112">This is an example of installing the [d3 library](https://www.npmjs.com/package/d3) and the [@types/d3](https://www.npmjs.com/package/@types/d3) package, using [npm](https://www.npmjs.com/).</span></span>

<span data-ttu-id="9265d-113">สำหรับตัวอย่างเต็มรูปแบบ โปรดดูรหัส[การแสดงภาพ Power BI](https://github.com/microsoft/powerbi-visuals-gantt/blob/master/src/gantt.ts#L29)</span><span class="sxs-lookup"><span data-stu-id="9265d-113">For a full example, see the [Power BI visualizations](https://github.com/microsoft/powerbi-visuals-gantt/blob/master/src/gantt.ts#L29) code.</span></span>

1. <span data-ttu-id="9265d-114">ติดตั้งแพคเกจ *d3* และแพคเกจ *ชนิด d3*</span><span class="sxs-lookup"><span data-stu-id="9265d-114">Install the *d3* package and the *d3 types* package.</span></span>

    ```powershell
    npm install d3@5 --save
    npm install @types/d3@5 --save
    ```

2. <span data-ttu-id="9265d-115">นำเข้าไลบรารี *d3* ในไฟล์ที่ใช้เช่น `visual.ts`</span><span class="sxs-lookup"><span data-stu-id="9265d-115">Import the *d3* library in the files that use it, such as `visual.ts`.</span></span>

    ```typescript
    import * as d3 from "d3";
    ```

## <a name="css-framework"></a><span data-ttu-id="9265d-116">CSS framework</span><span class="sxs-lookup"><span data-stu-id="9265d-116">CSS framework</span></span>

1. <span data-ttu-id="9265d-117">ติดตั้งไลบรารี JavaScript ภายนอกโดยใช้ตัวจัดการแพคเกจต่างๆ เช่น *npm* หรือ *yarn*</span><span class="sxs-lookup"><span data-stu-id="9265d-117">Install an external CSS framework by using any package manager such as *npm* or *yarn*.</span></span>
2. <span data-ttu-id="9265d-118">ใน`.less`ไฟล์ของการแสดงผลด้วยภาพ รวมถึง`import`คำสั่ง</span><span class="sxs-lookup"><span data-stu-id="9265d-118">In the `.less` file of the visual, include the `import` statement.</span></span>

### <a name="installing-bootstrap"></a><span data-ttu-id="9265d-119">กำลังติดตั้ง bootstrap</span><span class="sxs-lookup"><span data-stu-id="9265d-119">Installing bootstrap</span></span>

<span data-ttu-id="9265d-120">นี่คือตัวอย่างของการติดตั้ง [bootstrap](https://www.npmjs.com/package/bootstrap) จากการใช้ [npm](https://www.npmjs.com/)</span><span class="sxs-lookup"><span data-stu-id="9265d-120">This is an example of installing [bootstrap](https://www.npmjs.com/package/bootstrap) using [npm](https://www.npmjs.com/).</span></span>

<span data-ttu-id="9265d-121">สำหรับตัวอย่างเต็มรูปแบบ โปรดดูรหัส[การแสดงภาพ Power BI](https://github.com/Microsoft/powerbi-visuals-sankey/blob/c8200da56913cd8b253be949a35fad0f4472b6de/style/visual.less#L32)</span><span class="sxs-lookup"><span data-stu-id="9265d-121">For a full example, see the [Power BI visualizations](https://github.com/Microsoft/powerbi-visuals-sankey/blob/c8200da56913cd8b253be949a35fad0f4472b6de/style/visual.less#L32) code.</span></span>

1. <span data-ttu-id="9265d-122">ติดตั้งแพคเกจ *bootstrap*</span><span class="sxs-lookup"><span data-stu-id="9265d-122">Install the *bootstrap* package.</span></span>

    ```powershell
    npm install bootstrap --save
    ```

2. <span data-ttu-id="9265d-123">รวม`import`คำสั่งใน`visual.less`</span><span class="sxs-lookup"><span data-stu-id="9265d-123">Include the `import` statement in `visual.less`.</span></span>

    ```less
    @import (less) "node_modules/bootstrap/dist/css/bootstrap.css";
    ```
