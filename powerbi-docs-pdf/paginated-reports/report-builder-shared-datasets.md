---
title: สร้างรายงานแบบแบ่งหน้าด้วยชุดข้อมูลที่ใช้ร่วมกันของ Power BI - ตัวสร้างรายงาน Power BI
description: สร้างรายงานแบบแบ่งหน้าในตัวสร้างรายงาน Power BI โดยอ้างอิงจากชุดข้อมูลที่ใช้ร่วมกันของ Power BI
author: maggiesMSFT
ms.author: maggies
ms.date: 11/18/2020
ms.service: powerbi
ms.subservice: report-builder
ms.topic: how-to
ms.openlocfilehash: 7e74a64aad33f310109b754bba09fd61043747ff
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96415783"
---
# <a name="create-a-paginated-report-based-on-a-power-bi-shared-dataset"></a><span data-ttu-id="ed125-103">สร้างรายงานแบบแบ่งหน้าโดยอ้างอิงจากชุดข้อมูลที่ใช้ร่วมกันของ Power BI</span><span class="sxs-lookup"><span data-stu-id="ed125-103">Create a paginated report based on a Power BI shared dataset</span></span>

<span data-ttu-id="ed125-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [yes-desktop](../includes/yes-desktop.md)]</span><span class="sxs-lookup"><span data-stu-id="ed125-104">[!INCLUDE [applies-to](../includes/applies-to.md)] [!INCLUDE [yes-service](../includes/yes-service.md)] [!INCLUDE [yes-paginated](../includes/yes-paginated.md)] [!INCLUDE [yes-premium](../includes/yes-premium.md)] [!INCLUDE [yes-desktop](../includes/yes-desktop.md)]</span></span> 

<span data-ttu-id="ed125-105">คุณสามารถใช้ชุดข้อมูลที่คุณสร้างใน Power BI Desktop เป็นแหล่งข้อมูลสำหรับรายงานแบบแบ่งหน้าจากตัวสร้างรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="ed125-105">You can use a dataset that you create in Power BI Desktop as a data source for Power BI Report Builder paginated reports.</span></span> <span data-ttu-id="ed125-106">นึกภาพสถานการณ์สมมตินี้: คุณได้สร้างรายงาน Power BI ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ed125-106">Picture this scenario: You've created a Power BI report in Power BI Desktop.</span></span> <span data-ttu-id="ed125-107">คุณใช้เวลามากมายในการออกแบบแบบจำลองข้อมูล จากนั้นสร้างรายงาน Power BI ที่สวยงามพร้อมวิชวลที่ยอดเยี่ยมทุกประเภท</span><span class="sxs-lookup"><span data-stu-id="ed125-107">You spent a lot of time designing the data model, then created a beautiful Power BI report with all sorts of great visuals.</span></span> <span data-ttu-id="ed125-108">รายงานของคุณมีเมทริกซ์ที่มีหลายแถว ดังนั้นคุณต้องเลื่อนเพื่อดูทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="ed125-108">Your report has a matrix with many rows, so you have to scroll to see them all.</span></span> <span data-ttu-id="ed125-109">ผู้อ่านรายงานของคุณต้องการรายงานที่พวกเขาสามารถพิมพ์ออกมาได้ ซึ่งจะแสดงแถวทั้งหมดในเมทริกซ์นั้น</span><span class="sxs-lookup"><span data-stu-id="ed125-109">Your report readers want a report they can print out, that will show all the rows in that matrix.</span></span> <span data-ttu-id="ed125-110">รายงานแบบแบ่งหน้าของ Power BI จะสามารถทำได้: พิมพ์ตารางหรือเมทริกซ์ที่รันไปหลายหน้า ด้วยส่วนหัวและส่วนท้ายของหน้าและเค้าโครงหน้าที่สมบูรณ์แบบที่คุณออกแบบ</span><span class="sxs-lookup"><span data-stu-id="ed125-110">A Power BI paginated report can do that: print a table or matrix that runs to multiple pages, with page headers and footers and a perfect page layout that you design.</span></span> <span data-ttu-id="ed125-111">ซึ่งจะเติมเต็มรายงาน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ed125-111">It will complement the Power BI Desktop report.</span></span> <span data-ttu-id="ed125-112">คุณต้องการให้รายงานยึดตามข้อมูลเดียวกันอย่างแม่นยำ ไม่มีความขัดแย้ง ดังนั้นคุณต้องใช้ชุดข้อมูลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="ed125-112">You want them to be based on the exact same data, no discrepancies, so you use the same dataset.</span></span>

![Power BI Desktop ไปเป็นรายงานแบบแบ่งหน้าจากตัวสร้างรายงาน Power BI](media/report-builder-shared-datasets/power-bi-desktop-report-builder-arrow-26-pgs.png)

