---
title: แก้ไขตัวแปร SAP ในบริการ Power BI
description: Azure และ Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: conceptual
ms.date: 11/12/2019
LocalizationGroup: Data from databases
ms.openlocfilehash: 179e8740bed71d3d295cfc2fe5f103744e9dbd07
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96402742"
---
# <a name="edit-sap-variables-in-the-power-bi-service"></a><span data-ttu-id="d3c94-103">แก้ไขตัวแปร SAP ในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="d3c94-103">Edit SAP variables in the Power BI service</span></span>

<span data-ttu-id="d3c94-104">เมื่อคุณใช้ SAP Business Warehouse หรือ SAP HANA กับ DirectQuery ในขณะนี้ผู้เขียนรายงานสามารถอนุญาตให้ผู้ใช้ปลายทางแก้ไขตัวแปร SAP ใน **บริการ Power BI** สำหรับพื้นที่ทำงานแบบพรีเมียมและที่ใช้งานร่วมกันได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="d3c94-104">When using SAP Business Warehouse or SAP HANA with DirectQuery, report authors can now allow end users to edit SAP variables in the **Power BI Service** for Premium and shared workspaces.</span></span> <span data-ttu-id="d3c94-105">โปรดทราบว่าคุณลักษณะนี้ไม่สามารถใช้งานกับรายงานในแท็บ แชร์กับฉัน ของ พื้นที่ทำงานของฉัน และแอปที่สร้างจากพื้นที่ทำงาน V1 ได้</span><span class="sxs-lookup"><span data-stu-id="d3c94-105">Note that this feature does NOT work for reports in the Shared with me tab of My Workspace and Apps created from V1 Workspaces.</span></span> 

![แก้ไขกล่องโต้ตอบตัวแปร](media/service-edit-sap-variables/sap-edit-variables-dialog.png)

<span data-ttu-id="d3c94-107">เอกสารนี้อธิบายข้อกำหนดสำหรับการแก้ไขตัวแปรใน Power BI วิธีการเปิดใช้งานคุณลักษณะนี้ และตำแหน่งที่จะแก้ไขตัวแปรในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="d3c94-107">This document describes the requirements for editing variables in Power BI, how to enable this feature, and where to edit variables in the Power BI service.</span></span>

## <a name="requirements-for-sap-edit-variables"></a><span data-ttu-id="d3c94-108">ข้อกำหนดสำหรับตัวแปรแก้ไข SAP</span><span class="sxs-lookup"><span data-stu-id="d3c94-108">Requirements for SAP edit variables</span></span>

<span data-ttu-id="d3c94-109">มีข้อกำหนดบางอย่างสำหรับการใช้คุณลักษณะตัวแปรแก้ไขของ SAP</span><span class="sxs-lookup"><span data-stu-id="d3c94-109">There are a few requirements for using the SAP edit variables feature.</span></span> <span data-ttu-id="d3c94-110">รายการต่อไปนี้แสดงข้อกำหนดเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="d3c94-110">The following list describes these requirements.</span></span>

<span data-ttu-id="d3c94-111">**จำเป็นต้องมีประสบการณ์การใช้งานตัวกรองใหม่** – คุณต้องมี [ประสบการณ์ตัวกรองใหม่](../create-reports/power-bi-report-filter.md)ที่เปิดใช้งานสำหรับรายงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="d3c94-111">**New Filter Experience required** – you must have the [new filter experience](../create-reports/power-bi-report-filter.md) enabled for your report.</span></span> <span data-ttu-id="d3c94-112">นี่คือวิธีที่คุณสามารถเปิดใช้งานสำหรับรายงานของคุณใน Power BI Desktop:</span><span class="sxs-lookup"><span data-stu-id="d3c94-112">Here's how you can enable it for your report in Power BI Desktop:</span></span>
- <span data-ttu-id="d3c94-113">ใน Power BI Desktop เลือกตัวเลือก **ไฟล์** > **และตัวเลือก** > **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="d3c94-113">In Power BI Desktop, select **File** > **Options and Settings** > **Options**</span></span>
- <span data-ttu-id="d3c94-114">ในบานหน้าต่างนำทาง ภายใต้ **ไฟล์ปัจจุบัน** ให้เลือก **การตั้งค่ารายงาน**</span><span class="sxs-lookup"><span data-stu-id="d3c94-114">In the nav pane, under **Current file**, select **Report settings**.</span></span>
- <span data-ttu-id="d3c94-115">ภายใต้ **ประสบการณ์การกรอง** ให้เลือก **เปิดใช้งานบานหน้าต่างตัวกรองที่อัปเดตแล้ว**</span><span class="sxs-lookup"><span data-stu-id="d3c94-115">Under **Filtering experience**, select **Enable the updated filter pane**.</span></span>

