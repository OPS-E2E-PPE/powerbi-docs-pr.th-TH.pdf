---
title: การใช้หน้าคำแนะนำเครื่องมือของหน้ารายงานใน Power BI
description: หน้าคำแนะนำเครื่องมือใน Power BI Desktop ช่วยให้คุณสร้างคำแนะนำเครื่องมือเมื่อโฮเวอร์ที่สวยงาม สำหรับวิชวลในรายงานของคุณ
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 07/26/2019
LocalizationGroup: Create reports
ms.openlocfilehash: 60eb647c6910a50512669c6b18f8a9010ab89867
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96412678"
---
# <a name="create-tooltips-based-on-report-pages-in-power-bi-desktop"></a><span data-ttu-id="199d2-103">สร้างคำแนะนำเครื่องมือตามหน้ารายงานใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="199d2-103">Create tooltips based on report pages in Power BI Desktop</span></span>
<span data-ttu-id="199d2-104">คุณสามารถสร้าง **คำแนะนำเครื่องมือรายงาน** ที่สวยงาม ที่ปรากฏเมื่อคุณโฮเวอร์เหนือวิชวล จากหน้ารายงานที่คุณสร้างใน **Power BI Desktop** ได้</span><span class="sxs-lookup"><span data-stu-id="199d2-104">You can create visually rich **report tooltips** that appear when you hover over visuals, based on report pages you create in **Power BI Desktop**.</span></span> <span data-ttu-id="199d2-105">โดยการสร้างหน้ารายงานที่เป็นคำแนะนำเครื่องมือของคุณ คำแนะนำเครื่องมือแบบกำหนดเองของคุณสามารถรวม วิชวล รูปภาพ และคอลเลกชันของรายการใด ๆ ที่คุณสร้างไว้ในหน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="199d2-105">By creating a report page that serves as your tooltip, your custom tooltips can include visuals, images, and any other collection of items you create in the report page.</span></span> 

![คำแนะนำเครื่องมือรายงานสำหรับ Power BI Desktop](media/desktop-tooltips/desktop-tooltips_00a.png)

<span data-ttu-id="199d2-107">คุณสามารถสร้างหน้าคำแนะนำเครื่องมือต่าง ๆ ได้มากเท่าที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="199d2-107">You can create as many tooltip pages as you want.</span></span> <span data-ttu-id="199d2-108">คำแนะนำเครื่องมือแต่ละหน้า สามารถเชื่อมโยงกับหนึ่งหรือหลายเขตข้อมูลในรายงานของคุณ ดังนั้น เมื่อคุณโฮเวอร์เหนือวิชวลที่มีเขตข้อมูลที่เลือก คำแนะนำเครื่องมือที่คุณสร้างขึ้นจะปรากฏ เมื่อคุณโฮเวอร์เหนือวิชวลนั้น โดยกรองตามจุดข้อมูลที่เมาส์ของคุณกำลังโฮเวอร์อยู่</span><span class="sxs-lookup"><span data-stu-id="199d2-108">Each tooltip page can be associated with one or more fields in your report, so that when you hover over a visual that includes the selected field, the tooltip you created on your tooltip page appears when you hover over the visual, filtered by the datapoint over which your mouse is hovering.</span></span> 

<span data-ttu-id="199d2-109">มีหลายสิ่งน่าสนใจ ที่คุณสามารถทำได้ด้วยคำแนะนำเครื่องมือรายงาน</span><span class="sxs-lookup"><span data-stu-id="199d2-109">There are all sorts of interesting things you can do with report tooltips.</span></span> <span data-ttu-id="199d2-110">ลองมาดูวิธีการสร้างคำแนะนำเครื่องมือ และสิ่งที่คุณต้องทำเพื่อกำหนดค่าเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="199d2-110">Let's take a look at how to create tooltips and what you must do to configure them.</span></span>

