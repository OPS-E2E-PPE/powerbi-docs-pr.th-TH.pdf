---
title: ภาพรวมไปป์ไลน์การปรับใช้
description: เรียนรู้เกี่ยวกับไปป์ไลน์การปรับใช้ใน Power BI
author: KesemSharabi
ms.author: kesharab
ms.topic: conceptual
ms.service: powerbi
ms.subservice: pbi-deployment
ms.custom: contperf-fy21q1
ms.date: 10/21/2020
ms.openlocfilehash: ba2aedd4d503d468ba47640dd29fcfe004825ba5
ms.sourcegitcommit: 7bf09116163afaae312eb2b232eb7967baee2c92
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/17/2020
ms.locfileid: "97621130"
---
# <a name="introduction-to-deployment-pipelines"></a><span data-ttu-id="0a044-103">บทนำเกี่ยวกับขั้นตอนการปรับใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0a044-103">Introduction to deployment pipelines</span></span>

<span data-ttu-id="0a044-104">ในโลกปัจจุบัน การวิเคราะห์ถือเป็นส่วนสำคัญของการตัดสินใจในเกือบทุกองค์กร</span><span class="sxs-lookup"><span data-stu-id="0a044-104">In today’s world, analytics is a vital part of decision making in almost every organization.</span></span> <span data-ttu-id="0a044-105">การใช้งาน Power BI ในฐานะเครื่องมือวิเคราะห์ ที่เพิ่มขึ้นนั้นจำเป็นต้องใช้ข้อมูลมากขึ้น ต้องให้ดูน่าสนใจ และใช้งานง่าย</span><span class="sxs-lookup"><span data-stu-id="0a044-105">The growing use of Power BI as an analytics tool, requires it to use more data, look appealing and  be user-friendly.</span></span> <span data-ttu-id="0a044-106">อย่างไรก็ตามเหนือสิ่งอื่นใดนั้น Power BI จำเป็นต้องพร้อมให้ใช้งาน และเชื่อถือได้อยู่เสมอ</span><span class="sxs-lookup"><span data-stu-id="0a044-106">Above all however, Power BI needs to always be available and reliable.</span></span> <span data-ttu-id="0a044-107">เพื่อให้เป็นไปตามข้อกำหนดเหล่านี้ ผู้สร้าง BI จำเป็นต้องทำงานร่วมกันอย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="0a044-107">To meet these requirements, BI creators must collaborate effectively.</span></span>

<span data-ttu-id="0a044-108">เครื่องมือไปป์ไลน์การปรับใช้จะช่วยให้ผู้สร้าง BI จัดการวงจรชีวิตของเนื้อหาเชิงองค์กรได้</span><span class="sxs-lookup"><span data-stu-id="0a044-108">The deployment pipelines tool enables BI creators to manage the lifecycle of organizational content.</span></span> <span data-ttu-id="0a044-109">เครื่องมือนี้เป็นเครื่องมือที่ทรงประสิทธิภาพและนำกลับมาใช้งานใหม่ได้สำหรับผู้สร้างในองค์กรที่ใช้ความจุแบบ Premium</span><span class="sxs-lookup"><span data-stu-id="0a044-109">It's an efficient and reusable tool for creators in an enterprise with Premium capacity.</span></span> <span data-ttu-id="0a044-110">ไปป์ไลน์การปรับใช้ช่วยให้ผู้สร้างสามารถพัฒนาและทดสอบเนื้อหาของ Power BI ก่อนที่ผู้ใช้จะนำเนื้อหาไปใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="0a044-110">Deployment pipelines enables creators to develop and test Power BI content before the content is consumed by users.</span></span> <span data-ttu-id="0a044-111">ชนิดของเนื้อหาดังกล่าวประกอบด้วยรายงาน แดชบอร์ด และชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0a044-111">The content types include reports, dashboards, and datasets.</span></span>

<span data-ttu-id="0a044-112">เครื่องมือได้รับการออกแบบมาเป็นไปป์ไลน์ที่มีสามขั้นตอนดังนี้:</span><span class="sxs-lookup"><span data-stu-id="0a044-112">The tool is designed as a pipeline with three stages:</span></span>

