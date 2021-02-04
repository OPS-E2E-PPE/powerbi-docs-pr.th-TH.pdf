---
title: เชื่อมต่อกับฐานข้อมูล Oracle ด้วย Power BI Desktop
description: ขั้นตอนและการดาวน์โหลดที่จำเป็นต้องเชื่อมต่อ Oracle กับ Power BI Desktop
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 01/04/2021
LocalizationGroup: Connect to data
ms.openlocfilehash: 134c11108da77c87ba087df9ac5564521d7a303d
ms.sourcegitcommit: 932f6856849c39e34229dc9a49fb9379c56a888a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/06/2021
ms.locfileid: "97926387"
---
# <a name="connect-to-an-oracle-database-with-power-bi-desktop"></a><span data-ttu-id="4272a-103">เชื่อมต่อกับฐานข้อมูล Oracle ด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4272a-103">Connect to an Oracle database with Power BI Desktop</span></span>
<span data-ttu-id="4272a-104">การเชื่อมต่อกับฐานข้อมูล Oracle ด้วย Power BI Desktop นั้น ต้องติดตั้งซอฟต์แวร์ไคลเอ็นต์ Oracle ที่ถูกต้องบนคอมพิวเตอร์ที่ใช้งาน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="4272a-104">To connect to an Oracle database with Power BI Desktop, the correct Oracle client software must be installed on the computer running Power BI Desktop.</span></span> <span data-ttu-id="4272a-105">ซอฟต์แวร์ไคลเอ็นต์ Oracle ที่คุณใช้ขึ้นอยู่กับเวอร์ชันของ Power BI Desktop ที่คุณได้ติดตั้ง: 32 บิต หรือ 64 บิต</span><span class="sxs-lookup"><span data-stu-id="4272a-105">The Oracle client software you use depends on which version of Power BI Desktop you've installed: 32-bit or 64-bit.</span></span> <span data-ttu-id="4272a-106">นอกจากนี้ยังขึ้นอยู่กับเวอร์ชันของเซิร์ฟเวอร์ Oracle ของคุณ</span><span class="sxs-lookup"><span data-stu-id="4272a-106">It also depends on your version of Oracle server.</span></span>

<span data-ttu-id="4272a-107">เวอร์ชัน Oracle ที่รองรับ:</span><span class="sxs-lookup"><span data-stu-id="4272a-107">Supported Oracle versions:</span></span> 
- <span data-ttu-id="4272a-108">Oracle Server 9 และเวอร์ชันที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="4272a-108">Oracle Server 9 and later</span></span>
- <span data-ttu-id="4272a-109">ซอฟต์แวร์ Oracle Data Access Client (ODAC) 11.2 และเวอร์ชันที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="4272a-109">Oracle Data Access Client (ODAC) software 11.2 and later</span></span>

> [!NOTE]
> <span data-ttu-id="4272a-110">หากคุณกำลังกำหนดค่าฐานข้อมูล Oracle สำหรับ Power BI Desktop เกตเวย์ข้อมูลในองค์กร หรือ เซิร์ฟเวอร์รายงาน Power BI โปรดดูข้อมูลในบทความ[ชนิดการเชื่อมต่อ Oracle](/sql/reporting-services/report-data/oracle-connection-type-ssrs?view=sql-server-ver15)</span><span class="sxs-lookup"><span data-stu-id="4272a-110">If you're configuring an Oracle database for Power BI Desktop, On Premises Data Gateway or Power BI Report Server, consult the information in the [Oracle Connection Type](/sql/reporting-services/report-data/oracle-connection-type-ssrs?view=sql-server-ver15) article.</span></span> 


## <a name="determining-which-version-of-power-bi-desktop-is-installed"></a><span data-ttu-id="4272a-111">หา Power BI Desktop ที่ติดตั้งอยู่เวอร์ชันใด</span><span class="sxs-lookup"><span data-stu-id="4272a-111">Determining which version of Power BI Desktop is installed</span></span>
<span data-ttu-id="4272a-112">เมื่อต้องการตรวจสอบเวอร์ชันของ Power BI Desktop ที่ถูกติดตั้ง ให้เลือก **ไฟล์** > **วิธีใช้** > **เกี่ยวกับ** จากนั้นให้ตรวจสอบบรรทัด **เวอร์ชัน**</span><span class="sxs-lookup"><span data-stu-id="4272a-112">To determine which version of Power BI Desktop is installed, select **File** > **Help** > **About**, then check the **Version** line.</span></span> <span data-ttu-id="4272a-113">ในรูปต่อไปนี้ Power BI Desktop เวอร์ชัน 64 บิตถูกติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="4272a-113">In the following image, a 64-bit version of Power BI Desktop is installed:</span></span>