## <a name="create-a-report-tooltip-page"></a><span data-ttu-id="199d2-111">สร้างหน้าคำแนะนำเครื่องมือรายงาน</span><span class="sxs-lookup"><span data-stu-id="199d2-111">Create a report tooltip page</span></span>
<span data-ttu-id="199d2-112">เพื่อเริ่มต้นใช้งาน สร้างหน้ารายงานใหม่ โดยการคลิกที่ปุ่ม **+** ที่อยู่ด้านล่างของพื้นที่ทำงาน **Power BI Desktop** บริเวณแท็บหน้า</span><span class="sxs-lookup"><span data-stu-id="199d2-112">To get started, create a new report page by clicking the **+** button, found along the bottom of the **Power BI Desktop** canvas, in the page tabs area.</span></span> <span data-ttu-id="199d2-113">ปุ่มอยู่ข้างถัดจากหน้าสุดท้ายของรายงาน</span><span class="sxs-lookup"><span data-stu-id="199d2-113">The button is located beside the last page in the report.</span></span> 

![สร้างหน้ารายงานใหม่สำหรับคำแนะนำ](media/desktop-tooltips/desktop-tooltips_02.png)

<span data-ttu-id="199d2-115">คำแนะนำเครื่องมือของคุณสามารถมีขนาดใดก็ได้ แต่เนื่องจากคำแนะนำเครื่องมือจะโฮเวอร์เหนือพื้นที่ทำงาน ดังนั้นคุณอาจต้องการให้มีขนาดค่อนข้างเล็ก</span><span class="sxs-lookup"><span data-stu-id="199d2-115">Your tooltip can be any size, but keep in mind that tooltips hover over the report canvas, so you might want to keep them reasonably small.</span></span> <span data-ttu-id="199d2-116">ในบานหน้าต่าง **รูปแบบ** ในการ์ด **ขนาดหน้า** คุณสามารถเห็นขนาดหน้าใหม่ที่เรียกว่า *คำแนะนำเครื่องมือ*</span><span class="sxs-lookup"><span data-stu-id="199d2-116">In the **Format** pane in the **Page Size** card, you can see a new page size template called *Tooltip*.</span></span> <span data-ttu-id="199d2-117">ซึ่งทำให้ขนาดของหน้ารายงาน เหมาะกับคำแนะนำเครื่องมือของคุณ</span><span class="sxs-lookup"><span data-stu-id="199d2-117">This provides a report page canvas size that's ready for your tooltip.</span></span>

![เลือก คำแนะนำเครื่องมือ ในขนาดหน้า สำหรับคำแนะนำเครื่องมือที่เตรียมไว้ให้แล้ว](media/desktop-tooltips/desktop-tooltips_03.png)

<span data-ttu-id="199d2-119">ตามค่าเริ่มต้น **Power BI Desktop** จะปรับให้พื้นที่ทำงานเท่ากับพื้นที่ทั้งหมดบนหน้า</span><span class="sxs-lookup"><span data-stu-id="199d2-119">By default, **Power BI Desktop** fits your report canvas to the available space on the page.</span></span> <span data-ttu-id="199d2-120">ซึ่งมักเป็นสิ่งที่ดี แต่ไม่ใช่ในกรณีของคำแนะนำเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="199d2-120">Often that's good, but not in the case of tooltips.</span></span> <span data-ttu-id="199d2-121">เพื่อให้เข้าใจได้ดีขึ้นว่า คำแนะนำเครื่องมือของคุณจะมีหน้าตาเป็นอย่างไรเมื่อเสร็จแล้ว คุณสามารถเปลี่ยน **มุมมองหน้า** เป็นขนาดจริงได้</span><span class="sxs-lookup"><span data-stu-id="199d2-121">To get a better sense and view of what your tooltip will look like when you're done, you can change the **Page View** to actual size.</span></span> 

<span data-ttu-id="199d2-122">เมื่อต้องการทำเช่นนั้น เลือกแท็บ **มุมมอง** จาก ribbon</span><span class="sxs-lookup"><span data-stu-id="199d2-122">To do that, select the **View** tab from the ribbon.</span></span> <span data-ttu-id="199d2-123">จากที่นั่น เลือก **มุมมองหน้า > ขนาดจริง** ดังแสดงในรูปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="199d2-123">From there, select **Page View > Actual Size**, as shown in the following image.</span></span>

![แสดงหน้ารายงานในขนาดจริง เพื่อให้สร้างคำแนะนำเครื่องมือได้ง่ายขึ้น](media/desktop-tooltips/desktop-tooltips_04.png)

