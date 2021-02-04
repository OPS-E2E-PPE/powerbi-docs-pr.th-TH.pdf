---
title: 'บทช่วยสอน: รวมข้อมูลจาก Excel และตัวดึงข้อมูล OData ใน Power BI Desktop'
description: 'บทช่วยสอน: รวมข้อมูลจาก Excel และตัวดึงข้อมูล OData'
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: tutorial
ms.date: 01/17/2020
LocalizationGroup: Learn more
ms.openlocfilehash: 391c8fef1e95aa39ff6dfcd8aab8088f692504e7
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96404927"
---
# <a name="tutorial-analyze-sales-data-from-excel-and-an-odata-feed"></a><span data-ttu-id="2b8e8-103">บทช่วยสอน: วิเคราะห์ข้อมูลยอดขายจาก Excel และตัวดึงข้อมูล OData</span><span class="sxs-lookup"><span data-stu-id="2b8e8-103">Tutorial: Analyze sales data from Excel and an OData feed</span></span>

<span data-ttu-id="2b8e8-104">ซึ่งถือเป็นเรื่องปกติที่มีข้อมูลในแหล่งข้อมูลหลายแหล่ง</span><span class="sxs-lookup"><span data-stu-id="2b8e8-104">It's common to have data in multiple data sources.</span></span> <span data-ttu-id="2b8e8-105">ตัวอย่างเช่น คุณสามารถมีสองฐานข้อมูล ฐานข้อมูลหนึ่งสำหรับข้อมูลผลิตภัณฑ์ และอีกหนึ่งสำหรับข้อมูลการขาย</span><span class="sxs-lookup"><span data-stu-id="2b8e8-105">For example, you could have two databases, one for product information, and another for sales information.</span></span> <span data-ttu-id="2b8e8-106">ด้วย *Power BI Desktop* คุณสามารถรวมข้อมูลจากแหล่งข้อมูลที่แตกต่างกัน เพื่อสร้างการวิเคราะห์ข้อมูลและการแสดงภาพที่น่าสนใจ และน่าดึงดูดใจได้</span><span class="sxs-lookup"><span data-stu-id="2b8e8-106">With *Power BI Desktop*, you can combine data from different sources to create interesting, compelling data analyses and visualizations.</span></span>

<span data-ttu-id="2b8e8-107">ในบทช่วยสอนนี้ คุณสามารถรวมข้อมูลจากแหล่งข้อมูลสองแหล่ง:</span><span class="sxs-lookup"><span data-stu-id="2b8e8-107">In this tutorial, you combine data from two data sources:</span></span>

* <span data-ttu-id="2b8e8-108">สมุดงาน Excel ที่มีข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="2b8e8-108">An Excel workbook with product information</span></span>
* <span data-ttu-id="2b8e8-109">ตัวดึงข้อมูล OData ประกอบด้วยข้อมูลคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-109">An OData feed containing orders data</span></span>

<span data-ttu-id="2b8e8-110">คุณกำลังจะนำเข้าแต่ละชุดข้อมูล และดำเนินการแปลงและรวม</span><span class="sxs-lookup"><span data-stu-id="2b8e8-110">You're going to import each dataset and do transformation and aggregation operations.</span></span> <span data-ttu-id="2b8e8-111">จากนั้น คุณจะใช้ข้อมูลของสองแหล่งเพื่อสร้างรายงานการวิเคราะห์การขายพร้อมการแสดงภาพแบบโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-111">Then, you'll use the two source's data to produce a sales analysis report with interactive visualizations.</span></span> <span data-ttu-id="2b8e8-112">ต่อมา คุณสามารถใช้เทคนิคเหล่านี้กับคิวรี SQL Server ไฟล์ CSV และแหล่งข้อมูลอื่น ๆ ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2b8e8-112">Later, you can apply these techniques to SQL Server queries, CSV files, and other data sources in Power BI Desktop.</span></span>

>[!NOTE]
><span data-ttu-id="2b8e8-113">ใน Power BI Desktop งานหนึ่งงานมักทำได้หลายวิธี</span><span class="sxs-lookup"><span data-stu-id="2b8e8-113">In Power BI Desktop, there are often a few ways to accomplish a task.</span></span> <span data-ttu-id="2b8e8-114">ตัวอย่างเช่น คุณสามารถคลิกขวา หรือใช้เมนู **ตัวเลือกเพิ่มเติม** บนคอลัมน์หรือเซลล์เพื่อดูการเลือกริบบิ้นเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="2b8e8-114">For example, you can right-click or use a **More options** menu on a column or cell to see additional ribbon selections.</span></span> <span data-ttu-id="2b8e8-115">วิธีทางเลือกหลายวิธีจะอธิบายในขั้นตอนด้านล่างนี้</span><span class="sxs-lookup"><span data-stu-id="2b8e8-115">Several alternate methods are described in the steps below.</span></span>

## <a name="import-excel-product-data"></a><span data-ttu-id="2b8e8-116">นำเข้าข้อมูลผลิตภัณฑ์ Excel</span><span class="sxs-lookup"><span data-stu-id="2b8e8-116">Import Excel product data</span></span>

<span data-ttu-id="2b8e8-117">ก่อนอื่น นำเข้าข้อมูลผลิตภัณฑ์จากสมุดงาน Excel *Products.xlsx* ลงใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2b8e8-117">First, import product data from the *Products.xlsx* Excel workbook into Power BI Desktop.</span></span>

