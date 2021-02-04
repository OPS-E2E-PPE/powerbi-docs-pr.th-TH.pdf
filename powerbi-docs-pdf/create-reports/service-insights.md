---
title: สร้างข้อมูลเชิงลึกเกี่ยวกับชุดข้อมูลของคุณโดยอัตโนมัติ
description: เรียนรู้วิธีการรับข้อมูลเชิงลึกเกี่ยวกับไทล์ของชุดข้อมูลและแดชบอร์ดของคุณ
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
featuredvideoid: et_MLSL2sA8
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 09/28/2020
LocalizationGroup: Dashboards
ms.openlocfilehash: 8db804ec3afe4b752ab6f5f8546782cac7135055
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96388482"
---
# <a name="generate-data-insights-on-your-dataset-automatically-with-power-bi"></a><span data-ttu-id="95833-103">สร้างข้อมูลเชิงลึกโดยอัตโนมัติด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="95833-103">Generate data insights on your dataset automatically with Power BI</span></span>
<span data-ttu-id="95833-104">คุณมีชุดข้อมูลใหม่ และไม่แน่ใจว่าจะเริ่มใช้งานจากจุดไหนใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="95833-104">Do you have a new dataset and aren't sure where to start?</span></span>  <span data-ttu-id="95833-105">จำเป็นต้องสร้างแดชบอร์ดอย่างรวดเร็วใช่ไหม</span><span class="sxs-lookup"><span data-stu-id="95833-105">Need to build a dashboard quickly?</span></span>  <span data-ttu-id="95833-106">ต้องการค้นหาข้อมูลเชิงลึกที่คุณอาจพลาดไปใช่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="95833-106">Want to look for insights you may have missed?</span></span>

<span data-ttu-id="95833-107">เรียกใช้ข้อมูลเชิงลึกด่วนเพื่อสร้างการแสดงภาพที่น่าสนใจโดยยึดตามข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="95833-107">Run quick insights to generate interesting visualizations based on your data.</span></span> <span data-ttu-id="95833-108">บทความนี้อธิบายวิธีการเรียกใช้ข้อมูลเชิงลึกด่วนบนชุดข้อมูลทั้งหมด (ข้อมูลเชิงลึกด่วน)</span><span class="sxs-lookup"><span data-stu-id="95833-108">This article explains how to run quick insights on an entire dataset (quick insights).</span></span> <span data-ttu-id="95833-109">คุณยังสามารถเรียกใช้ข้อมูลเชิงลึกด่วน [บนไทล์แดชบอร์ดที่เฉพาะเจาะจง](../consumer/end-user-insights.md) (คลุมข้อมูลเชิงลึก)</span><span class="sxs-lookup"><span data-stu-id="95833-109">You can also run [quick insights on a specific dashboard tile](../consumer/end-user-insights.md) (scoped insights).</span></span> <span data-ttu-id="95833-110">แม้ว่าคุณสามารถเรียกใช้ข้อมูลเชิงลึกบนข้อมูลเชิงลึก</span><span class="sxs-lookup"><span data-stu-id="95833-110">You can even run insights on an insight!</span></span>

> [!NOTE]
> <span data-ttu-id="95833-111">ข้อมูลเชิงลึกไม่สามารถใช้งานได้กับ DirectQuery ข้อมูลเชิงลึกสามารถใช้งานได้กับข้อมูลที่อัปโหลดไปยัง Power BI เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="95833-111">Insights doesn't work with DirectQuery; it only works with data uploaded to Power BI.</span></span>
> 

<span data-ttu-id="95833-112">เราได้สร้างคุณลักษณะเชิงลึกในชุด [ที่เพิ่มขึ้นของอัลกอริทึมเชิงวิเคราะห์ขั้นสูง](../consumer/end-user-insight-types.md) ที่เราพัฒนาขึ้นด้วยการวิจัยของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="95833-112">We built the insights feature on a growing [set of advanced analytical algorithms](../consumer/end-user-insight-types.md) that we developed with Microsoft Research.</span></span> <span data-ttu-id="95833-113">เรายังคงใช้อัลกอริทึมเหล่านี้เพื่อช่วยให้บุคคลมากขึ้นในการค้นหาข้อมูลเชิงลึกในรูปแบบใหม่และใช้งานง่าย</span><span class="sxs-lookup"><span data-stu-id="95833-113">We continue to use these algorithms to help more people to find insights in their data in new and intuitive ways.</span></span> <span data-ttu-id="95833-114">คุณอาจสนใจในการเรียนรู้วิธีการ [ปรับข้อมูลของคุณให้เหมาะสมสำหรับ](service-insights-optimize.md)ข้อมูลเชิงลึกด่วน</span><span class="sxs-lookup"><span data-stu-id="95833-114">You might also be interested in learning how to [optimize your data for quick insights](service-insights-optimize.md).</span></span>