<span data-ttu-id="d3c94-116">**จำเป็นต้องมีการเชื่อมต่อ DirectQuery** – คุณต้องเชื่อมต่อกับแหล่งข้อมูล SAP โดยใช้ DirectQuery</span><span class="sxs-lookup"><span data-stu-id="d3c94-116">**DirectQuery connections required** – you must be connecting to the SAP data source using DirectQuery.</span></span> <span data-ttu-id="d3c94-117">การเชื่อมต่อการนำเข้าไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="d3c94-117">Import connections aren't supported.</span></span>

<span data-ttu-id="d3c94-118">**จำเป็นต้องตั้งค่า SSO** – เพื่อให้คุณลักษณะนี้ใช้งานได้ ต้องกำหนดค่าการลงชื่อเข้าระบบครั้งเดียว (SSO)</span><span class="sxs-lookup"><span data-stu-id="d3c94-118">**SSO set-up required** – for this feature to work, single sign-on (SSO) must be configured.</span></span> <span data-ttu-id="d3c94-119">ดู[ภาพรวมของการลงชื่อเข้าใช้ครั้งเดียว (SSO)](service-gateway-sso-overview.md) สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d3c94-119">See [overview of single sign-on (SSO)](service-gateway-sso-overview.md) for more information.</span></span>

<span data-ttu-id="d3c94-120">**จำเป็นต้องมีเกตเวย์บิตใหม่** - ดาวน์โหลดเกตเวย์ล่าสุดและอัปเดตเกตเวย์ที่มีอยู่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d3c94-120">**New Gateway bits required** - Download latest gateway and update your existing gateway.</span></span> <span data-ttu-id="d3c94-121">ดู[เกตเวย์บริการ](service-gateway-onprem.md)สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d3c94-121">See [service gateway](service-gateway-onprem.md) for more information.</span></span>

<span data-ttu-id="d3c94-122">**หลายมิติสำหรับ SAP HANA เท่านั้น** - สำหรับ SAP HANA, คุณสมบัติตัวแปรแก้ไข SAP จะทำงานร่วมกับแบบจำลองหลายมิติเท่านั้นและไม่ทำงานกับแหล่งข้อมูลเชิงสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="d3c94-122">**Multidimensional only for SAP HANA** – for SAP HANA, the SAP edit variables feature only works with multidimensional models and doesn't work on relational sources.</span></span>

<span data-ttu-id="d3c94-123">**ไม่ได้รับการสนับสนุนในบริการคลาวด์สาธารณะ** – ขณะนี้ Power Query ออนไลน์ไม่สามารถใช้งานได้ในบริการคลาวด์สาธารณะ ดังนั้นคุณลักษณะนี้ยังไม่ได้รับการสนับสนุนในบริการคลาวด์สาธารณะ</span><span class="sxs-lookup"><span data-stu-id="d3c94-123">**Not supported in Sovereign clouds** – Currently Power Query Online isn't available in Sovereign clouds; therefore, this feature is also not supported in Sovereign clouds.</span></span>

## <a name="how-to-enable-the-feature"></a><span data-ttu-id="d3c94-124">วิธีการเปิดใช้งานคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="d3c94-124">How to enable the feature</span></span>

<span data-ttu-id="d3c94-125">เมื่อต้องการเปิดใช้งานคุณลักษณะ **ตัวแปรแก้ไข SAP** ใน Power BI Desktop เชื่อมต่อกับแหล่งข้อมูล SAP HANA หรือ SAP BW</span><span class="sxs-lookup"><span data-stu-id="d3c94-125">To enable the **SAP edit variables** feature, in Power BI Desktop connect to an SAP HANA or SAP BW data source.</span></span> <span data-ttu-id="d3c94-126">จากนั้นไปที่ **ไฟล์ > ตัวเลือกและการตั้งค่า > ตัวเลือก** จากนั้นในส่วนไฟล์ปัจจุบันในบานหน้าต่างด้านซ้าย ให้เลือก **DirectQuery**</span><span class="sxs-lookup"><span data-stu-id="d3c94-126">Then go to **File > Options and settings > Options** and then, in the Current File section in the left pane, select **DirectQuery**.</span></span> <span data-ttu-id="d3c94-127">เมื่อคุณเลือกตัวเลือกนั้น ในบานหน้าต่างด้านขวาคุณจะเห็นตัวเลือก DirectQuery และช่องทำเครื่องหมายที่คุณสามารถ **อนุญาตให้ผู้ใช้ปลายทางเปลี่ยนตัวแปร SAP ในรายงาน** ดังที่แสดงในภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d3c94-127">When you select that, in the right pane you see DirectQuery options, and a checkbox where you can **Allow end users to change SAP variables in the report**, as shown in the following image.</span></span>

