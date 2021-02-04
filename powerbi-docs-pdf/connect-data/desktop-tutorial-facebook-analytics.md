---
title: 'บทช่วยสอน: วิเคราะห์ข้อมูล Facebook โดยใช้ Power BI Desktop'
description: เรียนรู้วิธีการนำเข้าข้อมูลจาก Facebook และใช้ใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: tutorial
ms.date: 05/06/2020
LocalizationGroup: Learn more
ms.openlocfilehash: c138b5d3b03b360ee1f83c57a98906b5fec25d6e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410976"
---
# <a name="tutorial-analyze-facebook-data-by-using-power-bi-desktop"></a><span data-ttu-id="ae49d-103">บทช่วยสอน: วิเคราะห์ข้อมูล Facebook โดยใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ae49d-103">Tutorial: Analyze Facebook data by using Power BI Desktop</span></span>

<span data-ttu-id="ae49d-104">ในบทช่วยสอนนี้ คุณจะเรียนรู้วิธีการนำเข้าข้อมูลจาก Facebook และใช้ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ae49d-104">In this tutorial, you learn how to import data from Facebook and use it in Power BI Desktop.</span></span> <span data-ttu-id="ae49d-105">คุณจะเชื่อมต่อและนำเข้าข้อมูลจากหน้า Facebook ของ Power BI ทำการแปลงข้อมูลนำเข้า และใช้ข้อมูลในการแสดงภาพรายงาน</span><span class="sxs-lookup"><span data-stu-id="ae49d-105">You'll connect and import data from the Power BI Facebook page, apply transformations to the imported data, and use the data in report visualizations.</span></span>

> [!WARNING]
> <span data-ttu-id="ae49d-106">เนื่องจากข้อจำกัดสิทธิ์ของแอป Facebook ความสามารถในการเชื่อมต่อที่อธิบายไว้ในบทความนี้ไม่ได้ทำงานอย่างถูกต้องในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="ae49d-106">Due to Facebook App permission restrictions, the connector capabilities described in this article are not currently working properly.</span></span> <span data-ttu-id="ae49d-107">เรากำลังทำงานกับ Facebook เพื่อทำให้ฟังก์ชันการทำงานนี้สามารถใช้ได้โดยเร็วที่สุดเท่าที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="ae49d-107">We’re working with Facebook to return this functionality as soon as possible.</span></span>


## <a name="connect-to-a-facebook-page"></a><span data-ttu-id="ae49d-108">เชื่อมต่อไปยังหน้า Facebook</span><span class="sxs-lookup"><span data-stu-id="ae49d-108">Connect to a Facebook page</span></span>

