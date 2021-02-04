---
title: จัดรูปแบบตารางใน Power BI Desktop ตามเงื่อนไข
description: นำการจัดรูปแบบแบบกำหนดเองลงในตาราง
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 12/14/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 9e0ec57b2b37c237db94cf5710d853cbbb2cd6ed
ms.sourcegitcommit: 46cf62d9bb33ac7b7eae7910fbba6756f626c65f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/15/2020
ms.locfileid: "97492207"
---
# <a name="use-conditional-formatting-in-tables"></a><span data-ttu-id="b8bf4-103">ใช้การจัดรูปแบบตามเงื่อนไขในตาราง</span><span class="sxs-lookup"><span data-stu-id="b8bf4-103">Use conditional formatting in tables</span></span> 

<span data-ttu-id="b8bf4-104">ด้วยการจัดรูปแบบตามเงื่อนไขสำหรับตารางใน Power BI Desktop คุณสามารถระบุสีของเซลล์ รวมถึงการไล่ระดับสี โดยขึ้นอยู่กับค่าของเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b8bf4-104">With conditional formatting for tables in Power BI Desktop, you can specify customized cell colors, including color gradients, based on field values.</span></span> <span data-ttu-id="b8bf4-105">นอกจากนี้คุณยังสามารถแสดงค่าเซลล์ด้วยแถบข้อมูลหรือไอคอน KPI หรือในฐานะลิงก์เว็บที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="b8bf4-105">You can also represent cell values with data bars or KPI icons, or as active web links.</span></span> <span data-ttu-id="b8bf4-106">คุณสามารถใช้การจัดรูปแบบตามเงื่อนไขกับข้อความหรือเขตข้อมูลใดก็ตามได้ตราบใดที่คุณจัดรูปแบบตามเขตข้อมูลที่มีตัวเลข ชื่อสี หรือรหัสฐานสิบหกหรือค่า URL ของเว็บ</span><span class="sxs-lookup"><span data-stu-id="b8bf4-106">You can apply conditional formatting to any text or data field, as long as you base the formatting on a field that has numeric, color name or hex code, or web URL values.</span></span> 

<span data-ttu-id="b8bf4-107">เมื่อต้องการใช้การจัดรูปแบบตามเงื่อนไข ให้เลือกการแสดงผลข้อมูลด้วยภาพแบบ **ตาราง** หรือ **เมทริกซ์** ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="b8bf4-107">To apply conditional formatting, select a **Table** or **Matrix** visualization in Power BI Desktop.</span></span> <span data-ttu-id="b8bf4-108">ในส่วน **เขตข้อมูล** ของบานหน้าต่าง **การแสดงผลข้อมูลด้วยภาพ** ให้คลิกขวาหรือเลือกลูกศรลงที่อยู่ถัดจากเขตข้อมูลใน **ค่า** ที่คุณต้องการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="b8bf4-108">In the **Fields** section of the **Visualizations** pane, right-click or select the down-arrow next to the field in the **Values** well that you want to format.</span></span> <span data-ttu-id="b8bf4-109">เลือก **การจัดรูปแบบตามเงื่อนไข** จากนั้นเลือกประเภทของการจัดรูปแบบที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="b8bf4-109">Select **Conditional formatting**, and then select the type of formatting to apply.</span></span>

![เมนูการจัดรูปแบบตามเงื่อนไข](media/desktop-conditional-table-formatting/table-formatting-0-popup-menu.png)

> [!NOTE]
> <span data-ttu-id="b8bf4-111">การจัดรูปแบบตามเงื่อนไขจะแทนที่พื้นหลังหรือสีฟอนต์แบบกำหนดเองที่คุณนำไปใช้กับเซลล์ที่มีการจัดรูปแบบตามเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="b8bf4-111">Conditional formatting overrides any custom background or font color you apply to the conditionally formatted cell.</span></span>

<span data-ttu-id="b8bf4-112">เพื่อเอาการจัดรูปแบบตามเงื่อนไขออกจากวิชวล ให้เลือก **ลบการจัดรูปแบบตามเงื่อนไขออก** จากเมนูแบบเลื่อนลงของเขตข้อมูล จากนั้นให้เลือกชนิดของการจัดรูปแบบที่จะเอาออก</span><span class="sxs-lookup"><span data-stu-id="b8bf4-112">To remove conditional formatting from a visualization, select **Remove conditional formatting** from the field's drop-down menu, and then select the type of formatting to remove.</span></span>

![เมนูลบการจัดรูปแบบตามเงื่อนไขออก](media/desktop-conditional-table-formatting/table-formatting-1-remove.png)

<span data-ttu-id="b8bf4-114">ส่วนต่อไปนี้อธิบายตัวเลือกการจัดรูปแบบตามเงื่อนไขแต่ละตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="b8bf4-114">The following sections describe each conditional formatting option.</span></span> <span data-ttu-id="b8bf4-115">คุณสามารถรวมตัวเลือกมากกว่าหนึ่งตัวเลือกลงในคอลัมน์ตารางเดียว</span><span class="sxs-lookup"><span data-stu-id="b8bf4-115">You can combine more than one option in a single table column.</span></span>

