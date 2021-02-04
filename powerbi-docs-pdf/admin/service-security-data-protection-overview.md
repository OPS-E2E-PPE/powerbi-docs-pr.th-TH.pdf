---
title: การป้องกันข้อมูลใน Power BI
description: เรียนรู้เกี่ยวกับการป้องกันข้อมูลใน Power BI
author: paulinbar
ms.author: painbar
manager: rkarlin
ms.service: powerbi
ms.subservice: powerbi-eim
ms.topic: conceptual
ms.date: 09/17/2020
LocalizationGroup: Data from files
ms.openlocfilehash: 4405b83dae3d517b16099725ab10990cc8e503f4
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413368"
---
# <a name="data-protection-in-power-bi"></a><span data-ttu-id="d60c4-103">การป้องกันข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="d60c4-103">Data protection in Power BI</span></span>

## <a name="overview"></a><span data-ttu-id="d60c4-104">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="d60c4-104">Overview</span></span>

<span data-ttu-id="d60c4-105">Power BI มีบทบาทสำคัญในการนำข้อมูลเชิงลึกไปเผยแพร่ให้กับทุกคนในองค์กร</span><span class="sxs-lookup"><span data-stu-id="d60c4-105">Power BI plays a key role in bringing data insights to everyone in an organization.</span></span> <span data-ttu-id="d60c4-106">อย่างไรก็ตาม เนื่องจากข้อมูลเป็นสิ่งที่สามารถเข้าถึงได้มากขึ้นเพื่อช่วยในการตัดสินใจ ความเสี่ยงของการแชร์พร่ำเพรื่อโดยไม่ได้ตั้งใจหรือการใช้ข้อมูลที่สำคัญทางธุรกิจในทางที่ผิดจะเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="d60c4-106">However, as data becomes more accessible to inform decisions, risk of accidental oversharing or misuse of business-critical information increases.</span></span>

<span data-ttu-id="d60c4-107">Microsoft มีระบบการรักษาความปลอดภัยระดับโลกเพื่อช่วยคุ้มครองลูกค้าจากภัยคุกคามต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="d60c4-107">Microsoft has world-class security capabilities to help protect customers from threats.</span></span> <span data-ttu-id="d60c4-108">นักวิจัยด้านการรักษาความปลอดภัยมากกว่า 3,500 รายและระบบปัญญาประดิษฐ์ที่มีความซับซ้อนต่างวิเคราะห์สัญญาณมากกว่า 6.5 ล้านล้านรูปแบบเพื่อปกป้องลูกค้าจากภัยคุกคามต่าง ๆ ที่ Microsoft</span><span class="sxs-lookup"><span data-stu-id="d60c4-108">Over 3,500 security researchers along with sophisticated AI models reason every day over 6.5+ trillion signals globally to help protect customers against threats at Microsoft.</span></span>

<span data-ttu-id="d60c4-109">ความสามารถในการปกป้องข้อมูลใน Power BI สร้างขึ้นโดยใช้จุดแข็งของ Microsoft ในเรื่องการรักษาความปลอดภัย และเปิดโอกาสให้ลูกค้าสามารถเพิ่มประสิทธิภาพให้กับผู้ใช้ Power BI ทุกคน และเพิ่มการป้องกันให้กับข้อมูลไม่ว่าจะมีการเข้าถึงถึงด้วยวิธีการใดและเข้าถึงที่ใด</span><span class="sxs-lookup"><span data-stu-id="d60c4-109">Data protection capabilities in Power BI build on Microsoft’s strengths in security and enable customers to empower every user with Power BI and better protect their data no matter how or where it is accessed.</span></span>


