---
title: ใช้ SAP HANA ใน Power BI
description: ใช้ SAP HANA ใน Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 01/15/2020
LocalizationGroup: Connect to data
ms.openlocfilehash: 708a4439262111954012c944a464dd8e59db8068
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96404467"
---
# <a name="connect-to-sap-hana-databases-in-power-bi"></a><span data-ttu-id="a5dd6-103">เชื่อมต่อกับฐานข้อมูลของ SAP HANA ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="a5dd6-103">Connect to SAP HANA databases in Power BI</span></span>

<span data-ttu-id="a5dd6-104">ตอนนี้คุณสามารถเข้าถึงฐานข้อมูล *SAP HANA* ได้ด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="a5dd6-104">With Power BI Desktop, you can now access *SAP HANA* databases.</span></span> <span data-ttu-id="a5dd6-105">ในการใช้ SAP HANA คุณต้องมีไดรเวอร์ SAP HANA ODBC ติดตั้งอยู่ในคอมพิวเตอร์ไคลเอนต์ในพื้นที่เพื่อให้การเชื่อมต่อข้อมูล SAP HANA ของ Power BI Desktop ทำงานได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="a5dd6-105">To use SAP HANA, you must have the SAP HANA ODBC driver installed on the local client computer for the Power BI Desktop's SAP HANA data connection to work properly.</span></span> <span data-ttu-id="a5dd6-106">คุณสามารถดาวน์โหลดเครื่องมือ SAP HANA Client ได้จาก [เครื่องมือการพัฒนาของ SAP](https://tools.hana.ondemand.com/#hanatools) ซึ่งมีโปรแกรมควบคุม ODBC ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="a5dd6-106">You can download the SAP HANA Client tools from [SAP Development Tools](https://tools.hana.ondemand.com/#hanatools), which contains the necessary ODBC driver.</span></span> <span data-ttu-id="a5dd6-107">หรือ คุณสามารถรับได้จาก [ศูนย์ดาวน์โหลดซอฟต์แวร์ SAP](https://support.sap.com/en/my-support/software-downloads.html)</span><span class="sxs-lookup"><span data-stu-id="a5dd6-107">Or you can get it from the [SAP Software Download Center](https://support.sap.com/en/my-support/software-downloads.html).</span></span> <span data-ttu-id="a5dd6-108">ในพอร์ทัลซอฟต์แวร์ ให้ค้นหา *SAP HANA CLIENT* สำหรับคอมพิวเตอร์ที่ใช้ Windows</span><span class="sxs-lookup"><span data-stu-id="a5dd6-108">In the Software portal, search for the *SAP HANA CLIENT* for Windows computers.</span></span> <span data-ttu-id="a5dd6-109">เนื่องจากศูนย์ดาวน์โหลดซอฟต์แวร์ SAP นั้นมีการเปลี่ยนแปลงโครงสร้างบ่อยครั้ง คำแนะนำการนำทางที่เฉพาะเจาะจงมากกว่านี้ในเว็บไซต์ดังกล่าวจึงไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a5dd6-109">Since the SAP Software Download Center changes its structure frequently, more specific guidance for navigating that site isn't available.</span></span>

<span data-ttu-id="a5dd6-110">ในการเชื่อมต่อกับฐานข้อมูล SAP HANA ให้เลือก **รับข้อมูล** เลือก **ฐานข้อมูล** > **ฐานข้อมูล SAP HANA** จากนั้นเลือก **เชื่อมต่อ**:</span><span class="sxs-lookup"><span data-stu-id="a5dd6-110">To connect to a SAP HANA database, select **Get Data**, choose **Database** > **SAP HANA Database**, and then select **Connect**:</span></span>

![ฐานข้อมูล SAP HANA กล่องโต้ตอบรับข้อมูล Power BI Desktop](media/desktop-sap-hana/sap-hana-1.png)

<span data-ttu-id="a5dd6-112">เมื่อคุณเชื่อมต่อกับฐานข้อมูล SAP HANA ให้ระบุชื่อเซิร์ฟเวอร์</span><span class="sxs-lookup"><span data-stu-id="a5dd6-112">When you connect to a SAP HANA database, specify the server name.</span></span> <span data-ttu-id="a5dd6-113">จากนั้นจากดรอปดาวน์และกล่องป้อนข้อมูล ให้ระบุพอร์ต</span><span class="sxs-lookup"><span data-stu-id="a5dd6-113">Then from the dropdown and input box, specify the port.</span></span>

