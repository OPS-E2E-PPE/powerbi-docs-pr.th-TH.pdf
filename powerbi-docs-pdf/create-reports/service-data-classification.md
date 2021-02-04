---
title: การจัดประเภทข้อมูลของแดชบอร์ด
description: เรียนรู้เกี่ยวกับการจัดประเภทข้อมูลแดชบอร์ด รวมถึงสิ่งที่ีผู้ดูแลระบบควรตั้งค่า และวิธีที่เจ้าของแดชบอร์ดสามารถเปลี่ยนการจัดประเภท
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-reports-dashboards
ms.topic: how-to
ms.date: 08/10/2017
LocalizationGroup: Dashboards
ms.openlocfilehash: e576cb5c0092d61d8c4b30fd180f66cef2922b0e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96388804"
---
# <a name="dashboard-data-classification"></a><span data-ttu-id="094c9-103">การจัดประเภทข้อมูลของแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="094c9-103">Dashboard data classification</span></span>
<span data-ttu-id="094c9-104">แดชบอร์ดทุกตัวจะแตกต่างกันไป และขึ้นอยู่กับแหล่งข้อมูลที่เชื่อมต่อ คุณอาจจะเห็นว่าคุณและเพื่อนร่วมงานของคุณแชร์ความต้องการมาตรการที่แตกต่างกัน โดยขึ้นอยู่กับระดับความลับของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="094c9-104">Every dashboard is different, and depending on the data source you are connecting to, you will likely find that you and the colleagues you share with will need to take different precautions depending on the sensitivity of the data.</span></span> <span data-ttu-id="094c9-105">แดชบอร์ดบางตัวไม่ควรจะหรือพิมพ์หรือใช้ร่วมกันกับที่อยู่ภายนอกบริษัทของคุณ ในขณะที่ตัวอื่นๆสามารถแชร์ได้อย่างอิสระ</span><span class="sxs-lookup"><span data-stu-id="094c9-105">Some dashboards should never be shared with those outside your company or printed out, while others can be shared freely.</span></span> <span data-ttu-id="094c9-106">โดยใช้การจัดประเภทข้อมูลแดชบอร์ด คุณจะสามารถสร้างความตระหนักให้กับบุคคลที่กำลังดูแดชบอร์ดของคุณ เกี่ยวกับระดับการรักษาความปลอดภัยใดควรใช้</span><span class="sxs-lookup"><span data-stu-id="094c9-106">By using dashboard data classification, you will be able to raise awareness with those viewing your dashboards about what level of security should be used.</span></span> <span data-ttu-id="094c9-107">คุณสามารถแท็กแดชบอร์ดของคุณ ด้วยการจัดประเภทที่กำหนดโดยแผนก IT ของบริษัทของคุณ ดังนั้นทุกคนที่ดูเนื้อหาจะมีการทำความเข้าใจเกี่ยวกับระดับความลับของข้อมูลในระดับเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="094c9-107">You can tag your dashboards with classifications defined by your company’s IT department, so everyone viewing the content will have the same level of understanding around the sensitivity of the data.</span></span>

![ภาพหน้าจอของแดชบอร์ด ที่แสดงการจัดประเภทข้อมูลจากตัวอย่าง](media/service-data-classification/dashboard_tagged_as_hbi.png)

## <a name="data-classification-tags"></a><span data-ttu-id="094c9-109">แท็กการจัดประเภทข้อมูล</span><span class="sxs-lookup"><span data-stu-id="094c9-109">Data classification tags</span></span>
<span data-ttu-id="094c9-110">แท็กการจัดประเภทข้อมูลแสดงอยู่ถัดจากชื่อแดชบอร์ด เพื่อแจ้งให้ทุกคนที่ดูอยู่ทราบระดับความปลอดภัยที่ควรใช้กับแดชบอร์ดและข้อมูลที่มี</span><span class="sxs-lookup"><span data-stu-id="094c9-110">Data classification tags show up next to the dashboard name, letting anyone viewing it know the level of security that should be applied to the dashboard and the data it contains.</span></span>

![ภาพหน้าจอของแดชบอร์ด ที่แสดงแท็กการจัดประเภทข้อมูลที่อยู่ถัดจากชื่อแดชบอร์ด](media/service-data-classification/tag_next_to_title.png)

