---
title: ใช้ภาษาธรรมชาติกับ import, live connect และ direct query
description: ในบทความนี้ เราจะดูว่าคุณลักษณะ Q&A ทำงานร่วมกับแหล่งข้อมูลประเภทต่างๆ ที่มีอยู่ใน Power BI อย่างไร นอกจากนี้ เราจะดูแนวคิดของการจัดทำดัชนีและการแคช
author: mohaali
ms.author: mohaali
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: conceptual
ms.date: 08/19/2020
ms.openlocfilehash: 23ecc8edd82f6c1694c850f73fef2a892230ff14
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96418980"
---
# <a name="use-natural-language-with-import-live-connect-and-direct-query"></a><span data-ttu-id="a9860-104">ใช้ภาษาธรรมชาติกับ import, live connect และ direct query</span><span class="sxs-lookup"><span data-stu-id="a9860-104">Use natural language with import, live connect, and direct query</span></span>

<span data-ttu-id="a9860-105">คุณลักษณะ Q&A ใน Power BI ช่วยให้คุณรับคำตอบจากข้อมูลของคุณได้อย่างรวดเร็วโดยใช้ภาษาธรรมชาติเพื่อถามคำถามเกี่ยวกับข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="a9860-105">The Q&A feature in Power BI lets you quickly get answers from your data by using natural language to ask questions about that data.</span></span> <span data-ttu-id="a9860-106">บทความนี้อธิบายถึงวิธีการใช้การจัดทำดัชนีและการแคชเพื่อปรับปรุงประสิทธิภาพสำหรับการกำหนดค่าที่รองรับแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="a9860-106">This article describes how indexing and caching are used to improve performance for each supported configuration.</span></span>

## <a name="what-data-sources-are-supported-in-qa"></a><span data-ttu-id="a9860-107">Q&A รองรับแหล่งข้อมูลใดบ้าง</span><span class="sxs-lookup"><span data-stu-id="a9860-107">What data sources are supported in Q&A?</span></span>

<span data-ttu-id="a9860-108">การกำหนดค่าต่อไปนี้รองรับ Q&A :</span><span class="sxs-lookup"><span data-stu-id="a9860-108">Q&A is supported in the following configurations:</span></span>

- <span data-ttu-id="a9860-109">โหมดการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="a9860-109">Import mode</span></span>
- <span data-ttu-id="a9860-110">โหมด Live connect - การใช้ SQL Server Analysis Services ภายในองค์กร, Azure Analysis Services หรือชุดข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="a9860-110">Live connect mode – Using on-premises SQL Server Analysis Services, Azure Analysis Services, or Power BI datasets</span></span>
- <span data-ttu-id="a9860-111">Direct Query – Azure Synapse, Azure SQL และ SQL Server 2019</span><span class="sxs-lookup"><span data-stu-id="a9860-111">Direct Query – Azure Synapse, Azure SQL, and SQL Server 2019.</span></span> <span data-ttu-id="a9860-112">แม้ว่าแหล่งข้อมูลอื่นอาจทำงานได้ในโหมด Direct Query แต่เราไม่ได้สนับสนุนแหล่งข้อมูลเหล่านี้อย่างเป็นทางการ</span><span class="sxs-lookup"><span data-stu-id="a9860-112">Although other sources may work in direct query mode, we do not officially support these sources.</span></span>

<span data-ttu-id="a9860-113">ตามค่าเริ่มต้น Q&A จะเปิดใช้งานภายในรายงานถ้าคุณใช้วิชวล Q&A</span><span class="sxs-lookup"><span data-stu-id="a9860-113">By default, Q&A is enabled inside a report if you use the Q&A visual.</span></span> <span data-ttu-id="a9860-114">พร้อมท์จะปรากฏขึ้นถ้าคุณกำลังใช้ Direct Query หรือ Live connect</span><span class="sxs-lookup"><span data-stu-id="a9860-114">A prompt will appear if you're using Direct Query or Live connect.</span></span> <span data-ttu-id="a9860-115">คุณสามารถเปิด/ปิดความสามารถภาษาธรรมชาติสำหรับรายงานได้อย่างชัดเจนโดยเข้าไปในตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="a9860-115">You can explicitly turn on/off the natural language capabilities for a report by going into options.</span></span>

![ตัวเลือก Q&A desktop](media/qna-desktop-options.png)

<span data-ttu-id="a9860-117">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ข้อจำกัดของ Power BI Q&A](q-and-a-limitations.md)</span><span class="sxs-lookup"><span data-stu-id="a9860-117">For more information, see [Limitations of Power BI Q&A](q-and-a-limitations.md).</span></span>

## <a name="how-does-indexing-work-with-qa"></a><span data-ttu-id="a9860-118">การจัดทำดัชนีทำงานร่วมกับ Q&A อย่างไร</span><span class="sxs-lookup"><span data-stu-id="a9860-118">How does indexing work with Q&A?</span></span>

<span data-ttu-id="a9860-119">เมื่อคุณเปิดใช้งาน Q&A ดัชนีจะถูกสร้างขึ้นเพื่อให้คำติชมแบบเรียลไทม์แก่ผู้ใช้อย่างรวดเร็วและช่วยตีความคำถามของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="a9860-119">When you enable Q&A, an index is built to quickly provide real-time feedback to the user and to help interpret the user’s questions.</span></span> <span data-ttu-id="a9860-120">ดัชนีอาจใช้เวลาสักครู่ในการสร้างและจะมีองค์ประกอบและข้อจำกัดดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a9860-120">The index can take some time to build and will have the following elements and limitations.</span></span>