## <a name="run-quick-insights-on-a-dataset"></a><span data-ttu-id="95833-115">เรียกใช้ข้อมูลเชิงลึกด่วนบนชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="95833-115">Run quick insights on a dataset</span></span>
<span data-ttu-id="95833-116">ดูอแมนด้าเรียกใช้ข้อมูลเชิงลึกด่วนบนชุดข้อมูลและเปิดความเข้าใจในโหมดโฟกัส</span><span class="sxs-lookup"><span data-stu-id="95833-116">Watch Amanda run quick insights on a dataset and open an insight in Focus mode.</span></span> <span data-ttu-id="95833-117">อแมนด้าปักหมุดข้อมูลเชิงลึกเป็นไทล์บนแดชบอร์ดจากนั้นจะได้รับความเข้าใจสำหรับไทล์แดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="95833-117">Amanda pins an insight as a tile on the dashboard, then gets insights for a dashboard tile.</span></span>

<iframe width="560" height="315" src="https://www.youtube.com/embed/et_MLSL2sA8" frameborder="0" allowfullscreen></iframe>


<span data-ttu-id="95833-118">ในตอนนี้จะเปิดใช้งานของคุณ</span><span class="sxs-lookup"><span data-stu-id="95833-118">Now it's your turn.</span></span> <span data-ttu-id="95833-119">สำรวจข้อมูลเชิงลึกโดยใช้ [ตัวอย่างการวิเคราะห์คุณภาพผู้จัดหา](sample-supplier-quality.md)</span><span class="sxs-lookup"><span data-stu-id="95833-119">Explore insights by using the [Supplier Quality Analysis sample](sample-supplier-quality.md).</span></span>

1. <span data-ttu-id="95833-120">จากแท็บ **ชุดข้อมูล** เลือก **ตัวเลือกเพิ่มเติม** (...) แล้วเลือก **รับข้อมูลเชิงลึกด่วน**</span><span class="sxs-lookup"><span data-stu-id="95833-120">From the **Datasets** tab, select **More options** (...), and then choose **Get quick insights**.</span></span>
   
    ![แท็บชุดข้อมูล](media/service-insights/power-bi-ellipses.png)
   
    ![เมนูจุดไข่ปลา](media/service-insights/power-bi-tab.png)
2. <span data-ttu-id="95833-123">Power BI ใช้[อัลกอริธึมต่าง ๆ](../consumer/end-user-insight-types.md)เพื่อค้นหาแนวโน้มในชุดข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="95833-123">Power BI uses [various algorithms](../consumer/end-user-insight-types.md) to search for trends in your dataset.</span></span>
   
    ![กำลังค้นหาสำหรับข้อมูลเชิงลึก](media/service-insights/pbi_autoinsightssearching.png)
3. <span data-ttu-id="95833-125">ภายในไม่กี่วินาที ข้อมูลเชิงลึกของคุณพร้อม</span><span class="sxs-lookup"><span data-stu-id="95833-125">Within seconds, your insights are ready.</span></span>  <span data-ttu-id="95833-126">เลือก **ดูข้อมูลเชิงลึก** เพื่อแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="95833-126">Select **View insights** to display visualizations.</span></span>
   
    ![ข้อความแสดงความสำเร็จ](media/service-insights/pbi_autoinsightsuccess.png)
   
    > [!NOTE]
    > <span data-ttu-id="95833-128">ชุดข้อมูลบางชุดไม่สามารถสร้างข้อมูลเชิงลึกได้เนื่องจากข้อมูลไม่มีนัยสำคัญทางสถิติ</span><span class="sxs-lookup"><span data-stu-id="95833-128">Some datasets can't generate insights because the data isn't statistically significant.</span></span>  <span data-ttu-id="95833-129">เมื่อต้องการเรียนรู้เพิ่มเติม ดู[ข้อมูลของคุณสำหรับข้อมูลเชิงลึกที่ปรับให้เหมาะสม](service-insights-optimize.md)</span><span class="sxs-lookup"><span data-stu-id="95833-129">To learn more, see [Optimize your data for insights](service-insights-optimize.md).</span></span>
    > 
    
4. <span data-ttu-id="95833-130">แสดงภาพที่แสดงในพิเศษ **ข้อมูลเชิงลึกด่วน** ผืนผ้าใบกับบัตรข้อมูลเชิงลึกที่แยกต่างหาก 32</span><span class="sxs-lookup"><span data-stu-id="95833-130">The visualizations display in a special **Quick Insights** canvas with up to 32 separate insight cards.</span></span> <span data-ttu-id="95833-131">บัตรแต่ละใบมีแผนภูมิ หรือกราฟ และคำอธิบายสั้น ๆ</span><span class="sxs-lookup"><span data-stu-id="95833-131">Each card has a chart or graph plus a short description.</span></span>
   
    ![คานวาสข้อมูลเชิงลึกด่วน](media/service-insights/power-bi-insights.png)

## <a name="interact-with-the-insight-cards"></a><span data-ttu-id="95833-133">โต้ตอบกับบัตรข้อมูลเชิงลึก</span><span class="sxs-lookup"><span data-stu-id="95833-133">Interact with the insight cards</span></span>

1. <span data-ttu-id="95833-134">อีกทางหนึ่งคือ เลื่อนไปเหนือภาพแล้วเลือกไอคอนหมุดเพื่อเพิ่มการแสดงภาพไปยังแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="95833-134">Hover over a card and select the pin icon to add the visualization to a dashboard.</span></span>

