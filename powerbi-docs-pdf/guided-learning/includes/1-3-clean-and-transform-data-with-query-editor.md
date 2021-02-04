---
ms.openlocfilehash: e8b920763ea619fe74af2b71730164183f333a95
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2019
ms.locfileid: "61265200"
---
<span data-ttu-id="e19ca-101">**Power BI Desktop** มี**ตัวแก้ไขคิวรี** ซึ่งเป็นเครื่องมือที่มีประสิทธิภาพสำหรับการจัดรูปร่างและการแปลงข้อมูล เพื่อให้พร้อมสำหรับแบบจำลองและการจัดรูปแบบการแสดงข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="e19ca-101">**Power BI Desktop** includes **Query Editor**, a powerful tool for shaping and transforming data so it's ready for your models and visualizations.</span></span> <span data-ttu-id="e19ca-102">เมื่อคุณเลือกตัวแก้ไขจากตัวนำทาง ตัวแก้ไขคิวรีจะเปิดขึ้นพร้อมกับตารางหรือรายการอื่นๆ ที่คุณเลือกจากแหล่งข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="e19ca-102">When you select Edit from Navigator, Query Editor launches and is populated with the tables or other entities you selected from your data source.</span></span>

<span data-ttu-id="e19ca-103">คุณยังสามารถเรียกใช้**ตัวแก้ไขคิวรี**ได้โดยตรงจาก **Power BI Desktop** โดยใช้ปุ่ม **แก้ไขคิวรี** บน Ribbon **หน้าแรก**</span><span class="sxs-lookup"><span data-stu-id="e19ca-103">You can also launch **Query Editor** directly from **Power BI Desktop**, using the **Edit Queries** button on the **Home** ribbon.</span></span>

![](media/1-3-clean-and-transform-data-with-query-editor/1-3_1.png)

<span data-ttu-id="e19ca-104">เมื่อตัวแก้ไขคิวรีมีข้อมูลที่พร้อมให้คุณจัดรูปร่างแล้ว คุณจะเห็นส่วนต่างๆ:</span><span class="sxs-lookup"><span data-stu-id="e19ca-104">Once Query Editor is loaded with data that's ready for you to shape, you see a handful of sections:</span></span>

1. <span data-ttu-id="e19ca-105">ใน Ribbon มีปุ่มจำนวนมากพร้อมใช้งานเพื่อโต้ตอบกับข้อมูลในคิวรี</span><span class="sxs-lookup"><span data-stu-id="e19ca-105">In the ribbon, many buttons are now active to interact with the data in the query</span></span>
2. <span data-ttu-id="e19ca-106">ในบานหน้าต่างด้านซ้าย คิวรี (สำหรับแต่ละตารางหรือรายการ) จะแสดงอยู่และพร้อมใช้งานสำหรับการเลือก การดู และการจัดรูปร่าง</span><span class="sxs-lookup"><span data-stu-id="e19ca-106">In the left pane, queries (one for each table, or entity) are listed and available for selection, viewing, and shaping</span></span>
3. <span data-ttu-id="e19ca-107">ในบานหน้าต่างตรงกลาง ข้อมูลจากคิวรีที่เลือกจะแสดงและพร้อมใช้งานสำหรับการจัดรูปร่าง</span><span class="sxs-lookup"><span data-stu-id="e19ca-107">In the center pane, data from the selected query is displayed and available for shaping</span></span>
4. <span data-ttu-id="e19ca-108">หน้าต่างการตั้งค่าคิวรีจะปรากฏขึ้น พร้อมกับคุณสมบัติของคิวรีและขั้นตอนที่ถูกนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="e19ca-108">The Query Settings window appears, listing the query’s properties and applied steps</span></span>

![](media/1-3-clean-and-transform-data-with-query-editor/1-3_2.png)

