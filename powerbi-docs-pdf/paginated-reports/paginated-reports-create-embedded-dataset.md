---
title: สร้างชุดข้อมูลแบบฝังตัวสำหรับรายงานแบบแบ่งหน้า Power BI
description: ในบทความนี้ คุณจะได้เรียนรู้วิธีการสร้างชุดข้อมูลแบบฝังตัว โดยอ้างอิงจากแหล่งข้อมูลแบบฝังตัว สำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: report-builder
ms.topic: how-to
ms.date: 11/5/2018
ms.openlocfilehash: 81d755a529edb2f4fdae0ae6dbe90026b5b290d8
ms.sourcegitcommit: ccf53e87ff7cba1fcd9d2cca761a561e62933f90
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/04/2020
ms.locfileid: "93297665"
---
# <a name="create-an-embedded-dataset-for-a-paginated-report-in-the-power-bi-service"></a><span data-ttu-id="01141-103">สร้างชุดข้อมูลแบบฝังตัวสำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="01141-103">Create an embedded dataset for a paginated report in the Power BI service</span></span>

<span data-ttu-id="01141-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span><span class="sxs-lookup"><span data-stu-id="01141-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [no-desktop](../includes/no-desktop.md)]</span></span> 

<span data-ttu-id="01141-105">ในบทความนี้ คุณจะได้เรียนรู้วิธีการสร้างชุดข้อมูลแบบฝังตัว โดยอ้างอิงจากแหล่งข้อมูลแบบฝังตัว สำหรับรายงานแบบแบ่งหน้าในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="01141-105">In this article, you learn how to create an embedded dataset, based on an embedded data source, for a paginated report in the Power BI service.</span></span> <span data-ttu-id="01141-106">ชุดข้อมูลแบบฝังตัวนั้นอยู่ในรายงานแบบแบ่งหน้าแต่ละอัน สำหรับใช้ในรายงานนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="01141-106">Embedded datasets are contained in a single paginated report, for use in that report.</span></span> <span data-ttu-id="01141-107">ในตอนนี้ รายงานแบบแบ่งหน้าที่เผยแพร่ไปยังบริการของ Power BI ต้องใช้ชุดข้อมูลแบบฝังตัวและแหล่งข้อมูลแบบฝังตัว</span><span class="sxs-lookup"><span data-stu-id="01141-107">Currently, paginated reports published to the Power BI service need embedded datasets and embedded data sources.</span></span> <span data-ttu-id="01141-108">คุณอาจสร้างแหล่งข้อมูลแบบฝังตัวและชุดข้อมูลได้ในตัวสร้างรายงาน Power BI ขณะที่คุณสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="01141-108">You create the embedded data source and dataset in Power BI Report Builder, while you're creating your report.</span></span> 

<span data-ttu-id="01141-109">ก่อนที่คุณจะสร้างชุดข้อมูลได้ คุณต้องสร้างแหล่งข้อมูลก่อน</span><span class="sxs-lookup"><span data-stu-id="01141-109">Before you can create the dataset, you need to create a data source.</span></span> <span data-ttu-id="01141-110">โปรดดู [แหล่งข้อมูลแบบฝังตัวสำหรับรายงานแบบแบ่งหน้า](paginated-reports-embedded-data-source.md) ในบริการของ Power BI เพื่อเรียนรู้วิธี</span><span class="sxs-lookup"><span data-stu-id="01141-110">See [Embedded data sources for paginated reports](paginated-reports-embedded-data-source.md) in the Power BI service to learn how.</span></span>
  
## <a name="create-an-embedded-dataset"></a><span data-ttu-id="01141-111">สร้างชุดข้อมูลแบบฝังตัว</span><span class="sxs-lookup"><span data-stu-id="01141-111">Create an embedded dataset</span></span>
  
1. <span data-ttu-id="01141-112">ที่แผงข้อมูลรายงานในตัวสร้างรายงาน Power BI ให้คุณเลือก **ชุดข้อมูล** > **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="01141-112">In the Report Data pane in Power BI Report Builder, select **New** > **Dataset**.</span></span>

