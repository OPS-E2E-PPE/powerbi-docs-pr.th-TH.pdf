---
title: ฝังเนื้อหาในแอปพลิเคชันการวิเคราะห์แบบฝังตัว Power BI ของคุณเพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นสําหรับองค์กรของคุณ
description: เรียนรู้วิธีการรวม Power BI เข้ากันกับแอปพลิเคชันของคุณโดยใช้ซอฟต์แวร์การวิเคราะห์แบบฝังตัว, เครื่องมือการวิเคราะห์แบบฝังตัวหรือเครื่องมือข่าวกรองธุรกิจแบบฝังตัว เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: tutorial
ms.custom: seodec18
ms.date: 12/17/2020
ms.openlocfilehash: fbae63597ecf4ff36783ad83785f87c242359f90
ms.sourcegitcommit: 2e81649476d5cb97701f779267be59e393460097
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 02/02/2021
ms.locfileid: "99494991"
---
# <a name="tutorial-embed-power-bi-content-using-a-sample-embed-for-your-organization-application"></a>บทช่วยสอน: ฝังเนื้อหา Power BI โดยใช้ตัวอย่างฝังตัวสำหรับแอปพลิเคชัน *สำหรับองค์กรของคุณ*

Power BI embedded analytics ช่วยให้คุณสามารถฝังเนื้อหา Power BI เช่นรายงานแดชบอร์ดและไทล์ลงในแอปพลิเคชันของคุณ

ในบทช่วยสอนนี้ คุณจะเรียนรู้วิธีการ:

>[!div class="checklist"]
>* ตั้งค่าสภาพแวดล้อมแบบฝังตัวของคุณ
>* กำหนดค่า *ฝังตัวสำหรับองค์กรของคุณ* (หรือที่เรียกว่า *ผู้ใช้เป็นเจ้าของข้อมูล*) แอปพลิเคชันตัวอย่าง

หากต้องการใช้แอปพลิเคชันของคุณผู้ใช้ของคุณจะต้องลงชื่อเข้าใช้ Power BI

โซลูชันฝังตัวสำหรับองค์กรของคุณมักจะใช้โดยวิสาหกิจและองค์กรขนาดใหญ่ และมีไว้สำหรับผู้ใช้ภายใน

## <a name="code-sample-specifications"></a>ข้อมูลจำเพาะตัวอย่างของโค้ด

บทช่วยสอนนี้รวมถึงคำแนะนำสำหรับการกำหนดค่าฝังตัวสำหรับแอปพลิเคชันตัวอย่าง *องค์กรของคุณ* ในหนึ่งในกรอบงานต่อไปนี้:

* .NET Framework
* .NET Core
* การตอบสนอง TypeScript

>[!NOTE]
>*.Net Core* และตัวอย่าง *.NET Framework* จะอนุญาตให้ผู้ใช้สามารถดูแดชบอร์ด Power BI, รายงานหรือไทล์ที่พวกเขามีสิทธิ์เข้าถึงในบริการของ Power BI ตัวอย่างการ *ตอบสนอง TypeScript* ช่วยให้คุณสามารถฝังหนึ่งรายงานที่ผู้ใช้ปลายทางของคุณมีสิทธิ์เข้าถึงบริการของ Power BI ได้

ตัวอย่างโค้ดรองรับเบราว์เซอร์ต่อไปนี้:

* Microsoft Edge
* Google Chrome
* Mozilla Firefox

## <a name="prerequisites"></a>สิ่งที่จำเป็นต้องมี

ก่อนที่คุณจะเริ่มต้นบทช่วยสอนนี้ ให้ตรวจสอบว่าคุณมีการขึ้นต่อกันทั้งของ Power BI และโค้ดที่แสดงรายการด้านล่าง:

* **การขึ้นต่อกันของ Power BI**

    * [ผู้เช่า Azure Active Directory](create-an-azure-active-directory-tenant.md) ของคุณเอง

    * หนึ่งในสิทธิ์การใช้งานต่อไปนี้:

        * [Power BI Pro](../../admin/service-admin-purchasing-power-bi-pro.md)

        * [Premium ต่อผู้ใช้ (PPU)](../../admin/service-premium-per-user-faq.md)

    >[!NOTE]
    >หากต้องการ [ย้ายไปยังการผลิต](move-to-production.md) คุณจะต้องมีการกำหนดค่าต่อไปนี้อย่างน้อยหนึ่ง:
    >* ผู้ใช้ทั้งหมดที่มีใบอนุญาต Pro
    >* ผู้ใช้ทั้งหมดที่มีใบอนุญาต PPU
    >* ความ[จุ](embedded-capacity.md) การกำหนดค่านี้อนุญาตให้ผู้ใช้ทุกคนได้รับสิทธิ์อนุญาตฟรี

