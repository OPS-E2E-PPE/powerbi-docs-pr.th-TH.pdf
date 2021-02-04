---
ms.openlocfilehash: 679c3e8c3d94c93899e9dcfae1e57f4b678fb218
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/05/2020
ms.locfileid: "73800170"
---
<span data-ttu-id="e5468-101">Power BI ให้คุณสร้างความสัมพันธ์ระหว่างหลายตาราง รวมถึงตารางที่มาจากแหล่งข้อมูลที่แตกต่างกันโดยสิ้นเชิง</span><span class="sxs-lookup"><span data-stu-id="e5468-101">Power BI lets you create relationships among multiple tables, including tables that come from completely different data sources.</span></span> <span data-ttu-id="e5468-102">คุณสามารถดูความสัมพันธ์เหล่านั้นสำหรับรูปแบบข้อมูลใดๆ ได้ในมุมมอง **ความสัมพันธ์** ของ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="e5468-102">You can see those relationships for any data model in the **Relationships** view of Power BI Desktop.</span></span>

![](media/7-5-table-relationships-and-dax/dax-relationships_1.png)

## <a name="dax-relational-functions"></a><span data-ttu-id="e5468-103">ฟังก์ชันความสัมพันธ์ของ DAX</span><span class="sxs-lookup"><span data-stu-id="e5468-103">DAX relational functions</span></span>
<span data-ttu-id="e5468-104">DAX มี**ฟังก์ชันความสัมพันธ์**ที่ทำให้คุณสามารถโต้ตอบกับตารางที่คุณได้สร้างความสัมพันธ์ไว้ได้</span><span class="sxs-lookup"><span data-stu-id="e5468-104">DAX has **relational functions** that enable you to interact with tables that have established relationships.</span></span>

<span data-ttu-id="e5468-105">คุณสามารถส่งกลับค่าของคอลัมน์ หรือคุณสามารถส่งกลับแถวทั้งหมดในความสัมพันธ์ได้โดยใช้ฟังก์ชัน DAX</span><span class="sxs-lookup"><span data-stu-id="e5468-105">You can return the value of a column, or you can return all rows in a relationship using DAX functions.</span></span>

<span data-ttu-id="e5468-106">ตัวอย่างเช่น ฟังก์ชัน **RELATED** จะติดตามความสัมพันธ์แล้วส่งกลับค่าของคอลัมน์หนึ่ง ขณะที่ **RELATEDTABLE** จะติดตามความสัมพันธ์แล้วส่งกลับทั้งตารางที่ถูกกรองให้เหลือแต่แถวที่เกี่ยวข้องแล้ว</span><span class="sxs-lookup"><span data-stu-id="e5468-106">For example, the **RELATED** function follows relationships and returns the value of a column, while **RELATEDTABLE** follows relationships, and returns an entire table that is filtered to include only related rows.</span></span>

![](media/7-5-table-relationships-and-dax/dax-relationships_2.png)

<span data-ttu-id="e5468-107">ฟังก์ชัน **RELATED** ทำงานกับความสัมพันธ์แบบ*กลุ่มต่อหนึ่ง* ขณะที่ **RELATEDTABLE** มีไว้สำหรับความสัมพันธ์แบบ*หนึ่งต่อกลุ่ม*</span><span class="sxs-lookup"><span data-stu-id="e5468-107">The **RELATED** function works on *many-to-one* relationships, while **RELATEDTABLE** is for *one-to-many* relationships.</span></span>

<span data-ttu-id="e5468-108">คุณสามารถใช้ฟังก์ชันความสัมพันธ์เพื่อสร้างนิพจน์ที่มีค่าในหลายตารางได้</span><span class="sxs-lookup"><span data-stu-id="e5468-108">You can use relational functions to build expressions that include values across multiple tables.</span></span> <span data-ttu-id="e5468-109">DAX จะส่งกลับผลลัพธ์ด้วยฟังก์ชันเหล่านี้ไม่ว่าห่วงโซ่ความสัมพันธ์จะยาวเพียงใด</span><span class="sxs-lookup"><span data-stu-id="e5468-109">DAX will return a result with these functions, regardless of the length of the chain of the relationship.</span></span>

> <span data-ttu-id="e5468-110">เนื้อหาวิดีโอโดย [Alberto Ferrari, SQBI](https://www.sqlbi.com/learning-dax)</span><span class="sxs-lookup"><span data-stu-id="e5468-110">Video content courtesy of [Alberto Ferrari, SQLBI](https://www.sqlbi.com/learning-dax)</span></span>
> 
> 