2. <span data-ttu-id="95833-135">วางเมาส์เหนือการ์ด เลือก **ตัวเลือกเพิ่มเติม** (...) แล้วเลือก **ดูข้อมูลเชิงลึก**</span><span class="sxs-lookup"><span data-stu-id="95833-135">Hover over a card, select **More options** (...), and then choose **View insights**.</span></span> 

    <span data-ttu-id="95833-136">หน้าจอข้อมูลเชิงลึกจะเปิดขึ้นในโหมดโฟกัส</span><span class="sxs-lookup"><span data-stu-id="95833-136">The insight screen opens in Focus mode.</span></span>
   
    ![โหมดโฟกัสของข้อมูลเชิงลึก](media/service-insights/power-bi-insight-focus.png)
3. <span data-ttu-id="95833-138">ในโหมดโฟกัสคุณสามารถ:</span><span class="sxs-lookup"><span data-stu-id="95833-138">In Focus mode you can:</span></span>
   
   * <span data-ttu-id="95833-139">กรองการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="95833-139">Filter the visualizations.</span></span> <span data-ttu-id="95833-140">ถ้าบานหน้าต่างตั **วกรอง** ไม่ได้เปิดอยู่ให้ขยายโดยการเลือกลูกศรทางด้านขวาของหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="95833-140">If the **Filters** pane isn't already open, expand it by selecting the arrow on the right side of the window.</span></span>

       ![ขยายเมนูตัวกรองของข้อมูลเชิงลึกแล้ว](media/service-insights/power-bi-insights-filter-new.png)
   * <span data-ttu-id="95833-142">ปักหมุดการ์ดข้อมูลเชิงลึกในแดชบอร์ดโดยการเลือก **ปักหมุดวิชวล**</span><span class="sxs-lookup"><span data-stu-id="95833-142">Pin the insight card to a dashboard by selecting **Pin visual**.</span></span>
   * <span data-ttu-id="95833-143">เรียกใช้ข้อมูลเชิงลึกบนการ์ดเองซึ่งมักจะเรียกว่า *ข้อมูลเชิงลึกคลุม*</span><span class="sxs-lookup"><span data-stu-id="95833-143">Run insights on the card itself, which is often referred to as *scoped insights*.</span></span> <span data-ttu-id="95833-144">ที่มุมบนขวา เลือกไอคอนหลอดไฟ![ไอคอนรับข้อมูลเชิงลึก](media/service-insights/power-bi-bulb-icon.png) หรือ **รับข้อมูลเชิงลึก**</span><span class="sxs-lookup"><span data-stu-id="95833-144">In the top-right corner, select the lightbulb icon ![Get insights icon](media/service-insights/power-bi-bulb-icon.png) or **Get Insights**.</span></span>
     
       ![ไอคอนรับข้อมูลเชิงลึก](media/service-insights/pbi-autoinsights-tile.png)
     
     <span data-ttu-id="95833-146">ข้อมูลเชิงลึกจะแสดงทางด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="95833-146">The insight displays on the left.</span></span> <span data-ttu-id="95833-147">การ์ดใหม่โดยยึดตามข้อมูลในเชิงลึกเดียวเท่านั้นให้แสดงตามด้านขวา</span><span class="sxs-lookup"><span data-stu-id="95833-147">New cards, based solely on the data in that single insight, display along the right.</span></span>
     
       ![ข้อมูลเชิงลึกเกี่ยวกับข้อมูลเชิงลึก](media/service-insights/power-bi-insights-on-insights-new.png)
4. <span data-ttu-id="95833-149">เมื่อต้องการกลับไปยังต้นฉบับข้อมูลเชิงลึกพื้นที่ ที่มุมบนซ้าย เลือก **โหมดโฟกัสออกจาก**</span><span class="sxs-lookup"><span data-stu-id="95833-149">To return to the original insights canvas, in the top-left corner, select **Exit Focus mode**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="95833-150">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="95833-150">Next steps</span></span>
- <span data-ttu-id="95833-151">ถ้าคุณเป็นเจ้าของชุดข้อมูล[ปรับให้เหมาะสมสำหรับข้อมูลเชิงลึกด่วน](service-insights-optimize.md)</span><span class="sxs-lookup"><span data-stu-id="95833-151">If you own a dataset, [optimize it for Quick Insights](service-insights-optimize.md).</span></span>
- <span data-ttu-id="95833-152">เรียนรู้เกี่ยวกับ[ชนิดของข้อมูลเชิงลึกด่วนที่พร้อมใช้งาน](../consumer/end-user-insight-types.md)</span><span class="sxs-lookup"><span data-stu-id="95833-152">Learn about the [types of Quick Insights available](../consumer/end-user-insight-types.md).</span></span>

<span data-ttu-id="95833-153">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="95833-153">More questions?</span></span> <span data-ttu-id="95833-154">[ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)</span><span class="sxs-lookup"><span data-stu-id="95833-154">[Try the Power BI Community](https://community.powerbi.com/).</span></span>