<span data-ttu-id="199d2-125">คุณยังสามารถตั้งชื่อหน้ารายงาน เพื่อให้เห็นจุดประสงค์ที่ชัดเจน</span><span class="sxs-lookup"><span data-stu-id="199d2-125">You can also name the report page so its purpose is clear.</span></span> <span data-ttu-id="199d2-126">เพียงเลือกการ์ด **ข้อมูลเกี่ยวกับหน้า** ในบานหน้าต่าง **รูปแบบ** แล้วพิมพ์ชื่อลงในเขตข้อมูล **ชื่อ** ที่คุณพบที่นั่น</span><span class="sxs-lookup"><span data-stu-id="199d2-126">Just select the **Page Information** card in the **Format** pane, then type the name into the **Name** field you find there.</span></span> <span data-ttu-id="199d2-127">ในรูปต่อไปนี้ ชื่อรายงานคำแนะนำเครื่องมือคือ *Tooltip 1* แต่คุณสามารถตั้งชื่ออื่นที่สร้างแรงบันดาลใจยิ่งขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="199d2-127">In the following image the tooltip report name is *Tooltip 1*, but feel free to name yours something more inspired.</span></span>

![ตั้งชื่อหน้ารายงานคำแนะนำเครื่องมือของคุณ](media/desktop-tooltips/desktop-tooltips_05.png)

<span data-ttu-id="199d2-129">จากนั้น คุณสามารถสร้างวิชวลใดก็ตาม ที่คุณต้องการให้แสดงในคำแนะนำเครื่องมือของคุณ</span><span class="sxs-lookup"><span data-stu-id="199d2-129">From there, you can create whatever visuals you would like to show up in your tooltip.</span></span> <span data-ttu-id="199d2-130">ในรูปต่อไปนี้ มีการ์ดสองใบ และมีแผนภูมิแท่งแบบกลุ่มหนึ่งแผนภูมิ บนหน้าคำแนะนำเครื่องมือ พร้อมกับสีพื้นหลังของหน้า และพื้นหลังของแต่ละวิชวล เพื่อให้ได้หน้าที่มีลักษณะที่เราต้องการ</span><span class="sxs-lookup"><span data-stu-id="199d2-130">In the following image, there are two cards and one clustered bar chart on the tooltip page, along with a background color for the page itself, and backgrounds for each of the visuals, to give it the look we wanted.</span></span>

![สกรีนช็อตแสดงคำแนะนำเครื่องมือรายงานแบบกำหนดเอง](media/desktop-tooltips/desktop-tooltips_06.png)

<span data-ttu-id="199d2-132">ยังมีอีกหลายขั้นตอนที่ต้องทำ เพื่อให้คำแนะนำเครื่องมือของหน้ารายงานของคุณ พร้อมทำงานเป็นคำแนะนำเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="199d2-132">There are more steps to complete before your tooltip report page is ready to work as a tooltip.</span></span> <span data-ttu-id="199d2-133">คุณจำเป็นต้องกำหนดค่าหน้าคำแนะนำเครื่องมือ ซึ่งทำได้สองสามวิธี ตามที่จะอธิบายในส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="199d2-133">You need to configure the tooltip page in a few ways, as described in the next section.</span></span> 

## <a name="configure-your-tooltip-report-page"></a><span data-ttu-id="199d2-134">กำหนดค่าหน้ารายงานคำแนะนำเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="199d2-134">Configure your tooltip report page</span></span>

<span data-ttu-id="199d2-135">เมื่อคุณสร้างหน้ารายงานคำแนะนำเครื่องมือแล้ว คุณจำเป็นต้องกำหนดค่าหน้า เพื่อให้ **Power BI Desktop** ลงทะเบียนเป็นคำแนะนำเครื่องมือ และให้แน่ใจว่าจะปรากฏขึ้นเหนือวิชวลที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="199d2-135">Once you have the tooltip report page created, you need to configure the page in order for **Power BI Desktop** to register it as a tooltip, and to ensure it appears in over the right visuals.</span></span>

<span data-ttu-id="199d2-136">เริ่มต้นจาก คุณจำเป็นต้องเลื่อนแถบเลื่อน **คำแนะนำเครื่องมือ** ให้เป็น **เปิด** ในการ์ด **ข้อมูลเกี่ยวกับหน้า** เพื่อทำให้หน้าเป็นคำแนะนำเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="199d2-136">To begin with, you need to turn the **Tooltip** slider to **On**, in the **Page Information** card, to make the page a tooltip.</span></span> 

