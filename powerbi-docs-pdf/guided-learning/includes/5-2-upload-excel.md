---
ms.openlocfilehash: cff8e70e43496b264fd0dd549759f939bf90e33f
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2019
ms.locfileid: "61271526"
---
<span data-ttu-id="5d569-101">ในหัวข้อนี้ ก่อนอื่นเราจะมาดูวิธีที่คุณสามารถนำเข้าไฟล์เวิร์กบุ๊ก Excel ซึ่งมี**ตาราง**แบบง่ายๆ จากไดรฟ์ภายในลงใน Power BI</span><span class="sxs-lookup"><span data-stu-id="5d569-101">In this topic, we'll first take a look at how you can import an Excel workbook file containing a simple **table** from a local drive into Power BI.</span></span> <span data-ttu-id="5d569-102">จากนั้นคุณจะได้เรียนรู้วิธีที่คุณสามารถเริ่มสำรวจข้อมูลของตารางใน Power BI ด้วยการสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="5d569-102">You'll then learn how you can begin exploring that table's data in Power BI by creating a report.</span></span>

## <a name="make-sure-your-data-is-formatted-as-a-table"></a><span data-ttu-id="5d569-103">ตรวจสอบให้แน่ใจว่าข้อมูลของคุณได้รับการจัดรูปแบบเป็นตารางแล้ว</span><span class="sxs-lookup"><span data-stu-id="5d569-103">Make sure your data is formatted as a table</span></span>
<span data-ttu-id="5d569-104">เพื่อให้ Power BI นำเข้าข้อมูลจากเวิร์กบุ๊กของคุณได้ ข้อมูลดังกล่าวต้องได้รับการ**จัดรูปแบบเป็นตาราง**</span><span class="sxs-lookup"><span data-stu-id="5d569-104">In order for Power BI to import data from your workbook, that data needs to be  **formatted as a table**.</span></span> <span data-ttu-id="5d569-105">ง่ายมากๆ</span><span class="sxs-lookup"><span data-stu-id="5d569-105">It's easy.</span></span> <span data-ttu-id="5d569-106">ใน Excel คุณสามารถเน้นช่วงของเซลล์ จากนั้นบนแท็บ **แทรก** ของ Ribbon ของ Excel ให้คลิก **ตาราง**</span><span class="sxs-lookup"><span data-stu-id="5d569-106">In Excel, you can highlight a range of cells, then on the **Insert** tab of the Excel ribbon, click **Table**.</span></span>

![](media/5-2-upload-excel/5-2_1.png)

<span data-ttu-id="5d569-107">คุณจะต้องแน่ใจว่าแต่ละคอลัมน์มีชื่อที่ดี</span><span class="sxs-lookup"><span data-stu-id="5d569-107">You'll want to make sure each column has a good name.</span></span> <span data-ttu-id="5d569-108">ซึ่งจะทำให้ง่ายต่อการค้นหาข้อมูลที่คุณต้องการเมื่อสร้างรายงานของคุณใน Power BI</span><span class="sxs-lookup"><span data-stu-id="5d569-108">It will make it easier to find the data you want when creating your reports in Power BI.</span></span>

## <a name="import-from-a-local-drive"></a><span data-ttu-id="5d569-109">นำเข้าข้อมูลจากไดรฟ์ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="5d569-109">Import from a local drive</span></span>
<span data-ttu-id="5d569-110">ไม่ว่าคุณจะเก็บไฟล์ไว้ที่ใด Power BI จะทำให้การนำเข้าเป็นเรื่องง่าย</span><span class="sxs-lookup"><span data-stu-id="5d569-110">Wherever you keep your files, Power BI makes it easy to import them.</span></span> <span data-ttu-id="5d569-111">ใน Power BI คุณสามารถใช้ **รับข้อมูล** > **ไฟล์** > **ไฟล์บนเครื่อง** เพื่อค้นหาและเลือกไฟล์ Excel ที่เราต้องการ</span><span class="sxs-lookup"><span data-stu-id="5d569-111">In Power BI, you can use **Get Data** > **Files** > **Local File**, to find and select the Excel file we want.</span></span>

