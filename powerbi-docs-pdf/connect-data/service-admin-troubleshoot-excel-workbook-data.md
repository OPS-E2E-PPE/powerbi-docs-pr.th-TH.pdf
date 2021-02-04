---
title: 'ข้อผิดพลาด: เราไม่พบข้อมูลใด ๆ ในสมุดงาน Excel ของคุณ'
description: 'ข้อผิดพลาด: เราไม่พบข้อมูลใด ๆ ในสมุดงาน Excel ของคุณ'
author: kfollis
ms.author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: troubleshooting
ms.date: 04/30/2019
ms.custom: seodec18
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 6e78dba3e6a18544f68fae4b737a7840d1fa2724
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96403800"
---
# <a name="error-we-couldnt-find-any-data-in-your-excel-workbook"></a><span data-ttu-id="d5954-103">ข้อผิดพลาด: เราไม่พบข้อมูลใด ๆ ในสมุดงาน Excel ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d5954-103">Error: We couldn't find any data in your Excel workbook</span></span>

>[!NOTE]  
><span data-ttu-id="d5954-104">บทความนี้นำไปใช้กับ Excel 2007 และเวอร์ชันที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="d5954-104">This article applies to Excel 2007 and later.</span></span>

<span data-ttu-id="d5954-105">เมื่อคุณนำเข้าสมุดงาน Excel ไปใน Power BI คุณอาจเห็นข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d5954-105">When you import an Excel workbook into Power BI, you may see the following error:</span></span>

<span data-ttu-id="d5954-106">*ข้อผิดพลาด: เราไม่พบข้อมูลใดๆ ที่จัดรูปแบบเป็นตาราง เมื่อต้องการนำเข้าจากโปรแกรม Excel ลงในบริการของ Power BI คุณต้องจัดรูปแบบข้อมูลเป็นตาราง เลือกข้อมูลทั้งหมดที่คุณต้องการในตารางและกด Ctrl + T*</span><span class="sxs-lookup"><span data-stu-id="d5954-106">*Error: We couldn't find any data formatted as a table. To import from Excel into the Power BI service, you need to format the data as a table. Select all the data you want in the table and press Ctrl+T.*</span></span>

![ไม่พบข้อมูลในสมุดงาน](media/service-admin-troubleshoot-excel-workbook-data/power-bi-we-couldnt-find-any-data.png)