![เปิดแถบเลื่อนเพื่อระบุว่า หน้าเป็นคำแนะนำเครื่องมือ](media/desktop-tooltips/desktop-tooltips_07.png)

<span data-ttu-id="199d2-138">เมื่อแถบเลื่อนถูกตั้งค่าเป็นเปิด คุณต้องระบุเขตข้อมูลที่คุณต้องการให้คำแนะนำเครื่องมือรายงานปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="199d2-138">Once that slider is set to on, you specify the fields for which you want the report tooltip to appear.</span></span> <span data-ttu-id="199d2-139">สำหรับวิชวลในรายงานที่มีเขตข้อมูลที่คุณระบุ คำแนะนำจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="199d2-139">For visuals in the report that include the field you specify, the tooltip will appear.</span></span> <span data-ttu-id="199d2-140">คุณระบุหนึ่งหรือหลายเขตข้อมูลที่จะใช้ โดยการลากเขตข้อมูลลงในบักเก็ต **เขตข้อมูลคำแนะนำเครื่องมือ** ที่พบในส่วน **เขตข้อมูล** ของบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="199d2-140">You specify which field or fields apply by dragging them into the **Tooltip fields** bucket, found in the **Fields** section of the **Visualizations** pane.</span></span> <span data-ttu-id="199d2-141">ในรูปต่อไปนี้ เขตข้อมูล *SalesAmount* ได้ถูกลากลงในบักเก็ต **เขตข้อมูลคำแนะนำเครื่องมือ**</span><span class="sxs-lookup"><span data-stu-id="199d2-141">In the following image, the *SalesAmount* field has been dragged into the **Tooltips fields** bucket.</span></span>

![เพิ่มเขตข้อมูลเพื่อระบุว่า คำแนะนำเครื่องมือจะปรากฏขึ้นที่ไหนบ้าง](media/desktop-tooltips/desktop-tooltips_08.png)
 
<span data-ttu-id="199d2-143">คุณสามารถใส่เขตข้อมูล ทั้งที่เป็นประเภทหรือเป็นตัวเลข ในบักเก็ต **เขตข้อมูลคำแนะนำเครื่องมือ** รวมถึงหน่วยวัดได้</span><span class="sxs-lookup"><span data-stu-id="199d2-143">You can include both categorical and numerical fields in the **Tooltips fields** bucket, including measures.</span></span>

<span data-ttu-id="199d2-144">เมื่อเสร็จเรียบร้อย หน้ารายงานคำแนะนำเครื่องมือที่คุณสร้าง จะถูกใช้เป็นคำแนะนำเครื่องมือในวิชวล ในรายงานที่ใช้เขตข้อมูลที่คุณวางลงในบักเก็ต **เขตข้อมูลคำแนะนำเครื่องมือ** แทนที่จะเป็นคำแนะนำเครื่องมือเริ่มต้นของ Power BI</span><span class="sxs-lookup"><span data-stu-id="199d2-144">Once completed, the tooltip report page you created will be used as a tooltip in visuals in the report that use any fields you placed into the **Tooltips fields** bucket, replacing the default Power BI tooltip.</span></span>

## <a name="manually-setting-a-report-tooltip"></a><span data-ttu-id="199d2-145">การตั้งค่าคำแนะนำเครื่องมือรายงานด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="199d2-145">Manually setting a report tooltip</span></span>

<span data-ttu-id="199d2-146">นอกจากการสร้างคำแนะนำเครื่องมือที่ปรากฏโดยอัตโนมัติ เมื่อโฮเวอร์เหนือวิชวลที่มีเขตข้อมูลที่ระบุ คุณสามารถตั้งค่าคำแนะนำด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="199d2-146">In addition to creating a tooltip that automatically appears when hovering over a visual that contains the specified field, you can manually set a tooltip.</span></span> 

<span data-ttu-id="199d2-147">วิชวลใด ๆ ที่สนับสนุนคำแนะนำเครื่องมือรายงานในขณะนี้ มีการ์ด **คำแนะนำเครื่องมือ** ในบานหน้าต่าง **การจัดรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="199d2-147">Any visual that supports report tooltips now has a **Tooltip** card in its **Formatting** pane.</span></span> 

