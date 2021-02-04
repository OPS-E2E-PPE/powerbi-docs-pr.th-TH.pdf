---
title: รับข้อมูลจากไฟล์ Comma Separated Value (.CSV) (ใช้จุลภาคเป็นตัวคั่น)
description: เรียนรู้วิธีการรับข้อมูลจากไฟล์ CSV ลงใน Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 05/08/2019
LocalizationGroup: Data from files
ms.openlocfilehash: 01bef505d48f28df869bf2be705dcda963b3d0f9
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96403340"
---
# <a name="get-data-from-comma-separated-value-csv-files"></a><span data-ttu-id="fcc60-103">รับข้อมูลจากไฟล์ Comma Separated Value (.CSV) (ใช้จุลภาคเป็นตัวคั่น)</span><span class="sxs-lookup"><span data-stu-id="fcc60-103">Get data from Comma Separated Value (.CSV) files</span></span>
![ไอคอน C S V](media/service-comma-separated-value-files/csv_icon.png)

<span data-ttu-id="fcc60-105">ไฟล์ค่าที่ใช้จุลภาคเป็นตัวคั่นเป็นที่รู้จักกันในรูปแบบ .CSV ซึ่งเป็นไฟล์ข้อความอย่างง่ายที่มีแถวของข้อมูล โดยที่แต่ละค่าจะถูกคั่นด้วยเครื่องหมายจุลภาค</span><span class="sxs-lookup"><span data-stu-id="fcc60-105">Comma separated value files, often known as a .CSV, are simple text files with rows of data where each value is separated by a comma.</span></span> <span data-ttu-id="fcc60-106">ชนิดของไฟล์เหล่านี้อาจประกอบด้วยข้อมูลจำนวนมากภายในขนาดไฟล์ค่อนข้างเล็ก ทำให้ไฟล์เหล่านี้เป็นแหล่งข้อมูลที่เหมาะสมที่สุดสำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="fcc60-106">These types of files can contain very large amounts of data within a relatively small file size, making them an ideal data source for Power BI.</span></span> <span data-ttu-id="fcc60-107">คุณสามารถดาวน์โหลดตัวอย่างไฟล์ .CSV [ที่นี่](https://go.microsoft.com/fwlink/?LinkID=619356)</span><span class="sxs-lookup"><span data-stu-id="fcc60-107">You can download a sample .CSV file [here](https://go.microsoft.com/fwlink/?LinkID=619356).</span></span>

<span data-ttu-id="fcc60-108">ถ้าคุณมu .CSV ถึงเวลาไปที่ไซต์ Power BI ของคุณในฐานเป็นชุดข้อมูล ซึ่งคุณสามารถเริ่มการสำรวจข้อมูล สร้างแดชบอร์ดบางรายการ และแชร์ข้อมูลเชิงลึกของคุณกับผู้อื่นได้</span><span class="sxs-lookup"><span data-stu-id="fcc60-108">If you have a .CSV, it’s time to get it into your Power BI site as a dataset where you can begin exploring your data, create some dashboards, and share your insights with others.</span></span>

>[!TIP]
><span data-ttu-id="fcc60-109">องค์กรจำนวนมากส่งออกผลลัพธ์ .CSV ด้วยข้อมูลที่อัปเดตแต่ละวัน</span><span class="sxs-lookup"><span data-stu-id="fcc60-109">Many organizations output a .CSV with updated data each day.</span></span> <span data-ttu-id="fcc60-110">เมื่อต้องการตรวจสอบว่าชุดข้อมูลของคุณใน Power BI ยังคงรวมอยู่กับไฟล์ที่อัปเดตแล้วหรือไม่นั้น ตรวจสอบให้แน่ใจว่าไฟล์ถูกบันทึกไปยัง OneDrive ด้วยชื่อเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="fcc60-110">To make sure your dataset in Power BI stays in-sync with your updated file, be sure the file is saved to OneDrive with the same name.</span></span>

## <a name="where-your-file-is-saved-makes-a-difference"></a><span data-ttu-id="fcc60-111">ตำแหน่งที่คุณบันทึกไฟล์สร้างความแตกต่างได้</span><span class="sxs-lookup"><span data-stu-id="fcc60-111">Where your file is saved makes a difference</span></span>
<span data-ttu-id="fcc60-112">**ภายในเครื่อง** - ถ้าคุณบันทึกไฟล์ .CSV ลงในไดรฟ์ภายในเครื่องคอมพิวเตอร์ของคุณหรือในตำแหน่งอื่นในองค์กรของคุณ จาก Power BI คุณสามารถ *นำเข้า* ไฟล์ของคุณไปยัง Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="fcc60-112">**Local** - If you save your .CSV file to a local drive on your computer or another location in your organization, from Power BI you can *import* your file into Power BI.</span></span> <span data-ttu-id="fcc60-113">ไฟล์ของคุณจะยังคงอยู่บนไดรฟ์ในเครื่อง ดังนั้นจึงไม่มีการนำเข้าใน Power BI จริง ๆ</span><span class="sxs-lookup"><span data-stu-id="fcc60-113">Your file will actually remain on your local drive, so the whole file isn’t really imported into Power BI.</span></span> <span data-ttu-id="fcc60-114">สิ่งที่เกิดขึ้นจริง ๆ คือมีการสร้างชุดข้อมูลใหม่ใน Power BI และข้อมูลจากไฟล์ .CSV จะโหลดลงในชุดข้อมูลดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="fcc60-114">What really happens is a new dataset is created in Power BI and data from the .CSV file is loaded into the dataset.</span></span>

<span data-ttu-id="fcc60-115">**OneDrive - ธุรกิจ**– ถ้าคุณมี OneDrive for Business และคุณลงชื่อเข้าใช้ด้วยบัญชีเดียวกันกับที่คุณลงชื่อเข้าใช้ Power BI ปัจจุบัน นี่คือวิธีที่มีประสิทธิภาพที่สุดในการเก็บไฟล์ .CSV และชุดข้อมูล รายงาน และแดชบอร์ดใน Power BI ของคุณให้รวมกัน เนื่องจากทั้ง Power BI และ OneDrive อยู่ในระบบคลาวด์ Power BI จะ *เชื่อมต่อ* ไปยังไฟล์ของคุณบน OneDrive ประมาณทุกชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="fcc60-115">**OneDrive - Business** – If you have OneDrive for Business and you sign into it with the same account you sign into Power BI with, this is by-far the most effective way to keep your .CSV file and your dataset, reports, and dashboards in Power BI in-sync. Because both Power BI and OneDrive are in the cloud, Power BI *connects* to your file on OneDrive about every hour.</span></span> <span data-ttu-id="fcc60-116">ถ้าพบการเปลี่ยนแปลงใด ๆ ก็ตาม Power BI จะอัปเดต ชุดข้อมูล รายงาน และแดชบอร์โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="fcc60-116">If any changes are found, your dataset, reports, and dashboards are automatically updated in Power BI.</span></span>

<span data-ttu-id="fcc60-117">**OneDrive - ส่วนบุคคล** – ถ้าคุณบันทึกไฟล์ของคุณไปยังบัญชี OneDrive ของคุณเอง คุณจะยังได้รับประโยชน์หลายอย่างแบบเดียวกับที่คุณได้จาก OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="fcc60-117">**OneDrive - Personal** – If you save your files to your own OneDrive account, you’ll get many of the same benefits as you would with OneDrive for Business.</span></span> <span data-ttu-id="fcc60-118">ความแตกต่างที่สำคัญที่สุด คือเมื่อคุณเชื่อมต่อกับไฟล์ของคุณ (โดยใช้ รับข้อมูล > ไฟล์ > OneDrive – ส่วนบุคคล) คุณจำเป็นต้องลงชื่อเข้าใช้ OneDrive ของคุณด้วยบัญชี Microsoft ของคุณ ซึ่งโดยปกติแล้วจะแตกต่างจากที่คุณใช้ลงชื่อเข้าใช้ Power BI</span><span class="sxs-lookup"><span data-stu-id="fcc60-118">The biggest difference is when you first connect to your file (using Get Data > Files > OneDrive – Personal) you’ll need to sign in to your OneDrive with your Microsoft account, which is usually different from what you use to sign in to Power BI.</span></span> <span data-ttu-id="fcc60-119">เมื่อลงชื่อเข้าใช้ด้วย OneDrive ของคุณด้วยบัญชี Microsoft ตรวจสอบให้แน่ใจว่าได้เลือกตัวเลือก คงการลงชื่อเข้าใช้ของฉันไว้เสมอ</span><span class="sxs-lookup"><span data-stu-id="fcc60-119">When signing into your OneDrive with your Microsoft account, be sure to select the Keep me signed in option.</span></span> <span data-ttu-id="fcc60-120">ด้วยวิธีนี้ Power BI จะสามารถเชื่อมต่อกับไฟล์ของคุณประมาณทุกชั่วโมง และทำให้คุณแน่ใจว่า ชุดข้อมูลของคุณใน Power BI มีข้อมูลที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="fcc60-120">This way, Power BI will be able to connect to your file about every hour and make sure your dataset in Power BI is in-sync.</span></span>

<span data-ttu-id="fcc60-121">**SharePoint - ของไซต์ของทีม** การบันทึกไฟล์ Power BI Desktop ของคุณไปยัง SharePoint ไซต์ของทีมจะเหมือนกับการบันทึกไปยัง OneDrive for Business มาก</span><span class="sxs-lookup"><span data-stu-id="fcc60-121">**SharePoint Team-Sites** – Saving your Power BI Desktop files to SharePoint – Team Sites is much the same as saving to OneDrive for Business.</span></span> <span data-ttu-id="fcc60-122">ความแตกต่างที่สำคัญที่สุดคือ วิธีที่คุณเชื่อมต่อไปยังไฟล์จาก Power BI</span><span class="sxs-lookup"><span data-stu-id="fcc60-122">The biggest difference is how you connect to the file from Power BI.</span></span> <span data-ttu-id="fcc60-123">คุณสามารถระบุ URL หรือเชื่อมต่อไปยังโฟลเดอร์รากฐานได้</span><span class="sxs-lookup"><span data-stu-id="fcc60-123">You can specify a URL or connect to the root folder.</span></span>

## <a name="import-or-connect-to-a-csv-file"></a><span data-ttu-id="fcc60-124">นำเข้าหรือเชื่อมต่อกับไฟล์ .CSV</span><span class="sxs-lookup"><span data-stu-id="fcc60-124">Import or connect to a .CSV file</span></span>
>[!IMPORTANT]
><span data-ttu-id="fcc60-125">ขนาดไฟล์สูงสุดที่คุณสามารถนำเข้าใน Power BI ได้คือ 1 กิกะไบต์</span><span class="sxs-lookup"><span data-stu-id="fcc60-125">The maximum file size you can import into Power BI is 1 gigabyte.</span></span>

1. <span data-ttu-id="fcc60-126">ใน Power BI ในพื้นที่ตัวนำทาง คลิก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="fcc60-126">In Power BI, in the navigator pane, click **Get Data**.</span></span>
   
   ![ภาพหน้าจอของรับข้อมูลใน Power BI Desktop ที่แสดงปุ่มในบานหน้าต่างตัวนำทาง](media/service-comma-separated-value-files/csv_get_data_button.png)
2. <span data-ttu-id="fcc60-128">ใน **ไฟล์** คลิก **รับ**</span><span class="sxs-lookup"><span data-stu-id="fcc60-128">In **Files**, click **Get**.</span></span>
   
   ![ภาพหน้าจอของกล่องโต้ตอบไฟล์ ที่แสดงปุ่มรับ](media/service-comma-separated-value-files/csv_files_get.png)
3. <span data-ttu-id="fcc60-130">ค้นหาไฟล์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="fcc60-130">Find your file.</span></span>
   
   ![ภาพหน้าจอของไทล์สี่รายการเพื่อค้นหาไฟล์ของคุณ ที่แสดงการเลือกไฟล์ภายในเครื่อง, OneDrive Business, OneDrive Personal และ SharePoint](media/service-comma-separated-value-files/csv_find_your_file.png)

## <a name="next-steps"></a><span data-ttu-id="fcc60-132">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="fcc60-132">Next steps</span></span>
<span data-ttu-id="fcc60-133">**สำรวจข้อมูลของคุณ** เมื่อคุณได้รับข้อมูลจากไฟล์ของคุณลงใน Power BI แล้ว นั่นก็ถึงเวลาการสำรวจ</span><span class="sxs-lookup"><span data-stu-id="fcc60-133">**Explore your data** - Once you get data from your file into Power BI, it's time to explore.</span></span> <span data-ttu-id="fcc60-134">เพียงคลิกขวาที่ชุดข้อมูลใหม่ จากนั้นคลิก **สำรวจ**</span><span class="sxs-lookup"><span data-stu-id="fcc60-134">Just right-click the new dataset and then click **Explore**.</span></span>

<span data-ttu-id="fcc60-135">**กำหนดการรีเฟรช** ถ้าไฟล์ของคุณบันทึกลงในไดรฟ์ภายในเครื่อง คุณสามารถตั้งค่ารีเฟรชตามกำหนดการได้ เพื่อให้ชุดข้อมูลและรายงานใน Power BI ของคุณเป็นเวอร์ชันล่าสุดเสมอ</span><span class="sxs-lookup"><span data-stu-id="fcc60-135">**Schedule refresh** - If your file is saved to a local drive, you can setup scheduled refresh so your dataset and reports in Power BI stay up-to-date.</span></span> <span data-ttu-id="fcc60-136">เมื่อต้องการเรียนรู้เพิ่มเติม ดู[รีเฟรชข้อมูลใน Power BI](refresh-data.md)</span><span class="sxs-lookup"><span data-stu-id="fcc60-136">To learn more, see [Data refresh in Power BI](refresh-data.md).</span></span> <span data-ttu-id="fcc60-137">ถ้าไฟล์ของคุณถูกบันทึกไปยัง OneDrive, Power BI จะรวมข้อมูลกับ OneDrive ประมาณทุกชั่วโมงโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="fcc60-137">If your file is saved to OneDrive, Power BI will automatically synchronize with it about every hour.</span></span>

