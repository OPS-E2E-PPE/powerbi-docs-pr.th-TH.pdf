---
title: เพิ่มหน้าเริ่มต้น (Landing Page) ไปยังวิชวล Power BI ของคุณในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีเพิ่มหน้าเริ่มต้นไปยังวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: reference
ms.date: 06/18/2019
ms.openlocfilehash: 4381ecf63c0864c4d68e48959efc14baa9d4553b
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97886361"
---
# <a name="add-a-landing-page-to-your-power-bi-visuals"></a><span data-ttu-id="5530f-104">เพิ่มหน้าเริ่มต้น (landing page) ไปยังวิชวล Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5530f-104">Add a landing page to your Power BI visuals</span></span>

<span data-ttu-id="5530f-105">ด้วย API 2.3.0 คุณสามารถเพิ่มหน้าเริ่มต้นไปยังวิชวล Power BI ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="5530f-105">With API 2.3.0, you can add a landing page to your Power BI visuals.</span></span> <span data-ttu-id="5530f-106">เมื่อต้องการทำเช่นนั้น ให้เพิ่ม `supportsLandingPage` ไปยังความสามารถและตั้งค่าเป็น จริง</span><span class="sxs-lookup"><span data-stu-id="5530f-106">To do so, add `supportsLandingPage` to the capabilities, and set it to true.</span></span> <span data-ttu-id="5530f-107">การดำเนินการนี้จะเริ่มต้นและอัปเดตวิชวลของคุณก่อนที่คุณจะเพิ่มข้อมูลลงไป</span><span class="sxs-lookup"><span data-stu-id="5530f-107">This action initializes and updates your visual before you add data to it.</span></span> <span data-ttu-id="5530f-108">เนื่องจากวิชวลจะไม่แสดงลายน้ำอีกต่อไป คุณสามารถออกแบบหน้าเริ่มต้นของคุณเองเพื่อให้แสดงในวิชวลได้ตราบใดที่ไม่มีข้อมูลอยู่</span><span class="sxs-lookup"><span data-stu-id="5530f-108">Because the visual no longer shows a watermark, you can design your own landing page to be displayed in the visual as long as it has no data.</span></span>

```typescript
export class BarChart implements IVisual {
    //...
    private element: HTMLElement;
    private isLandingPageOn: boolean;
    private LandingPageRemoved: boolean;
    private LandingPage: d3.Selection<any>;

    constructor(options: VisualConstructorOptions) {
            //...
            this.element = options.element;
            //...
    }

    public update(options: VisualUpdateOptions) {
    //...
        this.HandleLandingPage(options);
    }

    private HandleLandingPage(options: VisualUpdateOptions) {
        if(!options.dataViews || !options.dataViews.length) {
            if(!this.isLandingPageOn) {
                this.isLandingPageOn = true;
                const SampleLandingPage: Element = this.createSampleLandingPage(); //create a landing page
                this.element.appendChild(SampleLandingPage);
                this.LandingPage = d3.select(SampleLandingPage);
            }

        } else {
                if(this.isLandingPageOn && !this.LandingPageRemoved){
                    this.LandingPageRemoved = true;
                    this.LandingPage.remove();
                }
        }
    }
```

<span data-ttu-id="5530f-109">ตัวอย่างหน้าเริ่มต้นจะแสดงในรูปต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5530f-109">An example landing page is shown in the following image:</span></span>

![สกรีนช็อตของหน้าเริ่มต้น](media/landing-page/app-landing-page.png)