<span data-ttu-id="199d2-148">เพื่อตั้งค่าแนะนำเครื่องมือด้วยตนเอง เลือกวิชวลที่คุณต้องการระบุคำแนะนำเครื่องมือด้วยตนเอง จากนั้นในบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล** เลือกส่วน **รูปแบบ** และขยายการ์ด **คำแนะนำเครื่องมือ**</span><span class="sxs-lookup"><span data-stu-id="199d2-148">To set a tooltip manually, select the visual for which you want to specify the manual tooltip, then in the **Visualizations** pane, select the **Format** section and expand the **Tooltip** card.</span></span>

![การ์ดคำแนะนำเครื่องมือสำหรับแต่ละวิชวล](media/desktop-tooltips/desktop-tooltips_09.png)

<span data-ttu-id="199d2-150">จากนั้น ในแดรอปดาวน์ **หน้า** เลือกหน้าคำแนะนำเครื่องมือที่คุณต้องการใช้สำหรับวิชวลที่เลือก</span><span class="sxs-lookup"><span data-stu-id="199d2-150">Then, in the **Page** dropdown, select the tooltip page you want to use for the selected visual.</span></span> <span data-ttu-id="199d2-151">สังเกตว่า เฉพาะหน้ารายงานที่มีระบุเป็น **คำแนะนำเครื่องมือ** เท่านั้น ที่จะแสดงขึ้นในกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="199d2-151">Note that only report pages that are specified as **Tooltip** pages show up in the dialog.</span></span>

![เลือกหน้าคำแนะนำเครื่องมือสำหรับคำแนะนำเครื่องมือด้วยตนเอง](media/desktop-tooltips/desktop-tooltips_10.png)

<span data-ttu-id="199d2-153">การที่สามารถกำหนดคำแนะนำเครื่องมือได้เอง มีการใช้งานได้หลายอย่าง</span><span class="sxs-lookup"><span data-stu-id="199d2-153">Being able to manually set a tooltip has many uses.</span></span> <span data-ttu-id="199d2-154">คุณสามารถตั้งค่าหน้าเปล่าสำหรับคำแนะนำ จึงเป็นการยกเลิกค่าเริ่มต้นคำแนะนำเครื่องมือของ Power BI</span><span class="sxs-lookup"><span data-stu-id="199d2-154">You can set a blank page for a tooltip, and thereby override the default Power BI tooltip selection.</span></span> <span data-ttu-id="199d2-155">อีกการใช้งานหนึ่งคือ เมื่อคุณไม่ต้องการคำแนะนำเครื่องมือที่ถูกเลือกอัตโนมัติโดย Power BI</span><span class="sxs-lookup"><span data-stu-id="199d2-155">Another use is when you don't want the tooltip that is automatically selected by Power BI to be the tooltip.</span></span> <span data-ttu-id="199d2-156">ตัวอย่างเช่น ถ้าคุณมีวิชวลที่มีสองเขตข้อมูล และทั้งสองเขตข้อมูลเหล่านั้นมีคำแนะนำเครื่องมือเชื่อมโยงอยู่ Power BI จะเลือกเพียงหนึ่งในนั้นเพื่อแสดง</span><span class="sxs-lookup"><span data-stu-id="199d2-156">For example, if you have a visual that includes two fields, and both of those fields have an associated tooltip, Power BI selects only one to show.</span></span> <span data-ttu-id="199d2-157">คุณอาจไม่ต้องการอย่างนั้น ดังนั้นคุณสามารถเลือกคำแนะนำเครื่องมือที่จะแสดงด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="199d2-157">You might not want that to be the case, so you could manually select which tooltip should be displayed.</span></span>

## <a name="reverting-to-default-tooltips"></a><span data-ttu-id="199d2-158">การเปลี่ยนกลับเป็นค่าเริ่มต้นคำแนะนำเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="199d2-158">Reverting to default tooltips</span></span>