* **การขึ้นต่อกันของโค้ด**

    # <a name="net-core"></a>[.NET Core](#tab/net-core)

    * [.NET Core 3.1 SDK](https://dotnet.microsoft.com/download/dotnet-core) (หรือสูงกว่า)
    
    * เครื่องมือพัฒนาโปรแกรม (integrated development environment : IDE) เราขอแนะนำให้ใช้หนึ่งในรายการต่อไปนี้:

        * [Visual Studio](https://visualstudio.microsoft.com/)

        * [รหัส Visual Studio](https://code.visualstudio.com/)

    # <a name="net-framework"></a>[.NET Framework](#tab/net-framework)

    * [.NET Framework 4.8](https://dotnet.microsoft.com/download/dotnet-framework/)
    
    * [Visual Studio](https://visualstudio.microsoft.com/)

    # <a name="react-typescript"></a>[การตอบสนอง TypeScript](#tab/react)

    * ตัวแก้ไขข้อความ

    * Terminal บรรทัดคำสั่ง (หรือ PowerShell)

---

## <a name="method"></a>วิธีการ

เมื่อต้องการสร้างการ *ฝังตัวสำหรับแอปตัวอย่างองค์กรของคุณ* ให้ทำตามขั้นตอนเหล่านี้:

1. [ลงทะเบียนแอปพลิเคชัน Azure AD](#step-1---register-an-azure-ad-application)

2. [สร้างพื้นที่ทำงาน Power BI](#step-2---create-a-power-bi-workspace)

3. [สร้าง และเผยแพร่รายงาน Power BI](#step-3---create-and-publish-a-power-bi-report)

4. [รับค่าพารามิเตอร์การฝัง](#step-4---get-the-embedding-parameter-values)

5. [ฝังตัวเนื้อหาของคุณ](#step-5---embed-your-content)

## <a name="step-1---register-an-azure-ad-application"></a>ขั้นตอนที่ 1-ลงทะเบียนแอปพลิเคชัน Azure AD

การลงทะเบียนแอปพลิเคชันของคุณด้วย Azure AD ช่วยให้คุณสร้างข้อมูลประจำตัวสำหรับแอปของคุณ

[!INCLUDE[Register Azure AD app](../../includes/embed-tutorial-register-app.md)]

## <a name="step-2---create-a-power-bi-workspace"></a>ขั้นตอนที่ 2-สร้างพื้นที่ทำงานของ Power BI

[!INCLUDE[Create a Power BI workspace](../../includes/embed-tutorial-create-workspace.md)]

## <a name="step-3---create-and-publish-a-power-bi-report"></a>ขั้นตอนที่ 3-สร้างและเผยแพร่รายงาน Power BI

[!INCLUDE[Create a Power BI report](../../includes/embed-tutorial-create-report.md)]

## <a name="step-4---get-the-embedding-parameter-values"></a>ขั้นตอนที่ 4-รับค่าพารามิเตอร์การฝัง

หากต้องการฝังเนื้อหาของคุณคุณจะต้องได้รับค่าพารามิเตอร์บางอย่าง ค่าพารามิเตอร์ที่คุณต้องการจะขึ้นอยู่กับภาษาของแอปพลิเคชันตัวอย่างที่คุณต้องการใช้ ตารางด้านล่างแสดงค่าพารามิเตอร์ที่จำเป็นสำหรับแต่ละตัวอย่าง

|พารามิเตอร์  |.NET Core  |เฟรมเวอร์ค .NET  |การตอบสนอง TypeScript |
|---------|---------|---------|---------|
|[ID ของไคลเอนต์](#client-id) |![นำไปใช้กับ](../../media/yes.png) |![นำไปใช้กับ](../../media/yes.png)         |![นำไปใช้กับ](../../media/yes.png) |
|[ข้อมูลลับไคลเอ็นต์](#workspace-id) |![นำไปใช้กับ](../../media/yes.png) |![นำไปใช้กับ](../../media/yes.png) |![ไม่นำไปใช้](../../media/no.png) |
|[รหัสพื้นที่ทำงาน]() |![ไม่นำไปใช้](../../media/no.png) |![ไม่นำไปใช้](../../media/no.png) |![นำไปใช้กับ](../../media/yes.png) |
|[รหัสรายงาน]() |![ไม่นำไปใช้](../../media/no.png) |![ไม่นำไปใช้](../../media/no.png) |![นำไปใช้กับ](../../media/yes.png) |

### <a name="client-id"></a>ID ของไคลเอนต์

>[!TIP]
>**นำไปใช้กับ:** ![ นำ ](../../media/yes.png) ไปใช้กับ ... NET Core ![ ใช้กับ ... ](../../media/yes.png) NET Framework ![ จะนำไป ](../../media/yes.png) ใช้ การตอบสนอง TypeScript

[!INCLUDE[Get the client ID](../../includes/embed-tutorial-client-id.md)]

### <a name="client-secret"></a>ข้อมูลลับไคลเอ็นต์

>[!TIP]
>**นำไปใช้กับ:** ![ นำ ](../../media/yes.png) ไปใช้กับ ... NET Core ![ ใช้กับ ... ](../../media/yes.png) ไม่มี ![ การใช้งาน ](../../media/no.png) NET Framework การตอบสนอง TypeScript

[!INCLUDE[Get the client secret](../../includes/embed-tutorial-client-secret.md)]

### <a name="workspace-id"></a>ID พื้นที่ทำงาน

>[!TIP]
>**นำไปใช้กับ:** ![ ไม่ ](../../media/no.png) นำไปใช้กับ ... ไม่มี ![ การใช้งานหลักสุทธิกับ ... ](../../media/no.png) NET Framework ![ จะนำไป ](../../media/yes.png) ใช้ การตอบสนอง TypeScript

[!INCLUDE[Get the workspace ID](../../includes/embed-tutorial-workspace-id.md)]

### <a name="report-id"></a>รหัสรายงาน

>[!TIP]
>**นำไปใช้กับ:** ![ ไม่ ](../../media/no.png) นำไปใช้กับ ... ไม่มี ![ การใช้งานหลักสุทธิกับ ... ](../../media/no.png) NET Framework ![ จะนำไป ](../../media/yes.png) ใช้ ReactTypeScript

[!INCLUDE[Get the report ID](../../includes/embed-tutorial-report-id.md)]

## <a name="step-5---embed-your-content"></a>ขั้นตอนที่ 5 - ฝังเนื้อหาของคุณ

แอปพลิเคชันตัวอย่าง Power BI embedded ช่วยให้คุณสามารถสร้างแบบฝังตัวสำหรับแอป power BI *สำหรับองค์กรของคุณ*

ทำตามขั้นตอนเหล่านี้เพื่อปรับเปลี่ยนการฝังตัวสำหรับแอปพลิเคชันตัวอย่าง *องค์กรของคุณ* เพื่อฝังรายงาน Power BI ของคุณ

[!INCLUDE[Embedding steps](../../includes/embed-tutorial-embedding-steps.md)]

4. เปิดหนึ่งในโฟลเดอร์เหล่านี้ ทั้งนี้ขึ้นอยู่กับภาษาที่คุณต้องการให้แอปพลิเคชันของคุณใช้:

    * .NET Core
    * เฟรมเวอร์ค .NET
    * การตอบสนอง-TS

    >[!NOTE]
    >การฝังตัวสำหรับแอปพลิเคชันตัวอย่าง *ขององค์กรของคุณ* สนับสนุนเฉพาะกรอบงานที่แสดงรายการข้างต้นเท่านั้น แอปพลิเคชันตัวอย่างของ *Java*, *Node.js* และ *ไพธอน* สนับสนุนการ *[ฝังตัวสำหรับโซลูชันสำหรับลูกค้าของคุณ](embed-sample-for-customers.md)* เท่านั้น

# <a name="net-core"></a>[.NET Core](#tab/net-core)

### <a name="configure-your-azure-ad-app"></a>กำหนดค่าแอป Azure AD ของคุณ

[!INCLUDE[Configure the Azure AD authentication options](../../includes/embed-tutorial-org-azure-ad-app.md)]

5. ในการ *กำหนดค่าแพลตฟอร์ม* เปิดแพลตฟอร์ม *เว็บ* ของคุณและในส่วน **URIs เปลี่ยนเส้น** `https://localhost:5000/signin-oidc` ทางเพิ่ม

    > [!NOTE]
    >ถ้าคุณไม่มีแพลตฟอร์ม **เว็บ** เลือก **เพิ่มแพลตฟอร์ม** และในหน้าต่าง *กำหนดค่าแพลตฟอร์ม* เลือก **เว็บ**

6. บันทึกการเปลี่ยนแปลงของคุณ

:::image type="content" source="media/embed-sample-for-your-organization/azure-ad-net-configurations.png" alt-text="ภาพหน้าจอที่แสดงการกำหนดค่าการรับรองความถูกต้องของแอป Azure AD รวมถึงการเปลี่ยนเส้นทางเว็บ U R ฉันสำหรับตัวอย่างแอป .NET core":::

### <a name="configure-the-sample-embedding-app"></a>กำหนดค่าแอปตัวอย่างที่ฝัง

1. เปิดการ **ฝังตัวสำหรับโฟลเดอร์องค์กรของคุณ**

2. เปิด *แอปตัวอย่างแบบฝังตัวสำหรับองค์กรของคุณ* โดยใช้วิธีใดวิธีหนึ่งต่อไปนี้:

    * ถ้าคุณกำลังใช้ [Visual Studio](https://visualstudio.microsoft.com/)เปิดไฟล์ **sln UserOwnsData**

    * ถ้าคุณกำลังใช้ [รหัส Visual Studio](https://code.visualstudio.com/)เปิดโฟลเดอร์ **UserOwnsData**

3. เปิด **appsettings.js** และเติมค่าพารามิเตอร์ต่อไปนี้:

    * `ClientId`-ใช้ GUID [ID ไคลเอ็นต์](#client-id)

    * `ClientSecret` -ใช้ข้อมูล [ลับของไคลเอ็นต์](#client-secret)

### <a name="run-the-sample-app"></a>เรียกใช้แอปตัวอย่าง

1. เรียกใช้โครงการโดยการเลือกตัวเลือกที่เหมาะสม:

    * หากคุณกำลังใช้ **Visual Studio** ให้เลือก **IIS Express** (เล่น)

    * หากคุณกำลังใช้ **Visual Studio Code** ให้เลือก **เรียกใช้> เริ่มต้นการดีบัก**

[!INCLUDE[The embedded application sample app interface](../../includes/embed-tutorial-org-sample-app.md)]

# <a name="net-framework"></a>[.NET Framework](#tab/net-framework)

### <a name="configure-your-azure-ad-app"></a>กำหนดค่าแอป Azure AD ของคุณ

[!INCLUDE[Configure the Azure AD authentication options](../../includes/embed-tutorial-org-azure-ad-app.md)]

5. ในการ *กำหนดค่าแพลตฟอร์ม* กำหนดค่าต่อไปนี้:

    1. ในแพลตฟอร์ม *เว็บ* ของคุณในส่วน **URIs เปลี่ยนเส้น** ทาง `https://localhost:44300/` เพิ่ม

        > [!NOTE]
        >ถ้าคุณไม่มีแพลตฟอร์ม **เว็บ** เลือก **เพิ่มแพลตฟอร์ม** และในหน้าต่าง *กำหนดค่าแพลตฟอร์ม* เลือก **เว็บ**
    
    2. ในการให้ *สิทธิ์โดยปริยายและโฟลว์ไฮบริด* เปิดใช้งานตัวเลือก **โทเค็น ID**
    
6. บันทึกการเปลี่ยนแปลงของคุณ

:::image type="content" source="media/embed-sample-for-your-organization/azure-ad-framework-configurations.png" alt-text="ภาพหน้าจอที่แสดงการกำหนดค่าการรับรองความถูกต้องของแอป Azure AD รวมถึงการเปลี่ยนเส้นทางเว็บ U R I และตัวเลือกโทเค็นการเข้าถึงที่เลือกสำหรับตัวอย่างแอป .NET framework":::

### <a name="configure-the-sample-embedding-app"></a>กำหนดค่าแอปตัวอย่างที่ฝัง

1. เปิดการ **ฝังตัวสำหรับโฟลเดอร์องค์กรของคุณ**

2. การใช้ [Visual Studio](https://visualstudio.microsoft.com/)เปิดไฟล์ **sln UserOwnsData**

3. เปิด **Web.config** และเติมค่าพารามิเตอร์ต่อไปนี้:

    * `clientId`-ใช้ GUID [ID ไคลเอ็นต์](#client-id)

    * `clientSecret` -ใช้ข้อมูล [ลับของไคลเอ็นต์](#client-secret)

### <a name="run-the-sample-app"></a>เรียกใช้แอปตัวอย่าง

1. เรียกใช้โครงการโดยการเลือก **IIS Express** (เล่น)

[!INCLUDE[The embedded application sample app interface](../../includes/embed-tutorial-org-sample-app.md)]

# <a name="react-typescript"></a>[การตอบสนอง TypeScript](#tab/react)

### <a name="configure-your-azure-ad-app"></a>กำหนดค่าแอป Azure AD ของคุณ

[!INCLUDE[Configure the Azure AD authentication options](../../includes/embed-tutorial-org-azure-ad-app.md)]

5. ในการ *กำหนดค่าแพลตฟอร์ม* กำหนดค่าแพลตฟอร์ม **เว็บ** ของคุณดังนี้:

    1. ในการ **เปลี่ยนเส้นทาง URIs** เพิ่ม `https://localhost:3000` และเลือก **กำหนดค่า**

        > [!NOTE]
        >ถ้าคุณไม่มีแพลตฟอร์ม **เว็บ** เลือก **เพิ่มแพลตฟอร์ม** และในหน้าต่าง *กำหนดค่าแพลตฟอร์ม* เลือก **เว็บ**

    2. ในการให้ *สิทธิ์โดยปริยายและโฟลว์ไฮบริด* เปิดใช้งานทั้งสองตัวเลือก:
        * **โทเค็นการเข้าถึง**
        * **โทเค็น ID**
    
6. บันทึกการเปลี่ยนแปลงของคุณ

:::image type="content" source="media/embed-sample-for-your-organization/azure-ad-react-configurations.png" alt-text="ภาพหน้าจอที่แสดงการกำหนดค่าการรับรองความถูกต้องของแอป Azure AD รวมถึงการเปลี่ยนเส้นทางเว็บ U R ฉันตั้งค่าสำหรับ localhost ๓๐๐๐":::

### <a name="configure-the-sample-embedding-app"></a>กำหนดค่าแอปตัวอย่างที่ฝัง

1. เปิดโฟลเดอร์แบบ **ฝังตัวสำหรับองค์กรของคุณ**  >  **UserOwnsData**  >  **src**

2. การใช้ตัวแก้ไขข้อความเปิดไฟล์ **Config** และเติมค่าพารามิเตอร์ต่อไปนี้:

    * `clientId`-ใช้ GUID [ID ไคลเอ็นต์](#client-id)

    * `workspaceId` -ใช้ [ID พื้นที่ทำงาน](#client-secret)

    * `reportId` -ใช้ [ID รายงาน](#report-id)

3. บันทึกไฟล์

### <a name="run-the-sample-app"></a>เรียกใช้แอปตัวอย่าง

1. เปิด terminal ในและนำทางไป **ฝังสำหรับองค์กรของคุณ**  >  **UserOwnsData**

2. ติดตั้งการอ้างอิงที่จำเป็นโดยการดำเนินการคำสั่งต่อไปนี้:

   `npm install`

3. เรียกใช้แอปพลิเคชันโดยการดำเนินการคำสั่งต่อไปนี้:

   `npm run start`

    >[!NOTE]
    >ในระหว่างการลงชื่อเข้าใช้ครั้งแรกของคุณคุณจะได้รับพร้อมท์เพื่ออนุญาตให้สิทธิ์ Azure AD สำหรับแอป

---

## <a name="developing-your-application"></a>การพัฒนาแอปพลิเคชันของคุณ

หลังจากกำหนดค่าและเรียกใช้แอปพลิเคชันตัวอย่าง *การฝังตัวสำหรับลูกค้าของคุณ* คุณสามารถเริ่มต้นการพัฒนาแอปพลิเคชันของคุณเองได้

[!INCLUDE[Move to production](../../includes/embed-tutorial-production.md)]

## <a name="next-steps"></a>ขั้นตอนถัดไป

> [!div class="nextstepaction"]
>[ย้ายไปยังการผลิต](move-to-production.md)

>[!div class="nextstepaction"]
>[ฝังสำหรับลูกค้าของคุณ](embed-sample-for-customers.md)

> [!div class="nextstepaction"]
>[รายงานที่มีการแบ่งหน้าแบบฝังตัวสำหรับลูกค้าของคุณ](embed-paginated-reports-customers.md)

> [!div class="nextstepaction"]
>[รายงานกิจกรรมแบบฝังสำหรับองค์กรของคุณ](embed-paginated-reports-organization.md)

>[!div class="nextstepaction"]
>[ถามชุมชน Power BI](https://community.powerbi.com/)