---
title: มุมมองแบบจำลองใน Power BI Desktop
description: มุมมองแบบจำลองใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: how-to
ms.date: 01/17/2020
LocalizationGroup: Model your data
ms.openlocfilehash: b257fc5af97cb16798cc27bdbdb92c1b63a65181
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96413782"
---
# <a name="work-with-model-view-in-power-bi-desktop"></a><span data-ttu-id="a1c98-103">ทำงานร่วมกับมุมมองแบบจำลองใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a1c98-103">Work with Model view in Power BI Desktop</span></span>

<span data-ttu-id="a1c98-104">*มุมมองแบบจำลอง* แสดงตาราง คอลัมน์ และความสัมพันธ์ทั้งหมดในรูปแบบข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="a1c98-104">*Model view* shows all of the tables, columns, and relationships in your model.</span></span> <span data-ttu-id="a1c98-105">ซึ่งจะเป็นประโยชน์โดยเฉพาะเมื่อรูปแบบของคุณมีความสัมพันธ์ระหว่างตารางต่าง ๆ ที่ซับซ้อน</span><span class="sxs-lookup"><span data-stu-id="a1c98-105">This view can be especially helpful when your model has complex relationships between many tables.</span></span>

<span data-ttu-id="a1c98-106">เลือกไอคอน **แบบจำลอง** ที่อยู่ใกล้กับด้านข้างของหน้าต่างเพื่อดูมุมมองของแบบจำลองที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="a1c98-106">Select the **Model** icon near the side of the window to see a view of the existing model.</span></span> <span data-ttu-id="a1c98-107">วางเมาส์เคอร์เซอร์ของคุณเหนือเส้นความสัมพันธ์เพื่อแสดงคอลัมน์ที่ใช้</span><span class="sxs-lookup"><span data-stu-id="a1c98-107">Hover your cursor over a relationship line to show the columns that are used.</span></span>

![มุมมองแบบจำลอง, Power BI Desktop](media/desktop-relationship-view/model-view-full-screen.png)

<span data-ttu-id="a1c98-109">ในรูป คุณสามารถเห็นว่าตาราง *ร้านค้า* มีคอลัมน์ *StoreKey* ที่เกี่ยวข้องกับตาราง *ยอดขาย* ซึ่งมีคอลัมน์ *StoreKey* เช่นเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="a1c98-109">In the figure, the *Stores* table has a *StoreKey* column that’s related to the *Sales* table, which also has a *StoreKey* column.</span></span> <span data-ttu-id="a1c98-110">ตารางทั้งสองมีความสัมพันธ์แบบ *กลุ่มต่อหนึ่ง* (\*: 1)</span><span class="sxs-lookup"><span data-stu-id="a1c98-110">The two tables have a *Many to One* (\*:1) relationship.</span></span> <span data-ttu-id="a1c98-111">ลูกศรที่กึ่งกลางเส้นแสดงทิศทางโฟลว์ของบริบทตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="a1c98-111">An arrow in the middle of the line shows the direction of the filter context flow.</span></span> <span data-ttu-id="a1c98-112">ลูกศรคู่หมายความว่า ทิศทางตัวกรองแบบไขว้ ถูกตั้งค่าเป็น *ทั้งสอง*</span><span class="sxs-lookup"><span data-stu-id="a1c98-112">The double arrows mean the cross-filter direction is set to *Both*.</span></span>

<span data-ttu-id="a1c98-113">คุณสามารถดับเบิลคลิกที่ความสัมพันธ์เพื่อเปิดรายการในกล่องโต้ตอบ **แก้ไขความสัมพันธ์**</span><span class="sxs-lookup"><span data-stu-id="a1c98-113">You can double-click a relationship to open it in the **Edit Relationship** dialog box.</span></span> <span data-ttu-id="a1c98-114">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับความสัมพันธ์ ดู[สร้าง และจัดการความสัมพันธ์ใน Power BI Desktop](desktop-create-and-manage-relationships.md)</span><span class="sxs-lookup"><span data-stu-id="a1c98-114">To learn more about relationships, see [Create and manage relationships in Power BI Desktop](desktop-create-and-manage-relationships.md).</span></span>
