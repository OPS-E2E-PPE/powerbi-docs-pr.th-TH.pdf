---
title: เรียนรู้แพ็คเกจ Python ที่รองรับ
description: แพ็คเกจ Python ที่ได้รับการรองรับ และไม่รองรับใน Power BI
author: otarb
ms.author: otarb
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: conceptual
ms.date: 06/26/2020
LocalizationGroup: Connect to data
ms.openlocfilehash: 07b16bb90b548f071472f9f7d22095ccdff78f56
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96401730"
---
# <a name="create-visuals-by-using-python-packages-in-the-power-bi-service"></a><span data-ttu-id="112d7-103">สร้างวิชวลโดยใช้แพ็คเกจ Python ในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="112d7-103">Create visuals by using Python packages in the Power BI service</span></span>
<span data-ttu-id="112d7-104">คุณสามารถใช้ [ภาษาคอมพิวเตอร์ Python](https://www.python.org/) ที่มีประสิทธิภาพเพื่อสร้างภาพในบริการ Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="112d7-104">You can use the powerful [Python programming language](https://www.python.org/) to create visuals in the Power BI service.</span></span> <span data-ttu-id="112d7-105">แพ็คเกจ Python หลายแพ็กเกจได้รับการรองรับในบริการ Power BI และหลายแพ็คเกจจะได้รับการรองรับตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="112d7-105">Many Python packages are supported in the Power BI service and more are being supported all the time.</span></span>

<span data-ttu-id="112d7-106">ส่วนต่อไปนี้ให้ตารางที่เรียงตามตัวอักษรของแพ็คเกจ Python ที่ได้รับการรองรับใน Power BI</span><span class="sxs-lookup"><span data-stu-id="112d7-106">The following sections provide an alphabetical table of which Python packages are supported in Power BI.</span></span> 

## <a name="request-support-for-a-new-python-package"></a><span data-ttu-id="112d7-107">ขอรับการสนับสนุนสำหรับแพ็คเกจ Python ใหม่</span><span class="sxs-lookup"><span data-stu-id="112d7-107">Request support for a new Python package</span></span>
<span data-ttu-id="112d7-108">แพ็คเกจ Python รองรับการ **บริการ Power BI** ที่พบในส่วนต่อไปนี้ ชื่อว่า **แพ็คเกจที่ได้รับการรองรับ**</span><span class="sxs-lookup"><span data-stu-id="112d7-108">Supported Python packages for the **Power BI service** are found in the following section, titled **Supported Packages**.</span></span> <span data-ttu-id="112d7-109">ถ้าคุณต้องการขอรับการรองรับให้กับแพ็คเกจ Python ที่ไม่พบในรายการที่แสดงอยู่ โปรดส่งคำขอของคุณมาที่ [Power BI Ideas](https://ideas.powerbi.com)</span><span class="sxs-lookup"><span data-stu-id="112d7-109">If you would like to request support of an Python package not found in that list, please submit your request to [Power BI Ideas](https://ideas.powerbi.com).</span></span>

## <a name="requirements-and-limitations-of-python-packages"></a><span data-ttu-id="112d7-110">แพ็คเกจข้อกำหนดและขีดจำกัดของ Python</span><span class="sxs-lookup"><span data-stu-id="112d7-110">Requirements and Limitations of Python packages</span></span>
<span data-ttu-id="112d7-111">มีข้อกำหนดและขีดจำกัดสำหรับแพคเกจ Python อยู่เล็กน้อยดังนี้:</span><span class="sxs-lookup"><span data-stu-id="112d7-111">There are a handful of requirements and limitations for Python packages:</span></span>

* <span data-ttu-id="112d7-112">รันไทม์ของ Python ปัจจุบัน: Python 3.7.7.</span><span class="sxs-lookup"><span data-stu-id="112d7-112">Current Python runtime: Python 3.7.7.</span></span>
* <span data-ttu-id="112d7-113">บริการ Power BI ส่วนใหญ่รองรับแพ็คเกจ Python ที่มีใบอนุญาตซอฟต์แวร์แบบเปิดและฟรี เช่น GPL-2 GPL-3 MIT+ และอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="112d7-113">The Power BI service, for the most part, supports Python packages with free and open-source software licenses such as GPL-2, GPL-3, MIT+, and so on.</span></span>
* <span data-ttu-id="112d7-114">บริการ Power BI รองรับแพ็คเกจที่เผยแพร่ใน PyPI</span><span class="sxs-lookup"><span data-stu-id="112d7-114">The Power BI service supports packages published in PyPI.</span></span> <span data-ttu-id="112d7-115">บริการไม่รองรับแพ็คเกจ Python ส่วนตัว หรือแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="112d7-115">The service does not support private or custom Python packages.</span></span> <span data-ttu-id="112d7-116">แนะนำให้ผู้ใช้สร้างแพ็คเกจส่วนตัวของพวกเขาพร้อมใช้งานบน PyPI ก่อนที่จะร้องขอแพ็คเกจมีอยู่ในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="112d7-116">Users are encouraged to make their private packages available on PyPI prior to requesting the package be available in the Power BI service.</span></span>
* <span data-ttu-id="112d7-117">สำหรับภาพของ Python ใน **Power BI Desktop** คุณสามารถติดตั้งแพ็คเกจใดก็ได้รวมถึงแพ็คเกจ Python แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="112d7-117">For Python visuals in **Power BI Desktop**, you can install any package, including custom Python packages.</span></span>
* <span data-ttu-id="112d7-118">สำหรับเหตุผลทางด้านความปลอดภัยและความเป็นส่วนตัว แพ็คเกจ Python ที่มีคิวรีจากไคลเอนต์-เซิร์ฟเวอร์ทั่วเครือข่ายเวิลด์ไวด์เว็บ  บริการนี้จะไม่รองรับ</span><span class="sxs-lookup"><span data-stu-id="112d7-118">For security and privacy reasons, Python packages that provide client-server queries over the World-Wide Web in the service, are not supported.</span></span> <span data-ttu-id="112d7-119">ระบบเครือข่ายบล็อกการกระทำดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="112d7-119">Networking is blocked for such attempts.</span></span>
* <span data-ttu-id="112d7-120">กระบวนการอนุมัติเพื่อรวมแพ็คเกจ Python ใหม่มีแผนภูมิต้นไม้ของความสัมพันธ์ โดยที่บางความสัมพันธ์ต้องมีการติดตั้งในการบริการที่ไม่รองรับก่อน</span><span class="sxs-lookup"><span data-stu-id="112d7-120">The approval process for including a new Python package has a tree of dependencies; some dependencies required to be installed in the service cannot be supported.</span></span>

## <a name="python-packages-that-are-supported-in-power-bi"></a><span data-ttu-id="112d7-121">แพ็คเกจ Python ที่ได้รับการรองรับใน Power BI</span><span class="sxs-lookup"><span data-stu-id="112d7-121">Python packages that are supported in Power BI</span></span>
<span data-ttu-id="112d7-122">ตารางต่อไปนี้แสดงแพ็คเกจที่ **ได้รับการสนับสนุน** ในบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="112d7-122">The following table shows which packages **are supported** in the Power BI service.</span></span>


|        <span data-ttu-id="112d7-123">แพ็คเกจ</span><span class="sxs-lookup"><span data-stu-id="112d7-123">Package</span></span>        |   <span data-ttu-id="112d7-124">เวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="112d7-124">Version</span></span>   |                                   <span data-ttu-id="112d7-125">ลิงก์</span><span class="sxs-lookup"><span data-stu-id="112d7-125">Link</span></span>                                   |
|-----------------------|-------------|--------------------------------------------------------------------------|
|<span data-ttu-id="112d7-126">matplotlib</span><span class="sxs-lookup"><span data-stu-id="112d7-126">matplotlib</span></span>|<span data-ttu-id="112d7-127">3.2.1</span><span class="sxs-lookup"><span data-stu-id="112d7-127">3.2.1</span></span>|https://pypi.org/project/matplotlib|
|<span data-ttu-id="112d7-128">numpy</span><span class="sxs-lookup"><span data-stu-id="112d7-128">numpy</span></span>|<span data-ttu-id="112d7-129">1.18.4</span><span class="sxs-lookup"><span data-stu-id="112d7-129">1.18.4</span></span>|https://pypi.org/project/numpy|
|<span data-ttu-id="112d7-130">แพนด้า</span><span class="sxs-lookup"><span data-stu-id="112d7-130">pandas</span></span>|<span data-ttu-id="112d7-131">1.0.1</span><span class="sxs-lookup"><span data-stu-id="112d7-131">1.0.1</span></span>|https://pypi.org/project/pandas|
|<span data-ttu-id="112d7-132">scikit-learn</span><span class="sxs-lookup"><span data-stu-id="112d7-132">scikit-learn</span></span>|<span data-ttu-id="112d7-133">0.23.0</span><span class="sxs-lookup"><span data-stu-id="112d7-133">0.23.0</span></span>|https://pypi.org/project/scikit-learn|
|<span data-ttu-id="112d7-134">scipy</span><span class="sxs-lookup"><span data-stu-id="112d7-134">scipy</span></span>|<span data-ttu-id="112d7-135">1.4.1</span><span class="sxs-lookup"><span data-stu-id="112d7-135">1.4.1</span></span>|https://pypi.org/project/scipy|
|<span data-ttu-id="112d7-136">s eaborn</span><span class="sxs-lookup"><span data-stu-id="112d7-136">s  eaborn</span></span>|<span data-ttu-id="112d7-137">0.10.1</span><span class="sxs-lookup"><span data-stu-id="112d7-137">0.10.1</span></span>|https://pypi.org/project/seaborn|
|<span data-ttu-id="112d7-138">statsmodels</span><span class="sxs-lookup"><span data-stu-id="112d7-138">statsmodels</span></span>|<span data-ttu-id="112d7-139">0.11.1</span><span class="sxs-lookup"><span data-stu-id="112d7-139">0.11.1</span></span>|https://pypi.org/project/statsmodels|
|<span data-ttu-id="112d7-140">xgboost</span><span class="sxs-lookup"><span data-stu-id="112d7-140">xgboost</span></span>|<span data-ttu-id="112d7-141">1.1.0</span><span class="sxs-lookup"><span data-stu-id="112d7-141">1.1.0</span></span>|https://pypi.org/project/xgboost|

## <a name="next-steps"></a><span data-ttu-id="112d7-142">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="112d7-142">Next steps</span></span>
<span data-ttu-id="112d7-143">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Python ใน Power BI โปรดดูที่บทความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="112d7-143">For more information about Python in Power BI, take a look at the following articles:</span></span>

* [<span data-ttu-id="112d7-144">สร้างวิชวลของ Power BI โดยใช้ Python</span><span class="sxs-lookup"><span data-stu-id="112d7-144">Create Power BI visuals using Python</span></span>](desktop-python-visuals.md)
* [<span data-ttu-id="112d7-145">ขั้นตอนการเรียกใช้สคริปต์ Python ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="112d7-145">Running Python scripts in Power BI Desktop</span></span>](desktop-python-scripts.md)
* [<span data-ttu-id="112d7-146">การใช้ Python ใน Query Editor</span><span class="sxs-lookup"><span data-stu-id="112d7-146">Using Python in Query Editor</span></span>](desktop-python-in-query-editor.md)
