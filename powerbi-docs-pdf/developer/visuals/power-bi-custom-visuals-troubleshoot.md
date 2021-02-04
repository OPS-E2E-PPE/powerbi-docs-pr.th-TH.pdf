---
title: การแก้ไขปัญหาวิธีการพัฒนาวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายถึงปัญหาทั่วไปที่คุณอาจพบเมื่อพัฒนาหรือสร้าง Power BI แบบกำหนดเอง เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: troubleshooting
ms.date: 11/06/2018
ms.openlocfilehash: 440bb6648dca1eaa85b697a10e9fd41180c66d7e
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888109"
---
# <a name="troubleshoot-power-bi-visuals"></a><span data-ttu-id="84886-104">แก้ปัญหาวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="84886-104">Troubleshoot Power BI visuals</span></span>

## <a name="debug"></a><span data-ttu-id="84886-105">แก้</span><span class="sxs-lookup"><span data-stu-id="84886-105">Debug</span></span>

<span data-ttu-id="84886-106">**ไม่พบคำสั่ง Pbiviz (หรือข้อผิดพลาดที่คล้ายกัน)**</span><span class="sxs-lookup"><span data-stu-id="84886-106">**Pbiviz command not found (or similar errors)**</span></span>

<span data-ttu-id="84886-107">เมื่อคุณเรียกใช้ `pbiviz` ในบรรทัดคำสั่งของเทอร์มินัล คุณควรเห็นหน้าจอความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="84886-107">When you run `pbiviz` in your terminal's command line, you should see the help screen.</span></span> <span data-ttu-id="84886-108">ถ้าไม่มี แสดงว่าคำสั่งนั้นไม่ได้ถูกติดตั้งอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="84886-108">If not, then it is not installed correctly.</span></span> <span data-ttu-id="84886-109">ตรวจสอบให้แน่ใจว่า คุณติดตั้ง NodeJS เวอร์ชันขั้นต่ำ 4.0</span><span class="sxs-lookup"><span data-stu-id="84886-109">Make sure you have at least the 4.0 version of NodeJS installed.</span></span>

<span data-ttu-id="84886-110">**ไม่พบวิชวลดีบักในแท็บการแสดงภาพ**</span><span class="sxs-lookup"><span data-stu-id="84886-110">**Can't find the debug visual in the Visualizations tab**</span></span>

<span data-ttu-id="84886-111">ดีบักวิชวล มีลักษณะเหมือนไอคอนรูปพร้อมท์ภายในแท็บ **แสดงภาพ**</span><span class="sxs-lookup"><span data-stu-id="84886-111">The debug visual looks like a prompt icon within the **Visualizations** tab.</span></span>

![การเลือกวิชวล](media/power-bi-custom-visuals-troubleshoot/powerbi-developer-visual-selection.png)

<span data-ttu-id="84886-113">ถ้าคุณไม่เห็นไอคอนนั้น ตรวจสอบให้แน่ใจว่าคุณได้เปิดใช้งานภายในการตั้งค่า Power BI</span><span class="sxs-lookup"><span data-stu-id="84886-113">If you don't see it, make sure you have enabled it within the Power BI settings.</span></span>

> [!NOTE]
> <span data-ttu-id="84886-114">ดีบักวิชวล ในขณะใช้งานได้เฉพาะ ในบริการของ Power BI และยังไม่รองรับโดย Power BI Desktop หรือแอปสำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="84886-114">The debug visual is currently only available in the Power BI service and not in Power BI Desktop or the mobile app.</span></span> <span data-ttu-id="84886-115">วิชวลที่แพคเกจแล้วจะยังคงทำงานได้ทุก ๆ ที่</span><span class="sxs-lookup"><span data-stu-id="84886-115">The packaged visual will still work everywhere.</span></span>

<span data-ttu-id="84886-116">**ไม่สามารถติดต่อเซิร์ฟเวอร์วิชวล**</span><span class="sxs-lookup"><span data-stu-id="84886-116">**Can't contact visual server**</span></span>

<span data-ttu-id="84886-117">เรียกใช้เซิร์ฟเวอร์วิชวลด้วยคำสั่ง `pbiviz start` ในบรรทัดคำสั่งของเทอร์มินัล จากรากของโครงการวิชวลของคุณ</span><span class="sxs-lookup"><span data-stu-id="84886-117">Run the visual server with the command `pbiviz start` in your terminal's command line from the root of your visual project.</span></span> <span data-ttu-id="84886-118">ถ้าเซิร์ฟเวอร์ไม่ทำงาน เป็นไปได้ว่าไม่ได้ติดตั้งใบรับรอง SSL ของคุณอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="84886-118">If the server is not running, it is likely that your SSL certificates weren't installed correctly.</span></span>

<span data-ttu-id="84886-119">โปรดติดต่อทีมฝ่ายสนับสนุนด้านวิชวล Power BI (pbicvsupport@microsoft.com) เพื่อสอบถามข้อสงสัย แสดงความเห็น หรือแจ้งประเด็นใด ๆ ที่คุณมี</span><span class="sxs-lookup"><span data-stu-id="84886-119">Feel free to contact the Power BI visuals support team (pbicvsupport@microsoft.com) with any questions, comments, or issues you have.</span></span>

## <a name="next-steps"></a><span data-ttu-id="84886-120">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="84886-120">Next steps</span></span>

<span data-ttu-id="84886-121">สำหรับข้อมูลเพิ่มเติม โปรดเยี่ยมชม[คำถามที่ถามบ่อยเกี่ยวกับการแสดงผล Power BI](power-bi-custom-visuals-faq.md#organizational-power-bi-visuals)</span><span class="sxs-lookup"><span data-stu-id="84886-121">For more information, visit [Frequently asked questions about Power BI visuals](power-bi-custom-visuals-faq.md#organizational-power-bi-visuals).</span></span>