<span data-ttu-id="ae49d-109">บทช่วยสอนนี้ใช้ข้อมูลจาก[หน้า Facebook ของ Microsoft Power BI](https://www.facebook.com/microsoftbi)</span><span class="sxs-lookup"><span data-stu-id="ae49d-109">This tutorial uses data from the [Microsoft Power BI Facebook page](https://www.facebook.com/microsoftbi).</span></span> <span data-ttu-id="ae49d-110">คุณไม่จำเป็นใช้ข้อมูลประจำตัวใด ๆ เป็นพิเศษเพื่อเชื่อมต่อ และนำเข้าข้อมูลจากหน้านี้ ยกเว้นบัญชี Facebook ส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="ae49d-110">You don't need any special credentials to connect and import data from this page except for a personal Facebook account.</span></span>

1. <span data-ttu-id="ae49d-111">เปิด Power BI Desktop แล้วเลือก **รับข้อมูล** ในกล่องโต้ตอบ **เริ่มต้นใช้งาน** หรือในแท็บริบบิ้น **หน้าแรก** เลือก **รับข้อมูล** แล้วเลือก **เพิ่มเติม**</span><span class="sxs-lookup"><span data-stu-id="ae49d-111">Open Power BI Desktop and select **Get data** in the **Getting Started** dialog box, or in the **Home** ribbon tab, select **Get Data** and then select **More**.</span></span>
   
2. <span data-ttu-id="ae49d-112">ในกล่องโต้ตอบ **รับข้อมูล** เลือก **Facebook** จากกลุ่ม **บริการออนไลน์** จากนั้นเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="ae49d-112">In the **Get Data** dialog box, select **Facebook** from the **Online Services** group, and then select **Connect**.</span></span>
   
   ![รับข้อมูล](media/desktop-tutorial-facebook-analytics/t_fb_getdataother.png)
   
   <span data-ttu-id="ae49d-114">กล่องโต้ตอบจะปรากฏเพื่อแจ้งเตือนคุณว่า มีความเสี่ยงจากการใช้บริการของบริษัทอื่น</span><span class="sxs-lookup"><span data-stu-id="ae49d-114">A dialog box appears to alert you to the risks of using a third-party service.</span></span>
   
   ![คำเตือนเกี่ยวกับบุคคลที่สาม](media/desktop-tutorial-facebook-analytics/t_fb_connectingtotps.png)
   
3. <span data-ttu-id="ae49d-116">เลือก **ดำเนินต่อ**</span><span class="sxs-lookup"><span data-stu-id="ae49d-116">Select **Continue**.</span></span> 
   
4. <span data-ttu-id="ae49d-117">ในกล่องโต้ตอบ **Facebook** ให้ป้อนชื่อหน้า **microsoftbi** เป็น **ชื่อผู้ใช้** เลือก **โพสต์** จากดรอปดาวน์ **การเชื่อมต่อ** จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ae49d-117">In the **Facebook** dialog box, enter the page name **microsoftbi** as the **user name**, select **Posts** from the **Connection** dropdown, and then select **OK**.</span></span>
   
   ![เชื่อมต่อ](media/desktop-tutorial-facebook-analytics/2.png)
   
5. <span data-ttu-id="ae49d-119">เมื่อได้รับพร้อมท์สำหรับข้อมูลประจำตัว ให้ลงชื่อเข้าใช้บัญชีผู้ใช้ Facebook ของคุณ และอนุญาตให้ Power BI เข้าถึงบัญชีของคุณ</span><span class="sxs-lookup"><span data-stu-id="ae49d-119">When prompted for credentials, sign in to your Facebook account, and allow Power BI access to your account.</span></span>
   
   ![ข้อมูลประจำตัว](media/desktop-tutorial-facebook-analytics/facebookcredentials.png)

   <span data-ttu-id="ae49d-121">หลังจากเชื่อมต่อไปยังหน้า Facebook ของ Power BI แล้ว คุณจะเห็นตัวอย่างของข้อมูลการโพสต์ของหน้าเพจ</span><span class="sxs-lookup"><span data-stu-id="ae49d-121">After you connect to the Power BI Facebook page, you see a preview of the page's posts data.</span></span> 
   
   ![แสดงตัวอย่างข้อมูล](media/desktop-tutorial-facebook-analytics/t_fb_1-loadpreview.png)
   
## <a name="shape-and-transform-the-imported-data"></a><span data-ttu-id="ae49d-123">จัดรูปทรง และแปลงข้อมูลนำเข้า</span><span class="sxs-lookup"><span data-stu-id="ae49d-123">Shape and transform the imported data</span></span>

<span data-ttu-id="ae49d-124">สมมติว่าคุณต้องการเห็นและแสดงว่า โพสต์ไหนมีจำนวนความคิดเห็นมากที่สุดในแต่ละเวลา แต่คุณสังเกตเห็นในตัวอย่างข้อมูลการโพสต์ว่าข้อมูล **created_time** อ่านและเข้าใจยาก และขาดข้อมูลความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="ae49d-124">Suppose you want to see and show which posts have the most comments over time, but you notice in the posts data preview that the **created_time** data is hard to read and understand, and there's a lack of comments data.</span></span> <span data-ttu-id="ae49d-125">เมื่อต้องการดึงข้อมูลออกมาให้มากที่สุด คุณจำเป็นต้องดำเนินการจัดรูปทรง และทำความสะอาดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ae49d-125">To pull the most out of it, perform some shaping and cleansing of the data.</span></span> <span data-ttu-id="ae49d-126">หากต้องการทำเช่นนั้น คุณสามารถใช้ตัวแก้ไข Power Queryใน Power BI Desktop เพื่อแก้ไขข้อมูล ก่อนหรือหลังการนำเข้าใน Power BI Desktop ได้</span><span class="sxs-lookup"><span data-stu-id="ae49d-126">To do so, use the Power BI Desktop Power Query Editor to edit the data, before or after importing it into Power BI Desktop.</span></span> 

### <a name="split-the-datetime-column"></a><span data-ttu-id="ae49d-127">แยกคอลัมน์ วันที่/เวลา</span><span class="sxs-lookup"><span data-stu-id="ae49d-127">Split the date/time column</span></span>

<span data-ttu-id="ae49d-128">ก่อนอื่น แยกค่าวันที่และเวลาในคอลัมน์ **created_time** เพื่อให้อ่านได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="ae49d-128">First, separate the date and time values in the **created_time** column to be more readable.</span></span> 

1. <span data-ttu-id="ae49d-129">ในตัวอย่างข้อมูล Facebook เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="ae49d-129">In the Facebook data preview, select **Edit**.</span></span> 
   
   ![แก้ไขตัวอย่างข้อมูล](media/desktop-tutorial-facebook-analytics/t_fb_1-editpreview.png)
   
   <span data-ttu-id="ae49d-131">ตัวแก้ไข Power Query ของ Power BI Desktop จะเปิดหน้าต่างใหม่ และแสดงตัวอย่างข้อมูลจากหน้า Facebook ของ Power BI</span><span class="sxs-lookup"><span data-stu-id="ae49d-131">The Power BI Desktop Power Query Editor opens in a new window and displays the data preview from the Power BI Facebook page.</span></span> 
   
   ![ตัวแก้ไข Power Query](media/desktop-tutorial-facebook-analytics/t_fb_1-intoqueryeditor.png)
   
2. <span data-ttu-id="ae49d-133">เลือกคอลัมน์ **created_time**</span><span class="sxs-lookup"><span data-stu-id="ae49d-133">Select the **created_time** column.</span></span> <span data-ttu-id="ae49d-134">โปรดสังเกตว่า คอลัมน์เป็นข้อมูลชนิด **ข้อความ** ตามที่แสดงโดยไอคอน **ABC** ในส่วนหัวของคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="ae49d-134">Notice that it's a **Text** data type, as denoted by an **ABC** icon in the column header.</span></span> <span data-ttu-id="ae49d-135">คลิกขวาที่ส่วนหัวและเลือก **แยกคอลัมน์** > **โดยตัวคั่น** ในรายการดรอปดาวน์</span><span class="sxs-lookup"><span data-stu-id="ae49d-135">Right-click the header and select **Split Column** > **By Delimiter** in the drop-down list.</span></span> <span data-ttu-id="ae49d-136">หรือเลือก **แยกคอลัมน์** > **โดยตัวคั่น** ภายใต้กลุ่ม **แปลง** ในแท็บ **หน้าแรก** ของริบบิ้น</span><span class="sxs-lookup"><span data-stu-id="ae49d-136">Or, select **Split Column** > **By Delimiter** under the **Transform** group in the **Home** tab of the ribbon.</span></span>  
   
   ![แบ่งคอลัมน์ตามตัวคั่น](media/desktop-tutorial-facebook-analytics/delimiter1.png)
   
3. <span data-ttu-id="ae49d-138">ในกล่องโต้ตอบ **แยกคอลัมน์ตามตัวคั่น** ให้เลือก **แบบกำหนดเอง** จากดรอปดาวน์ ใส่ **T** (ตัวอักษรที่เริ่มต้นส่วนเวลาของ **created_time**) ในเขตข้อมูลอินพุต และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ae49d-138">In the **Split Column by Delimiter** dialog box, select **Custom** from the dropdown, enter **T** (the character that starts the time part of the **created_time** values) in the input field, and then select **OK**.</span></span> 
   
   ![กล่องโต้ตอบแยกคอลัมน์ตามตัวคั่น](media/desktop-tutorial-facebook-analytics/delimiter2.png)
   
   <span data-ttu-id="ae49d-140">คอลัมน์จะแบ่งออกเป็นสองคอลัมน์ที่ประกอบด้วย สตริงก่อนและหลังตัวคั่น *T*</span><span class="sxs-lookup"><span data-stu-id="ae49d-140">The column splits into two columns that contain the strings before and after the *T* delimiter.</span></span> <span data-ttu-id="ae49d-141">คอลัมน์ใหม่มีชื่อว่า **created_time .1** และ **created_time 2** ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="ae49d-141">The new columns are named **created_time.1** and **created_time.2**, respectively.</span></span> <span data-ttu-id="ae49d-142">Power BI ตรวจสอบและเปลี่ยนชนิดข้อมูลเป็น **Date** สำหรับคอลัมน์แรก และ **Time** สำหรับคอลัมน์สองโดยอัตโนมัติ และจัดรูปแบบค่าวันที่และเวลาเพื่อให้อ่านง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="ae49d-142">Power BI has automatically detected and changed the data types to **Date** for the first column and **Time** for the second column, and formatted the date and time values to be more readable.</span></span>
   
4. <span data-ttu-id="ae49d-143">เปลี่ยนชื่อสองคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="ae49d-143">Rename the two columns.</span></span> <span data-ttu-id="ae49d-144">เลือกคอลัมน์ **created_time.1** จากนั้นเลือก **เปลี่ยนชื่อ** ในกลุ่ม **คอลัมน์ใดก็ได้** ของแท็บ **แปลง** ในริบบิ้น</span><span class="sxs-lookup"><span data-stu-id="ae49d-144">Select the **created_time.1** column, and then select **Rename** in the **Any Column** group of the **Transform** tab in the ribbon.</span></span> <span data-ttu-id="ae49d-145">หรือดับเบิลคลิกที่ส่วนหัวของคอลัมน์แล้วป้อนชื่อคอลัมน์ใหม่เป็น **created_date**</span><span class="sxs-lookup"><span data-stu-id="ae49d-145">Or, double-click the column header and enter the new column name, **created_date**.</span></span> <span data-ttu-id="ae49d-146">ทำซ้ำสำหรับคอลัมน์ **created_time .2** และเปลี่ยนชื่อเป็น **created_time**</span><span class="sxs-lookup"><span data-stu-id="ae49d-146">Repeat for the **created_time.2** column, and rename it **created_time**.</span></span>
   
   ![คอลัมน์วันที่และเวลาใหม่](media/desktop-tutorial-facebook-analytics/delimiter3.png)
   
### <a name="expand-the-nested-column"></a><span data-ttu-id="ae49d-148">ขยายคอลัมน์ซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="ae49d-148">Expand the nested column</span></span>

<span data-ttu-id="ae49d-149">ตอนนี้ข้อมูลวันที่และเวลาอยู่ในรูปแบบที่คุณต้องการแล้ว คุณสามารถเปิดเผยข้อมูลความคิดเห็นโดยการขยายคอลัมน์ที่ซ้อนกันได้</span><span class="sxs-lookup"><span data-stu-id="ae49d-149">Now that the date and time data are as you want them, you can expose comments data by expanding a nested column.</span></span> 

1. <span data-ttu-id="ae49d-150">เลือกไอคอน ![ขยายไอคอน](media/desktop-tutorial-facebook-analytics/14.png) ที่ด้านบนของคอลัมน์ **object_link** เพื่อเปิดกล่องโต้ตอบ **ขยาย/รวม**</span><span class="sxs-lookup"><span data-stu-id="ae49d-150">Select the ![expand icon](media/desktop-tutorial-facebook-analytics/14.png) icon at the top of the **object_link** column to open the **Expand/Aggregate** dialog box.</span></span> <span data-ttu-id="ae49d-151">เลือก **connections** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ae49d-151">Select **connections**, and then select **OK**.</span></span> 
   
   ![ขยาย object_link](media/desktop-tutorial-facebook-analytics/expand1.png)
   
   <span data-ttu-id="ae49d-153">ส่วนหัวของคอลัมน์เปลี่ยนไปเป็น **object_link.connections**</span><span class="sxs-lookup"><span data-stu-id="ae49d-153">The column heading changes to **object_link.connections**.</span></span>
2. <span data-ttu-id="ae49d-154">เลือกไอคอน ![ขยายไอคอน](media/desktop-tutorial-facebook-analytics/14.png) ที่ด้านบนของคอลัมน์ **object_link.connections** เลือก **ความคิดเห็น** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ae49d-154">Select the ![expand icon](media/desktop-tutorial-facebook-analytics/14.png) icon at the top of the **object_link.connections** column, select **comments**, and then select **OK**.</span></span> <span data-ttu-id="ae49d-155">ส่วนหัวของคอลัมน์เปลี่ยนไปเป็น **object_link.connections.comments**</span><span class="sxs-lookup"><span data-stu-id="ae49d-155">The column heading changes to **object_link.connections.comments**.</span></span>
   
3. <span data-ttu-id="ae49d-156">เลือกไอคอน ![ขยายไอคอน](media/desktop-tutorial-facebook-analytics/14.png) ที่ด้านบนของคอลัมน์ **object_link.connections.comments** และตอนนี้เลือก **รวม** แทนที่จะเป็น **ขยาย** ในกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="ae49d-156">Select the ![expand icon](media/desktop-tutorial-facebook-analytics/14.png) icon at the top of the **object_link.connections.comments** column, and this time select **Aggregate** instead of **Expand** in the dialog box.</span></span> <span data-ttu-id="ae49d-157">เลือก **จำนวนของ id** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ae49d-157">Select **# Count of id**, and then select **OK**.</span></span> 
   
   ![รวมความคิดเห็น](media/desktop-tutorial-facebook-analytics/expand2.png)
   
   <span data-ttu-id="ae49d-159">ตอนนี้คอลัมน์แสดงจำนวนความคิดเห็นของแต่ละข้อความแล้ว</span><span class="sxs-lookup"><span data-stu-id="ae49d-159">The column now displays the number of comments for each message.</span></span> 
   
4. <span data-ttu-id="ae49d-160">เปลี่ยนชื่อคอลัมน์ **จำนวนของ object_link.connections.comments.id** เป็น **Number of comments**</span><span class="sxs-lookup"><span data-stu-id="ae49d-160">Rename the **Count of object_link.connections.comments.id** column to **Number of comments**.</span></span>
   
5. <span data-ttu-id="ae49d-161">เลือกลูกศรลงที่อยู่ถัดจากส่วนหัวของคอลัมน์ **Number of comments** และเลือก **เรียงลำดับจากมากไปน้อย** เพื่อดูโพสต์เรียงลำดับความคิดเห็น จากมากที่สุดไปน้อยที่สุด</span><span class="sxs-lookup"><span data-stu-id="ae49d-161">Select the down arrow next to the **Number of comments** column header and select **Sort Descending** to see the posts sorted from most to fewest comments.</span></span> 
   
   ![ความคิดเห็นสำหรับแต่ละข้อความ](media/desktop-tutorial-facebook-analytics/data-fixed.png)
   
### <a name="review-query-steps"></a><span data-ttu-id="ae49d-163">ตรวจสอบขั้นตอนคิวรี</span><span class="sxs-lookup"><span data-stu-id="ae49d-163">Review query steps</span></span>

<span data-ttu-id="ae49d-164">ขณะที่คุณจัดรูปทรงและแปลงข้อมูลใน **ตัวแก้ไข Power Query** แต่ละขั้นตอนจะถูกบันทึกไว้ในพื้นที่ของ **ขั้นตอนที่กำหนดใช้** ของบานหน้าต่าง **ตั้งค่าคิวรี** ทางด้านขวาของ ตัวแก้ไข Power Query</span><span class="sxs-lookup"><span data-stu-id="ae49d-164">As you shape and transform data in the Power Query Editor, each step is recorded in the **Applied Steps** area of the **Query Settings** pane at the right side of the **Power Query Editor** window.</span></span> <span data-ttu-id="ae49d-165">คุณสามารถย้อนกลับผ่าน **ขั้นตอนที่นำมาใช้** เพื่อดูการเปลี่ยนแปลงที่คุณทำ และแก้ไข ลบ หรือจัดเรียงใหม่ได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="ae49d-165">You can step back through the **Applied Steps** to see exactly what changes you made, and edit, delete, or rearrange them if necessary.</span></span> <span data-ttu-id="ae49d-166">ใช้ความระมัดระวังเมื่อปรับเปลี่ยนขั้นตอนเหล่านี้ เนื่องจากการเปลี่ยนแปลงขั้นตอนก่อนหน้านี้อาจทำให้ขั้นตอนในภายหลังเสียหายได้</span><span class="sxs-lookup"><span data-stu-id="ae49d-166">Use caution when modifying these steps, because changing preceding steps can break later steps.</span></span> 

<span data-ttu-id="ae49d-167">หลังจากใช้การแปลงข้อมูลจนถึงตอนนี้ **ขั้นตอนที่นำมาใช้** ของคุณควรปรากฏดังนี้:</span><span class="sxs-lookup"><span data-stu-id="ae49d-167">After applying the data transformations so far, your **Applied Steps** should appear as follows:</span></span>
   
   ![ขั้นตอนที่กำหนดใช้](media/desktop-tutorial-facebook-analytics/applied-steps.png)
   
   >[!TIP]
   ><span data-ttu-id="ae49d-169">**ขั้นตอนที่นำมาใช้** โดยพื้นฐานแล้วเป็นสูตรที่เขียนใน [ภาษาสูตร Power Query M](/powerquery-m/quick-tour-of-the-power-query-m-formula-language)</span><span class="sxs-lookup"><span data-stu-id="ae49d-169">Underlying the **Applied Steps** are formulas written in the [Power Query M formula language](/powerquery-m/quick-tour-of-the-power-query-m-formula-language).</span></span> <span data-ttu-id="ae49d-170">เมื่อต้องการดูและแก้ไขสูตร เลือก **เครื่องมือแก้ไขขั้นสูง** ในกลุ่ม **คิวรี** ของแท็บ **หน้าแรก** ของริบบอน</span><span class="sxs-lookup"><span data-stu-id="ae49d-170">To see and edit the formulas, select **Advanced Editor** in the **Query** group of the **Home** tab of the ribbon.</span></span> 

### <a name="import-the-transformed-data"></a><span data-ttu-id="ae49d-171">นำเข้าข้อมูลที่ถูกแปลง</span><span class="sxs-lookup"><span data-stu-id="ae49d-171">Import the transformed data</span></span>

<span data-ttu-id="ae49d-172">เมื่อคุณพอใจกับข้อมูลแล้ว เลือก **ปิดและนำไปใช้** > **ปิดและนำไปใช้** ในแท็บ **หน้าแรก** ของริบบิ้นเพื่อนำเข้าไปใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ae49d-172">When you're satisfied with the data, select **Close & Apply** > **Close & Apply** in the **Home** tab of the ribbon to import it into Power BI Desktop.</span></span> 
   
   ![ปิดและนำไปใช้](media/desktop-tutorial-facebook-analytics/t_fb_1-loadandclose.png)
   
   <span data-ttu-id="ae49d-174">กล่องโต้ตอบแสดงความคืบหน้าของการโหลดข้อมูลลงในแบบจำลองข้อมูล Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ae49d-174">A dialog box displays the progress of loading the data into the Power BI Desktop data model.</span></span> 
   
   ![กำลังโหลดข้อมูล](media/desktop-tutorial-facebook-analytics/t_fb_1-loading.png)
   
   <span data-ttu-id="ae49d-176">เมื่อโหลดข้อมูลแล้ว ข้อมูลจะปรากฏในมุมมอง **รายงาน** เป็นคิวรีใหม่ในบานหน้าต่าง **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="ae49d-176">Once the data is loaded, it appears in the **Report** view as a new query in the **Fields** pane.</span></span>
   
   ![สกรีนช็อตแสดงเขตข้อมูลที่พร้อมใช้งานสำหรับคิวรีที่เรียกว่า Query1](media/desktop-tutorial-facebook-analytics/fb-newquery.png)
   
## <a name="use-the-data-in-report-visualizations"></a><span data-ttu-id="ae49d-178">ใช้ข้อมูลในการแสดงภาพรายงาน</span><span class="sxs-lookup"><span data-stu-id="ae49d-178">Use the data in report visualizations</span></span> 

<span data-ttu-id="ae49d-179">ตอนนี้คุณได้นำเข้าข้อมูลจากหน้า Facebook แล้ว คุณสามารถรับข้อมูลเชิงลึกเกี่ยวกับข้อมูลคุณได้อย่างรวดเร็ว และง่ายดาย โดยใช้การแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="ae49d-179">Now that you have imported data from the Facebook page, you can quickly and easily gain insights about your data by using visualizations.</span></span> <span data-ttu-id="ae49d-180">การสร้างการแสดงผลข้อมูลด้วยภาพเป็นเรื่องง่าย เพียงแค่เลือกเขตข้อมูล หรือลากจากบานหน้าต่าง **เขตข้อมูล** ลงในพื้นที่รายงาน</span><span class="sxs-lookup"><span data-stu-id="ae49d-180">Creating a visualization is easy, just select a field or drag it from the **Fields** pane onto the report canvas.</span></span>

### <a name="create-a-bar-chart"></a><span data-ttu-id="ae49d-181">สร้างแผนภูมิแท่ง</span><span class="sxs-lookup"><span data-stu-id="ae49d-181">Create a bar chart</span></span>

1. <span data-ttu-id="ae49d-182">ในมุมมอง **รายงาน** Power BI Desktop ให้เลือก **ข้อความ** จากบานหน้าต่าง **เขตข้อมูล** หรือลากลงบนพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="ae49d-182">In Power BI Desktop **Report** view, select **message** from the **Fields** pane, or drag it onto the report canvas.</span></span> <span data-ttu-id="ae49d-183">ตารางแสดงโพสต์ข้อความทั้งหมดจะปรากฏบนพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="ae49d-183">A table showing all post messages appears on the canvas.</span></span> 
   
   ![สกรีนช็อตแสดงมุมมองรายงานด้วยรายการข้อความ](media/desktop-tutorial-facebook-analytics/table-viz.png)
   
2. <span data-ttu-id="ae49d-185">เมื่อเลือกตารางนั้นแล้ว ให้เลือก **จำนวนความคิดเห็น** จากบานหน้าต่าง **เขตข้อมูล** หรือลากลงในตาราง</span><span class="sxs-lookup"><span data-stu-id="ae49d-185">With that table selected, also select **Number of comments** from the **Fields** pane, or drag it into the table.</span></span> 
   
3. <span data-ttu-id="ae49d-186">เลือกไอคอน **แผนภูมิแท่งแบบเรียงซ้อน** ในบานหน้าต่าง **การแสดงผลข้อมูลด้วยภาพ**</span><span class="sxs-lookup"><span data-stu-id="ae49d-186">Select the **Stacked bar chart** icon in the **Visualizations** pane.</span></span> <span data-ttu-id="ae49d-187">ตารางจะเปลี่ยนเป็นแผนภูมิแท่ง แสดงจำนวนความคิดเห็นของแต่ละโพสต์</span><span class="sxs-lookup"><span data-stu-id="ae49d-187">The table changes to a bar chart showing the number of comments per post.</span></span> 
   
   ![แผนภูมิแท่ง](media/desktop-tutorial-facebook-analytics/barchart1.png)
   
4. <span data-ttu-id="ae49d-189">เลือก **ตัวเลือกเพิ่มเติม** (...) ถัดจากการแสดงผลข้อมูลด้วยภาพ แล้วเลือก **เรียงตาม** > **จำนวนความคิดเห็น** เพื่อเรียงลำดับตารางตามจำนวนความคิดเห็น จากมากไปหาน้อย</span><span class="sxs-lookup"><span data-stu-id="ae49d-189">Select **More options** (...) next to the visualization, and then select **Sort by** > **Number of comments** to sort the table by descending number of comments.</span></span> 

   <span data-ttu-id="ae49d-190">สังเกตว่า ความคิดเห็นจำนวนมากที่สุดถูกเชื่อมโยงกับข้อความ **(ว่าง)** (โพสต์เหล่านี้อาจเป็นเรื่องราว ลิงก์ วิดีโอ หรือเนื้อหาอื่นที่ไม่ใช่ข้อความ)</span><span class="sxs-lookup"><span data-stu-id="ae49d-190">Notice that the most comments were associated with **(Blank)** messages (these posts may have been stories, links, videos, or other non-text content).</span></span> 
   
5. <span data-ttu-id="ae49d-191">เมื่อต้องการกรองแถวที่ว่างออก เลือก **ข้อความคือ (ทั้งหมด)** จากบานหน้าต่าง **ตัวกรอง** เลือก **เลือกทั้งหมด** และจากนั้นเลือก **(ว่าง)** เพื่อยกเลิกการเลือกเฉพาะรายการนี้</span><span class="sxs-lookup"><span data-stu-id="ae49d-191">To filter out the blank rows, select **message is (All)** from the **Filters** pane, select **Select all**, and then select **(Blank)** to deselect it.</span></span> 

   <span data-ttu-id="ae49d-192">บานหน้าต่าง **ตัวกรอง** เปลี่ยนเป็น **ข้อความที่ไม่ใช่ (ว่าง)** และแถว **(ว่าง)** ได้หายไปจากการแสดงผลข้อมูลด้วยภาพแบบแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="ae49d-192">The **Filters** pane entry changes to **message is not (Blank)**, and the **(Blank)** row disappears from the chart visualization.</span></span>
   
   ![กรองแถวว่างออก](media/desktop-tutorial-facebook-analytics/barchart3.png)
   
### <a name="format-the-chart"></a><span data-ttu-id="ae49d-194">จัดรูปแบบแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="ae49d-194">Format the chart</span></span>

<span data-ttu-id="ae49d-195">การแสดงภาพกำลังน่าสนใจมากขึ้น แต่คุณไม่สามารถมองเห็นข้อความส่วนใหญ่ในแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="ae49d-195">The visualization is getting more interesting, but you can't see much of the post text in the chart.</span></span> <span data-ttu-id="ae49d-196">เพื่อแสดงข้อความที่โพสต์ให้มากขึ้น:</span><span class="sxs-lookup"><span data-stu-id="ae49d-196">To show more of the post text:</span></span>

1. <span data-ttu-id="ae49d-197">ใช้การจัดการบนการแสดงผลข้อมูลด้วยภาพแบบแผนภูมิเพื่อปรับขนาดแผนภูมิให้มีขนาดใหญ่ที่สุดเท่าที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="ae49d-197">Use the handles on the chart visualization to resize the chart to be as large as possible.</span></span> 
   
2. <span data-ttu-id="ae49d-198">เมื่อเลือกแผนภูมิแล้ว ให้เลือกไอคอน **รูปแบบ** (ลูกกลิ้งทาสี) ในบานหน้าต่าง **การแสดงผลข้อมูลด้วยภาพ**</span><span class="sxs-lookup"><span data-stu-id="ae49d-198">With the chart selected, select the **Format** icon (paint roller) in the **Visualizations** pane.</span></span>
   
3. <span data-ttu-id="ae49d-199">เลือกลูกศรลงที่อยู่ถัดจาก **แกน Y** แล้วลากตัวเลื่อน **ขนาดสูงสุด** ไปทางด้านขวาจนสุด (**50%** )</span><span class="sxs-lookup"><span data-stu-id="ae49d-199">Select the down arrow next to **Y axis**, and drag the **Maximum size** slider all the way to the right (**50%**).</span></span> 
4. <span data-ttu-id="ae49d-200">ลด **ขนาดของข้อความ** ให้เหลือ **10 pt** เพื่อแสดงข้อความได้มากขึ้น</span><span class="sxs-lookup"><span data-stu-id="ae49d-200">Reduce the **Text size** to **10 pt** to fit more text.</span></span>
   
   ![เปลี่ยนแปลงการจัดรูปแบบ](media/desktop-tutorial-facebook-analytics/barchart4.png)
   
   <span data-ttu-id="ae49d-202">แผนภูมิตอนนี้แสดงเนื้อหาของโพสต์มากขึ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="ae49d-202">The chart now shows more of the post content.</span></span> 
   
   ![แสดงโพสต์มากขึ้น](media/desktop-tutorial-facebook-analytics/barchart5.png)
   
<span data-ttu-id="ae49d-204">แกน X (จำนวนความคิดเห็น) ของแผนภูมิไม่ได้แสดงค่าที่ชัดเจน และดูหลุดหายไปที่ด้านล่างของแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="ae49d-204">The x axis (number of comments) of the chart doesn't show exact values, and looks lost at the bottom of the chart.</span></span> <span data-ttu-id="ae49d-205">มาลองใช้ป้ายชื่อข้อมูลแทน:</span><span class="sxs-lookup"><span data-stu-id="ae49d-205">Let's use data labels instead:</span></span> 

1. <span data-ttu-id="ae49d-206">เลือกไอคอน **รูปแบบ** จากนั้นตั้งค่าตัวเลื่อนสำหรับ **แกน X** เป็น **ปิด**</span><span class="sxs-lookup"><span data-stu-id="ae49d-206">Select the **Format** icon, and then set the slider for **X axis** to **Off**.</span></span> 
   
2. <span data-ttu-id="ae49d-207">เลือกตัวเลื่อน **ป้ายชื่อข้อมูล** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="ae49d-207">Select the **Data labels** slider to **On**.</span></span> 

   <span data-ttu-id="ae49d-208">ตอนนี้ แผนภูมิแสดงจำนวนความคิดเห็นของแต่ละโพสต์ที่ชัดเจน</span><span class="sxs-lookup"><span data-stu-id="ae49d-208">Now the chart shows the exact number of comments for each post.</span></span>
   
   ![ใช้ป้ายชื่อข้อมูล](media/desktop-tutorial-facebook-analytics/barchart6.png)
   
### <a name="edit-the-data-type"></a><span data-ttu-id="ae49d-210">แก้ไขชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ae49d-210">Edit the data type</span></span>

<span data-ttu-id="ae49d-211">นั่นดีขึ้นแล้ว แต่มีป้ายชื่อข้อมูลทั้งหมดมีจุดทศนิยม **.0** ซึ่งดูขัดตาและไม่ถูกต้อง เพราะ **จำนวนความคิดเห็น** จะต้องเป็นจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="ae49d-211">That's better, but all the data labels have a **.0** decimal place, which is distracting and misleading, because **Number of posts** must be a whole number.</span></span> <span data-ttu-id="ae49d-212">เพื่อแก้ไขปัญหาดังกล่าว คุณจำเป็นต้องเปลี่ยนชนิดข้อมูลของคอลัมน์ **จำนวนความคิดเห็น** ให้เป็น **จำนวนเต็ม**:</span><span class="sxs-lookup"><span data-stu-id="ae49d-212">To fix them, you need to change the data type of the **Number of posts** column to **Whole Number**:</span></span>

1. <span data-ttu-id="ae49d-213">คลิกขวา **Query1** ในบานหน้าต่าง **เขตข้อมูล** หรือวางเมาส์ไว้เหนือส่วนดังกล่าว และเลือก **ตัวเลือกเพิ่มเติม** (...)</span><span class="sxs-lookup"><span data-stu-id="ae49d-213">Right-click **Query1** in the **Fields** pane, or hover over it and select **More options** (...).</span></span> 

2. <span data-ttu-id="ae49d-214">จากเมนูบริบท ให้เลือก **แก้ไขคิวรี**</span><span class="sxs-lookup"><span data-stu-id="ae49d-214">From the context menu, select **Edit query**.</span></span> <span data-ttu-id="ae49d-215">หรือ เลือก **แก้ไขคิวรี** > **แก้ไขคิวรี** จากกลุ่ม **ข้อมูลภายนอก** ของแท็บ **หน้าแรก** ในริบบิ้น</span><span class="sxs-lookup"><span data-stu-id="ae49d-215">Or, select **Edit Queries** > **Edit Queries** from the **External data** group of the **Home** tab in the ribbon.</span></span> 
   
3. <span data-ttu-id="ae49d-216">จากหน้าต่าง **ตัวแก้ไข Power Query** ให้เลือกคอลัมน์ **จำนวนความคิดเห็น** และเปลี่ยนชนิดข้อมูลโดยทำตามหนึ่งในขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ae49d-216">From the **Power Query Editor** window, select the **Number of comments** column, and change the data type by following one of these steps:</span></span> 
   - <span data-ttu-id="ae49d-217">เลือกไอคอน **1.2** ที่อยู่ถัดจากส่วนหัวของคอลัมน์ **Number of comments** และเลือก **จำนวนเต็ม** จากรายการดรอปดาวน์</span><span class="sxs-lookup"><span data-stu-id="ae49d-217">Select the **1.2** icon next to the **Number of comments** column header, and then select **Whole number** from the drop-down list</span></span>
   - <span data-ttu-id="ae49d-218">คลิกขวาที่ส่วนหัวของคอลัมน์ และเลือก **เปลี่ยนชนิด** > **จำนวนเต็ม**</span><span class="sxs-lookup"><span data-stu-id="ae49d-218">Right-click the column header, and then select **Change Type** > **Whole Number**.</span></span>
   - <span data-ttu-id="ae49d-219">เลือก **ชนิดข้อมูล: เลขทศนิยม** ในกลุ่ม **แปลง** ของแท็บ **หน้าแรก** หรือกลุ่ม **คอลัมน์ใดก็ตาม** ของแท็บ **แปลง** และจากนั้นเลือก **จำนวนเต็ม**</span><span class="sxs-lookup"><span data-stu-id="ae49d-219">Select **Data type: Decimal Number** in the **Transform** group of the **Home** tab, or in the **Any Column** group of the **Transform** tab, and then select **Whole Number**.</span></span>
   
   <span data-ttu-id="ae49d-220">ไอคอนในส่วนหัวของคอลัมน์เปลี่ยนไปเป็น **123** โดยแสดงถึงชนิดข้อมูล **จำนวนเต็ม**</span><span class="sxs-lookup"><span data-stu-id="ae49d-220">The icon in the column header changes to **123**, denoting a **Whole Number** data type.</span></span>
   
   ![เปลี่ยนชนิดข้อมูล](media/desktop-tutorial-facebook-analytics/change-datatype.png)
   
3. <span data-ttu-id="ae49d-222">เมื่อต้องใช้การเปลี่ยนแปลง ให้เลือก **ไฟล์** > **ปิดและนำไปใช้** หรือ **ไฟล์** > **นำไปใช้** เพื่อทำให้หน้าต่าง **ตัวแก้ไข Power Query** เปิดอยู่เสมอ</span><span class="sxs-lookup"><span data-stu-id="ae49d-222">To apply the changes, select **File** > **Close & Apply**, or **File** > **Apply** to keep the **Power Query Editor** window open.</span></span> 

   <span data-ttu-id="ae49d-223">หลังจากโหลดการเปลี่ยนแปลงแล้ว ป้ายชื่อข้อมูลบนแผนภูมิกลายเป็นจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="ae49d-223">After the changes load, the data labels on the chart become whole numbers.</span></span>
   
   ![แผนภูมิที่เป็นตัวเลขจำนวนเต็ม](media/desktop-tutorial-facebook-analytics/vis-3.png)
   
### <a name="create-a-date-slicer"></a><span data-ttu-id="ae49d-225">สร้างตัวแบ่งส่วนข้อมูลวันที่</span><span class="sxs-lookup"><span data-stu-id="ae49d-225">Create a date slicer</span></span>

<span data-ttu-id="ae49d-226">สมมติว่าคุณต้องการแสดงภาพจำนวนความคิดเห็นบนโพสต์เทียบกับเวลา</span><span class="sxs-lookup"><span data-stu-id="ae49d-226">Suppose you want to visualize the number of comments on posts over time.</span></span> <span data-ttu-id="ae49d-227">คุณสามารถสร้างตัวแบ่งส่วนข้อมูล เพื่อกรองข้อมูลแผนภูมิที่ช่วงเวลาต่าง ๆ กัน</span><span class="sxs-lookup"><span data-stu-id="ae49d-227">You can create a slicer visualization to filter the chart data to different time frames.</span></span> 

1. <span data-ttu-id="ae49d-228">คลิกที่พื้นที่ว่างของพื้นที่ทำงาน จากนั้นเลือกไอคอน **ตัวแบ่งส่วนข้อมูล** ในบานหน้าต่าง **การแสดงผลข้อมูลด้วยภาพ**</span><span class="sxs-lookup"><span data-stu-id="ae49d-228">Select a blank area of the canvas, and then select the **Slicer** icon in the **Visualizations** pane.</span></span> 

   <span data-ttu-id="ae49d-229">ตัวแบ่งส่วนข้อมูลที่ว่างเปล่าจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="ae49d-229">A blank slicer visualization appears.</span></span>
   
   ![เลือกไอคอนตัวแบ่งส่วนข้อมูล](media/desktop-tutorial-facebook-analytics/slicer1.png)
   
2. <span data-ttu-id="ae49d-231">เลือกเขตข้อมูล **created_date** จากบานหน้าต่าง **เขตข้อมูล** หรือลากลงในตัวแบ่งส่วนข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="ae49d-231">Select the **created_date** field from the **Fields** pane, or drag it into the new slicer.</span></span> 

   <span data-ttu-id="ae49d-232">ตัวแบ่งส่วนข้อมูลเปลี่ยนเป็นแถบเลื่อนช่วงวันที่ โดยอิงตามชนิดข้อมูล **Date** ของเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ae49d-232">The slicer changes to a date range slider, based on the field's **Date** data type.</span></span>
   
   ![แถบเลื่อนช่วงวันที่](media/desktop-tutorial-facebook-analytics/slicer2.png)
   
3. <span data-ttu-id="ae49d-234">ย้ายจุดจับตัวเลื่อน เพื่อเลือกช่วงวันที่แตกต่างกัน และสังเกตว่าแผนภูมิกรองข้อมูลอย่างไร</span><span class="sxs-lookup"><span data-stu-id="ae49d-234">Move the slider handles to select different date ranges, and note how the chart data filters accordingly.</span></span> <span data-ttu-id="ae49d-235">คุณยังสามารถเลือกเขตข้อมูลวันที่ในตัวแบ่งส่วนข้อมูล และพิมพ์ในวันที่ที่ต้องการ หรือเลือกจากปฏิทินที่ป็อปอัพ</span><span class="sxs-lookup"><span data-stu-id="ae49d-235">You can also select the date fields in the slicer and type in specific dates, or choose them from a calendar popup.</span></span>
    
   ![แบ่งกลุ่มข้อมูล](media/desktop-tutorial-facebook-analytics/slicer3.png)
   
### <a name="format-the-visualizations"></a><span data-ttu-id="ae49d-237">จัดรูปแบบการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="ae49d-237">Format the visualizations</span></span>

<span data-ttu-id="ae49d-238">ให้ชื่อที่สื่อความหมายและน่าดึงดูดยิ่งขึ้นแก่แผนภูมิ:</span><span class="sxs-lookup"><span data-stu-id="ae49d-238">Give the chart a more descriptive and attractive title:</span></span> 

1. <span data-ttu-id="ae49d-239">เมื่อเลือกแผนภูมิแล้ว ให้เลือกไอคอน **รูปแบบ** ในบานหน้าต่าง **การแสดงผลข้อมูลด้วยภาพ** จากนั้นเลือกลูกศรดรอปดาวน์ถัดจาก **ชื่อ** เพื่อขยาย</span><span class="sxs-lookup"><span data-stu-id="ae49d-239">With the chart selected, select the **Format** icon in the **Visualizations** pane, and then select the drop-down arrow next to **Title** to expand it.</span></span>

2. <span data-ttu-id="ae49d-240">การเปลี่ยนแปลง **ข้อความสำหรับชื่อเรื่อง** เมื่อต้องการ **จำนวนความคิดเห็นต่อโพสต์**</span><span class="sxs-lookup"><span data-stu-id="ae49d-240">Change the **Title text** to **Comments per post**.</span></span> 

3. <span data-ttu-id="ae49d-241">เลือกลูกศรดรอปดาวน์ที่อยู่ถัดจาก **สีแบบอักษร** และเลือกสีเขียวเพื่อให้ตรงกับแท่งสีเขียวของการแสดงผลข้อมูลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="ae49d-241">Select the drop-down arrow next to **Font color**, and select a green color to match the green bars of the visualization.</span></span>

4. <span data-ttu-id="ae49d-242">เพิ่ม **ขนาดแบบอักษร** เป็น **10 pt** และเปลี่ยน **ตระกูลแบบอักษร** เป็น **Segoe (Bold)**</span><span class="sxs-lookup"><span data-stu-id="ae49d-242">Increase the **Text size** to **10 pt**, and change the **Font family** to **Segoe (Bold)**.</span></span>

5. <span data-ttu-id="ae49d-243">ทดลองตัวเลือกจัดรูปแบบและการตั้งค่าอื่น ๆ เพื่อปรับเปลี่ยนการแสดงภาพของคุณ</span><span class="sxs-lookup"><span data-stu-id="ae49d-243">Experiment with other formatting options and settings to change the appearance of your visualizations.</span></span> 

   ![การแสดงผลข้อมูลด้วยภาพ](media/desktop-tutorial-facebook-analytics/vis-1.png)

## <a name="create-more-visualizations"></a><span data-ttu-id="ae49d-245">สร้างการแสดงภาพเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ae49d-245">Create more visualizations</span></span>

<span data-ttu-id="ae49d-246">คุณน่าจะเห็นแล้วว่า การปรับเปลี่ยนการแสดงภาพในรายงานของคุณ เพื่อนำเสนอข้อมูลในแบบที่คุณต้องการนั้น เป็นเรื่องง่าย</span><span class="sxs-lookup"><span data-stu-id="ae49d-246">As you can see, it's easy to customize visualizations in your report to present the data in ways that you want.</span></span> <span data-ttu-id="ae49d-247">เพื่อเป็นตัวอย่าง ลองใช้ข้อมูลนำเข้าจาก Facebook เพื่อสร้างแผนภูมิเส้นที่แสดงจำนวนความคิดเห็นเทียบกับเวลา</span><span class="sxs-lookup"><span data-stu-id="ae49d-247">For example, try using the imported Facebook data to create this line chart showing the number of comments over time.</span></span>

![แผนภูมิเส้น](media/desktop-tutorial-facebook-analytics/moreviz.png)

<span data-ttu-id="ae49d-249">Power BI Desktop ให้ประสบการณ์ที่ราบรื่น ตั้งแต่การรับข้อมูลจากแหล่งข้อมูลต่าง ๆ และจัดรูปทรงให้ตรงกับความต้องการการวิเคราะห์ของคุณ ไปจนถึงการแสดงข้อมูลนี้ในแบบที่สวยงามและโต้ตอบได้</span><span class="sxs-lookup"><span data-stu-id="ae49d-249">Power BI Desktop provides a seamless end-to-end experience, from getting data from a wide range of data sources and shaping it to meet your analysis needs, to visualizing this data in rich and interactive ways.</span></span> <span data-ttu-id="ae49d-250">เมื่อรายงานของคุณพร้อมแล้ว คุณสามารถ[อัปโหลดไปยังบริการของ Power BI](../create-reports/desktop-upload-desktop-files.md) และสร้างแดชบอร์ดจากรายงานเพื่อแชร์ให้กับผู้ใช้ Power BI อื่นได้</span><span class="sxs-lookup"><span data-stu-id="ae49d-250">When your report is ready, you can [upload it to the Power BI service](../create-reports/desktop-upload-desktop-files.md) and create dashboards based on it to share with other Power BI users.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ae49d-251">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="ae49d-251">Next steps</span></span>
* [<span data-ttu-id="ae49d-252">Microsoft Learn สำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="ae49d-252">Microsoft Learn for Power BI</span></span>](/learn/powerplatform/power-bi?WT.mc_id=powerbi_landingpage-docs-link)
* [<span data-ttu-id="ae49d-253">เยี่ยมชมกระดานสนทนา Power BI</span><span class="sxs-lookup"><span data-stu-id="ae49d-253">Visit the Power BI Forum</span></span>](https://go.microsoft.com/fwlink/?LinkID=519326)
* [<span data-ttu-id="ae49d-254">อ่านบล็อก Power BI</span><span class="sxs-lookup"><span data-stu-id="ae49d-254">Read the Power BI Blog</span></span>](https://go.microsoft.com/fwlink/?LinkID=519327)