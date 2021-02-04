---
ms.openlocfilehash: 0296512b59baf828dd284088e0109af819aee261
ms.sourcegitcommit: 66b1a0c74b8a7dcb33a2f8570fb67bce2401a895
ms.contentlocale: th-TH
ms.lasthandoff: 06/08/2020
ms.locfileid: "84562297"
---
<span data-ttu-id="32ce4-101">มีการคำนวณหลักสองแบบที่คุณสามารถสร้างได้โดยใช้ DAX:</span><span class="sxs-lookup"><span data-stu-id="32ce4-101">There are two primary calculations you can create using DAX:</span></span>

* <span data-ttu-id="32ce4-102">**คอลัมน์จากการคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="32ce4-102">**calculated columns**</span></span>
* <span data-ttu-id="32ce4-103">**หน่วยวัด**</span><span class="sxs-lookup"><span data-stu-id="32ce4-103">**measures**</span></span>

<span data-ttu-id="32ce4-104">ก่อนเจาะลึกลงไปถึงการสร้างสองสิ่งนั้น คุณควรเข้าใจถึงไวยากรณ์ DAX สำหรับตารางและคอลัมน์ ซึ่งคุณจะใช้เมื่อสร้าง**คอลัมน์จากการคำนวณ**หรือ**หน่วยวัด**</span><span class="sxs-lookup"><span data-stu-id="32ce4-104">Before digging into creating either of those, it's good to have a firm grasp on DAX syntax for tables and columns, which you will use when creating either **calculated columns** or **measures**.</span></span>

## <a name="dax-table-and-column-name-syntax"></a><span data-ttu-id="32ce4-105">ไวยากรณ์ของชื่อตารางและคอลัมน์ DAX</span><span class="sxs-lookup"><span data-stu-id="32ce4-105">DAX table and column name syntax</span></span>
<span data-ttu-id="32ce4-106">ไม่ว่าคุณจะสร้างคอลัมน์หรือการวัดใหม่ สิ่งสำคัญคือการรู้จักรูปแบบทั่วไปของชื่อตารางใน DAX:</span><span class="sxs-lookup"><span data-stu-id="32ce4-106">Whether you're creating a new column or measure, it's important to know the general format of table names in DAX:</span></span>

    'Table Name'[ColumnName]

<span data-ttu-id="32ce4-107">ถ้ามีช่องว่างในชื่อตาราง (ดังที่แสดงอยู่ด้านบน) จะต้องมีอัญประกาศเดี่ยวคร่อมชื่อตาราง</span><span class="sxs-lookup"><span data-stu-id="32ce4-107">If there are spaces in the table name (as shown above), the single quotes around the table name are mandatory.</span></span> <span data-ttu-id="32ce4-108">ถ้าชื่อตารางไม่มีช่องว่าง คุณสามารถละเว้นอัญประกาศเดี่ยวได้ ดังนั้นไวยากรณ์จะมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="32ce4-108">If the table name has no spaces, the single quotes can be omitted, so the syntax looks like the following:</span></span>

    TableName[ColumnName]

<span data-ttu-id="32ce4-109">รูปต่อไปนี้แสดงสูตร DAX ที่กำลังถูกสร้างใน Power BI</span><span class="sxs-lookup"><span data-stu-id="32ce4-109">The following image shows a DAX formula being created in Power BI:</span></span>

![](media/7-2-dax-calculation-types/dax-calc-types_1.png)

<span data-ttu-id="32ce4-110">คุณสามารถละเว้นชื่อตารางแล้วใช้เพียงชื่อคอลัมน์ได้เช่นกัน แต่นี่ไม่ใช่วิธีที่ดีในการเขียนฟังก์ชันที่ชัดเจน (และโค้ด DAX ที่ชัดเจน)</span><span class="sxs-lookup"><span data-stu-id="32ce4-110">You can also omit the table name completely and just use the column name, but this is not a best practice for writing clear functions (and thus, for clear DAX code).</span></span> <span data-ttu-id="32ce4-111">ชื่อคอลัมน์ต้องมีวงเล็บสี่เหลี่ยมเสมอ</span><span class="sxs-lookup"><span data-stu-id="32ce4-111">Column names must always include the square brackets.</span></span>