<span data-ttu-id="a5dd6-114">สำหรับรุ่นเผยแพร่นี้ SAP HANA ในโหมด [DirectQuery](desktop-directquery-sap-hana.md) ได้รับการสนับสนุนใน Power BI Desktop และบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="a5dd6-114">In this release, SAP HANA in [DirectQuery](desktop-directquery-sap-hana.md) mode is supported in Power BI Desktop and the Power BI service.</span></span> <span data-ttu-id="a5dd6-115">คุณสามารถเผยแพร่และอัปโหลดรายงานที่ใช้ SAP HANA ในโหมด DirectQuery ไปยังบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="a5dd6-115">You can publish and upload reports that use SAP HANA in DirectQuery mode to the Power BI service.</span></span> <span data-ttu-id="a5dd6-116">คุณยังสามารถเผยแพร่และอัปโหลดรายงานไปยังบริการ Power BI เมื่อไม่ได้ใช้ SAP HANA ในโหมด DirectQuery ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="a5dd6-116">You can also publish and upload reports to the Power BI Service when not using SAP HANA in DirectQuery mode.</span></span>

## <a name="supported-features-for-sap-hana"></a><span data-ttu-id="a5dd6-117">ฟีเจอร์ที่ได้รับการสนับสนุนสำหรับ SAP HANA</span><span class="sxs-lookup"><span data-stu-id="a5dd6-117">Supported features for SAP HANA</span></span>

<span data-ttu-id="a5dd6-118">รุ่นนี้มีความสามารถสำหรับ SAP HANA มากมาย ดังที่แสดงในรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a5dd6-118">This release has many capabilities for SAP HANA, as shown in the following list:</span></span>

* <span data-ttu-id="a5dd6-119">ตัวเชื่อมต่อ Power BI ของ SAP HANA ใช้ไดร์ฟเวอร์ SAP ODBC เพื่อประสบการณ์การใช้งานที่ดีที่สุดของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="a5dd6-119">The Power BI connector for SAP HANA uses the SAP ODBC driver to provide the best user experience.</span></span>

* <span data-ttu-id="a5dd6-120">SAP HANA สนับสนุนทั้งโหมด DirectQuery และตัวเลือกการนำเข้าข้อมูลต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="a5dd6-120">SAP HANA supports both DirectQuery and Import options.</span></span>

* <span data-ttu-id="a5dd6-121">Power BI สนับสนุนโมเดลข้อมูล HANA เช่น มุมมองการวิเคราะห์และการคำนวณ และมีตัวนำทางที่มีประสิทธิภาพมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="a5dd6-121">Power BI supports HANA information models, such as Analytic and Calculation Views, and has optimized navigation.</span></span>

* <span data-ttu-id="a5dd6-122">ด้วย SAP HANA คุณยังสามารถใช้ฟีเจอร์ SQL โดยตรงเพื่อเชื่อมต่อตารางแถวและคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="a5dd6-122">With SAP HANA, you can also use the direct SQL feature to connect to Row and Column Tables.</span></span>

* <span data-ttu-id="a5dd6-123">Power BI ประกอบด้วยการนำทางที่มีประสิทธิภาพสูงสุดสำหรับโมเดล HANA</span><span class="sxs-lookup"><span data-stu-id="a5dd6-123">Power BI includes Optimized Navigation for HANA Models.</span></span>

* <span data-ttu-id="a5dd6-124">Power BI สนับสนุนตัวแปรต่าง ๆ ของ SAP HANA และพารามิเตอร์ที่นำเข้ามา</span><span class="sxs-lookup"><span data-stu-id="a5dd6-124">Power BI supports SAP HANA Variables and Input parameters.</span></span>