<span data-ttu-id="094c9-112">ซึ่งจะแสดงถัดจากแดชบอร์ดไทล์ในรายการโปรดของคุณด้วย</span><span class="sxs-lookup"><span data-stu-id="094c9-112">It will also show up next to the dashboard tile in your Favorites list.</span></span>

![ภาพหน้าจอของรายการโปรด ที่แสดงแท็กการจัดประเภทข้อมูลที่อยู่ถัดจากไทล์แดชบอร์ดในรายการโปรดของคุณ](media/service-data-classification/tag_on_dashboard_tile.png)

<span data-ttu-id="094c9-114">เมื่อคุณวางเคอร์เซอร์เหนือแท็ก คุณจะเห็นชื่อเต็มของการจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="094c9-114">When you hover over the tag, you will see the full name of the classification.</span></span>

![<span data-ttu-id="094c9-115">ภาพหน้าจอของแท็ก HBI ที่แสดงชื่อเต็มของการจัดประเภทเมื่อคุณวางเมาส์เหนือแท็ก</span><span class="sxs-lookup"><span data-stu-id="094c9-115">Screenshot of the H B I tag, showing the full name of the classification when you hover over the tag.</span></span> ](media/service-data-classification/tag_tooltip.png)

<span data-ttu-id="094c9-116">ผู้ดูแลระบบยังสามารถตั้งค่าเป็น URL สำหรับแท็กที่ให้ข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="094c9-116">Admins can also set an URL for a tag to provide additional information.</span></span>

> [!NOTE]
> <span data-ttu-id="094c9-117">โดยขึ้นอยู่กับการตั้งค่าการจัดประเภท ที่ตั้งโดยผู้ดูแลระบบของคุณ การจัดประเภทบางชนิดอาจไม่แสดงเป็นแท็กบนแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="094c9-117">Depending the classification settings set by your admin, some classification types may not show as a tag on the dashboard.</span></span> <span data-ttu-id="094c9-118">ถ้าคุณเป็นเจ้าของแดชบอร์ด คุณสามารถตรวจสอบชนิดการจัดประเภทแดชบอร์ดของคุณภายใต้การตั้งค่าแดชบอร์ดได้เสมอ</span><span class="sxs-lookup"><span data-stu-id="094c9-118">If you are a dashboard owner, you can always check your dashboard classification type under the dashboard settings.</span></span>
> 
> 

## <a name="setting-a-dashboards-classification"></a><span data-ttu-id="094c9-119">ตั้งค่าการจัดประเภทของแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="094c9-119">Setting a dashboard’s classification</span></span>
<span data-ttu-id="094c9-120">ถ้าการจัดประเภทข้อมูลถูกเปิดใช้งานสำหรับบริษัทของคุณ แดชบอร์ดทั้งหมดจะเริ่มด้วยการจัดประเภทชนิดเริ่มต้น แต่ในฐานะเจ้าของแดชบอร์ด คุณสามารถเปลี่ยนการจัดประเภทเพื่อให้ตรงกับระดับความปลอดภัยของแดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="094c9-120">If data classification is turned on for your company, all dashboards start out with a default classification type, but as a dashboard owner, you can change the classification to match your dashboards security level.</span></span>

<span data-ttu-id="094c9-121">เมื่อต้องเปลี่ยนชนิดการจัดประเภท ให้ทำสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="094c9-121">To change the classification type, do the following:</span></span>

1. <span data-ttu-id="094c9-122">ไปที่การตั้งค่าแดชบอร์ดโดยการเลือก **จุดไข่ปลา** ถัดจากชื่อแดชบอร์ดและเลือก **ตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="094c9-122">Go to the dashboard settings by selecting the **ellipsis** next to the dashboard name and select **Settings**.</span></span>
   
    ![ภาพหน้าจอของแดชบอร์ด ที่แสดงการเลือกการตั้งค่า](media/service-data-classification/dashboard_settings.png)