![เวอร์ชัน Power BI Desktop](media/desktop-connect-oracle-database/connect-oracle-database_1.png)

## <a name="install-the-oracle-client"></a><span data-ttu-id="4272a-115">ติดตั้ง Oracle client</span><span class="sxs-lookup"><span data-stu-id="4272a-115">Install the Oracle client</span></span>
- <span data-ttu-id="4272a-116">สำหรับ Power BI Desktop เวอร์ชัน 32 บิต [ดาวน์โหลดและติดตั้งไคลเอ็นต์ Oracle 32 บิต](https://www.oracle.com/technetwork/topics/dotnet/utilsoft-086879.html).</span><span class="sxs-lookup"><span data-stu-id="4272a-116">For the 32-bit version of Power BI Desktop, [download and install the 32-bit Oracle client](https://www.oracle.com/technetwork/topics/dotnet/utilsoft-086879.html).</span></span>

- <span data-ttu-id="4272a-117">สำหรับ Power BI Desktop เวอร์ชัน 64 บิต [ดาวน์โหลดและติดตั้งไคลเอ็นต์ Oracle 64 บิต](https://www.oracle.com/database/technologies/odac-downloads.html).</span><span class="sxs-lookup"><span data-stu-id="4272a-117">For the 64-bit version of Power BI Desktop, [download and install the 64-bit Oracle client](https://www.oracle.com/database/technologies/odac-downloads.html).</span></span>

> [!NOTE]
> <span data-ttu-id="4272a-118">เลือกเวอร์ชันของ Oracle Data Access Client (ODAC) ซึ่งสามารถทำงานร่วมกับเซิร์ฟเวอร์ Oracle ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="4272a-118">Choose a version of Oracle Data Access Client (ODAC) which is compatible with your Oracle Server.</span></span> <span data-ttu-id="4272a-119">ตัวอย่างเช่น ODAC 12.x ไม่รองรับเซิร์ฟเวอร์ Oracle เวอร์ชัน 9</span><span class="sxs-lookup"><span data-stu-id="4272a-119">For instance, ODAC 12.x does not always support Oracle Server version 9.</span></span>
> <span data-ttu-id="4272a-120">เลือกตัวติดตั้ง Windows ของไคลเอ็นต์ Oracle</span><span class="sxs-lookup"><span data-stu-id="4272a-120">Choose the Windows installer of the Oracle Client.</span></span>
> <span data-ttu-id="4272a-121">ระหว่างการตั้งค่าของไคลเอ็นต์ Oracle คุณต้องตรวจสอบให้แน่ใจว่าได้เปิดใช้งาน *กำหนดค่า ODP.NET และ/หรือผู้ให้บริการ Oracle สำหรับ ASP.NET ที่ระดับเครื่อง* โดยการเลือกกล่องกาเครื่องหมายที่เกี่ยวข้องในระหว่างการตั้งค่าตัวช่วยสร้าง</span><span class="sxs-lookup"><span data-stu-id="4272a-121">During the setup of the Oracle client, make sure you enable *Configure ODP.NET and/or Oracle Providers for ASP.NET at machine-wide level* by selecting the corresponding checkbox during the setup wizard.</span></span> <span data-ttu-id="4272a-122">ตัวช่วยสร้างไคลเอ็นต์ Oracle บางเวอร์ชันเลือกกล่องกาเครื่องหมายตามค่าเริ่มต้น ซึ่งเวอร์ชันอื่น ๆ ไม่ทำเช่นนี้</span><span class="sxs-lookup"><span data-stu-id="4272a-122">Some versions of the Oracle client wizard selects the checkbox by default, others do not.</span></span> <span data-ttu-id="4272a-123">ตรวจสอบให้แน่ใจว่าคุณได้เลือกกล่องกาเครื่องหมายเพื่อให้ Power BI สามารถเชื่อมต่อกับฐานข้อมูล Oracle ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="4272a-123">Make sure that checkbox is selected so that Power BI can connect to your Oracle database.</span></span>

## <a name="connect-to-an-oracle-database"></a><span data-ttu-id="4272a-124">เชื่อมต่อกับฐานข้อมูล Oracle</span><span class="sxs-lookup"><span data-stu-id="4272a-124">Connect to an Oracle database</span></span>
<span data-ttu-id="4272a-125">หลังจากที่คุณติดตั้งไคลเอ็นต์ไดร์ฟเวอร์ Oracle ที่ตรงกัน คุณสามารถเชื่อมต่อกับฐานข้อมูล Oracle</span><span class="sxs-lookup"><span data-stu-id="4272a-125">After you install the matching Oracle client driver, you can connect to an Oracle database.</span></span> <span data-ttu-id="4272a-126">เมื่อต้องทำการเชื่อมต่อ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4272a-126">To make the connection, take the following steps:</span></span>

1. <span data-ttu-id="4272a-127">จากแท็บ **หน้าแรก** ให้เลือก **รับข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="4272a-127">From the **Home** tab, select **Get Data**.</span></span> 

2. <span data-ttu-id="4272a-128">จากหน้าต่าง **รับข้อมูล** ที่ปรากฏขึ้น ให้เลือก **เพิ่มเติม** (ถ้าจำเป็น) เลือก **ฐานข้อมูล** > **ฐานข้อมูล Oracle** และจากนั้นเลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="4272a-128">From the **Get Data** window that appears, select **More** (if necessary), select **Database** > **Oracle database**, and then select **Connect**.</span></span>
   
   ![เชื่อมต่อฐานข้อมูล Oracle](media/desktop-connect-oracle-database/connect-oracle-database_2.png)
3. <span data-ttu-id="4272a-130">ในกล่องโต้ตอบ **ฐานข้อมูล Oracle** ที่ปรากฏขึ้น ให้ใส่ชื่อของ **เซิร์ฟเวอร์** และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4272a-130">In the **Oracle database** dialog that appears, provide the name of the **Server**, and select **OK**.</span></span> <span data-ttu-id="4272a-131">หากกำหนดให้มี SID ให้ระบุโดยใช้รูปแบบ: *ServerName/SID* โดยที่ *SID* เป็นชื่อที่ไม่ซ้ำกันของฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4272a-131">If a SID is required, specify it by using the format: *ServerName/SID*, where *SID* is the unique name of the database.</span></span> <span data-ttu-id="4272a-132">ถ้ารูปแบบ *ServerName/SID* ไม่ทำงาน ให้ใช้ *ServerName/ServiceName* โดยที่ *ServiceName* เป็นนามแฝงที่คุณใช้เพื่อเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="4272a-132">If the *ServerName/SID* format doesn't work, use *ServerName/ServiceName*, where *ServiceName* is the alias you use to connect.</span></span>


   ![ใส่ชื่อเซิร์ฟเวอร์ Oracle](media/desktop-connect-oracle-database/connect-oracle-database_3.png)

   > [!NOTE]
   > <span data-ttu-id="4272a-134">หากคุณกำลังใช้ฐานข้อมูลในเครื่องหรือการเชื่อมต่อฐานข้อมูลที่ทำงานแบบอิสระ คุณอาจต้องวางชื่อเซิร์ฟเวอร์ในเครื่องหมายคำพูดเพื่อหลีกเลี่ยงข้อผิดพลาดในการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="4272a-134">If you are using a local database, or autonomous database connections, you may need to place the server name in quotation marks to avoid connection errors.</span></span> 
      
4. <span data-ttu-id="4272a-135">ถ้าคุณต้องการนำเข้าข้อมูลโดยใชคิวรี่ของฐานข้อมูลแบบเนทีฟ ให้ใส่คิวรีของคุณในกล่อง **คำสั่ง SQL** ที่ปรากฏขึ้นเมื่อคุณขยายส่วน **ตัวเลือกขั้นสูง** ของกล่องโต้ตอบ **ฐานข้อมูล Oracle**</span><span class="sxs-lookup"><span data-stu-id="4272a-135">If you want to import data by using a native database query, put your query in the **SQL statement** box, which appears when you expand the **Advanced options** section of the **Oracle database** dialog.</span></span>
   
   ![ขยายตัวเลือกขั้นสูง](media/desktop-connect-oracle-database/connect-oracle-database_4.png)


5. <span data-ttu-id="4272a-137">หลังจากที่คุณป้อนข้อมูลของฐานข้อมูล Oracle ของคุณลงในกล่องโต้ตอบฐานข้อมูล **Oracle** (รวมถึงข้อมูลประกอบใดๆ เช่น SID หรือคิวรี่ฐานข้อมูลเนทีฟ) ให้เลือก **ตกลง** เพื่อเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="4272a-137">After you've entered your Oracle database information in the **Oracle database** dialog (including any optional information such as a SID or a native database query), select **OK** to connect.</span></span>
5. <span data-ttu-id="4272a-138">ถ้าฐานข้อมูล Oracle ต้องใช้ข้อมูลประจำตัวผู้ใช้ฐานข้อมูล ให้ป้อนข้อมูลประจำตัวเหล่านั้นในกล่องโต้ตอบเมื่อได้รับการขอจากระบบ</span><span class="sxs-lookup"><span data-stu-id="4272a-138">If the Oracle database requires database user credentials, input those credentials in the dialog when prompted.</span></span>


## <a name="troubleshooting"></a><span data-ttu-id="4272a-139">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="4272a-139">Troubleshooting</span></span>

<span data-ttu-id="4272a-140">คุณอาจพบข้อผิดพลาดต่าง ๆ มากมายจาก Oracle เมื่อไวยากรณ์การตั้งชื่อไม่ถูกต้อง หรือไม่ได้กำหนดค่าอย่างถูกต้อง:</span><span class="sxs-lookup"><span data-stu-id="4272a-140">You might encounter any of several errors from Oracle when the naming syntax is either incorrect or not configured properly:</span></span>

* <span data-ttu-id="4272a-141">ORA-12154: TNS: ไม่สามารถแก้ไขตัวระบุการเชื่อมต่อที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="4272a-141">ORA-12154: TNS:could not resolve the connect identifier specified.</span></span>
* <span data-ttu-id="4272a-142">ORA-12514: TNS: ในขณะนี้ ตัวรอรับการติดต่อไม่รู้จักบริการที่ร้องขอในตัวอธิบายการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="4272a-142">ORA-12514: TNS:listener does not currently know of service requested in connect descriptor.</span></span>
* <span data-ttu-id="4272a-143">ORA-12541: TNS: ไม่มีตัวรอรับการติดต่อ</span><span class="sxs-lookup"><span data-stu-id="4272a-143">ORA-12541: TNS:no listener.</span></span>
* <span data-ttu-id="4272a-144">ORA-12170: TNS: เกิดเหตุการณ์การเชื่อมต่อหมดเวลา</span><span class="sxs-lookup"><span data-stu-id="4272a-144">ORA-12170: TNS:connect timeout occurred.</span></span>
* <span data-ttu-id="4272a-145">ORA-12504: TNS: ตัวรอรับการติดต่อไม่ได้รับ SERVICE_NAME ใน CONNECT_DATA</span><span class="sxs-lookup"><span data-stu-id="4272a-145">ORA-12504: TNS:listener was not given the SERVICE_NAME in CONNECT_DATA.</span></span>

<span data-ttu-id="4272a-146">ข้อผิดพลาดเหล่านี้อาจเกิดขึ้นหากไม่ได้ติดตั้ง Oracle client หรือกำหนดค่าไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="4272a-146">These errors might occur if the Oracle client either isn't installed or isn't configured properly.</span></span> <span data-ttu-id="4272a-147">ถ้ามีการติดตั้งอยู่แล้ว ให้ตรวจสอบว่ามีการกำหนดค่าไฟล์ tnsnames.ora อย่างถูกต้องหรือไม่ และคุณกำลังใช้ net_service_name ที่เหมาะสมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4272a-147">If it's installed, verify that the tnsnames.ora file is properly configured and you're using the proper net_service_name.</span></span> <span data-ttu-id="4272a-148">นอกจากนี้ คุณจะต้องตรวจสอบให้แน่ใจว่า net_service_name สำหรับเครื่องที่ใช้ Power BI Desktop และเครื่องที่ใช้งานเกตเวย์นั้นเป็นตัวเดียวกันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4272a-148">You also need to make sure that the net_service_name is the same between the machine that uses Power BI Desktop and the machine that runs the gateway.</span></span> <span data-ttu-id="4272a-149">สำหรับข้อมูลเพิ่มเติม โปรดดู [ติดตั้ง Oracle Client](#install-the-oracle-client)</span><span class="sxs-lookup"><span data-stu-id="4272a-149">For more information, see [Install the Oracle client](#install-the-oracle-client).</span></span>

<span data-ttu-id="4272a-150">คุณอาจประสบปัญหาความเข้ากันได้ระหว่างเวอร์ชัน Oracle server และเวอร์ชัน Oracle Data Access Client</span><span class="sxs-lookup"><span data-stu-id="4272a-150">You might also encounter a compatibility issue between the Oracle server version and the Oracle Data Access Client version.</span></span> <span data-ttu-id="4272a-151">โดยทั่วไปแล้ว คุณต้องใช้เวอร์ชันที่สอดคล้องกัน เนื่องจากชุดการทำงานบางอย่างอาจไม่เข้ากัน</span><span class="sxs-lookup"><span data-stu-id="4272a-151">Typically, you want these versions to match, as some combinations are incompatible.</span></span> <span data-ttu-id="4272a-152">ตัวอย่างเช่น ODAC 12.x นั้นไม่รองรับเซิร์ฟเวอร์ Oracle เวอร์ชัน 9</span><span class="sxs-lookup"><span data-stu-id="4272a-152">For instance, ODAC 12.x does not support Oracle Server version 9.</span></span>

<span data-ttu-id="4272a-153">ถ้าคุณดาวน์โหลด Power BI Desktop จาก Microsoft Store คุณอาจไม่สามารถเชื่อมต่อกับฐานข้อมูล Oracle เนื่องจากปัญหาโปรแกรมควบคุม Oracle</span><span class="sxs-lookup"><span data-stu-id="4272a-153">If you downloaded Power BI Desktop from the Microsoft Store, you might be unable to connect to Oracle databases because of an Oracle driver issue.</span></span> <span data-ttu-id="4272a-154">ถ้าคุณพบปัญหานี้ ข้อความแสดงข้อผิดพลาดที่ส่งคืนคือ: *ไม่ได้ตั้งค่าการอ้างอิงอ็อปเจ็กต์*</span><span class="sxs-lookup"><span data-stu-id="4272a-154">If you encounter this issue, the error message returned is: *Object reference not set*.</span></span> <span data-ttu-id="4272a-155">การแก้ไขปัญหา ให้ทำหนึ่งในขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="4272a-155">To address the issue, do one of these steps:</span></span>

* <span data-ttu-id="4272a-156">ดาวน์โหลด Power BI Desktop จาก [ศูนย์ดาวน์โหลด](https://www.microsoft.com/download/details.aspx?id=58494) แทนที่จะเป็น Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="4272a-156">Download Power BI Desktop from the [Download Center](https://www.microsoft.com/download/details.aspx?id=58494) instead of Microsoft Store.</span></span>

* <span data-ttu-id="4272a-157">ถ้าคุณต้องการใช้เวอร์ชันจาก Microsoft Store: บนคอมพิวเตอร์ของคุณ ให้คัดลอก oraons.dll จาก _12.X.X\client_X_ ลงใน _12.X.X\client_X\bin_ โดยที่ _X_ แสดงเวอร์ชันและหมายเลขไดเรกทอรี่</span><span class="sxs-lookup"><span data-stu-id="4272a-157">If you want to use the version from Microsoft Store: on your local computer, copy oraons.dll from _12.X.X\client_X_ to _12.X.X\client_X\bin_, where _X_ represents version and directory numbers.</span></span>

<span data-ttu-id="4272a-158">หากคุณเห็นข้อความแสดงข้อผิดพลาด *ไม่ได้ตั้งค่าการอ้างอิงอ็อปเจ็กต์* ใน Power BI Gateway เมื่อคุณเชื่อมต่อกับฐานข้อมูล Oracle ให้ทำตามคำแนะนำใน [จัดการแหล่งข้อมูลของคุณ - Oracle](service-gateway-onprem-manage-oracle.md)</span><span class="sxs-lookup"><span data-stu-id="4272a-158">If you see the error message, *Object reference not set*, in the Power BI Gateway when you connect to an Oracle database, follow the instructions in [Manage your data source - Oracle](service-gateway-onprem-manage-oracle.md).</span></span>

<span data-ttu-id="4272a-159">ถ้าคุณกำลังใช้เซิร์ฟเวอร์รายงาน Power BI ให้ดูคำแนะนำในบทความ [ชนิดการเชื่อมต่อ Oracle](/sql/reporting-services/report-data/oracle-connection-type-ssrs?view=sql-server-ver15)</span><span class="sxs-lookup"><span data-stu-id="4272a-159">If you're using Power BI Report Server, consult the guidance in the [Oracle Connection Type](/sql/reporting-services/report-data/oracle-connection-type-ssrs?view=sql-server-ver15) article.</span></span>