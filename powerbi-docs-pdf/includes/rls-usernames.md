---
ms.openlocfilehash: 3e89344ef1298864b485f465b28c56397a7e1511
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/05/2020
ms.locfileid: "61194084"
---
## <a name="using-the-username-or-userprincipalname-dax-function"></a><span data-ttu-id="b0058-101">การใช้ฟังก์ชัน DAX the username() หรือ userprincipalname()</span><span class="sxs-lookup"><span data-stu-id="b0058-101">Using the username() or userprincipalname() DAX function</span></span>
<span data-ttu-id="b0058-102">คุณสามารถใช้ประโยชน์จากฟังก์ชัน DAX *username()* หรือ*userprincipalname()* ภายในชุดข้อมูลของคุณได้</span><span class="sxs-lookup"><span data-stu-id="b0058-102">You can take advantage of the DAX functions *username()* or *userprincipalname()* within your dataset.</span></span> <span data-ttu-id="b0058-103">คุณสามารถใช้กับนิพจน์ใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="b0058-103">You can use them within expressions in Power BI Desktop.</span></span> <span data-ttu-id="b0058-104">เมื่อคุณเผยแพร่แบบจำลองของคุณ จะมีการใช้แบบจำลองภายในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="b0058-104">When you publish your model, it will be used within the Power BI service.</span></span>

<span data-ttu-id="b0058-105">ภายใน Power BI Desktop *username()* จะส่งผู้ใช้กลับในรูปแบบของ*DOMAIN\User*และ*userprincipalname()* จะส่งผู้ใช้กลับในรูปแบบของ<em>user@contoso.com</em></span><span class="sxs-lookup"><span data-stu-id="b0058-105">Within Power BI Desktop, *username()* will return a user in the format of *DOMAIN\User* and *userprincipalname()* will return a user in the format of <em>user@contoso.com</em>.</span></span>

<span data-ttu-id="b0058-106">ภายในบริการ Power BI *username()* และ*userprincipalname()* จะส่งกลับชื่อผู้ใช้หลัก (UPN)</span><span class="sxs-lookup"><span data-stu-id="b0058-106">Within the Power BI service, *username()* and *userprincipalname()* will both return the user's User Principal Name (UPN).</span></span> <span data-ttu-id="b0058-107">ซึ่งมีลักษณะคล้ายกับที่อยู่อีเมล์</span><span class="sxs-lookup"><span data-stu-id="b0058-107">This looks similar to an email address.</span></span>

