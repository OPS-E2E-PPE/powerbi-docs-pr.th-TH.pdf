---
title: ปรับข้อมูลของคุณให้เหมาะสมสำหรับข้อมูลเชิงลึกด่วนของ Power BI
description: ปรับข้อมูลของคุณให้เหมาะสมสำหรับข้อมูลเชิงลึกด่วนของ Power BI ถ้า Power BI ไม่พบข้อมูลเชิงลึกในข้อมูลของคุณ นี่คือสิ่งที่คุณสามารถทำได้
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 03/02/2017
LocalizationGroup: Dashboards
ms.openlocfilehash: 41250b3d6de7708912b82376a2a5f07d2e686105
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96388459"
---
# <a name="optimize-your-data-for-power-bi-quick-insights"></a><span data-ttu-id="a6d93-104">ปรับข้อมูลของคุณให้เหมาะสมสำหรับ ข้อมูลเชิงลึกด่วนของ Power BI</span><span class="sxs-lookup"><span data-stu-id="a6d93-104">Optimize your data for Power BI Quick Insights</span></span>
<span data-ttu-id="a6d93-105">ต้องการปรับปรุงผลลัพธ์ข้อมูลเชิงลึกด่วนหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="a6d93-105">Want to improve quick insights results?</span></span>  <span data-ttu-id="a6d93-106">ถ้าคุณเป็นเจ้าของชุดข้อมูล ลองขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="a6d93-106">If you are a dataset owner, try these:</span></span>

* <span data-ttu-id="a6d93-107">ซ่อนหรือยกเลิกการซ่อนคอลัมน์ในชุดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="a6d93-107">Hide or unhide columns in your dataset.</span></span> <span data-ttu-id="a6d93-108">ข้อมูลเชิงลึกด่วน Power BI ไม่ค้นหาคอลัมน์ที่ซ่อนอยู่</span><span class="sxs-lookup"><span data-stu-id="a6d93-108">Power BI quick insights doesn't search hidden columns.</span></span>  <span data-ttu-id="a6d93-109">ดังนั้นซ่อนคอลัมน์ที่ซ้ำกันหรือไม่จำเป็น และยกเลิกการซ่อนคอลัมน์ที่น่าสนใจ</span><span class="sxs-lookup"><span data-stu-id="a6d93-109">So hide duplicate or unnecessary columns and unhide interesting columns.</span></span>
* <span data-ttu-id="a6d93-110">ใช้ข้อมูลชนิดผสม เช่น ชื่อ เวลา วันที่ และตัวเลข</span><span class="sxs-lookup"><span data-stu-id="a6d93-110">Use a mix of data types such as names, times, dates, and numbers.</span></span>
* <span data-ttu-id="a6d93-111">หลีกเลี่ยง (หรือซ่อน) คอลัมน์ที่มีข้อมูลที่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="a6d93-111">Avoid (or hide) columns with duplicate information.</span></span>  <span data-ttu-id="a6d93-112">ซึ่งขั้นตอนนี้ช่วยประหยัดเวลาอันมีค่าในการค้นหารูปแบบที่มีความหมาย</span><span class="sxs-lookup"><span data-stu-id="a6d93-112">This takes valuable time away from searching for meaningful patterns.</span></span>  <span data-ttu-id="a6d93-113">ตัวอย่างเช่น หนึ่งคอลัมน์ที่แสดงชื่อที่ีสะกดทีละคำและอีกคอลัมน์ที่แสดงเป็นตัวย่อ</span><span class="sxs-lookup"><span data-stu-id="a6d93-113">For example, one column with state names spelled out and another column with state name abbreviations.</span></span>
* <span data-ttu-id="a6d93-114">คุณได้รับการข้อความข้อผิดพลาดที่ระบุว่า ข้อมูลของคุณไม่มีนัยสำคัญทางสถิติหรือไม่?</span><span class="sxs-lookup"><span data-stu-id="a6d93-114">Do you get an error message stating that your data isn't statistically significant?</span></span>  <span data-ttu-id="a6d93-115">ซึ่งสามารถเกิดขึ้นได้กับแบบจำลองที่เรียบง่ายมาก หรือแบบจำลองที่ไม่มีวันที่หรือตัวเลขคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="a6d93-115">This can happen with models that are very simple, or that don't have much data, or that don't have date or numeric columns.</span></span>

### <a name="next-steps"></a><span data-ttu-id="a6d93-116">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a6d93-116">Next steps</span></span>
[<span data-ttu-id="a6d93-117">ข้อมูลเชิงลึกด่วนใน Power BI</span><span class="sxs-lookup"><span data-stu-id="a6d93-117">Power BI quick insights</span></span>](../consumer/end-user-insights.md)

<span data-ttu-id="a6d93-118">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a6d93-118">More questions?</span></span> [<span data-ttu-id="a6d93-119">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="a6d93-119">Try the Power BI Community</span></span>](https://community.powerbi.com/)
