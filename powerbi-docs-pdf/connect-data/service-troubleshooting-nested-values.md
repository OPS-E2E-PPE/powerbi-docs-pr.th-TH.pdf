---
title: การแก้ไขปัญหาค่าที่ซ้อนกันกลับคืนเป็นข้อความในบริการ Power BI
description: เรียนรู้เกี่ยวกับวิธีแก้ไขปัญหาค่าที่ซ้อนกันที่ถูกแปลงเป็นสตริเมื่อใช้การตั้งค่าความเป็นส่วนตัวของแหล่งข้อมูลที่ไม่เหมาะสม
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: troubleshooting
ms.date: 6/4/2019
LocalizationGroup: Reports
ms.openlocfilehash: b34f6ae838122b0b2036a953296d5032bdfe76b8
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96401385"
---
# <a name="troubleshooting-nested-values-returned-as-text-in-power-bi-service"></a><span data-ttu-id="94b03-103">การแก้ไขปัญหาค่าที่ซ้อนกันกลับคืนเป็นข้อความในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="94b03-103">Troubleshooting Nested Values returned as Text in Power BI Service</span></span>

## <a name="cause"></a><span data-ttu-id="94b03-104">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="94b03-104">Cause</span></span>

<span data-ttu-id="94b03-105">ในอดีต มีกรณีที่รายงาน Power BI รีเฟรชได้เป็นอย่างดีบนเดสก์ท็อป แต่ล้มเหลวบนบริการ Power BI ที่มีข้อผิดพลาดเช่น "เราไม่สามารถแปลงค่า "[ตาราง]" เพื่อพิมพ์ตาราง"</span><span class="sxs-lookup"><span data-stu-id="94b03-105">In the past, there have been cases where a Power BI report refreshed fine in the Desktop, but failed on the Power BI service with an error like “We cannot convert the value "[Table]" to type Table”.</span></span> <span data-ttu-id="94b03-106">หนึ่งในสาเหตุของข้อผิดพลาดนี้คือว่า เมื่อไฟร์วอลล์ความเป็นส่วนตัวของข้อมูล บัฟเฟอร์แหล่งข้อมูล ค่าที่ไม่ใช่สเกลที่ซ้อนกัน (เช่น ตาราง ระเบียน รายการ และฟังก์ชัน) จะถูกแปลงเป็นค่าข้อความ (เช่น "[ตาราง]" หรือ "[ระเบียน]") โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="94b03-106">One of the causes of this error is that when the Data Privacy Firewall buffers a data source, nested non-scalar values (such as tables, records, lists, and functions) are automatically converted to text values (such as “[Table]” or “[Record]”).</span></span>