<span data-ttu-id="32ce4-112">วิธีปฏิบัติที่ดีที่สุด*เสมอ* มีดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="32ce4-112">It's best practice to *always* do the following:</span></span>

* <span data-ttu-id="32ce4-113">ไม่มีช่องว่างในชื่อตาราง</span><span class="sxs-lookup"><span data-stu-id="32ce4-113">No spaces in table names</span></span>
* <span data-ttu-id="32ce4-114">ใส่ชื่อตารางในสูตรเสมอ (อย่าละเว้น แม้ DAX จะยอมให้คุณทำเช่นนั้นได้)</span><span class="sxs-lookup"><span data-stu-id="32ce4-114">Always include the table name in formulas (don't omit it, even though DAX lets you)</span></span>

## <a name="creating-calculated-columns"></a><span data-ttu-id="32ce4-115">การสร้างคอลัมน์จากการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="32ce4-115">Creating calculated columns</span></span>
<span data-ttu-id="32ce4-116">**คอลัมน์จากการคำนวณ** มีประโยชน์เมื่อคุณต้องการแบ่งส่วนหรือกรองค่า หรือถ้าคุณต้องการการคำนวณสำหรับทุกแถวในตารางของคุณ</span><span class="sxs-lookup"><span data-stu-id="32ce4-116">**Calculated columns** are useful when you want to slice or filter on the value, or if you want a calculation for every row in your table.</span></span>

<span data-ttu-id="32ce4-117">คุณสามารถสร้างคอลัมน์จากการคำนวณใน Power BI Desktop ได้โดยเลือก **คอลัมน์ใหม่** จากแท็บ **การวางรูปแบบ** วิธีที่ดีที่สุดคืออยู่ในมุมมอง **ข้อมูล** (แทนที่จะเป็นมุมมอง **รายงาน** หรือมุมมอง **ความสัมพันธ์**) เนื่องจากคุณจะเห็นคอลัมน์ใหม่ที่สร้างขึ้นและ **แถบสูตร** จะมีข้อมูลอยู่แล้วและพร้อมสำหรับสูตร DAX ของคุณ</span><span class="sxs-lookup"><span data-stu-id="32ce4-117">You can create calculated columns in Power BI Desktop by selecting **New Column** from the **Modeling** tab. It's best to be in **Data** view (rather than **Report** or **Relationships** view), since you can see the new column created and the **Formula Bar** is populated and ready for your DAX formula.</span></span>

![](media/7-2-dax-calculation-types/dax-calc-types_2a.png)

<span data-ttu-id="32ce4-118">เมื่อคุณเลือกปุ่ม **คอลัมน์ใหม่** **แถบสูตร** จะถูกเติมด้วยชื่อคอลัมน์พื้นฐาน (ที่คุณจะเปลี่ยนให้เข้ากับสูตร) และ **=** ตัวดำเนินการ และคอลัมน์ใหม่จะปรากฏขึ้นในตารางข้อมูลดังที่แสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="32ce4-118">Once you select the **New Column** button, the **Formula Bar** is populated with a basic column name (which you change to suit your formula, of course) and the **=** operator, and the new column appears in the data grid, as shown in the following image.</span></span>

![](media/7-2-dax-calculation-types/dax-calc-types_3.png)

<span data-ttu-id="32ce4-119">องค์ประกอบที่จำเป็นสำหรับคอลัมน์จากการคำนวณมีดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="32ce4-119">The required elements for a calculated column are the following:</span></span>

* <span data-ttu-id="32ce4-120">ชื่อคอลัมน์ใหม่</span><span class="sxs-lookup"><span data-stu-id="32ce4-120">a new column name</span></span>
* <span data-ttu-id="32ce4-121">ฟังก์ชันหรือนิพจน์อย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="32ce4-121">at least one function or expression</span></span>

<span data-ttu-id="32ce4-122">ถ้าคุณอ้างอิงตารางหรือคอลัมน์ในสูตรคอลัมน์จากการคำนวณของคุณ คุณจะไม่จำเป็นต้องระบุแถวในตาราง Power BI จะคำนวณคอลัมน์สำหรับแถวปัจจุบันในทุกการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="32ce4-122">If you reference a table or column in your calculated column formula, you do not need to specify a row in the table - Power BI calculates the column for the current row for each calculation.</span></span>

## <a name="creating-measures"></a><span data-ttu-id="32ce4-123">การสร้างหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="32ce4-123">Creating measures</span></span>
<span data-ttu-id="32ce4-124">ใช้**หน่วยวัด**เมื่อคุณคำนวณเปอร์เซ็นต์หรืออัตราส่วน หรือคุณต้องการการรวมที่ซับซ้อน</span><span class="sxs-lookup"><span data-stu-id="32ce4-124">Use a **measure** when you are calculating percentages or ratios, or you need complex aggregations.</span></span> <span data-ttu-id="32ce4-125">เมื่อต้องการสร้างการวัดโดยใช้สูตร DAX ให้เลือกปุ่ม **การวัดใหม่** จากแท็บ **การวางรูปแบบ** และเช่นเดียวกัน วิธีที่ดีที่สุดคืออยู่ในมุมมอง **ข้อมูล** ของ Power BI Desktop เนื่องจากมุมมองนี้จะแสดง **แถบสูตร** และทำให้ง่ายต่อการเขียนสูตร DAX ของคุณ</span><span class="sxs-lookup"><span data-stu-id="32ce4-125">To create a measure using a DAX formula, select the **New Measure** button from the **Modeling** tab. Again, it's best to be in the **Data** view of Power BI Desktop since it shows the **Formula Bar** and makes it easy to write your DAX formula.</span></span>

![](media/7-2-dax-calculation-types/dax-calc-types_4.png)

<span data-ttu-id="32ce4-126">ด้วย **การวัด** คุณจะเห็นไอคอนการวัดใหม่ปรากฏขึ้นในบานหน้าต่าง **เขตข้อมูล** พร้อมชื่อของการวัด</span><span class="sxs-lookup"><span data-stu-id="32ce4-126">With **measures**, you see a new measure icon appear in the **Fields** pane with the name of the measure.</span></span> <span data-ttu-id="32ce4-127">**แถบสูตร** จะมีชื่อสูตร DAX ของคุณอยู่แล้วเช่นเดียวกัน (คราวนี้ด้วยการวัดของคุณ)</span><span class="sxs-lookup"><span data-stu-id="32ce4-127">The **Formula Bar** is again populated with the name of your DAX formula (this time, with your measure).</span></span>

![](media/7-2-dax-calculation-types/dax-calc-types_5.png)

<span data-ttu-id="32ce4-128">องค์ประกอบที่จำเป็นสำหรับหน่วยวัดจะเหมือนกับของคอลัมน์จากการคำนวณ:</span><span class="sxs-lookup"><span data-stu-id="32ce4-128">The required elements for a measure are the same as they are for a calculated column:</span></span>

* <span data-ttu-id="32ce4-129">ชื่อการวัดใหม่</span><span class="sxs-lookup"><span data-stu-id="32ce4-129">a new measure name</span></span>
* <span data-ttu-id="32ce4-130">ฟังก์ชันหรือนิพจน์อย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="32ce4-130">at least one function or expression</span></span>

> <span data-ttu-id="32ce4-131">เนื้อหาวิดีโอโดย [Alberto Ferrari, SQBI](https://www.sqlbi.com/learning-dax)</span><span class="sxs-lookup"><span data-stu-id="32ce4-131">Video content courtesy of [Alberto Ferrari, SQLBI](https://www.sqlbi.com/learning-dax)</span></span>
> 
> 