1. <span data-ttu-id="01141-113">ในแท็บ **คิวรี** ของกล่องโต้ตอบ **คุณสมบัติชุดข้อมูล** ให้คุณตั้งชื่อให้ชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="01141-113">In the **Query** tab of the **Dataset Properties** dialog box, give the dataset a name.</span></span> <span data-ttu-id="01141-114">แหล่งข้อมูลแบบฝังตัวอยู่ในกล่อง **แหล่งข้อมูล** อยู่แล้ว หรือคุณอาจเลือก **ใหม่** เพื่อสร้างแหล่งข้อมูลแบบฝังตัวอื่นได้</span><span class="sxs-lookup"><span data-stu-id="01141-114">The embedded data source is already in the **Data source** box, or you can select **New** to create a different embedded data source.</span></span>
 
   ![ชุดข้อมูลใหม่](media/paginated-reports-create-embedded-dataset/power-bi-paginated-new-dataset.png)  

3. <span data-ttu-id="01141-116">ที่ใต้ **ชนิดคิวรี** ให้คุณเลือกชนิดคำสั่งหรือคิวรีที่จะใช้กับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="01141-116">Under **Query type** , select the type of command or query to use for the dataset.</span></span> 
    - <span data-ttu-id="01141-117">**ข้อความ** จะเรียกใช้คิวรีให้ดึงข้อมูลจากฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="01141-117">**Text** runs a query to retrieve data from the database.</span></span> <span data-ttu-id="01141-118">ซึ่งเป็นค่าเริ่มต้นและใช้กับคิวรีส่วนมาก</span><span class="sxs-lookup"><span data-stu-id="01141-118">It's the default and is used for most queries.</span></span> <span data-ttu-id="01141-119">พิมพ์คิวรีหรือนำเข้าคิวรีที่มีอยู่ก่อนโดยการเลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="01141-119">Type a query or import a pre-existing query by selecting **Import**.</span></span> <span data-ttu-id="01141-120">เลือก **ตัวออกแบบคิวรี** เพื่อสร้างคิวรีโดยใช้กราฟิก</span><span class="sxs-lookup"><span data-stu-id="01141-120">To build the query graphically, select **Query Designer**.</span></span> <span data-ttu-id="01141-121">ถ้าคุณใช้ตัวออกแบบคิวรีเพื่อสร้างคิวรี ข้อความของคิวรีนั้นจะปรากฏในกล่องนี้</span><span class="sxs-lookup"><span data-stu-id="01141-121">If you use the query designer to build a query, the text of the query will appear in this box.</span></span> <span data-ttu-id="01141-122">เลือกปุ่ม **นิพจน์** ( **fx** ) เพื่อใช้นิพจน์ในการสร้างคิวรีแบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="01141-122">Select the **Expression** ( **fx** ) button to use an expression to dynamically generate the query.</span></span> 
    - <span data-ttu-id="01141-123">**ตาราง** จะเลือกเขตข้อมูลทั้งหมดภายในตาราง</span><span class="sxs-lookup"><span data-stu-id="01141-123">**Table** selects all the fields within a table.</span></span> <span data-ttu-id="01141-124">ใส่ชื่อของตารางที่คุณต้องการใช้เป็นชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="01141-124">Enter the name of the table that you want to use as a dataset.</span></span>
    - <span data-ttu-id="01141-125">**Stored Procedure** จะเรียกใช้ขั้นตอนที่เก็บไว้จากชื่อ</span><span class="sxs-lookup"><span data-stu-id="01141-125">**Stored Procedure** runs a stored procedure by name.</span></span>

4. <span data-ttu-id="01141-126">ในตัวออกแบบคิวรี คุณจะเห็นและได้โต้ตอบกับตารางและเขตข้อมูลในชุดข้อมูล รวมถึงนำเข้าคิวรีหรือแก้ไขในรูปแบบข้อความ</span><span class="sxs-lookup"><span data-stu-id="01141-126">In the Query Designer, you can see and interact with the tables and fields in the dataset, import a query, or edit as text.</span></span> <span data-ttu-id="01141-127">คุณยังสามารถเพิ่มตัวกรองและพารามิเตอร์ได้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="01141-127">You can also add filters and parameters here.</span></span> 

    ![ตัวออกแบบคิวรี](media/paginated-reports-create-embedded-dataset/power-bi-paginated-embedded-dataset-edit-query.png)

