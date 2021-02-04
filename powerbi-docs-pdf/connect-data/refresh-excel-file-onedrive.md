---
title: รีเฟรชชุดข้อมูลที่สร้างขึ้นจากสมุดงาน Excel - ระบบคลาวด์
description: รีเฟรชชุดข้อมูลที่สร้างขึ้นจากสมุดงาน Excel ใน OneDrive หรือ SharePoint Online
author: davidiseminger
ms.author: davidi
ms.reviewer: kayu
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 06/06/2019
LocalizationGroup: Data refresh
ms.openlocfilehash: ed4ba65da4c4b027d5e789844a86e57c2a9c478c
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410815"
---
# <a name="refresh-a-dataset-created-from-an-excel-workbook-on-onedrive-or-sharepoint-online"></a><span data-ttu-id="178b7-103">รีเฟรชชุดข้อมูลที่สร้างขึ้นจากสมุดงาน Excel ใน OneDrive หรือ SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="178b7-103">Refresh a dataset created from an Excel workbook on OneDrive, or SharePoint Online</span></span>

<span data-ttu-id="178b7-104">คุณสามารถนำเข้าสมุดงาน Excel ที่เก็บไว้บนเครื่องของคุณ หรือในพื้นที่เก็บข้อมูลบนคลาวด์ เช่น OneDrive สำหรับธุรกิจ หรือ SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="178b7-104">You can import Excel workbooks that are stored on your local machine, or in cloud storage such as OneDrive for Business or SharePoint Online.</span></span> <span data-ttu-id="178b7-105">เราจะดูที่ข้อดีของการใช้พื้นที่เก็บข้อมูลบนคลาวด์สำหรับไฟล์ Excel ของคุณ</span><span class="sxs-lookup"><span data-stu-id="178b7-105">We will look at the advantages of using cloud storage for your Excel files.</span></span> <span data-ttu-id="178b7-106">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการนำเข้าไฟล์ Excel ลงใน Power BI ดูที่[รับข้อมูลจากไฟล์สมุดงาน Excel](service-excel-workbook-files.md)</span><span class="sxs-lookup"><span data-stu-id="178b7-106">For more information on how to import Excel files into Power BI, see [Get data from Excel workbook files](service-excel-workbook-files.md).</span></span>

## <a name="what-are-the-advantages"></a><span data-ttu-id="178b7-107">มีข้อดีอะไรบ้าง</span><span class="sxs-lookup"><span data-stu-id="178b7-107">What are the advantages?</span></span>

<span data-ttu-id="178b7-108">การนำเข้าไฟล์จาก OneDrive หรือ SharePoint Online เป็นวิธีที่ดีในการตรวจสอบให้แน่ใจว่างานที่คุณกำลังทำอยู่ใน Excel ยังคงซิงค์กับบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="178b7-108">Importing files from OneDrive, or SharePoint Online, is a great way to make sure the work you’re doing in Excel stays in-sync with the Power BI service.</span></span> <span data-ttu-id="178b7-109">ข้อมูลใด ๆ ที่คุณโหลดลงในแบบจำลองของไฟล์จะได้รับการนำเข้าลงในชุดข้อมูล และจะมีการโหลดรายงานใด ๆ ที่คุณสร้างในไฟล์ลงใน “รายงาน” ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="178b7-109">Any data you’ve loaded into your file’s model is imported into the dataset, and any reports you’ve created in the file are loaded into Reports in Power BI.</span></span> <span data-ttu-id="178b7-110">ถ้าคุณทำการเปลี่ยนแปลงไฟล์ของคุณใน OneDrive หรือ SharePoint Online เช่น เพิ่มหน่วยวัดใหม่ เปลี่ยนชื่อคอลัมน์ หรือแก้ไขการแสดงวิชวล เมื่อคุณบันทึก การเปลี่ยนแปลงเหล่านั้นจะได้รับการอัปเดตใน Power BI เช่นกัน โดยปกติจะดำเนินการอัปเดตภายในหนึ่งชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="178b7-110">If you make changes to your file on OneDrive, or SharePoint Online, like add new measures, change column names, or edit visualizations, once you save, those changes are updated in Power BI too, usually within about an hour.</span></span>

