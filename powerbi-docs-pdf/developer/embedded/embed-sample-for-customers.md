---
title: ฝังเนื้อหาในแอปพลิเคชันการวิเคราะห์แบบฝังตัว Power BI ของคุณเพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นสําหรับลูกค้าของคุณ
description: เรียนรู้วิธีการฝังรายงาน แดชบอร์ด หรือไทล์ลงในตัวอย่างการวิเคราะห์แบบฝังตัวของ Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.topic: tutorial
ms.service: powerbi
ms.subservice: powerbi-developer
ms.custom: seodec18
ms.date: 12/22/2020
ms.openlocfilehash: 28081342763ca297648f67f953a29b46d02bf478
ms.sourcegitcommit: 2e81649476d5cb97701f779267be59e393460097
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 02/02/2021
ms.locfileid: "99494856"
---
# <a name="tutorial-embed-power-bi-content-using-a-sample-embed-for-your-customers-application"></a>บทช่วยสอน: ฝังเนื้อหา Power BI โดยใช้แอปพลิเคชันตัวอย่าง *การฝังตัวสำหรับลูกค้าของคุณ*

**การวิเคราะห์แบบฝังตัว** และ **Power BI Embedded** (ข้อเสนอของ Azure) ช่วยให้คุณสามารถฝังเนื้อหา Power BI เช่น รายงาน แดชบอร์ด และไทล์ลงในแอปพลิเคชันของคุณได้

ในบทช่วยสอนนี้ คุณจะเรียนรู้วิธีการ:

>[!div class="checklist"]
>* ตั้งค่าสภาพแวดล้อมแบบฝังตัวของคุณ
>* กำหนดค่าแอปพลิเคชันตัวอย่าง *การฝังตัวสำหรับลูกค้าของคุณ* (หรือที่เรียกว่า *แอปเป็นเจ้าของข้อมูล*)

หากต้องการใช้แอปพลิเคชันของคุณ ผู้ใช้ของคุณจะไม่จำเป็นต้องลงชื่อเข้าใช้ Power BI หรือไม่จำเป็นต้องมีสิทธิการใช้งาน Power BI

เราขอแนะนำให้ใช้วิธี *การฝังตัวสำหรับลูกค้าของคุณ* เพื่อฝังเนื้อหา Power BI ของคุณ หากคุณเป็นผู้จำหน่ายซอฟต์แวร์อิสระ (ISV) หรือนักพัฒนาที่ต้องการสร้างแอปพลิเคชันสำหรับบุคคลที่สาม

## <a name="code-sample-specifications"></a>ข้อมูลจำเพาะตัวอย่างของโค้ด

บทช่วยสอนนี้มีคำแนะนำสำหรับการกำหนดค่าฝังตัวสำหรับแอปพลิเคชันตัวอย่าง *ของลูกค้าของคุณ* ในหนึ่งในกรอบงานต่อไปนี้:

* .NET Framework
* .NET Core
* Java
* Node JS
* Python

ตัวอย่างโค้ดรองรับเบราว์เซอร์ต่อไปนี้:

* Microsoft Edge
* Google Chrome
* Mozilla Firefox

## <a name="prerequisites"></a>สิ่งที่จำเป็นต้องมี

ก่อนที่คุณจะเริ่มต้นบทช่วยสอนนี้ ให้ตรวจสอบว่าคุณมีการขึ้นต่อกันทั้งของ Power BI และโค้ดที่แสดงรายการด้านล่าง:

