---
title: เชื่อมต่อกับฐานข้อมูล Impala ใน Power BI Desktop
description: เชื่อมต่อและใช้ฐานข้อมูล Impala ใน Power BI Desktop ได้อย่างง่ายดาย
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 01/04/2021
LocalizationGroup: Connect to data
ms.openlocfilehash: a9d817dc3e34cae2f496136fe19353ba5b993c8a
ms.sourcegitcommit: 932f6856849c39e34229dc9a49fb9379c56a888a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/06/2021
ms.locfileid: "97926416"
---
# <a name="connect-to-an-impala-database-in-power-bi-desktop"></a><span data-ttu-id="bb5b2-103">เชื่อมต่อกับฐานข้อมูล Impala ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="bb5b2-103">Connect to an Impala database in Power BI Desktop</span></span>
<span data-ttu-id="bb5b2-104">ใน Power BI Desktop คุณสามารถเชื่อมต่อกับฐานข้อมูล **Impala** และใช้ข้อมูลเบื้องต้นเช่นเดียวกับแหล่งข้อมูลอื่นใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="bb5b2-104">In Power BI Desktop, you can connect to an **Impala** database and use the underlying data just like you can with any other data source in Power BI Desktop.</span></span>

## <a name="connect-to-an-impala-database"></a><span data-ttu-id="bb5b2-105">เชื่อมต่อกับฐานข้อมูล Impala</span><span class="sxs-lookup"><span data-stu-id="bb5b2-105">Connect to an Impala database</span></span>
<span data-ttu-id="bb5b2-106">หากต้องการเชื่อมต่อกับฐานข้อมูล **Impala** ให้ปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bb5b2-106">To connect to an **Impala** database, take the following steps:</span></span> 

1. <span data-ttu-id="bb5b2-107">เลือก **รับข้อมูล** จาก ribbon **หน้าแรก** ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="bb5b2-107">Select **Get Data** from the **Home** ribbon in Power BI Desktop.</span></span> 

2. <span data-ttu-id="bb5b2-108">เลือก **ฐานข้อมูล** จากหมวดหมู่ทางด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="bb5b2-108">Select **Database** from the categories on the left.</span></span> <span data-ttu-id="bb5b2-109">คุณจะเห็น **Impala**</span><span class="sxs-lookup"><span data-stu-id="bb5b2-109">Then you see **Impala**.</span></span>

    ![รับข้อมูล](media/desktop-connect-impala/connect_impala_2.png)

3. <span data-ttu-id="bb5b2-111">ในหน้าต่าง **Impala** ที่ปรากฏขึ้น ให้พิมพ์หรือวางชื่อเซิร์ฟเวอร์ Impala ลงในกล่อง</span><span class="sxs-lookup"><span data-stu-id="bb5b2-111">In the **Impala** window that appears, type or paste the name of your Impala server into the box.</span></span> <span data-ttu-id="bb5b2-112">จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bb5b2-112">Then select **OK**.</span></span> <span data-ttu-id="bb5b2-113">คุณสามารถเลือก **นำเข้า** ข้อมูลได้โดยตรงลงใน
 Power BI หรือจะใช้ **DirectQuery** ก็ได้</span><span class="sxs-lookup"><span data-stu-id="bb5b2-113">You can **Import** data directly into Power BI or you can use **DirectQuery**.</span></span> <span data-ttu-id="bb5b2-114">เรียนรู้เพิ่มเติมเกี่ยวกับ [การใช้ DirectQuery](desktop-use-directquery.md)</span><span class="sxs-lookup"><span data-stu-id="bb5b2-114">Learn more about [using DirectQuery](desktop-use-directquery.md).</span></span>

    ![หน้าต่าง Impala](media/desktop-connect-impala/connect_impala_3a.png)