5. <span data-ttu-id="01141-129">ในตัวออกแบบคิวรี ให้คุณเลือก **เรียกใช้คิวรี** เพื่อทดสอบ จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="01141-129">In the Query Designer, select **Run Query** to test it, then select **OK**.</span></span>

1. <span data-ttu-id="01141-130">กลับไปดูที่กล่องโต้ตอบคุณสมบัติชุดข้อมูล ในกล่อง **การหมดเวลา (เป็นวินาที)** ให้คุณพิมพ์จำนวนวินาทีก่อนที่คิวรีจะหมดเวลา ค่าเริ่มต้นคือ 30 วินาที</span><span class="sxs-lookup"><span data-stu-id="01141-130">Back in the Dataset Properties dialog box, in the **Time out (in seconds)** box, type the number of seconds until the query times out. The default is 30 seconds.</span></span> <span data-ttu-id="01141-131">ค่าสำหรับ **การหมดเวลา** ต้องว่างเปล่าหรือมากกว่าศูนย์</span><span class="sxs-lookup"><span data-stu-id="01141-131">The value for **Time out** must be empty or greater than zero.</span></span> <span data-ttu-id="01141-132">ถ้าค่าว่างเปล่า คิวรีจะไม่หมดเวลา</span><span class="sxs-lookup"><span data-stu-id="01141-132">If it is empty, the query does not time out.</span></span>

7.  <span data-ttu-id="01141-133">คุณสามารถตั้งค่าคุณสมบัติอื่นๆ สำหรับชุดข้อมูลได้ที่แท็บอื่น:</span><span class="sxs-lookup"><span data-stu-id="01141-133">You can set other properties for the dataset on the other tabs:</span></span>
    - <span data-ttu-id="01141-134">สร้างเขตข้อมูลที่คำนวณที่แท็บ **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="01141-134">Create calculated fields on the **Fields** tab.</span></span>
    - <span data-ttu-id="01141-135">ตั้งค่าตัวเลือกขั้นสูงที่แท็บ **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="01141-135">Set advanced options on the **Options** tab.</span></span>
    - <span data-ttu-id="01141-136">เพิ่มหรืออัปเดต **ตัวกรอง** และ **พารามิเตอร์** ที่แท็บที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="01141-136">Add or update **Filters** and **Parameters** on their respective tabs.</span></span>

8. <span data-ttu-id="01141-137">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="01141-137">Select **OK**</span></span>
 
   <span data-ttu-id="01141-138">รายงานจะเปิดขึ้นในมุมมองการออกแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="01141-138">The report opens in Report Design View.</span></span> <span data-ttu-id="01141-139">แหล่งข้อมูล ชุดข้อมูล และคอลเลกชันเขตข้อมูลของชุดข้อมูลจะปรากฏในแผงข้อมูลรายงาน และคุณสามารถออกแบบรายงานแบบแบ่งหน้าต่อได้</span><span class="sxs-lookup"><span data-stu-id="01141-139">The data source, dataset, and dataset field collection appear in the Report Data pane, and you can continue designing your paginated report.</span></span>  

    ![ชุดข้อมูลในมุมมองการออกแบบรายงาน](media/paginated-reports-create-embedded-dataset/power-bi-paginated-embedded-dataset-report-design-view.png) 
 
## <a name="next-steps"></a><span data-ttu-id="01141-141">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="01141-141">Next steps</span></span> 

- [<span data-ttu-id="01141-142">รายงานแบบแบ่งหน้าใน Power BI Premium คืออะไร</span><span class="sxs-lookup"><span data-stu-id="01141-142">What are paginated reports in Power BI Premium?</span></span>](paginated-reports-report-builder-power-bi.md)  
- [<span data-ttu-id="01141-143">บทช่วยสอน: สร้างรายงานแบบแบ่งหน้าและอัปโหลดไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="01141-143">Tutorial: Create a paginated report and upload it to the Power BI service</span></span>](paginated-reports-quickstart-aw.md)
- [<span data-ttu-id="01141-144">เผยแพร่รายงานแบบแบ่งหน้าไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="01141-144">Publish a paginated report to the Power BI service</span></span>](paginated-reports-save-to-power-bi-service.md)

