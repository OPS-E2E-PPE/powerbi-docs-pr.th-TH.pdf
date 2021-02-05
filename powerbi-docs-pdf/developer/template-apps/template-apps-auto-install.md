---
title: ทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตสำหรับลูกค้าของคุณเป็นแบบอัตโนมัติ
description: เรียนรู้เกี่ยวกับการทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตเป็นแบบอัตโนมัติ
author: paulinbar
ms.author: painbar
ms.topic: conceptual
ms.service: powerbi
ms.subservice: powerbi-developer
ms.date: 11/23/2020
ms.openlocfilehash: 0852fcb2c932680f6c20aeee94a89c68f473e46d
ms.sourcegitcommit: 1cad78595cca1175b82c04458803764ac36e5e37
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/19/2021
ms.locfileid: "98565731"
---
# <a name="automated-configuration-of-a-template-app-installation"></a>การกำหนดค่าของการติดตั้งแอปเทมเพลตแบบอัตโนมัติ

แอปเทมเพลตเป็นวิธีที่ยอดเยี่ยมสำหรับลูกค้าในการเริ่มรับข้อมูลเชิงลึกจากข้อมูลของตน แอปเทมเพลตช่วยให้แอปเหล่านี้ทำงานได้อย่างรวดเร็วโดยการเชื่อมต่อกับข้อมูล แอปเทมเพลตจะให้รายงานที่สร้างไว้ล่วงหน้าแก่ลูกค้าซึ่งพวกเขาสามารถปรับแต่งได้ตามต้องการ

ลูกค้ามักไม่คุ้นเคยกับรายละเอียดของวิธีการเชื่อมต่อกับข้อมูลของพวกเขา การให้รายละเอียดเหล่านี้ในขณะที่พวกเขาติดตั้งแอปเทมเพลต จะสร้างความยุ่งยากให้

หากคุณเป็นผู้ให้บริการข้อมูลและได้สร้างแอปเทมเพลตเพื่อช่วยให้ลูกค้าเริ่มต้นใช้งานข้อมูลในบริการของคุณ คุณสามารถทำให้พวกเขาติดตั้งแอปเทมเพลตของคุณได้ง่ายขึ้น คุณสามารถทำให้การกำหนดค่าพารามิเตอร์ของแอปเทมเพลตเป็นแบบอัตโนมัติ เมื่อลูกค้าลงชื่อเข้าใช้พอร์ทัลของคุณ พวกเขาจะเลือกลิงก์พิเศษที่คุณเตรียมไว้ ลิงก์นี้:

- เปิดการทำงานอัตโนมัติ ซึ่งรวบรวมข้อมูลที่ต้องการ
- กำหนดค่าพารามิเตอร์แอปเทมเพลตไว้ล่วงหน้า
- เปลี่ยนเส้นทางลูกค้าไปยังบัญชี Power BI ของพวกเขาซึ่งพวกเขาสามารถติดตั้งแอปได้

สิ่งที่พวกเขาต้องทำคือเลือก **ติดตั้ง** และรับรองความถูกต้องเทียบกับแหล่งข้อมูลของพวกเขา เท่านี้ก็เรียบร้อย!

ประสบการณ์ของลูกค้านี้แสดงเป็นภาพประกอบไว้ที่นี่

![ภาพประกอบของประสบการณ์ผู้ใช้กับแอปพลิเคชันที่มีการติดตั้งอัตโนมัติ](media/template-apps-auto-install/high-level-flow.png)

บทความนี้อธิบายถึงโฟลว์พื้นฐาน ข้อกำหนดเบื้องต้น และขั้นตอนหลักและ API ที่คุณต้องการเพื่อทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตเป็นแบบอัตโนมัติ หากคุณต้องการเพียงแค่เข้าไปและเริ่มต้นใช้งาน คุณสามารถข้ามไปที่[บทช่วยสอน](template-apps-auto-install-tutorial.md) ซึ่งคุณสามารถทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตเป็นแบบอัตโนมัติได้โดยใช้แอปพลิเคชันตัวอย่างง่าย ๆ ที่เราเตรียมไว้ซึ่งใช้ฟังก์ชัน Azure