<span data-ttu-id="178b7-111">เมื่อคุณนำเข้าสมุดงาน Excel จาก OneDrive ส่วนบุคคลของคุณ ข้อมูลใด ๆ ในสมุดงาน เช่น ตารางในแผ่นงานและ/ หรือข้อมูลที่โหลดลงในแบบจำลองข้อมูล Excel และโครงสร้างของแบบจำลองข้อมูล จะได้รับการนำเข้าลงในชุดข้อมูลใหม่ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="178b7-111">When you import an Excel workbook from your personal OneDrive, any data in the workbook, like tables in worksheets and/or data that are loaded into the Excel data model and the structure of the data model, are imported into a new dataset in Power BI.</span></span> <span data-ttu-id="178b7-112">การแสดงวิชวล Power View ใด ๆ จะได้รับการสร้างใหม่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="178b7-112">Any Power View visualizations are re-created in Reports.</span></span> <span data-ttu-id="178b7-113">Power BI เชื่อมต่อกับสมุดงานใน OneDrive หรือ SharePoint Online โดยอัตโนมัติเพื่อตรวจสอบการอัปเดตทุก ๆ ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="178b7-113">Power BI automatically connects to the workbook on OneDrive, or SharePoint Online, about every hour to check for updates.</span></span> <span data-ttu-id="178b7-114">ถ้าสมุดงานมีการเปลี่ยนแปลง Power BI จะรีเฟรชชุดข้อมูลและรายงานในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="178b7-114">If the workbook has changed, Power BI will refresh the dataset and reports in the Power BI service.</span></span>

<span data-ttu-id="178b7-115">คุณสามารถรีเฟรชชุดข้อมูลในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="178b7-115">You can refresh the dataset in the Power BI service.</span></span> <span data-ttu-id="178b7-116">เมื่อคุณทำการรีเฟรชด้วยตนเอง หรือรีเฟรชตามกำหนดการในชุดข้อมูล Power BI จะเชื่อมต่อโดยตรงไปยังแหล่งข้อมูลภายนอกเพื่อสร้างคิวรีสำหรับข้อมูลที่อัปเดตแล้ว และโหลดลงในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="178b7-116">When you manually refresh, or schedule refresh, on the dataset, Power BI connects directly to the external data sources to query for updated data it then loads into the dataset.</span></span> <span data-ttu-id="178b7-117">การรีเฟรชชุดข้อมูลจากภายใน Power BI จะไม่รีเฟรชข้อมูลในสมุดงานใน OneDrive หรือ SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="178b7-117">Refreshing a dataset from within Power BI does not refresh the data in the workbook on OneDrive, or SharePoint Online.</span></span> 

## <a name="whats-supported"></a><span data-ttu-id="178b7-118">รับรองอะไรบ้าง</span><span class="sxs-lookup"><span data-stu-id="178b7-118">What’s supported?</span></span>

<span data-ttu-id="178b7-119">ใน Power BI **รีเฟรชตอนนี้** และ **กำหนดการรีเฟรช** ใช้กับชุดข้อมูลที่สร้างจากไฟล์ Power BI Desktop ที่นำเข้าจากไดรฟ์ภายในเครื่องที่มีการใช้ “รับข้อมูล/ตัวแก้ไขคิวรี” เพื่อเชื่อมต่อและโหลดข้อมูลจากแหล่งข้อมูลหนึ่งจากหลาย ๆ แหล่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="178b7-119">In Power BI, **Refresh Now** and **Schedule Refresh** are supported for datasets created from Power BI Desktop files imported from a local drive where Get Data/Query Editor is used to connect to and load data from any of the following data sources:</span></span>  

### <a name="power-bi-gateway---personal"></a><span data-ttu-id="178b7-120">Power BI Gateway - Personal</span><span class="sxs-lookup"><span data-stu-id="178b7-120">Power BI Gateway - Personal</span></span>

