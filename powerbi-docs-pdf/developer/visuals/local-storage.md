---
title: API ที่เก็บข้อมูลภายในของวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายวิธีการใช้ API ของวิชวล Power BI เพื่อเข้าถึงที่เก็บข้อมูลภายในเครื่องของเบราว์เซอร์ เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: rkarlin
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: reference
ms.date: 01/21/2019
ms.openlocfilehash: abec68c5622d3dcd96746148ed7a6da4f06c8ec0
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888201"
---
# <a name="local-storage-api"></a><span data-ttu-id="3e343-104">API ที่เก็บข้อมูลภายใน</span><span class="sxs-lookup"><span data-stu-id="3e343-104">Local Storage API</span></span>

<span data-ttu-id="3e343-105">API ที่เก็บข้อมูลภายในคือ API ที่วิชวลแบบกำหนดเองสามารถใช้เพื่อร้องขอให้โฮสต์ทำการบันทึกหรือโหลดข้อมูลจากที่จัดเก็บของอุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="3e343-105">The Local Storage API is an API a custom visual can use to request the host to save or load data from the device's storage.</span></span> <span data-ttu-id="3e343-106">ซึ่งแยกจากกันได้โดยการแยกการเข้าถึงพื้นที่เก็บข้อมูลระหว่างวิชวลชนิดที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="3e343-106">It's isolated in the sense that there's separation of storage access between different visual types.</span></span>

## <a name="sample"></a><span data-ttu-id="3e343-107">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3e343-107">Sample</span></span>

<span data-ttu-id="3e343-108">ถ้าวิชวลแบบกำหนดเองควรเพิ่มตัวนับบางตัวทุกครั้งที่มีการเรียกใช้วิธีการอัปเดต แต่ค่าตัวนับควรคงไว้และไม่ได้ตั้งค่าใหม่ในทุกครั้งที่เริ่มต้นวิชวล:</span><span class="sxs-lookup"><span data-stu-id="3e343-108">If the custom visual should increase some counter every time the update method is called, but the counter value should also be preserved and not reset on every visual start:</span></span>

```typescript
export class Visual implements IVisual {
        // ...
        private updateCountName: string = 'updateCount';
        private updateCount: number;
        private storage: ILocalVisualStorageService;
        // ...

        constructor(options: VisualConstructorOptions) {
            // ...
            this.storage = options.host.storageService;
            // ...

            this.storage.get(this.updateCountName).then(count =>
            {
                this.updateCount = +count;
            })
            .catch(() =>
            {
                this.updateCount = 0;
                this.storage.set(this.updateCountName, this.updateCount.toString());
            });
            // ...
        }

        public update(options: VisualUpdateOptions) {
            // ...
            this.updateCount++;
            this.storage.set(this.updateCountName, this.updateCount.toString());
            // ...
        }
}
```

## <a name="known-limitations-and-issues"></a><span data-ttu-id="3e343-109">ข้อจำกัดและปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="3e343-109">Known limitations and issues</span></span>

<span data-ttu-id="3e343-110">API ที่เก็บข้อมูลภายในจะไม่ถูกเปิดใช้งานสำหรับวิชวล Power BI ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3e343-110">Local Storage API isn't activated for Power BI visuals by default.</span></span> <span data-ttu-id="3e343-111">ถ้าคุณต้องการเปิดใช้งานสำหรับวิชวล Power BI ของคุณ โปรดส่งคำขอไปยังฝ่ายสนับสนุนวิชวล Power BI `pbicvsupport@microsoft.com`</span><span class="sxs-lookup"><span data-stu-id="3e343-111">If you want to activate it for your Power BI visual, send a request to Power BI visuals Support `pbicvsupport@microsoft.com`.</span></span>  
<span data-ttu-id="3e343-112">**โปรดทราบว่าวิชวลของคุณควรมีอยู่ใน [AppSource](https://appsource.microsoft.com/en-us/marketplace/apps?product=power-bi-visuals) และ [ได้รับการรับรอง](https://powerbi.microsoft.com/en-us/documentation/powerbi-custom-visuals-certified/)**</span><span class="sxs-lookup"><span data-stu-id="3e343-112">**Please note that your visual should be available in [AppSource](https://appsource.microsoft.com/en-us/marketplace/apps?product=power-bi-visuals) and be [certified](https://powerbi.microsoft.com/en-us/documentation/powerbi-custom-visuals-certified/).**</span></span>