## <a name="quick-solution"></a><span data-ttu-id="d5954-108">แก้ไขปัญหาอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="d5954-108">Quick solution</span></span>
1. <span data-ttu-id="d5954-109">แก้ไขมุดงานใน Excel</span><span class="sxs-lookup"><span data-stu-id="d5954-109">Edit your workbook in Excel.</span></span>
2. <span data-ttu-id="d5954-110">เลือกช่วงของเซลล์ที่มีข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="d5954-110">Select the range of cells that contain your data.</span></span> <span data-ttu-id="d5954-111">แถวแรกควรประกอบด้วยส่วนหัวของคอลัมน์ (ชื่อคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="d5954-111">The first row should contain your column headers (the column names).</span></span>
3. <span data-ttu-id="d5954-112">กด **Ctrl + T** เพื่อสร้างตาราง</span><span class="sxs-lookup"><span data-stu-id="d5954-112">Press **Ctrl + T** to create a table.</span></span>
4. <span data-ttu-id="d5954-113">บันทึกสมุดงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="d5954-113">Save your workbook.</span></span>
5. <span data-ttu-id="d5954-114">กลับไปยัง Power BI และนำเข้าสมุดงานของคุณอีกครั้ง หรือถ้าคุณกำลังทำงานใน Excel 2016 และคุณได้บันทึกสมุดงานของคุณไปยัง OneDrive for Business ใน Excel ให้คลิกไฟล์ > เผยแพร่</span><span class="sxs-lookup"><span data-stu-id="d5954-114">Return to Power BI and import your workbook again, or if you're working in Excel 2016 and you've saved your workbook to OneDrive for Business, in Excel, click File > Publish.</span></span>

## <a name="details"></a><span data-ttu-id="d5954-115">รายละเอียด</span><span class="sxs-lookup"><span data-stu-id="d5954-115">Details</span></span>
### <a name="cause"></a><span data-ttu-id="d5954-116">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="d5954-116">Cause</span></span>
<span data-ttu-id="d5954-117">ใน Excel คุณสามารถสร้า **ตาราง** นอกช่วงของเซลล์ได้ ซึ่งทำให้ง่ายขึ้นเมื่อต้องการเรียงลำดับ กรอง และจัดรูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d5954-117">In Excel, you can create a **table** out of a range of cells, which makes it easier to sort, filter, and format data.</span></span>

<span data-ttu-id="d5954-118">เมื่อคุณนำเข้าสมุดงาน Excel, Power BI จะค้นหาตารางเหล่านี้และนำเข้าในชุดข้อมูลหนึ่ง ถ้าไม่พบตารางใด คุณจะเห็นข้อความข้อผิดพลาดนี้</span><span class="sxs-lookup"><span data-stu-id="d5954-118">When you import an Excel workbook, Power BI looks for these tables and imports them into a dataset; if it doesn't find any tables, you'll see this error message.</span></span>

### <a name="solution"></a><span data-ttu-id="d5954-119">วิธีแก้</span><span class="sxs-lookup"><span data-stu-id="d5954-119">Solution</span></span>
1. <span data-ttu-id="d5954-120">เปิดสมุดงานของคุณใน Excel</span><span class="sxs-lookup"><span data-stu-id="d5954-120">Open your workbook in Excel.</span></span> 
    >[!NOTE]
    ><span data-ttu-id="d5954-121">รูปภาพต่อไปนี้เป็นภาพของ Excel 2013</span><span class="sxs-lookup"><span data-stu-id="d5954-121">The pictures here are of Excel 2013.</span></span> <span data-ttu-id="d5954-122">ถ้าคุณกำลังใช้เวอร์ชันอื่น องค์ประกอบต่าง ๆ อาจแตกต่างกันเล็กน้อย แต่ขั้นตอนต่าง ๆ จะเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="d5954-122">If you're using a different version, things may look a little different, but the steps are the same.</span></span>
    
    ![เปิดเวิร์กบุ๊ก](media/service-admin-troubleshoot-excel-workbook-data/power-bi-troubleshoot-excel-worksheet-1.png)
2. <span data-ttu-id="d5954-124">เลือกช่วงของเซลล์ที่มีข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="d5954-124">Select the range of cells that contain your data.</span></span> <span data-ttu-id="d5954-125">แถวแรกควรประกอบด้วยส่วนหัวของคอลัมน์ (ชื่อคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="d5954-125">The first row should contain your column headers (the column names):</span></span>
   
    ![เลือกช่วงของเซลล์](media/service-admin-troubleshoot-excel-workbook-data/power-bi-troubleshoot-excel-worksheet-2.png)
3. <span data-ttu-id="d5954-127">ใน Ribbon บนแถบ **แทรก** คลิก **ตาราง**</span><span class="sxs-lookup"><span data-stu-id="d5954-127">In the ribbon on the **INSERT** tab, click **Table**.</span></span> <span data-ttu-id="d5954-128">(หรือโดยการใช้ทางลัด กด **Ctrl + T**)</span><span class="sxs-lookup"><span data-stu-id="d5954-128">(Or, as a shortcut, press **Ctrl + T**.)</span></span>
   
    ![ใส่ตาราง](media/service-admin-troubleshoot-excel-workbook-data/power-bi-troubleshoot-excel-worksheet-3.png)
4. <span data-ttu-id="d5954-130">คุณจะเห็นกล่องโต้ตอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d5954-130">You'll see the following dialog.</span></span> <span data-ttu-id="d5954-131">ตรวจสอบให้แน่ใจว่าได้เลือก **ตารางของฉันมีส่วนหัว** และเลือก **ตกลง**:</span><span class="sxs-lookup"><span data-stu-id="d5954-131">Make sure **My table has headers** is checked, and select **OK**:</span></span>
   
    ![สร้างตาราง](media/service-admin-troubleshoot-excel-workbook-data/power-bi-troubleshoot-excel-create-table.png)
5. <span data-ttu-id="d5954-133">ในตอนนี้ ข้อมูลของคุณถูกจัดรูปแบบเป็นตาราง:</span><span class="sxs-lookup"><span data-stu-id="d5954-133">Now your data is formatted as a table:</span></span>
   
    ![ข้อมูลที่จัดรูปแบบเป็นตาราง](media/service-admin-troubleshoot-excel-workbook-data/power-bi-troubleshoot-excel-table.png)
6. <span data-ttu-id="d5954-135">บันทึกสมุดงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="d5954-135">Save your workbook.</span></span>
7. <span data-ttu-id="d5954-136">กลับไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="d5954-136">Return to Power BI.</span></span> <span data-ttu-id="d5954-137">เลือก รับข้อมูล ที่ด้านล่างของบานหน้าต่างนำทาง</span><span class="sxs-lookup"><span data-stu-id="d5954-137">Select Get Data at the bottom of the nav pane.</span></span>
   
    ![รับข้อมูล](media/service-admin-troubleshoot-excel-workbook-data/power-bi-get-data.png)
8. <span data-ttu-id="d5954-139">ในกล่อง **ไฟล์** เลือก **รับ**</span><span class="sxs-lookup"><span data-stu-id="d5954-139">In the **Files** box, select **Get**.</span></span>
   
    ![รับไฟล์](media/service-admin-troubleshoot-excel-workbook-data/power-bi-get-files.png)
9. <span data-ttu-id="d5954-141">นำเข้าสมุดงาน Excel ของคุณอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="d5954-141">Import your Excel workbook again.</span></span> <span data-ttu-id="d5954-142">ขณะนี้ การนำเข้าควรพบตารางและดำเนินการสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="d5954-142">This time, the import should find the table and succeed.</span></span>
   
    <span data-ttu-id="d5954-143">ถ้าการนำเข้ายังคงล้มเหลว แจ้งให้เราทราบโดยการคลิก \*\* ชุมชน \*\* ในเมนูช่วยเหลือ:</span><span class="sxs-lookup"><span data-stu-id="d5954-143">If the import still fails, let us know by clicking \*\*Community \*\*in the help menu:</span></span>
   
    ![ลิงก์ไปยังกลุ่มชุมชน](media/service-admin-troubleshoot-excel-workbook-data/power-bi-question-menu-community.png)