<span data-ttu-id="94b03-107">หลังจากที่บริการ Power BI สนับสนุนการตั้งค่าระดับความเป็นส่วนตัว (หรือปิดไฟร์วอลล์ทั้งหมด) คุณสามารถหลีกเลี่ยงข้อผิดพลาดดังกล่าวโดย[การกำหนดค่าการตั้งค่าความเป็นส่วนตัวของแหล่งข้อมูล](https://powerbi.microsoft.com/blog/privacy-levels-for-cloud-data-sources/)ในบริการ Power BI เป็นแบบที่ไม่ใช่ส่วนตัวได้</span><span class="sxs-lookup"><span data-stu-id="94b03-107">Now that the Power BI service supports the setting of privacy levels (or turning off the Firewall entirely), such errors can be avoided by [configuring the data source privacy settings](https://powerbi.microsoft.com/blog/privacy-levels-for-cloud-data-sources/) in the Power BI service to be non-Private.</span></span>

<span data-ttu-id="94b03-108">เริ่มต้นด้วย June Power BI เมื่อไฟร์วอลล์บัฟเฟอร์การตาราง/ระเบียน/รายการ/ฯลฯ ที่ซ้อนกันแทนการแปลงค่าดังกล่าวเป็นค่าข้อความโดยอัตโนมัติซึ่งข้อผิดพลาดต่อไปนี้จะเกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="94b03-108">Starting with June Power BI, when the Firewall buffers a nested table/record/list/etc., instead of silently converting such values to text, the following error will be produced:</span></span> 

`We cannot return a value of type Table in this context`

## <a name="effect-on-loadrefresh"></a><span data-ttu-id="94b03-109">เกิดเอฟเฟกต์บนการโหลด/การรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="94b03-109">Effect on Load/Refresh</span></span>

<span data-ttu-id="94b03-110">ในขณะที่การเปลี่ยนแปลงจะถูกผลักดันโดยการบัฟเฟอร์ไฟร์วอลล์ ผลกระทบจะขยายไปยังการโหลด/การรีเฟรชได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="94b03-110">While the change is motivated by Firewall buffering, its impact extends to Load/Refresh as well.</span></span> <span data-ttu-id="94b03-111">ในการแก้ปัญหาลักษณะการบัฟเฟอร์ไฟร์วอลล์ เรายังต้องทำการเปลี่ยนแปลงลักษณะของการโหลดตารางที่ซ้อนกัน/ระเบียน/อื่น ๆ ไปยังแบบจำลอง Power BI และแบบจำลองข้อมูล Excel ใน PQ สำหรับ Excel</span><span class="sxs-lookup"><span data-stu-id="94b03-111">In order to address the Firewall buffering behavior, we also had to change the behavior of loading nested tables/records/etc. to the Power BI Model and the Excel Data Model in PQ for Excel.</span></span> <span data-ttu-id="94b03-112">ก่อนจะโหลดตารางที่ซ้อนกัน/ระเบียน/และอื่นๆ เป็นค่าข้อความ (เช่น "[ตาราง]" หรือ "[ระเบียน]")</span><span class="sxs-lookup"><span data-stu-id="94b03-112">Before, nested tables/records/etc. would be loaded as text values (such as “[Table]” or “[Record]”).</span></span> <span data-ttu-id="94b03-113">ตอนนี้จะถูกจัดเป็นข้อผิดพลาด ซึ่งจะส่งผลให้ไม่มีค่าในตารางที่โหลดและการเพิ่มจำนวนการนับข้อผิดพลาดในการโหลดผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="94b03-113">They'll now be treated as errors, which will result in a null value in the loaded table and an error count increment in the load results.</span></span>

<span data-ttu-id="94b03-114">เนื่องจากข้อผิดพลาดเหล่านี้เกิดขึ้นในระหว่างการโหลด/รีเฟรชเท่านั้นซึ่งจะไม่ปรากฏใน Power Query Editor</span><span class="sxs-lookup"><span data-stu-id="94b03-114">Since these errors only occur during Load/Refresh, they will not appear in the Power Query Editor.</span></span>

### <a name="before"></a><span data-ttu-id="94b03-115">ก่อน</span><span class="sxs-lookup"><span data-stu-id="94b03-115">Before</span></span>

- <span data-ttu-id="94b03-116">โหลด/รีเฟรชโดยไม่มีข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="94b03-116">Load/Refresh with no errors</span></span>
- <span data-ttu-id="94b03-117">ตารางที่โหลดประกอบด้วย "[ตาราง]" "[ระเบียน]" และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="94b03-117">Loaded table contains “[Table]”, “[Record]”, etc.</span></span>
 

### <a name="after"></a><span data-ttu-id="94b03-118">หลังจาก</span><span class="sxs-lookup"><span data-stu-id="94b03-118">After</span></span>

- <span data-ttu-id="94b03-119">โหลด/รีเฟรชโดยมีข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="94b03-119">Load/Refresh with errors</span></span>
- <span data-ttu-id="94b03-120">ตารางที่โหลดประกอบด้วยค่า NULLS (แทน "[ตาราง]" "[ระเบียน]" และอื่น ๆ)</span><span class="sxs-lookup"><span data-stu-id="94b03-120">Loaded table contains NULLs (instead of “[Table]”, “[Record]”, etc.)</span></span>
 

## <a name="resolution"></a><span data-ttu-id="94b03-121">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="94b03-121">Resolution</span></span>

<span data-ttu-id="94b03-122">คุณกำลังโหลดคอลัมน์ที่ประกอบด้วยค่าไม่ใช่สเกล (เช่น ตาราง รายการ ระเบียน และอื่น ๆ) อยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="94b03-122">Are you loading a column that contains non-scalar values (for example tables, lists, records, etc.)?</span></span>
<span data-ttu-id="94b03-123">ถ้าเป็นเช่นนั้น คุณอาจสามารถกำจัดข้อผิดพลาดโดยการลบคอลัมน์ออกได้</span><span class="sxs-lookup"><span data-stu-id="94b03-123">If so, you should be able to eliminate the errors by removing the column.</span></span>
<span data-ttu-id="94b03-124">ถ้าคุณไม่สามารถลบคอลัมน์ คุณอาจสามารถจำลองลักษณะการทำงานเดิม โดยการเพิ่มคอลัมน์แบบกำหนดเอง และใช้ตรรกะดังตัวอย่างต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="94b03-124">If you cannot remove the column, you should be able to replicate the old behavior by adding a custom column and using logic like the following sample:</span></span>

`if [MyColumn] is table then "[Table]" else if [MyColumn] is record then "[Record]" else if [MyColumn] is list then "[List]" else if [MyColumn] is function then "[Function]" else [MyColumn]`

<span data-ttu-id="94b03-125">เกิดปัญหาซ้ำขึ้นใน Power BI Desktop หรือไม่ถ้าคุณตั้งค่าการตั้งค่าความเป็นส่วนตัวของแหล่งข้อมูลทั้งหมดของคุณเป็นส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="94b03-125">Does the issue repro in Power BI Desktop if you set all your data source privacy settings to Private?</span></span>
<span data-ttu-id="94b03-126">ถ้าเป็นเช่นนั้น คุณควรสามารถแก้ไขข้อผิดพลาดโดย[กำหนดค่าการตั้งค่าความเป็นส่วนตัวของแหล่งข้อมูล](https://powerbi.microsoft.com/blog/privacy-levels-for-cloud-data-sources/)ในบริการ Power BI ให้เป็นแบบที่ไม่ใช่ส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="94b03-126">If so, you should be able to resolve the error by [configuring their data source privacy settings](https://powerbi.microsoft.com/blog/privacy-levels-for-cloud-data-sources/) in the Power BI service to be non-Private.</span></span>