* <span data-ttu-id="178b7-121">แหล่งข้อมูลออนไลน์ทั้งหมดที่แสดงใน รับข้อมูลและตัวแก้ไขคิวรี ของ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="178b7-121">All online data sources shown in Power BI Desktop’s Get Data and Query Editor.</span></span>
* <span data-ttu-id="178b7-122">แหล่งข้อมูลภายในองค์กรทั้งหมดที่แสดงอยู่ใน รับข้อมูลและตัวแก้ไขคิวรี ของ Power BI Desktop ยกเว้นไฟล์ Hadoop (HDFS) และ Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="178b7-122">All on-premises data sources shown in Power BI Desktop’s Get Data and Query Editor except for Hadoop file (HDFS) and Microsoft Exchange.</span></span>

<!-- Refresh Data sources-->
[!INCLUDE [refresh-datasources](../includes/refresh-datasources.md)]

> [!NOTE]
> <span data-ttu-id="178b7-123">เกตเวย์ต้องได้รับการติดตั้ง และเรียกใช้เพื่อให้ Power BI เชื่อมต่อกับแหล่งข้อมูลภายในองค์กร และรีเฟรชชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="178b7-123">A gateway must be installed and running in order for Power BI to connect to on-premises data sources and refresh the dataset.</span></span>
>
>

## <a name="onedrive-or-onedrive-for-business-whats-the-difference"></a><span data-ttu-id="178b7-124">OneDrive หรือ OneDrive สำหรับธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="178b7-124">OneDrive or OneDrive for Business.</span></span> <span data-ttu-id="178b7-125">ความแตกต่างคืออะไร</span><span class="sxs-lookup"><span data-stu-id="178b7-125">What’s the difference?</span></span>

<span data-ttu-id="178b7-126">ถ้าคุณมีทั้ง OneDrive ส่วนบุคคล และ OneDrive สำหรับธุรกิจ เราแนะนำให้คุณเก็บไฟล์ต่างๆ ที่คุณต้องการนำเข้าไปใน Power BI ใน OneDrive สำหรับธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="178b7-126">If you have both a personal OneDrive and OneDrive for Business, it’s recommended you keep any files you want to import into Power BI in OneDrive for Business.</span></span> <span data-ttu-id="178b7-127">นี่คือสาเหตุว่าทำไม: คุณอาจใช้บัญชีที่ต่างกันสองบัญชีในการลงชื่อเข้าใช้ OneDrive ส่วนบุคคล และ OneDrive สำหรับธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="178b7-127">Here’s why: You likely use two different accounts to sign into them.</span></span>