- <span data-ttu-id="a9860-121">ชื่อคอลัมน์และตารางทั้งหมดจะถูกแทรกลงในดัชนี เว้นแต่จะถูกปิดอย่างชัดเจนจากภายในเครื่องมือ Q&A</span><span class="sxs-lookup"><span data-stu-id="a9860-121">All column names and tables are inserted into the index unless it has been explicitly turned off from within the Q&A tooling.</span></span>
- <span data-ttu-id="a9860-122">ค่าข้อความทั้งหมดที่น้อยกว่า 100 อักขระจะถูกจัดทำดัชนี</span><span class="sxs-lookup"><span data-stu-id="a9860-122">All text values fewer than 100 characters will be indexed.</span></span> <span data-ttu-id="a9860-123">ค่าข้อความที่มากกว่า 100 อักขระจะไม่ถูกจัดทำดัชนี</span><span class="sxs-lookup"><span data-stu-id="a9860-123">Text values greater than 100 characters won't be indexed.</span></span> 
- <span data-ttu-id="a9860-124">Q&A จะเก็บค่าที่ไม่ซ้ำกันสูงสุด 5 ล้านค่าในดัชนี</span><span class="sxs-lookup"><span data-stu-id="a9860-124">Q&A will store a maximum of 5 million unique values in its index.</span></span> <span data-ttu-id="a9860-125">หากคุณมีค่าเกินเกณฑ์นี้ ดัชนีจะไม่เก็บค่าที่เป็นไปได้ทั้งหมดซึ่งอาจลดความแม่นยำของผลลัพธ์ที่คุณได้รับจาก Q&A</span><span class="sxs-lookup"><span data-stu-id="a9860-125">If you exceed this threshold, the index won't hold all the potential values which may decrease the accuracy of the results you receive from Q&A.</span></span>
- <span data-ttu-id="a9860-126">หากเกิดข้อผิดพลาดระหว่างการจัดทำดัชนี ดัชนีจะยังคงอยู่ในสถานะบางส่วนและจะถูกสร้างขึ้นใหม่ในการรีเฟรชครั้งถัดไป ตามที่อธิบายไว้ในส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a9860-126">If an error occurs during indexing, the index will remain in a partial state and will be recreated on the next refresh, as described in the next section.</span></span>

## <a name="how-often-is-the-index-refreshed-and-cached"></a><span data-ttu-id="a9860-127">มีการรีเฟรชและแคชดัชนีบ่อยแค่ไหน</span><span class="sxs-lookup"><span data-stu-id="a9860-127">How often is the index refreshed and cached?</span></span>

<span data-ttu-id="a9860-128">ใน Power BI Desktop ดัชนีจะถูกสร้างขึ้นในเวลาที่คุณใช้ Q&A</span><span class="sxs-lookup"><span data-stu-id="a9860-128">In Power BI Desktop, the index is created at the time you use Q&A.</span></span> <span data-ttu-id="a9860-129">ไอคอนเล็ก ๆ จะปรากฏขึ้นเพื่อแจ้งให้คุณทราบว่ากำลังมีการสร้างดัชนี</span><span class="sxs-lookup"><span data-stu-id="a9860-129">A small icon will appear letting you know the index is being built.</span></span> <span data-ttu-id="a9860-130">ในช่วงเวลานี้ อาจใช้เวลาโหลดวิชวล Q&A รวมถึงคำแนะนำสักครู่</span><span class="sxs-lookup"><span data-stu-id="a9860-130">During this time, the Q&A visual, including suggestions, may take some time to load.</span></span>

<span data-ttu-id="a9860-131">ในบริการ Power BI ดัชนีจะถูกสร้างขึ้นใหม่เมื่อเผยแพร่/เผยแพร่ใหม่และรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="a9860-131">In Power BI Service, the index is recreated on publish/republish and refresh.</span></span> <span data-ttu-id="a9860-132">ดัชนี Q&A ไม่ได้ถูกสร้างขึ้นโดยอัตโนมัติเสมอไป และบางครั้งจะขึ้นอยู่กับเกณฑ์ตามความต้องการเพื่อปรับการรีเฟรชชุดข้อมูลให้เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="a9860-132">The Q&A index isn't always created automatically and will sometimes be based upon an on-demand basis to optimize the dataset refreshes.</span></span> <span data-ttu-id="a9860-133">สำหรับ Direct Query เราจะจัดทำดัชนีข้อมูลไม่เกินวันละครั้งเพื่อลดผลกระทบต่อแหล่งที่มาของ Direct Query</span><span class="sxs-lookup"><span data-stu-id="a9860-133">For Direct Query, we'll index the data at most once per day to reduce the impact on the Direct Query source.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a9860-134">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a9860-134">Next steps</span></span>

<span data-ttu-id="a9860-135">คุณสามารถผสานรวมภาษาธรรมชาติในรายงานของคุณได้หลายวิธี</span><span class="sxs-lookup"><span data-stu-id="a9860-135">You can integrate natural language in your reports in a variety of ways.</span></span> <span data-ttu-id="a9860-136">สำหรับข้อมูลเพิ่มเติม โปรดดูบทความเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="a9860-136">For more information, see these articles:</span></span>

* [<span data-ttu-id="a9860-137">วิชวลระบบถามตอบ</span><span class="sxs-lookup"><span data-stu-id="a9860-137">Q&A visual</span></span>](../visuals/power-bi-visualization-q-and-a.md)
* [<span data-ttu-id="a9860-138">แนวทางปฏิบัติที่ดีที่สุดของระบบถามตอบ</span><span class="sxs-lookup"><span data-stu-id="a9860-138">Q&A best practices</span></span>](q-and-a-best-practices.md)
