---
title: ข้อจำกัดของ Power BI REST API ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: 'Power BI REST API มีข้อจำกัดดังต่อไปนี้: เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI'
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: 1196917f0223ccde012d203d75c4e96fbc3b9dcf
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887672"
---
# <a name="power-bi-rest-api-limitations"></a><span data-ttu-id="289c5-104">ข้อจำกัดของ Power BI REST API</span><span class="sxs-lookup"><span data-stu-id="289c5-104">Power BI REST API limitations</span></span>  
  
<span data-ttu-id="289c5-105">**การโพสต์แถว**</span><span class="sxs-lookup"><span data-stu-id="289c5-105">**To POST Rows**</span></span>
  
* <span data-ttu-id="289c5-106">สูงสุด 75 คอลัมน์</span><span class="sxs-lookup"><span data-stu-id="289c5-106">75 max columns</span></span>
* <span data-ttu-id="289c5-107">สูงสุด 75 ตาราง</span><span class="sxs-lookup"><span data-stu-id="289c5-107">75 max tables</span></span>
* <span data-ttu-id="289c5-108">สามารถขอแถวได้สูงสุด 10,000 แถวต่อหนึ่งโพสต์</span><span class="sxs-lookup"><span data-stu-id="289c5-108">10,000 max rows per single POST rows request</span></span>  
* <span data-ttu-id="289c5-109">ภายใน 1 ชั่วโมงสามารถเพิ่มแถวได้ 1,000,000 แถวต่อหนึ่งชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="289c5-109">1,000,000 rows added per hour per dataset</span></span>  
* <span data-ttu-id="289c5-110">สามารถส่งคำขอโพสต์แถวได้สูงสุด 5 คำขอต่อหนึ่งชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="289c5-110">5 max pending POST rows requests per dataset</span></span>  
* <span data-ttu-id="289c5-111">ภายใน 1 นาทีสามารถส่งคำขอ 120 โพสต์แถวต่อหนึ่งชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="289c5-111">120 POST rows requests per minute per dataset</span></span>
* <span data-ttu-id="289c5-112">ถ้าตารางมีแถว 250,000 แถวหรือมากกว่า จะสามารถส่งคำขอได้ 120 โพสต์แถวต่อ 1ชั่วโมงสำหรับแต่ละชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="289c5-112">If table has 250,000 or more rows, 120 POST rows requests per hour per dataset</span></span>
* <span data-ttu-id="289c5-113">สามารถเก็บแถวได้สูงสุด 200,000 แถวต่อ 1 ตารางในชุดข้อมูล FIFO</span><span class="sxs-lookup"><span data-stu-id="289c5-113">200,000 max rows stored per table in FIFO dataset</span></span>
* <span data-ttu-id="289c5-114">สามารถเก็บแถวได้สูงสุด 5,000,000 แถวต่อ 1 ตารางในชุดข้อมูลที่ชื่อ ' ไม่มีข้อบังคับสำหรับการเก็บข้อมูล'</span><span class="sxs-lookup"><span data-stu-id="289c5-114">5,000,000 max rows stored per table in 'none retention policy' dataset</span></span>  
* <span data-ttu-id="289c5-115">ขั้นตอนการโพสต์แถวอนุญาตให้มีเพียง 4000 ตัวอักษรต่อค่าตัวเลขในสตริงคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="289c5-115">4,000 characters per value for string column in POST rows operation</span></span>
  
## <a name="see-also"></a><span data-ttu-id="289c5-116">นอกจากนี้ โปรดดู</span><span class="sxs-lookup"><span data-stu-id="289c5-116">See also</span></span>

* [<span data-ttu-id="289c5-117">ข้อจำกัดและข้อปฏิบัติของบริการ Azure AD</span><span class="sxs-lookup"><span data-stu-id="289c5-117">Azure AD service limits and restrictions</span></span>](/azure/active-directory/active-directory-service-limits-restrictions)   
* [<span data-ttu-id="289c5-118">ภาพรวมของ Power BI REST API</span><span class="sxs-lookup"><span data-stu-id="289c5-118">Overview of Power BI REST API</span></span>](/rest/api/power-bi/)