---
ms.openlocfilehash: b1658a9351c05a8673c6cc582a4e54ad982791fc
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2019
ms.locfileid: "61257086"
---
<span data-ttu-id="9cb89-101">Power BI ช่วยให้คุณสามารถตั้งค่าความสัมพันธ์ที่มองเห็นได้ระหว่างตารางและองค์ประกอบ</span><span class="sxs-lookup"><span data-stu-id="9cb89-101">Power BI allows you to visually set the relationship between tables or elements.</span></span> <span data-ttu-id="9cb89-102">เมื่อต้องการดูมุมมองแผนผังของข้อมูลของคุณ ให้ใช้ **มุมมองความสัมพันธ์** ที่อยู่ทางด้านซ้ายสุดของหน้าจอ ถัดจากพื้นที่ทำงานของรายงาน</span><span class="sxs-lookup"><span data-stu-id="9cb89-102">To see a diagrammatic view of your data, use the **Relationship view**, found on the far left side of the screen next to the Report canvas.</span></span>

![](media/2-2-manage-data-relationships/2-2_1.png)

<span data-ttu-id="9cb89-103">จากมุมมอง**ความสัมพันธ์** คุณจะเห็นบล็อกที่แสดงแทนแต่ละตารางและคอลัมน์ และเส้นที่แสดงความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="9cb89-103">From the **Relationships** view, you can see a block that represents each table and its columns, and lines between them to represent relationships.</span></span>

<span data-ttu-id="9cb89-104">การเพิ่มและการลบความสัมพันธ์สามารถทำได้ง่าย</span><span class="sxs-lookup"><span data-stu-id="9cb89-104">Adding and removing relationships is simple.</span></span> <span data-ttu-id="9cb89-105">เมื่อต้องการลบความสัมพันธ์ ให้คลิกขวา แล้วเลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="9cb89-105">To remove a relationship, right-click on it and select **Delete**.</span></span> <span data-ttu-id="9cb89-106">เมื่อต้องการสร้างความสัมพันธ์ ให้ลากแล้วปล่อยเขตข้อมูลที่คุณต้องการเชื่อมโยงระหว่างตาราง</span><span class="sxs-lookup"><span data-stu-id="9cb89-106">To create a relationship, drag and drop the fields that you want to link between tables.</span></span>

![](media/2-2-manage-data-relationships/2-2_2.png)

<span data-ttu-id="9cb89-107">เมื่อต้องการซ่อนตารางหรือคอลัมน์จากรายงานของคุณ ให้คลิกขวาในมุมมองความสัมพันธ์ แล้วเลือก **ซ่อนในมุมมองรายงาน**</span><span class="sxs-lookup"><span data-stu-id="9cb89-107">To hide a table or individual column from your report, right-click on it in the Relationship view and select **Hide in Report View**.</span></span>

![](media/2-2-manage-data-relationships/2-2_3.png)

<span data-ttu-id="9cb89-108">สำหรับมุมมองโดยละเอียดของความสัมพันธ์ของข้อมูลของคุณ ให้เลือก **จัดการความสัมพันธ์** ในแท็บ **หน้าแรก** กล่องโต้ตอบ **จัดการความสัมพันธ์** จะเปิดขึ้น และแสดงความสัมพันธ์เป็นรายการแทนที่จะเป็นแผนผังรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="9cb89-108">For a more detailed view of your data relationships, select **Manage Relationships** in the **Home** tab. This will open the **Manage Relationships** dialog, which displays your relationships as a list instead of a visual diagram.</span></span> <span data-ttu-id="9cb89-109">จากที่นี่ คุณสามารถเลือก **ตรวจหาโดยอัตโนมัติ** เพื่อค้นหาความสัมพันธ์ในข้อมูลใหม่หรือข้อมูลที่มีการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="9cb89-109">From here you can select **Autodetect** to find relationships in new or updated data.</span></span> <span data-ttu-id="9cb89-110">เลือก **แก้ไข** ในกล่องโต้ตอบ **จัดการความสัมพันธ์** เพื่อแก้ไขความสัมพันธ์ของคุณด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9cb89-110">Select **Edit** in the **Manage Relationships** dialog to manually edit your relationships.</span></span> <span data-ttu-id="9cb89-111">นอกจากนี้ คุณจะพบตัวเลือกขั้นสูงเพื่อตั้งค่า*คาร์ดินาลลิตี้* และทิศทาง*ข้ามตัวกรอง*ของความสัมพันธ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="9cb89-111">This is also where you can find advanced options to set the *Cardinality* and *Cross-filter* direction of your relationships.</span></span>

![](media/2-2-manage-data-relationships/2-2_4.png)

<span data-ttu-id="9cb89-112">ตัวเลือกของคุณสำหรับ คาร์ดินาลลิตี้ คือ *กลุ่มต่อหนึ่ง* และ *หนึ่งต่อหนึ่ง*</span><span class="sxs-lookup"><span data-stu-id="9cb89-112">Your options for Cardinality are *Many to One*, and *One to One*.</span></span> <span data-ttu-id="9cb89-113">*กลุ่มต่อหนึ่ง* คือข้อเท็จจริงของความสัมพันธ์ชนิดขนาด ตัวอย่างเช่น ตารางยอดขายที่มีหลายแถวต่อหนึ่งผลิตภัณฑ์ที่จับคู่กับผลิตภัณฑ์รายการในตารางในแถวที่ไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="9cb89-113">*Many to One* is the fact to dimension type relationship, for example a sales table with multiple rows per product being matched up with a table listing products in their own unique row.</span></span> <span data-ttu-id="9cb89-114">*หนึ่งต่อหนึ่ง* มักจะใช้สำหรับการเชื่อมต่อรายการเดียวในตารางอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="9cb89-114">*One to One* is used often for linking single entries in reference tables.</span></span>

<span data-ttu-id="9cb89-115">ตามค่าเริ่มต้น ความสัมพันธ์จะถูกตั้งค่าให้ข้ามตัวกรองในทั้งสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="9cb89-115">By default, relationships will be set to cross-filter in both directions.</span></span> <span data-ttu-id="9cb89-116">การข้ามตัวกรองเพียงทิศทางเดียวจะจำกัดความสามารถการวางรูปแบบบางอย่างในความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="9cb89-116">Cross-filtering in just one direction limited some of the modeling capabilities in a relationship.</span></span>

<span data-ttu-id="9cb89-117">การตั้งค่าความสัมพันธ์ที่แม่นยำระหว่างข้อมูลของคุณจะช่วยให้คุณสามารถสร้างการคำนวณที่ซับซ้อนในหลายองค์ประกอบข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="9cb89-117">Setting accurate relationships between your data allows you to create complex calculations across multiple data elements.</span></span>

