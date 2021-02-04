---
title: เคล็ดลับประสิทธิภาพในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: วิธีการสร้างวิชวล Power BI ประสิทธิภาพสูง เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: how-to
ms.date: 04/20/2020
ms.openlocfilehash: c8bcf5e13ba769b976ab123adb3ba37f46b0359e
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97885947"
---
# <a name="how-to-build-a-high-performance-power-bi-visual"></a><span data-ttu-id="75d7e-104">วิธีการสร้างวิชวล Power BI ประสิทธิภาพสูง</span><span class="sxs-lookup"><span data-stu-id="75d7e-104">How to build a high performance Power BI visual</span></span>
<span data-ttu-id="75d7e-105">บทความนี้จะครอบคลุมเทคนิคเกี่ยวกับวิธีที่นักพัฒนาสามารถทำงานได้อย่างมีประสิทธิภาพสูงเมื่อแสดงวิชวล</span><span class="sxs-lookup"><span data-stu-id="75d7e-105">This article will cover techniques on how a developer can achieve high performance when rendering visuals.</span></span> 

<span data-ttu-id="75d7e-106">ไม่มีใครต้องการให้วิชวลใช้เวลาในการแสดงผลและการบีบลดประสิทธิภาพลงทุกครั้งที่คุณสามารถออกจากรหัสได้กลายเป็นสิ่งสำคัญเมื่อการแสดงผล</span><span class="sxs-lookup"><span data-stu-id="75d7e-106">No one wants a visual to take its time when rendering and squeezing every drop of performance you can out of code becomes critical when rendering.</span></span> 

> [!NOTE]
> <span data-ttu-id="75d7e-107">ในขณะที่เรายังคงพัฒนาและปรับปรุงแพลตฟอร์ม จะมีการเผยแพร่เวอร์ชันใหม่ของ API อย่างต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="75d7e-107">As we continue to improve and enhance the platform, new versions of the API are constantly being released.</span></span> <span data-ttu-id="75d7e-108">เพื่อให้ได้ประโยชน์สูงสุดจากแพลตฟอร์มและชุดคุณลักษณะของวิชวล Power BI แนะนำให้คุณอัปเดตเป็นเวอร์ชันล่าสุดอยู่เสมอ</span><span class="sxs-lookup"><span data-stu-id="75d7e-108">In order to get the most out of the Power BI visuals' platform and feature set, it's recommended you keep up-to-date with the most recent version.</span></span>
>
> <span data-ttu-id="75d7e-109">นับตั้งแต่ **เวอร์ชัน 2.1** ล่าสุด เวลาการโหลดวิชวล Power BI ได้รับการปรับปรุงโดยเฉลี่ย 20%</span><span class="sxs-lookup"><span data-stu-id="75d7e-109">Since the latest **version 2.1**, Power BI visual load times have improved on average by 20%.</span></span>

## <a name="power-bi-visual-performance-tips"></a><span data-ttu-id="75d7e-110">เคล็ดลับประสิทธิภาพการทำงานของวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="75d7e-110">Power BI visual performance tips</span></span>
<span data-ttu-id="75d7e-111">ต่อไปนี้เป็นคำแนะนำเกี่ยวกับวิธีการทำให้วิชวลมีประสิทธิภาพที่ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="75d7e-111">Here are some recommendations on how to achieve optimal visual performance.</span></span> 

### <a name="use-user-timing-api"></a><span data-ttu-id="75d7e-112">ใช้ API ไทม์มิ่งของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="75d7e-112">Use User Timing API</span></span>
<span data-ttu-id="75d7e-113">การใช้ **API ไทม์มิ่งของผู้ใช้** ในการวัดประสิทธิภาพ JavaScript ของแอปสามารถช่วยให้คุณตัดสินใจได้ว่าส่วนใดของสคริปต์ที่จำเป็นต้องปรับให้เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="75d7e-113">Using the **User Timing API** to measure your app's JavaScript performance can help you decide which parts of the script need optimization.</span></span>

