---
title: เชื่อมต่อไปยังข้อมูล Azure Cost Management ใน Power BI Desktop
description: เชื่อมต่อไปยัง Azure และรับข้อมูลเชิงลึกเกี่ยวกับค่าใช้จ่ายและการใช้งาน Azure ของคุณด้วย Power BI Desktop ได้อย่างง่ายดาย
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 12/10/2020
LocalizationGroup: Connect to data
ms.openlocfilehash: 6d99e91657d0c5f0bbd1e9c665f00d16c34ba24f
ms.sourcegitcommit: 772c65b7b440ab082510bf3f64b871d19139d451
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/12/2020
ms.locfileid: "97353254"
---
# <a name="create-visuals-and-reports-with-the-azure-cost-management-connector-in-power-bi-desktop"></a><span data-ttu-id="3c511-103">สร้างวิชวลและรายงานด้วยตัวเชื่อมต่อ Azure Cost Management ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3c511-103">Create visuals and reports with the Azure Cost Management connector in Power BI Desktop</span></span>

<span data-ttu-id="3c511-104">คุณสามารถใช้ตัวเชื่อมต่อการจัดการค่าใช้จ่ายของ Azure สำหรับ Power BI Desktop เพื่อสร้างการแสดงภาพและรายงานแบบกำหนดเองที่ทรงพลังซึ่งช่วยให้คุณเข้าใจการใช้งาน Azure ของคุณได้ดียิ่งขึ้น</span><span class="sxs-lookup"><span data-stu-id="3c511-104">You can use the Azure Cost Management connector for Power BI Desktop to make powerful, customized visualizations and reports that help you better understand your Azure spend.</span></span> <span data-ttu-id="3c511-105">ตัวเชื่อมต่อ Azure Cost Management ในขณะนี้สนับสนุนลูกค้าด้วย[Microsoft Customer Agreement](https://azure.microsoft.com/pricing/purchase-options/microsoft-customer-agreement/) หรือ [Enterprise Agreement (EA)](https://azure.microsoft.com/pricing/enterprise-agreement/)</span><span class="sxs-lookup"><span data-stu-id="3c511-105">The Azure Cost Management connector currently supports customers with a [Microsoft Customer Agreement](https://azure.microsoft.com/pricing/purchase-options/microsoft-customer-agreement/) or an [Enterprise Agreement (EA)](https://azure.microsoft.com/pricing/enterprise-agreement/).</span></span>  

<span data-ttu-id="3c511-106">ตัวเชื่อมต่อ Azure Cost Management ใช้ OAuth 2.0 สำหรับการรับรองความถูกต้องกับ Azure และระบุตัวตนผู้ใช้ที่กำลังจะใช้ตัวเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="3c511-106">The Azure Cost Management connector uses OAuth 2.0 for authentication with Azure and identifies users who are going to use the connector.</span></span> <span data-ttu-id="3c511-107">โทเค็นที่สร้างขึ้นในกระบวนการนี้จะใช้ได้สำหรับช่วงเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3c511-107">Tokens generated in this process are valid for a specific period.</span></span> <span data-ttu-id="3c511-108">Power BI เก็บรักษาโทเค็นสำหรับการเข้าสู่ระบบครั้งถัดไป</span><span class="sxs-lookup"><span data-stu-id="3c511-108">Power BI preserves the token for the next login.</span></span> <span data-ttu-id="3c511-109">OAuth 2.0 เป็นมาตรฐานสำหรับกระบวนการที่อยู่เบื้องหลังเพื่อให้แน่ใจว่าการจัดการสิทธิ์เหล่านี้มีความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="3c511-109">OAuth 2.0, is a standard for the process that goes on behind the scenes to ensure the secure handling of these permissions.</span></span> <span data-ttu-id="3c511-110">หากต้องการเชื่อมต่อคุณต้องใช้บัญชี[ผู้ดูแล Enterprise](/azure/billing/billing-understand-ea-roles) สำหรับข้อตกลงขององค์กรหรือ[เจ้าของบัญชีเรียกเก็บเงิน](/azure/billing/billing-understand-mca-roles) สำหรับข้อตกลงลูกค้าของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="3c511-110">To connect, you must use an [Enterprise Administrator](/azure/billing/billing-understand-ea-roles) account for Enterprise Agreements, or a [Billing account owner](/azure/billing/billing-understand-mca-roles) for Microsoft Customer Agreements.</span></span> 

> [!NOTE]
> <span data-ttu-id="3c511-111">ตัวเชื่อมต่อนี้จะแทนที่ตัวเชื่อมต่อ [Azure Consumption Insights และ Azure Cost Management (Beta)](desktop-connect-azure-consumption-insights.md) ที่มีอยู่ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="3c511-111">This connector replaces the previously available [Azure Consumption Insights and Azure Cost Management (Beta)](desktop-connect-azure-consumption-insights.md) connectors.</span></span> <span data-ttu-id="3c511-112">รายงานใดๆ ที่สร้างขึ้นด้วยตัวเชื่อมต่อก่อนหน้านี้จะต้องได้รับการจัดรูปแบบใหม่โดยใช้การเชื่อมต่อนี้</span><span class="sxs-lookup"><span data-stu-id="3c511-112">Any reports created with the previous connector must be recreated using this connector.</span></span>

> [!NOTE]
> <span data-ttu-id="3c511-113">ตัวเชื่อมต่อ Azure Cost Management สำหรับ Power BI Desktop ไม่รองรับการเชื่อมต่อกับคลาวด์ของรัฐบาล</span><span class="sxs-lookup"><span data-stu-id="3c511-113">The Azure Cost Management connector for Power BI Desktop does not support connecting to government clouds.</span></span> 


## <a name="connect-using-azure-cost-management"></a><span data-ttu-id="3c511-114">เชื่อมต่อโดยใช้ยังการจัดการค่าใช้จ่ายของ Azure</span><span class="sxs-lookup"><span data-stu-id="3c511-114">Connect using Azure Cost Management</span></span>

<span data-ttu-id="3c511-115">ในการใช้ตัวเชื่อมต่อ **การจัดการค่าใช้จ่ายของ Azure** ใน Power BI Desktop ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3c511-115">To use the **Azure Cost Management connector** in Power BI Desktop, take the following steps:</span></span>

1.  <span data-ttu-id="3c511-116">ใน Ribbon **หน้าแรก** ให้เลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="3c511-116">In the **Home** ribbon, select **Get Data**.</span></span>
2.  <span data-ttu-id="3c511-117">เลือก **Azure** จากรายการของประเภทข้อมูล</span><span class="sxs-lookup"><span data-stu-id="3c511-117">Select **Azure** from the list of data categories.</span></span>
3.  <span data-ttu-id="3c511-118">เลือก **Azure Cost Management**</span><span class="sxs-lookup"><span data-stu-id="3c511-118">Select **Azure Cost Management**.</span></span>

    ![รับข้อมูล](media/desktop-connect-azure-cost-management/azure-cost-management-00b.png)

4. <span data-ttu-id="3c511-120">ในกล่องโต้ตอบที่ปรากฏขึ้นให้ใส่ **ID โปรไฟล์การชำระเงินของคุณ\*\*\*\*ข้อตกลงของลูกค้า Microsoft** หรือ **หมาขเลขการสมัครเข้า** ของคุณสำหรับ **ข้อตกลงองค์กร (EA)**</span><span class="sxs-lookup"><span data-stu-id="3c511-120">In the dialog that appears, enter either your **Billing Profile ID** for **Microsoft Customer Agreements**, or your **Enrollment Number** for **Enterprise Agreements (EA)**.</span></span> 


## <a name="connect-to-a-microsoft-customer-agreement-account"></a><span data-ttu-id="3c511-121">เชื่อมต่อกับบัญชีข้อตกลงลูกค้าของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="3c511-121">Connect to a Microsoft Customer Agreement account</span></span> 

<span data-ttu-id="3c511-122">หากต้องการเชื่อมต่อกับบัญชี **ข้อตกลงลูกค้าของ Microsoft** คุณสามารถรับ **ID โปรไฟล์การชำระเงินของคุณ** จากพอร์ทัล Azure:</span><span class="sxs-lookup"><span data-stu-id="3c511-122">To connect with a **Microsoft Customer Agreement** account, you can get your **Billing profile ID** from the Azure portal:</span></span>

1.  <span data-ttu-id="3c511-123">ใน [Azure portal](https://portal.azure.com/) นำทางไปยัง **การจัดการค่าใช้จ่าย + การเรียกเก็บเงิน**</span><span class="sxs-lookup"><span data-stu-id="3c511-123">In the [Azure portal](https://portal.azure.com/), navigate to **Cost Management + Billing**.</span></span>
2.  <span data-ttu-id="3c511-124">เลือกโปรไฟลการ์เรียกเก็บเงินของคุณ</span><span class="sxs-lookup"><span data-stu-id="3c511-124">Select your Billing profile.</span></span> 
3.  <span data-ttu-id="3c511-125"> ในเมนู **การตั้งค่า** ให้เลือก **คุณสมบัติ** ในแถบด้านข้าง</span><span class="sxs-lookup"><span data-stu-id="3c511-125">Under **Settings** in the menu, select **Properties** in the sidebar.</span></span>
4.  <span data-ttu-id="3c511-126">ในเมนู **โปรไฟล์การเรียกเก็บเงิน** ให้คัดลอก **ID**</span><span class="sxs-lookup"><span data-stu-id="3c511-126">Under **Billing profile**, copy the **ID**.</span></span> 
5.  <span data-ttu-id="3c511-127">สำหรับ **ขอบเขตการเลือก** ให้เลือก **ID โปรไฟล์การเรียกเก็บเงิน** และวาง ID โปรไฟล์การเรียกเก็บเงินจากขั้นตอนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="3c511-127">For **Choose Scope**, select **Billing Profile ID** and paste the billing profile ID from the previous step.</span></span> 
6.  <span data-ttu-id="3c511-128">ใส่จำนวนเดือนและเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3c511-128">Enter the number of months and select **OK**.</span></span>

    ![สกรีนช็อตแสดงคุณสมบัติ Azure Cost Management พร้อมขอบเขตของ ID โปรไฟล์การเรียกเก็บเงิน](media/desktop-connect-azure-cost-management/azure-cost-management-01a.png)

7.  <span data-ttu-id="3c511-130">เมื่อได้รับพร้อมท์ให้ลงชื่อเข้าใช้ด้วยบัญชีผู้ใช้และรหัสผ่าน Azure ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3c511-130">When prompted, sign in with your Azure user account and password.</span></span> <span data-ttu-id="3c511-131">คุณต้องใช้เจ้าของบัญชีการเรียกเก็บเงินเพื่อการเข้าถึงที่ประสบความสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="3c511-131">You must use a Billing account owner for successful access.</span></span> 


## <a name="connect-to-an-enterprise-agreement-account"></a><span data-ttu-id="3c511-132">เชื่อมต่อไปยังบัญชีข้อตกลงองค์กร</span><span class="sxs-lookup"><span data-stu-id="3c511-132">Connect to an Enterprise Agreement account</span></span>

<span data-ttu-id="3c511-133">หากต้องการเชื่อมต่อกับบัญชี ข้อตกลงองค์กร (EA) คุณจะได้รับ ID การลงทะเบียนของคุณจากพอร์ทัล Azure:</span><span class="sxs-lookup"><span data-stu-id="3c511-133">To connect with an Enterprise Agreement (EA) account, you can get your enrollment ID from the Azure portal:</span></span>

1.  <span data-ttu-id="3c511-134">ใน [Azure portal](https://portal.azure.com/) นำทางไปยัง **การจัดการค่าใช้จ่าย + การเรียกเก็บเงิน**</span><span class="sxs-lookup"><span data-stu-id="3c511-134">In the [Azure portal](https://portal.azure.com/), navigate to **Cost Management + Billing**.</span></span>
2.  <span data-ttu-id="3c511-135">เลือกบัญชีสำหรับการเรียกเก็บเงินของคุณ</span><span class="sxs-lookup"><span data-stu-id="3c511-135">Select your billing account.</span></span>
3.  <span data-ttu-id="3c511-136">ในเมนู **ภาพรวม** คัดลอก **ID บัญชีการเรียกเก็บเงิน**</span><span class="sxs-lookup"><span data-stu-id="3c511-136">On the **Overview** menu, copy the **Billing account ID**.</span></span>
4.  <span data-ttu-id="3c511-137">สำหรับ **ขอบเขตการเลือก** ให้เลือก **หมายเลขการสมัครเข้า** และวาง ID บัญชีการเรียกเก็บเงินจากขั้นตอนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="3c511-137">For **Choose Scope**, select **Enrollment Number** and paste the billing account ID from the previous step.</span></span> 
5.  <span data-ttu-id="3c511-138">ใส่จำนวนเดือนและจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3c511-138">Enter the number of months and then select **OK**.</span></span>

    ![สกรีนช็อตแสดงคุณสมบัติ Azure Cost Management พร้อมขอบเขตของหมายเลขการลงทะเบียน](media/desktop-connect-azure-cost-management/azure-cost-management-01b.png)

6.  <span data-ttu-id="3c511-140">เมื่อได้รับพร้อมท์ให้ลงชื่อเข้าใช้ด้วยบัญชีผู้ใช้และรหัสผ่าน Azure ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3c511-140">When prompted, sign in with your Azure user account and password.</span></span> <span data-ttu-id="3c511-141">คุณต้องใช้บัญชีผู้ดูแลระบบองค์กรสําหรับข้อตกลงขององค์กร</span><span class="sxs-lookup"><span data-stu-id="3c511-141">You must use an Enterprise Administrator account for Enterprise Agreements.</span></span>

## <a name="data-available-through-the-connector"></a><span data-ttu-id="3c511-142">ข้อมูลที่พร้อมใช้งานผ่านตัวเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="3c511-142">Data available through the connector</span></span>

<span data-ttu-id="3c511-143">เมื่อคุณรับรองความถูกต้องเรียบร้อยแล้ว หน้าต่าง **ตัวนำทาง** จะปรากฏขึ้นพร้อมกับตารางข้อมูลที่พร้อมใช้งานดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3c511-143">Once you successfully authenticate, a **Navigator** window appears with the following available data tables:</span></span>

| <span data-ttu-id="3c511-144">**ตาราง**</span><span class="sxs-lookup"><span data-stu-id="3c511-144">**Table**</span></span> | <span data-ttu-id="3c511-145">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="3c511-145">**Description**</span></span> |
| --- | --- |
| <span data-ttu-id="3c511-146">**สรุปยอดดุล**</span><span class="sxs-lookup"><span data-stu-id="3c511-146">**Balance summary**</span></span> | <span data-ttu-id="3c511-147">สรุปยอดดุลสำหรับข้อตกลงองค์กร (EA)</span><span class="sxs-lookup"><span data-stu-id="3c511-147">Summary of the balance for Enterprise Agreements (EA).</span></span> |
| <span data-ttu-id="3c511-148">**กิจกรรมในการเรียกเก็บเงิน**</span><span class="sxs-lookup"><span data-stu-id="3c511-148">**Billing events**</span></span> | <span data-ttu-id="3c511-149">แฟ้มบันทึกเหตุการณ์ของใบแจ้งหนี้ใหม่ ซื้อเครดิต และอื่น ๆ ข้อตกลงลูกค้าของ Microsoft เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3c511-149">Event log of new invoices, credit purchases, etc. Microsoft Customer Agreement only.</span></span> |
| <span data-ttu-id="3c511-150">**งบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="3c511-150">**Budgets**</span></span> | <span data-ttu-id="3c511-151">รายละเอียดงบประมาณเพื่อดูค่าใช้จ่ายจริงหรือการใช้งานกับเป้าหมายงบประมาณที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3c511-151">Budget details to view actual costs or usage against existing budget targets.</span></span> |
| <span data-ttu-id="3c511-152">**ค่าธรรมเนียม**</span><span class="sxs-lookup"><span data-stu-id="3c511-152">**Charges**</span></span> | <span data-ttu-id="3c511-153">สรุปการใช้งาน Azure ระดับเดือน ค่าธรรมเนียม Market Place และค่าธรรมเนียมที่เรียกเก็บเงินแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="3c511-153">A month-level summary of Azure usage, Marketplace charges, and charges billed separately.</span></span> <span data-ttu-id="3c511-154">ข้อตกลงลูกค้าของ Microsoft เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3c511-154">Microsoft Customer Agreement only.</span></span> |
| <span data-ttu-id="3c511-155">**เครดิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="3c511-155">**Credit lots**</span></span> | <span data-ttu-id="3c511-156">รายละเอียดการสั่งซื้อเครดิต Azure ทั้งหมดสำหรับโปรไฟล์การเรียกเก็บเงินที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="3c511-156">Azure credit lot purchase details for the provided billing profile.</span></span> <span data-ttu-id="3c511-157">ข้อตกลงลูกค้าของ Microsoft เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3c511-157">Microsoft Customer Agreement only.</span></span> |
| <span data-ttu-id="3c511-158">**ใบราคา**</span><span class="sxs-lookup"><span data-stu-id="3c511-158">**Pricesheets**</span></span> | <span data-ttu-id="3c511-159">อัตราการใช้โดยตัววัดสำหรับโปรไฟล์การเรียกเก็บเงินที่ระบุหรือการสมัครเข้า EA</span><span class="sxs-lookup"><span data-stu-id="3c511-159">Applicable meter rates for the provided billing profile or EA enrollment.</span></span> |
| <span data-ttu-id="3c511-160">**ค่าใช้จ่าย RI**</span><span class="sxs-lookup"><span data-stu-id="3c511-160">**RI charges**</span></span> | <span data-ttu-id="3c511-161">ค่าใช้จ่ายที่เชื่อมโยงกับอินสแตนซ์ที่สงวนไว้ของคุณมากกว่า 24 เดือนที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="3c511-161">Charges associated to your Reserved Instances over the last 24 months.</span></span> |
| <span data-ttu-id="3c511-162">**คำแนะนำ RI (ใช้ร่วมกัน)**</span><span class="sxs-lookup"><span data-stu-id="3c511-162">**RI recommendations (shared)**</span></span> | <span data-ttu-id="3c511-163">คำแนะนำในการซื้อมีอินสแตนซ์ที่สงวนไว้ยึดตามแนวโน้มการใช้งานของคุณในการสมัครใช้งานทั้งหมดในช่วง 7, 30 หรือ 60 วัน</span><span class="sxs-lookup"><span data-stu-id="3c511-163">Reserved Instance purchase recommendations based on all your subscription usage trends for the last 7, 30 or 60 days.</span></span> |
| <span data-ttu-id="3c511-164">**คำแนะนำ RI (เดียว)**</span><span class="sxs-lookup"><span data-stu-id="3c511-164">**RI recommendations (single)**</span></span> | <span data-ttu-id="3c511-165">คำแนะนำในการซื้อมีอินสแตนซ์ที่สงวนไว้ยึดตามแนวโน้มการใช้งานของคุณในการสมัครใช้งานครั้งเดียวในช่วง 7, 30 หรือ 60 วัน</span><span class="sxs-lookup"><span data-stu-id="3c511-165">Reserved Instance purchase recommendations based on your single subscription usage trends for the last 7, 30 or 60 days.</span></span> |
| <span data-ttu-id="3c511-166">**รายละเอียดการใช้งาน RI**</span><span class="sxs-lookup"><span data-stu-id="3c511-166">**RI usage details**</span></span> | <span data-ttu-id="3c511-167">รายละเอียดของปริมาณการใช้สำหรับอินสแตนซ์ที่สงวนไว้ของคุณที่มีอยู่ในช่วงเดือนที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="3c511-167">Consumption details for your existing Reserved Instances over the last month.</span></span> |
| <span data-ttu-id="3c511-168">**ข้อมูลสรุปการใช้งาน RI**</span><span class="sxs-lookup"><span data-stu-id="3c511-168">**RI usage summary**</span></span> | <span data-ttu-id="3c511-169">เปอร์เซ็นต์การใช้งานการของ Azure รายวัน</span><span class="sxs-lookup"><span data-stu-id="3c511-169">Daily Azure reservation usage percentage.</span></span> |
| <span data-ttu-id="3c511-170">**รายละเอียดการใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="3c511-170">**Usage details**</span></span> | <span data-ttu-id="3c511-171">การแบ่งรายละเอียดของปริมาณการใช้และค่าธรรมเนียมโดยประมาณสำหรับโปรไฟล์การเรียกเก็บเงินที่ให้ไว้ในการสมัครเข้า EA</span><span class="sxs-lookup"><span data-stu-id="3c511-171">A breakdown of consumed quantities and estimated charges for the given billing profile on EA enrollment.</span></span> |
| <span data-ttu-id="3c511-172">**รายละเอียดการใช้งานที่คืนทุน**</span><span class="sxs-lookup"><span data-stu-id="3c511-172">**Usage details amortized**</span></span> | <span data-ttu-id="3c511-173">การแบ่งรายละเอียดของปริมาณการใช้และค่าธรรมเนียมโดยประมาณสำหรับโปรไฟล์การเรียกเก็บเงินที่คืนทุนที่ให้ไว้ในการสมัครเข้า EA</span><span class="sxs-lookup"><span data-stu-id="3c511-173">A breakdown of consumed quantities and estimated amortized charges for the given billing profile on EA enrollment.</span></span> |

<span data-ttu-id="3c511-174">คุณสามารถเลือกตารางเพื่อดูตัวอย่างบทสนทนา</span><span class="sxs-lookup"><span data-stu-id="3c511-174">You can select a table to see a preview dialog.</span></span> <span data-ttu-id="3c511-175">คุณสามารถเลือกโดยการติ๊กกล่องด้านข้างชื่อของพวกเขาอย่างน้อยหนึ่งตาราง จาก นั้นเลือก **การโหลด**</span><span class="sxs-lookup"><span data-stu-id="3c511-175">You can select one or more tables by selecting the boxes beside their name and then select **Load**.</span></span>

![สกรีนช็อตแสดงกล่องโต้ตอบตัวนำทาง](media/desktop-connect-azure-cost-management/azure-cost-management-01c.png)

<span data-ttu-id="3c511-177">เมื่อคุณเลือก **โหลด** ข้อมูลจะถูกโหลดลงใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3c511-177">When you select **Load**, the data is loaded into Power BI Desktop.</span></span> 

<span data-ttu-id="3c511-178">เมื่อข้อมูลที่คุณเลือกถูกโหลด ตารางและเขตข้อมูลที่ปรากฏสามารถเห็นได้ในบานหน้าต่าง **เขตข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="3c511-178">When the data you selected is loaded, the data tables and fields are shown in the **Fields** pane.</span></span>


## <a name="next-steps"></a><span data-ttu-id="3c511-179">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="3c511-179">Next steps</span></span>

<span data-ttu-id="3c511-180">คุณสามารถเชื่อมต่อไปยังแหล่งข้อมูลต่าง ๆ มากมายโดยใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3c511-180">You can connect to many different data sources using Power BI Desktop.</span></span> <span data-ttu-id="3c511-181">สำหรับข้อมูลเพิ่มเติม ให้ดูบทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3c511-181">For more information, see the following articles:</span></span>

* [<span data-ttu-id="3c511-182">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="3c511-182">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
* [<span data-ttu-id="3c511-183">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3c511-183">Data Sources in Power BI Desktop</span></span>](desktop-data-sources.md)
* [<span data-ttu-id="3c511-184">จัดรูปทรงและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3c511-184">Shape and Combine Data with Power BI Desktop</span></span>](desktop-shape-and-combine-data.md)
* [<span data-ttu-id="3c511-185">เชื่อมต่อกับเวิร์กบุ๊ก Excel ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3c511-185">Connect to Excel workbooks in Power BI Desktop</span></span>](desktop-connect-excel.md)   
* [<span data-ttu-id="3c511-186">ใส่ข้อมูลลงใน Power BI Desktop โดยตรง</span><span class="sxs-lookup"><span data-stu-id="3c511-186">Enter data directly into Power BI Desktop</span></span>](desktop-enter-data-directly-into-desktop.md)