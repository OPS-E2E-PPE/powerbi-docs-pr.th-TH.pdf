---
title: ควบคุมการใช้งานชุดข้อมูลทั่วทั้งพื้นที่ทำงาน - Power BI
description: เรียนรู้วิธีการจำกัดการไหลของข้อมูลในผู้เช่า Power BI
author: paulinbar
ms.author: painbar
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: how-to
ms.date: 04/30/2020
LocalizationGroup: Share your work
ms.openlocfilehash: d94be70bd61988f009900432e3bc77756a3821df
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96392576"
---
# <a name="control-the-use-of-datasets-across-workspaces"></a><span data-ttu-id="59b00-103">ควบคุมการใช้งานชุดข้อมูลทั่วทั้งพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="59b00-103">Control the use of datasets across workspaces</span></span>

<span data-ttu-id="59b00-104">การใช้ชุดข้อมูลทั้งพื้นที่ทำงานเป็นวิธีมีประสิทธิภาพเพื่อส่งเสริมวัฒนธรรมการเก็บข้อมูลและการพัฒนาข้อมูลให้เป็นระบบภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="59b00-104">Using datasets across workspaces is a powerful way to drive data culture and data democratization within an organization.</span></span> <span data-ttu-id="59b00-105">ถ้าคุณเป็นผู้ดูแลระบบ Power BI ในบางครั้งคุณต้องการจำกัดการไหลของข้อมูลภายในผู้เช่า Power BI</span><span class="sxs-lookup"><span data-stu-id="59b00-105">Still, if you're a Power BI admin, sometimes you want to restrict the flow of information within your Power BI tenant.</span></span> <span data-ttu-id="59b00-106">ด้วยการตั้งค่าผู้เช่า **ใช้ชุดข้อมูลทั้งพื้นที่ทำงาน** คุณสามารถจำกัดการใช้ชุดข้อมูลซ้ำ ไม่ว่าจะทั้งหมดหรือบางส่วนต่อกลุ่มความปลอดภัยได้</span><span class="sxs-lookup"><span data-stu-id="59b00-106">With the tenant setting **Use datasets across workspaces**, you can restrict dataset reuse either completely or partially per security groups.</span></span>

![การตั้งค่าพื้นที่ทำงานของผู้ดูแลระบบ Power BI](media/service-datasets-admin-across-workspaces/power-bi-admin-workspace-settings.png)

<span data-ttu-id="59b00-108">หากคุณปิดการตั้งค่านี้ จะมีผลกระทบต่อผู้สร้างรายงาน:</span><span class="sxs-lookup"><span data-stu-id="59b00-108">If you turn off this setting, here are the effects on report creators:</span></span>

- <span data-ttu-id="59b00-109">ปุ่มคัดลอกรายงานทั้งพื้นที่ทำงานไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="59b00-109">The button to copy reports across workspaces isn't available.</span></span> 
- <span data-ttu-id="59b00-110">ในรายงานที่ยึดตามชุดข้อมูลที่ใช้ร่วมกัน ปุ่ม **แก้ไขรายงาน** ไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="59b00-110">In a report based on a shared dataset, the **Edit report** button isn't available.</span></span>
- <span data-ttu-id="59b00-111">ในบริการของ Power BI ประสบการณ์การค้นหาจะแสดงเฉพาะชุดข้อมูลในพื้นที่ทำงานปัจจุบันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="59b00-111">In the Power BI service, the discovery experience only shows datasets in the current workspace.</span></span>
- <span data-ttu-id="59b00-112">ใน Power BI Desktop ประสบการณ์การค้นหาจะแสดงเฉพาะชุดข้อมูลจากพื้นที่ทำงานที่คุณเป็นสมาชิกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="59b00-112">In Power BI Desktop, the discovery experience only shows datasets from workspaces where you're a member.</span></span>
- <span data-ttu-id="59b00-113">ใน Power BI Desktop ถ้าผู้ใช้เปิดไฟล์.pbix ด้วยการเชื่อมต่อสดไปยังชุดข้อมูลที่อยู่นอกพื้นที่ทำงานใด ๆ ที่ผู้ใช้เป็นสมาชิกของ พวกเขาจะเห็นข้อความแสดงข้อผิดพลาด ซึ่งขอให้พวกเขาเชื่อมต่อกับชุดข้อมูลอื่น</span><span class="sxs-lookup"><span data-stu-id="59b00-113">In Power BI Desktop, if users open a .pbix file with a live connection to a dataset outside any workspaces they are a member of, they see an error message asking them to connect to a different dataset.</span></span>

## <a name="provide-a-link-for-the-certification-process"></a><span data-ttu-id="59b00-114">มีลิงก์สำหรับกระบวนการออกใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="59b00-114">Provide a link for the certification process</span></span>

<span data-ttu-id="59b00-115">ในฐานะผู้ดูแลระบบ Power BI คุณสามารถใส่ URL สำหรับลิงก์ **เรียนรู้เพิ่มเติม** บนหน้าการตั้งค่า **การรับรอง** ได้</span><span class="sxs-lookup"><span data-stu-id="59b00-115">As a Power BI admin, you can provide a URL for the **Learn more** link on the **Endorsement** setting page.</span></span>  <span data-ttu-id="59b00-116">ดู [เปิดการใช้งานใบรับรองเนื้อหา](../admin/service-admin-setup-certification.md) สำหรับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="59b00-116">See [Enable content certification](../admin/service-admin-setup-certification.md) for detail.</span></span> <span data-ttu-id="59b00-117">ลิงก์นี้สามารถไปที่เอกสารประกอบเกี่ยวกับกระบวนการออกใบรับรองของคุณ</span><span class="sxs-lookup"><span data-stu-id="59b00-117">This link can go to documentation about your certification process.</span></span> <span data-ttu-id="59b00-118">ถ้าคุณไม่กำหนดปลายทางสำหรับลิงก์ **เรียนรู้เพิ่มเติม** ตามค่าเริ่มต้นจะลิงก์ไปยังบทความ [รับรองเนื้อหาของคุณ](../collaborate-share/service-endorse-content.md)</span><span class="sxs-lookup"><span data-stu-id="59b00-118">If you don't provide a destination for the **Learn more** link, by default it points to the [Endorse your content](../collaborate-share/service-endorse-content.md) article.</span></span>

![เรียนรู้เพิ่มเติมเกี่ยวกับใบรับรองชุดข้อมูล](media/service-datasets-admin-across-workspaces/service-admin-certification-setup-dialog.png)

## <a name="next-steps"></a><span data-ttu-id="59b00-120">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="59b00-120">Next steps</span></span>

- [<span data-ttu-id="59b00-121">ใช้ชุดข้อมูลทั่วทั้งพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="59b00-121">Use datasets across workspaces</span></span>](service-datasets-across-workspaces.md)
- <span data-ttu-id="59b00-122">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="59b00-122">Questions?</span></span> [<span data-ttu-id="59b00-123">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="59b00-123">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
