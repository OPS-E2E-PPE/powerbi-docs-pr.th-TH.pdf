---
title: ตัวแก้ไขสูตรใน Power BI Desktop
description: สร้าง และแก้ไขสูตร DAX ใน Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-transform-model
ms.topic: conceptual
ms.date: 05/08/2019
LocalizationGroup: Transform and shape data
ms.openlocfilehash: 78132a180035971df8a0ffb18af9ef16d276bd4d
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415737"
---
# <a name="formula-editor-in-power-bi-desktop"></a><span data-ttu-id="942b5-103">ตัวแก้ไขสูตรใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="942b5-103">Formula editor in Power BI Desktop</span></span>

<span data-ttu-id="942b5-104">เริ่มต้นด้วย **Power BI Desktop** ที่เผยแพร่ในเดือนตุลาคม ค.ศ. 2018 ตัวแก้ไขสูตร (มักเรียกว่าตัวแก้ไข DAX) ประกอบด้วยการแก้ไขอย่างจริงจังและการปรับปรุงทางลัดเพื่อให้การเขียนและแก้ไขสูตรง่ายขึ้นและใช้งานได้ง่ายยิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="942b5-104">Beginning with the October 2018 **Power BI Desktop** release, the formula editor (often referred to as the DAX editor) includes robust editing and shortcut enhancements to make authoring and editing formulas easier and more intuitive.</span></span> 

## <a name="using-the-formula-editor"></a><span data-ttu-id="942b5-105">ใช้ตัวแก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="942b5-105">Using the formula editor</span></span>

<span data-ttu-id="942b5-106">คุณสามารถใช้แป้นพิมพ์ลัดต่อไปนี้ เพื่อเพิ่มประสิทธิภาพการทำงานของคุณ และเพิ่มประสิทธิภาพการสร้างสูตรในตัวแก้ไขสูตร</span><span class="sxs-lookup"><span data-stu-id="942b5-106">You can use the following keyboard shortcuts to increase your productivity and to streamline creating formulas in the formula editor.</span></span>


