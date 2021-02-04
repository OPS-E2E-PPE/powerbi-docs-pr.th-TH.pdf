---
title: API ของการวิเคราะห์แบบฝังตัวของ Power BI ที่ใช้นโยบายการเก็บรักษาข้อมูลอัตโนมัติสำหรับข้อมูลแบบเรียลไทม์เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังตัวที่ดีขึ้น
description: เรียนรู้เกี่ยวกับนโยบายการเก็บรักษาข้อมูลโดยอัตโนมัติในบริการ Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: 81c975332abc4cb599a7172f1697c1b06ea34eba
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887741"
---
# <a name="automatic-retention-policy-for-real-time-data"></a><span data-ttu-id="eb092-104">นโยบายการเก็บข้อมูลโดยอัตโนมัติสำหรับข้อมูลแบบเรียลไทม์</span><span class="sxs-lookup"><span data-stu-id="eb092-104">Automatic retention policy for real-time data</span></span>

<span data-ttu-id="eb092-105">นโยบายการเก็บข้อมูลโดยอัตโนมัติในบริการ Power BI คือ พารามิเตอร์สตริงคิวรีที่อนุญาตให้การเก็บข้อมูลใหม่สามารถล้างข้อมูลเก่าโดยอัตโนมัติในขณะที่ยังคงรักษาความต่อเนื่องของข้อมูลใหม่ที่จะลงในแดชบอร์ดของคุณ</span><span class="sxs-lookup"><span data-stu-id="eb092-105">The automatic retention policy in the Power BI service is a query string parameter, which enables a default retention policy to automatically clean up old data while keeping a constant flow of new data going into your dashboard.</span></span> <span data-ttu-id="eb092-106">นโยบายการเก็บข้อมูลครั้งแรกจะเรียกว่า *ข้อมูลไหนเข้าก่อนข้อมูลนั้นออกก่อน (FIFO)*</span><span class="sxs-lookup"><span data-stu-id="eb092-106">The first retention policy is called *first in first out (FIFO)*.</span></span> <span data-ttu-id="eb092-107">เมื่อเปิดใช้งานจะสามารถเก็บรวบรวมข้อมูลในตารางจนกว่าจะถึง 200,000 แถว</span><span class="sxs-lookup"><span data-stu-id="eb092-107">When enabled, the data is collected in a table until it hits 200,000 rows.</span></span> <span data-ttu-id="eb092-108">เมื่อข้อมูลที่เกินกว่า 200,000 แถว ระบบจะค่อยๆ ทิ้งแถวเดิมในชุดข้อมูลออกไป</span><span class="sxs-lookup"><span data-stu-id="eb092-108">Once the data goes beyond 200,000 rows, the oldest rows get dropped from the dataset.</span></span> <span data-ttu-id="eb092-109">ซึ่งจะอยู่ระหว่างแถวที่ 200,000 ถึงแถวที่ 210,000 ของข้อมูลล่าสุดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="eb092-109">This maintains between 200,000 and 210,000 rows of only the latest data.</span></span>  
  
<center>

![นโยบายการเก็บข้อมูล](media/api-Automatic-retention-policy-for-real-time-data/retention-policy.png) 

</center>

<span data-ttu-id="eb092-111">นโยบายการเก็บข้อมูลจะเปิดใช้งานเมื่อคุณสร้างชุดข้อมูลครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="eb092-111">The retention policies are enabled when you first create your datasets.</span></span> <span data-ttu-id="eb092-112">สิ่งที่คุณต้องทำคือการเพิ่มพารามิเตอร์คิวรี "นโยบายการเก็บข้อมูลค่าเริ่มต้น" เข้าไปยังชุดข้อมูล POST ของคุณจากนั้นให้เรียกใช้และตั้งค่าเท่ากับ *basicFIFO*</span><span class="sxs-lookup"><span data-stu-id="eb092-112">All you need to do is add the "default retention policy" query parameter to your POST datasets call and set it equal to *basicFIFO*.</span></span>  

```console
POST https://api.powerbi.com/v1.0/myorg/datasets?defaultRetentionPolicy={None | basicFIFO}
```