<span data-ttu-id="199d2-159">ถ้าคุณสร้างคำแนะนำเครื่องมือด้วยตนเองสำหรับวิชวล แต่คุณตัดสินใจที่จะกลับไปใช้คำแนะนำเครื่องมือเริ่มต้นแทน คุณสามารถกลับไปใช้คำแนะนำเครื่องมือเริ่มต้นของ Power BI ได้เสมอ</span><span class="sxs-lookup"><span data-stu-id="199d2-159">If you create a manual tooltip for a visual but decide you want the default tooltip instead, you can always return to the default tooltip that Power BI provides.</span></span> <span data-ttu-id="199d2-160">เพื่อทำเช่นนั้น เลือกที่วิชวลและขยายการ์ด **คำแนะนำเครื่องมือ** เพียงเลือก *อัตโนมัติ* จากดรอปดาวน์ **หน้า** เพื่อย้อนกลับเป็นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="199d2-160">To do so, when a visual is selected and the **Tooltip** card is expanded, just select *Auto* from the **Page** dropdown to go back to the default.</span></span>

![กลับไปยังคำแนะนำเครื่องมือเริ่มต้นสำหรับวิชวล](media/desktop-tooltips/desktop-tooltips_11.png)

## <a name="custom-report-tooltips-and-line-charts"></a><span data-ttu-id="199d2-162">คำแนะนำเครื่องมือรายงานที่กำหนดเอง และแผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="199d2-162">Custom report tooltips and line charts</span></span>

<span data-ttu-id="199d2-163">มีข้อควรพิจารณาสองสามข้อที่ควรทราบ เมื่อคำแนะนำเครื่องมือรายงานของคุณโต้ตอบกับวิชวลแผนภูมิเส้น และเมื่อวิชวลมีไฮไลต์แบบเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="199d2-163">There are a few considerations to keep in mind when your report tooltips are interacting with line chart visuals, and with visuals when cross-highlighting.</span></span>

### <a name="report-tooltips-and-line-charts"></a><span data-ttu-id="199d2-164">คำแนะนำเครื่องมือรายงานและแผนภูมิเส้น</span><span class="sxs-lookup"><span data-stu-id="199d2-164">Report tooltips and line charts</span></span>

<span data-ttu-id="199d2-165">เมื่อคำแนะนำเครื่องมือรายงานแสดงสำหรับแผนภูมิเส้น มีเพียงคำแนะนำเครื่องมือเดียวเท่านั้นที่จะแสดงสำหรับทุกเส้นในแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="199d2-165">When a report tooltip is displayed for a line chart, only one tooltip for all lines in the chart is displayed.</span></span> <span data-ttu-id="199d2-166">ซึ่งเหมือนกับลักษณะคำแนะนำเครื่องมือเริ่มต้นของแผนภูมิเส้น ซึ่งแสดงคำแนะนำเครื่องมือเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="199d2-166">This is similar to the default tooltip behavior for line charts, which also displays only one tooltip.</span></span> 

<span data-ttu-id="199d2-167">เนื่องจากเขตข้อมูลในคำอธิบายแผนภูมิ ไม่ได้ส่งผ่านตัวกรองสำหรับคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="199d2-167">This is because the field in the legend does not get passed through as a filter for the tooltip.</span></span> <span data-ttu-id="199d2-168">ในรูปต่อไปนี้ คำแนะนำที่แสดงจะแสดงจำนวนหน่วยทั้งหมดที่ขายได้ในวันวันนั้น ของทั้งสามประเภทรวมกัน ในคำแนะนำเครื่องมือรายงาน (ในตัวอย่างคือ Deluxe, Economy และ Regular)</span><span class="sxs-lookup"><span data-stu-id="199d2-168">In the following image, the tooltip being displayed is showing all units sold on that day across all three classes displayed in the report tooltip (in this example, Deluxe, Economy, and Regular).</span></span> 

![แผนภูมิเส้นแสดงคำแนะนำเครื่องมือของข้อมูลรวมเท่านั้น](media/desktop-tooltips/desktop-tooltips_12.png)

### <a name="report-tooltips-and-cross-highlighting"></a><span data-ttu-id="199d2-170">คำแนะนำเครื่องมือและไฮไลต์แบบเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="199d2-170">Report tooltips and cross-highlighting</span></span>