2. <span data-ttu-id="094c9-124">ภายใต้การตั้งค่าแดชบอร์ด คุณจะสามารถดูการจัดประเภทปัจจุบันของแดชบอร์ดของคุณ และใชดร๊อปดาวน์เพื่อเปลี่ยนชนิดการจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="094c9-124">Under Dashboard settings, you will be able to see the current classification for your dashboard and use the drop down to change the classification type.</span></span>
   
    ![ภาพหน้าจอของการตั้งค่าแดชบอร์ด ที่แสดงการจัดประเภทปัจจุบันและการเลือกรายการแบบดรอปดาวน์สำหรับการจัดประเภทข้อมูล](media/service-data-classification/classification_setting_dropdown.png)
3. <span data-ttu-id="094c9-126">ให้เลือก **นำไปใช้** เมื่อทำเสร็จแล้ว</span><span class="sxs-lookup"><span data-stu-id="094c9-126">Select **Apply** when finished.</span></span>

<span data-ttu-id="094c9-127">หลังจากทีใช้การเปลี่ยนแปลง ทุกคนที่คุณแชร์ จะเห็นการปรับปรุงในครั้งถัดไปที่พวกเขารีโหลดแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="094c9-127">After you apply the change, anyone you shared with will see the update the next time they reload the dashboard.</span></span>

## <a name="working-with-data-classification-tags-as-an-admin"></a><span data-ttu-id="094c9-128">ทำงานกับแท็กการจัดประเภทข้อมูลในฐานะผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="094c9-128">Working with data classification tags as an admin</span></span>
<span data-ttu-id="094c9-129">จัดประเภทข้อมูลถูกตั้งค่าโดยผู้ดูแลระบบส่วนกลางสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="094c9-129">Data classification is set up by the global admin for your organization.</span></span> <span data-ttu-id="094c9-130">เพื่อเปิดการจัดประเภทข้อมูล ให้ทำสิ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="094c9-130">To turn data classification on, do the following:</span></span>

1. <span data-ttu-id="094c9-131">ให้เลือกเฟืองการตั้งค่า และเลือก **ผู้ดพอร์ทัล**</span><span class="sxs-lookup"><span data-stu-id="094c9-131">Select the Settings gear and select **Admin Portal**.</span></span>
   
    ![ภาพหน้าจอของเฟืองการตั้งค่า ที่แสดงการเลือกพอร์ทัลผู้ดูแลระบบ](media/service-data-classification/admin_portal_in_settings.png)
2. <span data-ttu-id="094c9-133">เปลี่ยน **การจัดประเภทข้อมูลของแดชบอร์ดและรายงาน** เป็น *เปิด* ภายในแท็บ **การตั้งค่าผู้เช่า**</span><span class="sxs-lookup"><span data-stu-id="094c9-133">Switch **Data classification for dashboards and reports** to *on* within the **Tenant settings** tab.</span></span>
   
    ![ภาพหน้าจอของพอร์ทัลผู้ดูแล ที่แสดงการตั้งค่าผู้เช่าและการเลือกการจัดประเภทข้อมูลสำหรับแดชบอร์ดและรายงาน](media/service-data-classification/data_classification_switch_location.png)

<span data-ttu-id="094c9-135">เมื่อเปิดใช้งาน คุณจะเห็นแบบฟอร์มเพื่อสร้างการแบ่งประเภทต่างๆ ในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="094c9-135">Once turned on, you will be presented with a form to create the various classifications in your organization.</span></span>

![ภาพหน้าจอของฟอร์ม ที่แสดงรายการเขตข้อมูลสำหรับการจัดประเภทต่างๆ ในองค์กรของคุณ](media/service-data-classification/blank_classification_form.png)

<span data-ttu-id="094c9-137">แต่ละประเภทมี **ชื่อ** และ **ตัวย่อ** ซึ่งจะปรากฏในแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="094c9-137">Each classification has a **name** and a **shorthand** which will appear on the dashboard.</span></span> <span data-ttu-id="094c9-138">สำหรับการจัดประเภทแต่ละตัว คุณสามารถตัดสินใจว่าจะให้แท็กอ้างอิงแบบย่อปรากฏในแดชบอร์ดหรือไม่ โดยการเลือก **แสดงแท็ก**</span><span class="sxs-lookup"><span data-stu-id="094c9-138">For each classification, you can decide if the shorthand tag will appear on the dashboard or not by selecting **Show tag**.</span></span> <span data-ttu-id="094c9-139">ถ้าคุณตัดสินใจไม่แสดงชนิดการจัดประเภทบนแดชบอร์ด เจ้าของจะยังคงสามารถดูชนิดได้โดยการตรวจสอบการตั้งค่าแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="094c9-139">If you decide not to show the classification type on the dashboard, the owner will still be able to see the type by checking the dashboard settings.</span></span> <span data-ttu-id="094c9-140">นอกจากนี้ คุณสามารถเลือกที่จะเพิ่มเป็น **URL** ที่มีข้อมูลเพิ่มเติมเกี่ยวกับแนวทางการจัดประเภทและความต้องการใช้งานขององค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="094c9-140">Additionally, you can optionally add a **URL** that contains more information about your organization’s classification guidelines and usage requirements.</span></span>  