* <span data-ttu-id="0a044-113">**<a name="development"></a>การพัฒนา**</span><span class="sxs-lookup"><span data-stu-id="0a044-113">**<a name="development"></a>Development**</span></span>
    
    <span data-ttu-id="0a044-114">ขั้นตอนนี้ใช้เพื่อออกแบบ สร้าง และอัปโหลดเนื้อหาใหม่กับผู้สร้างคนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="0a044-114">This stage is used to design, build, and upload new content with  fellow creators.</span></span> <span data-ttu-id="0a044-115">ขั้นตอนนี้เป็นขั้นแรกในไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="0a044-115">This is the first stage in deployment pipelines.</span></span>

* <span data-ttu-id="0a044-116">**<a name="test"></a>การทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="0a044-116">**<a name="test"></a>Test**</span></span>

    <span data-ttu-id="0a044-117">คุณจะพร้อมเข้าสู่ขั้นตอนการทดสอบทันที หลังจากที่คุณทำการเปลี่ยนแปลงที่จำเป็นทั้งหมดต่อเนื้อหาของคุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="0a044-117">You're ready to enter the test stage after you've made all the needed changes to your content.</span></span> <span data-ttu-id="0a044-118">คุณเพียงแค่อัปโหลดเนื้อหาที่ปรับเปลี่ยนแล้วขึ้นไป เพื่อให้สามารถไปยังขั้นตอนการทดสอบนี้ได้</span><span class="sxs-lookup"><span data-stu-id="0a044-118">You upload the modified content so it can be moved to this test stage.</span></span> <span data-ttu-id="0a044-119">นี่คือตัวอย่างสามของสิ่งที่คุณสามารถทำได้ในสภาพแวดล้อมการทดสอบ:</span><span class="sxs-lookup"><span data-stu-id="0a044-119">Here are three examples of what can be done in the test environment:</span></span>

    * <span data-ttu-id="0a044-120">แชร์เนื้อหากับผู้ทดสอบและผู้รีวิว</span><span class="sxs-lookup"><span data-stu-id="0a044-120">Share content with testers and reviewers</span></span>

    * <span data-ttu-id="0a044-121">โหลดและเรียกใช้การทดสอบในปริมาณข้อมูลขนาดใหญ่</span><span class="sxs-lookup"><span data-stu-id="0a044-121">Load and run tests with larger volumes of data</span></span>

    * <span data-ttu-id="0a044-122">ทดสอบแอปของคุณเพื่อดูว่าผู้ใช้ของคุณจะมองเห็นแอปในลักษณะใด</span><span class="sxs-lookup"><span data-stu-id="0a044-122">Test your app to see how it will look for your end users</span></span>

* <span data-ttu-id="0a044-123">**<a name="production"></a>การผลิต**</span><span class="sxs-lookup"><span data-stu-id="0a044-123">**<a name="production"></a>Production**</span></span>

    <span data-ttu-id="0a044-124">หลังทดสอบเนื้อหาแล้ว ให้ใช้ขั้นตอนการผลิตเพื่อแชร์เนื้อหาเวอร์ชันสุดท้ายของคุณกับผู้ใช้ทางธุรกิจทั่วทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="0a044-124">After testing the content, use the production stage to share the final version of your content with business users across the organization.</span></span>

![สกรีนช็อตของไปป์ไลน์การปรับใช้งานที่มีทั้งสามขั้นตอน ได้แก่ การพัฒนา การทดสอบและการผลิต การเพิ่มข้อมูล](media/deployment-pipelines-overview/deployment-pipelines.png)

## <a name="next-steps"></a><span data-ttu-id="0a044-126">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="0a044-126">Next steps</span></span>

>[!div class="nextstepaction"]
>[<span data-ttu-id="0a044-127">เริ่มต้นกับไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="0a044-127">Get started with deployment pipelines</span></span>](deployment-pipelines-get-started.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="0a044-128">ทำความเข้าใจกระบวนการไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="0a044-128">Understand the deployment pipelines process</span></span>](deployment-pipelines-process.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="0a044-129">การแก้ไขปัญหาไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="0a044-129">Deployment pipelines troubleshooting</span></span>](deployment-pipelines-troubleshooting.md)

>[!div class="nextstepaction"]
>[<span data-ttu-id="0a044-130">แนวทางปฏิบัติที่ดีที่สุดสำหรับไปป์ไลน์การปรับใช้</span><span class="sxs-lookup"><span data-stu-id="0a044-130">Deployment pipelines best practices</span></span>](deployment-pipelines-best-practices.md)
