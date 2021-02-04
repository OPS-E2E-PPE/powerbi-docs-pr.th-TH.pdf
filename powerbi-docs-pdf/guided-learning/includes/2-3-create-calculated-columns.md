---
ms.openlocfilehash: fcf73962534ec8f1fda009304768fd43aaa0955a
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2019
ms.locfileid: "61257092"
---
<span data-ttu-id="c7c33-101">การสร้างคอลัมน์จากการคำนวณคือวิธีง่ายๆ ในการส่งเสริมและเพิ่มประสิทธิภาพของข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7c33-101">Creating calculated columns is a simple way to enrich and enhance your data.</span></span> <span data-ttu-id="c7c33-102">**คอลัมน์จากการคำนวณ**คือ คอลัมน์ใหม่ที่คุณสร้างขึ้นโดยการกำหนดการคำนวณที่แปลงหรือรวมสององค์ประกอบหรือมากกว่าของข้อมูลที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="c7c33-102">A **calculated column** is a new column that you create by defining a calculation that transforms or combines two or more elements of existing data.</span></span> <span data-ttu-id="c7c33-103">ตัวอย่างเช่น คุณสามารถสร้างคอลัมน์ใหม่โดยการรวมสองคอลัมน์ให้เป็นคอลัมน์เดียว</span><span class="sxs-lookup"><span data-stu-id="c7c33-103">For example, you can create a new column by combining two columns into one.</span></span>

<span data-ttu-id="c7c33-104">สาเหตุหนึ่งข้อที่เป็นประโยชน์สำหรับการสร้างคอลัมน์จากการคำนวณคือเพื่อสร้างความสัมพันธ์ระหว่างตาราง เมื่อไม่มีเขตข้อมูลที่ไม่ซ้ำกันที่คุณสามารถใช้เพื่อสร้างความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="c7c33-104">One useful reason for creating a calculated column is to establish a relationship between tables, when no unique fields exist that can be used to establish a relationship.</span></span> <span data-ttu-id="c7c33-105">การขาดความสัมพันธ์จะปรากฏอย่างชัดเจนเมื่อคุณสร้างการแสดงข้อมูลตารางง่ายๆ ใน Power BI Desktop และคุณจะได้รับค่าเดียวกับสำหรับรายการทั้งหมด แม้ว่าคุณจะทราบว่าข้อมูลย่อยต่างกัน</span><span class="sxs-lookup"><span data-stu-id="c7c33-105">The lack of a relationship becomes apparent when you create a simple table visual in Power BI Desktop, and you get the same value for all entries, yet you know the underlying data is different.</span></span>

![](media/2-3-create-calculated-columns/2-3_1.png)

<span data-ttu-id="c7c33-106">เมื่อต้องการสร้างความสัมพันธ์ด้วยเขตข้อมูลที่ไม่ซ้ำกันในข้อมูล คุณสามารถสร้างคอลัมน์จากการคำนวณใหม่สำหรับ “หมายเลขโทรศัพท์แบบเต็ม” โดยการผสมค่าจากคอลัมน์ “รหัสพื้นที่” และ “หมายเลขท้องถิ่น” เมื่อมีค่าเหล่านั้นอยู่ในข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7c33-106">To create a relationship with unique fields in data, you can, for example, create a new calculated column for "Full Phone Number" by combining the values from the "Area Code" and "Local Number" columns when those values exist in your data.</span></span> <span data-ttu-id="c7c33-107">คอลัมน์จากการคำนวณคือ เครื่องมือที่มีประโยชน์สำหรับการสร้างแบบจำลองและการจัดรูปแบบการแสดงข้อมูลอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="c7c33-107">Calculated columns are a useful tool for quickly creating models and visualizations.</span></span>

<span data-ttu-id="c7c33-108">เมื่อต้องการสร้างคอลัมน์จากการคำนวณ ให้เลือก **มุมมองข้อมูล** ใน Power BI Desktop จากด้านซ้ายของพื้นที่ทำงานของรายงาน</span><span class="sxs-lookup"><span data-stu-id="c7c33-108">To create a calculated column, select the **Data view** in Power BI Desktop from the left side of the report canvas.</span></span>

![](media/2-3-create-calculated-columns/2-3_2.png)

<span data-ttu-id="c7c33-109">จากแท็บ การวางรูปแบบ ให้เลือก **คอลัมน์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c7c33-109">From the Modeling tab, select **New Column**.</span></span> <span data-ttu-id="c7c33-110">การทำเช่นนี้จะเปิดใช้งานแถบสูตรที่คุณสามารถใส่การคำนวณโดยใช้ภาษา DAX (นิพจน์วิเคราะห์ข้อมูล)</span><span class="sxs-lookup"><span data-stu-id="c7c33-110">This will enable the formula bar where you can enter calculations using DAX (Data Analysis Expressions) language.</span></span> <span data-ttu-id="c7c33-111">DAX คือ ภาษาสูตรที่มีประสิทธิภาพ ที่ใช้ใน Excel ที่ช่วยให้คุณสามารถสร้างการคำนวณที่ซับซ้อนได้</span><span class="sxs-lookup"><span data-stu-id="c7c33-111">DAX is a powerful formula language, also found in Excel, that lets you build robust calculations.</span></span> <span data-ttu-id="c7c33-112">เมื่อคุณพิมพ์สูตร Power BI Desktop จะแสดงสูตรหรือองค์ประกอบข้อมูลที่ตรงกัน เพื่อช่วยเหลือและเร่งความเร็วในการสร้างสูตรของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7c33-112">As you type a formula, Power BI Desktop displays matching formulas or data elements to assist and accelerate the creation of your formula.</span></span>

<span data-ttu-id="c7c33-113">แถบสูตรของ Power BI จะแนะนำฟังก์ชัน DAX เฉพาะและคอลัมน์ข้อมูลที่เกี่ยวข้องเมื่อคุณใส่นิพจน์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c7c33-113">The Power BI formula bar will suggest specific DAX functions and related data columns as you enter your expression.</span></span>

![](media/2-3-create-calculated-columns/2-3_3.png)

<span data-ttu-id="c7c33-114">เมื่อคอลัมน์จากการคำนวณถูกสร้างขึ้นในแต่ละตารางแล้ว จะสามารถใช้เป็นคีย์ที่ไม่ซ้ำกันเพื่อสร้างความสัมพันธ์ระหว่างตารางได้</span><span class="sxs-lookup"><span data-stu-id="c7c33-114">Once the calculated columns are created in each table, they can be used as a unique key to establish a relationship between them.</span></span> <span data-ttu-id="c7c33-115">เมื่อไปที่มุมมอง**ความสัมพันธ์** คุณจะสามารถลากเขตข้อมูลจากตารางหนึ่งไปยังอีกตารางหนึ่งได้เพื่อสร้างความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="c7c33-115">Going to **Relationship** view, you can then drag the field from one table to the other to create the relationship.</span></span>

![](media/2-3-create-calculated-columns/2-3_4.png)

<span data-ttu-id="c7c33-116">เมื่อย้อนกลับไปที่มุมมอง**รายงาน** คุณจะเห็นค่าต่างๆ สำหรับแต่ละเขต</span><span class="sxs-lookup"><span data-stu-id="c7c33-116">Returning to **Report** view, you now see a different value for each district.</span></span>

![](media/2-3-create-calculated-columns/2-3_5.png)

<span data-ttu-id="c7c33-117">ยังมีสิ่งอื่นๆ อีกมากมายที่คุณสามารถทำได้โดยการสร้างคอลัมน์จากการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="c7c33-117">There are all sorts of other things you can do by creating calculated columns, too.</span></span>

