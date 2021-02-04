---
ms.openlocfilehash: fa6296485897b983c3ca4044ffa2875de3326dec
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2019
ms.locfileid: "61265196"
---
<span data-ttu-id="70d4d-101">ขณะที่ Power BI สามารถนำเข้าข้อมูลของคุณได้จากเกือบทุกแหล่งข้อมูล เครื่องมือการจัดรูปแบบการแสดงข้อมูลและการวางรูปแบบก็สามารถทำงานได้อย่างดีเยี่ยมกับข้อมูลที่เป็นคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="70d4d-101">While Power BI can import your data from almost any source, its visualization and modeling tools work best with columnar data.</span></span> <span data-ttu-id="70d4d-102">ในบางครั้ง ข้อมูลของคุณจะถูกจัดรูปแบบให้เป็นคอลัมน์ง่ายๆ ซึ่งมักจะเกิดขึ้นเมื่อคุณใช้สเปรดชีต Excel ซึ่งมีเค้าโครงตารางลักษณะสวยงามที่ไม่จำเป็นต้องปรับสำหรับคิวรีอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="70d4d-102">Sometimes your data will not be formatted in simple columns, which is often the case with Excel spreadsheets, where a table layout that looks good to the human eye is not necessarily optimal for automated queries.</span></span> <span data-ttu-id="70d4d-103">ตัวอย่างเช่น สเปรดชีตต่อไปนี้มีส่วนที่ขยายเป็นหลายคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="70d4d-103">For example, the following spreadsheet has headers that span multiple columns.</span></span>

![](media/1-5-cleaning-irregular-data/1-5_1.png)

<span data-ttu-id="70d4d-104">โชคดีที่ Power BI มีเครื่องมือในการแปลงตารางหลายคอลัมน์ให้เป็นชุดข้อมูลที่คุณสามารถใช้งานได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="70d4d-104">Fortunately, Power BI has tools to quickly transform multi-column tables into datasets that you can use.</span></span>

## <a name="transpose-data"></a><span data-ttu-id="70d4d-105">สลับเปลี่ยนแถวข้อมูลกับคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="70d4d-105">Transpose data</span></span>
<span data-ttu-id="70d4d-106">ตัวอย่างเช่น เมื่อใช้ **สลับเปลี่ยนแถวกับคอลัมน์** ใน **ตัวแก้ไขคิวรี** คุณจะสามารถพลิกข้อมูล (เปลี่ยนคอลัมน์ให้เป็นแถว และเปลี่ยนแถวให้เป็นคอลัมน์) เพื่อให้คุณสามารถแบ่งข้อมูลเป็นรูปแบบที่คุณสามารถจัดการได้</span><span class="sxs-lookup"><span data-stu-id="70d4d-106">For example, using **Transpose** in **Query Editor**, you can flip data (turn columns to rows, and rows into columns) so you can break data down into formats that you can manipulate.</span></span>

![](media/1-5-cleaning-irregular-data/1-5_2.png)

<span data-ttu-id="70d4d-107">เมื่อคุณทำเช่นนี้เพียงไม่กี่ครั้ง ตามที่ได้อธิบายไว้ในวิดีโอ ตารางของคุณจะเริ่มมีลักษณะที่ Power BI สามารถนำไปใช้งานได้ง่ายยิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="70d4d-107">Once you do that a few times, as described in the video, your table begins to shape into something that Power BI can more easily work with.</span></span>

## <a name="format-data"></a><span data-ttu-id="70d4d-108">จัดรูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="70d4d-108">Format data</span></span>
<span data-ttu-id="70d4d-109">คุณยังอาจต้องจัดรูปแบบข้อมูล เพื่อให้ Power BI สามารถจัดประเภทและระบุข้อมูลได้อย่างถูกต้องเมื่อนำเข้า</span><span class="sxs-lookup"><span data-stu-id="70d4d-109">You also may need to format data, so Power BI can properly categorize and identify that data once it's imported.</span></span>

<span data-ttu-id="70d4d-110">ด้วยการแปลงต่างๆ รวมถึง *การเพิ่มระดับแถวให้เป็นส่วนหัว* เพื่อแบ่งส่วนหัว การใช้ **เติม** เพื่อเปลี่ยนค่า *Null* ให้เป็นค่าที่อยู่ทางด้านบนหรือด้านล่างของคอลัมน์ที่ระบุ และ **ยกเลิกคอลัมน์** คุณสามารถล้างข้อมูลนั้นไปเป็นชุดข้อมูลที่คุณสามารถใช้ใน Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="70d4d-110">With a handful of transformations, including *promoting rows into headers* into to break headers, using **Fill** to turn *null* values into the values found above or below in a given column, and **Unpivot Columns**, you can cleanse that data into a dataset that you can use in Power BI.</span></span>

