---
title: ปิดใช้งานการรีเฟรชพื้นหลังของ Power Query
description: คำแนะนำเมื่อปิดใช้งานการรีเฟรชพื้นหลังของ Power Query
author: peter-myers
ms.author: v-pemyer
manager: asaxton
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 09/26/2019
ms.openlocfilehash: 54e8524d2997e086b218e7d5b569e58ace21c48e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418658"
---
# <a name="disable-power-query-background-refresh"></a><span data-ttu-id="e4909-103">ปิดใช้งานการรีเฟรชพื้นหลังของ Power Query</span><span class="sxs-lookup"><span data-stu-id="e4909-103">Disable Power Query background refresh</span></span>

<span data-ttu-id="e4909-104">บทความนี้มุ่งเป้าหมายไปที่เรื่อง ตัวสร้างแบบจำลองข้อมูลนำเข้าที่ทำงานกับ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e4909-104">This article targets Import data modelers working with Power BI Desktop.</span></span>

<span data-ttu-id="e4909-105">ตามค่าเริ่มต้นเมื่อ Power Query นำเข้าข้อมูลจะยังเก็บแถวของข้อมูลตัวอย่างถึง 1000 แถวสำหรับแต่ละคิวรี</span><span class="sxs-lookup"><span data-stu-id="e4909-105">By default, when Power Query imports data, it also caches up to 1000 rows of preview data for each query.</span></span> <span data-ttu-id="e4909-106">ข้อมูลตัวอย่างจะช่วยแสดงตัวอย่างด่วนของข้อมูลต้นฉบับ และผลลัพธ์การแปลงสำหรับแต่ละขั้นตอนของแบบสอบถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="e4909-106">Preview data helps to present you with a quick preview of source data, and of transformation results for each step of your queries.</span></span> <span data-ttu-id="e4909-107">ซึ่งจะถูกเก็บแยกบนแผ่นดิสก์หรือไฟล์ภายในของ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e4909-107">It's stored separately on-disk and not inside the Power BI Desktop file.</span></span>

<span data-ttu-id="e4909-108">อย่างไรก็ตามเมื่อไฟล์ Power BI Desktop ของคุณมีแบบสอบถามจำนวนมาก การดึงและจัดเก็บข้อมูลการแสดงตัวอย่างสามารถขยายเวลาที่ใช้เพื่อทำการรีเฟรชให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e4909-108">However, when your Power BI Desktop file contains many queries, retrieving and storing preview data can extend the time it takes to complete a refresh.</span></span>

## <a name="recommendation"></a><span data-ttu-id="e4909-109">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="e4909-109">Recommendation</span></span>

<span data-ttu-id="e4909-110">คุณจะได้รับการรีเฟรชได้รวดเร็วยิ่งขึ้นโดยการตั้งค่าไฟล์ Power BI Desktop เพื่ออัปเด การแสดงตัวอย่างของแคช _ในพื้นหลัง_</span><span class="sxs-lookup"><span data-stu-id="e4909-110">You'll achieve a faster refresh by setting the Power BI Desktop file to update the preview cache _in the background_.</span></span> <span data-ttu-id="e4909-111">ใน Power BI Desktop คุณเปิดใช้งานโดยการเลือก _ไฟล์ > ตัวเลือกและการตั้งค่า > ตัวเลือก_ จากนั้นเลือกหน้า _โหลดข้อมูล_</span><span class="sxs-lookup"><span data-stu-id="e4909-111">In Power BI Desktop, you enable it by selecting _File > Options and settings > Options_, and then selecting the _Data Load_ page.</span></span> <span data-ttu-id="e4909-112">คุณสามารถเปิดตัวเลือก **การอนุญาตให้ดาวน์โหลดภาพแสดงตัวอย่างข้อมูลในพื้นหลัง**</span><span class="sxs-lookup"><span data-stu-id="e4909-112">You can then turn on the **Allow data preview to download in the background** option.</span></span> <span data-ttu-id="e4909-113">โปรดทราบว่าตัวเลือกนี้สามารถกำหนดสำหรับไฟล์ปัจจุบันได้</span><span class="sxs-lookup"><span data-stu-id="e4909-113">Note this option can only be set for the current file.</span></span>

![ภาพหน้าจอของ Power BI Desktop ที่แสดงตัวเลือกข้อมูลพื้นหลัง](media/power-query-background-refresh/power-query-options-background-data.png)

<span data-ttu-id="e4909-115">การเปิดใช้งานการรีเฟรชพื้นหลังสามารถทำให้ข้อมูลแสดงตัวอย่างหมดอายุแล้ว</span><span class="sxs-lookup"><span data-stu-id="e4909-115">Enabling background refresh can result in preview data becoming out of date.</span></span> <span data-ttu-id="e4909-116">ถ้าเกิดขึ้น ตัวแก้ไข Power Query จะแจ้งให้คุณทราบด้วยคำเตือนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e4909-116">If it occurs, the Power Query Editor will notify you with the following warning:</span></span>

![ภาพหน้าจอของหน้าต่าง Power BI Desktop ที่แสดงคำเตือนของตัวแก้ไข Power Query เกี่ยวกับข้อมูลตัวอย่างเก่า](media/power-query-background-refresh/power-query-preview-data-old.png)

<span data-ttu-id="e4909-118">สามารถอัปเดตแคชตัวอย่างได้</span><span class="sxs-lookup"><span data-stu-id="e4909-118">It's always possible to update the preview cache.</span></span> <span data-ttu-id="e4909-119">คุณสามารถอัปเดตสำหรับคิวรีเดียว หรือคิวรีทั้งหมดโดยใช้คำสั่ง **รีเฟรชตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="e4909-119">You can update it for a single query, or for all queries by using the **Refresh Preview** command.</span></span> <span data-ttu-id="e4909-120">คุณจะพบที่ริบบิ้น **หน้าหลัก** ของหน้าต่างตัวแก้ไข Power Query</span><span class="sxs-lookup"><span data-stu-id="e4909-120">You'll find it on the **Home** ribbon of the Power Query Editor window.</span></span>

![ภาพหน้าจอของหน้าต่าง Power BI Desktop ที่แสดงคำสั่งของตัวแก้ไข Power Query เพื่อรีเฟรชข้อมูลตัวอย่าง](media/power-query-background-refresh/power-query-refresh-preview-data.png)

## <a name="next-steps"></a><span data-ttu-id="e4909-122">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="e4909-122">Next steps</span></span>

<span data-ttu-id="e4909-123">สำหรับข้อมูลเพิ่มเติมที่เกี่ยวข้องกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e4909-123">For more information related to this article, check out the following resources:</span></span>

- [<span data-ttu-id="e4909-124">เอกสาร Power Query</span><span class="sxs-lookup"><span data-stu-id="e4909-124">Power Query Documentation</span></span>](/power-query/)
- <span data-ttu-id="e4909-125">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="e4909-125">Questions?</span></span> [<span data-ttu-id="e4909-126">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="e4909-126">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