|<span data-ttu-id="942b5-107">คำสั่งแป้นพิมพ์</span><span class="sxs-lookup"><span data-stu-id="942b5-107">Keyboard Command</span></span>  |<span data-ttu-id="942b5-108">ผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="942b5-108">Result</span></span>  |
|---------|---------|
|<span data-ttu-id="942b5-109">Ctrl+C</span><span class="sxs-lookup"><span data-stu-id="942b5-109">Ctrl+C</span></span>  | <span data-ttu-id="942b5-110">คัดลอกบรรทัด (ไม่มีรายการที่เลือก)</span><span class="sxs-lookup"><span data-stu-id="942b5-110">Copy line (empty selection)</span></span> |
|<span data-ttu-id="942b5-111">Ctrl+G</span><span class="sxs-lookup"><span data-stu-id="942b5-111">Ctrl+G</span></span>  |<span data-ttu-id="942b5-112">ไปที่บรรทัด...</span><span class="sxs-lookup"><span data-stu-id="942b5-112">Go to line…</span></span> |
|<span data-ttu-id="942b5-113">Ctrl+I</span><span class="sxs-lookup"><span data-stu-id="942b5-113">Ctrl+I</span></span>  |<span data-ttu-id="942b5-114">เลือกบรรทัดปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="942b5-114">Select current line</span></span>  |
|<span data-ttu-id="942b5-115">Ctrl+M</span><span class="sxs-lookup"><span data-stu-id="942b5-115">Ctrl+M</span></span>  |<span data-ttu-id="942b5-116">สลับแท็บย้ายโฟกัส</span><span class="sxs-lookup"><span data-stu-id="942b5-116">Toggle Tab moves focus</span></span> |
|<span data-ttu-id="942b5-117">Ctrl + U</span><span class="sxs-lookup"><span data-stu-id="942b5-117">Ctrl+U</span></span>  |<span data-ttu-id="942b5-118">เลิกทำการดำเนินการของเคอร์เซอร์ล่าสุด</span><span class="sxs-lookup"><span data-stu-id="942b5-118">Undo last cursor operation</span></span>  |
|<span data-ttu-id="942b5-119">Ctrl+X</span><span class="sxs-lookup"><span data-stu-id="942b5-119">Ctrl+X</span></span>   | <span data-ttu-id="942b5-120">ตัดบรรทัด (ไม่มีรายการที่เลือก)</span><span class="sxs-lookup"><span data-stu-id="942b5-120">Cut line (empty selection)</span></span> |
|<span data-ttu-id="942b5-121">Ctrl+Enter</span><span class="sxs-lookup"><span data-stu-id="942b5-121">Ctrl+Enter</span></span>  |<span data-ttu-id="942b5-122">แทรกบรรทัดด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="942b5-122">Insert line below</span></span>  |
|<span data-ttu-id="942b5-123">Ctrl+Shift+Enter</span><span class="sxs-lookup"><span data-stu-id="942b5-123">Ctrl+Shift+Enter</span></span>  |<span data-ttu-id="942b5-124">แทรกบรรทัดด้านบน</span><span class="sxs-lookup"><span data-stu-id="942b5-124">Insert line above</span></span>  |
|<span data-ttu-id="942b5-125">Ctrl+Shift+</span><span class="sxs-lookup"><span data-stu-id="942b5-125">Ctrl+Shift+</span></span>\  |<span data-ttu-id="942b5-126">ข้ามไปยังวงเล็บที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="942b5-126">Jump to matching bracket</span></span>  |
|<span data-ttu-id="942b5-127">Ctrl+Shift+K</span><span class="sxs-lookup"><span data-stu-id="942b5-127">Ctrl+Shift+K</span></span>  |<span data-ttu-id="942b5-128">ลบบรรทัด</span><span class="sxs-lookup"><span data-stu-id="942b5-128">Delete line</span></span>  |
|<span data-ttu-id="942b5-129">Ctrl+] / [</span><span class="sxs-lookup"><span data-stu-id="942b5-129">Ctrl+] / [</span></span>  |<span data-ttu-id="942b5-130">เยื้องบรรทัดเข้า/เยื้องบรรทัดออก</span><span class="sxs-lookup"><span data-stu-id="942b5-130">Indent/outdent line</span></span>  |
|<span data-ttu-id="942b5-131">Ctrl + Home</span><span class="sxs-lookup"><span data-stu-id="942b5-131">Ctrl+Home</span></span>  |<span data-ttu-id="942b5-132">ไปที่จุดเริ่มต้นของไฟล์</span><span class="sxs-lookup"><span data-stu-id="942b5-132">Go to beginning of file</span></span>  |
|<span data-ttu-id="942b5-133">Ctrl + End</span><span class="sxs-lookup"><span data-stu-id="942b5-133">Ctrl+End</span></span>  |<span data-ttu-id="942b5-134">ไปที่จุดสิ้นสุดของไฟล์</span><span class="sxs-lookup"><span data-stu-id="942b5-134">Go to end of file</span></span>  |
|<span data-ttu-id="942b5-135">Ctrl+↑ / ↓</span><span class="sxs-lookup"><span data-stu-id="942b5-135">Ctrl+↑ / ↓</span></span>   |<span data-ttu-id="942b5-136">เลื่อนบรรทัดขึ้น/ลง</span><span class="sxs-lookup"><span data-stu-id="942b5-136">Scroll line up/down</span></span>  |
|<span data-ttu-id="942b5-137">Ctrl + Shift + Alt + (แป้นลูกศร)</span><span class="sxs-lookup"><span data-stu-id="942b5-137">Ctrl+Shift+Alt + (arrow key)</span></span>  |<span data-ttu-id="942b5-138">เลือกคอลัมน์ (กล่อง)</span><span class="sxs-lookup"><span data-stu-id="942b5-138">Column (box) selection</span></span>  |
|<span data-ttu-id="942b5-139">Ctrl+Shift+Alt +PgUp/PgDn</span><span class="sxs-lookup"><span data-stu-id="942b5-139">Ctrl+Shift+Alt +PgUp/PgDn</span></span>  |<span data-ttu-id="942b5-140">เลื่อนหน้าการเลือกคอลัมน์ (กล่อง) ขึ้น/ลง</span><span class="sxs-lookup"><span data-stu-id="942b5-140">Column (box) selection page up/down</span></span> |
|<span data-ttu-id="942b5-141">Ctrl+Shift+L</span><span class="sxs-lookup"><span data-stu-id="942b5-141">Ctrl+Shift+L</span></span>  |<span data-ttu-id="942b5-142">เลือกสิ่งที่ปรากฏทั้งหมดของสิ่งที่เลือกปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="942b5-142">Select all occurrences of current selection</span></span> |
|<span data-ttu-id="942b5-143">Ctrl+Alt+ ↑ / ↓</span><span class="sxs-lookup"><span data-stu-id="942b5-143">Ctrl+Alt+ ↑ / ↓</span></span>  |<span data-ttu-id="942b5-144">แทรกเคอร์เซอร์บน/ล่าง</span><span class="sxs-lookup"><span data-stu-id="942b5-144">Insert cursor above / below</span></span>  |
|<span data-ttu-id="942b5-145">Ctrl+F2</span><span class="sxs-lookup"><span data-stu-id="942b5-145">Ctrl+F2</span></span>  |<span data-ttu-id="942b5-146">เลือกสิ่งที่ปรากฏทั้งหมดของคำที่เลือกปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="942b5-146">Select all occurrences of current word</span></span> | 
|<span data-ttu-id="942b5-147">Shift + Alt + (ลากเมาส์)</span><span class="sxs-lookup"><span data-stu-id="942b5-147">Shift+Alt + (drag mouse)</span></span> |<span data-ttu-id="942b5-148">เลือกคอลัมน์ (กล่อง)</span><span class="sxs-lookup"><span data-stu-id="942b5-148">Column (box) selection</span></span>  |
|<span data-ttu-id="942b5-149">Shift+Alt + ↓ / ↑</span><span class="sxs-lookup"><span data-stu-id="942b5-149">Shift+Alt + ↓ / ↑</span></span>  |<span data-ttu-id="942b5-150">คัดลอกบรรทัดขึ้น/ลง</span><span class="sxs-lookup"><span data-stu-id="942b5-150">Copy line up/down</span></span>  |
|<span data-ttu-id="942b5-151">Shift+Alt+→</span><span class="sxs-lookup"><span data-stu-id="942b5-151">Shift+Alt+→</span></span>  |<span data-ttu-id="942b5-152">ขยายส่วนที่เลือก</span><span class="sxs-lookup"><span data-stu-id="942b5-152">Expand selection</span></span>  |
|<span data-ttu-id="942b5-153">Shift+Alt+←</span><span class="sxs-lookup"><span data-stu-id="942b5-153">Shift+Alt+←</span></span>  |<span data-ttu-id="942b5-154">ลดขนาดส่วนที่เลือก</span><span class="sxs-lookup"><span data-stu-id="942b5-154">Shrink selection</span></span> |
|<span data-ttu-id="942b5-155">Shift+Alt+I</span><span class="sxs-lookup"><span data-stu-id="942b5-155">Shift+Alt+I</span></span>  |<span data-ttu-id="942b5-156">แทรกเคอร์เซอร์ที่จุดสิ้นสุดของแต่ละบรรทัดที่เลือก</span><span class="sxs-lookup"><span data-stu-id="942b5-156">Insert cursor at end of each line selected</span></span> |
|<span data-ttu-id="942b5-157">Alt+ ↑ / ↓</span><span class="sxs-lookup"><span data-stu-id="942b5-157">Alt+ ↑ / ↓</span></span>  | <span data-ttu-id="942b5-158">คัดลอกบรรทัดขึ้น/ลง</span><span class="sxs-lookup"><span data-stu-id="942b5-158">Move line up/down</span></span> |
|<span data-ttu-id="942b5-159">Alt+PgUp / PgDn</span><span class="sxs-lookup"><span data-stu-id="942b5-159">Alt+PgUp / PgDn</span></span>  |<span data-ttu-id="942b5-160">เลื่อนหน้าขึ้น/ลง</span><span class="sxs-lookup"><span data-stu-id="942b5-160">Scroll page up/down</span></span>  |
|<span data-ttu-id="942b5-161">Alt + คลิก</span><span class="sxs-lookup"><span data-stu-id="942b5-161">Alt+Click</span></span>  |<span data-ttu-id="942b5-162">แทรกเคอร์เซอร์</span><span class="sxs-lookup"><span data-stu-id="942b5-162">Insert cursor</span></span>  |
|<span data-ttu-id="942b5-163">หน้าแรก / สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="942b5-163">Home / End</span></span>  |<span data-ttu-id="942b5-164">ไปที่จุดเริ่มต้น/สิ้นสุดของบรรทัด</span><span class="sxs-lookup"><span data-stu-id="942b5-164">Go to beginning/end of line</span></span>  |

## <a name="next-steps"></a><span data-ttu-id="942b5-165">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="942b5-165">Next steps</span></span>

<span data-ttu-id="942b5-166">บทความต่อไปนี้แสดงข้อมูลเพิ่มเติมเกี่ยวกับสูตรและ DAX ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="942b5-166">The following articles provide more information about formulas and DAX in Power BI Desktop.</span></span>

* [<span data-ttu-id="942b5-167">พื้นฐาน DAX ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="942b5-167">DAX basics in Power BI Desktop</span></span>](desktop-quickstart-learn-dax-basics.md)
* <span data-ttu-id="942b5-168">[DAX ใน Power BI Desktop](/learn/paths/dax-power-bi/) หลักสูตร Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="942b5-168">[DAX in Power BI Desktop](/learn/paths/dax-power-bi/) Microsoft Learn course</span></span>
* [<span data-ttu-id="942b5-169">การอ้างอิงเกี่ยวกับ DAX</span><span class="sxs-lookup"><span data-stu-id="942b5-169">DAX reference</span></span>](/dax/)