![](media/1-5-cleaning-irregular-data/1-5_3.png)

<span data-ttu-id="70d4d-111">เมื่อใช้ Power BI คุณสามารถทดลองใช้การแปลงเหล่านี้กับข้อมูลของคุณ และกำหนดชนิดข้อมูลที่จะทำเป็นรูปแบบตารางที่ทำงานกับ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="70d4d-111">With Power BI, you can experiment with these transformations on your data, and determine which types get your data into the columnar format that lets Power BI work with it.</span></span> <span data-ttu-id="70d4d-112">และจำไว้ว่า การกระทำทุกอย่างที่คุณทำจะถูกบันทึกไว้ในส่วนขั้นตอนที่ถูกนำไปใช้ของตัวแก้ไขคิวรี ดังนั้น ถ้าการแปลงไม่ทำงานตามที่คุณคาดไว้ คุณสามารถคลิก **x** ที่อยู่ถัดจากขั้นตอน แล้วเลิกทำได้</span><span class="sxs-lookup"><span data-stu-id="70d4d-112">And remember, all actions you take are recorded in the Applied Steps section of Query Editor, so if a transformation doesn't work the way you intended, you can simply click the **x** next to the step, and undo it.</span></span>

![](media/1-5-cleaning-irregular-data/1-5_5.png)

## <a name="create-visuals"></a><span data-ttu-id="70d4d-113">สร้างการแสดงผลด้วยภาพ</span><span class="sxs-lookup"><span data-stu-id="70d4d-113">Create visuals</span></span>
<span data-ttu-id="70d4d-114">เมื่อข้อมูลของคุณอยู่ในรูปแบบที่ Power BI สามารถใช้ได้ ไม่ว่าจะด้วยการแปลงและการล้างข้อมูล คุณสามารถเริ่มสร้างการแสดงข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="70d4d-114">Once your data is in a format that Power BI can use, by transforming and cleansing the data, you can begin to create visuals.</span></span>

![](media/1-5-cleaning-irregular-data/1-5_4.png)

## <a name="next-steps"></a><span data-ttu-id="70d4d-115">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="70d4d-115">Next steps</span></span>
<span data-ttu-id="70d4d-116">**ยินดีด้วย!**</span><span class="sxs-lookup"><span data-stu-id="70d4d-116">**Congratulations!**</span></span> <span data-ttu-id="70d4d-117">คุณได้สำเร็จส่วนนี้ของหลักสูตร **การเรียนรู้พร้อมคำแนะนำ** สำหรับ Power BI แล้ว</span><span class="sxs-lookup"><span data-stu-id="70d4d-117">You've completed this section of the **Guided Learning** course for Power BI.</span></span> <span data-ttu-id="70d4d-118">ในตอนนี้ คุณทราบวิธีการ**รับข้อมูล**เข้าสู่ Power BI Desktop และวิธีการ*จัดรูปทรง*หรือ*แปลง*ข้อมูลนั้น เพื่อให้คุณสามารถสร้างการแสดงข้อมูลที่ดูน่าสนใจได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="70d4d-118">You now know how to **get data** into Power BI Desktop, and how to *shape* or *transform* that data, so you can create compelling visuals.</span></span>

<span data-ttu-id="70d4d-119">ขั้นตอนถัดไปในการเรียนรู้การทำงานของ Power BI และการทำงานที่เหมาะ*สำหรับคุณ*คือการทำความเข้าใจสิ่งที่ใช้ใน**การวางรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="70d4d-119">The next step in learning how Power BI works, and how to make it work *for you*, is to understand what goes into **modeling**.</span></span> <span data-ttu-id="70d4d-120">ตามที่คุณได้เรียนรู้ **ชุดข้อมูล**คือโครงสร้างพื้นฐานของ Power BI แต่บางชุดข้อมูลอาจซับซ้อนและยึดตามแหล่งข้อมูลจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="70d4d-120">As you learned, a **dataset** is a basic building block of Power BI, but some datasets can be complex and based on many different sources of data.</span></span> <span data-ttu-id="70d4d-121">และในบางครั้ง คุณต้องเพิ่มสัมผัสพิเศษของคุณเอง (หรือ*เขตข้อมูล*) ให้กับชุดข้อมูลที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="70d4d-121">And sometimes, you need to add your own special touch (or *field*) to the dataset you create.</span></span>

<span data-ttu-id="70d4d-122">คุณจะได้เรียนรู้เกี่ยวกับ**การวางรูปแบบ** และสิ่งอื่นๆ อีกมากมายในส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="70d4d-122">You'll learn about **modeling**, and a whole lot more, in the next section.</span></span> <span data-ttu-id="70d4d-123">เจอกันที่นั่น!</span><span class="sxs-lookup"><span data-stu-id="70d4d-123">See you there!</span></span>