<span data-ttu-id="199d2-171">เมื่อวิชวลมีการไฮไลต์แบบเชื่อมโยงในรายงาน คำแนะนำเครื่องมือจะแสดงข้อมูลที่ถูกเชื่อมโยงเสมอ แม้ว่าคุณกำลังวางเมาส์ไว้เหนือส่วนที่สีจางของจุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="199d2-171">When a visual is being cross-highlighted in a report, report tooltips always show the cross-highlighted data, even if you're hovering over the faded section of the data point.</span></span> <span data-ttu-id="199d2-172">ในรูปต่อไปนี้ เมาส์กำลังโฮเวอร์เหนือส่วนที่สีจางของกราฟแท่ง (ส่วนที่ไม่ถูกไฮไลต์) แต่คำแนะนำเครื่องมือรายงาน ยังคงแสดงข้อมูลสำหรับส่วนที่สีเข้มสำหรับจุดข้อมูลน้ัน (ข้อมูลที่ถูกไฮไลต์)</span><span class="sxs-lookup"><span data-stu-id="199d2-172">In the following image, the mouse is hovering over the faded section of the bar graph (the section that is not highlighted), but the report tooltip still shows data for the highlighted portion of that datapoint (the highlighted data).</span></span>

![คำแนะนำเครื่องมือรายงานแสดงข้อมูลที่ถูกไฮไลต์ เมื่อมีไฮไลต์แบบเชื่อมโยง](media/desktop-tooltips/desktop-tooltips_13.png)



## <a name="limitations-and-considerations"></a><span data-ttu-id="199d2-174">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="199d2-174">Limitations and considerations</span></span>
<span data-ttu-id="199d2-175">มีข้อจำกัดและข้อควรพิจารณาบางข้อสำหรับ **คำแนะนำเครื่องมือ** ที่คุณควรทราบ</span><span class="sxs-lookup"><span data-stu-id="199d2-175">There are a few limitations and considerations for **tooltips** to keep in mind.</span></span>

* <span data-ttu-id="199d2-176">เริ่มตั้งแต่เดือนธันวาคม 2018 ที่วางจำหน่าย **Power BI Desktop** วิชวลของปุ่มยังรองรับเคล็ดลับเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="199d2-176">Beginning with the December 2018 release of **Power BI Desktop**, Button visuals also support tooltips.</span></span>
* <span data-ttu-id="199d2-177">วิชวล Power BI ไม่สนับสนุนกล่องแสดงคำอธิบายสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="199d2-177">Report tooltips are not supported for Power BI visuals.</span></span> 
* <span data-ttu-id="199d2-178">คลัสเตอร์ เป็นเขตข้อมูลที่ยังไม่สนับสนุนการแสดงคำแนะนำเครื่องมือรายงานในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="199d2-178">Clusters are not currently supported as fields that can be shown in report tooltips.</span></span> 
* <span data-ttu-id="199d2-179">เมื่อต้องการเลือกเขตข้อมูลสำหรับแสดงคำแนะนำเครื่องมือรายงาน เมื่อใช้เขตข้อมูลเมื่อเทียบกับประเภท วิชวลที่มีเขตข้อมูลนั้นจะแสดงคำแนะนำที่ระบุเมื่อ ข้อสรุปของเขตข้อมูลที่เลือกตรงกัน</span><span class="sxs-lookup"><span data-stu-id="199d2-179">When choosing a field to be shown for report tooltips, when using a field versus a category, visuals that contain that field will only show the specified tooltip when summarization with the selected field matches.</span></span> 



## <a name="next-steps"></a><span data-ttu-id="199d2-180">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="199d2-180">Next steps</span></span>
<span data-ttu-id="199d2-181">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะที่คล้ายกัน หรือโต้ตอบกับคำแนะนำเครื่องมือรายงาน โปรดดูที่บทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="199d2-181">For more information about features that are similar or interact with report tooltips, take a look at the following articles:</span></span>

* [<span data-ttu-id="199d2-182">ใช้ตัวเจาะเข้าถึงรายละเอียดใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="199d2-182">Use drillthrough in Power BI Desktop</span></span>](desktop-drillthrough.md)
* [<span data-ttu-id="199d2-183">แสดงไทล์แดชบอร์ดหรือรายงานวิชวลในโหมดโฟกัส</span><span class="sxs-lookup"><span data-stu-id="199d2-183">Display a dashboard tile or report visual in Focus mode</span></span>](../consumer/end-user-focus.md)