* <span data-ttu-id="a5dd6-125">Power BI สนับสนุนมุมมองการคำนวณตามคอนเทนเนอร์ HDI</span><span class="sxs-lookup"><span data-stu-id="a5dd6-125">Power BI supports HDI-container-based Calculation Views.</span></span>

  * <span data-ttu-id="a5dd6-126">การสนับสนุนมุมมองการคำนวณตามคอนเทนเนอร์ HDI ในตัวอย่างสาธารณะในการเปิดตัว Power BI Desktop เมื่อเดือนสิงหาคม 2019</span><span class="sxs-lookup"><span data-stu-id="a5dd6-126">Support for HDI-container-based Calculation Views is in public preview in the August 2019 release of Power BI Desktop.</span></span> <span data-ttu-id="a5dd6-127">หากต้องการเข้าถึงมุมมองการคำนวณตามคอนเนทเนอร์ HDI ใน Power BI ของคุณ คุณต้องตรวจสอบให้แน่ใจว่าผู้ใช้ฐานข้อมูล HANA ที่คุณใช้งานกับ Power BI มีสิทธิ์ในการเข้าถึงคอนเทนเนอร์รันไทม์ HDI ที่บันทึกมุมมองที่คุณต้องการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="a5dd6-127">To access your HDI-container-based Calculation Views in Power BI, ensure that the HANA database users you use with Power BI have permission to access the HDI runtime container that stores the views you want to access.</span></span> <span data-ttu-id="a5dd6-128">เพื่อให้สิทธิ์การเข้าถึงนี้ ให้สร้างบทบาทที่อนุญาตให้เข้าถึงคอนเทนเนอร์ HDI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a5dd6-128">To grant this access, create a Role that allows access to your HDI container.</span></span> <span data-ttu-id="a5dd6-129">จากนั้นมอบหมายบทบาทให้กับผู้ใช้ฐานข้อมูล HANA ที่คุณจะใช้กับ Power BI</span><span class="sxs-lookup"><span data-stu-id="a5dd6-129">Then assign the role to the HANA database user you'll use with Power BI.</span></span> <span data-ttu-id="a5dd6-130">(ผู้ใช้รายนี้ต้องมีสิทธิ์ในการอ่านจากตารางของระบบในสคีมา \_SYS\_BI ตามปกติ) ดูคำแนะนำต่าง ๆ เกี่ยวกับวิธีการสร้างและกำหนดบทบาทฐานข้อมูลอย่างละเอียดในเอกสาร SAP ทางการ</span><span class="sxs-lookup"><span data-stu-id="a5dd6-130">(This user must also have permission to read from the system tables in the \_SYS\_BI schema, as usual.) Consult the official SAP documentation for detailed instructions on how to create and assign database roles.</span></span> <span data-ttu-id="a5dd6-131">[บล็อกโพสต์](https://blogs.sap.com/2018/01/24/the-easy-way-to-make-your-hdi-container-accessible-to-a-classic-database-user/)ใน SAP นี้อาจเป็นจุดเริ่มต้นที่ดี</span><span class="sxs-lookup"><span data-stu-id="a5dd6-131">[This SAP blog post](https://blogs.sap.com/2018/01/24/the-easy-way-to-make-your-hdi-container-accessible-to-a-classic-database-user/) may be a good place to start.</span></span>

  * <span data-ttu-id="a5dd6-132">มีข้อจำกัดบางอย่างในปัจจุบันนี้สำหรับตัวแปร HANA ที่ติดตั้งมากับมุมมองการคำนวณตาม HDI</span><span class="sxs-lookup"><span data-stu-id="a5dd6-132">There are currently some limitations for HANA variables attached to HDI-based Calculation Views.</span></span> <span data-ttu-id="a5dd6-133">ข้อจำกัดเหล่านี้เป็นเพราะข้อผิดพลาดในด้าน HANA</span><span class="sxs-lookup"><span data-stu-id="a5dd6-133">These limitations are because of errors on the HANA side.</span></span>
  
    <span data-ttu-id="a5dd6-134">ข้อจำกัดแรกคือเป็นไปไม่ได้ที่จะใช้ตัวแปร HANA กับคอลัมน์ที่แชร์จากมุมมองการคำนวณตามคอนเทนเนอร์ HDI ได้</span><span class="sxs-lookup"><span data-stu-id="a5dd6-134">First, it isn't possible to apply a HANA variable to a shared column of an HDI-container-based Calculation View.</span></span> <span data-ttu-id="a5dd6-135">เพื่อแก้ไขข้อจำกัดนี้ ให้อัปเกรดเป็น HANA 2 เวอร์ชัน 37.02 ขึ้นไป หรือ HANA 2 เวอร์ชัน 42 ขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="a5dd6-135">To fix this limitation, upgrade to HANA 2 version 37.02 and onwards or to HANA 2 version 42 and onwards.</span></span> <span data-ttu-id="a5dd6-136">ข้อจำกัดที่สองคือค่าเริ่มต้นหลายรายการสำหรับตัวแปรและพารามิเตอร์ปัจจุบันไม่สามารถแสดงใน Power BI UI ได้</span><span class="sxs-lookup"><span data-stu-id="a5dd6-136">Second, multi-entry default values for variables and parameters currently don't show up in the Power BI UI.</span></span> <span data-ttu-id="a5dd6-137">ข้อผิดพลาดใน SAP HANA ทำให้เกิดข้อจำกัดนี้ แต่ SAP ยังไม่ได้ประกาศการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="a5dd6-137">An error in SAP HANA causes this limitation, but SAP hasn't announced a fix yet.</span></span>