<span data-ttu-id="ed125-114">ชุดข้อมูลไม่จำเป็นต้องอยู่ในพื้นที่ทำงานในความจุแบบพรีเมียมและคุณไม่จำเป็นต้องเป็นสมาชิกของพื้นที่ทำงานนั้น</span><span class="sxs-lookup"><span data-stu-id="ed125-114">The dataset doesn't have to be in a workspace in a Premium capacity, and you don't need to be a member of that workspace.</span></span> <span data-ttu-id="ed125-115">คุณเพียงแค่ต้องมี[สิทธิ์ในการสร้าง](../connect-data/service-datasets-build-permissions.md)ชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ed125-115">You just need to have [Build permission](../connect-data/service-datasets-build-permissions.md) for the dataset.</span></span> <span data-ttu-id="ed125-116">ในการเผยแพร่รายงานแบบแบ่งหน้า คุณจำเป็นต้องมีสิทธิ์การใช้งาน Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="ed125-116">To publish your paginated report, you do need a Power BI Pro license.</span></span> <span data-ttu-id="ed125-117">นอกจากนี้คุณยังต้องมีบทบาทผู้สนับสนุนสำหรับพื้นที่ทำงานในความจุพรีเมียมด้วยเป็นอย่างน้อย</span><span class="sxs-lookup"><span data-stu-id="ed125-117">You also need at least a Contributor role for a workspace in a Premium capacity.</span></span>

## <a name="what-you-need"></a><span data-ttu-id="ed125-118">สิ่งที่คุณจำเป็นต้องมี</span><span class="sxs-lookup"><span data-stu-id="ed125-118">What you need</span></span>

<span data-ttu-id="ed125-119">ต่อไปนี้คือรายการของสิ่งที่คุณจำเป็นต้องและไม่จำเป็นต้องใช้ชุดข้อมูลที่ใช้ร่วมกันในตัวสร้างรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="ed125-119">Here's a list of what you need and don't need to use a shared dataset in Power BI Report Builder.</span></span>