![](media/5-2-upload-excel/5-2_2.png)

<span data-ttu-id="5d569-112">เมื่อนำเข้าไฟล์ลงใน Power BI แล้ว คุณสามารถเริ่มสร้างรายงานได้</span><span class="sxs-lookup"><span data-stu-id="5d569-112">Once imported into Power BI, you can begin creating reports.</span></span>

<span data-ttu-id="5d569-113">แน่นอนว่าไฟล์ของคุณจะไม่จำเป็นต้องอยู่บนไดรฟ์ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="5d569-113">Your files don't have to be on a local drive, of course.</span></span> <span data-ttu-id="5d569-114">ถ้าคุณบันทึกไฟล์ของคุณบน OneDrive หรือทีมไซต์ SharePoint ได้ก็จะดียิ่งกว่า</span><span class="sxs-lookup"><span data-stu-id="5d569-114">If you save your files on OneDrive or SharePoint Team Site, that's even better.</span></span> <span data-ttu-id="5d569-115">เราจะอธิบายรายละเอียดเพิ่มเติมเกี่ยวกับหัวข้อนี้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="5d569-115">We'll go into more details about that in a later topic.</span></span>

## <a name="start-creating-reports"></a><span data-ttu-id="5d569-116">เริ่มสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="5d569-116">Start creating reports</span></span>
<span data-ttu-id="5d569-117">เมื่อนำเข้าข้อมูลของเวิร์กบุ๊กของคุณแล้ว ชุดข้อมูลจะถูกสร้างใน Power BI</span><span class="sxs-lookup"><span data-stu-id="5d569-117">Once your workbook's data has been imported, a dataset is created in Power BI.</span></span> <span data-ttu-id="5d569-118">ซึ่งจะปรากฏขึ้นภายใต้ **ชุดข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="5d569-118">It appears under **Datasets**.</span></span> <span data-ttu-id="5d569-119">ขณะนี้คุณสามารถเริ่มสำรวจข้อมูลของคุณโดยการสร้างรายงานและแดชบอร์ด</span><span class="sxs-lookup"><span data-stu-id="5d569-119">Now you can begin exploring your data by creating reports and dashboards.</span></span> <span data-ttu-id="5d569-120">เพียงแค่คลิกบนไอคอน **เปิดเมนู** ถัดจากชุดข้อมูล จากนั้นคลิก **สำรวจ**</span><span class="sxs-lookup"><span data-stu-id="5d569-120">Just click on the **Open menu** icon next to the dataset and then click **Explore**.</span></span> <span data-ttu-id="5d569-121">พื้นที่รายงานเปล่าอันใหม่จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="5d569-121">A new blank report canvas appears.</span></span> <span data-ttu-id="5d569-122">ทางด้านขวา ภายใต้ **เขตข้อมูล** คุณจะเห็นตารางและคอลัมน์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5d569-122">Over on the right, under **Fields**, you'll see your tables and columns.</span></span> <span data-ttu-id="5d569-123">เพียงแค่เลือกเขตขอมูลที่คุณต้องการสร้างการจัดรูปแบบการแสดงข้อมูลใหม่บนผืนผ้าใบ</span><span class="sxs-lookup"><span data-stu-id="5d569-123">Just select the fields you want to create a new visualization on the canvas.</span></span>

![](media/5-2-upload-excel/5-2_3.png)

<span data-ttu-id="5d569-124">คุณสามารถเปลี่ยนชนิดของการจัดรูปแบบการแสดงข้อมูล และใช้ **ตัวกรอง** และคุณสมบัติอื่นภายใต้ **การจัดรูปแบบการแสดงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="5d569-124">You can change the type of visualization and apply **filters** and other properties under **Visualizations**.</span></span>