<span data-ttu-id="178b7-128">การเชื่อมต่อกับ OneDrive for Business ใน Power BI มักทำได้อย่างราบรื่น เพราะบัญชีที่คุณลงชื่อเข้าใช้ Power BI มักเป็นบัญชีเดียวกับที่ลงชื่อเข้าใช้ใน OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="178b7-128">Connecting to OneDrive for Business in Power BI is typically seamless because the same account you use to sign into Power BI is often the same account used to sign into OneDrive for Business.</span></span> <span data-ttu-id="178b7-129">แต่ใน OneDrive ส่วนบุคคล คุณลงชื่อเข้าใช้ด้วย[บัญชี Microsoft](https://account.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="178b7-129">But, with personal OneDrive, you likely sign in with a different [Microsoft account](https://account.microsoft.com).</span></span>

<span data-ttu-id="178b7-130">เมื่อคุณลงชื่อเข้าใช้บัญชี Microsoft ของคุณ ตรวจสอบให้แน่ใจว่าเลือก **ให้ฉันลงชื่อเข้าใช้เสมอ**</span><span class="sxs-lookup"><span data-stu-id="178b7-130">When you sign in with your Microsoft account, be sure to select **Keep me signed in**.</span></span> <span data-ttu-id="178b7-131">และจากนั้น Power BI จะสามารถซิงโครไนซ์การอัปเดตใด ๆ ที่คุณทำกับไฟล์ใน Power BI Desktop ด้วยชุดข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="178b7-131">Power BI can then synchronize any updates you make in the file in Power BI Desktop with datasets in Power BI.</span></span>  

![ให้ฉันลงชื่อเข้าใช้เสมอ](media/refresh-excel-file-onedrive/refresh_signin_keepmesignedin.png)

<span data-ttu-id="178b7-133">ถ้าคุณทำการเปลี่ยนแปลงกับไฟล์ของคุณใน OneDrive ที่ไม่สามารถซิงโครไนซ์กับชุดข้อมูลหรือรายงานใน Power BI เนื่องจากข้อมูลประจำตัวของบัญชี Microsoft ของคุณอาจมีการเปลี่ยนแปลง คุณจะต้องเชื่อมต่อ และนำเข้าไฟล์ของคุณอีกครั้งจาก OneDrive ส่วนบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="178b7-133">If you make changes to your file on OneDrive that cannot be synchronized with the dataset or reports in Power BI, because your Microsoft account credentials might have changed, you’ll need to connect to and import your file again from your personal OneDrive.</span></span>

## <a name="options-for-connecting-to-excel-file"></a><span data-ttu-id="178b7-134">ตัวเลือกสำหรับการเชื่อมต่อไปยังไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="178b7-134">Options for connecting to Excel file</span></span>

<span data-ttu-id="178b7-135">เมื่อคุณเชื่อมต่อกับสมุดงาน Excel ใน OneDrive สำหรับธุรกิจ หรือ SharePoint Online คุณจะมีสองตัวเลือกเกี่ยวกับวิธีการนำสิ่งที่อยู่ในสมุดงานของคุณลงใน Power BI</span><span class="sxs-lookup"><span data-stu-id="178b7-135">When you connect to an Excel workbook in OneDrive for Business, or SharePoint Online, you’ll have two options on how to get what’s in your workbook into Power BI.</span></span>

<span data-ttu-id="178b7-136">[**นำเข้าข้อมูล Excel ลงใน Power BI**](service-excel-workbook-files.md#import-or-connect-to-an-excel-workbook-from-power-bi) – เมื่อคุณนำเข้าสมุดงาน Excel จาก OneDrive สำหรับธุรกิจ หรือ SharePoint Online จะมีการทำงานตามที่อธิบายไว้ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="178b7-136">[**Import Excel data into Power BI**](service-excel-workbook-files.md#import-or-connect-to-an-excel-workbook-from-power-bi) – When you import an Excel workbook from your OneDrive for Business, or SharePoint Online, it works as described above.</span></span>

<span data-ttu-id="178b7-137">[**เชื่อมต่อ จัดการ และดู Excel ใน Power BI**](service-excel-workbook-files.md#one-excel-workbook--two-ways-to-use-it) – เมื่อใช้ตัวเลือกนี้ ให้คุณสร้างการเชื่อมต่อจาก Power BI กับสมุดงานของคุณใน OneDrive สำหรับธุรกิจ หรือ SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="178b7-137">[**Connect, Manage, and View Excel in Power BI**](service-excel-workbook-files.md#one-excel-workbook--two-ways-to-use-it) – When using this option, you create a connection from Power BI right to your workbook on OneDrive for Business, or SharePoint Online.</span></span>

<span data-ttu-id="178b7-138">เมื่อคุณเชื่อมต่อกับสมุดงาน Excel ด้วยวิธีนี้ จะไม่มีการสร้างชุดข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="178b7-138">When you connect to an Excel workbook this way, a dataset is not created in Power BI.</span></span> <span data-ttu-id="178b7-139">อย่างไรก็ตาม สมุดงานจะปรากฏในบริการ Power BI ภายใต้ “รายงาน” ด้วยไอคอน Excel ที่อยู่ถัดจากชื่อ</span><span class="sxs-lookup"><span data-stu-id="178b7-139">However, the workbook will appear in the Power BI service under Reports with an Excel icon next to the name.</span></span> <span data-ttu-id="178b7-140">ซึ่งแตกต่างกับ Excel Online คือเมื่อคุณเชื่อมต่อกับสมุดงานของคุณจาก Power BI ถ้าสมุดงานของคุณมีการเชื่อมต่อกับแหล่งข้อมูลภายนอกที่โหลดข้อมูลลงในแบบจำลองข้อมูล Excel คุณสามารถตั้งค่าการรีเฟรชตามกำหนดการได้</span><span class="sxs-lookup"><span data-stu-id="178b7-140">Unlike with Excel Online, when you connect to your workbook from Power BI, if your workbook has connections to external data sources that load data into the Excel data model, you can set up a refresh schedule.</span></span>

<span data-ttu-id="178b7-141">เมื่อคุณตั้งค่ากำหนดการรีเฟรชด้วยวิธีนี้ จะมีความแตกต่างเพียงอย่างเดียวคือ ข้อมูลที่ได้รับการรีเฟรชจะเข้าไปอยู่ในแบบจำลองข้อมูลของสมุดงานใน OneDrive หรือ SharePoint Online แทนที่จะไปอยู่ในชุดข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="178b7-141">When you set up a refresh schedule this way, the only difference is refreshed data goes into the workbook’s data model on OneDrive, or SharePoint Online, rather than a dataset in Power BI.</span></span>

## <a name="how-do-i-make-sure-data-is-loaded-to-the-excel-data-model"></a><span data-ttu-id="178b7-142">ฉันจะแน่ใจได้อย่างไรว่าข้อมูลได้รับการโหลดไปยังแบบจำลองข้อมูล Excel</span><span class="sxs-lookup"><span data-stu-id="178b7-142">How do I make sure data is loaded to the Excel data model?</span></span>

<span data-ttu-id="178b7-143">เมื่อคุณใช้ Power Query (**รับและแปลงข้อมูล** ใน Excel 2016) เพื่อเชื่อมต่อกับแหล่งข้อมูล คุณจะมีหลายตัวเลือกสำหรับตำแหน่งที่จะโหลดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="178b7-143">When you use Power Query (**Get & Transform** in Excel 2016) to connect to a data source, you have several options where to load the data.</span></span> <span data-ttu-id="178b7-144">เมื่อต้องการตรวจสอบให้แน่ใจว่า คุณโหลดข้อมูลลงในแบบจำลองข้อมูล คุณต้องเลือก **เพิ่มข้อมูลนี้ลงในตัวเลือกแบบจำลองข้อมูล** ใน **โหลดไปยัง** กล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="178b7-144">To make sure you load data into the data model, you must select the **Add this data to the Data Model** option in the **Load To** dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="178b7-145">รูปภาพนี้แสดง Excel 2016</span><span class="sxs-lookup"><span data-stu-id="178b7-145">The images here show Excel 2016.</span></span>
>
>

<span data-ttu-id="178b7-146">ใน **ตัวนำทาง** คลิก **โหลดไปยัง...**</span><span class="sxs-lookup"><span data-stu-id="178b7-146">In **Navigator**, click **Load To…**</span></span>  

![โหลดไปยัง... คำสั่ง](media/refresh-excel-file-onedrive/refresh_loadtodm_1.png)

<span data-ttu-id="178b7-148">หรือ ถ้าคุณคลิก **แก้ไข** ใน **ตัวนำทาง** ตัวแก้ไขคิวรีจะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="178b7-148">Or, If you click **Edit** in **Navigator**, you’ll open the Query Editor.</span></span> <span data-ttu-id="178b7-149">ซึ่งคุณสามารถคลิก **ปิด & โหลดไปยัง...**</span><span class="sxs-lookup"><span data-stu-id="178b7-149">There you can click **Close & Load To….**</span></span>  

![ปิด & โหลดไปยัง... คำสั่ง](media/refresh-excel-file-onedrive/refresh_loadtodm_2.png)

<span data-ttu-id="178b7-151">จากนั้นใน **โหลดไปยัง** ตรวจสอบให้แน่ใจว่าคุณเลือก **เพิ่มข้อมูลนี้ลงในแบบจำลองข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="178b7-151">Then in **Load To**, make sure you select **Add this data to the Data Model**.</span></span>  

![เพิ่มสิ่งนี้ไปยังกล่องกาเครื่องหมายแบบจำลองข้อมูล](media/refresh-excel-file-onedrive/refresh_loadtodm_3.png)

### <a name="what-if-i-use-get-external-data-in-power-pivot"></a><span data-ttu-id="178b7-153">เกิดอะไรขึ้นถ้าฉันใช้ “รับข้อมูลภายนอกใน Power Pivot”</span><span class="sxs-lookup"><span data-stu-id="178b7-153">What if I use Get External Data in Power Pivot?</span></span>

<span data-ttu-id="178b7-154">ไม่มีปัญหา</span><span class="sxs-lookup"><span data-stu-id="178b7-154">No problem.</span></span> <span data-ttu-id="178b7-155">เมื่อใดก็ตามที่คุณใช้ Power Pivot เพื่อเชื่อมต่อ และคิวรีข้อมูลจากแหล่งข้อมูลภายในองค์กร หรือแหล่งข้อมูลออนไลน์ ข้อมูลจะได้รับการโหลดลงในแบบจำลองข้อมูลโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="178b7-155">Whenever you use Power Pivot to connect to and query data from an on-premises or online data source, the data is automatically loaded to the data model.</span></span>

## <a name="how-do-i-schedule-refresh"></a><span data-ttu-id="178b7-156">ฉันจะกำหนดเวลารีเฟรชได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="178b7-156">How do I schedule refresh?</span></span>

<span data-ttu-id="178b7-157">เมื่อคุณตั้งค่ากำหนดการรีเฟรช Power BI จะเชื่อมต่อโดยตรงไปยังแหล่งข้อมูลโดยใช้ข้อมูลการเชื่อมต่อและข้อมูลประจำตัวในชุดข้อมูลเพื่อคิวรีข้อมูลที่อัปเดตแล้ว จากนั้นจึงโหลดข้อมูลที่อัปเดตแล้วลงในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="178b7-157">When you set up a refresh schedule, Power BI connects directly to the data sources using connection information and credentials in the dataset to query for updated data, then loads the updated data into the dataset.</span></span> <span data-ttu-id="178b7-158">การแสดงภาพด้วยข้อมูลในรายงานและแดชบอร์ดที่อิงชุดข้อมูลนั้นในบริการของ Power BI จะได้รับการอัปเดตตามไปด้วย</span><span class="sxs-lookup"><span data-stu-id="178b7-158">Any visualizations in reports and dashboards based on that dataset in the Power BI service are also updated.</span></span>

<span data-ttu-id="178b7-159">สำหรับรายละเอียดเกี่ยวกับวิธีการตั้งค่าการรีเฟรชตามกำหนดการ ดูที่[กำหนดค่าการรีเฟรชตามกำหนดการ](refresh-scheduled-refresh.md)</span><span class="sxs-lookup"><span data-stu-id="178b7-159">For details on how to set up scheduled refresh, see [Configure scheduled refresh](refresh-scheduled-refresh.md).</span></span>

## <a name="when-things-go-wrong"></a><span data-ttu-id="178b7-160">เมื่อเกิดสิ่งผิดปกติขึ้น</span><span class="sxs-lookup"><span data-stu-id="178b7-160">When things go wrong</span></span>

<span data-ttu-id="178b7-161">เมื่อเกิดสิ่งผิดปกติขึ้น ซึ่งโดยปกติจะเกิดเนื่องจาก Power BI ไม่สามารถลงชื่อเข้าใช้แหล่งข้อมูล หรือถ้าชุดข้อมูลเชื่อมต่อกับแหล่งข้อมูลภายในองค์กร เกตเวย์จะออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="178b7-161">When things go wrong, it’s usually because Power BI can’t sign into data sources, or if the dataset connects to an on-premises data source, the gateway is offline.</span></span> <span data-ttu-id="178b7-162">ตรวจสอบให้แน่ใจว่า Power BI สามารถลงชื่อเข้าใช้แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="178b7-162">Make sure Power BI can sign into data sources.</span></span> <span data-ttu-id="178b7-163">ถ้ามีการเปลี่ยนแปลงรหัสผ่านที่คุณลงชื่อเพื่อเข้าใช้แหล่งข้อมูล หรือ Power BI ได้รับการให้ออกจากแหล่งข้อมูล กรุณาลองลงชื่อเข้าใช้แหล่งข้อมูลของคุณอีกครั้งในข้อมูลประจำตัวของแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="178b7-163">If a password you use to sign into a data source changes, or Power BI gets signed out from a data source, be sure to try signing into your data sources again in Data Source Credentials.</span></span>

<span data-ttu-id="178b7-164">โปรดแน่ใจว่าคุณออกจาก **ส่งอีเมล์แจ้งเตือนเมื่อการรีเฟรชล้มเหลวให้ฉันตรวจสอบ**</span><span class="sxs-lookup"><span data-stu-id="178b7-164">Be sure to leave the **Send refresh failure notification email to me checked**.</span></span> <span data-ttu-id="178b7-165">คุณต้องทราบทันทีว่าการรีเฟรชตามกำหนดการล้มเหลวหรือไม่</span><span class="sxs-lookup"><span data-stu-id="178b7-165">You’ll want to know right away if a scheduled refresh fails.</span></span>

## <a name="important-notes"></a><span data-ttu-id="178b7-166">หมายเหตุสำคัญ</span><span class="sxs-lookup"><span data-stu-id="178b7-166">Important notes</span></span>

<span data-ttu-id="178b7-167">การรีเฟรชไม่ได้รับการสนับสนุนสำหรับฟีด OData ที่เชื่อมต่อ และคิวรีจาก Power Pivot</span><span class="sxs-lookup"><span data-stu-id="178b7-167">Refresh is not supported for OData feeds connected to and queried from Power Pivot.</span></span> <span data-ttu-id="178b7-168">เมื่อใช้ฟีด OData เป็นแหล่งข้อมูล ให้ใช้ Power Query</span><span class="sxs-lookup"><span data-stu-id="178b7-168">When using an OData feed as a data source, use Power Query.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="178b7-169">แนวทางการแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="178b7-169">Troubleshooting</span></span>

<span data-ttu-id="178b7-170">การรีเฟรชข้อมูลอาจไม่เป็นไปตามที่คาดไว้ในบางครั้ง</span><span class="sxs-lookup"><span data-stu-id="178b7-170">Sometimes refreshing data may not go as expected.</span></span> <span data-ttu-id="178b7-171">โดยทั่วไปแล้วเป็นปัญหาที่เกี่ยวข้องกับเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="178b7-171">Typically this is an issue connected with a gateway.</span></span> <span data-ttu-id="178b7-172">โปรดดูที่บทความแก้ไขปัญหาเกตเวย์สำหรับเครื่องมือและปัญหาที่ทราบแล้ว</span><span class="sxs-lookup"><span data-stu-id="178b7-172">Take a look at the gateway troubleshooting articles for tools and known issues:</span></span>

- [<span data-ttu-id="178b7-173">การแก้ไขปัญหา เกตเวย์ข้อมูลในองค์กร</span><span class="sxs-lookup"><span data-stu-id="178b7-173">Troubleshooting the On-premises data gateway</span></span>](service-gateway-onprem-tshoot.md)
- [<span data-ttu-id="178b7-174">แก้ไขปัญหาเกตเวย์ Power BI - ส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="178b7-174">Troubleshooting the Power BI Gateway - Personal</span></span>](service-admin-troubleshooting-power-bi-personal-gateway.md)

<span data-ttu-id="178b7-175">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="178b7-175">More questions?</span></span> [<span data-ttu-id="178b7-176">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="178b7-176">Try the Power BI Community</span></span>](https://community.powerbi.com/)