![ตัวเลือก DirectQuery](media/service-edit-sap-variables/sap-preview-setting-in-desktop.png)

## <a name="use-sap-edit-variables-in-power-bi-desktop"></a><span data-ttu-id="d3c94-129">ใช้ตัวแปรแก้ไข SAP ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d3c94-129">Use SAP edit variables in Power BI Desktop</span></span>

<span data-ttu-id="d3c94-130">เมื่อใช้ตัวแปรแก้ไข SAP ใน Power BI Desktop คุณสามารถแก้ไขตัวแปรได้โดยการเลือกลิงก์แก้ไขตัวแปรจากเมนู **แก้ไขคิวรี** ในริบบอน</span><span class="sxs-lookup"><span data-stu-id="d3c94-130">When using SAP edit variables in Power BI Desktop, you can edit the variables by selecting the Edit variables link from **Edit Queries** menu in the ribbon.</span></span> <span data-ttu-id="d3c94-131">จากที่นี่ หน้าต่างกล่องโต้ตอบต่อไปนี้ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="d3c94-131">From there, the following dialog appears.</span></span> <span data-ttu-id="d3c94-132">คุณลักษณะนี้มีให้ใช้งานใน Power BI Desktop ชั่วขณะ</span><span class="sxs-lookup"><span data-stu-id="d3c94-132">This feature has been available in Power BI Desktop for a while.</span></span> <span data-ttu-id="d3c94-133">ผู้สร้างรายงานสามารถเลือกตัวแปรสำหรับรายงานโดยใช้กล่องโต้ตอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d3c94-133">Report creators can select variables for the report using the following dialog.</span></span>

![เพิ่มรายการ](media/service-edit-sap-variables/sap-variables-add-items.png)

## <a name="use-sap-edit-variables-in-the-service"></a><span data-ttu-id="d3c94-135">ใช้ตัวแปรแก้ไข SAP ในบริการ</span><span class="sxs-lookup"><span data-stu-id="d3c94-135">Use SAP edit variables in the service</span></span>

<span data-ttu-id="d3c94-136">เมื่อรายงานถูกเผยแพร่ไปยังบริการของ Power BI ผู้ใช้สามารถดูลิงก์ **แก้ไขตัวแปร** ในบานหน้าต่างตัวกรองใหม่</span><span class="sxs-lookup"><span data-stu-id="d3c94-136">Once the report is published to the Power BI service, users can see the **Edit variables** link in the new Filter pane.</span></span> <span data-ttu-id="d3c94-137">ถ้าคุณกำลังเผยแพร่รายงานเป็นครั้งแรก อาจใช้เวลาสูงสุด 5 นาทีก่อนที่ลิงก์แก้ไขตัวแปรจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="d3c94-137">If you're publishing the report for the first time, it may take up to 5 minutes before the Edit variable link appears.</span></span> <span data-ttu-id="d3c94-138">ถ้าลิงก์ไม่ปรากฏขึ้น คุณจะต้องรีเฟรชชุดข้อมูลด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d3c94-138">If the link hasn't appeared, you will need to manually refresh the dataset.</span></span>
<span data-ttu-id="d3c94-139">คุณสามารถทำได้โดย:</span><span class="sxs-lookup"><span data-stu-id="d3c94-139">You can do so by:</span></span>

1. <span data-ttu-id="d3c94-140">ในบริการของ Power BI ให้เลือกแท็บ **ชุดข้อมูล** ในรายการเนื้อหาสำหรับพื้นที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="d3c94-140">In the Power BI service, select the **Datasets** tab in the content list for a workspace.</span></span>

2. <span data-ttu-id="d3c94-141">ค้นหาชุดข้อมูลที่คุณจำเป็นต้องรีเฟรชและเลือกไอคอน **รีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="d3c94-141">Find the dataset you need to refresh, and select the **Refresh** icon.</span></span>

    ![แก้ไขตัวแปร](media/service-edit-sap-variables/sap-edit-variables-link.png)

