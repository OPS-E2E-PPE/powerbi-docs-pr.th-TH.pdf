---
title: แนวทางการกำกับดูแล และการปรับใช้งาน
description: เอกสารทางเทคนิค สำหรับเรียนรู้ แนวคิด ตัวเลือก และคำแนะนำสำหรับการกำกับดูแลภายในระบบนิเวศของ Power BI
author: kfollis
ms.author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 09/13/2019
LocalizationGroup: Administration
ms.openlocfilehash: 537fb25d1b8514efdcaf17fe9f922eb11de46c3f
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413667"
---
# <a name="governance-and-deployment-approaches"></a><span data-ttu-id="47874-103">แนวทางการกำกับดูแล และการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="47874-103">Governance and deployment approaches</span></span>

<span data-ttu-id="47874-104">ในหลายทศวรรษที่ผ่านมา บริษัทจำนวนมากได้รับรู้ถึงความจำเป็นที่มากขึ้นของการนำสินทรัพย์จากข้อมูลมาใช้ประโยชน์และสร้างกำไรจากโอกาสในตลาด</span><span class="sxs-lookup"><span data-stu-id="47874-104">Over the last few decades, companies have become increasingly aware of the need to leverage data assets to profit from market opportunities.</span></span> <span data-ttu-id="47874-105">โดยการวิเคราะห์การแข่งขัน หรือ โดยการทำความเข้าใจรูปแบบการดำเนินงาน ตอนนี้องค์กรจำนวนมากเข้าใจแล้วว่า พวกเขาอยู่เหนือคู่แข่งได้ด้วยการใช้ประโยชน์จากการมีกลยุทธ์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="47874-105">Either by performing competitive analysis or by understanding operational patterns, many organizations now understand they can benefit from having a data strategy as a way to stay ahead of their competition.</span></span>  

<span data-ttu-id="47874-106">เอกสารทางเทคนิค[วางแผนการปรับใช้ Power BI Enterprise](https://go.microsoft.com/fwlink/?linkid=2057861)ให้เฟรมเวิร์กสำหรับเพิ่มผลจากการลงทุนที่เกี่ยวข้องกับ Power BI เมื่อบริษัทต่างๆ ก็พยายามที่จะเป็นผู้ที่เข้าใจข้อมูลมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="47874-106">The [Planning a Power BI Enterprise Deployment](https://go.microsoft.com/fwlink/?linkid=2057861) whitepaper provides a framework for increasing the return on investment related to Power BI as companies increasingly seek to become more data-savvy.</span></span>

<span data-ttu-id="47874-107">ผู้ที่ศึกษาด้านข่าวกรองธุรกิจ มักนิยามบริษัทที่มีความเชี่ยวชาญข้อมูล ว่าเป็นบริษัทที่ได้ประโยชน์จากการใช้ข้อมูลจริงมาสนับสนุนการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="47874-107">Business Intelligence practitioners typically define data-savvy companies as those that benefit from the use of factual information to support decision making.</span></span>  <span data-ttu-id="47874-108">แม้กระทั่งกล่าวถึงบางองค์กรว่ามี *วัฒนธรรมเชิงข้อมูล*</span><span class="sxs-lookup"><span data-stu-id="47874-108">We even describe certain organizations as having a *data culture*.</span></span> <span data-ttu-id="47874-109">ไม่ว่าจะอยู่ในระดับองค์กร หรือ ระดับแผนก วัฒนธรรมข้อมูลสามารถส่งผลบวกต่อความสามารถของบริษัทที่จะปรับตัวและเติบโต</span><span class="sxs-lookup"><span data-stu-id="47874-109">Whether at the organizational level, or at a departmental level, a data culture can positively alter a company’s ability to adapt and thrive.</span></span>  <span data-ttu-id="47874-110">ข้อมูลเชิงลึกไม่จำเป็นต้องอยู่ในระดับองค์กรถึงจะส่งผลได้กว้างไกลเสมอไป กล่าวคือ ข้อมูลเชิงลึกด้านการดำเนินงานเล็ก ๆ ที่เปลี่ยนการดำเนินงานรายวันก็สามารถสร้างความเปลี่ยนแปลงได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="47874-110">Data insights don't always have to be at enterprise scope to be far-reaching: small operational insights that alter day-to-day operations can be transformational as well.</span></span>

<span data-ttu-id="47874-111">สำหรับบริษัทเหล่านี้ ความเข้าใจว่า ข้อเท็จจริง – และการวิเคราะห์ข้อเท็จจริง – ต้องขับเคลื่อนคำนิยามของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="47874-111">For these companies, there is an understanding that facts – and fact analysis – must drive how business processes are defined.</span></span> <span data-ttu-id="47874-112">สมาชิกในทีมต่างพยายามค้นหาข้อมูล มองหารูปแบบ และแชร์สิ่งที่พบกับผู้อื่น</span><span class="sxs-lookup"><span data-stu-id="47874-112">Team members attempt to seek data, identify patterns, and share findings with others.</span></span> <span data-ttu-id="47874-113">วิธีการนี้มีประโยชน์ ไม่ว่าจะใช้การวิเคราะห์นี้กับปัจจัยภายใน หรือปัจจัยภายนอกธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="47874-113">This approach can be useful regardless of if the analysis is done over external or internal business factors.</span></span> <span data-ttu-id="47874-114">มันเป็นมุมมอง ไม่ใช่กระบวนการ</span><span class="sxs-lookup"><span data-stu-id="47874-114">It is first and foremost a perspective, not a process.</span></span> <span data-ttu-id="47874-115">อ่านเอกสารทางเทคนิคเพื่อเรียนรู้เกี่ยวกับ แนวคิด, ตัวเลือก และคำแนะนำสำหรับการกำกับดูแลภายในระบบนิเวศของ Power BI</span><span class="sxs-lookup"><span data-stu-id="47874-115">Read the whitepaper to learn about concepts, options and suggestions for governance within the Power BI ecosystem.</span></span>