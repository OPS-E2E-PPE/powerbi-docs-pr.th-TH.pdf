---
ms.openlocfilehash: 5bc0d3bbfb2c2b67b56e6406646f6131a360b97d
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/05/2020
ms.locfileid: "73800173"
---
<span data-ttu-id="8fceb-101">ข้อแตกต่างหลักอย่างหนึ่งระหว่างภาษาสูตรของ **DAX** และ Excel คือ DAX อนุญาตให้คุณผ่าน*ทั้งตาราง*ได้ระหว่างนิพจน์ แทนที่จะถูกจำกัดอยู่ที่ค่าเดี่ยว</span><span class="sxs-lookup"><span data-stu-id="8fceb-101">One significant difference between **DAX** and the Excel formula language is that DAX allows you to pass *entire tables* between expressions, rather than being constrained to a single value.</span></span> <span data-ttu-id="8fceb-102">ผลกระทบใหญ่อย่างหนึ่งคือ DAX อนุญาตให้คุณกรองตารางในนิพจน์ได้ จากนั้น DAX จะทำงานกับชุดค่าที่ได้รับการกรองแล้ว</span><span class="sxs-lookup"><span data-stu-id="8fceb-102">One powerful effect is that DAX allows you to filter tables in its expressions, then work with the filtered set of values.</span></span>

![](media/7-6-dax-tables-and-filtering/dax-tables-filtering_1.png)

<span data-ttu-id="8fceb-103">ด้วย DAX คุณสามารถสร้างตารางที่ได้รับการคำนวณใหม่ทั้งตาราง จากนั้นทำกับตารางนั้นเหมือนเป็นตารางอื่นๆ ได้ รวมถึงการสร้างความสัมพันธ์ระหว่างตารางนั้นกับตารางอื่นๆ ในรูปแบบข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="8fceb-103">With DAX, you can create entirely new calculated tables and then treat them like any other table - including creating relationships between them and other tables in your data model.</span></span>

## <a name="dax-table-functions"></a><span data-ttu-id="8fceb-104">ฟังก์ชันตารางของ DAX</span><span class="sxs-lookup"><span data-stu-id="8fceb-104">DAX table functions</span></span>
<span data-ttu-id="8fceb-105">DAX มีชุดฟังก์ชัน**ตาราง**จำนวนมาก รวมถึงฟังก์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8fceb-105">DAX has a rich set of **table** functions, including the following:</span></span>

* <span data-ttu-id="8fceb-106">FILTER</span><span class="sxs-lookup"><span data-stu-id="8fceb-106">FILTER</span></span>
* <span data-ttu-id="8fceb-107">ALL</span><span class="sxs-lookup"><span data-stu-id="8fceb-107">ALL</span></span>
* <span data-ttu-id="8fceb-108">VALUES</span><span class="sxs-lookup"><span data-stu-id="8fceb-108">VALUES</span></span>
* <span data-ttu-id="8fceb-109">DISTINCT</span><span class="sxs-lookup"><span data-stu-id="8fceb-109">DISTINCT</span></span>
* <span data-ttu-id="8fceb-110">RELATEDTABLE</span><span class="sxs-lookup"><span data-stu-id="8fceb-110">RELATEDTABLE</span></span>

<span data-ttu-id="8fceb-111">ฟังก์ชันเหล่านี้จะส่งกลับทั้งตาราง แทนที่จะเป็นค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8fceb-111">These functions return a full table rather than a value.</span></span> <span data-ttu-id="8fceb-112">โดยทั่วไป คุณจะใช้ผลลัพธ์ของฟังก์ชัน**ตาราง**ในการวิเคราะห์เพิ่มเติมซึ่งเป็นส่วนหนึ่งของนิพจน์ที่ใหญ่กว่า แทนที่จะใช้ตารางที่ถูกส่งกลับมาเป็นค่าสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="8fceb-112">Typically you'll use the results of a **table** function in further analysis as part of a greater expression, rather than using that returned table a final value.</span></span> <span data-ttu-id="8fceb-113">โปรดทราบว่าเมื่อคุณใช้ฟังก์ชันตาราง ผลลัพธ์จะสืบต่อความสัมพันธ์ของคอลัมน์มาด้วย</span><span class="sxs-lookup"><span data-stu-id="8fceb-113">It's important to note that When you use a table function, the results inherit the relationships of their columns.</span></span>

<span data-ttu-id="8fceb-114">คุณสามารถผสมฟังก์ชันตารางในนิพจน์ของคุณได้ ตราบใดที่แต่ละฟังก์ชันใช้หนึ่งตารางและส่งกลับหนึ่งตาราง</span><span class="sxs-lookup"><span data-stu-id="8fceb-114">You can mix table functions in your expression, as long as each function uses a table and returns a table.</span></span> <span data-ttu-id="8fceb-115">ตัวอย่างเช่น ลองพิจารณานิพจน์ DAX ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8fceb-115">For example, consider the following DAX expression:</span></span>

    FILTER (ALL (Table), Condition)