## <a name="format-background-or-font-color"></a><span data-ttu-id="b8bf4-116">จัดรูปแบบสีพื้นหลังหรือสีฟอนต์</span><span class="sxs-lookup"><span data-stu-id="b8bf4-116">Format background or font color</span></span>

<span data-ttu-id="b8bf4-117">เมื่อต้องการจัดรูปแบบสีพื้นหลังหรือสีฟอนต์ของเซลล์ ให้เลือก **การจัดรูปแบบตามเงื่อนไข** สำหรับเขตข้อมูล จากนั้นเลือก **สีพื้นหลัง** หรือ **สีฟอนต์** จากเมนูดรอปดาวน์</span><span class="sxs-lookup"><span data-stu-id="b8bf4-117">To format cell background or font color, select **Conditional formatting** for a field, and then select either **Background color** or **Font color** from the drop-down menu.</span></span> 

![เลือกสีพื้นหลังหรือสีตัวอักษร](media/desktop-conditional-table-formatting/table-formatting-1-color-by-rules-dialog.png)

<span data-ttu-id="b8bf4-119">กล่องโต้ตอบ **สีพื้นหลัง** หรือ **สีฟอนต์** จะเปิดขึ้นพร้อมชื่อของเขตข้อมูลที่คุณกำลังจัดรูปแบบในชื่อเรื่อง</span><span class="sxs-lookup"><span data-stu-id="b8bf4-119">The **Background color** or **Font color** dialog box opens, with the name of the field you're formatting in the title.</span></span> <span data-ttu-id="b8bf4-120">หลังจากเลือกตัวเลือกการจัดรูปแบบตามเงื่อนไขแล้ว ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b8bf4-120">After selecting conditional formatting options, select **OK**.</span></span> 

![กล่องโต้ตอบสีพื้นหลังและสีฟอนต์](media/desktop-conditional-table-formatting/table-formatting-2-diverging.png)

<span data-ttu-id="b8bf4-122">ตัวเลือก **สีพื้นหลัง** และ **สีฟอนต์** เหมือนกัน แต่มีผลกับสีพื้นหลังของเซลล์และสีฟอนต์ ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="b8bf4-122">The **Background color** and **Font color** options are the same, but affect the cell background color and font color, respectively.</span></span> <span data-ttu-id="b8bf4-123">คุณสามารถใช้การจัดรูปแบบตามเงื่อนไขที่เหมือนกันหรือแตกต่างกับสีฟอนต์และสีพื้นหลังของเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b8bf4-123">You can apply the same or different conditional formatting to a field's font color and background color.</span></span> <span data-ttu-id="b8bf4-124">ถ้าคุณทำให้ฟอนต์และพื้นหลังของเขตข้อมูลมีสีเดียวกัน ฟอนต์จะรวมกันเป็นพื้นหลัง ดังนั้นคอลัมน์ตารางจะแสดงเฉพาะสี</span><span class="sxs-lookup"><span data-stu-id="b8bf4-124">If you make a field's font and background the same color, the font blends into the background so the table column shows only the colors.</span></span>

## <a name="color-by-color-scale"></a><span data-ttu-id="b8bf4-125">สีตามสเกลสี</span><span class="sxs-lookup"><span data-stu-id="b8bf4-125">Color by color scale</span></span>

<span data-ttu-id="b8bf4-126">เมื่อต้องการจัดรูปแบบสีพื้นหลังหรือสีฟอนต์ของเซลล์ตามสเกลสี ในเขตข้อมูล **รูปแบบตาม** ของกล่องโต้ตอบ **สีพื้นหลัง** หรือ **สีฟอนต์** ให้เลือก **สเกลสี**</span><span class="sxs-lookup"><span data-stu-id="b8bf4-126">To format cell background or font color by color scale, in the **Format by** field of the **Background color** or **Font color** dialog box, select **Color scale**.</span></span> <span data-ttu-id="b8bf4-127">ภายใต้ **ยึดตามเขตข้อมูล** ให้เลือกเขตข้อมูลเพื่อยึดการจัดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="b8bf4-127">Under **Based on field**, select the field to base the formatting on.</span></span> <span data-ttu-id="b8bf4-128">คุณสามารถจัดรูปแบบตามเขตข้อมูลปัจจุบันหรือในเขตข้อมูลใดก็ตามในแบบจำลองของคุณที่มีข้อมูลตัวเลขหรือสีได้</span><span class="sxs-lookup"><span data-stu-id="b8bf4-128">You can base the formatting on the current field, or on any field in your model that has numerical or color data.</span></span> 

<span data-ttu-id="b8bf4-129">ภายใต้ **การสรุป** ให้ระบุประเภทการรวมที่คุณต้องการใช้สำหรับเขตข้อมูลที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b8bf4-129">Under **Summarization**, specify the aggregation type you want to use for the selected field.</span></span> <span data-ttu-id="b8bf4-130">ภายใต้ **การจัดรูปแบบเริ่มต้น** ให้เลือกการจัดรูปแบบเพื่อนำไปใช้กับค่าว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="b8bf4-130">Under **Default formatting**, select a formatting to apply to blank values.</span></span> 