4. <span data-ttu-id="bb5b2-116">เมื่อได้รับพร้อมท์ ใส่ข้อมูลประจำตัวของคุณ หรือเชื่อมต่อแบบไม่ระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="bb5b2-116">When prompted, enter your credentials or connect anonymously.</span></span> <span data-ttu-id="bb5b2-117">ตัวเชื่อมต่อ Impala รองรับการรับรองความถูกต้องแบบไม่ระบุชื่อ, แบบพื้นฐาน (ชื่อผู้ใช้ + รหัสผ่าน) และแบบ Windows</span><span class="sxs-lookup"><span data-stu-id="bb5b2-117">The Impala connector supports Anonymous, Basic (user name + password), and Windows authentication.</span></span>

    ![ตัวเชื่อมต่อ Impala](media/desktop-connect-impala/connect_impala_4.png)

    > [!NOTE]
    > <span data-ttu-id="bb5b2-119">หลังจากคุณใส่ชื่อผู้ใช้และรหัสผ่านสำหรับเซิร์ฟเวอร์ **Impala** ที่เฉพาะเจาะจงแล้ว Power BI Desktop จะใช้ข้อมูลประจำตัวเดียวกันนั้นเพื่อพยายามเชื่อมต่อในลำดับถัดมา</span><span class="sxs-lookup"><span data-stu-id="bb5b2-119">After you put in your user name and password for a particular **Impala** server, Power BI Desktop uses those same credentials in subsequent connection attempts.</span></span> <span data-ttu-id="bb5b2-120">คุณสามารถปรับเปลี่ยนข้อมูลประจำตัวเหล่านั้นได้โดยไปที่ **ไฟล์ > ตัวเลือกและการตั้งค่า > การตั้งค่าแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="bb5b2-120">You can modify those credentials by going to **File > Options and settings > Data source settings**.</span></span>


5. <span data-ttu-id="bb5b2-121">หลังจากที่คุณเชื่อมต่อ หน้าต่าง **ตัวนำทาง** จะปรากฏขึ้น และแสดงข้อมูลที่พร้อมใช้งานบนเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="bb5b2-121">After you connect, a **Navigator** window appears and displays the data that's available on the server.</span></span> <span data-ttu-id="bb5b2-122">เลือกองค์ประกอบจากข้อมูลนี้เพื่อนำเข้าและใช้ใน **Power BI Desktop**</span><span class="sxs-lookup"><span data-stu-id="bb5b2-122">Choose elements from this data to import and use in **Power BI Desktop**.</span></span>

    ![หน้าต่างตัวนำทาง](media/desktop-connect-impala/connect_impala_5.png)

## <a name="considerations-and-limitations"></a><span data-ttu-id="bb5b2-124">ข้อควรพิจารณาและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="bb5b2-124">Considerations and limitations</span></span>
<span data-ttu-id="bb5b2-125">มีบางข้อจำกัดและข้อควรพิจารณาที่ควรระลึกถึงสำหรับตัวเชื่อมต่อ **Impala**:</span><span class="sxs-lookup"><span data-stu-id="bb5b2-125">There are a few limitations and considerations to keep in mind with the **Impala** connector:</span></span>

* <span data-ttu-id="bb5b2-126">เกตเวย์ข้อมูลภายในองค์กรรองรับตัวเชื่อมต่อ Impala โดยใช้กลไกการรับรองความถูกต้องที่รองรับสามแบบ</span><span class="sxs-lookup"><span data-stu-id="bb5b2-126">The Impala connector is supported on the on-premises data gateway, using any of the three supported authentication mechanisms.</span></span>

## <a name="next-steps"></a><span data-ttu-id="bb5b2-127">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="bb5b2-127">Next steps</span></span>
<span data-ttu-id="bb5b2-128">มีแหล่งข้อมูลต่าง ๆ มากมายที่คุณสามารถเชื่อมต่อโดยการใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="bb5b2-128">There are many different data sources that you can connect to by using Power BI Desktop.</span></span> <span data-ttu-id="bb5b2-129">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแหล่งข้อมูล โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bb5b2-129">For more information about data sources, check out the following resources:</span></span>

* [<span data-ttu-id="bb5b2-130">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="bb5b2-130">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="bb5b2-131">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="bb5b2-131">Data sources in Power BI Desktop</span></span>](desktop-data-sources.md)
* [<span data-ttu-id="bb5b2-132">จัดรูปร่างและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="bb5b2-132">Shape and combine data with Power BI Desktop</span></span>](desktop-shape-and-combine-data.md)
* [<span data-ttu-id="bb5b2-133">เชื่อมต่อกับเวิร์กบุ๊ก Excel ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="bb5b2-133">Connect to Excel workbooks in Power BI Desktop</span></span>](desktop-connect-excel.md)   
* [<span data-ttu-id="bb5b2-134">ใส่ข้อมูลลงใน Power BI Desktop โดยตรง</span><span class="sxs-lookup"><span data-stu-id="bb5b2-134">Enter data directly into Power BI Desktop</span></span>](desktop-enter-data-directly-into-desktop.md)   
