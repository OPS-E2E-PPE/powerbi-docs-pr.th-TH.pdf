---
title: 'การแก้ไข: "ความล้มเหลวในการสื่อสาร" ในแอปสำหรับอุปกรณ์เคลื่อนที่ iOS - Power BI'
description: บทความนี้อาจช่วยคุณได้ถ้าคุณเห็นข้อความนี้, 'เราพบความล้มเหลวในการสื่อสาร ความล้มเหลวอาจเกี่ยวข้องกับการตั้งค่าพร็อกซีบนการเชื่อมต่อ Wi-Fi ของคุณ'
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-mobile
ms.topic: conceptual
ms.date: 03/11/2020
ms.openlocfilehash: 1af46edad96ce191798502a1887c6c402a0e7319
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415346"
---
# <a name="fixing-communication-failures-in-ios-mobile-apps---power-bi"></a><span data-ttu-id="a7ee6-104">การแก้ไข: "ความล้มเหลวในการสื่อสาร" ในแอปสำหรับอุปกรณ์เคลื่อนที่ iOS - Power BI</span><span class="sxs-lookup"><span data-stu-id="a7ee6-104">Fixing "communication failures" in iOS mobile apps - Power BI</span></span>

| ![iPhone](./media/mobile-known-issues-with-the-iphone-app/iphone-logo-50-px.png) | ![iPad](./media/mobile-known-issues-with-the-iphone-app/ipad-logo-50-px.png) |
|:--- |:--- |
| <span data-ttu-id="a7ee6-107">iPhones</span><span class="sxs-lookup"><span data-stu-id="a7ee6-107">iPhones</span></span> |<span data-ttu-id="a7ee6-108">iPad</span><span class="sxs-lookup"><span data-stu-id="a7ee6-108">iPads</span></span> |

## <a name="we-encountered-communication-failures"></a><span data-ttu-id="a7ee6-109">"เราพบความล้มเหลวในการสื่อสาร"</span><span class="sxs-lookup"><span data-stu-id="a7ee6-109">"We encountered communication failures"</span></span>
<span data-ttu-id="a7ee6-110">"เราพบความล้มเหลวในการสื่อสาร</span><span class="sxs-lookup"><span data-stu-id="a7ee6-110">"We encountered communication failures.</span></span> <span data-ttu-id="a7ee6-111">ความล้มเหลวอาจเกี่ยวข้องกับการตั้งค่าพร็อกซีบนการเชื่อมต่อ Wi-Fi ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a7ee6-111">The failures might be related to proxy settings on your Wi-Fi connection.</span></span> <span data-ttu-id="a7ee6-112">การสลับไปยังการเชื่อมต่อ Wi-Fi อื่นอาจแก้ปัญหาได้"</span><span class="sxs-lookup"><span data-stu-id="a7ee6-112">Switching to a  different Wi-Fi connection may resolve the issue."</span></span>

<span data-ttu-id="a7ee6-113">คุณอาจเห็นข้อความนี้ถ้าการเชื่อมต่ออินเทอร์เน็ตของ iPhone หรือ iPad ต้องใช้พร็อกซี HTTP ที่ถูกกำหนดค่าที่บังคับชัดเจนไม่ว่าด้วยตนเองหรืออัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a7ee6-113">You may see this message if your iPhone or iPad internet connection requires a mandatory explicit HTTP proxy configured, either manual or automatic.</span></span> <span data-ttu-id="a7ee6-114">ในกรณีนี้ แอป Power BI จะไม่ทำงานบนอุปกรณ์ iOS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a7ee6-114">In this case, the Power BI app won't work on your iOS device.</span></span>

### <a name="workaround"></a><span data-ttu-id="a7ee6-115">วิธีการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="a7ee6-115">Workaround</span></span>
<span data-ttu-id="a7ee6-116">สลับ iPhone หรือ iPad ไปยังการเชื่อมต่ออื่นที่ไม่จำเป็นต้องมีการตั้งค่าพร็อกซี HTTP อย่างชัดเจน (เช่น ตัวที่กำหนดค่าเป็นพร็อกซี HTTP นั้นปิดอยู่)</span><span class="sxs-lookup"><span data-stu-id="a7ee6-116">Switch the iPhone or iPad to another connection that doesn't require an explicit HTTP proxy setting (i.e., one configured as HTTP Proxy is Off).</span></span>

## <a name="other-issues"></a><span data-ttu-id="a7ee6-117">ปัญหาอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="a7ee6-117">Other issues?</span></span>
<span data-ttu-id="a7ee6-118">ลองถาม[ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="a7ee6-118">Try asking the [Power BI Community](https://community.powerbi.com/).</span></span>

