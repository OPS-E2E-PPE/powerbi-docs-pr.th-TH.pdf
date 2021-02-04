---
ms.openlocfilehash: e3d62b182f9b142f912a608bee693b7356b1a68d
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2019
ms.locfileid: "61257004"
---
<span data-ttu-id="c571a-101">ในบทเรียนนี้ เราจะเริ่มโดยการสร้าง *กลุ่ม*</span><span class="sxs-lookup"><span data-stu-id="c571a-101">In this lesson, we start by creating a *group*.</span></span> <span data-ttu-id="c571a-102">**กลุ่ม** จะกำหนดเซตของผู้ใช้ที่มีสิทธิ์เข้าถึงแดชบอร์ด รายงาน และข้อมูลที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="c571a-102">A **group** defines a set of users who have access to specific dashboards, reports, and data.</span></span>

<span data-ttu-id="c571a-103">กลุ่มใน Power BI จะขึ้นอยู่กับกลุ่มใน Office 365 ดังนั้นถ้าคุณใช้กลุ่ม Office 365 เพื่อจัดการอีเมล ปฏิทิน และเอกสารของกลุ่มของคุณ คุณจะเห็นว่า Power BI มีฟีเจอร์เหมือนกัน และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="c571a-103">Groups in Power BI are based on groups in Office 365, so if you've been using Office 365 groups to manage your group's email, calendar, and documents, you'll see that Power BI offers the same features, and more.</span></span> <span data-ttu-id="c571a-104">เมื่อคุณสร้างกลุ่มใน Power BI จริงๆ แล้วคุณจะสร้างกลุ่ม Office 365 ขึ้นมา</span><span class="sxs-lookup"><span data-stu-id="c571a-104">When you create a group in Power BI, you're actually creating an Office 365 group.</span></span>

<span data-ttu-id="c571a-105">โมดูลนี้ใช้สถานการณ์สมมติในการจัดตั้งกลุ่มการเงินใหม่</span><span class="sxs-lookup"><span data-stu-id="c571a-105">This module uses the scenario of setting up a new finance group.</span></span> <span data-ttu-id="c571a-106">เราจะแสดงวิธีการตั้งค่ากลุ่ม แชร์แดชบอร์ด รายงาน และชุดข้อมูลลงในกลุ่ม และเพิ่มสมาชิกที่มีสิทธิ์เข้าถึงรายการในกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="c571a-106">We'll show how to set up the group, share dashboards, reports, and datasets into the group, and add members who'll have access to the items in the group.</span></span>

<span data-ttu-id="c571a-107">ฉันเริ่มต้นที่นี่ในพื้นที่ทำงานของฉัน</span><span class="sxs-lookup"><span data-stu-id="c571a-107">I start here in My Workspace.</span></span> <span data-ttu-id="c571a-108">นี่คือแดชบอร์ด รายงาน และชุดข้อมูลที่ฉันสร้าง หรือบุคคลอื่นแชร์กับฉัน</span><span class="sxs-lookup"><span data-stu-id="c571a-108">These are the dashboards, reports, and datasets that I've created or that someone shared with me.</span></span>

![แชร์ และทำงานร่วมกันใน Power BI](./media/6-1-create-groups/pbi_learn06_01myworkspace.png)

<span data-ttu-id="c571a-110">ถ้าฉันจะขยายพื้นที่ทำงานของฉัน ฉันสามารถเลือก **สร้างกลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="c571a-110">If I expand My Workspace, I can select **Create a group**.</span></span>

![แชร์ และทำงานร่วมกันใน Power BI](./media/6-1-create-groups/pbi_learn06_01expandmywkspace.png)

<span data-ttu-id="c571a-112">ในตอนนี้ฉันสามารถตั้งชื่อกลุ่มได้</span><span class="sxs-lookup"><span data-stu-id="c571a-112">Here I can give it a name.</span></span> <span data-ttu-id="c571a-113">เรากำลังใช้สถานการณ์สมมติหรือก็คือกลุ่มการเงิน ดังนั้นฉันจะเรียกว่า การเงิน</span><span class="sxs-lookup"><span data-stu-id="c571a-113">We're using the scenario or a finance group, so I'll call it Finance.</span></span> <span data-ttu-id="c571a-114">Power BI ตรวจสอบให้แน่ใจว่าไม่มีชื่ออยู่บนโดเมนอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="c571a-114">Power BI makes sure the name doesn't exist on the domain.</span></span>

![แชร์ และทำงานร่วมกันใน Power BI](./media/6-1-create-groups/pbi_learn06_01creategroupdialog.png)

<span data-ttu-id="c571a-116">ฉันสามารถตั้งค่าระดับความเป็นส่วนตัวด้วยการกำหนดว่า บุคคลในองค์กรของฉันสามารถดูเนื้อหาของกลุ่มได้หรือไม่ หรือเฉพาะสมาชิกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c571a-116">I can set the privacy level by deciding whether anyone in my organization can see the contents of the group, or only its members.</span></span>

<span data-ttu-id="c571a-117">ฉันพิมพ์ที่อยู่อีเมล กลุ่มความปลอดภัย และรายชื่อการแจกจ่ายที่นี่</span><span class="sxs-lookup"><span data-stu-id="c571a-117">I type email addresses, security groups, and distribution lists here.</span></span> <span data-ttu-id="c571a-118">ฉันเลือก **เพิ่ม** เพื่อทำให้พวกเขาเป็นสมาชิกของกลุ่ม และบันทึกกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="c571a-118">I select **Add** to make them members of the group, and save the group.</span></span>

![แชร์ และทำงานร่วมกันใน Power BI](./media/6-1-create-groups/pbi_learn06_01savegroup.png)

<span data-ttu-id="c571a-120">ไปต่อสู่บทเรียนถัดไป!</span><span class="sxs-lookup"><span data-stu-id="c571a-120">On to the next lesson!</span></span>