## <a name="limitations-of-sap-hana"></a><span data-ttu-id="a5dd6-138">ขีดจำกัดของ SAP HANA</span><span class="sxs-lookup"><span data-stu-id="a5dd6-138">Limitations of SAP HANA</span></span>

<span data-ttu-id="a5dd6-139">ในการใช้ SAP HANA นั้นมีข้อจำกัดบางประการตามที่แสดงไว้ด้านล่าง:</span><span class="sxs-lookup"><span data-stu-id="a5dd6-139">There are also a few limitations to using SAP HANA, shown below:</span></span>

* <span data-ttu-id="a5dd6-140">สตริง NVARCHAR จะถูกตัดทอนให้อยู่ที่ความยาวสูงสุด 4000 ตัวอักขระ Unicode</span><span class="sxs-lookup"><span data-stu-id="a5dd6-140">NVARCHAR strings are truncated to a maximum length of 4000 Unicode characters.</span></span>
* <span data-ttu-id="a5dd6-141">ไม่สนับสนุน SMALLDECIMAL</span><span class="sxs-lookup"><span data-stu-id="a5dd6-141">SMALLDECIMAL isn't supported.</span></span>
* <span data-ttu-id="a5dd6-142">ไม่สนับสนุน VARBINARY</span><span class="sxs-lookup"><span data-stu-id="a5dd6-142">VARBINARY isn't supported.</span></span>
* <span data-ttu-id="a5dd6-143">วันที่ใช้งานได้อยู่ระหว่าง 1899/12/30 และ 9999/12/31</span><span class="sxs-lookup"><span data-stu-id="a5dd6-143">Valid Dates are between 1899/12/30 and 9999/12/31.</span></span>
* <span data-ttu-id="a5dd6-144">ในขณะนี้ระบบไม่รองรับการรีเฟรช SAP Hana ด้วย SSO สำหรับสมุดงาน Excel ที่รีเฟรชในเวลาปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="a5dd6-144">SAP HANA refresh with SSO is currently not supported for Excel workbook refreshes at the current time.</span></span> <span data-ttu-id="a5dd6-145">หากต้องการรีเฟรชข้อมูลใน Power BI คุณสามารถใช้รายงาน Power BI กับ SAP Hana SSO ได้</span><span class="sxs-lookup"><span data-stu-id="a5dd6-145">To refresh the data in Power BI, you can use a Power BI report with SAP HANA SSO.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a5dd6-146">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="a5dd6-146">Next steps</span></span>

<span data-ttu-id="a5dd6-147">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ DirectQuery และ SAP HANA กรุณาดูที่แหล่งข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a5dd6-147">For more information about DirectQuery and SAP HANA, see the following resources:</span></span>

* [<span data-ttu-id="a5dd6-148">DirectQuery และ SAP HANA</span><span class="sxs-lookup"><span data-stu-id="a5dd6-148">DirectQuery and SAP HANA</span></span>](desktop-directquery-sap-hana.md)
* [<span data-ttu-id="a5dd6-149">ใช้ DirectQuery ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="a5dd6-149">Use DirectQuery in Power BI</span></span>](desktop-directquery-about.md)
* [<span data-ttu-id="a5dd6-150">แหล่งข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="a5dd6-150">Power BI data sources</span></span>](power-bi-data-sources.md)
* [<span data-ttu-id="a5dd6-151">เปิดใช้งานการเข้ารหัสลับสำหรับ SAP HANA</span><span class="sxs-lookup"><span data-stu-id="a5dd6-151">Enable encryption for SAP HANA</span></span>](desktop-sap-hana-encryption.md)