<span data-ttu-id="094c9-141">สิ่งสุดท้ายที่คุณจำเป็นต้องตัดสินใจคือชนิดการจัดประเภทที่จะเป็นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="094c9-141">The last thing you need to decide is which classification type will be the default.</span></span>  

<span data-ttu-id="094c9-142">เมื่อคุณกรอกแบบฟอร์มพร้อมกับชนิดของการจัดประเภท ให้เลือก **นำไปใช้** เพื่อบันทึกการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="094c9-142">Once you fill in the form with your classification types, select **Apply** to save the changes.</span></span>

![ภาพหน้าจอของฟอร์ม ที่แสดงรายการที่เติมด้วยชนิดการจัดประเภทที่จะนำไปใช้](media/service-data-classification/filled_in_classification_form.png)

<span data-ttu-id="094c9-144">ในตอนนี้ แดชบอร์ดทั้งหมดจะได้รับการกำหนดค่าการจัดประเภทเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="094c9-144">At this point, all dashboards will be assigned the default classification.</span></span> <span data-ttu-id="094c9-145">เจ้าของแดชบอร์ดสามารถอัปเดตชนิดการจัดประเภทให้เหมาะสมกับเนื้อหาของตนได้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="094c9-145">Dashboard owners can now update the classification type to the one appropriate for their content.</span></span> <span data-ttu-id="094c9-146">คุณสามารถกลับมาที่นี่ในอนาคตเมื่อต้องเพิ่มหรือลบชนิดการจัดประเภท หรือเปลี่ยนค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="094c9-146">You can return here in the future to add or remove classification types or change the default.</span></span>  

> [!NOTE]
> <span data-ttu-id="094c9-147">มีบางสิ่งที่สำคัญที่ต้องทราบเมื่อคุณกลับมาทำการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="094c9-147">There are a few important things to remember when you come back to make changes:</span></span>
> 
> * <span data-ttu-id="094c9-148">ถ้าคุณปิดใช้งานการจัดประเภทข้อมูล จะไม่จดจำแท็ก</span><span class="sxs-lookup"><span data-stu-id="094c9-148">If you turn data classification off, none of the tags are remembered.</span></span> <span data-ttu-id="094c9-149">คุณจะต้องเริ่มต้นใหม่ทั้งหมด ถ้าคุณตัดสินใจกลับไปเป็นเหมือนเก่าภายหลัง</span><span class="sxs-lookup"><span data-stu-id="094c9-149">You will need to start over if you decide to turn it back on later.</span></span>  
> * <span data-ttu-id="094c9-150">ถ้าคุณลบชนิดการจัดประเภท แดชบอร์ดใดๆที่ถูกกำหนด ชนิดการจัดประเภทที่ถูกลบออก จะถูกกำหนดให้กลับไปเป็นค่าเริ่มต้นจนกว่าเจ้าของจะตั้งค่าอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="094c9-150">If you remove a classification type, any dashboards assigned the removed classification type will be assigned back to the default until the owner goes and sets it again.</span></span>  
> * <span data-ttu-id="094c9-151">ถ้าคุณเปลี่ยนค่าเริ่มต้น แดชบอร์ดทั้งหมดที่ไม่ได้กำหนดชนิดการจัดประเภทโดยเจ้าของ จะเปลี่ยนเป็นค่าเริ่มต้นตัวใหม่</span><span class="sxs-lookup"><span data-stu-id="094c9-151">If you change the default, all dashboards that weren’t already assigned a classification type by the owner will change to the new default.</span></span>
> 
> 