<span data-ttu-id="8fceb-116">นิพจน์ดังกล่าวจะใส่ตัวกรองลงในทั้ง*ตาราง* โดยไม่สนใจเนื้อหาของตัวกรองใดๆ ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="8fceb-116">That expression would put a filter over the entirety of *Table*, ignoring any current filter content.</span></span>

<span data-ttu-id="8fceb-117">ฟังก์ชัน DISTINCT จะส่งกลับค่าเฉพาะของคอลัมน์ที่มองเห็นได้ในบริบทในปัจจุบันเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="8fceb-117">The DISTINCT function returns the distinct values of a column that are also visible in the current context.</span></span> <span data-ttu-id="8fceb-118">ดังนั้นในการใช้นิพจน์ DAX ดังกล่าว การใช้ **ALL** ในนิพจน์นั้นจะละเว้นตัวกรอง ขณะที่การแทนที่ **ALL** ด้วย **DISTINCT** จะดูตัวกรองเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="8fceb-118">So to use the above DAX expression example, using **ALL** in that expression ignores filters, while replacing **ALL** with **DISTINCT** would observe them.</span></span>

## <a name="counting-values-with-dax"></a><span data-ttu-id="8fceb-119">การนับค่าด้วย DAX</span><span class="sxs-lookup"><span data-stu-id="8fceb-119">Counting values with DAX</span></span>
<span data-ttu-id="8fceb-120">คำถามโดยทั่วไปคำถามหนึ่งที่ผู้สร้างรายงาน Power BI ต้องการตอบมีใจความดังนี้:</span><span class="sxs-lookup"><span data-stu-id="8fceb-120">One common question that Power BI report builders want to answer is the following:</span></span>

* <span data-ttu-id="8fceb-121">ฉันมีค่าจำนวนเท่าใดในคอลัมน์นี้</span><span class="sxs-lookup"><span data-stu-id="8fceb-121">How many values do I have for this column?</span></span>

<span data-ttu-id="8fceb-122">นั่นอาจเป็นคำถามที่ตอบไม่ยากหากมีตารางเปิดอยู่ตรงหน้าคุณ แต่ DAX จะเข้าถึงคำตอบในวิธีที่ต่างออกไป โดยเฉพาะในกรณีที่มีความสัมพันธ์ระหว่างตาราง</span><span class="sxs-lookup"><span data-stu-id="8fceb-122">That may be a simple question to answer with a table displayed in front of you, but DAX approaches in a different way, particularly when there's a relationship between tables.</span></span>

<span data-ttu-id="8fceb-123">ตัวอย่างเช่น Power BI และ DAX จะรวมค่าที่ไม่ได้ถูกทำดัชนีโดยอ้างอิงกันอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="8fceb-123">For example, Power BI and DAX includes values that are not properly cross-indexed.</span></span> <span data-ttu-id="8fceb-124">ถ้าความสัมพันธ์ที่เข้ามาถูกตัดขาด DAX จะเพิ่มแถวใหม่ลงในตารางที่เกี่ยวข้องที่มีช่องว่างในทุกเขตข้อมูล แล้วเชื่อมโยงแถวใหม่นั้นกับแถวที่ไม่ถูกทำดัชนีเพื่อรับรองความถูกต้องของการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="8fceb-124">If the incoming relationship is broken, DAX adds a new row to the related table that has blanks in every field, and links that new row to the unindexed row to guarantee referential integrity.</span></span> <span data-ttu-id="8fceb-125">ถ้าฟังก์ชันของคุณมีแถวเปล่า เช่นในกรณีที่เกิดขึ้นบ่อยเมื่อใช้ **ALL** แถวเปล่าเหล่านั้นจะถูกรวมในค่าที่ส่งกลับของคอลัมน์นั้น</span><span class="sxs-lookup"><span data-stu-id="8fceb-125">If your function includes blank rows, such as is often the case when using **ALL**, those blank rows will then be included in the number of values returned for that column.</span></span>

<span data-ttu-id="8fceb-126">คุณยังสามารถสร้างตารางที่ได้รับการคำนวณใหม่ทั้งตารางโดยใช้ฟังก์ชัน DAX ได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="8fceb-126">You can also create entire calculated tables using DAX functions.</span></span> <span data-ttu-id="8fceb-127">ตารางที่ได้รับการคำนวณที่สร้างโดยใช้ DAX จำเป็นต้องมีฟังก์ชัน **NAME** และ **TABLE**</span><span class="sxs-lookup"><span data-stu-id="8fceb-127">Calculated tables created using DAX require a **NAME** and a **TABLE** function.</span></span> <span data-ttu-id="8fceb-128">ตารางที่ได้รับการคำนวณสามารถนำไปใช้ได้เหมือนกับตารางอื่นๆ รวมถึงการสร้างความสัมพันธ์ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="8fceb-128">Calculated tables can be used like any other table, including establishing relationships.</span></span>

> <span data-ttu-id="8fceb-129">เนื้อหาวิดีโอโดย [Alberto Ferrari, SQBI](https://www.sqlbi.com/learning-dax)</span><span class="sxs-lookup"><span data-stu-id="8fceb-129">Video content courtesy of [Alberto Ferrari, SQLBI](https://www.sqlbi.com/learning-dax)</span></span>
> 
> 

