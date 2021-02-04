---
title: เชื่อมต่อกับข้อมูลใน Power BI Desktop
description: เชื่อมต่อกับข้อมูลใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 01/21/2020
LocalizationGroup: Connect to data
ms.openlocfilehash: a9fdb4e2ebd71d652c66220ad4a70473ef6dd764
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411298"
---
# <a name="connect-to-data-sources-in-power-bi-desktop"></a><span data-ttu-id="3e568-103">เชื่อมต่อกับแหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3e568-103">Connect to data sources in Power BI Desktop</span></span>

<span data-ttu-id="3e568-104">ด้วย Power BI Desktop คุณสามารถเชื่อมต่อไปทั่วโลกแห่งข้อมูลที่กำลังขยายตัวได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="3e568-104">With Power BI Desktop, you can easily connect to the ever expanding world of data.</span></span> <span data-ttu-id="3e568-105">ถ้าคุณไม่มี Power BI Desktop คุณสามารถ[ดาวน์โหลด](https://go.microsoft.com/fwlink/?LinkID=521662)และติดตั้งได้</span><span class="sxs-lookup"><span data-stu-id="3e568-105">If you don’t have Power BI Desktop, you can [download](https://go.microsoft.com/fwlink/?LinkID=521662) and install it.</span></span>

<span data-ttu-id="3e568-106">ใน Power BI Desktop จะมีแหล่งข้อมูลต่าง ๆ *ทุกประเภท* ที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3e568-106">There are *all sorts* of data sources available in Power BI Desktop.</span></span> <span data-ttu-id="3e568-107">รูปต่อไปนี้แสดงวิธีการเชื่อมต่อกับข้อมูลโดยการเลือก **รับข้อมูล** > **อื่น ๆ** > **เว็บ**</span><span class="sxs-lookup"><span data-stu-id="3e568-107">The following image shows how to connect to data, by selecting **Get Data** > **Other** > **Web**.</span></span>

![รับข้อมูลจากเว็บ](media/desktop-connect-to-data/get-data-from-the-web.png)

## <a name="example-of-connecting-to-data"></a><span data-ttu-id="3e568-109">ตัวอย่างการเชื่อมต่อกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3e568-109">Example of connecting to data</span></span>

<span data-ttu-id="3e568-110">สำหรับตัวอย่างนี้ เราจะเชื่อมต่อไปยัง **Web** แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3e568-110">For this example, we'll connect to a **Web** data source.</span></span>

<span data-ttu-id="3e568-111">สมมติว่าคุณกำลังจะเกษียณ</span><span class="sxs-lookup"><span data-stu-id="3e568-111">Imagine you’re retiring.</span></span> <span data-ttu-id="3e568-112">คุณต้องการใช้ชีวิตในสถานที่ที่มีแสงแดดเยอะ ๆ มีการเก็บภาษีที่เหมาะสม และมีการดูแลสุขภาพที่ดี</span><span class="sxs-lookup"><span data-stu-id="3e568-112">You want to live where there’s lots of sunshine, preferable taxes, and good health care.</span></span> <span data-ttu-id="3e568-113">หรือ...</span><span class="sxs-lookup"><span data-stu-id="3e568-113">Or…</span></span> <span data-ttu-id="3e568-114">คุณอาจจะเป็นนักวิเคราะห์ข้อมูล และคุณต้องการให้ข้อมูลเหล่านั้นเป็นประโยชน์ต่อลูกค้าของคุณ เช่น ช่วยลูกค้าผู้ผลิตเสื้อกันฝนในการตั้งเป้าหมายการขายในสถานที่ที่มีฝนตก *เยอะ*</span><span class="sxs-lookup"><span data-stu-id="3e568-114">perhaps you’re a data analyst, and you want that information to help your customers, as in, help your raincoat manufacturing client target sales where it rains a *lot*.</span></span>

<span data-ttu-id="3e568-115">ไม่ว่าวิธีใด คุณจะพบแหล่งข้อมูลบนเว็บที่มีข้อมูลที่น่าสนใจเกี่ยวกับหัวข้อเหล่านั้น และอื่น ๆ อีกมาก</span><span class="sxs-lookup"><span data-stu-id="3e568-115">Either way, you find a Web resource that has interesting data about those topics, and more:</span></span>

[https://www.bankrate.com/finance/retirement/best-places-retire-how-state-ranks.aspx](https://www.bankrate.com/finance/retirement/best-places-retire-how-state-ranks.aspx)

<span data-ttu-id="3e568-116">เลือก **รับข้อมูล** > **อื่น ๆ** > **เว็บ**</span><span class="sxs-lookup"><span data-stu-id="3e568-116">Select **Get Data** > **Other** > **Web**.</span></span> <span data-ttu-id="3e568-117">ใน **จากเว็บ** ให้ใส่ที่อยู่</span><span class="sxs-lookup"><span data-stu-id="3e568-117">In **From Web**, enter the address.</span></span>

![ป้อนที่อยู่เแหล่งที่มาของเว็บ](media/desktop-connect-to-data/connecttodata_3.png)

<span data-ttu-id="3e568-119">เมื่อคุณเลือก **ตกลง** ฟังก์ชันการทำงานของ Power BI Desktop ของ *Query* จะทำงาน</span><span class="sxs-lookup"><span data-stu-id="3e568-119">When you select **OK**, the *Query* functionality of Power BI Desktop goes to work.</span></span> <span data-ttu-id="3e568-120">Power BI Desktop ติดต่อแหล่งข้อมูลเว็บ และหน้าต่าง **ตัวนำทาง** ส่งกลับผลลัพธ์ของสิ่งที่พบบนหน้าเว็บ</span><span class="sxs-lookup"><span data-stu-id="3e568-120">Power BI Desktop contacts the Web resource, and the **Navigator** window returns the results of what it found on that Web page.</span></span> <span data-ttu-id="3e568-121">ในกรณีนี้ จะพบตารางและเอกสารโดยรวม</span><span class="sxs-lookup"><span data-stu-id="3e568-121">In this case, it found a table and the overall Document.</span></span> <span data-ttu-id="3e568-122">เราสนใจตาราง ดังนั้นเราเลือกตารางจากรายการ</span><span class="sxs-lookup"><span data-stu-id="3e568-122">We're interested in the table, so we select it from the list.</span></span> <span data-ttu-id="3e568-123">หน้าต่าง **ตัวนำทาง** จะแสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3e568-123">The **Navigator** window displays a preview.</span></span>

![การแสดงตัวอย่างข้อมูลในตัวนำทาง](media/desktop-connect-to-data/datasources_fromnavigatordialog.png)

<span data-ttu-id="3e568-125">ในตอนนี้ คุณสามารถแก้ไขการคิวรีก่อนทำการโหลดตาราง โดยการเลือก **แปลงข้อมูล** จากด้านล่างของหน้าต่าง หรือเพียงแค่โหลดตาราง</span><span class="sxs-lookup"><span data-stu-id="3e568-125">At this point, you can edit the query before loading the table, by selecting **Transform Data** from the bottom of the window, or just load the table.</span></span>

<span data-ttu-id="3e568-126">เลือก **แปลงข้อมูล** เพื่อโหลดตารางและเปิดใช้งานตัวแก้ไข Power Query</span><span class="sxs-lookup"><span data-stu-id="3e568-126">Select **Transform Data** to load the table and launch Power Query Editor.</span></span> <span data-ttu-id="3e568-127">บานหน้าต่าง **การตั้งค่าคิวรี** จะแสดงขึ้นมา</span><span class="sxs-lookup"><span data-stu-id="3e568-127">The **Query Settings** pane is displayed.</span></span> <span data-ttu-id="3e568-128">ถ้าไม่ใช่ เลือก **ดู** จาก ribbon จากนั้น **การตั้งค่าคิวรี** เพื่อแสดงบานหน้าต่าง **การตั้งค่าคิวรี**</span><span class="sxs-lookup"><span data-stu-id="3e568-128">If it's not, select **View** from the ribbon, then **Query Settings** to display the **Query Settings** pane.</span></span> <span data-ttu-id="3e568-129">ซึ่งจะมีลักษณะเช่นนี้</span><span class="sxs-lookup"><span data-stu-id="3e568-129">Here’s what that looks like.</span></span>

![ตัวแก้ไข Power Query พร้อมการตั้งค่าคิวรี](media/desktop-connect-to-data/designer_gsg_editquery.png)

<span data-ttu-id="3e568-131">คะแนนเหล่านั้นเป็นข้อความมากกว่าจะเป็นตัวเลข และเราต้องการให้มันเป็นตัวเลข</span><span class="sxs-lookup"><span data-stu-id="3e568-131">All those scores are text rather than numbers, and we need them to be numbers.</span></span> <span data-ttu-id="3e568-132">ไม่มีปัญหา</span><span class="sxs-lookup"><span data-stu-id="3e568-132">No problem.</span></span> <span data-ttu-id="3e568-133">แค่เพียงคลิกขวาที่ส่วนหัวของคอลัมน์ และเลือก **เปลี่ยนชนิด** > **จำนวนเต็ม** เพื่อทำการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="3e568-133">Just right-click the column header, and select **Change Type** > **Whole Number** to change them.</span></span> <span data-ttu-id="3e568-134">เมื่อต้องเลือกมากกว่าหนึ่งคอลัมน์ ก่อนอื่นให้เลือกคอลัมน์ แล้วกดค้างที่ปุ่ม Shift เลือกคอลัมน์ที่อยู่ติดกันเพิ่มเติม และจากนั้นคลิกขวาที่ส่วนหัวของคอลัมน์เมื่อต้องเปลี่ยนคอลัมน์ที่เลือกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3e568-134">To choose more than one column, first select a column then hold down Shift, select additional adjacent columns, and then right-click a column header to change all selected columns.</span></span> <span data-ttu-id="3e568-135">ใช้ Ctrl เมื่อต้องเลือกคอลัมน์ที่ไม่ได้อยู่ติดกัน</span><span class="sxs-lookup"><span data-stu-id="3e568-135">Use Ctrl to choose columns that aren't adjacent.</span></span>

![เปลี่ยนชนิดข้อมูลเป็นจำนวนเต็ม](media/desktop-connect-to-data/designer_gsg_changedatatype.png)

<span data-ttu-id="3e568-137">ใน **การตั้งค่า Query** **ขั้นตอนที่กำหนดใช้** จะแสดงการเปลี่ยนแปลงทุกอย่างที่เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="3e568-137">In **Query Settings**, the **APPLIED STEPS** will reflect any changes that were made.</span></span> <span data-ttu-id="3e568-138">ขณะที่คุณทำการเปลี่ยนแปลงเพิ่มเติมไปยังข้อมูลตัวแก้ไข Power Query จะบันทึกการเปลี่ยนแปลงเหล่านั้นใน **ขั้นตอนที่กำหนดใช้** เป็นส่วนที่คุณสามารถ เข้ามาดูอีกครั้ง หรือลบได้หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="3e568-138">As you make additional changes to the data, Power Query Editor will record those changes in the **APPLIED STEPS** section, which you can adjust, revisit, rearrange, or delete as necessary.</span></span>

![ขั้นตอนที่กำหนดใช้](media/desktop-connect-to-data/designer_gsg_appliedsteps_changedtype.png)

<span data-ttu-id="3e568-140">คุณยังคงสามารถทำการเปลี่ยนแปลงเพิ่มเติมไปยังตารางหลังจากที่ทำการโหลดแล้วได้ แต่ในตอนนี้ยังไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="3e568-140">Additional changes to the table can still be made after it's loaded, but for now this will do.</span></span> <span data-ttu-id="3e568-141">เมื่อคุณทำเสร็จแล้ว ให้เลือก **ปิด & ใช้** จาก **หน้าหลัก** แถบ ribbon และ Power BI Desktop นำการเปลี่ยนแปลงไปใช้ และปิดตัวแก้ไข Power Query</span><span class="sxs-lookup"><span data-stu-id="3e568-141">When you're done, select **Close & Apply** from the **Home** ribbon, and Power BI Desktop applies the changes and closes Power Query Editor.</span></span>

![ปิดและใช้](media/desktop-connect-to-data/connecttodata_closenload.png)

<span data-ttu-id="3e568-143">ด้วยโมเดลข้อมูลที่โหลดใน **รายงาน** มุมมองใน Power BI Desktop เราสามารถเริ่มสร้างแสดงภาพ โดยการลากเขตข้อมูลลงบนพื้นที่รายงานได้</span><span class="sxs-lookup"><span data-stu-id="3e568-143">With the data model loaded, in **Report** view in Power BI Desktop, we can begin creating visualizations by dragging fields onto the canvas.</span></span>

![ลากค่าไปยังพื้นที่ทำงาน](media/desktop-connect-to-data/connecttodata_dragontoreportview.png)

<span data-ttu-id="3e568-145">แน่นอนว่า นี่คือโมเดลอย่างง่ายด้วยการเชื่อมต่อข้อมูลเดียว</span><span class="sxs-lookup"><span data-stu-id="3e568-145">Of course, this model is simple, with a single data connection.</span></span> <span data-ttu-id="3e568-146">รายงาน Power BI Desktop ส่วนใหญ่จะมีการเชื่อมต่อกับแหล่งข้อมูลอื่นที่แตกต่างกันไป สร้างรูปร่างเพื่อให้ตรงกับความต้องการของของคุณด้วยความสัมพันธ์ที่สร้างโมเดลข้อมูลที่สมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3e568-146">Most Power BI Desktop reports will have connections to different data sources, shaped to meet your needs, with relationships that produce a rich data model.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3e568-147">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3e568-147">Next steps</span></span>
<span data-ttu-id="3e568-148">มีมากมายหลากหลายสิ่งที่คุณสามารถทำได้ด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3e568-148">There are all sorts of things you can do with Power BI Desktop.</span></span> <span data-ttu-id="3e568-149">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับขีดความสามารถ กรุณาดูแหล่งทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3e568-149">For more information on its capabilities, check out the following resources:</span></span>

* [<span data-ttu-id="3e568-150">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="3e568-150">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="3e568-151">เกี่ยวกับการใช้ตัวแก้ไขคิวรีใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3e568-151">About using Query Editor in Power BI Desktop</span></span>](../transform-model/desktop-query-overview.md)
* [<span data-ttu-id="3e568-152">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3e568-152">Data sources in Power BI Desktop</span></span>](desktop-data-sources.md)
* [<span data-ttu-id="3e568-153">จัดรูปร่างและรวมข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3e568-153">Shape and combine data in Power BI Desktop</span></span>](desktop-shape-and-combine-data.md)
* [<span data-ttu-id="3e568-154">ใช้งานคิวรีที่ใช้บ่อยใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3e568-154">Perform common query tasks in Power BI Desktop</span></span>](../transform-model/desktop-common-query-tasks.md)   

<span data-ttu-id="3e568-155">ต้องการส่งคำติชมถึงเราหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3e568-155">Want to give us feedback?</span></span> <span data-ttu-id="3e568-156">เยี่ยม!</span><span class="sxs-lookup"><span data-stu-id="3e568-156">Great!</span></span> <span data-ttu-id="3e568-157">ใช้รายการเมนู **ส่งความคิดเห็น** ใน Power BI Desktop หรือเยี่ยมชม [คำติชมชุมชน](https://community.powerbi.com/t5/Community-Feedback/bd-p/community-feedback)</span><span class="sxs-lookup"><span data-stu-id="3e568-157">Use the **Submit an Idea** menu item in Power BI Desktop or visit [Community Feedback](https://community.powerbi.com/t5/Community-Feedback/bd-p/community-feedback).</span></span> <span data-ttu-id="3e568-158">เราหวังว่าจะได้รับคำติชมจากคุณ!</span><span class="sxs-lookup"><span data-stu-id="3e568-158">We look forward to hearing from you!</span></span>

![นำส่งแนวความคิด](media/desktop-connect-to-data/sendfeedback.png)