- <span data-ttu-id="ed125-120">ตัวสร้างรายงานใน Power BI</span><span class="sxs-lookup"><span data-stu-id="ed125-120">Power BI Report Builder.</span></span> <span data-ttu-id="ed125-121">[ดาวน์โหลดและติดตั้งตัวสร้างรายงานใน Power BI](https://aka.ms/pbireportbuilder)</span><span class="sxs-lookup"><span data-stu-id="ed125-121">[Download and install Power BI Report Builder](https://aka.ms/pbireportbuilder).</span></span>
- <span data-ttu-id="ed125-122">หากต้องการเข้าถึงชุดข้อมูล Power BI คุณจะต้องมีสิทธิ์ในการสร้างชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ed125-122">To access a Power BI dataset, you need to have Build permission for the dataset.</span></span> <span data-ttu-id="ed125-123">อ่านเกี่ยวกับ[สิทธิ์ในการสร้าง](../connect-data/service-datasets-build-permissions.md)</span><span class="sxs-lookup"><span data-stu-id="ed125-123">Read about [Build permission](../connect-data/service-datasets-build-permissions.md).</span></span>
- <span data-ttu-id="ed125-124">คุณไม่จำเป็นต้องมีใบอนุญาต Power BI Pro เพื่อสร้างรายงานแบบแบ่งหน้าในตัวสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed125-124">You don't need a Power BI Pro license to create a paginated report in Report Builder.</span></span> 
- <span data-ttu-id="ed125-125">คุณจำเป็นต้องมีสิทธิ์การใช้งาน Power BI Pro เพื่อเผยแพร่รายงานแบบแบ่งหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="ed125-125">You do need a Power BI Pro license to publish your paginated report.</span></span> <span data-ttu-id="ed125-126">นอกจากนี้คุณยังต้องมีบทบาทผู้สนับสนุนสำหรับพื้นที่ทำงานในความจุพรีเมียมด้วยเป็นอย่างน้อย</span><span class="sxs-lookup"><span data-stu-id="ed125-126">You also need at least a Contributor role for a workspace in a Premium capacity.</span></span> 
- <span data-ttu-id="ed125-127">ทางเลือก: ถ้าคุณต้องการทำตามบทความนี้ให้ดาวน์โหลดไฟล์ .pbix [ตัวอย่างการวิเคราะห์ด้านการขายปลีก](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix)ของ Power BI Desktop จากนั้นเปิดไฟล์ใน Power BI Desktop และเพิ่มตารางที่มีคอลัมน์จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="ed125-127">Optional: If you want to follow along with this article, download the Power BI Desktop [Retail Analysis sample .pbix](https://download.microsoft.com/download/9/6/D/96DDC2FF-2568-491D-AAFA-AFDD6F763AE3/Retail%20Analysis%20Sample%20PBIX.pbix) file, open it in Power BI Desktop and add a table with a lot of columns.</span></span> <span data-ttu-id="ed125-128">ในบานหน้าต่าง **รูปแบบ** ให้ปิด **ผลรวม**</span><span class="sxs-lookup"><span data-stu-id="ed125-128">In the **Format** pane, turn off **Totals**.</span></span> <span data-ttu-id="ed125-129">จากนั้นเผยแพร่ไปยังพื้นที่ทำงานในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="ed125-129">Then publish it to a workspace in the Power BI service.</span></span>

    ![ผลรวมปิดอยู่](media/report-builder-shared-datasets/power-bi-desktop-totals-off.png)

## <a name="connect-to-the-power-bi-dataset"></a><span data-ttu-id="ed125-131">เชื่อมต่อกับชุดข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="ed125-131">Connect to the Power BI dataset</span></span>

1. <span data-ttu-id="ed125-132">เกิดตัวสร้างรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="ed125-132">Open Power BI Report Builder.</span></span>
1. <span data-ttu-id="ed125-133">เลือก **ลงชื่อเข้าใช้** ที่มุมบนขวาของตัวสร้างรายงานเพื่อลงชื่อเข้าใช้บัญชี Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ed125-133">Select **Sign in** in the upper-right corner of Report Builder to sign in to your Power BI account.</span></span>
1. <span data-ttu-id="ed125-134">ในบานหน้าต่างข้อมูลรายงาน ให้เลือก **ใหม่** >  **การเชื่อมต่อชุดข้อมูล Power BI**</span><span class="sxs-lookup"><span data-stu-id="ed125-134">In the Report Data pane, select **New** > **Power BI Dataset Connection**.</span></span>

    ![ชุดข้อมูลในบานหน้าต่างข้อมูลรายงาน](media/report-builder-shared-datasets/power-bi-report-builder-new-dataset.png)

    > [!NOTE]
    > <span data-ttu-id="ed125-136">คุณไม่สามารถสร้างแหล่งข้อมูลหรือชุดข้อมูลสำหรับชุดข้อมูล Power BI ได้โดยใช้ตัวช่วยสร้างตาราง เมทริกซ์ หรือแผนภูมิของตัวสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed125-136">You can't create the data source or dataset for a Power BI dataset by using the Report Builder Table, Matrix, or Chart wizards.</span></span> <span data-ttu-id="ed125-137">หลังจากที่คุณได้สร้างขึ้นแล้ว คุณสามารถใช้ตัวช่วยสร้างตาราง เมทริกซ์ หรือแผนภูมิที่ยึดตามรายงานเหล่านั้นได้</span><span class="sxs-lookup"><span data-stu-id="ed125-137">After you've created them, you can use the wizards to create tables, matrixes, or charts based on them.</span></span>

1. <span data-ttu-id="ed125-138">ค้นหาหรือเรียกดูชุดข้อมูลหรือพื้นที่ทำงานในที่ซึ่งมีชุดข้อมูลอยู่ > **เลือก**</span><span class="sxs-lookup"><span data-stu-id="ed125-138">Search or browse for the dataset or the workspace where it resides > **Select**.</span></span>
    <span data-ttu-id="ed125-139">เติมตัวสร้างรายงานในชื่อชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ed125-139">Report Builder fills in the dataset name.</span></span>

    ![เลือกชุดข้อมูล](media/report-builder-shared-datasets/power-bi-report-builder-select-dataset.png)
    
1. <span data-ttu-id="ed125-141">ชุดข้อมูลจะแสดงอยู่ภายใต้แหล่งข้อมูลในบานหน้าต่างข้อมูลรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed125-141">The dataset is listed under Data Sources in the Report Data pane.</span></span>

    ![ชุดข้อมูลภายใต้แหล่งข้อมูลในบานหน้าต่างข้อมูลรายงาน](media/report-builder-shared-datasets/power-bi-report-builder-data-source.png)

    <span data-ttu-id="ed125-143">โปรดจำไว้ว่าคุณสามารถเชื่อมต่อกับชุดข้อมูล Power BI หลายชุดและแหล่งข้อมูลอื่น ๆ ในรายงานแบบแบ่งหน้าเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="ed125-143">Remember, you can connect to multiple Power BI datasets and other data sources in the same paginated report.</span></span>


## <a name="get-the-dax-query-for-the-dataset"></a><span data-ttu-id="ed125-144">รับคิวรี DAX สำหรับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ed125-144">Get the DAX query for the dataset</span></span>

<span data-ttu-id="ed125-145">เมื่อคุณต้องการให้ข้อมูลในรายงาน Power BI ของคุณและในรายงานของตัวสร้างรายงานเป็นแบบเดียวกัน การเชื่อมต่อกับชุดข้อมูลจะไม่เพียงพอ</span><span class="sxs-lookup"><span data-stu-id="ed125-145">When you want the data in your Power BI report and in your Report Builder report to be the same, it's not enough to connect to the dataset.</span></span> <span data-ttu-id="ed125-146">คุณยังจำเป็นต้องมีคิวรีที่สร้างขึ้นบนชุดข้อมูลนั้นด้วย</span><span class="sxs-lookup"><span data-stu-id="ed125-146">You also need the query that's built on that dataset.</span></span>

### <a name="video-get-the-dax-query"></a><span data-ttu-id="ed125-147">วิดีโอ: รับคิวรี DAX</span><span class="sxs-lookup"><span data-stu-id="ed125-147">Video: Get the DAX query</span></span>

<span data-ttu-id="ed125-148">ในวิดีโอต่อไปนี้ Chris Finlan สาธิตวิธีรับ DAX ที่คุณต้องการสำหรับรายงานที่มีการแบ่งหน้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="ed125-148">In the following video, Chris Finlan demonstrates how to get the DAX you need for your paginated report.</span></span>

<iframe width="400" height="450" src="https://www.youtube.com/embed/NfoOK4QRkhI" frameborder="0" allowfullscreen></iframe>

### <a name="steps-to-get-the-dax-query"></a><span data-ttu-id="ed125-149">ขั้นตอนในการรับคิวรี DAX</span><span class="sxs-lookup"><span data-stu-id="ed125-149">Steps to get the DAX query</span></span>

<span data-ttu-id="ed125-150">ในตอนนี้นี่คือขั้นตอนในการรับคิวรี</span><span class="sxs-lookup"><span data-stu-id="ed125-150">Now here are the steps to get the query.</span></span>

1. <span data-ttu-id="ed125-151">เปิดรายงาน Power BI (.pbix) ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ed125-151">Open the Power BI report (.pbix) in Power BI Desktop.</span></span>
1. <span data-ttu-id="ed125-152">ตรวจสอบให้แน่ใจว่าคุณมีตารางในรายงานที่มีข้อมูลทั้งหมดที่คุณต้องการในรายงานแบบแบ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="ed125-152">Make sure you have a table in your report that contains all the data you want in your paginated report.</span></span> <span data-ttu-id="ed125-153">ตารางต้องมีคุณสมบัติตรงตามข้อกำหนดทั้งสองนี้:</span><span class="sxs-lookup"><span data-stu-id="ed125-153">The table needs to meet these two requirements:</span></span>
    - <span data-ttu-id="ed125-154">ต้องเป็นตารางแบน ไม่ใช่เมทริกซ์หรือวิชวลอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="ed125-154">It needs to be a flat table, not a matrix or other visual.</span></span> <span data-ttu-id="ed125-155">หากไม่ใช่ตาราง ให้แปลงเป็นตารางตอนนี้ ทำตามขั้นตอนของ Performance Analyzer ที่ตามมา จากนั้นแปลงกลับเป็นวิชวลที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="ed125-155">If it's not a table, convert it to a table now, go through the Performance Analyzer steps that follow, then convert it back to the visual you want.</span></span>
    - <span data-ttu-id="ed125-156">สำหรับเขตข้อมูลแบบตัวเลข คุณจำเป็นต้องใช้ *หน่วยวัดที่กำหนดไว้ล่วงหน้า*</span><span class="sxs-lookup"><span data-stu-id="ed125-156">For your numeric fields, you need to use *predefined measures*.</span></span> <span data-ttu-id="ed125-157">หน่วยวัดดังกล่าวมีสัญลักษณ์เครื่องคิดเลขอยู่ข้างๆ</span><span class="sxs-lookup"><span data-stu-id="ed125-157">They have a calculator symbol next to them.</span></span> <span data-ttu-id="ed125-158">อ่านเกี่ยวกับ [การสร้างหน่วยวัด](../transform-model/desktop-measures.md)</span><span class="sxs-lookup"><span data-stu-id="ed125-158">Read about [creating measures](../transform-model/desktop-measures.md).</span></span> 

        ![ไอคอนหน่วยวัด](media/report-builder-shared-datasets/power-bi-measure-icon.png)

1. <span data-ttu-id="ed125-160">บนริบบอน **มุมมอง** ให้เลือก **ตัววิเคราะห์ประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="ed125-160">On the **View** ribbon, select **Performance Analyzer**.</span></span>

    ![เปิด ตัววิเคราะห์ประสิทธิภาพ (Performance Analyzer)](media/report-builder-shared-datasets/power-bi-performance-analyzer.png)

1. <span data-ttu-id="ed125-162">ในบานหน้าต่าง **ตัววิเคราะห์ประสิทธิภาพ** ให้เลือก **เริ่มการบันทึก** จากนั้นเลือก **รีเฟรชวิชวล**</span><span class="sxs-lookup"><span data-stu-id="ed125-162">In the **Performance Analyzer** pane, select **Start recording**, then select **Refresh visuals**.</span></span>

    ![รีเฟรชวิชวล](media/report-builder-shared-datasets/power-bi-performance-analyzer-refresh-visuals.png)

1. <span data-ttu-id="ed125-164">ขยายเครื่องหมายบวก ( **+** ) ที่อยู่ถัดจากชื่อตาราง แล้วเลือก **คัดลอกคิวรี**</span><span class="sxs-lookup"><span data-stu-id="ed125-164">Expand the plus sign (**+**) next to the table name, and select **Copy query**.</span></span> <span data-ttu-id="ed125-165">คิวรีเป็นสูตร DAX ที่คุณต้องการสำหรับชุดข้อมูลในตัวสร้างรายงานของ Power BI</span><span class="sxs-lookup"><span data-stu-id="ed125-165">The query is the DAX formula you need for the dataset in Power BI Report Builder.</span></span>

    ![คัดลอกคิวรี](media/report-builder-shared-datasets/power-bi-performance-analyzer-copy-query.png)

## <a name="create-the-dataset-with-the-query"></a><span data-ttu-id="ed125-167">สร้างชุดข้อมูลพร้อมคิวรี</span><span class="sxs-lookup"><span data-stu-id="ed125-167">Create the dataset with the query</span></span>

1. <span data-ttu-id="ed125-168">กลับไปที่ตัวสร้างรายงานของ Power BI</span><span class="sxs-lookup"><span data-stu-id="ed125-168">Go back to Power BI Report Builder.</span></span>
1. <span data-ttu-id="ed125-169">คลิกขวาที่ชุดข้อมูลภายใต้ **แหล่งข้อมูล** และเลือก **เพิ่มชุดข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="ed125-169">Right-click the dataset under **Data Sources** and select **Add Dataset**.</span></span>

    ![เพิ่มชุดข้อมูล](media/report-builder-shared-datasets/power-bi-report-builder-add-dataset.png)

1. <span data-ttu-id="ed125-171">ในคุณสมบัติชุดข้อมูล ให้กำหนดชื่อ และเลือก **ตัวออกแบบคิวรี**</span><span class="sxs-lookup"><span data-stu-id="ed125-171">In Dataset Properties, give it a name, and select **Query Designer**.</span></span>

4. <span data-ttu-id="ed125-172">ตรวจสอบให้แน่ใจว่ามีการเลือก **DAX** และยกเลิกการเลือกไอคอน **โหมดการออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="ed125-172">Make sure **DAX** is selected, and deselect the **Design Mode** icon.</span></span>

    ![ตัวออกแบบคิวรีในตัวสร้างรายงาน](media/report-builder-shared-datasets/power-bi-report-builder-query-designer.png)

1. <span data-ttu-id="ed125-174">ในกล่องด้านบน ให้วางคิวรีที่คุณคัดลอกจาก Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="ed125-174">In the upper box, paste the query you copied from Power BI Desktop.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ed125-175">ถ้าคิวรีของคุณมีฟังก์ชัน TOPN ให้ลบออกจากคิวรีของคุณ</span><span class="sxs-lookup"><span data-stu-id="ed125-175">If your query includes the TOPN function, delete it from your query.</span></span>

1. <span data-ttu-id="ed125-176">เลือก **ดำเนินการคิวรี** (เครื่องหมายอัศเจรีย์สีแดง !) เพื่อให้แน่ใจว่าคิวรีของคุณทำงาน</span><span class="sxs-lookup"><span data-stu-id="ed125-176">Select **Execute Query** (the red exclamation mark, !) to be sure your query works.</span></span> 

    ![เรียกใช้คิวรี](media/report-builder-shared-datasets/power-bi-report-builder-run-query.png)

    <span data-ttu-id="ed125-178">คุณจะเห็นผลลัพธ์ของคิวรีในกล่องด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="ed125-178">You see the results of the query in the lower box.</span></span>

    ![ผลลัพธ์คิวรี](media/report-builder-shared-datasets/power-bi-report-builder-query-results.png)

1. <span data-ttu-id="ed125-180">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ed125-180">Select **OK**.</span></span>

    <span data-ttu-id="ed125-181">คุณเห็นคิวรีของคุณในหน้าต่าง **คิวรี** ของกล่องโต้ตอบ **คุณสมบัติของชุดข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="ed125-181">You see your query in the **Query** window of the **Dataset Properties** dialog box.</span></span>

    ![ในกล่องโต้ตอบ คุณสมบัติของชุดข้อมูล](media/report-builder-shared-datasets/power-bi-report-builder-dataset-properties.png)

1. <span data-ttu-id="ed125-183">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ed125-183">Select **OK**.</span></span>

    <span data-ttu-id="ed125-184">ในตอนนี้คุณจะเห็นชุดข้อมูลใหม่ของคุณที่มีรายการของเขตข้อมูลในบานหน้าต่างข้อมูลรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed125-184">Now you see your new dataset with a list of its fields in the Report Data pane.</span></span>

    ![ชุดข้อมูลในบานหน้าต่างข้อมูลรายงาน](media/report-builder-shared-datasets/power-bi-report-builder-dataset.png)

## <a name="create-a-table-in-the-report"></a><span data-ttu-id="ed125-186">สร้างตารางในรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed125-186">Create a table in the report</span></span>

<span data-ttu-id="ed125-187">หนึ่งในแนวทางที่รวดเร็วสำหรับการสร้างตารางคือ ใช้ตัวช่วยสร้างตาราง</span><span class="sxs-lookup"><span data-stu-id="ed125-187">One quick way to create a table is to use the Table Wizard.</span></span>

1. <span data-ttu-id="ed125-188">บนริบบอน **แทรก** เลือก **ตาราง** > **ตัวช่วยสร้างตาราง**</span><span class="sxs-lookup"><span data-stu-id="ed125-188">On the **Insert** ribbon, select **Table** > **Table Wizard**.</span></span>

    ![เริ่มตัวช่วยสร้างตาราง](media/report-builder-shared-datasets/power-bi-report-builder-table-wizard.png)

1. <span data-ttu-id="ed125-190">เลือกชุดข้อมูลที่คุณสร้างขึ้นด้วยคิวรี DAX > **ถัดไปt**</span><span class="sxs-lookup"><span data-stu-id="ed125-190">Choose the dataset you created with the DAX query > **Next**.</span></span>

    ![เลือกชุดข้อมูล](media/report-builder-shared-datasets/power-bi-report-builder-choose-dataset.png)

1. <span data-ttu-id="ed125-192">หากต้องการสร้างตารางแบน ให้เลือกเขตข้อมูลที่คุณต้องการใน **เขตข้อมูลที่พร้อมใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="ed125-192">To make a flat table, select the fields you want in **Available fields**.</span></span> <span data-ttu-id="ed125-193">คุณสามารถเลือกเขตข้อมูลหลายรายการในครั้งเดียวโดยการเลือกรายการแรกที่คุณต้องการ จากนั้นกดปุ่ม Shift ค้างไว้และเลือกรายการสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="ed125-193">You can select multiple fields at a time by selecting the first one you want, holding the Shift key, and selecting the last one.</span></span>

    ![เลือกเขตข้อมูลหลายรายการ](media/report-builder-shared-datasets/power-bi-report-builder-select-fields.png)

1. <span data-ttu-id="ed125-195">ลากเขตข้อมูลไปยังกล่อง **ค่า** > **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="ed125-195">Drag the fields to the **Values** box > **Next**.</span></span>

    ![ตัวช่วยสร้างตาราง](media/report-builder-shared-datasets/power-bi-report-builder-value-fields.png)

1. <span data-ttu-id="ed125-197">เลือกตัวเลือกเค้าโครงที่คุณต้องการ > **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="ed125-197">Choose the layout options you want > **Next**.</span></span>

1. <span data-ttu-id="ed125-198">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="ed125-198">Select **Finish**.</span></span>
    <span data-ttu-id="ed125-199">คุณจะเห็นตารางของคุณในมุมมองออกแบบ</span><span class="sxs-lookup"><span data-stu-id="ed125-199">You see your table in Design View.</span></span>

    ![มุมมองการออกแบบรายงาน](media/report-builder-shared-datasets/power-bi-report-builder-design-view.png)

1. <span data-ttu-id="ed125-201">เลือก **คลิกเพื่อเพิ่มชื่อเรื่อง** และเพิ่มชื่อเรื่อง</span><span class="sxs-lookup"><span data-stu-id="ed125-201">Select **Click to add title** and add a title.</span></span>

1. <span data-ttu-id="ed125-202">เลือก **เรียกใช้** เพื่อแสดงตัวอย่างรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed125-202">Select **Run** to preview your report.</span></span>

    ![การแสดงตัวอย่างรายงาน](media/report-builder-shared-datasets/power-bi-report-builder-preview.png)

1. <span data-ttu-id="ed125-204">เลือก **พิมพ์เค้าโครง** เพื่อดูว่ารายงานของคุณจะมีลักษณะอย่างไร</span><span class="sxs-lookup"><span data-stu-id="ed125-204">Select **Print Layout** to see how your report will look printed.</span></span> 

    <span data-ttu-id="ed125-205">เค้าโครงรายงานนี้ต้องการการทำงานบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="ed125-205">This report layout needs some work.</span></span> <span data-ttu-id="ed125-206">ซึ่งมี 54 หน้า เนื่องจากคอลัมน์และระยะขอบทำให้ตารางกว้างสองหน้า</span><span class="sxs-lookup"><span data-stu-id="ed125-206">It has 54 pages because the columns and margins make the table two pages wide.</span></span>

    ![พิมพ์เค้าโครงของรายงาน](media/report-builder-shared-datasets/power-bi-report-builder-print-layout-2-p1-p2.png)

## <a name="format-the-report"></a><span data-ttu-id="ed125-208">จัดรูปแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed125-208">Format the report</span></span>

<span data-ttu-id="ed125-209">คุณมีตัวเลือกการจัดรูปแบบหลายตัวเลือกเพื่อทำให้ตารางของคุณพอดีกับหนึ่งหน้า</span><span class="sxs-lookup"><span data-stu-id="ed125-209">You have several formatting options to make your table fit on one page.</span></span> 

1. <span data-ttu-id="ed125-210">คุณสามารถบีบระยะขอบของหน้าให้แคบลงได้ในบานหน้าต่างคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="ed125-210">You can narrow the page margins in the Properties pane.</span></span> <span data-ttu-id="ed125-211">หากคุณไม่เห็นบานหน้าต่างคุณสมบัติ บนริบบอน **มุมมอง** ให้เลือกช่องทำเครื่องหมาย **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="ed125-211">If you don't see the Properties pane, on the **View** ribbon, select the **Properties** check box.</span></span>

1. <span data-ttu-id="ed125-212">เลือกรายงาน ไม่ใช่ตารางหรือชื่อเรื่อง</span><span class="sxs-lookup"><span data-stu-id="ed125-212">Select the report, not the table or title.</span></span>
1. <span data-ttu-id="ed125-213">ในบานหน้าต่าง **คุณสมบัติของรายงาน** ภายใต้ **หน้า**, ขยาย **ระยะขอบ** และเปลี่ยนแต่ละรายการเป็น **0.75in**</span><span class="sxs-lookup"><span data-stu-id="ed125-213">In the **Report Properties** pane, under **Page**, expand **Margins** and change each one to **0.75in**.</span></span>

    ![ตั้งค่าระยะขอบกระดาษ](media/report-builder-shared-datasets/power-bi-report-builder-page-margins.png)

1. <span data-ttu-id="ed125-215">คุณยังสามารถทำให้คอลัมน์แคบลงได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="ed125-215">You can also make columns narrower.</span></span> <span data-ttu-id="ed125-216">เลือกเส้นขอบคอลัมน์และลากด้านขวาไปทางซ้าย</span><span class="sxs-lookup"><span data-stu-id="ed125-216">Select the column border and drag the right side to the left.</span></span>

    ![ตั้งค่าความกว้างคอลัมน์](media/report-builder-shared-datasets/power-bi-report-builder-column-width.png)

1. <span data-ttu-id="ed125-218">ตัวเลือกอื่นคือ เพื่อตรวจสอบให้แน่ใจว่ามีการจัดรูปแบบค่าตัวเลขไว้อย่างดีแล้ว</span><span class="sxs-lookup"><span data-stu-id="ed125-218">Another option is to make sure the number values are formatted well.</span></span> <span data-ttu-id="ed125-219">เลือกเซลล์ที่มีค่าตัวเลข</span><span class="sxs-lookup"><span data-stu-id="ed125-219">Select a cell with a number value.</span></span> 
    > [!TIP]
    > <span data-ttu-id="ed125-220">คุณสามารถจัดรูปแบบได้มากกว่าหนึ่งเซลล์ในครั้งเดียวโดยการกดแป้น Shift ค้างไว้ในขณะที่คุณเลือกเซลล์อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="ed125-220">You can format more than cell at a time by holding down the Shift key while you select the other cells.</span></span>

    ![เลือกมากกว่าหนึ่งเซลล์](media/report-builder-shared-datasets/power-bi-report-builder-select-cells.png)

1. <span data-ttu-id="ed125-222">บนริบบอน **หน้าแรก** ในส่วน **ตัวเลข** ให้เปลี่ยนรูปแบบ **ค่าเริ่มต้น** เป็นรูปแบบตัวเลข เช่น **สกุลเงิน**</span><span class="sxs-lookup"><span data-stu-id="ed125-222">On the **Home** ribbon, in the **Number** section, change the **Default** format to a numeric format such as **Currency**.</span></span>

    ![ตั้งค่ารูปแบบตัวเลข](media/report-builder-shared-datasets/power-bi-report-builder-number-format.png)

1. <span data-ttu-id="ed125-224">เปลี่ยนสไตล์ **ข้อความตัวอย่าง** เป็น **ค่าตัวอย่าง** เพื่อให้คุณเห็นการจัดรูปแบบในเซลล์</span><span class="sxs-lookup"><span data-stu-id="ed125-224">Change the **Placeholder** style to **Sample Values** so you can see the formatting in the cell.</span></span> 

    ![แสดงค่าตัวอย่าง](media/report-builder-shared-datasets/power-bi-report-builder-sample-values.png)

1. <span data-ttu-id="ed125-226">หากเหมาะสม ในส่วน **ตัวเลข** ให้ลดตำแหน่งทศนิยมเพื่อประหยัดพื้นที่มากขึ้น</span><span class="sxs-lookup"><span data-stu-id="ed125-226">If appropriate, in the **Number** section decrease the decimals to save more space.</span></span>

### <a name="getting-rid-of-blank-pages"></a><span data-ttu-id="ed125-227">การกำจัดหน้าว่าง</span><span class="sxs-lookup"><span data-stu-id="ed125-227">Getting rid of blank pages</span></span>

<span data-ttu-id="ed125-228">แม้ว่าคุณจะทำให้ระยะขอบและคอลัมน์ของตารางแคบลง แต่รายงานของคุณก็อาจลงท้ายด้วยหน้าว่างเปล่าได้</span><span class="sxs-lookup"><span data-stu-id="ed125-228">Even if you've made the margins and the table columns narrower, you may still end up with every other page being blank.</span></span> <span data-ttu-id="ed125-229">ทำไม?</span><span class="sxs-lookup"><span data-stu-id="ed125-229">Why?</span></span> <span data-ttu-id="ed125-230">เป็นเรื่องของคณิตศาสตร์</span><span class="sxs-lookup"><span data-stu-id="ed125-230">Because of the math.</span></span> 

<span data-ttu-id="ed125-231">เมื่อคุณเพิ่มระยะขอบของหน้าตามที่คุณตั้งค่าไว้ รวมถึงความกว้างของ *เนื้อความ* ในรายงาน ซึ่งจะต้องมีค่าน้อยกว่าความกว้างของรูปแบบรายงาน</span><span class="sxs-lookup"><span data-stu-id="ed125-231">When you add up the page margins you set, plus the width of the *body* of the report, it has to be less than the width of the report format.</span></span>

<span data-ttu-id="ed125-232">ตัวอย่างเช่น สมมติว่ารายงานของคุณมีรูปแบบ 8.5" X 11" และคุณได้ตั้งค่าระยะขอบด้านข้างแต่ละด้านเป็น 0.75</span><span class="sxs-lookup"><span data-stu-id="ed125-232">For example, say your report has an 8.5" X 11" format and you've set the side margins to 0.75 each.</span></span> <span data-ttu-id="ed125-233">ระยะขอบทั้งสองบีบเข้าหากันรวม 1.5" ดังนั้นส่วนเนื้อความจะต้องมีความกว้างน้อยกว่า 7"</span><span class="sxs-lookup"><span data-stu-id="ed125-233">The two margins together make 1.5", so the body has to be less than 7" wide.</span></span>

1. <span data-ttu-id="ed125-234">เลือกขอบด้านขวาของพื้นผิวการออกแบบรายงานและลาก ดังนั้นจึงมีค่าน้อยกว่าจำนวนที่ต้องการบนไม้บรรทัด</span><span class="sxs-lookup"><span data-stu-id="ed125-234">Select the right edge of the report design surface, and drag it so it's less than the desired number on the ruler.</span></span> 

    > [!TIP]
    > <span data-ttu-id="ed125-235">คุณสามารถตั้งค่าได้อย่างแม่นยำยิ่งขึ้นในคุณสมบัติ **เนื้อความ**</span><span class="sxs-lookup"><span data-stu-id="ed125-235">You can set it more accurately in the **Body** properties.</span></span> <span data-ttu-id="ed125-236">ภายใต้ **ขนาด** ให้ตั้งค่าคุณสมบัติ **ความกว้าง**</span><span class="sxs-lookup"><span data-stu-id="ed125-236">Under **Size**, set the **Width** property.</span></span>

    ![ตั้งค่าขนาดเนื้อความ](media/report-builder-shared-datasets/power-bi-report-builder-body-size.png)

1. <span data-ttu-id="ed125-238">เลือก **เรียกใช้งาน** เพื่อดูตัวอย่างรายงานของคุณและตรวจสอบให้แน่ใจว่าคุณได้กำจัดหน้าว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="ed125-238">Select **Run** to preview your report and make sure you've gotten rid of the blank pages.</span></span> <span data-ttu-id="ed125-239">ในตอนนี้ รายงานนี้มีเพียง 26 หน้าแทนที่จะเป็น 54 ตามเดิม</span><span class="sxs-lookup"><span data-stu-id="ed125-239">This report now has only 26 pages, instead of the original 54.</span></span> <span data-ttu-id="ed125-240">สำเร็จ!</span><span class="sxs-lookup"><span data-stu-id="ed125-240">Success!</span></span>

    ![พิมพ์หน้าที่ไม่ว่างเปล่า](media/report-builder-shared-datasets/power-bi-report-builder-print-26-pgs.png)

## <a name="limitations-and-considerations"></a><span data-ttu-id="ed125-242">ข้อจำกัดและข้อควรพิจารณา</span><span class="sxs-lookup"><span data-stu-id="ed125-242">Limitations and considerations</span></span> 

- <span data-ttu-id="ed125-243">สำหรับชุดข้อมูลที่ใช้การเชื่อมต่อสดไปยังบริการวิเคราะห์ข้อมูล คุณสามารถเชื่อมต่อโดยตรงโดยใช้การเชื่อมต่อบริการวิเคราะห์พื้นฐานแทนชุดข้อมูลที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="ed125-243">For datasets that use a Live Connection to Analysis Services, you can connect directly by using the underlying Analysis Services connection instead of a shared dataset.</span></span>
- <span data-ttu-id="ed125-244">ถ้าคุณต้องการใช้ชุดข้อมูล Power BI ที่ใช้ DirectQuery ใน Power BI Report Builder ชุดข้อมูลจะต้องรวมหน่วยวัด แม้ว่าคุณจะไม่ได้วางแผนที่จะแสดงหน่วยวัดในรายงานของคุณก็ตาม</span><span class="sxs-lookup"><span data-stu-id="ed125-244">If you want to use a Power BI dataset that uses DirectQuery in Power BI Report Builder, the dataset has to include a measure, even if you don't plan to surface the measure in your report.</span></span> <span data-ttu-id="ed125-245">หากไม่มีหน่วยวัด ชุดข้อมูลจะไม่ส่งคืนผลลัพธ์ข้อมูลที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="ed125-245">Without the measure, the dataset won't return proper data results.</span></span>
- <span data-ttu-id="ed125-246">ชุดข้อมูลที่มีการส่งเสริมหรือได้รับการรับรองจะปรากฏในรายการชุดข้อมูลที่มี แต่ไม่ได้ทำเครื่องหมายเช่นนั้น</span><span class="sxs-lookup"><span data-stu-id="ed125-246">Datasets with Promoted or Certified endorsements appear in the list of available datasets, but they aren't marked as such.</span></span> 
- <span data-ttu-id="ed125-247">คุณไม่สามารถฝังรายงานที่มีการแบ่งหน้าที่อ้างอิงตามชุดข้อมูลที่ใช้ร่วมกันของ Power BI ในสถานการณ์ "แอปเป็นเจ้าของข้อมูล"</span><span class="sxs-lookup"><span data-stu-id="ed125-247">You can't embed paginated reports that are based on Power BI shared datasets in the "App Owns Data" scenario.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ed125-248">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="ed125-248">Next steps</span></span>

- [<span data-ttu-id="ed125-249">รายงานแบบแบ่งหน้าใน Power BI Premium คืออะไร</span><span class="sxs-lookup"><span data-stu-id="ed125-249">What are paginated reports in Power BI Premium?</span></span>](paginated-reports-report-builder-power-bi.md)