1. <span data-ttu-id="2b8e8-118">[ดาวน์โหลดเวิร์กบุ๊ก Excel Products.xlsx](https://download.microsoft.com/download/1/4/E/14EDED28-6C58-4055-A65C-23B4DA81C4DE/Products.xlsx) และบันทึกเป็น *Products.xlsx*</span><span class="sxs-lookup"><span data-stu-id="2b8e8-118">[Download the Products.xlsx Excel workbook](https://download.microsoft.com/download/1/4/E/14EDED28-6C58-4055-A65C-23B4DA81C4DE/Products.xlsx) and save it as *Products.xlsx*.</span></span>

1. <span data-ttu-id="2b8e8-119">เลือกลูกศรที่อยู่ถัดจาก **รับข้อมูล** ในแท็บ **หน้าแรก** ของริบบอน Power BI Desktop แล้วเลือก **Excel** จากเมนู **ส่วนใหญ่โดยทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-119">Select the arrow next to **Get Data** in the Power BI Desktop ribbon's **Home** tab, and then select **Excel** from the **Most Common** menu.</span></span>

   ![รับข้อมูล](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_1.png)

   >[!NOTE]
   ><span data-ttu-id="2b8e8-121">คุณยังสามารถเลือกรายการ **รับข้อมูล** โดยตรง หรือเลือก **รับข้อมูล** จากกล่องโต้ตอบ **การเริ่มต้นใช้งาน** Power BI แล้วเลือก **Excel** หรือ **ไฟล์** > **Excel** ในกล่องโต้ตอบ **รับข้อมูล** จากนั้นเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-121">You can also select the **Get Data** item itself, or select **Get Data** from the Power BI **Get started** dialog box, then select **Excel** or **File** > **Excel** in the **Get Data** dialog box, and then select **Connect**.</span></span>

1. <span data-ttu-id="2b8e8-122">ในกล่องโต้ตอบ **เปิด** นำทางไปยังและเลือกไฟล์ **Products.xlsx** แล้ว ลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-122">In the **Open** dialog box, navigate to and select the **Products.xlsx** file, and then select **Open**.</span></span>

1. <span data-ttu-id="2b8e8-123">ใน **ตัวนำทาง** ให้เลือกแบบตาราง **ผลิตภัณฑ์** จากนั้น เลือก **แปลงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-123">In the **Navigator**, select the **Products** table and then select **Transform Data**.</span></span>

   ![บานหน้าต่างตัวนำทางสำหรับ Excel](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_2.png)

<span data-ttu-id="2b8e8-125">การแสดงตัวอย่างของตารางเปิดขึ้นใน Power Query Editor ที่คุณสามารถใช้การแปลงเพื่อล้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2b8e8-125">A table preview opens in the Power Query Editor, where you can apply transformations to clean up the data.</span></span>

![ตัวแก้ไข Power Query](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_3.png)

>[!NOTE]
><span data-ttu-id="2b8e8-127">คุณยังสามารถเปิด Power Query Editor โดยการเลือก **แก้ไขคิวรี** > **แก้ไขคิวรี** จากริบบอน **หน้าแรก** ใน Power BI Desktop โดยคลิกขวา หรือเลือก **ตัวเลือกเพิ่มเติม** ถัดจากคิวรีใดก็ตามใน **มุมมองรายงาน** และเลือก **แก้ไขคิวรี**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-127">You can also open the Power Query Editor by selecting **Edit Queries** > **Edit Queries** from the **Home** ribbon in Power BI Desktop, or by right-clicking or choosing **More options** next to any query in the **Report** view, and selecting **Edit Query**.</span></span>

## <a name="clean-up-the-products-columns"></a><span data-ttu-id="2b8e8-128">ล้างคอลัมน์ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="2b8e8-128">Clean up the products columns</span></span>

<span data-ttu-id="2b8e8-129">รายงานรวมของคุณจะใช้คอลัมน์ **ProductID**, **ProductName**, **QuantityPerUnit** และ **UnitsInStock** จากเวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="2b8e8-129">Your combined report will use the Excel workbook's  **ProductID**, **ProductName**, **QuantityPerUnit**, and **UnitsInStock** columns.</span></span> <span data-ttu-id="2b8e8-130">คุณสามารถเอาคอลัมน์อื่น ๆ ออกได้</span><span class="sxs-lookup"><span data-stu-id="2b8e8-130">You can remove the other columns.</span></span>

1. <span data-ttu-id="2b8e8-131">ใน Power Query Editor ให้เลือกคอลัมน์ **ProductID**, **ProductName**, **QuantityPerUnit** และ **UnitsInStock**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-131">In Power Query Editor, select the **ProductID**, **ProductName**, **QuantityPerUnit**, and **UnitsInStock** columns.</span></span> <span data-ttu-id="2b8e8-132">คุณสามารถใช้ Ctrl เพื่อเลือกมากกว่าหนึ่งคอลัมน์ หรือ Shift เพื่อเลือกคอลัมน์ที่อยู่ติดกัน</span><span class="sxs-lookup"><span data-stu-id="2b8e8-132">You can use Ctrl to select more than one column, or Shift to select columns next to each other.</span></span>

1. <span data-ttu-id="2b8e8-133">คลิกขวาที่ส่วนหัวใด ๆ ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2b8e8-133">Right-click any of the selected headers.</span></span> <span data-ttu-id="2b8e8-134">เลือก **เอาคอลัมน์อื่นออก** จากเมนูแบบดรอปดาวน์</span><span class="sxs-lookup"><span data-stu-id="2b8e8-134">Select **Remove Other Columns** from the drop-down menu.</span></span>
   <span data-ttu-id="2b8e8-135">คุณยังสามารถเลือก **เอาคอลัมน์ออก** > **เอาคอลัมน์อื่นออก** จากในกลุ่ม **จัดการคอลัมน์** ในแท็บ ribbon **หน้าแรก**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-135">You can also select **Remove Columns** > **Remove Other Columns** from the **Manage Columns** group in the **Home** ribbon tab.</span></span>

   ![เอาคอลัมน์อื่นออก](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/analyzingsalesdata_removeothercolumns.png)

## <a name="import-the-odata-feeds-order-data"></a><span data-ttu-id="2b8e8-137">นำเข้าข้อมูลคำสั่งซื้อของตัวดึงข้อมูล OData</span><span class="sxs-lookup"><span data-stu-id="2b8e8-137">Import the OData feed's order data</span></span>

<span data-ttu-id="2b8e8-138">ถัดไป นำเข้าข้อมูลคำสั่งซื้อจากตัวดึงข้อมูล OData ตัวอย่างระบบการขายของ Northwind</span><span class="sxs-lookup"><span data-stu-id="2b8e8-138">Next, import the order data from the sample Northwind sales system OData feed.</span></span>

1. <span data-ttu-id="2b8e8-139">ใน Power Query Editor เลือก **แหล่งข้อมูลใหม่** แล้วจากรายการแบบดรอปดาวน์ **ส่วนใหญ่โดยทั่วไป** เลือก **ตัวดึงข้อมูล OData**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-139">In Power Query Editor, select **New Source** and then, from the **Most Common** menu, select **OData feed**.</span></span>

   ![รับ OData](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/get_odata.png)

1. <span data-ttu-id="2b8e8-141">ในกล่องโต้ตอบ **ตัวดึงข้อมูล OData** วาง URL ตัวดึงข้อมูล Northwind OData`https://services.odata.org/V3/Northwind/Northwind.svc/`</span><span class="sxs-lookup"><span data-stu-id="2b8e8-141">In the **OData feed** dialog box, paste the Northwind OData feed URL, `https://services.odata.org/V3/Northwind/Northwind.svc/`.</span></span> <span data-ttu-id="2b8e8-142">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-142">Select **OK**.</span></span>

   ![กล่องโต้ตอบตัวดึงข้อมูล OData](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/get_odata2.png)

1. <span data-ttu-id="2b8e8-144">ในบานหน้าต่าง **ตัวนำทาง** เลือกตาราง **Orders** จากนั้นเลือก **แปลงข้อมูล** เพื่อโหลดข้อมูลลงใน Power Query Editor</span><span class="sxs-lookup"><span data-stu-id="2b8e8-144">In **Navigator**, select the **Orders** table, and then select **Transform Data** to load the data into Power Query Editor.</span></span>

   ![ตัวนำทางสำหรับ OData](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/analyzingsalesdata_odatafeed.png)

   >[!NOTE]
   ><span data-ttu-id="2b8e8-146">ใน **ตัวนำทาง** คุณสามารถเลือกที่ชื่อตารางใด ๆ โดยต้องไม่เลือกกล่องกาเครื่องหมาย เพื่อดูตัวอย่างได้</span><span class="sxs-lookup"><span data-stu-id="2b8e8-146">In **Navigator**, you can select any table name, without selecting the checkbox, to see a preview.</span></span>

## <a name="expand-the-order-data"></a><span data-ttu-id="2b8e8-147">ขยายข้อมูลคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-147">Expand the order data</span></span>

<span data-ttu-id="2b8e8-148">คุณสามารถใช้การอ้างอิงตารางเพื่อสร้างคิวรีเมื่อเชื่อมต่อกับแหล่งข้อมูลที่มีหลายตารางได้ เช่น ฐานข้อมูลเชิงสัมพันธ์หรือตัวดึงข้อมูล Northwind OData</span><span class="sxs-lookup"><span data-stu-id="2b8e8-148">You can use table references to build queries when connecting to data sources with multiple tables, such as relational databases or the Northwind OData feed.</span></span> <span data-ttu-id="2b8e8-149">ตาราง **Orders** ประกอบด้วยการอ้างอิงไปยังตารางที่เกี่ยวข้องหลายตาราง</span><span class="sxs-lookup"><span data-stu-id="2b8e8-149">The **Orders** table contains references to several related tables.</span></span> <span data-ttu-id="2b8e8-150">คุณสามารถเพิ่มการดำเนินการขยายเพื่อเพิ่มคอลัมน์ **ProductID**, **UnitPrice** และ **Quantity** จากตาราง **Order_Details** ที่เกี่ยวข้องลงในตารางชื่อ (**Orders**)</span><span class="sxs-lookup"><span data-stu-id="2b8e8-150">You can use the expand operation to add the **ProductID**, **UnitPrice**, and **Quantity** columns from the related **Order_Details** table into the subject (**Orders**) table.</span></span>

1. <span data-ttu-id="2b8e8-151">เลื่อนไปทางขวาในตาราง **Orders** จนกว่าคุณจะเห็นคอลัมน์ **Order_Details**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-151">Scroll to the right in the **Orders** table until you see the **Order_Details** column.</span></span> <span data-ttu-id="2b8e8-152">คอลัมน์ประกอบด้วยการอ้างอิงไปยังตารางอื่นและไม่ใช่ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2b8e8-152">It contains references to another table and not data.</span></span>

   ![คอลัมน์ Order_Details](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/order-details-column.png)

1. <span data-ttu-id="2b8e8-154">เลือกไอคอน **ขยาย** (![ไอคอนขยาย](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/expand.png)) ในส่วนหัวของคอลัมน์ **Order_Details**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-154">Select the **Expand** icon (![Expand icon](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/expand.png)) in the **Order_Details** column header.</span></span>

1. <span data-ttu-id="2b8e8-155">ในเมนูดรอปดาวน์:</span><span class="sxs-lookup"><span data-stu-id="2b8e8-155">In the drop-down menu:</span></span>

   1. <span data-ttu-id="2b8e8-156">เลือก **(เลือกคอลัมน์ทั้งหมด)** เพื่อล้างคอลัมน์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2b8e8-156">Select **(Select All Columns)** to clear all columns.</span></span>

   1. <span data-ttu-id="2b8e8-157">เลือก **ProductID**, **UnitPrice** และ **Quantity** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-157">Select **ProductID**, **UnitPrice**, and **Quantity**, and then select **OK**.</span></span>

      ![ขยายเมนูดรอปดาวน์](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/expand-drop-down-menu.png)

<span data-ttu-id="2b8e8-159">หลังจากที่คุณขยายตาราง **Order_Details** คอลัมน์ตารางที่ซ้อนกันใหม่สามคอลัมน์จะแทนที่คอลัมน์ **Order_Details**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-159">After you expand the **Order_Details** table, three new nested table columns replace the **Order_Details** column.</span></span> <span data-ttu-id="2b8e8-160">มีแถวใหม่ในตารางสำหรับข้อมูลที่เพิ่มเติมของแต่ละคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-160">There are new rows in the table for each order's added data.</span></span>

![คอลัมน์ที่ขยายแล้ว](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/expanded-columns.png)

## <a name="create-a-custom-calculated-column"></a><span data-ttu-id="2b8e8-162">สร้างคอลัมน์จากการคำนวณแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="2b8e8-162">Create a custom calculated column</span></span>

<span data-ttu-id="2b8e8-163">ตัวแก้ไข Power Query ให้คุณสามารถสร้างการคำนวณและเขตข้อมูลแบบกำหนดเองเพื่อเติมแต่งข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-163">Power Query Editor lets you create calculations and custom fields to enrich your data.</span></span> <span data-ttu-id="2b8e8-164">คุณจะสร้างคอลัมน์แบบกำหนดเองที่คูณราคาต่อหน่วยกับปริมาณของรายการเพื่อคำนวณราคารวมสำหรับแต่ละรายการของคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-164">You'll create a custom column that multiplies the unit price by item quantity to calculate the total price for each order's line item.</span></span>

1. <span data-ttu-id="2b8e8-165">ในแท็บริบบิ้น **เพิ่มคอลัมน์** ของตัวแก้ไข Power Query เลือก **คอลัมน์แบบกำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-165">In the Power Query Editor's **Add Column** ribbon tab, select **Custom Column**.</span></span>

   ![การเพิ่มคอลัมน์แบบกำหนดเอง](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/adding-a-custom-column.png)

1. <span data-ttu-id="2b8e8-167">ในกล่องโต้ตอบ **คอลัมน์แบบกำหนดเอง** พิมพ์ **LineTotal** ในเขตข้อมูล **ชื่อคอลัมน์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-167">In the **Custom Column** dialog box, type **LineTotal** in the **New column name** field.</span></span>

1. <span data-ttu-id="2b8e8-168">ในเขตข้อมูล **สูตรคอลัมน์แบบกำหนดเอง** หลังจาก **=** ใส่ **[Order_Details.UnitPrice]** \* **[Order_Details.Quantity]**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-168">In the **Custom column formula** field after the **=**, enter **[Order_Details.UnitPrice]** \* **[Order_Details.Quantity]**.</span></span> <span data-ttu-id="2b8e8-169">คุณยังสามารถเลือกชื่อเขตข้อมูลจากกล่องเลื่อน **คอลัมน์ที่มีให้เลือกใช้งาน** และเลือก **<< แทรก** แทนที่จะพิมพ์ลงไป</span><span class="sxs-lookup"><span data-stu-id="2b8e8-169">You can also select the field names from the **Available columns** scroll box and select **<< Insert**, instead of typing them.</span></span>

1. <span data-ttu-id="2b8e8-170">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-170">Select **OK**.</span></span>

   ![กล่องโต้ตอบคอลัมน์แบบกำหนดเอง](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/custom-column-dialog-box.png)

   <span data-ttu-id="2b8e8-172">เขตข้อมูล **LineTotal** ใหม่จะปรากฏเป็นคอลัมน์สุดท้ายในตาราง **Orders**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-172">The new **LineTotal** field appears as the last column in the **Orders** table.</span></span>

## <a name="set-the-new-fields-data-type"></a><span data-ttu-id="2b8e8-173">ตั้งค่าชนิดข้อมูลสำหรับเขตข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="2b8e8-173">Set the new field's data type</span></span>

<span data-ttu-id="2b8e8-174">เมื่อตัวแก้ไข Power Query เชื่อมต่อกับข้อมูลจะสามารถคาดเดาได้ดีที่สุดว่าเป็นชนิดข้อมูลของแต่ละเขตข้อมูลสำหรับวัตถุประสงค์ในการแสดงผล</span><span class="sxs-lookup"><span data-stu-id="2b8e8-174">When Power Query Editor connects to data, it makes a best guess as to each field's data type for display purposes.</span></span> <span data-ttu-id="2b8e8-175">ไอคอนส่วนหัวระบุชนิดข้อมูลที่กำหนดของแต่ละเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2b8e8-175">A header icon indicates each field's assigned data type.</span></span> <span data-ttu-id="2b8e8-176">นอกจากนี้ คุณสามารถดูภายใต้ **ชนิดข้อมูล** ในกลุ่ม **แปลง** ของแท็บริบบิ้น **หน้าหลัก** ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="2b8e8-176">You can also look under **Data Type** in the **Home** ribbon tab's **Transform** group.</span></span>

<span data-ttu-id="2b8e8-177">คอลัมน์ **LineTotal** ใหม่ของคุณมีชนิดข้อมูล **ใด ๆ** แต่มีค่าสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="2b8e8-177">Your new **LineTotal** column has an **Any** data type, but it has currency values.</span></span> <span data-ttu-id="2b8e8-178">เพื่อกำหนดชนิดข้อมูล คลิกขวาที่ส่วนหัวของคอลัมน์ **LineTotal** เลือก **เปลี่ยนชนิดข้อมูล** จากเมนูแบบดรอปดาวน์ แล้วเลือก **จำนวนทศนิยมตายตัว**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-178">To assign a data type, right-click the **LineTotal** column header, select **Change Type** from the drop-down menu, and then select **Fixed decimal number**.</span></span>

![เปลี่ยนชนิดข้อมูลเป็นทศนิยมคงที่](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/change-data-type-to-fixed-decimal.png)

>[!NOTE]
><span data-ttu-id="2b8e8-180">คุณยังสามารถเลือกคอลัมน์ **LineTotal** แล้วเลือกลูกศรถัดจาก **ชนิดข้อมูล** ในพื้นที่ **แปลง** ของแท็บริบบอน **หน้าแรก** จากนั้นเลือก **จำนวนทศนิยมตายตัว**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-180">You can also select the **LineTotal** column, then select the arrow next to **Data Type** in the **Transform** area of the **Home** ribbon tab, and then select **Fixed decimal number**.</span></span>

## <a name="clean-up-the-orders-columns"></a><span data-ttu-id="2b8e8-181">ล้างคอลัมน์คำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-181">Clean up the orders columns</span></span>

<span data-ttu-id="2b8e8-182">เพื่อทำให้แบบจำลองของคุณง่ายต่อการทำงานในรายงาน คุณสามารถลบ เปลี่ยนชื่อ และเรียงลำดับคอลัมน์บางคอลัมน์ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="2b8e8-182">To make your model easier to work with in reports, you can delete, rename, and reorder some columns.</span></span>

<span data-ttu-id="2b8e8-183">รายงานของคุณจะใช้คอลัมน์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2b8e8-183">Your report is going to use the following columns:</span></span>

* <span data-ttu-id="2b8e8-184">**OrderDate**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-184">**OrderDate**</span></span>
* <span data-ttu-id="2b8e8-185">**ShipCity**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-185">**ShipCity**</span></span>
* <span data-ttu-id="2b8e8-186">**ShipCountry**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-186">**ShipCountry**</span></span>
* <span data-ttu-id="2b8e8-187">**Order_Details.ProductID**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-187">**Order_Details.ProductID**</span></span>
* <span data-ttu-id="2b8e8-188">**Order_Details.UnitPrice**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-188">**Order_Details.UnitPrice**</span></span>
* <span data-ttu-id="2b8e8-189">**Order_Details.Quantity**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-189">**Order_Details.Quantity**</span></span>
* <span data-ttu-id="2b8e8-190">**LineTotal**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-190">**LineTotal**</span></span>

<span data-ttu-id="2b8e8-191">เลือกคอลัมน์เหล่านี้ และใช้ **เอาคอลัมน์อื่นออก** เหมือนที่คุณดำเนินการกับข้อมูล Excel</span><span class="sxs-lookup"><span data-stu-id="2b8e8-191">Select these columns and use **Remove Other Columns** as you did with the Excel data.</span></span> <span data-ttu-id="2b8e8-192">หรือคุณสามารถเลือกคอลัมน์ที่ไม่ได้อยู่ในรายการ โดยคลิกขวาบนหนึ่งในคอลัมน์ แล้วเลือก **เอาคอลัมน์ออก** ได้</span><span class="sxs-lookup"><span data-stu-id="2b8e8-192">Or, you can select the non-listed columns, right-click on one of them, and select **Remove Columns**.</span></span>

<span data-ttu-id="2b8e8-193">คุณสามารถตั้งชื่อคอลัมน์ที่ขึ้นต้นด้วย "**Order_Details**" ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="2b8e8-193">You can rename the columns prefixed with "**Order_Details.**"</span></span> <span data-ttu-id="2b8e8-194">เพื่อให้อ่านได้ง่ายขึ้น:</span><span class="sxs-lookup"><span data-stu-id="2b8e8-194">to make them easier to read:</span></span>

1. <span data-ttu-id="2b8e8-195">ดับเบิลคลิก หรือแตะค้างไว้ที่ส่วนหัวของแต่ละคอลัมน์ หรือคลิกขวาที่ส่วนหัวของคอลัมน์ และเลือก **ตั้งชื่อใหม่** จากเมนูแบบดรอปดาวน์</span><span class="sxs-lookup"><span data-stu-id="2b8e8-195">Double-click or tap and hold each column header, or right-click the column header, and select **Rename** from the drop-down menu.</span></span>

1. <span data-ttu-id="2b8e8-196">ลบ **Order_Details.**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-196">Delete the **Order_Details.**</span></span> <span data-ttu-id="2b8e8-197">คำนำหน้าจากแต่ละชื่อ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-197">prefix from each name.</span></span>

<span data-ttu-id="2b8e8-198">สุดท้าย เพื่อทำให้คอลัมน์ **LineTotal** ง่ายต่อการเข้าถึง ลาก และวางลงไปด้านซ้าย ตรงด้านขวาของคอลัมน์ **ShipCountry**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-198">Finally, to make the **LineTotal** column easier to access, drag and drop it to the left, just to the right of the **ShipCountry** column.</span></span>

![ตารางที่ล้างข้อมูลแล้ว](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/cleaned-up-table.png)

## <a name="review-the-query-steps"></a><span data-ttu-id="2b8e8-200">ตรวจทานขั้นตอนคิวรี</span><span class="sxs-lookup"><span data-stu-id="2b8e8-200">Review the query steps</span></span>

<span data-ttu-id="2b8e8-201">จะมีการบันทึกแอคชันตัวแก้ไข Power Query เพื่อทำให้เป็นรูปแบบและแปลงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2b8e8-201">Your Power Query Editor actions to shape and transform data are recorded.</span></span> <span data-ttu-id="2b8e8-202">แต่ละแอคชันที่ปรากฏขึ้นทางด้านขวามือในบานหน้าต่าง **การตั้งค่าคิวรี** ภายใต้ **ขั้นตอนที่กำหนดใช้**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-202">Each action appears on the right in the **Query Settings** pane under **Applied Steps**.</span></span> <span data-ttu-id="2b8e8-203">คุณสามารถย้อนกลับผ่าน **ขั้นตอนที่กำหนดใช้** เพื่อตรวจสอบขั้นตอนของคุณ และแก้ไข ลบ หรือจัดเรียงใหม่ได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="2b8e8-203">You can step back through the **Applied Steps** to review your steps, and edit, delete, or rearrange them if necessary.</span></span> <span data-ttu-id="2b8e8-204">อย่างไรก็ตาม ขั้นตอนก่อนหน้าที่เปลี่ยนแปลงจะมีความเสี่ยงเนื่องจากสามารถทำให้ขั้นตอนลำดับถัดไปเสียหายได้</span><span class="sxs-lookup"><span data-stu-id="2b8e8-204">However, changing preceding steps is risky as that can break later steps.</span></span>

<span data-ttu-id="2b8e8-205">เลือกแต่ละคิวรีของคุณในรายการ **คิวรี** ทางด้านซ้ายของตัวแก้ไข Power Query และตรวจทาน **ขั้นตอนที่กำหนดใช้** ใน **การตั้งค่าแบบสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-205">Select each of your queries in the **Queries** list on the left side of Power Query Editor, and review the **Applied Steps** in **Query Settings**.</span></span> <span data-ttu-id="2b8e8-206">หลังจากที่นำการเปลี่ยนแปลงข้อมูลก่อนหน้าไปใช้ **ขั้นตอนที่กำหนดใช้กับคิวรีทั้ง** สองของคุณควรมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="2b8e8-206">After applying the previous data transformations, the **Applied Steps** for your two queries should look like this:</span></span>

![ขั้นตอนที่กำหนดใช้คิวรี Products](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/products-query-applied-steps.png) &nbsp;&nbsp; ![ขั้นตอนที่กำหนดใช้คิวรี Orders](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/orders-query-applied-steps.png)

>[!TIP]
><span data-ttu-id="2b8e8-209">ขั้นตอนที่กำหนดใช้โดยพื้นฐานแล้วเป็นสูตรที่เขียนใน *ภาษา Power Query* หรือที่เรียกว่า [ภาษา M](/powerquery-m/power-query-m-reference)</span><span class="sxs-lookup"><span data-stu-id="2b8e8-209">Underlying the Applied Steps are formulas written in the *Power Query Language*, also known as the [M language](/powerquery-m/power-query-m-reference).</span></span> <span data-ttu-id="2b8e8-210">เมื่อต้องการดูและแก้ไขสูตร เลือก **เครื่องมือแก้ไขขั้นสูง** ในกลุ่ม **คิวรี** ของแท็บ **หน้าแรก** ของริบบอน</span><span class="sxs-lookup"><span data-stu-id="2b8e8-210">To see and edit the formulas, select **Advanced Editor** in the **Query** group of the **Home** tab of the ribbon.</span></span>

## <a name="import-the-transformed-queries"></a><span data-ttu-id="2b8e8-211">นำเข้าคิวรีที่ถูกแปลง</span><span class="sxs-lookup"><span data-stu-id="2b8e8-211">Import the transformed queries</span></span>

<span data-ttu-id="2b8e8-212">เมื่อคุณพอใจกับข้อมูลของคุณที่ถูกแปลงแล้ว และพร้อมที่จะนำเข้าข้อมูลลงในมุมมอง **รายงาน** Power BI Desktop เลือก **ปิด & ใช้** > **ปิด & ใช้** ในกลุ่ม **ปิด** ของแท็บริบบอน **หน้าแรก**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-212">When you're satisfied with your transformed data and ready to import it into Power BI Desktop **Report** view, select **Close & Apply** > **Close & Apply** in the **Home** ribbon tab's **Close** group.</span></span>

![ปิดและนำไปใช้](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_4.png)

<span data-ttu-id="2b8e8-214">เมื่อข้อมูลถูกโหลดแล้ว คิวรีจะปรากฏในรายการ **เขตข้อมูล** ในมุมมอง **รายงาน** ของ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2b8e8-214">Once the data is loaded, the queries appear in the **Fields** list in the Power BI Desktop **Report** view.</span></span>

![คิวรีในรายการเขตข้อมูล](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/queries-in-fields-list.png)

## <a name="manage-the-relationship-between-the-datasets"></a><span data-ttu-id="2b8e8-216">จัดการความสัมพันธ์ระหว่างชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2b8e8-216">Manage the relationship between the datasets</span></span>

<span data-ttu-id="2b8e8-217">Power BI Desktop ไม่จำเป็นต้องเรียกร้องให้รวมคิวรี่เป็นรายงาน</span><span class="sxs-lookup"><span data-stu-id="2b8e8-217">Power BI Desktop doesn't require you to combine queries to report on them.</span></span> <span data-ttu-id="2b8e8-218">อย่างไรก็ตาม คุณสามารถใช้ความสัมพันธ์ระหว่างชุดข้อมูล ตามเขตข้อมูลที่มีร่วมกัน เพื่อขยายและเติมแต่งรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-218">However, you can use the relationships between datasets, based on common fields, to extend, and enrich your reports.</span></span> <span data-ttu-id="2b8e8-219">Power BI Desktop อาจตรวจพบความสัมพันธ์โดยอัตโนมัติ หรือคุณสามารถสร้างได้ในกล่องโต้ตอบ **จัดการความสัมพันธ์** ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2b8e8-219">Power BI Desktop may detect relationships automatically, or you can create them in the Power BI Desktop **Manage Relationships** dialog box.</span></span> <span data-ttu-id="2b8e8-220">สำหรับข้อมูลเพิ่มเติม ดู[สร้างและจัดการความสัมพันธ์ใน Power BI Desktop](../transform-model/desktop-create-and-manage-relationships.md)</span><span class="sxs-lookup"><span data-stu-id="2b8e8-220">For more information, see [Create and manage relationships in Power BI Desktop](../transform-model/desktop-create-and-manage-relationships.md).</span></span>

<span data-ttu-id="2b8e8-221">เขตข้อมูล `ProductID` ที่มีการแชร์จะสร้างความสัมพันธ์ระหว่างชุดข้อมูล `Orders` และ `Products` ของบทช่วยสอนนี้</span><span class="sxs-lookup"><span data-stu-id="2b8e8-221">The shared `ProductID` field creates a relationship between this tutorial's `Orders` and `Products` datasets.</span></span>

1. <span data-ttu-id="2b8e8-222">ในมุมมอง **รายงาน** Power BI Desktop เลือก **จัดการความสัมพันธ์** ในพื้นที่ **ความสัมพันธ์** ของแท็บริบบอน **หน้าแรก**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-222">In Power BI Desktop **Report** view, select **Manage Relationships** in the **Home** ribbon tab's **Relationships** area.</span></span>

   ![Ribbon จัดการความสัมพันธ์](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_5.png)

1. <span data-ttu-id="2b8e8-224">ในกล่องโต้ตอบ **จัดการความสัมพันธ์** คุณสามารถดูว่า Power BI Desktop ตรวจพบ และแสดงความสัมพันธ์ที่ใช้งานอยู่ระหว่างตาราง **Products** และ **Orders** อยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="2b8e8-224">In the **Manage relationships** dialog box, you can see that Power BI Desktop has already detected and listed an active relationship between the **Products** and **Orders** tables.</span></span> <span data-ttu-id="2b8e8-225">เพื่อดูความสัมพันธ์ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-225">To view the relationship, select **Edit**.</span></span>

   ![กล่องโต้ตอบจัดการความสัมพันธ์](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_6.png)

   <span data-ttu-id="2b8e8-227">**แก้ไขความสัมพันธ์** จะเปิดขึ้น ซึ่งแสดงรายละเอียดเกี่ยวกับความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="2b8e8-227">**Edit Relationship** opens, showing details about the relationship.</span></span>  

   ![กล่องโต้ตอบแก้ไขความสัมพันธ์](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_7.png)

1. <span data-ttu-id="2b8e8-229">Power BI Desktop มีการตรวจพบความสัมพันธ์ได้อย่างถูกต้องโดยอัตโนมัติ ดังนั้นคุณสามารถเลือก **ยกเลิก** แล้วเลือก **ปิด** ได้</span><span class="sxs-lookup"><span data-stu-id="2b8e8-229">Power BI Desktop has autodetected the relationship correctly, so you can select **Cancel** and then **Close**.</span></span>

<span data-ttu-id="2b8e8-230">ใน Power BI Desktop ทางด้านซ้ายมือ เลือก **แบบจำลอง** เพื่อดู และจัดการความสัมพันธ์คิวรี</span><span class="sxs-lookup"><span data-stu-id="2b8e8-230">In Power BI Desktop, on the left side, select **Model** to view and manage query relationships.</span></span> <span data-ttu-id="2b8e8-231">ดับเบิลคลิกที่ลูกศรบนเส้นที่เชื่อมต่อระหว่างสองคิวรีเพื่อเปิดกล่องโต้ตอบ **แก้ไขความสัมพันธ์** และดูหรือเปลี่ยนแปลงความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="2b8e8-231">Double-click the arrow on the line connecting the two queries to open the **Edit relationship** dialog and view or change the relationship.</span></span>

![มุมมองความสัมพันธ์](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_8.png)

<span data-ttu-id="2b8e8-233">เพื่อกลับไปยังมุมมอง **รายงาน** จากมุมมอง **แบบจำลอง** เลือกไอคอน **รายงาน**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-233">To get back to **Report** view from **Model** view, select the **Report** icon.</span></span>

![ไอคอนมุมมองรายงาน](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_9.png)

## <a name="create-visualizations-using-your-data"></a><span data-ttu-id="2b8e8-235">สร้างการแสดงภาพโดยใช้ข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-235">Create visualizations using your data</span></span>

<span data-ttu-id="2b8e8-236">คุณสามารถสร้างการแสดงภาพที่แตกต่างกันในมุมมองการตรวจสอบ Power BI Desktop เพื่อรับข้อมูลเชิงลึก</span><span class="sxs-lookup"><span data-stu-id="2b8e8-236">You can create different visualizations in Power BI Desktop Review View to gain data insights.</span></span> <span data-ttu-id="2b8e8-237">คุณสามารถมีหลายหน้า และแต่ละหน้าสามารถมีหลายวิชวล</span><span class="sxs-lookup"><span data-stu-id="2b8e8-237">Reports can have multiple pages, and each page can have multiple visuals.</span></span> <span data-ttu-id="2b8e8-238">คุณและผู้อื่นสามารถโต้ตอบกับการแสดงภาพของคุณ เพื่อช่วยวิเคราะห์ และทำความเข้าใจข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2b8e8-238">You and others can interact with your visualizations to help analyze and understand data.</span></span> <span data-ttu-id="2b8e8-239">สำหรับข้อมูลเพิ่มเติม ดู [โต้ตอบกับรายงานในมุมมองการแก้ไขในบริการ Power BI](../create-reports/service-interact-with-a-report-in-editing-view.md)</span><span class="sxs-lookup"><span data-stu-id="2b8e8-239">For more information, see [Interact with a report in Editing view in Power BI service](../create-reports/service-interact-with-a-report-in-editing-view.md).</span></span>

<span data-ttu-id="2b8e8-240">คุณสามารถใช้ทั้งสองชุดข้อมูลของคุณ และความสัมพันธ์ระหว่างกัน เพื่อช่วยให้มองเห็นภาพ และวิเคราะห์ข้อมูลยอดขายของคุณได้</span><span class="sxs-lookup"><span data-stu-id="2b8e8-240">You can use both of your data sets, and the relationship between them, to help visualize and analyze your sales data.</span></span>

<span data-ttu-id="2b8e8-241">ก่อนอื่น สร้างแผนภูมิคอลัมน์แบบเรียงซ้อนที่ใช้เขตข้อมูลจากทั้งสองคิวรี เพื่อแสดงปริมาณของแต่ละผลิตภัณฑ์ที่สั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-241">First, create a stacked column chart that uses fields from both queries to show the quantity of each product ordered.</span></span>

1. <span data-ttu-id="2b8e8-242">เลือกเขตข้อมูล **Quantity** จาก **Orders** ในบานหน้าต่าง **เขตข้อมูล** ด้านขวา หรือลากไปที่ว่างบนพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="2b8e8-242">Select the **Quantity** field from **Orders** in the **Fields** pane at the right, or drag it onto a blank space on the canvas.</span></span> <span data-ttu-id="2b8e8-243">จะมีการสร้างแผนภูมิคอลัมน์แบบเรียงซ้อน ที่แสดงจำนวนรวมของผลิตภัณฑ์ทั้งหมดที่สั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-243">A stacked column chart is created showing the total quantity of all products ordered.</span></span>

1. <span data-ttu-id="2b8e8-244">เลือก **ProductName** จาก **Products** ในบานหน้าต่าง **เขตข้อมูล** หรือลากลงบนแผนภูมิ เพื่อแสดงปริมาณของแต่ละผลิตภัณฑ์ที่สั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-244">To show the quantity of each product ordered, select **ProductName** from **Products** in the **Fields** pane, or drag it onto the chart.</span></span>

1. <span data-ttu-id="2b8e8-245">เลือก **ตัวเลือกเพิ่มเติม** ที่จุดไข่ปลา ( **...** ) ที่มุมบนขวาของการแสดงภาพ จากนั้นเลือก **เรียงลำดับตามปริมาณ** เพื่อเรียงลำดับผลิตภัณฑ์ ตามการสั่งซื้อมากที่สุดไปหาน้อยที่สุด</span><span class="sxs-lookup"><span data-stu-id="2b8e8-245">To sort the products by most to least ordered, select the **More options** ellipsis (**...**) at the visualization's upper right, and then select **Sort By Quantity**.</span></span>

1. <span data-ttu-id="2b8e8-246">ใช้จุดจับที่มุมของแผนภูมิเพื่อขยายให้มองเห็นชื่อผลิตภัณฑ์เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2b8e8-246">Use the handles at the corners of the chart to enlarge it so more product names are visible.</span></span>

   ![แผนภูมิแท่ง Quantity ตาม ProductName](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/quantity-by-productname-bar-chart.png)

<span data-ttu-id="2b8e8-248">ถัดไป สร้างแผนภูมิที่แสดงยอดเงินดอลลาร์ของคำสั่งซื้อ (**LineTotal**) ตามเวลา (**OrderDate**)</span><span class="sxs-lookup"><span data-stu-id="2b8e8-248">Next, create a chart showing order dollar amounts (**LineTotal**) over time (**OrderDate**).</span></span>

1. <span data-ttu-id="2b8e8-249">โดยไม่ได้เลือกอะไรบนพื้นที่ทำงาน เลือก **LineTotal** จาก **Orders** ในบานหน้าต่าง **เขตข้อมูล** หรือลากไปยังที่ว่างบนพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="2b8e8-249">With nothing selected on the canvas, select **LineTotal** from **Orders** in the **Fields** pane, or drag it to a blank space on the canvas.</span></span> <span data-ttu-id="2b8e8-250">แผนภูมิคอลัมน์แบบเรียงซ้อน จะแสดงยอดเงินดอลลาร์ทั้งหมดของทุกคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-250">The stacked column chart shows the total dollar amount of all orders.</span></span>

1. <span data-ttu-id="2b8e8-251">เลือกแผนภูมิแบบเรียงซ้อน แล้วจึงเลือก **OrderDate** จาก **Orders** หรือลากไปที่แผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-251">Select the stacked chart, then select **OrderDate** from **Orders**, or drag it onto the chart.</span></span> <span data-ttu-id="2b8e8-252">แผนภูมิตอนนี้แสดงเส้น ผลรวมรายการสำหรับแต่ละวันสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-252">The chart now shows line totals for each order date.</span></span>

1. <span data-ttu-id="2b8e8-253">ลากจุดจับมุมเพื่อปรับขนาดการแสดงภาพ และดูข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2b8e8-253">Drag the corners to resize the visualization and see more data.</span></span>

   ![แผนภูมิเส้น LineTotals ตาม OrderDate](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/linetotals-by-orderdate-line-chart.png)

   >[!TIP]
   ><span data-ttu-id="2b8e8-255">ถ้าคุณเห็นแต่ **Years** เท่านั้นบนแผนภูมิ (มีเพียง 3 จุดข้อมูล) ดรอปดาวน์กลูกศรที่อยู่ถัดจาก **OrderDate** ในเขตข้อมูล **แกน** ของบานหน้าต่าง **การแสดงผลข้อมูลด้วยภาพ** และเลือก **OrderDate** แทน **Date Hierarchy**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-255">If you only see **Years** on the chart and only three data points, select the arrow next to **OrderDate** in the **Axis** field of the **Visualizations** pane, and select **OrderDate** instead of **Date Hierarchy**.</span></span>

<span data-ttu-id="2b8e8-256">สุดท้าย สร้างการแสดงภาพแผนที่ ที่แสดงยอดเงินสั่งซื้อจากแต่ละประเทศ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-256">Finally, create a map visualization showing order amounts from each country.</span></span>

1. <span data-ttu-id="2b8e8-257">โดยไม่ได้เลือกอะไรบนพื้นที่ทำงาน เลือก **ShipCountry** จาก **Orders** ในบานหน้าต่าง **เขตข้อมูล** หรือลากไปยังที่ว่างบนพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="2b8e8-257">With nothing selected on the canvas, select **ShipCountry** from **Orders** in the **Fields** pane, or drag it to a blank space on the canvas.</span></span> <span data-ttu-id="2b8e8-258">Power BI Desktop ตรวจพบว่า ข้อมูลเป็นชื่อประเทศ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-258">Power BI Desktop detects that the data is country names.</span></span> <span data-ttu-id="2b8e8-259">จากนั้นจะสร้างการแสดงภาพแผนที่โดยอัตโนมัติ พร้อมจุดข้อมูลสำหรับแต่ละประเทศที่มีคำสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-259">It then automatically creates a map visualization, with a data point for each country with orders.</span></span>

1. <span data-ttu-id="2b8e8-260">เมื่อต้องการทำให้ขนาดจุดข้อมูลแสดงจำนวนการสั่งซื้อของแต่ละประเทศ ลากเขตข้อมูล **LineTotal** ลงบนแผนที่</span><span class="sxs-lookup"><span data-stu-id="2b8e8-260">To make the data point sizes reflect each country's order amounts, drag the **LineTotal** field onto the map.</span></span> <span data-ttu-id="2b8e8-261">นอกจากนี้ คุณยังสามารถลากไปที่ **ลากเขตข้อมูลที่นี่** ภายใต้ **ขนาด** ในบานหน้าต่าง **การแสดงภาพ** ได้</span><span class="sxs-lookup"><span data-stu-id="2b8e8-261">You can also drag it to **Drag data fields here** under **Size** in the **Visualizations** pane.</span></span> <span data-ttu-id="2b8e8-262">ขนาดของวงกลมบนแผนที่ ตอนนี้จะสะท้อนถึงยอดเงินดอลลาร์ของคำสั่งซื้อจากแต่ละประเทศ</span><span class="sxs-lookup"><span data-stu-id="2b8e8-262">The sizes of the circles on the map now reflect the dollar amounts of the orders from each country.</span></span>

   ![การแสดงภาพของแผนที่ LineTotals ตาม ShipCountry](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/linetotals-by-shipcountry-map-visualization.png)

## <a name="interact-with-your-report-visuals-to-analyze-further"></a><span data-ttu-id="2b8e8-264">โต้ตอบกับวิชวลในรายงานของคุณเพื่อวิเคราะห์เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2b8e8-264">Interact with your report visuals to analyze further</span></span>

<span data-ttu-id="2b8e8-265">ใน Power BI Desktop คุณสามารถโต้ตอบกับรูปภาพที่ไฮไลท์สลับกัน และกรองซึ่งกันและกัน เมื่อต้องการเปิดเผยแนวโน้มที่เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2b8e8-265">In Power BI Desktop, you can interact with visuals that cross-highlight and filter each other to uncover further trends.</span></span> <span data-ttu-id="2b8e8-266">สำหรับข้อมูลเพิ่มเติม ดู[การกรอง และการไฮไลต์ในรายงาน Power BI](../create-reports/power-bi-reports-filters-and-highlighting.md)</span><span class="sxs-lookup"><span data-stu-id="2b8e8-266">For more information, see [Filters and highlighting in Power BI reports](../create-reports/power-bi-reports-filters-and-highlighting.md).</span></span>

<span data-ttu-id="2b8e8-267">เนื่องจากความสัมพันธ์ระหว่างคิวรีของคุณ การโต้ตอบกับการแสดงภาพหนึ่งภาพมีผลต่อการแสดงภาพอื่น ๆ ทั้งหมดบนหน้า</span><span class="sxs-lookup"><span data-stu-id="2b8e8-267">Because of the relationship between your queries, interactions with one visualization affect all the other visualizations on the page.</span></span>

<span data-ttu-id="2b8e8-268">ในการแสดงภาพแผนที่ เลือกวงกลมที่ศูนย์กลางอยู่ใน **แคนาดา**</span><span class="sxs-lookup"><span data-stu-id="2b8e8-268">On the map visualization, select the circle centered in **Canada**.</span></span> <span data-ttu-id="2b8e8-269">การแสดงภาพอีกสองภาพ จะกรองเพื่อไฮไลต์เส้นผลรวม และปริมาณคำสั่งซื้อสำหรับแค่แคนาดา</span><span class="sxs-lookup"><span data-stu-id="2b8e8-269">The other two visualizations filter to highlight the Canadian line totals and order quantities.</span></span>

![ข้อมูลยอดขายที่ถูกกรองสำหรับแคนาดา](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/sales-data-filtered-for-canada.png)

<span data-ttu-id="2b8e8-271">เลือกผลิตภัณฑ์แผนภูมิ **Quantity by ProductName** เพื่อดูแผนที่และตัวกรองแผนภูมิวันที่เพื่อสะท้อนถึงข้อมูลของผลิตภัณฑ์นั้น</span><span class="sxs-lookup"><span data-stu-id="2b8e8-271">Select a **Quantity by ProductName** chart product to see the map and the date chart filter to reflect that product's data.</span></span> <span data-ttu-id="2b8e8-272">เลือกวันที่ของแผนภูมิ **LineTotal by OrderDate** เพื่อดูแผนที่และตัวกรองแผนภูมิผลิตภัณฑ์เพื่อแสดงข้อมูลของวันที่ของแผนภูมินั้น</span><span class="sxs-lookup"><span data-stu-id="2b8e8-272">Select a **LineTotal by OrderDate** chart date to see the map and the product chart filter to show that date's data.</span></span>

>[!TIP]
><span data-ttu-id="2b8e8-273">เพื่อยกเลิกการเลือก เลือกอีกครั้ง หรือเลือกการแสดงภาพอื่น</span><span class="sxs-lookup"><span data-stu-id="2b8e8-273">To deselect a selection, select it again, or select one of the other visualizations.</span></span>

## <a name="complete-the-sales-analysis-report"></a><span data-ttu-id="2b8e8-274">รายงานการวิเคราะห์การขายที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="2b8e8-274">Complete the sales analysis report</span></span>

<span data-ttu-id="2b8e8-275">รายงานที่เสร็จสมบูรณ์ของคุณได้รวมข้อมูลจากไฟล์ Excel *Products.xlsx* และตัวดึงข้อมูล OData ของ Northwind ในวิชวลเพื่อช่วยคุณวิเคราะห์ข้อมูลคำสั่งซื้อสำหรับประเทศ กรอบเวลา และผลิตภัณฑ์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="2b8e8-275">Your completed report combines data from the *Products.xlsx* Excel file and the Northwind OData feed in visuals that help you analyze different countries' order information, time frames, and products.</span></span> <span data-ttu-id="2b8e8-276">เมื่อรายงานของคุณพร้อมแล้ว คุณสามารถ[อัปโหลดไปยังบริการของ Power BI](../create-reports/desktop-upload-desktop-files.md) เพื่อแชร์ให้กับผู้ใช้ Power BI อื่นได้</span><span class="sxs-lookup"><span data-stu-id="2b8e8-276">When your report is ready, you can [upload it to Power BI service](../create-reports/desktop-upload-desktop-files.md) to share it with other Power BI users.</span></span>

## <a name="next-steps"></a><span data-ttu-id="2b8e8-277">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="2b8e8-277">Next steps</span></span>

* [<span data-ttu-id="2b8e8-278">Microsoft Learn สำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="2b8e8-278">Microsoft Learn for Power BI</span></span>](/learn/powerplatform/power-bi?WT.mc_id=powerbi_landingpage-docs-link)
* [<span data-ttu-id="2b8e8-279">ดูวิดีโอ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2b8e8-279">Watch Power BI Desktop videos</span></span>](../fundamentals/desktop-videos.md)
* [<span data-ttu-id="2b8e8-280">เยี่ยมชมกระดานสนทนา Power BI</span><span class="sxs-lookup"><span data-stu-id="2b8e8-280">Visit the Power BI Forum</span></span>](https://go.microsoft.com/fwlink/?LinkID=519326)
* [<span data-ttu-id="2b8e8-281">อ่านบล็อก Power BI</span><span class="sxs-lookup"><span data-stu-id="2b8e8-281">Read the Power BI Blog</span></span>](https://go.microsoft.com/fwlink/?LinkID=519327)