* **การขึ้นต่อกันของ Power BI**

    * [ผู้เช่า Azure Active Directory](create-an-azure-active-directory-tenant.md) ของคุณเอง

    * หากต้องการรับรองความถูกต้องของแอปกับ Power BI คุณจะต้องมีหนึ่งในรายการต่อไปนี้:

        * [โครงร่างสำคัญของบริการ](embed-service-principal.md) - Azure Active Directory (Azure AD) [ออบเจ็กต์โครงร่างสำคัญของบริการ](/azure/active-directory/develop/app-objects-and-service-principals#service-principal-object)ที่อนุญาตให้ Azure AD รับรองความถูกต้องของแอปของคุณ

        * สิทธิ์การใช้งาน [Power BI Pro](../../admin/service-admin-purchasing-power-bi-pro.md) - ซึ่งจะเป็น **ผู้ใช้หลัก** ของคุณและแอปของคุณจะใช้เพื่อรับรองความถูกต้องกับ Power BI

        * สิทธิ์การใช้งาน Power BI [Premium Per User (PPU)](../../admin/service-premium-per-user-faq.md) - ซึ่งจะเป็น **ผู้ใช้หลัก** ของคุณและแอปของคุณจะใช้เพื่อรับรองความถูกต้องกับ Power BI

    >[!NOTE]
    >หากต้องการ[ย้ายไปยังการผลิต](move-to-production.md) คุณจะต้องมี[ความจุ](embedded-capacity.md)

* **การขึ้นต่อกันของโค้ด**

    # <a name="net-core"></a>[.NET Core](#tab/net-core)
    
    * [.NET Core 3.1 SDK](https://dotnet.microsoft.com/download/dotnet-core) (หรือสูงกว่า)
    
    * เครื่องมือพัฒนาโปรแกรม (integrated development environment : IDE) เราขอแนะนำให้ใช้หนึ่งในรายการต่อไปนี้:
    
        * [Visual Studio](https://visualstudio.microsoft.com/)
    
        * [รหัส Visual Studio](https://code.visualstudio.com/)

    # <a name="net-framework"></a>[.NET Framework](#tab/net-framework)
    
    * [.NET Framework 4.8](https://dotnet.microsoft.com/download/dotnet-framework/)
    
    * [Visual Studio](https://visualstudio.microsoft.com/)

    # <a name="java"></a>[Java](#tab/java)
    
    * [JDK (หรือ JRE)](https://www.oracle.com/java/technologies/)
    
    * [Eclipse IDE](https://www.eclipse.org/downloads/packages/) - ตรวจสอบว่าคุณมี *Eclipse for Java EE Developers* (รุ่นสำหรับองค์กร)
    
    * [Apache Tomcat Binary Distributions](https://tomcat.apache.org/)
    
    # <a name="node-js"></a>[Node JS](#tab/node-js)
    
    * [.NET Framework 4.8](https://dotnet.microsoft.com/download/dotnet-framework/)
    
    * เครื่องมือพัฒนาโปรแกรม (integrated development environment : IDE) เราขอแนะนำให้ใช้หนึ่งในรายการต่อไปนี้:
    
        * [Visual Studio](https://visualstudio.microsoft.com/)
    
        * [รหัส Visual Studio](https://code.visualstudio.com/)
    
    # <a name="python"></a>[Python](#tab/python)
    
    * [Python 3](https://www.python.org/downloads/) (หรือสูงกว่า)
    
        >[!NOTE]
        >* หากคุณติดตั้ง *Python* เป็นครั้งแรก ให้เลือกตัวเลือก **เพิ่ม Python ไปยัง PATH** เพื่อเพิ่มการติดตั้งลงในตัวแปร `PATH`
        >* หากคุณติดตั้ง *Python* ไว้แล้วให้ตรวจสอบว่าตัวแปร `PATH` มีเส้นทางการติดตั้ง สำหรับข้อมูลเพิ่มเติม โปรดดู [Excursus: การตั้งค่าตัวแปรของสภาพแวดล้อม](https://docs.python.org/3/using/windows.html#excursus-setting-environment-variables) เอกสารประกอบ Python (ลิงก์นี้อ้างอิงถึง Python 3)
    
    * เครื่องมือพัฒนาโปรแกรม (integrated development environment : IDE) เราขอแนะนำให้ใช้หนึ่งในรายการต่อไปนี้:
    
        * [Visual Studio](https://visualstudio.microsoft.com/)
    
        * [รหัส Visual Studio](https://code.visualstudio.com/)
    
    ---

## <a name="method"></a>วิธีการ

หากต้องการสร้างแอปตัวอย่าง *การฝังตัวสำหรับลูกค้าของคุณ* ให้ทำตามขั้นตอนเหล่านี้:

1. [เลือกวิธีการรับรองความถูกต้องของคุณ](#step-1---select-your-authentication-method)

2. [ลงทะเบียนแอปพลิเคชัน Azure AD](#step-2---register-an-azure-ad-application)

3. [สร้างพื้นที่ทำงาน Power BI](#step-3---create-a-power-bi-workspace)

4. [สร้าง และเผยแพร่รายงาน Power BI](#step-4---create-and-publish-a-power-bi-report)

5. [รับค่าพารามิเตอร์การฝัง](#step-5---get-the-embedding-parameter-values)

6. [สิทธิ์การเข้าถึง API ของโครงร่างสำคัญของบริการ](#step-6---service-principal-api-access)
 
7. [เปิดใช้งานการเข้าถึงพื้นที่ทำงาน](#step-7---enable-workspace-access)

8. [ฝังตัวเนื้อหาของคุณ](#step-8---embed-your-content)

## <a name="step-1---select-your-authentication-method"></a>ขั้นตอนที่ 1 - เลือกวิธีการรับรองความถูกต้องของคุณ

โซลูชันแบบฝังตัวของคุณจะแตกต่างกันโดยขึ้นอยู่กับวิธีการรับรองความถูกต้องที่คุณเลือก ดังนั้นสิ่งสำคัญคือต้องเข้าใจความแตกต่างระหว่างวิธีการรับรองความถูกต้องและตัดสินใจว่าวิธีใดเหมาะสมกับโซลูชันของคุณมากที่สุด

ตารางด้านล่างนี้อธิบายความแตกต่างที่สำคัญบางประการระหว่างวิธีการรับรองความถูกต้องแบบ [โครงร่างสำคัญของบริการ](embed-service-principal.md) และ **ผู้ใช้หลัก**

|ข้อควรพิจารณา  |โครงร่างสำคัญของบริการ  |ผู้ใช้หลัก  |
|---------|---------|---------|
|กลไก     |[ออบเจ็กต์โครงร่างสำคัญของบริการ](/azure/active-directory/develop/app-objects-and-service-principals#service-principal-object)ของแอป Azure AD ของคุณช่วยให้ Azure AD สามารถรับรองความถูกต้องของแอปโซลูชันแบบฝังตัวของคุณกับ Power BI ได้        |แอป Azure AD ของคุณใช้ข้อมูลประจำตัว (ชื่อผู้ใช้และรหัสผ่าน) ของผู้ใช้ Power BI เพื่อรับรองความถูกต้องกับ Power BI         |
|ความปลอดภัย     |*โครงร่างสำคัญของบริการ* เป็นวิธีการรับรองความถูกต้องที่แนะนำของ Azure AD ถ้าคุณกำลังใช้โครงร่างสำคัญของบริการ *คุณสามารถรับรองความถูกต้องโดยใช้ *ข้อมูลลับของแอปพลิเคชัน* หรือ *ใบรับรอง*</br></br>บทช่วยสอนนี้อธิบายเฉพาะการใช้ *โครงร่างสำคัญของบริการ* ด้วย *ข้อมูลลับของแอปพลิเคชัน* หากต้องการฝังโดยใช้ *โครงร่างสำคัญของบริการ* และ *ใบรับรอง* โปรดดูบทความ [โครงร่างสำคัญของบริการด้วยใบรับรอง](embed-service-principal-certificate.md)         |วิธีการรับรองความถูกต้องนี้ไม่ได้รับการพิจารณาว่าปลอดภัยเท่ากับการใช้ *โครงร่างสำคัญของบริการ* เนื่องจากคุณต้องระมัดระวังข้อมูลประจำตัว *ผู้ใช้หลัก* (ชื่อผู้ใช้และรหัสผ่าน) ตัวอย่างเช่น คุณต้องไม่เปิดเผยในแอปพลิเคชันการฝังของคุณ และคุณควรเปลี่ยนรหัสผ่านบ่อย ๆ         |
|สิทธิ์ที่ได้รับมอบหมายของ Azure AD |ไม่จำเป็นต้องมี |*ผู้ใช้หลัก* ของคุณหรือผู้ดูแลระบบต้องให้ความยินยอมเพื่อให้แอปของคุณเข้าถึง [สิทธิ์](/azure/active-directory/develop/v2-permissions-and-consent) Power BI REST API (หรือที่เรียกว่าขอบเขต) ตัวอย่างเช่น *Report.ReadWrite All* |
|สิทธิ์การเข้าถึงบริการของ Power BI |คุณไม่สามารถเข้าถึงบริการ Power BI ด้วย *โครงร่างสำคัญของบริการ*|คุณสามารถเข้าถึงบริการ Power BI ด้วยข้อมูลประจำตัวของ *ผู้ใช้หลัก* ของคุณ|
|สิทธิ์การใช้งาน     |ไม่จำเป็นต้องมีสิทธิ์การใช้งาน Pro คุณสามารถใช้เนื้อหาจากพื้นที่ทำงานใดก็ได้ที่คุณเป็นสมาชิกหรือผู้ดูแลระบบ         |ต้องมีสิทธิ์การใช้งาน [Power BI Pro](../../admin/service-admin-purchasing-power-bi-pro.md)         |

## <a name="step-2---register-an-azure-ad-application"></a>ขั้นตอนที่ 2 - ลงทะเบียนแอปพลิเคชัน Azure AD

การลงทะเบียนแอปพลิเคชันของคุณด้วย Azure AD ช่วยให้คุณสามารถ:
> [!div class="checklist"]
>* สร้างข้อมูลประจำตัวสำหรับแอปของคุณ
>* อนุญาตให้แอปของคุณเข้าถึง [Power BI REST APIs](/rest/api/power-bi/)
>* ถ้าคุณกำลังใช้ *ผู้ใช้หลัก* - ให้ระบุ [สิทธิ์ Power BI REST](/azure/active-directory/develop/v2-permissions-and-consent) ของแอปของคุณ

[!INCLUDE[Register Azure AD app](../../includes/embed-tutorial-register-app.md)]

>[!NOTE]
>ก่อนที่จะลงทะเบียนแอปพลิเคชันของคุณ คุณจะต้องตัดสินใจว่าจะใช้วิธีการรับรองความถูกต้องใด *โครงร่างสำคัญของบริการ* หรือ *ผู้ใช้หลัก*

## <a name="step-3---create-a-power-bi-workspace"></a>ขั้นตอนที่ 3 - สร้างพื้นที่ทำงาน Power BI

[!INCLUDE[Create a Power BI workspace](../../includes/embed-tutorial-create-workspace.md)]

## <a name="step-4---create-and-publish-a-power-bi-report"></a>ขั้นตอนที่ 4 - สร้าง และเผยแพร่รายงาน Power BI

[!INCLUDE[Create a Power BI report](../../includes/embed-tutorial-create-report.md)]

## <a name="step-5---get-the-embedding-parameter-values"></a>ขั้นตอนที่ 5 -รับค่าพารามิเตอร์การฝัง

หากต้องการฝังเนื้อหาของคุณ คุณจะต้องขอรับค่าพารามิเตอร์บางอย่าง ตารางด้านล่างแสดงค่าที่จำเป็นและระบุว่าจะใช้ได้กับวิธีการรับรองความถูกต้อง *หลักของบริการ* หรือไม่วิธีการรับรองความถูกต้องของ *ผู้ใช้หลัก* หรือทั้งสองอย่าง

ก่อนที่คุณจะฝังเนื้อหาของคุณ ควรตรวจสอบให้แน่ใจว่าคุณมีค่าทั้งหมดที่แสดงอยู่ด้านล่าง ค่าบางอย่างจะแตกต่างกันขึ้นอยู่กับวิธีการรับรองความถูกต้องที่คุณกำลังใช้

|พารามิเตอร์   |โครงร่างสำคัญของบริการ   |ผู้ใช้หลัก  |
|-------------------|---|---|
|[ID ของไคลเอนต์](#client-id) |![นำไปใช้กับ](../../media/yes.png) |![นำไปใช้กับ](../../media/yes.png) |
|[รหัสพื้นที่ทำงาน](#workspace-id)     |![นำไปใช้กับ](../../media/yes.png) |![นำไปใช้กับ](../../media/yes.png) |
|[รหัสรายงาน](#report-id)           |![นำไปใช้กับ](../../media/yes.png) |![นำไปใช้กับ](../../media/yes.png) |
|[ข้อมูลลับไคลเอ็นต์](#client-secret) |![นำไปใช้กับ](../../media/yes.png) |![ไม่นำไปใช้](../../media/no.png) |
|[ID ผู้เช่า](#tenant-id)                 |![นำไปใช้กับ](../../media/yes.png) |![ไม่นำไปใช้](../../media/no.png) |
|[ชื่อผู้ใช้ Power BI](#power-bi-username-and-password)   |![ไม่นำไปใช้](../../media/no.png) |![นำไปใช้กับ](../../media/yes.png) |
|[รหัสผ่าน Power BI](#power-bi-username-and-password)   |![ไม่นำไปใช้](../../media/no.png) |![นำไปใช้กับ](../../media/yes.png) |

### <a name="client-id"></a>ID ของไคลเอนต์

>[!TIP]
>**นำไปใช้กับ:** ![นำไปใช้กับ](../../media/yes.png)โครงร่างสำคัญของบริการ![ นำไปใช้กับ](../../media/yes.png)ผู้ใช้หลัก

[!INCLUDE[Get the client ID](../../includes/embed-tutorial-client-id.md)]

### <a name="workspace-id"></a>ID พื้นที่ทำงาน

>[!TIP]
>**นำไปใช้กับ:** ![นำไปใช้กับ](../../media/yes.png)โครงร่างสำคัญของบริการ![ นำไปใช้กับ](../../media/yes.png)ผู้ใช้หลัก

[!INCLUDE[Get the workspace ID](../../includes/embed-tutorial-workspace-id.md)]

### <a name="report-id"></a>รหัสรายงาน

>[!TIP]
>**นำไปใช้กับ:** ![นำไปใช้กับ](../../media/yes.png)โครงร่างสำคัญของบริการ![ นำไปใช้กับ](../../media/yes.png)ผู้ใช้หลัก

[!INCLUDE[Get the report ID](../../includes/embed-tutorial-report-id.md)]

### <a name="client-secret"></a>ข้อมูลลับไคลเอ็นต์

>[!TIP]
>**นำไปใช้กับ:** ![นำไปใช้กับ](../../media/yes.png)โครงร่างสำคัญของบริการ![ ไม่นำไปใช้กับ](../../media/no.png)ผู้ใช้หลัก

[!INCLUDE[Get the client secret](../../includes/embed-tutorial-client-secret.md)]

### <a name="tenant-id"></a>ID ผู้เช่า

>[!TIP]
>**นำไปใช้กับ:** ![นำไปใช้กับ](../../media/yes.png)โครงร่างสำคัญของบริการ![ ไม่นำไปใช้กับ](../../media/no.png)ผู้ใช้หลัก

หากต้องการรับ GUID สำหรับ ID ผู้เช่า ให้ทำตามขั้นตอนเหล่านี้:

1. ลงชื่อเข้าใช้ใน [Microsoft Azure](https://ms.portal.azure.com/#allservices)

2. ค้นหา **การลงทะเบียนแอป** และเลือกลิงก์ **การลงทะเบียนแอป**

3. เลือกแอป Azure AD ที่คุณใช้สำหรับการฝังเนื้อหา Power BI ของคุณ

4. จากส่วน **ภาพรวม** ให้คัดลอก GUID สำหรับ **ID ของ Directory (ผู้เช่า)**

### <a name="power-bi-username-and-password"></a>ชื่อผู้ใช้และรหัสผ่าน Power BI

>[!TIP]
>**นำไปใช้กับ:** ![ไม่นำไปใช้กับ](../../media/no.png)โครงร่างสำคัญของบริการ![ นำไปใช้กับ](../../media/yes.png)ผู้ใช้หลัก

รับ *ชื่อผู้ใช้* และ *รหัสผ่าน* ของผู้ใช้ Power BI ที่คุณใช้เป็น **ผู้ใช้หลัก** ของคุณ ซึ่งเป็นผู้ใช้เดียวกับที่คุณใช้ในการสร้างพื้นที่ทำงานและอัปโหลดรายงานในบริการ Power BI

## <a name="step-6---service-principal-api-access"></a>ขั้นตอนที่ 6 - สิทธิ์การเข้าถึง API ของโครงร่างสำคัญของบริการ

>[!TIP]
>**นำไปใช้กับ:** ![นำไปใช้กับ](../../media/yes.png)โครงร่างสำคัญของบริการ![ ไม่นำไปใช้กับ](../../media/no.png)ผู้ใช้หลัก
>
>ขั้นตอนนี้จะเกี่ยวข้องก็ต่อเมื่อคุณใช้วิธีการรับรองความถูกต้องแบบ *โครงร่างสำคัญของบริการ* หากคุณกำลังใช้ *ผู้ใช้หลัก* ให้ข้ามขั้นตอนนี้และดำเนินการต่อด้วย [ขั้นตอนที่ 7 - เปิดใช้งานการเข้าถึงพื้นที่ทำงาน](#step-7---enable-workspace-access)

เพื่อให้แอป Azure AD สามารถเข้าถึงเนื้อหา Power BI และ API ได้ ผู้ดูแลระบบ Power BI จำเป็นต้องเปิดใช้งานการเข้าถึงบริการหลักในพอร์ทัลผู้ดูแลระบบของ Power BI หากคุณไม่ใช่ผู้ดูแลระบบของผู้เช่าของคุณ ให้แจ้งผู้ดูแลระบบของผู้เช่าเพื่อเปิดใช้งาน *การตั้งค่าผู้เช่า* ให้กับคุณ
        
1. ใน *บริการ Power BI* ให้เลือก **การตั้งค่า** > **การตั้งค่า** > **พอร์ทัลผู้ดูแลระบบ**
        
    :::image type="content" source="media/embed-sample-for-customers/admin-settings.png" alt-text="สกรีนช็อตที่แสดงตัวเลือกเมนูการตั้งค่าผู้ดูแลระบบในเมนูการตั้งค่าบริการ Power BI":::
        
2. เลือก **การตั้งค่าผู้เช่า** จากนั้นเลื่อนลงไปที่ส่วน **การตั้งค่าสำหรับนักพัฒนาซอฟต์แวร์**
        
3. ขยาย **อนุญาตให้โครงร่างสำคัญของบริการใช้ Power BI APIs** และเปิดใช้งานตัวเลือกนี้
        
    :::image type="content" source="media/embed-sample-for-customers/developer-settings.png" alt-text="สกรีนช็อตที่แสดงวิธีเปิดใช้งานตัวเลือกการตั้งค่าของนักพัฒนาในตัวเลือกเมนูการตั้งค่าผู้เช่าในบริการ Power BI":::
        
>[!NOTE]
>เมื่อใช้ *โครงร่างสำคัญของบริการ* ขอแนะนำให้จำกัดการเข้าถึงการตั้งค่าผู้เช่าโดยใช้ *กลุ่มความปลอดภัย* เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะนี้ ให้ดูส่วนเหล่านี้ในบทความ[โครงร่างสำคัญของบริการ](embed-service-principal.md):
> * [สร้างกลุ่มความปลอดภัย Azure AD](embed-service-principal.md#step-2---create-an-azure-ad-security-group)
>* [เปิดใช้งานการตั้งค่าการจัดการบริการ Power BI](embed-service-principal.md#step-3---enable-the-power-bi-service-admin-settings)

## <a name="step-7---enable-workspace-access"></a>ขั้นตอนที่ 7 - เปิดใช้งานการเข้าถึงพื้นที่ทำงาน

หากต้องการเปิดใช้งานการเข้าถึงแอป Azure AD ของคุณ เช่น รายงาน แดชบอร์ด และชุดข้อมูลในบริการ Power BI ให้เพิ่ม *โครงร่างสำคัญของบริการ* หรือ *ผู้ใช้หลัก* ในฐานะที่เป็น *สมาชิก* หรือ *ผู้ดูแลระบบ* ในพื้นที่ทำงานของคุณ

1. ลงชื่อเข้าใช้บริการ Power BI

2. เลื่อนไปยังพื้นที่ทำงานที่คุณต้องการเปิดใช้งานการเข้าถึง และจากเมนู **เพิ่มเติม** เลือก **การเข้าถึงพื้นที่ทำงาน**

    :::image type="content" source="media/embed-service-principal/workspace-access.png" alt-text="สกรีนช็อตแสดงปุ่มการเข้าถึงพื้นที่ทำงานในเมนูเพิ่มเติมของพื้นที่ทำงาน Power BI":::

3. ในบานหน้าต่าง **การเข้าถึง** ซึ่งขึ้นอยู่กับวิธีการรับรองความถูกต้องที่คุณใช้ ให้คัดลอก *โครงร่างสำคัญของบริการ* หรือ *ผู้ใช้หลัก* ไปยังกล่องข้อความ **ป้อนที่อยู่อีเมล**

    >[!NOTE]
    >ถ้าคุณกำลังใช้ *โครงร่างสำคัญของบริการ* ชื่อนี้เป็นชื่อที่คุณตั้งให้แอป Azure AD ของคุณ

4. เลือก **เพิ่ม**

## <a name="step-8---embed-your-content"></a>ขั้นตอนที่ 8 - ฝังเนื้อหาของคุณ

แอปพลิเคชันตัวอย่าง Power BI embedded ช่วยให้คุณสามารถสร้างแอป Power BI *การฝังตัวสำหรับลูกค้าของคุณ*

ทำตามขั้นตอนเหล่านี้เพื่อปรับเปลี่ยนแอปพลิเคชันตัวอย่าง *การฝังตัวสำหรับลูกค้าของคุณ* เพื่อฝังรายงาน Power BI ของคุณ  

[!INCLUDE[Embedding steps](../../includes/embed-tutorial-embedding-steps.md)]

4. เปิดหนึ่งในโฟลเดอร์เหล่านี้ ทั้งนี้ขึ้นอยู่กับภาษาที่คุณต้องการให้แอปพลิเคชันของคุณใช้:

    * .NET Core
    * เฟรมเวอร์ค .NET
    * Java
    * Node JS
    * Python

    >[!NOTE]
    >การฝังตัวสำหรับแอปพลิเคชันตัวอย่าง *ของลูกค้าของคุณ* สนับสนุนเฉพาะกรอบงานที่แสดงรายการข้างต้นเท่านั้น แอปพลิเคชันตัวอย่างการ *ตอบสนอง* สนับสนุนการ *[ฝังตัวสำหรับโซลูชันองค์กรของคุณ](embed-sample-for-your-organization.md)* เท่านั้น

5. เปิดโฟลเดอร์ **การฝังตัวสำหรับลูกค้าของคุณ**

# <a name="net-core"></a>[.NET Core](#tab/net-core)

6. เปิด *แอปตัวอย่างการฝังตัวสำหรับลูกค้าของคุณ* โดยใช้วิธีใดวิธีหนึ่งต่อไปนี้:

    * หากคุณกำลังใช้ [Visual Studio](https://visualstudio.microsoft.com/) ให้เปิดไฟล์ **AppOwnsData.sln**

    * ถ้าคุณกำลังใช้ [รหัส Visual Studio](https://code.visualstudio.com/)เปิดโฟลเดอร์ **AppOwnsData**

7. เปิด **appsettings.json**

8. ให้กรอกค่าพารามิเตอร์ต่อไปนี้ ทั้งนี้ขึ้นอยู่กับวิธีการรับรองความถูกต้องของคุณ:

    |พารามิเตอร์            |โครงร่างสำคัญของบริการ  |ผู้ใช้หลัก  |
    |---------------------|---------|---------|
    |`AuthenticationMode` |ServicePrincipal         |MasterUser         |
    |`ClientId`           |[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ         |[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ         |
    |`TenantId`           |[ID ผู้เช่า](#tenant-id)ของแอป Azure AD ของคุณ         |N/A         |
    |`PbiUsername`        |N/A         |ชื่อผู้ใช้ของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)         |
    |`PbiPassword`        |N/A         |รหัสผ่านของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)         |
    |`ClientSecret`       |[ข้อมูลลับไคลเอ็นต์](#client-secret)ของ Azure AD ของคุณ         |N/A         |
    |`WorkspaceId`        |ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)          |ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)         |
    |`ReportId`           |ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)            |ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)         |

9. เรียกใช้โครงการโดยการเลือกตัวเลือกที่เหมาะสม:

    * หากคุณกำลังใช้ **Visual Studio** ให้เลือก **IIS Express** (เล่น)

    * หากคุณกำลังใช้ **Visual Studio Code** ให้เลือก **เรียกใช้> เริ่มต้นการดีบัก**

# <a name="net-framework"></a>[.NET Framework](#tab/net-framework)

6. กำลังใช้ [Visual Studio](https://visualstudio.microsoft.com/) ให้เปิดไฟล์ **AppOwnsData.sln**

7. เปิด **Web.config**

8. ให้กรอกค่าพารามิเตอร์ต่อไปนี้ ทั้งนี้ขึ้นอยู่กับวิธีการรับรองความถูกต้องของคุณ:

    |พารามิเตอร์            |โครงร่างสำคัญของบริการ  |ผู้ใช้หลัก  |
    |---------------------|---------|---------|
    |`authenticationType` |ServicePrincipal         |MasterUser         |
    |`applicationId`           |[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ         |[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ         |
    |`workspaceId`        |ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)          |ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)         |
    |`reportId`           |ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)            |ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)         |
    |`pbiUsername`        |N/A         |ชื่อผู้ใช้ของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)         |
    |`pbiPassword`        |N/A         |รหัสผ่านของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)         |
    |`applicationSecret`       |[ข้อมูลลับไคลเอ็นต์](#client-secret)ของ Azure AD ของคุณ         |N/A         |
    |`tenant`           |[ID ผู้เช่า](#tenant-id)ของแอป Azure AD ของคุณ         |N/A         |

9. เรียกใช้โครงการโดยการเลือก **IIS Express** (เล่น)

# <a name="java"></a>[Java](#tab/java)

6. เปิด **Eclipse** และทำตามคำแนะนำที่อธิบายไว้ด้านล่าง

    >[!NOTE]
    >คำแนะนำสำหรับ *แอปตัวอย่างการฝังตัวสำหรับลูกค้าของคุณ* ด้วยภาษา Java โปรดดูที่ [Eclipse IDE สำหรับ Java EE Developers](https://www.eclipse.org/downloads/packages/) (รุ่นสำหรับองค์กร) หากคุณกำลังใช้แอปพลิเคชันอื่น คุณจะต้องตั้งค่าด้วยตนเอง

7. เพิ่มเซิร์ฟเวอร์ Tomcat ไปยัง Eclipse:

    a. เลือก **หน้าต่าง** > **แสดงมุมมอง** > **เซิร์ฟเวอร์**

    b. ในแท็บเซิร์ฟเวอร์ ให้เลือก **ไม่มีเซิร์ฟเวอร์ที่พร้อมใช้งาน คลิกที่ลิงก์นี้เพื่อสร้างเซิร์ฟเวอร์ใหม่**

    c. ในหน้าต่าง **กำหนดเซิร์ฟเวอร์ใหม่** ขยาย **Apache** และเลือกเซิร์ฟเวอร์ Tomcat ที่คุณใช้งานบนเครื่องของคุณ ตัวอย่างเช่น *เซิร์ฟเวอร์ Tomcat v9.0*

    d. เลือก **ถัดไป**

    e. ในหน้าต่าง **เซิร์ฟเวอร์ Tomcat** เลือก **เรียกดู** และไปที่โฟลเดอร์ที่มีเซิร์ฟเวอร์ Tomcat

    f. ในหน้าต่าง **เซิร์ฟเวอร์ Tomcat** ให้เลือก **JREs ที่ติดตั้ง**

    เช่น ในหน้าต่าง **JREs ที่ติดตั้ง** ให้เลือก *jre* ที่มีอยู่ แล้วเลือก **นำไปใช้และปิด**

    h. ในหน้าต่าง **เซิร์ฟเวอร์ Tomcat** ให้เลือก **เสร็จสิ้น** คุณจะเห็นเซิร์ฟเวอร์ Tomcat ในแท็บ *เซิร์ฟเวอร์*

8. เปิดโครงการใน Eclipse:

    >[!IMPORTANT]
    >Eclipse อาจประสบปัญหาหากชื่อพาธของคุณยาวเกินไป เพื่อหลีกเลี่ยงปัญหานี้ ให้ตรวจสอบว่าโฟลเดอร์ของแอปตัวอย่างของคุณไม่ได้ซ้อนกันมากเกินไปในโครงสร้างโฟลเดอร์ของเครื่องของคุณ

    a. เลือก **ไฟล์** จากนั้นเลือก **เปิดโครงการจากระบบไฟล์**

    b. ในหน้าต่าง **นำเข้าโครงการจากระบบไฟล์หรือที่เก็บถาวร** เลือก **Directory** และเปิดโฟลเดอร์ **AppOwnsData**

    c. เลือก **เสร็จสิ้น**

9. เพิ่มเซิร์ฟเวอร์ Tomcat ไปยังโครงการ:

    a. ในบานหน้าต่าง **ตัวต้นหาแพคเกจ** คลิกขวาที่ **AppOwnsData** และเลือก **คุณสมบัติ**

    b. ในหน้าต่าง **คุณสมบัติสำหรับ AppOwnesData** ให้เลือก **รันไทม์ที่กำหนดเป้าหมาย** จากนั้นเลือก **Apache Tomcat** การเลือกนี้จะรวมถึงเวอร์ชันของ *Apache ทขนาด* ที่คุณกำลังใช้งานตัวอย่างเช่น *Apache ทขนาด v 9.0*

    c. เลือก **นำไปใช้และปิด**

10. ระบุพารามิเตอร์ที่จำเป็น:

    a. ใน **ตัวต้นหาแพคเกจ** ขยายโครงการ **AppOwnsData**

    b. ขยาย **Java Resources**

    c. ขยาย **src**

    d. ขยาย **com.embedsample.appoensdata.config**

    e. เปิด **Config.java**

    f. ให้กรอกค่าพารามิเตอร์ต่อไปนี้ ทั้งนี้ขึ้นอยู่กับวิธีการรับรองความถูกต้องของคุณ:

    |พารามิเตอร์            |โครงร่างสำคัญของบริการ  |ผู้ใช้หลัก  |
    |---------------------|---------|---------|
    |`authenticationType` |ServicePrincipal         |MasterUser         |
    |`workspaceId`        |ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)          |ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)         |
    |`reportId`           |ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)            |ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)         | 
    |`clientId`           |[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ         |[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ         |
    |`pbiUsername`        |N/A         |ชื่อผู้ใช้ของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)         |
    |`pbiPassword`        |N/A         |รหัสผ่านของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)         |
    |`tenantId`           |[ID ผู้เช่า](#tenant-id)ของแอป Azure AD ของคุณ         |N/A         |
    |`appSecret`       |[ข้อมูลลับไคลเอ็นต์](#client-secret)ของ Azure AD ของคุณ         |N/A         |

11. เรียกใช้โครงการ

    a. ใน **ตัวต้นหาแพคเกจ** คลิกขวา **AppOwnesData**

    b. เลือก **เรียกใช้เป็น**  > **เรียกใช้บนเซิร์ฟเวอร์**

    c. ในหน้าต่าง **เรียกใช้บนเซิร์ฟเวอร์** ให้เลือก **เลือกเซิร์ฟเวอร์ที่มีอยู่** และเลือกเซิร์ฟเวอร์ *Tomcat*

    d. เลือก **เสร็จสิ้น**

# <a name="node-js"></a>[Node JS](#tab/node-js)

6. เปิดโฟลเดอร์ **แอปเป็นเจ้าของข้อมูล** โดยใช้ IDE ที่คุณต้องการ เราขอแนะนำให้ใช้หนึ่งในรายการต่อไปนี้:

    * [Visual Studio](https://visualstudio.microsoft.com/)

    * [รหัส Visual Studio](https://code.visualstudio.com/)

7. เปิดเทอร์มินัลและติดตั้งการขึ้นต่อกันที่จำเป็นโดยดำเนินการ: `npm install`

8. ขยายโฟลเดอร์ **กำหนดค่า** และเปิด **config.json**

9. ให้กรอกค่าพารามิเตอร์ต่อไปนี้ ทั้งนี้ขึ้นอยู่กับวิธีการรับรองความถูกต้องของคุณ:

    |พารามิเตอร์            |โครงร่างสำคัญของบริการ  |ผู้ใช้หลัก  |
    |---------------------|---------|---------|
    |`authenticationMode` |ServicePrincipal         |MasterUser         |
    |`clientId`           |[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ         |[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ         |
    |`workspaceId`        |ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)          |ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)         |
    |`reportId`           |ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)            |ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)         |
    |`pbiUsername`        |N/A         |ชื่อผู้ใช้ของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)         |
    |`pbiPassword`        |N/A         |รหัสผ่านของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)         |
    |`clientSecret`       |[ข้อมูลลับไคลเอ็นต์](#client-secret)ของ Azure AD ของคุณ         |N/A         |
    |`tenantId`           |[ID ผู้เช่า](#tenant-id)ของแอป Azure AD ของคุณ         |N/A         |

10. เรียกใช้โครงการโดยทำดังต่อไปนี้:

    a. ในเทอร์มินัล IDE ให้ดำเนินการ `npm start`

    b. เปิดแท็บใหม่ในเบราว์เซอร์ของคุณและนำทางไปยัง `http://localhost:5300`

# <a name="python"></a>[Python](#tab/python)

6. เปิด **PowerShell** หรือ **Command Prompt**

7. ตรวจสอบว่าคุณอยู่ในโฟลเดอร์ **Python** > **การฝังสำหรับลูกค้าของคุณ** และไฟล์ **requirements.txt** อยู่ในโฟลเดอร์และเรียกใช้ `pip3 install -r requirements.txt`

8. เปิดโฟลเดอร์ **แอปเป็นเจ้าของข้อมูล** โดยใช้ IDE ที่คุณต้องการ เราขอแนะนำให้ใช้หนึ่งในรายการต่อไปนี้:

    * [Visual Studio](https://visualstudio.microsoft.com/)

    * [รหัส Visual Studio](https://code.visualstudio.com/)

9. เปิด **config.py**

10. ให้กรอกค่าพารามิเตอร์ต่อไปนี้ ทั้งนี้ขึ้นอยู่กับวิธีการรับรองความถูกต้องของคุณ:

    |พารามิเตอร์            |โครงร่างสำคัญของบริการ  |ผู้ใช้หลัก  |
    |---------------------|---------|---------|
    |`AUTHENTICATION_MODE` |ServicePrincipal         |MasterUser         |
    |`WORKSPACE_ID`        |ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)          |ID ของพื้นที่ทำงานที่มีรายงานแบบฝังตัวของคุณ โปรดดู [ID พื้นที่ทำงาน](#workspace-id)         |
    |`REPORT_ID`           |ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)            |ID ของรายงานที่คุณกำลังฝัง โปรดดูที่ [ID ของรายงาน](#report-id)         |
    |`TENANT_ID`           |[ID ผู้เช่า](#tenant-id)ของแอป Azure AD ของคุณ         |N/A         |
    |`CLIENT_ID`           |[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ         |[ID ไคลเอ็นต์](#client-id)ของแอป Azure AD ของคุณ         |
    |`CLIENT_SECRET`       |[ข้อมูลลับไคลเอ็นต์](#client-secret)ของ Azure AD ของคุณ         |N/A         |
    |`POWER_BI_USER`        |N/A         |ชื่อผู้ใช้ของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)         |
    |`POWER_BI_PASS`        |N/A         |รหัสผ่านของ *ผู้ใช้หลัก* ของคุณ โปรดดูที่ [ชื่อผู้ใช้และรหัสผ่าน Power BI](#power-bi-username-and-password)         |

11. บันทึกไฟล์

12. เรียกใช้โครงการโดยทำดังต่อไปนี้:

    a. ใน **PowerShell** หรือ **Command Prompt** ให้ไปที่โฟลเดอร์ **Python**  > **การฝังสำหรับลูกค้าของคุณ** > **AppOwnesData** และดำเนินการ `flask run`

    b. เปิดแท็บใหม่ในเบราว์เซอร์ของคุณและนำทางไปยัง `http://localhost:5300`

---

## <a name="developing-your-application"></a>การพัฒนาแอปพลิเคชันของคุณ

หลังจากกำหนดค่าและเรียกใช้แอปพลิเคชันตัวอย่าง *การฝังตัวสำหรับลูกค้าของคุณ* คุณสามารถเริ่มต้นการพัฒนาแอปพลิเคชันของคุณเองได้

[!INCLUDE[Move to production](../../includes/embed-tutorial-production.md)]

## <a name="next-steps"></a>ขั้นตอนถัดไป

> [!div class="nextstepaction"]
>[ย้ายไปยังการผลิต](move-to-production.md)

>[!div class="nextstepaction"]
>[ฝังตัวสำหรับองค์กรของคุณ](embed-sample-for-your-organization.md)

> [!div class="nextstepaction"]
>[รายงานที่มีการแบ่งหน้าแบบฝังตัวสำหรับลูกค้าของคุณ](embed-paginated-reports-customers.md)

> [!div class="nextstepaction"]
>[รายงานกิจกรรมแบบฝังสำหรับองค์กรของคุณ](embed-paginated-reports-organization.md)

>[!div class="nextstepaction"]
>[ถามชุมชน Power BI](https://community.powerbi.com/)