<span data-ttu-id="75d7e-114">สำหรับข้อมูลเพิ่มเติม ให้ดู [API ไทม์มิ่งของผู้ใช้](https://msdn.microsoft.com/library/hh772738(v=vs.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="75d7e-114">For more information, see the [User Timing API](https://msdn.microsoft.com/library/hh772738(v=vs.85).aspx).</span></span>

### <a name="review-animation-loops"></a><span data-ttu-id="75d7e-115">ตรวจสอบการวนรอบของภาพเคลื่อนไหว</span><span class="sxs-lookup"><span data-stu-id="75d7e-115">Review animation loops</span></span>
<span data-ttu-id="75d7e-116">การวนรอบภาพเคลื่อนไหวจะวาดองค์ประกอบที่ไม่เปลี่ยนแปลงใหม่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="75d7e-116">Does the animation loop redraw unchanged elements?</span></span> 

 - <span data-ttu-id="75d7e-117">ปัญหา: การดำเนินการดังกล่าวจะทำให้เสียเวลาในการวาดองค์ประกอบที่ไม่มีการเปลี่ยนแปลงจากเฟรมต่อเฟรม</span><span class="sxs-lookup"><span data-stu-id="75d7e-117">Problem: It wastes time to draw elements that don’t change from frame-to-frame.</span></span>

 - <span data-ttu-id="75d7e-118">วิธีการแก้ไข: ปรับปรุงเฟรมที่เลือก</span><span class="sxs-lookup"><span data-stu-id="75d7e-118">Solution: Update frames selectively.</span></span> 
 
<span data-ttu-id="75d7e-119">เมื่อถึงเวลาที่จะเคลื่อนไหวการแสดงภาพแบบคงที่ การแสดงภาพแบบคงที่จะพยายามรวมรหัสการวาดเป็นฟังก์ชันการอัปเดตเดียว และใช้งานซ้ำได้ด้วยข้อมูลใหม่สำหรับการทำซ้ำแต่ละครั้งของการวนรอบของภาพเคลื่อนไหว</span><span class="sxs-lookup"><span data-stu-id="75d7e-119">When the time comes to animate static visualizations, it’s tempting to lump draw code into one update function and repeatedly call it with new data for each iteration of the animation loop.</span></span>

<span data-ttu-id="75d7e-120">โปรดพิจารณารูปแบบการอัปเดตดังต่อไปนี้ ใช้วิธีการสร้างวิชวลเพื่อวาดทุกอย่างแบบคงที่ จากนั้นฟังก์ชันอัปเดตจะต้องวาดเฉพาะองค์ประกอบการแสดงภาพที่เปลี่ยนแปลงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="75d7e-120">Instead consider the following update pattern, use a visual constructor method to draw everything static, then the update function only needs to draw visualization elements that change.</span></span> 

   > [!TIP]
   > <span data-ttu-id="75d7e-121">การวนรอบของภาพเคลื่อนไหวที่ไม่มีประสิทธิภาพจะพบได้ทั่วไปในแกนและคำอธิบายแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="75d7e-121">Inefficient animation loops are commonly found in axes and legends.</span></span>

### <a name="cache-dom-nodes"></a><span data-ttu-id="75d7e-122">โหนด DOM แคช</span><span class="sxs-lookup"><span data-stu-id="75d7e-122">Cache DOM Nodes</span></span> 
<span data-ttu-id="75d7e-123">เมื่อมีการเรียกใช้โหนดหรือรายการของโหนดจาก DOM คุณจะต้องคิดว่าคุณสามารถนำมาใช้ใหม่ได้ในการคำนวณภายหลัง (บางครั้งแม้แต่การทำซ้ำในการวนรอบถัดไป)</span><span class="sxs-lookup"><span data-stu-id="75d7e-123">When a node or list of nodes is retrieved from the DOM, you need to think about whether you can reuse them in later computations (sometimes even the next loop iteration).</span></span> <span data-ttu-id="75d7e-124">ตราบใดที่คุณไม่จำเป็นต้องเพิ่มหรือลบโหนดเพิ่มเติมในพื้นที่ที่เกี่ยวข้อง การแคชโหนดเหล่านั้นสามารถปรับปรุงประสิทธิภาพโดยรวมของแอปพลิเคชันของคุณได้</span><span class="sxs-lookup"><span data-stu-id="75d7e-124">As long as you don't need to add or delete additional nodes in the relevant area, caching them can improve your application's overall efficiency.</span></span>

<span data-ttu-id="75d7e-125">หากต้องการตรวจสอบให้แน่ใจว่ารหัสของคุณรวดเร็วและไม่ทำให้เบราว์เซอร์ช้าลง ให้รักษาการเข้าถึง DOM ไว้ที่ระดับต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="75d7e-125">To make sure that your code is fast and doesn’t slow down the browser, keep DOM access to a minimum.</span></span> 

- <span data-ttu-id="75d7e-126">ก่อน:</span><span class="sxs-lookup"><span data-stu-id="75d7e-126">Before:</span></span> 

   ```javascript
   public update(options: VisualUpdateOptions) { 
       let axis = $(".axis"); 
   }
   ```

- <span data-ttu-id="75d7e-127">หลัง:</span><span class="sxs-lookup"><span data-stu-id="75d7e-127">After:</span></span> 

   ```javascript
   public constructor(options: VisualConstructorOptions) { 
       this.$root = $(options.element); 
       this.xAxis = this.$root.find(".xAxis"); 
   } 
 
   public update(options: VisualUpdateOptions) { 
       let axis = this.axis; 
   }
   ```

### <a name="avoid-dom-manipulation"></a><span data-ttu-id="75d7e-128">หลีกเลี่ยงการจัดการ DOM</span><span class="sxs-lookup"><span data-stu-id="75d7e-128">Avoid DOM manipulation</span></span> 
<span data-ttu-id="75d7e-129">จำกัดการจัดการ DOM ให้มากที่สุดเท่าที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="75d7e-129">Limit DOM manipulation as much as possible.</span></span>  <span data-ttu-id="75d7e-130">การแทรกการดำเนินการเช่น `prepend()`, `append()`และ `after()` ใช้เวลานาน และไม่ควรใช้เว้นแต่ว่าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="75d7e-130">Insert operations like `prepend()`, `append()`, and `after()` are time-consuming and shouldn't be used unless necessary.</span></span>

<span data-ttu-id="75d7e-131">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="75d7e-131">For instance:</span></span>

  ```javascript
  for (let i=0; i<1000; i++) { 
      $('#list').append('<li>'+i+'</li>');
  }
  ```

<span data-ttu-id="75d7e-132">ตัวอย่างข้างต้นอาจถูกทำให้เร็วขึ้นโดยใช้ `html()` และสร้างรายการล่วงหน้า:</span><span class="sxs-lookup"><span data-stu-id="75d7e-132">The above example could be quickened using `html()` and building the list beforehand:</span></span> 

  ```javascript
  let list = ''; 
  for (let i=0; i<1000; i++) { 
      list += '<li>'+i+'</li>'; 
  } 

  $('#list').html(list); 
  ```

### <a name="reconsider-jquery"></a><span data-ttu-id="75d7e-133">พิจารณา JQuery อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="75d7e-133">Reconsider JQuery</span></span>

<span data-ttu-id="75d7e-134">การจำกัดเฟรมเวิร์ก JS ของคุณและการใช้ JS แบบดั้งเดิมเมื่อใดก็ตามที่เป็นไปได้สามารถเพิ่มแบนด์วิดท์ที่มีอยู่ และลดค่าใช้จ่ายในการประมวลผลของคุณได้</span><span class="sxs-lookup"><span data-stu-id="75d7e-134">Limiting your JS frameworks and using native JS whenever possible can increase the available bandwidth and lower your processing overhead.</span></span> <span data-ttu-id="75d7e-135">นอกจากนี้ยังสามารถจำกัดปัญหาความเข้ากันได้กับเบราว์เซอร์รุ่นเก่าได้</span><span class="sxs-lookup"><span data-stu-id="75d7e-135">This can also limit compatibility issues with older browsers.</span></span> 

<span data-ttu-id="75d7e-136">สำหรับข้อมูลเพิ่มเติม โปรดดู [youmightnotneedjquery.com](http://youmightnotneedjquery.com/) สำหรับตัวอย่างทางเลือกในฟังก์ชันเช่น `show`, `hide`, `addClass` ของ JQuery และอื่นๆ อีกมากมาย</span><span class="sxs-lookup"><span data-stu-id="75d7e-136">For more information, see [youmightnotneedjquery.com](http://youmightnotneedjquery.com/) for alternative examples to functions such as JQuery's `show`, `hide`, `addClass`, and more.</span></span>  

### <a name="use-canvas-or-webgl"></a><span data-ttu-id="75d7e-137">ใช้พื้นที่ทำงานหรือ WebGL</span><span class="sxs-lookup"><span data-stu-id="75d7e-137">Use canvas or WebGL</span></span> 
<span data-ttu-id="75d7e-138">สำหรับการใช้ภาพเคลื่อนไหวซ้ำ ให้พิจารณาการใช้ **พื้นที่ทำงาน** หรือ **WebGL** แทนที่จะเป็น SVG</span><span class="sxs-lookup"><span data-stu-id="75d7e-138">For repeated use of animations consider using **Canvas** or **WebGL** instead of SVG.</span></span> <span data-ttu-id="75d7e-139">ซึ่งแตกต่างจาก SVG เพราะว่าประสิทธิภาพการทำงานของตัวเลือกเหล่านี้จะถูกกำหนดโดยขนาดแทนที่จะเป็นเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="75d7e-139">Unlike SVG, with these options performance is determined by size rather than content.</span></span> 

<span data-ttu-id="75d7e-140">คุณสามารถอ่านเพิ่มเติมเกี่ยวกับความแตกต่างใน [SVG กับ พื้นที่ทำงาน: วิธีการเลือก](/previous-versions/windows/internet-explorer/ie-developer/samples/gg193983(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="75d7e-140">You can read more about the differences in [SVG vs Canvas: How to Choose](/previous-versions/windows/internet-explorer/ie-developer/samples/gg193983(v=vs.85)).</span></span> 

### <a name="use-requestanimationframe-instead-of-settimeout"></a><span data-ttu-id="75d7e-141">ใช้ requestAnimationFrame แทน setTimeout</span><span class="sxs-lookup"><span data-stu-id="75d7e-141">Use requestAnimationFrame instead of setTimeout</span></span> 
<span data-ttu-id="75d7e-142">ถ้าคุณใช้ [requestAnimationFrame](https://www.w3.org/TR/animation-timing/) เพื่ออัปเดตภาพเคลื่อนไหวบนหน้าจอ ฟังก์ชันภาพเคลื่อนไหวของคุณจะเรียกว่า **ก่อน** เบราว์เซอร์จะเรียกว่าการทำสีใหม่อีกอย่าง</span><span class="sxs-lookup"><span data-stu-id="75d7e-142">If you use [requestAnimationFrame](https://www.w3.org/TR/animation-timing/) to update your on-screen animations, your animation functions are called **before** the browser calls another repaint.</span></span>

<span data-ttu-id="75d7e-143">สำหรับข้อมูลเพิ่มเติม โปรดด[ูตัวอย่าง](https://testdrive-archive.azurewebsites.net/Graphics/RequestAnimationFrame/Default.html)นี้เกี่ยวกับภาพเคลื่อนไหวที่ราบรื่นโดยใช้ `requestAnimationFrame`</span><span class="sxs-lookup"><span data-stu-id="75d7e-143">For more information, see this [sample](https://testdrive-archive.azurewebsites.net/Graphics/RequestAnimationFrame/Default.html) on smooth animation using `requestAnimationFrame`.</span></span>

## <a name="next-steps"></a><span data-ttu-id="75d7e-144">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="75d7e-144">Next steps</span></span>

<span data-ttu-id="75d7e-145">เรียนรู้เพิ่มเติมเกี่ยวกับเทคนิคการเพิ่มประสิทธิภาพใน[คำแนะนำการปรับให้เหมาะสมสำหรับ Power BI](../../guidance/power-bi-optimization.md)</span><span class="sxs-lookup"><span data-stu-id="75d7e-145">Learn more about optimization techniques in the [Optimization guide for Power BI](../../guidance/power-bi-optimization.md).</span></span>