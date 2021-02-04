---
ms.openlocfilehash: 8dc488a47ac2b5b4e7980b7404b2722b1120b6ab
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/05/2020
ms.locfileid: "77464417"
---
## <a name="validate-the-roles-within-power-bi-desktop"></a><span data-ttu-id="b88a5-101">ตรวจสอบบทบาทภายใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="b88a5-101">Validate the roles within Power BI Desktop</span></span>
<span data-ttu-id="b88a5-102">คุณสามารถทดสอบผลลัพธ์ของบทบาทภายใน Power BI Desktop ได้หลังจากที่คุณสร้างบทบาทของตัวเองแล้ว</span><span class="sxs-lookup"><span data-stu-id="b88a5-102">After you've created your roles, test the results of the roles within Power BI Desktop.</span></span>

1. <span data-ttu-id="b88a5-103">จากแท็บ **การวางรูปแบบ** เลือก **ดูในฐานะบทบาท**</span><span class="sxs-lookup"><span data-stu-id="b88a5-103">From the **Modeling** tab, select **View as Roles**.</span></span> 

    ![เลือกดูในฐานะบทบาท](./media/rls-desktop-view-as-roles/powerbi-desktop-rls-view-as-roles.png)

    <span data-ttu-id="b88a5-105">หน้าต่าง **ดูในฐานะบทบาท** จะปรากฏขึ้นเมื่อคุณมองเห็นบทบาทที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="b88a5-105">The **View as roles** window appears, where you see the roles you've created.</span></span>

    ![หน้าต่างดูในฐานะบทบาท](./media/rls-desktop-view-as-roles/powerbi-desktop-rls-view-as-roles-dialog.png)

3. <span data-ttu-id="b88a5-107">เลือกบทบาทที่คุณสร้าง จากนั้นเลือก **ตกลง** เพื่อนำไปใช้กับบทบาทดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="b88a5-107">Select a role you created, and then select **OK** to apply that role.</span></span> 

   <span data-ttu-id="b88a5-108">รายงานจะแสดงข้อมูลที่เกี่ยวข้องกับบทบาทนั้น</span><span class="sxs-lookup"><span data-stu-id="b88a5-108">The report renders the data relevant for that role.</span></span>

4. <span data-ttu-id="b88a5-109">นอกจากนี้คุณยังสามารถเลือก **ผู้ใช้อื่น** และใส่ผู้ใช้ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="b88a5-109">You can also select **Other user** and supply a given user.</span></span> 

    ![เลือกผู้ใช้อื่น](./media/rls-desktop-view-as-roles/powerbi-desktop-rls-other-user.png)

   <span data-ttu-id="b88a5-111">การใส่ชื่อผู้ใช้หลัก (UPN) เป็นสิ่งบริการ Power BI และเซิร์ฟเวอร์รายงาน Power BI จะใช้เป็นสิ่งที่ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="b88a5-111">It's best to supply the User Principal Name (UPN) as that's what the Power BI service and Power BI Report Server use.</span></span>

   <span data-ttu-id="b88a5-112">ภายใน Power BI Desktop **ผู้ใช้อื่น** จะแสดงผลลัพธ์ที่แตกต่างกันในกรณีที่คุณใช้การรักษาความปลอดภัยแบบไดนามิก โดยยึดตามนิพจน์ DAX ของคุณ</span><span class="sxs-lookup"><span data-stu-id="b88a5-112">Within Power BI Desktop, **Other user** displays different results only if you're using dynamic security based on your DAX expressions.</span></span> 

5. <span data-ttu-id="b88a5-113">เลือก**ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b88a5-113">Select **OK**.</span></span> 

   <span data-ttu-id="b88a5-114">รายงานจะแสดงผลตามสิ่งที่ผู้ใช้นั้นสามารถมองเห็นได้</span><span class="sxs-lookup"><span data-stu-id="b88a5-114">The report renders based on what that user can see.</span></span>



