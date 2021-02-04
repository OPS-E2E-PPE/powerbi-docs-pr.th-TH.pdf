---
title: แก้ไขปัญหารีเฟรชตามกำหนดการสำหรับ Azure SQL Database
description: แก้ไขปัญหาการรีเฟรชตามกำหนดการสำหรับ Azure SQL Database ใน Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: troubleshooting
ms.date: 09/04/2019
ms.custom: seodec18
LocalizationGroup: Troubleshooting
ms.openlocfilehash: a9f69c8177766352d768d86903f15977ae0d8d1c
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410746"
---
# <a name="troubleshooting-scheduled-refresh-for-azure-sql-databases-in-power-bi"></a><span data-ttu-id="fcdbd-103">แก้ไขปัญหาการรีเฟรชตามกำหนดการสำหรับ Azure SQL Database ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="fcdbd-103">Troubleshooting scheduled refresh for Azure SQL Databases in Power BI</span></span>

<span data-ttu-id="fcdbd-104">สำหรับข้อมูลโดยละเอียดเกี่ยวกับการรีเฟรช โปรดดูหัวข้อ [รีเฟรชข้อมูลใน Power BI](refresh-data.md) และ [กำหนดค่าการรีเฟรชตามกำหนดเวลา](refresh-scheduled-refresh.md)</span><span class="sxs-lookup"><span data-stu-id="fcdbd-104">For detailed information about refresh, see [Refresh data in Power BI](refresh-data.md) and [Configure scheduled refresh](refresh-scheduled-refresh.md).</span></span>

<span data-ttu-id="fcdbd-105">ขณะที่กำลังตั้งค่าการรีเฟรชตามกำหนดเวลสสำหรับฐานข้อมูล Azure SQL หากคุณได้รับข้อผิดพลาดที่มีรหัสข้อผิดพลาด 400 เมื่อแก้ไขข้อมูลประจำตัว กรุณาลองทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่ากฎไฟร์วอลล์ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="fcdbd-105">While setting up scheduled refresh for Azure SQL database, if you get an error with error code 400 when editing the credentials, try the following to set up the appropriate firewall rule:</span></span>

1. <span data-ttu-id="fcdbd-106">ลงชื่อเข้าใช้ไปยัง [พอร์ทัล Azure](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="fcdbd-106">Sign in to the [Azure portal](https://portal.azure.com).</span></span>

1. <span data-ttu-id="fcdbd-107">ไปยังฐานข้อมูล Azure SQL ที่คุณกำลังกำหนดค่าการรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="fcdbd-107">Go to the Azure SQL database for which you're configuring refresh.</span></span>

1. <span data-ttu-id="fcdbd-108">ที่ด้านบนของแผ่น **ภาพรวม** ให้เลือก **ตั้งค่าไฟร์วอลล์ของเซิร์ฟเวอร์**</span><span class="sxs-lookup"><span data-stu-id="fcdbd-108">At the top of the **Overview** blade, select **Set server firewall**.</span></span>

1. <span data-ttu-id="fcdbd-109">บนแผ่น **การตั้งค่าไฟร์วอลล์** คุณควรตรวจสอบให้แน่ใจว่ามีการตั้งค่า **อนุญาตการเข้าถึงบริการ Azure** เป็น **ON**</span><span class="sxs-lookup"><span data-stu-id="fcdbd-109">On the **Firewall settings** blade, make sure that **Allow access to Azure services** is set to **ON**.</span></span>

    ![บริการ Azure ที่ได้รับอนุญาต](media/service-admin-troubleshooting-scheduled-refresh-azure-sql-databases/azurerefresh.png)  

<span data-ttu-id="fcdbd-111">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="fcdbd-111">More questions?</span></span> [<span data-ttu-id="fcdbd-112">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="fcdbd-112">Try the Power BI Community</span></span>](https://community.powerbi.com/)