<span data-ttu-id="b8bf4-131">ภายใต้ **ต่ำสุด** และ **สูงสุด** ให้เลือกว่าจะใช้ชุดรูปแบบสีตามค่าเขตข้อมูลต่ำสุดและสูงสุดหรือบนค่าที่คุณป้อน</span><span class="sxs-lookup"><span data-stu-id="b8bf4-131">Under **Minimum** and **Maximum**, choose whether to apply the color scheme based on the lowest and highest field values, or on custom values you enter.</span></span> <span data-ttu-id="b8bf4-132">ดรอปดาวน์และเลือกตัวอย่างสี (swatch) ที่คุณต้องการนำไปใช้กับค่าต่ำสุดและสูงสุด</span><span class="sxs-lookup"><span data-stu-id="b8bf4-132">Drop down and select the colors swatches you want to apply to the minimum and maximum values.</span></span> <span data-ttu-id="b8bf4-133">เลือกกล่องกาเครื่องหมาย **ขยายออก** เพื่อระบุค่า **ศูนย์** และสี</span><span class="sxs-lookup"><span data-stu-id="b8bf4-133">Select the **Diverging** check box to also specify a **Center** value and color.</span></span> 

![ตั้งค่าพื้นหลังของเซลล์ด้วยสเกลสี](media/desktop-conditional-table-formatting/table-formatting-1-diverging-table.png)

<span data-ttu-id="b8bf4-135">ตารางตัวอย่างที่มีการจัดรูปแบบพื้นหลังตามสเกลสีบนคอลัมน์ **Affordability** มีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="b8bf4-135">An example table with color scale background formatting on the **Affordability** column looks like this:</span></span>

![ตารางตัวอย่างที่มีสเกลสีพื้นหลังที่ขยายออก](media/desktop-conditional-table-formatting/table-formatting-1-apply-color-to.png)

<span data-ttu-id="b8bf4-137">ตารางตัวอย่างที่มีการจัดรูปแบบฟอนต์ตามสเกลสีบนคอลัมน์ **Affordability** มีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="b8bf4-137">The example table with color scale font formatting on the **Affordability** column looks like this:</span></span>

![ตารางตัวอย่างที่มีสเกลสีฟอนต์ที่ขยายออก](media/desktop-conditional-table-formatting/table-formatting-2-table.png)

## <a name="color-by-rules"></a><span data-ttu-id="b8bf4-139">สีตามกฎ</span><span class="sxs-lookup"><span data-stu-id="b8bf4-139">Color by rules</span></span>

<span data-ttu-id="b8bf4-140">เมื่อต้องการจัดรูปแบบสีพื้นหลังหรือสีฟอนต์ของเซลล์ตามกฎ ในเขตข้อมูล **รูปแบบตาม** ของกล่องโต้ตอบ **สีพื้นหลัง** หรือ **สีฟอนต์** ให้เลือก **กฎ**</span><span class="sxs-lookup"><span data-stu-id="b8bf4-140">To format cell background or font color by rules, in the **Format by** field of the **Background color** or **Font color** dialog box, select **Rules**.</span></span> <span data-ttu-id="b8bf4-141">อีกครั้ง **ยึดตามเขตข้อมูล** แสดงเขตข้อมูลที่จะใช้ในการจัดรูปแบบ และ **การสรุป** แสดงชนิดการรวมสำหรับเขตข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b8bf4-141">Again, **Based on field** shows the field to base the formatting on, and **Summarization** shows the aggregation type for the field.</span></span> 

<span data-ttu-id="b8bf4-142">ภายใต้ **กฎ** ให้ป้อนช่วงของค่าหนึ่งหรือหลายช่วง และตั้งค่าสีสำหรับแต่ละช่วง</span><span class="sxs-lookup"><span data-stu-id="b8bf4-142">Under **Rules**, enter one or more value ranges, and set a color for each one.</span></span> <span data-ttu-id="b8bf4-143">ช่วงค่าแต่ละช่วงเริ่มต้นจากเงื่อนไขค่า *ถ้า* เงื่อนไขค่า *และ* และสี</span><span class="sxs-lookup"><span data-stu-id="b8bf4-143">Each value range has an *If value* condition, an *and* value condition, and a color.</span></span> <span data-ttu-id="b8bf4-144">พื้นหลังของเซลล์หรือฟอนต์ในแต่ละช่วงค่าแต่ละช่วงจะเป็นสีตามสีที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="b8bf4-144">Cell backgrounds or fonts in each value range are colored with the given color.</span></span> <span data-ttu-id="b8bf4-145">ตัวอย่างต่อไปนี้มีสามกฎ:</span><span class="sxs-lookup"><span data-stu-id="b8bf4-145">The following example has three rules:</span></span>

![สีตามกฎ](media/desktop-conditional-table-formatting/table-formatting-1-color-by-rules-if-value.png)

<span data-ttu-id="b8bf4-147">ตารางตัวอย่างที่มีการจัดรูปแบบสีพื้นหลังตามกฎบนคอลัมน์ **Affordability** มีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="b8bf4-147">An example table with rules-based background color formatting on the **Affordability** column looks like this:</span></span>

