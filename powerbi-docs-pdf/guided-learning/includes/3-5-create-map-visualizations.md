---
ms.openlocfilehash: 033436e7078723508d6b9481807ace424c3f109f
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2019
ms.locfileid: "61397979"
---
<span data-ttu-id="63443-101">Power BI มีการจัดรูปแบบการแสดงข้อมูลแผนที่ที่แตกต่างกันอยู่สองชนิดคือ: แผนที่แบบฟองที่วางฟองเหนือจุดทางภูมิศาสตร์ และแผนที่รูปร่างที่แสดงเค้าร่างของพื้นที่ที่คุณต้องการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="63443-101">Power BI has two different types of map visualizations: a bubble map that places a bubble over a geographic point, and a shape map that actually shows the outline of area you want to visualize.</span></span>

![](media/3-5-create-map-visualizations/3-5_1.png)

> [!NOTE]
> <span data-ttu-id="63443-102">เมื่อทำงานกับประเทศหรือภูมิภาค ให้ใช้ตัวย่อสามตัวเพื่อให้แน่ใจว่าการเข้ารหัสทางภูมิศาสตร์ทำงานได้อย่างถูกต้องในการจัดรูปแบบการแสดงข้อมูลแผนที่</span><span class="sxs-lookup"><span data-stu-id="63443-102">When working with countries or regions, use the three-letter abbreviation to ensure that geocoding works properly in map visualizations.</span></span> <span data-ttu-id="63443-103">*อย่า*ใช้ตัวย่อสองตัวอักษร เนื่องจากอาจไม่รู้จักบางประเทศหรือบางภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="63443-103">Do *not* use two-letter abbreviations, as some countries or regions may not be properly recognized.</span></span>
> <span data-ttu-id="63443-104">ถ้าคุณมีเพียงตัวย่อสองตัว ให้ดู[บล็อกโพสต์ภายนอกนี้](https://blog.ailon.org/how-to-display-2-letter-country-data-on-a-power-bi-map-85fc738497d6#.yudauacxp)สำหรับขั้นตอนวิธีการเชื่อมโยงตัวย่อประเทศ/ภูมิภาคแบบสองตัวของคุณเข้ากับตัวย่อประเทศ/ภูมิภาคแบบสามตัว</span><span class="sxs-lookup"><span data-stu-id="63443-104">If you only have two-letter abbreviations, check out [this external blog post](https://blog.ailon.org/how-to-display-2-letter-country-data-on-a-power-bi-map-85fc738497d6#.yudauacxp) for steps on how to associate your two-letter country/region abbreviations with three-letter country/region abbreviations.</span></span>
> 
> 

## <a name="create-bubble-maps"></a><span data-ttu-id="63443-105">สร้างแผนที่แบบฟอง</span><span class="sxs-lookup"><span data-stu-id="63443-105">Create bubble maps</span></span>
<span data-ttu-id="63443-106">เมื่อต้องการสร้างแผนที่แบบฟอง ให้เลือกตัวตัวเลือก **แผนที่** ในบานหน้าต่าง **การจัดรูปแบบการแสดงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="63443-106">To create a bubble map, select the **Map** option in the **Visualization** pane.</span></span> <span data-ttu-id="63443-107">คุณต้องเพิ่มค่าไปยังบักเก็ต *ตำแหน่งที่ตั้ง* ในตัวเลือก **การจัดรูปแบบการแสดงข้อมูล** เพื่อใช้การแสดงผลด้วยภาพแผนที่</span><span class="sxs-lookup"><span data-stu-id="63443-107">You must add a value to the *Location* bucket in the **Visualizations** options to use a map visual.</span></span>

![](media/3-5-create-map-visualizations/3-5_2.png)

<span data-ttu-id="63443-108">Power BI มีความยืดหยุ่นเกี่ยวกับชนิดของค่าตำแหน่งที่ตั้งที่ยอมรับ ตั้งแต่รายละเอียดเพิ่มเติม เช่น ชื่อเมืองหรือรหัสสนามบินลงไป จนถึงข้อมูลละติจูดและลองจิจูดที่เฉพาะเจาะจงอย่างมาก</span><span class="sxs-lookup"><span data-stu-id="63443-108">Power BI is flexible about what type of location value it accepts, from more general details like city name or airport code, down to very specific latitude and longitude data.</span></span> <span data-ttu-id="63443-109">เพิ่มเขตข้อมูลไปยังบักเก็ต **ขนาด** เพื่อเปลี่ยนขนาดของฟองตามแต่ละตำแหน่งที่ตั้งของแผนที่</span><span class="sxs-lookup"><span data-stu-id="63443-109">Add a field to the **Size** bucket to change the size of the bubble accordingly for each map location.</span></span>

![](media/3-5-create-map-visualizations/3-5_3.png)

## <a name="create-shape-maps"></a><span data-ttu-id="63443-110">สร้างแผนที่รูปร่าง</span><span class="sxs-lookup"><span data-stu-id="63443-110">Create shape maps</span></span>
<span data-ttu-id="63443-111">เมื่อต้องการสร้างแผนที่รูปร่าง ให้เลือกตัวเลือก **แผนที่แถบสี** ในบานหน้าต่างการจัดรูปแบบการแสดงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="63443-111">To create a shape map, select the **Filled Map** option in the Visualization pane.</span></span> <span data-ttu-id="63443-112">เช่นเดียวกับแผนที่แบบฟอง คุณต้องเพิ่มค่าให้กับบักเก็ตตำแหน่งที่ตั้งเพื่อใช้การแสดงผลด้วยภาพนี้</span><span class="sxs-lookup"><span data-stu-id="63443-112">As with bubble maps, you must add some kind of value to the Location bucket to use this visual.</span></span> <span data-ttu-id="63443-113">เพิ่มเขตข้อมูลลงในบักเก็ตขนาดเพื่อเปลี่ยนความเข้มของสีเติมโดยสอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="63443-113">Add a field to the Size bucket to change the intensity of the fill color accordingly.</span></span>

![](media/3-5-create-map-visualizations/3-5_4.png)

<span data-ttu-id="63443-114">ไอคอนคำเตือนในมุมบนซ้ายของการแสดงผลด้วยภาพของคุณระบุว่า แผนที่จำเป็นต้องมีข้อมูลตำแหน่งที่ตั้งเพิ่มเติมเพื่อให้ลงค่าได้อย่างแม่นยำ</span><span class="sxs-lookup"><span data-stu-id="63443-114">A warning icon in the top left corner of your visual indicates that the map needs more location data to accurately plot values.</span></span> <span data-ttu-id="63443-115">ซึ่งเป็นปัญหาที่พบบ่อยเมื่อข้อมูลในเขตข้อมูลตำแหน่งที่ตั้งของคุณไม่ชัดเจน เช่น ใช้ชื่อพื้นที่อย่าง *วอชิงตัน* ที่อาจหมายถึงรัฐหรือเขต</span><span class="sxs-lookup"><span data-stu-id="63443-115">This is a particularly common problem when the data in your location field is ambiguous, such as using an area name like *Washington* that could indicate a state or a district.</span></span> <span data-ttu-id="63443-116">วิธีหนึ่งในการแก้ไขปัญหานี้คือการเปลี่ยนชื่อคอลัมน์ของคุณให้เจาะจงมากขึ้นเช่น *รัฐ*</span><span class="sxs-lookup"><span data-stu-id="63443-116">One way to resolve this problem is to rename your column to be more specific, such as *State*.</span></span> <span data-ttu-id="63443-117">อีกวิธีหนึ่งในการแก้ปัญหาคือการรีเซ็ตประเภทข้อมูลด้วยตนเองโดยการเลือก **ประเภทข้อมูล** ในแท็บการวางรูปแบบ จากนั้นคุณสามารถกำหนดประเภทให้กับข้อมูลของคุณเช่น "รัฐ" หรือ "เมือง"</span><span class="sxs-lookup"><span data-stu-id="63443-117">Another way to resolve it is to manually reset the data category by selecting **Data Category** in the Modeling tab. From there you can assign a category to your data such as "State" or "City".</span></span>

![](media/3-5-create-map-visualizations/3-5_5.png)

