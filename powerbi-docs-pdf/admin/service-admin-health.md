---
title: ติดตามสถานภาพบริการ Power BI ใน Microsoft 365
description: เรียนรู้วิธีการดูสถานภาพบริการปัจจุบันและในอดีตในศูนย์การจัดการ Microsoft 365
author: kfollis
ms.author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: how-to
ms.date: 09/09/2019
LocalizationGroup: Administration
ms.openlocfilehash: 1aa873993cbc3384482f11086e775f41ddbe8917
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96408814"
---
# <a name="track-power-bi-service-health-in-microsoft-365"></a><span data-ttu-id="2afd6-103">ติดตามสถานภาพบริการ Power BI ใน Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2afd6-103">Track Power BI service health in Microsoft 365</span></span>

<span data-ttu-id="2afd6-104">ศูนย์การจัดการ Microsoft 365 มีเครื่องมือที่สำคัญสำหรับผู้ดูแลระบบ Power BI</span><span class="sxs-lookup"><span data-stu-id="2afd6-104">The Microsoft 365 admin center provides important tools for Power BI admins.</span></span> <span data-ttu-id="2afd6-105">เครื่องมือนี้รวมข้อมูลปัจจุบันและอดีตเกี่ยวกับสุขภาพบริการ</span><span class="sxs-lookup"><span data-stu-id="2afd6-105">The tools include current and historical information about service health.</span></span> <span data-ttu-id="2afd6-106">หากต้องการเข้าถึงข้อมูลบริการสุขภาพ คุณต้องได้รับหน้าที่เป็นหนึ่งในตำแหน่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2afd6-106">To access service health info, you must be in one of the following roles:</span></span>

* <span data-ttu-id="2afd6-107">ผู้ดูแลระบบบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="2afd6-107">Power BI Service Administrator</span></span>

* <span data-ttu-id="2afd6-108">ผู้ดูแลระบบส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="2afd6-108">Global Administrator</span></span>

<span data-ttu-id="2afd6-109">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับบทบาท ดู[บทบาทผู้ดูแลระบบที่เกี่ยวข้องกับ Power BI](service-admin-administering-power-bi-in-your-organization.md#administrator-roles-related-to-power-bi)</span><span class="sxs-lookup"><span data-stu-id="2afd6-109">For more info about roles, see [Administrator roles related to Power BI](service-admin-administering-power-bi-in-your-organization.md#administrator-roles-related-to-power-bi).</span></span>

1. <span data-ttu-id="2afd6-110">ลงชื่อเข้าใช้ [ศูนย์การจัดการ Microsoft 365](https://portal.office.com/adminportal)</span><span class="sxs-lookup"><span data-stu-id="2afd6-110">Sign in to the [Microsoft 365 admin center](https://portal.office.com/adminportal).</span></span>

1. <span data-ttu-id="2afd6-111">จากบานหน้าต่างนำทาง ให้เลือก **แสดง** > **บริการสุขภาพ** > **ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="2afd6-111">From the nav pane, select **Show all** > **Health** > **Service health**.</span></span> <span data-ttu-id="2afd6-112">หน้าบริการสุขภาพจะปรากฏ:</span><span class="sxs-lookup"><span data-stu-id="2afd6-112">The Service health page appears:</span></span>

    ![สกรีนช็อตของศูนย์การเรียกตัวจัดการ Microsoft 365 ด้วยตัวเลือกสุขภาพและความสมบูรณ์ของบริการออกมา](media/service-admin-health/service-health-tile.png)

1. <span data-ttu-id="2afd6-114">จากรายการ **บริการทั้งหมด** ให้เลือก **คำแนะนำ** หรือ **เหตุการณ์** และตรวจสอบผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="2afd6-114">From the **All services** list, select **Advisories** or **Incidents** and review the results.</span></span> <span data-ttu-id="2afd6-115">ในสกรีนช็อตด้านล่าง คุณจะเห็นหนึ่งในสามคำแนะนำที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="2afd6-115">In the screenshot below, you see one of three active advisories.</span></span>

    ![สกรีนช็อตของการเรียกหน้าบริการสุขภาพที่มีสามคำแนะนำสำหรับ Power BI และแสดงรายละเอียดตัวเลือกออกมา](media/service-admin-health/active-advisories.png)

1. <span data-ttu-id="2afd6-117">เมื่อต้องการดูข้อมูลเพิ่มเติม เลือก **แสดงรายละเอียด** สำหรับรายการ</span><span class="sxs-lookup"><span data-stu-id="2afd6-117">To see more information, select **Show details** for an item.</span></span> <span data-ttu-id="2afd6-118">ในสกรีนช็อตด้านล่าง คุณจะเห็นรายละเอียดเพิ่มเติม รวมถึงการปรับปรุงสถานะล่าสุดด้วย</span><span class="sxs-lookup"><span data-stu-id="2afd6-118">In the screenshot below, you see additional details, including recent status updates.</span></span>

    ![ภาพหน้าจอของรายละเอียดคำแนะนำ ที่แสดงข้อมูลเพิ่มเติม](media/service-admin-health/advisory-details.png)

    <span data-ttu-id="2afd6-120">เลื่อนลงเพื่อดูข้อมูลเพิ่มเติม จากนั้นปิดบานหน้าต่างเมื่อคุณทำเสร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="2afd6-120">Scroll down to see more info, then close the pane when you're finished.</span></span>

1. <span data-ttu-id="2afd6-121">ในการดูข้อมูลในอดีตทั่วทั้งบริการ ที่มุมบนขวาของ **หน้าบริการสุขภาพ** เลือก **ดูประวัติ**</span><span class="sxs-lookup"><span data-stu-id="2afd6-121">To see historical information across all services, in the upper-right corner of the **Service health** page, select **View history**.</span></span> <span data-ttu-id="2afd6-122">จากนั้นเลือก **7 วันที่ผ่าน** หรือ **30 วันที่ผ่าน**</span><span class="sxs-lookup"><span data-stu-id="2afd6-122">Then select **Last 7 days** or **Last 30 days**.</span></span> 

1. <span data-ttu-id="2afd6-123">เมื่อต้องการกลับไปยังสถานภาพบริการปัจจุบัน เลือก **ดูสถานะปัจจุบัน**</span><span class="sxs-lookup"><span data-stu-id="2afd6-123">To return to current service health, select **View current status**.</span></span>