## <a name="basic-flow"></a>โฟลว์พื้นฐาน

โฟลว์พื้นฐานของการทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตเป็นแบบอัตโนมัติเป็นดังนี้:

1. ผู้ใช้ลงชื่อเข้าใช้พอร์ทัลของ ISV และเลือกลิงก์ที่ให้มา การดำเนินการนี้จะเริ่มใช้โฟลว์อัตโนมัติ พอร์ทัลของ ISV เตรียมการกำหนดค่าเฉพาะของผู้ใช้ในลำดับขั้นนี้

1. ISV ได้รับโทเค็น *เฉพาะแอป* ตาม [องค์ประกอบหลักของบริการ (โทเค็นเฉพาะแอป)](../embedded/embed-service-principal.md) ที่ลงทะเบียนในผู้เช่าของ ISV

1. ด้วยการใช้ [Power BI REST APIs](/rest/api/power-bi/) ISV จะสร้าง *ตั๋วการติดตั้ง* ซึ่งมีการกำหนดค่าพารามิเตอร์เฉพาะของผู้ใช้ตามที่ ISV เตรียมไว้

1. ISV เปลี่ยนเส้นทางผู้ใช้ไปยัง Power BI โดยใช้วิธีการเปลี่ยนเส้นทาง ```POST``` ที่มีตั๋วการติดตั้ง

1. ผู้ใช้จะถูกเปลี่ยนเส้นทางไปยังบัญชี Power BI ของพวกเขาด้วยตั๋วการติดตั้งและได้รับพร้อมท์แจ้งให้ติดตั้งแอปเทมเพลต เมื่อผู้ใช้เลือก **ติดตั้ง** แอปเทมเพลตจะถูกติดตั้งสำหรับพวกเขา

>[!Note]
>แม้ว่าค่าพารามิเตอร์จะถูกกำหนดโดย ISV ในกระบวนการสร้างตั๋วการติดตั้ง แต่ข้อมูลประจำตัวที่เกี่ยวข้องกับแหล่งข้อมูลจะถูกจัดเตรียมโดยผู้ใช้ในขั้นตอนสุดท้ายของการติดตั้งเท่านั้น การดำเนินการนี้จะป้องกันไม่ให้มีการเปิดเผยข้อมูลประจำตัวกับบุคคลที่สาม และทำให้มั่นใจได้ว่าการเชื่อมต่อระหว่างผู้ใช้และแหล่งข้อมูลของแอปเทมเพลตมีความปลอดภัย

## <a name="prerequisites"></a>สิ่งที่จำเป็นต้องมี

หากต้องการให้ประสบการณ์การติดตั้งที่กำหนดไว้ล่วงหน้าสำหรับแอปแม่แบบ คุณจำเป็นต้องมีข้อกำหนดเบื้องต้นต่อไปนี้:

