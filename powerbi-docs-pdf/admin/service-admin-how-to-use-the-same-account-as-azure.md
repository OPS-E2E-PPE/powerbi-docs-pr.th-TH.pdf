---
title: การใช้บัญชีเดียวกันสำหรับ Power BI และ Azure
description: วิธีใช้บัญชีเดียวกันสำหรับเข้าสู่ระบบ Power BI และ Azure
author: kfollis
ms.author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 09/09/2019
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 2706fd8eb4cb2fddda99710e7c1dc32c2300aa26
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413621"
---
# <a name="using-the-same-account-for-power-bi-and-azure"></a><span data-ttu-id="a0e8f-103">การใช้บัญชีเดียวกันสำหรับ Power BI และ Azure</span><span class="sxs-lookup"><span data-stu-id="a0e8f-103">Using the same account for Power BI and Azure</span></span>

<span data-ttu-id="a0e8f-104">ถ้าคุณเป็นทั้งผู้ใช้ Power BI และ Azure คุณอาจต้องการใช้บัญชีเดียวกันสำหรับเข้าสู่ระบบทั้งสอง เพื่อคุณจะได้ไม่เป็นต้องพิมพ์รหัสผ่านของคุณซ้ำสองครั้ง</span><span class="sxs-lookup"><span data-stu-id="a0e8f-104">If you are a user of both Power BI and Azure, you might want to use the same login for both services so that you don't need to type in your password twice.</span></span>

<span data-ttu-id="a0e8f-105">Power BI ลงชื่อคุณเข้าใช้ ด้วยบัญชีองค์กรของคุณ ซึ่งเชื่อมโยงกับที่อยู่อีเมลงานหรือโรงเรียนของคุณ</span><span class="sxs-lookup"><span data-stu-id="a0e8f-105">Power BI signs you in with your organizational account, associated with your work or school email address.</span></span>  <span data-ttu-id="a0e8f-106">Azure ลงชื่อคุณเข้าใช้ ด้วยบัญชี Microsoft หรือบัญชีองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="a0e8f-106">Azure signs you in with either a Microsoft Account or your organizational account.</span></span>

<span data-ttu-id="a0e8f-107">ถ้าคุณต้องการใช้บัญชีเดียวกันสำหรับทั้ง Azure และ Power BI ให้แน่ใจว่าได้ลงชื่อเข้าใช้ Azure ด้วยบัญชีองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="a0e8f-107">If you want to use the same login for both Azure and Power BI, be sure to sign in to Azure with your organizational account.</span></span>

<span data-ttu-id="a0e8f-108">**เกิดอะไรขึ้นถ้าฉันลงชื่อเข้าใช้ Azure ด้วยบัญชี Microsoft ของฉันไปแล้ว?**</span><span class="sxs-lookup"><span data-stu-id="a0e8f-108">**What if I already sign in to Azure with my Microsoft Account?**</span></span>

<span data-ttu-id="a0e8f-109">คุณสามารถเพิ่มบัญชีผู้ใช้องค์กรของคุณเป็นผู้ดูแลร่วมใน Azure โดยทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="a0e8f-109">You can add your organizational account as a co-administrator in Azure by following these steps:</span></span>

1. <span data-ttu-id="a0e8f-110">ลงชื่อเข้าใช้ไปยัง [พอร์ทัล Azure](https://portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="a0e8f-110">Sign in to the [Azure portal](https://portal.azure.com/).</span></span> <span data-ttu-id="a0e8f-111">ถ้าคุณเป็นผู้ใช้ในหลายไดเรกทอรีใน Azure เลือก **การสมัครใช้งาน** และกรองเพื่อดูเฉพาะไดเรกทอรีและการสมัครใช้งานที่คุณต้องการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="a0e8f-111">If you are a user in multiple Azure directories, select **Subscriptions** and then filter to view only the directory and subscriptions you want to edit.</span></span>

1. <span data-ttu-id="a0e8f-112">ในบานหน้าต่างการนำทาง ให้เลือก **ตัวควบคุมการเข้าถึง (IAM)** จากนั้นจึงเลือก **เพิ่ม** \> **เพิ่มผู้ดูแลระบบร่วม**</span><span class="sxs-lookup"><span data-stu-id="a0e8f-112">In the nav pane, select **Access control (IAM)**, then select **Add** \> **Add co-administrator**.</span></span>

    ![ภาพหน้าจอของการควบคุมการเข้าถึงที่มีการเพิ่มผู้ดูแลระบบร่วมที่เรียกให้มาช่วย](media/service-admin-how-to-use-the-same-account-as-azure/add-co-administrator.png)

1. <span data-ttu-id="a0e8f-114">ใส่ที่อยู่อีเมลที่เชื่อมโยงกับบัญชีองค์กรของคุณ และเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="a0e8f-114">Enter the email address associated with your organizational account, and select **Add**.</span></span>

1. <span data-ttu-id="a0e8f-115">ครั้งถัดไปที่คุณลงชื่อเข้าใช้ใน ฃพอร์ทัล Azure ให้ใช้ที่อยู่อีเมลองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="a0e8f-115">Next time you sign in to the Azure portal, use your organizational email address.</span></span>

<span data-ttu-id="a0e8f-116">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a0e8f-116">More questions?</span></span> [<span data-ttu-id="a0e8f-117">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="a0e8f-117">Try the Power BI Community</span></span>](https://community.powerbi.com/)