![ตารางตัวอย่าง ด้วยสีตามกฎ](media/desktop-conditional-table-formatting/table-formatting-1-color-by-rules-table.png)

## <a name="color-by-color-values"></a><span data-ttu-id="b8bf4-149">สีตามค่าสี</span><span class="sxs-lookup"><span data-stu-id="b8bf4-149">Color by color values</span></span>

<span data-ttu-id="b8bf4-150">ถ้าคุณมีเขตข้อมูลหรือหน่วยวัดที่มีชื่อสีหรือข้อมูลค่าฐานสิบหก คุณสามารถใช้การจัดรูปแบบตามเงื่อนไขเพื่อนำสีเหล่านั้นไปใช้กับสีพื้นหลังหรือสีฟอนต์ของคอลัมน์ได้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b8bf4-150">If you have a field or measure with color name or hex value data, you can use conditional formatting to automatically apply those colors to a column's background or font color.</span></span> <span data-ttu-id="b8bf4-151">คุณยังสามารถใช้ตรรกะแบบกำหนดเองเพื่อนำสีไปใช้กับฟอนต์หรือพื้นหลังได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="b8bf4-151">You can also use custom logic to apply colors to the font or background.</span></span>

<span data-ttu-id="b8bf4-152">เขตข้อมูลสามารถใช้ค่าสีใดก็ตามที่แสดงอยู่ในสเปคสี CSS ที่ [https://www.w3.org/TR/css-color-3/](https://www.w3.org/TR/css-color-3/)</span><span class="sxs-lookup"><span data-stu-id="b8bf4-152">The field can use any color values listed in the CSS color spec at [https://www.w3.org/TR/css-color-3/](https://www.w3.org/TR/css-color-3/).</span></span> <span data-ttu-id="b8bf4-153">ค่าสีเหล่านี้อาจรวมถึง:</span><span class="sxs-lookup"><span data-stu-id="b8bf4-153">These color values can include:</span></span>
- <span data-ttu-id="b8bf4-154">รหัสฐานสิบหก 3 6 หรือ 8 หลัก ตัวอย่างเช่น #3E4AFF</span><span class="sxs-lookup"><span data-stu-id="b8bf4-154">3, 6 or 8-digit hex codes, for example #3E4AFF.</span></span> <span data-ttu-id="b8bf4-155">ตรวจสอบให้แน่ใจว่าคุณได้ใช้สัญลักษณ์ # ที่จุดเริ่มต้นของรหัส</span><span class="sxs-lookup"><span data-stu-id="b8bf4-155">Make sure you include the # symbol at the start of the code.</span></span> 
- <span data-ttu-id="b8bf4-156">ค่า RGB หรือ RGBA เช่น RGBA(234, 234, 234, 0.5)</span><span class="sxs-lookup"><span data-stu-id="b8bf4-156">RGB or RGBA values, like RGBA(234, 234, 234, 0.5).</span></span>
- <span data-ttu-id="b8bf4-157">ค่า HSL หรือ HSLA เช่น HSLA(123, 75%, 75%, 0.5)</span><span class="sxs-lookup"><span data-stu-id="b8bf4-157">HSL or HSLA values, like HSLA(123, 75%, 75%, 0.5).</span></span>
- <span data-ttu-id="b8bf4-158">ชื่อสี เช่น Green, SkyBlue หรือ PeachPuff</span><span class="sxs-lookup"><span data-stu-id="b8bf4-158">Color names, such as Green, SkyBlue, or PeachPuff.</span></span> 

<span data-ttu-id="b8bf4-159">ตารางต่อไปนี้มีชื่อสีที่เกี่ยวข้องกับแต่ละรัฐ:</span><span class="sxs-lookup"><span data-stu-id="b8bf4-159">The following table has a color name associated with each state:</span></span> 

![ตารางรัฐ (State) พร้อมชื่อสี](media/desktop-conditional-table-formatting/conditional-table-formatting_01.png)

<span data-ttu-id="b8bf4-161">เมื่อต้องการจัดรูปแบบคอลัมน์ **สี** ตามค่าเขตข้อมูล ให้เลือก **การจัดรูปแบบตามเงื่อนไข** สำหรับเขตข้อมูล **สี** จากนั้นเลือก **สีพื้นหลัง** หรือ **สีฟอนต์**</span><span class="sxs-lookup"><span data-stu-id="b8bf4-161">To format the **Color** column based on its field values, select **Conditional formatting** for the **Color** field, and then select **Background color** or **Font color**.</span></span> 

<span data-ttu-id="b8bf4-162">ในกล่องโต้ตอบ **สีพื้นหลัง** หรือ **สีฟอนต์** ให้เลือก **ค่าเขตข้อมูล** จากเขตข้อมูลดรอปดาวน์ **รูปแบบตาม**</span><span class="sxs-lookup"><span data-stu-id="b8bf4-162">In the **Background color** or **Font color** dialog box, select **Field value** from the **Format by** drop-down field.</span></span>

![จัดรูปแบบโดยค่าเขตข้อมูล](media/desktop-conditional-table-formatting/conditional-table-formatting_02.png)

<span data-ttu-id="b8bf4-164">ตารางตัวอย่างที่มีการจัดรูปแบบ **สีพื้นหลัง** ตามค่าเขตข้อมูลสี ในเขตข้อมูล **สี** มีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="b8bf4-164">An example table with color field value-based **Background color** formatting on the **Color** field looks like this:</span></span>

![ตารางตัวอย่างที่มีการจัดรูปแบบพื้นหลังตามค่าเขตข้อมูล](media/desktop-conditional-table-formatting/conditional-table-formatting_03.png)

<span data-ttu-id="b8bf4-166">หากคุณยังใช้ **ค่าเขตข้อมูล** เพื่อจัดรูปแบบ **สีฟอนต์** ของคอลัมน์ ผลลัพธ์จะเป็นสีทึบในคอลัมน์ **สี**:</span><span class="sxs-lookup"><span data-stu-id="b8bf4-166">If you also use **Field value** to format the column's **Font color**, the result is a solid color in the **Color** column:</span></span>

![จัดรูปแบบพื้นหลังและฟอนต์ตามค่าเขตข้อมูล](media/desktop-conditional-table-formatting/conditional-table-formatting_04.png)

## <a name="color-based-on-a-calculation"></a><span data-ttu-id="b8bf4-168">สีที่ยึดตามการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="b8bf4-168">Color based on a calculation</span></span>

<span data-ttu-id="b8bf4-169">คุณสามารถสร้างการคำนวณที่แสดงค่าที่แตกต่างกันโดยยึดตามเงื่อนไขเชิงตรรกะทางธุรกิจที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="b8bf4-169">You can create a calculation that outputs different values based on business logic conditions you select.</span></span> <span data-ttu-id="b8bf4-170">การสร้างสูตรมักจะเร็วกว่าการสร้างกฎหลายกฎในกล่องโต้ตอบการจัดรูปแบบตามเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="b8bf4-170">Creating a formula is usually faster than creating multiple rules in the conditional formatting dialog.</span></span> 

<span data-ttu-id="b8bf4-171">ตัวอย่างเช่น สูตรต่อไปนี้จะใช้ค่าสีฐานสิบหกไปยังคอลัมน์ **Affordability rank** ใหม่โดยยึดตามค่าของคอลัมน์ **Affordability** ที่มีอยู่:</span><span class="sxs-lookup"><span data-stu-id="b8bf4-171">For example, the following formula applies hex color values to a new **Affordability rank** column, based on existing **Affordability** column values:</span></span>

![การคำนวณสูตร](media/desktop-conditional-table-formatting/conditional-table-formatting_05.png)

<span data-ttu-id="b8bf4-173">เมื่อต้องการใช้สี ให้เลือกการจัดรูปแบบตามเงื่อนไข **สีพื้นหลัง** หรือ **สีฟอนต์** สำหรับคอลัมน์ **Affordability** และยึดการจัดรูปแบบตาม **ค่าเขตข้อมูล** ของคอลัมน์ **Affordability rank**</span><span class="sxs-lookup"><span data-stu-id="b8bf4-173">To apply the colors, select **Background color** or **Font color** conditional formatting for the **Affordability** column, and base the formatting on the **Field value** of the **Affordability rank** column.</span></span> 

![ยึดสีพื้นหลังตามคอลัมน์จากการคำนวณ](media/desktop-conditional-table-formatting/conditional-table-formatting_06.png)

<span data-ttu-id="b8bf4-175">ตารางตัวอย่างที่มีสีพื้นหลัง **Affordability** ยึดตามคอลัมน์ **Affordability rank** จากการคำนวณมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="b8bf4-175">The example table with **Affordability** background color based on calculated **Affordability rank** looks like this:</span></span>

![ตารางตัวอย่างที่มีสีตามค่าจากการคำนวณ](media/desktop-conditional-table-formatting/conditional-table-formatting_07.png)

<span data-ttu-id="b8bf4-177">คุณสามารถสร้างรูปแบบอื่นๆ อีกมากมายเพียงแค่ใช้จินตนาการและการคำนวณจำนวนหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b8bf4-177">You can create many more variations, just by using your imagination and some calculations.</span></span>

## <a name="add-data-bars"></a><span data-ttu-id="b8bf4-178">เพิ่มแถบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b8bf4-178">Add data bars</span></span>

<span data-ttu-id="b8bf4-179">เมื่อต้องการแสดงแถบข้อมูลตามค่าเซลล์ ให้เลือก **การจัดรูปแบบตามเงื่อนไข** สำหรับเขตข้อมูล **Affordability** จากนั้นเลือก **แถบข้อมูล** จากเมนูดรอปดาวน์</span><span class="sxs-lookup"><span data-stu-id="b8bf4-179">To show data bars based on cell values, select **Conditional formatting** for the **Affordability** field, and then select **Data bars** from the drop-down menu.</span></span> 

<span data-ttu-id="b8bf4-180">ในกล่องโต้ตอบ **แถบข้อมูล** ตัวเลือก **แสดงแถบอย่างเดียว** จะไม่ถูกเลือกตามค่าเริ่มต้น ดังนั้น เซลล์ของตารางจะแสดงทั้งแถบและค่าจริง</span><span class="sxs-lookup"><span data-stu-id="b8bf4-180">In the **Data bars** dialog, the **Show bar only** option is unchecked by default, so the table cells show both the bars and the actual values.</span></span> <span data-ttu-id="b8bf4-181">เมื่อต้องการแสดงเฉพาะแถบข้อมูล ให้เลือกกล่องกาเครื่องหมาย **แสดงเฉพาะแถบข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="b8bf4-181">To show the data bars only, select the **Show bar only** check box.</span></span>

<span data-ttu-id="b8bf4-182">คุณสามารถระบุค่า **ต่ำสุด** และ **สูงสุด** สีของแถบข้อมูลและทิศทาง และสีแกนได้</span><span class="sxs-lookup"><span data-stu-id="b8bf4-182">You can specify **Minimum** and **Maximum** values, data bar colors and direction, and axis color.</span></span> 

![กล่องโต้ตอบแถบข้อมูล](media/desktop-conditional-table-formatting/table-formatting-3-default.png)

<span data-ttu-id="b8bf4-184">ด้วยแถบข้อมูลที่ใช้กับคอลัมน์ **Affordability** ตารางตัวอย่างจะมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="b8bf4-184">With data bars applied to the **Affordability** column, the example table looks like this:</span></span>

![ตารางตัวอย่างที่มีแถบข้อมูล](media/desktop-conditional-table-formatting/table-formatting-3-default-table-bars.png)

## <a name="add-icons"></a><span data-ttu-id="b8bf4-186">เพิ่มไอคอน</span><span class="sxs-lookup"><span data-stu-id="b8bf4-186">Add icons</span></span>

<span data-ttu-id="b8bf4-187">เมื่อต้องการแสดงไอคอนตามค่าเซลล์ ให้เลือก **การจัดรูปแบบตามเงื่อนไข** สำหรับเขตข้อมูล จากนั้นเลือก **ไอคอน** จากเมนูดรอปดาวน์</span><span class="sxs-lookup"><span data-stu-id="b8bf4-187">To show icons based on cell values, select **Conditional formatting** for the field, and then select **Icons** from the drop-down menu.</span></span> 

<span data-ttu-id="b8bf4-188">ในกล่องโต้ตอบ **ไอคอน** ภายใต้ **จัดรูปแบบตาม** ให้เลือก **กฎ** หรือ **ค่าเขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="b8bf4-188">In the **Icons** dialog, under **Format by**, select either **Rules** or **Field value**.</span></span> 

<span data-ttu-id="b8bf4-189">เมื่อต้องการจัดรูปแบบตามกฎ ให้เลือก **ยึดตามเขตข้อมูล**, วิธี **การสรุป**, **โครงร่างไอคอน**, **การจัดเรียงไอคอน**, ไอคอน **สไตล์** และอย่างน้อยหนึ่ง **กฎ**</span><span class="sxs-lookup"><span data-stu-id="b8bf4-189">To format by rules, select a **Based on field**, **Summarization** method, **Icon layout**, **Icon alignment**, icon **Style**, and one or more **Rules**.</span></span> <span data-ttu-id="b8bf4-190">ภายใต้ **กฎ** ให้ป้อนอย่างน้อยหนึ่งกฎที่มีเงื่อนไขค่า *ถ้า* และเงื่อนไขค่า *และ* และเลือกไอคอนเพื่อใช้กับแต่ละกฎ</span><span class="sxs-lookup"><span data-stu-id="b8bf4-190">Under **Rules**, enter one or more rules with an *If value* condition and an *and* value condition, and select an icon to apply to each rule.</span></span> 

<span data-ttu-id="b8bf4-191">เมื่อต้องการจัดรูปแบบตามค่าเขตข้อมูล ให้เลือก **ยึดตามเขตข้อมูล**, วิธี **การสรุป**, **โครงร่างไอคอน** และ **การจัดเรียงไอคอน**</span><span class="sxs-lookup"><span data-stu-id="b8bf4-191">To format by field values, select a **Based on field**, **Summarization** method, **Icon layout**, and **Icon alignment**.</span></span>

<span data-ttu-id="b8bf4-192">ตัวอย่างต่อไปนี้เพิ่มไอคอนที่ยึดตามกฎสามข้อ:</span><span class="sxs-lookup"><span data-stu-id="b8bf4-192">The following example adds icons based on three rules:</span></span>

![กล่องโต้ตอบไอคอน](media/desktop-conditional-table-formatting/table-formatting-1-default-table.png)

<span data-ttu-id="b8bf4-194">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b8bf4-194">Select **OK**.</span></span> <span data-ttu-id="b8bf4-195">ด้วยไอคอนที่ใช้กับคอลัมน์ **Affordability** ตามกฎตารางตัวอย่างจะมีลักษณะดังนี้:</span><span class="sxs-lookup"><span data-stu-id="b8bf4-195">With icons applied to the **Affordability** column by rules, the example table looks like this:</span></span>

![ตารางตัวอย่างที่มีไอคอน](media/desktop-conditional-table-formatting/table-formatting-1-default-dialog.png)

## <a name="format-as-web-urls"></a><span data-ttu-id="b8bf4-197">จัดรูปแบบเป็น URL เว็บ</span><span class="sxs-lookup"><span data-stu-id="b8bf4-197">Format as web URLs</span></span>

<span data-ttu-id="b8bf4-198">หากคุณมีคอลัมน์หรือหน่วยวัดที่ประกอบด้วย URL เว็บไซต์ คุณสามารถใช้การจัดรูปแบบตามเงื่อนไขเพื่อใช้ URL เหล่านั้นกับเขตข้อมูลเป็นลิงก์ที่ใช้งานอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="b8bf4-198">If you have a column or measure that contains website URLs, you can use conditional formatting to apply those URLs to fields as active links.</span></span> <span data-ttu-id="b8bf4-199">ตัวอย่างเช่น ตารางต่อไปนี้มีคอลัมน์ **Website** ที่มี URL ของเว็บไซต์สำหรับแต่ละรัฐ:</span><span class="sxs-lookup"><span data-stu-id="b8bf4-199">For example, the following table has a **Website** column with website URLs for each state:</span></span>

![ตารางที่มีคอลัมน์ URL ของเว็บ](media/desktop-conditional-table-formatting/table-formatting-1-diverging.png)

<span data-ttu-id="b8bf4-201">เมื่อต้องการแสดงชื่อรัฐแต่ละชื่อเป็นลิงก์แบบสดไปยังเว็บไซต์ ให้เลือก **การจัดรูปแบบตามเงื่อนไข** สำหรับเขตข้อมูล **State** จากนั้นเลือก **URL ของเว็บ**</span><span class="sxs-lookup"><span data-stu-id="b8bf4-201">To display each state name as a live link to its website, select **Conditional formatting** for the **State** field, and then select **Web URL**.</span></span> <span data-ttu-id="b8bf4-202">ในกล่องโต้ตอบ **URL ของเว็บ** ภายใต้ **ยึดตามเขตข้อมูล** ให้เลือก **เว็บไซต์** จากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b8bf4-202">In the **Web URL** dialog box, under **Based on field**, select **Website**, and then select **OK**.</span></span> 

<span data-ttu-id="b8bf4-203">ด้วยการจัดรูปแบบตาม **URL ของเว็บ** ที่ใช้กับเขตข้อมูล **State** ชื่อรัฐแต่ละชื่อจะเป็นลิงก์ที่ใช้งานไปยังเว็บไซต์ของแต่ละรัฐ</span><span class="sxs-lookup"><span data-stu-id="b8bf4-203">With **Web URL** formatting applied to the **State** field, each state name is an active link to its website.</span></span> <span data-ttu-id="b8bf4-204">ตารางตัวอย่างต่อไปนี้มีการจัดรูปแบบตาม **URL ของเว็บ** ซึ่งนำไปใช้กับคอลัมน์ **State** และ **แถบข้อมูล** แบบเงื่อนไขและ **การจัดรูปแบบพื้นหลัง** ที่ใช้กับคอลัมน์ **Affordability**</span><span class="sxs-lookup"><span data-stu-id="b8bf4-204">The following example table has **Web URL** formatting applied to the **State** column, and conditional **Data bars** and **Background formatting** applied to the **Affordability** column.</span></span> 

![ตารางที่มี URL ของเว็บ แถบข้อมูล และสีพื้นหลัง](media/desktop-conditional-table-formatting/table-formatting-3-default-table.png)

## <a name="totals-and-subtotals"></a><span data-ttu-id="b8bf4-206">ผลรวมทั้งหมดและผลรวมย่อย</span><span class="sxs-lookup"><span data-stu-id="b8bf4-206">Totals and subtotals</span></span>

<span data-ttu-id="b8bf4-207">เริ่มต้นด้วยการเปิดตัวในเดือนเมษายน 2020 คุณสามารถนำกฎการจัดรูปแบบตามเงื่อนไขไปใช้กับผลรวมทั้งหมดและผลรวมย่อย สำหรับวิชวลทั้งของตารางและเมทริกซ์ได้</span><span class="sxs-lookup"><span data-stu-id="b8bf4-207">Beginning with the April 2020 release, you can apply conditional formatting rules to totals and subtotals, for both table and matrix visuals.</span></span> 

<span data-ttu-id="b8bf4-208">คุณสามารถใช้งานกฎการจัดรูปแบบตามเงื่อนไขได้โดยใช้ **นำไปใช้กับ** รายการแบบหล่นลงในการจัดรูปแบบตามเงื่อนไข ตามที่แสดงในรูภาพปต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b8bf4-208">You apply the conditional formatting rules by using the **Apply to** drop-down in conditional formatting, as shown in the following image.</span></span>

![จัดรูปแบบผลรวมทั้งหมดและผลรวมย่อย](media/desktop-conditional-table-formatting/table-formatting-4.png)

<span data-ttu-id="b8bf4-210">คุณต้องตั้งค่าเกณฑ์และช่วงสำหรับกฎการจัดรูปแบบตามเงื่อนไขด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b8bf4-210">You must manually set the thresholds and ranges for conditional formatting rules.</span></span> <span data-ttu-id="b8bf4-211">สำหรับเมทริกซ์ **ค่า** จะอ้างอิงถึงระดับการมองเห็นต่ำสุดของลำดับชั้นเมทริกซ์</span><span class="sxs-lookup"><span data-stu-id="b8bf4-211">For matrices, **Values** will refer to the lowest visible level of the matrix hierarchy.</span></span>


## <a name="considerations-and-limitations"></a><span data-ttu-id="b8bf4-212">ข้อควรพิจารณาและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="b8bf4-212">Considerations and limitations</span></span>
<span data-ttu-id="b8bf4-213">มีข้อควรพิจารณาบางประการที่ควรคำนึงถึงเมื่อทำงานเกี่ยวกับการจัดรูปแบบตารางตามเงื่อนไข:</span><span class="sxs-lookup"><span data-stu-id="b8bf4-213">There are a few considerations to keep in mind when working with conditional table formatting:</span></span>

- <span data-ttu-id="b8bf4-214">การจัดรูปแบบตามเงื่อนไขสามารถใช้ได้เฉพาะกับค่าของวิชวลแบบตารางหรือเมทริกซ์เท่านั้น และไม่นำไปใช้กับผลรวมย่อย ผลรวมทั้งหมด หรือแถว **Total**</span><span class="sxs-lookup"><span data-stu-id="b8bf4-214">Conditional formatting applies only to the values of Table or Matrix visuals, and doesn't apply to any subtotals, grand totals, or the **Total** row.</span></span> 
- <span data-ttu-id="b8bf4-215">ตารางใดก็ตามที่ไม่มีการจัดกลุ่มจะแสดงเป็นแถวเดียวที่ไม่สนับสนุนการจัดรูปแบบตามเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="b8bf4-215">Any table that doesn't have a grouping is displayed as a single row that doesn't support conditional formatting.</span></span>
- <span data-ttu-id="b8bf4-216">คุณไม่สามารถใช้การจัดรูปแบบไล่ระดับสีด้วยค่าสูงสุด/ต่ำสุดอัตโนมัติ หรือการจัดรูปแบบตามกฎที่มีกฎเปอร์เซ็นต์ได้ หากข้อมูลของคุณประกอบด้วยค่า *NaN*</span><span class="sxs-lookup"><span data-stu-id="b8bf4-216">You can't apply gradient formatting with automatic maximum/minimum values, or rule-based formatting with percentage rules, if your data contains *NaN* values.</span></span> <span data-ttu-id="b8bf4-217">NaN หมายถึง "ไม่ใช่ตัวเลข" ซึ่งเกิดจากการหารด้วยค่าศูนย์ที่ผิดพลาดโดยทั่วไปมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="b8bf4-217">NaN means "Not a number," most commonly caused by a divide by zero error.</span></span> <span data-ttu-id="b8bf4-218">คุณสามารถใช้[ฟังก์ชัน DIVIDE() DAX ](/dax/divide-function-dax) เพื่อหลีกเลี่ยงข้อผิดพลาดเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="b8bf4-218">You can use the [DIVIDE() DAX function](/dax/divide-function-dax) to avoid these errors.</span></span>
- <span data-ttu-id="b8bf4-219">การจัดรูปแบบตามเงื่อนไขต้องการการรวมหรือหน่วยวัดที่จะนำไปใช้กับค่า</span><span class="sxs-lookup"><span data-stu-id="b8bf4-219">Conditional formatting needs an aggregation or measure to be applied to the value.</span></span> <span data-ttu-id="b8bf4-220">ด้วยเหตุนี้คุณจึงเห็น 'First' หรือ 'Last' ในตัวอย่าง **สีตามค่า**</span><span class="sxs-lookup"><span data-stu-id="b8bf4-220">That's why you see 'First' or 'Last' in the **Color by value** example.</span></span> <span data-ttu-id="b8bf4-221">ถ้าคุณกำลังสร้างรายงานของคุณกับลูกบาศก์แบบหลายมิติของ Analysis Services คุณจะไม่สามารถใช้แอตทริบิวต์สำหรับการจัดรูปแบบตามเงื่อนไขได้เว้นแต่ว่าเจ้าของลูกบาศก์ได้สร้างหน่วยวัดที่ให้ค่า</span><span class="sxs-lookup"><span data-stu-id="b8bf4-221">If you're building your report against an Analysis Service multidimensional cube, you won't be able to use an attribute for conditional formatting unless the cube owner has built a measure that provides the value.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b8bf4-222">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="b8bf4-222">Next steps</span></span>

<span data-ttu-id="b8bf4-223">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดรูปแบบสี โปรดดู [เคล็ดลับและลูกเล่นในการจัดรูปแบบสีใน Power BI](../visuals/service-tips-and-tricks-for-color-formatting.md)</span><span class="sxs-lookup"><span data-stu-id="b8bf4-223">For more information about color formatting, see [Tips and tricks for color formatting in Power BI](../visuals/service-tips-and-tricks-for-color-formatting.md)</span></span>