* สิทธิการใช้งาน Power BI Pro หากคุณยังไม่ได้สมัคร Power BI Pro ให้ [สมัครทดลองใช้งานฟรี](https://powerbi.microsoft.com/pricing/) ก่อนที่คุณจะเริ่ม
* ตั้งค่าผู้เช่า Azure Active Directory (Azure AD) ของคุณเอง สำหรับคำแนะนำเกี่ยวกับวิธีการตั้งค่า โปรดดูที่[สร้างผู้เช่า Azure AD](../embedded/create-an-azure-active-directory-tenant.md)
* **องค์ประกอบหลักของบริการ (โทเค็นเฉพาะแอป)** ที่ลงทะเบียนในผู้เช่าก่อนหน้านี้ สำหรับข้อมูลเพิ่มเติม โปรดดู[ฝังเนื้อหา Power BI ด้วยองค์ประกอบหลักของบริการและข้อมูลลับของแอปพลิเคชัน](../embedded/embed-service-principal.md) ตรวจสอบให้แน่ใจว่าได้ลงทะเบียนแอปพลิเคชันเป็นแอปแบบ **เว็บแอปพลิเคชันฝั่งเซิร์ฟเวอร์** คุณลงทะเบียนแอปพลิเคชันเว็บฝั่งเซิร์ฟเวอร์เพื่อสร้างเป็นความลับของแอปพลิเคชัน จากขั้นตอนนี้คุณต้องบันทึก *ID แอปพลิเคชัน* (ID ไคลเอ็นต์) และ *ข้อมูลลับของแอปพลิเคชัน* (ข้อมูลลับของไคลเอ็นต์) สำหรับขั้นตอนในภายหลัง
* **แอปเทมเพลต** แบบกำหนดพารามิเตอร์ที่พร้อมสำหรับการติดตั้ง ต้องสร้างแอปเทมเพลตในผู้เช่าเดียวกันกับที่คุณลงทะเบียนแอปพลิเคชันของคุณใน Azure AD สำหรับข้อมูลเพิ่มเติม โปรดดูที่[เคล็ดลับแอปเทมเพลต](../../connect-data/service-template-apps-tips.md)หรือ[สร้างแอปเทมเพลตใน Power BI](../../connect-data/service-template-apps-create.md) จากแอปเทมเพลต คุณต้องจดข้อมูลต่อไปนี้สำหรับขั้นตอนต่อไป:
     * *App ID*, *Package Key* และ *Owner ID* ตามที่ปรากฏใน URL การติดตั้งในตอนท้ายของกระบวนการ [กำหนดคุณสมบัติของแอปเทมเพลต](../../connect-data/service-template-apps-create.md#define-the-properties-of-the-template-app)เมื่อสร้างแอปขึ้นแล้ว คุณยังสามารถรับลิงก์เดียวกันได้โดยเลือกที่ **รับลิงก์** ในบานหน้าต่าง [การจัดการนำไปใช้งานจริง](../../connect-data/service-template-apps-create.md#manage-the-template-app-release)ของแอปเทมเพลต
    * *ชื่อพารามิเตอร์* ตามที่กำหนดไว้ในชุดข้อมูลของแอปเทมเพลต ชื่อพารามิเตอร์เป็นสตริงที่คำนึงถึงตัวพิมพ์เล็กและใหญ่ และยังสามารถดึงชื่อดังกล่าวได้จากแท็บ **การตั้งค่าพารามิเตอร์** เมื่อคุณ [กำหนดคุณสมบัติของแอปเทมเพลต](../../connect-data/service-template-apps-create.md#define-the-properties-of-the-template-app) หรือจากการตั้งค่าชุดข้อมูลใน Power BI

    >[!NOTE]
    >คุณสามารถทดสอบแอปพลิเคชันการติดตั้งที่กำหนดค่าไว้ล่วงหน้าบนแอปเทมเพลตของคุณได้หากแอปเทมเพลตพร้อมสำหรับการติดตั้งแม้ว่าจะยังไม่พร้อมใช้งานแบบสาธารณะใน AppSource ก็ตาม เพื่อให้ผู้ใช้ภายนอกผู้เช่าของคุณสามารถใช้แอปพลิเคชันการติดตั้งอัตโนมัติเพื่อติดตั้งแอปเทมเพลตของคุณได้ แอปเทมเพลตจะต้องพร้อมใช้งานแบบสาธารณะใน [Power BI Apps marketplace](https://app.powerbi.com/getdata/services) ก่อนที่คุณจะแจกจ่ายแอปเทมเพลตของคุณโดยใช้แอปพลิเคชันการติดตั้งอัตโนมัติที่คุณกำลังสร้างขึ้น อย่าลืมเผยแพร่ไปยัง[ศูนย์พันธมิตร](/azure/marketplace/partner-center-portal/create-power-bi-app-offer)ก่อน

## <a name="main-steps-and-apis"></a>ขั้นตอนหลักและ Api

ขั้นตอนหลักสำหรับการทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตและ API ที่คุณต้องการเป็นแบบอัตโนมัติมีอธิบายไว้ในส่วนต่อไปนี้ แม้ว่าขั้นตอนส่วนใหญ่จะดำเนินการด้วย [Power BI REST APIs](/rest/api/power-bi/) แต่ตัวอย่างโค้ดที่อธิบายที่นี้ใช้ .NET SDK

## <a name="step-1-create-a-power-bi-client-object"></a>ขั้นตอนที่ 1: สร้างออบเจ็กต์ไคลเอนต์ Power BI

เมื่อคุณใช้งาน Power BI REST API คุณจำเป็นต้องได้รับ *โทเค็นการเข้าถึง* สำหรับ [องค์ประกอบหลักของบริการ](../embedded/embed-service-principal.md)ของคุณจาก Azure AD คุณต้องได้รับ[โทเค็นการเข้าถึง Azure AD](../embedded/get-azuread-access-token.md#access-token-for-non-power-bi-users-app-owns-data) สำหรับแอปพลิเคชัน Power BI ของคุณก่อนที่คุณจะเรียกใช้ [Power BI REST API](/rest/api/power-bi/)
เมื่อต้องการสร้าง Power BI Client ด้วยโทเค็นการเข้าถึง คุณจำเป็นต้องสร้างออบเจ็กต์ไคลเอ็นต์ Power BI ซึ่งช่วยให้คุณสามารถโต้ตอบกับ [Power BI REST APIs](/rest/api/power-bi/) ได้ คุณสร้างวัตถุไคลเอ็นต์ Power BI ได้โดยการคลุม **AccessToken** ด้วยวัตถุ **Microsoft.Rest.TokenCredentials**

```csharp
using Microsoft.IdentityModel.Clients.ActiveDirectory;
using Microsoft.Rest;
using Microsoft.PowerBI.Api.V2;

var tokenCredentials = new TokenCredentials(authenticationResult.AccessToken, "Bearer");

// Create a Power BI client object. It's used to call Power BI APIs.
using (var client = new PowerBIClient(new Uri(ApiUrl), tokenCredentials))
{
    // Your code goes here.
}
```

## <a name="step-2-create-an-install-ticket"></a>ขั้นตอนที่ 2: สร้างตั๋วการติดตั้ง

สร้างตั๋วการติดตั้งซึ่งใช้เมื่อคุณเปลี่ยนเส้นทางผู้ใช้ของคุณไปยัง Power BI API ที่ใช้สำหรับการดำเนินการนี้คือ **CreateInstallTicket** API
* [แอปเทมเพลต CreateInstallTicket](/rest/api/power-bi/templateapps/createinstallticket)

ตัวอย่างวิธีการสร้างตั๋วการติดตั้งสำหรับการติดตั้งและการกำหนดค่าแอปเทมเพลตสามารถดูได้จากไฟล์ [InstallTemplateApp / InstallAppFunction.cs](https://github.com/microsoft/Template-apps-examples/blob/master/Developer%20Samples/Automated%20Install%20Azure%20Function/InstallTemplateAppSample/InstallTemplateApp/InstallAppFunction.cs) ใน [แอปพลิเคชันตัวอย่าง](https://github.com/microsoft/Template-apps-examples/tree/master/Developer%20Samples/Automated%20Install%20Azure%20Function/InstallTemplateAppSample)


ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการใช้ **CreateInstallTicket** REST API ของแอปเทมเพลต
```csharp
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

// Create Install Ticket Request.
InstallTicket ticketResponse = null;
var request = new CreateInstallTicketRequest()
{
    InstallDetails = new List<TemplateAppInstallDetails>()
    {
        new TemplateAppInstallDetails()
        {
            AppId = Guid.Parse(AppId),
            PackageKey = PackageKey,
            OwnerTenantId = Guid.Parse(OwnerId),
            Config = new TemplateAppConfigurationRequest()
            {
                Configuration = Parameters
                                    .GroupBy(p => p.Name)
                                    .ToDictionary(k => k.Key, k => k.Select(p => p.Value).Single())
            }
        }
    }
};

// Issue the request to the REST API using .NET SDK.
InstallTicket ticketResponse = await client.TemplateApps.CreateInstallTicketAsync(request);
```

## <a name="step-3-redirect-users-to-power-bi-with-the-ticket"></a>ขั้นตอนที่ 3: เปลี่ยนเส้นทางผู้ใช้ไปยัง Power BI ด้วยตั๋ว

หลังจากคุณสร้างตั๋วการติดตั้งแล้ว คุณจะใช้ตั๋วดังกล่าวเพื่อเปลี่ยนเส้นทางผู้ใช้ของคุณไปยัง Power BI เพื่อดำเนินการติดตั้งและการกำหนดค่าแอปเทมเพลตต่อไป คุณใช้วิธีการเปลี่ยนเส้นทาง ```POST``` ไปยัง URL การติดตั้งของแอปเทมเพลต ด้วยตั๋วการติดตั้งในเนื้อความของคำขอ

มีวิธีการเปลี่ยนเส้นทางโดยใช้คำขอ ```POST``` ที่จัดทำเป็นเอกสารมากมาย การเลือกอย่างใดอย่างหนึ่งขึ้นอยู่กับสถานการณ์และวิธีการที่ผู้ใช้ของคุณโต้ตอบกับพอร์ทัลหรือบริการของคุณ

ตัวอย่างแบบง่ายนี้ ที่ส่วนใหญ่ใช้เพื่อวัตถุประสงค์ในการทดสอบ ใช้ฟอร์มที่มีเขตข้อมูลที่ซ่อนอยู่ซึ่งจะส่งตัวเองโดยอัตโนมัติเมื่อโหลด

```javascript
<html>
    <body onload='document.forms["form"].submit()'>
        <!-- form method is POST and action is the app install URL -->
        <form name='form' action='https://app.powerbi.com/....' method='post' enctype='application/json'>
            <!-- value should be the new install ticket -->
            <input type='hidden' name='ticket' value='H4sI....AAA='>
        </form>
    </body>
</html>
```

ตัวอย่างต่อไปนี้ของการตอบสนองของ[แอปพลิเคชันตัวอย่าง](https://github.com/microsoft/Template-apps-examples/tree/master/Developer%20Samples/Automated%20Install%20Azure%20Function/InstallTemplateAppSample)เก็บตั๋วการติดตั้งและเปลี่ยนเส้นทางผู้ใช้ไปยัง Power BI โดยอัตโนมัติ การตอบสนองสำหรับฟังก์ชัน Azure นี้เป็นแบบฟอร์มการส่งด้วยตนเองโดยอัตโนมัติแบบเดียวกับที่เราเห็นในตัวอย่าง HTML ก่อนหน้า

```csharp
...
    return new ContentResult() { Content = RedirectWithData(redirectUrl, ticket.Ticket), ContentType = "text/html" };
}

...

public static string RedirectWithData(string url, string ticket)
{
    StringBuilder s = new StringBuilder();
    s.Append("<html>");
    s.AppendFormat("<body onload='document.forms[\"form\"].submit()'>");
    s.AppendFormat("<form name='form' action='{0}' method='post' enctype='application/json'>", url);
    s.AppendFormat("<input type='hidden' name='ticket' value='{0}' />", ticket);
    s.Append("</form></body></html>");
    return s.ToString();
}
```

>[!Note]
>แม้ว่าจะมีวิธีการหลากหลายในการใช้เบราว์เซอร์ ```POST``` เปลี่ยนเส้นทาง แต่คุณควรใช้วิธีที่ปลอดภัยที่สุดเสมอซึ่งขึ้นอยู่กับความต้องการและข้อจำกัดของบริการของคุณ โปรดจำไว้ว่ารูปแบบการเปลี่ยนเส้นทางที่ไม่ปลอดภัยบางรูปแบบอาจส่งผลให้ผู้ใช้หรือบริการของคุณพบปัญหาด้านความปลอดภัย

## <a name="step-4-move-your-automation-to-production"></a>ขั้นตอนที่ 4: ย้ายการทำงานโดยอัตโนมัติของคุณไปยังการผลิต

เมื่อการทำงานโดยอัตโนมัติที่คุณออกแบบไว้พร้อมแล้ว อย่าลืมย้ายไปยังการผลิต

## <a name="next-steps"></a>ขั้นตอนถัดไป

* ลองดู[บทช่วยสอน](template-apps-auto-install-tutorial.md)ของเราซึ่งใช้ฟังก์ชัน Azure อย่างง่ายเพื่อทำให้การกำหนดค่าการติดตั้งแอปเทมเพลตเป็นแบบอัตโนมัติ
* มีคำถามเพิ่มเติมหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)