>[!VIDEO https://www.youtube.com/embed/zEx0449K7F8]

<span data-ttu-id="d60c4-110">ด้วยความสามารถในการปกป้องข้อมูลของ Power BI คุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="d60c4-110">With Power BI's data protection capabilities you can:</span></span>

* <span data-ttu-id="d60c4-111">**จัดประเภทและป้ายชื่อข้อมูล Power BI ที่เป็นความลับ** โดยใช้ป้ายบอกระดับความลับของ Microsoft Information Protection ที่ใช้ใน Office และผลิตภัณฑ์อื่น ๆ ของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="d60c4-111">**Classify and label sensitive Power BI data** using Microsoft Information Protection sensitivity labels used in Office and other Microsoft products.</span></span>  
* <span data-ttu-id="d60c4-112">**บังคับใช้นโยบายการกำกับดูแลแม้ว่าเนื้อหา Power BI จะถูกส่งออก** ไปยัง Excel, PowerPoint, PDF และรูปแบบการส่งออกที่ได้รับการสนับสนุนอื่น ๆ เพื่อช่วยให้แน่ใจว่าข้อมูลจะได้รับการป้องกันแม้ว่าข้อมูลเหล่านั้นจะออกจาก Power BI ไปแล้ว</span><span class="sxs-lookup"><span data-stu-id="d60c4-112">**Enforce governance policies even when Power BI content is exported** to Excel, PowerPoint, PDF, and other supported export formats to help ensure data is protected even when it leaves Power BI.</span></span>
* <span data-ttu-id="d60c4-113">**ตรวจสอบและปกป้องกิจกรรมของผู้ใช้ในข้อมูลสำคัญในแบบเรียลไทม์** ด้วยการแจ้งเตือน การตรวจสอบเซสชั่น และการบรรเทาความเสี่ยงด้วยระบบ Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="d60c4-113">**Monitor and protect user activity on sensitive data in real time** with alerts, session monitoring, and risk remediation using Cloud App Security.</span></span>
* <span data-ttu-id="d60c4-114">**เพิ่มประสิทธิภาพให้กับผู้ดูแลระบบความปลอดภัย** ที่ใช้รายงานการป้องกันข้อมูลและระบบการตรวจสอบความปลอดภัยด้ว Microsoft Cloud App Security เพื่อยกระดับการกำกับดูแลขององค์กร</span><span class="sxs-lookup"><span data-stu-id="d60c4-114">**Empower security administrators** who use data protection reports and security investigation capabilities with Microsoft Cloud App Security to enhance organizational oversight.</span></span>

<span data-ttu-id="d60c4-115">อ่านเพิ่มเติมเกี่ยวกับ [ป้ายบอกระดับความลับ](/microsoft-365/compliance/sensitivity-labels?view=o365-worldwide) และ [Cloud App Security](/cloud-app-security/what-is-cloud-app-security)</span><span class="sxs-lookup"><span data-stu-id="d60c4-115">Read more about [Microsoft Information Protection sensitivity labels](/microsoft-365/compliance/sensitivity-labels?view=o365-worldwide) and [Cloud App Security](/cloud-app-security/what-is-cloud-app-security).</span></span>


## <a name="next-steps"></a><span data-ttu-id="d60c4-116">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d60c4-116">Next steps</span></span>

* [<span data-ttu-id="d60c4-117">เรียนรู้เกี่ยวกับป้ายบอกระดับความลับใน Power BI และวิธีการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d60c4-117">Learn about sensitivity labels in Power BI and how to use them</span></span>](service-security-sensitivity-label-overview.md)
* [<span data-ttu-id="d60c4-118">ติดตั้งและใช้ระบบควบคุม Cloud App Security ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="d60c4-118">Set up and use Cloud App Security controls in Power BI</span></span>](service-security-using-microsoft-cloud-app-security-controls.md)
* [<span data-ttu-id="d60c4-119">หลักสูตรวิดีโอ Microsoft Business Applications Summit - การปกป้องข้อมูลของ Power BI และ Microsoft - ตัวพลิกเกมสำหรับ secure BI</span><span class="sxs-lookup"><span data-stu-id="d60c4-119">Microsoft Business Applications Summit video session - Power BI and Microsoft Information Protection - The game changer for secure BI</span></span>](https://mymbas.microsoft.com/sessions/f30c8368-6590-4be3-80d4-2bc677f596a4?source=sessions)