3. <span data-ttu-id="d3c94-143">การเลือกลิงก์แก้ไขตัวแปรจะเปิดกล่องโต้ตอบ **แก้ไขตัวแปร** ซึ่งผู้ใช้สามารถแทนที่ตัวแปรได้</span><span class="sxs-lookup"><span data-stu-id="d3c94-143">Selecting the Edit variables link brings up the **Edit variables** dialog, where users can override variables.</span></span> <span data-ttu-id="d3c94-144">การเลือกปุ่ม **รีเซ็ต** จะรีเซ็ตตัวแปรเป็นค่าเดิมที่ปรากฏขึ้นเมื่อเปิดกล่องโต้ตอบนี้</span><span class="sxs-lookup"><span data-stu-id="d3c94-144">Selecting the **Reset** button resets the variables to the original values that appeared when this dialog was opened.</span></span>

    ![แก้ไขกล่องโต้ตอบตัวแปร](media/service-edit-sap-variables/sap-edit-variables-dialog.png)

4. <span data-ttu-id="d3c94-146">การเปลี่ยนแปลงใดๆ ในกล่องโต้ตอบ **แก้ไขตัวแปร** ยังคงอยู่เฉพาะสำหรับผู้ใช้รายนี้เท่านั้น (คล้ายกับลักษณะการทำงานที่มีอยู่อื่นๆ ใน Power BI)</span><span class="sxs-lookup"><span data-stu-id="d3c94-146">Any changes in the **Edit variables** dialog persist only for this user (similar to other persistence behaviors in Power BI).</span></span> <span data-ttu-id="d3c94-147">การเลือก **รีเซ็ตเป็นค่าเริ่มต้น** ที่แสดงในรูปต่อไปนี้จะรีเซ็ตค่ารายงานให้เป็นสถานะเดิมของผู้สร้างรายงาน รวมถึงตัวแปร</span><span class="sxs-lookup"><span data-stu-id="d3c94-147">Selecting **Reset to default**, shown in the following image, resets the report to the report creator's original state, including the variables.</span></span>

    ![รีเซ็ตเป็นค่าเริ่มต้น](media/service-edit-sap-variables/reset-to-default.png)

<span data-ttu-id="d3c94-149">เมื่อทำงานกับรายงานที่เผยแพร่ในบริการของ Power BI ที่ใช้ SAP Hana หรือ SAP BW ด้วยคุณลักษณะ **แก้ไขตัวแปร** ที่เปิดใช้งาน เจ้าของรายงานสามารถเปลี่ยนค่าเริ่มต้นเหล่านั้นได้</span><span class="sxs-lookup"><span data-stu-id="d3c94-149">When working on a published report in the Power BI service that uses SAP HANA or SAP BW with the **Edit variables** feature enabled, the report owner can change those defaults.</span></span> <span data-ttu-id="d3c94-150">เจ้าของรายงานสามารถเปลี่ยนตัวแปรในโหมดแก้ไขและบันทึกรายงานเพื่อเปิดใช้งานการตั้งค่าเหล่านั้นเพื่อให้กลายเป็น *การตั้งค่าเริ่มต้นใหม่* สำหรับรายงานนั้น</span><span class="sxs-lookup"><span data-stu-id="d3c94-150">The owner of the report can change the variables in edit mode, and save the report to enable those settings to become the *new default settings* for that report.</span></span> <span data-ttu-id="d3c94-151">ผู้ใช้รายอื่นที่เข้าถึงรายงานหลังจากมีการเปลี่ยนแปลงโดยเจ้าของรายงานจะเห็นการตั้งค่าใหม่เหล่านั้นเป็นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d3c94-151">Any other users who access the report after such changes are made by the report owner will see those new settings as the defaults.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d3c94-152">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d3c94-152">Next steps</span></span>

<span data-ttu-id="d3c94-153">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ SAP HANA, SAP BW หรือ DirectQuery กรุณาอ่านบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d3c94-153">For more information about SAP HANA, SAP BW, or DirectQuery, read the following articles:</span></span>

- [<span data-ttu-id="d3c94-154">ใช้ SAP HANA ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d3c94-154">Use SAP HANA in Power BI Desktop</span></span>](desktop-sap-hana.md)
- [<span data-ttu-id="d3c94-155">DirectQuery และ SAP Business Warehouse (BW)</span><span class="sxs-lookup"><span data-stu-id="d3c94-155">DirectQuery and SAP Business Warehouse (BW)</span></span>](desktop-directquery-sap-bw.md)
- [<span data-ttu-id="d3c94-156">DirectQuery และ SAP HANA</span><span class="sxs-lookup"><span data-stu-id="d3c94-156">DirectQuery and SAP HANA</span></span>](desktop-directquery-sap-hana.md)
- [<span data-ttu-id="d3c94-157">การใช้ DirectQuery ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="d3c94-157">Using DirectQuery in Power BI</span></span>](desktop-directquery-about.md)