<span data-ttu-id="e19ca-109">ในบานหน้าต่างตรงกลาง การคลิกขวาบนคอลัมน์จะแสดงการแปลงต่างๆ จำนวนหนึ่งที่พร้อมใช้งาน เช่น การนำคอลัมน์ออกจากตาราง การทำซ้ำคอลัมน์โดยใช้ชื่อใหม่ และการแทนที่ค่า</span><span class="sxs-lookup"><span data-stu-id="e19ca-109">In the center pane, right-clicking on a column displays a number of different available transformations, such as removing the column from the table, duplicating the column under a new name, and replacing values.</span></span> <span data-ttu-id="e19ca-110">จากเมนูนี้ คุณยังสามารถแยกคอลัมน์ข้อความเป็นหลายคอลัมน์ได้โดยใช้ตัวคั่นทั่วไป</span><span class="sxs-lookup"><span data-stu-id="e19ca-110">From this menu you can also split text columns into multiples by common delimiters.</span></span>

![](media/1-3-clean-and-transform-data-with-query-editor/1-3_3.png)

<span data-ttu-id="e19ca-111">Ribbon ของ**ตัวแก้ไขคิวรี**มีเครื่องมือเพิ่มเติม เช่น การเปลี่ยนชนิดข้อมูลของข้อมูล การเพิ่มสัญลักษณ์ทางวิทยาศาสตร์ หรือการแยกองค์ประกอบจากวันที่ เช่น วันในสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="e19ca-111">The **Query Editor** ribbon contains additional tools, such as changing the data type of columns, adding scientific notation, or extracting elements from dates, such as day of the week.</span></span>

![](media/1-3-clean-and-transform-data-with-query-editor/1-3_4.png)

<span data-ttu-id="e19ca-112">เมื่อคุณนำการแปลงไปใช้ แต่ละขั้นตอนจะปรากฏในรายการ **ขั้นตอนที่ถูกนำไปใช้** ในบานหน้าต่าง **การตั้งค่าคิวรี** ทางด้านขวาของ **ตัวแก้ไขคิวรี**</span><span class="sxs-lookup"><span data-stu-id="e19ca-112">As you apply transformations, each step appears in the **Applied Steps** list in the **Query Settings** pane on the right side of **Query Editor**.</span></span> <span data-ttu-id="e19ca-113">คุณสามารถใช้รายการเพื่อเลิกทำหรือตรวจทานการเปลี่ยนแปลงต่างๆ หรือแม้แต่เปลี่ยนชื่อของขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="e19ca-113">You can use this list to undo or review specific changes, or even change the name of a step.</span></span> <span data-ttu-id="e19ca-114">เมื่อต้องการบันทึกการเปลี่ยนของคุณ ให้เลือก **ปิดและนำไปใช้** บนแท็บ **หน้าแรก**</span><span class="sxs-lookup"><span data-stu-id="e19ca-114">To save your transformations, select **Close & Apply** on the **Home** tab.</span></span>

![](media/1-3-clean-and-transform-data-with-query-editor/1-3_5.png)

<span data-ttu-id="e19ca-115">เมื่อคุณเลือก **ปิดและนำไปใช้** ตัวแก้ไขคิวรีจะนำการเปลี่ยนแปลงที่คุณทำไปใช้ และนำไปใช้กับ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e19ca-115">Once you select **Close & Apply**, Query Editor applies the query changes you made, and applies them to Power BI Desktop.</span></span>

![](media/1-3-clean-and-transform-data-with-query-editor/1-3_6.png)

<span data-ttu-id="e19ca-116">ยังมีสิ่งต่างๆ อีกมากมายที่คุณสามารถทำได้เมื่อแปลข้อมูลใน**ตัวแก้ไขคิวรี** รวมถึง การแปลงขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="e19ca-116">There are all sorts of things you can do when transforming data in **Query Editor**, including advanced transformations.</span></span> <span data-ttu-id="e19ca-117">ในส่วนถัดไป เราจะอธิบายบางส่วนของการแปลงขั้นสูงเหล่านั้น เพื่อให้คุณเข้าใจวิธีที่คุณสามารถแปลงข้อมูลของคุณด้วย**ตัวแก้ไขคิวรี**ได้อย่างไม่จำกัด</span><span class="sxs-lookup"><span data-stu-id="e19ca-117">In the next section, we take a look at a few of those advanced transformations, to give you a sense of the almost immeasurable ways you can transform your data with **Query Editor**.</span></span>

